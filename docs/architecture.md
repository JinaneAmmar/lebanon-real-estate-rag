# System Architecture

## Overview

The Lebanon Real Estate RAG system uses Retrieval-Augmented Generation to provide intelligent real estate investment advice.

## Components

### 1. Data Layer
- **Properties:** 200 Lebanese real estate listings (CSV)
- **Reports:** 4 RAMCO quarterly market reports (PDFs)

### 2. Processing Layer
- **Data Cleaning:** Standardization, validation, enrichment
- **PDF Extraction:** OCR for scanned documents
- **Chunking:** Breaking reports into searchable segments

### 3. Storage Layer
- **Vector Database:** ChromaDB
  - Properties Collection: 200 documents
  - Reports Collection: 121 chunks
- **Embeddings:** Automatic with ChromaDB

### 4. Retrieval Layer
- **Semantic Search:** Vector similarity
- **Metadata Filtering:** Price, location, bedrooms
- **Ranking:** Relevance-based ordering

### 5. Generation Layer
- **LLM:** TinyLlama-1.1B-Chat
- **Prompt Engineering:** Context-aware prompts
- **Response Formatting:** Structured output

### 6. Interface Layer
- **Web UI:** Gradio
- **Public Sharing:** Automatic link generation

## Data Flow
```
User Query
    ↓
[Query Understanding]
    ↓
[Vector Search] → Properties + Reports
    ↓
[Context Assembly]
    ↓
[LLM Generation]
    ↓
[Response Formatting]
    ↓
User Interface
```

## Technologies

- **Python 3.10+**
- **ChromaDB:** Vector database
- **Transformers:** Hugging Face models
- **Gradio:** Web interface
- **Tesseract:** OCR engine
- **pdfplumber:** PDF processing

## Performance

- **Latency:** 30-60 seconds per query
- **Throughput:** Sequential processing
- **Memory:** ~4GB RAM
- **Storage:** ~2GB (models + data)

## Scalability

Current system handles:
- 200-500 properties efficiently
- Can scale to 10,000+ with optimization
- Single-user concurrent access (Colab limitation)
