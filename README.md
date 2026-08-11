# lpwpower.github.io

Personal academic homepage of **Peiwen Li** (Ph.D. student, Yale CS).
A single static page in a "technical drawing / blueprint" design language — no framework, no build step.

Live at **https://lpwpower.github.io/** — GitHub Pages serves this repo as-is
(Settings → Pages → Deploy from a branch, `main` / root).

## Structure

```
index.html      the entire site (HTML + CSS + a little vanilla JS)
404.html        not-found page
figures/        avatar + publication figures (all images the page uses)
.nojekyll       tells GitHub Pages to serve files as-is
```

## Publishing changes

```bash
git add -A && git commit -m "update" && git push
```

The site refreshes a minute or so after pushing to `main`.

## Everyday maintenance

- **New paper** — copy an existing `<div class="pub">…</div>` block inside `<div class="publist">`,
  edit title / authors / tag / links, and add `data-fa="1"` if first-author (feeds the sort toggle).
  Add its hand-drawn fallback by copying a `<svg class="thumb">` sketch, or just let it show the figure.
- **New figure** — drop a PNG into `figures/` and set its path in that paper's `data-srcs`.
  `data-srcs` accepts a `|`-separated cascade; the first source that loads wins, and if none
  load the hand-drawn SVG sketch shows instead.
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
