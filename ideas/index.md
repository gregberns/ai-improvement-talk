# Ideas Index

All ideas. Ones with folders have source material built out. Others are index-only until we develop them.

Category tags: `[foundation]` `[metadata]` `[context]` `[workflow]` `[quality]` `[mindset]` `[collab]` `[framing]` `[structure]`

---

## Unrefined — Has Folder

- [001-intro-world-is-changing](001-intro-world-is-changing/) `[framing]` — Empathetic opening. The world is changing, tools feel broken, but what if it's us? Stop complaining, get to work.
- [002-where-are-you](002-where-are-you/) `[framing]` — Self-assessment. Shapiro's Five Levels, Yegge's evolution model. Know where you are to know what's next.
- [003-stop-model-hopping](003-stop-model-hopping/) `[foundation]` — Best model, max effort, stop counting tokens. The engine matters.
- [004-pick-one-agent](004-pick-one-agent/) `[foundation]` — Pick one tool, go deep. Table stakes.
- [005-setup-project-metadata](005-setup-project-metadata/) `[metadata]` — "It's not following my conventions!" — encode guardrails. CLAUDE.md, AGENTS.md, hooks, commands.
- [006-evolve-project-metadata](006-evolve-project-metadata/) `[metadata]` — Ongoing practice. Analyze sessions, generalize, encode improvements. 10 min/hr for 1 day.
- [007-sub-agents](007-sub-agents/) `[workflow]` — Be the orchestrator. Delegate to sub-agents. Stop burning context.
- [008-kill-bad-sessions](008-kill-bad-sessions/) `[context]` — Session gone south? STOP. Summarize, clear, restart. Don't try to recover.
- [009-session-continuity](009-session-continuity/) `[context]` — STATUS.md + TASKS.md. Pre-compaction saves. Features spanning threads = anti-pattern.
- [010-write-specs](010-write-specs/) `[workflow]` — "I don't like the results" → write specs. Brain dump, iterate, formalize, implement.
- [011-implement-with-loops](011-implement-with-loops/) `[workflow]` — Ralph Loop for implementation. Multi-agent review for spec gaps.
- [012-encode-your-process](012-encode-your-process/) `[workflow]` `[mindset]` — Meta: define your workflow, encode it, formalize it. Create commands.
- [013-progression-overview](013-progression-overview/) `[structure]` — The 9-step progression from the talk. Structural backbone for the series.
- [014-code-isnt-right](014-code-isnt-right/) `[workflow]` `[mindset]` — "I told it to implement X and it didn't do it right." The sneaky spec — brainstorm, research, plan together, then implement.
- [015-it-missed-things](015-it-missed-things/) `[workflow]` — "It says it's done but stuff is missing." Self-review against the plan. Plants the seed for the Ralph Loop.
- [016-agent-wont-follow-process](016-agent-wont-follow-process/) `[workflow]` `[metadata]` — "It won't follow the process I told it!" Where rules/hooks get introduced — to solve git workflow, test running, etc.
- [017-execution-vs-reasoning](017-execution-vs-reasoning/) `[mindset]` `[workflow]` — "It keeps reinventing things that already exist." Deep dive on execution mode vs. reasoning mode — why commands trigger procedural behavior, how to consciously separate the two phases. The mechanism behind 014.

## Unrefined — Index Only

