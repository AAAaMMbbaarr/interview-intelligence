# Interview Intelligence Agent

🎯 AI-powered interview preparation tool that predicts exactly what you'll be asked based on your resume and the job description.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.63-red)
![Gemini](https://img.shields.io/badge/Google%20Gemini-Free-green)

## What It Does

Upload your resume + paste a job description → get a full interview prediction:

- **📊 Fit Score** — How well your resume matches the JD (0-100%)
- **🎯 Top 10 Questions** — With probability scores (50-99%), categorized by type
- **⚠️ Interviewer Concerns** — Red flags and how to address them
- **🥊 Attack Mode** — Skeptical interviewer stress-tests your claims
- **🔗 Follow-up Chains** — Simulates real drill-down conversations
- **🎤 Voice Mock Interview** — Practice with an AI interviewer that speaks and listens

## Why This Is Different

Most interview prep tools give generic questions. This tool:
1. Cross-references **YOUR resume** with **THIS job**
2. Predicts **probability** of each question
3. Explains the **interviewer's motivation**
4. **Attacks your claims** so you're never caught off guard
5. **Voice interview** — AI speaks questions, you answer with your mic

> Your resume doesn't just determine IF you get an interview. It determines WHAT you'll be asked.

## Quick Start

### 1. Get a free API key
Go to [aistudio.google.com/apikey](https://aistudio.google.com/apikey) → Create API Key (no credit card needed)

### 2. Clone & setup
```bash
git clone https://github.com/YOUR_USERNAME/interview-intelligence.git
cd interview-intelligence

pip install -r requirements.txt
```

### 3. Add your API key
Create a `.env` file:
```
GOOGLE_API_KEY=your_api_key_here
```

### 4. Run
```bash
streamlit run app.py
```
Opens at `http://localhost:8501`

## How It Works

```
Resume PDF ──────┐
                 ↓
              Gemini API  →  5-Step Analysis  →  Results + Voice Interview
                 ↑
Job Description ─┘
```

The app runs **5 parallel AI analyses**:
1. Resume-JD fit scoring
2. Question prediction with probabilities
3. Interviewer concern identification
4. Resume claim stress-testing
5. Follow-up chain generation

Results are returned as **structured JSON** and rendered in clean, tabbed cards.

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Frontend | Streamlit |
| AI/LLM | Google Gemini (free tier) |
| PDF Parsing | PyPDF |
| Voice (TTS) | Browser SpeechSynthesis API |
| Voice (STT) | Gemini multimodal audio input |

## Project Structure

```
interview-intelligence/
├── app.py              # Entire application (UI + prompts + API calls)
├── .env                # API key (not committed)
├── requirements.txt    # Python dependencies
├── .gitignore          # Git ignore rules
└── README.md           # This file
```

## Screenshots

### Step 1: Upload
Upload your resume and paste/upload the job description.

### Step 2: Analysis
5-step AI analysis with live progress and countdown timer.

### Step 3: Results
Tabbed results with fit score, predicted questions, concerns, and attack mode.

### Step 4: Voice Interview
Practice with an AI interviewer that speaks questions and listens to your answers.

## Cost

**Free.** Uses Google Gemini's free tier (15 requests/minute). No credit card required.

## License

MIT
