# Contrôle d'acces

## Configuration de Symfony

### Roles

Afin de gérer les controles d'accès aux différents parties de l'application 3 rôles ont été créés :

- **Super Admin** : Administrateur de l'application, il a accès aux outils d'administration, la gestion des compte nottament
- **Organizer** : Organisateurs de raids
- **Helper** : Bénévoles

### security.yml

Ces rôles sont définis dans la partie `role_hierarchy` du fichier `app/config/security.yml`

Ce fichier comprend également la configuration des accès en fonction de l'url. On peut ainsi désigner les rôles qui ont accès aux différents partie de l'application web. Ainsi, seul les super administrateurs peuvent accèder aux adresse commençant par `/admin`avec la configuration suivante : `- { path: ^/admin, role: ROLE_SUPER_ADMIN }`



## *Voter* : gestion de l'accès aux ressources

Les controles d'accès basés sur le rôles de l'utilisateur permettent de restreindre l'accès à certaines partie de l'application mais ne suffisent pas pour limiter l'accès à certaines ressources.

Afin d'éviter qu'un organisateur ne puisse modifier un raid qui ne lui appartient pas il faut limiter l'accès à certaines pages aux propriétaires des ressources. C'est le rôle des *Voter* de Symfony.

Un *voter* permet de vérifier certaines informations puis de valider ou non l'accès à certaines ressources. 

Pour utiliser un *Voter* on utilise l'*authorization checker* de Symfony et on utilise la fonction *isGranted* en précisant le *Voter* et la ressource dont l'accès doit être vérifié. 

```php
$authChecker = $this->get('security.authorization_checker');
if (!$authChecker->isGranted(RaidVoter::EDIT, $raid)) {
    throw $this->createAccessDeniedException();
}
```

Dans le cas présenté ci-dessus on utilise le *RaidVoter* pour vérifier que l'utilisateur courant a bien les droits suffisants pour modifier un raid (ie. il est le créateur).

Ce *Voter* est placé dans le répertoire `OrganizerBundle/Security/RaidVoter.php`.