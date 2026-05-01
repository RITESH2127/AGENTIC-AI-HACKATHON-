# 🚀 Agentic AI Hackathon

<p align="center">
  <b>A production-style, multi-agent intelligence system for discovering high-signal engineering trends and converting them into investment-grade research briefs.</b>
</p>

<p align="center">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-API%20Gateway-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img alt="Groq" src="https://img.shields.io/badge/LLM-Groq-f55036?style=for-the-badge" />
  <img alt="SQLite" src="https://img.shields.io/badge/Storage-SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" />
  <img alt="MIT License" src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" />
</p>

---

## ✨ What This Project Is

**Agentic AI Hackathon** is a modular autonomous research pipeline that behaves like a mini analyst team:

1. **Scout Agent** ingests and filters noisy tech/news signals.
2. **GitHub Quant Agent** performs repository-level quantitative analysis.
3. **Partner Agent** drafts strategic narrative memos from structured evidence.
4. **FastAPI Gateway** orchestrates execution, persistence, security checks, and UI delivery.

The result: from raw internet chatter to a clean, reasoned, and evidence-backed output stream.

---

## 🧠 Why It Stands Out

- **Agent specialization over monolithic prompting**: each module has a constrained role and typed outputs.
- **Rate-limit aware LLM key pooling**: automatic key rotation and reset handling for resilience.
- **Signal-over-hype architecture**: explicit logic discourages funding-news noise and marketing fluff.
- **Quant + narrative blend**: hard repo metrics plus explainable memo synthesis.
- **Live operational interface**: a richly styled HTML terminal-like dashboard.

---

## 🏗️ Architecture at a Glance

```text
Hacker News / RSS / Manual Input
            │
            ▼
     Agent 1: Scout
 (classify SIGNAL vs NOISE)
            │
            ▼
  Agent 2: GitHub Quant
 (velocity, issues, profile)
            │
            ▼
   Agent 3: Partner Memo
 (strategic write-up + thesis)
            │
            ▼
 FastAPI Gateway + SQLite + UI
```

---

## 🤖 Core Agents

### 1) Agent Scout (`agent1_scout.py`)
- Ingests candidate items from supported sources.
- Extracts GitHub URLs from text.
- Uses strict JSON-formatted classification via LLM.
- Buckets items into **SIGNAL** and **NOISE**.

### 2) GitHub Quant (`agent2_github_quant.py`)
- Queries GitHub GraphQL for repository metrics.
- Computes commit velocity windows (30/60/90 day style trends).
- Evaluates issue-resolution behavior.
- Builds structured enrichment artifacts for downstream synthesis.

### 3) Partner Agent (`agent3_partner.py`)
- Converts structured evidence into memo-ready context blocks.
- Produces narrative output designed for strategic decision support.
- Keeps provenance tied to upstream signal and metrics.

### 4) API Gateway (`server.py` + `api_gateway.py`)
- Provides orchestration and endpoint surface.
- Handles Groq key management and failover.
- Adds message safety guardrails and runtime state tracking.
- Stores/retrieves data with SQLite (`researchers.db`).

---

## 🎨 Frontend Experience

The `index.html` interface is intentionally crafted as a **Signal Terminal** with:
- Elegant typography + premium card aesthetics.
- Multi-theme modes (including cyberpunk style).
- Pipeline controls and live chat/analysis panes.
- A visual experience that feels like an operations cockpit, not a plain demo page.

---

## 📦 Project Structure

```bash
.
├── agent1_scout.py
├── agent2_github_quant.py
├── agent3_partner.py
├── api_gateway.py
├── server.py
├── index.html
├── requirements.txt
├── LICENSE
└── README.md
```

---

## ⚙️ Quick Start

### 1) Clone
```bash
git clone https://github.com/ritesh2127/agentic-ai-hackathon-.git
cd agentic-ai-hackathon-
```

### 2) Create virtual environment
```bash
python -m venv .venv
source .venv/bin/activate
# Windows (PowerShell): .venv\Scripts\Activate.ps1
```

### 3) Install dependencies
```bash
pip install -r requirements.txt
```

### 4) Configure environment
Create a `.env` file in project root:

```env
# Required (single key or pool)
GROQ_API_KEY=your_groq_key_here
# OR
GROQ_API_KEYS=key1,key2,key3

# Optional (enables live GitHub quant instead of fallback/mock paths)
GITHUB_TOKEN=your_github_token_here
```

### 5) Run the API server
```bash
uvicorn server:app --reload
```

Then open:
- App/UI: `http://127.0.0.1:8000`
- API docs: `http://127.0.0.1:8000/docs`

---

## 🔐 Environment Variables

| Variable | Required | Purpose |
|---|---:|---|
| `GROQ_API_KEY` | Yes* | Single Groq key |
| `GROQ_API_KEYS` | Yes* | Comma-separated key pool |
| `GITHUB_TOKEN` | Optional | Enables GitHub GraphQL live metrics |

> \* At least one Groq key source is required.

---

## 🧪 Suggested Developer Workflow

```bash
# 1) install deps
pip install -r requirements.txt

# 2) run app
uvicorn server:app --reload

# 3) trigger pipeline from UI and inspect outputs
```

If you are extending the system:
- Add new agents as isolated modules with explicit schemas.
- Keep orchestration concerns in gateway/server layers.
- Preserve traceability from raw item → quant evidence → memo text.

---

## 🛡️ Design Principles

- **Deterministic interfaces, probabilistic internals**
- **Structured outputs before beautiful prose**
- **Safety checks before assistant responses**
- **Graceful degradation under API limits**
- **Composable agent ecosystem for future expansion**

---

## 🗺️ Roadmap Ideas

- Add pluggable sources (Reddit, arXiv, Product Hunt, dev newsletters).
- Add scoring dashboards and historical signal performance.
- Introduce eval harness for agent output quality.
- Add Docker and CI for one-command reproducibility.

---

## 🤝 Contributing

PRs are welcome. If you contribute:
1. Keep modules focused and typed.
2. Document new endpoints/flows.
3. Preserve UX quality in the terminal dashboard.
4. Avoid breaking current pipeline contracts.

---

## 📄 License

This project is licensed under the **MIT License**. See [`LICENSE`](LICENSE) for details.

---

## 🌟 Final Note

This repository is more than a hackathon prototype—it is a foundation for **autonomous research operations** where specialized AI agents collaborate to transform weak signals into sharp, actionable intelligence.

If you like it, give it a ⭐ and build your own agent squad on top.
