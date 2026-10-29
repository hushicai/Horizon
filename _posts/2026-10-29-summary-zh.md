---
layout: default
title: "Horizon Summary: 2026-10-29 (ZH)"
date: 2026-10-29
lang: zh
---

> 从 38 条内容中筛选出 16 条重要资讯。

---

**科技新闻**
1. [Google 发布 Gemini 4 Carbon](#item-tech-news-1) ⭐️ 9.0/10
2. [Dayjob: Tax – evaluating AI agents on 50 professional tax assignments](#item-tech-news-2) ⭐️ 8.0/10
3. [macOS system utilities still trust revoked eMudhra CA certificates](#item-tech-news-3) ⭐️ 8.0/10
4. [GitHub Octoverse 2026：AI 代理推动开发活动创下历史新高](#item-tech-news-4) ⭐️ 7.0/10
5. [Amazon 发布 AI 时代开发者角色指南：AI 工具无效视为发现而非失败](#item-tech-news-5) ⭐️ 7.0/10
6. [Harvard Assistant Professor Stephen Casper AMA on AI Safeguards and Governance](#item-tech-news-6) ⭐️ 7.0/10
7. [EmbeddingGemma-2 audio benchmark jumps to \#1 via zero‑training PCA null‑space injection](#item-tech-news-7) ⭐️ 7.0/10
8. [人类在环境下语音分离中胜过 ASR 模型，但差距不足以构成 CAPTCHA](#item-tech-news-8) ⭐️ 7.0/10
9. [GPT-OSS-20B 上 generic feedback line 匹配逆向自蒸馏中的 self-written critiques \(ACM ICAIF &\#x27;26\)](#item-tech-news-9) ⭐️ 7.0/10
10. [VentureBeat 调研：企业 GPU 严重闲置却持续扩建 AI 算力](#item-tech-news-10) ⭐️ 7.0/10
11. [长鑫存储拟量产 HBM3E，良率仅两三成](#item-tech-news-11) ⭐️ 7.0/10
12. [Apple 新款 MacBook Pro 首发 PROLED XDR 显示屏并加入触控](#item-tech-news-12) ⭐️ 7.0/10
13. [ChatGPT Pro 和 Business 用户每月可领取最高 500 美元 API 额度](#item-tech-news-13) ⭐️ 7.0/10

**财经新闻**
1. [长鑫科技正式纳入上证指数并位列第一大权重股](#item-finance-news-1) ⭐️ 8.0/10
2. [韩国对苹果和谷歌开出罚款](#item-finance-news-2) ⭐️ 7.0/10
3. [Google 将 AI 模式搜索广告推向全球市场](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Google 发布 Gemini 4 Carbon](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/) ⭐️ 9.0/10

Google 发布了 Gemini 4 Carbon，并称其为目前最强的前沿 AI 模型，主打网络安全与长时程自主任务。它在复杂多步工程问题上可持续自主工作数天，并在编程、代理、科学任务、全栈网页开发和多模态理解上获得明显提升。相比前代 Argon，安全代码生成成功率提升超过两倍，对齐和幻觉问题大幅下降，并在部分网络安全基准上领先。目前以入门价格发布，输入和输出价格分别为每百万 token 2 美元和 10 美元，与 Argon 相同，后续可能翻倍。

telegram · zaihuapd · 10月28日 17:09

**「Gemini 4 Carbon 背景」** 要理解 Google 发布 Gemini 4 Carbon，需要先看到它承袭的上一代模型迭代背景。此前被称作 Argon 的前沿模型已经涉及安全代码生成、对齐与幻觉控制等方向，而 Gemini 4 Carbon 被报道为继续推进并强调网络安全与长时程任务能力。

**「影响」** 对可接受范围内的网络安全防御者和可信合作伙伴，Gemini 4 Carbon 可能带来更强的代码生成与漏洞定位能力；对后续更广泛的开发者、企业和消费者，则可能带来更高级的自主 AI 应用。Google 表示将逐步向部分网络安全防御者和可信合作伙伴开放，包括美国政府预发布测试，之后再向更广泛用户提供。这一分阶段开放和后续可能翻倍的价格也意味着早期用户需要关注可用性和成本安排。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/">Introducing Gemini 4 Carbon - The Keyword</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google`, `#Gemini`, `#Cybersecurity`, `#Large Language Models`

---

<a id="item-tech-news-2"></a>
### [Dayjob: Tax – evaluating AI agents on 50 professional tax assignments](https://surgehq.ai/blog/dayjob-tax) ⭐️ 8.0/10

A blog post detailing an evaluation of AI agents on 50 professional tax assignments, offering insights into AI capabilities and limitations in tax preparation.

hackernews · landonxi · 10月28日 15:46 · [社区讨论](https://news.ycombinator.com/item?id=50275626)

**标签**: `#AI evaluation`, `#tax AI`, `#benchmark dataset`, `#open source AI`, `#software engineering`

---

<a id="item-tech-news-3"></a>
### [macOS system utilities still trust revoked eMudhra CA certificates](https://emudhra.we-have-a-problem.com/apple.html) ⭐️ 8.0/10

Apple&\#x27;s macOS continues to trust revoked eMudhra CA certificates in built‑in utilities such as git, affecting all macOS users and developers who rely on these tools. The certificates were compromised and revoked, but they remain present in the system’s /etc/ssl and /etc/certs trust stores, leaving the default git and other command‑line tools vulnerable. Apple&\#x27;s support article \(https://support.apple.com/en-us/149555\) advises a manual edit of the certificate chain, a workaround that can be overwritten by future OS updates. This creates a persistent security risk for anyone using the system‑provided git or other utilities that inherit the OS trust store.

hackernews · galadran · 10月28日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=50271640)

**「背景」** 印度证书颁发机构 eMudhra 的八个中间证书因私钥过于脆弱、可被几乎即时恢复而被吊销，Mozilla、Google 和 Apple 等厂商随后将其列入阻止列表。Apple 支持文档指出，macOS 自带的命令行工具（包括 git、curl、openssl 等）会针对 /etc/ssl/cert.pem 检查证书，但对链至该文件中根 CA 证书的证书，不检查 Apple 的阻止列表或吊销状态。Apple 正在开发针对命令行工具剩余问题的 macOS 更新。

**「Impact」** Developers and users who apply Apple’s manual certificate removal must reapply it after each macOS update, leaving the system exposed until the next patch is installed.

**「Community discussion」** Commenters note that the problem extends beyond git to many system utilities and criticize Apple’s reliance on a fragile manual fix that may be undone by OS updates, calling for a permanent removal of the revoked CA from the system trust store.

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.apple.com/en-us/149555">About the compromised eMudhra intermediate CAs - Apple Support</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/mozilla-google-apple-block-compromised-emudhra-ca-certificates/">Mozilla, Google, Apple block compromised eMudhra CA certificates</a></li>
<li><a href="https://www.news18.com/tech/apple-blocks-vulnerable-emudhra-security-certificates-macos-fix-still-in-development-10397973.html">Apple Blocks Vulnerable eMudhra Security Certificates, macOS ...</a></li>

</ul>
</details>

**标签**: `#security`, `#macOS`, `#certificates`, `#git`, `#vulnerability`

---

<a id="item-tech-news-4"></a>
### [GitHub Octoverse 2026：AI 代理推动开发活动创下历史新高](https://simonwillison.net/2026/Oct/28/github-octoverse-2026/) ⭐️ 7.0/10

GitHub 在 2026 年 Octoverse 报告中公布三项关键平台指标创下历史新高：合并 Pull Request 达到每月 2.2 亿（不到一年内翻三倍），提交量达到每月 73.8 亿（翻三倍以上，且大部分增长集中在下半年），新建仓库达到每月 3030 万（年内翻倍）。博主 Simon Willison 将此归因于「代理工程」（agentic engineering）对 GitHub 的影响。报告还新增了按行业（通过多语言嵌入模型按 NAICS 行业分类）和「互操作性或逆向工程」相关仓库的细分数据，其中国家推送量使用了 LLM 分类来消除 VPN 使用带来的偏差。

rss · Simon Willison · 10月28日 16:45

**「背景脉络」** Octoverse 是 GitHub 的年度开发者生态报告，历年持续追踪平台上的提交、Pull Request 和新建仓库等核心指标。2026 年的报告在方法论上做了显著升级：引入 LLM 分类来提取用户个人资料中的 ISO 国家代码以校正 VPN 偏差，使用微调的多语言嵌入模型按 NAICS 行业对 2022 至 2026 年创建的公开仓库进行分类，并通过关键词匹配识别与互操作性或逆向工程相关的仓库。

**「影响与关注点」** 对于软件工程和 AI 实践者而言，这些数据表明 AI 代理已大规模渗透到日常开发流程中，平台级开发活动量在 2026 年下半年出现爆发式增长。但需注意，上述指标均为平台总量数据，不能直接等同于个体开发者效率的提升；同时，代理工程的快速扩张也引发了对代码质量、安全审计和归属权的潜在担忧，目前报告并未对此提供进一步分析。

**标签**: `#GitHub`, `#Octoverse`, `#developer metrics`, `#AI agents`

---

<a id="item-tech-news-5"></a>
### [Amazon 发布 AI 时代开发者角色指南：AI 工具无效视为发现而非失败](https://simonwillison.net/2026/Oct/28/terk-terkowitz/) ⭐️ 7.0/10

Amazon 工程领导 Terk Terkowitz 发布了《AI 时代软件工程师角色指南》，明确规定：如果当前 AI 工具未为工作带来效益，这被视为“发现”而非“失败”，工程师应记录原因、同行分享并上报管理者以寻求解决方案。该指南强调，能够阐明 AI 尚未帮助其工作之处的工程师，展现了 Amazon 所要求的判断力。该指南现已发布，适用于 Amazon 软件工程师群体，并对 AI 工具的适用范围设定了明确的评估边界。

rss · Simon Willison · 10月28日 10:09

**「背景」** 亚马逊工程领导层近期更新了软件开发工程师的角色指南，强调最终结果而非所使用的工具。该指南由副总裁 Terk Terkowitz 在备忘录中发布，指出 AI 正在以前所未有的速度改变软件开发，并要求工程师更贴近客户。

**「影响」** 依据该指南，Amazon 软件工程师被要求对 AI 工具的使用效益进行正式记录和汇报，这将促使团队在 AI 集成决策中更透明，并显著减少对无效工具的盲目依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aboutamazon.com/news/company-news/amazon-software-engineer-role-guideline-ai">An update from Amazon engineering leadership on the role of ...</a></li>
<li><a href="https://www.businessinsider.com/amazon-software-engineers-prioritize-results-over-ai-usage-2026-10">Amazon Tells Software Engineers to Prioritize Results Over AI ...</a></li>
<li><a href="https://economictimes.indiatimes.com/ai/ai-insights/amazon-asks-engineers-to-reconnect-with-customers-as-ai-reshapes-software-development/articleshow/135254616.cms">Amazon asks engineers to reconnect with customers as AI ...</a></li>

</ul>
</details>

**标签**: `#amazon`, `#ai`, `#software-engineering`, `#generative-ai`, `#agentic-engineering`

---

<a id="item-tech-news-6"></a>
### [Harvard Assistant Professor Stephen Casper AMA on AI Safeguards and Governance](https://www.reddit.com/r/MachineLearning/comments/1xhpnfs/ama_this_wednesday_stephen_cas_casper_harvard/) ⭐️ 7.0/10

Harvard Assistant Professor Stephen “Cas” Casper will host a live AMA on Wednesday, 28 October, from 3 pm to 4 pm ET \(19:00 UTC, 20:00 CET\) to discuss AI safeguards, incidents, and governance, answering community questions directly. The AMA thread will be posted by u/HarvardKennedy shortly before the start, with a dated verification photo, and Cas will type his own responses; participants can submit questions in the comments if they cannot attend live. Casper, a computer scientist who earned a PhD at MIT and completed a research residency at the UK AI Security Institute, has stated he will not work for big tech or sign non‑disparagement agreements.

reddit · r/MachineLearning · /u/NeuralNomad87 · 10月28日 14:30

**「前提背景」** 围绕人工智能安全与治理的公共政策讨论日益活跃，为理解现代 AI 风险管理提供了背景。哈佛肯尼迪学院助理教授 Stephen &quot;Cas&quot; Casper 专注于 AI 事件与治理研究，本次 AMA 为公众提供了直接向该领域专家提问的机会。

**「对社区参与者的影响」** 机器学习与人工智能社区的研究者、开发者、政策制定者和公众可通过本次 AMA 直接向哈佛学者 Stephen Casper 提问，获得关于 AI 安全、保障措施、风险、治理、州与联邦立法及 AI 恐怖主义事件的公开存档式专家解答；无法在直播时段（10 月 28 日 3–4 点 ET）参会者仍可提前提交问题。鉴于其声明从未为大型科技公司工作且从未签署贬低性保密协议，这些回答预期行业偏向较低，可作为独立参考资源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://agihunt.info/en/p/1a1780923b03428d36d699f7f7d">AMA: Harvard&#x27;s Stephen &quot;Cas&quot; Casper on AI… · AGI Hunt</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#Governance`, `#AMA`, `#Harvard`, `#AI research`

---

<a id="item-tech-news-7"></a>
### [EmbeddingGemma-2 audio benchmark jumps to \#1 via zero‑training PCA null‑space injection](https://www.reddit.com/r/MachineLearning/comments/1xho7pr/r_taking_embeddinggemma2_577m_from_rank_26_to_1/) ⭐️ 7.0/10

A Reddit‑reported experiment shows that injecting PCA‑reduced Conformer layers into the 256‑dimensional null space of google/embeddinggemma‑2 \(577 M\) raises its MAEB audio macro score from 49.3 % to 54.4 % \(+5.1 points\), moving the model from rank \#26 to \#1 on the audio‑only leaderboard and from \#16 to \#1 on the full MAEB set. The method requires no retraining: the 512‑dimensional text subspace is left untouched, while the unused 256 dimensions are filled with PCA‑compressed representations of intermediate layers \(Layer 2 and Layer 6\) derived from external audio data. The approach also introduces trade‑offs, such as loss of spoken‑intent classification performance and the inability to truncate to lower dimensions without retraining.

reddit · r/MachineLearning · /u/JeanMichelRanu · 10月28日 13:34

**「Background」** EmbeddingGemma‑2 projects 512‑dimensional text vectors into a 768‑dimensional space using a linear matrix that leaves a 256‑dimensional null space unused by text. By compressing intermediate Conformer layers with PCA and injecting them into this null space, the model can capture additional acoustic information without altering the text‑aligned subspace. The MAEB benchmark evaluates audio tasks such as speaker clustering, emotion recognition, and environmental sound retrieval, and is part of the broader MTEB leaderboard.

**「Impact」** The zero‑training injection yields a measurable +5.1 point gain on MAEB audio tasks, but it reduces spoken‑intent classification accuracy, illustrating a trade‑off between acoustic enrichment and semantic purity.

**标签**: `#EmbeddingGemma`, `#audio embeddings`, `#null space`, `#PCA`, `#MTEB`

---

<a id="item-tech-news-8"></a>
### [人类在环境下语音分离中胜过 ASR 模型，但差距不足以构成 CAPTCHA](https://www.reddit.com/r/MachineLearning/comments/1xhuado/cocktailparty_audio_as_a_reverse_turing_test/) ⭐️ 7.0/10

一项将反向图灵测试应用于混音环境语音分离的实验表明，人类在从背景噪音中提取目标说话人时的表现优于八种 ASR 模型，但差距过小，无法作为可靠的音频 CAPTCHA。实验比较了 146 名人类参与者和 8 种模型配置（包括 Whisper base/small、Vosk、Wav2Vec2、Qwen3-ASR 0.6B、Parakeet CTC 0.6B 和 Gemini 3.8 Flash）在 40 个合成音频片段上的表现，人类的平均词准确率为 0.71，而 Gemini 为 0.54，Qwen3-ASR 为 0.55，人类通过率为 77%，Gemini 为 55%。由于人类与最佳模型之间的词准确率差距仅为约 0.13，远未达到人类&gt;80%和机器&lt;20%的预期分离，无法满足 CAPTCHA 所需的可靠性，同时实验仅涉及 18 个会话、单一合成场景和有限的英语受众等限制。

reddit · r/MachineLearning · /u/cloud\_kj · 10月28日 17:17

**「背景」** 混音环境中的语音分离（所谓“鸡尾酒会问题”）是指从重叠声音源中提取特定说话人语音的能力。ASR 模型如 Whisper、Vosk 等在干净音频上表现良好，但在复杂混音场景中往往难以将目标语音与背景噪音区分开来。反向图灵测试 CAPTCHA 利用人类在特定任务上优于机器的优势，常用于身份验证。

**「影响」** 由于当前 ASR 模型与人类之间的表现差距过小，音频 CAPTCHA 的设计者不能仅依赖这些模型来形成可靠的人机差异，需提高音频难度或结合其他验证手段以达到实用目的。

**标签**: `#speech recognition`, `#ASR`, `#reverse Turing test`, `#audio CAPTCHA`, `#benchmark`

---

<a id="item-tech-news-9"></a>
### [GPT-OSS-20B 上 generic feedback line 匹配逆向自蒸馏中的 self-written critiques \(ACM ICAIF &\#x27;26\)](https://www.reddit.com/r/MachineLearning/comments/1xhv8yp/how_much_does_the_hint_matter_a_generic_feedback/) ⭐️ 7.0/10

研究团队在 GPT-OSS-20B 上探索了面向多步金融推理的逆向自蒸馏，学生模型会定位自身的第一个错误步骤并撰写 critique，随后通过 reverse KL 散度将条件于前缀加 critique 的冻结副本蒸馏回学生。实验表明，用固定的 generic feedback line 替代 self-written critique 也能获得约 3 个点的性能提升，而来自 6 倍更大模型的 critique 并未显著提升性能，这表明逆向蒸馏中提供的位置信息显著降低了有效训练所需的特权信息。Fin-SD 在使用 9.5% 更少 tokens 的情况下，与基于完整参考解的 OPSD 实现了匹配。

reddit · r/MachineLearning · /u/jhzyu · 10月28日 17:52

**「背景」** 大模型自蒸馏框架常通过模型自身的输出进行自我纠正，以提升推理可靠性与对齐质量。

**「影响」** 对于金融推理任务的开发者而言，可直接使用固定的 generic feedback line 代替自写 critique，在性能约损失 3 个点的情况下，可省去大模型 critique 生成的开销，并结合 Fin-SD 的 9.5% token 效率提升降低整体推理成本。

---

<a id="item-tech-news-10"></a>
### [VentureBeat 调研：企业 GPU 严重闲置却持续扩建 AI 算力](https://venturebeat.com/infrastructure/ai-bubble-update-79-of-companies-say-their-gpus-sit-idle-at-least-half-the-time-yet-most-plan-new-ai-platforms) ⭐️ 7.0/10

VentureBeat 最新企业调研显示，79%受访企业的 GPU 平均利用率不足 50%，91%的 AI 基础设施投资未经财务部门正式 ROI 审计；尽管利用率低下，70%此类企业仍计划在未来 12 个月内继续采购部署新 AI 计算平台。

telegram · zaihuapd · 10月28日 02:37

**「背景」** GPU 利用率衡量计算卡在一段时间内实际承担 AI 训练或推理任务的比例，低于 50% 意味着超过一半时间闲置；ROI 审计是财务部门对资本投入是否产生相应业务回报的正式评估。此前 VentureBeat 相关调研已显示企业 AI 芯片普遍未满载运行（tool-1-2），本次调研进一步量化了算力闲置与缺乏财务审计之间的脱节。

**「实际影响」** 企业在缺乏投资回报验证的情况下持续扩大算力采购，可能导致资本大量沉淀在闲置硬件上，挤占本可用于模型优化、数据治理或业务落地的预算，加剧 AI 项目商业闭环缺失的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://verdice.news/article/86-of-in-house-ai-chips-run-half-empty-survey-qxpvpdw">86% of In-House AI Chips Run Half -Empty: Survey | Verdice News</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#GPU utilization`, `#enterprise AI`, `#ROI`, `#technology industry`

---

<a id="item-tech-news-11"></a>
### [长鑫存储拟量产 HBM3E，良率仅两三成](https://www.reuters.com/world/china/chinas-cxmt-start-advanced-ai-memory-production-despite-poor-yields-sources-say-2026-10-28/) ⭐️ 7.0/10

长鑫存储（CXMT）已向多家国内 AI 芯片设计公司送样 HBM3E，并计划在未来两个月内启动限量生产。知情人士称，其良率仅 20% 至 30%，远低于 SK 海力士约 70%；测试中性能更接近 SK 海力士上一代 HBM3，预计售价高于海外同类产品。这属于厂商推进的计划，尚未实现高良率量产。

telegram · zaihuapd · 10月28日 06:19

**「背景」** HBM 是 AI 加速器的关键高带宽内存，受美国出口管制影响，国内难以获取先进 HBM 产品，导致 AI 内存供应紧张。作为中国存储制造商，长鑫存储此次转向 HBM3E 是为填补国内高端 AI 内存空白。

**「影响」** 国内 AI 芯片设计公司可获样品验证，但需注意该 HBM3E 性能更接近上一代 HBM3，且良率低、价格高，可能限制其在大规模 AI 集群中的成本效益与兼容性适配。

**标签**: `#HBM3E`, `#CXMT`, `#AI memory`, `#semiconductor manufacturing`, `#China tech`

---

<a id="item-tech-news-12"></a>
### [Apple 新款 MacBook Pro 首发 PROLED XDR 显示屏并加入触控](https://www.apple.com/newsroom/2026/10/apple-unveils-groundbreaking-macbook-pro-with-proled-xdr-display/) ⭐️ 7.0/10

苹果发布新款 MacBook Pro，面向硬件爱好者、开发者和 AI/ML 从业者，首发 PROLED XDR 串联 OLED 显示屏，峰值亮度 2000 尼特、对比度约 1000 万:1，并首次为 Mac 加入触控。新机搭载 M5 Pro 或 M5 Max 芯片，14 英寸和 16 英寸机身更薄更轻，并提供最长 24 小时续航。该机于 2026 年 10 月 28 日预售，11 月 6 日开售，14 英寸版起售 22999 元人民币，16 英寸版起售 27999 元人民币。

telegram · zaihuapd · 10月28日 17:16

**「显示技术变迁」** 此前 MacBook Pro 系列均搭载 Liquid Retina 或 mini-LED 背光的 XDR 显示屏。本次发布的 PROLED XDR 串联 OLED 屏和首次触控功能标志着苹果笔记本显示技术的重大突破。

**「影响」** 对依赖苹果新硬件、高端 Mac 与 AI/ML 场景的开发者和用户而言，首次触控和更强的显示规格可能带来新的移动交互与开发体验。不过，来源仅提供发布信息，第三方软件兼容性和实际体验仍待确认。

**标签**: `#hardware`, `#apple`, `#laptop`, `#display`, `#semiconductor`

---

<a id="item-tech-news-13"></a>
### [ChatGPT Pro 和 Business 用户每月可领取最高 500 美元 API 额度](https://developers.openai.com/api/docs/guides/chatgpt-api-credits) ⭐️ 7.0/10

OpenAI 将 API 额度作为 ChatGPT Pro 和 Business 订阅权益捆绑发放：Pro 用户按订阅档位领取对应额度（$100/$200/$500），Business 用户按付费席位计算（Standard $20/席、Premium $100/席，工作区合计上限 $500/月）。用户需在 ChatGPT 或 API Platform 中关联已有 API 组织以激活权益。

telegram · zaihuapd · 10月29日 01:12

**「订阅权益背景」** OpenAI 之前将 API 额度与单独的开发者计划或信用优惠绑定，而非直接捆绑在个人或团队的 ChatGPT 订阅中。这种将订阅费与 API 使用额度挂钩的模式，是近年来云服务商常见的流量与信用结合方式。

**「对开发者与企业的直接影响」** 开发者若已拥有 OpenAI API 组织并使用 ChatGPT Pro 或 Business 订阅，可直接将订阅额度转为 API 调用额度，无需额外购买；Business 用户需注意席位上限为工作区合计 $500/月，超出部分仍需单独付费。

**标签**: `#OpenAI`, `#API`, `#ChatGPT`, `#pricing`, `#developer-tools`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [长鑫科技正式纳入上证指数并位列第一大权重股](https://m.gelonghui.com/live/2733034) ⭐️ 8.0/10

Changxin Technology has been added to the Shanghai Stock Exchange composite indices, becoming the top‑weight stock in both with weights of 4.67% and 15.74%, and the inclusion aligns with a new rule limiting single‑stock weights to 15%.

telegram · zaihuapd · 10月28日 08:03

**标签**: `#Index Inclusion`, `#Weight Adjustment`, `#Regulatory Change`, `#China A‑share`

---

<a id="item-finance-news-2"></a>
### [韩国对苹果和谷歌开出罚款](https://appleinsider.com/articles/26/10/28/south-korea-becomes-the-latest-to-fine-apple-and-google-millions-over-their-app-stores) ⭐️ 7.0/10

韩国通信监管机构对苹果和谷歌开出罚款，苹果被处 1550 万美元、谷歌 3200 万美元，并要求两家允许应用内外部支付链接并改进应用审核流程。

telegram · zaihuapd · 10月28日 12:30

**「韩国应用商店支付法背景」** 韩国在 2021 年修改《电信业务法》，成为首个禁止应用商店强制开发者使用单一应用内支付系统的国家。

**「韩国对苹果、谷歌处以罚款并要求改进支付政策」** 韩国监管机构对苹果罚款 1550 万美元，谷歌罚款 3200 万美元，要求其允许外部支付链接并改善应用审核流程，直接影响到开发者和应用生态系统

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tech-quire.com/articles/south-korea-fines-google-apple-app-payment/">South Korea fines Google and Apple 63.7 billion won over in- app ...</a></li>
<li><a href="https://www.euronews.com/2026/10/28/south-korea-fines-google-apple-for-pushing-app-developers-onto-their-payment-systems">South Korea fines Google , Apple for pushing app developers onto...</a></li>
<li><a href="https://finance.yahoo.com/technology/articles/south-korea-fines-google-apple-095158608.html">South Korea fines Google and Apple over unfair app market practices</a></li>
<li><a href="https://www.aa.com.tr/en/asia-pacific/south-korea-fines-google-apple-45m-over-app-store-payment-policies/4103750">Anadolu Ajansı: South Korea fines Google , Apple $45M over app ...</a></li>

</ul>
</details>

**标签**: `#South Korea regulation`, `#App Store payments`, `#antitrust enforcement`, `#Apple`, `#Google`

---

<a id="item-finance-news-3"></a>
### [Google 将 AI 模式搜索广告推向全球市场](https://techcrunch.com/2026/10/28/google-expands-ai-search-ads-globally-as-core-ad-growth-slows/) ⭐️ 7.0/10

Google expands AI mode search ads globally amid a slowdown in core search ad growth, highlighting its shift toward generative AI monetization in a key revenue segment.

telegram · zaihuapd · 10月29日 01:43

**标签**: `#Google`, `#AI search ads`, `#earnings`, `#digital advertising`, `#Alphabet`

---