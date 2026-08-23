# GooCampus Australia — Landing Pages

Landing pages for GooCampus Australia (AMC Standard Pathway guidance for
International Medical Graduates). Static HTML, no build step.

**Live:** https://beast-clone.github.io/goocampus-australia-rebrand/

| File | URL | Page |
|---|---|---|
| `index.html` | `/` | Become a doctor in Australia — the main landing page |
| `index-v3.html` | `/index-v3.html` | Australia AMC MCQ Coaching Program |
| `amc-clinical.html` | `/amc-clinical.html` | Australia AMC Clinical Prep |
| `privacy.html` | `/privacy.html` | Privacy Policy |

`index-v3.html` and `amc-clinical.html` keep those filenames because those URLs
have been shared publicly. Don't rename them.

## Design system

One system across all four pages. An earlier emerald/gold/Sora landing page was
retired in Aug 2026 — if `forest`, `ivory`, `Sora` or `C69749` ever reappear in
this repo, that's a regression.

| Token | Value | Use |
|---|---|---|
| `accent` | `#FF3C00` | brand mark, rules, non-text |
| `cta` | `#D93000` | filled buttons carrying white text |
| `cta` hover | `#BF2A00` | |
| `ink` | `#0A0A0A` | headings |
| `body` | `#5B5B5B` | body copy |
| `paper` | `#F7F7F5` | page background |
| `line` | `rgba(0,0,0,.08)` | hairlines |

**`#FF3C00` fails AA behind white text**, which is why filled buttons use `#D93000`
instead. Keep that split — don't "simplify" the two oranges into one.

Type is **Inter** throughout, on the Trillo scale: H1 90px / weight 500 /
−0.044em, H2 48px, body 16/27.2. Buttons are 52px tall with a 12px radius.

One exception: `index.html` still sets **Urbanist** as its body font while the
other three use Inter. Unresolved.

## Run locally

Any static server works — there's nothing to build.

```bash
npx serve .
```

## Deploy

**GitHub Pages, from `main` at the repo root.** Any push to `main` publishes
immediately; there is no Netlify project for this repo. Pages caches hard, so
append `?v=1` when checking a change or you may be looking at a stale copy.

## Notes

- Pages load Tailwind from the **Play CDN**, which is not intended for
  production — compile Tailwind if this moves to a real domain. The Play CDN's
  MutationObserver also prevents browser-automation tools from reaching
  `document_idle`, so scroll and text-extraction time out against these pages.
- Hero and pillar images are licensed Unsplash placeholders. Swap in real
  GooCampus faculty and student photography.
- These pages capture leads via Fillout forms and WhatsApp. They run **no
  analytics and no advertising pixels**, and `privacy.html` says so — if you add
  tracking, update the policy first.
- `privacy.html` is framed on the Privacy Act 1988 (Cth) and the Australian
  Privacy Principles. **It has not been reviewed by a lawyer.**
