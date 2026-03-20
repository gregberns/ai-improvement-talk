# Evoking Staff-Level AI Engineers

## 1. The Transition

The job you loved — refining and building beautiful systems — is changing underneath you.

> "To quote a programmer friend, 'I'm having a real hard time letting go.'"

> "hm, (if/)when I do start to use AI I'll have to try that approach"

We've been promised these tools are amazing. In practice, working with AI feels like working with a mid-dev who makes a mess more often than not.


### Problem

**But...** what if it's not the tools that are sub-par — it's how we're using them?



### Hope

You CAN work with staff-level AI engineers. They don't come out of the box. You need to learn how to evoke that performance.

**How this talk works:** You have a pain point? It corresponds to a level. Here's a solution to experiment with. Don't just spot-fix — examine your entire engineering process. You are a system. Improve it.

**Where are you?** Others have mapped the progression. Be honest about where you are. This talk gives you the next step.





### Dan Shapiro's Five Levels
1. **Spicy Autocomplete** — Tab-completing code suggestions
2. **Junior Dev Chat** — Ask questions, get code snippets, copy-paste
3. **Pair Programmer** — Agent in your IDE, working alongside you
4. **Senior Dev** — Agent handles full tasks, you review and direct
5. **Software Factory** — Multiple agents, orchestrated workflows, you architect

### Yegge's Developer Agent Evolution Model
1. **Zero/Near-Zero AI** — Maybe code completions, sometimes ask chat questions
2. **Coding agent, permissions on** — Narrow agent in sidebar, asks permission to run tools
3. **Agent, YOLO mode** — Trust goes up, permissions off, agent gets wider
4. **In IDE, wide agent** — Agent fills the screen, code is just for diffs
5. **CLI, single agent YOLO** — Diffs scroll by, you may or may not look
6. **CLI, multi-agent YOLO** — 3-5 parallel instances, very fast
7. **10+ agents, hand-managed** — Pushing limits of hand-management
8. **Building your own orchestrator** — On the frontier, automating your workflow












---

## 2. The Foundation — Stop Experimenting

**Problem:** "Tokens are expensive / I want something cheaper / I like OSS"

Stop model-hopping. Claude Opus. HIGH effort. Tune it in.

You're building a Formula 1 car. Don't install a lawn mower engine.

DO NOT CONCERN YOURSELF WITH TOKENS. Never again.












---

## 3. Set Up Your Project Metadata

**Problem:** "It's not following my conventions! Every time it's missing things!"

Claude's context isn't loaded with your conventions. You need to set it up for success.

You put guardrails on your programs — WHY NOT YOUR CODING AGENTS?

**"Project Metadata"** = rules, AGENTS.md, CLAUDE.md, hooks, commands. Root CLAUDE/AGENTS files should be 100-150 lines max.

**Action:** New session → "Research how to set up this project so Claude Code follows its conventions." Tell it what you're struggling with. Review what it generates. Ask questions — "What is a command?", "Why CLAUDE files several folders deep?"

**Result:** Context gets auto-injected. Better performance. More consistency.












---

## 4. Evolving Your Project Metadata

This isn't a problem/solution — it's an ongoing practice.

After every task (at 50-75% context), ask Claude: "Look at what just happened. What improvements can we make to our CLAUDE/AGENTS files? What missteps happened? What worked? Generalize — don't overfit."

Spend 10 minutes per hour of coding - for 1 day.

**Example:** You build a feature, tell Claude to commit. Then push. Then PR. Then a fix. Then all those steps again. You shouldn't need to repeat this. Ask: "How do we prevent me giving you these steps every time?"

**Key:** Generalize learnings. Build abstractions. Claude tends to parrot exact words — push for general principles.












---

## 5. Sub Agents — Be The Orchestrator

**Symptom:** Main thread doing everything — research, file reads, code changes, commits. You're burning context. How often do you compact? Can you finish a feature in one context?

**Solution:** Delegate. Tell Claude: "You are the orchestrator, use subagents, delegate your work."

