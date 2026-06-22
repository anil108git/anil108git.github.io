# AGENTS.md — Anil Kumar Profile Page

## Overview

Single-file static portfolio page (`index.html`) with embedded CSS/JS. No build
tooling, no framework, no package manager, no tests.

## File structure

```
index.html          — entire app (HTML, CSS, JS)
resume/
  Kumar_Anil_Resume_17June26.pdf   — downloadable resume
  PP_Size_Anil_Black.png           — hero photo
  Anil_Kumar_QAManager.md          — resume source (not linked from page)
test.js             — placeholder, not meaningful
```

## Local dev

Serve with any static file server:

```bash
npx serve .
# or
python3 -m http.server
```

No build step, no install.

## Theme system

6 themes controlled by `data-theme` attribute on `<html>`. Theme picker at
bottom-right. Selection persisted in `localStorage` (key: `theme`).

CSS custom properties (`--bg`, `--accent`, etc.) drive all colors. To add a
theme: add a `[data-theme="name"]` block in `<style>` and a button in the
palette HTML.

## Deploy

GitHub Pages — push to `main`, enable in repo Settings → Pages → `main` branch
/ root. No build step.

## Image assets

Hero photo uses JPG extension but is a PNG file (`PP_Size_Anil_Black.png`).
Don't rename unless you update the `<img src>` in `index.html`.
