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
- [ ] Current: `20+`
- Memory notes 25 years Navy
- Decision needed: confirm the number (20+, 25, 25+)

### 3. "NATO" claim appears in two places
- [ ] Stats bar: `"NATO — Advisory experience"`
- [ ] Expertise card #1 (Defense & Maritime Strategy): `"...allied force coordination across NATO and Indo-Pacific theaters."`
- Decision needed: confirm both, or replace with verified credentials. If only one is accurate, flag which.

### 4. Stats bar — "Languages: EN, FR, ZH"
- [ ] Current: EN, FR, ZH
- Memory confirms Mandarin (ZH) fluency; French (FR) is not documented
- Decision needed: confirm French, or drop to "EN, ZH" (and possibly adjust the count)

### 5. Second book placeholder
- [x] **Resolved on branch** `content/accuracy-fixes`. Swapped in real title: "Command in the Age of AI — Forthcoming. Details to be announced." Description intentionally minimal so JD can write the real blurb when the book copy is ready.

### 6. Newsletter — "The Bow Wave" → "Rudder Orders"
- [x] **Resolved on branch** `content/rename-newsletter-to-rudder-orders` (pending merge). JD confirmed the newsletter is Rudder Orders. Replaced all four references in `index.html` (h2, epigraph, subscribe CTA, newsletter visual title) and rewrote the epigraph to match Navy terminology for rudder orders. Subscribe link still points to `#connect` — once we have the LinkedIn newsletter URL, update the href.

### 7. "Naval Officer's Guide — 14th Edition" co-author claim
- [ ] Current: claims JD is co-author of the 14th edition
- Decision needed: confirm this is accurate. If yes, add link to the book; if no, replace with an accurate publication.

### 8. Forthcoming book section missing link
- [ ] Once #5 is resolved, add a preorder / announcement link or a "notify me" capture

### 9. No headshot
- [ ] Site has no photo of JD
- Decision needed: add duotone navy/brass headshot in hero, or leave text-only

### 10. Connect section — no form, no calendar link
- [ ] Current: LinkedIn + mailto links only
- Decision needed: add Calendly / scheduling link, or keep it lean

---

## Resolved

_None yet._
