# Category A — Ambiguous or non-scientific wording

A finding belongs here when the sentence is grammatical and its place in the argument
is fine, but the wording itself lets the reader down: it can be read more than one way,
it is too vague to be checked or reproduced, or it uses a register that does not belong
in a scientific paper.

The test for scientific wording: could another researcher, reading only this sentence
and what precedes it, know exactly what was done, measured, or claimed, and check it?

## Subtypes

| Subtype | What to look for | Example → direction of fix |
|---------|------------------|----------------------------|
| `unclear-reference` | "this", "it", "they", "these", "which", "the former" with more than one possible antecedent, or none | "This increased the yield" → name what "this" is |
| `ambiguous-syntax` | Sentence structure that allows two readings: stacked noun modifiers, scope of "only", "not", "and/or", "respectively" with mismatched lists, unclear attachment of a phrase | "mice treated with the drug and controls" (were controls treated?); "old cell culture medium" |
| `vague-quantity` | Amount, degree, frequency, or time given in words where a value exists or is needed | "several", "many", "a few", "a large amount", "much higher", "relatively low", "often", "recently", "for a long time", "about" without a figure |
| `incomplete-comparison` | A comparative with no stated baseline, measure, or condition | "The treated group performed better" → better than what, on which measure, by how much |
| `missing-detail` | Value reported without unit, uncertainty, sample size, condition, or method needed to interpret it | "The temperature was 37"; "mean of 4.2" with no SD/CI or n; "incubated overnight" |
| `significance` | "Significant(ly)" without it being clear that it means statistical significance, or statistical claims without test, threshold, or effect size; "trend toward significance"; "marginally significant" | "significantly different" → name test and p-value, or use "substantially" if not statistical |
| `undefined-term` | Abbreviation, symbol, or specialist term used before or without definition; a term coined in the draft and never explained | First use of "ROS" with no expansion |
| `inconsistent-term` | One concept given several names, or one name used for several concepts; inconsistent symbols or units for the same quantity | "participants / subjects / patients / volunteers" for the same people; "expression" meaning mRNA in one place and protein in another |
| `subjective` | Evaluative, promotional, or emotive words that assert importance instead of showing it | "remarkable", "striking", "dramatic", "novel", "groundbreaking", "excellent", "huge", "perfectly", "unfortunately", "surprisingly", "interestingly", "obviously", "clearly" |
| `informal` | Colloquial words, idioms, contractions, rhetorical questions, exclamation marks, conversational fillers | "a lot of", "got", "kind of", "turned out", "can't", "big", "done by" |
| `absolute` | Unqualified universals and certainty words that evidence cannot support | "always", "never", "all", "none", "proves", "undoubtedly", "it is certain that", "the first ever" |
| `unsupported-generality` | Appeal to common knowledge or unnamed sources in place of a citation or data | "it is well known that", "studies have shown" with no citation, "researchers believe", "as everyone knows" |
| `anthropomorphism` | Intent, desire, or agency attributed to things that have none, where it could mislead about mechanism | "the cells try to", "the protein wants to", "evolution designed" |
| `false-precision` | More digits than the measurement or sample supports, or exact figures for estimates | "23.4567%" from n = 30 |
| `hidden-agent` | Passive or nominalised construction where the reader needs to know who or what acted and cannot tell | "It was decided to exclude three samples" → who decided, on what criterion |

## How to check

**Pronoun pass.** At every "this", "it", "they", "these", "those", "which", stop and
name the antecedent. If you hesitate, or if a noun closer to the pronoun could also
fit, flag it. Suggest replacing the pronoun with the noun phrase.

**Quantifier pass.** Search for the word lists in the table above (Grep is quick for
this on long drafts). For each hit, ask whether a number, unit, range, or citation
should stand there. Some vague words are legitimate (an Introduction may say "several
studies" before citing them); flag those that sit where a result, method, or
comparison needs a value.

**Term ledger.** While reading, keep a list of abbreviations, symbols, and key terms
with the place each is first used and first defined. At the end, anything used before
definition, never defined, defined twice differently, or used under several names is a
finding. Report each term once with all its locations.

**Register pass.** Read Abstract, Results, and Conclusion once looking only for
adjectives and adverbs. Each should carry measurable content; those that only
intensify or advertise are `subjective`.

**Two-readings test.** For any sentence you had to read twice, try to write down two
different things it could mean. If you can, quote both readings in the finding; this is
the clearest way to show the author the problem.

## Writing the suggestion

When the fix needs information you do not have, do not invent it. Offer a template
with a marked gap and ask the question:

- Original: "The yield was much higher in the treated group."
- Suggestion: "The yield was [X-fold / X%] higher in the treated group than in
  [comparison group] ([value ± uncertainty] vs [value ± uncertainty], n = [N])."
  Question for author: what are the two yields and the group sizes?

When the fix is purely a matter of wording (informal, subjective, unclear reference
with an obvious antecedent), give the full rewritten sentence.

Appropriate hedging is scientific, not vague. "These results suggest" and "may
contribute to" are correct when evidence is partial; do not flag them. Flag hedges
only when they are stacked ("may possibly suggest") or when they blur a result the
draft actually has ("the difference seemed to be somewhat larger").

## Do not flag

- Standard field terminology and abbreviations that the target journal's readers do not
  need defined (DNA, PCR, pH). When unsure, check whether the draft defines comparable
  terms; follow its own convention.
- "We" and first-person active voice; most journals accept it.
- Words like "significant" inside a quoted questionnaire item, title, or reference.
- Conventional anthropomorphic shorthand that cannot mislead ("the data show",
  "Table 2 presents", "this paper argues").

## Deeper checklists

- [third-party/flonat/check-categories.md](third-party/flonat/check-categories.md) §4
  (academic tone: filler phrases, vague quantifiers, tautologies), §2 (notation
  consistency), §9 ("significant" ambiguity, coefficients without units).
- [third-party/k-dense/writing_principles.md](third-party/k-dense/writing_principles.md)
  — "Numbers and units" lists what every reported number needs; "Accuracy before
  fluency" covers keeping observation, estimate, interpretation, and speculation
  distinct.
- [third-party/minhuw/grammar-checker.md](third-party/minhuw/grammar-checker.md) Pass 3
  and Pass 4 — inappropriate words, wordy and redundant phrases.
