# Varshitha Kothakota — Portfolio

A single-page portfolio site for Varshitha Kothakota, AI Product Manager.
Pure HTML/CSS/JS — no build step, no framework.

## Structure

```
index.html          Page markup, all copy, SEO meta tags, JSON-LD schema
style.css            Full design system (tokens, layout, components, responsive, animations)
script.js            Particle background, typewriter headline, scroll reveal, counters, nav, contact form
robots.txt           Crawler rules
sitemap.xml           Single-page sitemap
assets/
  favicon.svg         Scalable favicon (used by modern browsers)
  favicon-32.png       32×32 fallback favicon
  apple-touch-icon.png 180×180 iOS home-screen icon
  og-image.png        1200×630 social share image (Open Graph / Twitter Card)
```

## Libraries (loaded via CDN, no install needed)

- [particles.js](https://vincentgarreau.com/particles.js/) — hero background network
- [Typed.js](https://github.com/mattboldt/typed.js/) — hero headline typewriter effect
- [AOS](https://michalsnik.github.io/aos/) — scroll-triggered reveals
- [GSAP](https://greensock.com/gsap/) — hero load-in sequence

All are loaded from cdnjs and require no build tooling. If deploying somewhere
with no internet access to CDNs, download these four files locally and update
the `<script src>` paths in `index.html`.

## Running locally

No build step — open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Before going live — please check these

1. **Domain.** `index.html`, `robots.txt`, and `sitemap.xml` currently use
   `https://varshithakothakota.com/` as a placeholder canonical/OG URL.
   Replace every instance with the real deployed domain.
2. **Contact form.** The form has no backend — submitting it opens the
   visitor's email client with the message pre-filled (a `mailto:` link).
   That's a deliberate choice, not a shortcut, since there's no server here
   to receive form submissions. If you'd rather have a real inbox-style
   submission, wire it to a form service (e.g. Formspree, Web3Forms) inside
   `initContactForm()` in `script.js`.
3. **Photo.** There's no headshot in this build. The hero and About section
   are designed to work without one — if a photo is added later, it can slot
   into the hero next to the name without restructuring anything.
4. **"Product Manager" positioning.** The headline and About section
   present Varshitha as an AI Product Manager per her current direction.
   The Experience timeline itself only includes roles with confirmed
   employer names and dates. If there's a specific current PM role/company
   to credit, add it as a new `.timeline__item` at the top of the timeline
   in `index.html`.
5. **Testimonials.** Intentionally omitted — no fabricated quotes from
   people who don't exist. If real ones become available, a `.philosophy`-style
   section is a natural place to add them.

## Content honesty notes

- The two flagship case studies (OpsMind AI, What's My Move) describe what's
  actually implemented in each repository, not the aspirational scope
  described in OpsMind's own README (which describes a FastAPI/Neo4j/live-LLM
  backend that isn't in the current codebase — the shipped version is a
  Next.js + Supabase dashboard with a seeded dataset).
- The two "Product Thinking" teardowns (GitHub Copilot, Way2News) are
  original analysis essays written for this portfolio, grounded in public,
  researched facts — not claims that these were previously published pieces.
