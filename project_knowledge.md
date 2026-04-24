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
4. **Projects / Portfolio** — Two consulting cards (X9 Inc, Wellmatics). Both focused purely on X-ray inspection work. No hardware specifics, no fee/licensing language.
5. **Skills** — Four groups: Languages, Frameworks & Libraries, Research Interests, Hardware & Deployment. Model architectures intentionally NOT listed as skills (YOLO, DINO, PatchCore, I-JEPA removed). Flask kept; REST APIs and ZeroMQ removed per user note that only Flask of those was well-known.
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
- **2026-04-24** — Redesigned hero: added formal photo (`chad.jpeg`), dual role tags, bulleted bio. Corrected lab affiliation to CEAL / Dr. Sen Lin with link to https://slin70.github.io/terms/. Generalized Active Projects to three thematic cards. Added SQL to Languages. Nav logo updated to "chad weatherly." Note: ECCV 2026 submission intentionally NOT mentioned anywhere on the site while under review.
- **2026-04-24 (round 2)** — Enlarged hero photo (340px wide, portrait 4:5 aspect). Rewrote hero bio in first person to feel less CV-like. Dropped the "Continual Edge AI Lab" meta-row chip (lab is already mentioned in bio). Consulting section pared down to two cards (X9 + Wellmatics), focused only on X-ray inspection work; removed hardware specifics, fee/licensing mentions, and the OAKCameraQC card. Skills: trimmed model architectures (YOLO/DINO/PatchCore/I-JEPA removed), consolidated web tools to just Flask, added a "Research Interests" group, collapsed Hardware+Infrastructure+Tools into a single "Hardware & Deployment" group.
