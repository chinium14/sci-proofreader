# Category G — Grammar

A finding belongs here when the sentence breaks a rule of written English: a reader
who knows the rule would call it an error regardless of the science. If the sentence is
grammatical but its meaning is unclear, it belongs in category A; if it is clear but
does not follow from the surrounding text, category L.

## Subtypes

Use one of these as the subtype label in each finding.

| Subtype | What to look for | Example → fix |
|---------|------------------|---------------|
| `spelling` | Misspellings, typos, wrong technical term spelling, duplicated words, search-and-replace leftovers | "the the sample"; "flourescence" → "fluorescence" |
| `agreement` | Subject–verb and pronoun–antecedent number agreement, especially across long intervening phrases | "The effect of the inhibitors were measured" → "was measured" |
| `tense` | Tense shifts inside a section; wrong tense for the function (methods and own results: past; established facts and what a figure shows: present) | "Cells were lysed and the lysate is centrifuged" → "was centrifuged" |
| `article` | Missing, extra, or wrong a/an/the | "We propose method" → "We propose a method"; "an unique" → "a unique" |
| `preposition` | Wrong preposition in a fixed pairing | "different with" → "different from"; "consists in" → "consists of"; "correlated to" → "correlated with" |
| `word-form` | Wrong part of speech or confusable pair | affect/effect, principal/principle, complement/compliment, "compared than" |
| `sentence-structure` | Fragments, run-ons, comma splices, missing words, dangling or misplaced modifiers | "Using PCR, the samples were amplified" (who used PCR?) → "We amplified the samples by PCR" |
| `parallelism` | Items in a list or comparison that are not grammatically parallel | "to measure, recording, and analysis of" → "to measure, record, and analyse" |
| `punctuation` | Missing or misplaced commas, semicolons, apostrophes; hyphenation of compound modifiers; that/which punctuation | "a well known method" → "a well-known method"; "it's value" → "its value" |
| `countability` | Count/non-count and singular/plural noun errors | "many evidences" → "much evidence"; "these data shows" → "these data show"; "researches" → "studies" |
| `capitalisation` | Inconsistent or wrong capitalisation of names, units, gene/protein conventions | "celsius" → "Celsius"; "Western Blot" mid-sentence → "western blot" |

Number and unit formatting that is purely mechanical also goes here: missing space
between number and unit ("5mg" → "5 mg"), a sentence starting with a numeral, mixed
decimal separators.

## How to check

Read each sentence on its own, slowly, as a copy editor would. Long sentences hide
agreement errors: find the grammatical subject, skip the intervening phrases, and read
the subject directly against its verb. For each participle phrase at the start of a
sentence ("Using…", "Based on…", "After adding…"), check that the subject of the main
clause is the thing doing the action.

Errors made repeatedly by the same author usually share a cause (article use,
prepositions, and countability are the common ones for authors whose first language is
not English). When the same error appears three or more times, report it once as a
pattern with all locations.

## What not to flag

- Anything inside math, code, citation keys, labels, URLs, or LaTeX/Markdown commands.
- Passive voice as such. It is normal in Methods. Flag it only when it hides who did
  what and the reader needs to know; that is then a category A finding, not grammar.
- Field-standard jargon, nomenclature, and abbreviations you do not recognise. Look for
  consistent use across the draft before deciding it is a typo.
- British or American spelling. Flag only a mix within one draft, as a single
  `spelling` pattern finding, and suggest standardising on whichever dominates.
- Stylistic preferences where both forms are accepted (split infinitives, sentence-final
  prepositions, "data is" in fields that use it, serial comma). Consistency within the
  draft is the only test.

## Deeper checklists

Read these when a draft has many grammar problems or you want a fuller list of
patterns. Their output formats and venue-specific rules do not apply here.

- [third-party/minhuw/grammar-checker.md](third-party/minhuw/grammar-checker.md) — five
  scanning passes and a list of frequent article, preposition, tense, and typo errors.
- [third-party/christopherkenny/proofread.md](third-party/christopherkenny/proofread.md)
  — detailed usage rules (that/which, whether/if, since/while, compare to/with) and a
  full punctuation section.
- [third-party/flonat/check-categories.md](third-party/flonat/check-categories.md) §1
  and §5 — spelling, and LaTeX-specific problems visible in the source.
