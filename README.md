# Connecticut Food Finder — v2 pilot

Static GitHub Pages application with a small curated public-source dataset, Leaflet map, filters, links to source pages, and **local-only partner editing demonstration**.

## Deploy
Create a GitHub repository; upload `index.html` and `locations.json` to the root; enable Settings → Pages → Deploy from branch → main / root. GitHub Pages serves both files. No build step required.

## Important limitations
- Six initial public-source records only. This is **not** a complete or authoritative Connecticut Foodshare partner directory.
- Mobile dates are **selected explicitly published 2026 dates**, not a complete synchronized schedule. Confirm all schedules before traveling. No dates are extrapolated from recurrence patterns.
- Coordinates are approximate for map display; Directions searches use the published address.
- Partner portal is a **localStorage-only demo**; anyone can edit their own browser copy, but no shared database, secure accounts, approvals, or cross-device persistence exist.
- Do not represent public third-party listings as confirmed Connecticut Foodshare partner agencies without verification.
- Public data licensing and redistribution rights must be reviewed before importing a full directory from 211 or other third-party services.

## Suggested production backend
Supabase Auth + PostgreSQL with agency, program, location, service schedule, event, user_membership, and audit log tables. Enforce Row Level Security based on agency membership; do not put service-role keys in GitHub Pages. All changes should be reviewed or tracked with an audit trail. Schedule ingestion should run server-side with source provenance and cancellation support.

## Public source URLs
See `source` per record in `locations.json`. Published 2026 schedules are subject to change.
