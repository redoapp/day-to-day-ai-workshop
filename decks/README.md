# decks/ — presentations you build (deliverables)

One file per deck. Each is a deliverable **you own** — the AI drafts and revises it **when you
ask**, but it sits outside `raw/` and `wiki/`, so the ingest/query/lint cycles never rewrite it.
The knowledge base **feeds** your decks (e.g. *"draft slides from `wiki/syntheses/…` and
`wiki/concepts/…`"*); the deck itself lives here.

## Format
Plain markdown with `---` between slides and `#` for slide titles. Present it with Obsidian's
**Slides** plugin (`Cmd/Ctrl+P → "Slides: Start presentation"`) — works from any folder. For
themes, fragments, and PDF export, install the **Advanced Slides** community plugin.

## Make a deck
*"Draft a deck in `decks/<name>.md` from [these wiki pages] — `---`-separated slides, `#` titles,
one idea per slide. Then iterate with me."*

## What's here
- [`workshop-overview.md`](workshop-overview.md) — a starter deck stub to copy.
