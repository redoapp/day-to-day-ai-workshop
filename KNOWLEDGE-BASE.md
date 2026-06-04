# Your LLM Knowledge Base

> Most people use AI like a search engine with amnesia: ask, answer, close the tab, start
> over tomorrow. This flips it. You collect raw material; the AI compiles it into a wiki that
> gets **smarter every time you touch it**. It's been *synthesised*, not just indexed.

Based on Andrej Karpathy's "LLM knowledge bases" idea and the community write-up of the full
system. This repo *is* the vault — open it in [Obsidian](https://obsidian.md/) to browse.

## The three layers

| Layer | Folder | Who owns it |
|---|---|---|
| **1. Raw sources** | [`raw/`](raw/) | You. The single source of truth. The AI reads it, never edits it. |
| **2. Compiled wiki** | [`wiki/`](wiki/) | The AI. Summaries, concepts, entities, syntheses, query outputs. You rarely hand-edit. |
| **3. The schema** | [`CLAUDE.md`](CLAUDE.md) | The config that tells the AI how the wiki is structured and what operations exist. |

## The four cycles (they repeat and compound)

```
  INGEST  →  you drop sources in raw/; AI writes summaries, concept & entity pages, links
  COMPILE →  AI weaves new info into existing pages and updates the index
  QUERY   →  you ask; AI researches across the wiki, answers with citations, FILES IT BACK
  LINT    →  AI health-checks for contradictions, gaps, broken links, stale content
```

The **filing loop is the superpower**: every answer is saved back into `wiki/outputs/`, so the
next question benefits from all previous work.

## Daily use (Claude Code in this folder)

Run `claude` in this directory — it auto-loads `CLAUDE.md`. Then:

| You want to… | Do this |
|---|---|
| Add knowledge | Drop a file in `raw/articles/`, then run `/wiki-ingest` (or just say *"ingest the new files in raw/"*). |
| Ask a question | `/wiki-query How does X relate to Y?` — the answer gets filed into `wiki/outputs/`. |
| Health-check | `/wiki-lint` — finds contradictions, orphans, broken links, gaps; fixes what it can. |

No terminal? The same prompts work in Claude Chat — create a Project, paste `CLAUDE.md` into
the project instructions, upload your `raw/` and `wiki/` files, and copy outputs back by hand.

## Collecting sources fast

- **Obsidian Web Clipper** (browser extension) → save any page straight into `raw/articles/`.
- **PDFs / docs** → `pip install markitdown` then `markitdown file.pdf > raw/papers/name.md`
  (or just paste the text into a new note — the AI only needs the text).

## See it work

There's a seeded example: one raw source ([`raw/articles/karpathy-llm-knowledge-bases.md`](raw/articles/karpathy-llm-knowledge-bases.md))
already compiled into a [source summary](wiki/sources/), a [concept page](wiki/concepts/), and an
[entity page](wiki/entities/), all wired into [`wiki/index.md`](wiki/index.md). Open Obsidian's
**Graph View** to see them connected. Then point `CLAUDE.md`'s Overview line at *your* topic,
clear the example, drop in 3–5 sources, and run `/wiki-ingest`.

## Going further (optional, beyond this workshop)

The full write-up covers automation if you want it: a daily `/loop` or `/schedule` to compile
overnight, a GitHub Action to compile in the cloud with your computer off, and a ready-made
`wiki-skills` plugin (`/plugin marketplace add kfchou/wiki-skills`). Start manual; layer
automation on once the loop feels natural.
