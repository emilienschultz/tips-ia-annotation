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

Outils en place : 

- LabelStudio (docker)
- Doccano (docker)

Outils émergents : 

- Active Tigger

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