# LLM Knowledge Bases

> ⚠️ **This is a worked example** so you can see the quality bar. Duplicate this folder for
> your own topic, then empty it out. The note below was *distilled by an LLM* from the files
> in [`sources/`](sources/) — that's the whole idea.

**Topic:** Using LLMs to build and maintain personal knowledge bases.
**Last updated by:** LLM, from 1 source.

## Overview

A personal knowledge base is an "external brain": markdown notes about topics you care
about, **built and maintained by an LLM** rather than by hand. You collect raw sources; the
LLM compiles them into a distilled wiki and keeps enhancing it as you add more or ask
questions. [karpathy-llm-knowledge-bases]

## Key ideas

- **Manipulate knowledge, not just code.** The interesting use of LLM "token throughput" is
  increasingly turning messy sources into durable, structured knowledge. [karpathy-llm-knowledge-bases]
- **Sources in → distilled notes out.** Raw material ("junk": web, PDFs, pastes) is collected,
  then compiled into a `.md` wiki. Irrelevant sources are discarded. [karpathy-llm-knowledge-bases]
- **The LLM owns the wiki.** You rarely hand-edit. Operating on it (Q&A, enhancement) happens
  through the LLM via CLIs/agents. [karpathy-llm-knowledge-bases]
- **Read it in Obsidian.** The notes are plain markdown, so any markdown tool works for
  browsing, search, and links. [karpathy-llm-knowledge-bases]

## How to apply this

1. Pick a topic you keep researching.
2. Drop sources into `sources/` as you find them.
3. Ask the LLM to distill them into this `README.md` — **synthesis with citations**, not a
   per-source summary.
4. Ask questions; let the LLM answer and append to `questions.md`, enhancing this note when
   it learns something durable.

## Open questions

- What's the right granularity — one big topic note, or split once it gets long?
- How do you keep citations trustworthy as the source pile grows?

## Sources

- `[karpathy-llm-knowledge-bases]` — [sources/karpathy-llm-knowledge-bases.md](sources/karpathy-llm-knowledge-bases.md)
