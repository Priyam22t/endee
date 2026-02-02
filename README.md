# RAG-Based Document Question Answering using Endee

## Project Overview

This project demonstrates a **Retrieval-Augmented Generation (RAG)** style application built on top of **Endee**, a high-performance open-source vector database. The goal of the project is to showcase how Endee can be effectively used as the core vector search engine in real-world AI workflows such as semantic search and document-based question answering.

The application allows users to ingest textual documents, store their semantic embeddings, and retrieve the most relevant information in response to natural language queries.

---

## Problem Statement

Large Language Models (LLMs) often generate inaccurate or hallucinated responses when they lack access to domain-specific knowledge. Retrieval-Augmented Generation (RAG) solves this problem by retrieving relevant context from an external knowledge base before generating an answer.

This project addresses the problem by:
- Converting documents into vector embeddings
- Storing and retrieving those embeddings efficiently
- Using similarity search to fetch relevant context for user queries

---

## Use Case Demonstrated

- **Retrieval-Augmented Generation (RAG)**
- **Semantic Search**
- **Knowledge-based Question Answering**

This aligns directly with common production use cases such as:
- Internal knowledge assistants
- Chatbots
- Document QA systems

---

## System Architecture

The system follows a simple and effective RAG pipeline:

```
Documents
  |
Text Embeddings
  |
Endee (Vector Database)
  |
Similarity Search
  |
Retrieved Context
  |
Final Answer
```

---

## Technical Approach

### 1. Document Ingestion
- Input documents are read from a text file.
- Each document is converted into a dense vector embedding using a transformer-based embedding model.
- These embeddings capture the semantic meaning of the text.

### 2. Vector Storage with Endee
- Endee is used as the vector database to store document embeddings.
- It enables fast and efficient similarity search using vector distance metrics.
- Endee serves as the backbone of the retrieval layer.

### 3. Query Processing
- User queries are embedded using the same embedding model.
- A similarity search is performed against stored vectors in Endee.
- The most relevant document chunks are retrieved as context.

### 4. Answer Generation
- The retrieved context is used to produce an accurate and grounded response.
- This demonstrates the core idea behind Retrieval-Augmented Generation.

---

## How Endee is Used

Endee is used as the **central vector database** in this project. Its responsibilities include:
- Storing high-dimensional vector embeddings
- Performing efficient similarity search
- Enabling scalable retrieval for AI applications

The project is structured as an application **built on top of Endee**, without modifying Endee’s core implementation.

---

## Project Structure

```
ai_examples/rag_document_qa/
├── data/
│   └── documents.txt
├── src/
│   ├── ingest.py
│   └── query.py
├── requirements.txt
└── README.md
```

---

## Setup and Execution

### Prerequisites
- Python 3.9+
- Git
- Endee repository (this project lives inside a fork of Endee)

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Ingest Documents
```bash
python src/ingest.py
```

### Run Query
```bash
python src/query.py
```

---

## Output

- Documents are successfully embedded and stored.
- User queries return relevant context based on semantic similarity.
- The system produces grounded, context-aware answers.

---

## Why This Project

This project demonstrates:
- Practical usage of Endee as a vector database
- A real-world AI/ML application using vector search
- Clean system design and modular structure
- Alignment with production RAG architectures

---

## Conclusion

This project serves as a concise but complete example of how **Endee can be integrated into modern AI systems** that rely on vector search as a core component. It highlights Endee’s suitability for building scalable, retrieval-driven AI applications such as RAG-based assistants and semantic search systems.
