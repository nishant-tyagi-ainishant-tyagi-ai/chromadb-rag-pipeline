# ChromaDB RAG Pipeline

## About This Project

This is my first Retrieval-Augmented Generation (RAG) project built while learning LangChain and Vector Databases.

Instead of only watching tutorials, I implemented the complete workflow myself, fixed multiple package/import issues, and pushed the final working project to GitHub.

The goal was to understand how documents move through a RAG pipeline before being used by an LLM.

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
* Context chunking strategy for RAG systems

---

### Phase 2: Vector Database Pipeline

I created sample AI-related documents and built a complete vector search workflow.

Sample topics included:

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

Model:

sentence-transformers/all-MiniLM-L6-v2

#### Results

* Generated 384-dimensional vector embeddings
* Converted text into semantic vector representations
* Stored vectors inside ChromaDB

---

## Similarity Search

After storing embeddings in ChromaDB, I tested semantic retrieval using queries such as:

"What is machine learning?"

The vector database successfully returned the most relevant document chunks based on semantic similarity instead of keyword matching.

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

## Personal Note

This is the first RAG project I completed end-to-end.

While building it, I learned how documents are transformed into chunks, converted into embeddings, stored in a vector database, and retrieved through similarity search.

More importantly, I spent time understanding the workflow, debugging dependency issues, and making the complete pipeline run successfully rather than simply executing pre-written code.
