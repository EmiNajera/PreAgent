# PreAgent — Prompts para Hermes

## Prompt 1: Setup (primera vez)

> Usa este prompt UNA SOLA VEZ para instalar PreAgent como recurso permanente.

```text
PreAgent es una metodología spec-first para desarrollo de software con IA.

1. Descarga el repo en una carpeta permanente:
   git clone https://github.com/EmiNajera/preagent.git ~/Documents/PreAgent

   (Si el repo no existe aún en GitHub, la fuente local está en
   ~/Documents/PreAgent/ — cópiala a una ubicación fija)

2. Crea un skill de Hermes que apunte al recurso:
   - Skill name: preagent
   - Descripción: "Metodología spec-first para desarrollo de software con IA"
   - Contenido: breve resumen de los 4 pasos + ruta al template

3. Guarda este recurso como carpeta importante en la rama principal.
   No es un proyecto, es un sistema metodológico.
   Debe quedar disponible para cualquier sesión futura.

Estructura del recurso:
~/Documents/PreAgent/
├── README.md                    ← Descripción general
├── template/                    ← Plantillas para proyectos
│   ├── AGENTS.md                ← Protocolo para el agente
│   ├── 📊 Product Requirements.md
│   ├── 🏗️ Technical Architecture.md
│   ├── 🎨 UI Specifications.md
│   ├── 📋 Tasks Template.md
│   ├── *.schema.json
│   └── ... (resto de plantillas)
```

---

## Prompt 2: Ejecutar PreAgent en un proyecto (uso diario)

> Usa este prompt al INICIO de cada proyecto nuevo.  
> Le dice al agente qué archivos leer y cuáles ignorar.

```text
Vamos a desarrollar [Nombre del Proyecto] usando la metodología PreAgent.

No leas todos los archivos del template. Solo necesitas:

📌 ARCHIVOS ESENCIALES (lee estos siempre):
- product-requirements.json    → alcance, usuarios, features
- technical-architecture.json  → stack, DB, API, estructura
- ui-specifications.json       → diseño (si existe)
- tasks.md                     → plan de ejecución (fase actual)
- AGENTS.md                    → protocolo de ejecución

🚫 ARCHIVOS QUE NO DEBES LEER (son para el humano, no para el agente):
- Los .md template (Product Requirements Template.md, etc.)
- Los .schema.json (son plantillas vacías)
- Dev Checklist.md
- Quick Start Guide.md
- El Hub principal
- Cualquier archivo sin contenido del proyecto real

📋 REGLAS DE EJECUCIÓN:
1. Tu tarea asignada está en tasks.md → grupo activo
2. No salgas del grupo asignado
3. No modifiques archivos fuera del scope del grupo
4. Si encuentras deuda técnica, anótala — no la arregles ahora
5. Cada grupo se prueba y se commitea antes del siguiente
```
