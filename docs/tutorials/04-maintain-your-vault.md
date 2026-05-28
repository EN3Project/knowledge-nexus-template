# Tutorial 04: Maintain Your Vault

## Goal

Add maintenance workflows for a growing vault.

## Steps

1. Install Core.
2. Copy everything inside `templates/packs/maintenance/` into the vault root.
3. Run:

```txt
review-system
```

4. Review findings before accepting edits.
5. Run:

```txt
task-audit
```

6. Keep only active, actionable tasks in `Memory/INDEX.md`.

## Expected Result

You should identify stale docs, missing workflow coverage, and outdated tasks
without rewriting your whole vault.
