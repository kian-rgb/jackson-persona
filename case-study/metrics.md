# Metrics

Pulled from the actual git history of the Landjourney user guide repo.

---

## Commits

| Commit | Message | Files | Changes |
|---|---|---|---|
| `79660db` | Improve discussions docs clarity for lender audience | 2 | 52 lines |
| `e1c894a` | Personality Wording (rest of sections) | 17 | 130 lines |

Plus additional edits interspersed across other feature commits (creating-a-request, customers, backoffice header standardization, e-signatures, pre-fill function).

---

## Files touched

### Backoffice (12 pages, ~10 edited)
- `home-dashboard.md`
- `requests.md`
- `request-overview.md`
- `creating-a-request.md`
- `reviewing-tasks.md`
- `customers.md`
- `templates.md`
- `discussions.md`
- `settings-users.md`
- `settings-export.md`
- `messenger.md`

### Borrower Portal (5 pages, all edited)
- `home.md`
- `my-requests.md`
- `settings-communications.md`
- `settings-profile.md`
- `settings-sharing.md`

### Getting Started (3 pages, all edited)
- `creating-your-account.md`
- `logging-in.md`
- `platform-overview.md`

### Reference (2 pages, 1 edited)
- `faq.md`
- `security.md` — intentionally left alone (compliance language)

**Total: 22 pages in scope, ~19 edited through the filter.**

---

## The vocabulary shift

Top recurring terms swapped, with approximate frequency across the repo:

| Before | After | Occurrences |
|---|---|---|
| sidebar | left menu / right side | ~14 |
| panel(s) | section(s) | ~11 |
| toggle | switch / turn on-off | ~8 |
| wizard | setup process | ~6 |
| dynamic form(s) | online form(s) | ~6 |
| threaded / threading | organized by task | ~4 |
| widget(s) | section(s) | ~3 |
| modal | window / pop-up window | ~3 |
| authenticate | sign in | ~2 |
| breadcrumb | path | ~2 |
| rich text editor | message box | ~2 |
| overlay | window on screen | ~1 |

Header renames: **3** section titles rewritten for skim-ability.
Backoffice title prefix cleanup (`Backoffice — X` → `X`): **3 files**.

---

## Doubling as sync work

Every source-file edit was mirrored to `app/public/docs/backoffice/` (and equivalents). So the raw file-edit count is roughly **2×** the numbers above — every change was applied twice for consistency.

---

## What the numbers don't show

The interesting outcome isn't the count of replacements. It's the **consistency**:

- Every page now uses the same word for the same thing.
- New pages written after the filter existed (E-Signatures, Pre-Fill Function) were consistent from the first draft.
- Anyone editing the repo now has a documented reference for the vocabulary choice — arguments about "sidebar vs. menu" are settled.

That's the real deliverable. The counts are just evidence.
