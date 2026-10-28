---
layout: default
title: "Horizon Summary: 2026-10-28 (ZH)"
date: 2026-10-28
lang: zh
---

> 从 112 条内容中筛选出 17 条重要资讯。

---

**科技新闻**
1. [Codex CLI 实测：配置 100 万上下文，实际报告 82.84 万](#item-tech-news-1) ⭐️ 8.0/10
2. [Codex 命令行工具 0.165.0：新增谷歌云 Vertex AI 接入](#item-tech-news-2) ⭐️ 7.0/10
3. [aiedit：用代码而非提示词阻止 AI 读取指定代码](#item-tech-news-3) ⭐️ 7.0/10
4. [开源大模型网关 Keystone 1.0 发布，可集中管理密钥并按任务难度选模型](#item-tech-news-4) ⭐️ 6.0/10
5. [用语言模型控制机器人：搭建系列第三篇讲传感器与 PID 控制](#item-tech-news-5) ⭐️ 6.0/10
6. [OpenAI 发布 Codex 命令行工具 0.166.0 早期测试版，未附更新说明](#item-tech-news-6) ⭐️ 5.0/10
7. [Survival LLM：装在个人电脑上的离线应急助手](#item-tech-news-7) ⭐️ 5.0/10
8. [GitHub 大会徽章跑起了 Game Boy Color 游戏](#item-tech-news-8) ⭐️ 5.0/10
9. [Liquid AI 发布 LFM3，作为定制图文模型的基础](#item-tech-news-9) ⭐️ 5.0/10
10. [作者称 16GB 显存的 RTX 4070 Ti SUPER 跑本地模型达每秒 125 个 token](#item-tech-news-10) ⭐️ 5.0/10
11. [LiteLLM 短暂被植入登录凭据窃取代码，Railway 撤销全部密钥](#item-tech-news-11) ⭐️ 5.0/10
12. [Habr 作者测试少样本示例能否改善 GLM 与 Haiku 的编码表现](#item-tech-news-12) ⭐️ 5.0/10
13. [dsh 桌面版以管理员运行报 0xC0000142，改用普通用户可解决](#item-tech-news-13) ⭐️ 5.0/10

**财经新闻**
1. [欧盟 11 月起对非欧盟直邮包裹征收 2 欧元处理费](#item-finance-news-1) ⭐️ 7.0/10
2. [微软向约 6 万员工提供自愿离职补偿](#item-finance-news-2) ⭐️ 7.0/10
3. [广电总局发布 IPTV 暂行规定：开机看直播且禁开机广告](#item-finance-news-3) ⭐️ 7.0/10
4. [泡泡玛特三季度营收近腰斩，Labubu 热度消退](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Codex CLI 实测：配置 100 万上下文，实际报告 82.84 万](https://habr.com/ru/articles/1100196/?utm_campaign=1100196&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 8.0/10

一位 Codex CLI 用户在 10 月 27 日发布的实测记录中称，他在配置文件 ~/.codex/config.toml 里把模型上下文窗口（模型一次能读入的文字总量）设为 1,000,000 个词元（token，模型处理文本的最小单位），但 Codex 在 GPT-6.1 Sol 上执行每个任务时仍只报告 828,400。他通过自建模型目录（让命令行工具按自定义参数识别模型的文件）把上限提高到 900,000，并用带校验标记的合成长文本跑通了 890,547 个词元的输入。对照实验的结果更出人意料：同一份输入在 888,330 个词元时，不做任何修改也能通过，尽管界面显示的上限只有 828,400。测试使用的是 Codex CLI 0.163.0，通过 ChatGPT 订阅登录；文中部分数据来自 9 月对 GPT-6 Astra 的测试，作者已单独标注。这是单个用户的博客记录，并非 OpenAI 官方确认的结论。

rss · Habr AI · 10月27日 15:11

**「背景知识」** Codex CLI 是 OpenAI 推出的命令行工具，用户在本机终端里让它读取代码、修改代码（据其开源仓库介绍）。大模型一次能“看见”的文字总量叫上下文窗口，单位是 token：token 是模型切分文字的最小单位，大致相当于英文单词的一小段，因此窗口越大，一次能塞进去的代码和对话越多。Codex CLI 的配置文件 \`config.toml\` 里确实有 \`model\_context\_window\` 这个设置项，公开文档也列了它，但据外部记录，2026 年 4 月 23 日前后提交的 GitHub issue \#19185 反映这些设置“并未被遵守”，另有分析文章提醒，手动覆盖服务器下发的模型目录数值有风险。

**「实际影响」** 对使用 Codex CLI 的付费用户来说，这意味着在 config.toml 里调大 model\_context\_window 不保证会生效，而界面显示的 828,400 也不是硬性上限；按作者未做修改的那次测试，888,330 个词元仍能通过。判断一段代码或文档能否一次放进请求里，不能只依赖这个显示数字。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.alexdunlop.com/writing/codex-cli-config-toml">Codex CLI config . toml (2026): What Actually Works With Non-OpenAI...</a></li>
<li><a href="https://codex.danielvaughan.com/2026/07/26/codex-cli-gpt56-sol-context-window-cap-272k-latency-regression-infrastructure-limits/">The 272K Reality: How GPT-5.6 Sol’s Context Window Cap and July...</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai/ codex : Lightweight coding agent that runs in your...</a></li>

</ul>
</details>

**标签**: `#Codex CLI`, `#context window`, `#GPT-6.1 Sol`, `#config.toml`, `#model catalog`

---

<a id="item-tech-news-2"></a>
### [Codex 命令行工具 0.165.0：新增谷歌云 Vertex AI 接入](https://github.com/openai/codex/releases/tag/rust-v0.165.0) ⭐️ 7.0/10

OpenAI 的 Codex 命令行编程助手（在终端里运行、由模型替你写代码和改代码的工具）发布 rust-v0.165.0。这一版内置了 Google Cloud Vertex AI 接入，用户只要在设置文件里把模型来源写成 model\_provider = &quot;gcp&quot;，就能通过谷歌云调用模型；可选模型清单里还加入了 GPT-6.1 Terra，但更新说明没有介绍这个模型的能力、价格或开放范围。默认行为有两处变化：对支持的模型，对话进行中就能调整「推理力度」（让模型多想一会儿还是快速作答），不必重开对话；新建的用户配置默认启用 memory v2（跨会话记忆，让工具记住之前的偏好和上下文），并支持从其他智能体导入记忆。此外，会话选择器可按代码仓库筛选、按目录分组，方便在多个关联的代码工作副本之间切换。这是一个 0.x 增量版本，不是能力上的大跨越。

github · github-actions\[bot\] · 10月27日 20:09

**「背景」** Codex CLI 是 OpenAI 推出的终端编程助手：用户在命令行窗口里输入任务，AI 代理会读取代码、修改文件并执行命令。它通过 0.x 版本号持续迭代，0.165.0 是在 0.164.0 基础上的一次小版本更新，因此默认设置的调整往往比单个新功能更影响日常使用。这里的“记忆”指工具跨会话保留的项目信息，“推理强度”指模型为回答问题愿意投入多少计算步骤。

**「对日常使用者的实际影响」** 对每天用 Codex 写代码的人来说，升级后最直接的变化是两处默认设置：对话中途可以调整“推理力度”（模型每次回答愿意花多少计算去思考，调高通常更慢但更稳），不用重开会话；新建的配置会默认启用 memory v2（跨会话保留的长期记忆），并支持从其他智能体工具导入记忆。旧配置不会自动改用 v2 记忆，想用新记忆或通过 Google Cloud Vertex AI 调用模型的人，需要新建配置或把模型提供方设置改为 \`gcp\`。模型选择列表里还多了 GPT-6.1 Terra，但发布说明没有交代它和现有模型的区别，实际体验要以你账号里能选的项为准。

**标签**: `#codex-cli`, `#openai`, `#coding-agents`, `#model-catalog`, `#vertex-ai`

---

<a id="item-tech-news-3"></a>
### [aiedit：用代码而非提示词阻止 AI 读取指定代码](https://habr.com/ru/articles/1100200/?utm_campaign=1100200&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 7.0/10

作者发布了名为 aiedit 的开源桌面代码编辑器，用 Python 编写。它允许 AI 编程模型处理整个项目，但看不到被标记为“关闭”的整个文件或单个代码行。与在提示词（给 AI 的指令）中要求模型“不要看这些代码”不同，aiedit 由编辑器代码直接把关闭内容排除在发给模型的请求之外，因此这些内容不会到达模型。项目以 MIT 许可证开源（一种允许他人自由使用和修改的开放源代码许可）；作者同时承认，在同一个模型下，它的代码生成质量仍不如 Claude Code。

rss · Habr AI · 10月27日 15:16

**「背景」** 用 AI 修改代码时，工具通常要把项目文件或选中的代码放进发给模型的请求里；模型只能看到请求中实际包含的内容。提示词（给模型的文字指令）只能要求模型“别看”，却无法让内容在请求发出前消失。aiedit 因此把“排除某些文件或某些行”做成编辑器代码里的规则，在请求发出前直接剔除这些内容。

**「实际影响」** 对使用 AI 编程工具的人来说，这套机制可以把不想让模型看到的文件或代码行排除在请求之外，而不必依赖模型自觉遵守指令。代价是模型能参考的上下文变少，作者也表示生成质量仍落后于 Claude Code；按文章描述，这套保护是在 aiedit 编辑器内部实现的，使用者需要在这个独立的桌面编辑器里打开项目。

**标签**: `#coding agents`, `#AI code editor`, `#open source`, `#context privacy`, `#developer tooling`

---

<a id="item-tech-news-4"></a>
### [开源大模型网关 Keystone 1.0 发布，可集中管理密钥并按任务难度选模型](https://habr.com/ru/articles/1099790/?utm_campaign=1099790&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

开源项目 Keystone（全称 Keystone. The Model Switchboard，简称 KTMS）发布 1.0 版：这是一个用 Go 语言编写、可以装在自己服务器上的大模型网关（统一接住各个程序的请求、再转给不同 AI 模型的中间层），采用 Apache 2.0 许可证，可免费使用和修改。它把各家模型厂商的 API 密钥（程序调用付费接口时用来验证身份的字符串）集中到一处，调用方只需说明任务有多复杂，由网关决定调用哪个模型、用哪把密钥，或者干脆把请求交给自己的显卡处理。随 1.0 一起发布的还有网页管理后台 ktms-admin 和费用统计工具 light-tokenmeter，三者都用 Go 编写；作者称它空闲时只占 7 MiB 内存，并承诺 1.x 版本内接口不会做不兼容的改动。文中对功能的描述对应的是 1.3 版，但没有给出安装步骤、性能测试或第三方验证。

rss · Habr AI · 10月27日 08:31

**「什么是大模型网关」** 大模型网关（LLM gateway，也常被叫作 API 代理或中转服务）是夹在自家程序和模型厂商之间的一层软件：程序只把请求交给它，由它决定调用哪家模型、带上哪把厂商密钥（向模型厂商证明「这个请求是我发的」的账号凭证）。这类工具的共同卖点是集中保管密钥、按规则分流请求并统计花费；Keystone 的官方介绍同样把它定位为用 Go 编写的自托管网关，与 light-tokenmeter、ktms-admin 配合完成密钥保管、按任务难度路由、故障切换和消费上限。

**「实际影响」** 对同时维护多个 AI 应用的人来说，换模型、换厂商或把请求切到本地显卡，只需改网关一处配置，不必逐个服务改代码，密钥也不再散落在各个项目的配置里。代价是这台网关要自己部署和维护，而且所有厂商密钥都汇聚在它身上，一旦被攻破，损失比分散保管更大。另外，“按任务复杂度自动选模型”依赖调用方自己判断并标注难度，文章没有给出选型准确率的数据；由于缺少独立测试，正式接入前最好先在测试环境里跑一遍自己的请求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai-process.dev/">ai - process — open-source infrastructure for production LLMs</a></li>

</ul>
</details>

**标签**: `#LLM gateway`, `#API proxy`, `#open source`, `#cost tracking`, `#self-hosted`

---

<a id="item-tech-news-5"></a>
### [用语言模型控制机器人：搭建系列第三篇讲传感器与 PID 控制](https://habr.com/ru/articles/1089244/?utm_campaign=1089244&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 6.0/10

一位俄语作者在 Habr 上发表了系列文章的第三篇，主题是如何从零搭一个由语言模型（LLM，像 ChatGPT 那样能理解并生成文字、也能被要求做决定的模型）控制的机器人。按文章自己的说明，这一篇是全技术内容：指南针、陀螺仪、PID（一种按偏差不断自动修正动作的控制方法）、让模型反复“观察—决策—行动”的智能体循环（agent loop），以及接入四家不同厂商的语言模型和 ffmpeg（处理音视频的工具）。作者称整个系列分十七个章节、前后投入约两百小时。需要注意的是，目前能看到的只是导语和指向正文的链接，导语中并没有确认公开的源代码、零件清单或可照做的安装步骤，也没有第三方验证这个机器人确实能正常工作。

rss · Habr AI · 10月27日 06:41

**「前情与项目背景」** 这是作者 stg34 在 Habr 上连载的第三篇。前作《我把神经网络放进现实世界——然后就不好笑了》记录了让 AI 走出屏幕、去操控现实设备的尝试（该文列在作者本人的 Habr 文章列表里）；作者名下还有一个名为 robo-llm 的 GitHub 仓库，但本篇给出的只是导语，尚未展示代码或零件清单。按作者说法，整个项目共 17 个章节、约 200 小时工作量，本篇覆盖罗盘、陀螺仪、PID 控制（一种根据偏差反复微调、让设备稳定到达目标位置的自动调节方法）、智能体循环（让模型不断「看当前状态—决定下一步动作」的流程）以及四家 LLM 服务商。

**「对动手者的意义」** 对想自己做一个“会听指令的机器人”的爱好者来说，这篇提供的是分模块的搭建思路，尤其是传感器读数和 PID 修正这两块——它们决定了机器人能不能走直线、会不会转错方向。但由于导语没有给出零件清单和代码，读者现在还不能照着复现；要判断值不值得跟做，得先看正文里有没有可下载的代码和明确型号的硬件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/stg34/robo-llm/tree/main">GitHub - stg34/robo-llm</a></li>
<li><a href="https://habr.com/ru/users/stg34/articles/">Статьи / Профиль stg 34 / Хабр</a></li>

</ul>
</details>

**标签**: `#LLM robotics`, `#DIY robot`, `#PID control`, `#agent loop`, `#hardware`

---

<a id="item-tech-news-6"></a>
### [OpenAI 发布 Codex 命令行工具 0.166.0 早期测试版，未附更新说明](https://github.com/openai/codex/releases/tag/rust-v0.166.0-alpha.1) ⭐️ 5.0/10

OpenAI 在 GitHub 上发布了 Codex CLI 的 0.166.0-alpha.1 版本，但发布页只有版本号，没有任何更新说明、改动清单或修复列表。Codex CLI 是 OpenAI 推出的命令行工具（在电脑的终端窗口里用文字指令操作），可以让它的编程助手直接读取项目文件、修改代码并执行命令。版本号里的 alpha 表示这是面向早期测试者的预览版，通常先于正式版出现，稳定性没有保证。由于官方没有说明这一版改了什么，目前无法判断它与上一版的实际差别，也无法确认是否修复了某个具体问题。

github · github-actions\[bot\] · 10月27日 01:33

**「背景」** Codex CLI 是 OpenAI 的编程助手工具，用户在终端（以文字命令操作的界面）里输入需求，让它协助编写和修改代码。版本号中的 alpha 表示这是稳定版之前的早期测试版，功能和表现都可能随时变化。

**「对使用者的实际影响」** 对不使用这款工具的人没有影响。正在使用 Codex CLI 的人，如果只是日常写代码，没必要为了这个版本专门升级，因为它既没有说明修复了什么，也带着早期测试版的不稳定风险；若遇到具体故障并想尝试新版，建议先保留旧版本，以便出问题时回退。

**标签**: `#codex-cli`, `#coding-agents`, `#openai`, `#release`, `#developer-tooling`

---

<a id="item-tech-news-7"></a>
### [Survival LLM：装在个人电脑上的离线应急助手](https://www.brangus.io/survival-llm) ⭐️ 5.0/10

一个名为 Survival LLM 的项目把一个小型大语言模型（能生成文字回答的 AI 模型）和一套应急参考资料打包在一起，让它在用户自己的电脑上离线运行（不连接互联网）。项目在 Hacker News（一个技术讨论网站）上发布后引发讨论，但现有信息没有说明它具体搭载哪个模型、占用多少空间、需要什么安装步骤。一位评论者引用项目页面的表格称，在内存为 16–31 GB 的 Mac 或 PC 上，它使用 IBM 的 Granite 4.2 8B 模型（8B 指约 80 亿个参数），22 道题答对 14 道，模型本身约 6 GB。它面向停电、断网等紧急情况下的查询，而不是日常通用的 AI 助手。

hackernews · Luc · 10月27日 19:55 · [社区讨论](https://news.ycombinator.com/item?id=50264853)

**「背景：什么叫“跑在自己电脑上”」** 平时用的 AI 助手（比如 ChatGPT）其实是把问题发到公司的数据中心，由那里的机器算出答案再传回来，所以断网就用不了。所谓“本地模型”，是把模型文件整个下载到自己电脑上，用本机的处理器运算，因此没有网络也能回答，提问也不会离开这台机器；代价是模型必须足够小，才能塞进普通电脑的内存里。这个项目在介绍页上给出的配置是：内存 16–31 GB 的 Mac 或 PC 搭配 IBM 的 Granite 4.2 8B 模型（Granite 是 IBM 公开发布、可自由下载的一族模型，8B 指 80 亿参数，参数量大致对应模型大小和对硬件的要求）。

**「实际影响」** 如果你把它当作断网时的应急查询工具，实际要先看两件事：自己的电脑是否有 16–31 GB 内存（按评论者引用的项目页面数据），以及能否接受这个小模型给出的答案出错。更稳妥的用法是让它帮你找到相关资料，再把关键结论对照离线保存的原文，尤其是医疗和手术类问题。

**「社区讨论」** 评论区的核心分歧是：既然模型和资料库都不大，为什么不直接做一个可搜索的静态资料包？有评论者以 Kiwix（把维基百科等网站打包成离线可搜索文件的工具）为例，认为那样更可靠、开销更小；也有人主张把模型只当作搜索入口，用语义搜索（按意思相近程度找内容，而不只是匹配关键词）帮人找到原文，而不是信任它直接给建议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.brangus.io/survival-llm">Survival LLM</a></li>
<li><a href="https://github.com/anonnerdfrenzy/survival-llm">anonnerdfrenzy/ survival - llm : A free AI assistant and survival library ...</a></li>
<li><a href="https://www.ibm.com/granite">Granite | IBM</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#self-hosted`, `#offline-ai`, `#open-weight-models`, `#emergency-preparedness`

---

<a id="item-tech-news-8"></a>
### [GitHub 大会徽章跑起了 Game Boy Color 游戏](https://simonwillison.net/2026/Oct/27/game-boy-color-on-my-conference-badge/) ⭐️ 5.0/10

在 GitHub 于本周举办的 Universe 大会（GitHub 一年一度的开发者大会）上，参会者拿到的胸牌本身是一台带彩色屏幕的小电脑。开发者 Steve Francia 借助谷歌的 Gemini 模型让它跑起了任天堂红白机（NES）的模拟器（在一台设备上用软件模仿另一台旧游戏机的程序），随后又做出了 Game Boy 和 Game Boy Color 掌机的模拟器。Simon Willison 在博客中贴出照片，显示这块徽章正以全彩运行《塞尔达传说：织梦岛》，前提是你自己手里有这款游戏的 ROM（把游戏卡带内容拷贝出来的文件）。把徽章倒过来拿，机身自带的触摸按键就成了游戏手柄。这篇帖子只给出结果和链接，没有代码、零件清单或安装步骤，具体做法写在 Francia 自己的博客里。

rss · Simon Willison · 10月27日 19:34

**「背景」** 模拟器是一类软件，让一台设备“假装”成另一台设备，从而运行原本为别的机器编写的游戏。GitHub Universe 是 GitHub 每年举办的开发者大会，据 Simon Willison 记录，2025 年那届的参会胸牌就已经是一台带彩色屏幕的小电脑，今年的胸牌延续了这一做法，所以同一块硬件上再次出现了改装玩法。Steve Francia 先让一个完整的任天堂 NES 模拟器在胸牌上跑起来，随后又进一步扩展到 Game Boy 和 Game Boy Color 两种机型的模拟器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Oct/27/game-boy-color-on-my-conference-badge/">Game Boy Color on My Conference Badge | Simon Willison’s Weblog</a></li>

</ul>
</details>

**标签**: `#emulation`, `#game-boy`, `#hardware-hacking`, `#gemini`, `#conference-badge`

---

<a id="item-tech-news-9"></a>
### [Liquid AI 发布 LFM3，作为定制图文模型的基础](https://huggingface.co/blog/LiquidAI/lfm3) ⭐️ 5.0/10

10 月 27 日，Liquid AI 在 Hugging Face 的博客上发文介绍 LFM3，从标题看，讲的是如何以这个模型为基础，构建面向特定用途的多模态模型（能同时处理文字、图像等不同类型输入的模型）。但公开出来的只有标题和来源，正文内容、模型权重（训练好的模型文件）的下载入口、参数规模、许可证条款和性能测试数据都没有出现，所以目前无法确认它是否已经可以直接下载使用、需要什么配置的电脑或显卡，以及允许哪些用途。

rss · Hugging Face Blog · 10月27日 17:16

**「背景：LFM 是什么」** LFM 是 Liquid AI 的“液态基础模型”系列（Liquid Foundation Models），主打让模型直接跑在手机、笔记本等设备上，而不是只放在云端。据 Liquid AI 的发布页和第三方解读，LFM3 是该系列的新一代开放权重模型家族，规模在 20 亿参数上下（参数可粗略理解为模型的“体量”，越大通常越吃算力），分成文字、图像与视频、音频、“全模态”和“决策”等几种版本，官方称可在单块显卡上做微调。这里的“开放权重”指模型文件可以下载下来自己运行和改造，但具体能商用与否要看官方许可条款；本条目提供的原文只有标题、没有正文，上述细节来自外部介绍而非原帖核对。

**「实际影响」** 如果你关心的是在手机、笔记本或私有服务器上运行能处理文字、图片和声音的模型，这一系列的价值在于：模型权重公开，可用一张显卡拿自己的数据做微调（在已有模型上继续训练），再部署到本地。但其中的 1.7B 文本版（约 17 亿参数）被明确标注不适合智能体编程（能自己调用工具、分多步完成任务的程序）和复杂多步推理，知识密集型任务也建议外接检索，选型时不要把它当成通用大模型的替代品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.liquid.ai/blog/lfm3">Introducing LFM3: Every Modality for Specialized Intelligence</a></li>
<li><a href="https://explainx.ai/blog/liquid-ai-lfm3-open-weight-2b-family-text-vision-audio-omni-decision-models-2026">Liquid AI LFM3: Open 2B Models for Text, Vision, Audio ...</a></li>
<li><a href="https://www.liquid.ai/models">Liquid Foundation Models | Liquid AI</a></li>
<li><a href="https://www.liquid.ai/blog/lfm3">Introducing LFM 3 : Every Modality for Specialized Intelligence | Liquid AI</a></li>
<li><a href="https://huggingface.co/LiquidAI/LFM3-1.7B">LiquidAI/ LFM 3 -1.7B · Hugging Face</a></li>
<li><a href="https://www.marktechpost.com/2026/10/27/liquid-ai-lfm3-open-weight-2b-multimodal-models/">Liquid AI Releases LFM 3 : 6 Open-Weight 2B-Class Multimodal Models</a></li>

</ul>
</details>

**标签**: `#lfm3`, `#liquid-ai`, `#open-weight-models`, `#multimodal`, `#fine-tuning`

---

<a id="item-tech-news-10"></a>
### [作者称 16GB 显存的 RTX 4070 Ti SUPER 跑本地模型达每秒 125 个 token](https://habr.com/ru/articles/1099962/?utm_campaign=1099962&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位作者在 Habr 上发文称，他用一张 16 GB 显存的 NVIDIA RTX 4070 Ti SUPER 显卡（目前约 900 美元）在本机运行大语言模型，速度达到每秒 125 个 token（token 是模型读写文本的最小单位，大致相当于一个词或半个词），足以支撑一个编程助手连续工作。作者给出的对照是：过去在这类显卡上跑一个约 270 亿参数的“稠密”模型（每生成一个字都要调用全部参数），只有每秒 10–20 个 token，而顺手使用编程助手需要每秒 100–150 个。但公开出来的只有文章开头，没有写明用的是哪个模型、做了何种量化（把模型参数压到更低精度以便塞进显存）、用哪套运行软件以及具体配置，因此这个速度目前既无法核对，也无法照搬。

rss · Habr AI · 10月27日 09:20

**「背景：令牌速度与显存限制」** 这里说的大语言模型，是那种用大量文本训练、能生成文字和代码的软件；令牌（token）是它读写文本的小单位，每秒令牌数就是它的生成速度。原文以 Qwen 3.8 27B 这类“稠密”模型为例：稠密意味着每生成一个令牌都要经过全部约 270 亿个参数，因此在这类 16GB 显存的显卡上，通常要把模型压缩精度（量化）才放得下，而原文给出的速度只有 10–20 令牌/秒。写代码的智能体（会反复读文件、改代码、运行命令的程序）需要多轮生成，原文因此把 100–150 令牌/秒视为比较顺手的门槛。

**「实际影响」** 对想在自己电脑上跑编程助手的人来说，这条消息暂时还不能变成可执行的方案：本地生成速度由“模型有多大”“压缩到什么程度”“用哪套软件跑”三者共同决定，任何一环不同，每秒 125 个 token 的结果都可能不成立。作者引用的 GaugeDB 调查称，16 GB 显存的显卡占桌面用户的 27.21%，是最常见的一档，所以很多人会关心这个数字是否真实；在拿到模型名称和配置清单之前，不宜按它来决定买哪张卡。

**标签**: `#local-llm`, `#coding-agents`, `#gpu-inference`, `#open-weight-models`, `#consumer-hardware`

---

<a id="item-tech-news-11"></a>
### [LiteLLM 短暂被植入登录凭据窃取代码，Railway 撤销全部密钥](https://habr.com/ru/articles/1099718/?utm_campaign=1099718&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一篇俄语安全周报的摘要称，LiteLLM（供开发者统一调用多家大模型服务的软件组件）曾带着窃取登录凭据的代码出现在 PyPI（Python 的公共软件包仓库）上，前后不到两小时；事件发生后，云服务商 Railway 撤销了全部 API 令牌（调用其服务时使用的密钥）。这直接关系到那段时间安装或更新过 LiteLLM 的开发者，以及使用 Railway 并依赖这类令牌的用户，因为被盗的密钥可能被用来冒用其账号或消耗其付费额度。摘要没有给出受影响版本、恶意版本标识、泄露迹象或具体补救步骤，因此目前无法判断哪些安装一定中招。

rss · Habr AI · 10月27日 07:00

**「先弄清 LiteLLM 是什么」** LiteLLM 是一个开源中间层软件：开发者把它放在自己的程序和各家 AI 模型之间，用同一套接口去调用 OpenAI、Anthropic 等不同厂商的模型，所以它通常保管着多家服务的付费密钥。它通过 PyPI（Python 语言的公共软件包仓库，开发者敲一条命令就能装上）分发给使用者。据安全媒体记录，2026 年 10 月 21 日发布的 1.107.0 版本里被塞进了窃取登录凭据的代码，分发出去的七个安装文件全部受影响；Socket 的复盘文章还把这次事件追溯到一枚此前被公开泄露的主密钥。

**「对使用者的实际影响」** 如果你所在的团队用 LiteLLM 这类中间软件统一调用多家 AI 服务，需要把 10 月 21 日发布的 v1.107.0 视为高风险版本：LiteLLM 官方说明称该版本被推送到 PyPI 和 Docker 镜像库，内含窃取登录凭据的恶意代码，Datadog 的安全分析也提到发布者账号遭到入侵。当时配置在其中的 OpenAI、Anthropic 等服务密钥（调用接口用的付费凭证）应视为可能已泄露并立即更换，同时核对安装记录并回退到未受影响版本；这篇汇总还提到 Railway 在事件后撤销了所有 API 令牌，依赖这些令牌的自动部署或应用会失效，需要重新授权。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dev.to/romdevin/leaked-litellm-master-key-exploited-to-compromise-github-release-malicious-pypi-and-container-dc4">Leaked LiteLLM Master Key Exploited to... - DEV Community</a></li>
<li><a href="https://socket.dev/blog/litellm-attack-timeline">New Evidence Shows LiteLLM Secret- Stealing Workflows... | Socket</a></li>
<li><a href="https://cybersecuritynews.com/litellm-compromised/">LiteLLM Compromised - Hackers Injected an Infostealer and RAT in...</a></li>
<li><a href="https://docs.litellm.ai/blog/security-incident-oct-21-2026">Contained: Oct 21, 2026 LiteLLM release v1.107.0 Compromised</a></li>
<li><a href="https://securitylabs.datadoghq.com/articles/litellm-compromised-pypi-docker/">LiteLLM supply chain compromise: What you need to know</a></li>

</ul>
</details>

**标签**: `#litellm`, `#supply-chain-security`, `#api-keys`, `#llm-proxy`, `#security-roundup`

---

<a id="item-tech-news-12"></a>
### [Habr 作者测试少样本示例能否改善 GLM 与 Haiku 的编码表现](https://habr.com/ru/articles/1099792/?utm_campaign=1099792&amp;utm_source=habrahabr&amp;utm_medium=rss) ⭐️ 5.0/10

一位 Habr 作者发文说，他做了两个小型非正式实验：在已有的任务约定和自动检查之上，再给模型加几个“照着做”的范例（业内叫少样本提示，即在提问里附上几个正确样例），看能否让 GLM 和 Claude Haiku 这两个可用于写代码的 AI 模型在实现任务时少犯糊涂，并试着把这套做法写进工作流程。但公开出来的内容只有开头：没有提示词、配置、对比数字，也没有可复现的结果，作者本人也明确说这不算严格的实验。所以目前只能知道他打算测什么，无法判断是否有效。

rss · Habr AI · 10月27日 04:30

**「背景」** Few-shot（少量示例提示）指的是在给 AI 的任务说明里附上几个「输入—正确输出」的样例，让模型照着样子做，而不是只靠一句指令去猜格式和标准。文中提到的 GLM 和 Claude Haiku 都是能写代码、承接实现任务的模型：前者被作者当作处理大批量工作的「劳力」，后者是 Anthropic 主打速度与成本的小型模型。作者所说的「契约」和「自动检查」，指他工作流程里已有的接口约定和跑一遍就能判断对错的测试；这次要验证的是在这两层之上再加几个示例，能不能让模型少跑偏。据文中交代，他先在本机运行的小模型上试了一轮，再换到 GLM 和 Haiku，共两轮，并明确说明这不具备学术上的严谨性。

**「对使用者的实际影响」** 对平时用这类模型写代码的人来说，眼下还没有能照搬的做法：文章没给示例数量、提示词写法或前后对比，无法判断在已有自动检查之外再加范例是否值得。要等完整数据公布，才谈得上调整自己的工作流程。

**标签**: `#few-shot prompting`, `#GLM`, `#Claude Haiku`, `#coding agents`, `#prompt engineering`

---

<a id="item-tech-news-13"></a>
### [dsh 桌面版以管理员运行报 0xC0000142，改用普通用户可解决](https://linux.do/u/gangpula32) ⭐️ 5.0/10

论坛用户 gangpula32 发帖称，dsh 桌面版的 workspace-write 模式（允许 AI 代理在电脑上写文件、执行命令的一种工作模式）启动 shell（命令行窗口）时，会报错 0xC0000142。他的判断是：原因在于 dsh 进程的“令牌”权限过高（令牌是 Windows 发给每个程序的权限凭证，管理员启动的程序拿到的是高完整性级别），而该模式只接受 Medium（中等）完整性级别，所以启动失败。给出的两种做法是：不以管理员身份运行 dsh，改普通用户身份启动；或者继续用超级管理员运行，但给内置 Administrator 账户设置 FilterAdministratorToken=1 并重启系统，帖主称这样宿主进程同样会降到 Medium 完整性，问题消失。这是单个用户在自有环境中的经验帖，没有写明 dsh 的版本号，也没有官方确认或可复现步骤。

telegram · linuxdo\_tg · 10月28日 00:42

**「背景：Windows 的权限级别」** Windows 启动程序时会附带一个“令牌”（记录该程序以什么权限运行的凭证），并按完整性级别区分：普通用户通常是 Medium，管理员提权后是 High。系统内置的 Administrator 账户默认不受 UAC（Windows 的权限确认弹窗）限制，直接以 High 运行；将 FilterAdministratorToken 设为 1 后，它也会先以 Medium 启动、需要时再请求提权，这正是发帖人让 dsh 以 Medium 级别运行的办法。

**「对使用者的实际影响」** 如果你在 Windows 上用这类桌面 AI 工具，遇到同样的报错，可以先试最简单的做法：不要“以管理员身份运行”，直接用普通账户双击打开，再让它执行命令。帖主的第二种方案是对内置 Administrator 账户做系统级设置并重启，属于对自己电脑权限策略的改动，他只在自己的机器上验证过，会影响该账户的其它行为，动手前值得先确认是否真的需要以管理员身份跑这个工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-gpsb/7c705718-f58e-4886-8057-37c8fd9aede1">[MS-GPSB]: FilterAdministratorToken | Microsoft Learn</a></li>
<li><a href="https://docs.0xkholod.com/002-pentesting/windows-pentesting/filteradministratortoken">FilterAdministratorToken</a></li>
<li><a href="https://learn.microsoft.com/en-us/windows/security/application-security/application-control/user-account-control/settings-and-configuration">User Account Control settings and configuration UAC hardening and Windows Administrator protection Tutorial GPO - Enable FilterAdministratorToken User Account Control approval mode for the built-in ... UAC Bypass - DFIR Handbook</a></li>

</ul>
</details>

**标签**: `#coding-agents`, `#sandbox`, `#windows`, `#troubleshooting`, `#developer-tooling`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [欧盟 11 月起对非欧盟直邮包裹征收 2 欧元处理费](https://www.luxtimes.lu/europeanunion/new-levy-on-non-eu-parcels-kicks-in-november-1/163611818.html) ⭐️ 7.0/10

欧盟将从 2026 年 11 月 1 日起，对从欧盟以外直接寄给消费者的包裹按每件商品征收 2 欧元处理费，不论包裹价值。该费用由电商平台、卖家及中间商缴纳；欧盟称此举用于补偿海关处理大量包裹的成本，另有一项针对低价值小包裹的 3 欧元费用，暂行至 2028 年 7 月 1 日。

telegram · zaihuapd · 10月27日 02:30

**「背景」** 这一收费建立在欧盟海关改革的第一步之上：自 2026 年 7 月 1 日起，欧盟已对价值不超过 150 欧元的入境小包裹按每件商品征收 3 欧元海关关税，而 11 月 1 日起的 2 欧元处理费是在此之外新增的长期收费。

**「谁受影响」** 对从欧盟以外购买低价商品的消费者和跨境卖家来说，每件包裹的固定成本会叠加：欧盟自 2026 年 7 月 1 日起已对低价值包裹按件征收 3 欧元临时关税，11 月 1 日起再新增 2 欧元处理费；这笔费用由电商平台、卖家和中间商缴纳，可能通过涨价转嫁给买家。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.revenue.ie/en/customs/individuals/union-handling-fee/index.aspx">Union Handling Fee (UHF) – 1 November 2026 - revenue.ie</a></li>
<li><a href="https://trade.ec.europa.eu/access-to-markets/en/news/eu-applies-eu3-customs-duty-item-low-value-e-commerce-consignments">EU applies €3 customs duty per item on low-value e-commerce ...</a></li>

</ul>
</details>

**标签**: `#EU trade policy`, `#cross-border e-commerce`, `#customs fees`, `#consumer prices`, `#parcel logistics`

---

<a id="item-finance-news-2"></a>
### [微软向约 6 万员工提供自愿离职补偿](https://www.bloomberg.com/news/articles/2026-10-26/microsoft-to-offer-buyouts-to-60-000-workers-in-latest-cost-cut) ⭐️ 7.0/10

据彭博报道，微软向美国、加拿大、印度和英国的约 6 万名副总裁及以下员工提供自愿离职补偿，覆盖 Xbox、Windows、Copilot 和财务等部门，数据中心、销售和营销等岗位不在范围内。微软发言人称该方案接近标准遣散方案；截至 6 月底公司员工总数为 22.3 万人，此次并非已确认的裁员，也未公布接受人数。

telegram · zaihuapd · 10月27日 03:09

**「背景」** 截至 6 月底，微软全球员工约 22.3 万人；据路透社，此次约 6 万名符合条件者占其全球员工四分之一以上，公司称此举意在控制成本。此前 7 月，微软已向接近退休年龄的员工提供过类似自愿离职方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/technology/microsoft-is-offering-buyouts-around-60000-employees-business-insider-reports-2026-10-26/">Microsoft offers buyouts to around 60,000 employees to ...</a></li>
<li><a href="https://www.cnbc.com/2026/10/26/microsoft-msft-voluntary-buyouts.html">Microsoft offers voluntary buyouts to 60,000 employees - CNBC</a></li>

</ul>
</details>

**标签**: `#Microsoft`, `#workforce restructuring`, `#voluntary buyouts`, `#cost cutting`, `#technology sector`

---

<a id="item-finance-news-3"></a>
### [广电总局发布 IPTV 暂行规定：开机看直播且禁开机广告](https://www.nrta.gov.cn/art/2026/10/27/art_1588_74296.html) ⭐️ 7.0/10

国家广播电视总局发布《交互式网络电视运营服务管理暂行规定》，自 2026 年 11 月 27 日起施行，要求 IPTV 实现开机看全屏直播、不得播放开机广告，并允许用户自行选择进入直播或交互主页。

telegram · zaihuapd · 10月27日 05:59

**「背景」** IPTV 指通过宽带网络向电视用户提供直播和点播内容的电视服务，此次规定针对其开机界面、内容分区和收费展示。

**「影响」** 受影响最直接的是 IPTV 运营方和智能电视厂商：前者不能再播放开机广告，后者需支持直播频道优先呈现和遥控器一键切换直播信源。

**标签**: `#IPTV regulation`, `#broadcasting policy`, `#startup advertising`, `#smart TVs`, `#consumer media rules`

---

<a id="item-finance-news-4"></a>
### [泡泡玛特三季度营收近腰斩，Labubu 热度消退](https://asia.nikkei.com/business/consumer/pop-mart-s-revenue-halves-in-q3-as-labubu-craze-cools) ⭐️ 7.0/10

Pop Mart disclosed a 45-50% year-over-year Q3 revenue decline as Labubu demand cooled, with overseas sales falling much faster and gross margin expected to narrow.

telegram · zaihuapd · 10月27日 14:30

**标签**: `#Pop Mart`, `#Q3 revenue decline`, `#Labubu`, `#consumer discretionary`, `#gross margin`

---