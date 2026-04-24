# Setup

First-time configuration to stand this pipeline up end-to-end. Everything here
is idempotent — you can re-run any step safely.

> This repo deliberately does **not** commit environment-specific identifiers
> (Notion database IDs, data source IDs, cron IDs, workspace/sandbox paths).
> Fill those into your own private config file or Computer memory — never this
> repo.

---

## 1. Prerequisites

- A Perplexity Computer account
- A Notion workspace you own (or can add databases to)
- Connected apps in Computer:
  - **Notion** (required — target for the audit writes)
  - **GitHub** (optional — if you want the agent to also push artifacts here)

---

## 2. Notion database

Create a database named **All Brand Standards DB** (or whatever you like — the
name is referenced by your private prompt, not this repo).

Minimum schema:

| Property | Type   | Purpose                                  |
|----------|--------|------------------------------------------|
| Name     | Title  | Brand name (e.g., "Stripe")              |

Everything else lives in the **page body** — do not put audit content into
properties. You'll add:

- An H1 title line
- 10 H2 sections with H3 subsections
- Page icon set to `https://www.google.com/s2/favicons?domain={DOMAIN}&sz=128`

After creating the database, grab its **data source ID** from the Notion URL or
via the Notion connector's `notion-get-data-sources` tool. Store that ID in
your private Computer memory — not in this repo.

---

## 3. Load the skill

The canonical workflow lives in
[`skills/brand-standards-audit/SKILL.md`](./skills/brand-standards-audit/SKILL.md).

To make Computer aware of it:

1. Copy the file into your Computer user-skills directory, or
2. Paste its contents when creating/editing the skill in the Computer UI.

Once loaded, invoke it with:

> "Run the brand-standards-audit skill for {BRAND_NAME} at {BRAND_URL} and add
> the results to my Notion brand standards database."

---

## 4. Seed the queue

Already done in this repo:

- `config/brands.json` — full ordered queue (170 brands with `name`, `url`,
  `domain`)
- `config/state.json` — starts with `current_index: 0`, empty `completed`, empty
  `failed`

If you want to add brands, append to `brands.json` — do not reorder entries the
cursor has already passed (it would re-audit or skip).

---

## 5. Schedule the cron

In Computer, create a scheduled task with:

- **Schedule:** `0 13 * * 0-5` UTC (= 8:00 AM Central, Sunday–Friday, no
  Saturday)
- **Exact:** true
- **Background:** false (foreground, because it writes files, calls subagents,
  and uses `notion-update-page` with `replace_content`)
- **Task prompt:** see `config/cron_task_template.md` below, or adapt to taste

### Minimum cron task prompt

```
Run today's daily brand audit.

1. Read config/state.json. Read config/brands.json.
2. Pick the brand at index = current_index.
3. Follow skills/brand-standards-audit/SKILL.md exactly.
4. Write the audit to audits/{brand-slug}.md.
5. Create a new Notion page in the brand standards database (name = brand,
   icon = favicon URL for the domain) and replace its body with the audit.
6. Update config/state.json: increment current_index, append the completed
   entry with brand, date, and notion_page_id.
7. Append a new row to logs/run_log.md.
8. Send an in-app notification titled "Brand Audit Complete: {BRAND}" with the
   Notion page URL. On failure, add to the failed[] array, log it, and still
   notify with the failure reason.
```

Record the cron ID Computer returns in your private notes — not here.

---

## 6. Smoke test

Before letting the daily schedule run on its own, do one manual invocation on
a known brand (e.g., your own company). Verify:

- [ ] Notion page was created with the correct name and favicon icon
- [ ] Page body has H1 title line + 10 H2 sections + H3 subsections
- [ ] At least 12 pages listed in Section 10
- [ ] `config/state.json` incremented and `completed[]` appended
- [ ] `logs/run_log.md` has a new row
- [ ] You got an in-app completion notification

If any step fails, see [RUNBOOK.md](./RUNBOOK.md#failure-modes).
