# Routes API - Messages


- `GET /api/helper/raid/{raidId}/message` récupère les messages d'un bénévole
  - Paramètres :

    - *raidId* : Identifiant du raid

  - Retour (tableau) : 

    - *id* :  identifiant du message
    - *text* : Contenu du message
    - *type* : Type du message
    - *datetime* : Date et heure du message