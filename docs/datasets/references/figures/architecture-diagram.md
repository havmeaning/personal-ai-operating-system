# PAIOS Reference Architecture

**Personal AI Operating System — Conceptual Architecture Diagram**

---

## Overview

The diagram below illustrates the layered architecture of a Personal AI Operating System (PAIOS), showing how the user interface, agent orchestration layer, memory systems, and tool integrations relate to each other.

---

## Architecture Layers

```
┌─────────────────────────────────────────────────────────┐
│                     USER INTERFACE                      │
│          (Chat, Dashboard, Workflow Builder)             │
└─────────────────────┬───────────────────────────────────┘
                      │
┌─────────────────────▼───────────────────────────────────┐
│              ORCHESTRATION LAYER (AgentOS)               │
│                                                         │
│   ┌─────────────┐  ┌─────────────┐  ┌───────────────┐  │
│   │  Planner    │  │  Executor   │  │  Coordinator  │  │
│   │  Agent      │◄─►  Agents     │◄─►  (Router)     │  │
│   └─────────────┘  └─────────────┘  └───────────────┘  │
│                                                         │
└──────────────┬──────────────────────────────────────────┘
               │
┌──────────────▼──────────────────────────────────────────┐
│                    MEMORY SYSTEM                        │
│                                                         │
│   ┌──────────────┐  ┌────────────┐  ┌───────────────┐  │
│   │ Short-Term   │  │  Episodic  │  │   Semantic    │  │
│   │ (Context     │  │  (Session  │  │  (Knowledge   │  │
│   │  Window)     │  │   History) │  │   Base / RAG) │  │
│   └──────────────┘  └────────────┘  └───────────────┘  │
│                                                         │
│   ┌──────────────────────────────────────────────────┐  │
│   │       Vector Store (Embeddings Index)            │  │
│   └──────────────────────────────────────────────────┘  │
│                                                         │
└──────────────┬──────────────────────────────────────────┘
               │
┌──────────────▼──────────────────────────────────────────┐
│                    TOOL LAYER                           │
│                                                         │
│  Web Search  │  Code Exec  │  Calendar  │  File System  │
│  Email       │  Notes      │  APIs      │  Databases    │
│                                                         │
└─────────────────────────────────────────────────────────┘
               │
┌──────────────▼──────────────────────────────────────────┐
│              PERSONAL DATA LAYER                        │
│        (User-owned, privacy-preserving)                 │
│                                                         │
│   Documents  │  Notes  │  Email  │  Calendar  │  Code   │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## Data Flow

1. **User** issues a request via the interface (chat, workflow trigger, scheduled task).
2. **Orchestration Layer** receives the request; the **Planner Agent** decomposes it into sub-tasks.
3. Sub-tasks are routed to specialised **Executor Agents** (research, writing, scheduling, etc.).
4. Agents query the **Memory System** for relevant context (past sessions, knowledge base documents).
5. Agents call **Tools** as needed (search, code execution, calendar, file access).
6. Results are aggregated by the **Coordinator** and returned to the user.
7. The interaction is stored in **Episodic Memory** for future retrieval.

---

## Framework Mapping

| Architecture Component | LangGraph | AutoGen | CrewAI | Haystack |
|------------------------|-----------|---------|--------|---------|
| Planner Agent          | Graph node | AssistantAgent | Task planner | Pipeline node |
| Executor Agents        | Graph nodes | UserProxy + tools | Crew members | Component |
| Coordinator/Router     | Conditional edges | GroupChat | Crew manager | Router |
| Short-Term Memory      | State dict | Conversation context | Task context | Pipeline state |
| Episodic Memory        | Checkpointer | External | External | Document store |
| Semantic Memory        | VectorStore integration | VectorStore | VectorStore | Built-in |
| Tool Use               | Tool nodes | FunctionCall | Tool decorator | Tool component |

---

*See the [white paper](../../white-paper/agentos-frameworks-2026.md) for full architectural analysis.*
