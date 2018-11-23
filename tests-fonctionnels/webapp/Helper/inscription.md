# Tests fonctionnels : Inscription helper



## Inscription à un raid avec création de compte

### Situation de départ

En tant que futur bénévole, dépourvu de compte sur la plate-forme, je veux m'inscrire à un raid. J'ai en ma possession un lien fourni par les organisateurs qui prend la forme `/helper/invite/{id}`.

### Déroulement 

1. Je me rends sur le lien fourni par les organisateurs
2. Je n'ai pas de compte, je clique sur le bouton **Se créer un compte**, je suis redirigé vers une page de formulaire (`helper/register/{id}`)
3. Je remplis le formulaire avec les information adéquates, je précise notamment mon type de poste favori pour ce raid, puis je valide le formulaire. Je suis alors redirigé vers une nouvelle page (`helper/invite/success/{id}`) 
4. Un message me confirme mon inscription et un bouton me propose d'accéder à mon compte
5. Je clique sur le bouton et suis redirigé vers la liste des raids auxquels je suis inscrit (un seul pour le moment) : `/helper`



## Inscription à un raid avec un compte existant

### Situation de départ

En tant que futur bénévole, avec un compte sur la plate-forme, je veux m'inscrire à un raid. J'ai en ma possession un lien fourni par les organisateurs qui prend la forme `/helper/invite/{id}`.

### Déroulement 

1. Je me rends sur le lien fourni par les organisateurs
2. J'ai déjà un compte, je clique sur le bouton **Se connecter**, je suis redirigé vers une page de formulaire (`helper/join/{id}`)
3. Je rentre mon adresse et mon mot de passe afin de m'identifier et je précise mon type de poste favori pour ce raid. Je valide le formulaire et je suis dirigé vers une nouvelle page (`helper/invite/success/{id}`). 
4. Un message me confirme mon inscription et un bouton me propose d'accéder à mon compte. Sur cette page, je trouve également un lien pour pouvoir télécharger l'application mobile.
5. Je clique sur le bouton **Accéder à mon compte** et suis redirigé vers la liste des raids auxquels je suis inscrit ( `/helper`)