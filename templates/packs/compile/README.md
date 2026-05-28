# Compile Pack

Adds workflows for turning raw or scattered notes into LLM-ready knowledge
artifacts.

Install after Core. It pairs well with Research Pack, but it can also compile
existing vault notes without new web research.

## Includes

- `compile-knowledge`
- `synthesize`
- compiled artifact template
- synthesis digest template

## Principle

Do not make the LLM reinterpret raw documents on every query. Stable knowledge
should be compiled once with type, scope, citations, and retrieval hints.

## When To Use

Use this pack when:

- the same knowledge will be reused across tasks
- source notes are too long or inconsistent for direct retrieval
- multiple notes need to become one decision-ready artifact
- you want progressive disclosure: index first, details second
