# Jackson: A Persona-Driven Content Design System

**Author:** Kian Sadeghi
**Client / Case Study:** Landjourney (agricultural lending platform)
**Time period:** March 2026

---

## The one-liner

I built a synthetic user persona — Jackson — and turned him into a **repeatable editing filter** for a fintech user guide. The result: 20+ documentation pages rewritten for the actual end user, not the engineers who built the product.

---

## The problem

Landjourney's user guide was written by people close to the product. It read like software documentation.

The actual reader is a loan officer at an ag-lender, often with 15+ years in the field and low tech comfort. They don't know what a "wizard," "toolbar," "modal," or "breadcrumb" is. They don't want to learn — they want to process a loan.

Every jargon word is a small tax on adoption. Across 20+ pages, that tax adds up to lenders bouncing to phone support, or worse, deciding the platform is "too complicated."

**The gap:** documentation existed. It was accurate. It was also unreadable for its actual audience.

---

## The approach

Rather than editing page-by-page in the writer's own head, I built a system:

### 1. Define the user (Jackson)

A concrete, opinionated persona instead of a vague "our users." See [`persona/jackson.md`](persona/jackson.md).

### 2. Turn the persona into a filter

A word-substitution guide plus a 4-question test. Anyone on the team can now apply it without re-doing the persona research. See [`framework/word-swaps.md`](framework/word-swaps.md) and [`framework/the-test.md`](framework/the-test.md).

### 3. Apply it systematically, page by page

Instead of "make it clearer" (subjective), the edit becomes: "does this word appear on the swap list? if yes, swap it." Repeatable, auditable, delegate-able. See [`framework/how-to-apply.md`](framework/how-to-apply.md).

### 4. Measure

Track files edited, terms replaced, and the specific patterns that keep showing up. See [`case-study/metrics.md`](case-study/metrics.md).

---

## The outcome

Real numbers from the Landjourney repo:

| Metric | Value |
|---|---|
| Pages rewritten | 20+ |
| Sections of the guide touched | 4 (Getting Started, Backoffice, Borrower Portal, Reference) |
| Distinct jargon terms replaced | 20+ recurring patterns |
| Consistency across pages | "sidebar," "toggle," "wizard" now render as the same plain-language equivalent everywhere |
| New content shipped through the filter | E-signatures + Pre-Fill Function pages — written Jackson-ready from the first draft |

Beyond the numbers: **the filter now works without me.** Any writer, contractor, or AI-assisted draft can be run through the word swap and the test and come out in the right voice.

---

## Why this matters for PM work

This project is small on the surface (documentation edits). What it demonstrates:

- **Systems thinking.** I didn't do 20 one-off edits — I built one filter and applied it 20 times.
- **User empathy translated into artifacts.** "Understand the user" is a slogan; a word-swap table is an object anyone can pick up.
- **Repeatability over craft.** The system doesn't require me to keep applying it. That's leverage.
- **Measurable outcome.** I can point to specific commits, specific replacements, specific files.
- **Bias toward shipping.** The filter is documented enough to use, not so documented it becomes a project of its own.

---

## Repo map

```
jackson-persona/
├── README.md                       ← you are here
├── persona/
│   └── jackson.md                  ← the persona itself
├── framework/
│   ├── word-swaps.md               ← substitution guide
│   ├── the-test.md                 ← 4-question checklist
│   └── how-to-apply.md             ← step-by-step methodology
└── case-study/
    ├── landjourney.md              ← client context and results
    ├── metrics.md                  ← by-the-numbers
    └── examples/
        ├── 01-discussions.md       ← before/after: full page
        ├── 02-request-overview.md  ← before/after: hardest jargon
        └── 03-getting-started.md   ← before/after: lightest touch
```

---

## Contact

kian@landjourney.ai
