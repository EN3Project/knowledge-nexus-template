---
note_type: compiled-knowledge
artifact_type: decision-guide
tags: [example, knowledge-base, compiled-artifact]
source: compile-knowledge
updated: 2026-05-29
---

# Knowledge Base Architecture Decision Guide

## Purpose

Help a small team choose between long-context prompting, RAG, and an LLM Wiki
style compiled knowledge base.

## Scope

This guide applies to small teams or individual operators choosing a knowledge
base architecture for LLM-assisted work. It does not cover enterprise
governance, RBAC, PII review, or managed knowledge platforms.

## Compiled Summary

Start with the simplest system that fits the corpus and reuse pattern.

- Use long-context prompting when the corpus is small and one-off.
- Use RAG when the corpus is large or frequently updated.
- Use an LLM Wiki when knowledge is stable, reused often, and should be shared
  across agents.

The key distinction is when knowledge is structured:

| Pattern | Structure Timing | Best For |
|---|---|---|
| Long context | query time | small one-off source sets |
| RAG | query time retrieval | large or changing corpora |
| LLM Wiki | ingest / compile time | stable reusable knowledge |

## Key Claims

| Claim | Source | Confidence |
|---|---|---|
| Long-context prompting is enough when all relevant material fits in context and reuse is low. | `raw-notes/01-long-context.md` | High |
| RAG is better when documents are too large for one prompt or change frequently. | `raw-notes/02-rag.md` | High |
| Chunk quality and evaluation determine RAG usefulness more than vector search alone. | `raw-notes/02-rag.md` | Medium |
| LLM Wiki-style compilation is strongest for stable knowledge and repeated questions. | `raw-notes/03-llm-wiki.md` | High |
| Compile-time structure reduces repeated query-time reinterpretation. | `raw-notes/01-long-context.md`, `raw-notes/03-llm-wiki.md` | High |

## Decision Rules

1. If the corpus fits in the context window and will be used once, use long-context prompting.
2. If documents update frequently, use RAG or hybrid search.
3. If the same knowledge will be reused across sessions or agents, compile it into structured notes or artifacts.
4. If exact terms matter, prefer hybrid retrieval over vector-only search.
5. If the system will be trusted for decisions, create a small golden set before optimizing.

## Examples

| Situation | Recommended Pattern | Reason |
|---|---|---|
| Five design docs for one planning session | Long context | simplest and low overhead |
| Hundreds of support articles updated weekly | RAG | frequent updates and broad search |
| A team's stable operating principles | LLM Wiki / compiled artifacts | repeated reuse and shared agent context |
| Mixed current tickets and stable architecture docs | Hybrid | hot material in RAG, stable knowledge compiled |

## Retrieval Hints

- Use this artifact when choosing a knowledge base architecture.
- Related terms: long context, RAG, LLM Wiki, compiled knowledge, retrieval, golden set.
- If the user asks "Should I use RAG?", retrieve this guide first.
- If the user asks about enterprise governance, this artifact is out of scope.

## Open Questions

- What is the actual corpus size in tokens?
- How often do source documents change?
- Will agents reuse this knowledge across sessions?
- Are citations, access control, or audit logs required?

## Sources

- `raw-notes/01-long-context.md`
- `raw-notes/02-rag.md`
- `raw-notes/03-llm-wiki.md`
