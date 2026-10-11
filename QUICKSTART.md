# Quickstart

About 20 minutes to a working setup.

## 1. Create your copy

Option A, GitHub template: click **Use this template**, then **Create a new repository**. Choose **Private**.

Option B, clone and re-initialize:

```bash
git clone https://github.com/<owner>/startup-os-template.git my-startup-os
cd my-startup-os
rm -rf .git
git init -b main
git add .
git commit -m "chore: initialize from startup-os-template"
```

Then create your own private repo and push.

## 2. Fill in the basics

1. Edit `CLAUDE.md` section 1 (company, stage, owner).
2. Edit `LICENSE`: replace `[YOUR NAME]`, or swap the license entirely. A private startup repo usually should not carry an open-source license.
3. Fill `01-vision-and-thesis/executive_summary.md`. Write what you actually know; leave `[TBD]` elsewhere.

## 3. Feed it raw material

1. Drop notes, transcripts, or brain dumps into `00-inbox-raw-data/`.
2. In Claude Code, run: "Run the ingest-raw-notes skill on everything in 00-inbox-raw-data."
3. Review the inventory and routing map. Approve, adjust, or reject.
4. Only then does the assistant write files.

In a Claude Project instead of Claude Code: paste `CLAUDE.md` into project instructions, upload `.claude/skills/ingest-raw-notes/SKILL.md`, paste your notes into a message, and download generated files into the right folders yourself.

## 4. Build the habit

- After any real decision: run `generate-adr`.
- Weekly: run `weekly-review` and act on the top three findings.
- Before any outside conversation: run `generate-briefing` for that audience and read the Leak check before sending.

## 5. Before you commit anything sensitive

Re-read the "Never commit" list in `CLAUDE.md`. If in doubt, store it elsewhere and reference it with `[EXTERNAL: ...]`.
