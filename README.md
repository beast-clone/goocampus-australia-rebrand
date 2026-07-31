# GooCampus Australia — Landing Page Rebrand

A rebranded, single-file landing page for GooCampus Australia (AMC Standard Pathway
guidance for International Medical Graduates). Same content as the live site, elevated
to a premium medical-institution identity.

- **Palette:** deep emerald + gold + warm ivory
- **Type:** Sora (display) + Inter (body)
- **Motion:** GSAP ScrollTrigger reveals + testimonial marquee, all reduced-motion safe
- **Stack:** single `index.html`, Tailwind (Play CDN), Phosphor icons, GSAP

## Run locally
```bash
python3 -m http.server 8777
# open http://localhost:8777/index.html
```

## Production notes
- Uses the Tailwind Play CDN for the demo. For production, compile Tailwind
  (a build step) rather than shipping the CDN script.
- Images are licensed Unsplash stock placeholders. Swap in real GooCampus faculty
  and student photography for the most authentic result.
