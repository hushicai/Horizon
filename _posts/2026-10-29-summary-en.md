---
layout: default
title: "Horizon Summary: 2026-10-29 (EN)"
date: 2026-10-29
lang: en
---

> From 38 items, 16 important content pieces were selected

---

**Technology News**
1. [Google releases Gemini 4 Carbon for cybersecurity and long-horizon tasks](#item-tech-news-1) ⭐️ 9.0/10
2. [Dayjob: Tax – evaluating AI agents on 50 professional tax assignments](#item-tech-news-2) ⭐️ 8.0/10
3. [macOS still trusts revoked eMudhra certificates in system git](#item-tech-news-3) ⭐️ 8.0/10
4. [GitHub Octoverse 2026 reports record PRs, commits, and AI agent usage](#item-tech-news-4) ⭐️ 7.0/10
5. [Amazon&\#x27;s Terk Terkowitz on AI Utility in Engineering Work](#item-tech-news-5) ⭐️ 7.0/10
6. [Harvard AI safety researcher Stephen Casper hosts AMA on AI safeguards](#item-tech-news-6) ⭐️ 7.0/10
7. [PCA null-space injection lifts EmbeddingGemma-2 to \#1 on MAEB audio](#item-tech-news-7) ⭐️ 7.0/10
8. [Human advantage narrow in cocktail‑party speech separation test](#item-tech-news-8) ⭐️ 7.0/10
9. [Generic feedback matches self-critiques in hindsight self-distillation for financial reasoning](#item-tech-news-9) ⭐️ 7.0/10
10. [Enterprise AI GPU Underutilization Survey Findings](#item-tech-news-10) ⭐️ 7.0/10
11. [CXMT Pursues HBM3E Production Despite Low Yields](#item-tech-news-11) ⭐️ 7.0/10
12. [Apple Unveils MacBook Pro with PROLED XDR Display and Touch Support](#item-tech-news-12) ⭐️ 7.0/10
13. [OpenAI Bundles Up to $500 Monthly API Credits with ChatGPT Pro and Business](#item-tech-news-13) ⭐️ 7.0/10

**Financial News**
1. [长鑫科技正式纳入上证指数并位列第一大权重股](#item-finance-news-1) ⭐️ 8.0/10
2. [South Korea fines Apple and Google over app store practices](#item-finance-news-2) ⭐️ 7.0/10
3. [Google 将 AI 模式搜索广告推向全球市场](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Google releases Gemini 4 Carbon for cybersecurity and long-horizon tasks](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/) ⭐️ 9.0/10

Google has released Gemini 4 Carbon, its most advanced frontier model, targeting cybersecurity and long-horizon autonomous tasks. The model can work continuously for days on complex multi-step engineering problems such as locating and fixing vulnerabilities in large codebases and low-level system debugging. Compared to its predecessor Argon, Gemini 4 Carbon more than doubles safe code generation success rates and significantly reduces alignment and hallucination issues, with unsupported claims cut roughly in half and high-severity misalignment alerts down nearly 80%. It leads on cybersecurity benchmarks including SEC-bench Pro at 88.2% and vulnerability detection and patch generation. The model launches at introductory pricing of $2 per million input tokens and $10 per million output tokens \(matching Argon, with prices set to double later\), initially available to select cybersecurity defenders and trusted partners including U.S. government pre-release testing, before broader rollout to developers, enterprises, and consumers.

telegram · zaihuapd · Oct 28, 17:09

**「Background」** Google has been iterating its Gemini line of frontier AI models, with the previous generation, Gemini 4 Argon, serving as the baseline for comparison. The new Gemini 4 Carbon is positioned as the direct successor, claiming substantial improvements in safety, code generation, and cybersecurity over Argon. This release continues Google&\#x27;s strategy of pushing frontier models toward specialized, high-stakes domains like security and long-running autonomous tasks.

**「Impact」** Security teams and trusted partners gain immediate access to a model that can autonomously hunt and patch vulnerabilities across large codebases for days, potentially accelerating defensive cyber operations. The introductory pricing parity with Argon provides a cost-neutral upgrade path for early adopters, though the planned price doubling will affect budgeting for sustained use.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/">Introducing Gemini 4 Carbon - The Keyword</a></li>
<li><a href="https://www.theverge.com/tech/1021339/google-gemini-4-carbon-cybersecurity-frontier">Google launches Gemini 4 Carbon with a ‘significant leap’ in ...</a></li>
<li><a href="https://www.online-tech-tips.com/google-gemini-4-carbon-cybersecurity-long-context/">Google announces Gemini 4 Carbon with state-of-the-art ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Google`, `#Gemini`, `#Cybersecurity`, `#Large Language Models`

---

<a id="item-tech-news-2"></a>
### [Dayjob: Tax – evaluating AI agents on 50 professional tax assignments](https://surgehq.ai/blog/dayjob-tax) ⭐️ 8.0/10

A blog post detailing an evaluation of AI agents on 50 professional tax assignments, offering insights into AI capabilities and limitations in tax preparation.

hackernews · landonxi · Oct 28, 15:46 · [Discussion](https://news.ycombinator.com/item?id=50275626)

**Tags**: `#AI evaluation`, `#tax AI`, `#benchmark dataset`, `#open source AI`, `#software engineering`

---

<a id="item-tech-news-3"></a>
### [macOS still trusts revoked eMudhra certificates in system git](https://emudhra.we-have-a-problem.com/apple.html) ⭐️ 8.0/10

macOS continues to trust revoked eMudhra CA certificates in system-provided utilities, including the OS-supplied git, leaving those tools able to accept certificates chained to the compromised authority. Apple&\#x27;s support article 149555 offers only a manual certificate-chain workaround, and commenters report that OS updates can revert the edit and reintroduce the exposure. Homebrew-installed git and curl may behave differently, but that has not been confirmed in the supplied material.

hackernews · galadran · Oct 28, 11:03 · [Discussion](https://news.ycombinator.com/item?id=50271640)

**「Compromised eMudhra certificates and macOS trust behavior」** Certificate authority eMudhra revoked eight compromised intermediate certificates on October 21, 2026 after researchers found their private keys were weak enough to be recovered almost instantly \(tool-1-2\). Apple subsequently blocked the vulnerable certificates and said a macOS update for certain command-line tools was still in development \(tool-1-3\). Apple Support explains that macOS command-line tools including git and curl check certificates against /etc/ssl/cert.pem and do not check Apple&\#x27;s blocklist or whether such certificates have been revoked \(tool-1-1\).

**「Impact」** Developers and organizations relying on Apple&\#x27;s system git or other macOS utilities that use the OS trust store may not receive warnings when connecting to servers presenting eMudhra-chained certificates. The manual mitigation from Apple support article 149555 must be reapplied after OS updates that restore the revoked certificates.

**「Community discussion」** Commenters note the problem is not limited to git and affects other system utilities that trust macOS certificates, while one user speculates without evidence that the weak-key generation was intentional. Several commenters point to Apple support article 149555 as the vendor-recommended patch.

<details><summary>References</summary>
<ul>
<li><a href="https://support.apple.com/en-us/149555">About the compromised eMudhra intermediate CAs - Apple Support</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/mozilla-google-apple-block-compromised-emudhra-ca-certificates/">Mozilla, Google, Apple block compromised eMudhra CA certificates</a></li>
<li><a href="https://www.news18.com/tech/apple-blocks-vulnerable-emudhra-security-certificates-macos-fix-still-in-development-10397973.html">Apple Blocks Vulnerable eMudhra Security Certificates, macOS ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#macOS`, `#certificates`, `#git`, `#vulnerability`

---

<a id="item-tech-news-4"></a>
### [GitHub Octoverse 2026 reports record PRs, commits, and AI agent usage](https://simonwillison.net/2026/Oct/28/github-octoverse-2026/) ⭐️ 7.0/10

GitHub&\#x27;s 2026 Octoverse report shows merged pull requests climbing to 220 million per month, commits reaching 7.38 billion per month, and new repositories hitting 30.3 million per month. These record‑breaking metrics, driven largely by the rise of AI‑assisted agentic engineering, indicate that developers are increasingly using autonomous agents to create and merge code at unprecedented scale.

rss · Simon Willison · Oct 28, 16:45

**「Background」** Agentic engineering describes autonomous AI agents that plan, write, and execute code, a capability that has surged on GitHub as developers adopt AI tools. This trend builds on earlier AI‑assisted coding features introduced in previous years.

**「Impact」** Developers will need to adjust their workflows to review and validate AI‑generated code, as the surge in merged PRs and commits reflects higher reliance on autonomous agents.

**Tags**: `#GitHub`, `#Octoverse`, `#developer metrics`, `#AI agents`

---

<a id="item-tech-news-5"></a>
### [Amazon&\#x27;s Terk Terkowitz on AI Utility in Engineering Work](https://simonwillison.net/2026/Oct/28/terk-terkowitz/) ⭐️ 7.0/10

Amazon engineering leader Terk Terkowitz advised engineers that if their work does not benefit from current AI tooling, this should be treated as a valuable finding rather than a failure. He encouraged documenting the reasons, sharing insights with peers and managers, and working toward solutions, noting that explaining where AI does not yet help demonstrates the judgment Amazon seeks in developers.

rss · Simon Willison · Oct 28, 10:09

**「Background」** Amazon engineering leaders recently revised the software engineer role guidelines to emphasize outcomes over tool usage, reflecting AI&\#x27;s rapid impact on development. This policy shift frames the new advice that engineers should treat cases where AI does not help as documented findings rather than failures, encouraging critical evaluation and sharing of those insights.

**「Impact」** This guidance provides engineers and managers with a framework for critically evaluating AI integration in software development, potentially reducing pressure to adopt AI tools where they offer limited value and encouraging more thoughtful, evidence-based implementation decisions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aboutamazon.com/news/company-news/amazon-software-engineer-role-guideline-ai">An update from Amazon engineering leadership on the role of ...</a></li>
<li><a href="https://www.businessinsider.com/amazon-software-engineers-prioritize-results-over-ai-usage-2026-10">Amazon Tells Software Engineers to Prioritize Results Over AI ...</a></li>

</ul>
</details>

**Tags**: `#amazon`, `#ai`, `#software-engineering`, `#generative-ai`, `#agentic-engineering`

---

<a id="item-tech-news-6"></a>
### [Harvard AI safety researcher Stephen Casper hosts AMA on AI safeguards](https://www.reddit.com/r/MachineLearning/comments/1xhpnfs/ama_this_wednesday_stephen_cas_casper_harvard/) ⭐️ 7.0/10

An AMA with Harvard’s Stephen Casper on AI safeguards, incidents, and governance will take place on Wednesday, October 28, 2026, from 3 to 4 pm ET \(19:00 UTC, 20:00 CET\). Casper is an Assistant Professor of Public Policy at the Harvard Kennedy School and a Faculty Affiliate of the Harvard School of Engineering and Applied Sciences, where his research focuses on AI safety, risk, governance, and AI terrorism events; he earned his PhD at MIT and previously held a research residency with the UK AI Security Institute. The AMA thread will be posted by u/HarvardKennedy shortly before 3 pm ET with a dated photo for verification, and Casper will type his own answers; participants who cannot attend can submit questions in the comments for later carryover.

reddit · r/MachineLearning · /u/NeuralNomad87 · Oct 28, 14:30

**「Background」** The upcoming Reddit AMA features Stephen &quot;Cas&quot; Casper, an Assistant Professor of Public Policy at Harvard Kennedy School and Faculty Affiliate of the Harvard School of Engineering and Applied Sciences, who studies AI safeguards, incidents, and governance. His background includes a PhD from MIT and a research residency with the UK AI Security Institute, and the event is expected to cover AI safety, risk, governance, legislation, and AI terrorism events.

**「Community can ask Harvard expert about AI safeguards, incidents, governance」** The AMA on Wednesday 28 Oct 3‑4pm ET will let community members directly ask Harvard Assistant Professor Stephen Casper about AI safeguards, incidents, governance, legislation and AI terrorism events.

<details><summary>References</summary>
<ul>
<li><a href="https://agihunt.info/en/p/1a1780923b03428d36d699f7f7d">AMA: Harvard&#x27;s Stephen &quot;Cas&quot; Casper on AI… · AGI Hunt</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#Governance`, `#AMA`, `#Harvard`, `#AI research`

---

<a id="item-tech-news-7"></a>
### [PCA null-space injection lifts EmbeddingGemma-2 to \#1 on MAEB audio](https://www.reddit.com/r/MachineLearning/comments/1xho7pr/r_taking_embeddinggemma2_577m_from_rank_26_to_1/) ⭐️ 7.0/10

A Reddit experiment by /u/JeanMichelRanu reports that google/embeddinggemma-2 \(577M\) improved its MAEB audio macro score from 49.3% to 54.4% \(+5.1 points\) by injecting PCA-reduced Layer 2 and Layer 6 Conformer features into the model&\#x27;s unused 256d null space, with no training. The modified weights are available as BrunoHays/embeddinggemma-2-nullspace-audio, and the result reportedly moves the model from Rank \#26 to \#1 on MAEB audio-only \(\#16 to \#1 on full MAEB\), ahead of 8B-9B multimodal models. Text embeddings remain bit-for-bit unchanged and text-to-audio retrieval is stable within 0.05 points, but the method requires all 768 dimensions, with no Matryoshka truncation, and it harms speaker-ignoring audio tasks: SIBFLEURS drops from 57.2% to 21.3% and MInDS14 from 97.6% to 88.3%. The finding is a single unverified Reddit report and has not been independently replicated.

reddit · r/MachineLearning · /u/JeanMichelRanu · Oct 28, 13:34

**「Background」** MAEB is the 30-task audio subset of the MTEB embedding leaderboard. EmbeddingGemma-2&\#x27;s terminal projection maps 512d text hidden states to 768d, so text embeddings occupy only a 512d subspace, leaving 256 orthogonal directions that text never uses. Prior layer-probing work cited in the post shows speaker, prosodic, and semantic attributes peak at different depths in speech encoders, which the experiment exploits by injecting PCA-compressed intermediate Conformer layers into those unused directions.

**「Impact」** Affected developers can download the modified weights \(BrunoHays/embeddinggemma-2-nullspace-audio\) and use them for text tasks without change, since text embeddings remain bit-for-bit identical. However, the method requires all 768 dimensions, eliminating 512/256/128 truncation options, and it harms audio tasks that should ignore speaker voice, with SIBFLEURS dropping from 57.2% to 21.3% and MInDS14 from 97.6% to 88.3%.

**Tags**: `#EmbeddingGemma`, `#audio embeddings`, `#null space`, `#PCA`, `#MTEB`

---

<a id="item-tech-news-8"></a>
### [Human advantage narrow in cocktail‑party speech separation test](https://www.reddit.com/r/MachineLearning/comments/1xhuado/cocktailparty_audio_as_a_reverse_turing_test/) ⭐️ 7.0/10

The experiment evaluated human transcription accuracy against eight ASR models on 40 synthetic cocktail‑party audio clips, finding humans achieved a mean word accuracy of 0.71 versus 0.54 for Gemini \(and 0.55 for Qwen3‑ASR\). The average gap of 0.13 \(95 % CI +0.03 to +0.23\) and overlapping pass rates \(77 % humans vs. 55 % Gemini\) make the task too easy for machines to serve as a reliable audio CAPTCHA. The study used 146 human transcriptions from 18 sessions, mostly native English speakers, and limited the models to Whisper base/small, Vosk, Wav2Vec2, Qwen3‑ASR 0.6B, Parakeet CTC 0.6B, and Gemini 3.8 Flash, noting the small sample and synthetic setup as key limitations.

reddit · r/MachineLearning · /u/cloud\_kj · Oct 28, 17:17

**「Background」** The &quot;cocktail party problem&quot; describes isolating a target speaker from overlapping speech, a challenge that humans typically solve well. Reverse‑Turing‑test audio CAPTCHAs aim to exploit this human advantage to block automated bots. This experiment builds on prior ASR benchmarks and audio CAPTCHA concepts by directly comparing human performance to eight state‑of‑the‑art speech models on a controlled synthetic dataset.

**「Impact」** Because the performance gap is insufficient for a dependable CAPTCHA, the method cannot be used as a robust bot‑prevention barrier, and the narrow margin suggests that future audio CAPTCHAs will need harder tasks or larger model variations. Additionally, the instruction prompt raised Gemini’s accuracy from 0.34 to 0.54, highlighting how prompt engineering can affect model outcomes on this type of separation task.

**Tags**: `#speech recognition`, `#ASR`, `#reverse Turing test`, `#audio CAPTCHA`, `#benchmark`

---

<a id="item-tech-news-9"></a>
### [Generic feedback matches self-critiques in hindsight self-distillation for financial reasoning](https://www.reddit.com/r/MachineLearning/comments/1xhv8yp/how_much_does_the_hint_matter_a_generic_feedback/) ⭐️ 7.0/10

Researchers studied hindsight self-distillation on GPT-OSS-20B for multi-step financial reasoning. The student model identifies its first wrong step and writes a critique; a frozen copy conditioned on the prefix plus critique is distilled back under reverse KL. Replacing the critique with a fixed generic feedback line achieves the same ~3-point gain, and critiques from a 6× larger model do not materially improve performance. The method, Fin-SD, matches OPSD from full reference solutions using 9.5% fewer tokens.

reddit · r/MachineLearning · /u/jhzyu · Oct 28, 17:52

**「Background」** Hindsight self-distillation trains a model on its own corrected trajectories by conditioning on prefixes and critiques. Prior work such as OPSD \(Optimal Policy Self-Distillation\) uses full reference solutions, which are token-intensive. This paper investigates whether the critique content itself matters or if the positional signal of knowing where the error occurred is sufficient.

**「Impact」** The finding that a generic feedback line matches self-written critiques suggests hindsight distillation&\#x27;s value lies primarily in providing positional error information rather than detailed corrective reasoning. This could reduce token costs and simplify training pipelines for multi-step reasoning tasks, though the result is demonstrated on a single model \(GPT-OSS-20B\) and financial reasoning domain.

---

<a id="item-tech-news-10"></a>
### [Enterprise AI GPU Underutilization Survey Findings](https://venturebeat.com/infrastructure/ai-bubble-update-79-of-companies-say-their-gpus-sit-idle-at-least-half-the-time-yet-most-plan-new-ai-platforms) ⭐️ 7.0/10

A VentureBeat survey of global enterprises reveals that 79% of companies have GPUs operating at less than 50% average utilization and 91% of AI infrastructure investments have never undergone formal ROI audits. Despite this underutilization, 70% of firms with low GPU usage still plan to purchase and deploy new AI compute platforms within the next 12 months. The findings highlight a disconnect between heavy spending on AI hardware and effective monitoring of its financial return.

telegram · zaihuapd · Oct 28, 02:37

**「Enterprise AI Infrastructure Utilization」** VentureBeat&\#x27;s survey of 573 technical leaders found that enterprises are deploying AI agents faster than controls can govern them, with 86% of AI chips running below full capacity, highlighting a growing gap between AI infrastructure investment and actual utilization.

**「Impact」** Enterprises are allocating capital to AI hardware that sits idle much of the time and lacks ROI scrutiny, resulting in wasted spending and inefficient resource use; organizations should implement utilization monitoring and formal ROI audits before further AI compute purchases.

<details><summary>References</summary>
<ul>
<li><a href="https://verdice.news/article/86-of-in-house-ai-chips-run-half-empty-survey-qxpvpdw">86% of In-House AI Chips Run Half -Empty: Survey | Verdice News</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#GPU utilization`, `#enterprise AI`, `#ROI`, `#technology industry`

---

<a id="item-tech-news-11"></a>
### [CXMT Pursues HBM3E Production Despite Low Yields](https://www.reuters.com/world/china/chinas-cxmt-start-advanced-ai-memory-production-despite-poor-yields-sources-say-2026-10-28/) ⭐️ 7.0/10

According to two sources, Chinese memory maker CXMT has sent HBM3E samples to several domestic AI chip design companies and plans limited production within about two months, though its reported yield may be only 20% to 30%, far below SK Hynix&\#x27;s roughly 70%. The reported move is meant to ease a domestic AI memory shortage after US export controls, though the yields and performance remain early concerns.

telegram · zaihuapd · Oct 28, 06:19

**「HBM3E and Supply Context」** HBM3E is an advanced high-bandwidth memory used in AI accelerators, and SK Hynix has been a leading supplier with a much higher reported yield. CXMT&\#x27;s reported low-yield HBM3E effort comes as US export controls have contributed to severe domestic AI memory shortages.

**「Potential Domestic Supply Impact」** For domestic AI chip design companies, the reported samples offer a potential domestic source of advanced memory, but the low yield and performance closer to SK Hynix&\#x27;s prior HBM3 could limit immediate capacity or usable product quality. Buyers may face higher prices than comparable overseas memory, making adoption slower or more costly.

**Tags**: `#HBM3E`, `#CXMT`, `#AI memory`, `#semiconductor manufacturing`, `#China tech`

---

<a id="item-tech-news-12"></a>
### [Apple Unveils MacBook Pro with PROLED XDR Display and Touch Support](https://www.apple.com/newsroom/2026/10/apple-unveils-groundbreaking-macbook-pro-with-proled-xdr-display/) ⭐️ 7.0/10

Apple announced new 14- and 16-inch MacBook Pro models featuring a PROLED XDR tandem OLED display with 2,000-nit peak brightness and 10,000,000:1 contrast ratio, marking the first Macs with touchscreen support. The laptops are powered by M5 Pro and M5 Max chips, are thinner and lighter than predecessors, and claim up to 24 hours of battery life. Pre-orders begin October 28 with availability November 6; the 14-inch model starts at 22,999 RMB and the 16-inch at 27,999 RMB.

telegram · zaihuapd · Oct 28, 17:16

**「Background」** Previous MacBook Pro models did not offer tandem OLED displays or built-in touchscreen input, so Apple describes both features as firsts for the Mac line. This context explains why the display technology and input method are presented as changes to the existing product.

**「Impact」** The addition of touch input changes the Mac interaction model for the first time, requiring developers to consider touch targets and gestures in macOS apps. The PROLED XDR display&\#x27;s 2,000-nit peak brightness and 10,000,000:1 contrast directly benefit HDR video editing, color grading, and high-dynamic-range content creation workflows. The claimed 24-hour battery life, if realized in real-world use, would significantly extend mobile productivity for professionals.

**Tags**: `#hardware`, `#apple`, `#laptop`, `#display`, `#semiconductor`

---

<a id="item-tech-news-13"></a>
### [OpenAI Bundles Up to $500 Monthly API Credits with ChatGPT Pro and Business](https://developers.openai.com/api/docs/guides/chatgpt-api-credits) ⭐️ 7.0/10

OpenAI has added a monthly API credit benefit for eligible ChatGPT Pro and Business subscribers, activated by linking an API organization in ChatGPT or the API Platform. Pro subscribers on the $100, $200, and $500 plans receive matching monthly credits of $100, $200, and $500. Business subscribers receive $20 per Standard seat and $100 per Premium seat, with a workspace-wide cap of $500 per month. The credits are a subscription perk tied to the user&\#x27;s plan, not a change to standalone API pricing.

telegram · zaihuapd · Oct 29, 01:12

**「背景」** OpenAI 此前将 ChatGPT 订阅服务与 API 访问权分开定价，开发者和企业需单独为 API 使用付费。此次将 API 额度纳入 ChatGPT Pro 和 Business 订阅权益，是 OpenAI 首次将两项服务直接捆绑，旨在降低开发者的使用门槛并推动 API 生态增长。

**「Impact」** API users on these plans can reduce their out-of-pocket OpenAI API costs, but they must manually link an API organization to activate the credits. Business workspaces are capped at $500 per month regardless of the number of paid seats, so larger teams may hit the ceiling before receiving per-seat credits for every seat.

**Tags**: `#OpenAI`, `#API`, `#ChatGPT`, `#pricing`, `#developer-tools`

---

## Financial News

<a id="item-finance-news-1"></a>
### [长鑫科技正式纳入上证指数并位列第一大权重股](https://m.gelonghui.com/live/2733034) ⭐️ 8.0/10

Changxin Technology has been added to the Shanghai Stock Exchange composite indices, becoming the top‑weight stock in both with weights of 4.67% and 15.74%, and the inclusion aligns with a new rule limiting single‑stock weights to 15%.

telegram · zaihuapd · Oct 28, 08:03

**Tags**: `#Index Inclusion`, `#Weight Adjustment`, `#Regulatory Change`, `#China A‑share`

---

<a id="item-finance-news-2"></a>
### [South Korea fines Apple and Google over app store practices](https://appleinsider.com/articles/26/10/28/south-korea-becomes-the-latest-to-fine-apple-and-google-millions-over-their-app-stores) ⭐️ 7.0/10

South Korea&\#x27;s communications regulator fined Apple $15.5 million and Google $32 million for restricting third-party app payments and delaying app reviews, ordering both to allow external payment links under a 2021 telecommunications law.

telegram · zaihuapd · Oct 28, 12:30

**「South Korea&\#x27;s 2021 law forced app stores to allow third-party payments」** South Korea amended its Telecommunications Business Act in 2021 to stop app store operators from forcing developers to use their own payment systems, making it the first country to do so.

**「Impact」** South Korean app developers are the directly affected party, as the regulator&\#x27;s order requires Apple and Google to permit external payment links and improve app review processes, which could lower developers&\#x27; payment processing costs and reduce review delays.

<details><summary>References</summary>
<ul>
<li><a href="https://tech-quire.com/articles/south-korea-fines-google-apple-app-payment/">South Korea fines Google and Apple 63.7 billion won over in- app ...</a></li>
<li><a href="https://www.aa.com.tr/en/asia-pacific/south-korea-fines-google-apple-45m-over-app-store-payment-policies/4103750">South Korea fines Google, Apple $45M over app store payment ...</a></li>
<li><a href="https://sg.news.yahoo.com/korea-considers-50-5-million-020842524.html">South Korea warns Google, Apple of possible fines over apps marketing</a></li>
<li><a href="https://www.euronews.com/2026/10/28/south-korea-fines-google-apple-for-pushing-app-developers-onto-their-payment-systems">South Korea fines Google , Apple for pushing app developers onto...</a></li>
<li><a href="https://finance.yahoo.com/technology/articles/south-korea-fines-google-apple-095158608.html">South Korea fines Google and Apple over unfair app market practices</a></li>
<li><a href="https://www.aa.com.tr/en/asia-pacific/south-korea-fines-google-apple-45m-over-app-store-payment-policies/4103750">Anadolu Ajansı: South Korea fines Google , Apple $45M over app ...</a></li>

</ul>
</details>

**Tags**: `#South Korea regulation`, `#App Store payments`, `#antitrust enforcement`, `#Apple`, `#Google`

---

<a id="item-finance-news-3"></a>
### [Google 将 AI 模式搜索广告推向全球市场](https://techcrunch.com/2026/10/28/google-expands-ai-search-ads-globally-as-core-ad-growth-slows/) ⭐️ 7.0/10

Google expands AI mode search ads globally amid a slowdown in core search ad growth, highlighting its shift toward generative AI monetization in a key revenue segment.

telegram · zaihuapd · Oct 29, 01:43

**Tags**: `#Google`, `#AI search ads`, `#earnings`, `#digital advertising`, `#Alphabet`

---