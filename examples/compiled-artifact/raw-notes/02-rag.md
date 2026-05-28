---
note_type: raw-note
tags: [example, knowledge-base, rag]
source: example
---

# RAG Notes

Retrieval-Augmented Generation is useful when the corpus is too large for a
single prompt or changes frequently.

Good fit:

- frequently updated documents
- large document collections
- search-first workflows
- cases where query-time freshness matters

Risks:

- poor chunk quality lowers answer quality
- vector search alone can miss exact terms
- the LLM may need to reconstruct context from fragments
- evaluation is required; subjective "it feels better" is not enough

Practical pattern:

- use hybrid search when exact terms matter
- keep chunks self-contained
- measure retrieval with a small golden set
