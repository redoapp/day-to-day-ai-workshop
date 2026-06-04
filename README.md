# Day-to-Day AI — Workshop Starter

An opinionated starter for turning AI from a chat box into a **coworker** you delegate to.

This repo is the "end state" from the workshop, ready to fork. It gives you four things:

1. **A wiki** (`/wiki`) — durable context AI can read: your role, workflows, taste, projects.
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
4. Start with [`wiki/00-start-here.md`](wiki/00-start-here.md).

---

## The three activities (map to folders)

| Activity | Folder | Prompt to paste into your AI |
|---|---|---|
| **1. Build your wiki** | `/wiki` | *"Interview me until you understand my role, then write the notes in `/wiki` so a new coworker could get up to speed on me in five minutes. Push back where my answers are vague."* |
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
- **Treat the wiki as source of truth.** Point `AGENTS.md` at it and prune it as it drifts.

---

## Your next 7 days

- [ ] Add one note to `/wiki` each day.
- [ ] Add one line to `AGENTS.md` (one persistent instruction).
- [ ] Turn one repeated task into a skill or checklist in `/skills`.
- [ ] Ship one tiny artifact from `/site`.
- [ ] Ask your AI to summarize what it learned about how you work.

---

## What's in here

```
.
├── AGENTS.md          # persistent instructions for your AI coworker
├── wiki/              # durable memory: who you are, how you work
├── skills/            # packaged, repeatable workflows
├── site/              # a simple page to deploy (Cloudflare Pages)
├── DEPLOY.md          # how to put the page on the internet
└── .gitignore
```

The tools will change. The durable skill is building context, asking better questions,
delegating clearly, and verifying outcomes. That's how AI becomes a coworker.
