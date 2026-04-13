<h1 align="center">Hi, I'm Eman Chaudhary </h1>
<h3 align="center">Full-Stack AI Engineer · Generative AI · LLM & RAG Systems  · NUST '26</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/eman-chaudhary/"><img src="https://img.shields.io/badge/LinkedIn-eman--chaudhary-0A66C2?style=flat&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:eman.abc05@gmail.com"><img src="https://img.shields.io/badge/Email-eman.abc05@gmail.com-D14836?style=flat&logo=gmail&logoColor=white"/></a>
  
</p>

---

## About Me

I'm a Software Engineering undergraduate at **NUST, Islamabad** (graduating May 2026), building production-grade AI systems across the full stack — from LLM fine-tuning and RAG pipeline architecture to React/FastAPI applications and cloud deployment.

-  **Mitacs Globalink Research Scholar**: AI intern at Brock University (2026), building automated Root Cause Analysis systems with Code Llama + RAG
-  **NASA OSDR AIML Working Group**: ML on space biology imaging datasets (OSD-366)
-  **Previously: Machine Learning Intern @ SINES EmbedAIoT Lab** — Architected edge-optimized CNNs for 5G channel estimation (Published at ICODT 2025)
-  **Previously:** SWE Intern @ Apna-Wifi (NSTP)

---

## Featured Projects & Research

### [AI-Driven Customer Service Assistant for NUST Bank (RAG System)](https://github.com/eman-abc/nust-bank-llm-assistant)
> `Gemma-3-4B`, `PEFT/LoRA`, `Qdrant`, `sentence-transformers`, `Presidio`, `Celery`, `FastAPI`, `Redis`, `Gradio`, `Docker`
- Architected an end-to-end Retrieval-Augmented Generation (RAG) pipeline for a banking assistant,
integrating hybrid retrieval (dense semantic search via all-MiniLM-L6-v2 embeddings + BM25 sparse retrieval)
with a cross-encoder reranker (ms-marco-MiniLM-L-6-v2) to maximize context precision and reduce
hallucinations.
- Fine-tuned Gemma-3-4B using PEFT/LoRA (rank=8, alpha=16) on domain-specific banking FAQs and policy
documents, achieving convergence in under 10 epochs on a single GPU while preserving base model generalization.
- Built a multi-layered safety guardrails framework: pre-LLM prompt injection detection via DeBERTa-based
classifiers, post-LLM confidence gating (similarity threshold 0.8), and regex-based PII leak prevention on generated
outputs.
- Engineered a zero-trust data pipeline using Presidio and spaCy NER for full PII anonymization (names,
account numbers, addresses) before ingestion, combined with semantic chunking (512-token chunks) and async
document processing via Celery workers and Redis task queuing.
- Deployed vectors in Qdrant with real-time indexing to support live knowledge base updates without model
retraining, achieving sub-second response times via FastAPI asynchronous backend architecture
---

