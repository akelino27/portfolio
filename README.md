# Portfolio site — deploy notes

Single-file static site (`index.html`). No build step. `.nojekyll` included for GitHub Pages.

## Deploy: GitHub Pages (free)

1. github.com → **New repository** → name it `portfolio` (or `<username>.github.io` for a root URL) → **Public** → Create.
2. In the repo → **Add file → Upload files** → drag `index.html` (+ `.nojekyll`) → Commit.
3. **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main` / `/ (root)` → Save.
4. Wait ~1 min. Live at:
   - `https://<username>.github.io/portfolio/` , or
   - `https://<username>.github.io/` if the repo is named `<username>.github.io`.

## Alternatives (free)

- **Netlify** / **Cloudflare Pages** / **Vercel** — drag-drop the folder, free tier, custom domain support. Cloudflare Pages = unlimited bandwidth.
- **Netlify Drop**: app.netlify.com/drop → drag the `portfolio` folder → instant URL.

## Free database (if/when a project needs one)

- **Supabase** — Postgres + auth + storage + REST/realtime. 500MB DB, 2 free projects. Best all-rounder.
- **Neon** — serverless Postgres, 0.5GB free.
- **Turso** — SQLite at the edge, generous free tier.
- **Cloudflare D1** — SQLite, free with a Cloudflare account.
- **MongoDB Atlas** — 512MB free.

The portfolio itself is static — no DB needed unless we add a contact form (easy path: **Formspree** free tier) or a live demo app.
