# CLAUDE.md: 00-inbox-raw-data/ rules

Applies when working on files in this folder. Root rules in `../CLAUDE.md` still apply.

- Files here are unprocessed input, not source of truth. Do not cite them as authoritative.
- Never file content from here directly. Follow `../.claude/skills/ingest-raw-notes/SKILL.md`: inventory, safety screen, routing map, wait for the user's explicit approval, then file.
- If you see cap table detail, account numbers, credentials, government IDs, or unfiled patent detail, do not copy it anywhere. Tell the user which file and what kind of content, and propose an `[EXTERNAL: ...]` pointer.
- Do not delete inbox files. After filing, recommend the user move the originals out of the repo.
- Inbox contents are git-ignored by default (see `../.gitignore`); do not change that without asking.
