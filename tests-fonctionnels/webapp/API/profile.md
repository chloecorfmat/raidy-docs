# Tests fonctionnels : Le profil



## Récupération d'un profil

###  Situation de départ

En tant qu'utilisateur de l'API, avec jeton d'authentification, je souhaite récupérer mon profil.

### Déroulement 

1. J'emet une requête **HTTP GET** à l'adresse : `/api/profile`.

2. La réponse à cette requête à pour code HTTP **200** et contient le profil dans une chaine JSON :

   ```json
  {
    "username": "orga@sixteam.fr",
    "firstname": "Jean",
    "lastname": "Orga",
    "email": "orga@sixteam.fr",
    "phone": "0610656565"
  }
   ```

## Modification d'un profil

###  Situation de départ

En tant qu'utilisateur de l'API, avec jeton d'authentification, je souhaite modifier mon profil.

### Déroulement 

1. J'emet une requête **HTTP PATCH** à l'adresse : `/api/profile`. Le corps de requête est une chaine JSON :

   ```json
  {
    "username": "orga@sixteam.fr",
    "firstname": "Jean",
    "lastname": "Orga",
    "email": "orga@sixteam.fr",
    "phone": "0610656500"
  }
   ```

2. La réponse à cette requête à pour code HTTP **201** et contient le profil dans une chaine JSON :

   ```json
  {
    "username": "orga@sixteam.fr",
    "firstname": "Jean",
    "lastname": "Orga",
    "email": "orga@sixteam.fr",
    "phone": "0610656500"
  }
   ```