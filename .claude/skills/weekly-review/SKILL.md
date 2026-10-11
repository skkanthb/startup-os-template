---
name: weekly-review
description: Review the repo for stale documents, untested assumptions, overdue risks, unresolved placeholders, and decision gaps, then produce a prioritized action list. Use weekly or before any fundraising or planning session.
---

# Weekly Review

1. **Staleness.** Read front matter across the repo. List documents whose `last_reviewed` is older than 60 days (30 for `05-investors-and-fundraising/` and `08-risks-and-mitigations/`), and documents missing front matter.
2. **Placeholders.** Count `[TBD` and `[PLACEHOLDER` occurrences per folder. Report the folders least filled in.
3. **Assumptions.** Read `08-risks-and-mitigations/blindspots_and_assumptions.md`. List assumptions past their test deadline or untested with impact 4 or 5. Check that every `[ASSUMPTION]` tag in the repo appears in the log.
4. **Risks.** Read the risk register. List risks scoring 15+ with no mitigation plan, and risks not reviewed this month.
5. **Decisions.** Compare recent changes (git log if available) against ADRs. Flag apparent decisions with no ADR.
6. **Contradictions.** Spot-check the executive summary against the roadmap, GTM, and investor memo for conflicting claims.
7. **Never-commit scan.** Search for patterns suggesting sensitive data (account numbers, keys, equity percentages). Report locations without repeating the values.
8. **Output.** Save `13-generated-outputs/YYYY-MM-DD_weekly-review.md` with a ranked top-five action list first, then findings by category. Be direct about what is weak.
9. End with **Strategic Suggestions & Next Options**.
