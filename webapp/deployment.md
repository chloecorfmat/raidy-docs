# Déploiement de l'application Web en production

Afin de faire fonctionner l'application web Raidy il convient de suivre la procédure ci-dessous. Il est fortement conseillé d'utiliser un serveur sous Linux.

Les serveurs de pré-production utilisaient une distribution Linux Ubuntu 18.04, il est conseillé d'utiliser une distribution similaire. Ce document détaille l'installation sur ce type d'infrastructure.



## Prérequis

Pour installer et faire fonctionner l'application, il faut :

- **PHP 7.2**
- Un serveur de base de données **MySQL** 
- **[Composer](https://getcomposer.org/)** 
- **[Node.js et npm](https://nodejs.org)**
- Un serveur web - apache de préférence



## Installation

### Installation de Symfony et de la base de données

  * Installer le code livré dans le répertoire de votre choix, généralement le dossier `/www/html` de votre serveur apache.

  * Dupliquer le fichier `app/config/parameters.yml.dist` et le nommer `app/config/parameters.yml` : `cp app/config/parameters.yml.dist app/config/parameters.yml`

  * Créer une base de données **MySQL** en utilisant l'encodage **utf8_general_ci**  et reporter les informations de connexion dans le fichier `app/config/parameters.yml`:

```yaml
parameters:
    database_host: 127.0.0.1 #Adresse du serveur de base de données
    database_port: ~ #Port du serveur de base de données
    database_name: 'into-the-woods' #Nom de la base de données
    database_user: 'itw' #Utilisateur
    database_password: 'itw' #Mot de passe
    mailer_transport: smtp
    mailer_encryption: tls
    mailer_port: 587
    mailer_host: smtps.enssat.fr
    mailer_user: ccorfmat@enssat.fr
    mailer_password: tom_mdp
    secret: ThisTokenIsNotSoSecretChangeIt
```

  * Exécuter la commande `composer install` pour télécharger les dépendances
  
  * Exécuter les migrations `php bin/console doctrine:migrations:migrate`

  * Génerer la base de données avec `php bin/console doctrine:schema:update --force` 

### Configuration d'Apache

Afin de rediriger les utilisateurs vers l'application il convient de configurer le serveur Apache. Pour ce faire, créer un fichier `/etc/apache2/sites-available/into-the-woods.conf` et utiliser le configuration de base ci-dessous.

  * Remplacer le nom de domaine, le port, les noms des fichiers de logs et le répertoire d'hébergement en fonction de votre installation.

```xml
<VirtualHost *:80>
    ServerName raidy.fr
    
    DocumentRoot /var/www/html/into-the-woods-webapp/web
    <Directory /var/www/html/into-the-woods-webapp/web>
        AllowOverride All
        Order Allow,Deny
        Allow from All
    </Directory>

    ErrorLog /var/log/apache2/itw_error.log
    CustomLog /var/log/apache2/itw_access.log combined
    
RewriteEngine on
RewriteCond %{SERVER_NAME} = raidy.fr
RewriteRule ^ https://%{SERVER_NAME}%{REQUEST_URI} [END,NE,R=permanent]
</VirtualHost>

```

  * Activer la configuration : `a2ensite into-the-woods.conf`

  * Redémarrer le serveur Apache : `service apache2 restart`

**Attention l'utilisateur Linux executant le serveur Apache doit pouvoir écrire dans les répertoires /var/logs et /var/cache**

### Génération des feuilles de styles et des scripts

L'application utilise l'écosystème Node.js pour générer les feuilles de styles et les scripts nécessaires au bon fonctionnement du site.

  * Se rendre à la racine du projet

  * Installer les dépendances avec la commande `npm install`
  
  * Générer le code vuejs avec la commande `npm run dev`

  * Générer les feuilles de styles et les scripts avec la commande `gulp`








