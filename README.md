<h1 align="center">👋 Hi, I'm Nguyen Tam Thang</h1>

<h3 align="center">AI Engineer | Computer Science Student at HCMUT</h3>

<p align="center">
  I build AI applications with a focus on retrieval, recommendation, evaluation, and reliable serving.
  My projects connect model experiments with APIs, user interfaces, and reproducible engineering evidence.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/thangnguyen0512/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&amp;logo=linkedin&amp;logoColor=white" alt="LinkedIn profile" /></a>
  <a href="https://www.facebook.com/ntt0512/"><img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&amp;logo=facebook&amp;logoColor=white" alt="Facebook profile" /></a>
  <a href="https://nguyentamthang.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&amp;logo=vercel&amp;logoColor=white" alt="Personal portfolio" /></a>
  <a href="mailto:thang.nguyen0512@hcmut.edu.vn"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&amp;logo=gmail&amp;logoColor=white" alt="Email Nguyen Tam Thang" /></a>
</p>

## 👨‍💻 About me

- 🎓 Computer Science student at **Ho Chi Minh City University of Technology (HCMUT, VNU-HCM)**.
- 🤖 Interested in **machine learning, recommender systems, information retrieval, and retrieval-augmented generation**.
- 🔬 I compare alternatives with explicit evaluation protocols, then document the quality, cost, and operational trade-offs.
- 🛠️ My hands-on work spans data preparation, model experiments, API development, Docker, CI, observability, and web demonstrations.

## 🌟 Featured projects

### 🛒 E-commerce Recommendation System

**Chronological recommendation evaluation, hybrid retrieval, and learned ranking on 2.76 million Retailrocket events.**

