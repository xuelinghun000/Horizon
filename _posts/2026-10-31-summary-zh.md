---
layout: default
title: "Horizon Summary: 2026-10-31 (ZH)"
date: 2026-10-31
lang: zh
---

> 从 115 条内容中筛选出 20 条重要资讯。

---

**科技新闻**
1. [Cursor 插件市场出现被篡改的 Claude Code 扩展，暗中植入 SSH 后门](#item-tech-news-1) ⭐️ 8.0/10
2. [Claude 将 Max 套餐改名，Ultra 用户取消五小时用量限制](#item-tech-news-2) ⭐️ 8.0/10
3. [有人把红白机模拟器塞进了约 1GB 的 Qwen 模型权重里](#item-tech-news-3) ⭐️ 7.0/10
4. [个人 Telegram 客户端让 OpenCode 编程代理可在手机操作](#item-tech-news-4) ⭐️ 7.0/10
5. [论坛帖称 Antigravity 11 月 2 日下架 Claude 4.6 等模型](#item-tech-news-5) ⭐️ 7.0/10
6. [开发者把经典 Mac OS 移植到任天堂 Wii](#item-tech-news-6) ⭐️ 6.0/10
7. [文章称可移交命令行 AI 会话，方法未公开](#item-tech-news-7) ⭐️ 6.0/10
8. [小米开源 8 亿参数文档理解模型 Xiaomi-OCR-0](#item-tech-news-8) ⭐️ 6.0/10
9. [腾讯开源世界模型 Hy-Nomas，宣称可在单张 RTX 4090 上运行](#item-tech-news-9) ⭐️ 6.0/10
10. [Habr 文章称 3210 亿参数混合专家模型可跑在单张 RTX 3090 上](#item-tech-news-10) ⭐️ 5.0/10
11. [FLUX.3 klein 生成 290 张牙医宣传照，作者称花费约 3 美元](#item-tech-news-11) ⭐️ 5.0/10
12. [俄语教程：在 HuggingFace 上挑选并运行开源模型](#item-tech-news-12) ⭐️ 5.0/10
13. [LTX-2.5 视频模型称能在 10GB 显存 RTX 3080 上运行](#item-tech-news-13) ⭐️ 5.0/10
14. [用户称 Claude 在身份验证后停用账号](#item-tech-news-14) ⭐️ 5.0/10
15. [爱好者把 MSI 笔记本键盘改成独立 USB 键盘](#item-tech-news-15) ⭐️ 5.0/10
16. [开源项目声称用 AI 将 Jira 工单自动推进到已审核的代码合并请求](#item-tech-news-16) ⭐️ 5.0/10
17. [DeepSeek 官网代码出现“Cyber”模型申请入口，需企业资质](#item-tech-news-17) ⭐️ 5.0/10

**财经新闻**
1. [DeepSeek 据报完成第二轮融资 1055 亿元，估值超 6155 亿元](#item-finance-news-1) ⭐️ 7.0/10
2. [四家日系车企 4 至 9 月在华产量同比下降 32%](#item-finance-news-2) ⭐️ 7.0/10
3. [法国国民议会通过数据流量税修正案](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Cursor 插件市场出现被篡改的 Claude Code 扩展，暗中植入 SSH 后门](https://phorion.io/blog/offical-claude-code-vsx-compromise/) ⭐️ 8.0/10

10 月 29 日，Cursor 的插件市场里上架了一份被篡改的 Claude Code 扩展（VS Code 代码编辑器用的插件，版本号 2.1.313），它不是 Anthropic 自己发布的版本。安装后，它会把一枚攻击者的 SSH 公钥——相当于一把可以免密码远程登录你电脑的备用钥匙——写进用户电脑的授权登录名单（~/.ssh/authorized\_keys），并收集主机信息。这份版本在市场上挂了约 11 小时（太平洋时间凌晨 2:27 到下午 1:35），Cursor 估计最多约 5000 名用户受影响；由于建立隧道需要管理员权限，多数电脑上的后门没能装成。Cursor 已下架该版本、短暂关闭整个市场，轮换密钥后重新上线，攻击者的服务器也已下线。Anthropic 的员工在讨论中说明，这不是 Anthropic 的系统被攻破，官方渠道发布的版本不受影响，受影响的只有从 Cursor 市场安装的用户。

hackernews · \_chall · 10月30日 07:09 · [社区讨论](https://news.ycombinator.com/item?id=50300683)

**「背景：插件是从哪来的」** Claude Code 是 Anthropic 出品的编程助手，除了在命令行里用，它还有一个装在编辑器里的插件版本。所谓插件（extension），就是加装到 VS Code 这类写代码的软件里、给它增加功能的小程序；这类小程序由各自的“插件商店”负责分发，而 Cursor 的商店底层接的是 Open VSX 这个公共插件库，与微软官方的 VS Code 商店是两套系统。因此同一个插件名会同时出现在多个商店里，谁往哪个商店上传了哪一版就成了关键——有报道称微软官方商店没有受到影响，但对 Open VSX 是否也被波及，目前各方说法并不一致。

**「如果你装过，现在该做什么」** 在这段时间里从 Cursor 市场安装或更新过 Claude Code 插件的人，应当按 Cursor 公布的方法自查：在 macOS 上运行一条命令，搜索 ~/.ssh/authorized\_keys 里有没有名为 svc-telemetry 的密钥，Windows 上有对应的检查步骤。查到就说明这台机器被写入过，应删掉该密钥、更换自己的 SSH 密钥，再从 Anthropic 官方渠道重新安装插件。讨论中也有人提醒，目前公开的几份说明都只点明 Cursor 市场和 Open VSX（一个供非微软编辑器使用的开放插件仓库），没有明确说明微软官方插件市场是否也受影响，因此最稳妥的做法是只从 Anthropic 官方渠道获取插件。

**「讨论中的澄清与疑问」** Anthropic 的 Felix Rieseberg 在评论中澄清，攻击者是借用了 Cursor 市场的发布权限，上传了一份并非 Anthropic 构建的仿冒扩展，因此不算 Anthropic 的系统或员工电脑被入侵。另一位评论者则提出疑问：既然不是 Anthropic 发布的，这份篡改版本究竟是如何通过审核上架的；还有人指出，最初的报道详细描述了攻击手法，值得直接阅读原文。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/official-claude-code-vs-code-extension.html">Official Claude Code Extension on Cursor Marketplace ...</a></li>
<li><a href="https://www.stepsecurity.io/blog/claude-code-extension-trojanized">Trojanized Claude Code Extension Delivered Persistent SSH ...</a></li>

</ul>
</details>

**标签**: `#security`, `#claude-code`, `#cursor`, `#supply-chain`, `#vs-code-extensions`

---

<a id="item-tech-news-2"></a>
### [Claude 将 Max 套餐改名，Ultra 用户取消五小时用量限制](https://x.com/claudeai/status/2116220869479428500) ⭐️ 8.0/10

Anthropic 把 Claude 的两档付费订阅改了名字：原来的 Max 5x 现在叫 Max，原来的 Max 20x 现在叫 Ultra，月费维持 100 美元和 200 美元不变，已有订阅者不需要做任何操作。从 10 月 30 日起，通过身份验证的 Ultra 账户不再受「每 5 小时重置一次」的用量额度限制，多数现有订阅者会先被纳入。新账户在完成验证之前仍保留临时限制，官方说明这是为了防范欺诈和滥用，限制解除时会发邮件通知。按周计算的用量上限没有变化。

telegram · zaihuapd · 10月30日 17:44

**「背景」** Claude 是 Anthropic 公司提供的付费 AI 聊天服务，用户按月付费使用，用量按两种上限计量：一种是每隔 5 小时重置一次的短期上限，另一种是以一周为周期的长期上限；达到上限后要等窗口重置才能继续对话。对每天长时间使用它的人来说，真正卡住他们的是上限本身而不是价格，所以上限规则一改，感受最明显的就是这类重度用户。

**「对使用者的实际影响」** 对每月付 200 美元的 Ultra 用户，变化在于不用再等五小时窗口刷新才能继续对话，长时间连续作业时不会被中途卡住；但每周总额度仍在，所以能用的总量并没有变多，只是可以更集中地用。刚注册的新账户要先通过验证才能享受这一待遇，在此期间仍按原规则受限。

**标签**: `#Claude`, `#Anthropic`, `#subscription plans`, `#rate limits`, `#usage quotas`

---

<a id="item-tech-news-3"></a>
### [有人把红白机模拟器塞进了约 1GB 的 Qwen 模型权重里](https://github.com/dbreunig/nesformer) ⭐️ 7.0/10

开发者 Drew Breunig 在 GitHub 上公开了 nesformer：一个能运行的任天堂红白机（NES）模拟器，但它不是普通程序，而是被做进了 Qwen3.5-4B（一个约 40 亿参数、可自由下载的开源模型）约 1GB 的权重文件里——权重就是模型训练后得到的那批数值，模型平时靠它们来回答问题。现在《超级马力欧兄弟》这类游戏可以在模型内部跑起来，代价是速度比真实主机慢 150–290 倍。作者称这套权重和配套代码是他向 Anthropic 的 Opus 5.5 发出两条提示词后由模型自行写出的，这属于本人自述，未获独立核实；做法沿用了 Divyansh Agrawal 先前的 qwenputer 项目，过程中还用上了 Christopher Pow 15 年前发布的 NES 处理器一致性测试集。

hackernews · dbreunig · 10月30日 16:40 · [社区讨论](https://news.ycombinator.com/item?id=50306442)

**「背景」** 普通模拟器是用一段程序逐条模仿旧游戏机的硬件；nesformer 则把 NES 的 6502 处理器和内存的行为放进 Qwen3.5-4B 的模型权重（训练后保存下来的大量数值，模型靠它们作出反应）里，让模型本身来充当这台游戏机。它延续了 Divyansh Agrawal 的 qwenputer 项目的思路：那个项目已示范如何把一台简易计算机放进 Qwen 的权重中，这次则换成了 NES 的处理器和内存。

**「对实际使用意味着什么」** 对在本地跑开源小模型的人来说，可操作的路径是去仓库取权重，用作者提供的命令行工具指向自备的游戏镜像文件（ROM，即卡带内容的文件拷贝）来复现演示。按目前慢 150–290 倍的速度，它只能当作教学和展示样本，不能替代任何真正的模拟器来玩。

**「评论区在争论什么」** armcat 认为同样的办法可以把小型虚拟机（例如 Python 解释器、shell，以及 sed、grep 这类小工具）编译进权重，直接用模型内部的矩阵运算执行，不必像现在这样一个词一个词地输出再调用外部工具。jacquesm 和 pbohun 则更强调这是一次有趣的炫技：与普通程序相比它慢上千倍、算力消耗也多数千倍，恰好说明确定性代码有多高效；cafebeen 还指出，让他意外的是连内存（RAM）也被放进了模型内部，靠一种叫 gated deltanet 的结构来表示。

**标签**: `#open-weight models`, `#Qwen`, `#emulation`, `#GitHub projects`, `#LLM capability demos`

---

<a id="item-tech-news-4"></a>
### [个人 Telegram 客户端让 OpenCode 编程代理可在手机操作](https://habr.com/ru/articles/1101612/?utm_campaign=1101612&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 7.0/10

开发者 greenrus 在 2026 年新年假期把自己为方便使用而写的 Telegram 客户端开源，项目名为 opencode-telegram-bot，用来从手机操作 OpenCode 编程代理（能调用 AI 读文件、执行命令并修改代码的工具）。截至文章写作时，该项目在 GitHub 上获得 1298 个星标（用户收藏或表示支持的标记），并有 48 名贡献者。文章摘录只说明了项目起因和热度，没有给出安装步骤、功能清单或兼容范围，因此它是否已适合普通用户日常使用仍无法从现有内容确认。

rss · Habr AI · 10月30日 09:19

**「背景」** OpenCode 是一个在电脑命令行窗口里运行的 AI 编程代理（能按文字指令直接读写代码的软件）。作者最初只是为了用手机跟进这类任务，才写了 opencode-telegram-bot：它相当于给 OpenCode 加一个 Telegram 遥控器，任务仍在自己的电脑上执行，手机上可以派活、看进度、切换模型和管理会话。

**「实际影响」** 对已经在用 OpenCode 的人，这个项目提供了一个从手机发起和查看编码任务的入口；但文章摘录没有说明安装方式、支持的功能或与 OpenCode 的兼容范围，想尝试的人应先到项目页面核对这些信息，再决定是否把日常编码任务交给它。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/grinev/opencode-telegram-bot">GitHub - grinev/ opencode - telegram - bot : OpenCode mobile client via...</a></li>
<li><a href="https://skillsllm.com/skill/opencode-telegram-bot">opencode - telegram - bot - AI Agents on GitHub (1.2k ) | SkillsLLM</a></li>

</ul>
</details>

**标签**: `#opencode`, `#coding-agents`, `#telegram-bot`, `#open-source`, `#developer-tooling`

---

<a id="item-tech-news-5"></a>
### [论坛帖称 Antigravity 11 月 2 日下架 Claude 4.6 等模型](https://linux.do/u/KennethCC) ⭐️ 7.0/10

一则发布在 linux.do 论坛、经 Telegram 频道转发的帖子称，谷歌的 AI 编程工具 Antigravity 将在 11 月 2 日下架 Claude Sonnet 4.6、Claude Opus 4.6 和 GPT-OSS-120b 三款模型（前两个来自 Anthropic，第三个是 OpenAI 的开源模型）。按帖子说法，免费账号和 Google AI Plus 账号届时只剩 Gemini 3.8 Flash 可用；付费的 Google AI Pro（不含试用）、Ultra 和企业版仍可使用 Claude Sonnet 5.5 与 Opus 5.5。该消息目前只有这一个论坛来源，Antigravity 与谷歌均无官方确认，因此日期、模型名称和分档安排都应视为未经证实的说法。

telegram · linuxdo\_tg · 10月31日 02:02

**「背景」** Antigravity 是谷歌推出的 AI 编程工具：用户在一个编辑器里用对话让 AI 写代码、改代码，并从下拉菜单里选用哪家公司的 AI 模型。也就是说，哪些模型能在里面用、哪个订阅档位能用，由谷歌决定，而不是用户自己安装。据外部页面记录，Antigravity 的模型清单此前就把 Claude Sonnet 4.6、Opus 4.6 和 GPT-OSS-120b 列为可供免费、Google AI Plus 与 Google AI Pro 用户选择，并附注这些模型将在 2026 年 11 月 2 日移除；同一份模型说明还写明，Claude 5.5 只对非试用的 Google AI Pro 和 Ultra 开放。

**「对使用者的实际影响」** 如果你正用免费或 Google AI Plus 账号在 Antigravity 里调用 Claude 模型，按这则帖子，11 月 2 日之后这条路径就没有了，只剩 Gemini 3.8 Flash，习惯用 Claude 写代码或读长文档的人需要另找工具或改用其他入口。打算靠升级解决问题的人要注意：帖子明确说 Pro 试用版不含 Claude 5.5，只有付费的 Pro、Ultra 和企业版才有。在官方发布说明出来之前，先别据此调整订阅。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.orcarouter.ai/blog/claude-opus-5-5-and-sonnet-5-5-in-antigravity">Claude Opus 5 . 5 and Sonnet 5 . 5 Land in Google Antigravity</a></li>
<li><a href="https://smartscope.blog/en/blog/antigravity-claude-55-pro-trial-model-retirement-2026/">Google Antigravity : Why Sonnet 5 . 5 / Opus 5 . 5 Are... - SmartScope</a></li>

</ul>
</details>

**标签**: `#Antigravity`, `#Claude`, `#subscription-tiers`, `#model-deprecation`, `#access-restrictions`

---

<a id="item-tech-news-6"></a>
### [开发者把经典 Mac OS 移植到任天堂 Wii](https://virtuallyfun.com/2026/10/29/my-favourite-powermac-is-a-nintendo-wii/) ⭐️ 6.0/10

一位开发者在一篇实操博客中介绍了把经典 Mac OS（苹果早期麦金塔电脑使用的操作系统）移植到任天堂 Wii 上运行的过程；移植就是把为一种机器写的软件改到另一种机器上运行。这不是苹果或任天堂发布的官方功能，而是面向已改装（破解）Wii 的自制软件（爱好者自己编写、非官方发布的程序）尝试；现有条目没有提供可直接照做的完整安装步骤或程序源代码（编写软件的原始文本）。它只影响愿意折腾老游戏机和复古系统的爱好者，普通 Wii 或 Mac 用户不会因此获得新功能。

hackernews · DHowett · 10月30日 17:25 · [社区讨论](https://news.ycombinator.com/item?id=50307190)

**「为什么 Wii 能跑 Mac 系统」** 经典 Mac OS（苹果 2001 年以前的老 Mac 系统）当年主要运行在使用 PowerPC 处理器的 Mac 上，而任天堂 Wii 的主处理器同属 PowerPC 家族，两边底层指令能对得上，这是把老系统搬上游戏机的硬件前提。此前已有爱好者把 Windows NT 移植到 GameCube、Wii 和 Wii U 上（项目名为 entii-for-workcubes），作者 Wack0 也以这类移植闻名；这次让 Wii 运行 Mac OS 属于同一路数的自制软件（homebrew，指非官方、由爱好者编写的程序）尝试。

**「实际影响」** 如果你手上只有一台未改装的 Wii，这项移植不能直接使用；它也不会让普通 Mac 软件获得在 Wii 上的官方支持。想尝试的人需要先准备破解环境和加载自制软件的方法。

**「评论讨论」** 有评论称，这位移植者也是 GitHub 上 Macintosh 与 GameCube/Wii 相关项目的作者 Wack0，并给出了项目链接；另一位评论者希望这个移植能进入 Wii 自制软件商店 Open Shop Channel。还有人问能否反向把 PowerMac（苹果早期麦金塔电脑）变成 Wii，并表示模拟器满足不了自己，想去找一台经典 Mac 实机。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Wack0">Wack0 (Rairii) · GitHub</a></li>
<li><a href="https://archive.org/details/github.com-Wack0-entii-for-workcubes_-_2025-03-07_19-40-52">github.com-Wack0-entii-for-workcubes_-_2025-03-07_19-40-52</a></li>

</ul>
</details>

**标签**: `#emulation`, `#platform-port`, `#nintendo-wii`, `#classic-mac-os`, `#homebrew`

---

<a id="item-tech-news-7"></a>
### [文章称可移交命令行 AI 会话，方法未公开](https://habr.com/ru/companies/ruvds/articles/1101674/?utm_campaign=1101674&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

俄罗斯 Habr 网站上由 RUVDS 发布的一篇教程预告称，命令行 AI 代理（在终端里执行编程任务的 AI 工具）用完五小时额度后，可以把正在进行的会话移交给另一个代理，甚至连同未保存的文件一起转到另一台电脑。文章认为，常见的 HANDOFF.md 做法——让模型自己写一份交接摘要——会丢失上下文细节，下一个代理还得重新解释任务，并额外消耗 token（模型读写文本的计量单位）。但这段预告没有给出具体命令、脚本、代码仓库，也没有展示成功结果，因此它目前只是一项待公开的方法，不能当成已经验证可用的功能。

rss · Habr AI · 10月30日 13:01

**「背景」** 在终端里运行的编程助手（命令行 AI 代理）通常按订阅套餐计费，用量有上限，常见的是一个五小时的额度窗口，用满就得等下一次重置。这类工具会把整段对话详细写入本机的日志文件，各家的格式互不相同；即使执行了 /compact——让模型压缩上下文、腾出空间的命令——旧内容也不会从日志里被删掉，文件只会不断往后追加。所以一次进行到一半的会话实际上仍留在本机上，难点只在于怎样把它交给另一个代理接着做：过去常见的办法是让模型自己写一份交接摘要（HANDOFF.md），但那是模型的转述，细节容易走样，还要额外消耗用量。

**「实际影响」** 对同时使用多个有额度限制的编程助手的人来说，这针对的是额度用尽后的切换成本：理想情况下不必把项目背景重讲一遍。但在具体命令和演示公布前，读者无法照做；预告也只提到会带走未保存的文件，没有说明另一台电脑上的环境、权限或安全条件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://habr.com/ru/companies/ruvds/articles/1101674/">Перенос сессий между консольными ИИ - агентами без... / Хабр</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#session handoff`, `#rate limits and quotas`, `#developer tooling`, `#workflow`

---

<a id="item-tech-news-8"></a>
### [小米开源 8 亿参数文档理解模型 Xiaomi-OCR-0](https://x.com/XiaomiTech_/status/2116154468358316380) ⭐️ 6.0/10

小米开源了文档理解模型 Xiaomi-OCR-0，参数规模为 0.8B，也就是约 8 亿个参数（参数是模型内部可调的数值，数量多少大致对应模型大小和运行它所需的算力）。它可以做三件事：解析文档版面与内容、从文档中提取关键信息，以及“文字识别视觉问答”——给它一张文档图片并提问，它读出文字后作答。小米称，在 OmniDocBench v1.6 这项文档解析测试中，该模型在 10 亿参数以下的模型里排名第一；这是小米自己提交并说明的成绩，随附信息里没有可复现的评测细节。模型权重（训练好的模型文件）、运行模型的推理代码和演示都已公开，可自行下载。

telegram · zaihuapd · 10月30日 16:00

**「背景」** 文档理解模型不只把扫描件或照片里的字认出来（OCR，光学字符识别），还要保留标题、表格、段落等版面结构，并按指令提取字段或回答关于图片的问题。0.8B（约 8 亿参数）是衡量模型规模的粗略指标，参数越少通常越容易在普通电脑或单张显卡上运行。OmniDocBench 是业界用来比较文档解析效果的公开测试集。

**「对你意味着什么」** 如果你需要把扫描件、发票或表格图片转成可检索的文字和结构化信息，又不希望把文件上传到别人的云端服务，公开的权重意味着可以在自己的电脑或公司服务器上运行。8 亿参数在同类模型里属于偏小的一档，对硬件要求相对低。但实际效果需要你自己搭好运行环境、用自家文档试过才算数，厂商给出的榜单排名不能直接当作准确率保证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/xiaomi-research/Xiaomi-OCR-0">xiaomi-research/ Xiaomi - OCR - 0 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#open-weight models`, `#OCR`, `#document understanding`, `#Xiaomi`, `#small models`

---

<a id="item-tech-news-9"></a>
### [腾讯开源世界模型 Hy-Nomas，宣称可在单张 RTX 4090 上运行](https://hy-nomas.hy.tencent.com/demo) ⭐️ 6.0/10

腾讯把自家的世界模型（一种能按文字或相机指令生成连续视频、模拟场景随时间变化的 AI 模型）Hy-Nomas 的代码和模型权重公开了，采用 Apache 2.0 许可，任何人都可以下载、修改，也可以商用。模型用文字和相机运动控制画面，视频分段生成，段与段之间靠 KV 缓存（把前一段的内部状态存下来）保持连贯，相机路径既能提前设定，也能在片段之间改动。官方还给出了用 LoRA（一种只训练少量参数的低成本微调方法）在自己的视频上继续训练的办法，并附带“电影感画面”和“机器人”两类现成适配器。运行方面，帖子称有一份面向单张 RTX 4090 家用显卡的配置，用 INT8 量化（把模型数值精度压低以节省显存）、限制历史长度，并把部分模型卸载到内存，但这个模式的速度没有公布；作为对照，在 8 张 B200（英伟达的数据中心级显卡）上跑完整历史时，速度约为每秒 18.5 帧。上述数字来自一条简短的聚合帖，原始材料中没有独立核实。

telegram · ai\_newz · 10月30日 13:37

**「什么是“世界模型”」** 世界模型（world model）是一类能像“可以玩的视频”那样持续生成画面的模型：你给出文字指令和镜头方向，它就一段接一段地往下演，而不是一次输出一段固定长度的短片。据 Hy-Nomas 在 Hugging Face 上的模型页，它正是靠文字指令和镜头控制来实现这种多轮交互的。同赛道的产品此前多以在线演示或封闭预览的形式出现（如 Odyssey-3），所以这次能否下载到代码和权重，对想自己跑起来的人是实质区别。

**「对实际使用者的影响」** 想自己生成可交互视频，或为机器人搭建训练场景的人，现在可以把这套模型下载到本地，在一张消费级显卡（RTX 4090）上运行，并用自己拍的视频做 LoRA 微调（在已有模型上追加少量训练，让它学会特定画面风格或场景）；官方还提供了现成的电影画面和机器人适配器。需要留意的是，腾讯只公布了 8 块 B200 专业卡、保留完整历史时约 18.5 帧/秒的成绩，单卡模式的速度没有说明；如果制作流程对帧率有要求，最好先等第三方实测单卡速度，再决定是否按这个配置准备硬件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/tencent/Hy-Nomas">tencent / Hy - Nomas · Hugging Face</a></li>
<li><a href="https://www.orcarouter.ai/blog/hy-nomas-vs-odyssey-3">Hy - Nomas vs Odyssey-3: Open Weights vs a Closed Preview</a></li>

</ul>
</details>

**标签**: `#open-weight models`, `#world models`, `#video generation`, `#LoRA fine-tuning`, `#self-hosting`

---

<a id="item-tech-news-10"></a>
### [Habr 文章称 3210 亿参数混合专家模型可跑在单张 RTX 3090 上](https://habr.com/ru/articles/1101852/?utm_campaign=1101852&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

10 月 30 日发表于 Habr 的一篇文章宣称，1250 亿参数的混合专家模型（MoE：每次回答只调用网络中一部分“专家”子模型的大模型）已经能在家用显卡 RTX 5070 上运行，而 3210 亿参数的模型则跑在单张 RTX 3090 配 64 GB 内存的机器上。文章还称，就在 9 月，跑 1250 亿参数的模型还被看作只有机架式服务器用户才玩得起的事。但目前公开的只是文章开头：没有给出模型名称，没有说明显存和内存如何分配，也没有任何实测速度数字。文章承诺在后文解释具体做法并给出真实吞吐量，这些内容不在现有材料中，因此上述说法目前无法核实。

rss · Habr AI · 10月30日 15:38

**「背景：为什么家用显卡能跑大模型」** 混合专家模型（MoE）把一个大模型拆成许多个“专家”子网络，每次回答只调用其中一小部分，所以模型总体可以很大，单次计算却相对轻。配合“专家卸载”（把暂时用不到的专家权重放在内存或硬盘，等需要时再送进显卡），今年 10 月已有公开项目 Strata 展示过相近做法：在 12GB 显存加 64GB 内存的家用电脑上运行 125B（约 1250 亿参数）级 MoE 模型。Habr 这篇预告则称，类似思路已能在家用显卡 RTX 5070 上运行 125B 模型，并在单张 RTX 3090 加 64GB 内存上运行 321B 模型。

**「对想在家跑大模型的人意味着什么」** 判断这类方案能不能实际使用，关键数字是生成速度，也就是每秒能输出多少字，而这个数字恰恰没有出现在文章开头。在读到完整的方法说明和实测数据之前，仅凭“跑得起来”不足以作为购买 RTX 5070 或给机器加内存的依据：能把模型加载进去，和能流畅地一问一答，是两件不同的事。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://runaihome.com/blog/strata-inference-engine-125b-gaming-gpu-guide-2026/">Strata Runs a 125B Model on a 12GB Gaming GPU: Real ...</a></li>
<li><a href="https://stratallm.org/">Strata LLM – Run 125B+ MoE Models on 12GB VRAM Consumer GPUs ...</a></li>
<li><a href="https://getaibook.com/news/strata-moe-offloading-125b-models-on-gaming-pcs/">Strata Runs a 125B Model on a Gaming PC at 94 Tokens Per ...</a></li>

</ul>
</details>

**标签**: `#local-llm-inference`, `#open-weight-models`, `#moe-models`, `#consumer-gpus`, `#quantization-offloading`

---

<a id="item-tech-news-11"></a>
### [FLUX.3 klein 生成 290 张牙医宣传照，作者称花费约 3 美元](https://habr.com/ru/articles/1101804/?utm_campaign=1101804&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位为牙科诊所投放付费广告的营销人员在 Habr 上发文，称自己不再请摄影师给医生拍宣传照，改用图像生成模型 FLUX.3 klein 批量出图：在 ComfyUI 里搭好流程，租用云 GPU 平台 RunPod 运行，一共生成 290 张，花费约 3 美元。按他的说法，诊所原本要为每位医生安排拍摄、付摄影师费用，而且广告素材大约一个月就会“跑疲”，需要不断补新图。需要说明的是，目前能看到的只有文章开头，具体的提示词、参数设置和成片效果都在“阅读全文”之后，无法核实生成图片的质量，也无法独立确认这 3 美元的成本。这是一个从业者自述的案例，不是第三方测评。

rss · Habr AI · 10月30日 13:52

**「背景」** 这条案例把原本要请摄影师到诊所拍医生的流程，换成了在云端租显卡运行图像生成。FLUX.3 klein 是 Black Forest Labs 发布的开放权重图像模型（模型文件可公开下载，能装在自己或租来的机器上运行），可在 ComfyUI 中完成文字生成图片和按指令修改图片；ComfyUI 是用连线搭流程的图形界面，RunPod 则提供云端显卡租用服务。这样就能理解作者为何说 290 张图只花约 3 美元：成本主要变成显卡租用费，而不是摄影师和场地费用。

**「对实际使用意味着什么」** 如果你负责诊所或小企业的广告素材，这条信息给出的参考是：把“拍一次照片”换成“生成几百张图”，成本可能从摄影师报价降到个位数美元外加一点学习时间。但落地前有两个现实问题：一是文章没有公开样图和参数，你无法在动手前判断出图是否够真实、够专业；二是用 AI 生成一位真实医生的形象用于宣传，涉及本人同意和肖像使用的问题，实操中仍需按真人照片的规则处理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.comfy.org/tutorials/flux/flux-3-klein">FLUX 3 Image Klein in ComfyUI: Text-to-Image and Edit</a></li>
<li><a href="https://docs.runpod.io/tutorials/pods/comfyui">Generate images with ComfyUI - Runpod Documentation</a></li>

</ul>
</details>

**标签**: `#FLUX.3`, `#ComfyUI`, `#RunPod`, `#image-generation`, `#cost-efficiency`

---

<a id="item-tech-news-12"></a>
### [俄语教程：在 HuggingFace 上挑选并运行开源模型](https://habr.com/ru/companies/bothub/articles/1101764/?utm_campaign=1101764&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

俄罗斯技术社区 Habr 上，BotHub 发布了一篇面向初学者的 HuggingFace 使用教程，讲的是如何在这个平台上找到模型、判断该选哪个，以及怎样把它跑起来。HuggingFace 是一个集中存放公开人工智能模型和训练数据的网站，常被比作“AI 领域的 GitHub”；作者说上面约有 80 万个模型，新手进去很容易不知道该从哪下手，并把这种体验比作第一次走进 1990 年代的莫斯科批发市场——什么都有，就是没人告诉你怎么开始。需要说明的是，从目前可见的导语部分看，这篇教程没有给出具体模型名称、性能对比数字或经过验证的操作步骤，更接近一篇入门导航。教程正文为俄语。

rss · Habr AI · 10月30日 12:53

**「背景」** HuggingFace 是一个让开发者共享、查找和协作开发机器学习模型与数据集的平台，常被比作“AI 领域的 GitHub”（类似程序员共享代码的网站）。这篇教程称平台上已有约 80 万个模型，但界面默认访客已经熟悉平台的操作方式，因此初学者往往不知道从哪里开始挑选和运行模型。

**「实际影响」** 对想把开源模型下载到自己电脑上运行的中文读者来说，第一个障碍是语言：全文是俄语，而导语里也没有可直接照做的命令清单。可以把它当作了解这个平台有哪些内容、大致怎么分类的读物，但不要指望照着它就能完成一次本地部署；真要动手，多半还得另找中文或英文的分步教程来对照。

**标签**: `#Hugging Face`, `#open-weight models`, `#model selection`, `#local inference`, `#beginner tutorial`

---

<a id="item-tech-news-13"></a>
### [LTX-2.5 视频模型称能在 10GB 显存 RTX 3080 上运行](https://habr.com/ru/articles/1101646/?utm_campaign=1101646&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位 Habr 作者称，已在 Windows 上让 220 亿参数的 LTX-2.5 视频生成模型在自己那张只有 10 GB 显存（显卡上专门用于模型计算的内存）的 RTX 3080 上本地运行，并把它接入了短视频制作流程。参数是模型内部参与计算的数值，数量越多通常模型越大；按文章给出的数字，视频主干网络的权重（训练后保存下来的数值）占 39 GB，负责把文字提示转成模型输入的文本编码器另占 24.5 GB，都远大于 10 GB 显存。但提供的摘要没有交代具体配置、生成速度、画质或可复现步骤，所以这目前只是作者的自述，尚不能独立验证。

rss · Habr AI · 10月30日 11:17

**「为什么 22B 模型装不进 10GB 显存」** LTX-2.5 是 Lightricks 发布的视频生成模型，权重公开可下载；官方发布页把模型按组件拆成多个文件，其中包含一个压缩到 8 位精度（用更少的位数保存每个数值，以缩小体积）的版本。所谓“参数”，指模型内部可调的数值，22B 就是 220 亿个；这些数值在运行时必须放进显卡自带的内存（显存）里，因此仅 39GB 的主体权重就已经远超这块卡 10GB 的容量。文本编码器负责把用户写的提示词转换成模型能处理的形式，它在发布页上是与视频主体模型分开的独立文件。

**「实际影响」** 对想在本地生成视频的人，实际影响是：如果作者之后公开步骤，10 GB 显存的旧显卡可能多一个尝试选项；但在那之前，不应据此购买显卡或把短视频生产流程建立在它上面。现有信息也没有说明生成一条视频要多久、画质能否用于发布，以及这套做法是否适用于其他显卡和 Windows 以外的系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Lightricks/LTX-2.5">Lightricks/ LTX - 2 . 5 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#LTX-2.5`, `#local inference`, `#RTX 3080`, `#video generation`, `#VRAM optimization`

---

<a id="item-tech-news-14"></a>
### [用户称 Claude 在身份验证后停用账号](https://habr.com/ru/companies/aurorium/articles/1101594/?utm_campaign=1101594&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一家反检测浏览器（可伪装浏览器特征、用来管理多个账号的工具）厂商的文章称，近期有 Claude 用户在做完身份验证后账号被停用，相关报告集中在 Reddit；文章把这些封号与用户护照所属国家及 VPN（把上网流量转到其他国家的服务）使用联系起来，但所给摘录在解释具体做法前就结束了。文章还称，Anthropic 的服务规则禁止在特定国家提供或经营服务，却没有明文规定持有某些国家护照的人不能使用；这一区别是当前争议的核心。现阶段可核实的是有用户这样报告，而不是 Anthropic 已公开确认了一套按护照或 VPN 封号的规则。发文方本身销售反检测浏览器，读者应把这层商业背景考虑在内。

rss · Habr AI · 10月30日 10:06

**「背景」** Claude 是 Anthropic 公司的人工智能聊天服务，近期开始要求部分用户完成身份验证，也就是上传护照等证件照片、交由第三方公司 Persona Identities 核对（据 Claude 帮助中心的说明）。10 月 29 日 Meduza 报道，Reddit、X 和 Telegram 上陆续有用户称，自己在提交俄罗斯护照完成验证后账号被封；这篇 Habr 文章正是围绕这些案例讨论。需要说明的是，文章作者是一家销售「反检测浏览器」的厂商，这类工具可以伪装设备和网络特征、方便同时登录多个账号，而文章后半段就是它的产品推广；文中也指出，Claude 的条款禁止在特定国家提供服务，但并未明文规定持哪一国护照就算违规。

**「实际影响」** 对使用 Claude 付费账号的人，具体后果是账号可能在完成验证后立刻无法登录，已付费的服务随之中断；目前公开信息没有说明触发条件、停用时长或恢复流程。若收到验证要求，先确保账号绑定的邮箱和付款方式仍可用，并保留订阅记录，以便之后向客服说明情况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://meduza.io/en/feature/2026/10/29/claude-users-say-their-accounts-were-banned-after-verification-showed-a-russian-passport">Claude users say their accounts were banned after verification ...</a></li>
<li><a href="https://support.claude.com/en/articles/14328960-identity-verification-on-claude">Identity verification on Claude | Claude Help Center</a></li>

</ul>
</details>

**标签**: `#account-bans`, `#anthropic-claude`, `#access-restrictions`, `#identity-verification`, `#anti-detect-browsers`

---

<a id="item-tech-news-15"></a>
### [爱好者把 MSI 笔记本键盘改成独立 USB 键盘](https://habr.com/ru/articles/1101616/?utm_campaign=1101616&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位爱好者把妻子那台 MSI GS75 笔记本上的键盘做成了一把可以插在电脑上独立使用的 USB 键盘，目前是能工作的原型机。成品有 102 个按键、USB Type-C 接口，保留 Fn 键和多媒体组合键，支持 NKRO（全键无冲，同时按下多个键也不会漏报），还带一套自己写的故障诊断功能。做法是先后做了两版以 STM32 微控制器（一种可以自己编程的芯片）为核心的电路板，并自己编写固件，让电脑通过 USB HID 标准（电脑识别键盘、鼠标这类外设的通用协议）把它当成普通键盘。作者说，最难的并不是把板子造出来，而是让每一次按键都被正确识别，为此要处理“幽灵按键”，也就是没人按却被判定为按下的情况。目前公开的只有文章开头部分，电路图、固件代码和零件清单都还没有出现在可见内容里。

rss · Habr DIY · 10月30日 09:23

**「背景：笔记本键盘为何不能直接插上就用」** 笔记本键盘通常没有自己的 USB 控制电路：按键被排成横竖交叉的电信号“矩阵”（靠行列交叉来定位每个按键），再由笔记本主板扫描并转换成按键信号。要把这样的键盘单独使用，就需要用一块可编程的 STM32 微控制器接替主板的角色，并编写 USB HID 固件（设备内置的控制软件），让电脑把它识别为普通 USB 键盘。作者正是这样做的，因此原型保留了 102 个按键，并支持 Fn（功能组合键）和多媒体组合键。

**「实际影响」** 对舍不得换掉某款笔记本键盘的人来说，这个项目说明笔记本键盘本身只是一组排成行列的按键开关，可以用另一块控制板重新驱动，不必依赖原装主板。但它属于一次性的个人制作：需要自己测出键盘排线的接口定义、焊接电路板并写入固件，文中也没有给出可直接照做的图纸或固件，所以既买不到成品，也很难原样搬到别的笔记本型号上。

**标签**: `#hardware`, `#STM32`, `#keyboard`, `#USB-HID`, `#DIY`

---

<a id="item-tech-news-16"></a>
### [开源项目声称用 AI 将 Jira 工单自动推进到已审核的代码合并请求](https://github.com/pruthvidarji1993/ai-automation-jira) ⭐️ 5.0/10

GitHub 上出现一个名为 ai-automation-jira 的开源项目，声称能把 Jira（团队用来记录任务和缺陷的工单系统）中的一张工单，经由 9 个阶段的 AI 处理，一路推进到“已审查的合并请求”（pull request，即把改好的代码提交给项目、等待审核并入的请求）。项目说明称它支持 Claude Code 与 GitHub Copilot 两种 AI 编程助手，并在“计划（Plan）”和“代码差异（Diff）”两处设置人工审核点，可选 Opus、Sonnet 两档 Claude 模型；代码用 Python 编写，采用 MIT 宽松开源许可证。但该项目目前只有 1 个收藏（star）、0 次复制（fork）、2 个未关闭的问题报告，来源也只是一段推广性质的简介，没有代码片段、演示或运行结果，9 阶段流程是否真的可用尚未得到验证。对使用这类编码助手的人来说，它可以作为一个待观察的自动化思路，但现阶段不宜当作成熟工具采用。

telegram · aipluscn · 10月30日 05:07

**「先弄清两个工具和一类助手」** 先认识两个日常工具：Jira 是软件团队登记和跟踪任务的系统，每一条任务通常叫“工单”（ticket）；拉取请求（pull request，简称 PR）是开发者把改好的代码提交上去、请同事逐行查看并同意后才并入主代码库的请求。Claude Code 和 GitHub Copilot 是能读懂代码库、并按指令直接动手改代码的 AI 编程助手，通常装在开发者自己的开发环境里。这个仓库想做的，是用一条分成 9 个阶段的流程把三者串起来：从 Jira 工单出发，在“制定方案”和“查看代码改动”两个环节要求真人确认，最后产出一个经过审核的 PR。

**「对使用者的实际影响」** 对正在用 AI 编程助手写代码的团队来说，这个项目想做的事是把「从 Jira 任务单到提交审核的代码改动」串成一条流水线，并在两处停下来等人确认：一处是 AI 给出的修改计划，一处是最终代码差异。也就是说，它不会让 AI 直接合并代码，审核仍在人手里。但项目目前只有 1 个星标、0 个 fork（别人复制去参与开发的数量），除宣传说明外没有代码示例或运行结果作证，现阶段只适合当作流程思路参考，不建议接进团队的正式开发流程。真要用还得先确认自己有 Claude Code 或 GitHub Copilot 的付费账号，并按要求以插件方式安装。

**标签**: `#Claude Code`, `#GitHub Copilot`, `#Jira`, `#AI workflow automation`, `#developer tooling`

---

<a id="item-tech-news-17"></a>
### [DeepSeek 官网代码出现“Cyber”模型申请入口，需企业资质](https://x.com/ProbiusOfficial/status/2116001318053777661) ⭐️ 5.0/10

有用户在 DeepSeek 官网的 JavaScript（网页里运行的脚本代码，普通访客看不到）中发现了一个与“Cyber”有关的模型申请入口。据这条爆料，正式申请渠道要求申请方具备企业身份，并提交授权书、营业执照等材料；此外还有一条个人特邀渠道，但具体条件不明。该消息来自社交平台 X 上的用户 ProbiusOfficial，经 Telegram 频道转发，DeepSeek 官方尚未确认这个模型的存在。爆料没有说明模型的能力、价格、使用额度或上线时间，“Cyber”也可能只是内部代号而非最终名称。

telegram · zaihuapd · 10月30日 05:45

**「背景」** “官网 JavaScript 里的申请入口”，指的是网页里供浏览器执行的脚本代码——普通访客在页面上看不到，但查看网页源码就能搜到其中的文字。DeepSeek 过去有过“官网先露出、官方后说明”的先例：据 DataLearnerAI 4 月 8 日的报道，其官网模型曾被怀疑在未发公告的情况下更新，实测输入上限达 100 万 tokens（token 是模型处理文字的最小单位，可粗略理解为字数），但当时也未经官方确认。至于企业申请通道要求营业执照和授权书，通常是为了确认申请方是公司而非个人，这类限制多见于面向机构开放、额度或用途受控的服务。

**「对普通用户意味着什么」** 如果爆料属实，这将是 DeepSeek 少见的、把新模型入口放在企业验证之后的安排，普通个人用户无法直接申请，只能等特邀渠道或后续开放。目前没有任何可以操作的入口，也没有官方页面可供核对，因此不建议向非官方渠道提交营业执照、授权书这类材料。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.datalearner.com/blog/deepseek-new-model-not-v3-2-confirmed">DeepSeek 官 网 模 型 疑似更新为 DeepSeek ... | DataLearnerAI</a></li>

</ul>
</details>

**标签**: `#deepseek`, `#model-release-rumor`, `#access-restrictions`, `#enterprise-access`, `#ai-news`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [DeepSeek 据报完成第二轮融资 1055 亿元，估值超 6155 亿元](https://www.theinformation.com/articles/behind-deepseeks-16-billion-funding-chinese-tech-titans-state-players) ⭐️ 7.0/10

据 The Information 报道，DeepSeek 在第二轮融资中募资 1055 亿元人民币，估值超过 6155 亿元人民币；报道称近 30 家投资方参与，其中国资背景投资者出资约占 27%，高于今年 6 月首轮约 510 亿元融资时的 2%。该消息经 Telegram 聚合账号转述，DeepSeek 尚未公开确认。

telegram · zaihuapd · 10月30日 12:37

**「背景」** 这是 DeepSeek 的第二轮融资，首轮于今年 6 月完成，规模约 510 亿元，当时有国资背景的投资者仅贡献约 2% 的资金，低于本轮的约 27%。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theinformation.com/articles/behind-deepseeks-16-billion-funding-chinese-tech-titans-state-players">Behind DeepSeek’s $16 Billion Funding: Chinese Tech Titans ...</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI financing`, `#China tech`, `#startup valuation`, `#state-backed investment`

---

<a id="item-finance-news-2"></a>
### [四家日系车企 4 至 9 月在华产量同比下降 32%](https://weibo.com/1642634100/Rp6qUwLKa) ⭐️ 7.0/10

2026 年 4 月至 9 月，丰田、本田、日产和马自达在华合计产量约 102 万辆，同比下降 32%，创 2008 年以来同期新低，不足 2020 年同期峰值的四成。本田还计划将其在华燃油车年产能从 149 万辆削减至 100 万辆。

telegram · zaihuapd · 10月30日 13:38

**「背景」** 据市场分析，日系车在华市场份额此前五年间已从 23.1%降至约 9.6%，其中丰田依靠混动车型勉强维持增长，本田和日产销量大幅下滑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://post.smzdm.com/p/a95lm43o/">post.smzdm.com/p/a95lm43o</a></li>

</ul>
</details>

**标签**: `#Japanese automakers`, `#China auto production`, `#Honda`, `#capacity cuts`, `#auto industry`

---

<a id="item-finance-news-3"></a>
### [法国国民议会通过数据流量税修正案](https://www.assemblee-nationale.fr/dyn/17/amendements/3210A/AN/1358) ⭐️ 7.0/10

法国国民议会通过一项预算修正案，拟对内容供应商向互联网用户发送的数据按每 GB 0.055 欧元征税，并设置与企业营业额挂钩的税额上限。提案方预计该税每年可带来 100 亿欧元税收，但修正案仍须经过后续立法程序、可能被修改或删除，企业是否将成本转嫁给消费者也尚不确定。

telegram · zaihuapd · 10月31日 02:05

**「背景」** 这项修正案由社会党在预算辩论中提出并获得通过，税额按互联网接入运营商计量的数据流量（以 GB 为单位）计算，由内容供应商缴纳。

**「潜在影响」** 由于税额按传输的数据流量而非营收计算，向法国用户传输大量数据的视频、云服务和社交平台（如 Google、Meta、Amazon、Netflix）将相对承担更重的税负；用户订阅费用是否上涨取决于企业是否转嫁成本，目前尚不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://next.ink/264997/le-parti-socialiste-a-fait-passer-sa-taxe-au-gigaoctet-a-lassemblee-nationale/">Le Parti socialiste a fait passer sa taxe au gigaoctet à l’ Assemblée ...</a></li>
<li><a href="https://www.digitalbusiness.africa/france-les-deputes-adoptent-une-taxe-de-0055-euro-par-gigaoctet-de-donnees-envoyees-par-google-meta-netflix-et-les-geants-du-numerique/">France : les députés adoptent une taxe de 0,055 euro par ...</a></li>

</ul>
</details>

**标签**: `#法国`, `#数据流量税`, `#财政预算`, `#数字政策`, `#科技监管`

---