# Tests fonctionnels : Badgeage des participants

###  Situation de départ

En tant que bénévole d'un raid, je veux badges les participants du raid pour indiquer leur passage à un checkpoint.

## Scanner un badge

### Déroulement

1. J'ouvre l'application et me connecte à mon compte.
2. Sur la page qui s'affiche, la liste des raids auxquels je suis inscrit s'affiche. Je clique sur celui désiré.
3. Je clique sur l'inglet **Participants**. La liste des participants au raid s'affiche.
4. Si mon poste d'affectation est un checkpoint, je peux cliquer sur le bouton **Badger les participants**.
5. J'active le NFC sur mon appareil.
6. Je clique sur le bouton **Activer le scan** en haut de la page.
7. Je scanne la puce NFC du badge.
8. Une infobulle m'informe que le passage du participant à été enregistré.
9. Cette information s'affiche également dans l'historique des scans.


## Scanner un badge non associé

### Déroulement

1. J'ouvre l'application et me connecte à mon compte.
2. Sur la page qui s'affiche, la liste des raids auxquels je suis inscrit s'affiche. Je clique sur celui désiré.
3. Je clique sur l'inglet **Participants**. La liste des participants au raid s'affiche.
4. Si mon poste d'affectation est un checkpoint, je peux cliquer sur le bouton **Badger les participants**.
5. J'active le NFC sur mon appareil.
6. Je clique sur le bouton **Activer le scan** en haut de la page.
7. Je scanne la puce NFC du badge.
8. Une infobulle m'informe que badge n'est associé à aucun participant.
9. Cette information s'affiche également dans l'historique des scans.


## Enregistrer un participant qui a perdu son badge

### Déroulement

1. J'ouvre l'application et me connecte à mon compte.
2. Sur la page qui s'affiche, la liste des raids auxquels je suis inscrit s'affiche. Je clique sur celui désiré.
3. Je clique sur l'inglet **Participants**. La liste des participants au raid s'affiche.
4. Si mon poste d'affectation est un checkpoint, je peux cliquer sur le bouton **Badger les participants**.
5. J'active le NFC sur mon appareil.
6. Je saisis le numéro de dossard du participant dans le champs **Numéro de dossard**.
7. Je clique sur le bouton **Checker** afin de valider la saisie.
8. Une infobulle m'informe que le passage du participant à été enregistré.
9. Cette information s'affiche également dans l'historique des scans.


## Scanner un badge sans connexion internet

### Déroulement

1. J'ouvre l'application et me connecte à mon compte.
2. Sur la page qui s'affiche, la liste des raids auxquels je suis inscrit s'affiche. Je clique sur celui désiré.
3. Je clique sur l'inglet **Participants**. La liste des participants au raid s'affiche.
4. Si mon poste d'affectation est un checkpoint, je peux cliquer sur le bouton **Badger les participants**.
5. J'active le NFC sur mon appareil.
6. Je clique sur le bouton **Activer le scan** en haut de la page.
7. Je scanne la puce NFC du badge.
8. Une infobulle m'informe que le passage du participant à été sauvegardé et qu'une synchronisation est requise.
9. Cette information s'affiche également dans l'historique des scans.
10. Lorsque je retrouve une connexion internet, j'actualise la page ou scanne un nouveau badge.
11. Une infobulle m'informe que la synchonisation a été effectuée avec le serveur.