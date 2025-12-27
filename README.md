<div align="center">
  <h1>ANDRIY VLONHA</h1>
  <h3>Junior MLOps Engineer | Cloud Infrastructure Architect</h3>
  <p>
    <b>Specializing in High-Availability NLP Systems, Container Orchestration, and Automated Deployment Pipelines.</b>
  </p>
  <p>
    <a href="https://www.linkedin.com/in/андрій-влонга-9562b537b">
      <img src="https://img.shields.io/badge/Connect_on_LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
    </a>
    <a href="mailto:andriy.vlonha.dev.com">
      <img src="https://img.shields.io/badge/Contact_via_Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
    </a>
  </p>
</div>

<hr/>

## 0x01. SYSTEM STATUS / INTRODUCTION

I am a Computer Science student and an aspiring MLOps Engineer focusing on the intersection of Software Engineering and Machine Learning. My primary interest lies not just in model training, but in the **operationalization of ML models**—ensuring they are served reliably, scalably, and securely in production environments.

I approach infrastructure with a software engineering mindset: strictly typed, version-controlled, and tested. My goal is to build systems where deployment is a boring, predictable event rather than a stressful manual process.

**Current Focus:**
* Developing low-latency microservices for NLP inference.
* Optimizing Docker container sizes and build times.
* Implementing strict observability standards (Prometheus/Grafana).

---

## 0x02. TECHNICAL PROFICIENCY

My technical stack is selected to cover the full MLOps lifecycle: from containerization to cloud deployment and monitoring.

### Core Engineering
| Technology | Proficiency | Usage Context |
| :--- | :--- | :--- |
| **Python** | Primary | Backend development, scripting, data processing (Pandas/NumPy). |
| **FastAPI** | Advanced | Building asynchronous REST APIs, dependency injection, Pydantic validation. |
| **SQL** | Intermediate | Relational database design, query optimization (PostgreSQL/MySQL). |
| **Bash/Shell** | Intermediate | Automation scripts, server maintenance, Linux administration. |

### Infrastructure & DevOps
| Technology | Proficiency | Usage Context |
| :--- | :--- | :--- |
| **Docker** | Advanced | Multi-stage builds, Docker Compose orchestration, networking optimization. |
| **AWS** | Intermediate | EC2 instance management, S3 storage integration, Security Groups, IAM. |
| **Nginx** | Intermediate | Reverse Proxy configuration, SSL termination, load balancing, timeout tuning. |
| **Redis** | Intermediate | Caching layers, message brokering (LPUSH/RPOP), asynchronous task queues. |
| **GitHub Actions** | Advanced | CI/CD pipelines, automated testing, SSH deployment strategies. |

### Machine Learning Operations (MLOps)
| Technology | Proficiency | Usage Context |
| :--- | :--- | :--- |
| **HuggingFace** | Intermediate | Model serving, pipeline integration, tokenizer management. |
| **W&B** | Intermediate | Experiment tracking, model registry, artifact logging. |
| **Prometheus** | Intermediate | Metrics scraping, time-series database management. |
| **Grafana** | Intermediate | Dashboard creation, visualizing RPS/Latency/Memory usage. |
| **Locust** | Intermediate | Load testing, stress testing, bottleneck identification. |

<div align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
</div>

---

## 0x03. FEATURED ARCHITECTURE: NLP INFERENCE SYSTEM

### [Project Repository: nlp-inference-service](https://github.com/Western-1/nlp-inference-service)

This project represents a comprehensive, production-grade microservice designed to serve Natural Language Processing models (Sentiment Analysis and Translation) under real-world constraints.

#### The Challenge
Deploying heavy Transformer models (DistilBERT, Helsinki-NLP) on limited hardware (AWS t3.micro, 1GB RAM) while maintaining high availability, security, and observability.

#### The Solution Architecture
I designed a decoupled architecture to separate the API layer from the persistence layer, orchestrated via Docker Compose.

1.  **Ingress Layer:** Nginx acts as the entry point, handling SSL/TLS termination (Let's Encrypt) and proxying traffic to the application server.
2.  **Application Layer:** A FastAPI service managed by Gunicorn/Uvicorn workers. It implements a "Lazy Loading" strategy for ML models to optimize startup time and memory usage.
3.  **Data Layer:** Redis is utilized for high-throughput asynchronous logging. This prevents disk I/O blocking during inference requests.
4.  **Observability Layer:** A sidecar stack consisting of Prometheus (metrics collection), Alertmanager (downtime alerting), and Grafana (visualization).

#### Key Engineering Achievements
* **Deterministic Reproducibility:** Implemented strict model versioning by pinning specific Git SHA hashes (`revision='714eb0f'`) for HuggingFace downloads. This prevents "silent failures" caused by upstream model updates.
* **Capacity Benchmarking:** Conducted extensive stress testing using **Locust**. Identified a safe throughput limit of ~5 RPS on single-core hardware before CPU saturation leads to 504 Gateway Timeouts.
* **Security Implementation:** Secured public endpoints with API Key authentication middleware. Managed secrets via environment variables and GitHub Secrets for CI/CD.
* **Automated CI/CD:** Built a GitHub Actions pipeline that performs linting (flake8), security scanning (bandit), building, and SSH-based deployment to AWS EC2 upon every push to the main branch.

---

## 0x04. DEVELOPMENT METHODOLOGY

I follow a strict set of principles to ensure code quality and system reliability:

* **Infrastructure as Code (IaC):** Services are defined in `docker-compose.yml`, ensuring the environment is identical across development and production.
* **Observability First:** No service is deployed without health checks (`/health`) and metrics exposure (`/metrics`).
* **Security Left-Shift:** Credentials are never hardcoded. `.env` files and secret management are used from day one.
* **Documentation:** Detailed READMEs with architectural diagrams (Mermaid.js) and API specifications are standard for my repositories.

---

## 0x05. TELEMETRY / GITHUB STATS

<div align="center">
  <img src="https://github-readme-stats-eight-theta.vercel.app/api?username=Western-1&show_icons=true&theme=graywhite&hide_border=true" alt="GitHub Stats" />
  <br/>
  <img src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=Western-1&layout=compact&theme=graywhite&hide_border=true&langs_count=8" alt="Top Languages" />
</div>

<br/>
<div align="center">
  <i>"Reliability is the most important feature."</i>
</div>
