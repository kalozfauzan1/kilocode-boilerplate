# Project Architecture Rules (Non-Obvious Only)

## Capability Boundary (Enforced)

- Scope: System design, planning, trade-off analysis, and architecture documentation.
- Allowed operations: read/search/inspect and markdown/doc outputs.
- Forbidden operations: source-code implementation, runtime behavior changes, dependency installs.
- Handoff trigger: If user asks to build/modify code, switch to Code mode first.

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

## Mandatory Deliverable: Design Artifact + Execution Inputs

- For non-trivial tasks, produce a design artifact before orchestration begins.
- The design artifact MUST include:
  - Problem statement and scope boundaries
  - Options considered + selected approach with trade-offs
  - Interface/contract expectations and affected areas
  - Risks, assumptions, and acceptance criteria
- Add a dedicated section titled `Execution Inputs` that is optimized for orchestrator handoff.
- `Execution Inputs` MUST contain:
  - Milestones that can become checklist items in `/plans/<task>.md`
  - Expected file impact areas (high-level only)
  - Validation requirements (tests/checks)
  - Rollback/mitigation notes
- Architect MUST NOT edit implementation files; architect outputs design and handoff-ready documentation only.

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
