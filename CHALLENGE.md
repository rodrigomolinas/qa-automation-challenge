# QA Automation Engineer — Take-Home Challenge

Welcome, and thanks for taking the time. This challenge is designed to take about
**3 hours**. It's a take-home: do it on your own schedule, on your own machine.

## The scenario

> You've just joined as the **senior QA automation engineer** for an e-commerce
> company. The product is **https://automationexercise.com** — a working online
> store (browse products, register/login, add to cart, checkout, etc.).
>
> There is **no test automation yet**. A release is coming and you have limited
> time. Your job is to **lay the foundation** of an automation suite: decide what
> matters most, automate it well, and document the strategy behind your choices.

You are **not** expected to automate the whole site. We are far more interested in
your judgment than in your line count.

## Using AI is encouraged

Use Claude Code, Copilot, ChatGPT, or whatever you normally work with. We assume
you do — that's how modern engineering works. We're not testing whether you can
write a selector from memory; we're testing your **judgment, your craft, and your
ability to direct and verify AI output**. (See the "How I used AI" section below —
we want you to be open about it.)

## What to deliver

A single Git repository containing two things:

### 1. `STRATEGY.md` — your thinking (the most important deliverable)

A short document (roughly 1–2 pages — bullet points are fine) covering:

- **What you chose to automate, and why** — prioritized by risk and business value.
- **What you deliberately chose *not* to automate** — and the reasoning. This
  matters as much as what you included.
- **Key assumptions and trade-offs** you made given the 3-hour limit.
- **How I used AI** — what you used it for, an example where it gave you something
  wrong or suboptimal and how you caught it, and what you verified by hand.

### 2. A focused, well-architected test suite

- **Recommended stack: Playwright.** Use **C#** or **TypeScript**. You may use a
  different framework/language if you prefer — just justify it briefly in
  `STRATEGY.md`.
- Cover the **highest-value flows only**. A handful of well-designed, reliable
  tests will score *higher* than a large pile of shallow ones.
- Show your craft: sensible structure (e.g. page objects / fixtures), reusable
  helpers, meaningful assertions, externalized test data/config.
- Include a short **README** with the exact commands to install and run the tests.

### 3. One robustness ask

The live site is occasionally slow or flaky. Pick **one** flow that's prone to
flakiness, make it **reliable**, and briefly note in `STRATEGY.md`:

- how you made it robust (and what you avoided — e.g. arbitrary `sleep`s), and
- any **actual defects or odd behavior** you noticed on the site while testing.

## What we explicitly value (and don't)

- ✅ A small, well-reasoned suite over a large, shallow one.
- ✅ Clear reasoning about what you skipped and why.
- ✅ Honesty about where you used AI and where you overrode it.
- ❌ Volume for its own sake. Auto-generating 50 tests that all assert "page
  loaded" will score **lower**, not higher.
- ❌ Tests that don't run. We will run them.

## Submitting

- Put everything in a **private GitHub repository** and **share it** with the
  reviewer named in your invitation email (add them as a collaborator).
- The clock is **3 hours from when you start.** Commit and push what you have when
  time is up — we'd rather see an honest, partial submission with clear notes in
  `STRATEGY.md` than an over-polished one. Your commit history is fine to leave as-is.
- Before you finish, make sure a **fresh checkout runs** by following only your
  README.

## A note on the follow-up interview

We'll read your submission before we talk, and the interview will be built
**around it** — we'll ask you to walk through your decisions, defend trade-offs,
and adapt your design to new requirements live. So make choices you can stand
behind and explain. There are no trick questions; we just want to understand how
you think.

Good luck — we're looking forward to seeing your approach.
