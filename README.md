<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:7c3aed,100:2dd4bf&height=200&section=header&text=Aquib%20Ansari&fontSize=52&fontColor=ffffff&fontAlignY=36&desc=AI%20Engineer&descAlignY=58&descSize=22" alt="Aquib Ansari, AI Engineer" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1200&color=A78BFA&center=true&vCenter=true&width=720&lines=Production+Agentic+Systems+%26+RAG;LangGraph+multi-agent+systems+on+FastAPI;MCP+integrations+%2B+LLM+security+guardrails;Published+research+in+NLP+%26+computer+vision" alt="Production agentic systems and RAG" />

<p>
  <a href="https://aqib420.github.io/landing-page/"><img src="https://img.shields.io/badge/Portfolio-aqib420.github.io-7c3aed?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/aquib-ansari-641ba1200/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge" alt="LinkedIn" /></a>
  <a href="mailto:aquibahmed2000@gmail.com"><img src="https://img.shields.io/badge/Email-Say%20hello-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

<p>
  <img src="https://img.shields.io/badge/Live%20AI%20products-5-7c3aed?style=for-the-badge&labelColor=1f2937" alt="5 live AI products" />
  <img src="https://img.shields.io/badge/Guardrail%20layers-12-2dd4bf?style=for-the-badge&labelColor=1f2937" alt="12 guardrail layers" />
  <img src="https://img.shields.io/badge/MCP%20integrations-10-7c3aed?style=for-the-badge&labelColor=1f2937" alt="10 MCP integrations" />
  <img src="https://img.shields.io/badge/Published%20reports-3-2dd4bf?style=for-the-badge&labelColor=1f2937" alt="3 published reports" />
</p>

</div>

---

### 👋 About me

I'm an **AI Engineer who owns production AI products end to end**: architecture, backend, deployment, and client delivery. I ship **LangGraph multi-agent systems**, **RAG pipelines**, **MCP tool integrations**, and **LLM security guardrails** on **FastAPI**, used live by non-profit and business clients.

My work is backed by applied research in low-resource NLP and computer vision, with technical reports published on Zenodo.

| 🏢 Now | 🎓 Education | 📄 Research | 🎯 Focus |
|---|---|---|---|
| AI Engineer at **BigGorillaApps** (since Feb 2026) | BSc Computer Science, **Habib University** (2020 – 2025) | **3 technical reports** on Zenodo | Agentic AI · RAG · LLM security |

---

### 🚀 What I ship

Core engineer on a small team shipping **five live AI products** for non-profit and business clients at BigGorillaApps. Tap a product to expand.

<details open>
<summary><b>🧠 Skraggle Assist</b> — AI assistant for a non-profit fundraising and CRM platform</summary>

<br>

- LangGraph agent (**Planner → Executor → Gate → Responder**, FastAPI + SSE) that turns plain-language requests into branded landing pages, designed emails, and donor segments
- Playwright crawler that learns each charity's **brand persona** from its website (Cloudflare bypass fallbacks, sitemap discovery, resumable crawls) and feeds a **Qdrant RAG** layer whose answers cite source URLs
- **Natural-language segment builder**: "lapsed donors in London" becomes a segment-filter API payload, with IDs resolved through lookup APIs
- **12-layer guardrail system** (prompt injection, jailbreak, tool authorization and argument validation, data-leakage prevention, malicious URLs, scope control), verified by **50+ automated tests**
- Led a **13-category production-readiness audit**: found and fixed a cross-tenant data-access flaw, added per-token rate limiting (20/min, 300/day) and per-call cost logging

</details>

<details>
<summary><b>🤝 crewGorilla</b> — multi-agent AI workspace for businesses</summary>

<br>

- Consolidated standalone agents (**Linda, Penny, Sonny, EVA**) into one **supervisor-agent monorepo** with rule-based routing, @mention targeting, and a shared Supabase context store
- Built **10 MCP server integrations** (Gmail, Google Calendar, Drive, Outlook Mail and Calendar, OneDrive, Jira, Zoom, HubSpot, Notion) through Nango-managed OAuth
- Secured all five chat endpoints with **Redis-backed per-user rate limiting** and two-tier input guardrails (regex pre-filter + LLM classifier) that also scan uploaded documents for injected prompts
- Document-to-knowledge-base ingestion for per-user clone agents, so agents answer from uploaded PDFs and DOCX files (reusing the Qdrant RAG pipeline)

</details>

<details>
<summary><b>🤖 Agent products and analytics</b> — Sonny, Penny, Giverr, Skraggle analytics</summary>

<br>

