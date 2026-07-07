# Diagrams

GitHub renders these Mermaid diagrams automatically in Markdown.

## Software Platform Evolution

```mermaid
timeline
    title Software Platform Shifts
    1990 : Desktop apps
    2005 : Web apps
    2010 : Mobile apps
    2015 : Cloud native
    2020 : Data and ML products
    2022 : LLM applications
    2023 : Copilots
    2024 : AI agents
    2025 : Autonomous software systems
```

## Concept Hierarchy

```mermaid
flowchart TD
    AI["Artificial Intelligence"]
    ML["Machine Learning"]
    DL["Deep Learning"]
    LLM["Large Language Models"]
    APP["LLM Applications"]
    COP["Copilots"]
    AGENT["AI Agents"]

    AI --> ML
    ML --> DL
    DL --> LLM
    LLM --> APP
    APP --> COP
    APP --> AGENT
```

## Modern AI Application Stack

```mermaid
flowchart TD
    User["User"]
    UI["Frontend or Chat UI"]
    App["AI Application Service"]
    Controller["Agent or Workflow Controller"]
    Planner["Planner"]
    Memory["Memory"]
    Tools["Tool Calling"]
    RAG["Retrieval / RAG"]
    Eval["Evaluation Harness"]
    Trace["Observability and Tracing"]
    MCP["MCP Servers"]
    DB["SQL / Object Storage"]
    Vector["Vector Database"]
    Model["LLM / Embedding / Reranker"]
    Infra["Hosted Inference / GPU Infrastructure"]

    User --> UI --> App --> Controller
    Controller --> Planner
    Controller --> Memory
    Controller --> Tools
    Controller --> RAG
    Controller --> Eval
    Controller --> Trace
    Tools --> MCP
    Memory --> DB
    RAG --> Vector
    Controller --> Model
    Model --> Infra
```

## Agent Loop

```mermaid
flowchart LR
    Goal["User Goal"]
    Observe["Observe Context"]
    Reason["Reason"]
    Plan["Plan Next Step"]
    Tool["Select Tool"]
    Act["Call Tool"]
    Result["Observe Result"]
    Reflect["Reflect"]
    Stop{"Done?"}
    Answer["Return Answer or Artifact"]

    Goal --> Observe --> Reason --> Plan --> Tool --> Act --> Result --> Reflect --> Stop
    Stop -- "No" --> Observe
    Stop -- "Yes" --> Answer
```

## Ecosystem Map

```mermaid
flowchart TB
    subgraph Models["Model Providers"]
        OpenAI["OpenAI"]
        Anthropic["Anthropic"]
        Gemini["Google Gemini"]
        Groq["Groq"]
        Ollama["Ollama"]
    end

    subgraph Apps["Developer and User Apps"]
        Cursor["Cursor"]
        ClaudeCode["Claude Code"]
        Codex["Codex"]
        Copilot["GitHub Copilot"]
    end

    subgraph Frameworks["Agent Frameworks"]
        OAI["OpenAI Agents SDK"]
        LangGraph["LangGraph"]
        CrewAI["CrewAI"]
        SK["Semantic Kernel"]
        AutoGen["AutoGen"]
        ADK["Google ADK"]
        PAI["PydanticAI"]
        Agno["Agno"]
        Mastra["Mastra"]
    end

    subgraph Protocols["Protocols and Tool Access"]
        MCP["MCP"]
        A2A["A2A"]
        Playwright["Playwright"]
        BrowserUse["Browser Use"]
        N8N["n8n"]
    end

    Apps --> Models
    Frameworks --> Models
    Frameworks --> Protocols
    Protocols --> Models
```

## Cursor-Style Coding Assistant Flow

```mermaid
sequenceDiagram
    participant User
    participant Editor
    participant Context as Context Builder
    participant Agent as Coding Agent
    participant Tools
    participant Model as LLM

    User->>Editor: Ask coding question
    Editor->>Context: Provide open files, diagnostics, selection
    Context->>Agent: Build task context
    Agent->>Model: Ask for next step
    Model-->>Agent: Reasoned action
    Agent->>Tools: Search files / run tests / inspect code
    Tools-->>Agent: Results
    Agent->>Model: Add observations
    Model-->>Agent: Proposed fix and explanation
    Agent-->>Editor: Apply or suggest changes
    Editor-->>User: Show response
```

