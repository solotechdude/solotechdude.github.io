# solotechdude

Single-page personal brand site for **solotechdude** — dual-platform operator running generative AI bets in freight and hospitality, with shipped Chrome extensions as the distribution wedge.

Live: **https://solotechdude.github.io**

## Layout

```
.
├── index.html              # Site (copy + styles + Chrome user counts)
├── favicon.ico             # Tab icons (kept at root for browsers)
├── favicon.png
├── apple-touch-icon.png
├── assets/
│   └── brand/              # Logo mark used on the site
│       ├── logo.svg
│       ├── logo.png
│       ├── logo-512.png
│       └── favicon-32.png
└── docs/                   # Notes / plans (not deployed content)
```

Site-critical files stay at the repo root for GitHub Pages. Marketing exports (`creatives/` — X headers, QR codes) stay on your machine only and are gitignored.

## Edit copy

All page content lives in `index.html`:

- **Hero** — brand name, operator lede, Email me CTA
- **Platforms** — Freight AI and Hostline (stealth; no public URLs)
- **Shipped products** — Chrome extensions grouped under **Freight distribution** (BestAmazonBooker, FactoRight, LockTheLoad) and **General tools** (TubePack, TabMD, Unlimited Shortcuts, X-Vault); domains + Chrome Web Store links
- **Clients** — contractor client list
- **Contact** — `solotechdude@gmail.com`

Platform bets have no public URLs on this page. Chrome Web Store **user counts** load from Shields.io at runtime (`data-chrome-id` on each product). No backend required.

No build step.

## Local preview

```bash
python3 -m http.server
```

Then visit `http://localhost:8000`.

## Deploy

Push to `main` on `solotechdude/solotechdude.github.io`. Pages serves from the repo root.
