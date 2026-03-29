# AgentForge

> An open-source AI Agent development and orchestration platform.  
> Build, connect, and deploy intelligent agents — visually.

[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white)](https://react.dev/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.110+-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)](https://python.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-4169E1?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## What is AgentForge?

AgentForge is a full-stack platform for creating, orchestrating, and deploying AI agents. Instead of writing boilerplate agent code from scratch, users design agent workflows visually — connecting LLM nodes, tools, knowledge bases, and decision logic through a drag-and-drop canvas.

**Key capabilities:**

- **Agent Builder** — Create custom AI agents with configurable prompts, tools, and memory
- **RAG Engine** — Upload documents to build knowledge bases with vector search and reranking
- **Visual Workflow Editor** — Drag-and-drop canvas to design multi-step agent pipelines
- **Multi-Agent Orchestration** — Define agent teams with roles, communication patterns, and shared context
- **MCP Integration** — Connect external tools and services via the Model Context Protocol
- **Production Dashboard** — Monitor token usage, latency, costs, and error rates in real-time

---

## Architecture

```
┌─────────────────────────────────────────────────────┐
│                    Frontend                         │
│         React 18 · TypeScript · Tailwind CSS        │
│         React Flow · Zustand · TanStack Query       │
├─────────────────────────────────────────────────────┤
│                   API Gateway                       │
│              FastAPI · WebSocket · SSE              │
├──────────┬──────────┬──────────┬────────────────────┤
│  Agent   │   RAG    │ Workflow │   Multi-Agent      │
│  Engine  │  Engine  │ Engine   │   Orchestrator     │
│          │          │          │                    │
│ LangChain│ pgvector │  State   │   LangGraph        │
│ Tool Call│ Embedding│  Machine │   Event-driven     │
│ Memory   │ Rerank   │  DAG     │   Message Bus      │
├──────────┴──────────┴──────────┴────────────────────┤
│                  Data Layer                         │
│        PostgreSQL · Redis · Vector Store            │
├─────────────────────────────────────────────────────┤
│                Infrastructure                       │
│     Docker Compose · CI/CD · Prometheus · Grafana   │
└─────────────────────────────────────────────────────┘
```

---

## Roadmap

| Phase | Focus | Status |
|-------|-------|--------|
| **1 — Foundation** | Full-stack skeleton, auth, project CRUD, API design | 🔄 In Progress |
| **2 — Agent Core** | Single agent engine, tool calling, conversation, memory | ⬜ Planned |
| **3 — RAG Engine** | Document processing, vector search, retrieval pipeline | ⬜ Planned |
| **4 — Visual Builder** | Drag-and-drop workflow editor, node system, execution | ⬜ Planned |
| **5 — Multi-Agent** | Agent teams, role assignment, message passing, coordination | ⬜ Planned |
| **6 — Production** | Monitoring dashboard, logging, CI/CD, cost tracking | ⬜ Planned |
| **7 — MCP & Ecosystem** | MCP protocol support, plugin marketplace, security audit | ⬜ Planned |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18, TypeScript, Tailwind CSS, React Flow, Zustand |
| Backend | FastAPI, Python 3.12, SQLAlchemy, Pydantic |
| AI/Agent | LangChain, LangGraph, OpenAI / DeepSeek API |
| Database | PostgreSQL 16, pgvector, Redis |
| Infra | Docker Compose, GitHub Actions, Prometheus, Grafana |

---

## Getting Started

> ⚠️ AgentForge is in early development. Phase 1 is currently in progress.

### Prerequisites

- Docker & Docker Compose
- Node.js 20+
- Python 3.12+

### Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/agentforge.git
cd agentforge

# Start all services
docker compose up -d

# Frontend (development)
cd frontend && npm install && npm run dev

# Backend (development)
cd backend && pip install -r requirements.txt && uvicorn app.main:app --reload
```

---

## Project Structure

```
agentforge/
├── frontend/                # React + TypeScript + Tailwind
│   ├── src/
│   │   ├── components/      # Shared UI components
│   │   ├── features/        # Feature modules (agents, workflows, rag...)
│   │   ├── hooks/           # Custom React hooks
│   │   ├── stores/          # Zustand state stores
│   │   └── lib/             # Utilities and API client
│   └── ...
├── backend/                 # FastAPI + Python
│   ├── app/
│   │   ├── api/             # Route handlers
│   │   ├── core/            # Config, security, dependencies
│   │   ├── models/          # SQLAlchemy models
│   │   ├── schemas/         # Pydantic schemas
│   │   ├── services/        # Business logic
│   │   └── agent/           # Agent engine core
│   └── ...
├── docker-compose.yml       # Development environment
├── .github/workflows/       # CI/CD pipelines
└── docs/                    # Documentation
```

---

## Contributing

AgentForge is a personal portfolio project currently in active development. Contributions, feedback, and discussions are welcome — feel free to open an issue.

---

## License

[MIT](LICENSE)

---

<p align="center">
  Built by <a href="https://junshuolu.com">Junshuo Lu</a> · 2026
</p>
