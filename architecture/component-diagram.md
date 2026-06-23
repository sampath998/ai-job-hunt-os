# Component Diagram

## Overview

The Component Diagram illustrates the internal modules of AI Job Hunt OS and their relationships.

The architecture is designed using modular principles so that new capabilities can be added without modifying existing business logic.

---

```mermaid
flowchart TD

subgraph Career["Career Intelligence"]
CT["Career Twin"]
RA["Resume Agent"]
ATS["ATS Analyzer"]
IA["Interview Agent"]
CR["Company Research"]
CL["Cover Letter Generator"]
end

subgraph Prompt["Prompt Platform"]
PE["Prompt Engine"]
PL["Prompt Library"]
CB["Context Builder"]
MM["Memory Manager"]
WE["Workflow Engine"]
end

subgraph Knowledge["Knowledge Platform"]
KP["Career Profile"]
SK["Skills"]
PJ["Projects"]
ACH["Achievements"]
CERT["Certifications"]
KB["Knowledge Repository"]
end

subgraph AI["AI Provider Layer"]
API["AI Provider Interface"]
Claude["Claude"]
OpenAI["OpenAI"]
Azure["Azure OpenAI"]
Gemini["Gemini"]
Ollama["Ollama"]
end

CT --> PE
RA --> PE
ATS --> PE
IA --> PE
CR --> PE
CL --> PE

PE --> PL
PE --> CB
PE --> MM
PE --> WE

CB --> KB

KB --> KP
KB --> SK
KB --> PJ
KB --> ACH
KB --> CERT

PE --> API

API --> Claude
API --> OpenAI
API --> Azure
API --> Gemini
API --> Ollama
```

---

## Design Principles

- Modular architecture
- Separation of concerns
- AI provider abstraction
- Shared prompt orchestration
- Centralized career knowledge
- Extensible by design

---

## Future Components

The following modules are planned for future releases:

- LinkedIn Optimizer
- Salary Negotiation Agent
- Portfolio Analyzer
- Mock Interview Coach
- Application Tracker
- Career Analytics Dashboard