# Jackson

**A persona-driven messaging system for a fintech platform — and the filter that keeps every page in the customer's language.**

Kian Thompson · Landjourney (agricultural lending) · March 2026

---

## The sentence where we lost him

> "The right sidebar contains three discussion panels."

Accurate. Grammatical. Written by someone who understood the product completely.

It's also the sentence where a loan officer with fifteen years of experience stops reading. He has forty files to get through today. He doesn't know what a *panel* is, he doesn't want to learn, and he has two options: call support, or decide the platform is too complicated and go back to email.

Now put that sentence on twenty pages. That's not a writing problem. That's a leak in the funnel.

---

## The real problem wasn't the writing

Landjourney's user guide was written by people close to the product — engineers, PMs, writers with software backgrounds. Every page was correct.

But the product was describing itself in *its own* vocabulary, and the customer had a different one. Sidebar, toggle, wizard, modal, dynamic form, reusable configurations. None of those words exist in an ag-lender's day. Jackson knows guarantors, disclosures, credit analysis, closing. He does not know software.

Every mismatched word is a small tax paid at the exact moment a new user is deciding whether this thing is worth learning. Onboarding is where self-serve adoption is won or lost, and we were spending it on translation.

The fix isn't "write more clearly." Clarity is subjective and doesn't survive a handoff. The fix is to make the customer's vocabulary the standard, and make the standard enforceable by someone who isn't me.

---

## So I stopped editing and built a filter

Three artifacts. Each one is a thing someone else can pick up.

### 1. Name the customer → [`persona/jackson.md`](persona/jackson.md)

Jackson is a composite ag-lending loan officer: fifteen years in the field, deep domain knowledge, low tech comfort, skims before he reads, gives up after two unfamiliar words in a row.

He's deliberately fictional so the team can argue about *him* instead of about taste. Once Jackson existed, every editorial debate stopped being "is this clear enough?" and became "would Jackson read this?" — a question with an answer.

### 2. Turn the persona into vocabulary → [`framework/word-swaps.md`](framework/word-swaps.md)

A substitution table, every row pulled from a real edit. `sidebar → left menu`. `toggle → turn on`. `wizard → setup process`. `reusable configurations → saved setups`.

It also documents what *not* to swap — product UI names, industry terms Jackson already uses, compliance language. The goal is his vocabulary, not a smaller one.

### 3. Gate the work → [`framework/the-test.md`](framework/the-test.md)

Four questions any draft has to pass before it ships. Would he know every word? Can he find the next action in three seconds of skimming? Does the copy match what the screen actually says? Does he need the *why* to use the feature?

Plus the [step-by-step for running it across a doc set](framework/how-to-apply.md) — by pattern, not by page, because page-by-page editing is where consistency goes to die.

---

## Proof

Real numbers from the Landjourney repo. Full breakdown in [`case-study/metrics.md`](case-study/metrics.md), before/afters in [`case-study/examples/`](case-study/examples).

| | |
|---|---|
| Pages rewritten | 20+ |
| Sections of the guide covered | 4 (Getting Started, Backoffice, Borrower Portal, Reference) |
| Recurring jargon patterns eliminated | 20+ |
| Vocabulary decisions made | Once. Then reused everywhere. |
| New pages shipped in-voice from the first draft | E-Signatures, Pre-Fill Function |

The number I care about is the last row.

---

## The part that makes it a system

Anyone can clean up twenty pages. The question is what happens to page twenty-one.

The E-Signatures and Pre-Fill Function pages were written *after* the filter existed, and came out Jackson-ready with no retrofit. That's the whole test. If a filter only ever touches legacy content, it was a cleanup project. If it changes how the next thing gets written — by a contractor, a new hire, or an AI-assisted draft — it's a system, and it keeps paying after I'm off the project.

Arguments about "sidebar vs. menu" are now settled in a file instead of relitigated in a review.

---

## Where this goes next

The docs were the cheapest surface to prove it on. The same machine extends:

**To the app itself.** Docs are downstream of the UI. "Dynamic Forms" is a product-named feature that means nothing to Jackson — I renamed it in the guide, but the real fix is renaming it on screen. Docs work surfaces product-copy debt.

**To the marketing site and sales collateral.** Same method, different persona — because *Jackson doesn't sign the contract.* The loan officer uses the platform; a chief credit officer buys it, and they care about portfolio risk, compliance exposure, and what happens when an examiner walks in. Two personas, two vocabularies, one system for keeping each surface honest to its reader.

**To CI.** The swap table is a lint rule waiting to happen. Any PR that adds "sidebar" to a customer-facing file gets flagged. Message governance that doesn't need a human gatekeeper.

**To real Jacksons.** He's a composite built from real conversations, not a substitute for them. The next validation is putting the rewritten pages in front of actual loan officers and measuring where they still stall.

---

## What this demonstrates

- **Voice of customer, turned into an object.** "Know your user" is a slogan. A word-swap table is something a stranger can pick up and use on a Tuesday.
- **Positioning enforced at the word level.** Consistency across twenty pages isn't a style preference — it's the difference between a product that feels built for you and one that feels built for someone else.
- **Adoption treated as a messaging problem.** The friction wasn't in the feature set. It was in the first hour of contact with it.
- **Enablement over authorship.** The leverage isn't that I write well. It's that the system works without me in the room.
- **Honest scope.** I documented what I deliberately *didn't* change — and why — in [`case-study/landjourney.md`](case-study/landjourney.md).

You're not Jackson, so this page wasn't written through his filter. It was written through the same four questions, pointed at a different reader. That's the transferable part.

---

## Repo map

```
jackson-persona/
├── README.md                       ← you are here
├── persona/
│   └── jackson.md                  ← who we write for
├── framework/
│   ├── word-swaps.md               ← the vocabulary standard
│   ├── the-test.md                 ← the 4-question gate
│   └── how-to-apply.md             ← running it across a doc set
└── case-study/
    ├── landjourney.md              ← client context, decisions, tradeoffs
    ├── metrics.md                  ← the receipts
    └── examples/
        ├── 01-discussions.md       ← before/after: the reference case
        ├── 02-request-overview.md  ← before/after: the hardest page
        └── 03-getting-started.md   ← before/after: the lightest touch
```

---

**Kian Thompson** · kian@landjourney.ai
