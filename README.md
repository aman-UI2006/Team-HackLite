🎙️ MeetPulse — AI-Powered Live Meeting Intelligence System

DevClash 2026 | Problem Statement 4
Turning conversations into real-time structured intelligence

📌 Table of Contents
Overview
Features
Tech Stack
Architecture
How It Works
Quick Start
Environment Variables
Core Modules
Unique Innovations
Future Scope
Contributing
License
🚀 Overview

MeetPulse is a next-generation AI meeting assistant that runs seamlessly alongside Google Meet, Zoom, and Microsoft Teams.

Unlike traditional tools that only record meetings, MeetPulse:

Understands conversations in real-time
Extracts actionable insights
Tracks unresolved discussions across sessions

It acts like a live AI co-pilot for meetings — helping teams stay aligned, productive, and accountable.

✨ Features
🎤 Live Transcription
Real-time speech-to-text using Deepgram Nova-2
Speaker diarization (who said what)
Low-latency streaming via WebSockets
🧠 AI Intelligence Extraction
Powered by Groq Llama 3 models
Automatically detects:
✅ Action Items
📌 Decisions
❓ Open Questions
Assigns responsibility + priority
📋 Live Summary Engine
Rolling summary updated every few sentences
Helps users stay focused without missing context
📸 Smart Screenshot Detection
Detects visual changes:
Slides
Diagrams
Screen shares
Captures and stores with timestamps
🔁 Meeting Debt Tracker (🚀 Core Innovation)
Tracks unresolved topics across meetings
Prevents repeated discussions without closure
Builds long-term team memory
📄 AI Meeting Debrief
Generated at meeting end
Includes:
Summary
Action items
Decisions
Questions
Full transcript
💾 Persistent Storage
Stored in MongoDB Atlas
Enables:
Cross-meeting insights
Historical tracking
Data retrieval
🛠️ Tech Stack
Frontend (Extension)
Chrome Extension (MV3)
JavaScript (Vanilla)
Sidebar UI (Google-style UX)
Backend
FastAPI (Python)
WebSockets (real-time streaming)
Async processing
AI & Data
Groq Llama 3 (8B + 70B)
Deepgram Nova-2 (Speech-to-Text)
MongoDB Atlas
🏗️ Architecture
Chrome Extension (MV3)
├── background.js      → Audio capture + message routing
├── offscreen.js       → Microphone + Deepgram streaming
├── content.js         → Sidebar injection + screenshot detection
├── sidebar.html/js    → Live UI dashboard
└── popup.html/js      → Control interface

FastAPI Backend
├── main.py            → WebSocket handler + orchestration
├── ai/
│   ├── groq_client.py → AI inference
│   └── prompts.py     → Structured prompts
├── db/mongo.py        → MongoDB client
├── routes/
│   ├── meetings.py    → Meeting APIs
│   ├── debrief.py     → Debrief generation
│   └── debt_log.py    → Cross-session tracking
└── models.py          → Data schemas
⚙️ How It Works
🎙️ User joins a meeting (Meet / Zoom / Teams)
🔊 Audio is captured via Chrome Extension
📡 Stream sent to Deepgram for transcription
🧠 AI processes transcript using Groq
📊 Sidebar displays:
Live transcript
Action items
Summary
📸 Screenshots captured on visual change
📄 Final debrief generated after meeting
🚀 Quick Start
1️⃣ Start Backend
cd backend
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
python main.py

Backend:

http://localhost:8000

Docs:

http://localhost:8000/docs
2️⃣ Load Extension
Open chrome://extensions
Enable Developer Mode
Click Load Unpacked
Select /extension folder
3️⃣ Use in Meeting
Join meeting
Click MeetPulse extension
Press Start AI Capture
View real-time insights
🔐 Environment Variables

Create .env in backend:

GROQ_API_KEY=your_key
DEEPGRAM_API_KEY=your_key
MONGO_URI=your_mongodb_uri
🧩 Core Modules
🔹 Transcription Engine
Real-time streaming via WebSockets
Partial + final transcript handling
🔹 AI Processing Layer
Prompt-engineered extraction
Structured JSON outputs
🔹 Intelligence Engine
Action detection
Topic clustering
Meeting memory system
🔹 UI System
Sidebar dashboard
Live updates
Minimal, clean UX
💡 Unique Innovations
🔁 Meeting Debt Tracking (rare feature)
⚡ Real-time AI processing (not post-meeting)
🧠 Context-aware extraction (not keyword-based)
📊 Structured intelligence instead of raw notes
🚧 Future Scope
🔗 Integration with Notion / Jira
📊 Meeting analytics dashboard
🌍 Multilingual support
👥 Team collaboration insights
🤖 Fine-tuned enterprise AI models
🤝 Contributing

We welcome contributions!

fork → clone → branch → commit → PR 🚀
📜 License

MIT License

🧠 Vision

Meetings shouldn’t be forgotten conversations.
They should become structured intelligence that drives execution.

⭐ Support

If you find this project useful:

⭐ Star the repo
🍴 Fork it
🧠 Contribute
👨‍💻 Built For
Hackathons (DevClash 2026)
Productivity tools
AI-powered SaaS products
Real-world enterprise workflows
