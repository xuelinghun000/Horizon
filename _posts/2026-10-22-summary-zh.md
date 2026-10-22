---
layout: default
title: "Horizon Summary: 2026-10-22 (ZH)"
date: 2026-10-22
lang: zh
---

> 从 142 条内容中筛选出 22 条重要资讯。

---

**科技新闻**
1. [PyPI 上的 LiteLLM 1.107.0 被植入窃取凭据的后门](#item-tech-news-1) ⭐️ 8.0/10
2. [Anthropic 在美国小范围测试主动型助手 Claude Duet](#item-tech-news-2) ⭐️ 8.0/10
3. [Ollama v0.40.8 新增 400 亿参数编程模型 Flint，暂仅支持 macOS](#item-tech-news-3) ⭐️ 7.0/10
4. [OpenAI 调整缓存：Codex 闲置后免重写，API 可选 12 小时](#item-tech-news-4) ⭐️ 7.0/10
5. [开源面板 Slightly Parallel：用一个网页管理多个 AI 编程项目](#item-tech-news-5) ⭐️ 6.0/10
6. [免费不联网的会议转写：T-one 出实时草稿，GigaAM 会后重写](#item-tech-news-6) ⭐️ 6.0/10
7. [Railway 凭证疑泄露，LiteLLM 1.107.0 遭下架](#item-tech-news-7) ⭐️ 6.0/10
8. [第三方插件 Hey 为 Claude Code 加上 Markdown 任务清单与 AI 估算](#item-tech-news-8) ⭐️ 6.0/10
9. [fal 与 BFL 发布 FLUX 3 Max，10 秒 720p 视频约 12.45 秒生成](#item-tech-news-9) ⭐️ 6.0/10
10. [new-api 发布 v1.0.0-rc.46，修复安全漏洞并调整计费](#item-tech-news-10) ⭐️ 5.0/10
11. [SemiAnalysis 发文分析华为升腾 950PR 与 DeepSeek 模型适配](#item-tech-news-11) ⭐️ 5.0/10
12. [Hugging Face 博客称精简小模型词表可省 77% 推理成本](#item-tech-news-12) ⭐️ 5.0/10
13. [IBM 发布 Granite Speech 5.0 语音模型](#item-tech-news-13) ⭐️ 5.0/10
14. [开发者用 AI 助手 Claude 花六周复活停产的 Hello Sense 睡眠追踪器](#item-tech-news-14) ⭐️ 5.0/10
15. [有人把银行卡、手机和 200 多个工具接口交给 AI 助手做实测](#item-tech-news-15) ⭐️ 5.0/10
16. [Habr 教程：拆解 ReAct 智能体的模型、工具与循环](#item-tech-news-16) ⭐️ 5.0/10
17. [ESP8266 单片机跑 3D 游戏：作者拆解光线投射代码](#item-tech-news-17) ⭐️ 5.0/10
18. [OpenAI 模型将进入 Google Cloud 企业模型目录](#item-tech-news-18) ⭐️ 5.0/10
19. [未经证实：OpenAI 模型将进入谷歌 Antigravity](#item-tech-news-19) ⭐️ 5.0/10
20. [AI 编码智能体技能包上线：号称支持多平台，细节有限](#item-tech-news-20) ⭐️ 5.0/10
21. [有帖子称主流网站开始封堵 AI 智能体，但未给出可核实来源](#item-tech-news-21) ⭐️ 5.0/10
22. [Anthropic 的 Opus 5.5 模型服务出现异常，官方称已修复并在监控](#item-tech-news-22) ⭐️ 5.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [PyPI 上的 LiteLLM 1.107.0 被植入窃取凭据的后门](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) ⭐️ 8.0/10

据 safedep.io 发布的分析，Python 软件包仓库 PyPI 上的 LiteLLM 1.107.0 版本被植入恶意代码，安装后会窃取凭据（API 密钥、账号密码这类能证明身份的东西），并留下后门（让攻击者能远程进入系统的入口）。LiteLLM 是一个开源的大模型接口网关，作用是把 OpenAI、Anthropic 等不同厂商的模型调用统一成一套接口，很多团队把它部署在服务器上转发请求。该分析指出，使用者应立刻避开或锁定这一版本，并更换（轮换）所有可能已经暴露的 API 密钥。目前公开信息没有说明这个版本在 PyPI 上架了多久、被下载了多少次，也没有说明它是否已被下架。

hackernews · abhisek · 10月21日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=50181114)

**「背景」** LiteLLM 是一个开源的 Python 软件包，常被开发者当作“中间层”使用：把它装在自己的服务器上，就能用同一套接口把请求转发给 OpenAI、Anthropic 等不同厂商的模型，因此它手里往往同时握着多家服务的密钥。PyPI 是 Python 的公共软件仓库，用户执行安装命令时，仓库里的代码会直接在自己的机器上运行——一旦发布账号被盗，攻击者就能把恶意代码塞进正式版本，安装者不需要做错任何事也会中招。

**「实际影响」** 对把 LiteLLM 当作统一入口的团队来说，风险不止于装了这个包的那台机器：网关通常集中保存着多家模型厂商的 API 密钥，一旦被窃，攻击者可以直接拿这些密钥调用模型并产生费用。可以采取的动作是先把版本固定在此前一个可信版本上，再按密钥清单逐个更换，而不是只换最近用过的几个。

**「社区讨论」** 评论者 rsanheim 称这已是 LiteLLM 近一两年内第二次重大供应链攻击，并说上一次发生在今年 3 月；threecheese 则提到攻击者获取了 3 名开发者的 GitHub 凭据，建议把 LiteLLM 固定在此版本之前的版本上，直到情况明朗。linsomniac 推荐使用 canarytokens.org 这类“诱饵令牌”服务，在密钥被他人使用时收到提醒。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/">Compromised LiteLLM 1.107.0 on PyPI Installs a Credential ...</a></li>
<li><a href="https://github.com/BerriAI/litellm/issues/47826">[SECURITY] litellm 1.107.0 compromised (PyPI removed ... - GitHub</a></li>

</ul>
</details>

**标签**: `#LiteLLM`, `#supply-chain attack`, `#credential theft`, `#PyPI`, `#API proxy`

---

<a id="item-tech-news-2"></a>
### [Anthropic 在美国小范围测试主动型助手 Claude Duet](https://claude.com/resources/articles/claude-duet) ⭐️ 8.0/10

Anthropic 已开启 Claude Duet 的早期测试（研究预览），这是一款会主动推送每日简报、并在后台替用户执行任务的独立 AI 助手应用，已上线 iOS、Android 和 claude.ai。测试目前只面向美国的 Pro 和 Max 付费订阅用户，且需加入等候名单；据来源称，它基于 Claude Opus 5.5 模型，并与其他 Claude 产品共用订阅的使用额度。涉及发送消息、付款、签署文件或删除内容时，它会先展示将要执行的操作并等待用户批准；证券交易和账户间转账则即使获得授权也不允许。

telegram · zaihuapd · 10月22日 00:02

**「背景」** 普通的聊天机器人要等用户提问才回应；这里说的“代理”（能自己拆解任务、调用工具并连续执行多步的 AI 程序）则被允许在后台按目标自行推进，所以厂商会用“关键操作前先批准”和禁止某些操作来控制风险。Claude 是 Anthropic 的订阅制聊天助手，Pro 和 Max 是它的两档付费方案。

**「对订阅用户的实际影响」** 对已经付费的 Pro 和 Max 用户来说，最直接的变化是 Duet 与 Claude 其他产品共用同一份订阅额度：让它在后台跑任务会占用你平时对话的用量，重度使用前最好先看看自己还剩多少。另外，凡是发消息、付款、签字、删除这类操作，它都会先停下来等你确认，所以它更像一个随时待命、但要你点头才动手的助手，而不是完全放手不管；美国以外的用户目前还只能等。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claude.com/resources/articles/claude-duet">Introducing Claude Duet | Claude by Anthropic</a></li>
<li><a href="https://www.testingcatalog.com/claude-duet/">Anthropic opens Claude Duet preview for US Pro and Max users</a></li>

</ul>
</details>

**标签**: `#Claude`, `#Anthropic`, `#AI agents`, `#subscription access`, `#research preview`

---

<a id="item-tech-news-3"></a>
### [Ollama v0.40.8 新增 400 亿参数编程模型 Flint，暂仅支持 macOS](https://github.com/ollama/ollama/releases/tag/v0.40.8) ⭐️ 7.0/10

Ollama v0.40.8 于 2026 年 10 月 21 日发布，新增 Recursive 公司的编程模型 Flint；Ollama 是一个在自己电脑上运行 AI 模型的工具，Mac 用户现在可用 \`ollama run flint\` 直接下载并运行。Flint 以 Apache 2.0 许可证发布（一种允许公开使用、修改和商用的开源许可证），是一个 400 亿参数的混合专家模型（把模型拆成多个子网络，每次只启用一部分），每个词元约启用 25 亿参数，上下文窗口为 26.2 万词元（词元是模型处理文字的基本单位），面向跨文件理解代码、追踪缺陷、实现功能和补测试等任务。Recursive 自行公布的评测成绩是 Terminal-Bench 2.1 54.9%、SWE-bench Verified 74.2%，这两项都是编程任务测试集，目前没有独立验证。当前版本只支持 macOS，其他 GPU 支持要等后续版本。

github · github-actions\[bot\] · 10月21日 16:20

**「背景」** Ollama 是一个把开放权重的模型下载到本地电脑上运行的工具；开放权重指训练好的模型参数可以公开获取，用户不必依赖云端服务。Flint 是混合专家模型：总参数约 400 亿个，但每生成一小段文本只调用其中约 25 亿个，因此总规模大、实际计算量相对小。上下文窗口指模型一次能读入并处理的文本量，262K 表示它能容纳很长的代码和操作记录，适合跨文件的任务。

**「实际影响」** 对已经在 Mac 上用 Ollama 辅助写代码的人，Flint 可以马上用一条命令试用，长上下文适合让它一次读入多个代码文件；但 Windows、Linux 和其他显卡用户暂时用不上。若准备把它放进正式开发流程，应先把厂商自报的分数当作参考，在自己的代码库上试跑后再决定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/recursive/flint-v1.0:free">Flint (free) - API Pricing &amp; Providers | OpenRouter</a></li>
<li><a href="https://huggingface.co/RecursiveSI/flint">RecursiveSI/ flint · Hugging Face</a></li>

</ul>
</details>

**标签**: `#ollama`, `#open-weight models`, `#coding models`, `#local inference`, `#model release`

---

<a id="item-tech-news-4"></a>
### [OpenAI 调整缓存：Codex 闲置后免重写，API 可选 12 小时](https://telegram.me/ai_newz/4813) ⭐️ 7.0/10

据 Telegram 频道 ai\_newz 报道，OpenAI 调整了提示缓存（把对话中重复使用的前文暂存起来，下次不必重新处理）：订阅用户使用编程工具 Codex 和 ChatGPT Work 时，缓存会一直保留，离开几小时后再继续同一会话，也不用重新写入缓存、消耗额度。API（让其他软件直接调用模型的接口）用户则新增了保留 12 小时的缓存档位，其缓存写入价格是现有 30 分钟档的两倍。报道没有给出具体价格，也没有说明这些改动是否已向所有用户开放。

telegram · ai\_newz · 10月21日 03:44

**「背景」** 提示缓存（prompt caching）不是让模型“记住”对话，而是把重复出现的输入内容暂存起来，下次直接复用，省去重新处理和计费；OpenAI 在 2024 年 10 月上线这项功能时，对复用部分给出五折优惠。此前 API 的缓存写入档位是 30 分钟，这次新增 12 小时档；按这条消息的说法，Codex 和 Work 的会话缓存还会一直保留。

**「实际影响」** 对经常中断再回来的 Codex 用户，最直接的变化是闲置时间不再白白吃掉用量限额；对 API 用户，12 小时档适合一天内反复复用同一段很长输入的场景，如果两次使用间隔很短，按两倍价格写入缓存可能反而更贵。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/api-prompt-caching/">Prompt Caching in the API - OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Codex`, `#prompt caching`, `#API pricing`, `#rate limits`

---

<a id="item-tech-news-5"></a>
### [开源面板 Slightly Parallel：用一个网页管理多个 AI 编程项目](https://habr.com/ru/articles/1097130/?utm_campaign=1097130&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

Habr 作者 nmar33 发布了一个名为 Slightly Parallel 的开源工具，由本地服务器加网页界面组成，用来管理同时进行的多个项目——这些项目里的代码主要由 AI 编程智能体（能自己读写代码、执行命令的 AI 程序）来写。它面向独立开发者，以及经常使用 Claude Code、Codex、OpenCode 这三款编程智能体的人，作者表示之后还计划支持 ZCode。工具可在 Windows、Linux 和 macOS 上运行，代码放在 GitHub 上公开。不过这篇发布文本身只是一则简短公告：除了一段演示动图和仓库链接，没有功能清单、安装步骤，也没有成熟度或使用情况的说明。

rss · Habr AI · 10月21日 09:02

**「背景」** 编程智能体（在终端里运行、能自己读写项目文件并执行命令的 AI 程序）通常一次只服务一个项目：Claude Code、Codex、OpenCode 各自在命令行里跑，项目一多，就很难看清每个项目里到底发生了什么。作者在代码仓库里把 Slightly Parallel 描述为“跑在一台笔记本上的自托管面板”，用来汇总这几个工具在各自项目里的动作；其中 OpenCode 是开源的终端编程智能体，同时也有桌面版和编辑器插件版本。所谓“本地服务器 + 网页界面”，是指程序装在自己电脑上、用浏览器打开页面来操作，项目代码不必上传到别人的服务器。

**「对使用者的实际影响」** 想尝试的人目前只能自己打开 GitHub 仓库，从代码和说明里判断它是否合用，因为文章没有交代怎么安装、需要什么环境。在缺少这些信息的情况下，比较稳妥的做法是先拿一个不重要的项目试跑，确认它和你正在用的编程智能体配合正常，再考虑放到日常开发里。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/NMar33/slightly-parallel">GitHub - NMar 33 / slightly - parallel : A dashboard for coding agents ...</a></li>
<li><a href="https://opencode.ai/docs">Intro | AI coding agent built for the terminal</a></li>

</ul>
</details>

**标签**: `#coding-agents`, `#claude-code`, `#developer-tooling`, `#open-source`, `#multi-project-workflow`

---

<a id="item-tech-news-6"></a>
### [免费不联网的会议转写：T-one 出实时草稿，GigaAM 会后重写](https://habr.com/ru/articles/1096758/?utm_campaign=1096758&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一位作者在 Habr 上公开了一套完全在本机运行、不把录音上传到云端的会议转写方案：开会时用 T-one 模型（一种把语音变成文字的软件）生成延迟约 1 秒的草稿字幕，会议结束后再用 GigaAM 模型把整段录音重新转写一遍，得到质量更好的定稿。他在自己 2 小时 21 分钟的工作通话上统计，定稿改掉了草稿中 11.9% 的词，同时把 1.5% 原本正确的词改错。在他手动复听的一段录音里，定稿达到了云端转写服务 Deepgram 的水平；但他也发现，用来对照的人工转写在每四个有争议的地方就有一个是错的，而同事用着有效的“再加一个模型”的做法，在他这里反而更差。文章附了复现用的代码仓库链接和费用计算。

rss · Habr AI · 10月21日 04:16

**「背景」** 语音转文字工具通常有两种做法：把录音传到云端（外部厂商的服务器）处理，或者直接在自己的电脑上运行识别模型（经过训练、能把声音转成文字的软件）。作者在上一篇文章中测试过 T-one，发现它能以约一秒的延迟生成实时字幕，但不加标点，准确率也明显不如云端服务；这次他在这套流程后面再接上 GigaAM，等会议结束后用整段录音重新转写，把实时生成的草稿字幕整理成更准确的版本。

**「实际影响」** 对想把会议记录留在本地、不交给云端服务的人来说，这套方案的实际含义是：实时字幕只能当草稿用，事后仍要花时间校对——按作者的数据，大约每八个词就有一个会被改写，另有一小部分会被改错。想照搬的人还要注意，作者自己测试的“多加一个模型”的级联方案并没有带来改善，效果得在自己的录音上验证。

**标签**: `#speech-to-text`, `#self-hosted`, `#GigaAM`, `#T-one`, `#workflow`

---

<a id="item-tech-news-7"></a>
### [Railway 凭证疑泄露，LiteLLM 1.107.0 遭下架](https://linux.do/u/lingo) ⭐️ 6.0/10

一篇论坛汇总帖称，Railway（一个用来部署和运行应用的云平台）检测到存储客户环境变量的系统出现异常活动，部署已暂停，并建议用户轮换（作废旧凭证、换新的）全部凭证，包括 API 密钥（调用服务时用的密码式凭证）。同一帖子还称，LiteLLM（一个常用来统一转发各家 AI 模型请求的软件）的 1.107.0 版本被植入恶意代码，已从 PyPI（Python 的公共软件包仓库）下架，帖子将此事称为供应链攻击（在别人依赖的软件包里植入恶意代码）。这些说法来自论坛转述，帖子没有给出可独立核实的细节；使用 Railway 托管应用或项目里用到 LiteLLM 1.107.0 的人，应优先检查密钥和版本。

telegram · linuxdo\_tg · 10月21日 23:17

**「背景」** LiteLLM 是用于把应用接到不同 AI 模型服务上的中间层软件；PyPI 是 Python 的公共软件包仓库，开发者从那里安装这类组件。供应链攻击指攻击者污染正规软件包，让恶意代码随安装进入系统。Railway 是让开发者部署应用并集中保存配置的云平台，这些配置以“环境变量”（程序运行时读取的键值，常放 API key 和密码）的形式存放。

**「实际影响」** 如果你用 Railway 托管应用，应把存放在环境变量里的 API 密钥、登录密码等视为可能已暴露，尽快到各服务商后台作废并重新生成，再更新部署配置；如果项目里用到 LiteLLM，先避开 1.107.0 版本，等官方说明后再决定是否升级。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/litellm-compromised-in-supply-chain.html">LiteLLM Compromised in Supply Chain Attack Delivering Credential...</a></li>
<li><a href="https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/">Compromised LiteLLM 1 . 107 . 0 on PyPI Installs a Credential Stealer...</a></li>
<li><a href="https://blog.railway.com/p/security-disclosure-wednesday-october-21st">Security Disclosure: Wednesday October 21st | Railway Blog</a></li>

</ul>
</details>

**标签**: `#supply-chain-attack`, `#LiteLLM`, `#API keys and credentials`, `#security advisory`, `#Railway`

---

<a id="item-tech-news-8"></a>
### [第三方插件 Hey 为 Claude Code 加上 Markdown 任务清单与 AI 估算](https://github.com/keenkim1202/Hey) ⭐️ 6.0/10

一个名为 Hey 的第三方插件已上架 Claude Code 的插件市场，为这款由 Anthropic 提供的命令行编程助手（在终端里用自然语言让 AI 读写代码的工具）加上基于 Markdown（用简单符号排版的纯文本格式）的任务清单，以及由模型给出的任务估算。安装后可以用 /hey-ledger、/wassup 等命令记录任务和日志；脚本部分只用 Python 标准库、不依赖外部库，另一部分“技能”由模型读取后用来执行任务和估算。该插件由个人开发者发布，并非 Anthropic 官方功能，来源没有给出具体安装步骤、版本号，也没有提供任何证据说明它的估算是否准确、是否好用。

telegram · aipluscn · 10月21日 07:10

**「背景」** Claude Code 是运行在终端里的 AI 编程助手，用户用日常语言让它读写代码、执行命令。插件是给它加装额外功能的小程序，一般从内置的插件市场一键安装。Hey 这类工具把 Markdown（一种用纯文本写标题和列表的轻量格式）文件当作任务账本，一天的任务都记在同一个文件里；据其 GitHub 项目页的描述，早晚的简报与记录、以及时间估算都由脚本算出，模型只负责读取和执行。

**「实际影响」** 想试用的人需要通过 Claude Code 的插件市场安装；按官方插件仓库的说明，第三方和社区插件被单独归在 external\_plugins 一类，与官方插件分开列出，安装前值得先看清来源。Hey 的脚本只用 Python 标准库，因此电脑上装有 Python 就能运行，不必再装额外依赖；但帖子没有给出任何估算准确度的证据，模型给出的工时和任务拆分只适合当作参考，仍要自己核对。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/topics/task-management?l=python&amp;o=desc&amp;s=updated">task-management · GitHub Topics · GitHub</a></li>
<li><a href="https://claude.com/marketplace/plugins">Plugins | Claude Marketplace | Claude by Anthropic</a></li>
<li><a href="https://github.com/anthropics/claude-plugins-official">GitHub - anthropics/ claude - plugins -official: Official...</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#developer tooling`, `#plugins`, `#task management`, `#open source`

---

<a id="item-tech-news-9"></a>
### [fal 与 BFL 发布 FLUX 3 Max，10 秒 720p 视频约 12.45 秒生成](https://fal.ai/flux-3-max) ⭐️ 6.0/10

fal 与模型开发方 BFL 发布了 FLUX 3 Max，这是一个可根据文字或图片生成带声音视频的模型，并在 fal 平台上提供试用。fal 称，生成一段 10 秒、720p 的视频只需 12.45 秒，而对比模型 Seedance 2.5 在同一测试中需要 277.8 秒，约快 22 倍；这是 fal 自家测出的结果，不是独立复测。价格方面，11 月 7 日前 720p 视频按每秒 0.0425 美元计费，10 秒片段约 0.425 美元，促销结束后同样片段为 1.70 美元。评测机构 Artificial Analysis 的图像生视频（用图片生成视频）排行榜把 FLUX 3 Max 列在领先组，与 Seedance 2.5 和 MiniMax H3 相邻。

telegram · ai\_newz · 10月21日 18:35

**「背景」** FLUX 是 BFL 的模型系列，fal 是提供模型云端运行服务的平台；用户不必自己准备显卡，就能调用模型生成内容。这里说的“推理”，就是让训练好的模型实际执行生成任务的过程，这次加速缩短的正是从提交文字或图片到拿到视频的等待时间。

**「实际影响」** 如果你打算试用，11 月 7 日是明确的成本分界点：此前一条 10 秒 720p 片段约 0.425 美元，之后为 1.70 美元，约贵四倍。速度数字来自 fal 自家测试，实际体验可能因使用条件不同而有差异，不能把它当作独立验证过的保证。

**标签**: `#FLUX`, `#video generation`, `#fal.ai`, `#pricing`, `#model release`

---

<a id="item-tech-news-10"></a>
### [new-api 发布 v1.0.0-rc.46，修复安全漏洞并调整计费](https://github.com/QuantumNous/new-api/releases/tag/v1.0.0-rc.46) ⭐️ 5.0/10

自己搭建的 API 中转面板（把多个模型服务商的接口接到一起、自己管理密钥和用量的工具）new-api 发布 v1.0.0-rc.46 候选版（正式版前的测试版本），主要变化是修复公开漏洞 CVE-2026-111943，并把运行环境换成 Go 1.26.10（开发该软件所用的编程语言版本）。这一版在检查网站证书时会拒绝一小批已不再受信任的中间证书（证书链中用来证明服务器身份的中间凭证）；从源码自行编译的人也必须使用 Go 1.26.10。它还新增用 Resend（一家邮件发送服务）代替 SMTP 发信、在数据看板显示缓存用量（请求中命中缓存的 token 数量，token 是模型处理文字时的计费单位），并支持阿里云百炼的 qwen3-vl-embedding 多模态向量模型（把文字和图片转成可比较的数值向量，常用于搜索和推荐）。计费方面，它修复了任务换到另一个服务商重试时仍按上一次价格扣费的问题：更贵的渠道会先补足预扣，余额不够就不发出请求；同时修复可灵（Kling，视频生成服务）不接受单个调用密钥、DeepSeek 余额显示为 0 等问题。

github · Calcium-Ion · 10月21日 16:25

**「背景」** new-api 是一个可以自己部署的“中转面板”：它把各家大模型的接口统一成一套，方便团队分发密钥、记录用量和计费，本身用 Go 语言编写。CVE-2026-111943 是 Go 标准库证书校验环节的一个公开漏洞编号——八把 eMudhra 中间证书（介于根证书和网站证书之间、用来搭起信任链的一层证书）的私钥被泄露，而旧版 Go 在系统根证书库没有及时更新时，可能仍然接受由这些已不可信的中间证书签出的证书，让攻击者有机会冒充服务器、窃听加密通信。因此这次的修复方式不是改 new-api 自己的代码，而是把编译时用的 Go 升到 1.26.10。

**「实际影响」** 如果你自己运行 new-api，应尽快升级；从源码编译的还要把 Go 工具链换成 1.26.10。升级后证书校验更严，仍在使用那批旧中间证书的上游模型服务可能连接失败，需要先确认；任务换渠道重试的计费也会先补预扣，余额不足时请求不会发出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://app.opencve.io/cve/CVE-2026-111943">CVE-2026-111943 - Vulnerability Details - OpenCVE</a></li>
<li><a href="https://access.redhat.com/security/cve/cve-2026-111943">CVE-2026-111943 - Red Hat Customer Portal</a></li>
<li><a href="https://socprime.com/blog/cve-2026-111943-analysis/">CVE-2026-111943: eMudhra CA Key Compromise - socprime.com</a></li>

</ul>
</details>

**标签**: `#api-relay`, `#security-cve`, `#release-notes`, `#self-hosted`, `#qwen`

---

<a id="item-tech-news-11"></a>
### [SemiAnalysis 发文分析华为升腾 950PR 与 DeepSeek 模型适配](https://newsletter.semianalysis.com/p/huawei-deepseek) ⭐️ 5.0/10

SemiAnalysis 于 10 月 21 日发布一篇分析文章，主题是华为与 DeepSeek 之间的相互配合，内容涵盖三部分：对华为升腾 950PR 芯片的小型性能测试（microbenchmark，即针对特定运算跑分，结果不等于真实业务中的表现）、对 DeepSeek 模型 DSv4.1 Flash 的分析，以及 DeepSeek 对升腾芯片的支持情况。目前可获取的内容只有文章的小节标题，没有给出具体跑分数字、价格、供货量或上线时间，因此文中这些结论都无法核实。升腾是华为自研的 AI 芯片系列，DeepSeek 是中国的 AI 模型开发团队；所谓“支持升腾”，指模型可以直接在华为芯片上运行，而不必依赖英伟达的显卡。

rss · Semianalysis · 10月21日 17:34

**「背景」** 华为的升腾（Ascend）是英伟达显卡之外的一条国产 AI 芯片路线，DeepSeek 则是中国的大模型团队；模型要在升腾上跑起来需要专门的软件适配，并非插上就能用。据 dev.to 上的一篇分析文章，DeepSeek 于 2026 年 4 月 24 日发布的 V4 是首个在升腾 950PR 上完整验证推理（让训练好的模型实际回答问题）的顶级模型。SemiAnalysis 这篇通讯延续这条线索，对 950PR 做微基准测试（用小程序测芯片单项性能），并分析被称为 DSv4.1 Flash 的 DeepSeek 模型。

**「对调用 DeepSeek 接口的人意味着什么」** 对通过接口调用 DeepSeek 的开发者来说，需要留意模型名称的变化：据 DeepSeek 接口文档，旧的 deepseek-v4-flash 和 deepseek-v4-flash-vision-exp 这两个名称仍然可以照常调用，但对应的模型已经下线，请求会转由 DeepSeek-V4.1-Flash-1017 处理，并按 Flash 的价格计费。也就是说，代码里不改模型名不会报错，但实际回答问题的已经是另一个模型；如果应用依赖旧模型的具体输出表现，就需要自己重新验证结果是否仍然符合预期。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dev.to/lanternproton/deepseek-v4-on-huaweis-ascend-950-a-real-stress-test-for-chinas-ai-chip-ecosystem-ook">DeepSeek V4 on Huawei&#x27;s Ascend 950: A Real Stress Test for ...</a></li>
<li><a href="https://api-docs.deepseek.com/quick_start/pricing?tool=deepseek">Models &amp; Pricing | DeepSeek API Docs</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4.1-flash-1017">DeepSeek V4.1 Flash 1017 - API Pricing &amp; Benchmarks</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#Huawei Ascend`, `#AI infrastructure`, `#model analysis`, `#inference`

---

<a id="item-tech-news-12"></a>
### [Hugging Face 博客称精简小模型词表可省 77% 推理成本](https://huggingface.co/blog/Dharma-AI/vocabx-vocabulary-specialization) ⭐️ 5.0/10

Hugging Face 上的一篇博客文章（作者 Dharma-AI，发布于 2026 年 10 月 21 日）称，针对具体应用改写小语言模型（SLM，指参数量较小、可以低成本运行的语言模型）的词表，能把推理成本降低 77%。推理指模型处理一次请求、给出回答时消耗的计算资源，词表则是模型认识的全部“词块”（token，模型处理文本的最小单位）的清单。文章把 77% 说成真实应用中的结果，但从目前可见的信息看，文中没有给出可独立核对的测量条件，也没有随文发布可直接下载使用的模型或代码，因此这个数字应视为作者的说法而非经过验证的结论。其基本思路是：词表越贴合实际业务里的文字，同样一段内容被切成的词块越少，需要计算的部分也越少；这类改动通常要重新训练或调整模型，而不是改一个设置就能完成。

rss · Hugging Face Blog · 10月21日 17:35

**「背景：词表为什么会影响成本」** 小型语言模型（SLM）指参数规模远小于主流大模型、通常只针对某一类任务训练的模型。模型的“词表”是它能识别和输出的全部文字片段的清单，这些片段称为 token（模型处理文本的最小单位）；词表越长，模型每生成一个 token 都要在这张更长的清单上做一遍比对计算，这部分开销会随词表规模一起增长。Dharma-AI 是一家巴西研究机构，专做面向具体行业问题的小型专用模型；外部一篇行业文章给出的量级对比是，处理同样 1,000 个 token，大模型约需 0.02 美元，而高效的小模型可低至 0.001 美元。

**「对使用者的实际影响」** 对在自己服务器上运行小模型的团队来说，这篇文章提示词表大小是影响单次调用开销的一个可调项，而不只是模型参数规模；但由于没有配套的模型或代码放出，现在无法直接照搬，只能作为自建方案时的一个评估方向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Dharma-AI">Dharma - AI ( Dharma - AI )</a></li>
<li><a href="https://www.linkedin.com/pulse/enterprise-ai-deployment-strategic-pivot-from-llm-scale-don-zou-ossae">Enterprise AI Deployment: The Strategic Pivot from LLM Scale to SLM ...</a></li>

</ul>
</details>

**标签**: `#SLM`, `#inference cost`, `#vocabulary specialization`, `#model optimization`, `#Hugging Face`

---

<a id="item-tech-news-13"></a>
### [IBM 发布 Granite Speech 5.0 语音模型](https://huggingface.co/blog/ibm-granite/granite-speech-5) ⭐️ 5.0/10

IBM 在模型分享平台 Hugging Face 上发布了 Granite Speech 5.0，称这个语音模型（用语音数据训练、可自动识别和处理说话内容的软件）在把语音转成文字、语音翻译以及判断每句话由谁说出（说话人归属）这三件事上更准确、也更快。IBM 没有随发布提供许可条款、对比测试结果或使用费用，因此目前只能确认这是一项厂商声明，无法独立判断它比旧版或其他模型好多少。

rss · Hugging Face Blog · 10月21日 14:58

**「背景」** Granite Speech 并非首次出现。据 IBM 的模型文档，这一系列是体量较小、专门处理多语言语音的模型：把说话内容转成文字（语音识别），以及把一种语言的说话内容转成另一种语言的文字（语音翻译），覆盖英语、法语、德语、西班牙语、葡萄牙语和日语。Hugging Face 上的发布说明显示，这次 5.0 更新包含一个新的 20 亿参数模型 granite-speech-5.0-2b（参数是模型内部的数值规模，通常越大越能处理复杂情况，但运行也更慢），以及两个已有模型的修订版：主打极快转录的 granite-speech-5.0-470m-turboctc 和 granite-speech-4.1-2b-plus。

**「商用前先看清是哪个版本」** 如果想把语音转写做进自己的产品或内部工具，最需要留意的是许可证分两种：据第三方报道，主推的 470M TurboCTC 版本采用 Apache 2.0 许可证（一种允许修改和商用的开源协议），可以商用；另一个用受限数据训练的版本只允许非商业用途，下载前要确认拿的是哪一个。该模型约 4.7 亿参数，小到可以在普通服务器甚至本地设备上运行，但“处理速度达实时的 12,600 倍”和 5.00% 的词错率目前都是 IBM 自己的说法，尚无独立测试证实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/granite/docs/models/speech">Granite Speech | IBM Granite</a></li>
<li><a href="https://huggingface.co/blog/ibm-granite/granite-speech-5">Granite Speech 5.0: Transcribe, Translate, and Attribute more ...</a></li>
<li><a href="https://www.orcarouter.ai/blog/granite-speech-5-0-470m-turboctc-apache-explained">Granite Speech 5 . 0 470M TurboCTC: Apache-2.0 ASR, 12.6K RTFx</a></li>
<li><a href="https://slator.com/ibm-granite-speech-5-transcription-model/">IBM Releases Granite Speech 5 . 0 Model</a></li>

</ul>
</details>

**标签**: `#speech-model`, `#ibm-granite`, `#model-release`, `#open-weight`, `#transcription`

---

<a id="item-tech-news-14"></a>
### [开发者用 AI 助手 Claude 花六周复活停产的 Hello Sense 睡眠追踪器](https://habr.com/ru/articles/1097526/?utm_campaign=1097526&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

据一篇俄语报道，美国开发者约瑟夫·斯佩里耶在 2026 年夏天用 AI 助手 Claude，让一款已停产的 Hello Sense 睡眠追踪器重新工作。这款设备所属的公司 Hello 已在 2017 年关闭，配套云服务（设备联网后依赖的远程服务器）也随之停运。报道称整个过程花了六周，期间遇到接线问题、装错固件（设备内部控制硬件的基础软件），还和 Claude 一起卡在同一个难题上 19 天；但文章没有给出代码、零件清单、安装步骤或别人能照着复现的证据，因此不能当成一套可照做的修复方法。

rss · Habr AI · 10月21日 19:23

**「背景」** Hello 是一家做睡眠追踪的创业公司，其 Sense 由一个床头球体和一条铺在床垫下的感应带组成：除了记录睡眠，它还会测量卧室的光线、噪音和湿度，并挑在睡眠周期较浅的时刻把人叫醒（2015 年融资时公司估值约 2.5 亿至 3 亿美元）。公司在 2017 年倒闭，配套的手机应用和云端账号服务一起关停，而这类设备要靠厂商的服务器才能工作，服务器一停就等于报废——这正是斯珀里尔要解决的问题。他本人把整个过程写在自己的博客上，标题是“AI 复活了一家已经死掉的睡眠公司”。

**「实际影响」** 对拥有类似停服设备的人来说，最直接的提醒是：设备不能用，未必是硬件坏了，可能是厂商关掉了云端服务器。如果你手里有这类产品，先确认它是否必须连厂商服务器才能使用；这篇报道没有提供可照做的修复步骤，不能把它当成维修指南。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.josephspurrier.com/ai-revives-a-dead-sleep-company">AI Revives a Dead Sleep Company | Joseph Spurrier</a></li>
<li><a href="https://www.youtube.com/watch?v=1VBMrLPwXjU">Unboxing the Sense sleep tracker from Hello - YouTube</a></li>
<li><a href="https://techcrunch.com/2015/06/15/sense-sleep-tracker-maker-hello-valued-between-250m-and-300m-in-latest-funding-round/">Sense Sleep Tracker Maker Hello Valued Between... | TechCrunch</a></li>

</ul>
</details>

**标签**: `#Claude`, `#Hello Sense`, `#hardware revival`, `#AI-assisted repair`, `#reverse engineering`

---

<a id="item-tech-news-15"></a>
### [有人把银行卡、手机和 200 多个工具接口交给 AI 助手做实测](https://habr.com/ru/articles/1097430/?utm_campaign=1097430&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

俄罗斯技术社区 Habr 上的一篇第一人称文章称，作者给一个 AI 智能体（能自己调用工具、连续执行多步任务的 AI 程序）配了一张专用银行卡用于付款，还给了它一部手机、一个浏览器，以及 200 多个 MCP 和 API 的接入权限，用来测试它能否在现实世界里独立办事。MCP 是一种让 AI 助手统一连接外部工具和服务的接口标准。据文章摘要，这个智能体替她买了机票、囤了一年的咖啡，还进了几家餐厅的黑名单。但公开的摘要只有这几句结论，没有交代用的是哪个模型、花了多少钱、哪些任务失败、权限怎么设置，也没有可复现的证据，因此这些说法目前只是作者的自述，无法核实。

rss · Habr AI · 10月21日 15:27

**「背景」** AI 智能体（agent）指的是能自己连续完成多步操作的 AI 程序：它不只回答问题，还会打开网页、填写表单、下单付款。MCP（Model Context Protocol，模型上下文协议）是一套公开的接口标准，作用类似一个通用转接头，让 AI 能接上邮箱、日历、购物网站、银行接口这类外部服务；文中说的“200+ MCP 和 API”，就是接了两百多个这样的外部工具。这类“给 AI 一张真卡、让它自己办事”的测试此前也有人做过：据 SecurityLab 2026 年 5 月的报道，英国数学家 Hannah Fry 团队的类似实验很快就出现了失控迹象，这也是此类测试通常把重点放在“自主性该在哪里停下”的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.securitylab.ru/news/572386.php">ИИ дали банковскую карту и доступ в интернет. Эксперимент ...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#MCP`, `#agent autonomy`, `#real-world testing`, `#LLM tooling`

---

<a id="item-tech-news-16"></a>
### [Habr 教程：拆解 ReAct 智能体的模型、工具与循环](https://habr.com/ru/articles/1096976/?utm_campaign=1096976&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

10 月 21 日，Habr 上一位署名 NullPilot 的作者发布了一篇教程，拆解 ReAct 智能体（一种让语言模型先说明打算做什么、再调用工具、再根据返回结果继续的循环方式）的内部结构：由模型决定下一步动作，由外部程序真正执行工具，执行结果再被拼进下一次请求。文章先给出请求与响应往返的示意图，然后用 Python 从零实现这个循环，不依赖任何智能体框架（把这类循环封装好的现成软件库），示例代码放在 GitHub 上。文中没有提出新模型或新产品，属于原理讲解，而非功能发布。

rss · Habr AI · 10月21日 05:46

**「背景：ReAct 是什么」** ReAct 这个名字来自 2022 年 10 月发表的一篇研究论文（2023 年被 ICLR 会议收录），它让语言模型把「想」和「做」交替起来：先写下一段推理，再决定调用哪个工具，看到工具返回的结果后接着推理。这里的「工具」指模型之外的程序，比如读一个文件、搜索网页或执行一条命令；模型本身只会输出文字，真正动手的是外面这层程序。这篇教程拆解的正是这个循环，而据技术博客 LLMBase 的梳理，如今许多代理框架都沿用同一套思路。

**「对使用者的实际意义」** 对使用编程智能体的人来说，这篇教程把“黑箱”拆成可以逐步对照的环节：模型给出动作、程序解析并执行、结果回填进下一轮请求。当智能体反复调用同一个工具、读错文件或过早收尾时，可以按这三步去定位是哪一环出了问题，而不是只能笼统地归因于模型能力。想动手验证的人可以照着 GitHub 上的代码跑一遍，但那是教学示例，不是可直接投入生产使用的成品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2210.03629">[2210.03629] ReAct: Synergizing Reasoning and Acting in ...</a></li>
<li><a href="https://spawn08.github.io/llmbase/06_research_papers/19_react/">ReAct: Reasoning and Acting - LLMBase - spawn08.github.io</a></li>

</ul>
</details>

**标签**: `#ReAct`, `#LLM agents`, `#Python`, `#tool use`, `#GitHub code`

---

<a id="item-tech-news-17"></a>
### [ESP8266 单片机跑 3D 游戏：作者拆解光线投射代码](https://habr.com/ru/articles/1097380/?utm_campaign=1097380&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位作者在 Habr 上发布了系列文章的第二篇，拆解他如何让 ESP8266（一款几美元、自带 Wi-Fi 的低功耗单片机芯片）画出 3D 游戏画面；第一篇讲的是硬件和外壳组装。代码用 C++ 写在 Arduino IDE 里，整个项目放在一个文件中，内含三款游戏（作者称源码里其实已有五款），靠一个名为 gameState 的状态变量在游戏之间切换。画面不是靠绘制 3D 多边形，而是用光线投射（raycasting，从玩家位置发出射线、看视线撞到哪面墙，再拼出伪 3D 画面的方法）：每帧发出 320 条射线，与一张 32×32 的网格地图求交，具体用 DDA 算法（一种逐格步进、判断射线先碰到哪条网格线的算法）实现。目前可见的内容只有文章开头，实际的代码清单、元件清单、安装步骤，以及项目确实能跑起来的证据，都不在这段摘录里。

rss · Habr DIY · 10月21日 16:39

**「背景」** 这是该项目的第二篇文章：第一篇介绍了硬件、外壳组装和部分软件实现，本篇进入源码，拆解数学、算法以及针对弱硬件的优化。光线投射（raycasting）不绘制真正的三维多边形，而是从玩家位置发射一束束射线，看它们与网格地图中的墙在哪里相交，用二维计算模拟出第一人称三维画面；早期第一人称游戏常用这种办法。文章中的引擎在 ESP8266（一种便宜、自带 Wi-Fi 的小型可编程芯片）上用 C++ 编写，开发环境是 Arduino IDE（给这类小板子写程序的工具），整个项目放在一个文件里，向 32×32 的网格发射 320 条射线，并用一个名为 gameState 的变量记录当前该运行哪款游戏——正文说有三款，作者又称源码里已有五款。

**标签**: `#ESP8266`, `#raycasting`, `#Arduino`, `#embedded graphics`, `#game development`

---

<a id="item-tech-news-18"></a>
### [OpenAI 模型将进入 Google Cloud 企业模型目录](https://openai.com/index/openai-models-google-cloud/) ⭐️ 5.0/10

OpenAI 公布与 Google Cloud 的合作：计划把 OpenAI 的先进模型和 Codex 智能体工作流（让 AI 分多步完成编程任务的工具）接入 Google Cloud 的 Model Garden（模型目录）。按公布的说法，企业客户可通过 Google Cloud 的 Marketplace（云软件市场）购买，并用已承诺的 Google Cloud 消费额度（企业此前承诺的最低云支出）抵扣。这些模型还计划进入谷歌的 Antigravity 和 Gemini Agent 产品，预计数周内开放。OpenAI 表示微软仍是其主要云合作伙伴；目前没有公布具体模型版本、价格、用量限制或确切上线日期。

telegram · zaihuapd · 10月21日 13:40

**「背景」** Google Cloud 的 Model Garden 是一个企业挑选并调用各家 AI 模型的目录，企业可以在同一个云平台里购买和使用不同公司的模型。Google Cloud 表示，OpenAI 模型进入后，它成为唯一同时提供谷歌 Gemini、Anthropic Claude 和 OpenAI GPT 这三个模型系列的大型云服务商；OpenAI 则称微软仍是其主要云合作伙伴。

**「实际影响」** 对已经在使用 Google Cloud 的企业，最直接的变化是采购入口：OpenAI 模型若按计划上架，可以走现有的 Google Cloud 采购和预算流程，并用承诺消费抵扣，相当于增加一个企业采购渠道。由于版本、价格、配额和上线日期都未公布，IT 负责人现在还不能据此做迁移或预算安排，只能等正式条款。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/openai-models-google-cloud/">OpenAI models are coming to Google Cloud</a></li>
<li><a href="https://cloud.google.com/blog/products/ai-machine-learning/google-cloud-brings-openai-models-to-customers">Google Cloud brings OpenAI models to customers | Google Cloud ...</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Google Cloud`, `#Model Garden`, `#Codex`, `#enterprise access`

---

<a id="item-tech-news-19"></a>
### [未经证实：OpenAI 模型将进入谷歌 Antigravity](https://telegram.me/AI_Copilot_Channel/926) ⭐️ 5.0/10

一条 Telegram 频道消息称，OpenAI 的 AI 模型将在未来几周内面向付费用户出现在谷歌的编程工具 Antigravity 中。Antigravity 是谷歌推出的、能自动执行写代码任务的编程工具（所谓“代理式”编程环境）。该消息没有说明会提供哪些模型、价格或使用额度，也没有附官方链接或其他来源，因此目前只能视为未经证实的说法。

telegram · AI\_Copilot\_Channel · 10月21日 18:57

**「背景」** Antigravity 是谷歌推出的编程工具，属于“智能体式”开发环境：用户给出目标后，AI 能自己分步骤读代码、改文件、跑测试，而不只是补全一行代码。OpenAI 也有对位的编程产品 Codex，两家在这一领域此前一直是各卖各的工具（据 Lushbinary 的工具对比和 getbind 的产品介绍）。所以“OpenAI 模型进入 Antigravity”若成真，等于谷歌的编程工具里要接入竞争对手的模型。

**「影响」** 如果这一安排真的上线，已经为 Antigravity 付费的人就能在同一个工具里切换使用 OpenAI 的模型，而不必另开一个编程助手；但在具体模型、额度和价格公布前，用户无法判断是否值得为此续费或改套餐。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lushbinary.com/blog/ai-coding-agents-comparison-cursor-windsurf-claude-copilot-kiro-2026/">AI Coding Agents 2026: Claude Code vs Antigravity ... | Lushbinary</a></li>
<li><a href="https://blog.getbind.co/introducing-google-antigravity-overview-and-comparison-with-openai-codex/">Introducing Google Antigravity , Overview and Comparison with...</a></li>

</ul>
</details>

**标签**: `#antigravity`, `#openai`, `#coding-agents`, `#model-availability`, `#subscription-access`

---

<a id="item-tech-news-20"></a>
### [AI 编码智能体技能包上线：号称支持多平台，细节有限](https://github.com/Maik326/rayfernando-skills) ⭐️ 5.0/10

一个 Telegram 频道发布消息，称一套面向 AI 编码智能体（能自己读代码、改代码的 AI 助手）的“技能包”已上线，可配合 Claude Code、Cursor、Codex 等编程工具使用，并支持同时安装多个插件。帖子点名了 waves、running-bug-review-board、bootstrap-ios 等几个功能模块，称其用于处理复杂任务和并行验证，但未说明每个模块具体做什么。项目以 GitHub 仓库形式给出，帖子另附两条 Telegram 链接作为“上手步骤”。消息中没有版本号、安装命令，也没有任何演示或测试结果，因此这套技能包是否真能按描述工作，目前无法从帖子本身确认。

telegram · aipluscn · 10月21日 01:50

**「背景」** 这里的“技能包”可以理解为一组可安装的说明文件：每个文件告诉 AI 编码助手（能按自然语言指令改代码的工具）在某一类任务中按什么步骤做、检查什么。GitHub 上的这个项目被介绍为 Ray Fernando 收集的这类可安装技能文件，其中 running-bug-review-board 是一个面向真实用户测试的缺陷评审流程，带有反馈循环。按技能目录网站的介绍，这些技能可通过 skills 命令行工具安装到 Claude Code、Cursor 等编码助手中。

**「对使用者的实际影响」** 想尝试的人需要先打开 GitHub 仓库或那两条 Telegram 链接，自己找安装方法，因为帖子正文没有给出任何命令。另外，这类技能包通常要配合特定版本的编程工具才能用，而帖子没有说明适配范围，安装前最好先确认自己的工具版本是否匹配。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://skillsllm.com/skill/rayfernando-skills">rayfernando - skills - AI Agents on GitHub | SkillsLLM</a></li>
<li><a href="https://github.com/RayFernando1337/rayfernando-skills">RayFernando1337/ rayfernando - skills : Ray Fernando &#x27;s collection of...</a></li>
<li><a href="https://www.skills.sh/rayfernando1337">rayfernando 1337 — Agent skills</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#Claude Code`, `#Cursor`, `#Codex`, `#GitHub project`

---

<a id="item-tech-news-21"></a>
### [有帖子称主流网站开始封堵 AI 智能体，但未给出可核实来源](http://cars.com/) ⭐️ 5.0/10

一则中文 Telegram 帖子称，一批主流网站正在阻止 AI 智能体（能自己打开网页、代替人点击和填表的 AI 程序）访问。帖子列举说：Yelp 只允许参加其付费数据授权计划的智能体进入；达美航空阻止智能体代用户订机票；摩根大通和嘉信理财以安全为由阻止智能体访问用户账户；亚马逊屏蔽了 Meta 的 Muse、xAI 的 Grok、Instinct 的智能体以及 OpenAI 的 Dots。帖子还称 Cars.com 和 Amtrak 等网站已无法访问，Meta 则改为与沃尔玛、Gap、Sephora、百思买等零售商合作。该帖子没有给出来源链接、具体时间或可复现的细节，上述说法均未获得独立确认。

telegram · aipluscn · 10月21日 01:51

**「背景」** AI 智能体是能自己打开网页、点击按钮、填写表单，替人完成订票或购物等任务的软件。此前 OpenAI、Meta、xAI 等公司把它宣传成可以代替用户上网办事；但网站会用验证码、登录限制和反机器人系统来区分真人与自动化程序，智能体一旦被挡，普通用户也会卡在中间。

**「对使用者的影响」** 对使用这类“代上网”功能的人来说，最直接的变化是任务可能中途失败：让助手订机票、查账户或下单时，网站会直接拒绝，用户只能自己手动完成。如果这类封锁扩大，智能体浏览功能能用在哪些网站，将取决于各网站是否愿意放行，而不只取决于 AI 产品本身的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theverge.com/ai-artificial-intelligence/1013195/ai-agents-blocked-web">Websites are closing their doors to AI agents | The Verge</a></li>
<li><a href="https://techcrunch.com/2026/10/06/the-next-hurdle-for-ai-agents-getting-websites-to-let-them-in/">The next hurdle for AI agents : getting websites to let... | TechCrunch</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#access restrictions`, `#agentic browsing`, `#platform policy`

---

<a id="item-tech-news-22"></a>
### [Anthropic 的 Opus 5.5 模型服务出现异常，官方称已修复并在监控](https://telegram.me/aipluscn/3164) ⭐️ 5.0/10

Anthropic 的 Opus 5.5 模型服务出现异常报错，公司表示已经实施修复，正在监控服务恢复情况，异常原因仍在调查中。Opus 5.5 是 Anthropic 旗下 Claude 系列模型的一个版本，用户通过网页或程序接口调用它来生成回答。这条消息没有说明报错的具体表现、持续了多久、影响了哪些地区，也没有给出可复现的证据或官方状态页链接，因此目前只能确认“出过故障、已做修复、仍在观察”这三点。

telegram · aipluscn · 10月21日 02:06

**「背景」** Opus 5.5 是 Anthropic 提供的 Claude 系列 AI 模型之一，用户通过网页、手机应用或程序接口（让其他软件直接调用模型的服务）来使用它。这类模型运行在 Anthropic 自己的服务器上，因此一旦服务端出问题，用户端看到的是对话卡住、报错或请求失败，而不是自己设备上的故障。

**「对使用者的影响」** 对把 Opus 5.5 接入批量任务或企业应用的人来说，故障期间发出的请求可能直接失败或拿不到结果，需要重试。由于这条消息没有给出时间窗口和受影响范围，使用者无法据此判断自己的请求是否落在故障期内，只能以自己实际收到的报错为准。

**标签**: `#Anthropic`, `#Claude`, `#service outage`, `#model availability`

---