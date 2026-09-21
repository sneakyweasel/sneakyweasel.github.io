---
layout: page
title: Math
permalink: /math/
---

I like number representations that make structure visible. Balanced ternary, where every integer is one unique word over the digits `-`, `0`, `+`, is my favourite, and most of my mathematical work since 2019 grows out of it.

Feel free to [contact me](mailto:philippe@cochin.fr)!

My publications are listed on ORCID: [0009-0004-1939-3382](https://orcid.org/0009-0004-1939-3382).

## 🔢 OEIS sequences

In January 2019 I contributed three sequences to the [OEIS](https://oeis.org/wiki/User:Philippe_Cochin), the "warp primes": primes whose balanced ternary representation, read backwards, is again a prime or a negated prime.

- [A323782](https://oeis.org/A323782) - primes that warp to a prime or a negated prime
- [A323783](https://oeis.org/A323783) - the corresponding warped values, a(n) = A134028(A323782(n))
- [A323784](https://oeis.org/A323784) - primes that warp to a composite
- Python code, b-files up to 10^6 and a D3 Ulam spiral of the two prime families: [WarpPrimes](https://github.com/sneakyweasel/WarpPrimes)

## 🧪 Balanced Ternary Mathematical Laboratory

[btlab](https://github.com/sneakyweasel/btlab) is an exact-arithmetic research platform (Python, MIT licence). Its core is balanced ternary: encoding, arithmetic, operators, a trit calculus, polynomials, automata and transducers. Open problems are attached as independent modules that import the core and never the reverse.

- Every claim carries its evidence class: human proof, Lean-verified, computationally verified, conjecture, observation, or refuted. Finite checks are never presented as proofs.
- Each research direction runs explore, distill, prove or refute, decide, under a written budget, and ends in exactly one decision: promote, park or close. Closed branches stay documented so nobody rediscovers them.
- The formal layer is [Lean 4 with Mathlib](https://github.com/sneakyweasel/btlab/tree/main/formal), with no `sorry`.

## 🤹 The Juggler map

The active application is the Juggler map ([A094683](https://oeis.org/A094683)): T(n) = ⌊√n⌋ when n is even and ⌊n√n⌋ when n is odd. Whether every orbit reaches 1 is open, as it is for Collatz. Three preprints, September 2026, on Zenodo under CC BY 4.0:

- [Lower Bounds for Cycle Lengths in the Juggler Map](https://doi.org/10.5281/zenodo.22676452) - a cycle-financing inequality, n log n (3^o - 2^L) <= L 3^o for a cycle of length L with o odd steps, refined through an irrational rotation and Denjoy-Koksma estimates, yields period lower bounds for hypothetical nontrivial cycles at each verified descent floor.
- [Fate Contagion and Termination Criteria for the Juggler Map](https://doi.org/10.5281/zenodo.22678164) - every set closed under preimages, so every cycle basin and the set of unbounded orbits if any, has logarithmic mass at least c (log x)^lambda for every lambda below about 0.4927; the second proof is formalized in Lean 4 inside btlab for every lambda <= 100/203.
- [Five-Step Descent Certificates for the Juggler Map: Parity Statistics of Nested Floor Powers](https://doi.org/10.5281/zenodo.22864933) - the starting values that admit a power-envelope descent certificate within five operations have natural density 7/8 (13/16 for four), by exact carry identities, centered Fourier expansions and van der Corput differencing.

None of this claims a solution of the Juggler or Collatz problems. There is an [interactive companion](https://balanced-ternary-beta.vercel.app) to explore the orbits.

## 🔁 The 3n−1 map

The 3n−1 map (g(y) = y/2 for even y and (3y−1)/2 for odd y) is the shortcut 3n+1 map read on the negative integers. Its known cycles are 1, (5, 7, 10) and the eleven-element cycle at 17, and every start below 2^51 reaches one of them. One preprint, September 2026, on Zenodo under CC BY 4.0:

- [No m-cycles of the 3n−1 map for m ≤ 58](https://doi.org/10.5281/zenodo.22876189) - the Simons–de Weger template for 3n+1 m-cycles, transposed to this map with its constants derived on this side and combined with the bound of Rhin on linear forms in logarithms: no m-cycle with 1 ≤ m ≤ 58 other than the two known ones. The statement is new for 3 ≤ m ≤ 58; for m ≤ 2 it is a floor-dependent form of a theorem of Simons.

## 🧮 Older toys

- [padic-rust](https://github.com/sneakyweasel/padic-rust) and [padic-ts](https://github.com/sneakyweasel/padic-ts) - p-adic number libraries in Rust and TypeScript
- [Euler](https://github.com/sneakyweasel/Euler) and [DNA](https://github.com/sneakyweasel/DNA) - my Project Euler and Rosalind archives
