## 0x03. FEATURED PROJECTS

### [NLP Inference Service](https://github.com/Western-1/nlp-inference-service)
This production-ready microservice serves NLP models (sentiment analysis via DistilBERT and translation via Helsinki-NLP) with a focus on reliability under constraints like AWS t3.micro (1GB RAM).

#### The Challenge
Deploying heavy Transformer models on limited hardware while ensuring high availability, security, observability, and reproducibility without "silent failures" from upstream changes.

#### The Solution Architecture
A decoupled, containerized stack orchestrated via Docker Compose:
1. **Ingress Layer:** Nginx for SSL/TLS (Let's Encrypt auto-renewal), proxying, and load balancing.
2. **Application Layer:** FastAPI with Gunicorn/Uvicorn workers; lazy model loading for fast startup; endpoints like `/sentiment`, `/translate`, `/history`.
3. **Data Layer:** Redis for async logging (LPUSH/LTRIM) to avoid I/O blocking; scheduled archiving to AWS S3 via APScheduler.
4. **Observability Layer:** Prometheus for metrics collection, Alertmanager for downtime alerts (e.g., Telegram), Grafana for dashboards (RPS, latency, memory).

#### Key Engineering Achievements
* **Deterministic Reproducibility:** Pinned model versions with Git SHA hashes (e.g., `distilbert @ 714eb0f`) to prevent updates breaking inference.
* **Capacity Benchmarking:** Locust stress tests show ~5 RPS stability on single-core; identifies CPU saturation at higher loads (504 timeouts at 15 users).
* **Security Implementation:** API key auth (X-API-Key), secrets via .env/GitHub Secrets; SSL for public endpoints.
* **Automated CI/CD:** GitHub Actions pipeline: linting (Flake8), security (Bandit), testing (Pytest with mocks), build, and SSH deploy to AWS EC2 on main pushes.
* **MLOps Integration:** W&B for tracking experiments; mocked tests for CI; health checks and metrics at `/health`, `/metrics`.
* **Live Demo:** API at [https://western-nlp.ddns.net/docs](https://western-nlp.ddns.net/docs); use public key `demo`.

### [Enterprise-grade RAG System (Talk to Your Docs)](https://github.com/Western-1/rag-doc-chat)
v3 of a production-ready RAG microservice for querying PDFs via natural language, with emphasis on accuracy, observability, and scalability. Builds on NLP foundations with advanced retrieval and MLOps.

#### The Challenge
Handling PDF ingestion, high-recall retrieval, and hallucination-free LLM responses on constrained setups, integrated with full monitoring and evaluation.

#### The Solution Architecture
Modular, containerized system with Docker Compose and Kubernetes support:
1. **Ingestion & Storage Layer:** Page-aware PDF extraction, text cleaning (hyphens, citations), chunking/deduplication (MD5), embeddings in Qdrant.
2. **Retrieval & Reranking Layer:** Multi-query for deep search (top-50), FlashRank reranker (top-7) for precision.
3. **Generation Layer:** FastAPI API with Groq (or OSS LLMs) for inference; strict prompts to ground answers.
4. **UI & Interaction Layer:** Streamlit for chat, async ingestion, feedback, citations (page numbers/snippets).
5. **Observability Layer:** Langfuse v3 for tracing/feedback, Prometheus metrics, Grafana dashboards, Ragas for eval.

#### Key Engineering Achievements
* **High-Performance RAG:** 94% recall/89% precision with reranking; faithfulness 1.00 (zero hallucinations) via Ragas.
* **Production Readiness:** Background ingestion, error handling, health checks; Kubernetes manifests for scaling.
* **Observability Integration:** Langfuse traces (tokens/latency), user feedback loops, Grafana for real-time insights (latency/errors/throughput).
* **Automated Workflows:** GitHub Actions CI/CD (linting/testing/eval); Makefile for ops (`make up`, `make eval`); W&B for benchmarks.
* **Enhancements in v3:** Langfuse v3 upgrade, Prometheus/Grafana addition, UI/API separation, better logging/fallbacks.