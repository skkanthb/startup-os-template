---
name: ingest-raw-notes
description: Process unstructured material in 00-inbox-raw-data/ into the right startup-os documents. Inventories first, flags contradictions, proposes a routing map, and files only after the user approves. Use when the user drops notes, transcripts, or brain dumps and asks to process, file, or ingest them.
---

# Ingest Raw Notes

Never write to a target document until the user has approved the routing map (step 4).

## Steps

1. **Inventory.** List every file in `00-inbox-raw-data/` (excluding README and .gitkeep). For each: name, type, approximate size, one-line summary. If the folder is empty, say so and stop.
2. **Safety screen.** Scan for content on the "Never commit" list in `CLAUDE.md` (cap table detail, account numbers, credentials, government IDs, unfiled patent detail, third-party personal data). If found, do not copy it anywhere. Tell the user which file and what kind of content, and propose an `[EXTERNAL: ...]` pointer instead.
3. **Extract and check.** From each source, extract discrete items: facts, decisions, assumptions, risks, action items, customer evidence, open questions. Compare against existing documents and flag:
   - **Contradictions** with current content (quote both, name the files)
   - **Duplicates** of what is already filed
   - **Claims with no source** (tag `[ASSUMPTION]`)
4. **Routing map (stop here for approval).** Present a table: item, proposed target file, action (add / update / supersede), and confidence. Include decisions that deserve an ADR and assumptions that belong in `08-risks-and-mitigations/blindspots_and_assumptions.md`. Ask the user to approve, edit, or reject. Do not continue without an explicit answer.
5. **File.** Apply only approved changes. For updates to existing living documents, archive the prior version as `archive/YYYY-MM-DD_<filename>` beside the file first. Decisions become new ADRs, never silent edits. Preserve the source's wording for quotes and evidence.
6. **Report.** Write `13-generated-outputs/YYYY-MM-DD_ingestion-report.md` listing what was filed where, what was skipped and why, unresolved contradictions, and open questions.
7. **Clean up.** Tell the user the inbox originals have been processed and recommend moving them out of the repo. Do not delete them yourself.

## Rules

- No fabrication. If a template section has no supporting source, leave it `[TBD]`.
- Do not merge conflicting claims; surface them.
- Keep one fact in one home and link elsewhere.
- End with a **Strategic Suggestions & Next Options** section (two or three items).
