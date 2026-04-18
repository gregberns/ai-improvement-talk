# Tasks

**Last updated:** 2026-04-17

## Current Priority: Polish and Publish First Two Groups

Metadata (005, 006) and Process (014, 015, 016, 017) are drafted. Six articles ready for review and refinement.

### Article Writing — Completed Drafts
- [x] **metadata-01** — Set Up Your Project Metadata (~700 words, drafted)
- [x] **metadata-02** — Evolve Your Project Metadata (~710 words, drafted)
- [x] **process-01** — The Code Isn't Right (iterated, drafted)
- [x] **process-02** — It Missed Things (drafted)
- [x] **process-03** — The Agent Won't Follow the Process (drafted)
- [x] **process-04** — Reasoning vs Execution (drafted 2026-04-17, deep-dive format)

### Review and Polish
- [ ] **Consistency pass across all 6 articles** — voice, format, transitions between them
- [ ] **005 minor tweaks** — first sentence of opening still needs work ("How they're going to take our jobs" follow-up)
- [ ] **006 anti-pattern review prompt** — build prompt for experienced users to review past conversations for anti-patterns (deferred deliverable from idea file)
- [ ] **Series thesis placement** — decide where `ideas/series-thesis.md` content lives long-term (intro page, manifesto article, capstone)

### Publishing / Distribution
- [ ] **Decide where to publish** — blog, GitHub Pages, newsletter, something else?
- [ ] **Share with discord group** — articles are now in a consumable format via articles/index.md
- [ ] **Review reading order end-to-end** — once sharing, check that a fresh reader can follow the progression

### Decisions Pending
- [ ] **003/004** — Are these their own articles, folded into one, or just a brief mention in 005's preamble? They're "foundation" pieces (best model, pick one agent) but 005 is the real entry point.
- [ ] **Group names** — "Metadata" and "Process" are working names. Finalize before publishing.

### Next Group: Context (007-009)
- [ ] **Review ideas 007, 008, 009** against article template and story arc
- [ ] **Write article 007** — Sub-agents / orchestration
- [ ] **Write article 008** — Kill bad sessions
- [ ] **Write article 009** — Session continuity

### Later Groups
- [ ] **Write 010-012** — Specs, Ralph Loop, engineering your process
- [ ] **Write 013** — Progression overview / table of contents
- [ ] **Write 018** — Directive vs iterative pattern (needs Anthropic Economic Index research)

### Research Tasks
- [ ] **Anthropic Economic Index report** — read https://www.anthropic.com/research/economic-index-march-2026-report for directive vs collaborative interaction patterns
- [ ] **Nate "buying intelligence through tokens" video** — verify https://youtu.be/-bQcWs1Z9a0?si=-2t7svUMBIde-snW is the right one, extract key points
- [ ] **Verify research references** — Barke et al. "Grounded Copilot" 2023, Schulhoff "The Prompt Report" 2024, Anthropic "Claude Code Best Practices" blog post

### After All Groups
- [ ] **Build out remaining idea folders** — ~25 index-only ideas still need folders when developed

## Backlog / Ideas Captured but Not Developed
- Orchestration overview article (video ref: https://youtu.be/eT1F2BAZJ64)
- Brownfield convention conflicts (old vs new patterns in metadata)
- Symptom-routing entry point — behavior checklist that routes devs to the right starting article
- Quality practices cluster (testing, types, linting, architecture enforcement)
- Advanced collaboration patterns (from high-collab session notes)
- The three core problems framing (consistency, workflow shift, mindset change)
- "Buying intelligence through tokens" concept
- High-collaboration mode as a teachable skill
- Publishing structure that supports article insertion

## Notes for Next Session
- Read `STATUS.md`, `TASKS.md`, `articles/WRITING-GUIDE.md`, and `articles/index.md` first
- Read all 5 articles in `articles/` — they use group-based naming: `metadata-01-`, `process-01-`
- `metadata-01-setup-project-metadata.md` is the reference article for format and voice
- The writing process: lay out structure as bullets → align on arc → section by section (purpose → options → pick → iterate → lock) → review agents → final pass
- Review agents run as three personas in parallel: (1) flow/logic, (2) developer reader, (3) writing guide compliance
- Key terms: "communicate the problem, not the solution" is the headline insight; execution mode vs reasoning mode introduced lightly in process-01, deep dive in 017
- Don't use "creative work" for implementation
- Prompts must work when run blindly — they're the product
- Lean before the fix, depth after — tight above the prompt, teaching below
- Tone: not accusatory — "you're a good engineer, these patterns are new"
