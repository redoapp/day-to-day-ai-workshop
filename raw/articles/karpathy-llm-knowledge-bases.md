---
title: "LLM Knowledge Bases"
source: "https://x.com/karpathy/status/2039805659525644595"
author: "Andrej Karpathy"
clipped: 2026-06-04
tags:
  - raw
type: article
status: raw
---

# LLM Knowledge Bases — Andrej Karpathy

> Something I'm finding very useful recently: using LLMs to build personal knowledge bases
> for various topics of research interest. In this way, a large fraction of my recent token
> throughput is going less into manipulating code, and more into manipulating knowledge
> (stored as markdown and images). The latest LLMs are quite good at it. So:
>
> TLDR: raw data from a given number of sources is collected, then compiled by an LLM into a
> .md wiki, then operated on by various CLIs by the LLM to do Q&A and to incrementally
> enhance the wiki, and all of it viewable in Obsidian. You rarely ever write or edit the
> wiki manually, it's the domain of the LLM. I think there is room for an incredible new
> product instead of a hacky collection of scripts.

## Diagram notes
- "JUNK" (RSS / web / PDF sources) → LLM → "KNOWLEDGE BASE" (a brain made of `.md` files),
  viewable in Obsidian / terminal. Irrelevant sources get trashed.
- Shift: token spend moves from *manipulating code* to *manipulating knowledge*.
- Constraint: humans rarely hand-edit — the wiki is the LLM's domain.

*(This is an example raw source so the wiki has something to compile. Replace it with your
own sources once you point the knowledge base at your topic.)*
