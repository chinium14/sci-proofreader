# Category L — Logic disconnection

A finding belongs here when each sentence is readable on its own but the connection
between pieces of the text fails: a conclusion does not follow from what precedes it, a
step is missing, two parts of the draft disagree, or the evidence presented is weaker
than the claim built on it.

This is a check of the draft's internal reasoning, not a peer review. Do not judge
whether the study design is good or the result is true. Judge whether the text, taken
at its word, hangs together.

## Subtypes

| Subtype | Definition | Typical signal |
|---------|------------|----------------|
| `non-sequitur` | A stated inference ("therefore", "thus", "this shows") whose conclusion does not follow from the stated premise | Connective present, but the premise is about something else or is too weak |
| `missing-step` | The inference could hold, but a premise or intermediate step the reader needs is absent | Reader has to guess why B follows from A; an assumption is used but never stated |
| `overclaim` | Claim strength exceeds what the reported evidence or design supports | Causal verbs from correlational data; "proves"; generalising beyond the sample or conditions tested; mechanism claimed without mechanistic data; non-significance read as "no effect" |
| `contradiction` | Two statements in the draft cannot both be true | Abstract vs Results; text vs table or figure; one section vs another; a limitation that undercuts an earlier unqualified claim |
| `numeric-inconsistency` | Numbers that disagree or do not add up | Different N in Methods and Results; subgroups not summing to the total; percentage not matching the counts; effect direction in text opposite to the table; p-value and "significant" label disagreeing with the stated threshold |
| `wrong-connective` | The linking word signals a relation the content does not have | "However" with no contrast; "therefore" joining two unrelated facts; "in contrast" between results that agree; "similarly" between dissimilar things |
| `structure-gap` | The document's parts do not line up | Aim stated in the Introduction never addressed; result reported with no method; method described with no result; Conclusion introducing a claim not in Results; hypothesis changes between sections |
| `coherence-break` | A paragraph or sentence does not connect to its neighbours | Topic jumps with no transition; a paragraph whose sentences do not serve one point; a sentence that answers a question nobody asked |
| `circular` | The conclusion is assumed in the premise, or a term is defined by itself | "X is effective because it works" |
| `fallacy` | Any other named reasoning error | See the fallacy catalogue below; name the fallacy in the finding |
| `cross-reference` | A pointer leads to the wrong place or nowhere | "as shown in Figure 3" where Figure 3 shows something else; reference to a section, equation, or table that does not exist; a figure never cited in the text |

## How to check

Sentence-by-sentence reading does not find these. Use the working map built in the
first read (central claim, each section's job, key terms, key numbers, study design).

**Connective audit.** For every inferential word (therefore, thus, hence, so,
consequently, as a result, because, since, given that, this shows / indicates /
suggests / demonstrates / confirms / implies), name the premise and the conclusion,
then ask: if I accepted the premise, would I have to accept the conclusion? If the
premise is elsewhere in the draft, fine. If it is nowhere, that is `missing-step`. If
it is present but does not get you there, `non-sequitur`. Do the same for contrast
words (however, but, although, in contrast, whereas, nevertheless): is there an actual
contrast?

**Reverse outline.** Write one sentence stating the point of each paragraph. A
paragraph with no single point, or two unrelated points, is a `coherence-break`. Read
the outline top to bottom: where the sequence jumps, the draft is missing a transition
or a step.

**Claim–evidence trace.** For each claim in the Abstract and Conclusion, locate the
result that supports it. Compare the strength of the wording with the strength of the
result. Check that the verb fits the design the draft itself describes:

| Design described in the draft | Language it can support |
|-------------------------------|-------------------------|
| Randomised or controlled experiment | "caused", "increased", "the effect of" (within the conditions tested) |
| Observational, cross-sectional, correlational | "was associated with", "correlated with", "predicted" |
| In vitro or animal model | Claims about that system; "suggests" for humans or in vivo |
| Single sample, cell line, site, or dataset | Claims about that sample; hedged language beyond it |
| Simulation or model | "the model predicts"; not "we observed" |

**Number reconciliation.** List every number that appears more than once or that can be
derived from others (sample sizes, group sizes, percentages, means, p-values, fold
changes, dates, durations). Check that repeated values match everywhere and derived
values are arithmetically right. Do the arithmetic; do not eyeball it. A count and its
percentage, subgroup sizes and the total, a stated fold change and the two values it
compares are the usual failures.

**Section alignment.** Aims ↔ Methods ↔ Results ↔ Conclusions should be a one-to-one
chain. List the aims or hypotheses from the Introduction and tick off where each is
tested and answered. List the methods and tick off where each produces a result.
Anything left over on either side is a `structure-gap`.

**Pointer check.** For each reference to a figure, table, equation, or section, confirm
the target exists and contains what the sentence says it contains. If figures are not
available to you (text-only input), say so once in the report's notes instead of
guessing.

## Writing the suggestion

Logic findings often cannot be fixed by rewording alone, because the fix depends on
facts only the author has. Choose whichever of these fits:

- **Reword to match the evidence** when the claim is simply too strong:
  "X causes Y" → "X was associated with Y".
- **Name the missing step** and ask the author to supply it: "State why a higher
  expression level implies increased activity, or cite support for it."
- **Ask which is correct** when two statements conflict: "Methods gives n = 48, Table 2
  gives n = 46. Which is correct? If two samples were excluded, say where and why."
- **Propose a connective or transition** when only the link is wrong.

Never resolve a contradiction by picking one side yourself, and never supply a missing
number, citation, or mechanism.

## Do not flag

- Disagreement with the authors' scientific judgement, choice of method, or
  interpretation, when the text is internally consistent.
- Missing information that the genre does not require at that point (an abstract need
  not state every method).
- Ordinary hedged speculation that is marked as speculation ("one possible explanation
  is…").

## Deeper checklists

- [third-party/k-dense/logical_fallacies.md](third-party/k-dense/logical_fallacies.md)
  — 40 fallacies with scientific examples. Read it when a passage's reasoning feels
  wrong and you need to name why. Most relevant to drafts: 1–4 (causation), 5 and 7
  (hasty generalisation, cherry picking), 18 and 19 (false dichotomy, circular
  reasoning), 27 (multiple comparisons), 30 (equivocation), 34 (argument from
  ignorance), 39 and 40 (affirming the consequent, denying the antecedent).
- [third-party/flonat/check-categories.md](third-party/flonat/check-categories.md) §8
  (numeric text↔table cross-check), §9 (causal-language audit), §10 (equation
  completeness: every symbol defined, indices consistent).
