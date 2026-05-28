# Workflow: Handoff

## Objective

Save a short-term restart buffer using the same fixed format as `condense`.

## Procedure

1. Generate the `Condense.md` fixed format.
2. Save it to `99_System/Handoff/CURRENT_CONTEXT.md`.
3. Tell the user what was saved.

## Rules

- `CURRENT_CONTEXT.md` is temporary.
- Ask before loading it on the next `run` / `load`.
- Do not use handoff as long-term memory.
