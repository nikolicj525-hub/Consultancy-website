# EU Consultancy Website

A simple, static, responsive website for an EU regulatory compliance consultancy. No build tools or backend required — just plain HTML, CSS and a touch of JS.

## Structure

```
index.html      Home page
services.html   Detailed services
about.html      About / approach
contact.html    Contact info + form (not yet wired up)
css/style.css   All styling
js/main.js      Mobile nav toggle
```

## Before publishing, customize:

1. **Business name** — replace every `[Your Consultancy Name]` (in the nav, page titles, and footers of all 4 pages).
2. **Contact details** — in `contact.html`, replace `[your-email@example.com]`, `[+xx xxx xxx xxxx]` and `[City, Country]` with real details.
3. **Services** — `services.html` is written around EU regulatory compliance (GDPR, CE marking, gap analysis, etc.). Edit the cards to match your actual service offering.
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
