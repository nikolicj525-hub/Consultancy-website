# EU Consultancy Website

A simple, static, responsive website for an EU regulatory watch &amp; alignment consultancy. No build tools or backend required — just plain HTML, CSS and a touch of JS.

The site is centered on four EU regulatory files:

- **EES / ETIAS** — the EU border entry/exit and travel authorisation regime
- **EUDR** — the EU Deforestation Regulation (2023/1115)
- **PPWR** — the Packaging and Packaging Waste Regulation (2025/40)
- **IAA** — the Industrial Accelerator Act proposal (COM(2026) 100)

## Structure

```
index.html               Home page — dossier overview + positioning
regulatory-watch.html    The core page: status, timeline & sources for all 4 files
services.html            Monitoring, alignment & advisory services
about.html               About / approach
contact.html             Contact info + form (not yet wired up)
css/style.css            All styling
js/main.js               Mobile nav toggle
```

## Keeping the Regulatory Watch page current

`regulatory-watch.html` is the centerpiece of the site and is **manually maintained** —
there is no live feed or backend pulling from EUR-Lex/EP OEIL automatically. Each dossier
card has a "Latest development" paragraph, a timeline, and source links; update these as
each file progresses, and bump the "Last reviewed" date near the top of the page. If you
later want real-time or automated tracking (e.g. polling EUR-Lex/OEIL and emailing alerts),
that's a separate backend project, not something a static site can do on its own.

Current status captured as of **17 September 2026**:

| File | Status |
|---|---|
| EES | Fully operational since 10 Apr 2026 |
| ETIAS | Not yet launched; Commission expects Q4 2026, no confirmed date |
| EUDR | Applies from 30 Dec 2026 (large/medium) / 30 Jun 2027 (small) after Dec 2025 postponement |
| PPWR | General application began 12 Aug 2026; more requirements phase in through 2040 |
| IAA | Proposal from 4 Mar 2026; EP joint-committee draft report presented 8 Sep 2026 |

## Before publishing, customize:

1. **Business name** — replace every `[Your Consultancy Name]` (in the nav, page titles, and footers of all 5 pages).
2. **Contact details** — in `contact.html`, replace `[your-email@example.com]`, `[+xx xxx xxx xxxx]` and `[City, Country]` with real details.
3. **Regulatory Watch content** — verify/refresh the four dossier cards in `regulatory-watch.html` against the linked official sources before publishing, since legislative timelines shift.
4. **Contact form** — the form in `contact.html` doesn't send anywhere yet. Easiest options:
   - [Formspree](https://formspree.io) — add an endpoint, no backend needed.
   - Netlify Forms — if you host on Netlify, add `netlify` and `data-netlify="true"` attributes to the `<form>`.
   - Or just remove the form and keep the plain email link.
5. **Colors/branding** — edit the CSS variables at the top of `css/style.css` (`--eu-blue`, `--eu-gold`, etc.) if you want a different look.

## Running locally

No build step needed — just open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Deploying

Any static host works: GitHub Pages, Netlify, Vercel, Cloudflare Pages. Just point it at this folder.
