# Routes API - types de points d'intérêt


- `GET /api/organizer/raid/{raidId}/poitype` liste les types de points d'intérêt liés à l'organisateur du raid {raidId}
  - Paramètres :
    - *raidId* : Identifiant du raid
  - Retour : 
    - *id* : identifiant du type de point d'intérêt
    - *type* : nom du type de point d'intérêt
    - *color* : couleur du type de point d'intérêt