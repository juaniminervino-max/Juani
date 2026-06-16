# Luxury Yachts — Website

A world-class single-page marketing site for **Luxury Yachts**, a premium superyacht brokerage. Dark, cinematic, premium — inspired by top-tier automotive and Web3 brand aesthetics.

## Stack

- **Vanilla HTML / CSS / JS** — single self-contained `index.html`, no build step.
- **CDN libraries only:** **Three.js** (live 3D), **GSAP + ScrollTrigger** (scroll animation), **Lenis** (smooth scroll).
- Fonts: Space Grotesk (display) + Inter (body) + Cormorant italic (accents).

## Highlights

- **3D ocean hero:** a live Three.js water surface — dark navy waves displaced in real time with a moving gold point-light for travelling reflections, plus floating geometric shapes with mouse parallax.
- **Scroll-driven 3D:** a pinned section where a wireframe yacht model rotates and scales while the camera orbits it, all driven by ScrollTrigger progress.
- **Depth parallax:** each section layers 3 blurred colour fields that move at different speeds on scroll for a real depth illusion.
- **3D flip cards:** fleet cards do a full 3D `rotateY` flip on hover/focus, revealing full specs on the back.
- **Magnetic buttons:** primary CTAs pull toward the cursor within an ~80px radius and spring back on exit.
- **Smooth scroll:** Lenis replaces native scroll, synced to GSAP's ticker and ScrollTrigger.
- **Plus:** glassmorphism, neon gold glow, animated gradient-border CTA, cursor glow, scroll-progress bar, count-up stats, grain + vignette.

## Accessible & resilient

- Full `prefers-reduced-motion` fallback: 3D/animation disabled, Lenis off, flip cards stack to show specs, count-up resolves instantly.
- **WebGL feature-detected** — if unavailable, the hero falls back to a gradient and the 3D section is hidden; the page still works with no GSAP/Three/Lenis (graceful degradation).
- Keyboard focus rings, focusable flip cards, semantic landmarks, alt text, labelled form fields.

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
