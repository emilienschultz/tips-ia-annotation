# LibreQDA

Dernière modification de la fiche : 18/09/2026

Version testée : v1.2

Site web : [https://aide.libreqda.org/](https://aide.libreqda.org/)

Code : [https://gitlab.com/bin-cirst/libreqda/libre-qda](https://gitlab.com/bin-cirst/libreqda/libre-qda)

## Description générale

*Logiciel libre d’annotation thématique de corpus textuels, conçu comme une solution simple et collaborative pour l’analyse qualitative.*

LibreQDA est un logiciel libre d'annotation de thèmes dans un corpus de documents textuels, porté par la
[Plateforme en humanités numériques (phun)](https://www.usherbrooke.ca/flsh/recherche/centres-groupes-et-equipes-de-recherche/phun) de l'Université de Sherbrooke (Canada).  
Il permet de définir ses codes, puis, après avoir annoté, de retrouver et d'étudier les thématiques choisies à l'aide d'un explorateur. L'outil se veut simple d'accès et n'embarque ([volontairement](https://www.usherbrooke.ca/flsh/actualites/nouvelles/details/54194)) que très peu de fonctionnalités d'analyse ou de quantification.
Une sélection d’extraits encodés ou le projet en entier peuvent être exportés.  
Un gros atout est la possibilité de collaborer avec d'autres personnes dans toutes ces étapes.

<!-- Aviser si mon ajout sur le peu de fonctions analyse / quanti vous semble pertinent, l'impression que c'est une revendication des dev face usine à gaz caqdas modernes -->

## Licence

*Logiciel libre et gratuit d'usage sous licence BSD 3-Clause.*

## Installation

*LibreQDA peut être accédé en ligne, installé localement ou déployé sur un serveur.*

Une instance est disponible en ligne sur <https://libreqda.org/>. Elle pose néanmoins la question du RGPD : l'hébergement sur un serveur universitaire au Canada suppose une sortie des données de l'UE (qu'il sera nécessaire de signaler pour validation dans votre déclaration RGPD).

L'installation en local est possible sous Linux, Mac ou Windows :

- ~~via un installateur prêt à l'emploi pour Windows et Mac~~ (TODO : PAS POUR L'INSTANT)
- en ligne de commande via pip (demande l'ouverture d'un terminal)
- via Docker
  
<!-- TODO: info pour ceux qui veulent (aviser au nettoyage)

Les étapes de l'installation pip nécessitent en réalité une modification du fichier de config
version officielle :
```
pip install libreqda
libreqda default-config > libreqda.conf
libreqda server libreqda.conf
```
il faudra en réalité modifier le fichier libreqda.conf avant de lancer le serveur pour :
- créer un chemin valable pour DATABASE (ie modifier DATABASE = "sqlite:////non/existent/taguette/database.sqlite3" avec votre chemin utilisateur / dossier cible
- préciser un fichier tos (TOS_FILE = 'tos.html') ou passer la modalité à None (TOS_FILE = None)

Pour la version dev, les étapes indiquées sont obsolètes (modif poetry)
https://gitlab.com/bin-cirst/libreqda/libre-qda/-/work_items/30

Workaround : 
```bash
git clone https://gitlab.com/bin-cirst/libreqda/libre-qda/
cd libre-qda
poetry env use python3.11
poetry install
poetry run bash scripts/update_translations.sh
poetry run libreqda --debug
```

ou :
```bash
git clone https://gitlab.com/bin-cirst/libreqda/libre-qda/
cd libre-qda
poetry env use python3.11
poetry install
eval $(poetry env activate)
bash scripts/update_translations.sh
libreqda --debug
```
-->

## Corpus

*Logiciel orienté vers les données textuelles (pas de prise en charge image / audio / vidéo).*

- des fichiers textes : pdf, texte, odt, docx, html, epub, mobi, rtf
- (pas de prise en charge image / audio / vidéo)

## Interopérabilité

*Le logiciel permet l'import/export de données dans des formats standards.*

Un projet entier peut être exportée en base sqlite3.  
Les sous-éléments peuvent également être exportés dans différents formats :

- Codebook : CSV, DOCX, Excel, HTML, PDF
- Coded selections : CSV, Excel, HTML, PDF
- Documents : DOCX, HTML, PDF

L'interopérabilité reste partielle (pas de standard REFI-QDA, etc.)
<!-- TODO : aviser si on n'est plus dur ici côté interopérabilité que sur d'autres logiciels ? -->

## Communauté

*Un logiciel porté par la communauté universitaire canadienne en SHS, encore peu adopté en France.*

L'aide est bien rédigée ([https://aide.libreqda.org/](https://aide.libreqda.org/)) et intègre quelques extraits vidéos tutoriels. On peut obtenir des réponses en écrivant à l'adresse <libreqda@usherbrooke.ca>.  
En France, il n’existe pas véritablement de communauté dédiée, et les ressources spécifiques restent limitées (mais on peut toutefois s’appuyer sur les communautés francophones existantes).

## Collaboratif

*Il est possible de collaborer sur un même projet et de gérer les permissions accordées, mais sans fonctionnalités avancées.*

Le logiciel dans sa version en ligne est pensé pour collaborer à plusieurs sur un projet.  
Il est possible d'ajouter des utilisateurs à un projet en gérant les permissions accordées (Consulter, Encoder, Modifier les codes, Importer et supprimer des documents, etc.)
Les modifications sont appliquées en temps réel à l’ensemble de l’équipe (ce qui peut influer sur la lecture et l’interprétation des données), il n'y a pas de logique d'arbitrage entre les désaccords d'annotation.

<!-- TODO : confirmer si on est bien ok sur désaccords etc. -->

## IA

*Pas d'intégration de l'IA dans le logiciel.*

<!-- Faut il rajouter une note sur le fait que le logiciel a pour but de simplifier ce qu'ils dénoncent comme le côté bloat des caqdas propriétaires, y compris les trucs lexico, et que c'est donc très probablement pas dans leur feuille de route ? -->

## Prise en main

**Retour d'expérience (Léo Mignot) :**
<!-- évidemment on vire selon le ton qu'en veut et si on veut ou non garder des retours au final. Je le pose par écris pour stabiliser mon avis et pouvoir faire un retour aux collègue du labo. -->

***Hot-Take : L'anti usine à gaz***  

Le logiciel est simple mais pas simpliste, et l'on dispose ainsi d'un surligneur numérique qui permettra de réexplorer les codages réalisés à l'aide de l'explorateur de sélections ou encore d'explorer les arbres de codes en format visuel, etc. L'UI est agréable et la documentation fait bien le travail pour identifier les fonctionnalités qui ne sauteraient pas directement aux yeux.

La Ford T pouvait être choisie en noir ou en noir. libreQDA fait un choix comparable : il se concentre sur l’annotation qualitative de contenus textuels, sans chercher à multiplier les options d'analyse. On peut aimer, ou détester si l'on a besoin de ce type de fonctionnalités. Mais si votre but est d'analyser qualitativement des contenus textuels (entretiens, etc.) sans velléité lexicométrique ou de quantification, libreqda est une très bonne alternative facile à prendre en main.

> [!NOTE]
> Les développeurs se montrent à ce titre [critiques](https://www.usherbrooke.ca/flsh/actualites/nouvelles/details/54194) de la dimension « usine à gaz » de certains CAQDAS propriétaires, qui favoriseraient un "glissement de la recherche qualitative vers des méthodes quantitatives". La mise en avant de fonctionnalités « clés en main » inciterait à les appliquer, y compris là où il ne faudrait pas, parfois sans recul méthodologique.
<!-- This is an HTML comment cause markdown linter doesn't want blank line - I hate you -->
> [!CAUTION]
> N.B. : le test n'a toutefois pas été réalisé sur de gros corpus, et le passage des textes en format quasi brut peut causer des soucis d'affichage. Voir les [limites](https://aide.libreqda.org/limites/) soulevées par les développeurs.  
> N.B.2 : Au 18/09/2026, l'installation locale est encore peu/mal documentée en l'attente de mise à disposition des fichiers d'installation. Côté ligne de commande, certaines procédures d'installation (version dev notamment) méritent encore d'être clarifiées. Le logiciel est "jeune" et régulièrement mis à jour, on peut donc espérer que ce soit rapidement corrigé.

## TODO

Ouvrir le fichier brut si vous voulez voir les commentaires intégrés en balise `<!-- -->`  
Sans doute harmoniser graphie du logiciel.