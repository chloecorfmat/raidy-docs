# Tests fonctionnels : Les bénévoles

## Lister les bénévoles de mon raid

###  Situation de départ

En tant qu'organisateur de raids, je souhaite voir la liste des bénévoles inscrits pour mon raid.

### Pré-requis

  * Une personne s'est inscrite en tant que bénévole au raid.

### Déroulement 

  1. Je me rends sur la page [/organizer/raid/helpers/{id}](/organizer/raid/helpers/{id}).
  2. À gauche de l'écran, je peux voir toutes les informations liées à un bénévole :
    * Nom & prénom
    * Statut (c'est-à-dire s'il a validé son bénévolat ou non)
    * Poste souhaité (type de point d'intérêt souhaité)
    * Poste affecté (point d'intérêt affecté)
  3. À droite de l'écran, je peux voir la carte avec l'ensemble des parcours et des points d'intérêt de mon raid. Les informations ne sont pas modifiables, mais je peux cliquer sur les points d'intérêt pour avoir des informations qui y sont relatives.
  

## Associer un bénévole à un point d'intérêt

###  Situation de départ

En tant qu'organisateur de raids, je souhaite lié un bénévole à un point d'intérêt.

### Pré-requis

  * Une personne s'est inscrite en tant que bénévole au raid.
  * Des points d'intérêt existent sur le raid.

### Déroulement 

  1. Je me rends sur la page [/organizer/raid/helpers/{id}](/organizer/raid/helpers/{id}).
  2. Sur la ligne d'un bénévole, je modifie la valeur dans la colonne "Poste affecté".
  3. Le statut est automatiquement mis à jour : un point rouge remplace le point gris précédent.


## Vérifier le statut d'un bénévole le jour du raid

###  Situation de départ

En tant qu'organisateur de raids, je souhaite savoir si un bénévole a validé son bénévolat.

### Pré-requis

  * Une personne s'est inscrite en tant que bénévole au raid et a été associée à un point d'intérêt.

### Déroulement 

  1. Je me rends sur la page [/organizer/raid/helpers/{id}](/organizer/raid/helpers/{id}).
  2. Sur la ligne d'un bénévole, j'ai accès à son statut :
    * Si le point est **gris** : le bénévole n'a pas été associé à un point d'intérêt.
    * Si le point est **rouge** : le bénévole a été associé à un point d'intérêt, mais n'a pas encore validé son bénévolat.
    * Si le point est **vert** : le bénévolat a été validé.