# Memory Index

Lightweight index loaded during `run` / `load`. Keep this file small.

## Always Load

- Knowledge Nexus is an Obsidian-first memory and workflow layer for LLM agents.
- `SYSTEM_MANIFEST.md` is the boot contract.
- `CommandProtocol.md` is the command source of truth.
- `CURRENT_CONTEXT.md` is never auto-loaded; ask first.
- Destructive changes require user confirmation.

## User Preferences

- Add stable preferences here only after confirmation or clear repeated behavior.

## Active Protocols

- `condense` and `handoff` share the same fixed 11-section format.
- `handoff` writes to `99_System/Handoff/CURRENT_CONTEXT.md`.
- `clear-handoff` deletes only `CURRENT_CONTEXT.md`.
- `crystallize` proposes long-term memory changes; do not silently rewrite memory.

## Open Tasks

- Keep active tasks short and actionable.

## Related Files

- [[SYSTEM_MANIFEST]]
- [[99_System/Prompts/Protocols/CommandProtocol]]
- [[99_System/Handoff/README]]
