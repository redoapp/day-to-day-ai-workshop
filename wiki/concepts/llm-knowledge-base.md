---
title: "LLM Knowledge Base"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "A personal markdown wiki that an LLM compiles from raw sources and maintains over time, turning scattered material into synthesised, interlinked knowledge."
tags: [llm, knowledge-management]
type: concept
status: final
related:
  - "[[andrej-karpathy]]"
source_count: 2
confidence: emerging
---

# LLM Knowledge Base

An **LLM knowledge base** is a personal wiki of plain-markdown notes that an LLM **compiles
from raw sources and maintains over time** — an "external brain" you read while the model does
the writing. It was popularised by [[andrej-karpathy]]. [[karpathy-2026-llm-knowledge-bases]]

## How it differs from normal AI use
Ordinary chat is a "search engine with amnesia": ask, answer, close the tab, start over.
A knowledge base adds a **filing loop** — every answer is saved back into the wiki, so each
interaction compounds rather than evaporating. The LLM acts as a **compiler** (synthesising
and connecting ideas) rather than a retriever (returning similar chunks).

## The shape
- **Raw layer** — immutable source material the model reads but never edits.
- **Compiled layer** — summaries, concept pages, entities, and filed query outputs the model
  writes and maintains.
- **Schema** — a config doc telling the model how the wiki is structured and what operations
  (ingest, query, lint) exist.

## Why markdown
Plain text is portable and inspectable: readable by any tool, on any OS, with no vendor
lock-in. Tools like Obsidian render the `[[wikilinks]]` as a navigable graph.

## Related
- Built on the [[three-layer-architecture]] and the [[ingest-query-lint]] cycles.
- Compounds through the [[filing-loop]]; the AI works as [[ai-as-compiler]], not a search engine.

## Sources
- [[karpathy-2026-llm-knowledge-bases]] · [[hoeem-2026-llm-knowledge-base-course]]
