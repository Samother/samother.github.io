# cedricbuche.github.io

Static site migrated from `web.enib.fr/~buche`, new design (no build step, no framework).

## Deploy

1. Copy every file in this folder into the root of your `cedricbuche/cedricbuche.github.io` repo (keep the `assets/` folder as-is).
2. Commit and push to the `main` (or `master`) branch — GitHub Pages will serve it automatically.
3. Add your photo at `assets/img/buche_pepper.png` (referenced from `contact.html`; the page degrades gracefully if it's missing).

## Structure

- `index.html` — home / bio / positions / degrees
- `research.html` — research statement + 16 project write-ups
- `publications.html` — full bibliography (117 entries), rendered from `assets/publications-data.js`, filterable by category
- `supervision.html` — PhD / postdoc / engineer / master supervision, in progress & completed
- `grants.html` — grants and industrial contracts
- `collaboration.html` — international collaborations by country
- `teaching.html` — courses taught
- `robobreizh.html` — links out to the RoboBreizh team site
- `contact.html` — email, LinkedIn, CV links, photo
- `assets/style.css` — shared design system (see below)
- `assets/main.js` — mobile nav toggle, active-link highlighting, publication filter

## Editing content

- To add/edit a publication, edit the `PUBLICATIONS` array in `assets/publications-data.js` — each entry is a plain object (`cat`, `y`, `a`, `t`, `v`, `b`, `l`). No rebuild needed.
- Everything else is plain HTML; each page repeats the same nav block at the top — update all pages if you add/rename a nav item.

## Design notes

The look is a "field notebook of a robotics lab": graph-paper background, ink-navy type, a teal/amber accent pair, `Fraunces` for headings, `Inter` for body text, `IBM Plex Mono` for data (years, ranks, venues). The homepage hero includes a small SVG diagram of the three research pillars (learning / anticipating / human-in-the-loop) converging on "adaptive behaviour" — a nod to how the research overview itself is described. Colors and type are defined as CSS custom properties at the top of `assets/style.css` if you want to retheme.
