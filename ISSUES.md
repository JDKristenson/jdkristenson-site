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
- [ ] Current: `"Naval officer. McKinsey alumni. AI strategist. Author. I help organizations operate at the intersection of emerging technology, defense, and global commerce."`
- **Locked bio line** (per `~/.claude/memory/feedback_jd_bio_line.md`): `"I'm a former Navy warship captain who went on to McKinsey and now leads client success at Ayna, an AI-enabled industrial consulting firm."`
- Decision needed: replace hero tagline with locked bio line verbatim, or adapt it (retaining the exact "went on to McKinsey" and "AI-enabled" phrasing)

### 2. Stats bar — "20+ Years of service & strategy"
- [ ] Current: `20+`
- Memory notes 25 years Navy
- Decision needed: confirm the number (20+, 25, 25+)

### 3. Stats bar — "NATO Advisory experience"
- [ ] Current: claims NATO advisory
- Decision needed: confirm this is accurate, or replace with a verified credential

### 4. Stats bar — "Languages: EN, FR, ZH"
- [ ] Current: EN, FR, ZH
- Memory confirms Mandarin (ZH) fluency; French (FR) is not documented
- Decision needed: confirm French, or drop to "EN, ZH" (and possibly adjust the count)

### 5. Second book placeholder
- [ ] Current: `"New Title — In Progress · A forthcoming work exploring the intersection of technology, leadership, and strategic decision-making. Details to be announced."`
- Actual forthcoming book (per memory): `"Command in the Age of AI"`
- Decision needed: swap in the real title and write a one-paragraph description

### 6. Newsletter — "The Bow Wave"
- [ ] Current: `"The Bow Wave — Biweekly dispatch for maritime and defense professionals."`
- Existing newsletter in the system (per memory): `"Rudder Orders"` — biweekly maritime tech LinkedIn newsletter
- Decision needed: is "The Bow Wave" a new separate newsletter, a rename of Rudder Orders, or a VA invention? If it's real, fine. If not, replace with Rudder Orders or remove the section.

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
