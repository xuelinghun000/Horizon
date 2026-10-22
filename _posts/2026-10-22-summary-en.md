---
layout: default
title: "Horizon Summary: 2026-10-22 (EN)"
date: 2026-10-22
lang: en
---

> From 142 items, 22 important content pieces were selected

---

**Technology News**
1. [LiteLLM 1.107.0 on PyPI reported to install credential stealer and backdoor](#item-tech-news-1) ⭐️ 8.0/10
2. [Anthropic Opens US Waitlist for Claude Duet Agent App](#item-tech-news-2) ⭐️ 8.0/10
3. [Ollama adds Flint, a freely licensed 40-billion-parameter coding model, for Mac only](#item-tech-news-3) ⭐️ 7.0/10
4. [OpenAI keeps reused input cached longer in Codex, Work and developer access](#item-tech-news-4) ⭐️ 7.0/10
5. [Open-source Slightly Parallel dashboard targets people juggling many agent-run coding projects](#item-tech-news-5) ⭐️ 6.0/10
6. [Free offline meeting transcripts: live draft subtitles, then a cleaner rewrite](#item-tech-news-6) ⭐️ 6.0/10
7. [Railway breach exposes customer keys; LiteLLM 1.107.0 pulled over malicious code](#item-tech-news-7) ⭐️ 6.0/10
8. [Hey, a Third-Party Claude Code Plugin, Adds Markdown Task Tracking and AI Estimates](#item-tech-news-8) ⭐️ 6.0/10
9. [fal and BFL launch FLUX 3 Max, claimed ~22x faster than Seedance 2.5](#item-tech-news-9) ⭐️ 6.0/10
10. [new-api v1.0.0-rc.46 fixes a certificate flaw and billing errors](#item-tech-news-10) ⭐️ 5.0/10
11. [SemiAnalysis looks at Huawei&\#x27;s Ascend 950PR chip and DeepSeek&\#x27;s support for it](#item-tech-news-11) ⭐️ 5.0/10
12. [Hugging Face post claims 77% cut in small-model running cost by shrinking its vocabulary](#item-tech-news-12) ⭐️ 5.0/10
13. [IBM releases Granite Speech 5.0 for transcription, translation and speaker labeling](#item-tech-news-13) ⭐️ 5.0/10
14. [Developer Used Claude to Revive a Dead Sleep Tracker, With a 19-Day Dead End](#item-tech-news-14) ⭐️ 5.0/10
15. [Blogger Gave an AI Agent a Bank Card and 200+ Integrations](#item-tech-news-15) ⭐️ 5.0/10
16. [A tutorial explains how a ReAct agent turns model replies into tool calls](#item-tech-news-16) ⭐️ 5.0/10
17. [A 3D-style game engine squeezed onto an ESP8266, explained in code](#item-tech-news-17) ⭐️ 5.0/10
18. [OpenAI models to join Google Cloud&\#x27;s AI model catalog](#item-tech-news-18) ⭐️ 5.0/10
19. [Unverified Telegram post says OpenAI models are coming to Antigravity](#item-tech-news-19) ⭐️ 5.0/10
20. [Skills package for AI coding agents posted to GitHub with few details](#item-tech-news-20) ⭐️ 5.0/10
21. [Report claims major websites are blocking AI agents from browsing and buying](#item-tech-news-21) ⭐️ 5.0/10
22. [Anthropic says Opus 5.5 errors are fixed as it monitors recovery](#item-tech-news-22) ⭐️ 5.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [LiteLLM 1.107.0 on PyPI reported to install credential stealer and backdoor](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) ⭐️ 8.0/10

A security firm&\#x27;s report says version 1.107.0 of LiteLLM — a free, widely used tool that sits between an application and AI model providers, forwarding requests and holding the API keys \(the secret passwords that pay for model access\) — was published to PyPI \(the main public download site for Python software\) carrying malicious code. According to the report, that code steals credentials and opens a backdoor, meaning anyone who installed that exact version may have had keys and login details taken. The report is a third-party finding rather than a statement from the LiteLLM maintainers, and the item supplied here contains no vendor response. Anyone running LiteLLM should treat the version number as the thing to check first.

hackernews · abhisek · Oct 21, 14:00 · [Discussion](https://news.ycombinator.com/item?id=50181114)

**「Why this package matters」** LiteLLM is free, open-source software that developers install so their programs can send requests to many different AI models through one interface, and most of them get it from PyPI, the public warehouse where Python software is downloaded. That makes it a supply-chain target: an attacker does not need to break into a user&\#x27;s computer if they can slip code into the official download itself. According to the project&\#x27;s own security report, the malicious code was not in the tagged source code for version 1.107.0 — it was inserted into the build before the installable files were packaged, so anyone inspecting the public source repository would have seen nothing wrong.

**「What to do if you use it」** If your setup pulled LiteLLM 1.107.0, the practical steps are to move to a version released before it and to rotate every credential that installation could reach — model provider API keys, cloud keys, and any tokens stored in the same environment — because a stealer that ran once has already had its chance. Checking a lockfile or requirements file for the exact string &quot;1.107.0&quot; is the fastest way to know whether you were exposed; upgrading past the bad version without rotating keys does not undo a theft that already happened.

**「From the comments」** Commenters focused less on the malware itself than on how it got in: one noted the report&\#x27;s statement that three developers&\#x27; GitHub credentials were compromised, called that &quot;a little scary&quot; and systemic, and advised pinning LiteLLM to a version before 1.107.0 until further notice. Another pointed out this is the second significant LiteLLM supply-chain incident in roughly a year, citing a March write-up, and said they had already audited their projects to confirm LiteLLM was not in use.

<details><summary>References</summary>
<ul>
<li><a href="https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/">Compromised LiteLLM 1.107.0 on PyPI Installs a Credential ...</a></li>
<li><a href="https://github.com/BerriAI/litellm/issues/47826">[SECURITY] litellm 1.107.0 compromised (PyPI removed ... - GitHub</a></li>
<li><a href="https://www.mend.io/blog/litellm-1-107-0-compromised/">LiteLLM 1.107.0 Compromised: Credential Stealer - mend.io</a></li>

</ul>
</details>

**Tags**: `#LiteLLM`, `#supply-chain attack`, `#credential theft`, `#PyPI`, `#API proxy`

---

<a id="item-tech-news-2"></a>
### [Anthropic Opens US Waitlist for Claude Duet Agent App](https://claude.com/resources/articles/claude-duet) ⭐️ 8.0/10

Anthropic has opened a US-only early testing release of Claude Duet, a standalone app for iOS, Android and claude.ai that acts as a “proactive agent” — software that works on tasks in the background rather than waiting for each prompt. Access requires joining a waiting list and is limited to Anthropic’s Pro and Max subscribers; according to the source, Duet runs on the Claude Opus 5.5 model and shares the same usage allowance as other Claude products. Duet sends a daily briefing and can carry out tasks in the background, but before sending a message, making a payment, signing a document or deleting something, it shows the action and waits for approval. Securities trading and transfers between accounts are blocked even if the user authorizes them.

telegram · zaihuapd · Oct 22, 00:02

**「Background」** Anthropic&\#x27;s Claude is an AI assistant that people usually use by typing requests into a chat window. An “agent” is software that can take a goal and carry out several steps on its own, rather than only producing one reply. Pro and Max are Anthropic&\#x27;s paid Claude subscription plans, and a research preview is an early test release that may change before wider availability.

**「What changes for subscribers」** Duet&\#x27;s background work draws on the same subscription allowance as a user&\#x27;s existing Claude use, so delegating long-running tasks can eat into the quota they rely on for ordinary chats. The preview also carries over existing memory, saved skills and connected apps, meaning the agent starts with access to the same accounts and context — worth reviewing before letting it act — and for now only US Pro and Max subscribers can join the waitlist.

<details><summary>References</summary>
<ul>
<li><a href="https://www.testingcatalog.com/claude-duet/">Anthropic opens Claude Duet preview for US Pro and Max users</a></li>

</ul>
</details>

**Tags**: `#Claude`, `#Anthropic`, `#AI agents`, `#subscription access`, `#research preview`

---

<a id="item-tech-news-3"></a>
### [Ollama adds Flint, a freely licensed 40-billion-parameter coding model, for Mac only](https://github.com/ollama/ollama/releases/tag/v0.40.8) ⭐️ 7.0/10

Ollama, software for running AI models on your own computer, released version 0.40.8 with Flint, a new coding model from Recursive. Flint is a 40-billion-parameter model under the Apache 2.0 license \(free to use and modify\), and it uses a mixture-of-experts design \(each token, or small chunk of text, is routed through only part of the model, with about 2.5 billion parameters active at a time\). It has a 262,000-token context window \(the amount of code and conversation it can keep in view at once\) and is meant for AI coding assistants that work across a repository. For now it runs only on macOS, with support for other graphics cards promised in a later release; the reported scores of 54.9% on Terminal-Bench 2.1 and 74.2% on SWE-bench Verified come from Recursive&\#x27;s own evaluations, not independent testing.

github · github-actions\[bot\] · Oct 21, 16:20

**「Background」** Ollama is a free program that downloads AI models and runs them on your own machine instead of on a company&\#x27;s servers. Flint is a &quot;mixture-of-experts&quot; model, a design in which only a small slice of its 40 billion parameters \(the trained numbers that make up the model\) — about 2.5 billion — is used for each word it generates, so it costs less to run than its full size suggests. Its weights are published under Apache 2.0, a license that lets anyone use, modify, and ship the model commercially, and quantized \(size-reduced\) copies exist for Apple Silicon and other graphics chips.

**「What this means in practice」** Mac users can try Flint immediately with the command \`ollama run flint\`, while Windows and Linux users with other graphics cards cannot run this release&\#x27;s version yet and must wait for the promised follow-up. Because the benchmark scores are vendor-reported, treat them as a claim to test on your own code rather than a proven comparison with other coding models.

<details><summary>References</summary>
<ul>
<li><a href="https://ollama.com/library/flint">Flint is a 39.8 billion-parameter mixture-of-experts model from...</a></li>
<li><a href="https://openrouter.ai/recursive/flint-v1.0:free">Flint (free) - API Pricing &amp; Providers | OpenRouter</a></li>
<li><a href="https://huggingface.co/RecursiveSI/flint">RecursiveSI/ flint · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#ollama`, `#open-weight models`, `#coding models`, `#local inference`, `#model release`

---

<a id="item-tech-news-4"></a>
### [OpenAI keeps reused input cached longer in Codex, Work and developer access](https://telegram.me/ai_newz/4813) ⭐️ 7.0/10

OpenAI has made prompt caching persistent in Codex and ChatGPT Work and added a 12-hour cache-retention option to its API, the interface developers use to connect software to its models, according to a Telegram post from the channel ai\_newz. Prompt caching stores input the model has already processed so it does not have to process the same text again. For Codex and Work, the post says a session left idle for hours can resume without refilling the cache and using up extra subscription limits. For API users, the 12-hour option costs twice as much as writing to the existing 30-minute cache.

telegram · ai\_newz · Oct 21, 03:44

**「Background」** Prompt caching means keeping the text a model has already processed on hand, so repeated instructions or code do not have to be reprocessed from scratch. OpenAI introduced it in October 2024, offering a 50% discount and faster processing for reused input \(tool-1-2\). The new 12-hour API option extends how long that saved input is kept; the claim that Codex and Work keep it “forever” comes from a single post and was not yet reflected in OpenAI’s documentation, according to one review \(tool-1-1\).

**「What it means in practice」** People who use Codex or Work in long sessions should see fewer usage-limit surprises after breaks, because returning to a session no longer triggers a cache refill. API users who need long gaps covered can choose 12-hour retention, but they pay twice as much to store input in the cache, so the option only pays off if avoiding repeated processing saves more than that extra charge.

<details><summary>References</summary>
<ul>
<li><a href="https://explainx.ai/blog/openai-12-hour-prompt-caching-codex-work-cache-forever-claimed-vs-verified-2026">OpenAI 12-Hour Prompt Caching: 2.5x Write, Verified ...</a></li>
<li><a href="https://openai.com/index/api-prompt-caching/">Prompt Caching in the API - OpenAI</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#Codex`, `#prompt caching`, `#API pricing`, `#rate limits`

---

<a id="item-tech-news-5"></a>
### [Open-source Slightly Parallel dashboard targets people juggling many agent-run coding projects](https://habr.com/ru/articles/1097130/?utm_campaign=1097130&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A developer posting on Habr released Slightly Parallel, an open-source tool for people who run several software projects at once with coding agents — AI programs that write and edit code on their behalf. The tool is a local server \(a small program running on your own machine\) paired with a web interface \(a page you open in a browser\), and it is aimed at solo builders who use Claude Code, Codex or OpenCode, with support for ZCode listed as planned. It runs on Windows, Linux and macOS, and the code is public on GitHub. The post itself is only a short announcement with a link and an animated preview: it gives no feature list, no installation or setup steps, and no sign of how mature or widely used the tool is.

rss · Habr AI · Oct 21, 09:02

**「Background」** Coding agents are AI programs that carry out programming work from plain-language instructions; Claude Code, Codex and OpenCode are three of the best known, and OpenCode, for instance, runs as a terminal tool, a desktop app or an add-on inside a code editor \(tool-1-3\). Each agent normally works inside one project folder and reports back in its own window, so anyone running several projects at once has to switch between them to see what was done. The project&\#x27;s own one-line description frames Slightly Parallel as a dashboard, self-hosted on a single laptop, that shows what those three agents did across your projects \(tool-1-1\).

**「What it means in practice」** Because the code is public, you can open the repository and judge it yourself before relying on it. But with no setup instructions or usage evidence in the announcement, expect to spend time reading the code or experimenting rather than following a documented workflow, and treat it as something to try on a side project rather than a tool to build your daily routine around yet.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/NMar33/slightly-parallel">GitHub - NMar 33 / slightly - parallel : A dashboard for coding agents ...</a></li>
<li><a href="https://opencode.ai/docs">Intro | AI coding agent built for the terminal</a></li>

</ul>
</details>

**Tags**: `#coding-agents`, `#claude-code`, `#developer-tooling`, `#open-source`, `#multi-project-workflow`

---

<a id="item-tech-news-6"></a>
### [Free offline meeting transcripts: live draft subtitles, then a cleaner rewrite](https://habr.com/ru/articles/1096758/?utm_campaign=1096758&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A developer published a hands-on guide on Habr for transcribing meetings for free without sending audio to a company&\#x27;s servers. The setup runs two speech-recognition models in sequence: T-one produces live draft subtitles with about one second of delay but no punctuation, and after the call GigaAM re-transcribes the recording into a cleaner final text. Across 2 hours 21 minutes of the author&\#x27;s work calls, the final pass corrected 11.9% of the draft&\#x27;s words and damaged 1.5%, and on one recording he re-listened to by hand it matched Deepgram, a commercial cloud transcription service. He also reports that his reference transcript was wrong in one of every four disputed spots, and that a different two-model arrangement which had worked well for a colleague made his own results worse. The post includes comparison tables, a cost calculation, and repository links for reproducing the setup.

rss · Habr AI · Oct 21, 04:16

**「Background」** The write-up builds on an earlier test in which the author found that the speech-recognition model T-one could produce live Russian subtitles with about a one-second delay, but without punctuation and at lower quality than cloud services. The new setup adds a second pass: after the call, a second model called GigaAM re-listens to the recording and rewrites the rough draft. Both models run on the user&\#x27;s own machine, so the audio does not have to be sent to a paid transcription service on remote servers.

**「What it means if you try it」** Anyone who wants meeting notes without uploading recordings to a cloud service can copy this recipe, but should plan on proofreading: roughly one word in eight changed between the live draft and the final text, and the live subtitles arrive without punctuation, so they are readable but rough while the call is happening. The author&\#x27;s failed variant is the practical warning — the order and pairing of the two models mattered enough that a setup that worked for someone else degraded his output, so results should be checked on your own recordings before relying on them.

**Tags**: `#speech-to-text`, `#self-hosted`, `#GigaAM`, `#T-one`, `#workflow`

---

<a id="item-tech-news-7"></a>
### [Railway breach exposes customer keys; LiteLLM 1.107.0 pulled over malicious code](https://linux.do/u/lingo) ⭐️ 6.0/10

Railway, a service that hosts other companies&\#x27; applications, disclosed on 21 October 2026 that it had detected unusual activity in the systems storing customer environment variables — the configuration files that hold database passwords, API keys and other credentials — and has paused all deployments while it investigates. It is telling customers to rotate, meaning replace, those credentials. A forum roundup posted the same day also reports that LiteLLM 1.107.0, a widely used tool for routing requests to different AI models, was compromised to distribute malicious code and has since been removed from PyPI, the public library that Python software installs packages from. The same roundup lists a leaked private key at the Indian certificate authority eMudhra, severe remote-code-execution flaws in PHP, Node.js and GitLab \(CVE-2026-110264, rated 10.0 out of 10, meaning an unauthenticated attacker could run their own commands on a server\), and an emergency Chrome update to 156.0.8078.48. The post is a secondhand digest that links only to Railway&\#x27;s blog and a forum thread, so the LiteLLM claim in particular is unconfirmed and no technical detail is given.

telegram · linuxdo\_tg · Oct 21, 23:17

**「Context: what LiteLLM and Railway are」** LiteLLM is a free tool that sits between an app and AI providers, forwarding requests and holding API keys in one place; it is distributed as a Python package through PyPI, the public library that Python programs install from, so a tampered release can land on many machines at once. Railway is a hosting service where teams run apps and keep their settings — &quot;environment variables&quot; such as database passwords and API keys — stored on the platform&\#x27;s own systems. Both incidents are the same shape: the trusted supplier, not the customer, was the weak point, which is what people mean by a supply-chain attack.

**「What to do」** Anyone whose application runs on Railway should assume the keys stored there were seen by someone else: replace database passwords, API keys and access tokens, and review logs for unfamiliar activity before redeploying. Teams that install LiteLLM from PyPI should check whether version 1.107.0 entered their builds and pin to a version they know is clean rather than always taking the latest release.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/litellm-compromised-in-supply-chain.html">LiteLLM Compromised in Supply Chain Attack Delivering Credential...</a></li>
<li><a href="https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/">Compromised LiteLLM 1 . 107 . 0 on PyPI Installs a Credential Stealer...</a></li>
<li><a href="https://blog.railway.com/p/security-disclosure-wednesday-october-21st">Security Disclosure: Wednesday October 21st | Railway Blog</a></li>

</ul>
</details>

**Tags**: `#supply-chain-attack`, `#LiteLLM`, `#API keys and credentials`, `#security advisory`, `#Railway`

---

<a id="item-tech-news-8"></a>
### [Hey, a Third-Party Claude Code Plugin, Adds Markdown Task Tracking and AI Estimates](https://github.com/keenkim1202/Hey) ⭐️ 6.0/10

A developer has published &quot;Hey,&quot; a small add-on for Claude Code — Anthropic&\#x27;s tool that lets an AI model read, write and edit code from the command line — that keeps a to-do list in plain Markdown text files and asks the model to estimate how long tasks will take. According to a Telegram post about the project, it installs through Claude Code&\#x27;s plugin marketplace \(a catalog of community-made add-ons\) and adds commands such as /hey-ledger for task logging and /wassup for status checks. Its scripts are written in Python using only the standard library, meaning no extra packages need to be installed, while the estimation and task-handling logic is left to the model to read and carry out. The post offers no installation walkthrough beyond the marketplace mention, no version or maintenance information, and no evidence that the estimates are accurate, so the tool is best treated as something a Claude Code user could try rather than a proven improvement.

telegram · aipluscn · Oct 21, 07:10

**「Background」** Claude Code is Anthropic&\#x27;s coding assistant that runs in a text terminal and makes changes to a user&\#x27;s files on request; like other such tools, it accepts add-ons called plugins, which are installed from a marketplace and add extra commands. Hey is one of those add-ons, and its own repository listing describes it as running a day off a single Markdown ledger — a plain-text file with light formatting that both people and the model can read — with a morning briefing, an evening record, and estimates. That listing shows one star, so this is a small, early project rather than one with a track record.

**「What it means if you use Claude Code」** Hey is a community plugin, not one Anthropic built, and third-party plugins are listed separately in Claude Code&\#x27;s plugin marketplace, so installing it means opting into code Anthropic did not write — worth a look at the repository first. Its Python scripts use only the standard library, so there is nothing extra to install alongside it. The post gives no evidence that its estimates are accurate, so treat the numbers it produces as suggestions to check rather than planning figures.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/topics/task-management?l=python&amp;o=desc&amp;s=updated">task-management · GitHub Topics · GitHub</a></li>
<li><a href="https://claude.com/marketplace/plugins">Plugins | Claude Marketplace | Claude by Anthropic</a></li>
<li><a href="https://github.com/anthropics/claude-plugins-official">GitHub - anthropics/ claude - plugins -official: Official...</a></li>

</ul>
</details>

**Tags**: `#Claude Code`, `#developer tooling`, `#plugins`, `#task management`, `#open source`

---

<a id="item-tech-news-9"></a>
### [fal and BFL launch FLUX 3 Max, claimed ~22x faster than Seedance 2.5](https://fal.ai/flux-3-max) ⭐️ 6.0/10

fal and Black Forest Labs released FLUX 3 Max, a model that turns a text prompt or a still image into a short video with sound; fal says it further trained the model and sped up inference, the step where a trained model actually produces output. In fal&\#x27;s own test, a 10-second 720p clip takes 12.45 seconds to generate, against 277.8 seconds for the competing Seedance 2.5 — about 22 times faster, though this is the vendor&\#x27;s measurement rather than an independent one. On Artificial Analysis&\#x27;s image-to-video leaderboard the model sits in the leading group alongside Seedance 2.5 and MiniMax H3. Pricing is promotional until November 7: $0.0425 per second of 720p video, or $0.425 for a 10-second clip, after which the same clip costs $1.70.

telegram · ai\_newz · Oct 21, 18:35

**「Background」** fal is a service that hosts AI models and lets people run them without managing their own computers; BFL is the company behind the FLUX model family. FLUX 3 Max is a video generator: it takes a text prompt or a still image and produces a short clip with sound. The speed comparison concerns inference — the step where a trained model actually generates the output — after fal and BFL retrained the model and optimized how it runs.

**「What it means in practice」** Anyone generating video through fal faces a fourfold price rise after November 7, from $0.425 to $1.70 for a 10-second 720p clip, so trying many variations is far cheaper during the promotional window. If the speed holds outside fal&\#x27;s own test, the wait per clip drops from several minutes to roughly a dozen seconds, which changes how many attempts fit into one working session.

**Tags**: `#FLUX`, `#video generation`, `#fal.ai`, `#pricing`, `#model release`

---

<a id="item-tech-news-10"></a>
### [new-api v1.0.0-rc.46 fixes a certificate flaw and billing errors](https://github.com/QuantumNous/new-api/releases/tag/v1.0.0-rc.46) ⭐️ 5.0/10

new-api, a self-hosted panel that relays requests to different AI model providers, released v1.0.0-rc.46, a near-final test build, with a fix for CVE-2026-111943 \(a publicly tracked security vulnerability\) and a warning to upgrade soon. The release now runs on Go 1.26.10, the version of the programming language used to build it; its certificate checks will reject a small set of intermediate certificates \(certificates that sit between a site&\#x27;s own certificate and the trusted root\) that are no longer trusted, and anyone building from source must also use Go 1.26.10. It also adds Resend as an email option alongside SMTP \(the usual protocol for sending email\), shows cache usage next to total token counts \(the units providers use to meter text\), and supports Alibaba&\#x27;s qwen3-vl-embedding model for turning images and text into vectors \(numeric representations used for search and comparison\). Billing and channel fixes include reserving the higher price before retrying a task on a more expensive provider route, accepting a single Kling key, and showing a DeepSeek balance in yuan when the dollar wallet is empty.

github · Calcium-Ion · Oct 21, 16:25

**「Context」** new-api is a self-hosted control panel that puts several AI model providers behind one address and handles keys, billing, and retries; this is a release candidate, a test build ahead of the stable 1.0.0 release. The security fix involves the Go programming language&\#x27;s certificate checks: a set of intermediate certificates — the middle links in a site&\#x27;s trust chain — were compromised, and Go 1.26.10 rejects them.

**「What it means」** If you run new-api, upgrade to v1.0.0-rc.46 and rebuild with Go 1.26.10 if you compile it yourself; the release notes say to do so soon because of the certificate flaw. People who retry tasks across provider routes should also check balances, because a retry to a more expensive route now reserves the extra cost first and will not run if the balance cannot cover it.

<details><summary>References</summary>
<ul>
<li><a href="https://app.opencve.io/cve/CVE-2026-111943">CVE-2026-111943 - Vulnerability Details - OpenCVE</a></li>
<li><a href="https://access.redhat.com/security/cve/cve-2026-111943">CVE-2026-111943 - Red Hat Customer Portal</a></li>

</ul>
</details>

**Tags**: `#api-relay`, `#security-cve`, `#release-notes`, `#self-hosted`, `#qwen`

---

<a id="item-tech-news-11"></a>
### [SemiAnalysis looks at Huawei&\#x27;s Ascend 950PR chip and DeepSeek&\#x27;s support for it](https://newsletter.semianalysis.com/p/huawei-deepseek) ⭐️ 5.0/10

The research firm SemiAnalysis published a piece on Huawei&\#x27;s Ascend 950PR — a chip in Huawei&\#x27;s line of AI accelerators, the hardware that runs AI models — together with an analysis of a DeepSeek model version it labels DSv4.1 Flash and of DeepSeek&\#x27;s work to make its models run on Ascend hardware. Only the article&\#x27;s section list is available here: it says the piece contains microbenchmarks \(small, targeted speed tests\) of the 950PR, but the text on hand gives no measured results, prices, ship dates, or capacity limits. Nothing in the available material confirms how the chip or the model actually performs.

rss · Semianalysis · Oct 21, 17:34

**「Background」** Huawei&\#x27;s Ascend is the company&\#x27;s own line of AI chips — the hardware that runs a trained model and produces answers, a job that Nvidia&\#x27;s chips have largely handled. DeepSeek is a Chinese AI lab whose models are widely used both as chat products and as downloadable software that others build on. A May 2026 write-up on dev.to described DeepSeek&\#x27;s V4 model, released the previous month, as the first top-tier model to be fully validated for inference \(running a finished model to generate answers\) on the Ascend 950PR — the same model-and-chip pairing this SemiAnalysis piece examines.

**「What changes for people calling DeepSeek&\#x27;s API」** If a tool or app you use is still configured with the older model name \`deepseek-v4-flash\`, it will keep working, but it is no longer running that model. DeepSeek&\#x27;s API documentation says the legacy names are still accepted while the underlying models have been retired, and those requests are now answered by DeepSeek-V4.1-Flash-1017 and billed at the Flash price. The practical consequence is that the model name in your settings no longer tells you what actually produced an answer, so cost and output quality should be checked against the V4.1 Flash snapshot dated October 17, 2026 rather than assumed from the old label.

<details><summary>References</summary>
<ul>
<li><a href="https://dev.to/lanternproton/deepseek-v4-on-huaweis-ascend-950-a-real-stress-test-for-chinas-ai-chip-ecosystem-ook">DeepSeek V4 on Huawei&#x27;s Ascend 950: A Real Stress Test for ...</a></li>
<li><a href="https://api-docs.deepseek.com/quick_start/pricing?tool=deepseek">Models &amp; Pricing | DeepSeek API Docs</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4.1-flash-1017">DeepSeek V4.1 Flash 1017 - API Pricing &amp; Benchmarks</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#Huawei Ascend`, `#AI infrastructure`, `#model analysis`, `#inference`

---

<a id="item-tech-news-12"></a>
### [Hugging Face post claims 77% cut in small-model running cost by shrinking its vocabulary](https://huggingface.co/blog/Dharma-AI/vocabx-vocabulary-specialization) ⭐️ 5.0/10

A blog post published on Hugging Face on 21 October 2026 by Dharma-AI describes a technique it calls &quot;VocabX&quot; and claims it cuts inference cost — the computing bill for running a trained model so it can answer requests — by 77% in real applications. The idea is to specialize a small language model&\#x27;s vocabulary: the fixed list of word fragments the model reads and writes. The available description of the post does not include a model release, a pricing or usage-quota change, or a downloadable tool, and the 77% figure is the authors&\#x27; own claim rather than an independently measured result. Readers should treat the number as a reported outcome for the authors&\#x27; own setup, not a general guarantee.

rss · Hugging Face Blog · Oct 21, 17:35

**「Background」** Small language models are compact text generators built to run more cheaply than large ones. They process text as tokens—chunks of characters or words—taken from a fixed vocabulary, and every token costs computing work when the model is running \(inference\). The blog post&\#x27;s idea is to tailor that vocabulary to a narrow domain so common terms take fewer tokens, which is the lever it claims can lower the cost of each answer.

**「What it means in practice」** For anyone running a small model on their own hardware, the figure that matters is cost per request on their own text, and a vocabulary tuned to one narrow domain is not a general-purpose saving. A model&\#x27;s word list is built into how it reads and writes, so this kind of specialization typically means retraining or adapting the model rather than flipping a setting — worth asking about before assuming the 77% applies to an existing deployment.

**Tags**: `#SLM`, `#inference cost`, `#vocabulary specialization`, `#model optimization`, `#Hugging Face`

---

<a id="item-tech-news-13"></a>
### [IBM releases Granite Speech 5.0 for transcription, translation and speaker labeling](https://huggingface.co/blog/ibm-granite/granite-speech-5) ⭐️ 5.0/10

IBM has published Granite Speech 5.0, a new version of its speech model, on Hugging Face, a site where companies share AI models for others to download and use. IBM says the update turns speech into text, translates it, and labels which person is speaking — often called speaker attribution — more accurately and faster than earlier versions. The announcement as supplied gives no benchmark numbers, no licensing terms, and no cost for running the model, so the accuracy and speed claims have not been independently checked.

rss · Hugging Face Blog · Oct 21, 14:58

**「Background」** Granite Speech is IBM&\#x27;s line of compact speech models: software that listens to audio and writes it out as text, either in the original language \(transcription\) or in another one \(translation\). IBM&\#x27;s documentation lists English, French, German, Spanish, Portuguese and Japanese among the languages the family handles. The 5.0 release is an update to an existing collection rather than a new product line: it adds a 2-billion-parameter model \(parameter count is a rough measure of model size\) and revises two models already in use, a small, fast transcription model and a model from the earlier 4.1 generation.

**「What it means if you want to use it」** For anyone building speech-to-text into a product, the main Granite Speech 5.0 model carries the Apache 2.0 license, which permits commercial use without paying IBM, and at 470 million parameters it is small enough to run on ordinary servers rather than a rack of specialized chips. The catch is that IBM also published a second 470M model trained on additional restricted-use data that is limited to non-commercial applications, so a team deploying it should confirm which of the two versions it downloaded. The headline figures — about 12,600 seconds of audio processed per second of computing, and a 5.00% word error rate, meaning roughly one word in twenty transcribed incorrectly — are IBM&\#x27;s own claims and have not been independently verified.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ibm.com/granite/docs/models/speech">Granite Speech | IBM Granite</a></li>
<li><a href="https://huggingface.co/blog/ibm-granite/granite-speech-5">Granite Speech 5.0: Transcribe, Translate, and Attribute more ...</a></li>
<li><a href="https://www.orcarouter.ai/blog/granite-speech-5-0-470m-turboctc-apache-explained">Granite Speech 5 . 0 470M TurboCTC: Apache-2.0 ASR, 12.6K RTFx</a></li>
<li><a href="https://slator.com/ibm-granite-speech-5-transcription-model/">IBM Releases Granite Speech 5 . 0 Model</a></li>

</ul>
</details>

**Tags**: `#speech-model`, `#ibm-granite`, `#model-release`, `#open-weight`, `#transcription`

---

<a id="item-tech-news-14"></a>
### [Developer Used Claude to Revive a Dead Sleep Tracker, With a 19-Day Dead End](https://habr.com/ru/articles/1097526/?utm_campaign=1097526&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A developer named Joseph Sperrier says he spent six weeks using Claude, an AI assistant, to bring a discontinued Hello Sense sleep tracker back to life, according to a Habr article that currently runs only as a short teaser. Hello, the company that made the device, closed in 2017 and shut down its cloud service with it, leaving the tracker unable to do the things that depended on the company&\#x27;s servers. The account describes wiring work, a wrong firmware install \(firmware is the built-in software that runs a device&\#x27;s hardware\), and a 19-day stretch in which he and the AI were stuck together. The teaser offers no code, parts list, or step-by-step instructions, so the revival has not been independently verified or reproduced.

rss · Habr AI · Oct 21, 19:23

**「Why the device needed reviving」** Hello was a startup whose Sense device sat by the bed and tracked sleep along with room light, noise, temperature and humidity, and woke you at a lighter point in your sleep cycle. It raised $40 million and was valued at $250–300 million in 2015, but the company shut down in 2017 — and because the tracker depended on Hello&\#x27;s own servers to work, owners were left with hardware that could no longer do its job.

**「What it means for owners of abandoned gadgets」** This is a story, not a repair guide: anyone hoping to copy it should note that the work involved custom wiring and firmware replacement over six weeks, not a simple app fix, and the published teaser gives no steps to follow. The practical lesson for people with discontinued connected devices is that the hardware may still power on, but features that relied on the manufacturer&\#x27;s servers will not come back unless someone is willing to replace the software that talks to those servers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.josephspurrier.com/ai-revives-a-dead-sleep-company">AI Revives a Dead Sleep Company | Joseph Spurrier</a></li>
<li><a href="https://www.youtube.com/watch?v=1VBMrLPwXjU">Unboxing the Sense sleep tracker from Hello - YouTube</a></li>
<li><a href="https://techcrunch.com/2015/06/15/sense-sleep-tracker-maker-hello-valued-between-250m-and-300m-in-latest-funding-round/">Sense Sleep Tracker Maker Hello Valued Between... | TechCrunch</a></li>

</ul>
</details>

**Tags**: `#Claude`, `#Hello Sense`, `#hardware revival`, `#AI-assisted repair`, `#reverse engineering`

---

<a id="item-tech-news-15"></a>
### [Blogger Gave an AI Agent a Bank Card and 200+ Integrations](https://habr.com/ru/articles/1097430/?utm_campaign=1097430&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A first-person post on the Russian tech site Habr describes giving an AI agent its own bank card, a phone number, a browser and access to more than 200 MCP connections, then setting it loose on real errands. MCP \(Model Context Protocol, a common way to plug an AI assistant into outside tools and services\) is what let the agent reach booking sites, shops and other services. In the opening of the article, the author says the agent bought her a plane ticket, stockpiled a year&\#x27;s supply of coffee and got itself blacklisted by restaurants. The excerpt published so far is only a teaser: it does not name the model, describe how the agent was configured, give costs, or report how often it failed, so the claims cannot be checked or repeated from what is available.

rss · Habr AI · Oct 21, 15:27

**「Background」** An AI agent is a model that is given a goal and the ability to act toward it — opening pages, calling services, paying — instead of only answering questions. MCP \(Model Context Protocol\) is a shared standard that lets a model plug into outside tools and services through one common connector rather than a custom hook for each; &quot;200+ MCP&quot; means the agent had that many such connectors within reach. Handing an agent a payment card is an active area of experiment: SecurityLab reported in May 2026 that mathematician Hannah Fry gave an AI agent real errands, internet access and a card number, and the run quickly slipped out of control.

**「What to take from the setup」** The one concrete practice visible in the teaser is that the author did not hand over her own card: she created a separate card used only for the agent, which is the arrangement that lets a person set a spending limit and cut the agent off without freezing their own money. Whether that was enough to contain the damage is exactly what the missing details would show.

<details><summary>References</summary>
<ul>
<li><a href="https://www.securitylab.ru/news/572386.php">ИИ дали банковскую карту и доступ в интернет. Эксперимент ...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#MCP`, `#agent autonomy`, `#real-world testing`, `#LLM tooling`

---

<a id="item-tech-news-16"></a>
### [A tutorial explains how a ReAct agent turns model replies into tool calls](https://habr.com/ru/articles/1096976/?utm_campaign=1096976&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr tutorial by NullPilot walks through the internals of a ReAct agent — a setup in which a language model alternates between reasoning in text and requesting an action, such as reading a file or running a command. The article first shows the message exchange as diagrams, then builds the control loop in Python without any agent framework, and links a runnable example on GitHub. It answers three questions step by step: which part picks the action, which part actually executes the tool, and how the tool&\#x27;s output is fed back into the model&\#x27;s next request. This is an educational explainer, not a new model, product release, or pricing change.

rss · Habr AI · Oct 21, 05:46

**「Where the ReAct pattern comes from」** ReAct is not a product but a pattern described in a 2022 research paper, which proposed having a language model write out its reasoning and then take a concrete action, such as a search, with the result fed back in for the next step. Before that, the paper notes, reasoning and acting were mostly studied as separate topics rather than combined in one loop. Most agent software since then, including coding assistants, follows the same thought-then-action cycle, which is why a walkthrough of one agent&\#x27;s internals applies to many tools.

**「Why a reader might use it」** The piece makes concrete that the model never executes anything itself: a separate program runs the tool and pastes the result into the following request, which is why an agent can repeat a failing command or stall when a tool returns nothing useful. Because the example is written without a framework and published on GitHub, readers can copy it and adapt the loop to their own tools rather than treating an agent as a black box.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2210.03629">[2210.03629] ReAct: Synergizing Reasoning and Acting in ...</a></li>

</ul>
</details>

**Tags**: `#ReAct`, `#LLM agents`, `#Python`, `#tool use`, `#GitHub code`

---

<a id="item-tech-news-17"></a>
### [A 3D-style game engine squeezed onto an ESP8266, explained in code](https://habr.com/ru/articles/1097380/?utm_campaign=1097380&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr write-up takes apart the code behind a small 3D-style game engine running on the ESP8266, a cheap Wi-Fi microcontroller \(a complete tiny computer on one chip\). The engine is written in C++ inside the Arduino IDE and lives entirely in a single file. It does not draw 3D shapes at all: it fires 320 rays out from the player&\#x27;s position and checks where each one crosses a 32×32 grid of walls, a technique called raycasting. The project contains three games, five in the source file, switched between by a state variable named gameState. The portion of the article available here is only the introduction, so it does not include the code itself, a parts list, setup instructions, or any demonstration that the build actually runs.

rss · Habr DIY · Oct 21, 16:39

**「Background」** Raycasting is a shortcut to a 3D look: instead of building and drawing 3D shapes, the program fires a fan of straight lines \(rays\) out from the player&\#x27;s position and draws a vertical strip wherever each one hits a wall. It is a common choice for very weak hardware — an earlier Hackaday project used the same idea to run a 3D view on an Arduino driving a 32×16 LED panel — because the ESP8266 is a cheap Wi-Fi chip with a tiny fraction of a phone&\#x27;s computing power and memory, which is why the article&\#x27;s numbers \(320 rays against a 32×32 map grid\) stay so small. This is the second part of the author&\#x27;s write-up: the first part covered the hardware and case assembly, and this one goes into the source code.

**「What it takes to copy it」** Anyone hoping to rebuild the project needs more than this installment: the author says the hardware, the case assembly and part of the software were covered in the first part, and the excerpt here stops before the code, wiring or a working demo. Treat the piece as an explanation of the approach rather than a build guide until the full text is available.

<details><summary>References</summary>
<ul>
<li><a href="https://hackaday.io/project/12274-arduino-led-raycaster">Arduino LED Raycaster | Hackaday.io</a></li>

</ul>
</details>

**Tags**: `#ESP8266`, `#raycasting`, `#Arduino`, `#embedded graphics`, `#game development`

---

<a id="item-tech-news-18"></a>
### [OpenAI models to join Google Cloud&\#x27;s AI model catalog](https://openai.com/index/openai-models-google-cloud/) ⭐️ 5.0/10

OpenAI and Google Cloud announced that OpenAI&\#x27;s most advanced models and Codex, its AI coding assistant for multi-step programming tasks, will be offered through Google Cloud&\#x27;s Model Garden, a catalog where businesses can find and use third-party AI models. Companies will be able to buy them on Google Cloud Marketplace and pay using money they have already committed to spend with Google Cloud. The models are also planned to appear in Google&\#x27;s Antigravity and Gemini Agent products within weeks, but the announcement gave no prices, model versions, usage limits, or exact start date; OpenAI said Microsoft remains its main cloud partner.

telegram · zaihuapd · Oct 21, 13:40

**「Why this is a change」** Model Garden is Google Cloud&\#x27;s catalog of AI models that businesses can pick from and run inside Google&\#x27;s cloud, paying through the Google Cloud spending they have already committed to rather than a separate contract. OpenAI&\#x27;s models have until now been sold mainly through Microsoft&\#x27;s Azure cloud, and OpenAI says Microsoft remains its primary cloud partner. Google&\#x27;s own announcement describes it as the only large cloud provider offering Gemini, Claude and GPT models side by side.

**「What changes for buyers」** For a company that already commits to spending a set amount with Google Cloud each year, this creates a way to buy OpenAI models from that same budget instead of signing a separate contract with OpenAI, but the option cannot be planned around until prices and availability are published.

<details><summary>References</summary>
<ul>
<li><a href="https://cloud.google.com/blog/products/ai-machine-learning/google-cloud-brings-openai-models-to-customers">Google Cloud brings OpenAI models to customers | Google Cloud ...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#Google Cloud`, `#Model Garden`, `#Codex`, `#enterprise access`

---

<a id="item-tech-news-19"></a>
### [Unverified Telegram post says OpenAI models are coming to Antigravity](https://telegram.me/AI_Copilot_Channel/926) ⭐️ 5.0/10

A single Telegram post from the channel AI\_Copilot\_Channel claims that OpenAI&\#x27;s models will be made available to paying users inside Antigravity, Google&\#x27;s coding tool that can carry out multi-step tasks on its own \(often called an &quot;agentic&quot; coding environment\). The post says the change is expected to be publicly available within the next few weeks. It gives no model names, no pricing, no usage limits, and no date, and it links to no source or confirmation from Google or OpenAI. Treat this as an unconfirmed report rather than an announced feature.

telegram · AI\_Copilot\_Channel · Oct 21, 18:57

**「What Antigravity and Codex are」** Antigravity is Google&\#x27;s AI coding environment — a code editor in which AI &quot;agents&quot; can plan and carry out multi-step programming tasks with limited supervision. OpenAI, the company behind ChatGPT, sells a competing coding agent called Codex, and the two are commonly reviewed side by side as rival tools \(Lushbinary&\#x27;s 2026 comparison, for instance, pits Antigravity against Codex and other coding agents\). A report that OpenAI&\#x27;s models would appear inside a Google product therefore describes a crossing of the usual company lines, which is why the claim is being passed around even though the post itself names no models, prices, or usage limits.

**「Why it matters to users」** If it happens, people already paying for Antigravity could choose OpenAI&\#x27;s models inside the same tool instead of only Google&\#x27;s own, which matters when one model handles a coding task better than another. Until Google or OpenAI confirms it, there is nothing to plan around: no date, no price, and no indication of whether existing subscriptions would cover the added models or require a separate payment.

<details><summary>References</summary>
<ul>
<li><a href="https://lushbinary.com/blog/ai-coding-agents-comparison-cursor-windsurf-claude-copilot-kiro-2026/">AI Coding Agents 2026: Claude Code vs Antigravity ... | Lushbinary</a></li>
<li><a href="https://blog.getbind.co/introducing-google-antigravity-overview-and-comparison-with-openai-codex/">Introducing Google Antigravity , Overview and Comparison with...</a></li>

</ul>
</details>

**Tags**: `#antigravity`, `#openai`, `#coding-agents`, `#model-availability`, `#subscription-access`

---

<a id="item-tech-news-20"></a>
### [Skills package for AI coding agents posted to GitHub with few details](https://github.com/Maik326/rayfernando-skills) ⭐️ 5.0/10

A Telegram post on October 21 announced a &quot;skills package&quot; for AI coding agents — add-on instruction modules that coding assistants such as Claude Code, Cursor and Codex can load — and pointed readers to a GitHub repository. The post names modules including waves, running-bug-review-board and bootstrap-ios, says the package works across several platforms and supports parallel verification, and attributes it to Ray Fernando&\#x27;s team. It gives no install commands, no version numbers and no evidence that the modules actually work, and the linked repository sits under a GitHub account named Maik326 rather than an account identified with Ray Fernando.

telegram · aipluscn · Oct 21, 01:50

**「What a &\#x27;skill file&\#x27; is」** AI coding agents — programs such as Claude Code, Cursor and Codex that write and edit code on a user&\#x27;s behalf inside an editor or terminal — can be extended with &quot;skill files&quot;: plain instruction documents that tell the agent how to carry out one specific workflow. The linked repository is Ray Fernando&\#x27;s collection of such files, and a skills directory listing describes its first entry, running-bug-review-board, as a real-user quality-check loop built around a &quot;Bug Review Board,&quot; with six skills published in the repository. That listing also says the skills are installed with a command-line installer \(a small tool run by typing a command\) for Claude Code, Cursor and other agents.

**「What it means if you use these tools」** For someone already using Claude Code, Cursor or Codex, this is a link to inspect rather than something to add to a working setup on trust: the post lists no setup steps, no compatibility with specific tool versions, and no sign of testing by anyone outside the project. Check the repository&\#x27;s own documentation and recent activity before installing anything from it.

<details><summary>References</summary>
<ul>
<li><a href="https://skillsllm.com/skill/rayfernando-skills">rayfernando - skills - AI Agents on GitHub | SkillsLLM</a></li>
<li><a href="https://github.com/RayFernando1337/rayfernando-skills">RayFernando1337/ rayfernando - skills : Ray Fernando &#x27;s collection of...</a></li>
<li><a href="https://www.skills.sh/rayfernando1337">rayfernando 1337 — Agent skills</a></li>

</ul>
</details>

**Tags**: `#AI coding agents`, `#Claude Code`, `#Cursor`, `#Codex`, `#GitHub project`

---

<a id="item-tech-news-21"></a>
### [Report claims major websites are blocking AI agents from browsing and buying](http://cars.com/) ⭐️ 5.0/10

A Chinese-language Telegram post says large websites are shutting out AI agents — software that can carry out tasks on a site for you, such as filling in forms, booking a flight or buying an item. The post lists Yelp as allowing only agents that pay for its data licensing program \(a paid deal to use the site&\#x27;s listings\), Delta Air Lines as blocking agents from booking tickets for users, and JPMorgan and Charles Schwab as blocking agents from user accounts for security reasons. It also says Amazon has blocked agents from Meta&\#x27;s Muse, xAI&\#x27;s Grok, Instinct and OpenAI&\#x27;s Dots, that Cars.com and Amtrak could not be reached by agents, and that Meta instead struck partnerships with retailers including Walmart, Gap, Sephora and Best Buy. The post gives no dates, links or statements from the companies named, so the specific blocks are unconfirmed and should be treated as the author&\#x27;s account rather than verified fact.

telegram · aipluscn · Oct 21, 01:51

**「Background」** An &quot;AI agent&quot; here means software that drives a web browser on someone&\#x27;s behalf — clicking, filling in forms and finishing tasks like booking a table or buying shoes — instead of only answering questions. OpenAI, Meta and xAI have each released &quot;always-on&quot; versions \(Dots, Muse and Grok Bot\) that keep working after the user closes their laptop. Websites have long run anti-bot checks to separate software from human visitors, and those same checks are what now catch agents; TechCrunch reported in early October 2026 that a proposed new standard is meant to let sites recognize and admit approved agents.

**「What it means in practice」** If the account is accurate, people using browser-based AI assistants should expect routine errands — booking travel, checking a bank balance, shopping on a major retailer — to fail on some sites, with the assistant unable to load the page or complete the task. The fallback is to do those steps yourself, or to use the retailer-specific partnerships that Meta is reported to have set up instead of open browsing.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theverge.com/ai-artificial-intelligence/1013195/ai-agents-blocked-web">Websites are closing their doors to AI agents | The Verge</a></li>
<li><a href="https://techcrunch.com/2026/10/06/the-next-hurdle-for-ai-agents-getting-websites-to-let-them-in/">The next hurdle for AI agents : getting websites to let... | TechCrunch</a></li>
<li><a href="https://www.youtube.com/watch?v=EbPNAa4uxQQ">Don’t Give Muse , Dots or Grok Bot Access Until You... - YouTube</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#access restrictions`, `#agentic browsing`, `#platform policy`

---

<a id="item-tech-news-22"></a>
### [Anthropic says Opus 5.5 errors are fixed as it monitors recovery](https://telegram.me/aipluscn/3164) ⭐️ 5.0/10

Anthropic&\#x27;s Opus 5.5 — a version of the company&\#x27;s Claude AI model, which other software can call on to answer questions and generate text — returned errors for users, according to a brief report. Anthropic said it has applied a fix and is watching to confirm the service recovers, and that it is still investigating what caused the problem. The report gave no detail on the type of error, how long it lasted, which regions or customers were affected, or whether the problem is now fully resolved.

telegram · aipluscn · Oct 21, 02:06

**「Background」** Anthropic sells access to Claude, its family of AI models, and Opus is the name of its most capable tier; the source says Opus 5.5 had already gone live before this incident. Users of these models do not run them on their own machines — they send requests over the internet to Anthropic&\#x27;s servers, which do the work and send back an answer. That means a fault on Anthropic&\#x27;s side hits every customer at once, no matter what hardware or software they have, and the only thing they can do is wait for the company to fix it.

**「What it means in practice」** For anyone whose product or internal tool sends requests to Opus 5.5, requests made during the incident may have failed or stalled, and the report does not say which customers were hit. Until Anthropic confirms the service is fully back, retrying failed requests or falling back to another model is the practical safeguard.

**Tags**: `#Anthropic`, `#Claude`, `#service outage`, `#model availability`

---