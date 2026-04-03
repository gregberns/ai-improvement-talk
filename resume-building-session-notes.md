
## Structural Conversation Patterns

1. Funnel pattern: explore wide, then converge, then refine

We started with 5 parallel drafts — deliberately different angles. Then reviewed them, pulled out what worked from each, merged to 2, then to 1. Then went sentence by sentence. The width at the beginning prevented us from getting trapped in a local maximum. Most resume sessions start with one draft and iterate — which means you're polishing whatever direction you happened to start in.

2. Purpose before language

For the summary, we didn't start writing. We first defined: "What does sentence 1 need to DO? What does sentence 2 need to DO?" Then we wrote to the purpose. This meant when a phrase wasn't working, we could evaluate it against the purpose ("does this convey identity?") instead of just "does this sound good?" It made the iteration directional, not circular.

3. Options, not proposals

I consistently generated 5-8 options instead of presenting "the best one." You picked pieces from multiple options, combined them, and pushed further. The creative output was genuinely collaborative — neither of us would have arrived at "thrives in ambiguity, ships clarity" alone. That emerged from the selection pressure of seeing many options side by side.

4. Context injections that reframe

Several times you shared background that completely pivoted the approach:
- "The AI ambitions weren't undefined — there were TOO MANY ideas" → changed "undefined" to "sprawling" to "distilled"
- "It was operating in a couple months, not delivered at 6 months" → changed the whole timeline framing
- "I'm IC-focused, not management-track" → reframed every leadership bullet

These weren't corrections — they were context that made the framing more accurate. The pattern: when the output feels off, the fix is usually more context, not more wordsmithing.

5. Explicit locking

"Lock it, next." This prevented the infinite refinement loop. Once locked, we didn't revisit. This is critical for creative work — you can always make something slightly different, but at some point you have to commit and move energy to the next thing.

6. Review agents as external perspectives

Using agents to critique from a hiring manager viewpoint brought in concerns neither of us had (team sizes missing, "sole engineer" sounding like a loner, the testing bullet being a methodology statement not an achievement). The reviews were most valuable when they identified gaps in the story, not when they suggested rewrites.

7. Terse consistently won

Almost every iteration went from longer to shorter. "Staff Software Engineer — thrives in ambiguity, ships clarity" beat every 20-word version. The pattern: start with the full idea, then compress until the meaning nearly breaks, then back off one step. The compressing is where the punch comes from.

8. Capturing insights as they surface

We built talking points alongside the resume. Every time a background detail surfaced ("herding executive cats," "Professor Berns," "low-risk first strategy"), we captured it. The resume process became a vehicle for articulating the career story in ways that wouldn't have happened in a "write me talking points" session. The best insights came as byproducts of doing other work.

9. Separating content from presentation

We wrote in markdown, iterated freely, and only dealt with docx/formatting at the end. Then built infrastructure (YAML + generate pipeline) that let us change content and regenerate instantly. This meant formatting never slowed down content decisions.

10. Real signal over generic advice

The Amira hiring manager feedback was worth more than the entire best-practices doc we started with. Real evaluation criteria from a real decision maker > compiled advice from the internet. The pattern: whenever you can get real signal about how real people evaluate, it trumps everything else.


## Session Differences

The challenge is that what made this work wasn't a checklist, it was a mode of interaction. The CLAUDE.md can set the stage, but the real question is: what does a new session need to know to drop into this mode instead of the default "here's my best answer" mode?

Let me think about what was actually different here compared to a typical session:

* You were the decision maker, I was the option generator. In most sessions, the user asks for something and the AI delivers "the answer." Here, you were actively selecting, combining, and redirecting. That's a fundamentally different dynamic — and it produced better results because your taste and context were doing the filtering, not mine.

* We worked at the atomic level. Not "write me a resume" but "let's work on this one sentence." The granularity forced depth. When you work on one sentence for 15 minutes, you discover things about what you're actually trying to say that you wouldn't find in a full-document pass.

* I branched when you said "more." Instead of refining the same direction, I'd deliberately try different framings — lead with the action, lead with the result, lead with the environment, shortest possible. This prevented convergence on something mediocre.

* You shared the WHY behind corrections. Not "change this word" but "here's what was actually happening in that situation." That let me generate options that were more accurate, not just different.

## Overarching Pattern

But you're right that there's something bigger here that applies to the other two things you mentioned (the article series, coding sessions).

The pattern underneath all 10 of those points is really one thing: the human provides taste, context, and judgment while the AI provides breadth, speed, and optionality. When those roles get inverted — AI making the judgment calls, human just approving — the output is mediocre.

For the article series, this could literally be the framework you teach: "Here's how to interact with Claude Code so it operates at Staff level." The 10 patterns map directly:
- "Generate options, not proposals" → ask for 5 approaches to the architecture, pick the best pieces
- "Purpose before language" → define what a module/function needs to accomplish before writing it
- "Context reframes" → when the code feels off, share the business context, not just "try again"

For coding sessions — that's the most interesting one. Your spec-driven approach already gets at some of this. But the funnel pattern (explore multiple architectures before committing), the atomic-level iteration (one function at a time), and the "branch when asked for more" pattern could make coding sessions feel more like this one.
