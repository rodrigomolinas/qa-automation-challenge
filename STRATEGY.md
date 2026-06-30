# Strategy

> Fill in each section below — bullets are fine, ~1–2 pages total. Reference cases by
> number. The full case list is in `TEST_CASES.md`. Delete these quote-blocks as you
> go.

## Stack

> Which framework/language did you use? We recommend Playwright with TypeScript or
> C# — if you chose something else, explain why.

## Architecture

> Your main abstractions (page objects, fixtures, actions, data builders) and how
> shared flows are reused. How is the repeated checkout flow (cases 14, 15, 16, 23,
> 24) implemented in one place?

## Reliability

> How you keep the suite stable against a shared, occasionally slow site: web-first
> waiting, retries, test-data isolation, download/dialog handling — and what you
> deliberately avoided (e.g. fixed sleeps).

## Redundancy

> Which of the 26 overlap or add little value (be specific by number — e.g. the
> scroll cases 25/26, the subscription cases 10/11, the near-identical order cases),
> and how that shaped your design.

## Gaps

> The 26 are happy-path only. What important coverage is missing (negative/validation
> paths, boundaries, data, security, accessibility, cross-browser), and what you
> would add first.

## Assumptions & trade-offs

> What you assumed, and what you traded off given the 3-hour limit. If the suite is
> partial, what is done and what is next.

## Defects / oddities

> Anything notable you found on the site while testing.
