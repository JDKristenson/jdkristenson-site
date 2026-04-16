# assets/

Static assets referenced by `index.html`.

## Required files

| Filename | Purpose | Spec |
|---|---|---|
| `jd-headshot.jpg` | Hero portrait | Portrait crop, min 800×1000px, JPG or WebP. Color photo preferred — CSS applies a navy/brass duotone filter at render time. |

## How to add the headshot

1. Drop the image into this directory as `jd-headshot.jpg` (exact filename)
2. Preview locally: `python3 -m http.server 8000` from the repo root
3. Commit the asset on a branch: `git checkout -b assets/add-headshot && git add assets/jd-headshot.jpg && git commit -m "assets: add JD headshot for hero"`
4. Push and merge

The hero markup already references `assets/jd-headshot.jpg`. Until the file exists, an `onerror` handler hides the `<img>` so the hero still looks clean without it.

## Future assets

When we add more (favicons, OG images, book cover thumbnails), document them here first so we don't lose track.
