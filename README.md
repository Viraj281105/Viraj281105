<!-- HUD HEADER SYSTEM -->
<p align="center">
  <img width="100%" src="./hud-header.svg" alt="HUD Diagnostic System Header" />
</p>

<!-- DYNAMIC TELEMETRY TAGLINE -->
<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3500&pause=1000&color=00F0FF&center=true&vCenter=true&width=750&lines=System+Protocol%3A+Full-Stack+Engineering+%7C+Causal+%26+Multi-Agent+AI;Status%3A+Production-Grade+AI+Systems+%7C+Spring+Boot+%2B+FastAPI+Backends;Ingestion%3A+Tri-Service+Microservices+%7C+High-Throughput+Vector+Search;Query%3A+Entailment-Calibrated+Hallucination+Detection" alt="System Diagnostics Typewriter" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CORE_CAPABILITY-FULL_STACK_AI_SYSTEMS-00f0ff?style=for-the-badge&labelColor=0d1117" />
  <img src="https://img.shields.io/badge/ORCHESTRATION-LANGGRAPH%20%2F%20MULTI--AGENT-a855f7?style=for-the-badge&labelColor=0d1117" />
  <img src="https://img.shields.io/badge/BACKEND-SPRING%20BOOT%20%2B%20FASTAPI-6366f1?style=for-the-badge&labelColor=0d1117" />
</p>

---

### 💻 SYSTEM ACTIVE // CORE STATUS

<p align="center">
  <img width="100%" src="./diag-terminal.svg" alt="System Diagnostic Logs" />
</p>
---

## 🛠️ ARCHITECTURAL STACK & PIPELINES

<blockquote>
<b>Engineering Directive:</b> Build scalable, evidence-grounded AI systems from mathematical formulation up to containerized microservice architectures — full-stack, end to end.
</blockquote>

### 🧑‍💻 Core Languages
`Python` `Java` `TypeScript` `C++`

### 🧠 Causal Inference & Probabilistic AI
* **Frameworks & Orchestration:** `DoWhy` | `LangGraph` | `LangChain` | `PyTorch` | `scikit-learn` | `Hugging Face Transformers`
* **Foundational Mechanics:** Structural Causal Models (SCMs), Backdoor/Frontdoor Identifiability, Average & Conditional Average Treatment Effect (ATE/CATE) Estimation under distribution shift, Rosenbaum bounds sensitivity metrics, E-value sensitivity diagnostics, probabilistic calibration curves (ECE)
* **Generative & Representation Learning:** LoRA adapter fine-tuning, conditional GANs (Pix2Pix U-Net/PatchGAN), Text-to-Image synthesis (Stable Diffusion), Neural Style Transfer (VGG-19 feature optimization), `sentence-transformers` embedding pipelines
* **Applied ML & Forecasting:** Isolation Forest anomaly detection, time-series risk/cash-flow forecasting, schema-aware NLP-to-SQL query generation
* **Explainability & Trust:** SHAP feature attribution, entailment-based hallucination detection (NLI formulation), zero-hallucination RAG citation schemas

### 🎨 Frontend & Interactive UI
* **Core Frameworks:** `React` | `Next.js 15`
* **Styling & State Management:** `Tailwind CSS` | `Zustand`
* **Data Visualization & Motion:** `Recharts` | `D3.js` | `Plotly` | `Framer Motion` | `Mapbox`
* **UX Patterns:** live SSE-driven streaming interfaces, real-time geospatial dashboards, animated multi-step agent execution views

### ⚙️ Distributed Systems & Backend
* **Microservices:** `Spring Boot` (Java) | `FastAPI` (Python) | `Flask` | `Node.js`
* **APIs & Auth:** RESTful API design, JWT-based authentication, async request handling, schema validation
* **Architecture Patterns:** decoupled write-heavy ingestion vs. query-heavy retrieval pipelines, Server-Sent Events (SSE) streaming, asynchronous event brokers via Redis Streams, tri-service/multi-service orchestration
* **Infrastructure & Tooling:** `Docker` | `Docker Compose` | `Nginx` | SSL/TLS reverse proxying, `Linux`, `Git`, production-grade serving configs

### 🗄️ Database & Retrieval Engineering
* **Vector & Relational Engines:** `pgvector` (PostgreSQL) | `FAISS` (dense vector search) | `MongoDB` | `Redis` caching
* **Geospatial:** `PostGIS` | `Mapbox`
* **Search Paradigms:** hybrid sparse-dense index merging (BM25 + dense embeddings), sub-second semantic retrieval over multi-million-record clusters, dynamic parameter-bound geospatial query execution, schema-aware NL-to-SQL translation
---

