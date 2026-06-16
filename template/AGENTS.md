# AGENTS.md

*PreAgent methodology for autonomous AI agents — read once, execute with structure.*

> **Contexto:** Este archivo aplica cuando trabajas con Codex CLI, agentes autónomos sin plataforma propia o proyectos standalone.  
> **No necesario en:** Hermes Agent, OpenClaw u otros entornos que ya tienen su propio protocolo de agente nativo (AGENTS.md integrado o similar).  
> En esos entornos, el plan vive en product-requirements.md + tasks.md, pero el *cómo ejecutar* lo dicta la plataforma, no este archivo.

---

## ⚠️ HOW TO USE THIS FILE

You are an autonomous AI agent. This file defines:
1. **How you work** — the execution protocol (fixed, do not modify)
2. **What you work on** — the project context (filled per project)

At the start of each session, read this file, then proceed.

---

## 📋 PROJECT CONTEXT

*Fill this section when setting up a new project. The agent reads this to know what it's building.*

```yaml
project:
  name: "[Project Name]"
  description: "[One-line description of what this app does]"
  type: "[SaaS / Web App / Mobile / E-commerce / Internal Tool]"

docs:
  product_requirements: "product-requirements.json"
  technical_architecture: "technical-architecture.json"
  ui_specifications: "ui-specifications.json"       # optional
  tasks: "tasks.md"

tech_stack:
  frontend: "[Next.js / React / Vue / etc.]"
  language: "[TypeScript / JavaScript]"
  styling: "[Tailwind CSS / etc.]"
  backend: "[Next.js API routes / Express / FastAPI / etc.]"
  database: "[PostgreSQL / Supabase / etc.]"
  orm: "[Prisma / Drizzle / etc.]"
  auth: "[NextAuth / Clerk / Supabase Auth / etc.]"
  package_manager: "[pnpm / npm / yarn]"

conventions:
  test_command: "[pnpm test / npm test / etc.]"
  lint_command: "[pnpm lint / npm run lint]"
  build_command: "[pnpm build / npm run build]"
  format_command: "[pnpm format / prettier --write .]"

current:
  phase: "[Phase 1 / Phase 2 / Phase 3]"
  active_group: "[Group X.Y: Name]"
  status: "[not_started / in_progress / completed]"
```

---

## 🧠 EXECUTION PROTOCOL

*This is the fixed protocol. Follow it exactly. Do not deviate.*

### 1. BEFORE WRITING ANY CODE

Read these files — they are the source of truth:
- `product-requirements.json` — what to build, who it's for, what's excluded
- `technical-architecture.json` — tech stack, DB schema, API patterns, file structure
- `tasks.md` — your assigned task group for this session

### 2. SCOPE: STAY IN YOUR GROUP

- You will be assigned **one task group** (e.g. "Group 2.1: Patients Module")
- Complete ONLY the tasks in that group
- Do NOT refactor, optimize, or add features outside the group
- If you discover issues outside scope: **note them, report them, do not fix them**
- If infrastructure changes are needed (new deps, config changes, DB migrations): **stop and report — do not proceed**

### 3. EXECUTION LOOP

```
1. Read docs (product-requirements.json, technical-architecture.json, tasks.md)
2. Execute ALL tasks in the assigned group
3. Write the minimum code that satisfies the acceptance criteria
4. Run lint → fix → run tests → fix (max 2 retry attempts per failure)
5. Report results:
   - ✅ Group completed: list what was done, which files changed
   - ❌ Group failed: explain what failed, what you tried, what you need
6. STOP. Do not proceed to the next group.
```

### 4. CODE STANDARDS

- Write the **minimum required code** — don't pre-build for future features
- Use the project's **existing patterns** — don't invent new ones
- Every component handles: **loading, empty, error, success** states
- Use **TypeScript types** — no `any` unless unavoidable
- Follow **file structure** from technical-architecture.json exactly
- **Don't break existing functionality** — if tests fail, fix before continuing

### 5. ERROR HANDLING

| Situation | Action |
|---|---|
| Test fails | Analyze → fix → retry (max 2 attempts). If still failing: report with details |
| Build fails | Same: analyze → fix → retry × 2. If stuck: report |
| Missing dependency | Check technical-architecture.json. If not listed: **stop and ask** |
| Unclear requirement | Check product-requirements.json. If still unclear: **stop and ask** |
| Scope creep detected | Note it, finish assigned group, report the discovery |

### 6. AFTER COMPLETING A GROUP

Report this structure:

```
## Group X.Y: [Name] — COMPLETED ✅

### Changes
- `path/to/file.tsx` — [what changed, why]
- `path/to/other.ts` — [what changed, why]

### Test results
- Tests: N passed, 0 failed
- Lint: clean
- Build: successful

### Notes
- [Anything the human should know before the next group]
- [Issues discovered outside scope]
```

---

## 📁 FILE STRUCTURE REFERENCE

*The agent should expect this layout in the project root:*

```
project-root/
├── AGENTS.md                      ← this file
├── product-requirements.json      ← what to build
├── technical-architecture.json    ← how it's structured
├── ui-specifications.json         ← (optional) visual specs
└── tasks.md                       ← phases + task groups
```

---

*🧠 Read the docs. Execute the group. Report. Stop. No vibe coding.*
