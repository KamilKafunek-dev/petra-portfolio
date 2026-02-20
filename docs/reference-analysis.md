# Reference Analysis (IA/UI) — Petra Portfolio

Date: 2026-02-20
Sources: jakubhrusa.com, heinzferlesch.com

## Blocker + workaround
- **Blocker:** Browser automation unavailable, so no full visual audit (exact spacing/typography scale/interactions).
- **Workaround:** Structure-first analysis from fetched content + known portfolio patterns; validate visual details later in manual QA.

## 10 practical points (MVP-ready)
1. **IA must stay shallow:** max 6 top-level items (Home, Bio, Performances, Media, Pedagogy/Projects, Contact), target <=2 clicks to key info.
2. **Hero should be identity-first:** name + role + one-line positioning; no long intro above the fold.
3. **Homepage needs “Now” block:** next concert, latest video, latest project/news to prove active work.
4. **Typography priority:** readable serif/sans pairing, large heading contrast, generous line-height for long bios.
5. **Section rhythm:** alternate dense info blocks (events) with visual/media blocks to avoid text wall fatigue.
6. **CTA clarity:** one primary CTA (“Booking / Collaboration”) repeated in hero and contact section.
7. **Navigation behavior:** sticky simple top nav; mobile single-level menu (no deep nesting).
8. **Event IA:** automatic split Upcoming vs Archive, chronological sorting (upcoming ASC, archive DESC).
9. **Media strategy:** embed-first (YouTube/Spotify) with stable aspect ratios; avoid heavy self-hosted video in MVP.
10. **Credibility modules:** visible institutional links (VŠMU, ensembles, partners) near bio/projects for trust.

## Immediate implementation decisions
- Keep first release to 6 primary pages.
- Use reusable homepage sections: Hero, Now, Featured Media, CTA.
- Treat Performances + Media as primary CMS collections from day 1.
