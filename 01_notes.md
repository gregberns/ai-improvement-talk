# Presentation Notes - Append-Only Log

## Entry 1 - Initial Brain Dump

### Audience
- Good developers struggling with the AI transition
- Two core pain points:
  1. AI is threatening/changing their primary job
  2. AI doesn't consistently do what they want - doesn't follow best practices, isn't reliable
- Their experience: sometimes it's magic, most of the time you're cleaning up after it, sometimes it's a dumpster fire

### Structure Idea
- Open with acknowledgment: "You're not alone" - include quotes from real devs who are struggling
- Core framework: "Are you struggling with X? That's Level 2. Here's the one or two things you're probably NOT doing that are critical to your success."
- Pattern: "You're here, but you're not doing X and it's hampering you. Do Y next, consistently, and you'll see significantly better results."
- Leveling-up staircase - each level has a specific unlock

### Format
- Simple: Title, Bullets, Title, Bullets
- Each title = a new slide/section
- Minimal text, well-illustrated ideas

### Process
1. Brain dump ideas into notes (this file)
2. Capture major sections (separate doc TBD)
3. Refine ideas - collaborative clarification
4. Structure and polish into final presentation

---

## Entry 2 - Core Ideas Brain Dump (The Meat)

### Problem: "Tokens are expensive / I want something cheaper / I like OSS"
- SOLUTION: Stop experimenting with models. Turn on Claude Opus HIGH Effort. Do not use any other models. Only use Claude Code and tune it in.

### Problem: "In one workflow Claude is great, in the next it's total shit"
- SOLUTION Part 1: Get your agents/claude.md files, .claude commands, agents, hooks, rules, etc situated. This is done in one big first pass. Use Claude to research and do the major work.
  - We might want to do a brief overview of what each of these things is for
  - Use this process to have Claude teach you about the tools and what they're for
- SOLUTION Part 2: Restart your session. Just kill it. Don't try and recover. It's futile.

### Practice: Analyze Good Conversations
- For one day, you'll have a good conversation, and before you move on, ask Claude to analyze the conversation for places you weren't aligned
- Then think very hard about how to generalize the ideas
- Discuss the ideas
- Then save them in various ways

### Mindset Shift: Stop thinking about what you like/don't like. Think about ENCODING your process.
- Do you have a workflow you really like to operate in? Start by creating a command.
- Use a command - just because it's a good way to get your feet wet.
- Say: "We're going to write this feature. At the same time, we're going to encode the process I use in a command. I want to be able to go through this same process every time. Help me work through this problem and at the same time we'll encode the steps and my thinking process, so we can replicate this next time."
- Why not use something off the shelf?? Because if you don't know how it works/what it does, and you aren't using them now, then installing them isn't going to help.

### Prerequisite: Install oh-my-claudecode. Period.
- If you don't have an 'agent framework' - you need one, and you need to start using one.

