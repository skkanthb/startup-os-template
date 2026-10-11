# 11 Finance and Metrics

**Purpose:** how the business is measured, and the logic behind runway and financial planning.

**Sensitivity:** high. No bank balances, account numbers, or the financial model itself. Keep the model in a spreadsheet or accounting system and reference it as `[EXTERNAL: ...]`. This repo holds definitions and assumptions only.

## Files

| File | Answers |
|---|---|
| `metrics_definitions.md` | What exactly does each metric mean, where does the data come from, what decision does it drive? |
| `runway_and_model_notes.md` | What assumptions drive the model, how is runway calculated, and what triggers action? |

## How to use

Define a metric here before using it anywhere else. Update current values with an "as of" date.

## Related

Fundraising timing depends on runway: `../05-investors-and-fundraising/fundraising_tracker.md`.

## For AI assistants

- Use only metrics defined in `metrics_definitions.md` in investor or public material, with value, date, and source.
- Label projections as projections and list their assumptions. Do not generate unit economics from nothing.
- Do not record actual balances, salaries, or account details.
- Root rules: `../CLAUDE.md` (or `../AGENTS.md`).
