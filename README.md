[README.md](https://github.com/user-attachments/files/27048138/README.md)
# 🌊 PulseCity — AI-Powered Citizen Urban Intelligence

> **Hackathon:** Project 2030: MyAI Future Hackathon | Track 4: Green Horizon (Smart Cities & Mobility)
> **Deployed Live:** [Your Cloud Run URL here]

---

## 🚨 The Problem

Kuala Lumpur floods cost millions of ringgit every year. But the tragedy is that the warning signs are everywhere — clogged drains, waterlogged roads, broken infrastructure — reported by citizens on social media, ignored by systems that aren't listening.

**The city has sensors. They're called citizens. Nobody was connecting them.**

---

## 💡 What PulseCity Does

PulseCity turns every Malaysian citizen into a city sensor. You snap a photo of an urban problem — a clogged drain, a flooded road, illegal dumping — and PulseCity's AI does the rest:

1. **Gemini Vision** classifies the issue type and severity in real time
2. **Urgency scoring** routes it to the right department automatically
3. **Pattern recognition** across aggregated reports detects flood hotspots *before* floods happen
4. **Live city dashboard** visualizes urban health across KL in real time

The twist: we don't just log complaints. We **predict urban breakdown** before it becomes a crisis.

---

## 🧠 AI Architecture

| Layer | Technology | Purpose |
|-------|-----------|---------|
| Vision Intelligence | Gemini 1.5 Flash (multimodal) | Photo → issue classification + urgency score |
| Prediction Engine | Gemini 1.5 Pro + RAG | Pattern recognition across historical reports |
| Orchestration | Firebase Genkit | Agentic multi-step AI workflow |
| Context & Memory | Vertex AI Search | Grounded RAG over KL flood/infrastructure data |
| Deployment | Google Cloud Run | Serverless, scalable, live |

### How the AI pipeline works:
```
User uploads photo
       ↓
Gemini Vision API → classifies issue (drain/pothole/flooding/dumping)
       ↓
Urgency scorer → assigns priority 1–5
       ↓
Department router → maps to correct city department
       ↓
Pattern aggregator → checks if cluster of similar reports nearby
       ↓
Flood risk predictor → flags hotspot if threshold crossed
       ↓
Dashboard update → real-time city health map
```

---

## 🛠️ Tech Stack

**Backend**
- Python (FastAPI)
- Google Gemini API (Vision + Text)
- Firebase Genkit (agentic orchestration)
- Google Cloud Run (deployment)
- Vertex AI Search (RAG)

**Frontend**
- React + Vite
- Deployed on Vercel / Cloud Run

**AI Tools Used**
- Google AI Studio (prototyping)
- Gemini 1.5 Flash (image classification)
- Gemini 1.5 Pro (prediction reasoning)

---

## 🚀 Setup & Run Locally

### Prerequisites
- Python 3.11+
- Node.js 18+
- Google Cloud account
- Gemini API key

### Backend
```bash
git clone https://github.com/YOUR_USERNAME/pulsecity
cd pulsecity/backend

# Install dependencies
pip install -r requirements.txt

# Set environment variables
cp .env.example .env
# Add your GEMINI_API_KEY to .env

# Run locally
uvicorn main:app --reload
```

### Frontend
```bash
cd pulsecity/frontend
npm install
npm run dev
```

### Test the API
```bash
# Health check
curl https://YOUR_CLOUD_RUN_URL/api/stats

# Submit a report (with image)
curl -X POST https://YOUR_CLOUD_RUN_URL/api/report \
  -F "image=@test_drain.jpg" \
  -F "location=Chow Kit, KL"
```

---

## 📁 Project Structure

```
pulsecity/
├── backend/
│   ├── main.py              # FastAPI app entry point
│   ├── gemini_vision.py     # Image classification with Gemini
│   ├── urgency_scorer.py    # AI urgency scoring logic
│   ├── flood_predictor.py   # Pattern-based flood risk detection
│   ├── router.py            # Department routing logic
│   ├── Dockerfile           # Cloud Run deployment
│   └── requirements.txt
├── frontend/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── components/
│   │   │   ├── ReportForm.jsx      # Photo upload + submission
│   │   │   ├── CityDashboard.jsx   # Real-time map view
│   │   │   └── AlertCard.jsx       # Flood warning component
│   │   └── index.css
│   └── package.json
└── README.md
```

---

## 🎯 Key Features

- 📸 **One-tap reporting** — snap photo, AI does the rest
- 🔍 **Gemini multimodal classification** — identifies 6 issue types
- ⚡ **Real-time urgency scoring** — 1–5 priority scale
- 🗺️ **Live city health map** — visual dashboard of KL
- 🌊 **Flood prediction** — hotspot detection before crisis hits
- 🏛️ **Auto-routing** — right issue to right department

---

## 🇲🇾 National Alignment

PulseCity directly addresses Malaysia's national agenda:
- **MyDIGITAL Blueprint** — End-to-end digital civic services
- **Net Zero 2050 / NKRA** — Smart infrastructure monitoring
- **Malaysia Madani** — Citizen-first, technology-enabled governance

---

## ⚠️ AI Usage Disclosure

This project uses AI-generated code assistance (Gemini, GitHub Copilot). All code has been reviewed, understood, and is fully defensible by the team. No copyrighted datasets were used. All AI outputs are grounded in public infrastructure data.

---

## 👥 Team

| Name | Role |
|------|------|
| ANI YASSIR | Backend + AI pipeline |
| HANAN NASR| Frontend + UI/UX |
| AYA ABUALGASIM| Deployment + Pitch |

---

## 📄 License

MIT License — open source and free to build upon.

---

*Built for Project 2030: MyAI Future Hackathon | Google Developer Groups On Campus UTM*
*"Advancing the Nation by Building Solutions with Google AI"*
