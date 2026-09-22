---
layout: post
title:  "From silicon to language: how does metal think?"
date:   2023-11-24 16:13:05 +0200
categories: AI
ref: metal
excerpt: "Talk notes: from the transistor to the LLM in three steps, the automaton, the neural network, the language model, with the links to redo everything yourself."
---

- In the manner of St Thomas's *Summa contra Gentiles*, we will start from shared rational foundations to build a "thinking" logical automaton.
- I will try to demystify how LLMs (Large Language Models) work by having you relive the intellectual adventure that leads from matter to AI.
  - First we will build a computer.
  - Then we will see how an artificial neural network works.
  - Finally we will see how an LLM works.

## I - The computing automaton

### Fundamental logic

Logic is the science of the principles of valid reasoning. It is fundamental to philosophy, mathematics and computer science, and it rests on the principle of non-contradiction.
The NAND gate is a universal gate: every other logic gate can be built by combining it.

- Aristotle - Organon: <https://en.wikipedia.org/wiki/Aristotle#Logic>
- Propositional calculus: <https://en.wikipedia.org/wiki/Propositional_calculus>
- Boolean algebra: <https://en.wikipedia.org/wiki/Boolean_algebra>
- Logic gate: <https://en.wikipedia.org/wiki/Logic_gate>
- Universal gate (NAND): <https://en.wikipedia.org/wiki/NAND_gate>

### Imagining the automaton

In theoretical computer science, a Turing machine is an abstract model of how mechanical computing devices, such as a computer, work.

- Turing machine: <https://en.wikipedia.org/wiki/Turing_machine>
- Turing Complete: <https://www.youtube.com/watch?v=-YY73ejihZo>
- Nand to Tetris: <https://www.nand2tetris.org/>
- nandgame solutions: <https://github.com/Elidevin/nandgame.com-solutions/blob/master/Hardware.md>

> NANDGAME: <https://www.nandgame.com/>

### Building the automaton

The discovery of P-N junctions makes it possible to build tiny silicon transistors. These transistors can be assembled into integrated circuits, from which a computer can be built.

- Silicon: <https://en.wikipedia.org/wiki/Silicon>
- P-N junction (PMOS, NMOS): <https://en.wikipedia.org/wiki/P%E2%80%93n_junction>
- CMOS: <https://en.wikipedia.org/wiki/CMOS#Example:_NAND_gate_in_physical_layout>
- Semiconductor: <https://en.wikipedia.org/wiki/Semiconductor>
- Transistor: <https://en.wikipedia.org/wiki/Transistor>
- Integrated circuit: <https://en.wikipedia.org/wiki/Integrated_circuit>
- 8-bit computer: <https://eater.net/8bit>

> Minecraft CPU: <https://youtu.be/TxatLwlj0lU?si=aYUfTmiCIc7kXt56&t=34>

### Controlling the automaton

We now have to control our automaton and make it compute. We create languages with ever higher and ever more elegant levels of abstraction.
We gain a new kind of relationship to language: execution, on top of reading and writing.

- Programming language: <https://en.wikipedia.org/wiki/Programming_language>
- Assembly language: <https://en.wikipedia.org/wiki/Assembly_language>
- Lambda calculus: <https://en.wikipedia.org/wiki/Lambda_calculus>
- Rust: <https://en.wikipedia.org/wiki/Rust_(programming_language)>
- High-level language: <https://en.wikipedia.org/wiki/High-level_programming_language>
- Python: <https://en.wikipedia.org/wiki/Python_(programming_language)>
- NANDGAME (software part): <https://www.nandgame.com/>

### Speeding up the automaton

After a while, transistor miniaturisation and clock frequency hit physical limits. Other ways of increasing computing power are needed: duplicate and parallelise, spreading the workload over many cores.

