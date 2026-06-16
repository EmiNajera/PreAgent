# 📋 Tasks Template

*Phased task groups — the Anti Vibe Coding execution layer of PreAgent*

---

## 🎯 What is tasks.md?

`tasks.md` is the **execution plan**. While the core docs define *what* and *how*, `tasks.md` organizes the work into **phases → task groups** that an AI agent executes as coherent units.

---

## 🧠 Prompt to Generate It

After you have your architecture defined, use:

```
Based on that architecture, generate a phased implementation plan for the MVP.

Organize the work into phases (e.g., Foundation, Core Features, Polish).
Within each phase, group related tasks that can be executed together.

Each task must:
- Be small and testable
- Have a clear beginning and end
- Address only one technical concern

I'll be using an AI agent that will execute one task group at a time.
I will test the group, commit, and then proceed to the next group.
```

Save the output as `tasks.md` in the project root.

---

## 📋 Structure: Phases → Task Groups → Tasks

```markdown
# tasks.md

## 🔷 Phase 1: Foundation (tasks T01–T08)
*Goal: Project scaffold, auth, DB schema, core API structure.*

### Group 1.1: Project Setup
- [ ] **T01** Scaffold Next.js + Prisma + Tailwind
- [ ] **T02** Configure tsconfig, ESLint, folder structure
- [ ] **T03** Set up Supabase/DB connection + env vars

### Group 1.2: Auth & Core API
- [ ] **T04** Implement auth (login, register, session)
- [ ] **T05** Create base API middleware (auth, validation, errors)
- [ ] **T06** Define and migrate core DB schema
- [ ] **T07** Generate Prisma client + seed script
- [ ] **T08** Create shared UI shell (layout, nav, theme)

## 🔷 Phase 2: Core Features (tasks T09–T20)
*Goal: Main business modules working end-to-end.*

### Group 2.1: Patients Module
- [ ] **T09** Patient API routes (CRUD)
- [ ] **T10** PatientForm component + validation
- [ ] **T11** PatientList with search + pagination

### Group 2.2: Appointments Module
- [ ] **T12** Appointment API routes (CRUD)
- [ ] **T13** CalendarView component
- [ ] **T14** AppointmentForm with patient lookup
```

---

## 📋 Task Format

```markdown
- [ ] **T04** Implement auth (login, register, session)
  **File(s):** `app/api/auth/`, `lib/auth.ts`
  **Depends on:** T03 (DB connection)
  **Acceptance:**
  - Login with email + password returns JWT
  - Register creates user with hashed password
  - Protected routes reject unauthenticated requests
```

---

## 🧠 Task Group Protocol

Start each session with:

```
You are the engineer of this project.
- Read architecture.md and tasks.md thoroughly.
- Execute the next pending task group.
- Complete all tasks in the group before stopping.
- I will test the group, commit, and then we proceed to the next.

Coding protocol:
- Write the minimum required code for each task
- Don't make unrelated changes outside the group scope
- Keep code clean, modular, and testable
- Don't break existing features
- If infrastructure changes are required, clearly notify me first
```

---

## 🚫 Anti-Vibe Rules

| ❌ Vibe Coding | ✅ Structured (tasks.md) |
|---|---|
| "Build me a dashboard" | "Execute Group 3.2: Dashboard widgets" |
| AI decides scope on the fly | Task group defines exact scope |
| 15 files changed, untested | Group executed → tested → committed atomically |
| Features mixed with refactors | Refactors are their own explicit group |
| No clear "done" state | Every group has acceptance criteria |

---

## 🔗 Where It Fits

| PreAgent Doc | Role |
|---|---|
| `product-requirements.json` | Defines *what* to build |
| `technical-architecture.json` | Defines *how* it's structured |
| **`tasks.md`** | **Phases → Groups → Tasks execution plan** |
| `AGENTS.md` | Enforces the protocol for autonomous agents |

---

*🧠 Phases give direction. Groups give focus. Tasks keep it testable. No vibe coding.*