- Built a nine-fold rolling benchmark with cutoff-time catalogs, seen-item filtering, and separate warm/cold cohorts.
- Improved **HR@20 from 0.038518 to 0.054566 (+41.7% relative)** with learned ranking over the same candidate pool across **59,323 warm user-windows**. These are inspected folds 5–9: **post-selection diagnostics, not blind validation**. [Ranking report](https://github.com/Thazg/ecommerce-recsys/blob/v1.0.0/docs/LEARNED_RANKING_REPORT.md)
- Packaged the selected policy into a verified snapshot bundle and a **local FastAPI service**, with input guards, optional caching, metrics, and lifecycle checks. The local release preserved **101/101 reference outputs before and after restart**. [Local release evidence](https://github.com/Thazg/ecommerce-recsys/blob/v1.0.0/docs/LOCAL_RELEASE_REPORT.md)
- Published **RecoLens**, an explorer of stored model outputs, and **RecoMe**, a separate interactive shopping illustration. RecoMe computes browser-side suggestions; neither website hosts the Retailrocket model API.

**Tech:** Python, NumPy/SciPy, pandas/Parquet, implicit ALS, FastAPI, Docker, GitHub Actions, JavaScript

<p>
  <a href="https://github.com/Thazg/ecommerce-recsys"><img src="https://img.shields.io/badge/Source%20Code-181717?style=for-the-badge&amp;logo=github&amp;logoColor=white" alt="Recommendation system source code" /></a>
  <a href="https://ecommerce-recsys.vercel.app/"><img src="https://img.shields.io/badge/Model%20Explorer-1E477A?style=for-the-badge&amp;logo=vercel&amp;logoColor=white" alt="RecoLens stored-model explorer" /></a>
  <a href="https://shoprecome.vercel.app/"><img src="https://img.shields.io/badge/Shopping%20Demo-2563EB?style=for-the-badge&amp;logo=vercel&amp;logoColor=white" alt="RecoMe browser-side shopping demo" /></a>
</p>

### 🧠 Enterprise Knowledge Intelligence Platform

**Hybrid RAG over seven indexed technical-documentation collections, with cited answers and separate local/cloud runtime profiles.**

- Built the full pipeline from ingestion and chunking through embeddings, retrieval, grounded generation, API serving, and a Next.js interface with streamed answers and source citations.
- Benchmarked **Dense, BM25, Weighted RRF, Multi-Query, and reranking** on **100 manually verified retrieval queries**. Kept Weighted RRF as the deployed design after comparing quality and retrieval cost; Multi-Query and reranking remain evaluated alternatives. [Quality and latency trade-offs](https://github.com/Thazg/knowledge-intelligence-platform#why-v1-keeps-weighted-rrf)
- Local Weighted RRF reached **0.7247 MRR and 0.9300 Hit@10**. The cloud profile reached **0.7119 MRR and 0.9300 Hit@10**. [Retrieval results](https://github.com/Thazg/knowledge-intelligence-platform#measured-results)
- Verified **100/100 exact BM25 Top-10 orders** in a **500-chunk migration canary**; this is a sample parity check. [Parity evidence](https://github.com/Thazg/knowledge-intelligence-platform/blob/main/benchmarks/retrieval/reports/rank-bm25-qdrant-parity-canary-v1.json)
- Added dependency-aware readiness checks, request IDs, structured logging, Prometheus metrics, timeouts, bounded concurrency, admission control, CI, and regression tests.
- Built a validated **~130.5 MB cloud deployment image**, using FastEmbed and a compact BM25 query artifact to keep the full corpus and heavyweight local inference dependencies out of the cloud runtime. [Deployment characterization](https://github.com/Thazg/knowledge-intelligence-platform/blob/main/docs/04_evaluation_and_benchmarks.md#10-deployment-characterization)
- Deployed the API with **Render, Qdrant Cloud, and Groq**, alongside a **Vercel** web interface. The separate Docker Compose reference stack includes Qdrant, Ollama, Prometheus, and Grafana.

**Evaluation scope:** retrieval scores do not establish answer correctness. The frozen local Ollama E2E review passed runtime/structure checks, but its **semantic release gate did not pass**. [Decision report](https://github.com/Thazg/knowledge-intelligence-platform/blob/main/benchmarks/e2e/reports/e2e_v1_decision.md)

**Tech:** Python, FastAPI, Qdrant, BGE, BM25, FastEmbed, Docker, Next.js, GitHub Actions, Prometheus, Grafana

<p>
  <a href="https://github.com/Thazg/knowledge-intelligence-platform"><img src="https://img.shields.io/badge/Source%20Code-181717?style=for-the-badge&amp;logo=github&amp;logoColor=white" alt="Enterprise KIP source code" /></a>
  <a href="https://enterprisekip.vercel.app/"><img src="https://img.shields.io/badge/Web%20Demo-1E477A?style=for-the-badge&amp;logo=vercel&amp;logoColor=white" alt="Enterprise KIP web demo" /></a>
  <a href="https://enterprise-kip-api.onrender.com/docs"><img src="https://img.shields.io/badge/API%20Docs-009688?style=for-the-badge&amp;logo=fastapi&amp;logoColor=white" alt="Enterprise KIP API documentation" /></a>
</p>

The Render Free backend may take time to wake after inactivity.

### 💬 Nova RAG Workspace

**A full-stack workspace for uploading personal documents, asking questions, and inspecting the passages behind streamed answers.**

- Built document ingestion, account-scoped indexes, conversation history, and a React workspace with filename, PDF-page, and extracted-line source references.
- Kept **BM25 as the default retriever** and reused the application's parser, chunker, retriever, and context packer in offline evaluation. FAISS/RRF retrieval remains an explicit opt-in configuration.
- Recorded a **100-question benchmark over 10 checksum-pinned arXiv PDFs**: 160 pages, 555 chunks, 90 answerable and 10 unanswerable questions. Production-path BM25 reached **75/90 Page Hit@5 (83.33%) and 0.5541 MRR@5** on the answerable subset. [Pinned evaluation report](https://github.com/Thazg/NovaRAGChatBot/blob/a70087f2eeb1da56c36e21a3b424537c0b02b098/backend/evaluation/results.json)
- Added ownership checks, rotating refresh-token sessions, memory-only access tokens, bounded upload validation, and SSRF controls for remote PDF downloads.
- Implemented checksum-verified index revisions, cache invalidation, and deletion barriers for background indexing. Interrupted answer streams retain partial output and an incomplete status.
- Deployed the frontend on **Vercel** and the FastAPI backend on **Render**, with **Groq** for hosted generation and an **Ollama** option for local use.
- Added backend regression and retrieval gates, frontend build/unit checks, and **Playwright** browser tests in GitHub Actions. Browser fixtures check application behavior separately from model quality.

**Evaluation scope:** independent annotation review is pending. Unanswerable retrieval scored **0/10 correct abstentions**; there is no calibrated refusal threshold or human-validated generated-answer quality result. These retrieval scores do not establish chatbot factuality.

**Tech:** Python, FastAPI, BM25, FAISS (opt-in), React, TypeScript, Vite, Tailwind CSS, Groq/Ollama, Docker, Playwright, GitHub Actions

<p>
  <a href="https://github.com/Thazg/NovaRAGChatBot"><img src="https://img.shields.io/badge/Source%20Code-181717?style=for-the-badge&amp;logo=github&amp;logoColor=white" alt="Nova RAG Workspace source code" /></a>
  <a href="https://novachatbot.vercel.app/"><img src="https://img.shields.io/badge/Web%20Demo-1E477A?style=for-the-badge&amp;logo=vercel&amp;logoColor=white" alt="Nova RAG Workspace web demo" /></a>
  <a href="https://novaaiagent-4.onrender.com/docs"><img src="https://img.shields.io/badge/API%20Docs-009688?style=for-the-badge&amp;logo=fastapi&amp;logoColor=white" alt="Nova RAG Workspace API documentation" /></a>
</p>

### 🌐 Personal Portfolio

A responsive website presenting my projects, skills, education, and contact information, with reduced-motion support and a validated email contact form.

**Tech:** Next.js, React, TypeScript, Tailwind CSS, Framer Motion, Zod, Resend, Vercel

<p>
  <a href="https://github.com/Thazg/Portfolio"><img src="https://img.shields.io/badge/Source%20Code-181717?style=for-the-badge&amp;logo=github&amp;logoColor=white" alt="Personal portfolio source code" /></a>
  <a href="https://nguyentamthang.vercel.app/"><img src="https://img.shields.io/badge/Live%20Website-000000?style=for-the-badge&amp;logo=vercel&amp;logoColor=white" alt="Personal portfolio website" /></a>
</p>

## 🛠️ Tech stack

| Area | Tools and methods |
| :--- | :--- |
| **🧠 ML & data** | <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&amp;logo=python&amp;logoColor=white" alt="Python" height="20" /> <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&amp;logo=pytorch&amp;logoColor=white" alt="PyTorch" height="20" /> <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&amp;logo=numpy&amp;logoColor=white" alt="NumPy" height="20" /> <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&amp;logo=scipy&amp;logoColor=black" alt="SciPy" height="20" /> <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&amp;logo=pandas&amp;logoColor=white" alt="pandas" height="20" /> <img src="https://img.shields.io/badge/Parquet-2563EB?style=flat-square" alt="Parquet" height="20" /> |
| **🔎 Retrieval & ranking** | <img src="https://img.shields.io/badge/implicit%20ALS-2563EB?style=flat-square" alt="implicit ALS" height="20" /> <img src="https://img.shields.io/badge/ItemKNN-1E477A?style=flat-square" alt="ItemKNN" height="20" /> <img src="https://img.shields.io/badge/Learned%20ranking-1E477A?style=flat-square" alt="Learned ranking" height="20" /> <img src="https://img.shields.io/badge/BM25-4B8BBE?style=flat-square" alt="BM25" height="20" /> <img src="https://img.shields.io/badge/Hybrid%20rank%20fusion-1E477A?style=flat-square" alt="Hybrid rank fusion" height="20" /> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&amp;logo=qdrant&amp;logoColor=white" alt="Qdrant" height="20" /> <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&amp;logo=huggingface&amp;logoColor=black" alt="Hugging Face" height="20" /> <img src="https://img.shields.io/badge/SentenceTransformers-2455A6?style=flat-square" alt="SentenceTransformers" height="20" /> <img src="https://img.shields.io/badge/FastEmbed-FF6B6B?style=flat-square" alt="FastEmbed" height="20" /> <img src="https://img.shields.io/badge/FAISS-2563EB?style=flat-square" alt="FAISS" height="20" /> |
| **⚙️ Backend** | <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&amp;logo=fastapi&amp;logoColor=white" alt="FastAPI" height="20" /> <img src="https://img.shields.io/badge/Pydantic-E92063?style=flat-square&amp;logo=pydantic&amp;logoColor=white" alt="Pydantic" height="20" /> <img src="https://img.shields.io/badge/REST%20APIs-1E477A?style=flat-square" alt="REST APIs" height="20" /> |
| **💻 Web** | <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&amp;logo=nextdotjs&amp;logoColor=white" alt="Next.js" height="20" /> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&amp;logo=react&amp;logoColor=61DAFB" alt="React" height="20" /> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&amp;logo=typescript&amp;logoColor=white" alt="TypeScript" height="20" /> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&amp;logo=javascript&amp;logoColor=black" alt="JavaScript" height="20" /> <img src="https://img.shields.io/badge/Tailwind%20CSS-0F172A?style=flat-square&amp;logo=tailwindcss&amp;logoColor=38BDF8" alt="Tailwind CSS" height="20" /> <img src="https://img.shields.io/badge/Framer%20Motion-0055FF?style=flat-square&amp;logo=framer&amp;logoColor=white" alt="Framer Motion" height="20" /> <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&amp;logo=vite&amp;logoColor=white" alt="Vite" height="20" /> |
| **🚀 Engineering** | <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&amp;logo=git&amp;logoColor=white" alt="Git" height="20" /> <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&amp;logo=githubactions&amp;logoColor=white" alt="GitHub Actions" height="20" /> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&amp;logo=docker&amp;logoColor=white" alt="Docker" height="20" /> <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&amp;logo=prometheus&amp;logoColor=white" alt="Prometheus" height="20" /> <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&amp;logo=grafana&amp;logoColor=white" alt="Grafana" height="20" /> <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&amp;logo=ollama&amp;logoColor=white" alt="Ollama" height="20" /> <img src="https://img.shields.io/badge/Render-000000?style=flat-square&amp;logo=render&amp;logoColor=white" alt="Render" height="20" /> <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&amp;logo=vercel&amp;logoColor=white" alt="Vercel" height="20" /> <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square" alt="Playwright" height="20" /> |
| **⌨️ Languages** | <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&amp;logo=cplusplus&amp;logoColor=white" alt="C++" height="20" /> <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&amp;logo=openjdk&amp;logoColor=white" alt="Java" height="20" /> <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square" alt="SQL" height="20" /> |

These tools span different projects and runtime profiles; each repository documents its implemented stack and evaluated alternatives.

## 🎯 Current focus

- Strengthening my foundations in machine learning and deep learning.
- Building recommendation and RAG systems with explicit evaluation protocols and reproducible results.
- Improving the connection between model quality, resource cost, API behavior, and user experience.
- Exploring multimodal AI as a further learning direction.
