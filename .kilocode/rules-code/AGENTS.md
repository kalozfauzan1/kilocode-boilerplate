# Project Coding Rules (Non-Obvious Only)

## Capability Boundary (Enforced)

- Scope: Implement features, refactor, and maintain code quality for requested scope.
- Allowed operations: create/edit/delete source and test files, run verification commands.
- Required: keep changes scoped, preserve backward compatibility unless user approved breaking changes.
- Forbidden operations: broad unrelated refactors, architecture-only planning without implementation intent.

## Mandatory Tool Usage

- **Sequential Thinking**: Always use before implementing complex features or refactoring
- **Context7**: Always query for library documentation when using:
  - Framework-specific patterns and features
  - Language-specific type system features
  - Framework-specific styling integration

## Requirement Clarification Policy

- **ALWAYS ask before implementing** when:

  - File paths or targets are unclear
  - Expected behavior has multiple interpretations
  - Edge cases are not specified
  - Changes might affect existing functionality

- **Use `ask_followup_question` tool** with 2-4 suggested implementation approaches
- **Never assume** - confirm understanding of requirements before writing code

## Mandatory Plan Progress Updates (/plans)

- Code mode MUST read the assigned plan file under `/plans/` before implementing.
- After each meaningful implementation batch (one or more file edits), code mode MUST update the same plan file with:
  - checklist item state change
  - timestamped progress log entry
  - short note of changed files and what was implemented
- When implementation is complete, code mode MUST:
  - mark remaining completed checklist items
  - set final status to `Done`
  - add a concise final summary
- If code changes are made but `/plans` progress is not updated, the task is considered incomplete.

## Import Order

<!-- TODO: Define your project's import order convention -->
<!-- EXAMPLE: react → built-in → third-party → `types` → `@local/` → `@/config/` → `@/providers/` → `@/libs/` → `@/hooks/` → `@/features/` → `@/components/` → relative -->

## Path Aliases

<!-- TODO: Define your path aliases (e.g., @/components/* → ./src/components/*) -->
<!-- EXAMPLE: `@/components/*` → `./src/components/*` -->

## Code Style

<!-- TODO: Define your project's code style guidelines -->
<!-- EXAMPLE: Single quotes (JSX too), semicolons, 2-space tabs, trailing commas (es5) -->

## Serena Workflow (Mandatory)

**ALWAYS follow this workflow when working with code:**

1. **LOAD CONTEXT** → `list_memories()` + `read_memory()` from Serena
2. **THINK** → Sequential Thinking for analysis
3. **LOOKUP** → Context7 if external libraries involved
4. **EXECUTE** → Serena tools for code operations
5. **VERIFY** → Check results
6. **SAVE** → `write_memory()` to Serena after completing work

**Memory Rules:**

- ALWAYS load memories BEFORE starting any task
- ALWAYS save memories AFTER completing significant work
- Keep memories CONCISE — focus on key points
- Memory naming: `descriptive_name_YYYY_MM` (e.g., `auth_system_2025_01`)
