---
title: "Karpathy — LLM Knowledge Bases"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "Karpathy's note proposing LLM-built, LLM-maintained personal knowledge bases compiled from raw sources into a markdown wiki, viewable in Obsidian."
tags: [llm, knowledge-management]
type: source
status: final
source_url: "https://x.com/karpathy/status/2039805659525644595"
authors:
  - "Andrej Karpathy"
---

# Karpathy — LLM Knowledge Bases

**Summary.** [[andrej-karpathy]] describes a workflow he's found increasingly useful: using
LLMs to build personal **knowledge bases** for topics of research interest. The core shift he
names is that a growing share of his LLM usage goes into *manipulating knowledge* (stored as
markdown and images) rather than *manipulating code*. The mechanism is a pipeline: raw data
from many sources is collected, **compiled by an LLM into a `.md` wiki**, then operated on by
CLIs so the LLM can do Q&A and incrementally enhance the wiki — all viewable in Obsidian. A
defining constraint is that the human rarely writes or edits the wiki by hand; maintenance is
"the domain of the LLM." He notes there's room for a real product here rather than a hacky
collection of scripts. See [[llm-knowledge-base]] for the distilled concept.

## Key points
- LLM token throughput is shifting from code to **knowledge management**.
- Sources in → distilled `.md` wiki out; irrelevant sources are discarded.
- The LLM, not the human, maintains the wiki.
- Plain markdown + Obsidian keeps it portable and inspectable.

## Concepts
- [[llm-knowledge-base]]

## Entities
- [[andrej-karpathy]]
