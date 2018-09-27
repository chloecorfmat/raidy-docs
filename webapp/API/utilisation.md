# Utilisation de l'API

L'API **Into The Woods** est une API REST interrogeable via des requêtes HTTP. 

Ces requêtes exploitent différents verbes HTTP qui sont liées à différentes actions :

- **GET** : récupération d'informations
- **POST** : Créer une entité
- **PUT** : Remplacer une entité
- **PATCH** : Mettre à jour une entité
- **DELETE** : Supprimer une entité



Afin de communiquer des données à l'API il est recommandé d'utiliser le format **JSON** dans le corps de la requête.



 ```json
{
	"login":test,
	"password":"azerty"
}
 ```

*Exemple de données lors de l'authentification*

Le type de retour de l'API est également le **JSON**.



## Utiliser le jeton

Une fois l'utilisateur authentifié l'API lui retourne un jeton qu'il soit stocker et utiliser à chaque requête sur l'API.

Pour passer ce jeton à l'API il faut ajouter un champ `X-Auth-Token` dans l'entête de la requête HTTP. Ce champ prend pour valeur le jeton.

Si la requête ne contient pas ce jeton le serveur répond avec une erreur HTTP **500**.



## Valeurs de retour

Lorsqu'une réponse ne contient pas de données ou dans le cas d'une erreur l'API retourne un objet JSON contenant deux champs : 

- **code** : code de retour HTTP

- **message** : message associé


```json
{
	"code":500,
	"message":"Invalid authentication token"
}
```

*Exemple de valeur de retour*



