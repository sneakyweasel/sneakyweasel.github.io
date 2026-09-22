---
layout: post
title:  "Talk notes: generative AI and education"
date:   2024-01-05 16:13:05 +0200
categories: AI
ref: education
excerpt: "Talk notes: what learning means for a machine, from the perceptron to generative AI, for teachers."
---

## Intro

We use the terms machine learning and deep learning a lot, and tend to forget that learning is first of all a natural biological process, used by almost every living thing. (video: a fox cub playing)
Biologically, learning shows up as the strengthening of synaptic connections in the brain. (image: a synapse)
When we talk about machine learning we mean a mathematical process inspired by that biological process, which we will now describe.

## Artificial neural networks

### The difficulty with classical computing

- Classical computing is based on logical instructions executed by a processor. These instructions are executed sequentially and are deterministic: run the same program twice on the same input and you always get the same output.
- This works very well for precise, well-defined tasks, such as adding two numbers or sorting a list of numbers.
- The world, however, is fuzzy, imprecise and uncertain, and humans have evolved to fit it. We can make decisions in uncertain situations, adapt to new ones, extrapolate missing information and decide from past experience.

### Artificial neural networks

- By biomimicry, researchers have tried to reproduce this human faculty by creating artificial neural networks modelled on the human brain.
- An artificial neural network is a set of artificial neurons connected to one another. Each artificial neuron is a mathematical function that takes a vector of numbers as input and returns a number. (image: ANN)

### Perceptron

- The perceptron is the simplest artificial neuron. It takes a vector of numbers as input and returns a number. (image: perceptron)

### Supervised learning

- We quickly follow the path of the information through the perceptron. (video: 3b1b)
- We start with random weights and feed input data through the perceptron. We compare the perceptron's output with the expected output and adjust the weights so that the output moves closer to what was expected. (video: 3b1b)
- We repeat this process millions of times with different data, and at the end we have a perceptron able to predict the expected output from the input. (gradient descent)

### Querying the model

- The model can now be queried by giving it an input and asking it to predict the output. This is called inference.

### Vocabulary

- LLMs: Large Language Models
- AI: Artificial "Intelligence"
- Embedding: a vector of numbers that represents a word in a vector space.
- Weight: the strength of the connection between two neurons in the network. The heart of the neural network.
- Pre-prompt: text that sets the context and the tone of the answer.
- Prompt: the user's question, sent to the model to guide its text generation.

## Generative AI

### LLMs (ChatGPT, GPT-4, Llama 2, etc.)

- Several innovations made generative AI possible: the transformer as a mathematical model, and the sharp rise in parallel computing power.
- Language is a sequential structure in which the position of words matters. (image: text)
- LLMs are language models able to generate text from an input text. (image: LLM)
- They are next-word prediction algorithms. (image: LLM)

### Image generation

- Generative AI is not limited to text. Images can be generated too. (image: GAN)
- Dall-E demo: <https://openai.com/blog/dall-e/>
- Demo: <https://thispersondoesnotexist.com/>

### Code generation

- Demo: <https://github.com/features/copilot>
- Recursion: AIs that code themselves (AutoGPT).
