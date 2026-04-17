---
title: "Set Up Your Project Metadata"
group: metadata
order: 1
idea: "005"
status: draft
---

# Set Up Your Project Metadata

*This is a series about moving your coding agent from intern to senior developer. It's for devs who are already using agents but not getting the results they keep hearing about.*

*Each article targets a specific problem. What you're experiencing, why it's happening, and what to do about it — with a prompt you can run immediately.*

*The articles build on each other. Start here and work forward. If you're not feeling the pain described, feel free to skip ahead.*

---

All we keep hearing is how amazing AI coding agents are. How they're going to take our jobs. Meanwhile, you're babysitting yours. It ignores your conventions. It rewrites code that already exists. It writes fifteen lines of new code instead of calling the function ten lines up. You fix it, explain why, and next session it does the exact same thing. These things can barely follow your conventions — they're not taking anyone's job. Right?

**Symptom:**

The agent's output is inconsistent. It follows your conventions in one area and ignores them in another. One session is great, the next is a mess. There's no pattern to when it works and when it doesn't.

**Why:**

Every time you start a new session, your agent is a new developer joining the team. It knows nothing about your conventions, your patterns, or how your project is structured. Day one — would any dev know that? No — you'd onboard them. Conventions, patterns, where things live and why. You're not doing that for your agent. That's what's wrong.

**Fix:**

Your project needs AGENTS.md files — properly structured and spread throughout the project. You almost certainly don't have any in subfolders. They're critical.

Run the prompt below. Then read the rest while it works.

Open a new session and run this prompt:

> I need you to set up this project so coding agents can work effectively with it. Research best practices for agent configuration, then explore the project — understand the conventions, patterns, and structure across different areas. Identify where an agent would lack context or get confused. Ask me about any conventions or workflows I care about that you can't infer from the code. Create AGENTS.md files where needed, with CLAUDE.md symlinked to them. Use sub-agents to research different areas of the project.

On a medium to large project, this will take a while. That's good — the more surface area it covers, the better. Some concepts in the prompt (like sub-agents) will be covered in later articles. For now, they're instructions for the agent, not you.

**While it works:**

Review what the agent produces. Correct anything that's factually wrong — wrong conventions, outdated patterns, things that don't apply anymore. But mostly, ask questions. Ask why it did something you don't understand. Does it add rules? What are they? Ask it. You're building a new skill — working effectively with an agent. Everything that follows builds on what you learn here.

**How it works:**

AGENTS.md is a cross-tool standard for agent configuration — most coding agents read it natively. Claude Code uses CLAUDE.md instead, so we symlink CLAUDE.md to AGENTS.md to get both.

Claude Code loads CLAUDE.md files hierarchically. It reads the root file at startup, then loads subdirectory CLAUDE.md files on demand as the agent works in those areas. This means the root file acts like a table of contents for the project, and deeper files provide localized context exactly when the agent needs it. The agent knows how to structure this — you don't need to dictate it.

**What's next:**

1. Commit the changes the agent made.
2. Get back to work. Use your agent like you normally would. It may take a couple sessions to really start feeling the improved consistency — don't expect miracles in the next hour.
3. Tomorrow, start practicing the process in the next article — tuning the base your agent just built.

**Not yet:**

If you ran into hooks, rules, skills, or commands — yes, they exist. We'll get to these in an upcoming article, where we'll use them to improve our frequent or more complex workflows. But if you want to explore them with your agent, go for it.
