<!-- HUD HEADER SYSTEM -->
<p align="center">
  <img width="100%" src="./hud-header.svg" alt="HUD Diagnostic System Header" />
</p>

<!-- DYNAMIC TELEMETRY TAGLINE -->
<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3500&pause=1000&color=00F0FF&center=true&vCenter=true&width=750&lines=System+Protocol%3A+Causal+Inference+%7C+Multi-Agent+Orchestration;Status%3A+Production-Grade+AI+Reliability+Engineering;Ingestion%3A+Tri-Service+Microservices+%7C+High-Throughput+Vector+Search;Query%3A+Entailment-Calibrated+Hallucination+Detection" alt="System Diagnostics Typewriter" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CORE_CAPABILITY-CAUSAL_AI-00f0ff?style=for-the-badge&labelColor=0d1117" />
  <img src="https://img.shields.io/badge/ORCHESTRATION-LANGGRAPH-a855f7?style=for-the-badge&labelColor=0d1117" />
  <img src="https://img.shields.io/badge/DATA_STREAM-POSTGRES%20%2F%20REDIS-6366f1?style=for-the-badge&labelColor=0d1117" />
</p>

---

### 💻 SYSTEM ACTIVE // CORE STATUS

<p align="center">
  <img width="100%" src="./diag-terminal.svg" alt="System Diagnostic Logs" />
</p>

---

## 🛠️ ARCHITECTURAL STACK & PIPELINES

<blockquote>
<b>Engineering Directive:</b> Build scalable, evidence-grounded AI systems from mathematical formulation up to containerized microservice architectures.
</blockquote>

### 🧠 Causal Inference & Probabilistic AI
* **Frameworks & Orchestration:** `DoWhy` | `LangGraph` | `LangChain` | `PyTorch` | `scikit-learn`
* **Foundational Mechanics:** Structural Causal Models (SCMs), Backdoor/Frontdoor Identifiability, Average & Conditional Average Treatment Effect (ATE/CATE) Estimation under distribution shift, Rosenbaum bounds sensitivity metrics, probabilistic calibration curves (ECE).
* **Generative & Representation Learning:** LoRA adapter fine-tuning, conditional GANs (Pix2Pix U-Net/PatchGAN), Text-to-Image (Stable Diffusion), neural style transfer, embedding pipelines.

### ⚙️ Distributed Systems & Backend
* **Microservices:** Spring Boot (Java), FastAPI (Python), Flask, Node.js.
* **Architecture Patterns:** Decoupled write-heavy ingestion and query-heavy retrieve pipelines, Server-Sent Events (SSE) streaming, asynchronous event brokers via Redis Streams.
* **Infrastructure:** Docker Compose, Nginx, SSL/TLS reverse proxying, production-grade serving.

### 🗄️ Database & Retrieval Engineering
* **Vector & Relational engines:** `pgvector` (PostgreSQL), `FAISS` (dense vector search), Mapbox, PostGIS (geospatial queries), MongoDB, Redis caching.
* **Search Paradigms:** Hybrid sparse-dense index merging (BM25 + Dense embeddings), sub-second semantic retrieval over multi-million record clusters.

---

## 🛰️ ACTIVE MISSION ARCHIVES (PROJECTS)

<details>
<summary><b>🚀 SYSTEM // MEDGUARD : AI Medical Billing Auditor & Appeal Engine</b></summary>
<br />

> **Telemetry Status:** Operational | **Built For:** Nexus 2.0 Hackathon | **Architecture Type:** 5-Agent Directed Acyclic Graph (DAG)

#### Visual Schematic
```
Hospital Bill (PDF) ──> LayoutLMv3 + EasyOCR ──> Document Auditor Agent
                                                      │
                                        Clinical Reviewer Agent
                                                      │
                            RAG System (FAISS + sentence-transformers)
                                                      │
                                     Regulatory Advisor Agent
                                                      │
                                         Appeal Drafter Agent
                                                      │
                                  QA Judge Agent ──> SSE Stream ──> Next.js UI
```

#### Core Specifications
* **5-Agent Pipeline:** Sequential orchestration (Auditor → Clinical Reviewer → Regulatory Advisor → Appeal Drafter → QA Judge) with deterministic handoffs and fallback states.
* **Multimodal Extraction:** OCR parsing via LayoutLMv3 + EasyOCR, automatically auditing charges against national CGHS baseline structures.
* **Evidence-Grounded RAG:** Dynamic context compilation from national regulatory circulars with strict citation schemas to eliminate agent hallucinations.
* **Low Latency SSE Output:** Streaming execution steps live to Next.js UI via Server-Sent Events.

`Next.js` `FastAPI` `PostgreSQL` `pgvector` `FAISS` `LangGraph` `Docker`

