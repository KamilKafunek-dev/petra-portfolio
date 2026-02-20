# Reference Analysis — Jakub Hrůša & Heinz Ferlesch

Date: 2026-02-20
Context: Petra Portfolio (Next.js + Payload)

## Input sources
- https://www.jakubhrusa.com/
- https://www.heinzferlesch.com/

## Blocker + workaround
- **Blocker:** Browser automation service is currently unavailable in this environment (no runnable browser), so full visual/UI inspection (spacing, typography rhythm, interactions) could not be captured directly.
- **Workaround:** Used content extraction and structural analysis from fetched pages + common patterns from classical music artist websites. Decisions below are marked practical/MVP-first and should be validated in visual QA later.

---

## What to copy (practical UI/IA patterns)

### 1) Homepage as an editorial “now” surface
**Observed pattern:** Both references foreground current activity (latest releases/projects/events).

**Apply to Petra:**
- Hero = compact identity block (name, role, one-line positioning).
- Immediate “Now” section below hero:
  - next performance (date/place)
  - latest video
  - latest news/project mention
- Keep first scroll focused on **proof of active work**, not biography wall.

### 2) Strong top-level IA with low click-depth
**Observed pattern:** Artist, projects, events, media, contact are clearly separable.

**Apply to Petra:**
Top navigation (MVP):
1. Home
2. Bio
3. Performances
4. Media
5. Pedagogy & Projects (VŠMU + educational work)
6. Contact

Rule: user reaches any key content in <=2 clicks.

### 3) Biography split: short + full version
**Observed pattern:** Long-form about text exists, but discoverability starts from short intro.

**Apply to Petra:**
- On homepage: 3–5 sentence short bio.
- Dedicated Bio page:
  - tabs/switcher for SK / EN (and optional DE later)
  - downloadable CV/PDF links
  - selected milestones timeline

### 4) Event-oriented content needs date intelligence
**Observed pattern:** Conductor sites rely on event chronology.

**Apply to Petra:**
- Performance item has required start date/time + venue + city.
- Auto-separate into:
  - Upcoming
  - Archive
- Sort upcoming ASC, archive DESC.

### 5) Media should be embed-first, not upload-heavy
**Observed pattern:** External platforms (YouTube/Spotify) are key distribution channels.

**Apply to Petra:**
- Media entries support provider URL + optional local thumbnail.
- Render by type:
  - YouTube video embed
  - Spotify album/show embed
  - Image gallery block
- Avoid storing large video files in MVP.

### 6) Institutional links as credibility blocks
**Observed pattern:** Professional affiliations matter for trust.

**Apply to Petra:**
- Dedicated “Affiliations” module with logo, role, link.
- Include VŠMU profile, ensembles, partner institutions.

### 7) Contact page should minimize friction
**Observed pattern:** Direct communication is central for bookings.

**Apply to Petra:**
- One clear CTA: “Booking / Collaboration inquiry”.
- Contact channels: email (required), management (optional), social links.
- Optional simple form with anti-spam (Payload/Next server action).

---

## UX writing guidance for this domain
- Tone: professional, warm, factual.
- Avoid startup language; prefer artistic/professional vocabulary.
- Dates and credits must be precise.
- Program/repertoire names should preserve diacritics and official naming.

---

## IA decisions for MVP (implementation-ready)
1. Launch with 6 primary pages only (no deep mega-menu).
2. Build reusable section blocks for Home (Hero, Now, Selected Work, CTA).
3. Treat Performances and Media as first-class collections in CMS.
4. Keep biography multilingual via localized fields (SK/EN now, DE optional).
5. Separate “Pedagogy & Projects” to reflect Petra’s VŠMU and student work.

---

## Validation checklist for visual pass (once browser/preview works)
- [ ] Hero hierarchy readable in first 3 seconds.
- [ ] Upcoming event card visible above fold on desktop.
- [ ] Mobile nav remains within 1-level depth.
- [ ] Media embeds keep aspect ratio and don’t shift layout.
- [ ] SK/EN switcher obvious and persistent on Bio page.
