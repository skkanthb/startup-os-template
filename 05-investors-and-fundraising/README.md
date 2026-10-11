# 05 Investors and Fundraising

**Purpose:** investor-facing narrative and the fundraising pipeline.

**Sensitivity:** high. Never commit cap table detail, term sheet economics, SAFE or note terms, or wiring details. Reference them as `[EXTERNAL: data room / Carta / counsel]`.

## Files and folders

| Path | Answers |
|---|---|
| `investor_memo.md` | The full written narrative for venture investors |
| `fundraising_tracker.md` | Who we are talking to, status, passes and reasons |
| `pitch_decks/` | Deck outlines and speaker notes per stage and audience |

## How to use

Write the memo first; decks are derived from it. Update the tracker after every investor touchpoint. Generate deck outlines with the `generate-pitch-deck` skill.

## Related

Evidence and sizing: `../02-market-and-competition/`. Risks to disclose candidly: `../08-risks-and-mitigations/risk_register.md`. Runway: `../11-finance-and-metrics/`.

## For AI assistants

- Load `../.claude/rules/investor-narrative.md` before writing anything here.
- Every metric needs value, date, and source. Never imply traction, customers, or partnerships that are not documented.
- Do not copy detail from `../06-team-and-organization/cofounder_agreements.md` equity discussion into investor material.
- Fundraising communications can carry legal obligations; remind the user to involve counsel before distribution.
- Root rules: `../CLAUDE.md` (or `../AGENTS.md`).
