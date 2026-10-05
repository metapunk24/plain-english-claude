# Oxford Plain English Copywriting — Claude Skill

A plain-English rewriting skill for [Claude](https://claude.ai), based on Martin Cutts' *Oxford Guide to Plain English* (5th ed., 2020).

## What it does

Takes any foggy, jargon-filled text — legal documents, emails, reports, contracts — and rewrites it into clear, reader-centred prose. Works for English and Russian texts.

**Standard output: two documents**
1. **Rewritten text** — brief diagnosis + clean plain-English version, ready to use
2. **Change report** — every edit, the principle applied, why it helps the reader, metrics before vs. after

Optional: export the result to Word with `scripts/docx-export.py`.

## Install

**Claude Code:** clone into `~/.claude/skills/oxford-plain-english-copywriting/`.

**Claude.ai / desktop:** zip the folder (with `SKILL.md` at the root of the folder) and upload it in Settings → Capabilities → Skills.

## Structure

```
oxford-plain-english-copywriting/
  SKILL.md                         ← Main skill file (YAML frontmatter: name + description)
  references/
    thirty-guidelines.md           ← All 30 chapters of Cutts' book
    examples-bank.md               ← Before/after examples by category
    quick-checklist.md             ← 20-point pre-publication checklist
    readability-tools.md           ← Readability formulas and targets
    source-notes.md                ← Book structure, chapter map, OCR error log
  templates/
    rewrite-template.md            ← Two-document output template
  scripts/
    docx-export.py                 ← Markdown → Word export (needs python-docx)
```

## Metrics

- **Target sentence length:** 15–20 words average
- **Target reading age:** 13 (general UK/US audience)
- **Target active voice:** >70%
- **Max noun string:** 2 nouns (3+ = "knotty")

## License

MIT — based on publicly documented principles from *Oxford Guide to Plain English*.

## Author

**MetaPunk** (`metapunk24`) — assembled and tested for Claude.
