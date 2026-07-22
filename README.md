# Personal-Portfolio-website
Personal portfolio website built with React 18 and Vite, featuring client-side routing, persistent dark mode, a typewriter hero effect, an accessible validated contact form, and a fully responsive design following modern web accessibility best practices.
Personal portfolio website built for the **Front-End Programming** final project.

## Framework
**React 18 + Vite 5** with React Router v6
**You must have installed node js as well**
## Features
- **3 pages:** Home, About, Contact — linked via React Router
- **Dark mode toggle** that persists in `localStorage` and respects `prefers-color-scheme`
- **Typewriter effect** on the Home hero cycling through role descriptions
- **Fully validated contact form** with per-field error messages, `aria-invalid`, `aria-describedby`, and a success state
- **Accessible:** skip-to-content link, semantic HTML (`<header>`, `<nav>`, `<main>`, `<footer>`, `<aside>`), ARIA labels, visible focus indicators, AA color contrast
- **Responsive:** mobile hamburger menu, fluid grid layouts, `clamp()` typography
## Quick start
```
# 1. Install dependencies
open VS code and open a terminal, then npm install
# 2. Start the dev server
npm run dev
```
It's going to apper a link, copy and open it [http://localhost:5173](http://localhost:5173) in your browser.
```
# Build for production
npm run build
# Preview the production build locally
npm run preview
```
## Project structure
```
mau-portfolio/
├── index.html               ← entry point (theme flash prevention script here)
├── vite.config.js
├── package.json
└── src/
    ├── main.jsx             ← React root
    ├── App.jsx              ← Router + theme state
    ├── index.css            ← All styles (CSS variables, light/dark tokens, components)
    ├── components/
    │   ├── Nav.jsx          ← Sticky nav with hamburger and dark mode toggle
    │   └── Footer.jsx
    └── pages/
        ├── Home.jsx         ← Hero + Project cards + Skills snapshot
        ├── About.jsx        ← Bio + Skills grouped by category + Languages
        └── Contact.jsx      ← Validated form with ARIA error/success states
- Connect the repo on Vercel/Netlify — it auto-detects Vite and sets the correct build command (`npm run build`) and output directory (`dist`)
## Accessibility notes
- Run a Lighthouse audit in Chrome DevTools → Lighthouse tab to verify 100 on Accessibility
- All interactive elements are reachable with Tab / Enter / Space
- Color contrast ratios: text on bg ≥ 10:1, links ≥ 5.7:1 (both AA/AAA)
- Dark mode keeps the same contrast ratios
