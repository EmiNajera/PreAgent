# ✅ Dev Checklist

*Enforce feature prompt standards for Cursor AI*

---

## 🎯 Purpose

This checklist ensures every prompt to Cursor includes the necessary context and follows established standards. No more vague requests that lead to generic code.

---

## 📋 Pre-Prompt Checklist

### 🔍 Before Writing Any Prompt

**Required Context:**

- [ ]  **Feature clearly defined** in Product Requirements
- [ ]  **Technical approach** aligns with Architecture doc
- [ ]  **UI specifications** exist for any visual components
- [ ]  **Acceptance criteria** is specific and testable

**Prompt Structure:**

- [ ]  **Clear objective** stated in first sentence
- [ ]  **Specific requirements** listed (not "make it work")
- [ ]  **Referenced documentation** (which JSON files to check)
- [ ]  **Expected outcome** described in detail

**Technical Requirements:**

- [ ]  **File paths** specified for changes
- [ ]  **Function/component names** provided
- [ ]  **Data flow** described (input → processing → output)
- [ ]  **Error handling** requirements included

---

## 🎯 Prompt Templates

### 🔧 Feature Implementation

```
**Objective:** Implement [specific feature name] as defined in product-requirements.json

**Requirements:**
- Reference: [specific section of requirements doc]
- Technical specs: [specific section of technical-architecture.json]
- UI specs: [specific section of ui-specifications.json]

**Implementation details:**
- File to modify: [exact file path]
- Component/function name: [specific name]
- Input parameters: [list expected inputs]
- Expected behavior: [specific user outcome]
- Error scenarios: [what could go wrong and how to handle]

**Acceptance criteria:**
- [ ] [Specific testable outcome 1]
- [ ] [Specific testable outcome 2]
- [ ] [Specific testable outcome 3]
```

### 🐛 Bug Fix

```
**Objective:** Fix [specific bug description]

**Current behavior:** [what happens now]
**Expected behavior:** [what should happen]
**Steps to reproduce:** [exact steps]

**Investigation:**
- Likely file locations: [where to look]
- Suspected root cause: [hypothesis]
- Related components: [what else might be affected]

**Fix requirements:**
- Must not break: [existing functionality]
- Should maintain: [performance/UX standards]
- Test scenarios: [how to verify fix]
```

### 🎨 UI Component

```
**Objective:** Create [component name] following ui-specifications.json

**Design system reference:**
- Component type: [atom/molecule/organism]
- Visual specs: [specific section in UI doc]
- Variants needed: [list all variants]
- States required: [default/hover/active/disabled/loading]

**Technical requirements:**
- Framework: [from technical-architecture.json]
- Props interface: [expected TypeScript types]
- Accessibility: [ARIA labels, keyboard support]
- Responsive behavior: [mobile/tablet/desktop]

**Integration:**
- Used in screens: [list specific screens]
- Parent components: [where it fits]
- Child components: [what it contains]
```

---

## 🚫 Prompt Anti-Patterns

**Avoid these vague requests:**

- ❌ "Make the login work"
- ❌ "Add a button here"
- ❌ "Fix the styling"
- ❌ "Implement the feature we discussed"
- ❌ "Make it look better"

**Instead use specific requests:**

- ✅ "Implement email/password authentication using Firebase Auth as specified in technical-architecture.json, with validation states defined in ui-specifications.json"
- ✅ "Add a primary button component with loading state that follows the Button atom specification in ui-specifications.json"
- ✅ "Fix button hover state to match primary-500 color from design system in ui-specifications.json"

---

## 🔄 Iterative Development

### 📝 When Refining Features

1. **Reference previous implementation**
2. **Specify exact changes needed**
3. **Maintain consistency** with existing code
4. **Update documentation** if architecture changes

### 🧪 Testing Requirements

Every prompt should include:

- **Unit test expectations**
- **Integration test scenarios**
- **User acceptance criteria**
- **Edge case handling**

---

## ⚡ Quick Reference

**Essential Questions Before Prompting:**

1. What specific outcome do I want?
2. Which docs should Cursor reference?
3. What are the acceptance criteria?
4. How will I know it's working correctly?
5. What could go wrong?

**Required Documentation References:**

- 📊 `product-requirements.json` - for user needs and feature scope
- 🏗️ `technical-architecture.json` - for implementation approach
- 🎨 `ui-specifications.json` - for visual and interaction design

---

*🎯 Remember: Specific prompts with clear context = accurate, efficient code generation*

## 🚫 Patrones Anti-Prompt

**Evita estas solicitudes vagas:**

- ❌ "Haz que el inicio de sesión funcione"
- ❌ "Añade un botón aquí"
- ❌ "Arregla el estilo"
- ❌ "Implementa la función que discutimos"
- ❌ "Hazlo verse mejor"

**En su lugar, usa solicitudes específicas:**

- ✅ "Implementa la autenticación de correo electrónico/contraseña usando Firebase Auth como se especifica en technical-architecture.json, con estados de validación definidos en ui-specifications.json"
- ✅ "Añade un componente de botón primario con estado de carga que siga la especificación del átomo Button en ui-specifications.json"
- ✅ "Corrige el estado hover del botón para que coincida con el color primary-500 del sistema de diseño en ui-specifications.json"

---

## 🔄 Desarrollo Iterativo

### 📝 Al Refinar Funcionalidades

1. **Hacer referencia a la implementación anterior**
2. **Especificar exactamente los cambios necesarios**
3. **Mantener consistencia** con el código existente
4. **Actualizar la documentación** si la arquitectura cambia

### 🧪 Requisitos de Pruebas

Cada prompt debe incluir:

- **Expectativas de pruebas unitarias**
- **Escenarios de pruebas de integración**
- **Criterios de aceptación del usuario**
- **Manejo de casos extremos**

---

## ⚡ Referencia Rápida

**Preguntas Esenciales Antes de Hacer Prompts:**

1. ¿Qué resultado específico quiero?
2. ¿Qué documentos debería consultar Cursor?
3. ¿Cuáles son los criterios de aceptación?
4. ¿Cómo sabré que funciona correctamente?
5. ¿Qué podría salir mal?

**Referencias de Documentación Requeridas:**

- 📊 `product-requirements.json` - para necesidades del usuario y alcance de funcionalidades
- 🏗️ `technical-architecture.json` - para enfoque de implementación
- 🎨 `ui-specifications.json` - para diseño visual y de interacción

---

*🎯 Recuerda: Prompts específicos con contexto claro = generación de código precisa y eficiente*