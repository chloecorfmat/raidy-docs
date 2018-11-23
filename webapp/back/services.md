# Services métier

L'application web repose sur une architcture en services. Ces services complètent le modéle MVC classique en sortant le code dit "métier" des controlleurs.

Cela permet nottament d'éviter la duplication de code et de permettre une maintenance simplifiée. Chaque service est contient diverses méthodes permettant d'effectuer des actions sur des Objets métier sans avoir de lien avec le reste de l'application.



## Liste des services et des méthodes

- ContactService
  - *contactsArrayToJson* : Transforme un tableau de contacts en chaine JSON
  - *cloneContacts* : Clone les contacts d'un raid
- FormatService
  - *telephoneNumber* : Formate un numéro de téléphone
  - *mobilePhoneNumber*  : Vérifie que le numéro de téléphone est bien un mobile
- HelperService
  - *updateHelperToPoiFromArray* : attribut un Poi à un Helper
  - *helperToJson* : Transforme un Helper en chaine JSON
  - *checkDataAffectationArray* : Vérifie la validité d'une requête de *check-in* transmis depuis une requête d'API
- PoiService
  - *poiFromArray* : Crée un Poi d'après un tableau associatif
  - *poiToJson* : Transforme un Poi en chaine JSON
  - *poisArrayToJson* : Transforme un tableau de Poi en chaine JSON
  - *updatePoiFromArray* : Met à jour un Poi d'après un tableau associatif et le retourne
  - *checkDataArray* : Vérifie la validité d'un tableau associatif d'une requete
- ProfileService
  - *profileToJson* : Transforme les informations publiques d'un utilisateur en chaine JSON
  - *updateProfileFromArray* : Met à jour un utilisateur depuis un tableau associatif
- PoiTypeService
  - *poiTypeFromForm* : Crée un type de POI depuis un objet de formulaire
  - *updatePoiTypeFromForm* :  Met à jour un type de POI depuis un objet de formulaire
  - *poiTypesArrayToJson* : Transforme un tableau de POI en chaine JSON
- RaidService
  - *raidToJson* : Transforme un Raid en JSON
  - *raidsArrayToJson* : Transforme un tableau de Raids en chaine JSON
  - *cloneRaid* : Clone un raid
- SportTypeService
  - *sportTypeFromForm* : Crée un type de Sport depuis un objet de formulaire
  - *updateSportTypeFromForm* :  Met à jour un type de Sport depuis un objet de formulaire
  - *sportTypesArrayToJson* : Transforme un tableau de Sports en chaine JSON
- TrackService
  - *trackFromArray* : Crée un parcours d'après un tableau associatif
  - *trackToJson* : Transforme un parcours en JSON
  - *tracksArrayToJson* : Transforme un tableau de parcours en JSON
  - *updateTrackFromArray* : Met à jour un tracé depuis un tableau associatif
  - *checkDataArray* : Vérifie la validité d'un tableau associatif d'une requete
- UploadedFileService
  - *saveFile* : Enregistre une image en générant un nom unique dans un dossier et retourne le nom du fichier
  - *generateUniqueFileName* : Génère un nom de fichier unique

