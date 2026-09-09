# Example 1: The Discussions Page

The first page I applied the filter to. This is the reference example — it's the cleanest demonstration of the swap-table in action.

**Actual commit:** [`79660db`](https://github.com/) — "Improve discussions docs clarity for lender audience"
**Files changed:** 2 (source + app copy)
**Lines changed:** 52
**Time to edit:** ~10 minutes

---

## Full before/after diffs

### Intro paragraph

**Before:**
> Landjourney provides a built-in discussion system that lets you communicate about loan requests without leaving the platform. Discussions are **threaded**, task-specific, and support @ mentions to notify specific people.

**After:**
> Landjourney provides a built-in discussion system that lets you communicate about loan requests without leaving the platform. Discussions are **organized by task** and support @ mentions to notify specific people.

Swap: `threaded` → `organized by task`

Jackson doesn't know what "threaded" means outside of a needle. "Organized by task" is what he was already imagining in his head.

---

### Section layout description

**Before:**
> Every request has three discussion **panels**, accessible from the **right sidebar** of the Request Overview and from individual **task detail views**.

**After:**
> Every request has three discussion **sections**, accessible from the **right side** of the Request Overview and from individual **task views**.

Three swaps in one sentence:
- `panels` → `sections`
- `right sidebar` → `right side`
- `task detail views` → `task views` (dropped a filler word)

---

### Message posting instructions

**Before:**
> 1. Open the discussion **panel** you want to use...
> 2. Click "Add a Message" or "Add to Thread" depending on the **panel**.
> 3. Type your message in the **rich text editor**.

**After:**
> 1. Open the discussion **section** you want to use...
> 2. Click "Add a Message" or "Add to Thread" depending on the **section**.
> 3. Type your message in the **message box**.

Two swaps:
- `panel` → `section`
- `rich text editor` → `message box`

"Rich text editor" is a term Jackson has heard maybe once — in a spam email. "Message box" is what he sees.

---

### Header renames

Three headers were rewritten in this page:

| Before | After |
|---|---|
| `@ Mentions` | `Tagging People` |
| `Viewing Discussion History` | `Viewing Past Messages` |
| `Messenger vs. Discussions` | `When to Use Discussions vs. Messenger` |

The third one is the most interesting. The original header just names a comparison. The new header tells Jackson what the section is *for* — helping him decide which tool to use.

---

### Table cell rename

**Before:**
> | **Threading** | Organized by task | Organized by conversation |

**After:**
> | **Organization** | Organized by task | Organized by conversation |

The row label was the leftover jargon inside an otherwise clear table. Fixed.

---

## What the whole page looked like as a diff

52 lines of change across 2 files. No sentences added, no paragraphs restructured. Only:

- 8 unique word swaps
- 3 section header rewrites
- 1 table header rewrite

That's it. The page is now readable by Jackson. The information content is unchanged.

---

## Why this is the reference example

Because it's the shape every filter application should have:

- The **content** was correct before and after.
- The **structure** was correct before and after.
- Only the **vocabulary** changed.

If a Jackson-filter application looks like a rewrite, you're doing something bigger than filtering. That's fine — but call it what it is.
