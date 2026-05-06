# Architecture Skill

> **PROJECT CONTEXT:** This skill was generated for a Astro project.

## 🇪🇸 Versión en Español

### Principios Arquitectónicos

1. **Separación de responsabilidades:** Cada módulo debe tener una única responsabilidad.
2. **Dependencias explícitas:** Evitar dependencias circulares.
3. **Configuración centralizada:** Usar archivos de configuración para valores variables.

### Estructura Recomendada

La estructura de carpetas debe adaptarse al framework detectado.

---

## 🇬🇧 English Version (For AI Agents)

### Architectural Rules

- Rule: Each module MUST have a single, well-defined responsibility.
- Rule: Circular dependencies MUST be avoided.
- Rule: Configuration MUST be centralized (no hardcoded values).
- Rule: Public APIs MUST be documented and versioned.
- Constraint: NEVER assume specific paths without checking project structure.
- Constraint: MUST respect directories listed in No Touch Rule.

### Project Configuration

- Framework: Astro
- CSS Framework: Tailwind CSS
- Frontend: true

### Recommended Folder Structure

```
src/
├── assets/         # Static files (images, fonts)
├── components/     # Reusable Astro/UI components
├── content/        # Content collections (Astro)
├── layouts/        # Page layouts
├── pages/          # File-based routes
├── styles/         # Global CSS (Tailwind)
├── utils/          # Utility functions
└── lib/            # Core library code
```

### No Touch Directories



### CSS Architecture

- Rule: Prioritize Tailwind utility classes.
- Rule: Custom CSS MUST go to centralized style files.
- Constraint: NEVER use scoped or inline styles in components.
