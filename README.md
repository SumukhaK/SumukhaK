# Hi, I'm Sumukha 👋

I've spent the last 10+ years building native Android applications — shipping features, fixing the hard bugs, and living with the consequences of my own architecture decisions in production. Recently I started learning AI Engineering and Python. Rather than working through isolated tutorials, I've been building complete, production-style projects — a retrieval-augmented generation system and a local multi-agent coding assistant — to understand the full lifecycle of an AI system end to end: how it's designed, how it's evaluated, and how it actually fails. I'm documenting that journey publicly here on GitHub.

## My Journey

After a decade of building Android apps — and consuming AI APIs like any other backend dependency — I wanted to understand what actually happens on the other side of those calls. So I started learning, from the ground up:

- Python
- Data Engineering
- Machine Learning
- FastAPI
- Explainable AI
- Retrieval-Augmented Generation
- Multi-agent systems & LLM orchestration
- MLOps fundamentals
- GitHub Actions
- CI/CD

The goal isn't to become someone who just calls AI APIs. It's to understand how production AI systems are actually designed, trained, explained, tested, and served — the same way I'd want to understand any system before I ship it. I'm early in this, and I'd rather be upfront about that than overstate it.

Two projects since then took me past reading and into actually shipping and evaluating something: a retrieval-augmented generation system that I load-tested until it broke — memory exhaustion at 6,000 of a 10,000-document target — and root-caused rather than quietly shrinking the test; and a local multi-agent coding assistant where every fix was measured against the real system before being trusted, including one I built, tested, and then honestly reverted because the data showed it didn't work. Both taught me the same lesson from different angles: production AI systems fail in specific, measurable ways, and the real engineering work is finding out exactly why and how far a system can be pushed — not just getting a demo to work once.

## Current Focus

Things I'm actively learning right now:

- Python
- AI Engineering
- Machine Learning
- FastAPI
- XGBoost
- SHAP
- RAG
- Multi-agent orchestration
- MLOps
- Production AI systems

## Tech Stack

**Android** (10+ years)

Kotlin · Java · Jetpack Compose · MVVM · Coroutines · Flow · Room · Hilt · Retrofit

**AI & Backend** (learning, applied in the projects below)

Python · FastAPI · XGBoost · SHAP · RAG · Ollama · LangGraph · Qdrant · pytest · GitHub Actions · Git · Markdown

## Featured Projects

### [Football Intelligence Platform](https://github.com/SumukhaK/football-intelligence-platform)

An end-to-end football analytics platform, and the project I'm using to learn AI engineering by actually building it rather than reading about it. It's a complete system, not a notebook:

- A native Android application (Compose Multiplatform) consuming a real backend
- A FastAPI backend serving predictions and an assistant over REST
- A data engineering pipeline that ingests and validates match data before it's used
- An XGBoost pipeline that predicts match outcomes
- SHAP explainability attached to every single prediction, not just the model as a whole
- A retrieval-augmented assistant that answers questions grounded in the platform's own data, running locally
- CI/CD via GitHub Actions
- Documentation, including architecture decisions, kept alongside the code

### [Agentic RAG](https://github.com/SumukhaK/agentic-rag)

A retrieval-augmented generation system built to production standards, not a demo: hybrid dense/sparse search over a Qdrant vector store, cross-encoder reranking, per-user access control, prompt-injection detection at the query boundary, and an explicit "I don't know" instead of a hallucinated answer when the indexed corpus can't support one. Generation and embeddings run locally via Ollama (Mistral, Nomic-embed-text).

- Ingestion and query pipelines with caching, query rewriting, and query decomposition for complex questions
- Containerized (Docker + FastAPI), with liveness/readiness health checks and correlation IDs on every request
- Load-tested against a 10,000-document target, not just a small demo corpus — and reporting the real result honestly: it failed at 6,000 documents from sustained memory exhaustion in the embedded vector index. I root-caused it (the in-memory HNSW graph outgrowing available RAM) rather than quietly shrinking the test. The fix — moving off embedded/in-memory Qdrant to a server deployment with on-disk storage — is identified, not yet built.

### [Claude Multiagent](https://github.com/SumukhaK/claude-multiagent)

A local-first, multi-agent AI coding assistant — a Planner, a Coder, and a Tool agent cooperating under an orchestrator loop (LangGraph) to turn a plain-language request into tested, reviewed code, running entirely on local hardware via Ollama, no paid APIs.

- Graded against a fixed set of ten tasks with hidden tests the system never sees, not by trusting its own report of success
- The first two models I tried both scored 0% on that test set; getting from there to a best result of 69% took nine separate, individually measured fixes — each one root-caused from real failure evidence first, never guessed at
- One candidate fix was built, measured, and found to do nothing — so it's documented and reverted, not kept for appearances
- The honest ceiling is written down too: what's left is the local 7B model's own code-generation reliability, which I confirmed, more than once, does not improve just by rewording the instructions it's given

## What I've Learned

Building complete projects taught me more than finishing a dozen disconnected tutorials ever did. Tutorials show you a step. A real project forces you to make the step work with the step before it and the step after it — data quality feeding a model, a model's output feeding an explanation, an explanation feeding a UI, a fix's effect feeding the next decision about whether to keep it. That's where I started to see how software engineering and AI engineering actually depend on each other, rather than being two separate skills.

## Connect

- LinkedIn: [linkedin.com/in/sumukha-aithal-77954858](https://www.linkedin.com/in/sumukha-aithal-77954858/)
- Email: sumukh.aithal@gmail.com
