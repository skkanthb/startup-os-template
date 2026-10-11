---
name: generate-pitch-deck
description: Produce a stage-appropriate pitch deck outline with speaker notes from the repo's current documents. Use when the user wants a pre-seed, seed, or Series A deck outline or a pitch rewrite for a specific audience.
---

# Generate Pitch Deck Outline

1. Load `.claude/rules/investor-narrative.md` and follow it.
2. Ask (if not stated): stage, audience (angel, seed fund, strategic), and the one point the deck must land.
3. Read `01-vision-and-thesis/`, `02-market-and-competition/`, `04-go-to-market-and-sales/gtm_strategy.md`, `05-investors-and-fundraising/investor_memo.md`, and `08-risks-and-mitigations/risk_register.md`. Use only what is there.
4. Draft an outline (typically 10-14 slides). For each slide: title, the single claim, supporting evidence with source, and speaker notes. Stage guidance:
   - Pre-seed: problem insight, founder fit, early validation, vision
   - Seed: traction evidence, repeatable acquisition signals, unit economics (estimated or actual), team
   - Series A: proven growth and retention, unit economics at scale, expansion plan
5. Where evidence is missing, write `[TBD: evidence needed]` and list it in a gap table at the end. Never fill the gap with invented numbers.
6. Do not include cap table slides, individual equity, or confidential customer names.
7. Save as `05-investors-and-fundraising/pitch_decks/YYYY-MM_<stage>_<audience>.md`.
8. Append a **Leak check** and **Strategic Suggestions & Next Options** (including the weakest slide and the toughest likely investor question).
