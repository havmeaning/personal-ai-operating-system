# Security Threat Model

**Personal AI Operating System (PAIOS) — Security Documentation**

---

## Overview

Personal AI Operating Systems introduce novel attack surfaces that differ from traditional software security. This document catalogues the primary threat categories identified during the PAIOS research programme and maps them to mitigations within the six-layer stack.

---

## Threat Categories

### 1. Prompt Injection

**Description:** Malicious content embedded in external inputs (documents, emails, web pages) hijacks the AI's instruction context, causing it to execute attacker-controlled actions.

**Affected layers:** Orchestration (n8n/LangGraph), Reasoning (Claude API)

**Mitigations:**
- Sanitise all external content before insertion into prompt context
- Use structured tool-call interfaces rather than free-form prompt concatenation
- Apply input validation at orchestration layer boundaries

---

### 2. Memory Poisoning

**Description:** Adversarial data is injected into the PKG or vector store, corrupting long-term memory and causing persistently incorrect AI behaviour.

**Affected layers:** Storage (Obsidian), Memory (MemOS-style)

**Mitigations:**
- Cryptographic hashing of PKG entries (SOUL format vector hashes)
- Immutable append-only audit log for all memory writes
- Periodic cognitive audit review of memory contents

---

### 3. Data Exfiltration

**Description:** AI tools or orchestration workflows are manipulated to transmit sensitive personal data to external endpoints.

**Affected layers:** Orchestration, Capture (Read AI)

**Mitigations:**
- Local-first storage with selective cloud reasoning (no raw data transmission)
- Network egress monitoring for orchestration workflows
- Principle of least privilege for all tool integrations

---

### 4. Shadow Decisions

**Description:** AI agents make consequential decisions (sending messages, scheduling meetings, modifying files) without surfacing them for human review.

**Affected layers:** Orchestration, Governance (cognitive-audit loop)

**Mitigations:**
- All write-actions require explicit human-in-the-loop confirmation
- Decision log with reversibility for all agentic actions
- Weekly cognitive audit with veto rights

---

## EU AI Act Compliance Notes

Under Annex III (effective 2 August 2026), personal AI systems used in high-risk contexts must implement:

- Risk assessment documentation
- Human oversight mechanisms
- Transparency and logging obligations
- Data governance and minimisation practices

The PAIOS governance layer (Layer 6) is designed to satisfy these requirements through the four-mechanism cognitive-audit model: detection, evaluation, veto, and adaptation.

---

## Responsible Disclosure

Security issues in this research repository or associated PAIOS tooling should be reported privately before public disclosure. Please open a GitHub Security Advisory or contact the maintainer directly.
