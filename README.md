# Gestion_de_conges
Création Gestion de congé en Full-Stack : 
## Installation

Installer les dépendences:

### Client
- Node.js
- npm
- Angular

### Serveur
- Java
- Maven
- Spring Boot
- My SQL 

```
pushd client
npm install
popd
```

## Utilisation

A partir de la racine du projet, éxécuter la commande `./start`, qui s'occupe de lancer le client et le serveur.

## Structure

La structure du projet est la suivante:

-SERVER-

- Config : La configuration de Spring .
- Controller : Un contrôleur est une classe Java portant l'annotation @Controller. L'objectif d'un contrôleur est de réagir à une interaction avec l'utilisateur, cela signifie que l'utilisateur envoie des requêtes HTTP au serveur. Elles sont traitées par les services, qui retournent les résultats sous forme de DTO.
- DTO :  (Data Transfer Object, en anglais) est un patron de conception utilisé dans les architectures logicielles objets. Son but est de simplifier les transferts de données entre les sous-systèmes d'une application logicielle. 
- Entités : Une entité est une instance d'une classe qui sera persistante (que l'on pourra sauvegarder dans / charger depuis une base de données relationnelle). Une entité est signalée par l'annotation @Entity dans la classe. Elle appartient en général à un repository (une table de base de données). 
- Enums : Ce sont les énumérations métier ( A PRECISER).
- Repositories :  @Repository est une annotation Spring pour indiquer que l’interface a pour rôle de communiquer avec les tables de base de données, via JPA, donc ça contient optionnellement des méthodes de requête.
- Services : Traite les requêtes venant du contrôleur, en s'aidant des repositories. C'est là que repose le cœur du métier. 
- Security : Implémentation de l'authentification Spring via un Salarie. 
- Helpers : Les helpers sont des classes outils qui contiennent du code susceptible d'être utilisable partout dans une application.

-CLIENT- 

- Guards : Gère qui peut accéder à certains chemins de l'application (si l'utilisateur est connecté ou a les droits pour) // 
- Localisation : Traduction du texte de l'application.
- Model : Equivalent aux entités du côté serveur, c'est les objets métier.
- Services : Gère la communication avec le serveur, effectue les requêtes pour obtenir et transmettre les informations (ça touche aux contrôleurs du serveur).
- Site : Les pages et composants du site, en général ça injecte des services pour communiquer avec le serveur. Ces pages contiennent un module qui spécifie la route vers celle-ci, et un composant qui définit la logique (.TS) et le contenu de la page (.HTML/.CSS).
- Shared : Les composants partagés entre les pages, y compris la barre de navigation et les validateurs de formulaire.

## Convention de nommage 

Pour la partie code en JAVA, les conventions de nommage seront :
- Package : Le nom du package doit être en minuscule (ex : project, java ...).
- Classes : Les classes commencent par une lettre majuscule et doivent être de type « Nom »
(ex : Button, Object ...).
- Méthodes : Les méthodes doivent commencer par une lettre minuscule et être de type
« Verbe » (ex : create(), check() ...).
- Variables : Les variables doivent commencer par une lettre minuscule (ex : name, number).
- CamelCase : Si le nom d’une classe/méthode/variable est composé de deux mots ou plus,
chaque mot suivant doit commencer par une lettre majuscule (ex :firstName,checkPassword()…).

Pour la partie Base de données SQL, les conventions de nommages seront :  Ne pas utiliser les mots réservés (date, delete, add …), Ne pas utiliser de caractères spéciaux ,  Eviter les majuscules, privilégier les underscores pour l’utilisation de deux mots (ex : « date_inscription » plutôt que « DateInscription »), Eviter l’utilisation d’abréviation.
 Noms des tables : Utiliser un nom représentatif du contenu, utiliser un seul mot si possible, préfixer les noms des tables (ex : user_data, company_data …), Noms des colonnes : Préfixer toutes les colonnes de la même façon pour chaque table (plus pratique pour les jointures), Global : Ecrire en anglais.




