# 🚀 Quick Start Guide

*From zero to shipping with the PreAgent methodology*

---

## 🎯 What You'll Achieve

- ✅ Three core docs that define your entire app (.md + .schema.json)
- ✅ A phased task plan with testable task groups (tasks.md)
- ✅ AI agent configured to execute with structure, not vibe (AGENTS.md)

---

## 🗺️ The 4 Steps (~2 hours total)

### Step 1: Product Requirements (30 min)

1. Lee `📊 Product Requirements.md` — es tu cuestionario
2. Responde cada sección (usuarios, problema, features, exclusiones, métricas)
3. Pide a la IA que llene `product-requirements.schema.json` con tus respuestas
4. Guarda el resultado como `product-requirements.json` en tu proyecto

### Step 2: Technical Architecture (45 min)

1. Lee `🏗️ Technical Architecture.md` — es tu cuestionario
2. Define stack, DB schema, API structure, file organization
3. Pide a la IA que llene `technical-architecture.schema.json`
4. Guarda como `technical-architecture.json` en tu proyecto

### Step 3: Tasks Plan (30 min)

1. Lee `📋 Tasks Template.md` para entender el formato
2. Usa el prompt incluido con tu architecture.json
3. La IA genera `tasks.md` con fases y task groups
4. Guarda `tasks.md` en tu proyecto

### Step 4: Configure the Agent (10 min)

1. Copia `AGENTS.md` a la raíz de tu proyecto
2. Llena el bloque `📋 PROJECT CONTEXT` con los datos de tu proyecto
3. Estructura final del proyecto:
   ```
   your-project/
   ├── AGENTS.md
   ├── product-requirements.json
   ├── technical-architecture.json
   ├── ui-specifications.json      (opcional)
   └── tasks.md
   ```

---

## 🔥 Development Loop

```
Pick next task group from tasks.md
        ↓
Prompt agent: "Execute Group X.Y: [name]"
        ↓
Agent completes all tasks in the group
        ↓
You test the group → commit
        ↓
Move to next group
```

---

## ✅ Verification

**Setup complete when:**
- [ ] 3 core docs filled out (no quedan placeholders)
- [ ] .json files generados y en raíz del proyecto
- [ ] tasks.md has phases + groups + acceptance criteria
- [ ] AGENTS.md in project root (con PROJECT CONTEXT lleno)
- [ ] Agent responds with doc references, not generic code

**Ready to develop when:**
- [ ] First task group executed successfully
- [ ] Agent stays within group scope without drifting
- [ ] You can test → commit → next group without friction

---

## 🛠️ Troubleshooting

**Agent ignores the docs?** → Check AGENTS.md is in project root and .json files are accessible.

**Agent drifts beyond task group?** → Add: "Complete ONLY the tasks in this group. Do not touch other files."

**tasks.md is too vague?** → Break groups into smaller tasks. Each task should touch 1-3 files max.

---

*🧠 .md es tu cuestionario. .schema.json es tu plantilla. .json en tu proyecto es tu plano de ejecución. No vibe coding.*
