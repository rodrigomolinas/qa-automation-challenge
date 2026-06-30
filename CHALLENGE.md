# QA Automation Engineer — Take-Home Challenge

This challenge takes about **3 hours**. Work on your own machine, on your own
schedule.

## Overview

`https://automationexercise.com` is a working e-commerce site — browse products,
register and log in, add to cart, and check out. It publishes 26 functional test
cases, reproduced in **[`TEST_CASES.md`](./TEST_CASES.md)** so the challenge is
self-contained.

There is no automation yet. Your task is to **automate all 26 cases as a single,
well-structured test framework** running against the live site.

## Your task

Automate every case in `TEST_CASES.md`. The cases are written as happy-path scripts
— translate them into maintainable automation, not 26 standalone scripts.

Several cases share the same flows: registration, login, and the checkout sequence
recur across cases 14, 15, 16, 23 and 24. Structure your code so those flows are
written once and reused.

## Deliverables

A single Git repository (your fork) containing the following.

### 1. The test suite — all 26 cases

- **Recommended stack: Playwright** with **TypeScript** or **C#**. You may use
  another framework or language; if you do, explain why in `STRATEGY.md`.
- Each test mapped to its case number.
- Built as a framework: shared page objects/fixtures, reusable actions,
  externalized test data and config, no duplicated flows.
- Reliable: web-first waiting (no fixed `sleep`s), correct handling of downloads,
  dialogs, and test-data isolation.
- Meaningful assertions — verify real outcomes (prices, quantities, totals,
  addresses, the invoice), not just that an element is present.
- A **README** with the exact commands to install and run the suite.

### 2. `STRATEGY.md`

A short document (1–2 pages, bullets are fine) covering:

- **Architecture** — your main abstractions and how shared flows are reused.
- **Reliability** — how you keep the suite stable against a shared, occasionally
  slow site.
- **Redundancy** — which of the 26 overlap or add little value (by number), and how
  that shaped your design.
- **Gaps** — the 26 are happy-path only. What important coverage is missing
  (negative/validation paths, boundaries, security, accessibility, cross-browser),
  and what you would add first.
- **Assumptions & trade-offs** — given the 3-hour limit. If your suite is partial,
  say what is done and what is next.
- **Defects / oddities** — anything notable you found on the site.

## What we look for

- A clean, DRY framework where the 26 tests reuse shared flows.
- Tests that pass reliably, run after run.
- Meaningful assertions and clear reasoning about redundancy and gaps.

We will run the suite, more than once.

## Tooling

Use whatever tools you normally work with, including AI assistants. We care about
the result and the reasoning behind it.

## Getting started & submitting

- **Start:** fork this repo and work in your fork. The fork's creation time is your
  start time.
- **Time:** 3 hours. Commit and push what you have when the time is up — an honest
  partial submission with clear notes beats an over-polished one. Leave your commit
  history as-is.
- **Submit:** share your fork with the reviewer named in your invitation email (add
  them as a collaborator if your fork is private).
- Before you finish, confirm that a fresh checkout runs by following only your
  README.

Replace this repo's `README.md` with your own project README. Fill in `STRATEGY.md`.
Leave `CHALLENGE.md` and `TEST_CASES.md` in place.

## The interview

We read your submission before we talk and build the conversation around it — your
architecture, your trade-offs, the redundancy and gaps you identified, and adapting
the design to new requirements. Make choices you can explain.
