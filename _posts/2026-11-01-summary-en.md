---
layout: default
title: "Horizon Summary: 2026-11-01 (EN)"
date: 2026-11-01
lang: en
---

> From 77 items, 14 important content pieces were selected

---

**Technology News**
1. [OpenAI plans shared ChatGPT and Codex usage limits from December](#item-tech-news-1) ⭐️ 8.0/10
2. [Memdoor example teams five small open models against a bigger coding model](#item-tech-news-2) ⭐️ 7.0/10
3. [A creator&\#x27;s repeatable pipeline for 24-second AI cartoons, tested across six models](#item-tech-news-3) ⭐️ 7.0/10
4. [New mcp-linter scans AI assistant servers for protocol and security errors](#item-tech-news-4) ⭐️ 7.0/10
5. [Open-source Qiyan adds Codex account switching and usage tracking](#item-tech-news-5) ⭐️ 7.0/10
6. [ChatGPT Account-Takeover Flaw Fixed After HTML Preview Sandbox Escape](#item-tech-news-6) ⭐️ 6.0/10
7. [Open-source C\# model router FAIRouter arrives on NuGet](#item-tech-news-7) ⭐️ 6.0/10
8. [Unverified report claims Anthropic bans accounts used to train larger AI models](#item-tech-news-8) ⭐️ 5.0/10
9. [Datasette Agent now reuses the default model set in LLM](#item-tech-news-9) ⭐️ 5.0/10
10. [Blogger tests Qwen coding models by building a hidden-data scanner without an IDE](#item-tech-news-10) ⭐️ 5.0/10
11. [TBook adds phone and desktop readers and a second book format](#item-tech-news-11) ⭐️ 5.0/10
12. [ChatGPT Adds Two-Account Switching on Web, iOS and Android](#item-tech-news-12) ⭐️ 5.0/10
13. [Unverified Report Says Grok Accepts Alipay, Halves First Month](#item-tech-news-13) ⭐️ 5.0/10

**Financial News**
1. [HKT Agrees to Halt U.S. Telecom Operations Under FCC Pressure](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenAI plans shared ChatGPT and Codex usage limits from December](https://x.com/thsottiaux/status/2116692529970311254) ⭐️ 8.0/10

A Telegram report says OpenAI will combine the usage allowances for ChatGPT and its coding tool Codex into one shared pool for its Plus, Pro and Business subscription plans starting in December 2026. Usage will be counted in tokens \(the small chunks of text an AI model reads and produces\), so more advanced models and more complex tasks use up more of the allowance. The report says ordinary, immediate chat replies will not count, users can see the combined remaining amount and reset time in settings, and after hitting the limit they can wait for a reset, upgrade their plan or buy extra usage credits. It cites an OpenAI Help Center page but gives no token counts or rate-limit figures.

telegram · zaihuapd · Nov 1, 01:29

**「Context」** ChatGPT and Codex currently have separate usage allowances. Codex is OpenAI&\#x27;s coding assistant, which can carry out programming tasks on a user&\#x27;s behalf. Tokens are the chunks of text a model reads and generates, and OpenAI&\#x27;s help center says ChatGPT and Codex usage is measured in them.

**「What changes for paying users」** The practical effect is that Codex work and ChatGPT use now draw on one shared allowance, so a heavy coding session can leave less room for other ChatGPT features later, and vice versa. Until now, Codex on Plus and Pro came with its own separate time-window and weekly limits, which the reports say Codex users tracked on their own \(tool-3-1, tool-3-3\). Since the numbers have not been published, users who rely on Codex daily should check the combined remaining usage and reset time in settings after the change takes effect, and plan on either waiting for the reset, upgrading the plan, or buying extra credits. Instant chat is said to be exempt from the metering, so quick questions should not use up the allowance. Because this comes from a secondhand relay of a tweet rather than an OpenAI announcement with figures, treat the details as reported and not final.

<details><summary>References</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/20001625-understanding-chatgpt-and-codex-usage-limits">Understanding ChatGPT and Codex usage limits | OpenAI Help ...</a></li>
<li><a href="https://standardcompute.com/codex-usage-limits">Codex Usage Limits (Oct 2026): Plus vs Pro, Weekly Limit, Reset</a></li>
<li><a href="https://usagebox.com/articles/openai-codex-pricing-usage-limits-2026">OpenAI Codex Pricing &amp; Usage Limits (October 2026): Every ...</a></li>

</ul>
</details>

**Tags**: `#ChatGPT`, `#Codex`, `#usage quotas`, `#OpenAI`, `#subscription pricing`

---

<a id="item-tech-news-2"></a>
### [Memdoor example teams five small open models against a bigger coding model](https://github.com/guregodevo/memdoor/tree/main/examples/workflows/team-solve) ⭐️ 7.0/10

A developer has published an example workflow called Memdoor on GitHub that hands one coding problem to five copies of a mid-sized open-weight model — a model whose files anyone can download and run on their own computer — and coordinates them as a team. The project claims this group scores better on LiveCodeBench Hard, a public set of difficult programming puzzles used to rank coding models, than a model the write-up calls &quot;Fable 5&quot;. No scores, settings, hardware details or costs are included, and neither &quot;Qwen3.8-27B&quot; nor &quot;Fable 5&quot; clearly matches a model the public can identify, so the comparison is an unverified claim rather than a measured result. What exists today is the copyable setup itself: a runnable example of several smaller models working the same problem together.

hackernews · guregodevo · Oct 31, 22:46 · [Discussion](https://news.ycombinator.com/item?id=50320995)

**「Background」** LiveCodeBench Hard is a set of difficult competitive-programming problems used to compare coding models on unfamiliar tasks. Qwen3.8-27B is an open-weight model, meaning its files can be downloaded and run on a user&\#x27;s own computer rather than only through a company&\#x27;s online service. Memdoor&\#x27;s team-solve example is a harness—a workflow script that assigns five copies of the model separate roles \(planner, two idea generators, solver, manager, and repair worker\) and has them exchange information only by writing files to disk.

**「What copying this setup would actually cost」** Anyone tempted to copy this setup should budget for multiplied compute, not just for the model. The project&\#x27;s own discussion puts a price on one small experiment: fifty runs — five passes over ten LiveCodeBench Hard problems — cost $35.79 in output tokens through OpenRouter \(a paid service that resells access to many models\), or $38.77 counting 16 attempts lost to a timeout, a fix, or a pause. Running locally changes the bill but not the direction: a commenter reports a 27-billion-parameter Qwen model at about 50 tokens per second on a reasonably priced gaming PC, enough to make a five-model team usable but slow, and the same commenter points out that any harness clever enough to lift the small models would lift the stronger model they are measured against too — so the headline comparison is worth treating as unproven until the configuration behind it is published.

**「From the comments」** The most concrete report comes from a commenter who says a 27-billion-parameter Qwen model can run at roughly 50 tokens \(small chunks of text\) per second on a reasonably priced gaming PC using a compressed version of the model, and notes that the same team approach would presumably also improve the stronger model it is being compared against. Another commenter argues that piling on more models, more attempts and differing opinions is becoming a scaling method of its own, though it is held back by how well the models communicate with each other and by computing power, while a third says the point is to keep locally run models competitive with the large cloud providers.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/guregodevo/memdoor/tree/main/examples/workflows/team-solve">memdoor/examples/workflows/team-solve at main · guregodevo ...</a></li>
<li><a href="https://aiweekly.co/alerts/memdoors-five-qwen38-27b-team-beats-fable-5-at-livecodebench">Memdoor&#x27;s five-Qwen3.8-27B team beats Fable 5 at LiveCodeBench</a></li>
<li><a href="https://daily.dev/posts/memdoor-a-team-of-5-qwen3-8-27b-models-beats-fable-5-on-livecodebench-hard-ghdvz1p3j">Memdoor: A team of 5 Qwen3.8-27B models beats Fable 5 on...</a></li>

</ul>
</details>

**Tags**: `#open-weight models`, `#multi-agent workflows`, `#coding benchmarks`, `#local inference`, `#Qwen`

---

<a id="item-tech-news-3"></a>
### [A creator&\#x27;s repeatable pipeline for 24-second AI cartoons, tested across six models](https://habr.com/ru/articles/1102098/?utm_campaign=1102098&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 7.0/10

A creator published a step-by-step account on the Russian-language tech site Habr of how they make a 24-second vertical cartoon series, &quot;Forest Street,&quot; using six cloud AI services: four that generate video \(Wan, Kling, Veo and Seedance\) and two that generate still images \(GPT Image and Nano Banana Pro\). Between 29 and 31 October 2026 the same episode was rebuilt roughly ten different ways, and the post presents the order of steps that survived that testing — a script broken down second by second, fixed character sheets that keep the heroes looking the same from shot to shot, and shot selection — plus a cost table, examples of spoiled shots paired with the fix that rescued them, and a list of problems that were never solved. The author states one clear limit: there are no audience numbers yet, so the piece is about production only, and the excerpt available here does not include the cost table itself, meaning its figures cannot be checked. Two finished episodes, &quot;А телефон куда?&quot; and &quot;Подменишь?&quot;, were out as of 31 October, while two others are described as production trials.

rss · Habr AI · Oct 31, 14:55

**「Why consistency is the hard part」** AI video generators such as Kling, Veo and Seedance turn a written prompt or a still image into a short clip, but each clip is generated separately, so a character&\#x27;s face, clothing and proportions can drift from shot to shot. To keep a cartoon cast recognizable, the Habr author uses a &quot;reference sheet&quot;: a fixed set of images that defines how each character should look. &quot;Vertical&quot; means the episode is framed for a phone screen, and the per-second script divides the 24-second episode into timed beats so each generated clip covers a specific moment.

**「Budget for retries」** For anyone making a short animated episode with these cloud video tools, the practical consequence is to plan and pay for repeated generations, not a single clean pass: the creator reports rebuilding the 24-second episode about ten ways across Wan, Kling, Veo and Seedance, and keeping a character from being duplicated depended on feeding each model a fixed reference sheet \(a set of character images\) and choosing shots by hand. The post says it includes a cost table, but the excerpt does not show the figures, so it cannot yet be used to budget a similar episode.

**Tags**: `#AI video generation`, `#Kling`, `#multi-model pipeline`, `#cost breakdown`, `#production workflow`

---

<a id="item-tech-news-4"></a>
### [New mcp-linter scans AI assistant servers for protocol and security errors](https://habr.com/ru/articles/1102086/?utm_campaign=1102086&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 7.0/10

An independent developer has published mcp-linter, a command-line checker for servers built on the Model Context Protocol \(MCP\), the standard that lets AI assistants such as Claude Desktop and Cursor call outside tools and data. It is a Node.js tool with no third-party dependencies, applies 34 protocol and security rules, and gives each server a health score from A+ to F on a 0–100 scale. It can apply some fixes automatically, export findings in SARIF \(a standard report format for code-security tools\) for GitHub Security, and run as a GitHub Action. The author says the tool found bugs in Anthropic&\#x27;s official MCP servers, but the post does not list or reproduce those findings, so that claim is unverified; the supplied text also gives no release version.

rss · Habr AI · Oct 31, 13:55

**「Background」** MCP \(Model Context Protocol\) is a shared protocol that lets AI assistants such as Claude Desktop and Cursor call outside tools and read data sources. Each MCP server is a small program that exposes those tools. A linter is a checking tool that scans such a server for protocol and security mistakes before users run into them — for example, a stray debug print that corrupts the messages exchanged with the assistant, or a dangerous tool without a label telling the assistant to ask for confirmation.

**「What this means if you run MCP servers」** If you connect MCP servers to Claude Desktop or Cursor, this gives you a way to inspect one before trusting it: a single command scans the server&\#x27;s code and tool descriptions, prints a 0–100 health score, and lists what tripped one of the 34 rules, so a stray debug print that would freeze the client or a dangerous tool missing its warning label shows up before the agent uses it. Two practical limits apply. It needs Node.js installed, and it only reads the server&\#x27;s code and descriptions, so a good grade does not prove the server&\#x27;s own logic is safe or correct. The author&\#x27;s claim that the linter found bugs in Anthropic&\#x27;s official servers is his own assertion; the post does not reproduce the specific findings, so treat that part as unconfirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/modelcontextprotocol/servers">GitHub - modelcontextprotocol/ servers : Model Context Protocol Servers</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#developer tooling`, `#linter`, `#security`, `#Claude Desktop`

---

<a id="item-tech-news-5"></a>
### [Open-source Qiyan adds Codex account switching and usage tracking](https://linux.do/u/user400) ⭐️ 7.0/10

An open-source project called Qiyan is offering preview desktop apps for macOS and Windows that add account switching, usage-limit checks and token statistics to Codex, OpenAI&\#x27;s AI coding assistant. The code is published under the MIT license \(a permissive open-source license\), with preview downloads listed as version 1.6.0-preview.1 for macOS and 1.5.0-preview.1 for Windows. The app is unofficial and still in preview, and the post gives no independent check that its quota or token counts—tokens being the text chunks an AI model processes and bills for—are accurate.

telegram · linuxdo\_tg · Nov 1, 05:47

**「Why an account switcher for Codex exists」** Codex is OpenAI&\#x27;s coding assistant, usable as a program on your own machine, where a paid account comes with usage limits and consumption is counted in tokens \(the small chunks of text a model reads and writes\). Because that allowance is tied to a single signed-in account, moving between accounts usually means logging out and back in, and the remaining quota is not shown in one place — which is why unofficial helpers already circulate: a GitHub project called Codex Switcher saves the current account&\#x27;s credentials before writing a new one and tells users to close Codex before switching, and another sells a Mac menu-bar switcher for the same job. Qiyan&\#x27;s stated difference is bundling account switching, quota checks and token counts into one window on both macOS and Windows.

**「What it means in practice」** For Codex users who work with more than one account or need to watch a usage cap, Qiyan puts account switching, remaining quota and token counts in one desktop window. Its macOS and Windows builds are different preview versions, so features may not match, and because the tool is unofficial, users should compare its figures with official usage records before depending on them.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Lampese/codex-switcher">GitHub - Lampese/ codex - switcher : A Desktop Application for...</a></li>
<li><a href="https://www.codexswitch.com/">Codex Switcher for Mac | Switch ChatGPT accounts fast</a></li>

</ul>
</details>

**Tags**: `#codex`, `#coding-agents`, `#open-source`, `#developer-tooling`, `#quotas`

---

<a id="item-tech-news-6"></a>
### [ChatGPT Account-Takeover Flaw Fixed After HTML Preview Sandbox Escape](https://simonwillison.net/2026/Oct/31/how-we-took-over-chatgpt-accounts/) ⭐️ 6.0/10

Security researchers at Parameter Labs published a detailed account of how they could take over a signed-in user&\#x27;s ChatGPT account by getting that person to open a specially crafted shared link. OpenAI has since closed the hole and paid a $5,000 bug bounty. The attack began in ChatGPT&\#x27;s HTML preview feature \(previously called Canvas\), which displays interactive web pages written by the model inside a sandbox — an isolated box meant to keep their code away from the rest of the site. A flaw in how ChatGPT&\#x27;s math-graph support handled messages from the MathLive on-screen keyboard let code inside that box insert a new frame without the usual restrictions, and a YouTube endpoint was then used to get JavaScript \(the code that makes web pages interactive\) running on the main ChatGPT page. From there, the attackers could read private data through ChatGPT&\#x27;s own interfaces and send it out through an image link; simply visiting the crafted share URL while signed in was enough. Simon Willison, whose post summarizes the disclosure, called the $5,000 payout &quot;a bit cheap&quot; for a flaw this serious.

rss · Simon Willison · Oct 31, 23:15

**「Background」** ChatGPT&\#x27;s HTML preview — the pane that displays small interactive apps written in code, previously called Canvas — runs that code inside a sandboxed iframe: a sealed box within the page, meant to stop the code from reaching the rest of ChatGPT or the user&\#x27;s private data. A Content Security Policy is a browser-level rule that lists which scripts a page is allowed to run, a second barrier if the box fails. A bug bounty is a cash payment a company makes to an outside researcher who reports a security flaw; according to the disclosure discussion, OpenAI confirmed the report, fixed the flaw and paid $5,000.

**「What it means for users」** Until the fix, a shared ChatGPT link was enough on its own to expose an account — no download or password entry required — so a ChatGPT share link deserves the same caution as any unexpected link from a stranger. Because OpenAI has already closed the hole, there is nothing for users to install or change; the published write-up does not include proof-of-concept code, so the attack cannot be re-run from the details given.

<details><summary>References</summary>
<ul>
<li><a href="https://www.parameter.ai/labs/we-found-a-gap-at-openai">Do the Math : How We Took Over ChatGPT Accounts - Parameter</a></li>
<li><a href="https://news.ycombinator.com/item?id=50314699">Do the math : How we took over ChatGPT accounts | Hacker News</a></li>

</ul>
</details>

**Tags**: `#security`, `#ChatGPT`, `#sandbox-escape`, `#exploit-disclosure`, `#artifacts`

---

<a id="item-tech-news-7"></a>
### [Open-source C\# model router FAIRouter arrives on NuGet](https://habr.com/ru/articles/1101942/?utm_campaign=1101942&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

FAIRouter, an open-source router for AI models written in C\#, is now published on NuGet — the public package library from which .NET developers add prebuilt code to their projects. A model router is software that sits in front of several AI models and decides, request by request, which one should answer. The project&\#x27;s stated goal is to balance speed, cost and quality, so that an answer of adequate quality arrives faster and cheaper. The Habr post says it covers installing the package, sending a first request, training the router on user feedback, and plugging in your own candidate models, but the available text is only an introduction: no version number, installation command, benchmark results, or evidence of how well the routing actually performs is included.

rss · Habr AI · Oct 31, 08:53

**「What FAIRouter does」** A model router is a piece of software that sits between an application and several AI models and picks one for each request — for example the cheapest model likely to answer well, or the fastest one. FAIRouter is an open-source project; a follow-up article on the same Habr post says the C\# version previously had to be compiled from source code, and that publishing it on NuGet \(the standard package repository for .NET software\) means developers can now install it instead. The router also includes a &quot;judge&quot; component that scores answers and feeds those scores back so the router&\#x27;s choices can improve over time. The supplied material gives no version number, benchmark, or independent evidence of how well the routing works.

**「Who this affects」** For developers building .NET applications that call AI models, this is a library they could add instead of hard-coding a single model for every request, letting the routing layer trade cost against quality. Because the announcement publishes no benchmarks or version details, a team considering it would need to run its own comparison against whatever setup it uses today before relying on it.

<details><summary>References</summary>
<ul>
<li><a href="https://habr.com/ru/articles/1101942/">FAIRouter вышел на NuGet. Выбираем языковую модель под задачу ...</a></li>

</ul>
</details>

**Tags**: `#model routing`, `#C\#`, `#.NET`, `#open source`, `#LLM cost optimization`

---

<a id="item-tech-news-8"></a>
### [Unverified report claims Anthropic bans accounts used to train larger AI models](https://twitter.com/jiahaoshao1/status/2116475922190922088) ⭐️ 5.0/10

A post on X dated October 31, 2026 claims that Anthropic is terminating accounts whose users bring Claude into work connected with training larger AI models — teaching a model by feeding it very large amounts of text so it picks up patterns. The claim comes from a single social-media account, quoted no Anthropic policy text, named no affected users, and offered no dates or other evidence; the item supplied here contains no source material beyond the post&\#x27;s headline, and Anthropic has not been quoted confirming or denying it. It drew about 160 comments on Hacker News, but those discuss vendor reliance and Claude&\#x27;s refusals in general rather than corroborating the specific blocking claim. Treat the report as an unconfirmed signal, not an established rule change.

hackernews · pretext · Oct 31, 19:39 · [Discussion](https://news.ycombinator.com/item?id=50319358)

**「Background」** Anthropic revised its rules on misuse of Claude in October 2026, saying account-level penalties would be kept for serious cases and that cutting off individual conversations would stay the main way it enforces the rules; it added that the policy was not aimed at ordinary criticism, dark-themed creative writing, or legitimate model testing and research. Separately, users have reported account bans tied to holding several Claude Max subscriptions at once, a pattern that predates this claim.

**「What it means in practice」** Because nothing here verifies which uses are actually restricted, the practical takeaway is precaution rather than a new rule to obey: anyone who pays for Claude and whose work involves building or training models should keep a second provider set up and keep prompts, code, and documents in formats they can move elsewhere. If a ban of this kind were real, the loss would not be the subscription fee but access to work stored inside one vendor&\#x27;s tools.

**「Community discussion」** Commenters argued less about the ban claim itself than about dependence on one supplier. One \(zmmmmm\) said every professional user should actively cultivate alternatives and push for portable, standardized tools, calling Anthropic opinionated and willing to drop whole groups of users; another \(juanre\) said model access must become a commodity, comparing single-vendor reliance to an earlier business of his where most revenue ended up going to Google. Others reported Claude refusing tasks they considered legitimate — copying code out of their own codebase, or signing in for browser testing — which are anecdotes about refusals, not evidence of account terminations.

<details><summary>References</summary>
<ul>
<li><a href="https://theaiinnovator.com/anthropic-bans-users-from-abusing-claude-under-new-ai-policy/">Anthropic Bans Users From Abusing Claude Under New AI Policy</a></li>
<li><a href="https://metricnexus.ai/blog/anthropic-banning-multiple-claude-accounts">Anthropic Is Banning Users With Multiple Claude Accounts ...</a></li>

</ul>
</details>

**Tags**: `#anthropic`, `#claude`, `#account-bans`, `#access-restrictions`, `#terms-of-service`

---

<a id="item-tech-news-9"></a>
### [Datasette Agent now reuses the default model set in LLM](https://simonwillison.net/2026/Oct/31/datasette-llm/) ⭐️ 5.0/10

datasette-llm 0.1a9, an early test release of a small add-on for the Datasette data-publishing tool, now picks up the default AI model already configured in LLM — Simon Willison&\#x27;s command-line tool for sending prompts to language models, where the default is the model used when no other is named. As a result, Datasette Agent, the add-on that lets an AI model work with a Datasette database, can start without the extra setting that previously had to name a model, such as \`-s plugins.datasette-agent.default\_model gpt-6-astra\`. Willison calls this a tiny usability improvement and says larger Datasette Agent upgrades are still in the pipeline, without giving details.

rss · Simon Willison · Oct 31, 22:10

**「Background」** Datasette is a tool for publishing and browsing databases as a website, and plugins add features to it. LLM is a separate command-line program that keeps its own settings, including which AI model to use by default.

**「What it means in practice」** For someone who already uses LLM with a chosen default model, the startup command gets shorter: the model flag disappears, leaving one less setting to remember. The release notes do not say what happens when LLM has no default model configured, so that case may still require an explicit setting.

**Tags**: `#datasette`, `#datasette-agent`, `#llm`, `#developer-tooling`, `#release`

---

<a id="item-tech-news-10"></a>
### [Blogger tests Qwen coding models by building a hidden-data scanner without an IDE](https://habr.com/ru/articles/1102144/?utm_campaign=1102144&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Russian-language Habr post by author BlackEric001 describes an attempt to write a scanner for NTFS alternate data streams — hidden attachments that can be glued to a file on Windows drives and are invisible to ordinary file listings — using Qwen and Qwen Coder, the coding-focused models from Alibaba&\#x27;s Qwen family, instead of a normal programming environment. The author frames the exercise explicitly as a test of how well the Qwen models can write software. In the excerpt available here, however, the post only states the intent and explains what alternate data streams are; it does not yet show the prompts used, the setup, the generated code, or any result, so no claim about the models&\#x27; coding ability can be judged from it. This is one person&\#x27;s experiment, not a benchmark or a verified workflow.

rss · Habr AI · Oct 31, 18:18

**「Background」** NTFS is the standard file system for modern Windows, and Alternate Data Streams \(ADS\) are extra hidden data channels that can be attached to a file without appearing in normal file listings. Qwen is a family of AI language models, and Qwen Coder is a version aimed at programming tasks; the author is testing them by asking them to write an ADS scanner without using an integrated development environment \(IDE\), the usual all-in-one code-writing application.

**「Why it matters to readers」** For anyone considering letting an AI model write small utility programs, the useful detail would be how much of the work the model actually completed and how much had to be corrected by hand — and that is exactly what the visible portion of this post does not provide. Readers should treat it as an unfinished account until the full write-up is available.

**Tags**: `#qwen`, `#code-generation`, `#coding-agents`, `#model-capability`, `#windows`

---

<a id="item-tech-news-11"></a>
### [TBook adds phone and desktop readers and a second book format](https://habr.com/ru/articles/1100334/?utm_campaign=1100334&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

TBook, a personal project that turns foreign-language books into bilingual editions with the original and translation kept in matching positions, has released a second version of the file format it uses for these books, four months after the first write-up. It now has an app on Google Play, desktop readers for three operating systems, dictionaries that work without an internet connection, and two converters: an online one with a shared book library and a Telegram bot, and a graphical one distributed as ready-to-run programs. The translation and matching layout are generated by inexpensive AI models \(software trained on large amounts of text\), and the author says the method avoids the common failure where translated passages slip out of step with the original. Twenty reports on translation-quality experiments were also published.

rss · Habr AI · Oct 31, 12:45

**「Background」** TBook is a personal reading project for foreign-language books: it pairs the original text with a translation line by line, so the reader can follow both without losing their place. The author introduced the format in July and uses inexpensive AI language models to produce those aligned translations; this update covers the four months of work since then.

**Tags**: `#LLM translation`, `#interlinear alignment`, `#reading app`, `#prompt engineering`, `#side project`

---

<a id="item-tech-news-12"></a>
### [ChatGPT Adds Two-Account Switching on Web, iOS and Android](https://x.com/thsottiaux/status/2116405414921384099) ⭐️ 5.0/10

OpenAI has added account switching to ChatGPT on the web, iPhone and Android, letting people stay signed in to as many as two accounts and move between them without logging out. Each account keeps its own chat history, memory \(the saved details ChatGPT carries between chats\), files, workspace \(a shared team account\) and billing. Mobile devices can also receive notifications for both signed-in accounts, and tapping one opens the matching account. OpenAI says desktop support is coming soon, so the feature is not yet available in the desktop app.

telegram · zaihuapd · Oct 31, 05:58

**「Background」** Until now, using both a work and a personal ChatGPT account meant signing out of one before signing in to the other. Each login carries its own chat history, saved memory, files and subscription, which is why keeping those accounts separate mattered.

**「What It Means in Practice」** People who keep separate work and personal ChatGPT accounts can now leave both signed in on the same phone or browser and switch without re-entering credentials, while their chats, saved memory and files remain separate. The trade-off is that notifications from both accounts can arrive on the same phone, so adding a work account to a personal device can surface work alerts there.

**Tags**: `#ChatGPT`, `#OpenAI`, `#account-management`, `#subscription`, `#access`

---

<a id="item-tech-news-13"></a>
### [Unverified Report Says Grok Accepts Alipay, Halves First Month](https://x.com/jordan1oi/status/2116371730965172442) ⭐️ 5.0/10

An X user claims that Grok, the chatbot from AI company xAI, now accepts Alipay \(China&\#x27;s widely used payment app\) and offers half off the first month. The post was relayed through a Telegram channel and gives no plan name, price, discount terms, eligibility rules, or confirmation from xAI, so the offer cannot be verified. The same user says the move would shake up the market and hurt services that buy subscriptions on customers&\#x27; behalf.

telegram · zaihuapd · Oct 31, 06:41

**「Context」** Grok is the chatbot made by xAI, Elon Musk&\#x27;s AI company, and it is sold as a monthly subscription. Paying for an overseas AI subscription from mainland China usually requires a foreign bank card, so accepting Alipay \(the Chinese wallet most people already have on their phones\) removes a step that normally blocks would-be subscribers. News reports citing user screenshots say the Alipay and UnionPay options appear when an account&\#x27;s region is set to mainland China, with the charge converted from yuan, and that X — which shares Grok&\#x27;s payment system — can be subscribed to the same way.

**「What It Could Mean」** If confirmed, Alipay users could pay for Grok directly instead of going through a reseller, but the post gives no price, plan, or eligibility details, so there is nothing to check before signing up.

<details><summary>References</summary>
<ul>
<li><a href="https://phemex.com/news/article/xais-grok-adds-china-unionpay-and-alipay-payment-support-offers-halfprice-firstmonth-subscription-101964">xAI Grok Now Supports Alipay &amp; UnionPay Payments With Half-P ...</a></li>
<li><a href="https://panews.io/articles/01a19192-e2ac-7780-b036-8db851615833">Musk&#x27;s xAI Grok Now Supports China UnionPay and Alipay ...</a></li>
<li><a href="https://www.ainvest.com/news/grok-takes-alipay-payment-rail-signal-china-launch-57x-sales-spacex-2610/">Grok Takes Alipay: a Payment-Rail Signal, Not a China Launch ...</a></li>

</ul>
</details>

**Tags**: `#Grok/xAI`, `#subscription pricing`, `#payment methods`, `#regional access`, `#promotions`

---

## Financial News

<a id="item-finance-news-1"></a>
### [HKT Agrees to Halt U.S. Telecom Operations Under FCC Pressure](https://www.cnbc.com/2026/10/31/hong-kong-telecom-firm-agrees-to-halt-us-operations-under-pressure.html) ⭐️ 7.0/10

Hong Kong Telecom \(HKT\) agreed under pressure from the U.S. Federal Communications Commission to shut down its U.S. operations, filing a cessation application within 30 days and ending telecom services to and within the U.S. by September 1, 2027. The FCC opened proceedings in October 2025 to revoke HKT&\#x27;s operating authority, citing national security and its links to China Unicom; that proceeding will not move forward after the settlement, and parent company PCCW declined immediate comment, CNBC reported.

telegram · zaihuapd · Oct 31, 10:22

**「Background」** The agreement follows the FCC’s October 2025 move to revoke HKT’s permission to provide U.S. telecom services, citing national-security concerns and its affiliation with China Unicom; the settlement ends that proceeding.

**「Impact」** Customers relying on HKT for U.S. telecom services will need to switch providers before those services end on Sept. 1, 2027.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/10/31/hong-kong-telecom-firm-agrees-to-halt-us-operations-under-pressure.html">Hong Kong telecom firm agrees to halt U.S. operations under ...</a></li>
<li><a href="https://docs.fcc.gov/public/attachments/DOC-415089A1.pdf">FCC Moves to Expel Hong Kong Telecom from U.S. Telecom ...</a></li>
<li><a href="https://www.straitstimes.com/world/hong-kong-telecom-company-agrees-to-halt-us-operations-under-pressure">FCC forces HKT to halt US telecom operations | The Straits Times</a></li>

</ul>
</details>

**Tags**: `#HKT`, `#FCC`, `#telecom regulation`, `#US market exit`, `#national security`

---