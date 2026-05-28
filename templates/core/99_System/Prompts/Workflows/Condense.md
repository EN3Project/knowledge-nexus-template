# Workflow: Condense

## Objective

Compress the current conversation into a reusable context summary.

## Output Format

```md
# Condensed Context

## Purpose

## Current State

## Decisions

## Constraints

## Open Issues

## Next Actions

## References

## audit_trail

## decision_rationale

## open_questions

## Excluded Context
```

## Rules

- Keep the section order fixed.
- Write `None` when a section has no content.
- Exclude raw search dumps, rejected options, jokes, and irrelevant detail.
- If long-term memory should be saved, recommend `crystallize`.
