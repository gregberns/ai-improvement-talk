# 014 — The Code Isn't Right (Article Skeleton)

**Status:** Skeleton aligned with the user, ready for section-by-section writing

## Arc Position

This is the first of three articles (014-016) that shift the developer's *process*. The prior two articles (005-006) gave the agent *knowledge*. Now we give it process.

**Reader's shift:** "I need to communicate differently" — mindset shift.

**The thread across 014-016:** The agent will do exactly what you set it up to do — no more. If the results aren't good enough, define the job better. The agent isn't bad at its job — you haven't defined the job clearly enough. And that's fine. This is new for everyone.

## Where 014 Starts and Stops

**Starts at:** The developer jumping from idea to implementation with no intermediate step. The gap between what's in their head and what they told the agent.

**Stops at:** Planning and communication. We don't teach verification here. We don't explain the review/validation steps in the prompt. We don't talk about encoding process. The reader learns to brief differently and review a plan. That's enough.

**Forward pointer to 015:** The plan caught the big stuff, but implementation details can still get missed. That's next.

## Section-by-Section Skeleton

### Opening (frustration energy)
- You told it exactly what to do. It did something — but not the right thing.
- The more precisely you tell it what to do, the worse it gets.
- You're writing more instructions than code at this point.
- The reader should feel seen — this is their daily experience.

### Symptom
- You give the agent instructions. It implements something — but not what you meant.
- Wrong approach, wrong patterns, missed expectations.
- You spend more time fixing than it would've taken to write it yourself.

### Why
- **Core insight: communicate the problem, not the solution.**
- You compress a rich mental model into thin instructions, drop all the context and reasoning, and expect the agent to reconstruct what was lost. It can't. Nobody could.
- When you give step-by-step instructions, the agent executes literally — doesn't ask whether your approach is right, doesn't explore alternatives, doesn't check conventions.
- Every micro-decision you didn't specify, it guesses.
- A new human developer getting "go change this function to do X" would also miss expectations — they'd just ask clarifying questions. The agent in execution mode doesn't ask. It just goes.
- The developer had ideas in their head they never communicated. Conventions they expected the agent to pick up. The agent missed expectations that were never actually stated.

### Fix
- Brief the agent like a new developer joining your team. Describe the problem — what's broken, what's needed, why it matters, where it lives. Don't dictate the solution.
- The prompt encodes the full workflow (including steps covered in later articles). Run it. It works.
- "Some concepts in the prompt will be covered in later articles. For now, they're instructions for the agent, not you." (Same pattern as 005.)

### The Prompt
- The existing prompt from v3 — encodes explore → clarify → plan → spec → review → tasks → validate → implement.
- Reader appends their problem description after the prompt.
- The prompt is the product. It has to work when run blindly.

### While it works
- Review the plan before any code gets written.
- This is where you catch misalignment — wrong approach, missed constraints, bad assumptions.
- Dramatically cheaper to correct a plan than to untangle an implementation.
- If the plan doesn't match your mental model, say so. If you don't understand why it chose an approach, ask.

### How it works
- Execution mode vs. reasoning mode. Same model, dramatically different behavior.
- When you give instructions, the agent executes. When you give context and intent, it reasons — explores the codebase, finds patterns, builds its own plan.
- The plan is in language the model understands because it wrote it. Implementation from that plan is dramatically better.
- You're not writing more — you're writing earlier. And you're writing the right thing: context about why and where, instead of incomplete instructions about what.

### Resist the urge (reinforcing pattern)
- The hardest part is not dictating the solution. You know how you'd implement it.
- Every time you dictate, you push the agent out of reasoning mode and back into execution mode.
- Give it the problem. Let it find the approach. Correct the plan if it's wrong. That's the loop.

### What's next
- Numbered steps. Start with one feature. See the difference.

### Not yet
- Forward pointer: the plan catches the big stuff. But implementation details can still get missed. That's what the next article addresses.

## Tone Notes
- Empathetic about the frustration, then blunt about the fix.
- Not accusatory — "you're a good engineer using patterns that worked for decades. They don't transfer cleanly to this new thing."
- The reader is learning. Most of us are not prepared for this shift. That just means we need to open our minds to the possibility of being wrong, be ok with that, and modify our behaviors.

## Open Questions (from v3, still live)
- "GSD mode" vs "plan/reason mode" — do we use this language or softer terms?
- Before/after example? Same task, directive style vs. context-and-intent style?
- "New developer" analogy — lean into it or keep it light?

## Sources
- v3.md in this folder (the rich idea file)
- articles/014-code-isnt-right.md (agent-produced draft — guidance only, not the starting point)
