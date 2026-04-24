# ChadWeatherly.github.io — Project Knowledge

## Overview
Personal academic + portfolio website for Chad Weatherly, deployed to GitHub Pages.

## GitHub Repository
- **Repo:** `ChadWeatherly/ChadWeatherly.github.io`
- **URL:** https://chadweatherly.github.io
- **Visibility:** Public

## Site Structure
Single-file architecture — everything lives in `index.html` (HTML + embedded CSS + JS). No build tools, no dependencies.

### Sections
1. **Hero / About** — Name, one-liner, bio, lab affiliation (Pattern Analysis Lab, UH, under Kakadiaris)
2. **Research** — Two cards: LeJEPA-AD and Continual AD Benchmarking, with GitHub links
3. **Publications** — Single paper (MET Project, Open Forum Infectious Diseases, 2022)
4. **Projects / Portfolio** — Three consulting cards: X9 Inc, Wellmatics, OAKCameraQC
5. **Skills** — Six groups: Languages, ML/AI, Web/Backend, Hardware/Edge, Infrastructure, Tools
6. **Contact** — Email, GitHub, LinkedIn links

### Design Decisions
- **Layout:** Top navbar (dark), light body, teal accent (`#0d9488`)
- **Typography:** Inter for body, JetBrains Mono for code/DOI
- **Dark/Light toggle:** Saves to localStorage, respects `prefers-color-scheme`
- **Mobile:** Hamburger menu at 768px breakpoint, single-column card layout
- **Animations:** Intersection Observer fade-in on scroll, active nav highlighting
- **No frameworks:** Vanilla HTML/CSS/JS — loads fast, zero dependencies beyond Google Fonts

## Deployment
- GitHub Pages serves from the `main` branch root
- Push to `main` triggers automatic deployment
- `gh` CLI used for repo creation and management

## Maintenance Plan
- Chad wants a **weekly scheduled task** to auto-update the site
- Potential updates: new publications, research progress, project additions
- Update process: edit `index.html` → commit → push → Pages auto-deploys

## Current Status
- [x] index.html created with all sections
- [x] project_knowledge.md created
- [ ] Git repo initialized and pushed to GitHub
- [ ] Site verified live at https://chadweatherly.github.io

## To-Do (Future)
- Add a blog/writing section if Chad starts publishing posts
- Add a CV/resume download link (PDF)
- Consider adding a favicon and social meta (og:image, twitter:card)
- Set up weekly scheduled task for auto-updates
- Add Google Analytics or Plausible for visitor tracking (optional)
