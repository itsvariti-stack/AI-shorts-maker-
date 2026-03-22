# 🎬 ShortsAI Agent

> Automatically generate viral YouTube Shorts — script, visuals, voice, subtitles & video — powered by AI agents.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🧠 AI Script Agent | GPT-4o generates viral hooks + retention-optimized scripts |
| 🎨 Scene Generator | Cinematic DALL·E image prompts per scene |
| 🎙️ Voiceover | ElevenLabs TTS synced to scenes |
| 📽️ Video Generation | Runway/Replicate clip generation |
| 📝 Auto Subtitles | Word-by-word animated captions |
| 📤 Export | 1080×1920 MP4, YouTube-ready |
| 📊 Dashboard | History, re-edit, viral metadata |

---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- npm or yarn

### 1. Clone & Install

```bash
git clone <repo-url>
cd shortsai

# Install server deps
cd server && npm install

# Install client deps
cd ../client && npm install
```

### 2. Configure Environment

```bash
cp .env.example server/.env
```

Edit `server/.env` with your API keys.

### 3. Run Development

```bash
# Terminal 1 — Backend
cd server && npm run dev

# Terminal 2 — Frontend
cd client && npm run dev
```

Open [http://localhost:5173](http://localhost:5173)

---

## 🔑 API Keys Required

| Service | Purpose | Get Key |
|---|---|---|
| OpenAI | Script + hooks + image prompts | [platform.openai.com](https://platform.openai.com) |
| ElevenLabs | AI voiceover | [elevenlabs.io](https://elevenlabs.io) |
| Replicate | Video generation | [replicate.com](https://replicate.com) |
| Stability AI | Image generation | [stability.ai](https://stability.ai) |

---

## 🗂️ Project Structure

```
shortsai/
├── client/                  # React + Vite + Tailwind
│   └── src/
│       ├── pages/           # Dashboard, TextToShort, ImageToShort
│       ├── components/      # Reusable UI components
│       ├── hooks/           # Custom React hooks
│       └── context/         # Global state
├── server/                  # Express API
│   ├── routes/              # API route handlers
│   ├── services/            # AI service integrations
│   └── middleware/          # Auth, rate limiting
├── .env.example
└── README.md
```

---

## 📡 API Routes

```
POST /api/generate-hook        → Viral hook generation
POST /api/generate-script      → Full script + scenes
POST /api/generate-images      → DALL·E scene images
POST /api/generate-voice       → ElevenLabs TTS
POST /api/generate-video       → Replicate video clips
POST /api/export-video         → Final MP4 assembly
POST /api/viral-metadata       → Titles, hashtags, description
GET  /api/projects             → List saved projects
GET  /api/projects/:id         → Get project details
```

---

## ☁️ Deploy to Vercel

```bash
# Deploy client
cd client
vercel --prod

# Deploy server (as serverless functions or separate service)
cd server
vercel --prod
```

Set environment variables in Vercel dashboard.

---

## 🎨 Content Style Rules

- ⚡ **Fast pacing** — cut every 2-3 seconds
- 🪝 **Strong hooks** — first 3 seconds are everything
- 🔄 **Pattern interrupts** — surprise every 5 seconds
- 💬 **Simple language** — 6th grade reading level
- 🎭 **Dramatic storytelling** — tension + resolution

---

## 📄 License

MIT
