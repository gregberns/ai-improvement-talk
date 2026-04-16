# Project Status

**Last updated:** 2026-04-15
**Current phase:** Phase 4 (writing articles) — early phase articles being written

## What We've Done

### Session 1 (2026-04-03 → 2026-04-07)

1. **Established collaboration model** — high-collab mode based on resume-building session patterns. Methodology codified in `methodology.md`.

2. **Restructured the repo:**
   - `sources/` — original talk notes, brainstorm docs, reference material
   - `ideas/` — numbered idea folders with versioned files + index
   - `articles/` — empty, will hold published content
   - `CLAUDE.md` + `methodology.md` at root

3. **Captured ~40 ideas** in `ideas/index.md` — seeded from talk (01_notes, 02_organized, 03_talk) plus new ideas from discussion.

4. **Created 16 idea folders** with versioned working notes (v1-v3):
   - 001-013: Original talk ideas
   - 014-016: New transition articles filling the gap between 006 and 007

5. **Defined the early phase progression** — the sequence that hits the broadest audience:
   ```
   003  Stop model-hopping              [foundation]
   004  Pick one agent                  [foundation]
   005  Set up project metadata         [metadata]
   006  Evolve project metadata         [metadata]
   014  The code isn't right            [workflow/mindset] — THE key article
   015  It missed things                [workflow]
   016  Agent won't follow process      [workflow/metadata]
   ```

6. **Defined article template:** Symptom → What to Change → Reinforcing Patterns → Why What You Were Doing Wasn't Working → Why the Alternative Works Better

7. **Discovered the hidden arc:** The series walks devs toward spec-driven development without them knowing it. Each article plants seeds for the next.

8. **Discovered the key mechanism (014):** "GSD mode" vs "plan/reason mode" — when you give explicit instructions the model executes without judgment; when you give context and intent it plans and reasons. The user needs the LLM to write its own implementation instructions.

9. **Drafted prompt templates for:**
   - 005: Project metadata setup
   - 006: Post-session analysis
   - 014: The sneaky spec (plan-first workflow)
   - 015: Self-review against plan (simple prompt)
   - 016: Diagnose process failures (simple prompt)

### Session 2 (2026-04-14 → 2026-04-15)

1. **Established article writing process** — documented in `articles/WRITING-GUIDE.md`. Key discovery: the idea outlines are 90% of the article. The job is smoothing seams and tightening, not writing from scratch. Process: lay out structure as bullets → align on arc → write section by section (purpose → options → pick → iterate → lock).

2. **Defined the article format:**
   - Preamble (series intro, shared across articles)
   - Opening prose hook (make reader feel the pain)
   - **Symptom** / **Why** / **Fix** (with prompt) / **While it works** / **How it works** / **What's next** / **Not yet**
   - Action first, explanation after. "Run the prompt below. Then read the rest while it works."

3. **Wrote article 005 (Set Up Your Project Metadata)** — ~700 words. Iterated section by section with review agents. Verified AGENTS.md/CLAUDE.md auto-loading behavior (CLAUDE.md loads hierarchically, AGENTS.md not natively supported by Claude Code but symlink approach works).

4. **Wrote article 006 (Evolve Your Project Metadata)** — ~710 words. Different energy from 005: not "things are broken" but "you're not done, tune it in." Added Bonus section: embed the refinement practice into the AGENTS file so the agent reminds you.

5. **Generated first drafts of 014** — agent-produced, in `articles/`. Needs section-by-section iteration.

6. **Series framing established:** "Moving your coding agent from intern to senior developer." Target: devs already using agents but not getting the results they keep hearing about.

### Session 3 (2026-04-15)

1. **Aligned on the 014-016 arc** — these three articles shift the developer's *process* (005-006 gave the agent *knowledge*). The progression:
   - 014: "I need to communicate differently" — mindset shift
   - 015: "I need to verify, not just trust" — practice shift
   - 016: "I need to encode, not just expect" — system shift

2. **Identified the core thread:** "The agent will do exactly what you set it up to do — no more. If the results aren't good enough, define the job better." The message isn't accusatory — it's "you're a good engineer using patterns that worked for decades. They don't transfer cleanly."

3. **014's headline insight:** "Communicate the problem, not the solution." Devs compress a rich mental model into thin instructions, drop context and reasoning, expect the agent to reconstruct what was lost. It can't. The fix: brief the agent on the problem, let it plan, review the plan, then implement.

4. **Decided: prompts must work when run blindly.** The prompt is the product. If the reader runs it and gets bad output, we lose them. Full pipeline stays in the prompt even if the article only explains part of it. Steps the reader doesn't understand yet are fine — they're instructions for the agent, not the reader.

5. **Built article skeletons for 014, 015, 016** — section-by-section structure with what each section needs to SAY, where each article starts/stops, and forward pointers between them. Saved as versioned skeleton files in idea folders.

## What's In Progress

- **Article 014 (The Code Isn't Right)** — skeleton aligned, ready for section-by-section writing
- **Article 015 (It Missed Things)** — skeleton aligned, queued after 014
- **Article 016 (Agent Won't Follow Process)** — skeleton aligned, queued after 015
- **Review feedback on 005** — some items addressed, minor tweaks may remain
- **006 anti-pattern review prompt** — deferred from session 1, still TODO

## Key Decisions Made

- **Linear progression, not categories** — articles ordered by "when should a dev adopt this," categories are just tags
- **Ideas and articles are separate** — ideas get refined in `ideas/`, promoted to `articles/` when ready, with cross-references
- **Folder numbering = creation order** (stable IDs), reading order lives in the index only
- **File versioning** — v1.md, v2.md, etc. in each idea folder
- **Audience:** engineers in Claude Code/Codex/terminal TUI agents, not code-completion level. May do on-ramp later.
- **AGENTS.md as source of truth** — industry moving to AGENTS.md standard. CLAUDE.md symlinked to it for Claude Code compatibility.
- **Rules/hooks not introduced until 016** — when they solve a specific pain, not as a concept to learn
- **Article 005 is the entry point** — first article for the target audience. 003/004 (foundation) may come later or be folded in.
- **Action before explanation** — get the reader doing something immediately. They can read the "how it works" while the agent runs.
- **Prompts are the product** — must work when run blindly. Full pipeline in the prompt even if article only teaches part of it. Reader trust depends on the prompt producing good results.
- **014-016 arc: knowledge → process** — 005-006 gave the agent knowledge (what the project is). 014-016 give it process (how to work on it).
- **Tone for process articles** — not accusatory. "You're a good engineer. These patterns are new. Here are better ones." Respect the reader's learning capacity.
