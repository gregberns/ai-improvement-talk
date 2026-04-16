# AI Improvement Talk — Article Series Project

## What This Is

A series of articles teaching developers to dramatically improve their outcomes with AI coding agents. The series framing: **"Moving your coding agent from intern to senior developer."**

Origin: a talk presented to a dev team (`sources/03_talk.md`). Now a full article series.

Target audience: developers using AI coding agents (Claude Code, Codex, Gemini CLI, etc.) but frustrated with results or not getting the outcomes they see others getting.

## Current State

**Phase 4** — writing articles. See `STATUS.md` for full history and `TASKS.md` for what's next.

Articles 005 and 006 are drafted. 014 has a first draft needing iteration. The rest of the early phase sequence (003, 004, 015, 016) are in idea stage.

## How We Work

See `methodology.md` for the full collaboration model. Key points:

- **High-collaboration mode** — human provides taste, context, and judgment; AI provides breadth, speed, and optionality. When those roles invert, output is mediocre.
- Generate options, not proposals. Branch when asked for more.
- Lock decisions and move on. Don't revisit locked elements.
- When new ideas surface during any work, append them to `ideas/index.md` immediately.

For article writing specifically, see `articles/WRITING-GUIDE.md` — the authoritative guide for format, voice, and process.

## Project Structure

- `STATUS.md` / `TASKS.md` — Session continuity. Read these first.
- `methodology.md` — Collaboration model
- `articles/` — Article drafts and writing guide
  - `WRITING-GUIDE.md` — Article format, voice, and writing process
  - `005-setup-project-metadata.md` — Reference article (match this format and voice)
  - `006-evolve-project-metadata.md` — Sequential article template
  - `014-code-isnt-right.md` — First draft, needs iteration
- `ideas/` — Idea backlog. `index.md` lists all ideas with status and category tags. Ideas get individual numbered folders (e.g., `001-topic/`) with versioned files.
- `sources/` — Reference material:
  - `03_talk.md` — Original talk notes (11-step progression)
  - `high-collab-session-notes/` — Patterns from the resume-building session
  - `01_notes.md`, `02_organized-ideas.md` — Original brainstorm and organized notes

## Content Philosophy

- Each article = a **discrete action** a developer can take
- Action first, explanation after. The reader should be doing something within the first few sections.
- Terse wins. Compress until meaning nearly breaks, back off one step.
- Tone: empathetic about the struggle, then blunt about the fix
- Don't over-polish early. Content and structure first, refinement later.
- The series is a **linear progression**, ordered by "when should a dev adopt this?"
- Categories (quality, context, workflow, mindset) are tags, not the organizing principle.
- AGENTS.md is the source of truth for agent configuration. CLAUDE.md symlinked to it.

## Guidelines for Agents

- Read `STATUS.md` and `TASKS.md` first for current state
- Read `articles/WRITING-GUIDE.md` before any article writing work
- Read `methodology.md` before starting content work
- Check `ideas/index.md` for current state of the backlog
- When new ideas surface during work, append them to `ideas/index.md` immediately
- Don't restructure the idea tree without explicit discussion
- Don't polish prose in early phases — focus on content and structure
- Print article sections inline in conversation — don't make the user read files
