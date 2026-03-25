# AGENTS.md

## Stack

This is a boilerplate template for KiloCode configurations. When using this template, update with your project's specific stack:

- Framework: [e.g., Next.js, Express, Django, FastAPI]
- Language: [e.g., TypeScript, JavaScript, Python, Rust]
- Package Manager: [e.g., npm, pip, poetry, cargo]

## Commands

Common commands for projects using this boilerplate (update as needed):

- `npm run dev` - Start dev server
- `npm run build` - Production build
- `npm run start` - Start production server
- `npm run lint` / `npm run check-lint` - Run linters
- `npm run check-format` / `npm run format` - Format code
- `npm run check-types` - Type checking

## Non-Obvious Conventions

Project-specific conventions that differ from standard practices (examples - customize for your project):

- Path aliases: `@/components/*`, `@/features/*`, `@/providers/*`, `@/libs/*` → `./src/*`
- i18n: next-translate-plugin, locales in `/locales` (en, id), middleware strips locale from URL
- Test framework: [e.g., Jest, Vitest, Mocha, PyTest]

## Codebase Search Guidelines

When **KiloCode's Codebase Indexing is enabled**, the AI will automatically use semantic search to find relevant code across your project. The AI will:

- Automatically use `codebase_search` for natural language queries about your codebase
- Perform semantic searches like "find user authentication logic" or "show me database connection handling"
- Combine search results with other tools for comprehensive analysis

## Mode-Specific Rules

- [Ask Mode](.kilocode/rules-ask/AGENTS.md)
- [Code Mode](.kilocode/rules-code/AGENTS.md)
- [Architect Mode](.kilocode/rules-architect/AGENTS.md)
- [Debug Mode](.kilocode/rules-debug/AGENTS.md)
- [Orchestrator Mode](.kilocode/rules-orchestrator/AGENTS.md)

## Serena Workflow

This project uses the Serena workflow for enhanced code intelligence:

### Available Workflows

- `/serena-setup.md` - Initial project setup and context loading
- `/serena-dev-workflow.md` - Complete development workflow
- `/serena-general.md` - General purpose workflow

### Core Workflow Steps

1. **LOAD CONTEXT** → `list_memories()` + `read_memory()` from Serena
2. **THINK** → Sequential Thinking for analysis
3. **LOOKUP** → Context7 if external libraries involved
4. **EXECUTE** → Serena tools for code operations
5. **VERIFY** → Check results
6. **SAVE** → `write_memory()` to Serena after completing work

### Memory Management

- ALWAYS load memories BEFORE starting any task
- ALWAYS save memories AFTER completing significant work
- Memory naming: `descriptive_name_YYYY_MM` (e.g., `auth_system_2025_01`)
