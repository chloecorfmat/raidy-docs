# Routes API - Poi

- `GET /api/helper/raid/{raidId}/poi` poi lié au helper qui émet la requête pour le raid donné 
  - Paramètres :
    - *raidId* : Identifiant du raid
  - Retour : 
    - *id* : identifiant du point d'intérêt
    - *name* : nom du point d'intérêt
    - *longitude* : longitude du point d'intérêt
    - *latitude* : latitude du point d'intérêt
    - *requiredHelpers* : nombre de bénévoles requis
    - *raid* : identifiant du raid correspondant à ce point d'intérêt
    - *poiType* : type de point d'intérêt
- `GET /api/helper/raid/{raidId}/check-in` valide la bénévolat d'un helper
  - Paramètres :
    - *raidId* : Identifiant du raid
  - Retour : 
    - *checkInTime* : Heure de prise en compte du check-in
    - *code* : Code de retour HTTP