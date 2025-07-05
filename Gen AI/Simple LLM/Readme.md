# 🤖 Building a Simple Transformer-Based Language Model

This project demonstrates how to **build a simple transformer-based language model** from scratch using PyTorch. The model uses key transformer components like self-attention, positional encoding, and a feedforward network to learn language representations.

⚠️ **Goal:**  
The focus of this project is to build a language model that can predict the next word in a sequence based on the provided input text. This can be extended to larger datasets for real-world applications such as text generation, translation, or classification.

---

## 📌 What is a Transformer Model?

A **Transformer** is a deep learning architecture introduced in the paper "Attention is All You Need" that uses self-attention mechanisms to process sequences of data. Unlike previous models like RNNs or LSTMs, transformers can process the entire input sequence simultaneously, making them much faster and more efficient for large datasets.

---

## 🚀 How the Model Works

### 🔷 1. Tokenize the Text Data
- **Tokenization** converts the input text into numerical sequences by mapping each word to a unique index from the vocabulary.
- In this project, a simple vocabulary is created manually, where words are mapped to indices, and unknown words are mapped to a special token (`<UNK>`).

### 🔷 2. Create the Embedding Layer
- An **embedding layer** is used to convert tokenized input (word indices) into dense vectors of fixed size (embedding dimension). This helps the model learn the semantic meaning of words in a lower-dimensional space.

### 🔷 3. Apply Positional Encoding
- Since transformers don’t process data sequentially, **positional encoding** is added to the embeddings to provide information about the position of words in the sequence.
- This encoding allows the model to learn the order of words in the input text.

### 🔷 4. Self-Attention Mechanism
- The **self-attention** mechanism allows the model to weigh the importance of each word in the sequence relative to others. It helps the model focus on the most relevant parts of the input text when making predictions.

### 🔷 5. Transformer Block
- The transformer block consists of multiple layers of **self-attention** followed by **feedforward layers**. This block enables the model to learn hierarchical relationships in the data.
- Each transformer block also uses **layer normalization** to stabilize training.

### 🔷 6. Output Layer
- The final output layer is a **linear layer** that maps the transformed embeddings to the vocabulary size, producing a probability distribution over all possible next words.

### 🔷 7. Training the Model
- The model is trained using **cross-entropy loss**, which measures the difference between the predicted word distribution and the true target word.
- The **Adam optimizer** is used to update the model's weights during training.

### 🔷 8. Predicting the Next Word
- After training, the model can be used to predict the next word in a given sequence by selecting the word with the highest probability.

---

## 🛠️ Tech Stack

- **Python**
- [PyTorch](https://pytorch.org/)
- **Transformers**
- **NumPy**

---

## 🧪 Example Usage

### Step-by-Step Guide

1. **Install the Dependencies**

   To start using the model, make sure you have **PyTorch** installed in your environment:

   ```bash
   pip install torch

