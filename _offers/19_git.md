---
title: Analyse des conflits de fusion dans Git

people:
  - seb
  - ben

level: graduate  
language: FR

layout: offer
last-updated: 2018-11-30
---

## Contexte du projet

Git est le gestionnaire de version le plus utilisé actuellement. Un des gros
problèmes lors de l’utilisation de ce gestionnaire de version est le traitement
des fusions de code conflictuelle, quand un développeur ou une développeuse
souhaite intégrer dans sa branche de développement des modifications provenant
d’une autre branche, qui ne sont pas compatible avec les modifications qu’il ou
elle a lui-même effectué. Dans ce projet, nous souhaitons cartographier les
différents types de conflits rencontrés par la communauté du logiciel libre, en
analysant des projets logiciels disponible sur les plateformes communautaires
Github et GitLab.  

## Travail à réaliser

Les objectifs du projet sont les suivants :

1. Définir une bibliothèque logicielle capable d’analyser un projet hébergé dans
un dépôt Git en collectant les commits de fusion ainsi que des métriques
associées au projet (nombre de contributeurs, quantité de code source impliqué, …) ;
2.	Lancer une campagne de collecte qui viendra compléter le corpus amorcé dans
l’équipe à l’été 2018 ;
3.	Analyser les commits conflictuels , en collectant
quantitativement des métriques les concernant (par exemple le nombre de
marqueurs de conflits, la taille des conflits en lignes de codes) ;
4.	Qualifier qualitativement (par exemple « déplacement d’une méthode », « encodage de caractères », « espaces contre tabulations », « renommage d’une variable ») les  différents types de conflits et définir des règles permettant de catégoriser le corpus constitué.

Si le temps le permet, en fonction de l’avancé sur les points
précédents :

5.	Définir des règles de réécriture de code pour résoudre les
conflits les plus fréquents;
6.	Intégrer ces réécritures dans Git.

## Organisation de l’équipe

L’équipe travaille de façon agile, plus particulièrement via la
définition de récits utilisateurs pour décrire les fonctionnalités à développer
et un rythme de livraison (démonstration & rétrospective) hebdomadaire.
