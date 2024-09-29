# 📚 **AttentionPlease: Dive into Transformers & Attention**

Welcome to **AttentionPlease**! This repository is dedicated to helping you understand the core concepts behind *attention mechanisms* and *transformer models*, the building blocks of modern natural language processing (NLP) systems like ChatGPT.

## 🚀 What is a Transformer?

The **Transformer** is a groundbreaking neural network architecture introduced in the paper ["Attention is All You Need"](https://arxiv.org/abs/1706.03762) by Vaswani et al. in 2017. Unlike previous models that processed data sequentially, the Transformer processes data in parallel, making it highly efficient for tasks like translation, text generation, and question-answering. It’s used extensively in state-of-the-art NLP models, including GPT (Generative Pre-trained Transformers).

### Key Components of a Transformer:
1. **Encoder-Decoder Structure**: Transformers consist of two main parts—an encoder and a decoder.
   - The **encoder** processes the input sequence and converts it into a hidden representation.
   - The **decoder** takes this hidden representation and generates an output sequence (e.g., translated text, predicted tokens).

2. **Multi-Head Attention**: This is the heart of the transformer. It allows the model to focus on different parts of the input sequence simultaneously, understanding context at multiple scales. Each “head” focuses on different aspects of the input.

3. **Positional Encoding**: Since transformers process all tokens simultaneously (in parallel), positional encodings are added to give the model information about the order of tokens in the input sequence.

4. **Feedforward Layers**: After attention, the transformer uses fully connected layers to process the information and pass it through non-linearities, adding depth and complexity to the model’s understanding.

### Transformer Workflow:
1. The input sequence (e.g., a sentence) is first tokenized into smaller units (tokens).
2. Positional encodings are added to the tokens to indicate their position in the sequence.
3. The sequence is fed into the multi-head attention layers, which allow the model to focus on relevant parts of the input.
4. The processed information is passed through feedforward layers.
5. The decoder generates the final output (such as a translated sentence or next token in a sequence).

---

## 🎯 What is Attention?

**Attention** is a mechanism that helps the model decide which parts of the input are most important for generating an output. Instead of processing every word or token with the same weight, the model learns to focus on specific parts of the input depending on the task at hand.

In simpler terms, **attention** allows the model to "pay attention" to different words in the sentence based on their relevance. For instance, when translating a sentence, certain words in the source language might correspond closely to specific words in the target language, and attention helps the model learn those relationships.

### Types of Attention in Transformers:
- **Self-Attention**: The model pays attention to different parts of the same input sequence. For example, in a sentence like "The cat sat on the mat," the word "cat" has a stronger connection to "sat" than to "mat."
- **Cross-Attention**: In the decoder, the model pays attention to the encoder's outputs while generating new tokens.

### Attention Formula:
Attention calculates a weighted sum of the input values, where the weights are determined by how much "attention" each word should get based on a query-key-value mechanism:
- **Query**: What the model is looking for.
- **Key**: What the model compares against.
- **Value**: The information being retrieved based on the attention weights.

The formula for attention is:

