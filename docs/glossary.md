# Glossary

**Personal AI Operating System (PAIOS) Research — Key Terms**

This glossary defines terms used in the white paper and throughout this repository.

---

## A

**Agent**  
An autonomous software entity that perceives its environment, reasons about goals, and takes actions to accomplish tasks. In the context of PAIOS, agents are AI-powered units that handle specific cognitive functions such as search, summarisation, or scheduling.

**Agent Loop**  
The core execution cycle of an AI agent: *Observe → Think → Act → Reflect*. The loop runs continuously until a goal is achieved or a stopping condition is met.

**AgentOS (Agent Operating System)**  
A framework or runtime environment that manages the lifecycle of AI agents — including their memory, tool access, task scheduling, and inter-agent communication. Analogous to an operating system for autonomous AI processes.

**Agentic AI**  
AI systems designed to act autonomously over extended tasks with minimal per-step human supervision. Distinguished from conversational AI, which requires a human prompt for every response.

**Architecture (Cognitive)**  
The structural design of a system that models how information is perceived, stored, reasoned about, and acted upon. In PAIOS, cognitive architecture refers to how memory, planning, and execution modules are organised.

---

## C

**Context Window**  
The maximum amount of text (measured in tokens) that a language model can process in a single inference call. A key constraint when designing long-running agents.

**Cognitive Load**  
The mental effort required by a human user to manage and interact with an AI system. A primary usability metric for personal-scale AI systems.

---

## E

**Embedding**  
A numerical vector representation of text, used to capture semantic meaning. Embeddings power similarity search in memory systems (e.g., retrieving relevant past notes or documents).

**Episodic Memory**  
Memory of specific past events or interactions. In PAIOS, episodic memory enables agents to recall what the user asked yesterday, last week, or in a prior session.

---

## F

**Framework (AgentOS)**  
A software toolkit or platform providing abstractions for building, running, and connecting AI agents. Examples include LangGraph, CrewAI, AutoGen, and OpenAI Swarm.

---

## G

**Goal Decomposition**  
The process of breaking a high-level goal into a sequence of smaller, actionable sub-tasks. A core capability of planning agents.

---

## H

**Human-in-the-Loop (HITL)**  
A design pattern where a human provides oversight, correction, or approval at key decision points in an agent workflow. Essential for trust and safety in personal AI systems.

---

## K

**Knowledge Graph**  
A structured representation of entities and their relationships, used as a long-term semantic memory store. Enables agents to reason over connected information rather than flat text.

**Knowledge Work**  
Cognitive labour focused on creating, processing, and applying information — including research, writing, planning, analysis, and communication. The primary use-case domain for PAIOS.

---

## L

**LLM (Large Language Model)**  
A neural network trained on large corpora of text, capable of generating, summarising, and reasoning about language. The reasoning engine powering most modern AI agents.

**Long-Term Memory (LTM)**  
Persistent storage of information that survives across sessions. In PAIOS, LTM allows agents to maintain continuity of knowledge over days, weeks, and months.

---

## M

**Memory System**  
The component of an agent architecture responsible for storing and retrieving information. Typically combines short-term (in-context), episodic, semantic, and procedural memory layers.

**Multi-Agent System**  
An architecture in which multiple specialised agents collaborate, each handling a distinct sub-task and communicating results to a coordinating agent.

---

## O

**Orchestration**  
The coordination of multiple agents, tools, and memory systems to execute a complex workflow. The orchestrator manages task routing, sequencing, and error handling.

---

## P

**PAIOS (Personal AI Operating System)**  
A unified, user-owned AI infrastructure designed for individual knowledge work. PAIOS integrates agent orchestration, persistent memory, personal data access, and user-defined workflows into a coherent personal computing layer.

**Persona**  
A defined role or identity assigned to an agent that shapes its tone, focus, and reasoning style (e.g., "research assistant", "writing editor", "project planner").

**Planning Agent**  
An agent specialised in decomposing goals into structured plans and delegating sub-tasks to executor agents.

**Procedural Memory**  
Memory of *how to do things* — learned routines and workflows that an agent can apply repeatedly. Equivalent to skill or habit memory in cognitive science.

---

## R

**RAG (Retrieval-Augmented Generation)**  
A technique combining a language model with a retrieval system (e.g., vector database) so that the model can ground its responses in relevant retrieved documents. Widely used in personal knowledge management agents.

**Reasoning**  
The process by which an agent evaluates options, infers conclusions, and selects actions. May involve chain-of-thought, tree-of-thought, or tool-assisted reasoning approaches.

**ReAct (Reason + Act)**  
An agent prompting strategy that interleaves reasoning steps with action calls, enabling the model to iteratively refine its approach based on tool outputs.

---

## S

**Semantic Memory**  
Memory of facts and concepts, independent of specific episodes. In PAIOS, semantic memory stores the user's accumulated knowledge base — notes, documents, and reference materials.

**Short-Term Memory (STM)**  
The information available to an agent within its active context window during a single session or task execution.

**Swarm**  
A multi-agent pattern in which many lightweight agents collaborate on a task with minimal central coordination, relying on emergent behaviour from simple local rules.

---

## T

**Task Queue**  
A managed list of pending agent tasks, enabling asynchronous and parallel execution of workflows.

**Token**  
The basic unit of text processed by a language model (roughly ¾ of a word on average). Token count determines inference cost and context window utilisation.

**Tool Use**  
The ability of an agent to invoke external functions or APIs (e.g., web search, code execution, calendar access) to extend its capabilities beyond pure language generation.

---

## V

**Vector Database**  
A database optimised for storing and querying embedding vectors, used as the backing store for semantic and episodic memory in agent systems. Examples: Chroma, Weaviate, Pinecone, Qdrant.

---

## W

**Workflow**  
A defined sequence of agent steps and tool calls that accomplishes a repeatable task. In PAIOS, workflows are the reusable "programs" that agents execute on behalf of the user.

---

*See the [white paper](white-paper/agentos-frameworks-2026.md) for in-depth discussion of these concepts.*
