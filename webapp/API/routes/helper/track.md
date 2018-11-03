# Routes API - points d'intérêt


- `GET /api/helper/raid/{raidId}/track` liste les parcours liés au raid *{raidId}*

  - Paramètres :

    Pas de paramètres.

  - Retour : 

    - *id* : identifiant du parcours
    - *name* : nom du parcours
    - *color* : couleur du parcours
    - *raid* : identifiant du raid correspondant à ce parcours
    - *sportType* : sport lié au parcours (vide si aucun)
    - *trackpoints* : points du parcours
    - *isVisible* : le tracé est-il visible ou non
    - *isCalibration* : le tracé est-il calibré ou non