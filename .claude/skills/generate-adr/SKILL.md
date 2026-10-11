---
name: generate-adr
description: Write an Architecture or Product Decision Record in 03-product-and-technology/adr/ from a decision the user describes. Use when a significant technical, product, or strategic choice has been made or is being weighed.
---

# Generate ADR

1. Read `03-product-and-technology/adr/0001-template.md` and list existing files in `adr/` to find the next number (zero-padded, four digits).
2. Ask for anything missing that you cannot infer: the context, options considered, and why the chosen option won. Do not invent options or rationale.
3. Check whether this decision supersedes an earlier ADR. If so, set the old ADR's `status` to `superseded by ADR-NNNN` and nothing else in it.
4. Write `adr/NNNN-short-kebab-title.md` using the template. Always include "do nothing" as an option.
5. List the assumptions the decision depends on and add each to `08-risks-and-mitigations/blindspots_and_assumptions.md`. Add any new risk to the risk register after asking the user.
6. Set a concrete revisit trigger.
7. Report the new file path and any open questions. Include **Strategic Suggestions & Next Options**.
