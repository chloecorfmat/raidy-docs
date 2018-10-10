# Tests fonctionnels : authentification

## Connexion avec les droits suffisants

### Situation de départ

En tant qu'organisateur de raids, avec un compte disposant du rôle **organizer** déconnecté, je veux accéder à l'application organizer.

### Déroulement 

1. Je me rends sur la page [/organizer](/organizer).
2. Je suis redirigé sur la page de connexion et je rentre les identifiants du compte et je valide le formulaire
3. Je suis redirigé vers la page /organizer



## Connexion avec des droits insuffisants

### Situation de départ

En tant qu'organisateur de raids, avec un compte disposant du rôle **organizer** déconnecté, je veux accéder à lla partie administration

### Déroulement 

1. Je me rends sur la page [/admin](/admin).
2. Je suis redirigé sur la page de connexion et je rentre les identifiants du compte et je valide le formulaire
3. Je suis redirigé vers la page /