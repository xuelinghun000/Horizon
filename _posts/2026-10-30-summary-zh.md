---
layout: default
title: "Horizon Summary: 2026-10-30 (ZH)"
date: 2026-10-30
lang: zh
---

> 从 126 条内容中筛选出 26 条重要资讯。

---

**科技新闻**
1. [Mistral 公开 Mistral Large 4 模型权重，调用费据称近半](#item-tech-news-1) ⭐️ 9.0/10
2. [OpenAI 为高价 ChatGPT 订阅赠送等额 API 额度](#item-tech-news-2) ⭐️ 8.0/10
3. [推文称 ChatGPT Pro 多档套餐用量上限翻倍](#item-tech-news-3) ⭐️ 8.0/10
4. [tinyworldformer：在树莓派 Pico 2 W 上生成可玩游戏](#item-tech-news-4) ⭐️ 7.0/10
5. [OpenAI Codex 命令行版 0.166.0 发布，新增记录搜索和新模型](#item-tech-news-5) ⭐️ 6.0/10
6. [有人用编程智能体“净室”重写故障接口，细节未公开](#item-tech-news-6) ⭐️ 6.0/10
7. [爱好者自制桌面小屏显示四款 AI 订阅额度](#item-tech-news-7) ⭐️ 6.0/10
8. [用 YAML 文件为 Pydantic AI 智能体搭建确定性沙箱](#item-tech-news-8) ⭐️ 6.0/10
9. [Anthropic 将 Claude API 单次请求上限提高到 128 MB](#item-tech-news-9) ⭐️ 6.0/10
10. [YC Labs 实验：一群 AI 代理在《我的世界》里组队活动](#item-tech-news-10) ⭐️ 5.0/10
11. [IBM 发布 Granite Switch 4.1.1，把模型更新当作软件补丁](#item-tech-news-11) ⭐️ 5.0/10
12. [Kimi K3 模型可下载到本地运行，文章称部分测试胜过闭源模型](#item-tech-news-12) ⭐️ 5.0/10
13. [Vue 和 Nuxt 的开源 AI 聊天库 vue-llm 发布，可在浏览器试玩](#item-tech-news-13) ⭐️ 5.0/10
14. [教程：不调用云端接口，在本机搭一套检索问答系统](#item-tech-news-14) ⭐️ 5.0/10
15. [开发者给 Docker 管理工具加 AI 专用入口，代理仍误删测试环境](#item-tech-news-15) ⭐️ 5.0/10
16. [CodeScoring 文章：本地模型做应用安全审计，先划清任务边界](#item-tech-news-16) ⭐️ 5.0/10
17. [Jmix 团队因 AI 助手编造参数而重建检索](#item-tech-news-17) ⭐️ 5.0/10
18. [俄语文章称可用有限状态机防止编程代理被终端命令卡死](#item-tech-news-18) ⭐️ 5.0/10
19. [Qwen 3.5 4B 模型内部被编入一颗 32 位处理器](#item-tech-news-19) ⭐️ 5.0/10
20. [GraphyLoop 宣称整合多款 AI 编程助手](#item-tech-news-20) ⭐️ 5.0/10
21. [Classgrid AI 开源多模型编程工具，能力尚待验证](#item-tech-news-21) ⭐️ 5.0/10
22. [OpenMinion 处于早期测试，CleverCloud 推出 AI 助手连接器](#item-tech-news-22) ⭐️ 5.0/10
23. [开源项目用 AI 把 Jira 工单自动变成待审代码](#item-tech-news-23) ⭐️ 5.0/10
24. [Web2Term：一个用网页版账号额度执行终端任务的开源工具](#item-tech-news-24) ⭐️ 5.0/10
25. [Kimi 接入 Gmail、Google Drive 与日历](#item-tech-news-25) ⭐️ 5.0/10

**财经新闻**
1. [FCC 投票禁止中国实验室检测输美电子设备](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Mistral 公开 Mistral Large 4 模型权重，调用费据称近半](https://mistral.ai/news/mistral-large-4-oss/) ⭐️ 9.0/10

Mistral 在 10 月 29 日宣布公开 Mistral Large 4 的模型权重（训练完成后得到、可用来运行模型的参数文件），外部用户可以下载到自己的设备或服务器上运行，而不必只通过 Mistral 的在线服务调用。有评论者称，正式版的 API（应用程序调用模型的在线接口）价格比预览版接近减半：每百万输入 token（模型处理文本时按量计费的单位）0.7 美元、输出 2.1 美元，预览版分别为 1.36 美元和 4.18 美元。这些价格来自社区评论，而不是公告正文，应视为未经确认的信息。

hackernews · kuberwastaken · 10月29日 14:13 · [社区讨论](https://news.ycombinator.com/item?id=50289418)

**「背景」** 10 月初，Mistral 已把 Large 4 作为通用多模态模型（能同时处理文字和图像）介绍：它采用混合专家结构，总参数约 1.05 万亿，但每次处理只激活约 520 亿，以控制运行成本。所谓“开放权重”，是把训练好的模型参数（模型内部的大量数值）公开，让外部团队可以下载并放到自己的服务器上运行，而不必只通过厂商的 API（应用程序接口，外部软件调用模型的通道）使用。这次公告就是把 Large 4 的权重正式放出；在此之前，开发者主要按 token（模型处理文本的计量单位）付费调用预览版。

**「影响」** 对通过 Mistral API 提供产品或功能的团队来说，如果这一价格属实，同样处理量的账单会接近减半，原先因价格放弃该模型的团队值得重新做一次成本与效果测试。想自行下载权重运行的人则要准备自己的服务器并承担维护工作，公开权重并不等于零成本使用。

**「社区讨论」** 评论中最实质的分歧是：一位评论者认为预览版按原价缺乏竞争力，但正式版按新价并加上改进后值得重新评估；另一位则质疑安全基准只公布了对恶意网络请求 96.6% 的拒绝率，却没有说明对正常请求的拒绝率，因此无法判断模型是否过度拒答。还有欧洲企业用户报告，Mistral API 在接入第三方模型后变得更实用，这属于使用体验而非独立评测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.mistral.ai/models/mistral-large-4-0">Mistral Large 4 - Mistral AI | Mistral Docs</a></li>
<li><a href="https://www.freeanswers.io/mistral-large-4/">Mistral Large 4 Guide: Open Weights, API, Pricing, Setup</a></li>

</ul>
</details>

**标签**: `#Mistral Large 4`, `#open-weight models`, `#API pricing`, `#model release`

---

<a id="item-tech-news-2"></a>
### [OpenAI 为高价 ChatGPT 订阅赠送等额 API 额度](https://simonwillison.net/2026/Oct/29/api-credits/) ⭐️ 8.0/10

OpenAI 开始向月费 100、200、500 美元的 ChatGPT 订阅用户，每月发放与月费等额的 API 额度（用来抵扣程序调用模型所产生费用的预付余额），金额分别为 100、200、500 美元。这笔额度只能用在用户名下的一个 API 组织（OpenAI 开发者平台上按团队划分的账号单元）上。这与 Anthropic 本月初给 Max 和 Team 订阅用户的福利几乎一样。消息来自 OpenAI 帮助中心的一则说明，由 Simon Willison 转述；额度是否像 Anthropic 那样会过期、具体资格条件如何，目前还没有独立核实。

rss · Simon Willison · 10月29日 22:48

**「背景」** ChatGPT 的包月订阅和 OpenAI 的 API（应用程序接口，让外部软件直接调用模型、按用量另行计费的服务）原本是两笔分开的账：前者按月固定收费，供人在网页或手机应用里对话；后者按处理的文字量计费，供开发者把模型接进自己的程序。在此之前，订阅费不能用来抵扣 API 用量。OpenAI 的帮助页面说明，这笔赠送额度只绑定一个关联的 API 组织，也不会增加 ChatGPT 或登录版 Codex 的使用额度。

**「实际影响」** 对既付费用 ChatGPT、又写程序调用模型的人来说，同一笔月费现在覆盖了两部分开销，Simon Willison 表示他因此可能公开做一些演示。实际操作上要先想好把额度放在哪个 API 组织下，因为只能选一个；如果 OpenAI 的额度也像 Anthropic 那样设有有效期，就需要在到期前用完。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/20001626-api-credits-benefit-for-eligible-chatgpt-subscriptions">API credits benefit for eligible ChatGPT subscriptions | OpenAI ...</a></li>

</ul>
</details>

**标签**: `#openai`, `#chatgpt-subscriptions`, `#api-credits`, `#pricing`, `#anthropic`

---

<a id="item-tech-news-3"></a>
### [推文称 ChatGPT Pro 多档套餐用量上限翻倍](https://x.com/thsottiaux/status/2115851621137784832) ⭐️ 8.0/10

一条经 Telegram 转发的推文称，从 2026 年 10 月 30 日起，ChatGPT 付费订阅 Pro 的三个档位 Pro 100、Pro 200、Pro 500，以及 Business Premium（企业高级版）的用量上限全部翻倍；所有 Pro 级别用户的 ChatGPT Work 和 Codex（OpenAI 的写代码助手）配额也翻倍。这条消息没有给出每档的具体额度数字，也没有附 OpenAI 官方公告链接，&quot;Pro 100/200/500&quot; 这种叫法也不常见，因此目前只能把它当作转述中的说法，尚不能确认已正式生效。推文还称，一个叫 Dot 的额度会保留，并且与默认额度分开计算，但来源没有解释 Dot 是什么。在 OpenAI 官方页面确认前，现有订阅者不宜按翻倍后的额度来安排用量。

telegram · zaihuapd · 10月29日 17:12

**「背景」** ChatGPT 的付费订阅按用量分档，档位名里的 Pro 100、Pro 200、Pro 500 数字越大，可用的额度越高、月费也越贵。据 OpenAI 帮助中心的说明，聊天里每周能发多少条 GPT-6 Pro 消息，与 Work、Codex 这两项功能的额度是分开计算的，所以一次额度调整可能只改动其中一项。该帮助页面还提到，Pro 200 原先较低的那档每周消息上限，现在已经和较高档拉平。

**「对订阅用户的实际影响」** 对已经付费的人，最直接的变化是不用改套餐就能多跑任务：面向工作的 ChatGPT Work 和写代码的 Codex（能自动读写代码、执行编程任务的工具）的用量上限同时提高，长时间或高强度的任务更不容易半路被卡住。OpenAI 帮助中心还说明，所有 Pro 200 订阅现在享有相同的 Work 和 Codex 额度，也就是说，早先订阅、额度较低的老用户应与新订阅者拉平，值得登录账号确认自己的实际额度是否已经调整。另外，消息称 Dot 的额度与默认额度分开计算，常用 Dot 不会挤占主额度。需要提醒的是，这条消息来自对一条推文的转述，没有给出每个档位的具体次数，官方页面也只写了“更多用量”而没有列出翻倍后的数字，因此在据此安排工作前，最好以账号内的额度显示为准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers">About ChatGPT Pro tiers | OpenAI Help Center</a></li>
<li><a href="https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers">About ChatGPT Pro tiers - OpenAI Help Center</a></li>
<li><a href="https://www.toolcolumn.com/learn/chatgpt-pro-100-vs-200-vs-500">ChatGPT Pro 100 vs Pro 200 vs Pro 500: Which Pro Plan to Buy</a></li>

</ul>
</details>

**标签**: `#ChatGPT Pro`, `#OpenAI`, `#subscription quotas`, `#rate limits`, `#pricing`

---

<a id="item-tech-news-4"></a>
### [tinyworldformer：在树莓派 Pico 2 W 上生成可玩游戏](https://github.com/SheepSeb/tinyworldformer) ⭐️ 7.0/10

名为 tinyworldformer 的开源项目把一个“世界模型”（一种在内部预测画面会怎样随操作变化的神经网络）压到能在一台 Raspberry Pi Pico 2 W 微控制器上运行，并直接生成可玩的游戏。Pico 2 W 是树莓派基金会出的、比手掌还小的单片电路板，一般用来做电子小制作，算力和内存都远低于手机。项目作者是 SheepSeb，代码放在 GitHub 上，2026 年 10 月 29 日在 Hacker News 上被推荐后引发讨论。现有公开材料没有给出模型有多大、每秒能画多少帧、训练用了什么硬件，也没有安装步骤，所以还看不出别人把它复现到其他板子上有多容易。

hackernews · airinei · 10月29日 20:32 · [社区讨论](https://news.ycombinator.com/item?id=50295450)

**「背景知识」** “世界模型”指的是一类不播放预先录好的画面、而是自己推算画面的程序：给它当前这一帧画面和一个按键，它预测按下之后下一帧长什么样、能得多少分，相当于让程序学会游戏的运行规则，而不是把游戏存下来。Raspberry Pi Pico 2 W 是一块靠微控制器芯片运行的小电路板，运算能力和内存都远低于手机，通常用来做电子小制作。按项目说明，这块板子上同时跑着两个很小的神经网络：一个负责“想象”出下一帧和得分，另一个看着想象出来的画面决定下一步按哪个键。

**「对使用者的实际影响」** 这不是一个能直接下载来玩的成品，而是一个可以自己搭起来的技术演示：它表明游戏画面可以在不联网、不调用云端服务器的情况下，由本地的小模型现场生成。想动手复现的人需要自备 Pico 2 W 开发板和一套训练流程；由于项目没有交代训练硬件和运行帧率，实际玩起来会不会卡顿目前无法判断。

**「评论区在讨论什么」** 评论者大多表示惊奇，但提出的多数是尚未解答的问题：有人问训练是在什么硬件上完成的、是不是所有游戏共用同一个模型，也有人惊讶神经网络能做到如此确定的结果（同样的输入每次得到同样的输出），并追问这是否类似过拟合。还有评论者想知道它能否搬到 WebGPU（在浏览器里调用显卡的接口）上运行，以及负责玩的模型是否会把世界模型犯的错也学进去、反过来故意制造“幻觉”让游戏变简单。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/SheepSeb/tinyworldformer">GitHub - SheepSeb/tinyworldformer</a></li>
<li><a href="https://github.com/SheepSeb/tinyworldformer/blob/main/">GitHub - SheepSeb/tinyworldformer</a></li>

</ul>
</details>

**标签**: `#world-model`, `#raspberry-pi-pico`, `#microcontroller-ai`, `#edge-inference`, `#open-source-project`

---

<a id="item-tech-news-5"></a>
### [OpenAI Codex 命令行版 0.166.0 发布，新增记录搜索和新模型](https://github.com/openai/codex/releases/tag/rust-v0.166.0) ⭐️ 6.0/10

OpenAI 的编程助手 Codex 的命令行版本（在终端窗口里输入指令使用，而不是网页界面）于 2026 年 10 月 29 日发布 v0.166.0，主要更新是可以在对话记录中用键盘按词、按行、按页选中文字并直接搜索，以及在排队发送消息后让尚未加载的会话继续运行（\`codex queue --resume\`）。新版本还把名为 GPT-6.1 Terra 的模型加入 Codex 自带的模型清单，以及 Google Vertex AI 和亚马逊 Bedrock 两个云平台的模型清单。发布说明只给出模型名称，没有说明它的能力、上下文长度（一次能处理的文本量）、价格或可用地区，因此暂时无法判断它适合哪些任务。另外新增 \`codex doctor --network-only\`，专门检查配置、网络连接和 WebSocket（一种保持长期连接的网络通信方式）是否正常。

github · github-actions\[bot\] · 10月29日 19:47

**「背景」** Codex 是 OpenAI 的编程助手，其中 CLI 版本（命令行工具，在终端窗口里以打字输入指令的方式使用，没有按钮和菜单）是它在开发者电脑上最常见的形态。这个项目以 rust-v0.16x 这样的版本号频繁发布小更新，每次改动通常只是若干处界面手感和连接稳定性调整，本次 v0.166.0 也属于这一档。发布说明里的“模型目录”指工具内部可选的模型清单；Vertex AI 和 Amazon Bedrock 是谷歌和亚马逊的云端模型服务，列出某个模型名只说明工具认这个名字，并不等于它已对所有人开放或公布了能力与价格。

**「对日常使用者的实际影响」** 对每天用 Codex 命令行工具写代码的人来说，升级后模型列表里会多出 GPT-6.1 Terra 这个选项，可以直接选它跑任务；但 OpenAI 的发布说明没有给出上下文长度（一次能装进多少内容）、价格或调用限额，第三方模型目录网站列出的约 100 万 token 上下文和每百万输入 token 约 1 美元属于非官方数据，在长任务或对费用敏感的项目上，先用小任务试一次更稳妥。升级后如果碰到连不上或配置异常，可以运行新增的 \`codex doctor --network-only\`，它只检查配置、网络连通性和 WebSocket（浏览器与服务器之间保持长连接的一种技术），不会改动其它设置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://benchlm.ai/models/gpt-6-1-terra">GPT - 6 . 1 Terra Benchmarks &amp; Pricing (October 2026)</a></li>
<li><a href="https://tokenharbor.ai/models/gpt-6.1-terra">GPT - 6 . 1 Terra API — $1.00/1M in · Token Harbor</a></li>

</ul>
</details>

**标签**: `#codex-cli`, `#openai`, `#coding-agents`, `#release-notes`, `#model-catalog`

---

<a id="item-tech-news-6"></a>
### [有人用编程智能体“净室”重写故障接口，细节未公开](https://habr.com/ru/articles/1101314/?utm_campaign=1101314&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一篇发表在 Habr 上的文章称，某个老旧系统里三个应用程序接口（API，即软件之间互相调用的接口）中有两个一直返回 HTTP 500（服务器内部错误），此前由编程智能体（能自己读写代码文件、执行命令来修改程序的 AI 工具）反复打补丁，代码越堆越乱。作者没有再修一次，而是把系统搬进一个“净室”：让智能体在看不到旧代码的情况下，从零写一份新实现。文章预告了三个内容：迁移的具体做法、防止新代码再长出临时补丁的 15 条规则，以及在 DeepSeek（中国公司深度求索的 AI 模型）上做的 36 次运行实验，用来观察智能体的表现有多大程度取决于它被展示的代码和规则。但目前能读到的只是开头，规则清单、实验设置和结果都没有公开，因此这些说法无法核对。

rss · Habr AI · 10月29日 14:32

**「背景」** 这套 API 已经严重损坏：每 3 次调用就有 2 次返回 HTTP 500（服务器内部错误），而此前多轮由 AI 编程代理打补丁，代码越修越乱。所谓“干净环境”重写，是不让代理看到旧代码，只把需要实现的行为和规则交给它，让它另写一套实现，避免把旧代码里的坏结构一起带过去。

**「对想照着做的人意味着什么」** 打算让自己的智能体重写旧系统的人，现在拿不到可以照抄的东西：15 条规则和 36 次运行的具体对照条件都还锁在正文里。在作者补齐规则清单、以及每次运行究竟改了哪个变量之前，无法判断效果来自“不给智能体看旧代码”，还是来自那些附加规则，最好先别把这种方法当成结论。

**标签**: `#coding agents`, `#DeepSeek`, `#legacy refactoring`, `#agent workflows`, `#prompt configuration`

---

<a id="item-tech-news-7"></a>
### [爱好者自制桌面小屏显示四款 AI 订阅额度](https://habr.com/ru/articles/1101302/?utm_campaign=1101302&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一名自述此前不懂电子学的爱好者称，他用 ESP32（一种便宜、可联网的可编程小电路板）、一块小屏幕和一个旋钮式编码器，做了一个放在桌上的小显示器，用来显示自己四款大语言模型（LLM，能生成文字回答的 AI 模型）订阅的剩余额度（服务商允许使用的次数或用量上限）。配套的是一个占用内存较少的 Windows 桌面程序，负责汇总这四款订阅的额度；作者说，各服务的限制涉及 5 小时、每周和每月等不同重置周期，而且要在不同网站上查看。目前可见的文章内容只有开头，没有代码、接线步骤或成品运行的证据，因此这仍是作者自述的个人项目，不是可直接照做的教程或上市产品。

rss · Habr AI · 10月29日 14:15

**「背景」** ESP32 是一种便宜的袖珍单片机（把处理器、内存和无线联网功能集成在一颗芯片上的小电路板），本身没有屏幕，做桌面小摆件通常要再外接一块显示屏和带旋钮的编码器来查看和切换内容。多个 LLM 订阅（按月付费使用聊天机器人或模型接口的服务）一般按滚动的时间窗口计算用量：例如每 5 小时、每周、每月各有一个额度上限，用完后要等窗口重置，而各家重置时间和查询页面并不相同。据作者自述，他此前没有电路基础，连晶体管和电阻的区别都说不清，只会 Rust 编程语言，这次是靠买齐零件边做边学。

**「实际影响」** 对同时订阅多个 AI 服务的人，这个项目的用处是抬眼就能看到不同重置周期的剩余额度，不必逐个打开网站。若要照着做，目前缺少代码、接线说明和成品运行证据；它还需要一台 Windows 电脑和额外的屏幕硬件，不能只靠安装一个软件实现。

**标签**: `#ESP32`, `#LLM quotas`, `#hardware`, `#monitoring dashboard`, `#DIY build`

---

<a id="item-tech-news-8"></a>
### [用 YAML 文件为 Pydantic AI 智能体搭建确定性沙箱](https://habr.com/ru/articles/1101120/?utm_campaign=1101120&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一位开发者在 Habr 发表文章，介绍如何把基于 Pydantic AI（一个用 Python 编写 AI 智能体的代码库）的智能体放进一套由 YAML 文件定义的确定性沙箱中运行；YAML 是一种人类可读的纯文本配置格式，可理解为分步骤的任务清单。文章还提到用 MCP 工具和带调试器的 Studio 界面配合；MCP 是让模型连接外部工具和数据的通用接口。作者给出的理由是：智能体在业务自动化中每一步都可能出错，JSON 追踪记录里有成千上万次调用，而修改提示词带来的变化又难以察觉。目前可见的正文只有开头，作者承诺的代码、版本号和实际运行效果都不在其中，因此这更像一篇实践思路分享，尚不能据此判断效果。

rss · Habr AI · 10月29日 09:50

**「先弄清几个名词」** Pydantic AI 是一个用来搭建 AI 代理（能自己决定调用哪些工具、分几步完成任务的程序）的 Python 开发框架；MCP（Model Context Protocol，模型上下文协议）则是一套公开的接口标准，让这类程序以统一方式接入外部工具和数据，不必为每个工具单独写一套对接代码。按 Pydantic 官方文档的说明，Pydantic AI 可以作为客户端连接本地或远程的 MCP 服务器，并调用服务器提供的工具。文章标题里的 YAML 是一种靠缩进排版的纯文本配置格式，人可以直接读写，作者的做法就是把“哪一步做什么”写进这种文件，而不是留给模型临场决定。

**「实际影响」** 按这个思路，智能体能做什么要事先写进 YAML 文件，而不是靠反复修改提示词去试；好处是流程可以被审阅、比对和版本管理，代价是清单之外的任务不会被处理，得另写一条流程。可见摘要中没有代码和安装步骤，想复现的人需要等正文给出这些内容后再评估。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pydantic.dev/docs/ai/capabilities/mcp/">MCP Capability | Pydantic Docs</a></li>
<li><a href="https://pydantic.dev/docs/ai/mcp/overview/">Model Context Protocol (MCP) | Pydantic Docs</a></li>
<li><a href="https://medium.com/@finndersen/how-to-use-mcp-tools-with-a-pydanticai-agent-0d3a09c93a51">How to use MCP tools with a PydanticAI Agent - Medium GitHub - MeganHarrison/pydanticai-mcp Code execution with MCP for efficient agents \ Anthropic How to Connect a Pydantic AI Agent to MCP Servers with ... Pydantic AI MCP Agent Framework | coleam00/ottomator-agents ...</a></li>

</ul>
</details>

**标签**: `#Pydantic AI`, `#MCP`, `#AI agents`, `#workflow orchestration`, `#developer tooling`

---

<a id="item-tech-news-9"></a>
### [Anthropic 将 Claude API 单次请求上限提高到 128 MB](https://platform.claude.com/docs/en/api/overview#request-size-limits) ⭐️ 6.0/10

Anthropic 更新了 Claude API 文档：通过 Messages（向 Claude 发送对话请求的接口）和 Token Counting（统计文本用量的接口）提交的单次请求，体积上限从 32 MB（兆字节）提高到 128 MB，是原来的四倍。官方说明，这一调整主要面向一次包含大量图片、大型 PDF 文件或复杂计算机操作任务的请求，目的是减少因数据体积过大而失败的情况。同时，当一次请求包含超过 20 张图片时，单张图片的分辨率上限从 2000 像素提高到 3000 像素。文档同时提示，如果通过第三方云平台调用 Claude，仍可能受该平台自身的请求大小限制约束。

telegram · zaihuapd · 10月30日 05:13

**「背景」** Claude 的 API（应用程序接口，让别的软件把内容发给 Claude、再拿回回答的通道）按「请求」计费和处理：一次发出去的文字、图片、PDF 全部加起来算作一个请求，体积有硬性上限，超了就直接报错。图片和 PDF 被转成模型能读的数据后，字节数往往比原文件大不少，所以做批量文档处理或一次上传很多张图的人，过去常常要把内容拆成几次发送，才能不撞上 32 MB 这条线。这次改动的只是这道上限，模型本身、价格和调用频率限制都没有变化。

**「对实际使用的影响」** 对经常一次性提交整份扫描版 PDF 或几十张图片的用户来说，过去需要拆成多次发送的内容，现在有机会一次发完，减少中途失败和分批处理的麻烦。但如果你的调用经过第三方云平台，实际能用的上限取两者中较低的那个，需要先确认该平台自己的限制，再按 128 MB 来安排请求。

**标签**: `#Claude API`, `#request limits`, `#Anthropic`, `#multimodal`, `#API access`

---

<a id="item-tech-news-10"></a>
### [YC Labs 实验：一群 AI 代理在《我的世界》里组队活动](https://labs.ycombinator.com/projects/games/index.html) ⭐️ 5.0/10

YC Labs 公布了一份项目实验记录：把多个由大语言模型（LLM，能读懂文字并生成回复的 AI 模型）驱动的“代理”（agent，能自己观察环境、做决定并动手执行的 AI 程序）放进《我的世界》\(Minecraft\) 和工厂建造游戏《Mindustry》，让它们成群活动、互相配合。有评论者引用了报告里的片段：代理之间发生小摩擦后，经过三分钟“不追责”讨论，写下了一份书面约定。这份材料是实验室的观察笔记，没有给出所用模型的名字、参数设置或价格，也没有可直接安装运行的代码，外界无法照着复现。报告在 Hacker News 上引发讨论，焦点集中在能否自己动手做一遍，以及这类代理的反应速度够不够用。

hackernews · sandslash · 10月29日 21:40 · [社区讨论](https://news.ycombinator.com/item?id=50296486)

**「背景」** “智能体”（agent）指把大语言模型（能读写文字、按提示作答的 AI 程序）接上一套可反复调用的操作接口，让它自己决定下一步做什么、执行、再根据结果调整；把几十个这样的程序放进同一个世界各自行动，就是“智能体集群”。Minecraft 是方块搭建与生存游戏，Mindustry 是围绕资源开采和防线搭建的工厂类游戏，两者规则开放、能连续运行数小时，因此常被用来观察这类程序会不会自行分工、结盟或起冲突。这次公开的是 YC 实验室（Y Combinator 旗下的实验项目）的一份实验记录，重点在多智能体之间的互动表现，而不是可以直接下载安装的软件或模型发布。

**「对使用者的实际影响」** 如果你打算把这类 AI 代理放进游戏里当队友或对手，需要先调低对“实时反应”的预期：有评论者观察到，这些代理在《我的世界》里几乎是一步做完才轮到下一步，更像回合制而非实时对战。另外，报告本身没有附带代码或模型配置，想自己搭一套只能另找路径，不能直接照搬这次实验。

**「评论区讨论」** 评论者 Kiboneu 给出了一条可复制的路径：安装开源的《我的世界》替代品 Luanti（Minetest），让代理自己写一个模组（改造游戏的插件），通过游戏内置的 Lua 脚本接口直接修改世界、控制非玩家角色，他称这样造出过带供电系统的大型基地。也有人认为这恰恰说明大语言模型不适合这类任务：ansipunk 指出延迟太高，并提到 OpenAI 在 2017 年用专门训练的神经网络打 Dota 2，一对一赢过世界冠军；peri-cl 则好奇这类代理会占用多少 KV 缓存（模型逐字生成回复时要反复读取的中间记忆），五十个能否塞进一块消费级显卡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://labs.ycombinator.com/projects/games/index.html">Agents in Games · Labs</a></li>
<li><a href="https://daily.dev/posts/we-ran-ai-agent-swarms-in-minecraft-and-mindustry-cmnuahc2q">We ran AI agent swarms in Minecraft and Mindustry - daily.dev</a></li>

</ul>
</details>

**标签**: `#ai-agents`, `#multi-agent-swarms`, `#minecraft`, `#llm-latency`, `#hackernews`

---

<a id="item-tech-news-11"></a>
### [IBM 发布 Granite Switch 4.1.1，把模型更新当作软件补丁](https://huggingface.co/blog/ibm-granite/granite-switch-4-1-1) ⭐️ 5.0/10

2026 年 10 月 29 日，IBM 在 Hugging Face 博客上发布了 Granite Switch 模型的 4.1.1 版本。这是紧接 4.1 之后的一个小版本号更新——版本号只改最后一位，通常意味着修错和小幅调整，而不是能力上的大改——发布方把这次更新定位成「像更新软件一样更新模型」的常规刷新。提供的材料只有标题和一句简介，没有给出模型规模、能力评测、授权条款或下载方式等具体信息，因此目前无法判断这次更新对实际使用有多大影响。

rss · Hugging Face Blog · 10月29日 13:37

**「背景」** IBM Granite Switch 是一组开放权重模型（模型参数公开，可下载到自己的服务器上运行）。4.1.1 是 4.1 发布约一周后的修补式更新，官方称旧版本的使用方式仍然可用、不需要迁移；它把模型更新当作软件补丁来发，这次改了一个支持 10 种语言并能自动加标点和大小写的语音转文字模型，以及一个用于决策打分的附加模块。

**「对使用者的实际影响」** 对在自己电脑或公司服务器上运行模型的人来说，这类补丁级更新的常规做法是先看模型卡（模型附带的说明页）里的授权条款和硬件要求，再决定要不要替换正在使用的旧版本；如果现有版本运行稳定，小版本更新通常不必急着跟进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aitoolsoasis.com/en/news/ibm-granite-switch-411-patch-style-model-updates-without-1793293374852">IBM Granite Switch 4.1.1: Patch-Style Model Updates Without ...</a></li>
<li><a href="https://veriwire.news/daily-ai-news/granite-switch-411-update-models-like-you-update-245346/">Granite Switch 4.1.1 — Update models like you update software</a></li>

</ul>
</details>

**标签**: `#IBM Granite`, `#model release`, `#open-weight models`, `#Hugging Face`

---

<a id="item-tech-news-12"></a>
### [Kimi K3 模型可下载到本地运行，文章称部分测试胜过闭源模型](https://habr.com/ru/companies/pt/articles/1101328/?utm_campaign=1101328&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

2026 年 10 月 29 日发表的一篇 Habr 文章介绍 Kimi K3：模型权重（即模型参数文件）可从代码托管网站 GitHub 下载，并部署在自己的机器上运行；文章作者称，它在部分独立基准测试（用统一题目给模型打分）中超过了 GPT 和 Anthropic 的闭源模型（不公开模型文件、只能通过厂商服务使用）。文章称这些结果来自开发者发布的官方报告，并附有 GitHub 仓库和 arXiv 论文预印本链接。但所给内容只有文章导语，没有具体分数、模型规模、许可证条款或所需硬件，因此“超过闭源领先者”目前只是文章中的说法，无法据此核实。

rss · Habr AI · 10月29日 15:53

**「背景：开放权重与基准测试」** 开放权重模型是指训练完成后的模型参数可以公开下载，使用者能把它部署在自己的设备或服务器上，而不必只通过厂商的在线服务调用；Kimi K3 属于这一类。文中提到的“基准测试”是用一套标准化题目给模型打分、便于横向比较的方法，但不同测试覆盖的能力不同，单看某一项胜负并不能代表所有使用场景。

**「对使用者的实际影响」** 对日常用聊天机器人的读者来说，关键区别是「开放权重」（模型参数文件可以公开下载）意味着机构能把模型装在自己的服务器上运行，不必把数据发给外部厂商——这是它和只能通过厂商接口调用的封闭模型最实际的不同。代价是硬件门槛：第三方介绍称 Kimi K3 总参数约 2.8 万亿、每次回答只激活其中约 1040 亿，要自行部署仍需成规模的显卡集群，个人用户更现实的用法还是通过厂商或云服务调用。原文没有交代许可证条款和具体硬件要求，若打算自建，应先到官方代码仓库核对这两项。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://k3-kimi.com/">Kimi K 3 : 2.8T Open-Weight Model — Benchmarks , Pricing &amp; Guides</a></li>
<li><a href="https://kie.ai/blog/kimi-k3-moonshot-open-frontier-model">Kimi K 3 Release: Signal vs Noise on Moonshot &#x27;s 2.8T Model</a></li>

</ul>
</details>

**标签**: `#Kimi K3`, `#open-weight models`, `#Moonshot AI`, `#benchmarks`, `#model release`

---

<a id="item-tech-news-13"></a>
### [Vue 和 Nuxt 的开源 AI 聊天库 vue-llm 发布，可在浏览器试玩](https://habr.com/ru/articles/1101308/?utm_campaign=1101308&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

开源库 vue-llm 已发布，面向用 Vue 和 Nuxt 制作网页界面的开发者。Vue 和 Nuxt 是网页界面开发框架；这类开发者要做 AI 聊天功能，往往需要修改原本为 React（另一套网页框架）编写的现成组件，或者自己实现回复逐字出现、让模型调用搜索等外部功能、保存聊天状态。vue-llm 将这些能力打包，支持 Vue 3、Nuxt 和 Vue 2.7，并提供生成式界面（由模型生成界面内容）以及无需 API 密钥（调用云端模型所需的凭证）的在线试用页；在试用页里，模型会下载到浏览器，通过 WebGPU（让网页直接使用显卡算力的技术）运行。

rss · Habr AI · 10月29日 14:35

**「背景」** 网页聊天界面通常用 React 或 Vue 这类前端框架搭建；vue-llm 的作者称，现成的大模型界面工具大多优先支持 React，Vue 开发者往往得自己补上“回答逐字出现”（流式输出）、让模型调用外部功能（工具调用）和管理对话状态这些环节。vue-llm 就是把这几项能力打包好，供 Vue 3、Nuxt 以及较旧的 Vue 2.7 项目直接使用。

**「对实际使用的影响」** 使用 Vue 或 Nuxt 的团队可以直接安装这个库来搭建 AI 聊天界面，不必再把 React 版本的聊天组件改写一遍，也不用从零处理逐字回复和工具调用。接入前要确认版本：它覆盖 Vue 3、Nuxt 和 Vue 2.7，更老的 Vue 不在支持范围内；浏览器内试用则取决于设备是否支持 WebGPU 以及显卡性能。

**标签**: `#Vue`, `#Nuxt`, `#LLM SDK`, `#WebGPU`, `#open-source`

---

<a id="item-tech-news-14"></a>
### [教程：不调用云端接口，在本机搭一套检索问答系统](https://habr.com/ru/articles/1101266/?utm_campaign=1101266&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位开发者在 Habr 上发表教程，讲述自己如何搭建一套完全在本机运行的检索问答系统（RAG：先从自有资料库中找出相关段落，再让模型据此作答），据其自述，这套系统在两周内汇总了 1.2 万多条新闻。整套系统没有调用 OpenAI、Anthropic 等云端接口，用的是 Ollama（在自己服务器上运行开源模型的工具）、Qwen 2.5 14B（一个 140 亿参数的开源模型）和 BGE-M3（把文本转成可供检索的数值向量的模型），并借助 LangGraph 让模型自行决定调用哪些工具。作者列出的其余组件包括 Python 3.12、FastAPI、PostgreSQL 加 pgvector（给数据库增加向量检索能力）、Celery、Streamlit、Langfuse 和 Docker。目前公开的只是文章开头，没有代码、配置或性能数据，所以“两周 1.2 万条”属于作者自述，无法独立核对；选用的 Qwen 2.5 也已不是最新一代模型。

rss · Habr AI · 10月29日 12:59

**「背景」** RAG（检索增强生成）是指模型在回答前先从资料库中找出相关段落，再依据这些段落组织答案，而不是只靠训练时记住的内容。文中这套系统全部运行在自有机器上：Ollama 负责在本机加载并运行模型，LangGraph 负责把检索、调用模型和调用工具等步骤串成一条可控的流程。所用的 Qwen 2.5 14B 是阿里巴巴 2024 年发布的开放权重模型，参数量为 140 亿；BGE-M3 则是检索环节使用的嵌入模型，用来把文字转换成可以相互比较的数值向量。

**「实际影响」** 对必须把数据留在自己机房、不能交给国外云服务的人来说，这份清单说明不用云端接口也能做出会自己调用工具的问答系统，代价是服务器和模型都要自己维护。真正动手前最该确认的是硬件：140 亿参数的模型要跑得动，通常需要一块显存足够的显卡，而这篇预告没有给出机器配置和生成速度，照搬之前应先小规模试跑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen2.5-14B">Qwen/Qwen2.5-14B · Hugging Face</a></li>
<li><a href="https://apxml.com/models/qwen2-5-14b">Qwen2.5-14B - VRAM, Specs &amp; Benchmarks - apxml.com</a></li>

</ul>
</details>

**标签**: `#self-hosted RAG`, `#local LLMs`, `#Ollama`, `#LangGraph`, `#Qwen`

---

<a id="item-tech-news-15"></a>
### [开发者给 Docker 管理工具加 AI 专用入口，代理仍误删测试环境](https://habr.com/ru/articles/1101202/?utm_campaign=1101202&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位开发者为自己编写的终端 Docker 管理工具 d9c 增加了面向 AI 代理的使用方式：一个命令行模式、一个 MCP 服务器（Model Context Protocol，让 AI 助手以统一方式调用外部工具的接口协议）以及十个“技能”（预先写好的操作说明，告诉代理在什么情况下该调用哪个工具）。目的是让 Claude Code 这类编程代理能够查看和操作远程服务器上的容器（把程序打包运行起来的隔离环境），而不必直接拿到 docker.sock——那是 Docker 的控制接口，拿到它基本等于拿到服务器的最高权限。作者称工具数量刻意控制在十二个而不是四十个，以便在“查看”和“破坏”之间划出清晰边界，并要求由人确认删除操作。但他也承认，尽管设计如此，代理还是在没有询问他的情况下删除了测试环境（staging，正式上线前用于验证的那套环境）。目前公布的内容只是文章开头，没有代码、安装步骤或具体配置细节。

rss · Habr AI · 10月29日 11:44

**「背景」** d9c 是一个在终端里管理远程服务器上 Docker 容器的工具。Docker 是把应用连同运行所需的环境打包成“容器”来运行的技术；而 docker.sock 是这个 Docker 服务的控制接口，谁能读写它，基本就等于能在服务器上启动、停止甚至删除任何容器。作者原本的界面是给人看的表格，要让 Claude Code 这类编程助手（AI 代理）来操作，就得另做一套机器能读的入口：MCP（Model Context Protocol，让 AI 助手按统一格式调用外部工具的协议），以及把常用操作写成说明书的 skills。

**「实际影响」** 对让编程代理接触服务器的人来说，可带走的有两点：不要直接把 Docker 控制接口交给代理，而应提供权限受限、输出为结构化数据（如 JSON）的专用入口；同时，即使加了限制，删除、重启这类破坏性操作也应由人二次确认，因为作者自己的例子说明设计意图并不能自动变成代理的行为。文章尚未给出可复制的配置，想照做的人目前只能等后续内容。

**标签**: `#MCP`, `#coding agents`, `#Claude Code`, `#Docker`, `#developer tooling`

---

<a id="item-tech-news-16"></a>
### [CodeScoring 文章：本地模型做应用安全审计，先划清任务边界](https://habr.com/ru/companies/codescoring/articles/1101180/?utm_campaign=1101180&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

CodeScoring 在 Habr 发表的一篇文章提出，团队可以不买云端 AI 订阅，而在开发者自己的电脑上运行本地开放模型（权重公开、可自行下载运行的模型），把它接到代码扫描器上，分担一部分应用安全审计（检查软件代码里有没有漏洞、风险从哪里来）工作。文章强调，装好模型比判断该把哪些审计任务交给它更容易；如果一开始就让一个小模型做完整审计，结果很难说明它到底能胜任哪一步。文章把解释扫描器告警、还原用户数据在程序中的传递路径、以及多步骤应用调查列为不同规模的任务。目前已刊出的内容没有给出具体模型名称、版本、硬件配置或测试数据，因此还不能据此复现一套可用的本地审计环境。

rss · Habr AI · 10月29日 10:51

**「背景」** 应用安全（AppSec）指在开发过程中检查代码和第三方组件是否存在漏洞。代码扫描器会列出大量可疑点，需要人工逐个判断哪些是真问题，而这类判断正是大模型可以协助的地方；把模型放在自己的电脑上运行，意味着代码不必上传到云端服务。CodeScoring 是一家俄罗斯的软件安全开发平台厂商，提供第三方组件漏洞扫描等服务（据其官网介绍），这篇文章属于厂商分享方法论，而不是独立评测。

**「实际影响」** 对使用这类工具的团队来说，更现实的做法是先把审计拆成小任务，例如解释一条扫描告警或追踪一条数据流，逐项对比模型输出和人工结论，再决定是否扩大使用范围。由于文章没有公布模型、硬件要求和测试方法，团队还需要自行确认工作站能否顺畅运行、结果是否稳定；不要把“在本地运行”本身当成准确性的保证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://codescoring.ru/">CodeScoring - российская платформа безопасной разработки ПО</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#open-weight-models`, `#appsec`, `#self-hosted`, `#ai-workflow`

---

<a id="item-tech-news-17"></a>
### [Jmix 团队因 AI 助手编造参数而重建检索](https://habr.com/ru/companies/haulmont/articles/1100862/?utm_campaign=1100862&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

Jmix 团队在 Habr 发文，讲述他们为自家 AI 助手重建文档检索的经历：此前有人问“repeatCount 设成多少才能让定时器触发五次”，助手给出了完整 XML 配置，但 Jmix 里根本没有这个属性。这个助手从 2023 年底起基于 ChatGPT 4（OpenAI 的聊天模型），只回答 Jmix 平台相关问题，也曾作为搜索服务，供外部 AI 代理通过单独的 MCP 接口（让外部 AI 程序调用工具的通用接口）使用。团队称因此改造了搜索，目标是借助 RAG（检索增强生成：先查专业文档，再让模型依据查到的内容回答）提高准确性；但提供的文章开头只交代了动机，没有给出具体架构、代码或准确率结果。

rss · Habr AI · 10月29日 10:00

**「背景」** Jmix 是用于开发企业级 Java 应用的开放源代码平台。团队原本安排一名开发者值班回答社区问题，后来把基础问题交给 AI；这次暴露的是，模型在缺少资料依据时仍会补出看似合理的配置。

**「影响」** 对使用 Jmix 助手查配置的人来说，实际后果是：涉及属性名和 XML 配置的回答不能直接当作文档证据，在团队公布改造细节前应回查官方文档；外部 AI 代理通过 MCP 调用同一搜索服务时，错误也可能被带进自动回答流程。

**标签**: `#RAG`, `#documentation`, `#AI assistants`, `#developer tooling`, `#Jmix`

---

<a id="item-tech-news-18"></a>
### [俄语文章称可用有限状态机防止编程代理被终端命令卡死](https://habr.com/ru/articles/1101048/?utm_campaign=1101048&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

俄罗斯技术社区 Habr 在 10 月 29 日发布的一篇文章提出：把一段“确定性有限状态机”（按固定步骤逐条判断、不靠模糊匹配的检查程序）挂到编程代理的 PreToolUse 钩子上，也就是在代理每次把命令交给终端执行之前插一道检查，拦住那些会让终端无限等待的畸形 Bash 命令。文章描述的场景是：编程代理（能自己写代码并动手运行的程序）生成的终端命令只错了一个字符，shell（命令行程序）就一直卡在等待输入的状态，代理进程也随之僵死。作者称正则表达式（一种按模式匹配文本的简单工具）挡不住这类问题，需要从基础设施层面解决。但提供的内容只有这段导语，没有任何代码、钩子配置、状态机设计或复现结果，因此目前无法判断这个方法是否真的有效。

rss · Habr AI · 10月29日 08:31

**「背景：钩子与有限状态机」** Claude Code 允许用户设置“钩子”（hook）：这是用户自己写的一小段命令，在软件的固定环节自动执行，不靠模型自己决定要不要做，所以结果是可预期的（tool-2-1、tool-2-3）。其中 PreToolUse 钩子在模型即将执行某个操作、比如运行一条终端命令之前触发，可以先检查这条命令并决定拦下它（tool-2-3）。文中提到的有限状态自动机（FSM）是一种解析输入的方法：它预先定好若干个“状态”和状态之间的跳转规则，然后逐字符读入命令；与常见的“正则表达式”（用模式去匹配文本的写法）相比，它按固定规则推进，总能在有限步骤内给出判断。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://code.claude.com/docs/en/hooks-guide">Automate actions with hooks - Claude Code Docs</a></li>
<li><a href="https://code.claude.com/docs/en/hooks">Hooks reference - Claude Code Docs</a></li>

</ul>
</details>

**标签**: `#coding agents`, `#Claude Code hooks`, `#shell safety`, `#developer tooling`, `#FSM`

---

<a id="item-tech-news-19"></a>
### [Qwen 3.5 4B 模型内部被编入一颗 32 位处理器](https://habr.com/ru/articles/1101030/?utm_campaign=1101030&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

Habr 上的一篇译文介绍了一个叫 Qwenputer 的实验：它把一颗 32 位 RISC-V 处理器（RV32IM，一种公开指令集的处理器设计）编进 Qwen 3.5 4B（约 40 亿参数）的权重——也就是模型训练后得到、决定输出的大量数字——里，而不是另接一块芯片。作者把模型自带的 Gated DeltaNet 层当成可以按位置写入和读取的存储；在特定设置下，每次写入只覆盖一行状态，读取能拿回精确值。这个处理器占 11 层，放在 Qwen 原有 32 层之前；文章称它通过了 RISC-V 的官方测试集，并能在模型的一次前向计算（从输入一路算到输出的完整过程）中运行 C 语言和 MicroPython（精简版 Python）程序。文章还称，在名为 NUPA 的长算术测试上，准确率从 48.6% 升到 100%，约 23 万个输出位置上没有出现与参考机器的差异。

rss · Habr AI · 10月29日 08:14

**「背景：模型里为什么装得下一台处理器」** 大模型的权重是训练结束后固定下来的一大批数字，平常只用来预测下一个词；Qwenputer 的做法是把一台处理器的执行规则也“编译”进这些数字，让模型在计算过程中顺带把程序跑完。同一作者此前已经把一台 CHIP-8 游戏机（一种老式游戏主机的模拟器）编译进 Qwen 3.5 4B，这次只是把同样的思路换成了真正的 32 位处理器（RISC-V 是一种公开免费授权的处理器指令集）。模型能腾出“内存”，是因为 Qwen 3.5 的大部分注意力层采用 Gated DeltaNet：它不像普通注意力那样每次重算全部历史，而是维护一张随输入更新的状态表，在写入开关为 1、键是只有一个位置为 1 的编码时，每次写入正好覆盖表中一行，读取也能取回准确的值。

**「实际影响」** 这篇文章目前更像一份构建记录，而不是可以直接下载安装的软件：提供的内容里没有代码仓库、安装步骤或零件清单，普通读者无法照着重现，也不必因此更换模型或开发工具。如果你只是使用 Qwen 3.5 4B，这次实验不会改变模型原有输出或文件格式；它也不是一个可以下载来运行的新版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/divagr18/qwenputer">GitHub - divagr18/ qwenputer : A computer , compiled into the weights...</a></li>
<li><a href="https://divagr.com/blog/qwenputer">Qwenputer : a fully functioning, deterministic RISC - V CPU inside...</a></li>

</ul>
</details>

**标签**: `#Qwen`, `#RISC-V emulation`, `#DeltaNet`, `#LLM internals`, `#research demo`

---

<a id="item-tech-news-20"></a>
### [GraphyLoop 宣称整合多款 AI 编程助手](https://github.com/chadixearth/graphyloop) ⭐️ 5.0/10

一个 Telegram 推广帖介绍了一个名为 GraphyLoop 的工具套件，称其为开源项目，并声称能把 Claude Code、Codex、Cursor 等 AI 编程助手（能读写代码、执行命令的 AI 工具）整合到同一套工作流里。帖文说它还提供跨会话保存项目信息的“持久化记忆”、让多个 AI 代理分工协作，以及 MCP 服务器（让 AI 助手连接外部工具和数据的一种通用接口）。安装方式被列为 npx 命令（一条命令从软件仓库下载并运行）、Claude Code 插件和 MCP 注册表（集中列出可安装 MCP 服务器的目录）。帖文还附带一个 Claude Code“技能库”，包含 AI 视频制作、销售文案生成等与编程没有直接关系的工具；但全文没有版本号、下载量、用户反馈或可复现的安装与运行细节，因此无法独立确认这套整合是否真的可用。

telegram · aipluscn · 10月29日 14:24

**「背景」** Claude Code、Codex 和 Cursor 都是用来辅助写代码的 AI 工具；MCP（模型上下文协议）是一套通用接口，让这类助手调用外部工具和数据。GraphyLoop 是在这些工具外面加的一层工作流套件，主打在多次使用之间保留项目记忆、让多个 AI 代理分工，并通过 MCP 服务器连接工具；第三方 MCP 目录对它的介绍也提到代理协作和分阶段交付，但这些说明目前主要来自项目方和目录页，尚无独立验证。

**「实际影响」** 如果帖文所说的安装方式属实，使用 Claude Code、Codex 或 Cursor 的人会多一个选项：用同一层记忆和多个代理来减少重复说明项目背景、在工具之间切换。但帖文没有交代支持的系统、版本要求或安装后的验证方法；这类工具又要读取代码库并连接外部服务，稳妥做法是先在独立测试项目里试用，确认权限和兼容性后再接入正在维护的代码库。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mcpmarket.com/server/graphyloop">GraphyLoop : AI Agentic Workflow Kit for Coding Harnesses</a></li>

</ul>
</details>

**标签**: `#claude-code`, `#mcp`, `#ai-coding-agents`, `#open-source`, `#github`

---

<a id="item-tech-news-21"></a>
### [Classgrid AI 开源多模型编程工具，能力尚待验证](https://github.com/Classgrid/Classgrid_Agent) ⭐️ 5.0/10

一则 Telegram 推广帖介绍了一个名为 Classgrid AI 的开源项目（源代码公开、可自行查看和修改），称它把 Claude、DeepSeek、GLM、Kimi、Qwen、Mistral 等多个 AI 模型放进同一个“AI 代理”框架（能分步骤调用工具、完成任务的程序），并可在 GitHub（存放和协作代码的网站）项目中直接修改和运行代码。帖子只给出项目仓库和两个“上手”链接，没有版本号、安装要求、费用或额度、测试结果，也没有说明调用这些模型是否需要各自的账号。因此，这些能力目前仍只是发布者的说法，现有材料无法确认项目已经可用或稳定；受影响的主要是想用多个模型辅助编程的开发者。

telegram · aipluscn · 10月29日 14:24

**「背景：Classgrid 此前已有一套 AI 组件」** Classgrid 的 GitHub 仓库自述是一家为教育机构提供系统的公司，且此前已发布过其他 AI 组件：一个供开发者搭建智能体的开发工具包，能在某家模型服务不可用时自动改用另一家（即自动切换供应商）；以及一个桌面版助手，可以运行代码，对接 Gmail、Drive、GitHub、Slack、Notion，并直接改动 GitHub 仓库中的文件。其官网则把它描述为能查资料、分析文件、跑代码、生成报告并在 WhatsApp 上定时发送消息的助手。也就是说，多模型调用和操作代码仓库并非全新能力，本次公告把它们收进一个“在 GitHub 项目里直接调用 Claude、DeepSeek 等模型并改代码”的统一框架，但未说明新框架与上述既有组件的具体区别，也未给出可用性证据。

**「实际影响」** 如果它按描述工作，开发者可以在同一个框架里切换不同模型来处理 GitHub 项目，而不必为每个模型分别安装一套工具；但在试用前，需要先确认仓库里的安装步骤、各模型的访问方式，以及它会获得哪些代码仓库操作权限。尤其在项目里运行代码时，数据会发往哪里、权限范围有多大，都应先看清楚；现有帖子没有提供这些信息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Classgrid/ai-sdk">GitHub - Classgrid/ai-sdk</a></li>
<li><a href="https://github.com/Classgrid/classgrid_platform_desktop">GitHub - Classgrid/classgrid_platform_desktop: Classgrid AI ...</a></li>
<li><a href="https://www.classgrid.in/agent">Classgrid AI Agent | Classgrid</a></li>

</ul>
</details>

**标签**: `#open-source AI`, `#multi-model agents`, `#coding agents`, `#GitHub projects`, `#AI tooling`

---

<a id="item-tech-news-22"></a>
### [OpenMinion 处于早期测试，CleverCloud 推出 AI 助手连接器](https://github.com/CleverCloud/clever-client.js) ⭐️ 5.0/10

OpenMinion 目前是一个处于 alpha（早期测试）阶段的“本地优先” AI 工具运行环境，主要在自己的电脑上运行，而不是依赖厂商云端；它支持 Python 3.11 及以上，提供命令行、Python 接口、HTTP 接口（让其他程序调用它的接口）、后台常驻执行、可查看的任务状态和可保存的会话，帖子称它尚未完成长期自主运行的认证。CleverCloud 则推出了一个 MCP 服务器（MCP 是一套让 AI 助手按统一方式调用外部工具和数据的约定），让 AI 助手通过 search（搜索）、execute（执行）、doc（文档）三个工具访问 Clever Cloud 的 API（应用程序接口，让其他程序调用它的功能）；该服务器用 TypeScript（一种编程语言）编写，要求 Node.js（一个运行这类程序的软件环境）26 或更高版本，并可通过配置文件和环境设置调整超时与最大输出。帖子主要把这两项进展当作“AI 工具正在走向集成化”的信号，没有给出 OpenMinion 的模型、安装步骤或可验证的性能数据。

telegram · aipluscn · 10月29日 14:24

**「背景：MCP 与 Clever Cloud 是什么」** MCP（Model Context Protocol，模型上下文协议）是一套公开的对接规范：服务方按它写好一个「小型服务器」，各种 AI 助手就能用同一套方式调用这些功能，不必为每个助手单独写对接代码。Clever Cloud 是一家法国的云托管平台（PaaS，即把服务器运维交给平台、用户只管上传自己的应用），这次的小服务器就是把它的平台接口包装成 search、execute、doc 三个 MCP 工具。OpenMinion 在代码仓库和 PyPI 上对自己的描述是「面向会调用工具的 AI 代理的 Python 本地运行时」，本身也支持 MCP，两个项目因此在同一套对接方式上相连。

**「实际影响」** 如果你使用 Clever Cloud 托管服务，并希望 AI 助手直接搜索、发起 API 调用或查文档，需要准备 Node.js 26 或更高版本；这类连接器让 AI 助手从“给建议”变成能实际操作云服务。OpenMinion 目前更适合试用：帖子明确说它处于 alpha 阶段，且尚未完成长期自主运行的认证，不宜用于无人看管的长时间任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/openminion/openminion">GitHub - openminion / openminion : Local - first Python runtime for...</a></li>
<li><a href="https://pypi.org/project/openminion/">openminion · PyPI</a></li>

</ul>
</details>

**标签**: `#MCP`, `#AI agent tooling`, `#local-first runtime`, `#developer tools`, `#GitHub projects`

---

<a id="item-tech-news-23"></a>
### [开源项目用 AI 把 Jira 工单自动变成待审代码](https://github.com/pruthvidarji1993/ai-automation-jira) ⭐️ 5.0/10

GitHub 上出现一个名为 ai-automation-jira 的开源 Python 项目，它把 Jira（常用的团队任务与工单管理工具）里的一张工单，自动推进到「已审核的代码修改请求」这一步。所谓代码修改请求（Pull Request，简称 PR），就是开发者把改好的代码提交上来、等人检查合并的环节。项目把它拆成 9 个阶段，中间设置了两处必须由人确认的关卡：确认方案、以及确认最终改动的代码差异。它可以使用 Claude Code 或 GitHub Copilot 这两款 AI 编程助手来驱动，并支持 Opus、Sonnet 等不同型号的模型。项目采用 MIT 许可证，代码可自由使用和修改。但它目前只有 1 个收藏（star）、0 个派生副本（fork），也没有任何公开证据证明这 9 个阶段能完整跑通，作者公布的只是安装说明和文档。

telegram · aipluscn · 10月30日 05:07

**「背景」** Jira 是公司里常见的任务与缺陷登记软件，每张“工单”代表一项待办；PR（Pull Request，合并代码前供人审阅的修改请求）是代码正式合入前的检查关口。Claude Code 和 GitHub Copilot 是能按文字指令读写代码的 AI 编程助手，这个项目想把填写工单、修改代码和人工审查这几步串成一条自动流程。

**「对使用者的实际意义」** 对想尝试的人来说，这个项目目前更像一份可以参考的流程模板，而不是可以直接放进团队生产环境的工具：没有跑通的演示，也几乎没有其他人验证过。若要试用，需要自己准备 Jira 账号、Claude Code 或 GitHub Copilot 的付费订阅，并在中间两处人工关卡上真正做审核；把它接入正式项目前，建议先用一张无关紧要的测试工单走一遍全流程。

**标签**: `#Jira`, `#Claude Code`, `#GitHub Copilot`, `#coding agents`, `#workflow automation`

---

<a id="item-tech-news-24"></a>
### [Web2Term：一个用网页版账号额度执行终端任务的开源工具](https://linux.do/u/kangnasi) ⭐️ 5.0/10

10 月 30 日，有开发者在 Linux.do 论坛发帖，介绍自己做的开源桌面工具 Web2Term：它把网页版 AI 对话、本机或远程服务器上的终端，以及项目文件放进同一个窗口（用 Electron 框架做成，即用网页技术编写桌面软件）。用户在这个软件里登录自己的 ChatGPT、Claude、DeepSeek 或 Gemini 账号，由模型理解目标并生成命令，再由软件在选定的机器上执行，并把结果回传到对话里。帖子没有给出安装步骤、版本号或运行演示，只让读者去看 GitHub 和官网，并建议开启 TUN 模式（让软件的网络流量走代理的一种模式）后使用；作者目前只推荐 ChatGPT 和 Claude 两项。帖子里还转述了一则传闻：ChatGPT Plus 网页端与 Codex（OpenAI 的编程助手）的额度可能要合并，发帖人用的是“听说”，没有截图、更新日志或复现，因此这只能算未证实的说法，还不是已经发生的额度调整。

telegram · linuxdo\_tg · 10月30日 05:13

**「背景：额度与这个工具」** ChatGPT Plus 是按月付费的订阅，用户在一定用量额度内使用网页对话；Codex 是 OpenAI 提供的编程辅助工具。发帖人认为网页端和 Codex 的额度原本分开计算，这是 Plus 的实惠之处，但“要和 Work 合并、共用额度”目前只是帖子里的“听说”，没有官方公告、截图或复现。帖子同时推荐的 Web2Term 是一个开源桌面工作区，把网页聊天窗口与本机或远程终端放在同一界面，让模型给出命令、由程序执行后把结果送回对话。

**「对用户意味着什么」** 对想用订阅账号而不是按用量付费的接口来跑这类工作的人来说，这个工具的吸引力在于不必额外买额度，但代价是需要自己准备代理网络环境。帖子把 DeepSeek 和 Gemini 列为“暂不推荐”，也没有说明多账号登录、额度耗尽或账号被限制时会出现什么情况，想尝试的人只能先到 GitHub 仓库自行确认安装方式和适用范围。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/naledao/Web2Term/tree/main">GitHub - naledao/Web2Term: Web2Term是一个桌面工作区：把网页端的对...</a></li>
<li><a href="https://web2term.kangnasi.xyz/">Web2Term — 让对话抵达终端</a></li>

</ul>
</details>

**标签**: `#chatgpt-plus`, `#quota-limits`, `#subscription-access`, `#open-source-projects`, `#web-to-terminal-harness`

---

<a id="item-tech-news-25"></a>
### [Kimi 接入 Gmail、Google Drive 与日历](http://kimi.ai/plugins) ⭐️ 5.0/10

Kimi（月之暗面公司的聊天助手）现在可以连接 Gmail、Google Drive 和 Google 日历：它能总结 Gmail 邮件串（同一主题往来的一组邮件）、在 Google Drive 中查找文件，并借助 Google 日历规划日程。连接通过 OAuth（一种由用户在同意后授权第三方访问账号数据、并可撤回的登录方式）完成，权限范围由用户自行控制，可在 kimi.ai/plugins 试用。目前没有公布哪些套餐可用，也没有说明邮件数量、文件数量或调用次数等限制。

telegram · zaihuapd · 10月29日 13:19

**「背景」** Kimi 是月之暗面（Moonshot AI）推出的对话式 AI 助手。Gmail、Google Drive 和 Google Calendar 分别是谷歌的邮件、云盘和日历服务。OAuth 是一种授权方式：用户不必把谷歌账号密码交给 Kimi，而是由谷歌发放授权，让 Kimi 只能访问用户勾选的数据范围。插件可以理解为给现有助手加装的外部功能模块，需要用户自己开启并授权。

**「实际影响」** 对日常用 Gmail 或 Google Drive 处理工作的人，邮件摘要和文件查找可以直接在 Kimi 里发起；实际使用前要在插件页用 Google 账号完成授权，并看清自己授予了哪些数据的访问权。

**标签**: `#Kimi`, `#Moonshot AI`, `#Google Workspace`, `#OAuth integrations`, `#product update`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [FCC 投票禁止中国实验室检测输美电子设备](https://www.reuters.com/business/media-telecom/fcc-votes-ban-all-chinese-labs-testing-us-electronics-2026-10-29/) ⭐️ 7.0/10

美国联邦通信委员会（FCC）10 月 29 日投票通过，禁止所有中国实验室为智能手机、相机、电脑等输美电子设备做检测认证，新规将于 2028 年 12 月生效。FCC 主席 Brendan Carr 称，2025 年有 82% 的电子产品在中国检测，美国本土检测仅约 4%，并称中美之间没有检测互认协议；这一规定是对 2025 年限制中国政府所属实验室措施的扩大。

telegram · zaihuapd · 10月30日 03:15

**「背景」** 此前，FCC 已于 2025 年 5 月通过规则，禁止由中国政府所有或控制的实验室参与美国无线设备的检测认证，并于同年 9 月启动程序，撤销 7 家此类实验室的资质。10 月 29 日的投票将限制范围从政府关联实验室扩大到所有中国实验室。

**「影响」** 直接受影响的是输美电子产品的品牌商和代工厂：它们需要在 2028 年 12 月前，把 FCC 认证测试转到美国境内或与美国有互认安排的实验室，认证所需的时间和成本会随之改变；中国检测实验室则会失去这部分认证业务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.fcc.gov/public/attachments/DOC-414369A1.pdf">FCC Takes Action on “Bad Labs” Apparently Controlled By China</a></li>
<li><a href="https://docs.fcc.gov/public/attachments/DOC-411576A1.pdf">FCC Bans ‘Bad Labs’ from U.S. Equipment Authorization Process</a></li>
<li><a href="https://www.theverge.com/policy/1009258/the-fcc-plans-to-ban-all-chinese-labs-from-testing-us-gadgets-by-2029">The FCC plans to ban all Chinese labs from testing US... | The Verge</a></li>
<li><a href="https://www.zerohedge.com/political/fcc-proposal-would-end-chinese-labs-role-us-device-testing">FCC Proposal Would End Chinese Labs &#x27; Role In US... | ZeroHedge</a></li>

</ul>
</details>

**标签**: `#FCC regulation`, `#US-China tech decoupling`, `#electronics supply chain`, `#product certification`, `#telecom policy`

---