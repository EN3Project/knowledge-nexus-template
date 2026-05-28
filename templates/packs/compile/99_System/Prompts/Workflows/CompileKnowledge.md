# Workflow: CompileKnowledge

## Objective

Turn raw notes, clippings, research outputs, or scattered resources into
LLM-ready compiled knowledge artifacts.

## Trigger

Use when stable knowledge should be reused instead of reinterpreted from raw
sources on every query.

Example commands:

- `compile-knowledge`
- `compile this topic`
- `compile these notes`

## Inputs

- source note paths
- topic or domain
- target audience or agent
- expected reuse case

## Procedure

1. **Scope**
   - Define topic boundary.
   - List source notes.
   - Decide artifact type.
2. **Extract**
   - Extract reusable claims, definitions, constraints, examples, and decisions.
   - Preserve citations or source paths for each major claim.
3. **Normalize**
   - Remove duplicate claims.
   - Resolve terminology drift.
   - Mark conflicts and uncertainty.
4. **Compile**
   - Write a typed artifact using `Compiled_Knowledge_Artifact_Template.md`.
   - Add retrieval hints and related notes.
5. **Review**
   - Check source coverage, faithfulness, and missing assumptions.
6. **Save**
   - Save only after user confirmation.
   - Update any index file if the vault uses one.

## Artifact Types

- `concept-brief`
- `decision-guide`
- `playbook`
- `comparison-matrix`
- `agent-context`
- `retrieval-index`

## Output Rules

- Compiled artifacts must be self-contained.
- Every major claim should point to a source note or URL.
- Keep raw excerpts short; prefer paraphrase and structure.
- Include `## Retrieval Hints` for future agents.
- Include `## Open Questions` when source coverage is incomplete.
