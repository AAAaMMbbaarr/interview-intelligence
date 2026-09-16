# 🎯 Interview Intelligence Agent

> **An end-to-end AI career intelligence platform that predicts exact interview questions, stress-tests candidate claims, and conducts real-time voice mock interviews tailored to your resume and job description.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Streamlit%20Cloud-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://interview-intelligence-evmru5zdac3kcsqsfqcsu9.streamlit.app/)
[![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Google Gemini](https://img.shields.io/badge/Google%20Gemini-Multimodal%20LLM-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

👉 **[Launch Live Application](https://interview-intelligence-evmru5zdac3kcsqsfqcsu9.streamlit.app/)**

---

## 💡 The Problem

Standard interview preparation platforms generate generic question banks (*"Tell me about a time you faced a challenge..."*). In reality, interviewers scrutinize **your specific resume** line-by-line against **the target company's job requirements**.

**Interview Intelligence Agent bridges this gap.** It acts as an elite technical recruiter and hiring manager to anticipate high-probability questions, uncover unspoken red flags, attack ambiguous resume claims, and put you in the hot seat with an interactive voice interviewer.

---

## ✨ Key Capabilities

| Feature | Description |
|---|---|
| 📊 **Role Alignment & Fit Score** | Quantifies profile match (0–100%) and extracts immediate strengths and critical skill gaps. |
| 🎯 **Targeted Question Prediction** | Predicts top 10 questions with probability scoring (50–99%), categorized by *Resume→JD*, *JD→Gap*, *Resume Suspicion*, and *Transition*. |
| ⚠️ **Interviewer Concern Radar** | Surfaces unspoken risks and skepticism recruiters will have, with concrete mitigation strategies. |
| 🥊 **Skeptical Attack Mode** | Puts resume claims through rigorous stress tests, simulating senior interviewers probing for depth. |
| 🔗 **Multi-Turn Follow-Up Chains** | Generates multi-layered questioning trees, revealing the "traps" interviewers set and the ideal response arcs. |
| 🎤 **Interactive Voice Mock Interview** | Live speech-to-speech mock interview. The AI speaks questions aloud, listens to candidate mic input, transcribes accurately, and scores every response in real time. |

---

## 🕹️ Product Walkthrough

```
  ┌─────────────────┐       ┌─────────────────┐
  │   Resume (PDF)  │  ───► │  Job Spec / JD  │
  └────────┬────────┘       └────────┬────────┘
           │                         │
           └────────────┬────────────┘
                        ▼
       ┌─────────────────────────────────┐
       │   5-Stage AI Intelligence Engine │
       │  • Cross-referenced Fit Score   │
       │  • Question Probability Matrix   │
       │  • Concern & Risk Detection     │
       │  • Claim Verification & Attack  │
       │  • Adaptive Follow-Up Chains    │
       └────────────────┬────────────────┘
                        ▼
       ┌─────────────────────────────────┐
       │   Interactive Executive Suite    │
       │  • Detailed Tabbed Breakdown    │
       │  • Downloadable Markdown Brief   │
       │  • Real-Time Voice Simulation   │
       └─────────────────────────────────┘
```

### 1. Unified Ingestion
Upload any standard PDF resume and either paste the job description or upload JD documents (.pdf / .txt) with instant text preview.

### 2. Multi-Pass Reasoning Pipeline
Executes five concurrent structured analysis routines via Google Gemini with strict schema enforcement to generate deterministic, actionable metrics.

### 3. Voice-Driven Simulation Room
- **Audio Out**: Dynamic browser-level SpeechSynthesis voices prompt the candidate naturally.
- **Audio In**: Multimodal audio recording captures the candidate's spoken response and sends raw bytes to Gemini for accurate transcription and performance scoring.
- **Instant Rubric**: Delivers an objective Score (1–10), Highlights (what worked), Vulnerabilities (what fell short), and actionable improvement tips.

---

## 🛠️ Engineering Architecture & Tech Stack

- **Application Frontend**: Streamlit with custom CSS design, optimized layout, responsive cards, and dynamic state machines.
- **Reasoning Engine**: Google Gemini Models (`gemini-3.5-flash` with dynamic fallback chain to `gemini-3.5-flash-lite` and `gemini-3.1-flash-lite`).
- **Resilience Engine**: Built-in automatic retry backoff and high-availability model routing to ensure zero-downtime during peak API spikes.
- **Multimodal Audio Processing**: Gemini Audio API for direct audio ingestion without external third-party transcription dependencies.
- **Client Speech Synthesis**: Native Web Speech API integration for zero-latency voice generation.
- **Document Extraction**: Stream-based PyPDF text extraction.
- **Zero-Cost Deployment**: Optimized for Streamlit Community Cloud without requiring high-cost infrastructure.

---

## ⚙️ Quick Start (Local Development)

If you wish to run or customize this project locally:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AAAaMMbbaarr/interview-intelligence.git
   cd interview-intelligence
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Environment:**
   Create a `.env` file in the root directory:
   ```env
   GOOGLE_API_KEY=your_gemini_api_key_here
   ```
   *(Obtain a free API key at [Google AI Studio](https://aistudio.google.com/apikey))*

4. **Launch Application:**
   ```bash
   streamlit run app.py
   ```

---

## 🌐 Production Deployment

This application is ready for 1-click deployment on **Streamlit Community Cloud**:

1. Fork or push to your GitHub repository.
2. Sign in to [Streamlit Community Cloud](https://share.streamlit.io).
3. Select `app.py` as the entrypoint.
4. Add `GOOGLE_API_KEY` in **App Settings ➔ Secrets**.
5. Deploy and share your live application URL with recruiters and hiring managers!

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

<div align="center">
  <b>Engineered by <a href="https://github.com/AAAaMMbbaarr">AAAaMMbbaarr</a></b><br>
  <i>Empowering candidates with AI-powered hiring intelligence.</i>
</div>