## 🛰️ CURRENTLY BUILDING

## 🏥 AROGYARAKSHAK — AI-Driven Patient Advocacy Platform

> **Status:** Guide-approved, in implementation · **Context:** Final Year Engineering Project (Team of 5) · **Institution:** PES Modern College of Engineering, Pune (SPPU 2019 Pattern)

**The problem:** Healthcare in India isn't hard to navigate because care is unavailable — it's hard because the systems *around* care are fragmented and opaque. Hospital bills are near-impossible for a patient to validate against regulatory benchmarks, government health schemes are buried across dense multilingual documentation nobody reads end to end, and medicine prices vary in ways patients have no way to catch.

**How it works:**

Any Document (bill / prescription / rejection letter) │ Shared Extraction Agent │ Kadi — Shared Case Context Layer │            │            │ BillNyay    SchemeSetu    DawaCheck (bill audit  (scheme       (medicine

- appeal)   eligibility)   pricing)

One upload feeds all three modules — a patient never re-uploads the same document twice.

**The three modules:**
- **BillNyay** *("Nyay" = justice)* — OCR extracts line items from a hospital bill, benchmarks them against CGHS government rate schedules, flags overcharges, and runs a 5-agent pipeline (Document Auditor → Clinical Reviewer → Regulatory Advisor → Appeal Drafter → QA Judge) to draft an IRDAI-compliant appeal letter as a downloadable PDF. Carries forward and refines an existing hackathon build rather than starting from scratch.
- **SchemeSetu** — A short intake or a bill/prescription upload triggers a RAG layer over PMJAY (national) and MJPJAY (Maharashtra state) scheme documents; an agent reasons through eligibility rules and outputs which government scheme(s) apply plus a step-by-step claim guide.
- **DawaCheck** — Upload a medicine strip photo or prescription; OCR reads the drug name/batch and benchmarks the MRP against NPPA ceiling prices for ~800–900 Schedule-I price-controlled formulations, flagging overcharging and suggesting generic substitutes. Deliberately scoped to Schedule-I only — the one segment with a clean, government-published ground-truth price.

