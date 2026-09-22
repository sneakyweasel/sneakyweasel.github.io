---
layout: page
title: IA
permalink: /fr/ai/
ref: ai
description: "Systèmes LLM en production, workflows agentiques, modèles locaux, pipelines de médias génératifs et recherche avec des modèles, par un développeur qui travaille sur l'IA depuis 2016."
---

Je travaille sur l'IA depuis 2016 et construire des systèmes à base de modèles de langage est mon métier, aujourd'hui en freelance. Avec [Logicien](https://www.logicien.fr), je construis des IA sur mesure pour les organisations qui veulent en garder la maîtrise : leur code, leur infrastructure. Ce qui suit est ce que je fais réellement, avec les dépôts qui le montrent.

N'hésitez pas à [me contacter](mailto:philippe@cochin.fr) !

## 🛠 Ce que je construis

- **Des systèmes LLM en production** : génération augmentée par récupération sur des données structurées, embeddings et recherche vectorielle, usage d'outils, évaluation, et toute la plomberie qui oblige un modèle à rester honnête sur ses sources. Exemple de corpus : le Catéchisme converti en une [base de récupération](https://github.com/sneakyweasel/open-catholic) Markdown reliée, pour un assistant GPT-4.
- **Des workflows agentiques** : je mène la recherche comme une opération multi-agents. Le [laboratoire de ternaire équilibré](https://github.com/sneakyweasel/btlab) est travaillé par plusieurs agents de codage à la fois, sous un guide écrit pour les agents, des compétences sur mesure, un serveur MCP pour Lean, un index des théorèmes que les agents doivent interroger avant de toucher à une preuve, et des garde-fous qui refusent un manuscrit dont les nombres ne se reproduisent pas. Chaque branche se termine par une décision consignée, et ce qui a échoué est conservé pour que personne ne le redécouvre.
- **Des modèles locaux sur mon propre matériel** : une RTX 5090 qui fait tourner Qwen3-8B, GPT-2 XL, Whisper large-v3, FLUX et Wan via ComfyUI. J'écris autour d'eux le code de notation, de traitement par lots reprenable et de file d'attente GPU ; la prochaine étape est un petit prouveur affiné sur les lemmes du laboratoire lui-même.
- **Des pipelines de médias génératifs** : des paroles écrites en conversation, l'audio par Suno, chaque prise réécoutée par Whisper et alignée sur les paroles avant de pouvoir être masterisée, des pochettes rendues avec FLUX sous une seule règle visuelle, des boucles vidéo avec Wan, le tout verrouillé par des scripts qui refusent d'empaqueter une sortie à laquelle il manque un champ. Le résultat est sur la page [Art](/fr/art/).
- **Du machine learning et du deep learning classiques** : GAN et deepfakes, détection d'objets sur un Raspberry Pi, prévision par LSTM, neurofeedback ; et des méthodes évolutionnaires, d'un [algorithme génétique](https://github.com/sneakyweasel/genetic-quantum-correction) pour la correction d'erreurs quantiques qui a fini cité dans Phys. Rev. A à une [croissance inspirée de l'embryologie](https://github.com/sneakyweasel/genetic-growth) encodée en ADN d'opcodes.

## 🔬 De la recherche avec des modèles

- **Mesurer ce qu'un modèle trouve inévitable.** Avec un modèle local, je note chaque ligne d'un texte pour sa surprise, son entropie et ce que les lignes précédentes lui ont fait mériter, ce qui trie les lignes en inévitables, chutes, clichés et bruit. La probabilité du token de rire détecte les blagues sans entraînement à 0,85 d'AUC sur des jeux de données notés par des humains, deux modèles dont les tailles diffèrent d'un facteur dix s'accordent à 0,85 de corrélation de rang sur les lignes méritées, et un album de mon cru a été placé face à 3 043 vraies chansons sur la même échelle. La même sonde tourne sur quatre mille preuves Lean vérifiées par le noyau, où la surprise se loge dans le choix du lemme appelé. Les prédictions sont écrites avant chaque passage, et les échecs sont publiés avec le reste.
- **Des mathématiques formelles assistées par l'IA.** Des agents rédigent et réparent des preuves Lean 4 contre Mathlib à l'intérieur du laboratoire, avec vérification des axiomes et aucun `sorry` laissé passer ; l'index des théorèmes empêche humains et agents de prouver deux fois le même lemme. Voir [Maths](/fr/math/).
- **Un cerveau dans la boucle.** La prochaine étape est un protocole EEG sur mon propre montage OpenBCI, seize canaux, pour tester si les lignes qu'un modèle dit méritées arrivent différemment chez un lecteur humain, avec la N400 pour étalon. Le montage, les marqueurs et l'analyse sont écrits ; la réponse n'est pas encore là.
- **Du machine learning quantique**, une fois, au MIT iQuHACK 2023 : une recherche par marche quantique sur du matériel IonQ alimentant des transformers et Stable Diffusion, [Quintessence](https://github.com/sneakyweasel/quintessence).

## 🛡 Sûreté, éthique et débat public

- Injection de prompt, jailbreaks et red teaming, côté attaquant comme côté défenseur ; la sûreté de l'IA comme discipline d'ingénierie plutôt que comme slogan.
- Quatre années de philosophie et de théologie avant une carrière dans l'IA me donnent un point de vue inhabituel sur ce que ces systèmes sont et ne sont pas. J'en ai parlé à Sorbonne Université, dans des conférences religieuses de haut niveau et devant un conseil d'éthique à Paris. Les notes de certaines de ces interventions sont parmi les [billets](/fr/) de la page d'accueil.

## 📜 Certificats

- [Deep Learning Specialization](https://coursera.org/share/060c260c19a2007f337dfae390fe4382) et [Generative AI with Large Language Models](https://coursera.org/share/e39f9086732f131d4d6b0fef988d9d82), tous deux d'Andrew Ng. La liste complète est sur la page [Certifications](/fr/certifications/).
