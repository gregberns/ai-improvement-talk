# 015 — It Missed Things (Article Skeleton)

**Status:** Skeleton aligned with the user, ready for section-by-section writing after 014

## Arc Position

Second of three articles (014-016) shifting the developer's process.

**Reader's shift:** "I need to verify, not just trust" — practice shift.

**The thread:** The agent will do exactly what you set it up to do — no more. If you don't set up verification, it won't verify.

## Where 015 Starts and Stops

**Starts at:** The reader has adopted 014's approach. They have a plan. The agent implemented it. But things got dropped — details, edge cases, conventions. Not the big stuff. The small stuff that adds up.

**Stops at:** Verification of implementation work. We don't talk about procedural/pipeline steps (that's 016). We don't talk about encoding process into configuration.

**Callback to 014:** "Remember the prompt from last article? There were review and validation steps baked in. Here's why those matter and how to make them actually catch things."

**Forward pointer to 016:** You're verifying the creative work (planning, implementation). But what about the procedural stuff? Git workflows, tests, push. That's next.

## Section-by-Section Skeleton

### Opening (deflation energy — not frustration)
- You had a plan. It was good. The agent implemented it. But things got dropped.
- You thought you were past the "fixing the agent's work" phase. You're not.
- Not anger — more like: "I thought we solved this."

### Symptom
- The plan was solid. The implementation missed things.
- Not the big stuff — the details. A convention wasn't followed. An edge case was skipped. A step from the plan didn't make it into the code.
- You're still reviewing everything line by line.

### Why
- Humans miss things. That's why we have code review, tests, QA.
- We don't trust ourselves to get everything right in one pass — we build checks.
- You're trusting the agent to get everything right in one pass. Why?
- Same principle, new context: build verification in.

### Fix
- The prompt/practice for systematic self-review.
- At each stage — plan, implementation, completion — the agent verifies against what was specified.
- Not "does this code work" but "does this code match the plan."
- The first step is NOT to read the code yourself. Leverage the AI to do the review.
- Simple, powerful: point the agent at the plan, make it do the comparison.

### While it works
- Watch what it catches. Some will be genuine misses. Some will be convention violations the plan didn't cover.
- Both are valuable signal.

### How it works
- Verification at each step catches small issues before they compound.
- A missed detail in the plan is a one-line fix. A missed detail in implementation is a debugging session. A missed detail that makes it to "done" is your afternoon.
- Written plan = checklist the agent can verify against. Self-review catches gaps before you find them manually.

### Two failure modes after review (from v2)
- **Mode 1:** The change WAS in the plan but wasn't implemented. Agent forgot. Point it at the gap.
- **Mode 2:** The change was NOT in the plan — should have been captured but wasn't. Different problem. Acknowledge it exists, point reader back toward improving their planning.
- Don't try to solve mode 2 fully here.

### What's next
- Numbered steps.

### Not yet
- Forward pointer: you're verifying the creative work. But procedural steps — git, tests, push — are a different category. That's next.

## Tone Notes
- Less frustration than 014, more "I thought I had this solved."
- The insight is quieter: "of course you'd verify — you already do this for human work."
- Frame it as extending a practice they already believe in, not learning something new.

## Open Questions (from v2, still live)
- Do we hint that later they'll use SEPARATE agents for review?
- How do we frame "the agent forgot" without undermining confidence in the tool?
- Does 015 need its own prompt, or is it more of a practice/habit article?

## Sources
- v2.md in this folder
- Informed by talk section 9 (implement with loops)
