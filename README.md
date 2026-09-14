# NYC AI Product Board

A single-page, self-contained job board tracking open **AI / data product-management
roles in the New York metro**, matched against 13 years of AI and data product work
(RAG systems, agent orchestration, MCP integrations, and LLM evaluation).

Every role was confirmed against a live applicant-tracking feed — not just a career
page that renders — and is scored for fit, level match, and compensation band.

## What's here

- **`index.html`** — the entire board. No build step, no dependencies, no backend.
  Open it in a browser and it runs. Roles are embedded as JSON inside the page.

## Features

- **Tiered ranking** — roles grouped into *Apply this week* (fit ≥ 9),
  *Strong, with one stretch* (7.5–8.9), and *Worth a look* (< 7.5).
- **Filter & search** — by sector (big tech, AI labs, enterprise, NYC-HQ), by level
  (Director+), and free-text search across title, company, and reasoning.
- **Sort** — by fit score, top of compensation band, or company.
- **Per-role status tracking** — cycle each role through *track → shortlisted →
  applied → interviewing → closed*.
- **Verification notes** — a closing section documents how each posting was checked
  and which companies could not be confirmed.

## Viewing it

Open `index.html` directly, or serve it locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

### GitHub Pages

Enable Pages for this repository (Settings → Pages → deploy from branch) to publish
the board at a shareable URL.

> **Note on status tracking:** the board persists status changes through the Claude
> Artifacts runtime. Served as plain static HTML (e.g. GitHub Pages), it still renders
> and filters fully, but per-role status changes are session-only and are not saved
> between visits.

---

*Data re-verified 2026-09-10 · 63 roles across 24 organizations.*
