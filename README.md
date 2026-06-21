# Plain English Copywriting — Claude Skill

A plain-English rewriting skill for [Claude](https://claude.ai), based on Martin Cutts' *Oxford Guide to Plain English* (5th ed., 2020).

## What it does

Takes any foggy, jargon-filled text — legal documents, emails, reports, contracts — and rewrites it into clear, reader-centred prose.

**Standard output: two documents**
1. **Rewritten text** — clean plain-English version, ready to use
2. **Change report** — standalone audit explaining every edit, principle applied, and before/after comparison

## Install

Copy the contents of this folder into your Claude project or context directory:

```
.claude/
  plain-english.mdc            ← Main skill file
  references/
    examples-bank.mdc
    quick-checklist.mdc
    readability-tools.mdc
    thirty-guidelines.mdc
  templates/
    rewrite-template.mdc
```

Or simply paste `plain-english.mdc` into the chat context when working on a rewrite.

## Structure

| File | Purpose |
|------|---------|
| `SKILL.mdc` | Main skill file — no YAML frontmatter, adapted for Claude |
| `references/thirty-guidelines.mdc` | All 30 chapters from Cutts' book |
| `references/examples-bank.mdc` | Before/after examples by category |
| `references/quick-checklist.mdc` | 20-point pre-publication checklist |
| `references/readability-tools.mdc` | Readability formulas and targets |
| `templates/rewrite-template.mdc` | Structured template for rewrites |

## Metrics

- **Target sentence length:** 15–20 words average
- **Target reading age:** 13 (general UK/US audience)
- **Target active voice:** >70%
- **Max noun string:** 2 nouns (3+ = "knotty")

## License

MIT — based on publicly documented principles from *Oxford Guide to Plain English*.

## Author

**MetaPunk** (`metapunk24`) — assembled and tested for Claude.
