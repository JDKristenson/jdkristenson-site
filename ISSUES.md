# ISSUES.md — Content accuracy corrections

Tracking known content fabrications or unverified claims in the VA's first pass. **Resolve these before the site goes live.** Every item needs JD's sign-off.

## How to resolve

For each item below:
1. JD confirms the correct value (reply in chat or edit this file)
2. Open a branch `content/fix-<slug>`, update `index.html`, open a PR
3. Check the box here, move the entry to the "Resolved" section at the bottom with the PR number

---

## Open

### 1. Hero bio line mismatch
- [x] **Resolved on branch** `content/accuracy-fixes`. Replaced VA's "Naval officer. McKinsey alumni. AI strategist. Author..." with the locked bio line verbatim plus a single value-prop sentence: `"I'm a former Navy warship captain who went on to McKinsey and now leads client success at Ayna, an AI-enabled industrial consulting firm. I help leaders navigate emerging technology, defense, and global commerce."`

### 2. Stats bar — "20+ Years of service & strategy"
- [x] **Resolved on branch** `content/accuracy-fixes`. JD confirmed `25+`. Changed stat-number from `20+` to `25+`.

### 3. "NATO" claim appears in two places
- [x] **Confirmed by JD.** Both references stand as-is (stats bar + expertise card #1). No code change required.

### 4. Stats bar — "Languages: EN, FR, ZH"
- [x] **Confirmed by JD** ("Ouais"). EN, FR, ZH stands. No code change required.

### 5. Second book placeholder
- [x] **Resolved on branch** `content/accuracy-fixes`. Swapped in real title: "Command in the Age of AI — Forthcoming. Details to be announced." Description intentionally minimal so JD can write the real blurb when the book copy is ready.

### 6. Newsletter — "The Bow Wave" → "Rudder Orders"
- [x] **Resolved on branch** `content/rename-newsletter-to-rudder-orders` (pending merge). JD confirmed the newsletter is Rudder Orders. Replaced all four references in `index.html` (h2, epigraph, subscribe CTA, newsletter visual title) and rewrote the epigraph to match Navy terminology for rudder orders. Subscribe link still points to `#connect` — once we have the LinkedIn newsletter URL, update the href.

### 7. "Naval Officer's Guide — 14th Edition" authorship
- [x] **Resolved on branch** `content/accuracy-fixes`. JD clarified he is **lead author** (not co-author). Updated pub-tag from "Co-author" to "Lead Author".

### 8. Publication links missing
- [ ] Naval Officer's Guide (14th Ed): add publisher / purchase URL on pub-card
- [ ] Command in the Age of AI: add preorder / announcement link or "notify me" capture when available

### 9. Headshot
- [x] **Resolved on branch** `content/accuracy-fixes`. JD confirmed "yes." Added `.hero-portrait` markup + CSS (duotone navy/brass filter, 280×360, right-side of hero, hidden below 1100px). Image source: `assets/jd-headshot.jpg`. Until JD drops the file, an `onerror` handler hides the broken img so the hero still looks clean.
- **JD action needed:** drop a photo in `assets/jd-headshot.jpg` (spec in `assets/README.md`).

### 10. Connect section — no form, no calendar link
- [x] **Decision: leave lean.** JD confirmed "Leave." LinkedIn + mailto links stay as-is.

---

## Resolved

_None yet._
