# Installation en développement


## Pré-requis

__Pour installer et faire fonctionner l'application il faut :__

- **[Node.js](https://nodejs.org)**

## Installation de PhoneGap

1. Cloner le projet git `git clone git@github.com/chloecorfmat/into-the-woods-phoneapp-helper.git` pour l'application Helper.
2. Cloner le projet git `git clone git@github.com/chloecorfmat/into-the-woods-phoneapp-organizer.git` pour l'application Organizer.
3. Télécharger **[PhoneGap](http://docs.phonegap.com/getting-started/1-install-phonegap/desktop/)**
4. `npm install` pour télécharger les modules requis
5. `cordova prepare` pour importer les plugins cordova et les plateformes
6. `gulp` pour générer les fichiers de style
7. `phonegap serve` pour tester l'application dans phonegap

# Déploiement des applications

Pour déployer les applications, il faut disposer d'un compte [Adobe PhoneGap Build](https://build.phonegap.com/). Via l'interface en ligne, il est possible d'importer un dossier zippé contenant le répertoire `www/` et le fichier `config.xml`. Les commandes `phonegap remote` permettent la même chose.

# Utilisation de fichiers apk

Phonegap permet de créer des fichiers **apk**. Pour installer une application à partir de ce type de fichier, il faut autoriser les éditeurs non vérifiés à installer des applications sur l'appareil, via les paramètres de sécurité. Ensuite, l'ouverture du fichier apk lance l'installation.