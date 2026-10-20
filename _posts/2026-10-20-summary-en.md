---
layout: default
title: "Horizon Summary: 2026-10-20 (EN)"
date: 2026-10-20
lang: en
---

> From 56 items, 6 important content pieces were selected

---

**Technology News**
1. [Plex vulnerabilities being exploited in the wild to drop a cryptominer](#item-tech-news-1) ⭐️ 8.0/10
2. [SemiAnalysis Projects 50 Gigawatts of New Datacenter Capacity in 2027](#item-tech-news-2) ⭐️ 8.0/10
3. [Wine ported to OpenBSD](#item-tech-news-3) ⭐️ 7.0/10
4. [Open-source Mac.apk project runs Android apps directly on Apple Silicon Macs, no emulator needed](#item-tech-news-4) ⭐️ 7.0/10
5. [Engineers split on shipping AI-written code they don&\#x27;t fully understand](#item-tech-news-5) ⭐️ 7.0/10
6. [US Homeland Security orders DeepSeek products removed from civilian federal agencies](#item-tech-news-6) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Plex vulnerabilities being exploited in the wild to drop a cryptominer](http://www.boredhackerblog.info/2026/10/plex-vulnerabilities-being-exploited-in.html) ⭐️ 8.0/10

Attackers are exploiting known, unpatched Plex server vulnerabilities in the wild to install cryptominers \(and other payloads\), prompting Plex users to urgently update their media servers.

hackernews · mindracer · Oct 19, 13:36 · [Discussion](https://news.ycombinator.com/item?id=50152321)

**Tags**: `#security`, `#plex`, `#vulnerability-exploitation`, `#cryptomining`, `#self-hosting`

---

<a id="item-tech-news-2"></a>
### [SemiAnalysis Projects 50 Gigawatts of New Datacenter Capacity in 2027](https://newsletter.semianalysis.com/p/datacenters-2027-the-year-of-acceleration) ⭐️ 8.0/10

The industry research firm SemiAnalysis projects that datacenters — buildings packed with the computers that run online services and AI — will add roughly 50 gigawatts \(a measure of electrical power; one gigawatt is about the output of a large nuclear reactor\) of new capacity in 2027 alone. The firm counts about 60 gigawatts already under construction and reports roughly $1.3 trillion in datacenter lease contracts signed so far this year — long-term rental commitments that lock in demand before the buildings are finished. SemiAnalysis warns that the next shortage may shift from buildings and power to chips, the specialized processors that run AI. These figures are projections based on the firm&\#x27;s tracking of construction and leasing activity, not capacity already in service.

rss · Semianalysis · Oct 19, 05:39

**「Background」** Datacenters — the building-sized facilities packed with computers that run AI and online services — are sized by how much electricity they can draw, measured in gigawatts \(GW\); one gigawatt is roughly the output of a large power plant. Because a new facility takes years to plan and build, the long-term rental contracts \(leases\) that cloud and AI companies sign today act as early signals of how much will actually be built years later. Each datacenter also needs a second ingredient — the specialized chips that carry out AI calculations — so a shortage of either buildings-and-power or chips can set the pace of growth.

**「What it means for you」** If chip supply becomes the limiting factor, having more buildings will not automatically mean more AI computing power, so the pace at which AI services expand could slow even as construction booms. Because the $1.3 trillion in leases represents signed commitments rather than running capacity, it is reasonable to treat companies&\#x27; announced AI capacity plans as promises still pending rather than services already available.

<details><summary>References</summary>
<ul>
<li><a href="https://aicoder.com/news/news-1792424548152-h6xez">SemiAnalysis Releases Landmark Datacenters 2027 Report: +50GW ...</a></li>

</ul>
</details>

**Tags**: `#datacenters`, `#AI infrastructure`, `#semiconductors`, `#capacity planning`, `#industry analysis`

---

<a id="item-tech-news-3"></a>
### [Wine ported to OpenBSD](https://marc.info/?l=openbsd-ports&amp;m=179236125692175) ⭐️ 7.0/10

Wine, the Windows application compatibility layer, has been ported to OpenBSD, with the developer sharing technical details and community members demonstrating Windows games running on the OS.

hackernews · iamnothere · Oct 19, 13:35 · [Discussion](https://news.ycombinator.com/item?id=50152307)

**Tags**: `#OpenBSD`, `#Wine`, `#operating-systems`, `#open-source`, `#compatibility-layer`

---

<a id="item-tech-news-4"></a>
### [Open-source Mac.apk project runs Android apps directly on Apple Silicon Macs, no emulator needed](https://github.com/kksimp/Mac.apk) ⭐️ 7.0/10

A community-built, open-source project called Mac.apk \(its code is public on GitHub for anyone to inspect\) lets people run Android phone apps directly on Macs with Apple Silicon chips \(Apple&\#x27;s own processors, such as the M-series\). It needs no emulator \(software that imitates another device\) and no virtual machine \(a separate simulated computer running inside the Mac\); the Android apps run on the Mac&\#x27;s own system. The project drew a busy Hacker News discussion \(275 upvotes, 144 comments\), where early users report real successes — one now plays Minecraft on a Mac with friends on phones and consoles — but also limits: apps that depend on Google Play Services, Google&\#x27;s background software that many Android apps require, may not work. It is an early-stage tool rather than an official product from Apple or Google.

hackernews · flocked · Oct 19, 16:45 · [Discussion](https://news.ycombinator.com/item?id=50154624)

**「Background」** Android apps are normally built for phones and tablets, and running them on a Mac has traditionally required an emulator \(software that imitates an entire phone, including its processor\) or a virtual machine \(a separate simulated computer running inside your real one\) — approaches that tend to be slow and clunky. The project behind this story, called Mac.apk, takes a different route: it recreates the parts of Android that apps depend on directly on top of macOS, so an app runs as an ordinary Mac program. It uses the Mac&\#x27;s own graphics chip and processor at full speed, and the apps appear in the Dock and behave like regular Mac windows.

**「Practical impact」** For Mac users, the concrete payoff is running apps that were previously phone- or console-only: one commenter says the Android version of Minecraft lets them play with friends on consoles and phones without resorting to workarounds like running their own game server. The compatibility caveat matters in practice — before relying on the tool, check whether the specific app you need depends on Google Play Services, since those apps may fail.

**「What readers are saying」** Commenters&\#x27; main criticisms were practical: irskep objected that the project stores each app&\#x27;s data inside the app file itself rather than macOS&\#x27;s standard folder for app data \(Application Support\), calling the project&\#x27;s justification &quot;a false choice,&quot; and bilalq predicted that apps tied to Google&\#x27;s own services will keep the tool less useful than it could be. Several readers, including qalmakka, were more struck by the project&\#x27;s readme — its phrasing \(&quot;No emulator, no virtual machine, no Linux underneath&quot;\) struck them as recognizably AI-written, which they took as a caution about the project&\#x27;s polish rather than its function.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/kksimp/Mac.apk">GitHub - kksimp/Mac.apk: Mac.apk: Run Android apps natively ...</a></li>
<li><a href="https://daily.dev/posts/android-apps-running-native-on-macos-gcspqvspy">Android apps running native on macOS - daily.dev</a></li>

</ul>
</details>

**Tags**: `#android`, `#macos`, `#apple-silicon`, `#open-source`, `#runtime`

---

<a id="item-tech-news-5"></a>
### [Engineers split on shipping AI-written code they don&\#x27;t fully understand](https://news.ycombinator.com/item?id=50151036) ⭐️ 7.0/10

A question posted to Hacker News — a popular online forum for software developers — on October 19, 2026 drew 294 upvotes and 439 comments, asking how engineers should handle releasing code written by AI tools when they don’t fully understand it. The poster quoted a Meta engineer’s LinkedIn post describing coding that now feels like a “black box”: checking every line takes too long, so developers end up knowing a system’s big picture but not its details. Replies split into two camps — some keep control by designing the software’s structure themselves and letting the AI write the actual code, or lean heavily on testing, while others insist at least one person must be able to read and explain every line before it reaches real users. The thread is a practitioner debate rather than a product release or study, but the volume of responses shows how many working engineers are grappling with the question.

hackernews · rzk · Oct 19, 11:24

**「Background」** The discussion stems from a LinkedIn post by Ali Hamie, a software engineer at Meta \(the company behind Facebook and Instagram\), who said he has not manually written a single line of code in three months, instead directing AI tools to write it for him — and that the resulting code now feels like a &quot;black box&quot; he does not fully understand. AI coding assistants \(software that generates program code from plain-language instructions\) have spread quickly enough in workplaces that some engineers now review and release far more code than they personally wrote or read. The Hacker News thread asks what responsibility an engineer still carries when they ship code they could not have checked line by line.

**「Practical impact」** For people who simply use software, the near-term effect is that features may be built faster, but their quality depends on how much teams test what the AI writes instead of reading it line by line. Several commenters said they now redirect time saved on writing code into testing; one reported that an AI review of his own mature code — which he had considered flawless — turned up problems he had missed.

**「What commenters said」** The sharpest pushback came from a commenter who called fellow posters’ avoid-reading habits “horrifying” and argued that someone at every company must be able to explain any code running for real users — automated tests help, he said, but can’t be relied on alone. Against that, a self-described principal engineer \(a senior engineering role\) argued that AI simply lets everyone work the way senior engineers long have: design the system yourself, then let the AI build the details the way junior staff once did.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/ali-hamie_im-an-engineer-at-meta-and-i-never-felt-share-7517317918666211328-7C8N">Ali Hamie’s Post - LinkedIn</a></li>
<li><a href="https://ca.linkedin.com/in/ali-hamie">Ali Hamie - Software Engineer @ Meta | LinkedIn From Coding to Directing: Leveraging AI in ... - LinkedIn Ali Hamie’s Post - LinkedIn Meta Engineers Now Direct AI Code Generation | Ali Hamie ... From Code to AI Management: Evolving Software Engineer Role Ask HN: How to deal with shipping AI-written code you don&#x27;t ...</a></li>

</ul>
</details>

**Tags**: `#ai-generated-code`, `#software-engineering`, `#code-review`, `#developer-practices`, `#llm`

---

<a id="item-tech-news-6"></a>
### [US Homeland Security orders DeepSeek products removed from civilian federal agencies](https://www.federalregister.gov/public-inspection/2026-21447/order-exclusion-and-removal-of-deepseek-products-from-federal-civilian-executive-branch-information) ⭐️ 7.0/10

The U.S. Department of Homeland Security has issued an order, published in the Federal Register \(the government&\#x27;s official rule-notice publication\), that bars products from the Chinese AI company DeepSeek and its affiliated entities from being purchased by federal civilian agencies, and requires those agencies to remove any DeepSeek products already running in their systems. The order relies on the Federal Acquisition Supply Chain Security Act, a law that lets the government block technology it considers a supply-chain risk \(meaning worry that a component could be compromised or misused by its maker\). Notably, the ban extends beyond DeepSeek&\#x27;s own software to third-party products and services that were built using DeepSeek. This follows similar restrictions the Department of Defense and U.S. intelligence agencies had already placed on DeepSeek; the vendor&\#x27;s claims are a matter of official government action, not a technical evaluation published this week.

telegram · zaihuapd · Oct 19, 13:32

**「Background」** DeepSeek \(full company name: Hangzhou DeepSeek Artificial Intelligence Basic Technology Research Co., Ltd.\) is a Chinese company that makes artificial-intelligence products and services, and other companies can build their own software on top of them. The order relies on the Federal Acquisition Supply Chain Security Act, a U.S. law that works like a government-wide do-not-buy list: it lets agencies bar technology considered a supply-chain security risk and requires removing it from systems already in use. According to the source, the Pentagon and U.S. intelligence agencies had already imposed similar restrictions on DeepSeek, so this order extends those limits to the federal government&\#x27;s civilian agencies.

**「What this means in practice」** If your company sells software or services to U.S. federal civilian agencies, you now need to check whether any product relies on DeepSeek \(a Chinese AI company whose models power many chatbots and tools\) — even indirectly, through another vendor — because such products are barred from purchase and must be removed from agency systems. Vendors using DeepSeek models under a different brand name are still covered, so simply relabeling a product does not avoid the order.

**「What people are saying」** No community comments were available for this item.

<details><summary>References</summary>
<ul>
<li><a href="https://public-inspection.federalregister.gov/2026-21447.pdf">DEPARTMENT OF HOMELAND SECURITY Procurements Notice of Order ...</a></li>
<li><a href="https://articlesaboutai.com/us-deepseek-removal-order-federal-agencies/">US Orders Removal of DeepSeek AI Products From Federal ...</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#DeepSeek`, `#government procurement`, `#supply chain security`, `#US-China tech`

---