# solotechdude — Premium Resume Page Design

**Date:** 2026-07-26  
**Status:** Approved (conversation)  
**Deploy target:** GitHub Pages (`solotechdude.github.io`)

## Goal

A single-page personal brand / resume site for **solotechdude** — solopreneur with enterprise engineering background, now building products for trucking, government contracting, and related tools. Free hosting on GitHub Pages with free `username.github.io` domain.

## Approach

**Single static HTML page** — one `index.html` with embedded or adjacent CSS (and minimal CSS-only motion). No build step. Public repo root publishes to `https://solotechdude.github.io`.

## Content model

Placeholder contact links are editable after ship.

| Section | Purpose | Content |
| --- | --- | --- |
| Hero | Brand-first first viewport | Dominant **solotechdude**; one supporting sentence about building tools for trucking, gov contracting, and operators; one text CTA (Contact) |
| Now | Current focus | Short statement: developing own products and tools (trucking, government contracting, other) |
| Selected experience | Credibility | Sharp list (not cards): JPMorgan Chase, FCC, Walmart Labs, College Board, Comcast, AEP — company names large; optional light role lines as placeholders |
| Contact | Next step | Email / LinkedIn / GitHub as large plain text links |

No stats strips, no card grids, no floating badges.

## Visual system

**Tone:** Cool industrial — graphite field, sharp white type, electric cyan accent only for links/hover.

**Typography**

- Display: Syne (Google Fonts) — brand and section titles
- Body: IBM Plex Sans — supporting copy and meta
- Brand size: `clamp(4rem, 12vw, 8rem)`
- Section titles: ~2.5–3.5rem
- Body: 1.125–1.25rem
- Labels: uppercase, tracked

**Color (CSS variables)**

- `--bg: #0c0e10`
- `--ink: #f2f2f0`
- `--muted: #8a9199`
- `--accent: #3de0c5`
- `--rule: rgba(242, 242, 240, 0.12)`

**Layout**

- Max width ~1100px, large horizontal padding
- Large vertical section spacing
- Hairline 1px rules between sections
- Sharp edges only (`border-radius: 0`)
- No cards, no pill buttons

**Atmosphere**

- Subtle diagonal grain or fine grid wash over `--bg` (CSS, no image dependency required)
- Not flat black; not purple gradients

**Motion (CSS only, 2–3 intentional)**

1. Staggered fade / slide-up on load: hero → now → experience → contact
2. Link hover: accent color + underline draw
3. Optional: soft accent hairline on section enter (prefers-reduced-motion respected)

## Technical constraints

- Static assets only (HTML/CSS/JS as needed)
- Google Fonts via stylesheet link (acceptable for Pages)
- Mobile: stack cleanly; brand still hero-scale but clamped
- Accessibility: semantic headings, sufficient contrast, `prefers-reduced-motion`
- Repo name for user site: `solotechdude.github.io`; publish from `main` / root

## Out of scope

- Custom domain purchase
- Blog, CMS, backend, contact form server
- Project case-study subpages (can add later as project Pages sites)

## Success criteria

- First viewport reads as one composition with **solotechdude** as the brand signal
- Feels premium: large type, large space, sharp geometry
- Live on GitHub Pages with zero monthly hosting cost
- Copy/placeholders easy to edit in one file
