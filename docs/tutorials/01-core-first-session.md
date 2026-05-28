# Tutorial 01: First Core Session

## Goal

Install Core into a blank Obsidian vault and run your first Knowledge Nexus
session.

## What You Will Build

A vault that can:

- load a memory index
- create a handoff
- clear stale context
- propose a memory update

## Steps

1. Create a blank Obsidian vault.
2. Copy everything inside `templates/core/` into the vault root.
3. Open your LLM tool in that vault.
4. Type:

```txt
run
```

5. Ask:

```txt
Help me plan a two-week writing project.
```

6. Type:

```txt
handoff
```

7. Confirm this file exists:

```txt
99_System/Handoff/CURRENT_CONTEXT.md
```

8. Type:

```txt
clear-handoff
```

## Expected Result

You should understand the difference between:

- Memory: long-term reusable context.
- Handoff: short-term restart buffer.
- Condense: visible summary without saving a file.
