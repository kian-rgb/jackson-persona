# Example 2: The Request Overview Page

The hardest page to filter. Dense with layout terminology and cross-references to other features. Good example of the filter under pressure.

---

## Why this page was hard

The Request Overview is the central workspace inside a request. The docs page describes:

- A stage pipeline at the top
- A request header with actions
- A progress summary
- Customer sections with task tables
- Discussion panels on the right

Every one of those sentences had UI-layout vocabulary the source-writer used because it was concise for them. It wasn't concise for Jackson.

---

## Before/after: page title

**Before:** `# Backoffice — Request Overview`
**After:** `# Request Overview`

The `Backoffice —` prefix was on 3 pages across the guide. It duplicates what the navigation already tells the user. Removed for consistency with the other 20+ pages that don't use a section prefix.

---

## Before/after: page layout section

**Before:**
> The Request Overview is divided into three areas:
>
> - **Top bar** — Shows the request name, stage pipeline, and action buttons.
> - **Main area** — Displays the progress summary and each customer's task list.
> - **Right sidebar** — Contains the three discussion panels.

**After:**
> The Request Overview is divided into three areas:
>
> - **Top bar** — Shows the request name, stage pipeline, and action buttons.
> - **Main area** — Displays the progress summary and each customer's task list.
> - **Right side** — Contains the three discussion sections.

Two swaps: `sidebar` → `right side`, `panels` → `sections`.

The "Top bar" and "Main area" already read fine — no swap needed. Filter left them alone.

---

## Before/after: the discussions section (bottom of page)

**Before:**
> ## Right Sidebar — Discussions
>
> The right sidebar provides three discussion panels for communication within the request.
>
> - Request-Wide Discussions — Visible to anyone with access to the request. Use for general announcements or questions.
> - Customer Task Discussions — **Threaded** discussions tied to specific tasks. Visible to the borrower. Use to communicate about individual task requirements.
> - Internal Task Discussions — Private discussions visible only to your internal team. Use for internal notes and coordination.

**After:**
> ## Discussions
>
> The right side of the page provides three discussion sections for communication within the request.
>
> - Request-Wide Discussions — Visible to anyone with access to the request. Use for general announcements or questions.
> - Customer Task Discussions — Discussions **organized by task**. Visible to the borrower. Use to communicate about individual task requirements.
> - Internal Task Discussions — Private discussions visible only to your internal team. Use for internal notes and coordination.

Swaps:
- Header `Right Sidebar — Discussions` → `Discussions` (just the feature name)
- Body `sidebar` → `right side of the page`
- Body `panels` → `sections`
- Body `Threaded discussions` → `Discussions organized by task`

---

## What was NOT changed

Places where the filter deliberately held off:

- **"Stage pipeline"** — Kept. It's the product's own term for how requests move through stages, and the UI shows it visually as a pipeline.
- **"Customer sections"** — Kept. "Section" was already the plain-English word.
- **"Progress summary"** — Kept. Two normal English words describing exactly what Jackson sees.
- **"Task Table"** heading — Kept. It is a table. It is of tasks.

The filter is a tool, not a mandate. When the word is already right, you leave it alone.

---

## What this page teaches

Dense pages don't need a rewrite. They need a **targeted swap on the words carrying the jargon load**. The filter isolates those words. The rest of the page keeps working.

The Request Overview is 130+ lines. The Jackson filter touched about 8 lines. It stayed at ~5% of the surface area — but that 5% is what would have made Jackson bounce.
