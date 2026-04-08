# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repo contains weekly lecture slide decks for the **IXD 620/320** course ("Human Perception Revisited" and related topics). Each week lives in its own folder (`week09/`, `week10/`, etc.) with an `index.html` that is a self-contained Reveal.js presentation.

## Architecture

- **Single-file slides**: Each week's `index.html` contains all HTML, CSS, and JS inline (no external stylesheets or build step).
- **Reveal.js 4.6.1** loaded from CDN (`cdn.jsdelivr.net/npm/reveal.js@4.6.1`).
- **Font**: Inter via Google Fonts.
- **Design system**: Dark background (`#0a0a0a`), white text, accent color `#C84B30`. All slides are left-aligned, not centered.
- **Slides are `<section>` elements** inside `.reveal > .slides`. Each section wraps content in a `<div class="slide ...">` with vertical-alignment helpers (`center-v`, `bottom-v`, `top-v`).

## How to View

Open `index.html` directly in a browser, or serve locally:

```
npx serve .
# or
python3 -m http.server
```

No build, install, or compile step is needed.

## Slide Authoring Conventions

- **Typography classes**: `display` (hero), `section-word` (divider), `statement` (big idea), `heading` (content header), `eyebrow` / `section-eyebrow` (small uppercase label in accent color).
- **Slide metadata**: A `<div class="slide-meta">` at the bottom of key slides with format `Week N · IXD 620 / 320 · Topic`.
- **Interactive elements**: Some slides embed inline `<script>` blocks for toggles/demos (e.g., AI summary buttons). These are scoped IIFEs.
- **Images**: Placed alongside `index.html` or in an `images/` subfolder (see week09). Referenced with relative paths.
- Reveal.js config: `hash: true`, `transition: 'fade'`, `width: 1440`, `height: 810`, `center: false`.
