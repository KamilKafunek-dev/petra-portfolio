# MVP Issues (max 10)

Project: Petra Portfolio (Next.js + Payload)
Date: 2026-02-20

Legend: P0 = launch critical, P1 = after core flow

## 1) P0 — Repo scaffold (Next.js + Payload)
**Acceptance criteria**
- Runnable structure for frontend/backend exists.
- Root scripts for dev/build are defined.
- README has start instructions.
**Estimate:** 3-4h

## 2) P0 — Implement core Payload schema
**Acceptance criteria**
- Collections: biographies, performances, mediaItems, projects, institutions.
- Globals: siteSettings, homepage, contactPage.
- Admin can create/publish each type.
**Estimate:** 4-6h

## 3) P0 — Base frontend layout + navigation
**Acceptance criteria**
- Header/footer and 6 IA routes are present.
- Mobile nav is one-level and usable.
- 404 page exists.
**Estimate:** 3-5h

## 4) P0 — Homepage sections (Hero + Now + CTA)
**Acceptance criteria**
- Hero renders from CMS global.
- “Now” shows featured performance/media.
- Primary CTA visible above and below fold.
**Estimate:** 2-4h

## 5) P0 — Performances page (Upcoming/Archive)
**Acceptance criteria**
- Upcoming/Archive split works by date/status.
- Sorting is correct (ASC upcoming, DESC archive).
- Empty states are implemented.
**Estimate:** 3-4h

## 6) P0 — Bio page with SK/EN switch
**Acceptance criteria**
- SK and EN content render correctly.
- Switcher is visible and persistent.
- Optional CV download link works.
**Estimate:** 2-3h

## 7) P0 — Media page with embeds
**Acceptance criteria**
- YouTube + Spotify embeds render.
- Image gallery entries render as responsive grid.
- Layout does not jump during media load.
**Estimate:** 3-5h

## 8) P0 — Contact page + anti-spam baseline
**Acceptance criteria**
- Booking contact is visible.
- Contact form (if enabled) validates server-side.
- Honeypot or rate-limit protection active.
**Estimate:** 2-4h

## 9) P1 — SEO baseline
**Acceptance criteria**
- Global metadata defaults from CMS.
- Per-page title/description overrides supported.
- OG image fallback configured.
**Estimate:** 2-3h

## 10) P1 — CI baseline
**Acceptance criteria**
- CI runs lint + typecheck on PR.
- Failed checks block merge.
- Status badge visible in README.
**Estimate:** 1-2h

---

## Blocker + workaround
- **Blocker:** Full visual benchmark of references limited (browser automation unavailable).
- **Workaround:** continue structure/content-first; schedule manual visual QA once preview/browser is available.
