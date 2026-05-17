# Anthropic Agent Lab

Hands-on **AI agent** notebooks built with the [Anthropic Claude API](https://docs.anthropic.com/): custom tools, multi-turn agent loops, streaming, web search, code execution, extended thinking, and hybrid RAG retrieval.

> These notebooks implement **agentic patterns**: the model plans, calls tools, receives results, and continues until the task is done.

---

## About this project

This repository contains coursework and exercises from **Anthropic's official AI training** (Claude API / agent development curriculum). The notebooks document my progress learning production-style **agentic AI** patterns — tool orchestration, control loops, and retrieval — not single-shot prompts.

---

## What this repo demonstrates

| Capability | Description |
|------------|-------------|
| **Custom tools** | JSON schemas, Python handlers, `tool_use` / `tool_result` flow |
| **Agent control loop** | Repeat until `stop_reason != "tool_use"` |
| **Multi-step agents** | Chaining tools across turns (e.g. datetime → reminder) |
| **Coding agents** | Text-editor tool (view, replace, create, undo) |
| **Streaming agents** | Streamed responses with live tool use |
| **Built-in tools** | Web search, sandboxed code execution |
| **Reasoning agents** | Extended thinking for harder tasks |
| **RAG foundations** | Hybrid BM25 + vector retrieval |

---

## Notebooks

| File | Focus |
|------|--------|
| `01-custom-tools-agent-loop.ipynb` | Custom tools + full agent loop |
| `02-text-editor-coding-agent.ipynb` | File-editing coding agent |
| `03-streaming-agent.ipynb` | Streaming + tool loop |
| `04-web-search-agent.ipynb` | Agent with live web search |
| `05-code-execution-agent.ipynb` | Agent with code execution |
| `06-extended-thinking-agent.ipynb` | Extended thinking / reasoning |
| `07-hybrid-rag-retrieval.ipynb` | Hybrid retrieval for RAG agents |

---

## Quick start

```bash
git clone https://github.com/Ghaidaa-Alkhudhair/Anthropic-Agent-Lab.git
cd Anthropic-Agent-Lab

python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate

pip install -r requirements.txt

cp .env.example .env
# Edit .env and set your ANTHROPIC_API_KEY

jupyter notebook
```

---

## Environment variables

| Variable | Required | Used in |
|----------|----------|---------|
| `ANTHROPIC_API_KEY` | Yes | Notebooks 01–06 |
| `VOYAGE_API_KEY` | Notebook 07 only | Hybrid RAG / embeddings |

**Never commit `.env` or real API keys.** See `.gitignore`.

---

## Tech stack

- [Anthropic Claude API](https://docs.anthropic.com/) (Messages API, tools, streaming)
- Python · Jupyter
- [Voyage AI](https://www.voyageai.com/) embeddings (notebook 07)

---


