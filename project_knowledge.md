# ChadWeatherly.github.io — Project Knowledge

## Overview
Personal academic + portfolio website for Chad Weatherly, deployed to GitHub Pages.

## GitHub Repository
- **Repo:** `ChadWeatherly/ChadWeatherly.github.io`
- **URL:** https://chadweatherly.github.io
- **Visibility:** Public

## Site Structure
Single-file architecture — everything lives in `index.html` (HTML + embedded CSS + JS). No build tools, no dependencies.

### Sections (current order, as of 2026-05-26)
1. **Hero / About** — Dual tags (PhD Candidate · CS/AI  +  Automation & Software Engineer), name, bio in bulleted list, formal photo (chad.jpeg), lab affiliation (**Continual Edge AI Lab** under Dr. Sen Lin, linked to https://slin70.github.io/terms/)
2. **Research / Active Projects** — Three general cards describing research themes (latent-space prediction for AD, continual AD under industrial drift, foundation models on the edge). Deliberately free of specific model names, architectures, or results.
3. **Projects / Portfolio** — Two consulting cards (X9 Inc, Wellmatics). Both focused purely on X-ray inspection work. No hardware specifics, no fee/licensing language.
4. **Skills** — Four groups: Languages, Frameworks & Libraries, Research Interests, Hardware & Deployment. Model architectures intentionally NOT listed as skills (YOLO, DINO, PatchCore, I-JEPA removed). Flask kept; REST APIs and ZeroMQ removed per user note that only Flask of those was well-known.
5. **Contact** — Email, GitHub, LinkedIn links
6. **Publications** — Two subsections (Pre-prints, Published Work), papers as `pub-card`s with bolded `Weatherly C`, venue/year metadata, and a clickable DOI/arXiv link. Now lives at the BOTTOM of the page — reads as the reference list. Section was moved here from position #3 on 2026-05-26.

### Publications policy (confirmed 2026-05-26)
- **Pre-prints subsection**: ONLY arXiv (or similar) papers Chad has self-posted publicly. Self-posted arXiv preprints are public-by-definition and OK to list, even pre-review.
- **Published Work subsection**: peer-reviewed venue acceptance. Must have a DOI or official venue URL.
- **Do NOT list** papers that are submitted to a venue but not publicly posted anywhere. Submitted-and-under-review-only papers stay off the site. (E.g., the ECCV 2026 submission referenced in the prior changelog is still NOT listed — it doesn't have an arXiv ID.)

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
### Weekly auto-update scheduled task (set up 2026-05-26)
- **Task ID:** `weekly-website-papers-update`
- **Schedule:** Every Monday at 9:00 AM local
- **Task file:** `/Users/chadw/Documents/Claude/Scheduled/weekly-website-papers-update/SKILL.md`
- **What it does:** Checks Google Scholar, ORCID, and arXiv for new Chad Weatherly papers, classifies each (Pre-print vs Published per the policy above), and stages edits into `index.html` at the top of the appropriate `pub-list`. If a Pre-print picks up a DOI between runs, it moves the entry from Pre-prints → Published Work instead of duplicating.
- **Workflow:** Stage locally, **do NOT auto-commit or push**. Chad reviews `git diff` and pushes himself.
- **Data sources:**
  - Google Scholar: https://scholar.google.com/citations?user=1Dk8HCwAAAAJ&hl=en
  - ORCID: 0000-0002-1290-8695 (note: JS-rendered — may need Chrome MCP for full fidelity)
  - arXiv author search for "Chad Weatherly" / "C. Weatherly"

### General update process
- Edit `index.html` → review diff → `git commit` → `git push` → Pages auto-deploys
- Pre-print card template and Published Work card template are documented in the scheduled task prompt for reference.

## Current Status
- [x] index.html created with all sections
- [x] project_knowledge.md created
- [x] Page reordered — Publications moved to bottom (2026-05-26)
- [x] Pre-prints subsection added with arXiv paper 2605.24251 (2026-05-26)
- [x] Weekly scheduled task `weekly-website-papers-update` created (2026-05-26)
- [ ] Chad to review the staged changes and `git push` to go live
- [ ] Git repo initialized and pushed to GitHub
- [ ] Site verified live at https://chadweatherly.github.io

## To-Do (Future)
- Buy a custom domain and point it at GitHub Pages (user asked about this 2026-04-24)
- Add a blog/writing section if Chad starts publishing posts
- Add a CV/resume download link (PDF)
- Consider adding a favicon and social meta (og:image, twitter:card)
- Add Google Analytics or Plausible for visitor tracking (optional)

## Changelog
- **2026-04-24** — Redesigned hero: added formal photo (`chad.jpeg`), dual role tags, bulleted bio. Corrected lab affiliation to CEAL / Dr. Sen Lin with link to https://slin70.github.io/terms/. Generalized Active Projects to three thematic cards. Added SQL to Languages. Nav logo updated to "chad weatherly." Note: ECCV 2026 submission intentionally NOT mentioned anywhere on the site while under review.
- **2026-04-24 (round 2)** — Enlarged hero photo (340px wide, portrait 4:5 aspect). Rewrote hero bio in first person to feel less CV-like. Dropped the "Continual Edge AI Lab" meta-row chip (lab is already mentioned in bio). Consulting section pared down to two cards (X9 + Wellmatics), focused only on X-ray inspection work; removed hardware specifics, fee/licensing mentions, and the OAKCameraQC card. Skills: trimmed model architectures (YOLO/DINO/PatchCore/I-JEPA removed), consolidated web tools to just Flask, added a "Research Interests" group, collapsed Hardware+Infrastructure+Tools into a single "Hardware & Deployment" group.
- **2026-05-26** — Restructured page: moved Publications section from position #3 to the BOTTOM of the page (after Contact). Updated navbar order to match. Added a `Pre-prints` subsection inside Publications with new CSS (`.pub-subsection-title`, `.pub-list`). Section title renamed from "Published Work" to "Papers" with two subheadings underneath. Added the arXiv preprint *Rethinking Continual Anomaly Detection on the Edge: Benchmarking Under Realistic Industrial Conditions* (arXiv:2605.24251, May 2026) to the Pre-prints subsection. Confirmed publications policy: arXiv-self-posted preprints OK to list; submitted-but-not-posted papers stay off the site. Created weekly Monday-9am scheduled task `weekly-website-papers-update` to auto-stage future paper updates.
