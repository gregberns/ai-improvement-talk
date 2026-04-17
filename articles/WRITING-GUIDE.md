# Article Writing Guide

## Article Format

### Front Matter

Every article starts with YAML front matter:

```yaml
---
title: "Article Title"
group: metadata|process|context|...
order: 1
idea: "005"
status: draft|review|published
---
```

### Formatting

- Preamble separated from body with `---`
- Group intro (if first article in a new group) separated from article body with `---`
- Section labels (`**Symptom:**`, `**Why:**`, etc.) on their own line, content below
- Cross-references use markdown links with relative paths: `[Article Title](./group-NN-slug.md)`

### Structure

Every article follows this exact structure:

1. **Preamble** — Shared series intro (see Preamble section below)
2. **Group intro** — (first article in a group only) Bridge from previous group to this one
3. **Opening prose** — Hook. Make the reader feel the pain. Empathetic, then direct.
4. **Symptom:** — The specific problem this article addresses
5. **Why:** — Direct diagnosis. Don't be indirect.
6. **This matters:** — (optional) For when the reader might skip the step. Emphasize why it's critical.
7. **Fix:** — Action first. Get to the prompt fast.
8. `Run the prompt below. Then read the rest while it works.`
9. **The prompt** — Copy-pasteable block. Key deliverable.
10. Expectation setting (how long, what to expect)
11. **While it works:** — What to do during the process
12. **How it works:** — Explanation (reader reads this while agent runs)
13. **What's next:** — Numbered steps, not a paragraph
14. **Bonus:** — (optional) Self-reinforcing practices, extra credit
15. **Not yet:** — Forward pointers to concepts not covered yet

Not every article needs every section. But the order doesn't change.

## Preamble

The preamble varies by position in the series.

**Entry point article (metadata-01):**
> *This is a series about moving your coding agent from intern to senior developer. It's for devs who are already using agents but not getting the results they keep hearing about.*
>
> *Each article targets a specific problem. What you're experiencing, why it's happening, and what to do about it — with a prompt you can run immediately.*
>
> *The articles build on each other. Start here and work forward. If you're not feeling the pain described, feel free to skip ahead.*

**Sequential articles within the same group (metadata-02):**
> *This is a series about moving your coding agent from intern to senior developer. It's for devs who are already using agents but not getting the results they keep hearing about.*
>
> *Each article targets a specific problem. What you're experiencing, why it's happening, and what to do about it — with a prompt you can run immediately.*
>
> *The articles build on each other. If you haven't gone through the [previous article](./link-to-previous.md), start there.*

**Articles in a new group (process-01, context-01, etc.):**
> *This is a series about moving your coding agent from intern to senior developer. It's for devs who are already using agents but not getting the results they keep hearing about.*
>
> *Each article targets a specific problem. What you're experiencing, why it's happening, and what to do about it — with a prompt you can run immediately.*
>
> *The articles build on each other. If you haven't gone through the previous articles, consider starting [at the beginning](./index.md).*

## Group Intro

The first article in a new group gets a bridge paragraph between the preamble `---` and the opening. It tells the reader what the previous group covered and what this group is about.

Example (process-01):
> In the previous articles we set up the agent's knowledge — project conventions, patterns, structure. Now we're shifting to how you work with the agent. The next few articles are about your process: how you communicate what needs to be done, how you verify the work, and how you make the routine stuff reliable.

Followed by another `---`, then the opening.

## Voice

- Direct, slightly impatient
- Empathetic about frustration, then blunt about the fix
- "We/our" for shared experience, "you/yours" for reader's specific problem
- Terse — compress until meaning nearly breaks
- No fluff, no blog-post energy
- Concrete examples over abstractions
- Don't be definitive about outcomes the reader hasn't experienced. "You should start to notice" not "you will see."
- End sections with a short punchy closer. "That friction is signal." "You're tuning yourself, not just the config." "You'll know the move." These land the point.
- Not accusatory — "you're a good engineer using patterns that worked for decades. They don't transfer cleanly." Respect the reader's learning capacity.

## Opening Energy

The opening varies by article type:

- **"You have a problem you don't know about"** (metadata-01) — frustration hook. Make the reader feel seen. They're experiencing pain and don't know why.
- **"You're not done yet"** (metadata-02) — forward momentum. Acknowledge where they are, push them to the next step. Not frustration — continuation.
- **"This is your daily experience"** (process-01) — frustration with a concrete example. Reader recognizes their own workflow. "Yes, this is my life."
- **"I thought we solved this"** (process-02) — deflation, not frustration. Progress was made, but something's still off. Quieter energy.
- **"Two steps forward, one step back"** (process-03) — mild exasperation. The hard stuff works now but the easy stuff keeps getting skipped.
- **Sequential articles acknowledge where the reader is coming from.** Ground the reader in what they've already done.

## Writing Process

1. Read the latest idea file (highest version) and any skeleton files
2. Lay out the whole article as bullet points — what each section needs to SAY (not prose)
3. Align on the arc before writing any prose
4. Write section by section: define purpose → generate 2-4 options → pick/combine → iterate → lock
5. After a draft: review agents check flow, logic, reader experience
6. Iterate. Nothing is locked until explicitly declared.

### Process Details

- **Compression is where quality happens.** The cycle: draft → "too wordy" → compress → pick. Almost every section gets shorter, not longer.
- **When the user gives raw ideas ("play with that", "something like that"):** take the intent and compose it. Don't copy his words verbatim, don't ignore them. Shape the meaning into clean prose, offer 2-4 options.
- **Print sections inline in the conversation.** Don't make the user read files — display content directly.
- **Review agents work best as three specific personas in parallel:** (1) flow/logic, (2) developer reader specific to where they are in the series, (3) writing guide compliance.
- **Prompts must work when run blindly.** The prompt is the product. Full pipeline stays in the prompt even if the article only explains part of it. Reader trust depends on producing good results.
- **Lean before the fix, depth after.** Keep everything above the prompt tight. The teaching happens below — in While it works, How it works.

## Article Groups

Articles are organized into named groups. Each group has a theme:

- **metadata** — Give the agent knowledge about the project
- **process** — Change how the developer works with the agent
- **context** — (coming) Session management and context hygiene
- **tying-together** — (coming) Specs, loops, engineering your process

Groups control file naming (`group-NN-slug.md`) and reading order. The `articles/index.md` defines group order.

## Reference

- metadata-01-setup-project-metadata.md — template for entry point articles
- metadata-02-evolve-project-metadata.md — template for same-group sequential articles
- process-01-code-isnt-right.md — template for cross-group first article (with group intro)
- process-02-it-missed-things.md — quieter opening energy, lighter article
- process-03-agent-wont-follow-process.md — builds on prior techniques, cross-references other articles
