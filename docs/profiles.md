# Install Profiles

## Which Pack Do You Need?

Start with Core. Then ask yourself:

- Do you need to research topics and save source-backed notes?
  → Add **Research Pack**
- Do you want to compile scattered notes into LLM-ready artifacts?
  → Add **Compile Pack**
- Is your vault growing and starting to feel cluttered?
  → Add **Maintenance Pack**
- Do you want the agent to adapt to your working style?
  → Add **Personalization Pack**

You do not need all packs. Most users need only Core + one or two packs.

---

## Core

Minimum viable Knowledge Nexus.

Install:

```txt
templates/core/
```

Use for:

- persistent memory index
- session startup
- context compression
- short-term handoff

## Research Pack

Install after Core:

```txt
templates/packs/research/
```

Use for:

- source-backed research
- librarian / investigator / analyst / critic / scribe roles
- reusable research notes

## Compile Pack

Install after Core when you want to turn raw or scattered notes into reusable
LLM-ready artifacts.

```txt
templates/packs/compile/
```

Use for:

- compile-on-ingest workflows
- cross-note synthesis
- typed artifacts with citations
- progressive disclosure indexes

## Maintenance Pack

Install after Core, optionally after Research:

```txt
templates/packs/maintenance/
```

Use for:

- memory pruning
- system review
- open task audit
- quality golden set evaluation

## Personalization Pack

Install only when you want a named persona or self-context.

```txt
templates/packs/personalization/
```

Use for:

- persona templates
- self-context
- observer profile

Keep job-search notes, company exchange, and private project modules out of the
public template unless they are examples.
