# Otacon — "coming soon" deploy folder

This folder **is** the entire published site at <https://zedvawn.github.io/otacon/> while the
new Otacon site is in *coming soon* mode. GitHub Pages serves these files exactly as-is —
**no build step runs.** The full Astro site in `site3/` stays in source, untouched, until you flip.

## Contents

| File | Purpose |
|------|---------|
| `index.html` | The coming-soon landing page (self-contained; relative `assets/img/…` paths). |
| `404.html` | Shown for any other path. Uses absolute `/otacon/…` paths (a 404 is served from arbitrary URLs). |
| `assets/img/` | Avatar, favicon, and og image — the only assets these two pages need. |

## Preview locally

Just open `index.html` in a browser — assets resolve from the sibling `assets/` folder.
(`404.html` won't show its images locally because it uses absolute `/otacon/` paths; that's expected.)

## Swap the avatar

Drop a square PNG into `assets/img/` (e.g. `otacon-build.png`) and change the single
`<img src="assets/img/otacon-nervous.png" …>` line in `index.html`.

## 🚀 Go live with the FULL site (flip out of coming-soon)

Deploys are driven by [`.github/workflows/pages.yml`](../../.github/workflows/pages.yml),
which runs on every push to **`main`**.

1. Open `.github/workflows/pages.yml`.
2. **Comment out** the `Upload artifact (coming soon)` step.
3. **Uncomment** the whole `FLIP TO FULL SITE` block
   (`Setup Node` → `Build site3` → `Upload artifact (full site)`).
4. Commit and push to `main`. Actions runs `npm ci && npm run build` in `site3/` and
   publishes `site3/dist` — the full Hero + CommandBrowser + docs + features site.

## ↩️ Revert to coming-soon

Reverse those two edits (re-enable `Upload artifact (coming soon)`, re-comment the full block)
and push to `main`.

## Notes

- Nothing goes live until changes reach `main` — working on `develop` is safe.
- The legacy plain-HTML site in `site/` is no longer deployed but is left in the repo untouched.
