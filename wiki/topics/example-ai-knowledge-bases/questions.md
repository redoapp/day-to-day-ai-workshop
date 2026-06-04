# Questions log

> A running Q&A on this topic. You ask; the LLM answers from `sources/` (and says when a
> source is missing). Good answers get promoted into `README.md`. New answers go on top.

---

### Q: Do I have to write any of the wiki by hand?

**A:** No — that's the point. You collect sources and ask questions; the LLM writes and
maintains the notes. Your job is curation: feed it good sources, read the output, prune what's
wrong. *(from [karpathy-llm-knowledge-bases])*

---

### Q: What if the LLM doesn't have a source for something I ask?

**A:** It should tell you instead of guessing — and ideally suggest what source to add to
`sources/` so the answer can be grounded next time. *(behavior to enforce via [`AGENTS.md`](../../../AGENTS.md))*
