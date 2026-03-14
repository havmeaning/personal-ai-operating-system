# Personal AI Operating System (PAIOS)

> A research repository exploring the architecture, evaluation, and governance of Personal AI Operating Systems and AgentOS frameworks.

**Author:** Sheldon Howard  
**Date:** March 2026  
**License:** MIT

---

## Project Description

The Personal AI Operating System (PAIOS) project develops a blueprint for individuals to deploy sovereign, privacy-preserving AI operating environments. Rather than relying on monolithic cloud platforms, PAIOS proposes a modular six-layer stack that integrates capture, orchestration, storage, memory, reasoning, and governance into a coherent personal-scale system.

This repository contains the primary research paper, comparison datasets, architecture diagrams, and governance documentation produced as part of the PAIOS research programme.

---

## Research Objective

To identify the most effective AgentOS architecture for high-performance individual knowledge workers operating in regulated European environments—prioritising privacy, EU AI Act compliance, modularity, and immediate deployability over academic novelty or enterprise scale.

---

## Architecture Overview

The PAIOS six-layer stack:

| Layer | Component | Role |
|-------|-----------|------|
| 1. Capture | Read AI | Meeting intelligence and cross-channel indexing |
| 2. Orchestration | n8n / LangGraph | Stateful workflow automation with human-in-the-loop |
| 3. Storage | Obsidian (local-first) | Persistent knowledge vault with vector search |
| 4. Memory | MemOS-style hierarchy | Short, medium, and long-term memory coherence |
| 5. Reasoning | Claude (API) | Advanced language model for synthesis and analysis |
| 6. Governance | Cognitive-audit loop | Weekly audit, veto, and adaptation mechanisms |

---

## White Paper

**AgentOS Frameworks in 2026: A Comparative Evaluation for Personal-Scale Knowledge Work**

A structured comparison of seven AgentOS frameworks across maturity, orchestration, privacy, and EU AI Act readiness—identifying the PAIOS modular hybrid as the sole immediately deployable solution.

[Read the White Paper](docs/white-paper/agentos-frameworks-2026.md)

---

## Repository Structure

```
personal-ai-operating-system/
│
├── README.md                        # This file
├── CITATION.cff                     # Citation metadata
├── LICENSE                          # MIT License
│
├── docs/
│   ├── white-paper/
│   │   └── agentos-frameworks-2026.md   # Primary research paper
│   ├── architecture/                # Architecture documentation
│   ├── governance/                  # Governance model documentation
│   ├── roadmap.md                   # Research roadmap
│   ├── glossary.md                  # Key terms and definitions
│   └── security.md                  # Security threat model
│
├── diagrams/
│   ├── paios-architecture.png       # Six-layer PAIOS stack diagram
│   └── system-stack.png             # System component diagram
│
├── research-notes/
│   ├── experiments/                 # Experiment logs and results
│   └── literature-review/           # Literature survey notes
│
├── datasets/
│   ├── raw/                         # Raw comparison data
│   └── processed/                   # Processed datasets
│
└── .github/
    ├── ISSUE_TEMPLATE/              # Issue templates
    └── PULL_REQUEST_TEMPLATE.md     # PR template
```

---

## PAIOS Research Program

The PAIOS Research Program is a structured multi-phase initiative addressing the full lifecycle of personal AI operating environments:

### Architecture Development
Design and validation of the six-layer PAIOS stack—evaluating component interoperability, failure modes, and performance at personal scale.

### Governance Models
Formal specification of the four-layer cognitive-audit governance model: detection, evaluation, veto, and adaptation mechanisms for AI decision oversight.

### Interoperability Standard (SOUL)
Development of the **Simple Open Universal Layer (SOUL)** format—a portable knowledge interchange standard using Markdown + YAML + JSON-LD + vector hashes + manifest to enable cross-framework PKG portability.

### Evaluation Benchmarks
Construction of reproducible benchmarks for evaluating AgentOS frameworks on knowledge-work productivity, privacy preservation, regulatory compliance, and cognitive load.

---

## Citation

To cite this research, please use the following format or see [`CITATION.cff`](CITATION.cff):

```
Howard, S. (2026). AgentOS Frameworks in 2026: A Comparative Evaluation for
Personal-Scale Knowledge Work. Personal AI Operating System Research Repository.
https://github.com/havmeaning/personal-ai-operating-system
```

---

## License

This project is licensed under the [MIT License](LICENSE).

© 2026 Sheldon Howard / havmeaning
