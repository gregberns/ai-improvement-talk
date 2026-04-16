
## Symptom

"It's not following my project's conventions! Every time it's missing things or doing dumb stuff!"

Are you consistently yelling at your agent? 

Does it seem like every session is with a new developer where you have to explain you conventions, layout, or patterns?

## Change to Make

You need to spend time having your coding agent configure itself.

You're probably familiar with the `AGENTS.md` file, or corresponding `CLAUDE.md` or similar files.

There can be many of these files spread throughout your project - not just one in your root. These files are loaded into context when an agent opens a folder looking for a file.

Open your coding agent and run this prompt:

(If you're using something other than Claude Code, you may want to tweak it.)

> I need you to set up this project so coding agents can work effectively with it. Research best practices for agent configuration, then explore the project — understand the conventions, patterns, and structure across different areas. Identify where an agent would lack context or get confused. Ask me about any conventions or workflows I care about that you can't infer from the code. Create AGENTS.md files where needed, with CLAUDE.md symlinked to them. Use sub-agents to research different areas of the project.
