# Authentification sur l'API

Afin de sécuriser l'accès aux données exposées par l'API les utilisateurs doivent s'authentifier. Cette authentification exploite un jeton afin d'éviter d'utiliser les identifiants de connexion à chaque fois.

Le jeton est alors lié à un utilisateur, on sauvegarde également la date de création du jeton. On pourra considérer le jeton comme expiré après une certaine durée et éxiger que l'utilisateur se reconnecte.



## Connexion à l'API

Pour se connecter l'utilisateur doit donner son identifiant et son mot de passe, le serveur vérifie la véracité des données et donne un jeton à l'utilisateur. Ce jeton prend la forme d'une chaine de caractère.

La connexion utilise la route `POST /api/auth-tokens` et prend en paramètres le `login` et le `password`.



## Déconnexion de l'API

L'utilisateur peut de lui-même révoquer son jeton en demandant la suppression du jeton.

La déconnexion utilise la route`DELETE /api/auth-tokens` et prend en paramètres le `token`.

