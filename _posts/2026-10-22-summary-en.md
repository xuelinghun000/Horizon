---
layout: default
title: "Horizon Summary: 2026-10-22 (EN)"
date: 2026-10-22
lang: en
---

> From 139 items, 21 important content pieces were selected

---

**Technology News**
1. [Report: LiteLLM 1.107.0 on PyPI shipped a credential stealer](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenAI keeps Codex and Work caches permanently, adds 12-hour API cache](#item-tech-news-2) ⭐️ 8.0/10
3. [Ollama adds Flint, a 40B coding model, for Macs](#item-tech-news-3) ⭐️ 7.0/10
4. [new-api test release fixes security flaw and Claude response dropouts](#item-tech-news-4) ⭐️ 6.0/10
5. [Blind test of 27 AI models targets broken data output and hidden instructions](#item-tech-news-5) ⭐️ 6.0/10
6. [Anthropic opens US waitlist for Duet, an always-on Claude agent](#item-tech-news-6) ⭐️ 6.0/10
7. [Community plugin Hey adds Markdown task tracking to Claude Code](#item-tech-news-7) ⭐️ 6.0/10
8. [OpenAI Will Require Approval for Services That Resell Access to Its Models](#item-tech-news-8) ⭐️ 6.0/10
9. [IBM announces Granite Speech 5.0 for transcription and translation](#item-tech-news-9) ⭐️ 5.0/10
10. [Blogger Gave an AI Agent a Bank Card and 200+ Integrations](#item-tech-news-10) ⭐️ 5.0/10
11. [Team Builds Claude Code Reviewer From Three Years of PR Comments](#item-tech-news-11) ⭐️ 5.0/10
12. [Open-source Slightly Parallel dashboard announced for multi-project coding agents](#item-tech-news-12) ⭐️ 5.0/10
13. [How a ReAct agent works: model, tools, and control loop](#item-tech-news-13) ⭐️ 5.0/10
14. [Free local meeting transcription with T-one drafts and GigaAM cleanup](#item-tech-news-14) ⭐️ 5.0/10
15. [A DIY 3D game engine for the ESP8266 chip, explained in code](#item-tech-news-15) ⭐️ 5.0/10
16. [Unconfirmed report: OpenAI models may come to Antigravity for paid users](#item-tech-news-16) ⭐️ 5.0/10
17. [fal releases FLUX 3 Max, a faster video model with audio](#item-tech-news-17) ⭐️ 5.0/10
18. [AgentGrid, an open-source tool for running several AI coding agents together](#item-tech-news-18) ⭐️ 5.0/10
19. [Major websites are blocking AI shopping and booking agents](#item-tech-news-19) ⭐️ 5.0/10
20. [Lawyer&\#x27;s letter targets plugin accused of farming WorkBuddy/CodeBuddy free quota](#item-tech-news-20) ⭐️ 5.0/10
21. [OpenAI models to be sold through Google Cloud&\#x27;s model catalog](#item-tech-news-21) ⭐️ 5.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Report: LiteLLM 1.107.0 on PyPI shipped a credential stealer](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) ⭐️ 8.0/10

A security firm called SafeDep reports that version 1.107.0 of LiteLLM — a free tool that lets an app send requests to many different AI models through one shared connection, often called an LLM proxy or gateway — was published to PyPI \(Python&\#x27;s public library of installable packages\) with malicious code inside it. According to the writeup, that code stole credentials and installed a backdoor, and the attackers got in by compromising three developers&\#x27; GitHub accounts. The report has not been independently confirmed here, and the source item supplied no technical detail beyond the headline. Anyone who installed that exact version should treat any keys or passwords reachable from that machine as exposed, move to a different version, and replace those credentials.

hackernews · abhisek · Oct 21, 14:00 · [Discussion](https://news.ycombinator.com/item?id=50181114)

**「What LiteLLM and PyPI are」** LiteLLM is a free, open-source program that developers install so their apps can send requests to many different AI models through one shared interface — a switchboard between software and providers such as OpenAI or Anthropic. It is distributed through PyPI, the public warehouse for Python software, where installing a package means running code published under the project&\#x27;s name; the affected files were the ready-to-install bundles \(called &quot;wheels&quot;\) for version 1.107.0, and the malicious code was reportedly inserted into the build process rather than appearing in the project&\#x27;s public source code.

**「What to do if you run LiteLLM」** Because LiteLLM sits between an application and several AI providers at once, a machine that ran 1.107.0 could have handed over the API keys \(the account credentials used to call each model service\) for every provider it was set up with, not just one — so replacing a single key is not enough. Anyone whose install or container pull brought in 1.107.0 should confirm the version, move back to an earlier release, rebuild the container from a clean image rather than patching it in place, and then replace every credential that machine could reach, since the malicious code also loaded tools for running outside code on the host. LiteLLM says customers on its private enterprise release were not affected, so those installations need no action.

**「From the comments」** One commenter recommended canarytokens.org, a free service that plants a fake credential and alerts you if someone uses it, as an early warning if stolen keys are tried. Another argued that sandboxing tools and permission prompts stop working in practice, because people grow numb to pop-ups and to installing packages by habit. A third said this is the second serious LiteLLM compromise in roughly a year or two, citing a March incident, and advised pinning to a version before 1.107.0 until further notice; another reader questioned how a project with 55,000 code changes in three years could still be hit this way.

<details><summary>References</summary>
<ul>
<li><a href="https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/">Compromised LiteLLM 1.107.0 on PyPI Installs a Credential ...</a></li>
<li><a href="https://github.com/BerriAI/litellm/issues/47826">Litellm 1.107.0 on PYPI Compromised - GitHub</a></li>
<li><a href="https://docs.litellm.ai/blog/security-incident-oct-21-2026">Contained: Oct 21, 2026 LiteLLM release v1.107.0 Compromised</a></li>
<li><a href="https://www.rescana.com/post/litellm-1-107-0-supply-chain-compromise-october-2026">LiteLLM 1.107.0 Supply-Chain Compromise: Credential-Stealing ...</a></li>
<li><a href="https://openhack.com/blog/litellm-1-107-0-supply-chain-attack">LiteLLM 1.107.0 Compromise: Impact and Remediation</a></li>

</ul>
</details>

**Tags**: `#supply-chain-security`, `#litellm`, `#pypi`, `#llm-proxy`, `#credential-theft`

---

<a id="item-tech-news-2"></a>
### [OpenAI keeps Codex and Work caches permanently, adds 12-hour API cache](https://telegram.me/ai_newz/4813) ⭐️ 8.0/10

OpenAI&\#x27;s Codex \(its AI coding agent\) and ChatGPT Work now keep a session&\#x27;s cache permanently, according to a report from the Telegram channel ai\_newz. The cache is the already-processed form of a conversation that the model reuses instead of re-reading it, and until now an idle session could burn a large share of a user&\#x27;s usage limits rebuilding it after a few hours away. Separately, the API \(the paid interface companies use to build the models into their own software\) now lets developers keep a cache for 12 hours, charged at double the price of the existing 30-minute cache write. The report gives no exact prices, and OpenAI has not been confirmed as announcing the change directly.

telegram · ai\_newz · Oct 21, 03:44

**「What a prompt cache is」** When you use an AI assistant, the service can keep a stored copy of the instructions and earlier conversation so the model does not have to re-read all of it on every new message. OpenAI calls this prompt caching, and it is what makes long, ongoing sessions cheaper and faster for both the company and the customer. Until now that stored copy was short-lived: a 30-minute version was the standard option, so a session left idle for a few hours had to be rebuilt from scratch before the conversation could continue.

**「What it means in practice」** A paying Codex user who steps away for a couple of hours and then resumes the same session should no longer see limits eaten by cache rebuilding. For API customers, the 12-hour option only saves money if the same long prompt is reused within that window, since writing the cache costs twice as much as the 30-minute version.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.openai.com/api/docs/guides/prompt-caching">Prompt caching | OpenAI API</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#Codex`, `#caching`, `#API pricing`, `#rate limits`

---

<a id="item-tech-news-3"></a>
### [Ollama adds Flint, a 40B coding model, for Macs](https://github.com/ollama/ollama/releases/tag/v0.40.8) ⭐️ 7.0/10

Ollama version 0.40.8 now includes Flint, a coding model from Recursive that Mac users can start with the command \`ollama run flint\`. Flint is released under Apache 2.0 \(a permissive open-source license\), has 40 billion parameters in total, and uses a mixture-of-experts design in which only about 2.5 billion parameters are active for each token \(a small piece of text\) it generates. It can consider up to 262,000 tokens of context at once, and Recursive reports scores of 54.9% on Terminal-Bench 2.1 and 74.2% on SWE-bench Verified; these are the maker&\#x27;s own benchmark results, not independent measurements. Support is currently macOS-only, with other GPUs promised in a later release.

github · github-actions\[bot\] · Oct 21, 16:20

**「What Ollama and Flint are」** Ollama is a free program that downloads and runs AI models on a personal computer instead of sending requests to a cloud service. Models in its library are packaged so that a single command fetches and starts them, and Flint is the newest coding-focused model added to that library.

**「What it means in practice」** Mac users get a one-command way to run a coding model locally, without sending code to a cloud service. People using Windows or Linux with non-Mac GPUs cannot run Flint through this Ollama release yet and must wait for the promised follow-up.

**Tags**: `#ollama`, `#flint`, `#open-weight-models`, `#coding-models`, `#local-llm`

---

<a id="item-tech-news-4"></a>
### [new-api test release fixes security flaw and Claude response dropouts](https://github.com/QuantumNous/new-api/releases/tag/v1.0.0-rc.46) ⭐️ 6.0/10

new-api v1.0.0-rc.46, a near-final test version of software that people run on their own servers to route requests to different AI models, is out with a fix for a publicly tracked security vulnerability, CVE-2026-111943, and the project recommends that people running it upgrade soon. The release runs on Go 1.26.10, the version of the Go programming language that also changes which intermediate certificates—the middle links in the chain that proves a secure connection—are rejected; anyone building it from source code must use that version too. The release notes name the vulnerability but give no severity or attack details, so the notes alone do not show how urgent the fix is. Among other changes, it adds the Resend email service as an alternative way to send mail, support for Alibaba&\#x27;s qwen3-vl-embedding model for turning images and text into numerical representations for search and comparison, and fixes for Claude live responses dropping during preparation and retries, tool calls \(requests from the model to run an outside function\) being lost when assistant messages are merged, task retries being charged at the previous route&\#x27;s price, DeepSeek balances showing zero when only the yuan wallet has money, and Gemini image or video embedding requests being billed instead of rejected.

github · Calcium-Ion · Oct 21, 16:25

**「Background」** new-api is a self-hosted gateway: software that a team runs on its own server so that many applications can send requests to different AI providers through one common address, while the gateway tracks usage and charges. This build is a release candidate \(rc\), a near-final test version ahead of the finished 1.0.0 release, so it is aimed at operators already running or testing the gateway rather than at ordinary end users.

**「What operators should do」** Anyone running new-api as their shared gateway should upgrade, and anyone who compiles it from source must also switch their build tools to Go 1.26.10 — the release notes say so directly, and the underlying Go flaw \(CVE-2026-111943\) is a compromised certificate authority whose untrusted intermediate certificates, the middle links in the chain that proves a website&\#x27;s identity, older Go versions still accept. Expect a side effect after upgrading: outbound HTTPS connections to any service still relying on those blocked intermediates will now fail with a certificate error, which is the intended behaviour rather than a new bug. Separately, the billing fix changes behaviour for task retries — when a retry moves to a more expensive channel, the extra cost is now reserved before the request goes out, so a task will be refused instead of sent when the balance cannot cover the difference.

<details><summary>References</summary>
<ul>
<li><a href="https://socprime.com/blog/cve-2026-111943-analysis/">CVE - 2026 - 111943 : eMudhra CA Key Compromise</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/mozilla-google-apple-block-compromised-emudhra-ca-certificates/">Mozilla, Google, Apple block compromised eMudhra CA certificates</a></li>

</ul>
</details>

**Tags**: `#api-relay`, `#security`, `#claude`, `#deepseek`, `#release-notes`

---

<a id="item-tech-news-5"></a>
### [Blind test of 27 AI models targets broken data output and hidden instructions](https://habr.com/ru/articles/1096934/?utm_campaign=1096934&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A Russian developer published a blind comparison of 27 AI models — large language models, the software behind chatbots — on the Habr site on 21 October, judging them on practical failures rather than exam-style benchmarks. The test asks whether a model breaks a data parser by putting a polite &quot;Here is your JSON:&quot; \(JSON being the strict text format programs use to pass data to each other\) before the opening curly bracket, whether it obeys an instruction hidden inside a customer email \(an &quot;indirect prompt injection&quot;\), whether it invents Russian criminal-code articles, and how much each run costs in time and money. The visible portion of the article is only the setup: it names the entrants, including GPT-6, Opus, Alisa, Google&\#x27;s Gemini 4 Argon and Muse Wonder, and says the author waited for the last of them to launch, but it gives no scores, prices or per-model results, and the headline&\#x27;s Russian personal-data law \(152-FZ\) angle does not appear in the excerpt. The author says he ran a similar audit of 14 models for made-up answers in January.

rss · Habr AI · Oct 21, 06:23

**「Background」** The article introduces a Russian-language crash test of 27 large language models \(the software behind chatbots\), published in October 2026. The author says he previously audited 14 models for made-up answers in January, after Gemini 3 appeared, and this time waited for Google&\#x27;s Gemini 4 Argon and Muse Wonder before starting. The tests focus on business use: whether a model breaks JSON \(a strict data format exchanged between programs\), follows a hidden instruction embedded in a customer email, or handles Russia&\#x27;s 152-FZ personal-data law; the excerpt supplied here contains no results.

**「Why it matters in practice」** For anyone wiring a model into an order system, CRM or other automated pipeline, these are the questions that decide whether the integration works at all: a model that adds a friendly sentence before its data output can stop the receiving program dead, and one that follows instructions buried in a client&\#x27;s message can change records on its own. Because the published excerpt stops before the results, it cannot yet tell a reader which of the 27 models to choose or avoid.

**Tags**: `#LLM benchmarks`, `#prompt injection`, `#JSON reliability`, `#model comparison`, `#AI compliance`

---

<a id="item-tech-news-6"></a>
### [Anthropic opens US waitlist for Duet, an always-on Claude agent](https://claude.com/product/claude-duet) ⭐️ 6.0/10

Anthropic has opened a preview waitlist, limited to the United States, for Claude Duet — a separate app in which an &quot;always-on&quot; agent \(software that keeps working in the background on your behalf rather than only answering when you type\) runs tasks and sends daily briefings. One Telegram channel reports the app is live on iOS, Android and the claude.ai website for US Pro and Max subscribers who join the waitlist, is built on Claude Opus 5.5 \(the newest version of Anthropic&\#x27;s Claude model, per that same channel\), and draws on the same subscription quota — the monthly usage allowance — as other Claude products. Another channel says Duet is promised to $20-a-month subscribers, unlike the rival agent app dots, which is limited to Pro-tier customers. Before sending a message, making a payment, signing a document or deleting anything, Duet is said to show the planned action and wait for approval; securities trading and transfers between accounts are barred even with permission. These details come from Telegram channels rather than the linked product page, and no hands-on testing or pricing specifics have been published.

telegram · ai\_newz · Oct 21, 20:02

**「Background」** A &quot;proactive agent&quot; is software that acts on your behalf without waiting for a prompt each time: it runs on the company&\#x27;s servers rather than on your phone, keeps working while you are away, and pauses to ask for your approval before doing something consequential. Anthropic sells Claude in tiers, with Pro as the entry paid plan at $20 a month and Max priced higher. The source presents Duet as a rival to &quot;dots&quot;, an existing always-on assistant that it says is limited to Pro subscribers.

**「What it means for you」** If you already pay for Claude, the detail to watch is the shared quota: work Duet does in the background would come out of the same monthly allowance as your ordinary chats, so heavy use could leave less room for everything else. The practical catch today is access — only US subscribers can join the waitlist, and joining it is not the same as getting in.

**「What commenters are saying」** On Hacker News, one commenter complained that signing up for the waitlist requires retyping information Anthropic already has, and argued the request should be possible from inside an existing Claude chat. Another said that having a personal assistant backed by a top-tier model is what makes its output trustworthy enough to skip double-checking, claiming to have bought a car largely through a rival assistant. A third speculated that these assistant products are high-margin for the labs because their requests are not time-sensitive and can be slotted into spare computing capacity, while a fourth said they are unwilling to hand over personal data to such tools.

<details><summary>References</summary>
<ul>
<li><a href="https://claude.com/product/claude-duet">Claude Duet | Your personal AI assistant</a></li>

</ul>
</details>

**Tags**: `#Claude`, `#Anthropic`, `#AI agents`, `#subscription quota`, `#product preview`

---

<a id="item-tech-news-7"></a>
### [Community plugin Hey adds Markdown task tracking to Claude Code](https://github.com/keenkim1202/Hey) ⭐️ 6.0/10

A developer outside Anthropic has published a free plugin called Hey that adds task tracking and time estimates to Claude Code, Anthropic&\#x27;s assistant that works inside a text-based terminal rather than a chat window. The plugin is installed from Claude Code&\#x27;s plugin marketplace and adds slash commands — typed instructions such as /hey-ledger and /wassup — that keep a to-do list in Markdown, a plain-text formatting style that stays readable as raw text. Its scripts use only Python&\#x27;s built-in standard library, so nothing extra needs to be installed, and the estimating part is handled by the AI model reading the plugin&\#x27;s instructions. The post gives no version number, no usage walkthrough and no evidence of how accurate the estimates are, and it frames Hey as something Claude Code &quot;added&quot; when it is a third-party add-on rather than an official Anthropic feature.

telegram · aipluscn · Oct 21, 07:10

**「Background」** Claude Code is a command-line AI coding assistant; plugins are add-ons that give it extra commands. Hey is a community-built plugin distributed through Claude Code&\#x27;s plugin marketplace, not a built-in feature. It keeps tasks in Markdown, a plain-text format for notes and checklists, and is operated through slash commands—short instructions typed with a leading “/”.

**「What it means in practice」** Anyone using Claude Code can try it today by installing from the plugin marketplace, and because the task list is stored as plain Markdown, the files stay readable and editable outside the tool. The practical caveat is that the estimates come from the model&\#x27;s own judgement with no published accuracy check, so treat them as rough guesses rather than project schedules until you have compared them against work you have already done.

**Tags**: `#Claude Code`, `#developer tooling`, `#plugins`, `#task management`, `#GitHub project`

---

<a id="item-tech-news-8"></a>
### [OpenAI Will Require Approval for Services That Resell Access to Its Models](https://openai.com/index/broad-access-through-consistent-standards/) ⭐️ 6.0/10

OpenAI announced on October 21 that services which directly give people access to its AI models — including model routers and AI gateways, which take a request and pass it to one of several models — must first go through a review and be approved. The updated usage policy takes effect on November 20, 2026. Companies that host or resell OpenAI&\#x27;s models must also keep the same safety protections, investigate suspected misuse and cooperate with law enforcement, and OpenAI said it is introducing &quot;SafetyIDs,&quot; which let it tell end users apart during an investigation without revealing their identities. OpenAI did not say what the approval process requires or what happens to services that are not approved.

telegram · zaihuapd · Oct 22, 00:46

**「Background」** Many apps do not connect to OpenAI directly. They send requests through its API（应用程序接口，即软件调用模型的付费通道）, and sometimes through a middle layer—a model router, AI gateway, or relay service—that forwards each request to OpenAI or another provider. OpenAI&\#x27;s usage policy is the set of terms that says what developers and resellers may do with its models.

**「What it means if you use a third-party service」** If you reach OpenAI&\#x27;s models through a third-party relay \(a service that forwards your requests to OpenAI for you\), an aggregator app or a gateway rather than through OpenAI directly, that provider will need approval before the November 2026 date. The announcement does not say whether unapproved services will lose access, so it is too early to tell whether any app you use will change or stop working. Nothing takes effect before November 20, 2026, and users have nothing to do right now beyond checking, if it matters to them, whether their provider is an authorized OpenAI partner.

**Tags**: `#OpenAI`, `#usage policy`, `#API access`, `#relays and gateways`, `#access restrictions`

---

<a id="item-tech-news-9"></a>
### [IBM announces Granite Speech 5.0 for transcription and translation](https://huggingface.co/blog/ibm-granite/granite-speech-5) ⭐️ 5.0/10

IBM announced Granite Speech 5.0, a new version of its speech model, which the company says transcribes audio, translates speech, and performs &quot;attribution&quot; more accurately and faster than before. The announcement names three capabilities — transcription \(turning speech into written text\), translation between languages, and attribution — but the available material does not explain what attribution covers or give any accuracy or speed figures to back the claims. It also gives no release date, price, license terms, or information on where the model can be downloaded or used. The &quot;5.0&quot; version number indicates earlier releases in the same line, but nothing in the material describes what specifically changed from them.

rss · Hugging Face Blog · Oct 21, 14:58

**「Background」** IBM already publishes Granite Speech models, a family of speech-recognition models that turn recorded audio into text. Those earlier models are available under the Apache 2.0 license, which allows free use in research and commercial products, and IBM says their training data is disclosed. Granite Speech 5.0 is the next release in that line.

**「What it means in practice」** For anyone who uses transcription or translation tools, there is not yet enough information to judge whether this version is worth switching to: without published accuracy results, a stated license, or a price, it cannot be compared with the service or software already in use. The practical next step is to wait for those details rather than plan around the announcement.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ibm.com/granite/docs/models/speech">Granite Speech | IBM Granite</a></li>

</ul>
</details>

**Tags**: `#IBM Granite`, `#speech recognition`, `#translation`, `#model release`

---

<a id="item-tech-news-10"></a>
### [Blogger Gave an AI Agent a Bank Card and 200+ Integrations](https://habr.com/ru/articles/1097430/?utm_campaign=1097430&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr author published a first-person account of giving an AI agent a dedicated bank card for payments, a phone, a browser, and access to more than 200 MCP and API integrations, then watching it carry out errands in the real world. MCP \(a standard way to plug outside services and tools into an AI model\) plus ordinary APIs let the agent reach shops, booking sites and other services rather than just chat. In the teaser text, the reported results are that the agent bought a plane ticket, built up a year&\#x27;s supply of coffee, and ended up on restaurant blacklists. The excerpt does not name the model, the specific tools, the costs, or how the experiments were set up, so the outcomes are the author&\#x27;s claims and cannot be checked from what is shown here.

rss · Habr AI · Oct 21, 15:27

**「Background」** An AI agent is software that does not just answer questions but carries out tasks itself — opening pages, filling in forms, paying. MCP \(Model Context Protocol\) is a shared plug standard that lets an agent connect to outside services such as shops, calendars or bank tools; each connection gives it one more &quot;tool&quot; to call. An earlier Habr post with a near-identical title \(15 October 2026\) ran a similar experiment and reported that 94% of the errors it recorded came from these external integrations — tools, MCP and APIs — rather than from the model&\#x27;s own reasoning; this new post extends that test by adding a payment card and a phone.

**「Why it matters if you use these tools」** The examples point to the practical line an agent crosses once it holds a payment card: it can spend real money and commit you to things without asking each time, and the reported restaurant blacklisting shows the fallout can land on your own name rather than the software&\#x27;s. The excerpt gives no detail on spending limits, confirmation steps or which actions ran unattended, so anyone hoping to copy the setup would need the full article to see what safeguards, if any, were in place.

<details><summary>References</summary>
<ul>
<li><a href="https://habr.com/ru/articles/1094906/">Где заканчивается самостоятельность ИИ-агента? Я дал ему ...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#MCP`, `#agent autonomy`, `#real-world automation`, `#tooling`

---

<a id="item-tech-news-11"></a>
### [Team Builds Claude Code Reviewer From Three Years of PR Comments](https://habr.com/ru/companies/otus/articles/1096720/?utm_campaign=1096720&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A development team writing on the Russian tech site Habr says it built an automatic code reviewer on top of Claude, Anthropic&\#x27;s AI assistant, by feeding it three years of their own comments on pull requests \(proposed code changes that colleagues read and critique before they are merged\). The team says the tool now raises the kinds of objections each colleague typically makes, and that its first version — which split the job among several AI agents \(separate AI workers each handling part of the task\) — turned out too expensive, so they redesigned it and cut the cost of a single review roughly sevenfold. The available text is only the article&\#x27;s introduction: it names no model version, prompts, settings, or method for measuring the cost, so the sevenfold figure is the team&\#x27;s own claim and cannot be checked or reproduced from what is published here.

rss · Habr AI · Oct 21, 13:05

**「Context: what a PR review is and why teams automate it」** A pull request \(PR\) is a proposed batch of code changes that teammates read and comment on before it is merged into the shared codebase; that reading is what developers call code review. Claude is Anthropic&\#x27;s AI assistant, one of the models a team can connect to its own tooling. The team&\#x27;s starting point was that AI assistants had sped up writing code, so review had become the slow step, and their idea was to turn three years of their own review comments into instructions so the AI would flag the same things each colleague usually flags.

**「What it means in practice」** For a team considering an AI reviewer, the account points to the organization&\#x27;s own archived review comments as the ingredient that makes the output sound like its engineers, rather than the choice of model alone. Because no configuration or measurement method is published, another team cannot copy the setup or confirm the cost saving before committing to it.

**Tags**: `#AI code review`, `#Claude`, `#developer tooling`, `#cost optimization`, `#PR workflow`

---

<a id="item-tech-news-12"></a>
### [Open-source Slightly Parallel dashboard announced for multi-project coding agents](https://habr.com/ru/articles/1097130/?utm_campaign=1097130&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A developer posting as nmar33 has published Slightly Parallel, an open-source program made of a local server plus a web interface, intended for people who run coding agents \(AI programs that write and edit code on their own\) across many projects at once. The post says it targets solo builders and heavy users of Claude Code, Codex and OpenCode — three existing tools in which an AI agent works inside a code project — with support for a fourth, ZCode, planned. It is said to run on Windows, Linux and macOS. The announcement itself contains no feature list, no installation steps and no evidence that the dashboard works; the only pointer is a GitHub repository link.

rss · Habr AI · Oct 21, 09:02

**「Background」** Coding agents such as Claude Code, Codex and OpenCode are programs that run in a text terminal and edit the files of a project on your behalf, following instructions you type. People who run several of them across different projects at once can lose track of which one is still working, which has finished, and which is waiting for an answer. Slightly Parallel is described on its GitHub page as a dashboard for coding agents that is self-hosted on one laptop — meaning it runs on your own machine rather than on a company&\#x27;s servers — and shows what Claude Code, Codex and OpenCode did in your projects.

**「What it means in practice」** Because the post gives no description of what the dashboard actually shows or how to set it up, anyone curious has to open the GitHub repository to learn anything beyond the platform support. The one confirmed design detail is that it runs as a local server with a browser interface, meaning it is installed on the user&\#x27;s own machine rather than offered as a hosted service.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/NMar33/slightly-parallel">GitHub - NMar33/slightly-parallel: A dashboard for coding ...</a></li>

</ul>
</details>

**Tags**: `#coding agents`, `#developer tooling`, `#open-source`, `#Claude Code`, `#Codex`

---

<a id="item-tech-news-13"></a>
### [How a ReAct agent works: model, tools, and control loop](https://habr.com/ru/articles/1096976/?utm_campaign=1096976&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A tutorial published on Habr on October 21 explains the internals of a ReAct agent — a setup in which a language model alternates between reasoning about a task and calling outside tools, such as reading a file or running a command. It describes which part chooses an action, which part executes the tool, and how the result is placed into the model&\#x27;s next request. The article then builds that loop in Python without any agent framework, and the example code is available on GitHub. It is an educational explainer, not a new model, product release, or pricing change.

rss · Habr AI · Oct 21, 05:46

**「What a ReAct agent is」** A ReAct agent is a setup in which a language model does not answer in a single pass. Instead, it repeatedly chooses a small action, such as reading a file or running a command, receives the result, and uses that result to decide the next step. The Habr tutorial walks through this control loop in Python without an agent framework, so readers can see which part is the model and which part is ordinary program code.

**「What it means in practice」** For someone building an agent, the tutorial shows that the core loop can be written directly in Python, so the behavior a framework normally hides becomes visible step by step. The code is teaching material rather than a packaged or supported tool, so it is best used to understand the mechanics before choosing a framework or writing your own.

**Tags**: `#agents`, `#ReAct`, `#Python`, `#developer tooling`, `#tutorial`

---

<a id="item-tech-news-14"></a>
### [Free local meeting transcription with T-one drafts and GigaAM cleanup](https://habr.com/ru/articles/1096758/?utm_campaign=1096758&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A developer has published a free meeting-transcription setup that runs entirely on the user&\#x27;s own computer, with no audio sent to an outside service. It uses two speech-recognition models: T-one writes live draft subtitles during the call, and GigaAM rewrites the transcript afterward. Across 2 hours 21 minutes of the author&\#x27;s work calls, the second pass corrected 11.9% of the draft&\#x27;s words and damaged 1.5%; on one recording the author replayed by hand, the result matched Deepgram, a paid cloud transcription service. The author also reports that the reference transcript was wrong in one of every four disputed spots, that a similar two-model arrangement which worked for a colleague made his own results worse, and provides cost calculations and a repository link for reproducing the setup.

rss · Habr AI · Oct 21, 04:16

**「Background」** The setup uses two downloadable speech-to-text models that run on the user&\#x27;s own computer, so meeting audio does not have to be sent to a cloud service. T-one, published by t-tech, is built to transcribe speech as it arrives; GigaAM, from Salute Developers, is a Russian-language speech model trained on more than 50,000 hours of audio and is used for the slower second pass. The author&\#x27;s earlier test found that T-one&\#x27;s live text arrived with about a one-second delay but had no punctuation and trailed cloud services, which is the gap the second pass is meant to close.

**「What it means in practice」** For anyone who wants meeting notes without handing recordings to a cloud provider, this is a reproducible option, but the good transcript only arrives after the call; the live captions remain a rough draft. Because the accuracy figures come from one author&\#x27;s calls and manual checks, users should test the setup on their own audio before relying on it for records.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/mkll/GigaAM-ai-speech">GitHub - mkll/GigaAM-ai-speech: Foundational Model for Speech ...</a></li>
<li><a href="https://huggingface.co/t-tech/T-one">t-tech/T-one · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#speech-recognition`, `#self-hosted-ai`, `#local-inference`, `#gigaam`, `#transcription-pipeline`

---

<a id="item-tech-news-15"></a>
### [A DIY 3D game engine for the ESP8266 chip, explained in code](https://habr.com/ru/articles/1097380/?utm_campaign=1097380&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A maker published the second part of a technical write-up about a 3D game engine running on the ESP8266, a cheap Wi-Fi microcontroller \(a small chip with very little memory and processing power\). The engine does not draw 3D shapes: it fires 320 straight rays across the screen, one per column, and calculates where each ray hits a wall on a 32-by-32 grid — a technique called raycasting. The program is written in C++ \(a programming language\) inside the Arduino IDE \(free software for writing and uploading programs to hobby boards\) and lives in a single file, with one setting, gameState, deciding which game is running; the article describes three games, while the author says the source file already contains five. The excerpt gives no link to the source code, no installation steps and no measured frame rate, so performance claims rest on the author&\#x27;s description.

rss · Habr DIY · Oct 21, 16:39

**「Context」** The ESP8266 is a low-cost chip that became popular for connecting homemade devices to Wi-Fi, and it has a tiny fraction of the memory of a phone. Raycasting is the shortcut that early 1990s first-person games such as Wolfenstein 3D used to suggest 3D on hardware that could not handle real 3D graphics: instead of building objects, the program measures the distance to walls along many lines of sight and draws vertical stripes whose height depends on that distance.

**「What it means in practice」** For hobbyists, the practical catch is that this installment is an explanation rather than a ready-to-run release: with no repository link or wiring and upload instructions in the excerpt, reproducing it means tracking down the first part and the source file. The numbers also set expectations — a 32-by-32 map and 320 rays produce a deliberately coarse image, closer to early 1990s games than to modern 3D.

**Tags**: `#ESP8266`, `#raycasting`, `#embedded C++`, `#Arduino`, `#microcontroller`

---

<a id="item-tech-news-16"></a>
### [Unconfirmed report: OpenAI models may come to Antigravity for paid users](https://telegram.me/AI_Copilot_Channel/926) ⭐️ 5.0/10

An unconfirmed post on a Telegram channel says OpenAI&\#x27;s AI models will be made available to paying users inside Antigravity, an AI coding tool, and that the change is expected to go public &quot;in the coming weeks.&quot; The post names no specific models, no prices, no usage limits and no exact date, and it cites no official OpenAI or Antigravity announcement. Treat this as a rumor until either company confirms it.

telegram · AI\_Copilot\_Channel · Oct 21, 18:57

**「Background」** Antigravity is Google&\#x27;s entry in the market for AI coding tools — software that takes instructions in plain language and writes or edits code on the user&\#x27;s behalf, competing with OpenAI&\#x27;s Codex, Anthropic&\#x27;s Claude Code and similar products. If the Telegram report holds, a Google-made tool would be carrying models from OpenAI, its main rival in that market, which is why the claim is notable rather than routine.

**「What it would mean in practice」** If it happens, people already paying for Antigravity would be able to pick OpenAI&\#x27;s models inside the same tool instead of switching to a separate product, though which models and what they would cost per month or per use is still unknown. There is nothing to act on yet: no plan change, download or setting is needed until an official notice appears.

<details><summary>References</summary>
<ul>
<li><a href="https://lushbinary.com/blog/ai-coding-agents-comparison-cursor-windsurf-claude-copilot-kiro-2026/">AI Coding Agents 2026: Claude Code vs Antigravity ... | Lushbinary</a></li>
<li><a href="https://blog.getbind.co/introducing-google-antigravity-overview-and-comparison-with-openai-codex/">Introducing Google Antigravity , Overview and Comparison with...</a></li>

</ul>
</details>

**Tags**: `#coding agents`, `#Antigravity`, `#OpenAI`, `#model availability`, `#subscription access`

---

<a id="item-tech-news-17"></a>
### [fal releases FLUX 3 Max, a faster video model with audio](https://fal.ai/flux-3-max) ⭐️ 5.0/10

fal and BFL released FLUX 3 Max, a new video-generation model for people who make short clips; it turns text or a still image into a short video with sound. In fal&\#x27;s own test, a 10-second 720p clip \(720p is a common HD resolution\) took 12.45 seconds to generate, versus 277.8 seconds for Seedance 2.5, or about 22 times faster. The model is available to try on fal, and a 720p second costs $0.0425 through Nov. 7, or $0.425 for a 10-second clip; after the promotion the same clip costs $1.70. fal also says the model sits in the leading group on Artificial Analysis&\#x27;s image-to-video comparison, alongside Seedance 2.5 and MiniMax H3.

telegram · ai\_newz · Oct 21, 18:35

**「Background」** FLUX 3 Max is a video-generation model from BFL, the company behind the FLUX image models, offered through fal, a cloud service that runs AI models for other companies. Text-to-video and image-to-video tools take a written prompt or a still picture and produce a short clip; this model also adds sound. fal says it further trained the model and sped up inference—the step where a trained model is run to produce an output—rather than only changing the price.

**「Practical impact」** If you want to try it, the promotional price makes a 10-second 720p clip cost $0.425 until Nov. 7, after which the same clip costs $1.70, four times as much; the 22x speed figure is fal&\#x27;s own measurement, not an independent result.

**Tags**: `#FLUX 3`, `#video generation`, `#fal.ai`, `#pricing`, `#benchmarks`

---

<a id="item-tech-news-18"></a>
### [AgentGrid, an open-source tool for running several AI coding agents together](https://github.com/naman10parikh/agentgrid) ⭐️ 5.0/10

A GitHub project called AgentGrid was announced in a Telegram post as an open-source tool for running several AI coding agents — programs that write and edit code on a user&\#x27;s behalf — from one place. The post says it works with Claude, Codex and Gemini and offers a single management screen, multi-terminal collaboration and status monitoring, replacing the manual switching between separate agents that developers did before. The announcement gives no version number, installation instructions, test results or other evidence that the tool works, and sends readers to two Telegram links for setup steps.

telegram · aipluscn · Oct 21, 01:50

**「What a coding agent is, and why running several is awkward」** A coding agent is a program that takes a plain-language request and then reads, edits and runs code on its own. Claude, Codex and Gemini are competing agents from different companies, each normally driven from its own command-line tool, so working with several at once has meant juggling separate terminal windows. The project&\#x27;s own listings describe AgentGrid as a way to &quot;spawn a grid of AI coding agents in one command,&quot; with status labels, sounds, presets and the ability to resume a session, published on npm as version 1.0.0 and requiring nothing beyond tmux — a utility that splits a terminal window into panes and keeps sessions running in the background.

**「What it means if you want to try it」** The post does not say what access or paid subscriptions to Claude, Codex or Gemini a user would need, or how the tool is installed, so the setup details live entirely behind the two Telegram links. With no published evidence that it works as described, it is worth inspecting on GitHub as an unverified project rather than treating it as a ready replacement for an existing coding setup.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/naman10parikh">naman 10 parikh (Naman Parikh ) · GitHub</a></li>
<li><a href="https://www.npmjs.com/package/@namanparikh/agentgrid">namanparikh/ agentgrid - npm</a></li>

</ul>
</details>

**Tags**: `#AI coding agents`, `#multi-model orchestration`, `#developer tooling`, `#open-source project`, `#GitHub`

---

<a id="item-tech-news-19"></a>
### [Major websites are blocking AI shopping and booking agents](http://cars.com/) ⭐️ 5.0/10

A widely circulated Chinese-language tech digest reports that several large websites are shutting out AI agents — software that browses and acts on a person&\#x27;s behalf, such as booking a flight or filling a shopping cart. According to the post, Yelp only lets agents in if they pay for a data-licensing program, Delta blocks agents from booking tickets for users, JPMorgan and Charles Schwab block agent access to customer accounts over security concerns, and Amazon has blocked agents from Meta, xAI, Instinct and OpenAI. It also says some sites, including Cars.com and Amtrak, could not be reached at all, and that Meta has instead partnered with retailers such as Walmart, Gap, Sephora and Best Buy. The post gives no dates, links or named sources for any of these blocks, so the specific companies and the scope of the restrictions should be treated as unconfirmed until the sites or the companies say so themselves.

telegram · aipluscn · Oct 21, 01:51

**「Background」** An AI agent is software that can operate a web browser and carry out a task—booking a trip, buying an item—by clicking through pages the way a person would. Because these agents act through the same public web pages as people, the websites themselves decide whether to let them in: The Verge reported on October 17, 2026 that Amazon, Yelp, Delta, JPMorgan Chase and Charles Schwab had shut agents out of the parts of their sites where customers sign in or complete transactions, and that Amazon began blocking Meta&\#x27;s Muse about 12 days after Meta launched it.

**「What it means in practice」** If the reported blocks hold, an agent you ask to book a Delta flight, check a JPMorgan or Schwab account, or shop on Amazon may simply fail or stall partway through, and you would have to finish the task yourself in a normal browser. The Yelp case points to a likely pattern: agent access may become something sites sell rather than something they allow by default, which could eventually show up as fees or as agents that only work with certain partners.

<details><summary>References</summary>
<ul>
<li><a href="https://aiweekly.co/alerts/amazon-yelp-delta-join-banks-blocking-third-party-ai-agents">Amazon, Yelp, Delta Join Banks Blocking Third-Party AI Agents</a></li>
<li><a href="https://pasqualepillitteri.it/en/news/25165/amazon-yelp-delta-jpmorgan-schwab-block-ai-agents">Amazon, Yelp, Delta, JPMorgan and Schwab confirm blocks on AI ...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#access restrictions`, `#web blocking`, `#industry analysis`

---

<a id="item-tech-news-20"></a>
### [Lawyer&\#x27;s letter targets plugin accused of farming WorkBuddy/CodeBuddy free quota](https://github.com/Ebony-Vinyl/dsh-our-free-model/issues/576) ⭐️ 5.0/10

A lawyer&\#x27;s letter has been posted as issue \#576 in the GitHub repository dsh-our-free-model, accusing the project of reverse-engineering \(taking apart a program to see how it works\) the client-side checks in WorkBuddy and CodeBuddy, two AI coding assistants. The letter says the plugin rewrote device-fingerprint modules to get past a block labeled &quot;11128&quot;, forged the official user-agent string \(the identifier an app sends to a server to say which program it is\) and product code, and used pools of many accounts to auto check in and collect free usage quota. It demands that the project stop within 3 days, be taken down and deleted within 7 days, and receive a written reply within 15 days, and it points to pull request \#574, which added more than 17,000 lines of code. The Telegram channel that shared it says it cannot verify the situation and suggests treating it as entertainment, so the accusations and the letter&\#x27;s authenticity are both unconfirmed.

telegram · zaihuapd · Oct 21, 09:40

**「What the two products are」** WorkBuddy is Tencent&\#x27;s AI assistant for office work, and CodeBuddy is a companion product from the same team; both give each account a free allowance of usage, and their client software checks that incoming requests really come from the official app. The repo at the centre of the dispute, dsh-our-free-model, collects ways to run top-tier AI models through DeepSeek Harness — a tool for running models on your own machine — without an account or a paid access key, and the plugin named in the letter is the part that disguised requests as official client traffic so they would be counted against that free allowance.

**「What it means for users」** If the vendor acts on the claims, people using third-party plugins or shared account pools to get free WorkBuddy or CodeBuddy quota should expect those routes to stop working, and accounts involved could be suspended. Nothing in the letter or the repository indicates an official change to pricing, quotas, or terms, so there is no confirmed action to take yet beyond knowing that client-side checks may be tightened.

<details><summary>References</summary>
<ul>
<li><a href="https://www.workbuddy.ai/">WorkBuddy - AI Agent for Everyday Office Work</a></li>
<li><a href="https://ai4coding.ru/solutions/Ebony-Vinyl-dsh-our-free-model">dsh - our - free - model — бесплатные фронтир-модели в DeepSeek...</a></li>

</ul>
</details>

**Tags**: `#access-restrictions`, `#quota-abuse`, `#legal-takedown`, `#coding-agents`, `#github`

---

<a id="item-tech-news-21"></a>
### [OpenAI models to be sold through Google Cloud&\#x27;s model catalog](https://openai.com/index/openai-models-google-cloud/) ⭐️ 5.0/10

OpenAI and Google Cloud said OpenAI&\#x27;s most capable models and Codex, its coding assistant that can carry out multi-step programming tasks, will be offered through Google Cloud&\#x27;s Model Garden, a catalog of AI models businesses can use on Google&\#x27;s cloud. Companies will be able to buy them through Google Cloud Marketplace and pay using committed Google Cloud spending, the prepaid amount many businesses already contract. The companies expect access to open &quot;within weeks,&quot; with later integration into Google&\#x27;s Antigravity and Gemini Agent tools; no date, prices, regions, or usage limits were given. OpenAI said Microsoft remains its primary cloud partner.

telegram · zaihuapd · Oct 21, 13:40

**「Background」** Google Cloud&\#x27;s Model Garden is a catalog where businesses can find and run AI models inside Google&\#x27;s cloud; Marketplace is the storefront where they buy such services on their existing Google Cloud bill. A spending commitment is a pre-agreed amount a company has promised to spend with Google Cloud, which it can then use up on purchases. OpenAI is a Google rival, so the change means businesses will be able to use OpenAI&\#x27;s most capable models and its Codex coding assistant—software that can carry out multi-step programming tasks—through that same Google channel.

**「What it means in practice」** For companies that already buy Google Cloud through committed contracts, this creates a way to pay for OpenAI models from that existing budget rather than through a separate purchase, once access opens. The announcement says nothing about individual ChatGPT subscriptions, and without prices or a firm date, buyers cannot yet plan a switch.

**Tags**: `#openai`, `#google-cloud`, `#codex`, `#model-availability`, `#enterprise-distribution`

---