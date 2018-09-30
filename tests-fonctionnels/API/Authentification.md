# Tests fonctionnels : Authentification à l'API



## Authentification réussie

###  Situation de départ

En tant qu'utilisateur de l'API, sans jeton d'authentification, je souhaite m'authentifier auprès de l'API pour récupérer un jeton.

### Déroulement 

1. J'emet une requête HTTP POST à l'adresse : `/api/auth-tokens` avec comme corps de requête une chaine JSON listant le login et le mot de passe d'un utilisateur existant

   ```json
   {
   	"login":test,
   	"password":"azerty"
   }
   ```

2. La réponse à cette requête à pour code HTTP **200** et contient le jeton d'authentification dans une chaine JSON :

   ```json
   {
   	"token": "azertuiopqsdfghj"
   }
   ```



## Authentification échouée

### Situation de départ

En tant qu'utilisateur de l'API, sans jeton d'authentification, je souhaite m'authentifier auprès de l'API pour récupérer un jeton.

### Déroulement 

1. J'emet une requête HTTP POST à l'adresse : `/api/auth-tokens` avec comme corps de requête une chaine JSON listant un couple login et mot de passe erroné

   ```json
   {
   	"login":test,
   	"password":"azerty"
   }
   ```

2. La réponse à cette requête à pour code HTTP **500** et à pour contenu une chaine JSON :

   ```json
   {
   	"code": "500",
       "message": "Bad credentials"
   }
   ```



## Révocation du jeton réussie

### Situation de départ

En tant qu'utilisateur de l'API, authentifié avec un jeton, je souhaite révoquer mon jeton.

### Déroulement 

1. j'emet une requête HTTP DELETE à l'adresse : `/api/auth-tokens` avec comme corps de requête une chaine JSON contenant un jeton d'authentification valable

   ```json
   {
   	"token": "azertuiopqsdfghj"
   }
   ```

   La requête possède également un champ d'entête **X-Auth-Token** qui prend comme valeur le jeton d'authentification.

2. La réponse à cette requête à pour code HTTP **200** et à pour contenu une chaine JSON :

   ```json
   {
   	"code": "200",
       "message": "deleted"
   }
   ```



## Révocation du jeton échouée

### Situation de départ

En tant qu'utilisateur de l'API, authentifié avec un jeton, je souhaite révoquer mon jeton.

### Déroulement 

1. j'emet une requête HTTP DELETE à l'adresse : `/api/auth-tokens` avec comme corps de requête une chaine JSON contenant un jeton d'authentification non valable

   ```json
   {
   	"token": "123"
   }
   ```

   La requête possède également un champ d'entête **X-Auth-Token** qui prend comme valeur le jeton d'authentification.

2. La réponse à cette requête à pour code HTTP **500** et à pour contenu une chaine JSON :

   ```json
   {
   	"code": "500",
       "message": "Unknow token"
   }
   ```

