---
layout: default
title: "Horizon Summary: 2026-10-31 (EN)"
date: 2026-10-31
lang: en
---

> From 35 items, 13 important content pieces were selected

---

**Technology News**
1. [Azure Cross‑Tenant Compromise Findings](#item-tech-news-1) ⭐️ 9.0/10
2. [Working NES emulator built from ~1 GB Qwen model](#item-tech-news-2) ⭐️ 8.0/10
3. [Signoz newsletter: AI deskilling erodes SRE understanding](#item-tech-news-3) ⭐️ 8.0/10
4. [Backdoor in Claude Code for VS Code extension on the Cursor Marketplace](#item-tech-news-4) ⭐️ 7.0/10
5. [Northflank Breached](#item-tech-news-5) ⭐️ 7.0/10
6. [The $6.3B Binance hack was pulled off in just 20 minutes](#item-tech-news-6) ⭐️ 7.0/10
7. [Soft-MTP: One-Line Fix Improves Multi-Token Prediction](#item-tech-news-7) ⭐️ 7.0/10
8. [美 FCC 拟禁止中国三大运营商直接获取美国号码资源](#item-tech-news-8) ⭐️ 7.0/10
9. [Cursor 扩展市场 OpenVSX 中 Claude Code 插件被投毒](#item-tech-news-9) ⭐️ 7.0/10

**Financial News**
1. [DeepSeek raises 10.55 billion RMB in second funding round](#item-finance-news-1) ⭐️ 8.0/10
2. [US Semiconductor Stocks Plunge, Intel Drops Over 26%](#item-finance-news-2) ⭐️ 8.0/10
3. [📱 苹果下调中国台湾地区 App Store 交易佣金费率，由 30% 降至 26%](#item-finance-news-3) ⭐️ 7.0/10
4. [Four Japanese automakers&\#x27; China production falls below 40% of 2020 peak](#item-finance-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Azure Cross‑Tenant Compromise Findings](https://www.binarysecurity.no/posts/2026/10/one-root-case) ⭐️ 9.0/10

Security researcher swq115 disclosed five full cross‑tenant compromises in Microsoft Azure, demonstrating that the admin consent callback on login.microsoftonline.com/XXX/v2.0/adminconsent can be forged by an attacker who knows a different tenant’s ID. The report also identified path‑traversal and IDOR weaknesses that have been active since the services were introduced. These vulnerabilities affect any Azure customer whose applications use the affected authentication flow.

hackernews · swq115 · Oct 30, 10:06 · [Discussion](https://news.ycombinator.com/item?id=50301854)

**「Earlier Research on Azure Cross-Tenant Vulnerabilities」** Prior research revealed that Azure Logic Apps API Connections had an insecure architecture enabling full cross-tenant compromise, including access to Key Vault and other backends \(tool-1-1, tool-1-2\). A related talk detailed three critical cross-tenant breaks sharing the same architectural root cause, which together earned over $120,000 in bounties \(tool-1-3\).

**「Impact」** Organizations using Azure may suffer unauthorized access to resources if they rely on the vulnerable admin consent flow, requiring immediate mitigation such as disabling the callback or enforcing stricter token validation.

**「Community Discussion」** The community highlighted that the forgeable admin consent callback on login.microsoftonline.com is a critical issue, with a user urging Microsoft to remediate it, while others noted Azure&\#x27;s relative abundance of cross‑tenant leaks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.binarysecurity.no/posts/2026/10/one-root-case">Azure&#x27;s Weakest Link - Five Full Cross-Tenant Compromises</a></li>
<li><a href="https://binarysecurity.no/posts/2025/08/azures-weakest-link-part2">Azure&#x27;s Weakest Link - Full Cross-Tenant Compromise</a></li>
<li><a href="https://citation.thinkst.com/talk/113267">One Root Cause, Three Cross-Tenant Breaks in Azure</a></li>

</ul>
</details>

**Tags**: `#Azure Security`, `#Cross-Tenant Vulnerabilities`, `#Cloud Security`, `#Zero Trust`

---

<a id="item-tech-news-2"></a>
### [Working NES emulator built from ~1 GB Qwen model](https://github.com/dbreunig/nesformer) ⭐️ 8.0/10

A working Nintendo Entertainment System emulator has been released as an open‑source project on GitHub, implemented entirely from a ~1 GB Qwen language model that includes both CPU and RAM emulation via a gated deltanet architecture. The model was generated using Opus 5.5 with only two prompts, based on the Qwenputer article and a description of NES chip emulation. Benchmarks reported in the discussion show the emulator runs 150–290× slower than a real NES console, highlighting the current compute inefficiency of LLM‑driven hardware emulation.

hackernews · dbreunig · Oct 30, 16:40 · [Discussion](https://news.ycombinator.com/item?id=50306442)

**「Background」** The project builds on earlier LLM‑driven emulation work such as Qwenputer, which demonstrated using a Qwen model to emulate a simple CPU, and extends that concept to emulate a full Nintendo Entertainment System—including both the CPU and RAM—within a ~1 GB model, representing a new approach to hardware emulation using large language models.

**「Impact」** The project demonstrates that while LLMs can be coaxed into functional hardware emulation, the resulting system is orders of magnitude slower and more compute‑intensive than traditional deterministic programs, setting realistic expectations for AI‑based emulation approaches.

**「Community discussion」** Commenters highlighted the novelty of the two‑prompt generation \(dbreunig\), suggested embedding a VM inside the model weights for internal tool execution \(armcat\), and emphasized the severe performance penalty, noting the 150–290× slowdown \(pbohun, jacquesm\).

**Tags**: `#LLM`, `#NES emulation`, `#Open source`, `#AI research`, `#Hardware`

---

<a id="item-tech-news-3"></a>
### [Signoz newsletter: AI deskilling erodes SRE understanding](https://newsletter.signoz.io/p/ai-isnt-replacing-sres-its-deskilling) ⭐️ 8.0/10

The Signoz newsletter argues that AI tools are eroding the deep system understanding essential to Site Reliability Engineering, framing the effect as deskilling rather than replacement. It draws on safety-critical systems thinking and resonated with practitioners, sparking extensive debate on automation&\#x27;s impact on SRE roles. The piece does not claim AI will replace SREs outright, but warns of gradual skill erosion in complex incident management.

hackernews · dorianniemiec · Oct 30, 15:52 · [Discussion](https://news.ycombinator.com/item?id=50305693)

**「SRE expertise and automation deskilling」** Site Reliability Engineering \(SRE\) depends on engineers maintaining deep, hands-on understanding of production systems—data flow, application architecture, logs, and failure modes—so they can diagnose and restore service during incidents. The concern that automation can erode that expertise, known as deskilling, has been documented in other safety-critical fields, including medicine and aviation, where reliance on autopilot has been associated with atrophied manual flying skills.

**「Impact」** SREs may gradually lose the deep system understanding needed to resolve complex incidents independently, as AI handles more routine tasks, creating a dependency risk for organizations relying on sustained operational expertise.

**「Community Discussion」** Commenters widely echoed the deskilling concern, with one noting that designating AI-handled incidents as human practice opportunities mirrors aviation&\#x27;s mandatory manual flying time to preserve pilot skills. Others argued AI is simply a productivity tool, but the dominant view highlighted erosion of fundamental SRE competencies.

<details><summary>References</summary>
<ul>
<li><a href="https://link.springer.com/article/10.1007/s10462-025-11352-1">AI -induced Deskilling in Medicine: A Mixed-Method Review and...</a></li>
<li><a href="https://www.businessinsider.com/avoid-ai-deskilling-pilots-autopilot-2026-10">Want to Avoid AI Deskilling ? Pilots May Have the... - Business Insider</a></li>

</ul>
</details>

**Tags**: `#SRE`, `#AI-impact`, `#deskilling`, `#observability`, `#platform-engineering`

---

<a id="item-tech-news-4"></a>
### [Backdoor in Claude Code for VS Code extension on the Cursor Marketplace](https://phorion.io/blog/offical-claude-code-vsx-compromise/) ⭐️ 7.0/10

A malicious actor tampered with the Claude Code extension on the Cursor marketplace, adding an attacker&\#x27;s SSH key to users&\#x27; authorized\_keys, while Anthropic&\#x27;s systems remained unaffected.

hackernews · \_chall · Oct 30, 07:09 · [Discussion](https://news.ycombinator.com/item?id=50300683)

**Tags**: `#security`, `#supply-chain-attack`, `#AI-coding`, `#VSCode`, `#Cursor`

---

<a id="item-tech-news-5"></a>
### [Northflank Breached](https://status.northflank.com/) ⭐️ 7.0/10

A Northflank breach triggers Hacker News discussion on recurring multi-tenant SaaS security incidents and potential industry shifts toward hyperscalers.

hackernews · js4ever · Oct 30, 15:10 · [Discussion](https://news.ycombinator.com/item?id=50305025)

**Tags**: `#security`, `#saas`, `#devops`, `#multi-tenant`, `#cloud infrastructure`

---

<a id="item-tech-news-6"></a>
### [The $6.3B Binance hack was pulled off in just 20 minutes](https://www.wired.com/story/the-dollar63-billion-binance-hack-was-pulled-off-in-just-20-minutes/) ⭐️ 7.0/10

A reported $6.3 billion Binance hack is claimed to have been executed in just 20 minutes, prompting discussion on exploit preparation, execution speed, and potential supply-chain AI tool connections.

hackernews · domhudson · Oct 30, 12:50 · [Discussion](https://news.ycombinator.com/item?id=50303172)

**Tags**: `#supply-chain-attack`, `#software-exploitation`, `#crypto-security`, `#ai-code-generation`, `#industry-impact`

---

<a id="item-tech-news-7"></a>
### [Soft-MTP: One-Line Fix Improves Multi-Token Prediction](https://www.reddit.com/r/MachineLearning/comments/1xjnz40/multitoken_prediction_done_right_r/) ⭐️ 7.0/10

The paper presents Soft-MTP, a one‑line code change \(h\_ntp += h\_mtp.detach\(\) - h\_mtp\) that recovers the KL self‑distillation gradient hidden in standard Multi‑Token Prediction. This simple fix yields measurable performance improvements across a range of pre‑training tasks, effectively providing a &quot;free lunch&quot; for LLM researchers and engineers.

reddit · r/MachineLearning · /u/jayden\_teoh\_ · Oct 30, 18:53

**「Background」** Multi-token prediction \(MTP\) is a standard recipe in large language model pre-training that adds auxiliary heads to predict multiple future tokens, improving sample efficiency and enabling speculative decoding. The standard MTP gradient, however, contains a noisy residual that hides a beneficial KL self-distillation signal. The paper identifies this hidden KL gradient and proposes a one-line code modification to recover it, yielding performance gains across tasks.

**「Impact」** Developers can add the single line to their training code to obtain better model quality and more reliable speculative decoding without additional compute, directly benefiting researchers and engineering teams.

**Tags**: `#multi-token prediction`, `#large language models`, `#machine learning`, `#pre-training`, `#speculative decoding`

---

<a id="item-tech-news-8"></a>
### [美 FCC 拟禁止中国三大运营商直接获取美国号码资源](https://fccid.io/news/fcc-draft-national-security-voip-direct-access-numbering-rules) ⭐️ 7.0/10

The US FCC is proposing to ban Chinese mobile operators \(China Mobile, China Telecom, China Unicom\) and VoIP service providers from directly accessing US phone number resources, citing national security and fraud prevention concerns, with a decision expected on November 19, 2024.

telegram · zaihuapd · Oct 30, 08:01

**Tags**: `#FCC`, `#telecommunications`, `#national-security`, `#Chinese-telecom`, `#VoIP-regulation`

---

<a id="item-tech-news-9"></a>
### [Cursor 扩展市场 OpenVSX 中 Claude Code 插件被投毒](https://cursor.com/blog/claude-code-extension-security-notice) ⭐️ 7.0/10

A compromised Claude Code extension in the OpenVSX marketplace attempted to install SSH backdoors and collect host data before being removed by Cursor.

telegram · zaihuapd · Oct 30, 08:44

**Tags**: `#security`, `#software supply chain`, `#AI coding tools`, `#VS Code extensions`

---

## Financial News

<a id="item-finance-news-1"></a>
### [DeepSeek raises 10.55 billion RMB in second funding round](https://www.theinformation.com/articles/behind-deepseeks-16-billion-funding-chinese-tech-titans-state-players) ⭐️ 8.0/10

Chinese AI startup DeepSeek has raised 10.55 billion RMB in a second round of financing, bringing its valuation above 61.55 billion RMB. Nearly 30 investors participated in the round, including Tencent, CATL, SMIC, Meituan, vivo, and Xiaohongshu.

telegram · zaihuapd · Oct 30, 12:37

**「Background」** This follows DeepSeek&\#x27;s first funding round of approximately 5.1 billion RMB completed in June 2026, with state-backed investors now accounting for about 27% of total capital, up from just 2% in the first round.

**Tags**: `#AI`, `#Funding`, `#Investors`, `#China Tech`, `#DeepSeek`

---

<a id="item-finance-news-2"></a>
### [US Semiconductor Stocks Plunge, Intel Drops Over 26%](https://www.cls.cn/detail/2521210) ⭐️ 8.0/10

On October 30, US semiconductor stocks fell sharply, with the Philadelphia Semiconductor Index dropping 5.67% and Intel shares plunging over 26%, while AMD fell more than 10%, SanDisk declined 8.38%, and Nvidia slipped 2.51%.

telegram · zaihuapd · Oct 30, 13:48

**「Philadelphia Semiconductor Index background」** The Philadelphia Semiconductor Index \(SOX\) tracks major chip makers, with Intel as a top component, so its 5.67% drop reflects a broad sell‑off in the sector.

<details><summary>References</summary>
<ul>
<li><a href="https://www.investing.com/indices/phlx-semiconductor-components">Philadelphia Semiconductor Index Companies Stock List ...</a></li>
<li><a href="https://indexes.nasdaqomx.com/Index/Overview/SOX">Overview for SOX - Nasdaq PHLX Semiconductor (^SOX) Components - Yahoo Finance PHLX Semiconductor Sector Index - Nasdaq SOX Index | Components, Quotes &amp; Sectors PHLX SOX · PHLX Semiconductor Index Constituent Breakdown by ... Philadelphia Semiconductor Index Components – NASDAQ:SOX ...</a></li>
<li><a href="https://finance.yahoo.com/quote/%5ESOX/components/?fr=sycsrp_catchall">PHLX Semiconductor (^SOX) Components - Yahoo Finance</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#Intel`, `#earnings`, `#market-move`, `#Philadelphia Semiconductor Index`

---

<a id="item-finance-news-3"></a>
### [📱 苹果下调中国台湾地区 App Store 交易佣金费率，由 30% 降至 26%](https://developer.apple.com/news/?id=w9mxlhek) ⭐️ 7.0/10

Apple reduces App Store commission in its Taiwan region from 30% to 26%, effective Oct 31 2026, after discussions with local regulators.

telegram · zaihuapd · Oct 30, 09:25

**Tags**: `#Apple`, `#App Store`, `#Developer Economics`, `#Regulatory Change`

---

<a id="item-finance-news-4"></a>
### [Four Japanese automakers&\#x27; China production falls below 40% of 2020 peak](https://weibo.com/1642634100/Rp6qUwLKa) ⭐️ 7.0/10

Japanese automakers&\#x27; China production dropped to about 1.02 million vehicles in April‑September 2026, a 32% year‑over‑year decline and less than 40% of the 2020 peak, while Honda announced a cut of its fuel‑car capacity in China from 1.49 million to 1.00 million units.

telegram · zaihuapd · Oct 30, 13:38

**「Background」** The 2020 peak of roughly 2.55 million vehicles set the benchmark for the four automakers&\#x27; China output.

**「Impact」** The capacity cuts may pressure Honda&\#x27;s Chinese sales and strain its supply chain, affecting investors and the broader Chinese auto industry.

**Tags**: `#Automotive`, `#China`, `#Production`, `#Japanese automakers`, `#Capacity cuts`

---