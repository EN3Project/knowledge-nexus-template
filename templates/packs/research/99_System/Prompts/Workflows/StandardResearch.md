# Workflow: StandardResearch

## Objective

Collect, verify, synthesize, and optionally save source-backed knowledge.

## Trigger Conditions

### Claude / Gemini

Broad research instructions can be treated as workflow candidates:

- "research this"
- "investigate"
- "tell me about..."
- "compare..."

### Codex

Subagent dispatch should require explicit workflow intent:

- `StandardResearch`
- `research workflow`
- `investigation workflow`

Codex can still answer normal research questions directly when no workflow is
explicitly requested.

## Phases

| Phase | Agent | Role |
|---|---|---|
| 1 | `@librarian` | Search existing vault knowledge |
| 2 | `@investigator` | Collect external sources |
| 3 | `@analyst` | Synthesize structure and insights |
| 4 | `@critic` | Review logic and source quality |
| 5 | `@scribe` | Format and save output |

## Output Requirements

- Include source URLs for external claims.
- Mark uncertain claims clearly.
- Save only after the user confirms the destination.
- Include a `## Supporting Sources` section in saved notes.
