# 08 Risks and Mitigations

**Purpose:** what could go wrong, what you are assuming without proof, and what you will do about it.

**Sensitivity:** internal. Candor matters more here than anywhere else; a risk register that hides risks is worse than none.

## Files

| File | Answers |
|---|---|
| `risk_register.md` | What are the risks, scored by likelihood and impact, with owners and early-warning signals? |
| `blindspots_and_assumptions.md` | Which beliefs are untested, how bad if wrong, and when will we test them? |
| `mitigation_plans.md` | For high-scoring risks, what is the trigger and the contingency? |

## How to use

Every `[ASSUMPTION]` tag in the repo gets a row in the assumptions file. Any risk scoring 15 or more needs a mitigation plan. Review monthly; the `weekly-review` skill checks for gaps.

## Related

Decisions create risks: see `../03-product-and-technology/adr/`.

## For AI assistants

- Challenge optimism. If a document makes a claim with no evidence, add it to the assumptions log and say so.
- Do not downplay scores to make the register look tidy. If nothing scores high, ask what is being missed.
- When a decision, pivot, or new document implies a new risk, propose a row; do not add silently.
- For audits, use `../.claude/rules/regulatory-audit.md` and describe only controls that exist.
- Root rules: `../CLAUDE.md` (or `../AGENTS.md`).
