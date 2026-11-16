# Proofreading report: sample_draft.md

**Date:** 2026-11-16 · **Scope:** whole draft · **Length:** ~500 words

## Summary

| Category | High | Medium | Low | Total |
|----------|------|--------|-----|-------|
| G · Grammar | 0 | 3 | 2 | 5 |
| L · Logic disconnection | 9 | 3 | 0 | 12 |
| A · Ambiguous / non-scientific wording | 1 | 6 | 3 | 10 |
| **Total** | 10 | 12 | 5 | 27 |

**Most important to fix:**
- **L3:** the main result is called significant at p = 0.07 although Methods sets the threshold at p < 0.05. The Abstract and the Discussion both build on it as a positive finding.
- **L1 and L2:** the key numbers disagree. The sample size is 60, 64 or 62 depending on the place, and the placebo mean is 356 ms in the Abstract but 365 ms in Results and Table 1 (the stated 44 ms difference fits only 356).
- **L4, L9, L10, L11, L12:** the Abstract, Results and Discussion make claims the reported data do not reach ("prove", "causes", "must act by", "will apply to", "the best countermeasure").
- **Recurring habit:** subject–verb agreement fails five times (G1), usually where a phrase separates the subject from the verb.

**Notes:**
- The draft cites "[1, 2]" but contains no reference list, so the citations could not be checked.
- Table 1 is the only table and there are no figures. Table 1 was checked against the text.
- Lapses, subjective alertness, habitual coffee intake and dopamine levels are mentioned without values or methods (L8), so nothing about them could be reconciled.

## G · Grammar

### G1 · agreement (pattern, 5 instances) · Medium
- **Where:** Abstract — `sample_draft.md:5`; Methods §2.2 — `:21`; Results — `:25`; Discussion — `:38`, `:40`
- **Original:**
  - `:5` "Sleep deprivation impair cognitive performance"
  - `:21` "the reaction time of each participant were recorded over 10 minutes"
  - `:25` "The number of lapses were also much lower in the caffeine group."
  - `:38` "The dopamine levels measured in our participants supports this mechanism."
  - `:40` "plasma caffeine concentrations was not measured"
- **Problem:** In each case the verb does not agree in number with its subject ("deprivation", "time", "number", "levels", "concentrations"). In four of the five, a phrase between subject and verb hides the mismatch.
- **Suggestion:**
  - `:5` "Sleep deprivation impairs cognitive performance"
  - `:21` "the reaction time of each participant was recorded over 10 minutes" (see also G5)
  - `:25` "The number of lapses was also much lower in the caffeine group." (see also A8)
  - `:38` "The dopamine levels measured in our participants support this mechanism." (see also L8)
  - `:40` "plasma caffeine concentrations were not measured"

### G2 · punctuation · Low
- **Where:** Introduction — `sample_draft.md:9`
- **Original:** "Caffeine is an adenosine receptor antagonist, and it's stimulant effects have been studied for a long time."
- **Problem:** "it's" is the contraction of "it is"; the possessive is "its".
- **Suggestion:** "Caffeine is an adenosine receptor antagonist, and its stimulant effects have been studied for a long time." (see also A2)

### G3 · preposition · Low
- **Where:** Introduction — `sample_draft.md:9`
- **Original:** "Despite of this, little is known about the dose-response relationship in adults deprived of sleep for more than 24 hours."
- **Problem:** "Despite" takes no preposition ("despite this" or "in spite of this").
- **Suggestion:** "Despite this, little is known about the dose-response relationship in adults deprived of sleep for more than 24 hours."

### G4 · agreement · Medium
- **Where:** Methods §2.2 — `sample_draft.md:21`
- **Original:** "After that, they received either a capsule with 200 mg caffeine or a placebo capsule, and it was tested with the psychomotor vigilance task (PVT) some time later."
- **Problem:** The singular "it" does not agree with "they" (the participants). As written, "it" points to the capsule, so the sentence says the capsule was tested with the PVT.
- **Suggestion:** "After that, they received either a capsule with 200 mg caffeine or a placebo capsule, and they were tested with the psychomotor vigilance task (PVT) some time later." (see also A6)

