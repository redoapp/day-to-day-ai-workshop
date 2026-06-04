# Ship it: put your site on the internet

**Local** = only your machine sees it. **Deployed** = the internet does. GitHub stores the
files; **Cloudflare Pages** hosts the site. Pick one of the two paths below.

Each site lives in its own folder under [`sites/`](sites/) (e.g. `sites/personal-page`) and
becomes **its own Cloudflare Pages project**. Below, replace `sites/<name>` with the folder you
want to ship.

## Path A — Git-connected (auto-deploys on every push)

1. Get the repo on GitHub:
   ```bash
   git add . && git commit -m "My AI workbench" && git push
   ```
2. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git** →
   pick this repo.
3. Build config:
   - **Framework preset:** None
   - **Build command:** *(empty — plain HTML, no build)*
   - **Build output directory:** `sites/<name>` (e.g. `sites/personal-page`)
4. **Save and Deploy.** You get a `*.pages.dev` URL, and every `git push` redeploys.

> Multiple sites? Repeat these steps once per folder under `sites/` — each is a separate Pages
> project pointed at its own `sites/<name>` output directory, all from this one repo.

## Path B — CLI (one command, no dashboard)

```bash
npx wrangler pages deploy sites/<name> --project-name=<name>
```

First run will prompt you to authenticate and create the project. Faster than the dashboard
once you've done it once; good for iterating. Run it once per site, with a distinct
`--project-name` each time.

## Verify it actually shipped

Don't trust "deploy succeeded" — confirm the page loaded. Ask your AI:

> *"Fetch my live URL and confirm the page rendered with my content, not a 404 or a blank shell."*

If something's off, ask: *"what changed, what failed, and what will you try next?"*

## Other hosts (same idea, different button)

**GitHub Pages**, **Netlify**, and **Vercel** all do the same job: point them at the repo,
set the output folder to `sites/<name>`, deploy. Ask your AI to compare them for your case and recommend one.
