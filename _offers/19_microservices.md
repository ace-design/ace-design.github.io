---
title: Déploiement à la carte de micro-services

people:
  - seb
  - naouel

level: graduate  
language: FR

layout: offer
last-updated: 2018-11-30
---

## Contexte du projet

Les micro-services sont un paradigme de développement récent qui met en œuvre des principes beaucoup plus anciens : architectures hexagonales (Cockburn, 2005) et Conception pilotée par le domaine (Evans, 2003). Dans ce paradigme, les fonctionnalités métiers sont implémentés via un ou plusieurs micro-services dont les API publiques sont exposée à leurs consommateurs et qui communiquent entre eux par l’envoi de messages sur un bus (par exemple Kafka).

Dans ce projet, nous proposons d’explorer comment établir et maintenir une traçabilité entre les fonctionnalités métiers (par exemple définies par des récits utilisateurs), les services développés et les messages échangés entre ces services. Sur la base de ce modèle de trace, on pourra mettre en œuvre un mécanisme de déploiement à la carte permettant l’activation ou la désactivation de certaines fonctionnalités métiers en fonction des récits choisis pour un déploiement donné.


## Travail à réaliser

Les objectifs du projet sont les suivants :

1.	Implémenter une petite architecture de micro-services en utilisant les technologies de l’état de l’art (par exemple nodeJs, kafka), en lien avec une spécification agile (par exemple Github Project pour héberger des récits utilisateurs et Cucumber pour écrire des scénarios d’acceptation utilisateur) ;
2.	Définir un analyseur de code pour identifier les liens implicites entre fonctionnalités sur la base des messages échangés ;
3.	Permettre le déploiement à la carte de sous-ensemble de services sur la base des liens de traçabilité et des liens implicites découverts.

Si le temps le permet, en fonction de l’avancé sur les points précédents :

4.	Mettre en place des mécanismes de supervisions pour observer des déploiements et affiner dynamiquement les résultats de l’analyse statique (qui seront par nature sur-contraint) ;
5.	Appliquer l’outil développé à des systèmes de micro-services disponible sur Github ou Gitlab.

## Organisation de l’équipe

L’équipe travaille de façon agile, plus particulièrement via la
définition de récits utilisateurs pour décrire les fonctionnalités à développer
et un rythme de livraison (démonstration & rétrospective) hebdomadaire.
