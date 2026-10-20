---
layout: default
title: "Horizon Summary: 2026-10-20 (ZH)"
date: 2026-10-20
lang: zh
---

> 从 56 条内容中筛选出 6 条重要资讯。

---

**科技新闻**
1. [Plex vulnerabilities being exploited in the wild to drop a cryptominer](#item-tech-news-1) ⭐️ 8.0/10
2. [SemiAnalysis 预测：2027 年数据中心新增用电容量约 50 吉瓦](#item-tech-news-2) ⭐️ 8.0/10
3. [Wine ported to OpenBSD](#item-tech-news-3) ⭐️ 7.0/10
4. [开源项目 Mac.apk：无需模拟器在苹果芯片 Mac 上直接运行安卓应用](#item-tech-news-4) ⭐️ 7.0/10
5. [程序员热议：上线自己没读懂的 AI 代码怎么办](#item-tech-news-5) ⭐️ 7.0/10
6. [美国国土安全部下令：联邦文职机构禁购并清除 DeepSeek 产品](#item-tech-news-6) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Plex vulnerabilities being exploited in the wild to drop a cryptominer](http://www.boredhackerblog.info/2026/10/plex-vulnerabilities-being-exploited-in.html) ⭐️ 8.0/10

Attackers are exploiting known, unpatched Plex server vulnerabilities in the wild to install cryptominers \(and other payloads\), prompting Plex users to urgently update their media servers.

hackernews · mindracer · 10月19日 13:36 · [社区讨论](https://news.ycombinator.com/item?id=50152321)

**标签**: `#security`, `#plex`, `#vulnerability-exploitation`, `#cryptomining`, `#self-hosting`

---

<a id="item-tech-news-2"></a>
### [SemiAnalysis 预测：2027 年数据中心新增用电容量约 50 吉瓦](https://newsletter.semianalysis.com/p/datacenters-2027-the-year-of-acceleration) ⭐️ 8.0/10

行业研究机构 SemiAnalysis 在 2026 年 10 月 19 日发布的分析中预测，数据中心（集中放置服务器、为网站和 AI 服务提供运算能力的设施）的新增容量将在 2027 年加速到约 50 吉瓦（功率单位，衡量设施需要多少电力，1 吉瓦大致相当于一座大型核电机组的输出）。作为判断依据的先行指标（用来提前反映趋势的信号）包括：今年以来各方已签署约 1.3 万亿美元的机房长期租用合同，另有 60 吉瓦容量的数据中心正在建设中。分析认为，目前的短缺集中在电力和机房，接下来可能转移到芯片（尤其是运行 AI 所需的专用处理器）上。需要说明，这是一份预测而非已落成的产能，实际进度仍取决于电力、设备和供应链等条件。

rss · Semianalysis · 10月19日 05:39

**「背景」** 数据中心行业习惯用“吉瓦”（GW，功率单位，1 吉瓦等于 10 亿瓦，大致相当于一座大型核电机组的发电能力）来衡量规模，因为人工智能计算最直接的约束是电力供应。SemiAnalysis 是一家专注芯片与人工智能基础设施研究的机构，这份报告属于对未来的预测，而不是已建成的统计数字。其推算依据之一是所谓“先行指标”：企业会提前数年签下数据中心的长期租约，因此年内签约量被用来推测之后的实际建设节奏。

**「实际影响」** 对使用 AI 服务的普通人来说，数据中心是聊天机器人、云服务这类功能背后的“厂房”：如果预测成真，机房和电力会大幅扩容，但瓶颈可能卡在芯片上——房子盖好了，“发动机”却可能不够，AI 服务的扩容速度仍会受限。对需要租用机房或采购芯片的企业而言，这份报告提示相关资源正被大额长约提前锁定，采购规划可能需要更早启动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/datacenters-2027-the-year-of-acceleration">Datacenters 2027: The Year of Acceleration, +50GW in a Single ...</a></li>
<li><a href="https://aicoder.com/news/news-1792424548152-h6xez">SemiAnalysis Releases Landmark Datacenters 2027 Report: +50GW ...</a></li>

</ul>
</details>

**标签**: `#datacenters`, `#AI infrastructure`, `#semiconductors`, `#capacity planning`, `#industry analysis`

---

<a id="item-tech-news-3"></a>
### [Wine ported to OpenBSD](https://marc.info/?l=openbsd-ports&amp;m=179236125692175) ⭐️ 7.0/10

Wine, the Windows application compatibility layer, has been ported to OpenBSD, with the developer sharing technical details and community members demonstrating Windows games running on the OS.

hackernews · iamnothere · 10月19日 13:35 · [社区讨论](https://news.ycombinator.com/item?id=50152307)

**标签**: `#OpenBSD`, `#Wine`, `#operating-systems`, `#open-source`, `#compatibility-layer`

---

<a id="item-tech-news-4"></a>
### [开源项目 Mac.apk：无需模拟器在苹果芯片 Mac 上直接运行安卓应用](https://github.com/kksimp/Mac.apk) ⭐️ 7.0/10

一个名为 Mac.apk 的开源项目（代码公开，任何人可查看和改进）能让安卓应用直接运行在搭载苹果自研芯片的 Mac 电脑上。它不需要模拟器（用软件模拟出一台安卓手机）或虚拟机（在 Mac 里再运行一个完整的虚拟系统），底层也不必借助 Linux 系统（一种常见的开源操作系统）。该项目 2026 年 10 月 19 日登上科技新闻社区 Hacker News，获得 275 个赞和 144 条评论，目前由社区开发者维护、仍处于早期阶段，并非苹果或谷歌的官方功能。评论者指出，依赖谷歌移动服务（不少安卓应用靠它登录账号、接收通知）的应用可能无法正常使用，这会限制项目的实用性。

hackernews · flocked · 10月19日 16:45 · [社区讨论](https://news.ycombinator.com/item?id=50154624)

**「背景」** 过去想在电脑上运行手机应用，通常要借助“模拟器”或“虚拟机”——这类软件先让电脑假扮成一部安卓手机，再在里面启动应用，代价是速度慢、画面和操作常常不跟手。转机来自芯片：2020 年后的 Mac 改用苹果自研的 Apple Silicon 芯片，它与安卓手机芯片同属一个设计家族（ARM），使用同一套底层指令，因此安卓应用的代码无需翻译就能被芯片直接执行。Mac.apk 正是利用这一点，在 macOS 上直接重建安卓应用的运行环境，让应用作为普通的 Mac 程序启动、由 Mac 的图形芯片负责画面。

**「实际影响」** 对想在 Mac 上使用手机应用的人来说，最直接的收益是能运行那些没有 Mac 版的安卓应用。有用户举例：在 Mac 上运行安卓版《我的世界》基岩版（手机和游戏机通用的版本），就能和手机、游戏机上的朋友联机。动手前需留意兼容性：依赖谷歌移动服务的应用可能无法正常运行，建议先确认自己要用的应用是否有此依赖。

**「社区讨论」** 评论中的主要批评有两点：一是项目把应用数据存在应用文件内部，而不是 Mac 系统惯用的数据文件夹，被认为不合常规；二是项目说明文档的行文被指带有明显的 AI 生成痕迹，让部分人对项目质量有所保留。也有评论者肯定其价值，认为尽管有这些短板，项目依然很酷、有实际用处。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/kksimp/Mac.apk">GitHub - kksimp/Mac.apk: Mac.apk: Run Android apps natively ...</a></li>
<li><a href="https://daily.dev/posts/android-apps-running-native-on-macos-gcspqvspy">Android apps running native on macOS - daily.dev</a></li>

</ul>
</details>

**标签**: `#android`, `#macos`, `#apple-silicon`, `#open-source`, `#runtime`

---

<a id="item-tech-news-5"></a>
### [程序员热议：上线自己没读懂的 AI 代码怎么办](https://news.ycombinator.com/item?id=50151036) ⭐️ 7.0/10

一位 Meta 工程师在社交平台发文说，如今大量用 AI（大语言模型，能根据描述自动生成代码的工具）写代码，快到来不及逐行检查，结果自己搭建的系统只有大概轮廓清楚，细节却说不明白，这让他感到不安。这条帖子在程序员社区 Hacker News 引发热议，获得 294 个点赞和 439 条评论。讨论的核心是：当 AI 替人写代码成为常态，工程师到底需要理解多少代码、又由谁为后果负责。这目前是一场行业内部的观点争论，而不是某家公司的新政策或新产品发布。

hackernews · rzk · 10月19日 11:24

**「背景」** 大型语言模型（根据文字指令生成内容的软件）如今能按工程师的描述直接写出程序代码，越来越多的公司把“让 AI 写代码、人来审核”当作日常工作方式。发帖所引用的作者、Meta 工程师 Ali Hamie 在另一则帖子中称，过去三个月他没有手动写过一行代码，但提交的代码量可能超过此前一整年的总和。这种“只把握大概、不逐行理解”的写法，正是这轮讨论的起点。

**「实际影响」** 对使用 AI 编程工具的普通用户来说，这意味着他们接触到的软件和网站，作者本人可能也无法解释其中的每个细节，出问题时排查可能更慢。文中提到的普遍做法是把更多精力转向测试（反复运行程序、确认结果正确），但社区提醒测试只能发现问题，不能代替对代码的理解。

**「社区讨论」** 社区里形成两种立场：一种主张“先设计、后实现”，即工程师自己定好整体结构和思路，只让 AI 填充具体细节，这样至少知道代码大概怎么运作；另一位资深工程师类比说，这就像过去由资深工程师设计、初级员工实现，现在人人都能当“设计者”。反对者则认为这些做法是在逃避责任，主张上线前必须有人能读懂并解释每一行代码，因为测试无法保证覆盖所有情况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ca.linkedin.com/in/ali-hamie">Ali Hamie - Software Engineer @ Meta | LinkedIn From Coding to Directing: Leveraging AI in ... - LinkedIn Ali Hamie’s Post - LinkedIn Meta Engineers Now Direct AI Code Generation | Ali Hamie ... From Code to AI Management: Evolving Software Engineer Role Ask HN: How to deal with shipping AI-written code you don&#x27;t ...</a></li>
<li><a href="https://www.linkedin.com/posts/ali-hamie_in-the-past-3-months-at-meta-i-havent-written-activity-7443757855276716032-hrCH">From Coding to Directing: Leveraging AI in ... - LinkedIn</a></li>

</ul>
</details>

**标签**: `#ai-generated-code`, `#software-engineering`, `#code-review`, `#developer-practices`, `#llm`

---

<a id="item-tech-news-6"></a>
### [美国国土安全部下令：联邦文职机构禁购并清除 DeepSeek 产品](https://www.federalregister.gov/public-inspection/2026-21447/order-exclusion-and-removal-of-deepseek-products-from-federal-civilian-executive-branch-information) ⭐️ 7.0/10

美国国土安全部发布命令，将中国人工智能公司深度求索（DeepSeek）及其关联实体的信息技术产品与服务，排除出美国联邦文职行政部门（即除军方和情报机构之外的联邦行政机构）的采购范围。命令依据《联邦采购供应链安全法》（一部用于把被认为有安全风险的产品挡在政府采购之外的美国法律）发布，通知已刊登在《联邦公报》（美国政府发布法规的官方刊物）上。命令还要求各文职机构从现有信息系统中移除所有 DeepSeek 及相关实体的产品，范围延伸到借助 DeepSeek 实现的第三方产品与服务——也就是说，其他公司的产品里只要用到了 DeepSeek，同样受影响。据命令通知，美国国防部与情报机构此前已对 DeepSeek 有类似的使用限制，此次是将禁令扩展到整个文职政府部门。

telegram · zaihuapd · 10月19日 13:32

**「背景」** 深度求索（DeepSeek）是一家总部位于杭州的中国人工智能公司。这并非美国政府首次针对它：此前国防部（负责军队事务的部门）与情报界（美国各情报机构的统称）已对 DeepSeek 采取过类似的使用限制，此次命令则把这类限制延伸到了所有文职政府机构。命令所依据的《联邦采购供应链安全法》，是一部授权美国政府将认为存在安全风险的信息技术产品排除出采购范围、并要求从现有系统中移除的法律。

**「实际影响」** 命令的直接后果落在向美国政府卖软件的公司和联邦文职机构（政府中除军方、情报部门外的行政机构）身上：这些机构需要排查并清除系统里的 DeepSeek 相关产品，而软件公司若在产品中集成了 DeepSeek 的模型（即用这家中国公司训练好的 AI 来提供问答等功能），即使产品挂的是自己的牌子，也会被当作“使用 DeepSeek 实现的第三方产品”一并禁止，需先替换掉相关部分才能继续参与联邦采购。命令只约束政府系统与采购，普通人在自己设备上使用 DeepSeek 应用不受此令直接限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.federalregister.gov/public-inspection/2026-21447/order-exclusion-and-removal-of-deepseek-products-from-federal-civilian-executive-branch-information">Federal Register :: Public Inspection: Order: Exclusion and ...</a></li>
<li><a href="https://articlesaboutai.com/us-deepseek-removal-order-federal-agencies/">US Orders Removal of DeepSeek AI Products From Federal ...</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#DeepSeek`, `#government procurement`, `#supply chain security`, `#US-China tech`

---