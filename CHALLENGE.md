# QA Automation Engineer — Take-Home Challenge

Welcome, and thanks for taking the time. This challenge is designed to take about
**3 hours**. It's a take-home: do it on your own schedule, on your own machine.

## The scenario

> You've just joined as the **senior QA automation engineer** for an e-commerce
> company. The product is **https://automationexercise.com** — a working online
> store (browse products, register/login, add to cart, checkout, etc.).
>
> The site publishes **26 documented test cases** here:
> **https://automationexercise.com/test_cases** (also listed below). They are
> almost all happy-path, step-by-step scripts.
>
> There is **no test automation yet**. A release is coming and you have limited
> time. Your job as the senior is **not to mechanically automate all 26** — it's to
> decide what actually matters, automate that well, and tell us what's missing from
> this list.

You are **not** expected to automate the whole list. In fact, automating all 26
shallowly will score **lower** than automating a well-chosen handful properly. We
are far more interested in your judgment than your line count.

## Using AI is encouraged

Use Claude Code, Copilot, ChatGPT, or whatever you normally work with. We assume
you do — that's how modern engineering works.

Note that the 26 published cases come with step-by-step instructions, so an AI can
churn out automation for any of them almost verbatim. That's exactly why this
challenge is about the things AI *can't* do for you: **prioritization, critique,
craft, and verifying that what the AI produced is actually correct.** (See the
"How I used AI" section below — be open about it.)

## The 26 published test cases

These are the documented cases on the site. Treat this as your backlog — the raw
material you prioritize and critique. Full steps for each are at
https://automationexercise.com/test_cases.

1. Register User
2. Login User with correct email and password
3. Login User with incorrect email and password
4. Logout User
5. Register User with existing email
6. Contact Us Form
7. Verify Test Cases Page
8. Verify All Products and product detail page
9. Search Product
10. Verify Subscription in home page
11. Verify Subscription in Cart page
12. Add Products in Cart
13. Verify Product quantity in Cart
14. Place Order: Register while Checkout
15. Place Order: Register before Checkout
16. Place Order: Login before Checkout
17. Remove Products From Cart
18. View Category Products
19. View & Cart Brand Products
20. Search Products and Verify Cart After Login
21. Add review on product
22. Add to cart from Recommended items
23. Verify address details in checkout page
24. Download Invoice after purchase order
25. Verify Scroll Up using 'Arrow' button and Scroll Down functionality
26. Verify Scroll Up without 'Arrow' button and Scroll Down functionality

## What to deliver

A single Git repository (your fork) containing the following.

### 1. `STRATEGY.md` — your thinking (the most important deliverable)

A short document (roughly 1–2 pages — bullet points are fine) covering:

- **Prioritization** — which of the 26 cases you chose to automate, ranked by risk
  and business value. Reference them by number.
- **What you deliberately cut, and why** — which cases you judged low-value or not
  worth automating, with reasoning. This matters as much as what you included.
- **Gaps in the published suite** — these 26 are nearly all happy-path. What's
  *missing*? Call out the most important untested risks (e.g. negative/validation
  paths, boundary/data cases, security, accessibility, cross-browser) and which
  one or two you'd add first.
- **Key assumptions and trade-offs** you made given the 3-hour limit.
- **How I used AI** — what you used it for, an example where it gave you something
  wrong or suboptimal and how you caught it, and what you verified by hand.

### 2. A focused, well-architected test suite

- **Recommended stack: Playwright.** Use **C#** or **TypeScript**. You may use a
  different framework/language if you prefer — just justify it briefly in
  `STRATEGY.md`.
- Automate the **subset you prioritized** — a handful of well-designed, reliable
  tests beats a large pile of shallow ones. Map each test to the case number(s) it
  covers.
- You are encouraged to **go beyond the literal published steps** where it adds
  real value (e.g. stronger assertions, a negative variant of a happy-path case).
- Show your craft: sensible structure (e.g. page objects / fixtures), reusable
  helpers, meaningful assertions, externalized test data/config.
- Include a short **README** with the exact commands to install and run the tests.

### 3. One robustness ask

The live site is occasionally slow or flaky. Pick **one** flow that's prone to
flakiness, make it **reliable**, and briefly note in `STRATEGY.md`:

- how you made it robust (and what you avoided — e.g. arbitrary `sleep`s), and
- any **actual defects or odd behavior** you noticed on the site while testing.

## What we explicitly value (and don't)

- ✅ A small, well-reasoned subset over a large, shallow one.
- ✅ Clear reasoning about what you cut and what the published suite is missing.
- ✅ Honesty about where you used AI and where you overrode it.
- ❌ Volume for its own sake. Automating all 26 with shallow "page loaded"
  assertions will score **lower**, not higher.
- ❌ Tests that don't run. We will run them.

## Getting started & submitting

- **Start:** **fork this repo** and work in your fork. Your fork's creation
  timestamp is your official start time.
- **Clock:** you have **3 hours from that start time.** Commit and push what you
  have when time is up — we'd rather see an honest, partial submission with clear
  notes in `STRATEGY.md` than an over-polished one. Leave your commit history as-is.
- **Deliver:** share your fork with the reviewer named in your invitation email
  (add them as a collaborator if your fork is private).
- Before you finish, make sure a **fresh checkout runs** by following only your
  README.

This repo includes a `STRATEGY.md` template with the sections we expect — fill it
in. Replace this challenge `README.md` with your own project README (how to install
and run your tests).

## A note on the follow-up interview

We'll read your submission before we talk, and the interview will be built
**around it** — we'll ask you to walk through your prioritization, defend what you
cut, justify the gaps you identified, and adapt your design to new requirements
live. So make choices you can stand behind and explain. There are no trick
questions; we just want to understand how you think.

Good luck — we're looking forward to seeing your approach.
