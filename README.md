# SmartDocMate — Distributed Document Intelligence Pipeline

> AI-powered document classification and summarization at scale. Built for the **IIIT Madras Appian AI Application Challenge** — Top 15 nationally.

![Python](https://img.shields.io/badge/Python-0d1117?style=flat-square&logo=python&logoColor=58a6ff)
![React](https://img.shields.io/badge/React-0d1117?style=flat-square&logo=react&logoColor=61dafb)
![Redis](https://img.shields.io/badge/Redis-0d1117?style=flat-square&logo=redis&logoColor=dc382d)
![Celery](https://img.shields.io/badge/Celery-0d1117?style=flat-square&logo=celery&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-0d1117?style=flat-square&logo=huggingface&logoColor=yellow)

---

## What it does

SmartDocMate is a distributed document intelligence pipeline that automates classification and summarization of unstructured financial documents. Instead of manual review, documents are ingested, classified by type and owner, and summarized — all in parallel across async workers.

**Key results:**
- **30x throughput improvement** over sequential processing
- Handles **250+ documents** in batch
- Covers PDFs, images, and text files across multiple languages
- Processes **5+ government ID types** (national IDs, driving licences, voter IDs) across India and the UAE

---

## Architecture

```
Document Upload (React drag-and-drop)
        ↓
  Celery Task Queue (Redis broker)
        ↓
  LayoutLMv3 Classification + Summarization
        ↓
  Owner Association (name / ID / email matching)
        ↓
  Voice AI Assistant + Results Dashboard
```

---

## Features

- **Hierarchical classification** — associates documents to the correct individual and categorizes by type (applications, identity documents, receipts)
- **Batch processing** — Redis + Celery queue handles large volumes with fault-tolerant execution
- **Multilingual support** — processes documents in multiple languages
- **Voice-enabled assistant** — communicates key document details interactively
- **Drag-and-drop UI** — React frontend with confidence score display

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React |
| Classification | HuggingFace LayoutLMv3 |
| OCR | Tesseract |
| Task Queue | Celery + Redis |
| Deployment | Streamlit Cloud (backend), Vercel (frontend) |

---

## Setup

```bash
# Backend
cd backend
pip install -r requirements.txt
streamlit run app.py

# Frontend
cd frontend
npm install
npm start
```

---

## Contributors

- Mir Inayat Ahmed
- Mohammed Muqeet Us Salam
- Abdullah Shaikh
- Armaan Rashid Pathan
