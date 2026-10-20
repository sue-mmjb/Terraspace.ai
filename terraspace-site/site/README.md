# TerraSpace.ai — website

Static single-page site. No build step.

- `index.html` — the page (HTML, CSS and JS in one file)
- `assets/` — imagery; swap any file to change a section's photo
- `vercel.json` — clean URLs and long cache for assets
- `app/` — the clickable TerraSpace app prototype, served at `/app`. One HTML file plus its photos. Edit data in `app/index.html` (search for `const PLANTS`, `const BASE_THEMES`, `const AISLES`, `const CREWS`, `const CURRENCIES`). No backend: everything a visitor does stays in their own browser.

## Showroom QR signs

`../showroom-qr-codes/` holds the eight printable aisle signs. They point to `https://terraspace-ai.vercel.app/app#aisle-1` through `#aisle-8`. If the domain or the `/app` path changes, regenerate them. The QR codes shown inside the app use the current address automatically.

## Hero before/after

The hero slider compares `assets/hero-before.jpg` (left, "Your photo") with `assets/img-01.jpg` (right, "Your design").

`hero-before.jpg` is a placeholder: a sketch-style site capture generated from `img-01.jpg`, because no bare-plot photo exists in the assets yet. Replace it with a real, unglamorous photo of the same plot (bare lawn, concrete courtyard, dirt lot) and keep the same 16:9 framing so the slider lines up. The "Quote ready" card in the hero shows sample values; edit them in `index.html` under `.est`.

Deploy: push to GitHub, import the repo in Vercel, framework preset "Other", output directory `.`.
