# Utilisation de l'API IGN

L'application Raidy utilise plusieurs fonctionnalités offertes par l'Institut national de l'information géographique et forestière (IGN) français afin d'offrir certains services :

- Le fond de carte IGN TOP25 ;
- La gestion de l'altimétrie des parcours ;
- La fonctionnalité de tracé automatique, qui exploite l'API de création d'itinéraires.



## Paramétrages de l'API

Afin d'accéder aux services de l'API il est nécessaire d'utiliser une clé dédiée au projet. Cette clé est paramétrable dans le fichier *web/assets/js/variables.js*. 

`const IGNAPIKEY = "choisirgeoportail";`



### Création d'une clé IGN

L'application est livrée avec une clé de développement, fournie par Géoportail. Cette clé ne doit en aucun cas être utilisée en production en dehors de limites fixées par IGN.

La création d'une clé se fait via l'espace professionnels IGN : http://professionnels.ign.fr/

La création d'un clé est gratuite dans le cadre de la license *N°1 - Utilisation des Ressources Géoportail - Utilisateur final Grand Public* . 

