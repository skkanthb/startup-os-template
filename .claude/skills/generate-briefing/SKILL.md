---
name: generate-briefing
description: Produce an audience-scoped, sanitized external briefing (candidate, partner, technical advisor, public talk, enterprise, or audit) from internal documents, following the matching rule file. Use before sharing anything about the startup with an outside party.
---

# Generate External Briefing

1. Identify the audience. If unclear, ask. Map it to a rule file in `.claude/rules/` and read that file completely. If no rule matches, ask the user before writing.
2. Ask for the purpose and the specific outcome wanted (for example "candidate to scope the ingestion module").
3. Select source documents. Use only material the rule allows. Do not open or quote documents on the rule's exclusion list.
4. Draft a standalone document: no links into the repo, no references to internal file names, no internal-only terminology.
5. Save to the location the rule specifies (`09-external-briefings/<audience>/YYYY-MM-DD_<audience>_<topic>.md`).
6. Append a **Leak check** section:
   - Categories excluded and why
   - Every figure, name, or technical description included, for the human to verify
   - Any IP or patent concern (public disclosure risk)
   - Whether an NDA is recommended before sending
7. State plainly that a human must review before it leaves the repo, and that sending repo access instead of an exported copy defeats the scoping.
8. Include **Strategic Suggestions & Next Options**.
