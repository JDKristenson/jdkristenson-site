# DESIGN.md — jdkristenson.com

Design system spec for the personal site. Use this file as the source of truth when building new pages or components so the look and feel stays consistent.

## Aesthetic

**Naval wardroom meets modern editorial.** Deep navy backgrounds, brass accents, serif display type paired with a geometric sans. Sparse, confident, no-filler. The site should feel like the jacket of a hardcover book written by someone who has actually done the work, not a SaaS landing page.

Reference motifs: compass rose, bow wave, spine of a book, chart marks, horizon line.

## Palette

| Token | Hex | Role |
|---|---|---|
| `--navy` | `#0d1b2a` | Primary background |
| `--navy-mid` | `#152236` | Alternating section background |
| `--navy-light` | `#1e3352` | Elevated surfaces (publication spines, accents) |
| `--brass` | `#b89a5a` | Primary accent (buttons, rules, dividers) |
| `--brass-light` | `#d4b97a` | Hover state, italic emphasis in headings |
| `--cream` | `#f5f0e8` | (Reserved — not currently used) |
| `--cream-mid` | `#ede5d4` | (Reserved — not currently used) |
| `--text-primary` | `#f0ece4` | Body and heading text on navy |
| `--text-secondary` | `#9aa8b8` | Supporting copy, taglines |
| `--text-muted` | `#5a6a7e` | Labels, captions, footer |
| `--border` | `rgba(184, 154, 90, 0.2)` | Brass-tinted borders |
| `--border-subtle` | `rgba(255, 255, 255, 0.07)` | Section dividers, card edges |

## Typography

| Element | Family | Weight | Notes |
|---|---|---|---|
| Headings (h1, h2, h3) | `Cormorant Garamond` | 500–600 | Italic variant used for emphasis (`<em>` inside h1/h2) in brass-light |
| Body, nav, buttons | `DM Sans` | 300–500 | Letter-spacing increased for uppercase labels |
| Display numerals | `Cormorant Garamond` | 500–600 | Stat numbers, expertise numerals |

**Scale:**
- h1: `clamp(3.2rem, 5.5vw, 5.5rem)`, line-height 1.05, letter-spacing -0.01em
- h2: `clamp(2rem, 3.5vw, 3rem)`, line-height 1.15
- Body: 0.95–1.05rem, line-height 1.6–1.85, font-weight 300
- Eyebrow/label: 0.68–0.72rem, uppercase, letter-spacing 0.12–0.25em, in brass

**Rules:**
- Uppercase labels always have wide letter-spacing
- Italic in headings is always `--brass-light`, never plain italic on navy
- No all-caps body copy

## Layout

- **Section padding:** `6rem 4rem` desktop, `5rem 1.5rem` mobile
- **Nav height:** fixed, ~72px, blurred navy background
- **Max content width:** sections are full-bleed, but `.hero-content` and `.connect-wrap` cap at 640–660px
- **Grid patterns:**
  - Expertise: 3-column grid with 1px `--border-subtle` cell dividers
  - Publications: 2-column grid, 2rem gap
  - Newsletter: 2-column grid, 6rem gap
- **Breakpoint:** single breakpoint at 900px; below it all grids collapse to 1fr

## Components

### Navigation
Fixed top, glass effect (navy at 92% opacity + 12px backdrop blur), brass-light logo in Cormorant with wide letter-spacing, uppercase nav links in DM Sans.

### Buttons
Two variants, both uppercase DM Sans at 0.78rem, letter-spacing 0.1em, padding `0.85rem 2rem`:
- **Primary:** solid brass background, navy text, subtle translate-Y on hover
- **Ghost:** 1px brass border at 40% alpha, brass-light text, border darkens on hover

### Section label (eyebrow)
Small uppercase brass text preceded by a 20–32px brass horizontal rule. Used above every h2.

### Stat cell
Large Cormorant numeral in brass-light, small uppercase label underneath in muted text. Separated by 1px vertical `--border-subtle` rules on desktop; rules removed on mobile.

### Expertise card
Navy tile, large ghost numeral (`01`–`06`) in brass at 12% alpha as background element. Title in Cormorant, desc in DM Sans 300. Hover: background lifts to `--navy-mid` and a 2px brass underline sweeps in from the left.

### Publication card
Horizontal card with a vertical "book spine" on the left (navy-light background, 3px brass left border, vertical-rl text in brass). Info area has a small brass-bordered tag, Cormorant title, DM Sans desc.

### Decorative SVG
Compass rose used as hero background at 6% opacity. Wave line paths used under newsletter visual at 15% opacity. All decorative SVGs use brass stroke at 0.5–1px.

## Motion

- `scroll-behavior: smooth` on html
- Hero content: staggered `fadeUp` animation (0.8s ease), eyebrow → h1 → tagline → CTA with 0.15s delays
- Button hover: `translateY(-1px)` over 0.15s
- Card hover: background lift (0.25s) + brass underline sweep (0.3s)
- No parallax, no scroll-triggered animations beyond what exists today

## Voice (for content within the site)

Per `~/.claude/rules/writing-style.md`:
- Direct. Specific. Short sentences. Shorter paragraphs.
- No filler (`just`, `really`, `actually`)
- No AI fingerprint words (`delve`, `foster`, `tapestry`, `landscape`, `robust`)
- No em dashes in copy (they're reserved for the design, not the prose)
- No hedges (`it's worth noting`, `you may want to consider`)
- Active voice only

## Anti-patterns

- Do not introduce a new accent color without adding it to the palette table here first
- Do not use plain italic on navy — italic always gets brass-light
- Do not use em dashes as visual rules (we use `::before` elements with brass background)
- Do not add gradient backgrounds on cards — the aesthetic is flat + selective glow
- Do not use stock photography — if we add imagery, it should be photography of JD, book covers, or custom illustration only

## Future elements (not yet built)

When these ship, extend this file rather than improvising:
- Headshot treatment (duotone navy/brass is the leading candidate)
- Contact form (currently just LinkedIn + email links)
- Blog / writing index
- Speaking engagements list
- Book preorder / sample chapter download
