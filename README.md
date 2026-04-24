# Daily Brand Audit

Automated daily brand standards audit — browses a brand's website, extracts a
10-section audit at senior-designer depth, writes it into Notion, and advances
to the next brand in the queue. Runs Sunday–Friday at 8:00 AM Central.

---

## What this is

An agent-driven pipeline, not a traditional app. The "runtime" is
[Perplexity Computer](https://perplexity.ai), which fires a scheduled task each
morning and executes the workflow defined in `skills/brand-standards-audit/SKILL.md`
against the next brand in `config/brands.json`.

Each run:

1. Reads `config/state.json` and resolves the next brand.
2. Opens the brand's site, browses 12+ pages, reads the DOM, captures
   screenshots, and synthesizes a 10-section audit.
3. Creates a new page in the Notion brand-standards database and writes the
   full audit into the page body (with favicon as page icon).
4. Increments `config/state.json`, appends a row to `logs/run_log.md`, and
   sends an in-app completion notification.

---

## Repository layout

```
audits/       One markdown file per completed brand audit
config/       brands.json (queue), state.json (cursor), audit_prompt.md (template)
logs/         run_log.md — append-only cron run history
research/     Supporting research (e.g., which brands have public brand portals)
skills/       brand-standards-audit skill definition (the canonical workflow spec)
SETUP.md      First-time configuration: connectors, Notion database, cron
RUNBOOK.md    Day-to-day operations: expediting brands, reconciling state, failures
```

---

## Audit structure

Every audit follows the 10-section template in `config/audit_prompt.md` and the
full spec in `skills/brand-standards-audit/SKILL.md`:

1. Color Palette
2. Typography
3. Logo & Wordmark
4. Layout & Grid System
5. UI Components
6. Iconography
7. Photography & Imagery Style
8. Brand Voice & Language Style
9. Platform & Technical Notes
10. Pages Browsed

Rules that make an audit "senior-designer-grade":

- 12+ pages browsed per site, page-type-diverse
- Exact hex codes, font names, px values, verbatim CTA text
- Strategic "why" beside every "what"
- Notable absences documented in every relevant section
- No section shallower than the Brand Voice section

---

## Getting started

- New to the project? Start with [SETUP.md](./SETUP.md).
- Running it day-to-day? See [RUNBOOK.md](./RUNBOOK.md).
- Want to understand the audit itself? Read
  [skills/brand-standards-audit/SKILL.md](./skills/brand-standards-audit/SKILL.md).

---

## Progress

- Queue: 170 brands (`config/brands.json`)
- Completed: see `audits/` and `logs/run_log.md`
- Current cursor: `config/state.json.current_index`
