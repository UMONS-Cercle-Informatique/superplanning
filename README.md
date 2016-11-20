# Superplanning

Superplanning - Gérez mieux votre planning.

## Qu'est-ce Superplanning ?

Hyperplanning est un logiciel de gestion de planning utilisé par plusieurs
établissement d'études supérieures, dont l'UMONS. Par exemple, on peut trouver
le planning pour l'année académique 2016-2017
à [cette adresse](https://hplanning2016.umons.ac.be).

Hyperplanning n'est pas user-friendly au niveau de l'utilisation. L'interface
est assez horrible et de plus, elle n'est pas responsive pour le mobile. Et ces divers problèmes sont très critiqués par les étudiants.

Le projet Superplanning est là pour apporter une nouvelle interface, web et mobile, à Hyperplanning.
Le projet dispose de plusieurs sous-projets:

- [le backend](https://github.com/UMONS-Cercle-Informatique/superplanning-backend) qui contient tous les horaires (récupérés grâce aux fichiers iCal provenant d'hyperplanning) et qui fournit une interface REST pour les clients.

- [le frontend](https://github.com/UMONS-Cercle-Informatique/superplanning-frontend), le client web.
- [l'application mobile native Android](https://github.com/UMONS-Cercle-Informatique/superplanning-android-native), l'application mobile native Android (client).
- [l'application mobile native iOS](https://github.com/UMONS-Cercle-Informatique/superplanning-ios-native), l'application mobile native iOS (client).

## Backend.

Le backend contient une base de donnée comportant tous les horaires. Il est séparé en deux services.

1. Récupération des fichiers iCal d'hyperplanning, grâce à un headless browser, et importations des horaires dans la base de données.
2. Interface REST pour les clients du genre `section/annee/?cours`.

## Clients.

Les 3 derniers sous-projets que sont l'interface web et les applications mobiles
natives sont les clients qui font appels au backend.

Elles consistent à fournir des interfaces plus modernes et plus utilisables que
celle d'hyperplanning.

## Stack

Le projet se veut être éducatif pour les personnes participantes. Des choix ont
été réalisées pour apprendre en premier lieu, non pour l'efficacité ou la
maintenabilité. Les différentes technos utilisées sont:

- SGBD: PostGreSQL.
- Backend - récupération fichier iCal et importation dans la BDD: Python 3+, Selenium.
- Backend - API REST: SmallTalk (Pharo) + Teapot.
- Client Web: Java, Play Framework, Bootstrap.
- Client Android: natif, Java.
- Client iOS: natif, iOS.
