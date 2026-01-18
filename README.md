# 🚀 RAG with Gemma-3

A **fully local, modular Retrieval-Augmented Generation (RAG) system** powered by **Gemma-3**, designed for privacy-first document understanding and intelligent question answering.  
The system enables users to upload documents, index them into vector embeddings, and interact with their content using natural language — all while running locally with complete control over data and inference.

This project focuses on **clean architecture, modular design, and real-world RAG workflows**, making it suitable for learning, research, and production-ready experimentation.

---

## 📌 Overview

**RAG with Gemma-3** is an end-to-end RAG pipeline that integrates:
- Local LLM inference using **Gemma-3 via Ollama**
- Efficient vector search with **FAISS**
- Modular orchestration using **LangChain**
- A responsive frontend built with **Streamlit**
- A scalable backend using **FastAPI**

The system supports **multi-document ingestion per user**, persistent session history, real-time streaming responses, and document previews — delivering a complete RAG experience.

---

## 📃 Table of Contents
- [Project Goals](#-project-goals)
- [System Architecture](#-system-architecture)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Installation](#-installation)
  - [Virtual Environment](#virtual-environment)
  - [Docker Setup](#-docker-setup)
- [Additional Configuration](#-additional-configuration)
- [Future Enhancements](#-future-enhancements)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🎯 Project Goals

- Build a **robust and extensible RAG system**
- Enable **local inference for privacy and cost efficiency**
- Demonstrate a **clean modular architecture**
- Support **real-time streaming responses**
- Provide an **intuitive UI for document interaction**

---

## 🧠 System Architecture

The system follows a modular, service-oriented design:

1. **Frontend (Streamlit)**
   - Document upload & preview
   - Chat interface with streaming responses
   - Session and file management

2. **Backend (FastAPI)**
   - User authentication
   - File ingestion and processing
   - SSE-based streaming responses

3. **LLM Orchestration Layer**
   - Document chunking
   - Vector embedding
   - Context retrieval
   - History summarization
   - Response generation

4. **Storage Layer**
   - FAISS for vector indices
   - SQLite for users, sessions, and metadata

---

## ✨ Key Features

### 🔐 User Authentication
- Secure authentication using **SQLite** and **bcrypt**
- Session persistence with automatic cleanup of stale data

### 📄 Document Handling
- Upload multiple documents per user
- Support for PDF, TXT, Markdown (extendable)
- Live document previews
- Public and private document scopes

### 🔍 Retrieval-Augmented Generation
- High-quality vector embeddings
- Semantic similarity search with FAISS
- Context-aware responses grounded in retrieved documents

### 💬 Real-Time Chat Experience
- Server-Sent Events (SSE) for streaming output
- Display of retrieved sources and metadata
- Optional support for reasoning / thinking models

### 🧩 Modular LLM System
- Pluggable components for:
  - Ingestion
  - Embeddings
  - Retrieval
  - History management
  - Response generation
- Tracing support via **LangSmith**

### 🐳 Dockerized Deployment
- Single Dockerfile supporting:
  - Development mode
  - Production deployment
- Compatible with Hugging Face Spaces

---

## 🧑‍💻 Tech Stack

**Core**
- LangChain
- Gemma-3 (via Ollama)
- FAISS
- FastAPI
- Streamlit

**Infrastructure**
- Docker
- SQLite
- LangSmith
- bcrypt

**Deployment**
- Hugging Face Spaces
- GitHub Actions (CI/CD & secret scanning)

---

## 🛠️ Installation

You can run the project either using a **virtual environment** or **Docker**.

---

### Virtual Environment

1. Clone the repository:
```bash
git clone --depth 1 https://github.com/Bbs1412/rag-with-gemma3.git
cd rag-with-gemma3
