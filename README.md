# Bootstrap 5 Exercise Pack

A single-file, self-contained HTML reference that brings together **19 modules and 38 exercises** covering the full Bootstrap 5 curriculum — with every exercise rendered as a live, interactive demo.

---

## Overview

`bootstrap5-exercises.html` is a standalone study guide and cheat sheet. Open it in any browser and you get a sticky side-nav, live component previews, and syntax-highlighted code snippets — no build step, no server required.

---

## Modules Covered

| # | Module | Exercises |
|---|--------|-----------|
| 01 | Setting Up Bootstrap 5 | CDN setup, npm/local install |
| 02 | Bootstrap Structure & Files | Directory layout, JS bundle |
| 03 | Responsive Grid Layout | Stacked → 2-col → 3-col, container/row/col |
| 04 | Column Layouts & Grid Classes | Sidebar + content, four equal columns |
| 05 | Alignment & Reordering | justify/align center, `order-md-*` |
| 06 | Responsive Flexbox Utilities | flex-column → flex-md-row, card flex layout |
| 07 | Typography | Display classes, text transforms |
| 08 | Forms | Registration form, floating labels |
| 09 | Buttons | Button variants, sizes, groups |
| 10 | Navbars | Responsive navbar with toggler |
| 11 | Cards | Pricing card deck, image cards |
| 12 | Spacing Utilities | Margin/padding scale |
| 13 | Colors & Backgrounds | Contextual color utilities |
| 14 | Display Utilities | `d-none`, `d-md-block`, visibility |
| 15 | Borders & Shadows | Border radius, shadow utilities |
| 16 | Position Utilities | Fixed, sticky, absolute positioning |
| 17 | Bootstrap Icons | Social footer icons, icon-only buttons |
| 18 | JavaScript Plugins | Modal popup, accordion |
| 19 | Customization with Sass | npm + Sass setup, variable overrides |

---

## Getting Started

No installation needed. Just open the file in a browser:

```bash
# macOS
open bootstrap5-exercises.html

# Windows
start bootstrap5-exercises.html

# Linux
xdg-open bootstrap5-exercises.html
```

An internet connection is required on first load for the CDN assets (Bootstrap CSS/JS and Bootstrap Icons). After that, the browser caches them.

---

## Dependencies (CDN)

All loaded automatically — nothing to install locally.

| Dependency | Version | Purpose |
|------------|---------|---------|
| Bootstrap CSS | 5.3.3 | Styles and utility classes |
| Bootstrap JS Bundle | 5.3.3 | JS plugins + Popper.js |
| Bootstrap Icons | 1.11.3 | Icon font |
| Google Fonts | — | Syne, DM Sans, DM Mono |

---

## Project Structure

```
bootstrap5-exercises.html   ← everything in one file
README.md
```

The single HTML file contains:

- Custom CSS variables and component styles in `<style>`
- A sticky sidebar navigation for jumping between modules
- 19 `<section>` elements, one per module
- Live demo markup and syntax-highlighted code blocks per exercise
- Bootstrap JS bundle loaded before `</body>` for plugin support

---

## Sass Customization (Module 19)

Module 19 covers how to move beyond the CDN and compile your own Bootstrap build with Sass:

```bash
npm init -y
npm install bootstrap sass
```

Then create `scss/custom.scss`, override variables before importing Bootstrap, and compile:

```scss
// Override before importing
$primary: #e84d1c;
$border-radius: 0.75rem;

@import "../node_modules/bootstrap/scss/bootstrap";
```

```bash
# Add to package.json scripts
"build-css": "sass scss/custom.scss dist/css/custom.css"

npm run build-css
```

---

## Design

The page uses a custom editorial theme on top of Bootstrap:

- **Fonts:** Syne (headings), DM Sans (body), DM Mono (code/labels)
- **Palette:** warm paper background (`#f5f2eb`), ink dark (`#0d0d0d`), accent red-orange (`#e84d1c`), accent blue (`#1c6fe8`)
- **Layout:** full-width masthead, sticky 2-column layout (sidebar + main content) on large screens

---

## License

This project is intended for educational use. Bootstrap is licensed under the [MIT License](https://github.com/twbs/bootstrap/blob/main/LICENSE).

