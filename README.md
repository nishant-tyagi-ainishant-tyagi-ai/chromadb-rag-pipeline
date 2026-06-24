# ChromaDB RAG Pipeline

## About This Project

This is my RAG learning repository built while studying LangChain, Vector Databases, and LLM application development.

The objective was to understand how documents are ingested, chunked, converted into embeddings, stored in a vector database, and retrieved through semantic search before being provided as context to an LLM.

During development, I worked through package compatibility issues, environment setup challenges, and LangChain dependency management to build complete end-to-end pipelines.

---

## What I Built

### Phase 1: PDF Processing

Loaded a PDF document using LangChain's PyPDFLoader and prepared it for retrieval.

**Results**
- Loaded 4 pages from PDF
- Split 4 pages into 6 chunks
- Chunk Size = 500, Chunk Overlap = 50

**Skills Learned**
- PDF ingestion using PyPDFLoader
- LangChain Document objects
- RecursiveCharacterTextSplitter
- Context chunking strategies used in RAG systems

---

### Phase 2: Vector Database Pipeline

Created sample AI-related documents and built a complete vector search workflow.

**Sample Topics**
- Machine Learning Fundamentals
- Deep Learning & Neural Networks
- Natural Language Processing

**Workflow**
Documents → DirectoryLoader → Document Chunks → HuggingFace Embeddings → ChromaDB → Similarity Search

**Embedding Model:** `sentence-transformers/all-MiniLM-L6-v2`

**Results**
- Generated 384-dimensional vector embeddings
- Stored embeddings inside ChromaDB
- Performed semantic similarity search on queries like "What is machine learning?"

**Skills Learned**
- HuggingFace Embeddings integration
- ChromaDB vector storage
- Semantic search vs keyword search

---

### Phase 3: HyDE RAG Pipeline (Hypothetical Document Embeddings)

Implemented HyDE — an advanced retrieval technique that improves semantic search by generating a hypothetical answer before querying the vector database.

**How HyDE Works**
User Query → LLM generates Hypothetical Answer → Embed Hypothetical Answer → ChromaDB Search → Retrieve Real Documents → Final Answer

**Why HyDE?**
Standard RAG embeds the user query directly. Since queries are short and documents are long, embedding similarity is weak. HyDE solves this by generating a fake but realistic answer first — its embedding is structurally closer to real documents, improving retrieval quality.

**Results**
- Successfully generated hypothetical documents using Llama 3.3 70B via Groq
- Retrieved semantically relevant documents using hypothetical embeddings
- Built end-to-end HyDE chain using LangChain LCEL

**Technologies Used**
- LangChain LCEL (pipe syntax)
- ChatGroq (Llama 3.3 70B)
- ChromaDB
- HuggingFace Embeddings
- ChatPromptTemplate

---

## Technologies Used

- Python
- LangChain
- ChromaDB
- HuggingFace Embeddings
- Sentence Transformers
- Groq API (Llama 3.3 70B)
- PyPDFLoader
- RecursiveCharacterTextSplitter
- Git / GitHub

---

## Key Concepts Learned

- Document Loading and PDF Ingestion
- Document Chunking Strategies
- Embeddings and Vector Representations
- ChromaDB Vector Storage
- Semantic Search and Similarity Retrieval
- Basic RAG Architecture
- HyDE (Hypothetical Document Embeddings)
- LangChain LCEL Chain Building
- Groq LLM Integration

---

## Challenges Faced

Multiple dependency and import issues with LangChain packages, HuggingFace integrations, and environment configuration. Resolving these issues helped me better understand Python environments, package management, and the LangChain ecosystem.

---

## Personal Note

This repository documents my hands-on RAG learning journey — from basic PDF ingestion to advanced retrieval techniques like HyDE.

Each phase was built and debugged independently, focusing on understanding the workflow rather than copying pre-written code.
