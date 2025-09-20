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

```
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

### 3. Install dependencies

```
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

## 🚀 Usage

### 1. Data Preparation

* Place institutional documents (PDFs, handbooks, policies) inside data/raw/.

* Run extraction + cleaning scripts (see notebooks/ or src/data_processing/).

### 2. Build Knowledge Base

```
python src/embeddings/embedder.py
```

### 3. Run Chatbot API

```
uvicorn src.api.app:app --reload
```

This starts the FastAPI server at http://127.0.0.1:8000.

### 4. Run Web Interface

```
streamlit run frontend/web/app.py
```

### 📊 Example Query Flow

#### 1. Student asks in Hindi: "परीक्षा की तारीख कब है?"

#### 2. Bot detects language → translates → retrieves exam schedule.

#### 3. Answer generated in English → translated back to Hindi.

#### 4. If low confidence, bot triggers human handoff.


## 🧪 Testing

Run unit tests:

```
pytest tests/
```

## 🛠️ Tech Stack
### 🛠️ Tech Stack

**Backend**:
* FastAPI
* Python

**Frontend**:
* Streamlit / React.js (web)
* Flutter (mobile)

**NLP**:
* Hugging Face Transformers
* Sentence-Transformers

**Vector DB**:
* FAISS / Pinecone

**LLM Integration**:
* GPT / LLaMA 2 / Falcon

**Deployment**:
* Docker
* Gunicorn
* Nginx


### 🤝 Contributing

1.  **Fork** the repository.
2.  Create a new branch (`feature/xyz`).
3.  **Commit** your changes and **push** them to your branch.
4.  Open a **Pull Request**.

---

### 📜 License

This project is licensed under the **MIT License**—see the `LICENSE` file for details.

---

### 👨‍🎓 Author

**Suman Giri** (Student, VIT Chennai)
*Project Guide*: **M. Kaliyappan**