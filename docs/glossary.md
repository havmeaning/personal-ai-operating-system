# PAIOS Glossary

Key terms and definitions used in the Personal AI Operating System research programme.

---

## A

**AgentOS**  
An AI-native operating system in which a large language model (LLM) functions as the core kernel, managing tasks, data, and application interactions through natural language. The term encompasses both academic proposals (e.g., arXiv:2603.08938) and production frameworks.

**Agentic AI**  
AI systems that autonomously plan, execute multi-step tasks, call tools, and adapt behaviour based on feedback—beyond single-turn question answering.

**AIOS (Rutgers)**  
An LLM-based operating system framework from Rutgers University that implements kernel-level LLM scheduling, demonstrating 2.1× throughput improvement in published benchmarks.

---

## C

**Cognitive Audit**  
A structured weekly review process in which a knowledge worker evaluates AI-generated decisions and outputs, exercising veto rights and updating system rules. Part of the PAIOS four-layer governance model.

---

## E

**EU AI Act**  
Regulation (EU) 2024/1689—the European Union's comprehensive AI regulatory framework. Annex III high-risk obligations become enforceable on 2 August 2026.

---

## I

**Intent Alignment Paradox**  
The observation that as AI systems become more capable of inferring user intent, they may take actions that technically fulfil stated objectives while diverging from underlying values—identified as a key systemic risk in PAIOS deployments.

---

## J

**J-Curve of Agentic Adoption**  
The productivity pattern observed in agentic AI deployments: an initial dip caused by setup overhead and cognitive adjustment, followed by a steeper recovery as automation benefits compound.

---

## L

**LangGraph**  
A production-grade stateful workflow runtime built on the LangChain ecosystem, providing persistent checkpoints, conditional branching, and human-in-the-loop controls for agentic applications.

---

## M

**MemOS**  
A hierarchical memory management system for LLMs, providing short-term, medium-term, and long-term memory coherence. Demonstrates leading performance on LongMemEval benchmark subtasks.

---

## P

**PAIOS (Personal AI Operating System)**  
A six-layer modular architecture for deploying sovereign, privacy-preserving AI operating environments at personal scale. Layers: Capture → Orchestration → Storage → Memory → Reasoning → Governance.

**Personal Knowledge Graph (PKG)**  
A structured, machine-readable graph of an individual's knowledge, relationships, and context—used as a persistent long-term memory substrate in PAIOS deployments.

---

## S

**SOUL (Simple Open Universal Layer)**  
A proposed portable knowledge interchange format for PKG data: Markdown + YAML + JSON-LD + vector hashes + manifest. Designed to enable zero-friction data portability across AgentOS frameworks.

---

## T

**Tri-Agent Kernel**  
An architectural pattern proposed in arXiv:2603.08938 using three cooperating agents (planner, executor, memory manager) as the core operating kernel of an AgentOS.
