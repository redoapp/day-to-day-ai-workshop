# Skills

A **skill** turns a good one-off interaction into a **repeatable capability**.

It's usually just markdown (plus optional scripts). It teaches AI how to do a specific
kind of work the way *you* want it done — so you don't re-explain it every time.

## Anatomy

Each skill lives in its own folder with a `SKILL.md`:

```
skills/
└── draft-update/
    └── SKILL.md     # name + description + instructions
```

The `description` is what an AI assistant reads to decide *when* to use the skill, so
make it specific about the trigger.

## Make your own (Activity 2)

Paste this to your AI:

> "Grill me about a real task until you can write a clear spec with checklist milestones.
> Then save it as a new skill folder under `/skills` with a `SKILL.md`."

Start from [`draft-update/SKILL.md`](draft-update/SKILL.md) as a worked example.
