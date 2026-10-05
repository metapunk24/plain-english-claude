# Readability Tools & Formulas

A quick reference for measuring and improving the readability of plain-English copy.

## Core Formulas

### 1. Flesch Reading Ease (FRE)
- **Formula:** 206.835 − (1.015 × average sentence length) − (84.6 × average syllables per word)
- **Score guide**
  | Score | Reading Level |
  |-------|---------------|
  | 90–100 | Very easy (5th grade) |
  | 60–70 | Standard / Average (8th–9th grade) |
  | 0–30 | Very difficult (college graduate) |
- **Target for general public:** 60–70 (comfortable for most adults).

### 2. Flesch–Kincaid Grade Level (FKGL)
- **Formula:** (0.39 × average sentence length) + (11.8 × average syllables per word) − 15.59
- **Output:** U.S. school grade level.
- **Target for mass audience:** 7th–8th grade (ages 12–13).

### 3. Gunning Fog Index
- **Formula:** 0.4 × [(words ÷ sentences) + 100 × (complex words ÷ total words)]  
  *(Complex word = 3+ syllables, excluding proper nouns & compound words)*
- **Output:** Years of formal education needed.
- **Target for mainstream copy:** 8–10 (high-school level).

### 4. SMOG (Simple Measure of Gobbledygook)
- **Formula:** √(number of polysyllabic words in 30 sentences) × 30 ÷ √(number of sentences sampled) + 3  
  *(Short cut: count polysyllabic words in 10 consecutive sentences near start, middle, and end; take the square root and add 3.)*
- **Output:** Years of education required.
- **Target:** ≤ 8 for broad public materials.

### 5. Coleman–Liau Index
- **Formula:** 0.0588 × (average letters per 100 words) − 0.296 × (average sentences per 100 words) − 15.8
- **Output:** U.S. grade level.
- **Advantage:** Relies on character count rather than syllable count (easier to automate).

## Online Services

| Tool | Best For | Key Feature |
|------|----------|-------------|
| **Hemingway Editor** (hemingwayapp.com) | Live editing | Highlights hard-to-read sentences, adverbs, passive voice; gives grade-level score |
| **Readable.com** | Professional reports | Multiple formulas, keyword density, tone analysis, PDF exports |
| **Automatic Readability Checker** (readabilityformulas.com) | Batch scoring | Runs several formulas at once |
| **Microsoft Word Editor** | In-app convenience | Displays FRE and FKGL in Proofing settings |
| **Grammarly** | Grammar + style | Offers readability alerts alongside grammar checks |

## Interpreting Results

1. **Pick one primary formula** (usually FKGL or SMOG) and track it consistently across drafts.
2. **Match grade level to audience:**
   - General public / web copy → grade 7–8 (reading age ~13)
   - Professionals / specialists → grade 10–12
   - Legal / medical patients → grade 5–6
3. **A low score alone does not guarantee clarity.** Always pair metrics with a human review (see `quick-checklist.md`).
4. **Recheck after edits:** Changing one long sentence can shift the grade level by a full point.

## Quick Targets Summary

| Audience | FKGL | Reading Age | FRE Score |
|----------|------|-------------|-----------|
| Mass market | 7–8 | ~13 | 60–70 |
| Wide public (simplified) | 5–6 | 10–11 | 70–80 |
| Professional / trade | 10–12 | 15–17 | 40–50 |

---

*Remember: formulas measure structural complexity, not meaning. Use them as guardrails, not as the final judge of good writing.*
