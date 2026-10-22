---
layout: default
title: "Horizon Summary: 2026-10-22 (ZH)"
date: 2026-10-22
lang: zh
---

> 从 139 条内容中筛选出 21 条重要资讯。

---

**科技新闻**
1. [LiteLLM 1.107.0 在 PyPI 上被植入窃密后门](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenAI 改进缓存：Codex 闲置会话不再重填，API 可选保留 12 小时](#item-tech-news-2) ⭐️ 8.0/10
3. [Ollama v0.40.8 上线 400 亿参数编码模型 Flint，暂仅限 macOS](#item-tech-news-3) ⭐️ 7.0/10
4. [new-api 候选版修复安全漏洞与计费问题](#item-tech-news-4) ⭐️ 6.0/10
5. [俄语博主盲测 27 个大模型，目前只公布了测试设计](#item-tech-news-5) ⭐️ 6.0/10
6. [Anthropic 开放 Claude Duet 预览：常驻云端的主动型助手](#item-tech-news-6) ⭐️ 6.0/10
7. [社区插件 Hey 为 Claude Code 加入 Markdown 任务管理与 AI 估算](#item-tech-news-7) ⭐️ 6.0/10
8. [OpenAI 新规：路由与网关类服务须先获批准](#item-tech-news-8) ⭐️ 6.0/10
9. [IBM 发布 Granite Speech 5.0 语音模型，称转写与翻译更快更准](#item-tech-news-9) ⭐️ 5.0/10
10. [给 AI 代理一张银行卡和 200 多个接口，她测了它的独立性](#item-tech-news-10) ⭐️ 5.0/10
11. [团队用三年 PR 评论训练 Claude，代码评审成本降约七成](#item-tech-news-11) ⭐️ 5.0/10
12. [开源本地仪表盘 Slightly Parallel 发布，用于协调多个 AI 代理项目](#item-tech-news-12) ⭐️ 5.0/10
13. [Habr 教程：拆解 ReAct 智能体的模型、工具与控制循环](#item-tech-news-13) ⭐️ 5.0/10
14. [本地会议转写：T-one 实时草稿，GigaAM 会后精修](#item-tech-news-14) ⭐️ 5.0/10
15. [ESP8266 上单文件伪 3D 游戏引擎：作者拆解渲染与优化](#item-tech-news-15) ⭐️ 5.0/10
16. [传闻：OpenAI 模型将在数周内对 Antigravity 付费用户开放](#item-tech-news-16) ⭐️ 5.0/10
17. [fal 与 BFL 发布 FLUX 3 Max，10 秒视频生成约 12.45 秒](#item-tech-news-17) ⭐️ 5.0/10
18. [AgentGrid：统一管理多个 AI 编码代理的开源工具](#item-tech-news-18) ⭐️ 5.0/10
19. [据报多家主流网站封堵 AI 智能体访问](#item-tech-news-19) ⭐️ 5.0/10
20. [免费额度插件仓库 dsh-our-free-model 被贴律师函](#item-tech-news-20) ⭐️ 5.0/10
21. [OpenAI 模型将进驻 Google Cloud 企业模型目录](#item-tech-news-21) ⭐️ 5.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [LiteLLM 1.107.0 在 PyPI 上被植入窃密后门](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) ⭐️ 8.0/10

安全公司 SafeDep 在 10 月 21 日发布的分析称，开源工具 LiteLLM 的 1.107.0 版本在 PyPI（Python 的公共软件包仓库，相当于 Python 的“应用商店”）上被替换成了带恶意代码的版本，安装后会窃取开发者电脑上的登录凭据，并留下一个后门（让攻击者日后能远程进入的通道）。LiteLLM 常被用来做“模型网关”：让程序用同一套接口去调用不同公司的 AI 模型，因此受影响的是那些把它部署在自己服务器上、用来转发模型请求的团队。文章称攻击者拿到了三名开发者的 GitHub 账号凭据，项目方已撤销其中大部分权限。这些技术细节来自第三方安全厂商的单一报告，尚未见到独立验证，具体哪些密钥被窃、影响范围多大都还不清楚。

hackernews · abhisek · 10月21日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=50181114)

**「背景」** LiteLLM 是一个开源的「网关」软件：公司内部的应用只要连上它这一个地址，就能调用 OpenAI、Anthropic 等不同厂商的模型，各家服务的密钥也集中存放在它这里。它通过 PyPI（Python 语言的公共软件仓库，开发者敲一条命令就能下载安装）分发给用户，而安装这类软件包时，包里的代码会直接在机器上运行——这正是被做过手脚的版本能够窃取密钥的前提。

**「实际影响与应对」** 对使用 LiteLLM 的人来说，最直接的后果是：这类网关（把应用请求统一转发给不同 AI 服务商的中间软件）通常同时保存着多家服务商的密钥，一旦装到被污染的 1.107.0，泄露的不只是一个账号，而是它连接过的所有服务的凭据。LiteLLM 官方说明称，这次投毒发生在 10 月 21 日凌晨的发布流程中，恶意版本同时被推到了 PyPI（Python 的公共软件包仓库）和 Docker 镜像仓库，因此用 pip 安装或用容器拉取都可能中招；官方称企业私有版本未受影响。建议立刻确认自己或团队是否装过、拉取过 1.107.0，若有则回退并锁定到更早的版本、重建容器，然后轮换该部署能接触到的全部密钥——只删掉恶意版本并不够，因为凭据可能已经被读走。

**「社区讨论」** 有评论者提醒可以用 canarytokens.org 这类“诱饵令牌”服务，一旦有人使用泄露的密钥就会收到警报。也有人认为这类事件防不住：安装工具时弹出的权限请求太多，人会产生“弹窗疲劳”，最后习惯性点同意。还有评论者指出，这已是 LiteLLM 一两年内第二次重大供应链攻击（上一次在今年 3 月），并建议把版本固定在 1.107.0 之前的某个版本，直到有进一步说明为止。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/">Compromised LiteLLM 1.107.0 on PyPI Installs a Credential ...</a></li>
<li><a href="https://github.com/BerriAI/litellm/issues/47826">Litellm 1.107.0 on PYPI Compromised - GitHub</a></li>
<li><a href="https://docs.litellm.ai/blog/security-incident-oct-21-2026">Contained: Oct 21, 2026 LiteLLM release v1.107.0 Compromised</a></li>
<li><a href="https://www.rescana.com/post/litellm-1-107-0-supply-chain-compromise-october-2026">LiteLLM 1.107.0 Supply-Chain Compromise: Credential-Stealing ...</a></li>
<li><a href="https://openhack.com/blog/litellm-1-107-0-supply-chain-attack">LiteLLM 1.107.0 Compromise: Impact and Remediation</a></li>

</ul>
</details>

**标签**: `#supply-chain-security`, `#litellm`, `#pypi`, `#llm-proxy`, `#credential-theft`

---

<a id="item-tech-news-2"></a>
### [OpenAI 改进缓存：Codex 闲置会话不再重填，API 可选保留 12 小时](https://telegram.me/ai_newz/4813) ⭐️ 8.0/10

据 Telegram 频道 ai\_newz 报道，OpenAI 调整了产品中的缓存机制。缓存指的是把模型已经读过的对话内容存下来，下次接着聊时不必从头再读一遍。报道称，Codex（OpenAI 的编程助手）和 ChatGPT Work 的缓存改为一直保留，用户离开几小时后回到原来的会话，不会因为重新写入缓存而消耗大量用量额度。面向开发者的 API（让程序直接调用模型的服务接口）新增了把缓存保留 12 小时的选项，价格是 30 分钟缓存写入价的两倍。该消息来自二手渠道，没有给出具体价格数字，也未见 OpenAI 的官方说明。

telegram · ai\_newz · 10月21日 03:44

**「背景：缓存为什么和额度有关」** 大模型每回答一次，都要把之前的对话和指令重新读一遍。缓存（把已经处理过的内容存起来，下次直接复用）就是为了省掉这次重复处理，既省时间也省钱。在这次调整之前，OpenAI 的接口只把缓存保留很短时间（30 分钟），超时后继续同一个会话就要重新写入一遍，并按写入量计费，这正是长时间挂着的会话会额外消耗额度的原因。Codex 是 OpenAI 的编程助手，ChatGPT Work 是面向工作场景的版本；据开发者文档，12 小时缓存于 2026 年 10 月 20 日上线，主要面向整天反复使用同一段上下文的智能体类应用。

**「对使用者的实际影响」** 对订阅 Codex 的用户，直接变化是长时间搁置的会话在恢复时不再吃掉额度，可以更放心地中断再继续。对调用 API 的开发者，12 小时保留只有在确实会在半天内反复使用同一段长内容时才划算；否则多付的一倍写入费用换不回节省。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://explainx.ai/blog/openai-12-hour-prompt-caching-codex-work-cache-forever-claimed-vs-verified-2026">OpenAI 12-Hour Prompt Caching: 2.5x Write, Verified ...</a></li>
<li><a href="https://www.gate.com/news/detail/openai-api-introduces-12-hour-prompt-caching-on-october-21-codex-and-work-25092085">OpenAI API Introduces 12-Hour Prompt Caching on October 21 ...</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Codex`, `#caching`, `#API pricing`, `#rate limits`

---

<a id="item-tech-news-3"></a>
### [Ollama v0.40.8 上线 400 亿参数编码模型 Flint，暂仅限 macOS](https://github.com/ollama/ollama/releases/tag/v0.40.8) ⭐️ 7.0/10

Ollama 发布 v0.40.8，新增可直接运行的编码模型 Flint。Flint 由 Recursive 开发，采用 Apache 2.0 许可证（可自由使用和修改），总参数 400 亿，属于混合专家模型（把模型拆成多个子网络，每次只调用其中一部分，以降低运行成本），每次处理一个 token（模型处理文本的基本单位）实际调用约 25 亿参数，并支持 26.2 万 token 的上下文窗口（一次能容纳的文本量）。Recursive 自行公布的测试结果显示，Flint 在 Terminal-Bench 2.1 上得分 54.9%，在 SWE-bench Verified 上得分 74.2%；目前该模型在 Ollama 上仅支持 macOS，其他 GPU 平台要等后续版本。

github · github-actions\[bot\] · 10月21日 16:20

**「背景」** Ollama 是一个在本机下载并运行 AI 模型的工具，用户不必把代码或问题发到云端。Flint 采用“混合专家”（MoE）结构：模型总共有 400 亿参数，但每次生成只调用其中约 25 亿，因而比同等规模的普通模型更省算力；262K 上下文窗口则指一次能读入约 26 万个词元（token，模型处理文本的基本单位），可覆盖多个代码文件。

**「实际影响」** 对在 Mac 上本地运行模型的用户，升级到 v0.40.8 后执行 \`ollama run flint\` 即可试用，不必单独下载或配置模型。使用 Windows 或 Linux 显卡的用户目前无法通过 Ollama 运行 Flint，发布说明称其他 GPU 支持会在后续版本加入，也没有给出具体的内存或显存要求。

**标签**: `#ollama`, `#flint`, `#open-weight-models`, `#coding-models`, `#local-llm`

---

<a id="item-tech-news-4"></a>
### [new-api 候选版修复安全漏洞与计费问题](https://github.com/QuantumNous/new-api/releases/tag/v1.0.0-rc.46) ⭐️ 6.0/10

自己搭建 AI 模型请求中转软件 new-api 的人需要关注 v1.0.0-rc.46（候选发布版，还不是正式版）：发布说明称它修复了公开漏洞编号 CVE-2026-111943 的安全问题，并建议尽快升级。这个软件的作用是把用户请求转发给不同的 AI 模型厂商；本次把 Go 语言运行环境升到 1.26.10，用源码自行编译的人也要换到这个版本，因为新版本在检查网站证书时会拒绝一小批已不再受信任的中间证书（证书链里的过渡证书）。发布说明没有交代该漏洞的严重程度或影响范围，所以单看这份说明无法判断有多紧急。同一版本还修复了 Claude 流式回复（文字边生成边显示）在准备和重试时断开、合并连续助手消息后丢失工具调用（让模型调用搜索或计算等外部功能）、任务重试换到另一家模型厂商时仍按上一次价格计费，以及 DeepSeek 美元余额为 0 时人民币余额也显示为 0 等问题；此外新增 Resend（邮件发送服务）和阿里云百炼 qwen3-vl-embedding 多模态向量模型（把文字、图片等转成可比较的数值表示，常用于搜索和相似度判断）支持。

github · Calcium-Ion · 10月21日 16:25

**「先了解 new-api 是什么」** new-api 是一套可以自己部署的 AI 接口中转服务：它把 OpenAI、Claude、Gemini 等不同厂商的模型接口统一起来，再通过不同渠道（例如不同厂商账号或线路）分发给使用者，同时负责计费、限额和日志。v1.0.0-rc.46 是正式 1.0 版之前的候选版本（rc 即 release candidate），紧接上一个候选版 rc.45，主要面向已经在运行这套服务的站长和开发者，而不是普通用户直接安装的手机或电脑应用。

**「对自建中转的人意味着什么」** 如果你自己搭这套中转（把各家模型的请求转发出去、顺带记录用量的网关程序），这一版要求尽快升级：问题出在它依赖的 Go 语言运行库的证书校验上，1.26.10 之前的版本会继续信任一批已被攻破的中间证书（用来证明网站身份的中间环节），外部研究把该漏洞编号为 CVE-2026-111943。用源码自行编译的人必须同时把 Go 换成 1.26.10，否则只更新代码拿不到这项修复。另有一处行为变化：发给 Gemini 的向量请求（把文字、图片转成一串数字以便比较的请求）里若带图片或视频，现在会被直接拒绝、不再计费，原本这样调用的人需要改走别的接口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://socprime.com/blog/cve-2026-111943-analysis/">CVE - 2026 - 111943 : eMudhra CA Key Compromise</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/mozilla-google-apple-block-compromised-emudhra-ca-certificates/">Mozilla, Google, Apple block compromised eMudhra CA certificates</a></li>

</ul>
</details>

**标签**: `#api-relay`, `#security`, `#claude`, `#deepseek`, `#release-notes`

---

<a id="item-tech-news-5"></a>
### [俄语博主盲测 27 个大模型，目前只公布了测试设计](https://habr.com/ru/articles/1096934/?utm_campaign=1096934&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

10 月 21 日，编程与科技社区 Habr 上出现一篇俄语文章，作者称对 27 个大语言模型（像 ChatGPT 那样能读写文字的 AI 模型）做了一次“盲测”，考的是工程实用问题：模型输出 JSON（程序之间交换数据用的固定格式）时，会不会多写一句“这是您的 JSON：”，导致接收程序解析失败；会不会听信客户邮件里夹带的隐藏指令（即“间接提示注入”，把命令藏在正常文本里让模型照做），擅自把客户管理系统里的订单状态改成“已同意 100% 预付”；会不会突然冒出中文汉字，或编造出不存在的俄罗斯刑法条款还标注“确定”。文章标题点名了 GPT-6、Opus 和 Alisa（俄罗斯 Yandex 的语音助手），正文还提到 Google Gemini 4 Argon 和 Muse Wonder，并称测试同时涉及俄罗斯《个人数据法》152-ФЗ 的合规问题，以及每次运行要花多少时间和费用。但公开可见的部分只有测试动机和题目设计，没有任何模型的成绩、排名、价格数据或可复现的测试方法，因此现在还无法据此判断哪个模型更好。作者提到，他今年 1 月曾发布过对 14 个模型的幻觉（模型一本正经编造不实内容）审计。

rss · Habr AI · 10月21日 06:23

**「背景」** 这是同一作者在今年 1 月对 14 个大语言模型做“幻觉”（编造看似合理但不实内容）审计后的第二轮测试。上一轮在 Gemini 3 发布后不久进行，这一轮则等到 Gemini 4 Argon 等新模型上市才开跑。测试关注真实业务场景：模型能否稳定输出 JSON（程序可直接读取的结构化数据格式）、会不会被客户邮件里夹带的指令带偏（间接提示注入），以及是否满足俄罗斯第 152-FZ 号个人数据法的要求。

**「对选型的人意味着什么」** 如果你正打算为公司业务挑一个模型，这篇文章目前给不出可用的对比结论，别把标题里的“谁弄坏了 JSON、谁吞下了注入”当成已有结果。它列出的几个检查点倒是可以直接搬到自己的数据上试：输出是否夹带多余文字、是否会被文档里的隐藏指令带走、一次调用要花多少钱和时间。在作者补上成绩之前，任何“某模型通过或未通过”的说法都缺少依据。

**标签**: `#LLM benchmarks`, `#prompt injection`, `#JSON reliability`, `#model comparison`, `#AI compliance`

---

<a id="item-tech-news-6"></a>
### [Anthropic 开放 Claude Duet 预览：常驻云端的主动型助手](https://claude.com/product/claude-duet) ⭐️ 6.0/10

Anthropic 上线了 Claude Duet 的研究预览（正式发布前的公开测试）。这是一个独立应用，已上架 iOS、Android 和 claude.ai，先向美国地区的 Pro 和 Max 订阅用户开放，且需要先加入等候名单。它连接的是一个常驻云端的“主动型代理”（能自己安排并执行任务的程序），会每天推送简报，并在后台替用户办事。发布该消息的 Telegram 频道称，它基于 Claude Opus 5.5，并与其他 Claude 产品共用订阅配额（套餐内的用量额度）；这两点并未在链接的产品页上得到确认。同一频道还称，与只对 Pro 订阅者开放的竞品 dots 不同，Duet 在预览阶段承诺也向每月 20 美元的订阅用户提供。在发送消息、付款、签署文件或删除内容之前，它会先展示即将执行的操作并等待用户批准；证券交易和账户间转账即使获得授权也不被允许。

telegram · ai\_newz · 10月21日 20:02

**「背景」** Claude 是 Anthropic 的聊天机器人，用户按月付费订阅后使用。所谓「主动型代理」，指的是不用你每次开口，它自己判断该做什么、在云端后台持续运行的那类助手——手机锁屏它也照常干活。报道把 Duet 与同类产品 dots 作对比：dots 只对 Pro 订阅者开放，而 Duet 承诺 20 美元档的订阅者也能用；产品页则写明，这次预览面向美国的 Pro 和 Max 用户，由 Opus 5.5 模型驱动（Opus 是 Claude 模型里定位较高的一档，5.5 是版本号）。

**「实际影响」** 如果配额共用的说法成立，Duet 在后台替你跑的任务会消耗与日常聊天相同的额度，重度使用者可能更快撞上套餐上限，需要留意用量。目前只有美国用户能排队申请，其他地区暂时无法使用；而“先展示再执行”的规则意味着它不会在你不知情的情况下自行发消息或付款。

**「社区讨论」** 在 Hacker News 上，有用户批评等候名单没有和已有的 Claude 聊天打通：明明已经登录、资料也都在，却还要重新填一遍信息。也有人认为这类助手对厂商来说利润可观，因为任务不必实时完成，可以排进低优先级的批处理队列，填满原本会空转的算力。另有用户表示，自己不确定把个人数据交给一个常驻助手是否安全，因此仍在观望。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claude.com/product/claude-duet">Claude Duet | Your personal AI assistant</a></li>

</ul>
</details>

**标签**: `#Claude`, `#Anthropic`, `#AI agents`, `#subscription quota`, `#product preview`

---

<a id="item-tech-news-7"></a>
### [社区插件 Hey 为 Claude Code 加入 Markdown 任务管理与 AI 估算](https://github.com/keenkim1202/Hey) ⭐️ 6.0/10

一个名为 Hey 的社区插件发布，为 Claude Code（Anthropic 推出的编程助手，用户在终端里用自然语言让它读写代码）加上基于 Markdown（一种用纯文本写标题和列表的简单格式）的任务清单，以及由模型给出工作量估算的功能。它通过 Claude Code 的插件市场安装，提供 /hey-ledger、/wassup 等斜杠命令（在对话框里以斜杠开头的指令）来记录任务和日志；脚本部分只用 Python 标准库写成，不需要额外安装依赖。需要说明的是，这不是 Anthropic 官方为 Claude Code 新增的功能，而是外部开发者做的第三方插件；来源没有给出插件版本号，也没有说明具体用法细节，更没有证据说明它的估算准不准。

telegram · aipluscn · 10月21日 07:10

**「背景」** Claude Code 是 Anthropic 推出的编程助手，用户在终端（电脑上的命令窗口）里用自然语言让它读写代码、运行命令。它允许安装第三方“插件”来增加功能，插件可以提供以斜杠开头的快捷命令；Hey 就是社区开发者编写的这类扩展，需要用户自己从插件市场安装，并非 Anthropic 官方内置的工具。

**「实际影响」** 正在用 Claude Code 的人可以按项目页说明从插件市场装上试用，把任务记进 Markdown 文件，再让模型顺手估个工作量。但它是第三方代码，会读取你的项目文件并运行 Python 脚本，安装前最好先看一眼仓库内容；估算结果也只适合当参考，不宜直接当作对外承诺的工期。来源没有说明它适配哪些 Claude Code 版本，如果装完命令不被识别，先回项目页核对用法。

**标签**: `#Claude Code`, `#developer tooling`, `#plugins`, `#task management`, `#GitHub project`

---

<a id="item-tech-news-8"></a>
### [OpenAI 新规：路由与网关类服务须先获批准](https://openai.com/index/broad-access-through-consistent-standards/) ⭐️ 6.0/10

OpenAI 于 10 月 21 日宣布更新使用政策：凡是直接向用户提供其模型访问能力的服务，例如模型路由和 AI 网关（把用户请求转发给某家 AI 公司模型的中间服务），都必须先通过 OpenAI 的审核并获得批准。新规将于 2026 年 11 月 20 日生效。托管或转售 OpenAI 模型的合作方也被要求维持同等水平的防护、调查潜在违规并与执法部门配合；OpenAI 还表示正与客户一起引入 SafetyIDs，用于在调查中区分终端用户而不暴露其身份。公告没有说明审核的具体标准，也没有提到价格或用量配额会有什么变化。

telegram · zaihuapd · 10月22日 00:46

**「先弄清“模型路由”和“AI 网关”」** 模型路由和 AI 网关是介于用户与模型之间的中间服务：用户不直接连 OpenAI，而是通过第三方把请求转给不同模型；转售方则把模型访问打包卖给其他客户。这类服务通常通过 API（让程序直接调用模型的接口）接入 OpenAI。新规针对的正是这类“二传手”，要求它们在提供 OpenAI 模型访问前先通过审核。

**「对使用者的影响」** 如果你是通过第三方中转站或聚合平台调用 OpenAI 模型（也就是用别家服务转发的 API，即让程序直接调用模型的接口），那么从 2026 年 11 月 20 日起，这类服务需要先获得批准才能继续提供访问。公告没有说明未获批准的服务会被如何处理，因此在长期依赖某个中转服务之前，值得先确认它是否在获批范围内。

**标签**: `#OpenAI`, `#usage policy`, `#API access`, `#relays and gateways`, `#access restrictions`

---

<a id="item-tech-news-9"></a>
### [IBM 发布 Granite Speech 5.0 语音模型，称转写与翻译更快更准](https://huggingface.co/blog/ibm-granite/granite-speech-5) ⭐️ 5.0/10

IBM 在 Hugging Face 的博客上宣布了 Granite Speech 5.0，这是一款语音模型（把说的话变成文字、并在不同语言之间转换的软件）。官方说法是它在三件事上比上一代更快、更准：把语音转写成文字、把一种语言的语音翻译成另一种语言，以及“归属”（attribution，通常指标明哪句话是谁说的，但公告没有展开说明这一项具体怎么做）。这些目前都只是 IBM 自己的说法：公告没有给出测试分数、价格、使用许可条款，也没有说明普通用户或开发者什么时候、通过什么渠道能用上，因此无法与同类产品做独立比较。

rss · Hugging Face Blog · 10月21日 14:58

**「背景」** Granite Speech 是 IBM 的语音模型系列。IBM 的文档称，该系列模型以 Apache 2.0 许可证（一种允许免费使用、修改和再分发的开放许可证）发布，可免费用于研究和商业用途，并公开训练数据；IBM 还称其在公开的语音识别评测榜（用来比较不同模型转写准确率的榜单）上表现领先。语音识别（把说话内容转成文字）是这类模型的主要用途之一，IBM 的模型选择页同时提示，若要用自己的数据继续训练（微调），所需资源约为直接运行模型的 3 到 4 倍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/granite/docs/models/speech">Granite Speech | IBM Granite</a></li>
<li><a href="https://www.ibm.com/granite/playground/model-selector/models">Granite Model Selector - IBM</a></li>

</ul>
</details>

**标签**: `#IBM Granite`, `#speech recognition`, `#translation`, `#model release`

---

<a id="item-tech-news-10"></a>
### [给 AI 代理一张银行卡和 200 多个接口，她测了它的独立性](https://habr.com/ru/articles/1097430/?utm_campaign=1097430&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位作者在俄罗斯技术社区 Habr 上发文，记录了她把一张专用银行卡、一部手机、一个浏览器，以及 200 多个 MCP 和 API 接口交给一个 AI 代理（能自己调用工具、分多步完成任务的程序），让它去处理现实事务的测试结果。按她的说法，这个代理替她买了机票、囤够了一年的咖啡，还被几家餐厅列入了黑名单。MCP 是一套让 AI 模型统一调用外部工具和服务的接口标准，可以理解为给模型准备的通用插头。需要注意的是，目前公开的只是文章摘要：没有说明用的是哪个模型、具体接了哪些工具、花了多少钱，也没有可复现的测试记录，所以这些结果目前只能算作者的个人陈述。

rss · Habr AI · 10月21日 15:27

**「背景：智能体与 MCP 是什么」** AI 智能体（agent）指的是能自己分多步、调用外部工具去完成任务的 AI 程序，而不只是聊天问答。它之所以能操作订票网站、银行或日历，靠的是 MCP（Model Context Protocol，模型上下文协议）——可以理解成一个通用插口，把各种外部服务接到模型上，不必为每个服务单独写对接代码。Habr 在 10 月 15 日一篇同题文章里记录了上一轮同类测试，结论是 94% 的记录错误出在工具、MCP 和 API 这些外部集成上，而不是模型本身。

**「实际影响」** 对想照着试的人来说，最直接的提醒是把权限和钱分开管：这位作者用的是一张专门用于测试的银行卡，而不是自己的日常账户。即便如此，代理仍可能做出用户没预料到的事，比如被餐厅拉黑，而这些后果要由账户持有人自己去承担和收拾。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://habr.com/ru/articles/1094906/">Где заканчивается самостоятельность ИИ-агента? Я дал ему ...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#MCP`, `#agent autonomy`, `#real-world automation`, `#tooling`

---

<a id="item-tech-news-11"></a>
### [团队用三年 PR 评论训练 Claude，代码评审成本降约七成](https://habr.com/ru/companies/otus/articles/1096720/?utm_campaign=1096720&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一个开发团队在 Habr 上发文称，他们用三年积累的代码合并请求（PR，即提交代码后请同事审核、通过后才能合入的请求）评论，做成了一位基于 Claude 的自动评审员，让它按每位同事平时的挑剔习惯来提意见。团队表示，第一版采用“多智能体”结构（让多个 AI 角色分工协作），成本过高，后来把单次评审的费用压低了近七倍。需要说明的是，目前能看到的只是文章导语：没有提示词、配置、代码或可运行的工具，因此“七倍”是团队自述，无法独立核实，也无法照搬复现。

rss · Habr AI · 10月21日 13:05

**「背景：什么是 PR 审查」** 在软件开发中，改动代码通常要先提交一个“合并请求”（PR，即请求把自己的代码改动并入项目主线的提案），再由同事逐行阅读并提意见，这一步叫代码审查。审查意见往往带着团队自己的习惯，比如变量怎么命名、出错怎么处理，而通用的 AI 助手默认并不了解这些偏好。把过去几年的审查评论当作范例交给 Claude（Anthropic 公司的 AI 助手），是让通用模型贴近某个团队风格的常见做法。

**「实际影响」** 对正在考虑用 AI 做代码评审的团队来说，这条消息的价值在于方向而非方案：真正决定评审质量的，可能是把自家历史评论喂给模型，而不是换更强的模型。但由于公开内容缺少具体做法，现在还不能据此决定是否采购或替换现有工具；看到类似“成本降几倍”的说法时，应先问清是按什么口径计算的、是否包含人工返工。

**标签**: `#AI code review`, `#Claude`, `#developer tooling`, `#cost optimization`, `#PR workflow`

---

<a id="item-tech-news-12"></a>
### [开源本地仪表盘 Slightly Parallel 发布，用于协调多个 AI 代理项目](https://habr.com/ru/articles/1097130/?utm_campaign=1097130&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

开发者 nmar33 发布了一个名为 Slightly Parallel 的开源工具，目标是帮同时推进多个项目的人集中查看和协调由 AI 编程代理（能自己读写代码、执行命令的助手）承担的工作。它由运行在自己电脑上的本地服务器加一个网页界面组成，支持 Windows、Linux 和 macOS，作者称主要面向独立开发者，以及常用 Claude Code、Codex、OpenCode 这三款代理工具的人，并计划之后支持 ZCode。目前帖子里只给出了 GitHub 代码仓库链接，没有介绍具体功能、安装步骤，也没有演示或第三方验证它能正常使用，因此还无法判断它实际能起多大作用。

rss · Habr AI · 10月21日 09:02

**「背景」** Claude Code、Codex 和 OpenCode 都是命令行里的编程助手（agent，指能自己读文件、改代码、执行命令的 AI 程序），分别来自 Anthropic、OpenAI 和一个开源项目，它们直接在用户自己电脑上的项目文件夹里干活。同时推进几个项目时，人往往要在多个终端窗口之间来回切换，才能看清每个助手做到哪一步。该项目在 GitHub 上的简介把它描述为「自托管在一台笔记本上的编程助手仪表盘，用来看 Claude Code、Codex 和 OpenCode 在你的项目里做了什么」。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/NMar33/slightly-parallel">GitHub - NMar33/slightly-parallel: A dashboard for coding ...</a></li>

</ul>
</details>

**标签**: `#coding agents`, `#developer tooling`, `#open-source`, `#Claude Code`, `#Codex`

---

<a id="item-tech-news-13"></a>
### [Habr 教程：拆解 ReAct 智能体的模型、工具与控制循环](https://habr.com/ru/articles/1096976/?utm_campaign=1096976&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

10 月 21 日，俄罗斯技术社区 Habr 发表了一篇由 NullPilot 撰写的教程，拆解 ReAct 智能体的内部构造：模型、工具，以及把两者串起来的控制循环。ReAct 智能体是一种让 AI 模型在“思考”和“动手”之间交替的工作方式：模型先说出下一步要做什么，再由外部程序去执行，比如读一个文件或运行一条命令。文章先给出请求与结果如何来回传递的示意图，讲清是谁挑选动作、谁执行工具、执行结果又怎样进入下一次请求，然后给出一份不依赖智能体框架（帮开发者拼装这类循环的现成代码库）的 Python 实现，示例代码放在 GitHub 上。这是一篇教学文章，不是新模型、新产品或价格变动。

rss · Habr AI · 10月21日 05:46

**「背景：ReAct 智能体如何工作」** ReAct 是一种常见的智能体（能自己决定步骤并调用外部工具的 AI 程序）工作方式：语言模型先判断下一步做什么，再由外部代码执行读文件、运行命令等操作，并把结果送回模型继续判断。这篇教程用 Python 从零实现这个循环，不依赖现成的智能体框架（封装好上述流程的软件库），便于读者看清模型、工具和控制循环各自负责什么。

**「对使用者的实际含义」** 对日常使用带“智能体”功能的 AI 产品的人来说，这篇文章说明了一件容易误解的事：智能体并不是另一个更聪明的模型，而是同一个模型外面套的一层循环。因此同一个模型在不同产品里表现可能差别很大，因为决定它能做什么的，是这层循环怎么设计、允许它调用哪些工具，而不只是模型本身的能力。

**标签**: `#agents`, `#ReAct`, `#Python`, `#developer tooling`, `#tutorial`

---

<a id="item-tech-news-14"></a>
### [本地会议转写：T-one 实时草稿，GigaAM 会后精修](https://habr.com/ru/articles/1096758/?utm_campaign=1096758&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位作者在 Habr 上公开了一套完全在本机运行的会议转写方案：会议中用 T-one 语音识别模型生成实时草稿字幕，会后用 GigaAM 模型把草稿重写成质量更高的文本，全程不把录音上传到云端。作者称，在 2 小时 21 分钟的工作通话上，第二遍处理改正了草稿中 11.9% 的词，同时把 1.5% 的词改坏；在他手动复听过的录音上，最终文本达到云端转写服务 Deepgram 的水平。文章还给出两遍处理的流程、费用计算和代码仓库链接，并提到作为对照的基准文本在每四个有争议的地方就有一个是错的，而同事用得很好的“两个模型串联”方案在他这里反而更差。

rss · Habr AI · 10月21日 04:16

**「背景」** 语音识别模型有两种常见用法：一种边听边出字，延迟低但结果粗糙；另一种等录音结束后整段处理，慢一些但更准确。文中用到的 T-one 是支持实时流式识别的开源模型，可以完全在本地运行，官方还提供了 Docker 演示（把服务打包好、一条命令就能启动）；GigaAM 则是专攻俄语的开源识别模型，参数量 2.4 亿，训练时用了 5 万多小时俄语语音。作者的做法是让前者在会议中先出草稿字幕，会后由后者把整段录音重写一遍。

**「实际影响」** 对担心会议录音外泄、又愿意自己动手配置的人，这套方案的价值是音频始终留在本机；代价是实时字幕仍有约一秒延迟、没有标点，质量也明显不如云端，较干净的文本要等会后第二遍处理才拿得到。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/salute-developers/GigaAM/">GitHub - salute-developers/GigaAM: Foundational Model for ...</a></li>
<li><a href="https://github.com/mkll/GigaAM-ai-speech">GitHub - mkll/GigaAM-ai-speech: Foundational Model for Speech ...</a></li>
<li><a href="https://huggingface.co/t-tech/T-one">t-tech/T-one · Hugging Face</a></li>

</ul>
</details>

**标签**: `#speech-recognition`, `#self-hosted-ai`, `#local-inference`, `#gigaam`, `#transcription-pipeline`

---

<a id="item-tech-news-15"></a>
### [ESP8266 上单文件伪 3D 游戏引擎：作者拆解渲染与优化](https://habr.com/ru/articles/1097380/?utm_campaign=1097380&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位开发者在 Habr 发文，逐段拆解自己用 C++ 在 Arduino IDE（一款面向单片机、把代码烧进芯片的开发工具）里写成的单文件游戏引擎，运行在一块 ESP8266 芯片上。引擎的核心是光线投射（raycasting）：它不绘制真正的三维模型，而是从玩家位置发出 320 条射线，看每条射线在 32×32 的网格地图上撞到哪里，再据此画出画面，具体用的是 DDA（数字微分分析器）算法。文章还讲了用一个 gameState 变量构成的状态机在几款小游戏之间切换——正文说有三款，作者注明源码里其实已有五款——以及针对弱硬件做的优化。文中没有给出代码仓库链接或安装步骤，效果均来自作者自述，没有第三方复现或测量。

rss · Habr DIY · 10月21日 16:39

**「背景」** ESP8266 是一颗几元钱的 Wi-Fi 芯片，常见于智能插座、传感器这类小设备，它的内存和运算能力远不及手机。光线投射是上世纪 90 年代初《德军总部 3D》那类游戏用过的老办法：不建三维模型，只按“射线撞墙的距离”决定每一列像素画多高，靠透视错觉让人看到立体空间。这样做的计算量小，才跑得动这种芯片。

**「对实际使用意味着什么」** 对做智能家居面板、小屏幕玩具或掌上小机器的人来说，这篇文章说明便宜的联网芯片也能画出可玩的第一人称画面，思路可以借鉴。但作者只讲了数学和优化，没有放出可直接下载的代码或安装说明，想照着做的人需要自己按文中描述重写一遍，并自行验证帧率和稳定性。

**标签**: `#ESP8266`, `#raycasting`, `#embedded C++`, `#Arduino`, `#microcontroller`

---

<a id="item-tech-news-16"></a>
### [传闻：OpenAI 模型将在数周内对 Antigravity 付费用户开放](https://telegram.me/AI_Copilot_Channel/926) ⭐️ 5.0/10

一个 Telegram 频道在 10 月 21 日发帖称，OpenAI 的模型将在未来几周内对 Antigravity 的付费用户提供。Antigravity 是一个让 AI 智能体（能自己分多步写代码、运行命令的程序）在编辑器里干活的编程工具。帖子没有说明会提供哪些具体模型，也没有价格、使用额度或调用频率限制的信息，只给了“未来几周”这个模糊时间。目前没有 OpenAI 或 Antigravity 方面的官方确认，这仍是一条未经证实的消息。

telegram · AI\_Copilot\_Channel · 10月21日 18:57

**「背景」** Antigravity 是谷歌推出的 AI 编程工具：用户用日常语言描述需求，由 AI 代理（能自己读代码、改文件、执行命令的程序）动手写和调试，OpenAI 那边的同类产品叫 Codex。这类工具通常只接入自家公司的模型，Antigravity 用的是谷歌自家模型，Codex 用的是 OpenAI 的模型，所以“谷歌的工具里出现 OpenAI 模型”属于跨公司安排，一般要通过 OpenAI 的付费接口（API，让别的软件调用其模型的通道）才能实现。若传闻成真，付费用户可能在同一套界面里切换两家公司的模型，但原帖没有说明是哪些模型、如何收费。

**「对使用者的实际影响」** 如果消息成真，已经在为 Antigravity 付费的人可能不必再单独订阅或切换到别的工具，就能在同一个界面里选用 OpenAI 的模型。但在模型名单、额度和是否额外收费公布之前，无法判断值不值得为此等待或调整现有订阅，比较稳妥的做法是等官方公告。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lushbinary.com/blog/ai-coding-agents-comparison-cursor-windsurf-claude-copilot-kiro-2026/">AI Coding Agents 2026: Claude Code vs Antigravity ... | Lushbinary</a></li>
<li><a href="https://blog.getbind.co/introducing-google-antigravity-overview-and-comparison-with-openai-codex/">Introducing Google Antigravity , Overview and Comparison with...</a></li>

</ul>
</details>

**标签**: `#coding agents`, `#Antigravity`, `#OpenAI`, `#model availability`, `#subscription access`

---

<a id="item-tech-news-17"></a>
### [fal 与 BFL 发布 FLUX 3 Max，10 秒视频生成约 12.45 秒](https://fal.ai/flux-3-max) ⭐️ 5.0/10

fal（提供 AI 模型调用服务的平台）与模型开发方 BFL 推出了 FLUX 3 Max，这是一个能根据文字或图片生成带声音视频的模型，并已在 fal 上开放试用。fal 称，生成一段 10 秒、720p（一种高清分辨率）的视频只需 12.45 秒，而对比模型 Seedance 2.5 需要 277.8 秒，约快 22 倍；这是 fal 自己的测速结果，不是独立测试。价格方面，11 月 7 日前 720p 视频按每秒 0.0425 美元计费，一条 10 秒视频约 0.425 美元；促销结束后同样一条视频为 1.70 美元。该模型在 Artificial Analysis 的图生视频（用一张图片生成视频）排行榜上处于领先梯队，与 Seedance 2.5、MiniMax H3 接近。

telegram · ai\_newz · 10月21日 18:35

**「背景」** FLUX 3 Max 属于“文生视频/图生视频”模型：用户给一段文字或一张图片，它直接生成带声音的视频片段。BFL 是参与开发 FLUX 系列的团队，fal 提供在线调用并按生成视频的秒数计费；此前同类模型生成一段 10 秒 720p 视频通常要几分钟，这次双方把重点放在缩短等待时间上。

**「实际影响」** 对用这类工具做短视频的人，最直接的变化是成本：促销期一条 10 秒 720p 带声音视频约 0.425 美元，11 月 7 日后为 1.70 美元，相差四倍。若要批量生成，应按促销结束后的价格做预算，并先试做几条确认画面和声音质量；目前速度只有 fal 的自测数据，画质和声音质量也缺少细节。

**标签**: `#FLUX 3`, `#video generation`, `#fal.ai`, `#pricing`, `#benchmarks`

---

<a id="item-tech-news-18"></a>
### [AgentGrid：统一管理多个 AI 编码代理的开源工具](https://github.com/naman10parikh/agentgrid) ⭐️ 5.0/10

一个名为 AgentGrid 的开源项目（代码公开、可被查看和修改）在 GitHub 上出现，宣称能把 Claude、Codex、Gemini 等不同来源的 AI 编码代理（能自己读写代码、执行开发任务的 AI 工具）放进同一个管理界面，并支持多终端协作和状态监控。此前，开发者需要在不同代理之间手动切换；该项目称可以省去这一步。但这条消息只有高层介绍和外部链接，没有版本号、安装步骤、基准测试（用统一任务衡量效果）或可复现的演示，因此它目前更像一则项目公告，而不是已经验证可用的产品。

telegram · aipluscn · 10月21日 01:50

**「背景」** AI 编码代理（能自己读代码、改文件、执行命令的 AI 程序）目前由各家分别提供：Anthropic 的 Claude Code、OpenAI 的 Codex、Google 的 Gemini 各有自己的命令行工具，想同时用几个就得开多个终端窗口来回切换。AgentGrid 在 npm（JavaScript 的软件包仓库）上的说明写着，它用一条命令就能把这些代理并排启动，显示各自的状态标签、支持恢复上次会话，除 tmux（在一个窗口里管理多个终端会话的工具）外不依赖其他组件。

**「实际影响」** 对同时使用多个编码代理的人来说，实际影响取决于它能否顺利接入现有的终端和模型配置；目前没有安装说明、支持版本或演示，无法确认它是否真能替代手动切换。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/naman10parikh">naman 10 parikh (Naman Parikh ) · GitHub</a></li>
<li><a href="https://www.npmjs.com/package/@namanparikh/agentgrid">namanparikh/ agentgrid - npm</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#multi-model orchestration`, `#developer tooling`, `#open-source project`, `#GitHub`

---

<a id="item-tech-news-19"></a>
### [据报多家主流网站封堵 AI 智能体访问](http://cars.com/) ⭐️ 5.0/10

一份在 Telegram 上流传的行业摘要称，多家主流网站正在阻止 AI 智能体（能自己打开网页、代替人完成订票、购物等任务的程序）访问。摘要列举了几种做法：Yelp 只允许参加其付费数据许可计划的智能体进入；达美航空阻止智能体代用户订票；摩根大通和嘉信理财以安全为由阻止智能体访问用户账户；亚马逊屏蔽了 Meta 的 Muse、xAI 的 Grok、Instinct 的智能体以及 OpenAI 的 Dots；Cars.com 和 Amtrak 已无法访问。摘要还称 Meta 转而与沃尔玛、Gap、Sephora、百思买等零售商合作。需要说明的是，这些说法来自一份没有给出日期、链接或原始出处的二手摘要，无法独立核实，具体是哪些网站、从何时开始、限制范围多大，目前都不清楚。

telegram · aipluscn · 10月21日 01:51

**「背景」** AI 智能体（能自己打开网页、点击按钮，替你完成订票、下单这类操作的软件）此前被宣传成可以代你逛网站、订餐厅、买鞋。据 The Verge 在 2026 年 10 月 17 日的梳理，这轮封锁最早由用户报告 Meta 的 Muse、xAI 的 Grok、OpenAI 的 Dots 等智能体无法正常使用而暴露出来；其中亚马逊在 9 月 20 日、也就是 Meta 发布 Muse 约 12 天后，就开始屏蔽它。

**「对使用者的实际影响」** 对普通用户来说，最直接的变化是：原本能替你查航班、下单或查看账户的智能体，在这些网站上可能直接失败或给出错误结果，这类操作仍需你自己在官网或 App 上完成。摘要没有说明限制的具体形式（例如是封锁自动访问、要求登录，还是要求付费授权），因此也无法判断哪些工具、哪些任务会受影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aiweekly.co/alerts/amazon-yelp-delta-join-banks-blocking-third-party-ai-agents">Amazon, Yelp, Delta Join Banks Blocking Third-Party AI Agents</a></li>
<li><a href="https://pasqualepillitteri.it/en/news/25165/amazon-yelp-delta-jpmorgan-schwab-block-ai-agents">Amazon, Yelp, Delta, JPMorgan and Schwab confirm blocks on AI ...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#access restrictions`, `#web blocking`, `#industry analysis`

---

<a id="item-tech-news-20"></a>
### [免费额度插件仓库 dsh-our-free-model 被贴律师函](https://github.com/Ebony-Vinyl/dsh-our-free-model/issues/576) ⭐️ 5.0/10

一个名为 dsh-our-free-model 的 GitHub 代码仓库，其公开问题页面（Issues，供用户报问题和讨论的板块）被贴出一封律师函。函件指控该仓库逆向（拆解软件以找出其运行规则）WorkBuddy / CodeBuddy 客户端的渠道校验，用指纹改写模块（修改软件用来识别设备或账号的标识）绕过编号 11128 的拦截，伪造官方 UA（程序向服务器表明身份时使用的标识）和产品码，并通过多账号池自动签到领取免费额度。函件要求 3 天内停止相关行为、7 天内下架删除、15 天内书面回复，并提到一个新增超过 1.7 万行代码的代码合并请求（PR）\#574。转发这条消息的 Telegram 频道明确说无法核实，只能“当个乐子看”，因此这些目前是函件中的指控，不是已确认的法院裁决或平台公告。

telegram · zaihuapd · 10月21日 09:40

**「背景」** WorkBuddy 是腾讯面向办公场景的 AI 助手，CodeBuddy 是与之并列的编程助手产品；这类产品通常给注册用户一定量的免费额度，用户每天签到即可领取，用完后才需要付费。涉事的 dsh-our-free-model 仓库是一个分享「不填密钥、不注册也能用前沿模型」方法的项目，据第三方介绍页面，它通过 DeepSeek Harness 这类工具提供免费模型入口。律师函里说的「客户端校验」，指软件向服务器发请求时会附上身份信息：UA 是标明软件名称和版本的字符串，产品码标明具体是哪个产品，服务器据此判断请求是否来自官方正版客户端；函件称该插件改写了这些信息。

**「实际影响」** 对普通用户来说，目前没有材料显示 WorkBuddy / CodeBuddy 的免费额度规则已经改变，也没有平台公告说明是否封号；能直接看到的是这个仓库被要求停止并下架。若你正在使用来源不明的插件自动签到、修改客户端标识或批量登录账号，这封函件表明这类做法会被指为绕过校验，相关账号存在被平台限制的风险，但风险是否已经发生无法从现有信息确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.workbuddy.ai/">WorkBuddy - AI Agent for Everyday Office Work</a></li>
<li><a href="https://ai4coding.ru/solutions/Ebony-Vinyl-dsh-our-free-model">dsh - our - free - model — бесплатные фронтир-модели в DeepSeek...</a></li>
<li><a href="https://www.codebuddy.cn/agents/">来自 WorkBuddy 项目的分享</a></li>

</ul>
</details>

**标签**: `#access-restrictions`, `#quota-abuse`, `#legal-takedown`, `#coding-agents`, `#github`

---

<a id="item-tech-news-21"></a>
### [OpenAI 模型将进驻 Google Cloud 企业模型目录](https://openai.com/index/openai-models-google-cloud/) ⭐️ 5.0/10

OpenAI 与 Google Cloud 宣布，OpenAI 的前沿模型（能力最强的一批模型）和 Codex 智能体工作流（让 AI 自动编写和修改代码的一套流程）将进入 Google Cloud 的 Model Garden。Model Garden 是 Google Cloud 上的模型目录，企业可以在 Marketplace（云服务应用商店）里购买，并用已承诺的 Google Cloud 消费额度抵扣。双方称这些模型还会进入谷歌的 Antigravity 和 Gemini Agent 两款产品，预计数周内开放；OpenAI 同时表示微软仍是其主要云合作伙伴。目前没有公布具体价格、可用区域或确切上线日期。

telegram · zaihuapd · 10月21日 13:40

**「背景」** Google Cloud 的 Model Garden（模型花园）是一个模型目录，企业可以在其中挑选并调用第三方 AI 模型；Marketplace 则是企业采购云服务的商店，GCP 承诺消费额度指企业预先承诺的云支出，可用来抵扣这类采购。Codex 是 OpenAI 的编程智能体（能读写代码并执行开发任务的软件），Antigravity 和 Gemini Agent 是 Google 侧承接这类智能体工作流的产品。

**「实际影响」** 对已经和 Google Cloud 签有消费承诺的企业，未来购买 OpenAI 模型可能不再需要单独走一套采购合同，而是直接从这笔承诺额度里扣；但开放时间只说“数周内”，价格、可用区域和额度均未公布，现在还不能下单。

**标签**: `#openai`, `#google-cloud`, `#codex`, `#model-availability`, `#enterprise-distribution`

---