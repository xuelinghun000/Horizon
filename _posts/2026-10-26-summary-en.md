---
layout: default
title: "Horizon Summary: 2026-10-26 (EN)"
date: 2026-10-26
lang: en
---

> From 90 items, 14 important content pieces were selected

---

**Technology News**
1. [One-sentence prompt tells AI coding agents to trust code over stale docs](#item-tech-news-1) ⭐️ 7.0/10
2. [Claude&\#x27;s payment page adds mainland China, Hong Kong, Macau and Taiwan options](#item-tech-news-2) ⭐️ 7.0/10
3. [Testing a local 8B coding agent on a 12GB graphics card](#item-tech-news-3) ⭐️ 6.0/10
4. [Guide explains how Russian companies can pay for Claude and GPT by invoice](#item-tech-news-4) ⭐️ 6.0/10
5. [Android client for a PC-run DeepSeek agent, with no cloud or Google push](#item-tech-news-5) ⭐️ 6.0/10
6. [new-api v1.0.0-rc.47 adds 12-hour cache pricing and shared channel routing](#item-tech-news-6) ⭐️ 5.0/10
7. [Analysis: Why OpenAI and Anthropic Cut AI Model Access Prices Up to 80%](#item-tech-news-7) ⭐️ 5.0/10
8. [Open-source Deki Engine offers visual game editor for ESP32 boards](#item-tech-news-8) ⭐️ 5.0/10
9. [Open-Source Meshtastic Collar Aims to Track Pets Without a Subscription](#item-tech-news-9) ⭐️ 5.0/10
10. [Kalman filter shows no edge over simpler rules for accepting AI code edits](#item-tech-news-10) ⭐️ 5.0/10
11. [A User Warns Against Chinese AI Reseller 基元律动 After a 200-Yuan Top-Up](#item-tech-news-11) ⭐️ 5.0/10
12. [MailFlare: a self-hosted catch-all inbox that pulls out one-time codes](#item-tech-news-12) ⭐️ 5.0/10
13. [Claude Opus 5.5 reportedly stops some software reverse-engineering answers](#item-tech-news-13) ⭐️ 5.0/10

**Financial News**
1. [China&\#x27;s 2025 Population Falls by 3.39 Million to 1.40489 Billion](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [One-sentence prompt tells AI coding agents to trust code over stale docs](https://linux.do/u/czm) ⭐️ 7.0/10

A post on the linux.do forum is circulating a one-sentence instruction that people can paste into CLAUDE.md or AGENTS.md — the plain-text files of standing instructions that AI coding tools such as Claude Code read at the start of a session — telling the agent that when a project&\#x27;s documentation and its existing code disagree, it should follow the conventions in the code and list every inconsistency in its final reply. The post, by user czm, gives the sentence in both English and Chinese and credits an arXiv paper \(a research preprint that has not necessarily been peer reviewed\) at arxiv.org/pdf/2610.30571. The author says the line &quot;greatly improves&quot; how often agents obey code over conflicting instructions, but the post itself gives no test numbers, sample sizes or measurements, so the size of any improvement is unverified here.

telegram · linuxdo\_tg · Oct 26, 02:11

**「Why a stale instruction file causes trouble」** Coding agents — programs such as Claude Code or Codex CLI that read, write and edit code on a user&\#x27;s behalf — load a project instruction file named CLAUDE.md or AGENTS.md at the start of a session and treat it as standing orders. When that file describes an older version of the project, the agent can follow the outdated text instead of what the code in the folder actually does. The post points to an arXiv paper \(2610.30571\) that proposes adding one sentence to that file so the code wins and the mismatch gets reported.

**「What it means in practice」** Anyone using these tools can add the sentence to a project&\#x27;s instruction file today; no software update or version requirement is involved, because the file is just text the agent reads. The trade-off is that it deliberately tilts the agent toward existing code, so in a project where the documentation is the intended specification and the code is what is wrong, the agent will now preserve the existing behavior and report the mismatch instead of changing the code to match the docs. It also appends a list of documentation-versus-code conflicts to each reply, which helps surface stale instructions but adds material to read.

**Tags**: `#coding-agents`, `#prompt-engineering`, `#AGENTS.md`, `#Claude Code`, `#arXiv`

---

<a id="item-tech-news-2"></a>
### [Claude&\#x27;s payment page adds mainland China, Hong Kong, Macau and Taiwan options](https://claude.ai/upgrade/pro?interval=monthly) ⭐️ 7.0/10

A Telegram channel reported that Claude&\#x27;s subscription upgrade page now lists mainland China, Hong Kong, Macau and Taiwan as billing regions, and that its editor was able to attach a UnionPay card \(China&\#x27;s main domestic card network, similar in role to Visa or Mastercard\) to pay. The report is a single, unconfirmed observation rather than an Anthropic announcement, and it does not mean the chatbot is now officially available in those places: Anthropic&\#x27;s help center still says users must be located in a supported region to use Claude. So the change, if it holds, is a new way to pay for Claude Pro, not a lifting of the regional service restriction. The post gives no details on which card types work, whether payment succeeds end to end, or whether the option appears for every user.

telegram · zaihuapd · Oct 26, 01:03

**「Why a payment option is not the same as access」** Claude Pro is Anthropic&\#x27;s paid subscription for its chatbot, and the upgrade page is where an existing account enters card details. Anthropic has previously widened the Chinese-language interface for users in markets it already serves while still blocking mainland China, as the South China Morning Post reported on October 8, 2026, so a new payment choice does not by itself change who is allowed to use the service.

**「What changes for people trying to pay」** If you are in mainland China, Hong Kong, Macau or Taiwan, the practical change is that a UnionPay card — the network most Chinese bank cards run on, and the largest card network in the world by cards in circulation — may now be accepted on the Claude Pro upgrade page, so paying no longer necessarily requires a foreign-issued card. But a successful payment does not change Anthropic&\#x27;s regional rules: check the supported-country list in its help centre before subscribing, because a charge can go through while the account still sits outside the regions where Claude is offered, leaving you paying for something you cannot use.

<details><summary>References</summary>
<ul>
<li><a href="https://www.scmp.com/tech/big-tech/article/3370154/us-ai-firm-anthropic-enables-chinese-language-options-claude-chatbot">Anthropic’s Claude AI gets Chinese-language options settings</a></li>
<li><a href="https://www.adyen.com/zh_CN/payment-methods/unionpay">UnionPay 支 付 方式- UnionPay 支 付 - Adyen</a></li>

</ul>
</details>

**Tags**: `#claude`, `#subscriptions`, `#payments`, `#regional-availability`, `#access-routes`

---

<a id="item-tech-news-3"></a>
### [Testing a local 8B coding agent on a 12GB graphics card](https://habr.com/ru/articles/1099230/?utm_campaign=1099230&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A Habr post describes an experiment to see whether a small, locally run AI model can power a terminal coding agent — a program that works on code from the command line — without sending anything to an outside service. The author chose Opencode, an open-source agent that is not tied to one model, and set the target at an 8-billion-parameter model with a 32K context window \(roughly the amount of text the model can consider at once\) running on a 12GB graphics card. The stated period is late April to late October 2026. The visible excerpt gives only the premise: it contains no results, configuration details, benchmarks, or installation steps, so it does not yet show whether the approach works or what tasks it can handle.

rss · Habr AI · Oct 25, 19:30

**「What the experiment rests on」** A terminal coding agent is a program that runs in a plain text command window and writes or edits code on your behalf. Opencode, the tool this experiment is built on, is an open-source one that can be pointed at any model instead of being tied to a single vendor&\#x27;s service; its own documentation describes it as a terminal-based agent that works with any AI model. The &quot;8B&quot; in the post means a model with 8 billion internal settings, small enough to fit on a single consumer graphics card with 12GB of memory, and &quot;32K context&quot; means it can keep roughly 32,000 tokens \(word fragments\) of conversation in view at once, which caps how much of a codebase it can consider at a time. The author frames the piece as an experiment running from late April to late October 2026, asking whether such a local setup can match models with 100 billion to 1 trillion settings.

**「What it could mean in practice」** If the experiment succeeds, a developer with a 12GB consumer graphics card could use a coding assistant without a paid subscription or sending source code to an outside company. The excerpt does not establish that this works, so it should not be treated as a setup guide or as evidence that a small local model matches larger hosted ones.

<details><summary>References</summary>
<ul>
<li><a href="https://opencode.ai/">OpenCode | The open source AI coding agent</a></li>
<li><a href="https://www.producthunt.com/products/opencode">opencode: Your terminal&#x27;s AI agent, with any model you want ...</a></li>

</ul>
</details>

**Tags**: `#terminal agents`, `#Opencode`, `#local LLMs`, `#self-hosting`, `#coding agents`

---

<a id="item-tech-news-4"></a>
### [Guide explains how Russian companies can pay for Claude and GPT by invoice](https://habr.com/ru/articles/1099218/?utm_campaign=1099218&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A Russian-language guide published on Habr on 25 October 2026 walks a company in Russia through paying for Anthropic&\#x27;s Claude and OpenAI&\#x27;s GPT by invoice, rather than through an employee&\#x27;s personal subscription charged to someone else&\#x27;s card, and through working out what a token \(the unit these services bill by, roughly a fragment of a word\) really costs. It covers an Anthropic rule about 50% ownership, the value-added tax \(VAT\) that a Russian buyer must withhold and pass on as a &quot;tax agent&quot; when purchasing from a foreign seller, and the dollar exchange rate folded into an intermediary&\#x27;s price. The excerpt available here contains no prices, rates or worked examples, so the specific figures the guide promises cannot be checked from it.

rss · Habr AI · Oct 25, 18:30

**「Background」** Claude and GPT are the paid AI assistants made by Anthropic and OpenAI, and both charge for use by the token — the small chunks of text a model reads and writes. The guide starts from the situation Russian companies run into: paying for these tools usually happens either through an employee&\#x27;s personal subscription, sometimes charged to someone else&\#x27;s card, or through an intermediary that issues an invoice and the closing documents a Russian accounting department needs to book the expense. It also walks through a rule that applies when a Russian company buys services from a foreign supplier: the company must act as a &quot;tax agent,&quot; calculating and paying the value-added tax itself rather than being billed it by the seller.

**「What it means in practice」** For a company budgeting for these models, the guide&\#x27;s practical point is that the published dollar price per token is not the price the company ends up paying: withheld VAT on a foreign purchase and an intermediary&\#x27;s exchange-rate markup sit on top, so a budget built from list prices will come out low. It also treats an employee&\#x27;s personal subscription paid on someone else&\#x27;s card as unsuitable for corporate accounting, which leaves the invoice route and its paperwork as the alternative to plan for.

**Tags**: `#Claude`, `#GPT`, `#pricing`, `#Russia`, `#access routes`

---

<a id="item-tech-news-5"></a>
### [Android client for a PC-run DeepSeek agent, with no cloud or Google push](https://habr.com/ru/articles/1099110/?utm_campaign=1099110&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A developer published a Habr post describing an Android app that controls a DeepSeek Harness agent running on a home computer, without a cloud server and without FCM \(Firebase Cloud Messaging, Google&\#x27;s service that apps normally use to receive messages while closed\). The app pairs with the computer by scanning a QR code and uses certificate pinning, meaning it trusts only that one specific machine&\#x27;s identity and refuses impostors. Instead of an embedded browser view \(WebView\), the author wrote a plugin that runs inside the DeepSeek Harness process itself, and added a receipt journal so the phone never resends a command blindly. The post is a write-up: the supplied excerpt contains no source code, installation steps, or evidence of a published, working build.

rss · Habr AI · Oct 25, 13:48

**「What DeepSeek Harness is」** DeepSeek Harness \(dsh\) is DeepSeek&\#x27;s own open-source &quot;agent harness&quot;: a program that runs an AI agent on your own computer, with a local web interface and every capability added as a plugin \(tool-2-1, tool-2-2\). It is in public preview worldwide under the MIT licence, which lets anyone reuse and modify the code \(tool-2-3\). Reaching an agent like that from a phone normally means either a cloud server sitting in the middle or FCM, Google&\#x27;s push-notification service that wakes an app when it is closed — the two things this project sets out to avoid.

**「What it means in practice」** For someone who leaves a coding agent working on their own machine, this describes a way to check on or steer it from a phone without sending commands through someone else&\#x27;s server. The excerpt does not say how the phone reaches the computer — whether both must be on the same Wi-Fi network or something else is required — so that is the first thing to confirm before trying it. It is also Android-only, and without code or setup instructions in the excerpt, readers cannot yet reproduce it from this text alone.

<details><summary>References</summary>
<ul>
<li><a href="https://deepseekagent.io/guides/deepseek-harness">DeepSeek Harness (dsh): Official DeepSeek Agent Setup Guide</a></li>
<li><a href="https://github.com/deepseek-ai/deepseek-harness">DeepSeek Harness - GitHub</a></li>
<li><a href="https://www.deepseek.com/en/harness/">DeepSeek Harness | Explore the limits of intelligence</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#coding agents`, `#Android client`, `#remote access`, `#developer tooling`

---

<a id="item-tech-news-6"></a>
### [new-api v1.0.0-rc.47 adds 12-hour cache pricing and shared channel routing](https://github.com/QuantumNous/new-api/releases/tag/v1.0.0-rc.47) ⭐️ 5.0/10

new-api, a self-hosted API relay \(software that forwards app requests to AI providers and tracks usage and billing\), has published release candidate v1.0.0-rc.47, a pre-release test version. On image, video and OpenAI Responses requests \(an OpenAI interface for model replies\), a model available through both a regular channel \(a normal route to a provider or account\) and a task plugin \(an add-on that handles jobs such as generation\) is now chosen by priority and weight \(how traffic is split\) instead of always going to the plugin. Operators must set a separate regular-channel price, or the request returns a price error and is not charged. The release also bills OpenAI&\#x27;s 12-hour prompt cache \(a provider-stored copy of part of a request, reused to avoid resending it\) at 2.5 times the input price, and moves the automatic refund wait for video tasks from 24 to 72 hours unless the operator has set TASK\_TIMEOUT\_MINUTES.

github · Calcium-Ion · Oct 25, 09:04

**「What this software is」** new-api is a self-hosted gateway: software an operator runs on their own server so apps can reach several AI companies through one address, while the gateway decides which route serves each request and records what it costs. In this project a “channel” is one configured route to a provider, and a “task plugin” is an add-on for longer jobs such as image or video generation. Version 1.0.0-rc.47 is a pre-release test build for the upcoming 1.0.0, not the final release.

**「Impact」** Operators upgrading should check the price list for any model that exists in both a regular channel and a task plugin before routing traffic to it: the release does not fall back to the plugin&\#x27;s price, so a missing regular-channel price produces a price error and no charge. They should also confirm whether their task-timeout setting is intentional, because the new 72-hour refund delay applies only when TASK\_TIMEOUT\_MINUTES is unset.

**Tags**: `#api-relay`, `#new-api`, `#pricing`, `#openai`, `#self-hosted`

---

<a id="item-tech-news-7"></a>
### [Analysis: Why OpenAI and Anthropic Cut AI Model Access Prices Up to 80%](https://minimaxir.com/2026/10/cheap-llms/) ⭐️ 5.0/10

OpenAI and Anthropic have cut the prices they charge for API access—the pay-per-use connection that lets other software call their models—by as much as 80% over a few months, according to an analysis piece discussed on the technology site Hacker News. The piece is a retrospective explanation, not an announcement of a new price change, and it does not provide a current price list. The people most directly affected are developers and businesses that pay these companies per use to power chatbots, writing tools, and other products.

hackernews · minimaxir · Oct 25, 21:11 · [Discussion](https://news.ycombinator.com/item?id=50236102)

**「How the price cuts unfolded」** OpenAI and Anthropic do not sell their models outright; they rent access through an API \(application programming interface — a paid connection that lets other software send text to a model and get an answer back\), billed per token \(the small chunks of text a model reads and writes\). The cuts were not one announcement: reporting from mid-August 2026 described OpenAI lowering prices on two of its models within a single week, Anthropic quietly cancelling a planned price increase, and Chinese lab DeepSeek — which built its reputation on cheap access — raising its own API prices by as much as 1,100%. That mix of cuts and a reversal is the backdrop for the current argument over how much room the Western labs still have to go lower.

**「Impact」** For a team building on these APIs, the same amount of text can now cost less—by as much as 80%—which can make a chat product or automated writing tool cheaper to operate. Because the piece is an explanation rather than a price list, teams should still check the providers&\#x27; current rates before changing a budget.

**「Community discussion」** Several commenters point to competition from cheaper Chinese models such as Kimi and GLM; one says their team switched after hitting “cybersecurity” refusals at OpenAI and Anthropic and found the alternatives cheaper. Others argue the cuts are partly a regulatory strategy to sideline Chinese open models \(models published for others to download and run\), or cite DeepSeek&\#x27;s claimed $38 revenue per graphics chip per hour for its Flash V4 model to suggest the large providers still have room to cut; a separate comment asks whether low prices are effectively subsidized by customer data.

<details><summary>References</summary>
<ul>
<li><a href="https://www.thetechwatcher.com/2026/08/ai-price-war-openai-anthropic-deepseek-zai-2026.html">AI Price War 2026: OpenAI, Anthropic, DeepSeek and Z.ai Are ...</a></li>
<li><a href="https://mlq.ai/news/openai-anthropic-cut-ai-prices-as-chinese-models-widen-the-cost-gap/">OpenAI, Anthropic cut AI prices as Chinese models widen the ...</a></li>

</ul>
</details>

**Tags**: `#llm-pricing`, `#openai`, `#anthropic`, `#api-costs`, `#industry-analysis`

---

<a id="item-tech-news-8"></a>
### [Open-source Deki Engine offers visual game editor for ESP32 boards](https://www.cnx-software.com/2026/10/25/deki-engine-esp32-gets-an-open-source-unity-style-editor-and-c-2d-game-engine/) ⭐️ 5.0/10

Deki Engine, a new open-source 2D game engine written in C++ \(a widely used programming language\), provides a visual editor for building games and installing them on ESP32 boards—small, low-cost chips used in hobby electronics. The editor runs on Windows and Linux, is published under the Apache 2.0 open-source license on GitHub, and lets users place images, text, particles, grid-based maps and animation effects in a scene instead of writing all the layout code by hand. It is optimized for the LilyGO T-Deck Plus and T-Display S3 AMOLED, with support for the Elecrow CrowPanel Advanced 7-inch ESP32-P4 promised soon; projects can also run on a desktop PC through SDL3 \(a standard library for drawing graphics in a window\). The project claims 60 frames per second on an ESP32-S3 chip, but that figure comes from the project rather than an independent test, and the supplied article is truncated, so capabilities beyond its feature list are unverified.

rss · CNX Software · Oct 25, 03:00

**「Background」** ESP32 is a family of low-cost microcontroller chips — small computers on a single chip — used in hobby electronics and small devices. Unity is a popular game-making tool whose editor lets people assemble scenes by dragging objects instead of writing every layout by hand; Deki borrows that approach for 2D games on ESP32 hardware. It also runs on an ordinary Windows or Linux PC through SDL3, a free graphics-and-input library, so developers can test a game before loading it onto a board.

**「What it changes for makers」** For hobbyists and small teams, the practical change is that a game prototype can be assembled in a desktop editor and installed on a supported board from the same Build panel, instead of setting up a separate programming environment for the tiny device. Compatibility depends on hardware packages: the T-Deck Plus package is listed as covering its screen, touch, keyboard, trackball, SD card, GPS and LoRa \(long-range\) radio, so owners of other boards should check for a matching package before assuming the editor can install to it.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnx-software.com/2026/10/25/deki-engine-esp32-gets-an-open-source-unity-style-editor-and-c-2d-game-engine/">Deki Engine - ESP 32 gets an open source Unity - style editor and C++...</a></li>

</ul>
</details>

**Tags**: `#ESP32`, `#game engine`, `#open source`, `#embedded development`, `#microcontroller`

---

<a id="item-tech-news-9"></a>
### [Open-Source Meshtastic Collar Aims to Track Pets Without a Subscription](https://hackaday.com/2026/10/25/meshtastic-pet-tracking/) ⭐️ 5.0/10

A maker named Jon G Aguado has designed LIA, an open-source pet collar tracker built on Meshtastic, according to a Hackaday write-up. Meshtastic is a free, open-source system in which small low-power radios form their own local network and pass messages between each other; LoRa is the long-range, low-power radio technique those radios use. LIA uses a custom circuit board \(PCB, the board that carries and connects the electronics\) and is positioned as an alternative to commercial pet trackers, which the article says need a subscription or a network connection to work. The published excerpt stops before any parts list, firmware download, or assembly instructions, so there is no confirmed buildable package yet.

rss · Hackaday · Oct 25, 11:00

**「The radio network behind the collar」** Meshtastic is a free, open-source system in which small radios pass messages to one another directly over LoRa, a low-power radio signal that can carry short data for kilometers without cell towers or a paid network. Commercial pet trackers usually depend on cellular service and a monthly subscription; LIA pairs a GPS receiver with a LoRa radio so the collar reports its position through that do-it-yourself network instead. The project was entered in the 2026 Meshtastic Build-Off competition, and its design files and code are published openly.

**「What it means in practice」** Anyone interested would have to build this themselves: it is a do-it-yourself design with a custom circuit board, not a product on a shelf, and the material available so far gives no parts list, software download, or step-by-step guide. The trade-off is that it replaces a monthly fee with radio range — the collar communicates over LoRa rather than a paid cellular plan, so usefulness depends on radio coverage, and the source provides no range or battery-life figures.

<details><summary>References</summary>
<ul>
<li><a href="https://jgaguado.github.io/LIA/">LIA — Off-grid. On track.</a></li>
<li><a href="https://github.com/JGAguado/LIA">GitHub - JGAguado/LIA: Low-power pet tracking platform built ...</a></li>
<li><a href="https://www.seeedstudio.com/blog/2026/08/19/lia-an-open-meshtastic-gps-tracker-built-for-off-grid-use/">LIA Meshtastic GPS Tracker: Open Off-Grid Design - Seeed Studio</a></li>

</ul>
</details>

**Tags**: `#meshtastic`, `#lora`, `#open-source-hardware`, `#esp32`, `#pet-tracker`

---

<a id="item-tech-news-10"></a>
### [Kalman filter shows no edge over simpler rules for accepting AI code edits](https://habr.com/ru/articles/1098756/?utm_campaign=1098756&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr author tested whether a Kalman filter — a mathematical method for combining a prediction with noisy measurements — is a better rule for deciding which AI-suggested code edits to keep in an &quot;author–critic&quot; loop, where one AI model writes edits and another reviews them. In a pilot of 720 model responses \(144 used for calibration and 576 for evaluation across six Python code-optimization tasks\), all four edit-acceptance rules met the success criterion, and the Kalman filter showed no measurable advantage over the simpler rules. In simulation the filter did improve the estimate of the underlying state and reduced the size of edits. The author published the notebook, source code, results, charts, a description of limitations, and a ready-made package for running your own author–critic experiment through the OpenAI API \(a paid interface for sending prompts to OpenAI&\#x27;s models\), including instructions, calibration, and pause/resume support.

rss · Habr AI · Oct 25, 08:56

**「Key concepts」** A Kalman filter is a standard method for combining a prediction with an imperfect measurement—originally developed for tracking moving objects—to produce a better estimate than either source alone. In this experiment, the prediction comes from the AI author and the measurement is the critic AI&\#x27;s feedback on a code edit; the question is whether combining them is a better way to decide which edits to accept than simpler rules. An author–critic loop means one AI model proposes code changes and another reviews them, a common setup in AI coding tools.

**「What it means in practice」** For anyone using AI coding assistants, the pilot suggests that a more elaborate scoring rule for accepting edits did not produce better outcomes than plain rules on these six tasks, so adding a Kalman filter is not an obvious upgrade. The released package lets others rerun the comparison on their own tasks, but the result comes from a single small pilot and does not establish how the method behaves on larger or different codebases.

**Tags**: `#AI coding agents`, `#author-critic loop`, `#Kalman filter`, `#reproducible experiment`, `#OpenAI API`

---

<a id="item-tech-news-11"></a>
### [A User Warns Against Chinese AI Reseller 基元律动 After a 200-Yuan Top-Up](https://linux.do/u/att1008) ⭐️ 5.0/10

A user on the Chinese forum linux.do has warned others against putting money into 基元律动, an API relay \(a middleman that resells access to AI models\), saying the service did not behave as advertised after a 200-yuan top-up. In the post dated 26 October 2026, the user says they paid in during a &quot;top up this much, get this much free&quot; promotion, then found that requests rarely reached DeepSeek&\#x27;s official service, that a &quot;reasoning level&quot; setting \(which controls how much internal thinking the model does before answering\) had no effect whatever was selected, and that prompt caching \(a feature that reuses text the model has already processed to cut cost and waiting time\) did not work on the service&\#x27;s Anthropic-compatible interface. The user says a few hours of use cost about 70 yuan, and that the site offers only a third-party feedback page and a support email, with no refund channel. This is one person&\#x27;s account with no configuration details or repeatable tests, so it is a caution rather than confirmed evidence about the service.

telegram · linuxdo\_tg · Oct 26, 02:07

**「What a relay service is」** Chinese AI models such as DeepSeek are normally reached through the developer&\#x27;s own paid interface \(an API — the channel software uses to send requests to a model\). Third-party &quot;relay&quot; services resell that access, often bundling several model providers behind one address and selling credit in top-up promotions; the poster bought 200 yuan of credit from one called 基元律动 during such a bonus offer. Prompt caching, the feature at the centre of the complaint, lets a provider store the repeated part of a request so later calls containing the same text are billed at a lower rate.

**「What to check before paying」** Anyone buying model access through a reseller should test with a small top-up first: confirm which provider is actually answering the requests, and check that cost-saving features such as prompt caching and reasoning settings take effect before committing a large balance. In this case the reported caching failure is what turned a few hours of use into a 70-yuan bill, and the user found no way to get the money back — so the amount at risk is the prepaid balance itself.

**Tags**: `#API relay`, `#DeepSeek`, `#prompt caching`, `#provider warning`, `#cost`

---

<a id="item-tech-news-12"></a>
### [MailFlare: a self-hosted catch-all inbox that pulls out one-time codes](https://linux.do/u/nayumi.DEV) ⭐️ 5.0/10

A developer posting as nayumi.DEV has open-sourced MailFlare, an inbox you run yourself that accepts mail sent to any address at a domain you own and tries to pull one-time verification codes out of the subject line or body so they can be copied with one click. It is built on Cloudflare Email Routing \(Cloudflare&\#x27;s service for directing mail sent to a domain you control\) with a FastAPI backend \(a Python web framework\), and it gives each mailbox its own permissions — owner, read-only shared, and an admin override — instead of one inbox everyone shares. The interface is deliberately Gmail-like for the list, reading and composing views, data can be stored in SQLite or Postgres \(two database systems\), and replies can be sent from a mailbox through Cloudflare&\#x27;s paid Workers service. The documentation is in Chinese, English and several other languages. All of this comes from the author&\#x27;s own promotional forum post; there are no benchmarks, independent tests, or evidence of adoption yet.

telegram · linuxdo\_tg · Oct 26, 02:10

**「Background」** A catch-all address is a single rule that accepts mail for every possible name at a domain — anything@yourdomain.com — so you never have to create a mailbox in advance. One-time codes \(OTP, short for one-time password\) are the digits sites email or text you to prove it is really you; gathering them in one place keeps them out of a personal inbox. &quot;Self-hosted&quot; means the software runs on a server you control rather than on a company&\#x27;s service.

**「What it takes to use」** Anyone who wants this needs to own a domain, route its mail through Cloudflare, and run a Python service themselves; sending replies from the inbox also requires a paid Cloudflare Workers plan, so the free path is receive-only. For people who sign up for many services and do not want codes landing in a personal mailbox, the per-mailbox permissions are the practical difference from a plain shared inbox.

**Tags**: `#self-hosted`, `#open-source`, `#email`, `#OTP`, `#Cloudflare`

---

<a id="item-tech-news-13"></a>
### [Claude Opus 5.5 reportedly stops some software reverse-engineering answers](https://linux.do/u/BunnHack) ⭐️ 5.0/10

A reposted IT之家 article reports that some Claude Opus 5.5 users say the model has stopped helping with reverse engineering — taking apart software to see how it works — after an October 21 update to several Claude products. They describe an automatic safety check cutting off answers partway through when asked to analyze copyrighted or otherwise protected material, and say rewording the request did not restore the analysis. Anthropic has not announced a new Opus 5.5 version or confirmed any change, and the evidence is a Reddit thread with mixed reports; some users said Claude&\#x27;s reverse-engineering help was already unreliable. The article says Anthropic has often adjusted model behavior without release notes, so a silent restriction is plausible but unproven.

telegram · linuxdo\_tg · Oct 26, 02:13

**「Background」** Claude Opus 5.5 is Anthropic&\#x27;s flagship chatbot model, released on September 22, 2026, as reported at the time by 9to5Mac. &quot;Reverse engineering&quot; here means asking the chatbot to take apart a finished program — a game, or the built-in software on a TV — and reconstruct how it works, which is how some users produced browser versions of games. Anthropic does not publish a changelog every time it adjusts how a model responds, so a change in behavior can only be inferred by users comparing what the model did before and after an update.

**「What it means」** For people who use Claude for code work, the practical effect is unpredictability: a request to inspect or modify protected software may now be cut off mid-answer, and there is no official release note to confirm what changed. If such work matters, test the specific request before depending on it and keep a manual or alternative-tool fallback.

<details><summary>References</summary>
<ul>
<li><a href="https://9to5mac.com/2026/09/22/anthropic-upgrades-claude-with-new-opus-5-5-model-details-here/">Anthropic upgrades Claude with new Opus 5 . 5 model... - 9to5Mac</a></li>

</ul>
</details>

**Tags**: `#Claude Opus 5.5`, `#Anthropic`, `#model capability change`, `#reverse engineering`, `#silent restriction`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s 2025 Population Falls by 3.39 Million to 1.40489 Billion](https://weibo.com/1796087453/5357878513767954) ⭐️ 7.0/10

According to China Statistical Yearbook 2026 data cited in a Weibo post, China&\#x27;s population at the end of 2025 was 1.40489 billion, down 3.39 million from the end of 2024, with 7.92 million births and a natural growth rate of -2.41‰, leaving the total near the 1.4 billion threshold.

telegram · zaihuapd · Oct 25, 12:02

**「Background」** The 2025 figures were published by China’s National Bureau of Statistics; the total fertility rate was about 0.96, well below the 2.1 replacement level, and people aged 60 and over made up 23% of the population.

<details><summary>References</summary>
<ul>
<li><a href="https://www.caixinglobal.com/2026-01-19/chinas-population-decline-accelerates-as-births-hit-modern-era-low-in-2025-102405520.html">China ’s Population Decline Accelerates as Births Hit... - Caixin Global</a></li>
<li><a href="https://www.globaltimes.cn/page/202610/1372925.shtml">Nine provincial-level regions in China post birth rates ... - Global Times</a></li>

</ul>
</details>

**Tags**: `#China demographics`, `#population decline`, `#birth rate`, `#macroeconomy`, `#statistical data`

---