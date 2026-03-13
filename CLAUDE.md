# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Static personal academic website for Yuanshen Guan, hosted via GitHub Pages at jonbarron.info (CNAME). Forked from Jon Barron's academic website template.

## Architecture

- **index.html** — Single-page site. All content (bio, education, publications, awards) lives here. Uses table-based layout (max-width 800px, centered). Publications use a flexbox `.publication` pattern with a thumbnail and text block.
- **stylesheet.css** — Global styles. Lato font loaded from Google Fonts. Key classes: `.publication`, `.pub-thumb`, `.pub-text`, `.papertitle`, `.name`. Highlighted publications get `bgcolor="#ffffd0"` on their `<tr>`.
- **images/** — Profile photo (`me.JPG`) and publication thumbnails (`images/thumbnails/`).
- **resume_ysguan.pdf** — Linked resume.

No build step, no JavaScript, no templating. Edit HTML/CSS directly.

## Development

Open `index.html` in a browser to preview. No server required (pure static files). Deploy by pushing to `main` — GitHub Pages serves automatically.

## Conventions

- Publications are added as `<tr>` blocks inside the publications `<tbody>`. Each contains a `.publication` div with a `.pub-thumb` image and `.pub-text` div.
- The author's name is wrapped in `<strong>` tags in author lists.
- A commented-out copy of the full page exists at the bottom of `index.html` (lines 320-637) — this appears to be a previous version kept for reference.
