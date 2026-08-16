# Writing skills

Reusable [Agent Skills](https://agentskills.io/specification) for researching, drafting, reviewing, and sharing Japanese technical blog articles. Each directory under [`skills/`](skills/) is an independent skill and can be installed separately.

## Skills

| Skill | Purpose |
| --- | --- |
| [`write-blog-article`](skills/write-blog-article/) | Research, validate, and draft a Japanese technical article in azukiazusa's house style while keeping the author involved in the learning and editorial decisions. |
| [`article-review`](skills/article-review/) | Review a Japanese technical article against azukiazusa's structure, explanation rhythm, prose, spacing, and media conventions. |
| [`tech-review`](skills/tech-review/) | Verify technical claims, sources, code, reproducibility, risk, and compatibility. |
| [`codepen-share`](skills/codepen-share/) | Turn a verified browser-only sample into a launcher for an unsaved CodePen. |

`write-blog-article` uses `article-review` and `tech-review` when they are installed, but also includes a compact fallback checklist. `codepen-share` remains separate because most technical articles do not target CodePen.

## Default article output

Unless the user chooses another location, `write-blog-article` creates an article and an internal validation workspace:

```text
articles/
└── <slug>.md
examples/
└── <slug>/
```

The article requires only this frontmatter:

```yaml
---
title: "Article title"
about: "A specific summary of the topic and outcome."
---
```

## Install

List the skills available in this repository:

```bash
npx skills add azukiazusa1/skills --list
```

Start the interactive installer and select the skills and target agents:

```bash
npx skills add azukiazusa1/skills
```

Install one skill for Codex in the current project:

```bash
npx skills add azukiazusa1/skills \
  --skill write-blog-article \
  --agent codex
```

Install all writing skills for Codex globally:

```bash
npx skills add azukiazusa1/skills \
  --skill write-blog-article \
  --skill article-review \
  --skill tech-review \
  --skill codepen-share \
  --agent codex \
  --global
```

## License

[MIT](LICENSE)
