# DocuMind – AI-Powered Document Chatbot

A full-stack AI-powered document assistant that allows users to upload PDF, DOC, and DOCX files and ask questions about their contents.

## Overview

DocuMind uses Retrieval-Augmented Generation (RAG) to retrieve relevant information from uploaded documents and generate context-aware answers using Google Gemini.

The application combines a React frontend, Python FastAPI backend, ChromaDB vector database, and Google Gemini API.

## Features

### Document Processing

* Upload PDF, DOC, and DOCX documents.
* Extract text from uploaded documents.
* Split document content into smaller chunks.
* Support document-based question answering.

### AI and Retrieval

* Semantic search using ChromaDB.
* Generate embeddings for document content.
* Retrieve relevant document sections.
* Generate context-aware responses using Google Gemini.
* Provide answers based on uploaded documents.

### User Interface

* React-based chatbot interface.
* Document upload functionality.
* Chat interface for asking questions.
* Conversation handling.
* Responsive user interface.

## Technology Stack

| Component           | Technology                     |
| ------------------- | ------------------------------ |
| Frontend            | React.js                       |
| Backend             | Python, FastAPI                |
| AI Model            | Google Gemini                  |
| Vector Database     | ChromaDB                       |
| Embeddings          | OpenAI / Sentence Transformers |
| Document Processing | PyMuPDF, python-docx           |
| HTTP Requests       | Axios                          |
| API Server          | Uvicorn                        |

## How It Works

1. **Upload:** The user uploads a PDF, DOC, or DOCX document.
2. **Extraction:** The backend extracts text from the document.
3. **Chunking:** The extracted text is divided into smaller sections.
4. **Embedding:** Embeddings are generated for the document sections.
5. **Storage:** The embeddings are stored in ChromaDB.
6. **Retrieval:** When the user asks a question, relevant sections are retrieved using similarity search.
7. **Generation:** The retrieved content and question are sent to Google Gemini.
8. **Response:** The chatbot generates an answer using the retrieved document information.

## Project Structure

```text
DocuMind/
│
├── backend/
│   ├── app/
│   │   ├── models/
│   │   ├── routers/
│   │   ├── services/
│   │   └── main.py
│   ├── requirements.txt
│   └── .env.example
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── App.js
│   │   ├── App.css
│   │   └── index.js
│   └── package.json
│
└── README.md
```

## Installation and Setup

### Prerequisites

* Python 3.10 or later
* Node.js and npm
* Google Gemini API key

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd DocuMind
```

### 2. Backend Setup

```bash
cd backend

python -m venv venv

venv\Scri
```
