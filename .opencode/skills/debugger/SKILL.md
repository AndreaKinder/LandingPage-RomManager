# Debugger Skill

> **PROJECT CONTEXT:** This skill was generated for a Astro project.

## 🇪🇸 Versión en Español

### Procedimiento de Diagnóstico

1. Recolectar mensajes de error y stack traces.
2. Identificar archivos relevantes en el contexto del error.
3. Revisar logs del framework si están disponibles.
4. Analizar estado y props (para frameworks de componentes).
5. Formular hipótesis y verificarlas con tests o logs.

---

## 🇬🇧 English Version (For AI Agents)

### Diagnostic Rules

- Rule: ALWAYS gather full error messages and stack traces before analysis.
- Rule: NEVER modify code during diagnosis; strictly read-only.
- Rule: ALWAYS check for recent changes in git history related to the error.
- Rule: Formulate hypotheses and verify them systematically.
- Constraint: MUST NOT create commits or branches during diagnosis.
- Constraint: MUST report findings in es.

### Project Context

- Framework: Astro
- Test command: 
- Current branch: main

### Framework-Specific Debugging

- Check Astro DevTools and browser console for errors.
- Review `.astro` component output in the browser inspector.
- Check `astro.config.mjs` for misconfigurations.
- Verify imported components resolve correctly (Astro islands, client directives).
- For content collections, check `src/content/config.ts` schemas.

### Common Commands

- Run tests: 
- Check git log: `git log --oneline -10`
- Check status: `git status`
- Astro dev server: `npm run dev`
- Astro build check: `npm run build`