- Moore's law: <https://en.wikipedia.org/wiki/Moore%27s_law>
- Tunnel effect: <https://en.wikipedia.org/wiki/Quantum_tunnelling>
- Parallel computing: <https://en.wikipedia.org/wiki/Parallel_computing>
- GPU: <https://en.wikipedia.org/wiki/Graphics_processing_unit>
- Nvidia: <https://en.wikipedia.org/wiki/Nvidia>
- CUDA, the GPU programming language: <https://en.wikipedia.org/wiki/CUDA>

## II - Grasping an uncertain world

### Neural networks and machine vision (ANNs)

Our machine is deterministic, fast and precise, but it does not like uncertainty, ambiguity or approximation.
So we look at how the human brain manages to grasp the uncertain world around us with its networks of neurons, and take inspiration from nature to create artificial neural networks.
(Human vision is said to be 576 megapixels, and the human brain holds 86 billion neurons. The near-instant processing of visual information is fascinating.)

- ANN: <https://en.wikipedia.org/wiki/Artificial_neural_network>
- Perceptron: <https://en.wikipedia.org/wiki/Perceptron>
- Linear algebra: <https://en.wikipedia.org/wiki/Linear_algebra>
- Tensor: <https://en.wikipedia.org/wiki/Tensor>
- PyTorch machine learning framework: <https://pytorch.org/>
- Deep learning visualisations: <https://distill.pub/>
- 3B1B video series on ANNs: <https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi>
- 3B1B lessons: <https://www.3blue1brown.com/lessons/neural-networks>
- Coursera Deep Learning Specialization: <https://www.coursera.org/learn/neural-networks-deep-learning/home/welcome>
- Backprop: <https://youtu.be/Ilg3gGewQ5U?si=4FssMbXM6CRK5rmQ&t=261>

> 3B1B perceptron recap: <https://youtu.be/IHZwWFHWa-w?si=LE5qWstbH01bqKZO&t=29>

### Large Language Models (LLMs)

One theory of the emergence of human faculties is the diversion of part of our visual computing power towards meta-cognition and abstract concepts.
LLMs are neural networks trained on very large corpora of text. They can generate text from a prompt.

- Deep learning: <https://en.wikipedia.org/wiki/Deep_learning>
- Transformer: <https://en.wikipedia.org/wiki/Transformer_(deep_learning_architecture)>
- Attention is all you need: <https://arxiv.org/abs/1706.03762>
- NanoGPT: <https://github.com/karpathy/nanoGPT>
- LLMs: <https://en.wikipedia.org/wiki/Large_language_model>
- LLM course: <https://www.coursera.org/learn/generative-ai-with-llms/home/week/1>

> NanoLLM visualisation: <https://bbycroft.net/llm>

Here is an example of GPT-4 used to create a Catholic chatbot which, enriched with the *Catechism of the Catholic Church*, answers users' questions.

### Pre-training corpus

Give the model a corpus of text large and varied enough for it to learn the structure of language.
Redundant data and biases must be avoided, markup cleaned, and so on.

- Common Crawl, the primary training corpus of every LLM: 82% of the raw tokens used to train GPT-3.
- Common Crawl (98.38 TiB): <https://commoncrawl.org/>
- The Pile (825 GiB): <https://pile.eleuther.ai/>
- Wikipedia dumps: <https://dumps.wikimedia.org/>
- Wiki dump preprocessing: <https://towardsdatascience.com/pre-processing-a-wikipedia-dump-for-nlp-model-training-a-write-up-3b9176fdf67>
- OSCAR: <https://oscar-project.github.io/documentation/versions/oscar-2301/>

### Domain corpus

- A corpus for adapting to a particular domain and its jargon: medical, legal, financial, and so on.

### Tokenisation

Converting a text into a sequence of tokens (words, characters, sub-words, and so on) that the model will use.

- Tokenisation: <https://en.wikipedia.org/wiki/Lexical_analysis>
- Byte Pair Encoding: <https://en.wikipedia.org/wiki/Byte_pair_encoding>

### Choosing the type of LLM

Different architectures suit different tasks:

