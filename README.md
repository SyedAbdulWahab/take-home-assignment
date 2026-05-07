# Take-Home Assignment — Product-Minded Software Engineer

## Context

We're building an internal **Employee Directory & Lifecycle** service for HR teams.

Your primary user is **Priya, an HR Business Partner**. She opens this tool several times a day to:
- Answer questions like "who's on Maya's team?" or "who joined this quarter?"
- Onboard new hires into the directory
- Process departures when people leave the company

You're the engineer building the first version. There is no PM yet — you'll be making product calls as well as engineering ones.

## Stack

- **Backend:** Spring Boot (Java). A starter project is provided.
- **Frontend:** React, with Jest for tests.
- **Data:** `data.json` is provided as the seed source. You can keep it as a file or move to an in-memory DB — tell us why in your decision log.

## A note on AI tools

We use Claude and similar tools daily ourselves and expect you will too. We're not testing whether you can avoid them; we're testing your judgment when using them. In your decision log, be transparent about:

- Where you accepted AI output as-is vs. where you modified or rejected it
- Decisions where you chose to think it through yourself before prompting
- Anything the AI suggested that, on reflection, was wrong

Submissions that read as "pasted-in Claude output" without engineering judgment behind them are easy to spot and don't do well in the follow-up call.

## What to build

### Backend

A small HTTP service that supports Priya's workflow. At minimum we'd like:

1. **A way to find people.** Priya should get useful answers to questions like "who's on a given team?" and "who joined recently?" The exact endpoint shape and query design are your call.
2. **A way to add a new employee** to the directory.
3. **A way to handle a departure** — when someone leaves the company, they should no longer appear as active. *There are real edge cases buried in this one. We want to see how you reason about them, not just a flag flip.*

Treat the three above as a **starting point, not a checklist.** Add endpoints you think Priya needs. Skip or defer anything you don't think is worth the time, as long as you say why in your decision log.

All responses are JSON. Add the validation and error handling you'd expect in a code review at a serious company.

### Frontend

A single page Priya opens when she sits down at her desk. It should help her do her job — we trust you to figure out what that means in practice.

We'll look at:
- Which information you surface first, and why
- How you handle empty, loading, and error states
- Whether the page reflects Priya's actual workflow, not just "render every field"

You don't need to wire up every backend endpoint to a UI element. If something is backend-only, that's fine — note it.

### Tests

Some unit tests on both sides. We don't expect full coverage. We'd rather see a few well-chosen tests — **including at least one that exercises an edge case you identified yourself** — than a sea of trivial ones.

## What to submit

A repo (or zip) named `{lastname}-exercise` containing the code and a `DECISIONS.md` file with the following sections:

1. **Assumptions.** What did you assume about Priya, the data, the company? What would you have asked a PM if you could? List 3-5.
2. **Trade-offs.** Pick the three decisions you spent the most time on. For each: what you chose, what you rejected, and why.
3. **Edge cases.** What did you find — especially around departures and the manager/reports relationship? Which did you handle, which did you defer, and why? Be specific. *"I handled validation"* says nothing; *"if Maya is deactivated while she has four direct reports, I [X] because [Y], though [Z] would be a stronger long-term fix"* says everything.
4. **What you'd build next.** Three things, ranked, with reasoning. ("More tests" and "more polish" don't count.)
5. **AI usage.** A few lines: where Claude helped, where you overrode it, where you didn't use it.

Keep `DECISIONS.md` to roughly 1-2 pages. We read it carefully — often before the code.

## How we evaluate

After you submit, we'll have a **30-minute call** to walk through your submission together. Expect us to:

- Ask why you didn't do something reasonable that you skipped (there's no wrong answer if your reasoning is solid)
- Change a requirement on you mid-conversation and see how you'd adapt the design
- Push on the edge cases you raised in `DECISIONS.md`

You don't need to anticipate every question. You do need to be able to defend or revise the calls you made — and saying *"I'd change my mind, here's why"* is a perfectly good answer.

Good luck — we're looking forward to seeing what you build.
