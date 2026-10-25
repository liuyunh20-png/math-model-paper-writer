# math-model-paper-writer

A writing skill for mathematical modeling contest papers (China Undergraduate Mathematical Contest in Modeling and similar competitions), bundled with a corpus of national first-prize papers. This directory itself is a standard Skill package.

## Directory structure

```
math-model/                        <- Skill package root
├── SKILL.md                       Skill entry point: workflows, writing principles, resource index
├── README.md                      This file
├── references/                    Reference docs, loaded on demand
│   ├── paper-structure.md         Detailed breakdown of the ten-section paper structure
│   ├── writing-tips.md            Section-by-section writing techniques
│   ├── common-models.md           Catalog of commonly used models and methods
│   ├── excellent-paper-cases.md   Case analysis of award-winning papers
│   ├── figure-guide.md            Figure/table conventions and count recommendations
│   ├── title-patterns.md          Title templates and selection decision tree
│   ├── abstract-sop.md            Standard operating procedure for abstracts
│   ├── keyword-strategy.md        Keyword selection strategy
│   └── academic-expressions.md    Academic phrasing thesaurus
├── assets/
│   └── paper-template.md          Ten-section paper template ready to fill in
├── outstanding-paper/             Award-winning papers (original files)
│   ├── 2017C/   3 PDFs
│   ├── 2018C/   3 PDFs
│   ├── 2019C/   3 PDFs
│   ├── 2020C/   4 PDFs
│   ├── 2021C/   4 scanned JPG sets (225 files)
│   ├── 2022C/   3 scanned JPG sets (113 files)
│   └── 2023C/   4 PDFs
```

## Capabilities

This skill merges two original skill packages and covers the full paper-writing workflow:

| Original skill | What it contributes | Files here |
|---|---|---|
| `math-modeling-paper` | Ten-section outline, per-section writing methods, model selection, figure conventions, template, case studies | `paper-structure.md`, `writing-tips.md`, `common-models.md`, `figure-guide.md`, `excellent-paper-cases.md`, `assets/paper-template.md` |
| `math-model-abstract-writer` | Title generation, abstract SOP, keyword strategy, academic polishing | `title-patterns.md`, `abstract-sop.md`, `keyword-strategy.md`, `academic-expressions.md` |

## Quick workflow

1. Start a new paper from `assets/paper-template.md`, filling in each section against the ten-section outline in `references/paper-structure.md`.
2. Choose models with `references/common-models.md`.
3. Plan figures and tables with `references/figure-guide.md`.
4. After the body is complete, refine the front matter: title (`title-patterns.md`) -> abstract (`abstract-sop.md`) -> keywords (`keyword-strategy.md`), then polish with `academic-expressions.md`.
5. To study real writing, browse `outstanding-paper/` by year.

## Rename history

| Original file | Current file |
|---|---|
| `math-model-content/论文图片统计与使用指南.md` | `references/figure-guide.md` |
| `references/abstract_sop.md` | `references/abstract-sop.md` |
| `references/academic_expressions.md` | `references/academic-expressions.md` |
| `references/keyword_strategy.md` | `references/keyword-strategy.md` |
| `references/title_patterns.md` | `references/title-patterns.md` |

Only the naming style was unified (underscores to hyphens); file contents were not modified.

## Notes

This directory contains only documentation and corpus assets. It has no build or test pipeline.
