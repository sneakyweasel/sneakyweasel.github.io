---
layout: page
title: Maths
permalink: /fr/math/
ref: math
description: "L'application Juggler et les applications de Collatz signées : cinq prépublications, le laboratoire btlab, le compagnon visuel Frontier Forge, et trois suites de l'OEIS en ternaire équilibré."
---

J'aime les représentations des nombres qui rendent la structure visible. Le ternaire équilibré, où chaque entier est un unique mot sur les chiffres `-`, `0`, `+`, est ma préférée, et l'essentiel de mon travail mathématique depuis 2019 en découle. Ce travail porte aujourd'hui sur deux problèmes ouverts, l'application Juggler et les applications de Collatz signées, travaillés dans un seul laboratoire, rédigés en prépublications et dessinés sur un site compagnon.

N'hésitez pas à [me contacter](mailto:philippe@cochin.fr) !

## 🤹 Deux problèmes ouverts

**L'application Juggler** ([A094683](https://oeis.org/A094683)) envoie n sur ⌊√n⌋ si n est pair et sur ⌊n√n⌋ si n est impair. Savoir si toute orbite atteint 1 est une question ouverte, comme pour Collatz : une orbite pourrait aussi tomber dans un autre cycle ou croître sans limite, et les articles ci-dessous ne tranchent pas.

**L'application 3n−1** envoie y sur y/2 si y est pair et sur (3y−1)/2 si y est impair ; c'est l'application 3n+1 raccourcie, lue sur les entiers négatifs. Ses cycles connus sont 1, (5, 7, 10) et le cycle à onze éléments issu de 17, et tout point de départ inférieur à 2^51 atteint l'un d'eux. Avec 3n+1, elle forme les applications de Collatz signées.

## 📄 Publications

