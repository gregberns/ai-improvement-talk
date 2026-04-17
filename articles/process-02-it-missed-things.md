---
title: "It Missed Things"
group: process
order: 2
idea: "015"
status: draft
---

# Process: It Missed Things

*This is a series about moving your coding agent from intern to senior developer. It's for devs who are already using agents but not getting the results they keep hearing about.*

*Each article targets a specific problem. What you're experiencing, why it's happening, and what to do about it — with a prompt you can run immediately.*

*The articles build on each other. If you haven't gone through the previous articles, consider starting [at the beginning](./index.md).*

---

The planning approach is working. The agent investigates, thinks it through, brings you a plan, and it's implemented. The big stuff is right — approach, architecture, structure. But you review the implementation and things are missing. Details from the plan didn't make it into the code. Steps were skipped in the implementation.

Wasn't the plan supposed to fix this?

**Symptom:**

The plan was solid. The implementation missed things — not the big stuff, the small stuff. The stuff that adds up. You're still reviewing everything line by line.

**Why:**

Humans miss things. Agents miss things. We have code review, tests, QA — we know we need more than one pass. Agents need the same thing.

The problem isn't that the agent should do better. It's that one pass isn't enough. The agent needs to take multiple loops: review against the plan, fix the gaps, review again.

**Fix:**

Once the agent has finished — don't start by reviewing the code yourself. Get the agent to.

Point the agent at the plan and have it compare what was specified against what was built.

> Review the implementation against the plan in [plan file]. Compare every requirement and detail. What's missing? What doesn't match? What was skipped? Report the gaps — don't fix them yet.

Run it. Then keep reading.

**While it works:**

The review agent is going to come back with a list of gaps. Walk through them. Some will be obvious misses — things from the plan that didn't make it into the code. Some might be things the implementing agent interpreted differently than you expected.

You can either accept them all and tell the agent to go fix them, or work through them one at a time.

Once fixed, don't hesitate to run the review again if there were more than one or two items.

**How it works:**

Notice how the review agent reports the gaps — it doesn't fix them. This is deliberate. You're creating an adversarial process — one agent puts pressure on another to improve.

Why not just have the implementing agent review its own work? Same reason you don't proofread your own writing. The implementing agent has context bias — it "knows" what it intended, so it sees what it meant to build, not what it actually built. A separate review, working only from the plan, sees what's actually there.

Without a review step, "done" means "I think I'm done." With a review step, "done" means "it's been checked against the plan."

A missed detail caught at review is a quick fix. A missed detail that makes it to "done" could consume your afternoon.

**What's next:**

1. Make this part of your process. Every implementation gets a review against the plan.
2. When the review finds gaps — fix them, then review again.
3. Start paying attention to what gets missed. You can feed that back into your AGENTS file.

**Not yet:**

What you're building here — plan, implement, review, fix — is the core loop. We'll name it and formalize it later in the series.

You're verifying the creative work — did the implementation match the plan? But there's another category: procedural steps. Git workflows. Running tests. Pushing commits. The stuff that should happen the same way every time. That's next.
