---
layout: default
title: "Horizon Summary: 2026-11-06 (EN)"
date: 2026-11-06
lang: en
---

> From 51 items, 19 important content pieces were selected

---

**Technology News**
1. [Claude Code sends your email address to websites](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenSSH Password Authentication Bypass on Alpine](#item-tech-news-2) ⭐️ 8.0/10
3. [600,000 NVIDIA H200 chips stuck in Hong Kong awaiting China import approval](#item-tech-news-3) ⭐️ 8.0/10
4. [Hugging Face releases MoE training handbook for Megatron-LM](#item-tech-news-4) ⭐️ 7.0/10
5. [Publication expectations for ML PhDs at top US schools](#item-tech-news-5) ⭐️ 7.0/10
6. [DialFork benchmark released to measure procedural hallucination in conversational agents](#item-tech-news-6) ⭐️ 7.0/10
7. [Microsoft Says Windows 11 High Memory Use Is Fine](#item-tech-news-7) ⭐️ 7.0/10
8. [中国叫停软银 54 亿美元收购 ABB 机器人业务](#item-tech-news-8) ⭐️ 7.0/10
9. [Huawei Cloud openPangu-2.1-Pro launches November 15, enhances ArkTS code generation](#item-tech-news-9) ⭐️ 7.0/10
10. [DeepSeek Harness reaches 1.54 million daily active users with over 35,000 plugins](#item-tech-news-10) ⭐️ 7.0/10
11. [Google Releases Gemini Omni 1.2 Flash Video Model](#item-tech-news-11) ⭐️ 7.0/10
12. [India Announces 24-Month Plan for Homegrown GPU and RISC-V SHAKTI/VEGA Commercialization](#item-tech-news-12) ⭐️ 7.0/10

**Technology Blog**
1. [A database is a store for global variables](#item-tech-blog-1) ⭐️ 7.0/10

**Financial News**
1. [Democrats Urge AI Data Center Moratorium After Midterms](#item-finance-news-1) ⭐️ 8.0/10
2. [Barkin signals further gradual rate hikes](#item-finance-news-2) ⭐️ 7.0/10
3. [Premarket Stock Movers: Unity Software Surges, Qualcomm Falls, Wendy&\#x27;s Rejects Takeover](#item-finance-news-3) ⭐️ 7.0/10
4. [Micron pauses $4.5 billion Taiwan DRAM plant over labor dispute](#item-finance-news-4) ⭐️ 7.0/10
5. [Switch 2 sales decline and earnings miss](#item-finance-news-5) ⭐️ 7.0/10
6. [Chip Stock Sell-Off Intensifies, Nasdaq 100 Drops 5%](#item-finance-news-6) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Claude Code sends your email address to websites](https://github.com/anthropics/claude-code/issues/107757) ⭐️ 8.0/10

Claude Code inadvertently includes users&\#x27; email addresses in request headers, exposing them to spam and privacy breaches.

hackernews · motoroco · Nov 5, 22:17 · [Discussion](https://news.ycombinator.com/item?id=50385272)

**Tags**: `#privacy`, `#AI tools`, `#security`, `#software engineering`

---

<a id="item-tech-news-2"></a>
### [OpenSSH Password Authentication Bypass on Alpine](https://alpinelinux.org/posts/2026-11-05-openssh-password-authentication-bypass/) ⭐️ 8.0/10

Alpine Linux published a security advisory describing a password-authentication bypass in OpenSSH. The advisory centered on musl&\#x27;s crypt\(\) function returning the wildcard string &\#x27;\*&\#x27; as an error indicator when a key is over 256 bytes, and the discussion noted that this value could match stored fields for accounts without passwords. The incident prompted broader discussion about C library design and error handling.

hackernews · pantalaimon · Nov 5, 14:44 · [Discussion](https://news.ycombinator.com/item?id=50379704)

**「Background」** Since August 29, 2012, musl libc&\#x27;s crypt\(\) function has returned the string &quot;\*&quot; as an error indicator when the input key exceeds 256 bytes for SHA-256 and SHA-512 hashing, and this same &quot;\*&quot; string is what Alpine Linux stores in the password field for every account with no password set. When OpenSSH on Alpine \(which uses musl libc\) operates without PAM, it compares the crypt\(\) output against this stored field, so the error sentinel matches the locked-account placeholder and the login succeeds. Testing of 17,600 login attempts against six sshd builds confirmed that only musl-based builds without PAM accepted entries they should have rejected.

**「Impact」** The affected behavior could lead to password-based authentication bypass in Alpine Linux OpenSSH deployments. The discussion mentioned disabling password logins, such as setting PasswordAuthentication no and restarting sshd, as a mitigation. It also raised broader concerns about C error handling and authentication design.

**「Community Discussion」** Commenters debated why musl&\#x27;s crypt\(\) uses &\#x27;\*&\#x27; as an error indicator and whether other C libraries behave similarly, with some criticism of the design. Others argued that Rust&\#x27;s Result-based error handling is safer than C patterns using sentinels or null pointers, and one commenter linked an earlier Hacker News discussion.

<details><summary>References</summary>
<ul>
<li><a href="https://elsolitario.org/en/2026/11/05/musl-report-finds-asterisk-that-opens-ssh-accounts/">Musl libc: Report Reveals Bug Affecting OpenSSH</a></li>
<li><a href="https://hadrian.io/vulnerability-alerts/openssh-on-musl-accepts-any-long-password-for-locked-accounts">From * to Access: How musl’s crypt () Behavior Undermines ...</a></li>
<li><a href="https://daily.dev/posts/openssh-on-musl-linux-without-pam-can-accept-logins-it-should-reject-nmuhpvoh8">OpenSSH on musl Linux without PAM can accept logins it...</a></li>

</ul>
</details>

**Tags**: `#security`, `#OpenSSH`, `#Alpine Linux`, `#musl`, `#vulnerability`

---

<a id="item-tech-news-3"></a>
### [600,000 NVIDIA H200 chips stuck in Hong Kong awaiting China import approval](https://www.reuters.com/world/china/nvidia-chips-pile-up-hong-kong-china-withholds-import-approval-2026-11-05/) ⭐️ 8.0/10

Around 600,000 NVIDIA H200 AI chips are stockpiled in Hong Kong awaiting Beijing&\#x27;s approval for large-scale import to mainland China, according to people familiar with the matter cited by Reuters. Only a few Chinese internet companies have received roughly 10,000 chips each in recent months, with small volumes entering through intermediaries and indirect channels. H200 servers in mainland China were quoted at over 6 million yuan for an eight-card configuration at the end of October, about triple the price from a year earlier, although the H200 is not NVIDIA&\#x27;s newest model.

telegram · zaihuapd · Nov 5, 14:42

**「Background」** Since mid‑2026, Beijing has permitted a conditional H200 import pathway under revised U.S. export‑control terms, granting each company a per‑allowance of up to 100,000 units while directing the remainder toward Hong Kong rather than the mainland. Regulators have required most H200 shipments to be routed to Hong Kong, which lacks sufficient data‑centre capacity and grid headroom; a single chip draws up to 700 W and an eight‑way server needs roughly ten kilowatts before cooling, creating a bottleneck for the roughly 500,000 H200 units built for Chinese customers.

**「Impact」** Organizations in mainland China planning AI/ML infrastructure face delayed deliveries and sharply higher costs for H200-based systems, with end-of-October quotes exceeding 6 million yuan per eight-card server, roughly three times the year-ago price. Buyers should treat current availability as limited to small allotments and indirect channels until large-scale import approval is granted.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/pc-components/gpus/first-nvidia-h200-shipments-reach-bytedance-and-tencent-as-beijing-loosens-its-import-block">First Nvidia H 200 shipments reach China ... | Tom&#x27;s Hardware</a></li>
<li><a href="https://aiinasia.com/news/china-nvidia-h200-imports-hong-kong-limit-news-2026-08-20">China Lets In Ten Thousand H 200 s and Parks the Rest… | AI in Asia</a></li>

</ul>
</details>

**Tags**: `#Hardware Supply Chain`, `#NVIDIA H200`, `#AI Infrastructure`, `#China Import Regulations`, `#GPU Availability`

---

<a id="item-tech-news-4"></a>
### [Hugging Face releases MoE training handbook for Megatron-LM](https://www.reddit.com/r/MachineLearning/comments/1xorgq0/the_ultimate_moe_training_handbook_training/) ⭐️ 7.0/10

Hugging Face engineers released a comprehensive handbook for training Mixture-of-Experts models with Megatron-LM, based on about 800,000 GH200 GPU-hours from MoE training on the Alps cluster at CSCS. The release includes the handbook, 55 accompanying figures, publicly available scripts, and a consolidated set of recommended Megatron-LM flags. It is designed for practitioners who have trained dense models and want to transition to MoE, with frontier model claims citing original papers, configs, or code, and toy simulations clearly labelled. The handbook covers architecture, routing, load balancing, expert design, systems, and serving.

reddit · r/MachineLearning · /u/Norlax\_42 · Nov 5, 19:13

**「Background」** The handbook extends the concepts introduced in Hugging Face&\#x27;s Ultra-Scale and Smol Training Playbooks, which documented dense model training methodologies. It provides a structured runbook for practitioners transitioning from dense to MoE architectures using Megatron-LM.

**「Impact」** The publicly released handbook, figures, and Megatron-LM flag scripts allow practitioners to train Mixture-of-Experts models using configurations validated across about 800,000 GH200 GPU-hours on the Alps cluster at CSCS.

**Tags**: `#Mixture-of-Experts`, `#Megatron-LM`, `#Training Systems`, `#Hugging Face`

---

<a id="item-tech-news-5"></a>
### [Publication expectations for ML PhDs at top US schools](https://www.reddit.com/r/MachineLearning/comments/1xoc358/publication_expectations_for_ml_phds_at_top10_us/) ⭐️ 7.0/10

A Reddit user states that approximately four first-author papers at top machine learning conferences such as NeurIPS, ICML, and ICLR are commonly perceived as a standard expectation for graduating from a top US ML PhD program. The same user notes that this impression may be biased by the specific Reddit posts they have encountered and asks whether the norm holds for top-10 US CS schools or similarly competitive machine learning groups. The post reflects a broader discussion about publication expectations in machine learning doctoral training, without asserting an official or universally applicable requirement.

reddit · r/MachineLearning · /u/Hope999991 · Nov 5, 06:56

**「Typical publication expectations for top ML PhD programs」** Community discussions indicate that graduating from a top‑10 US ML PhD program typically requires about four first‑author papers published in premier conferences such as NeurIPS, ICML, or ICLR. Earlier forum posts have noted that three to five such papers are viewed as evidence of sufficient capability, with three being a minimal threshold and five representing a strong profile.

<details><summary>References</summary>
<ul>
<li><a href="https://beyondmarketintelligence.com/post/would-you-let-an-ml-phd-student-graduate-without-a-top-tier-cmqo3i4jl08h9yt0pmdno2j16">Would you let an ML PhD student graduate without a top -tier paper ? [D]</a></li>
<li><a href="https://theaterfi.re/post/3728948">How cooked am I for ML research roles with this PhD ... | TheaterFire</a></li>

</ul>
</details>

**Tags**: `#Academic expectations`, `#PhD requirements`, `#Machine learning`, `#Education`, `#Career advice`

---

<a id="item-tech-news-6"></a>
### [DialFork benchmark released to measure procedural hallucination in conversational agents](https://www.reddit.com/r/MachineLearning/comments/1xofjrn/dialfork_a_benchmark_for_procedural_hallucination/) ⭐️ 7.0/10

Idiap Research Institute, in joint work with Logitech, has released DialFork, an open benchmark for measuring procedural hallucination in conversational LLM agents—situations where agents stay fluent and factual and make correct tool calls but stop following required dialogue steps. The release covers 24 tasks across 12 domains and over 36,000 forked dialogues with annotated drift points, plus code, dataset, human judgments, and a Hugging Face leaderboard with turn-, dialogue-, and set-level tracks. The authors describe it as the first benchmark for this axis and report initial results in arXiv paper 2610.21561, though independent verification of those results is not yet available.

reddit · r/MachineLearning · /u/sergbur · Nov 5, 10:44

**「Background」** Conversational agents are typically evaluated on factual accuracy and correct tool use. DialFork targets a separate failure mode: an agent can be accurate and tool-correct while still skipping or reordering the non-tool steps of a dialogue procedure, such as asking for confirmation or delivering a result.

**「Impact」** Developers can evaluate conversational agents for procedural drift using DialFork&\#x27;s three tasks and public Hugging Face leaderboard, submitting predictions as a single CSV file. The authors suggest uses such as detecting drift after a model upgrade or checking whether user-simulator dialogues unfold like real ones.

**Tags**: `#LLM agents`, `#procedural hallucination`, `#benchmarking`, `#conversational AI`, `#evaluation`

---

<a id="item-tech-news-7"></a>
### [Microsoft Says Windows 11 High Memory Use Is Fine](https://www.windowslatest.com/2026/11/05/windows-11-using-most-of-your-ram-microsoft-says-thats-a-good-thing-as-the-real-test-is-whether-your-pc-stays-responsive/) ⭐️ 7.0/10

Microsoft Windows head Pavan Davuluri said that Windows 11 can show 70% or 90% memory usage in Task Manager without indicating a memory shortage. He explained that Windows uses caching and releases memory when apps need it, comparing memory to a desktop and SSD to a drawer. Microsoft said the real test is whether the PC stays responsive, and a new tuning for 8 GB devices may allow up to 2 GB more active data to remain cached.

telegram · zaihuapd · Nov 5, 09:04

**「Background」** Prior to this announcement, many Windows 11 users reported that the operating system consistently used 70% or more of available RAM, even under light loads. This sparked discussions about potential memory leaks or inefficient resource handling. Microsoft&\#x27;s statement is the first official explanation that such usage is an intentional caching mechanism aimed at improving system responsiveness.

**「What This Means for Users」** The clarification may help users who see high memory numbers on Windows 11 avoid mistaking caching for a hardware problem. Developers and system reviewers should treat responsiveness as the key signal rather than low memory consumption, though the evidence about the 8 GB optimization remains limited to Microsoft&\#x27;s announcement.

**Tags**: `#Windows 11`, `#Memory Management`, `#OS Performance`, `#Caching`

---

<a id="item-tech-news-8"></a>
### [中国叫停软银 54 亿美元收购 ABB 机器人业务](https://www.bloomberg.com/news/articles/2026-11-05/china-blocks-softbank-s-acquisition-of-abb-industrial-robot-unit) ⭐️ 7.0/10

China&\#x27;s foreign investment security review blocked SoftBank&\#x27;s $5.4B acquisition of ABB&\#x27;s robotics business over concerns about industrial data and core technology transfer.

telegram · zaihuapd · Nov 5, 10:44

**Tags**: `#robotics`, `#AI regulation`, `#geopolitics`, `#mergers-acquisitions`, `#China tech policy`

---

<a id="item-tech-news-9"></a>
### [Huawei Cloud openPangu-2.1-Pro launches November 15, enhances ArkTS code generation](https://m.gelonghui.com/live/2748413) ⭐️ 7.0/10

Huawei Cloud announced that its MaaS platform will launch the openPangu-2.1-Pro flagship model on November 15, notifying current users via SMS. The release improves ArkTS code generation quality for HarmonyOS native application development. It synchronizes with Huawei&\#x27;s AgentArts, CodeArts, and OfficeAce platforms, integrating the model across the company&\#x27;s core developer tools.

telegram · zaihuapd · Nov 5, 13:27

**「Huawei Cloud openPangu Background」** The reported launch builds on Huawei Cloud&\#x27;s earlier openPangu model efforts and its MaaS platform, and it centers on ArkTS, the language used in HarmonyOS native app development. The release was said to improve ArkTS code generation and to integrate the flagship model into developer tools such as AgentArts, CodeArts, and OfficeAce.

**「Consequence for users」** From November 15, Huawei Cloud MaaS users can access openPangu-2.1-Pro for ArkTS code generation across AgentArts, CodeArts, and OfficeAce, while the previous Pangu model system is confirmed discontinued, requiring users to transition.

**Tags**: `#Huawei Cloud`, `#openPangu`, `#ArkTS`, `#AI model`, `#Developer tools`

---

<a id="item-tech-news-10"></a>
### [DeepSeek Harness reaches 1.54 million daily active users with over 35,000 plugins](https://mp.weixin.qq.com/s/xqyrRaiBpIcf0jeJzP7W0g) ⭐️ 7.0/10

DeepSeek Harness officially reported that as of November 4, its platform reached 1.54 million daily active users and consumes 92.1 trillion tokens per day, with nearly 35,000 third-party plugins and about 60% of active users using or developing plugins. The vendor announced plans to improve plugin API stability, launch an official plugin marketplace, and introduce an author support program offering token incentives, recommendations, and enterprise cooperation. These marketplace and incentive plans are announced intentions, not yet shipped capabilities. DeepSeek Harness describes its long-term vision as an &quot;Agent era operating system&quot; built on its plugin ecosystem.

telegram · zaihuapd · Nov 5, 15:20

**「Platform Growth History」** DeepSeek Harness&\#x27;s first version launched on August 13, with a desktop edition added on September 29, preceding the November 4 milestone of 1.54 million daily active users reported on November 5 \(tool-1-2\). The platform now hosts approximately 35,000 third-party plugins, with about 60% of active users having installed or created at least one, marking a substantial expansion from the initial release \(tool-1-1\).

**「Impact」** For developers and AI engineers, the reported plugin count and user engagement indicate a substantial existing ecosystem, but the promised official marketplace and API stability improvements are not yet available, so integrations built today may face breaking changes before the plugin API stabilizes.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gate.com/news/detail/deepseek-harness-discloses-154-million-daily-active-users-920-trillion-25432747">DeepSeek Harness Discloses 1.54 Million Daily Active Users ...</a></li>
<li><a href="https://finance.biggo.com/news/0d0b1b77-05b4-4f09-999f-09870787c613">DeepSeek Harness Daily Active Users Surge 468% to 1.54 Million</a></li>

</ul>
</details>

**Tags**: `#AI Agents`, `#Plugin Ecosystem`, `#Developer Tools`, `#Software Engineering`, `#Technology Industry`

---

<a id="item-tech-news-11"></a>
### [Google Releases Gemini Omni 1.2 Flash Video Model](https://x.com/Google/status/2118390406316728555) ⭐️ 7.0/10

Google DeepMind has released Gemini Omni 1.2 Flash, a video generation model that is faster and claims a 30% cost reduction. The model offers a two-step workflow: generating drafts at 360p or 720p resolution for $0.07 per second, then optionally upscaling to 1080p or 4K. Videos can be any length from 3 to 15 seconds. New capabilities include conversational per-turn adjustments to background, subject, or lighting; more natural multi-speaker lip-sync; and more controllable camera motion with fewer jump cuts.

telegram · zaihuapd · Nov 6, 00:21

**「Background」** Google DeepMind has been developing the Gemini family of multimodal models, which includes capabilities for text, image, and video generation. Prior video generation efforts from Google included models like Veo and Imagen Video, which focused on high-quality video synthesis. The Gemini Omni 1.2 Flash release represents a continuation of this line, emphasizing speed and cost efficiency for shorter-form video generation with interactive editing features.

**「Impact」** The 30% cost reduction and pay-per-second pricing at $0.07 for draft resolution make AI video generation more affordable for developers and content creators. The conversational per-turn editing and controllable camera motion directly address common pain points in AI-generated video, potentially reducing the need for manual post-production correction.

**Tags**: `#AI video generation`, `#Gemini`, `#Google DeepMind`, `#model release`, `#cost efficiency`

---

<a id="item-tech-news-12"></a>
### [India Announces 24-Month Plan for Homegrown GPU and RISC-V SHAKTI/VEGA Commercialization](https://www.tomshardware.com/tech-industry/semiconductors/india-targets-creating-homegrown-gpus-within-2-years-and-plans-to-commercialize-indigenous-shakti-and-vega-risc-v-processors-sees-ai-boom-as-a-potential-repeat-of-the-y2k-opportunity-for-its-it-industry) ⭐️ 7.0/10

India&\#x27;s Ministry of Electronics and Information Technology announced a roughly 24-month plan under Semiconductor Mission 2.0 to develop domestically designed GPU chips, with Secretary S. Krishnan disclosing the timeline on November 4. The government also plans to commercialize RISC-V-based SHAKTI and VEGA processors, though no manufacturer or chip supplier was identified. India&\#x27;s semiconductor market is currently about $50 billion and is projected to reach nearly $100 billion by 2030. The GPU effort is an announced roadmap rather than a shipped or independently verified product.

telegram · zaihuapd · Nov 6, 02:00

**「Background」** India&\#x27;s Semiconductor Mission is the government program through which the country is pursuing domestic chip design and fabrication capacity. SHAKTI and VEGA are RISC-V-based processor designs that India plans to bring to commercial markets alongside the new GPU effort.

**「Impact」** If delivered on the roughly 24-month schedule, the homegrown GPU would give Indian AI and computing customers a domestically designed processor option, but the government has not named a foundry, chip supplier, or target architecture, so the manufacturing and availability path remains unspecified.

**Tags**: `#semiconductor policy`, `#RISC-V`, `#GPU development`, `#India tech industry`, `#AI hardware`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [A database is a store for global variables](https://seangoedecke.com/a-database-is-a-store-for-global-variables/) ⭐️ 7.0/10

rss · Sean Goedecke · Nov 6, 00:00

**「Background」** The article observes that databases are definitionally global variables—any part of a program can read or write them—yet conventional wisdom condemns global variables while praising databases, creating an apparent contradiction.

**「Solution」** The author examines five explanations for why database-backed applications avoid the architectural problems of global variables. He dismisses the idea that ACID guarantees are the key difference, arguing that synchronization doesn&\#x27;t address the fundamental coupling problem. He also rejects the flexibility argument as only relevant to untyped languages. The two most convincing reasons are that database queries are syntactically explicit—requiring connection objects and query functions that are visible during code review—and that developers follow disciplined norms around database usage, such as validating column types and restricting databases to appropriate use cases. These advantages are contingent on practice, not inherent to databases; a codebase with strong conventions around global variables could achieve similar safety.

**「Takeaway」** The inconsistency between &quot;avoid global variables&quot; and &quot;use databases for state&quot; reveals that much software engineering wisdom consists of loose heuristics rather than rigorous principles, and engineers should be suspicious of appeals to &quot;best practice&quot; without concrete reasoning.

**Tags**: `#software architecture`, `#global state`, `#databases`, `#design heuristics`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Democrats Urge AI Data Center Moratorium After Midterms](https://www.cnbc.com/2026/11/05/democrats-data-center-restrictions-midterms.html) ⭐️ 8.0/10

After the 2026 U.S. midterm elections, some Democratic leaders called for a national moratorium on AI data center construction, and AI chip stocks sold off sharply; the iShares Semiconductor ETF fell nearly 9%, Nvidia dropped 8%, and AMD fell more than 14%.

rss · CNBC Finance · Nov 5, 20:17

**「background」** Democrats&\#x27; call for a national data center moratorium follows midterm election gains and a poll showing 56% of voters prioritized AI/data centers, with Texas accounting for 27% of planned capacity and several states already imposing moratoriums.

**「Impact」** The proposed moratorium and investor concerns were tied to sharp declines in AI chip and tech stocks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/05/democrats-data-center-restrictions-midterms.html">Top Democrats call to rein in AI buildout after midterms sweep...</a></li>
<li><a href="https://www.cnbc.com/2026/11/04/midterm-election-blue-wave-trump-billionaires.html">Midterm election takeaways: Tech billionaires hit as Democrats beat...</a></li>
<li><a href="https://www.businessinsider.com/ai-data-centers-backlash-debate-poll-midterm-election-2026-10">Many Voters Say AI Data Centers Will Shape Their Midterm Vote</a></li>

</ul>
</details>

**Tags**: `#data centers`, `#AI regulation`, `#midterm elections`, `#semiconductor stocks`, `#market impact`

---

<a id="item-finance-news-2"></a>
### [Barkin signals further gradual rate hikes](https://www.cnbc.com/2026/11/05/barkin-sees-interest-rate-hikes-ahead-but-at-a-gradual-pace.html) ⭐️ 7.0/10

Richmond Fed President Thomas Barkin says the Fed will likely raise rates further, with markets pricing over 80% chance of a December hike.

rss · CNBC Finance · Nov 5, 16:34

**「Background」** The Fed’s benchmark rate is currently 3.75%-4% after a recent hold, and Barkin will become a voting FOMC member in 2027.

**Tags**: `#Federal Reserve`, `#interest rates`, `#monetary policy`, `#inflation`, `#FOMC`

---

<a id="item-finance-news-3"></a>
### [Premarket Stock Movers: Unity Software Surges, Qualcomm Falls, Wendy&\#x27;s Rejects Takeover](https://www.cnbc.com/2026/11/05/stocks-making-the-biggest-moves-premarket-shak-wen-pton-u.html) ⭐️ 7.0/10

In premarket trading on November 5, 2026, Unity Software shares jumped 22% after reporting third-quarter earnings of 25 cents per share on $622 million revenue, beating estimates of 5 cents and $567 million; Qualcomm dropped 9% despite a slight earnings beat as its current-quarter guidance of $2.15-$2.35 per share fell short of the $2.26 consensus; and Wendy&\#x27;s shares were little changed after rejecting a $1.4 billion \($7.35 per share\) takeover offer from Trian Fund Management.

rss · CNBC Finance · Nov 5, 13:17

**「Background」** The moves reflect investor reactions to a wave of third-quarter earnings reports and guidance updates across technology, consumer, and semiconductor sectors.

**「Impact」** The mixed reactions highlight how guidance and forward-looking metrics often outweigh headline beats, potentially setting the tone for broader market sentiment during earnings season.

**Tags**: `#Earnings`, `#M&amp;A`, `#Pre-market`, `#Stock movements`

---

<a id="item-finance-news-4"></a>
### [Micron pauses $4.5 billion Taiwan DRAM plant over labor dispute](https://www.bloomberg.com/news/articles/2026-11-05/micron-pauses-work-on-4-5-billion-taiwan-plant-after-labor-spat) ⭐️ 7.0/10

Micron has paused construction of its $4.5 billion Taoyuan, Taiwan DRAM \(dynamic random‑access memory\) plant after a labor dispute, according to Bloomberg, delaying the facility’s planned 2028 start.

telegram · zaihuapd · Nov 5, 11:26

**「Background」** The Taoyuan plant, which would add capacity to Micron’s DRAM \(dynamic random‑access memory\) line that supplies about 60% of its global DRAM output, had been scheduled to begin production in 2028, according to the report.

**「Impact」** The pause may delay DRAM supply to device manufacturers and strain Taiwan’s semiconductor supply chain.

**Tags**: `#Micron`, `#DRAM`, `#Taiwan`, `#labor dispute`, `#semiconductor manufacturing`

---

<a id="item-finance-news-5"></a>
### [Switch 2 sales decline and earnings miss](https://mp.weixin.qq.com/s/XTw5DXy2CvqFSs4WYx73Xg) ⭐️ 7.0/10

Nintendo reported Switch 2 sales of 2.67 million units in Q2 ending September 30, 2026, down 41% year-on-year, with revenue of 44.82 billion yen and profit of 73.5 billion yen both below market expectations; the company maintained its full-year target of 16.5 million units for the fiscal year ending March 2027.

telegram · zaihuapd · Nov 5, 14:12

**「Background」** The results cover Nintendo&\#x27;s second fiscal quarter ending September 30, 2026, following the Switch 2&\#x27;s market launch.

**Tags**: `#Nintendo`, `#Switch 2`, `#sales decline`, `#earnings miss`

---

<a id="item-finance-news-6"></a>
### [Chip Stock Sell-Off Intensifies, Nasdaq 100 Drops 5%](https://www.bloomberg.com/news/articles/2026-11-04/stock-market-today-dow-s-p-live-updates) ⭐️ 7.0/10

On November 4, 2026, US chip stocks sold off sharply, with the Nasdaq 100 dropping 5% and the Philadelphia Semiconductor Index falling 36% from its June high, as investors assessed potential AI regulation following the Democratic congressional sweep.

telegram · zaihuapd · Nov 5, 15:39

**「Background」** The sell-off intensifies amid investor concern that a Democratic-controlled Congress may impose stricter regulations on AI-driven trading, a shift from the prior Republican majority.

**「Impact」** Capital has rotated into defensive sectors such as consumer staples and healthcare, while US Treasuries, yen, and Swiss franc strengthened, as markets priced in potential AI regulation following the Democratic congressional sweep.

**Tags**: `#stock market`, `#semiconductor`, `#Nasdaq`, `#regulation`, `#earnings`

---