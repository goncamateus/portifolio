# AGENTS.md — Portfolio Repo

## Deploy
- GitHub Pages via GitHub Actions — `.github/workflows/deploy.yml`
- Push to `main` triggers auto-deploy
- No build step. No npm. No frameworks. Browser-native only.
- **For root URL (`/`)**: Name the repo `<username>.github.io` exactly.
- **For subpath (`/portfolio/`)**: Any other repo name works. All paths are relative so both work without code changes.

## Stack
- Vanilla HTML/CSS/JS. No package.json. No bundler.
- Edit files directly.

## Dev
- Chrome blocks `file://` protocol on Linux. Use local server:
  `python3 -m http.server 8000` → `http://localhost:8000`
- Firefox works with `file://`, but prefer local server for consistency.

## Path Rules
- All paths relative. CSS: `../css/style.css`. Pages: `./about.html`.
- Shared nav/header duplicated in each HTML file. No templating engine.

## Style
- System color scheme via `prefers-color-scheme` + CSS variables.
- Mobile-first responsive layout.

## Assets
- Placeholder images via `https://via.placeholder.com/` or inline SVG.
- Real assets go in `assets/images/`, `assets/fonts/`, and `assets/cv/`.

## Page Structure (Bilingual)
- `index.html` — auto-detects browser language, redirects to `/en/` or `/pt/`
- `en/index.html` — English landing
- `en/pages/about.html` — English bio
- `en/pages/publications.html` — English publications
- `en/pages/cv.html` — English CV
- `en/pages/projects.html` — English projects
- `pt/index.html` — Portuguese landing
- `pt/pages/about.html` — Portuguese bio
- `pt/pages/publications.html` — Portuguese publications
- `pt/pages/cv.html` — Portuguese CV
- `pt/pages/projects.html` — Portuguese projects
- `css/style.css` — shared styles
- `js/main.js` — shared scripts (mobile nav, theme toggle)

## Path Rules
- All paths relative. From `en/pages/about.html`: `../../css/style.css`, `../index.html`
- Shared nav/header duplicated in each HTML file. No templating engine.
- Language toggle in nav links to corresponding page in other language.
