# MVP Issue Skeleton

Project: Petra Portfolio (Next.js + Payload)
Date: 2026-02-20

Legend:
- P0 = must-have for launch
- P1 = important after core flow works

## P0 — Foundation

### MVP-001: Decide and scaffold project structure (web + cms)
**Goal:** repo contains runnable skeleton for Next.js frontend and Payload backend.
**Acceptance criteria:**
- Clear folder structure committed.
- Root README explains run commands.
- `npm/pnpm` scripts for dev/build exist.

### MVP-002: Configure Payload with core collections/globals
**Goal:** implement content model from `docs/content-model.md`.
**Acceptance criteria:**
- Collections: biographies, performances, mediaItems, projects, institutions.
- Globals: siteSettings, homepage, contactPage.
- Admin can create and publish entries.

### MVP-003: Next.js base layout + navigation
**Goal:** render top-level IA pages with consistent shell.
**Acceptance criteria:**
- Header + footer present.
- Routes: `/`, `/bio`, `/performances`, `/media`, `/projects`, `/contact`.
- Mobile nav works.

### MVP-004: Upcoming/Archive performances page
**Goal:** key domain page functional.
**Acceptance criteria:**
- Upcoming list sorted ascending by date.
- Archive list sorted descending by date.
- Empty states defined.

### MVP-005: Media page with external embeds
**Goal:** publish videos/audio quickly.
**Acceptance criteria:**
- YouTube and Spotify links render correctly.
- Image gallery entries render as grid/lightbox (basic).
- No layout shift on load.

### MVP-006: Multilingual bio (SK/EN)
**Goal:** present profile in two languages.
**Acceptance criteria:**
- SK and EN content manageable in CMS.
- UI switcher/tabs on Bio page.
- Optional CV file download link.

### MVP-007: Contact page + anti-spam
**Goal:** enable booking/collaboration communication.
**Acceptance criteria:**
- Booking email visible.
- Optional form with server-side validation.
- Basic anti-spam (honeypot or rate-limit).

## P0 — Quality / Ops

### MVP-008: SEO + social metadata baseline
**Acceptance criteria:**
- Title/description/OG defaults from CMS global.
- Per-page override for major pages.

### MVP-009: CI baseline
**Acceptance criteria:**
- PR/commit runs lint + typecheck.
- Failing checks block merge.

---

## P1 — Post-core improvements

### MVP-010: Affiliation logos and institutional links block
### MVP-011: Press mentions / reviews section
### MVP-012: Rich homepage modules (quote, featured projects)
### MVP-013: Analytics and consent-safe tracking
### MVP-014: Performance detail pages with repertoire metadata

---

## Known blockers
1. Visual benchmarking of reference sites is partially limited (browser automation unavailable).
   - Workaround: continue structure-first implementation; do later manual visual QA.

## Suggested first execution order
1. MVP-001
2. MVP-002
3. MVP-003
4. MVP-004 + MVP-006
5. MVP-005
6. MVP-007
7. MVP-008 + MVP-009
