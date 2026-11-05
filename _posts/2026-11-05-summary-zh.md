---
layout: default
title: "Horizon Summary: 2026-11-05 (ZH)"
date: 2026-11-05
lang: zh
---

> 从 130 条内容中筛选出 28 条重要资讯。

---

**科技新闻**
1. [Moonshot 公开 Kimi K3.1 Pro 权重，架构改动主打降低推理成本](#item-tech-news-1) ⭐️ 8.0/10
2. [Ripple-65B 预览：650 亿参数、权重公开的编程模型](#item-tech-news-2) ⭐️ 6.0/10
3. [在月租约 1500 卢布的 CPU 服务器上实测九款小型模型](#item-tech-news-3) ⭐️ 6.0/10
4. [16 GB 显存本地 Qwen：调整配置后作者称扳回一城](#item-tech-news-4) ⭐️ 6.0/10
5. [Keystone 推出 Claude Code 插件，协助安装自建 AI 模型网关](#item-tech-news-5) ⭐️ 6.0/10
6. [AgentScope 发布 Piccolo 决策模型系列，含 27B、9B 和 4B](#item-tech-news-6) ⭐️ 6.0/10
7. [第三方 Airtable MCP 工具：约 72 项操作，本地运行](#item-tech-news-7) ⭐️ 6.0/10
8. [new-api 候选版加签名缓存与任务插件原生接口](#item-tech-news-8) ⭐️ 5.0/10
9. [OpenAI 称 AI 生成近千个夺取 Linux 最高权限的攻击程序](#item-tech-news-9) ⭐️ 5.0/10
10. [Hugging Face 发布 Phonon TTS：宣称评测领先的本机语音合成模型](#item-tech-news-10) ⭐️ 5.0/10
11. [Dharma 推出文档转 JSON 抽取工具，但未公布具体细节](#item-tech-news-11) ⭐️ 5.0/10
12. [PiPedal：用树莓派模拟吉他效果器和音箱](#item-tech-news-12) ⭐️ 5.0/10
13. [Lumio 1.4 为 MacBook 刘海应用新增 Qwen Code 和 Cline 支持](#item-tech-news-13) ⭐️ 5.0/10
14. [自制家用 AI 助理用 LoRA 把聊天经历写进模型权重](#item-tech-news-14) ⭐️ 5.0/10
15. [评论：AI 助手 Claude 访问暂停 15 小时引出的依赖问题](#item-tech-news-15) ⭐️ 5.0/10
16. [pepper-orchestrator：把多模块改动拆给多个 AI 智能体并行处理](#item-tech-news-16) ⭐️ 5.0/10
17. [俄语博文主张：编程助手的项目上下文该存进代码仓库，而不是聊天记录](#item-tech-news-17) ⭐️ 5.0/10
18. [非程序员用 ESP32 和 24 GHz 雷达做出短租房噪音监测器](#item-tech-news-18) ⭐️ 5.0/10
19. [三个按钮加一块 0.96 英寸屏：他在 ESP8266 上直接编写梯形图](#item-tech-news-19) ⭐️ 5.0/10
20. [小米在青年公寓试运营机器人，连续执行任务超 30 分钟](#item-tech-news-20) ⭐️ 5.0/10
21. [华为云 11 月 15 日上线 openPangu-2.1-Pro，主打鸿蒙应用代码生成](#item-tech-news-21) ⭐️ 5.0/10
22. [agents-scaffold 发布：为多种 AI 编码代理提供项目模板](#item-tech-news-22) ⭐️ 5.0/10
23. [桌面工具 Isle 宣称新增 AI 用量统计与代理权限管理](#item-tech-news-23) ⭐️ 5.0/10
24. [AI 代理工具库 DmitriyYukhanov/agent-plugins 发布，是 AI 工具集成化趋势的信号](#item-tech-news-24) ⭐️ 5.0/10
25. [MaccyPlus 让 AI 程序用文字命令读写剪贴板历史](#item-tech-news-25) ⭐️ 5.0/10
26. [NVIDIA 推出 OpenShell，为 AI 代理设置独立权限](#item-tech-news-26) ⭐️ 5.0/10

**财经新闻**
1. [中国叫停软银 54 亿美元收购 ABB 机器人业务](#item-finance-news-1) ⭐️ 8.0/10
2. [任天堂 Switch 2 第二财季销量 267 万台，同比下滑 41%](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Moonshot 公开 Kimi K3.1 Pro 权重，架构改动主打降低推理成本](https://huggingface.co/moonshotai/Kimi-K3.1-Pro) ⭐️ 8.0/10

Moonshot AI 已在 Hugging Face 上公开 Kimi K3.1 Pro 的开放权重，也就是把训练好的模型参数直接放出，任何人都可以下载部署。据转述该消息的 Telegram 频道说，这次除了对「后训练」（基础模型训练完成后再做的一轮调教）做更新，还小幅改动了架构：把原来的 Gated MLA 换成 Gated DSA。评论者称，这一替换是为了降低推理成本（运行模型回答问题所需的算力开销）和 KV 缓存压力；KV 缓存是模型处理长文本时为了记住前文而占用的内存。来源本身没有给出任何基准测试数据，个人也基本无法在自己的机器上运行该模型——有评论估计需要一台配备 8 块 B300 显卡的服务器；因此普通用户实际多半是通过 OpenRouter 等第三方服务使用它，评论者称 Together 在相同价格下的吞吐量是 Moonshot 官方接口的两倍。

hackernews · abrarthought · 11月4日 15:30 · [社区讨论](https://news.ycombinator.com/item?id=50366999)

**「背景：K3 是什么，换掉的那层有什么用」** Kimi K3 是 Moonshot 在 2026 年 7 月发布的上一代旗舰模型，总参数约 2.8 万亿（参数可以粗略理解为模型内部的“连接”数量，越多通常越强，也越难跑起来），上下文窗口为 100 万 token（token 是模型处理文本的最小单位，100 万 token 大致相当于几十万个汉字），并且公开了模型权重（训练好的模型文件，别人可以下载后自行部署）。据第三方技术分析，K3 的注意力层（模型回答时回看前文、判断该重点看哪一句的机制）由 KDA 和 Gated MLA 两种按 3 比 1 混合组成。K3.1 是同一代的修补版本，这次改动落在其中一类注意力层上，把它换成 DSA，按 Moonshot 的说法是为了提升模型在大上下文下的效率，而不是让它整体更聪明。

**「实际影响」** 对每天用 Kimi 跑 Agent（让模型自己连续调用工具、多步完成任务）的人来说，实际可用的方式仍是第三方托管，而不是自己部署：OpenRouter 这类模型聚合平台（用一套账号和接口调用多家厂商的模型）已经在提供 K3.1 Pro，有评论称 Together 的出字速度（每秒生成多少内容）是同价位的 Moonshot 官方接口的两倍，Modal 又是 Together 的两倍。也就是说，同一个模型换一家供应商，速度和稳定性可能差出数倍而价格不变，接入前值得先测几家再定默认线路。自己部署并不现实，评论估计需要 8 张 B300 级别的数据中心显卡组成一台机器。

**「讨论中的不同看法」** 有评论者认为架构替换才是这次发布里最容易被忽略的关键，理论上能大幅降低长上下文时的内存压力。也有人持保留态度，称 K3.1 相比 DeepSeekV4.1-Flash 提升不大，在 Hy4 公布的内部基准上得分并不高，怀疑它是「为榜单调优」的模型。另有使用者报告各家托管服务速度差异明显：Together 吞吐约为官方接口的两倍，Modal 又是 Together 的两倍，并据此认为推理价格还有下降空间；还有评论认为，即便无法自建，这类发布也在推动推理能力从少数公司手中分散出来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://inferencex.semianalysis.com/model/kimi-k3">Kimi K3 — Architecture, Evals &amp; Inference Performance</a></li>
<li><a href="https://dhruvpendharkar.github.io/2026/07/31/understanding-kimi-k3s-attention.html">understanding kimi k3&#x27;s attention - dhruvpendharkar.github.io</a></li>
<li><a href="https://openrouter.ai/moonshotai/kimi-k3">Kimi K 3 - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**标签**: `#kimi`, `#open-weight-models`, `#moonshot-ai`, `#inference-cost`, `#model-release`

---

<a id="item-tech-news-2"></a>
### [Ripple-65B 预览：650 亿参数、权重公开的编程模型](https://www.ricursive.com/ripple) ⭐️ 6.0/10

Ripple-65B 以预览形式亮相：这是一个 650 亿参数的“开放权重”模型（权重可公开下载，供人自行运行或改造），主打“智能体编程”（让编程助手自己调用工具、连续完成多步编码任务），并称在这一方向上达到美国开放权重模型的最先进水平。但现有材料只有预览标题和讨论，没有许可证、权重下载、价格、上下文长度（模型一次能读入的文字量）或可复现的基准测试（用统一题目给模型打分）结果，因此还不能当作已经交付、可独立验证的能力。

hackernews · Philpax · 11月4日 18:53 · [社区讨论](https://news.ycombinator.com/item?id=50369925)

**「背景」** 这里的“智能体编程”指让 AI 自己调用工具、修改代码并反复试错，而不只是补全一行代码；开放权重则指训练好的模型参数可以下载，让外部在自己的服务器或电脑上运行，而不是只能通过厂商的在线服务调用。Ripple-65B Preview 以 Apache 2.0 许可（一种允许商用和修改的开源许可证）发布；它是 650 亿参数的稠密模型（每次计算都会用到全部参数），发布页称它用 12 万亿个 token（模型处理文本的基本单位）训练，上下文长度最高 100 万 token（一次能处理的文本量）。这种规模通常很难在普通家用显卡上流畅运行，也是社区讨论其自托管门槛的原因。

**「实际影响」** 对打算自己下载运行的人，650 亿参数的稠密模型（每次计算都要用上全部参数，而不是只激活一部分）在消费级显卡上会非常慢；评论中也有人指出这一点。若有团队想用它自建编程助手，应先等许可证、权重和可复现成绩公布，再判断能否部署。

**「社区讨论」** 评论者主要争两点：有人讽刺“最先进”被限定到“美国、开放权重、某个规模、某类基准”后已失去意义；也有人认为 65B 稠密模型对个人玩家太慢，难以像更小的 Qwen 模型那样流行。另有评论者给出 Terminal Bench 2.1（一个考模型在终端里完成任务的基准）的分数——Ripple-65B 为 80.5，Qwen 3.8 Flash Next 为 84.3——并提醒要看它是否针对该基准过度调优。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ricursive.com/ripple">Recursive Self-Improvement via AI for Chip... - Ricursive Intelligence</a></li>
<li><a href="https://iamag.it/en/news/ripple-65b-preview-open-weight-agentic-coding-model">Ripple - 65 B Preview: Dense 65 B Model Tops US Agentic Coding</a></li>

</ul>
</details>

**标签**: `#open-weight-models`, `#agentic-coding`, `#model-release`, `#benchmarks`, `#self-hosting`

---

<a id="item-tech-news-3"></a>
### [在月租约 1500 卢布的 CPU 服务器上实测九款小型模型](https://habr.com/ru/articles/1103894/?utm_campaign=1103894&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一位作者在 Habr 上发文，记录了自己在一台租来的普通服务器上运行小型 AI 模型的测试。这台服务器月租约 1500 卢布，配置为 4 个虚拟 CPU 核心、4 GB 内存，没有显卡，并预装了 Ollama（一个免费工具，用来下载并在本机运行公开的 AI 模型）。他选用了九个体量在 1B–4B 之间的模型（这里的 B 指十亿个参数，参数越多模型通常越大越强），让它们处理七项日常业务任务，例如归类客户来信、从邮件中提取联系方式、判断评价好坏，另外还做了一次压力测试，看这台机器能同时应付多少请求。需要说明的是，目前可见的正文只有开头部分，九款模型的具体名称、速度数据、质量对比和最终结论都还没有出现在其中，因此这次测试究竟得出了什么结果，暂时无法核实。

rss · Habr AI · 11月5日 10:44

**「背景」** 公司日常用的大型 AI 模型通常跑在昂贵的显卡上，而显卡本身也不容易买到。但很多任务其实不需要那么强的模型，就像不需要用显微镜去钉钉子。参数量在 1B–4B 的小模型可以只靠普通处理器运行，代价是回答更慢、复杂任务上更弱。这篇文章想回答的就是：一台最便宜的服务器，够不够撑起这类活儿。

**「对实际使用意味着什么」** 如果你正在为“读邮件、抽联系方式、给留言分类”这类简单活儿按次付费调用云端 AI，那么这项测试的关键数字是：一台 4 GB 内存的机器每分钟能处理多少条，以及小模型出错的比例有多高。这两个数字决定了它能否省钱，而目前公开的片段里还没有给出答案。另一个现实约束是内存：4 GB 能同时装下的模型和并发请求都很有限，规模稍大就需要加钱升级配置。

**标签**: `#local-inference`, `#ollama`, `#open-weight-models`, `#self-hosting`, `#vps-cost`

---

<a id="item-tech-news-4"></a>
### [16 GB 显存本地 Qwen：调整配置后作者称扳回一城](https://habr.com/ru/articles/1103784/?utm_campaign=1103784&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一位作者在一台装有英伟达 RTX 5080 显卡（16 GB 显存，即显卡自带的内存）和 62 GB 内存的工作站上，重新测试了本地运行的 Qwen 3.8，并称调整后它在同样硬件上“扳回一城”。此前测试中，经过量化压缩的 Qwen 3.8（量化指把模型文件压小，以便塞进有限显存）在实验室日志问答上只答对 8/24，另一个本地模型 gpt-oss-20b 为 40%。在三个闭源 Delphi 程序（一种编程语言）的修错任务中，Qwen 3.8 Coder 完成 16/20，低于云端 Claude Sonnet 5.5 的 19/20。作者把差距部分归因于模型压缩过度、运行软件的配置不当，以及工具对数据格式小错误过于苛刻；改用完整模型文件并修正后称本地模型明显改善，但摘录没有给出新分数或完整配置。

rss · Habr AI · 11月5日 08:36

**「背景」** 这位作者一直在自己的一台工作站上测试本地运行的语言模型：硬件是一块 RTX 5080 显卡（16 GB 显存，即显卡上专门用来存放模型的内存）和 62 GB 内存，题目来自他日常的实验室电子日志数据处理，以及三个用 Delphi（一种编程工具）开发的内部项目的修错工作。更早的测试为了让模型塞进有限的显存，用了压缩程度很高的模型版本（业内叫“量化”，也就是降低模型参数的精度、把文件变小），结果本地模型明显落后于云端最强的几款模型。本文接着排查差距来自硬件上限还是设置问题：他把被裁剪的模型参数文件（权重）换成更完整的版本，并调整服务器和工具配置。

**「实际影响」** 对用 16 GB 显卡跑本地模型的人，实际教训是：遇到答对率不理想，先检查模型是否压缩过度、运行软件的设置是否合适，再考虑加显卡；但文章摘录没有给出可照抄的设置，复现这次改善仍需查看原文的完整配置。

**标签**: `#local LLM`, `#Qwen`, `#quantization`, `#VRAM`, `#model comparison`

---

<a id="item-tech-news-5"></a>
### [Keystone 推出 Claude Code 插件，协助安装自建 AI 模型网关](https://habr.com/ru/articles/1100548/?utm_campaign=1100548&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一篇 Habr 文章介绍了 Keystone 面向 Claude Code（Anthropic 的编程助手）的插件，目标是让用户在跟助手的一次对话中装好这个自建 AI 模型网关。Keystone 本身是一个自建模型网关，也就是自己部署、统一接收各家 AI 模型的请求，并保管密钥和花费限额的服务。文章说，插件带有八项预先写好的操作技能，知道真实的命令、选项和配置项；另有一个 MCP 服务器（让助手能查询外部服务状态的接口），使助手能看到网关上正在运行什么。文章还称密钥不会进入聊天。不过目前可见内容主要是一段介绍，没有安装命令、配置示例或独立测试结果，因此“在一次对话里装好”目前只是文章的说法，尚不能确认实际效果。

rss · Habr AI · 11月5日 08:30

**「背景」** Claude Code 是 Anthropic 的命令行编程助手，用户用自然语言交代任务，它就能在项目里执行命令、修改文件；MCP（Model Context Protocol，模型上下文协议）则是让这类助手连接外部工具的一套通用接口。Keystone（KTMS）是一个自托管（装在自己或公司的服务器上，而不是用厂商的云服务）的 LLM（大语言模型）网关：各种服务只连它一个地址，由它统一保管各家模型厂商的密钥、按规则挑选模型、在故障时切换，并控制花费上限。这篇帖子介绍的插件把 Keystone 的真实命令、参数和配置字段整理成 Claude Code 可调用的操作指南（文中称为“技能”），再通过 MCP 服务器让助手查看网关当前运行状态。

**「实际影响」** 对需要把多家模型服务接到一个入口的团队，按文章描述，安装和排查时不必把供应商密钥贴进聊天，助手还能依据网关的实际运行状态给出操作，而不是猜一套并不存在的配置项。问题在于现有摘录没有给出安装命令、配置样例或兼容性说明，读者无法据此判断是否真能一次装好。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ai-process/ktms">GitHub - ai-process/ ktms : Self - hosted LLM gateway : vendor keys...</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#MCP`, `#LLM gateway`, `#self-hosted`, `#developer tooling`

---

<a id="item-tech-news-6"></a>
### [AgentScope 发布 Piccolo 决策模型系列，含 27B、9B 和 4B](https://linux.do/u/chenxr) ⭐️ 6.0/10

AgentScope 团队宣布推出 Piccolo 决策模型系列，包含 27B、9B 和 4B 三个尺寸（B 指模型参数量，单位为十亿，数字越大通常模型越大）。团队同时提供了在线体验页面，以及 ModelScope 网站上的模型下载链接。不过，目前公布的信息只有这些入口，没有给出评测成绩、授权条款、硬件要求或价格，因此还无法判断这些模型的实际能力和使用条件。

telegram · linuxdo\_tg · 11月5日 14:33

**「背景」** Piccolo 型号中的 27B、9B、4B 指模型参数量约为 270 亿、90 亿和 40 亿；同一系列里参数越多，通常能力更强，但运行所需的内存和算力也更大。AgentScope 这次同时给出了在线体验页面和魔搭社区的下载入口，但公告没有说明这些“决策模型”具体负责哪类判断，也没有交代许可条款或硬件要求。

**「实际影响」** 对普通用户来说，最直接的变化是：不需要下载任何东西，就能在官方网页试玩页面（decisionplayground.agentscope.io）里试用这个模型。打算把它装到自己电脑或公司服务器上的人现在还没法判断：官方只给了 ModelScope 下载链接，没有说明运行需要多大的显存（显卡内存）、采用什么许可协议、能否商用，也没有说 27B、9B、4B 三个尺寸分别适合什么设备；这些信息要等团队补充后才能决定是否采用。

**标签**: `#模型发布`, `#开源模型`, `#AgentScope`, `#Piccolo`, `#决策模型`

---

<a id="item-tech-news-7"></a>
### [第三方 Airtable MCP 工具：约 72 项操作，本地运行](https://github.com/Automations-Project/VSCode-Airtable-Formula) ⭐️ 6.0/10

一款面向 Airtable 用户的开源 MCP 工具已发布。MCP 是一种让 AI 助手调用外部软件和数据的通用接口，这套工具以 VS Code 扩展和 MCP 服务器的形式，把对 Airtable 表格的约 72 项操作交给 AI 助手执行。据项目介绍，它可一键安装进 VS Code、Cursor、Windsurf、Claude Desktop、Cline、Amp 等 AI 编辑器，并可在本机运行，数据不离开电脑；登录凭证保存在操作系统密钥链中，权限分为只读、安全写入和完全访问三档，还支持公式校验、创建字段、管理视图、复制记录等操作。需要留意的是，它调用的是 Airtable 的内部接口，而非官方对外提供的 REST API（即网站给其他程序调用的标准入口），因此功能更全，但稳定性取决于 Airtable 会不会改动这些内部接口——原文提到这一点，却没有做测试。项目采用 MIT 许可证、免费使用，可与 Airtable 官方 MCP 服务器并用；目前所有说法均来自推广方，尚无第三方实测。

telegram · aipluscn · 11月5日 01:48

**「背景：MCP 与 Airtable 的内部接口」** Airtable 是一款把表格和数据库结合起来的在线协作工具，很多团队用它管理项目、客户名单和内容素材。MCP（Model Context Protocol，一种让 AI 助手调用外部软件和数据的通用接口）则让装在 VS Code、Cursor 这类编辑器里的 AI 能直接读写这些数据。Airtable 本身有官方提供的这类接口，但能做的事情有限；这个项目改用 Airtable 内部自己调用的那套接口，因此能覆盖更多操作，代价是内部接口并非对外承诺长期不变，Airtable 一旦调整，工具就可能失灵。

**「实际影响与注意事项」** 对已经在用 Airtable 管理表格和数据的用户来说，这个工具的实际影响是要在它和 Airtable 官方自家的 MCP 服务器之间做选择：官方版本由 Airtable 直接维护，能连接 Claude、ChatGPT、Cursor 等工具来读数据、建记录和做自动化（见 Airtable 官方文档）。这个第三方扩展功能更多，但走的是 Airtable 未公开的内部接口，Airtable 一旦调整内部结构就可能失效，而且不会提前通知。安装时建议先用只读模式试，确认 AI 读取的范围符合预期，再决定是否开放写入或完全访问权限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/automations-Project/VSCode-Airtable-Formula">GitHub - Automations - Project / VSCode - Airtable - Formula : VS Code...</a></li>
<li><a href="https://support.airtable.com/articles/9897799762-using-the-airtable-mcp-server">Using the Airtable MCP server</a></li>
<li><a href="https://airtable.com/developers/agents/mcp/getting-started">MCP server overview - Airtable Developers</a></li>

</ul>
</details>

**标签**: `#mcp`, `#airtable`, `#developer-tooling`, `#vscode-extension`, `#open-source`

---

<a id="item-tech-news-8"></a>
### [new-api 候选版加签名缓存与任务插件原生接口](https://github.com/QuantumNous/new-api/releases/tag/v1.0.0-rc.48) ⭐️ 5.0/10

自建 AI 服务中转软件 new-api 发布 v1.0.0-rc.48 候选版（正式版之前的测试版本），给 Redis（一种常用的内存数据库）里的用户、调用凭证和登录会话缓存加上了签名，用来验证这些内容没有被改过。多节点部署必须把所有节点一起升级，否则新节点遇到旧版本写入的缓存时，会回到数据库重新读取。任务类插件（把可灵等外部生成服务接入 new-api 的扩展）现在可以直接使用厂商自己规定的接口地址，原有带 new-api 前缀的地址仍然可用；但可灵、Vidu、MiniMax 和火山方舟的请求如果带 callback\_url（任务完成后由厂商回调通知的网址）会被拒绝。版本还增加了任务模型的价格提醒：插件改动后无法继续计费的模型，会在“模型定价”里标为“价格待处理”。

github · Calcium-Ion · 11月4日 15:40

**「背景」** new-api 是一个可自行部署的开源“中转网关”：服务运营者用它把多家 AI 模型提供商的接口接到同一个入口，并统一管理访问密钥、用量和计费。普通用户通常不会直接打开它，而是间接使用由它转发出去的模型服务。版本号里的 rc 指候选发布版（正式版前供测试的版本）；这个项目把用户、令牌和会话等频繁读取的数据放在 Redis（一种常用的内存缓存数据库）里，因此升级时会涉及缓存兼容和多节点部署。

**「影响」** 对运行 new-api 的团队来说，最直接的动作是把多节点部署一次性全部升级，否则新节点每次遇到旧缓存都要回数据库重新读取；升级后还应检查“模型定价”里的“价格待处理”列表，避免插件改动后继续提供无法计费的任务模型。

**标签**: `#api-relay`, `#self-hosted`, `#release-notes`, `#coding-tooling`, `#security`

---

<a id="item-tech-news-9"></a>
### [OpenAI 称 AI 生成近千个夺取 Linux 最高权限的攻击程序](https://openai.com/index/a-thousand-fewer-paths-to-root/) ⭐️ 5.0/10

OpenAI 的网络攻防团队在官网发布报告称，其自动化漏洞研究流程在 2026 年 10 月对 Linux 内核（服务器和安卓手机底层运行的核心程序）做了一次扫描，动态复现出 1,724 个漏洞，并写出 948 个可用的攻击程序，让本机上的普通用户直接拿到 root（系统的最高管理员权限），另有 291 个只用于证明漏洞存在的信息泄露验证程序。报告称总 API（按调用量计费的模型接口）开销约 121 万美元，平均每个成功夺取最高权限的攻击程序约 1,279 美元，团队表示实际开发成本更低、约 359 美元。报告还称其中至少 10 种攻击手法是此前未知的新方法，并有外部专家确认其新颖性。但这是厂商自述：报告没有公布所用模型版本、代码或漏洞清单，外界无法独立验证，也没有说明这些漏洞是否已上报给 Linux 维护者。

hackernews · dangelosaurus · 11月4日 23:33 · [社区讨论](https://news.ycombinator.com/item?id=50372929)

**「背景知识」** Linux 内核是这类系统的核心部件，负责管理内存、设备和权限；一旦内核里存在“提权漏洞”，普通账号的用户就能借它拿到最高管理员权限（root），相当于从普通住户变成能改整栋楼门锁的人。所谓“自主漏洞研究流水线”，是指让 AI 程序自己去读代码、复现缺陷，并写出真正能用的攻击程序（exploit），而不是由人逐行排查。正因如此，外界关心的不只是发现了多少条路径，还包括这些缺陷分布在哪些子系统、属于哪类问题，以及换一套代码是否还能同样奏效。

**「对普通用户意味着什么」** 对使用 Linux 服务器、路由器或安卓手机的人来说，实际影响落在打补丁这一步：OpenAI 称这条流水线除了找出 948 个提权漏洞，还为每个漏洞生成了修复补丁；如果这些补丁被内核社区接受，它们就会以常规安全更新的形式推送到各发行版，用户需要及时安装。但材料没有说明这些补丁有多少已被上游采纳，也没有给出漏洞在各子系统（内核中负责不同功能的模块）中的分布，所以暂时无法判断哪些设备会先收到修复。用于发现漏洞的是一个尚未发布的、专门面向网络安全的模型，外部安全团队无法用同样的工具自查代码，防守方只能等公开的更新。

**「社区讨论」** 讨论中最集中的疑问是数据不够细：一位评论者希望看到漏洞分布在哪些子系统、易受攻击代码的存在时间中位数，以及它们属于内存破坏、逻辑错误还是并发时序问题，认为只有这些信息才能判断该方法能否迁移到别的代码库。也有人怀疑这 948 个并不是 948 个彼此独立的缺陷，并用“一个 SQL 注入漏洞（把恶意指令混进数据库查询）可以有几千种利用写法”作类比，认为这更像宣传而非可核查的结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/openai-ai-pipeline-generates-948-linux.html">OpenAI AI Pipeline Generates 948 Linux Root Escalation ...</a></li>
<li><a href="https://openai.com/index/a-thousand-fewer-paths-to-root/">A thousand fewer paths to root - OpenAI</a></li>
<li><a href="https://startupfortune.com/openais-ai-pipeline-turned-2308-linux-kernel-bugs-into-948-root-exploits/">OpenAI&#x27;s AI pipeline turned 2,308 Linux kernel bugs into 948 ...</a></li>

</ul>
</details>

**标签**: `#AI security research`, `#OpenAI`, `#autonomous agents`, `#Linux kernel`, `#capability claims`

---

<a id="item-tech-news-10"></a>
### [Hugging Face 发布 Phonon TTS：宣称评测领先的本机语音合成模型](https://huggingface.co/blog/phonon-tts) ⭐️ 5.0/10

Hugging Face 于 11 月 5 日在其博客发布 Phonon TTS，这是一个语音合成（TTS，把文字转成朗读音频）模型，特点是直接在本机运行，不必把文字上传到云端服务器。博文宣称该模型在公开评测（benchmark，用统一测试集给模型打分并排名）中名列前茅，但发布内容没有给出模型参数量、授权许可、运行速度数据，也没有说明模型文件（训练好的权重）和代码是否可供下载，因此这些领先说法目前无法被外部核实。对于想在手机或电脑本地做语音朗读、又不想把内容发到云端的人来说，这值得关注，但要等具体发布细节确认后才能判断是否可用。

rss · Hugging Face Blog · 11月5日 00:00

**「背景」** 文本转语音（TTS）就是把文字读成声音。Phonon TTS 是 Gradium 的一套小型 TTS 模型，Hugging Face 博客称它能在用户自己的设备上运行，不需要服务器或网络，输入的文字也不会离开设备。一个浏览器版本的项目资料显示，这个模型约有 3100 万个参数（参数是模型内部可调整的数值，数量通常用来衡量模型大小），首次使用需下载约 44.3 MB 的文件，之后可从浏览器缓存读取。

**「实际使用前需要确认版本与授权」** 如果你打算把语音合成放进手机应用或本地程序，先要弄清拿到的是哪一个版本：外部报道显示，Gradium 在 10 月以 Apache 2.0 协议（可商用、不必另行申请授权）开放的是 3100 万参数的小模型，而产品页描述的是约 1 亿参数的版本、走另外的授权方式；参数指模型内部的数值规模，规模越大通常越占内存，两者对硬件的要求不同，选错会直接决定它能否在断网设备上跑起来。另一个现实问题是，厂商所说的榜单领先来自公开测试集，与你的实际文本（专有名词、专业术语、口音、数字读法）差别很大，上线前应当用自己的句子测一遍首次出声的延迟和读错率，而不是直接照搬榜单结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/docs/transformers/v5.22.1/model_doc/gradium_phonon_tts">Gradium Phonon TTS - Hugging Face</a></li>
<li><a href="https://github.com/huggingface/blog/blob/main/phonon-tts.md">blog/phonon-tts.md at main · huggingface/blog · GitHub</a></li>
<li><a href="https://github.com/blixt/phonon">GitHub - blixt/phonon: Phonon 31M text-to-speech on WebGPU ...</a></li>
<li><a href="https://lancartech.co.id/en/blog/phonon-tts-on-device-memilih-lisensi-dan-runtime">Phonon On-Device TTS: Picking a License, a Runtime, and a ...</a></li>
<li><a href="https://gradium.ai/content/gradium-phonon-on-device-tts">Gradium Phonon: On-Device Text-to-Speech | Gradium</a></li>
<li><a href="https://www.marktechpost.com/2026/10/22/gradium-phonon-31m-on-device-tts/">Gradium Open-Sources Phonon, a 31M-Parameter On-Device TTS ...</a></li>

</ul>
</details>

**标签**: `#TTS`, `#on-device AI`, `#open-weight models`, `#Hugging Face`, `#benchmarks`

---

<a id="item-tech-news-11"></a>
### [Dharma 推出文档转 JSON 抽取工具，但未公布具体细节](https://huggingface.co/blog/Dharma-AI/dharma-field-extractor) ⭐️ 5.0/10

Hugging Face 社区博客上出现一篇文章，介绍一个名为 Dharma Field Extractor 的工具，声称能把“任何文档”提取成 JSON 格式的结构化字段（JSON 是一种用“字段名＋对应值”组织信息的数据格式，程序很容易读取）。但该文章目前只有标题和链接，没有给出模型规格、价格、评测成绩或安装使用方法。目前也没有证据表明它已经发布了可直接下载或试用的版本，因此无法判断实际效果如何，以及它适用于哪些文档类型。

rss · Hugging Face Blog · 11月4日 17:50

**「背景」** 过去要把扫描件或照片里的信息整理成表格，通常得先用文字识别（OCR，把图片里的字转成可编辑文字）读一遍，再让另一个程序按固定格式去填。Dharma Field Extractor 把这两步合成一步：直接读文档图片，输出 JSON（一种计算机容易读取的“字段名＋内容”文本格式），既可以自动找出文档里有什么字段，也可以按用户事先给定的字段清单来填。据 Hugging Face 上的介绍文章，它是一个 20 亿参数的小模型——参数可粗略理解为模型的内部设置数量，越少通常运行越便宜——由 Dharma-AI 在自家的文字识别模型 DharmaOCR-LITE v1.1 基础上用 LoRA 适配器改造而来，这种适配器的做法是只额外训练一小部分参数，把通用模型调成专用模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/Dharma-AI/dharma-field-extractor">Dharma Field Extractor: Any Document In, Structured Fields in ...</a></li>
<li><a href="https://huggingface.blog/blog/dharma-ai-dharma-field-extractor/">Schema-First Document Extraction Needs More Than Valid JSON</a></li>
<li><a href="https://explainx.ai/blog/dharma-field-extractor-2b-document-to-json-0-834-vs-claude-opus-5-0-816-l40s-claimed-vs-verified-2026">Dharma Field Extractor: 2B Model Beats Opus 5? Checked ...</a></li>

</ul>
</details>

**标签**: `#document extraction`, `#structured output`, `#JSON`, `#Hugging Face`, `#AI tooling`

---

<a id="item-tech-news-12"></a>
### [PiPedal：用树莓派模拟吉他效果器和音箱](https://hackaday.com/2026/11/04/pipedal-grants-guitar-effects-amp-emulation-and-more/) ⭐️ 5.0/10

Hackaday 介绍了一个名为 PiPedal 的项目：它让树莓派（一种信用卡大小的低价小型电脑）或类似的单板电脑负责处理吉他效果和音箱模拟（用软件模仿不同吉他音箱的声音），用户通过手机、平板或网页浏览器来调节。报道没有给出新版本号、价格或安装步骤，也没有提供延迟和音质的独立测试数据，只说明项目代码和文档放在 GitHub（一个存放和协作代码的网站）上。对于想少买几块效果器踏板和音箱的吉他手，这提供了一条用现有小电脑搭建音色系统的路径。

rss · Hackaday · 11月5日 06:00

**「背景」** 电吉他效果器通常是一只脚踏小盒子，用来改变音色；吉他音箱模拟则是用软件模仿不同音箱的声音，过去这两类设备往往要分开购买。PiPedal 是一套开源软件（代码公开、可自行修改），运行在树莓派（Raspberry Pi，一种信用卡大小的低价小型电脑）这类单板计算机上，用户通过手机、平板或网页浏览器选择效果并调节参数。它把处理声音的工作放在这块小电脑上完成，因此不必购买一堆实体踏板或音箱。

**「实际影响」** 实际动手的人要先查项目文档，确认自己的树莓派型号和音频输入输出设备能配合工作；报道没有列出兼容清单，也没有说明现场演出所需的低延迟表现。调节音色时用手机或浏览器操作，可以少接一台显示器和键鼠，这是它相对传统踏板组合最直接的使用差异。

**标签**: `#raspberry-pi`, `#guitar-effects`, `#amp-emulation`, `#audio`, `#hardware`

---

<a id="item-tech-news-13"></a>
### [Lumio 1.4 为 MacBook 刘海应用新增 Qwen Code 和 Cline 支持](https://habr.com/ru/articles/1103620/?utm_campaign=1103620&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

据开发者介绍，Lumio 1.4 是一款免费 MacBook 应用，常驻屏幕顶部刘海，用来查看哪些 AI 编程助手（能自行读写代码、执行命令的 AI 程序）正在工作、哪些在等待用户确认，并可从刘海一键批准命令。新版本在原有 Claude Code、Codex、Cursor 等之外，加入了对 Qwen Code 和 Cline 的支持。应用还会用像素办公室展示每个会话：对应一个小人坐在桌前，喝咖啡，晚上开灯。这篇发布说明没有给出安装方式或具体系统要求。

rss · Habr AI · 11月5日 10:35

**「背景」** Claude Code、Codex、Qwen Code 和 Cline 都属于“AI 编程代理”：接到任务后，它们会读写代码、运行命令，并在执行某些操作前停下来等用户确认。Lumio 的作用是把这些等待确认的请求集中显示在 MacBook 屏幕顶部凹口（俗称“刘海”）里，让用户不必在各个窗口之间来回切换。

**「对使用者的实际影响」** 对同时开好几个编程智能体（能自己写代码、跑命令的 AI 程序）的人来说，升级到 1.4 后，Qwen Code 和 Cline 的会话会和其他智能体一起出现在 MacBook 的刘海里；某个智能体需要你批准一条命令时，直接在刘海里点一下就行，不必切回终端窗口去找它。限制是它只适用于带刘海的 MacBook，外接显示器或没有刘海的 Mac 用不上；软件本身免费。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lumiomac.com/">Lumio for Mac: your AI agents, in the notch</a></li>
<li><a href="https://www.youtube.com/shorts/TxF-wLDpLQg">My AI agents got an office · Lumio 1.4 #shorts - YouTube AI coding agents, right in the MacBook notch — Lumio Lumio — your AI agents, in the Mac notch - YouTube GitHub - shixiaoke1004-cmyk/Lumio: Turn your MacBook&#x27;s notch ... Lumio — your Claude Code &amp; Codex agents, in the MacBook notch</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#macOS app`, `#developer tooling`, `#Lumio`, `#Qwen Code`

---

<a id="item-tech-news-14"></a>
### [自制家用 AI 助理用 LoRA 把聊天经历写进模型权重](https://habr.com/ru/articles/1103860/?utm_campaign=1103860&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位爱好者把自己在家用硬件上运行的 AI 助理项目更新到第四部分：他把助理长期积累的对话和行为记录整理成训练样本，用 LoRA（一种只额外训练少量参数、给现成模型“补课”的低成本微调方法）把这些经历直接写进模型权重，而不是每次对话时再翻查历史。作者称，经过监督微调（用整理好的问答样本继续训练模型）后，模型在 IFEval（检查模型是否照指令做事的测试集）上提高 2%，在 LogiQA（逻辑推理测试集）上提高 12%；他还通过纠正行为和加入一份“动机契约”，让助理能连续自主执行 100 步而不偏离目标。文中另称，微调后的模型用 73 分钟改写了助理自己的系统，把它切换成语音对话模式（语音转文字加文字转语音）。这些数字都出自作者自己的测试，摘录没有给出所用模型名称、训练样本数量、硬件配置和花费，也没有可复现的对照实验。

rss · Habr AI · 11月5日 10:03

**「背景」** 这是 Habr 上一个连载项目的第四篇。据 9 月的首篇介绍，作者用两块 12GB 显存的消费级显卡在家里运行本地 AI 助手，把语言模型与检索、图结构记忆、外部工具调用和语音输入输出组合在一起（工具搜索结果 tool-2-1、tool-2-3）。LoRA 是一种外挂式的轻量微调办法：不重新训练整个模型，只训练一小块附加参数并挂到原模型上，用一批示例改变模型的回答习惯；这种用示范对话教模型的做法通常称为 SFT（监督微调）。

**「对自建助理的人意味着什么」** 对想在自己电脑上跑 AI 助理的人来说，这个方向的实际吸引力在于把日积月累的使用习惯固化进模型，不必每次启动都重新交代背景。但目前它只能当作个人实验记录看：没有模型名、数据量和硬件清单，别人无法照做，也无法判断 2% 和 12% 的提升是方法有效还是测试波动；作者在同一篇里还更换了模型和硬件，读者很难分清进步来自训练还是来自换新。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://habr.com/ru/articles/1083752/">Как я создавал персонального ассистента на домашнем железе</a></li>
<li><a href="https://www.braintools.ru/article/35687">Как я создавал персонального ассистента на домашнем железе</a></li>

</ul>
</details>

**标签**: `#LoRA`, `#fine-tuning`, `#local LLM`, `#personal assistant`, `#self-hosted AI`

---

<a id="item-tech-news-15"></a>
### [评论：AI 助手 Claude 访问暂停 15 小时引出的依赖问题](https://habr.com/ru/articles/1103470/?utm_campaign=1103470&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

这是一篇评论，不是新的事件报道：它围绕 2026 年 4 月金融科技公司 Belo 的 60 多名员工无法使用 AI 助手 Claude 约 15 小时一事，讨论企业把工作流程交给单一 AI 供应商的风险。据文章转述，停用通知称相关账号违反了使用规则，但没有给出具体细节，只提供了一份申诉表；约 15 小时后访问恢复，这次封锁后来被称作可能的误判。Belo 当时还有另一款 AI 助手 Gemini 可用，但由于已经积累了对话历史、常用工具和系统集成，公司没能迅速切换。文章明确说，这些细节来自公司公开说法和媒体报道，并非独立调查；作者进一步提出假设：如果企业连一线支持、财务操作、销售辅助和编程都依赖 AI，那么一旦供应商涨价、限制访问或新模型变差，恢复工作会有多难。

rss · Habr AI · 11月5日 07:11

**「背景」** Claude 和 Gemini 都是企业可以购买的 AI 助手服务，公司能把客服、文档处理或编程等工作接到这类服务上。问题在于，企业一旦围绕某一家服务积累了大量对话记录、配套工具和系统连接，账号被暂停后就不只是换一个登录入口，重新搭好替代方案也需要时间。Belo 的经历说明，平时越依赖某一家服务，临时切换的代价就越高。

**「实际影响」** 对已经让 AI 承担客服一线、财务操作、销售辅助或编程的公司，这件事的具体提醒是：多准备一个备用服务，并不等于有了备用流程；切换还会被积累的对话历史、定制工具和现有集成拖慢。这篇评论因此建议企业事先确认，哪些工作能在没有原供应商的情况下继续运转。

**标签**: `#Claude`, `#account suspensions`, `#AI dependency`, `#vendor lock-in`, `#access restrictions`

---

<a id="item-tech-news-16"></a>
### [pepper-orchestrator：把多模块改动拆给多个 AI 智能体并行处理](https://habr.com/ru/articles/1103656/?utm_campaign=1103656&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

Habr 上署名 MNikitin 的作者介绍了其团队开发的插件 pepper-orchestrator，它面向 Claude Code 和 Codex 这两款 AI 编程助手（在终端里读代码、改文件并执行命令的智能体工具）。据文中描述，插件会把一个目标转成一份“程序”和若干工作包，各部分交给不同智能体同时去做，而每一处“完成”都要单独经过一次独立验证，而不是由动手改代码的那个智能体自己确认。文章称用一个真实案例从头到尾走了一遍，从第一条命令一直到交付。但可见内容没有给出插件的版本号、价格、获取或安装方式，也没有可复现的案例数据，所以它实际效果如何目前没有独立验证。

rss · Habr AI · 11月4日 21:50

**「背景：什么是“智能体”和上下文窗口」** Claude Code（Anthropic 推出的写代码助手）和 Codex（OpenAI 的同类工具）都能让 AI 在项目里自己读文件、改代码、执行命令，这类能连续完成多步操作、而不是只回答一个问题的程序，通常被称为“智能体”（agent）。它们在一次会话里能记住的内容有上限，这个上限叫上下文窗口；当一个需求同时牵涉多个模块或多个代码仓库时，需求说明加上相关代码往往塞不进一次会话，于是出现“改一处、崩一处”的问题。作者所说的 pepper-orchestrator 就是按这个思路做的插件（给现成软件添加功能的小模块）；据一个收录页面的说明，这类插件要解压到 Claude Code 的个人 skills 目录、重启后再按提示调用。

**「对使用者的实际影响」** 对常用 Claude Code 或 Codex 一次改动多个模块的人来说，这套方案瞄准的是一个具体麻烦：改一处容易在另一处出问题，而完整的需求说明又超出一次会话的上下文窗口（模型一次能读入的内容量上限）。不过文章没有说明安装方式、支持的模型或版本范围，以及是否收费，读者暂时无法判断能不能用在自家项目上，只能先当作思路参考。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.agensi.io/skills/pepper-orchestrator-for-claude-code">Pepper Orchestrator for Claude Code - Agensi</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#Codex`, `#AI agents`, `#orchestration`, `#developer tooling`

---

<a id="item-tech-news-17"></a>
### [俄语博文主张：编程助手的项目上下文该存进代码仓库，而不是聊天记录](https://habr.com/ru/articles/1103614/?utm_campaign=1103614&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

11 月 4 日，Hubr 上的一篇俄语博文公开反对另一位作者的做法。那位作者写了自己如何从 Claude Code 迁移到 Codex（两者都是能读写代码、替人干活的编程助手），并保留了聊天历史。本文作者认为，把过去的对话存档并不等于留下了项目的最终决定。他提出的替代方案是把项目上下文放进代码仓库（存放项目文件、带版本记录的文件夹），并称自己这样做已有半年，还把方法整理成一套叫 GRACE 的流程，最终做成一个名为 doubled-graph 的小工具。需要注意的是，目前只能看到文章的开头部分：没有配置方法、安装步骤，也没有任何证据说明这个工具确实有效，因此读者暂时无法照做。

rss · Habr AI · 11月4日 17:55

**「背景」** 这篇 Habr 文章是在回应另一篇《离开 Claude Code 之后：我如何迁移到 Codex 并保留项目历史》。Claude Code 和 Codex 都是能读项目文件、替人改代码的 AI 编程助手；前一篇的做法是把项目历史留在聊天记录里，本文作者反对这样做，因为聊天记录留下的是讨论过程，不是最终决定。他称自己过去半年把项目背景放在代码仓库（存放代码和说明文件的地方）里，用的是 GRACE 方法，并把它整理成 doubled-graph 工具；据 ai-manual.ru 介绍，这套方法用五个交代项目背景的文件、两组约定标记和两张关系图来记录项目结构和改动（tool-1-1），Dzen 上的说明则称使用方式是安装工具后让助手先“读仓库”（tool-1-2）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai-manual.ru/article/kontekst-proekta-v-repozitorii-a-ne-v-chate-kak-ustroenyi-metodika-grace-i-utilita-doubled-graph/">Контекст проекта в репозитории , а не в чате: как... | AiManual</a></li>
<li><a href="https://dzen.ru/a/auu-O-BozWj2Mre3">Храните контекст в репозитории , а не в чатах, чтобы... | Дзен</a></li>

</ul>
</details>

**标签**: `#coding agents`, `#context management`, `#Claude Code`, `#Codex`, `#developer workflow`

---

<a id="item-tech-news-18"></a>
### [非程序员用 ESP32 和 24 GHz 雷达做出短租房噪音监测器](https://habr.com/ru/articles/1103842/?utm_campaign=1103842&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位自称海关报关员的作者在 Habr 发文，介绍他给短租房做的一款噪音与人员监测器：用 ESP32（一种便宜、可编程、自带联网功能的小电路板）测量噪音的分贝值（dBA，按人耳感受加权的声音大小单位），再用 24 GHz 雷达（靠无线电波判断屋里有没有人活动）确认房间是否有人，客人入住或吵闹时向房东手机推送通知。设备通过加密的 MQTT（设备与服务器之间传消息的轻量协议）上报数据，后端使用 Node.js 和 PostgreSQL，前端是 PWA（可在手机浏览器里像应用一样使用的网页），电路板则用 KiCad（画电路板的软件）由代码生成。作者称前后改了三版、两次把设备从房源撤回，而且没有手写过一行代码，全部借助 AI 完成；不过他也承认，最初曾试着自己动手写。目前这篇文章只是导语，没有给出所用模型、提示词、源码、元件清单或安装步骤。

rss · Habr DIY · 11月5日 09:47

**「背景」** ESP32 是一种便宜、可编程的芯片，常被爱好者用来制作联网小设备；24 GHz 雷达则靠无线电波判断房间里有没有人、是否在动，不需要摄像头，人坐着不动时也能察觉。作者把这两类现成零件装进一个小盒子，让短租房房东能远程知道客人有没有入住、屋里声音有多吵。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openelab.io/products/gravity-mmwave-c4001-24ghz-human-presence-detection-sensor-i2c-uart">Gravity: 24 GHz mmWave Radar Human Presence Sensor for Arduino...</a></li>
<li><a href="https://shillehtek.com/blogs/news/esp32-ld2410-smart-light-presence-sensing">ESP 32 HLK-LD2410: Smart light with presence sensing | ShillehTek</a></li>

</ul>
</details>

**标签**: `#ESP32`, `#24GHz radar`, `#AI-assisted hardware`, `#KiCad`, `#home automation`

---

<a id="item-tech-news-19"></a>
### [三个按钮加一块 0.96 英寸屏：他在 ESP8266 上直接编写梯形图](https://habr.com/ru/articles/1103650/?utm_campaign=1103650&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

开发者 viordash 在 Habr 上记录了自己用 ESP8266 芯片（一种便宜、自带 Wi-Fi 的微控制器）做的一台可编程逻辑控制器（PLC，工业上用来控制机器启停和动作顺序的小型专用电脑）。它的特别之处是把编程和监控都放进了设备本身：在一块 0.96 英寸的 OLED 小屏上，只用三个按钮就能编写梯形图（一种用电路符号画控制逻辑的编程方式，工控行业常用）。设备运行时，同一张图会显示哪些触点闭合、输入端是什么值、哪些输出被打开，整个过程不需要电脑。这是一篇爱好者制作记录，提供的摘要中没有源码、元件清单或制作步骤，也没有说明是否做成可购买的产品。

rss · Habr DIY · 11月5日 08:03

**「背景」** PLC（可编程逻辑控制器）是工业现场按固定逻辑开关设备的控制盒，通常要先用电脑写好程序再下载进去。梯形图是它常用的一种图形化编程方式，画法像电路图：触点和线圈怎么连，就表示什么条件下接通什么输出。ESP8266 则是一块便宜、带 Wi-Fi 的微型可编程芯片，常被爱好者用来做自己的控制设备。

**「对使用者的实际意义」** 如果这类设备能稳定工作，直接的好处是修改控制逻辑时不必把笔记本电脑搬到机器旁：操作者可以对着三个按钮在现场改，并当场看到输入输出的变化。但按目前提供的信息，这仍是个人项目，没有成品可买；想照着做的人需要自己准备硬件并编写固件，而文章摘要里没有给出这些内容。

**标签**: `#ESP8266`, `#Ladder Diagram`, `#PLC`, `#embedded hardware`, `#DIY controller`

---

<a id="item-tech-news-20"></a>
### [小米在青年公寓试运营机器人，连续执行任务超 30 分钟](https://weibo.com/1749127163/5361796274981767) ⭐️ 5.0/10

小米已在公司青年公寓试运营一套机器人 Agent 系统（能自己规划一串步骤并执行的软件）。该系统以 Xiaomi-Robotics-1 具身基座模型（让机器人把看到的情况转成动作的模型）为底座，能自己规划并执行桌面整理、垃圾清扫、物品分类归位、房间巡检和全屋复检等任务。小米称，这次长程任务（需要连续多步完成、不能中途断掉的任务）验证连续运行超过 30 分钟、覆盖 3 个房间、包含 50 多个任务。目前只是内部试运营，没有公布技术细节、硬件清单、价格或对外可用时间。

telegram · zaihuapd · 11月5日 08:19

**「背景」** 所谓“具身基座模型”，可以理解成给机器人用的通用“大脑”：它先在大量操作数据上训练好，之后不必为每个动作单独写程序，就能听懂指令并控制身体去干活。据 IT 之家 2026 年 8 月 5 日报道，小米当时已把 Xiaomi-Robotics-1 正式开源，也就是公开模型、让外部的人也能下载使用；据新浪财经同期报道，小米称该模型用 10 万小时数据训练。此前公开的是模型本身，这次试运营则是把它接进数据采集、任务规划和执行的一整套系统，放到真实公寓里跑起来。

**「对普通用户意味着什么」** 如果你在等能整理房间的家用机器人，这次消息还不是购买信号：小米没有公布价格、硬件配置或对外可用时间，试运营也只发生在公司青年公寓。连续 30 分钟跨 3 个房间是内部验证结果，普通家庭中的稳定性和可靠性仍没有公开数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.sina.cn/tech/2026-08-05/detail-inimhawf5211207.d.html?fromtech=1&amp;vt=4">10万 小 时训练！ 小 米 具 身 基 座 模 型 Xiaomi - Robotics - 1 正式开源</a></li>
<li><a href="https://m.ithome.com/html/985985.htm">小 米 具 身 基 座 模 型 Xiaomi - Robotics - 1 正式开源 - IT之家</a></li>

</ul>
</details>

**标签**: `#小米机器人`, `#具身智能`, `#Agent系统`, `#Xiaomi-Robotics-1`, `#机器人试运营`

---

<a id="item-tech-news-21"></a>
### [华为云 11 月 15 日上线 openPangu-2.1-Pro，主打鸿蒙应用代码生成](https://m.gelonghui.com/live/2748413) ⭐️ 5.0/10

据市场消息，华为云将于 11 月 15 日在其 MaaS 平台（把厂商训练好的模型通过云服务提供给开发者调用的平台）上线 openPangu-2.1-Pro 旗舰模型，并已通过短信通知现有用户。该版本重点提升 ArkTS（华为鸿蒙原生应用使用的编程语言）的代码生成质量，还将接入智能体平台 AgentArts、代码开发工具 CodeArts 和办公产品 OfficeAce。报道没有给出价格、性能测试结果或具体调用方式，也没有说明模型是否公开权重（可下载到本地自行运行）；对于“华为云已完全停售盘古大模型”的说法，报道称这是外界误读。

telegram · zaihuapd · 11月5日 13:27

**「背景」** 盘古（Pangu）是华为的大模型系列，华为云通过 MaaS（“模型即服务”，企业通过云端接口使用模型，而不必自己部署）向客户提供这些模型。鸿蒙原生应用的开发会用到 ArkTS 语言，因此这次对代码生成的改进，最直接相关的是做鸿蒙应用开发的人。来源还提到，此前“华为云完全停售盘古大模型”的说法属于外界误读。

**「实际影响」** 对已经在通过华为云 MaaS（云端按需调用模型的服务）使用 openPangu 2.0-Pro 或 2.0-Flash 的团队来说，眼下最实际的事是准备迁移：华为云已于 11 月 2 日发布这两款模型服务的退市通知，11 月 15 日上线的 2.1-Pro 是接替选项，现有调用代码需要重新测试兼容性。做鸿蒙原生应用（用 ArkTS 语言写界面与逻辑）的开发者可以重点验证新版本的代码生成是否真的更好用，但官方没有公布价格、评测分数或开放权重情况，正式替换前最好先用自己项目的实际任务对比一次。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://t.me/linux_do_channel/553819">LINUX DO Channel – Telegram</a></li>

</ul>
</details>

**标签**: `#Huawei Cloud`, `#openPangu`, `#model release`, `#ArkTS`, `#HarmonyOS`

---

<a id="item-tech-news-22"></a>
### [agents-scaffold 发布：为多种 AI 编码代理提供项目模板](https://github.com/LeeYudok/agents-scaffold) ⭐️ 5.0/10

一个名为 agents-scaffold 的 GitHub 项目经 Telegram 频道发布，宣称能把 Claude Code、Codex 和 Antigravity 这三种 AI 编码代理（能读写代码、执行命令来完成编程任务的工具）接入同一套项目脚手架（预先搭好的目录结构和配置文件模板），并提供 Next.js、Spring Boot、Python 等现成的技术栈预设。发布内容把这件事描述为 AI 编码代理走向“集成化”的信号，但没有给出安装命令、使用示例，也没有演示或第三方验证说明它实际能做什么。原帖只留下项目地址和两个 Telegram 教程链接，因此目前能确认的只是这个项目被公开介绍过，工具本身是否可用仍未得到证实。

telegram · aipluscn · 11月5日 01:47

**「背景」** AI 编码代理（能自己读代码、改文件、执行命令来完成编程任务的 AI 助手）并不止一种，Claude Code、Codex、Antigravity 分别来自不同厂商，各自的配置文件和规则写法并不通用。agents-scaffold 这类“脚手架”（预先备好目录结构和配置模板、开发者复制后按需填写的起始项目）要解决的正是这个问题：它把这几种代理的规则、技能和常用开发栈模板放进同一套结构，并设置一道在提交代码前统一执行的检查关卡。

**「对使用者的实际影响」** 对已经在用 Claude Code 或 Codex 的人来说，这类预设脚手架能省去的是新项目开头的目录和配置搭建工作，而不是代理本身的能力提升；由于发布者没有提供安装步骤和效果示例，在用它之前应当把它当作未经检验的早期项目，先在临时目录里试跑，再决定是否用于正式代码库。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claudeers.com/agents-scaffold">agents - scaffold — Developer Tools for Claude | Claudeers</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#developer tooling`, `#GitHub project`, `#Claude Code`, `#Codex`

---

<a id="item-tech-news-23"></a>
### [桌面工具 Isle 宣称新增 AI 用量统计与代理权限管理](https://github.com/galyarderlabs/isle) ⭐️ 5.0/10

一个名为 Isle 的桌面工具在宣传帖中称，它新增了 AI 使用统计，可显示 Claude 和 ChatGPT 各套餐的用量，并加入了对 AI 代理的权限管理。Isle 的作用是把多个 AI 代理（能自行执行任务的 AI 程序，如 Claude Code、Codex、Hermes）和 MCP 服务器（一种让 AI 助手连接外部工具与数据源的通用接口）集中到一个桌面程序里，此前主打语音助手、歌词同步、通知整合等本地功能。帖子附了 GitHub 项目地址和后续教程链接，但没有给出软件版本号，也没有说明用量数据从哪里取得、以什么形式呈现，同样没有截图或可复现的证据。因此目前只能确认这是发布方的说法，社区里也没有使用者反馈可以佐证，不能当作已被验证的能力。

telegram · aipluscn · 11月5日 01:48

**「背景」** MCP（模型上下文协议）可以理解为 AI 助手连接外部工具和数据的统一插头：无论是写代码的代理还是聊天机器人，只要按这套标准接入，就能读取本地文件、调用其他软件。Isle 是第三方开发的桌面小工具，常驻在 Linux 系统的 GNOME 顶栏，把这些 AI 代理和 MCP 服务收进同一个面板里。正因为这类代理能真的动手操作电脑，谁被允许做什么、每个套餐额度用了多少，才成了需要单独查看和管理的项目。

**「实际影响」** 对使用这类桌面代理聚合工具的人来说，这项更新声称的能力意味着可以在同一个界面里看到 Claude、ChatGPT 套餐的剩余用量，并为不同代理分别设定权限。但原帖没有版本号，也没有说明用量数据从哪里读取、统计口径是什么，更没有截图或可复现的说明，所以在依赖它之前，最好先去那个 GitHub 仓库确认功能是否真的已经发布、是否支持你使用的账号类型。把账号查询和代理权限交给一个第三方桌面工具前，也值得先弄清它需要登录哪些账号、会拿到哪些权限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/galyarderlabs/isle">GitHub - galyarderlabs/isle: Independent GNOME top-bar island ...</a></li>
<li><a href="https://blog.cyberdesserts.com/ai-agent-security-risks/">AI Agent Security Risks 2026: MCP, OpenClaw &amp; Supply Chain</a></li>

</ul>
</details>

**标签**: `#MCP`, `#AI agents`, `#developer tooling`, `#usage tracking`, `#Claude Code`

---

<a id="item-tech-news-24"></a>
### [AI 代理工具库 DmitriyYukhanov/agent-plugins 发布，是 AI 工具集成化趋势的信号](https://github.com/DmitriyYukhanov/agent-plugins) ⭐️ 5.0/10

A Telegram post announcing the open-source agent-plugins collection of skills for Claude Code, Codex and Copilot, framed as a sign of AI tool consolidation but with no concrete capability, install detail or evidence provided.

telegram · aipluscn · 11月5日 03:20

**标签**: `#AI agent plugins`, `#Claude Code`, `#Codex`, `#developer tooling`, `#open-source`

---

<a id="item-tech-news-25"></a>
### [MaccyPlus 让 AI 程序用文字命令读写剪贴板历史](https://github.com/roypadina/maccyplus) ⭐️ 5.0/10

MaccyPlus 是一款 macOS 剪贴板历史工具，它提供命令行接口（CLI，用文字命令操作软件的方式），让 AI 代理（可自动执行多步任务的 AI 程序）读取和写入剪贴板历史。项目称支持规则匹配、自动执行操作、快捷键和插件，并能把内容粘贴到当前应用；这需要辅助功能权限（允许软件控制其他应用界面的系统权限）。它要求 macOS 14 Sonoma 或更高版本，兼容 Apple Silicon 和 Intel 处理器，可用命令 brew install --cask roypadina/tap/maccyplus 通过 Homebrew（macOS 常用的软件安装工具）安装。不过，现有介绍主要是趋势评论，没有 CLI 使用示例、演示，也没有证据表明 AI 代理工作流已经实际跑通。

telegram · aipluscn · 11月5日 03:20

**「背景」** 剪贴板管理器是一类常驻后台的小工具，会把你复制过的文字、链接和图片存成一份历史记录，方便之后找回。MaccyPlus 是开源 macOS 剪贴板管理器 Maccy 的分支版本（在原有代码基础上另起一版开发），在保留历史记录的同时加入规则匹配和自动执行动作，并提供命令行接口，也就是用输入文字指令代替点按钮来操作程序。这项接口之所以与 AI 有关，是因为 AI 代理（能自己调用工具、连续执行多步任务的 AI 程序）需要此类接口才能读写本机剪贴板，而不是只在对话框里回答问题。

**「实际影响」** 对使用 macOS 剪贴板工具并想让自动化程序取用历史内容的人来说，实际门槛是系统和权限：必须运行 macOS 14 Sonoma 或更高版本，让程序把内容粘贴到其他应用时还要手动授予辅助功能权限。由于来源没有展示代理读写的实际操作，安装后应先用自己的任务验证命令和权限流程，再决定是否依赖它。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://alternativeto.net/software/maccyplus/about/">MaccyPlus : Maccy clipboard manager plus rules... | AlternativeTo</a></li>

</ul>
</details>

**标签**: `#macOS clipboard tool`, `#AI agent tooling`, `#CLI integration`, `#Homebrew`, `#developer tooling`

---

<a id="item-tech-news-26"></a>
### [NVIDIA 推出 OpenShell，为 AI 代理设置独立权限](https://telegram.me/aipluscn/3603) ⭐️ 5.0/10

NVIDIA 发布了一个名为 OpenShell 的开源项目（代码公开、别人可以查看和修改），目标是给 AI 代理（能自行调用工具、执行多步任务的 AI 程序）提供安全的运行环境。按照发布信息的说法，用户可以为每个代理单独设定权限，例如允许它读取 GitHub（存放和协作编写代码的网站）上的数据，但禁止它发布内容。OpenShell 称支持 Claude Code、Codex、OpenCode 以及 GitHub Copilot 的命令行工具等编程助手，并通过改动操作系统内核（管理底层权限的核心软件）和形式化验证（用数学方法检查程序是否遵守规则）来约束代理行为。不过目前能看到的只是一则简短介绍，没有代码仓库链接、安装步骤或版本号，因此还无法确认普通用户何时能实际用上。

telegram · aipluscn · 11月5日 04:08

**「背景」** AI 编码代理（能自己读写代码、运行命令来完成编程任务的 AI 工具）通常直接跑在用户的电脑或服务器上，权限往往跟启动它的账户一样大。OpenShell 这类“安全运行环境”相当于给代理加一个受规则约束的隔离区（常叫沙箱）：代理仍可调用 Claude Code、Codex 等工具，但读写文件、联网或调用外部服务时要先经过权限检查。NVIDIA 的页面称 OpenShell 管理代理如何执行、能访问什么，以及模型请求被送到哪里；有介绍文章还提到它可选配一个独立监控组件 Sentry。

**「实际影响」** 如果这些权限控制按描述工作，使用编程代理的人可以把“能读代码、能调用 GitHub、不能发布内容”拆成不同权限，而不必把整个账号或电脑的控制权交给代理。但现阶段没有安装方式和版本信息，打算采用的人应先等代码仓库和文档公开后，再把它接入现有的开发流程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-sg/ai/openshell/">NVIDIA OpenShell | Open , Secure Runtime for AI Agents</a></li>
<li><a href="https://windowsforum.com/news/nvidia-openshell-and-sentry-what-the-open-agent-safety-platform-really-delivers.446321/">NVIDIA OpenShell and Sentry: What the Open Agent Safety Platform...</a></li>

</ul>
</details>

**标签**: `#NVIDIA OpenShell`, `#AI agent security`, `#coding agents`, `#permissions`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [中国叫停软银 54 亿美元收购 ABB 机器人业务](https://www.bloomberg.com/news/articles/2026-11-05/china-blocks-softbank-s-acquisition-of-abb-industrial-robot-unit) ⭐️ 8.0/10

ABB 于 11 月 5 日确认，中国外国投资安全审查机构通知禁止软银以约 54 亿美元收购其机器人业务在中国实施，软银布局人工智能与机器人的计划因此受阻。据报，中国监管部门担忧该业务涉及的工业数据、供应链及核心技术可能转移海外并被用于训练人工智能模型，而中国约占 ABB 机器人业务市场的 30%。

telegram · zaihuapd · 11月5日 10:44

**「背景」** 2025 年 10 月 8 日，软银与 ABB 签署确定性协议，以 53.75 亿美元企业价值收购 ABB 机器人业务；ABB 此前原计划将该业务分拆为独立上市公司。

**「影响」** 此次叫停直接限制 ABB 机器人业务约占 30% 的中国市场，也使软银原计划将工业机器人硬件与其人工智能能力整合的路径在中国境内无法实施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://group.softbank/en/news/press/20251008">Acquisition of ABB Ltd’s Robotics Business | SoftBank Group Corp.</a></li>
<li><a href="https://www.abb.com/global/en/news/129685/abb-to-divest-robotics-division-to-softbank-group">ABB to divest Robotics division to SoftBank Group</a></li>

</ul>
</details>

**标签**: `#China FDI review`, `#SoftBank`, `#ABB robotics`, `#cross-border M&amp;A`, `#AI and robotics`

---

<a id="item-finance-news-2"></a>
### [任天堂 Switch 2 第二财季销量 267 万台，同比下滑 41%](https://mp.weixin.qq.com/s/XTw5DXy2CvqFSs4WYx73Xg) ⭐️ 7.0/10

任天堂公布，截至 9 月 30 日的第二财季 Switch 2 主机销量为 267 万台，同比下滑 41%；当季营收 4482 亿日元、净利润 735 亿日元，均低于市场预期，公司仍维持截至 2027 年 3 月的财年 1650 万台销量目标。

telegram · zaihuapd · 11月5日 14:12

**「背景」** 作为对比，Switch 2 在 2025 年同期售出 454 万台，本季度 267 万台同比下滑 41%，公司仍维持截至 2027 年 3 月的财年 1650 万台目标。

**「影响」** 存储芯片涨价带来的成本压力已通过上调零售价转嫁给玩家：美国市场 Switch 2 售价自 9 月 1 日起由 449.99 美元升至 499.99 美元，日本市场则上调 1 万日元；这意味着有意购机的家庭需要多付出这笔额外支出。（工具结果）

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tech-insider.org/nintendo-q2-net-profit-falls-29-percent-switch-2-slows-2026/">Nintendo Net Profit Falls 29% as Switch 2 Slows [2026]</a></li>
<li><a href="https://shattered.io/switch-2-2-67-million-q2-fy27-16-5-million-target-h2-math-2026/">Switch 2 Sells 2.67M in Q2 FY27: H2 Math [2026]</a></li>
<li><a href="https://www.cnbc.com/2026/05/08/nintendo-switch-2-price-hike-sales-fall-memory-crunch.html">Nintendo hikes Switch 2 prices and expects console sales to ...</a></li>
<li><a href="https://bitsfrombytes.com/nintendo-switch-2-price-increase/">Nintendo Switch 2 Price Increase: Every Country, Every Date ...</a></li>

</ul>
</details>

**标签**: `#Nintendo`, `#Switch 2`, `#earnings miss`, `#console sales`, `#memory chip costs`

---