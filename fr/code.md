---
layout: page
title: Code
permalink: /fr/code/
ref: code
description: "Développeur full-stack : deux réseaux sociaux et une plateforme de trading en Rails, Django et Laravel dans des dépôts privés, et les projets publics de sneakyweasel sur GitHub, par sujet."
---

🏆 **Nommé aux Webby Awards 2023.** Le simulateur d'optique quantique dont j'ai été le développeur principal au CQT de Singapour, devenu Virtual Lab de Quantum Flytrap, a été [nommé dans la catégorie Science](https://www.webbyawards.com/crafted-with-code/virtual-quantum-lab/) des Webby Awards 2023, les « Oscars d'Internet », avec l'équipe de Quantum Flytrap, aux côtés du Jet Propulsion Laboratory de la NASA et d'OpenAI. [Quantum Zeitgeist](https://quantumzeitgeist.com/quantum-flytraps-virtual-quantum-lab-receives-webby-award-nomination-quantum-game-gets-worldwide-recognition/) a consacré un article à cette nomination. L'histoire est sur la page [Quantique](/fr/quantum/).

L'essentiel de ce que je fabrique est du code, et l'essentiel de ce code n'est pas sur GitHub. Je suis développeur full-stack, indépendant depuis 2016 : j'ai construit deux réseaux sociaux et une plateforme de trading de bout en bout, en Rails, Django et Laravel, et ce travail vit dans des dépôts privés. Ce qui est public est sur GitHub sous le nom [sneakyweasel](https://github.com/sneakyweasel) : 31 projets à moi et 25 forks dont je suis parti, depuis 2011, surtout les projets de recherche et les projets annexes décrits sur les autres pages.

N'hésitez pas à [me contacter](mailto:philippe@cochin.fr) !

## 🏗 Full-stack, dans des dépôts privés

Deux réseaux sociaux et une plateforme de trading, chacun construit de bout en bout, en Ruby on Rails, Django et Laravel. Ils vivent dans des dépôts privés, c'est pourquoi ils n'apparaissent pas ci-dessous. Les postes et leurs dates sont sur la page [À propos](/fr/about/#parcours).

## 🧰 Langages

Sur le travail full-stack : Ruby, Python et PHP côté serveur, TypeScript et JavaScript côté client, SQL en dessous. Sur les dépôts publics, au poids en octets : Python loin devant, puis Lean 4, JavaScript et TypeScript avec Vue, HTML et CSS, LaTeX, des carnets Jupyter, et de plus petites quantités de Rust, Ruby, C++, CUDA et GLSL. En pratique : Python pour le code de recherche, TypeScript et Vue pour les interfaces, Lean 4 avec Mathlib pour les preuves, Rust quand la vitesse compte, CUDA quand une recherche doit tourner sur le GPU.

## 🔢 Théorie des nombres et preuve formelle

- [btlab](https://github.com/sneakyweasel/btlab) - le laboratoire de ternaire équilibré : arithmétique exacte, les programmes Juggler et 3n−1, une couche formelle Lean 4 + Mathlib et un vérificateur CUDA (Python, Lean, LaTeX, CUDA). Voir [Maths](/fr/math/).
- [WarpPrimes](https://github.com/sneakyweasel/WarpPrimes) - le générateur derrière mes suites de l'OEIS, avec une spirale d'Ulam en D3 (Python, JavaScript)
- [padic-rust](https://github.com/sneakyweasel/padic-rust) et [padic-ts](https://github.com/sneakyweasel/padic-ts) - des bibliothèques de nombres p-adiques en Rust et en TypeScript
- [Euler](https://github.com/sneakyweasel/Euler) et [DNA](https://github.com/sneakyweasel/DNA) - Project Euler en Ruby, la bio-informatique de Rosalind en Python

## ⚛️ Quantique

- [quantumweasel](https://github.com/sneakyweasel/quantumweasel) - une simulation d'optique quantique légère sur le moteur quantum-tensors (TypeScript)
- [photon](https://github.com/sneakyweasel/photon) et [quantum-photon-vue](https://github.com/sneakyweasel/quantum-photon-vue) - visualisation d'états de photons en D3, puis en composant Vue autonome
- [QuantumDisplay](https://github.com/sneakyweasel/QuantumDisplay) et [ComingSoonQuantum](https://github.com/sneakyweasel/ComingSoonQuantum) - amorce front-end et page d'attente de Quantum Game 2 au CQT ; le jeu lui-même est [Quantum-Game/quantum-game-2](https://github.com/Quantum-Game/quantum-game-2), construit sur [quantum-tensors](https://github.com/Quantum-Flytrap/quantum-tensors)
- [genetic-quantum-correction](https://github.com/sneakyweasel/genetic-quantum-correction) - un algorithme génétique pour les casse-têtes de Decodoku sur le code torique, cité dans Phys. Rev. A (JavaScript). Voir [Quantique](/fr/quantum/).
- [quantum-loom](https://github.com/sneakyweasel/quantum-loom) - tressage d'anyons : construire les portes manquantes d'un ordinateur quantique universel à partir de quasi-particules tressées, avec le moins de tresses possible (JavaScript)
- [quintessence](https://github.com/sneakyweasel/quintessence) - MIT iQuHACK 2023 : une recherche par marche quantique sur du matériel IonQ alimentant un pipeline génératif (Jupyter, Python, Vue)

## 🤖 IA et agents

- [genetic-growth](https://github.com/sneakyweasel/genetic-growth) - une croissance inspirée de l'embryologie, encodée en un petit « ADN » d'opcodes et exécutée tic par tic sur un tissu de Voronoï (TypeScript)
- [open-catholic](https://github.com/sneakyweasel/open-catholic) - le Catéchisme de l'Église catholique converti en Markdown avec des liens internes, comme texte lisible et comme corpus de récupération
- [mimic-octopus](https://github.com/sneakyweasel/mimic-octopus) - un chatbot de 2015 sur Hubot, ma première « IA philosophique axiomatique »
- Repris de : [Auto-GPT](https://github.com/sneakyweasel/Auto-GPT), un [bot Telegram GPT](https://github.com/sneakyweasel/chatgpt_telegram_bot) personnel, les [compagnons IA à mémoire](https://github.com/sneakyweasel/catholicum-companion) d'a16z, l'[inversion textuelle](https://github.com/sneakyweasel/sd-enable-textual-inversion) pour Stable Diffusion, la [détection d'objets TensorFlow sur un Raspberry Pi](https://github.com/sneakyweasel/TF-OD-Pi-Test), un [modèle de trading LSTM](https://github.com/sneakyweasel/freqAI-LSTM) et le neurofeedback [OpenNFB](https://github.com/sneakyweasel/OpenNFB)

## 🔐 Cybersécurité

- [hhhhh](https://github.com/sneakyweasel/hhhhh) - un outil d'attaque par extension de longueur de hachage, construit pour le CTF de la DGA (Python), le versant pratique de l'habitude des CTF et du bug bounty

## 🩺 Matériel libre pour la Covid-19

- [covid3d.org](https://web.archive.org/web/20200501153857/https://covid3d.org/) - le site que j'ai codé pour COVID3D-APHP, la fédération des initiatives de conception et d'impression 3D contre la Covid-19 en Île-de-France, cofondée en mars 2020 autour de la ferme d'impression 3D de l'hôpital Cochin : les modèles open source d'équipements de protection et de matériel médical conçus pour la crise. Le lien mène à la copie archivée.
- [COVID](https://github.com/sneakyweasel/COVID) et [COVID-FR](https://github.com/sneakyweasel/COVID-FR) - la liste des projets de matériel médical d'urgence open source rassemblée au début de la pandémie, maintenue aujourd'hui sur [AmisDesMalades/COVID](https://github.com/AmisDesMalades/COVID)
- [Respirateur-COVID](https://github.com/sneakyweasel/Respirateur-COVID) - un prototype de respirateur d'urgence construit autour d'un ballon Ambu
- [OpenICU](https://github.com/sneakyweasel/OpenICU) - des idées pour une unité de soins intensifs à bas coût et de haut niveau

## 🎮 Jeux, graphisme et visualisation

- [GameOfFire](https://github.com/sneakyweasel/GameOfFire) - l'hommage de Quanta Magazine à Conway (Vue, TypeScript)
- [HoloWeasel](https://github.com/sneakyweasel/HoloWeasel) - un écran holographique Looking Glass piloté avec Three.js et des shaders WebGL (JavaScript, GLSL)
- [ts-grid](https://github.com/sneakyweasel/ts-grid) - un portage TypeScript des grilles de Red Blob Games : grilles carrées, triangulaires et hexagonales avec leurs arêtes, sommets et tuiles
- Repris de : le Jeu de la vie en [Vue 2](https://github.com/sneakyweasel/Game-of-Life-Vue2) et en [Rust et WebAssembly](https://github.com/sneakyweasel/wasm_game_of_life), [particle-life](https://github.com/sneakyweasel/particle-life), le jeu de tactique en Rust [zemeroth](https://github.com/sneakyweasel/zemeroth), un [composant Vue de démineur](https://github.com/sneakyweasel/vue-defuse), les [Alligator Eggs](https://github.com/sneakyweasel/AlligatorEggs) de Bret Victor pour le lambda-calcul, et [OpenRelativity](https://github.com/sneakyweasel/OpenRelativity)

## 🌐 Web et outillage

- [sneakyweasel.github.io](https://github.com/sneakyweasel/sneakyweasel.github.io) - ce site, Jekyll sur GitHub Pages
- [rails-devise-pundit](https://github.com/sneakyweasel/rails-devise-pundit) - base d'authentification et d'autorisation pour Rails
- Repris de : un [squelette de bibliothèque TypeScript](https://github.com/sneakyweasel/typescript-library-starter), le [guide React, Redux et TypeScript](https://github.com/sneakyweasel/react-redux-typescript-guide), [hubot-meteorchat](https://github.com/sneakyweasel/hubot-meteorchat), [vim-sneak](https://github.com/sneakyweasel/vim-sneak), un [Held-Karp](https://github.com/sneakyweasel/held-karp) en pur Python et [Programming with Nothing](https://github.com/sneakyweasel/nothing) de Tom Stuart
