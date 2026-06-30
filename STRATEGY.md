# Strategy

> All 26 cases are in scope, so this doc is where you show senior judgment *about*
> them — architecture, reliability, redundancy, and gaps. Fill in each section
> (bullets are fine, ~1–2 pages). Reference cases by number. Delete these
> quote-blocks as you go.
>
> The case list with full steps is in `TEST_CASES.md`.

## Stack choice

> Which framework/language did you use? We recommend Playwright with C# or
> TypeScript — if you chose something else, justify it briefly here.

## Architecture

> How did you structure the suite so 26 tests share flows instead of duplicating
> them? What are your main abstractions (page objects, fixtures, actions, data
> builders) and why? How is the heavily-repeated checkout flow (14/15/16/23/24)
> handled in one place?

## Reliability

> How do you keep the suite green against a flaky, shared live site? Web-first
> waiting, retries, test-data isolation, download/dialog handling — and what did you
> deliberately avoid (e.g. arbitrary sleeps)?

## Redundancy & value

> Which of the 26 are low-value or overlap heavily (be specific by number — e.g. the
> scroll cases 25/26, the subscription cases 10/11, the near-identical order cases)?
> How did that shape your design?

## Gaps in the published suite

> The 26 are nearly all happy-path. What's missing? Call out the most important
> untested risks (negative/validation paths, boundaries, data, security,
> accessibility, cross-browser, etc.) and which one or two you'd add first.

## Assumptions & trade-offs

> What did you assume about the product/users? What did you trade off given the
> 3-hour limit? If the suite is partial, what's done and what's next?

## How I used AI

> What you used AI for. A concrete example where it gave you something wrong or
> suboptimal and how you caught it. What you verified by hand.

## Defects / oddities noticed

> Any real bugs or odd behavior you ran into on the site while testing.
