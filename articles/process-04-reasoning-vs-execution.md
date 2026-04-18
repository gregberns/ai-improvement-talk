---
title: "Reasoning vs Execution"
group: process
order: 4
idea: "017"
status: draft
---

# Process: Reasoning vs Execution

*This is a series about moving your coding agent from intern to senior developer. It's for devs who are already using agents but not getting the results they keep hearing about.*

*Each article targets a specific problem. What you're experiencing, why it's happening, and what to do about it.*

*The articles build on each other. If you haven't gone through the previous articles, consider starting [at the beginning](./index.md).*

---

In the past several articles, we dove into building processes for agent consistency: planning gives the agent's execution structure, review finds gaps, rules provide guardrails.

Now we'll dive deeper into a topic we touched on in [The Code Isn't Right](./process-01-code-isnt-right.md): Reasoning and Execution modes.

---

Agents have two opposing modes — execution and reasoning. Same with you.

Pat your head. Now rub your belly. Now both at once. See?

Asking an agent to solve it and build it at the same time makes it good at neither.

**The two modes:**

Reasoning is for thinking: the agent reads, investigates, asks, plans — slow.

Execution is for doing: tool calls, file writes, instruction following — fast.

Your prompt's language dictates the mode. Wrong mode, wrong outcome.

**Splitting the prompt:**

Take [The Code Isn't Right](./process-01-code-isnt-right.md)'s prompt — "Add a new REST endpoint..." It's a command. Straight to execution.

Let's split it:

1. Figure out how we'd implement this endpoint.
2. Now implement the plan.

Part one fires reasoning. Part two fires execution. Two prompts, two modes — same intent, different outcomes.

**Your own process:**

You already do this. Every time a task lands, your brain starts working before your hands do. You picture the relevant part of the codebase. You remember how you solved something similar. You anticipate what could break.

On a small task, that takes seconds. On a big one, it can take days — whiteboarding, reading old PRs, arguing with a teammate.

You think before you build. Every time.

Your agent needs to do the same. Without planning, there's no reasoning. Without reasoning, you're missing the model's real power.

**Plan, then execute:**

Plan first. Then execute. Two phases separated by a pause, each triggered by a different kind of prompt.

Any real work needs a plan. Even small changes benefit: "What would you change to modify this function?"

Start defaulting to the split. Build the habit.

**Trigger reasoning:**

Here's how. Start talking to the agent like a teammate, not a micromanager. "Think through this problem." "Help me understand." "How should we approach this?" "Let's plan this out." There's plenty of styles — find yours.

You'll know reasoning fired when you see "Thinking..." or a long pause before output.

Execution is the default — commands fire instantly. You already do this. Reasoning's the one you practice to fire deliberately.

**Why this matters:**

Triggering reasoning is a major pillar of this series.

Once you can put the agent in the right mode at the right time, small reliable steps stack into reliable processes. Errors caught earlier. Less babysitting. Results you can trust.

We're building a development lifecycle. Each step needs a distinct mode — we need both, at different times. You'll learn to flip between them consistently.

**One last thing:**

As you build this habit, watch for when you slip back into micromanaging.

When a session goes south, do you give more commands? When you're yelling at your agent, how did you form your last three prompts? Can you get it back into reasoning mode? Can you drop the frustration and change your frame of reference?

This is a learning process. Good luck.
