---
name: sci-proofread
description: Proofread a scientific draft (manuscript, thesis chapter, abstract, grant or report text) and produce a categorised findings report covering three things - grammar errors, logic disconnections, and ambiguous or non-scientific wording - each with its location, the original text, and a suggested fix. Use this whenever the user asks to proofread, check, polish, or review the writing, language, clarity, or logical flow of a paper, manuscript, draft, thesis, or abstract, in LaTeX, Markdown, Word, PDF, or pasted text, even if they only mention one of the three categories. Report-only - it never edits the draft.
argument-hint: "[path-to-draft] [optional: section or focus]"
---

# Scientific draft proofreading

Proofread the draft named in the arguments (or pasted in the conversation) and write a
findings report. Every finding carries exactly one of three category labels:

| Label | Category | The problem is… | Reference |
|-------|----------|-----------------|-----------|
| **G** | Grammar | the sentence breaks a rule of written English | [references/grammar.md](references/grammar.md) |
| **L** | Logic disconnection | the pieces of text do not connect: a conclusion does not follow, a step is missing, two parts disagree, or a claim outruns its evidence | [references/logic.md](references/logic.md) |
| **A** | Ambiguous or non-scientific wording | the sentence can be read more than one way, is too vague to check or reproduce, or uses a register that does not belong in a paper | [references/wording.md](references/wording.md) |

Read all three reference files before starting. They define the subtypes, how to hunt
for each, what not to flag, and how to phrase suggestions. They in turn point to
longer public checklists under `references/third-party/` for when you need more depth.

## Ground rules

**Report, do not edit.** The author decides what to change. Leave the draft untouched
and put everything in the report file. An author who finds their file silently altered
can no longer trust what they submitted.

**Never invent science.** A suggestion may reword what the draft already says. It may
not supply a number, unit, citation, mechanism, or result the draft does not contain,
and it may not settle a contradiction by picking a side. When the fix depends on a fact
only the author has, give a template with a marked gap `[…]` and a direct question.
A plausible-looking invented value that slips into a submitted paper is far worse than
an unanswered question.

**Quote exactly.** Copy the original text character for character, enough of it for the
author to find by search. A misquoted finding costs the author's trust in the rest.

**Flag errors, not preferences.** If a competent editor could reasonably leave the text
as it is, leave it. A short report the author acts on beats a long one they skim.

**Stay inside proofreading.** Check whether the text is correct, connected, and precise.
Do not review whether the study design is sound or the findings are novel; that is peer
review. Category L is about the draft's internal consistency, not the truth of its claims.

## Choosing the label

Most findings are obvious. For the rest, ask these in order and stop at the first yes:

1. Is a rule of English broken (even if that also makes the meaning unclear)? → **G**.
   Mention the ambiguity in the problem line.
2. Is the sentence clear on its own, but in conflict with, unsupported by, or
   disconnected from something else in the draft? → **L**
3. Is the sentence itself unclear, vague, or in the wrong register? → **A**

Common borderline cases:

| Case | Label | Why |
|------|-------|-----|
| "This" with no clear antecedent | A · `unclear-reference` | The sentence is grammatical; the meaning is open |
| Dangling modifier ("Using PCR, the samples…") | G · `sentence-structure` | A rule is broken |
| "X causes Y" from correlational data | L · `overclaim` | Clear wording, evidence does not reach it |
| "significantly higher" with no test reported | A · `significance` | Unclear what is being claimed |
| "significant (p = 0.08)" at a stated 0.05 threshold | L · `numeric-inconsistency` | Two statements disagree |
| "However" with no contrast | L · `wrong-connective` | The link is wrong, not the grammar |
| Abbreviation never defined | A · `undefined-term` | |
| Same quantity, different value in text and table | L · `numeric-inconsistency` | |
| One concept called by three names | A · `inconsistent-term` | Unless the meaning actually shifts mid-argument; then L · `fallacy` (equivocation) |

One problem gets one finding and one label. If a sentence has two separate problems,
write two findings.

## Workflow

### 1. Get the text with stable locations

| Input | How to read it | Location format |
|-------|----------------|-----------------|
| `.tex`, `.md`, `.qmd`, `.rst`, `.txt` | Read tool (gives line numbers). For LaTeX, follow `\input`/`\include` to all source files | `file:line` plus section name |
| `.docx` | `textutil -convert txt -stdout <file>` on macOS, or `pandoc -t plain <file>` | Section name + paragraph number within it |
| `.pdf` | Read tool with `pages` | Page + section |
| Pasted text | As given | Section or paragraph number |

Skip the contents of code blocks, math, citation keys, labels, and the reference list
(reference formatting is out of scope). Do read figure and table captions, table
contents, footnotes, and the abstract. If figures or tables referred to in the text are
not available to you, say so in the report's notes rather than guessing about them.

If the arguments name a section or a focus ("only the Discussion", "logic only"),
restrict findings to that, but still read the whole draft, because logic checks need
the rest as context.

### 2. First read: build a working map

Read the whole draft once without flagging anything. Note for your own use:

- the central claim and the aims or hypotheses;
- what each section and paragraph is for (one line each: the reverse outline);
- the study design as the draft describes it (this sets how strong the claims may be);
- a term ledger: abbreviations, symbols, key terms, with where each is first used and defined;
- a number ledger: every sample size, group size, percentage, statistic, and value that
  appears more than once or can be derived from others.

