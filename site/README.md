# Luxury Yachts — Website

A single-page marketing site for **Luxury Yachts**, a premium yacht brokerage and sales company.

## Design

Design choices were generated with the `ui-ux-pro-max` skill:

- **Palette:** premium black + gold (`#0C0A09` ink, `#1C1917` stone, `#CA8A04` gold, `#FAFAF9` sand)
- **Typography:** Cormorant (display) + Montserrat (body) — luxury/high-end pairing
- **Structure:** Enterprise Gateway landing pattern — hero, stats, fleet, services, about, testimonials, contact

## Sections

1. Floating glass navbar (solidifies on scroll, mobile menu)
2. Full-screen hero with CTAs
3. Stats bar
4. Featured fleet (3 listing cards with specs and pricing)
5. Services (sales, charter, management, new construction)
6. About / why-us with credibility points
7. Client testimonials
8. Contact form (client-side validation, demo only — no backend)
9. Footer

## Run

It is a static, self-contained file. Open directly or serve locally:

```bash
cd site
python3 -m http.server 8000
# visit http://localhost:8000
```

## Notes

- **Tailwind** is loaded via CDN (`cdn.tailwindcss.com`) for zero build setup. For production, install Tailwind and purge unused classes.
- **Images** are pulled from Unsplash via hotlink for the demo. Replace `images.unsplash.com/...` URLs with your own licensed assets before launch.
- **Contact form** is front-end only; wire the `submit` handler in `index.html` to your CRM/email backend.
- Accessibility: semantic landmarks, alt text, form labels, visible focus rings, and `prefers-reduced-motion` support are all included.
