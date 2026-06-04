---
title: "What Makes a Knowledge Base Compound"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "A cross-cutting look at why an LLM knowledge base gets more valuable over time, drawing the filing loop, synthesis, and the three-layer design into one picture."
tags: [llm, knowledge-management, synthesis]
type: synthesis
status: final
source_count: 2
---

# What Makes a Knowledge Base Compound

Three ideas from the sources combine to explain why an [[llm-knowledge-base]] *appreciates*
instead of decaying like a chat history.

**1. Inputs are immutable; outputs are regenerable.** The [[three-layer-architecture]] keeps
`raw/` read-only, so the AI can rewrite and reconnect the `wiki/` layer freely without ever
losing or corrupting the originals. Growth is safe.

**2. The AI synthesises rather than retrieves.** Because the AI works as
[[ai-as-compiler]], each new source isn't just stored — it's woven into existing concept and
entity pages with new links. The graph of ideas densifies with every ingest. The guardrail
against over-connecting is [[two-model-validation]].

**3. Answers are saved, not spent.** The [[filing-loop]] writes every query result back into
`wiki/outputs/`, so reasoning accumulates the way sources do. The next question stands on all the
previous ones.

Put together: collection compounds (sources), synthesis compounds (links), and reasoning
compounds (filed answers) — three reinforcing loops, all run by the [[ingest-query-lint]] cycles.
That's the difference between a folder of notes and an "external brain that gets smarter every
time you touch it."

## Sources
- [[karpathy-2026-llm-knowledge-bases]] · [[hoeem-2026-llm-knowledge-base-course]]
