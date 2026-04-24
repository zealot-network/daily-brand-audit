# Daily Brand Audit

Automated daily brand standards audit agent — browses brand websites, extracts
10-section audits, writes them to Notion, and runs on a Sun–Fri schedule via
Perplexity Computer.

One brand is audited per day at 8:00 AM Central. The agent visits 12+ pages per
site, reads the DOM, captures screenshots, and produces a senior-designer-level
brand standards document covering color, typography, logo, layout, UI
components, iconography, photography, voice, platform/tech, and the list of
pages browsed.

## Repository layout

```
audits/       Per-brand brand standards audits (markdown, one file per brand)
config/       brands.json (full queue), state.json (progress), audit_prompt.md (template)
logs/         run_log.md — cron run history
research/     Supporting research (e.g., which brands have public brand portals)
```

## Schedule

- Cron: `0 13 * * 0-5` UTC (8:00 AM Central, Sunday through Friday — no Saturday)
- One brand per run, picked from `config/brands.json` using `config/state.json.current_index`
- On completion: audit is written to Notion, `state.json` increments, `logs/run_log.md` appends a new row, and an in-app notification fires

## Audit structure

Every audit follows the 10-section template in `config/audit_prompt.md`:

1. Color Palette
2. Typography
3. Logo & Wordmark
4. Layout & Grid System
5. UI Components
6. Iconography
7. Photography / Imagery Style
8. Brand Voice & Language Style
9. Platform & Technical Notes
10. Pages Browsed

## Current progress

See `config/state.json` for the live queue position and `logs/run_log.md` for
run history. Completed audits live in `audits/`.
