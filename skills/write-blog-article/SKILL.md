---
name: write-blog-article
description: Research, validate, and draft a Japanese technical blog article that reproduces azukiazusa's editorial structure, tone, explanation rhythm, and formatting conventions while helping the author learn the subject. Use when the user asks to write, draft, or develop a technical article, API introduction, implementation tutorial, technology comparison, or engineering experience post in this house style. Do not use for non-technical marketing copy or review-only requests.
---

# Write a technical blog article

Create an evidence-backed technical article in azukiazusa's house style without hiding the research and validation process from the author. Reproducing this house style takes priority over generic technical-writing conventions when they differ.

## Preserve the learning process

Explain discoveries when they affect the author's understanding or decisions. Distinguish current behavior, historical design discussion, observed results, inference, and opinion. Do not reduce the interaction to status updates.

## Load the relevant guidance

- Always read [azukiazusa house style](references/azukiazusa-style.md) before the interview, before drafting, and during the final editorial pass.
- Read [article types](references/article-types.md) before proposing the structure.
- Read [research and validation](references/research-and-validation.md) when the article makes externally verifiable technical claims or includes code.
- Read [case studies](references/case-studies.md) only when a concrete structural example would help.
- Read [review checklist](references/review-checklist.md) when dedicated review skills are unavailable.

## Follow the workflow

### 1. Understand the request

Inspect user-provided files and relevant workspace context before asking questions. Assume no repository-specific publishing convention unless the user supplies one. Classify the article as one primary type:

1. New API or feature introduction
2. Hands-on implementation tutorial
3. Investigation or comparison
4. Opinion or experience

Infer details that available evidence answers. Ask about authorial intent only when it changes the result.

### 2. Reach the first agreement gate

Conduct a thorough design interview until the user and author share the same understanding of the article. Treat the interview as a decision tree, not a fixed questionnaire.

- Ask exactly one substantive question at a time.
- For every question, recommend an answer and explain why it is the best default.
- Follow each answer into its dependent decisions and resolve every material branch before moving on.
- Challenge vague, contradictory, or underspecified answers with concrete examples and tradeoffs instead of silently choosing an interpretation.
- When the user asks what a question means, answer the clarification and then return to the unresolved question.
- Inspect the workspace or available sources instead of asking the user for facts that can be discovered directly.
- Track decisions throughout the interview. Revisit an earlier decision when a later answer conflicts with it.
- Do not declare alignment merely because the user accepts several recommendations. Continue until no unresolved decision could materially change the thesis, evidence, sample, structure, or reader outcome.

At minimum, reach shared understanding on:

- target reader and assumed knowledge;
- the concrete conclusion or capability the reader should take away;
- included and excluded scope;
- claims that require research;
- claims a sample must demonstrate;
- validation environment and success criteria;
- article type and provisional structure;
- title direction, `about` direction, and a short English kebab-case slug.

After resolving the full decision tree, summarize the decisions, assumptions, rejected alternatives, and remaining non-blocking uncertainties. Ask the user to correct the summary, then obtain explicit approval. Do not create the article file before approval unless the user explicitly asks to skip this gate.

### 3. Research and teach

Research the agreed questions. Browse whenever information may have changed, when the user requests current information, or when a cited source must be inspected. Prefer specifications, official documentation, official repositories, standards discussions, and release notes.

Explain important findings as they emerge, including surprising constraints, changes from older behavior, and documented design reasons. Do not invent a rationale when primary sources do not state one.

### 4. Plan and validate the evidence

Map each central claim to evidence. When execution can establish a central claim, create the smallest reproducible sample under `examples/<slug>/` and validate it in the relevant runtime or browser.

Keep the sample focused on the behavior being taught. Include required imports, dependencies, configuration, and commands. Record the date, environment, versions, success condition, and observed result. Ask before installing software, changing security-sensitive settings, or enabling experimental system flags.

Treat `examples/<slug>/` as an internal validation artifact by default. It supports the author's verification process but is not assumed to accompany the published article. Do not plan article sections around readers having access to this artifact unless the user explicitly agrees to publish it.

If the necessary environment is unavailable, mark the claim as unverified and stop short of presenting the article as complete. Never write an expected result as though it was observed.

### 5. Reach the second agreement gate

Present:

- the central thesis;
- important evidence and relevant design context;
- constraints, compatibility concerns, and unresolved questions;
- the proposed headings;
- the sample and validation result or plan;
- the primary sources.

Explain the choices, answer questions, and obtain explicit approval before drafting. Allow the user to explicitly waive this gate for a lightweight article.

### 6. Draft the article

Write in Japanese unless the user explicitly requests another language. Apply [azukiazusa house style](references/azukiazusa-style.md) to the metadata, introduction, transitions, explanations, formatting, media narration, summary, and references.

Unless the user selects another location, create `articles/<slug>.md` with only the required metadata:

```yaml
---
title: "<article title>"
about: "<specific summary that states the topic and outcome>"
---
```

Start with the reader's problem, relevant context, and destination. Introduce prerequisites before dependent concepts. Place evidence links near the claims they support. Before a code sample, state its purpose; after it, explain the important lines and observed result.

Keep public article examples distinct from internal validation artifacts. Include self-contained code excerpts needed to teach the behavior, and state the validation environment and observed result when useful. Unless the user explicitly agrees that the validation artifact will be published with the article, do not mention its local path, directory name, startup command, repository location, or availability to readers. Avoid phrases such as `検証用サンプルでは`; describe the tested condition and observation directly.

For behavior whose appearance, interaction, or change over time is material, show the result with an image, video, or interactive example. If the required media is not available, insert a non-rendering Markdown comment at the exact intended location instead of omitting the visual evidence or inventing an asset:

```markdown
<!-- TODO(media): Insert a <screenshot|video|interactive demo> showing <specific state or action>. The reader should observe <specific result>. Alt text/caption: <description>. -->
```

Introduce the intended observation before the comment and interpret the expected or verified result after it. Use `codepen-share` when it is available and an interactive browser-only example is appropriate; otherwise keep the comment as a human action item.

Include limitations, failure conditions, compatibility, and fallback strategies when relevant. End with a summary containing concrete bullet-point propositions and no new information. Include a references section whenever external sources were used.

### 7. Review the finished draft

If `article-review` is available, use it for editorial review and explicitly require comparison against [azukiazusa house style](references/azukiazusa-style.md). If `tech-review` is available, use it for technical review. Otherwise apply [the bundled review checklist](references/review-checklist.md).

Correct objective errors, typos, grammar mistakes, house-style mismatches, and mismatches with verified results. Manually check Japanese/Latin spacing even when no prose-validation tool is installed. Before changing the thesis, structure, scope, or author's opinion, explain the evidence and proposed revision and obtain agreement.

Repeat the affected review until no publication-blocking findings remain. Do not claim that an unavailable review skill or validation tool ran.

### 8. Report completion

Report:

- article path, type, audience, and central conclusion;
- primary sources and important design reasoning;
- internal validation artifact path, reproduction commands, environment, and result for the author's handoff, clearly separated from article content;
- completed reviews and any checks that could not run;
- unresolved questions and remaining human actions;
- the main ideas the author learned.

Do not publish, translate, generate promotional images, stage, commit, or push unless the user separately requests it.

## Stop conditions

Stop and ask for direction when a missing authorial choice would materially change the article, when a central claim cannot be verified, or when continuing requires new authority. Continue answering questions about the subject after the draft is complete.
