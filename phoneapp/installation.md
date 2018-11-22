# Installation


## Pré-requis

Pour installer et faire fonctionner l'application il faut :

- **[Node.js](https://nodejs.org)**

## Installation de PhoneGap

Cloner le projet git `git clone git@github.com/chloecorfmat/into-the-woods-phoneapp-helper.git` pour l'application Helper.
Cloner le projet git `git clone git@github.com/chloecorfmat/into-the-woods-phoneapp-organizer.git` pour l'application Organizer.

Télécharger **[PhoneGap](http://docs.phonegap.com/getting-started/1-install-phonegap/desktop/)**

`npm install` pour télécharger les modules requis

`cordova prepare` pour importer les plugins cordova et les plateformes

`gulp` pour générer les fichiers de style

`phonegap serve` pour tester l'application dans phonegap

# Déploiement des applications

Pour déployer les applications, il faut disposer d'un compte [Adobe PhoneGap Build](https://build.phonegap.com/). Via l'interface en ligne, il est possible d'importer un dossier zippé contenant le répertoire `www/` et le fichier `config.xml`. Les commandes `phonegap remote` permettent la même chose.