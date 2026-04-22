# Mateus Gonçalves Machado — Portfolio

[![Deploy to GitHub Pages](https://github.com/goncamateus/portifolio/actions/workflows/deploy.yml/badge.svg)](https://github.com/goncamateus/portifolio/actions/workflows/deploy.yml)
[![Site](https://img.shields.io/badge/live-site-coral)](https://goncamateus.github.io/portifolio/)

> PhD Student in Reinforcement Learning & Robotics

A bilingual, static portfolio built with vanilla HTML/CSS/JS. No frameworks, no build step — just clean, hand-crafted code.

## Features

- **Bilingual** — Auto-detects browser language (EN/PT-BR) with manual toggle
- **Dark mode** — Respects `prefers-color-scheme` with warm coral accents
- **CV page** — Transcribed professional/academic experience with PDF download
- **Publications** — Papers with abstracts and direct links
- **Projects** — GitHub repos from `phd_things` with descriptions
- **Responsive** — Mobile-first layout with collapsible nav
- **Fast** — Zero dependencies, zero JS frameworks

## Tech Stack

| Layer | Tech |
|-------|------|
| Markup | Vanilla HTML5 |
| Styling | Vanilla CSS3 (custom properties, flexbox, grid) |
| Scripts | Vanilla JS (mobile nav toggle) |
| Deploy | GitHub Actions → GitHub Pages |

## Structure

```
├── index.html                 # Language auto-detect redirect
├── en/                        # English pages
│   ├── index.html
│   └── pages/
│       ├── about.html
│       ├── publications.html
│       ├── cv.html
│       └── projects.html
├── pt/                        # Portuguese pages
│   ├── index.html
│   └── pages/
│       ├── about.html
│       ├── publications.html
│       ├── cv.html
│       └── projects.html
├── css/style.css              # Shared styles, warm coral theme
├── js/main.js                 # Mobile nav toggle
├── assets/
│   ├── images/                # Avatar, placeholders
│   └── cv/                    # PDF CV
└── .github/workflows/deploy.yml
```

## Local Development

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

Push to `main` — GitHub Actions handles the rest.

## License

© 2026 Mateus Gonçalves Machado
