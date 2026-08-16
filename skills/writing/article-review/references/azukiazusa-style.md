# Azukiazusa house style

Use this guide to identify meaningful differences from azukiazusa's recurring editorial structure and prose. Do not require copied phrases; require the same editorial decisions and cadence in original wording.

## Required patterns

- Use polite Japanese in `です`/`ます` form with a calm, precise teaching voice.
- Start from the reader's problem, relevant change, or practical outcome, then state the scope and destination.
- Let `about` use two or three concrete sentences covering background, technology, and outcome.
- Explain the previous approach or prerequisite before the new solution, and progress from a minimal example to a practical one.
- Before code or media, state its purpose or observation target. After it, explain the important part and the observed or expected result.
- Put experimental status or major compatibility limitations near the introduction; keep detailed fallback guidance later.
- End with `## まとめ` containing concrete propositions and `## 参考` containing primary sources when external sources were used.

## Japanese formatting

- Insert a half-width space between Japanese text and Latin letters, Arabic numerals, units, or inline code: `CSS の`, `` `shape()` 関数``, `SVG パス`, `幅 320px`, `2 つ`, `2026 年 8 月 16 日`.
- Do not insert a space before Japanese punctuation or between Japanese characters.
- Use half-width Arabic numerals by default and preserve official spelling.

## Visual evidence

Require an image for a material spatial or static result, a video for motion or time-dependent behavior, or an interactive demo when manipulating the example improves understanding. If the asset is unavailable, require a comment at the exact intended location:

```markdown
<!-- TODO(media): Insert a <screenshot|video|interactive demo> showing <specific state or action>. The reader should observe <specific result>. Alt text/caption: <description>. -->
```

The surrounding prose must tell readers what to inspect and what the result confirms. Never accept an invented asset, URL, or observation.

Treat projects created to validate claims as internal artifacts unless the user explicitly agrees to publish them. Flag article references to local paths, repository directories, startup commands, or an accompanying validation sample that readers will not receive. Keep useful validation evidence by stating the date, environment, tested condition, and observed result directly.
