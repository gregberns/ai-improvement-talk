---
title: "The Code Isn't Right"
group: process
order: 1
idea: "014"
status: draft
---

# The Code Isn't Right

*This is a series about moving your coding agent from intern to senior developer. It's for devs who are already using agents but not getting the results they keep hearing about.*

*Each article targets a specific problem. What you're experiencing, why it's happening, and what to do about it — with a prompt you can run immediately.*

*The articles build on each other. If you haven't gone through the previous articles, consider starting at the beginning.*

---

Your PM says you need a new REST endpoint. Straightforward — there are endpoints that do almost the same thing. You tell your agent what to build.

"Add a new REST endpoint POST /api/users/invite. Check if the user exists, generate an invitation token, send an email through the notification service, return the status. Use the auth middleware for admin-only access. Add tests."

Good instructions. Covers all the pieces. Should be straightforward.

The agent finishes and it's a mess. Existing patterns ignored. Conventions missed. Code that reinvents things that already exist.

You try again — more detail, every step spelled out. Somehow its worse.

**Symptom:**

The agent builds something — and you spend the next hour undoing it. Wrong approach, wrong patterns, wrong conventions. The output doesn't match what you'd have written. You think: "Half the time I'd be faster without the agent."

**Why:**

When you tell the agent to "go implement this," it executes. It doesn't question your approach, doesn't explore the codebase, doesn't look at how similar things are already done. It just does what you said.

"Add a new REST endpoint" is a command. Commands put the agent into execution mode. What you want is reasoning mode.

The trigger: replace "Add a new REST endpoint" with "Think through how we would add a new REST endpoint."

**Fix:**

Treat the agent like a senior developer who just joined your team. They're capable — they just need context. Explain your intent, not the steps. Describe the problem, not the solution.

Grab your next feature. Describe what you're trying to achieve. Mention gotchas, old patterns, anything you'd tell a new smart teammate. Append that to this prompt:

> Below is the next task we need to work on. Let's work through this together — gathering info, clarifying the challenge, and digging into the details — step by step. Once we've agreed on the plan, write a spec with explicit implementation instructions and save it to a file. Have an agent review the spec and correct any issues. Break the spec into discrete ordered tasks, write them to a file, and have them reviewed. Delegate implementation to a sub-agent — one task at a time — and act as the orchestrator. Before proceeding with implementation, ask if we're ready. If additional context would help understand the problem better — ask. Here's what we need:

Run it. While it's running, keep reading to understand the why.

**NOTE:** Do not let Claude Code go into "Plan Mode" — that's a tool setting, not what we're doing here.

Details in this prompt will be covered in later articles. Study it or just run it — we'll get there.

**While it works:**

The agent is going to come back with a plan. You need to work with it, section by section, to refine what's needed, clarify conventions and patterns, and fill non-obvious gaps. Ask questions. Challenge assumptions. Get clarification.

You're working to create alignment. Modifying the plan is much cheaper than refactoring. The larger the change, the more time you should spend here.

**How it works:**

"Add a REST endpoint." That's a command — and it invokes execution mode. Every decision you didn't make, it guesses. It doesn't look around. It doesn't ask. It just goes.

"Think through how we would add a REST endpoint." That invokes reasoning mode. The agent investigates. Finds existing patterns. Thinks through the approach. Brings you a plan. Implements from its own understanding — not your incomplete shorthand.

Same model. Completely different behavior.

**What's next:**

1. Work through the plan with the agent until it matches your expectations.
2. Let it implement. One task at a time.
3. Start with one feature. You should see a difference.

**Not yet:**

The plan catches the big stuff — wrong approach, missed constraints, bad assumptions. But implementation details can still get missed. Conventions skipped, edge cases dropped, steps forgotten. We'll cover how to find those gaps in the next article.
