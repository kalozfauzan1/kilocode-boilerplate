# Project Coding Rules (Non-Obvious Only)

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
