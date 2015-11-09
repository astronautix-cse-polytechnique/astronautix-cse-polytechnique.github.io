---
author: Etienne Houzé
comments: false
date: 2015-11-08 23:00:00+00:00
layout: article
slug: lancement-x-cube-sat
title: X-CubeSat, un lancement prévu fin 2016
---


*Le premier nano-satellite étudiant du Centre Spatial Etudiant ! Le lancement est prévu pour la fin 2016, le projet est donc dans sa phase de finalisation*

## Historique du projet

Le projet X_CubeSat s’inscrit dans le cadre de la coopération internationale QB50. Piloté par le Von Karman Institute for Fluid Dynamics à Bruxelles, le projet QB50 est le premier projet d’envoi d’une constellation de 50 CubeSat (c’est-à-dire des nanosatellites de taille 10cm*10cm*20cm) pour optimiser les mesures scientifiques prises en orbite. L’objectif du projet QB50 est de montrer qu’il est possible d’envoyer un réseau de cinquante nanosatellites fabriqués par des étudiants d’universités du monde pour étudier la basse thermosphère. Au programme donc : recherche scientifique, démonstration technologique, simplification de l’accès à l’espace, formation d’étudiants.

Une équipe de polytechniciens de la promotion X2010 a préparé et envoyé un dossier de candidature au Von Karman Institute pour la réalisation d’un de ces CubeSat. L’École Polytechnique a ensuite été retenue pour faire partie de la coopération internationale QB50. L’équipe d’X 2012 a réalisé le modèle de qualification, c’est-à-dire le modèle sur lequel on réalise les tests mécaniques, thermiques, logiciels.

L'équipe d'X 2013 s'est donc chargée en grande partie de la partie software du satellite, notemment l'ordinateur de bord, ainsi que du système de contrôle d'attitude par bobines magnétiques, l'ADCS. Elle s'est aussi chargée de la réalisation d'une sstation sol composée d'antennes radio, de modems et d'un pc qui pourra ainsi communiquer avec le satellite lors de sa mission.

La promotion X2014 est l'équipe actuellement en charge du projet, et sera la dernière à travailler sur le satellite, étant donné que la livraison est prévue pour février 2016. Le lancement, lui, sera effectué en deux étapes : tout d'abord, un lanceur pour le moment indéterminé enverra la constellation QB50 sur la Station Spatiale Internationnale (ISS), puis les nano-satellites seront envoyés sur leur orbite par un bras robotique de la Station.

## L'état actuel du projet

### La mécanique

Globalement, la structure mécanique du satellite est déjà bien avancée grâce au travail
effectué les années précédentes. Il reste à faire les derniers ajustements et finir les dessins
numériques pour que le modèle de vol pouisse être réalisé et le satellite livré.

La structure du satellite est composée des parties suivantes :
* l’interface FIPEX, qui adapte la sonde FIPEX sur le châssis ;
* le châssis, qui contient les cartes électroniques et sert de soutien aux panneaux solaires
et autres composants structurels du satellite ;
* l’embase, qui lie le châssis, les cartes électroniques et le boîtier antennes, et qui contient
des interrupteurs pour les batteries et pour allumer le satellite au lancement ;
* le boîtier antennes, avec les antennes et leur mécanisme de déploiement.

Les dernières tâches à effectuer sont :
* optimiser la structure, l’antenne doit être refaite avec un matériau plus rigide que du
mètre ruban ;
* tester en vibration et en vide thermique le satellite pour valider la FRR ;
* mettre à jour les dessins numériques du satellite sur le logiciel CATIA et réaliser les
dessins techniques demandés par le VKI.


### Le contrôle d'attitude : l'ADCS

L’objectif de notre année est de parvenir à une carte ADCS (Attitude Determination and
Control Subsystem) fonctionnelle et intégrée au CubeSat, en partant du travail déjà réalisé
les années précédentes. Le fonctionnement de notre ADCS étant totalement nouveau, nous
n’utilisons pas de roue à inertie, il a fallu prouver la fiabilité de notre système grâce à de
nombreuses simulations.

