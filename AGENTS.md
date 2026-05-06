# AGENTS.md (Root Orchestrator)

> **SYSTEM INSTRUCTION FOR AI AGENTS:** This is the root orchestrator for rom-manager-landing.

## Global Rules

1. **Communication Language:** You MUST always respond to the user in **es**.
2. **Code Language:** All code, variables, functions, and technical implementations MUST be written in **English**.
3. **No Touch Rule:** The directories  must NEVER be modified unless explicitly instructed by the user.
4. **Git Commit Rule:** You MUST NEVER create Git commits unless the user explicitly instructs you to do so. If the user asks for a commit, you MUST invoke the `@git-manager` agent.

## Project Configuration

- **Name:** rom-manager-landing
- **Framework:** Astro
- **CSS Framework:** Tailwind CSS
- **Test Runner:** None
- **Default Merge Target:** main
- **Blocked Merge Targets:** 
- **Pre-push Test Command:** 

## Global Agents (Symlinked)

These agents live in `~/.dotfiles/editors/opencode/agents/` and are symlinked to `.opencode/agents/`.
They contain minimal instructions and load local skills for project-specific behavior.

- **Clean Code & Anti-Hardcoding**: Invoke `@clean-js`.
- **Git Operations**: Invoke `@git-manager`.
- **Branch Merging**: Invoke `@git-merge`.
- **Project Setup/Reconfiguration**: Invoke `@project-setup`.

## Local Agents (Generated)

These agents are generated specifically for this project and live in `.opencode/agents/`.
They contain minimal instructions and load local skills with dynamic project context.

- **Documentation**: Invoke `@docs`.
- **Testing & QA**: Invoke `@testing`.
- **Error Diagnostics**: Invoke `@debugger`.
- **Architecture**: Invoke `@architecture`.

## Progressive Discovery Index

Before performing a task, load the specific role or documentation:
- **Clean Code Rules**: Invoke `@clean-js` (loads `.opencode/skills/clean-js/SKILL.md`).
- **Git Operations**: Invoke `@git-manager` (loads `.opencode/skills/git-manager/SKILL.md`).
- **Branch Merging**: Invoke `@git-merge` (loads `.opencode/skills/git-merge/SKILL.md`).
- **Documentation Standards**: Invoke `@docs` (loads `.opencode/skills/docs/SKILL.md`).
- **Testing & QA**: Invoke `@testing` (loads `.opencode/skills/testing/SKILL.md`).
- **Error Diagnosis**: Invoke `@debugger` (loads `.opencode/skills/debugger/SKILL.md`).
- **Architecture**: Invoke `@architecture` (loads `.opencode/skills/architecture/SKILL.md`).
- **Coding Conventions**: Refer to `docs/conventions.md`.
- **Commit Standards**: Refer to `docs/standard-commits.md`.
