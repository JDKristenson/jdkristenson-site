# jdkristenson.com

Personal website for JD Kristenson: biography, areas of expertise, publications,
Rudder Orders newsletter, and contact links.

This is a personal-site project, not an application framework or a reference
collection. The existing collaboration workflow credits JD and VA, and the initial
commit records a VA first pass. Preserve that collaborative attribution when
describing or reusing this project.

## Stack and prerequisites

- Static HTML and CSS in `index.html`, with local images and an SVG favicon.
- Python 3 for the local preview command below; any static HTTP server can serve
  the site. A browser is the runtime.
- No package installation, Node requirement, compilation, generated output, or
  build command. Keep this zero-build setup unless a new requirement justifies
  changing it.
- Google Fonts is an external runtime dependency. Without network access, the
  CSS falls back to generic serif and sans-serif fonts.

There is no application backend, database, contact-form submission, or newsletter
subscription service in this checkout. The newsletter button currently goes to
`#connect`; the contact buttons open LinkedIn or the visitor's email client.

## Local preview

From the repository root:

```bash
python3 --version
python3 -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000/>. Stop the server with Ctrl+C. If port 8000 is in use,
choose another port and use the same port in the URL.

This server is for development, not production. Binding to loopback keeps the
preview local. Python serves the whole directory, including documentation; do not
use it to expose a working checkout to the public.

## Verification before a PR

There is currently no automated test suite, linter, or CI workflow. A successful
preview is a smoke check, not proof of content accuracy, accessibility, or external
service availability.

1. Preview the site at desktop and narrow/mobile widths. Check the navigation
   anchors, portrait, favicon, publications, and contact links. The portrait is
   intentionally hidden at viewport widths of 1100px or less.
2. Confirm the local assets return successfully (with the server running):

   ```bash
   curl --fail --silent --output /dev/null http://127.0.0.1:8000/
   curl --fail --silent --output /dev/null http://127.0.0.1:8000/assets/jd-headshot.png
   curl --fail --silent --output /dev/null http://127.0.0.1:8000/assets/favicon.svg
   curl --fail --silent --output /dev/null http://127.0.0.1:8000/assets/og-image.jpg
   ```

   `curl` is optional tooling for these HTTP checks; the browser's Network panel
   can check the same responses. Local asset checks do not verify the absolute
   production social-card URL or third-party links.
3. For diagram or documentation edits, check JSON syntax and whitespace:

   ```bash
   python3 -m json.tool docs/architecture.excalidraw > /dev/null
   git diff --check
   ```

   JSON syntax alone does not validate the drawing's layout. Open it in an
   Excalidraw-compatible editor to check that the text and arrows remain readable.
4. Review biographical/publication changes with JD using `ISSUES.md`. Do not
   invent missing URLs, credentials, or professional claims.

## Architecture and editable drawing

[Open or download the editable Excalidraw source](docs/architecture.excalidraw).
Open the downloaded file in Excalidraw using **Open**, or drag it onto the canvas.
The diagram contains native text, rectangles, and arrows, not a flattened image.

The drawing follows the source: `index.html` and `assets/` are served unchanged by
a static HTTP server, then rendered by the browser. The browser also requests
Google Fonts and follows outbound contact links. `DESIGN.md` and `ISSUES.md` guide
maintenance; they are not runtime services. `CNAME` and the canonical/social meta
tags record domain intent, not proof of DNS, a hosting provider, or deployment.

## Key files

- [`index.html`](index.html): page content, inline styles, metadata, and the
  portrait's inline error handler.
- [`assets/`](assets/): portrait, social card, favicon, and asset notes. The current
  portrait uses black linework on a cream panel; inspect the CSS before replacing it.
- [`DESIGN.md`](DESIGN.md): design guidance. Some notes describe earlier treatments;
  compare them with the current source before changing visuals.
- [`ISSUES.md`](ISSUES.md): content accuracy decisions and missing publication links.
  Some checked items still describe historical branch status.
- [`CNAME`](CNAME): intended custom domain for compatible static hosting.
- [`docs/architecture.excalidraw`](docs/architecture.excalidraw): editable source map.

## Collaboration workflow

JD and VA develop this together. Start from an up-to-date `main`, then use a
feature branch:

1. With a clean working tree, `git switch main` then `git pull --ff-only origin main`.
2. `git switch -c docs/your-change` (or `feat/...`, `fix/...`, `content/...`, `design/...`).
3. Edit, preview locally, and commit with a conventional message.
4. `git push -u origin <branch>` and open a PR.
5. Review and merge through the repository's protections.

**Do not commit directly to `main`.** Always go through a PR so we have a review
checkpoint. Keep existing attribution; the checkout does not include an
open-source license granting reuse of the site, portrait, or copy.

Commit format: `<type>: <short description>`, with an optional explanatory body.
Existing types: `feat`, `fix`, `content`, `design`, `docs`, `chore`.
Read `DESIGN.md` before proposing visual changes.

## Hosting and publication boundaries

The files are suitable for static hosting without a build step. This checkout
contains `CNAME` and canonical/social URLs, but no hosting workflow or provider
configuration proving how the live site is published. Confirm hosting and DNS
with the maintainer before changing deployment settings. Do not treat a local
preview as a verified production deployment.

Before publishing any new material, review personal contact details, portrait
rights, and content accuracy. Keep private drafts and credentials out of this
repository. A `.gitignore` entry is not a secret scanner and does not remove files
already committed to history.
