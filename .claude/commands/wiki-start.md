---
description: First-run onboarding — guided, click-through setup of this knowledge base
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Wiki Start (guided onboarding)

You're onboarding someone who just forked this template — likely sitting in a workshop, maybe
non-technical. **Make it feel like clicking through a short form, not an interview.**

> **Use the AskUserQuestion tool for every choice below**, with the option sets given. The user
> picks instead of typing (they can always choose "Other" to write their own). Only fall back to
> free text where the answer is inherently personal — the exact topic name, or pasting source
> text. Keep momentum: ask, confirm in one line, then act.

First, read `CLAUDE.md` and `KNOWLEDGE-BASE.md` so you can answer "what is this?" in one sentence
if they ask. Then welcome them in 1–2 lines and go.

## Step 1 — Topic + about you  (ONE AskUserQuestion call, batch all four)

Ask these four questions together so it reads like a quick form:

1. **header "Topic"** — "What do you want your knowledge base to be about?"
   - "A work domain" — *e.g. returns & reverse logistics, support, sales ops*
   - "A market or competitors" — *an industry or set of companies you track*
   - "Something I'm learning" — *a tool, framework, or skill*
   - "A personal interest" — *health, finance, a hobby*
   *(Most people will pick "Other" and type the real thing — that's the topic. If they pick a
   category, ask one quick free-text follow-up for the specific name.)*

2. **header "Your role"** — "What's your role?"
   - "Sales" · "Support / Success" · "Operations" · "Engineering / Product"
   *(Other = type it.)*

3. **header "Working style"**, `multiSelect: true` — "How should the AI work with you?"
   - "Keep answers concise" · "Ask before big tasks" · "Show a draft first" · "Explain as it goes"

4. **header "Tech level"** — "How technical are you?"
   - "Non-technical — explain simply" · "I can read code" · "I write code"

Then write the results: set the **Overview** line of `CLAUDE.md` to their topic, and fill
[`wiki/_operator.md`](../../wiki/_operator.md) from their role / working style / tech level
(replace the italic prompts). Keep it tight.

## Step 2 — Clear the example?  (AskUserQuestion)

"This repo ships with a worked example (the Karpathy source + its compiled pages) so the graph
isn't empty. Clear it to make room for your topic?"
- "Clear it (Recommended)" — delete `raw/articles/karpathy-llm-knowledge-bases.md`,
  `wiki/sources/karpathy-2026-llm-knowledge-bases.md`, `wiki/concepts/llm-knowledge-base.md`,
  `wiki/entities/andrej-karpathy.md`; reset `wiki/index.md` (their topic, zero articles),
  `wiki/log.md` (just the header), and each `wiki/*/_index.md` to its heading with no entries.
- "Keep it as a reference" — leave everything; their pages will sit alongside it.
- "Decide later" — skip for now.

## Step 3 — Add your first sources  (AskUserQuestion for the HOW, then hand off)

"How do you want to add your first 3–5 sources?"
- "I'll paste article text" — tell them: new file in `raw/articles/`, put `source: <url>` on top.
- "Obsidian Web Clipper" — one click saves a page into `raw/articles/`.
- "I have PDFs" — `markitdown file.pdf > raw/papers/name.md`, or just paste the text.
- "Help me find some" — suggest 3–5 good sources on their topic; with their OK, fetch and save
  each into `raw/articles/`. Never invent sources or fabricate content.

After giving the matching instructions, **stop and wait** — ask them to say "done" once the files
are in `raw/`. (If they chose "Help me find some" and approved, you add the files yourself.)

## Step 4 — First compile

Run the INGEST cycle (same as `/wiki-ingest`): read `CLAUDE.md`, process each new file in `raw/`,
create source summaries + concept/entity pages with `[[wikilinks]]`, update `wiki/index.md` and
`wiki/log.md`. Report what you created in a short list.

## Step 5 — First question + handoff  (AskUserQuestion)

"Want to try your first question against the wiki?"
- "Suggest one and run it" — propose a question based on their sources, then run the QUERY cycle
  (file the answer into `wiki/outputs/`).
- "I'll type my own" — take their question and run the QUERY cycle.
- "Not now" — skip.

Finish with a short handoff: open the folder in **Obsidian**, press `Cmd/Ctrl+G` for Graph View,
and the daily loop — drop sources in `raw/`, `/wiki-ingest`, `/wiki-query`, `/wiki-lint` weekly.
