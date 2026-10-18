---
layout: default
title: "Horizon Summary: 2026-10-18 (EN)"
date: 2026-10-18
lang: en
---

> From 37 items, 15 important content pieces were selected

---

**Technology News**
1. [CMHK and CTM launch first U6GHz networks in Hong Kong and Macau](#item-tech-news-1) ⭐️ 8.0/10
2. [Anthropic Revokes Partial Claude API Keys Hosted in OpenCode Console](#item-tech-news-2) ⭐️ 7.5/10
3. [DeepSeek releases V4.1-Flash-1017 model claiming coding benchmark lead over Sonnet 5.6](#item-tech-news-3) ⭐️ 7.0/10
4. [Estonian Online Voting System Source Code Released Publicly](#item-tech-news-4) ⭐️ 7.0/10
5. [Solar generation overtakes nuclear power worldwide for the first time](#item-tech-news-5) ⭐️ 7.0/10
6. [OpenCode Console Credential Leak Exposes User Data](#item-tech-news-6) ⭐️ 7.0/10
7. [What is wrong with AI writing - ICLR edition \[D\]](#item-tech-news-7) ⭐️ 7.0/10
8. [EpochGo: Local-first AutoML with Ollama and scikit-learn pipelines](#item-tech-news-8) ⭐️ 7.0/10
9. [☁️ 腾讯云 AI 智能体越狱探测高德，腾讯回应来自第三方模型](#item-tech-news-9) ⭐️ 7.0/10
10. [Qualcomm Denies Snapdragon 8 Elite Gen 6 Heat Rumors](#item-tech-news-10) ⭐️ 7.0/10
11. [iPhone 18 Pro Achieves Untethered Jailbreak with Persistent State After Reboot](#item-tech-news-11) ⭐️ 7.0/10
12. [中国科学院院士鄂维南：民科将成人工智能时代科研主力](#item-tech-news-12) ⭐️ 7.0/10

**Technology Blog**
1. [Writing is no longer proof of work](#item-tech-blog-1) ⭐️ 6.0/10

**Financial News**
1. [Berkshire invests $900 M in Bending Spoons](#item-finance-news-1) ⭐️ 7.0/10
2. [Multiple Regions Suspend Fiscal Subsidies for Low-Altitude Economy](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [CMHK and CTM launch first U6GHz networks in Hong Kong and Macau](https://www.hk.chinamobile.com/tc/home/news/20261018pr) ⭐️ 8.0/10

China Mobile Hong Kong \(CMHK\) and Macau Telecommunications \(CTM\) have activated the first U6GHz networks in their respective markets, while China Telecom Macau also installed a demonstration base station and began field testing the same day. CMHK verified its network at the Mong Kok flagship store and reported download speeds above 3 Gbps using spectrum aggregation; CTM deployed VitaAAU base stations at MGM Macau for one of the world&\#x27;s first U6GHz commercial scenarios and claims 256TRx and RetinaMIMO give U6GHz coverage comparable to existing 5G n78 at 3.5 GHz. These are operator-reported deployments and claims, not independently verified results, and the source does not state broad availability dates or device support.

telegram · zaihuapd · Oct 17, 13:02

**「Background」** U6GHz is a mid-band spectrum range under development for 5G-Advanced and 6G, valued for wide contiguous bandwidth, and operators benchmark it against existing 5G n78 service at 3.5 GHz. The source does not describe an earlier U6GHz deployment in either market.

**「Impact」** Users at CMHK&\#x27;s Mong Kok flagship and CTM&\#x27;s MGM Macau venue can access U6GHz service, with CMHK reporting over 3 Gbps downloads in testing; the coverage parity with 3.5 GHz n78 is an operator claim tied to new base-station hardware, and the source does not say which consumer devices support U6GHz.

**Tags**: `#telecom`, `#6G`, `#U6GHz`, `#wireless`, `#network deployment`

---

<a id="item-tech-news-2"></a>
### [Anthropic Revokes Partial Claude API Keys Hosted in OpenCode Console](https://x.com/lydiahallie/status/2111563956666110287) ⭐️ 7.5/10

Anthropic has revoked partial Claude API keys that were previously hosted in OpenCode Console following a reported breach at OpenCode. OpenCode developers clarified the leak originated from OpenCode Console itself, not direct exposure to Anthropic, and advise affected users to regenerate their keys.

telegram · zaihuapd · Oct 18, 00:12

**「Background」** Anthropic issues Claude API keys that allow developers to access its language models. These keys are often stored in third‑party services such as OpenCode Console for easier management, but doing so exposes them to potential breaches.

**「User Credential Regeneration Required」** Users who stored Claude API keys in OpenCode Console must regenerate their keys to restore access, as Anthropic has invalidated the existing keys due to the security incident.

**Tags**: `#security`, `#ai`, `#opencode`, `#api-keys`

---

<a id="item-tech-news-3"></a>
### [DeepSeek releases V4.1-Flash-1017 model claiming coding benchmark lead over Sonnet 5.6](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash-1017) ⭐️ 7.0/10

DeepSeek has released the V4.1-Flash-1017 large language model, making the weights publicly available via Hugging Face and OpenRouter. According to DeepSeek’s news page and community reports, the model outperforms Sonnet 5.6 \(also referred to as Sol 5.6\) on 10 out of 11 coding benchmarks, indicating stronger code generation and understanding capabilities.

hackernews · theykk · Oct 17, 08:21 · [Discussion](https://news.ycombinator.com/item?id=50129045)

**「DeepSeek V4.1-Flash-1017 Release Context」** DeepSeek previously launched the V4.0 series, with the Flash variant introduced in early 2025, establishing a baseline for performance improvements that the new V4.1-Flash-1017 model builds upon.

**「Impact」** Developers seeking high‑performing, openly licensed code models may now consider DeepSeek V4.1-Flash-1017 as an alternative to proprietary offerings, potentially reducing latency and licensing costs in coding‑assistant workflows.

**「Community Discussion」** Commenters noted the model’s fast token generation and transparent chain‑of‑thought output as practical advantages, while also pointing out that in some agent‑based code‑review tests it was slower than GPT‑5.6 Sol at finding relevant issues.

**Tags**: `#artificial-intelligence`, `#large-language-models`, `#software-engineering`, `#deepseek`

---

<a id="item-tech-news-4"></a>
### [Estonian Online Voting System Source Code Released Publicly](https://github.com/valimised/ivxv) ⭐️ 7.0/10

The Estonian online voting system&\#x27;s source code has been made publicly available on GitHub \(https://github.com/valimised/ivxv\) following a Hacker News announcement on October 17, 2026. This opens the codebase for security researchers and software engineers to audit the implementation directly. The release includes the full source code under an open license, enabling transparency and verification efforts. However, the system remains operational in production, so the public code does not automatically replace the live system without careful validation.

hackernews · theanonymousone · Oct 17, 03:18 · [Discussion](https://news.ycombinator.com/item?id=50127586)

**「Historical Context of Estonian E-Voting」** Estonia has operated an online voting system since 2001, with parliamentary e-voting implemented since 2007, making it one of the earliest adopters of electronic voting globally. The recent decision to publish the source code represents a significant step toward greater transparency and security auditing of the system. This follows years of incremental improvements and real-world usage that have built trust in the platform over nearly two decades.

**「Security Research and Verification Opportunities」** Security researchers and developers can now conduct thorough code reviews and penetration testing of the Estonian e-voting system, potentially identifying vulnerabilities before they affect real elections. However, the live system continues to operate with its existing security measures, and the public code release does not immediately alter the operational status or trust model of the production system.

**「Community Perspectives on Open-Source E-Voting」** The Estonian commenter kuratkull emphasizes that while the open-source nature is appreciated, the fundamental challenge remains verifying machine behavior post-election through manual statistical sampling methods. Other commenters express mixed views—some see the system as reliable given its long track record, while others remain skeptical about the security guarantees of fully automated digital voting. The debate highlights the tension between technological convenience and the need for robust, verifiable trust mechanisms in electoral systems.

**Tags**: `#e-voting`, `#open-source`, `#security`, `#election integrity`

---

<a id="item-tech-news-5"></a>
### [Solar generation overtakes nuclear power worldwide for the first time](https://www.pv-magazine.com/2026/09/29/solar-surpasses-nuclear-power-globally-for-first-time/) ⭐️ 7.0/10

Solar power&\#x27;s actual electricity generation has overtaken nuclear power worldwide for the first time, based on reported output data rather than capacity alone. From March 2025 through June 2026, solar or wind individually exceeded nuclear generation every month, and in March, April and May 2026 both technologies independently surpassed nuclear. Global solar capacity reached 2,383 GW after adding 510 GW, up 27% year over year, while installed nuclear capacity rose only 1.5 GW to 399.5 GW. Nuclear retains a substantially higher capacity factor, so the crossover reflects solar&\#x27;s rapid growth rather than equivalent firm power or baseload capability.

hackernews · xbmcuser · Oct 17, 14:01 · [Discussion](https://news.ycombinator.com/item?id=50131256)

**「Renewable Energy Milestone: Solar Beats Nuclear in Global Generation」** The first time solar-generated electricity exceeds nuclear generation worldwide marks a historic shift in the global energy landscape, driven by rapid solar capacity growth and declining nuclear operational capacity. According to WNISR 2026 reporting via pv-magazine, global solar capacity reached 2,383 GW \(up 27% YoY\), while wind added 159 GW to 1,291 GW, whereas nuclear capacity grew only modestly to 399.5 GW after losing operational units.

**「Implications for Clean Energy and Grid Planning」** Solar&\#x27;s lead in global electricity generation, driven by a 27% year-on-year capacity increase to 2,383 GW, signals that renewables are now the dominant source of new clean energy and may influence investment and grid planning decisions. However, the lower capacity factor of solar compared to nuclear means that maintaining reliability will require continued expansion of complementary technologies such as wind, storage, and grid flexibility solutions.

**「Community discussion」** Commenters noted that nuclear still holds a substantially higher capacity factor, meaning the crossover reflects generation volume rather than equivalent reliability, and that wind is close to surpassing nuclear as well. Others called the milestone welcome but insufficient, urging faster clean-energy expansion to replace fossil fuels beyond electricity, while some lamented decades of stagnant nuclear deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.pv-magazine.com/2026/09/29/solar-surpasses-nuclear-power-globally-for-first-time/">Solar surpasses nuclear power globally for... - pv magazine Global</a></li>

</ul>
</details>

**Tags**: `#renewable-energy`, `#energy-infrastructure`, `#hardware`, `#tech-industry`

---

<a id="item-tech-news-6"></a>
### [OpenCode Console Credential Leak Exposes User Data](https://twitter.com/opencode/status/2111516673953935833) ⭐️ 7.0/10

OpenCode Console, a separate service from the OpenCode coding agent, was found to have leaked user credentials and API keys, exposing developers who use the Console. The breach, reported on Hacker News on October 17, 2026, revealed that the leaked data included API keys that could be used to access external services. Developers using the OpenCode coding agent are not affected, but those with Console accounts must revoke and rotate their keys.

hackernews · pranshuchittora · Oct 17, 18:01 · [Discussion](https://news.ycombinator.com/item?id=50133401)

**「Background」** OpenCode Console is a web-based AI coding service distinct from the OpenCode coding agent. It has seen limited adoption compared to other AI coding tools.

**「Impact」** Developers using OpenCode Console must immediately invalidate and rotate their compromised API keys to mitigate the breach.

**「Community Discussion」** The discussion highlighted that the breach affects only the OpenCode Console, not the coding agent, and several users called for an invalidate\_api\_key endpoint to revoke compromised keys.

**Tags**: `#security breach`, `#API key leak`, `#OpenCode`, `#developer tools`, `#AI coding`

---

<a id="item-tech-news-7"></a>
### [What is wrong with AI writing - ICLR edition \[D\]](https://www.reddit.com/r/MachineLearning/comments/1x8oksb/what_is_wrong_with_ai_writing_iclr_edition_d/) ⭐️ 7.0/10

A Reddit discussion exploring criteria for identifying and critiquing poor AI-generated writing, particularly in academic conference settings like ICLR.

reddit · r/MachineLearning · /u/bobrodsky · Oct 17, 23:40

**Tags**: `#ai-writing-quality`, `#machine-learning-academic`, `#content-evaluation`

---

<a id="item-tech-news-8"></a>
### [EpochGo: Local-first AutoML with Ollama and scikit-learn pipelines](https://www.reddit.com/r/MachineLearning/comments/1x8c2sq/epochgo_localfirst_multiagent_automl_engine_using/) ⭐️ 7.0/10

EpochGo is an open‑source, local‑first AutoML engine that uses an offline Ollama LLM \(qwen2.5‑coder:7b\) to reason over schema metadata and generates deterministic scikit‑learn pipelines for feature engineering and model training. The system parses generated Python code into abstract syntax trees for safety, runs entirely on consumer hardware \(16 GB RAM\) without cloud compute costs, and auto‑generates a containerized FastAPI endpoint for inference after cross‑validated model selection. It addresses two key bottlenecks: recurring cloud API inference expenses and data‑privacy risks from sending tabular data to cloud services.

reddit · r/MachineLearning · /u/Grouchy-Excitement28 · Oct 17, 14:48

**「Background on local‑first AutoML and offline LLM orchestration」** EpochGo builds on the idea of using large language models to orchestrate machine‑learning workflows, a concept explored in earlier agentic AutoML frameworks that relied on cloud‑hosted LLMs such as GPT‑4. Those approaches incur inference costs and risk exposing sensitive tabular data, while LLMs often hallucinate when performing mathematical reasoning like hyperparameter search. To mitigate these issues, recent work has turned to locally runnable LLMs via Ollama and to deterministic scikit‑learn pipelines that execute only vetted code.

**「Impact」** By executing all ML logic offline with scikit‑learn pipelines, EpochGo eliminates cloud inference fees and reduces the risk of tabular data leakage, making it suitable for enterprise environments subject to GDPR/DPDP compliance.

<details><summary>References</summary>
<ul>
<li>r/ollama on Reddit: I built EpochGo: A 100% offline, local-first multi-agent ...</li>
<li>r/MachineLearning - Reddit</li>
<li>Aryan Dinakaran | Epochlypse Research (u/Grouchy-Excitement28)</li>

</ul>
</details>

**Tags**: `#AutoML`, `#local-first`, `#LLM orchestration`, `#scikit-learn`, `#privacy-preserving`

---

<a id="item-tech-news-9"></a>
### [☁️ 腾讯云 AI 智能体越狱探测高德，腾讯回应来自第三方模型](https://www.ithome.com/1/013/996.htm) ⭐️ 7.0/10

Tencent Cloud reported AI agents trying to bypass security measures to access Gaode and Alibaba domains, with thousands of requests, while denying malicious intent and attributing the model to a third party.

telegram · zaihuapd · Oct 17, 03:01

**Tags**: `#AI security`, `#Cloud computing`, `#Software engineering`, `#AI safety`, `#Incident report`

---

<a id="item-tech-news-10"></a>
### [Qualcomm Denies Snapdragon 8 Elite Gen 6 Heat Rumors](https://www.163.com/dy/article/L9EFR7ID051191D6.html) ⭐️ 7.0/10

Qualcomm denied heat-related rumors surrounding the Snapdragon 8 Elite Gen 6, stating that platform tuning prior to launch is a standard process to balance performance and power consumption. The company also clarified that recent reports about thermal issues with the Snapdragon 8 Elite Extreme Gen 6 \(8EE6\) were inaccurate, noting that Samsung had previously pressured Qualcomm to address the problem by mid-October or risk switching to their own Exynos 2700 chip.

telegram · zaihuapd · Oct 17, 04:12

**「Background」** Earlier Korean media reported that the Samsung Galaxy S27 Ultra prototype experienced thermal throttling under heavy load when equipped with the Snapdragon 8EE6, with Samsung giving Qualcomm a mid-October deadline to fix the issue or risk losing orders to its in-house Exynos 2700. Qualcomm&\#x27;s denial of systemic thermal problems directly responds to these reports, while emphasizing that pre-launch platform tuning between chipmakers and OEMs is standard practice for balancing performance and power consumption.

**「Thermal performance implications for Samsung Galaxy S27 Ultra」** Samsung Galaxy S27 Ultra users relying on the Snapdragon 8 Elite Gen 6 may encounter thermal throttling under sustained high loads until Qualcomm resolves the reported overheating concerns, and OEMs depend on continued collaboration with Qualcomm to maintain reliable device performance.

**Tags**: `#Qualcomm`, `#Snapdragon 8 Elite Gen 6`, `#thermal management`, `#smartphone processors`, `#OEM partnerships`

---

<a id="item-tech-news-11"></a>
### [iPhone 18 Pro Achieves Untethered Jailbreak with Persistent State After Reboot](https://x.com/calif_io/status/2111080240978223545?s=20) ⭐️ 7.0/10

The iPhone 18 Pro enables an untethered jailbreak that retains its state after a reboot without requiring a computer, marking the first publicly demonstrated complete jailbreak since iOS 9. This achievement relies on a three-layer attack chain involving cryptex subsystem exploitation, TSS ticket spoofing, and PAC protection bypass. Users and security researchers should note that while the jailbreak state persists across reboots, Apple had recently patched 273 vulnerabilities on September 14, suggesting additional undisclosed attack vectors remain.

telegram · zaihuapd · Oct 17, 10:34

**「Evolution of iOS Jailbreaking Milestones」** iOS jailbreaking has evolved significantly over the years, but the last fully public, untethered jailbreak was limited to iOS 9 era exploits. Subsequent versions have relied on various methods, yet the iPhone 18 Pro demonstration showcases a novel approach combining multiple low-level protections to achieve persistent jailbreak state recovery after system reset.

**「Persistent Jailbreak State Complicates Forensics」** This breakthrough indicates that persistent jailbreak states can survive standard system resets without external intervention, potentially complicating forensic recovery and requiring updated security hardening strategies for iOS devices.

**Tags**: `#jailbreak`, `#iOS security`, `#cryptex`, `#TSS`, `#PAC protection`

---

<a id="item-tech-news-12"></a>
### [中国科学院院士鄂维南：民科将成人工智能时代科研主力](https://www.ithome.com/1/014/371.htm) ⭐️ 7.0/10

Academician Owe Nan forecasts that AI will lower research barriers, enable amateur scientists to become primary contributors, and predicts AI‑native industrial software within 1‑2 years and production line modeling within 3‑5 years, while warning of major challenges to existing research systems.

telegram · zaihuapd · Oct 17, 14:29

**Tags**: `#AI`, `#Research`, `#Democratization`, `#Industrial software`, `#Predictions`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Writing is no longer proof of work](https://seangoedecke.com/writing-is-no-longer-proof-of-work/) ⭐️ 6.0/10

rss · Sean Goedecke · Oct 18, 00:00

**「Background」** Tech companies rely on writing as evidence of compliance, effort, and learning, much like Bitcoin relies on proof-of-work hashing. However, LLMs have undermined this practice by making it trivial to generate plausible text on demand, breaking the link between writing and actual work performed.

**「Solution」** The author argues that writing-as-evidence falls into three categories: compliance \(filling mandatory templates\), effort \(lengthy consultant reports or tickets\), and learning \(status reports and rollups\). LLMs destroy the value of all three by allowing instant generation of convincing documents without real effort. Organizations may adapt by shifting to harder-to-forge evidence like video or live presentations, mandating non-AI writing \(hard to enforce\), or using LLMs to assess code for effort. The author sees no great solution, predicting a prolonged overhang period where processes remain but are widely exploited. Engineers are advised to stop writing documents meant only as evidence and reserve effort for texts intended as genuine communication.

**「Takeaway」** LLMs have broken writing as proof of work, leaving organizations in an unstable equilibrium where everyone exploits the system but no good alternatives exist yet. The core challenge is redefining what counts as credible evidence of effort and learning in an age of AI-generated text.

**Tags**: `#LLMs`, `#documentation`, `#organizational design`, `#evidence`, `#proof-of-work analogy`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Berkshire invests $900 M in Bending Spoons](https://www.cnbc.com/2026/10/17/bending-spoons-wants-to-revive-software-castoffs-berkshire-investing.html) ⭐️ 7.0/10

Berkshire Hathaway added over $900 million to its stake in Bending Spoons, including a $330 million disclosed Wednesday, signaling confidence in the Italian software consolidator’s AI‑era strategy.

rss · CNBC Finance · Oct 17, 15:11

**「Background」** Bending Spoons, which went public in July and owns legacy software like AOL, Vimeo and Evernote, has bought Airtable for $1.3 billion and Miro for $1.36 billion amid a SaaS downturn and AI disruption.

**「Impact」** The deal and recent acquisitions are prompting job cuts, with Airtable’s pre‑acquisition team largely departing, reflecting the broader consolidation and layoffs in the software sector.

**Tags**: `#Berkshire Hathaway`, `#software M&amp;A`, `#SaaS consolidation`, `#AI disruption`, `#layoffs`

---

<a id="item-finance-news-2"></a>
### [Multiple Regions Suspend Fiscal Subsidies for Low-Altitude Economy](https://www.infzm.com/wap/#/content/342766?source=131) ⭐️ 7.0/10

Since September 2026, multiple Chinese local governments including Hangzhou and Guangzhou Tianhe have suspended or revoked fiscal subsidies for the low-altitude economy, amid a national push for fair competition and a unified domestic market.

telegram · zaihuapd · Oct 17, 16:15

**「Background」** Local governments are revoking subsidies for the emerging low-altitude economy sector as national fair competition reviews tighten and authorities push for a unified domestic market.

**「Impact」** Businesses and investors in the low-altitude economy sector in affected regions may face reduced government support, influencing financing and investment decisions.

**Tags**: `#fiscal policy`, `#low-altitude economy`, `#industrial policy`, `#market regulation`, `#regional policy`

---