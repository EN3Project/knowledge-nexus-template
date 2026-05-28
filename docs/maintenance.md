# Maintenance Checklist

Use this checklist when syncing improvements from a private Nexus into the template.

## When to Run

- A command was added, renamed, or removed in the private Nexus
- A workflow procedure changed
- A new pack-level feature was stabilized and is generic enough to share
- Docs or tutorials feel stale after real-world use

## Sync Checklist

### 1. Identify What Changed

- [ ] Review recent commits or session notes in the private Nexus
- [ ] List changed files: `SYSTEM_MANIFEST.md`, `CommandProtocol.md`, workflow files, agent definitions
- [ ] Mark each change as **generic** (goes to template) or **personal** (stays private)

### 2. Update Template Files

- [ ] `templates/core/SYSTEM_MANIFEST.md` — reflect any manifest rule changes
- [ ] `templates/core/99_System/Prompts/Protocols/CommandProtocol.md` — sync command specs
- [ ] `templates/core/99_System/Prompts/Workflows/` — update changed workflows
- [ ] `templates/packs/*/` — update pack files if a pack-level feature changed

### 3. Update Docs

- [ ] `docs/getting-started.md` — update if install steps or core commands changed
- [ ] `docs/profiles.md` — update if a pack's scope changed
- [ ] `docs/tutorials/` — update affected tutorials
- [ ] `docs/llm-compatibility.md` — update if LLM behavior guidance changed

### 4. Verify Template Integrity

- [ ] Confirm `templates/core/` works standalone (no private paths or personal context)
- [ ] Confirm pack files reference only paths within their own pack or core
- [ ] Confirm no personal details leaked (persona names, private project names, local paths)

### 5. Push

- [ ] Commit with a clear message describing what was synced
- [ ] Push to `main`

## What Stays Out of the Template

- Private persona files (e.g., named character personas)
- Personal self-context, observer profile, job status
- Company exchange protocols
- Absolute local paths
- Private project module definitions
