# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Personal landing page for [code.nanotaboada.com.ar](https://code.nanotaboada.com.ar), hosted on GitHub Pages. Static HTML/CSS only — no build system, no package manager, no JavaScript authored here.

## Development

No build step. Open `index.html` directly in a browser, or use VS Code's Live Server extension. There are no tests, no linter config, and no CI pipeline.

## Architecture

Single-page site with a top navbar only:

- `index.html` — the entire page; Bootstrap 5 (CDN), Google Fonts Fira Code (CDN), Material Symbols Rounded (CDN)
- `assets/styles/main.css` — all custom styles; flat file, no preprocessor
- `assets/images/background.jpg` — full-bleed fixed background image
- `CNAME` — GitHub Pages custom domain

The navbar links out to GitHub, LeetCode, CodeSignal, HackerRank, and LinkedIn. No server-side logic exists.

## Commit convention

```
type(scope): description   — max 80 chars
```

Types: `feat` `fix` `chore` `docs` `refactor` `ci` `perf`

Scopes: `nav` `styles` `assets` `html` `deps`

## Style constraints

- Line wrap at 127 characters (enforced by `.vscode/settings.json`)
- HTML formatted on save via VS Code's built-in HTML formatter
- No border-radius on interactive elements (navbar, dropdowns, toggler) — intentional design choice
- Color palette: `#212529` (dark) and `#F8F9FA` (light) for hover states; no other custom colors