### G5 · sentence-structure · Medium
- **Where:** Methods §2.2 — `sample_draft.md:21`
- **Original:** "Using a standard laptop, the reaction time of each participant were recorded over 10 minutes."
- **Problem:** Dangling modifier: the subject of the main clause is "the reaction time", which did not use the laptop.
- **Suggestion:** "The reaction time of each participant was recorded on a standard laptop over 10 minutes."

## L · Logic disconnection

### L1 · numeric-inconsistency · High
- **Where:** Abstract (`sample_draft.md:5`) vs Methods §2.1 (`:17`) vs Table 1 (`:31`–`:32`)
- **Original:** "in 60 sleep-deprived adults" / "Sixty-four healthy adults (aged 20–35 years) were recruited" / "a caffeine group (n = 32) or a placebo group (n = 30)"
- **Problem:** Three different sample sizes appear: 60 (Abstract), 64 (recruited), and 32 + 30 = 62 (group sizes in Methods and Table 1). No exclusions or withdrawals are described.
- **Suggestion:** Question for author: how many participants were recruited, randomised and analysed? State each number once and account for the differences, e.g. "Of 64 adults recruited, [N] were randomised and [N] were analysed; [N] were excluded because [reason]." Then make the Abstract match the number analysed.

### L2 · numeric-inconsistency · High
- **Where:** Abstract (`sample_draft.md:5`) vs Results (`:25`) vs Table 1 (`:32`)
- **Original:** "(mean reaction time 312 ms vs 356 ms)" / "compared to 365 ± 48 ms in the placebo group (Table 1). The difference of 44 ms was significant" / Table 1: "| Placebo | 30 | 365 | 48 |"
- **Problem:** The placebo mean is 356 ms in the Abstract but 365 ms in Results and Table 1. The stated difference of 44 ms equals 356 − 312; with the Results and Table 1 value the difference is 365 − 312 = 53 ms. The Results sentence therefore disagrees with itself.
- **Suggestion:** Question for author: is the placebo mean 356 ms or 365 ms? Correct the wrong value everywhere and recompute the difference (44 ms if 356; 53 ms if 365).

### L3 · numeric-inconsistency · High
- **Where:** Methods §2.2 (`sample_draft.md:21`) vs Results (`:25`), Abstract (`:5`) and Discussion (`:38`)
- **Original:** "p < 0.05 was considered significant" / "The difference of 44 ms was significant (p = 0.07)." / "responded significantly faster than those who received placebo" / "Our findings show that caffeine improves reaction time after sleep deprivation."
- **Problem:** p = 0.07 does not meet the draft's own threshold of p < 0.05, yet the difference is called significant in Results and in the Abstract, and the Discussion treats it as an established effect.
- **Suggestion:** Question for author: is the p-value or the label wrong? If p = 0.07 is correct, reword in all three places, e.g. Results: "The difference of [44/53] ms was not statistically significant (p = 0.07)."; Abstract: "Mean reaction time was lower in the caffeine group than in the placebo group (312 ms vs [356/365] ms), but the difference was not statistically significant (p = 0.07)."; and soften the first Discussion sentence accordingly.

### L4 · overclaim · High
- **Where:** Abstract — `sample_draft.md:5`
- **Original:** "These results prove that caffeine fully restores cognitive function after sleep loss."
- **Problem:** The claim outruns the evidence in three ways: "prove" is stronger than a single group comparison allows (and that comparison has p = 0.07, see L3); "fully restores" needs a rested baseline, and the draft reports none; "cognitive function" is broader than the one measure reported, PVT reaction time.
- **Suggestion:** Reword to what was measured, in line with the answer to L3, e.g. "These results suggest that a single 200 mg dose of caffeine may shorten reaction time after 30 h of wakefulness." Question for author: was a rested or pre-deprivation baseline measured? Without it, "restores" cannot be supported.

