# Third-party reference material

These files are unmodified copies from public, MIT-licensed agent-skill repositories,
pinned to the commit shown. Each folder carries the upstream `LICENSE`. They are
reference checklists only: the category labels, report format, and workflow come from
`../../SKILL.md`, which takes precedence wherever an upstream file says otherwise
(for example, upstream output formats, scoring rubrics, or venue-specific style rules).

| File | Upstream | Commit | Used for |
|------|----------|--------|----------|
| `minhuw/grammar-checker.md` | [minhuw/claude-writer](https://github.com/minhuw/claude-writer) `skills/grammar-checker/SKILL.md` | `b8754fa` | Grammar: multi-pass error lists, common non-native-speaker errors |
| `christopherkenny/proofread.md` | [christopherkenny/skills](https://github.com/christopherkenny/skills) `skills/proofread/SKILL.md` | `4682938` | Grammar: detailed usage and punctuation rules |
| `flonat/check-categories.md` | [flonat/flonat-research](https://github.com/flonat/flonat-research) `skills/proofread/references/check-categories.md` | `fbb0d35` | Logic: text↔table numeric cross-check, causal-language audit, equation completeness. Wording: academic tone, vague quantifiers. LaTeX notation consistency |
| `k-dense/logical_fallacies.md` | [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) `skills/scientific-critical-thinking/references/logical_fallacies.md` | `ec59a29` | Logic: catalogue of 40 reasoning fallacies with scientific examples |
| `k-dense/writing_principles.md` | same repo, `skills/scientific-writing/references/writing_principles.md` | `ec59a29` | Wording: evidence-proportional language, numbers and units |

Notes:

- Some upstream files link to sibling files that are not copied here
  (`review_sources.md`, `shared/tikz-rules.md`, `conventions.md`, and similar).
  Those links are dead in this copy; ignore them.
- Upstream rules that are specific to one venue or field (APSA style, American-English
  default, CS-conference tense conventions, economics identification strategies) apply
  only when the draft being proofread belongs to that venue or field.
- To update a file, re-download it from the upstream path and change the commit above.
