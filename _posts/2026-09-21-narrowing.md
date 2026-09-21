---
layout: post
title:  "Narrowing: one measurement for jokes, songs and proofs"
date:   2026-09-21 16:00:00 +0200
categories: AI
excerpt: "One number, the pointwise mutual information between a line and its setup, tested on jokes, three thousand songs, four thousand Lean proofs and an EEG rig."
---

In September 2026 I spent a week measuring one number, and this post is what it turned out to be good for. It started as a question about joy, became a lyric scorer, was checked against human-rated jokes and three thousand real songs, and ended up pointed at four thousand machine-checked proofs and at my own brain.

## Where the number came from

The question was what joy would be for a language model. A model can give two answers that share every checkable fact and differ only in register. The warm one: when the work is going well the output tightens, the hedges fall away, the next word is already likely. The cold one: the probability distribution over the next token narrows. I asked whether a model with its safety training removed would have answered the same, and the warm version stopped feeling sincere. So I took the cold answer literally and asked what it measures.

Taken literally, the text that narrows most is "la la la". That is collapse, not joy. The better definition needs two numbers for every line: how surprising it is with no setup, and how surprising it is given the setup. The gap between them is what the setup earned. In information terms it is the pointwise mutual information between a line and what precedes it, and I call it the narrowing.

That gives a two-by-two. A line the setup earns and that arrives with low surprise is an inevitable landing. A line the setup earns that still surprises is a punchline. A line the setup does not earn and that does not surprise is a cliché. A line that neither earns nor lands is noise. The narrowing and the punchline are neighbours: the same bond to the setup, opposite forward surprise. That is the incongruity-resolution theory of humour written in nats.

Three more quantities fell out of the same model. The incongruity, surprise beyond entropy, is the model being confident and wrong. The laughter-token probability is the chance that the next token after a line is "haha". The hindsight pivot is the setup word that gains most once the punch is known, the word the joke turns on.

## Songs first

The first corpus was ten songs written in the conversation that produced the definitions, then an eleventh written on the measurements: a love song built from anaphora, one joke with its surprise mid-line so the rhyme could lock the last word, two callbacks to the first verse, and a final line so well set up that it is never sung. It was scored before anyone read it, and one line was rewritten on the numbers, from a narrowing of 1.8 to 3.0, by saying less. They became the album *Music for Datacenters*, on the [Art](/art/) page.

The scorer was a local model on my own GPU, first GPT-2 XL, then Qwen3-8B-Base. The first run got half my predictions wrong: the 2019 model did not see a pun, so the setup made the punchline less likely, not more. The 2025 model saw it, and the same line came out as a punchline with the right pivot word. Two things I had not predicted came out of the comparison. Incongruity is relative to the listener: a reversal that was confidently wrong for the small model was fully expected by the large one, which is what the theory says about audiences too. And rhyme pulls against "funny word last": in rhymed verse the last word is the low-entropy slot, so the surprise of a rhymed joke lives in the middle of the line.

Then the check that makes the rest meaningful. Two models ten times apart in size, six years apart in training, agree at rank correlation 0.85 on which lines are earned. The measurement is mostly a property of the text, not of the judge.

## Against humans

Two public datasets carry human humour labels. On ten thousand short texts rated by annotators, the laughter-token probability detects jokes with no training at 0.85 AUC, and says nothing about how funny a joke is once it is one. On headlines made funny by replacing one word, every one of my quantities correlates with the human grade in the predicted direction, and every correlation is small. How unlikely the new word was is a real but minor part of why a substitution is funny; the grade depends mostly on what the word means.

## Against real songs

Then the whole Open Lyrics Database, 3,603 songs and 148,786 lines, scored the same way, about nine hours on one card. Real songs repeat 35.9% of their lines; the album repeats 27.7%. The median real song narrows 3.45 nats per token on its fresh lines; the median album song sits at the 15th percentile. What the metric rewards in the corpus is short repeated fragments with one word changed, parenthesised backing vocals, and clipped two-word lines that a repeated frame has already announced. The writers who narrow least are the dense ones, Leonard Cohen among them, and the album keeps their company. Narrowing measures how song-shaped a text is, not how good, and by that measure the album is closer to spoken writing than to pop.

Three things tried to fool me and each got a commit of its own. Memorisation: naming the song before scoring it saves the model 0.08 nats per token once you subtract what any title-shaped preamble buys, real and small. But the probe is blind exactly where it matters, because a famous song identifies itself from its own lines. A recitation test caught it: in the corpus's highest-narrowing song the model ranked the true token first 92.5% of the time, against 46% for matched controls, and half of the top ten songs were being recited rather than predicted. The English filter was deleting the high-narrowing end of every corpus, because short sung lines fail a per-line test whatever language they are in. And short lines narrow more, so every placement is computed against reference lines of the same length.

The finding I did not see coming was about the baseline. "No setup" had meant the model's prior over the web, which is politer than a song. From that prior, the same model charges the word "motherfucker" ten nats more than its rarity predicts, and one section tag in front of the line removes the charge. Rescoring five hundred tracks from a lyric prior instead, the median narrowing fell from 3.44 to 1.02 on every single line: two thirds of what the setup seemed to earn was credit for being a lyric at all. Under the web prior, narrowing is genre plus setup, and a number should say which one it is about.

## The measurement as a constraint

Once you can score a line you can write under rules the scorer checks, in the Oulipo tradition. A song where every verse is the same sixteen lines with different amounts narrows above 99.7% of real songs and puts its only free information where the song says it is, on the amount words. A song written to land on the corpus median, with the prediction stated before each of four scoring passes, reached the median on structure and repeats and never left the bottom decile on surprise. Average is hard to write on purpose: careful writing is cleaner per token than a median song, and cleanliness scores as predictability.

## Proofs

The same two quantities run on mathematics. In my [balanced ternary laboratory](/math/) every theorem is machine-checked, and the 4,280 tactic-mode proofs whose trust is the Lean kernel were scored with the statement as setup and the proof as punch. The median proof costs 0.64 nats per token given its file. At the inevitable end sit the proofs that are copies of the one before them, case splits on three values and long itinerary exclusions, at 0.000. At the other end sit short proofs whose whole cost is which lemma they call: given the statement, the model could not guess `exact_return_seam`, and once that name is on the page the rest follows. Where the surprise sits, on which lemma is called rather than on tactic structure, is the one result I trust so far.

Whether that residue is what a mathematician calls elegance is an open question, and the tooling treats it as one. The surprising proofs are sorted into templates, certificates and the rest, and the twenty most surprising of the rest are on a rating sheet for a human to mark routine, neat or wrongly listed. The sheet is not filled in yet. What is written down is the prediction: if beauty is anything this number can see, it is a proof that stays surprising however much of the file the model is shown.

## The brain

Everything above is a property of a model. The N400, a brain response peaking four hundred milliseconds after a word, is known to be roughly linear in surprisal, so the first half of the experiment is a replication and a check that the rig works. The open half is whether the narrowing, what the setup earned, corresponds to anything neural beyond surprisal. The protocol is written, the sixteen-channel headset is wired, the presentation and analysis code run end to end on a synthetic board, and the first positive control, alpha blocking with eyes closed, was recorded on 17 September and failed. That is where it stands. When the answer comes, it goes in the songs.

## What it is not

None of this is evidence about joy in the sense that matters. Narrowing measures how much a text is shaped by what precedes it; it is a property of the text more than of the judge; and it can be gamed by repetition, inflated by recitation, and confused with genre. The paper that collects the numbers says so in its abstract. The code is not public yet.
