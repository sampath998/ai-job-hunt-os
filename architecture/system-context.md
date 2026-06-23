# System Context Diagram

## Overview

The System Context Diagram illustrates how AI Job Hunt OS interacts with external users, AI providers, data sources, and output artifacts.

The platform serves as the orchestration layer between career knowledge, AI models, and automation workflows.

---

```mermaid
flowchart LR

User["👤 User"]

AIJob["🤖 AI Job Hunt OS"]

Claude["Claude"]
OpenAI["OpenAI"]
Azure["Azure OpenAI"]
Gemini["Gemini"]

GitHub["GitHub"]
LinkedIn["LinkedIn"]
JobBoards["Job Boards"]

Storage["Local Knowledge Base"]

Output["Resume / ATS / Interview Prep"]

User --> AIJob

AIJob --> Claude
AIJob --> OpenAI
AIJob --> Azure
AIJob --> Gemini

AIJob --> GitHub
AIJob --> LinkedIn
AIJob --> JobBoards

AIJob --> Storage

AIJob --> Output
```