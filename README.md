# ✨ OSS Signal

## Autonomous VC Intelligence Engine (AGENTIC-FORAGER)

> Not just software — an always-on, thinking system that scouts the internet, evaluates innovation like an engineer, and decides like an investor.

---

## 🌌 What is OSS Signal?

In a world drowning in information, **OSS Signal** extracts clarity.

It is a fully autonomous, multi-agent intelligence pipeline that continuously scans the open web, detects high-value engineering breakthroughs, validates them with real-world data, and transforms them into **investment-grade insights** — all in real time.

Every 30 minutes, it thinks.
Every cycle, it learns.
Every output, it decides.

---

## ⚡ The Core Loop (How It Thinks)

```
Discover → Filter → Quantify → Synthesize → Stream
```

Behind this simple flow lies a powerful system:

1. **Discovery** — Tracks emerging signals from Hacker News
2. **Filtering** — Eliminates noise using AI judgment
3. **Quantification** — Pulls real GitHub metrics
4. **Synthesis** — Produces structured VC memos
5. **Streaming** — Delivers insights live via dashboard

---

## 🧠 System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                     Intelligence Engine                     │
│                        (FastAPI Core)                      │
│                                                             │
│   Trigger     Stream     Chat                              │
│    │            │          │                               │
│    ▼            ▼          ▼                               │
│ ┌───────────────────────────────────────────────────────┐  │
│ │            Autonomous Orchestration Loop              │  │
│ │                                                       │  │
│ │   HackerNews → Scout → Quant → Partner               │  │
│ └───────────────────────────────────────────────────────┘  │
│                                                             │
│   API Gateway · Key Pool · LLM Proxy · Secrets Manager      │
│                                                             │
│   SQLite DB · GitHub GraphQL · Safety Guardrail             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🤖 The Agents (Where Intelligence Emerges)

### 🛰 Agent 1 — The Scout

**“Find signal in chaos.”**

The Scout operates at the edge of noise. It scans raw internet content and filters out everything except meaningful engineering breakthroughs.

**What it does:**

* Detects GitHub-linked discussions
* Filters weak or irrelevant posts
* Classifies into `SIGNAL` or `NOISE`
* Explains *why* something matters

It doesn’t just see — it **judges**.

---

### 📊 Agent 2 — The Quantitative Engineer

**“Replace opinion with data.”**

Once a signal is detected, the Quant validates it using real-world metrics from GitHub.

**It measures:**

* 🚀 **Commit Velocity** → Is development accelerating?
* 🛠 **Issue Resolution** → Are maintainers responsive?
* 📦 **Repository Strength** → Adoption, scale, ecosystem

It transforms intuition into **evidence**.

---

### 🧾 Agent 3 — The Partner

**“Think like a venture capitalist.”**

The Partner synthesizes everything into a structured investment memo.

**Every memo answers:**

* What is the core innovation?
* Is developer momentum real?
* Are maintainers reliable?
* How strong is the signal?
* What are the risks?
* Should we invest?

**Final verdict:**

* 🟢 HIGH CONVICTION BUY
* 🟡 MONITOR
* 🔴 PASS

It doesn’t describe — it **decides**.

---

## ⚙️ Infrastructure (Built for Reality)

### 🔑 API Gateway

* Multi-key rotation (no downtime under limits)
* Intelligent failover
* Secure secrets handling

---

### 🚀 FastAPI Engine

* Fully asynchronous
* Background autonomous loop
* Real-time streaming via SSE

---

### 🖥 Frontend (Zero Build)

* Live signal feed
* Interactive investment cards
* Deep-dive memo viewer
* Ecosystem graph visualization
* Context-aware AI chat

Everything updates instantly — no refresh, no delay.

---

## 🔐 Security (Intelligence with Boundaries)

Every user interaction is screened using an AI guardrail system:

* Prevents prompt injection
* Blocks jailbreak attempts
* Stops data leakage
* Filters harmful queries

**Design Philosophy:**

> Availability first. Safety enforced intelligently, not blindly.

---

## 🧬 Data Flow (From Raw Data to Decisions)

```
RawItem → ClassifiedItem → EnrichedItem → Investment Memo
```

Each stage:

* Adds structure
* Adds intelligence
* Reduces uncertainty

By the end, noise becomes **clarity**.

---

## 📡 API Surface

| Method | Endpoint              | Purpose                  |
| ------ | --------------------- | ------------------------ |
| GET    | `/`                   | Dashboard                |
| GET    | `/api/stream`         | Live pipeline feed       |
| POST   | `/api/run`            | Trigger analysis         |
| GET    | `/api/status`         | System health            |
| GET    | `/api/results`        | All outputs              |
| POST   | `/api/chat`           | Context-aware AI chat    |
| POST   | `/api/ecosystem/map`  | Generate ecosystem graph |
| POST   | `/api/waitlist`       | Join access list         |
| GET    | `/api/waitlist/stats` | Insights                 |

---

## 🛠 Setup

### Requirements:

* Python 3.11+
* Groq API Key
* (Optional) GitHub Token

### Installation:

```bash
pip install -r requirements.txt
pip install uvicorn python-dotenv
```

---

## ⚙️ Configuration

Create `.env`:

```env
GROQ_API_KEYS=key1,key2,key3
GITHUB_TOKEN=your_token_here
```

---

## ▶️ Run the System

```bash
python server.py
```

or:

```bash
uvicorn server:app --host 0.0.0.0 --port 8000
```

Open:

```
http://localhost:8000
```

---

## 🧪 Run Agents Individually

```bash
python agent1_scout.py
python agent2_github_quant.py
python agent3_partner.py
```

---

## 📁 Project Structure

```
.
├── agent1_scout.py
├── agent2_github_quant.py
├── agent3_partner.py
├── api_gateway.py
├── server.py
├── index.html
├── requirements.txt
├── .env
└── researchers.db
```

---

## ⚖️ Design Philosophy

This system was built with intentional trade-offs:

* ⚡ **Speed over complexity** → Single GraphQL calls
* 🔁 **Resilience over fragility** → Multi-key rotation
* 🧠 **Reasoning over output** → Structured LLM decisions
* 📊 **Transparency over polish** → Verbatim data gaps
* 🔓 **Availability over rigidity** → Fail-open guardrails

---

## 🏁 Closing Thought

OSS Signal is not a dashboard.
It’s not just automation.
It’s not just AI.

It is a **self-operating intelligence layer** —
one that watches the frontier of engineering,
understands it deeply,
and converts it into decisions that matter.

---

## 💡 Built With

FastAPI · Groq · GitHub GraphQL · Pydantic · SQLite

---

> *“In a world full of noise, OSS Signal listens only to what matters.”*
