# 📘 DocuMind AI

**Your Intelligent Document Assistant**

DocuMind AI is a sleek, lightweight, and efficient Retrieval-Augmented Generation (RAG) application built with Streamlit. It allows users to upload PDF documents and query them intelligently using the DeepSeek LLM model and Ollama Embeddings. Perfect for students, researchers, and professionals who need quick, context-aware insights from large documents.

---

## 🚀 Features

- 📄 **Upload PDF Files**
  - Parse research papers, reports, and more using `PDFPlumberLoader`.

- 🧠 **Chunking & Embedding**
  - Uses `RecursiveCharacterTextSplitter` to break documents into semantic chunks.
  - Embeds content into memory with `OllamaEmbeddings`.

- 🔍 **Semantic Search**
  - Finds the most relevant chunks using vector similarity search via `InMemoryVectorStore`.

- 🤖 **LLM-Powered Answers**
  - Powered by `deepseek-r1:1.5b` using `OllamaLLM` for fast, context-based responses.

- 🎨 **Dark Mode UI**
  - Custom-designed Streamlit interface with dark theme and enhanced styling.

---

## 🛠️ Tech Stack

| Component       | Technology                         |
|-----------------|-------------------------------------|
| Frontend        | Streamlit                          |
| PDF Loader      | `PDFPlumberLoader` (LangChain)     |
| Chunking        | `RecursiveCharacterTextSplitter`   |
| Vector Store    | `InMemoryVectorStore`              |
| Embeddings      | `OllamaEmbeddings` (`deepseek-r1`) |
| LLM Model       | `OllamaLLM` (`deepseek-r1`)        |

---

## 📦 Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/KhawajaAbdullah2000/llm_rag_deep_seek.git
cd llm_rag_deep_seek
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Start Ollama & Pull the Model
Make sure Ollama is installed and running the required model:
```bash
ollama run deepseek-r1:1.5b
```

### 4. Launch the App
```bash
streamlit run deep_rag.py
```

---

## 🧪 How It Works

1. Upload a PDF document.
2. The document is parsed, chunked, and embedded in memory.
3. Type your question into the chat interface.
4. The app searches for relevant context and generates a concise, factual answer using the LLM.

---

## 📁 Directory Structure

```
documind-ai/
│
├── app.py                     # Main Streamlit application
├── document_store/            # Uploaded PDFs are stored here
├── requirements.txt           # Python dependencies
└── README.md                  # This file
```

---

## 🧠 Prompt Template

```text
You are an expert research assistant. Use the provided context to answer the query. 
If unsure, state that you don't know. Be concise and factual (max 3 sentences).

Query: {user_query} 
Context: {document_context} 
Answer:
```

---

## 💡 Future Enhancements

- ✅ Multi-file upload and document management
- ✅ Persistent vector store (e.g., FAISS or ChromaDB)
- ✅ PDF OCR support for image-based documents
- ✅ Summarization, citation extraction, and document tagging

---

## 📋 License

This project is licensed under the **MIT License**. Feel free to use and modify as needed.

---

## 🙌 Acknowledgments

- [LangChain](https://www.langchain.com/)
- [Ollama](https://ollama.com/)
- [Streamlit](https://streamlit.io/)
- [PDFPlumber](https://github.com/jsvine/pdfplumber)

---

