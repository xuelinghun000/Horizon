---
layout: default
title: "Horizon Summary: 2026-10-31 (EN)"
date: 2026-10-31
lang: en
---

> From 115 items, 20 important content pieces were selected

---

**Technology News**
1. [Tampered Claude Code add-on on Cursor&\#x27;s marketplace tried to install a backdoor](#item-tech-news-1) ⭐️ 8.0/10
2. [Claude renames Max plans to Max and Ultra, drops 5-hour cap for verified Ultra](#item-tech-news-2) ⭐️ 8.0/10
3. [NES Emulator Runs Inside 1GB of Qwen Model Weights](#item-tech-news-3) ⭐️ 7.0/10
4. [Developer&\#x27;s Telegram client for OpenCode AI coding tool gets 1,298 GitHub stars](#item-tech-news-4) ⭐️ 7.0/10
5. [Unverified Report: Antigravity to Drop Claude 4.6 and GPT-OSS-120b on Nov 2](#item-tech-news-5) ⭐️ 7.0/10
6. [Hobbyist Gets Classic Mac OS Running on a Nintendo Wii](#item-tech-news-6) ⭐️ 6.0/10
7. [Habr Teaser Proposes Handing Off a Live Console AI Agent Session](#item-tech-news-7) ⭐️ 6.0/10
8. [Xiaomi releases Xiaomi-OCR-0, a small open document-reading model](#item-tech-news-8) ⭐️ 6.0/10
9. [Tencent releases Hy-Nomas video world model as open source](#item-tech-news-9) ⭐️ 6.0/10
10. [Habr teaser: 125-billion-parameter AI model on an RTX 5070, details missing](#item-tech-news-10) ⭐️ 5.0/10
11. [FLUX.3 klein used to make 290 dentist ad photos for about $3](#item-tech-news-11) ⭐️ 5.0/10
12. [HuggingFace for Beginners: Choosing and Running a Model](#item-tech-news-12) ⭐️ 5.0/10
13. [22-Billion-Parameter LTX-2.5 Video Model Reported Running on a 10 GB RTX 3080](#item-tech-news-13) ⭐️ 5.0/10
14. [Reports: Claude accounts suspended right after passport checks](#item-tech-news-14) ⭐️ 5.0/10
15. [DIY project turns an MSI GS75 laptop keyboard into a standalone USB keyboard](#item-tech-news-15) ⭐️ 5.0/10
16. [ai-automation-jira claims nine-stage Jira-to-reviewed-code AI workflow](#item-tech-news-16) ⭐️ 5.0/10
17. [Leak: DeepSeek website code hints at &\#x27;Cyber&\#x27; model limited to businesses](#item-tech-news-17) ⭐️ 5.0/10

**Financial News**
1. [DeepSeek Reportedly Raises RMB 105.5 Billion in Second Round](#item-finance-news-1) ⭐️ 7.0/10
2. [Four Japanese automakers&\#x27; China output falls below 40% of peak](#item-finance-news-2) ⭐️ 7.0/10
3. [法国国民议会通过数据流量税修正案](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Tampered Claude Code add-on on Cursor&\#x27;s marketplace tried to install a backdoor](https://phorion.io/blog/offical-claude-code-vsx-compromise/) ⭐️ 8.0/10

A tampered copy of Anthropic&\#x27;s Claude Code add-on for the VS Code code editor, labeled version 2.1.313, appeared on Cursor&\#x27;s add-on marketplace on Thursday, Oct. 29. Cursor says the copy was not built by Anthropic and that at most 5,000 users were affected; it tried to add an attacker&\#x27;s digital key to the SSH authorized-keys file \(the list of keys that can log in to a machine remotely without a password\). Because that step requires administrator rights, Cursor says most attempts to create a remote access route failed. Anthropic says its own distribution channels were not affected and the problem is limited to Cursor users; Cursor has removed the version, temporarily closed the marketplace, replaced its security keys and published steps to check for a key labeled svc-telemetry.

hackernews · \_chall · Oct 30, 07:09 · [Discussion](https://news.ycombinator.com/item?id=50300683)

**「Background」** Claude Code is Anthropic’s assistant for writing software, and its VS Code extension is an add-on that plugs it into VS Code \(Microsoft’s code editor\) and Cursor, a competing editor built on the same foundation. Cursor can draw add-ons from Open VSX, a separate public catalogue of VS Code extensions used by Cursor and some other editors, rather than Microsoft’s official VS Code Marketplace. A report from The Hacker News says the tampered package spread only through Cursor’s marketplace, with no evidence it reached Open VSX or Microsoft’s marketplace, while other accounts were unsure whether Open VSX itself was affected.

**「What this means in practice」** The practical risk is persistent access: if the attacker&\#x27;s key was added, uninstalling the add-on would not remove it, and the attacker could keep logging in without a password until the key is deleted. Cursor&\#x27;s detection step is to search the SSH authorized-keys file for &quot;svc-telemetry&quot;; anyone who installed the add-on through Cursor&\#x27;s marketplace between about 2:27 a.m. and 1:35 p.m. PT on Oct. 29 should run that check and, if the key is present, remove it and reinstall from Anthropic&\#x27;s official channel.

**「Community discussion」** An Anthropic employee, felixrieseberg, disputed the framing that Anthropic itself was compromised, saying a malicious actor used access to Cursor&\#x27;s marketplace to publish a copy Anthropic did not build or publish, and that official Anthropic channels were unaffected. Commenters also debated scope: one noted the bad build came through the Open VSX registry used by Cursor, while another cautioned that the write-ups do not make clear whether Microsoft&\#x27;s official VS Code marketplace was involved.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/official-claude-code-vs-code-extension.html">Official Claude Code Extension on Cursor Marketplace ...</a></li>
<li><a href="https://www.stepsecurity.io/blog/claude-code-extension-trojanized">Trojanized Claude Code Extension Delivered Persistent SSH ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#claude-code`, `#cursor`, `#supply-chain`, `#vs-code-extensions`

---

<a id="item-tech-news-2"></a>
### [Claude renames Max plans to Max and Ultra, drops 5-hour cap for verified Ultra](https://x.com/claudeai/status/2116220869479428500) ⭐️ 8.0/10

Anthropic renamed the two top tiers of its Claude chatbot subscriptions: the $100-a-month Max 5x plan is now just Max, and the $200-a-month Max 20x plan is now Ultra. Prices are unchanged, and existing subscribers do not have to do anything. From October 30, Ultra accounts that have passed an account-verification step are no longer bound by the 5-hour usage limit \(a cap on how much you can use the chatbot within any five-hour window\), with most current subscribers being covered first. New accounts keep a temporary limit until they verify, which the post says is meant to deter fraud and abuse, and users get an email when it is lifted; the weekly usage limits are unchanged.

telegram · zaihuapd · Oct 30, 17:44

**「Background」** Claude is Anthropic&\#x27;s paid chatbot service: subscribers pay a monthly fee for a set amount of usage rather than unlimited conversation. Its two most expensive plans had both carried the “Max” name, with 5x and 20x suffixes meant to show different usage allowances, and each imposed a cap on usage within every five-hour window in addition to a weekly ceiling.

**「What it means in practice」** For someone paying $200 a month for Ultra, the change removes enforced pauses during long working sessions, but not the overall ceiling — the weekly cap still decides how much you can use in total. Anyone signing up for Ultra now should expect the five-hour limit to apply until their account clears verification, so a heavy first week may still hit a wall before the email arrives.

**Tags**: `#Claude`, `#Anthropic`, `#subscription plans`, `#rate limits`, `#usage quotas`

---

<a id="item-tech-news-3"></a>
### [NES Emulator Runs Inside 1GB of Qwen Model Weights](https://github.com/dbreunig/nesformer) ⭐️ 7.0/10

A working emulator — software that behaves like a game console — for the Nintendo Entertainment System now exists inside roughly 1GB of an AI model&\#x27;s weights, the files that hold what a model has learned. The model is Qwen3.5-4B, a publicly downloadable model with 4 billion internal settings. The project, called nesformer, runs NES game files such as Super Mario Bros. at 150 to 290 times slower than the original console, according to its author, Drew Breunig, who published the code and weights on GitHub. It reproduces both the console&\#x27;s processor and its memory inside the model, an approach inspired by an earlier project called qwenputer. Breunig says Anthropic&\#x27;s Opus 5.5 generated the working code and weights from two prompts; that account has not been independently verified.

hackernews · dbreunig · Oct 30, 16:40 · [Discussion](https://news.ycombinator.com/item?id=50306442)

**「Prior context」** nesformer follows qwenputer, an earlier experiment by Divyansh Agrawal that used the same trick to run a small computer inside a language model&\#x27;s weights \(the billions of numbers a model learns during training and then uses to generate its answers\). The Nintendo Entertainment System is the 1980s console whose games ran on a 6502 processor with only a few kilobytes of working memory, so reproducing it inside a model means the model has to carry out the chip&\#x27;s step-by-step behavior rather than just describe it.

**「Community Discussion」** Commenters largely treated the project as a striking illustration of the efficiency gap between AI models and ordinary software: jacquesm called it &quot;horrifying&quot; on efficiency grounds, and pbohun noted that an equivalent conventional program would need far less compute. armcat took a more speculative view, suggesting that small virtual machines and tools could be built inside model weights and run using the model&\#x27;s own calculations.

**Tags**: `#open-weight models`, `#Qwen`, `#emulation`, `#GitHub projects`, `#LLM capability demos`

---

<a id="item-tech-news-4"></a>
### [Developer&\#x27;s Telegram client for OpenCode AI coding tool gets 1,298 GitHub stars](https://habr.com/ru/articles/1101612/?utm_campaign=1101612&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 7.0/10

A developer has described building opencode-telegram-bot, a Telegram client for the OpenCode AI coding agent \(software that can write and edit code on a user&\#x27;s behalf\), initially for personal use. The author says the project now has 1,298 stars on GitHub — the site&\#x27;s bookmark-style approval count — and 48 contributors, meaning people who have contributed code to it. The article excerpt is cut off before installation steps or feature details, so it is not possible to verify how complete or easy to use the tool is.

rss · Habr AI · Oct 30, 09:19

**「What the bot does」** OpenCode is a coding agent: software that can carry out coding tasks on a computer from typed instructions. It normally runs in a terminal through text commands, known as a CLI \(command-line interface\). The Telegram bot works as a remote control for an OpenCode session on the user&\#x27;s own machine, letting them start tasks, follow progress, switch models, and manage sessions from a phone chat.

**「What it could mean in practice」** For people who already use a coding agent, the appeal is being able to send instructions from a phone instead of sitting at a computer. The excerpt does not show setup requirements or compatibility, so anyone interested should not assume it will work with their own setup until the full instructions are available.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/grinev/opencode-telegram-bot">GitHub - grinev/ opencode - telegram - bot : OpenCode mobile client via...</a></li>

</ul>
</details>

**Tags**: `#opencode`, `#coding-agents`, `#telegram-bot`, `#open-source`, `#developer-tooling`

---

<a id="item-tech-news-5"></a>
### [Unverified Report: Antigravity to Drop Claude 4.6 and GPT-OSS-120b on Nov 2](https://linux.do/u/KennethCC) ⭐️ 7.0/10

An unverified post on the linux.do forum, dated 31 October 2026, says Antigravity — an AI coding tool that lets users pick among models from different companies — will remove Claude Sonnet 4.6, Claude Opus 4.6 \(two Anthropic models, one tuned for speed and one for harder tasks\) and GPT-OSS-120b \(an OpenAI model that anyone can download and run\) on 2 November. According to the post, free accounts and Google AI Plus subscribers would then have only Gemini 3.8 Flash, Google&\#x27;s fast, lower-cost model tier, to choose from. Paid Google AI Pro accounts \(excluding free trials\), plus Ultra and Enterprise plans, would keep Claude Sonnet 5.5 and Claude Opus 5.5, the newer generation of those Anthropic models. Neither Antigravity nor Google has confirmed the change, and the post offers no pricing detail or evidence beyond the claim itself, so the model names, tiers and date should be treated as a claim rather than settled fact.

telegram · linuxdo\_tg · Oct 31, 02:02

**「What Antigravity is and why tiers decide model access」** Antigravity is Google&\#x27;s AI coding tool, and instead of being tied to one model it lets users pick from a menu: Claude \(made by Anthropic\), Gemini \(Google&\#x27;s own\), and GPT-OSS-120b \(an openly downloadable model from OpenAI\). What a user can pick depends on the plan attached to their Google account — free, Google AI Plus, Google AI Pro, Google AI Ultra, or an enterprise plan — and a &quot;trial&quot; here means a short free sample of a paid plan rather than a full subscription. Antigravity&\#x27;s own model list has carried a footnote saying Claude Sonnet 4.6, Claude Opus 4.6 and GPT-OSS-120b would be removed on 2 November 2026, and some Google AI Pro subscribers have reported the newer 5.5 models never appearing in their model picker even though the models page lists them for non-trial Pro and Ultra accounts.

**「What to check before 2 November」** If the report is accurate, anyone on a free or AI Plus account who uses Claude or GPT-OSS inside Antigravity would lose those options and would need to either work with Gemini 3.8 Flash or move to a paid plan. Someone currently on a Google AI Pro free trial should check their billing status, because the post says trial accounts are excluded from Claude 5.5 access even though paid Pro accounts get it.

<details><summary>References</summary>
<ul>
<li><a href="https://www.orcarouter.ai/blog/claude-opus-5-5-and-sonnet-5-5-in-antigravity">Claude Opus 5 . 5 and Sonnet 5 . 5 Land in Google Antigravity</a></li>
<li><a href="https://discuss.ai.google.dev/t/claude-opus-sonnet-5-5-not-showing-on-google-ai-pro-offered-through-jio/186704">claude Opus / Sonnet 5 . 5 not showing on Google AI Pro offered...</a></li>
<li><a href="https://smartscope.blog/en/blog/antigravity-claude-55-pro-trial-model-retirement-2026/">Google Antigravity : Why Sonnet 5 . 5 / Opus 5 . 5 Are... - SmartScope</a></li>

</ul>
</details>

**Tags**: `#Antigravity`, `#Claude`, `#subscription-tiers`, `#model-deprecation`, `#access-restrictions`

---

<a id="item-tech-news-6"></a>
### [Hobbyist Gets Classic Mac OS Running on a Nintendo Wii](https://virtuallyfun.com/2026/10/29/my-favourite-powermac-is-a-nintendo-wii/) ⭐️ 6.0/10

A hands-on blog post reports getting classic Mac OS—Apple&\#x27;s Mac operating system from before 2001—to run on a Nintendo Wii. The author calls the console their favourite &\#x27;PowerMac,&\#x27; a nod to Apple&\#x27;s older Mac desktop line, and treats the result as a hobbyist project rather than an official Apple or Nintendo product. The post is an account of the experiment, not an announcement of a packaged release for ordinary users.

hackernews · DHowett · Oct 30, 17:25 · [Discussion](https://news.ycombinator.com/item?id=50307190)

**「Background」** Classic Mac OS is Apple&\#x27;s older Mac operating system, from before today&\#x27;s macOS, and a PowerMac is one of the Apple desktop computers that ran it. The project in this post is a hobbyist port that gets that old Mac software running on Nintendo&\#x27;s Wii, a 2006 game console sold to play games rather than Mac software. It is not an official Apple or Nintendo product; it depends on the Wii homebrew scene, in which owners modify their consoles to run unofficial software.

**「What it means」** The practical audience is people with a Wii already modified to run homebrew \(unofficial software for a locked-down console\). The post does not offer a route for a standard Mac, PC, or unmodified Wii to run old Mac programs.

**「From the comments」** Commenters connect the work to a developer&\#x27;s related projects, including Windows NT \(an older Microsoft operating system\) on Macintosh and GameCube/Wii hardware, suggesting it belongs to a wider homebrew effort. One reader asks whether the trick could be reversed by turning a PowerMac into a Wii, while another says emulators do not reproduce the experience of playing classic Mac games.

**Tags**: `#emulation`, `#platform-port`, `#nintendo-wii`, `#classic-mac-os`, `#homebrew`

---

<a id="item-tech-news-7"></a>
### [Habr Teaser Proposes Handing Off a Live Console AI Agent Session](https://habr.com/ru/companies/ruvds/articles/1101674/?utm_campaign=1101674&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A Habr article published by the hosting company RUVDS on 30 October 2026 describes a problem familiar to people who use command-line AI coding agents \(programs that run in a text terminal and edit code for you\): when a five-hour usage quota runs out mid-task, you want to continue with a different agent that still has allowance left. The common workaround is to have the model write a summary of the work into a file, conventionally named HANDOFF.md, which the next agent reads. The article says this often fails, because the model&\#x27;s own retelling is poor quality, context details are lost, the next agent has to be told the task again, and extra tokens \(the units of text a model is billed for\) are spent in the process. The teaser promises to explain how to pull a live session out of local log files and pass it to another agent, or move the work with its unsaved files to another computer, using a single command. No command, script, repository link, or evidence that the method works is included in the supplied text; the technique and its results remain unverified until the full article is available.

rss · Habr AI · Oct 30, 13:01

**「Where the session record lives」** Console AI agents are programs that run in a terminal window, read and edit files, and carry out coding chores on command. Each one keeps a detailed journal of the session on disk in its own format, and running a compaction command such as /compact to shorten the conversation does not erase the older entries — the journals are append-only, as the article notes. That stored record is what allows a live session to be moved to another agent instead of asking a model to write a fresh summary of the work so far.

**「What it means in practice」** For now, anyone hitting a five-hour cap still has the old choice: spend tokens on a written summary that may lose detail, or re-explain the task from scratch to the next agent. Copying the session&\#x27;s log files directly is only worth trying once the actual procedure is published, since log formats differ between agents and a failed transfer can leave unsaved work in a worse state than a careful manual summary.

<details><summary>References</summary>
<ul>
<li><a href="https://habr.com/ru/companies/ruvds/articles/1101674/">Перенос сессий между консольными ИИ - агентами без... / Хабр</a></li>

</ul>
</details>

**Tags**: `#AI coding agents`, `#session handoff`, `#rate limits and quotas`, `#developer tooling`, `#workflow`

---

<a id="item-tech-news-8"></a>
### [Xiaomi releases Xiaomi-OCR-0, a small open document-reading model](https://x.com/XiaomiTech_/status/2116154468358316380) ⭐️ 6.0/10

Xiaomi has published Xiaomi-OCR-0, an open-source \(free to download and modify\) document-understanding model with 0.8 billion parameters \(the adjustable numerical settings that make up a model; 0.8 billion is small by current standards\). It is designed to read documents, pull out key fields, and answer questions about text in images, a task called OCR visual question answering \(OCR turns pictures of text into machine-readable text\). Xiaomi says the model ranks first among models under 1 billion parameters on OmniDocBench v1.6, a document-parsing test, but this is a company-run claim with no independent confirmation or detailed scores in the source. The model&\#x27;s trained files, the code needed to run it, and a demo have been released.

telegram · zaihuapd · Oct 30, 16:00

**「Background」** Xiaomi-OCR-0 is a “vision-language” model: it reads a page as an image and produces text and layout information, rather than working only on text typed into a chat box. Its 0.8B size means about 800 million internal settings, small enough to download and run on modest hardware instead of a data-center cluster. “Open weights” means the trained model file and the code that runs it are published for anyone to use locally — not merely described in a paper or offered only through a hosted service.

**「What it means in practice」** For teams that need to turn scanned forms, invoices, or PDFs into usable text and fields, the release provides a downloadable model they can test without asking Xiaomi for access. Because the quality evidence is Xiaomi&\#x27;s own benchmark claim, they should check accuracy on their own documents and confirm the hardware needed before relying on it.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/xiaomi-research/Xiaomi-OCR-0">xiaomi-research/ Xiaomi - OCR - 0 · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#open-weight models`, `#OCR`, `#document understanding`, `#Xiaomi`, `#small models`

---

<a id="item-tech-news-9"></a>
### [Tencent releases Hy-Nomas video world model as open source](https://hy-nomas.hy.tencent.com/demo) ⭐️ 6.0/10

Tencent published Hy-Nomas, a &quot;world model&quot; — software that generates video of a scene from text and camera instructions — as open source under the Apache 2.0 licence, releasing both the code and the trained weights \(the files that let anyone download and run the model themselves\). The video is built up piece by piece, with earlier fragments kept in a memory buffer \(a KV cache\) so the scene stays consistent, and camera movement can be fixed in advance or changed between fragments. Tencent says the model can be fine-tuned on a user&\#x27;s own videos using LoRA \(a low-cost tuning method that adjusts only a small part of the model\), with ready-made add-ons for cinematic footage and robotics; a configuration for a single RTX 4090 home graphics card uses INT8 quantization \(crunching the model down to 8-bit numbers\), limited history and offloading to ordinary system memory, but its speed is not stated. The only published speed figure, roughly 18.5 frames per second, was measured on eight B200 data-centre GPUs with full history, so how fast it runs on a home machine is unknown.

telegram · ai\_newz · Oct 30, 13:37

**「What a world model is」** A “world model” here means software that generates video of a simulated scene and lets a user steer it with text instructions or camera moves, rather than producing one fixed clip from a prompt. The source post places Tencent’s Hy-Nomas alongside other recent systems such as MIRA, Solaris and Odyssey-3 and says it was announced a few days before Genie 4. Hy-Nomas builds the video in successive pieces while carrying earlier context forward, so the camera path can be set in advance or changed between pieces.

**「What it means in practice」** Anyone hoping to run this on a home computer has no way to judge whether it will be usable in real time: Tencent describes a setup that fits on a single RTX 4090 by lowering the video&\#x27;s numeric precision \(INT8 quantization\), keeping only a limited history of past frames and moving parts of the model into ordinary system memory, but it publishes no frame rate for that mode. The one speed figure given, about 18.5 frames per second, comes from eight datacenter-grade B200 chips running with full history, so it says nothing about home use. What the release does offer is customization: under the Apache 2.0 licence, with ready-made LoRA adapters \(small add-on weight sets that steer a model&\#x27;s output toward a particular look or task\), users can retrain it on their own video.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/tencent/Hy-Nomas">tencent / Hy - Nomas · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#open-weight models`, `#world models`, `#video generation`, `#LoRA fine-tuning`, `#self-hosting`

---

<a id="item-tech-news-10"></a>
### [Habr teaser: 125-billion-parameter AI model on an RTX 5070, details missing](https://habr.com/ru/articles/1101852/?utm_campaign=1101852&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A post on the Russian tech site Habr says a 125-billion-parameter &quot;MoE&quot; model — a model built from many specialist sub-networks, of which only a few are used for each request — now runs on an Nvidia RTX 5070 gaming graphics card, and that a 321-billion-parameter model runs on a single RTX 3090 with 64 GB of ordinary system memory. Parameters are the internal settings that make up a model; the count is a rough measure of its size. The post, dated 30 October, presents this as a jump from September, when it says the same kind of workload required server hardware. The excerpt contains nothing that would let a reader check the claim: no model names, no description of how the model is stored or split between system memory and the graphics card, and no measured speed. The author says the explanation and the real-world speed numbers are in the full article, which was not included.

rss · Habr AI · Oct 30, 15:38

**「Background」** MoE \(mixture-of-experts\) models split their parameters — the billions of learned numbers that make up the model — into many specialist sub-networks and activate only a few of them for each word they produce, so a 125B model never has to fit all 125 billion numbers into the graphics card&\#x27;s own memory \(VRAM\) at once. The technique behind this class of setup is to keep most of the model in the computer&\#x27;s ordinary system memory or on a fast solid-state drive and stream in only the pieces needed, with external write-ups of a similar tool, Strata, listing at least 12 GB of VRAM and 64 GB of system memory as the minimum. The Habr post frames the change as recent: in September, it says, running a 125-billion-parameter model on a home PC was a pastime for people with server racks, while by late October the same class of model reportedly runs on an RTX 5070.

**「What to check before believing it」** If such a claim holds up, the model is not sitting entirely inside the graphics card: a 321-billion-parameter model is many times larger than the memory on any consumer card, so most of it has to stay in ordinary system memory and be fed to the card as text is generated, which is usually far slower than a model that fits in graphics memory alone. For anyone considering this kind of home setup, the numbers that decide whether it is usable are the speed in tokens \(word fragments\) per second and the exact compressed, lower-precision copy of the model — called a quantization — that was used. Neither appears in the excerpt.

<details><summary>References</summary>
<ul>
<li><a href="https://runaihome.com/blog/strata-inference-engine-125b-gaming-gpu-guide-2026/">Strata Runs a 125B Model on a 12GB Gaming GPU: Real ...</a></li>
<li><a href="https://stratallm.org/">Strata LLM – Run 125B+ MoE Models on 12GB VRAM Consumer GPUs ...</a></li>
<li><a href="https://getaibook.com/news/strata-moe-offloading-125b-models-on-gaming-pcs/">Strata Runs a 125B Model on a Gaming PC at 94 Tokens Per ...</a></li>

</ul>
</details>

**Tags**: `#local-llm-inference`, `#open-weight-models`, `#moe-models`, `#consumer-gpus`, `#quantization-offloading`

---

<a id="item-tech-news-11"></a>
### [FLUX.3 klein used to make 290 dentist ad photos for about $3](https://habr.com/ru/articles/1101804/?utm_campaign=1101804&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A marketer who buys paid ads for dental clinics says he stopped booking photo shoots of doctors and generated the images instead: 290 frames for roughly $3, about one cent each. He used FLUX.3 klein — a small version of the FLUX image-generation model, which turns written descriptions into pictures — inside ComfyUI, a free program that chains image-generation steps together, running on RunPod, a service that rents cloud graphics cards by the hour. His stated reason is that a real doctor&\#x27;s face in the clinic outperforms stock photography, but arranging the shoot is slow and expensive and the ads burn out within a month. Only the opening of the article is visible in the feed; the prompts, settings and sample results are behind a &quot;read more&quot; link, so the pipeline and the picture quality cannot be checked from what is available.

rss · Habr AI · Oct 30, 13:52

**「The tools behind the setup」** FLUX.3 klein is an image model from Black Forest Labs whose files can be downloaded and run on your own hardware; it handles both generating pictures from text and editing existing ones. ComfyUI is the visual workspace used to run it, where a user connects image-generation steps instead of writing code, and RunPod supplies rented cloud graphics cards for the job. The case study describes replacing a paid photographer with that combination.

**「What it means in practice」** For a small clinic, or the freelancer buying its ads, the concrete promise is refreshing ad creative every month without paying a photographer — a few dollars of rented computing instead of a studio day. Reproducing it means opening a RunPod account, paying for graphics-card time and setting up a ComfyUI workflow, and since the article&\#x27;s actual settings are not in the accessible portion, the $3 total remains the author&\#x27;s claim rather than a verified per-image price.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.comfy.org/tutorials/flux/flux-3-klein">FLUX 3 Image Klein in ComfyUI: Text-to-Image and Edit</a></li>
<li><a href="https://www.runpod.io/articles/guides/comfy-ui-flux">ComfyUI + Flux on Runpod: Automate AI Image Workflows</a></li>
<li><a href="https://docs.runpod.io/tutorials/pods/comfyui">Generate images with ComfyUI - Runpod Documentation</a></li>

</ul>
</details>

**Tags**: `#FLUX.3`, `#ComfyUI`, `#RunPod`, `#image-generation`, `#cost-efficiency`

---

<a id="item-tech-news-12"></a>
### [HuggingFace for Beginners: Choosing and Running a Model](https://habr.com/ru/companies/bothub/articles/1101764/?utm_campaign=1101764&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A new Russian-language guide on Habr aims to help beginners navigate HuggingFace, a developer platform where people share openly available machine-learning models \(downloadable trained files that power AI programs\), datasets \(collections of example data\) and apps; the author describes it as a GitHub for AI, a shared library where people upload and download files. HuggingFace lists about 800,000 models, and the guide says its interface assumes users already know the platform, so a newcomer can end up downloading the wrong datasets or giving up. The visible excerpt only sets up that problem and promises a walkthrough of the site and of working with data and model weights \(the numeric parameters that make a trained model work\); it does not name a recommended model, give download sizes or hardware requirements, or show a verified step-by-step run.

rss · Habr AI · Oct 30, 12:53

**「Background」** Hugging Face is an online hub where people publish and download open AI models and data sets; the article describes it as a GitHub for AI \(a public site for sharing and collaborating on files\) and notes that it lists roughly 800,000 models. A model&\#x27;s “weights” are the files that let it perform a task, and running a model locally means using those files on your own computer instead of through a company&\#x27;s online service.

**「In practice」** For a non-developer, the practical consequence is that HuggingFace is a catalogue and sharing hub, not a single ready-made AI product: a newcomer has to choose a model and work with its files rather than open one app and start using it.

**Tags**: `#Hugging Face`, `#open-weight models`, `#model selection`, `#local inference`, `#beginner tutorial`

---

<a id="item-tech-news-13"></a>
### [22-Billion-Parameter LTX-2.5 Video Model Reported Running on a 10 GB RTX 3080](https://habr.com/ru/articles/1101646/?utm_campaign=1101646&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr author reports running LTX-2.5, a video-generation model with 22 billion parameters \(the learned numeric settings that make up the model\), on his own Windows PC with an RTX 3080 graphics card and 10 GB of video memory \(VRAM, the card&\#x27;s dedicated memory\). He says he also integrated it into a chain of steps for making short videos. The post&\#x27;s figures show the scale of the gap: the model&\#x27;s main transformer weights — the trained numbers that do most of the work — take 39 GB, and its text encoder \(the part that turns a written prompt into instructions the model can use\) takes another 24.5 GB. The excerpt gives no configuration, memory-saving method, speed or quality measurements, code, or reproducible steps, so this is an unverified report rather than a setup others can copy.

rss · Habr AI · Oct 30, 11:17

**「What the numbers mean」** LTX-2.5 is a video-generation model from Lightricks, distributed as downloadable model files that can run on a local computer rather than only through a hosted service. Its “22 billion parameters” are the learned numerical settings that shape each generated frame; the count is a rough measure of model size, not a guarantee of quality. The practical constraint is video memory \(VRAM, the graphics card’s own working memory\): the model’s components total far more than the 10 GB on an RTX 3080, so running it requires loading, compressing, or swapping pieces instead of holding the whole model in memory at once.

**「What it means in practice」** For people who make video on a home PC, the claim suggests that a 10 GB card might not be an absolute barrier to a 22-billion-parameter model. But without the settings, speed, resolution, clip length, or quality results, there is nothing here to reproduce or to use when judging whether a similar card can do the same job. Treat it as a report to watch, not as buying advice.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/Lightricks/LTX-2.5">Lightricks/ LTX - 2 . 5 · Hugging Face</a></li>
<li><a href="https://ltx.io/model/ltx-2-5">LTX - 2 . 5 : LTX&#x27;s Latest AI Open-Source Foundation Model | LTX</a></li>

</ul>
</details>

**Tags**: `#LTX-2.5`, `#local inference`, `#RTX 3080`, `#video generation`, `#VRAM optimization`

---

<a id="item-tech-news-14"></a>
### [Reports: Claude accounts suspended right after passport checks](https://habr.com/ru/companies/aurorium/articles/1101594/?utm_campaign=1101594&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

Users of Anthropic&\#x27;s Claude chatbot have reported that their accounts were suspended immediately after they submitted identity documents, according to a Habr post published by Aurorium, a company that sells anti-detect browsers \(browsers built to disguise the fact that several accounts are being run from one machine\). The post says the suspensions hit holders of passports from countries Anthropic restricts, and that VPN use \(routing a connection through another country so the service sees a different location\) was also cited as a trigger, even though, it argues, Claude&\#x27;s published rules bar serving certain countries rather than barring users by the country on their passport. The supporting evidence is a linked Reddit thread, not any statement from Anthropic, and the section of the article that promises to explain the actual detection mechanism is cut off in the available text. The author sells a product aimed at exactly this problem, so the framing carries a commercial interest.

rss · Habr AI · Oct 30, 10:06

**「Earlier context」** Claude, Anthropic&\#x27;s AI chatbot, uses an outside company called Persona Identities to check users&\#x27; identity documents, according to Anthropic&\#x27;s help centre. A Meduza report published on 29 October said users had complained on Reddit, X and Telegram that their Claude accounts were suspended soon after they completed that check with Russian passports. The Habr post is from a seller of anti-detect browsers \(browsers built to disguise a device and its location\) and promises to separate the reports from speculation, but the visible excerpt ends before it explains how any ban worked.

**「What it means if you pay for Claude」** If Claude asks you to upload a passport or other ID to keep using a paid account, the reported pattern means access can vanish at the moment you comply rather than later. The available text gives no verified way to predict which documents or connection routes are accepted, and no stated remedy once an account is suspended.

<details><summary>References</summary>
<ul>
<li><a href="https://meduza.io/en/feature/2026/10/29/claude-users-say-their-accounts-were-banned-after-verification-showed-a-russian-passport">Claude users say their accounts were banned after verification ...</a></li>
<li><a href="https://support.claude.com/en/articles/14328960-identity-verification-on-claude">Identity verification on Claude | Claude Help Center</a></li>

</ul>
</details>

**Tags**: `#account-bans`, `#anthropic-claude`, `#access-restrictions`, `#identity-verification`, `#anti-detect-browsers`

---

<a id="item-tech-news-15"></a>
### [DIY project turns an MSI GS75 laptop keyboard into a standalone USB keyboard](https://habr.com/ru/articles/1101616/?utm_campaign=1101616&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A home-built prototype now lets the keyboard from an MSI GS75 laptop work as a separate USB keyboard. The maker worked out how the keys are wired, designed two versions of a circuit board around an STM32 chip \(a small programmable microcontroller\), and wrote custom USB HID firmware \(device software that lets a keyboard connect without special drivers\). The prototype has 102 keys, a USB Type-C connection, an Fn key for secondary shortcuts and media controls, and an NKRO mode \(which registers many keys pressed at once\). The write-up says the hardest part was getting key handling right, including false “phantom” keypresses, and the supplied excerpt provides no schematics, firmware, parts list, or independent proof that others can reproduce it.

rss · Habr DIY · Oct 30, 09:23

**「Why a laptop keyboard can&\#x27;t just be unplugged and reused」** A laptop keyboard is not a self-contained USB device. It is a grid of switches wired in rows and columns \(a &quot;matrix&quot;\), and it only means anything to the laptop&\#x27;s own built-in controller chip, which constantly scans that grid to work out which key is pressed. To use the keyboard on a desk, someone has to supply that missing controller: a small microcontroller \(a cheap chip that runs one simple program\) wired to the grid, plus firmware — the program on the chip — that makes the computer see it as an ordinary USB keyboard. The author&\#x27;s project is essentially rebuilding that part from scratch, which is why the article covers reverse-engineering the key wiring, two versions of a custom circuit board, and writing the USB keyboard software himself.

**「Practical impact」** Anyone hoping to copy the result should expect a hands-on electronics project, not a plug-and-play adapter: the prototype depends on a custom circuit board and firmware, and the excerpt offers no board files or code to build one.

**Tags**: `#hardware`, `#STM32`, `#keyboard`, `#USB-HID`, `#DIY`

---

<a id="item-tech-news-16"></a>
### [ai-automation-jira claims nine-stage Jira-to-reviewed-code AI workflow](https://github.com/pruthvidarji1993/ai-automation-jira) ⭐️ 5.0/10

A GitHub project called ai-automation-jira is being promoted as a nine-stage AI workflow that takes a Jira ticket \(a task in the Jira project-tracking system\) through to a reviewed pull request \(a proposed code change checked before it is merged\), using either Claude Code or GitHub Copilot \(AI assistants that write and edit code\). The MIT-licensed project \(MIT allows others to reuse and modify the code\) says it has two human review points, one when the plan is made and one when the exact code changes, or diff, are reviewed, and that it supports two Claude models, Opus and Sonnet. The promotion gives no code examples, setup details, or evidence that the workflow works as described; the repository had 1 star, 0 forks, and 2 open issues, so it is an unvalidated early project rather than a proven tool.

telegram · aipluscn · Oct 30, 05:07

**「Background」** Jira is a widely used work-tracking tool: each bug or feature request is filed as a &quot;ticket&quot; \(a work order with a description and a status such as to-do, in progress or done\) and moved through stages by the team. A pull request, or PR, is a proposed code change that a teammate reviews before it is merged into the shared codebase. Claude Code and GitHub Copilot are AI coding assistants that can read a project&\#x27;s files and write or edit code on a developer&\#x27;s behalf; this project&\#x27;s stated aim is to chain those tools to a ticket&\#x27;s stages, pausing for a person to approve the plan and again to approve the code change.

**「What trying it would involve」** Treat this as a starting point you would have to check yourself: the repository shows 1 star, 0 forks and 2 open issues, so there is no visible sign of other teams running it in real work. You would do the setup yourself — installing the plugin and connecting it to a Jira project \(the issue tracker many teams use for tasks and bug reports\) — and the connection needs credentials that let a script read tickets and open pull requests \(proposed code changes awaiting review\) on your code repository, so those permissions should be narrowly scoped. The two human checkpoints, at the plan stage and at the diff \(the before-and-after view of the changed code\), mean the flow is built to keep a person approving each step rather than merging code unattended.

**Tags**: `#Claude Code`, `#GitHub Copilot`, `#Jira`, `#AI workflow automation`, `#developer tooling`

---

<a id="item-tech-news-17"></a>
### [Leak: DeepSeek website code hints at &\#x27;Cyber&\#x27; model limited to businesses](https://x.com/ProbiusOfficial/status/2116001318053777661) ⭐️ 5.0/10

A tipster \(X user @ProbiusOfficial\) says they found an application form for a DeepSeek model called &quot;Cyber&quot; inside the JavaScript on DeepSeek&\#x27;s official website — the code that makes its web pages work. According to the post, the official application route requires a business identity, including a business license and a letter of authorization, while a separate invitation channel for individuals exists but its conditions are unknown. DeepSeek has not confirmed that such a model exists, and the post gives no detail on what the model does, what it would cost, how much usage it allows, or when it might appear.

telegram · zaihuapd · Oct 30, 05:45

**「Background」** A website sends its page code — including JavaScript, the programming language a browser runs to make pages interactive — to every visitor&\#x27;s computer, and unfinished or unlinked pieces of that code can sit there before any public page points to them. That is how enthusiasts occasionally spot features a company has not announced, which is the nature of this tip: strings in DeepSeek&\#x27;s site code, not a working page. Asking for a business licence \(营业执照, the registration document for a Chinese company\) plus an authorization letter is the usual paperwork when a company, rather than an individual, applies for a business service.

**「What it could mean for users」** If the entry is real, people without a registered company would not be able to use the public application form and would depend on the unexplained individual invitation route, so access would not automatically open to everyone at launch. Nothing can be signed up for or planned around yet.

**Tags**: `#deepseek`, `#model-release-rumor`, `#access-restrictions`, `#enterprise-access`, `#ai-news`

---

## Financial News

<a id="item-finance-news-1"></a>
### [DeepSeek Reportedly Raises RMB 105.5 Billion in Second Round](https://www.theinformation.com/articles/behind-deepseeks-16-billion-funding-chinese-tech-titans-state-players) ⭐️ 7.0/10

DeepSeek reportedly raised RMB 105.5 billion in a second funding round at a valuation above RMB 615.5 billion, with nearly 30 investors, according to The Information; the report has not been confirmed by the company. State-linked investors supplied about 27% of the round, up from 2% in the June 2026 first round that raised about RMB 51 billion.

telegram · zaihuapd · Oct 30, 12:37

**「Background」** The reported round is DeepSeek’s second, following a first round completed in June 2026 that raised about RMB 51 billion and drew roughly 2% of its capital from state-linked investors, according to the same report.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theinformation.com/articles/behind-deepseeks-16-billion-funding-chinese-tech-titans-state-players">Behind DeepSeek’s $16 Billion Funding: Chinese Tech Titans ...</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#AI financing`, `#China tech`, `#startup valuation`, `#state-backed investment`

---

<a id="item-finance-news-2"></a>
### [Four Japanese automakers&\#x27; China output falls below 40% of peak](https://weibo.com/1642634100/Rp6qUwLKa) ⭐️ 7.0/10

Combined China production at Toyota, Honda, Nissan and Mazda fell 32% year on year to about 1.02 million vehicles in April–September 2026, the lowest for that period since 2008 and less than 40% of the 2020 peak. Honda plans to cut its annual China fuel-vehicle capacity from 1.49 million to 1 million units.

telegram · zaihuapd · Oct 30, 13:38

**「Background」** The comparison point is the 2020 peak: Japanese brands’ share of China’s car market has fallen from 23.1% to about 9.6% over five years, according to a market analysis.

<details><summary>References</summary>
<ul>
<li><a href="https://post.smzdm.com/p/a95lm43o/">post.smzdm.com/p/a95lm43o</a></li>

</ul>
</details>

**Tags**: `#Japanese automakers`, `#China auto production`, `#Honda`, `#capacity cuts`, `#auto industry`

---

<a id="item-finance-news-3"></a>
### [法国国民议会通过数据流量税修正案](https://www.assemblee-nationale.fr/dyn/17/amendements/3210A/AN/1358) ⭐️ 7.0/10

法国国民议会通过一项预算修正案，拟对内容供应商向互联网用户发送的数据按每 GB 0.055 欧元征税，并设置与企业营业额挂钩的税额上限；提案方预计该税每年可带来 100 亿欧元收入。该修正案尚需经过后续立法程序，可能被修改或删除，企业是否会把成本转嫁给消费者仍不确定。

telegram · zaihuapd · Oct 31, 02:05

**「Background」** The measure is a Socialist-sponsored amendment to the budget bill and still needs further legislative approval; under the proposed mechanism, internet access providers would count the gigabytes sent by each content provider so the tax can be billed to that provider.

<details><summary>References</summary>
<ul>
<li><a href="https://www.jeuxvideo.com/forums/42-51-77491997-1-0-1-0-nouvelle-taxe-sur-les-flux-de-donnees-internet-0-05-eur-par-giga.htm">Nouvelle taxe sur les flux de données internet : 0 ,05... - jeuxvideo.com</a></li>
<li><a href="https://next.ink/264997/le-parti-socialiste-a-fait-passer-sa-taxe-au-gigaoctet-a-lassemblee-nationale/">Le Parti socialiste a fait passer sa taxe au gigaoctet à l’ Assemblée ...</a></li>

</ul>
</details>

**Tags**: `#法国`, `#数据流量税`, `#财政预算`, `#数字政策`, `#科技监管`

---