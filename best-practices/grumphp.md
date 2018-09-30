# GrumPHP

GrumPHP permet d'automatiser certaines tâches. 

Nous l'utiliserons pour vérifier que les standards de code de Symfony sont bien respectés.

Pour cela, il faut utiliser la commande : 
```
grump run
```


Il existe également un fixer qui permet de ne pas corriger toutes les erreurs à la main. 
Pour le lancer, il faut utiliser la commande :
```
./vendor/bin/php-cs-fixer fix src --rules=@Symfony
```
