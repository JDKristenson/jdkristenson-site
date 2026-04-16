# jdkristenson.com

Personal website for JD Kristenson — former Navy warship captain, now leading client success at Ayna.

## Stack

Static HTML + CSS. No build step. One file, one preview, one deploy.

## Local preview

```bash
python3 -m http.server 8000
```

Open http://localhost:8000

## Collaboration workflow

JD and VA develop this together. Branching workflow:

1. `git pull origin main`
2. `git checkout -b feat/your-change` (or `fix/...`, `content/...`, `design/...`)
3. Edit, preview locally, commit with conventional message
4. `git push -u origin <branch>` and open a PR
5. Review, merge, delete branch

**Do not commit directly to `main`.** Always go through a PR so we have a review checkpoint.

## Commit format

```
<type>: <short description>

<optional body>
```

Types: `feat`, `fix`, `content`, `design`, `docs`, `chore`

## Key files

| File | Purpose |
|---|---|
| `index.html` | The site — single file, all styles inline |
| `DESIGN.md` | Design system spec (palette, typography, components, motion). The source of truth for look and feel. |
| `ISSUES.md` | Outstanding content accuracy corrections (fabrications to fix before going live) |
| `README.md` | This file |

## Design direction

Read `DESIGN.md` before proposing visual changes. It captures the current aesthetic as a reusable spec so we can build new pages that match.

## Deploy

TBD. Options under consideration: GitHub Pages, Cloudflare Pages, Netlify, or pointing jdkristenson.com at a static host.
