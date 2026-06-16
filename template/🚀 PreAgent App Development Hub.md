# 🚀 PreAgent App Development Hub

*Structured docs + task groups. Zero vibe coding.*

---

## 📖 Overview

**PreAgent** replaces vague prompts with structured context. Three core docs define your app; `tasks.md` executes it in phases; `AGENTS.md` tells the autonomous agent how to work.

### Workflow

```
📄 .md (questionnaire)  →  🤖 AI fills  →  📋 .schema.json  →  💾 .json in your project
```

Each document has:
- A **`.md`** with instructions, examples, and the JSON schema reference
- A **`.schema.json`** template — ready for the AI to fill with your project
- The final **`.json`** lives in your project root

---

## 📋 System Documents

### 🔸 Core Phases

| # | Phase | Questionnaire | Schema JSON |
|---|---|---|---|
| **1** | **📊 Product Requirements** | `.md` — users, problems, features, exclusions | `product-requirements.schema.json` |
| **2** | **🏗️ Technical Architecture** | `.md` — stack, DB schema, API, file structure | `technical-architecture.schema.json` |
| **3** | **🎨 UI Specifications** *(optional)* | `.md` — design system, components, screens | `ui-specifications.schema.json` |
| **4** | **📋 Tasks Plan** | `📋 Tasks Template.md` → generates `tasks.md` with phases + groups | — |

### 🔸 Execution (Tasks = Phase 4)

| Document | Function |
|---|---|
| **📋 Tasks Template** | Guide to generate `tasks.md` — phases → task groups → executable tasks |
| **✅ Dev Checklist** | Prompt quality standards for structured AI interaction |
| **🎯 Accountability Rules** | 4 rules: docs first, stay in scope, no undocumented changes, minimum code |

### 🔸 Configuration

| Document | Function |
|---|---|
| **AGENTS.md** | Protocol for autonomous agents + fillable project template |
| **📋 Project Template** | Project profile + development log |
| **🚀 Quick Start Guide** | This guide in step-by-step format |

---

## 🎓 How to use this system

### 📊 Phase 1: Product Requirements
1. Read `📊 Product Requirements.md` as your questionnaire
2. Answer: target users, problem, P0/P1/P2 features, exclusions, metrics
3. Ask AI: *"Fill product-requirements.schema.json with this information: [your answers]"*
4. Save as `product-requirements.json` in your project

### 🏗️ Phase 2: Technical Architecture
1. Read `🏗️ Technical Architecture.md` as your questionnaire
2. Define: tech stack, DB schema, API endpoints, file structure
3. Ask AI: *"Fill technical-architecture.schema.json with: [stack, tables, endpoints]"*
4. Save as `technical-architecture.json` in your project

### 🎨 Phase 3: UI Specifications *(optional)*
1. Read `🎨 UI Specifications.md` as your questionnaire
2. Define: design system, components, screens, navigation
3. Ask AI to fill `ui-specifications.schema.json`
4. Save as `ui-specifications.json`

### 📋 Phase 4: Tasks Plan
1. Read `📋 Tasks Template.md` to understand the format
2. Ask AI: *"Based on technical-architecture.json, generate tasks.md with phases and task groups"*
3. Save `tasks.md` in your project
4. Tasks.md is generated after architecture because it defines which modules, APIs, and components exist

### ⚙️ Configure the Agent *(optional)*
1. Copy `AGENTS.md` to your project root
2. Fill the `📋 PROJECT CONTEXT` block with your project details
3. Final project structure:
   ```
   your-project/
   ├── AGENTS.md
   ├── product-requirements.json
   ├── technical-architecture.json
   ├── ui-specifications.json      (optional)
   └── tasks.md
   ```

### 🔥 Development Loop
```
Pick next task group from tasks.md
        ↓
"AI, execute Group X.Y: [name]"
        ↓
AI completes all tasks in the group
        ↓
You test → commit
        ↓
Move to next group
```

---

## ✨ Benefits

- **🎯 Precise code** — AI follows specs, doesn't improvise
- **⚡ Faster** — no "that's not what I meant" cycles
- **📈 Consistent** — aligned architecture, design, and functionality
- **🔄 Iterable** — one task group at a time, test, advance
- **📦 Portable** — `.json` files travel with your project

---

*🧠 Stop expecting AI to read your mind. Give it structured docs and an execution plan.*

---

*This file is a template overview. For step-by-step instructions, see `🚀 Quick Start Guide.md`.*
