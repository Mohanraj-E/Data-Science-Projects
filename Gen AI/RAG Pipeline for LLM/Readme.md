# 🧠 Retrieval-Augmented Generation (RAG) Pipeline Demo

This project demonstrates how to build a **Retrieval-Augmented Generation (RAG)** pipeline from scratch using Python and Hugging Face Transformers — with Wikipedia as a sample knowledge base.

⚠️ **Goal:**  
The focus is **not on Wikipedia QA**, but on understanding how to integrate the **key components of a RAG pipeline**, which can be extended to other domains (e.g., finance, healthcare, legal documents).

---

## 📌 What is RAG?

**RAG (Retrieval-Augmented Generation)** is a hybrid NLP approach that combines:

- **Retrieval:** Finds relevant documents/passages from a large corpus using semantic search.
- **Generation or Extraction:** Uses a language model to generate or extract an answer based on the retrieved content.

---

## 🚀 How the Pipeline Works

### 🔷 1. Content Retrieval
- Fetches content from Wikipedia using a user-defined topic.

### 🔷 2. Text Chunking
- Splits long documents into overlapping text chunks using a tokenizer.

### 🔷 3. Embedding Generation
- Converts each chunk into dense vector embeddings using `sentence-transformers`.

### 🔷 4. Indexing with FAISS
- Builds a fast similarity index (`FAISS`) from the embeddings for efficient search.

### 🔷 5. Query Handling
- Accepts a user question and converts it into an embedding.

### 🔷 6. Semantic Retrieval
- Searches the FAISS index to get top-k most relevant chunks.

### 🔷 7. Question Answering
- Feeds the question and relevant context to a pre-trained QA model (`deepset/roberta-base-squad2`) to extract the answer.

---

## 🛠️ Tech Stack

- **Python**
- [Wikipedia API](https://pypi.org/project/wikipedia/)
- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [Sentence Transformers](https://www.sbert.net/)
- [FAISS (Facebook AI Similarity Search)](https://github.com/facebookresearch/faiss)

---

## 🧪 Example Usage

```bash
$ python rag_pipeline.py

Enter a topic to learn about: Artificial Intelligence
[INFO] Text split into 48 chunks.
Ask a question about the topic: Who invented AI?

Answer: John McCarthy

