# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Lodestone Labs marketing website - a Jekyll static site with Tailwind CSS, hosted on GitHub Pages.

## Build Commands

```bash
make watch     # Start dev server with live reload (http://localhost:4000)
make build     # Build the static site for production
```

**Prerequisites:** Ruby with Bundler, Node.js, and image libraries (libvips, libpng, libwebp, libjpeg).

## Architecture

**Stack:**
- Jekyll 4.2 (Ruby) - static site generator
- Tailwind CSS 3.4 with PostCSS - styling
- Flowbite 2.3 - UI component library
- jekyll-postcss - processes Tailwind in Jekyll pipeline

**CSS Pipeline:**
- Entry point: `assets/css/main.css`
- PostCSS processes imports, Tailwind, autoprefixer
- Production builds (`JEKYLL_ENV=production`) also run cssnano minification

**Content Structure:**
- `_layouts/default.html` - main template (includes hero, about, services, contact sections)
- `_includes/navigation.html` - reusable nav component
- `index.markdown`, `about.markdown`, `contact.html` - page content
- `assets/images/logo/` - brand assets (SVG/PNG in black/white variants)

**Tailwind Content Sources** (from `tailwind.config.js`):
- `_includes/**/*.html`
- `_layouts/**/*.html`
- `_posts/*.md`
- `*.html`
- `node_modules/flowbite/**/*.js`

## Notes

- `_config.yml` is NOT hot-reloaded; restart `make watch` after changes
- Flowbite JS loaded via CDN in default layout
