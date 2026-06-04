---
description: Research a question across the wiki and file the answer back
allowed-tools: Read, Write, Edit, Glob, Grep
---

# Wiki Query

Read `CLAUDE.md` for conventions, then run the QUERY cycle for: **$ARGUMENTS**

1. Read `wiki/index.md` to see what's available.
2. Read the relevant wiki pages (load only what you need).
3. Synthesise an answer with `[[wikilink]]` citations to specific wiki pages. If the wiki
   lacks the material to answer, say so and suggest what source to add to `raw/`.
4. Save the answer to `wiki/outputs/{question-slug}.md` with full frontmatter.
5. Update `wiki/index.md` and append to `wiki/log.md`.
