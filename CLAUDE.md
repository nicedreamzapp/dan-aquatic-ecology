# Dan's Ecology Project — Working Notes for Claude Code

You are assisting **Dan Close**, a friend of Matt's, on the public-facing portfolio for his **HSU Master's Thesis Project** at **Cal Poly Humboldt · Marine Sciences**. These are self-contained, single-page educational web visualizations about aquatic and restoration ecology — pitched at a thesis defense / committee / outreach audience, scientifically credible, and runnable from a double-click on `index.html` (no build step, no dependencies). Always credit "By Dan Close · HSU Master's Thesis · Cal Poly Humboldt Marine Sciences" anywhere we surface authorship.

## What lives in this folder

- `index.html` — landing hub with four animated cards linking the four features below.
- `dan-aquatic-ecology.html` — "Scale of the Sea" hero (cycling 10-step log scale, click any tick to jump) → vertical scroll depth tour with click-to-learn modals per zone, hover labels on every organism, "🤿 Take a Dive" auto-tour, and an end-of-page quiz.
- `dan-restoration-ecology.html` — "Aquatic Restoration Ecology" — fullscreen Ken-Burns slide deck with arrow-key/click-edge navigation, auto-play, fullscreen.
- `dan-freshwater-restoration.html` — companion freshwater slide deck in the same family (rivers, beavers, dam removal, wetlands, urban green infra).
- `dan-scientific-diving.html` — long-form magazine-style narrative on the role of scientific diving in marine restoration ecology. 13 chapters, mix of confirmed Wikimedia photos and inline-SVG diver illustrations, scroll-progress, fade-in-on-scroll, TOC drawer.

Every page has a built-in **🎧 narration module** (bottom-right floating button) that uses Web Speech API. It auto-prefers Microsoft natural neural voices (Edge), then macOS premium female voices (Samantha/Ava/Allison), and warns the user if no Natural voice is installed.

## Design language (preserve when editing)

- Dark ocean palette: deep `#021024`, mid `#052a52`, shallow `#0a4d8c`, surface `#2a8fc9`, sun `#ffe9a8`, accent cyan `#6ee7ff`, ink `#f4fbff`.
- Sans stack: `-apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif`.
- Fluid typography: `clamp(min, vw, max)` everywhere — never hardcoded px for headlines.
- Motion is core: `swimL2R` / `swimR2L` / `bob` / `spin` / `wiggle` keyframes; bubbles rising; sun shimmer; Ken Burns zoom on slides.
- All organisms are inline SVG — no external images, no raster art. Stroke-and-fill style with cartoon highlights.
- Every page must remain a single HTML file with inline CSS and JS so Dan can email/AirDrop it.

## How to help Dan

- Default to **additive, low-risk edits** — adding a new depth band, fixing a typo, adjusting a color — over rewrites.
- If you add a new organism, match the existing SVG style (simple shapes, 1.5–3px strokes, the page's palette).
- Keep scientific accuracy — orders of magnitude on the depth scale, real taxa names, correct trophic relationships. If unsure, say so rather than inventing.
- Preserve the no-build constraint. No npm, no bundlers, no CDN dependencies unless Dan explicitly wants them.
- Mobile must work — there's already a `@media (max-width: 700px)` block; keep it healthy.
- When making a "way better" pass: think clarity of the science story first, polish of the motion second, copy third.

## Useful commands

```bash
open index.html                      # preview the hub
open dan-aquatic-ecology.html        # preview a single page
python3 -m http.server 8088          # serve folder if a file:// quirk shows up
```

## Out of scope unless asked

- Backends, databases, frameworks
- Adding analytics, fonts, or trackers
- Renaming the existing files (other tools may link to them)
