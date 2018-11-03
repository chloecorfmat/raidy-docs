# Tests fonctionnels : Les parcours pour l'API - Organizer



## Récupération des parcours liés à un raid

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite récupérer la liste des parcours du raid auquel je suis lié.

### Déroulement 

1. J'emet une requête **HTTP GET** à l'adresse : `/api/organizer/raid/{raidId}/track` avec *{raidId}* l'identifiant du raid auquel je suis rattaché.

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

## Ajout d'un parcours lié à un raid

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite ajouter un parcours au raid auquel je suis lié.

### Déroulement 

1. J'emet une requête **HTTP POST** à l'adresse : `/api/organizer/raid/{raidId}/track` avec *{raidId}* l'identifiant du raid auquel je suis rattaché et avec comme corps de requête une chaine JSON :

   ```json
  {
    "name": "Parcours course à pied",
    "color": "#f5f5f5",
    "raid": 1,
    "sportType": "Course à pied",
    "trackpoints": "[]",
    "isVisible": true,
    "isCalibration": false
  }
   ```

2. La réponse à cette requête à pour code HTTP **201** et contient le parcours dans une chaine JSON :

   ```json
  {
    "id": 3,
     "name": "Parcours course à pied",
    "color": "#f5f5f5",
    "raid": 1,
    "sportType": "Course à pied",
    "trackpoints": "[]",
    "isVisible": true,
    "isCalibration": false
  }
   ```

## Modification d'un parcours lié à un raid

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite modifier un parcours au raid auquel je suis lié.

### Déroulement 

1. J'emet une requête **HTTP PATCH** à l'adresse : `/api/organizer/raid/{raidId}/track/{trackId}` avec *{raidId}* l'identifiant du raid auquel je suis rattaché, et *{trackId}* l'identifiant de parcours. Le corps de requête est une chaine JSON :

   ```json
  {
    "name": "Parcours course à pied débutant",
    "color": "#f5f5f5",
    "raid": 1,
    "sportType": "Course à pied",
    "trackpoints": "[]",
    "isVisible": true,
    "isCalibration": false
  }
   ```

2. La réponse à cette requête à pour code HTTP **201** et contient le parcours dans une chaine JSON :

   ```json
  {
    "id": 3,
     "name": "Parcours course à pied débutant",
    "color": "#f5f5f5",
    "raid": 1,
    "sportType": "Course à pied",
    "trackpoints": "[]",
    "isVisible": true,
    "isCalibration": false
  }
   ```

## Suppression d'un parcours lié à un raid

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite supprimer un parcours au raid auquel je suis lié.

### Déroulement 

1. J'emet une requête **HTTP DELETE** à l'adresse : `/api/organizer/raid/{raidId}/track/{trackId}` avec *{raidId}* l'identifiant du raid auquel je suis rattaché, et *{trackId}* l'identifiant de parcours.

2. La réponse à cette requête à pour code HTTP **200** et contient la réponse dans une chaine JSON :

   ```json
  {
    "code": 200,
    "message": "Deleted"
  }
   ```