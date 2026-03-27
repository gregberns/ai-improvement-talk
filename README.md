# Improving Your AI Game

When using a hammer, if after using it if your thumb hurts, is it the hammers fault?

If you're frustrated by Claude's consistency... consider its the operator - not the tool. 

You can get better.

Much better, and quickly.

## Talk

[This doc contains notes from a talk](./03_talk.md) about simple steps that'll improve your experience with Claude (or whatever agent you're using). 

Those that have taken these steps, have seen a noticeable difference, within a week, in their experience. 

This isn't snake oil - there's nothing to sell. But you will be better.


## AI Motivation Low?

If you're not motivated to push hard on improving your AI skills, and you still want to be in this industry in a couple years, [read this](https://ghuntley.com/real/), maybe he can motivate you.

---

## Videos

* [fundamental skills and knowledge you must have in 2026 for SWE](https://www.youtube.com/watch?v=Jr2auYrBDA4)

---

Below are some additional things I've added

## Ralph Loop

Do this only once you have optimized (or at least improved) your 'project metadata' (AGENTS.md). This may not work as well as you'd like without updating the agents accessable metadata.

If Claude is generally performing correctly - one next step is to have it work longer without your intervention. To do that...

Become familiar with the Ralph loop...

[Read this](https://ghuntley.com/ralph/) - by the guy who coined the name, and watch his video(s) (start with [this one](https://www.youtube.com/watch?v=4Nna09dG_c0)).

The Ralph loop is what the frontier engineers are using. It may go [different names](https://factory.strongdm.ai/products/attractor), but its all the same thing in the end.

This is really quite important. You can re-use the concept too - thing of how you can use it in different contexts, manipulate it to serve different purposes.

## Context Rot though Unit Tests

Observation 1: As your context window grows, your performance will degrade.

Observation 2: Agents must compile/lint/etc then run tests - otherwise they have no feedback and produce garbage.

Observation 3: Testing frameworks produce large volumes of text output - either by default or when outputting errors.

Therefore: Running unit tests with defaults will cause performance to degrade.

But you respond "test | tail 50"!

But what if the error is above 50 from the bottom?

What can I do about this!

Ask Claude! 

Example of what Claude could see:

```
$ make ci
  [PASS]  [0/10] Shadow pytest config check (0.0s)
  [PASS]  [0.5/10] Runtime Python version check (0.0s)
  [PASS]  [1/10] Lock file check (0.0s)
  [PASS]  [2/10] SQL migration validation (1.4s)
  [PASS]  [3/10] Env var access audit (1.7s)
  [PASS]  [4/10] Pydantic deprecation check (0.2s)
  [PASS]  [5/10] Format auto-fix (1.3s)
  [PASS]  [6/10] Format check (1.0s)
  [PASS]  [7/10] Lint check (0.1s)
  [PASS]  [8/10] Type check (2.3s)
  [PASS]  [9/10] Unit tests (1m 18s)
  [PASS]  [9.5/10] Contract tests (5.9s)
  [PASS]  [9.6/10] Twin fidelity (3.9s)
  [PASS]  [10/10] Test count guardrail (7.7s)
  [PASS]  [FINAL] Diff coverage (0.4s)

  {{ERRORS HERE}}

  CI RESULT: PASS (1m 45s)
  Summary written to .ci/summary.txt
  Full logs: .ci/last-run.log
```



