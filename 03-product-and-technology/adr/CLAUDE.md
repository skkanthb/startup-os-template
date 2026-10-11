# CLAUDE.md: adr/ folder rules

Applies when working on files in this folder. Root rules in `../../CLAUDE.md` still apply.

- ADRs are append-only. Never edit the decision, context, or consequences of an ADR whose status is `accepted`. To change a decision, create a new ADR and set the old one's `status` to `superseded by ADR-NNNN`. That status line is the only permitted edit.
- Number sequentially (four digits). List this folder to find the next number. Do not reuse or renumber.
- Always include "do nothing" among the options considered.
- Never invent options or rationale; ask the user for what is missing.
- Update the index in `README.md` when you add an ADR.
- Add each ADR's dependent assumptions to `../../08-risks-and-mitigations/blindspots_and_assumptions.md`.
- `0001-template.md` is a template, not a decision. Do not fill it in as a real ADR.
