# 🚀 PreAgent

**Spec-first AI development methodology. No vibe coding.**

PreAgent replaces vague prompts with structured context. Instead of telling an AI "build me an app," you define **Product Requirements → Technical Architecture → UI Specifications → Tasks Plan** in JSON format. AI agents execute one task group at a time, guided by specs, not guesses.

---

## 🔥 The Problem

Most AI-assisted development follows a broken loop:

```
Vague prompt → AI guesses → Wrong output → Tweak prompt → Still wrong → Abandon
```

This works for prototypes. It fails for real products.

## ✅ The PreAgent Solution

```
Structured specs (.json) → Task groups → AI executes one group at a time → Test → Commit → Next group
```

Four documents, one methodology, zero guesswork:

| # | Phase | Output | Purpose |
|---|---|---|---|
| 1 | **📊 Product Requirements** | `product-requirements.json` | Who is this for? What problem? What's in/out of scope? |
| 2 | **🏗️ Technical Architecture** | `technical-architecture.json` | Stack, DB schema, API structure, file organization |
| 3 | **🎨 UI Specifications** | `ui-specifications.json` | Design system, components, screens, states *(optional)* |
| 4 | **📋 Tasks Plan** | `tasks.md` | Phased task groups with acceptance criteria |

---

## 📦 What's in this repo

```
PreAgent/
├── README.md                     ← You are here
├── LICENSE                       ← MIT
└── template/                     ← Full methodology template
    ├── AGENTS.md                 ← Protocol for autonomous AI agents
    ├── Quick Start Guide.md      ← From zero to shipping in 4 steps
    ├── Accountability Rules.md   ← 4 rules to prevent architecture drift
    ├── Dev Checklist.md          ← Prompt quality standards
    ├── 📊 Product Requirements.md
    ├── 📊 Product Requirements Template.md
    ├── 🏗️ Technical Architecture.md
    ├── 🏗️ Technical Architecture Template.md
    ├── 🎨 UI Specifications.md
    ├── 🎨 UI Specifications Template.md
    ├── 📋 Tasks Template.md
    ├── 📋 Project Template.md
    ├── product-requirements.schema.json
    ├── technical-architecture.schema.json
    └── ui-specifications.schema.json
```

---

## 🚀 Quick start (5 minutes)

```bash
# 1. Copy the template into your project
cp -r template/* /path/to/your/project/

# 2. Fill out Product Requirements
#    Read 📊 Product Requirements.md → Answer questions → Ask AI to fill the JSON

# 3. Fill out Technical Architecture
#    Read 🏗️ Technical Architecture.md → Define stack → Ask AI to fill the JSON

# 4. Generate Tasks Plan
#    Read 📋 Tasks Template.md → Ask AI to generate tasks.md from your architecture

# 5. Execute
#    Pick the first task group → "AI, execute Group 1.1" → Test → Commit → Next
```

---

## 🧠 How it works with AI agents

### With autonomous agents (Codex CLI, Claude Code, etc.)

Copy `AGENTS.md` to your project root. It contains:
- **PROJECT CONTEXT** — fillable YAML block (project name, stack, current phase)
- **EXECUTION PROTOCOL** — fixed rules the agent follows every session
- **SCOPE CONTROL** — stay in your task group, no scope creep

### With Cursor, Copilot, or chat interfaces

Use the structured `.json` files as reference documents. Each `📊 Product Requirements.md` file includes prompt templates for your AI tool.

---

## 🎯 Who is PreAgent for?

| Role | How they use it |
|---|---|
| **Solo devs** | Replace "vibe coding" with structured execution. Ship faster, rework less. |
| **Founders building MVP** | Define what matters, skip what doesn't. One task group at a time. |
| **Teams with AI agents** | Give every agent the same spec. Consistent architecture, consistent code. |
| **Agency/consultancy** | Onboard AI agents to client projects in minutes, not days. |

---

## 📐 The 4 Systems (optional ecosystem)

PreAgent is part of a larger knowledge management ecosystem. The companion methodology — **The 4 Systems** — covers:

| System | Question |
|---|---|
| **S1 — Navigation** | What exists? Where do I work? |
| **S2 — Second Brain** | Where does knowledge live? |
| **S3 — Governance** | Where should each thing go? |
| **S4 — Digestion** | How do we turn activity into knowledge? |

*(Coming soon to this repo)*

---

## 📄 License

MIT — use it, fork it, ship it. Attribution appreciated but not required.

---

Built for developers who want AI to execute, not improvise.
