# 🚀 PreAgent App Development Hub [TEMPLATE]

*Metodología de desarrollo con IA: documentos estructurados + task groups. Cero vibe coding.*

---

## 📖 Overview

El **sistema PreAgent** reemplaza prompts vagos con contexto estructurado. Tres documentos core definen tu app; tasks.md la ejecuta por fases; AGENTS.md le explica al agente autónomo cómo trabajar.

### Flujo de trabajo

```
📄 .md (cuestionario)  →  🤖 IA llena  →  📋 .schema.json  →  💾 .json en proyecto
```

Cada documento tiene:
- Un **`.md`** con instrucciones, ejemplos y el JSON schema de referencia
- Un **`.schema.json`** vacío — listo para que la IA lo llene con tu proyecto
- El resultado final es el **`.json`** que vive en la raíz de tu proyecto

---

## 📋 Documentos del Sistema

### 🔸 Fases del Sistema (Core Docs)

| Fase | Documento | Cuestionario | Schema JSON |
|---|---|---|---|
| **1** | **📊 Product Requirements** | `.md` — usuarios, problemas, features, exclusiones | `product-requirements.schema.json` |
| **2** | **🏗️ Technical Architecture** | `.md` — stack, DB schema, API, file structure | `technical-architecture.schema.json` |
| **3** | **🎨 UI Specifications** *(opcional)* | `.md` — design system, componentes, pantallas | `ui-specifications.schema.json` |
| **4** | **📋 Tasks Plan** | `📋 Tasks Template.md` — genera `tasks.md` con fases + task groups | — |

### 🔸 Ejecución (Tasks = Fase 4)

| Documento | Función |
|---|---|
| **📋 Tasks Template** | Guía para generar `tasks.md` — fases → task groups → tareas ejecutables |
| **✅ Dev Checklist** | Estándares de prompting estructurado |
| **🎯 Accountability Rules** | 4 reglas: docs first, stay in scope, no undocumented changes, minimum code |

### 🔸 Configuración

| Documento | Función |
|---|---|
| **AGENTS.md** | Protocolo para agentes autónomos + plantilla de proyecto rellenable |
| **📋 Project Template** | Ficha de proyecto + log de desarrollo |
| **🚀 Quick Start Guide** | Esta guía |

---

## 🎓 Cómo Usar Este Sistema

### 📊 Fase 1: Product Requirements
1. Lee `📊 Product Requirements.md` como cuestionario
2. Responde: usuarios, problema, features P0/P1/P2, exclusiones, métricas
3. Pide a la IA: *"Llena product-requirements.schema.json con esta información: [tus respuestas]"*
4. Guarda como `product-requirements.json` en tu proyecto

### 🏗️ Fase 2: Technical Architecture
1. Lee `🏗️ Technical Architecture.md` como cuestionario
2. Define: stack, DB schema, API endpoints, file structure
3. Pide a la IA: *"Llena technical-architecture.schema.json con: [tu stack, tablas, endpoints]"*
4. Guarda como `technical-architecture.json` en tu proyecto

### 🎨 Fase 3: UI Specifications *(opcional)*
1. Lee `🎨 UI Specifications.md` como cuestionario
2. Define: design system, componentes, pantallas, navegación
3. Pide a la IA que llene `ui-specifications.schema.json`
4. Guarda como `ui-specifications.json`

### 📋 Fase 4: Tasks Plan ← Continuación lógica del sistema
1. Lee `📋 Tasks Template.md`
2. Pide a la IA: *"Basado en technical-architecture.json, genera tasks.md con fases y task groups"*
3. Guarda `tasks.md` en tu proyecto
4. Tasks.md se genera **después de arquitectura** porque ahí se define qué módulos, APIs y componentes existen para poder planificarlos

### ⚙️ Configurar el Agente *(opcional)*
1. Copia `AGENTS.md` a la raíz de tu proyecto
2. Llena el bloque `📋 PROJECT CONTEXT` (nombre, stack, paths, fase actual)
3. Coloca los .json + tasks.md junto a AGENTS.md
4. El agente leerá AGENTS.md al iniciar y seguirá el protocolo

---

## ✨ Beneficios

- **🎯 Código preciso** — el agente sigue especificaciones, no improvisa
- **⚡ Más rápido** — sin ciclos de "no era lo que quería"
- **📈 Consistente** — arquitectura, diseño y funcionalidad alineados
- **🔄 Iterable** — un task group a la vez, testeas, avanzas
- **📦 Portable** — los .json viajan con el proyecto

---

*🧠 Deja de esperar que la IA lea tu mente. Dale docs estructurados y un plan de ejecución.*
