# LLM Knowledge Base — Schema

## Overview
Personal knowledge base on **[YOUR TOPIC HERE — e.g. "returns & reverse logistics" or
"AI agents for support teams"]**. Raw sources live in `raw/`. The compiled wiki lives in
`wiki/`. You (the AI) maintain all wiki content. I direct strategy; you execute compilation,
maintenance, and queries. I rarely hand-edit the wiki — that's your job.

See [`wiki/_operator.md`](wiki/_operator.md) for who I am and how I work.

## Directory structure
- `raw/` — source material. **Read-only for you**; I add files here.
- `wiki/index.md` — master index linking every page with a one-line summary.
- `wiki/log.md` — append-only changelog of all operations.
- `wiki/_operator.md` — context about me (hand-authored; read it, don't edit it).
- `wiki/concepts/` — one article per concept.
- `wiki/entities/` — people, organisations, tools (one per file).
- `wiki/sources/` — one summary per raw source.
- `wiki/syntheses/` — cross-cutting analysis articles.
- `wiki/outputs/` — filed answers to my queries.

## File conventions
- Filenames: **kebab-case**, lowercase (`active-inference.md`).
- Source summaries: `{author}-{year}-{short-title}.md`.
- Every page MUST start with YAML frontmatter:
  ```
  ---
  title: "Page Title"
  date_created: YYYY-MM-DD
  date_modified: YYYY-MM-DD
  summary: "One or two sentences describing this page."
  tags: [topic-tag]
  type: concept | entity | source | synthesis | output
  status: draft | review | final
  ---
  ```
- Use `[[wikilinks]]` for internal cross-references; link the first occurrence per section.
- Bold key terms on first use.
- **Only make connections explicitly supported by the source material.**

## Operations

### INGEST (I added raw sources)
1. Read the new file(s) in `raw/`.
2. Create a source summary in `wiki/sources/`.
3. Identify concepts + entities; create pages if missing (stub if single-mention).
4. Update existing pages by **appending — don't rewrite**.
5. Add `[[wikilinks]]` connecting new content to existing pages.
6. Update `wiki/index.md` and append to `wiki/log.md`.

### QUERY (I asked a question)
1. Read `wiki/index.md`, then the relevant pages.
2. Synthesise a cited answer (`[[wikilink]]` citations).
3. Save it to `wiki/outputs/{question-slug}.md`.
4. Update `wiki/index.md` and `wiki/log.md`.

### LINT (periodic health check)
1. Find contradictions, orphan pages, and broken `[[wikilinks]]`.
2. Find missing frontmatter fields and fix them.
3. Flag stale content (source >6 months old, no updates).
4. Create stubs for frequently-linked but missing concepts.
5. Write a report to `wiki/outputs/lint-report-{date}.md`; fix what you can automatically.

## Page creation threshold
- Full page when a subject appears in **2+ sources**.
- Stub (frontmatter + one-line definition + link to the source) for single mentions.
- Never leave a `[[wikilink]]` pointing to nothing.

## Quality standards
- Summaries 200–500 words; **synthesise, don't copy**.
- Concept articles 500–1500 words with a clear lead section.
- Trace claims to specific source pages.
- Flag contradictions with ⚠️, noting both positions; prefer recency when sources conflict.
