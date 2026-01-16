# 🧠 memex_ai
### Transform chaotic AI code generation into a predictable, stateful workflow.

`memex_ai` is a lightweight "context-anchoring" system designed for IDE-based AI agents (Cursor, Windsurf, GitHub Copilot, Claude Dev). It transforms chaotic LLM code generation into a predictable, stateful workflow using Scoping, Planning, and Coding definitions.

Most AI development failures occur because agents operate in a **context vacuum**. `memex_ai` solves this by providing a persistent "shared brain" across three simple files. It decouples **Strategy** (Scoping) from **Planning** (Architecting) and **Execution** (Coding).

---

## 📂 The Three-File System

- **`.ai_context.md`**: The Rulebook. Defines the "Bouncer" at the door. It sets universal protocols and role definitions to prevent the AI from reinventing your architecture.
- **`./.ai_context/PROJECT_BRIEF.md`**: The Constitution. The single source of truth for "What" and "Why." It defines the sandbox and the constraints.
- **`./.ai_context/TASKS.yaml`**: The Itinerary. A dynamic, atomic backlog that tracks progress and prevents context-drift during execution.

---

## 🚀 Quick Start

### 1. Initialize the Memex
Copy the base files into your project root:
```bash
mkdir ai_context
touch .ai_context.md ai_context/PROJECT_BRIEF.md ai_context/TASKS.yaml
```

### 2. The Initial Handshake

Open your AI-enabled IDE and use the following prompt to prime the agent:

```
Please inspect .ai_context.md to understand our workflow and project goals. Acknowledge when ready."
```

### 3. Follow the Loop

* Scope: Use a high-level model (Claude 3.5/GPT-4o) to populate the `PROJECT_BRIEF.md`.

* Plan: Ask the agent to act as a Planning Agent to break down the brief into atomic units in TASKS.yaml.

* Execute: Ask the agent to act as a Coding Agent to pick up the next pending task.

## 🛠 Role Definitions

`memex_ai` leverages Role-Specific Protocols to ensure the right "specialist" is on the job:

* Scoping Agent: The "What" and "Why" (scope: `PROJECT_BRIEF.md`)
* Planning Agent: The "How" (High Level)	(scope: `TASKS.yaml`)
* Coding Agent: Tactical Execution	(scope: Working Code)

--- 
LinkedIn Article: ()[http://xxx]

