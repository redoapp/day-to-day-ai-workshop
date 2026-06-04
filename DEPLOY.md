# Ship it: put your page on the internet

**Local** = only your machine sees it. **Deployed** = the internet does. GitHub stores the
files; **Cloudflare Pages** hosts the site. Pick one of the two paths below.

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
   - **Build output directory:** `site`
4. **Save and Deploy.** You get a `*.pages.dev` URL, and every `git push` redeploys.

## Path B — CLI (one command, no dashboard)

```bash
npx wrangler pages deploy site --project-name=<your-name>-workbench
```

First run will prompt you to authenticate and create the project. Faster than the dashboard
once you've done it once; good for iterating.

## Verify it actually shipped

Don't trust "deploy succeeded" — confirm the page loaded. Ask your AI:

> *"Fetch my live URL and confirm the page rendered with my content, not a 404 or a blank shell."*

If something's off, ask: *"what changed, what failed, and what will you try next?"*

## Other hosts (same idea, different button)

**GitHub Pages**, **Netlify**, and **Vercel** all do the same job: point them at the repo,
set the output folder to `site`, deploy. Ask your AI to compare them for your case and recommend one.
