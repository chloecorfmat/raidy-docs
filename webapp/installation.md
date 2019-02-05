# Installation en environnement de développement



## Prérequis

Pour installer et faire fonctionner l'application il faut :

- **PHP-7.2** et pouvoir le lancer dans un terminal
- Un serveur de base de données **MySQL** 
- **[Composer](https://getcomposer.org/)** 
- **[Node.js et npm](https://nodejs.org)**

 

## Installation de symfony

1. Cloner le projet git `git clone git@github.com:chloecorfmat/into-the-woods-webapp.git` 

2. Créer une base de données et reporter les informations de connexion dans le fichier `app/config/parameters.yml`

3. `composer install` pour télécharger les dépendances

4. `php bin/console server:run` pour démarrer le serveur de développement.

5. Génerer la base de données avec `php bin/console doctrine:schema:update --force` 

6. L'application permet d'envoyer des mails. Il est cependant nécessaire de configurer l'accès à un compte de messagerie au préalable. 

  * Ouvrir le fichier `app/config/parameters.yml` : `cp app/config/parameters.yml.dist app/config/parameters.yml`
  * Reporter les informations de connexion dans le fichier, sous la partie liée au à la base de données :
```yaml
    mailer_transport: smtp #Transport pour l'envoi des mails
    mailer_encryption: tls #Cryptage 
    mailer_port: 587 #Port utilisé
    mailer_host: smtps.enssat.fr #Hôte
    mailer_user: raidy@enssat.fr #Adresse mail de l'émetteur
    mailer_password: monmotdepasse #Mot de passe de l'émetteur
```

  * Les adresses d'envoi et de réception doivent également être configurées. Pour cela : 
    * Ouvrir le fichier `app/config/config_dev.yml`
    * Reporter les informations suivantes dans la section app :
```yaml
app:
            mail:
                 from: "raidy@enssat.fr" #Adresse d'envoi de mail
                 reply_to: "raidy_reply_to@enssat.fr" #Adresse de réception de mail
```

  * Exécuter la commande `composer update` pour mettre à jour les dépendances

**Après chaque mise à jour du dépot git il faut relancer un  `composer install` pour installer les nouvelles dépendances** 


## Créer un compte Super Admin

L'accès aux fonctionnalités d'administration est limité aux Super Administrateurs. Pour créer un compte Super Admin sans passer par un formulaire (nottament à l'installation de l'application) on utilise la commande `php bin/console superadmin:create`

Cette commande va permettre de préciser les informations d'un compte et de la créer avec les droits adéquats.


## Configurer PHPStorm

Pour utiliser PHPUnit dans PHPStorm :

- **Run** > **Edit configurations** 
- Cliquer sur **+**  > **PHPUnit**  
- Dans le champ **Directory** choisir le fichier **PHPUnit** dans le répertoire **vendor/bin/phpunit** 
