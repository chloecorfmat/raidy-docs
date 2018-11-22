# Routes API interne - helper

- `PATCH /editor/raid/{raidId}/helper/{helperId} ` Affecte un POI à un Helper
  - Paramètres :
    - URL
      - helperId: Identifiant du helper
    - Payload
      - *poi* : Identifiant du POI
  - Retour : 
    - *id* : identifiant du helper
    - *user* : identifiant de l'utilisateur lié
    - *isCheckedIn* (bool) : statut du bénévolat
    - *favoritePoiType* : identifiant du type de  POI préféré du helper
    - *Raid* : Identifiant du raid 