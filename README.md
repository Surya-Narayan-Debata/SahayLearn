# 🎓 Sahay - Gamified Learning Platform

Sahay is an interactive, gamified learning platform for Class 12th Physics and Chemistry powered by Google Gemini and ChromaDB.

---

## ✨ Features

- 📖 **Interactive Learning**: Chunked textbook content with step-by-step progression
- 💬 **AI Tutor Q&A**: Select any paragraph to ask questions, request Hinglish explanations, analogies, or examples
- 📊 **AI-Powered Assessments**: Dynamically generates 4 MCQs per part with instant grading and explanations
- 🔄 **Adaptive Learning**: Automatically generates simplified content and practice problems if score < 75%
- 🏆 **Gamification & Badges**: Earn achievement badges, track streak, and view progress dashboards

---

## 🚀 Getting Started

Follow these steps to set up and run Sahay on your computer.

### 1. Prerequisites
- Python 3.11 or higher
- Git

### 2. Clone the Repository
```bash
git clone https://github.com/Surya-Narayan-Debata/SahayLearn.git
cd SahayLearn
```

### 3. Create and Activate Virtual Environment (Recommended)

**On Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**On macOS / Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```

### 5. Set Up Gemini API Key

1. Get a free API key from [Google AI Studio](https://aistudio.google.com/apikey).
2. Create a `.env` file in the root folder (or copy from `.env.example`):
```bash
cp .env.example .env
```
3. Open `.env` and add your key:
```env
GEMINI_API_KEY=your_gemini_api_key_here
```

### 6. Run the Application
```bash
streamlit run app.py
```

The app will automatically open in your default web browser at `http://localhost:5000` (or `http://localhost:8501`).

---

## 📂 Project Structure

```
SahayLearn/
├── app.py                     # Main Streamlit application entry point
├── components/                # UI components
│   ├── learning_interface.py     # Content reader & AI Q&A chat
│   ├── assessment_interface.py   # MCQ quiz generator & evaluation
│   ├── performance_dashboard.py  # Student analytics & charts
│   └── badge_system.py           # Gamified achievements & badges
├── utils/                     # Backend services
│   ├── chromadb_manager.py       # ChromaDB vector store management
│   ├── gemini_client.py          # Google Gemini API client with multi-model fallback
│   ├── langchain_orchestrator.py # Content & assessment orchestration
│   └── pdf_processor.py          # PDF text extraction & chunking
├── attached_assets/           # PDF textbooks (Physics & Chemistry)
├── chroma_db/                 # ChromaDB persistent vector storage
├── requirements.txt           # Python package dependencies
├── .env.example               # Template for environment variables
└── README.md                  # Project documentation
```

---

## 🛠 Tech Stack

- **Frontend**: [Streamlit](https://streamlit.io/)
- **LLM**: [Google Gemini API](https://ai.google.dev/) (`google-genai` SDK with auto-fallback)
- **Vector Database**: [ChromaDB](https://www.trychroma.com/)
- **Document Processing**: PyPDF2
