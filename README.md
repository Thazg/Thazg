<div align="center">

# 👋 Hi, I'm Nguyen Tam Thang

### AI Engineer | Computer Science Student at HCMUT

I enjoy building practical AI systems, experimenting with different approaches, and turning what I learn into applications that can be evaluated and deployed.

<br />

<div>
  <a href="https://www.linkedin.com/in/thangnguyen0512/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://www.facebook.com/ntt0512/" target="_blank">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook" />
  </a>
  <a href="https://nguyentamthang.vercel.app/" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" />
  </a>
</div>

</div>

---

## 👨‍💻 About Me

- 🎓 Computer Science student at **Ho Chi Minh City University of Technology (HCMUT - VNU-HCM)**.
- 🤖 Interested in **AI Engineering, Machine Learning, Retrieval-Augmented Generation, and information retrieval**.
- 🔬 I like experimenting with different approaches and evaluating them with real benchmarks instead of relying only on intuition.
- 🛠️ I enjoy working across the full development process, from model and retrieval experiments to APIs, Docker, CI, deployment, and monitoring.
- 📚 Currently building my foundation in machine learning, deep learning, and production AI systems.

---

## 🛠️ Tech Stack

### 🤖 AI / ML & Retrieval

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face" />
  <img src="https://img.shields.io/badge/SentenceTransformers-000000?style=for-the-badge" alt="SentenceTransformers" />
  <img src="https://img.shields.io/badge/BM25-4B8BBE?style=for-the-badge" alt="BM25" />
  <img src="https://img.shields.io/badge/Hybrid%20Search-6C63FF?style=for-the-badge" alt="Hybrid Search" />
  <img src="https://img.shields.io/badge/FastEmbed-FF6B6B?style=for-the-badge" alt="FastEmbed" />
</p>

### ⚙️ Backend & Data

<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge&logo=qdrant&logoColor=white" alt="Qdrant" />
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white" alt="Pydantic" />
  <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas" />
</p>

### 🚀 Tools & Infrastructure

<p>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" alt="Prometheus" />
  <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Grafana" />
  <img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white" alt="Ollama" />
  <img src="https://img.shields.io/badge/Render-000000?style=for-the-badge&logo=render&logoColor=white" alt="Render" />
</p>

### 💻 Programming

<p>
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="C++" />
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
</p>

---

## 🌟 Featured Projects

### 🧠 Enterprise Knowledge Intelligence Platform

**Production-minded Retrieval-Augmented Generation platform for technical documentation.**

I built this project to go beyond a basic RAG demo and explore how retrieval quality, generation reliability, evaluation, deployment, and operational constraints affect a real AI system.

**Highlights:**

- Built the full pipeline from ingestion and chunking to embeddings, retrieval, generation, API serving, and deployment.
- Benchmarked **Dense, BM25, Weighted RRF, Multi-Query, and reranking** across 100 retrieval queries.
- Selected Weighted RRF with **0.7247 MRR** and **0.9300 Hit@10**.
- Reproduced local BM25 ranking in Qdrant Cloud with **100/100 exact top-10 parity** in the parity canary.
- Added readiness checks, metrics, request IDs, timeouts, admission control, CI, and regression testing.
- Built a lightweight cloud deployment image of approximately **130.5 MB**.
- Deployed the system publicly with **Render + Qdrant Cloud + Groq**.

**Tech:** Python, FastAPI, Qdrant, BGE, BM25, FastEmbed, Docker, GitHub Actions, Prometheus, Grafana

<p>
  <a href="https://github.com/Thazg/knowledge-intelligence-platform">
    <img src="https://img.shields.io/badge/Source%20Code-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://enterprise-kip-api.onrender.com/docs">
    <img src="https://img.shields.io/badge/Live%20API-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  </a>
</p>

---

### 🌐 Personal Portfolio

My personal website for presenting my projects, skills, and background.

**Tech:** Next.js, Tailwind CSS, Framer Motion

<p>
  <a href="https://github.com/Thazg/Portfolio">
    <img src="https://img.shields.io/badge/Source%20Code-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://nguyentamthang.vercel.app/">
    <img src="https://img.shields.io/badge/Live%20Website-000000?style=for-the-badge&logo=vercel&logoColor=white" />
  </a>
</p>

---

## 🎯 What I'm Working Toward

I'm currently focused on strengthening my foundations in:

- Machine Learning and Deep Learning
- Retrieval and RAG systems
- Multimodal AI
- Model evaluation and experimentation
- Production AI engineering

My goal is to keep building projects where I can understand not only **how to make a model or system work**, but also **how to evaluate it, improve it, and deploy it reliably**.

---

<div align="center">

### 📫 Connect with me

<a href="mailto:thang.nguyen0512@hcmut.edu.vn">
  <img src="https://img.shields.io/badge/Email-thang.nguyen0512%40hcmut.edu.vn-D14836?style=flat-square&logo=gmail&logoColor=white" />
</a>
<a href="https://www.linkedin.com/in/thangnguyen0512/">
  <img src="https://img.shields.io/badge/LinkedIn-Thang%20Nguyen-0077B5?style=flat-square&logo=linkedin&logoColor=white" />
</a>

</div>
