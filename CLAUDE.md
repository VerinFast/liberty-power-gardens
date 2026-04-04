# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Liberty Power Gardens is a landing page for a community-scale food waste recycling company, built with Jekyll.

## Commands

```bash
bundle install                # Install Ruby dependencies
bundle exec jekyll serve      # Start dev server with live reload at http://localhost:4000
bundle exec jekyll build      # Build static site to _site/
```

## Architecture

- **`_layouts/landing.html`** — Custom standalone landing page layout with embedded CSS (does not use Minima theme styles)
- **`index.html`** — Landing page entry point (uses `layout: landing`)
- **`_config.yml`** — Site title, description, build settings
- **`assets/images/`** — Logo SVG and image assets
- **`_site/`** — Generated output (gitignored, do not edit)

### Brand Colors
- `#f9e15e` — Flame yellow (accent)
- `#7FB2A5` — Teal green (primary)
- `#a5afa6` — Gray (borders, muted text)
