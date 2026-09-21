---
layout: post
title:  "Notes de conférence genAI et education"
date:   2024-01-05 16:13:05 +0200
categories: AI
---

## Intro

On utilise beaucoup les termes apprentissage-machine (Machine Learning), apprentissage-profond (Deep Learning) et l'on a tendance à oublier que l'apprentissage est d'abord un processus biologique naturel qui est utilisé par presque tous les êtres vivants. (vidéo renardeau qui joue)
D'un point de vue biologique l'apprentissage se traduit par le renforcement des connexions synaptiques dans le cerveau. (image synapse)
Lorsqu'on parle d'apprentissage-machine on parle d'un processus mathématique qui est inspiré de ce processus biologique que nous allons maintenant décrire.

## Réseau de neurones artificiels (Artificial Neural Network)

### Difficulté de l'informatique classique

- L'informatique classique est basée sur des instructions logiques qui sont exécutées par un processeur. Ces instructions sont exécutées séquentiellement et sont déterministes. Cela signifie que si on exécute deux fois le même programme avec les mêmes données en entrée, on obtiendra toujours le même résultat en sortie.
- Cela fonctionne très bien pour des tâches précises et bien définies comme par exemple additionner deux nombres ou trier une liste de nombres.
- Cependant, le monde est flou, imprécis et incertain et les humains ont évolué pour s'adapter à ce monde. Nous sommes capables de prendre des décisions dans des situations incertaines, nous sommes capables de nous adapter à des situations nouvelles, d'extrapoler des informations manquantes et de prendre des décisions en fonction de notre expérience passée.

### Réseau de neurones artificiels

- Par bio-mimétisme les chercheurs ont essayé de reproduire cette faculté humaine en créant des réseaux de neurones artificiels copiés sur le cerveau humain.
- Un réseau de neurones artificiels est un ensemble de neurones artificiels connectés entre eux. Chaque neurone artificiel est une fonction mathématique qui prend en entrée un vecteur de nombres et qui renvoie un nombre. (image ANN)

### Perceptron

- Le perceptron est le neurone artificiel le plus simple. Il prend en entrée un vecteur de nombres et renvoie un nombre. (image perceptron)

### Apprentissage supervisé

- On va suivre rapidement le parcours de l'information dans le perceptron. (vidéo 3b1b)
- On va démarrer avec des poids aléatoires et on va faire passer des données en entrée dans le perceptron. On va comparer la sortie du perceptron avec la sortie attendue et on va ajuster les poids pour que la sortie du perceptron se rapproche de la sortie attendue. (vidéo 3b1b)
- On va répéter ce processus des millions de fois avec des données différentes et à la fin on va obtenir un perceptron qui est capable de prédire la sortie attendue à partir de l'entrée. (descente de gradient)

### Interrogation du modèle

- On peut maintenant interroger le modèle en lui donnant une entrée et en lui demandant de prédire la sortie. C'est ce qu'on appelle l'inférence.

### Vocabulaire

- LLMs: Large Language Models
- IA: "Intelligence" Artificielle
- Embedding: Vecteur de nombres qui représente un mot dans un espace vectoriel.
- Poids (weight): Force de la connexion entre deux neurones dans le réseau. Coeur du réseau de neurones.
- Pré-Prompt: Texte qui défini le contexte, le ton de la réponse.
- Prompt: Question de l'utilisateur envoyée au modèle pour le guider dans la génération de texte.

## IA génératives

### LLMs (ChatGPT, GPT-4, Llama2, etc.)

- Plusieurs innovations ont permis l'émergence de l'IA générative: le modèle mathématique de transformers qui permet et la forte augmentation des capacités de calcul parallelisé.
- Le langage est une structure séquentielle où la position des mots a de l'importance. (image texte)
- Les LLMs sont des modèles de langage qui sont capables de générer du texte à partir d'un texte d'entrée. (image LLM)
- Ce sont des algorithmes de prédiction du mot d'après. (image LLM)

### Génération d'images

- Les IA génératives ne sont pas limitées au texte. On peut aussi générer des images. (image GAN)
- Démo de Dall-E: <https://openai.com/blog/dall-e/>
- Démo: <https://thispersondoesnotexist.com/>

### Génération de code

- Démo: <https://copilot.github.com/>
- Recursion des IA qui se codent elle meme (autoGPT).
