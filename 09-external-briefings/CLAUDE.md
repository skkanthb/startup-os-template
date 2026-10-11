# CLAUDE.md: 09-external-briefings/ rules

Applies when working on files in this folder. Root rules in `../CLAUDE.md` still apply.

- Nothing here is a source of truth. Every file is derived from internal documents under a specific audience rule in `../.claude/rules/`. Never create content here that does not exist, in safe form, in the source documents.
- Before writing, identify the audience and read the matching rule file completely. If none matches, ask the user; do not improvise.
- Write standalone documents: no links into the repo, no internal file names or internal-only terms.
- Every file ends with a **Leak check** section: categories excluded, every figure/name/technical description included (for human verification), any IP or patent concern, and whether an NDA is advisable.
- Do not open or quote documents on the audience rule's exclusion list while drafting.
- A human must review before anything leaves the repo. Never suggest granting repo access as a way to share; share exported copies.
- Naming: `YYYY-MM-DD_<audience>_<topic>.md`, in `candidates/`, `partners/`, or `public_talks/`.
