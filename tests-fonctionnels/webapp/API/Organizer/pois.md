# Tests fonctionnels : Les points d'intérêt pour l'API - Organizer



## Récupération des points d'intérêt liés à un raid

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite récupérer la liste des points d'intérêt de mon raid.

### Déroulement 

1. J'emet une requête **HTTP GET** à l'adresse : `/api/organizer/raid/{raidId}/poi` avec *{raidId}* l'identifiant du raid concerné.

2. La réponse à cette requête à pour code HTTP **200** et contient la liste des points d'intérêt dans une chaine JSON :

   ```json
  [{
    "id": 1,
    "name": "Parking 1 ",
    "longitude": "48.0526",
    "latitude": "1.256",
    "requiredHelpers": "2",
    "raid": 1,
    "poiType": 5
  },
  {
    "id": 2,
    "name": "Parking 2",
    "longitude": "48.5226",
    "latitude": "1.666",
    "requiredHelpers": "2",
    "raid": 1,
    "poiType": 5
  }]
   ```

## Récupération d'un point d'intérêt liés à un raid

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite récupérer un point d'intérêt particulier.

### Déroulement 

1. J'emet une requête **HTTP GET** à l'adresse : `/api/organizer/raid/{raidId}/poi/{poiId}` avec *{raidId}* l'identifiant du raid concerné et *{poiId}* l'identifiant de point d'intérêt.

2. La réponse à cette requête à pour code HTTP **200** et contient le point d'intérêt dans une chaine JSON :

   ```json
  {
    "id": 2,
    "name": "Parking 2",
    "longitude": "48.5226",
    "latitude": "1.666",
    "requiredHelpers": "2",
    "raid": 1,
    "poiType": 5
  }
   ```


## Ajout d'un point d'intérêt lié à un raid

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite ajouter un point d'intérêt à mon raid.

### Déroulement 

1. J'emet une requête **HTTP POST** à l'adresse : `/api/organizer/raid/{raidId}/poi` avec *{raidId}* l'identifiant du raid auquel je suis rattaché et avec comme corps de requête une chaine JSON :

   ```json
  {
    "name": "Virage",
    "longitude": "48.9522",
    "latitude": "1.6548",
    "requiredHelpers": 3,
    "raid": 1,
    "poiType": 4
  }
   ```

2. La réponse à cette requête à pour code HTTP **201** et contient le parcours dans une chaine JSON :

   ```json
  {
    "id": 2,
    "name": "Virage",
    "longitude": "48.9522",
    "latitude": "1.6548",
    "requiredHelpers": "3",
    "raid": 1,
    "poiType": 4
  }
   ```

## Modification d'un point d'intérêt lié à un raid

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite modifier un point d'intérêt de mon raid.

### Déroulement 

1. J'emet une requête **HTTP PATCH** à l'adresse : `/api/organizer/raid/{raidId}/poi/{poiId}` avec *{raidId}* l'identifiant du raid auquel je suis rattaché, et *{poiId}* l'identifiant de point d'intérêt. Le corps de requête est une chaine JSON :

   ```json
  {
    "name": "Virage",
    "longitude": "48.5555",
    "latitude": "1.6548",
    "requiredHelpers": 3,
    "raid": 1,
    "poiType": 4
  }
   ```

2. La réponse à cette requête à pour code HTTP **201** et contient le point d'intérêt dans une chaine JSON :

   ```json
  {
    "id": 2,
    "name": "Virage",
    "longitude": "48.5555",
    "latitude": "1.6548",
    "requiredHelpers": "3",
    "raid": 1,
    "poiType": 4
  }
   ```

## Suppression d'un point d'intérêt lié à un raid

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite supprimer un point d'intérêt de mon raid.

### Déroulement 

1. J'emet une requête **HTTP DELETE** à l'adresse : `/api/organizer/raid/{raidId}/poi/{poiId}` avec *{raidId}* l'identifiant du raid auquel je suis rattaché, et *{poiId}* l'identifiant du point d'intérêt.

2. La réponse à cette requête à pour code HTTP **200** et contient la réponse dans une chaine JSON :

   ```json
  {
    "code": 200,
    "message": "Deleted"
  }
   ```