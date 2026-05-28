---
note_type: raw-note
tags: [example, knowledge-base]
source: example
---

# Long Context Notes

Long-context models are often enough when the source corpus is small. If the
total material fits comfortably inside the context window, retrieval adds
unnecessary moving parts.

Useful when:

- the corpus is under roughly 100k tokens
- freshness is less important than simplicity
- the user can provide the whole source set at query time
- citations can be handled by section labels or file names

Limits:

- repeated prompts get expensive
- the model reinterprets raw text each time
- there is no durable compiled knowledge layer
- not ideal for many agents sharing knowledge over time

Source idea: prefer the simplest architecture that satisfies the corpus size and
reuse requirements.
