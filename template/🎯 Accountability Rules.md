# 🎯 Accountability Rules

*4 rules that prevent architectural drift and vibe coding*

---

## Rule 1: Docs Before Code

Before writing any code, consult:
- `product-requirements.json` → is this feature in scope?
- `technical-architecture.json` → does this follow existing patterns?
- `tasks.md` → is this the current task group?

**Red flag:** Implementing something not in the current task group.

---

## Rule 2: Stay in the Group

Execute only the tasks in the assigned group. No more, no less.

| ✅ | ❌ |
|---|---|
| Complete T09–T11 (Patients module) | Refactor the auth system "while I'm here" |
| Touch only files listed in the group | Touch 8 unrelated files |
| Stop when group acceptance criteria are met | Add "nice to have" improvements |

**If you discover technical debt during a group:** note it, finish the group, then create a dedicated refactor group.

---

## Rule 3: No Undocumented Changes

Any change that affects architecture requires updating the docs:

| Change | Doc to update |
|---|---|
| New dependency | `technical-architecture.json` (tech stack) |
| New DB table or column | `technical-architecture.json` (schema) |
| New API endpoint | `technical-architecture.json` (endpoints) |
| New feature idea | `product-requirements.json` (if in scope) |
| Scope change | `product-requirements.json` (exclusions/features) |

**Docs are the source of truth. Code reflects docs. Not the other way around.**

---

## Rule 4: Minimum Viable Code

- Write the minimum code that satisfies the acceptance criteria
- Don't pre-build for features that don't exist yet
- Don't add abstractions "just in case"
- If a task can be solved with 10 lines, don't write 100

---

## 🚨 Stop Immediately If

- Implementing features outside the current task group
- Using a library not in the approved tech stack
- Creating duplicate patterns instead of reusing existing ones
- Skipping error handling or validation
- Breaking existing functionality

---

*🏛️ Docs define the system. Rules protect the system. Groups execute the system.*
