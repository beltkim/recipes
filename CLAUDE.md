# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Family recipe cookbook static site deployed at **domusrecipes.com.br** via GitHub Pages. Self-contained single-page HTML files under `docs/`, no build process.

## Deployment

There is no build step. GitHub Pages serves the **`docs/` folder of `main`** (`docs/CNAME` holds the custom domain), so pushing to `main` publishes:

```bash
git add .
git commit -m "update cookbook"
git push origin main
```

There is no `gh-pages` branch.

## Login

`cookbook.html` and `icecreams.html` show a login overlay that POSTs Basic-auth credentials to `AUTH_URL` (`https://api-auth-y887.onrender.com/ghpages/login`). On success it sets `sessionStorage.auth = '1'`, which both pages check — logging in on one unlocks the other for the session. Users and passwords live in that auth service, not in this repo.

The gate is client-side only: the recipe content is still in the page source.

## Architecture

All CSS and JavaScript are inline within each file:

- **docs/cookbook.html** — Login-protected recipe catalog. Recipe cards are `<article class="card" data-cat="CATEGORY">`, filtered client-side by category pills and search.
- **docs/icecreams.html** — Login-protected "Sorvetes com 4 Ingredientes" (Lulo Fouet ebook) page, with tabs for recipes, techniques, equipment and science. Linked from the cookbook header.
- **docs/index.html** — Weekly meal planner with day cards, completion toggles, and filter buttons.
- **docs/assets/original_recipes/** — JPG recipe photos referenced by filename from `cookbook.html`.

### Recipe Card Structure (`cookbook.html`)

Each recipe is an `<article class="card" data-cat="CATEGORY">` block. Categories:

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

### Recipe Card Structure (`icecreams.html`)

Each recipe is a `<div class="recipe-card" data-type="TYPE">` with `TYPE` one of `gelato`, `sorbet`, `americano` (the filter pills). Custard-base recipes are `americano` with a "Custard" badge. Quantities go in `<span class="ing-qty">` inside `.ingredients-list` — a leading number makes them click-to-scale; `steps-list` / `step-item` hold the method when a card needs one.

## Tech Stack

- Vanilla HTML5/CSS3/JavaScript (ES6+) — no frameworks, no npm, no bundler
- Google Fonts (Playfair Display + DM Sans) loaded via CDN in `index.html`
- Login via the external auth service above, persisted in `sessionStorage`
