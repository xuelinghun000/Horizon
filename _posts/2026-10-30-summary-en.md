---
layout: default
title: "Horizon Summary: 2026-10-30 (EN)"
date: 2026-10-30
lang: en
---

> From 126 items, 26 important content pieces were selected

---

**Technology News**
1. [Mistral releases Mistral Large 4 with open weights and lower API prices](#item-tech-news-1) ⭐️ 9.0/10
2. [OpenAI adds separate usage credits to its top ChatGPT plans](#item-tech-news-2) ⭐️ 8.0/10
3. [OpenAI&\#x27;s Tibo says ChatGPT Pro usage limits double on October 30](#item-tech-news-3) ⭐️ 8.0/10
4. [An open-source tiny world model plays games on a Raspberry Pi Pico 2 W](#item-tech-news-4) ⭐️ 7.0/10
5. [OpenAI Codex 0.166.0 adds transcript search and a GPT-6.1 Terra model listing](#item-tech-news-5) ⭐️ 6.0/10
6. [Developer Rebuilt a Broken Legacy API With a Coding Agent Kept Blind to the Old Code](#item-tech-news-6) ⭐️ 6.0/10
7. [A Beginner&\#x27;s ESP32 Desk Screen for Tracking LLM Subscription Quotas](#item-tech-news-7) ⭐️ 6.0/10
8. [A YAML rulebook for keeping a Pydantic AI agent on task](#item-tech-news-8) ⭐️ 6.0/10
9. [Anthropic raises Claude API request limit to 128 MB](#item-tech-news-9) ⭐️ 6.0/10
10. [YC Labs Demonstrates Swarms of AI Characters in Minecraft and Mindustry](#item-tech-news-10) ⭐️ 5.0/10
11. [IBM&\#x27;s Granite Switch gets a 4.1.1 update billed as routine](#item-tech-news-11) ⭐️ 5.0/10
12. [Kimi K3 open-weight model claimed to beat GPT and Anthropic on some tests](#item-tech-news-12) ⭐️ 5.0/10
13. [vue-llm offers Vue and Nuxt developers a ready-made AI chat kit](#item-tech-news-13) ⭐️ 5.0/10
14. [How to build a local AI news agent with Ollama and LangGraph](#item-tech-news-14) ⭐️ 5.0/10
15. [Developer gives Claude Code a guarded entry into his Docker manager](#item-tech-news-15) ⭐️ 5.0/10
16. [CodeScoring article: local open AI models can take on parts of code audits](#item-tech-news-16) ⭐️ 5.0/10
17. [Jmix Reworked Its Documentation Assistant&\#x27;s Search After It Invented a Setting](#item-tech-news-17) ⭐️ 5.0/10
18. [Habr post proposes a guard against hanging Bash commands, but offers no details](#item-tech-news-18) ⭐️ 5.0/10
19. [A RISC-V processor runs inside Qwen 3.5&\#x27;s weights, using its layers as memory](#item-tech-news-19) ⭐️ 5.0/10
20. [GraphyLoop claims to merge Claude Code, Codex and Cursor into one workflow](#item-tech-news-20) ⭐️ 5.0/10
21. [Classgrid AI promotes an open-source tool that runs several AI models in GitHub projects](#item-tech-news-21) ⭐️ 5.0/10
22. [OpenMinion Alpha Runtime and CleverCloud&\#x27;s Three-Action AI Connector](#item-tech-news-22) ⭐️ 5.0/10
23. [Open-source Jira-to-pull-request AI workflow uses Claude Code or Copilot](#item-tech-news-23) ⭐️ 5.0/10
24. [Linux.do post floats ChatGPT Plus quota merge, promotes Web2Term](#item-tech-news-24) ⭐️ 5.0/10
25. [Kimi Connects to Gmail, Google Drive and Google Calendar](#item-tech-news-25) ⭐️ 5.0/10

**Financial News**
1. [FCC Bans Chinese Labs From Certifying U.S.-Bound Electronics](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Mistral releases Mistral Large 4 with open weights and lower API prices](https://mistral.ai/news/mistral-large-4-oss/) ⭐️ 9.0/10

Mistral released Mistral Large 4, the newest version of its Large model, and published its weights — the model files that anyone can download and run on their own hardware — on Hugging Face. Commenters say the hosted version is now priced at roughly half the preview&\#x27;s rate: $0.70 per million input tokens and $2.10 per million output tokens, against $1.36 and $4.18 for the preview \(a token is a chunk of text the model reads or writes, and prices are quoted per million of them\). Those figures and any capability improvements come from commenters rather than from the announcement text, so they are unverified. One commenter also flagged that the release reports a 96.6% refusal rate on malicious cyber requests — the highest it measures among open models — without giving a matching figure for how often the model refuses legitimate requests.

hackernews · kuberwastaken · Oct 29, 14:13 · [Discussion](https://news.ycombinator.com/item?id=50289418)

**「What &\#x27;open weights&\#x27; and the preview mean」** Mistral Large 4 is a general-purpose AI model from the French company Mistral that handles both text and images. Until now it was offered as a &quot;preview&quot; through Mistral&\#x27;s paid API, a service where other software sends requests to the model over the internet and pays for each chunk of text processed. Releasing the &quot;weights&quot; means publishing the billions of tuned numbers that make the model work, so outside teams can download it and run it on their own machines instead of only through Mistral&\#x27;s servers.

**「What it means in practice」** Anyone who tested the preview and set it aside on cost has a reason to re-run their comparison: one commenter who ran evaluations said the preview was &quot;not competitive&quot; at the old price and that the new price &quot;warrants a major reassessment.&quot; Because the weights are downloadable, a company can also run the model on its own servers instead of sending data to Mistral&\#x27;s hosted service, which matters for organizations with data-residency rules.

**「From the comments」** Commenters split between cost and safety. One reported that the price cut, plus improvements on top of the preview, makes the full release worth reassessing, while another questioned the refusal statistic as one-sided, noting that a model could score the same by rejecting everything. A third, writing for an EU-based company, said Mistral&\#x27;s API has worked well for them since it began offering third-party models alongside its own.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.mistral.ai/models/mistral-large-4-0">Mistral Large 4 - Mistral AI | Mistral Docs</a></li>
<li><a href="https://www.freeanswers.io/mistral-large-4/">Mistral Large 4 Guide: Open Weights, API, Pricing, Setup</a></li>

</ul>
</details>

**Tags**: `#Mistral Large 4`, `#open-weight models`, `#API pricing`, `#model release`

---

<a id="item-tech-news-2"></a>
### [OpenAI adds separate usage credits to its top ChatGPT plans](https://simonwillison.net/2026/Oct/29/api-credits/) ⭐️ 8.0/10

OpenAI&\#x27;s help center now lists a benefit giving subscribers to its $100, $200 and $500 ChatGPT plans the same dollar amount in API credits: $100, $200 or $500 respectively. An API is the connection other software uses to send requests to OpenAI&\#x27;s models; API use is billed separately from chatting in the ChatGPT app, and these credits pay for it. The credits apply to one API organization, the account that holds API projects and billing, according to the help page relayed by Simon Willison. The offer closely matches an earlier Anthropic benefit for its Max and Team plans; that version was described as giving expiring credits, while the relayed OpenAI page gives no expiry details.

rss · Simon Willison · Oct 29, 22:48

**「Context」** A ChatGPT subscription and API usage are normally two separate bills: the subscription pays for the chat app, while the API \(the pay-as-you-go way that software calls OpenAI&\#x27;s models directly\) is metered and charged separately. Earlier in October, Anthropic started giving its Max and Team subscribers credits equal to their monthly fee to spend through its API, and OpenAI&\#x27;s new benefit follows that same structure. OpenAI&\#x27;s documentation adds two conditions worth knowing: the credits are claimed for a single linked API account, and they do not raise the ChatGPT or Codex usage limits that come with the subscription.

**「What it means for subscribers」** Someone who already pays for a qualifying ChatGPT plan and also pays for API usage can now have up to the plan&\#x27;s dollar value of API charges covered by the subscription, reducing the second bill. Because the benefit is tied to one API organization, they should confirm which organization receives the credit before counting on it for a project.

<details><summary>References</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/20001626-api-credits-benefit-for-eligible-chatgpt-subscriptions">API credits benefit for eligible ChatGPT subscriptions | OpenAI ...</a></li>
<li><a href="https://developers.openai.com/api/docs/guides/chatgpt-api-credits">API credits for ChatGPT subscribers</a></li>

</ul>
</details>

**Tags**: `#openai`, `#chatgpt-subscriptions`, `#api-credits`, `#pricing`, `#anthropic`

---

<a id="item-tech-news-3"></a>
### [OpenAI&\#x27;s Tibo says ChatGPT Pro usage limits double on October 30](https://x.com/thsottiaux/status/2115851621137784832) ⭐️ 8.0/10

An OpenAI staff member who posts as Tibo said on X that the usage limits on ChatGPT Pro 100, Pro 200, Pro 500 and Business Premium will double starting October 30, 2026, according to a Telegram channel that relayed the post. A usage limit \(the cap on how much you can send or generate before a service makes you wait or charges more\) is the figure being doubled here. The relay gives no per-tier numbers, no link to an official OpenAI announcement, and does not explain what the 100/200/500 labels refer to; it adds that a separate allowance it calls Dot keeps its own quota, counted apart from the default one. Because this rests on a single relayed tweet, the doubling should be read as an announcement rather than a confirmed or measured change until OpenAI publishes its own notice.

telegram · zaihuapd · Oct 29, 17:12

**「Background」** ChatGPT Pro is OpenAI’s paid subscription; Pro 100, Pro 200 and Pro 500 are separate tiers, each with usage allowances rather than unlimited access. Those allowances are split between ordinary chat and work tools such as ChatGPT Work and Codex \(OpenAI’s coding assistant\), so one pool can change without the others. OpenAI’s help page says the weekly GPT-6 Pro chat limit on Pro 100 and Pro 500 is unchanged, and on Pro 200 only the lower limit was raised to match the higher one; a separate report says the Codex increase skips Pro 200 users who kept the older 20-times-Plus allowance.

**「What it means for Pro subscribers」** If you already pay for one of these plans, the practical effect is that the same monthly price now buys twice as many messages and coding tasks \(Codex is OpenAI&\#x27;s coding assistant\) before you hit a ceiling. Those tier names map to OpenAI&\#x27;s three monthly Pro plans at $100, $200 and $500, according to the company&\#x27;s help pages, and Pro 200 subscribers were moved onto a lower allowance when that tier reopened to new sign-ups on September 29, 2026, so the doubling is a partial give-back rather than a pure bonus for them. Because the only source here is a relayed tweet with no official OpenAI announcement, check the usage meter in your account settings before planning heavier work around the new limits.

<details><summary>References</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers">About ChatGPT Pro tiers | OpenAI Help Center</a></li>
<li><a href="https://dzen.ru/a/auOT8VOA8hIEiN5N">OpenAI удвоила квоту Codex на Pro -тарифах и отменила... | Дзен</a></li>
<li><a href="https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers">About ChatGPT Pro tiers - OpenAI Help Center</a></li>
<li><a href="https://www.toolcolumn.com/learn/chatgpt-pro-100-vs-200-vs-500">ChatGPT Pro 100 vs Pro 200 vs Pro 500: Which Pro Plan to Buy</a></li>

</ul>
</details>

**Tags**: `#ChatGPT Pro`, `#OpenAI`, `#subscription quotas`, `#rate limits`, `#pricing`

---

<a id="item-tech-news-4"></a>
### [An open-source tiny world model plays games on a Raspberry Pi Pico 2 W](https://github.com/SheepSeb/tinyworldformer) ⭐️ 7.0/10

A GitHub project called tinyworldformer runs a &quot;world model&quot; — a program that learns from example game footage and then generates the next frames itself, instead of running a normal game engine — on a Raspberry Pi Pico 2 W, a matchbox-sized microcontroller board with far less memory and computing power than a phone. The code is open source, so anyone can download it. The material supplied here does not give the model&\#x27;s size, the frame rate it reaches, or installation steps, so how smoothly the games actually play cannot be confirmed. Commenters described it as a working demo rather than a mock-up, and several asked follow-up questions that the supplied evidence does not answer.

hackernews · airinei · Oct 29, 20:32 · [Discussion](https://news.ycombinator.com/item?id=50295450)

**「Background」** A world model is a program that has learned to predict what happens next in an environment; this one takes the current game frame and a button press, then predicts the next frame and any reward. The project fits two small neural networks \(pattern-recognition programs trained on examples\) onto a Raspberry Pi Pico 2 W — a cheap microcontroller board, the kind of tiny computer used inside gadgets rather than a PC — with one network generating the game and the other choosing moves to play it.

**「What it means if you want to try it」** This is something you would have to assemble yourself from the public code repository; no setup instructions, supported-game list, or hardware shopping list appear in the material supplied here, and the only game named by commenters is a miniature version of Doom. Treat it as a demonstration of how small the hardware can get, not as a product you can install and play today.

**「What commenters asked」** One commenter asked which hardware was used to train the model, saying the answer was not obvious from the project&\#x27;s readme. Another remarked that &quot;looped transformers&quot; — a design where the same small network is applied repeatedly in a loop — were needed for mini-Doom but not for simpler games, while a third said they had not known neural networks could behave so deterministically and asked whether the effect is similar to overfitting, and whether a single model serves every game. These are readers&\#x27; questions and impressions, not confirmed details about the project.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/SheepSeb/tinyworldformer">GitHub - SheepSeb/tinyworldformer</a></li>
<li><a href="https://github.com/SheepSeb/tinyworldformer/blob/main/README.md">tinyworldformer/README.md at main · SheepSeb ... - GitHub</a></li>

</ul>
</details>

**Tags**: `#world-model`, `#raspberry-pi-pico`, `#microcontroller-ai`, `#edge-inference`, `#open-source-project`

---

<a id="item-tech-news-5"></a>
### [OpenAI Codex 0.166.0 adds transcript search and a GPT-6.1 Terra model listing](https://github.com/openai/codex/releases/tag/rust-v0.166.0) ⭐️ 6.0/10

OpenAI has released Codex 0.166.0, a new version of its command-line coding assistant \(a program that developers operate by typing commands rather than clicking\). The update adds keyboard selection and search in the transcript \(the on-screen record of the conversation\), including word-, line-, and page-at-a-time movement and customizable shortcuts, plus a &quot;codex queue --resume&quot; option that wakes a conversation that is no longer loaded when a message is queued to it. It also adds a model called GPT-6.1 Terra to Codex&\#x27;s built-in list of models it can use and to the model lists of Google Cloud&\#x27;s Vertex AI and Amazon Bedrock \(two services for running AI models\), but the release notes give no details on its capabilities, price, or when users can select it. The release also fixes a case where approved permission settings could be lost when a conversation was resumed or copied, and adds &quot;codex doctor --network-only&quot; for checking configuration, connectivity, and WebSocket \(live two-way connection\) problems.

github · github-actions\[bot\] · Oct 29, 19:47

**「Background」** Codex is OpenAI&\#x27;s coding assistant that runs as a command-line program: a text-only tool you operate by typing commands in a terminal instead of clicking through an app. This v0.166.0 release is a routine update to that program, following v0.165.0, and its model catalog is the built-in list of models the program is allowed to connect to.

**「What changes for Codex users」** Codex&\#x27;s model picker now offers GPT-6.1 Terra next to the existing choices, including when the tool is pointed at Google&\#x27;s Vertex AI or Amazon&\#x27;s Bedrock cloud services, so people can select it without reinstalling anything. The release note says nothing about price, speed, or context window \(how much text the model can hold in view at once\), so anyone switching has to look those up separately: third-party resellers advertise roughly $1 per million input tokens \(the text chunks models read and are billed by\) and a context window of about one million tokens, but those are unofficial listings that disagree with each other and that OpenAI&\#x27;s notes do not confirm. If you pay per use, check OpenAI&\#x27;s official pricing and model documentation before making it your default, since the cost of the same amount of work can change sharply from one model to the next.

<details><summary>References</summary>
<ul>
<li><a href="https://benchlm.ai/models/gpt-6-1-terra">GPT - 6 . 1 Terra Benchmarks &amp; Pricing (October 2026)</a></li>
<li><a href="https://tokenharbor.ai/models/gpt-6.1-terra">GPT - 6 . 1 Terra API — $1.00/1M in · Token Harbor</a></li>

</ul>
</details>

**Tags**: `#codex-cli`, `#openai`, `#coding-agents`, `#release-notes`, `#model-catalog`

---

<a id="item-tech-news-6"></a>
### [Developer Rebuilt a Broken Legacy API With a Coding Agent Kept Blind to the Old Code](https://habr.com/ru/articles/1101314/?utm_campaign=1101314&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A developer writing on the Russian tech site Habr describes rebuilding a failing legacy system — old code still in daily use — by moving it into a &quot;clean room&quot;: a separate setup where an AI coding agent \(software that writes and edits code on its own\) produces a new implementation without ever seeing the original. The starting point was a service where two of every three requests to its API \(the interface one program uses to call another\) returned HTTP 500, a generic server-failure error, after repeated rounds of AI-written patches had turned the code into what the author calls a tangle of &quot;neuroslop.&quot; The post says the article covers the transfer procedure, 15 rules meant to stop the agent from producing new quick fixes, and an experiment over 36 runs of DeepSeek, a Chinese AI model family, testing how much the agent&\#x27;s behavior depends on which code and which rules it is shown. Only this short teaser is available, so the procedure, the rules and any measured results from those 36 runs cannot be checked here.

rss · Habr AI · Oct 29, 14:32

**「Background」** An API is the interface one program uses to request work from another; a “legacy” API is an old one that is fragile and expensive to change. In this clean-room setup, a coding agent \(software that edits code from written instructions\) is asked to build a replacement without seeing the old implementation, so it cannot simply copy the accumulated patches. The Habr item is only a short teaser: it says the full article contains the transfer method, 15 protective rules, and a 36-run DeepSeek experiment, but the teaser itself provides no code, rules, or results.

**「Why it matters in practice」** The approach is a template for anyone overseeing a rewrite of crumbling software with AI help: hide the old code from the agent so it cannot copy the old workarounds, and give it an explicit written list of prohibitions instead. The teaser gives no outcome numbers, no error rates and no comparison against ordinary patching, so it should be treated as one team&\#x27;s method report rather than evidence that the rebuilt system works better.

**Tags**: `#coding agents`, `#DeepSeek`, `#legacy refactoring`, `#agent workflows`, `#prompt configuration`

---

<a id="item-tech-news-7"></a>
### [A Beginner&\#x27;s ESP32 Desk Screen for Tracking LLM Subscription Quotas](https://habr.com/ru/articles/1101302/?utm_campaign=1101302&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A maker who says he had no electronics background has published a Habr write-up of a desk-side display, built around an ESP32 board \(a cheap, low-power microcontroller\), that shows how much of his paid AI chatbot quotas he has left. The problem it addresses: he holds several subscriptions to LLM \(large language model\) services and each one limits usage on its own schedule — a five-hour window, a weekly window and a monthly ceiling — with the remaining allowance visible only by opening the relevant website. In his design, a lightweight Windows program gathers the limits for four subscriptions and the small ESP32 screen shows them within view of the keyboard. The supplied excerpt covers the parts he bought \(board, an unspecified screen, a rotary encoder knob\) and the goal, but not the code, wiring, or confirmation that the finished device works end to end.

rss · Habr AI · Oct 29, 14:15

**「Background」** Paid AI chatbot subscriptions usually cap usage in rolling windows — for example a five-hour window, a weekly cap and a monthly ceiling — and each provider resets them at a different time on a different website, so seeing what is left means opening several browser tabs. The ESP32 is a cheap, credit-card-sized microcontroller board with built-in Wi-Fi, the kind of part used in hobby weather stations and smart-home gadgets: it can drive a small screen, but it has no desktop operating system, so the author had to write the device&\#x27;s own software \(firmware\) in Rust, a programming language he already knew. He describes himself as having no electronics background, saying that until recently he could not tell a transistor from a resistor.

**「What it means in practice」** The quotas are collected by a companion Windows application rather than by the display itself, so the screen works as a readout for a PC that has to be running — it is not a standalone gadget. Because the available portion of the article gives no build steps or source code, someone wanting the same setup cannot reproduce it yet.

**Tags**: `#ESP32`, `#LLM quotas`, `#hardware`, `#monitoring dashboard`, `#DIY build`

---

<a id="item-tech-news-8"></a>
### [A YAML rulebook for keeping a Pydantic AI agent on task](https://habr.com/ru/articles/1101120/?utm_campaign=1101120&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A Russian-language post on the Habr developer blog describes putting an AI agent built with Pydantic AI — a toolkit for creating agents, programs in which a model can take several steps and call outside tools — inside a fixed workflow written in YAML, a plain-text configuration format. The setup also uses MCP tools \(a common connector that lets a model use outside services\) and a debugging tool the author calls Studio. The author argues that agents left free to choose their own steps are too unreliable for business automation and promises accompanying code, but the supplied excerpt contains only that premise: no version numbers, setup steps, measured results, or code are visible.

rss · Habr AI · Oct 29, 09:50

**「What the setup builds on」** An AI agent is a model that decides for itself which steps to take and which tools to call, which is why the author says it goes wrong on multi-step business tasks. Pydantic AI is a set of building blocks programmers use, in the widely used Python language, to assemble such agents, and Pydantic&\#x27;s own documentation says it can already connect them to outside systems through MCP \(Model Context Protocol\), an open standard for plugging an assistant into things like databases, file storage or web services rather than writing a custom link for each one. The article&\#x27;s premise is to remove that free choice by describing the steps in YAML, a plain-text configuration format in which indentation, not punctuation, defines the structure of each step.

**「What it means in practice」** For teams building agents that must carry out a business process, the described approach would trade the agent&\#x27;s freedom to decide each step for a fixed sequence that is easier to trace and repeat. The catch is that nothing here can be evaluated or adopted yet: without the code, example configurations, or version details, a reader cannot reproduce the sandbox or check whether it works with their current Pydantic AI setup.

<details><summary>References</summary>
<ul>
<li><a href="https://pydantic.dev/docs/ai/capabilities/mcp/">MCP Capability | Pydantic Docs</a></li>
<li><a href="https://pydantic.dev/docs/ai/mcp/overview/">Model Context Protocol (MCP) | Pydantic Docs</a></li>

</ul>
</details>

**Tags**: `#Pydantic AI`, `#MCP`, `#AI agents`, `#workflow orchestration`, `#developer tooling`

---

<a id="item-tech-news-9"></a>
### [Anthropic raises Claude API request limit to 128 MB](https://platform.claude.com/docs/en/api/overview#request-size-limits) ⭐️ 6.0/10

Anthropic has raised the maximum request size on Claude&\#x27;s application programming interface \(API, the channel software uses to send requests directly to the model\) from 32 MB to 128 MB, about four times the previous cap. The increase applies to the Messages interface, used to send prompts and conversations, and the Token Counting interface, used to estimate how many tokens \(the basic units of text or image data the model processes\) a request contains. The change is aimed at requests carrying many images, large PDF files, or complex tasks that involve operating a computer, and is intended to reduce failures caused by oversized requests. For requests containing more than 20 images, the maximum resolution allowed for each image also rose from 2,000 to 3,000 pixels. Requests made through third-party cloud platforms may still be subject to those platforms&\#x27; own size limits.

telegram · zaihuapd · Oct 30, 05:13

**「Why request size matters」** An API \(application programming interface\) is the channel software uses to send Claude a request programmatically rather than through the chat window. Everything needed for one turn — the instructions, the images and any attached PDFs — travels together as a single package whose size is measured in megabytes, so a batch of high-resolution images or a long scanned document can hit the ceiling quickly. Until this change that ceiling was 32 MB, meaning oversized requests were simply rejected rather than trimmed.

**「What it means」** Teams that send scanned documents, image-heavy reports, or long PDFs through the API can fit more material into a single request without hitting the old 32 MB ceiling. Anyone reaching Claude through a third-party cloud provider should check that provider&\#x27;s request-size limit, which may be lower than Anthropic&\#x27;s new 128 MB cap.

**Tags**: `#Claude API`, `#request limits`, `#Anthropic`, `#multimodal`, `#API access`

---

<a id="item-tech-news-10"></a>
### [YC Labs Demonstrates Swarms of AI Characters in Minecraft and Mindustry](https://labs.ycombinator.com/projects/games/index.html) ⭐️ 5.0/10

YC Labs published a project report on running many AI agents—software that uses a large language model \(a system trained on text to produce responses and decisions\) to decide what to do—at the same time inside the games Minecraft and Mindustry. The supplied material presents this as a lab demonstration, not a product release, and does not name the models used, give prices or setup details, or offer installable code. The item drew discussion on the tech site Hacker News, including a concrete replication suggestion and criticism that AI-driven characters respond too slowly.

hackernews · sandslash · Oct 29, 21:40 · [Discussion](https://news.ycombinator.com/item?id=50296486)

**「Context」** The report behind this discussion comes from YC Labs, which says it is running a new Minecraft colony with 25 agents built on &quot;GPT-6.1 Terra&quot; and is streaming it on Twitch. An earlier public write-up describes 50-agent Minecraft colonies and team games, including a Mindustry match that one model won 6-1 over another. In plain terms, an &quot;LLM agent&quot; is a model given a goal and a set of actions it can take on its own; Minecraft and Mindustry serve as cheap, open-ended test worlds where many such agents interact at once, which is why researchers use them to watch coordination and group behavior emerge.

**「What it means」** For anyone who wants to try this, the report is not a package to install: reproducing it means building the connection between an AI model and a game yourself. The community suggestion uses the free, community-built Luanti/Minetest game rather than Minecraft, so it is a starting point, not an exact copy of the original setup.

**「Community discussion」** One commenter gave a concrete way to try this: install Luanti with Minetest \(a free, community-built Minecraft-like game\) and have the agent write an add-on that connects to the game&\#x27;s built-in programming language, Lua, so it can change the world or control computer-run characters. Another argued that language models are poorly suited to fast games because of the delay between asking for an action and getting it, while a third said the Minecraft agents behaved almost turn-based, taking turns rather than acting continuously; those are discussion opinions, not report findings.

<details><summary>References</summary>
<ul>
<li><a href="https://labs.ycombinator.com/projects/games/index.html">Agents in Games · Labs</a></li>
<li><a href="https://daily.dev/posts/we-ran-ai-agent-swarms-in-minecraft-and-mindustry-cmnuahc2q">We ran AI agent swarms in Minecraft and Mindustry - daily.dev</a></li>

</ul>
</details>

**Tags**: `#ai-agents`, `#multi-agent-swarms`, `#minecraft`, `#llm-latency`, `#hackernews`

---

<a id="item-tech-news-11"></a>
### [IBM&\#x27;s Granite Switch gets a 4.1.1 update billed as routine](https://huggingface.co/blog/ibm-granite/granite-switch-4-1-1) ⭐️ 5.0/10

IBM published version 4.1.1 of Granite Switch, a family of AI models distributed through the Hugging Face model-sharing site, in a blog post dated October 29, 2026. The headline frames the release as maintenance rather than a leap: &quot;Update models like you update software.&quot; An open-weight model is one whose internal settings can be downloaded and run on your own machines instead of only through a company&\#x27;s online service, and the review of this item describes Granite Switch as likely belonging to that category without confirming it. No changelog, file sizes, benchmark figures, licensing terms or supported languages were available in the material reviewed, so what actually differs from the previous version is unknown.

rss · Hugging Face Blog · Oct 29, 13:37

**「A patch update, not a new generation」** The 4.1.1 label signals a patch: a small, numbered update rather than a new generation of the model. It follows IBM&\#x27;s Granite Switch 4.1 by about a week and is described as fully backward-compatible, so anyone already using 4.1 does not need to migrate. The changes are a refreshed speech-recognition model \(software that converts speech into text\) for 10 languages with punctuation and capitalization, plus an improved “Decision” add-on.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aitoolsoasis.com/en/news/ibm-granite-switch-411-patch-style-model-updates-without-1793293374852">IBM Granite Switch 4.1.1: Patch-Style Model Updates Without ...</a></li>
<li><a href="https://veriwire.news/daily-ai-news/granite-switch-411-update-models-like-you-update-245346/">Granite Switch 4.1.1 — Update models like you update software</a></li>

</ul>
</details>

**Tags**: `#IBM Granite`, `#model release`, `#open-weight models`, `#Hugging Face`

---

<a id="item-tech-news-12"></a>
### [Kimi K3 open-weight model claimed to beat GPT and Anthropic on some tests](https://habr.com/ru/companies/pt/articles/1101328/?utm_campaign=1101328&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr post introduces Kimi K3, a model from Moonshot AI whose weights — the downloaded files that let someone run the model on their own machines — are published on GitHub as an open-weight release. The post says that on some independent benchmarks \(standardized tests used to compare models\) Kimi K3 beats closed models from OpenAI \(GPT\) and Anthropic. It also links to an official technical report from the developers on arXiv, the preprint server, which the author says he read to explain the results. The excerpt itself gives no benchmark scores, no model size or parameter count, no license terms and no hardware requirements, so the comparison cannot be checked from this text alone; the performance claim rests on the post and the developers&\#x27; report.

rss · Habr AI · Oct 29, 15:53

**「What &quot;open weights&quot; means here」** A model is called &quot;open-weight&quot; when its trained files — the numeric settings that make it produce answers — can be downloaded and run on your own machines, instead of being reachable only through a company&\#x27;s paid online service. GPT \(from OpenAI\) and Anthropic&\#x27;s Claude are the closed kind, and open models have generally trailed them because their developers have had less computing power and data to train with. Kimi K3 comes from Moonshot AI, the Chinese company behind the Kimi chatbot, which has published the files on GitHub together with a technical report on arXiv, a site where researchers post papers before peer review — so the performance comparisons in this post trace back to the developers&\#x27; own document rather than to an outside audit.

**「What this means in practice」** A model whose weights can be downloaded and installed on your own machines matters most to organisations that cannot send data to an outside provider: they can keep everything in-house instead of paying per-use fees to a hosted service. The catch is hardware. Third-party write-ups describing the release report a 2.8-trillion-parameter model with about 104 billion parameters active at any moment and a context window of one million tokens \(roughly the length of several full-length books\) — figures the Habr post itself does not give, and a scale that puts the model well beyond an ordinary desktop computer. Because the post supplies no licence terms, no hardware requirements and no benchmark numbers, anyone considering a trial should read the linked GitHub repository and the official report first, rather than assume it can replace a paid chatbot subscription or fit existing equipment.

<details><summary>References</summary>
<ul>
<li><a href="https://k3-kimi.com/">Kimi K 3 : 2.8T Open-Weight Model — Benchmarks , Pricing &amp; Guides</a></li>
<li><a href="https://kie.ai/blog/kimi-k3-moonshot-open-frontier-model">Kimi K 3 Release: Signal vs Noise on Moonshot &#x27;s 2.8T Model</a></li>

</ul>
</details>

**Tags**: `#Kimi K3`, `#open-weight models`, `#Moonshot AI`, `#benchmarks`, `#model release`

---

<a id="item-tech-news-13"></a>
### [vue-llm offers Vue and Nuxt developers a ready-made AI chat kit](https://habr.com/ru/articles/1101308/?utm_campaign=1101308&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A developer has published vue-llm, a free, open-source add-on for Vue and Nuxt — a widely used toolkit for building websites and web apps — that supplies the parts needed for a chatbot interface: replies that appear word by word as the model writes them, tool calling \(letting the model trigger actions inside the app\), and Generative UI \(where the model&\#x27;s answer decides which interface elements are drawn\). The author says most ready-made chat components are written for React, Vue&\#x27;s main rival, so Vue developers end up rebuilding the same chat plumbing by hand. The library supports Vue 3 and Nuxt, and according to the author also Vue 2.7, and installs with the command \`npm i vue-llm\`; the code is on GitHub and the documentation is in Russian. A demo playground runs a model entirely inside the visitor&\#x27;s browser through WebGPU \(a browser feature that lets web pages use the graphics card for computation\), so no API key — the paid credential normally required to call a hosted model — is needed. This is the author&\#x27;s own announcement, and it gives no version number, independent testing, or performance figures.

rss · Habr AI · Oct 29, 14:35

**「Why this library exists」** Vue is a toolkit developers use to build web interfaces, and Nuxt is a framework built on top of it for complete web apps. Most ready-made tools for putting a large language model \(the software behind chatbots\) into an interface have been written for React, a competing toolkit, so Vue developers have had to adapt those tools or write the chat state, streaming text, and model-triggered actions themselves.

**「What it means in practice」** For someone putting a chat feature into a Vue site, the practical gain is that reply streaming and chat state no longer have to be written from scratch. The compatibility catch is the no-key demo: it depends on WebGPU, which is not available in every browser or on older devices, so an in-browser model is best treated as a showcase rather than something every visitor can rely on.

**Tags**: `#Vue`, `#Nuxt`, `#LLM SDK`, `#WebGPU`, `#open-source`

---

<a id="item-tech-news-14"></a>
### [How to build a local AI news agent with Ollama and LangGraph](https://habr.com/ru/articles/1101266/?utm_campaign=1101266&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr tutorial lays out a do-it-yourself system that collects news feeds and uses an AI agent—software that can choose and call tools such as search on its own—to work with them, with all models running on the author&\#x27;s own computer instead of through cloud services such as OpenAI or Anthropic. The author presents full independence from outside AI providers, including resilience to sanctions, as the reason to take on that extra setup. The design is a RAG system \(retrieval-augmented generation: the software first finds relevant news items, then has a language model write an answer from the passages it found\), built with Ollama \(software for running downloadable AI models locally\), the Qwen 2.5 14B and BGE-M3 models, and LangGraph \(a framework for organizing multi-step agent workflows\). The author says the system gathered more than 12,000 news items in two weeks; the supplied excerpt gives the component list and that usage claim, but no benchmark, code, or configuration to reproduce it.

rss · Habr AI · Oct 29, 12:59

**「Background」** Retrieval-augmented generation \(RAG\) means the software first searches a private document collection and then gives the most relevant passages to a language model, so answers are grounded in those documents rather than only in what the model learned during training. Ollama is a free program for running language models on your own computer or server, and LangGraph is a toolkit for arranging a model’s steps and tool calls into a workflow. The Qwen 2.5 14B model in this build is an open-weight model from Alibaba that can be downloaded and run locally; “14B” refers to roughly 14 billion parameters, a rough measure of model size.

<details><summary>References</summary>
<ul>
<li><a href="https://apxml.com/models/qwen2-5-14b">Qwen2.5-14B - VRAM, Specs &amp; Benchmarks - apxml.com</a></li>

</ul>
</details>

**Tags**: `#self-hosted RAG`, `#local LLMs`, `#Ollama`, `#LangGraph`, `#Qwen`

---

<a id="item-tech-news-15"></a>
### [Developer gives Claude Code a guarded entry into his Docker manager](https://habr.com/ru/articles/1101202/?utm_campaign=1101202&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A developer who maintains d9c, a text-based \(terminal\) manager for Docker containers running on remote servers, says he added a way for AI agents to use it: a command-line mode built for machines rather than people, an MCP server \(Model Context Protocol, a common plug-in standard that lets an AI assistant call outside tools\), and ten &quot;skills&quot; — packaged instructions that teach the agent specific tasks. The aim was to let Claude Code, Anthropic&\#x27;s terminal-based coding assistant, inspect his remote servers without giving it docker.sock, the control socket that grants full power over Docker on a machine. He kept the agent&\#x27;s toolset to twelve tools instead of forty and designed the setup so a human confirms deletions. Even so, the post says the agent deleted a staging environment without asking him first; the excerpt available here is an introduction only and contains no code, installation steps, or detail on how the permissions are actually enforced.

rss · Habr AI · Oct 29, 11:44

**「Context」** d9c is the author&\#x27;s own text-based tool for managing Docker containers — isolated application packages — running on remote servers. Docker&\#x27;s control socket, docker.sock, is effectively an all-powerful admin channel: anything that can reach it can start, stop, or delete containers, so handing it to an AI agent gives the agent the same power as a human administrator. The author instead built a narrower entry point: an MCP server \(a standard plug that exposes tools to AI assistants such as Claude Code\) plus a command-line mode and a set of skills, with the stated aim of separating &quot;inspect&quot; from &quot;destroy.&quot;

**「What it means in practice」** For anyone pointing a coding agent at real servers, the reported staging deletion is the part to act on: the confirmation step is what actually protects you, and here it did not hold. Keeping the agent&\#x27;s tool list short and requiring an explicit human yes for anything destructive matters more than the number of capabilities offered — as does avoiding docker.sock, which would let an agent control every container on the machine, not just the ones you meant to expose.

**Tags**: `#MCP`, `#coding agents`, `#Claude Code`, `#Docker`, `#developer tooling`

---

<a id="item-tech-news-16"></a>
### [CodeScoring article: local open AI models can take on parts of code audits](https://habr.com/ru/companies/codescoring/articles/1101180/?utm_campaign=1101180&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

CodeScoring, a vendor of software supply-chain security tools, published a Habr article arguing that a team can run an open AI model \(one whose weights anyone can download and run\) on a developer&\#x27;s own computer and connect it to code-scanning tools, instead of buying a cloud subscription. The article&\#x27;s central claim is that installing the model is the easy part; the hard part is deciding which pieces of a security audit to hand over. Reading a single scanner warning, tracing where a user&\#x27;s data travels through the program, and running a multi-step investigation of the whole application are tasks of very different size, and giving a whole audit to one small model at once makes it impossible to judge which individual tasks it can actually do. The supplied excerpt ends before any model name, version, hardware requirement, configuration or measured result, so it reads as a way of working rather than a tested, repeatable setup.

rss · Habr AI · Oct 29, 10:51

**「Background」** Application security \(AppSec\) is the work of finding and fixing security weaknesses in software, often with automated code analyzers that scan an application&\#x27;s written code and flag suspicious lines for a person to review. A large language model \(LLM\) is the text-generating AI behind tools such as chatbots. In this context, an open model is distributed as files a team can download and run itself, and a local model runs on the team&\#x27;s own laptop or desktop instead of through a cloud subscription.

**「What it means in practice」** For a team that is not allowed to send source code to an outside service, the article describes a route where the model, the code and the results all stay on machines the team controls, and where the team chooses what gets passed to the model. The practical catch is that the excerpt gives no model names, hardware figures or comparison data, so nobody can pick a setup from it; a team would have to test candidate models against their own scanner output and split audit work into small steps they can check one by one.

**Tags**: `#local-llm`, `#open-weight-models`, `#appsec`, `#self-hosted`, `#ai-workflow`

---

<a id="item-tech-news-17"></a>
### [Jmix Reworked Its Documentation Assistant&\#x27;s Search After It Invented a Setting](https://habr.com/ru/companies/haulmont/articles/1100862/?utm_campaign=1100862&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

The Jmix team, which maintains an open-source platform for building business applications in Java, says it has rebuilt the search component of the AI assistant that answers questions about Jmix documentation. The trigger was a deliberately tricky test question — which value of a setting called repeatCount would make a timer fire five times — to which the assistant confidently returned ready-to-use configuration code \(XML\) even though Jmix has no such setting. The assistant has answered Jmix-only questions since late 2023, when it was built on ChatGPT-4, and the same document index also serves outside AI agents that connect through MCP \(Model Context Protocol, a standard way for assistants to call external tools and data sources\). The published excerpt is introductory: it gives no new search architecture, configuration, or measured accuracy before and after the rebuild.

rss · Habr AI · Oct 29, 10:00

**「Background」** An assistant of this kind typically uses retrieval-augmented generation, or RAG: before answering, the software searches a prepared index of the product&\#x27;s documentation and passes the matching passages to a language model, which then writes the reply. The quality of that lookup largely decides whether the model works from the right material or fills gaps from memory. Jmix previously kept one developer on duty to answer every customer question, and the assistant was meant to take over the simplest ones.

**「What it means in practice」** For anyone who uses a documentation chatbot to write configuration, the episode shows the failure to watch for: an answer can look finished and specific — complete with a setting name and code — while referring to something the product does not have. Because the excerpt contains no details of the new search design or accuracy figures, there is no evidence yet that the rebuild fixes this, so generated configuration should still be checked against the official reference.

**Tags**: `#RAG`, `#documentation`, `#AI assistants`, `#developer tooling`, `#Jmix`

---

<a id="item-tech-news-18"></a>
### [Habr post proposes a guard against hanging Bash commands, but offers no details](https://habr.com/ru/articles/1101048/?utm_campaign=1101048&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr article argues that AI coding agents — programs that can run terminal commands as part of a task — can freeze when they generate a shell command with a small mistake, such as a misplaced quotation mark, and proposes using a deterministic finite-state machine \(a fixed set of rules that checks a command step by step\) inside a PreToolUse hook \(a checkpoint that runs before an agent is allowed to use a tool\) to stop the bad command before it runs. The published excerpt, however, is only a teaser: it contains no hook configuration, state-machine design, reproduction, or evidence that the approach works.

rss · Habr AI · Oct 29, 08:31

**「What hooks and state machines have to do with it」** Claude Code, Anthropic&\#x27;s coding agent, lets users attach &quot;hooks&quot; — small shell commands it runs automatically at fixed points in its own work, such as before or after it uses a tool; the PreToolUse hook fires just before the agent runs a command, so a check placed there can inspect or block that command before it reaches the terminal. The Habr post&\#x27;s premise is that an agent which mistypes a single character in a terminal command can leave the shell waiting forever, freezing the agent, and that pattern-matching checks miss such cases while a state machine — a checker that walks a fixed list of states step by step instead of hunting for text patterns — would catch them. The supplied excerpt contains only the introduction, with no hook configuration, state-machine design, or test results.

**「What this means in practice」** For people who use coding agents, there is no adoptable fix here: without the hook code, state definitions, or a tested example, they cannot add this guard to their own setup or judge whether it would prevent hangs. The post should be treated as a description of a failure mode, not as a working safety measure.

<details><summary>References</summary>
<ul>
<li><a href="https://code.claude.com/docs/en/hooks-guide">Automate actions with hooks - Claude Code Docs</a></li>
<li><a href="https://code.claude.com/docs/en/hooks">Hooks reference - Claude Code Docs</a></li>

</ul>
</details>

**Tags**: `#coding agents`, `#Claude Code hooks`, `#shell safety`, `#developer tooling`, `#FSM`

---

<a id="item-tech-news-19"></a>
### [A RISC-V processor runs inside Qwen 3.5&\#x27;s weights, using its layers as memory](https://habr.com/ru/articles/1101030/?utm_campaign=1101030&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A translated post on the Russian tech site Habr describes Qwenputer, a hobbyist project that compiles a 32-bit RISC-V processor \(an openly licensed chip design standard; this one implements the basic RV32IM instruction set\) into the numerical weights of Qwen 3.5 4B, a small open language model. The processor occupies 11 layers placed in front of Qwen&\#x27;s 32 layers, and its working memory is the model&\#x27;s own Gated DeltaNet layers — an internal memory mechanism — configured with gate and write strength set to 1 and one-hot keys \(a key with a single active position\) so that each write overwrites exactly one row of stored state and each read returns the exact value rather than an approximation. The author reports that the core passes the official riscv-tests suite and runs C and MicroPython inside the model&\#x27;s forward passes \(one run of input through the network\) with no external tools, and that on long NUPA arithmetic accuracy went from 48.6% to 100%, with no divergence from a reference machine across roughly 230,000 output positions. The post explains the design, its limits, and how a file system was attached to the model. It is a write-up of a build, not a released repository or an install guide.

rss · Habr AI · Oct 29, 08:14

**「What came before」** Qwenputer is not a new model but a set of extra layers attached to the stock Qwen 3.5 4B — the &quot;4B&quot; means 4 billion parameters, the numbers that store what a model has learned. An earlier version of the project compiled a CHIP-8 game console, the simple virtual machine behind 1970s-style games, into the same model, according to the project&\#x27;s GitHub page \[tool-1-1\]. This version can act as a general-purpose processor because of how Qwen 3.5 is built: three of every four of its attention layers use Gated DeltaNet, a mechanism that carries a running memory forward step by step and keeps a state matrix per head, updated by a rule called the delta rule — the property that makes those layers usable as writable memory \[tool-1-2\].

**「What it means in practice」** For anyone using Qwen 3.5 or another local model, nothing changes about cost, speed, or answer quality, and the project gives no reason to switch models or tools. It is also not something a reader can try: the post describes the construction but supplies no repository, install steps, or parts list, so the test results and the 48.6%-to-100% figure should be read as the author&\#x27;s own report rather than an independently reproduced measurement.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/divagr18/qwenputer">GitHub - divagr18/ qwenputer : A computer , compiled into the weights...</a></li>
<li><a href="https://divagr.com/blog/qwenputer">Qwenputer : a fully functioning, deterministic RISC - V CPU inside...</a></li>

</ul>
</details>

**Tags**: `#Qwen`, `#RISC-V emulation`, `#DeltaNet`, `#LLM internals`, `#research demo`

---

<a id="item-tech-news-20"></a>
### [GraphyLoop claims to merge Claude Code, Codex and Cursor into one workflow](https://github.com/chadixearth/graphyloop) ⭐️ 5.0/10

A Telegram channel post is promoting GraphyLoop, an open-source project hosted on GitHub that claims to combine several AI coding assistants — Claude Code, Codex and Cursor — into a single setup, adding persistent memory, several AI agents working in parallel, and an MCP server \(a standard connector that lets an AI assistant reach outside tools\). The post says it can be installed with npx \(a command that downloads and runs a program without a separate install step\), as a Claude Code plugin, or from the MCP registry. It gives no version number, no screenshots, no installation detail and no sign of how many people use it, so the claimed features are unverified. The second half of the post promotes a separate &quot;skill library&quot; for Claude Code containing templates for making AI video and sales copy, which is unrelated to the GraphyLoop tool itself.

telegram · aipluscn · Oct 29, 14:24

**「Background」** The tools GraphyLoop names are separate products: Claude Code and Codex are AI coding assistants from Anthropic and OpenAI that work from a text command line and can edit files and run commands, while Cursor is a code editor with an AI assistant built in. Each normally keeps its own conversation and forgets it when a session ends, which is why &quot;persistent memory&quot; \(a stored record the assistant can reuse next time\) and &quot;multi-agent&quot; working \(several assistants sharing one task\) are add-ons rather than built-in features. MCP — the Model Context Protocol, an open standard that lets an AI assistant call outside tools and data — is the usual way such extras get plugged in, and a marketplace listing describes GraphyLoop as orchestrating these workflows with coordinated agent teams, persistent memory and a five-stage delivery process across OpenCode, Claude Code, Codex and Cursor.

**「What it would mean in practice」** The pitch is aimed at people who already pay for or use Claude Code, Codex or Cursor: instead of moving between them, and losing the thread of a project each time, they would run one wrapper that keeps memory and coordinates agents. Because the post names no versions, requirements or compatibility beyond those three tools, anyone trying it should expect to set it up themselves and check that it works with their current tool versions before relying on it for real work.

<details><summary>References</summary>
<ul>
<li><a href="https://mcpmarket.com/server/graphyloop">GraphyLoop : AI Agentic Workflow Kit for Coding Harnesses</a></li>

</ul>
</details>

**Tags**: `#claude-code`, `#mcp`, `#ai-coding-agents`, `#open-source`, `#github`

---

<a id="item-tech-news-21"></a>
### [Classgrid AI promotes an open-source tool that runs several AI models in GitHub projects](https://github.com/Classgrid/Classgrid_Agent) ⭐️ 5.0/10

A post on Telegram, a messaging app, announced Classgrid AI, described as a free-to-reuse \(open-source\) tool that plugs several AI models into GitHub, the website where programmers store and share code. The post says the tool lets a user call Claude, DeepSeek, GLM, Kimi, Qwen and Mistral — rival AI models from different companies — from inside a GitHub project to edit and run code. The announcement itself carries no version number, no installation instructions, no price or usage limits, and no test results showing the tool works; the promised setup steps sit behind two links to other Telegram posts. It should therefore be read as a promotion for an unverified project, not as a demonstrated release.

telegram · aipluscn · Oct 29, 14:24

**「Background」** An AI “agent” is software that can carry out steps toward a goal, such as editing files, rather than only answering a single question. Classgrid’s public GitHub pages already list a software-development kit for building agents that work across multiple messaging channels, plus a desktop agent that can run code in an isolated sandbox and work with GitHub, Gmail and Slack, so the newly announced GitHub-project tool shares a name and product family with earlier Classgrid agent projects \(tool-1-1, tool-1-2\).

**「What it would mean in practice」** If it works as described, a programmer could swap between several AI models inside one project instead of paying for separate apps for each. For now, anyone tempted to try it has nothing to check compatibility against: the post gives no instructions for installing or running the tool, no statement of which models are free or paid, and no indication of what data the tool sends where. The GitHub repository address is the only concrete starting point.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Classgrid/ai-sdk">GitHub - Classgrid/ai-sdk</a></li>
<li><a href="https://github.com/Classgrid/classgrid_platform_desktop">GitHub - Classgrid/classgrid_platform_desktop: Classgrid AI ...</a></li>

</ul>
</details>

**Tags**: `#open-source AI`, `#multi-model agents`, `#coding agents`, `#GitHub projects`, `#AI tooling`

---

<a id="item-tech-news-22"></a>
### [OpenMinion Alpha Runtime and CleverCloud&\#x27;s Three-Action AI Connector](https://github.com/CleverCloud/clever-client.js) ⭐️ 5.0/10

OpenMinion, described as a local-first AI runtime—software that runs AI programs mainly on the user&\#x27;s own computer—is in alpha testing. It supports Python 3.11 or newer \(a programming language\), command-line, Python and web-request interfaces, background-service execution, status checks and sessions that keep their state; the post says it has not been certified for long unattended operation and gives no installation steps or model details. Separately, cloud hosting company CleverCloud has published an MCP server \(MCP is a connector format that lets an AI assistant call outside tools and data\) with three tools—search, execute and doc—for its own API. The server is built with TypeScript \(a programming language\), needs Node.js 26 or newer \(software that runs JavaScript programs\), and is set up through a .mcp.json file with timeout and maximum-output settings.

telegram · aipluscn · Oct 29, 14:24

**「Background: what a runtime and an MCP server are」** OpenMinion is a Python-based &quot;runtime&quot; — the layer of software that actually runs an AI agent and hands it abilities such as running commands or calling outside services — designed to work on the user&\#x27;s own machine rather than inside a vendor&\#x27;s cloud; its project listings describe command-line, code-level and network interfaces, plus memory and MCP support \(tool-2-1, tool-2-2\). MCP \(Model Context Protocol\) is a shared connector format: instead of writing custom glue for each service, an AI agent can talk to any service that publishes an &quot;MCP server,&quot; which in Clever Cloud&\#x27;s case means three callable actions — search, execute and doc — wrapped around that company&\#x27;s own platform interface.

**「What It Means in Practice」** For someone already using CleverCloud, the practical effect is that an AI assistant supporting MCP can be given three actions on their Clever Cloud account—search, execute and doc—subject to a configured time limit and maximum amount of returned text. The compatibility catch is Node.js 26 or newer. The three tools are tied to Clever Cloud&\#x27;s API, so this server does not by itself connect an assistant to another cloud provider.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/openminion/openminion">GitHub - openminion / openminion : Local - first Python runtime for...</a></li>
<li><a href="https://pypi.org/project/openminion/">openminion · PyPI</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#AI agent tooling`, `#local-first runtime`, `#developer tools`, `#GitHub projects`

---

<a id="item-tech-news-23"></a>
### [Open-source Jira-to-pull-request AI workflow uses Claude Code or Copilot](https://github.com/pruthvidarji1993/ai-automation-jira) ⭐️ 5.0/10

A developer has published an open-source Python project called ai-automation-jira that it says runs a nine-stage AI workflow starting from a Jira ticket \(the task-tracking software many teams use to log bugs and feature requests\) and ending at a reviewed pull request \(a proposed code change submitted for approval\). The project can drive either Claude Code or GitHub Copilot, two AI coding assistants, and builds in two human checkpoints: one on the written plan and one on the code differences. It supports Anthropic&\#x27;s Opus and Sonnet models and is released under the MIT license, which lets anyone reuse and modify it freely. Its traction is minimal so far, with 1 star, 0 forks and 2 open issues on GitHub, and the listing contains no demonstration that the full nine-stage flow works end to end.

telegram · aipluscn · Oct 30, 05:07

**「Background」** Jira is a widely used issue tracker where teams record work as individual &quot;tickets,&quot; and a pull request \(PR\) is a proposed code change that teammates review before it is merged into the shared codebase. AI coding assistants such as Anthropic&\#x27;s Claude Code and GitHub Copilot can carry out coding tasks from written instructions, but they are normally driven one step at a time. Moving a ticket all the way to a finished, reviewed PR has generally been a manual, multi-stage process, and this project packages those steps into one scripted flow.

**「What it means in practice」** In principle, a team that tracks work in Jira could hand a ticket to this tool and get back a reviewed code change with two approval stops along the way. On the available evidence it is better read as a template than adopted as a working product: with two open issues and no recorded successful run, anyone testing it should point it at a scratch code repository rather than live project work, and expect to repair the connections between stages themselves.

**Tags**: `#Jira`, `#Claude Code`, `#GitHub Copilot`, `#coding agents`, `#workflow automation`

---

<a id="item-tech-news-24"></a>
### [Linux.do post floats ChatGPT Plus quota merge, promotes Web2Term](https://linux.do/u/kangnasi) ⭐️ 5.0/10

A post on the Linux.do forum, reposted to Telegram on 30 October 2026, says that ChatGPT Plus subscribers&\#x27; separate allowances for the ChatGPT website and for Codex — OpenAI&\#x27;s coding agent, a tool that writes and runs code on the user&\#x27;s behalf — may be merged into one shared quota alongside a product the author calls &quot;Work&quot;. The author gives no screenshot, changelog or other evidence and frames it only as something they &quot;heard&quot; \(听说\), so the change is unconfirmed. The same post introduces Web2Term, an open-source desktop program built with Electron \(a toolkit for turning web pages into desktop apps\) that lets a person log in to ChatGPT, Claude, DeepSeek or Gemini through the normal web interface and use that chat subscription for terminal-style, agent-like work instead of paying per-use API fees \(API: the paid programmatic access route billed by amount of text processed\). The author recommends only ChatGPT and Claude for now and defers all setup detail to the GitHub repository, giving no install steps, version number or demonstration that it works; they also suggest turning on TUN mode, a setting that routes all of a computer&\#x27;s internet traffic through a VPN-style tunnel.

telegram · linuxdo\_tg · Oct 30, 05:13

**「Background」** ChatGPT Plus is a flat monthly subscription whose use is capped by quotas — allowances that refill over time — instead of being billed per question. OpenAI&\#x27;s Codex, a coding assistant that can write and run commands on a computer, has been counted against a separate allowance from the ordinary web chat window, which the poster says is the main reason the base plan felt generous. The project being pitched, Web2Term, is a free desktop program \(built with Electron, a common way of packaging a web-style interface as an installable app\) that places a normal logged-in chat session beside a terminal, so the model proposes commands and the app runs them on the chosen machine and sends the real output back into the conversation; its GitHub page lists Windows, macOS and Linux builds and says ChatGPT and DeepSeek work best for now, with a Windows-only option to let the model click and type on the desktop.

**「What it means in practice」** If the two allowances really do become one, a Plus subscriber who leans on Codex for coding would be spending from the same monthly budget as ordinary chatting, so heavy coding could leave less room for conversation — but with no confirmation from OpenAI, there is nothing to act on yet. For Web2Term, the post itself is only a pointer: anyone interested has to check the repository for instructions, and the advice to enable a full-traffic tunnel suggests access may depend on network configuration that ordinary users would need help with.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/naledao/Web2Term/tree/main">GitHub - naledao/Web2Term: Web2Term是一个桌面工作区：把网页端的对...</a></li>
<li><a href="https://github.com/naledao/gpt-web-to-codex-terminal">GPT Web to Codex Terminal - GitHub</a></li>
<li><a href="https://web2term.kangnasi.xyz/">Web2Term — 让对话抵达终端</a></li>

</ul>
</details>

**Tags**: `#chatgpt-plus`, `#quota-limits`, `#subscription-access`, `#open-source-projects`, `#web-to-terminal-harness`

---

<a id="item-tech-news-25"></a>
### [Kimi Connects to Gmail, Google Drive and Google Calendar](http://kimi.ai/plugins) ⭐️ 5.0/10

Kimi, the chatbot from Moonshot AI, now lets users connect it to Gmail, Google Drive and Google Calendar, the company said. Through OAuth \(the Google sign-in screen that asks whether an app may access an account\), users can have Kimi summarize email conversations, search for files in Drive and plan schedules in Calendar. Access is controlled by the permissions each user approves, and the features can be tried at kimi.ai/plugins. The notice did not say which Kimi plans include the connectors or what usage limits apply.

telegram · zaihuapd · Oct 29, 13:19

**「Context」** Kimi is the chatbot made by the AI company Moonshot AI. Normally, a chatbot can only work with text you type or files you upload; a connector lets it fetch information from another service on your behalf. OAuth is the Google sign-in step where you approve specific permissions — such as reading your mail — without giving the assistant your Google password.

**「What it means in practice」** For Kimi users with a Google account, this means the assistant can answer questions using email conversations, Drive files and calendar entries without the user copying that material into the chat. Using it requires approving Google&\#x27;s access request, so users should read the permission screen before connecting; the notice does not list the specific permissions requested.

**Tags**: `#Kimi`, `#Moonshot AI`, `#Google Workspace`, `#OAuth integrations`, `#product update`

---

## Financial News

<a id="item-finance-news-1"></a>
### [FCC Bans Chinese Labs From Certifying U.S.-Bound Electronics](https://www.reuters.com/business/media-telecom/fcc-votes-ban-all-chinese-labs-testing-us-electronics-2026-10-29/) ⭐️ 7.0/10

The U.S. Federal Communications Commission voted on Oct. 29 to bar all Chinese laboratories from certifying smartphones, cameras, computers and other electronics for the U.S. market, with the rule taking effect in December 2028; FCC Chair Brendan Carr said 82% of electronics were tested in China in 2025, versus about 4% in the U.S.

telegram · zaihuapd · Oct 30, 03:15

**「Background」** In May 2025 the FCC adopted rules blocking laboratories owned or controlled by the Chinese government from certifying wireless equipment for the US market; the new vote extends that restriction from government-linked labs to all Chinese laboratories.

**「Who is affected」** Electronics makers that ship to the US will have to shift certification testing to labs in the US or in countries that offer reciprocal treatment to US labs, because from December 2028 the FCC will authorize only labs meeting that condition.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.fcc.gov/public/attachments/DOC-411576A1.pdf">FCC Bans ‘Bad Labs’ from U.S. Equipment Authorization Process</a></li>
<li><a href="https://www.theverge.com/policy/1009258/the-fcc-plans-to-ban-all-chinese-labs-from-testing-us-gadgets-by-2029">The FCC plans to ban all Chinese labs from testing US... | The Verge</a></li>
<li><a href="https://www.globaltimes.cn/page/202610/1371820.shtml">US FCC plan to bar Chinese testing labs could disrupt... - Global Times</a></li>

</ul>
</details>

**Tags**: `#FCC regulation`, `#US-China tech decoupling`, `#electronics supply chain`, `#product certification`, `#telecom policy`

---