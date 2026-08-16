# Annotated article case studies

Use these examples to reproduce the author's editorial structure, explanation rhythm, tone, and evidence flow. Do not copy distinctive sentences verbatim; reproduce the recurring decisions and cadence in original wording. The source articles are in Japanese, and the resulting article should follow their Japanese house style unless the user explicitly requests another language.

## New API: Fetch API `textStream()`

Source: [Fetch API の textStream() でレスポンスをテキストとしてストリーミングする](https://azukiazusa.dev/blog/fetch-text-stream/)

Central outcome: readers learn how `textStream()` replaces an explicit `TextDecoderStream` pipeline and how the behavior can be observed.

Structural pattern:

1. State that the feature is new and establish its support status.
2. Show the previous approach before the new call so the value is concrete.
3. Explain the API's return value and edge behavior near the smallest example.
4. Run a focused browser sample and describe the observation.
5. Summarize the behavioral difference and link to specifications and implementation discussions.

Reusable lesson: introduce a new API as a change to an existing task, not as an isolated catalog of methods.

## Tutorial: Hono logs with Pino and OpenTelemetry

Source: [Hono のログを Pino と OpenTelemetry で計装する](https://azukiazusa.dev/blog/instrument-hono-logs-with-opentelemetry/)

Central outcome: readers build a Hono application whose structured logs can be correlated with traces and inspected in an observability backend.

Structural pattern:

1. Explain why logs and traces must be correlated before introducing packages.
2. Build the application in responsibility-sized stages: SDK, logger, spans, request logging, startup order, collector, and backend.
3. Give exact commands and complete configuration for a multi-process system.
4. Validate first that logs arrive, then that navigation from a log to its trace works.
5. End with operational constraints rather than stopping at successful startup.

Reusable lesson: a long tutorial remains navigable when each stage establishes one observable capability and prepares the next.

## Investigation: accessible streaming chat UI

Source: [ストリーミングされるチャット UI の回答をスクリーンリーダーに伝える手法の調査](https://azukiazusa.dev/blog/accessible-streaming-chat-ui/)

Central outcome: readers understand why token-by-token live-region updates can be disruptive and how to separate answer content from status announcements.

Structural pattern:

1. Define the accessibility primitives needed for the investigation.
2. Inspect multiple real products and libraries before proposing a solution.
3. Include a documented failure report to show that the problem occurs outside the author's sample.
4. Derive an implementation from the observations.
5. Validate it with a named browser and screen reader and state the limits of that environment.

Reusable lesson: comparisons become actionable when observations are converted into a design rule and then tested in a new sample.

## Experience: design-centered AI coding workflow

Source: [最近の AI コーディングで実践している、設計を中心とした開発の進め方](https://azukiazusa.dev/blog/recent-ai-coding-development-process-centered-on-design/)

Central outcome: readers see how one engineer shifted effort from implementation toward design, task boundaries, validation, and review as coding agents became more autonomous.

Structural pattern:

1. State the current practice and how it changed over time.
2. Describe concrete practices rather than presenting only a general opinion.
3. Explain the reasoning and tradeoffs behind each practice.
4. Mark uncertainty and ongoing experimentation instead of turning experience into universal law.
5. Close by connecting individual practices to a broader change in engineering bottlenecks.

Reusable lesson: an experience article is persuasive when it exposes context, reasons, limits, and unresolved questions.
