# QA Automation Engineer — Take-Home Challenge

Welcome, and thanks for taking the time. This challenge is designed to take about
**3 hours**. It's a take-home: do it on your own schedule, on your own machine.

## The scenario

> You've just joined as the **senior QA automation engineer** for an e-commerce
> company. The product is **https://automationexercise.com** — a working online
> store (browse products, register/login, add to cart, checkout, etc.).
>
> The site publishes **26 test cases** at
> https://automationexercise.com/test_cases. They are also reproduced in this repo
> in **[`TEST_CASES.md`](./TEST_CASES.md)** so your work is self-contained.
>
> There is **no test automation yet**. Your job is to **automate all 26 cases** —
> and, more importantly, to build them as a **real, maintainable automation
> framework**, not 26 disposable scripts.

## What this challenge is really testing

Automating 26 documented happy-path scripts is something an AI can churn out quickly
— and that's exactly the point. **We are not impressed by 26 passing tests.** We've
seen what a naive AI dump looks like: 26 brittle, copy-pasted scripts that each
re-implement login and checkout, full of hard-coded waits, that flake the moment the
shared live site is slow.

What we're looking for is what a **senior** does with the same task:

- **Architecture & reuse.** Many of the 26 share the same flows — registration,
  login, add-to-cart, and the checkout sequence repeat across cases 14/15/16/23/24.
  A senior factors that ruthlessly (page objects, fixtures, shared actions, test
  data builders) so 26 tests don't mean 26 copies. We will be reading for this.
- **Reliability at (small) scale.** 26 tests against a shared, occasionally-flaky
  live site is a real reliability problem. Make them pass *consistently* — proper
  web-first waiting, no arbitrary `sleep`s, sensible retry/isolation strategy.
- **Meaningful assertions.** Assert real outcomes (prices, quantities, totals,
  addresses, the actual invoice), not just "an element is visible."
- **Judgment, expressed in `STRATEGY.md`** (see below) — including which of the 26
  are low-value or redundant, and what the published suite is *missing*.

## Using AI is encouraged

Use Claude Code, Copilot, ChatGPT, or whatever you normally work with. We assume you
do. Since the 26 cases come with step-by-step instructions, an AI can generate
automation for them almost verbatim — so this challenge is deliberately about the
things AI *can't* do for you: **good architecture, real reliability, sound
judgment, and verifying that what the AI produced is actually correct.** Be open
about how you used it (see the "How I used AI" section below).

## What to deliver

A single Git repository (your fork) containing the following.

### 1. The automated suite — all 26 cases

- **Recommended stack: Playwright.** Use **C#** or **TypeScript**. You may use a
  different framework/language if you prefer — just justify it briefly in
  `STRATEGY.md`.
- **All 26 cases** from `TEST_CASES.md`, automated. Map each test to its case
  number so we can see the coverage.
- Built as a **framework, not a pile of scripts**: shared page objects/fixtures,
  reusable actions, externalized test data and config, no duplicated flows.
- **Reliable**: web-first waiting, no arbitrary `sleep`s, proper handling of
  downloads/dialogs/test-data isolation. We will run the suite, more than once.
- A short **README** with the exact commands to install and run the tests.

### 2. `STRATEGY.md` — your thinking

The 26 are a given; this is where you show senior judgment *about* them. A short
doc (roughly 1–2 pages, bullets are fine) covering:

- **Architecture** — how you structured the suite so 26 tests share flows instead of
  duplicating them. What are your main abstractions and why?
- **Reliability** — how you keep the suite green against a flaky shared site. What
  did you deliberately avoid?
- **Redundancy & value** — which of the 26 are low-value or overlap heavily (be
  specific by number), and how that influenced your design.
- **Gaps in the published suite** — the 26 are nearly all happy-path. What's
  *missing* (negative/validation paths, boundaries, security, accessibility,
  cross-browser…) and which one or two would you add first?
- **Assumptions & trade-offs** given the 3-hour limit.
- **How I used AI** — what you used it for, a concrete example where it gave you
  something wrong or suboptimal and how you caught it, and what you verified by hand.
- **Defects/oddities** — any real bugs or odd behavior you noticed on the site.

## What we explicitly value (and don't)

- ✅ A clean, DRY framework where 26 tests reuse shared flows.
- ✅ Tests that pass *reliably*, run after run.
- ✅ Meaningful assertions and honest judgment about redundancy and gaps.
- ✅ Openness about where you used AI and where you overrode it.
- ❌ 26 copy-pasted scripts that each re-implement login/checkout.
- ❌ Hard-coded `sleep`s and "element is visible" assertions that can't really fail.
- ❌ Tests that don't run, or that only pass sometimes.

## Getting started & submitting

- **Start:** **fork this repo** and work in your fork. Your fork's creation
  timestamp is your official start time.
- **Clock:** you have **3 hours from that start time.** Commit and push what you
  have when time is up — we'd rather see an honest, partial submission (with clear
  notes in `STRATEGY.md` on what's done and what you'd do next) than an over-polished
  one. Leave your commit history as-is.
- **Deliver:** share your fork with the reviewer named in your invitation email
  (add them as a collaborator if your fork is private).
- Before you finish, make sure a **fresh checkout runs** by following only your
  README.

This repo includes a `STRATEGY.md` template with the sections we expect — fill it
in. Replace this challenge `README.md` with your own project README (how to install
and run your tests).

## A note on the follow-up interview

We'll read your submission before we talk, and the interview will be built
**around it** — we'll ask you to walk through your architecture, defend your
abstractions, justify the gaps and redundancies you identified, and adapt your
design to new requirements live. So make choices you can stand behind and explain.
There are no trick questions; we just want to understand how you think.

Good luck — we're looking forward to seeing your approach.
