# Potato

Dernière modification de la fiche : 13/11/2026

Version testée : 2.14.0

Site web : [https://www.potatoannotator.com/fr](https://www.potatoannotator.com/fr)

Code : [https://github.com/davidjurgens/potato](https://github.com/davidjurgens/potato)

Citer le logiciel :

en français :
> @inproceedings{jurgens-etal-2026-potato,
>    title = "Potato 2.0: A Comprehensive Annotation Platform with {AI}-in-the-Loop Support",
>    author = "Jurgens, David  and
>      Chen, Michael  and
>      Iyer, Lina",
>    editor = "Durrett, Greg  and
>      Jian, Ping",
>    booktitle = "Proceedings of the 64th Annual Meeting of the Association for Computational Linguistics (Volume 3: System Demonstrations)",
>    month = jul,
>    year = "2026",
>    address = "San Diego, California, United States",
>    publisher = "Association for Computational Linguistics",
>    url = "https://aclanthology.org/2026.acl-demo.37/",
>    pages = "374--386",
>    ISBN = "979-8-89176-392-0",
>}



## Description générale

Potato est un logiciel open source pour de l'annotation sur une très large gamme de supports, du texte à la vidéo en passant par des formats plus exotiques, sur le principe d'un template flexible de configuration du panel d'annotation et des options d'annotation. Il couvre un nombre impressionnant d'usages, avec comme conséquence d'avoir une documentation assez pléthorique. Il a aussi la particularité d'avoir des connecteurs avec les pratiques agentiques : analyse de trajectoires, usage couplé à des harnais : "De zéro à l'annotation en quelques minutes. Annotation propulsée par l'IA pour chercheurs et équipes". L'outil semble suivre de très près les évolutions des solutions agentiques. Cependant, comme la configuration se fait via des JSON, les options ne sont pas directement disponibles et il est nécessaire de rentrer en détail dans le fonctionnement pour maîtriser ses particularités.

## Licence

Disponible sous licence GPL-3.0


## Installation

Potato est un package Python et peut être installé par pip ou cloné sur Github. Ensuite, Potato fonctionne comme une application tournant sur l'ordinateur et exposée dans le navigateur (architecture flask). Il est aussi doté d'une skill dédiée pour Claude/Codex afin d'automatiser l'usage.

Les usages spécifiques nécessitent d'installer de nouveaux packages (par exemple, pour faire du ML)


## Corpus

Potato manipule des formats très divers : images, textes (textes, pdf, word, etc.), vidéos, sons, signaux (EEG, ECG and sensor recordings), à la fois dans une perspective orientée machine learning et dans une perspective plus qualitatif (annotation libre, mémos...). Il y a aussi la possibilité de mettre en place des expérimentations.

Le type d'annotation est lui-aussi varié : catégories, span, texte libre, segmentation, différentes mesures configurables.

C'est une instance par corpus, et non pas du multiprojet.

## Interopérabilité

Le package semble fait pour la flexibilité. 

Par exemple, un module de capture de la [parole audio pour ajouter des commentaires pendant l'annotation](https://github.com/davidjurgens/potato/blob/master/docs/advanced/think_aloud.md).


## Communauté

Le logiciel a été présenté à différentes conférences d'apprentissage automatique

Il y a une grande gallerie d'exemple : https://www.potatoannotator.com/showcase

La documentation est pléthorique.

## Collaboratif

Le logiciel est pensé pour des campagnes d'annotation. La configuration peut permettre à des utilisateurs de s'enregistrer, avec différentes règles limitant le nombre et qui.

Il y a un panel administrateur permettant de suivre une campagne d'annotation, de gérer les utilisateurs, d'ajouter des tests d'attention, d'identifier les utilisateurs suscpicieux.



## IA

Le logiciel couvre tous les usages actuels liés à l'IA : il a des connecteurs pour permettre la pré-annotation par LLM (OpenAI, Anthropic, Ollama, vLLM, Gemini, HuggingFace, OpenRouter). Il est configurable pour faire de l'active learning. Et il permet d'entrainer et de fine-tuner des modèles soit en local avec les packages installés, soit avec des connecteurs (on the annotation server, on a GPU machine over ssh, on a SLURM cluster, or on a machine that polls for jobs). Un panel dédié sert à ce travail d'entrainement (admin/training ). Le paramétrage se fait avec des dictionnaires JSON


## Prise en main

