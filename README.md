# Liberty Power Gardens

Community-scale food waste recycling that diverts waste from landfills, reduces greenhouse gas emissions, and returns renewable energy and resources to the neighborhoods we serve.

## About

Liberty Power Gardens is building neighborhood-scale biodigestion systems that transform food waste into clean energy, fertile soil, and potable water. Unlike centralized waste processing, our sites become community gardens that pump renewable resources back into the local ecosystems they serve.

**Key impact areas:**
- Divert food waste from landfills (Jersey City alone generated ~40,000 tons in 2021)
- Reduce greenhouse gas emissions by capturing methane (20x more potent than CO₂)
- Lower residents' utility bills through locally generated electricity and heat
- Promote energy independence with distributed, community-owned infrastructure

## Tech Stack

- **Static site generator:** [Jekyll](https://jekyllrb.com/) 4.4.1
- **Theme base:** [Minima](https://github.com/jekyll/minima) ~2.5 (custom layouts override theme defaults)
- **Typography:** DM Serif Display (headings) + DM Sans (body) via Google Fonts
- **Hosting:** Static HTML — compatible with GitHub Pages, Netlify, or any static host
- **No build tools** beyond Ruby/Bundler — all CSS is inline within layouts

## Getting Started

### Prerequisites

- Ruby (~4.4.1)
- Bundler

### Setup

```bash
git clone <repo-url>
cd liberty-power-gardens
bundle install
```

### Development

```bash
bundle exec jekyll serve
```

Visit [http://localhost:4000](http://localhost:4000). The server watches for file changes and auto-regenerates (except `_config.yml` — restart the server after editing that file).

### Build

```bash
bundle exec jekyll build
```

Output goes to `_site/` (gitignored).

## Project Structure

```
├── index.html                 # Landing page (uses layout: landing)
├── blog.html                  # Blog listing page (uses layout: blog)
├── 404.html                   # Error page
├── _config.yml                # Jekyll site configuration
├── _layouts/
│   ├── landing.html           # Main landing page with all sections
│   ├── blog.html              # Blog archive/listing page
│   └── post.html              # Individual blog post template
├── _posts/                    # Blog posts (Markdown with YAML frontmatter)
├── assets/
│   └── images/
│       ├── lpg-logo.svg       # Torch logo
│       └── *.mp4              # Hero background video
├── Gemfile                    # Ruby dependencies
└── CLAUDE.md                  # Claude Code guidance
```

## Landing Page Sections

The landing page (`_layouts/landing.html`) is a single self-contained file with embedded CSS and includes:

1. **Fixed nav** with logo, section jump links, and mobile hamburger menu
2. **Hero** with looping video background, animated gradient overlays, and brand name
3. **Impact stats** — 4-column dark section with key metrics
4. **How It Works** — animated SVG process flow diagram (food waste → energy/soil/water) with flowing particle effects
5. **What We Deliver** — 4 value proposition cards
6. **Our Approach** — differentiator section
7. **Blog preview** — 3 most recent posts pulled dynamically via Liquid
8. **Contact form** — name, email, subject, message
9. **Footer**

## Blog

Posts live in `_posts/` using standard Jekyll naming: `YYYY-MM-DD-title.markdown`. The blog index at `/blog/` lists all posts with category tags, dates, and excerpts.

To add a new post:

```bash
touch _posts/2026-04-04-your-post-title.markdown
```

Front matter template:

```yaml
---
layout: post
title: "Your Post Title"
date: 2026-04-04
categories: sustainability
---

Your content here...
```

## Brand

### Colors

| Color | Hex | Usage |
|-------|-----|-------|
| Flame yellow | `#f9e15e` | Accents, output highlights, brand name |
| Teal green | `#7FB2A5` | Primary, nav links, process nodes, card borders |
| Gray | `#a5afa6` | Muted text, borders, connectors |
| Dark | `#1a1a1a` | Dark sections, text |

### Typography

- **Headings:** DM Serif Display (serif, weight 400)
- **Body:** DM Sans (sans-serif, weights 400–700)

Both loaded via Google Fonts.

### Logo

The torch logo (`assets/images/lpg-logo.svg`) uses the brand color palette — flame yellow for the torch flame, teal for the base, gray for the border.

## Responsive Design

- **Desktop:** Full layout with horizontal nav links, 4-column stats, 2-column cards
- **Tablet (≤768px):** Hamburger menu slide-out, 2-column stats, single-column cards
- **Mobile (≤480px):** Stacked stats, compact spacing

## License

All rights reserved. Copyright Liberty Power Gardens.
