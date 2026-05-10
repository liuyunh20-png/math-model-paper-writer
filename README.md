# math-model-abstract-writer

`math-model-abstract-writer` is a writing skill for Chinese Mathematical Modeling Competition papers (全国大学生数学建模竞赛), focused on **title**, **abstract**, and **keywords** generation/refinement.

It provides a structured framework distilled from analysis of 20+ excellent national papers (2019–2024).

## What this repository contains

- `SKILL.md`  
  Main skill definition, trigger scenarios, end-to-end workflow, and output format.
- `references/title_patterns.md`  
  Title templates (A/B/C/D), naming rules, and selection decision tree.
- `references/abstract_sop.md`  
  Standard operating procedure for abstract writing (structure, logic, wording, and length).
- `references/keyword_strategy.md`  
  Keyword selection strategy, layered method model, examples, and common pitfalls.
- `references/academic_expressions.md`  
  Domain-specific academic expressions and transition phrases for modeling papers.

## Core capabilities

1. **Title generation**
   - Selects title pattern by method complexity.
   - Produces concise, academic-style candidate titles.

2. **Abstract writing**
   - Follows a standardized structure:
     - Opening paragraph (background + objective)
     - Problem-by-problem method/result description
     - Optional conclusion (evaluation/sensitivity/improvement)

3. **Keyword recommendation**
   - Recommends 4–5 keywords with layered coverage:
     - Core method → auxiliary method → solving approach → validation/evaluation.

4. **Academic phrasing refinement**
   - Replaces colloquial language with formal research expressions.
   - Improves logical transitions across paragraphs and sub-problems.

## Typical workflow

1. Collect inputs:
   - problem background
   - number of sub-problems
   - methods/algorithms per sub-problem
   - key numerical results
   - tools/software used
2. Generate title candidates with `references/title_patterns.md`.
3. Draft abstract using `references/abstract_sop.md` + `references/academic_expressions.md`.
4. Select keywords using `references/keyword_strategy.md`.
5. Polish language and consistency with `references/academic_expressions.md`.

## Suggested output format

```text
标题：[生成的标题]

摘要：
[总起段]

针对问题一，[内容]
针对问题二，[内容]
针对问题三，[内容]

[可选总结段]

关键词：[关键词1] [关键词2] [关键词3] [关键词4] [关键词5]
```

## Notes

- This repository is primarily documentation/knowledge assets (no build or test pipeline included).
- Content is optimized for Chinese math-modeling paper writing conventions.

