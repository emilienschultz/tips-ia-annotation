# Profils de pratiques

## Objectif

Définir un nombre limité de cas rencontré d'usagers de logiciel d'annotation pour associer des tâches avec un jeu de données et permettre d'évaluer si les logiciel permettent de répondre à la tâche.

## Propositions

### Une sociologue veut annoter un ensemble de longs textes (ex: entretiens) au niveau de passage de texte en construisant au fur et à mesure sa grille de codage.

*Passage qui précise les besoins* Cette tâche d'annotation concerne des documents longs dans lesquels certains passages doivent être annotés avec une grille de codage qui peut évoluer dans le temps. Dans ce cas, la capacité d'avoir une vue générale du document, de pouvoir ajouter et enlever des codages, et d'avoir des statistiques d'annotation pour suivre la distributions des annotations par documents ou au contraire d'avoir les extraits par catégorie sont important. Le souhait est d'avoir une interconnexion facilité avec la bureautique et des formats classiques docw et xlsx.

*Passage qui précise les logiciels recommandés* Les solutions libres les plus adaptées qui couvrent ces activités sont associés au CAQDAS Computer-Assisted Qualitative Data Analysis Software sont le logiciel standalone [QualCoder](./logiciels/qualcoder.md) pour un travail sur l'ordinateur et la solution collaborative [LibreQDA](./logiciels/libreqda.md) (construit sur Taguette). Le logiciel QualCoder est assez facile à prendre en main en raison d'une communauté active, son ergonomie pouvant cependant dater un peu. Il couvre l'ensemble des besoins de l'annotation et permet facilement d'extraire les résultats pour des analyses ultérieures.

*Passage qui décrit les usages IA* Les usages IA dans ce cas peuvent prendre la forme de suggestion sur la base des annotations déjà faites. A COMPLETER

*Passage qui commente les autres usages possibles* D'autres logiciels plus éloignés peuvent être utilisés : Inception offre toutes les possibilités d'annotation, mais les options supplémentaires le rendent assez lourd pour cet usage ; Doccano ou LabelStudio ne facilite pas le travail de vue générale.

*Logiciels propriétaires correspondants : Nvivo, MaxQDA, AtlasTi.*


### Un politiste veut classifier un grand corpus de textes (ex: presse) avec des labels prédéfinis.

*Passage qui précise les besoins* Généralement les données sont sous des formats de tableaux (excel, csv), produit par un découpage et un nettoyage antérieur (la transformation n'est généralement pas prise en compte dans les logiciels). L'enjeu est que l'annotation prend du temps, qu'il est important de pouvoir garder une trace des étapes, et potentiellement de collaborer à cette annotation (soit pour aller plus vite, soit pour contrôler). Que ce soit les situations où toute l'annotation est humaine, ou les situation où l'objectif est d'automatiser l'annotation par prédiction, il y a un moment de lecture important des données. Dans le cas où il faut prédire, la question se pose de quelles sont les technologies de modèles utilisés, comment se fait l'évaluation de la qualité des prédictions, et comment s'organise le pipeline de travail. 

*Passage qui précise les logiciels recommandés* Pour annoter des textes, le logiciel permettant le plus de souplesse est [LabelStudio](./logiciels/label-studio.md) notamment en raison de sa possibilité d'avoir des template. Néanmoins, comme il a beaucoup d'option, la prise en main peut être assez complexe, et il n'est pas spécifiquement pensé pour les besoins des sciences sociales. Le logiciel [ActiveTigger](./logiciels/activetigger.md) a justement pour but d'organiser les différentes étapes de l'annotation dans un parcours adapté aux sciences sociales, notamment pour accélérer la classification de textes avec les méthodes d'active learning. Son ergonomie est pensée pour une prise en main facile. Le logiciel [Doccano](./logiciels/doccano.md) est aussi une solution adaptée pour des petits projets qui ont besoin d'une interface simple et épurée pour de l'annotation collaborative.

*Passage qui décrit les usages IA* LabelStudio et Doccano repose sur des solutions IA qui se connectent (recommandations, etc.). ActiveTigger intègre directement dans le pipeline un ensemble de méthodes (plongements des textes, distances sémantiques, entrainement de modèles BERT, appels génératifs).


### Une linguiste doit annoter des relations entre des entités du texte dans un corpus de textes de taille moyenne (centaine d'entretiens courts retranscrits) en ayant accès à un étiquetage morphosyntaxique

Outils en place : 

- TXM
- Inception

Outils émergents : 

- ??

### Une économiste veut extraire rapidement des informations contenues dans des documents dans un corpus de taille moyenne (ex : offres d'emploi)

Outils en place : 

- LabelStudio (docker)

Outils émergents : 

- wrapper Python (+ API)
- Argilla (+API)

### Un chercheur en science de l'éducation s'intéresse à une série de vidéos d'interaction en milieu naturel d'individus et doit annoter les échanges d'intérêt (verbaux et non verbaux)

Outils en place :

- Elan/avaa toolkit
- QualCoder

Outils émergents : 

- ?

### Divers

*Profils pour le futur*

- Un historien en humanité numérique (logiciel comme TACTEO)

## Décliner les personas en critères

Chaque profil pose des contraintes à l'usage d'un logiciel.

Ces contraintes seront développées pour chaque profil lors de la réflexion sur l'adéquation avec un logiciel, pour former une grille de tâches/demandes.