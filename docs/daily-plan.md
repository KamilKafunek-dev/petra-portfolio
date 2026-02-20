# Daily Implementation Plan + Taskboard

Date: 2026-02-20 (05:00–11:30)
Project: Petra Portfolio (Next.js + Payload)
Principle: small batches, fast feedback, documented decisions

## Day objective
Ship a working foundation: clear architecture docs + initial repo alignment with Next.js + Payload direction.

## Constraints / Blockers
- Browser service unavailable for full visual inspection of reference sites.
  - Workaround: extract structure/text via fetch; defer pixel-level UI decisions to visual QA checkpoint.

---

## Timeboxed execution plan

## 05:00–05:45 — Discovery + IA freeze
- [x] Analyze references and write practical UI/IA notes.
- [x] Define MVP navigation + page responsibilities.
- Output: `docs/reference-analysis.md`

## 05:45–06:30 — Content model design
- [x] Convert project notes into Payload globals/collections.
- [x] Define required fields + derived views (upcoming/archive).
- Output: `docs/content-model.md`

## 06:30–07:00 — Repo alignment
- [ ] Update README architecture from old Drupal wording to Next.js + Payload.
- [ ] Add near-term bootstrap checklist.
- Output: README update commit

## 07:00–08:30 — Technical bootstrap (MVP skeleton)
- [ ] Scaffold app folders for `apps/web` and `apps/cms` OR document final monorepo choice.
- [ ] Add baseline env examples and run scripts.
- [ ] Add minimal CI check (lint/typecheck placeholder).
- Output: bootstrap commit

## 08:30–09:30 — API contract & rendering slices
- [ ] Define first API slice: homepage + upcoming performances.
- [ ] Define Next data-fetch layer contract (types/interfaces).
- Output: `docs/api-contract.md` (or inline in content model if minimal)

## 09:30–10:30 — MVP issue breakdown
- [x] Create issue skeleton with acceptance criteria.
- [ ] Prioritize P0/P1 and estimate rough effort.
- Output: `docs/mvp-issues.md`

## 10:30–11:30 — Stabilize + handoff
- [ ] Ensure at least one merged commit exists.
- [ ] Summarize blockers, decisions, next action.
- Output: short EOD summary note

---

## Taskboard (live)

## TODO
- [ ] README stack migration (Drupal -> Payload + Next.js)
- [ ] Monorepo/app structure decision note
- [ ] Env + scripts skeleton
- [ ] CI placeholder checks
- [ ] API contract v0
- [ ] P0/P1 prioritization pass

## DOING
- [ ] (empty)

## DONE
- [x] Reference analysis document
- [x] Content model + IA document
- [x] MVP issue skeleton draft

---

## Decision log (today)
1. Prioritize content architecture first, visual polish second.
2. Use embed-first strategy for media (YouTube/Spotify links).
3. Keep scope tight: 6-page IA for MVP launch.

## Fast-feedback loop
After each artifact:
1. Save doc
2. Quick consistency check (fields/pages/URLs aligned)
3. Commit in small batch with explicit message
