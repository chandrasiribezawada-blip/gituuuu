#  InterviewMentor AI

An AI-powered multi-round mock interview assistant built using Retrieval-Augmented Generation (RAG), LangChain, FAISS Vector Database, HuggingFace Embeddings, and Groq LLMs.

The system conducts realistic AI interviews by analyzing uploaded resumes and dynamically generating interview questions with conversational memory and evaluation feedback.

---

#  Features

##  AI-Powered Mock Interviews
- Conducts realistic mock interviews
- Supports multiple interview rounds
- Dynamic question generation

##  Multi-Round Interview Support
Supports:
- HR Round
- Technical Round
- System Design Round
- Behavioral Round
- Aptitude Round

##  Resume Understanding
The system analyzes uploaded resumes and extracts:
- Skills
- Projects
- Technologies
- Education
- Experience Level

##  RAG (Retrieval-Augmented Generation)
Uses:
- Document chunking
- Embedding generation
- FAISS vector search
- MMR retrieval

to generate highly contextual interview questions.

##  Conversational Memory
Maintains previous:
- Questions
- Candidate Answers
- Interview Flow

to generate intelligent follow-up questions.

##  AI Evaluation System
Evaluates candidate answers based on:
- Technical Accuracy
- Clarity
- Communication
- Confidence
- Depth of Explanation

##  Final Interview Report
Provides:
- Overall Score
- Strengths
- Weaknesses
- Improvement Suggestions

##  Persistent FAISS Database
Stores vector database locally for faster reuse.

##  Duplicate PDF Handling
Prevents duplicate document indexing.

##  Corrupted PDF Handling
Gracefully handles invalid or corrupted PDFs.

---

#  Tech Stack

| Technology | Purpose |
|---|---|
| Streamlit | Frontend UI |
| LangChain | RAG Pipeline |
| FAISS | Vector Database |
| HuggingFace Embeddings | Text Embeddings |
| Groq LLM | Large Language Model |
| PyPDFLoader | PDF Processing |
| Python | Backend |

---

#  Architecture

```text
User Uploads Resume
        ↓
PDF Processing
        ↓
Text Chunking
        ↓
Embedding Generation
        ↓
FAISS Vector Storage
        ↓
MMR Retrieval
        ↓
Resume Understanding
        ↓
AI Interview Question Generation
        ↓
Candidate Answer Evaluation
        ↓
Conversation Memory
        ↓
Dynamic Follow-Up Questions
        ↓
Final Interview Report
```

---

#  Project Structure

```text
InterviewMentorAI/
│
├── app.py
├── .env
├── requirements.txt
├── faiss_index/
└── README.md
```

---

#  Installation

## 1️ Clone Repository

```bash
git clone <your-github-repo-link>
cd InterviewMentorAI
```

---

##  Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\\Scripts\\activate
```

### Linux/Mac

```bash
python3 -m venv venv
source venv/bin/activate
```

---

##  Install Dependencies

```bash
pip install -r requirements.txt
```

---

#  Required Libraries

```bash
pip install streamlit
pip install langchain
pip install langchain-community
pip install langchain-huggingface
pip install langchain-groq
pip install langchain-text-splitters
pip install sentence-transformers
pip install faiss-cpu
pip install pypdf
pip install python-dotenv
```

---

#  Environment Variables

Create a `.env` file in the project root.

```env
GROQ_API_KEY=your_groq_api_key
```

---

#  Run Application

```bash
streamlit run app.py
```

---

#  How It Works

## Step 1 — Upload Resume
Upload one or multiple PDF resumes/documents.

## Step 2 — Build Knowledge Base
The system:
- extracts text
- chunks documents
- creates embeddings
- stores vectors in FAISS

## Step 3 — Resume Analysis
The AI analyzes:
- skills
- education
- projects
- technologies

## Step 4 — AI Interview Starts
The interviewer dynamically asks:
- technical questions
- HR questions
- follow-up questions

based on the resume and conversation history.

## Step 5 — AI Evaluation
Candidate answers are evaluated in real time.

## Step 6 — Final Report
At the end of the interview:
- overall score
- performance feedback
- improvement suggestions

are generated.

---

#  Key Functionalities

| Feature | Implemented |
|---|---|
| Resume Parsing | ✅ |
| RAG Pipeline | ✅ |
| FAISS Vector DB | ✅ |
| MMR Retrieval | ✅ |
| Conversational Memory | ✅ |
| Follow-Up Questions | ✅ |
| AI Evaluation | ✅ |
| Persistent Vector DB | ✅ |
| Duplicate File Detection | ✅ |
| Error Handling | ✅ |

---

#  Interviewer Explanation

> “InterviewMentor AI is an industry-style AI mock interview platform developed using Retrieval-Augmented Generation (RAG). The application processes resumes using LangChain and FAISS vector search, generates contextual interview questions using Groq LLMs, maintains conversational memory for follow-up questioning, and evaluates candidate answers dynamically with structured feedback and scoring.”

---

#  Future Improvements

- Voice-based interviews
- Real-time speech evaluation
- Facial emotion analysis
- Code editor integration
- Multi-user authentication
- Cloud deployment
- Analytics dashboard
- Interview performance tracking

---

#  Author

Developed as an AI-powered interview preparation system using modern LLM and RAG technologies.
```text
+----------------------+
| Start Application    |
+----------+-----------+
           |
           v
