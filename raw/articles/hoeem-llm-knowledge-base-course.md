---
title: "How to create your own LLM knowledge bases today (full course)"
source: "https://x.com/hooeem/status/2041196025906418094"
author: "hoeem (@hooeem)"
clipped: 2026-06-04
tags:
  - raw
type: article
status: raw
---

# How to create your own LLM knowledge bases today (full course) — hoeem

A step-by-step write-up expanding Andrej Karpathy's LLM-knowledge-base idea into a working
system, offered in three versions: complete beginner, "the full system" (comfortable with AI
tools), and builder/developer (with automation).

## Why it matters
> Most people use AI like a search engine with amnesia. You ask a question, get an answer, close
> the tab. Tomorrow you start from scratch. Nothing accumulates. Karpathy's system flips this.

The loop:
1. You collect raw material (articles, papers, transcripts, PDFs) on a topic you care about.
2. The AI reads everything and writes a structured wiki (summaries, concept explanations,
   connections, a master index).
3. You ask questions against the wiki; it gives cited, synthesised answers.
4. Every answer gets filed back into the wiki, so the next question benefits from prior work.
5. The AI periodically health-checks the wiki for contradictions, gaps, and stale info.

> The result? A personal knowledge base that gets smarter every time you touch it — synthesised,
> not just indexed.

## The full system
- **Three-layer design.** Layer 1 `raw/` (read-only source of truth). Layer 2 `wiki/`
  (AI-generated and AI-maintained). Layer 3 `CLAUDE.md` (the schema/config controlling the AI).
- **Four operational cycles.** Ingest, Compile, Query, Lint — repeating and compounding.
- **Folder structure** under `wiki/`: `index.md`, `log.md`, `concepts/`, `entities/`,
  `sources/`, `syntheses/`, `outputs/`, `attachments/`.
- **Conventions.** kebab-case filenames; source summaries `{author}-{year}-{short-title}.md`;
  YAML frontmatter on every page; `[[wikilinks]]` for cross-references.

## Tools mentioned
- **Obsidian** — the markdown app you read the vault in (Graph View, plugins).
- **Claude Code** — CLI with filesystem access; reads/writes the wiki directly and auto-loads `CLAUDE.md`.
- **Obsidian Web Clipper** — one-click save of web pages into `raw/articles/`.
- **MarkItDown** (Microsoft) — converts PDFs/docs to markdown (`markitdown file.pdf > out.md`).
- **Dataview** (Obsidian plugin) — treats the vault as a queryable database via YAML frontmatter.
- **Obsidian Git, Templater, Linter, Tag Wrangler, Marp, Homepage** — supporting plugins.
- **QMD** (Tobi Lütke) — local search engine for markdown (keyword + semantic + rerank).

## Quality notes
- **The AI is a compiler, not a search engine** — it synthesises and connects, beyond retrieval.
- **Two-model validation** for high-stakes bases: one model writes, a second validates, to curb
  hallucinated connections.
- **Plain text is forever** — portable markdown, no vendor lock-in.

*(Second seed source. Captured from the linked X article; trimmed to the substantive content.)*
