---
layout: page
title: Math
permalink: /math/
ref: math
description: "The Juggler map and the signed Collatz maps: six preprints, the frontier-lab laboratory, its visual companion, Frontier Forge, and three OEIS sequences in balanced ternary."
---

I like number representations that make structure visible. Balanced ternary, where every integer is one unique word over the digits `-`, `0`, `+`, is my favourite, and most of my mathematical work since 2019 grows out of it. Today that work is two open problems, the Juggler map and the signed Collatz maps, worked in one laboratory, written up as six preprints and drawn on a companion site.

Feel free to [contact me](mailto:philippe@cochin.fr)!

## 🤹 Two open problems

**The Juggler map** ([A094683](https://oeis.org/A094683)) sends n to ⌊√n⌋ when n is even and to ⌊n√n⌋ when n is odd. Whether every orbit reaches 1 is open, as it is for Collatz: an orbit could also fall into another cycle or grow without bound, and the papers below do not pick a fate.

**The 3n−1 map** sends y to y/2 when y is even and to (3y−1)/2 when y is odd; it is the shortcut 3n+1 map read on the negative integers. Its known cycles are 1, (5, 7, 10) and the eleven-element cycle at 17, and every start below 2^51 reaches one of them. Together with 3n+1 it makes up the signed Collatz maps.

## 📄 Publications

My publications are listed on ORCID: [0009-0004-1939-3382](https://orcid.org/0009-0004-1939-3382). The six preprints, from September and October 2026, are on Zenodo under CC BY 4.0; each link is the concept DOI, which always opens the latest version.

- **A.** [Lower Bounds for Cycle Lengths in the Juggler Map](https://doi.org/10.5281/zenodo.22676452) - a cycle-financing inequality, n log n (3^o − 2^L) ≤ L·3^o for a cycle with minimum n, length L and o odd steps, refined through an irrational rotation, Denjoy–Koksma estimates and Ostrowski decompositions. With the verified descent floor of 350,000,000, any nontrivial cycle would need at least 780,239 steps.
- **B.** [Five-Step Descent Certificates for the Juggler Map: Parity Statistics of Nested Floor Powers](https://doi.org/10.5281/zenodo.22864933) - the starting values that admit a power-envelope descent certificate within five operations have natural density 7/8 (13/16 within four), by exact carry identities, centred Fourier expansions and van der Corput differencing. Its Theorem 6.3, a fair-share result for the two five-letter words, has an AI-assisted written proof that has not yet been independently reviewed.
- **C.** [Fate Contagion and Termination Criteria for the Juggler Map](https://doi.org/10.5281/zenodo.22678164) - every nonempty set closed under preimages, so every cycle basin and the set of unbounded orbits if there are any, satisfies ∑ 1/n ≥ c (log x)^(37/50) over its elements up to x, for all large x. The exponent 37/50 uses Theorem 6.3 of Paper B; without it the exponent is 5/8, and that result is machine-checked in Lean end to end.
- **D.** [No m-cycles of the 3n−1 map for m ≤ 61](https://doi.org/10.5281/zenodo.22876189) - the Simons–de Weger template for 3n+1 m-cycles, transposed to the 3n−1 map with its constants derived on this side and combined with Rhin's bound on linear forms in logarithms: no m-cycle with 1 ≤ m ≤ 61 other than the two known ones. For 3 ≤ m ≤ 61 no earlier statement is known; for m ≤ 2 it is a floor-dependent form of a theorem of Simons.
- **E.** [The Juggler Map and the 3n±1 Maps: Exact Coding and Arithmetic Obstructions](https://doi.org/10.5281/zenodo.22905649) - parity coding maps every Juggler orbit exactly into the 2-adic 3n−1 system and, on periodic orbits, keeps every return time; its value is an integer exactly when a word divisibility holds, and arbitrarily precise modular return does not force that divisibility. On the positive integers, every 3n−1 target prime to three has at least X^(21/25) ancestors below X, for all large X. Lean formalizations accompany the main results.
- **F.** [Beatty First-Passage Counts: Limit Laws, Fractal Geometry, and Arithmetic Rigidity](https://doi.org/10.5281/zenodo.23090399) - for a slope α > 1, count the binary words of length ⌊αr⌋ + 1 whose running proportion of ones stays at least 1/α on every proper prefix and falls below it at the last letter. For every α the normalized counts converge to an explicit limit law; at irrational slopes they follow the Beatty phase {rα}, which proves a hypothesis of Bauer, Godrèche and Luck, and the law is singular continuous on a null perfect set. That set has Minkowski dimension 2/3 at every irrational slope, while its Hausdorff dimension is governed by Diophantine approximation and takes every value in [0, 2/3]. The main limit and geometry theorems are formalized in Lean 4; the paper grew out of a boundary rate in Paper B.
- [Visualizing quantum mechanics in an interactive simulation: Virtual Lab by Quantum Flytrap](https://doi.org/10.1117/1.OE.61.8.081808), Optical Engineering 61(8), 081808 (2022), with P. Migdał, K. Jankiewicz, P. Grabarz and C. Decaroli. The physics is on the [Quantum](/quantum/) page.

None of this claims a solution of the Juggler or Collatz problems.

## 🎨 Juggler companion

The [Juggler companion](https://frontier-lab-quantumweasel.vercel.app/) is the visual side of the papers: pictures you can walk, built for the Juggler preprints. It opens on the three possible fates of an orbit, with a [tour](https://frontier-lab-quantumweasel.vercel.app/tour/the-map) of the pictures in fourteen chapters, a [playground](https://frontier-lab-quantumweasel.vercel.app/play/trajectory) that walks any start and its preimages and now explores the Beatty profile of Paper F, and [What the paper claims](https://frontier-lab-quantumweasel.vercel.app/claims), a plain-English scoreboard that sets each statement of Paper A beside its evidence. The PDFs remain the proofs.

## 🧪 frontier-lab

frontier-lab, formerly btlab, the balanced ternary laboratory, is the mathematical research laboratory where the papers above are made. It follows each question from exploration to a proof or a counterexample, and records what failed alongside what worked. The repository is private; each paper's sources and a standalone Lean supplement are deposited with it on Zenodo.

- **Papers**: the sources of the six preprints, rebuilt by one builder and pinned to the data they report, with their PDFs and publication kits.
- **Lean 4**: a library on Mathlib with no `sorry`, audited for axioms. Its search tool, Formalpedia, finds a result by name, statement or linked claim.
- **Evidence**: a theorem ledger labels every claim as a written proof, a Lean proof, a finite computation, a conjecture, an observation, a refutation or a reparameterization. Conditional results keep their open assumptions, and a finite check proves only its stated range.
- **Computation**: exact Python experiments with recorded provenance, certified numerical bounds with FLINT/Arb, and a CUDA verifier that runs the finite verification floors on the GPU.
- **Memory**: a dossier for each investigation, and a register of negative knowledge that says why a route failed and what would reopen it. Balanced ternary and exact arithmetic remain the shared foundation.

## 🧭 Frontier Forge

[Frontier Forge](https://frontierforge.io/) is a cooperative research strategy world, and a separate project from the laboratory. Its map represents mathematical understanding: a contributor opens an invitation, picks a bounded mission and hands it to their own coding agent, and what the agent returns is reviewed before it changes the map or earns any credit. Underneath is a Rust kernel over PostgreSQL that records provenance, attempts, failed work and signed verification receipts. It is an invited pilot in a private repository; the first raid reproduces a bounded Juggler certificate result from the laboratory, which keeps its own claims and proofs.

## 🔢 OEIS sequences

In January 2019 I contributed three sequences to the [OEIS](https://oeis.org/wiki/User:Philippe_Cochin), the "warp primes": primes whose balanced ternary representation, read backwards, is again a prime or a negated prime.

- [A323782](https://oeis.org/A323782) - primes that warp to a prime or a negated prime
- [A323783](https://oeis.org/A323783) - the corresponding warped values, a(n) = A134028(A323782(n))
- [A323784](https://oeis.org/A323784) - primes that warp to a composite
- Python code, b-files up to 10^6 and a D3 Ulam spiral of the two prime families: [WarpPrimes](https://github.com/sneakyweasel/WarpPrimes)

## 🧮 Older toys

- [padic-rust](https://github.com/sneakyweasel/padic-rust) and [padic-ts](https://github.com/sneakyweasel/padic-ts) - p-adic number libraries in Rust and TypeScript
- [Euler](https://github.com/sneakyweasel/Euler) and [DNA](https://github.com/sneakyweasel/DNA) - my Project Euler and Rosalind archives
