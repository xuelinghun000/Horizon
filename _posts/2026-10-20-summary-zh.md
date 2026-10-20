---
layout: default
title: "Horizon Summary: 2026-10-20 (ZH)"
date: 2026-10-20
lang: zh
---

> 从 57 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [SemiAnalysis：2027 年数据中心或单年新增 50GW](#item-tech-news-1) ⭐️ 8.0/10
2. [SGLang v0.5.22 发布：扩展模型支持并提升吞吐](#item-tech-news-2) ⭐️ 7.0/10
3. [单电机无人机用铰链与扭矩调制替代斜盘](#item-tech-news-3) ⭐️ 7.0/10
4. [Wine 移植到 OpenBSD，预计上游合并有限](#item-tech-news-4) ⭐️ 7.0/10
5. [Mac.apk 在 Apple Silicon 上原生运行 Android 应用](#item-tech-news-5) ⭐️ 7.0/10
6. [Mistral 发布 Timestral 时间序列基础模型](#item-tech-news-6) ⭐️ 7.0/10
7. [Plex 漏洞在野利用：服务器被植入挖矿程序](#item-tech-news-7) ⭐️ 7.0/10
8. [Let&\#x27;s Encrypt 域名验证新增两个远程视角](#item-tech-news-8) ⭐️ 7.0/10
9. [美国土安全部下令联邦文职部门排除并清除 DeepSeek 产品](#item-tech-news-9) ⭐️ 7.0/10
10. [Inception 发布扩散式语言模型 Mercury 3，声称吞吐超 1k TPS](#item-tech-news-10) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [SemiAnalysis：2027 年数据中心或单年新增 50GW](https://newsletter.semianalysis.com/p/datacenters-2027-the-year-of-acceleration) ⭐️ 8.0/10

SemiAnalysis 在 10 月 19 日发布的报告中预测，数据中心容量扩张将在 2027 年明显加速，单年新增规模可能达到 50GW。报告给出的支撑指标包括：目前约有 60GW 容量处于在建状态，年初至今已签署总额约 1.3 万亿美元的租约合同。报告还提出，随着供电和建设进度推进，供应链瓶颈可能从电力、土地转向芯片。上述数字与判断均来自该分析机构的预测和其“领先指标”，属于前瞻性分析，并非已投产容量或经独立核实的统计。

rss · Semianalysis · 10月19日 05:39

**「背景」** 在数据中心行业，通常用吉瓦（GW）衡量园区的电力接入与承载能力，因此“在建 60GW”指的是已进入施工阶段、对应相应供电规模的项目储备。SemiAnalysis 的这篇文章把 2027 年视为加速节点，依据是年内已签署的约 1.3 万亿美元租约，以及在建规模所预示的集中投产；其判断是供应瓶颈可能从电力、建设转向芯片。上述数字均为该机构的统计或预测，尚不构成已投产容量。

**「瓶颈或转向芯片与供电配额」** 如果这批在建容量在 2027 年前后集中投产，制约因素可能从厂房转向供电与芯片：S&amp;P Global 的分析认为最大障碍不是发电量而是输电与变电站容量，Gartner 则预测到 2027 年 40% 的现有 AI 数据中心会因电力可用性而运营受限；同时 Design News 报道 HBM 需求到 2027 年将占 32%，GPU 与内存供应持续紧张、价格上行。对计划同期上线的运营方而言，这意味着需要提前锁定并网与变电能力，以及 GPU/HBM 的长期采购配额，否则算力落地时间可能被外部供应而非自身建设进度决定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gartner.com/en/newsroom/press-releases/2024-11-12-gartner-predicts-power-shortages-will-restrict-40-percent-of-ai-data-centers-by-20270">Gartner Predicts Power Shortages Will Restrict 40% of AI Data ...</a></li>
<li><a href="https://www.designnews.com/electronics/can-chip-shortages-derail-the-ai-data-center-boom-">AI Data Center Boom Hits Critical Chip and Memory Shortages</a></li>
<li><a href="https://www.spglobal.com/market-intelligence/en/news-insights/research/2026/06/ai-data-center-power-demand-grid-constraints-energy-resilience">AI Power Demand: Data Center Growth Strains Global Grids</a></li>

</ul>
</details>

**标签**: `#datacenters`, `#AI infrastructure`, `#semiconductors`, `#supply chain`, `#capacity buildout`

---

<a id="item-tech-news-2"></a>
### [SGLang v0.5.22 发布：扩展模型支持并提升吞吐](https://github.com/sgl-project/sglang/releases/tag/v0.5.22) ⭐️ 7.0/10

SGLang 发布 v0.5.22，包含来自 245 位贡献者的 950 个 PR，新增 Clef/Clef Flash、PPLX-Decider v1/v1.1、EmbeddingGemma 2、LLaDA2.2、HunyuanImage-3.0-Instruct、Kandinsky 6 等 LLM、VLM、嵌入和扩散模型支持。发布说明称，DeepSeek-V4.1 在 H200 上每 GPU 吞吐最高提升 2.3 倍并可在 AMD MI350X/MI355X 上运行；Qwen3.8-Flash-Next 在 B200 上解码快 12%，GLM-5.3-Flash 在 B300 上快 10%，新的 InstantTensor 加载器使模型加载快 10 倍。该版本还修复了混合线性模型在同时使用投机解码和结构化输出时可能从错误 mamba 状态恢复的问题。升级要求 Python 3.11 或更高版本，并可通过 \`uv pip install --prerelease=allow sglang==0.5.22\` 安装。

github · ch-wan · 10月19日 02:55

**「背景」** SGLang 是一个开源的大语言模型与多模态模型推理和服务框架，针对智能体负载、强化学习 rollout 以及大规模在线服务进行了优化。本次 v0.5.22 属于该框架 0.5 系列中的一次增量版本更新，其投机解码、PD 分离、HiSparse 等改进均建立在框架已有的这些服务与优化组件之上。

**「升级与部署影响」** 现有环境若固定使用 Python 3.10 或更早版本，需要在升级前调整基础镜像或运行时；AMD MI35x/MI30x、Intel GPU 和 Intel CPU 用户应分别选用 \`v0.5.22-rocm10-mi35x\`、\`v0.5.22-rocm10-mi30x\`、\`v0.5.22-xpu\` 和 \`v0.5.22-xeon\` 镜像，而不是 NVIDIA CUDA 13 镜像。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/sgl-project/sglang">GitHub - sgl- project / sglang : SGLang is a high-performance serving ...</a></li>

</ul>
</details>

**标签**: `#SGLang`, `#LLM serving`, `#inference engine`, `#model integrations`, `#open source`

---

<a id="item-tech-news-3"></a>
### [单电机无人机用铰链与扭矩调制替代斜盘](https://www.youtube.com/watch?v=Ndftcft6XhU) ⭐️ 7.0/10

一位爱好者发布视频，展示了一架只用一个电机驱动的无人机：它通过特殊铰链结构、磁编码器和扭矩调制，在旋翼旋转时改变升力，从而不再需要传统直升机的斜盘。该演示的核心是把复杂的机械变距机构换成转子铰链与反馈控制；从现有材料看，目前只有创作者视频，未见独立测量或产品化信息。评论指出，这种单电机方案在空中会持续自旋，若追求实用性，带尾电机的双电机设计可能更合适。

hackernews · hakonjdjohnsen · 10月19日 09:05 · [社区讨论](https://news.ycombinator.com/item?id=50150089)

**「背景」** 欠驱动机器人指执行器数量少于需要独立控制的自由度的系统；这架单电机无人机要在只有一个动力源的情况下同时调节升力和姿态。常规四旋翼依靠四个电机的转速差产生控制力矩，传统直升机则用斜盘改变桨叶桨距。据 Tom&\#x27;s Hardware 和 STEINS Lab 的报道，作者 Joshua Bird 采用 45 度铰链桨毂与自定义固件，通过扭矩调制改变旋翼升力，从而绕开上述两套主流机构。

**「影响」** 对想复现的自制无人机开发者而言，关键工作从斜盘连杆转到磁编码器反馈与扭矩调制控制；同时必须处理机体在空中持续自旋的问题，实际设计可能需要额外的尾电机或偏航控制手段。

**「社区讨论」** 评论者 mrandish 指出，固定翼 RC 特技爱好者多年前已在用变距螺旋桨，小尺寸的集成变距电机也已存在，因此该应用不必自行改造螺旋桨；他认为这与单电机无人机相似但不同。TGower 则把它与欠驱动机器人联系起来，提到 BattleBots 中有单电机机器人仅靠控制转速，就能借助底盘冲击器和约 3000 RPM 的轮子实现移动与攻击。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/maker-stem/engineer-builds-tiny-3d-printed-single-motor-drone-in-their-bedroom-45-degree-hinged-rotor-and-sub-0-2ms-firmware-control-pitch-and-roll">Engineer builds tiny 3D-printed single-motor drone in their ...</a></li>
<li><a href="https://daily.steinslab.io/en/consumer/2026-10-18-single-propeller-flying-drone-hardware-hack/">Single-Motor Controllable Hover: Variable-Pitch Algorithms ...</a></li>

</ul>
</details>

**标签**: `#underactuated robotics`, `#drone design`, `#control systems`, `#hardware hacking`, `#variable-pitch propulsion`

---

<a id="item-tech-news-4"></a>
### [Wine 移植到 OpenBSD，预计上游合并有限](https://marc.info/?l=openbsd-ports&amp;m=179236125692175) ⭐️ 7.0/10

一封 OpenBSD ports 邮件列表公告称，Wine 已被移植到 OpenBSD；这是兼容层的一次移植，而非 Wine 上游正式宣布支持 OpenBSD 的新版本。相关评论引用邮件说明称，维护者把面向 OpenBSD 的改动标记为仅 OpenBSD，因此预计大部分改动不会合并到 Wine 上游；其中 %gs 桩在 Linux 上不会构建，因为 Linux 已正确设置 %gs，SIGUSR1 虽可用但效果较差。现有材料未说明所支持的 Wine 版本、可运行应用范围或正式发布时间。

hackernews · iamnothere · 10月19日 13:35 · [社区讨论](https://news.ycombinator.com/item?id=50152307)

**「背景」** Wine 是一个在非 Windows 系统上运行 Windows 程序的兼容层，但其上游实现长期依赖 Linux 特有的接口和假设。根据一篇技术分析，Thomas Frohwein 与贡献者此次将 Wine 移植到 OpenBSD 时，必须把这些 Linux 专用假设逐一剥离或改写；Adafruit 的报道还提到，该移植建议以单独的非特权用户运行 Wine，而 unveil\(2\) 围栏是否适用仍未解决。

**「实际影响」** 对 OpenBSD 用户而言，这意味着可以在该系统上通过 Wine 运行 Windows 程序；但由于 OpenBSD 不允许用户态设置 %gs/gsbase，该移植通过模拟 %gs 前缀来绕开这一限制，而非直接使用硬件段机制。因此，依赖 %gs 相对寻址的 Windows 应用在 OpenBSD 上可能需要额外测试，并可能承担模拟带来的开销。

**「社区讨论」** 有评论引用相关邮件称，维护者预计大部分 OpenBSD 改动不会进入 Wine 上游，因为相关代码被明确标记为仅 OpenBSD，这也成为讨论移植范围与上游协作的主要争点。另有评论贴出《极乐迪斯科》《空洞骑士》《掠食》等游戏的实机视频链接，但材料未说明具体配置或可复现性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.adafruit.com/2026/10/19/wine-ported-to-openbsd/">Wine ported to OpenBSD - Adafruit Industries</a></li>
<li><a href="https://www.hotmolts.com/post/porting-wine-to-openbsd-made-wines-linux-only-assu-6bb14581-6b00-48ea-9e07-c81795fa88bf">Porting Wine to OpenBSD made Wine&#x27;s Linux-only assumptions ...</a></li>
<li><a href="https://blog.adafruit.com/2026/10/19/wine-ported-to-openbsd/">Wine ported to OpenBSD - Adafruit Industries</a></li>

</ul>
</details>

**标签**: `#OpenBSD`, `#Wine`, `#software porting`, `#open source`, `#compatibility layers`

---

<a id="item-tech-news-5"></a>
### [Mac.apk 在 Apple Silicon 上原生运行 Android 应用](https://github.com/kksimp/Mac.apk) ⭐️ 7.0/10

一个名为 Mac.apk 的 GitHub 项目演示了在 Apple Silicon Mac 上原生运行 Android 应用，不依赖模拟器、虚拟机或 Linux 层。据评论者转述，项目把应用数据存放在 .app 包内，而不是 macOS 的 Application Support 目录，项目以“文件不会散落到主目录”为由解释这一选择。评论还指出，对 Google Play Services 等谷歌封闭生态组件的依赖会限制其实际可用性。

hackernews · flocked · 10月19日 16:45 · [社区讨论](https://news.ycombinator.com/item?id=50154624)

**「背景」** Android 应用通常依赖 Android 运行时、系统服务和专用 API，而不是直接调用 macOS 的内核与系统接口；因此在 Apple Silicon Mac 上运行它们，核心难点不只是 CPU 指令兼容，还包括把整套应用依赖重新承载到 macOS 用户态。传统方案往往借助模拟器或完整 Android 系统来提供这些依赖，而该项目声称跳过模拟器、虚拟机和 Linux 层，直接实现原生兼容。

**「使用限制」** 对最终用户而言，最直接的门槛是 Google Play 服务：依赖这些 API 的应用需要在构建时声明相应 SDK 并在兼容的 Android 设备或模拟器上运行，而该项目并未提供这套运行时，因此只能运行不依赖 GMS 的安卓应用，评论者 bilalq 也认为这会让实际可用性低于预期。另一个实际后果是安装方式——项目把应用数据存放在 .app 包内部而非 Application Support，评论者 irskep 指出这并非「不散落文件」的唯一选择，其代价是应用更新或替换包体时数据会随之被覆盖，也不会进入常规的用户目录备份路径。

**「社区讨论」** 有评论者认为，把应用数据放进 .app 包而非 Application Support 是怪异的设计选择，并反驳了项目“不会散落到主目录”的理由；也有人指出，Google Play Services 依赖会削弱其实用性。另有用户提到，这可用于在 Mac 上运行 Android 版 Minecraft，从而与主机或移动端的 Bedrock 玩家联机。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.google.com/android/guides/setup">Set up Google Play services | Google for Developers</a></li>

</ul>
</details>

**标签**: `#Android compatibility`, `#macOS`, `#Apple Silicon`, `#systems programming`, `#compatibility layer`

---

<a id="item-tech-news-6"></a>
### [Mistral 发布 Timestral 时间序列基础模型](https://mistral.ai/news/timestral/) ⭐️ 7.0/10

Mistral 发布了时间序列基础模型 Timestral，发布页称其可对生产计划、计划停机、天气预报等未来已知协变量进行条件建模，面向时间序列预测任务。当前可获得的材料主要是发布页与 Hacker News 讨论，未见模型规模、许可、价格或可核验的基准结果。对需要批量预测大量序列的团队而言，这提供了一个通用模型选项，但它相对按序列定制模型的准确性和泛化能力仍待独立验证。

hackernews · groar · 10月19日 09:59 · [社区讨论](https://news.ycombinator.com/item?id=50150434)

**「背景」** 时间序列基础模型试图先用大量序列预训练一个通用模型，使其能对未见过的序列做零样本预测，或只需少量微调，而不必为每条序列单独建模。Mistral 将 Timestral 称为其首个时间序列基础模型系列，提供 5M、28M、123M 和 209M 四种参数规模，并称其结合了合成预训练、协变量感知注意力与长上下文学习。

**「影响」** 拥有成千上万条短历史序列、难以逐条训练模型的企业，应重点验证 Timestral 在序列尺度不一致和协变量不完整时的表现；采用前需用自身数据做回测，并与单序列 XGBoost 等基线比较。

**「社区讨论」** 评论中的支持者认为，基础模型最适合成千上万条历史很短的序列：逐条训练不现实，而单模型又必须处理序列间的尺度差异；质疑者则指出“时间序列”异质性太大，并以缺少基准和对 Mistral 其他模型的使用体验为由保持怀疑。还有评论建议用高信噪比的数据生成过程来检验预测能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mistral.ai/news/timestral/">Timestral: Mistral&#x27;s time-series foundation models | Mistral</a></li>
<li><a href="https://explainx.ai/blog/timestral-mistral-time-series-foundation-models-209m-cpu-forecasting-2026">Timestral: Mistral Releases Time-Series Foundation Models ...</a></li>
<li><a href="https://cho.sh/mini/news/ai-2/timestral-time-series-models">Mistral releases Timestral, time-series foundation models ...</a></li>

</ul>
</details>

**标签**: `#time-series`, `#foundation models`, `#Mistral`, `#forecasting`, `#machine learning`

---

<a id="item-tech-news-7"></a>
### [Plex 漏洞在野利用：服务器被植入挖矿程序](http://www.boredhackerblog.info/2026/10/plex-vulnerabilities-being-exploited-in.html) ⭐️ 7.0/10

据安全博客报道，Plex 漏洞正被在野利用，攻击者借此在用户的自托管服务器上植入加密货币挖矿程序。报道称已出现感染案例，但没有给出受影响的具体 Plex 版本范围或漏洞编号，Plex 方面的修复与公告细节也未在材料中说明。对运行旧版的 Plex 运营者而言，需要立即核查主机进程和软件版本。

hackernews · mindracer · 10月19日 13:36 · [社区讨论](https://news.ycombinator.com/item?id=50152321)

**「背景」** 这轮攻击依托名为 Plex2Shell 的漏洞利用链：研究者 Zach Main 公开了将四个 Plex Media Server 漏洞串联成未授权远程代码执行的细节与 PoC。安全媒体报道称，PoC 发布次日（2026 年 10 月 17 日）就出现了实际利用，攻击者在蜜罐中投放了挖矿程序和代理工具。

**「实际影响」** 仍运行旧版 Plex 的自托管用户可能看到服务器 CPU 被挖矿进程占满，且不易第一时间识别为恶意软件；有评论者称自己错过 9 月 1 日的升级邮件、继续运行 13 个月前的版本后中招，并发现了名为“mylovelyminer”的进程。另一名 Gentoo 维护者称，修补版本自 7 月 15 日起已进入其主软件树，可作为发行版侧的缓解线索。

**「社区讨论」** 一名 Mac mini 用户报告发现名为“icloud-services”的进程占满 CPU，起初还以为是 Apple 的软件缺陷，重启后才发现异常文件。另有评论者称 Reddit 上出现大量类似报告，除挖矿程序外还有 DDoS 节点载荷，并把公开的 Plex2Shell 概念验证利用视为推动因素。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dailysecurityreview.com/resources/plex2shell-exploit-chain-hits-plex-servers-a-day-after-poc-release/">Plex2Shell Exploit Chain Hits Plex Servers a Day After PoC ...</a></li>
<li><a href="https://securityonline.info/plex2shell-plex-media-server-exploited/">Plex Media Server Vulnerabilities Exploited in the Wild</a></li>
<li><a href="https://cybersecuritynews.com/plex-vulnerabilities-exploited-in-wild/">Hackers Exploiting Plex Vulnerabilities in the Wild to Deploy ...</a></li>

</ul>
</details>

**标签**: `#Plex`, `#security vulnerabilities`, `#cryptominer`, `#in-the-wild exploitation`, `#self-hosted software`

---

<a id="item-tech-news-8"></a>
### [Let&\#x27;s Encrypt 域名验证新增两个远程视角](https://community.letsencrypt.org/t/lets-encrypt-is-adding-two-additional-remote-perspectives-for-domain-validation/252166) ⭐️ 7.0/10

Let&\#x27;s Encrypt 宣布将在 ACME 域名验证中增加两个额外的远程验证视角，使挑战和响应检查从更多物理位置、经由不同网络路径发起，以降低网络层攻击导致错误签发的风险。该改动面向使用 ACME 申请证书的用户，目前属于公布的计划，帖文未给出具体上线时间或部署细节。其核心是强化多视角验证，而非改变 ACME 的申请流程。

hackernews · gslin · 10月19日 10:53 · [社区讨论](https://news.ycombinator.com/item?id=50150809)

**「背景：多视角验证与 BGP 劫持」** ACME 域名验证通常由 CA 从外部发起挑战请求；多视角验证则是从多个物理位置、经不同网络路径执行同一检查，以降低单一路由被劫持就能骗过验证的风险。此前 8 月底，攻击者劫持了 Hetzner 承载 Softaculous/Virtualizor 的 162.55.80.0/24（AS62390），并利用一张技术上有效的 TLS 证书投递恶意更新；社区讨论指出，即便有多视角验证，这次攻击仍成功获得了证书。

**「对证书签发与运维的影响」** 对使用 ACME 自动签发证书的站点而言，实际变化是域名校验会从更多网络路径发起；如果挑战响应依赖单一路由、地理/IP 白名单或特定的 anycast 配置，运维者需要确认新增视角也能正常获取响应。评论中引用的 8 月 BGP 劫持事件也表明，多视角校验并不能完全阻止路由劫持导致的错误签发，证书持有者仍应保留监控和撤销等额外防护。

**「社区讨论」** 有评论者提醒，多视角验证并非万无一失：其引述的 8 月一起 BGP 劫持事件中，攻击者仍成功获得有效 TLS 证书并推送恶意更新，说明路由层攻击可能绕过现有防护。另有评论者解释，“远程视角”指从多个物理位置执行 ACME 挑战验证，从而让网络级攻击更难奏效。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ipregistry.co/blog/virtualizor-hetzner-bgp-hijack-rpki-valid">A 33-Hour BGP Hijack Passed RPKI , Fooled Let&#x27;s Encrypt, and...</a></li>
<li><a href="https://www.securityweek.com/malicious-virtualizor-update-served-via-bgp-hijacking/">Malicious Virtualizor Update Served via BGP Hijacking - SecurityWeek</a></li>
<li><a href="https://bgpkit.com/blog/virtualizor-bgp-hijack-anatomy/">Anatomy of the Virtualizor BGP Hijack : Reading the Attack... - BGPKIT</a></li>

</ul>
</details>

**标签**: `#TLS certificates`, `#Let&\#x27;s Encrypt`, `#ACME`, `#BGP hijacking`, `#internet security`

---

<a id="item-tech-news-9"></a>
### [美国土安全部下令联邦文职部门排除并清除 DeepSeek 产品](https://www.federalregister.gov/public-inspection/2026-21447/order-exclusion-and-removal-of-deepseek-products-from-federal-civilian-executive-branch-information) ⭐️ 7.0/10

美国国土安全部发布命令通知，依据《联邦采购供应链安全法》，将杭州深度求索人工智能基础技术研究有限公司（DeepSeek）及其关联实体的信息技术产品与服务排除出联邦文职行政部门采购，并要求文职机构从信息系统中移除所有 DeepSeek 及关联实体产品。命令还覆盖基于 DeepSeek 实现的第三方产品与服务。来源提到，美国国防部与情报界此前已对 DeepSeek 设有类似使用限制。

telegram · zaihuapd · 10月19日 13:32

**「背景：联邦采购供应链安全法的授权」** 《联邦采购供应链安全法》允许美国联邦机构以供应链安全风险为由，把特定产品或供应商排除出采购范围，并从既有信息系统中移除。此前国防部与情报界已对 DeepSeek 设有类似使用限制；此次国土安全部的命令把这一限制扩展到联邦文职行政部门的采购与在役系统，并明确覆盖基于 DeepSeek 实现的第三方产品与服务。

**标签**: `#DeepSeek`, `#AI regulation`, `#US government`, `#supply chain security`, `#procurement policy`

---

<a id="item-tech-news-10"></a>
### [Inception 发布扩散式语言模型 Mercury 3，声称吞吐超 1k TPS](https://www.inceptionlabs.ai/blog/introducing-mercury-3) ⭐️ 7.0/10

Inception 发布扩散式大语言模型 Mercury 3，并已通过 Inception API 和 OpenRouter 等平台提供。发布信息称其生成速度超过每秒 1000 tokens，上下文窗口达 100 万 tokens，参数量约为 Mercury 1 的 40 倍，输入定价为每百万 tokens 0.2 美元。该模型还宣称在多项基准上超过 GPT-6 Luna 与 Claude Haiku 5.5，但这些对比目前来自厂商及聚合信息，尚未经过独立验证。

telegram · zaihuapd · 10月20日 00:29

**「背景」** Mercury 系列采用的是扩散式（diffusion）文本生成：它不像主流大模型那样逐 token 自回归解码，而是通过多轮并行去噪与细化一次性产出整段文本，因此吞吐量天然占优；Inception 官网称其相对速度优化的前沿模型有 5–7 倍吞吐、首 token 延迟低于 300 毫秒。Mercury 3 是该系列的第三代产品，官方称其规模约为初代 Mercury 1 的 40 倍，并称其为迄今能力最强的扩散式 LLM（以上均为厂商说法）。

**「对开发者的实际影响」** 对需要低延迟、高并发或长文档处理的开发者，Mercury 3 以 100 万 tokens 上下文和每百万输入 tokens 0.2 美元的定价提供了新的低成本 API 选项；但 1,000+ tokens/s 的吞吐与基准领先均为 Inception 的厂商声明，且速度测试基于 NVIDIA GPU，迁移前应在自身任务上做 A/B 验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.inceptionlabs.ai/blog/introducing-mercury-3">Diffusion at Scale: Introducing Mercury 3 – Inception</a></li>
<li><a href="https://www.inceptionlabs.ai/">Inception – When Every Millisecond Matters</a></li>
<li><a href="https://finance.yahoo.com/technology/ai/articles/inception-launches-mercury-3-setting-164800350.html?fr=sycsrp_catchall">Inception Launches Mercury 3, Setting a New Pareto Frontier ...</a></li>
<li><a href="https://www.inceptionlabs.ai/blog/introducing-mercury-3">Diffusion at Scale: Introducing Mercury 3 – Inception</a></li>
<li><a href="https://interestingengineering.com/ai-robotics/mercury-3-diffusion-model-8-times-faster">Mercury 3 claims to outperform GPT-6 Luna, Claude Haiku 5.5 ...</a></li>

</ul>
</details>

**标签**: `#diffusion LLMs`, `#large language models`, `#model release`, `#inference speed`, `#API pricing`

---