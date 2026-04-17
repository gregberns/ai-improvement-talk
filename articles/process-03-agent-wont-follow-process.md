---
title: "The Agent Won't Follow the Process"
group: process
order: 3
idea: "016"
status: draft
---

# Process: The Agent Won't Follow the Process

*This is a series about moving your coding agent from intern to senior developer. It's for devs who are already using agents but not getting the results they keep hearing about.*

*Each article targets a specific problem. What you're experiencing, why it's happening, and what to do about it — with a prompt you can run immediately.*

*The articles build on each other. If you haven't gone through the previous articles, consider starting at the beginning.*

---

In the past couple articles we've made the implementation more consistent. Planning works. The review process catches gaps.

But the agent keeps dropping the ball on the basics. It says it's done, but the tests weren't run and there are failures. It compiled but didn't lint. It committed but didn't push. The last mile is unreliable.

Two steps forward, one step back. More babysitting.

**Symptom:**

The agent handles the hard stuff. But the routine stuff — testing, linting, committing, pushing — gets skipped. These are procedural workflows: multiple steps, done consistently, every time. The agent treats them as optional. You're babysitting the last mile.

**Why:**

Maybe you've told a hundred agents to run the tests before finishing. Maybe you've even mentioned it in the AGENTS file. But it's not working consistently. That's a signal — the agent doesn't have the instructions, they aren't encoded clearly enough, or they aren't getting reinforced.

Instead of getting frustrated and asking "why didn't you do that?" — we need to focus on reducing the likelihood of it happening again.

If it's not encoded, it's optional. If it's optional, it gets skipped. If it keeps getting skipped, the encoding isn't strong enough.

**Fix:**

When the agent misses a procedural step, don't just tell it again. Have the agent diagnose the problem and fix its own configuration.

> We're seeing a process issue. [Describe what was missed — e.g., "tests weren't run before marking the task complete"]. Look at the current agent configuration — AGENTS files, rules, hooks — and figure out why this wasn't enforced. Propose a fix that ensures this happens consistently. Diagnose the problem and implement the fix.

This combines two techniques we've already discussed. Continual improvement from [Evolve Your Project Metadata](./metadata-02-evolve-project-metadata.md) — see a problem in a session, have the agent improve the configuration. And posing the issue as a problem to be solved from [The Code Isn't Right](./process-01-code-isnt-right.md) — not a command to be obeyed. Think: "Let's figure out why this is happening."

**While it works:**

Review what the agent proposes. Does it make sense? Is it targeting the right step? Push back if it's too narrow — "always run `npm test` before committing" is more useful than "run `npm test` after implementing the invite endpoint."

This will take more than one pass. Just like [Evolve Your Project Metadata](./metadata-02-evolve-project-metadata.md) — where you looped back through sessions to refine your AGENTS files — you'll need to catch misses over several sessions and fix each one. The configuration gets more reliable each time.

**How it works:**

Every configuration fix gives the agent better data about how your workflow actually works. Each fix compounds — the agent gets more reliable, session after session.

The goal: you stay focused on the high-value work — planning, reviewing, making decisions. We're trying to automate away the low-value work — running tests, committing, pushing. The agent can handle all of this, but you need to reinforce the process.

The agent has tools beyond AGENTS files for this — rules, hooks, and other mechanisms that can enforce behavior more strictly. Work with your agent to identify the process failure and it'll reach for the right tool. If you want to learn more about them — ask it.

**What's next:**

1. Keep working normally. When the agent misses a procedural step, run the prompt above.
2. Expect this to take several sessions. Each fix compounds.
3. Once your core workflow — tests, commits, push — runs reliably, the babysitting drops off.

**Not yet:**

Once you can trust the agent to follow the process reliably, you can start trusting it to work more independently. That's where this is heading — but there are more pieces to put in place first.
