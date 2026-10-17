# Hi, I'm Sumukha 👋

I'm a software engineer with 10+ years of IT experience, primarily in native Android development, including client engagements with Zee5 and Zeta. I've shipped features, integrated APIs and SDKs, debugged difficult issues, and worked on application reliability.

I'm now building applied AI systems with Python, machine learning, RAG and agent orchestration. My personal projects connect models to backend services, mobile applications and cloud infrastructure, with testing and evaluation alongside the implementation.

## Featured Projects

### [Football Intelligence Platform](https://github.com/SumukhaK/football-intelligence-platform)

A football analytics platform connecting data ingestion, explainable predictions, an AI assistant and a native Android app.

- XGBoost match predictions and SHAP explanations using 26 seasons of data from five European leagues.
- FastAPI backend and Compose Multiplatform Android client with offline data access.
- Dockerized API deployed to invite-only Google Cloud Run staging, with Firestore-backed accounts and Secret Manager.
- Hosted RAG and tool calling through Cloudflare Workers AI, with bounded retries and signed, limited conversation history.
- Compared hosted model configurations: disabling hidden reasoning reduced measured p50 response time from 10 seconds to 3 seconds in a 31-question provider evaluation, retaining 20/20 abstention and 11/11 grounding results. [Evaluation details](https://github.com/SumukhaK/football-intelligence-platform/blob/main/docs/reports/hosted-assistant-evals.md).

### [Football Dashboard](https://github.com/SumukhaK/football-dashboard) · In progress

A companion monitoring console I'm building to understand how the football platform behaves.

- FastAPI, HTMX and ECharts views for component health, traffic, error rates and p50/p95 latency.
- Google Cloud log and trace readers, request search, error groups and trace waterfalls, with cached reads.
- Request-correlated telemetry and OpenTelemetry traces in the platform support investigation across retrieval, tool calls and generation.

### [Agentic RAG](https://github.com/SumukhaK/agentic-rag)

A local document question-answering system using Qdrant hybrid retrieval, cross-encoder reranking and Ollama.

- Document ingestion, query rewriting, source citations and per-user access control.
- Recorded local evaluation (**6 questions, 4 documents**): retrieved the expected source for **4/4 answerable questions**, correctly declined **2/2 unanswerable questions**, with **0 pipeline errors**.
- **3/4 answers judged faithful** and **1/6 questions flagged as hallucination**; **76.7s average evaluation time**, including LLM judging on local hardware. This small run is a smoke test, not a production benchmark. [Walkthrough and results](https://sumukhak.github.io/agentic-rag/artifact/walkthrough.html) · [Evaluation methodology](https://github.com/SumukhaK/agentic-rag/blob/main/eval/README.md).
- Load-test findings, memory limits and proposed architectural changes documented in the repository.

### [Claude Multiagent](https://github.com/SumukhaK/claude-multiagent)

A local coding assistant with Planner, Coder and Tool agents coordinated through LangGraph and Ollama.

- Pydantic contracts, bounded retries, allowlisted tools and OpenTelemetry tracing.
- Coding tasks evaluated with hidden acceptance tests, with fixes and failed experiments documented.

## Tech Stack

**AI & Backend:** Python · FastAPI · Pydantic · XGBoost · SHAP · RAG · LangChain · LangGraph · Qdrant · Ollama

**Cloud & Observability:** Google Cloud Run · Docker · Firestore · Secret Manager · Cloud Logging · Cloud Trace · OpenTelemetry · Cloudflare Workers AI

**Android:** Kotlin · Java · Jetpack Compose · Compose Multiplatform · MVVM · Coroutines · Flow · Room · Hilt · Retrofit

**Engineering:** Git · GitHub Actions · pytest

## How I Work

I like owning a system end to end: understanding the data, making architecture decisions, testing behaviour and following failures back to their cause. I keep decisions, experiments and remaining limitations alongside the code.

## Connect

- LinkedIn: [linkedin.com/in/sumukha-aithal-77954858](https://www.linkedin.com/in/sumukha-aithal-77954858/)
- Email: sumukh.aithal@gmail.com
