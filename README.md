# CAS Projet 5A

## Lancer le serveur CAS

Clonez ce dépôt sur votre ordinateur : 
```
https://github.com/AurelienBriot/cas-projet-5A.git
cd ./cas-projet-5A
```

Construisez et démarrez l'image Docker (cela peut prendre plusieurs minutes) :
```
docker compose up
```

Le serveur CAS sera disponible à l'adresse http://localhost:9090.
Deux utilisateurs sont disponibles : `user` avec le mot de passe `password`, et `admin` avec le mot de passe `admin`.

## Ajouter un nouvel utilisateur

Rendez-vous dans le fichier `/etc/cas/config/application.properties`. Ajoutez un nom d'utilisateur et un mot de passe de la façon `utilisateur::motdepasse` à la fin de la propriété `cas.authn.accept.users`. Attention il ne doit pas y avoir d'espaces !

Ces utilisateurs sont à utiliser à des fins de tests, étant donné qu'ils sont stockés en clair.

## Tester avec l'application

Assurez-vous d'avoir démarré le serveur CAS. Sur l'application, basculer sur la branche `ConnexionCAS`, et lancez l'application.

Rendez-vous à l'adresse http://localhost:8080/accueil. Vous y trouverez un bouton de connexion qui redirigera vers le CAS.

## Configuration du CAS sur l'application

La configuration du CAS dans l'application s'effectue dans le fichier `application.yaml`. Vous pouvez y configurer les adresses de connexion, de déconnexion mais aussi les pages nécessitant une authentification par le CAS.
