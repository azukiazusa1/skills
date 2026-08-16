# Editorial checklist for technical articles

Apply judgment; not every item creates a finding.

## Metadata

- The title identifies the technology or problem and the article's specific value.
- `about` usually uses two or three concrete sentences and works without surrounding context by stating the background, technology, and outcome.
- The title and `about` accurately represent the body rather than overselling it.

## Audience and introduction

- The intended reader and prerequisites can be inferred.
- The opening starts from a problem, decision, or useful outcome rather than empty scene-setting.
- Scope and destination appear early enough to guide the reader.
- Experimental status or a major limitation appears before readers invest in the procedure.

## Structure

- Headings follow the reader's questions or actions rather than the implementation's internal taxonomy alone.
- Prerequisites appear before concepts that depend on them.
- Difficulty increases gradually.
- Sections are proportionate to their importance.
- The draft does not repeat the same explanation in the introduction, body, and conclusion.

## Paragraphs and sentences

- Each paragraph advances one main idea.
- References such as “this,” “it,” and “the above” have clear antecedents.
- Causes, actions, and outcomes are not compressed into an overloaded sentence.
- Transitions make contrasts, consequences, and sequence explicit where needed.
- Abstract explanations are followed by a concrete example when one would materially help.
- Hedging and certainty match the evidence described by the author.

## Code and media narration

- Text before a sample tells readers why it appears.
- Text after a sample identifies the important part and the expected or observed result.
- Screenshots and diagrams are introduced and interpreted rather than left unexplained.
- Captions and alternative text describe useful content when present.
- Appearance, interaction, and time-based behavior have visual evidence or an exact `TODO(media)` comment specifying the medium, content, observation, and alt text or caption.
- The article does not mention internal validation paths, directories, startup commands, repositories, or an accompanying sample unless publication of that artifact was explicitly agreed.
- Validation conditions and observations are stated directly rather than attributed to an unavailable `検証用サンプル`.

## Language and consistency

- Japanese and Latin letters, numbers, units, and inline code use the spacing defined in `references/azukiazusa-style.md`.
- Grammar, spelling, punctuation, capitalization, and spacing follow one consistent pattern.
- Official product and API names use their official spelling.
- The same concept uses the same term throughout.
- Acronyms and specialist terms are explained at first use when the audience may need it.
- Prose style remains consistent without erasing the author's intentional voice.
- Links use descriptive labels rather than raw destinations when prose allows.

## Ending

- The summary restates concrete conclusions from the body.
- The summary introduces no new claim.
- References are present when the article relies on external material.
- Recurring headings use `## まとめ` and `## 参考` unless the article has a concrete reason to differ.
