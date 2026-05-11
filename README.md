# 🏆 SportsMind

**SportsMind** is an advanced, real-time AI-powered multi-sport commentary engine. It combines a sophisticated web scraper for live cricket data with cutting-edge Large Language Models (LLMs) to provide exciting, broadcast-style commentary and analysis.

[![Vite](https://img.shields.io/badge/Frontend-Vite%20%2B%20React-646CFF?style=flat-square&logo=vite)](https://vitejs.dev/)
[![Express](https://img.shields.io/badge/Backend-Express%20%2B%20TS-000000?style=flat-square&logo=express)](https://expressjs.com/)
[![Tailwind CSS](https://img.shields.io/badge/Styling-Tailwind%20CSS-38B2AC?style=flat-square&logo=tailwind-css)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

## 🌟 Features

### 🎙️ AI Commentator (Frontend)
- **Live Match Updates:** Real-time data fetching for Cricket, Football, and more.
- **Dynamic AI Commentary:** Generates broadcast-quality commentary using **Gemini 1.5 Flash** and **Llama 3 (via Groq)**.
- **High-Fidelity Audio:** Integrated **ElevenLabs TTS** for realistic voice commentary.
- **Visual Analytics:** Interactive charts (Chart.js) for match momentum and statistics.
- **Multi-Sport Support:** Dedicated sections for Cricket, Football, Basketball, and Tennis.

### 🏏 CricketScrap (Backend)
- **High-Performance Scraper:** Efficiently extracts live scores, commentary, scorecards, and squads from Cricbuzz.
- **Clean JSON API:** Exposes structured endpoints for match details, graphs, and highlights.
- **Advanced Caching:** Multi-tier caching strategy to ensure low latency and bypass rate limits.
- **Playwright Fallback:** Robust scraping with automated browser fallback for complex pages.
- **Health Monitoring:** Built-in system health and performance tracking.

## 🏗️ Architecture

SportsMind is structured as a **Monorepo** for seamless development:

```text
SportsMind/
├── frontend/             # React + Vite application (The UI & AI Logic)
├── backend/              # Node.js + Express + TS (The Scraper & API)
├── .env.example          # Unified environment template
└── package.json          # Root scripts for monorepo management
```

## 🚀 Getting Started

### Prerequisites
- **Node.js:** v18.0.0 or higher
- **npm:** v9.0.0 or higher

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/ByteLounge/SportsMind.git
    cd SportsMind
    ```

2.  **Install all dependencies:**
    ```bash
    npm run install-all
    ```

3.  **Configure Environment Variables:**
    Copy the template and fill in your API keys:
    ```bash
    cp .env.example .env
    ```
    *Required Keys:* `VITE_GEMINI_API_KEY`, `VITE_GROQ_API_KEY`, `VITE_ELEVENLABS_API_KEY`.

### Development

Launch both the frontend and backend concurrently:
```bash
npm run dev
```
- **Frontend:** [http://localhost:5173](http://localhost:5173) (or next available port)
- **Backend:** [http://localhost:3001](http://localhost:3001)

## 🛠️ Tech Stack

- **Frontend:** React, Vite, Tailwind CSS, Lucide React, Chart.js.
- **Backend:** Node.js, Express, TypeScript, Cheerio, Axios, Playwright.
- **AI/ML:** Google Gemini AI, Groq (Llama 3), ElevenLabs TTS.

## 📦 Deployment

### Backend
Deploy the `backend/` directory to **Railway**, **Render**, or any Node.js host. Ensure `CORS_ORIGIN` is set to your frontend URL.

### Frontend
Deploy the `frontend/` directory to **Vercel** or **Netlify**. Set the `VITE_BACKEND_URL` environment variable to point to your deployed backend API.

---

Built with ❤️ by [ByteLounge](https://github.com/ByteLounge)
