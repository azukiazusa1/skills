# Fallback review checklist

Use this checklist only when the dedicated `article-review` or `tech-review` skill is unavailable.

## Editorial review

- Does the draft follow `references/azukiazusa-style.md`, including Japanese/Latin spacing, polite explanatory tone, and recurring section names?
- Does the title name the technology and the article's specific value?
- Does `about` usually use two or three concrete sentences to state the background, technology, and outcome without hiding the conclusion?
- Does the introduction identify the reader's problem, scope, and destination?
- Do headings follow the reader's questions or actions in a logical order?
- Are prerequisites introduced before dependent concepts?
- Does each paragraph advance one main idea?
- Are grammar, spelling, terminology, tone, and formatting consistent?
- Does the draft preserve the author's voice instead of normalizing stylistic preferences?
- Does the summary restate concrete conclusions without new claims?
- When appearance, interaction, or time-based behavior matters, does the article include visual evidence or an exact `TODO(media)` comment with the medium, content, observation, and alt text or caption?
- Does an experimental or version-dependent feature state support status near the introduction, with details and fallback later when needed?
- Does the article avoid mentioning internal validation paths, directories, startup commands, repositories, or a supposedly accompanying sample unless publication of that artifact was explicitly agreed?
- Are validation conditions and observations stated directly instead of being attributed to an unavailable `検証用サンプル`?

## Technical review

- Are central claims supported by current primary sources or recorded observations?
- Are normative requirements, implementation behavior, inference, and opinion distinguished?
- Do code samples parse, run, and produce the stated result in the documented environment?
- Do article snippets match the verified sample?
- Are versions, prerequisites, imports, configuration, and commands complete?
- Are security, privacy, accessibility, compatibility, failure modes, and fallback addressed where relevant?
- Are historical discussions presented as historical rather than current requirements?
- Are unverified claims explicitly marked?

Prioritize findings as:

- `P0`: unsafe or fundamentally false; publication must stop
- `P1`: substantive error that should be fixed before publication
- `P2`: meaningful clarity or quality improvement
- `P3`: optional refinement
