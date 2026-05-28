# Getting Started

## 1. Install Core

Copy the contents of `templates/core/` into your Obsidian vault root.

Expected result:

```txt
your-vault/
  SYSTEM_MANIFEST.md
  99_System/
    README.md
    Memory/INDEX.md
    Handoff/README.md
    Prompts/
      Protocols/CommandProtocol.md
      Workflows/Condense.md
      Workflows/Handoff.md
      Workflows/Crystallize.md
```

## 2. Start a Session

Tell your LLM:

```txt
run
```

The agent should:

1. Read `SYSTEM_MANIFEST.md`.
2. Read `99_System/Memory/INDEX.md`.
3. Check whether `99_System/Handoff/CURRENT_CONTEXT.md` exists.
4. Ask before loading or deleting short-term context.

## 3. Use the Core Loop

| Command | Purpose |
|---|---|
| `run` / `load` | Restore persona, memory index, and optional handoff |
| `condense` | Print a fixed-format context summary |
| `handoff` | Save short-term context to `CURRENT_CONTEXT.md` |
| `clear-handoff` | Delete only `CURRENT_CONTEXT.md` |
| `crystallize` | Propose long-term memory updates |

## 4. Add Packs Later

Install packs only when you need them:

- `templates/packs/research/` for source-backed research.
- `templates/packs/compile/` for LLM-ready compiled knowledge artifacts.
- `templates/packs/maintenance/` for system hygiene and quality checks.
- `templates/packs/personalization/` for persona and self-context.

## 5. Continue With Tutorials

- [Tutorial 01: First Core Session](tutorials/01-core-first-session.md)
- [Tutorial 02: Add Research Pack](tutorials/02-add-research-pack.md)
- [Tutorial 03: Compile a Knowledge Artifact](tutorials/03-compile-knowledge-artifact.md)
- [Tutorial 04: Maintain Your Vault](tutorials/04-maintain-your-vault.md)
- [Tutorial 05: Personalize Safely](tutorials/05-personalize-safely.md)

## 6. Optional MCP

Knowledge Nexus works as files first. MCP is optional.

If you use an MCP vault server, expose at least:

- `vault_search(query)`
- `vault_read(path)`
- `vault_write(path, content)`

Keep MCP implementation details out of prompts when possible.
