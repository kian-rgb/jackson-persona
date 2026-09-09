# How to Apply the Filter

The full step-by-step for running the Jackson filter across a new documentation set.

---

## Prerequisites

- Read [`persona/jackson.md`](../persona/jackson.md) once. Five minutes.
- Have [`word-swaps.md`](word-swaps.md) open in a second window.
- Access to the docs you're editing.

That's it. No training, no onboarding.

---

## The process

### Step 1 — Take inventory

Before editing anything, list every documentation file in scope. For the Landjourney project this was:

- 12 backoffice pages
- 5 borrower-portal pages
- 3 getting-started pages
- 2 reference pages

**Why this step matters:** consistency comes from applying the same swap everywhere. If you edit "sidebar" → "left menu" on page 3 but miss it on page 7, Jackson notices.

---

### Step 2 — Find the recurring offenders

Grep the docs for the words in the swap table. The high-frequency ones in this case were:

```
sidebar     — appeared 14x across 9 files
toggle      — appeared 8x across 5 files
panel(s)    — appeared 11x across 6 files
wizard      — appeared 6x across 2 files
```

**Why this step matters:** knowing what appears often tells you where the pain is. It also lets you fix systemic issues in one pass instead of file-by-file.

---

### Step 3 — Edit in passes, not page-by-page

Instead of doing "clean up page 1, then page 2, then page 3," do:

- **Pass 1** — Fix all title-level issues (e.g., "Backoffice — X" prefix) across every file.
- **Pass 2** — Fix all navigation/layout jargon (sidebar, panel, widget) across every file.
- **Pass 3** — Fix all action jargon (toggle, authenticate, configure).
- **Pass 4** — Fix all object/concept jargon (wizard, dynamic form).
- **Pass 5** — Section header improvements.
- **Pass 6** — Reread each page top-to-bottom against the 4-question test.

**Why this step matters:** by-file editing lets consistency drift. By-pattern editing forces uniform vocabulary.

---

### Step 4 — Keep the app copy in sync

If the docs live in two places (source + published), edit both together. On Landjourney, the source lived in `02_backoffice/` and the app-served copy lived in `app/public/docs/backoffice/`. Every edit was applied to both.

**Why this step matters:** the app is what Jackson actually opens. Diverging copies mean the version he reads may not be the one you edited.

---

### Step 5 — Commit in logical batches

Not one giant commit. Not 200 tiny ones. Group by pass:

- `Improve discussions docs clarity for lender audience`
- `Personality wording — rest of the sections`

**Why this step matters:** a reviewer can understand what changed at a glance. Rollback is safe. Others can see the pattern of edits, not just the endpoint.

---

### Step 6 — Apply the filter to *new* content, too

Once the filter exists, all new pages should be written through it from the first draft. On Landjourney, the E-Signatures and Pre-Fill Function pages were written Jackson-ready — no retrofit needed.

**Why this step matters:** if the filter is only used on legacy content, it's a cleanup project. If it's used on new content, it's a system.

---

## Time estimate

For a repo of this size (~22 pages, ~50KB of markdown):

- Initial persona + filter build: 1 session
- Full application pass: 3–4 sessions of ~1 hour each
- Ongoing use on new content: adds negligible time to first drafts

---

## When to skip the filter

You do not need the filter for:

- Internal engineering docs (audience isn't Jackson)
- Legal / compliance pages where regulatory language is required
- Sales/marketing copy (different audience, different filter)
- API reference docs (different audience — developers)

If you can't name a "Jackson" for the audience, you probably need a different filter.
