# Hi, I'm Sumukha 👋

I'm a software engineer with 10+ years of IT experience, primarily in native Android development, including client engagements with Zee5 and Zeta. I've shipped features, integrated APIs and SDKs, debugged difficult issues, and worked on application reliability.

I'm now building applied AI systems with Python, machine learning, RAG and agent orchestration. My personal projects connect models to backend services, mobile applications and cloud infrastructure, with testing and evaluation alongside the implementation.

## Featured Projects

### [Football Intelligence Platform](https://github.com/SumukhaK/football-intelligence-platform)

A football analytics platform connecting data ingestion, explainable predictions, an AI assistant and a native Android app.

[Watch the 2-minute demo](https://fip-ai.dev/demo.mp4) · [Model evaluation](https://github.com/SumukhaK/football-intelligence-platform/blob/main/docs/reports/in-season-2026-27.md) · [Assistant evaluation](https://github.com/SumukhaK/football-intelligence-platform/blob/main/docs/reports/hosted-assistant-evals.md) · [Project website](https://fip-ai.dev/)

- XGBoost match predictions and SHAP explanations using 26 seasons of data from five European leagues.
- Season-based evaluation and a 250-match 2026/27 backtest, with bookmaker and Elo baseline comparisons and bootstrap uncertainty intervals. The live model scored 52.0% accuracy against Bet365's 51.6%; the difference was within uncertainty. [Live-model report](https://github.com/SumukhaK/football-intelligence-platform/blob/main/docs/reports/refit-all-seasons.md).
- FastAPI backend and Compose Multiplatform Android client with offline data access.
- Dockerized API deployed to invite-only Google Cloud Run staging, with Firestore-backed accounts and Secret Manager.
- Hosted RAG and tool calling through Cloudflare Workers AI, with bounded retries and signed, limited conversation history.
- Daily per-user and global assistant token budgets, transactional sign-in lockouts, and account-backed favourite-team preferences.
- Compared hosted model configurations: disabling hidden reasoning reduced measured p50 response time from 10 seconds to 3 seconds in a 31-question evaluation, retaining 20/20 abstention and 11/11 grounding results. These calls ran from a development machine to Workers AI; they do not measure full staging request latency.

### [Football Dashboard](https://github.com/SumukhaK/football-dashboard)

A companion monitoring console deployed on Cloud Run with owner-only Google sign-in, built with FastAPI, HTMX and ECharts.

[Narrated walkthrough](https://github.com/SumukhaK/football-dashboard/blob/main/docs/demo/README.md) (6 minutes, sample-data demo) · [Live deployment verification](https://github.com/SumukhaK/football-dashboard/blob/main/guide/D9.6-live-verification.md) · [Deployment failure investigation](https://github.com/SumukhaK/football-dashboard/blob/main/guide/adr/002-cloud-run-health-path.md)

- Request search, error investigation and trace waterfalls, plus assistant tool calls, fallbacks, reported tokens and cost.
- Data freshness and access monitoring, API release comparisons and bounded historical queries; optional Android crash views from Crashlytics exports in BigQuery.
- Read-only cloud telemetry access, cached reads and signed sessions. Deployment evidence records owner/non-owner sign-in checks, signing-key rotation and a private-first rollback exercise.
- Local sample-data demo and backend log-file support, with source limitations and missing data shown explicitly.
- Investigated Cloud Run returning a platform 404 for `/healthz`; added `/health` for hosted checks, retained local compatibility and verified the fix against the deployed image.

### [Agentic RAG](https://github.com/SumukhaK/agentic-rag)

A local document question-answering system using Qdrant hybrid retrieval, cross-encoder reranking and Ollama.

- Document ingestion, query rewriting, source citations and per-user access control.
- Small local smoke test (6 questions over 4 documents): expected sources found for **4/4 answerable questions** and **2/2 unanswerable questions correctly declined**. [Walkthrough and full results](https://sumukhak.github.io/agentic-rag/artifact/walkthrough.html) · [Evaluation methodology](https://github.com/SumukhaK/agentic-rag/blob/main/eval/README.md).
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