- "Auto-encoding", RoBERTa: fill-in-the-blank, sentiment analysis, NER, and so on
- "Auto-regressive", GPT: text generation
- "Sequence-to-sequence", BART: translation, summarisation, and so on

### Fine-tuning

The model's weights are changed to fit a particular task by giving it examples of the task and the expected answers.
The model can be split into parts, fine-tuning one part and freezing the weights of the rest (PEFT).
INSTRUCT mode answers the instructions the user gives.

- Fine-tuning: <https://en.wikipedia.org/wiki/Fine-tuning_(deep_learning)>
- Domain adaptation: <https://en.wikipedia.org/wiki/Domain_adaptation>
- Catastrophic forgetting: <https://en.wikipedia.org/wiki/Catastrophic_interference>
- Human Q&A set: <https://huggingface.co/datasets/knkarthick/dialogsum/viewer/knkarthick--dialogsum>
- PEFT: <https://huggingface.co/docs/peft/index>
- LoRA: <https://huggingface.co/docs/peft/conceptual_guides/lora>
- Prompt-tuning: <https://research.ibm.com/blog/what-is-ai-prompt-tuning>

### Benchmarks and evaluation metrics

The similarity between the generated text and the expected human text is measured with matching metrics such as BLEU or ROUGE.
Other tests are more general, such as MMLU.

- BLEU: <https://en.wikipedia.org/wiki/BLEU>
- ROUGE: <https://en.wikipedia.org/wiki/ROUGE_(metric)>
- MMLU: <https://en.wikipedia.org/wiki/MMLU>

### Reinforcement from human feedback (RLHF)

An LLM must follow the three H's: Helpful, Honest and Harmless.
Several answers are generated, a human is asked to rank them, and the model is fine-tuned against that feedback.
An LLM that is too "helpful" can be manipulated by a user into malicious activities.

- PPO: <https://en.wikipedia.org/wiki/Proximal_Policy_Optimization>

### Deployment

Compressing, optimising and deploying the model on a server so that it can answer users.

### Orchestration library

Lets the LLM talk to the other components of the system, query data, and so on.

- LangChain: <https://www.langchain.com/>

### Retrieval-Augmented Generation (RAG)

Adds further data sources to enrich the model's answers, through database queries, search-engine lookups, semantic search, API calls, and so on.
Vector similarity search (embedding vectors) finds texts similar to the query, which can be folded into the model's answer.

- RAG: <https://arxiv.org/abs/2104.05544>
- Vector database: <https://www.pinecone.io/>
- Vector PostgreSQL: <https://github.com/pgvector/pgvector>
- Embedding vectors: <https://en.wikipedia.org/wiki/Word_embedding>

> Bias in vectors: <https://wikipedia2vec.github.io/demo/>

### Program-aided language (PAL) models & ReAct

The model is given the ability to generate computer code that carries out complex tasks.
A complex calculation, for instance, is beyond an LLM, whereas it can write a simple program that solves it.
The model is given only a general task and plans the sub-tasks and agents needed to get there.

- AutoLLM: <https://github.com/fcakyon/autollm>
- ReAct: <https://arxiv.org/abs/2210.03629>
- LangChain: <https://www.langchain.com/>

### Prompt engineering

Depending on the model, we have a limited space in which to instruct it: the context window.
That window is where we put:

- the definition of the model's "personality" and orientation
- the instructions for the task
- the data from retrieval-augmented generation
- the user's question
- the conversation history with the user (0-shot, few-shot, and so on)

- Pre-prompt: <https://en.wikipedia.org/wiki/Prompt_engineering>
- Prompt engineering course: <https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/>

### UI/UX

The user interface is essential for humans to be able to use the model.
It is usually close to an instant-messaging interface with conversation bubbles.
It also includes user management, message history, and so on.

- User interface: <https://en.wikipedia.org/wiki/User_interface>
- UX: <https://en.wikipedia.org/wiki/User_experience>

## III - Case study

Demonstration of GPT-4 used to create a Catholic chatbot which, enriched with the *Catechism of the Catholic Church*, answers users' questions.