Notre travail consiste donc dans un premier temps à nous approprier les algorithmes de
détermination et de contrôle d’attitude qui ont été écrits l’année dernière. Les simulations
ont été effectuées sur Matlab en partenariat avec l’école des Mines qui développe un CubeSat
similaire au notre. Il nous faudra ensuite écrire le logiciel pour la carte électronique et mener
les tests pour nous assurer de son bon fonctionnement.

### La sonde FIPEX

La sonde FIPEX constitue la charge utile du satellite : elle permet de mesurer avec précision
le taux de dioxygène ambiant. Elle ne sera néanmoins pas activée en permanence sur la durée
de vie du satellite. Elle nécessite en effet un contrôle précis d’attitude, c’est-à-dire garder une
inclinaison constante, pour fournir des mesures correctes. Ce contrôle étant couteux en énergie,
il est nécessaire de le couper de temps en temps afin de recharger les batteries. De plus des
mesures ponctuelles à différentes altitudes restent des données expérimentales satisfaisantes.

Cette sonde doit donc être coordonnée par l’ordinateur de bord. C’est pourquoi nous devons
comprendre son fonctionnement afin de pouvoir rendre possible ce contrôle. Olivier Piras étant
chargé d’écrire le code de l’ordinateur de bord, cette mission consiste à lui décrire précisément
les différents modes de fonctionnement de la sonde et l’interface entre celle-ci et l’ordinateur de
bord. La date prévue pour l’implémentation de cette fonctionnalité dans l’ordinateur de bord
est le 15 décembre. Pour mener à bien cet objectif, nous comptons utiliser la documentation
fournie par le VKI à propos de la sonde ainsi que d’un logiciel d’émulation de celle-ci pour
vérifier la bonne compréhension de son fonctionnement.

### La station sol

La station sol est un élément vital du projet X-CubeSat. En effet, elle sera le seul intermé-
diaire entre l’équipe au sol et le satellite durant sa durée opérationnelle, et devra donc permettre
une communication claire et sans erreur des ordres avec le satellite, ainsi qu’une réception et
un traitement des données reçues. Notre travail, sera dans un premier temps de concevoir et
réaliser un logiciel muni d’une interface graphique qui devra effectuer les taches suivantes :
* réception des télémétries envoyées par le satellite (position, attitude, charge des batteries,
températures,...) et transcription des données brutes dans un format lisible ;
* envoi et transcription de commandes vers le satellite, via l’antenne dont est munie la
station sol ;
* affichage au sein d’une interface graphique des différentes données reçues et émises,
principalement sous l’aspect de graphiques ;
* affichage d’un satellite en 3D permettant de visualiser l’attitude du satellite réel ;
* mise à jour des différentes données utilisées à chaque passage en visibilité du satellite.

Le langage de programmation utilisé sera le C++, et l’interface sera produite grâce à la bibliothèque
Qt. Dans la suite du projet, il sera probablement nécessaire d’écrire de petits programmes
qui se chargeront de convertir les données reçues dans le format spécifié par le VKI, ainsi que
de prendre en main la station sol pour s’entraîner au suivi d’un satellite lors de son passage en
visibilité.

### Les TLE (Two-Line Elements)

Dans le cadre de la surveillance des satellites en orbite basse, on utilise un système de
coordonnées appelé TLE (Two Line Element). Il est composé de différents nombres caractérisant
l’orbite et la position du satellite sur celle-ci. Notre satellite récupère cette information mais le
système a besoin de la position sous un format (x,y,z) dans un repère donné. Ces informations
sont ensuite transmises à la station sol qui peut avoir besoin des TLE notamment pour les
comparer à des mesures extérieures. Les programmes de conversion (TLE vers (x,y,z) embarqué
sur le satellite, (x,y,z) vers TLE à la station sol) doivent donc être écrits et implémentés dans
leurs systèmes respectifs.


## L'équipe actuelle

L'équipe actuelle du X-CubeSat est constituée de :

* Clément Verlhac, chef de projet et responsable de la sonde FIPEX
* Tomas Lopez, responsable mécanique
* Adrian Valente et Lucas Gonzalez, responsables de l'ADCS
* Thomas Villard, responsable de la conversion des TLE
* Paul Godefroy et Etienne Houzé, responsables de la station sol