### L5 · wrong-connective · Medium
- **Where:** Introduction — `sample_draft.md:9`
- **Original:** "However, many studies have reported that caffeine improves vigilance during extended wakefulness [1, 2]."
- **Problem:** "However" signals a contrast, but this sentence agrees with the one before it (caffeine's stimulant effects are long studied). The real contrast comes in the next sentence ("little is known…").
- **Suggestion:** Remove the connective or use an additive one: "Many studies have reported that caffeine improves vigilance during extended wakefulness [1, 2]." Note that "many studies" is supported by two citations only; consider "Several studies" or adding citations.

### L6 · structure-gap · Medium
- **Where:** Introduction, gap statement (`sample_draft.md:9`) vs aims (`:11`) and Methods §2.2 (`:21`)
- **Original:** "little is known about the dose-response relationship in adults deprived of sleep for more than 24 hours" / "(i) to test whether a single dose of caffeine improves reaction time after 30 h of wakefulness"
- **Problem:** The stated knowledge gap is the dose-response relationship, but the study uses one dose (200 mg), which cannot describe a dose-response relationship. The aims do not address the gap the Introduction sets up.
- **Suggestion:** Question for author: what gap does the study fill? Either restate the gap so it matches the aims (e.g. "little is known about whether [a single dose / the effect in habitual vs non-habitual consumers] … after more than 24 hours of wakefulness"), or explain how a single-dose study bears on dose-response.

### L7 · structure-gap · Medium
- **Where:** Introduction, aim (ii) (`sample_draft.md:11`) vs Methods (`:17`–`:21`) and Results (`:34`)
- **Original:** "(ii) to determine whether the effect differs between habitual and non-habitual caffeine consumers" / "Reaction time was negatively correlated with habitual coffee intake across all participants (r = −0.21)."
- **Problem:** Aim (ii) asks whether the caffeine effect differs between two kinds of consumer. Methods defines no habitual and non-habitual groups, and Results gives only a correlation pooled over the caffeine and placebo groups. A pooled correlation does not show whether the effect of the capsule differs between consumer types, so aim (ii) is never answered as stated.
- **Suggestion:** Question for author: was the caffeine effect compared between habitual and non-habitual consumers (e.g. a group × consumption comparison)? If so, define the two groups in Methods and report that result. If only the correlation is available, reword aim (ii) to match it, e.g. "(ii) to examine whether reaction time is associated with habitual caffeine intake."

### L8 · structure-gap (pattern, 4 instances) · High
- **Where:** Results — `sample_draft.md:25`, `:34`; Discussion — `:38`; compare Methods §2.2 — `:21`
- **Original:**
  - `:25` "The number of lapses were also much lower in the caffeine group."
  - `:25` "the caffeine group showed a really huge improvement in subjective alertness"
  - `:34` "habitual coffee intake"
  - `:38` "The dopamine levels measured in our participants supports this mechanism."
- **Problem:** Four measures appear with no method behind them: lapses (not defined), subjective alertness (no scale or time of rating), habitual coffee intake (no instrument or unit) and dopamine levels (no sampling or assay). Methods describes only PVT reaction time and a t-test. Dopamine levels are also absent from Results, so the Discussion relies on data the reader never sees.
- **Suggestion:** For each measure, add how it was obtained to Methods and its values to Results, or remove the sentence. Questions for author: how was a lapse defined? Which alertness scale was used, and when? How was habitual intake assessed? Were dopamine levels actually measured, and if so, how and what were the values?

### L9 · overclaim · High
- **Where:** Results — `sample_draft.md:34`
- **Original:** "Therefore, habitual caffeine consumption causes faster reactions under sleep deprivation."
- **Problem:** A causal conclusion is drawn from a correlation (r = −0.21). Habitual consumption was not assigned by the experimenters, so the design the draft describes supports only an association, and no p-value shows that the correlation differs from zero (see A10).
- **Suggestion:** Reword to match the evidence, e.g. "Higher habitual coffee intake was thus associated with shorter reaction times under sleep deprivation (r = −0.21, p = […])." If the correlation is not significant, say so and drop "Therefore".

### L10 · non-sequitur · High
- **Where:** Discussion — `sample_draft.md:38`; compare the limitation at `:40`
- **Original:** "Because the caffeine group was faster, caffeine must act by blocking adenosine A2A receptors in the striatum."
- **Problem:** A shorter reaction time does not identify a receptor subtype or a brain region; the behavioural result is compatible with any mechanism of action. The only support offered is the dopamine data, which the draft never reports (L8). The certainty of "must" also sits badly with the limitation two sentences later that "the dose reaching the brain is unknown".
- **Suggestion:** Present the mechanism as an interpretation and give its source, e.g. "The faster responses in the caffeine group are consistent with blockade of adenosine A2A receptors in the striatum [citation], although this study did not test the mechanism." Question for author: is there a citation for this mechanism?

### L11 · overclaim · High
- **Where:** Discussion — `sample_draft.md:38`
- **Original:** "Since the effect was observed in young university volunteers, it will apply to shift workers, older adults and patients with insomnia."
- **Problem:** The premise argues against the conclusion: a result in healthy adults aged 20–35 after one night of supervised wakefulness does not establish the same effect in older adults, in chronic shift work or in a clinical sleep disorder. "Since… it will" presents the generalisation as a consequence of the sample.
- **Suggestion:** "Because the effect was observed in healthy young university volunteers, whether it applies to shift workers, older adults or patients with insomnia remains to be tested."

### L12 · overclaim · High
- **Where:** Discussion, conclusion — `sample_draft.md:40`
- **Original:** "In conclusion, caffeine is the best countermeasure for sleep loss and should be recommended always."
- **Problem:** The conclusion makes a claim that Results does not contain. "Best" requires a comparison with other countermeasures, and the study compared caffeine only with placebo. "Should be recommended always" is an unqualified universal drawn from one dose, one task and one sample, and it follows directly on a stated limitation.
- **Suggestion:** Restrict the conclusion to what was tested and align it with the answer to L3, e.g. "In conclusion, a single 200 mg dose of caffeine [shortened / did not significantly shorten] PVT reaction time after 30 h of wakefulness in healthy young adults."

## A · Ambiguous / non-scientific wording

### A1 · unsupported-generality · Medium
- **Where:** Introduction — `sample_draft.md:9`
- **Original:** "It is well known that sleep loss slows reaction time."
- **Problem:** An appeal to common knowledge stands in place of a citation.
- **Suggestion:** "Sleep loss slows reaction time [citation]."

### A2 · vague-quantity · Low
- **Where:** Introduction — `sample_draft.md:9`
- **Original:** "it's stimulant effects have been studied for a long time"
- **Problem:** "For a long time" gives no period and no source.
- **Suggestion:** "its stimulant effects have been studied for [period, e.g. more than N decades] [citation]", or delete the time phrase and cite a review: "its stimulant effects are well documented [citation]."

### A3 · inconsistent-term · Low
- **Where:** Introduction — `sample_draft.md:9`, `:11`; Methods §2.2 — `:21`
- **Original:** "more than 24 hours" / "after 30 h of wakefulness" / "stayed awake for 30 h" / "over 10 minutes"
- **Problem:** Time units are abbreviated in some places ("h") and spelled out in others ("hours", "minutes").
- **Suggestion:** Use one style throughout, e.g. "24 h", "30 h", "10 min".

### A4 · inconsistent-term · Medium
- **Where:** Introduction — `sample_draft.md:11`; Results — `:34`
- **Original:** "habitual and non-habitual caffeine consumers" / "habitual coffee intake" / "habitual caffeine consumption"
- **Problem:** "Coffee intake" and "caffeine consumption" are not the same quantity (caffeine also comes from tea, energy drinks and other sources), yet the draft moves between them within two sentences. The reader cannot tell which was measured.
- **Suggestion:** Question for author: was coffee intake or total caffeine intake assessed? Use that one term in the aim, the result and the conclusion drawn from it.

### A5 · inconsistent-term · Low
- **Where:** Abstract — `sample_draft.md:5`; Methods — `:17`, `:21`; Results — `:34`; Discussion — `:38`
- **Original:** "Participants who received caffeine" / "Subjects were randomly assigned" / "All volunteers gave written informed consent." / "Participants stayed awake" / "young university volunteers"
- **Problem:** The same people are called "participants", "subjects" and "volunteers". In §2.1 the three names appear in three consecutive sentences, which can suggest three different sets of people (for example, that only some gave consent).
- **Suggestion:** Use "participants" throughout: "Participants were randomly assigned…", "All participants gave written informed consent."

### A6 · vague-quantity · High
- **Where:** Methods §2.2 — `sample_draft.md:21`
- **Original:** "it was tested with the psychomotor vigilance task (PVT) some time later"
- **Problem:** The interval between capsule and test is not given. The study cannot be reproduced without it, and the result cannot be interpreted, because the effect of caffeine depends on the time since ingestion.
- **Suggestion:** "…and they were tested with the psychomotor vigilance task (PVT) [N] min later." Question for author: how long after the capsule did testing start, and was the interval the same for every participant?

### A7 · missing-detail · Medium
- **Where:** Methods §2.2 — `sample_draft.md:21`
- **Original:** "Data was analysed with a t-test and p < 0.05 was considered significant."
- **Problem:** "A t-test" does not say which test (independent-samples, Welch) or whether it was one- or two-sided, and it does not cover the correlation reported in Results.
- **Suggestion:** "Group means were compared with a [two-sided independent-samples / Welch] t-test; p < 0.05 was considered significant." Question for author: which t-test was used, and how was the correlation with habitual intake computed and tested?

### A8 · vague-quantity · Medium
- **Where:** Results — `sample_draft.md:25`
- **Original:** "The number of lapses were also much lower in the caffeine group."
- **Problem:** "Much lower" gives no values, no comparison group and no test, and "also" implies a significance that is in question (L3).
- **Suggestion:** "The number of lapses was lower in the caffeine group than in the placebo group ([value ± SD] vs [value ± SD]; p = […])." Question for author: what were the lapse counts in each group?

### A9 · subjective · Medium
- **Where:** Results — `sample_draft.md:25`
- **Original:** "Interestingly, the caffeine group showed a really huge improvement in subjective alertness, which was amazing given the small dose."
- **Problem:** "Interestingly", "really huge" and "amazing" are evaluative and informal and carry no measurable content; "improvement" has no stated baseline; "small dose" is a judgement with no reference dose. The sentence reports no value at all.
- **Suggestion:** "Subjective alertness was higher in the caffeine group than in the placebo group ([scale]: [value ± SD] vs [value ± SD]; p = […])." Question for author: what were the alertness scores, and compared with what is the improvement measured (placebo, or the participant's own score before the capsule)?

### A10 · missing-detail · Medium
- **Where:** Results — `sample_draft.md:34`
- **Original:** "Reaction time was negatively correlated with habitual coffee intake across all participants (r = −0.21)."
- **Problem:** The coefficient is given without its type (Pearson or Spearman), the number of participants it is based on, or a p-value, so the reader cannot judge whether the correlation differs from zero.
- **Suggestion:** "Reaction time was negatively correlated with habitual coffee intake across all participants ([Pearson/Spearman] r = −0.21, n = […], p = […])."
