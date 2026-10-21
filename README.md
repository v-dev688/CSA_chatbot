# 🏏 Cricket South Africa AI Assistant

An intelligent, context-aware chatbot dedicated to South African cricket, powered by **LangChain** and **Retrieval-Augmented Generation (RAG)**. The bot retrieves grounded domain knowledge—covering Proteas match history, player statistics, domestic fixtures, and team records—to deliver precise answers without hallucinating general cricket data.

Designed with clean, modular architecture, this project is lightweight and ready for single-node deployment on an **AWS EC2** instance.

---

## ✨ Features

- **Domain-Specific RAG Pipeline:** Ingests official documents, stats, and historical datasets to provide grounded answers about South African cricket.
- **LangChain Integration:** Simple, extensible chaining for document loading, vector embeddings, indexing, and LLM orchestration.
- **Vector Search:** Fast semantic retrieval using a lightweight vector database (FAISS / Chroma).
- **Plug-and-Play EC2 Deployment:** Minimal dependencies and environment setup, ready for `t2.micro` / `t3.small` or containerized execution via Docker.

---

## 🛠️ Architecture

1. **Ingestion & Splitting:** Cricket SA match reports, player bios, and rulebooks split into optimized text chunks.
2. **Embedding & Storage:** Chunks converted to vector embeddings and indexed in a vector store.
3. **Retrieval & Generation:** User queries trigger semantic similarity searches, providing relevant context to the LLM to generate the final response.

---

## 🚀 Quick Start (AWS EC2)

### 1. Launch & Connect to EC2
Launch an Ubuntu EC2 instance on AWS, configure security groups (allow SSH on port 22 and web/API traffic on your app's port), and connect:

```bash
ssh -i your-key.pem ubuntu@your-ec2-public-ip
