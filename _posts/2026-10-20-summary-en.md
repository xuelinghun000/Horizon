---
layout: default
title: "Horizon Summary: 2026-10-20 (EN)"
date: 2026-10-20
lang: en
---

> From 44 items, 13 important content pieces were selected

---

**Technology News**
1. [SGLang v0.5.22 adds new models, speedups; needs Python 3.11](#item-tech-news-1) ⭐️ 7.0/10
2. [Hobbyist drone flies on a single motor with a variable-pitch hinge](#item-tech-news-2) ⭐️ 7.0/10
3. [Wine ported to OpenBSD with OpenBSD-only changes](#item-tech-news-3) ⭐️ 7.0/10
4. [Mac.apk runs Android apps natively on Apple Silicon Macs](#item-tech-news-4) ⭐️ 7.0/10
5. [Mistral announces Timestral, a family of time-series foundation models](#item-tech-news-5) ⭐️ 7.0/10
6. [Ask HN debates shipping AI-written code engineers don&\#x27;t fully understand](#item-tech-news-6) ⭐️ 7.0/10
7. [Plex vulnerabilities reportedly exploited in the wild to install cryptominers](#item-tech-news-7) ⭐️ 7.0/10
8. [SemiAnalysis Expects Datacenter Build to Reach 50GW in 2027](#item-tech-news-8) ⭐️ 7.0/10
9. [XNU port boots unmodified iOS 16.7.16 on a Snapdragon Redmi Note 10 Pro](#item-tech-news-9) ⭐️ 7.0/10
10. [DHS bars DeepSeek from federal civilian procurement, orders removal](#item-tech-news-10) ⭐️ 7.0/10

**Technology Blog**
1. [Artistic Defenses of Technical Fields Miss Public Motivations](#item-tech-blog-1) ⭐️ 6.0/10

**Financial News**
1. [JPMorgan Chase invests $5 billion in defense and manufacturing startups in first year](#item-finance-news-1) ⭐️ 7.0/10
2. [Korea&\#x27;s pension fund loses about $137 billion as Samsung and SK Hynix shares fall](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [SGLang v0.5.22 adds new models, speedups; needs Python 3.11](https://github.com/sgl-project/sglang/releases/tag/v0.5.22) ⭐️ 7.0/10

SGLang v0.5.22 is out, comprising 950 PRs from 245 contributors and adding support for new LLM/VLM and diffusion models including Clef/Clef Flash, PPLX-Decider v1/v1.1, EmbeddingGemma 2, LLaDA2.2, HunyuanImage-3.0-Instruct, Kandinsky 6, Wan-Animate-2, SANA-Video 2.0, and LLaDA-Image. The release notes claim throughput gains—up to 2.3x per GPU for DeepSeek-V4.1 on H200, 12% faster Qwen3.8-Flash-Next decoding on B200, and 1.85x MiMo-V2.6-Pro decode with DFlash on B300—and a new InstantTensor loader that loads models 10x faster. It also adds Apple Silicon support through the standard PyTorch backend alongside MLX, requires Python 3.11 or newer, and is installable via pip with --prerelease=allow or through Docker images for NVIDIA CUDA 13, AMD MI35x/MI30x, Intel GPU, and Intel CPU.

github · ch-wan · Oct 19, 02:55

**「Background」** SGLang is an open-source framework for serving large language and diffusion models. Version 0.5.22 is a point release in the project&\#x27;s v0.5.x line, so its changes are framed as additions and fixes to an existing serving stack rather than a new major version.

**「Impact」** The hard compatibility change is Python 3.11 or newer: deployments still pinned to Python 3.10 or earlier must upgrade their runtime before adopting v0.5.22.

**Tags**: `#SGLang`, `#LLM inference`, `#model serving`, `#diffusion models`, `#open source`

---

<a id="item-tech-news-2"></a>
### [Hobbyist drone flies on a single motor with a variable-pitch hinge](https://www.youtube.com/watch?v=Ndftcft6XhU) ⭐️ 7.0/10

A build video posted to Hacker News shows a drone flying with only one motor, using a custom hinge, a magnetic encoder, and torque modulation to vary rotor pitch as it spins, eliminating the conventional helicopter swashplate. Commenters identify the creator as Joshua Bird, who previously built a four-axis 3D printer. The submission drew 392 points and 84 comments. The video itself was not reviewed for this summary, so the described mechanism rests on the post and discussion rather than independent inspection.

hackernews · hakonjdjohnsen · Oct 19, 09:05 · [Discussion](https://news.ycombinator.com/item?id=50150089)

**「Background」** Conventional helicopter rotors change blade pitch through a swashplate, the mechanical linkage that tilts the rotor disc to direct lift. Prior experiments have also flown copters without a swashplate by using separate motors to cyclically speed up and slow down; this build instead keeps a single motor and puts pitch variation in a custom hinge driven by torque modulation.

**「Why it matters for builders」** For hobbyist roboticists, the design&\#x27;s value is the trade it makes: the rotor hinge is mechanically simple, but all the difficulty moves into control, since lift is managed by modulating torque rather than by a mechanical swashplate. Commenter leoedin notes the single motor also spins the craft the moment it is airborne and suggests a two-motor layout with a tail motor would be more practical.

**「Community discussion」** Commenters placed the build in a wider lineage of underactuated machines: mrandish noted that fixed-wing RC aerobatics hobbyists have used variable-pitch propellers for years, with small integrated units available off the shelf, while TGower described a BattleBots design that moves in any direction and strikes opponents using a single motor&\#x27;s speed. Others, including nadermx, focused on the presentation, calling it a well-paced hacker-style build worth watching in full.

<details><summary>References</summary>
<ul>
<li><a href="https://electronics.stackexchange.com/questions/383671/how-this-flying-copter-actually-work">brushless dc motor - How this flying copter actually work - Electrical...</a></li>

</ul>
</details>

**Tags**: `#robotics`, `#underactuated-control`, `#drones`, `#hardware-hacking`, `#variable-pitch-propulsion`

---

<a id="item-tech-news-3"></a>
### [Wine ported to OpenBSD with OpenBSD-only changes](https://marc.info/?l=openbsd-ports&amp;m=179236125692175) ⭐️ 7.0/10

Wine, the compatibility layer for running Windows applications, has been ported to OpenBSD. The port is discussed on the openbsd-ports mailing list, and a linked message from the porter quoted in comments says many of the changes are OpenBSD-specific and unlikely to be merged upstream. That makes the work a separately maintained port rather than a set of changes expected to flow back into Wine.

hackernews · iamnothere · Oct 19, 13:35 · [Discussion](https://news.ycombinator.com/item?id=50152307)

**「Context」** Wine is a compatibility layer that implements Windows APIs so Windows binaries can run without a full Windows kernel or hardware emulator. On x86-64, its thread-local-storage handling depends on segment mechanisms such as %gs, and a report on the port says OpenBSD does not let userland set %gs/gsbase, which had been the sticking point. The port works around that restriction by emulating the %gs instruction prefix in software, clearing the way for the remaining compatibility work.

**「Impact」** OpenBSD users gain a way to run some Windows software through Wine, but because the porter marked OpenBSD-specific changes as OpenBSD-only and doubted much would be upstreamed, the port will need separate maintenance to track future Wine releases.

**「Community discussion」** A commenter highlighted the porter&\#x27;s statement that many OpenBSD changes are unlikely to be merged upstream, indicating that the port is expected to diverge from Wine upstream. No independent compatibility or performance results were reported in the supplied comments.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.adafruit.com/2026/10/19/wine-ported-to-openbsd/">Wine ported to OpenBSD - Adafruit Industries</a></li>

</ul>
</details>

**Tags**: `#Wine`, `#OpenBSD`, `#open source`, `#compatibility layer`, `#ports`

---

<a id="item-tech-news-4"></a>
### [Mac.apk runs Android apps natively on Apple Silicon Macs](https://github.com/kksimp/Mac.apk) ⭐️ 7.0/10

Mac.apk \(github.com/kksimp/Mac.apk\) is an open-source compatibility layer that, per its project description, runs Android apps natively on Apple Silicon Macs with no emulator, no virtual machine, and no Linux layer underneath. The supplied material characterizes it as an early proof of concept rather than a finished runtime, and includes no performance figures, supported-version list, or app-compatibility data. Its wiki, cited by a commenter, states that installed apps keep their data inside the .app bundle instead of in ~/Library/Application Support.

hackernews · flocked · Oct 19, 16:45 · [Discussion](https://news.ycombinator.com/item?id=50154624)

**「Background」** Android apps are typically written in Kotlin or Java and depend on Android&\#x27;s runtime and platform services, so running them on a Mac requires an emulator, a virtual machine, or a compatibility layer. Mac.apk&\#x27;s release materials describe it as a free public alpha that runs APKs as ordinary macOS processes on Apple Silicon, and APPDOOK reports that the alpha requires macOS 26.4 or later because it relies on an Apple capability for apps with native code.

**「Impact」** Practical usefulness will hinge on Google Play Services: commenter bilalq argued that Play Services dependencies and other Google walled-garden restrictions will make the layer &quot;less useful than it could otherwise be,&quot; so apps that require those APIs are unlikely to work. The in-bundle data layout also means deleting the .app removes the app&\#x27;s data with it, contradicting the macOS convention of storing user data separately from the application.

**「Community Discussion」** Commenters credited the technical achievement while disputing design choices: irskep called storing app data inside the .app file a &quot;false choice&quot; against the project&\#x27;s stated goal of not scattering files around the home folder, and andsoitis asked whether the approach still depends on the JVM given that Android apps are usually written in Kotlin or Java — a question left unanswered in the supplied thread. piro0919 offered a different take, saying they rarely want Android apps on a Mac but would want them on an iPhone, for cases such as SMS forwarding and a free VPN.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/kksimp/Mac.apk-Releases">kksimp / Mac . apk -Releases: MacDroid: Run Android apps natively on...</a></li>
<li><a href="https://appdook.com/news/mac-apk-android-apps-apple-silicon-alpha">Mac . apk runs Android apps on Apple silicon Macs - APPDOOK</a></li>

</ul>
</details>

**Tags**: `#android`, `#macos`, `#apple-silicon`, `#compatibility-layer`, `#open-source`

---

<a id="item-tech-news-5"></a>
### [Mistral announces Timestral, a family of time-series foundation models](https://mistral.ai/news/timestral/) ⭐️ 7.0/10

Mistral has announced Timestral, a family of foundation models for time-series forecasting, according to the company&\#x27;s announcement post. The available material carries no benchmarks, model sizes, licensing terms, or a clear statement of whether the models are released for use or only announced. The post, as quoted in the Hacker News thread, describes conditioning on known-future covariates — drivers such as production schedules, planned shutdowns, and weather forecasts that are known in advance — to inform forecasts.

hackernews · groar · Oct 19, 09:59 · [Discussion](https://news.ycombinator.com/item?id=50150434)

**「Background」** Time-series foundation models apply a pretrained, zero-shot approach to forecasting: one broadly trained model is meant to handle new series without fitting a separate model for each dataset. Mistral describes Timestral as its first family in this category, with the largest model at 209M parameters evaluated as a pretrained zero-shot forecaster on public benchmarks.

**「Impact」** With no published benchmarks in the supplied material, teams forecasting production or sensor time series would need to evaluate Timestral on their own data — including its handling of scale differences across series — before displacing existing per-series models or gradient-boosted baselines.

**「Community discussion」** Commenter logancbrown argues the case for a general model over the common &quot;just train XGBoost with holiday covariates&quot; advice: at 10,000 series, fitting one model per series leaves little history to learn from, while a single shared model must cope with scale mismatch between series. Others are more skeptical — joefourier questions whether &quot;time series&quot; is a coherent single category, and yaoke259 draws a ChatGPT-style zero-shot analogy but wonders whether large quant firms already have equivalent internal models.

<details><summary>References</summary>
<ul>
<li><a href="https://mistral.ai/news/timestral/">Timestral: Mistral&#x27;s time-series foundation models | Mistral</a></li>
<li><a href="https://explainx.ai/blog/timestral-mistral-time-series-foundation-models-209m-cpu-forecasting-2026">Timestral: Mistral Releases Time-Series Foundation Models ...</a></li>

</ul>
</details>

**Tags**: `#time-series`, `#foundation-models`, `#mistral`, `#forecasting`, `#machine-learning`

---

<a id="item-tech-news-6"></a>
### [Ask HN debates shipping AI-written code engineers don&\#x27;t fully understand](https://news.ycombinator.com/item?id=50151036) ⭐️ 7.0/10

An Ask HN thread asks how engineers should handle shipping AI-written code they do not fully understand, citing a LinkedIn post in which an engineer at Meta says the practice feels like a &quot;black box&quot; and conflicts with the instinct to understand what one builds. Commenters disagree on the remedy: some say engineers should design the abstractions and let an LLM fill in implementation, while others insist someone must read the code before production and treat tests as helpful but not sufficient. Others report spending less time coding and more time testing, including interactive testing with the model, and say they find implementation errors rather than coding errors.

hackernews · rzk · Oct 19, 11:24

**「Why reviewing AI-generated code is harder」** Large language model coding assistants can produce whole functions, files, and structures from a prompt, which shifts part of an engineer&\#x27;s work from writing code to reading and verifying code they did not compose. That verification is harder than reviewing a colleague&\#x27;s patch, because the reviewer has no prior model of the author&\#x27;s intent and must reconstruct the design from the output alone. The Ask HN thread grew out of a LinkedIn post in which a Meta engineer described shipping code that felt like a &quot;black box&quot; and asked how much understanding should be required before moving forward.

**「Impact」** For teams adopting LLM-assisted development, review and testing capacity becomes the constraint: commenters describe spending more time testing and warn that tests can themselves be wrong, so at least one person should be able to explain the shipped code.

**「Community discussion」** The thread&\#x27;s sharpest disagreement is over whether engineers should be expected to read and understand the code they ship: one commenter calls the comments &quot;horrifying&quot; for avoiding that responsibility, while others describe a principal-engineer model in which humans own the design and the LLM implements it. Several commenters say they now test more than before and find implementation errors rather than coding errors.

**Tags**: `#AI-assisted coding`, `#software engineering`, `#code review`, `#maintainability`, `#developer practices`

---

<a id="item-tech-news-7"></a>
### [Plex vulnerabilities reportedly exploited in the wild to install cryptominers](http://www.boredhackerblog.info/2026/10/plex-vulnerabilities-being-exploited-in.html) ⭐️ 7.0/10

Plex servers are reportedly being compromised in the wild to install cryptominers and other payloads, according to community reports relayed in a blog post that supplies little primary technical detail. Commenters point to a proof-of-concept exploit called Plex2Shell that chains several CVEs — no CVE identifiers appear in the supplied material — and say compromised hosts have also been used as DDoS nodes. The exposure described centers on operators running outdated versions: one commenter said their install was 13 months old and that they had missed Plex&\#x27;s &quot;please upgrade now&quot; email dated September 1. None of these reports are independently verified in the supplied material, and no affected or fixed version numbers were given.

hackernews · mindracer · Oct 19, 13:36 · [Discussion](https://news.ycombinator.com/item?id=50152321)

**「What is Plex2Shell?」** Plex2Shell is a public exploit chain that links four Plex Media Server vulnerabilities into unauthenticated remote code execution. A write-up and proof-of-concept were published on October 16, 2026, and attackers began targeting the chain one day later, according to reports.

**「Patch and check for miners」** Operators of internet-facing Plex servers should verify their installed version and upgrade, since one commenter reported a compromise traced to a 13-month-old install after missing Plex&\#x27;s September 1 upgrade notice, and another found a miner only after noticing sustained 100% CPU use. Because the payloads observed in the thread disguised themselves under ordinary-looking process names such as &quot;mylovelyminer&quot; and &quot;icloud-services,&quot; CPU monitoring alone may not identify an intrusion, and the supplied material contains no Plex-confirmed advisory, affected version list, or CVE identifiers to guide a targeted check.

**「Community discussion」** Firsthand accounts describe noticing infections through sudden CPU load: one user found a miner process named &quot;mylovelyminer&quot; on a 13-month-old install, while another traced a 100% CPU process disguised as &quot;icloud-services&quot; to a folder under Library on a Mac mini. Another commenter cited Reddit reports of additional payloads and questioned why anyone would expose Plex servers directly to the internet, a concern about internet-facing deployments rather than agreement on a fix.

<details><summary>References</summary>
<ul>
<li><a href="https://cybersecuritynews.com/plex-vulnerabilities-exploited-in-wild/">Hackers Exploiting Plex Vulnerabilities in the Wild to Deploy ...</a></li>
<li><a href="https://www.securityweek.com/plex2shell-exploit-chain-weaponized-against-plex-servers-hours-after-disclosure/">Plex2Shell Exploit Chain Weaponized Against Plex Servers ...</a></li>
<li><a href="https://securityonline.info/plex2shell-plex-media-server-exploited/">Plex Media Server Vulnerabilities Exploited in the Wild</a></li>

</ul>
</details>

**Tags**: `#Plex`, `#security vulnerabilities`, `#cryptomining malware`, `#exploits in the wild`, `#CVE chaining`

---

<a id="item-tech-news-8"></a>
### [SemiAnalysis Expects Datacenter Build to Reach 50GW in 2027](https://newsletter.semianalysis.com/p/datacenters-2027-the-year-of-acceleration) ⭐️ 7.0/10

SemiAnalysis&\#x27;s October 19 analysis projects that datacenter capacity additions will accelerate toward 2027, with 60GW under construction and annual build potentially reaching 50GW in a single year. It also cites $1.3 trillion in lease contracts signed year-to-date and warns that the supply bottleneck could shift from power and construction to chips. These are forward-looking estimates from the firm, not independently measured capacity or completed construction.

rss · Semianalysis · Oct 19, 05:39

**「Why capacity is counted in gigawatts」** Datacenter buildout is typically measured in gigawatts rather than floor space or server counts, because available power and grid interconnection set the ceiling on how much compute a site can actually run. SemiAnalysis&\#x27;s forecast is therefore a claim about power capacity added per year: 60GW currently under construction, a projected 50GW annual build, and $1.3T in lease contracts signed year-to-date. Because the supplied material is a summary of the analysis, the assumptions behind those figures — and the basis for the warning that the bottleneck could move to chips — are not detailed here.

**「Impact」** If annual datacenter additions approach the projected 50GW, operators and AI developers should secure accelerator allocations in parallel with power and construction contracts, because SemiAnalysis warns the bottleneck could shift to chips. Otherwise, capacity that is physically built may sit unusable if semiconductor supply tightens.

**Tags**: `#data centers`, `#AI infrastructure`, `#power constraints`, `#semiconductors`, `#industry analysis`

---

<a id="item-tech-news-9"></a>
### [XNU port boots unmodified iOS 16.7.16 on a Snapdragon Redmi Note 10 Pro](https://www.reddit.com/r/hackintosh/comments/1x95qq0/ios_16716_booting_on_a_snapdragon_732g_redmi_note/?sort=new) ⭐️ 7.0/10

A developer has ported Apple&\#x27;s open-source XNU kernel to a Redmi Note 10 Pro and booted an unmodified iPhone X iOS 16.7.16 user space to the iOS home screen, with touch and physical buttons working as of October 18. The proof-of-concept renders entirely on the CPU at about 20–30 frames per second; there is no GPU driver, and Wi-Fi and the camera are not yet usable. The code has been published on GitHub.

telegram · zaihuapd · Oct 19, 06:30

**「What XNU is and why this is hard」** XNU is the open-source kernel at the core of Apple&\#x27;s operating systems, but the iOS user space and the drivers for Apple&\#x27;s hardware are not open. Running iOS on a non-Apple phone therefore means pairing a ported kernel with a user space built for iPhone hardware, then writing drivers from scratch — which is why the project so far lacks GPU, Wi-Fi, and camera support and renders the interface on the CPU.

**「Impact」** The missing GPU, Wi-Fi, and camera support means this is not a practical daily-use phone system; developers can inspect the published code, but the hardware gaps limit it to a proof-of-concept.

**Tags**: `#XNU kernel`, `#iOS porting`, `#Snapdragon 732G`, `#mobile OS hacking`, `#open source`

---

<a id="item-tech-news-10"></a>
### [DHS bars DeepSeek from federal civilian procurement, orders removal](https://www.federalregister.gov/public-inspection/2026-21447/order-exclusion-and-removal-of-deepseek-products-from-federal-civilian-executive-branch-information) ⭐️ 7.0/10

The Department of Homeland Security issued an order under the Federal Acquisition Supply Chain Security Act excluding information technology products and services developed by Hangzhou DeepSeek Artificial Intelligence Basic Technology Research Co., Ltd. and its affiliated entities from federal civilian executive branch procurement. The order also requires that all DeepSeek and affiliate products be removed from civilian agency information systems, and explicitly extends to third-party products and services implemented using DeepSeek. The notice, published for public inspection in the Federal Register, follows earlier use restrictions imposed by the Department of Defense and the intelligence community. It is a policy and procurement directive rather than a technical assessment, and the source does not specify removal deadlines or an implementation timetable.

telegram · zaihuapd · Oct 19, 13:32

**「Background」** The order cites the Federal Acquisition Supply Chain Security Act, which lets U.S. federal agencies bar specified products from government procurement on supply-chain security grounds. DeepSeek was already subject to similar usage restrictions at the Department of Defense and within the intelligence community; this notice extends that treatment to civilian executive-branch agencies.

**「Impact」** Civilian agencies and their suppliers must now inventory systems for DeepSeek-derived components, including third-party offerings built on the model, and drop them from procurement pipelines — meaning organizations that embedded DeepSeek through a vendor product rather than directly still fall in scope and may need to re-evaluate those deployments.

**Tags**: `#DeepSeek`, `#AI policy`, `#supply chain security`, `#US government`, `#procurement`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Artistic Defenses of Technical Fields Miss Public Motivations](https://seangoedecke.com/laypeople-support-technical-fields-for-technology-not-art/) ⭐️ 6.0/10

rss · Sean Goedecke · Oct 20, 00:00

**「Background」** Some critics argue that LLMs should be excluded from programming and mathematics because those fields are essentially art rather than mere problem-solving. Sean Goedecke grants that technical work can be beautiful, but doubts that this claim can persuade people outside the field.

**「Solution」** He argues that laypeople support mathematics and programming because they value the technology those fields sustain, and they value science because it enables that technology; artistic value is accepted mainly insofar as it eventually advances the knowledge frontier. Telling the public that art is the real point of technical work therefore feels like a contractor insisting on hand tools to enjoy creation—and it is even less persuasive to employers. Goedecke says defenders must instead connect artistic value to practical effectiveness, for example by arguing that complex software needs elegant abstractions, mathematical progress needs new abstractions and human inspiration, or truly great software requires a human creative touch. He is not fully convinced by these arguments: he has not seen an LLM-built codebase hit a wall this year, sees no reason LLMs cannot create abstractions or have human-like inspiration, and questions whether great products require great code.

**「Takeaway」** The author&\#x27;s conclusion is that appeals to art alone concede the public&\#x27;s main reason for valuing technical work. Defenders of human-made programming and mathematics must make an affirmative case that artistic creativity makes technical work more effective.

**Tags**: `#LLMs`, `#software engineering`, `#mathematics`, `#public perception of science`, `#art vs technology`

---

## Financial News

<a id="item-finance-news-1"></a>
### [JPMorgan Chase invests $5 billion in defense and manufacturing startups in first year](https://www.cnbc.com/2026/10/19/jpmorgan-security-defense-investments.html) ⭐️ 7.0/10

JPMorgan Chase said it invested $5 billion in defense, manufacturing and supply-chain startups in the first year of its U.S. security and resiliency initiative, against a $10 billion target over a decade and faster than expected. The bank may expand the program beyond that initial amount, co-President Doug Petno told CNBC; disclosed stakes include automated-factory firm Hadrian and hypersonic-missile maker Castelion.

rss · CNBC Finance · Oct 19, 12:34

**「Background」** JPMorgan set up its Security and Resiliency Initiative as a $1.5 trillion, 10-year plan to finance and invest in industries deemed critical to economic security, with an initial $10 billion allocated to startup investments. In December 2025, it named former Berkshire Hathaway executive Todd Combs to lead that investment group.

<details><summary>References</summary>
<ul>
<li><a href="https://www.jpmorganchase.com/newsroom/press-releases/2025/jpmorganchase-names-todd-combs-to-head-strategic-investment-group">JPMorganChase names Todd Combs to head Strategic Investment ...</a></li>
<li><a href="https://www.jpmorgan.com/about-us/security-and-resiliency">Security and Resiliency Initiative: Boosting Critical Industries</a></li>

</ul>
</details>

**Tags**: `#defense technology`, `#banking`, `#venture capital`, `#supply chain`, `#national security`

---

<a id="item-finance-news-2"></a>
### [Korea&\#x27;s pension fund loses about $137 billion as Samsung and SK Hynix shares fall](https://www.bloomberg.com/news/articles/2026-10-19/samsung-sk-hynix-slide-causes-137-billion-hit-to-korea-pension?srnd=phx-technology) ⭐️ 7.0/10

South Korea&\#x27;s National Pension Service saw the value of its stakes of 5% or more in 287 listed companies fall to 333.53 trillion won on Oct. 15 from 515.93 trillion won at the end of June, a drop of about 182 trillion won \(roughly $137 billion\), Bloomberg reported. The fund attributed the decline to falling shares including Samsung Electronics and SK Hynix, marking its first quarterly drop since the fourth quarter of 2024.

telegram · zaihuapd · Oct 19, 08:00

**「Background」** The National Pension Service is South Korea&\#x27;s public pension fund, so this decline is a paper loss on the retirement savings it manages for members. It tracked a sharp slide in chip stocks: Samsung Electronics fell 17.8% and SK Hynix 24.3% in the week of Oct 12–16, Samsung&\#x27;s steepest weekly drop since October 2008, according to Korea Exchange data.

<details><summary>References</summary>
<ul>
<li><a href="https://en.sedaily.com/finance/2026/10/19/samsung-sk-hynix-post-worst-weekly-drop-since-2008-crisis">Samsung, SK hynix Post Worst Weekly Drop Since 2008 Crisis</a></li>

</ul>
</details>

**Tags**: `#South Korea pension fund`, `#Samsung Electronics`, `#SK Hynix`, `#semiconductor stocks`, `#market selloff`

---