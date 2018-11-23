# Tests fonctionnels : Les fichiers GPX

## Importer un fichier GPX

### Situation de départ

En tant qu'organisateur de raids, je souhaite importer un fichier GPX.

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}](/organizer/raid/{id}).
2. Je clique sur le bouton d'import en haut à gauche de la carte.
3. Une fenêtre s'ouvre. Je renseigne le fichier GPX source.
4. Le fichier est chargé, une liste de tracés et de points d'intérêts s'affiche. Je peux ensuite:
   1. Déselectionner les tracés et points d'intérêt à importer en décochant la case à gauche de leur nom.
   2. Affecter un type de sport aux tracés dans le menu deroulant à droite de leur nom.
   3. Affetter un type de point d'intérêt aux points d'intéret dans le menu déroulant à droite de leur nom
5. Une fois mes modifications effectués
   1. Je clique sur **Importer** pour importer les éléments selectionnés.
   2. J'annule mon action en cliquant sur **Annuler**.

## Export un fichier GPX

### Situation de départ

En tant qu'organisateur de raids, je souhaite exporter un fichier GPX de mes tracés et points d'intérets.

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}](/organizer/raid/{id}).
2. Je clique sur le bouton d'export en haut à gauche de la carte (sous le bouton d'import).
3. Une fenêtre s'ouvre
   1. Je clique sur **exporter en tant que tracés GPX** pour lancer le téléchargement du fichier GPX contenant tout mes tracés et mes points d'intérêts sous le format routes GPX.
   2. Je clique sur **exporter en tant que routes GPX** pour lancer le téléchargement du fichier GPX contenant tout mes tracés et mes points d'intérêts sous le format routes GPX.
   3. J'annule mon action en cliquant sur **Annuler**.