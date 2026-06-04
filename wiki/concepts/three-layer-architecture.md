---
title: "Three-Layer Architecture"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "The structural design of an LLM knowledge base: raw sources, an AI-maintained wiki, and a schema file that governs the AI's behaviour."
tags: [llm, knowledge-management, architecture]
type: concept
status: final
related:
  - "[[llm-knowledge-base]]"
  - "[[ingest-query-lint]]"
source_count: 1
confidence: established
---

# Three-Layer Architecture

An [[llm-knowledge-base]] separates into three layers, each with a different owner.
[[hoeem-2026-llm-knowledge-base-course]]

1. **Raw sources** (`raw/`) — the single source of truth. The AI **reads** but never edits it,
   which keeps every claim checkable against the original.
2. **Compiled wiki** (`wiki/`) — AI-generated and AI-maintained: summaries, concept and entity
   pages, syntheses, indexes, and filed query outputs. You rarely hand-edit it.
3. **The schema** (`CLAUDE.md`) — a config that tells the AI how the wiki is structured, what
   conventions to follow, and what operations exist. The "job description" for the AI librarian.

The separation is what lets the [[ingest-query-lint]] cycles run safely: immutable inputs,
regenerable outputs, and an explicit contract in between. Read in [[obsidian]].

## Sources
- [[hoeem-2026-llm-knowledge-base-course]]