### Problem: "I tell Claude in detail what I want, it goes and does it, and I really don't like the results"
- SOLUTION: Write Specs.
- This sounds boring as hell. Have you ever dreamed of being "An Architect!"? Well for half an hour, step away from coding, become that Architect you always wanted to be.
- WAIT - don't write it by hand! Claude is really good! There's a process:
  1. **Problem Space** (read: Brain Dump!)
  2. **Decompose & Requirements** (high level and low level ideas on what you're putting together)
  3. **Research** (Claude takes your ideas and researches them)
  4. **Nit Pick the Details Loop** (take a section at a time and nit pick what Claude came up with)
  5. **SPEC!** (Claude takes everything you've designed and formalizes it into a doc)
  6. **Implement** (tell Claude to implement - using a ralph loop)
  7. **YOU'RE NOT DONE - Review** (Send several code agents: architect, critic, and QA - these are from oh-my-claudecode)
  8. **STILL NOT DONE - SPEC REVIEW!** (send at least one or two architects to validate the spec) (This can also be swapped with the Code Review - not sure what's best)
- **DO NOT CONCERN YOURSELF WITH TOKENS!!!!!!!!! You do not think in tokens any more. NEVER AGAIN!**

### Problem: "I'm writing specs, I've got a detailed plan, and it doesn't implement it all!"
- SOLUTION: Use Ralph Loop. Think: implement a little, check what was implemented, write some more, check impl, loop - until the plan resembles the spec.
- There may be gaps in your spec!!

### Illustration: The Pyramid
- Base: Excellent model
- Level 2: Coding agent
- Level 3: Tuned-in coding agent - rules, hooks (maybe for git - might need to move), CLAUDE.md + AGENT.md fileS (PLURAL)
  - **THIS IS YOUR JOB AS AN ENGINEER! You put guardrails on your programs - WHY NOT YOUR CODING AGENTS!!!!!!!!!**
- Level 4: Encoding Your Workflows (encoding MORE practices into rules and CLAUDE.md files)
- Level 5: Using Sub Agents
- Level 6: Write Specs
- Level 7: Refine Specs + Refine Post-Implement

### Key Message
- You as an engineer have spent YEARS tuning your workflow. It works well. Spend time with Claude to formalize it, encode it, write it down.

### Conversation Example: Kuba
- "I work in a loop, ..." (REMINDER: grab that conversation)
- Use as illustration of trying to hand-hold the model
- Should instead: fine tune rules in .claude, then next step is writing specs

### References to Include
- Dan Shapiro: "The Five Levels from Spicy Autocomplete to the Software Factory" - https://www.danshapiro.com/blog/2026/01/the-five-levels-from-spicy-autocomplete-to-the-software-factory/
- Xexr gt-toolkit formulas (extremely reliable specs example) - https://github.com/Xexr/gt-toolkit/blob/main/formulas/README.md

---

## Entry 3 - Handwritten Notes Brain Dump

### Sub Agents - Use Them Constantly
- You should be working as the orchestrator. You need to be delegating all your work to sub agents.
- You need to actively be using subagents - constantly. It is actually feasible to go for many hours this way in a single thread!

### Session Hygiene
- If a conversation goes south, have it summarize the conversation or write it out and use the clear command. Stop wasting time in a bad session.
- Convos/features that take more than one thread - ANTI-PATTERN
- Stop using Claude Plan Mode - build your own. Write a spec in an iterative fashion, WRITE TO DISK!, then clear your session/compact - then implement.

### Root AGENTS/CLAUDE Size
- Root AGENTS/CLAUDE should be 100-150 lines. No more.

### Continual Agent Improvement Program
- Start by just spending the day - have a short good discussion, have Claude extract learnings.

### Git Process
- Does the agent not always do all the steps? Encode into a rule.

### Problem: "Working with Claude and there are just failures or inconsistent results"
- Claude won't consistently follow project conventions
  - Encode in project metadata
  - Specs - have Claude REALLY dig deep into how the code is going to be written
  - Idea: in the spec process make it write code samples - if they don't follow convention - ask what is missing? What needs to be added to the project metadata?

### Problem: "I told it what to build, it went off and built stuff which was shit! Spent the rest of the day cleaning it up."
- (Connects to: Write Specs solution from Entry 2)

### Problem: "Had a great day/session with Claude, and now it's terrible"
- (Connects to: Analyze Good Conversations, encoding learnings, session hygiene)

### Generalizing Learnings
- Ask Claude to generalize, build abstractions, "don't over fit!"
- There's a tendency for it to take the exact words you use - which will then be spit out later
- Use generalization when asking it to improve the "project metadata"

### Small Technique: Pre-Compaction Saves
- Set up a thing (probably hook) to fire before compaction to create a TASKS.md and STATUS.md files which contain what you're working on and its status
- Another idea: when you're at 10% before compaction - stop everything. Tell it to save to TASKS and STATUS and write a compaction summary. Copy the summary, clear command, and paste and go.

### Term: "Project Metadata"
- All the encoded patterns and practices embedded in the project through rules, AGENTS, etc.
- (Coined term - use throughout presentation)

---

## Entry 4 - Final Brain Dump + Meta Note

### Meta: This Process Is An Example
- While writing this post - told Claude to take braindump, create an append only file, write all ideas to it. Then in another file, take those notes, group and refine - and finally compress into something useful.
- EXPERIMENT! (Worth mentioning in the presentation as a real-time example of the process)

### Reference: Yegge's Developer Agent Evolution Model
- Source: https://justin.abrah.ms/blog/2026-01-08-yegge-s-developer-agent-evolution-model.html
- Our "Problems" should map into these levels somehow
- Levels:
  - Stage 1: Zero or Near-Zero AI - maybe code completions, sometimes ask Chat questions
  - Stage 2: Coding agent in IDE, permissions turned on. Narrow coding agent in sidebar asks permission to run tools.
  - Stage 3: Agent in IDE, YOLO mode - Trust goes up. Turn off permissions, agent gets wider.
  - Stage 4: In IDE, wide agent - Agent gradually grows to fill the screen. Code is just for diffs.
  - Stage 5: CLI, single agent. YOLO. Diffs scroll by. You may or may not look at them.
  - Stage 6: CLI, multi-agent, YOLO. Regularly use 3-5 parallel instances. Very fast.
  - Stage 7: 10+ agents, hand-managed. Pushing limits of hand-management.
  - Stage 8: Building your own orchestrator. On the frontier, automating your workflow.

---

## Entry 5 - oh-my-claudecode Reference

### Tool: oh-my-claudecode
- GitHub: https://github.com/yeachan-heo/oh-my-claudecode
- This is the agent framework mentioned throughout - the set of agents that help
- Provides: architect, critic, QA, ralph loop, ultrawork, sub-agent orchestration, and more
- Referenced in: spec review process (Section 8), sub agents (Section 7), install recommendation (Section 7)

---

## Entry 6 - Section 1 Refinement Notes + Quotes

### Engineer Quotes (raw)

Eng #1:
> "I do not write any of my code, but I micromanage the shit out of claude."
> "I do not use any skills, built-in planner, mcps or any other fancy features they keep adding."
> "I have a living document PLAN.md with a checklist for everything I do."
> "I find my approach maximizes the code quality and familiarity and minimizes tokens used, but sacrifices everything else. Can't do this while sleeping lol."
- NOTE: Use later in presentation, NOT in intro.

Eng #2:
> "I'm essentially still pair programming with Claude, Codex, etc, going over things function by function or file by file. I review its code, it reviews mine. In my gut I know if we're not yet at the point where this level of automated programming is viable it soon will be, but I'm having a hard time emotionally taking that step."
> "To quote a programmer friend, 'I'm having a real hard time letting go.'"
- NOTE: Use last line in intro: "I'm having a real hard time letting go."

Eng #3:
> "hm, (if/)when I do start to use AI I'll have to try that approach, I like to get a good feel for the problem by trying to implement the solution then refine things"
- NOTE: Use first part in intro: "hm, (if/)when I do start to use AI I'll have to try that approach"

### Corrections to Section 1 Framing

- NOT "lost" — it's a long, painful transition. Disrupting fundamental beliefs is difficult and takes time.
- NOT "fear of AI replacing their job" — it's losing the job they LIKED: spending time refining and building a beautiful system.
- NOT "AI not working well" — it's that AI behaves like a poorly performing mid-dev. Does a bunch of stuff, more often than not makes a mess.
- Be VERY precise about framing concerns. These engineers don't have the concerns media portrays. If we say "You're worried about X" and it's wrong, they'll tune out.

### Section 1 Flow (refined)

1. Set up the problem: a challenge with the transition. The job is fundamentally changing.
2. We've been promised "These things are amazing" - but really they kinda produce sub-par results when working with them over days and weeks.
3. Transition to: "But could it be us that are using them wrong?"
4. Suggest: we CAN be working with Staff level AI agents/engineers. But we need to learn how to evoke that from the models, agents, tools. They don't come out of the box.
5. Talk through pain points which correspond to the 'level' you are operating at. "You need to be ok with the level you are at. Everyone is at a different point. Focus on where you are and how you can refine your process."
6. Summary of what we'll review:
   - Structure: you have this symptom/pain point? Here's a possible solution to start experimenting with.
   - Don't limit yourself to "spot fixes"/small tweaks. Use these as a way to examine your 'engineering process architecture'. You are a system - understand how you - the system - works today, then use your eng skills to improve those processes. Meta-shit.

### Objective of the Talk
- Show devs they can work with senior and staff level AI agents/engineers
- They don't come out of the box, and without tuning you won't see that level of performance
- Pattern: "Your knee hurts - do this to make it stop hurting. Now you can run a little faster."
- Point out struggles → provide a tool that relieves them → give a PATH or next step → build confidence
- Show HOW to change, how to evolve. Not only techniques, but ways to think: "Encode your thinking and process into your tools."

---

## Entry 7 - Section 3 Reframe + Reordering

### Section 3 reframed
- Old framing: "In one workflow Claude is great, in the next it's total shit" — too similar to Section 5 (Continual Improvement)
- New framing: "It's not following my project's conventions! Every time it's missing things!"
- Root cause: Claude's context isn't getting loaded with critical info about conventions
- Solution: Claude has 'magic triggers' to load context. Set it up for success.
- Action: Start new session, tell Claude to research how to set up project for Claude Code, tell it what you're struggling with, review and ask questions
- WHY: In code you put guardrails. Do that here too.

### Reordering (Sections 3-5)
- Section 3: Set Up Your Project Metadata (first pass setup)
- Section 4: Evolving Your Project Metadata (continual improvement, was Section 5)
- Section 5: Encode Your Workflows (was Section 4)
- Git process example moved from Section 3 to Section 4

### Image idea from Section 1
- "Pounding a screw in with a hammer" for the "it's not the tools, it's how we're using them" turn

---

## Entry 8 - Refinement Pass Details (Sections 5-10)

### Section 5 (Sub Agents) refinements
- Added symptoms: main thread doing all the work, burning context, how often do you compact?
- Added outcomes: longer sessions, focused agent, more consistent sessions
- Structured as Symptom/Solution/Actions/Outcomes

### Section 6 (Abysmal Sessions) - split from old "Session Hygiene"
- Focused: just kill the session. Summarize, copy, clear, new session.

### Section 7 (Session Continuity) - split from old "Session Hygiene"
- STATUS.md + TASKS.md as uncommitted files that survive compaction
- Hint: implement as hook or command
- At 10% before compaction: stop, save state, write summary, copy, clear, paste and go
- Features spanning multiple threads = ANTI-PATTERN

### Section 8 (Write Specs) refinements
- Reframed: "But that's boring!" → "Don't write it all! Brain dump, iterate with Claude."
- Added: Start simple - single file, clear, implement
- Added: Disable Claude Plan Mode - actively iterate on spec
- Added: Write spec iteratively, WRITE TO DISK, clear/compact, then implement
- Warning: may see more success from this than any other step (caveat: needs Ralph for full power)
- Why: forces deep thinking, forces research, code snippets enforce conventions

### Section 9 (Implement With Loops) refinement
- Split into two problems:
  1. Agent doesn't implement the spec → Ralph Loop
  2. Spec actually has issues → Cross Reference/Forward-Backward review techniques

### Section 10 (Encode Your Workflows) - moved from old Section 5 position
- This is the "meta" step - think about your thinking
- Moved later because it requires more maturity in the process

### Reordering done during this pass
- Old Section 5 (Encode Workflows) moved to Section 10
- Old Session Hygiene split into Section 6 (Abysmal Sessions) + Section 7 (Session Continuity)
- "Stop using Claude Plan Mode" moved from Session Hygiene to Write Specs (Section 8)
- Sub Agents moved before Session Hygiene sections

### Process we used to refine
- Walked through 02_organized-ideas.md section by section, in order
- For each section: displayed current content, discussed, captured changes
- Corrections were precise - adjusted framing, added details, restructured
- When sections needed splitting (Session Hygiene → two sections), did that and renumbered
- When ordering felt wrong (Encode Workflows too early), moved and renumbered
- Kept notes file as append-only log of decisions and rationale
- Didn't go back to edit previous entries in notes - just added new entries

---

