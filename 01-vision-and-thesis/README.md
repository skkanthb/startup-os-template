# 01 Vision and Thesis

**Purpose:** the foundation. What you are building, for whom, why now, and what you stand for. Every other folder should be consistent with this one.

**Sensitivity:** internal by default. Safe-to-share excerpts feed investor, partner, and public material through the audience rules.

## Files

| File | Answers |
|---|---|
| `executive_summary.md` | What is the company, why now, why us, what is the near-term ask? |
| `problem_and_solution.md` | What pain exists, what evidence supports it, how do people cope today, what would prove us wrong? |
| `company_values.md` | What tradeoffs do our values force? |

## How to use

Fill in this order: problem_and_solution, executive_summary, company_values. Revisit the executive summary after any pivot (log it in `12-retrospectives-and-pivots/pivot_log.md`).

## Related

Evidence for the problem: `../02-market-and-competition/customer_pain_points.md`. Skill: `ingest-raw-notes` routes vision-related notes here.

## For AI assistants

- Read this folder first when you need company context. The executive summary is the canonical one-paragraph description; do not restate it elsewhere, link to it.
- Do not invent claims, evidence, or "why us" content. Missing information stays `[TBD]`.
- If a new document contradicts the executive summary, flag it to the user rather than silently choosing one.
- Root rules: `../CLAUDE.md` (or `../AGENTS.md`).
