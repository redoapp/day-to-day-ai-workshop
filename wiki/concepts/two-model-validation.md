---
title: "Two-Model Validation"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "A guardrail for high-stakes knowledge bases: one model writes wiki pages and a second, different model independently validates them before they go live."
tags: [llm, knowledge-management, quality]
type: concept
status: final
related:
  - "[[ai-as-compiler]]"
source_count: 1
confidence: emerging
---

# Two-Model Validation

For high-stakes bases (medical, legal, investment), use **two different models**: one writes the
wiki pages, a second independently validates them before they enter the "live" wiki. If both
agree, the content is likely sound; if they disagree, investigate. [[hoeem-2026-llm-knowledge-base-course]]

It exists to curb the main failure mode of [[ai-as-compiler]] — **hallucinated connections**
between unrelated ideas. Combined with an immutable raw layer (see [[three-layer-architecture]]),
it keeps the [[llm-knowledge-base]] trustworthy as it scales.

## Sources
- [[hoeem-2026-llm-knowledge-base-course]]
