---
title: "Claude Code"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "Anthropic's command-line agent with filesystem access; reads and writes the wiki directly and auto-loads CLAUDE.md, enabling the knowledge-base cycles without copy-paste."
tags: [tool]
type: entity
status: final
related:
  - "[[ingest-query-lint]]"
  - "[[obsidian]]"
source_count: 1
---

# Claude Code

Anthropic's CLI agent with full filesystem access. Run in the vault, it auto-loads the
`CLAUDE.md` schema and can create and edit wiki pages directly — so the [[ingest-query-lint]]
cycles run from a single prompt instead of a copy-paste loop. It's the engine behind this repo's
`/wiki-*` commands. [[hoeem-2026-llm-knowledge-base-course]]

## Sources
- [[hoeem-2026-llm-knowledge-base-course]]
