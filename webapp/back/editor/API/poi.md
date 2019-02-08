# Routes API interne - POI

- `GET /editor/raid/{raidId}/poi` liste les points d'intérêts liés au raid *{raidId}*

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

    - *description* : description du point d'intérêt

    - *image* : image du point d'intérêt

- `PUT /editor/raid/{raidId}/poi` crée un nouveau point d'intérêt pour le raid *{raidId}*

  - Paramètres :

    - *name* : nom du point d'intérêt
    - *longitude* : longitude du point d'intérêt
    - *latitude* : latitude du point d'intérêt
    - *requiredHelpers* : nombre de bénévoles requis
    - *poiType* : type de point d'intérêt
    - *description* : description du point d'intérêt
    - *image* : image du point d'intérêt

  - Retour : 

    - *id* : identifiant du point d'intérêt

    - *name* : nom du point d'intérêt

    - *longitude* : longitude du point d'intérêt

    - *latitude* : latitude du point d'intérêt

    - *requiredHelpers* : nombre de bénévoles requis

    - *raid* : identifiant du raid correspondant à ce point d'intérêt

    - *poiType* : type de point d'intérêt

    - *description* : description du point d'intérêt

    - *image* : image du point d'intérêt

- `PATCH /editor/raid/{raidId}/poi/{poiId}` modifie le point d'intérêt *{poiId}* pour le raid *{raidId}*

  - Paramètres :
    - *name* : nom du point d'intérêt
    - *longitude* : longitude du point d'intérêt
    - *latitude* : latitude du point d'intérêt
    - *requiredHelpers* : nombre de bénévoles requis
    - *poiType* : type de point d'intérêt
    - *description* : description du point d'intérêt
    - *image* : image du point d'intérêt
  - Retour : 
    - *id* : identifiant du point d'intérêt
    - *name* : nom du point d'intérêt
    - *longitude* : longitude du point d'intérêt
    - *latitude* : latitude du point d'intérêt
    - *requiredHelpers* : nombre de bénévoles requis
    - *raid* : identifiant du raid correspondant à ce point d'intérêt
    - *poiType* : type de point d'intérêt
    - *description* : description du point d'intérêt
    - *image* : image du point d'intérêt



- `DELETE /editor/raid/{raidId}/poi/{poiId}` supprime le point d'intérêt *{poiId}* pour le raid *{raidId}*
  - Paramètres
    - *raidId* : Identifiant du raid
    - *poiId* : Identifiant du POI
  - Retour : 
    - *status* : Status de la requête