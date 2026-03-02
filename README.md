# AI Operating System · The Foundation for General Intelligence

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Discord](https://img.shields.io/badge/chat-discord-7289da)](https://discord.gg/yourlink)
[![Twitter](https://img.shields.io/twitter/follow/hiTony270461?style=social)](https://x.com/hiTony270461)  

**AI OS is not an operating system, but the idea of one—a new computing paradigm built for intelligence.**

---

## 🌌 Vision

We believe future Artificial General Intelligence (AGI) will not emerge from a single monolithic model, but from **countless composable, evolvable intelligence units (Skills)** working together through a unified “operating system”. AI OS is that system: it manages the lifecycle of Skills, orchestrates their execution, ensures their safety, and lets developers build intelligent applications just like writing ordinary software.

**Core principles of AI OS:**
- **Skills as first-class citizens**: each Skill encapsulates a specific capability (flight search, code writing, mathematical reasoning) exposed via a uniform interface.
- **Declarative orchestration**: describe intent in a DSL, let the OS handle execution.
- **Evolvability**: Skills can learn from mistakes and continuously self‑improve.
- **Open ecosystem**: anyone can create, share, and compose Skills.

---

## 🧱 Layered Architecture

```
┌─────────────────────────────────────────────┐
│            Applications & Agents             │  (direct user interaction)
├─────────────────────────────────────────────┤
│         Orchestration Layer (Skill Flow)     │  (orchestration engine)
├─────────────────────────────────────────────┤
│              Skill Registry                   │  (discovery, versioning, quality)
├─────────────────────────────────────────────┤
│          Skill Execution Environment          │  (MCP servers, sandboxes)
├─────────────────────────────────────────────┤
│                LLM / AI Models                 │  (inference core)
└─────────────────────────────────────────────┘
```

Each layer is open and replaceable, but must adhere to a common specification.

---

## 🚀 Subproject Ecosystem

AI OS is not a single monolithic repository, but a constellation of collaborative open‑source projects. Each project addresses a key challenge:

| Project | Role | Status |
|---------|------|--------|
| [Skill Flow](projects/skill-flow/) | Declarative orchestration engine: turns YAML into Skill call chains | 🔧 In development |
| [Skill Forge](projects/skill-forge/) | Generate Skill configurations from natural language descriptions | ⏳ Planned |
| [Skill Match](projects/skill-match/) | Intelligent matching of user intent to Skills | ⏳ Planned |
| [Skill Adapt](projects/skill-adapt/) | Make Skills learn user preferences and adapt | ⏳ Planned |
| [Skill Memory](projects/skill-memory/) | Stateful Skills that retain context across sessions | ⏳ Planned |
| [Skill Test](projects/skill-test/) | Automated testing and quality assurance for Skills | ⏳ Planned |
| [Skill Hub](projects/skill-hub/) | Skill marketplace: discovery, rating, installation | ⏳ Planned |
| [Skill Learn](projects/skill-learn/) | Self‑evolution of Skills from failures | ⏳ Planned |

Click each project to see detailed roadmap and how to contribute.

---

## 📖 Whitepaper & Specifications

- [Vision Statement](manifesto/vision.md) – The philosophy and goals of AI OS
- [Architecture Design](manifesto/architecture.md) – Detailed layers and interface definitions
- [Skill Model](manifesto/skill-model.md) – Skill metadata, interface specification
- [Workflow DSL Specification](specs/workflow-dsl.md) – YAML syntax reference
- [Overall Roadmap](manifesto/roadmap.md) – 3‑year plan

---

## 🤝 Join Us

AI OS is a community‑driven vision. Whether you're a developer, researcher, or dreamer, you can contribute:

- 💬 [Discord](https://discord.gg/yourlink) – discuss ideas, get help
- 🐛 [Submit an Issue](https://github.com/yourname/ai-os/issues) – report problems or propose new directions
- 🔧 [Contribute Code](community/contributing.md) – join a subproject
- 🌟 Star this repo to spread the word!

---

## 📄 License

MIT © 2025 [Your Name/Organization]
```

### 2. `manifesto/vision.md` – Vision Whitepaper

```markdown
# Vision: The AI Operating System

## Why Do We Need an AI OS?

Today, building AI applications feels like programming in assembly on bare metal. We stitch together disparate APIs, craft prompts, and manually manage state. This approach does not scale, cannot be reused, and certainly cannot support true general intelligence.

AI OS “operationalizes” AI capabilities:

- **Resource Management**: manage Skills, LLM context, token budgets—just as an OS manages CPU and memory.
- **Process Scheduling**: concurrent Skill execution, priorities, preemption.
- **Filesystem**: a unified namespace for Skills, with versions and dependencies.
- **Security & Permissions**: isolation between Skills, data access controls.
- **User/Kernel Mode**: separation of ordinary Skills from system‑level Skills.

## Core Abstraction: Skill

A Skill is the “executable” of AI OS. Each Skill contains:

- **Metadata**: name, description, version, author
- **Interface Definition**: input/output JSON Schema
- **Implementation**: can be a prompt template + MCP tool calls, or native code
- **Dependencies**: other Skills or MCP servers it requires

## Orchestration: Workflow DSL

Developers describe tasks using a declarative DSL (YAML), for example:

```yaml
workflow:
  - skill: flight_search
    params: { from: ${departure}, to: ${destination} }
  - skill: hotel_search
    params: { location: ${flight.destination} }
```

The OS is responsible for translating the DSL into an executable plan, invoking the LLM to fill in details, scheduling MCP tools, handling errors, and returning the result.

## Ecosystem: Skill Marketplace

Anyone can create a Skill and publish it to a Skill Hub. AI OS has built‑in discovery that recommends the most suitable Skills based on user intent. Quality is ensured through community ratings and automated testing.

## Evolution: A Self‑Learning System

Skills can learn from successful and failed cases, automatically optimizing their prompts, parameter extraction rules. The entire OS evolves with usage.

---

## This Is Not Science Fiction; This Is the Roadmap

We are building AI OS one component at a time. Starting with [Skill Flow](projects/skill-flow/), we will progressively realize the other subprojects. Ultimately, AI OS will become the underlying infrastructure for all intelligent applications.

**The future is already here—it's just not evenly distributed.**
```

### 3. `manifesto/roadmap.md` – Overall Roadmap

```markdown
# AI OS Roadmap (2025–2027)

## Phase 0: Foundation (2025 Q2–Q3)
- [x] Establish vision and architecture
- [ ] **Skill Flow v0.1**: core orchestration engine MVP (linear execution, variable passing)
- [ ] **Skill metadata spec v1**: define Skill schema
- [ ] Build community

## Phase 1: Core Ecosystem (2025 Q4 – 2026 Q2)
- [ ] **Skill Flow v1.0**: support conditions, loops, error handling
- [ ] **Skill Forge**: generate Skill prototypes from natural language
- [ ] **Skill Match**: vector‑search‑based Skill recommendation
- [ ] **Skill Test**: automated testing framework
- [ ] **Skill Hub**: simple marketplace (GitHub‑based)

## Phase 2: Intelligence Enhancement (2026 Q3 – 2027 Q1)
- [ ] **Skill Memory**: stateful Skills
- [ ] **Skill Adapt**: personalization and adaptation
- [ ] **Skill Learn**: self‑optimization from feedback
- [ ] **Distributed execution**: cross‑machine scheduling
- [ ] **Secure sandbox**: isolated Skill execution

## Phase 3: Operationalization (2027+)
- [ ] **System Skills**: managing memory, files, processes
- [ ] **Multimodal Skills**: image, audio, video
- [ ] **Autonomous Agents**: long‑running agents automatically generated by the OS
- [ ] **Decentralized Skill network**: P2P Skill discovery and invocation

---

We welcome contributions of any kind—code, documentation, ideas. Specific milestones for each phase are detailed in the respective subproject `ROADMAP.md` files.
```

### 4. `projects/skill-flow/README.md` – Example Subproject

```markdown
# Skill Flow · Declarative Orchestration Engine

[![GitHub](https://img.shields.io/badge/repo-skill--flow-blue)](https://github.com/yourname/skill-flow)
[![Docs](https://img.shields.io/badge/docs-in--progress-yellow)](https://github.com/yourname/skill-flow/wiki)

**Core Mission**: As the orchestration layer of AI OS, translate declarative DSL into Skill call chains.

## Features
- Parse YAML workflow definitions
- Variable substitution and expression evaluation
- Integration with MCP servers
- Support for sequential, conditional, and loop execution (in progress)
- Pluggable LLM backends (LangChain compatible)

## Current Status
🔧 In development (Phase 0) – v0.1 expected Q3 2025

## How to Contribute
Please refer to the [skill-flow repository](https://github.com/yourname/skill-flow) for detailed contribution guidelines.

## Leads
- @seki2020 (architecture)
- Join us!
