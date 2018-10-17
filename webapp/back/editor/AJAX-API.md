# API AJAX

L'editeur de cartes a besoin de communiquer avec le serveur via des requêtes HTTP. Il n'a cependant pas besoin d'utiliser l'authentification de l'API car il utilise le session id de la page.



## Déclarer des routes d'API

La déclaration de routes d'API AJAX se fait via les annontations **Routes** standard. Il faut cependant déclarer la méthode HTTP à utiliser.

```php
@Route("/organizer/raid/{raidId}/track/{trackId}", name="editTrack", methods={"PATCH"})
```



## AjaxAPIController

Pour simplifier le développement de routes un type de controleur spécifique a été mis en place : l'**AjaxAPIController**.

Pour créer un nouveau controleur d'API pour l'éditeur on peut le faire étendre **AjaxAPIController** .

Cela permet d'utiliser les méthodes : 

- **buildJSONStatus(code, message)** : retourne un objet **Response** avec un code HTTP particulier et contenant une chaine JSON de statut. Cette méthode prend en paramètres le **code** de statut HTTP et un **message** textuel. 

```json
{"code":404, "message":"Not Found"}
```

- **buildJSONReturn(code, data)** : retourne un objet **Response** contenant des données. Cette méthode prend en paramètres  le **code** de statut HTTP et les données à envoyer.



