## Ideas

This repository started with some notes on a talk I presented to a dev team.

Its about how there are very discreet steps you can take to significantly improve your outcomes when working with AI Coding Agents - specifically Claude Code - but should work for all other coding agents as well.

There are quite a few things already there. There are also a couple other topics I've thought about in the mean time we'll want to capture.

We should start first by defining the 'mode' in which we want to communicate. Recently I had and incredibly productive conversation/session while writing a resume, and I'd like to see if we can replicate the pattern because of how effective it was.

Lets start by reading through the two files in `high-collab-session-notes` folder.
Those were a distilation of what worked, and hopefully patterns we could use in this session - and maybe even more important, work on refining, then release as part of an article or as a skill (or something).

I'd like your help to define the process we use. My first thoughts are:
* Start really broad, capture all the ideas, and get them documented
  * We need to figure out how to store these - I've found an 'append-only' model works really well
* We go through and add some context to each one - especially if the context/content around the idea is lacking
* Then put the ideas/subjects in a general order. The order is generally going to be based on the steps developers will want to implement them. 
  * Here's the challenge - this is kind of a tree based model - and we also want it somewhat linear. That means a developer should work through these actions step by step. If they are doing the thing already - then they can go to the next task. BUT - there are places where as ideas come up - we may want to add leaves to the tree. For example, there will probably a 'context management' section. We'll want to talk about clearing context regularly, tools to retain past information, tools to start a new conversation based on a past one, etc. But at some point we'll want to add anothe idea like - "How to prevent unit test output from consuming your context". If we don't think about that until later, we'll want to be able to inject that - without changing the structure of everything else - or having to change published material. This will be a critical thing to think through.
  * NOTE: In the high-collab notes - I think those ideas can be integrated into later articles. There are some really valuable ideas I think, especially in later steps. Also - in earlier steps, there may be a place for "If you are telling the model to modify a specific function in a specific file with a specific change - and thats your primary mode of operation - you may not be getting good results.". I know there are people out there doing that - we may want to address something like that - the challenge is that I don't know exactly what they're doing (Cause I'm not doing that anymore)
* Once in a general order we'll probably start from the simple first steps every developer needs to be taking - and probably isn't. We'll want to build out the ideas in each one, but probably not worry about polishing them - need to focus on the content and structure.
  * As ideas come up during that process, we'll want to either add them to a list we can review further later - or add them directly to the tree.
  * I think this is really where we need to focus on what the 'symptoms' devs are having, help point to a root cause, then suggest next steps to resolve these things.
  
* Once those are fleshed out, and we have a good chunk of them defined, then we can start refining and polishing. I think before I release anything, I'll want a good chunk of articles written. Then release one at a time, or 'promote one at a time' but then if someone wants they can go forward to more appropriate articles for where they are at.



Style or the way we're going to try to lay these out:
* Most of the ideas/articles/tasks should be or are going to be discrete actions a developer should take. We'll probably have some type of intro article about how this is a changing world and new things are hard - then we'll stop complaining and get down to actionable steps that can be taken. "Stop complaining, get to work :heart:"

Other:
* Where to publish - need to figure this out. But until the 'chunk' of articles is ready, I don't want to even discuss this.

Ok, theres quite a bit there. 

There may be some value in defining some type of methodology document, plus CLAUDE/AGENTS file that points to resources future agents need to know about.

Lets also get some type of task list where we can monitor where were at, whats needed, and that can be extended as we find more tasks and ideas to pursue.

Lets get started.
