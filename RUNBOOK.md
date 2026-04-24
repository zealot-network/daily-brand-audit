# Runbook

Day-to-day operations for the daily brand audit pipeline. Start here when
something needs attention.

---

## Daily happy path

Each morning at 8:00 AM Central (Sun–Fri) the cron fires and executes the
skill against the brand at `config/state.json.current_index`. You should see:

- A new row in `logs/run_log.md`
- A new page in the Notion brand-standards database
- An in-app notification titled "Brand Audit Complete: {BRAND}"
- `config/state.json.current_index` incremented by 1
- A new entry appended to `config/state.json.completed[]`

Nothing for you to do on a clean day.

---

## Common operations

### Expedite a specific brand (out-of-band)

When you need a brand audited immediately without touching the queue:

> "Run the brand-standards-audit skill for {BRAND_NAME} at {BRAND_URL} right
> now. Do **not** advance the daily cursor. Mark this run as on-demand in
> `logs/run_log.md`."

The agent will write a Notion page and log it, but leave `current_index` and
`completed[]` alone (or tag the completed entry with `"method": "on-demand
expedited"` for traceability).

### Add a brand to the queue

Append to `config/brands.json`. Never insert before `current_index` — the
cursor would either re-audit or skip.

### Pause the schedule

Tell Computer: "Pause my daily brand audit task." That deletes the cron. When
you're ready, create a new one with the same schedule in
[SETUP.md §5](./SETUP.md#5-schedule-the-cron). There is no "paused" state —
active or deleted only.

### Change the time or days

Edit the cron schedule directly. UTC format: `MIN HOUR * * DAYS`. Remember
Central is UTC−5 or UTC−6 depending on DST, so recompute each time you change
it.

---

## Reconciling state after an interrupted run

This is the most common manual fix. If a run wrote to Notion but never updated
`state.json` / `run_log.md` (e.g., the conversation was summarized mid-flow):

1. **Verify the Notion page exists** and has the full audit body (not just
   placeholder text). Use the Notion connector or open the page.
2. **Bump `config/state.json`:**
   - Increment `current_index` by 1
   - Append to `completed[]`:
     ```json
     {
       "brand": "<Brand Name>",
       "date": "YYYY-MM-DD",
       "notion_page_id": "<id from Notion>"
     }
     ```
3. **Append to `logs/run_log.md`** — one row in the history table, and update
   the "Latest Run" header.
4. **Commit and push** (if you're tracking in git).

Skip step 1 and you may double-audit the brand the next morning. Skip step 2
and the queue gets stuck.

---

## Failure modes

### Cron fired but no audit produced

Check the conversation in Computer for the cron ID. If the agent errored:
- If it's a transient browser/network failure, re-run manually for that brand.
- If the brand's site is bot-blocked or unreachable, move it to
  `config/state.json.failed[]` with a reason and increment `current_index`.

### Notion page created but empty or truncated

The most common cause: `notion-update-page` with `replace_content` hit a size
limit or got interrupted before finishing. Fix:

1. Re-run the write step — not the whole audit. The audit markdown is already
   on disk at `audits/{brand}.md`.
2. Spawn a subagent: "Read `audits/{brand}.md` in full and replace the body of
   Notion page `<id>` with it. Do not summarize or abbreviate."
3. Spot-check the page afterwards.

### Audit shallower than standard

If a completed audit is visibly thinner than peers (short sections, fewer than
12 pages browsed, missing hex codes), flag the brand for a re-run:

1. Move its `completed[]` entry to a `redo[]` array or delete it entirely.
2. Delete or archive the Notion page.
3. Expedite the brand manually.

### Saturday accidental run

The cron is `0-5` (Sun–Fri). If Saturday ever runs, the schedule was edited.
Restore to `0 13 * * 0-5` UTC.

---

## Quality bar (what "done" means)

A run is only Done when every box is checked:

- [ ] 12+ pages browsed, all listed in Section 10
- [ ] Every hex code has `#` and a usage context
- [ ] Every font family is named (not just "sans-serif")
- [ ] All 10 sections at equivalent depth (no section shorter than Brand Voice)
- [ ] Notable absences called out in each relevant section
- [ ] Notion page icon = `https://www.google.com/s2/favicons?domain={DOMAIN}&sz=128`
- [ ] `state.json` + `logs/run_log.md` updated
- [ ] Notification sent

If any box is empty, the run isn't done — go back and finish it.

---

## Maintenance

- **Quarterly:** re-audit brands whose sites have visibly changed. Mark the
  re-run in `logs/run_log.md` and leave the prior audit in place (or archive
  it under `audits/archive/{brand}-{date}.md`).
- **When the queue is empty:** decide whether to rotate (re-audit from the
  top), grow the list, or sunset the schedule.
- **When templates change:** update `config/audit_prompt.md` **and**
  `skills/brand-standards-audit/SKILL.md` together. Never let them drift.
