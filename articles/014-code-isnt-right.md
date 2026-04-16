# The Code Isn't Right

You told it exactly what to do. Add a filter to the REST API. Wire up the new service. Refactor the auth flow. It did something — but not the right thing. Wrong approach, wrong patterns, wrong structure. You spent the rest of the day cleaning up after it. So you try again, more detail this time. Spell out every step. It still misses. You're writing more instructions than code at this point, and the code it produces still isn't what you'd have written. The more precisely you tell it what to do, the worse it gets.

**Why:** When you give step-by-step instructions, the model switches into execution mode. You said what to do, so it does exactly that — no judgment, no exploration, no broader reasoning. It doesn't ask whether your approach is right. It doesn't look at how the rest of the codebase handles this. It just executes your instructions, filling in the dozens of micro-decisions you didn't specify — which patterns to follow, how to structure it, what to name things, how to handle edge cases — with whatever interpretation it lands on. You think you gave complete instructions. You didn't. Nobody does. The model in execution mode doesn't ask. It just goes.

What you actually want is the model in reasoning mode — exploring the code, understanding patterns, figuring out the right approach, and writing its own implementation plan. To get that, you need to stop telling it WHAT to do and start telling it WHY something needs to change and WHERE the relevant code lives. Give context and intent, not steps.

**Fix:** Think of the agent as a new developer who just joined your team. You got a half-baked ticket from the PM. Your job: brief this developer. Tell them about the problem — why the change matters, what area of the codebase it touches, any constraints they should know about. Don't tell them exactly what to do. Let them figure it out.

Open a session and use this prompt, appending your own context about the change after it:

> Here's a change I need to make. Before writing any code: explore the relevant code and ask clarifying questions until you understand the full picture. Write a plan, then we'll dig into the details one section at a time. Once the plan looks good, write a detailed spec with implementation instructions and code examples to a file. Have an agent review the spec and fix any issues. Break the spec into ordered, discrete tasks in a file, have another agent validate them and fix any issues, then ask me before proceeding. Implement one task at a time. If I don't give you the reason for a change, ask if the context would be helpful. Here's what I need:

Then describe the problem. Not the solution — the problem. What's broken, what's needed, why it matters. Mention the area of the codebase if you know it. Add constraints. Then stop. Let the agent do what it's good at: exploring code, finding patterns, and reasoning through an approach.

**Your role:** Review the plan before any code gets written. This is where you catch misalignment — wrong approach, missed constraints, bad assumptions. It's dramatically cheaper to correct a plan than to untangle an implementation. If the plan doesn't match your mental model, say so. If you don't understand why it chose an approach, ask. Get the plan right first.

**How it works:** When the model writes its own implementation plan, it's done real work to get there. It's explored the codebase and found actual patterns. It's identified the files, functions, and conventions that matter. It's reasoned through the approach before writing a single line of code. The plan is in language the model understands — because it wrote it. When it then implements from that plan, it's following its own detailed reasoning, not your incomplete shorthand.

You're not writing more — you're writing earlier. And you're writing the right thing: context about why and where, instead of incomplete instructions about what.

**Resist the urge:** The hardest part is not dictating the solution. You know how you'd implement it. You want to say "add a method here, call it from there, update this file." Don't. Every time you do, you're pushing the model out of reasoning mode and back into execution mode. Give it the problem. Let it find the approach. Correct the plan if it's wrong. That's the loop.
