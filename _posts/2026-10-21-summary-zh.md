---
layout: default
title: "Horizon Summary: 2026-10-21 (ZH)"
date: 2026-10-21
lang: zh
---

> 从 136 条内容中筛选出 18 条重要资讯。

---

**科技新闻**
1. [16GB Mac 继续训练 AI 模型：PyTorch MPS 与 Apple MLX 实测对比](#item-tech-news-1) ⭐️ 7.0/10
2. [小米 MiMo-V2.6-Pro 上线，称开源模型第一](#item-tech-news-2) ⭐️ 7.0/10
3. [OpenAI 称新模型把 COBOL 迁移准确率提高到 97.9%](#item-tech-news-3) ⭐️ 7.0/10
4. [OpenAI 接口提示缓存延长至 12 小时](#item-tech-news-4) ⭐️ 7.0/10
5. [Mistral 发布 Voxtral 3 语音模型和语音助手开发包](#item-tech-news-5) ⭐️ 6.0/10
6. [开发者把全天监听的应用放进 MacBook 刘海，替 Claude Code 派活](#item-tech-news-6) ⭐️ 6.0/10
7. [四款 Claude 与 ChatGPT 模型做同样八道编程题：正确率相近，价格最多差五倍](#item-tech-news-7) ⭐️ 6.0/10
8. [俄语文章盘点 10 个 API 中转站：免费或极低价调用 DeepSeek、GLM、GPT](#item-tech-news-8) ⭐️ 6.0/10
9. [Google 开源 TorchTPU：PyTorch 代码几乎不改就能跑在 TPU 上](#item-tech-news-9) ⭐️ 6.0/10
10. [DeepSeek 在 GitHub 发布 DeepInfer 推理框架，暂无技术细节](#item-tech-news-10) ⭐️ 5.0/10
11. [Veo 3.1 预览版即将停用，开发者实测迁移到 Gemini Omni Flash 的差异](#item-tech-news-11) ⭐️ 5.0/10
12. [用户用 Claude Code 清理智能电视首页广告](#item-tech-news-12) ⭐️ 5.0/10
13. [用 Claude Code 监控并唤醒 Codex：一名用户分享的终端工作流](#item-tech-news-13) ⭐️ 5.0/10
14. [MiniMax M3.1 Flash 在 Cline 免费开放，性能与 Space Bunny 归属未获证实](#item-tech-news-14) ⭐️ 5.0/10
15. [Ottili ONE 发布 39 个 AI Agent 技能包，适配 Claude Code 与 Codex](#item-tech-news-15) ⭐️ 5.0/10
16. [美国国土安全部下令联邦文职机构移除 DeepSeek 产品](#item-tech-news-16) ⭐️ 5.0/10

**财经新闻**
1. [工信部将隐藏式门把手等设计纳入汽车准入管理](#item-finance-news-1) ⭐️ 7.0/10
2. [SpaceX 与特斯拉董事会设特别委员会审议合并](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [16GB Mac 继续训练 AI 模型：PyTorch MPS 与 Apple MLX 实测对比](https://habr.com/ru/companies/otus/articles/1090656/?utm_campaign=1090656&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 7.0/10

Habr 上的一篇翻译实测文章比较了在 16 GB 内存的 Apple Silicon（苹果自研芯片）Mac 上，用 PyTorch MPS（PyTorch 调用 Mac 图形处理器加速的接口）和 Apple MLX（苹果为自家芯片开发的机器学习框架）继续训练（微调）大语言模型的表现。文章称，MLX 在微调时可能比 PyTorch MPS 慢几倍；但当 MPS 因内存不足而无法继续时，MLX 能运行大约两倍大的模型。测试用 Qwen 2.5（一个可在本地运行的语言模型系列）做了 10 次运行，覆盖不同模型大小和上下文长度（模型一次能处理的文本量）。

rss · Habr AI · 10月20日 17:46

**「背景」** MLX 是苹果专为自家芯片设计的机器学习框架；PyTorch 是更通用的主流框架，它通过 MPS 这个接口调用苹果芯片的图形处理器来加速计算。这里说的“微调”，是指拿一个已经训练好的模型，用你自己的数据继续训练，让它更符合特定用途，而这一步通常比单纯运行模型更吃内存。16 GB 的 Mac 使用统一内存，处理器和图形处理器共用这 16 GB，所以模型多大、一次能处理多长的文本，都会直接影响它能不能跑起来。

**「实际影响」** 如果你在 16 GB Mac 上微调模型，实际选择要看目标模型能否装下：短上下文、小模型可优先试 MPS 以争取速度；一旦出现内存不足，再换 MLX，可能慢几倍，但能装下约两倍大的模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://metalcloud.space/blog/mlx-vs-pytorch-comparison/">MLX vs PyTorch: When to Use Apple&#x27;s ML Framework</a></li>

</ul>
</details>

**标签**: `#Apple MLX`, `#PyTorch MPS`, `#local LLM fine-tuning`, `#Qwen 2.5`, `#Apple Silicon`

---

<a id="item-tech-news-2"></a>
### [小米 MiMo-V2.6-Pro 上线，称开源模型第一](https://weibo.com/6486870325/5356179212995907) ⭐️ 7.0/10

小米技术宣布，MiMo-V2.6-Pro 模型已在 WorkBuddy 平台开放体验。小米称该模型在 Artificial Analysis 智能指数（第三方模型评测榜单）上得 46 分，位列全球开源模型（通常指权重可被外部下载、修改和自行部署的模型）第一；这一分数和排名来自厂商公告，尚无独立验证。它支持 100 万 token 的上下文窗口（一次可处理的文本量约为 100 万个 token；token 是模型处理文字的基本单位），能联合理解图像、视频、音频和文本，并让多个 AI 智能体（各自负责一部分任务的 AI 角色）分工协作。目前没有公布价格、使用额度、许可证或模型权重下载信息。

telegram · zaihuapd · 10月20日 13:40

**「背景」** MiMo 是小米自研的大模型系列，V2.6 系列此前已经发布；小米官方称，其中 V2.6-Pro 在 Artificial Analysis 智能指数上得到 46.32 分，超过 Kimi K3、Qwen3.8 Max 等开源模型。Artificial Analysis 智能指数是第三方机构用一套统一试题给各家模型打分并排名，常被用来横向比较能力，但分数只反映那套试题考的内容。所谓“1M 上下文”，指模型一次能读入约 100 万个词元（模型处理文字的最小单位），因此可以把很长的资料整体交给它，而不必先切成小段。

**「实际影响」** 对需要处理长文档、视频或音频，或把复杂任务拆给多个 AI 分头执行的用户，现在可以直接去 WorkBuddy 试用；但如果打算自行部署或商用，目前还缺少许可证、权重下载和价格信息，不能仅凭“开源第一”就假定可以自由使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mimo.xiaomi.com/mimo-v2-6">MiMo-V2.6 | Xiaomi</a></li>
<li><a href="https://mimo.mi.com/models/en-US/mimo-v2.6-pro">Xiaomi MiMo-V2.6 Series: 3 New Models Officially Released</a></li>

</ul>
</details>

**标签**: `#model release`, `#Xiaomi MiMo`, `#open-weight models`, `#long context`, `#benchmarks`

---

<a id="item-tech-news-3"></a>
### [OpenAI 称新模型把 COBOL 迁移准确率提高到 97.9%](https://openai.com/index/low-resource-programming-languages/) ⭐️ 7.0/10

一则 Telegram 摘要称，OpenAI 公布了新模型在 COBOL 等“低资源编程语言”（训练数据较少、平时少有人用的语言）上的评测结果，称其代码生成和旧代码迁移能力大幅提升。在让模型用 20 种语言从零构建 SQLite 数据库引擎的测试中，GPT-6 Astra 的平均通过率从上一代 GPT-5.6 Sol 的 26.8% 升到 87.4%；低成本型号 GPT-6 Luna 为 40.3%，API（开发者付费调用模型的接口）成本下降 78%。在把老旧 COBOL 代码改写成现代语言的测试中，GPT-6.1 Sol 在低推理强度（模型答题前思考较少）下准确率从 5.4% 升到 86.6%，成本降低 39%；高推理强度下达到 97.9%。这些数字来自 OpenAI 自述的评测，相关评测集已在 GitHub 开源，但摘要没有给出模型正式发布或 API 定价信息，尚不能独立核实，也不应据此直接调整采购或迁移预算。

telegram · zaihuapd · 10月20日 14:24

**「背景」** COBOL、Fortran 这类语言被称为“低资源”，不是因为没人用，而是因为公开代码和训练资料少，AI 模型过去很少接触到它们；有报道称，COBOL 仍支撑超过 40% 的网上银行系统。OpenAI 这次公布的 MultiLangBench 要求模型从零写一个与 SQLite（一种常见的轻量数据库软件）兼容的数据库引擎，并在 20 种编程语言上分别测试。另一项 COBOL 迁移测试则是把旧代码改写成现代语言，考察模型能否处理真实的老系统。

**「对使用者的实际影响」** 对仍在维护 COBOL 老系统的银行、保险和政府部门来说，实际变化是：把老代码自动改写成现代语言，从过去几乎不可行（成功率 5.4%）变成可以先做小范围试点的程度；但 97.9% 出自 OpenAI 自己的评测集，并非独立复现的结果。评测集已在 GitHub 开源，技术团队可以先用自己的一段真实代码试跑，再决定是否投入。选型时还要注意：便宜得多的 GPT-6 Luna 通过率只有 40.3%，而据外部报道，OpenAI 已在 2026 年 9 月把 GPT-6 Sol 和 Luna 的 API 价格下调一半，帖子所称 Luna 成本再降 78% 属于另一项尚未被独立核实的说法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kucoin.com/news/flash/openai-improves-gpt-6-s-legacy-programming-capabilities-in-cobol-and-fortran">OpenAI Enhances GPT - 6 ’s Legacy Programming Capabilities... | KuCoin</a></li>
<li><a href="https://jendume.com/en/news/gpt-6-modelleri-dusuk-kaynakli-programlama-dillerinde-basari-sagladi/">GPT - 6 models advance coding in low-resource... | JEN DUME</a></li>
<li><a href="https://felloai.com/gpt-6-sol-luna/">GPT-6 Sol and Luna: OpenAI Halves Its API Prices</a></li>
<li><a href="https://www.unite.ai/openai-introduces-gpt-6-sol-and-luna-with-50-lower-api-prices/">OpenAI Introduces GPT-6 Sol and Luna With 50% Lower API ...</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#COBOL migration`, `#low-resource languages`, `#model benchmarks`, `#API pricing`

---

<a id="item-tech-news-4"></a>
### [OpenAI 接口提示缓存延长至 12 小时](https://x.com/OpenAIDevs/status/2112603916076781778) ⭐️ 7.0/10

OpenAI 的开发者账号在 X 上宣布，其 API（应用程序接口，开发者调用 OpenAI 模型的通道）的提示缓存（把之前发过的指令和上下文存下来，重复使用时按更便宜的“缓存输入”价格计费）现在可以保留 12 小时。这样一来，长时间运行的智能体（能自己连续执行任务的程序）可以全天反复复用同一套指令、工具说明和上下文，即使两次请求间隔数小时，仍按较低的缓存价格计费。此外，登录使用 Codex 和 Work 的用户获得“永久缓存”：回到旧对话或暂停数小时后继续，都不会因此失去缓存，OpenAI 保证命中缓存。这条消息来自 X 帖子，没有给出具体价格数字或文档链接，属于厂商说法。

telegram · zaihuapd · 10月21日 01:21

**「背景」** 提示缓存（prompt caching）是指把请求中重复出现的开头部分，例如系统指令、工具说明和长上下文，暂存起来供后续请求直接复用，从而不必每次重新处理，并按更低的缓存输入价格计费。对需要长时间运行的智能体（能自行连续调用工具完成任务的程序）来说，缓存能保留多久，直接决定它隔几小时再工作时是否还要为同一段内容重复付费。

**「对长时间运行智能体的实际影响」** 对需要让智能体（能自己连续执行多步任务的程序）长时间运行的开发者来说，最直接的变化是两次请求之间可以隔上几个小时，仍然按缓存输入的低价计费。OpenAI 在 2024 年 10 月介绍这项功能时，缓存通常在闲置 5 到 10 分钟后被清除，最迟在最后一次使用后一小时内移除；现在这个窗口延长到了 12 小时。缓存对支持的模型默认开启，不需要改代码，但官方没有公布具体价格，实际能省多少取决于用量；开发者可以在 Prompt Caching Dashboard 里查看缓存命中率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.openai.com/api/docs/guides/prompt-caching">Prompt caching | OpenAI API</a></li>
<li><a href="https://openai.com/index/api-prompt-caching/">Prompt Caching in the API - OpenAI</a></li>

</ul>
</details>

**标签**: `#openai`, `#prompt-caching`, `#api-pricing`, `#codex`, `#developer-tooling`

---

<a id="item-tech-news-5"></a>
### [Mistral 发布 Voxtral 3 语音模型和语音助手开发包](https://mistral.ai/news/voxtral-3/) ⭐️ 6.0/10

Mistral 发布了 Voxtral 3，这是一款语音模型，并配有语音助手开发包（一套让开发者把“听、思考、调用工具、说话”接进自己产品的工具）。Mistral 对开发包的描述是，它能在电话或网页的实时对话中完成这些步骤，让语音助手查询信息、操作业务系统并完成任务。但这次发布没有给出基准测试、价格或具体获取方式，因此转录质量、能否离线使用以及普通用户何时能用上都还不清楚。

hackernews · ilreb · 10月20日 16:02 · [社区讨论](https://news.ycombinator.com/item?id=50168396)

**「背景」** 语音模型通常做两件事：把说的话转成文字（语音识别），以及把文字读出来（语音合成）。所谓“语音智能体”，是把这两步和模型的理解、调用外部系统串成一个实时循环，用户打电话或在网页上说话时，系统边听、边想、边回答。Mistral 的 Voxtral 系列此前已推出过语音识别模型；有评论者提到，上一代 Voxtral Mini 4B Realtime 是开放权重（参数可下载、能自行部署）的，他用 4GB 显存就在普通笔记本上实现了离线实时转写。这次 Voxtral 3 把语音模型和一套语音智能体开发工具（SDK，帮开发者少写底层代码的软件包）一起发布。

**「对实际使用者的影响」** 对做会议记录或客服录音转写的团队来说，Voxtral Small Transcribe 3 能标出每句话是谁说的，还允许事先给一份关键词表来减少人名、术语被听错，这两点直接决定转写稿能不能拿来就用。但想在本地离线跑的人要注意：有评论者指出这一代是闭源模型，此前能在普通笔记本上离线运行的 Voxtral Mini 仍是自建方案，一位开发者称其 Windows 软件只需 4GB 显存就能实时转写。若通过 OpenRouter 调用其语音合成模型，标价是每百万字符 13 美元。

**「社区讨论」** 评论区最有用的一条实际经验来自一位开发者：他说上一代 Voxtral Mini 4B Realtime 已能在只有 4GB 显存（显卡内存）的普通笔记本上离线转写，速度超过实时，并已被他做成商业 Windows 软件。另一位评论者则失望地认为 Voxtral 3 不公开模型文件，延续了语音模型难以本地部署的问题；也有人质疑演示场景不真实，并提醒把语音助手直接接入公司内网会有安全风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mistral.ai/news/voxtral-3/">Voxtral 3: Voice Agent SDK &amp; Speech Models in 50+ Languages</a></li>
<li><a href="https://www.technobezz.com/news/mistral-ai-voxtral-3-voice-agent-sdk">Mistral AI Launches Voxtral 3 With Voice Agent SDK and 50 ...</a></li>
<li><a href="https://mistral.ai/news/voxtral-3/">Voxtral 3 : Voice Agent SDK &amp; Speech Models in 50+ Languages</a></li>
<li><a href="https://openrouter.ai/mistralai/voxtral-mini-tts-3-0">Voxtral TTS 3 - API Pricing &amp; Providers | OpenRouter</a></li>

</ul>
</details>

**标签**: `#Mistral`, `#Voxtral 3`, `#speech-to-text`, `#voice-agents`, `#model-release`

---

<a id="item-tech-news-6"></a>
### [开发者把全天监听的应用放进 MacBook 刘海，替 Claude Code 派活](https://habr.com/ru/articles/1097006/?utm_campaign=1097006&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一位开发者发布了一个采用 MIT 许可证（允许他人自由使用和修改代码的开源许可证）的 macOS 应用，它常驻在 MacBook 屏幕顶部的“刘海”区域，以一只 3D 浣熊的形象全天监听麦克风，把口述内容整理成任务，等用户说“好”之后发送到对应的 Claude Code 会话（Claude Code 是 Anthropic 的命令行编程助手，按指令改代码；一次会话相当于一段独立对话）。应用还会显示订阅的每周额度还剩多少、今天可以花多少。作者称约 4900 行代码全部是在与 Claude Code 的对话中写成的，他没有手改一行。他也提到一次代价不小的故障：语音识别悄悄停止工作，麦克风却一直开着，让他白录了一小时。

rss · Habr AI · 10月20日 22:18

**「背景」** Claude Code 是 Anthropic 推出的编程助手，用户可以在终端（用文字输入命令的窗口）里给它下指令，让它读写代码、执行命令；其订阅服务按周设有使用额度。MacBook 屏幕顶部的摄像头凹口常被称为“刘海”，开发者可以把自己的小程序显示在这块区域。

**「实际影响」** 想尝试的人要注意两点：这个应用只针对带刘海的 MacBook，而且作者遇到的静默失败说明麦克风指示灯亮着并不等于内容被正确转写，重要任务最好回看记录再确认。额度显示则能帮订阅用户判断当天还能派多少任务，避免每周额度提前用完。

**标签**: `#Claude Code`, `#AI agents`, `#open source`, `#macOS`, `#developer tooling`

---

<a id="item-tech-news-7"></a>
### [四款 Claude 与 ChatGPT 模型做同样八道编程题：正确率相近，价格最多差五倍](https://habr.com/ru/companies/syntx_ai/articles/1096542/?utm_campaign=1096542&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

SYNTX.AI 公司在 Habr 上发文称，他们用八道相同的编程题测试了四款模型——Claude Opus 5.5、Claude Sonnet 5.5、ChatGPT 6 Astra 和 ChatGPT 6.1 Sol，四款模型都第一次就写出了正确的代码，只有一份答案需要重新排版。差别出现在三处：跑完八道题的总耗时从 8 分钟到 28 分钟不等；按 token（模型计费所依据的最小文本单位）计算的价格最多相差 5 倍；写出的解法结构也不一样。目前这篇文章只是导语，没有给出逐题结果、测试环境或评分标准，文中这四个模型名称也与公开可查的版本对不上，因此这些结论还需要等完整内容或独立复现来验证。

rss · Habr AI · 10月20日 08:11

**「背景：这四款模型是什么关系」** 这四款模型来自两家公司的两档产品：Anthropic 的 Claude Opus 5.5 和 Claude Sonnet 5.5，以及 OpenAI 的 ChatGPT 6 Astra 和 ChatGPT 6.1 Sol。据 DataCamp 的报道，OpenAI 在 9 月 29 日的 DevDay 上发布了中端的 GPT-6.1 Sol，称其水平接近旗舰 GPT-6 Astra，而按 token（模型处理文字的最小计费单位）计算的价格只有后者的五分之一；Anthropic 则在一周前推出 Claude Opus 5.5，主打用低约四成的价格换来接近上一代旗舰的表现。两家都在推“性能够用、单价更低”的型号，因此同一批编程任务上到底谁更划算，需要实测来回答。

**「选型落到速度与花费」** 对打算用这些模型写代码的人来说，既然四个模型都能一次写对，实际选择就落在速度和花费上：文章测得跑完八道题的总耗时在 8 到 28 分钟之间，每 token（模型计费的最小文字单位）价格最多相差 5 倍。动手前还要先确认自己的账号能不能用——据 Convly 的对比，Claude Sonnet 5.5 在免费套餐内可用但有额度限制，GPT-6.1 Sol 需要付费的 ChatGPT 套餐；OpenRouter 列出的 Claude Opus 5.5 价格为每百万输入 token 4 美元、每百万输出 token 20 美元。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.datacamp.com/blog/gpt-6-1-sol-vs-opus-5-5">GPT-6.1 Sol vs. Claude Opus 5.5: Which Model to Use</a></li>
<li><a href="https://convly.ai/gemini-4-argon-vs-gpt-6-1-sol-vs-claude-sonnet-5-5/">Gemini 4 Argon vs GPT - 6 .1 Sol vs Claude Sonnet 5 . 5 | Convly</a></li>
<li><a href="https://kie.ai/blog/claude-opus-5-5-tuesday-checkpoint-signal">Claude Opus 5 . 5 Release Deep Dive</a></li>

</ul>
</details>

**标签**: `#model comparison`, `#Claude`, `#ChatGPT`, `#coding`, `#pricing`

---

<a id="item-tech-news-8"></a>
### [俄语文章盘点 10 个 API 中转站：免费或极低价调用 DeepSeek、GLM、GPT](https://habr.com/ru/articles/1096538/?utm_campaign=1096538&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

10 月 20 日，俄语技术社区 Habr 上的一篇文章盘点了 10 个 API 中转服务（第三方转发站：你把请求发给它，它再转给 DeepSeek、GLM、GPT 等模型厂商），这些服务提供免费模型、每日额度或注册赠送金额。作者称自己逐个注册试用，检查了哪些模型可以免费或极低价使用、存在哪些限制、接口调用是否真的能通，还看了是否有俄语界面、能否用卢布付款、以及在俄罗斯不挂 VPN 能否打开网站。名单包括 OrcaRouter、TeamoRouter、Srazu、RockAPI、OpenRouter、llmgw、VseGPT、Token Harbor、NaraRouter 和 FreeRouter。不过目前可见的内容只有开头介绍，文中承诺的两张汇总表和 17 张后台截图（具体价格、额度与测试结果）并不在可见部分，因此这些数字无法在此核实。

rss · Habr AI · 10月20日 07:08

**「背景」** API 路由器（一种中转服务）介于用户和模型公司之间：用户把请求发给它，它再转发给 DeepSeek、OpenAI 等模型，因此一个入口就能调用多家模型。这类服务不是模型开发者，免费额度、价格和可用性由各中转商自行设定，也可能随时变化；这篇汇总检查的正是这些第三方服务，而不是模型公司本身。

**「对使用者的实际影响」** 这类 API 路由器（中转服务，替你向模型厂商转发请求的中间商）大多兼容 OpenAI 的接口格式，所以如果你用的客户端或工具支持自定义接口地址，通常只要把地址和密钥换成中转商提供的，就能继续用原来的工具，不必改代码——TeamoRouter 的文档就写明它同时支持 OpenAI、Gemini 和 Anthropic 三种格式。但这篇汇总只给了结论，没有公布具体价格、每日额度和测试数据，作者所说的“免费额度”和“几乎免费”无法从文中核实，付费前最好先用最小额度试一次，确认调用真能通、限额与宣传一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://teamorouter.com/docs/api-integration">TeamoRouter API Integration Guide · Docs</a></li>

</ul>
</details>

**标签**: `#API routers`, `#DeepSeek`, `#GLM`, `#pricing`, `#regional access`

---

<a id="item-tech-news-9"></a>
### [Google 开源 TorchTPU：PyTorch 代码几乎不改就能跑在 TPU 上](https://cloud.google.com/blog/topics/ai-infrastructure/torchtpu-is-now-open-source-run-native-pytorch-on-tpus) ⭐️ 6.0/10

Google Cloud 宣布，与 Meta 的 PyTorch 团队共同开发的 TorchTPU 已在 GitHub 开源。PyTorch 是 Meta 维护的开源 AI 框架，开发者用它训练和运行模型；TPU 是 Google 自研的 AI 专用芯片。此前 PyTorch 主要面向英伟达的 GPU（图形处理器，AI 计算最常用的芯片），现在 TPU 成为与 GPU、CPU 并列的原生选项，现有代码几乎无需改动即可运行。vLLM、SGLang、llm-d、TorchTitan 等常用工具已接入，Hugging Face Transformers v5 可直接把模型部署到 TPU。这是代码层面的开源发布，公告没有提到价格、使用配额或开放区域的变化。

telegram · zaihuapd · 10月21日 00:47

**「背景」** PyTorch 是开发者用来搭建和训练 AI 模型的开源软件框架；TPU 是 Google 自研的 AI 加速芯片。此前，用 PyTorch 写的程序主要面向 NVIDIA 的 GPU（图形处理器，AI 计算常用芯片），想跑在 TPU 上通常要额外适配。TorchTPU 的作用是让 TPU 成为 PyTorch 直接支持的硬件选项，使同一套代码更容易在 Google 的芯片上运行。

**「对使用者的实际影响」** 对用 PyTorch 写模型的团队来说，同一份代码可以少改甚至不改就搬到 TPU 上跑，省去为换芯片重写代码的工夫。但能否真正用上，还取决于两件事：一是有没有 TPU 算力可用（通常要在 Google Cloud 上租用），二是所用工具链的版本，例如部署到 TPU 需要 Hugging Face Transformers v5。

**「社区讨论」** 有开发者（pcmoritz）说自己做了面向 Tenstorrent 加速器的开源 libtpu 实现，已能运行 TorchTPU 的大部分功能；npalli 指出亚马逊为自家芯片 Trainium 做了类似项目 torch-neuronx。fancyfredbot 认为 XLA（TPU 使用的编译器）可能比 PyTorch 自带的 inductor 编译器更好，并称这基本给 TensorFlow 画上句号；ismailmaj 则回忆过去要让 PyTorch 在 TPU 上跑得反复和 XLA 较劲，如今有了官方支持，认为 JAX 与 PyTorch 的选择更像风格偏好。这些均为个人观点。

**标签**: `#TorchTPU`, `#PyTorch`, `#TPU`, `#Google Cloud`, `#open source`

---

<a id="item-tech-news-10"></a>
### [DeepSeek 在 GitHub 发布 DeepInfer 推理框架，暂无技术细节](https://github.com/deepseek-ai/DeepInfer) ⭐️ 5.0/10

DeepSeek 的 GitHub 账号（deepseek-ai）下出现了一个名为 DeepInfer 的项目，标题称它是为 DeepSeek 自家模型打造的高性能推理框架（推理框架指把训练好的模型跑起来、让它能对外回答问题的软件）。该条目于 2026 年 10 月 20 日出现在 Hacker News 上，但公开信息里没有说明文档、跑分数据、安装步骤或授权条款，因此目前无法判断它支持哪些硬件、速度如何、DeepSeek 以外的人能否直接使用。换句话说，现在能确认的只是一个仓库名称和一句定位描述，而不是已经可以验证的性能成果。

hackernews · ggcr · 10月20日 09:08 · [社区讨论](https://news.ycombinator.com/item?id=50163277)

**「背景」** DeepInfer 是 DeepSeek 用来运行自家模型的推理框架（把训练好的模型跑起来、让它能回答问题的软件）。据其 GitHub 说明，这套框架原本支撑 DeepSeek 的大规模生产服务；10 月 20 日公开的版本以允许他人自由使用和修改的 Apache-2.0 许可证发布，主要基于另一个开源推理引擎 vLLM 构建，但只覆盖离线推理（先批量处理请求，而不是直接支撑在线服务），不包含 KV 缓存（避免重复计算、加快连续对话的缓存机制）和 PD 分离（把请求处理拆到不同机器上的做法）等在线服务常用组件。

**「自建部署前要先补齐一块」** 对打算在自己机器或自有服务器上跑 DeepSeek 模型的人来说，这个仓库目前还不是开箱即用的完整服务：项目页说明，要组成一套完整的推理服务还需要自备 KV 缓存系统（把对话上下文暂存起来、避免每轮重新计算的组件），而这一部分本次并未包含在发布里。项目页面同时提到支持华为升腾 950 芯片，所以它更直接相关的是使用非英伟达硬件的团队；如果只是想在现有英伟达显卡上试跑，需要先确认自己的环境是否在支持范围内。

**「评论区讨论」** 评论区的说法大多未获证实：有人引用一篇中文文章，称基于该框架已为“DeepSeek V4.1 Flash”提供单集群每天 155 万亿个 token 的服务量、每张卡每小时 38 美元收入，但这些数字没有独立来源佐证。另有评论者认为，若开源推理代码能支持华为升腾 950 这类非英伟达芯片，小型实验室便可在此基础上扩展，从而削弱英伟达在 AI 硬件上的主导地位——这属于对前景的推测，而非已确认的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/DeepInfer">GitHub - deepseek-ai/DeepInfer: DeepInfer: High-performance ...</a></li>
<li><a href="https://cldnavi.com/en/blog/deepinfer-inference-framework-2026/">DeepInfer: DeepSeek open-sourced the inference framework ...</a></li>
<li><a href="https://www.marktechpost.com/2026/10/20/deepseek-deepinfer-open-source-inference-framework/">DeepSeek Open-Sources DeepInfer, the Inference Framework ...</a></li>
<li><a href="https://github.com/deepseek-ai/DeepInfer">GitHub - deepseek -ai/ DeepInfer : DeepInfer : High- performance ...</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#inference framework`, `#open-weight models`, `#self-hosting`, `#GitHub`

---

<a id="item-tech-news-11"></a>
### [Veo 3.1 预览版即将停用，开发者实测迁移到 Gemini Omni Flash 的差异](https://habr.com/ru/articles/1096576/?utm_campaign=1096576&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

Google 将于 2026 年 10 月 22 日关闭 Gemini API 中三个 Veo 3.1 视频生成预览版模型（veo-3.1-generate-preview、veo-3.1-fast-generate-preview、veo-3.1-lite-generate-preview），并推荐改用 gemini-omni-1.1-flash（Gemini Omni Flash）。一位用这套接口制作广告和短视频的开发者发文称，迁移不能只改模型名字：新模型使用另一套 Interactions API（程序调用模型生成内容的接口），传入参考图片的方式变了，而且取消了控制视频时长的参数。他记录了自己迁移时遇到的报错，并做了画质对比：新模型在部分场景不输旧版，在部分场景更差。他还演示了如何根据接口返回的数据计算单条视频的成本。以上画质与成本结论来自作者个人实测，并非 Google 公布的对比数据。

rss · Habr AI · 10月20日 08:05

**「背景」** Veo 3.1 是 Google 通过 Gemini API 提供的视频生成模型，开发者用代码调用它，把文字或图片变成短视频（Gemini API 是 Google 让外部程序调用自家模型的接口）。名字里带 preview 的版本属于提前开放、随时可能下线的试用版，Google 已宣布在 10 月 22 日停用三个 Veo 3.1 试用版，并指定 Gemini Omni Flash 作为替代。由于替代模型换了请求格式，原来调用 Veo 的代码不能只改模型名字，需要按新接口重写。

**「对现有调用方的影响」** 如果你的代码或自动化流程里写死了 veo-3.1-generate-preview 这类模型名，10 月 22 日之后这些调用会直接失败，需要提前换成 gemini-omni-1.1-flash。但能改的不能只是模型名：新接口传递图片的方式不同，而且没有时长参数，原来靠指定秒数控制片长的逻辑必须重写。费用也要重新核对，作者的做法是按 API 返回的用量计算每条片段的价格；外部价格页的计价单位并不统一（有按条 0.11 美元起，也有按秒约 0.10 美元），照搬旧估算容易算错。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.google.dev/gemini-api/docs/veo">Generate videos with Veo 3 . 1 in Gemini API | Google AI for Developers</a></li>
<li><a href="https://unifically.com/blogs/gemini-omni-1.1-flash">Gemini Omni 1.1 Flash API Pricing: From $0.11/Video (2026)</a></li>
<li><a href="https://omniflash-ai.com/blog/gemini-omni-flash-api-tutorial">Gemini Omni Flash API Tutorial: Model ID, Pricing, and ...</a></li>

</ul>
</details>

**标签**: `#Gemini API`, `#Veo 3.1`, `#video generation`, `#API migration`, `#model pricing`

---

<a id="item-tech-news-12"></a>
### [用户用 Claude Code 清理智能电视首页广告](https://mashable.com/tech/smart-tv-ads-claude-code-ai-cleanup) ⭐️ 5.0/10

有智能电视用户开始借助 Claude Code（一款 AI 编程助手，用户用自然语言下达指令，它就能代为操作电脑和代码）清理电视首页广告和预装软件。一名开发者 10 月 17 日称，他把 Claude Code 连接到小米电视，删除了 25 个软件包，从而绕过开机广告直接进入 Netflix。这些做法被汇总到开源项目 CleanYourTV（公开源代码、可自行使用的工具）。不过，使用前需要在电脑上运行 Claude Code，而且目前只支持 Android TV 和 Google TV（两种谷歌电视系统）；报道没有提供可复现的代码或安装证据。

telegram · zaihuapd · 10月20日 13:18

**「背景」** Android TV 和 Google TV 是谷歌的两套电视操作系统，底层沿用安卓，因此电视里的预装应用可以像手机应用一样被逐项停用或删除。Claude Code 是 Anthropic 的 AI 编程助手，用户可以用自然语言让它执行电脑上的命令；把它接到电视上，就相当于让一个懂命令行的助手代劳清理。过去这类“去广告、去预装”操作多靠用户手动输入命令，门槛较高。

**「想自己动手的人要先看兼容性」** 想照着做的用户得先确认自家电视的系统：CleanYourTV 只适用于运行 Android TV 和 Google TV 的机型，三星（Tizen）和 LG（webOS）用的是另一套系统，Fire TV 则只能做“去臃肿”这一半，无法换成第三方桌面。操作时还需要一台电脑运行 Claude Code，通过 Wi-Fi 连上电视执行。项目方称整个过程不需要 root（获取系统最高控制权限），也没有真正卸载应用，因此改动原则上可以恢复。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Gathin23/cleanyourtv/">GitHub - Gathin23/ cleanyourtv : Debloat any Android or Google TV ...</a></li>
<li><a href="https://cleanyour.tv/">CleanYourTV</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#Android TV`, `#debloating`, `#AI coding agents`, `#CleanYourTV`

---

<a id="item-tech-news-13"></a>
### [用 Claude Code 监控并唤醒 Codex：一名用户分享的终端工作流](https://linux.do/u/demouo) ⭐️ 5.0/10

10 月 21 日，Linux.do 用户 demouo 发帖介绍了一种个人工作流：在一个叫 herdr 的终端复用器（把同一个终端窗口分成多个标签页、让程序在后台继续运行的工具）里，一个标签页运行 Codex（一种 AI 编程助手），另一个标签页运行 Claude Code（另一种 AI 编程助手）充当“监工”，在 Codex 卡住等待时把它唤醒。作者称 Codex 本身没有后台监控和唤醒能力，而让主任务一直开着又太贵，所以用便宜的模型（他提到 deepseek-flash）来做监控；帖中举例说 Codex 在 1:28 和 9 点被唤醒。帖子没有给出代码、配置或可复现的步骤，模型名称（如“GPT-6-Astra”）和唤醒时间都只是作者自述，未经独立验证。

telegram · linuxdo\_tg · 10月21日 02:13

**「背景」** Claude Code 和 Codex 都是运行在终端（命令行窗口）里的 AI 编程助手，各自在一个会话中执行任务。herdr 是一款专门为同时运行多个这类助手而设计的终端工具，它用标签页和分屏把它们放进同一个窗口，并显示每个助手当前是在工作、已完成还是卡住。这篇帖子针对的情况是：Codex 在等待一个耗时较长的结果时会停住不动，需要另一个会话来把它叫醒、让它继续。

**「对使用者的实际影响」** 对经常让 AI 编程助手连续跑长任务的人来说，这个做法提供的是一条省钱的旁路：主任务继续跑，另开一个便宜会话盯着，卡住时叫醒它，而不是一直为高成本的主会话付费或反复手动查看。但它依赖 herdr 和两个同时运行的会话，作者还强调监控方只能通过 herdr 操作；在没有可复现步骤的情况下，这只能当作思路参考，实际成本与稳定性都未经验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.chaseai.io/blog/herdr-terminal-multiplexer-ai-coding-agents">Herdr : Run Claude Code + Codex in One Terminal - Chase AI</a></li>
<li><a href="https://www.shareuhack.com/en/posts/herdr-terminal-agent-multiplexer-guide-2026">herdr 2026: Monitor Claude Code , Codex &amp; Devin in One Terminal</a></li>

</ul>
</details>

**标签**: `#claude-code`, `#codex`, `#agent-orchestration`, `#developer-workflow`, `#terminal-multiplexer`

---

<a id="item-tech-news-14"></a>
### [MiniMax M3.1 Flash 在 Cline 免费开放，性能与 Space Bunny 归属未获证实](https://telegram.me/aipluscn/3149) ⭐️ 5.0/10

一条 Telegram 频道消息称，MiniMax M3.1 Flash 已在编程工具 Cline（一个可以选用不同 AI 模型来写代码的助手）中免费开放。该消息还称，它的编程能力接近 Claude Opus 和 GPT 系列，使用成本比对比模型低约 25 倍，并称它就是此前以超过 200 万亿 token（模型处理文字的最小计量单位，常用来衡量用量）登顶使用榜的匿名模型 Space Bunny。这些说法都没有给出官方公告、价格页面或可复现的测试数据，消息本身也用了“据称”“有消息称”等不确定措辞，因此免费开放的具体范围、性能对比结果以及 Space Bunny 的归属目前都未得到证实。

telegram · aipluscn · 10月20日 14:59

**「背景」** Cline 是一款装在代码编辑器里的编程助手，用户下达任务后，它能自己读文件、改代码、执行命令，因此它接入哪个模型、按什么价格计费，直接决定使用者的开销。MiniMax 是一家中国大模型公司；此前模型调用榜上出现过一个叫「Space Bunny」的匿名模型，没有公开开发方，却凭超过 200 万亿 token（模型处理文字的基本计量单位，可粗略理解为字数）的调用量登上榜首。这条 Telegram 消息把两者联系起来，称 Space Bunny 的真身就是 MiniMax M3.1 Flash，但免费开放和这层身份目前都只有转述，没有官方公告或可核对的测试数据。

**「对使用者的实际影响」** 对使用 Cline 这类编程助手的人来说，最直接的变化是可以不花钱就把改代码、修 bug 这类日常任务交给这个模型试跑，在不增加预算的前提下和现有模型比一比效果。但“比肩 Claude Opus 与 GPT”目前只是转述，公开的模型页面只列出一项基准测试成绩（Terminal-Bench 4.0 得 25.8%，即用统一任务给模型打分的测试），没有与 Opus、GPT 的正面对比数据，所以在把重要项目迁过去之前，最好先拿自己熟悉的代码任务实测一遍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/minimax/minimax-m3.1-flash:free">MiniMax M 3 . 1 Flash (free) - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**标签**: `#MiniMax`, `#Cline`, `#free access`, `#model release`, `#pricing`

---

<a id="item-tech-news-15"></a>
### [Ottili ONE 发布 39 个 AI Agent 技能包，适配 Claude Code 与 Codex](https://github.com/Ottili-ONE/skills) ⭐️ 5.0/10

Ottili ONE 在 GitHub 上发布了一个含 39 个「技能包」的合集，供 Claude Code 和 Codex 这类 AI 编程助手使用；这两者分别是 Anthropic 和 OpenAI 推出的工具，能读写代码并执行开发任务。技能包可以理解为预先写好的操作说明和脚本，装上之后 AI 助手能按固定流程完成某类任务，不用每次从头交代。按发布方的说法，其中 10 个面向数据处理，10 个面向德国业务场景，10 个面向工程实践，其余 9 个没有说明。这是厂商自己发布的消息，没有安装演示、效果测试或实际使用数据，因此这些技能包是否好用、能否顺利装上，目前无法从材料中判断。

telegram · aipluscn · 10月21日 01:50

**「背景」** Claude Code 和 Codex 是能读写代码、执行命令的 AI 编程助手；“技能包”则是预先写好的操作说明和配套文件，安装后让助手在特定任务上按固定流程工作，类似给助手加一份可复用的操作手册。把多个技能包放在一个库里，使用者就能按任务类型挑选，而不必每次从零描述做法。

**「实际影响」** 对使用 Claude Code、Codex 这类工具的人来说，这意味着可以把现成的技能文件夹直接交给 AI 代理调用，而不必自己从零写指令。按该仓库的说明，每个技能都是包含指令、脚本和资源的文件夹，由 AI 代理自行发现并套用到具体任务上，因此启用前值得先翻看里面的脚本内容，确认它会在你的项目里做什么。另外，发布信息只说明适用于 Claude Code、Codex 等平台，并未交代这 39 个技能包分别兼容哪些平台、质量如何，采用前需要自行验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Ottili-ONE/skills">GitHub - Ottili - ONE / skills : Claude Code , Codex , OpenClaw and...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#Claude Code`, `#Codex`, `#skill library`, `#developer tooling`

---

<a id="item-tech-news-16"></a>
### [美国国土安全部下令联邦文职机构移除 DeepSeek 产品](https://telegram.me/aipluscn/3162) ⭐️ 5.0/10

美国国土安全部发布命令，将中国 AI 公司 DeepSeek 排除出联邦文职机构的采购范围，并要求各机构从自己的信息系统中移除所有 DeepSeek 产品，以及那些内置了 DeepSeek 的第三方产品和服务。命令援引美国网络安全相关法律作为依据。此前，美国国防部和情报部门已经对 DeepSeek 设过类似的使用限制。这一消息来自 Telegram 频道的转述，没有附上原始命令的链接，具体生效时间和执行细节尚不清楚。

telegram · aipluscn · 10月21日 01:51

**「背景」** DeepSeek 是一家中国人工智能公司，提供可对话的 AI 模型和产品。此前，美国国防部和情报机构已对 DeepSeek 设下类似使用限制；这次国土安全部的命令把范围扩大到联邦文职机构，也就是国防和情报系统之外的联邦政府部门。命令不仅针对 DeepSeek 自家产品，也覆盖用 DeepSeek 模型搭建的第三方产品和服务。

**「对实际使用者的影响」** 与美国联邦政府有合同关系的企业需要清点自己用的 AI 工具：如果产品里嵌入了 DeepSeek 的模型或调用接口，在政府项目里可能得换成别的供应商，否则会有合规风险。这条命令只针对政府文职机构的信息系统，普通用户订阅 DeepSeek 的聊天服务不受直接约束。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/security/2026/10/20/deepseek-deep-sixed-at-all-us-federal-civilian-agencies/5304010">DeepSeek deep -sixed at all US federal civilian agencies</a></li>
<li><a href="https://indrajitglobalnews.com/us-government-bans-deepseek-ai-federal-agencies/">US Orders Federal Agencies to Remove China’s DeepSeek AI Over...</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#访问限制`, `#美国政策`, `#政府采购`, `#AI供应链`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [工信部将隐藏式门把手等设计纳入汽车准入管理](https://m.chinanews.com/wap/detail/chs/zw/10717890.shtml) ⭐️ 7.0/10

中国工信部 10 月 20 日表示，将把隐藏式门把手、电吸门、虚拟操纵件等创新汽车设计纳入准入管理，并把 22 项推荐性标准升为强制性标准。通知要求电吸门具备防夹功能、禁止行驶中使用零重力座椅和旋转座椅，且可靠性测试不低于 3 万公里；总工程师王卫明称，未按要求申报或测试验证不充分的产品不予准入。

telegram · zaihuapd · 10月20日 12:48

**「背景」** 监管此前已就车门把手单独立规：工信部组织制定的强制性国家标准《汽车车门把手安全技术要求》（GB 48001—2026）已发布，将于 2027 年 1 月 1 日起实施，对隐藏式门把手等设计提出统一安全技术要求。

**「影响」** 直接受影响的是采用这些设计的车企及零部件供应商：相关车型须在上市前完成合规测试并满足强制要求，否则无法获得市场准入。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.douyin.com/shipin/7603935138652882995">汽 车 车 门 把 手 强 制 性 国家 标 准 发布-抖音</a></li>
<li><a href="https://m.dzplus.dzng.com/share/general/0/NEWS3126116DYYTTLEQLYDSN">m.dzplus.dzng.com/share/general/0/NEWS3126116DYYTTLEQLYDSN</a></li>

</ul>
</details>

**标签**: `#auto safety regulation`, `#MIIT`, `#mandatory standards`, `#vehicle design`, `#China auto industry`

---

<a id="item-finance-news-2"></a>
### [SpaceX 与特斯拉董事会设特别委员会审议合并](https://techcrunch.com/2026/10/20/spacex-and-tesla-boards-form-special-committees-to-review-merger/) ⭐️ 7.0/10

SpaceX 与特斯拉董事会各自成立了由独立董事组成的特别委员会，审议两家公司可能进行的合并。马斯克表示，委员会是应股东要求设立的，他因存在利益冲突不会参与相关讨论；双方目前尚未就交易条款达成一致，且交易最终需获得特斯拉全体股东中 50% 的赞成票。

telegram · zaihuapd · 10月21日 02:06

**「背景」** 马斯克同时掌管这两家公司，因此这类存在利益冲突的交易通常先由独立董事组成的特别委员会评估，他本人不参与讨论；两家公司股东结构不同，SpaceX 方面表决较易，特斯拉则需全体股东中半数赞成。

**「影响」** 此类规模的合并须向美国联邦贸易委员会和司法部提交反垄断申报（HSR 申报），因此交易能否推进不仅取决于特斯拉股东投票，也取决于监管审查结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.freemalaysiatoday.com/category/business/2026/10/21/musk-says-backs-spacex-tesla-merger-as-rocket-firm-turns-profit">Musk says backs SpaceX - Tesla merger as rocket firm turns profit | FMT</a></li>
<li><a href="https://tesorb.com/spacex-tesla-merger-requirements/">What a SpaceX-Tesla Merger Would Actually Require</a></li>

</ul>
</details>

**标签**: `#Tesla`, `#SpaceX`, `#mergers and acquisitions`, `#corporate governance`, `#Elon Musk`

---