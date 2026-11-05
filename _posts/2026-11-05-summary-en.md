---
layout: default
title: "Horizon Summary: 2026-11-05 (EN)"
date: 2026-11-05
lang: en
---

> From 130 items, 28 important content pieces were selected

---

**Technology News**
1. [Moonshot releases Kimi K3.1 Pro model files, claiming lower cost on long inputs](#item-tech-news-1) ⭐️ 8.0/10
2. [Ripple-65B Preview Claims Top U.S. Open-Weight Score for AI Coding Agents](#item-tech-news-2) ⭐️ 6.0/10
3. [Nine Small AI Models Tested on a Cheap Server Without a Graphics Card](#item-tech-news-3) ⭐️ 6.0/10
4. [A blogger&\#x27;s local Qwen on a 16 GB card narrowed the gap after setup fixes](#item-tech-news-4) ⭐️ 6.0/10
5. [Keystone plugin gives Claude Code assistant real commands for a self-hosted AI gateway](#item-tech-news-5) ⭐️ 6.0/10
6. [AgentScope Announces Piccolo Decision Models in 27B, 9B and 4B](#item-tech-news-6) ⭐️ 6.0/10
7. [Open-source Airtable tool gives AI assistants 72 actions](#item-tech-news-7) ⭐️ 6.0/10
8. [new-api 1.0.0-rc.48 signs its caches and adds vendors&\#x27; own task API addresses](#item-tech-news-8) ⭐️ 5.0/10
9. [OpenAI says its AI pipeline found 948 Linux root-escalation exploits](#item-tech-news-9) ⭐️ 5.0/10
10. [Hugging Face announces on-device Phonon text-to-speech model, claiming top benchmarks](#item-tech-news-10) ⭐️ 5.0/10
11. [Dharma Field Extractor claims to turn any document into structured JSON](#item-tech-news-11) ⭐️ 5.0/10
12. [PiPedal Turns a Raspberry Pi Into a Guitar Effects Rig](#item-tech-news-12) ⭐️ 5.0/10
13. [Lumio 1.4 adds Qwen Code and Cline to MacBook-notch AI agent monitor](#item-tech-news-13) ⭐️ 5.0/10
14. [Home assistant project reports gains from training on its own history](#item-tech-news-14) ⭐️ 5.0/10
15. [A 15-Hour Claude Suspension Shows the Risk of One-Vendor AI Reliance](#item-tech-news-15) ⭐️ 5.0/10
16. [Pepper-Orchestrator Add-On Splits Multi-Module Coding Work Across AI Agents](#item-tech-news-16) ⭐️ 5.0/10
17. [Habr Post Argues Coding-Agent Context Should Live in the Project Files, Not Chat](#item-tech-news-17) ⭐️ 5.0/10
18. [Customs Clerk Builds ESP32 Noise and Occupancy Monitor for Rental Apartments Using AI](#item-tech-news-18) ⭐️ 5.0/10
19. [DIY controller lets you program it on a tiny screen with three buttons](#item-tech-news-19) ⭐️ 5.0/10
20. [Xiaomi begins youth-apartment trial of Xiaomi-Robotics-1 robot system](#item-tech-news-20) ⭐️ 5.0/10
21. [Huawei Cloud to launch openPangu-2.1-Pro on Nov 15, targeting HarmonyOS code](#item-tech-news-21) ⭐️ 5.0/10
22. [agents-scaffold bundles Claude Code, Codex and Antigravity with project presets](#item-tech-news-22) ⭐️ 5.0/10
23. [Isle post claims AI usage stats and per-assistant permissions](#item-tech-news-23) ⭐️ 5.0/10
24. [AI 代理工具库 DmitriyYukhanov/agent-plugins 发布，是 AI 工具集成化趋势的信号](#item-tech-news-24) ⭐️ 5.0/10
25. [MaccyPlus gives AI agents a command line into macOS clipboard history](#item-tech-news-25) ⭐️ 5.0/10
26. [NVIDIA Announces OpenShell With Separate Permissions for AI Agents](#item-tech-news-26) ⭐️ 5.0/10

**Financial News**
1. [China Blocks SoftBank&\#x27;s $5.4 Billion Acquisition of ABB Robotics Unit](#item-finance-news-1) ⭐️ 8.0/10
2. [Nintendo Switch 2 second-quarter sales fall 41% year over year](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Moonshot releases Kimi K3.1 Pro model files, claiming lower cost on long inputs](https://huggingface.co/moonshotai/Kimi-K3.1-Pro) ⭐️ 8.0/10

Moonshot AI has published the model files, known as &\#x27;weights,&\#x27; for Kimi K3.1 Pro on Hugging Face, a public site for sharing AI models, so outside organizations can download and run it instead of only using Moonshot&\#x27;s own service. The source post says the update adds extra training after the main run and replaces one internal attention design, &\#x27;Gated MLA,&\#x27; with &\#x27;Gated DSA&\#x27;; attention is the part that decides which earlier text to weigh. That change is meant to make long inputs cheaper to process and reduce the memory needed to keep a long conversation in view, though the claim has not been independently verified. Most people will meet the model through apps or services that rent access to it—commenters say third-party providers including OpenRouter are already hosting it—and one commenter estimated that running it locally would take eight top-end Nvidia B300 chips, far beyond a personal computer.

hackernews · abrarthought · Nov 4, 15:30 · [Discussion](https://news.ycombinator.com/item?id=50366999)

**「Background」** Kimi K3, released in July 2026, is Moonshot&\#x27;s 2.8-trillion-parameter model \(parameters are the learned numbers that define a model&\#x27;s behavior\) with a context window of one million tokens — the amount of text it can consider at once. K3 used an attention design called Gated MLA to decide which earlier parts of that text to keep consulting; doing so requires holding a large &quot;KV cache,&quot; the model&\#x27;s working memory of the conversation, which gets expensive at long context. K3.1 Pro is a point update that, according to the release note and commenters, swaps those Gated MLA layers for a leaner variant called Gated DSA, intended to shrink that memory burden and lower the cost of serving the model.

**「What changes for people using it」** For anyone who uses these models through a chat app or coding assistant rather than running one themselves, K3.1 Pro is something you reach through a hosting company, not something you install: a commenter estimates it needs a node of eight high-end Nvidia B300 chips to run, far beyond a single desktop. Because the previous Kimi K3 was listed on OpenRouter at about $0.15 per million input tokens and $10.56 per million output tokens \(a token being a small chunk of text the model reads or writes\), buyers should compare each provider&\#x27;s price and speed for K3.1 Pro rather than assume the newer version is cheaper — one commenter reports Together serving it at roughly double Moonshot&\#x27;s own throughput for the same price.

**「Community discussion」** One commenter argued the key change is swapping the model&\#x27;s internal mechanism for weighing earlier text after training, which should sharply cut the memory needed to serve long conversations. Another reported that a third-party host appears to offer double Moonshot&\#x27;s response speed at the same price, while a third said the model does not clearly beat rival releases and looks tuned to test scores, leaving the practical gain disputed.

<details><summary>References</summary>
<ul>
<li><a href="https://inferencex.semianalysis.com/model/kimi-k3">Kimi K3 — Architecture, Evals &amp; Inference Performance</a></li>
<li><a href="https://dhruvpendharkar.github.io/2026/07/31/understanding-kimi-k3s-attention.html">understanding kimi k3&#x27;s attention - dhruvpendharkar.github.io</a></li>
<li><a href="https://openrouter.ai/moonshotai/kimi-k3">Kimi K 3 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://huggingface.co/moonshotai/Kimi-K3">moonshotai/ Kimi - K 3 · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#kimi`, `#open-weight-models`, `#moonshot-ai`, `#inference-cost`, `#model-release`

---

<a id="item-tech-news-2"></a>
### [Ripple-65B Preview Claims Top U.S. Open-Weight Score for AI Coding Agents](https://www.ricursive.com/ripple) ⭐️ 6.0/10

Ricursive has published a preview of Ripple-65B, which it describes as an open-weight model — meaning the underlying file \(the &quot;weights&quot;\) can in principle be downloaded and run by anyone — built for &quot;agentic coding,&quot; where an AI carries out coding tasks by taking actions on a computer rather than only answering questions. The model has 65 billion parameters \(the internal numbers a model learns during training; more parameters generally mean a larger, slower model\), and the preview bills it as state-of-the-art among U.S. open-weight models for that task. The announcement as supplied does not state the license, whether the weights are actually downloadable, the price of any hosted access, or the context length \(how much text the model can hold at once\). In the comments, one reader cites a score of 80.5 on Terminal Bench 2.1, a test of agentic coding, against 84.3 for Qwen 3.8 Flash Next and 73.0 for Qwen 3.8-27B — a comparison the company itself did not make in the material available here.

hackernews · Philpax · Nov 4, 18:53 · [Discussion](https://news.ycombinator.com/item?id=50369925)

**「What Ripple-65B Preview is」** Ripple-65B Preview is a preview release of an open-weight model: the trained model files are published so others can download and run or adapt them, rather than being available only through a company&\#x27;s hosted service. The &quot;65B&quot; means 65 billion parameters \(the model&\#x27;s internal settings, roughly a measure of its size\), which makes it much harder to run on ordinary consumer hardware than smaller models. It is aimed at &quot;agentic coding,&quot; meaning software that can carry out multi-step programming work such as editing files and running commands, not just answer a single coding question.

**「What it means if you want to use it」** Ripple-65B is a &quot;dense&quot; model, meaning all 65 billion parameters are used for every word it generates, unlike &quot;mixture-of-experts&quot; models that switch on only a fraction of their size per request. That makes it impractical to run on ordinary laptops or consumer graphics cards, so most users would end up paying a hosting provider instead — and the terms for that are not yet published. Anyone planning to standardize on it should wait for the license and weight-download details, since a preview does not guarantee either.

**「What commenters argued」** Several readers questioned the &quot;state of the art&quot; label, with one arguing the term has been narrowed until it only means best among U.S.-made open models of a certain size, and another noting the preview does not mention competing open-weight models at all. A local-model enthusiast welcomed the release but said a 65-billion-parameter dense model will be far too slow for hobbyists compared with smaller or mixture-of-experts models like Qwen&\#x27;s 27B-class offerings, while another commenter said U.S. jurisdiction is itself a real requirement for some users who are barred from non-U.S. providers.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/ricursiveAI/Ripple-65B-Preview">ricursiveAI/ Ripple - 65 B -Preview · Hugging Face</a></li>
<li><a href="https://www.ricursive.com/ripple">Recursive Self-Improvement via AI for Chip... - Ricursive Intelligence</a></li>

</ul>
</details>

**Tags**: `#open-weight-models`, `#agentic-coding`, `#model-release`, `#benchmarks`, `#self-hosting`

---

<a id="item-tech-news-3"></a>
### [Nine Small AI Models Tested on a Cheap Server Without a Graphics Card](https://habr.com/ru/articles/1103894/?utm_campaign=1103894&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A Russian-language Habr article describes a hands-on test of nine small language models, each with 1 billion to 4 billion parameters \(a rough measure of a model’s size\), on a rented server costing about 1,500 rubles a month. The server had four virtual processor cores, 4 GB of memory, and no graphics card; the models were run through Ollama, software for downloading and running AI models on a computer you control. The author says they were tried on seven business tasks — including sorting incoming requests, extracting contact details from email, and judging reviews — plus a load test \(a check of how the system handles repeated or simultaneous requests\). The excerpt available here stops before the model names, speed figures, quality results, and conclusions, so the test’s outcomes cannot be reported.

rss · Habr AI · Nov 5, 10:44

**「Background」** The largest commercial AI models are expensive to run and usually need graphics processors. The article’s premise is that many routine office tasks do not need that much capability. A virtual private server \(VPS\) is a rented slice of a shared computer; one with only an ordinary processor instead of a graphics card is cheaper but generally slower for AI work.

**Tags**: `#local-inference`, `#ollama`, `#open-weight-models`, `#self-hosting`, `#vps-cost`

---

<a id="item-tech-news-4"></a>
### [A blogger&\#x27;s local Qwen on a 16 GB card narrowed the gap after setup fixes](https://habr.com/ru/articles/1103784/?utm_campaign=1103784&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A Russian-language hands-on blog post reports that a locally run Qwen model closed much of the distance to cloud-hosted flagship models on the same hardware, after the author replaced his heavily squeezed copy of the model&\#x27;s weights \(the billions of numbers that make up the model\) with a fuller one and corrected his server configuration. The machine is a workstation with one Nvidia RTX 5080 graphics card holding 16 GB of video memory, plus 62 GB of ordinary system memory. In two earlier tests the author reported that very aggressively compressed builds of Qwen scored 33% \(8 of 24 questions\) on tasks over a laboratory notebook and 80% \(16 of 20\) on fixing bugs in Delphi programs, against 19 of 20 for Anthropic&\#x27;s cloud model Claude Sonnet 5.5; the builds named IQ2\_XS and IQ1\_M squeeze each weight into roughly two or one bits instead of the usual sixteen, which is what lets a large model fit in 16 GB at all. The published excerpt covers only the setup and the claim of a comeback: it gives no new scores, no timings and no configuration details, so the size of the improvement cannot yet be checked.

rss · Habr AI · Nov 5, 08:36

**「Background」** Running a language model on your own computer means loading its weights — the model’s learned parameters — into the graphics card’s memory, and a 16 GB card leaves little room. Earlier tests by this author on the same workstation found local models behind cloud services: a heavily compressed Qwen build scored 8 out of 24 on lab-journal questions, while a Qwen coding build solved 16 of 20 software bug-fixing tasks in Delphi, a programming language, short of Claude Sonnet 5.5’s 19 out of 20.

**「What it means in practice」** For anyone running a downloadable model on a 16 GB card, the author&\#x27;s argument is that a disappointing result may reflect the compression level and the surrounding tooling rather than the memory ceiling, so the least-compressed build that still fits, and a correctly configured server, are the first things to check before concluding the hardware is the limit. Readers cannot yet act on the specific settings, because the excerpt does not publish them, and the revised scores are the author&\#x27;s own claim, not an independent measurement.

**Tags**: `#local LLM`, `#Qwen`, `#quantization`, `#VRAM`, `#model comparison`

---

<a id="item-tech-news-5"></a>
### [Keystone plugin gives Claude Code assistant real commands for a self-hosted AI gateway](https://habr.com/ru/articles/1100548/?utm_campaign=1100548&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A Habr post introduces a Keystone plugin for Claude Code, Anthropic&\#x27;s coding assistant that runs in a terminal. The plugin bundles eight “skills”—packaged instructions that give the assistant Keystone&\#x27;s real commands, options, and configuration fields—plus an MCP server \(a connector built on the Model Context Protocol standard that lets the assistant inspect external software\) so it can see what the gateway is running. Keystone is a self-hosted large language model \(LLM\) gateway: software a user runs on their own systems to give applications one access point to multiple AI models while holding the credentials for model providers, routing requests, switching during failures, and enforcing spending limits. The post promises installation in a single conversation and says keys never appear in the chat, but the available text gives no install commands or configuration details and offers no independent test of those claims.

rss · Habr AI · Nov 5, 08:30

**「Context」** Keystone \(KTMS\) is a gateway you run on your own server: your applications send all their model requests to a single address, and it holds the vendors&\#x27; API keys, picks a model by rule, switches over when a provider fails, and enforces spending limits. Claude Code is an AI coding assistant that works in the terminal, and MCP \(Model Context Protocol, a shared way to plug outside tools into such assistants\) is how Keystone&\#x27;s server lets the assistant read and change the gateway&\#x27;s configuration itself rather than having scripts written against its interface, without the key ever reaching the assistant. That matters because an assistant told to &quot;set up the gateway for us&quot; cannot know the real commands, flags and config fields, so it produces plausible-looking settings that do not work — the plugin packages the accurate instructions that replace that guesswork.

**「What it means in practice」** For people who already use Claude Code with a self-hosted Keystone gateway, the practical benefit would be fewer invented settings when they ask the assistant to deploy or inspect it. Until the plugin&\#x27;s commands and setup steps are published, however, they cannot check compatibility or reproduce the promised single-conversation install.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ai-process/ktms">GitHub - ai-process/ ktms : Self - hosted LLM gateway : vendor keys...</a></li>

</ul>
</details>

**Tags**: `#Claude Code`, `#MCP`, `#LLM gateway`, `#self-hosted`, `#developer tooling`

---

<a id="item-tech-news-6"></a>
### [AgentScope Announces Piccolo Decision Models in 27B, 9B and 4B](https://linux.do/u/chenxr) ⭐️ 6.0/10

The AgentScope team has announced Piccolo, a family of three AI models it calls “decision models,” at sizes labeled 27B, 9B and 4B. The B numbers mean billions of parameters—the learned internal settings that scale with a model’s size—and the announcement does not define what “decision” tasks the models are built for. AgentScope linked an online playground and ModelScope download pages, but gave no benchmark results, license terms, hardware requirements or pricing, so users cannot yet judge performance or whether they may deploy the models.

telegram · linuxdo\_tg · Nov 5, 14:33

**「What the Piccolo models are」** Piccolo is presented as a family of “decision models,” meaning models meant to choose or recommend an action inside an automated workflow rather than hold a general conversation. The labels 27B, 9B and 4B refer to model size in billions of parameters—the internal settings adjusted during training—so the three versions differ mainly in how much computing power they need; a larger number does not by itself guarantee better results.

**「What it means if you want to try it」** The numbers in the name are parameter counts — a rough measure of model size and therefore of how much computer you need — so the 4B and 9B versions are the ones plausibly runnable on an ordinary laptop, while the 27B needs a serious machine or a compressed copy; third-party listings already show a Q4\_K\_M build of Piccolo-27B, a 4-bit squeezed version made for local use. Because the announcement itself gives no license terms or hardware requirements, anyone planning to self-host should confirm both before building around it, whereas the browser playground lets you test the models with no setup at all.

<details><summary>References</summary>
<ul>
<li><a href="https://pirateface.co/agentscope-ai/Piccolo-27B-Q4_K_M">agentscope -ai/ Piccolo - 27 B -Q4_K_M · Pirate Face</a></li>

</ul>
</details>

**Tags**: `#模型发布`, `#开源模型`, `#AgentScope`, `#Piccolo`, `#决策模型`

---

<a id="item-tech-news-7"></a>
### [Open-source Airtable tool gives AI assistants 72 actions](https://github.com/Automations-Project/VSCode-Airtable-Formula) ⭐️ 6.0/10

An open-source project is offering an add-on that lets AI assistants work with Airtable, a spreadsheet-like database service, through MCP \(a standard way for an AI assistant to call outside apps and data\). The project says it exposes 72 Airtable actions, including formula checks, field creation, view management and record duplication, and lists one-click installation for VS Code, Cursor, Windsurf, Claude Desktop, Cline and Amp. It runs locally, keeps the login in the computer&\#x27;s built-in password store, and offers read-only, safe-write and full-access modes; the code is free under the MIT open-source license. The caveat is that it uses Airtable&\#x27;s internal API, the connection behind Airtable&\#x27;s own website, rather than the official public API, and the post offers no hands-on test of whether it will keep working if Airtable changes that internal interface.

telegram · aipluscn · Nov 5, 01:48

**「Background」** An MCP server is a connector that lets an AI assistant use tools inside another piece of software; MCP stands for Model Context Protocol, a shared way for AI apps to find and call those tools. Airtable is a spreadsheet-like database service where teams keep structured records in “bases,” and this project connects those bases to AI assistants and code editors. It uses Airtable’s internal API \(the programming interface Airtable’s own apps use\) rather than the official public API, which is how it can offer actions the public API does not expose.

**「What it means if you use Airtable」** For Airtable users, the practical draw is that an AI assistant inside your editor can create fields, manage views, validate formulas and copy records, not just read and write rows the way Airtable&\#x27;s own official MCP connector does. The trade-off is durability: the extension talks to Airtable&\#x27;s internal API rather than the documented public one, so it can stop working without warning when Airtable changes its insides. Start it in read-only mode, and keep the official server alongside it for anything you depend on, since the extra power comes with the ability to modify or delete real data if you switch it to full access.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/automations-Project/VSCode-Airtable-Formula">GitHub - Automations - Project / VSCode - Airtable - Formula : VS Code...</a></li>
<li><a href="https://www.claudemarket.ai/mcp/Automations-Project/VSCode-Airtable-Formula">Airtable User MCP Server | Claude Market</a></li>
<li><a href="https://support.airtable.com/articles/9897799762-using-the-airtable-mcp-server">Using the Airtable MCP server</a></li>
<li><a href="https://airtable.com/developers/agents/mcp/getting-started">MCP server overview - Airtable Developers</a></li>

</ul>
</details>

**Tags**: `#mcp`, `#airtable`, `#developer-tooling`, `#vscode-extension`, `#open-source`

---

<a id="item-tech-news-8"></a>
### [new-api 1.0.0-rc.48 signs its caches and adds vendors&\#x27; own task API addresses](https://github.com/QuantumNous/new-api/releases/tag/v1.0.0-rc.48) ⭐️ 5.0/10

new-api, an open-source program that people run on their own servers to pass requests between their apps and AI vendors, published version 1.0.0-rc.48 on November 4, 2026 — an &quot;rc&quot; \(release candidate\) is a test build that comes before a final 1.0 release. Its headline change is a security fix: the user, token and session records it keeps in Redis \(a fast in-memory store used so the server does not have to look everything up in its main database each time\) are now signed, and any entry that was altered, lacks a signature, or has expired is re-read from the database. Operators running new-api on more than one server must upgrade every server together, because a new node that meets a cache entry written by an older version falls back to the database. The release also lets its task plugins — the ones that drive video and other long-running generation jobs — be called at the vendors&\#x27; own API addresses, such as Kling&\#x27;s /v1/videos/text2video and Vidu&\#x27;s /ent/v2/text2video, while the older prefixed addresses keep working, and it adds a &quot;price needs attention&quot; flag in the pricing page for task models that can no longer be charged correctly.

github · Calcium-Ion · Nov 4, 15:40

**「Background」** new-api is an open-source, self-hosted gateway: operators run it on their own servers so applications can reach many AI providers through one address and one billing setup. This v1.0.0-rc.48 build is a release candidate — a preview of the upcoming 1.0 release that is meant for testing before the final version. Its changes therefore matter mainly to the administrators who deploy and upgrade the gateway, not to end users of the AI products it connects to.

**「What to do if you run it」** For anyone operating a new-api server, the practical sequence is to upgrade all nodes in one go rather than one at a time; otherwise the upgraded nodes keep falling back to database reads \(slower, more load\) until the rest catch up. A second thing to check: requests sent to Kling, Vidu, MiniMax and Volcengine Ark at those new native addresses are rejected if they carry a callback\_url \(the field that asks the vendor to notify a web address when a job finishes\), so scripts or apps that rely on callbacks with those four vendors need adjusting. Task plugins otherwise pass native requests through exactly as the client wrote them and return the vendor&\#x27;s own response format and error codes.

**Tags**: `#api-relay`, `#self-hosted`, `#release-notes`, `#coding-tooling`, `#security`

---

<a id="item-tech-news-9"></a>
### [OpenAI says its AI pipeline found 948 Linux root-escalation exploits](https://openai.com/index/a-thousand-fewer-paths-to-root/) ⭐️ 5.0/10

OpenAI&\#x27;s cybersecurity team says an automated pipeline of its own, run against the Linux kernel in October 2026, reproduced 1,724 known vulnerabilities and generated 948 working exploits that let an ordinary local user take root — full administrative control of the machine. It also produced 291 proof-of-concept programs that leak information. The team put the total API \(programmatic access to its models\) bill at $1,213,430, or about $1,279 per working exploit, and roughly $359 counting only the runs that paid off; it says outside experts confirmed at least 10 of the exploitation techniques as new. The write-up ships no model version, tooling, or reproducible data, so the numbers are OpenAI&\#x27;s own account rather than an independently checked result.

hackernews · dangelosaurus · Nov 4, 23:33 · [Discussion](https://news.ycombinator.com/item?id=50372929)

**「Background」** The Linux kernel is the core of the operating system that manages memory, hardware, and who is allowed to do what. A privilege-escalation flaw lets an ordinary user break past those permission limits and gain administrator, or “root,” control of the machine.

**「What this means if you run Linux」** For anyone running Linux machines, nothing changes yet: OpenAI says its pipeline generated patches for the 948 flaws, but there is no indication those patches have been accepted into Linux or shipped in an update you can install, so there is no new fix to apply today. The write-up also gives no breakdown of which parts of the kernel are affected, which means an administrator cannot tell whether their servers or devices are among the exposed ones or prioritize anything. And at roughly $1.2 million in API costs \(paying per use of the model\) for a single run, this is not a check an ordinary security team can reproduce on its own code.

**「What readers pushed back on」** The most common request in the Hacker News thread was detail OpenAI did not publish: which parts of the kernel were affected, how old the vulnerable code is, and what kinds of bugs these are \(memory corruption, logic errors, race conditions\), since without that it is hard to judge whether the method would work on another codebase. One commenter doubted that 948 exploits represent 948 separate problems, comparing it to counting thousands of ways to attack a database through one SQL injection flaw; another asked whether the real lesson is that the kernel is too complex to secure patch by patch. A commenter identifying as a member of the team offered to answer questions.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/openai-ai-pipeline-generates-948-linux.html">OpenAI AI Pipeline Generates 948 Linux Root Escalation ...</a></li>
<li><a href="https://openai.com/index/a-thousand-fewer-paths-to-root/">A thousand fewer paths to root - OpenAI</a></li>

</ul>
</details>

**Tags**: `#AI security research`, `#OpenAI`, `#autonomous agents`, `#Linux kernel`, `#capability claims`

---

<a id="item-tech-news-10"></a>
### [Hugging Face announces on-device Phonon text-to-speech model, claiming top benchmarks](https://huggingface.co/blog/phonon-tts) ⭐️ 5.0/10

Hugging Face has announced Phonon TTS, a text-to-speech model \(software that turns written text into spoken audio\). It says the model runs on-device—locally on a phone or computer rather than on a company&\#x27;s servers—and claims it tops speech benchmarks \(standard tests used to compare model quality\). The supplied blog post gives no model size, licensing terms, hardware requirements, availability date, startup delay, or named benchmark results, so neither the local-running claim nor the benchmark lead can be checked. That would matter to people who want devices to read text aloud without an internet connection, but no downloadable release is confirmed in the supplied material.

rss · Hugging Face Blog · Nov 5, 00:00

**「What Phonon is」** Text-to-speech software turns written text into spoken audio. Most such systems run on a company&\#x27;s servers, so the text has to be sent over the internet; &quot;on-device&quot; means the model runs on the user&\#x27;s own phone, laptop, or browser instead. The Hugging Face post says Phonon was opened up two weeks earlier as a small model that needs no server and no network, and the model&\#x27;s documentation describes it as part of a family of on-device speech models trained with the recipe of an earlier model called Pocket TTS. A separate project page lists a 31-million-parameter version \(parameter count is a rough measure of model size\) that downloads about 44 MB of model files and a voice into a web browser on first use.

**「What this means if you build voice features」** For teams adding a voice to an app, the practical shift is that speech synthesis can live on the device instead of in a paid cloud service: Phonon is reported as a roughly 31-million-parameter model released under Apache 2.0, a license that permits commercial use, and Gradium describes it as designed to run without a network connection, with vendor claims of leading CPU latency for streaming \(audio that starts playing before the whole sentence is finished\). Before committing, test it on your own sentences rather than trusting the leaderboard: a third-party writeup notes that the short benchmark sentences differ from real product text, so intelligibility scores are only a shortlist. Also confirm what is actually downloadable, since the announcement itself supplied no parameter count, license, weights availability or hardware requirements, and one earlier product page listed a different size of about 100 million parameters.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/docs/transformers/v5.22.1/model_doc/gradium_phonon_tts">Gradium Phonon TTS - Hugging Face</a></li>
<li><a href="https://github.com/huggingface/blog/blob/main/phonon-tts.md">blog/phonon-tts.md at main · huggingface/blog · GitHub</a></li>
<li><a href="https://github.com/blixt/phonon">GitHub - blixt/phonon: Phonon 31M text-to-speech on WebGPU ...</a></li>
<li><a href="https://lancartech.co.id/en/blog/phonon-tts-on-device-memilih-lisensi-dan-runtime">Phonon On-Device TTS: Picking a License, a Runtime, and a ...</a></li>
<li><a href="https://gradium.ai/content/gradium-phonon-on-device-tts">Gradium Phonon: On-Device Text-to-Speech | Gradium</a></li>
<li><a href="https://www.marktechpost.com/2026/10/22/gradium-phonon-31m-on-device-tts/">Gradium Open-Sources Phonon, a 31M-Parameter On-Device TTS ...</a></li>

</ul>
</details>

**Tags**: `#TTS`, `#on-device AI`, `#open-weight models`, `#Hugging Face`, `#benchmarks`

---

<a id="item-tech-news-11"></a>
### [Dharma Field Extractor claims to turn any document into structured JSON](https://huggingface.co/blog/Dharma-AI/dharma-field-extractor) ⭐️ 5.0/10

A Hugging Face blog post announces a tool called Dharma Field Extractor, which it describes as taking any document as input and returning structured fields as JSON — a plain-text format that labels each piece of data so software can read it field by field, such as pulling a date, an amount and a name out of an invoice. The posting is only a title and link at this stage: the available listing includes no model name or size, no accuracy results, no pricing, no installation instructions, and no evidence that a working version can be downloaded and run. Readers should treat it as an announcement of intent rather than a verified, usable product until the post itself or a public model page supplies those details.

rss · Hugging Face Blog · Nov 4, 17:50

**「Background」** Document extraction means taking a scan or photo of a form, invoice, or report and pulling out individual pieces of information — a date, a total, a name — instead of leaving them locked in the image. Dharma says its Field Extractor does this with a 2-billion-parameter model \(parameters are the internal settings that shape a model&\#x27;s behavior\) built on its earlier DharmaOCR-LITE v1.1 document reader, and it returns the results as JSON, a standard text format that pairs each label with its value.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/Dharma-AI/dharma-field-extractor">Dharma Field Extractor: Any Document In, Structured Fields in ...</a></li>
<li><a href="https://huggingface.blog/blog/dharma-ai-dharma-field-extractor/">Schema-First Document Extraction Needs More Than Valid JSON</a></li>

</ul>
</details>

**Tags**: `#document extraction`, `#structured output`, `#JSON`, `#Hugging Face`, `#AI tooling`

---

<a id="item-tech-news-12"></a>
### [PiPedal Turns a Raspberry Pi Into a Guitar Effects Rig](https://hackaday.com/2026/11/04/pipedal-grants-guitar-effects-amp-emulation-and-more/) ⭐️ 5.0/10

PiPedal is an open-source project that turns a Raspberry Pi—a small, inexpensive computer—into a guitar effects and amplifier simulator, with settings controlled from a phone or web browser. Hackaday highlighted the project and pointed readers to its code and documentation; this is not a new product release, and the article gives no version number, price, or step-by-step setup. It is aimed at guitarists and hobbyists who already have a Raspberry Pi or a similar small Linux computer.

rss · Hackaday · Nov 5, 06:00

**「Background」** Amp emulation means software imitating the sound of a physical guitar amplifier rather than buying one; Neural Amp Modeler is a widely used tool for this that builds a &quot;profile&quot; describing how a particular real amp responds. PiPedal 2.0 added support for that tool&\#x27;s newer A2 profiles, which the project says are more accurate while using less processing power. The project&\#x27;s documentation lists Raspberry Pi OS \(Bookworm or Trixie\) or Ubuntu 24.x and later as supported, and warns Ubuntu users to set up a real-time-capable kernel — a system tuned so audio does not stutter.

**「What it means in practice」** A guitarist with a Raspberry Pi can experiment with many pedal and amplifier sounds without buying each physical unit, but the excerpt provides no setup instructions or independent sound-quality tests, so it should not be treated as a guaranteed plug-and-play replacement for real equipment.

<details><summary>References</summary>
<ul>
<li><a href="https://rerdavies.github.io/pipedal/">PiPedal | PiPedal guitar effects pedal for Raspberry Pi.</a></li>
<li><a href="https://rerdavies.github.io/pipedal/PiPedal2.html">PiPedal | PiPedal guitar effects pedal for Raspberry Pi.</a></li>

</ul>
</details>

**Tags**: `#raspberry-pi`, `#guitar-effects`, `#amp-emulation`, `#audio`, `#hardware`

---

<a id="item-tech-news-13"></a>
### [Lumio 1.4 adds Qwen Code and Cline to MacBook-notch AI agent monitor](https://habr.com/ru/articles/1103620/?utm_campaign=1103620&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

The developers of Lumio, a free Mac app that sits in the MacBook notch \(the cutout at the top of the screen\), have released version 1.4 with support for two more AI coding agents \(programs that can write and run code on a user&\#x27;s behalf\): Qwen Code and Cline. They join Claude Code, Codex, Cursor and others already supported. According to the release note, the app shows which agent sessions are working and which are waiting for the user, and lets the user approve a command with one click from the notch. It also shows each session as a person at a desk in a pixel-art office; the note gives no install instructions, repository link, or further detail on how approval works.

rss · Habr AI · Nov 5, 10:35

**「Context」** Coding agents such as Claude Code, Codex and Cursor are programs that carry out programming tasks on their own, but they routinely stop and ask the user for permission before running a command or changing files. Recent MacBooks have a black camera cutout at the top of the screen — the &quot;notch&quot; — that apps can draw small status displays into, which is where Lumio puts its agent list. Lumio already monitored several of these agents before version 1.4; this release widens the list rather than introducing the concept.

**「What changes for users」** People who already run Qwen Code or Cline on a Mac can now see those sessions and approve a waiting command from Lumio&\#x27;s MacBook notch \(the black cutout at the top of the screen\), alongside Claude Code and Codex. The practical limit is that Lumio is a free macOS-only monitoring layer for a MacBook with a notch, not a coding agent itself, so it changes nothing for Windows or Linux users or for agents it does not support.

<details><summary>References</summary>
<ul>
<li><a href="https://lumiomac.com/">Lumio for Mac: your AI agents, in the notch</a></li>
<li><a href="https://www.youtube.com/shorts/TxF-wLDpLQg">My AI agents got an office · Lumio 1.4 #shorts - YouTube AI coding agents, right in the MacBook notch — Lumio Lumio — your AI agents, in the Mac notch - YouTube GitHub - shixiaoke1004-cmyk/Lumio: Turn your MacBook&#x27;s notch ... Lumio — your Claude Code &amp; Codex agents, in the MacBook notch</a></li>

</ul>
</details>

**Tags**: `#AI coding agents`, `#macOS app`, `#developer tooling`, `#Lumio`, `#Qwen Code`

---

<a id="item-tech-news-14"></a>
### [Home assistant project reports gains from training on its own history](https://habr.com/ru/articles/1103860/?utm_campaign=1103860&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A home-hosted personal assistant project reports that it collected enough of its own conversation examples to continue training the AI model that generates its replies, using LoRA \(a low-cost method that adds a small adapter instead of retraining the whole model\). In part four of the series, the author says the assistant moved to new hardware and a newer language model, and that training on the assistant&\#x27;s history improved two test scores: IFEval, which measures instruction-following, rose 2%, and LogiQA, a reasoning test, rose 12%. The post also claims the assistant could run for 100 steps without losing its goal and, in a practical test, reprogrammed its own system into voice input and output in 73 minutes. These are project claims, not independently verified results; the excerpt names no base model, code, configuration or cost.

rss · Habr AI · Nov 5, 10:03

**「Context」** This is the fourth installment in a series about a personal AI assistant running on home hardware; the first part described an assistant built on two 12 GB consumer graphics cards that combined a language model with document lookup, a structured memory store, external tools, and voice input and output. This part relies on LoRA \(low-rank adaptation\), a way of teaching an existing model a new behavior by training a small add-on set of parameters rather than retraining the whole model, plus supervised fine-tuning, which means continuing training on a curated set of example conversations.

**「What it means in practice」** For someone running a similar self-hosted assistant, the practical consequence is that this is not a reproducible recipe: it reports claimed improvements but gives no base model name, training code, data format, hardware specifications or cost, so the setup cannot be copied from the post alone.

<details><summary>References</summary>
<ul>
<li><a href="https://habr.com/ru/articles/1083752/">Как я создавал персонального ассистента на домашнем железе</a></li>

</ul>
</details>

**Tags**: `#LoRA`, `#fine-tuning`, `#local LLM`, `#personal assistant`, `#self-hosted AI`

---

<a id="item-tech-news-15"></a>
### [A 15-Hour Claude Suspension Shows the Risk of One-Vendor AI Reliance](https://habr.com/ru/articles/1103470/?utm_campaign=1103470&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr commentary reports that fintech company Belo had Claude \(an AI assistant made by Anthropic\) suspended for more than 60 employees for about 15 hours in April 2026. The notice cited a rules violation without details and offered an appeal form; access was later restored and the suspension was described as probably a false alarm. Belo had access to Google&\#x27;s Gemini as an alternative, but the article says switching was not quick because of accumulated history, familiar tools and integrations. The piece uses the episode to argue that businesses are becoming dangerously dependent on AI suppliers, while acknowledging that its account rests on public statements and journalism rather than an independent investigation.

rss · Habr AI · Nov 5, 07:11

**「What Claude access means here」** Claude is a commercial AI assistant that a company uses online rather than installing and running on its own computers. The article is an opinion essay built around one reported incident, and its broader concern is dependency: when AI tools handle support, accounting, sales and coding work, losing access can stop normal operations rather than merely inconvenience a few employees.

**「What It Means in Practice」** For a team that uses an AI assistant for daily work, the concrete risk is that work can stop even when a second AI service is already available. Belo&\#x27;s case suggests keeping copies of important conversation histories and knowing which internal tools would need to be reconnected, rather than assuming a backup account is enough.

**Tags**: `#Claude`, `#account suspensions`, `#AI dependency`, `#vendor lock-in`, `#access restrictions`

---

<a id="item-tech-news-16"></a>
### [Pepper-Orchestrator Add-On Splits Multi-Module Coding Work Across AI Agents](https://habr.com/ru/articles/1103656/?utm_campaign=1103656&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr article describes pepper-orchestrator, an add-on for the AI coding assistants Claude Code and Codex. It turns a goal that spans several parts of a project&\#x27;s code, or several repositories \(storage locations for code\), into work packages that different AI agents \(software that carries out tasks on its own\) run in parallel, with each claimed completion checked separately. The excerpt provides no version, price, installation steps, or details that would let someone repeat the demonstrated case, so the add-on&\#x27;s practical availability and reliability are unverified.

rss · Habr AI · Nov 4, 21:50

**「Background」** Claude Code and Codex are AI coding assistants that can read, edit, and run code on a developer&\#x27;s behalf. A model&\#x27;s context window is the amount of code, instructions, and earlier messages it can keep in view at once; when a change spans several modules or repositories, that working set can outgrow a single session. Splitting the job among several agents keeps each part small, but the parts still have to be coordinated and checked so their results fit together.

**Tags**: `#Claude Code`, `#Codex`, `#AI agents`, `#orchestration`, `#developer tooling`

---

<a id="item-tech-news-17"></a>
### [Habr Post Argues Coding-Agent Context Should Live in the Project Files, Not Chat](https://habr.com/ru/articles/1103614/?utm_campaign=1103614&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr post by the author RouR pushes back on a recent write-up about moving from Claude Code to Codex \(two AI coding assistants that read and edit files on command\) while carrying project history across. The author disagrees with archiving old conversations, arguing that a chat log records the discussion about a project rather than the decisions that came out of it, so the working context — the background information handed to the assistant — should sit in the project&\#x27;s repository instead. He says this has been his own setup for six months, under a personal method he calls GRACE that he has since turned into a small utility named \`doubled-graph\`. The published text is only an introduction: it contains no setup steps, code, configuration, or evidence that the utility works, and there are no comments on the post.

rss · Habr AI · Nov 4, 17:55

**「Background」** Coding agents — AI tools that write and edit software on request — normally keep a project&\#x27;s thread inside the chat: instructions, decisions and file layout all pile up in the conversation, and the thread is lost or stranded when you switch tools. This post answers an earlier Habr write-up about moving from Claude Code to Codex and preserving project history as chat archives, arguing the real decisions belong in files stored next to the code. The approach it points to, GRACE, is described in a separate write-up as five context files plus a module graph placed inside the code repository \(the shared project folder that also tracks every change\), together with a small utility called doubled-graph meant to read that material back.

<details><summary>References</summary>
<ul>
<li><a href="https://ai-manual.ru/article/kontekst-proekta-v-repozitorii-a-ne-v-chate-kak-ustroenyi-metodika-grace-i-utilita-doubled-graph/">Контекст проекта в репозитории , а не в чате: как... | AiManual</a></li>

</ul>
</details>

**Tags**: `#coding agents`, `#context management`, `#Claude Code`, `#Codex`, `#developer workflow`

---

<a id="item-tech-news-18"></a>
### [Customs Clerk Builds ESP32 Noise and Occupancy Monitor for Rental Apartments Using AI](https://habr.com/ru/articles/1103842/?utm_campaign=1103842&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

An author who describes himself as a customs declarant has published a build report on Habr for a homemade monitoring device for short-term rental apartments. It measures loudness in dBA \(decibels adjusted to how the human ear perceives loudness\), uses a 24 GHz radar sensor to detect whether anyone is inside, and sends a push notification to the owner&\#x27;s phone when guests arrive or noise spikes. The device runs on an ESP32 \(a cheap, matchbox-sized microcontroller board with built-in Wi-Fi\), reports over MQTT with TLS encryption \(a lightweight messaging format used by connected devices, wrapped in encryption\), and is backed by a Node.js server, a PostgreSQL database and a PWA \(a website that can be installed and behaves like an app\). The author says the circuit board was generated by code in KiCad \(free software for designing circuit boards\), that the project went through three hardware revisions, that two units had to be pulled back from properties, and that no line of code was written by hand — though the post itself is only a teaser and names no AI models, parts list, source code or installation steps.

rss · Habr DIY · Nov 5, 09:47

**「Background」** The ESP32 is an inexpensive microcontroller board with built-in Wi-Fi, commonly used by hobbyists to connect sensors to home networks. A 24 GHz radar sensor is a small radio module that detects a person&\#x27;s presence or motion without using a camera; such modules are often paired with ESP32 boards in do-it-yourself occupancy-sensing projects, including lights that stay on when someone is sitting still.

**「What it means in practice」** For someone who rents out a flat, the post outlines a cheap owner-side monitor but does not give enough to copy it: without a parts list, wiring, firmware or the prompts used, a reader cannot rebuild the device. The author&\#x27;s own account of two recalls and three revisions also suggests the hardware was not dependable on the first attempt, so the claim that AI produced the code and the board covers the software work, not the physical testing.

<details><summary>References</summary>
<ul>
<li><a href="https://shillehtek.com/blogs/news/esp32-ld2410-smart-light-presence-sensing">ESP 32 HLK-LD2410: Smart light with presence sensing | ShillehTek</a></li>

</ul>
</details>

**Tags**: `#ESP32`, `#24GHz radar`, `#AI-assisted hardware`, `#KiCad`, `#home automation`

---

<a id="item-tech-news-19"></a>
### [DIY controller lets you program it on a tiny screen with three buttons](https://habr.com/ru/articles/1103650/?utm_campaign=1103650&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A maker writing on the Russian site Habr built a small programmable controller around the ESP8266, a cheap Wi-Fi-capable microcontroller chip, and made it programmable on the device itself. Programs are written in Ladder Diagram, the graphical logic style industrial electricians use — drawn as rungs of contacts and coils rather than lines of text — and edited on a 0.96-inch OLED screen using only three buttons. While the program runs, the same diagram shows what is happening in the process: which contacts are closed, what values the inputs hold, and which outputs are switched on. No computer is needed at any point. The post is a build log; the supplied excerpt contains no source code, parts list, or step-by-step instructions, so the details cannot be checked or reproduced from what is available here.

rss · Habr DIY · Nov 5, 08:03

**「Background」** A PLC, or programmable logic controller, is the small industrial computer that runs automation inside machines and factory equipment; it is normally programmed from a laptop and then runs the logic on its own. The ESP8266 is a low-cost microcontroller, meaning a tiny computer on a single chip, with built-in Wi-Fi and a large hobbyist following. Ladder Diagram is a visual programming language drawn as electrical switches and outputs, so the logic looks much like a circuit diagram rather than lines of code.

**「Why it matters in practice」** For people who tinker with home automation or small machines, this points to a controller that can be rewired and debugged standing at the panel, without carrying a laptop over. The trade-off is the interface: three buttons and a screen smaller than a matchbook make entering even a modest program slow, so this suits small logic — a pump, a gate, a few sensors — rather than anything elaborate. Anyone hoping to copy the project would need the wiring and code, which this post&\#x27;s excerpt does not provide.

**Tags**: `#ESP8266`, `#Ladder Diagram`, `#PLC`, `#embedded hardware`, `#DIY controller`

---

<a id="item-tech-news-20"></a>
### [Xiaomi begins youth-apartment trial of Xiaomi-Robotics-1 robot system](https://weibo.com/1749127163/5361796274981767) ⭐️ 5.0/10

Xiaomi has begun a closed trial of a robot agent system—software that can plan and carry out steps toward a goal with limited human direction—in its youth apartments. The system is built on Xiaomi-Robotics-1, which Xiaomi calls an embodied base model: an AI model meant to control a physical robot rather than only produce text or images. Xiaomi says the robot can tidy desks, sweep trash, sort and put items back, inspect rooms, and recheck the home, and that one validation run lasted more than 30 minutes, covered three rooms, and involved more than 50 tasks. The trial is closed, and Xiaomi has not released code, pricing, a parts list, or a date for wider availability.

telegram · zaihuapd · Nov 5, 08:19

**「Context」** Xiaomi-Robotics-1 is a general-purpose “embodied” model: software trained to turn sensor input into physical actions, rather than only text or images. Xiaomi released the model publicly in August 2026, with reports at the time describing it as trained on 100,000 hours of data. In the apartment trial, it runs inside an agent loop—the system collects data, chooses an action, and executes it—so it can plan a sequence of household tasks instead of performing one fixed motion.

**「What this means」** The practical effect is limited to people in those apartments: a robot may take on routine tidying and inspection, but Xiaomi has not said how residents request tasks, how the robot behaves around people, or what happens if it fails. For everyone else there is no product to buy, install, or plan around yet.

<details><summary>References</summary>
<ul>
<li><a href="https://m.ithome.com/html/985985.htm">小 米 具 身 基 座 模 型 Xiaomi - Robotics - 1 正式开源 - IT之家</a></li>
<li><a href="https://auto.news18a.com/news/storys_283840.html">小 米 开源 Xiaomi - Robotics - 1 具 身 基 座 模 型 ：10...</a></li>

</ul>
</details>

**Tags**: `#小米机器人`, `#具身智能`, `#Agent系统`, `#Xiaomi-Robotics-1`, `#机器人试运营`

---

<a id="item-tech-news-21"></a>
### [Huawei Cloud to launch openPangu-2.1-Pro on Nov 15, targeting HarmonyOS code](https://m.gelonghui.com/live/2748413) ⭐️ 5.0/10

Huawei Cloud plans to put a new flagship model, openPangu-2.1-Pro, on its MaaS platform on November 15, according to market reports cited by Chinese outlet Gelonghui; the report says existing customers were told by text message. MaaS \(model-as-a-service\) means renting access to an AI model hosted in the cloud rather than running it yourself. The version is described as improving the quality of code it writes in ArkTS, the programming language used to build native apps for HarmonyOS, Huawei&\#x27;s device operating system, and the same model is to be wired into three Huawei Cloud products: the agent-building platform AgentArts, the coding tool CodeArts, and the office suite OfficeAce. The report gives no price, no benchmark results and no access terms, and despite the &quot;open&quot; in the name it offers no evidence that the model&\#x27;s underlying weights will be published; it also says earlier reports that Huawei Cloud had stopped selling the Pangu model line entirely were a misreading.

telegram · zaihuapd · Nov 5, 13:27

**「Background」** Huawei Cloud sells access to AI models through a model-as-a-service \(MaaS\) setup: developers call the model over Huawei&\#x27;s cloud instead of installing and running it on their own machines. Pangu is Huawei&\#x27;s own family of large language models. ArkTS is the programming language for apps built natively for HarmonyOS, Huawei&\#x27;s device operating system, so a model tuned for ArkTS is aimed at generating code for that specific kind of app.

**「Who needs to act」** The people most affected are developers building native HarmonyOS apps in ArkTS, Huawei&\#x27;s programming language for those apps: the new version is specifically pitched at producing better ArkTS code, so code suggestions in Huawei&\#x27;s tools should need less fixing. Teams already running the earlier openPangu-2.0-Flash or 2.0-Pro model services on Huawei Cloud should plan a switch, since Huawei Cloud issued a retirement notice for those two services on November 2, ahead of the November 15 replacement. The notice gave no pricing, usage limits or access details, so confirm cost and quota with Huawei Cloud before moving production work onto it.

<details><summary>References</summary>
<ul>
<li><a href="https://t.me/linux_do_channel/553819">LINUX DO Channel – Telegram</a></li>

</ul>
</details>

**Tags**: `#Huawei Cloud`, `#openPangu`, `#model release`, `#ArkTS`, `#HarmonyOS`

---

<a id="item-tech-news-22"></a>
### [agents-scaffold bundles Claude Code, Codex and Antigravity with project presets](https://github.com/LeeYudok/agents-scaffold) ⭐️ 5.0/10

A Telegram post announced a GitHub project called agents-scaffold, which it says works with three AI coding agents \(software that writes and edits code on a user&\#x27;s behalf\): Claude Code, Codex and Antigravity. The post says the project also ships presets — ready-made configuration templates — for development stacks such as Next.js, Spring Boot and Python, so a new project can be set up quickly. It presents this as a move toward combining AI coding agents that have so far been used one at a time. The post itself supplies no installation steps, usage examples or evidence that the tool works as described; its only pointers are two Telegram links, so the capability should be treated as announced rather than demonstrated.

telegram · aipluscn · Nov 5, 01:47

**「Background」** AI coding agents are assistants that can open a project, change files and run commands on a developer&\#x27;s behalf; Claude Code, Codex and Antigravity are three such tools. The post describes these agents as mostly separate tools, each set up on its own. A scaffold is a starter kit — project files and preset settings — and this one is presented as a single setup covering several agents and common project types \(Next.js for websites, Spring Boot for Java server applications, and Python\).

**「What it would change in practice」** If the project works as described, someone who uses more than one of these coding agents could keep a single set of project rules and stack settings instead of repeating the setup for each agent separately. Because the announcement does not document what the presets contain or which versions of the agents they target, anyone interested should open the repository and check compatibility before relying on it.

**Tags**: `#AI coding agents`, `#developer tooling`, `#GitHub project`, `#Claude Code`, `#Codex`

---

<a id="item-tech-news-23"></a>
### [Isle post claims AI usage stats and per-assistant permissions](https://github.com/galyarderlabs/isle) ⭐️ 5.0/10

The makers of Isle, a desktop program that puts several AI assistants in one place, say they have added usage statistics for Claude and ChatGPT subscription plans and controls over what each AI agent—software that can carry out tasks, not just chat—is allowed to do. The post says the tool supports agents such as Claude Code, Codex and Hermes, and connects to outside tools and data through MCP servers \(add-ons that let AI assistants use other services\). It gives no version number, no explanation of how the usage figures are collected or exactly what they show, and no independent evidence; it also directs readers to additional Telegram channels. The post&\#x27;s title also mentions ORQST, but the text does not say what ORQST is.

telegram · aipluscn · Nov 5, 01:48

**「Background」** MCP, short for Model Context Protocol, is a shared convention that lets an AI assistant plug into outside tools and data — files, calendars, code repositories — through one common connector instead of a bespoke integration for each one. Isle, according to its GitHub page, is a &quot;living desktop notch&quot; for the GNOME Linux desktop: a strip that stays on screen and gathers AI agents, personal tools, and MCP connections in one place. That setup is what makes the usage figures and permission settings described in the Telegram post relevant to the same product.

**「What changes in practice」** For someone running several AI coding assistants on one machine, the practical change is that plan-usage checks and agent permission settings would sit in the same desktop window instead of separate dashboards and configuration screens. Before relying on it for team or quota control, verify where the usage numbers come from and whether the permission rules cover every supported agent, since the post does not describe either.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/galyarderlabs/isle">GitHub - galyarderlabs/isle: Independent GNOME top-bar island ...</a></li>
<li><a href="https://neuralcoretech.com/agentic-ai-model-context-protocol-mcp-architecture-2026/">Agentic AI and Model Context Protocol (MCP): Architecture ...</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#AI agents`, `#developer tooling`, `#usage tracking`, `#Claude Code`

---

<a id="item-tech-news-24"></a>
### [AI 代理工具库 DmitriyYukhanov/agent-plugins 发布，是 AI 工具集成化趋势的信号](https://github.com/DmitriyYukhanov/agent-plugins) ⭐️ 5.0/10

A Telegram post announcing the open-source agent-plugins collection of skills for Claude Code, Codex and Copilot, framed as a sign of AI tool consolidation but with no concrete capability, install detail or evidence provided.

telegram · aipluscn · Nov 5, 03:20

**Tags**: `#AI agent plugins`, `#Claude Code`, `#Codex`, `#developer tooling`, `#open-source`

---

<a id="item-tech-news-25"></a>
### [MaccyPlus gives AI agents a command line into macOS clipboard history](https://github.com/roypadina/maccyplus) ⭐️ 5.0/10

MaccyPlus is a new macOS clipboard-history tool — it keeps a record of the text and images you copy so you can find them again — and it adds a command-line interface so other software, including AI agents, can read and write that history. A command line is a text-only way to control a program, which makes it easy for another program to drive it. Alongside the interface it lists rule matching, automatic actions, keyboard shortcuts and plugins, and it installs through Homebrew \(a command-line app store for Macs\) with the command &quot;brew install --cask roypadina/tap/maccyplus&quot;. It requires macOS 14 Sonoma or later and runs on both Apple Silicon and Intel Macs. The post itself is mostly trend commentary: it gives no command examples, no demo and no evidence that an agent-driven workflow actually works, and it sends readers to Telegram posts for the setup steps.

telegram · aipluscn · Nov 5, 03:20

**「Background」** Clipboard managers are small utilities that keep a searchable history of everything you copy, so you can retrieve an earlier item instead of only the most recent one. MaccyPlus is a free, open-source offshoot of Maccy, an existing clipboard manager for macOS; its addition is automation — rules that recognize what you copied \(a web address, an email, an issue number\) and offer actions such as opening it in another app or transforming the text.

**「What it means if you try it」** A clipboard history holds everything a person has copied, including passwords and private text, so once this interface is available any program or script running on that Mac can read the whole record, not just what is currently copied. Before MaccyPlus can paste into the app you are working in, macOS requires you to grant it the Accessibility permission, a privacy setting that lets one program control others. Macs still on macOS 13 or earlier cannot run it.

<details><summary>References</summary>
<ul>
<li><a href="https://alternativeto.net/software/maccyplus/about/">MaccyPlus : Maccy clipboard manager plus rules... | AlternativeTo</a></li>

</ul>
</details>

**Tags**: `#macOS clipboard tool`, `#AI agent tooling`, `#CLI integration`, `#Homebrew`, `#developer tooling`

---

<a id="item-tech-news-26"></a>
### [NVIDIA Announces OpenShell With Separate Permissions for AI Agents](https://telegram.me/aipluscn/3603) ⭐️ 5.0/10

NVIDIA has announced OpenShell, an open-source project \(its underlying code is meant to be publicly available for inspection and reuse\) intended to give AI agents a safer place to run. AI agents are programs that can carry out multi-step tasks, such as running commands or editing files, on a user&\#x27;s behalf. OpenShell would let users set permissions for each agent separately, for example allowing it to read GitHub&\#x27;s API \(the interface programs use to access GitHub data\) but not post to GitHub. The post says it supports Claude Code, Codex, OpenCode, and GitHub Copilot CLI and uses changes to the operating system kernel \(its core layer\) plus formal verification \(a mathematical check that software behaves as specified\) to control agent behavior. But the post provides no repository link, installation steps, version number, or independent evidence, so this is an announcement rather than something readers can verify or use today.

telegram · aipluscn · Nov 5, 04:08

**「What an agent runtime does」** AI coding agents such as Claude Code and Codex can read files, run commands and call outside services on a person&\#x27;s behalf, so something has to define and enforce what each one is allowed to touch. That job falls to a runtime — the layer that starts and supervises a program while it runs — and often to a sandbox, an isolated box the program is confined to. NVIDIA&\#x27;s own page describes OpenShell as governing agent execution, access and where model requests are processed, and lists Claude Code, Codex, GitHub Copilot CLI, OpenCode and OpenClaw among the agents it supports.

**「What It Means in Practice」** For someone using Claude Code, Codex, OpenCode, or GitHub Copilot CLI, the near-term effect is that there is nothing to install or test from this announcement: it includes no repository link, setup guide, or version number. Until NVIDIA publishes those details, users cannot confirm that the per-agent permission rules work as described or whether OpenShell fits their existing setup.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nvidia.com/en-sg/ai/openshell/">NVIDIA OpenShell | Open , Secure Runtime for AI Agents</a></li>
<li><a href="https://windowsforum.com/news/nvidia-openshell-and-sentry-what-the-open-agent-safety-platform-really-delivers.446321/">NVIDIA OpenShell and Sentry: What the Open Agent Safety Platform...</a></li>

</ul>
</details>

**Tags**: `#NVIDIA OpenShell`, `#AI agent security`, `#coding agents`, `#permissions`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China Blocks SoftBank&\#x27;s $5.4 Billion Acquisition of ABB Robotics Unit](https://www.bloomberg.com/news/articles/2026-11-05/china-blocks-softbank-s-acquisition-of-abb-industrial-robot-unit) ⭐️ 8.0/10

China&\#x27;s foreign investment security review has blocked SoftBank Group&\#x27;s approximately $5.4 billion acquisition of ABB&\#x27;s robotics business, with ABB confirming on Nov. 5 that it was notified the deal may not be implemented in China. The review body&\#x27;s concerns centered on possible transfer abroad of industrial data, supply-chain links and core technology, including for training AI models; China accounts for roughly 30% of ABB&\#x27;s robotics business, according to the report.

telegram · zaihuapd · Nov 5, 10:44

**「Background」** SoftBank agreed in October 2025 to buy ABB’s robotics division for $5.375 billion as part of its AI-robotics strategy, and ABB dropped an earlier plan to spin the unit off as a separately listed company.

**「Impact」** The block leaves SoftBank unable to fold ABB’s China robotics operations—about 30% of that business—into its AI and robotics push, while ABB’s planned sale of the unit cannot proceed in China.

<details><summary>References</summary>
<ul>
<li><a href="https://group.softbank/en/news/press/20251008">Acquisition of ABB Ltd’s Robotics Business | SoftBank Group Corp.</a></li>
<li><a href="https://www.abb.com/global/en/news/129685/abb-to-divest-robotics-division-to-softbank-group">ABB to divest Robotics division to SoftBank Group</a></li>

</ul>
</details>

**Tags**: `#China FDI review`, `#SoftBank`, `#ABB robotics`, `#cross-border M&amp;A`, `#AI and robotics`

---

<a id="item-finance-news-2"></a>
### [Nintendo Switch 2 second-quarter sales fall 41% year over year](https://mp.weixin.qq.com/s/XTw5DXy2CvqFSs4WYx73Xg) ⭐️ 7.0/10

Nintendo said Switch 2 console sales in its fiscal second quarter ended September 30 were 2.67 million units, down 41% from a year earlier and below the previous quarter&\#x27;s 3.82 million. Revenue of ¥448.2 billion and net profit of ¥73.5 billion both came in under market expectations, while the company kept its target of 16.5 million units for the fiscal year ending March 2027.

telegram · zaihuapd · Nov 5, 14:12

**「Background」** Nintendo sold 4.54 million Switch 2 consoles in the same July–September quarter a year earlier, the baseline for the 41% decline.

**「Who pays for it」** The cost pressure has already been passed to buyers: Nintendo raised the Switch 2&\#x27;s US price from $449.99 to $499.99 on 1 September and its Japanese price by ¥10,000, so households buying the console now pay more than at launch.

<details><summary>References</summary>
<ul>
<li><a href="https://tech-insider.org/nintendo-q2-net-profit-falls-29-percent-switch-2-slows-2026/">Nintendo Net Profit Falls 29% as Switch 2 Slows [2026]</a></li>
<li><a href="https://www.cnbc.com/2026/05/08/nintendo-switch-2-price-hike-sales-fall-memory-crunch.html">Nintendo hikes Switch 2 prices and expects console sales to ...</a></li>
<li><a href="https://bitsfrombytes.com/nintendo-switch-2-price-increase/">Nintendo Switch 2 Price Increase: Every Country, Every Date ...</a></li>

</ul>
</details>

**Tags**: `#Nintendo`, `#Switch 2`, `#earnings miss`, `#console sales`, `#memory chip costs`

---