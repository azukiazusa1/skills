# Technical review checklist

Apply only relevant checks and prioritize findings by impact.

## Claims and sources

- Every central factual claim is supported by a primary source or a documented observation.
- Version-sensitive facts have been checked against current information.
- Specifications and official documentation are represented accurately and in context.
- Historical discussions are dated and not presented as current requirements.
- A source actually supports the nearby claim.
- Missing rationale is not replaced with speculation.
- Fact, observation, inference, and opinion are distinguishable.

## Code correctness

- Syntax, types, control flow, and API usage are correct for the stated versions.
- Imports, dependencies, environment variables, configuration, and startup order are complete.
- Commands run from the documented directory.
- Samples avoid undefined state inherited from an earlier omitted block.
- Article snippets match the authoritative sample project.
- Expected output matches observed output.
- Error handling is appropriate for the article's teaching goal.
- Comments explain non-obvious reasons rather than narrating syntax.

## Reproducibility

- The validation date and relevant environment versions are recorded.
- Success criteria are observable and specific.
- Automated checks prove the claim they are cited for.
- Manual checks describe exact actions and observations.
- A single environment is not generalized to every implementation.
- Unverified behavior is clearly labelled.

## Design and reader understanding

- The chosen approach solves the stated problem.
- Alternatives and tradeoffs are represented fairly when central to the conclusion.
- Simplifications made for teaching do not train an unsafe or invalid practice.
- The progression from minimal example to realistic use does not hide a necessary concept.

## Risk and compatibility

- Security and privacy implications are addressed where relevant.
- Secrets and real credentials are absent from samples and output.
- Accessibility semantics and keyboard or assistive-technology behavior are considered for UI examples.
- Browser, runtime, platform, and library compatibility is accurate.
- Failure conditions, cleanup, operational limits, and fallback behavior are documented when readers may encounter them.
- Experimental APIs and unstable dependencies are labelled early.
