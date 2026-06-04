---
description: Health-check the wiki and fix what can be fixed automatically
allowed-tools: Read, Write, Edit, Glob, Grep
---

# Wiki Lint

Read `CLAUDE.md` for conventions, then run the LINT cycle. Read the files in `wiki/` and report:

1. **CONTRADICTIONS** — claims in one article that conflict with another. List both sources.
2. **ORPHAN PAGES** — articles with no inbound `[[wikilinks]]`. Suggest where to add links.
3. **MISSING PAGES** — concepts frequently referenced as `[[wikilinks]]` but lacking their own
   article. Create stubs for the top 5.
4. **BROKEN LINKS** — `[[wikilinks]]` pointing to non-existent pages.
5. **INCOMPLETE METADATA** — pages missing required frontmatter. Fix them.
6. **STALE CONTENT** — pages whose source is >6 months old with no updates.
7. **SUGGESTED QUESTIONS** — 3–5 research questions worth exploring next.

Fix everything you safely can. For contradictions and major gaps, write a report to
`wiki/outputs/lint-report-{today}.md` and append a line to `wiki/log.md`.
