# Tests fonctionnels : Connexion à l'application mobile Organizer ou Helper

### Situation de départ
Sur l'application Organizer : En tant qu'organisateur de raid, je veux pouvoir me connecter à mon compte sur l'application Organizer pour vérifier mon parcours en conditions réelles.

Sur l'application Helper : En tant que bénévole, je veux pouvoir me connecter à mon compte sur l'application Helper pour gérer mon compte.
## Se connecter à son compte
### Déroulement
1. J'ouvre l'application Raidy Organizer ou Helper
2. Sur la page qui s'affiche, je saisi des identifiants existants
3. Je clique sur le bouton "Connexion" en bas
4. Je suis authentifié et accède à la page d'accueil
## Connexion erronée
### Déroulement
1. J'ouvre l'application Raidy Organizer ou Helper
2. Sur la page qui s'affiche, je saisi des identifiants inexistants
3. Je clique sur le bouton "Connexion" en bas
4. Un message d'erreur apparaît m'informant que mes identifiants sont mauvais
## Ne pas saisir d'identifiants
### Déroulement
1. J'ouvre l'application Raidy Organizer ou Helper
2. Sur la page qui s'affiche, je clique directement sur le bouton "Connexion" en bas
3. Une infobulle apparaît m'informant que les champs de saisie sont obligatoire.
## Se déconnecter de mon compte
### Situation de départ
Je suis au préalable connecté à un compte organizer ou helper existant.
### Déroulement
1. J'ouvre l'application Raidy Organizer ou Helper
2. Sur la page qui s'affiche, je clique sur le bouton "Déconnexion" en haut à droite de l'écran
3. Je suis déconnecté et redirigé vers la page de connexion