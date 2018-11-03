# Routes API - profil utilisateur


- `GET /api/profile` affiche le profil de l'utilisateur courant

  - Paramètres :

    Pas de paramètres.

  - Retour : 

    - *username* : identifiant 
    - *firstname* : prénom
    - *lastname* : nom
    - *email* : email
    - *phone* : numéro de téléphone

- `PATCH /api/profile` modifie le profil de l'utilisateur courant

  - Paramètres :
  
    - *username* : identifiant 
    - *firstname* : prénom
    - *lastname* : nom
    - *email* : email
    - *phone* : numéro de téléphone

  - Retour : 

    - *username* : identifiant 
    - *firstname* : prénom
    - *lastname* : nom
    - *email* : email
    - *phone* : numéro de téléphone