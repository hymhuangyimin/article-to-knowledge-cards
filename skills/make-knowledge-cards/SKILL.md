---
name: make-knowledge-cards
description: Convert pasted prose or local Markdown/TXT content into 5–8 concise knowledge cards with titles, core facts, explanations, and examples or self-check questions. Use for study-note review cards; do not use for web research, PDFs, Anki export, or image cards.
---

# Make Knowledge Cards

Turn the user's pasted prose, Markdown, or supplied local `.md`/`.txt` file into a compact set of reusable knowledge cards.

## Source handling

- Use only the content the user provides or the specified local Markdown/TXT file. If a file is named but unavailable, ask the user to provide it or paste the text.
- Do not browse the web, fetch pages, process PDFs, create Anki packages, or generate image cards.
- Preserve the source's intent and terminology. Do not invent facts, examples, dates, or definitions that are not supported by the source.

## Card selection

- Create **5–8 cards**. Choose the number based on the number of distinct, important concepts: fewer cards for a short or tightly focused source, more for a longer source with several independent concepts.
- Prefer one clearly useful concept per card. Merge overlapping material and remove duplication instead of rephrasing the same point across several cards.
- Cover the most important ideas first. If the source cannot support five distinct cards, say so and produce the smaller evidence-based set rather than padding with invented content.

## Required output

Return the cards in Markdown. Each card must include:

1. **Title** — a short concept name.
2. **Core knowledge** — the essential point, stated accurately and concisely.
3. **Brief explanation** — why it matters, how it works, or how it relates to the source.
4. **Example or self-check question** — use a source-grounded example when one exists; otherwise ask a question that helps the reader recall or apply the card.

Use a consistent format such as:

```markdown
## Card 1 — [Title]

**Core knowledge:** ...

**Brief explanation:** ...

**Example / self-check:** ...
```

Keep cards easy to scan and suitable for review. Before responding, check that each card is distinct, source-supported, and contains all four required parts.
