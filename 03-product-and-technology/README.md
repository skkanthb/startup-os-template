# 03 Product and Technology

**Purpose:** what you are building and how, at the level an advisor needs. Architecture, roadmap, IP strategy, and the decision records that explain why.

**Sensitivity:** internal. Highest IP risk in the repo. Never store unfiled invention detail, credentials, or internal endpoints. Implementation detail belongs in your code repository.

## Files and folders

| Path | Answers |
|---|---|
| `high_level_architecture.md` | What are the components, data flows, and trust boundaries? |
| `product_roadmap.md` | What is the MVP, and what outcomes come next? |
| `ip_and_patent_strategy.md` | What is core IP, how is it protected, what is open source? Includes a public disclosure log. |
| `adr/` | Decision records. One file per decision, never edited after acceptance. |

## How to use

Record each significant choice as an ADR first (`generate-adr` skill), then link it from the architecture or roadmap file.

## Related

Risks that follow from decisions: `../08-risks-and-mitigations/`. Safe external versions: `../09-external-briefings/`.

## For AI assistants

- Do not describe novel mechanisms in detail anywhere. If asked to, stop and recommend the user consult a patent attorney first; paraphrasing is still disclosure.
- Decisions go in `adr/`. Never edit an accepted ADR's decision; write a new one that supersedes it.
- Do not paste code, secrets, or infrastructure identifiers here.
- Root rules: `../CLAUDE.md` (or `../AGENTS.md`). Folder rules for `adr/`: `adr/CLAUDE.md`.
