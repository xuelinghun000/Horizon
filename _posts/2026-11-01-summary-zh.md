---
layout: default
title: "Horizon Summary: 2026-11-01 (ZH)"
date: 2026-11-01
lang: zh
---

> 从 77 条内容中筛选出 14 条重要资讯。

---

**科技新闻**
1. [ChatGPT 与 Codex 将从 12 月起共享用量额度](#item-tech-news-1) ⭐️ 8.0/10
2. [Memdoor 发布让五个开源模型组队写代码的工作流，宣称胜过更强的模型](#item-tech-news-2) ⭐️ 7.0/10
3. [创作者公布 24 秒竖屏动画的多模型制作流程与费用表](#item-tech-news-3) ⭐️ 7.0/10
4. [开发者发布 mcp-linter：用 34 条规则检查 MCP 服务器](#item-tech-news-4) ⭐️ 7.0/10
5. [开源工具「栖言」：为 Codex 桌面端加账号切换和用量统计](#item-tech-news-5) ⭐️ 7.0/10
6. [Parameter Labs 披露已修复的 ChatGPT 账号接管漏洞](#item-tech-news-6) ⭐️ 6.0/10
7. [开源模型路由器 FAIRouter 的 C\# 版上架 NuGet](#item-tech-news-7) ⭐️ 6.0/10
8. [网传 Anthropic 封停涉及训练更大模型的账号，政策未获证实](#item-tech-news-8) ⭐️ 5.0/10
9. [Datasette Agent 插件更新：启动时不必再指定默认模型](#item-tech-news-9) ⭐️ 5.0/10
10. [开发者尝试不用 IDE、只让 Qwen 与 Qwen Coder 写 NTFS 数据流扫描器](#item-tech-news-10) ⭐️ 5.0/10
11. [TBook 阅读格式更新：手机版、桌面阅读器、离线词典与第二版格式](#item-tech-news-11) ⭐️ 5.0/10
12. [ChatGPT 可同时登录两个账号并直接切换](#item-tech-news-12) ⭐️ 5.0/10
13. [用户称 Grok 支持支付宝付款并推首月半价，细节未确认](#item-tech-news-13) ⭐️ 5.0/10

**财经新闻**
1. [香港电讯同意在 FCC 压力下停止美国业务](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [ChatGPT 与 Codex 将从 12 月起共享用量额度](https://x.com/thsottiaux/status/2116692529970311254) ⭐️ 8.0/10

据 Telegram 频道“科技圈·茶馆”转述，OpenAI 计划从 12 月起把 ChatGPT 与 Codex（OpenAI 的编程助手）的用量额度合并，适用于 Plus、Pro 和 Business 三档付费套餐。合并后额度按词元（token，模型处理文字时使用的计量单位，可粗略理解为字词片段）计算：模型越先进、任务越复杂，消耗越大；即时聊天不占用额度。用户可在设置中查看合并后的剩余用量和重置时间，超出后可等待重置、升级套餐或购买积分（额外用量）。这条消息没有给出各套餐的具体额度或消耗速度，因此目前还无法判断影响有多大。

telegram · zaihuapd · 11月1日 01:29

**「背景」** ChatGPT 是 OpenAI 的通用聊天机器人，Codex 则是能代为写代码、执行开发任务的智能体（能自己分步骤完成任务的程序），两者的用量额度此前分开计算。额度按“词元”（token，模型读写文字时计量的基本单位）计算，模型越先进、任务越复杂，消耗就越多。

**「对重度用 Codex 的人最直接的影响」** 对同时用 Codex 和 ChatGPT 的付费用户来说，最直接的变化是两边不再各自拥有一份额度：据第三方整理的现有额度说明，Codex 在 Plus、Pro、Business 上原本有自己的五小时窗口和每周额度（tool-3-1），合并后这些高强度编码任务会从同一个池子里扣除，可能让原本够用的 ChatGPT 额度提前用尽。设置里会显示合并后的剩余用量和重置时间，超额后只能等重置、升级套餐或购买积分；由于官方目前没有公布各套餐对应的词元数量和折算比例，用户还无法提前算出一次具体任务会消耗多少。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/20001625-understanding-chatgpt-and-codex-usage-limits">Understanding ChatGPT and Codex usage limits | OpenAI Help ...</a></li>
<li><a href="https://standardcompute.com/codex-usage-limits">Codex Usage Limits (Oct 2026): Plus vs Pro, Weekly Limit, Reset</a></li>
<li><a href="https://usagebox.com/articles/openai-codex-pricing-usage-limits-2026">OpenAI Codex Pricing &amp; Usage Limits (October 2026): Every ...</a></li>

</ul>
</details>

**标签**: `#ChatGPT`, `#Codex`, `#usage quotas`, `#OpenAI`, `#subscription pricing`

---

<a id="item-tech-news-2"></a>
### [Memdoor 发布让五个开源模型组队写代码的工作流，宣称胜过更强的模型](https://github.com/guregodevo/memdoor/tree/main/examples/workflows/team-solve) ⭐️ 7.0/10

GitHub 上的项目 Memdoor 新增了一个名为 team-solve 的示例工作流：它把五个 Qwen 系列的开源权重模型（权重公开、可以下载到本地自己运行）组成一个「小组」，让它们一起解决编程题，并宣称在 LiveCodeBench Hard（一个用高难度题目测试写代码能力的题库）上的成绩超过了名为「Fable 5」的更强模型。这条消息在 Hacker News 上被讨论，作者只给出仓库路径，没有提供可复现的分数、具体配置或运行成本。标题里的两个模型名称（「Qwen3.8-27B」与「Fable 5」）也无法从现有材料中明确对应到具体版本，因此「胜过 Fable 5」目前只能算项目方的一面之词，不是经过独立验证的结果。

hackernews · guregodevo · 10月31日 22:46 · [社区讨论](https://news.ycombinator.com/item?id=50320995)

**「背景」** LiveCodeBench 是一套公开的编程题测试集，“Hard”是其中较难的一档，常被用来比较不同模型写代码的水平。这里说的“组队”并不是五个不同的大模型同台：而是把同一个开放权重模型（权重可以下载、装在自己的电脑或服务器上跑，不必连厂商的服务）复制成五份，分别扮演规划者、两个出点子的人、解题者和检查者，外加一个修补角色，彼此只靠读写同一批文件来沟通。按项目说明，这套流程复现的是他人提出的方法：五个 Qwen3.8-27B 副本在 Hard 档前十道题上跑五轮，平均得分 9.8（满分 10），原作者自己的流程为 9.6，单独运行 Fable 5 为 8.0。

**「想照着复现的人要先算两笔账」** 第一，这个对比并不对等：同一条“多个模型组队答题”的流程同样可以套在更强的模型上，评论者就指出 Fable 5 换上同样的框架大概率也会变强，所以“五个小模型打赢大模型”说明的是这套组合方式有效，而不是小模型本身追平了。第二，成本并不为零：据 daily.dev 的记录，在 OpenRouter 上跑完 50 次测试（10 道 LiveCodeBench Hard 题各跑 5 遍）花掉 35.79 美元的输出 token 费用（模型生成的文字按量计费，约 1530 万个），算上 16 次因超时或中断而作废的尝试则为 38.77 美元；若改在本地跑，则需要能装下量化后（压缩精度以便在消费级显卡上运行）的 27B 模型，有评论者称在价格合理的游戏 PC 上可达到每秒约 50 个 token 的速度。

**「社区讨论」** 评论者 roenxi 提供了一个具体的本地运行参考：经过 Bonsai 2 这类量化压缩（把模型体积压小以便在普通显卡上运行）后，Qwen 27B 可以在一台价格合理的游戏电脑上达到每秒约 50 个词块的生成速度，他认为这说明本地模型的性能上限可能相当高；但他同时提醒，同一套组队方法用在 Fable 上也会提升 Fable 的成绩，所以差距未必会缩小。另一位评论者 yurimo 认为，让多个模型协同正成为提升能力的新方向，但效果很受模型之间「沟通方式」的设计和算力限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/guregodevo/memdoor/tree/main/examples/workflows/team-solve">memdoor/examples/workflows/team-solve at main · guregodevo ...</a></li>
<li><a href="https://aiweekly.co/alerts/memdoors-five-qwen38-27b-team-beats-fable-5-at-livecodebench">Memdoor&#x27;s five-Qwen3.8-27B team beats Fable 5 at LiveCodeBench</a></li>
<li><a href="https://en.mycoding.id/memdoor-a-team-of-5-qwen3-8-27b-models-beats-fable-5-on-livecodebench-hard-75096">Memdoor: A team of 5 Qwen3.8-27B models beats Fable 5 on ...</a></li>
<li><a href="https://www.vals.ai/benchmarks/lcb">LiveCodeBench Leaderboard and Methodology | Vals AI</a></li>
<li><a href="https://daily.dev/posts/memdoor-a-team-of-5-qwen3-8-27b-models-beats-fable-5-on-livecodebench-hard-ghdvz1p3j">Memdoor: A team of 5 Qwen3.8-27B models beats Fable 5 on...</a></li>

</ul>
</details>

**标签**: `#open-weight models`, `#multi-agent workflows`, `#coding benchmarks`, `#local inference`, `#Qwen`

---

<a id="item-tech-news-3"></a>
### [创作者公布 24 秒竖屏动画的多模型制作流程与费用表](https://habr.com/ru/articles/1102098/?utm_campaign=1102098&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 7.0/10

一位俄罗斯创作者在技术社区 Habr 上发文，介绍如何用多款云端 AI 模型制作 24 秒竖屏动画短片《Лесная улица》（意为“森林街”），片中角色固定，对白为俄语。据文章开头，他在 2026 年 10 月 29 日至 31 日之间，用 Wan、Kling、Veo、Seedance 四款 AI 视频生成模型（输入文字或图片就能生成视频片段的云端服务）和 GPT Image、Nano Banana Pro 两款图像生成模型，把同一集试做了大约十种版本。文章说明会给出固定的操作顺序、费用表、“废片与修正”的对照，以及一份“始终没修好”的清单；但可见的摘要只到开头，具体金额和修正方法无法核实。文中提到，截至 10 月 31 日已发布《А телефон куда?》和《Подменишь?》两集，另外两集仍是制作试验；作者也明确说明目前没有观众数据，只谈制作过程。

rss · Habr AI · 10月31日 14:55

**「背景」** 这类片子靠“文生视频”模型生成：Wan、Kling、Veo、Seedance 都是把文字描述（可附一张参考图）变成几秒钟画面的云端服务；GPT Image 和 Nano Banana Pro 则属于图像模型，只出静态画面，其中 Nano Banana 是 Google 的文本生成与修图工具。视频模型很难每次都把同一个角色画成一个样子，所以常见做法是先用图像模型定出角色的“设定图”，再让视频模型照着它生成每个镜头——这就是文中“参考图”的作用。竖屏指手机竖着观看的画面比例，方便在短视频平台播放。

**「实际影响」** 对想自己制作这类竖屏短动画的人来说，实际结论是：一条 24 秒的成片无法靠一次生成完成。作者在同一集上换了约十种方案反复重做，并依靠固定的角色参考图（定妆图）防止人物走样：例如 Seedance 曾在同一画面里生成两个主角。因此，排期和预算要按“每个镜头多轮重试”来估算，不能只用镜头数乘以一次生成来算；费用则要按各家按秒计价的服务逐项核对（第三方对比文章举例说，Wan 2.7 的服务为每秒 0.018 美元）。原文虽提到附有费用表，但摘要中没有给出具体数字，单集成本无法在此核实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nanobanana.io/ru">Nano Banana : бесплатный онлайн AI-редактор изображений</a></li>
<li><a href="https://www.ainchina.com/blog/china-ai-video-models-conquer-global-market-kling-seedance-wan-2026/">Sora Is Dead, Long Live Kling : How Chinese AI Video Models...</a></li>

</ul>
</details>

**标签**: `#AI video generation`, `#Kling`, `#multi-model pipeline`, `#cost breakdown`, `#production workflow`

---

<a id="item-tech-news-4"></a>
### [开发者发布 mcp-linter：用 34 条规则检查 MCP 服务器](https://habr.com/ru/articles/1102086/?utm_campaign=1102086&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 7.0/10

10 月 31 日，一位作者在 Habr 上发布开源工具 mcp-linter，用来在把 MCP 服务器接入 AI 助手之前检查其代码（MCP 是让 Claude Desktop、Cursor 这类 AI 助手调用外部工具和数据的通用接口标准）。该工具用 Node.js/TypeScript 编写、不依赖任何第三方库，内置 34 条协议与安全检查规则，按 0 到 100 分给出 A+ 至 F 的健康评级，支持用 --fix 自动修复部分问题、导出 SARIF 报告（GitHub 安全页面能直接读取的格式），并附带现成的 GitHub Action；作者给出的一行试用命令是 npx mcp-linter，代码放在 GitHub 的 mcp-doctor 仓库。它针对的是几类具体故障：代码里一句普通的调试打印（console.log）写错位置，就会破坏 MCP 使用的 JSON-RPC 通信格式、让客户端卡死；删除数据库或文件这类危险操作若没有标注 destructiveHint（危险提示），AI 助手可能不经用户确认就执行；工具描述里还可能被塞入提示注入（prompt injection，藏在文本中操纵模型的内容），诱导模型泄露上下文。作者声称该工具在 Anthropic 官方 MCP 服务器中找出了 bug，但帖子没有列出具体问题或复现步骤，这目前只是作者本人的说法。

rss · Habr AI · 10月31日 13:55

**「背景」** MCP（Model Context Protocol，模型上下文协议）是一套约定，让 AI 助手能够调用外部程序提供的功能、读取外部数据；按这套约定写出的程序叫 MCP 服务器，Claude Desktop、Cursor 这类客户端会启动它，并通过固定的消息格式来回通信。作者点出的常见隐患是：服务器多打一行普通日志就可能打断通信、让客户端卡住；删除数据库或文件这类危险工具如果没有标明“会改坏数据”，模型可能不先征求用户同意就调用；工具说明文字里还可能藏有诱导模型泄露对话内容的内容。

**「对使用者的实际影响」** 对用 Claude Desktop 或 Cursor 的人来说，可执行的动作很具体：在把一个 MCP 服务器（让 AI 助手调用外部工具、读取文件或数据库的插件式程序）接入客户端之前，先用 npx mcp-linter 跑一遍。按作者的说明，它能查出三类会让日常使用出问题的地方：多余的打印输出会把客户端的通信协议打断、直接卡死；删除数据库或文件这类危险工具如果没标注“需要用户确认”，助手就会不问自取地执行；工具说明文字里还可能藏着提示注入，诱导模型泄露上下文。作者称用这个工具在 Anthropic 官方服务器里找到了 bug，但文中没有给出可复现的细节，因此在官方确认或修复前，这只能算线索而不是结论。

**标签**: `#MCP`, `#developer tooling`, `#linter`, `#security`, `#Claude Desktop`

---

<a id="item-tech-news-5"></a>
### [开源工具「栖言」：为 Codex 桌面端加账号切换和用量统计](https://linux.do/u/user400) ⭐️ 7.0/10

11 月 1 日，LINUX DO 论坛用户 user400 发布了一款名为「栖言」的开源桌面工具（源码仓库为 still-codex-switcher），为 OpenAI 的编程助手 Codex 的桌面客户端补上三项功能：在多个账号之间切换、查看账号剩余的可用额度、统计消耗的 token（模型处理文字时使用的计量单位，可粗略理解为按“字数”计费的单位）。项目采用 MIT 许可证，这是一种允许他人自由使用、修改和再发布的宽松开源协议；作者同时放出了 macOS 1.6.0-preview.1 和 Windows 1.5.0-preview.1 两个预览版下载，两个平台版本号不同，开发进度并不一致。作者在帖中声明项目已完整开源，并说明介绍文字由 AI 辅助撰写、附有截图。需要说明的是，这是第三方非官方工具，仍处于预览阶段，它显示的额度和 token 数字没有经过独立验证。

telegram · linuxdo\_tg · 11月1日 05:47

**「背景」** Codex 是 OpenAI 的编程助手，装在电脑上、用 ChatGPT 账号登录，按套餐额度使用。它的登录凭证保存在本机的一个文件里（~/.codex/auth.json），所以所谓「换账号」实际上就是替换这个文件；已有的第三方切换工具也提醒，切换前要先关掉正在运行的 Codex 或 ChatGPT，否则可能把当前账号的登录状态弄乱（tool-2-1）。栖言要做的，就是把这一套手动操作搬到桌面界面上。

**「对使用者的影响」** 对同时持有多个 Codex 账号、或经常碰到用量上限的人来说，这个工具把切换账号和查看剩余额度放进了同一个桌面界面，省去了一部分手动操作。但由于它只是预览版、又来自第三方，安装前应自行确认下载来源，其显示的额度与 token 统计也不宜当作账单依据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Lampese/codex-switcher">GitHub - Lampese/ codex - switcher : A Desktop Application for...</a></li>

</ul>
</details>

**标签**: `#codex`, `#coding-agents`, `#open-source`, `#developer-tooling`, `#quotas`

---

<a id="item-tech-news-6"></a>
### [Parameter Labs 披露已修复的 ChatGPT 账号接管漏洞](https://simonwillison.net/2026/Oct/31/how-we-took-over-chatgpt-accounts/) ⭐️ 6.0/10

安全公司 Parameter Labs 公开了一条已被 OpenAI 修复的 ChatGPT 漏洞组合：攻击者能制作一个 ChatGPT 分享链接，已登录用户点开后，私密数据可能被读走，账号也可能被以本人身份操作。问题出在 ChatGPT 展示交互式 HTML 小应用的隔离框（iframe，网页里再嵌一个网页，用来关住不信任代码）。据其描述，攻击者先借数学公式输入组件 MathLive 的虚拟键盘向主页面发消息，主页面又把消息内容当作网页代码插入，于是能塞进一个不受隔离限制的新框架；再借 YouTube 的嵌入接口绕过“只允许从少数网站加载程序代码”的白名单，拿到执行权限后读取并外传数据。OpenAI 已封堵漏洞并支付 5000 美元赏金；Simon Willison 在转述中认为，对这么严重的漏洞来说这笔赏金偏低。

rss · Simon Willison · 10月31日 23:15

**「背景」** ChatGPT 的 HTML 预览会把用户生成的网页放进一个“沙箱 iframe”：这相当于在 ChatGPT 页面里再嵌一个受限制的小网页，里面的代码不能直接读取账号数据，也不能使用 ChatGPT 的内部功能。Parameter Labs 研究的就是这道隔离能否被绕过；一旦绕过，别人发来的一个分享链接就可能在接收者已登录的情况下，替接收者操作账号或拿走私人数据。

**「对用户的影响」** 按现有披露，漏洞已经封堵，普通用户不需要为此更改设置或密码。实际可采取的做法仍是把别人发来的 ChatGPT 分享链接当作外部链接对待：先确认发送者是谁，再决定是否点开，因为在这类漏洞存在时，风险不只来自页面内容，仅访问链接就可能触发账号操作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.parameter.ai/labs/we-found-a-gap-at-openai">Do the Math : How We Took Over ChatGPT Accounts - Parameter</a></li>

</ul>
</details>

**标签**: `#security`, `#ChatGPT`, `#sandbox-escape`, `#exploit-disclosure`, `#artifacts`

---

<a id="item-tech-news-7"></a>
### [开源模型路由器 FAIRouter 的 C\# 版上架 NuGet](https://habr.com/ru/articles/1101942/?utm_campaign=1101942&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

开源 AI 模型路由器 FAIRouter（在多个 AI 模型之间自动挑选一个来回答请求的软件）的 C\#（微软主推的编程语言）版已发布到 NuGet（微软 .NET 开发平台使用的软件包仓库），用 C\#/.NET 开发软件的人可以安装使用。项目的目标是让程序在速度、成本和回答质量之间取得平衡：用更低的成本和更快的速度得到“足够好”的回答。文章摘要只说会介绍如何安装、发出第一个请求、根据反馈训练路由器，以及接入自选模型，并未给出包版本、性能测试或路由质量数据；因此“更便宜更快”目前是项目目标，不是已公开证实的实测结果。

rss · Habr AI · 10月31日 08:53

**「背景」** 大语言模型在速度和价格上差别很大，模型路由器的作用是先判断任务，再把请求交给其中一个模型来回答。据文章介绍，FAIRouter 还会让一个“裁判”检查回答，并让路由器和裁判根据反馈逐步调整；项目提供 C\# 实现，方便 .NET 开发者接入。此前使用 C\# 版需要从源代码自行构建，现在它已发布到 NuGet（.NET 的软件包仓库，可类比为开发者安装依赖的应用商店），可以直接安装。

**「实际影响」** 对正在用 C\#/.NET 做产品的团队来说，实际变化是多了一个可以从 NuGet 安装的模型路由候选；但由于公开摘要没有给出对比测试数据，采用前应拿自己业务中的真实请求，比较它选出的模型与固定使用单一模型的效果和账单。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://habr.com/ru/articles/1101942/">FAIRouter вышел на NuGet. Выбираем языковую модель под задачу ...</a></li>

</ul>
</details>

**标签**: `#model routing`, `#C\#`, `#.NET`, `#open source`, `#LLM cost optimization`

---

<a id="item-tech-news-8"></a>
### [网传 Anthropic 封停涉及训练更大模型的账号，政策未获证实](https://twitter.com/jiahaoshao1/status/2116475922190922088) ⭐️ 5.0/10

一条发布在 X（原推特）上的帖子称，Anthropic 正在封停那些用其对话式 AI 助手 Claude 从事“训练更大模型”相关工作的账号。这里的“训练”指用大量数据反复调整模型内部参数、让它学会完成任务的过程。帖子没有给出条款原文、被点名的用户或具体日期，Anthropic 也未公开确认，因此这只能算未经证实的说法；它在 Hacker News 上引来了约 160 条评论。

hackernews · pretext · 10月31日 19:39 · [社区讨论](https://news.ycombinator.com/item?id=50319358)

**「背景」** 大型 AI 服务商的用户条款通常禁止用户拿产品的输出去训练竞争对手的模型，最重的后果就是账号被封。据科技媒体报道，Anthropic 在 2026 年 10 月调整过一次针对滥用行为的政策，当时表示主要手段是让 Claude 中止某段对话，而不是直接处罚账号，并说明普通的不满、批评或正当的研究测试不受影响。2026 年 2 月也有用户反映，因为同时持有多个 Claude Max 订阅账号而被封禁。

**「对用户意味着什么」** 对付费使用 Claude 的人来说，真正麻烦的是界线不清：如果封号依据的是“用途”而非滥用行为，用户无法从公开条款判断自己的项目是否踩线，也就无法提前规避。评论者给出的应对是平时就备好可替换的模型和工具，但这属于用户建议，不是已确认的政策细节。

**「社区讨论」** 讨论中较有代表性的一种看法是：无论多喜欢 Claude，专业用户都应主动培养一套替代方案，避免被单一厂商锁死。也有用户报告说，Claude 近期在正常开发任务上频繁拒答，例如拒绝从自己公司的代码库中提取服务，或以涉及登录为由拒绝做浏览器测试。这些是个人经历和观点，反映的是用户对 Anthropic 限制风格的感受，并不能证实封号传闻本身。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://theaiinnovator.com/anthropic-bans-users-from-abusing-claude-under-new-ai-policy/">Anthropic Bans Users From Abusing Claude Under New AI Policy</a></li>
<li><a href="https://metricnexus.ai/blog/anthropic-banning-multiple-claude-accounts">Anthropic Is Banning Users With Multiple Claude Accounts ...</a></li>

</ul>
</details>

**标签**: `#anthropic`, `#claude`, `#account-bans`, `#access-restrictions`, `#terms-of-service`

---

<a id="item-tech-news-9"></a>
### [Datasette Agent 插件更新：启动时不必再指定默认模型](https://simonwillison.net/2026/Oct/31/datasette-llm/) ⭐️ 5.0/10

开发者 Simon Willison 发布了 datasette-llm 插件的 0.1a9 版本（版本号里的 a 表示这是供测试的早期预览版）。这个插件（给现有软件添加功能的小程序）现在会自动沿用他另一个命令行工具 LLM 里已经设好的默认模型，所以启动 Datasette Agent 时不用再额外加一段参数去指定模型。Datasette 是一个把数据文件变成可浏览网页的工具，Datasette Agent 则是在其之上接入大模型的部分。作者本人说明这只是一次很小的使用体验改进，并提到 Datasette Agent 还有较大的升级在准备中，但没有透露细节。

rss · Simon Willison · 10月31日 22:10

**「背景」** datasette-llm 是 Datasette（一个浏览和发布 SQLite 单文件数据库的工具）的插件，给 Datasette Agent 提供调用语言模型的能力。它通过作者开发的命令行工具 LLM 来调用模型，而 LLM 本身可以记住一个默认模型。0.1a9 之前，启动 Datasette Agent 还要另外指定这个默认模型；现在它会直接沿用 LLM 已配置的模型。

**「对使用者的影响」** 对已经用这套工具的人来说，启动命令变短了：原来要在命令后面补上类似“-s plugins.datasette-agent.default\_model 模型名”的设定，现在可以省略。前提是你在 LLM 工具里已经配置过一个默认模型，这一步仍然要事先做好，插件只是去读它，并不能替你选模型。

**标签**: `#datasette`, `#datasette-agent`, `#llm`, `#developer-tooling`, `#release`

---

<a id="item-tech-news-10"></a>
### [开发者尝试不用 IDE、只让 Qwen 与 Qwen Coder 写 NTFS 数据流扫描器](https://habr.com/ru/articles/1102144/?utm_campaign=1102144&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位作者在俄罗斯技术社区 Habr 上发文，记录自己尝试完全不使用 IDE（集成开发环境，即平时写代码用的那类带补全和调试功能的软件），只靠 Qwen 与 Qwen Coder（后者是该系列中面向编程的版本）来写一个扫描 Windows NTFS 文件系统“备用数据流”的小工具。他明确把这件事定位为对 Qwen 系列模型写代码能力的测试，而不是一个成品发布。备用数据流是 NTFS 的一个特性：可以把额外数据附加到某个文件上，而用系统常规方式看不到这些数据。需要注意的是，目前可见的文章内容只有开头，只交代了目标和背景，没有给出所用的提示词、环境配置、代码，也没有报告成功或失败的结果，所以这只是一次个人实验的记录，还不是经过验证的能力结论。

rss · Habr AI · 10月31日 18:18

**「背景：隐藏数据流与 AI 编程」** NTFS 是 Windows 系统常用的文件系统，它允许一个文件附带多个“替代数据流”（ADS），这些数据流就像藏在文件背后的附加内容，用资源管理器等常规方式看不到。Qwen 和 Qwen Coder 是能根据文字指令生成代码的 AI 模型；这篇文章的作者让它们在不使用集成开发环境（IDE，程序员编写和调试程序的整套软件）的情况下，试着写出一个找出这些隐藏数据流的扫描器，以此检验模型的编程能力。

**标签**: `#qwen`, `#code-generation`, `#coding-agents`, `#model-capability`, `#windows`

---

<a id="item-tech-news-11"></a>
### [TBook 阅读格式更新：手机版、桌面阅读器、离线词典与第二版格式](https://habr.com/ru/articles/1100334/?utm_campaign=1100334&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

在最初介绍 TBook 的文章发布四个月后，作者更新了这个把外语书排成原文与译文逐行对照的项目：Android 版已上架 Google Play 应用商店，电脑端阅读器覆盖三种操作系统，并增加了离线词典、在线转换器（带共享书库和 Telegram 机器人）、带图形界面的转换器及可直接运行的程序。作者还发布了第二版 TBook 格式；项目的关键做法是用价格较低的 AI 大语言模型（能生成和翻译文字的 AI 程序）自动把原文和译文对齐，减少越往后越错位的问题。更新中另附约二十份翻译质量实验报告，但这些进展和报告来自作者本人的说明，未见独立评测。

rss · Habr AI · 10月31日 12:45

**「背景」** TBook 是一种把外语书排成双语对照的阅读格式：原文旁边配上译文，方便逐句对照阅读。作者在今年 7 月的文章里说过，这个项目最初是因为他找不到合用的外语书阅读器；那篇文章有一半在讲，如何让便宜的 AI 模型稳定生成这种对照，又不让译文和原文错位。四个月后，这次更新介绍的是阅读应用、桌面阅读器、词典和格式第二版，而不是新的 AI 模型或翻译服务。

**标签**: `#LLM translation`, `#interlinear alignment`, `#reading app`, `#prompt engineering`, `#side project`

---

<a id="item-tech-news-12"></a>
### [ChatGPT 可同时登录两个账号并直接切换](https://x.com/thsottiaux/status/2116405414921384099) ⭐️ 5.0/10

OpenAI 为 ChatGPT 上线了账号切换功能：在网页端、iOS 和 Android 应用上，用户最多可以同时保持两个账号登录，不用退出当前账号就能切到另一个；桌面端计划很快支持。OpenAI 表示，切换后两个账号的聊天记录、记忆（让 ChatGPT 记住用户偏好和信息的设置）、文件、工作区（团队共用的资料和设置）以及订阅和账单都完全分开，不会合并或互通。手机端还能同时接收两个已登录账号的通知，点开哪条通知就进入对应账号。

telegram · zaihuapd · 10月31日 05:58

**「账号数据彼此独立」** ChatGPT 的聊天记录、记忆（它记住的关于你的偏好和事实）、文件和订阅都绑定在具体账号上。工作和个人账号因此相当于两套互不相通的数据，切换账号本质上是在两套数据之间切换，而不是换一个界面。

**「实际影响」** 对同时有工作号和个人号的用户，最直接的变化是不必反复退出再登录。但最多只能同时登录两个账号，而且每个账号的聊天记录、记忆、文件和订阅仍各自独立，切换后要留意当前处于哪个账号，避免在错误的账号里发消息或上传文件。

**标签**: `#ChatGPT`, `#OpenAI`, `#account-management`, `#subscription`, `#access`

---

<a id="item-tech-news-13"></a>
### [用户称 Grok 支持支付宝付款并推首月半价，细节未确认](https://x.com/jordan1oi/status/2116371730965172442) ⭐️ 5.0/10

一名 X 用户发帖称，Grok 现已支持用支付宝付款，并推出首月半价的优惠。帖子里没有说明是哪个套餐、原价多少、半价后多少钱、优惠持续多久，也没有说哪些地区或账户可以参加。xAI 官方没有确认这一说法，这条消息只是经 Telegram 频道转发的单一用户说法，目前既不能当作已经上线的付款方式，也不能当作可以照着付钱的价格。发帖者还认为，这会给替人代付的“代充”生意带来冲击，这同样是他的个人判断。

telegram · zaihuapd · 10月31日 06:41

**「背景」** Grok 是 xAI 开发的聊天机器人，它与 X（原 Twitter）共用同一套账号和付费体系，用户想获得 Plus 等级或更高用量，就需要按月订阅。过去，中国大陆用户为这类海外订阅付费，通常要么使用外币信用卡，要么找第三方“代充”（替人代付、收取手续费的中间商）；来源中提到代充生意受到冲击，这也说明这条路径是不少人的实际选择。

**「对想订阅的人意味着什么」** 如果支付宝真的能直接付款，最直接的变化是不必再找“代充”，也就是替没有境外信用卡的人代付、从中收取差价的中间商。不过在这条消息得到官方确认前，打算订阅的人最好先到 Grok 或 xAI 的官方订阅页面核对支持的付款方式和首月实际价格，再决定要不要把钱交给第三方代付。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://phemex.com/news/article/xais-grok-adds-china-unionpay-and-alipay-payment-support-offers-halfprice-firstmonth-subscription-101964">xAI Grok Now Supports Alipay &amp; UnionPay Payments With Half-P ...</a></li>

</ul>
</details>

**标签**: `#Grok/xAI`, `#subscription pricing`, `#payment methods`, `#regional access`, `#promotions`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [香港电讯同意在 FCC 压力下停止美国业务](https://www.cnbc.com/2026/10/31/hong-kong-telecom-firm-agrees-to-halt-us-operations-under-pressure.html) ⭐️ 7.0/10

香港电讯（HKT）在美美国联邦通信委员会（FCC）压力下同意停止其美国业务；按和解条件，它须在 30 天内提交停业申请，并在 2027 年 9 月 1 日前停止对美及在美电信服务。FCC 于 2025 年 10 月以国家安全及与联通关联为由启动撤销其运营授权程序；和解达成后，该程序不再推进，母公司电讯盈科（PCCW）拒绝立即置评。

telegram · zaihuapd · 10月31日 10:22

**「背景」** 美国联邦通信委员会（FCC）于 2025 年 10 月启动程序，拟撤销香港电讯在美提供国际及本地电信服务的授权，理由包括国家安全顾虑以及该公司与中国联通（China Unicom）的关联；双方和解后，这一撤销程序不再推进。

**「影响」** 依赖香港电讯美国线路的跨国企业和运营商客户，须在 2027 年 9 月 1 日服务终止前把相关通信业务转往其他供应商，否则将失去这条美港连接通道。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/10/31/hong-kong-telecom-firm-agrees-to-halt-us-operations-under-pressure.html">Hong Kong telecom firm agrees to halt U.S. operations under ...</a></li>
<li><a href="https://docs.fcc.gov/public/attachments/DOC-415089A1.pdf">FCC Moves to Expel Hong Kong Telecom from U.S. Telecom ...</a></li>
<li><a href="https://www.straitstimes.com/world/hong-kong-telecom-company-agrees-to-halt-us-operations-under-pressure">FCC forces HKT to halt US telecom operations | The Straits Times</a></li>

</ul>
</details>

**标签**: `#HKT`, `#FCC`, `#telecom regulation`, `#US market exit`, `#national security`

---