- **Sonny** (AI social media manager): LangGraph multi-agent system with Facebook publishing, Flux image generation, multi-platform OAuth via Nango, and Langfuse prompt caching that cut per-turn overhead
- **Penny** (AI blog writer): five-node LangGraph pipeline on NVIDIA NIM covering brand onboarding, keyword and SERP research, outline, article, and SEO checks, with auto-publishing tested across 8 scenarios · [🎥 watch the demo](https://aqib420.github.io/landing-page/#demo)
- **Giverr Donor Agent**: autonomous **Plan → Verify → Execute → Review (PVER)** workflow with real-time API integrations for decision-making on a live bidding platform, plus a draft-first, five-stage campaign creation agent
- **Skraggle analytics**: turned research code into a production **XGBoost + Prophet** forecasting service projected to drive **$650k+** in campaign revenue; built donor churn (30/60/90-day), RFM, and smart-ask scoring

</details>

#### How a Skraggle Assist request flows

```mermaid
flowchart LR
    U(["Plain-language request"]) --> P["Planner"]
    P --> E["Executor"]
    E --> G["Gate"]
    G --> R["Responder"]
    R -->|"SSE stream"| O(["Response"])
    E -.- K[("Qdrant RAG<br/>brand persona")]
    E -.- A[["Platform APIs<br/>segments and lookups"]]

    classDef agent fill:#7c3aed,stroke:#a78bfa,color:#ffffff;
    classDef data fill:#0f766e,stroke:#2dd4bf,color:#ffffff;
    class P,E,G,R agent;
    class K,A data;
```

---

### 📄 Published research

Three technical reports from Habib University, each published on Zenodo with the code open on GitHub.

| Report | Key result | Links |
|---|---|---|
| **Sentiment Analysis of Roman Urdu Using LSTM, BERT, and GPT-2**<br>Four-class classifier (incl. an *Abusive* class) for code-mixed text, built on a sentiment corpus merged with the RUHSOLD hate-speech dataset | Fine-tuned **GPT-2** wins: **70.24% accuracy**, **0.65 macro-F1**, beating mBERT despite English-only pre-training | <a href="https://doi.org/10.5281/zenodo.23836675"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.23836675.svg" alt="DOI 10.5281/zenodo.23836675" /></a><br>[Code ↗](https://github.com/aqib420/RomanUrduSentimentAnalysis) |
| **Identification of South Asian Musical Instruments Using CNNs**<br>New dataset of ~6,000 four-second clips across 15 classes (sitar, bansuri, harmonium, tabla, and combinations) | Multi-label CNN on mel-spectrograms: **0.94 precision / recall / F1** vs **45%** for a KNN baseline | <a href="https://doi.org/10.5281/zenodo.23829481"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.23829481.svg" alt="DOI 10.5281/zenodo.23829481" /></a><br>[Code ↗](https://github.com/aqib420/South-Asian-Identification-Tensorflow) |
| **Deep Fake Detection Using Transfer Learning with the ReActNet-MobileNet Architecture**<br>Leakage-free, video-level pipeline for Celeb-DF (v2) | Fine-tuned an ImageNet-pre-trained binary neural network (ReActNet) on class-balanced samples from **106k+ frames** | <a href="https://doi.org/10.5281/zenodo.23837621"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.23837621.svg" alt="DOI 10.5281/zenodo.23837621" /></a><br>[Code ↗](https://github.com/aqib420/CV-Project-me-) |

---

### 💼 Experience

| When | Role | Where |
|---|---|---|
| **Feb 2026 – Present** | AI Engineer | **BigGorillaApps** · London, UK (Remote) |
| Sep 2025 – Jan 2026 | Freelance NLP Developer | Independent · Remote. Confidential legal-sector NLP: fine-tuned Hugging Face classifiers, OpenAI API + spaCy |
| Jun 2025 – Aug 2025 | Machine Learning & AI Intern | **Bewhoop** · Remote. Real-time semantic search engine (FAISS + Sentence Transformers) over Supabase data |
| Jul 2024 – Sep 2024 | Software Engineering Fellow | **Headstarter** · Remote. Full-stack AI applications in an Agile/Scrum environment |

---

### ⚙️ Tech stack

**Agentic AI & LLMs**

<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph" />
<img src="https://img.shields.io/badge/MCP-7c3aed?style=flat-square&logo=modelcontextprotocol&logoColor=white" alt="MCP" />
<img src="https://img.shields.io/badge/RAG-0f766e?style=flat-square" alt="RAG" />
<img src="https://img.shields.io/badge/PVER-7c3aed?style=flat-square" alt="PVER" />
<img src="https://img.shields.io/badge/Tool%20Calling-4b5563?style=flat-square" alt="Tool Calling" />
<img src="https://img.shields.io/badge/Prompt%20Engineering-4b5563?style=flat-square" alt="Prompt Engineering" />
<img src="https://img.shields.io/badge/Langfuse-6366F1?style=flat-square" alt="Langfuse" />
<img src="https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white" alt="Claude" />
<img src="https://img.shields.io/badge/GPT--4-412991?style=flat-square" alt="GPT-4" />
<img src="https://img.shields.io/badge/NVIDIA%20NIM-76B900?style=flat-square&logo=nvidia&logoColor=white" alt="NVIDIA NIM" />

**LLM security**

<img src="https://img.shields.io/badge/Prompt%20Injection%20and%20Jailbreak%20Guardrails-b91c1c?style=flat-square" alt="Prompt injection and jailbreak guardrails" />
<img src="https://img.shields.io/badge/Tool%20Authorization-b91c1c?style=flat-square" alt="Tool authorization" />
<img src="https://img.shields.io/badge/Tenant%20Isolation-b91c1c?style=flat-square" alt="Tenant isolation" />
<img src="https://img.shields.io/badge/Rate%20Limiting-b91c1c?style=flat-square" alt="Rate limiting" />
<img src="https://img.shields.io/badge/Readiness%20Audits-b91c1c?style=flat-square" alt="Readiness audits" />

**Machine learning**

<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" alt="TensorFlow" />
<img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face" />
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn" />
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV" />
<img src="https://img.shields.io/badge/XGBoost-337ab7?style=flat-square" alt="XGBoost" />
<img src="https://img.shields.io/badge/Prophet-0b5fff?style=flat-square" alt="Prophet" />
<img src="https://img.shields.io/badge/BERT%20%2F%20GPT--2%20%2F%20LSTM-4b5563?style=flat-square" alt="BERT, GPT-2, LSTM" />
<img src="https://img.shields.io/badge/CNNs-4b5563?style=flat-square" alt="CNNs" />

**Backend and cloud**

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/FastAPI%20(SSE)-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
<img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" alt="Flask" />
<img src="https://img.shields.io/badge/REST-4b5563?style=flat-square" alt="REST" />
<img src="https://img.shields.io/badge/SQL-4b5563?style=flat-square" alt="SQL" />
<img src="https://img.shields.io/badge/AWS-FF9900?style=flat-square" alt="AWS" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions" />
<img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square" alt="Playwright" />

**Data and retrieval**

<img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white" alt="Qdrant" />
<img src="https://img.shields.io/badge/FAISS-0668E1?style=flat-square" alt="FAISS" />
<img src="https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white" alt="Supabase" />
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
<img src="https://img.shields.io/badge/Neo4j-4581C3?style=flat-square&logo=neo4j&logoColor=white" alt="Neo4j" />
<img src="https://img.shields.io/badge/Sentence%20Transformers-4b5563?style=flat-square" alt="Sentence Transformers" />
<img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="Pandas" />
<img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="NumPy" />

---

### 📌 Open-source projects

<p align="center">
  <a href="https://github.com/aqib420/RomanUrduSentimentAnalysis"><img width="49%" src="https://github-readme-stats.vercel.app/api/pin/?username=aqib420&repo=RomanUrduSentimentAnalysis&theme=tokyonight&hide_border=true" alt="RomanUrduSentimentAnalysis" /></a>
  <a href="https://github.com/aqib420/South-Asian-Identification-Tensorflow"><img width="49%" src="https://github-readme-stats.vercel.app/api/pin/?username=aqib420&repo=South-Asian-Identification-Tensorflow&theme=tokyonight&hide_border=true" alt="South-Asian-Identification-Tensorflow" /></a>
  <a href="https://github.com/aqib420/FAISS-Recommendation"><img width="49%" src="https://github-readme-stats.vercel.app/api/pin/?username=aqib420&repo=FAISS-Recommendation&theme=tokyonight&hide_border=true" alt="FAISS-Recommendation" /></a>
  <a href="https://github.com/aqib420/english-to-french-transformer"><img width="49%" src="https://github-readme-stats.vercel.app/api/pin/?username=aqib420&repo=english-to-french-transformer&theme=tokyonight&hide_border=true" alt="english-to-french-transformer" /></a>
</p>

<p align="center">
  <sub>Most of my production work lives in private client repositories, so the public graph understates it. See all public repos on <a href="https://github.com/aqib420?tab=repositories">GitHub</a>.</sub>
</p>

---

### 📫 Let's connect

<div align="center">

I'm open to **AI engineering roles** and **freelance projects** involving agentic systems, RAG, and production ML.

<a href="https://aqib420.github.io/landing-page/"><img src="https://img.shields.io/badge/Portfolio-7c3aed?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio" /></a>
<a href="https://www.linkedin.com/in/aquib-ansari-641ba1200/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge" alt="LinkedIn" /></a>
<a href="mailto:aquibahmed2000@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://x.com/aquiban14276041"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" alt="X" /></a>

<br><br>

<img src="https://komarev.com/ghpvc/?username=aqib420&label=Profile%20views&color=7c3aed&style=flat-square" alt="Profile views" />

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:7c3aed,100:2dd4bf&height=120&section=footer" alt="" />

</div>
