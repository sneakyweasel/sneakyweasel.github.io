---
layout: post
title:  "Du silicone au langage: comment le métal pense?"
date:   2023-10-24 16:13:05 +0200
categories: AI
---

- A la façon de la "Somme contre les gentils" de St Thomas, nous allons partir de fondements communs rationnels pour construire un automate logique "pensant".
- Je vais tenter de démystifier le fonctionnement des LLMs (Large Language Models) en vous faisant revivre l'aventure intellectuelle qui va de la matière à l'IA.
  - Tout d'abord nous fabriquerons un ordinateur.
  - Ensuite nous verrons le fonctionnement d'un réseau de neurones artificiel.
  - Enfin nous le fonctionnement d'un LLM.

## I - Automate de calcul

### Logique fondamentale

La logique est une science qui étudie les principes du raisonnement valide. Elle est fondamentale pour la philosophie, les mathématiques et l'informatique.
Elle est fondée sur le principe de non-contradiction.
La porte logique NAND est une porte universelle qui permet de construire toutes les autres portes logiques par combinaison.

- Aristote - Organon: <https://fr.wikipedia.org/wiki/Aristote#Logique>
- Calcul des propositions: <https://fr.wikipedia.org/wiki/Calcul_des_propositions>
- Algèbre de Boole: <https://fr.wikipedia.org/wiki/Alg%C3%A8bre_de_Boole_(logique)>
- Porte logique: <https://fr.wikipedia.org/wiki/Porte_logique>
- Porte universelle (ET-NON): <https://fr.wikipedia.org/wiki/Fonction_NON-ET>

### Imaginer l'automate

En informatique théorique, une machine de Turing est un modèle abstrait du fonctionnement des appareils mécaniques de calcul, tel un ordinateur.

- Machine de Turing: <https://fr.wikipedia.org/wiki/Machine_de_Turing>
- Turing Complete: <https://www.youtube.com/watch?v=-YY73ejihZo>
- Nand to Tetris: <https://www.nand2tetris.org/>

> NANDGAME: <https://www.nandgame.com/>

### Construire l'automate

La découverte des jonctions P-N permet de construire de minuscules transistors en silicium. Ces transistors peuvent être assemblés en circuits intégrés qui permettent de construire un ordinateur.

- Silicium: <https://fr.wikipedia.org/wiki/Silicium>
- Jonction P-N (Pmos, Nmos): <https://fr.wikipedia.org/wiki/Jonction_p-n>
- CMOS: <https://en.wikipedia.org/wiki/CMOS#Example:_NAND_gate_in_physical_layout>
- Semi-conducteur: <https://fr.wikipedia.org/wiki/Semi-conducteur>
- Transistor: <https://fr.wikipedia.org/wiki/Transistor>
- Circuit intégré: <https://fr.wikipedia.org/wiki/Circuit_int%C3%A9gr%C3%A9>
- Ordinateur 8-bits: <https://eater.net/8bit>

> Minecraft CPU: <https://youtu.be/TxatLwlj0lU?si=aYUfTmiCIc7kXt56&t=34>

### Controler l'automate

Nous devons maintenant controler notre automate et lui faire faire des calculs. Nous créons des langages avec des niveaux d'abstraction de plus en plus élevés et de plus en plus élégants.
Nous controlons un nouveau type de rapport au langage: l'exécution en plus de la lecture et de l'écriture.

- Langage de programmation: <https://fr.wikipedia.org/wiki/Langage_de_programmation>
- Assembleur: <https://fr.wikipedia.org/wiki/Assembleur>
- Calcul lambda: <https://fr.wikipedia.org/wiki/Lambda-calcul>
- Rust: <https://fr.wikipedia.org/wiki/Rust_(langage)>
- Langage de haut niveau: <https://fr.wikipedia.org/wiki/Langage_de_haut_niveau>
- Python: <https://fr.wikipedia.org/wiki/Python_(langage)>
- NANDGAME (partie logiciel): <https://www.nandgame.com/>

### Accélerer l'automate

Au bout d'un certains temps, la miniaturisation des transistors et la fréquence de calcul atteignent des limites physiques. Il faut donc trouver d'autres moyens d'augmenter la puissance de calcul: on duplique et on parallèlise en répartissant la charge de travail sur les différents coeurs.

- Loi de Moore: <https://fr.wikipedia.org/wiki/Loi_de_Moore>
- Effet tunnel: <https://fr.wikipedia.org/wiki/Effet_tunnel>
- Calcul parallèle: <https://fr.wikipedia.org/wiki/Parall%C3%A9lisme_(informatique)>
- GPU: <https://fr.wikipedia.org/wiki/Processeur_graphique>
- Nvidia: <https://fr.wikipedia.org/wiki/Nvidia>
- Langage de programmation GPU CUDA: <https://en.wikipedia.org/wiki/CUDA>

