# Routes API - parcours

- `GET /editor/raid/{raidId}/track` liste les parcours liés au raid *{raidId}*

  - Paramètres :

    - *raidId* : Identifiant du raid

  - Retour : 

    - *id* : identifiant du parcours

    - *name* : nom du parcours

    - *color* : couleur du parcours

    - *raid* : identifiant du raid correspondant à ce parcours

    - *sportType* : sport lié au parcours (vide si aucun)

    - *trackpoints* : points du parcours

    - *isVisible* : le tracé est-il visible ou non

    - *isCalibration* : le tracé est-il calibré ou non

- `PUT /editor/raid/{raidId}/track` crée un nouveau parcours pour le raid *{raidId}*

  - Paramètres :

    - URL
      - *raidId* : Identifiant du raid
    - Payload
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

- `PATCH /editor/raid/{raidId}/track/{trackId}` modifie le parcours *{trackId}* pour le raid *{raidId}*

  - Paramètres :

    - URL
      - *raidId* : Identifiant du raid
      - trackId: Identifiant du raid
    - Payload
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

- `DELETE /editor/raid/{raidId}/track/{trackId}` supprime le parcours *{trackId}* pour le raid *{raidId}*

  - Paramètres
    - *raidId* : Identifiant du raid
    - trackId: Identifiant du parcours
  - Retour : 
    - *status* : Status de la requête