# lpwpower.github.io

Personal academic homepage of **Peiwen Li** (Ph.D. student, Yale CS).
A single static page in a "technical drawing / blueprint" design language — no framework, no build step.

## Structure

```
index.html      the entire site (HTML + CSS + a little vanilla JS)
404.html        not-found page
figures/        publication framework figures (local copies win over remote fallbacks)
.nojekyll       tells GitHub Pages to serve files as-is
content/        KEEP — inherited from the old Hugo site; index.html reads
                publication figures and the avatar from here via relative paths
```

## Deploy (one-time)

1. In this repo, **delete the old Hugo machinery** so it stops rebuilding over the static site:
   - `.github/workflows/` (all YAML files), `netlify.toml`, `go.mod`, `hugoblox.yaml`,
     `config/`, `layouts/`, `publications.bib`, `package.json`
   - **Do NOT delete `content/`** (figures + avatar live there).
2. Copy everything in this folder into the repo root. Commit & push to `main`.
3. GitHub → Settings → Pages → Source: **Deploy from a branch**, Branch: `main` / `/ (root)`.
4. Visit https://lpwpower.github.io/ (allow a minute for the first build).

## Everyday maintenance

- **New paper** — copy an existing `<div class="pub">…</div>` block inside `<div class="publist">`,
  edit title / authors / tag / links, and add `data-fa="1"` if first-author (feeds the sort toggle).
  Add its hand-drawn fallback by copying a `<svg class="thumb">` sketch, or just let it show the figure.
- **New figure** — drop a PNG into `figures/` and put its path first in that paper's `data-srcs`.
  Cascade order: `figures/… | content/… (old-site copy) | remote fallback`. First one that loads wins.
- **News** — add an `<li>` at the top of `<ol class="news">`; retire old ones into the
  `<details class="newsarch">` drawer.
- **Under-review paper gets accepted** — swap its `vtag` text to the venue, delete the red
  `<span class="stamp">` and update the arXiv links if needed.
- **Publish your CV later** — drop `assets/cv.pdf` into the repo, then add one row to the
  sidebar `<nav class="links">`: `<a href="assets/cv.pdf" target="_blank" rel="noopener">Curriculum vitae<span class="mono">↓ 05</span></a>`.
- **Title-block revision tag** — bump `REV B` / date in the footer title block when you feel like it. :)

## Local preview

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

(Opening index.html via file:// also works; remote-fallback images need network.)

## Design notes

Palette: paper `#FCFDFE`, ink `#182838`, cobalt `#2B62A8`, teal `#177E76`, vermilion stamp `#B5482A`.
Type: Geist + Geist Mono (Kimi's stack), Caveat (signature), Lora (italic voice).
The page is a tracing sheet taped over graph paper: index flags on the right edge are fixed
navigation with scroll-spy; on narrow screens they re-mount along the top edge.
