# Tests fonctionnels : Les parcours

## Afficher des parcours

###  Situation de départ

En tant qu'organisateur de raids, je souhaite avoir les informations importantes liées aux parcours de mon raid.

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}](/organizer/raid/{id}).
2. Sur la page qui s'affiche : 
    1. Je peux cliquer sur le bouton **vert** dans la partie gauche pour afficher ou masquer le menu.
    3. Je peux sélectionner un ou plusieurs parcours à afficher en cliquant sur le bouton rond avec un **✓**.


## Ajouter un parcours

### Situation de départ

En tant qu'organisateur de raids, je souhaite pouvoir créer un parcours pour mon raid.

### Déroulement

1. Je me rends sur la page [/organizer/raid/{id}](/organizer/raid/{id}).
2. Je clique sur le bouton vert avec un marqueur blanc et un "+" en bas à droite de l'écran.
3. Un menu s'ouvre au dessus de ma souris. Je clique sur l'icône avec un marqueur vert **Ajouter un Parcours**.
4. Dans la fenêtre qui s'affiche :
  1. Je renseigne les informations liées à mon parcours :

    - Son nom
    - Le sport concerné par le parcours
    - Sa couleur
    
      2. J'envoie le formulaire en cliquant sur le bouton **Ajouter**.
      3. Je peux annuler ma tentative de création en cliquant sur **Annuler**.
     4. Une fois le parcours créé (il est ajouté dans le menu de gauche avec les autres parcours) j'ajoute .



## Editer le tracé d'un parcours	

### Situation de départ

En tant qu'organisateur de raids, je souhaite pouvoir éditer le tracé d'un parcours de mon raid.

### Déroulement

1. Je me rends sur la page [/organizer/raid/{id}](/organizer/raid/{id}).

2. Dans l'onglet **Parcours**, j'identifie le parcours que je veux éditer.

3. Je clique sur l'icône trois petits points du parcours que je veux éditer.

4. Un menu contextuel s'ouvre, je clique sur **Éditer le tracé**.

5. Je suis alors en mode édition de tracé.

   Des marqueurs ronds blancs apparaissent alors sur ce tracé.

   - Je peux les déplacer en les faisant glisser en maintenant le clique.
   - Je peux ajouter un point entre deux point en cliquant sur les marqueurs intermédiaire (transparents).

   - Je peux supprimer un point en double cliquant sur le marqueur.
   - Je peux terminer un tracé en cliquant sur le dernier point.
   - Quand un tracé est déja terminé je peux le reprendre en cliquant sur un point à une des extrémités.
   - Quand un tracé n'est pas terminé je peux ajouter un point en cliquant sur la carte 

6. Je quitte le mode édition en cliquant sur le bouton rouge avec un marqueur blanc et un "X" en bas à droite de l'écran.


## Modifier les informations d'un parcours	

### Situation de départ

En tant qu'organisateur de raids, je souhaite pouvoir modifier les informations d'un parcours de mon raid.

### Déroulement

1. Je me rends sur la page [/organizer/raid/{id}](/organizer/raid/{id}).
2. Dans l'onglet **Parcours**, j'identifie le parcours que je veux modifier.
3. Je clique sur l'icône trois petits points du parcours que je veux modifier.
4. Un menu contextuel s'ouvre, je clique sur **Modifier les infos** Dans la fenêtre qui s'affiche :
  5. Je modifie les informations liées à mon parcours :
  	- Son nom
  	- Le sport concerné par le parcours
  	- Sa couleur
    2. Je confirme l'édition du parcours en cliquant sur **Mettre à jour**.
    3. J'annule mon action en cliquant sur **Annuler**.


## Supprimer un parcours	

### Situation de départ

En tant qu'organisateur de raids, je souhaite pouvoir supprimer un parcours de mon raid.

### Déroulement

1. Je me rends sur la page [/organizer/raid/{id}](/organizer/raid/{id}).
2. Dans l'onglet **Parcours**, j'identifie le parcours que je veux supprimer.
3. Je clique sur l'icône trois petits points du parcours que je veux supprimer.
4. Un menu contextuel s'ouvre, je clique sur **Supprimer** Dans la fenêtre qui s'affiche :
   1. Je confirme la suppression du parcours en cliquant sur **Supprimer**.
   2. J'annule mon action en cliquant sur **Annuler**.
