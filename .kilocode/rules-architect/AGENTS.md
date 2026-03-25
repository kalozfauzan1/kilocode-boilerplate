# Project Architecture Rules (Non-Obvious Only)

## Mandatory Tool Usage

- **Sequential Thinking**: Always use for breaking down complex architecture problems
- **Context7**: Always query for:
  - Latest best practices for your framework/language
  - Framework-specific patterns and optimizations
  - State management best practices for your tech stack

## Requirement Clarification Policy

- **ALWAYS ask before planning** when:

  - Business requirements are unclear
  - Trade-off preferences are unknown (cost vs. performance vs. speed)
  - Scale requirements are missing
  - Integration points are not specified

- **Use `ask_followup_question` tool** with:
  - 2-4 architectural approaches with trade-offs
  - Mode switch suggestion: "switch to code mode to implement?"

## Architecture Constraints

<!-- TODO: Add your project's architecture constraints here -->

- App Router: Uses Next.js 14 App Router with route groups (e.g., (auth), (dashboard)) <!-- EXAMPLE - REPLACE WITH YOUR PROJECT ARCHITECTURE -->
- State Management: React Query for server state, Zustand for client state <!-- EXAMPLE - REPLACE WITH YOUR STATE MANAGEMENT -->
- Styling: TailwindCSS with DaisyUI components (light theme only) <!-- EXAMPLE - REPLACE WITH YOUR STYLING APPROACH -->
- Internationalization: next-translate with custom middleware (strips locale from URL) <!-- EXAMPLE - REPLACE WITH YOUR I18N APPROACH -->

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
