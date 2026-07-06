# INCEpTION

Dernière modification de la fiche : 6/07/2026

Version testée : 41.0

Site web : https://inception-project.github.io/

Code : https://github.com/inception-project/inception

Citer le logiciel : 

>Klie, J.-C., Bugert, M., Boullosa, B., Eckart de Castilho, R. and Gurevych, I. (2018): The INCEpTION Platform: Machine-Assisted and Knowledge-Oriented Interactive Annotation. In Proceedings of System Demonstrations of the 27th International Conference on Computational Linguistics (COLING 2018), Santa Fe, New Mexico, USA

![](../../img/inception.png)

## Description générale

*A quoi sert le logiciel ? : les principales fonctionnalité du logiciel, sa philosophie transversale*

Inception est un logiciel d'annotation dédié à annoter collaborativement des documents avec un système de gestion des droits et d'intégration de recommandations automatiques.

INCEpTION est une application open source d'annotation de textes destinée à des tâches d'analyse linguistique et sémantique sur des documents écrits, accessible par une interface web. Plusieurs utilisateurs peuvent travailler simultanément sur un même projet, et une seule installation peut héberger de nombreux projets en parallèle. L'outil s'organise autour de projets configurables où l'on définit des couches d'annotation (spans de texte, relations, chaînes de coréférence), des jeux d'étiquettes (tagsets) et des bases de connaissances permettant de lier les annotations à des entités externes comme Wikidata. INCEpTION gère également l'ensemble du cycle de vie d'un projet d'annotation : répartition des tâches entre annotateurs, suivi de la charge de travail, mesure de l'accord inter-annotateurs, et curation (adjudication) pour réconcilier les annotations divergentes de plusieurs personnes en un résultat final unique. Il propose enfin des fonctionnalités avancées comme la recherche dans les annotations, la constitution de corpus à partir de dépôts documentaires externes, et l'import/export dans de nombreux formats.

## Licence

*Conditions légale d'adoption : licence du logiciel \& prix*

PHRASE DE SYNTHESE

DETAILS

## Installation

*Conditions matérielles d'usage : sous forme de service (oui/non et sur quel serveur en terme de sécurité ; limite en terme de navigateur / adaptabilité smartphone) ; logiciel à installer (sur quel OS ? Windows, Mac, Linux) ; Niveau de complexité, notamment ligne de commande ? Existance d'une logique de plugin*

Possibilité de tester en ligne puis de déployer une instance avec Docker, l'installation complète est possible.

Le logiciel repose sur une architecture assez lourde (Java, Base de donnée, etc.). Le déploiement en production directement peut être assez compliquée.

## Corpus 

*Les corpus possibles traitables : Texte, Audio, Video, Images, PDF, Multimodal, Réseaux sociaux, etc.*

Le logiciel est dédié pour les documents textuels avec un focus documents et non pas corpus tabulaire.

DETAILS

## Interopérabilité

*Degré d'interopérabilité : formats d'échange des données, import et export*

PHRASE DE SYNTHESE

DETAILS

## Communauté

*Support communautaire à l'usage francophone : où trouver de l'aide / diffusé dans les réseaux métiers / tutoriaux disponibles*

PHRASE DE SYNTHESE

DETAILS

## Collaboratif

*Collaboratif : conditions de collaboration, extension de la collaboration*

PHRASE DE SYNTHESE

DETAILS

## IA

*Place de l'IA dans le logiciel : présent ou pas ; optionnel (et désactivable) ou au coeur de l'outil, possibilité de choisir les modèles utilisés, outil augmenté par l'IA ou outil pensé pour l'IA*

PHRASE DE SYNTHESE

Son système de recommandation intégré apprend des annotations déjà réalisées pour suggérer de nouvelles annotations au fil du travail, et une fonction d'apprentissage actif aide à traiter en priorité les cas incertains. 