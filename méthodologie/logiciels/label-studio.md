# Label Studio

Dernière modification de la fiche : 4/06/2026

Version testée : 1.23.0

Site web : [https://labelstud.io/](https://labelstud.io/)

Code : [https://github.com/HumanSignal/label-studio/](https://github.com/HumanSignal/label-studio/)

## Description générale

*À quoi sert le logiciel ? : les principales fonctionnalité du logiciel, sa philosophie transversale*

Label Studio est un logiciel d'annotation multimodale développé par la société HumanSignal.  
Il couvre un large type de tâches d'annotation : texte (classification, NER), images (détection d'objets, segmentation, classification), audio (interface de transcription, diarisation des locuteurs), séries temporelles, vidéo, PDF, etc.  
Il fonctionne sur le principe client-serveur (un serveur héberge l'instance et les annotateurs interagissent via leur navigateur web) et permet une gestion multi-utilisateurs pour travailler à plusieurs sur un projet.  
Étant développé par une société commerciale, son développement et sa maintenance bénéficient d'un soutien actif.

## Licence

*Conditions légale d'adoption : licence du logiciel \& prix*

Logiciel libre sous licence Apache-2.0.  
Il existe également deux versions payantes (Starter Cloud et Enterprise) qui proposent des services complémentaires et des fonctionnalités de gestion d'équipe, mais la "community edition" libre et gratuite est pleinement fonctionnelle pour un usage en recherche.

## Installation

*Conditions matérielles d'usage : sous forme de service (oui/non et sur quel serveur en terme de sécurité ; limite en terme de navigateur / adaptabilité smartphone) ; logiciel à installer (sur quel OS ? Windows, Mac, Linux) ; Niveau de complexité, notamment ligne de commande ?*

Label Studio peut être installé localement ou déployé sur un serveur distant. Dans le cas de l'usage en ligne : il n'existe pas d'instance publique mutualisée gratuite et il faut soit l'installer soi-même, soit souscrire à l'offre cloud payante de HumanSignal (Starter Cloud ou Enterprise).

L'installation est possible via pip / brew / git / docker sous des machines Linux, Mac ou Windows  :
- L'installation via pip suppose de savoir ouvrir un terminal et passer par une ligne de commande, mais elle est très facile.
- Une option Homebrew est disponible pour macOS.
- Docker pourra simplifier le déploiement d'une instance collective en ligne mais requiert une familiarité avec l'outil et des compétences en administration système.
- Possible de cloner directement le repo (mais autant passer par les autres options sauf cas spécifiques)

Le niveau de complexité est donc modéré : très raisonnable pour un profil ayant déjà manipulé Python et un terminal, un peu plus ardu pour les non-techniciens (pas d'installation "automatique" de l'application depuis un .dmg ou .exe). La mise en production sur un serveur partagé pour une équipe nécessite des compétences en administration système.  
**Update :** c'est pas la même limonade s'il est question de connecter soi-même le truc a des modèles qu'il faut faire tourner sur depuis leur label-studio-ml-backend avec docker

N.B. : La doc n'est pas toujours très cohérente sur la version de python minimale nécessaire : selon les endroits sont mentionnées la 3.6 ; 3.8 ; 3.10. L'installation via pip a ici marché sans problème avec python 3.10.

## Corpus

*Les corpus possibles traitables : Texte, Audio, Video, Images, PDF, Multimodal, Réseaux sociaux, etc.*

Label Studio permet d'annoter un peu tout (et sans doute un peu trop).

- Images (bmp, gif, jpg, jpeg, png, svg, webp)
- Audio (wav, mp3, flac, m4a, ogg)
- Video (mp4, webm)
- HTML / HyperText (html, htm, xml)
- Text (txt)
- Structured data (csv, tsv, json)
- PDF

TODO : des trucs que dans l'édition payante ?
```
    We recommend Cloud Storage over direct uploads due to upload limitations.
    For PDFs, use multi-image labeling. JSONL or Parquet (Enterprise only) files require cloud storage.
    Check the documentation to import preannotated data.
```

## Interopérabilité

*Degré d'interopérabilité : formats d'échange des données, import et export*

Les formats d'imports (voir ci-dessus ou TODO aviser si descend ici) sont très variés.  
Les formats d'export sont des standards connus (json, csv, tsv), ou ?moins connus? / plus spécifiques selon le type de données (CONLL2003, COCO, YOLO, Brush).

La création de projets et de schémas d'annotation est facilité par l'interface d'import de données et l'existence de templates de labellisation, mais ce n'est pas évident de s'y retrouver (énormément de possibilités sans que l'on soit super guidé sur ce qui marche ou non et pourquoi).  
Ex : j'ai un projet qui une fois configuré ne m'affiche que le titre de la colone, un autre qui marche nickel, visiblement parce que le csv lui va pas mais sans aucun indice de ce qui irait pas (ni que ça va pas).

TODO : aviser des formats spécifiques aux données que je maîtrise peu  
TODO : il nous faudrait une catégorie prise en main pour préciser ça peut-être

Liste des formats à virer après discussion :
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

## Communauté

*Support communautaire à l'usage francophone : où trouver de l'aide / diffusé dans les réseaux métiers / tutoriaux disponibles*

- La documentation officielle : https://labelstud.io/guide/
- Des tutoriels : https://labelstud.io/tutorials/

Le projet a 27k étoiles sur Github et, étant développé par une entreprise, bénéficie de la force de frappe de commerciale pour sa [documentation](https://labelstud.io/guide/), la création de [tutoriels]((https://labelstud.io/tutorials/)), un groupe d'échange sur [Slack](https://slack.labelstud.io/), etc.

La majorité des supports et de la communauté est anglophone.

TODO : quid de la communauté francophone ?  
TODO : préciser le degré d'adoption communautaire (hors commercial ?)

## Collaboratif

**aviser si précise ici ou dans installation (ou les deux)** Dans le cas de l'usage en ligne : il n'existe pas d'instance publique mutualisée gratuite et il faut soit l'installer soi-même, soit souscrire à l'offre cloud payante de HumanSignal (Starter Cloud ou Enterprise).

TODO : vérifier les cas d'usages multiutilisateurs, résolution de conflits, etc.

## IA

*Place de l'IA dans le logiciel : présent ou pas ; optionnel (et désactivable) ou au coeur de l'outil, possibilité de choisir les modèles utilisés, outil augmenté par l'IA ou outil pensé pour l'IA*

L'utilisation de l'IA n'est pas obligatoire et l'on peut rester sur une volonté de pure d'annotation manuelle.
Mais plusieurs templates de labellisation montrent une orientation forte vers les workflows RLHF, les pipelines ML/IA, y compris l'évaluation de LLMs et leur fine-tuning, RAG, l'évaluation de chatbot, etc.

TODO : affiner partie IA après tests