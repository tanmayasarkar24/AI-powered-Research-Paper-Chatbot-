# AI-powered-Research-Paper-Chatbot-
Summarization, Q&amp;A, and Semantic Search using Transformers, FAISS, and Streamlit.
# 🤖 Research Paper Chatbot

An intelligent **AI-powered assistant** that reads, understands, and answers questions from research papers.  
Built for researchers, students, and innovators to **interact with complex academic PDFs** effortlessly.  

This project uses a **hybrid retrieval + generation pipeline** powered by modern **NLP & LLM models**.

---

## 🚀 Overview

Traditional research exploration can be time-consuming — skimming through multiple sections like *methodology, results, and conclusion* for every paper.

**Research Paper Chatbot** solves that by allowing you to:
- 🧠 Upload any research paper (PDF)  
- 💬 Ask questions like *“What’s the accuracy?”* or *“Summarize the abstract”*  
- ⚙️ Get instant, context-aware answers extracted from the actual paper

---

## ✨ Features

- 📄 **PDF Parsing:** Extracts clean text using `PyMuPDF`
- ✂️ **Smart Text Chunking:** Keeps semantic flow intact with overlapping chunks
- 🔍 **Semantic Search:** Uses `SentenceTransformer (MiniLM-L6-v2)` for deep contextual retrieval
- 🧮 **FAISS Indexing:** Enables lightning-fast similarity search
- 🤖 **LLM-based Reasoning:** Combines `Flan-T5` for Q&A and `BART` for summarization
- 🧠 **Section-Aware Understanding:** Recognizes and handles questions by section (e.g., *abstract*, *results*, *methodology*)
- 💾 **Persistent State:** Saves embeddings, chunks, and indexes for each uploaded paper
- 🧩 **Modular Codebase:** Easily extendable for new models or datasets
- 🖥️ **Future Streamlit App:** Interactive, chat-style UI with PDF upload and chat history

---

## 🧩 How It Works

The chatbot follows a **hybrid retrieval + generation** architecture:

1. **📄 PDF Upload & Text Extraction**  
   Extracts and cleans text using PyMuPDF for robust PDF parsing.

2. **✂️ Text Chunking**  
   Splits text into overlapping, context-preserving chunks for better comprehension.

3. **🔢 Embedding Generation**  
   Generates semantic embeddings with `SentenceTransformer (all-MiniLM-L6-v2)`.

4. **🧮 FAISS Indexing**  
   Stores vectorized chunks for fast similarity-based retrieval.

5. **💬 Question Answering (LLM Reasoning)**  
   Uses `Flan-T5` to answer user questions with retrieved context.

6. **🧠 Section-Aware Routing**  
   Routes queries intelligently — for example, “summarize abstract” triggers BART summarization, while “accuracy” queries focus on result sections.

7. **💾 State Saving**  
   Saves all computed embeddings, indexes, and metadata for instant reuse.

---

## 🧱 Project Structure
📂 research_chatbot/
│
├── 📄 research_chatbot.ipynb # Main model notebook
├── 📁 saved_papers/ # Folder storing processed papers
│ ├── chunks.pkl
│ ├── embeddings.npy
│ ├── faiss.index
│ └── metadata.pkl
├── 📄 app.py # Streamlit Web App (coming soon)
├── 📄 requirements.txt # Dependencies
└── 🧾 README.md # Project documentation


---

## 🔮 Future Enhancements

✅ **Streamlit Web App Integration**  
→ A visually appealing web interface for chatting with uploaded papers.  

✅ **Multi-Paper Comparison Mode**  
→ Compare insights, results, and methods across multiple research papers.  

✅ **OCR Support for Scanned PDFs**  
→ Integrate `pytesseract` + `pdf2image` for extracting text from scanned documents.  

✅ **Advanced Model Fusion**  
→ Experiment with Llama 3 / Mistral for richer academic reasoning.  

✅ **Deployment**  
→ Host the full app on **Hugging Face Spaces** or **Streamlit Cloud** with GPU acceleration.

---

## ⚙️ Tech Stack

| Category | Tools / Models Used |
|-----------|--------------------|
| PDF Parsing | PyMuPDF (fitz) |
| Text Embedding | Sentence Transformers (MiniLM-L6-v2) |
| Semantic Search | FAISS |
| Summarization | Facebook BART Large CNN |
| Q&A | Google Flan-T5 Base |
| Visualization | Streamlit (UI) |
| OCR (Future) | pytesseract, pdf2image |


---

## 📜 License

This project is licensed under the **Apache 2.0 License**.  
Feel free to use, modify, and share — with proper credit.

---

> ⭐ *“Bringing research to your fingertips — one question at a time.”*
