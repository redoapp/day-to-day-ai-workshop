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

## First time? Run `/wiki-start`

Run `claude` in this directory and type **`/wiki-start`**. It asks you a few quick
multiple-choice questions — your topic, your role, how you like to work — then points the schema
at your topic, fills in your operator note, clears the example seed, helps you add your first
sources, and runs the first compile. The whole setup in one guided, click-through pass. The rest
of this doc is what `/wiki-start` automates, for when you want to do it by hand.

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

There's a fully-worked example seeded in the repo (topic: *LLM knowledge bases*): **2 raw
sources** compiled into **6 concepts, 7 entities, a synthesis, and a filed query answer**, all
cross-linked and listed in [`wiki/index.md`](wiki/index.md). Open it in Obsidian and:

- press `Cmd/Ctrl+G` for **Graph View** — you'll see a connected network, colour-coded by type
  (concepts / entities / sources / syntheses / outputs), not a lonely star;
- open [`wiki/dashboard.md`](wiki/dashboard.md) for **live Dataview tables** of the whole base;
- read [`wiki/outputs/how-is-this-different-from-rag-or-normal-chat.md`](wiki/outputs/how-is-this-different-from-rag-or-normal-chat.md)
  to see a **filed, cited answer** — the [filing loop](wiki/concepts/filing-loop.md) in action.

Then run `/wiki-start` to clear the example and point the base at *your* topic.

## Make Obsidian shine (recommended plugins)

The repo ships a curated `.obsidian/` (dark theme + a colour-coded graph), but the richest
features are community plugins — install via **Settings → Community plugins → Browse**.

### ⭐ Recommended: turn this on first — Obsidian Git
This vault is already a GitHub repo, and the AI rewrites your files (regenerates the index,
appends to pages, reshuffles links). **Obsidian Git** gives you a no-terminal commit + one-click
undo over every change — your safety net when an edit goes wrong. After installing, set:
- **Auto-commit-and-sync** every `10` minutes (also enable *commit-and-sync on save* if you like).
- **Pull on startup** — so you always open the latest.

Then any bad AI edit is one "restore previous version" away, and your work is continuously backed
up to GitHub without touching a terminal.

### Also worth it
- **Dataview** — powers [`wiki/dashboard.md`](wiki/dashboard.md); turns frontmatter into live tables.
- **Homepage** — set `wiki/dashboard.md` to open on launch.
- **Smart Connections** — surfaces semantically *related* notes (and chat-with-your-notes); runs a
  local embedding model so nothing leaves your machine. Pays off as the vault grows. Add its index
  folder (`.smart-env/`) to `.gitignore`.
- **Templater** — apply the note templates in [`templates/`](templates/) automatically.
- **Linter** — keep frontmatter and formatting consistent as the AI writes many files.

(Everything except Git is optional — the wiki is plain markdown and works without any of them.)

## Going further (optional, beyond this workshop)

The full write-up covers automation if you want it: a daily `/loop` or `/schedule` to compile
overnight, a GitHub Action to compile in the cloud with your computer off, and a ready-made
`wiki-skills` plugin (`/plugin marketplace add kfchou/wiki-skills`). Start manual; layer
automation on once the loop feels natural.
