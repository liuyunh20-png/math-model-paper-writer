# math-model-paper-writer

> A writing skill for mathematical modeling contest papers (CUMCM / MCM-ICM).
> **The author used this skill to write his own contest paper and won the Beijing First Prize (北京市一等奖) of the China Undergraduate Mathematical Contest in Modeling (CUMCM).**

---

## What it is

This is not a folder of sample papers. It is a **set of writing rules an AI agent can load and execute**: the tacit know-how of award-winning papers, decomposed into searchable, checkable, step-by-step reference files.

Drop this directory into the `skills/` folder of your AI coding/writing tool (CodeBuddy, Claude Code, etc.) and say "help me write a mathematical modeling paper". The agent follows the workflow in `SKILL.md`, loads the relevant references one at a time, and produces a paper that matches the reviewers' expectations: title, abstract, keywords, problem restatement, assumptions, notation, model building and solving, model evaluation, references, appendix.

## Why it improves your odds

Reviewers spend only a few minutes on a paper. **Structure, abstract, figures, and quantified results** largely determine the first impression. This skill turns each of them into a hard constraint:

| What reviewers look for | Corresponding rule in this skill |
| --- | --- |
| Is the abstract clear at a glance? | Three-part SOP, "every result must carry a number", always "本文" (this paper), never "we" |
| Is the structure complete and standard? | Ten-section framework with purpose, sub-structure, length share, and examples per section |
| Is the reasoning clear? | Problem analysis must include an overall flow chart |
| Is the modeling solid? | Candidate models by problem type, with applicability and pros/cons |
| Are the results credible? | Results must be interpreted for plausibility and real-world meaning; sensitivity analysis encouraged |
| Does it read like a paper? | Academic phrasing thesaurus and transition templates replace colloquial wording |
| Are figures sufficient? | Per-section figure/table recommendations, plus numbering and in-text citation rules |

## Where the rules come from

Every rule is reverse-engineered from real award-winning papers, and the source corpus ships with the repo so you can verify it yourself:

- **Ten-section framework, writing techniques, model catalog, figure conventions, case analysis** — derived from a structural analysis of **17 national first-prize papers** (2017C–2023C).
- **Title formulas, abstract SOP, keyword strategy, academic thesaurus** — derived from an analysis of the front matter of **20+ outstanding CUMCM papers (2019–2024)**.

The output is therefore not generic essay writing — it is text aligned with the writing paradigm of national first-prize papers.

## Directory structure

```
cumcm-math-model-skills/            <- Skill package root
├── SKILL.md                        Entry point: triggers, workflows, writing principles, resource index
├── README.md                       Chinese README
├── README-EN.md                    This file
├── references/                     Reference docs, loaded on demand
│   ├── paper-structure.md          Detailed breakdown of the ten-section structure
│   ├── writing-tips.md             Section-by-section techniques and pitfalls
│   ├── common-models.md            Catalog of common models with selection advice
│   ├── excellent-paper-cases.md    Case analysis of award-winning papers (by year)
│   ├── figure-guide.md             Figure/table conventions and per-section counts
│   ├── title-patterns.md           Title templates (patterns A–D) and decision tree
│   ├── abstract-sop.md             Standard operating procedure for abstracts
│   ├── keyword-strategy.md         Keyword selection strategy and thesaurus
│   └── academic-expressions.md     Academic phrasing thesaurus and transitions
├── assets/
│   └── paper-template.md           Ten-section template, ready to fill in
└── outstanding-paper/              Award-winning paper corpus (by year)
    ├── 2017C/  3 PDFs
    ├── 2018C/  3 PDFs
    ├── 2019C/  3 PDFs
    ├── 2020C/  4 PDFs
    ├── 2021C/  4 scanned JPG sets (225 files)
    ├── 2022C/  3 scanned JPG sets (113 files)
    └── 2023C/  4 PDFs
```

## How to use

### 1. Install

Copy the whole directory into your tool's skills folder (for example `~/.codebuddy/skills/` or the project's `.codebuddy/skills/`), keeping the structure unchanged. The frontmatter of `SKILL.md` declares `name` and `description`, so the tool auto-detects it and invokes the skill when you mention "mathematical modeling paper", "write the abstract", "suggest keywords", and similar intents.

### 2. Three typical workflows

**A. Write a full paper from scratch**

1. Load `references/paper-structure.md` to see what each section must contain.
2. Start from `assets/paper-template.md`.
3. Pick models with `references/common-models.md`; plan figures with `references/figure-guide.md`.
4. Once the body is done, refine title → abstract → keywords (these are finalized last).

**B. Write or polish only the front matter (title / abstract / keywords)**

Follow `title-patterns.md` → `abstract-sop.md` → `keyword-strategy.md` → `academic-expressions.md` to produce a ready-to-paste title, abstract, and keyword line.

**C. Review an existing paper**

Use `paper-structure.md` as a checklist, then cross-check with `writing-tips.md`, `figure-guide.md`, and `excellent-paper-cases.md` to find missing sections and scoring leaks.

### 3. Example prompts

```
Use the math modeling paper skill to write a complete paper for 2024 Problem C
Rewrite the abstract of this paper — every result must include concrete numbers
Suggest 5 keywords; core methods are grey prediction + genetic algorithm
Check whether the structure and figures of this paper follow the conventions
```

## Resource cheat sheet

| Task | File to load |
| --- | --- |
| Write a full paper / build the outline | `references/paper-structure.md` + `assets/paper-template.md` |
| How to write a specific section | `references/writing-tips.md` |
| Generate a title | `references/title-patterns.md` |
| Write an abstract | `references/abstract-sop.md` + `references/academic-expressions.md` |
| Choose keywords | `references/keyword-strategy.md` |
| Polish / academic phrasing | `references/academic-expressions.md` |
| Which model should I use? | `references/common-models.md` |
| Which figures, and how many? | `references/figure-guide.md` |
| See how others wrote it | `references/excellent-paper-cases.md` + `outstanding-paper/` |

## Hard rules

1. **Abstract first**: cover the whole paper within half to one page; one paragraph per sub-problem with "method + model + numerical conclusion".
2. **Use "this paper" (本文), never "we"**; refer to sub-problems as "For Problem 1 / 2 / 3 / 4".
3. **Quantify every result**, with concrete values and validation metrics.
4. **Problem analysis must include an overall flow chart.**
5. **Number every equation** so the body can cross-reference it.
6. **Key results must be visualized** as tables and figures, with counts controlled per section.
7. **Be objective in evaluation**: strengths, weaknesses, improvements, and generalization.
8. **Move code to the appendix**; keep the body clean.

## Who it is for

- First-time CUMCM / MCM-ICM participants unsure what a contest paper should look like.
- Teams that model well but lose points because they cannot write it up properly.
- Teams that need to align with national first-prize writing conventions in limited pre-contest time.
- Anyone turning existing modeling results into a well-formed paper (course papers, internal contests).

## Notes

- Documentation and corpus only — no build, no dependencies, no test pipeline.
- Papers under `outstanding-paper/` are for study and reference; copyright belongs to the original authors and the contest organizers. Not for commercial use.
- The skill provides writing patterns and methodological guidance; the models and conclusions are still yours to validate. Paper quality ultimately depends on the modeling itself.

Good luck with your contest.
