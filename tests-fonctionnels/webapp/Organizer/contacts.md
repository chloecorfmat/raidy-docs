# Tests fonctionnels : Les contacts

## Ajouter des contacts

###  Situation de départ

En tant qu'organisateur de raids, je souhaite ajouter des contacts à un raid pour donner leurs coordonnées aux bénévoles.

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}](/organizer/raid/{id}).
2. Sur la page qui s'affiche, je clique sur le bouton **Contacts** à droite de l'écran.
3. Je me retrouve alors sur la page [/organizer/raid/{id}/contacts](/organizer/raid/{id}/contact).
4. Dans le formulaire à droite de l'écran, je remplis les informations suivantes : 
    1. Rôle : SAMU
    2. Téléphone : 15
    3. Bénévole : <laisser vide>
5. Je clique sur le bouton "Créer un contact". J'aperçois mon contact dans la liste des contacts située à gauche de la page.
6. Dans le formulaire à droite de l'écran, je remplis les informations suivantes : 
    1. Rôle : Responsable buvette
    2. Téléphone : <laisser vide>
    3. Bénévole : <sélectionner un bénévole>
7. Je clique sur le bouton "Créer un contact". J'aperçois mon contact dans la liste des contacts située à gauche de la page.
8. Sur la ligne de mon nouveau contact dans le tableau, je vois que son numéro de téléphone a été récupéré automatiquement.




## Afficher les contacts

###  Situation de départ

En tant qu'organisateur de raids, je souhaite lister les contacts associés à un raid.

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}](/organizer/raid/{id}).
2. Sur la page qui s'affiche, je clique sur le bouton **Contacts** à droite de l'écran.
3. Je me retrouve alors sur la page [/organizer/raid/{id}/contacts](/organizer/raid/{id}/contact).
4. Dans le tableau qui s'affiche sur la gauche de l'écran, je peux :
  - Voir l'ensemble des contacts avec leurs coordonnées
  - Accéder à la page de modification d'un contact