- **If your primary mode is dictating specific changes to specific files** `[mindset]` — Address devs using AI as fancy find-and-replace. You're leaving value on the table. Frame without condescension. Related: Eng #2 quote "going over things function by function."
- **Brownfield convention conflicts — old patterns vs new patterns** `[metadata]` — When your codebase has legacy patterns AND new patterns and you only want new conventions followed. Needs explicit metadata: "pattern X exists in /legacy, all new code uses pattern Y, never use X in new code." Might be a sub-article of 005 or its own piece for more experienced devs.
- **"Fix the layout" — the directive pattern and why it fails** `[mindset]` — Directive style forces models into myopic mode. Specificity without context. Need to find Anthropic research.
- **Specificity without context vs. context with intent** `[mindset]` — "Change function X to do Y" (directive) vs. "we have this problem because of Z" (context + intent). The second lets the model use judgment.
- **Problem 1: Getting agents to perform consistently** `[framing]` — What early articles address. The "it works sometimes" frustration.
- **Problem 2: Shifting practices to spec → plan → implement** `[framing]` — Fundamental workflow change. Mid-stage articles.
- **Problem 3: Changing the developer's mindset (hardest of all)** `[mindset]` — "Make 3 versions, select the parts we like." Buying intelligence through tokens. Nate video — need to find.
- **Preventing unit test output from consuming context** `[context]` `[quality]` — Test output fills context, degrades performance. Custom CI summaries.
- **Clearing context regularly — when and why** `[context]` — When to fresh-start vs. push through. Signs of degradation.
- **Tools to retain information across sessions** `[context]` — Memory, STATUS.md, project metadata as persistent context.
- **Starting a new conversation from a past one** `[context]` — Bootstrapping new sessions. Summaries, specs, task lists as handoff.
- **Spec-first change management (beads pattern)** `[workflow]` — Advanced. Whole-program spec, change spec then update code. See `sources/prompt-planning-with-beads.md`.
- **Quality baseline: unit + integration tests** `[quality]` — Table stakes for agent-assisted dev.
- **Advanced testing: property, E2E, contract, scenario tests** `[quality]` — Different bug classes. Dive in slowly.
- **Digital twins for testing** `[quality]` — Test doubles mirroring production. Realistic agent feedback.
- **High unit test code coverage** `[quality]` — Fast, comprehensive feedback loops for agents.
- **Adding types, especially to non-typed languages** `[quality]` — Types as guardrails. High-ROI investment.
- **Aggressive linting** `[quality]` — Strict, not permissive. Catch agent-introduced anti-patterns.
- **Dependency checks / ensuring layered architecture** `[quality]` — Automated circular dependency checks. Architecture enforcement via tooling.
- **Generate options, not proposals** `[collab]` — 5 approaches, pick best pieces. Don't let AI converge early.
- **Purpose before implementation** `[collab]` — "What does this need to DO?" before "how?"
- **Context reframes when output feels wrong** `[collab]` — More context, not more attempts.
- **The funnel pattern for architecture** `[collab]` — Start wide, converge. Prevents local maxima.
- **Lock and move in coding sessions** `[collab]` — Lock decisions, don't revisit.
- **Atomic-level iteration for complex features** `[collab]` — One function, one interface, one test.
- **Using review agents for different perspectives** `[collab]` — Architect, security, performance, UX review.
- **Terse consistently wins (in code too)** `[collab]` — Compress. Simplest that works.
- **High-collaboration mode as a skill** `[collab]` `[structure]` — Resume session patterns as teachable mode.
- **Symptoms-first navigation / entry point routing** `[structure]` — Critical: devs need to start at the right article, not page 1. "Here are symptoms/behaviors — once you see one you're exhibiting, start there." If you're not model hopping, skip that article. This might be the actual landing page or intro piece — a behavior checklist that routes you into the series at the right point.
- **Publishing structure that supports growth** `[structure]` — Insert articles without disrupting published.
- **"Buying intelligence" through tokens** `[mindset]` — Tokens = purchasing better outcomes. 5 options, select best. Video reference: https://youtu.be/-bQcWs1Z9a0?si=-2t7svUMBIde-snW
- **Finding the Anthropic research on directive vs. collaborative patterns** `[mindset]` — PRIMARY SOURCE: https://www.anthropic.com/research/economic-index-march-2026-report (hints at interaction styles, directive/procedural vs planning). Also: Anthropic "Claude Code Best Practices" blog post, Barke et al. "Grounded Copilot" 2023 (acceleration vs exploration modes), Schulhoff et al. "The Prompt Report" 2024.
- **Orchestration overview** `[workflow]` — Intro to multi-agent orchestration: what it is, why it matters, the landscape of projects/tools. Later-stage — after sub-agents are comfortable. Reference: https://youtu.be/eT1F2BAZJ64?si=63_x0PRLcls9P4Nr

---

*Last updated: 2026-04-03*
*To add an idea: append to "Unrefined — Index Only" with a category tag. Create a folder when ready to develop it.*
