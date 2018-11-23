# Tests fonctionnels : Les raids pour l'API - Organizer



## Récupération des raids liés à l'organisateur

###  Situation de départ

En tant qu'organisateur utilisateur de l'API, avec jeton d'authentification, je souhaite récupérer la liste des raids que j'ai créé.

### Déroulement 

1. J'emet une requête **HTTP GET** à l'adresse : `/api/organizer/raid`

2. La réponse à cette requête à pour code HTTP **200** et contient la liste des raids dans une chaine JSON :

   ```json
   [{
     "id": 1,
     "name": "Mon super raid",
     "date": {
       "date": "2018-11-04 00:00:00.000000",
       "timezone_type": 3,
       "timezone": "UTC"
     },
     "address": "15 Rue Du Fer à Cheval",
     "addressAddition": "",
     "postCode": 35160,
     "city": "TALENSAC",
     "editionNumber": 1,
     "picture": "120919b85d8ce9b7eb4336b569c9b6e3.jpeg"
   }, {
     "id": 2,
     "name": "Raid des Bruyères",
     "date": {
       "date": "2018-11-17 00:00:00.000000",
       "timezone_type": 3,
       "timezone": "UTC"
     },
     "address": "18 Rue de la Forêt",
     "addressAddition": "",
     "postCode": 35160,
     "city": "MONTFORT-SUR-MEU",
     "editionNumber": 2,
     "picture": "d32b8dca243c6d2f8250d0838c9aa8b5.jpeg"
   }]
   ```