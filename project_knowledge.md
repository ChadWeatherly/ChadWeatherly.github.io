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
1. **Hero / About** — Dual tags (PhD Candidate · CS/AI  +  Automation & Software Engineer), name, bio in bulleted list, formal photo (chad.jpeg), lab affiliation (**Continual Edge AI Lab** under Dr. Sen Lin, linked to https://slin70.github.io/terms/)
2. **Research / Active Projects** — Three general cards describing research themes (latent-space prediction for AD, continual AD under industrial drift, foundation models on the edge). Deliberately free of specific model names, architectures, or results.
3. **Publications** — MET Project paper (Open Forum Infectious Diseases, 2022). ECCV 2026 submission is intentionally NOT listed while under review.
4. **Projects / Portfolio** — Three consulting cards: X9 Inc, Wellmatics (with impact metrics), OAKCameraQC
5. **Skills** — Six groups: Languages (Python, Rust, C/C++, C#, R, SQL), ML/AI, Web/Backend, Hardware/Edge, Infrastructure, Tools
6. **Contact** — Email, GitHub, LinkedIn links

### Corrected Lab Affiliation
- Previously (incorrectly) said: Pattern Analysis Lab under Dr. Ioannis Kakadiaris
- Correct: **Continual Edge AI Lab (CEAL)** under Dr. Sen Lin (https://slin70.github.io/terms/)
- Chad was previously in the Computational Biomedicine Lab (under Kakadiaris) from June 2021 – Dec 2022, which is where the MET Project paper came from. Main PhD advisor since Jan 2024 is Dr. Sen Lin.

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
- Buy a custom domain and point it at GitHub Pages (user asked about this 2026-04-24)
- Add a blog/writing section if Chad starts publishing posts
- Add a CV/resume download link (PDF)
- Consider adding a favicon and social meta (og:image, twitter:card)
- Set up weekly scheduled task for auto-updates
- Add Google Analytics or Plausible for visitor tracking (optional)

## Changelog
- **2026-04-24** — Redesigned hero: added formal photo (`chad.jpeg`), dual role tags, bulleted bio. Corrected lab affiliation to CEAL / Dr. Sen Lin with link to https://slin70.github.io/terms/. Generalized Active Projects to three thematic cards. Added SQL to Languages. Added impact metrics to Wellmatics card. Nav logo updated to "chad weatherly." Note: ECCV 2026 submission intentionally NOT mentioned anywhere on the site while under review.
