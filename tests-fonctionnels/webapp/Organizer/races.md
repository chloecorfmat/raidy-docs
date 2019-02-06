# Tests fonctionnels : Epreuves

## Afficher les épreuves

### Situation de départ

En tant qu'organisateur de raids, je souhaite avoir accès à l'éditeur d'épreuves

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}/race](/organizer/raid/{id}/race).
2. Sur la page qui s'affiche : 
   1. J'ai un bouton *Créer une épreuve*
   2. Le détail des épreuves déjà crées est affiché


## Créer une épreuve

### Situation de départ

En tant qu'organisateur de raids, je souhaite pouvoir créer une épreuve

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}/race](/organizer/raid/{id}/race).

2. Sur la page qui s'affiche : 
   1. J'ai un bouton *Créer une épreuve*
   2. je clique dessus

3. Une popin s'ouvre :

   1. Je remplis le champ *Nom de l'épreuve*
   2. Je cliquer sur "Créer une épreuve"
   3. Une nouvelle épreuve apparait

4. Je clique ensuite sur *Ajouter un parcours*

   1. Une ligne avec une liste déroulante apparait
   2. Je choisi un parcours et je clique sur le bouton *Ajouter un parcours*
   3. Le nouveau parcours est bien ajouté à l'épreuve

5. Je clique ensuite sur *Ajouter un checkpoint*

   1. Une ligne avec une liste déroulante apparait
   2. Je choisi un parcours et je clique sur le bouton *Ajouter un checkpoint* 
   3. Le nouveau Checkpoint est bien ajouté au parcours



## Gérer les éléments

### Situation de départ

En tant qu'organisateur de raids, je souhaite pouvoir ordonner les éléments d'une épreuve

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}/race](/organizer/raid/{id}/race).
2. Sur la page qui s'affiche :
   1. chaque élément d'une épreuve possède des fleches *haut* et *bas* 
3. Lorsque je clique sur la flèche *haut* d'un élément:
   1. L'élément prend la place de l'élement du dessus (si il existe)
4. Lorsque je clique sur la flèche *bas* d'un élément:
   1. L'élément prend la place de l'élement du dessous (si il existe)
5. Lorsque je clique sur la bouton *supprimer* d'un élément:
   1. L'élément est supprimé