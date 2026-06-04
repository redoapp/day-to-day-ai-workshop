---
title: "Ingest / Query / Lint Cycles"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "The repeating operational cycles that build and maintain an LLM knowledge base: ingest sources, compile them, query the wiki, and lint for health."
tags: [llm, knowledge-management, workflow]
type: concept
status: final
related:
  - "[[three-layer-architecture]]"
  - "[[filing-loop]]"
source_count: 1
confidence: established
---

# Ingest / Query / Lint Cycles

The four operational cycles that compound a [[llm-knowledge-base]] over time. In this repo each
maps to a slash command. [[hoeem-2026-llm-knowledge-base-course]]

- **Ingest / Compile** — you add raw sources; the AI writes summaries, concept and entity pages,
  cross-links them, and updates the index. (`/wiki-ingest`)
- **Query** — you ask a question; the AI researches across the wiki and produces a cited answer,
  then files it back via the [[filing-loop]]. (`/wiki-query`)
- **Lint** — the AI health-checks for contradictions, orphan pages, broken links, and stale
  content, fixing what it can. (`/wiki-lint`)

These run against the [[three-layer-architecture]], with onboarding handled once by `/wiki-start`.

## Sources
- [[hoeem-2026-llm-knowledge-base-course]]
