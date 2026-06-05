# Label Studio

Dernière modification de la fiche : 4/06/2026

Version testée : 1.23.0

Site web : [https://labelstud.io/](https://labelstud.io/)

Code : [https://github.com/HumanSignal/label-studio/](https://github.com/HumanSignal/label-studio/)

## Description générale

*À quoi sert le logiciel ? : les principales fonctionnalité du logiciel, sa philosophie transversale*

Label Studio est un logiciel d'annotation multimodale développé par la société HumanSignal. Il est pensé pour l'annotation de grands volumes de données, notamment dans une perspective d'entraînement de modèles.  
Il couvre un large type de tâches d'annotation : texte (classification, NER), images (détection d'objets, segmentation, classification), audio (interface de transcription, diarisation des locuteurs), séries temporelles, vidéo, PDF, etc.  
Il fonctionne sur le principe client-serveur (un serveur héberge l'instance et les annotateurs interagissent via leur navigateur web) et permet une gestion multi-utilisateurs pour travailler à plusieurs sur un projet.  
Il est développé par une société commerciale et son développement et sa maintenance bénéficient d'un soutien actif.

## Licence

*Conditions légale d'adoption : licence du logiciel \& prix*

Logiciel libre sous licence Apache-2.0.  
Il existe également deux versions payantes (Starter Cloud et Enterprise) qui proposent des services complémentaires et des fonctionnalités de gestion d'équipe.

NB : Certaines options (format parquet, etc.) ne sont disponible que dans la version entreprise, mais la "community edition" – libre et gratuite – est pleinement fonctionnelle pour un usage en recherche.

## Installation

*Conditions matérielles d'usage : sous forme de service (oui/non et sur quel serveur en terme de sécurité ; limite en terme de navigateur / adaptabilité smartphone) ; logiciel à installer (sur quel OS ? Windows, Mac, Linux) ; Niveau de complexité, notamment ligne de commande ?*

Label Studio peut être installé localement ou déployé sur un serveur distant.

L'installation est possible via pip / brew / git / docker sous des machines Linux, Mac ou Windows  :
- L'installation via pip suppose de savoir ouvrir un terminal et de passer par une ligne de commande, mais elle est facile.
- Une option Homebrew est disponible pour macOS.
- Docker pourra simplifier le déploiement d'une instance collective en ligne mais requiert une familiarité avec l'outil et des compétences en administration système.

Le niveau de complexité est donc modéré : raisonnable pour un profil ayant déjà manipulé Python et un terminal, un peu plus ardu pour les non-techniciens (pas d'installation "automatique" de l'application depuis un .dmg ou .exe). La mise en production sur un serveur partagé pour une équipe nécessite des compétences en administration système. L'usage des options d'IA nécessite également une installation plus avancée et la maîtrise de docker.  

## Corpus

*Les corpus possibles traitables : Texte, Audio, Video, Images, PDF, Multimodal, Réseaux sociaux, etc.*

Label Studio permet des données textuelles, des images, de l'audio, de la vidéo, des pdf, etc. Les formats d'entrée sont variés :

- Images (bmp, gif, jpg, jpeg, png, svg, webp)
- Audio (wav, mp3, flac, m4a, ogg)
- Video (mp4, webm)
- HTML / HyperText (html, htm, xml)
- Text (txt)
- Structured data (csv, tsv, json)
- PDF

## Interopérabilité

*Degré d'interopérabilité : formats d'échange des données, import et export*

Les formats d'import (voir ci-dessus) sont très variés.  
Les formats d'export sont des standards connus (json, csv, tsv), ou plus spécifiques selon le type de données (CONLL2003, COCO, YOLO, Brush).

## Communauté

*Support communautaire à l'usage francophone : où trouver de l'aide / diffusé dans les réseaux métiers / tutoriaux disponibles*

- La documentation officielle : https://labelstud.io/guide/
- Des tutoriels : https://labelstud.io/tutorials/

Le projet a 27k étoiles sur Github et, étant développé par une entreprise, bénéficie de la force de frappe de commerciale pour sa [documentation](https://labelstud.io/guide/), la création de [tutoriels]((https://labelstud.io/tutorials/)), un groupe d'échange sur [Slack](https://slack.labelstud.io/), etc.

La majorité des supports et de la communauté est anglophone.  
L'adoption par la communauté universitaire francophone semble plus en retrait.

## Collaboratif

Le logiciel est largement pensé vers les tâches d'annotation multi-utilisateurs et il est possible de collaborer à plusieurs sur un projet.

Dans le cas de l'usage collaboratif en ligne : il n'existe pas d'instance publique mutualisée gratuite compatible avec des données de recherche sensibles. Une instance est néanmoins disponible dans la stack Onyxia du [datalab sspcloud de l'INSEE](https://datalab.sspcloud.fr), mais la plateforme est limitée aux "données publiques et données usuelles (données de travail sans sensibilité particulière)".  
Il reste possible d'installer soi même une instance en ligne si l'on a accès à des serveurs et aux compétences nécessaires (ou de souscrire à l'offre cloud payante de HumanSignal – mais il faudra dans ce cas vérifier les conditions concernant les données sensibles).

## IA

*Place de l'IA dans le logiciel : présent ou pas ; optionnel (et désactivable) ou au coeur de l'outil, possibilité de choisir les modèles utilisés, outil augmenté par l'IA ou outil pensé pour l'IA*

L'utilisation de l'IA n'est pas obligatoire et l'on peut rester sur une volonté de pure d'annotation manuelle.
Mais plusieurs templates de labellisation montrent une orientation forte vers les workflows RLHF, les pipelines ML/IA, y compris l'évaluation de LLMs et leur fine-tuning, RAG, l'évaluation de chatbot, etc.
L'utilisation des possibilités d'IA suppose de connecter des modèles depuis une installation d'un backend ML avec Docker.

## Prise en main

**Retour d'expérience (Léo Mignot) :**

***Hot-Take : Fait tout. Et trop.***  
Le logiciel est beau, l'UI est bien pensée et les vidéos d'explication ainsi que la doc bienvenues. La création de projets et de schémas d'annotation est facilitée par l'interface d'import de données et l'existence de templates de labellisation (qu'il est possible de modifier, ou de créer de zéro). Le tout est très "pro". Néanmoins, l'expérience utilisateur pour le débutant n'est pas évidente. Il n'est pas facile de s'y retrouver dans la myriade d'options : il y a énormément de possibilités, sans que l'on soit super guidé sur ce qui marche dans nos cas d'usages ou non, ni pourquoi. Les configurations et le workflow ne tombent pas forcément sous le sens pour les néophytes. Il y a un côté "je peux tout faire, mais comment ?".

Si l'installation de base est facile pour qui sait ouvrir un terminal et connaît python, ce n'est pas la même limonade s'il est question de connecter soi-même le tout a des modèles qu'il faut faire tourner depuis leur label-studio-ml-backend avec docker

N.B. : La doc n'est pas toujours très cohérente sur la version de python minimale nécessaire : selon les endroits sont mentionnées la 3.6 ; 3.8 ; 3.10. L'installation via pip a ici marché sans problème avec python 3.10.

## TODO

TODO : affiner partie IA après tests
TODO : vérifier les cas d'usages multi-utilisateurs, résolution de conflits, etc.
TODO : afiner si besoin les trucs que dans l'édition payante ? (mais désormais mentionné dans la fiche)
TODO : aviser des formats spécifiques aux données que je maîtrise peu  

TODO : préciser le degré d'adoption communautaire (hors commercial) ? mais c'est désormais mentionné
TODO : si besoin sur les formats spécifiques, voir dessous
ou ici : https://labelstud.io/guide/export

Liste des formats mentionnés :
CONLL2003
sequence labeling
text tagging
named entity recognition
Popular format used for the CoNLL-2003 named entity recognition challenge.

COCO
image segmentation
object detection
keypoints
Popular machine learning format used by the COCO dataset for object detection and image segmentation tasks with polygons and rectangles.
COCO with Images
image segmentation
object detection
keypoints
COCO format with images downloaded.
Pascal VOC XML
image segmentation
object detection
Popular XML format used for object detection and polygon image segmentation tasks.

YOLO
image segmentation
object detection
keypoints
Popular TXT format is created for each image file. Each txt file contains annotations for the corresponding image file, that is object class, object coordinates, height & width.
YOLO with Images
image segmentation
object detection
keypoints
YOLO format with images downloaded.
YOLOv8 OBB
image segmentation
object detection
Popular TXT format is created for each image file. Each txt file contains annotations for the corresponding image file. The YOLO OBB format designates bounding boxes by their four corner points with coordinates normalized between 0 and 1, so it is possible to export rotated objects.
YOLOv8 OBB with Images
image segmentation
object detection
YOLOv8 OBB format with images downloaded.

Brush labels to NumPy
image segmentation
Export your brush labels as NumPy 2d arrays. Each label outputs as one image.
Brush labels to PNG
image segmentation
Export your brush labels as PNG images. Each label outputs as one image.
ASR Manifest
speech recognition
Export audio transcription labels for automatic speech recognition as the JSON manifest format expected by NVIDIA NeMo models.
Brush labels to COCO
image segmentation
brush annotations
Export your brush labels as COCO format for segmentation tasks. Converts RLE encoded masks to COCO polygons.