[![MedGuard Repository](https://img.shields.io/badge/Access_Secure_Files-MedGuard-00f0ff?style=for-the-badge&logo=github&labelColor=0d1117)](https://github.com/Viraj281105/MedGuard)

</details>

<details>
<summary><b>🌀 SYSTEM // CLIMATEX : Causal Policy Simulation Engine</b></summary>
<br />

> **Telemetry Status:** Operational | **Scale:** 700K+ Climate Records | **Engine Core:** DoWhy Causal Inference

#### Visual Schematic
```
Heterogeneous Streams ──> Async Ingest (Python) ──> pgvector + MongoDB
                                                         │
                                        SCM / DAG Topology Generation
                                                         │
                              Counterfactual Simulation (do-calculus)
                                                         │
                        FastAPI Backend ──> React + Mapbox Dashboard
```

#### Core Specifications
* **Policy Counterfactuals:** Models complex interventions via do-calculus (`do(X=x)`) to simulate policy shifts (e.g., fuel subsidies) and forecast localized air quality index.
* **Uncertainty Quantification:** Built-in Rosenbaum bounds and E-value sensitivity diagnostics to measure the impact of unobserved confounders.
* **Real-time Spatial Mapping:** Dynamically feeds CPCB/IMD weather datasets into a highly interactive Mapbox dashboard layered with Plotly diagnostics.
* **Async Ingestion Pipeline:** Streamlines high-velocity climate records into PostgreSQL with vector indexes for real-time document recommendations.

`DoWhy` `FastAPI` `pgvector` `React` `Mapbox` `Recharts` `Plotly` `Docker`

[![ClimateX Repository](https://img.shields.io/badge/Access_Secure_Files-ClimateX-00f0ff?style=for-the-badge&logo=github&labelColor=0d1117)](https://github.com/Viraj281105/ClimateX)

</details>

<details>
<summary><b>🔍 SYSTEM // FACTUALITY-GUARD : Hallucination Verification Pipeline</b></summary>
<br />

> **Telemetry Status:** Calibrated | **Goal:** Probabilistic Verification of Generative Outputs

#### Visual Schematic
```
Claim (LLM Output) ──> pgvector Retrievial ──> DeBERTa NLI Classifier
                                                      │
                                         Calibration (ECE Adjustment)
                                                      │
                                        SHAP Explainability Interface
```

#### Core Specifications
* **NLI Formulation:** Maps factuality validation to a Natural Language Inference sequence, asserting the probability `P(entailment | Evidence, Claim)`.
* **Precision Calibration:** Evaluates confidence alignment using ECE (Expected Calibration Error) metrics, adjusting models under data distribution shifts.
* **Modular Interface:** Encapsulates retrieval, entailment, and calibration models into decoupled, hot-swappable microservices served via Gradio UI.
* **XAI Diagnostics:** Generates feature-level attribution maps using SHAP to highlight exactly which evidence fragments support or contradict the claims.

`DeBERTa` `RoBERTa` `HuggingFace` `RAG` `pgvector` `SHAP` `Gradio`

[![Factuality-Guard Repository](https://img.shields.io/badge/Access_Secure_Files--Factuality--Guard-00f0ff?style=for-the-badge&logo=github&labelColor=0d1117)](https://github.com/Viraj281105/AI-Hallucination-Detection-Application)

</details>

<details>
<summary><b>📦 EXPERIMENTAL SYSTEM DIRECTORY (ADDITIONAL ARCHIVES)</b></summary>
<br />

| System | Codename | Functional Spec | Technology Core |
| :--- | :--- | :--- | :--- |
| **FloatChat** | `NL-TO-SQL` | Geospatial querying & live charts over 3.5M+ ocean records. | `FastAPI`, `PostGIS`, `FAISS`, `Plotly` |
| **FinGuard AI** | `RISK-SIM` | Tri-service statement ingestion & 5D risk forecasting engine. | `Spring Boot`, `FastAPI`, `Zustand`, `Docker` |
| **Multi-Agent RL** | `GOVERNANCE` | Emergent game theory negotiation using PPO/SAC. | `PyTorch`, `Redis Streams`, `FastAPI` |
| **ECG FPGA Accelerator** | `EMBEDDED-CNN` | Ultra-low power 1D CNN for real-time cardiac arrhythmia detection. | `FPGA`, `TensorFlow Lite`, `Python` |

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
      <b>STREAM ACTIVITY</b><br/><br/>
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

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Viraj281105&label=DATASTREAM_READS&color=00f0ff&style=flat-square" />
  <img src="https://img.shields.io/github/followers/Viraj281105?label=NETWORK_NODES&style=flat-square&color=00f0ff" />
</p>

---

## 📝 CREDENTIAL LOG & FIELD RECORD

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h4>🔑 AI &amp; COGNITIVE NETWORKS</h4>
      <ul>
        <li><b>Google x Hack2Skill</b> — 5-Day AI Agents Intensive Course</li>
        <li><b>AICTE Virtual Internship</b> — Google AI/ML Program</li>
        <li><b>AI Adventures (Google)</b> — ML, DL &amp; GenAI</li>
        <li><b>HCL GUVI</b> — AI/ML Certification</li>
      </ul>
    </td>
    <td width="50%" valign="top">
      <h4>📦 DISTRIBUTED ARCHITECTURES</h4>
      <ul>
        <li><b>AWS</b> — Cloud Foundations</li>
        <li><b>Prodigy InfoTech</b> — Generative AI Internship</li>
        <li><b>IIT Bombay</b> — Core Java Certification</li>
      </ul>
    </td>
  </tr>
</table>

---

## 📡 UPLINK PORTAL

<p align="center">
  <a href="mailto:viraj.jadhao28@gmail.com">
    <img src="https://img.shields.io/badge/ESTABLISH_UPLINK-EMAIL-00f0ff?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0d1117" />
  </a>
  &nbsp;
  <a href="https://www.linkedin.com/in/viraj-jadhao-0771b830b/">
    <img src="https://img.shields.io/badge/ESTABLISH_UPLINK-LINKEDIN-a855f7?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0d1117" />
  </a>
</p>

<p align="center">
  <sub style="color: #52525b">SYSTEM TERMINAL SECURED. ACCESS GRANTED.</sub>
</p>
