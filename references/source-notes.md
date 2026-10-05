# Extracted Content: Large-Book Workflow

## Source
- **Book:** *Oxford Guide to Plain English*, 5th edition
- **Author:** Martin Cutts
- **Publisher:** Oxford University Press, 2020
- **ISBN:** 978–0–19–884461–7
- **Extraction date:** 2026-06-21
- **Tool:** `markitdown` (CLI) on the PDF → `Oxford Guide to Plain English.md`

## Known OCR / Extraction Errors

| Page in source | Extracted text | Correct text | Notes |
|----------------|---------------|--------------|-------|
| 129 | "Keeping errors in Czech" | "Keeping errors in check" | OCR misread "check" as "Czech". Chapter is about proofreading. |

> **Lesson:** Always verify chapter titles against the table of contents. If a title looks absurd ("Czech" in a book about English writing), it's likely an OCR error.

## Extraction Workflow (for future source additions)

When converting a PDF book to a skill knowledge base:

1. **Convert:** `markitdown book.pdf -o output.md`
2. **Map structure:** Use `search_files` to find chapter headings (`pattern: ^\d+\s+\w+`)
3. **Verify titles:** Cross-check against table of contents. Look for OCR nonsense.
4. **Extract by section:** Read chunks with `read_file(offset, limit)` rather than loading the whole file.
5. **Chunk size:** Keep reference files under 100KB to avoid context overflow.
6. **Parallel extraction:** Use `delegate_task` with 3 concurrent agents for large books:
   - Agent A: Extract odd-numbered chapters
   - Agent B: Extract even-numbered chapters
   - Agent C: Extract examples and before/after pairs

## Book Structure

The book has 30 chapters grouped into themes:

| Theme | Chapters |
|-------|----------|
| Foundations | 1–3 (Planning, Organization, Sentences/Paragraphs) |
| Word choice | 4–7 (Plain words, Conciseness, Active voice, Vigorous verbs) |
| Structure & format | 8–10 (Lists, Positives, Punctuation) |
| Accuracy | 11–13 (Grammar, Proofreading, Troublesome words) |
| Style refinement | 14–20 (Foreign words, Noun strings, Myths, Clichés, Level, Starts/Ends) |
| Medium-specific | 21–23, 26–27 (Email, Inclusive language, Alternatives, Instructions, Web) |
| Management | 24–25, 28 (Customers, Colleagues, Legal) |
| Accessibility | 29 (Low-literacy) |
| Design | 30 (Page layout) |

## Recommended Reading Order for Skill Use

1. Start with `SKILL.md` — 12 main principles
2. Deep dive into `references/thirty-guidelines.md` for specific chapter details
3. Use `references/examples-bank.md` for before/after patterns
4. Check `references/quick-checklist.md` before publishing
