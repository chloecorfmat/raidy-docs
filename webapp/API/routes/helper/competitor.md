# Routes API - Participants


- `GET /api/helper/raid/{raidId}/competitor` liste les participants au raid *{raidId}*

  - Paramètres :

    - *raidId* : Identifiant du raid

  - Retour (tableau) : 

    - *id* :  identifiant du participant

    - *firstname* : prénom du participant

    - *lastname* : nom du participant

    - *number_sign* : numéro de dossard du participant

    - *nfc_serial_id* : numéro de série du badge du participant

    - *category* : catégorie du participant

    - *sex* : Sexe du du participant

    - *birthyear* : Année de naissance du participant

    - *race* : Epreuve liée

      - *id* : identifiant de l'épreuve
      - *name* : nom de l'épreuve

    - *raid* : identifiant du raid lié

- `GET /api/helper/raid/{raidId}/race/{raceId}/competitor` liste les participants au raid *{raidId}* et à l'épreuve {raceId}

  - Paramètres :

    - *raidId* : Identifiant du raid
    - *raceId* : Identifiant de l'épreuve 

  - Retour (tableau) : 

    - *id* :  identifiant du participant

    - *firstname* : prénom du participant

    - *lastname* : nom du participant

    - *number_sign* : numéro de dossard du participant

    - *nfc_serial_id* : numéro de série du badge du participant

    - *category* : catégorie du participant

    - *sex* : Sexe du du participant

    - *birthyear* : Année de naissance du participant

    - *race* : Epreuve liée

      - *id* : identifiant de l'épreuve
      - *name* : nom de l'épreuve

    - *raid* : identifiant du raid lié

- `GET /api/helper/raid/{raidId}/race/{raceId}/competitor/numbersign/{numberSign}` liste les participants au raid *{raidId}* et à l'épreuve *{raceId}* d'après leur numéro de dossard *{numberSign}* 

  - Paramètres :

    - *raidId* : Identifiant du raid
    - *raceId* : identifiant de l'épreuve
    - *numberSign* : Numéro de dossard
    - - *raceId* : Identifiant de l'épreuve 
    - 
    - - *raceId* : Identifiant de l'épreuve 
    - 

  - Retour : 

    - *id* :  identifiant du participant

    - *firstname* : prénom du participant

    - *lastname* : nom du participant

    - *number_sign* : numéro de dossard du participant

    - *nfc_serial_id* : numéro de série du badge du participant

    - *category* : catégorie du participant

    - *sex* : Sexe du du participant

    - *birthyear* : Année de naissance du participant

    - *race* : Epreuve liée

      - *id* : identifiant de l'épreuve
      - *name* : nom de l'épreuve

    - *raid* : identifiant du raid lié

- `GET /api/helper/raid/{raidId}/competitor/numbersign/{numberSign}` liste les participants au raid *{raidId}* d'après leur numéro de dossard *{numberSign}* 

  - Paramètres :

    - *raidId* : Identifiant du raid
    - *numberSign* : Numéro de dossard

  - Retour : 

    - *id* :  identifiant du participant

    - *firstname* : prénom du participant

    - *lastname* : nom du participant

    - *number_sign* : numéro de dossard du participant

    - *nfc_serial_id* : numéro de série du badge du participant

    - *category* : catégorie du participant

    - *sex* : Sexe du du participant

    - *birthyear* : Année de naissance du participant

    - *race* : Epreuve liée

      - *id* : identifiant de l'épreuve
      - *name* : nom de l'épreuve

    - *raid* : identifiant du raid lié

- `GET /api/helper/raid/{raidId}/race/{raceId}/competitor/nfcserialid/{nfcserialid}` liste les participants au raid *{raidId}* et à l'épreuve {raceId} d'après leur numéro de badge *{nfcserialid}* 

  - Paramètres :

    - *raidId* : Identifiant du raid
    - *raceId* : identifiant de l'épreuve
    - nfcserialid : Numéro de badge

  - Retour : 

    - *id* :  identifiant du participant

    - *firstname* : prénom du participant

    - *lastname* : nom du participant

    - *number_sign* : numéro de dossard du participant

    - *nfc_serial_id* : numéro de série du badge du participant

    - *category* : catégorie du participant

    - *sex* : Sexe du du participant

    - *birthyear* : Année de naissance du participant

    - *race* : Epreuve liée

      - *id* : identifiant de l'épreuve
      - *name* : nom de l'épreuve

    - *raid* : identifiant du raid lié

- `GET /api/helper/raid/{raidId}/competitor/numbersign/{nfcserialid}` liste les participants au raid *{raidId}* d'après leur numéro de badge *{nfcserialid}* 

  - Paramètres :

    - *raidId* : Identifiant du raid
    - *raceId* : identifiant de l'épreuve
    - *nfcserialid* : Numéro de badge

  - Retour : 

    - *id* :  identifiant du participant

    - *firstname* : prénom du participant

    - *lastname* : nom du participant

    - *number_sign* : numéro de dossard du participant

    - *nfc_serial_id* : numéro de série du badge du participant

    - *category* : catégorie du participant

    - *sex* : Sexe du du participant

    - *birthyear* : Année de naissance du participant

    - *race* : Epreuve liée

      - *id* : identifiant de l'épreuve
      - *name* : nom de l'épreuve

    - *raid* : identifiant du raid lié

- `PATCH /api/helper/raid/{raidId}/race/{raceId}/competitor/{numberSign}` assigne un numéro de badge à un participant

  - Paramètres :
    - URL
      - *raidId* : Identifiant du raid
      - *raceId* : identifiant de l'épreuve
      - *numberSign* : Numéro de dossard
    - Payload
      - *NFCSerialId* : Numéro de badge

  - Retour : 
    - *status* : Status de la requête

- `PUT /api/helper/raid/{raidId}/racetiming` ajoute un passage d'un participant à un checkpoint 

  - Paramètres :
    - URL
      - *raidId* : Identifiant du raid
    - Payload
      - *NFCSerialId* : Numéro de badge
      - *time* : Heur de passage
      - *poi_id* : Poi de passage
  - Retour : 
    - *status* : Status de la requête

