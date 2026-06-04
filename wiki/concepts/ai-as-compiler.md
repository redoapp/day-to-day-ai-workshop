---
title: "AI as Compiler (not Search Engine)"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "The idea that an LLM building a knowledge base synthesises and connects ideas across sources, rather than retrieving similar chunks the way search or RAG does."
tags: [llm, knowledge-management]
type: concept
status: final
related:
  - "[[llm-knowledge-base]]"
  - "[[two-model-validation]]"
source_count: 2
confidence: emerging
---

# AI as Compiler (not Search Engine)

A defining claim of the [[llm-knowledge-base]] approach: the AI acts as a **compiler**, not a
search engine. It reads the full [[three-layer-architecture]]'s raw layer and *synthesises* —
writing concept articles, drawing connections, reconciling sources — rather than returning the
nearest-matching chunks. [[hoeem-2026-llm-knowledge-base-course]]

This is why the result "no Google search could replicate": it has been **synthesised, not just
indexed**. [[andrej-karpathy]] frames the same shift as spending tokens "manipulating knowledge"
rather than retrieving it. [[karpathy-2026-llm-knowledge-bases]]

The tradeoff is that synthesis can invent connections the sources don't support — addressed by
keeping the raw layer immutable and by [[two-model-validation]].

## Sources
- [[hoeem-2026-llm-knowledge-base-course]] · [[karpathy-2026-llm-knowledge-bases]]
