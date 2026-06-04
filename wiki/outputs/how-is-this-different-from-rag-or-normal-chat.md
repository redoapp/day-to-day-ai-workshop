---
title: "How is this different from RAG or normal chat?"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "Filed answer: an LLM knowledge base differs from chat (no memory) and from RAG (retrieval) by synthesising sources into maintained pages and filing answers back so the base compounds."
tags: [llm, knowledge-management, query]
type: output
status: final
source_count: 2
---

# Query: How is this different from RAG or normal chat?

*Filed answer — an example of the [[filing-loop]] in action.*

**Short answer.** Normal chat has no memory; RAG has retrieval but no accumulation; an
[[llm-knowledge-base]] adds **synthesis** and a **filing loop**, so it compounds.

**vs. normal chat.** Chat is "a search engine with amnesia" — you ask, you answer, you close the
tab, and nothing accumulates. [[hoeem-2026-llm-knowledge-base-course]] A knowledge base persists
its work as durable markdown the AI maintains.

**vs. RAG / search.** Retrieval returns the chunks most *similar* to your query. A knowledge base
treats the AI as [[ai-as-compiler]]: it reads sources and *writes* synthesised concept pages and
cross-links, producing something "synthesised, not just indexed." It understands relationships
between documents, not only their similarity. [[karpathy-2026-llm-knowledge-bases]]

**The compounding part.** Every answer is saved back via the [[filing-loop]] into
`wiki/outputs/` (like this page), so future questions build on past ones — see
[[what-makes-a-knowledge-base-compound]]. RAG over a static corpus doesn't get smarter as you use
it; this does.

**Caveat.** Synthesis can hallucinate connections; the immutable `raw/` layer and
[[two-model-validation]] are the checks.

## Sources
- [[karpathy-2026-llm-knowledge-bases]] · [[hoeem-2026-llm-knowledge-base-course]]
