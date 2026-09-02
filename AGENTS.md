# AGENTS.md

## Project
Static website for صيدلية زهرة الشفاء. Plain HTML/CSS/JS — no build step, no framework, no package manager.

## Structure
- `index.html` — the entire site (single page)
- `images/` — product photos, named after the product
- `logo.png`, `hero-image.png` — brand assets

## Rules
- Do not preserve backward compatibility. Remove obsolete code instead of adding fallbacks.
- Choose the simplest implementation that meets current requirements. No speculative abstractions.
- Grow the site in layers. Never trade a working page for unfinished complexity.
- Keep concerns separated: structure in HTML, styling in CSS, behavior in JS.
- Prefer established libraries over reimplementing common functionality.
- Do not introduce a build step, framework, or npm packages without asking first.

## Conventions
- Arabic-first: `<html lang="ar" dir="rtl">`. All UI text in Arabic.
- Product images live in `images/` and are referenced with relative paths.
- Test by opening `index.html` directly in the browser — there is no dev server.
- Check the layout on mobile width before considering a task done.

## Product cards
- Copy the existing card markup exactly: image, name, price, description — same order, same classes.
- Every card needs a unique `id`. Search the file for the id before adding it.
- Products are grouped by `data-cat` inside `.product-grid`. Moving a card means moving the full block, not editing categories.
- After any card edit, verify opening and closing `<div>` counts still match.
- Image filename must match the product name and live in `images/`.