# 📄 Week 7 Assignment – Retrieval-Augmented Generation (RAG) Chatbot

## Overview

This project implements a **Retrieval-Augmented Generation (RAG)** chatbot that answers user questions based on the contents of a PDF document. Instead of relying only on the Large Language Model's pre-trained knowledge, the chatbot retrieves the most relevant information from the uploaded document and uses it to generate accurate, context-aware responses.

---

## Objectives

- Load and process a PDF document.
- Split the document into manageable text chunks.
- Convert text chunks into vector embeddings.
- Store embeddings in a FAISS vector database.
- Retrieve relevant document chunks for user queries.
- Generate answers using an LLM based on the retrieved context.

---

## Technologies Used

- Python
- LangChain
- Hugging Face Transformers
- Sentence Transformers
- FAISS
- PyPDFLoader
- RecursiveCharacterTextSplitter
- TinyLlama-1.1B-Chat-v1.0

---

## Project Workflow

### Step 1: Load PDF

The PDF document is loaded using **PyPDFLoader**.

```python
loader = PyPDFLoader("What is Retrieval.pdf")
documents = loader.load()
```

---

### Step 2: Text Chunking

The document is divided into smaller overlapping chunks.

Example configuration:

```python
chunk_size = 700
chunk_overlap = 150
```

This helps preserve context during retrieval.

---

### Step 3: Generate Embeddings

Each text chunk is converted into numerical vectors using:

```
sentence-transformers/all-MiniLM-L6-v2
```

Embeddings capture semantic meaning instead of simple keywords.

---

### Step 4: Create Vector Database

The generated embeddings are stored inside **FAISS**.

```python
vector_db = FAISS.from_documents(
    chunks,
    embeddings
)
```

FAISS enables efficient similarity search.

---

### Step 5: Retrieve Relevant Chunks

When a user asks a question,

- the question is converted into an embedding
- FAISS searches for the most similar chunks
- top-k relevant chunks are returned

Example:

```python
docs = vector_db.similarity_search(
    query,
    k=8
)
```

---

### Step 6: Prompt Construction

The retrieved chunks are combined with the user's question.

Example Prompt:

```
Context:
<Retrieved Text>

Question:
<User Question>

Answer only using the above context.
```

---

### Step 7: Generate Response

The prompt is passed to

```
TinyLlama-1.1B-Chat-v1.0
```

which generates the final answer.

---

## Model Used

### LLM

- TinyLlama-1.1B-Chat-v1.0

### Embedding Model

- sentence-transformers/all-MiniLM-L6-v2

### Vector Database

- FAISS

---


## Example Query

```
What is Retrieval-Augmented Generation?
```

### Output

```
Retrieval-Augmented Generation (RAG) combines information retrieval with text generation.
It first retrieves relevant information from external sources and then uses an LLM to
generate accurate and context-aware responses.
```

---

## Advantages

- Reduces hallucinations
- Provides context-aware responses
- Uses external knowledge
- No need for model retraining
- Easy to update knowledge by replacing documents

---

## Limitations

- Retrieval quality affects answer quality.
- Small LLMs may generate shorter responses.
- Large documents require more storage and indexing time.
- Poor chunking can reduce retrieval accuracy.

---

## Future Improvements

- Support multiple PDF documents.
- Add conversation memory.
- Implement Hybrid Search.
- Use reranking for better retrieval.
- Deploy as a Streamlit or Flask web application.
- Replace FAISS with Pinecone or ChromaDB for cloud deployment.

---

## Conclusion

This project demonstrates the complete implementation of a Retrieval-Augmented Generation (RAG) pipeline using LangChain, FAISS, Hugging Face embeddings, and TinyLlama. By combining document retrieval with LLM-based generation, the chatbot provides accurate, grounded, and context-aware responses from the uploaded PDF.
