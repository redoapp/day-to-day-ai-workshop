---
title: "DeepSWE (benchmark)"
date_created: 2026-06-04
date_modified: 2026-06-04
summary: "DataCurve AI's benchmark of 113 original, long-horizon coding tasks with behavioural verifiers, built to de-saturate frontier coding-agent evaluation."
tags: [tool, benchmark]
type: entity
status: final
related:
  - "[[datacurve-ai]]"
  - "[[swe-bench]]"
source_count: 1
---

# DeepSWE (benchmark)

A coding-agent **benchmark** from [[datacurve-ai]] — **113 original, long-horizon** software-
engineering tasks across TypeScript, Go, Python, JavaScript, and Rust, from 91 live open-source
repositories. It exists because public benchmarks like [[swe-bench]] are **saturating** at the
frontier. [[datacurve-2026-deep-swe-benchmark]]

Distinguishing design: **contamination-free** (tasks written from scratch), **harder** (~5.5×
more code, ~2× more output tokens than SWE-bench Pro), and **behavioural verification** — a
hand-written verifier accepts any solution whose *observable behaviour* is correct, rather than
matching code structure. Tasks use the **Harbor** format and the **Pier** evaluation system;
**mini-swe-agent** is the model-agnostic harness, and it also runs via [[claude-code]], codex,
gemini-cli, and opencode.

As of 2026-05-30, gpt-5.5 leads (~70%), with claude-opus-4.8 (~58%), gpt-5.4 (~56%), and
claude-opus-4.7 (~54%) behind.

> Not to be confused with Together AI / Agentica's **DeepSWE agent** — an RL-trained coding model
> on Qwen3-32B. Same name, different thing (an agent, not a benchmark).

## Sources
- [[datacurve-2026-deep-swe-benchmark]]
