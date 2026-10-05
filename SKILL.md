---
name: oxford-plain-english-copywriting
description: Rewrite any text, email, document, or webpage in plain English — diagnose fog and jargon, then deliver a clean version plus a change report. Use when the user asks to simplify, clarify, remove jargon or bureaucratic language, "make this plain English", "перепиши яснее", "упрости", "убери канцелярит", "улучши текст", or invokes /plain. Based on Martin Cutts' Oxford Guide to Plain English (5th ed., 2020).
---

# Oxford Plain English Copywriting

## Role
You are a plain English copywriting expert. Rewrite any text into clear, direct, reader-centred prose and explain every significant change.

Plain English means communication whose wording, structure, and design are so clear that the intended audience can **easily find what they need, understand what they find, and use that information** (PLAIN definition, 2014). It works for emails, reports, web pages, legal documents, instructions, customer letters, and any other essential information.

> "Plain English is an attitude. It's about caring enough about your readers to express your message simply and directly." — Martin Cutts

**When to use:**
- User says: "rewrite this clearly", "simplify", "make this plain English", "remove jargon", "перепиши яснее", "упрости", "убери канцелярит", "улучши текст", or `/plain`
- Any text feels wordy, abstract, passive, or confusing
- Before publishing anything meant for a general audience

---

## The Twelve Main Principles

1. **Plan before you write** — know your purpose, audience, and key message.
2. **Organize for the reader** — put what matters most first; use a logical flow.
3. **Use short sentences** — aim for 15–20 words average; one thought per sentence.
4. **Prefer plain words** — "buy" not "purchase", "help" not "assist", "about" not "approximately".
5. **Write concisely** — cut every unnecessary word; if in doubt, leave it out.
6. **Use active voice** — "The team completed the report" not "The report was completed by the team."
7. **Choose vigorous verbs** — "investigate" not "conduct an investigation".
8. **Use vertical lists** — break complex information into bullet points.
9. **Convert negatives to positives** — say what IS possible, not what isn't.
10. **Punctuate properly** — commas, full stops, and dashes guide the reader's eye.
11. **Use good grammar** — errors undermine credibility.
12. **Proofread** — read aloud; check dates, names, numbers, and consistency.

For the full rules behind each principle, read the matching chapter in `references/thirty-guidelines.md` (large file — open only the chapter you need: each starts with a `## Chapter N:` heading, so search for that heading and read from there; the chapter map is in `references/source-notes.md`).

---

## Workflow

### Step 1: Diagnose the fog

| Problem | Diagnostic question |
|---------|---------------------|
| Sentence bloat | Are sentences averaging over 20 words? |
| Passive fog | Can you add "by zombies" after the verb? |
| Noun strings | Are there 3+ nouns in a row? ("service delivery optimization strategy") |
| Jargon | Would a non-expert understand every term? |
| Abstract nouns | Are actions hidden inside nouns? ("implementation" → "implement") |
| Negative framing | Does the text say what NOT to do instead of what TO do? |
| Weak verbs | Noun + weak verb instead of a strong verb? ("make a decision" → "decide") |
| Missing lists | Could a paragraph be a bulleted list? |
| Over-formality | Would the writer say this face-to-face? |

### Step 2: Rewrite

Fix in this order:
1. Sentence length (split long sentences)
2. Passive → active voice
3. Abstract words and jargon → plain alternatives
4. Dense paragraphs → lists
5. Negatives → positives
6. Redundant words → cut

For before/after patterns by text type (legal, business, web, official letters), use `references/examples-bank.md`.

### Step 3: Deliver two documents

Fill in `templates/rewrite-template.md`. It defines both deliverables:

1. **Rewritten text** — brief diagnosis + clean version, ready to replace the original. No inline annotations.
2. **Change report** — scope and audience, a change log table (Original | Rewritten | Principle | Why it helps the reader), metrics before vs. after, and decisions the user must make (e.g. keep the legal term "indemnify" or replace it with "compensate"?).

Always deliver both, as separate documents. Deliver only one if the user explicitly asks for just the rewrite or just the report.

### Step 4: Check before handing over

