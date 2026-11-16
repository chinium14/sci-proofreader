# Scientific Proofreader

A Claude Code plugin that proofreads scientific drafts and reports three kinds of problem,
each labelled and paired with a suggested fix:

| Label | Category | Examples |
|-------|----------|----------|
| **G** | Grammar | agreement, tense, articles, prepositions, sentence structure, punctuation |
| **L** | Logic disconnection | conclusion does not follow, missing step, overclaim, contradiction between sections, numbers that disagree, wrong connective, aim never addressed |
| **A** | Ambiguous or non-scientific wording | unclear "this/it", vague quantities, comparison with no baseline, undefined or inconsistent terms, "significant" without a test, subjective or informal language |

It only writes a report. It never edits the draft.

## Install

In Claude Code (CLI or desktop app):

```
/plugin marketplace add chinium14/sci-proofreader
/plugin install sci-proofreader@scientific-proof
```

From a local clone instead of GitHub:

```
/plugin marketplace add /path/to/sci-proofreader
/plugin install sci-proofreader@scientific-proof
```

To try it for one session without installing:

```bash
claude --plugin-dir /path/to/sci-proofreader
```

## Use

Open the folder that holds your draft in Claude Code, then either:

- ask in plain words: `Use the sci-proofreader agent to proofread drafts/paper.tex`
- mention the agent: `@agent-sci-proofreader:sci-proofreader drafts/paper.docx, Discussion only`
- run the skill in the current conversation: `/sci-proofreader:sci-proofread drafts/paper.md`
- start a whole session as the proofreader: `claude --agent sci-proofreader:sci-proofreader`

Supported inputs: `.tex` (follows `\input`/`\include`), `.md`, `.qmd`, `.txt`, `.docx`, `.pdf`,
or pasted text. The report is saved next to the draft as `<draft-name>.proofread.md`.

Each finding looks like this:

```markdown
### L1 · numeric-inconsistency · High
- **Where:** Methods §2.1 (`paper.tex:58`) vs Table 2 (`paper.tex:171`)
- **Original:** "A total of 48 samples were analysed." / Table 2: "n = 46"
- **Problem:** The sample size differs between Methods and Table 2, and no exclusion is described.
- **Suggestion:** Question for author: which is correct? If two samples were excluded, state where and why.
```

When a fix needs a fact only the author has (a number, a citation, which of two conflicting
values is right), the agent asks a question instead of inventing an answer.

[examples/sample_draft.md](examples/sample_draft.md) is a short fictitious draft with 34
planted errors, [examples/sample_draft.seeded-errors.md](examples/sample_draft.seeded-errors.md)
lists them, and [examples/sample_draft.proofread.md](examples/sample_draft.proofread.md) is
the report the agent produced for it (33 of 34 found).

## Layout

```
.claude-plugin/
  plugin.json                        plugin manifest
  marketplace.json                   lets this repository be added as a plugin source
agents/sci-proofreader.md            the agent: role, tools, preloads the skill
skills/sci-proofread/
  SKILL.md                           workflow, labelling rules, severity, report format
  references/
    grammar.md  logic.md  wording.md     subtypes and checks for G, L, A
    third-party/                         public skill files used as deeper checklists
examples/                            sample draft, its planted errors, and the resulting report
```

No `version` is set in the manifests on purpose: installed copies then follow the
repository's commits, so pushing a change is enough to publish an update.

### Without the plugin system

Copy `agents/sci-proofreader.md` to `~/.claude/agents/` and `skills/sci-proofread/` to
`~/.claude/skills/`, and in the copied agent file change the `skills:` entry from
`sci-proofreader:sci-proofread` to `sci-proofread`. The agent is then called
`sci-proofreader` and the skill `/sci-proofread`.

## Public skills used

No public skill covers this three-way labelling, and none checks logical flow across a
draft, so the workflow and the logic checks are written for this project. Four public,
MIT-licensed skills supply the detailed checklists. Unmodified copies of the relevant
files are in `skills/sci-proofread/references/third-party/`, pinned to a commit, with
their licences; see `SOURCES.md` there.

| Source | Used for |
|--------|----------|
| [minhuw/claude-writer](https://github.com/minhuw/claude-writer) `grammar-checker` | grammar passes, frequent article/preposition/tense errors |
| [christopherkenny/skills](https://github.com/christopherkenny/skills) `proofread` | usage and punctuation rules |
| [flonat/flonat-research](https://github.com/flonat/flonat-research) `proofread` | text↔table number cross-check, causal-language audit, academic tone, notation consistency |
| [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) `scientific-critical-thinking`, `scientific-writing` | catalogue of 40 reasoning fallacies; rules for numbers, units, and evidence-proportional wording |

## Adjusting

- Journal or lab conventions (British spelling, "data is", tense rules): add them to the
  "What not to flag" lists in `references/grammar.md` or `references/wording.md`.
- New subtype: add a row to the table in the matching reference file.
- Different report layout: edit "Report format" in `SKILL.md`.

After editing, run `claude plugin validate .` in this folder.

## Licence

MIT; see [LICENSE](LICENSE). Third-party files keep their own licences.
