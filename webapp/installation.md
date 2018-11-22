# Installation



## Pré-requis

Pour installer et faire fonctionner l'application il faut :

- **PHP7** et pouvoir le lancer dans un terminal
- **[Composer](https://getcomposer.org/)** 
- **[Node.js et npm](https://nodejs.org)**

 

## Installation de symfony

Cloner le projet git `git clone git@github.com:chloecorfmat/into-the-woods-webapp.git` 

`composer install` pour télécharger les dépendances

`php bin/console server:start` pour démarrer le serveur de développement.

Génerer la base de données avec `php bin/console doctrine:schema:update --force` 

**Après chaque mise à jour du dépot git il faut relancer un  `composer install`pour installer les nouvelles dépendances** 

## Créer un compte Super Admin

L'accès aux fonctionnalités d'administration est limité aux Super Administrateurs. Pour créer un compte Super Admin sans passer par un formulaire (nottament à l'installation de l'application) on utilise la commande `php bin/console superadmin:create`

Cette commande va permettre de préciser les informations d'un compte et de la créer avec les droits adéquats.

## Configurer PHPStorm

Pour utiliser PHPUnit dans PHPStorm :

- **Run** > **Edit configurations** 
- Cliquer sur **+**  > **PHPUnit**  
- Dans le champ **Directory** choisir le fichier **PHPUnit** dans le répertoire **vendor/bin/phpunit** 
