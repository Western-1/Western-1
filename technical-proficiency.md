## 0x02. TECHNICAL PROFICIENCY
My technical stack covers the full MLOps lifecycle: from model serving and data pipelines to cloud deployment, monitoring, and evaluation. It's battle-tested in my projects, handling real-world constraints like limited hardware and high availability.

### Core Engineering
| Technology | Proficiency | Usage Context |
| :--- | :--- | :--- |
| **Python** | Primary | Backend development, scripting, data processing (Pandas/NumPy), ML pipelines. Used in FastAPI apps, ingestion scripts, and evaluation tools. |
| **FastAPI** | Advanced | Building asynchronous REST APIs with dependency injection, Pydantic validation, and Swagger docs. Core for inference and RAG endpoints. |
| **SQL** | Intermediate | Relational database design and query optimization (PostgreSQL/MySQL). Integrated for metadata storage in larger systems. |
| **Bash/Shell** | Intermediate | Automation scripts, server maintenance, Linux administration, and Makefile commands for dev workflows. |

### Infrastructure & DevOps
| Technology | Proficiency | Usage Context |
| :--- | :--- | :--- |
| **Docker** | Advanced | Multi-stage builds for optimized images (e.g., reducing size for ML models), Docker Compose for orchestration, networking, and persistence (e.g., Qdrant volumes). |
| **Kubernetes** | Intermediate | Manifests for deployments, services, and scaling; used for production-ready RAG systems with persistent storage. |
| **AWS** | Intermediate | EC2 management, S3 for archiving/data storage, IAM roles, Security Groups; CI/CD deployments with SSH. |
| **Nginx** | Intermediate | Reverse proxy, SSL/TLS termination (Let's Encrypt with auto-renewal), load balancing, and timeout tuning for secure APIs. |
| **Redis** | Intermediate | Caching, message brokering (LPUSH/RPOP/LTRIM), async logging to prevent I/O blocking in inference services. |
| **GitHub Actions** | Advanced | CI/CD pipelines: linting (Flake8/Ruff), security scans (Bandit), testing (Pytest), building, and automated deployments to AWS. |

### Machine Learning Operations (MLOps)
| Technology | Proficiency | Usage Context |
| :--- | :--- | :--- |
| **Hugging Face** | Intermediate | Model serving (Transformers), pipelines for sentiment/translation, tokenizers; pinned revisions for reproducibility (e.g., `714eb0f`). |
| **Groq** | Intermediate | Ultra-fast LLM inference in RAG systems for low-latency generation. |
| **Qdrant** | Intermediate | Vector database for embedding storage, semantic search, and metadata filtering in RAG pipelines. |
| **Langfuse** | Advanced | Observability with tracing, feedback loops (thumbs up/down), prompt management, and token/latency tracking (v3 upgrades). |
| **Ragas** | Intermediate | Automated evaluation of RAG pipelines (faithfulness, precision, recall); integrated with scripts and W&B reporting. |
| **Streamlit** | Intermediate | Interactive UIs for demos, chat interfaces with async features and source citations. |
| **Weights & Biases (W&B)** | Intermediate | Experiment tracking, model registry, artifact logging, and evaluation dashboards for reproducible benchmarks. |
| **Prometheus** | Intermediate | Metrics scraping (e.g., latency, throughput, errors), time-series storage; exposed via `/metrics`. |
| **Grafana** | Intermediate | Custom dashboards for visualizing RPS, memory usage, HTTP status, and alerts. |
| **Locust** | Intermediate | Load/stress testing to benchmark capacity (e.g., 5 RPS on t3.micro before saturation). |
| **FlashRank** | Intermediate | Reranking for high-precision retrieval in RAG (e.g., top-7 from 50 chunks). |
| **LangChain** | Intermediate | Chains for multi-query generation, chunking (RecursiveCharacterTextSplitter), and RAG orchestration. |
| **PyTorch / Transformers** | Intermediate | Inference for NLP models (DistilBERT, Helsinki-NLP); lazy loading to optimize memory/startup. |
| **Other Tools** | Intermediate | APScheduler for scheduled tasks (e.g., S3 archiving); Boto3 for AWS integrations; Ruff/Flake8/Bandit for code quality. |

<div align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" />
  <img src="https://img.shields.io/badge/Grafana-F2F4F9?style=for-the-badge&logo=grafana&logoColor=orange" />
</div>