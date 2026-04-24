# links

Single-page link hub for Tom McMillan's TikTok bio. Routes traffic to three destinations:

- **NWSL Notebook** — https://nwslnotebook.com
- **Research** — https://nwslt.com
- **Substack** — https://itstommcmillan.substack.com

## Edit the links

Open `index.html` and edit the three `<a>` elements inside `<nav>`. Each has an `href`, a `.title`, and a `.subtitle`. To reorder, move the `<a>` blocks; to add a fourth, duplicate one.

Header name and descriptor live in `<header>` at the top of `<main>`.

## Design

- Dark warm-ink surface (`#0F0E0C`) with Flexoki accent tones (red → orange → gold gradient on the italic display text).
- Typography: Instrument Serif (via Google Fonts, `display=swap` so first paint is unblocked) for the headline; system monospace for eyebrows, card indexes, and the arrow; system sans for card titles.
- Subtle drifting aurora gradient + SVG grain texture in the background, both pointer-events: none.
- Staggered fade-in on card load (80ms stagger). `prefers-reduced-motion` disables all motion.
- CSS inlined in `index.html` for fastest first paint.
- No JavaScript, no build step, one external dependency (Google Fonts).

## Deployment

Static site. Vercel auto-detects it on import — no `vercel.json` or `vercel.ts` needed.

After the first deploy, add an `og:url` meta tag pointing at the production URL so link previews reference the canonical address. An `og:image` can be added later by dropping a file at the repo root and adding one `<meta property="og:image">` tag.
