# Plan Files (`/plans`)

All non-trivial implementation work should be tracked in `/plans`.

## Filename Convention

- `YYYY-MM-DD_<task-slug>.md`

## Required Sections

```md
# Task: <title>
Status: Planned | In Progress | Blocked | Done
Owner Mode: orchestrator -> code

## Objective
- ...

## Scope
- In scope: ...
- Out of scope: ...

## Checklist
- [ ] Step 1 ...
- [ ] Step 2 ...

## Progress Log
- 2026-03-25 10:00 WIB | orchestrator | Plan created
- 2026-03-25 10:20 WIB | code | Implemented X in `path/to/file`; updated tests

## Risks / Notes
- ...

## Final Summary
- ...
```

## Ownership Rules

- **Architect**: provides design + `Execution Inputs` for planning.
- **Orchestrator**: creates and maintains plan structure/status.
- **Code**: updates checklist/progress after each implementation batch.

If code changes are made without corresponding plan updates, the task is incomplete.
