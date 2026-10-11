# Startup OS Template

A docs-as-code operating system for a startup. Plain Markdown in a git repo, structured so an AI assistant (Claude Code or a Claude Project) can read it, keep it current, and produce audience-safe documents from it.

It is not software. There is no app to run. The value is the structure, the conventions, and the on-demand skills in `.claude/`.

## What problem this solves

Early-stage strategy lives in scattered notes, chats, decks, and one person's head. Decisions get lost, assumptions never get tested, and every investor, candidate, or partner conversation means rebuilding context from scratch.

This template gives you:

1. **One source of truth** for non-code strategy: vision, market, product, go-to-market, fundraising, team, risks, legal, finance.
2. **An ingestion pipeline.** Drop raw notes into `00-inbox-raw-data/`; an AI-assisted workflow inventories them, proposes where each piece belongs, and files only after you approve.
3. **Decision records.** Why you chose something is written down, dated, and never silently overwritten.
4. **Audience-scoped outputs.** Rules in `.claude/rules/` define what each audience (investor, candidate, partner, public, auditor) may and may not see.
5. **A weekly review loop** that surfaces stale docs, untested assumptions, and open risks.

## Quickstart

See [QUICKSTART.md](QUICKSTART.md). Short version:

1. Click **Use this template** on GitHub (or clone and re-initialize git).
2. Replace every `[PLACEHOLDER]` in `CLAUDE.md` and `01-vision-and-thesis/executive_summary.md`.
3. Drop a few raw notes into `00-inbox-raw-data/` and run the ingestion skill.
4. Keep the repo **private** while it holds real startup content.

## Structure

Every numbered folder has its own `README.md` explaining its purpose, files, how to use them, and what must never go there. Start with the folder's README.

| Folder | Purpose |
|---|---|
| `00-inbox-raw-data/` | Drop zone for unstructured notes, transcripts, brain dumps |
| `01-vision-and-thesis/` | Vision, problem/solution, values |
| `02-market-and-competition/` | Market sizing, competitors, customer research |
| `03-product-and-technology/` | Architecture, roadmap, IP strategy, decision records (`adr/`) |
| `04-go-to-market-and-sales/` | GTM, ICP and personas, sales enablement |
| `05-investors-and-fundraising/` | Memo, tracker, pitch material |
| `06-team-and-organization/` | Founder agreements, hiring plan, onboarding |
| `07-stakeholders-and-contacts/` | Stakeholder map, relationship log |
| `08-risks-and-mitigations/` | Risk register, assumptions, mitigation plans |
| `09-external-briefings/` | Generated, sanitized documents for outside audiences |
| `10-legal-and-corporate/` | Entity, IP assignments, contracts index |
| `11-finance-and-metrics/` | Metrics definitions, runway, model notes |
| `12-retrospectives-and-pivots/` | Retrospectives and pivot logs |
| `13-generated-outputs/` | Internal generated artifacts (briefs, summaries, reviews) |
| `.claude/rules/` | Audience and IP-containment rules |
| `.claude/skills/` | On-demand workflows (ingest, ADR, briefing, review, pitch) |

## Important limitations (read these)

- **Folder-based access control is a prompting convention, not security.** Anything committed to git, including to a private repo, can be read by anyone with repo access and remains in history after deletion. Never commit cap tables, bank details, credentials, government IDs, or unfiled patent drafts. Use `[EXTERNAL: <system>]` pointers instead (see `CLAUDE.md`).
- **Generated briefings need human review before they leave your hands.** The rules reduce leakage risk; they do not eliminate it.
- **Public disclosure can affect patent rights.** Do not publish technical detail you may want to patent. Talk to a patent attorney first.
- **This is not legal, tax, or investment advice.**
- **The AI will draft; you decide.** Treat generated content as a first draft that needs verification, especially market numbers and citations.

## How it works with Claude

- In **Claude Code**, `CLAUDE.md` loads automatically and skills in `.claude/skills/` are available to the session.
- In a **Claude Project**, paste `CLAUDE.md` into the project instructions and upload the folders you want searchable. Generated files then need to be downloaded and committed manually.

## For AI assistants (Claude, OpenAI, Gemini, Cursor, others)

The repo is written to be navigated by AI tools as well as people:

- [AGENTS.md](AGENTS.md): tool-neutral entry point with a folder map and the non-negotiable rules. Tools that read `AGENTS.md` (for example OpenAI Codex) pick it up automatically.
- [CLAUDE.md](CLAUDE.md): full standing instructions. Claude Code loads it automatically; for other tools, paste it into the system prompt or project instructions.
- Each folder's `README.md` ends with a "For AI assistants" section. Three folders also have a short `CLAUDE.md` with folder-specific rules (`00-inbox-raw-data/`, `03-product-and-technology/adr/`, `09-external-briefings/`).
- `.claude/skills/*/SKILL.md` are plain-Markdown workflows. Claude Code discovers them as skills; any other assistant can open one and follow it as a checklist.

How well a given tool follows these files varies. Treat them as strong guidance and review what the assistant writes.

## Roadmap

- [ ] Audience-scoping generator that redacts any document per the rules in `.claude/rules/`
- [ ] Worked example company end to end
- [ ] Stale-doc and assumption-expiry checks in CI
- [ ] Optional Obsidian vault configuration

## Contributing

Issues and pull requests welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT. See [LICENSE](LICENSE).
