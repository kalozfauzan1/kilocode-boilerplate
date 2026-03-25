# Project Debug Rules (Non-Obvious Only)

## Mandatory Tool Usage

- **Sequential Thinking**: Always use for systematic debugging
- **Context7**: Always query for:
  - Known issues with libraries in use
  - Debugging patterns for your framework/language

## Requirement Clarification Policy

- **ALWAYS ask before debugging** when:

  - Error context is incomplete
  - Expected vs. actual behavior is not clearly stated
  - Steps to reproduce are missing
  - Environment details are unclear

- **Use `ask_followup_question` tool** with:
  - Specific questions about the error context
  - 2-4 potential root causes to investigate

## Environment

<!-- TODO: Add your project's environment requirements -->
<!-- EXAMPLE: Requires `.env` with `NEXT_PUBLIC_API` and `NEXT_PUBLIC_API_CONTENT` -->
<!-- EXAMPLE: NEXTAUTH_SECRET required for auth -->

## Gotchas

<!-- TODO: Add common gotchas specific to your project -->
<!-- EXAMPLE: Middleware strips locale from URL - check search params for `lang` -->
<!-- EXAMPLE: Auth middleware commented out in src/middleware.ts -->

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
