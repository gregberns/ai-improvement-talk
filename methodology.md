# Methodology — How We Work On This Project

## The Collaboration Model

This project uses a **high-collaboration mode** distilled from a session that produced dramatically better results than typical AI interactions. The quality came from the interaction pattern, not any single prompt.

**Core dynamic:** The human is the decision maker. The AI is the option generator. The human provides taste, context, and judgment. The AI provides breadth, speed, and optionality. When those roles invert — AI making judgment calls, human just approving — output is mediocre.

### Interaction Patterns

1. **Purpose before language.** Define what each piece needs to accomplish before trying to write it. "What does this section need to DO?" comes before "what should it say?"

2. **Generate options, not proposals.** Produce multiple genuinely different approaches — different framings, structures, starting points. The human picks pieces, combines, and pushes further. Best results emerge from selection pressure across many options.

3. **Branch when asked for more.** Don't refine the same direction — deliberately try different angles. Prevent convergence on something mediocre.

4. **Context reframes > word changes.** When output feels off, the fix is usually more context about the real situation, not better word choices. Share the WHY behind corrections.

5. **Terse consistently wins.** Start with the full idea, compress until meaning nearly breaks, back off one step.

6. **Lock and move.** Explicitly lock decisions and move on. Don't revisit locked elements. Prevents infinite refinement.

7. **Work at the atomic level.** One idea, one section, one concept at a time. Granularity forces depth.

8. **Capture insights as they surface.** When a compelling framing or new idea surfaces as a byproduct of other work, save it immediately to `ideas/index.md`. Don't assume it'll come back.

9. **Use review agents for external perspective.** Agents critiquing from a specific viewpoint catch blind spots. Most valuable for identifying gaps, not suggesting rewrites.

10. **Wide exploration first, then converge.** Start with multiple parallel approaches before committing. Width at the beginning prevents local maxima.

## The Phases

### Phase 1: Broad Capture (current)
- Cast wide. Get every idea documented in `ideas/index.md`.
- Append-only — add freely, never remove or reorder.
- Don't worry about quality, polish, or even coherence. Just capture.
- If an idea is half-formed, write it half-formed. A bad note is better than a lost idea.

### Phase 2: Add Context
- Go through each idea and add context, especially where content is thin.
- What's the symptom a dev experiences? What's the root cause? What's the action?
- Some ideas will merge. Some will split. That's fine.

### Phase 3: Order and Structure
- Arrange ideas into a **linear progression** developers follow step by step.
- This is NOT organized by category (all quality topics together, all context topics together). It's ordered by **"when should a dev adopt this?"** — meeting devs where they are.
- The progression interleaves topics: some foundational setup, then a couple context management techniques, then sub-agents, then some quality practices, then specs, then more advanced quality, etc.
- **Categories are tags, not sections.** Each article/node gets a category tag (quality, context, workflow, mindset, etc.) but the reading order is the primary structure.
- At some points in the progression, a small cluster of related items may sit together where internal order doesn't matter much. A dev can do them in any sequence within the cluster.
- **Critical constraint: inserting new articles between existing ones must be easy.** Adding an article between steps 5 and 6 shouldn't require renumbering or restructuring everything. This likely means we avoid hard numbering and use a flexible ordering scheme (or just an ordered list where insertion is cheap).
- A developer reads linearly, skipping what they already do. The first steps are essential things almost nobody is doing. Later steps assume earlier ones are in place.

### Phase 4: Flesh Out
- Starting from the simplest first steps, build out each idea.
- Focus on content and structure, not polish.
- Frame as: symptom → root cause → actionable next step.
- As ideas surface during this work, append to `ideas/index.md` or add directly as new branches.

### Phase 5: Refine and Polish
- Only after a good chunk of articles are fleshed out.
- Tighten prose. Ensure consistency. Add examples.
- Prepare for release — but don't discuss publishing venue until content is ready.

## The Append-Only Backlog (`ideas/index.md`)

This is the central artifact. Rules:

- **Append freely.** Any idea, any time, any level of completeness.
- **Don't delete.** If an idea turns out to be bad, mark it as such. The record of what we considered matters.
- **Don't reorder casually.** Restructuring is a deliberate Phase 3 activity.
- **Tag with status** so we know what state each idea is in.
- **New ideas from any phase** get added here. Working on Phase 4 and a new idea surfaces? Append it.

## Content Framing

Each article/idea targets a **discrete action** a developer can take:

- **Symptom:** What the developer is experiencing ("Claude keeps ignoring my conventions")
- **Root cause:** What's actually going on ("Your project metadata doesn't encode your conventions")
- **Action:** What to do about it ("Set up CLAUDE.md with your conventions. Here's how...")

Some articles will be introductory/framing (the world is changing, this is hard, here's the mindset). Then we stop complaining and get to work.

For developers operating in a very manual mode ("telling the model to modify a specific function in a specific file" as their primary pattern) — we need to address this early. The challenge is describing what they're doing wrong when we're not doing it ourselves anymore. Frame it as: "If this is how you work, here's why results feel inconsistent, and here's the shift."
