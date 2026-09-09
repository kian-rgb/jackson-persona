# The Jackson Test

Four questions. Run any user-facing text through them before shipping.

---

### 1. Would Jackson know every word here without Googling?

Scan the text. Circle any word that a career loan officer with low tech comfort wouldn't use himself.

- Yes to all words → pass.
- One unfamiliar word → check the [word-swap table](word-swaps.md). Swap or explain inline.
- Two or more → rewrite the sentence.

---

### 2. Can Jackson find the next action in under 3 seconds of skimming?

Look at the page as a whole, not the sentences.

- Are the actions **bolded**?
- Are steps **numbered**?
- Are the section headers actual verbs or nouns Jackson would search for?

If a Jackson scanning the page has to read a paragraph to find "click Save," you have failed the skim test.

---

### 3. Does the language match what the app actually shows on screen?

Jackson has the app open in another tab. He is checking whether the page in the docs matches.

- Button in the app says "Create New"? Docs must say "Create New" — not "create a new record" or "create a record."
- App has a section called "Field Management"? Don't call it "the field configuration area."
- If the docs and the app disagree, Jackson trusts the app.

---

### 4. Would Jackson need to understand *why* this feature exists to use it?

Cut the "why" unless it changes how he uses the feature.

- ❌ "This layered approach means you build each piece once and reuse it across multiple request templates." (architectural rationale — cut)
- ✅ "You build each piece once and reuse it across multiple request templates." (still true, no philosophy)

Explanations of platform architecture usually belong in a sales deck, not a user guide.

---

## When to override the test

The test is a filter, not a straitjacket.

- **Legal / compliance sections** may need to keep exact regulatory language (Section 1071, SOC 2, TLS). Leave those alone.
- **First occurrence of an unavoidable term** may need a one-line inline definition. Then use the term freely.
- **Named UI features** (E-Signatures, Pre-Fill Function, Signature Templates) stay named — even if a plainer word exists — because the app screen names them that way.

---

## What "passing" the test looks like in practice

Take the "before" and "after" of a real page (see [`case-study/examples/01-discussions.md`](../case-study/examples/01-discussions.md)):

- Words swapped: 8 unique terms
- Headings renamed: 3
- Structural rewrites: 0 (structure was already fine)
- Total edit time: ~10 minutes with the swap table open

That's the shape of a good filter application. If it takes an hour, you're doing more than filtering — you're redesigning the page, which is a different job.
