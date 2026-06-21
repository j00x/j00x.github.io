# AGENTS.md

## Cursor Cloud specific instructions

This repo is the **`j00x.github.io`** GitHub Pages *user* site that owns the custom domain
`learn.apnet-remote.net` (see `CNAME`). It is currently a placeholder ("Info on the way") and
uses the remote theme `pages-themes/minimal` via the `jekyll-remote-theme` plugin
(`_config.yml`). The richer content lives in the sibling **`apremote.github.io`** project-site repo.

### How to build / run locally

- There is **no `Gemfile`**. Build with the system gems directly:
  - `jekyll build` (output in `_site/`)
  - `jekyll serve --host 0.0.0.0 --port 4001` to preview
- Building requires the gems `jekyll`, `jekyll-remote-theme`, and `jekyll-seo-tag` (the minimal
  theme's layout pulls in `jekyll-seo-tag`). These are baked into the VM snapshot. The remote theme
  is **fetched from GitHub over HTTPS at build time**, so the build needs network access.
- The repo has no homepage source (`index.md`/`index.html`) yet, so `jekyll build` succeeds but
  produces no `index.html` — that matches the current placeholder state and is expected.
- No automated tests or linter; verification = a clean `jekyll build`.
