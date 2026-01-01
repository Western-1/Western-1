<div align="center">
  <h1>ANDRIY VLONHA</h1>
  <img src="https://img.shields.io/badge/Open%20to-Junior%20MLOps-orange?style=for-the-badge" alt="Open to work" />
  <h3>Junior MLOps Engineer | Cloud &amp; Infrastructure</h3>
  <p>
    <b>Specializing in High-Availability NLP Systems, Container Orchestration, Automated Deployment Pipelines, and Production-Grade RAG Microservices.</b>
  </p>
  <p>
    <a href="https://www.linkedin.com/in/андрій-влонга-9562b537b" rel="noopener">
      <img src="https://img.shields.io/badge/Connect_on_LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
    </a>
    <a href="mailto:andriy.vlonha.dev@gmail.com">
      <img src="https://img.shields.io/badge/Contact_via_Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
    </a>
  </p>
</div>
<hr/>
## 0x01. SYSTEM STATUS / INTRODUCTION
I am a Computer Science student and an aspiring MLOps Engineer focusing on the intersection of Software Engineering and Machine Learning. My primary interest lies not just in model training, but in the **operationalization of ML models**—ensuring they are served reliably, scalably, and securely in production environments.

I approach infrastructure with a software engineering mindset: strictly typed, version-controlled, and tested. My goal is to build systems where deployment is a boring, predictable event rather than a stressful manual process. I've built end-to-end solutions like a low-latency NLP inference service deployed on AWS with CI/CD, monitoring, and security, as well as an enterprise-grade RAG system for document querying with advanced retrieval, observability, and evaluation pipelines.

**Current Focus:**
* Developing low-latency microservices for NLP inference and RAG systems, optimized for resource-constrained environments (e.g., AWS t3.micro with 1GB RAM).
* Optimizing Docker container sizes, build times, and multi-stage builds for efficient deployments.
* Implementing strict observability standards (Prometheus/Grafana/Langfuse) with real-time metrics, tracing, and alerting.
* Enhancing ML reproducibility through pinned model versions (e.g., Git SHA hashes for Hugging Face models) and automated evaluation (Ragas, W&B).
* Exploring Kubernetes for scalable orchestration and integrating tools like FlashRank for advanced reranking in RAG pipelines.

For details on my skills and projects:
- [Technical Proficiency](./technical-proficiency.md)
- [Featured Projects](./featured-projects.md)

---
## 0x04. DEVELOPMENT METHODOLOGY
I follow a strict set of principles to ensure code quality and system reliability:
* **Infrastructure as Code (IaC):** Services are defined in `docker-compose.yml` and Kubernetes manifests, ensuring environments are identical across development, testing, and production.
* **Observability First:** No service is deployed without health checks (`/health`), metrics exposure (`/metrics`), and tracing (e.g., Langfuse decorators for token counts and latency).
* **Security Left-Shift:** Credentials are never hardcoded; use `.env` files, GitHub Secrets, and API key authentication from day one. Implement SSL/TLS with auto-renewal (Let's Encrypt).
* **Documentation:** Detailed READMEs with architectural diagrams (Mermaid.js), API specifications (Swagger), setup guides, and troubleshooting sections.
* **Testing & Quality:** Unit/integration tests with Pytest and mocking; linting with Ruff/Flake8; security scans with Bandit; load testing with Locust to identify bottlenecks (e.g., RPS limits).
* **CI/CD Automation:** GitHub Actions for linting, testing, building, and deploying to AWS EC2 or Kubernetes, triggered on every push to main.
* **MLOps Practices:** Experiment tracking with Weights & Biases (W&B), model versioning to prevent silent failures, and scheduled tasks (e.g., APScheduler for data archiving to S3).
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
