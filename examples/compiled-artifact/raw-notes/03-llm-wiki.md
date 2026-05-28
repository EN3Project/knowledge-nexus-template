---
note_type: raw-note
tags: [example, knowledge-base, llm-wiki]
source: example
---

# LLM Wiki Notes

An LLM Wiki compiles stable knowledge into structured pages when sources are
added. Query-time work becomes lighter because the agent can retrieve a
pre-structured page instead of raw source fragments.

Good fit:

- stable knowledge
- repeated questions
- small teams or individual operators
- agent workflows that need reusable context

Limits:

- high-frequency source streams can make ingest expensive
- page updates need linting and review
- contradictions can accumulate without maintenance

Useful fields:

- summary
- scope
- source links
- decision rules
- retrieval hints
- open questions

Design principle: compile once, retrieve progressively.
