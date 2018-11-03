# Tests fonctionnels : Les types de sports pour l'API


## Récupération des raids liés à l'organisateur

###  Situation de départ

En tant qu'utilisateur de l'API, avec jeton d'authentification, je souhaite récupérer la liste des types de sports.

### Déroulement 

1. J'emet une requête **HTTP GET** à l'adresse : `/api/sporttype`

2. La réponse à cette requête à pour code HTTP **200** et contient la liste des types de sports dans une chaine JSON :

   ```json
  [{
    "id": 2,
    "sport": "Course à pied",
    "icon": "b9d16ccf67663768b756201953aa3e31.jpeg"
  }, {
    "id": 3,
    "sport": "VTT",
    "icon": "dc64d205bd88ed8b2449a0977e42eea4.png"
  }]
   ```