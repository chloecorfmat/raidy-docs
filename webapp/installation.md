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



**Après chaque mise à jour du dépot git il faut relancer un  `composer install`pour installer les nouvelles dépendances** 



## Configurer PHPStorm

Pour utiliser PHPUnit dans PHPStorm :

- **Run** > **Edit configurations** 
- Cliquer sur **+**  > **PHPUnit**  
- Dans le champ **Directory** choisir le fichier **PHPUnit** dans le répertoire **vendor/bin/phpunit** 