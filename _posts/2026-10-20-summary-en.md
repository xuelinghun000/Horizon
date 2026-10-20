---
layout: default
title: "Horizon Summary: 2026-10-20 (EN)"
date: 2026-10-20
lang: en
---

> From 137 items, 7 important content pieces were selected

---

**Technology News**
1. [OpenAI models reportedly reach 97.9% accuracy on COBOL migration](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenCode confirms breach; 1.4% of users&\#x27; model access keys may be exposed](#item-tech-news-2) ⭐️ 8.0/10
3. [Xiaomi&\#x27;s MiMo-V2.6-Pro model goes live on WorkBuddy](#item-tech-news-3) ⭐️ 7.0/10
4. [Inception releases Mercury 3, a diffusion language model claiming 1,000+ tokens per second](#item-tech-news-4) ⭐️ 7.0/10
5. [Open-source kit lets Claude Code configure an OpenWrt One router](#item-tech-news-5) ⭐️ 7.0/10

**Technology Blog**
1. [vLLM TorchTPU Brings vLLM Serving to Google Cloud TPUs](#item-tech-blog-1) ⭐️ 4.0/10

**Financial News**
1. [China Tightens Auto Market Entry Rules for Innovative Designs](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenAI models reportedly reach 97.9% accuracy on COBOL migration](https://openai.com/index/low-resource-programming-languages/) ⭐️ 8.0/10

A Telegram post summarizing an OpenAI publication says OpenAI&\#x27;s newest models sharply improved coding in rarely used languages such as COBOL \(an old language still running many bank and government systems\), Fortran and Visual Basic — the kind of software that companies struggle to maintain because few programmers learn it. In a test that builds a small database engine \(SQLite\) in 20 languages, a model called &quot;GPT-6 Astra&quot; reportedly raised the average pass rate from 26.8% for &quot;GPT-5.6 Sol&quot; to 87.4%, while the cheaper &quot;GPT-6 Luna&quot; reached 40.3% with API costs \(the per-use fees developers pay to send requests to a model\) down 78%. For converting old COBOL code into modern languages, &quot;GPT-6.1 Sol&quot; reportedly rose from 5.4% to 86.6% accuracy at low reasoning effort \(how much computation the model spends before answering\) with 39% lower cost, and reached 97.9% at high effort; the test set is said to be published openly on GitHub. These figures come from a single Telegram summary, the model names could not be checked against OpenAI&\#x27;s own announcement, and none of the results have been independently measured.

telegram · zaihuapd · Oct 20, 14:24

**「Background」** COBOL is an older programming language, and AI coding tools have had relatively little example code to learn from, which is what “low-resource” means here. OpenAI’s new MultiLangBench evaluation asks a model to build a small database engine from scratch in each of 20 languages, while a separate COBOL test asks it to translate old programs into five modern languages without changing their behavior, including financial calculations and output formatting.

**「What this means for legacy-code teams」** For the organizations still running COBOL — banks, insurers, government agencies — the practical change is that a large conversion job can now be attempted with a model instead of a hand rewrite, and the cheaper GPT-6 Luna tier is quoted at roughly 78% lower estimated API cost \(the pay-per-request interface programmers use to call a model\) than the previous model, which matters when a migration runs to millions of lines. Budget with the published rates in mind: GPT-6 Sol is listed at $2 per million input tokens and $10 per million output tokens \(tokens are the text chunks a model is billed by\), with a 1.05-million-token context window, meaning it can hold a very large source file in one pass. The 97.9% figure is a benchmark pass rate, not a guarantee, so plan for human review of converted code and test the open-sourced evaluation set against your own codebase before committing to a migration.

<details><summary>References</summary>
<ul>
<li><a href="https://dataconomy.com/2026/10/20/openai-gpt-6-cobol-coding-migration-gains/">GPT-6.1 Sol scores 97.9% on OpenAI’s COBOL test - Dataconomy</a></li>
<li><a href="https://aicoder.com/news/news-20261020-openai-multilangbench-cobol-migration-low-resource-languages">OpenAI open-sources MultiLangBench and reports low-resource ...</a></li>
<li><a href="https://openai.com/index/low-resource-programming-languages/">Advancing coding in low‑resource programming languages | OpenAI</a></li>
<li><a href="https://openrouter.ai/openai/gpt-6-sol">GPT - 6 Sol - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#coding models`, `#COBOL`, `#benchmarks`, `#API pricing`

---

<a id="item-tech-news-2"></a>
### [OpenCode confirms breach; 1.4% of users&\#x27; model access keys may be exposed](https://telegram.me/aipluscn/3135) ⭐️ 8.0/10

OpenCode, an open-source AI coding tool, confirmed that hackers breached its platform and that model access keys \(the credentials that let software call AI models\) stored there may have leaked for about 1.4% of its Console users. Before the confirmation, developers reported unexpected charges on their OpenAI and Anthropic accounts, ranging from hundreds of dollars to more than $1,700. OpenCode said the incident is connected to a “large-scale distillation attack” — a term for attempts to extract a model’s behavior through large numbers of queries — but that description has not been independently confirmed by OpenAI, Anthropic, or Google; OpenCode says it is working with all three.

telegram · aipluscn · Oct 20, 11:52

**「Background」** OpenCode is an open-source coding assistant that runs in a text command window, and its Console is the web dashboard where users connect accounts from model providers such as OpenAI, Anthropic and Google. External reports date the intrusion to the night of October 16–17, 2026, and say keys saved in affected Console workspaces may have been exposed. OpenCode has described the incident as a “distillation attack” — an attempt to use a model’s outputs to train a competing model — but that label has not been independently confirmed by the model providers.

**「What users should do」** For developers who stored model keys in OpenCode, the practical step is to check OpenAI and Anthropic billing for unexpected charges and to revoke and replace any keys kept on the platform; replacing a key makes the old one stop working.

<details><summary>References</summary>
<ul>
<li><a href="https://www.explainx.ai/blog/opencode-console-breach-stored-api-keys-distillation-attack-what-to-do-2026">OpenCode Console Breach: Rotate Your API Keys Now (1.4% ...</a></li>
<li><a href="https://cybersecuritynews.com/opencode-security-breach/">OpenCode Security Breach Exposes Third-Party API Keys of its ...</a></li>
<li><a href="https://www.cyera.com/blog/opencode-breach-what-happened-and-how-to-rotate-exposed-ai-api-keys">OpenCode Breach: What Happened and How to Rotate Exposed AI ...</a></li>

</ul>
</details>

**Tags**: `#opencode`, `#security-breach`, `#api-keys`, `#coding-agents`, `#access-restrictions`

---

<a id="item-tech-news-3"></a>
### [Xiaomi&\#x27;s MiMo-V2.6-Pro model goes live on WorkBuddy](https://weibo.com/6486870325/5356179212995907) ⭐️ 7.0/10

Xiaomi&\#x27;s technology team announced that its MiMo-V2.6-Pro model is now available on WorkBuddy, and says it can be tried there for free. Xiaomi claims the model scores 46 on the Artificial Analysis intelligence index, a third-party leaderboard that ranks AI models, and that this puts it first among openly available models. The company says it can handle a context window of 1 million tokens \(roughly the amount of text in several long books at once\), understand images, video, audio and text together, and split work across multiple AI agents. Xiaomi lists long-running task management, deep research, design drafts, office documents and small tool-building as target uses. The score is Xiaomi&\#x27;s own claim and has not been independently confirmed, and the announcement gives no pricing, no download links for the model&\#x27;s weights \(the files that would let others run it themselves\) and no details for developers who want to connect to it through software.

telegram · zaihuapd · Oct 20, 13:40

**「Context」** MiMo-V2.6-Pro is not a brand-new model: it first appeared in late September 2026, when it was reported to have scored 46 on the Artificial Analysis Intelligence Index — a public leaderboard that runs a fixed set of tests and ranks models by the results — the highest mark reported for an open-weight model, meaning one whose files are published so others can download and run it themselves. The &quot;1M context&quot; figure describes how much text the model can hold in one session: about one million tokens \(the word fragments models read text in\), roughly hundreds of pages at once. This item is about that model becoming available to try inside WorkBuddy.

**「What it costs to use」** On the model marketplace OpenRouter, MiMo-V2.6-Pro is listed at about $0.41 per million input tokens and $0.83 per million output tokens \(a token is a small chunk of text, roughly a word fragment\), with a context window of 1,050,000 tokens and four providers serving it. Xiaomi says API pricing is unchanged from the previous V2.5 model, so teams already calling that version can switch without reworking their budgets, and an &quot;UltraSpeed&quot; mode claims up to 20 times faster output for tasks where waiting is the bottleneck.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/mimo-v2-6-pro">MiMo-V2.6-Pro Intelligence, Performance &amp; Price Analysis</a></li>
<li><a href="https://shattered.io/mimo-v2-6-pro-xiaomi-claude-probe-2026/">MiMo-V2.6-Pro Scores 46 as Xiaomi Faces Claude Probe</a></li>
<li><a href="https://openrouter.ai/xiaomi/mimo-v2.6-pro">MiMo - V 2 . 6 - Pro - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://mimo.mi.com/models/en-US/mimo-v2.6-pro">Xiaomi MiMo Home</a></li>
<li><a href="https://mimo.xiaomi.com/mimo-v2-6">MiMo - V 2 . 6 | Xiaomi</a></li>

</ul>
</details>

**Tags**: `#Xiaomi MiMo`, `#open-weight models`, `#model release`, `#long context`, `#multimodal`

---

<a id="item-tech-news-4"></a>
### [Inception releases Mercury 3, a diffusion language model claiming 1,000+ tokens per second](https://telegram.me/aipluscn/3134) ⭐️ 7.0/10

Inception has released Mercury 3, a language model that generates text differently from most chatbots: rather than writing one word at a time, it fills in a whole block of text at once, an approach called a diffusion model. The company says it produces more than 1,000 tokens per second \(a token is a word fragment, roughly three-quarters of a word\), has about 40 times as many internal parameters as its predecessor Mercury 1, and accepts a context window of 1 million tokens — the amount of text it can take in and keep in mind at once. It is live on Inception&\#x27;s own API \(the paid interface that software uses to call a model\) and on OpenRouter, a marketplace that lets developers reach many models through one account, with input priced at $0.20 per million tokens. The post also says Mercury 3 beats GPT-6 Luna and Claude Haiku 5.5 on several benchmarks, but that comparison is vague and has not been independently verified.

telegram · aipluscn · Oct 20, 11:52

**「Background」** A diffusion language model generates text by refining a whole chunk of text in parallel rather than writing one word at a time, the approach behind its speed. Inception&\#x27;s earlier Mercury 2.5 was listed at 1,107 tokens \(word pieces\) per second, a 260,000-token context window \(how much text the model can consider at once\), and $0.20 per million input tokens versus $0.75 per million output tokens. Mercury 3 is the company&\#x27;s newest model; the source says it expands the context window to about 1 million tokens and uses roughly 40 times as many parameters \(internal settings that roughly track model size\) as Mercury 1.

**「What it means in practice」** The appeal is for work that needs large amounts of text generated quickly — bulk summarization, sorting documents into categories, or automated assistants that call a model many times per task — where the low input price and reported speed matter more than top-end reasoning. Because it is listed on OpenRouter, teams can try it without signing a new contract. Since it is a different kind of model, its output quality on a specific job should be tested against whatever is already in use rather than assumed from the speed and benchmark claims.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/inception/mercury-3">Mercury 3 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://www.inceptionlabs.ai/blog/introducing-mercury-2-5">Introducing Mercury 2 .5 – Inception</a></li>

</ul>
</details>

**Tags**: `#diffusion-LLM`, `#model-release`, `#pricing`, `#API-access`, `#high-throughput`

---

<a id="item-tech-news-5"></a>
### [Open-source kit lets Claude Code configure an OpenWrt One router](https://github.com/1507078/openwrt-one-skills) ⭐️ 7.0/10

A developer has published an open-source kit that gives AI coding assistants such as Claude Code and Codex a set of Agent Skills for the OpenWrt One, a router that ships with the open-source OpenWrt operating system. Agent Skills are packaged instructions and scripts that an assistant can load and run; the kit is released under the MIT open-source license. The three skills cover first-time setup \(inventorying the device, checking whether official software packages can be installed, and making a backup without changing settings\), setting the router up as a home gateway \(configuring the internet connection, moving from an internet provider&\#x27;s equipment, and setting Wi-Fi, with scripts to check the changes\), and diagnosing network-speed bottlenecks, heat and roaming problems without changing settings. The author says the pack has been tested on an actual OpenWrt One running OpenWrt 25.12.4, the router&\#x27;s operating software.

telegram · aipluscn · Oct 20, 12:44

**「Background」** OpenWrt is a free, open-source operating system for routers, and the OpenWrt One is a router designed to run it, with built-in recovery options such as a backup boot partition and a front USB-C console. Agent Skills is a package format that gives an AI agent task-specific instructions and scripts; Claude Code is Anthropic&\#x27;s terminal-based coding assistant that can read that format. Most home routers expose only a phone app or web settings page, with no command line for an agent to log into, which is why this kind of automation has been rare.

**「Impact」** The practical effect is limited to people who already own an OpenWrt One: they can try the pack with Claude Code or Codex, but it will not work as-is on ordinary consumer routers, which usually offer only a phone app and a web settings page rather than a command line for an assistant to operate. The setup skill changes internet and Wi-Fi settings, while the first-time and diagnostic skills are described as read-only.

**Tags**: `#Agent Skills`, `#Claude Code`, `#OpenWrt One`, `#home router automation`, `#open-source hardware`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [vLLM TorchTPU Brings vLLM Serving to Google Cloud TPUs](https://vllm.ai/blog/2026-10-20-vllm-torchtpu) ⭐️ 4.0/10

rss · vLLM Blog · Oct 20, 00:00

**「Background」** Inferact and Google have released vLLM TorchTPU, an out-of-tree backend for running vLLM on Google Cloud TPUs while reusing vLLM&\#x27;s existing model definitions. The stated goals are easier TPU onboarding for new models and stronger open-source TPU inference without changing the familiar vLLM interface.

**「Solution」** The plugin is discovered through vllm.platform\_plugins and runs models through vLLM&\#x27;s standard runner, compiling them with torch.compile\(backend=&quot;tpu&quot;\) to XLA; each TPU device gets a worker process, devices communicate via torch.distributed, and the scheduler, KV cache manager, workers, and API server remain upstream vLLM. TPU-specific work sits underneath in JAX/Pallas custom ops for ragged paged attention, dense and sparse MLA, hybrid linear-attention kernels, fused MoE with expert parallelism, and FP8/INT8/MXFP4/NVFP4 matmuls. The author reports support for all six vLLM parallelism dimensions—TP, DP, PP, EP, PCP, and DCP—on single- and multi-host slices, recommending data-parallel attention with expert parallelism for large MoE models and PCP/DCP for long-context prefill and KV cache splitting. Through vLLM&\#x27;s KV connector interface, the TPU Sync C++ library reads device buffers directly to enable zero-copy KV cache offloading to host DRAM and disaggregated prefill/decode with resharding during transfer; speculative decoding and automatic prefix caching, including hybrid-model linear-attention state, are also listed as supported, while TPU v7x is recommended and tested in CI, v6e/v5e/v5p are experimental, and the announcement offers no benchmarks or measured comparisons.

**「Takeaway」** The release positions TorchTPU as a way to extend vLLM&\#x27;s serving stack to TPUs without forking its core, pushing performance work into Pallas kernels and TPU-aware scaling features. Its roadmap—automated model onboarding, cache-aware routing, and broader TorchTPU kernel interfaces—aims at day-one support for new open models rather than a one-off port.

**Tags**: `#vLLM`, `#TPU inference`, `#Pallas kernels`, `#KV cache offloading`, `#model serving`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China Tightens Auto Market Entry Rules for Innovative Designs](https://m.chinanews.com/wap/detail/chs/zw/10717890.shtml) ⭐️ 7.0/10

China&\#x27;s Ministry of Industry and Information Technology said on Oct. 20 that it will tighten vehicle market entry, bringing hidden door handles, power-closing doors and virtual controls under approval management and converting 22 recommended standards into mandatory ones. The rules also require reliability testing of at least 30,000 km.

telegram · zaihuapd · Oct 20, 12:48

**「Background」** The Ministry of Industry and Information Technology sets China’s vehicle market-access rules, and hidden door handles have become increasingly common on new-energy cars there in recent years.

**「Impact」** Automakers that fit power-closing doors and zero-gravity seats to mid-to-high-end models priced at 200,000–500,000 yuan—including AITO, NIO and Li Auto—will need to modify or re-test those features to meet the new anti-pinch and in-motion restrictions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.iautodaily.com/news/review/gongxinbuzhengdunyincangshimenbashounihaixiwangguanguanneixi/">工 信 部 整顿 隐 藏 式 门 把 手 ，你还希望管管哪些鸡肋功能？_ 汽 车 公 社</a></li>
<li><a href="https://k.sina.com.cn/article_6023189492_1670293f400101k39e.html">k.sina.com.cn/article_6023189492_1670293f400101k39e.html</a></li>
<li><a href="https://www.163.com/dy/article/L0J5F7KI05148UNS.html">163.com/dy/article/L0J5F7KI05148UNS.html</a></li>

</ul>
</details>

**Tags**: `#中国汽车监管`, `#工信部`, `#汽车安全标准`, `#强制性标准`, `#产品准入`

---