Mes publications sont recensées sur ORCID : [0009-0004-1939-3382](https://orcid.org/0009-0004-1939-3382). Les cinq prépublications, toutes de septembre 2026, sont sur Zenodo sous licence CC BY 4.0 ; chaque lien est le DOI de concept, qui ouvre toujours la dernière version.

- **A.** [Lower Bounds for Cycle Lengths in the Juggler Map](https://doi.org/10.5281/zenodo.22676452) - une inégalité de financement des cycles, n log n (3^o − 2^L) ≤ L·3^o pour un cycle de minimum n, de longueur L à o pas impairs, raffinée par une rotation irrationnelle, des estimations de Denjoy–Koksma et des décompositions d'Ostrowski. Avec le plancher de descente vérifié de 350 000 000, tout cycle non trivial aurait au moins 780 239 pas.
- **B.** [Five-Step Descent Certificates for the Juggler Map: Parity Statistics of Nested Floor Powers](https://doi.org/10.5281/zenodo.22864933) - les valeurs de départ qui admettent un certificat de descente par enveloppe de puissances en cinq opérations ont pour densité naturelle 7/8 (13/16 en quatre), par des identités de retenue exactes, des développements de Fourier centrés et la différenciation de van der Corput. Son théorème 6.3, un résultat de juste part pour les deux mots de cinq lettres, a une preuve écrite assistée par IA qui n'a pas encore été relue de façon indépendante.
- **C.** [Fate Contagion and Termination Criteria for the Juggler Map](https://doi.org/10.5281/zenodo.22678164) - tout ensemble non vide clos par préimages, donc tout bassin de cycle et l'ensemble des orbites non bornées s'il en existe, vérifie ∑ 1/n ≥ c (log x)^(37/50) sur ses éléments jusqu'à x, pour tout x assez grand. L'exposant 37/50 utilise le théorème 6.3 de l'article B ; sans lui, l'exposant est 5/8, et ce résultat est vérifié en Lean de bout en bout.
- **D.** [No m-cycles of the 3n−1 map for m ≤ 61](https://doi.org/10.5281/zenodo.22876189) - le schéma de Simons–de Weger pour les m-cycles de 3n+1, transposé à l'application 3n−1 avec ses constantes dérivées de ce côté-ci et combiné à la borne de Rhin sur les formes linéaires de logarithmes : aucun m-cycle avec 1 ≤ m ≤ 61 en dehors des deux connus. Pour 3 ≤ m ≤ 61, aucun énoncé antérieur n'est connu ; pour m ≤ 2, c'est une forme, dépendant du plancher, d'un théorème de Simons.
- **E.** [The Juggler Map and the 3n±1 Maps: Exact Coding and Arithmetic Obstructions](https://doi.org/10.5281/zenodo.22905649) - le codage par parité envoie exactement toute orbite de Juggler dans le système 2-adique de 3n−1 et, sur les orbites périodiques, conserve chaque temps de retour ; sa valeur est un entier exactement quand une divisibilité de mots est vérifiée, et un retour modulaire aussi précis qu'on veut n'impose pas cette divisibilité. Sur les entiers positifs, toute cible de 3n−1 première avec trois a au moins X^(21/25) ancêtres inférieurs à X, pour tout X assez grand. Des formalisations Lean accompagnent les résultats principaux.
- [Visualizing quantum mechanics in an interactive simulation: Virtual Lab by Quantum Flytrap](https://doi.org/10.1117/1.OE.61.8.081808), Optical Engineering 61(8), 081808 (2022), avec P. Migdał, K. Jankiewicz, P. Grabarz et C. Decaroli. La physique est sur la page [Quantique](/fr/quantum/).

Rien de tout cela ne prétend résoudre les problèmes de Juggler ou de Collatz.

## 🧭 Frontier Forge

[Frontier Forge](https://www.frontierforge.io/) est le versant visuel des articles : des images qu'on peut parcourir, conçues pour les prépublications sur Juggler. Le site s'ouvre sur les trois destins possibles d'une orbite, avec une [visite guidée](https://www.frontierforge.io/tour/the-map) des images, un [bac à sable](https://www.frontierforge.io/play/trajectory) qui parcourt n'importe quel point de départ et ses préimages, et [What the paper claims](https://www.frontierforge.io/claims), un tableau en langage clair qui met chaque énoncé de l'article A en regard de sa preuve. Les PDF restent les preuves.

## 🧪 btlab

[btlab](https://github.com/sneakyweasel/btlab), le laboratoire de ternaire équilibré, est devenu le Juggler–Collatz Mathematical Laboratory : le dépôt public, sous licence MIT, où ces articles sont fabriqués. Il suit chaque question de l'exploration jusqu'à une preuve ou un contre-exemple, et consigne ce qui a échoué à côté de ce qui a marché.

- **Articles** : les sources des cinq prépublications, reconstruites par un seul outil et épinglées aux données qu'elles rapportent, avec leurs PDF et leurs dossiers de publication.
- **Lean 4** : une bibliothèque sur Mathlib, sans aucun `sorry`, auditée pour ses axiomes. Son outil de recherche, Formalpedia, retrouve un résultat par nom, par énoncé ou par affirmation liée.
- **Degrés de preuve** : un registre des théorèmes étiquette chaque affirmation comme preuve écrite, preuve Lean, calcul fini, conjecture, observation, réfutation ou reparamétrage. Les résultats conditionnels gardent leurs hypothèses ouvertes, et une vérification finie ne prouve que son domaine annoncé.
- **Calcul** : des expériences Python exactes avec leur provenance consignée, des bornes numériques certifiées avec FLINT/Arb, et un vérificateur CUDA qui calcule les planchers de vérification finis sur le GPU.
- **Mémoire** : un dossier par investigation, et un registre des connaissances négatives qui dit pourquoi une piste a échoué et ce qui permettrait de la rouvrir. Le ternaire équilibré et l'arithmétique exacte en restent le socle commun.

## 🔢 Suites de l'OEIS

En janvier 2019, j'ai contribué trois suites à l'[OEIS](https://oeis.org/wiki/User:Philippe_Cochin), les « warp primes » : des nombres premiers dont la représentation en ternaire équilibré, lue à l'envers, est encore un nombre premier ou l'opposé d'un nombre premier.

- [A323782](https://oeis.org/A323782) - les premiers dont le renversement est un premier ou l'opposé d'un premier
- [A323783](https://oeis.org/A323783) - les valeurs renversées correspondantes, a(n) = A134028(A323782(n))
- [A323784](https://oeis.org/A323784) - les premiers dont le renversement est un nombre composé
- Le code Python, les b-files jusqu'à 10^6 et une spirale d'Ulam en D3 des deux familles de premiers : [WarpPrimes](https://github.com/sneakyweasel/WarpPrimes)

## 🧮 Jouets plus anciens

- [padic-rust](https://github.com/sneakyweasel/padic-rust) et [padic-ts](https://github.com/sneakyweasel/padic-ts) - des bibliothèques de nombres p-adiques en Rust et en TypeScript
- [Euler](https://github.com/sneakyweasel/Euler) et [DNA](https://github.com/sneakyweasel/DNA) - mes archives Project Euler et Rosalind
