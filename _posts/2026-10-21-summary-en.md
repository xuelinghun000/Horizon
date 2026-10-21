---
layout: default
title: "Horizon Summary: 2026-10-21 (EN)"
date: 2026-10-21
lang: en
---

> From 135 items, 4 important content pieces were selected

---

**Technology News**
1. [OpenAI models reportedly hit 97.9% accuracy on COBOL migration](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenAI API adds 12-hour prompt caching](#item-tech-news-2) ⭐️ 8.0/10

**Financial News**
1. [China&\#x27;s MIIT tightens market-entry rules for innovative car designs](#item-finance-news-1) ⭐️ 7.0/10
2. [SpaceX and Tesla Boards Form Special Committees to Review Merger](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenAI models reportedly hit 97.9% accuracy on COBOL migration](https://openai.com/index/low-resource-programming-languages/) ⭐️ 8.0/10

A Telegram channel that aggregates tech news reports that OpenAI&\#x27;s newest models sharply improved their ability to write and convert rarely used programming languages — COBOL, Fortran and Visual Basic — which still run many bank and government systems. In the post&\#x27;s figures, a model it calls GPT-6 Astra passed 87.4% of a test that builds a small database engine \(SQLite\) from scratch in 20 different languages, up from 26.8% for GPT-5.6 Sol, while a cheaper model, GPT-6 Luna, reached 40.3% with API costs \(the per-use fees developers pay to send requests to a model\) down 78%. For converting old COBOL code into modern languages, GPT-6.1 Sol rose from 5.4% to 86.6% accuracy at low reasoning effort \(how much internal computation the model spends before answering\) with 39% lower cost, and reached 97.9% at high effort. The post says the test set is now public on GitHub, but the model names, scores and prices have not been confirmed on OpenAI&\#x27;s own page, so the numbers should be read as a claim rather than a verified result.

telegram · zaihuapd · Oct 20, 14:24

**「Background」** Low-resource programming languages are languages with relatively little public code for AI models to learn from, such as COBOL, Fortran and Visual Basic. COBOL in particular still sits inside critical financial systems, and moving that old code to modern languages is a longstanding and costly task.

**「What it means in practice」** The people most affected are teams keeping old COBOL systems running — banks, insurers, government agencies — and for them the useful part is not the headline number but the claim that the test set is now public on GitHub, which would let them run a small trial migration and check the results before committing to a rewrite. The caution is that every figure here, including the 97.9% accuracy and the 78% cost reduction, comes from a Telegram aggregator rather than OpenAI&\#x27;s own page, so treat them as unconfirmed until the primary announcement and the open evaluation set can be inspected.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/low-resource-programming-languages/">Advancing coding in low‑resource programming languages - OpenAI</a></li>
<li><a href="https://the-decoder.com/openai-says-gpt-6-is-much-better-with-legacy-programming-languages-such-as-cobol-and-fortran/">OpenAI says GPT-6 is much better with legacy programming ...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#model-release`, `#code-migration`, `#API-pricing`, `#benchmarks`

---

<a id="item-tech-news-2"></a>
### [OpenAI API adds 12-hour prompt caching](https://x.com/OpenAIDevs/status/2112603916076781778) ⭐️ 8.0/10

OpenAI says its API \(the interface developers use to build OpenAI models into their own software\) now supports 12-hour prompt caching, meaning a stored copy of instructions, tools, and context can be reused across requests separated by several hours, with the reused input billed at a lower rate. The company also says logged-in users of Codex and Work get permanent caching with guaranteed cache hits, including when they return to an old conversation or resume after a pause. The announcement did not give specific prices or limits.

telegram · zaihuapd · Oct 21, 01:21

**「What prompt caching is」** Prompt caching lets OpenAI&\#x27;s API hold on to the start of a request — the standing instructions, the list of tools the model may call, and pasted-in context — so a follow-up request does not have to be processed from scratch, and that reused portion is billed at a lower input rate. The discount has depended on timing: it only helped if the next request arrived while the stored copy was still alive, so an assistant that sat idle for hours effectively started over at full price. The announcement presents the 12-hour window, and permanent caching for logged-in Codex and Work users, as removing that penalty for long gaps.

**「What changes for daily agent users」** For anyone running an assistant that works in bursts across a day — the same instructions, tool descriptions and background material sent again and again — those repeated parts can now be billed at the lower cached-input rate even when hours pass between requests, instead of being paid for at full price each time. The limit to plan around is the guarantee: OpenAI says only Codex and Work users who are signed in get a guaranteed cache hit, so API developers should treat the discount as likely rather than certain and check their own usage bills before budgeting a fixed cost per run. A third-party cost comparison puts OpenAI&\#x27;s cache-read price at one-tenth of the normal input price, which is where the saving comes from.

<details><summary>References</summary>
<ul>
<li><a href="https://ofox.ai/blog/prompt-caching-cost-math-anthropic-vs-openai-2026/">Anthropic vs OpenAI Prompt Caching 2026: Cost Math...</a></li>

</ul>
</details>

**Tags**: `#OpenAI API`, `#prompt caching`, `#Codex`, `#API pricing`, `#developer tooling`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s MIIT tightens market-entry rules for innovative car designs](https://m.chinanews.com/wap/detail/chs/zw/10717890.shtml) ⭐️ 7.0/10

China&\#x27;s Ministry of Industry and Information Technology said on October 20 that it will block vehicle products with unreasonable innovative designs or insufficient testing from entering the market, requiring features such as hidden door handles and electric suction doors to go through market-entry management. Under the notice, electric suction doors must have anti-pinch protection, zero-gravity and rotating seats are banned for use while driving, 22 recommended standards become mandatory, and reliability testing must cover at least 30,000 km.

telegram · zaihuapd · Oct 20, 12:48

**「Background」** The Oct 20 announcement follows a draft notice MIIT published on Oct 10, 2026, which proposed tighter approval requirements for innovative vehicle designs covering doors, displays and seats, after a mandatory national standard on door handle safety was released. In China&\#x27;s standards system, &quot;recommended&quot; standards are voluntary guidelines, while &quot;mandatory&quot; ones must be met before a model can be sold.

**「Who is affected」** Automakers selling in China, especially EV makers that adopted hidden door handles and electric suction doors, will have to redesign and re-certify those features before launch, with the mandatory hidden-door-handle standard taking effect on January 1, 2027.

<details><summary>References</summary>
<ul>
<li><a href="https://cnevpost.com/2026/10/10/china-proposes-tighter-vehicle-design-rules/">China proposes tighter vehicle design rules, reiterates ...</a></li>
<li><a href="https://www.reuters.com/world/asia-pacific/china-proposes-stricter-car-design-testing-rules-including-ban-fully-hidden-door-2026-10-10/">China proposes stricter car design, testing rules, including ...</a></li>
<li><a href="https://cnevpost.com/2026/02/03/china-new-auto-safety-standard-bans-hidden-door-handles/">China&#x27;s new auto safety standard bans hidden door handles</a></li>

</ul>
</details>

**Tags**: `#China auto policy`, `#MIIT regulation`, `#vehicle safety standards`, `#automotive industry`, `#consumer safety`

---

<a id="item-finance-news-2"></a>
### [SpaceX and Tesla Boards Form Special Committees to Review Merger](https://techcrunch.com/2026/10/20/spacex-and-tesla-boards-form-special-committees-to-review-merger/) ⭐️ 7.0/10

SpaceX and Tesla boards have each formed special committees of independent directors to review a possible merger, according to TechCrunch. Elon Musk said he would not take part because of a conflict of interest, and the two companies have not agreed on any deal terms; Musk said any transaction would need shareholder approval, including a 50% vote of all Tesla shareholders.

telegram · zaihuapd · Oct 21, 02:06

**「Background」** The committees are made up of independent directors — board members without management ties — and were formed at shareholders’ request; Musk, who backs a merger, said he would not take part because of a conflict of interest.

**「What it means for Tesla shareholders」** Any deal would need approval from holders of 50% of all Tesla shares, not just a majority of votes cast, so the outcome depends on how many shareholders actually vote — a higher bar than SpaceX&\#x27;s simpler shareholder vote described in the report.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/10/20/spacex-and-tesla-boards-form-special-committees-to-review-merger/">SpaceX and Tesla boards form special committees to review merger</a></li>

</ul>
</details>

**Tags**: `#SpaceX`, `#Tesla`, `#merger review`, `#corporate governance`, `#Elon Musk`

---