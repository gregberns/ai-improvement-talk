---
title: "Be the Orchestrator"
group: context
order: 1
idea: "007"
status: draft
---

# Context: Be the Orchestrator

*This is a series about moving your coding agent from intern to senior developer. It's for devs who are already using agents but not getting the results they keep hearing about.*

*Each article targets a specific problem. What you're experiencing, why it's happening, and what to do about it — with a prompt you can run immediately.*

*The articles build on each other. If you haven't gone through the previous articles, consider starting [at the beginning](./index.md).*

---

In the previous articles we set up the agent's knowledge and shifted your process. Now we're moving to context itself. What lives in your context window — and for how long — shapes everything downstream. The next few articles are about keeping it useful.

---

Your agent is changing files, reading files, making tool calls, and outputting responses. That's fine, right?

You have a problem and you don't know it. You're diluting your context and burning tokens.

But it's an easy solve.

**Symptom:**

Your main thread is doing everything. Research, planning, edits, tool calls, status messages — all in the same thread.

**Why:**

Everything you see on your screen — and more — is getting stored in context. Every file read, every grep, every bit of investigation. Even the quick detour "just to check something" — that stays too.

The more you pile in, the faster the window grows, the more your token usage climbs, and the faster quality degrades. The model reasons over the whole pile on every turn. And the whole pile gets re-sent on every turn.

**Fix:**

You need to delegate as many tasks to sub-agents as possible. Simple change — when you're about to do research, for example, add this to the end of your prompt:

> You are the orchestrator, use sub-agents, delegate your work.

Research and reviews especially — delegate that work.

When you have several tasks to do, delegate each one:

> Spawn three sub-agents in parallel to do those tasks.

**Next step:** Install oh-my-claudecode. Do it. Now. Don't worry about alternatives. You need an agent framework and you need to start using one. It ships with a bunch of stuff built in to make sub-agent delegation easier.

**How it works:**

A sub-agent is a separate context window with its own job. You hand it a task — "research how auth works in this codebase," "run the tests and fix what broke," "verify these edits match the plan" — and it goes off, does the work, and returns a summary. Whatever it read, searched, or explored to produce that summary stays in *its* context window. Not yours.

That's the whole move.

You want your main context as clean as possible for coordination. That's where the conversation happens, understanding builds, decisions get made, plans get constructed. You'll get much better performance with less noise in the way.

In earlier articles, we triggered the planning to start in reasoning mode. The first step of planning is research. And research is messy — exploratory, full of dead ends and tangents. You don't want that in your main context window.

The research agent goes off. Makes a bunch of tool calls. Reads files. Comes back with a summary that lands in the main agent's thread. Nice clean summary, without all the clutter.

That's the shift. The model working in your main thread reasons over just what matters. You pay for just what matters. Sessions stay useful for hours instead of degrading as research piles up.

**Side benefit:** sub-agents run in parallel. Three tasks, three sub-agents, all moving at once. More done per hour, main thread never blocked waiting.

**What's next:**

Delegation buys you time. But sessions still crash and burn — and you'll need new ones.

Next: how to spot a session that's gone south and kill it cleanly.

After that: techniques for restarting sessions regularly without losing your place.

**Not yet:**

Notice we didn't talk about making code changes? Should they be made in the main loop or in a sub-agent? We'll get to that later.
