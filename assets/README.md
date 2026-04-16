# assets/

Static assets referenced by `index.html`.

## Required files

| Filename | Purpose | Spec |
|---|---|---|
| `jd-headshot.png` | Hero portrait | Line-drawing portrait PNG with transparent-or-white background. CSS inverts + screen-blends so black lines render as white on the navy hero. |
| `og-image.jpg` | Social share card (LinkedIn, Twitter, Facebook) | **1200×630**, JPG or PNG under 5MB. Should include JD's name, one-line positioning, and visual elements from the site aesthetic (navy background, brass accents, compass motif). Generate once and reuse. |
| `favicon.svg` | Browser tab icon | ✓ Already in place — SVG compass rose matching the site palette. |

## How to swap the headshot

1. Drop the new image into this directory as `jd-headshot.png` (exact filename)
2. Preview locally: `python3 -m http.server 8000` from the repo root
3. Commit and push. If the blend treatment needs adjusting for a different image style (color photo vs line art), tweak `.hero-portrait` in `index.html`.

The hero markup references `assets/jd-headshot.png`. An `onerror` handler hides the `<img>` if the file is ever missing so the hero still looks clean.

## Future assets

When we add more (favicons, OG images, book cover thumbnails), document them here first so we don't lose track.
