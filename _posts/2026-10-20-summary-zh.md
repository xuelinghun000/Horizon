---
layout: default
title: "Horizon Summary: 2026-10-20 (ZH)"
date: 2026-10-20
lang: zh
---

> 从 44 条内容中筛选出 13 条重要资讯。

---

**科技新闻**
1. [SGLang v0.5.22 发布：新增多款模型并提升吞吐](#item-tech-news-1) ⭐️ 7.0/10
2. [自制单电机无人机：用铰链和扭矩调制控制桨距](#item-tech-news-2) ⭐️ 7.0/10
3. [Wine 的 Windows 兼容层移植到 OpenBSD](#item-tech-news-3) ⭐️ 7.0/10
4. [Mac.apk 尝试在 Apple Silicon Mac 上原生运行 Android 应用](#item-tech-news-4) ⭐️ 7.0/10
5. [Mistral 宣布 Timestral 时间序列基础模型系列](#item-tech-news-5) ⭐️ 7.0/10
6. [HN 讨论：如何交付自己不完全理解的 AI 生成代码](#item-tech-news-6) ⭐️ 7.0/10
7. [Plex 漏洞据报遭在野利用植入挖矿程序](#item-tech-news-7) ⭐️ 7.0/10
8. [SemiAnalysis：2027 年数据中心建设或加速，年增 50GW](#item-tech-news-8) ⭐️ 7.0/10
9. [XNU 内核移植至红米 Note 10 Pro，启动 iOS 16 用户空间](#item-tech-news-9) ⭐️ 7.0/10
10. [美国国土安全部下令联邦文职部门排除并移除 DeepSeek 产品](#item-tech-news-10) ⭐️ 7.0/10

**科技博客**
1. [技术领域的艺术论证需连回实际效用](#item-tech-blog-1) ⭐️ 6.0/10

**财经新闻**
1. [摩根大通首年向国防与制造初创企业投资 50 亿美元](#item-finance-news-1) ⭐️ 7.0/10
2. [三星、SK 海力士股价下跌，韩国养老金所持股份估值缩水 1370 亿美元](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [SGLang v0.5.22 发布：新增多款模型并提升吞吐](https://github.com/sgl-project/sglang/releases/tag/v0.5.22) ⭐️ 7.0/10

SGLang 发布 v0.5.22，合并了来自 245 位贡献者的 950 个 PR，新增 Clef/Clef Flash、PPLX-Decider v1/v1.1、EmbeddingGemma 2、LLaDA2.2，以及 HunyuanImage-3.0-Instruct、Kandinsky 6、Wan-Animate-2、SANA-Video 2.0、LLaDA-Image 等扩散模型支持。发布说明称，DeepSeek-V4.1 在 H200 上每 GPU 吞吐最高提升 2.3 倍，并可在 AMD MI350X/MI355X 上运行；新的 InstantTensor 加载器使模型加载快 10 倍。该版本还修复了混合线性模型在推测解码与结构化输出同时使用时可能从错误 mamba 状态恢复的问题。升级要求 Python 3.11 或更高版本，并提供 NVIDIA CUDA 13、AMD MI35x/MI30x、Intel GPU 和 Intel CPU 的 Docker 镜像。

github · ch-wan · 10月19日 02:55

**「发布背景」** SGLang 是开源的模型推理与服务框架，其新模型接入和性能优化以连续的 0.5.x 点版本（如本次 v0.5.22）陆续合入，因此升级通常叠加在此前版本已有的部署配置之上。升级前需要确认的环境前提是：从 v0.5.22 起要求 Python 3.11 或更高版本，且按发布说明需带 \`--prerelease=allow\` 参数安装。

**「影响」** 现有部署在升级前需确认 Python 版本不低于 3.11，并按硬件选择对应的新镜像；Apple Silicon Mac 用户现在可通过标准 PyTorch 后端运行 SGLang，同时仍保留 MLX 路径。

**标签**: `#SGLang`, `#LLM inference`, `#model serving`, `#diffusion models`, `#open source`

---

<a id="item-tech-news-2"></a>
### [自制单电机无人机：用铰链和扭矩调制控制桨距](https://www.youtube.com/watch?v=Ndftcft6XhU) ⭐️ 7.0/10

一段建造视频展示了一架只用一个电机的无人机：它借助特制铰链、磁编码器和扭矩调制，在旋翼旋转时改变桨距来控制升力，绕开了传统直升机所需的斜盘。视频条目的概述将其描述为可飞行的自制硬件与控制探索，而非厂商产品发布。不过有评论者指出，单电机方案会让机体一离地就持续自旋。

hackernews · hakonjdjohnsen · 10月19日 09:05 · [社区讨论](https://news.ycombinator.com/item?id=50150089)

**「背景」** 传统直升机和多旋翼依靠斜盘（swashplate）等连杆机构周期性地改变桨叶迎角，从而产生升降与操纵力矩，这也是其机械结构复杂的主要原因。此前已有不依赖斜盘的方案，例如让两个无刷电机按周期加减速来产生侧向力和力矩（tool-2-3），说明“用扭矩或转速调制替代复杂变距机构”是一条已被探索过的控制思路。

**「复现影响」** 对想复现的爱好者来说，真正要处理的是特制铰链、编码器反馈和扭矩调制的控制调参，而不只是少装一个电机；这也意味着机械结构简化的代价被转移到了控制软件上。

**「社区讨论」** 评论者把该项目与固定翼 RC 4D 特技中的变距螺旋桨、BattleBots 中仅靠单个电机转速控制运动的欠驱动机器人相提并论，认为这是欠驱动控制的一个有趣实例。也有人提醒单电机机体在空中会持续自旋，并推测双电机加尾桨会更实用；这些属于爱好者经验和判断，而非独立测试结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://electronics.stackexchange.com/questions/383671/how-this-flying-copter-actually-work">brushless dc motor - How this flying copter actually work - Electrical...</a></li>

</ul>
</details>

**标签**: `#robotics`, `#underactuated-control`, `#drones`, `#hardware-hacking`, `#variable-pitch-propulsion`

---

<a id="item-tech-news-3"></a>
### [Wine 的 Windows 兼容层移植到 OpenBSD](https://marc.info/?l=openbsd-ports&amp;m=179236125692175) ⭐️ 7.0/10

Wine 的 Windows 兼容层已被移植到 OpenBSD，相关消息发布在 openbsd-ports 邮件列表。移植者将 OpenBSD 专用修改单独标记，并称其中不少更新在技术上也能运行于其他操作系统，但预计不会有大量改动被合并到上游。现有信息未说明是否已有正式二进制包或官方支持级别。

hackernews · iamnothere · 10月19日 13:35 · [社区讨论](https://news.ycombinator.com/item?id=50152307)

**「背景」** Wine 是一个把 Windows API 调用转换为 POSIX 调用的兼容层，并不是完整模拟 Windows。根据 Adafruit 的报道，此次移植长期卡在 OpenBSD 不允许用户态设置 %gs/gsbase 这一限制上；移植工作改为在软件中模拟相关指令的 %gs 前缀，才使其余部分得以推进。

**「影响」** 对 OpenBSD 用户而言，这个端口提供了在该系统上运行 Windows 程序的途径；但由于改动以 OpenBSD 专用为主且上游合并预计有限，后续应关注 OpenBSD 端口自身的维护，而不是等待 Wine 上游同步。

**「社区讨论」** 评论中，t-3 引用移植者的说明称，OpenBSD 相关改动被特意标记为仅适用于 OpenBSD，因此预计不会有大量内容合并到上游；RunSet 则把这次移植视为 OpenBSD 成为躲避“slopcode”的避风港的又一例证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.adafruit.com/2026/10/19/wine-ported-to-openbsd/">Wine ported to OpenBSD - Adafruit Industries</a></li>

</ul>
</details>

**标签**: `#Wine`, `#OpenBSD`, `#open source`, `#compatibility layer`, `#ports`

---

<a id="item-tech-news-4"></a>
### [Mac.apk 尝试在 Apple Silicon Mac 上原生运行 Android 应用](https://github.com/kksimp/Mac.apk) ⭐️ 7.0/10

开源项目 Mac.apk 尝试让 Android 应用无需模拟器、虚拟机或底层 Linux，直接在 Apple Silicon Mac 上运行。项目将其定位为原生兼容层，但从现有讨论看，它仍处于早期概念验证阶段。社区指出，它把应用数据存放在 .app 包内，而非 macOS 的 Application Support 目录，并且依赖 Google Play 服务的应用可能无法完整运行。

hackernews · flocked · 10月19日 16:45 · [社区讨论](https://news.ycombinator.com/item?id=50154624)

**「背景」** 与模拟器或虚拟机的思路不同，兼容层要让 Android 应用作为普通 macOS 进程直接使用宿主的 CPU 和 GPU，而不是先启动一套完整的 Android 系统。据 APPDOOK 报道，Mac.apk 目前以免费公开 alpha 形式提供，要求 macOS 26.4 或更高版本，并占用约 280MB 磁盘空间；这一版本要求源于它依赖 Apple 在 macOS 26.4 中新增的一项面向包含原生代码应用的能力。

**「影响」** 对想在 Mac 上使用 Android 应用的用户来说，最直接的限制是 Google Play 服务：依赖 GMS 的应用预计无法完整运行，使用前需确认应用是否依赖相关 API。另一个兼容性问题是应用数据被放在 .app 包内，而非 Application Support，用户替换或迁移应用包时要留意数据是否随之保留。

**「社区讨论」** 评论中，irskep 认为把应用数据放进 .app 包而非 Application Support 是奇怪的选择，项目以“文件不会散落在主目录”为由解释，但 irskep 称这是伪选择；bilalq 则认为 Google Play 服务依赖会削弱实用性，不过项目仍然“很酷”。andsoitis 还追问这是否意味着不依赖 JVM，piro0919 则表示自己更希望在 iPhone 上运行 Android 应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/kksimp/Mac.apk-Releases">kksimp / Mac . apk -Releases: MacDroid: Run Android apps natively on...</a></li>
<li><a href="https://appdook.com/news/mac-apk-android-apps-apple-silicon-alpha">Mac . apk runs Android apps on Apple silicon Macs - APPDOOK</a></li>

</ul>
</details>

**标签**: `#android`, `#macos`, `#apple-silicon`, `#compatibility-layer`, `#open-source`

---

<a id="item-tech-news-5"></a>
### [Mistral 宣布 Timestral 时间序列基础模型系列](https://mistral.ai/news/timestral/) ⭐️ 7.0/10

Mistral 宣布推出 Timestral，一个面向时间序列预测的基础模型系列，面向需要做预测的开发者与企业。从现有材料看，模型规模、训练数据、基准结果、许可和可用性均无法确认，因此目前只能视为一项产品公告，尚不能核实其相对专用模型的实际效果。

hackernews · groar · 10月19日 09:59 · [社区讨论](https://news.ycombinator.com/item?id=50150434)

**「背景」** 时间序列基础模型的做法是先在大量来源各异的时间序列上预训练，再以零样本方式对新序列做概率预测，从而避免为每条序列单独建模。据 Mistral 的公告，Timestral 是该公司首个时间序列模型家族，最大模型仅 209M 参数，支持过去与未来协变量，并称其在 GIFT-Eval、TIME 和 fev-bench 三个公开预测基准上位居预训练零样本模型之首，且可在普通 CPU 上运行。

**「影响」** 对同时维护大量序列的团队，采用前应先用自有历史数据做回测，重点验证单一基础模型能否处理不同序列间的尺度差异与领域偏移，而不是直接替换逐序列模型。

**「社区讨论」** HN 评论的争论集中在基础时序模型是否必要：logancbrown 认为，面对 1 万条序列时逐条训练会缺少历史，而单一通用模型又需处理尺度不匹配，这正是基础模型的用武之地；joefourier 则质疑把差异巨大的“时间序列”归入同一模型是否合理。另有评论者以 ChatGPT 的零样本泛化作类比，但对其能否在量化预测等场景兑现表示怀疑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mistral.ai/news/timestral/">Timestral: Mistral&#x27;s time-series foundation models | Mistral</a></li>
<li><a href="https://explainx.ai/blog/timestral-mistral-time-series-foundation-models-209m-cpu-forecasting-2026">Timestral: Mistral Releases Time-Series Foundation Models ...</a></li>
<li><a href="https://opendatascience.com/mistral-launches-timestral-a-new-family-of-time-series-forecasting-models/">Mistral Launches Timestral, a New Family of Time-Series ...</a></li>

</ul>
</details>

**标签**: `#time-series`, `#foundation-models`, `#mistral`, `#forecasting`, `#machine-learning`

---

<a id="item-tech-news-6"></a>
### [HN 讨论：如何交付自己不完全理解的 AI 生成代码](https://news.ycombinator.com/item?id=50151036) ⭐️ 7.0/10

Hacker News 上由 rzk 发起的 Ask HN 帖引述一名 Meta 工程师的 LinkedIn 发言，讨论工程师在交付 AI 生成、自己未完全理解的代码时该如何自处；该工程师称写代码如今像面对黑盒，而逐行核查又赶不上当前的交付节奏。帖子直接询问其他工程师是否有同样感受、又如何处理。回复中没有形成统一做法，讨论主要分成三类：自己掌握抽象与设计、只让模型填充实现；坚持上线前读代码；以及用大量测试来弥补理解不足。

hackernews · rzk · 10月19日 11:24

**「背景」** 在传统软件工程实践中，代码评审、测试和设计文档是团队建立对生产代码共同理解的主要手段，提交者通常也被期望能解释自己交付的逻辑。生成式编码助手能快速产出实现，但这些机制并不会自动保证作者理解代码，因此交付速度与可维护性、责任归属之间的张力变得更加突出。

**「社区观点」** bitwizeshift 主张先自行确定抽象层级与各部分的交互（UML 层面），再让 LLM 只实现空缺，这样仍能说自己理解这套代码；jedberg 把这种分工类比为资深工程师做设计、初级工程师写实现。plastic041 则批评不少评论在回避阅读自己负责的代码，认为至少公司里应有人能解释代码，且测试本身也可能写错；ChrisMarshallNY 表示自己花更多时间做交互式测试，并称发现的多是实现层面的错误而非编码错误。

**标签**: `#AI-assisted coding`, `#software engineering`, `#code review`, `#maintainability`, `#developer practices`

---

<a id="item-tech-news-7"></a>
### [Plex 漏洞据报遭在野利用植入挖矿程序](http://www.boredhackerblog.info/2026/10/plex-vulnerabilities-being-exploited-in.html) ⭐️ 7.0/10

据博客文章和社区报告，Plex 漏洞正被在野利用，用于植入挖矿程序及其他载荷，包括 DDoS 节点；一条被称为 Plex2Shell 的利用链据称由大模型组合多个 CVE 而成。一名评论者称，其家庭服务器运行了 13 个月未更新的版本，在错过 9 月 1 日的升级提醒后 CPU 占用率达到 100%，并发现名为“mylovelyminer”的挖矿进程。另一名用户报告 Mac mini 上出现占用 100% CPU 的“icloud-services”进程，并追踪到 Library 目录；这些都是用户自述，材料中没有 Plex 官方公告或独立分析确认具体 CVE、影响版本与修复状态。

hackernews · mindracer · 10月19日 13:36 · [社区讨论](https://news.ycombinator.com/item?id=50152321)

**「背景：Plex2Shell 利用链」** 公开的 Plex2Shell 利用链把四个 Plex Media Server 漏洞串成未认证远程代码执行；据 SecurityWeek 报道，发现这些漏洞的研究人员于 10 月 16 日发布技术细节和 PoC，攻击者次日便开始尝试利用。安全媒体报道称，已有蜜罐在 10 月 17 日记录到攻击者投放挖矿程序和代理工具。

**「影响与应对」** 运行过时 Plex Media Server 且将服务暴露在公网的用户面临实际风险：评论者报告，在忽略 9 月 1 日的升级提醒后，其使用了 13 个月的旧版本被植入挖矿程序，表现为服务器 CPU 占用达到 100%，可疑进程名为 “mylovelyminer”；另一名 Mac mini 用户则发现名为 “icloud-services” 的进程占满 CPU。对这类部署而言，应立即将 Plex 升级到当前版本，并排查异常高 CPU 占用及陌生进程，而不能只依赖邮件提醒。

**「社区讨论」** 评论者对将 Plex 服务器直接暴露在公网表示担忧，有人反问谁会这样做；也有用户借讨论抱怨新版 Plex UI 缓慢，称已转用 Jellyfin，这与本次安全事件无直接关系。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/plex-vulnerabilities-exploited-in-wild/">Hackers Exploiting Plex Vulnerabilities in the Wild to Deploy ...</a></li>
<li><a href="https://www.securityweek.com/plex2shell-exploit-chain-weaponized-against-plex-servers-hours-after-disclosure/">Plex2Shell Exploit Chain Weaponized Against Plex Servers ...</a></li>
<li><a href="https://securityonline.info/plex2shell-plex-media-server-exploited/">Plex Media Server Vulnerabilities Exploited in the Wild</a></li>

</ul>
</details>

**标签**: `#Plex`, `#security vulnerabilities`, `#cryptomining malware`, `#exploits in the wild`, `#CVE chaining`

---

<a id="item-tech-news-8"></a>
### [SemiAnalysis：2027 年数据中心建设或加速，年增 50GW](https://newsletter.semianalysis.com/p/datacenters-2027-the-year-of-acceleration) ⭐️ 7.0/10

对数据中心运营商和 AI 基础设施投资者而言，SemiAnalysis 在 2026 年 10 月 19 日的行业分析中判断，数据中心容量建设正加速迈向 2027 年：目前有 60GW 项目在建，单年新增装机可能达到 50GW。该分析还称，今年迄今已签署的租赁合同金额达 1.3 万亿美元。文章同时警告，瓶颈可能从电力等环节转移到芯片供应。上述数字来自该分析摘要，属于前瞻性判断，并非已完成的建设或独立核实的结果。

rss · Semianalysis · 10月19日 05:39

**「背景：为何用吉瓦衡量数据中心」** 在 AI 基础设施领域，数据中心规模通常以功率（兆瓦、吉瓦）而非机架数量或建筑面积来衡量，因为训练与推理集群的扩张直接受制于可获得的电力与并网进度。所谓“在建 60GW”与“单年新增 50GW”，描述的是已开工项目的供电容量与年度并网节奏，而非已经投运的算力。在这一口径下，电力接入、变压器与发电能力长期被视为扩产的主要瓶颈，这也正是把“瓶颈是否会转移到芯片”作为讨论重点的前提。

**「采购风险从电力转向芯片」** 对正在签约或交付算力的买方来说，制约条件可能从电力和厂房转向芯片供应——SemiAnalysis 判断瓶颈会移到芯片一侧；另有行业估算认为，约 40% 的现有 AI 数据中心到 2027 年可能面临电力约束，也就是说已建成的容量未必能满负荷运行。这意味着采购方需要把加速器与内存的交付排期和并网时间当作两项独立风险，分别写入合同条款。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aptlytech.com/services/ai-datacenter-buildout/">AI Datacenter Buildout &amp; Support - Aptly Technology</a></li>

</ul>
</details>

**标签**: `#data centers`, `#AI infrastructure`, `#power constraints`, `#semiconductors`, `#industry analysis`

---

<a id="item-tech-news-9"></a>
### [XNU 内核移植至红米 Note 10 Pro，启动 iOS 16 用户空间](https://www.reddit.com/r/hackintosh/comments/1x95qq0/ios_16716_booting_on_a_snapdragon_732g_redmi_note/?sort=new) ⭐️ 7.0/10

开发者将苹果开源的 XNU 内核移植到搭载骁龙 732G 的红米 Note 10 Pro 上，并运行未经修改的 iPhone X 版 iOS 16.7.16 用户空间。该项目在 10 月 18 日已能启动至 iOS 主屏，支持触摸和实体按键操作。目前画面完全由 CPU 渲染，约为 20–30 帧/秒，尚无 GPU 驱动，Wi-Fi、相机等功能暂不可用；代码已在 GitHub 开源。

telegram · zaihuapd · 10月19日 06:30

**「背景」** XNU 是苹果开源的内核，Darwin、macOS 与 iOS 都以它为核心，但 iOS 用户空间通常只运行在苹果自家设备上，并依赖签名校验的启动链。此次移植使用的是 iPhone X 版本的 iOS 16.7.16 用户空间，未经修改便跑在高通骁龙 732G 平台上——换言之，同一份苹果系统上层代码被换到了非苹果内核宿主环境里启动。在没有 GPU 驱动的情况下，界面完全靠 CPU 软件渲染，这也解释了为何帧率只有约 20–30 帧/秒。

**「实际影响」** 这仍是一个硬件支持有限的原理验证项目，而非可用于日常使用的系统移植。希望复现的开发者目前只能验证启动和基础输入，若要扩展用途，还需补齐 GPU、Wi-Fi 和相机等驱动。

**标签**: `#XNU kernel`, `#iOS porting`, `#Snapdragon 732G`, `#mobile OS hacking`, `#open source`

---

<a id="item-tech-news-10"></a>
### [美国国土安全部下令联邦文职部门排除并移除 DeepSeek 产品](https://www.federalregister.gov/public-inspection/2026-21447/order-exclusion-and-removal-of-deepseek-products-from-federal-civilian-executive-branch-information) ⭐️ 7.0/10

美国国土安全部发布命令通知，依据《联邦采购供应链安全法》，将杭州深度求索人工智能基础技术研究有限公司（DeepSeek）及其关联实体开发的信息技术产品与服务排除出联邦文职行政部门采购范围。命令还要求从文职机构信息系统中移除所有 DeepSeek 及关联实体产品，以及使用 DeepSeek 实现的第三方产品与服务。此前，国防部与情报界已对 DeepSeek 实施类似使用限制。

telegram · zaihuapd · 10月19日 13:32

**「背景」** 这项命令援引《联邦采购供应链安全法》，该法涉及联邦采购中信息技术供应链的安全风险管理。来源还提到，美国国防部与情报界此前已对 DeepSeek 实施类似使用限制；此次命令把限制范围延伸至联邦文职行政部门。

**「影响」** 直接影响是：联邦文职机构及向它们供货的承包商不能继续采购 DeepSeek 相关产品，并需在现有系统中识别和移除 DeepSeek 及基于其实现的第三方产品；因此，第三方产品中嵌入 DeepSeek 的情况也属于供应链清理范围。

**标签**: `#DeepSeek`, `#AI policy`, `#supply chain security`, `#US government`, `#procurement`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [技术领域的艺术论证需连回实际效用](https://seangoedecke.com/laypeople-support-technical-fields-for-technology-not-art/) ⭐️ 6.0/10

rss · Sean Goedecke · 10月20日 00:00

**「背景」** 有人主张编程和数学本质上是艺术，因此不应让 LLM 介入；作者认为，无论这一说法是否成立，它都难以说服公众。

**「方案」** 作者同意这些领域可以很美，但指出该论证只对把自身视为艺术家的工程师有吸引力。普通公众支持技术领域，是因为他们享受现代技术成果，并相信数学、编程能维持和推进这些技术；艺术只有在最终促成科学洞见时才会被接受。若告诉公众“LLM 能加速解题，但真正目的是创作艺术，所以反对使用”，他们会觉得受骗，如同雇人装修却被坚持用手工工具体验创作乐趣；对技术雇主更无说服力。作者因此主张，捍卫者需把艺术价值与实用技术价值连接起来，例如优雅抽象需要人的创造力、数学进步依赖新抽象、突破依赖灵感、伟大软件需要人的启发。但作者对这些论据保留态度：他今年尚未见到 LLM 代码库真正撞墙，也不认为 LLM 必然无法创造抽象或获得灵感；伟大产品未必需要伟大代码，并借流水别墅的保温层作比。

**「启示」** 作者的结论是，与其只说人工技术工作因艺术而有价值，不如正面论证艺术如何让技术工作更有效；否则就等于放弃了公众支持这些领域的根本理由。

**标签**: `#LLMs`, `#software engineering`, `#mathematics`, `#public perception of science`, `#art vs technology`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [摩根大通首年向国防与制造初创企业投资 50 亿美元](https://www.cnbc.com/2026/10/19/jpmorgan-security-defense-investments.html) ⭐️ 7.0/10

摩根大通表示，其美国安全与韧性计划启动第一年已向国防、制造和供应链初创企业投资 50 亿美元，达到原定十年 100 亿美元目标的一半，进度快于预期。公司联席总裁佩特诺称可能扩大该计划规模，已披露的持股包括自动工厂企业 Hadrian 和高超音速导弹制造商 Castelion。

rss · CNBC Finance · 10月19日 12:34

**「背景」** 摩根大通一年前启动“安全与韧性倡议”，这是一项为期 10 年、总规模 1.5 万亿美元的融资与投资计划，其中最初 100 亿美元专门用于投资初创企业。

**「影响」** 对国防科技和先进制造初创企业来说，美国最大银行直接入股并参与大额融资，可能为它们扩大本土生产关键部件提供资本支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.jpmorgan.com/about-us/security-and-resiliency">Security and Resiliency Initiative: Boosting Critical Industries</a></li>

</ul>
</details>

**标签**: `#defense technology`, `#banking`, `#venture capital`, `#supply chain`, `#national security`

---

<a id="item-finance-news-2"></a>
### [三星、SK 海力士股价下跌，韩国养老金所持股份估值缩水 1370 亿美元](https://www.bloomberg.com/news/articles/2026-10-19/samsung-sk-hynix-slide-causes-137-billion-hit-to-korea-pension?srnd=phx-technology) ⭐️ 7.0/10

据彭博报道，韩国国民年金公团在 287 家上市公司中 5%以上持股的估值从 6 月底的 515.93 万亿韩元降至 10 月 15 日的 333.53 万亿韩元，减少约 182 万亿韩元（约 1370 亿美元），原因是三星电子和 SK 海力士等股价下跌。这是该基金自 2024 年第四季度以来首次出现季度缩水；此前，该基金在上半年刚录得创纪录回报。

telegram · zaihuapd · 10月19日 08:00

**「背景」** 这些持股按市价计值，股价下跌会直接压低基金资产；据韩国交易所数据，10 月 12 日至 16 日当周，三星电子下跌 17.8%，SK 海力士下跌 24.3%，为 2008 年金融危机以来最差周度表现。

**「影响」** 这笔约 182 万亿韩元的缩水是持仓市值变动，尚未实现为实际亏损，但直接压低了韩国国民年金公团的资产规模，而该基金承担着韩国参保人的退休给付。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.sedaily.com/finance/2026/10/19/samsung-sk-hynix-post-worst-weekly-drop-since-2008-crisis">Samsung, SK hynix Post Worst Weekly Drop Since 2008 Crisis</a></li>

</ul>
</details>

**标签**: `#South Korea pension fund`, `#Samsung Electronics`, `#SK Hynix`, `#semiconductor stocks`, `#market selloff`

---