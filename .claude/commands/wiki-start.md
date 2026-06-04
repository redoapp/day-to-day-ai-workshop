---
description: First-run onboarding — set up this knowledge base for a new person and topic
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Wiki Start (onboarding)

You are onboarding someone who just forked this template. Goal: in ~10 minutes, turn the
generic starter into *their* knowledge base, seeded with their first real sources. Be warm,
concise, and **interactive** — ask, wait for answers, don't do everything in one shot. First
read `CLAUDE.md` and `KNOWLEDGE-BASE.md` so you can explain the system in a sentence if asked.

Work through these steps in order. Confirm before any deletion.

## 1. Pick the topic
Ask: **"What's one topic you keep researching or want to accumulate knowledge on?"** Give a few
examples (a work area, a market, a domain you study). Keep them to ONE topic for now.

## 2. Quick operator interview
Ask 3–4 short questions to fill [`wiki/_operator.md`](../../wiki/_operator.md): their role, how
they like to work, what "good work" looks like to them, and their current focus. Then write
`wiki/_operator.md` from their answers (replace the italic prompts). Keep it tight.

## 3. Point the schema at their topic
Edit the **Overview** line of `CLAUDE.md` so `[YOUR TOPIC HERE …]` becomes their actual topic.
Leave the rest of the schema as-is.

## 4. Clear the example seed
Explain that the repo ships with a worked example (the Karpathy source + its compiled pages) so
the graph isn't empty, and you'll now clear it to make room for theirs. **Ask permission**, then:
- Delete `raw/articles/karpathy-llm-knowledge-bases.md`
- Delete `wiki/sources/karpathy-2026-llm-knowledge-bases.md`, `wiki/concepts/llm-knowledge-base.md`,
  `wiki/entities/andrej-karpathy.md`
- Reset `wiki/index.md` to an empty index (their topic in the Overview, zero articles) and
  `wiki/log.md` to just the `# Wiki Log` header
- Reset each `wiki/*/_index.md` to its heading with no entries
(If they'd rather keep the example as a reference, skip this and move it to `raw/articles/` instead.)

## 5. Collect the first sources (hand off to them)
Tell them to add **3–5 sources** on their topic to `raw/articles/`, and how:
- Paste article text into a new `.md` file (put `source: <url>` at the top), or
- Use the Obsidian Web Clipper (one click → `raw/articles/`), or
- For a PDF: `markitdown file.pdf > raw/papers/name.md`
Then **stop and wait** — ask them to tell you when the files are in. Don't fabricate sources.

## 6. First compile
Once sources are in, run the INGEST cycle (the same steps as `/wiki-ingest`): read `CLAUDE.md`,
process each new file in `raw/`, create source summaries + concept/entity pages with
`[[wikilinks]]`, and update `wiki/index.md` and `wiki/log.md`. Report what you created.

## 7. First query + handoff
Suggest one real question and offer to run it (the `/wiki-query` cycle), filing the answer into
`wiki/outputs/`. Then hand off: tell them to open the folder in **Obsidian** and press
`Cmd/Ctrl+G` for Graph View, and remind them of the daily loop — drop sources in `raw/`,
`/wiki-ingest`, `/wiki-query`, and `/wiki-lint` weekly.
