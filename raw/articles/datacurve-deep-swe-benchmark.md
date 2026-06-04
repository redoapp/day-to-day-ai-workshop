---
title: "DeepSWE — a benchmark for frontier coding agents on long-horizon tasks"
source: "https://deepswe.datacurve.ai/"
repo: "https://github.com/datacurve-ai/deep-swe"
author: "DataCurve AI"
clipped: 2026-06-04
tags:
  - raw
type: article
status: raw
---

# DeepSWE (DataCurve AI) — benchmark

> Note: not to be confused with Together AI / Agentica's *DeepSWE* coding **agent** (an
> RL-trained model on Qwen3-32B). This is DataCurve AI's **benchmark** of the same name.

## What it is
A benchmark measuring frontier coding agents on **original, long-horizon software engineering
tasks**. **113 tasks** across **5 languages** (TypeScript, Go, Python, JavaScript, Rust), drawn
from **91 active open-source repositories**, each with an isolated environment and a
program-based verifier.

## Why it was built
"Today's leading public coding benchmarks are starting to saturate at the frontier: top models
cluster within a narrow score band." Four stated advances:
- **Contamination-free** — tasks written from scratch, not adapted from existing code.
- **High diversity** — 91 repos across 5 languages.
- **Real-world complexity** — solutions require ~**5.5× more code** and **~2× more output
  tokens** than SWE-bench Pro.
- **Reliable verification** — hand-written verifiers test **behaviour, not implementation
  details** ("accepts any solution whose observable behaviour is correct").

## How it works
- Tasks use the **Harbor** task format: metadata (repo, base commit, language, resource limits),
  written instructions, Dockerized environments, test suites with **patch-based verifiers**, and
  reference solutions withheld from the agent.
- Evaluated via the **Pier** evaluation system on **Modal** infrastructure.
- Harness: **mini-swe-agent** (model-agnostic); also supports claude-code, codex, gemini-cli, opencode.

## Leaderboard (updated 2026-05-30)
- **gpt-5.5** [xhigh] — **70% ± 4%** | ~$6.61 avg cost | ~21m avg
- **claude-opus-4.8** [max] — **58% ± 5%** | ~$12.58 | ~43m
- **gpt-5.4** [xhigh] — **56% ± 5%** | ~$4.38 | ~27m
- **claude-opus-4.7** [max] — **54% ± 5%** | ~$18.19 | ~39m
- 18 models evaluated; lower performers ranged ~5–32%.

*(Collected from the project site and GitHub repo on 2026-06-04.)*
