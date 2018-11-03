# Routes API - authentification

- `POST \auth-tokens` Demander un jeton d'API

  - Paramètres

    - *Login* : identifiant de l'utilisateur
    - *Password* : mot de passe de l'utilisateur

  - Retour : 

    - *Token* : Jeton utilisateur

- `DELETE \auth-tokens` supprime un jeton d'API

  - Paramètres

    - *token* : jeton à supprimer
  - Retour : 
  
    - *status* : Status de la requête