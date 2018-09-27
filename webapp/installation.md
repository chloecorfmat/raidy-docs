# Installation

Cloner le projet git `git clone git@github.com:chloecorfmat/into-the-woods-webapp.git` 

`composer install` pour télécharger les dépendances

`php bin/console server:start` pour démarrer le serveur de développement.



**Après chaque mise à jour du dépot git il faut relancer un  `composer install`pour installer les nouvelles dépendances** 



## Configurer PHPStorm

Pour utiliser PHPUnit dans PHPStorm :

- **Run** > **Edit configurations** 
- Cliquer sur **+**  > **PHPUnit**  
- Dans le champ **Directory** choisir le fichier **PHPUnit** dans le répertoire **vendor/bin/phpunit** 