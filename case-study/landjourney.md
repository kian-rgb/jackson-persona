# Case Study: Landjourney User Guide

**Client:** Landjourney — an agricultural lending platform for lenders and borrowers.
**Scope:** Full user guide across 4 sections, 22+ pages.
**Timeline:** March 2026, iterative sessions.
**My role:** Owned the customer-facing language end to end — persona research, the messaging standard, and rolling it across every page.

---

## The client, briefly

Landjourney is a two-sided fintech: a **Backoffice** for loan officers and a **Borrower Portal** for farmers/borrowers. It sits inside institutions ranging from small community banks to Farm Credit branches.

The user guide covers every feature of both sides — home dashboards, request creation, task review, e-signatures, templates, communication, settings, exports.

---

## The problem I walked into

The docs existed. They were written by people close to the product — engineers, product managers, technical writers with software backgrounds. They were **accurate**.

They were also full of language the actual reader doesn't use:

- "The right sidebar contains three discussion panels."
- "Toggle the Show Closed Requests switch."
- "Templates are reusable configurations."
- "This layered approach means you build each piece once."
- "The messenger panel opens as an overlay."

A loan officer opening these pages spends mental effort on the *language* before spending it on the *product*. That's a leaking bucket for onboarding, adoption, and support tickets.

---

## What I did (in order)

### 1. Named the reader

Rather than say "our users," I built Jackson — a specific composite ag-lending loan officer with defined tech comfort, career history, and reading habits. See [`persona/jackson.md`](../persona/jackson.md).

Once Jackson existed, every editorial argument became "would Jackson read this?" instead of "is this technically clear?"

### 2. Extracted the filter

Every jargon term I found became a row in a swap table. See [`framework/word-swaps.md`](../framework/word-swaps.md). This turned the persona from an idea into a tool.

### 3. Applied the filter by pass, not by page

Instead of cleaning up page 1, then page 2, I fixed patterns across all pages at once:

- All "sidebar" instances → "left menu" (14 replacements, 9 files)
- All "toggle" instances → "switch" / "turn on" (8 replacements, 5 files)
- All "Backoffice — X" title prefixes → "X" (3 files)
- ...and so on

### 4. Improved headers, not just words

Some headers weren't jargon but were still bad for skimming:

- `@ Mentions` → `Tagging People`
- `Viewing Discussion History` → `Viewing Past Messages`
- `Messenger vs. Discussions` → `When to Use Discussions vs. Messenger`

The last one is the interesting change: a comparison header became a *decision* header. Jackson doesn't want to compare — he wants to know which one to click.

### 5. Kept new content in the filter

The E-Signatures and Pre-Fill Function pages were written from scratch during this project. Both were drafted Jackson-ready — no retrofit needed. That's the actual test of whether a filter works: does it change how the next thing gets written?

---

## What I explicitly did NOT change

To avoid over-editing:

- **Product terminology stayed exact.** If the UI button said "Create New," docs said "Create New."
- **Industry vocabulary stayed.** Guarantor, co-borrower, disclosure, pre-qualification — Jackson uses these words already.
- **Compliance language stayed.** SOC 2, TLS, audit trail, Section 1071 — regulatory language belongs.
- **Structural changes were minimal.** The docs were structured fine; they were worded badly. Different problem, different fix.

---

## What surprised me

- **The same words showed up everywhere.** "Sidebar" and "toggle" appeared across all four sections of the guide. This meant one filter fixed the whole product, not just one team's output.
- **Headers were often worse than body text.** The body was written carefully; headers were dashed off. Editing headers had disproportionate impact on skim-ability.
- **"Dynamic form" was a hidden trap.** It's a product-named feature, but it means nothing to Jackson. I renamed it to "online form" in docs — knowing that at some point the product should probably rename it in-app too. That's a note for product.

---

## What I'd do next

If this project continued:

1. **Coordinate with product on UI copy.** The docs are downstream of the app. Some app strings (e.g. "Dynamic Forms") force docs into awkward decisions.
2. **Build a lint rule.** The word-swap table could run as a CI check. Any PR that adds "sidebar" to a doc gets flagged.
3. **Test with a real Jackson.** The persona is a composite; the next validation step is putting the edited docs in front of actual ag-lending loan officers and measuring comprehension.
4. **Extend the persona set on the user side.** Jackson covers lenders. A parallel persona for borrowers (probably a farmer named something like "Ellie") would cover the other half of the platform.
5. **Build the buyer persona, not just the user persona.** Jackson doesn't sign the contract. A chief credit officer does, and they're reading for portfolio risk, compliance exposure, and examiner questions — a different vocabulary entirely. Same method, different reader, and it's the one that shapes sales and marketing copy rather than docs.

---

## What this project shows

The surface task was editing documentation. The actual work was go-to-market:

- **I found the systemic issue hiding inside the per-page task.** Twenty pages of "make this clearer" was really one problem — the product described itself in its own vocabulary instead of the customer's — and one filter fixed all twenty.
- **I turned voice of customer into an object.** Not a research deck. A swap table and a four-question gate that a contractor can use on their first day.
- **I treated onboarding friction as a messaging problem.** Every unfamiliar word in the first hour is a reason to call support instead of self-serving, and that cost lands in adoption, not in the doc.
- **I enforced one vocabulary across every surface.** The same word for the same thing on all twenty pages is what makes a product feel built for the person using it.
- **I measured honestly.** Real counts from real commits (see [`metrics.md`](metrics.md)), and I've named what I deliberately did *not* do rather than inflating the scope.
- **I built for handoff.** The filter runs without me in the room. That's the difference between writing well and building a system.
