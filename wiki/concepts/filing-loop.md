---
title: "Filing Loop"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "The habit of saving every AI answer back into the wiki, so each query enriches the base for future queries — the compounding mechanism of an LLM knowledge base."
tags: [llm, knowledge-management]
type: concept
status: final
related:
  - "[[llm-knowledge-base]]"
  - "[[ingest-query-lint]]"
source_count: 2
confidence: established
---

# Filing Loop

The **filing loop** is the discipline of **saving every answer back into the wiki**. When you
ask the base a question, the synthesised, cited answer is written to `wiki/outputs/` rather than
left in a chat thread — so the next question can build on it. [[hoeem-2026-llm-knowledge-base-course]]

This is what makes a [[llm-knowledge-base]] *compound*. Ordinary chat is "a search engine with
amnesia": ask, answer, close the tab, start over tomorrow. The filing loop turns each
interaction into durable, reusable context, so the base "gets smarter every time you touch it."
It is the payoff half of the [[ingest-query-lint]] cycles.

## Why it works
- Answers accumulate instead of evaporating.
- Later queries retrieve and synthesise across earlier answers.
- The base becomes a record of your *thinking*, not just your sources.

## Sources
- [[hoeem-2026-llm-knowledge-base-course]] · [[karpathy-2026-llm-knowledge-bases]]
