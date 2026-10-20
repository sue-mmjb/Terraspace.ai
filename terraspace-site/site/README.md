# TerraSpace.ai — website

Static single-page site. No build step.

- `index.html` — the page (HTML, CSS and JS in one file)
- `assets/` — imagery; swap any file to change a section's photo
- `vercel.json` — clean URLs and long cache for assets

## Hero before/after

The hero slider compares `assets/hero-before.jpg` (left, "Your photo") with `assets/img-01.jpg` (right, "Your design").

`hero-before.jpg` is a placeholder: a sketch-style site capture generated from `img-01.jpg`, because no bare-plot photo exists in the assets yet. Replace it with a real, unglamorous photo of the same plot (bare lawn, concrete courtyard, dirt lot) and keep the same 16:9 framing so the slider lines up. The "Quote ready" card in the hero shows sample values; edit them in `index.html` under `.est`.

Deploy: push to GitHub, import the repo in Vercel, framework preset "Other", output directory `.`.
