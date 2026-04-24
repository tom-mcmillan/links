# links

Single-page link hub for Tom McMillan's TikTok bio. Routes traffic to three destinations:

- **NWSL Notebook** — https://nwslnotebook.com
- **Research** — https://nwslt.com
- **Substack** — https://itstommcmillan.substack.com

## Edit the links

Open `index.html` and edit the three `<a>` elements inside `<nav>`. Each has an `href`, a `.title`, and a `.subtitle`. To reorder, move the `<a>` blocks; to add a fourth, duplicate one.

Header name and descriptor live in `<header>` at the top of `<main>`.

## Design

- Flexoki "paper" surface (`#F2F0E5`) with Flexoki ink tones.
- System font stack — no external font requests, no FOUT.
- CSS is inlined in `index.html` for fastest first paint (file is small enough that a separate stylesheet would add an HTTP round-trip without meaningful gain).
- No JavaScript, no build step, no dependencies.

## Deployment

Static site. Vercel auto-detects it on import — no `vercel.json` or `vercel.ts` needed.

After the first deploy, add an `og:url` meta tag pointing at the production URL so link previews reference the canonical address. An `og:image` can be added later by dropping a file at the repo root and adding one `<meta property="og:image">` tag.
