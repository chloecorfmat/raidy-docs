# Tests fonctionnels : Les collaborateurs

## Inviter des collaborateurs

###  Situation de départ

En tant qu'organisateur de raids, je veux inviter des collaborateurs pour m'aider à organiser l'évènement.

### Déroulement 

  1. Je me rends sur la page [/organizer/raid/{raid_id}/collaborator](/organizer/raid/{raid_id}/collaborator)
  2. Sur la page qui s'affiche, je remplis le formulaire avec l'adresse e-mail de mon collaborateur.
  3. Dans le tableau situé à gauche de l'écran, je récupère le lien unique généré (et je l'envoie à mon collaborateur).
  4. L'état de la collaboration est "En attente".
  5. Lorsque le collaborateur s'est inscrit sur l'interface, le statut passe à "Validé".
  
## Lister les collaborateurs

###  Situation de départ

En tant qu'organisateur de raids, je veux savoir qui peut m'aider à organiser l'évènement.

### Déroulement 

  1. Je me rends sur la page [/organizer/raid/{raid_id}/collaborator](/organizer/raid/{raid_id}/collaborator)
  2. Dans le tableau situé à gauche de la page, je peux savoir :
    - Quelles sont les adresses e-mails autorisées à collaborer ? 
    - Quel est le statut de la collaboration "En attente" ou "Validée" ?
