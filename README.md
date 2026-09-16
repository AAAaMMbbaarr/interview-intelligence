# 🎯 Interview Intelligence Agent

AI-powered interview preparation tool that predicts exactly what you'll be asked based on your resume and the job description.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.63-red)
![Gemini](https://img.shields.io/badge/Google%20Gemini-Free-green)

🔗 **[Try it live →](https://interview-intelligence.streamlit.app)**

---

## What It Does

Upload your resume + paste a job description → get a full interview prediction in ~60 seconds:

| Feature | Description |
|---------|-------------|
| 📊 **Fit Score** | How well your resume matches the JD (0-100%) |
| 🎯 **Top 10 Questions** | With probability scores (50-99%), categorized by type |
| ⚠️ **Interviewer Concerns** | Red flags and how to address them |
| 🥊 **Attack Mode** | Skeptical interviewer stress-tests your resume claims |
| 🔗 **Follow-up Chains** | Simulates real drill-down conversation threads |
| 🎤 **Voice Mock Interview** | AI speaks questions, you answer with your mic — live scoring |

## Why This Is Different

Most interview prep tools give generic questions. This tool:

1. Cross-references **YOUR resume** with **THIS specific job**
2. Predicts **probability** of each question being asked
3. Explains the **interviewer's motivation** behind each question
4. **Attacks your claims** so you're never caught off guard
5. **Voice mock interview** — AI speaks and listens, scores your answers live

> Your resume doesn't just determine IF you get an interview. It determines WHAT you'll be asked.

## Demo

### Step 1: Upload
Upload your resume (PDF) and paste or upload the job description.

### Step 2: AI Analysis
5-step analysis with live countdown timer — takes ~60-90 seconds.

### Step 3: Results
Tabbed results with fit score, predicted questions, concerns, and attack mode.

### Step 4: Voice Interview
Practice with an AI interviewer that speaks questions aloud and listens to your answers.

---

## Run Locally

### 1. Get a free Gemini API key
Go to [aistudio.google.com/apikey](https://aistudio.google.com/apikey) → Create API Key (free, no credit card)

### 2. Clone & install
```bash
git clone https://github.com/AAAaMMbbaarr/interview-intelligence.git
cd interview-intelligence

pip install -r requirements.txt
```

### 3. Add your API key
Create a `.env` file in the project root:
```
GOOGLE_API_KEY=your_api_key_here
```

### 4. Run
```bash
streamlit run app.py
```
Opens at `http://localhost:8501`

---

## Deploy (Free)

This app is deployed on **Streamlit Community Cloud** — free hosting for Streamlit apps.

### Deploy your own:
1. Fork this repo
2. Go to [share.streamlit.io](https://share.streamlit.io)
3. Connect your GitHub → select this repo → `app.py`
4. Add your `GOOGLE_API_KEY` in **Settings → Secrets**:
   ```toml
   GOOGLE_API_KEY = "your_api_key_here"
   ```
5. Click **Deploy** — you'll get a URL like `yourapp.streamlit.app`

---

## Architecture

```
Resume PDF ──────┐
                 ↓
              Gemini API  →  5-Step Analysis  →  Tabbed Results
                 ↑                                    ↓
Job Description ─┘                           Voice Mock Interview
                                             (TTS + Mic + Gemini)
```

### 5 AI Analysis Passes
1. **Fit Scoring** — resume vs JD alignment
2. **Question Prediction** — with probability and category
3. **Concern Identification** — interviewer red flags
4. **Resume Stress Test** — attacks claims for credibility
5. **Follow-up Chains** — multi-turn drill-down simulation

### Voice Interview
- **AI speaks** → Browser SpeechSynthesis API (free, built-in)
- **You speak** → Recorded via `st.audio_input`, sent to Gemini for transcription + evaluation
- **Scoring** → Real-time feedback after every answer

## Tech Stack

| Component | Technology | Cost |
|-----------|-----------|------|
| Frontend | Streamlit | Free |
| AI/LLM | Google Gemini 3.5 Flash | Free tier |
| PDF Parsing | PyPDF | Free |
| Voice TTS | Browser SpeechSynthesis | Free |
| Voice STT | Gemini multimodal audio | Free |
| Hosting | Streamlit Community Cloud | Free |

## Project Structure

```
interview-intelligence/
├── app.py              # Full application (1200+ lines)
├── .env                # API key (local only, not committed)
├── requirements.txt    # Python dependencies
├── .gitignore          # Keeps .env secret out
└── README.md           # This file
```

## Cost

**\$0.** Everything runs on free tiers:
- Google Gemini free tier: 15 requests/minute
- Streamlit Community Cloud: free hosting
- No credit card required anywhere

## License

MIT

---

Built by [AAAaMMbbaarr](https://github.com/AAAaMMbbaarr)
