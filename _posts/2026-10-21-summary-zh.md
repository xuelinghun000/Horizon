---
layout: default
title: "Horizon Summary: 2026-10-21 (ZH)"
date: 2026-10-21
lang: zh
---

> 从 135 条内容中筛选出 4 条重要资讯。

---

**科技新闻**
1. [网传 OpenAI 新模型提升 COBOL 等冷门语言能力，迁移准确率称达 97.9%](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenAI API 提示缓存延长至 12 小时](#item-tech-news-2) ⭐️ 8.0/10

**财经新闻**
1. [工信部收紧创新汽车设计准入，22 项推荐性标准升为强制性](#item-finance-news-1) ⭐️ 7.0/10
2. [SpaceX 与特斯拉董事会分别设立特别委员会，审议潜在合并](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [网传 OpenAI 新模型提升 COBOL 等冷门语言能力，迁移准确率称达 97.9%](https://openai.com/index/low-resource-programming-languages/) ⭐️ 8.0/10

一个 Telegram 频道在 10 月 20 日发帖称，OpenAI 的新模型大幅提升了 COBOL、Fortran、Visual Basic 这类“低资源编程语言”（网上公开代码少、AI 训练时见得少的语言）的编写与迁移能力。帖子给出的数字是：在“用 20 种语言从零写一个 SQLite 数据库引擎”的测试中，GPT-6 Astra 的平均通过率从上一代 GPT-5.6 Sol 的 26.8% 升到 87.4%；更便宜的 GPT-6 Luna 为 40.3%，同时 API（按调用量付费的接口）成本下降 78%。在把老 COBOL 代码（上世纪起大量用于银行、保险等系统的语言）改写成现代语言的测试中，GPT-6.1 Sol 在低“推理强度”（让模型少花时间思考的设置）下准确率从 5.4% 升到 86.6%、成本降低 39%，高强度下准确率达 97.9%；相关评测集已在 GitHub 开源。这些模型名称和数字目前只见于这条聚合帖，尚未获得 OpenAI 官方页面的核实，应视为待确认的说法。

telegram · zaihuapd · 10月20日 14:24

**「背景」** 低资源编程语言是指公开代码和训练资料很少、AI 模型通常支持较弱的语言，COBOL 就是典型：它长期用于银行、保险等大型系统，因此把旧代码迁到现代语言一直是费时费力的工作。OpenAI 这次还开源了 MultiLangBench 评测集（一套统一题目，用来比较模型在 20 种语言上的编程能力），让外界可以复现其测试结果。

**「对老系统维护团队的实际影响」** 对仍在维护 COBOL 老系统的银行、保险和公共部门团队来说，实际影响是：原本只能靠人工重写的老代码，现在值得切出一小块做自动化迁移试点——按帖子给出的数字，低推理强度下迁移准确率从 5.4% 升到 86.6%，成本还低 39%。但有两点要留意：97.9% 的最高准确率是在高推理强度下取得的，模型“想”得越多，单次任务的费用通常也越高；而且这些数字来自 Telegram 聚合账号的转述，模型名称和价格尚未经 OpenAI 官方页面确认。动手前应先用已开源的评测集在自家代码上试跑，并对照官方定价页核算成本（第三方价格追踪站已按每百万 token——模型计费的最小文本单位——列出 GPT-6 Astra、GPT-6.1 Sol 和 GPT-6 Luna 的单价）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://the-decoder.com/openai-says-gpt-6-is-much-better-with-legacy-programming-languages-such-as-cobol-and-fortran/">OpenAI says GPT-6 is much better with legacy programming ...</a></li>
<li><a href="https://aicoder.com/news/news-20261020-openai-multilangbench-cobol-migration-low-resource-languages">OpenAI open-sources MultiLangBench and reports low-resource ...</a></li>
<li><a href="https://benchlm.ai/openai/api-pricing">OpenAI API Pricing (October 2026): Model &amp; Token Costs</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#model-release`, `#code-migration`, `#API-pricing`, `#benchmarks`

---

<a id="item-tech-news-2"></a>
### [OpenAI API 提示缓存延长至 12 小时](https://x.com/OpenAIDevs/status/2112603916076781778) ⭐️ 8.0/10

OpenAI 的开发者账号宣布，OpenAI API（让其他软件调用其模型的接口）现在支持 12 小时的提示缓存：重复使用的指令、工具说明和上下文会被暂存，隔几小时再请求也能按较便宜的缓存输入价格计费。OpenAI 还称，登录 Codex（其编程助手）和 Work 的用户可使用“永久缓存”，回到旧对话或暂停数小时后继续不会受罚，并保证命中缓存。该消息是二手摘要，没有给出具体价格、缓存容量或各模型的支持范围。

telegram · zaihuapd · 10月21日 01:21

**「背景」** 提示缓存（prompt caching）是把模型已经读过的指令、工具说明和上下文暂存起来，后续请求遇到相同内容时直接复用，省去重复处理，费用按更低的缓存输入价计算。对通过 API（外部软件调用模型的接口）运行的智能体（能连续执行多步任务的程序）来说，这次变化让相隔数小时的请求仍能复用同一套设定；Codex 和 Work 的登录用户则不受 12 小时限制，缓存永久保留并保证命中。

**「实际影响」** 对每天反复调用同一套指令和工具的智能体来说，隔几小时再发请求时，这部分内容会按更便宜的“缓存输入”价格计费，而不是重新按全价算；据一篇对比两家缓存定价的博客，OpenAI 与 Anthropic 的缓存读取都按正常输入价格的 0.1 倍计。代价是缓存只认完全一致的开头：只要改动共享指令或工具列表里的一个字，这次请求就会退回全价，所以要把长期不变的内容放在最前面。Codex 与 Work 的登录用户则被保证命中缓存，隔几小时回到旧对话继续也不再多付这笔钱。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ofox.ai/blog/prompt-caching-cost-math-anthropic-vs-openai-2026/">Anthropic vs OpenAI Prompt Caching 2026: Cost Math...</a></li>

</ul>
</details>

**标签**: `#OpenAI API`, `#prompt caching`, `#Codex`, `#API pricing`, `#developer tooling`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [工信部收紧创新汽车设计准入，22 项推荐性标准升为强制性](https://m.chinanews.com/wap/detail/chs/zw/10717890.shtml) ⭐️ 7.0/10

中国工信部 10 月 20 日表示，将把隐藏式门把手、电吸门、虚拟操纵件等创新设计纳入准入管理，并把 22 项推荐性标准升为强制性标准，可靠性测试要求不低于 3 万公里。工信部总工程师王卫明称，对未按要求申报、测试验证不充分的产品不予准入，以防范不合理创新设计进入市场。

telegram · zaihuapd · 10月20日 12:48

**「背景」** 工信部已于 10 月 10 日发布征求意见稿，拟收紧对隐藏式门把手、车内显示屏和可调节座椅等创新设计的审批与研发测试要求，此前已出台门把手安全强制性国家标准（来源：cnevpost、路透社）。10 月 20 日的发布会表态是在这一草案基础上的进一步说明。

**「影响」** 在中国销售的车型如果采用隐藏式门把手等设计，就需要在 2027 年 1 月 1 日相关强制性标准生效前完成改型或重新测试验证，否则可能无法通过准入。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cnevpost.com/2026/10/10/china-proposes-tighter-vehicle-design-rules/">China proposes tighter vehicle design rules, reiterates ...</a></li>
<li><a href="https://www.reuters.com/world/asia-pacific/china-proposes-stricter-car-design-testing-rules-including-ban-fully-hidden-door-2026-10-10/">China proposes stricter car design, testing rules, including ...</a></li>
<li><a href="https://cnevpost.com/2026/02/03/china-new-auto-safety-standard-bans-hidden-door-handles/">China&#x27;s new auto safety standard bans hidden door handles</a></li>

</ul>
</details>

**标签**: `#China auto policy`, `#MIIT regulation`, `#vehicle safety standards`, `#automotive industry`, `#consumer safety`

---

<a id="item-finance-news-2"></a>
### [SpaceX 与特斯拉董事会分别设立特别委员会，审议潜在合并](https://techcrunch.com/2026/10/20/spacex-and-tesla-boards-form-special-committees-to-review-merger/) ⭐️ 7.0/10

SpaceX 与特斯拉董事会各自成立了由独立董事组成的特别委员会，审议两家公司可能进行的合并。马斯克表示，该委员会是应股东要求设立的，他因存在利益冲突而不参与讨论；双方尚未就交易条款达成一致，而且任何交易最终都需要股东批准，其中特斯拉需要获得全体股东 50% 的赞成票。

telegram · zaihuapd · 10月21日 02:06

**「背景」** 若特别委员会最终提出合并方案，交易仍需股东批准：特斯拉需要全体股东中 50%的赞成票，而 SpaceX 的股东投票相对容易。

**「影响范围」** 特斯拉股东是直接受影响方：任何合并都需获得全体股东中 50%的赞成票，因此交易能否推进取决于股东投票结果，而 SpaceX 方面的股东投票门槛相对较低。

**标签**: `#SpaceX`, `#Tesla`, `#merger review`, `#corporate governance`, `#Elon Musk`

---