# AI TUTOR PRO

## Overview

**AI TUTOR PRO** is a full-featured AI-powered web application that helps users solve math problems, understand concepts, and practice their skills. It also includes a Computer Science learning module. Users can input problems via text, image (OCR), camera, or voice and receive step-by-step explanations, mistake diagnosis, and personalized feedback.

---

## ✨ Features

### 🧠 Math Assistance
- **Step-by-Step Solutions** to math problems.
- **Mistake Diagnosis**: Upload your solution to receive AI-powered feedback.
- **Multiple Input Modes**:
  - Text Input
  - Image Upload (OCR)
  - Voice Dictation
  - Camera Input

### 🧪 Practice Generators
- **Mathematics**: Topic-based or problem-derived question generation.
- **Computer Science**: Chapter-wise generation of:
  - **MCQs**
  - **Coding Problems** (with in-browser code editor)
  - **Theory Questions**

### 💬 AI-Powered Explanations
- Interactive "Why" or "How" queries for math steps.
- CS solution analysis including:
  - Output simulation
  - Bug suggestions
  - Logic and style feedback

### 🎓 Learning Aids (CS Modules)
- **Flashcards**
- **Chapter Summaries**
- **Key Points**

### 📈 Graphing Tool
- Input equations and visualize them with plotted graphs.

### 🧑‍🏫 AI Tutor Chat
- Chat interface to ask math-related queries.

### 📊 Progress & XP System
- Experience points for solving problems.
- Levels and bookmarks for user tracking.

### ⚙️ Other Features
- User Authentication
- Bookmarking System
- Dark Mode & Responsive Design

---

## 🛠 Technologies Used

### Backend
- Python, FastAPI
- SQLAlchemy, Alembic
- Uvicorn, Pydantic
- Google Gemini API (AI capabilities)

### Frontend
- React + TypeScript
- Tailwind CSS, shadcn/ui, Radix UI
- React Router, TanStack Query
- KaTeX (math rendering), React Sketch Canvas
- React Simple Code Editor (for CS coding)

### Database
- SQLite

---

## 🗂 Project Structure

```
math-wiz-assistant/
├── alembic/              # Alembic migration scripts
├── backend/              # FastAPI backend app
│   ├── routers/          # API route files
│   ├── uploads/          # Image upload directory
│   ├── ocr.py            # OCR processing
│   ├── solver.py         # Math solving logic
│   └── graphing.py       # Graph generation logic
├── src/                  # Frontend React application
│   ├── components/       # Reusable UI & CS-specific components
│   ├── context/          # React context providers
│   ├── hooks/            # Custom hooks
│   ├── lib/              # Utilities & API helpers
│   ├── pages/            # Route-based page components
│   └── assets/           # Images and static resources
├── main.py               # FastAPI entry point
├── math_wiz_app.db       # SQLite database
├── README.md             # Project documentation
├── .env                  # Environment configuration
├── vite.config.ts        # Vite frontend config
└── package.json          # Frontend dependencies
```

---

## 🚀 Setup and Installation

### Prerequisites
- Python 3.8+
- Node.js + npm or bun
- Git

### Clone the Repository
```bash
git clone <REPO_URL>
cd math-wiz-assistant
```

---

### 🔧 Backend Setup

1. Create & activate virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

2. Install backend dependencies:
```bash
pip install -r backend/requirements.txt
```

3. Create `.env` file in root:
```
GOOGLE_API_KEY="your_google_api_key"
```

4. Run Alembic migration:
```bash
alembic upgrade head
```

5. Start FastAPI server:
```bash
uvicorn main:app --reload --port 8000
```

---

### 🖥️ Frontend Setup

1. Install frontend dependencies:
```bash
npm install
# OR
bun install
```

2. Create `.env` in root:
```
VITE_API_URL=http://127.0.0.1:8000
```

3. Start Vite dev server:
```bash
npm run dev
# OR
bun dev
```

Frontend available at `http://localhost:8003`

---

## 📡 API Endpoints (Summary)

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/register` | Register user |
| POST | `/api/login` | Login & get token |
| GET | `/api/users/me` | Get current user |
| POST | `/upload-image` | Upload image for OCR |
| POST | `/solve-text` | Solve text problem |
| POST | `/explain-step` | Clarify a solution step |
| POST | `/diagnose-solution` | Diagnose submitted solution |
| POST | `/generate-practice-problem` | Generate math problems |
| POST | `/cs/questions` | Generate CS question |
| POST | `/cs/submit` | Submit CS answer |
| POST | `/cs/learning-aids` | Get CS flashcards, summary, key points |
| POST | `/generate-graph` | Plot graph from equation |
| GET/POST/DELETE | `/api/bookmarks` | Manage bookmarks |
| GET | `/api/daily-puzzle` | Get daily puzzle |
| POST | `/api/submit-puzzle` | Submit puzzle answer |
| POST | `/api/chat` | (TBD) AI tutor chat |
| GET | `/user/data` | Get XP and progress |

---

## 🎮 Usage Guide

1. **Open App**: Go to `http://localhost:8003`
2. **Register/Login**
3. Explore:
   - 📐 Solve math problems
   - 🧠 Diagnose attempts
   - 🔁 Generate practice
   - 💻 Switch to CS module
   - ✍️ Try coding or theory questions
   - 🧾 Use AI-generated learning aids
   - 🧮 Use Graphing calculator
   - 📚 Bookmark your favorite problems
   - 🎯 Track progress with XP

---

## 🧪 Future Enhancements

- Full AI Tutor integration for CS
- Enhanced gamification (badges, streaks)
- Leaderboard and challenges
- Multilingual support

---

## 📄 License

This project is for educational purposes. Check `LICENSE` file if applicable.

---

## 🙌 Contributions

Pull requests and feedback are welcome!

---

## 👨‍💻 Developed By

Final Semester BCA Project  — AI TUTOR PRO
