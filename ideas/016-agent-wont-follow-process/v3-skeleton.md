# 016 — The Agent Won't Follow the Process (Article Skeleton)

**Status:** Skeleton aligned with the user, ready for section-by-section writing after 015

## Arc Position

Third of three articles (014-016) shifting the developer's process.

**Reader's shift:** "I need to encode, not just expect" — system shift.

**The thread:** The agent will do exactly what you set it up to do — no more. If it's not encoded, it's optional. If it's optional, it gets skipped.

## Where 016 Starts and Stops

**Starts at:** The reader's creative work is better — planning and verification are working. But the agent skips procedural steps. Doesn't run tests. Doesn't push commits. Doesn't follow the git workflow. Says "done" when it isn't.

**Stops at:** Encoding procedural steps. We don't get into full automation, orchestration, or advanced workflow design.

**Forward pointer:** Once you can trust the agent to follow the process reliably, you can start trusting it to work more independently. Seeds the automation/reliability articles later.

## Section-by-Section Skeleton

### Opening (mild exasperation — "two steps forward, one step back")
- The code is good now. Planning works. Verification catches the gaps.
- But the agent said it was done and didn't push. Or didn't run tests. Or left the branch in a weird state.
- It's like two steps forward and one step back. You thought you had it solved — but it won't do the small stuff. So again, more babysitting.
- The creative work is better. The procedural stuff is unreliable.

### Symptom
- The agent does the implementation work well but skips procedural steps.
- Doesn't run tests. Doesn't push commits. Doesn't follow the git workflow. Says "done" when it isn't.
- You have to babysit the last mile.

### Why
- Procedural steps aren't encoded anywhere. They're in your head, or mentioned once in a conversation and forgotten.
- Verbal instructions in a conversation are ephemeral. As context grows, earlier instructions lose influence.
- The agent isn't being disobedient. It's operating without persistent process definitions.
- You wouldn't expect a new hire to remember every verbal instruction from their first week — you'd put it in the onboarding docs.
- If it's not encoded, it's optional. If it's optional, it gets skipped.

### Fix
- Have a conversation with the agent after the problem happens. Prompt: describe the process failure, ask the agent to diagnose why and fix its own configuration.
- You're not learning hooks and rules syntax. You're putting on your engineering hat and asking the agent "how do we solve this." Make THAT the habit.
- The agent figures out the mechanism — AGENTS.md update, hook, rule, whatever. The point is: you identified a process failure and asked the agent to fix the underlying configuration.
- Same collaborative pattern from 014 applied to configuration: don't dictate the fix, describe the problem.

### How it works
- When process is embedded in agent configuration, it's loaded at the start of every interaction. Doesn't compete with conversation context. Doesn't get forgotten. Doesn't degrade over long sessions.
- You're moving from "telling the agent what to do" to "engineering the system the agent operates in."
- That's what you do as an engineer — you build reliable systems. Your agent configuration IS a system. Treat it like one.

### Reinforcing pattern
- Every time you catch the agent skipping a step: don't just tell it again. Fix the configuration.
- This is the same evolve-metadata practice from 006, but applied to process, not conventions.
- Think of it like engineering: if a system fails intermittently, you don't just restart it. You find the root cause and fix the system.

### Critical warning (from v2)
- If you do not reinforce this now, you WILL have problems downstream. Later articles assume actions occur consistently. Skip this and underlying process issues will plague your workflows.

### What's next
- Numbered steps.

### Not yet / Forward pointer
- Once you can trust the agent to follow the process reliably, you can start trusting it to work more independently.
- Seeds automation and advanced workflow articles.

## Tone Notes
- Not frustrated anymore — more like "of course this is the next thing."
- Two steps forward, one step back. But the fix is straightforward.
- Engineering mindset: this is a system reliability problem, and you know how to solve those.

## Open Questions (from v2, still live)
- Do we give example outputs of what the agent might suggest (hook, rule, AGENTS update)?
- How do we handle tool differences? Claude Code vs Codex etc. The "ask the agent how to solve it" approach sidesteps this.
- Do we explicitly say "this is like 006 but for process" or let them make the connection?

## Sources
- v2.md in this folder
- Informed by talk sections 3-4 (project metadata, encoding)
