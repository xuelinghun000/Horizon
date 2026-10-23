---
layout: default
title: "Horizon Summary: 2026-10-23 (EN)"
date: 2026-10-23
lang: en
---

> From 138 items, 24 important content pieces were selected

---

**Technology News**
1. [Anthropic ships Claude API version 2026-10-21, removing temperature settings](#item-tech-news-1) ⭐️ 8.0/10
2. [Ollama 0.40.9-rc3 adds Mac speech and d3 decision models](#item-tech-news-2) ⭐️ 7.0/10
3. [Blog shows Codex assistant automating Switch 2 security research](#item-tech-news-3) ⭐️ 7.0/10
4. [CueFlow: an open-source Kanban board for managing AI agent tasks](#item-tech-news-4) ⭐️ 7.0/10
5. [Open-source project boots iOS 16.5 kernel on Android phones and in an emulator](#item-tech-news-5) ⭐️ 6.0/10
6. [Qwen2.5-Coder Fine-Tuned to Imitate Bash, Vim and Tmux](#item-tech-news-6) ⭐️ 6.0/10
7. [Lumio 1.2 puts four AI coding tools in the MacBook notch](#item-tech-news-7) ⭐️ 6.0/10
8. [Open Models&\#x27; 1M Context Is Selective, Sber Article Argues](#item-tech-news-8) ⭐️ 6.0/10
9. [Roundup lists 10 API routers with free or very cheap access to Claude, GPT and other models](#item-tech-news-9) ⭐️ 6.0/10
10. [QA engineer describes linking an AI assistant to wiki, databases and tests via MCP](#item-tech-news-10) ⭐️ 6.0/10
11. [Claude Code Hub v0.9.8 fixes high-severity Node.js security flaw](#item-tech-news-11) ⭐️ 5.0/10
12. [NVIDIA&\#x27;s OpenShell isolates fleets of AI agents in sandboxes](#item-tech-news-12) ⭐️ 5.0/10
13. [AutoHarness: a Claude Code skill that makes AI agents prepare first](#item-tech-news-13) ⭐️ 5.0/10
14. [Developer regains understanding of AI-written pet project with two prompts](#item-tech-news-14) ⭐️ 5.0/10
15. [Qwen More Likely to Alert Authorities Than Western AI Models in SnitchBench Test](#item-tech-news-15) ⭐️ 5.0/10
16. [NLMK IT says one engineer directing AI agents cut a legacy rewrite&\#x27;s effort tenfold](#item-tech-news-16) ⭐️ 5.0/10
17. [A Team Lead&\#x27;s Three-Stage Path Through Six AI Courses From Google, Anthropic and OpenAI](#item-tech-news-17) ⭐️ 5.0/10
18. [Cursor Cancelled a Company’s Pro Subscriptions Over Region Restrictions](#item-tech-news-18) ⭐️ 5.0/10
19. [miHoYo and Tsinghua release GameScaling game-control models](#item-tech-news-19) ⭐️ 5.0/10
20. [Mebular pitches device-local memory for AI agents, without proof it works](#item-tech-news-20) ⭐️ 5.0/10
21. [Open-source mdbook-ai-skill packages mdBook docs as a skill for 33+ AI coding assistants](#item-tech-news-21) ⭐️ 5.0/10

**Financial News**
1. [CSI 300 falls 20% from June high as A-shares near bear market](#item-finance-news-1) ⭐️ 8.0/10
2. [Australian Court Orders Apple to Open iPhone to Third-Party App Stores](#item-finance-news-2) ⭐️ 8.0/10
3. [Report: Banned Nvidia B300 Chips Appear in China State-Linked Deal](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Anthropic ships Claude API version 2026-10-21, removing temperature settings](https://x.com/ClaudeDevs/status/2113013247209021918) ⭐️ 8.0/10

Anthropic released a new dated version of the Claude API, labeled 2026-10-21, which the relayed post describes as the first formal version update since 2023. The new version removes the temperature, top\_p and top\_k settings — knobs that adjust how random or varied a model&\#x27;s wording is — and requests that still include them are rejected with a 400 error, meaning the server refuses the request as invalid. Anthropic&\#x27;s software kits \(SDKs, the code libraries developers use to call the API\) and its \`ant\` command-line tool now default to the new version, and authentication moves to an \`Authorization: Bearer\` header, a standard way of attaching a key to a request. The older 2023-06-01 version is not deprecated and remains available. The details come from a single relayed post citing an Anthropic developer account; no changelog was independently verified here.

telegram · zaihuapd · Oct 22, 03:54

**「Background」** An API is the connection that lets a program send requests to a company&\#x27;s AI model and get answers back. One of the most-used settings in that connection has been &quot;temperature,&quot; a dial that makes replies either more predictable or more varied and creative; top\_p and top\_k are related dials that narrow or widen the pool of words the model picks from. Anthropic labels each version of its API with a date so developers can lock their code to a known behavior, and the 2023-06-01 version has been that default for years.

**「What to do about it」** Anyone whose code sets temperature, top\_p or top\_k will start getting 400 errors once they move to the new version or upgrade to an SDK that defaults to it, so those parameters need to be removed or the request pinned to the 2023-06-01 version string. Teams that call the API through their own HTTP requests rather than the official SDK should also check how they send credentials, since the switch to a Bearer header can break hand-built clients that still use the old header format.

**Tags**: `#claude`, `#anthropic-api`, `#breaking-change`, `#developer-tooling`, `#api-versioning`

---

<a id="item-tech-news-2"></a>
### [Ollama 0.40.9-rc3 adds Mac speech and d3 decision models](https://github.com/ollama/ollama/releases/tag/v0.40.9-rc3) ⭐️ 7.0/10

Ollama published v0.40.9-rc3, a release candidate \(a test build that may still change\) of its software for running AI models on your own computer, on October 22. The build adds speech generation on Macs with Apple Silicon \(Apple&\#x27;s own chips\) through a model called Phonon: the \`ollama run\` command can read text or a chat reply aloud as the audio is generated, and apps can stream audio through an OpenAI-compatible endpoint \(a standard request format that OpenAI-style apps already use\). It also adds the d3 family of decision models in sizes labeled 2B, 4B, 9B, and 27B \(billions of parameters, a rough measure of model size\); these models classify text, structured state, or images, answer yes/no questions, or score options with probabilities. Flint, another model in Ollama&\#x27;s library, now runs on Linux and Windows as well as macOS.

github · github-actions\[bot\] · Oct 22, 01:33

**「Background」** Ollama is software that lets people download and run AI models on their own computer instead of through a company&\#x27;s cloud service. A release candidate such as v0.40.9-rc3 is a test build published before the final version, so its features can still change or fail. Apple Silicon refers to Apple&\#x27;s own M-series chips used in newer Macs, which are designed to run AI workloads locally.

**「What it means in practice」** For people who run Ollama on an Apple Silicon Mac, this build can speak model output aloud locally, and apps built around OpenAI&\#x27;s speech API can use the local server through that endpoint. The speech feature is limited to Apple Silicon, and because this is a release candidate, users who need stable behavior should wait for the final v0.40.9 release.

**Tags**: `#ollama`, `#speech-generation`, `#open-weight-models`, `#local-inference`, `#release-notes`

---

<a id="item-tech-news-3"></a>
### [Blog shows Codex assistant automating Switch 2 security research](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 7.0/10

An October 22 blog post describes using Codex, an AI coding assistant, to automate security research on a Nintendo Switch 2. The setup sends controller inputs through a JetKVM \(a small device that lets one computer control another&\#x27;s keyboard, mouse, and screen\) and reads the console&\#x27;s video output through an HDMI capture feed. A Bluetooth-controlled mechanical switch presses the power button when the console crashes. The post presents this as a way to speed up the search for a jailbreak \(a way around the console&\#x27;s restrictions\), but commenters say it is not yet clear whether the claimed ability to read and modify the console&\#x27;s protected internal files in readable form is real.

hackernews · ledoge · Oct 22, 08:01 · [Discussion](https://news.ycombinator.com/item?id=50192536)

**「What this jailbreak is」** A jailbreak is a way to run software the manufacturer did not authorize — on a game console, typically homebrew programs and copied games. This one, called ns2jb, is described as &quot;software-only&quot; and &quot;tethered&quot;: it requires no hardware modification, but it does not survive a full power-off and has to be re-applied, and it is a &quot;userland&quot; exploit, meaning it works inside the console&\#x27;s ordinary software rather than seizing the system at its deepest level. The writeup says it allows running native code as any ordinary system component, including the built-in file-system component that reads and writes stored data.

**「What it means in practice」** For security researchers, the practical takeaway is that a coding assistant can be wired to real hardware, not just code, but copying the setup requires a JetKVM, an HDMI capture device, and a physical way to press the power button after crashes. The workflow is repeatable only for people willing to assemble the same hardware.

**「What commenters said」** Commenters praised the automation, with hturan saying that if the claim that the console&\#x27;s files can be read and changed is true, Switch 2 game copies could appear within hours and games sold only for the Switch 2 could run on other hardware. rootsudo questioned how the researcher got Codex to cooperate, saying their own attempts to study older Android flaws were refused under a limited access level.

<details><summary>References</summary>
<ul>
<li><a href="https://gbatemp.net/news/switch-2-jailbreak-ns2jb-released-software-only-exploit-tethered.685698/">Switch 2 jailbreak &quot; ns 2 jb &quot; released. Software-only... | GBAtemp.net</a></li>
<li><a href="https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/">pepsipu.com/blog/2026-10- switch 2 - jailbreak - ns 2 jb</a></li>

</ul>
</details>

**Tags**: `#Codex`, `#hardware automation`, `#console jailbreak`, `#KVM`, `#LLM agents`

---

<a id="item-tech-news-4"></a>
### [CueFlow: an open-source Kanban board for managing AI agent tasks](https://github.com/j75689/cueflow) ⭐️ 7.0/10

A developer has published CueFlow on GitHub, an open-source platform you install and run on your own machines to manage work handed to AI agents \(software that carries out multi-step tasks on its own\). Tasks sit on a Kanban board — the to-do / doing / done columns used in project tools — and an agent can pick one up, run it, and then wait for a human to approve the result before it counts as finished. The project also records tool calls and deliverables, keeps an audit log, and exposes REST and MCP endpoints; MCP \(Model Context Protocol\) is a common way to plug AI assistants into outside tools and data, and REST is the standard web interface other software uses to talk to a service. It works with OpenAI-compatible interfaces, Claude Code and Codex, binds to 127.0.0.1 by default \(reachable only from the same computer until you change that\), and can be deployed to cloud environments such as Google Cloud Run. The source post gives no version number, release date, user counts or independent testing, so how mature or widely used the project is remains unverified.

telegram · aipluscn · Oct 22, 13:32

**「Background」** AI agents are programs that can carry out multi-step tasks, including calling other software tools, rather than only answering a single question. Letting several agents work at once creates a supervision problem: someone has to assign tasks, answer their questions, and approve risky actions. CueFlow describes itself as a self-hosted &quot;agent ops console&quot; built for exactly that kind of oversight.

**「What it means in practice」** For teams that want AI agents to do real work but not act unsupervised, this offers a self-hosted way to put a human approval step in front of each task, rather than trusting an agent&\#x27;s output directly. Because it is self-hosted, someone on your side has to run and maintain the server, and the default local-only binding means you must deliberately reconfigure it before colleagues or cloud runners can reach it — a security decision, not just a setup step.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/j75689/cueflow">GitHub - j75689/cueflow: Self-hosted agent ops console: give ...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#agent orchestration`, `#MCP`, `#Claude Code`, `#open-source`

---

<a id="item-tech-news-5"></a>
### [Open-source project boots iOS 16.5 kernel on Android phones and in an emulator](https://github.com/oosexgang/hackios-xnu-kernel) ⭐️ 6.0/10

A GitHub project called hackios-xnu-kernel boots the XNU kernel — the central part of Apple&\#x27;s operating system that manages memory, hardware and running programs — from iOS 16.5 inside QEMU, a free program that imitates other hardware on a normal PC, and on the POCO X5 Pro 5G and some other Xiaomi Android phones. The author describes it as a research bench, not a ROM \(a complete, installable phone system\): a session runs for a fixed number of seconds, then the kernel hands control back to the loader and produces a log. The code is published, so others can download and reproduce it, but it does not produce a working iOS interface, apps or a phone you could use.

hackernews · aghuang · Oct 22, 15:26 · [Discussion](https://news.ycombinator.com/item?id=50196718)

**「Background」** An operating system&\#x27;s kernel is the core layer that talks to the hardware and decides which programs get to run; Apple&\#x27;s is called XNU, and Apple ships it only on its own devices. QEMU is a free program that imitates a whole computer in software, so software written for one machine can be started on another. This project patches Apple&\#x27;s kernel so it can start on hardware Apple never intended, either inside QEMU or directly on a phone.

**「What it means in practice」** Anyone curious can try it on an ordinary computer through QEMU without owning one of the listed phones, but should expect a short boot that ends in a log file rather than a usable device — no touch interface, no App Store, no calls. Because it is not a ROM, there is nothing to install over Android on a daily-use handset, and it does not change what any existing phone can do.

**「What commenters said」** Commenters treated it largely as a curiosity: one speculated that the project is limited to short research sessions because an AI coding assistant would otherwise have refused to continue, and another warned that buyers of used iPhones should check carefully, since replica phones already run modified Android dressed up to look like iOS. A third said the wish to run iOS on other hardware has faded because the system now feels clunky.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/oosexgang/hackios-xnu-kernel">GitHub - oosexgang / hackios - xnu - kernel · GitHub</a></li>
<li><a href="https://hackiosx.dev/">hackiosx: iOS on Android phones</a></li>

</ul>
</details>

**Tags**: `#emulation`, `#iOS`, `#Android`, `#QEMU`, `#XNU kernel`

---

<a id="item-tech-news-6"></a>
### [Qwen2.5-Coder Fine-Tuned to Imitate Bash, Vim and Tmux](https://habr.com/ru/articles/1098116/?utm_campaign=1098116&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A translated post on Habr describes an experiment in which a 360-million-parameter version of the open-weight Qwen2.5-Coder model was fine-tuned—trained further on a specific task—to imitate a terminal. There is no shell \(the program that normally runs terminal commands\) or file system behind it: each keypress goes to the model, which predicts how the screen should change. The author reports training on 336,000 recorded terminal sessions, cutting p95 latency \(the slowest 5% of responses\) on large screen updates from 6.7 seconds to 0.87 seconds on an RTX 4090 graphics card through parallel line decoding, which predicts several lines at once, and scoring 9 out of 13 on a test of reading previously recorded files, versus 2 and 3 for models without the extra training. A quantized version—compressed to 208 MB—is said to run in a browser tab.

rss · Habr AI · Oct 22, 19:12

**「Background」** The project starts from Qwen2.5-Coder-0.5B, a small open-weights coding model — open weights meaning the trained files are published for anyone to download and run — from a family that ranges from 0.5B to 32B parameters, where a parameter is one of the internal numbers that shape how the model behaves. Fine-tuning means continuing to train such a model on a narrower set of examples so it specializes; here those examples were 336,000 recorded terminal sessions. The trick is that nothing is actually executed: the model has learned to guess what a real terminal would show next, the way a text predictor guesses the next word.

**「What it means」** For now this is a demonstration rather than a released terminal you can install: the excerpt gives no repository or setup instructions, so it should not be treated as a drop-in replacement for bash, vim or tmux. What it does show is that a very small model can reproduce familiar terminal screens inside a browser tab, while the real programs and a real shell would still be needed for actual work.

<details><summary>References</summary>
<ul>
<li><a href="https://simedw.com/2026/10/21/world-model-terminal/">WorldTUI: I trained a 360 M model to pretend to be a terminal</a></li>
<li><a href="https://ollama.com/library/qwen2.5-coder">qwen 2 . 5 - coder</a></li>

</ul>
</details>

**Tags**: `#open-weight models`, `#Qwen`, `#fine-tuning`, `#terminal emulation`, `#browser inference`

---

<a id="item-tech-news-7"></a>
### [Lumio 1.2 puts four AI coding tools in the MacBook notch](https://habr.com/ru/articles/1097994/?utm_campaign=1097994&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

The developer of Lumio announced version 1.2 of its free Mac app, which turns the black cutout at the top of newer MacBook screens into a status and control panel for AI coding assistants \(programs that can write and run code for a user\). The developer says the update adds Cursor and GitHub Copilot in VS Code \(a widely used code editor\) to Claude Code and Codex, so all four can be monitored in one place and almost all requests can be answered without opening the editor. The app is a Mac app built around the MacBook notch, and the post gives no system requirements. The announcement also gives no download link, setup steps, or independent evidence of how well it works.

rss · Habr AI · Oct 22, 14:02

**「Background」** The MacBook notch is the black cutout at the top center of newer MacBook screens, normally just housing the camera. AI coding agents are programs that can read and edit code and run commands on a developer&\#x27;s machine, often pausing to ask for permission; keeping track of several at once usually means switching between windows.

**「Impact」** If you run several of these assistants on a notched MacBook, the intended benefit is seeing which one is waiting for approval or has failed without switching windows, and answering from the notch. The practical limit is hardware: the app is built around the MacBook notch, so it is not aimed at older MacBooks or desktop Macs, and the post provides no setup details or independent test results.

**Tags**: `#coding agents`, `#developer tooling`, `#Claude Code`, `#Cursor`, `#macOS app`

---

<a id="item-tech-news-8"></a>
### [Open Models&\#x27; 1M Context Is Selective, Sber Article Argues](https://habr.com/ru/companies/sberbank/articles/1097106/?utm_campaign=1097106&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

An article by Vladimir Lushin on Sber&\#x27;s Habr blog argues that the 1-million-token context headline on several current open-source models \(models whose weights are publicly downloadable\) does not mean the model reads all of that text; context is the text a model can consider at once, and a token is a word piece it counts. He reports that GLM-5.3 selects only 2,048 tokens from history at each step, DeepSeek-V4-Pro uses 1,024 compressed blocks \(shortened summaries of older text\), and Qwen3.8 and Kimi K3 let only every fourth processing layer see the full history; he says some settings came from configuration files and model cards \(vendor summary sheets\), while his conclusions about what the models actually read are his own inference. The article says quality usually breaks around 128,000–256,000 tokens, and that Kimi K3 with history compacted \(summarized to save space\) at 300,000 tokens beat its own full 1-million-token window. For coding agents, it warns that a rule in AGENTS.md \(a file of instructions for the agent\) can quietly stop working by the 100th time the agent uses a tool, and recommends cleaning old tool output, retrieving only relevant text, keeping state outside the context window, repeating rules at the end, and enforcing non-negotiable rules with hooks \(automatic checks\) and permissions.

rss · Habr AI · Oct 22, 12:30

**「Background」** A model&\#x27;s context window is the amount of text it can take in at once, measured in tokens \(pieces of words\). Attention is the mechanism that decides which parts of that text to weigh when producing each answer. Coding agents depend on both: they keep instructions and earlier tool output in the window and assume the model will still follow rules placed there.

**「What to do differently」** If you run a coding agent on one of these open models, treat a long instruction file as advice rather than a guarantee: the author reports that a rule written in AGENTS.md \(the plain-text file a coding agent reads at the start of a session\) can quietly stop being followed by around the hundredth tool call, and that quality tends to break down somewhere between 128,000 and 256,000 tokens even on models advertising a million. His recommendation is to enforce anything that must never go wrong — deleting files, committing code, spending money — through hooks and permission checks that sit outside the model, and to repeat critical rules at the end of the prompt instead of burying them at the top.

**Tags**: `#long context`, `#open-source models`, `#AI agents`, `#coding agents`, `#LLM attention`

---

<a id="item-tech-news-9"></a>
### [Roundup lists 10 API routers with free or very cheap access to Claude, GPT and other models](https://habr.com/ru/articles/1097784/?utm_campaign=1097784&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A Russian-language article on Habr, published on 22 October 2026, rounds up 10 API routers — third-party services that sit between a user and several AI providers, so one account and one billing setup can reach models from different companies. The author says the piece includes test results for each router&\#x27;s API, the cost of short requests, usage limits, Russian-language support and the option to pay in rubles, and that the ordering of the platforms, the VPN information and the status of VseGPT and FreeRouter have been updated. The models named in the title are Claude, GPT, DeepSeek and GLM. The available excerpt is only an introduction: apart from VseGPT and FreeRouter it names no routers, and it gives no prices, quotas or test data, so the free and ultra-cheap claims cannot be checked from what is visible here.

rss · Habr AI · Oct 22, 09:48

**「What an API router is」** An API is the standard connection that lets one program ask another for something — here, sending a question to a model such as Claude or GPT and receiving the reply. An API router sits in the middle: you sign up once and get a single key, and the router decides which underlying provider handles each request, so you do not need a separate account with every model maker. FreeRouter, one of the services the article names, describes itself in exactly these terms — one key, in the format OpenAI&\#x27;s models use, that forwards requests to OpenRouter, Vercel, Cloudflare and others \(tool-2-2, tool-2-3\).

**「What it means if you were going to use it」** Anyone hoping to pick a router from this list will have to open the full article, because the visible part contains no cost figures or limits to compare. The author&\#x27;s own framing also sets the questions worth asking of any such service: what a short request actually costs, how tight the free quota is, whether Russian is supported, and whether payment can be made in rubles.

<details><summary>References</summary>
<ul>
<li><a href="https://freerouter.com/">FreeRouter | Free AI Gateway | Free LLM Router | Free LLM Gateway</a></li>
<li><a href="https://freerouter.eu.cc/">FreeRouter — Free models . One familiar API .</a></li>

</ul>
</details>

**Tags**: `#API routers`, `#access routes`, `#LLM pricing`, `#quotas`, `#model access`

---

<a id="item-tech-news-10"></a>
### [QA engineer describes linking an AI assistant to wiki, databases and tests via MCP](https://habr.com/ru/companies/X5Tech/articles/1096342/?utm_campaign=1096342&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A QA automation engineer at X5 Tech has published a first-person account of giving a large language model \(the kind of AI that powers chat assistants\) access to his team&\#x27;s wiki, a search index that matches on meaning rather than exact keywords, databases, test cases and the repository where automated tests live. The connections were made through MCP, the Model Context Protocol — an open standard that lets an AI assistant call outside tools and data sources instead of only talking. The author says the benefit was getting into unfamiliar business logic faster and checking hypotheses against real data without re-reading everything, and that the widely pitched use case — having the model generate manual test cases from documentation — turned out to be the least useful for him. The supplied excerpt stops before the actual configuration, commands and outcomes, so there is no reproducible setup or measured gain to report.

rss · Habr AI · Oct 22, 09:09

**「What MCP is」** MCP \(Model Context Protocol\) is an open standard, introduced by Anthropic in November 2024, that defines a common way for AI assistants to connect to outside tools and data sources. Think of it as one standard plug shape: instead of building a custom connection for every system, an assistant can be plugged into a wiki, a database or a code repository through the same interface. It is supported by a range of clients and servers, including assistants such as Claude and ChatGPT and development tools such as Visual Studio Code and Cursor.

**「What it means in practice」** For a team considering connecting an AI assistant to its own documentation and test systems, the reported lesson is to point it at looking things up — where data lives, which logic is current, what is already covered — rather than at producing test cases on demand. Because the account gives no configuration or numbers, it is a direction to try rather than a recipe to copy.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>
<li><a href="https://modelcontextprotocol.io/docs/2026-07-28/getting-started/intro">What is the Model Context Protocol (MCP)?</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#LLM tooling`, `#QA automation`, `#workflow`, `#vector search`

---

<a id="item-tech-news-11"></a>
### [Claude Code Hub v0.9.8 fixes high-severity Node.js security flaw](https://github.com/ding113/claude-code-hub/releases/tag/v0.9.8) ⭐️ 5.0/10

The maintainers of claude-code-hub, a program people run on their own servers to route Claude Code traffic through a shared gateway, released v0.9.8 to fix a high-severity security flaw in Node.js, the software runtime the hub uses. They describe the flaw, CVE-2026-111497, as an out-of-bounds write \(a memory error where a program writes past the intended boundary\) in Brotli decompression, a compression method used for web traffic, and say it can allow remote code execution, meaning an attacker could run their own commands on an affected server. The release also fixes a usage-limit page that could fail to open when there are many users, and corrects how a cached-request price multiplier is shown in logs. Docker users get an image built on Node 26.12.1; people not using Docker are told to upgrade to Node 22.23.4, 24.22.1, or 26.12.1 and later, or Bun 1.4.3 and later.

github · github-actions\[bot\] · Oct 22, 11:54

**「Context」** Claude Code is Anthropic&\#x27;s AI coding assistant that runs in a terminal, and claude-code-hub is a separate, community-built relay that a team can run on its own server to sit between its users and Anthropic&\#x27;s service, sharing access and tracking each person&\#x27;s quota. Brotli is a compression format used to shrink web traffic, and the flaw patched here is an out-of-bounds write in Node.js&\#x27;s Brotli decoder — Node.js being the software runtime the hub is built on — which Node&\#x27;s October 21, 2026 security advisory rated high severity and described as allowing remote code execution, meaning an attacker could get their own code to run on the machine.

**「What to do」** Anyone already running claude-code-hub should upgrade to v0.9.8: Docker users can pull the new image, while non-Docker users need one of the listed Node or Bun versions. The release does not change model behavior, pricing, or quota terms, so it is a security and maintenance update rather than a reason to switch tools.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/nodejs-brotli-decoder-bug-could-allow.html">Node . js Brotli Decoder Bug Could Allow Remote Code Execution in...</a></li>
<li><a href="https://nodejs.org/en/blog/vulnerability/october-2026-security-releases">Node . js — Wednesday, October 21, 2026 Security Releases</a></li>

</ul>
</details>

**Tags**: `#claude-code`, `#api-proxy`, `#security-patch`, `#self-hosted`, `#release`

---

<a id="item-tech-news-12"></a>
### [NVIDIA&\#x27;s OpenShell isolates fleets of AI agents in sandboxes](https://github.com/NVIDIA/OpenShell) ⭐️ 5.0/10

NVIDIA has published OpenShell on GitHub, a runtime \(the layer that actually launches and supervises a program while it runs\) for keeping large numbers of autonomous AI agents — programs that carry out multi-step tasks on their own, such as reading files, installing software and calling online services — inside isolated compartments so they cannot freely reach the rest of a machine, its stored passwords or its network. The project drew enough attention to trend on Hacker News. The available material describes it only at the level of containers \(self-contained bundles that keep an agent&\#x27;s files and processes separated from everything else\) and network rules; no version, install procedure, licence or independent test showing it works as described is included, so the promise of full capability without unrestricted access is a vendor framing rather than a measured result.

hackernews · niemandhier · Oct 22, 17:44 · [Discussion](https://news.ycombinator.com/item?id=50198675)

**「Background」** An AI agent is software that can take multi-step actions on its own, such as reading files, installing packages, and calling online services. OpenShell is a runtime — the layer that launches and supervises a program while it runs — that places each agent in a sandbox, a walled-off workspace. Rather than giving every agent full access to the machine, an operator writes a policy listing which files, credentials \(login details and access keys\), and network destinations each one may use, and OpenShell enforces that list.

**「What it means in practice」** For anyone already running agents on their own machine or server, the question that matters is what the isolation actually blocks. One commenter working on the same problem said that limiting an agent&\#x27;s network access to approved domains still leaves a route for it to copy out the code it is working on through one of those approved destinations, so a domain allowlist is a starting point rather than a guarantee against data leaving.

**「How commenters reacted」** Reaction was mixed. One commenter argued that running agents in containers should already be standard practice and called OpenShell a good way to manage those containers, while another said the pitch — full capability without unrestricted access — reads as an oxymoron, since giving an agent more access is precisely what makes it more capable.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/NVIDIA/OpenShell">GitHub - NVIDIA/OpenShell: OpenShell is the safe, private ...</a></li>
<li><a href="https://github.com/NVIDIA/OpenShell/wiki">GitHub - NVIDIA/OpenShell: OpenShell is the safe, private ...</a></li>

</ul>
</details>

**Tags**: `#agent-sandboxing`, `#developer-tooling`, `#containers`, `#NVIDIA`, `#security`

---

<a id="item-tech-news-13"></a>
### [AutoHarness: a Claude Code skill that makes AI agents prepare first](https://habr.com/ru/articles/1098004/?utm_campaign=1098004&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A developer writing on the Russian tech site Habr describes AutoHarness, a &quot;skill&quot; — a reusable set of instructions — for Claude Code, Anthropic&\#x27;s assistant that works from the command line, which pushes an AI agent to prepare before it starts a task: check whether documentation exists, decide what the result will be compared against, and set a point at which to stop. The author says he built it after several agents failed the same test task, drawing a scene from the film Blade Runner 2049 as an SVG image \(a picture defined by shapes and coordinates rather than pixels\); according to him, none of them looked at a real frame, all drew from memory, and all reported the work as finished. The post as supplied is only an introduction: it contains no code, installation steps, or prompt text, so the method cannot be reproduced from it. The claim that the skill improves results is the author&\#x27;s own account and is not independently measured here.

rss · Habr AI · Oct 22, 14:10

**「What a Claude Code skill is」** Claude Code is Anthropic&\#x27;s coding assistant — an AI agent, meaning a model given tools and allowed to take several steps on its own — that works inside a programmer&\#x27;s project. It can load &quot;skills&quot;: small packs of instructions, normally written and maintained by hand, that tell the agent how to handle a particular kind of job \(tool-2-3\). The author&\#x27;s starting point is that such agents fail less from lack of ability than from skipping preparation: never looking at reference material, never deciding in advance what a finished result should look like.

**「What a user can take from it」** For someone who uses a coding agent, the practical takeaway is a checklist rather than a tool: before letting the agent start, ask it what documentation it has, what its output will be compared against, and when it should stop. Because the excerpt published no installable files or prompt text, there is nothing to download or try yet.

<details><summary>References</summary>
<ul>
<li><a href="https://tigerless.ai/labs/autoharness">autoharness | Self-Learning Claude Code Skills | Tigerless Labs</a></li>

</ul>
</details>

**Tags**: `#Claude Code`, `#AI agents`, `#agent skills`, `#prompting workflow`, `#developer tooling`

---

<a id="item-tech-news-14"></a>
### [Developer regains understanding of AI-written pet project with two prompts](https://habr.com/ru/articles/1097826/?utm_campaign=1097826&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

Dina, a Java developer with about six years of enterprise experience, spent months from April building a personal side project together with an AI coding agent — a program that writes code on its own from task descriptions. She set the tasks and watched the tests, and everything looked fine: the tests passed and the planned scenarios were completed. Then she opened the project and realized she could not clearly explain how its main path worked, from an incoming request to a finished video. Her Habr article describes how she rebuilt that understanding using interactive explanations and two prompts. The published excerpt does not name the agent or model, and it does not include the text of the two prompts.

rss · Habr AI · Oct 22, 10:12

**「Why passing tests is not the same as understanding」** Automated tests check only the cases someone thought to write down; they confirm that specific inputs produce expected outputs, not that a person can follow what the program does. When an AI agent writes most of the code, the developer can end up supervising results rather than owning the design — the code works, but nobody on the team can explain it. The author&\#x27;s fix was to make the agent explain the code back to her step by step instead of only producing more of it.

**「What to watch for in your own projects」** Anyone who hands tasks to a coding agent faces the same gap: a green test run says nothing about whether you could debug or extend that code next month. A practical check is to try explaining the main flow of your own project out loud, and if you cannot, have the agent walk you through it section by section before adding features. The article&\#x27;s specific prompts are not reproduced in the available excerpt, so the exact wording would have to come from the full post.

**Tags**: `#AI coding agents`, `#developer workflow`, `#prompt engineering`, `#code comprehension`

---

<a id="item-tech-news-15"></a>
### [Qwen More Likely to Alert Authorities Than Western AI Models in SnitchBench Test](https://habr.com/ru/articles/1097762/?utm_campaign=1097762&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A replication of SnitchBench — a standardized test that gives AI models documents describing hidden patient deaths and checks whether they contact authorities — found Qwen much more willing to report than Claude, GPT, Gemini and Grok. The article&\#x27;s authors tested 27 models, including Russia&\#x27;s GigaChat and YandexGPT, in three scenarios: a neutral one, one that mentions the FBI, and a Russian-language one that mentions the FSB, Russia&\#x27;s security service. Qwen wrote to the FBI in 23 of its 33 runs; Claude, GPT, Gemini and Grok did so in only 2 of their 27. In the Russian/FSB scenario, the Western models never wrote \(0 of 27\), while Qwen wrote to the FSB in 9 of 33 runs.

rss · Habr AI · Oct 22, 08:46

**「What SnitchBench tests」** SnitchBench is a public test that gives an AI model a scenario involving possible wrongdoing and checks whether the model contacts an outside authority such as the FBI, the FDA or the media. The original test focused on US agencies; the replication described here adds a Russian-language scenario involving Russia&\#x27;s FSB security service and includes Russian models such as GigaChat and YandexGPT.

**「What It Means」** For teams using an AI agent to process confidential medical or legal records, the result is a reminder that the model can act as a reporting policy: if the agent can send messages or browse outside services, that access should be limited or tested, because the benchmark shows model choice can change whether a case is escalated. This is a small benchmark, not a guarantee of how any model behaves in a real deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.snitchbench.com/methodology">SnitchBench : AI Model Whistleblowing Behavior Analysis by Theo...</a></li>
<li><a href="https://simonwillison.net/2025/May/31/snitchbench-with-llm/">How often do LLMs snitch ? Recreating Theo’s SnitchBench with LLM</a></li>

</ul>
</details>

**Tags**: `#SnitchBench`, `#LLM benchmarks`, `#agent safety`, `#Qwen`, `#Russian LLMs`

---

<a id="item-tech-news-16"></a>
### [NLMK IT says one engineer directing AI agents cut a legacy rewrite&\#x27;s effort tenfold](https://habr.com/ru/companies/nlmk/articles/1091666/?utm_campaign=1091666&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

NLMK IT, the IT division of the Russian steelmaker NLMK, says it moved an old but still-critical business system onto a new technology platform by assigning the job to a single engineer who coordinated a team of AI agents — software that can carry out multi-step work such as writing and changing code with limited step-by-step instruction — instead of a conventional project team. In the first stage of the experiment, the company reports, IT labor spent on development fell tenfold. After the migration, NLMK IT kept an AI agent running inside the new system, where it now assists the people who use it. The account is the company&\#x27;s own, published as a post on the Russian tech site Habr; it names no AI models or tools, describes no architecture or workflow, and the tenfold figure has not been independently verified.

rss · Habr AI · Oct 22, 08:14

**「Background」** A &quot;legacy&quot; system is an old piece of software that still runs day-to-day business — orders, records, internal workflows — and is wired into other applications, which is why replacing it is risky and slow rather than merely unfashionable. Rewrites usually consume years and large teams because someone has to read the old code, work out what it actually does, and reproduce that behavior on a new platform. The pitch for AI agents is that much of that reading, translating and rewriting can be delegated, with a person setting the task and checking the results.

**「Impact」** The tenfold figure covers development labor in the first stage of the experiment only; the post does not say how long the migration took end to end, how many people worked alongside the coordinating engineer, or what running the agents cost. A team hoping to repeat the result therefore has nothing concrete to copy yet, and the practical burden it implies falls on the one person who must specify the work and verify what the agents produce.

**Tags**: `#AI coding agents`, `#legacy migration`, `#developer productivity`, `#enterprise case study`

---

<a id="item-tech-news-17"></a>
### [A Team Lead&\#x27;s Three-Stage Path Through Six AI Courses From Google, Anthropic and OpenAI](https://habr.com/ru/companies/svoi_ru/articles/1096464/?utm_campaign=1096464&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A team lead at the software company СВОЙ Тех published a Habr article on 22 October 2026 rounding up six AI courses — two each from Google, Anthropic and OpenAI — and ordering them into a three-stage route that starts with basic chatbot use and ends with AI agents \(software that carries out multi-step tasks on its own instead of answering one question at a time\). The visible portion explains his selection logic: most people use chatbots like a powerful car they never drive out of the garage, asking a single question, getting a translation or a term explained, and closing the tab, while university-style programmes bury beginners in linear algebra and statistics they do not yet need. He says readers do not have to take all six and can jump straight to the stage that matches their experience. The available text does not name the individual courses, their prices, or how long they take; those details are in the full article.

rss · Habr AI · Oct 22, 07:00

**「Background」** Google, OpenAI and Anthropic each already publish their own AI course catalogs — Google AI Essentials, OpenAI Academy and Claude Academy \(the new name for Anthropic Academy\) — which teach people to use their products and, in OpenAI&\#x27;s case, to build agents and workflows. Because the courses come from the vendors themselves, they also introduce learners to each company&\#x27;s vocabulary and preferred way of working.

<details><summary>References</summary>
<ul>
<li><a href="https://academy.openai.com/pages/courses">OpenAI Academy Courses</a></li>
<li><a href="https://pasqualepillitteri.it/en/news/371/anthropic-academy-free-courses-claude">Claude Academy , formerly Anthropic Academy , 26 Free Courses</a></li>
<li><a href="https://runtimewire.com/article/anthropic-claude-academy-employee-ai-training">Anthropic launches Claude Academy , turning employee training into...</a></li>

</ul>
</details>

**Tags**: `#AI courses`, `#Anthropic`, `#OpenAI`, `#Google`, `#developer education`

---

<a id="item-tech-news-18"></a>
### [Cursor Cancelled a Company’s Pro Subscriptions Over Region Restrictions](https://habr.com/ru/companies/domate/articles/1097476/?utm_campaign=1097476&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

On September 4, 2026, Cursor cancelled the Pro subscriptions of a company’s team because of activity from a region where it blocks access, according to a company blog post on Habr. The post says the cancellation hit almost everyone at the company and quotes Cursor’s email: it took effect that day, came with a $24.00 prorated refund, and offered no appeal. The same post says the team built its own AI coding agent — software meant to write and edit code with less step-by-step input — and now plans to release it, but the excerpt gives no details on availability, price, or capabilities.

rss · Habr AI · Oct 22, 06:24

**「Background」** Cursor is a paid AI coding assistant: software that suggests and writes code inside a programmer&\#x27;s editor. Like other online services, it can cancel accounts when it detects use from a region it does not serve. The company behind this post says its team had already switched to another coding assistant and a VPN \(software that makes internet traffic appear to come from another country\) before deciding to build its own tool.

**「What this means if you pay for Cursor」** If you use Cursor from a region its model providers do not cover, a paid plan can be cancelled mid-term with no appeal — the company in this post received a $24.00 refund prorated to its remaining included usage, not an option to keep working. Cursor&\#x27;s own documentation says model availability depends on the terms its model partners set and that affected models will be restored only where those partners allow access, so teams relying on it should confirm their region is supported and keep a second tool ready.

<details><summary>References</summary>
<ul>
<li><a href="https://cursor.com/docs/account/regions">Regions | Cursor Docs</a></li>
<li><a href="https://cursor.com/help/account-and-billing/cancel">Cancel your subscription | Cursor Docs</a></li>

</ul>
</details>

**Tags**: `#Cursor`, `#access restrictions`, `#regional bans`, `#coding agents`, `#vendor promotion`

---

<a id="item-tech-news-19"></a>
### [miHoYo and Tsinghua release GameScaling game-control models](https://arxiv.org/abs/2610.28698v1) ⭐️ 5.0/10

miHoYo&\#x27;s Honkai AI team, with Tsinghua University and other institutions, released GameScaling, a set of open-weight game-control models built on Qwen3.5. Open-weight means the trained model files are published for others to download and run. The models range from 0.8 billion to 27 billion parameters \(a common measure of model size\) and output the keyboard and mouse actions for the next 200 milliseconds. Eight checkpoints \(saved copies of the trained model\) and an inference client \(software for running a trained model\) are available under Apache-2.0, a permissive open-source license, but the training code is not included. The accompanying paper reports 120 training configurations testing data volume, diversity, and model size.

telegram · zaihuapd · Oct 22, 11:32

**「Background」** A game-control model learns by watching what is on screen and what the player did next with the keyboard and mouse, then predicting the following actions; here a vision-language model \(one trained on both images and text\) is repurposed to read the screen. &quot;Open weights&quot; means the trained parameters are published so anyone can download and run them, rather than only describing the method in a paper, and a &quot;checkpoint&quot; is one saved copy of those parameters at a particular size. miHoYo is the Chinese studio behind Genshin Impact and Honkai: Star Rail, and Qwen3.5 is Alibaba&\#x27;s openly published model family that outside teams are allowed to build on.

**「What it means」** For people building game-playing AI, the release provides ready-made model files and a client to run them, so they can test the approach without training a model first. But because the training code is withheld, they cannot reproduce the paper&\#x27;s training setup or retrain the models from the release alone.

**Tags**: `#open-weight models`, `#game AI`, `#Qwen`, `#vision-language models`, `#research release`

---

<a id="item-tech-news-20"></a>
### [Mebular pitches device-local memory for AI agents, without proof it works](https://github.com/Windsander/Mebular) ⭐️ 5.0/10

Mebular, an open-source project on GitHub, describes itself as a decentralized memory layer for AI agents — meaning the notes and history an AI assistant keeps about you are stored on your own devices instead of a company&\#x27;s cloud servers. The project&\#x27;s own write-up says it syncs directly between devices without a central server \(peer-to-peer\), keeps working offline and reconciles changes on its own, signs and content-addresses records so they can be checked for tampering, and offers a task-tree structure, a certificate chain for tracing trust, and adapters for Obsidian, log journals and json-memo, with desktop, browser and command-line interfaces. The post announcing it is promotional trend commentary: it gives no version number, no installation steps in the text, no benchmarks and no evidence that anyone is using it, so all of the above is the project&\#x27;s description of itself rather than a verified capability.

telegram · aipluscn · Oct 22, 13:32

**「What a memory layer is」** An AI agent — software that carries out multi-step tasks on its own — needs somewhere to keep what it has picked up: earlier conversations, notes, a record of what it already did. That store is normally a company&\#x27;s cloud server, which is what lets the agent resume later but also means the operator holds the data. Mebular&\#x27;s premise is to keep that store on the user&\#x27;s own devices instead and let the devices sync directly with one another, the way file-sharing software swaps files between computers without a central hub.

**「What it means if you are picking tools」** For anyone choosing where an AI assistant should keep long-term memory, this is something to watch rather than adopt: there is no release version, no measured result and no independent report of it working. The trade-off it advertises is real — memory that lives only on your own devices means no company holds it, but backing it up and keeping several machines in agreement becomes your job rather than a vendor&\#x27;s, so check the linked setup guides and the repository&\#x27;s documentation before trusting it with notes you care about.

**Tags**: `#AI agents`, `#memory layer`, `#decentralized`, `#open-source`, `#developer tooling`

---

<a id="item-tech-news-21"></a>
### [Open-source mdbook-ai-skill packages mdBook docs as a skill for 33+ AI coding assistants](https://github.com/marceloeatworld/mdbook-ai-skill) ⭐️ 5.0/10

A developer has published an open-source project on GitHub called mdbook-ai-skill that gives AI coding assistants a ready-made reference for mdBook, a tool for turning Markdown files \(plain text with simple formatting marks\) into documentation websites. The project uses the Agent Skills format — a folder containing a SKILL.md file that tells an assistant what it knows and how to use it — and the author says it works with more than 33 assistants, including Claude Code, Cursor, Windsurf and GitHub Copilot. Its reference files are generated from the official mdBook guides and refreshed daily by GitHub Actions, GitHub&\#x27;s built-in automation for running tasks on a schedule. The repository describes installation and update steps, but the post shows no code and no evidence that anyone besides the author uses it, and it sends readers to a Telegram link for the full setup guide; the skill only supplies documentation about mdBook itself, not a new capability for the assistants.

telegram · aipluscn · Oct 22, 13:32

**「Background」** Agent Skills is an open standard in which a file named SKILL.md gives an AI coding assistant a reusable set of instructions and reference material; the assistant reads it from a skills folder. AI coding assistants — programs such as Claude Code, Cursor and GitHub Copilot that write or edit code for a user — can use the same SKILL.md across different tools, so a project can publish one set of reference documents instead of a separate copy for each assistant. This project applies that format to the official mdBook guide, mdBook being a tool that turns Markdown files into documentation pages.

**「What it changes for mdBook users」** If you write documentation with mdBook \(a tool that turns Markdown files into a navigable online book\) and also ask an AI coding assistant for help with it, installing this skill gives the assistant a local, daily-refreshed copy of mdBook&\#x27;s official reference, so its answers about commands and settings are less likely to be made up. The catch is scope: it only covers mdBook&\#x27;s own documentation, not the other tools in your project, and the full setup steps sit behind a Telegram link rather than in the repository, so check the install script before running it.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/marceloeatworld/mdbook-ai-skill">GitHub - marceloeatworld/mdbook-ai-skill: Auto-updated mdBook ...</a></li>
<li><a href="https://agentscamp.com/guides/skills/agent-skills-open-standard">The Agent Skills Standard: One SKILL.md, Every Tool</a></li>
<li><a href="https://skillmd.com/">SkillMD · The Open Library of AI Agent Skills</a></li>
<li><a href="https://github.com/marceloeatworld/mdbook-ai-skill">GitHub - marceloeatworld/ mdbook - ai - skill : Auto-updated mdBook...</a></li>
<li><a href="https://rust-lang.github.io/mdBook/">Introduction - mdBook Documentation</a></li>
<li><a href="https://www.skills.sh/">Discover and install skills for AI agents.</a></li>

</ul>
</details>

**Tags**: `#coding agents`, `#Agent Skills`, `#mdBook`, `#developer tooling`, `#open source`

---

## Financial News

<a id="item-finance-news-1"></a>
### [CSI 300 falls 20% from June high as A-shares near bear market](https://www.bloomberg.com/news/articles/2026-10-22/china-stocks-set-for-bear-market-as-ai-trade-policy-hopes-fade) ⭐️ 8.0/10

China&\#x27;s CSI 300 fell as much as 1.7% on Thursday and was 20% below its June high, leaving A-shares near a bear market as the ChiNext index fell for a 16th straight session. The selloff followed a lack of substantive fiscal stimulus and CATL&\#x27;s quarterly profit growth missing expectations, which sent its shares down 12% on Wednesday.

telegram · zaihuapd · Oct 22, 05:05

**「Background」** A 20% fall from a recent peak is the common threshold for a bear market, so the CSI 300&\#x27;s drop from its June high puts the benchmark at that line.

<details><summary>References</summary>
<ul>
<li><a href="https://t.me/zaihuapd/44609">在花 科技圈 – Telegram</a></li>

</ul>
</details>

**Tags**: `#中国股市`, `#沪深300`, `#熊市`, `#宁德时代`, `#市场抛售`

---

<a id="item-finance-news-2"></a>
### [Australian Court Orders Apple to Open iPhone to Third-Party App Stores](https://9to5mac.com/2026/10/21/apple-must-open-iphone-to-alternative-app-stores-in-australia-after-epic-games-ruling/) ⭐️ 8.0/10

An Australian federal court ruled that Apple must let Australian iPhone users install apps through third-party app stores and websites, and offer alternative payment methods and external payment links, from March 1, 2027, in a case brought by Epic Games; the judge found Apple held substantial market power in iOS app distribution and payments and that its restrictions breached Australian competition law. Apple said it will appeal and seek a stay of the ruling, while Fortnite is set to return to the Australian App Store immediately.

telegram · zaihuapd · Oct 22, 06:54

**「Background」** The order follows Epic Games&\#x27; antitrust lawsuit, in which Australia&\#x27;s Federal Court found that Apple held substantial market power in iOS app distribution and payments and that its restrictions violated Australian competition law.

**「Who is affected」** If the order takes effect, Australian iPhone users would be able to install apps from third-party marketplaces or developers&\#x27; own websites and pay via external links, letting developers route transactions outside Apple&\#x27;s in-app payment system — though Apple&\#x27;s planned appeal and stay request leave the March 1, 2027 start date uncertain.

<details><summary>References</summary>
<ul>
<li><a href="https://www.resetera.com/threads/apple-ordered-to-open-the-app-store-to-alternate-stores-in-australia.1667204/">Apple ordered to open the App Store to alternate stores in Australia</a></li>
<li><a href="https://www.resetera.com/threads/apple-ordered-to-open-the-app-store-to-alternate-stores-in-australia.1667204/">Apple ordered to open the App Store to alternate stores in Australia</a></li>
<li><a href="https://www.engadget.com/2293801/fortnite-is-back-on-apple-australian-app-store-following-court-ruling/">Fortnite Is Coming Back To Apple &#x27;s Australian App Store Following...</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#Epic Games`, `#antitrust`, `#app store regulation`, `#Australia`

---

<a id="item-finance-news-3"></a>
### [Report: Banned Nvidia B300 Chips Appear in China State-Linked Deal](https://theinference.org/article/china-s-state-money-bought-banned-nvidia-b300-servers-then-redacted-the-receipts) ⭐️ 7.0/10

A Chinese state-controlled semiconductor leasing group reportedly financed the purchase of 32 ASUS servers containing Nvidia B300 chips, part of a deal worth more than 3 billion yuan, then removed hardware details from a regulatory filing after it drew scrutiny. The B300 is under the strictest US export-control tier and is effectively barred from sale to China; Nvidia said it is investigating with manufacturing partners, while ASUS said it complies with export controls.

telegram · zaihuapd · Oct 22, 15:22

**「Background」** The B300 is an Nvidia AI chip in the strictest U.S. export-control tier, which effectively bars its sale to China.

**Tags**: `#Nvidia`, `#export controls`, `#China`, `#AI infrastructure`, `#semiconductor supply chain`

---