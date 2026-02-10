# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Divine Light is a single-page interactive website containing curated Quranic verses, Prophetic du'as, and stories organized around the theme of carrying ambition and worldly success as a Muslim. It is a single HTML file with no build system, no dependencies, and no framework.

## Development

There is no build step, package manager, or test suite. The entire application lives in `divine-light.html`.

```bash
# Run locally — just open the file in a browser
open divine-light.html
```

## Architecture

**Single-file application** — all HTML, CSS, and JavaScript are in `divine-light.html`:

- **CSS** (lines 8-478): CSS custom properties for theming (gold/teal/dark palette), card styles for different content types (`.verse-card`, `.dua-card`, `.story-card`, `.hadith-card`, `.checklist`), responsive breakpoint at 600px, entry animations via `@keyframes`
- **HTML** (lines 480-1010): Seven tab-navigated sections (`daily-dua`, `inner-light`, `spiritual-insight`, `stories`, `the-model`, `sulayman-strategy`, `checklist`), each as a `.section` div toggled via `.active` class
- **JavaScript** (lines 1012-1026): Minimal — just tab navigation via `data-section` attributes on nav buttons

**Fonts**: Google Fonts loaded externally — Cormorant Garamond (body), Amiri and Noto Naskh Arabic (Arabic text)

## Content Guidelines

- Arabic Quranic text and hadith text must be verified for accuracy — errors should be treated as critical bugs
- Translations are created as separate files: `divine-light-[language-code].html` (e.g., `divine-light-tr.html`)
- Content is intentionally Islamic and not secularized; maintain this tone in any additions
