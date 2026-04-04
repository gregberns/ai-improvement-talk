# AI Improvement Talk — Article Series Project

## What This Is

A content project producing a series of articles teaching developers discrete, actionable steps to dramatically improve their outcomes with AI coding agents (primarily Claude Code, but applicable broadly).

Origin: a talk presented to a dev team (`03_talk.md`). Now expanding into a full article series.

## How We Work

See `methodology.md` for the full collaboration model. Key points:

- **High-collaboration mode** — human provides taste, context, and judgment; AI provides breadth, speed, and optionality. When those roles invert, output is mediocre.
- Ideas are captured in `ideas/index.md` using an **append-only model** — add freely, don't remove or reorder until a deliberate restructuring pass.
- Work in phases: broad capture → add context → order → flesh out → polish. We are currently in early phases.
- Generate options, not proposals. Branch when asked for more.
- Lock decisions and move on. Don't revisit locked elements.
- When new ideas surface during any work, append them to `ideas/index.md` immediately — don't let them evaporate.

## Project Structure

- `README.md` — Public-facing project intro
- `methodology.md` — Our working process and collaboration model
- `ideas/` — Idea backlog. `index.md` lists all ideas with status and category tags. Ideas get individual numbered folders (e.g., `001-topic/`) with versioned files as they're developed.
- `articles/` — Published-ready content. `index.md` is the linear reading order. Each article folder back-references its source idea(s).
- `sources/` — Reference material that fed the ideas:
  - `03_talk.md` — Original talk notes (11-step progression)
  - `high-collab-session-notes/` — Distilled patterns from the resume-building session
  - `01_notes.md`, `02_organized-ideas.md` — Original brainstorm and organized notes
  - `prompt-planning-with-beads.md` — Example of spec-first change process
  - `01_starting-off.md` — Session capture from initial project planning

## Content Philosophy

- Each article = a **discrete action** a developer can take
- Frame as: **symptom → root cause → actionable next step**
- Terse wins. Compress until meaning nearly breaks, back off one step.
- Target audience: developers using AI tools but frustrated with results, or not getting the outcomes they see others getting
- Tone: empathetic about the struggle, then no-nonsense actionable ("stop complaining, get to work")
- Don't over-polish early. Content and structure first, refinement later.

## Content Structure

- The series is a **linear progression**, NOT organized by category. Ordered by "when should a dev adopt this?"
- Categories (quality, context, workflow, mindset) are **tags on articles**, not the organizing principle.
- The progression interleaves topics: some setup, then context, then sub-agents, then quality, then specs, etc.
- Inserting new articles between existing ones must be easy — no rigid numbering.
- Small clusters of related articles may sit together where internal order doesn't matter.

## Guidelines for Agents

- Read `methodology.md` before starting content work
- Check `ideas/index.md` for current state of the backlog
- When new ideas surface during work, append them to `ideas/index.md` immediately
- Don't restructure the idea tree without explicit discussion
- Don't polish prose in early phases — focus on content and structure
- The high-collab session notes contain patterns that are both: (a) how we work on this project, and (b) potential content for later articles about advanced AI collaboration
