# Petra Portfolio

Headless portfolio platform for Petra Torkošová, built with **Next.js** (frontend) and **Payload CMS** (content backend).

## Architecture
- `frontend/` — Next.js website (public pages, rendering, SEO)
- `backend/` — Payload CMS (content modeling, editorial workflow, API)
- `docs/` — product + implementation documentation
- `infra/` — local/dev environment and deployment helpers

## Current docs (execution baseline)
- `docs/reference-analysis.md` — practical UI/IA learnings from reference sites
- `docs/content-model.md` — information architecture + Payload content model
- `docs/daily-plan.md` — day execution plan + taskboard
- `docs/mvp-issues.md` — MVP issue skeleton and priorities

## Planned Stack
- Backend: Payload CMS
- Frontend: Next.js (App Router)
- Data flow: Payload API -> Next.js server components

## Status
Repository is in scaffold phase. Focus is on small batches, quick feedback, and documented decisions.

## Next Steps
1. Scaffold runnable Next.js + Payload apps
2. Implement core collections/globals from `docs/content-model.md`
3. Build top-level IA routes and navigation
4. Add CI checks (lint + typecheck)
