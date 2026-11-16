# Seeded errors in `sample_draft.md`

The sample draft is fictitious and was written with these problems planted, to check
how many the proofreader finds. A finding counts as a hit if it identifies the same
problem, whatever subtype it is filed under. Items marked (minor) are borderline; a
good report may reasonably skip them.

## G · Grammar (9)

| # | Where | Seeded text | Problem |
|---|-------|-------------|---------|
| G-a | Abstract | "Sleep deprivation impair" | agreement |
| G-b | §1 | "it's stimulant effects" | its / it's |
| G-c | §1 | "Despite of this" | preposition |
| G-d | §2.2 | "they received … and it was tested" | pronoun number (may be filed under A as unclear reference) |
| G-e | §2.2 | "Using a standard laptop, the reaction time … were recorded" | dangling modifier and agreement |
| G-f | §3 | "The number of lapses were" | agreement |
| G-g | §4 | "The dopamine levels … supports" | agreement |
| G-h | §4 | "plasma caffeine concentrations was not measured" | agreement |
| G-i | §4 | "should be recommended always" | word order (minor) |

Trap, not an error: "Data was analysed" is accepted usage; flagging it as more than a
low-severity consistency note is a false positive.

## L · Logic disconnection (14)

| # | Where | Problem |
|---|-------|---------|
| L-a | Abstract / §2.1 | Sample size: 60 (abstract), 64 recruited, groups 32 + 30 = 62 |
| L-b | Abstract / §3 / Table 1 | Placebo mean 356 ms (abstract) vs 365 ms (results, table) |
| L-c | §3 | "difference of 44 ms": 365 − 312 = 53 |
| L-d | §2.2 / §3 / Abstract | "significant (p = 0.07)" against a stated threshold of 0.05; abstract says "significantly faster" |
| L-e | Abstract | "prove that caffeine fully restores cognitive function": only reaction time measured, no rested baseline |
| L-f | §1 | "However, many studies have reported…": no contrast with the previous sentence |
| L-g | §1 | Gap named is the dose–response relationship; the study tests a single dose |
| L-h | §1 / §2 / §3 | Aim (ii), habitual vs non-habitual consumers: no method for measuring intake, no group comparison reported |
| L-i | §3 | "Therefore, habitual caffeine consumption causes faster reactions": causation from a weak correlation |
| L-j | §4 | "Because the caffeine group was faster, caffeine must act by blocking adenosine A2A receptors in the striatum": mechanism does not follow from behavioural data |
| L-k | §4 | "The dopamine levels measured in our participants": no such measurement in Methods or Results |
| L-l | §4 | "it will apply to shift workers, older adults and patients with insomnia": generalising beyond the sample |
| L-m | §4 | "caffeine is the best countermeasure": no other countermeasure was compared |
| L-n | §3 | Subjective alertness and lapses reported with no method and no data |

## A · Ambiguous or non-scientific wording (11)

| # | Where | Seeded text | Problem |
|---|-------|-------------|---------|
| A-a | §1 | "It is well known that" | unsupported generality, no citation |
| A-b | §1 | "for a long time" | vague |
| A-c | §2.1 | "Participants" / "Subjects" / "volunteers" | inconsistent term |
| A-d | §2.2 | "some time later" | interval between dose and test not given |
| A-e | §2.2 | "a t-test" | which test, one- or two-sided (minor) |
| A-f | §3 | "much lower" | no values for lapses |
| A-g | §3 | "Interestingly", "really huge", "amazing" | subjective / informal |
| A-h | §3 | "given the small dose" | 200 mg called small with no reference point (minor) |
| A-i | §3 | "habitual coffee intake" vs "caffeine consumption"; r with no p or n | inconsistent term, missing detail |
| A-j | Abstract / §4 | "prove", "fully", "best", "always" | absolutes |
| A-k | Abstract | "significantly faster" | significance claim with no test (overlaps L-d) |
