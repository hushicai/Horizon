---
layout: default
title: "Horizon Summary: 2026-10-24 (EN)"
date: 2026-10-24
lang: en
---

> From 33 items, 10 important content pieces were selected

---

**Technology News**
1. [Amazon Trainium Adds Native PyTorch Training Support](#item-tech-news-1) ⭐️ 8.0/10
2. [iPhone hack claimed on Hacker News, lacking technical exposition](#item-tech-news-2) ⭐️ 7.0/10
3. [Now Google says it might use your Gmail and Google Photos data to target ads](#item-tech-news-3) ⭐️ 7.0/10
4. [Kimi K3.1 Pro API launch with pricing, benchmarks, and pending open weights](#item-tech-news-4) ⭐️ 7.0/10
5. [ByteDance Volcano Engine releases Seedance 2.5 4K video model with draft mode](#item-tech-news-5) ⭐️ 7.0/10
6. [DeepSeek Agent AI Comments Flood Bilibili via Open-Source Plugin](#item-tech-news-6) ⭐️ 7.0/10
7. [China State Council Issues Guidelines to Curb AI Job Displacement](#item-tech-news-7) ⭐️ 7.0/10
8. [Sweden&\#x27;s government office bans ChatGPT and Claude, mandates Microsoft Copilot](#item-tech-news-8) ⭐️ 7.0/10
9. [Kimi K3.1-Pro: 3-Trillion-Parameter Open-Weight LLM Released](#item-tech-news-9) ⭐️ 7.0/10

**Financial News**
1. [EU Revokes Anti-Dumping Duties on Chinese Solar Glass](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Amazon Trainium Adds Native PyTorch Training Support](https://newsletter.semianalysis.com/p/amazons-trainium-takes-a-strike-at) ⭐️ 8.0/10

Amazon&\#x27;s Trainium chip now offers native PyTorch support for training workloads, positioning it as an alternative to GPUs for machine learning training. The update includes high-quality CI integration and TorchTitan compatibility, though the source does not specify release dates or independent benchmarks. This is a vendor-announced capability rather than an independently verified shipment.

rss · Semianalysis · Oct 23, 19:06

**「Trainium Training Background」** AWS Trainium had previously been positioned as an AI accelerator for training and inference workloads, with developers using the Neuron Kernel Interface to access its custom instruction set. The newly reported native PyTorch training support adds a more standard software path to that earlier AI-specific design.

**「Impact」** Developers using PyTorch can now target Trainium hardware for training without translation layers, potentially reducing cost and dependency on NVIDIA GPUs. However, performance parity and ecosystem maturity remain unproven.

**「Community Discussion」** No community comments are available for this announcement.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aboutamazon.com/news/aws/aws-trainium-graviton-ai-chips-explained">AWS Trainium and Graviton chips: How Amazon powers AI and ...</a></li>
<li><a href="https://aws.amazon.com/ai/machine-learning/trainium/">AI Accelerator - AWS Trainium - AWS - aws.amazon.com</a></li>

</ul>
</details>

**Tags**: `#Trainium`, `#ML hardware`, `#PyTorch`, `#AI training`, `#Amazon`

---

<a id="item-tech-news-2"></a>
### [iPhone hack claimed on Hacker News, lacking technical exposition](https://blog.calif.io/p/iphone) ⭐️ 7.0/10

The Hacker News post &\#x27;Today, we hacked what we&\#x27;d set out to hack: the iPhone&\#x27; claims a hack of the iPhone but provides no technical details about the method, version, or impact available in the excerpt. The discussion references jailbreak, Lockdown mode, and Apple&\#x27;s ecosystem restrictions, but the source material is too sparse to confirm specifics or measure real-world effect. Without technical exposition, the post remains an unsubstantiated claim rather than a verified capability.

hackernews · pavel\_lishin · Oct 23, 16:21 · [Discussion](https://news.ycombinator.com/item?id=50211474)

**「Background」** The article reports that a team has managed to hack the iPhone, achieving root access that bypasses Apple&\#x27;s built‑in security. This breakthrough builds on earlier iOS versions that limited unauthorized modifications, making the current exploit a notable advancement in iPhone security research.

**「Community Discussion」** A commenter reports that Apple can detect jailbreaks and lock access to iCloud and iMessage, effectively reducing the iPhone to an iPod touch if updates are applied. This reflects the commenter&\#x27;s experience and is distinct from the hack&\#x27;s technical status.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.calif.io/p/iphone">iPhone - Calif Newsletter</a></li>

</ul>
</details>

**Tags**: `#iPhone security`, `#iOS jailbreak`, `#cybersecurity`, `#mobile security`, `#Apple ecosystem`

---

<a id="item-tech-news-3"></a>
### [Now Google says it might use your Gmail and Google Photos data to target ads](https://www.theverge.com/tech/1017600/google-personal-intelligence-privacy-policy-ads-update) ⭐️ 7.0/10

Google updates privacy policy to permit using Gmail and Google Photos data for ad targeting, raising significant privacy concerns.

hackernews · JustSkyfall · Oct 23, 19:34 · [Discussion](https://news.ycombinator.com/item?id=50214218)

**Tags**: `#google-privacy`, `#data-usage`, `#ads-targeting`, `#gmail`, `#google-photos`

---

<a id="item-tech-news-4"></a>
### [Kimi K3.1 Pro API launch with pricing, benchmarks, and pending open weights](https://simonwillison.net/2026/Oct/23/kimi-k31-pro/) ⭐️ 7.0/10

Moonshot launched Kimi K3.1 Pro on the Kimi API on October 23, 2026, offering a competitive API model priced at $2.00 per million input tokens and $10 per million output tokens, with a faster &\#x27;Highspeed&\#x27; variant costing twice as much except for input token cache hits, which carry the base rate. The model is not yet open weights, but Moonshot promises full weight release by November 4, 2026. Artificial Analysis scored it 55, placing it behind only Claude Opus 5.5 \(58\) and ahead of several frontier models, marking the highest score yet for a soon-to-be open weight model.

rss · Simon Willison · Oct 23, 19:40

**「Kimi K3.1 Pro Launch Details」** Moonshot AI&\#x27;s Kimi K3.1 Pro has been introduced on the Kimi API as its latest large language model generation. The model is currently available only as an API service, with full open-weight release scheduled for November 4, 2026. A &\#x27;Highspeed&\#x27; variant offers 2-3x faster inference at double the pricing tier compared to standard versions.

**「Impact」** Developers benefit from a frontier-competitive model at half the cost of Claude Opus 5.5, but the open-weights delay until November 4, 2026 postpones self-hosting compatibility for workloads requiring full model access.

**Tags**: `#Kimi K3.1 Pro`, `#LLM API`, `#AI benchmarks`, `#model pricing`

---

<a id="item-tech-news-5"></a>
### [ByteDance Volcano Engine releases Seedance 2.5 4K video model with draft mode](https://mp.weixin.qq.com/s/yUa8oh-IWfl5lDQzGSKWeg) ⭐️ 7.0/10

ByteDance&\#x27;s Volcano Engine has released Seedance 2.5 4K, the latest version of its video generation model, currently available only to select enterprise customers for trial. The model supports 4K output with 10-bit color depth and a Draft mode that generates 480P samples for storyboard verification before producing 4K final videos. ByteDance says specialized training improves facial expressions, subtle movements, and visual detail, particularly in film and television dialogue scenes. A broader public release has not been confirmed.

telegram · zaihuapd · Oct 23, 08:27

**「Seedance 2.5 4K Background」** The release extends ByteDance&\#x27;s Fireworks Engine Seedance video-generation line with a higher-resolution 4K model and enhanced detail. It builds on earlier iterations of the Seedance series, while the supplied source does not describe the prior version&\#x27;s specifications in detail.

**「Impact」** Enterprise customers in the trial can test 4K video generation using a 480P draft workflow, but general availability, pricing, and compatibility with other tools remain unannounced, so other users cannot yet access the model.

**Tags**: `#AI`, `#Video Generation`, `#Machine Learning`, `#ByteDance`, `#4K Model`

---

<a id="item-tech-news-6"></a>
### [DeepSeek Agent AI Comments Flood Bilibili via Open-Source Plugin](https://mp.weixin.qq.com/s/MBrJeHsJ7nIql0PCVCIxgA) ⭐️ 7.0/10

Developer c1overzz released the open-source plugin dsh-bili-scroll, which lets DeepSeek Agent automatically search Bilibili videos, read captions, and post comments. Users adopted a unified whale-girl avatar and persona called &\#x27;Big Fat Fish,&\#x27; causing the technology section&\#x27;s comment sections to be flooded, with some videos receiving more comments than views. In response, another developer open-sourced dafeiyu-cleaner, a browser extension that filters and hides AI-generated comments based on nickname, avatar, and comment patterns, operating locally without deleting real comments.

telegram · zaihuapd · Oct 23, 11:10

**「Background」** DeepSeek Agent is an AI agent developed by DeepSeek that can perform tasks such as web browsing and content generation. Bilibili is a popular Chinese video-sharing platform known for its active comment culture, where users often engage in real-time discussions during video playback.

**「Impact」** This incident demonstrates how AI agents can be used to automate social media interactions at scale, raising concerns about the authenticity of online discourse. It also highlights the need for AI-content moderation tools, as shown by the rapid community response in developing filtering extensions.

**Tags**: `#AI agents`, `#open source`, `#social media automation`, `#Bilibili`, `#community tools`

---

<a id="item-tech-news-7"></a>
### [China State Council Issues Guidelines to Curb AI Job Displacement](https://mp.weixin.qq.com/s/St8URoMYcV-voM7kLAK3Bw) ⭐️ 7.0/10

China&\#x27;s State Council has issued guidelines titled &\#x27;Opinions on Adapting to AI Development to Support Building Employment-Friendly Development Approaches,&\#x27; aimed at slowing AI-driven job displacement. The guidelines direct prioritizing AI deployment in labor-short and high-risk environments, while urging caution in applying AI to labor-intensive industries. Enterprises are encouraged to explore establishing unemployment buffer periods, notifying affected workers in advance, and providing retraining and job transition support.

telegram · zaihuapd · Oct 23, 12:54

**「Policy Context: State Council AI Employment Mitigation Guidelines」** The State Council of China issued official guidelines titled &\#x27;关于适应人工智能技术发展助力构建就业友好型发展方式的意见&\#x27; \(Opinion on Adapting Artificial Intelligence Development to Build Employment-Friendly Development\), requiring prioritized AI adoption in labor-scarce and hazardous occupations while encouraging unemployment buffer systems and transition support for affected workers. These measures aim to balance AI advancement with employment protection across sectors. The policy represents a coordinated national strategy to manage AI&\#x27;s labor market impacts through targeted sectoral deployment and worker transition mechanisms.

**「Implications for AI Adoption」** The policy may slow AI adoption in labor-intensive sectors within China, as companies are advised to proceed cautiously and implement worker protection measures. Organizations deploying AI in China should prepare for potential requirements to offer advance notice and retraining support to affected employees, particularly in roles not classified as labor-short or high-risk.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gov.cn/zhengce/zhengceku/202610/content_7084108.htm">国务院办公厅关于适应人工智能技术发展助力构建就业友好型发展方式的...</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#employment`, `#China`, `#technology regulation`, `#AI ethics`

---

<a id="item-tech-news-8"></a>
### [Sweden&\#x27;s government office bans ChatGPT and Claude, mandates Microsoft Copilot](https://www.sverigesradio.se/artikel/chat-gpt-och-claude-forbjuder-regeringskansliet) ⭐️ 7.0/10

Sweden&\#x27;s Regeringskansliet will block ChatGPT and Claude on employee devices starting next Monday, requiring transition to vetted AI tools such as Microsoft Copilot due to security risks. The directive follows an earlier restriction on DeepSeek and aligns with similar bans at the Swedish Tax Authority and the National Institutions Authority \(SiS\), while Kronofogden evaluates whether to extend the ban. The digital chief&\#x27;s internal site warned that using unregistered AI services may jeopardize information security, though some staff may still access ChatGPT and Claude through a domestic platform.

telegram · zaihuapd · Oct 23, 14:11

**「Background」** Public agencies are increasingly limiting unvetted third‑party AI tools to protect information security, a practice that began with earlier restrictions such as the Swedish government office&\#x27;s prior ban on DeepSeek and has now expanded to ChatGPT and Claude.

**「Impact」** Government office employees must transition from ChatGPT and Claude to Microsoft Copilot for AI-assisted tasks, directly restricting use of the banned platforms on work devices and potentially affecting productivity and compliance timelines.

**Tags**: `#AI policy`, `#enterprise AI`, `#government procurement`, `#security concerns`, `#Microsoft Copilot`

---

<a id="item-tech-news-9"></a>
### [Kimi K3.1-Pro: 3-Trillion-Parameter Open-Weight LLM Released](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 7.0/10

Moonshot AI released Kimi K3.1-Pro, a 3-trillion-parameter open-weight LLM with 1-million-token context, the first model in the K3.1 series. It achieves 65.7% on Terminal-Bench 4.0 for coding, 92.7% on BenchCAD for 3D modeling, and improved financial modeling scores, while a Highspeed variant runs 2–3x faster. The model&\#x27;s internal hallucination rate dropped from 23.4% to 8.3%, though the source notes this does not reflect everyday usage error rates. Full weights are planned for release before November 4, 2026, and the model is currently accessible via Kimi, Work, Code, and API.

telegram · zaihuapd · Oct 23, 17:14

**「Background」** Kimi K3.1-Pro is built on the K3 architecture with expanded training scale, succeeding the earlier K3 model. The K3 series established Kimi&\#x27;s direction in large-scale open-weight models, and K3.1-Pro represents the first release in the upgraded K3.1 line.

**「Impact」** Organizations in software development, 3D design, and finance can now evaluate a competitive open-weight model against proprietary alternatives, with the full weight release planned for late 2026 enabling on-premises deployment and further fine-tuning.

**Tags**: `#Artificial Intelligence`, `#Large Language Models`, `#Open Source`, `#Software Engineering`, `#Technology News`

---

## Financial News

<a id="item-finance-news-1"></a>
### [EU Revokes Anti-Dumping Duties on Chinese Solar Glass](https://www.163.com/dy/article/L9R94K6105484D40.html) ⭐️ 7.0/10

The European Commission revoked anti-dumping and anti-subsidy duties on Chinese solar glass, effective October 22, 2026, with rates as high as 84.2%. Duties paid since July 22, 2025, can be refunded without interest.

telegram · zaihuapd · Oct 23, 06:54

**「Background」** The EU originally imposed these duties when Chinese imports held about 30.5% of the EU solar glass market, but now Chinese imports account for only about 3% and no active EU producers remain.

**「Impact」** Chinese solar glass exporters are freed from tariffs of up to 84.2% on EU sales, while European solar panel manufacturers that import Chinese glass may see lower input costs, though Chinese imports hold only about 3% of the EU market.

**Tags**: `#EU trade policy`, `#China solar industry`, `#anti-dumping duties`, `#solar supply chain`, `#tariff revocation`

---