### [LeadStream-Voice: AI-Powered B2B Call Triage Platform](https://github.com/eman-abc/LeadStream-voice)
> `Node.js` `TypeScript` `Groq API (Llama-3.1)` `Vapi` `Docker` `Render` `WebSockets`
> > **[Live Demo](https://dino-voice.onrender.com)**

Real-time voice AI triage agent for deterministic lead qualification and CRM dispatch.
- Engineered a native TypeScript state machine for routing and entity-aware conversational state, eliminating framework overhead (zero LangChain/LangGraph dependencies).
- Implemented a 3-layer hallucination defense system utilizing API-level stop sequences, full conversation history context, and post-processing regex to strictly prevent LLM autocomplete behaviors.
- Built a robust webhook controller to handle Vapi audio stream events, featuring an echo deduplication guard to prevent transcription feedback loops.
- Architected an asynchronous end-of-call pipeline using Groq (JSON mode) for reliable entity extraction (`{name, email}`) and one-sentence problem summaries for direct CRM injection.
- Deployed as a containerized webhook service via **Docker** on **Render**, featuring an in-memory session tracker and WebSockets to broadcast real-time call states to a live dashboard.


### [Autonomous AI Research Agent & Workflow Orchestration](https://github.com/eman-abc)
> `n8n` `Python` `Gemini 2.0` `LangGraph` `RAG` `Tavily API` `Vector Databases`

Multi-agent automation system for complex intelligence workflows.
- Engineered an Agentic RAG pipeline using **n8n** visual orchestration for dynamic vector DB querying + live web search
- Designed a Researcher LLM + Editor LLM collaboration architecture for end-to-end workflow automation
- Applied **LangGraph** orchestration: ReAct loops, tool calling, and specialist agent handoffs (Sequential, Routing, Handoff patterns)

---

### [SmartSketch: AI-Powered Forensic Facial Image Generator](https://github.com/eman-abc/smartsketch-ml)
> `SDXL 1.0` `LoRA` `ControlNet` `Qwen2.5-3B` `OpenAI CLIP` `PyTorch` `FastAPI`

Generative AI pipeline for text-guided forensic face synthesis.
- Integrated SDXL 1.0 with custom LoRA adapters + ControlNet, reducing synthesis time by **50% (~8.1s/edit)**
- Deployed **Qwen2.5-3B-Instruct** as an AI Agent orchestration layer for prompt validation, tool calling & safety gates — **95% task success rate**
- Evaluated via OpenAI CLIP (semantic alignment) and ArcFace biometric matching (**45.6% identity preservation**)
---

### [Edge AI for 5G: Lightweight CNNs for Channel Estimation][(https://github.com/Muqadas2/Deep-Learning-Data-Synthesis-for-5G-channel-estimation)]
> `PyTorch` `NVIDIA Jetson` `INT8 Quantization` `Structured Pruning` `Edge AI`

*Machine Learning Research Intern @ SINES EmbedAIoT Lab, NUST*
- Architected novel lightweight CNN and CNN-Transformer architectures (101–745 parameters) for 5G mmWave channel estimation on edge devices
- Achieved NMSE as low as -11.9 dB with **<1 ms inference latency** via INT8 quantization and structured pruning on NVIDIA Jetson hardware
- Benchmarked models demonstrating superior accuracy-efficiency trade-offs
- **Published:** [Results accepted for publication at the International Conference on Digital Technologies (ICODT 2025)](https://ieeexplore.ieee.org/document/11360709)

---

### [Lightweight CNN-BiGRU for Human Activity Recognition](https://github.com/eman-abc/HAR)
> `TensorFlow` `PyTorch` `Knowledge Distillation` `INT8 Quantization` `Structured Pruning`

Ultra-efficient deep learning for wearable edge devices.
- Achieved **99.7% parameter reduction** (33.7M → 90,066) while improving Macro F1 to **87.08%**
- Built a Teacher-Student Knowledge Distillation framework: 2,790-parameter CNN student from a Transformer teacher
- Compressed final model to **27.45 KB** via INT8 quantization, weight pruning (~50% sparsity) & weight clustering

---

### [Full-Stack & Cloud Platforms (Vid City + MERN Marketplace)](https://github.com/eman-abc)
> `React` `Node.js` `Express.js` `MongoDB` `GCP` `Docker` `REST APIs`

- Engineered a video streaming platform using microservices architecture deployed on **Google Cloud Platform**
- Built a full-stack MERN e-commerce + mentorship marketplace with role-based auth (buyer / seller / admin dashboards)
- Containerized with Docker, documented REST APIs, Git-based collaborative workflows

---

## Tech Stack

**AI & LLM Engineering**
```text
LLM Fine-Tuning (LoRA/PEFT) · RAG Pipelines · AI Agents · Prompt Engineering
LangChain · LlamaIndex · LangGraph · n8n · FAISS · Semantic Search
Gemma 3 · Qwen · Code Llama · BERT · DistilBERT · SDXL · ControlNet

```

**ML & Deep Learning**

```text
PyTorch · TensorFlow · Hugging Face (transformers + diffusers)
Knowledge Distillation · INT8 Quantization · Structured Pruning · OpenAI CLIP
Edge AI Deployment (NVIDIA Jetson)

```

**Full-Stack & Backend**

```text
Python · FastAPI · Django · Node.js · Express.js · React · Next.js · REST APIs

```

**Databases & Cloud**

```text
FAISS · PostgreSQL · MongoDB · MySQL · Docker · GCP · AWS (S3) · Git · Linux

```

---

## 🏆 Highlights

|  |  |
| --- | --- |
| 🎓 **Mitacs Globalink Scholar** | Fully-funded AI research, Brock University, Canada (2026) |
| 📄 **ICODT 2025 Publication** | Lightweight CNNs for 5G mmWave channel estimation <br>

<br> [Read Paper ([https://www.google.com/search?q=%23](https://ieeexplore.ieee.org/document/11360709))]|
| **NUST** | B.E. Software Engineering — Class of 2026 |

---

<p align="center">
<i>Open to full-time roles and research collaborations in AI/ML Engineering · Available from June 2026</i>
</p>
