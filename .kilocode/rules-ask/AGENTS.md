# Project Documentation Rules (Non-Obvious Only)

## Ask Mode Specific Rules

## Capability Boundary (Enforced)

- Scope: Explanation, analysis, and requirement clarification only.
- Allowed operations: read/search/inspect operations and question-asking.
- Forbidden operations: source edits, file create/delete, destructive commands, dependency changes.
- Handoff trigger: If implementation is requested, switch to Code mode before any file change.

### Mandatory Tool Usage

- **Sequential Thinking**: Always use before answering questions
- **Context7**: Always query for library documentation

### Requirement Clarification Policy

- **ALWAYS ask before proceeding** when requirements are ambiguous or vague
- **Use `ask_followup_question` tool** with 2-4 suggested answers
- **Never assume** - explicitly state assumptions and ask for confirmation

### Non-Obvious Project Context

<!-- TODO: Add your project-specific context here -->

- "src/" contains the main application code <!-- EXAMPLE - REPLACE WITH YOUR PROJECT CONTEXT -->
- UI runs in browser with standard web APIs <!-- EXAMPLE - REPLACE WITH YOUR PROJECT CONTEXT -->
- Package.json scripts can be run from root directory <!-- EXAMPLE - REPLACE WITH YOUR PROJECT CONTEXT -->

### Serena Workflow (Mandatory)

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
