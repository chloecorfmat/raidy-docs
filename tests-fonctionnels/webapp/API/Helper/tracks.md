# Tests fonctionnels : Les parcours pour l'API - Helper



## Récupération des parcours liés à un raid

###  Situation de départ

En tant que bénévole utilisateur de l'API, avec jeton d'authentification, je souhaite récupérer la liste des parcours du raid auquel je suis lié.

### Déroulement 

1. J'emet une requête **HTTP GET** à l'adresse : `/api/helper/raid/{raidId}/track` avec *{raidId}* l'identifiant du raid auquel je suis rattaché.

2. La réponse à cette requête à pour code HTTP **200** et contient la liste des parcours dans une chaine JSON :

   ```json
  [{
    "id": 1,
    "name": "Parcours Vélo",
    "color": "#10855c",
    "raid": 1,
    "sportType": "VTT",
    "trackpoints": "[]",
    "isVisible": true,
    "isCalibration": false
  }, {
    "id": 2,
    "name": "Parcours Kayak",
    "color": "#2e1da3",
    "raid": 1,
    "sportType": "Kayak",
    "trackpoints": "[]",
    "isVisible": true,
    "isCalibration": false
  }]
   ```