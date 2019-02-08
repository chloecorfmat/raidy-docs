# Tests fonctionnels : Live ! Tweets

**Prérequis :** Créer un raid

## Non affichage d'une liste de tweets paramétrées

###  Situation de départ

En tant que bénévole pour un raid, je ne souhaite pas pouvoir afficher les tweets liés à des hashtags ou des noms d'utilisateur. 

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}/live](/organizer/raid/{id}/live).
2. Les champs du formulaire ne sont pas remplis.
3. Je me rends sur la page [/live/raid/{id}](/live/raid/{id}).
4. Sur la page qui s'affiche :
    1. La colonne de tweets ne s'affiche pas.
    2. Seul le classement de la course s'affiche.

## Affichage d'une liste de tweets paramétrées

###  Situation de départ

En tant que bénévole pour un raid, je souhaite pouvoir afficher les tweets liés à des hashtags ou des noms d'utilisateur. 

### Déroulement 

1. Je me rends sur la page [/organizer/raid/{id}/live](/organizer/raid/{id}/live).
2. Je complète les champs "Twitter : hashtags" et "Twitter : comptes à suivre".
3. Je me rends sur la page [/live/raid/{id}](/live/raid/{id}).
4. Sur la page qui s'affiche :
    1. Une colonne de Tweets s'affiche sur la gauche de la page.
    2. Le classement s'affiche sur la droite.

## Affichage d'un tweet

### Situation de départ

Tous les éléments d'un tweet sont affichés.

### Déroulement

_Sur chaque tweet sont affichés : _
 * La **photo de profil** de l'utilisateur qui a tweeté.
 * Le **nom du compte utilisateur** qui a publié le tweet. Au clic sur ce nom, le compte Twitter s'ouvre dans une autre page.
 * La **date et l'heure** de publication du tweet.
 * Le **contenu** du tweet.
 * Le **lien du tweet** sur une icône représentant le logo de la plateforme Twitter.
 * Si le tweet publié est un retweet (RT) : une icône de retweet en bas à droite.
