---
layout: page
title: Maths
permalink: /fr/math/
ref: math
description: "Ternaire équilibré, trois suites de l'OEIS, le laboratoire btlab et sa couche formelle Lean 4, quatre prépublications sur l'application Juggler et l'application 3n−1."
---

J'aime les représentations des nombres qui rendent la structure visible. Le ternaire équilibré, où chaque entier est un unique mot sur les chiffres `-`, `0`, `+`, est ma préférée, et l'essentiel de mon travail mathématique depuis 2019 en découle.

N'hésitez pas à [me contacter](mailto:philippe@cochin.fr) !

Mes publications sont recensées sur ORCID : [0009-0004-1939-3382](https://orcid.org/0009-0004-1939-3382).

## 🔢 Suites de l'OEIS

En janvier 2019, j'ai contribué trois suites à l'[OEIS](https://oeis.org/wiki/User:Philippe_Cochin), les « warp primes » : des nombres premiers dont la représentation en ternaire équilibré, lue à l'envers, est encore un nombre premier ou l'opposé d'un nombre premier.

- [A323782](https://oeis.org/A323782) - les premiers dont le renversement est un premier ou l'opposé d'un premier
- [A323783](https://oeis.org/A323783) - les valeurs renversées correspondantes, a(n) = A134028(A323782(n))
- [A323784](https://oeis.org/A323784) - les premiers dont le renversement est un nombre composé
- Le code Python, les b-files jusqu'à 10^6 et une spirale d'Ulam en D3 des deux familles de premiers : [WarpPrimes](https://github.com/sneakyweasel/WarpPrimes)

## 🧪 Laboratoire mathématique de ternaire équilibré

[btlab](https://github.com/sneakyweasel/btlab) est une plateforme de recherche en arithmétique exacte (Python, licence MIT). Son cœur est le ternaire équilibré : encodage, arithmétique, opérateurs, un calcul sur les trits, polynômes, automates et transducteurs. Les problèmes ouverts y sont attachés comme des modules indépendants qui importent le cœur, jamais l'inverse.

- Chaque affirmation porte sa classe de preuve : preuve humaine, vérifiée en Lean, vérifiée par calcul, conjecture, observation ou réfutée. Les vérifications finies ne sont jamais présentées comme des preuves.
- Chaque direction de recherche passe par explorer, distiller, prouver ou réfuter, décider, sous un budget écrit, et se termine par exactement une décision : promouvoir, mettre en attente ou clore. Les branches closes restent documentées pour que personne ne les redécouvre.
- La couche formelle est [Lean 4 avec Mathlib](https://github.com/sneakyweasel/btlab/tree/main/formal), sans aucun `sorry`.

## 🤹 L'application Juggler

Le problème sur lequel je travaille est l'application Juggler ([A094683](https://oeis.org/A094683)) : T(n) = ⌊√n⌋ si n est pair et ⌊n√n⌋ si n est impair. Savoir si toute orbite atteint 1 est une question ouverte, comme pour Collatz. Trois prépublications, septembre 2026, sur Zenodo sous licence CC BY 4.0 :

- [Lower Bounds for Cycle Lengths in the Juggler Map](https://doi.org/10.5281/zenodo.22676452) - une inégalité de financement des cycles, n log n (3^o - 2^L) <= L 3^o pour un cycle de longueur L à o pas impairs, raffinée par une rotation irrationnelle et des estimations de Denjoy-Koksma, donne des bornes inférieures sur la période des hypothétiques cycles non triviaux à chaque plancher de descente vérifié.
- [Fate Contagion and Termination Criteria for the Juggler Map](https://doi.org/10.5281/zenodo.22678164) - tout ensemble clos par préimages, donc tout bassin de cycle et l'ensemble des orbites non bornées s'il en existe, a une masse logarithmique d'au moins c (log x)^lambda pour tout lambda inférieur à environ 0,4927 ; la seconde preuve est formalisée en Lean 4 dans btlab pour tout lambda <= 100/203.
- [Five-Step Descent Certificates for the Juggler Map: Parity Statistics of Nested Floor Powers](https://doi.org/10.5281/zenodo.22864933) - les valeurs de départ qui admettent un certificat de descente par enveloppe de puissances en cinq opérations ont pour densité naturelle 7/8 (13/16 pour quatre), par des identités de retenue exactes, des développements de Fourier centrés et la différenciation de van der Corput.

Rien de tout cela ne prétend résoudre les problèmes de Juggler ou de Collatz. Un [compagnon interactif](https://balanced-ternary-beta.vercel.app) permet d'explorer les orbites.

## 🔁 L'application 3n−1

L'application 3n−1 (g(y) = y/2 pour y pair et (3y−1)/2 pour y impair) est l'application 3n+1 raccourcie, lue sur les entiers négatifs. Ses cycles connus sont 1, (5, 7, 10) et le cycle à onze éléments issu de 17, et tout point de départ inférieur à 2^51 atteint l'un d'eux. Une prépublication, septembre 2026, sur Zenodo sous licence CC BY 4.0 :

- [No m-cycles of the 3n−1 map for m ≤ 58](https://doi.org/10.5281/zenodo.22876189) - le schéma de Simons–de Weger pour les m-cycles de 3n+1, transposé à cette application avec ses constantes dérivées de ce côté-ci et combiné à la borne de Rhin sur les formes linéaires de logarithmes : aucun m-cycle avec 1 ≤ m ≤ 58 en dehors des deux connus. L'énoncé est nouveau pour 3 ≤ m ≤ 58 ; pour m ≤ 2, c'est une forme, dépendant du plancher, d'un théorème de Simons.

## 🧮 Jouets plus anciens

- [padic-rust](https://github.com/sneakyweasel/padic-rust) et [padic-ts](https://github.com/sneakyweasel/padic-ts) - des bibliothèques de nombres p-adiques en Rust et en TypeScript
- [Euler](https://github.com/sneakyweasel/Euler) et [DNA](https://github.com/sneakyweasel/DNA) - mes archives Project Euler et Rosalind
