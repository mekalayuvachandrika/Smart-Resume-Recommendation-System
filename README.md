# Smart Resume Analysis & Recommendation System

An agentic AI-powered full-stack web application that analyzes resumes, evaluates ATS compatibility, identifies skill gaps, conducts Human-in-the-Loop interviews, and recommends suitable learning resources and job opportunities.
## Features

### 1. 📄 Intelligent Resume Analysis
- Extracts and analyzes resume content automatically.
- Identifies candidate skills, education, experience, and relevant keywords.
- Supports structured resume evaluation.

### 2. 🤖 Human-in-the-Loop (HITL) Interview
- Generates contextual questions based on the uploaded resume.
- Allows users to answer and interact with the AI agent.
- Maintains workflow state using LangGraph checkpointing.

### 3. 🔍 Resume Evidence & Proof
- Provides the specific resume sentence or information that triggered an AI-generated question.
- Helps users understand why a particular question or recommendation was generated.

### 4. 📊 ATS Resume Evaluation
- Evaluates resume ATS readability and compatibility.
- Generates an ATS score from 0–100.
- Highlights areas that need improvement.
- Provides immediate recommendations for improving the resume.

### 5. 🎯 Skill Gap Analysis
- Compares the candidate's existing skills with required skills.
- Identifies missing or weak skill areas.
- Suggests relevant learning resources.

### 6. 📚 Personalized Learning Recommendations
- Recommends learning resources based on identified skill gaps.
- Provides resources such as YouTube and Udemy courses.

### 7. 💼 Job Recommendation
- Matches candidate profiles with relevant job opportunities.
- Uses resume information and extracted skills for personalized recommendations.

### 8. 🧠 Dual AI Intelligence
- Uses local NLP/heuristic processing for basic analysis.
- Can integrate with OpenAI or Google Gemini when API keys are configured.
## Technologies Used

### Frontend
- React.js
- HTML5
- CSS3
- JavaScript

### Backend
- Python
- FastAPI

### AI & Agentic Framework
- LangGraph
- Large Language Models (LLMs)
- OpenAI API / Google Gemini API
- Human-in-the-Loop (HITL) workflow

### AI Communication & Integration
- Model Context Protocol (MCP)
- MCP Client
- MCP Server

### Database & Persistence
- SQLite
- LangGraph SQLite Checkpointing

### Development Tools
- Visual Studio Code
- Git
- GitHub
- Node.js
- npm
- ## System Architecture

The system follows an agentic workflow where the uploaded resume passes through multiple analysis and recommendation stages.

```text
                    ┌──────────────────┐
                    │   Resume Upload  │
                    └────────┬─────────┘
                             ↓
                 ┌──────────────────────┐
                 │ Resume Text          │
                 │ Extraction & Parsing │
                 └──────────┬───────────┘
                            ↓
                 ┌──────────────────────┐
                 │   AI Resume Analysis │
                 └──────────┬───────────┘
                            ↓
             ┌──────────────┴──────────────┐
             ↓                             ↓
    ┌─────────────────┐          ┌──────────────────┐
    │ HITL QA Agent   │          │ ATS Evaluation   │
    └────────┬────────┘          └────────┬─────────┘
             ↓                            ↓
    ┌─────────────────┐          ┌──────────────────┐
    │ Resume Evidence │          │ ATS Score &      │
    │ / Proof         │          │ Improvements    │
    └────────┬────────┘          └────────┬─────────┘
             └──────────────┬─────────────┘
                            ↓
                 ┌──────────────────────┐
                 │   Skill Gap Analysis │
                 └──────────┬───────────┘
                            ↓
             ┌──────────────┴──────────────┐
             ↓                             ↓
    ┌──────────────────┐          ┌──────────────────┐
    │ Learning         │          │ Job              │
    │ Recommendations  │          │ Recommendations  │
    └──────────────────┘          └──────────────────┘
## Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/mekalayuvachandrika/Smart-Resume-Recommendation-System.git
cd Smart-Resume-Recommendation-System
cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
OPENAI_API_KEY=your_api_key_here
GEMINI_API_KEY=your_api_key_here
uvicorn main:app --reload
cd frontend
npm install
npm run dev

### 5. Save it

Scroll to the bottom of the GitHub page.

You'll see **Commit changes...**

Click it.

Then choose:

**Commit directly to the `main` branch**

and click **Commit changes**.

---

⚠️ **One correction from me:** don't paste the section if your existing README already has an **Installation/Setup** section—we don't want duplicate instructions.

If you want, **send me a screenshot of your current README editor**, and I'll point out exactly **where to paste it**.
