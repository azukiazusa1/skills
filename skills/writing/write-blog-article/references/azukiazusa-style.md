# Azukiazusa house style

Use this guide to reproduce azukiazusa's recurring editorial decisions and cadence in original wording. House-style fidelity takes priority over generic technical-writing preferences. Do not copy distinctive sentences from existing articles.

## Metadata

- Keep the frontmatter limited to `title` and `about` unless the user requests more fields.
- Name the technology and the concrete value in the title. Use inline code for API, function, method, property, and syntax names when Markdown in the title is supported.
- Write `about` as two or three concrete sentences: establish the background or previous behavior, explain the feature or change, and state what the article demonstrates. Reveal the useful conclusion instead of teasing it.

## Article progression

1. Open with the reader's problem, relevant change, or practical outcome.
2. State the article's scope and destination with a phrase such as `この記事では` when it reads naturally.
3. For an experimental or version-dependent feature, state support and stability near the introduction. Keep detailed compatibility and fallback guidance later.
4. Explain the previous approach, prerequisite, or smallest concept before the new solution.
5. Progress from a minimal example to a practical example. Make each section establish one observable capability.
6. Explain constraints, failure conditions, compatibility, and fallback rather than stopping at the happy path.
7. End with `## まとめ` and concrete bullet-point propositions that introduce no new claims.
8. When external sources were used, end with `## 参考` and list primary sources. Also link evidence near the claims it supports.

## Voice and explanation rhythm

- Use polite Japanese in `です`/`ます` form. Prefer a calm, precise teaching voice over promotional excitement.
- Guide the reader through the sequence with natural transitions such as `まずは〜を確認しましょう`, `続いて〜を実装します`, `一方で`, `そのため`, and `このように`. Vary the wording; do not force a stock phrase into every section.
- Before code, explain its purpose. After code, identify the important lines and say what the reader can observe or conclude.
- Separate facts, observed results, inference, and opinion. Use softer first-person language only for genuine experience or interpretation.
- Prefer concrete explanations of causes and consequences over catalogs of syntax or features.

## Japanese formatting

- Insert a half-width space between Japanese text and Latin letters, Arabic numerals, units, or inline code: `CSS の`, `` `shape()` 関数``, `SVG パス`, `幅 320px`, `2 つ`, `2026 年 8 月 16 日`.
- Do not insert a space before Japanese punctuation or between Japanese characters.
- Use half-width Arabic numerals by default.
- Keep official product, specification, API, property, and method names in their official spelling.
- Use the same term for the same concept throughout the article.

## Code and visual evidence

- Keep samples small enough to reveal the behavior, but include the imports, markup, styles, configuration, and commands required to reproduce the stated result.
- Distinguish code shown to readers from an internal project created to validate the article. The internal project does not accompany the article by default. Do not mention its local path, repository directory, startup command, or reader availability unless the user explicitly agrees to publish it.
- Preserve useful evidence without exposing the internal artifact: write the validation date, environment, tested condition, and observed result directly. Prefer `フォールバックを強制した状態も確認したところ` over `検証用サンプルでは`.
- Use images for spatial or static results, video for motion or time-dependent behavior, and an interactive demo when manipulating the example materially improves understanding.
- Introduce every visual by telling readers what to inspect, then interpret what it confirms.
- If media is required but unavailable, leave this comment at the exact intended location:

```markdown
<!-- TODO(media): Insert a <screenshot|video|interactive demo> showing <specific state or action>. The reader should observe <specific result>. Alt text/caption: <description>. -->
```

- Never invent an asset, URL, observation, or caption. Keep the comment until a human or a separate media-sharing skill supplies the verified asset.

## Final comparison

Before completion, compare the draft with two or three azukiazusa articles of the same type when they are available. Check the opening, section progression, code narration, visual proof, support warning, transition phrases, summary, references, and Japanese/Latin spacing. Use the bundled case studies when the original articles are unavailable.
