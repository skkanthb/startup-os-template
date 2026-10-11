# AGENTS.md: Entry Point for AI Assistants

This file is for any AI assistant or coding agent working in this repository (OpenAI Codex, Gemini, Cursor, Copilot, Claude, or others). It is a short, tool-neutral summary. The full standing instructions are in [CLAUDE.md](CLAUDE.md); read that file too, the rules apply to every assistant, not only Claude.

## What this repository is

A docs-as-code operating system for a startup: Markdown files that hold strategy, market, product, go-to-market, fundraising, team, risk, legal, and finance knowledge. It contains no application code.

## Navigation in under a minute

1. Read `CLAUDE.md` (rules and conventions).
2. Read `01-vision-and-thesis/executive_summary.md` for company context. If it is still placeholders, the repo is a fresh template: ask the user for context rather than guessing.
3. Each numbered folder has a `README.md` stating its purpose, files, and a "For AI assistants" section. Read the folder README before editing inside that folder.
4. Audience rules for outside-facing documents: `.claude/rules/`.
5. Repeatable workflows (ingest notes, write a decision record, pitch outline, external briefing, weekly review): `.claude/skills/<name>/SKILL.md`. These are written as plain Markdown instructions. If your tool has no skill system, open the file and follow its steps as a checklist.

## Folder map

| Folder | Contents |
|---|---|
| `00-inbox-raw-data/` | Unprocessed input. Never treat as source of truth. |
| `01-vision-and-thesis/` | Vision, problem, values |
| `02-market-and-competition/` | Market sizing, competitors, customer evidence |
| `03-product-and-technology/` | Architecture, roadmap, IP strategy, `adr/` decision records |
| `04-go-to-market-and-sales/` | GTM, ICP, sales enablement |
| `05-investors-and-fundraising/` | Memo, tracker, deck outlines |
| `06-team-and-organization/` | Founder roles, hiring, onboarding |
| `07-stakeholders-and-contacts/` | Stakeholder map and relationship log |
| `08-risks-and-mitigations/` | Risk register, assumptions, mitigation plans |
| `09-external-briefings/` | Generated, sanitized outputs for outside audiences |
| `10-legal-and-corporate/` | Index of legal documents (not the documents) |
| `11-finance-and-metrics/` | Metric definitions and model logic (not the model) |
| `12-retrospectives-and-pivots/` | Retrospectives and pivot log |
| `13-generated-outputs/` | Internal generated reports |

## Non-negotiable rules (summary; full text in CLAUDE.md)

- **Do not fabricate.** Missing information is written `[TBD: what is needed]`. Never invent numbers, customers, quotes, or competitors.
- **Never write sensitive data into any file:** cap table or equity percentages, SAFE or note terms, bank or card numbers, credentials, government IDs, unfiled patent detail. Use `[EXTERNAL: <system>: <description>]` pointers instead. Git history is permanent.
- **Do not edit accepted decision records.** Supersede them with a new ADR.
- **Confirm with the user before moving, renaming, or deleting files.**
- **Tag untested beliefs** `[ASSUMPTION]` and log them in `08-risks-and-mitigations/blindspots_and_assumptions.md`.
- **Outside audiences:** load the matching file in `.claude/rules/` first; end the output with a Leak check; a human reviews before anything is sent.
- **Challenge flawed premises** rather than agreeing with them.

## Document front matter

Every document begins with `title`, `status`, `owner`, `last_reviewed`, and `audience`. Keep `last_reviewed` honest; the weekly review uses it.

## Search tips

- Find open work: search for `[TBD` and `[ASSUMPTION`.
- Find external pointers: search for `[EXTERNAL:`.
- Find stale documents: read `last_reviewed` in front matter.
- Find decisions: list `03-product-and-technology/adr/` and read its README index.
