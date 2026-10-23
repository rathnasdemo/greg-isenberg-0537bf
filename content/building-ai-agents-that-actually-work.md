---
schemaId: urn:gala:schema:content-frontmatter:2.0.0
schemaVersion: 2.0.0
id: 01a16924-c41c-72fb-b963-430d3de72574
kind: article
title: Building AI Agents that actually work (Full Course)
description: 'A beginner course on building AI agents: the agent loop, context files, memory, MCP and skills. My friend Remy walks me through building an executive assistant.'
language: en-US
authors:
- 01a16925-fde6-7282-8086-350fcd75ce35
tags:
- ai-agents
- claude-code
- skills
- mcp
- beginners
status: published
createdAt: '2026-03-17T12:00:00.000Z'
publishedAt: '2026-03-17T12:00:00.000Z'
slug: building-ai-agents-that-actually-work
hero:
  path: assets/content-building-ai-agents-that-actually-work-hero.jpg
  alt: Thumbnail of the video "Building AI Agents that actually work (Full Course)"
  role: informative
redirects: []
extensions: {}
---
*Adapted from the video [Building AI Agents that actually work (Full Course)](https://www.youtube.com/watch?v=eA9Zf2-qYYM)*

> **TL;DR:** AI is confusing, so I had my friend Remy explain agents in the simplest terms. A chat model goes from question to answer; an agent goes from goal to result by looping through observe, think and act. To build one, onboard it like an employee: an agents.md file for context, a memory file so it learns your preferences, MCP to connect your tools, and skills as standard operating procedures. Start with one role, then add more.

I think AI is confusing. There, I said it. There are a lot of terms, such as skills, MCPs and agent harnesses, that are difficult concepts to understand. So I had my friend Remy come on the podcast and explain it in the most simple terms possible. In this free course on how to master AI agents, he breaks down what each piece is, how they connect together, and the simplest ways beginners can start using them today.

I begged Remy to come on. He has structured his company so that folders and .md files run it. What I asked him to do was teach beginners how to do the same: set up their own executive assistant, head of marketing or chief financial officer, and explain the concepts behind all of it. His promise was that by the end you will know how to build agents that run complete departments of your life and company within any agent platform you choose.

## Chat is question to answer, an agent is goal to result

*[Watch from 2:11](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=131s)*

Remy's view is that the AI landscape is moving into stage two, from chat to agents, and most people are being left behind by using only chat models. He said that founders and employees who use agents are, no word of a lie, 10 to 20 times more productive in their day, and that stacks up over days, weeks and years.

The word agent is thrown around so much online that it has lost a lot of meaning, so he gave a clear definition. A chat model is question to answer: you ask, the AI replies, then you do the work. An agent is goal to result: you give it a task, it plans, executes and delivers a result. The way I think about it, chat is ping pong, back and forth, and with an agent you give it a goal and hope it gets closer over time. Remy said that is exactly it, and that it is a nice way to lay it out in your head: chat is question to answer, agent is goal to result. When you chat to an agent, you might give it a task like build me a website for some company, and it goes away, does its work and outputs the website to you.

## The agent loop: observe, think, act

*[Watch from 3:28](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=208s)*

If you tell an agent to build a website, it goes away and outputs the site. What happens inside that step is called the agent loop, with three parts: observe, think and act.

Remy's example was the prompt "build me a minimalist portfolio site" for me, given to a blank agent with no context. It loads the prompt and checks for files in the workspace. It thinks about what to do next, and decides to research who I am, because it does not know. It feeds the research back into the observe step, then decides the next step is to write a plan. It feeds the plan back in, then writes the code, and it keeps going through the loop as many times as it needs until it can conclude that the task is complete. It knows it is done based on the parameters you set in your prompt. The point Remy wanted to land is that this loop is what is actually happening inside the step where the agent is working, and it is why the agent can go as far as it needs without you pushing it forward each time. If you give it a research task, you might say compile 10 sources and create a report as a PowerPoint, and once it has done that, it can conclude the task is complete.

## The four parts of an agent, and what a harness is

*[Watch from 5:37](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=337s)*

An agent is made up of four components:

- **The LLM.** The brain behind it: think Claude Opus 4.6, GPT 5.4 or Gemini 3.
- **The loop.** It keeps going until the task is done instead of stopping after one response, so you go from ping pong to not having to babysit it.
- **Your tools.** It connects in all your tools.
- **Your context.** It connects in all your context.

A platform that facilitates this loop is known as an agent harness. All the popular AI agent platforms on the market are just agent harnesses: applications where this loop is facilitated.

## Watching the loop run in three harnesses

*[Watch from 6:30](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=390s)*

Remy prepared three demo folders and opened Codex, Claude Code and Antigravity, each with the same prompt to build a minimalist portfolio site for me and spin it up in a preview. He compared the folders to the projects feature in chat models like Claude and ChatGPT: a project holds your chats, your uploaded sources (your context) and custom instructions that tell it how to behave, which is a system prompt. The difference is that with agents the project is a folder local on your computer.

In Claude Code, he said, you can see the loop best. It decided to launch an agent to research me, using Perplexity, which he has connected as a tool via MCP. Then it fed that back into the observe step, wrote the HTML file, spun it up on a local server, and for the last iteration of the loop opened the site, took screenshots and reviewed them to check the site was complete. Antigravity showed its thinking too, examining the directory to see whether a project existed and then building the site with a localhost preview. The result was a nice, minimalist portfolio that I would totally launch. It had the wrong email address and said I live in South Canada, which I no longer do, so there were a few copy things, but it did a pretty good job. Remy and I both preferred the Gemini version. Codex had finished its own somewhat similar site. The Claude one was still going when he checked, and when it finished it was very similar to the Gemini one. Remy said the point of the demo was to show how the loop works in real time, and that all of these apps are different flavors of the same thing.

## Security: scope what the agent can access

*[Watch from 8:39](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=519s)*

I asked how people should think about security with these products. Remy thinks of it as scoping what the agent has access to. He said it comes down to what you feel comfortable giving the agent, and he built one the other week that manages Meta ads. By default Antigravity, Claude Code and Codex are very secure because they are built by massive companies with a lot on the line. For an agent that manages something risky, such as Meta ads and their budgets, it comes down to what you feel comfortable giving it. You can control its tool permissions so that if it were compromised, the worst case is not that bad, for example by giving it read-only access to important platforms. OpenClaw is another harness, but he called it the wild west, and he wanted to come back to it at the end.

## Learn to drive, then jump in any car

*[Watch from 9:58](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=598s)*

Remy's analogy: what we learn today is how to drive. You learn how the steering, pedals, brakes and handbrake work, and then you can jump in any car, whether it is an old Toyota or a Range Rover, and inherently know what to do. Remy told me the harnesses are different cars. Some have better features like seat warmers and cruise control, but once you know how to drive, you can use any of them.

Watching the demo, I wondered how many people would benefit from a very clean website, and how you could set up agents for a cold email loop: "I built you this website, do you want it? It's going to cost $250." Remy said that is a great idea, pre-making websites for companies and mass cold emailing them an off-the-shelf offer.

## Onboard the agent like a real employee

*[Watch from 14:44](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=884s)*

Remy showed that his workspace has a folder for each company or client, folders underneath for heads of departments, and within those the skills, MCPs and context, with an overarching agent at the top to manage them. Today the focus is an executive assistant that takes care of your manual day-to-day tasks and frees up at least 1 to 2 hours extra per day. It runs off local files, so he created a folder called executive assistant.

His way of thinking about building agents is onboarding them like a real employee. A real executive assistant could not just show up and take a task without you explaining your business, your clients, what you do and your tools. He worked in Cowork, another agent harness that does the same thing, because he thinks it has a simple UI that shows what is going on, and you can follow along in Claude Code, Codex, Antigravity or any harness. When he asked it to write a cold email, it had no context at all and asked what he even sells. (He dictated the prompt with a voice-to-text tool called Monologue; he said there are a lot out there, and I said mine looks really good.)

## Agents do not have memory unless you set it up

*[Watch from 17:44](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=1064s)*

One thing that might be a shock when moving from chat to agents is that memory works differently. If you open a fresh chat in ChatGPT or Claude with no files and ask "who am I and what do I do?", it will know a scary amount about you, because chat models have memory built in that saves things to the cloud where you cannot see or control it. With agents you have to set up memory and control exactly what you give it. Remy thinks that is a benefit, not a limitation: with auto memory, if you have talked about three different companies and relationship advice, then ask for landing page copy, it may pull in context from places you do not want.

## The agents.md file and context engineering

*[Watch from 19:28](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=1168s)*

The fix is a context file called agents.md. It is like a system prompt, like the custom instructions field in a custom GPT or a project. It is always on, and holds things like the agent's role, context about you and your preferences for working. Every new session, before it answers your query, it loads this context as part of the observe step of the loop. In Claude Code the file is called CLAUDE.md, in Gemini it is GEMINI.md, and in Codex or OpenClaw it is agents.md. It is the same concept: a file in the folder that the agent loads in before it starts working. If you title it correctly, the agent knows automatically to load it.

Remy had prepared one with all about him, what his business does, his working preferences and the tools he uses and for what, such as Notion for project management and Stripe, plus his ideal customer. If you want to make one, you can ask Claude chat or Cowork to interview you with questions to extract all the context, then build the file. After he dragged it into the folder, the same prompt, "write me a cold email", worked with all that context. I called it basically a reminder file, and Remy said pretty much: it loads in all this set context before you even start working.

This is the big shift from chat to agents. Prompt engineering used to be the thing, with its ultimate prompt for going viral. Now it is about context engineering: how well you can load your agent with information about your business so the prompt can be stupidly simple, like "write me a cold email", and you still get an amazing result. It was already asking whether the email was for a brand or sponsor, a potential partner or a consulting client.

## Bigger context: a context folder, and one file per role

*[Watch from 23:01](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=1381s)*

If you have a lot of context, Remy sometimes creates a folder called context with separate files about him, brand voice, ideal customer profile and so on. To keep the main file smaller, he writes in the CLAUDE.md to read the context folder before answering questions or doing any task. By default a context file sitting in the folder will not be loaded unless the CLAUDE.md tells the agent to check it. A lot of people have done this with Obsidian, telling the agent to check their Obsidian vault, their second brain, for context.

That is how you onboard an agent to your business. For a head of marketing, the file would look similar but begin with "you are my head of marketing", how it speaks, and its tasks and roles.

## Memory: the self-improving loop

*[Watch from 24:18](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=1458s)*

The new problem is that the agent does not remember the intricate details of your preferences across sessions unless you manually update the CLAUDE.md. Remy told it that his favorite color is lavender, and it said noted. In a new session in the same folder, it had no idea. The same happens if you tell a head of sales never to sign off emails with "cheers" but "warm regards": it says noted, then the next day does the same thing and you think your agent is broken. It is not broken; it is running off context files in the back, and unless you manually update them it will not know to save that preference.

So Remy adds a snippet at the top of the agents.md. It says to read all files in context, read memory.md (what you have learned over time), and when he corrects the agent or it learns something new, to update the relevant section in memory.md, keeping it current and replacing outdated info. He created a memory.md file with just the section headings. I said that memory.md is basically just what it sounds like, and that if the goal is AI employees that do things for us, they need to remember our preferences, and a good employee does and compounds that learning. Remy agreed: if you try Cowork and are not getting good results, a big part is often that you do not have a CLAUDE.md and a memory.md set up.

He noted that some harnesses, like OpenClaw, have a memory system built in that does the same thing under the hood, but it is still important to understand it. In a new session he said his favorite color is lavender, and the agent saved it to memory. For an executive assistant, the memory might hold how to sign off emails, or not to connect with clients on Slack because he wants client communication on email. For a head of marketing it might be how he likes ads structured in Facebook Manager; for a website or app folder, it might be "don't use dark mode". These rules compound, and the number of errors goes down.

## Will the memory file get too big?

*[Watch from 30:25](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=1825s)*

I asked whether memory files get so big that they become ineffective. Remy has not hit that threshold. The best practice for these Claude MD files is to keep them to no more than 200 lines. If you built one up over years, the rules might start stepping on each other's toes and you could do a manual clear. He would not worry too much: if it is saving the tiniest corrections, you can update the CLAUDE.md to say only save substantial corrections. Once it is set up, if you say "quit writing so formally", it does the task and then updates its CLAUDE.md to keep the tone casual, never formal, and keeps that in every new session.

## MCP: connecting your tools

*[Watch from 31:45](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=1905s)*

With memory and a role set up, the next step is to connect tools. By default most harnesses only have web search baked in. To link Gmail, calendar and the rest, where the real productivity gains are made, you use MCP. Remy took his explanation from when I had Ross on. Before MCP, an agent had to learn each tool's language: Claude speaks English, Notion speaks Spanish, Gmail French, your browser Japanese, Slack Chinese. It could connect, but it required extensive custom development that took a long time. Anthropic built MCP to sit in between as a translator that speaks every language, translating calls from the agent to the tool and back. It is an easy, standardized way to connect tools.

In Cowork you go to connectors, browse them, and add them: there are hundreds of the biggest apps, and you sign in. He said Codex would be the exact same, with its skills and settings, and the other harnesses he showed let you connect your tools in the same simple way, as does Perplexity Computer with its connectors. It is all the model context protocol. He had already connected Gmail, Google Calendar, Granola, Notion and others.

## An AI operating system in one place

*[Watch from 34:22](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=2062s)*

Remy then opened the executive assistant folder in Claude Code, inside Visual Studio Code, to show that all these harnesses are the same and work off your local files. He said the real future-proof AI stack is having markdown files on your computer, because markdown is the easiest format for an agent to digest compared to a docs or PDF file.

He thinks everyone will have an AI operating system that compounds over time, with personal agents and agents for each department, and people will not use the apps anymore. He has connected Gmail, Google Drive, calendar, Granola for meeting notes, Stripe for payments and Notion for project management, and he does not even enter these tools any more; he sits in Claude Code as one central place.

For a demo he emailed himself as a fake prospect and added a fake meeting in Granola. First came "summarize my inbox from today", one of the most basic agent tasks ever. I asked how valuable that is; he said the value is having the tools connected in one place without switching and copy-pasting context. Then he asked it to review the meeting notes from today, draft the email sending the proposal, create the Stripe payment link and set up the project in Notion. It went into Granola for the meeting, Stripe for the payment link and Notion for the project, and created a draft in Gmail ready to send. I said this is really a new way of working, and Remy agreed that it is so new. Even a simple task like sending an email based on a call, with a proposal link, done seven times faster without going into all these tools and copying meeting notes into a page to give it context compounds: you start to fit a week in a day and seven weeks in a week, and stacked over a year you are miles ahead.

Remy added that every time he does a process, even by manually prompting it like this, and knows he will do it again at some point, he turns it into a skill. If you automate three to five tiny manual processes each week with skills, you eventually automate your entire life with agents. He mentioned a tweet from Cody Schneider, whom I had on the pod the other week, saying that in the future everyone will have an AI operating system like this, and you will have the 100X employee because everyone comes into their role with one and builds skills for every manual process.

## Skills are SOPs for AI

*[Watch from 40:04](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=2404s)*

Remy's easiest way to think about skills: SOPs, standard operating procedures, for AI. Once you explain something once, you never have to explain it again. Without skills, creating a proposal means going back and forth: change the formatting, use this blue, put the price at the bottom. After 15 minutes or half an hour you land on a proposal you like. The next week, unless you find the same session, it has forgotten everything, and even with memory set up, this kind of thing does not belong clogging your memory. A skill packages the process into a .skill file, a markdown file explaining the exact process you went through, so every proposal comes out the same way.

I asked what the difference is between a memory.md and a skill, and whether a skill is just a memory.md for a particular job to be done. Remy said pretty much exactly. The skill file is basically like your memory.md, explaining the exact process for one task. All the agent harnesses now have skills as a feature. Locally they live in a hidden .claude folder. His writing-viral-hooks skill has a skill file explaining the process, plus packaged references such as hook formulas.

## Two ways to create a skill

*[Watch from 43:08](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=2588s)*

There are two ways Remy finds useful:

1. **Start from source material.** For viral hooks, he had a course, transcribed it, put the full transcript into Claude and said to build a viral hook skill based on it. All the major harnesses have a skill creator skill, which is skill-ception. He uses the result for his content team folder. The references folder was created by the agent on its own.
2. **Do the process once, then package it.** Go through the task manually once with Claude, and if you know you will do it again, say "create a skill for what we just did".

## Building skills live

*[Watch from 45:18](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=2718s)*

Remy suggested a daily brief skill that summarizes your calendar, inbox and Notion projects and plans your day, which you can run as a scheduled task at 9:00 a.m. every morning. For a live example, he asked the agent to draft an email referring the fake prospect to his friend Sebastian, who has an AI automation agency, using the Granola notes and contacts. It is a tiny manual process that might take 15 minutes of his day, so he told it to use its skill creator skill to create a Sebastian refer skill that knows what to do and has his email address. If that saves 15 minutes another five or six times, it starts to compound when you do this for every little process in your business. I said we should ask ourselves what the jobs to be done are in our day and what the repetitive processes, or SOPs, are, and set up as many as possible.

## A bigger setup: the content team and an ads analyst skill

*[Watch from 47:54](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=2874s)*

Remy showed the folder structure from the start of the video. His content team folder is a more elaborate version of the executive assistant: a CLAUDE.md that tells it that it is the main orchestrator with sub-agents, and a skill for Meta ads analysis. This is the kind of process a marketing agency owner can take inspiration from: taking competitors' ad libraries and breaking down all the creatives and landing pages.

He pastes in an ads library URL and clicks run. In the example he did the day before on a very large e-commerce brand, it took screenshots of the landing pages and scraped all 220 of the ads the brand was running. It then did a deep dive on every ad, with visual analysis, copy analysis, why it worked and what could be improved, plus a master report. When he ran a marketing agency, that manual process would have taken him three or four hours. To build the skill, he went through the process once in a fresh session with Claude for two hours, then said to use the skill creator skill to package the whole process as a skill. Now whenever he wants to run that process again he can invoke the skill and it knows what to do. I called it crazy, and Remy said absolutely crazy. The Sebastian refer skill is now live too: whenever he wants to refer someone to Sebastian, he can just ask and it uses that skill. It is the tiniest process, but you build these up for all the little tasks you do day to day, and it compounds and compounds.

## Chaining skills and scheduling them

*[Watch from 50:30](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=3030s)*

Remy said he can already think of an idea here: you can chain skills together and build some really cool workflows. He sees skills chaining together. A meeting prep skill researches the guest and compiles talking points. A podcast research skill could do that for my guests. A morning brief skill could say that if there are meetings or podcasts in my day, it should use the podcast research skill. Harnesses are also adding cruise control: in Cowork or Claude Code you can schedule a task such as "run my morning briefing skill" every morning at 9:00 a.m., and it becomes an automated workflow.

I told him I do this right now. I am buying a new car in a particular color and feature set that is hard to find, so every 3 hours an agent scrapes the car marketplaces and notifies me when something comes up. Otherwise I would spend an hour a day refreshing CarMax, cars.com and Autotrader like an insane person. Remy said that would be a good executive assistant skill. His own more elaborate ones include a weekly research skill for his newsletter team that runs every Thursday morning and scrapes Twitter and Reddit for what is new in AI. Combine skills with MCP so the agent can use your tools, and you can train it on all the processes in your business.

## An OpenClaw Meta ads buyer

*[Watch from 53:12](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=3192s)*

Remy built an OpenClaw agent to manage Meta ads that went pretty viral, using all these concepts. OpenClaw works the same way: it operates off an agents.md in a .openclaw folder instead of .claude, plus a memory.md and other files such as a soul, which gives it its personality, and an identity, which tells it who it is. It is the same idea of markdown context files, connected tools and skills.

He planned it out with Claude, asking it to help write the agents.md telling the agent it is his Meta ads media buyer and what processes it does. Then he created skills, such as an ad creative skill so it knew to look in the Dropbox folder and create creatives, and a copywriting skill, for probably around 15 skills in all. He combined scheduled tasks, which are cron jobs, with the skills and context files and gave it the tools it needed. It was the same process as the executive assistant.

## Which harness should a beginner use?

*[Watch from 55:25](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=3325s)*

I asked whether beginners should use OpenClaw or Cowork and the others. Remy said OpenClaw is probably one of the hardest to learn and set up, and Claude Code is probably the easiest. Perplexity Computer, which I did a video on, is pretty simple too. He would get comfortable with Claude Code or another of those first, and build out all the processes there first. For the executive assistant, over the next 2 weeks he might build skills like the Sebastian refer skill, a daily brief and meeting prep. Once he is happy with how it functions, he could migrate it to OpenClaw for its more autonomous nature. There is no right or wrong way to run these: he has one built for each other department of his business, and for the other businesses he works on.

## Global versus project level

*[Watch from 56:41](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=3401s)*

One last concept is global versus project level. Skills added at a global level apply to every project you work in. Remy has a truncate skill that shortens something by removing sentences that do not need to be there without compressing the ones that remain, and he wants that in every session, so it is global. The Sebastian refer skill he would not want with his head of marketing because it plugs up the context, so it is project level. The same split applies to CLAUDE.md files and to MCPs: global and project.

## Wrapping up

*[Watch from 58:01](https://www.youtube.com/watch?v=eA9Zf2-qYYM&t=3481s)*

Remy's summary of the whole crash course: it is a loop running in the back end to complete your task, with your tools, your context and the LLM connected in one place. To start, work out what roles you want to build an agent for, then go into Claude or your favorite chat model and have it help you build the context files through an interview-style process by saying "ask me questions to build this out". Connect all the tools you need, then build skills through daily use. Pretty soon you will have powerful AI agents for every aspect and department of your business.

*[Watch the full video on YouTube](https://www.youtube.com/watch?v=eA9Zf2-qYYM)*
