# Command Protocol

## run / load

Startup sequence:

1. Read `SYSTEM_MANIFEST.md`.
2. Read `99_System/Memory/INDEX.md`.
3. If `99_System/Handoff/CURRENT_CONTEXT.md` exists, ask the user:
   - `load`
   - `leave`
   - `show first`
   - `delete`
4. Do not read detailed memories unless needed.

## condense

Summarize the current conversation in the fixed format defined by
`99_System/Prompts/Workflows/Condense.md`.

Do not save a file.

## handoff

Generate the same fixed format as `condense` and save it to:

```txt
99_System/Handoff/CURRENT_CONTEXT.md
```

## clear-handoff

Delete only:

```txt
99_System/Handoff/CURRENT_CONTEXT.md
```

Do not change Memory or permanent notes.

## crystallize

Extract reusable decisions, preferences, tasks, and system changes.

Default behavior:

1. Propose what should be saved.
2. Ask before writing memory.
3. Update `99_System/Memory/INDEX.md` if new memory affects startup context.

## Optional MCP

If an MCP vault server exists, use these tools when available:

- `vault_search(query)`
- `vault_read(path)`
- `vault_write(path, content)`
