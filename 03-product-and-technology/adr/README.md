# Architecture and Product Decision Records (ADRs)

**Purpose:** a dated, append-only record of significant decisions: what was decided, why, what else was considered, and when to revisit.

## How to use

1. Copy `0001-template.md` to `NNNN-short-kebab-title.md` (next four-digit number).
2. Fill every section. Always include "do nothing" as an option.
3. Set `status` to `proposed`, then `accepted` once decided.
4. To change a decision, write a new ADR and mark the old one `superseded by ADR-NNNN`. Do not rewrite history.

The `generate-adr` skill (`../../.claude/skills/generate-adr/SKILL.md`) automates this.

## Naming

`0002-use-postgres-for-primary-store.md`, `0003-defer-mobile-app.md`.

## Index

Keep a running list here so assistants and humans can scan decisions quickly.

| ADR | Title | Status | Date |
|---|---|---|---|
| 0001 | Template (do not use as a real decision) | template | n/a |

## For AI assistants

- Read this index before proposing a decision; check whether one already exists or has been superseded.
- Number sequentially; list the folder to find the next number.
- Never modify the decision text of an accepted ADR.
- Add each ADR's dependent assumptions to `../../08-risks-and-mitigations/blindspots_and_assumptions.md`.
