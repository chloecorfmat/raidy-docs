# Tests fonctionnels : Live ! Classement

**Prérequis :** Créer un raid sans participant

## Affichage du classement sans participant

###  Situation de départ

En tant qu'organisateur d'un raid, je souhaite qu'un classement sans participant affiche si aucun participant n'est ajouté.

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}/live](/organizer/raid/{id}/live).
2. Le tableau du classement apparaît avec les colonnes : 
  * Classement
  * Temps
  * Nom du dossard
  * Catégorie
  * Course
3. Il n'y a aucun participant qui apparaît.

## Affichage du classement avec participant 

###  Situation de départ

En tant qu'organisateur d'un raid, je souhaite qu'un classement sans participant affiche si aucun participant n'est ajouté.

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}/live](/organizer/raid/{id}/live).
2. Le tableau du classement apparaît avec les colonnes : 
  * Classement
  * Temps
  * Nom du dossard
  * Catégorie
  * Course
3. La liste des participants apparaît classée par épreuve.

## Affichage du classement avec participant et épreuve démarrée 

###  Situation de départ

En tant qu'organisateur d'un raid, je souhaite qu'un classement soit affiché avec le classement temporaire.

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}/live](/organizer/raid/{id}/live).
2. Le tableau du classement apparaît avec les colonnes : 
  * Classement
  * Temps
  * Nom du dossard
  * Catégorie
  * Course
3. La liste des participants apparaît classée par épreuve et classement temporaire.

## Affichage du classement avec participant et épreuve terminée 

###  Situation de départ

En tant qu'organisateur d'un raid, je souhaite qu'un classement définitif soit affiché.

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}/live](/organizer/raid/{id}/live).
2. Le tableau du classement apparaît avec les colonnes : 
  * Classement
  * Temps
  * Nom du dossard
  * Catégorie
  * Course
3. La liste des participants apparaît classée par épreuve et classement. Les participants qui ont fraudé apparaissent en rouge.

## Tri du classement

###  Situation de départ

En tant qu'organisateur d'un raid, je souhaite retrouver le classement par course ou rechercher un participant par son nom.

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}/live](/organizer/raid/{id}/live).
2. Le tableau du classement apparaît avec les colonnes : 
  * Classement
  * Temps
  * Nom du dossard
  * Catégorie
  * Course
3. Lorsque je remplis le champ "Rechercher" avec le nom d'un participant, seul celui-ci est retourné.
4. Lorsque je sélectionne une course dans la liste déroulante, seuls les participants de cette course sont affichés.
5. Les filtres sont cumulables.

