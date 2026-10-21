---
layout: default
title: "Horizon Summary: 2026-10-21 (EN)"
date: 2026-10-21
lang: en
---

> From 136 items, 18 important content pieces were selected

---

**Technology News**
1. [Apple MLX vs PyTorch MPS: fine-tuning AI models on a 16 GB Mac](#item-tech-news-1) ⭐️ 7.0/10
2. [Xiaomi&\#x27;s MiMo-V2.6-Pro model goes live on WorkBuddy with 1M-token context](#item-tech-news-2) ⭐️ 7.0/10
3. [OpenAI claims 97.9% COBOL migration accuracy with new models](#item-tech-news-3) ⭐️ 7.0/10
4. [OpenAI API extends prompt caching to 12 hours](#item-tech-news-4) ⭐️ 7.0/10
5. [Mistral releases Voxtral 3 speech model and voice-agent SDK](#item-tech-news-5) ⭐️ 6.0/10
6. [Andreich App Sends Spoken Tasks From MacBook Notch to Claude Code](#item-tech-news-6) ⭐️ 6.0/10
7. [Test of four Claude and ChatGPT models finds similar coding accuracy, different speed and price](#item-tech-news-7) ⭐️ 6.0/10
8. [Roundup lists 10 services that resell cheap or free access to DeepSeek, GLM and GPT](#item-tech-news-8) ⭐️ 6.0/10
9. [Google publishes TorchTPU code to run PyTorch AI models on TPU chips](#item-tech-news-9) ⭐️ 6.0/10
10. [DeepSeek posts DeepInfer, a framework for running its models, with few details](#item-tech-news-10) ⭐️ 5.0/10
11. [A guide to moving video generation from Veo 3.1 to Gemini Omni Flash](#item-tech-news-11) ⭐️ 5.0/10
12. [Smart-TV Owners Use AI Coding Tool to Remove Home-Screen Ads](#item-tech-news-12) ⭐️ 5.0/10
13. [A forum user&\#x27;s workaround: a second Claude Code session to wake a stalled Codex](#item-tech-news-13) ⭐️ 5.0/10
14. [MiniMax M3.1 Flash reported free in Cline, claimed to match Claude Opus](#item-tech-news-14) ⭐️ 5.0/10
15. [Ottili ONE releases 39-skill library for Claude Code and Codex](#item-tech-news-15) ⭐️ 5.0/10
16. [US Homeland Security bars DeepSeek from federal civilian agency purchases](#item-tech-news-16) ⭐️ 5.0/10

**Financial News**
1. [China&\#x27;s MIIT Tightens Rules for Innovative Car Designs](#item-finance-news-1) ⭐️ 7.0/10
2. [SpaceX and Tesla Boards Form Special Committees to Review Possible Merger](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Apple MLX vs PyTorch MPS: fine-tuning AI models on a 16 GB Mac](https://habr.com/ru/companies/otus/articles/1090656/?utm_campaign=1090656&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 7.0/10

A translated Habr article reports a hands-on benchmark of two ways to fine-tune AI models on a 16 GB Apple Silicon Mac: Apple MLX, Apple&\#x27;s framework for training and running models on its chips, and PyTorch MPS, the Mac graphics-chip mode of the widely used PyTorch tool. Across 10 runs with Alibaba&\#x27;s Qwen 2.5 models of different sizes and context lengths \(the amount of text a model can consider at once\), the author found MLX could be several times slower than MPS during fine-tuning. However, when MPS hit memory limits, MLX could run a model twice as large. The article also examines whether quantization—storing model numbers in fewer bits to save memory—explains the gap.

rss · Habr AI · Oct 20, 17:46

**「Background」** Fine-tuning means continuing to train an existing model on your own examples; on a 16 GB Mac, the hard limit is memory shared by the processor and graphics chip. Apple MLX is Apple&\#x27;s framework built specifically for its chips, while PyTorch MPS is the mainstream PyTorch framework running through Apple&\#x27;s graphics support. The test also looks at quantization, which stores a model&\#x27;s numbers in fewer bits to shrink it, because that choice can change which framework fits the model at all.

**「What it means in practice」** For someone trying to fine-tune a model on a 16 GB Mac, the practical choice depends on whether the model fits in memory: MPS may be faster when it does, while MLX may be the only route to a larger model. Because the results cover only Qwen 2.5 and this hardware, users should test their own model size and text length before choosing a setup.

**Tags**: `#Apple MLX`, `#PyTorch MPS`, `#local LLM fine-tuning`, `#Qwen 2.5`, `#Apple Silicon`

---

<a id="item-tech-news-2"></a>
### [Xiaomi&\#x27;s MiMo-V2.6-Pro model goes live on WorkBuddy with 1M-token context](https://weibo.com/6486870325/5356179212995907) ⭐️ 7.0/10

Xiaomi says its MiMo-V2.6-Pro model is now available to try on WorkBuddy. The company claims the model scores 46 on the Artificial Analysis Intelligence Index \(an independent public leaderboard that runs models through a standard set of reasoning and knowledge tests\) and that this puts it first among open-source models — meaning models whose underlying files are published for others to download and run. Xiaomi also says it handles a context window of 1 million tokens \(the amount of text a model can hold in view at once; a token is a small chunk of text, roughly part of a word\), accepts images, video, audio and text together, and can split long jobs across several copies of itself working in parallel. All of these figures and rankings come from Xiaomi&\#x27;s own announcement, and the post gives no pricing, usage limits, license terms, or download links for the model&\#x27;s weights.

telegram · zaihuapd · Oct 20, 13:40

**「Context」** MiMo is Xiaomi&\#x27;s own family of AI models, issued in numbered versions, so V2.6-Pro is the successor to the V2.5 series. Two terms in the announcement carry most of the meaning: a &quot;1M context window&quot; means the model can take in about one million tokens — chunks of text, and here also images, video and audio — in a single session, roughly the length of several novels; and &quot;open-source&quot; here means the model&\#x27;s trained parameters can be downloaded and run by others rather than only used through Xiaomi. The Artificial Analysis Intelligence Index is a composite score compiled by Artificial Analysis, an independent site that tests and compares models, and Xiaomi&\#x27;s 46.32 figure comes from that outside scorecard even though the &quot;first among open-source models&quot; framing is the company&\#x27;s own.

**「What it means if you use these tools」** The practical draw is long work: a 1-million-token window is enough to keep something like a full book or a large batch of documents in view without chopping it up, and the mixed image, video and audio input suits research, design drafts and office paperwork. But because Xiaomi has not published cost, usage caps or license terms, anyone planning to build on it cannot yet tell what it will cost or whether they will be allowed to run it on their own machines — so for now the sensible step is to test it inside WorkBuddy rather than plan a rollout around it.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/mimo-v2-6-pro">MiMo-V2.6-Pro Intelligence, Performance &amp; Price Analysis</a></li>
<li><a href="https://mimo.xiaomi.com/mimo-v2-6">MiMo-V2.6 | Xiaomi</a></li>
<li><a href="https://mimo.mi.com/models/en-US/mimo-v2.6-pro">Xiaomi MiMo-V2.6 Series: 3 New Models Officially Released</a></li>

</ul>
</details>

**Tags**: `#model release`, `#Xiaomi MiMo`, `#open-weight models`, `#long context`, `#benchmarks`

---

<a id="item-tech-news-3"></a>
### [OpenAI claims 97.9% COBOL migration accuracy with new models](https://openai.com/index/low-resource-programming-languages/) ⭐️ 7.0/10

OpenAI published results saying its newest models handle rarely used programming languages — COBOL \(the decades-old language still running many bank, insurance and government systems\), Fortran and Visual Basic — far better than the previous generation. In a test that rebuilds a small database engine \(SQLite\) in 20 languages, a model called GPT-6 Astra passed 87.4% of the time on average, up from 26.8% for GPT-5.6 Sol, while a cheaper model, GPT-6 Luna, reached 40.3% with API costs \(the per-request fees developers pay to use a model\) down 78%. On rewriting old COBOL into modern code, GPT-6.1 Sol rose from 5.4% accuracy to 86.6% at low reasoning effort \(how much internal computation the model spends before answering\) at 39% lower cost, and reached 97.9% when allowed to think longer. The numbers come from OpenAI&\#x27;s own post, relayed by a Telegram channel, and the evaluation set has been published on GitHub; no independent verification is available yet.

telegram · zaihuapd · Oct 20, 14:24

**「Background」** COBOL is a decades-old programming language still used in many banking systems, and it is one of the “low-resource” languages that AI models encounter relatively rarely in their training data. OpenAI&\#x27;s new benchmark, MultiLangBench, asks models to build a small database engine from scratch in 20 languages, including COBOL, Fortran and Visual Basic. That setup is meant to test whether a model can handle languages outside the popular ones, such as Python, where public code is plentiful.

**「What changes for teams with old code」** For banks, insurers, and government agencies still running COBOL, the practical change is that modernizing old code could shift from writing replacements by hand to checking machine-written ones: OpenAI reports 97.9% accuracy when the model is allowed to work through the problem longer, against 5.4% for the previous generation. Those figures come from OpenAI&\#x27;s own test set, not independent testing, so a team should run the newly published benchmark on a sample of its own code before planning a migration around it. The 97.9% result also takes more time and money per task than the 86.6% fast-setting result, and the 78% cost drop is measured per task in the test — outside coverage of the GPT-6 family describes a 50% cut in API list prices.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kucoin.com/news/flash/openai-improves-gpt-6-s-legacy-programming-capabilities-in-cobol-and-fortran">OpenAI Enhances GPT - 6 ’s Legacy Programming Capabilities... | KuCoin</a></li>
<li><a href="https://jendume.com/en/news/gpt-6-modelleri-dusuk-kaynakli-programlama-dillerinde-basari-sagladi/">GPT - 6 models advance coding in low-resource... | JEN DUME</a></li>
<li><a href="https://felloai.com/gpt-6-sol-luna/">GPT-6 Sol and Luna: OpenAI Halves Its API Prices</a></li>
<li><a href="https://www.unite.ai/openai-introduces-gpt-6-sol-and-luna-with-50-lower-api-prices/">OpenAI Introduces GPT-6 Sol and Luna With 50% Lower API ...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#COBOL migration`, `#low-resource languages`, `#model benchmarks`, `#API pricing`

---

<a id="item-tech-news-4"></a>
### [OpenAI API extends prompt caching to 12 hours](https://x.com/OpenAIDevs/status/2112603916076781778) ⭐️ 7.0/10

OpenAI&\#x27;s API now keeps cached prompts — previously sent instructions and context that the model can reuse instead of processing again — for 12 hours, according to a relayed post from the company&\#x27;s developer account. OpenAI says long-running automated agents can reuse shared instructions, tools and context throughout the day and still pay the lower cached-input rate even when requests are hours apart. For signed-in users of Codex, OpenAI&\#x27;s coding tool, and Work, the company says caching is permanent and the system is guaranteed to find the stored material, so returning to an old conversation or pausing for hours carries no penalty. No specific prices were included.

telegram · zaihuapd · Oct 21, 01:21

**「What prompt caching is」** An API is the paid interface that lets other software send requests to OpenAI&\#x27;s models. Prompt caching lets the service keep a processed copy of repeated input, such as standing instructions, the list of tools an agent can use, or earlier conversation text, so later requests can reuse it instead of starting over. That reused portion is billed at a lower &quot;cached input&quot; rate, which is why a longer cache lifetime matters for agents: software that runs multi-step tasks and often resends the same context throughout the day.

**「Practical impact」** Teams running AI agents \(programs that carry out multi-step tasks\) can now leave up to 12 hours between requests and still have repeated instructions, tools, and context billed at the cheaper cached-input rate through OpenAI&\#x27;s prompt cache \(a stored copy the model reuses instead of reprocessing\). Caching is already on by default for supported models, so the practical check is the cache read hit rate in OpenAI&\#x27;s dashboard: a miss means paying the uncached input rate, and the diagnostics tool is there to show why reuse failed.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.openai.com/api/docs/guides/prompt-caching">Prompt caching | OpenAI API</a></li>
<li><a href="https://panews.io/articles/01a15c05-f237-73d6-8b72-63345c0d5e9f">OpenAI API Launches 12-Hour Prompt Caching; Cache for Codex ...</a></li>

</ul>
</details>

**Tags**: `#openai`, `#prompt-caching`, `#api-pricing`, `#codex`, `#developer-tooling`

---

<a id="item-tech-news-5"></a>
### [Mistral releases Voxtral 3 speech model and voice-agent SDK](https://mistral.ai/news/voxtral-3/) ⭐️ 6.0/10

Mistral has released Voxtral 3, a speech model, along with a voice-agent SDK — a toolkit for building apps that listen, reason, call other tools and speak back during live phone or web conversations. The material available gives no benchmark scores, pricing, or release date, so it is not established how much better it is than Mistral&\#x27;s earlier speech models or whether the model itself can be downloaded and run on a customer&\#x27;s own machines. The announcement frames the SDK around agents that can look things up and act in business systems mid-call.

hackernews · ilreb · Oct 20, 16:02 · [Discussion](https://news.ycombinator.com/item?id=50168396)

**「Background」** Speech models do two separate jobs: transcription \(turning audio into text\) and text-to-speech \(turning written text into spoken audio\). The &quot;3&quot; in the name marks this as the third iteration of Mistral&\#x27;s Voxtral speech line; one commenter says they already sell commercial Windows software that runs the previous open-weight model, Voxtral Mini 4B Realtime, offline on a laptop with 4GB of graphics memory. Voxtral 3 pairs the speech models with a voice-agent SDK, a toolkit for chaining listening, reasoning, tool calls and a spoken reply into one real-time stream.

**「What changes for offline and on-premise users」** Anyone who needs speech recognition to run on their own machine — for privacy, cost, or because there is no reliable internet — should not assume Voxtral 3 is a drop-in upgrade. A commenter notes the new model is closed, whereas the previous Voxtral Mini 4B Realtime was open-weight \(the files could be downloaded and run locally\) and, according to a developer who shipped a Windows product around it, ran faster than real time on an ordinary laptop using 4 GB of graphics memory. Teams that built on that earlier model would have to keep running it or send their audio to Mistral&\#x27;s hosted service instead. On the hosted side, Mistral&\#x27;s text-to-speech model is listed on the OpenRouter marketplace at $13 per million characters, so the bill grows with how much the voice agent speaks.

**「What commenters said」** Several commenters judged the release by whether it can run locally: one developer said they already sell commercial Windows software that runs the earlier open-weight \(parameters published for anyone to download\) Voxtral Mini 4B Realtime offline on an ordinary laptop with 4GB of graphics memory, faster than real time, and another read Voxtral 3 as closed, continuing a pattern of speech models that are hard to deploy on your own hardware. A separate complaint held that transcripts from Microsoft Teams and 8x8 are often too poor to feed reliably into AI models, and one commenter dismissed the demo as unrealistic because a dermatologist appointment cannot be had that fast in France.

<details><summary>References</summary>
<ul>
<li><a href="https://mistral.ai/news/voxtral-3/">Voxtral 3: Voice Agent SDK &amp; Speech Models in 50+ Languages</a></li>
<li><a href="https://www.technobezz.com/news/mistral-ai-voxtral-3-voice-agent-sdk">Mistral AI Launches Voxtral 3 With Voice Agent SDK and 50 ...</a></li>
<li><a href="https://openrouter.ai/mistralai/voxtral-mini-tts-3-0">Voxtral TTS 3 - API Pricing &amp; Providers | OpenRouter</a></li>

</ul>
</details>

**Tags**: `#Mistral`, `#Voxtral 3`, `#speech-to-text`, `#voice-agents`, `#model-release`

---

<a id="item-tech-news-6"></a>
### [Andreich App Sends Spoken Tasks From MacBook Notch to Claude Code](https://habr.com/ru/articles/1097006/?utm_campaign=1097006&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A developer has released Andreich, an open-source app under the MIT license \(which lets anyone reuse and modify the code\) that sits in the black cutout at the top of newer MacBook screens. It listens through the microphone all day, turns spoken remarks into tasks, and sends them to a chosen Claude Code session—one running conversation with Anthropic’s AI coding tool—after the user says “OK.” It also shows how much of the weekly usage limit on a paid Claude plan is left. The author says the roughly 4,900-line app was written entirely through conversations with Claude Code in about a day, with no manual edits, and warns that speech recognition—the software that turns speech into text—once failed silently while the microphone stayed on, costing an hour of recording.

rss · Habr AI · Oct 20, 22:18

**「Context」** Claude Code is Anthropic&\#x27;s AI coding assistant, which developers use in sessions to carry out coding tasks. The MacBook notch is the black cutout at the top center of newer MacBook screens, normally home to the camera and status icons. The app described here is a single developer&\#x27;s project released under the MIT license \(a permissive open-source license that allows reuse and modification\), not an Anthropic or Apple product.

**「What It Means in Practice」** Claude Code users with a notch-equipped MacBook could use it to capture tasks by voice and see how much weekly quota is left, but it is a one-person project released in a day, not an established product. Anyone trying it should verify that speech recognition is actually running, because the author reports it can fail silently while the microphone indicator stays on, and should consider whether an always-on microphone fits their privacy needs.

**Tags**: `#Claude Code`, `#AI agents`, `#open source`, `#macOS`, `#developer tooling`

---

<a id="item-tech-news-7"></a>
### [Test of four Claude and ChatGPT models finds similar coding accuracy, different speed and price](https://habr.com/ru/companies/syntx_ai/articles/1096542/?utm_campaign=1096542&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

An article on the Russian tech site Habr compared four AI models — Claude Opus 5.5 and Claude Sonnet 5.5 from Anthropic, and ChatGPT 6 Astra and ChatGPT 6.1 Sol from OpenAI — on the same eight programming tasks. According to the article, all four produced working code on the first attempt, and only one answer had to be reformatted. The differences appeared elsewhere: the total response time for all eight tasks ranged from 8 to 28 minutes, the price per token \(the unit of text that AI services bill for\) differed by up to five times, and the models organized their solutions differently. The post is a short teaser that points to a longer article, and the model names and figures come from the author without independent verification.

rss · Habr AI · Oct 20, 08:11

**「Why these four models are being compared」** All four are recent releases. OpenAI shipped GPT-6.1 Sol at its DevDay event on September 29, 2026, describing it as a mid-tier model that comes close to its flagship GPT-6 Astra at about a fifth of Astra&\#x27;s price per token, while Anthropic had launched Claude Opus 5.5 roughly a week earlier, pitched as reaching its earlier top model&\#x27;s performance for 40% less, with Sonnet 5.5 arriving in the same wave. Because the cheaper models are sold as near-flagship quality, the practical question for anyone paying for coding help is whether the lower price per token \(the small chunks of text that AI services bill for\) comes with slower or clumsier answers — which is what running the same eight tasks through all four is meant to show.

**「What this means if you&\#x27;re picking a coding assistant」** Since all four models wrote correct code on the first attempt, the real trade-off for someone choosing a coding assistant is waiting time and bill size, not accuracy: the same eight tasks took between 8 and 28 minutes in total, and the price charged per token \(the unit of text that AI providers bill for\) differed by up to five times. Access also varies by plan — Sonnet 5.5 can be used on Claude&\#x27;s free tier with usage limits, while GPT-6.1 Sol requires a paid ChatGPT subscription — so a free-tier user cannot run this comparison at all.

<details><summary>References</summary>
<ul>
<li><a href="https://www.datacamp.com/blog/gpt-6-1-sol-vs-opus-5-5">GPT-6.1 Sol vs. Claude Opus 5.5: Which Model to Use</a></li>
<li><a href="https://note.com/ai__worker/n/n3d128ad2dd06?hl=en">Latest AI Model Comparison [October 2026] | GPT-6.1 Sol ...</a></li>
<li><a href="https://convly.ai/gemini-4-argon-vs-gpt-6-1-sol-vs-claude-sonnet-5-5/">Gemini 4 Argon vs GPT - 6 .1 Sol vs Claude Sonnet 5 . 5 | Convly</a></li>

</ul>
</details>

**Tags**: `#model comparison`, `#Claude`, `#ChatGPT`, `#coding`, `#pricing`

---

<a id="item-tech-news-8"></a>
### [Roundup lists 10 services that resell cheap or free access to DeepSeek, GLM and GPT](https://habr.com/ru/articles/1096538/?utm_campaign=1096538&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

A Russian-language article published on Habr on 20 October lists ten &quot;API routers&quot; — services that sit between a user&\#x27;s software and the companies that make AI models, forwarding requests and sometimes pooling free quotas or reselling access at low prices. The services named are OrcaRouter, TeamoRouter, Srazu, RockAPI, OpenRouter, llmgw, VseGPT, Token Harbor, NaraRouter and FreeRouter. The author says he signed up for each one and checked which models are free or nearly free, what limits apply, whether calls through the API actually work, whether the interface is in Russian, whether payment can be made in rubles, and whether the site opens from Russia without a VPN. The excerpt published in the feed contains none of those results: the prices, quotas and test outcomes are said to sit in two comparison tables and 17 account screenshots inside the full article, so the specific claims cannot be checked from what is available here.

rss · Habr AI · Oct 20, 07:08

**「Background」** DeepSeek, GLM and GPT are families of AI models; normally software reaches them through an API, the connection that lets one program request answers from another. An API router is a middleman service, sometimes called a relay, that holds accounts with several model providers and forwards each request to the model the user chooses, which is how it can bundle shared free quotas, trial credit, or local payment and access options.

**「What to check before switching」** If the software you already use speaks OpenAI&\#x27;s API format, a router that copies that format can be dropped in without code changes — TeamoRouter&\#x27;s documentation, for example, says it accepts OpenAI, Google Gemini and Anthropic request formats — so the first practical check is whether a given router supports the format your tool already sends. The roundup&\#x27;s claims about free quotas and working calls come from the author&\#x27;s own testing and are not independently confirmed here, so try a small request on the free tier before moving any real work onto one of these services.

<details><summary>References</summary>
<ul>
<li><a href="https://teamorouter.com/docs/api-integration">TeamoRouter API Integration Guide · Docs</a></li>

</ul>
</details>

**Tags**: `#API routers`, `#DeepSeek`, `#GLM`, `#pricing`, `#regional access`

---

<a id="item-tech-news-9"></a>
### [Google publishes TorchTPU code to run PyTorch AI models on TPU chips](https://cloud.google.com/blog/topics/ai-infrastructure/torchtpu-is-now-open-source-run-native-pytorch-on-tpus) ⭐️ 6.0/10

Google Cloud has published the source code for TorchTPU, software developed with Meta&\#x27;s PyTorch team that lets PyTorch—a widely used framework for building and training AI models—run on Google&\#x27;s TPUs \(its custom AI chips\) as a standard option alongside graphics processors \(GPUs\) and ordinary processors \(CPUs\). Google says existing PyTorch code needs almost no changes, and that several tools for running and training models—vLLM, SGLang, llm-d and TorchTitan—already work with it, while the Hugging Face Transformers v5 library can deploy models to TPUs directly. The release is about software support: it does not announce new model capabilities, TPU pricing, quotas, or access changes.

telegram · zaihuapd · Oct 21, 00:47

**「Background」** PyTorch is the open-source software framework that many AI teams use to write and train models; TPUs are Google&\#x27;s own chips for that work, while Nvidia&\#x27;s GPUs have been the default hardware. Until now, running ordinary PyTorch code on a TPU took extra adaptation, so teams that wanted to use TPUs often had to change their code or rely on Google-specific tooling. TorchTPU is meant to remove that step by making the TPU a standard PyTorch target alongside GPUs and CPUs.

**「Impact」** For teams that use PyTorch, the practical change is that the same training or running code can be tried on Google Cloud&\#x27;s TPUs with far less rewriting, making TPUs a more realistic alternative to Nvidia GPUs. They still need to check that their framework is one of the integrated ones; the announcement gives no new TPU pricing, quota, or access terms.

**「Community discussion」** Commenters framed the release as part of a wider contest: one said Amazon already offers a similar PyTorch path for its Trainium AI chips, and another described an experimental open-source project that runs most of TorchTPU on Tenstorrent&\#x27;s AI chips. One commenter argued the bigger effect could be better compiler software, which translates model code for different chips, and the decline of TensorFlow, Google&\#x27;s older AI framework, while another said the choice between PyTorch and JAX, a competing framework, is now mostly a matter of style.

**Tags**: `#TorchTPU`, `#PyTorch`, `#TPU`, `#Google Cloud`, `#open source`

---

<a id="item-tech-news-10"></a>
### [DeepSeek posts DeepInfer, a framework for running its models, with few details](https://github.com/deepseek-ai/DeepInfer) ⭐️ 5.0/10

DeepSeek&\#x27;s GitHub account has published DeepInfer, software for running its AI models — the &quot;inference&quot; layer that takes a trained model and turns it into answers. The repository describes itself as a &quot;high-performance inference framework for DeepSeek models,&quot; but the material available at publication included no README, benchmark numbers, installation steps, or list of supported hardware, so it is not possible to say how fast it is or which models it covers. The project appeared on GitHub on October 20, 2026, and drew attention on Hacker News. Whether it is a working tool or an early placeholder remains unconfirmed.

hackernews · ggcr · Oct 20, 09:08 · [Discussion](https://news.ycombinator.com/item?id=50163277)

**「Background」** Running a trained AI model — inference — requires separate serving software that loads the model&\#x27;s weights \(the trained parameters\) and turns incoming requests into answers. DeepSeek, the Chinese lab that publishes its models&\#x27; weights for anyone to download, had kept that serving layer in-house; DeepInfer is the framework it says powers its large-scale production services, now released under the Apache-2.0 license on 20 October 2026. The release focuses on offline inference and leaves out some features that live services rely on, and the project was originally built mainly on top of vLLM, an existing open-source serving engine.

**「Not a complete serving setup yet」** Anyone hoping to run a DeepSeek model on their own servers straight from this repository should note that it is not a complete serving setup: the project&\#x27;s own description lists a KV cache system — the memory that keeps a conversation&\#x27;s earlier text so the model does not reprocess it for every new word — as required for a complete inference service and says it is not included in this release, so a team would have to supply or build that piece themselves. The code does list support for Huawei&\#x27;s Ascend 950 chips, so groups running that hardware instead of Nvidia&\#x27;s would need to confirm the rest of their serving stack fits.

**「What commenters said」** Commenters seized on two unverified claims: one quoted a Chinese blog post asserting the framework already serves a model called &quot;DeepSeek V4.1 Flash&quot; at 155 trillion tokens a day, and another said the code supports Huawei&\#x27;s Ascend 950 chips, which if true would let labs run DeepSeek models on hardware other than Nvidia&\#x27;s. Neither claim could be checked against the repository itself, and much of the rest of the thread was political commentary unrelated to the software.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/DeepInfer">GitHub - deepseek-ai/DeepInfer: DeepInfer: High-performance ...</a></li>
<li><a href="https://cldnavi.com/en/blog/deepinfer-inference-framework-2026/">DeepInfer: DeepSeek open-sourced the inference framework ...</a></li>
<li><a href="https://www.marktechpost.com/2026/10/20/deepseek-deepinfer-open-source-inference-framework/">DeepSeek Open-Sources DeepInfer, the Inference Framework ...</a></li>
<li><a href="https://github.com/deepseek-ai/DeepInfer">GitHub - deepseek -ai/ DeepInfer : DeepInfer : High- performance ...</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#inference framework`, `#open-weight models`, `#self-hosting`, `#GitHub`

---

<a id="item-tech-news-11"></a>
### [A guide to moving video generation from Veo 3.1 to Gemini Omni Flash](https://habr.com/ru/articles/1096576/?utm_campaign=1096576&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

A practitioner&\#x27;s guide on the Russian site Habr reports that Google will switch off the three preview \(early-release\) versions of its Veo 3.1 video-generation models in the Gemini API \(the interface software uses to call Google&\#x27;s AI models\) on 22 October 2026, and that the recommended replacement is Gemini Omni Flash \(gemini-omni-1.1-flash\). Swapping the model name is not enough: the new model is reached through a different request format called the Interactions API, takes images in a different way, and has no setting for how long a clip lasts. The author, who makes advertising and short videos through the API, describes the errors he hit while porting three workflows — turning an image into video, transitions between a first and last frame, and clips built from character references — and compares quality and per-clip cost, which he calculates from the API&\#x27;s response. The shutdown date and the replacement recommendation come from the author&\#x27;s account of Google&\#x27;s notice; the article does not show independent confirmation.

rss · Habr AI · Oct 20, 08:05

**「Background」** Veo is Google&\#x27;s model for turning text or images into video, and software reaches it through the Gemini API — the interface that lets a program send requests to Google&\#x27;s models and get results back. Google labels some versions &quot;preview,&quot; meaning an early release it can withdraw on a set date, which is what is happening to the three Veo 3.1 preview models. Google&\#x27;s own Veo documentation notes that building a clip from a chosen first and last frame works only on Veo 3.1 models, so anyone using that feature has to rebuild the request for the replacement rather than just swap a model name.

**「What changes for anyone calling the API」** Teams that generate video through the Gemini API have to rewrite their requests before October 22, 2026, when the three Veo 3.1 preview models stop working: Gemini Omni Flash expects images to be passed in a different role scheme and has no duration setting, so changing only the model name will produce errors or clips of the wrong length. Cost tracking also needs updating, because the price of a clip has to be calculated from what the API returns rather than from a duration the caller chose.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.google.dev/gemini-api/docs/veo">Generate videos with Veo 3 . 1 in Gemini API | Google AI for Developers</a></li>

</ul>
</details>

**Tags**: `#Gemini API`, `#Veo 3.1`, `#video generation`, `#API migration`, `#model pricing`

---

<a id="item-tech-news-12"></a>
### [Smart-TV Owners Use AI Coding Tool to Remove Home-Screen Ads](https://mashable.com/tech/smart-tv-ads-claude-code-ai-cleanup) ⭐️ 5.0/10

A report describes some smart-TV owners using AI coding assistants such as Claude Code—a tool that turns plain-language requests into commands a computer runs—to remove ads and unwanted preinstalled software from their TV&\#x27;s main menu. One developer said on October 17 that he connected it to a Xiaomi TV, removed 25 software packages \(installed apps and background services\), and skipped startup ads to go straight to Netflix. The efforts are gathered in a publicly shared project called CleanYourTV, which requires a separate computer running Claude Code and works only on Android TV and Google TV, Google&\#x27;s TV operating systems. TiVo says more than one-third of surveyed people complain about too many main-menu ads, though the report gives no reproducible instructions or independent verification.

telegram · zaihuapd · Oct 20, 13:18

**「Background」** Android TV and Google TV are Google&\#x27;s software platforms for televisions, and many sets sold with them include preinstalled apps and home-screen ads that owners cannot remove through normal settings. CleanYourTV is a publicly available open-source project that uses Claude Code — an AI assistant that writes and runs technical commands — on a separate computer to connect to the TV and uninstall unwanted software components.

**「Compatibility limits」** The catch is which TV you own: the project only works on sets running Android TV or Google TV, so Samsung \(Tizen\) and LG \(webOS\) televisions need a separate port, and on Amazon&\#x27;s Fire TV only the software-removal half works because Fire OS will not hand its home screen over to another launcher. It also needs a computer on the same Wi-Fi network running Claude Code, so this is not something you can do from the TV remote alone.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Gathin23/cleanyourtv/">GitHub - Gathin23/ cleanyourtv : Debloat any Android or Google TV ...</a></li>
<li><a href="https://cleanyour.tv/">CleanYourTV</a></li>

</ul>
</details>

**Tags**: `#Claude Code`, `#Android TV`, `#debloating`, `#AI coding agents`, `#CleanYourTV`

---

<a id="item-tech-news-13"></a>
### [A forum user&\#x27;s workaround: a second Claude Code session to wake a stalled Codex](https://linux.do/u/demouo) ⭐️ 5.0/10

On Oct. 21, a Linux.do forum user posting as demouo described a homemade fix for a common annoyance with AI coding agents: when a long-running Codex session \(OpenAI&\#x27;s terminal-based coding agent\) goes quiet, nothing brings it back. The user runs Codex in one tab of a terminal multiplexer — a program that keeps several terminal sessions open in a single window, in this case one called herdr — and opens a second Claude Code session \(Anthropic&\#x27;s competing terminal coding agent\) in another tab, telling it to watch Codex and nudge it when it stalls. The post says the monitor woke Codex at 1:28 a.m. and again at 9 a.m., and that the monitoring session ran on deepseek-flash, a model the user calls cheap enough to leave watching continuously. No code, configuration, or reproducible steps were shared, so the wake-up times and the setup are one user&\#x27;s anecdote rather than a verified capability.

telegram · linuxdo\_tg · Oct 21, 02:13

**「Background」** Claude Code and Codex are AI coding agents: programs that run in a text-only terminal window, take instructions in plain language, and edit files on the user&\#x27;s machine themselves. herdr is a free, open-source terminal multiplexer built for exactly this kind of tool — it puts several agents in one window as separate tabs and panes, with a sidebar showing whether each one is working, finished, or stuck. That sidebar status is what makes it possible for one agent to notice that another has gone quiet.

**「What it means in practice」** For anyone who leaves a coding agent working overnight, the post points to a real gap: these tools have no built-in way to notice a session has gone idle and restart it, and the poster dismisses the existing /btw command as too limited for the job. The proposed substitute costs a second model session running alongside the first and has to be set up by hand, and because no configuration was published, copying it means rebuilding the arrangement yourself. The poster also notes the main Codex session is expensive to restart, which is why the monitor is meant to prod it rather than replace it.

<details><summary>References</summary>
<ul>
<li><a href="https://knightli.com/en/2026/07/06/herdr-terminal-agent-multiplexer/">herdr AI Agent Multiplexer : Install, Manage Agents, and Use Remote...</a></li>
<li><a href="https://www.chaseai.io/blog/herdr-terminal-multiplexer-ai-coding-agents">Herdr : Run Claude Code + Codex in One Terminal - Chase AI</a></li>
<li><a href="https://www.shareuhack.com/en/posts/herdr-terminal-agent-multiplexer-guide-2026">herdr 2026: Monitor Claude Code , Codex &amp; Devin in One Terminal</a></li>

</ul>
</details>

**Tags**: `#claude-code`, `#codex`, `#agent-orchestration`, `#developer-workflow`, `#terminal-multiplexer`

---

<a id="item-tech-news-14"></a>
### [MiniMax M3.1 Flash reported free in Cline, claimed to match Claude Opus](https://telegram.me/aipluscn/3149) ⭐️ 5.0/10

An October 20 post on a Telegram AI channel says MiniMax&\#x27;s M3.1 Flash model is now free to use inside Cline, a coding assistant that writes and edits code inside a programmer&\#x27;s editor. The post claims the model&\#x27;s coding ability is on par with Claude Opus and OpenAI&\#x27;s GPT models while costing about 25 times less to run, and says it is the model behind &quot;Space Bunny,&quot; an anonymous model that earlier topped a usage leaderboard with more than 200 trillion tokens \(tokens are the chunks of text a model reads and writes; usage is counted in them\). None of this is confirmed: the post links to no MiniMax or Cline announcement, no pricing page and no benchmark results, and hedges both the performance claim and the Space Bunny attribution with wording like &quot;reportedly&quot; and &quot;there are reports.&quot; The free access, the 25-times cost figure and the identity of Space Bunny should all be treated as unverified until the companies say so directly.

telegram · aipluscn · Oct 20, 14:59

**「Context」** Cline is a coding assistant that runs inside a code editor: you describe a task in plain language and the AI model writes or edits the files for you. MiniMax, a Chinese AI company, uses the &quot;Flash&quot; label for its cheaper, faster models, and this post is the first word of M3.1 Flash being offered there at no charge. The &quot;Space Bunny&quot; reference is to an unnamed model that earlier climbed to the top of a usage leaderboard after handling more than 200 trillion tokens \(tokens are the small chunks of text a model reads and writes\), before anyone publicly said who made it.

**「What to do with the free access」** For anyone who uses a coding assistant, the practical move is to test the free version on your own work before switching anything over: OpenRouter lists a no-cost MiniMax M3.1 Flash endpoint, so the model can be tried without a Cline account or a bill. The one published number there is less flattering than the post suggests — 25.8% on Terminal-Bench 4.0, a test of multi-step command-line tasks — so treat &quot;on par with Claude Opus&quot; as something to check against your own tasks rather than a reason to move a project onto it.

<details><summary>References</summary>
<ul>
<li><a href="https://www.breakread.com/minimax-m3-1-flash-space-bunny-ai-launch/">MiniMax M 3 . 1 Flash Launches, Reveals Space Bunny AI</a></li>
<li><a href="https://openrouter.ai/minimax/minimax-m3.1-flash:free">MiniMax M 3 . 1 Flash (free) - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**Tags**: `#MiniMax`, `#Cline`, `#free access`, `#model release`, `#pricing`

---

<a id="item-tech-news-15"></a>
### [Ottili ONE releases 39-skill library for Claude Code and Codex](https://github.com/Ottili-ONE/skills) ⭐️ 5.0/10

Ottili ONE announced a library of 39 reusable &quot;skills&quot; for AI coding assistants such as Claude Code and Codex, published as a public project on GitHub. A skill is a packaged set of instructions that tells an assistant how to carry out a particular task, so users can add a capability without writing it themselves. The announcement says the packs cover data processing, German business topics, and engineering practices, but it breaks down only 30 of the 39: 10 for data processing, 10 for German business domains, and 10 for engineering practice. The post gives no installation evidence, no examples of results, and no independent testing, so the library&\#x27;s quality and whether all 39 packs work as described remain unverified.

telegram · aipluscn · Oct 21, 01:50

**「What a skill pack is」** Claude Code and Codex are AI coding assistants: programs that can read a project, run commands, and carry out multi-step development tasks. A “skill pack” is a reusable set of instructions and workflows that such an assistant can load for a particular job, so users do not have to describe the same procedure from scratch each time. Ottili ONE’s library groups its packs by subject—data processing, German business tasks, and engineering practice—so users can find one that matches the work at hand.

**「What it means if you use Claude Code or Codex」** A skill is not an app you install: it is a folder of instructions, scripts and reference files that the AI agent reads and then follows on the tasks it recognizes, so trying these out means putting the folders where Claude Code or Codex looks for skills. The announcement gives no install steps, no examples of what the 39 packs actually contain, and no testing results, so read a skill&\#x27;s files before switching it on — once enabled, the agent acts on those instructions.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Ottili-ONE/skills">GitHub - Ottili - ONE / skills : Claude Code , Codex , OpenClaw and...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#Claude Code`, `#Codex`, `#skill library`, `#developer tooling`

---

<a id="item-tech-news-16"></a>
### [US Homeland Security bars DeepSeek from federal civilian agency purchases](https://telegram.me/aipluscn/3162) ⭐️ 5.0/10

The US Department of Homeland Security has issued an order removing DeepSeek, a Chinese AI company whose models power a popular chatbot, from what federal civilian agencies may buy and use. The order requires civilian agencies to strip all DeepSeek products from their computer systems, along with products from related entities and any third-party software or services that run on DeepSeek&\#x27;s models. It cites US cybersecurity law as its authority. The military and intelligence agencies had already placed similar limits on DeepSeek. The report comes from a Telegram channel that did not link to the original order, so the exact wording and scope have not been independently confirmed.

telegram · aipluscn · Oct 21, 01:51

**「Background」** DeepSeek is a Chinese company that makes AI models — the underlying software that powers chatbots and other tools — and other companies can build their own products on top of those models. That is why the order reaches beyond DeepSeek-branded apps to third-party services built with its technology. The source says the Defense Department and intelligence agencies had already imposed similar limits, so this extends the restriction to civilian federal agencies \(government departments outside the military\).

**「Who has to act」** The practical burden falls on companies that sell software to US civilian agencies: a product that quietly sends queries to a DeepSeek model, even inside a larger tool from another vendor, would now have to be removed or reworked. Vendors bidding on government work will likely need to document which AI models their products rely on. Ordinary users of DeepSeek&\#x27;s chatbot or app are not directly affected by this order, which covers government systems rather than consumer access.

<details><summary>References</summary>
<ul>
<li><a href="https://indrajitglobalnews.com/us-government-bans-deepseek-ai-federal-agencies/">US Orders Federal Agencies to Remove China’s DeepSeek AI Over...</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#访问限制`, `#美国政策`, `#政府采购`, `#AI供应链`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s MIIT Tightens Rules for Innovative Car Designs](https://m.chinanews.com/wap/detail/chs/zw/10717890.shtml) ⭐️ 7.0/10

China&\#x27;s Ministry of Industry and Information Technology said on Oct. 20 that it would bar market entry for auto products with unreasonable innovative designs or insufficient testing, and that 22 recommended standards would become mandatory, including reliability testing of at least 30,000 km.

telegram · zaihuapd · Oct 20, 12:48

**「Background」** China’s Ministry of Industry and Information Technology administers the country’s vehicle market-entry rules, and it had already issued a mandatory national standard for car door-handle safety \(GB 48001—2026\) due to take effect on Jan 1, 2027.

**「Impact」** Automakers and suppliers using hidden door handles, electric suction doors, or zero-gravity and rotating seats will need to adjust designs and complete testing to secure market access.

<details><summary>References</summary>
<ul>
<li><a href="https://www.douyin.com/shipin/7603935138652882995">汽 车 车 门 把 手 强 制 性 国家 标 准 发布-抖音</a></li>
<li><a href="https://m.dzplus.dzng.com/share/general/0/NEWS3126116DYYTTLEQLYDSN">m.dzplus.dzng.com/share/general/0/NEWS3126116DYYTTLEQLYDSN</a></li>

</ul>
</details>

**Tags**: `#auto safety regulation`, `#MIIT`, `#mandatory standards`, `#vehicle design`, `#China auto industry`

---

<a id="item-finance-news-2"></a>
### [SpaceX and Tesla Boards Form Special Committees to Review Possible Merger](https://techcrunch.com/2026/10/20/spacex-and-tesla-boards-form-special-committees-to-review-merger/) ⭐️ 7.0/10

SpaceX and Tesla said their boards have each set up special committees of independent directors to review a possible merger, with Elon Musk saying he will stay out of the discussions because of a conflict of interest. No deal terms have been agreed, and Musk said any transaction would still need shareholder approval — a simple majority of SpaceX shareholders, but 50% of all Tesla shareholders.

telegram · zaihuapd · Oct 21, 02:06

**「Background」** A special committee of independent directors is a standard board mechanism for weighing a deal in which senior management has a conflict of interest, which is why Musk said he would stay out of the discussions. Musk said both panels were set up at shareholders&\#x27; request.

**「What comes next」** Any completed deal would also need an antitrust filing with the U.S. Federal Trade Commission and Department of Justice, so clearance from regulators — not just the shareholder votes — would gate the combination.

<details><summary>References</summary>
<ul>
<li><a href="https://www.freemalaysiatoday.com/category/business/2026/10/21/musk-says-backs-spacex-tesla-merger-as-rocket-firm-turns-profit">Musk says backs SpaceX - Tesla merger as rocket firm turns profit | FMT</a></li>
<li><a href="https://tesorb.com/spacex-tesla-merger-requirements/">What a SpaceX-Tesla Merger Would Actually Require</a></li>

</ul>
</details>

**Tags**: `#Tesla`, `#SpaceX`, `#mergers and acquisitions`, `#corporate governance`, `#Elon Musk`

---