# Working agreement (read me first)

This file is the persistent instructions for any AI assistant working in this repo.
Keep it **short**. Link to deeper files instead of stuffing everything in here.

> `AGENTS.md` is read by many AI coding tools. If you use Claude Code specifically, you
> can also keep a `CLAUDE.md` — same idea. Pick one as the source of truth and link the other.

## How to work with me

- **Match my level** — I can read code and use a terminal; explain decisions and tradeoffs, not syntax.
- **Ask clarifying questions before large work.** Don't guess on anything expensive to undo.
- Prefer **concise** answers. Lead with the conclusion.
- **Verify your work** before calling it done — run it, check it, show me evidence.
- Use my **wiki as the source of truth** ([`wiki/index.md`](wiki/index.md)). If it's stale, tell me.
- When something gets confusing, **slow down and teach me only the concept I need** —
  offer a diagram, tell me what changed, and what you'll try next.

## About me

See [`wiki/_operator.md`](wiki/_operator.md) for my role, how I work, and what good work looks like.

## The knowledge base

This repo is an LLM knowledge base. [`CLAUDE.md`](CLAUDE.md) is the schema — it defines the
`raw/` → `wiki/` layers and the ingest/query/lint operations. **Read it before touching the
wiki.** Ground every answer in `raw/`; if a source is missing, say so and suggest what to add
rather than guessing. I rarely hand-edit the wiki; maintaining it is your job.

## When you don't know the tool

Don't just answer "can you do this?" Instead: **research the current best way** — look for
docs, examples, current tools, and tradeoffs — then **recommend an approach** with reasoning.
Use sub-agents to investigate alternatives in parallel when it helps.
