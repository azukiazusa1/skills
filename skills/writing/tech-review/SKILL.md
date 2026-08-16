---
name: tech-review
description: Review a technical blog article for factual accuracy, source quality, current API behavior, code correctness, reproducibility, security, accessibility, compatibility, and consistency between claims and observed results. Use for technical review or pre-publication verification. Do not perform general copyediting or modify files unless the user asks for edits.
---

# Review technical accuracy

Review a technical article as a skeptical engineer and reader. Prioritize correctness, evidence, reproducibility, and the consequences of following the article.

## Inputs and default behavior

Accept a Markdown or MDX file, pasted draft, or clearly identified article. Inspect linked local sample files and relevant project configuration when available.

Review without modifying the source by default. Edit only when explicitly requested.

Infer the audience and article type from the draft when possible. Ask a question only when a missing fact blocks meaningful verification.

## Establish the verification scope

Read [the technical checklist](references/technical-checklist.md). Identify:

- central claims and conclusions;
- version-sensitive or time-sensitive statements;
- normative statements about specifications or APIs;
- code intended to run;
- reported observations and validation environments;
- advice with security, privacy, accessibility, compatibility, or operational consequences.

## Verify evidence and current behavior

Browse when a claim may have changed, when a cited source must be inspected, or when the user requests current verification. Prefer current specifications, official documentation, official repositories, release notes, standards discussions, and official tests.

Open sources rather than relying on search-result summaries. Distinguish normative requirements, implementation-specific behavior, historical proposals, author inference, and opinion. Do not invent a design rationale.

## Validate code proportionately

Prefer the article's complete sample project and documented commands over executing isolated Markdown blocks. Confirm that article snippets match the verified sample.

Use already available runtimes and project commands. Do not install packages, fetch dependencies, contact external services, or change system flags without the required user approval. Avoid executing destructive, credential-bearing, or production-targeting examples.

When execution is safe and possible, record the command, environment, result, and any divergence from the article. When it is not possible, perform a static review and label the limitation. Never treat a syntax check as proof of runtime behavior.

## Report actionable findings

Order findings by severity, then source location:

- `P0`: unsafe, fundamentally false, or publication-blocking
- `P1`: substantive technical error that should be fixed before publication
- `P2`: meaningful correctness, evidence, or reproducibility improvement
- `P3`: optional technical refinement

Use this compact form:

```text
[P1] Short finding title
Location: path/to/article.md:42
Impact: The concrete technical or reader consequence
Evidence: Source, command result, or reasoning that establishes the issue
Suggestion: A specific correction or verification step
```

Place citations next to claims they support. Keep line ranges tight and consolidate repeated instances. If there are no findings, say so and list material checks that could not be completed.

Do not add a praise section unless requested. Leave prose-only issues to `article-review` unless they change technical meaning.

## Apply requested edits

When the user requests fixes, apply objective corrections that the evidence supports. Ask before changing the thesis, scope, architecture, or authorial opinion. Re-run affected checks and report the files, commands, results, and unresolved items.