## II - Appréhender un monde incertain

### Réseaux de neurones et vision machine (ANNs)

Notre machine est déterministe, rapide et précise mais elle n'aime pas l'incertitude, l'ambiguité et l'approximation.
On explore alors comment le cerveau humain arrive à appréhender le monde incertain qui nous entoure avec ses réseaux de neurones.
On s'inspire de la nature pour créer des réseaux de neurones artificiels.
(La vision humaine serait de 576 million pixels, et le cerveau humain contient 86 milliards. Le traitement quasi-instantanée de l'information visuelle est fascinant.)

- ANN: <https://fr.wikipedia.org/wiki/R%C3%A9seau_de_neurones_artificiels>
- Perceptron: <https://fr.wikipedia.org/wiki/Perceptron>
- Algèbre linéaire: <https://fr.wikipedia.org/wiki/Alg%C3%A8bre_lin%C3%A9aire>
- Tenseur: <https://fr.wikipedia.org/wiki/Tenseur>
- Framework Machine Learning PyTorch: <https://pytorch.org/>
- Visualisations Deep Learning: <https://distill.pub/>
- Séries vidéos 3B1B sur les ANNs: <https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi>
- Cours 3B1B: <https://www.3blue1brown.com/lessons/neural-networks>
- Spécialisation Deep Learning Coursera: <https://www.coursera.org/learn/neural-networks-deep-learning/home/welcome>
- Backprop: <https://youtu.be/Ilg3gGewQ5U?si=4FssMbXM6CRK5rmQ&t=261>

> Recap perceptron 3B1B: <https://youtu.be/IHZwWFHWa-w?si=LE5qWstbH01bqKZO&t=29>

### Large Language Models (LLMs)

Une des théories de l'apparition des facultés humaines est le détournement d'une partie de notre puissance de calcul visuelle vers la méta-cognition et les concepts abstraits.
Les LLMs sont des réseaux de neurones qui ont été entrainés sur de très grands corpus de données textuelles. Ils sont capables de générer du texte à partir d'un prompt.

- Deep Learning: <https://fr.wikipedia.org/wiki/Apprentissage_profond>
- Transformeur: <https://fr.wikipedia.org/wiki/Transformeur>
- Attention is all you need: <https://arxiv.org/abs/1706.03762>
- NanoGPT: <https://github.com/karpathy/nanoGPT>
- LLMs: <https://fr.wikipedia.org/wiki/Grand_mod%C3%A8le_de_langage>
- Cours LLM: <https://www.coursera.org/learn/generative-ai-with-llms/home/week/1>

> Viz NanoLLM: <https://bbycroft.net/llm>

Voici un exemple d'utilisation de GPT-4 pour créer un chatbot catholique qui enrichi du "Cathéchisme de l'Eglise Catholique" réponds aux questions posées par les utilisateurs.

### Corpus de pré-training

Donner au modèle un corpus de texte suffisamment grand et varié pour qu'il puisse apprendre la structure du langage.
Il faut éviter les données redondantes, les biais, nettoyer les balises, etc.

- Common Crawl Primary training corpus in every LLM. 82% of raw tokens used to train GPT-3.
- Common Crawl (98.38 TiB): <https://commoncrawl.org/>
- The Pile (825 GiB): <https://pile.eleuther.ai/>
- Wikipedia dumps: <https://dumps.wikimedia.org/>
- OSCAR: <https://oscar-project.github.io/documentation/versions/oscar-2301/>

### Corpus de domaine

- Corpus d'adaptation à un domaine particulier et son jargon: médical, légal, financier, etc.

### Tokenisation

Conversion d'un texte en une séquence de tokens (mots, caractères, sous-mots, etc.) qui seront utilisés par le modèle.

- Tokenisation: <https://fr.wikipedia.org/wiki/Analyse_lexicale>
- Byte Pair Encoding: <https://en.wikipedia.org/wiki/Byte_pair_encoding>

### Choix du type de LLM

Des architectures différentes sont adaptées aux taches à réaliser:

- "Auto-encoding" RoBERTa: textes à trous, analyse de sentiments, NER, etc.
- "Auto-regressive" GPT: génération de texte
- "Sequence-to-sequence" BART: traduction, résumé, etc.

### Fine-tuning

On change les poids du modèle pour qu'il soit adapté à une tache particulière en lui donnant des exemples de la tache à réaliser et des réponses attendues.
On peut segmenter le modèle en plusieurs parties fine-tuner une partie et géler les poids du reste. (PEFT)
Le mode INSTRUCT réponds aux instructions données par l'utilisateur.

- Fine-tuning: <https://en.wikipedia.org/wiki/Fine-tuning_(deep_learning)>
- Adaptation au domaine: <https://en.wikipedia.org/wiki/Domain_adaptation>
- Catastrophic forgetting: <https://en.wikipedia.org/wiki/Catastrophic_interference>
- Ensemble QR humain: <https://huggingface.co/datasets/knkarthick/dialogsum/viewer/knkarthick--dialogsum>
- PEFT: <https://huggingface.co/docs/peft/index>
- LoRA: <https://huggingface.co/docs/peft/conceptual_guides/lora>
- Prompt-tuning: <https://research.ibm.com/blog/what-is-ai-prompt-tuning>

### Benchmark et métriques d'évaluation

On mesure la similarité entre le texte généré et le texte humain attendu avec des métriques de correspondances comme BLEU ou ROUGE.
D'autres tests sont plus généralistes comme MMLU.

- BLEU: <https://en.wikipedia.org/wiki/BLEU>
- ROUGE: <https://en.wikipedia.org/wiki/ROUGE_(metric)>
- MMLU: <https://paperswithcode.com/sota/multi-task-language-understanding-on-mmlu>

### Renforcement par feedback humain (RLHF)

Un LLM doit suivre les HHH: Helpful, Honest and Harmless
On génère plusieurs réponses, on demande à un humain de les classer et on fine-tune le modèle vis à vis de ce feedback.
Si un LLMs est trop "serviable" il peut être manipulé par un utilisateur pour des activités malveillantes.

- PPO: <https://en.wikipedia.org/wiki/Proximal_Policy_Optimization>

### Déploiement

Compression, optimisation et déploiement du modèle sur un serveur pour qu'il puisse être répondre aux utilisateurs.

### Librairie d'orchestration

Permet au LLM de communiquer avec d'autres composants du système, de faire des requetes de données, etc.

- LangChain: <https://www.langchain.com/>

### Génération Augmentée de Récupération (RAG)

Permet d'ajouter des sources de données supplémentaires pour enrichir les réponses du modèle à travers des requetes dans des bases de données, des interrogations de moteurs de recherche, de la recherche sémantique, des appels API, etc.
La recherche par similarité vectorielle (embedding vectors) permet de trouver des réponses des textes similaires à la requete qui peuvent être intégrées dans la réponse du modèle.

- RAG: <https://arxiv.org/abs/2104.05544>
- BDD vectorielle: <https://www.pinecone.io/>
- PostGreSQL vectoriel: <https://github.com/pgvector/pgvector>
- Embedding vectors: <https://en.wikipedia.org/wiki/Word_embedding>

> Biais dans les vecteurs: <https://wikipedia2vec.github.io/demo/>

### Program aided language (PAL) model & ReACT

On donne au modèle la capacité de générer du code informatique permettant de réaliser des taches complexes.
Par exemple un calcul complexe est hors de portée d'un LLM alors qu'il peut écrire un code informatique simple pouvant le résoudre.
Le modèle a juste une tache générale et fais un plan de sous taches et d'agents pour y arriver.

- AutoLLM: <https://github.com/safevideo/autollm>
- ReAct: <https://arxiv.org/abs/2210.03629>
- LangChain: <https://www.langchain.com/>

### Prompt Engineering

Nous disposons suivant les modèles d'un espace limité pour donner des instructions au modèle, la fenetre de contexte.
C'est dans cette fenetre que nous allons indiquer:

- la définition de la "personalité" du modèle et de son orientation
- les instructions pour la tâche à réaliser
- les données issues de la génération augmentée de récupération
- la question de l'utilisateur
- l'historique de discussion avec l'utilisateur (0-shot, few-shot, etc.)

- Pré-prompt: <https://en.wikipedia.org/wiki/Prompt_engineering>
- Cours prompt engineering: <https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/>

### UI/UX

L'interface utilisateur est un élément essentiel pour que le modèle puisse être utilisé par des humains.
Elle est généralement proche d'une interface de messagerie instantanée avec des bulles de conversation.
Elle comprends également un système de gestion des utilisateurs, un historique des messages, etc.

- Interface utilisateur: <https://fr.wikipedia.org/wiki/Interface_utilisateur>
- UX: <https://fr.wikipedia.org/wiki/Exp%C3%A9rience_utilisateur>

## III - Cas pratique

Démonstration de l'utilisation de GPT-4 pour créer un chatbot catholique qui enrichi du "Cathéchisme de l'Eglise Catholique" réponds aux questions posées par les utilisateurs.