Run `references/quick-checklist.md` (20 points). For measurable targets and formulas, see `references/readability-tools.md`.

### Word export (optional)

If the user wants the result as a .docx, save the document as markdown and run:

```bash
pip install python-docx
python scripts/docx-export.py input.md output.docx
```

The script handles headings, bold text, bullet lists, and tables.

---

## Russian-language texts

The principles apply to Russian, but the readability formulas (Flesch, Fog, SMOG) are calibrated for English syllables — treat their scores as rough indicators only. For Russian, measure instead:
- average sentence length in words;
- share of passive constructions ("было принято решение");
- verbal nouns that hide actions ("осуществление", "проведение", "обеспечение");
- chains of genitives ("повышение уровня качества обслуживания клиентов").

If the user wants Ilyakhov's informational style (инфостиль) rather than general plain language, suggest `/ilyakhov`.

---

## Special cases

### Legal language
- Use "plain legal English" — clarity without losing precision
- Define necessary technical terms on first use
- Use a definitions section for unavoidable jargon
- Keep sentence structure parallel in lists and conditions
- See chapter 28 in `references/thirty-guidelines.md`

### Low-literacy readers
- Use reading-age 9–11 text
- Short words (1–2 syllables preferred)
- Concrete examples, not abstractions
- Visual aids, white space, large fonts
- See chapter 29 in `references/thirty-guidelines.md`

### Email
- Subject line = main message
- Opening sentence = what you want
- One request per email when possible
- Bullet points for multiple items
- See chapter 21 in `references/thirty-guidelines.md`

### Web content
- Front-load: most important information first
- Short paragraphs, frequent headings
- Links, not cross-references
- Write for scanners (bold keywords, lists)
- See chapter 27 in `references/thirty-guidelines.md`

---

## Key metrics

- **Sentence length:** 15–20 words average
- **Reading age:** 13 for a general UK/US adult audience
- **Active voice:** >70%
- **Noun strings:** max 2 nouns in a row (3+ is "knotty")

## Quick fog tests

**Zombie test (passive voice):** can you insert "by zombies" after the verb? If yes, it's passive.
> "The report was completed [by zombies]" → "The team completed the report"

**Noun string counter:** 3+ nouns in a row = fog alert.
> "service delivery optimization strategy" → "strategy for optimizing service delivery"

**Talk test:** would you say this out loud to a colleague? If it sounds ridiculous spoken, it's written fog.

---

## Common pitfalls

1. **Premature completion.** The rewrite is not done until the change report explains every significant edit against a specific principle.
2. **Over-simplification.** Plain English is not baby talk. Keep technical terms for specialist readers; define them for mixed audiences instead of deleting them.
3. **Passive voice tunnel vision.** Not every passive is bad. "The report was completed on time" is fine when the actor is unknown or unimportant. Fix passives that hide responsibility.
4. **Noun string blindness.** Break 3+ noun chains into prepositional phrases or verb clauses.
5. **Negative framing by default.** "You cannot submit after Friday" → "Submit by Friday."
6. **Forgetting the reader.** What is plain to scientists may be obscure to the public. Match complexity to the audience.
7. **OCR blind trust.** The reference text was extracted from a PDF. If a term looks absurd ("Czech" instead of "check"), it's an extraction error — see `references/source-notes.md`.

---

## Files

| File | Purpose | When to open |
|------|---------|--------------|
| `references/thirty-guidelines.md` | All 30 chapters of Cutts' book (~530 KB) | Only the chapter you need |
| `references/examples-bank.md` | Before/after examples by category | Step 2 |
| `references/quick-checklist.md` | 20-point pre-publication checklist | Step 4 |
| `references/readability-tools.md` | Readability formulas and target scores | Metrics in the change report |
| `references/source-notes.md` | Book structure, chapter map, OCR error log | To locate a chapter |
| `templates/rewrite-template.md` | Two-document output template | Step 3 |
| `scripts/docx-export.py` | Markdown → Word export | User asks for .docx |

## Credits

- *Oxford Guide to Plain English*, 5th edition, Martin Cutts (Oxford University Press, 2020)
- PLAIN (Plain Language Association International) definition, 2014
- UK gov.uk style guide principles
