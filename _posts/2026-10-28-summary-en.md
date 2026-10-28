---
layout: default
title: "Horizon Summary: 2026-10-28 (EN)"
date: 2026-10-28
lang: en
---

> From 112 items, 17 important content pieces were selected

---

**Technology News**
1. [Codex CLI user finds the reported 828,400-token context limit is not a hard cap](#item-tech-news-1) ⭐️ 8.0/10
2. [Codex Command-Line Tool 0.165.0 Adds Google Cloud AI and Mid-Conversation Reasoning Control](#item-tech-news-2) ⭐️ 7.0/10
3. [aiedit: an open-source code editor that hides closed files from AI](#item-tech-news-3) ⭐️ 7.0/10
4. [Keystone 1.0 puts AI model choice and access keys in one place](#item-tech-news-4) ⭐️ 6.0/10
5. [Part 3 of a build log for a robot driven by a language model](#item-tech-news-5) ⭐️ 6.0/10
6. [OpenAI publishes Codex CLI alpha 0.166.0-alpha.1 without release notes](#item-tech-news-6) ⭐️ 5.0/10
7. [Survival LLM puts a small AI assistant and emergency library on your own PC](#item-tech-news-7) ⭐️ 5.0/10
8. [Game Boy Color emulator runs on a GitHub Universe conference badge](#item-tech-news-8) ⭐️ 5.0/10
9. [Liquid AI&\#x27;s LFM3 aims at custom models that handle text and images](#item-tech-news-9) ⭐️ 5.0/10
10. [Habr post claims 125 tokens/s coding agent on a 16 GB RTX 4070 Ti SUPER](#item-tech-news-10) ⭐️ 5.0/10
11. [LiteLLM briefly carried a credential stealer; Railway revoked API tokens](#item-tech-news-11) ⭐️ 5.0/10
12. [Habr post previews a test of few-shot examples on GLM and Haiku coding agents](#item-tech-news-12) ⭐️ 5.0/10
13. [Forum fix: run the &\#x27;dsh&\#x27; desktop agent unelevated so its shell can start](#item-tech-news-13) ⭐️ 5.0/10

**Financial News**
1. [EU to charge €2 fee on non-EU parcels from November 1](#item-finance-news-1) ⭐️ 7.0/10
2. [Microsoft offers voluntary buyouts to about 60,000 employees](#item-finance-news-2) ⭐️ 7.0/10
3. [China Sets IPTV Startup Rules: Live TV First, No Ads](#item-finance-news-3) ⭐️ 7.0/10
4. [泡泡玛特三季度营收近腰斩，Labubu 热度消退](#item-finance-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Codex CLI user finds the reported 828,400-token context limit is not a hard cap](https://habr.com/ru/articles/1100196/?utm_campaign=1100196&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 8.0/10

A Codex CLI user reports that the context window — the amount of text, measured in tokens \(word-like fragments\), that a model can consider at once — does not match the number set in the tool&\#x27;s settings file. In ~/.codex/config.toml the author set model\_context\_window = 1000000, but on the GPT-6.1 Sol model Codex displayed 828,400 for every task. By writing a custom model catalog \(a local file that tells the tool which models exist and what limits to apply\), the author raised the displayed figure to 900,000 and ran a synthetic input of 890,547 tokens with checkpoints to confirm it was processed. A control run of 888,330 tokens also went through without that edit, at the reported 828,400 window. The tests were run on 27 October 2026 with Codex CLI 0.163.0 through a ChatGPT subscription; this is one user&\#x27;s blog post, not an OpenAI confirmation, and some data comes from September trials on GPT-6 Astra.

rss · Habr AI · Oct 27, 15:11

**「Background」** Codex CLI is OpenAI’s coding assistant that runs on a user’s own computer, and some of its behavior can be adjusted in a settings file called config.toml. The “context window” is the amount of text the model can consider at once, counted in tokens, which are pieces of text roughly the size of word fragments. Codex lets users set that window with model\_context\_window, but users have previously reported that the setting is not always honored, including in a GitHub issue from around April 2026.

**「What it means in practice」** For someone using Codex CLI on long files or large codebases, the number the tool displays is not a reliable ceiling: inputs larger than that number can still be accepted, and raising the displayed limit requires editing a model catalog rather than the main settings file. The author&\#x27;s figures are tied to version 0.163.0 and a ChatGPT subscription, so results on other versions or plans may differ.

<details><summary>References</summary>
<ul>
<li><a href="https://www.alexdunlop.com/writing/codex-cli-config-toml">Codex CLI config . toml (2026): What Actually Works With Non-OpenAI...</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai/ codex : Lightweight coding agent that runs in your...</a></li>

</ul>
</details>

**Tags**: `#Codex CLI`, `#context window`, `#GPT-6.1 Sol`, `#config.toml`, `#model catalog`

---

<a id="item-tech-news-2"></a>
### [Codex Command-Line Tool 0.165.0 Adds Google Cloud AI and Mid-Conversation Reasoning Control](https://github.com/openai/codex/releases/tag/rust-v0.165.0) ⭐️ 7.0/10

OpenAI released Codex CLI rust-v0.165.0, an update to its command-line coding assistant \(software you run in a text window to get AI help writing and editing code\). The release adds a built-in connection to Google Cloud&\#x27;s Vertex AI service, selected with the setting model\_provider = &quot;gcp&quot;, and lists a new model called GPT-6.1 Terra in its list of usable models; the release notes give no further details about that model. For supported models, it enables mid-conversation changes to reasoning effort \(how much computation the model spends before answering\) by default, and makes memory v2—the newer version of its feature for remembering information between conversations—the default for new profiles, with support for importing memories from other AI agents. It also adds a repository filter and directory grouping to the session picker for people working across linked worktrees \(separate working copies of the same code repository\), and fixes bugs involving default approval settings, queued messages restarting after an interrupt or a switch to Plan mode, and marketplace URL validation.

github · github-actions\[bot\] · Oct 27, 20:09

**「Background」** Codex CLI is OpenAI&\#x27;s coding assistant for the command line \(the text-only terminal window where you type commands\); it can read project files, propose edits, and execute commands on your behalf. This release is labeled 0.165.0 and follows 0.164.0, so it is an incremental update to that same tool rather than a new product.

**「What changes for existing users」** The new memory system switches on only for fresh profiles, so upgrading an existing Codex install leaves your current memory setup untouched; you would need to start a fresh profile to get it, and to try pulling in memories saved by another coding agent. Separately, anyone whose company already pays for AI through Google Cloud can now point Codex at Vertex AI by setting \`model\_provider = &quot;gcp&quot;\`, keeping usage on that existing cloud bill instead of arranging separate OpenAI access.

**Tags**: `#codex-cli`, `#openai`, `#coding-agents`, `#model-catalog`, `#vertex-ai`

---

<a id="item-tech-news-3"></a>
### [aiedit: an open-source code editor that hides closed files from AI](https://habr.com/ru/articles/1100200/?utm_campaign=1100200&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 7.0/10

A developer has released aiedit, an open-source desktop code editor written in Python, in which AI models can work across an entire project but never receive the parts the user has marked as closed. Whole files can be closed, and so can individual lines, and the exclusion is carried out by the editor&\#x27;s own code rather than by an instruction written into the prompt \(the text sent to the model\) — closed code simply never appears in the request. The project is published under the MIT license, a permissive open-source license that allows anyone to use and modify it. The author states plainly that the code it produces still trails Claude Code, a competing AI coding tool, even when both run on the same underlying model, and says the post explains why further down.

rss · Habr AI · Oct 27, 15:16

**「How these assistants usually handle private code」** Most AI coding assistants work by reading files from a project and sending the relevant text over the internet to an AI model. Keeping a file private usually depends on an instruction the model may or may not follow, or on never opening that file. aiedit is built around a different arrangement: the editor itself decides what text goes into the message sent to the AI service, so a closed file or line can be left out before anything is sent.

**「What it changes in practice」** For someone who wants AI help on a codebase without handing over passwords, keys, or proprietary files, this offers a guarantee enforced by the tool itself instead of one the model is merely asked to honor. The costs are real: you have to move your work into a separate desktop editor, and by the author&\#x27;s own account the results are weaker than Claude Code&\#x27;s on the same model.

**Tags**: `#coding agents`, `#AI code editor`, `#open source`, `#context privacy`, `#developer tooling`

---

<a id="item-tech-news-4"></a>
### [Keystone 1.0 puts AI model choice and access keys in one place](https://habr.com/ru/articles/1099790/?utm_campaign=1099790&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

Keystone 1.0 \(KTMS\), a free program released under the open-source Apache 2.0 license, sits between an organization’s apps and AI model services so the model name and each AI company’s sign-in keys live in one place rather than in every app. It runs on the organization’s own computers, is not tied to one AI company’s models, and can send each request to a commercial model or to a local graphics chip \(GPU, the processor that can also run AI models on-site\), depending on how complex the app says the task is. Version 1.0 shipped with a web administration console, ktms-admin, and a usage-cost tracker, light-tokenmeter, that counts tokens \(the chunks of text AI services bill for\); all three are written in Go, a programming language. The author claims about 7 MiB \(roughly 7 megabytes\) of memory use when idle and says the programming interface will stay compatible for later 1-series releases, but the feature list in the post describes version 1.3 rather than 1.0, and the supplied excerpt includes no independent performance tests or installation steps.

rss · Habr AI · Oct 27, 08:31

**「Background」** An LLM gateway \(a large-language-model gateway\) is a self-hosted intermediary between an application and AI providers: the application sends one request to the gateway, and the gateway decides which vendor&\#x27;s model to call, which secret key to use, and whether to send the work to a local graphics card. Keystone&\#x27;s premise is that when ten separate services each embed a model name and vendor key, every model change or key rotation has to be repeated ten times; centralizing that choice in one service avoids the rewrite. The project&\#x27;s own site describes it as Apache-2.0-licensed software that routes by effort, falls back between providers and caps spending.

**「What changes in practice」** For a team running several apps against AI models, changing a default model or replacing an AI company’s key becomes one change in Keystone instead of edits in every app, and the cost tracker gives one place to see usage. Anyone installing the 1.0 release should check whether a feature they need is in 1.0 or only in the version 1.3 feature list described in the post.

<details><summary>References</summary>
<ul>
<li><a href="https://ai-process.dev/">ai - process — open-source infrastructure for production LLMs</a></li>

</ul>
</details>

**Tags**: `#LLM gateway`, `#API proxy`, `#open source`, `#cost tracking`, `#self-hosted`

---

<a id="item-tech-news-5"></a>
### [Part 3 of a build log for a robot driven by a language model](https://habr.com/ru/articles/1089244/?utm_campaign=1089244&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

The third instalment of a Russian-language build log about a homemade robot controlled by a large language model \(the kind of AI software behind chatbots\) has been published on Habr. The author says the series runs to seventeen sections and about two hundred hours of work; this part is described as entirely technical and covers a compass and a gyroscope as sensors, PID control \(a feedback routine that continuously corrects the robot&\#x27;s steering toward a target\), an agent loop \(the repeating cycle in which the model reads sensor readings, chooses an action and sees the result\), four different LLM providers — companies whose language-model services the robot can call — and ffmpeg, a tool for processing video. The supplied excerpt is only a teaser: it does not confirm that source code, a parts list or reproducible installation steps are included, and there is no independent evidence that the build works as described.

rss · Habr AI · Oct 27, 06:41

**「Earlier context」** This is the third installment in a series by the Habr author stg34, whose earlier article — titled, roughly, &quot;I released a neural network into the real world, and it stopped being funny&quot; — set up the premise of letting a language model act outside a screen, in physical space. That first piece was the story of the experiment; this one is the workshop manual, walking through sensors, motor correction \(PID, a standard feedback method that constantly adjusts output based on how far a device has drifted from its target\) and the loop that lets the model decide what to do next. A public code repository under the same author&\#x27;s name, robo-llm, holds experiment files dated April 2026, though the teaser itself does not confirm a parts list or step-by-step install instructions.

**「What it means for would-be builders」** Anyone hoping to copy the robot should treat this as a narrative build log rather than instructions: the excerpt names the topics covered but gives no parts list, wiring details, source code or setup steps, so whether the project can be reproduced has to be checked in the full article.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/stg34/robo-llm/tree/main">GitHub - stg34/robo-llm</a></li>
<li><a href="https://habr.com/ru/users/stg34/articles/">Статьи / Профиль stg 34 / Хабр</a></li>

</ul>
</details>

**Tags**: `#LLM robotics`, `#DIY robot`, `#PID control`, `#agent loop`, `#hardware`

---

<a id="item-tech-news-6"></a>
### [OpenAI publishes Codex CLI alpha 0.166.0-alpha.1 without release notes](https://github.com/openai/codex/releases/tag/rust-v0.166.0-alpha.1) ⭐️ 5.0/10

OpenAI has published version 0.166.0-alpha.1 of Codex CLI, a command-line tool that lets an AI model read and edit code from a terminal window. The release page contains only the version number: there are no release notes, no changelog, and no description of what changed. The “alpha” label means this is an early test build. Without notes, people who use Codex CLI cannot tell what was added, fixed, or broken.

github · github-actions\[bot\] · Oct 27, 01:33

**「What Codex CLI and an alpha build mean」** Codex CLI is OpenAI’s coding tool for the command line — a text interface where a user types instructions instead of clicking buttons. An “alpha” tag marks an early test build released before a stable version; it signals that the software is still changing, not what the build actually does.

**「What it means in practice」** Anyone testing Codex CLI early builds cannot judge from the release page whether this version is worth installing or whether it is more fragile than the previous one. The practical choice is to wait for release notes or a later non-alpha version unless they are deliberately testing unfinished software.

**Tags**: `#codex-cli`, `#coding-agents`, `#openai`, `#release`, `#developer-tooling`

---

<a id="item-tech-news-7"></a>
### [Survival LLM puts a small AI assistant and emergency library on your own PC](https://www.brangus.io/survival-llm) ⭐️ 5.0/10

A project called Survival LLM packages a small AI model — a large language model, meaning software that answers questions in plain text — together with an offline library of emergency reference material, so the whole thing runs on a user&\#x27;s own laptop or desktop without an internet connection. It was posted to Hacker News, where the main objection was that a plain searchable archive of the same sources, such as the offline Wikipedia reader Kiwix, would need far less computing power and could not invent wrong answers. One commenter, quoting the project&\#x27;s own comparison table, said an 8-billion-parameter IBM Granite model \(parameter count is a rough measure of a model&\#x27;s size and capability\) running on a Mac or PC with 16–31 GB of memory answered 14 of 22 test questions correctly, with a model file of about 6 GB. The posted material itself gave no detail on which model ships, the hardware requirements or the installation steps.

hackernews · Luc · Oct 27, 19:55 · [Discussion](https://news.ycombinator.com/item?id=50264853)

**「Background」** Most AI assistants work as cloud services: a question travels to a company&\#x27;s servers, and the answer comes back over the internet. A “local” AI model is a copy of the answer-generating software that runs on the user&\#x27;s own computer; the project says it keeps both that model and an emergency reference library on the machine, works with the internet off, and shows the source of each answer \(tool-1-1, tool-1-2\).

**「What it means in practice」** For anyone building an offline emergency kit, the deciding factor is the machine: the configuration described in the comments needs 16 GB of memory or more, which rules out older or cheaper laptops, while a static offline archive runs on almost anything with storage. Given the reported accuracy, the sensible use is to let the assistant point you to relevant passages in the bundled library and then read those passages yourself, rather than treating its answer as the authority.

**「What commenters argued」** One commenter argued the model is safer and more useful as a search tool than as an adviser — using it to surface relevant text without trusting its conclusions — and said this helps most when you do not know the right question to ask. Several others, including daniel\_iversen and rnd0, countered that a searchable static copy of sources such as WikiMed, MedlinePlus, Ready.gov and the CDC would be simpler, lighter on hardware and more reliable; daniel\_iversen suggested a middle ground where the software asks &quot;what&\#x27;s going on?&quot; and then raises things you might not have thought of. jvanderbot pointed to Project Nomad as an existing preconfigured alternative, and saaaaaam&\#x27;s reaction was that at 14 of 22 correct, &quot;just buy some books&quot; — opinions offered in the thread, not measured findings.

<details><summary>References</summary>
<ul>
<li><a href="https://www.brangus.io/survival-llm">Survival LLM</a></li>
<li><a href="https://github.com/anonnerdfrenzy/survival-llm">anonnerdfrenzy/ survival - llm : A free AI assistant and survival library ...</a></li>

</ul>
</details>

**Tags**: `#local-llm`, `#self-hosted`, `#offline-ai`, `#open-weight-models`, `#emergency-preparedness`

---

<a id="item-tech-news-8"></a>
### [Game Boy Color emulator runs on a GitHub Universe conference badge](https://simonwillison.net/2026/Oct/27/game-boy-color-on-my-conference-badge/) ⭐️ 5.0/10

At GitHub Universe this week, developer Steve Francia got emulators — software that imitates older game consoles — for the NES, Game Boy and Game Boy Color running on the conference&\#x27;s attendee badge, which Simon Willison describes as a full color-screen computer. Willison photographed the badge playing The Legend of Zelda: Link&\#x27;s Awakening in full color, with the badge turned upside down so the touch buttons built into its body work as a game controller. Francia built the emulators with help from Gemini, Google&\#x27;s AI assistant. To actually play, you need to obtain the game&\#x27;s ROM file \(a copy of the original cartridge&\#x27;s data\) yourself, and Willison&\#x27;s post is a short pointer to Francia&\#x27;s write-up rather than a set of installation instructions.

rss · Simon Willison · Oct 27, 19:34

**「What an emulator and a ROM are」** An emulator is software that imitates a game console&\#x27;s hardware so that games written for that console can run on a different machine. A ROM is a copy of a game&\#x27;s data, which the emulator loads and plays. The GitHub Universe badge is a small color-screen computer handed out to people attending GitHub&\#x27;s annual developer conference, and Willison notes that last year&\#x27;s badge was also a color-screen computer.

**Tags**: `#emulation`, `#game-boy`, `#hardware-hacking`, `#gemini`, `#conference-badge`

---

<a id="item-tech-news-9"></a>
### [Liquid AI&\#x27;s LFM3 aims at custom models that handle text and images](https://huggingface.co/blog/LiquidAI/lfm3) ⭐️ 5.0/10

Liquid AI published a Hugging Face blog post presenting LFM3 as a starting point for building specialized multimodal models — models that handle more than one kind of input, such as text and images. The material available for this item contains only the post&\#x27;s title, so the model&\#x27;s size, its license, whether the trained model files \(weights\) can be downloaded, and any performance results are unconfirmed. It is also unknown what hardware would be needed to run or fine-tune it, so readers cannot yet tell whether it is usable outside Liquid AI&\#x27;s own setup.

rss · Hugging Face Blog · Oct 27, 17:16

**「What Liquid AI&\#x27;s LFM family is」** Liquid AI markets its &quot;Liquid Foundation Models&quot; as compact systems built to run on a phone, laptop or other local device rather than in a data center, alongside larger cloud versions. &quot;Open weights&quot; means the trained model files are published so anyone can download, run or adapt them, and &quot;2B-class&quot; means roughly two billion parameters — the internal numbers set during training that largely determine a model&\#x27;s size and how much computing power it needs. LFM3&\#x27;s distinguishing move is putting text, image and video, audio, and &quot;decision&quot; outputs \(results tuned for picking an action rather than writing prose\) on one shared base model, so a single starting point can be adapted into many specialized versions.

**「What it means for local AI apps」** Because these are 2B-class models — small enough that Liquid AI says each can be fine-tuned \(retrained on your own data\) on a single graphics card — someone building a phone or laptop app can customize one and ship it running on the device itself instead of paying a cloud service per request. The limit is spelled out on the model page: the 1.7B text version is &quot;not recommended for agentic coding or complex multi-step reasoning&quot; because of its small size, and knowledge-heavy tasks are meant to be paired with search or lookup tools, so it is a fit for narrow, specialized jobs rather than a drop-in replacement for a large assistant.

<details><summary>References</summary>
<ul>
<li><a href="https://www.liquid.ai/blog/lfm3">Introducing LFM3: Every Modality for Specialized Intelligence</a></li>
<li><a href="https://explainx.ai/blog/liquid-ai-lfm3-open-weight-2b-family-text-vision-audio-omni-decision-models-2026">Liquid AI LFM3: Open 2B Models for Text, Vision, Audio ...</a></li>
<li><a href="https://www.liquid.ai/models">Liquid Foundation Models | Liquid AI</a></li>
<li><a href="https://www.liquid.ai/blog/lfm3">Introducing LFM 3 : Every Modality for Specialized Intelligence | Liquid AI</a></li>
<li><a href="https://huggingface.co/LiquidAI/LFM3-1.7B">LiquidAI/ LFM 3 -1.7B · Hugging Face</a></li>
<li><a href="https://www.marktechpost.com/2026/10/27/liquid-ai-lfm3-open-weight-2b-multimodal-models/">Liquid AI Releases LFM 3 : 6 Open-Weight 2B-Class Multimodal Models</a></li>

</ul>
</details>

**Tags**: `#lfm3`, `#liquid-ai`, `#open-weight-models`, `#multimodal`, `#fine-tuning`

---

<a id="item-tech-news-10"></a>
### [Habr post claims 125 tokens/s coding agent on a 16 GB RTX 4070 Ti SUPER](https://habr.com/ru/articles/1099962/?utm_campaign=1099962&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr article&\#x27;s introduction claims that a local language model can run as a full coding agent at 125 tokens per second — tokens being the word fragments a model generates — on an Nvidia GeForce RTX 4070 Ti SUPER, a consumer graphics card with 16 GB of video memory \(VRAM, the card&\#x27;s own working memory\). The only comparison given is that a &quot;smart&quot; dense model, meaning one that uses all of its parameters for every token, which the article calls &quot;Qwen 3.8 27B,&quot; produces 10–20 tokens per second on the same card, while the author sets 100–150 tokens per second as the comfort threshold for agent work. The author also cites a GaugeDB survey putting 16 GB cards at 27.21% of the market and a price of about $900 for this model. The supplied excerpt stops at that setup: it does not name the model actually used for the 125 figure, how it was compressed to fit in 16 GB, which runtime ran it, or any configuration details, so the result cannot be verified or reproduced from the text available.

rss · Habr AI · Oct 27, 09:20

**「Why speed is the bottleneck on a 16 GB card」** A local model has to sit entirely in the graphics card&\#x27;s own memory \(VRAM\), so a 16 GB card — the most common size among desktop owners, according to the survey figure the author cites — sets a hard ceiling on which models fit and how fast they run. A &quot;dense&quot; model such as Qwen 3.8 27B uses all of its roughly 27 billion parameters for every token \(a word fragment, the unit in which these speeds are counted\), which is why the author measured only 10–20 tokens per second; published setup guides for running that model on 16 GB cards depend on memory-saving configurations and extra acceleration tricks rather than running it at full size \[tool-1-2\], and a third-party test of a compressed 27B model reported about 68–70 tokens per second \[tool-1-1\]. Speed matters here because a coding agent writes and re-reads large amounts of text for a single task, so the wait grows with every step. The supplied excerpt ends before naming the model, the software used to run it, or the settings, so the 125 tokens-per-second figure cannot yet be checked or reproduced.

**「Why the missing details matter」** Because 16 GB is described as the most common amount of video memory among desktop users, the claim applies to a large group of ordinary home machines rather than an exotic setup. For anyone hoping to copy it, the decisive facts are exactly the ones absent: which model was used, how it was shrunk to fit 16 GB, and which software ran it. Without those, a reader cannot tell whether their own card can reach 125 tokens per second or whether the figure depends on settings specific to the author&\#x27;s machine.

<details><summary>References</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=975ILFNTKfk">Is Bonsai 2 27 B REALLY 98% of Qwen 3 . 8 27 B fp 16 ? - YouTube</a></li>
<li><a href="https://codersera.com/blog/how-to-run-qwen-3-8-locally-2026/">How to Run Qwen 3 . 8 Locally : 27 B on 16 –24 GB GPUs (2026)</a></li>

</ul>
</details>

**Tags**: `#local-llm`, `#coding-agents`, `#gpu-inference`, `#open-weight-models`, `#consumer-hardware`

---

<a id="item-tech-news-11"></a>
### [LiteLLM briefly carried a credential stealer; Railway revoked API tokens](https://habr.com/ru/articles/1099718/?utm_campaign=1099718&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A release of LiteLLM—a reusable software component that lets applications connect to several AI services—that stole login credentials and access keys was available on PyPI, the main public catalog for Python add-on software, for less than two hours, according to a Russian-language security roundup. The same roundup says cloud hosting service Railway revoked all API tokens after an incident; API tokens are long key-like passwords that let software access online services, often paid ones. The excerpt does not name affected versions, identify who was compromised, or give cleanup steps, so it is not enough to determine which installs were exposed.

rss · Habr AI · Oct 27, 07:00

**「Background」** LiteLLM is a proxy layer: software that lets an application send requests to many different AI model providers through one connection, so it often holds the paid API keys for those services. Socket and Cybersecurity News identify the malicious release as LiteLLM 1.107.0, published to PyPI \(Python&\#x27;s public package repository\) and as a container image on October 21, 2026; a DEV Community timeline traces the opening to a publicly exposed LiteLLM master key \(an administrative credential\) five months earlier. The roundup also says Railway revoked all API tokens \(digital keys that applications use to access its platform\) after the incident, so customers had to replace them.

**「What to check if your tools run on LiteLLM」** LiteLLM is a piece of software companies place between their own apps and AI providers to hold and route API keys — the long password-like codes that let software use a paid AI service and bill whoever owns it. According to LiteLLM&\#x27;s own incident notice, version v1.107.0 was published to PyPI \(the main public repository for Python software packages\) and to Docker on the morning of October 21, 2026, and contained compiled malware that steals credentials and pulls in tools for running remote code; Datadog&\#x27;s security team attributes the release to compromised maintainer accounts. The practical consequence: anyone who installed or pulled that version, or whose vendor did, should assume the AI service keys on that machine were copied and stop using them. The source notes that Railway revoked all of its API tokens after the incident, and the same logic applies here — rotate the affected keys and confirm which version is actually installed rather than relying on an automatic upgrade having been undone. The excerpt gives no remediation steps of its own, so treat the vendor&\#x27;s notice as the authoritative checklist.

<details><summary>References</summary>
<ul>
<li><a href="https://dev.to/romdevin/leaked-litellm-master-key-exploited-to-compromise-github-release-malicious-pypi-and-container-dc4">Leaked LiteLLM Master Key Exploited to... - DEV Community</a></li>
<li><a href="https://socket.dev/blog/litellm-attack-timeline">New Evidence Shows LiteLLM Secret- Stealing Workflows... | Socket</a></li>
<li><a href="https://cybersecuritynews.com/litellm-compromised/">LiteLLM Compromised - Hackers Injected an Infostealer and RAT in...</a></li>
<li><a href="https://docs.litellm.ai/blog/security-incident-oct-21-2026">Contained: Oct 21, 2026 LiteLLM release v1.107.0 Compromised</a></li>
<li><a href="https://securitylabs.datadoghq.com/articles/litellm-compromised-pypi-docker/">LiteLLM supply chain compromise: What you need to know</a></li>

</ul>
</details>

**Tags**: `#litellm`, `#supply-chain-security`, `#api-keys`, `#llm-proxy`, `#security-roundup`

---

<a id="item-tech-news-12"></a>
### [Habr post previews a test of few-shot examples on GLM and Haiku coding agents](https://habr.com/ru/articles/1099792/?utm_campaign=1099792&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A Habr author published a short account of two small experiments: whether adding a handful of worked examples to a prompt — &quot;few-shot&quot; prompting — improves the code a model writes when it already has written specifications \(&quot;contracts&quot;\) and automated tests to check its work. The author says GLM \(a model family from the Chinese company Zhipu AI\) is their everyday &quot;workhorse&quot; for large implementation jobs but sometimes performs poorly, and that the second experiment covered GLM and Claude Haiku \(Anthropic&\#x27;s small, fast model\). The author explicitly states there is no academic rigor here. The text available so far is only the introduction: it contains no prompts, settings, numbers or results, so the claimed &quot;noticeable practical signal&quot; cannot be checked, and the author frames the work as a reason to continue testing on real projects rather than a finished finding.

rss · Habr AI · Oct 27, 04:30

**「Background: worked examples for coding agents」** “Few-shot” prompting means giving an AI model a handful of worked examples of a task before asking it to handle a new case. The Habr author already uses written contracts \(rules for what the code must do\) and automated checks \(tests that catch mistakes\) around an AI coding agent—software that carries out coding tasks with limited supervision—and ran two small tests to see whether adding examples on top improves output from GLM, a general-purpose AI model used for bulk implementation work, and Claude Haiku, a model from Anthropic&\#x27;s Claude family. The first test used models running on the author&\#x27;s own machine; the author explicitly says the exercise is not academically rigorous, and the supplied excerpt stops after the setup, with no examples, settings, or results.

**「Why it matters for users」** Anyone who relies on these models for coding should treat this as an open question rather than advice for now: until the prompts, test setup and measurements are published, there is no way to tell whether adding examples to a request actually reduces bad output, or by how much. The one practical takeaway is the setup the author describes — examples layered on top of written specifications plus automated tests — which is a way of giving the model something checkable, not a setting you can switch on.

**Tags**: `#few-shot prompting`, `#GLM`, `#Claude Haiku`, `#coding agents`, `#prompt engineering`

---

<a id="item-tech-news-13"></a>
### [Forum fix: run the &\#x27;dsh&\#x27; desktop agent unelevated so its shell can start](https://linux.do/u/gangpula32) ⭐️ 5.0/10

A poster on the linux.do forum describes a fix for a Windows failure in the desktop version of a tool called &quot;dsh&quot;: when it runs in &quot;workspace-write&quot; mode \(a mode where the agent is allowed to create and change files in a designated folder\), it cannot start its shell — the command-line program the agent uses to carry out tasks — and returns error 0xC0000142, a Windows code meaning a program failed to launch. The poster&\#x27;s explanation is that dsh&\#x27;s process must run at &quot;Medium&quot; integrity rather than &quot;High&quot;: Windows tags every running program with an integrity level, with High meaning it holds administrator power and Medium meaning ordinary-user power, and the shell refuses to start under the higher one. The proposed fixes are to launch dsh as a normal user instead of as administrator, or, for people who stay logged in as the built-in Administrator account, to set the Windows registry value FilterAdministratorToken to 1 \(a setting that makes that account run with ordinary-user rights until a program explicitly asks for more\) and reboot. The post names no dsh version, gives no link to the software, and is a single user&\#x27;s account rather than a vendor statement or a reproduced test.

telegram · linuxdo\_tg · Oct 28, 00:42

**「Why administrator mode changes app permissions」** Windows User Account Control normally gives an administrator a standard-permission session \(called Medium integrity\) and asks for approval before switching to full administrator rights \(High integrity\). The built-in Administrator account is exempt from that split unless the FilterAdministratorToken setting is enabled, Microsoft&\#x27;s documentation shows; enabling it makes Windows apply the same approval step to that account.

**「What to do if you hit it」** If a desktop coding agent stops with 0xC0000142 the moment it tries to run a command, close it and start it again without administrator rights — for example by launching it normally rather than via &quot;Run as administrator&quot; — before changing anything else. The registry change is the fallback for people whose everyday account is the built-in Administrator; it lowers that account&\#x27;s default power across the whole machine until Windows is restarted, so other tasks that assume full administrator rights may start behaving differently.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.0xkholod.com/002-pentesting/windows-pentesting/filteradministratortoken">FilterAdministratorToken</a></li>
<li><a href="https://learn.microsoft.com/en-us/windows/security/application-security/application-control/user-account-control/settings-and-configuration">User Account Control settings and configuration UAC hardening and Windows Administrator protection Tutorial GPO - Enable FilterAdministratorToken User Account Control approval mode for the built-in ... UAC Bypass - DFIR Handbook</a></li>

</ul>
</details>

**Tags**: `#coding-agents`, `#sandbox`, `#windows`, `#troubleshooting`, `#developer-tooling`

---

## Financial News

<a id="item-finance-news-1"></a>
### [EU to charge €2 fee on non-EU parcels from November 1](https://www.luxtimes.lu/europeanunion/new-levy-on-non-eu-parcels-kicks-in-november-1/163611818.html) ⭐️ 7.0/10

The EU will impose a €2 handling fee per item on parcels sent directly from outside the EU to consumers from November 1, 2026, regardless of parcel value, alongside a temporary €3 fee on low-value parcels that runs until July 1, 2028. The fees are paid by e-commerce platforms, sellers and intermediaries, and the EU says they offset customs costs for handling large parcel volumes.

telegram · zaihuapd · Oct 27, 02:30

**「Background」** The €2 charge, known as the Union Handling Fee, is part of the EU&\#x27;s wider customs reform covering e-commerce purchases arriving from outside the bloc. A separate €3 customs duty has applied since 1 July 2026 to each item in parcels valued at €150 or less, and the source says that levy is temporary, running until 1 July 2028.

**「Who pays」** The charges fall first on the cross-border platforms, sellers and intermediaries shipping direct to EU consumers, with shoppers facing higher prices if those costs are passed on; the separate €3 low-value levy is a temporary customs duty running until 1 July 2028, after which normal customs duties apply.

<details><summary>References</summary>
<ul>
<li><a href="https://www.revenue.ie/en/customs/individuals/union-handling-fee/index.aspx">Union Handling Fee (UHF) – 1 November 2026 - revenue.ie</a></li>
<li><a href="https://www.ecommerceaccountants.co.uk/post/eu-handling-fee-parcels-november-2026">EU €2 handling fee from 1 November 2026: what a parcel to an ...</a></li>
<li><a href="https://trade.ec.europa.eu/access-to-markets/en/news/eu-applies-eu3-customs-duty-item-low-value-e-commerce-consignments">EU applies €3 customs duty per item on low-value e-commerce ...</a></li>

</ul>
</details>

**Tags**: `#EU trade policy`, `#cross-border e-commerce`, `#customs fees`, `#consumer prices`, `#parcel logistics`

---

<a id="item-finance-news-2"></a>
### [Microsoft offers voluntary buyouts to about 60,000 employees](https://www.bloomberg.com/news/articles/2026-10-26/microsoft-to-offer-buyouts-to-60-000-workers-in-latest-cost-cut) ⭐️ 7.0/10

Microsoft is offering voluntary severance to about 60,000 employees — vice presidents and below in the US, Canada, India and the UK — Bloomberg reported, with Xbox, Windows, Copilot and finance fully included while data centers, sales and marketing are excluded. A Microsoft spokesperson said the packages are close to its standard severance terms; the company had 223,000 employees as of the end of June, and offered a similar plan to retirement-age staff in July.

telegram · zaihuapd · Oct 27, 03:09

**「Background」** The roughly 60,000 eligible employees amount to more than a quarter of Microsoft&\#x27;s global workforce, which stood at 223,000 at the end of June, and in July the company offered a similar buyout to employees near retirement age.

<details><summary>References</summary>
<ul>
<li><a href="https://www.reuters.com/technology/microsoft-is-offering-buyouts-around-60000-employees-business-insider-reports-2026-10-26/">Microsoft offers buyouts to around 60,000 employees to ...</a></li>

</ul>
</details>

**Tags**: `#Microsoft`, `#workforce restructuring`, `#voluntary buyouts`, `#cost cutting`, `#technology sector`

---

<a id="item-finance-news-3"></a>
### [China Sets IPTV Startup Rules: Live TV First, No Ads](https://www.nrta.gov.cn/art/2026/10/27/art_1588_74296.html) ⭐️ 7.0/10

China’s National Radio and Television Administration issued temporary rules requiring IPTV services to open directly to full-screen live TV at startup and banning startup advertisements, effective November 27, 2026.

telegram · zaihuapd · Oct 27, 05:59

**「Background」** IPTV delivers television over broadband networks, and the NRTA is China’s broadcasting regulator.

**「Impact」** The rules directly affect IPTV operators and advertisers by removing startup ad slots, smart-TV makers by requiring live-channel priority and simpler one-button controls, and viewers by adding a free-content area and clearer fee information.

**Tags**: `#IPTV regulation`, `#broadcasting policy`, `#startup advertising`, `#smart TVs`, `#consumer media rules`

---

<a id="item-finance-news-4"></a>
### [泡泡玛特三季度营收近腰斩，Labubu 热度消退](https://asia.nikkei.com/business/consumer/pop-mart-s-revenue-halves-in-q3-as-labubu-craze-cools) ⭐️ 7.0/10

Pop Mart disclosed a 45-50% year-over-year Q3 revenue decline as Labubu demand cooled, with overseas sales falling much faster and gross margin expected to narrow.

telegram · zaihuapd · Oct 27, 14:30

**Tags**: `#Pop Mart`, `#Q3 revenue decline`, `#Labubu`, `#consumer discretionary`, `#gross margin`

---