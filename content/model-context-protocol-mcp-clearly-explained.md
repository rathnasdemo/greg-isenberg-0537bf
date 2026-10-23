---
schemaId: urn:gala:schema:content-frontmatter:2.0.0
schemaVersion: 2.0.0
id: 01a16922-a085-79a9-a137-93d9229cb9b3
kind: article
title: Model Context Protocol (MCP), clearly explained (why it matters)
description: MCP is a standard that lets an LLM talk to outside tools the same way every time. Ross Mike walks me through what it is and where the opportunity sits.
language: en-US
authors:
- 01a16925-fde6-7282-8086-350fcd75ce35
tags:
- mcp
- ai-agents
- llm-tools
- startup-ideas
status: published
createdAt: '2026-04-08T12:00:01.000Z'
publishedAt: '2026-04-08T12:00:01.000Z'
slug: model-context-protocol-mcp-clearly-explained
hero:
  path: assets/content-model-context-protocol-mcp-clearly-explained-hero.jpg
  alt: Thumbnail of the video "Model Context Protocol (MCP), clearly explained (why it matters)"
  role: informative
redirects: []
extensions: {}
---
*Adapted from the video [Model Context Protocol (MCP), clearly explained (why it matters)](https://www.youtube.com/watch?v=7j_NE6Pjv-E)*

> **TL;DR:** Everyone is talking about MCP and almost nobody can say what it is. My guest Ross Mike explains that an LLM alone only predicts the next word, tools make it more capable but are painful to glue together, and MCP is a standard layer that translates every tool into one language the LLM understands. The server lives with the service provider. For non-technical founders, the advice is to watch where the standard settles before acting.

Everyone is talking about MCPs and it has gone completely viral. The reality is that most people have no idea what MCPs are, what they mean, or what startup opportunities come with them.

I don't know what the hell MCPs are either, and I have been seeing them all over X. I have read a bunch of threads and watched a couple of videos, but nothing beats a Ross Mike explanation. So I brought on Professor Ross Mike, who is the best explainer of technical concepts for non-technical people that I know. He explains it beautifully in a short amount of time, and if you stay to the end you will hear a couple of his startup ideas that involve MCPs.

## Why standards matter and why an LLM alone can't do much

*[Watch from 1:22](https://www.youtube.com/watch?v=7j_NE6Pjv-E&t=82s)*

Ross started by saying that understanding MCP is important, but that it is a big deal and not a big deal at the same time. In programming, engineers love standards because standards let systems communicate with each other. The best-known example is REST APIs, a standard that every company follows when it builds its services so that an engineer can connect to them.

Then he asked me to hold on to one idea: LLMs by themselves are incapable of doing anything meaningful. If you open a basic chatbot and tell it to send you an email, it will just tell you it can't. The most you can do is ask it questions, for example about a historical figure. On its own, an LLM is good at one thing, which is predicting the next text. If you say "My Big Fat Greek", it will work out from its training data that the next word is "wedding".

## The second evolution: LLMs plus tools

*[Watch from 3:34](https://www.youtube.com/watch?v=7j_NE6Pjv-E&t=214s)*

The next step was that developers combined LLMs with tools, and you can think of a tool like an API. Chatbots that can search the internet are the example Ross gave. Perplexity lets you chat with an LLM that can fetch information from the internet, but the LLM itself cannot do that. They built a tool and gave it access to an external service.

Another example: every time you get an email, you want an entry in a spreadsheet. Services like Zapier and n8n let you build an automation and connect it to your LLM, and now it is a bit more meaningful.

## Why gluing tools together is a nightmare

*[Watch from 4:52](https://www.youtube.com/watch?v=7j_NE6Pjv-E&t=292s)*

It gets frustrating when you want an assistant that does several things, such as searching the internet, reading your emails and summarising them. You become someone who glues a bunch of different tools onto LLMs, and that is cumbersome. Ross said that is why we don't have an Iron Man level Jarvis assistant: connecting a tool to an LLM is one thing, but stacking tools on top of each other so they work cohesively is a nightmare.

He works at an AI startup, Tempo, and described the pain from experience. You have to find an external service, connect it to the LLM, and make sure the LLM doesn't hallucinate or do something stupid. As cool as LLMs are, he said, by themselves they are very, very dumb, and tools make them a bit more capable. I confirmed it was crystal clear so far.

## What MCP is: a layer that translates every tool into one language

*[Watch from 7:34](https://www.youtube.com/watch?v=7j_NE6Pjv-E&t=454s)*

Ross's simplest way to think about it, without getting too technical: imagine every tool you connect to is a different language. Tool one is English, tool two is Spanish, tool three is Japanese. It is not that there is no standard for how APIs work, but every service provider constructs theirs differently, with different information to pass and different setup. It will work, but at scale it gets very difficult.

MCP is a layer between your LLM and the services and tools, and it translates all those different languages into one unified language that makes sense to the LLM. It is the evolution of LLM plus tools, but it makes it very simple for the LLM to connect to outside resources such as a database. You can tell the LLM to create a new entry in your database, and because it is connected via MCP, it knows exactly what to do.

In the second evolution there is a lot of manual work, a lot of step-by-step planning and a lot of edge cases where it can fail. His example was simple: every time a Slack message arrives, your LLM reads it and texts you. Then Slack or the text service updates its API, and if that service is connected to others or part of a step-by-step automation, it becomes a nightmare. That is why, he said, even in the age of LLMs good engineers will still get paid. What MCP does is unify the LLM and the service in a layer where they can communicate efficiently.

## The pieces of the MCP ecosystem

*[Watch from 10:39](https://www.youtube.com/watch?v=7j_NE6Pjv-E&t=639s)*

Ross broke the ecosystem into four parts:

- **MCP client.** Something like Tempo, Windsurf or Cursor: the client-facing, LLM-facing side.
- **Protocol.** The two-way connection between the client and the server.
- **MCP server.** It translates the external service, its capabilities and what it can do, to the client.
- **Service.** The outside tool or database itself.

He thinks Anthropic is playing 3D chess with this design, because the MCP server is in the hands of the service provider. If he and I ran a dev tool company building the best database in the world and wanted people's LLMs to access it, it would be on us to construct the MCP server. Anthropic is in a way saying that it wants its LLMs to be more capable, but that it is the providers' job to figure that out. That is why external service providers are now building MCP servers and repos.

From a technology perspective, he said, all they did was create a standard, and it looks like companies and engineers are going to rally around it. You can build any API however you please, but if you want other developers and businesses to connect to your service as you scale, it has to be in a fashion that makes sense for them. MCP is that for LLMs, which are great at predicting the next word but not very capable on their own.

## The rough edges today

*[Watch from 13:25](https://www.youtube.com/watch?v=7j_NE6Pjv-E&t=805s)*

It is not all sunshine and rainbows. Ross pointed out that setting up an MCP server on any of your favorite MCP clients is annoying: a lot of downloading, moving files and copying things, and it is a lot of local stuff. There are kinks to figure out, and once it is polished, or the standard is updated, or someone comes up with a better one, we enter a world where LLMs become more capable. That is all MCP is, he said: making LLMs more capable. We are doing it with tools now and it kind of works, but MCP seems to be the next evolution.

He said it takes a lot of engineering hours when you build the second evolution by hand: one change happens, something breaks, and someone is on call and not sleeping. With MCP, if we all follow the standard, the LLM has access to everything it needs. It is not Einstein's fifth law of physics; it is literally a standard for LLMs, and something to be excited about.

## Does this matter for the average founder?

*[Watch from 15:39](https://www.youtube.com/watch?v=7j_NE6Pjv-E&t=939s)*

I ended on one question. Every time a protocol has become popular, such as HTTPS or SMTP, a lot of big businesses were built on top of it. So why now, and does this matter for the average person listening who is building out their ideas?

For the technical person, Ross had one idea, which he gave away for free: an MCP app store. There are a lot of repos of MCP servers out there, and it would be great if someone could go to a site, look at the different servers and their GitHub code, and click install or deploy. The server gets deployed and gives you a specific URL, which you paste into an MCP client. He even bought the domain, and it does nothing, so anybody should steal the idea. If you make millions, all he asks is that you send him a small cut.

## What to do if you are not technical

*[Watch from 17:25](https://www.youtube.com/watch?v=7j_NE6Pjv-E&t=1045s)*

For the non-technical person, Ross would stay up to date with the platforms building out MCP capability and watch where the standards are going. He doesn't know whether MCP has fully won; he thinks it needs to be challenged, and Anthropic might make an update. It is very early. Once the standard is finalized and service providers build out their MCP servers, or whatever the thing turns out to be, you can integrate much more seamlessly.

That is why every week there is a new chatbot interface with new tools. Step number two is not easy, especially making it cohesive and fast. He can sit for two hours and build something like it, but building the user experience, making it flawless and limiting hallucinations is very hard, and that is a lot of the work at Tempo. Standards make integrating easier, and you can think of the pieces as Lego blocks you keep stacking.

His advice to smart business owners is to keep close attention. He doesn't think we are at a place where any shots can be fired that make a smart business decision, so you sit, watch, observe and learn, and when the right thing at the right time happens, you strike. He doesn't see any crazy business opportunities right now for a non-technical person, and even for a technical person it is very early: imagine OpenAI came out with a standard tomorrow and everyone shifted to that. But understanding how this works means you will understand how the next thing works, and when it is finalized you hit the ground running.

*[Watch the full video on YouTube](https://www.youtube.com/watch?v=7j_NE6Pjv-E)*
