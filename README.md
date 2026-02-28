# SmileJet SEO Content Hub

SEO article site for [SmileJet](https://smilejet.app) — a dental tourism platform connecting patients with verified clinics worldwide.

## Structure

```
smilejet.app-SEO/
├── index.html                  # Homepage / article hub with destination filter
├── css/style.css               # Shared stylesheet
├── articles/
│   ├── vietnam/                # Vietnam destination articles
│   ├── thailand/               # Thailand destination articles
│   ├── mexico/                 # Mexico destination articles
│   └── guides/                 # General dental tourism guides
├── netlify.toml                # Netlify deployment config & redirects
└── README.md
```

## Adding a New Article

1. Create an HTML file in the appropriate directory under `articles/`
2. Follow the template structure (see existing articles)
3. Include all 4 JSON-LD blocks: Article, Organization, FAQPage, BreadcrumbList
4. Include Open Graph and Twitter Card meta tags
5. Add a card entry in `index.html`
6. `git add`, `git commit`, `git push` — Netlify auto-deploys

## SEO Template Checklist

Each article must include:

- [ ] `<title>` with keyword, year, and "SmileJet"
- [ ] `<meta name="description">` (~155 chars with price, savings, CTA)
- [ ] `<meta name="keywords">` (6-8 terms)
- [ ] `<link rel="canonical">` pointing to the clean URL
- [ ] Open Graph meta tags (og:title, og:description, og:type, og:url, og:site_name)
- [ ] Twitter Card meta tags
- [ ] JSON-LD: Article schema
- [ ] JSON-LD: Organization schema (SmileJet)
- [ ] JSON-LD: FAQPage schema (4-6 questions)
- [ ] JSON-LD: BreadcrumbList schema
- [ ] `<link rel="stylesheet" href="../../css/style.css">` (external CSS, not inline)
- [ ] Breadcrumb navigation in body
- [ ] FAQ section text matches JSON-LD exactly
- [ ] Related articles section (inter-article linking)
- [ ] CTA linking to smilejet.app/quote and destination page
- [ ] Footer with disclaimer and about blurb

## URL Structure

Clean URLs via Netlify redirects:
- `/guides/vietnam/best-dental-implant-clinics-vietnam` → `articles/vietnam/best-dental-implant-clinics-vietnam.html`
- `/guides/thailand/best-dental-implant-clinics-thailand` → `articles/thailand/best-dental-implant-clinics-thailand.html`

## Deployment

- **Platform:** Netlify
- **Trigger:** Auto-deploy on push to `main`
- **Build:** None (static HTML)