**Kadi — the shared context layer** *(कड़ी — "link"):* not a fourth module, but the infrastructure that makes the three modules actually interoperate:
- **Case & entity model** — `cases` / `entities` / `case_entities` tables sit alongside each module's own domain data in one Postgres instance.
- **Entity resolution pipeline** (the project's genuine research contribution): three similarity signals feed one confidence score — string similarity (surface variants like "Paracetamol 650mg" vs "Paracetamol"), **IndicXlit** transliteration matching (AI4Bharat — catches same word, different script, e.g. क्रोसिन ↔ Crocin), and **IndicSBERT** cross-lingual embeddings (L3Cube, Pune — catches translated concepts, e.g. बुखार ↔ Fever). A logistic regression combines all three into one confidence score, routing to merge / ask-user / new-entity.
- **Auto-triggering** — e.g. a bill mentioning a ₹4L cardiac surgery under general category silently checks SchemeSetu eligibility in the background and surfaces it alongside the BillNyay report, without a second upload.
- **Consent boundary** — a user explicitly opts in per-case before SchemeSetu/DawaCheck can see what BillNyay found; nothing is pooled silently by default.

**Multilingual — English, Hindi & Marathi, full scope:** touches OCR (Devanagari needs its own validation pass, separate from English OCR accuracy), UI, LLM output generation, and entity resolution independently — with native-speaker terminology QA on every generated appeal letter and scheme explanation, not just a fluency check.

**Target evaluation metrics** (module-level, from the project's formal evaluation framework):
| Metric | Target |
|---|---|
| Procedure Extraction Accuracy (BillNyay) | >95% |
| Benchmark Mapping Accuracy (BillNyay) | >92% |
| Billing Deviation Detection Precision/Recall | >90% / >90% |
| Average Report Generation Time | <5 seconds |

**Research contribution:** the Kadi entity-resolution ablation (string-only vs. transliteration-only vs. embedding-only vs. combined, measured by precision/recall/F1) is being written up as a standalone research note — no published system combines phonetic transliteration and cross-lingual embeddings specifically for trilingual medical entity linking under OCR noise, which is the genuine open question here.

**Stack:** `FastAPI` `Next.js 15` `PostgreSQL` `pgvector` `FAISS` `Groq (openai/gpt-oss-120b)` `IndicXlit` `IndicSBERT` `Docker Compose`

*(Private repository — full technical documentation maintained separately)*

## 🛡️ FINGUARD AI — AI-Powered Personal Finance Risk Advisor

> **Status:** In active development · **Team:** Viraj Jadhao + Bhumi · **Timeline:** March – July 2026 · *"Know your financial future before it happens."*

**The problem:** Most finance apps tell you where your money *went*. Nothing mainstream tells you where it's *going* — or lets you test a decision before you make it.

**How it works:** Upload a bank statement → AI classifies every transaction → get a Financial Risk Score (0–100) → see a 6-month cash flow forecast → run scenarios like "what if I close my personal loan?" and watch the risk score update instantly.

**Features:**
| Feature | What it does |
|---|---|
| 🧠 AI Expense Classification | Two-stage ML pipeline, **91% accuracy** on Indian bank statements |
| 📊 Financial Risk Score | Composite 0–100 index across 5 weighted dimensions: Liquidity (25%), Debt Burden (25%), Volatility (20%), Savings Stability (20%), Investment Diversification (10%) |
| 📈 Cash Flow Forecasting | 3–12 month predictions with confidence bands, based on actual spending history |
| 🎮 Scenario Simulator | Adjust real parameters (close a loan, increase SIP, cut dining spend) and see the risk score + cash flow shift live |
| 💡 AI Recommendations | Prioritized, severity-ranked action items specific to the user's own data — not generic tips |
| 📤 Bank Statement Import | HDFC, ICICI, SBI, Axis, Kotak supported; async processing, 500 rows classified in under 60 seconds |

**Architecture:** React frontend → Nginx (SSL) → Spring Boot backend (Auth/JWT, Data Ingestion, Risk Scoring, Scenario Engine, AI Gateway) → internal FastAPI AI microservices (`/classify`, `/risk-score`, `/forecast`, `/recommend`) → PostgreSQL + pgvector.

**Backend depth:** Spring Security 6 + JWT, Spring Data JPA/Hibernate/HikariCP, async CSV processing via `CompletableFuture`, Bucket4j rate limiting, Flyway migrations.
**AI/ML depth:** `sentence-transformers/all-MiniLM-L6-v2` embeddings, FAISS similarity search, Isolation Forest anomaly detection, Facebook Prophet forecasting (Phase 2).
**Security:** 15-min JWT access tokens + 7-day HttpOnly refresh cookies, BCrypt (cost 12), rate limiting on every endpoint, parameterized queries only, uploaded CSVs deleted post-parse.

**Stack:** `Spring Boot 3 (Java 21)` `FastAPI (Python 3.11)` `React 18 + TypeScript` `PostgreSQL + pgvector` `Docker Compose` `Nginx + Let's Encrypt`

[![FinGuard AI Repository](https://img.shields.io/badge/Access_Secure_Files-FinGuard_AI-00f0ff?style=for-the-badge&logo=github&labelColor=0d1117)](https://github.com/Viraj281105/Finguard-AI)

## 🔍 AI HALLUCINATION DETECTION APPLICATION — Dual-Judge Fact Verification

> **Status:** Backend operational, frontend in progress · **Architecture:** Retriever + NLI dual-judge system

**The problem:** LLM output is fluent but not reliably grounded. This system treats "is this claim actually supported by evidence" as a formal, explainable verification problem instead of a vibe check.

**How it works:** a "Retriever-Judge" workflow — the **Retriever** (`BAAI/bge-large-en-v1.5`) finds the most relevant evidence in a local vector knowledge base, and the **Judge** (`ynie/roberta-large-snli` — a specialized NLI model) determines whether that evidence *Contradicts* or *Entails* the claim.

**Features:**
- **REST API** — a fully headless FastAPI backend, integrable into any application
- **100% local vector knowledge base** via ChromaDB — no external dependency for retrieval
- **Dockerized & deployable** — containerized for one-command deployment to Render
- *(in progress)* **Dual-judge selection** — choice between a `fast` judge (RoBERTa) and an `accurate` judge (Mistral 7B) for a speed-vs-accuracy trade-off
- *(in progress)* **Live web search fallback** — if the local knowledge base has no relevant evidence
- *(in progress)* **Full-stack UI** — SvelteKit/React frontend deploying on Vercel

**Engineering practice:** built as a complete production-shaped system, not a notebook — includes a CI/CD pipeline (GitHub Actions), a `pytest` test suite, and a tracked `PLAN.md` sprint roadmap, run as a professional Git workflow (branching strategy + commit conventions) despite being a solo project.

**Stack:** `FastAPI` `ChromaDB` `sentence-transformers` `transformers (RoBERTa-large-NLI)` `SvelteKit/React` `Tailwind CSS` `Docker` `Render` `Vercel`

[![AI Hallucination Detection Repository](https://img.shields.io/badge/Access_Secure_Files-Hallucination_Detection-00f0ff?style=for-the-badge&logo=github&labelColor=0d1117)](https://github.com/Viraj281105/AI-Hallucination-Detection-Application)

## 🏦 FINANCIAL INTELLIGENCE PLATFORM — Enterprise NL-to-SQL for Finance

> **Status:** 🚧 Active development — scaffold complete · **Focus:** Governed, explainable natural-language database querying

**The problem:** Analysts and risk teams need to query complex financial databases without waiting on an engineer to write SQL — but a naive NL-to-SQL tool in a financial context is a security and compliance liability, not just a convenience feature.

**Core capabilities:**
- **Natural Language → SQL** via fine-tuned and RAG-augmented LLMs
- **Query validation & safety** enforced before any statement touches the database
- **Explainable outputs** — every generated query ships with a reasoning trace
- **Governance & audit logging** for compliance review
- **Secure multi-tenant API** with role-based access control

**Modular layered architecture:**
| Layer | Responsibility |
|---|---|
| `src/api/` | FastAPI REST endpoints, request routing, auth middleware |
| `src/core/` | Query orchestration, session management |
| `src/llm/` | LLM interface, prompt templates, model loading |
| `src/rag/` | Retrieval-augmented generation, vector store integration |
| `src/sql/` | SQL generation, validation, sanitization, execution |
| `src/security/` | Input/output guardrails, PII detection, injection prevention |
| `src/pipelines/` | End-to-end inference chaining |

**Security-first by design:** SQL injection prevention via sanitization/parameterization, PII detection before any logging or output exposure, prompt-injection guardrails, JWT auth with RBAC, full audit logging on every query execution.

**Stack:** `Python 3.10+` `FastAPI` `HuggingFace Transformers` `Docker Compose` — repo structured with dedicated `docs/architecture/`, `docs/security/`, and `docs/decisions/` (ADRs)

[![Financial Intelligence Platform Repository](https://img.shields.io/badge/Access_Secure_Files-Fin_Intelligence-00f0ff?style=for-the-badge&logo=github&labelColor=0d1117)](https://github.com/Viraj281105/fin-intelligence-platform)

Still open from last time: what to do with **ClimateX**/**FloatChat** (secondary table, or drop), and whether to drop the **DaaviSetu** naming reference for good.

---

## 💼 PROFESSIONAL EXPERIENCE

<details open>
<summary><b>🏢 SAS R&D — Customer Intelligence Department</b></summary>
<br />

> **Role:** Intern · **Duration:** 11 months (July 2, 2026 – onward) · **Engagement:** Full-time, paid

Currently interning in the Customer Intelligence department, working across a technical stack that's confidential to the role. The **Traffic-Simulation** project below was the technical assessment for this position — a demonstration of engineering ability during the evaluation process, not the ongoing work itself, which remains internal.

</details>

<details>
<summary><b>🤖 Prodigy InfoTech — Generative AI Intern</b></summary>
<br />

> **Duration:** Jan 2026 – Feb 2026 · **Format:** Remote

Completed 5 end-to-end generative AI tasks spanning language and vision:

- **Language:** Fine-tuned GPT-2 on a domain-specific corpus using Hugging Face Transformers; implemented N-gram Markov chain text generation from scratch (bigram through weighted n-gram), evaluating trade-offs across generative approaches in text vs. vision.
- **Vision:** Built a conditional GAN (U-Net + PatchGAN) for Pix2Pix image-to-image translation on building facade segmentation; implemented Neural Style Transfer via VGG-19 feature optimization; deployed Stable Diffusion for text-to-image synthesis.

`Hugging Face Transformers` `GPT-2` `Pix2Pix (cGAN)` `Neural Style Transfer` `Stable Diffusion`

</details>

---

## 📊 TELEMETRY FEEDS (LIVE ACTIVITY METRICS)

<table width="100%">
  <tr>
    <td width="50%" align="center">
      <b>SYSTEM METRICS</b><br/><br/>
      <img src="https://github-readme-stats.vercel.app/api?username=Viraj281105&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true&title_color=00f0ff&icon_color=00f0ff&text_color=ffffff&bg_color=0d1117&cache_seconds=1800" width="100%" />
    </td>
    <td width="50%" align="center">
      <b>STREAK ACTIVITY</b><br/><br/>
      <img src="https://streak-stats.demolab.com?user=Viraj281105&theme=tokyonight&hide_border=true&stroke=00f0ff&ring=00f0ff&fire=a855f7&currStreakLabel=00f0ff&background=0d1117" width="100%" />
    </td>
  </tr>
  <tr>
    <td width="50%" align="center">
      <b>CORE SYSTEM LANGUAGES</b><br/><br/>
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Viraj281105&layout=compact&theme=tokyonight&hide_border=true&title_color=00f0ff&text_color=ffffff&bg_color=0d1117&langs_count=8&cache_seconds=1800" width="100%" />
    </td>
    <td width="50%" align="center">
      <b>SYS_ACTIVITY DIAGRAM</b><br/><br/>
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=Viraj281105&theme=tokyo-night&hide_border=true&bg_color=0d1117&color=00f0ff&line=00f0ff&point=ffffff" width="100%" />
    </td>
  </tr>
</table>

---

### 🏆 ACHIEVEMENT MATRIX

<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=Viraj281105&theme=tokyonight&no-frame=true&no-bg=true&margin-w=8&margin-h=8&row=1&column=7" width="100%" />
</p>

---

### 🧬 SYSTEM COMPONENTS — SKILL MATRIX

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,java,ts,cpp,fastapi,spring,react,nextjs,postgres,docker,git,linux&theme=dark&perline=6" />
</p>

---

### 🐍 CONTRIBUTION GRID — LIVE SNAKE FEED

<p align="center">
  <img src="https://raw.githubusercontent.com/Viraj281105/Viraj281105/output/github-contribution-grid-snake-dark.svg" width="100%" />
</p>

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Viraj281105&label=DATASTREAM_READS&color=00f0ff&style=flat-square" />
  <img src="https://img.shields.io/github/followers/Viraj281105?label=NETWORK_NODES&style=flat-square&color=00f0ff" />
  <img src="https://img.shields.io/github/stars/Viraj281105?label=STARS_COLLECTED&style=flat-square&color=a855f7" />
</p>
---

## 📝 CREDENTIAL LOG & FIELD RECORD

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h4>🔑 AI & Cognitive Networks</h4>
      <ul>
        <li><img src="https://img.shields.io/badge/-Google-4285F4?style=flat-square&logo=google&logoColor=white" /> <b>Google × Hack2Skill</b> — 5-Day AI Agents Intensive Course</li>
        <li><img src="https://img.shields.io/badge/-AICTE-FF6F00?style=flat-square" /> <b>AICTE Virtual Internship</b> — Google AI/ML Program</li>
        <li><img src="https://img.shields.io/badge/-Google-4285F4?style=flat-square&logo=google&logoColor=white" /> <b>AI Adventures (Google)</b> — ML, DL & GenAI</li>
        <li><img src="https://img.shields.io/badge/-GUVI-00599C?style=flat-square" /> <b>HCL GUVI</b> — AI/ML Certification</li>
      </ul>
    </td>
    <td width="50%" valign="top">
      <h4>📦 Distributed Architectures</h4>
      <ul>
        <li><img src="https://img.shields.io/badge/-AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white" /> <b>AWS</b> — Cloud Foundations</li>
        <li><img src="https://img.shields.io/badge/-Prodigy_InfoTech-6366f1?style=flat-square" /> <b>Prodigy InfoTech</b> — Generative AI Internship (Jan–Feb 2026)</li>
        <li><img src="https://img.shields.io/badge/-IIT_Bombay-a855f7?style=flat-square" /> <b>IIT Bombay</b> — Core Java Certification</li>
      </ul>
    </td>
  </tr>
</table>

---

## 📡 UPLINK PORTAL

<p align="center">
  <img src="https://img.shields.io/badge/STATUS-OPEN_TO_OPPORTUNITIES-00f0ff?style=for-the-badge&labelColor=0d1117" />
</p>

<p align="center">
  <a href="mailto:viraj.jadhao28@gmail.com">
    <img src="https://img.shields.io/badge/ESTABLISH_UPLINK-EMAIL-00f0ff?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0d1117" />
  </a>
  &nbsp;
  <a href="https://www.linkedin.com/in/viraj-jadhao-0771b830b/">
    <img src="https://img.shields.io/badge/ESTABLISH_UPLINK-LINKEDIN-a855f7?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0d1117" />
  </a>
  &nbsp;
  <a href="https://github.com/Viraj281105">
    <img src="https://img.shields.io/badge/ESTABLISH_UPLINK-GITHUB-6366f1?style=for-the-badge&logo=github&logoColor=white&labelColor=0d1117" />
  </a>
</p>

<p align="center">
  <sub style="color: #52525b">SYSTEM TERMINAL SECURED. ACCESS GRANTED.</sub>
</p>
