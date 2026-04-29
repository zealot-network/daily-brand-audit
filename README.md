# Daily Brand Audit

Automated daily brand standards audit. Browses a brand's website, extracts a
10-section audit at senior-designer depth, writes it into Notion, and advances
to the next brand in the queue. Runs Sunday through Friday at 8:00 AM Central.

---

## What this is

An agent-driven pipeline, not a traditional app. The skill is runtime-portable
and can be executed by any Claude-compatible agent that exposes either browser
DOM tools or a `web_fetch` tool plus a Notion MCP connector. Originally built
on [Perplexity Computer](https://perplexity.ai), now also verified working in
Cowork (the desktop Claude app) and Claude Code.

The scheduled task fires each morning and executes the workflow defined in
`skills/brand-standards-audit/SKILL.md` against the next brand in
`config/brands.json`.

Each run:

1. Reads `config/state.json` and resolves the next brand.
2. Opens the brand's site, browses 12+ pages, captures the relevant DOM (or HTML via WebFetch), and synthesizes a 10-section audit.
3. Saves a local markdown copy of the audit alongside the state file.
4. Creates a new page in the Notion brand-standards database and writes the full audit into the page body (with favicon as page icon).
5. Increments `config/state.json`, appends a row to `logs/run_log.md`, and sends an in-app completion notification.

---

## Supported runtimes

The skill SKILL.md describes both supported execution paths in detail. Summary:

| Runtime | DOM access | Page fetching | Notion write |
| --- | --- | --- | --- |
| Perplexity Computer | `read_page`, `get_page_text`, screenshots | `browser_task` | `call_external_tool` |
| Cowork (Claude desktop) | None | `web_fetch` plus bash/grep | Notion MCP `notion-create-pages` |
| Claude Code | None | `web_fetch` or curl plus bash/grep | Notion MCP `notion-create-pages` |

If neither runtime is available, the skill halts and reports rather than falling back to pixel clicks through `computer-use`. Pixel clicking a 12-page scrape is not viable.

---

## Repository layout

```
audits/       One markdown file per completed brand audit
config/       brands.json (queue), state.json (cursor), audit_prompt.md (template)
logs/         run_log.md. Append-only cron run history
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

- 12+ pages browsed per site, page-type-diverse.
- Exact hex codes, font names, px values, verbatim CTA text.
- Strategic "why" beside every "what".
- Notable absences documented in every relevant section.
- No section shallower than the Brand Voice section.
- No em dashes anywhere in the output (hard punctuation rule).

---

## Getting started

- New to the project? Start with [SETUP.md](./SETUP.md).
- Running it day-to-day? See [RUNBOOK.md](./RUNBOOK.md).
- Want to understand the audit itself? Read [skills/brand-standards-audit/SKILL.md](./skills/brand-standards-audit/SKILL.md).

---

## Progress

- Queue: 170 brands (`config/brands.json`)
- Completed: see `audits/` and `logs/run_log.md`
- Current cursor: `config/state.json.current_index`
