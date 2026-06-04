# sites/ — websites you build (deliverables)

One folder per website. Each is a deliverable **you own** — the AI helps build and edit it
**when you ask**, but it sits outside `raw/` and `wiki/`, so the ingest/query/lint cycles never
touch it. Draw on the knowledge base when you build (e.g. *"make a page summarising
`wiki/concepts/…`"*), but the site itself lives here.

```
sites/
└── <site-name>/
    └── index.html      ← a static site; no build step needed
```

## Add a new site
*"Create a new site folder `sites/<name>` with a simple `index.html`. No database, no build step."*

## Deploy
Each site is its own **Cloudflare Pages project**, with build output directory `sites/<name>`.
See [`DEPLOY.md`](../DEPLOY.md) — the steps are the same per site, you just point Cloudflare at
that folder (or `npx wrangler pages deploy sites/<name>`).

## What's here
- [`personal-page/`](personal-page/) — the starter page from the workshop's "ship something small."
