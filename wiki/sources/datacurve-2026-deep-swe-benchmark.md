---
title: "DataCurve AI — DeepSWE benchmark"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "A contamination-free benchmark of 113 original, long-horizon coding tasks across 5 languages, with behavioural verifiers, built to de-saturate frontier coding-agent evaluation."
tags: [coding-agents, benchmark, evaluation]
type: source
status: final
source_url: "https://deepswe.datacurve.ai/"
authors:
  - "DataCurve AI"
---

# DataCurve AI — DeepSWE benchmark

**Summary.** [[deep-swe-benchmark]] (by [[datacurve-ai]]) is a coding-agent benchmark of **113
original, long-horizon software-engineering tasks** across 5 languages, sourced from 91 live
open-source repos. Its motivation is that public coding benchmarks are **saturating** — top
models cluster in a narrow band — so it raises difficulty and integrity on four axes:
**contamination-free** tasks (written from scratch), **diversity** (91 repos / 5 languages),
**real-world complexity** (~5.5× more code and ~2× more output tokens than [[swe-bench]] Pro),
and **behavioural verification** (hand-written verifiers that accept any solution whose
observable behaviour is correct). Tasks use the **Harbor** format (Dockerized env, withheld
reference solutions, patch-based verifiers) and are scored via the **Pier** system on Modal,
with **mini-swe-agent** as the model-agnostic harness — also runnable through [[claude-code]],
codex, gemini-cli, and opencode. As of the 2026-05-30 leaderboard, gpt-5.5 leads at **70%**,
followed by claude-opus-4.8 (**58%**), gpt-5.4 (**56%**), and claude-opus-4.7 (**54%**); 18
models evaluated, with lower performers at ~5–32%.

## Why it's useful to know
- A current, **harder** yardstick for agentic coding than the now-saturating [[swe-bench]].
- Its **behavioural verifier** design is a reusable idea for evaluating agents in general.
- The leaderboard is a quick read on where frontier coding agents actually stand on hard tasks.

## Entities
- [[deep-swe-benchmark]] · [[datacurve-ai]] · [[swe-bench]] · [[claude-code]]