Install [oh-my-claudecode](https://github.com/yeachan-heo/oh-my-claudecode). Now. You need an agent framework.

**Result:** Longer sessions. Focused agent. More consistency.












---

## 6. Abysmal Sessions

**Problem:** Session has gone south.

STOP. Kill it. Now. Don't try to recover — it's futile.

Summarize → copy → clear → new session.












---

## 7. Session Continuity

**If you must compact:** Create uncommitted STATUS.md + TASKS.md files. Before compaction, update them. They survive compaction. (Implement as a hook or command.)

At 10% before compaction: stop everything, save state, write summary, copy, clear, paste and go.

**But:** Features spanning multiple threads = ANTI-PATTERN. Use sub agents. Design first, then implement in a fresh session.












---

## 8. Write Specs — Become The Architect

**Problem:** "I tell Claude what I want, it builds it, and I don't like the results."

**Answer:** Specs.

"But that's boring!" — You don't write it all. Brain dump, then iterate with Claude. You're the architect, Claude helps you think through the details.

**Action:** Start simple — single spec file, clear session, implement. Disable Claude Plan Mode — actively iterate on the spec. Write to disk, then implement.

**Warning:** This may produce more improvement than any other step.

**Why it works:** Forces deep thinking. Forces research. Code snippets in specs enforce conventions. If samples don't follow convention — what's missing from the project metadata?





**The Full Process:**

Create agent or command

1. Brain dump
2. Decompose & requirements
3. Research
4. Nit pick details (section by section)
5. Formalize spec
6. Implement (Ralph Loop)
7. Code review (architect, critic, QA agents)
8. Spec review (architects validate spec)












---

## 9. Implement With Loops

Once you're using specs, they won't always turn out how you'd like. Two problems:

**Problem 1: Agent skips parts of the spec**
- Solution: Ralph Loop — implement a little, check against spec, write more, check, loop until implementation matches spec
- Contained in oh-my-claudecode

**Problem 2: Spec itself has issues**
- Solution: Multi-agent spec review before implementation
- 3 agents, different angles: spec→plan (forward coverage), plan→spec (reverse traceability), plan→context (codebase alignment)
- See: [Xexr gt-toolkit Stage 6: Plan Review](https://github.com/Xexr/gt-toolkit/blob/main/formulas/README.md#stage-6-plan-review)












---

## 10. Meta — Encode Your Process

**Next step:** Engineer your actual development workflow.

You have a process for building features. What is it? Define it. Encode it. Have Claude help you formalize it. If Claude doesn't follow it — refine until it does.

This forces you to think hard about what you actually do.

**Example:** This presentation — brain dump → refine each section → iterate → refine. A Ralph Loop for content.

**Start:** Create a command. "We're building this feature AND encoding my process, so we can replicate it next time." Off-the-shelf won't help if you don't understand how it works.












---

## 11. The Progression

It doesn't happen in a day — one step at a time.

1. **Excellent model** — Stop model-hopping. Best model, max effort, stop counting tokens.
2. **Coding agent** — Stick with one agent. Table stakes.
3. **Tuned-in agent** — Encode guardrails. Rules, hooks, CLAUDE.md, AGENT.md files.
4. **Evolve project metadata** — Analyze sessions, generalize learnings, encode what works.
5. **Sub agents** — Delegate. Be the orchestrator.
6. **Session hygiene** — Focus on dense sessions.
7. **Write specs** — Become the architect. Brain dump, iterate, formalize.
8. **Refine specs + implement loops** — Multi-agent spec review. Ralph Loop to close gaps.
9. **Meta** — Examine your mental development model.












---

## References
- [Dan Shapiro's Five Levels](https://www.danshapiro.com/blog/2026/01/the-five-levels-from-spicy-autocomplete-to-the-software-factory/) — Spicy Autocomplete to Software Factory
- [Yegge's Developer Agent Evolution Model](https://justin.abrah.ms/blog/2026-01-08-yegge-s-developer-agent-evolution-model.html) — 8 stages from zero AI to custom orchestrators
- [Xexr gt-toolkit](https://github.com/Xexr/gt-toolkit/blob/main/formulas/README.md) — reliable spec formulas
- [oh-my-claudecode](https://github.com/yeachan-heo/oh-my-claudecode) — agent framework (sub agents, ralph loop, review agents)
