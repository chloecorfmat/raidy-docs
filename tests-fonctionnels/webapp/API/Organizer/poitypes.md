# Tests fonctionnels : Les types de points d'intérêt pour l'API - Organizer



## Récupération des types de points d'intérêt liés à l'organisateur

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite récupérer la liste des types de points d'intérêt que j'ai créé.

### Déroulement 

1. J'emet une requête **HTTP GET** à l'adresse : `/api/organizer/poitype`

2. La réponse à cette requête à pour code HTTP **200** et contient la liste des types de points d'intérêt dans une chaine JSON :

   ```json
  [{
    "id": 4,
    "type": "Point dangereux",
    "color": "#44dbbd"
  }, {
    "id": 5,
    "type": "Parking",
    "color": "#b8652e"
  }]
   ```