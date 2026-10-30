# DocuMind – AI-Powered Document Chatbot

DocuMind is a full-stack AI-powered document assistant that allows users to upload PDF, DOC, and DOCX files and ask questions about their contents.

It uses Retrieval-Augmented Generation (RAG) to retrieve relevant information from uploaded documents and generate context-aware answers using Google Gemini.

## Overview

The application combines a React frontend, Python FastAPI backend, ChromaDB vector database, and Google Gemini API to provide document-based question answering.

## Features

### Document Processing

* Upload PDF, DOC, and DOCX documents.
* Extract text from uploaded documents.
* Split document content into smaller chunks.
* Process documents for question answering.

### AI and Retrieval

* Semantic search using ChromaDB.
* Generate embeddings for document content.
* Retrieve relevant document sections.
* Generate context-aware responses using Google Gemini.
* Answer questions based on uploaded documents.

### User Interface

* React-based chatbot interface.
* Document upload functionality.
* Chat interface for asking questions.
* Conversation handling.
* Responsive user interface.

## Technology Stack

| Component           | Technology                                |
| ------------------- | ----------------------------------------- |
| Frontend            | React.js                                  |
| Backend             | Python, FastAPI                           |
| AI Model            | Google Gemini                             |
| Vector Database     | ChromaDB                                  |
| Embeddings          | Sentence Transformers / OpenAI (optional) |
| Document Processing | PyMuPDF, python-docx                      |
| HTTP Requests       | Axios                                     |
| API Server          | Uvicorn                                   |

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
├── docs/
│   └── screenshots/
│
├── README.md
└── .gitignore
```

## Installation and Setup

### Prerequisites

* Python 3.10 or later
* Node.js and npm
* Google Gemini API key

### 1. Clone the Repository

```bash
git clone https://github.com/vinay-guntreddy/DocuMind.git
cd DocuMind
```

### 2. Backend Setup

Open a terminal in the project folder and run:

```powershell
cd backend

python -m venv venv

.\venv\Scripts\activate

pip install -r requirements.txt
```

### 3. Configure Environment Variables

Create your environment file:

```powershell
copy .env.example .env
```

Open `backend/.env` and add your Google Gemini API key:

```env
GOOGLE_API_KEY=your-gemini-api-key
OPENAI_API_KEY=
```

The OpenAI API key is optional. Sentence Transformers can be used as a fallback for embeddings.

**Important:** Never upload your `.env` file or share your API keys publicly.

### 4. Start the Backend

From the backend directory, run:

```bash
uvicorn app.main:app --reload --port 8000
```

The backend will run at:

```text
http://localhost:8000
```

### 5. Frontend Setup

Open a **second terminal** in the project folder and run:

```bash
cd frontend

npm install

npm start
```

The frontend will open at:

```text
http://localhost:3000
```

## Usage

1. Start both the backend and frontend servers.
2. Open the DocuMind application in your browser.
3. Upload a PDF, DOC, or DOCX document.
4. Wait for document processing to complete.
5. Enter a question related to the uploaded document.
6. Receive an AI-generated response based on the document content.

## Future Improvements

* Support for additional document formats.
* Improved retrieval accuracy.
* Faster response generation.
* Better conversation management.
* Enhanced user interface and experience.


## Maintainer

**Sai Vinay Guntreddy**

GitHub: https://github.com/vinay-guntreddy
