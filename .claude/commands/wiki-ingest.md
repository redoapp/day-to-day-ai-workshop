---
description: Compile new raw sources into the wiki
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Wiki Ingest

Read `CLAUDE.md` for project conventions, then run the INGEST cycle.

1. Glob `raw/**/*.md` to find all source files.
2. Glob `wiki/sources/**/*.md` to see which sources are already processed.
3. For each NEW (unprocessed) source:
   a. Create a source summary in `wiki/sources/` (`{author}-{year}-{short-title}.md`).
   b. Identify key concepts and entities.
   c. Create concept pages in `wiki/concepts/` and entity pages in `wiki/entities/` if they
      don't exist (stub if a subject appears in only one source).
   d. Update existing pages with new information — **append, don't rewrite**.
   e. Add `[[wikilinks]]` between related pages. Never link to a page you haven't created.
   f. Only assert connections the source material explicitly supports.
4. Update `wiki/index.md` (and the relevant `_index.md` files).
5. Append an entry to `wiki/log.md`.
6. Report: sources processed, pages created, pages updated.
