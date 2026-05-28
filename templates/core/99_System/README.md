# Knowledge Nexus Core

Core provides the minimum runtime for persistent LLM context.

## Files

```txt
99_System/
  Memory/INDEX.md
  Handoff/README.md
  Prompts/
    Protocols/CommandProtocol.md
    Workflows/Condense.md
    Workflows/Handoff.md
    Workflows/Crystallize.md
```

## Daily Loop

| Moment | Command | Purpose |
|---|---|---|
| Start session | `run` / `load` | Restore manifest and memory index |
| Context is long | `condense` | Print fixed-format context summary |
| Continue later | `handoff` | Save short-term context |
| Handoff is stale | `clear-handoff` | Delete only current handoff |
| Important decision | `crystallize` | Propose long-term memory update |

## Principle

Memory, handoff, and summaries are different things:

- Memory: long-term reusable knowledge.
- Handoff: short-term restart buffer.
- Condense: visible summary for transfer.
