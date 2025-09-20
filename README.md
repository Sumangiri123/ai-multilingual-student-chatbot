# 🎓 AI Multilingual Student Chatbot

An **AI-driven multilingual chatbot** designed to provide quick and reliable academic guidance for students.  
The chatbot supports **English + 3 regional languages** and integrates **Natural Language Understanding (NLU)**, **Retrieval-Augmented Generation (RAG)**, and **intent-slot extraction** to answer FAQs, academic queries, and handle student support tasks.  

This project is initially developed for **VTOP (VIT Online Portal)** as a demo and can be extended to other college portals to help students — especially from **rural backgrounds** — overcome language barriers.

---

## ✨ Features
- 🌐 **Multilingual Support** (English + 3 regional languages)  
- 📚 **RAG-enabled Knowledge Base** using institutional documents (handbooks, policies, exam schedules)  
- 🎯 **Intent & Slot Detection** for academic tasks (registration, deadlines, leave applications)  
- 👨‍🏫 **Human Handoff** for complex/low-confidence queries  
- 📊 **Analytics Dashboard** for usage, query types, and unanswered questions  
- 💻 **Web + Mobile Interfaces** for accessibility  

---

## 📂 Project Structure

```
ai-multilingual-student-chatbot/
│── README.md
│── requirements.txt
│── setup.py
│
├── data/
│ ├── raw/ # Raw PDFs, docs
│ ├── processed/ # Cleaned text
│ ├── chunks/ # Chunked text for embeddings
│ └── samples/ # Example queries/responses
│
├── notebooks/ # Jupyter notebooks for experiments
│ ├── 01_data_extraction.ipynb
│ ├── 02_translation.ipynb
│ ├── 03_embeddings_indexing.ipynb
│ └── 04_retrieval_testing.ipynb
│
├── src/
│ ├── data_processing/ # Cleaning, translation, chunking
│ ├── embeddings/ # Embedding + vector DB functions
│ ├── nlu/ # Intent & slot detection
│ ├── chatbot/ # Core chatbot pipeline
│ ├── handoff/ # Human handoff logic
│ └── api/ # FastAPI/Flask backend
│
├── tests/ # Unit + integration tests
│
├── frontend/
│ ├── web/ # Web chatbot (React/Streamlit)
│ └── mobile/ # Mobile app (Flutter/React Native)
│
└── docs/ # Documentation
```

## ⚙️ Installation

### 1. Clone the repo
```bash
git clone https://github.com/<your-username>/ai-multilingual-student-chatbot.git
cd ai-multilingual-student-chatbot
```

### 2. Create a virtual environment