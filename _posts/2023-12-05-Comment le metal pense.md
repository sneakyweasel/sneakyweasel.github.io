---
layout: post
title:  "Comment le métal pense?"
date:   2023-10-24 16:13:05 +0200
categories: AI
---

## Comment le métal pense?

### Introduction

- A la façon de la "Somme contre les gentils" de St Thomas, nous allons partir de fondements communs rationnels pour construire un automate logique.
- Je vais tenter de démystifier le fonctionnement des LLMs (Large Language Models) en vous faisant revivre l'aventure intellectuelle qui va de la matière à l'IA.
- Tout d'abord nous fabriquerons un ordinateur. (5-10 min)
- Ensuite nous verrons le fonctionnement de réseaux de neurones. (5-10 min)
- Enfin nous verrons un exemple pratique d'utilisation d'un LLM. (5-10 min)

### I - Automate logique

#### Logique

La logique est une science qui étudie les principes du raisonnement valide. Elle est fondamentale pour la philosophie, les mathématiques et l'informatique. Elle est fondée sur le principe de non-contradiction.
La porte logique NAND est une porte universelle qui permet de construire toutes les autres portes logiques par combinaison.

- Aristote - Organon: <https://fr.wikipedia.org/wiki/Aristote#Logique>
- Calcul des propositions: <https://fr.wikipedia.org/wiki/Calcul_des_propositions>
- Algèbre de Boole: <https://fr.wikipedia.org/wiki/Alg%C3%A8bre_de_Boole_(logique)>
- Porte logique: <https://fr.wikipedia.org/wiki/Porte_logique>
- Porte universelle (ET-NON): <https://fr.wikipedia.org/wiki/Fonction_NON-ET>
- NAND: <https://www.nandgame.com/>

#### De la porte universelle au processeur

En informatique théorique, une machine de Turing est un modèle abstrait du fonctionnement des appareils mécaniques de calcul, tel un ordinateur.

|2^x|2^7|2^6|2^5|2^4|2^3|2^2|2^1|2^0|
|---|---|---|---|---|---|---|---|---|
|dec|128|64|32|16|8|4|2|1|

|Nombre decimal| nombre binaire|
|---|---|
|0|00000000|
|1|00000001|
|2|00000010|
|3|00000011|

- Machine de Turing: <https://fr.wikipedia.org/wiki/Machine_de_Turing>
- Turing Complete: <https://www.youtube.com/watch?v=-YY73ejihZo>
- Nand to Tetris: <https://www.nand2tetris.org/>

> NANDGAME: <https://www.nandgame.com/>
> Minecraft CPU: <https://youtu.be/TxatLwlj0lU?si=aYUfTmiCIc7kXt56&t=34>

#### Matérialiser l'automate

La découverte des jonctions P-N permet de construire de minuscules transistors en silicium. Ces transistors peuvent être assemblés en circuits intégrés qui permettent de construire un ordinateur.

- Silicium: <https://fr.wikipedia.org/wiki/Silicium>
- Jonction PNP: <https://fr.wikipedia.org/wiki/Jonction_p-n>
- CMOS: <https://en.wikipedia.org/wiki/CMOS#Example:_NAND_gate_in_physical_layout>
- Semi-conducteur: <https://fr.wikipedia.org/wiki/Semi-conducteur>
- Transistor: <https://fr.wikipedia.org/wiki/Transistor>
- Circuit intégré: <https://fr.wikipedia.org/wiki/Circuit_int%C3%A9gr%C3%A9>
- Ordinateur 8-bits: <https://eater.net/8bit>

#### Course à la puissance

Au bout d'un certains temps, la miniaturisation des transistors et la vitesse de calcul atteignent des limites physiques. Il faut donc trouver d'autres moyens d'augmenter la puissance de calcul: vu qu'on ne peut plus augmenter la vitesse des processeurs on les duplique et on réparti la charge de travail sur les différents coeurs.

- Loi de Moore: <https://fr.wikipedia.org/wiki/Loi_de_Moore>
- Effet tunnel: <https://fr.wikipedia.org/wiki/Effet_tunnel>
- Calcul parallèle: <https://fr.wikipedia.org/wiki/Parall%C3%A9lisme_(informatique)>
- GPU: <https://fr.wikipedia.org/wiki/Processeur_graphique>
- Nvidia: <https://fr.wikipedia.org/wiki/Nvidia>
- Langage de programmation GPU CUDA: <https://en.wikipedia.org/wiki/CUDA>

