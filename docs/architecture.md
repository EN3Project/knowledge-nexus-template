# Architecture

Knowledge Nexus is organized around four context layers.

## Layers

| Layer | File / Folder | Purpose |
|---|---|---|
| Manifest | `SYSTEM_MANIFEST.md` | Small boot contract and system identity |
| Protocols | `99_System/Prompts/Protocols/` | Command semantics |
| Workflows | `99_System/Prompts/Workflows/` | Repeatable multi-step procedures |
| Memory | `99_System/Memory/INDEX.md` | Lightweight long-term memory index |
| Handoff | `99_System/Handoff/CURRENT_CONTEXT.md` | Short-term restart buffer |

## Design Rules

- Keep the manifest small.
- Put command details in `CommandProtocol.md`.
- Put procedural details in workflow files.
- Load `Memory/INDEX.md` before detailed memories.
- Never auto-load `CURRENT_CONTEXT.md`; ask the user first.
- Treat destructive changes as confirmation-only.

## Why Profiles

The private Nexus system can grow deep and personal. A public template should be
installable in layers:

1. Core first.
2. Research workflows when needed.
3. Maintenance workflows when the vault grows.
4. Personalization only when the user wants it.
