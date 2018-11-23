# Routes API - contacts

- `GET /api/helper/raid/{raidId}/contact` liste les contacts liés au raid *{raidId}*

  - Paramètres :
    - *raidId* : Identifiant du raid
  - Retour : 

    - *id* : Identifiant du contact
    - *role* : nom du role du contact
    - *phoneNumber* : Numéro de téléphone, rempli automatiquement
    - *raid* : Identifiant du raid
    - *helper* 
      - *id* : identifiant du helper
      - *user* : identifiant de l'utilisateur lié
      - *isCheckedIn* (bool) : statut du bénévolat
      - *favoritePoiType* : identifiant du type de  POI préféré du helper
      - *Raid* : Identifiant du raid 
    - *user* : 
      - *id* : Identifiant de l'utilisateur
      - *firstname* : Prénom de l'utilisateur
      - *nom* : Nom de l'utilisateur

