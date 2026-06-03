# Doccano

Dernière modification de la fiche : 3/06/2026

Version testée : 1.8.5

Site web : [https://doccano.web.webis.de/fr](https://doccano.web.webis.de/fr)

Code : [https://github.com/doccano/doccano](https://github.com/doccano/doccano)

## Description générale

*- A quoi sert le logiciel ? : les principales fonctionnalité du logiciel, sa philosophie transversale*

Logiciel d'annotation "pour les humains" qui fonctionne avec un serveur et un client web par le navigateur, et permet de travailler à plusieur sur un même projet. Il permet différents types de tâches : classification de textes, de séquences textuelles, d'images, d'objets (segmentation). Il est multilingue avec une interface fluide pour faciliter l'annotation des éléments. Néanmoins, il semble moins maintenu et ne parait pas avoir une dynamique très forte d'usage dans la recherche. 

## Licence

*- Conditions légale d'adoption : licence du logiciel \& prix*

Logiciel libre sous MIT license

## Installation

*- Conditions matérielles d'usage : sous forme de service (oui/non et sur quel serveur en terme de sécurité ; limite en terme de navigateur / adaptabilité smartphone) ; logiciel à installer (sur quel OS ? Windows, Mac, Linux) ; Niveau de complexité, notamment ligne de commande ?*

Doccano est développé en Python. Son installation est possible directement en Python (3.8). Il peut y avoir quelques soucis sous Windows + il faut bien penser à prendre une version 3.8+ de Python pour l'installation. Il y a aussi un docker permet de déployer l'instance rapidement.

## Corpus 

*- Les corpus possibles traitables : Texte, Audio, Video, Images, PDF, Multimodal, Réseaux sociaux, etc.*

Doccano permet d'annoter des données textuelles et des images. Les données textuelles sont chargées sous la forme de tableaux. Les formats d'entrées sont assez variés : csv, plain text, excel, jsonl, CoNLL.


## Interopérabilité

*- Degré d'interopérabilité : formats d'échange des données, import et export*

Doccano prend en entrée des données tabulaires et permet l'extraction des données annotées. L'export des annotation se fait en jsonl. Le chargement des corpus n'est pas entièrement fluide (choix des colonnes de métadonnées, vues du dataset, ...).

## Communauté

*- Support communautaire à l'usage francophone : où trouver de l'aide / diffusé dans les réseaux métiers / tutoriaux disponibles*

La documentation officielle : https://doccano.github.io/doccano/

La communauté est assez restreinte. S'il a 10k étoiles sur Github, il est peu cité dans les articles francophones de sciences sociales. Il y a peu de tutoriaux communautaires sur le sujet. 

## Collaboratif

*- Collaboratif : conditions de collaboration, extension de la collaboration *

Doccano permet de faire de l'annotation multiutilisateur. Il y a plusieurs modes : annotation parallèle, ou annotation collective. Par contre il n'y a pas de logique d'arbitrage entre les désaccords d'annotation. 

## IA

*- Place de l'IA dans le logiciel : présent ou pas ; optionnel (et désactivable) ou au coeur de l'outil, possibilité de choisir les modèles utilisés, outil augmenté par l'IA ou outil pensé pour l'IA*

Doccano donne la possibilité de faire de l'auto-annotation en s'appuyant sur une API web externe https://doccano.github.io/doccano/advanced/auto_labelling_config/ (auto-labeling feature). Il est donc possible de construire ses propres annotateurs externes (quelle que soit la technologie) et l'utiliser pour l'annotation.