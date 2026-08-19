# Portfolio — Alexander Urquico

A single self-contained page (`index.html`). No build step, no dependencies.

## Before you publish

1. Re-read the three project write-ups and confirm you're comfortable with every
   claim being public. They deliberately avoid internal URLs, endpoint names and
   the security findings from the legacy app — keep it that way.

## Deploy to GitHub Pages

```bash
# in this folder
git init
git add .
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/AlexanderUrquico/AlexanderUrquico.github.io.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save.**

- Repo named `AlexanderUrquico.github.io` publishes at `https://alexanderurquico.github.io`
- Any other repo name publishes at `https://alexanderurquico.github.io/<repo-name>/`

First build takes a minute or two. `.nojekyll` is included so GitHub serves the
files as-is instead of running Jekyll over them.

## Editing

Everything lives in `index.html` — CSS in the `<style>` block at the top, content
in the `<body>`. The palette is defined once in the `:root` block; changing
`--pink`, `--violet`, `--amber` and `--teal` restyles the whole page.

To add a project, copy an `<article class="card c1">` block and change the
`c1`/`c2`/`c3` class — that's what sets the offset shadow colour.
