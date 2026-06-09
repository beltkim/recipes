# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Family recipe cookbook static site deployed at **domusrecipes.com.br** via GitHub Pages. Two single-page apps, no build process.

## Deployment

There is no build step. Changes deploy by pushing to the **gh-pages** branch (not `main`):

```bash
git add .
git commit -m "update cookbook"
git push origin gh-pages
```

GitHub Pages serves from the `gh-pages` branch root. The `main` branch is for development; merge to `gh-pages` to publish.

## Changing the Password

Generate a SHA-256 hash in any browser console, then replace `PASS_HASH` near the bottom of `cookbook.html`:

```js
crypto.subtle.digest('SHA-256', new TextEncoder().encode('yourpassword'))
  .then(b => console.log(Array.from(new Uint8Array(b)).map(x=>x.toString(16).padStart(2,'0')).join('')))
```

## Architecture

Two self-contained HTML files — all CSS and JavaScript are inline within each file:

- **cookbook.html** — Password-protected recipe catalog. 103 recipe cards embedded directly in the HTML, filtered client-side. Uses `sessionStorage` for auth persistence.
- **index.html** — Weekly meal planner with 6 day cards (Mon–Sat), completion toggles, and filter buttons.
- **assets/original_recipes/** — 123 JPG recipe photos referenced by filename from `cookbook.html`.

### Recipe Card Structure (`cookbook.html`)

Each recipe is a `<div class="recipe-card" data-cat="CATEGORY">` block. Categories:

| `data-cat` value | Label |
|---|---|
| `indice` | Índice |
| `sobremesas-e-doces` | Sobremesas e Doces |
| `paes-e-massas-doces` | Pães e Massas Doces |
| `lanches-e-sanduiches` | Lanches e Sanduíches |
| `saladas-e-acompanhamentos` | Saladas e Acompanhamentos |
| `molhos-e-pastas` | Molhos e Pastas |
| `pratos-principais` | Pratos Principais |
| `massas-e-pizzas` | Massas e Pizzas |
| `bebidas` | Bebidas |

Instructions go in `<li class="step">` elements. Notes use a highlight-box style div. Photos reference `assets/original_recipes/filename.jpg`.

## Tech Stack

- Vanilla HTML5/CSS3/JavaScript (ES6+) — no frameworks, no npm, no bundler
- Google Fonts (Playfair Display + DM Sans) loaded via CDN
- Password auth: browser-side SHA-256 via `crypto.subtle`, stored in `sessionStorage`
