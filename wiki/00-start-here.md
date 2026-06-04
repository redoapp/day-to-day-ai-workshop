# Start here — your LLM wiki

This wiki has two parts:

1. **`_operator.md`** — light context about *you*: your role, how you work, what good looks like.
   You write this once and tweak it occasionally.
2. **`topics/`** — **LLM-maintained knowledge bases**, one folder per topic you care about.
   You drop in raw sources; the LLM distills and grows the notes. You mostly *read*.

## The model (why it's shaped this way)

This follows Andrej Karpathy's "LLM knowledge bases" idea:

> Raw data from many sources ("junk": web pages, PDFs, pastes) is **collected**, then
> **compiled by an LLM into a `.md` wiki**, then **operated on by CLIs** so the LLM can do
> Q&A and **incrementally enhance** it — all viewable in Obsidian. *You rarely ever write or
> edit the wiki manually — it's the domain of the LLM.*

So the wiki isn't a folder you maintain by hand. It's an **external brain the LLM maintains
for you** from the raw material you feed it.

## The loop (per topic)

```
   drop sources            ask the LLM to distill        ask questions
   into sources/    ──►     into README.md         ──►    LLM answers + appends
   (links, PDFs,           (synthesis, not a              to questions.md and
    pastes)                 dump — cite the sources)      enhances README.md
                                   ▲                              │
                                   └──────────────────────────────┘
                                        you mostly read & prune
```

## Anatomy of a topic

```
topics/<your-topic>/
├── sources/      # the inbox: raw "junk" you collect (one file per source)
├── README.md     # the distilled knowledge base — the LLM writes this
└── questions.md  # a running Q&A log the LLM appends to
```

See the worked example in [`topics/example-ai-knowledge-bases/`](topics/example-ai-knowledge-bases/).

## Start your own topic

Paste this to your AI:

> "Duplicate `wiki/topics/example-ai-knowledge-bases/` as `topics/<my-topic>`, empty out the
> example content, and tell me what sources to drop into `sources/`. Once I've added them,
> distill `README.md` from those sources — synthesize, don't summarize each one, and cite
> which source each claim came from."

## View it nicely

Open the repo (or just the `wiki/` folder) as an **Obsidian** vault to browse, search, and
follow links between notes. The LLM does the writing; Obsidian is how you read.
