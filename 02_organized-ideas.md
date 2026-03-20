# Presentation - Organized Ideas & Groupings

## Reference Frameworks
- Our Pyramid (from notes Entry 2)
- Dan Shapiro's Five Levels: https://www.danshapiro.com/blog/2026/01/the-five-levels-from-spicy-autocomplete-to-the-software-factory/
- Yegge's Developer Agent Evolution Model: https://justin.abrah.ms/blog/2026-01-08-yegge-s-developer-agent-evolution-model.html
- Xexr gt-toolkit (reliable specs example): https://github.com/Xexr/gt-toolkit/blob/main/formulas/README.md
- oh-my-claudecode (agent framework): https://github.com/yeachan-heo/oh-my-claudecode

---

## Section 1: Opening - The Transition

### Set up the problem
- The job is fundamentally changing. This is a long transition. Transitions are painful. Change is hard - can be fun, but disrupting fundamental beliefs is difficult and takes time.
- What's shifting: the job you loved - spending time refining and building a beautiful system - is changing underneath you.
- We've been promised "These things are amazing" - but really they kinda produce sub-par results when working with them over days and weeks.
- Working with AI today feels like working with a poorly performing mid-dev. It does a bunch of stuff, and more often than not makes a mess of things.

### Quotes
- Eng #2: "To quote a programmer friend, 'I'm having a real hard time letting go.'"
- Eng #3: "hm, (if/)when I do start to use AI I'll have to try that approach"
- (Eng #1 quotes used later in the talk)

### The turn
- I'd like you to consider the idea that it's not the model/tools that are sub-par - it's the way we're using them.
- (IMAGE IDEA: pounding a screw in with a hammer)
- You CAN work with senior and staff level AI agents/engineers. But they don't come out of the box. Without tuning, you won't see that level of performance. You need to learn how to evoke that from the models, agents, tools.

### Framing for the rest of the talk
- Pain points correspond to the 'level' you are operating at. You need to be ok with the level you are at. Everyone is at a different point. Focus on where you are and how you can refine your process.
- Structure: you have this symptom/pain point? Here's a possible solution to start experimenting with.
- Don't limit yourself to "spot fixes"/small tweaks. Use these as a way to examine your 'engineering process architecture'. You are a system - understand how you - the system - works today, then use your eng skills to improve those processes. Meta-shit.

## Section 2: The Foundation - Stop Experimenting
- Problem: "Tokens are expensive / I want something cheaper / I like OSS"
- Stop model-hopping. Pick one. Claude Opus, HIGH Effort. Tune it in.
- You are trying to build a Formula 1 race car. Do not stick in a lawn mower engine. Do not use a semi-truck transmission.
- DO NOT CONCERN YOURSELF WITH TOKENS. You do not think in tokens any more. NEVER AGAIN.

## Section 3: Set Up Your Project Metadata

### Your Problem
- "It's not following my project's conventions! Every time it's missing things! What is the problem!"
- Symptom: you're yelling at the agent because it didn't follow your conventions again

### Claude's Problem
- Its context isn't getting loaded with critical information about your conventions.

### Solution
- Claude has 'magic triggers' to load context. You need to set it up for success.
- In code you put guardrails. You need to be encoding your conventions in "Project Metadata".
- THIS IS YOUR JOB AS AN ENGINEER! You put guardrails on your programs - WHY NOT YOUR CODING AGENTS!
- Term: "Project Metadata" = all encoded patterns and practices (rules, AGENTS.md, CLAUDE.md, hooks, commands)
- Root AGENTS/CLAUDE should be 100-150 lines. No more.

### Action
- Start new Claude session: "I need you to do extensive research into how to best set up this large project to work well so Claude Code can work effectively and follow its conventions."
- Tell it what you're struggling with!
- Review what it generates. Ask "What is a command?", "Why are there CLAUDE files several folders deep?"

### Output
- More 'project metadata' - hooks, AGENTS/CLAUDE files, etc.

### Results you should see
- When changing code - Claude will have context automatically injected - resulting in generally better performance
- Consistency across sessions should improve a bit

## Section 4: Evolving Your Project Metadata

### This is a "tune the engine" step - not a problem/solution, it's an ongoing practice.

### The Process
- Tuesday you build out the project metadata (Section 3).
- Wednesday, after every task (between 50-75% of context), tell Claude:
  - "We're working to improve our CLAUDE/AGENTS files, rules, etc, so we can have better sessions. Please look through the last conversation and think about what improvements we could make? Were there missteps? Were there successes? How can we encode the successes so they happen next session? How can we avoid issues next session? Make sure to generalize - don't overfit the issues/improvements."
- Spend the day doing this - meaning spend 10 minutes for every hour you code.

### Example: The Git Process
- You've built a feature. You tell Claude to commit it. Then you have to tell it to push. Then create a PR. Oh you need a fix. Now you have to tell it all those steps again. Oh and it needs to merge/rebase origin main...
- You shouldn't need to tell it this every time.
- Ask it: "Think about the git process we just went through - how can we prevent me giving you these steps every time? How can we make next session go more smoothly?"

### Key principles
- Generalize the ideas - don't over fit! (Claude tends to take exact words and spit them back)
- Build abstractions from specific learnings
- Save them into project metadata in various ways

## Section 5: Use Sub Agents - Be The Orchestrator

### Symptom
- Is your "main thread" doing all the work? Research, reading files, making code changes, committing?
- You have a problem and you don't know it! You're burning your context.
- Another symptom: How often do you compact? Can you get a large feature complete in one context?

### Solution
- Use SubAgents as much as possible!

### Actions
- When starting a feature, tell Claude: "You are the orchestrator, use subagents, delegate your work."
- Install oh-my-claudecode. Do it. Now. Don't worry about alternatives. You need an agent framework and you need to start using one.

### Outcomes
- Sessions will last much longer
- Agent will remain focused
- Sessions will feel more consistent

## Section 6: Abysmal Sessions

### Problem
- "Why is this session so bad!"

### Action
- STOP! Do not proceed. Kill the session. End it. Now.
- Once a session has gone south it is very difficult to recover.
- Tell Claude to summarize what you were working on. Copy. Start new session. (Run clear command)

## Section 7: Session Continuity

### If you MUST continue a session
- Idea: Create two uncommitted files: STATUS.md + TASKS.md. Before compaction, tell it to update those files. They track where you're at and will survive compaction.
- (Hint: implement a hook or command to do this)
- At 10% before compaction: stop, save state, write compaction summary, copy, clear, paste and go.

### BUT
- Features that take more than one thread = ANTI-PATTERN
- You need to use SubAgents
- You need to design - then implement with a new session

## Section 8: Write Specs - Become The Architect

### Problem
- "I tell Claude in detail what I want, it goes and does it, and I really don't like the results"

### Answer: Specs.

### "But that's boring - I don't like writing all that!"
- Don't! Brain dump, then iterate with Claude to refine the ideas.
- Act as the Architect! Have Claude help you think through the problem. Dig into the details.

### Action
- DO IT!
- Start simple. Write a single file. Clear session and implement. You should see improvement.
- Disable Claude Plan Mode (ask Claude how) - you need to actively iterate on the plan
- Write spec iteratively, WRITE TO DISK, clear/compact, then implement.

### Warning
- If you do this, you may see more success out of this than any other step.
- (Caveat: to make it really good, you need Ralph)

### Why
- Specs force deep thinking about HOW code will be written.
- Forces research.
- The spec can have code snippets to enforce coding conventions.
- In the spec process: make it write code samples. If they don't follow convention, ask what's missing from the project metadata.

### Iteration - The Full Spec Process
1. Problem Space (Brain Dump)
2. Decompose & Requirements (high and low level ideas)
3. Research (Claude researches your ideas)
4. Nit Pick the Details Loop (section by section)
5. SPEC! (Claude formalizes into a doc)
6. Implement (using a ralph loop)
7. Review (architect, critic, QA agents)
8. Spec Review (architects validate the spec)

## Section 9: Implement With Loops - Don't Just Fire And Forget

### Problem 1: Agent doesn't implement the spec
- Solution: Ralph Loop - implement a little, check, write more, check, loop - until plan resembles spec

### Problem 2: Spec actually has issues
- Solution: Cross Reference/Forward-Backward on specs - review techniques
- There may be gaps in your spec - that's ok, review surfaces them

## Section 10: Encode Your Workflows
- Mindset shift: Stop thinking about what you like/don't like. Think about ENCODING your process.
- You've spent YEARS tuning your workflow. It works. Formalize it, encode it, write it down.
- Start by creating a command - good way to get your feet wet
- "We're going to write this feature AND encode the process I use, so we can replicate it next time"
- Why not off the shelf? If you don't know how it works and you aren't using it now, installing it won't help.

## Section 11: The Illustration - The Pyramid
- Base: Excellent model (stop experimenting)
- Level 2: Coding agent
- Level 3: Tuned-in coding agent (rules, hooks, CLAUDE.md + AGENT.md files - PLURAL)
- Level 4: Encoding Your Workflows (more practices into rules and CLAUDE.md)
- Level 5: Using Sub Agents
- Level 6: Write Specs
- Level 7: Refine Specs + Refine Post-Implement

## Conversation Examples To Include
- Kuba: "I work in a loop, ..." (REMINDER: grab that conversation) - illustration of hand-holding vs encoding
- Meta: this presentation itself was built using the braindump → organize → refine process

## Open Questions
- Pyramid vs Yegge levels vs Shapiro levels - how to reconcile/reference?
- Where does the pyramid illustration best fit - early framing or closing summary?
- Spec Review vs Code Review ordering - which first?
- Git hook example - where does it best fit in the flow?
