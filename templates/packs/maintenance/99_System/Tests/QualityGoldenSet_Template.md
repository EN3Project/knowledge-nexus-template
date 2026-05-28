# Quality Golden Set Template

Use this file to test whether your Knowledge Nexus setup answers important
system questions consistently.

## Scoring

| Metric | Meaning | Scale |
|---|---|---|
| faithfulness | matches source files | 0-2 |
| completeness | includes required details | 0-2 |
| usability | actionable and concise | 0-2 |

## Questions

### Q-01

- **Q:** What is loaded during `run` / `load`?
- **Expected:** Manifest, Memory INDEX, and optional handoff check; detailed memory only when needed.
- **Source:** `SYSTEM_MANIFEST.md`, `CommandProtocol.md`
- **Score:** -- / -- / --

### Q-02

- **Q:** What is the difference between `condense` and `handoff`?
- **Expected:** `condense` prints a fixed summary; `handoff` saves the same format to `CURRENT_CONTEXT.md`.
- **Source:** `Condense.md`, `Handoff.md`
- **Score:** -- / -- / --

### Q-03

- **Q:** Which changes require confirmation?
- **Expected:** destructive changes, archive moves, permanent note rewrites, and memory updates when uncertain.
- **Source:** `SYSTEM_MANIFEST.md`, maintenance workflows
- **Score:** -- / -- / --
