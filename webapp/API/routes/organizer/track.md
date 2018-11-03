# Routes API - points d'intérêt


- `GET /api/organizer/raid/{raidId}/track` liste les parcours liés au raid *{raidId}*

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

- `PUT /api/organizer/raid/{raidId}/track` crée un nouveau parcours pour le raid *{raidId}*

  - Paramètres :

    - *name* : nom du parcours
    - *color* : couleur du parcours
    - *raid* : identifiant du raid correspondant à ce parcours
    - *sportType* : sport lié au parcours (vide si aucun)
    - *trackpoints* : points du parcours
    - *isVisible* : le tracé est-il visible ou non
    - *isCalibration* : le tracé est-il calibré ou non

  - Retour : 

    - *id* : identifiant du parcours
    - *name* : nom du parcours
    - *color* : couleur du parcours
    - *raid* : identifiant du raid correspondant à ce parcours
    - *sportType* : sport lié au parcours (vide si aucun)
    - *trackpoints* : points du parcours
    - *isVisible* : le tracé est-il visible ou non
    - *isCalibration* : le tracé est-il calibré ou non

- `PATCH /api/organizer/raid/{raidId}/track/{trackId}` modifie le parcours *{trackId}* pour le raid *{raidId}*

  - Paramètres :
  
    - *name* : nom du parcours
    - *color* : couleur du parcours
    - *raid* : identifiant du raid correspondant à ce parcours
    - *sportType* : sport lié au parcours (vide si aucun)
    - *trackpoints* : points du parcours
    - *isVisible* : le tracé est-il visible ou non
    - *isCalibration* : le tracé est-il calibré ou non

  - Retour : 

    - *id* : identifiant du parcours
    - *name* : nom du parcours
    - *color* : couleur du parcours
    - *raid* : identifiant du raid correspondant à ce parcours
    - *sportType* : sport lié au parcours (vide si aucun)
    - *trackpoints* : points du parcours
    - *isVisible* : le tracé est-il visible ou non
    - *isCalibration* : le tracé est-il calibré ou non

- `DELETE /api/organizer/raid/{raidId}/track/{trackId}` supprime le parcours *{trackId}* pour le raid *{raidId}*

  - Paramètres
    
    Pas de paramètres.

  - Retour : 

    - *status* : Status de la requête