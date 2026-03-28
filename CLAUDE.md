# CLAUDE.md — ianbeatty.com

## Project overview

Personal website for Ian D. Beatty — a computational physicist pivoting into biosecurity research. Built with Jekyll, hosted on GitHub Pages at `ianbeatty.com`.

## Tech stack

- **Jekyll** via the `github-pages` gem (must stay GitHub Pages compatible)
- **No Ruby installed locally** — all Jekyll build/serve happens through Docker
- No JavaScript frameworks. Minimal JS only (e.g., dark mode toggle if added later).
- Pages authored in Markdown. Custom CSS in `assets/css/custom.css`.
- Base theme: "Minimal" with CSS overrides.

## Local development

```sh
docker compose up
# Site at http://localhost:4000
# LiveReload on port 35729
```

Do NOT suggest `bundle exec jekyll serve` or any command requiring a local Ruby install.

## Site structure

```
index.md          — Landing page (visually distinct "calling card" layout)
research.md       — Biosecurity & AI (lead) + Physics Education Research (secondary)
background.md     — Narrative: through-line, the pivot, technical skills
contact.md        — Email + LinkedIn + conversation welcome
publications.md   — Full PER publication list (NOT in main nav)
_layouts/default.html — Base layout with header nav + footer
_config.yml       — Jekyll config (url: https://ianbeatty.com, baseurl: "")
assets/css/custom.css — All style overrides
CNAME             — Contains exactly: ianbeatty.com
```

## Navigation

Header nav (every page): **Research | Background | Contact**

"Ian D. Beatty" in the header links to the landing page.

Publications page is NOT in the main nav — it's linked from the Research page.

## Style rules

- Clean sans-serif (system font stack)
- Generous whitespace, muted color palette, subtle accent for links
- No bright colors. No sidebar, widgets, blog feed, or social icons.
- Landing page headshot: circular/rounded, not too large
- PER section on research page should feel visually secondary to Biosecurity section
- Footer: "© 2026 Ian D. Beatty" (optionally + "Built with Jekyll")

## What to avoid

- No blog engine or post infrastructure
- No analytics or tracking
- No comments system
- No "Teaching" page or presentations list
- No JavaScript frameworks
- Don't add Ruby to the local dev workflow

## Known placeholders (marked with TODO in source)

- Headshot image
- LinkedIn URL
- Google Scholar URL
- Biosecurity publications list
- CV PDF file (`assets/cv.pdf`)

## Deployment

GitHub Pages deploys from the `main` branch root. The repo is `ibeatty/ibeatty.github.io`.
