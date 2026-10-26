<h1 align="center">Hi, I'm Nguyen Tam Thang</h1>

<h3 align="center">AI Engineer | Computer Science Student at HCMUT</h3>

<p align="center">
  I build AI applications with a focus on retrieval, recommendation, evaluation, and reliable serving.
  My projects connect model experiments with APIs, user interfaces, and reproducible engineering evidence.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/thangnguyen0512/">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn profile" />
  </a>
  <a href="https://nguyentamthang.vercel.app/">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Personal portfolio" />
  </a>
  <a href="mailto:thang.nguyen0512@hcmut.edu.vn">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Nguyen Tam Thang" />
  </a>
</p>

## About me

- Computer Science student at **Ho Chi Minh City University of Technology (HCMUT, VNU-HCM)**.
- Interested in **machine learning, recommender systems, information retrieval, and retrieval-augmented generation**.
- I compare alternatives with explicit evaluation protocols, then document the quality, cost, and operational trade-offs.
- My hands-on work spans data preparation, model experiments, API development, Docker, CI, observability, and web demonstrations.

## Featured projects

### E-commerce Recommendation System

**Chronological recommendation evaluation, hybrid retrieval, and learned ranking on 2.76 million Retailrocket events.**

- Built a nine-fold rolling benchmark with cutoff-time catalogs, seen-item filtering, and separate warm/cold cohorts.
- Improved **HR@20 from 0.038518 to 0.054566 (+41.7% relative)** with learned ranking over the same candidate pool across **59,323 warm user-windows**. These are inspected folds 5–9: **post-selection diagnostics, not blind validation**. [Ranking report](https://github.com/Thazg/ecommerce-recsys/blob/v1.0.0/docs/LEARNED_RANKING_REPORT.md)
- Packaged the selected policy into a verified snapshot bundle and a **local FastAPI service**, with input guards, optional caching, metrics, and lifecycle checks. The local release preserved **101/101 reference outputs before and after restart**. [Local release evidence](https://github.com/Thazg/ecommerce-recsys/blob/v1.0.0/docs/LOCAL_RELEASE_REPORT.md)
- Published **RecoLens**, an explorer of stored model outputs, and **RecoMe**, a separate interactive shopping illustration. RecoMe computes browser-side suggestions; neither website hosts the Retailrocket model API.

**Tech:** Python, NumPy/SciPy, pandas/Parquet, implicit ALS, FastAPI, Docker, GitHub Actions, JavaScript

[Source](https://github.com/Thazg/ecommerce-recsys) | [Model explorer](https://ecommerce-recsys.vercel.app/) | [Shopping demo](https://shoprecome.vercel.app/)

### Enterprise Knowledge Intelligence Platform

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

[Source](https://github.com/Thazg/knowledge-intelligence-platform) | [Web demo](https://enterprisekip.vercel.app/) | [API docs](https://enterprise-kip-api.onrender.com/docs)

The Render Free backend may take time to wake after inactivity.

### Personal Portfolio

A responsive website presenting my projects, skills, education, and contact information, with reduced-motion support and a validated email contact form.

**Tech:** Next.js, React, TypeScript, Tailwind CSS, Framer Motion, Zod, Resend, Vercel

[Source](https://github.com/Thazg/Portfolio) | [Live website](https://nguyentamthang.vercel.app/)

## Technologies I work with

| Area | Tools and methods |
| :--- | :--- |
| ML and data | Python, PyTorch, NumPy, SciPy, pandas, Parquet |
| Recommendation and retrieval | implicit ALS, ItemKNN, learned ranking, BM25, hybrid rank fusion, Qdrant, Hugging Face, SentenceTransformers, FastEmbed |
| Backend | FastAPI, Pydantic, REST APIs |
| Web | Next.js, React, TypeScript, JavaScript, Tailwind CSS, Framer Motion |
| Engineering and operations | Git, GitHub Actions, Docker, Prometheus, Grafana, Ollama, Render, Vercel |
| Additional languages | C++, Java, SQL |

These tools span different projects and runtime profiles; each repository documents its implemented stack and evaluated alternatives.

## Current focus

- Strengthening my foundations in machine learning and deep learning.
- Building recommendation and RAG systems with explicit evaluation protocols and reproducible results.
- Improving the connection between model quality, resource cost, API behavior, and user experience.
- Exploring multimodal AI as a further learning direction.

<p align="center">
  <a href="https://www.linkedin.com/in/thangnguyen0512/">LinkedIn</a> &nbsp;|&nbsp;
  <a href="mailto:thang.nguyen0512@hcmut.edu.vn">Email</a> &nbsp;|&nbsp;
  <a href="https://nguyentamthang.vercel.app/">Portfolio</a> &nbsp;|&nbsp;
  <a href="https://www.facebook.com/ntt0512/">Facebook</a>
</p>
