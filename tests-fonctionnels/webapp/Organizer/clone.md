# Tests fonctionnels : Cloner un raid

## Cloner un raid

###  Situation de départ

En tant qu'organisateur de raids, je veux repartir d'un raid passé pour faciliter l'organisation d'un nouvel évènement.

### Pré-requis
  * Avoir créer un raid.

### Déroulement 

  1. Je me rends sur la page [/organizer/raid/{raid_id}](/organizer/raid/{raid_id})
  2. Je clique ensuite sur le bouton "Cloner le raid" situé à droite de la page.
  3. Dans le formulaire qui s'affiche, je modifie les informations qui s'affichent :
    * Il faut obligatoirement changer le numéro d'édition du raid pour pouvoir le cloner.
  5. Je clique sur "Cloner ce raid".
  6. J'arrive alors sur ma liste de raid.
  7. Je vais sur la page [/organizer/raid/{clone_id}](/organizer/raid/{clone_id}).
  8. Je m'aperçois alors que :
    * Les informations du raid sont présentes.
    * Les tracés et points d'intérêt sont bien clonés.
    * Les bénévoles ne sont pas clonés.
    * Les contacts liés à un bénévole ne sont pas clonés.
    * Les contacts indépendants sont clonés.