+----------------------+
| Upload Resume PDFs   |
+----------+-----------+
           |
           v
+----------------------+
| PDF Processing       |
| (PyPDFLoader)        |
+----------+-----------+
           |
           v
+----------------------+
| Text Chunking        |
| Recursive Splitter   |
+----------+-----------+
           |
           v
+----------------------+
| Generate Embeddings  |
| HuggingFace Model    |
+----------+-----------+
           |
           v
+----------------------+
| Store in FAISS DB    |
+----------+-----------+
           |
           v
+----------------------+
| Resume Analysis      |
+----------+-----------+
           |
           v
+----------------------+
| Start Interview      |
+----------+-----------+
           |
           v
+----------------------+
| Generate Question    |
| using RAG + LLM      |
+----------+-----------+
           |
           v
+----------------------+
| Candidate Answers    |
+----------+-----------+
           |
           v
+----------------------+
| AI Evaluation        |
+----------+-----------+
           |
           v
+----------------------+
| Store Conversation   |
| in Memory            |
+----------+-----------+
           |
           v
+----------------------+
| Generate Follow-Up   |
| Question             |
+----------+-----------+
           |
           v
+----------------------+
| Interview Complete   |
+----------+-----------+
           |
           v
+----------------------+
| Generate Final       |
| Performance Report   |
+----------------------+
```
start application

upload resume pdfs

pdf processing

text chunking recursive splitter

generate embeddings hugging face model

store in FAISS DB

resume analysis

start interview

Generate Question   using RAG + LLM

candidate answers

ai evaluation

store conversation in memory

generate follow up question

Interview complete

generate Final Performance report
┌───────────────────────────────────────────────────┐
│                 User Interface                    │
│                  Streamlit UI                     │
└───────────────────────┬───────────────────────────┘
                        │
                        ▼
┌───────────────────────────────────────────────────┐
│             Resume Upload Module                 │
│              PDF File Handling                   │
└───────────────────────┬───────────────────────────┘
                        │
                        ▼
┌───────────────────────────────────────────────────┐
│              PDF Processing Layer                │
│                PyPDFLoader                       │
└───────────────────────┬───────────────────────────┘
                        │
                        ▼
┌───────────────────────────────────────────────────┐
│               Text Chunking Layer                │
│      RecursiveCharacterTextSplitter              │
└───────────────────────┬───────────────────────────┘
                        │
                        ▼
┌───────────────────────────────────────────────────┐
│             Embedding Generation                 │
│      HuggingFace all-MiniLM-L6-v2                │
└───────────────────────┬───────────────────────────┘
                        │
                        ▼
┌───────────────────────────────────────────────────┐
│              FAISS Vector Database               │
│          Semantic Similarity Search              │
└───────────────────────┬───────────────────────────┘
                        │
                        ▼
┌───────────────────────────────────────────────────┐
│                 MMR Retriever                    │
│          Context-Aware Retrieval                 │
└───────────────────────┬───────────────────────────┘
                        │
                        ▼
┌───────────────────────────────────────────────────┐
│                   Groq LLM                       │
│         llama-3.3-70b-versatile                  │
└───────────────────────┬───────────────────────────┘
                        │
         ┌──────────────┴──────────────┐
         │                             │
         ▼                             ▼

┌───────────────────────┐   ┌───────────────────────┐
│ Interview Question    │   │ Answer Evaluation     │
│ Generation            │   │ & Feedback            │
└─────────────┬─────────┘   └─────────────┬─────────┘
              │                           │
              └─────────────┬─────────────┘
                            │
                            ▼

┌───────────────────────────────────────────────────┐
│          Final Interview Report Module           │
└───────────────────────────────────────────────────┘
┌──────────────────────────────────────────────┐
│              User Browser                    │
│           Streamlit Frontend                 │
└──────────────────┬───────────────────────────┘
                   │
                   ▼
┌──────────────────────────────────────────────┐
│             Streamlit Server                 │
│                 app.py                       │
└──────────────────┬───────────────────────────┘
                   │
      ┌────────────┼────────────┐
      │            │            │
      ▼            ▼            ▼

┌─────────────┐ ┌─────────────┐ ┌────────────────┐
│ HuggingFace │ │ FAISS DB    │ │ Groq LLM API   │
│ Embeddings  │ │ VectorStore │ │ llama-3.3-70b  │
└─────────────┘ └─────────────┘ └────────────────┘

                   │
                   ▼

┌──────────────────────────────────────────────┐
│          Uploaded Resume PDFs                │
│         Temporary File Storage               │
└──────────────────────────────────────────────┘
