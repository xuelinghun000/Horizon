---
layout: default
title: "Horizon Summary: 2026-10-26 (ZH)"
date: 2026-10-26
lang: zh
---

> 从 90 条内容中筛选出 14 条重要资讯。

---

**科技新闻**
1. [一句提示词让编程助手优先相信代码而非过期文档](#item-tech-news-1) ⭐️ 7.0/10
2. [Claude 付款页新增中国大陆及港澳台选项，可绑银联卡](#item-tech-news-2) ⭐️ 7.0/10
3. [用 Opencode 搭建不依赖外部服务的本地编程助手实验](#item-tech-news-3) ⭐️ 6.0/10
4. [俄罗斯企业如何凭发票购买 Claude 和 GPT](#item-tech-news-4) ⭐️ 6.0/10
5. [开发者自制安卓客户端，用手机远程操控电脑上的 DeepSeek 智能体](#item-tech-news-5) ⭐️ 6.0/10
6. [new-api v1.0.0-rc.47 调整渠道选择与缓存计费](#item-tech-news-6) ⭐️ 5.0/10
7. [分析文章解释 OpenAI 与 Anthropic 的 AI 接口为何降价最多 80%](#item-tech-news-7) ⭐️ 5.0/10
8. [Deki Engine 推出面向 ESP32 的开源 2D 游戏编辑器](#item-tech-news-8) ⭐️ 5.0/10
9. [开源宠物项圈 LIA：用 Meshtastic 免订阅定位](#item-tech-news-9) ⭐️ 5.0/10
10. [用卡尔曼滤波筛选 AI 代码修改：小规模实验未发现优势](#item-tech-news-10) ⭐️ 5.0/10
11. [用户警告基元律动中转站：缓存失效数小时花掉 70 元](#item-tech-news-11) ⭐️ 5.0/10
12. [开源项目 MailFlare：自建收件箱自动提取验证码，按邮箱分权限](#item-tech-news-12) ⭐️ 5.0/10
13. [Anthropic 被曝悄悄限制 Claude Opus 5.5 的逆向工程能力](#item-tech-news-13) ⭐️ 5.0/10

**财经新闻**
1. [2025 年全国总人口减少 339 万](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [一句提示词让编程助手优先相信代码而非过期文档](https://linux.do/u/czm) ⭐️ 7.0/10

10 月 26 日，linux.do 论坛用户 czm 分享了一句可以写进 CLAUDE.md 或 AGENTS.md 的提示词。这两个文件放在代码仓库里，是专门给 AI 编程助手（能自己读代码、改文件、执行命令的 AI 工具，例如 Claude Code）看的项目说明，相当于给新同事的项目须知。这句提示词要求助手在文档与现有代码冲突时以代码为准，并在最终回复里逐条列出发现的不一致；帖子给出了中英文两个版本，中文版是“当仓库的文档与现有代码不一致时，请遵循现有代码所用的约定，并在最终回复中指出你发现的文档与代码之间的每一处不一致。”发帖者称这来自一篇 arXiv 论文（arXiv 是公开论文预印本库，上面的文章通常未经过同行评审），能“大幅提升”代码被遵循的比例，但帖子里没有给出具体测试数字、样本量或复现方法，实际效果需要使用者自己验证。

telegram · linuxdo\_tg · 10月26日 02:11

**「背景」** CLAUDE.md 或 AGENTS.md 是放在代码仓库里的说明文件，编程智能体（能自己读写代码、执行命令的 AI 助手）开始工作时会自动读取，作用类似给新同事看的项目须知。代码不断修改后，这些说明可能过期；智能体如果仍照旧说明办，就会和仓库里的实际写法冲突。那句提示词就是让它遇到冲突时以现有代码为准，并把不一致之处列出来。

**「对使用者的实际影响」** 对日常用 Claude Code、Codex CLI 这类工具写代码的人，这句话可以直接复制进项目根目录的 CLAUDE.md 或 AGENTS.md，不需要改代码，也不需要升级任何软件。代价是助手每次回复会多出一段“文档与代码不一致”的清单，回复会变长；而且它只在文档确实与代码冲突时才会改变助手的行为，文档本身是最新的情况下基本看不出差别。

**标签**: `#coding-agents`, `#prompt-engineering`, `#AGENTS.md`, `#Claude Code`, `#arXiv`

---

<a id="item-tech-news-2"></a>
### [Claude 付款页新增中国大陆及港澳台选项，可绑银联卡](https://claude.ai/upgrade/pro?interval=monthly) ⭐️ 7.0/10

Claude 的付费升级页面（订阅 Claude Pro 时用来付款的网页）近日新增了中国大陆、香港、澳门和台湾的选项，一位编辑测试后称可以成功绑定银联卡（中国主要的银行卡网络）。这一说法来自一个 Telegram 频道，Anthropic 官方尚未确认，也没有说明这些选项是否对所有用户都出现。能付款并不等于能使用：Anthropic 帮助中心仍要求用户位于其支持的国家或地区才能使用 Claude，这条限制没有改变。

telegram · zaihuapd · 10月26日 01:03

**「背景」** Claude 的付费订阅（Pro）一直只在 Anthropic 帮助中心列出的“支持地区”内销售，中国大陆不在名单上，所以“能不能付钱”和“能不能使用”本来就是两套分开的限制。据媒体报道，Anthropic 在 2026 年 10 月上旬刚给 Claude 加上中文界面选项，但当时仍明确屏蔽中国大陆用户。这次付款页出现中国大陆与港澳台选项，改变的是结账时可选的国家/地区，而不是服务条款里的可用范围。

**「对想订阅的人意味着什么」** 对想订阅 Claude Pro 的用户来说，实际变化只发生在付款这一步：结账时能选中国大陆、香港、澳门或台湾地区，并据该编辑的测试可以绑定银联卡完成付款（银联是中国大陆最普及的银行卡网络，据 Adyen 介绍全球流通卡量超过 70 亿张）。但付款成功不等于账号就能正常使用——Anthropic 帮助中心仍要求用户身处其支持地区，所以先付钱后遇到访问限制的风险依然存在，订阅前最好先确认自己的网络环境和账号状态是否符合官方支持地区的要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.scmp.com/tech/big-tech/article/3370154/us-ai-firm-anthropic-enables-chinese-language-options-claude-chatbot">Anthropic’s Claude AI gets Chinese-language options settings</a></li>
<li><a href="https://www.adyen.com/zh_CN/payment-methods/unionpay">UnionPay 支 付 方式- UnionPay 支 付 - Adyen</a></li>

</ul>
</details>

**标签**: `#claude`, `#subscriptions`, `#payments`, `#regional-availability`, `#access-routes`

---

<a id="item-tech-news-3"></a>
### [用 Opencode 搭建不依赖外部服务的本地编程助手实验](https://habr.com/ru/articles/1099230/?utm_campaign=1099230&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一位作者在 Habr 上发文，介绍他从 2026 年 4 月底到 10 月底做的一项实验：用开源终端编程工具 Opencode 搭一个不依赖外部服务的编程助手，看它在只有 12GB 显存的普通显卡上能做什么。所谓终端编程助手，是指在命令行里运行、能自己读写代码文件并执行命令的 AI 工具，Claude Code、Codex 都属于这一类；Opencode 的不同之处是开源，并且可以换用不同厂家的模型。作者设定的测试对象是一个 80 亿参数、上下文 32K 的本地模型——参数量大致代表模型规模，32K 上下文指它一次能读入的文本上限，约合两三万字。他选工具的标准是：不绑定特定模型、开源、代码容易改，方便反复试新想法。需要说明的是，目前可见的正文只有实验设想和选型理由，没有给出模型名称、具体配置、速度或效果数据，也没有安装步骤，所以这还不能算一个可以照做的方案，实验是否成功尚不清楚。

rss · Habr AI · 10月25日 19:30

**「背景」** Opencode 是一个开源、可在终端（用文字命令操作的界面）里运行的 AI 编程助手，它不绑定某一家模型，既能接 Claude、OpenAI、Google 的服务，也能接本地模型。这类终端代理能读代码、执行命令和改文件，替人完成一部分编程工作；这篇文章想弄清的是，不订阅外部服务、只靠本地硬件，是否也能得到够用的效果。它设定的条件是 8B（80 亿参数）的模型、32K（约 3.2 万个词元，即模型一次能参考的文本量）的上下文，以及一块 12GB 显存的显卡；参数和上下文越大，通常越占显存和计算资源。

**「对使用者的实际影响」** 如果你正考虑用本地模型替代按月订阅的编程助手，现在还不能据此行动：文章没有说明用了哪个模型、怎么压缩到 12GB 显存里运行、生成代码的速度和可用程度如何。在作者补上这些细节之前，把它当作一个待验证的设想更稳妥。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opencode.ai/">OpenCode | The open source AI coding agent</a></li>
<li><a href="https://www.producthunt.com/products/opencode">opencode: Your terminal&#x27;s AI agent, with any model you want ...</a></li>

</ul>
</details>

**标签**: `#terminal agents`, `#Opencode`, `#local LLMs`, `#self-hosting`, `#coding agents`

---

<a id="item-tech-news-4"></a>
### [俄罗斯企业如何凭发票购买 Claude 和 GPT](https://habr.com/ru/articles/1099218/?utm_campaign=1099218&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

2026 年 10 月 25 日，俄罗斯技术社区 Habr 发表了一篇指南，讲解俄罗斯公司如何以企业名义、凭发票（счёт，供应商开具的付款单据）购买 Claude 和 GPT，而不是让员工用别人的银行卡去买个人订阅。文章点出这条路径上三个容易被忽略的环节：Anthropic 一条关于「50% 所有权」的规定、向外国供应商采购时由买方代扣代缴的增值税（即买方充当「税务代理人」），以及中介把美元汇率藏进报价里的加价。作者的主线是教企业把这些都算进去，得出「真实的 token（模型处理文字时的计费单位）价格」。不过可见的导语没有给出任何具体金额、税率或费率，文中数字无法在此核实。

rss · Habr AI · 10月25日 18:30

**「背景」** 这篇指南针对的是一个具体处境：俄罗斯公司无法像普通用户那样，用公司银行卡直接为员工购买 Claude 或 GPT 的个人订阅——挂在别人卡上的个人订阅既不能记作公司支出，也开不出入账所需的凭证。于是企业采购改走中间商开票的路径，而账单价格里同时包含中间商按自家汇率折算的加价，以及由采购方代扣代缴的增值税（VAT，购买境外服务时由买方替境外卖方上缴的税）。此外，Anthropic 还有一条关于 50% 持股比例的规定，它决定了哪些公司有资格合规使用其服务。

**「对企业的实际影响」** 对在俄罗斯运营、想让员工合规使用 Claude 或 GPT 的公司来说，需要比较的不是官网标价，而是中介报价里含的汇率加价、再加上代扣增值税之后的单价；指南同时把可用于入账的凭证（закрывающие документы）列为公司采购的必要一环，而不只是把钱付出去。由于文章摘要没有给出可套用的费率，企业仍需向具体供应商索取报价单和单据样本，再自行核算。

**标签**: `#Claude`, `#GPT`, `#pricing`, `#Russia`, `#access routes`

---

<a id="item-tech-news-5"></a>
### [开发者自制安卓客户端，用手机远程操控电脑上的 DeepSeek 智能体](https://habr.com/ru/articles/1099110/?utm_campaign=1099110&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一位开发者在 Habr 上发文，介绍自己为 DeepSeek Harness 写的一个安卓客户端，让手机能远程指挥运行在个人电脑上的 DeepSeek 智能体（agent，能代替人读写文件、执行命令的 AI 程序），整个过程不经过云端服务器，也不使用谷歌的 FCM 推送服务（Firebase Cloud Messaging，安卓应用接收云端消息的常用通道）。按文中描述，客户端没有采用内嵌网页（WebView）的做法，而是在电脑端程序里装了一个插件；手机与电脑靠扫二维码配对，并启用了证书锁定（只信任事先写死的那一张证书，防止有人冒充电脑端）；此外还有一个“回执日志”，手机要等到电脑确认收到才算发送成功，避免网络不稳时把同一条命令重复执行。文章目前只是概述，没有给出源码、安装步骤，也没有说明是否已有人实际跑通。

rss · Habr AI · 10月25日 13:48

**「背景：这个“Harness”是什么」** DeepSeek Harness（简称 dsh）是 DeepSeek 开源的一套“智能体运行框架”：它跑在用户自己的电脑上，把大模型的回答变成实际动作，比如读写文件、执行命令，而且所有能力都以插件形式加装。据其官网和 GitHub 项目页介绍，它已面向全球开放公开预览并以 MIT 许可证开源。手机想远程指挥这样一个电脑上的程序，通常要么经过一台云端服务器中转，要么依赖谷歌的 FCM 推送（Firebase Cloud Messaging，安卓系统用来唤醒 App 的官方消息通道）；这篇文章介绍的客户端正是把这两样都去掉了。

**「对使用者的实际影响」** 对日常使用编程智能体的人来说，这个项目指向的是一种不依赖云端的手机遥控方式：电脑上的智能体继续运行，人离开工位后可以用手机查看进度、下达指令。但文章没有放出代码或安装包，现在还没法照着搭建；想尝试的人只能等作者补充材料，或者自己按同样的思路实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepseekagent.io/guides/deepseek-harness">DeepSeek Harness (dsh): Official DeepSeek Agent Setup Guide</a></li>
<li><a href="https://github.com/deepseek-ai/deepseek-harness">DeepSeek Harness - GitHub</a></li>
<li><a href="https://www.deepseek.com/en/harness/">DeepSeek Harness | Explore the limits of intelligence</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#coding agents`, `#Android client`, `#remote access`, `#developer tooling`

---

<a id="item-tech-news-6"></a>
### [new-api v1.0.0-rc.47 调整渠道选择与缓存计费](https://github.com/QuantumNous/new-api/releases/tag/v1.0.0-rc.47) ⭐️ 5.0/10

自建 AI 接口中转工具 new-api 发布 v1.0.0-rc.47，这是 1.0 正式版前的候选版本。在图片、视频和 Responses 接口（OpenAI 的一种模型调用接口）上，普通渠道（直接连接模型服务的上游线路）与任务插件（处理异步任务的扩展）现在按优先级和权重共同选择渠道，不再一律把请求发给插件；若模型价格仍只按任务插件填写，普通渠道会报价格错误且不扣额度，需要单独设置普通渠道价格。OpenAI 的 12 小时提示缓存（让模型重复使用此前读过的长文本、减少重复计算）新增单独计价，按输入价格的 2.5 倍收费，而此前按 30 分钟缓存价格计费。视频任务超过 24 小时就被退款的问题已修复，默认改为等待 72 小时，管理员自行设置过 TASK\_TIMEOUT\_MINUTES（任务超时分钟数）的仍按原值。

github · Calcium-Ion · 10月25日 09:04

**「背景」** new-api 是一个可自行部署的 API 中转网关（把用户请求转发给不同 AI 服务商、并统一记账的软件），管理员会把每个上游账号或线路配置成一个“渠道”。它同时支持“任务插件”，用来处理图片、视频等耗时任务。这里的“提示缓存”指服务商把重复的提示内容暂存起来供后续请求复用，缓存保留时长不同，写入费用也不同。

**「实际影响」** 对自建 new-api 的管理员来说，升级后应先检查同时由普通渠道和任务插件提供的模型价格：只写了插件价格时，普通渠道会返回价格错误、不扣额度，需要补设普通渠道价格才能正常结算。使用 OpenAI 12 小时缓存的请求会按更高单价结算，成本高于此前的 30 分钟缓存价；视频任务未完成时，退款等待时间从 24 小时延长到 72 小时。

**标签**: `#api-relay`, `#new-api`, `#pricing`, `#openai`, `#self-hosted`

---

<a id="item-tech-news-7"></a>
### [分析文章解释 OpenAI 与 Anthropic 的 AI 接口为何降价最多 80%](https://minimaxir.com/2026/10/cheap-llms/) ⭐️ 5.0/10

过去几个月，OpenAI 和 Anthropic 的大语言模型 API（让外部程序按使用量调用模型的接口，通常按 token 计费，token 可粗略理解为字词片段）价格最多下降了 80%，受影响的是按量付费调用这些接口的开发者与公司。一篇在 Hacker News 上被讨论的分析文章试图解释这轮降价，而不是宣布新的价格调整。围绕文章的讨论把原因归结为竞争（尤其是来自中国的开放权重模型，即参数公开、可自行下载运行的模型）、推理（模型回答问题时的计算过程）成本下降，以及 GPU（图形处理器，运行 AI 模型的主要芯片）算力闲置的压力；也有人认为推动监管才是重点。评论中引用的具体数字，例如 DeepSeek 每块 GPU 每小时 38 美元的收入，来自网友而非文章核实，应谨慎看待。

hackernews · minimaxir · 10月25日 21:11 · [社区讨论](https://news.ycombinator.com/item?id=50236102)

**「背景」** 大模型 API（应用程序接口，这里指按用量租用模型回答能力的服务）通常按“词元”计费：词元是模型处理文字的最小单位，大致相当于一个词或半个汉字，所以单价下调会直接反映在每百万词元的账单上。这轮降价不是突然发生的：据 8 月的报道，OpenAI 在同一周下调了两款模型的价格，Anthropic 悄悄取消了原定的涨价，而中国的 DeepSeek 反而把 API 价格最高上调了 1,100%（tool-2-1）。同期分析认为，中国模型已把日常任务的调用成本压得很低，使“前沿模型溢价”越来越难站得住脚（tool-2-3）。

**「实际影响」** 对用这些接口做产品的团队来说，同样的调用量账单可能明显下降，原本因为成本而搁置的功能变得更可行。但选型时不能只看单价：还要确认模型能力是否够用、服务条款是否允许你的用法，以及数据保留政策是否满足要求。

**「社区讨论」** 评论者中，有人把降价归因于竞争，称自己转用中国模型 Kimi 和 GLM 后成本更低、被“网络安全”拦截更少；也有人认为 OpenAI 和 Anthropic 推动监管是为了把中国开放模型挡在市场外。另有评论引用未经证实的 DeepSeek 每 GPU 收入数字，质疑降价是否可持续，并担心零数据保留（服务商不保存用户对话）等政策被削弱。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.thetechwatcher.com/2026/08/ai-price-war-openai-anthropic-deepseek-zai-2026.html">AI Price War 2026: OpenAI, Anthropic, DeepSeek and Z.ai Are ...</a></li>
<li><a href="https://mlq.ai/news/openai-anthropic-cut-ai-prices-as-chinese-models-widen-the-cost-gap/">OpenAI, Anthropic cut AI prices as Chinese models widen the ...</a></li>

</ul>
</details>

**标签**: `#llm-pricing`, `#openai`, `#anthropic`, `#api-costs`, `#industry-analysis`

---

<a id="item-tech-news-8"></a>
### [Deki Engine 推出面向 ESP32 的开源 2D 游戏编辑器](https://www.cnx-software.com/2026/10/25/deki-engine-esp32-gets-an-open-source-unity-style-editor-and-c-2d-game-engine/) ⭐️ 5.0/10

开源项目 Deki Engine 发布了面向 ESP32 微控制器（一类常用于小型电子设备的低功耗芯片）的 C++（一种编程语言）2D 游戏引擎，以及类似 Unity 的可视化编辑器（通过界面搭建场景，而不是只写代码）。编辑器可在 Windows 和 Linux 上运行，代码以 Apache 2.0 许可证发布在 GitHub 上。它目前针对 LilyGO T-Deck Plus、T-Display S3 AMOLED 等开发板优化，并计划支持 Elecrow CrowPanel Advanced 7 英寸 ESP32-P4；开发者也能在电脑上通过 SDL3（一套处理图形和输入的多媒体库）运行项目。项目方称在 ESP32-S3 上可达到每秒 60 帧，但所给文章内容不完整，除功能列表外的性能和兼容性说法尚未得到独立验证。

rss · CNX Software · 10月25日 03:00

**「背景」** ESP32 是乐鑫（Espressif）推出的低成本微控制器芯片，常见于各种电子 DIY 开发板，内存和算力都远小于手机或电脑。Unity 则是常见的游戏制作软件，开发者把图片、文字等素材拖进可视化界面拼出场景，不必从零写代码。Deki Engine 要做的，就是把这种“拖拽拼场景”的做法搬到这类小芯片上，让没有嵌入式开发经验的人也能给开发板做小游戏。

**「实际影响」** 对想给掌上设备做小游戏的爱好者来说，实际变化是可以在电脑上搭好场景、在编辑器里选择开发板并直接烧录，而不必从零处理屏幕、触摸和按键驱动。不过当前适配集中在少数 LilyGO 开发板，换用其他 ESP32 板子前需要确认对应的硬件包是否支持。

**标签**: `#ESP32`, `#game engine`, `#open source`, `#embedded development`, `#microcontroller`

---

<a id="item-tech-news-9"></a>
### [开源宠物项圈 LIA：用 Meshtastic 免订阅定位](https://hackaday.com/2026/10/25/meshtastic-pet-tracking/) ⭐️ 5.0/10

Hackaday 介绍了一个名为 LIA 的开源宠物追踪项圈，由 Jon G Aguado 设计。它基于 Meshtastic（一个用 LoRa 低功耗无线电让设备互相转发短消息的开源网络）和一块自制电路板（PCB，即印有线路的裸板），目的是绕开多数商用宠物追踪器必须按月付费订阅、或依赖运营商网络才能工作的限制。报道提到项圈外壳上印有狗形图案和“LIA”字样，图中还能看到 GPS 天线和 LoRa 无线电模块。不过目前公开的这段内容在列出零件清单、固件下载地址和组装步骤之前就截断了，因此价格、续航和实际定位距离都还没有确证信息。

rss · Hackaday · 10月25日 11:00

**「背景」** Meshtastic 是一套开源方案：它让多台低功耗、远距离的 LoRa 无线电（一种不依赖手机信号塔、可在数公里内收发数据的无线方式）互相转发消息，组成一张自建网络。LIA 就建在这套方案之上，项目主页和 GitHub 说明它不依赖手机信号、云端服务或月费（tool-2-1、tool-2-2）；Seeed Studio 的报道还提到，它参加了 2026 年的 Meshtastic Build-Off 设计比赛（tool-2-3）。

**「对想动手的人意味着什么」** 对愿意自己焊接和调试的爱好者来说，这类方案省掉的是长期订阅费，换来的是自己采购零件、刷固件并搭建 LoRa 接收端的工作量；由于报道尚未给出零件清单和固件链接，现在还不能照着做出一只可用的项圈，需要等作者放出完整资料。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jgaguado.github.io/LIA/">LIA — Off-grid. On track.</a></li>
<li><a href="https://github.com/JGAguado/LIA">GitHub - JGAguado/LIA: Low-power pet tracking platform built ...</a></li>
<li><a href="https://www.seeedstudio.com/blog/2026/08/19/lia-an-open-meshtastic-gps-tracker-built-for-off-grid-use/">LIA Meshtastic GPS Tracker: Open Off-Grid Design - Seeed Studio</a></li>

</ul>
</details>

**标签**: `#meshtastic`, `#lora`, `#open-source-hardware`, `#esp32`, `#pet-tracker`

---

<a id="item-tech-news-10"></a>
### [用卡尔曼滤波筛选 AI 代码修改：小规模实验未发现优势](https://habr.com/ru/articles/1098756/?utm_campaign=1098756&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位 Habr 作者发表了一项可复现实验，检验卡尔曼滤波（一种从带噪声的测量中估计真实状态的数学方法，常用于导航和信号处理）能否帮助判断该接受哪一条 AI 代码修改。实验采用「作者—批评者」循环：一个 AI 负责写代码修改，另一个 AI 负责评审，作者比较了四种「接受哪条修改」的规则。试点共收集 720 条模型回复，其中 144 条用于校准、576 条用于在六个 Python 代码优化任务上评估。结果在模拟环境中，卡尔曼滤波确实改善了状态估计并让修改幅度变小；但在真实试点中，四种规则全部达到了预设的成功标准，没有测出卡尔曼滤波的额外优势。作者随文公开了笔记本、源码、结果、图表和局限说明，以及一个可通过 OpenAI API（让程序调用模型的接口）自行运行同类实验的工具包，包含校准、暂停和续跑功能。

rss · Habr AI · 10月25日 08:56

**「背景」** 卡尔曼滤波是一种把“预测”和“有误差的测量”按各自可信程度加权合并的算法，常见于导航和信号处理。文中的“作者—批评者循环”是指一个 AI 先修改代码，另一个 AI 负责审阅并提意见，再由规则决定是否接受这次修改。作者先在小规模模拟中看到这种滤波能减小修改幅度，随后用 720 次模型回答的真实试验，检验它是否比更简单的接受规则更有用。

**「对实际使用意味着什么」** 如果你正在搭建「一个 AI 写、另一个 AI 审」的代码流程，这项试点的直接提示是：不必急着引入卡尔曼滤波这类复杂判定，更简单的接受规则在同样条件下表现相当。想自己验证的人可以直接用作者放出的工具包，换成自己的任务和模型重跑，但要注意结论的边界——这只是一次试点、六个任务，阴性结果不等于证明该方法在任何场景都无用。

**标签**: `#AI coding agents`, `#author-critic loop`, `#Kalman filter`, `#reproducible experiment`, `#OpenAI API`

---

<a id="item-tech-news-11"></a>
### [用户警告基元律动中转站：缓存失效数小时花掉 70 元](https://linux.do/u/att1008) ⭐️ 5.0/10

10 月 26 日，linux.do 论坛用户 att1008 发帖，提醒大家慎重选择 AI 接口中转服务“基元律动”（中转站指转卖各家 AI 模型调用权限的中间商，用户通过它间接使用模型）。他说自己趁“充多少送多少”的活动充值 200 元，当时该平台只提供 DeepSeek 官方线路，现在又增加了火山、无问等来源，但他实测“基本路由不到 DeepSeek 官方”。他点出两个问题：一是推理等级（控制模型“思考”多久的档位）不管怎么选都不生效；二是 Anthropic 格式接口的提示缓存（把重复的长段文字存下来复用，避免每次按全价重新计费）不生效，几个小时就花掉约 70 元。他还说官网只有一个第三方反馈页面和客服邮箱，找不到人工客服，也没有退款渠道。以上都是这一位用户的说法，帖中没有给出可复现的测试步骤或配置细节。

telegram · linuxdo\_tg · 10月26日 02:07

**「背景」** API 中转站（转卖大模型调用额度的第三方服务）自己不训练模型，而是把用户发来的请求转给 DeepSeek 等厂商，靠加价或“充多少送多少”这类充值活动吸引人。DeepSeek 是国内的大模型厂商，官方接口按处理的文字量计费，单位是 token（可粗略理解为字词片段）；提示缓存（prompt caching）能让重复的开头内容不必重新计费，长对话里能省下不少钱。发帖人正是冲着充值赠送活动一次充了 200 元，后来发现服务商列表里多了火山、无问等选项，实际请求很少落到 DeepSeek 官方。

**「对使用者的实际影响」** 如果你在用这类中转站跑长文本任务，账单可能按“每次全文重新计费”而不是缓存后的低价计算，费用会在几小时内明显超出预期。比较稳妥的做法是先小额充值试跑，确认缓存和推理档位是否真的生效，再决定是否大额充值，并保留充值记录以便日后追讨。

**标签**: `#API relay`, `#DeepSeek`, `#prompt caching`, `#provider warning`, `#cost`

---

<a id="item-tech-news-12"></a>
### [开源项目 MailFlare：自建收件箱自动提取验证码，按邮箱分权限](https://linux.do/u/nayumi.DEV) ⭐️ 5.0/10

开发者 nayumi.DEV 在 LINUX DO 社区发布了一个名为 MailFlare 的开源项目：把某个域名下所有地址收到的邮件都汇总进一个自建收件箱，网页界面刻意做得像 Gmail，并会尽量从邮件标题和正文里自动提取验证码（OTP，一次性验证码），复制即可使用。项目支持多用户按邮箱分权限，区分拥有者、只读共享和管理员覆盖，不是所有人共用一个收件箱；数据库可选 SQLite 或 Postgres，文档有中英文等多语言版本。它依靠 Cloudflare 的邮件路由服务接收邮件，后端用 Python 的 FastAPI 框架搭建；如果想从某个邮箱直接回信，需要开通 Cloudflare 的付费 Worker 外发功能。这是作者的自荐帖，没有给出性能测试、使用人数或与其他方案的对比数据。

telegram · linuxdo\_tg · 10月26日 02:10

**「背景」** 所谓 catch-all（全收）邮箱，是指把一个域名设成“任何地址寄来的信都收下”：比如 shop@你的域名、news@你的域名，都会落进同一个收件箱。很多人在注册各种服务时用不同地址，验证码就散落在各处，甚至混进私人主邮箱；自建这样一套收件箱，可以把这些临时地址和私人邮箱分开。

**「实际影响」** 对经常注册试用服务、需要反复接验证码的人来说，这套东西能让每个网站用不同地址、验证码集中在一处并自动挑出来。代价是门槛：你需要拥有一个域名并交给 Cloudflare 托管，还要有一台能长期运行 Python 服务的机器，想直接回信则要额外为 Cloudflare 的付费功能掏钱。项目刚开源，目前没有第三方测试或长期使用反馈可参考。

**标签**: `#self-hosted`, `#open-source`, `#email`, `#OTP`, `#Cloudflare`

---

<a id="item-tech-news-13"></a>
### [Anthropic 被曝悄悄限制 Claude Opus 5.5 的逆向工程能力](https://linux.do/u/BunnHack) ⭐️ 5.0/10

10 月 21 日 Anthropic 对多款 Claude 产品推送更新后，Reddit 的 r/Claude 社区在同一天出现帖子称，9 月 22 日发布的 Claude Opus 5.5 在协助逆向工程（把现成软件拆开、弄清它如何运作）时会被中途打断。多名用户描述，当要求它分析受版权保护的软件时，模型内置的安全护栏（内容过滤规则）会在回答生成到一半时触发，回复里出现“安全校验中途终止了本次回答”之类的提示，换一种说法重问也拿不到相应内容。Anthropic 没有发布新版本，也没有任何官方说明；帖子里也有少数用户认为，用 Claude 做这类工作本来就时好时坏，“分类器本身就很敏感，能不能成功全看运气”。IT 之家指出，Anthropic 过去确实有过不写进更新说明就调整模型行为的先例，所以这次改动“有不小概率”存在，但目前仍属未经证实的用户反馈。

telegram · linuxdo\_tg · 10月26日 02:13

**「背景」** Claude Opus 5.5 是 Anthropic 在 9 月 22 日发布的旗舰模型，据 9to5Mac 当时的报道，同系列的 Sonnet 5.5 和 Haiku 5.5 也计划在随后几周推出。发布之后，不少爱好者用它把老游戏拆开、改写再重新编译成能在浏览器里运行的版本，这种用日常语言描述需求、让模型代写代码的做法被称为“氛围编码”。这里的逆向工程指拆解已有的软件或固件、弄清其内部构造；模型厂商通常会在输出环节设置“安全护栏”，一旦判定内容涉及受版权保护的代码或固件，就可能中途掐断回答。

**「对使用者的实际影响」** 对平时用 Claude 拆解或改写现成软件的人来说，具体变化是回答可能在写到一半时被切断，而且按帖子的说法，换个问法也绕不过去。如果你手头有这类任务，最好同时准备本地工具或其他模型作为备选；由于 Anthropic 未作确认，也无法判断这是永久限制还是短期波动，遇到中断时不宜直接把它当成整个模型的能力上限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://9to5mac.com/2026/09/22/anthropic-upgrades-claude-with-new-opus-5-5-model-details-here/">Anthropic upgrades Claude with new Opus 5 . 5 model... - 9to5Mac</a></li>

</ul>
</details>

**标签**: `#Claude Opus 5.5`, `#Anthropic`, `#model capability change`, `#reverse engineering`, `#silent restriction`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [2025 年全国总人口减少 339 万](https://weibo.com/1796087453/5357878513767954) ⭐️ 7.0/10

微博转引《中国统计年鉴 2026》的数据显示，2025 年末全国总人口为 140489 万人，比 2024 年末减少 339 万人，已接近 14 亿关口；全年出生 792 万人，自然增长率为-2.41‰。

telegram · zaihuapd · 10月25日 12:02

**「背景」** 中国国家统计局数据显示，2025 年死亡人口为 1131 万，出生人口为 792 万；财新报道称总和生育率（平均每名妇女一生生育子女数）约 0.96，远低于 2.1 的更替水平。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.caixinglobal.com/2026-01-19/chinas-population-decline-accelerates-as-births-hit-modern-era-low-in-2025-102405520.html">China ’s Population Decline Accelerates as Births Hit... - Caixin Global</a></li>
<li><a href="https://www.globaltimes.cn/page/202610/1372925.shtml">Nine provincial-level regions in China post birth rates ... - Global Times</a></li>

</ul>
</details>

**标签**: `#China demographics`, `#population decline`, `#birth rate`, `#macroeconomy`, `#statistical data`

---