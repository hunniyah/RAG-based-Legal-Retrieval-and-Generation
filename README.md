---

# ⚖️ LexiFind — Legal Retrieval and Explanation System for Pakistan

LexiFind is a **Retrieval-Augmented Generation (RAG)** system designed to make Pakistan’s legal knowledge more accessible.
The system retrieves relevant legal text from a curated knowledge base and generates **simplified, contextual explanations** for user queries.

It bridges the gap between **complex legal language** and **public accessibility**, enabling both professionals and non-experts to understand legal provisions more easily.

---

# 🎯 Motivation

Legal information in Pakistan suffers from several challenges:

*  **Accessibility barriers** for the general public
*  **Fragmented and non-centralized legal resources**
*  **Complex legal language** rooted in historical and cultural contexts

This project aims to create a system that can:

1. Retrieve relevant legal documents
2. Provide simplified explanations
3. Maintain contextual grounding in the original legal text

---

# 🧠 System Overview

LexiFind follows a **Retrieval-Augmented Generation (RAG) architecture**.

```
User Query
     │
     ▼
Query Embedding
     │
     ▼
Semantic Retrieval from Legal Knowledge Base
     │
     ▼
Context + Query
     │
     ▼
LLM Response Generation
     │
     ▼
Simplified Legal Explanation
```

The system ensures that generated responses remain **grounded in actual legal sources**.

---

# 🏗️ Core Components

## 1️⃣ Knowledge Base

A curated collection of legal documents including:

* Pakistan’s Constitution
* Statutory legal provisions

Documents are preprocessed and segmented into smaller chunks for efficient retrieval.

---

## 2️⃣ Preprocessing Pipeline

The preprocessing module prepares legal texts for semantic search:

* Text cleaning
* Document chunking
* Embedding generation
* Storage in a searchable vector index

This enables efficient semantic retrieval instead of simple keyword search.

---

## 3️⃣ Retrieval Module

The retrieval system identifies the **most relevant legal passages** for a user query using vector similarity search.

Steps:

1. Convert query into embeddings
2. Compare against indexed document embeddings
3. Retrieve top-k relevant legal sections

---

## 4️⃣ Generation Module

The generation module uses a **Large Language Model (LLM)** with prompt templates to:

* Interpret the retrieved legal context
* Produce simplified explanations
* Maintain grounding in the original legal text

This prevents hallucinations and improves reliability.

---

# 📊 Evaluation Strategy

To assess system quality, an **LLM-as-a-Judge framework** was used.

Three key metrics were evaluated:

### Relevance

How well the retrieved context matches the user query.

### Groundedness

Whether the answer can be supported by the retrieved legal context.

### Naturalness

How understandable and coherent the generated explanation is.

---

# 🛠 Tech Stack

* Python
* Vector Embeddings
* Retrieval-Augmented Generation (RAG)
* Large Language Models
* Prompt Engineering
* Custom preprocessing pipeline

---

# 📁 Repository Structure

```
lexifind-legal-rag/
├── app.py
├── .env
├── README.md
├── Presentation.pptx
│
├── data/
│   ├── 01_Embedding_Chunking.ipynb
│   ├── embedded_data.json
│   ├── faiss_index.index
│   ├── final_chunks.json
│   └── metadata_list.json
│
├── routes/
│   └── main_routes.py
│
├── services/
│   ├── glove.py
│   ├── legalbert.py
│   ├── models.py
│   ├── rag_pipeline.py
│   └── retrieval.py
│
├── static/
│   ├── indexstyle.css
│   ├── style.css
│   └── tent.css
│
└── templates/
    ├── chatbot.html
    └── index.html
```

---

# 👩‍💻 Team Contributions

**Hunniyah Jahangir**

* Legal document preprocessing
* Embedding generation
* Semantic retrieval system

**Talha Ahmed Siddiqui**

* RAG pipeline
* Response generation using LLMs

**Eraj Jamil**

* Frontend development
* System integration

---

# 🚀 Future Improvements

Planned extensions for the system include:

### 📂 User Document Upload

Allow users to search within their own legal documents.

### 📚 Expanded Knowledge Base

Include:

* Case law
* Judicial interpretations
* Constitutional amendments

### ⚡ Real-Time Updates

Automated ingestion of newly published legal material.

### 📈 Scalable Embedding Pipeline

Enable large-scale indexing for broader legal coverage.

---

# 💡 Potential Impact

LexiFind demonstrates how **AI-powered legal retrieval systems** can:

* Improve access to legal knowledge
* Reduce complexity of legal language
* Support legal professionals and citizens alike

The project highlights the potential of **domain-specific RAG systems** in specialized knowledge fields.

---

Environment variables in .env file need to set before running the application (use personal Huggingface and Groq API keys).

