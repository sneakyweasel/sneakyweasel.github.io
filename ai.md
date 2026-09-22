---
layout: page
title: AI
permalink: /ai/
ref: ai
---

I've worked on AI since 2016 and I build language-model systems for a living, currently as a freelancer. Through [Logicien](https://www.logicien.fr) I build custom AI for organisations that want to own it: their code and their infrastructure. What follows is what I actually do, with the repositories that show it.

Feel free to [contact me](mailto:philippe@cochin.fr)!

## 🛠 What I build

- **LLM systems in production**: retrieval-augmented generation over structured data, embeddings and vector search, tool use, evaluation, and the plumbing that keeps a model honest about its sources. Example corpus: the Catechism converted to a linked Markdown [retrieval base](https://github.com/sneakyweasel/open-catholic) for a GPT-4 assistant.
- **Agentic workflows**: I run research as a multi-agent operation. The [balanced ternary laboratory](https://github.com/sneakyweasel/btlab) is worked by several coding agents at once, under a written agent guide, custom skills, an MCP server for Lean, a theorem index the agents must query before touching a proof, and gates that refuse a manuscript whose numbers do not reproduce. Every branch ends in one recorded decision, and what failed is kept so nobody rediscovers it.
- **Local models on my own hardware**: an RTX 5090 running Qwen3-8B, GPT-2 XL, Whisper large-v3, FLUX and Wan through ComfyUI. I write the scoring, resumable batch and GPU-queue code around them; the next step is a small prover fine-tuned on the laboratory's own lemmas.
- **Generative media pipelines**: lyrics written in conversation, audio from Suno, every take heard back by Whisper and aligned to the lyrics before it can be mastered, covers rendered with FLUX under one visual rule, video loops with Wan, all gated by scripts that refuse to package a release with a missing field. The result is on the [Art](/art/) page.
- **Classical machine learning and deep learning**: GANs and deepfakes, object detection on a Raspberry Pi, LSTM forecasting, neurofeedback; and evolutionary methods, from a [genetic algorithm](https://github.com/sneakyweasel/genetic-quantum-correction) for quantum error correction that ended up cited in Phys. Rev. A to [embryology-inspired growth](https://github.com/sneakyweasel/genetic-growth) encoded as opcode DNA.

## 🔬 Research with models

- **Measuring what a model finds inevitable.** With a local model I score every line of a text for its surprise, its entropy, and how much the lines before it earned it, which sorts lines into inevitable, punchline, cliché and noise. The laughter-token probability detects jokes zero-shot at 0.85 AUC on human-rated datasets, two models ten times apart in size agree at rank correlation 0.85 on which lines are earned, and an album of my own was placed against 3,043 real songs on the same scale. The same probe runs over four thousand kernel-checked Lean proofs, where the surprise sits on which lemma is called. Predictions are written down before each run, and the failures are published with the rest.
- **AI-assisted formal mathematics.** Agents draft and repair Lean 4 proofs against Mathlib inside the laboratory, with axiom checks and no `sorry` allowed through; the theorem index keeps humans and agents from proving the same lemma twice. See [Math](/math/).
- **A brain in the loop.** The next step is an EEG protocol on my own OpenBCI rig, sixteen channels, to test whether the lines a model calls earned land differently in a human reader, using the N400 as the yardstick. The rig, the markers and the analysis are written; the answer is not in yet.
- **Quantum machine learning**, once, at MIT iQuHACK 2023: a quantum-walk search on IonQ hardware feeding transformers and Stable Diffusion, [Quintessence](https://github.com/sneakyweasel/quintessence).

## 🛡 Safety, ethics and the public conversation

- Prompt injection, jailbreaks and red-teaming, from the attacker's side and the defender's; AI safety as an engineering discipline rather than a slogan.
- Four years of philosophy and theology before a career in AI give me an unusual vantage point on what these systems are and are not. I've spoken on that at Sorbonne University, at high-level religious conferences and before an ethics council in Paris. Notes from some of those talks are among the [posts](/) on the home page.

## 📜 Certificates

- [Deep Learning Specialization](https://coursera.org/share/060c260c19a2007f337dfae390fe4382) and [Generative AI with Large Language Models](https://coursera.org/share/e39f9086732f131d4d6b0fef988d9d82), both by Andrew Ng. The full list is on the [Certifications](/certifications/) page.
