# Evolve Your Project Metadata

*This is a series about moving your coding agent from intern to senior developer. It's for devs who are already using agents but not getting the results they keep hearing about.*

*Each article targets a specific problem. What you're experiencing, why it's happening, and what to do about it — with a prompt you can run immediately.*

*The articles build on each other. If you haven't gone through the previous article, start there.*

In the previous article you set up your AGENTS.md files. You've got a base to build on. But you're not done — that initial setup was a first pass. Over the course of one day — maybe 10 minutes every hour — you'll want to spend fine-tuning that base. Essentially once a feature or once a session.

**Symptom:** You've laid the base, but it's still going to miss things — conventions it didn't catch, areas it didn't explore deep enough, patterns that only surface when you're actually working. The base needs fine-tuning.

**Why:** Every session produces signal — where the agent got confused, what it didn't know, what you had to correct. That signal is free intelligence you can use to learn about gaps in the agent's knowledge. We want to leverage those raw conversations to fill in those gaps.

The initial setup was a rough draft — what the agent could infer from one pass. Now you need to get your hands dirty. Use real sessions, with real friction, to start refining the configuration.

**This matters.** One day of tuning will make a world of difference. With the base config plus tuning, you should see the difference between an agent that's "ok" and one you can start relying on. Everything that follows builds on this foundation.

**Fix:** At the end of each session, have the agent review itself. Run this prompt:

Good session? It reinforces what worked. Bad session? It finds the gaps. Either way, your config starts to align with how you actually work.

Run the prompt below. Then read the rest while it works.

> Look back at this conversation. Identify where you lacked context or got confused, where you didn't follow project conventions, and where I could have communicated more effectively. For each issue, determine what metadata improvement — to AGENTS files, rules, or other configuration — would prevent it next session. Generalize the improvements — don't overfit to this specific conversation. Make the changes.

Do this for one day. 10 minutes per hour of coding. That's it.

The agent will update your existing AGENTS files, maybe add new ones in subdirectories it thinks need more context, or propose rules it thinks would help. Review the changes to understand: What did it find? Where was the gap? How is it addressing it?

**While it works:** Watch what it proposes. Push back on anything too specific — "always use `UserRepository` for the users table" is overfitting to one task. "Use the repository pattern for data access" is a real convention. The agent tends to parrot your exact words back as rules. Make it generalize.

And remember — you're part of this system too. Maybe part of the problem. Assume you're making mistakes. Assume there are anti-patterns you don't know about yet. Take that feedback seriously. You're tuning yourself, not just the config.

**How it works:** Every session produces friction. That friction is signal. The refinement process turns it into a deeper understanding of your structures, patterns, and practices. Each pass compounds. Every session starts stronger than the last.

**What's next:**

1. Commit the changes after each refinement session.
2. Keep working normally. You'll start to notice the improvements within a couple days.
3. After the focused day, you can dial it back. But when you hit friction, you'll know the move.

**Bonus:** Tell your agent to add this practice to your root AGENTS file. Something like: "When a feature or task is complete and the session hasn't been compacted, suggest a refinement loop — analyze the session for metadata improvements before ending." Now the agent reminds you to do it. The practice sustains itself.

**Not yet:** You'll notice patterns in what you keep correcting. Those patterns will eventually become rules, skills, or hooks. We'll get to those in an upcoming article. For now, let the metadata evolve.
