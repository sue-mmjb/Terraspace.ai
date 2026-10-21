# TerraSpace.ai — website

Static site. No build step.

- `app/` — the TerraSpace app (Sofia's design). Served at the root address `/` through a rewrite in `vercel.json`, and also at `/app` so the printed QR signs keep working. One HTML file plus its photos; photo paths are absolute (`/app/...`) so both addresses work. Edit data in `app/index.html` (search for `const PLANTS`, `const BASE_THEMES`, `const AISLES`, `const CREWS`, `const CURRENCIES`). No backend: everything a visitor does stays in their own browser.
- `app/models/` — 3D plant models (.glb), the lawn texture and grass tuft used by the hero model and the Virtual tour, plus the CC BY 4.0 "Cloud Garden" scan by Brendan Harmon. Keep it next to `app/index.html`; paths are absolute (`/app/models/...`).
- `marketing/` — the light marketing page, served at `/marketing`. Its photos are in `marketing/assets/`.
- `vercel.json` — root rewrite, clean URLs and long cache for photos

## Showroom QR signs

`../showroom-qr-codes/` holds the eight printable aisle signs. They point to `https://terraspace-ai.vercel.app/app#aisle-1` through `#aisle-8`. If the domain or the `/app` path changes, regenerate them. The QR codes shown inside the app use the current address automatically.

## Hero before/after

The hero slider compares `assets/hero-before.jpg` (left, "Your photo") with `assets/img-01.jpg` (right, "Your design").

`hero-before.jpg` is a placeholder: a sketch-style site capture generated from `img-01.jpg`, because no bare-plot photo exists in the assets yet. Replace it with a real, unglamorous photo of the same plot (bare lawn, concrete courtyard, dirt lot) and keep the same 16:9 framing so the slider lines up. The "Quote ready" card in the hero shows sample values; edit them in `index.html` under `.est`.

Deploy: push to GitHub, import the repo in Vercel, framework preset "Other", output directory `.`.
