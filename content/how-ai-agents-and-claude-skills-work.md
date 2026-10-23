---
schemaId: urn:gala:schema:content-frontmatter:2.0.0
schemaVersion: 2.0.0
id: 01a16924-c2ad-7f5b-8ca2-2cd72394dacf
kind: article
title: How AI agents & Claude skills work (Clearly Explained)
description: Skip the big AGENT.md file and build your own skills by teaching the agent a workflow step by step. Ross Mike shows me how context works and why less is more.
language: en-US
authors:
- 01a16925-fde6-7282-8086-350fcd75ce35
tags:
- ai-agents
- claude-skills
- context-window
- agent-workflows
status: published
createdAt: '2026-04-08T12:00:00.000Z'
publishedAt: '2026-04-08T12:00:00.000Z'
slug: how-ai-agents-and-claude-skills-work
hero:
  path: assets/content-how-ai-agents-and-claude-skills-work-hero.jpg
  alt: Thumbnail of the video "How AI agents & Claude skills work (Clearly Explained)"
  role: informative
redirects: []
extensions: {}
---
*Adapted from the video [How AI agents & Claude skills work (Clearly Explained)](https://www.youtube.com/watch?v=S_oN3vlzpMw)*

> **TL;DR:** Ross Mike joined me to argue that the models are now good and context is what decides quality or slop. About 95% of people do not need an AGENT.md file because it burns tokens on every turn. Skills load only a name and description until needed. His method is to walk the agent through a workflow by hand, then have it write the skill, then fix it recursively. Start with one agent, add sub agents later, and keep the context window light.

I had Ross Mike back on the pod. His promise for the episode was to share some wisdom on how you can use agents better. There is a lot of information going around right now, he disagrees with most of it, and that is what we talked about. Whether you are building something or using an agent for work, the goal is the best outcome possible.

Anyone can follow along. It is a lot of diagrams and the basics, made easy to understand.

## The models are good, so context is what matters

*[Watch from 0:50](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=50s)*

Ross opened with the point he thinks previous episodes might have disagreed with: the models are now exceptionally good. He called Opus 4.6 amazing and GPT 5.4 amazing. There are two camps, especially in programming, with some saying Opus is the better UI designer and GPT 5.4 the better back end. Generally, he said, we have reached a point where the models are good. We are not at AGI yet, but context still matters, and you have the power to steer the models toward quality or toward slop.

## How context gets assembled

*[Watch from 1:17](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=77s)*

Context is the model assembling the information it needs to execute an action. In a coding agent, and really in any agent, that starts with a general system prompt, usually written by the model provider. Ross got to read the Claude Code system prompt when it leaked recently. It guides the model on how to act, what to do and what not to do.

## Why 95% of people do not need an AGENT.md

*[Watch from 1:43](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=103s)*

Many people also have AGENT.md or CLAUDE.md files. Ross said off the bat that 95% of people do not need one, because you have to assume the models are already good. His analogy: telling me every time we shoot a podcast that I need a microphone. If he is building a website with Claude Code and tells it that the code base uses React, he does not need to, because the code base is in context and it can check the code.

A lot of people put the onus on the harness and the context building. He is starting to strip things off and going super minimal. He added that he has not been acquired and none of these companies are paying him.

When I asked about the other 5%, he said it is proprietary information, such as something specific to your company or a methodology specific to you that has to be referenced in every single conversation. The annoying part of an AGENT.md is that every time you go back and forth with the agent, the file is added to the context. A thousand-line CLAUDE.md might be 7,000 tokens, and you spend 7,000 tokens on every run. It probably should be a skill, and wasting tokens in every single turn is the reason he is not a fan.

## Skills and progressive disclosure

*[Watch from 3:28](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=208s)*

Skills are designed around what is called progressive disclosure. A skill file looks like a name, a description, and underneath a bunch of information. Only the name and description are added to the context, not the rest. So you have two sentences instead of an AGENT.md with a thousand lines: thousands of tokens compared to a couple hundred.

Say you have a Notion report skill and you tell your agent to create a Notion report. It checks its context, sees it has that skill, and then reads the entire document. The name and description are enough for it to realise it needs the skill. Ross called himself a skills maxi, and said people do it wrong. If you have a certain way of generating a report or structuring code, why put it in the AGENT.md when the agent can call on it progressively when it needs it?

## What fills the context window

*[Watch from 6:03](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=363s)*

So far the context holds these pieces:

- **System prompt.** The general instructions from the model provider.
- **AGENT.md.** Added on every turn.
- **Skills.** Just names and descriptions.
- **Tools.** Claude Code has built-in tools such as the read tool and the write tool. They have to be in the context because the model does not call the tools; the agent harness around it does.
- **The code base.** A web app or mobile app. Ross said that if you are not technical, you really shouldn't care about the specific framework.
- **The user conversation.**

At the beginning this might be 20,000 tokens, and as the conversation grows you might reach a limit of 250,000 tokens. That is when both Claude Code and Codex compact.

## Teach the agent the workflow before you write the skill

*[Watch from 6:56](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=416s)*

Ross's example is his YouTube channel, which now gets sponsor emails, many of them not worth the time to comb through. He has an OpenClaw agent with its own email address. He did not give it access to his own email because there are attack vectors and he has been hacked before. Every time a sponsor emails him, he forwards it to the agent.

The first time, he told it to check every 15 minutes, research the sponsor and say whether they are worth it. Every email came back legit, legit, legit, perfect, perfect. There was no rejection and no deep research. So he realised the model needs a step-by-step guide, which is when you create a skill.

The mistake a lot of people make is to identify a workflow and jump straight to creating the skill. Ross said that is the worst thing you can do. Imagine hiring an employee or mentoring somebody: you tell them what to do, help when they ask, ideally let them fail and then tell them how it is done. There needs to be experiential learning. He now has a 100% hit rate because he walks the agent through the workflow step by step. For the sponsors he said: here is an email, tell me about the company, check their Twitter, check their YouTube, check their Trustpilot, check whether they raised any money. If two of these do not exist or are not in good standing, it is an automatic rejection. The agent checked, said he was absolutely right, and marked "no contact" in the Google Sheet.

## Why the agent needs to be walked through it

*[Watch from 9:58](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=598s)*

I said it is frustrating that a task seems so binary, and then when you ask why it did not look at Trustpilot, it says you are absolutely right. Ross's explanation is that the models do not actually think. They are predictors of tokens. When you give it English, it maps it onto a vector graph and looks for the closest resemblance. Ask for the capital of France and Paris is close by, so it gives you Paris. It feels like it understands, thinks and even has emotion because it has been trained on so much data, but it does not know how to think.

That is why he walks with it. He told it how to research, the research became part of the context, then he told it what qualities to look for in a good company and to send him an email when it is really good. Only after successful runs, again and again, did he convert it to a skill. Many people have the AI create the skill without the context of what a successful run looks like. Especially with OpenClaw, it will probably fail at the API call or get the data wrong. Ross's line:

> It will mimic you perfectly, but you've given it nothing to mimic.

His updated process is to identify the workflow, go back and forth and teach it, then tell the AI to review what it did and create the skill. He does not handwrite skills, and there is even a skill to create skills: skill inception.

## Do not download other people's skills

*[Watch from 12:34](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=754s)*

This is why Ross does not install skills such as a Notion skill or a social media skill. He will review them and even give them to his AI to see what can be learned, but he does not download them, because the agent needs the context of a successful run. Skills marketplaces are also an easy way to attack somebody, so be very careful with some random person's skills. The best way to create a skill is to work with the agent in your specific workflow, and after a successful run tell it to review what it just did and create the skill.

I said that this is how you would treat a hired employee: map out a workflow, identify what is right and wrong, do it iteratively, and once you have got there, codify it.

## Treat agents like new employees and scale for productivity

*[Watch from 13:51](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=831s)*

Ross agreed we should treat models like very new employees, not black magic boxes that know everything. They have been trained on a lot of data, but they do not know your workflow or your steps. He sees people set up OpenClaw with 15 sub agents and 30 skills without having set up their own workflows. There is a perfect time to use sub agents and he uses them a lot, but he calls his approach scaling for productivity, not for what looks cool.

He likes one popular agent setup he tried, but thinks people would be more productive building their own version from scratch. I said he is asking people to do the work, and he said 100%. If you want to scale for productivity, it starts with one agent and you building up the skills. Then you add a sub agent, and your one agent manages multiple agents. It is like starting a company with 10 employees on day one without ever having managed a team. He apologised that it is not sexy, but you have to put in the work and build it up.

## Human skills and the permanent underclass

*[Watch from 16:28](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=988s)*

Ross believes you are building your personal human skills, not skill.md files, and that as models and agents get better you become more valuable. As long as there is no new paradigm, LLMs just predict tokens and do not understand the way we do. The job scene is scary, but he genuinely believes that anyone who knows how these tools work, how to build agents, craft skills and make them productive is in for a good run.

I asked whether that means you will not join the permanent underclass. As we both understand the term from Twitter, it is the idea that once AGI comes, all white-collar workers lose their jobs, and if you do not know how to build skills and use AI you join the permanent underclass. Ross said it is ridiculous to call it permanent. Knowledge that took 20 people 20 years to acquire is now 20 bucks a month, which is a huge shift. He mentioned a non-technical person who vibe coded a whole app and hit a hundred million dollars; I jumped in and said 1.8 billion, USD, not Canadian carny coins. The takeaway I drew was that I overthink things. I need to drop the thing and release it, and there is wisdom in a level of delusion that this will work out and if it doesn't, it is onto the next one.

## Code is context, and templates come back

*[Watch from 18:40](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=1120s)*

Ross's recap: you do not need an AGENT.md unless you have something proprietary. Skills are valuable, but build your own, like his mom telling him as a kid that they have food at home. On the coding side, model companies have realised that agents are really good at writing code, particularly TypeScript, which is why you see advances like Claude Cowork and OpenClaw. Under the hood they write code and call APIs.

So for a project you do not need an agent file listing your tech stack, like React or Next.js and a database. Unless you have a specific workflow, it is unnecessary, because code itself has become context. The more important thing is a solid foundation. Templates used to be big and made people lots of money, and Ross believes they will have a renaissance, because a solid template for a web app or mobile app becomes context for the agent to build on. He needed no large AGENT.md or CLAUDE.md, just minimal context usage and skills.

## Recursively building skills

*[Watch from 20:25](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=1225s)*

His methodology is recursively building skills. After you set up a workflow with an agent and turn it into a skill.md, the agent will still mess up at some point because there are gaps in the skill. When it does, you work with it again:

1. **Find out why it failed.** Ask the agent what error it got. It will tell you descriptively, for example an error saying you have insufficient credits.
2. **Pass the failure back.** Tell it where it failed and to fix it. It writes code and does whatever it does.
3. **Update the skill.** Once it works, tell it to update the skill so this does not happen again.

Ross has a report generator for his YouTube channel that calls Notion, YouTube Analytics, Twitter Analytics and others, pulling from eight data sources. No single prompt would get the agent to do that, but now it executes the workflow flawlessly in about 10 minutes, because he went through five loops of recursively building the skill. If skills marketplaces become a thing, he thinks people will sell really well-defined, step-by-step skills, since most people create them without having built out the workflow with the agent. When the agent messes up, don't complain. It is a moment to identify the error, tell it to fix it, then tell it to update the skill file.

## Expect two weeks of early investment

*[Watch from 23:04](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=1384s)*

I said this is about shifting your expectation, because people assume it will work at the start. Ross agreed: there is an early investment that sucks, that nobody tells you, especially the agent harness companies, because they would not raise as much money. He would give it two weeks, since that is how long it took him. When he first set up OpenClaw he thought it was garbage and confusing, until he went lower level and realised that models and agents do not think like you and me.

If I asked a new colleague for a report on the financials in Notion, they would not know where to start, whereas someone with context of the business would. We brought up the episode of The Office where a new boss asks Jim for a rundown and Jim spends the episode asking around what a rundown is. Jim did not have the context. It goes back to the initial point: the models are really good now, but context matters more than anything.

## Start with one agent, add sub agents later

*[Watch from 25:41](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=1541s)*

Large agent companies and sub agents may work, but probably not for you off the bat, because you have not built up to that point. Ross started with one main agent that did everything: checked his spreadsheet, checked his sponsor email and so on. Once he had predefined workflows, for instance for working with sponsors, he could have a sub agent for the marketing work, with its own skills and context. It makes sense for him to have sub agents now. He has five: one for marketing, one for business, one for personal, and so on. He said:

> I didn't scale for what looks cool, I scale for productivity.

He is willing to bet that his system is more productive than anyone else's, going OpenClaw to OpenClaw. I said we have to clip that.

## The harness and tools matter, less is more

*[Watch from 26:58](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=1618s)*

Ross's closing point: the models are good, and the context plus the harness matters. He mentioned a benchmark, which he does not fully support, that found a difference in output quality between Cursor, Claude Code and Codex. To him that shows the models are really good and will probably get better, but the harness, the tools around it and the context you give it matter even more. Less is more: build up step by step and make it productive for you before adding the shiny new thing. If people took two or three weeks to build their own version of a popular agent setup, building what they actually need, their productivity would skyrocket.

He said that things can change; in two weeks it could be "give the agent everything". He mentioned a new memory paper from Google that lets the agent index information. But as it pertains to real life, less is more and simple is better. If you cannot explain it in a few sentences, you probably do not understand it. The model companies are focused on white-collar work, such as financial work and checking contracts. He said:

> The models are really, really good. What matters more is the harness and the tools you provided.

What you and I have that the models do not is our specific workflow, taste and strategy, and those can be codified in skills.

## A real skill, in tokens

*[Watch from 29:33](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=1773s)*

Ross showed one of his skills, and told people not to download it: he put it up just to get some GitHub stars. It is a code structure skill of 116 lines. After the AI has generated a bunch of code, he likes it structured in a certain way so it is easy for him to review. The only thing added to the context is the name, code structure, and a description that starts "use when multiple workflows duplicate the same operational logic". When he tells the agent to clean up the code structure, it sees the name, reads the description, realises it makes sense, and only then progressively discloses the rest.

If this were an AGENT.md, he checked with a tokenizer: 944 tokens added every single time he starts a chat. With just the name and description it is 53 tokens. I pointed out that you do not want to hit the limit quicker than you need to.

## Keep the context window light

*[Watch from 30:52](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=1852s)*

Ross explained that the model gets dumb as the context window fills. Perhaps 10% is already filled with the system prompt and so on, and you want to stay between fresh and about 70%. As you approach 99 or 100%, and even 90 or 80%, it starts to get dumb. It is like a human at school who never paid attention all year and then tries to learn polynomials, graphs and weird notation the night before. So save your context window: it saves money and makes a more performant agent.

Rely on the model's strengths. What the model needs is what is unique about you, your workflow and your business, not general knowledge. Do not tell it to use React, because it knows to use React. Do not tell it to denote money with a dollar sign, because it will. If you have a specific currency, or something the agent would not know by itself, that is when AGENT.md and CLAUDE.md files make sense, but otherwise he called them a farce. What it comes down to, he said, is skills, skills, skills.

## Why I asked Ross to come on

*[Watch from 33:05](https://www.youtube.com/watch?v=S_oN3vlzpMw&t=1985s)*

To close, I told the story of how Ross nearly did not come on the show. He said he did not have a banger, something new dropping to review, and that there are not that many tools dropping nowadays because the big dogs run the show. I told him to think about impact. I showed him a text from someone who saw a video we did together; it got him into coding, and now he runs a cake business and makes $150,000 a year and growing. He said the Greg and Ross Mike episode in November last year is what got him into coding.

It is not about the numbers. I hope this episode gets 200k views or more, but if it gets 2,000 views and two people take this information and change their business, productivity or the way they think, that is why we are on this planet: to inspire people to get their creative juices flowing. Ross thanked me and said he hopes this helps somebody.

*[Watch the full video on YouTube](https://www.youtube.com/watch?v=S_oN3vlzpMw)*
