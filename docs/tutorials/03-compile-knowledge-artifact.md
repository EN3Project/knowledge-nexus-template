# Tutorial 03: Compile a Knowledge Artifact

## Goal

Turn messy notes into one LLM-ready artifact.

## Why This Matters

Do not make the LLM reinterpret raw documents on every query. Stable knowledge
should be compiled once into a typed, cited, reusable artifact.

## What You Will Build

A `decision-guide` artifact with:

- scope
- key claims
- source links
- retrieval hints
- open questions

## Steps

1. Install Core.
2. Copy everything inside `templates/packs/compile/` into the vault root.
3. Inspect the example raw notes in `examples/compiled-artifact/raw-notes/`.
4. Ask:

```txt
compile-knowledge examples/compiled-artifact/raw-notes/ into a decision-guide artifact.
```

5. Confirm the artifact type and save destination.
6. Compare the raw notes against `examples/compiled-artifact/compiled/knowledge-base-decision-guide.md`.

## Expected Result

The compiled artifact should be easier for a future agent to use than the raw
notes. It should include source-linked claims and retrieval hints.
