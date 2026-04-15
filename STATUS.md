# Project Status

**Last updated:** 2026-04-14
**Current phase:** Phase 2 (adding context) — early phase articles being refined

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

## What's In Progress

- **006 anti-pattern review prompt** — TODO, was next up
- **006 exercise concept** — create a skill, use it, refine it, use it again (noted but not built)
- **Reviewing/refining early phase articles** — went through 003-006, 014-016 for story arc. Ideas 007-013 haven't been reviewed yet against the new template/arc.

## Key Decisions Made

- **Linear progression, not categories** — articles ordered by "when should a dev adopt this," categories are just tags
- **Ideas and articles are separate** — ideas get refined in `ideas/`, promoted to `articles/` when ready, with cross-references
- **Folder numbering = creation order** (stable IDs), reading order lives in the index only
- **File versioning** — v1.md, v2.md, etc. in each idea folder
- **Audience:** engineers in Claude Code/Codex/terminal TUI agents, not code-completion level. May do on-ramp later.
- **Claude disclaimer** — "We'll talk about Claude but these patterns apply to any coding agent"
- **Rules/hooks not introduced until 016** — when they solve a specific pain, not as a concept to learn
