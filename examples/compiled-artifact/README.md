# Compiled Artifact Example

This example shows how Compile Pack turns scattered raw notes into one
LLM-ready decision guide.

## Structure

```txt
raw-notes/
  01-long-context.md
  02-rag.md
  03-llm-wiki.md
compiled/
  knowledge-base-decision-guide.md
```

## Prompt

```txt
compile-knowledge raw-notes/ into a decision-guide artifact for a small team
choosing a knowledge base architecture.
```

## What To Notice

The compiled artifact:

- preserves source links back to raw notes
- removes duplicate claims
- turns rough notes into decision rules
- adds retrieval hints for future agents
- records open questions instead of hiding uncertainty
