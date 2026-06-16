# Luxury Yachts — Website

A world-class single-page marketing site for **Luxury Yachts**, a premium superyacht brokerage. Dark, cinematic, premium — inspired by top-tier automotive and Web3 brand aesthetics.

## Stack

- **Vanilla HTML / CSS / JS** — single self-contained `index.html`, no build step.
- **GSAP + ScrollTrigger** (the only external library) loaded from CDN for scroll-driven animation.
- Fonts: Space Grotesk (display) + Inter (body) + Cormorant italic (accents).

## Highlights

- **Hero:** full-screen animated aurora/gradient-mesh background (navy · purple · gold), gradient display type, and floating 3D geometric shapes (rotating cube, rings, triangle) that react to the mouse with parallax.
- **Animations:** GSAP scroll reveals on every section, service cards that flip up, testimonials that rise, stat numbers that count up on entry, and a **pinned horizontal-scroll** fleet section (desktop).
- **Visual effects:** glassmorphism cards (blur + transparency), neon gold glow, an **animated gradient-border CTA**, a **cursor glow** that follows the mouse, scroll-progress bar, film grain + vignette.
- **Accessible & resilient:** full `prefers-reduced-motion` fallback (animations off, content visible, count-up via IntersectionObserver), keyboard focus rings, semantic landmarks, alt text, labelled form fields. Degrades gracefully if the GSAP CDN is unavailable.

## Run locally

```bash
cd site
python3 -m http.server 8000   # visit http://localhost:8000
```

## Deploy

Deploy-ready for GitHub Pages — it's a static file. The repo's GitHub Actions workflow (`.github/workflows/deploy-pages.yml`) publishes `site/` automatically on push.

## Notes

- Yacht/ocean imagery is hotlinked from Unsplash for the demo — replace with licensed assets before launch.
- The contact form is front-end only; wire its `submit` handler to your CRM/email backend.
- The animated gradient-border CTA uses the CSS `@property` API for smooth rotation (supported in modern Chromium/Safari; older browsers fall back to a static gradient ring).
