# Summary
* [Introduction](README.md)
* [GitBook](installation/gitbook.md)
* Agilité
  * [Definition of Ready (DOR)](best-practices/DOR.md)
  * [Definition of Done (DOD)](best-practices/DOD.md)
* Application Web
    * [Installation en développement](webapp/installation.md)

    * [Déploiement en production](webapp/deployment.md)

    * [API IGN](webapp/IGN.md)

    * [GrumPHP](best-practices/grumphp.md)

    * [Base de données](webapp/database.md)

    * API
        * [Utilisation de l'API](webapp/API/utilisation.md)
        * [Authentification sur l'API](webapp/API/authentification.md)
        * Routes d'API
            * Helper
              - [Raid](webapp/API/routes/helper/raid.md)
              - [Participants](webapp/API/routes/helper/competitor.md)
              - [Messages](webapp/API/routes/helper/message.md)
              - [Parcours](webapp/API/routes/helper/track.md)
              - [Contacts](webapp/API/routes/helper/contact.md)
              - [POI](webapp/API/routes/helper/poi.md)
              - [Types de POI](webapp/API/routes/helper/poitype.md)
            * Organizer
              - [Raids](webapp/API/routes/organizer/raid.md)
              - [Parcours](webapp/API/routes/organizer/track.md)
              - [Points d'intérêts](webapp/API/routes/organizer/poi.md)
              - [Types de point d'intérêt](webapp/API/routes/organizer/poitype.md)
            - [Authentification](webapp/API/routes/authentification.md)
            - [Profile](webapp/API/routes/profile.md)
            - [Sports](webapp/API/routes/sporttype.md)

    * [Front-end](webapp/front/front.md)

        * [Gulp](webapp/front/gulp.md)

    * Back-end
        * Éditeur
            * API
                * [Parcours](webapp/back/editor/API/track.md)
                * [Helpers](webapp/back/editor/API/helper.md)
                * [Dernière édition](webapp/back/editor/API/lastEdition.md)
                * [POI](webapp/back/editor/API/poi.md)
                * [Types de POI](webapp/back/editor/API/poitype.md)
                * [Sports](webapp/back/editor/API/sporttype.md)
            * [AJAX API](webapp/back/editor/AJAX-API.md)
        * [Collaborateur](webapp/back/collaborator.md)
        * [Services métier](webapp/back/services.md)

    * Architecture
        * [Architecture](webapp/architecture/bundles.md)
        * [Contrôles d'accès](webapp/architecture/ControleAcces.md)
* Applications mobiles
  * [Installation](phoneapp/installation.md)
  * [Configuration](phoneapp/configuration.md)
* [Tests](tests-fonctionnels/tests.md)

  * Application Web
    * Administration
        * [Super administrateur](tests-fonctionnels/webapp/Admin/organizer.md)
        * Organizer 
            * [Contacts](tests-fonctionnels/webapp/Organizer/contacts.md)
            * [Bénévoles](tests-fonctionnels/webapp/Organizer/helpers.md)
            * [Collaborateurs](tests-fonctionnels/webapp/Organizer/collaborators.md)
            * [Epreuves](tests-fonctionnels/webapp/Organizer/races.md)
            * [Raids](tests-fonctionnels/webapp/Organizer/raids.md)
              * [Cloner](tests-fonctionnels/webapp/Organizer/clone.md)
              * [Parcours](tests-fonctionnels/webapp/Organizer/tracks.md)
                * [Points d'intérêt](tests-fonctionnels/webapp/Organizer/pois.md)
        * Helper
            * [Inscription](tests-fonctionnels/webapp/Helper/inscription.md)
            * [Compte utilisateur](tests-fonctionnels/webapp/Helper/account.md)
            * [Raids](tests-fonctionnels/webapp/Helper/raids.md)
        * Live !
            * [Tweets](tests-fonctionnels/webapp/Live/tweets.md)
    * API
        * [Authentification](tests-fonctionnels/webapp/API/authentification.md)
      * [Profil](tests-fonctionnels/webapp/API/profile.md)
      * [Sport](tests-fonctionnels/webapp/API/sporttypes.md)
      * Helper
        * [Raids](tests-fonctionnels/webapp/API/Helper/raids.md)
          * [Parcours](tests-fonctionnels/webapp/API/Helper/tracks.md)
      * Organizer
        * [Raids](tests-fonctionnels/webapp/API/Organizer/raids.md)
          * [Parcours](tests-fonctionnels/webapp/API/Organizer/tracks.md)
          * [Points d'intérêt](tests-fonctionnels/webapp/API/Organizer/pois.md)
          * [Type de points d'intérêt](tests-fonctionnels/webapp/API/Organizer/poitypes.md)
  * Applications mobiles
    * [Connexion](tests-fonctionnels/phoneapp/connexion.md)
    * [Compte utilisateur](tests-fonctionnels/phoneapp/compte.md)
    * Helper
      * [Raid](tests-fonctionnels/phoneapp/helper/raid.md)
      * [Bénévolat](tests-fonctionnels/phoneapp/helper/checkin.md)
    * Organizer
      * [Calibrage](tests-fonctionnels/phoneapp/organizer/calibration.md)


