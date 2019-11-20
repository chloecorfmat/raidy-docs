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
- Les extensions curl et php_curl doivent être installée et activée.



## Installation

### Installation de Symfony, de la base de données et du serveur mail

  * Installer le code livré dans le répertoire de votre choix, généralement le dossier `/www/html` de votre serveur apache.

  * Dupliquer le fichier `app/config/parameters.yml.dist` et le nommer `app/config/parameters.yml` : `cp app/config/parameters.yml.dist app/config/parameters.yml`
  * Dupliquer le fichier `app/config/config.yml.dist` et le nommer `app/config/config.yml` : `cp app/config/config.yml.dist app/config/config.yml`
  * Compléter la valeur du paramètre : fos_user.from_email.address
  * Dupliquer le fichier `app/config/config_prod.yml.dist` et le nommer `app/config/config_prod.yml` : `cp app/config/config_prod.yml.dist app/config/config_prod.yml`
  * Compléter et/ou modifier le fichier en fonction des besoins.

#### Base de données

  * Créer une base de données **MySQL** en utilisant l'encodage **utf8_general_ci**  et reporter les informations de connexion dans le fichier `app/config/parameters.yml`:

```yaml
parameters:
    database_host: 127.0.0.1 #Adresse du serveur de base de données
    database_port: ~ #Port du serveur de base de données
    database_name: 'into-the-woods' #Nom de la base de données
    database_user: 'itw' #Utilisateur
    database_password: 'itw' #Mot de passe
```

  * Exécuter la commande `composer install` pour télécharger les dépendances

  * Génerer la base de données avec `php bin/console doctrine:schema:update --force`

#### Service mail 

L'application permet d'envoyer des mails. Il est cependant nécessaire de configurer l'accès à un compte de messagerie au préalable. 

  * Ouvrir le fichier `app/config/parameters.yml` : `cp app/config/parameters.yml.dist app/config/parameters.yml`
  * Reporter les informations de connexion dans le fichier, sous la partie liée au à la base de données :
```yaml
    mailer_transport: smtp #Transport pour l'envoi des mails
    mailer_encryption: tls #Chiffrage 
    mailer_port: 587 #Port utilisé
    mailer_host: smtps.enssat.fr #Hôte
    mailer_user: raidy@enssat.fr #Adresse mail de l'émetteur
    mailer_password: monmotdepasse #Mot de passe de l'émetteur
```

  * Les adresses d'envoi et de réception doivent également être configurées. Pour cela : 
    * Ouvrir le fichier `app/config/config_prod.yml`
    * Reporter les informations suivantes dans la section app :
```yaml
app:
    mail:
        from: "raidy@enssat.fr" #Adresse d'envoi de mail
        reply_to: "raidy_reply_to@enssat.fr" #Adresse de réception de mail
```

  * Exécuter la commande `composer update` pour mettre à jour les dépendances

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

  * Si l'URL n'est pas racine, il faut modifier le fichier webpack.config.js pour l'adapter à l'url du projet : 
  
```javascript
    .setOutputPath('web/build/')
    // public path used by the web server to access the output path
    .setPublicPath('/build')
    // only needed for CDN's or sub-directory deploy
    .setManifestKeyPrefix('build/')
</VirtualHost>

```

  * A la racine du projet

  * Installer les dépendances avec la commande `npm install`

  * Générer les feuilles de styles et les scripts avec la commande `gulp`

  * Générer les composants Vue.js avec la commance `npm run prod`
  
### Les fichiers uploadés

Selon la configuration du serveur, il peut être nécessaire de créer les dossiers suivants. 

* web/uploads/raids
* web/uploads/sporttypes
* web/uploads/tracks/gpx
* web/uploads/competitors

C'est dans ces dossiers que seront stockés les images et fichiers uploadés avec l'application Raidy.

Si les images ne sont pas stockées dans le dossier web, il est important de modifier les chemins dans le fichier `app/config/config_prod.yml.dist`

### La console Symfony

La console Symfony peut être utilisée pour vider les caches, avoir des informations sur l'environnement... Par défaut, 
elles agissent sur l'environnement de développement (dev). Pour agir sur l'environnement de production, il faut préciser
l'option --env="prod" à la suite de la commande.

__Par exemples :__
  
```bash
    php bin/console about --env=prod
    php bin/console cache:clear --env=prod
```

