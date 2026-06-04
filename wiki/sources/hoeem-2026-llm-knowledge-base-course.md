---
title: "hoeem — How to Create Your Own LLM Knowledge Bases (full course)"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "A step-by-step course expanding Karpathy's idea into a working three-layer system with four operational cycles, conventions, and a tool stack centred on Obsidian and Claude Code."
tags: [llm, knowledge-management, tutorial]
type: source
status: final
source_url: "https://x.com/hooeem/status/2041196025906418094"
authors:
  - "hoeem"
---

# hoeem — How to Create Your Own LLM Knowledge Bases (full course)

**Summary.** [[hoeem]] turns the [[llm-knowledge-base]] idea from [[andrej-karpathy]] into a
concrete, buildable system. The framing is that most AI use is "a search engine with amnesia" —
nothing accumulates — whereas this system **compounds** via a [[filing-loop]]: collect raw
sources, have the AI compile a structured wiki, ask questions that get cited synthesised answers,
and **file every answer back** so the base gets smarter each time. It formalises the
[[three-layer-architecture]] (`raw/` → `wiki/` → schema), the four cycles in
[[ingest-query-lint]], and a stack built on [[obsidian]] + [[claude-code]], with [[dataview]] for
querying the vault, [[obsidian-web-clipper]] and [[markitdown]] for collection, and a
[[two-model-validation]] pattern for high-stakes bases. It stresses that **the AI is a compiler,
not a search engine** ([[ai-as-compiler]]) and that plain-text markdown means no lock-in.

## Key points
- Five-step loop: collect → compile → query → **file back** → health-check.
- Three layers and four cycles, with strict file/frontmatter conventions.
- Tooling: Obsidian, Claude Code, Web Clipper, MarkItDown, Dataview, QMD.
- Guardrail: two-model validation to curb hallucinated connections.

## Concepts
- [[filing-loop]] · [[three-layer-architecture]] · [[ingest-query-lint]] · [[ai-as-compiler]] · [[two-model-validation]]

## Entities
- [[hoeem]] · [[obsidian]] · [[claude-code]] · [[dataview]] · [[obsidian-web-clipper]] · [[markitdown]]
