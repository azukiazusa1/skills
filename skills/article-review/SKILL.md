---
name: article-review
description: Review a Japanese technical blog article against azukiazusa's house style, including title, summary, audience fit, structure, explanation rhythm, clarity, grammar, terminology, tone, spacing, media guidance, and consistency. Use for draft review, proofreading, copyediting, house-style comparison, or pre-publication editorial checks. Do not verify technical truth or modify the article unless the user asks for edits.
---

# Review a technical article

Act as an editor for Japanese technical blog articles. Focus on whether the intended reader can follow the argument accurately and efficiently and whether the draft reproduces azukiazusa's recurring editorial choices.

## Inputs and default behavior

Accept a Markdown or MDX file, pasted draft, or clearly identified article. If several plausible files exist and the target cannot be inferred, ask for the target.

Review without modifying the source by default. Edit only when the user explicitly requests changes.

Read the complete draft and [azukiazusa house style](references/azukiazusa-style.md) before reporting findings. Infer audience, article type, and maturity from the text when possible. If the user explicitly supplies another style guide, apply it instead and state that substitution.

## Review the draft

Read [the editorial checklist](references/editorial-checklist.md) and apply the relevant sections. Review:

- `title` and `about` when present;
- the introduction's problem, audience, scope, and destination;
- logical order and progression of headings;
- paragraph focus, transitions, and unnecessary repetition;
- explanations around code, figures, and examples;
- missing visual evidence and the specificity of `TODO(media)` comments;
- references to internal validation artifacts that readers will not receive;
- grammar, spelling, punctuation, terminology, tone, and formatting;
- the summary's fidelity to the body.

Treat documented house-style mismatches as findings rather than generic preferences. Preserve deliberate first-person usage, humor, and domain terminology when they remain consistent with the house style and do not obstruct the reader.

Do not claim to have checked technical accuracy. Flag a statement for `tech-review` when its truth or evidence is material, but keep the editorial finding about reader impact.

## Report actionable findings

Order findings by severity, then source location:

- `P0`: the article is unusable or materially misleading as written
- `P1`: a structural or language problem should be fixed before publication
- `P2`: a meaningful clarity or reader-experience improvement
- `P3`: an optional refinement

Use this compact form:

```text
[P1] Short finding title
Location: path/to/article.md:42
Impact: What the reader misunderstands or cannot do
Suggestion: Concrete replacement, move, deletion, or rewrite
```

Keep line ranges tight. Quote only enough text to identify the issue. Consolidate repeated instances of the same pattern. If there are no findings, say so and mention any portion that could not be reviewed.

Do not add a praise section unless requested.

## Apply requested edits

When the user requests edits, apply accepted changes while preserving meaning and voice. Do not silently alter the thesis, technical claims, scope, or author's opinion. Summarize changed files and any suggestions intentionally left unapplied.

When a screenshot, video, or interactive example is needed but unavailable, insert this non-rendering comment at the exact intended location:

```markdown
<!-- TODO(media): Insert a <screenshot|video|interactive demo> showing <specific state or action>. The reader should observe <specific result>. Alt text/caption: <description>. -->
```

Add prose before it that tells the reader what to watch for and prose after it that interprets the expected or verified observation. Never invent a media URL or claim that an unavailable asset was observed.
