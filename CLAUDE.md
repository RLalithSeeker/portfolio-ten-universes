# Portfolio — Ten Universes

Static single-file portfolio. `index.html` only (Tailwind precompiled inline + Google Fonts). No build step. Live: https://portfoliopush.vercel.app · repo RLalithSeeker/portfolio-ten-universes.

## Structure (all copy is data-driven JS consts in index.html)
- `projects[]` — 10 project cards
- `THEMES` / `UNAME` / `VIBE` — the 10 design universes (colors + fonts)
- `HERO[n]` — per-universe hero markup
- `ABOUT_COPY[n]` — `{ h: headline, p: [engineer, local-first, stack, location, personal] }`
- `PRIN[n]` — 8 ideology rules per universe (the "How I work" section)
- `PHIL[n]` / `PROJ[n]` — philosophy + project renderers
- Modes: auto (`STORY[]` cinematic scroll) + manual (X = world slider, Y = depth glance/brief/deep)

## Rules
- Keep the "I don't write code / I write intent" headline on **≤2 of 10 worlds** — owner dislikes it repeating on every scroll. The other worlds carry distinct true facets (ships-complete, free-tools-first, research-driven taste, India-first, never-guess-a-bug, privacy).
- Content source = owner's documented ideology (free-tools-first, demo→build, research-first taste, never-guess-debug, log-everything, local-first, ships the boring 20%, self-taught full-stack, India-first).
- Drop-caps: use a clean font (Space Grotesk), **never** the Playfair `--font-display` — ornamental glyphs + tight line-height clip and read as a curve.
- Validate the inline script parses before deploy (`new Function` over the `<script>` body).

## Deploy
`vercel --prod --yes` from this folder (Vercel project `_portfolio_push`, linked, static). Uploads the **whole working tree** (not git) → remove `*.bak`/secrets first or they go public.
