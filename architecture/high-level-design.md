# High-Level Architecture

## Overview

AI Job Hunt OS follows a layered architecture to ensure modularity, maintainability, scalability, and AI provider independence.

The system separates business logic from prompt orchestration, AI providers, and persistent knowledge, allowing each layer to evolve independently.

---

## Architectural Principles

- Separation of Concerns
- Modular Design
- AI Provider Independence
- Documentation First
- Knowledge-Centric Architecture
- Extensible by Design

---

## High-Level Architecture

```mermaid
flowchart TD

User["👤 User"]

Presentation["Presentation Layer
CLI • Web UI • Dashboard"]

Application["Application Layer
Career Twin
Resume Agent
ATS Analyzer
Interview Prep
Company Research"]

Prompt["Prompt Orchestration Layer
Templates
Agents
Chains
Memory"]

AI["AI Provider Layer
Claude
OpenAI
Azure OpenAI
Gemini
Local LLM"]

Knowledge["Knowledge Layer
Career Data
Templates
Examples
Projects
Skills"]

Infrastructure["Infrastructure Layer
Markdown
JSON
SQLite
Vector DB
Configuration"]

User --> Presentation

Presentation --> Application

Application --> Prompt

Prompt --> AI

Application --> Knowledge

Knowledge --> Infrastructure
```

---

## Layer Responsibilities

| Layer | Responsibility |
|---------|----------------|
| Presentation | User interaction |
| Application | Business capabilities |
| Prompt Orchestration | Prompt engineering |
| AI Provider | LLM abstraction |
| Knowledge | Persistent career intelligence |
| Infrastructure | Storage and configuration |

---

## Benefits

- Vendor independent
- Modular
- Easily testable
- Future-proof
- Open-source friendly
- Easy onboarding