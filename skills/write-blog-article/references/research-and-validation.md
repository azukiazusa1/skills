# Research and validation

## Use primary sources

Prefer sources in this order when they exist:

1. Current specifications, explainers, and official API documentation
2. Official repositories, release notes, and implementation documentation
3. Standards issues, pull requests, meeting records, and vendor positions
4. Official tests and samples

Use secondary sources for discovery and orientation, not as the only support for a central technical claim. Open the underlying source rather than relying on a search-result summary.

Investigate historical design discussion only when the article explains why an API has its current shape, compares rejected alternatives, or otherwise depends on that history. Do not make design-history research mandatory for a straightforward usage tutorial.

When no source documents a rationale, say that no rationale was confirmed. Keep dated historical proposals separate from current normative behavior.

## Build a claim-evidence map

Before implementing a sample, state the central claim and how it will be observed.

| Claim | Suitable evidence |
| --- | --- |
| An API returns a value | Output, assertion, or trace |
| DOM or accessibility behavior changes | DOM, accessibility tree, or assistive-technology observation |
| A failure occurs | Exact error and conditions |
| A fallback works | Reproduced unsupported condition and observed result |
| A type rule holds | Typecheck or type test |
| One option differs from another | Equivalent inputs and recorded outputs |

Do not add multiple scenarios unless they are necessary to support the article's conclusion.

## Create a reproducible sample

- Place complete files under `examples/<slug>/`.
- Exercise the technology itself rather than simulating the expected result.
- Keep UI and styling no larger than needed to observe the behavior.
- Record exact setup and run commands.
- Include required dependencies, imports, configuration, and environment-variable names.
- Avoid embedding secrets or production credentials.
- Prefer a project-level check over executing isolated Markdown snippets.
- Ensure article snippets match the verified source files.

## Record validation

Record:

- validation date;
- operating system when relevant;
- browser, runtime, compiler, framework, and package versions;
- commands and manual actions;
- success criteria;
- observed output;
- important failure conditions;
- anything that could not be verified.

Do not install missing software or change experimental flags without approval. If validation cannot be completed, label the draft as awaiting validation and avoid asserted results.
