
# 🧠 AgnoAgents — Multi-Agent GenAI System with Groq, GPT-4o, and Phidata

A high-performance agentic AI system built using **Agno (Phidata)** to orchestrate **Groq LPU** and **GPT-4o** agents for real-time financial analysis, web search, and document Q&A — powered by vector memory, prompt chaining, and modular teamwork.

---

## 🚀 Features

- 🤖 **Multi-Agent Orchestration** with Agno (Phidata)
- ⚡ **Real-Time Inference** via Groq LPU + OpenAI GPT-4o
- 📄 **PDF Knowledge Base** with LanceDB + OpenAI Embeddings
- 🔍 **Live Financial Data** via YFinance agent
- 🌐 **Real-Time Web Search** with DuckDuckGo
- 🧠 **Agent Memory + Hybrid Vector Search**
- 🧰 FastAPI + Playground CLI for local testing

---

## 🧩 Architecture

```mermaid
graph TD;
  UserQuery --> AgentTeam
  AgentTeam -->|Delegates| FinancialAgent
  AgentTeam -->|Delegates| WebAgent
  AgentTeam -->|Delegates| PDFMemoryAgent
  FinancialAgent --> YFinanceTools
  WebAgent --> DuckDuckGoTools
  PDFMemoryAgent --> LanceDB
  PDFMemoryAgent --> OpenAIEmbeddings
  AgentTeam --> OutputFormatter
````

---

## 📦 Tech Stack

| Component       | Technology Used                     |
| --------------- | ----------------------------------- |
| LLM Inference   | Groq LPU (Qwen 2.5, LLaMA3), GPT-4o |
| Agent Framework | Agno / Phidata                      |
| Vector DB       | LanceDB                             |
| Embeddings      | OpenAI (`text-embedding-3-small`)   |
| Tools           | DuckDuckGo, YFinance                |
| Interface       | FastAPI + CLI Playground            |

---

## 🧠 Agents

* **Financial Agent**: Real-time stock analysis using YFinance APIs
* **Web Agent**: Live search with DuckDuckGoTools (Groq LPU)
* **PDF Agent**: Memory-based answers using LanceDB + embedded PDFs

---

## 📂 Example Workflow

1. User asks: `"Summarize the financial status of NVDA"`
2. Team routes the task:

   * Financial Agent pulls YFinance data
   * Web Agent pulls latest news
   * PDF Agent checks memory if NVDA is present
3. Results are formatted with markdown + tables
4. Output is streamed live

---

## 🛠️ Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/arunkatika/agnoagent.git
cd agnoagent
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Setup `.env` for API keys

```env
OPENAI_API_KEY=your-key
PHI_API_KEY=your-key
GROQ_API_KEY=your-key
```

### 4. Run Playground App

```bash
python playground.py
```

---

## 📎 Sample Query

```python
multi_ai_agent.run("Get the analyst summary for Tesla and latest updates from news.")
```

---

## 🧪 Use Cases

* Internal finance assistant
* Research Q\&A from reports
* Agent collaboration demos
* Hybrid knowledge search

---

## 🧑‍💻 Author

**Arun Kumar Reddy Katika**
[LinkedIn](https://linkedin.com/in/arunkatika) · [GitHub](https://github.com/arunkatika)

---