Logic findings come almost entirely from this map. A proofreader who only reads
sentence by sentence finds the typos and misses the paragraph that contradicts the abstract.

### 3. Sentence pass (G and A)

Go through section by section, sentence by sentence, using the checks in
`grammar.md` and `wording.md`. For drafts longer than about 6,000 words, finish and
record findings for one section before reading the next closely; attention spread
across a long document misses things.

### 4. Connection pass (L)

Run the checks in `logic.md` against the working map: connective audit, reverse
outline, claim–evidence trace, number reconciliation (do the arithmetic), section
alignment, pointer check.

### 5. Verify before writing

For each candidate finding, re-read the passage in the source and confirm that:

- the quoted text is exact and the location is right;
- the problem is real in context (the term was not defined two paragraphs earlier, the
  "missing" step is not in the previous section, the number does not match after all);
- the suggestion does not change the scientific meaning or add content;
- it is an error, not a preference.

Drop anything that fails. Then merge repeats: when the same issue occurs three or more
times, report it once as a pattern with every location, so the report shows the author
the habit instead of burying it under near-identical entries.

### 6. Write the report

Save it beside the draft as `<draft-name>.proofread.md` (for `paper.tex`,
`paper.proofread.md`). If that file exists, do not overwrite it; use
`<draft-name>.proofread-2.md`, and so on. For pasted text with no file, give the report
in the reply.

Then tell the user where the report is and give the counts by category and the two or
three findings that matter most.

## Severity

| Level | Meaning |
|-------|---------|
| **High** | Changes or obscures the scientific meaning, or a reviewer would very likely object: contradictions, numbers that disagree, overclaims, sentences with two readings in Methods or Results, grammar errors that alter meaning |
| **Medium** | Clearly wrong or unclear and worth fixing, but the reader can recover the meaning |
| **Low** | Polish: minor typos, small consistency points |

## Report format

Use this structure. Number findings within each category (G1, G2…, L1…, A1…) so the
author can refer to them. Within a category, order by position in the draft.

```markdown
# Proofreading report: <draft file name>

**Date:** YYYY-MM-DD · **Scope:** <whole draft | section> · **Length:** ~N words

## Summary

| Category | High | Medium | Low | Total |
|----------|------|--------|-----|-------|
| G · Grammar | | | | |
| L · Logic disconnection | | | | |
| A · Ambiguous / non-scientific wording | | | | |
| **Total** | | | | |

**Most important to fix:** 2–4 lines naming the findings (by ID) that most affect how
the paper will be read, and any recurring habit worth the author's attention.

**Notes:** anything that limited the check (figures not available, section missing,
text extracted from PDF so line numbers are approximate). Omit if nothing applies.

## G · Grammar

### G1 · agreement · Medium
- **Where:** Results, §3.2 — `paper.tex:142`
- **Original:** "The effect of the two inhibitors were measured after 24 h."
- **Problem:** The subject is "effect" (singular); the verb is plural.
- **Suggestion:** "The effect of the two inhibitors was measured after 24 h."

## L · Logic disconnection

### L1 · numeric-inconsistency · High
- **Where:** Methods §2.1 (`paper.tex:58`) vs Table 2 (`paper.tex:171`)
- **Original:** "A total of 48 samples were analysed." / Table 2: "n = 46"
- **Problem:** The sample size differs between Methods and Table 2, and no exclusion is described.
- **Suggestion:** Question for author: which is correct? If two samples were excluded,
  state where and why, e.g. "Of 48 samples collected, 46 were analysed; two were
  excluded because [reason]."

## A · Ambiguous / non-scientific wording

### A1 · vague-quantity · Medium
- **Where:** Results, §3.1 — `paper.tex:120`
- **Original:** "The yield was much higher in the treated group."
- **Problem:** "Much higher" gives no magnitude, and the comparison group is not named.
- **Suggestion:** "The yield was [X-fold / X%] higher in the treated group than in
  [comparison group] ([value] vs [value])." Question for author: what are the two yields?

### A2 · subjective (pattern, 4 instances) · Low
- **Where:** `paper.tex:12`, `:88`, `:131`, `:207`
- **Original:** "remarkably", "strikingly", "dramatic", "excellent"
- **Problem:** Evaluative words assert importance without measurable content.
- **Suggestion:** Delete, or replace with the measured size of the effect.
```

Field rules:

- **Heading:** `ID · subtype · severity`. Subtypes are the ones listed in the reference
  files. For a pattern, add `(pattern, N instances)`.
- **Where:** section name plus the most exact locator the input allows. For L findings
  that involve two places, give both.
- **Original:** the exact text, in quotation marks, long enough to be found by search
  and to show the problem (usually the whole sentence).
- **Problem:** one or two plain sentences saying what is wrong and why it matters here.
  For a sentence with two readings, state both readings.
- **Suggestion:** a complete rewritten sentence when you can give one without adding
  content; otherwise a gap template and/or `Question for author:`. If you see no
  responsible suggestion, say what the author needs to decide.

If a category has no findings, keep its heading and write "No issues found." so the
author knows it was checked. Do not pad the report: no praise section, no general
writing advice, no score.
