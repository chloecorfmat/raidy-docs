# Routes API - raid


- `GET /api/helper/raid` liste les raids liés au bénévole

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

- `GET /api/helper/raid/{raidId}` liste les informations liées au raid *{raidId}*

  - Paramètres :
    - *raidId* : Identifiant du raid
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