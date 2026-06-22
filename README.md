# 🛡️ GIL: Multi-Agent Intelligence Swarm (Enterprise Edition)

**Global Intelligence Liaison (GIL)** is a strategic geopolitical intelligence desk powered by a highly orchestrated **Multi-Agent Swarm**. Designed for enterprise-grade performance, GIL dynamically processes ambiguous queries, fetches real-time data, and synthesizes complex intelligence using an **Ephemeral RAG** architecture and **Self-Healing Semantic Caching**.

## 🧠 Swarm Architecture & High-Performance Pipeline

GIL utilizes a **7-Agent Pipeline** built with LangChain (LCEL) to ensure high accuracy and low latency:

1.  **Agent 1: The Clarifier (Time-Aware):** Analyzes intent and auto-corrects queries. It uses **Dynamic Date Injection** to ground relative time (e.g., "last 2 days") into absolute calendar dates.
2.  **Agent 2: The Expander (Search Strategist):** Generates 3 optimized search variations while maintaining a **Context Anchor** to prevent subject drift.
3.  **Agent 3: Multi-Source Fetcher:**
    * *Targeted Search:* Queries verified defense/news domains via SerpAPI.
    * *URL/API Ingestion:* Dynamically scrapes and parses user-provided links using BeautifulSoup.
4.  **Agent 4: The Synthesizer:** Resolves contradictions and highlights multimodal evidence (satellite, video).
5.  **Agent 5: The Final Responder:** Formats intelligence into a strict **SITREP** or **Strategic Analysis** based on dynamic path routing.
6.  **Agent 6: Background Cache Manager:** A persistent FAISS store that serves identical requests instantly.
7.  **The Quality Gate (Self-Healing):** A background process that inspects cached responses. If a response contains "no data found," it is flagged as "poisoned" and bypassed to ensure only high-quality intelligence is served.

## 🚀 Key Enterprise Features

* **Asynchronous Processing:** Final responses are delivered immediately while caching tasks run in the background via FastAPI `BackgroundTasks`.
* **Model Agnostic (OpenRouter):** Integrated with OpenRouter to allow seamless switching between LLMs (Gemini, Claude, Llama).
* **Zero-Hallucination Policy:** The system is instructed to admit lack of data rather than fabricating intelligence.

## 🛠️ Tech Stack

* **Orchestration:** LangChain (LCEL)
* **Backend:** FastAPI (Microservice Architecture)
* **LLM:** openrouter/free (via OpenRouter)
* **Vector DB:** FAISS (Local persistent store)
* **Deployment:** Docker & Docker Compose

## 📋 Environment Setup

Create a `.env` file:
```env
OPENROUTER_API_KEY="your_key"
SERPAPI_API_KEY="your_key"
```

## 🚀 Deployment

### Docker (Recommended)
```bash
docker-compose up --build
```
The system is deployed at `https://huggingface.co/spaces/Ounaa2003/gil-intelligence-swarm`.

---
**Author:** Oun Alawamleh
*AI Engineer*
