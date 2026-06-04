# raw/ — Layer 1: your sources (read-only for the AI)

Your single source of truth. Drop raw material here; the AI **reads** from it but never
edits it. That immutability is what lets you always check the AI's claims against the original.

```
raw/
├── articles/   ← web-clipped articles, threads, pasted text
├── papers/     ← academic papers / PDFs (converted to markdown)
└── assets/     ← images from sources (add as needed)
```

**Conventions**
- One file per source, kebab-case name (`bitcoin-halving-2024-explainer.md`).
- Put the URL at the top: `source: "https://..."` (the Web Clipper does this for you).
- Don't organise or clean it — just get the text in. The AI does the structuring.

You don't need every subfolder on day one. `articles/` is enough to start.
