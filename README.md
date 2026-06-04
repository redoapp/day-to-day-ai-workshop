# Day-to-Day AI — Workshop Starter

An opinionated starter for turning AI from a chat box into a **coworker** you delegate to.

This repo is the "end state" from the workshop, ready to fork. It gives you four things:

1. **An LLM knowledge base** (`raw/` + `wiki/` + `CLAUDE.md`) — drop sources in `raw/`; the AI
   compiles and maintains a synthesised wiki. This is the centerpiece — see [`KNOWLEDGE-BASE.md`](KNOWLEDGE-BASE.md).
2. **Persistent instructions** (`AGENTS.md`) — how AI should always work with you.
3. **A skill** (`/skills/draft-update`) — a repeatable workflow, not a one-off prompt.
4. **A shippable page** (`/site`) — a real artifact you deploy to the internet.

> The point isn't the files. It's the operating model: **give your AI coworker the
> context, tools, constraints, and a clear finish line — then delegate and verify.**

---

## Use this template

1. Click **"Use this template" → Create a new repository** (or fork it).
2. Make it **public** and name it something like `your-name-workbench`.
3. Clone it and open the folder in your editor with your AI assistant running:
   ```bash
   git clone https://github.com/<you>/<your-repo>.git
   cd <your-repo>
   ```
4. Run `claude` in the folder (it auto-loads `CLAUDE.md`), then type **`/wiki-start`** — it sets up
   your wiki through a few quick multiple-choice questions. Or read [`KNOWLEDGE-BASE.md`](KNOWLEDGE-BASE.md) to do it by hand.

---

## The three activities (map to folders)

| Activity | Where | What to do |
|---|---|---|
| **1. Build your knowledge base** | `raw/` + `wiki/` | Run **`/wiki-start`** — it interviews you, sets your topic, clears the example, and helps you add your first 3–5 sources. Then `/wiki-query <a real question>` and watch the answer get filed into `wiki/outputs/`. |
| **2. Front-load a real task** | `/skills` | *"Grill me about a real task until you can write a clear spec with checklist milestones, then save it as a skill under `/skills`. Don't start the work until the spec is tight."* |
| **3. Ship something small** | `/site` | *"Make a simple page in `/site` — no database, no build step. Then deploy it to Cloudflare Pages and verify the live URL actually loaded."* |

After each activity, **debrief**: What did it miss? What did it get surprisingly right?
What would you now delegate without watching?

---

## Push it further

You already know your way around a repo — so use the parts of the model that pay off at scale:

- **Delegate, don't prompt.** Run one main thread to manage a project; spin off sub-agents
  for research or independent branches and have them return recommendations + tradeoffs + evidence.
- **Make the AI research tools you don't know.** Not *"can you do this?"* but *"research the
  current best way to do this — docs, examples, tradeoffs — and recommend an approach."*
- **Automate the knowledge base.** Once the manual loop feels natural, schedule `/wiki-ingest`
  to run daily, or compile in the cloud with a GitHub Action — see [`KNOWLEDGE-BASE.md`](KNOWLEDGE-BASE.md).

---

## Your next 7 days

- [ ] Drop one source into `raw/` each day and run `/wiki-ingest`.
- [ ] Ask the wiki one real question with `/wiki-query` and let it file the answer.
- [ ] Add one line to `AGENTS.md` (one persistent instruction).
- [ ] Turn one repeated task into a skill or checklist in `/skills`.
- [ ] Ship one tiny artifact from `/site`.
- [ ] Ask your AI to summarize what it learned about how you work.

---

## What's in here

```
.
├── CLAUDE.md          # the knowledge-base schema (auto-loaded by Claude Code)
├── KNOWLEDGE-BASE.md  # how the system works (read this first)
├── AGENTS.md          # persistent instructions for your AI coworker
├── .obsidian/         # curated Obsidian config (dark theme + colour-coded graph)
├── raw/               # Layer 1: your sources (AI reads, never edits)
├── wiki/              # Layer 2: the AI-compiled wiki (index, concepts, entities, sources…)
│   ├── dashboard.md   #   live Dataview dashboard (Obsidian Homepage)
│   └── _operator.md   #   light context about you (hand-authored)
├── templates/         # note templates (concept / source / entity)
├── .claude/commands/  # /wiki-start, /wiki-ingest, /wiki-query, /wiki-lint
├── .agents/skills/    # bundled skills (source of truth): find-skills, grill-me
├── .claude/skills  →  symlink to ../.agents/skills (so Claude Code sees the same set)
├── skills-lock.json   # pins the bundled skills (restore with `npx skills experimental_install`)
├── skills/            # an example skill you can copy (draft-update)
├── site/              # a simple page to deploy (Cloudflare Pages)
└── DEPLOY.md          # how to put the page on the internet
```

The tools will change. The durable skill is building context, asking better questions,
delegating clearly, and verifying outcomes. That's how AI becomes a coworker.
