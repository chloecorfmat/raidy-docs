# Tests fonctionnels : calibration

## Chargement des données

### Situation de départ

Sur l'application Organizer, en tant qu'utilisateur connecté, j'accède à l'interface de calibrage depuis la vue du raid en question. La géolocalisation est activée et je suis dans un endroit permettant la réception des signaux

### Déroulement

1. La carte s'affiche et ma position est signalée par un point bleu qui tourne en fonction de mon orientation
2. Je clique sur l'onglet **parcours** 
3. Un panneau s'ouvre, il liste les différents parcours du Raid
4. Je clique sur l'onglet **Points d'intérêts** 
5. Un panneau s'ouvre, il liste les différents points d'intérêts du Raid
6. Je clique une nouvelle fois sur l'onglet **Points d'intérêts** 
7. Le panneau se ferme et la carte apparait de nouveau



## Enregistrement d'un parcours

### Situation de départ

Sur l'application Organizer, en tant qu'utilisateur connecté, j'accède à l'interface de calibrage depuis la vue du raid en question. La géolocalisation est activée et je suis dans un endroit permettant la réception des signaux

### Déroulement

1. Je clique sur l'onglet **parcours** 
2. Un panneau s'ouvre, il liste les différents parcours du Raid
3. Je clique sur le bouton **Démarrer un calibrage**
4. Une popin s'ouvre, je remplis le nom du parcours et je sélectionne une couleur
5. Je clique sur **Ajouter un parcours**
6. La fenêtre se ferme
7. Un bandeau rouge apparait au dessus de la carte
8. Lors d'un déplacement :
   1. Le point bleu suit mes déplacements
   2. Toutes les 5 secondes, le tracé en cours d'enregistrement rejoint ma position
   3. La distance se met à jour dans le bandeau rouge
9. A la fin de l'enregistrement, je clique sur l'onglet **Parcours**
10. Je clique sur le bouton **Arrêter le calibrage**
11. Le nouveau parcours apparait dans la liste
12. Si je suis connecté à internet au moment de la fin de l'enregistrement : le parcours est visible sur la Webapp
13. Si je ne suis pas connecté à internet au moment de la fin de l'enregistrement : le parcours est visible sur la Webapp dès que mon équipement retrouve une connexion internet



## Edition d'un parcours

### Situation de départ

Sur l'application Organizer, en tant qu'utilisateur connecté, j'accède à l'interface de calibrage depuis la vue du raid en question. La géolocalisation est activée et je suis dans un endroit permettant la réception des signaux

### Déroulement

1. Je clique sur l'onglet **parcours** 
2. Un panneau s'ouvre, il liste les différents parcours du Raid
3. Je clique sur le bouton *3 points* à droite de la ligne du parcours que je veux modifier
4. Une fenêtre s'ouvre, affichant un formulaire pré-rempli avec les informations du parcours en question
5. Je modifie les information souhaitées (Ex: le nom)
6. Je clique sur le bouton **Mettre à jour**
7. La fenêtre se ferme et la liste des parcours est mise à jour
8. Si je suis connecté à internet au moment de la fin de l'enregistrement : le parcours est visible sur la Webapp
9. Si je ne suis pas connecté à internet au moment de la fin de l'enregistrement : le parcours est visible sur la Webapp dès que mon équipement retrouve une connexion internet

## Ajout d'un POI

### Situation de départ

Sur l'application Organizer, en tant qu'utilisateur connecté, j'accède à l'interface de calibrage depuis la vue du raid en question. La géolocalisation est activée et je suis dans un endroit permettant la réception des signaux

### Déroulement

1. Sur la carte, je clique sur le bouton **+** situé en bas à droite de l'écran
2. Une popin s'ouvre, je remplis le nom du point d'intérêts, un nombre de bénévoles requis et je sélectionne un type de point
3. Je clique sur **Ajouter un point d'intérêt**
4. La fenêtre se ferme et le point est ajouté dans la liste et sur la carte
5. Si je suis connecté à internet au moment de la fin de l'enregistrement : le point d'intérêt est visible sur la Webapp
6. Si je ne suis pas connecté à internet au moment de la fin de l'enregistrement : le point d'intérêt est visible sur la Webapp dès que mon équipement retrouve une connexion internet



## Edition d'un POI

### Situation de départ

Sur l'application Organizer, en tant qu'utilisateur connecté, j'accède à l'interface de calibrage depuis la vue du raid en question. La géolocalisation est activée et je suis dans un endroit permettant la réception des signaux

### Déroulement

1. Je clique sur l'onglet **point d'intérêt** 
2. Un panneau s'ouvre, il liste les différents points d'intérêt du Raid
3. Je clique sur le bouton *3 points* à droite de la ligne du point d'intérêt que je veux modifier
4. Une fenêtre s'ouvre, affichant un formulaire pré-rempli avec les informations du point d'intérêt en question
5. Je modifie les information souhaitées (Ex: le nom)
6. Je clique sur le bouton **Mettre à jour**
7. La fenêtre se ferme et la liste des points d'intérêt est mise à jour
8. Si je suis connecté à internet au moment de la fin de l'enregistrement : le point d'intérêt est visible sur la Webapp
9. Si je ne suis pas connecté à internet au moment de la fin de l'enregistrement : le point d'intérêt est visible sur la Webapp dès que mon équipement retrouve une connexion internet