#### Programmation et niveaux d'abstraction

Nous avons désormais une machine capable d'exécuter d'impressionnantes quantités d'instructions de calcul en un temps record. Nous avons les moyens de la programmer à des niveaux d'abstraction élévés en utilisant des langages de programmation de haut niveau et des librairies de fonctions complexes.
Nous controlons un nouveau type de rapport au langage: l'exécution en plus de la lecture et de l'écriture.

- Langage de programmation: <https://fr.wikipedia.org/wiki/Langage_de_programmation>
- Assembleur: <https://fr.wikipedia.org/wiki/Assembleur>
- Calcul lambda: <https://fr.wikipedia.org/wiki/Lambda-calcul>
- Rust: <https://fr.wikipedia.org/wiki/Rust_(langage)>
- Langage de haut niveau: <https://fr.wikipedia.org/wiki/Langage_de_haut_niveau>
- Python: <https://fr.wikipedia.org/wiki/Python_(langage)>

### II - Appréhender un monde incertain

#### Réseaux de neurones et vision machine

Notre machine est déterministe, rapide et précise mais elle n'aime pas l'incertitude, l'ambiguité et l'approximation.
On explore alors comment le cerveau humain arrive à appréhender le monde incertain qui nous entoure avec ses réseaux de neurones.
On s'inspire de la nature pour créer des réseaux de neurones artificiels.
(La vision humaine serait de 576 million pixels, et le cerveau humain contient 86 milliards. Le traitement quasi-instantanée de l'information visuelle est fascinant.)

- ANN: <https://fr.wikipedia.org/wiki/R%C3%A9seau_de_neurones_artificiels>
- Perceptron: <https://fr.wikipedia.org/wiki/Perceptron><https://distill.pub/2017/aia/>
- Algèbre linéaire: <https://fr.wikipedia.org/wiki/Alg%C3%A8bre_lin%C3%A9aire>
- Tenseur: <https://fr.wikipedia.org/wiki/Tenseur>
- Framework ML PyTorch: <https://pytorch.org/>
- Visualisations DL: <https://distill.pub/>
- 3B1B Neural network: <https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi>
- Cours DL: <https://www.coursera.org/learn/neural-networks-deep-learning/home/welcome>

> Recap perceptron: <https://youtu.be/IHZwWFHWa-w?si=LE5qWstbH01bqKZO&t=29>
> 3B1B: <https://www.3blue1brown.com/lessons/neural-networks>

#### LLMS: Large Language Models

Une des théories de l'apparition des facultés humaines est le détournement d'une partie de notre puissance de calcul visuelle vers la méta-cognition et les concepts abstraits.
Les LLMs sont des réseaux de neurones qui ont été entrainés sur de très grands corpus de données textuelles. Ils sont capables de générer du texte à partir d'un prompt.

- Deep Learning: <https://fr.wikipedia.org/wiki/Apprentissage_profond>
- Transformeur: <https://fr.wikipedia.org/wiki/Transformeur>
- Attention is all you need: <https://arxiv.org/abs/1706.03762>
- LLMs: <https://fr.wikipedia.org/wiki/Grand_mod%C3%A8le_de_langage>
- Cours LLM: <https://www.coursera.org/learn/generative-ai-with-llms/home/week/1>

> Viz NanoLLM: <https://bbycroft.net/llm>

### III - Utilisation d'un LLM pour un chatbot

Voici un exemple d'utilisation de GPT-4 pour créer un chatbot catholique qui enrichi du "Cathéchisme de l'Eglise Catholique" réponds aux questions posées par les utilisateurs.

- Pré-train: <https://fr.wikipedia.org/wiki/Pr%C3%A9-entra%C3%AEnement>
- Tokenisation: <https://fr.wikipedia.org/wiki/Analyse_lexicale>
- Byte Pair Encoding: <https://en.wikipedia.org/wiki/Byte_pair_encoding>
- Fine-tuning: <https://en.wikipedia.org/wiki/Fine-tuning_(deep_learning)>
- NanoGPT: <https://github.com/karpathy/nanoGPT>
- RLHF: <https://en.wikipedia.org/wiki/Reinforcement_learning_from_human_feedback>
- PPO: <https://en.wikipedia.org/wiki/Proximal_Policy_Optimization>
- RAG: <https://arxiv.org/abs/2104.05544>
- Pré-prompt: <https://en.wikipedia.org/wiki/Prompt_engineering>

> Biais religieux: <https://arxiv.org/pdf/2106.13219.pdf>
