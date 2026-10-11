# Pitch Decks

Store deck outlines and speaker notes here as Markdown. Binary decks (`.pptx`, `.pdf`) usually belong outside git; reference them with `[EXTERNAL: Drive: Seed deck v3]`.

Naming: `YYYY-MM_stage_audience.md`, for example `2026-11_preseed_angels.md`.

Generate an outline with the `generate-pitch-deck` skill. Each outline should state its stage, audience, and the single point the deck must land.

Do not include cap table slides or detailed terms in files committed here.

## For AI assistants

- Follow `../../.claude/skills/generate-pitch-deck/SKILL.md` and `../../.claude/rules/investor-narrative.md`.
- Use only evidence present in the repo. Missing evidence is `[TBD: evidence needed]` plus a gap table, never invented numbers.
- Root rules: `../../CLAUDE.md` (or `../../AGENTS.md`).
