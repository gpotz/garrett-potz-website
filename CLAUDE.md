# Garrett Potz — Mortgage Broker Website

Personal-brand website for **Garrett Potz**, Senior Loan Officer / independent
mortgage broker with **Affinity Home Lending LLC** (Woodstock, GA). Hand-coded
**static HTML** — no build step, no framework. Deploys to **Hostinger** (folder
`public_html`) from GitHub, auto-deploy on push to `main`.

## How to work on this site
- Every page is a standalone `.html` file with its own inline `<style>` block.
- **Sitewide changes** (nav, footer, brand tokens) must be applied to ALL pages
  consistently — they were historically done with a script looping over `*.html`.
  When you change shared markup/CSS, change it on every page, then verify counts.
- `index.html` is the homepage (entry point for the domain root).
- No JS build, no bundler, no localStorage. Keep it simple and static.

## Brand tokens (defined in `:root` on every page)
- Colors: `--pine:#161616`, `--pine-deep:#0a0a0a` (footer), `--brass:#850000`
  (deep red brand), `--brass-soft:#d64545` (lighter red, hover on dark),
  `--cream:#f6f5f5` (page bg), `--paper:#fff`, `--ink:#141414`, `--muted:#5d5d5d`,
  `--line:#e4e4e6`.
- Fonts: **Fraunces** (display serif), **Inter** (body), **Spline Sans Mono**
  (labels/mono). Signature red `<mark>` highlight.
- Buttons: `.btn` = 10px rounded rectangle (not pill). Footer is dark.

## Key facts (keep accurate everywhere)
- Garrett NMLS #631592 · Affinity Company NMLS #1181151 · GA Residential Mortgage
  Licensee #42129 · Equal Housing Lender.
- Phone (770) 401-1759 (tel/sms +17704011759) · gpotz@affinityhomelending.com
- Licensed in GA, FL, AL, TN, SC (5 states). Positioned as "independent broker,
  45 lenders, 5 states." Specialty: self-employed (Bank Statement, 1099, DSCR, P&L).
- Online application (1003): https://garrettpotz.my1003app.com/register
- Google review (write): https://search.google.com/local/writereview?placeid=ChIJt1a_mMEV9YgRbO2uMtHKA9Q
- Socials (all @garrettpotz): facebook.com/garrettpotz, instagram.com/garrettpotz,
  linkedin.com/in/garrettpotz, youtube.com/@GarrettPotz

## Structure
- `index.html` — homepage
- Core: about, loan-options, contact, calculator, rent-vs-buy, affordability,
  second-opinion, roadmap, guides, guide-self-employed, blog, home-value, locations
- 15 city pages (e.g. `woodstock-ga.html`), 36 dated `blog-*.html` posts
- Legal: `privacy-policy.html`, `terms.html` (linked in every footer)

## Conventions / gotchas
- Footer + nav are repeated on every page and must stay identical.
- Loan programs order (homepage + footer): Purchase, Refinance first (most
  popular, "featured"), then Bank Statement, 1099, DSCR, P&L.
- Headshot is embedded as a base64 data URI in `index.html` and `about.html`.
- Keep community references GENERIC (no specific school/team names).
- Review gating is prohibited — never route reviews by rating.

## Pending / ideas
- "Home Search" nav item is still a placeholder (`#`) — needs an IDX service.
- Home-value + newsletter forms need a real endpoint (currently mailto).
- Consider a community photo (rights permitting).
- Badge on homepage headshot says "Senior Loan Officer" — may want
  "Independent Mortgage Broker" to match the rest of the site.

## Deployment
- Hostinger hPanel → Advanced → Git → repo, branch `main`, target `public_html`,
  Automatic deployment ON. Exclude `.git`, `*.md`, `*.zip`.
- NOT part of the website (do not deploy): the Google Apps Script review tool,
  any `journal.txt` / transcript / `SETUP.md` files.
