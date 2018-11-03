# Routes API - raid


- `GET /api/organizer/raid` liste les raids liés à l'organisateur

  - Paramètres :

    Pas de paramètres.

  - Retour : 

    - *id* : identifiant du raid
    - *name* : nom du raid
    - *date* : date du raid
    - *adress* : adresse
    - *addressAddition* : complément d'adresse (vide si aucun)
    - *postCode* : code postal
    - *city* : ville
    - *editionNumber* : numéro d'édition
    - *picture* : photo/illustration pour le raid

## ** Non implémenté **

- `GET /api/organizer/raid/{raidId}` liste les informations liées au raid *{raidId}*

  - Paramètres :

    Pas de paramètres.

  - Retour : 

    - *id* : identifiant du raid
    - *name* : nom du raid
    - *date* : date du raid
    - *adress* : adresse
    - *addressAddition* : complément d'adresse (vide si aucun)
    - *postCode* : code postal
    - *city* : ville
    - *editionNumber* : numéro d'édition
    - *picture* : photo/illustration pour le raid