# ChromaDB RAG Pipeline

## About This Project

This is my first Retrieval-Augmented Generation (RAG) project built while learning LangChain, Vector Databases, and the fundamentals of modern LLM applications.

The objective of this project was to understand how documents are ingested, chunked, converted into embeddings, stored in a vector database, and retrieved through semantic search before being provided as context to an LLM.

During development, I also worked through package compatibility issues, environment setup challenges, and LangChain dependency management to build a complete end-to-end pipeline.

---

## What I Built

### Phase 1: PDF Processing

I loaded a PDF document using LangChain's PyPDFLoader and prepared it for retrieval.

#### Results

* Loaded 4 pages from PDF
* Split 4 pages into 6 chunks
* Chunk Size = 500
* Chunk Overlap = 50

#### Skills Learned

* PDF ingestion using PyPDFLoader
* LangChain Document objects
* RecursiveCharacterTextSplitter
* Context chunking strategies used in RAG systems

---

### Phase 2: Vector Database Pipeline

I created sample AI-related documents and built a complete vector search workflow.

#### Sample Topics

* Machine Learning Fundamentals
* Deep Learning & Neural Networks
* Natural Language Processing

#### Workflow

Documents

↓

DirectoryLoader

↓

Document Chunks

↓

HuggingFace Embeddings

↓

ChromaDB

↓

Similarity Search

---

## Embedding Model Used

**Model:** `sentence-transformers/all-MiniLM-L6-v2`

#### Results

* Generated 384-dimensional vector embeddings
* Converted text into semantic vector representations
* Stored embeddings inside ChromaDB
* Performed semantic similarity search

---

## Similarity Search

After storing embeddings in ChromaDB, I tested semantic retrieval using queries such as:

> "What is machine learning?"

The vector database successfully retrieved the most relevant document chunks based on semantic similarity rather than exact keyword matching.

---

## Technologies Used

* Python
* LangChain
* ChromaDB
* HuggingFace Embeddings
* Sentence Transformers
* PyPDFLoader
* RecursiveCharacterTextSplitter
* Git
* GitHub

---

## Key Concepts Learned

* Document Loading
* PDF Ingestion
* Document Chunking
* Embeddings
* Vector Databases
* ChromaDB
* Semantic Search
* Similarity Retrieval
* Basic RAG Architecture

---

## Challenges Faced

While building this project, I encountered multiple dependency and import issues related to LangChain packages, HuggingFace integrations, and environment configuration. Resolving these issues helped me better understand Python environments, package management, and the LangChain ecosystem.

---

## Personal Note

This is the first RAG project I completed end-to-end.

Building it helped me understand how documents move through a retrieval pipeline: from ingestion and chunking to embedding generation, vector storage, and semantic retrieval.

More importantly, I focused on understanding each stage of the workflow and troubleshooting issues during implementation rather than simply executing pre-written code.
