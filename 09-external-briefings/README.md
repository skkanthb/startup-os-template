# 09 External Briefings

Generated, sanitized documents for people outside the core team. Nothing in here is a source of truth; each file is derived from internal documents under a specific audience rule.

| Folder | Audience | Rule file |
|---|---|---|
| `candidates/` | Potential contributors, technical hires | `.claude/rules/candidate-scoping.md` |
| `partners/` | Integration partners, technical advisors | `.claude/rules/partner-briefing.md`, `.claude/rules/technical-briefing.md` |
| `public_talks/` | Conferences, meetups, public posts | `.claude/rules/public-conference.md` |

## Process

1. Generate with the `generate-briefing` skill.
2. Read the **Leak check** at the bottom of the generated file.
3. A human approves before the file leaves the repo.
4. Name files `YYYY-MM-DD_<audience>_<topic>.md`.

## For AI assistants

- Identify the audience, read the matching file in `.claude/rules/`, then follow `.claude/skills/generate-briefing/SKILL.md`.
- Produce standalone documents with no repo links, and end every file with a Leak check.
- Folder rules: `CLAUDE.md` in this folder. Root rules: `../CLAUDE.md` (or `../AGENTS.md`).

## Warning

If this repo is private and you share these files by copy or export, that is safe. If you grant someone access to the repo itself, they can read everything, including history. Share exported copies, not repo access.
