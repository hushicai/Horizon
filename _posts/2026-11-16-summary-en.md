---
layout: default
title: "Horizon Summary: 2026-11-16 (EN)"
date: 2026-11-16
lang: en
---

> From 36 items, 10 important content pieces were selected

---

**Technology News**
1. [Meta FAIR &amp; NYU Unbundle Vision Encoding in Multimodal LLMs](#item-tech-news-1) ⭐️ 8.0/10
2. [Open-source tuner makes Pageable cudaMemcpy 5x faster on B300 GPUs](#item-tech-news-2) ⭐️ 8.0/10
3. [Jensen Huang may return as Nvidia CEO amid leadership crisis](#item-tech-news-3) ⭐️ 8.0/10
4. [Protomaps makes self-hosting map tiles cheap and easy](#item-tech-news-4) ⭐️ 7.0/10
5. [Datasette 1.0a43 adds streaming renderers and view transitions](#item-tech-news-5) ⭐️ 7.0/10
6. [Interactive Airflow 3 ML orchestration tutorial published in English and Spanish](#item-tech-news-6) ⭐️ 7.0/10
7. [Meituan open-sources LongCat-2.5, claims training without Nvidia GPUs](#item-tech-news-7) ⭐️ 7.0/10

**Financial News**
1. [Lutnick faces ethics scrutiny as Cantor cuts Nvidia stake](#item-finance-news-1) ⭐️ 7.0/10
2. [Electric Bike Certification Pause Limits Consumer Registration](#item-finance-news-2) ⭐️ 7.0/10
3. [美法官驳回美光三星等 DRAM 价格操纵案撤诉动议](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Meta FAIR &amp; NYU Unbundle Vision Encoding in Multimodal LLMs](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR and NYU trained over 200 multimodal large language models from scratch to test whether vision encoder pretraining is needed. They found that pretraining the encoder is optional, but vision‑only parameters are required for performance, as shown on Qwen3‑1.7B/4B models with 0.4 B vision capacity across 16 VQA and 12 language benchmarks. Models without dedicated vision parameters lag by up to threefold in compute and underperform on VQA.

reddit · r/MachineLearning · /u/trungh98 · Nov 15, 17:38

**「Background」** Prior work assumed that vision encoders required separate pretraining and that they bundled pretraining, vision‑only parameters, and placement before the LLM. This study isolates each choice by training models from scratch on the same data and compute budget.

**「Impact」** Developers can omit costly encoder pretraining while preserving VQA accuracy, provided they include dedicated vision‑only parameters, simplifying training pipelines and reducing compute needs.

**Tags**: `#multimodal LLMs`, `#vision encoders`, `#architecture search`, `#empirical study`, `#Meta FAIR`

---

<a id="item-tech-news-2"></a>
### [Open-source tuner makes Pageable cudaMemcpy 5x faster on B300 GPUs](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 8.0/10

An open-source tool called cudamemcpy-tuner makes pageable host-to-device memory copies up to 5x faster on NVIDIA B300 \(Blackwell\) GPUs. The author demonstrates the speedup with a reproducible PyTorch benchmark, where copying a 1 GB tensor improves from 10.2 GB/s to 51.5 GB/s. The tool requires no changes to existing code because pageable memory is the default in PyTorch. The blog post, benchmark code, and GitHub repository are publicly available.

reddit · r/MachineLearning · /u/makneeee · Nov 15, 18:20

**「Background」** Pageable host memory is the default allocation mode in PyTorch and CUDA, but host-to-device transfers using pagable memory are substantially slower than those using pinned \(page-locked\) memory, which NVIDIA&\#x27;s documentation has long recommended for maximizing bandwidth. This performance gap exists because the CUDA driver must stage pagable transfers through a temporary pinned buffer, adding overhead. On newer GPU architectures like the B300 \(Blackwell\), where aggregate bandwidth has increased significantly, the gap between pagable and pinned transfer rates remains a known bottleneck for workloads that do not explicitly pin host memory.

**「Impact」** ML practitioners using PyTorch on B300 GPUs can now achieve dramatically faster host-device data transfers by running their workloads through the tuner, without needing to switch to pinned memory. The tool is specifically tuned for the B300 architecture, so users on other NVIDIA GPUs should verify compatibility before relying on it.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/how-optimize-data-transfers-cuda-cc/">How to Optimize Data Transfers in CUDA C/C++ | NVIDIA Technical...</a></li>

</ul>
</details>

**Tags**: `#cuda`, `#gpu-optimization`, `#memory-transfer`, `#pytorch`, `#blackwell-architecture`

---

<a id="item-tech-news-3"></a>
### [Jensen Huang may return as Nvidia CEO amid leadership crisis](https://www.ft.com/content/0f30a230-4d66-481b-a4fd-3a4ed0c45855) ⭐️ 8.0/10

Jensen Huang is reportedly considering a return to the Nvidia CEO role after resigning last week following two extramarital affairs, one allegedly involving a Chinese spy, which sparked concerns over AI chip exports to China. Allies have formed a Silicon Valley executive “war room” to lobby the board and seek White House backing, with a petition gathering over 156,000 signatures. The board has also begun discussions with Arm CEO Rene Haas as a potential successor.

telegram · zaihuapd · Nov 16, 01:06

**「Background」** The potential return follows Jensen Huang&\#x27;s resignation as Nvidia&\#x27;s president and CEO after reports of extramarital relationships, including one with a woman U.S. intelligence determined was a Chinese spy. Nvidia said Chief Financial Officer Colette Kress would serve as interim CEO, leaving the company to manage both a succession process and national-security scrutiny.

**「Potential export policy shift」** A return of Huang could lead Nvidia to revise its AI chip export controls to China, affecting customers and partners dependent on those products.

<details><summary>References</summary>
<ul>
<li><a href="https://tech.yahoo.com/general/breaking-news/article/nvidia-ceo-jensen-huang-resigns-after-extramarital-affairs-raise-national-security-concerns-140401302.html">Nvidia CEO Jensen Huang resigns after extramarital affairs ...</a></li>
<li><a href="https://www.nytimes.com/2026/11/11/technology/jensen-huang-nvidia-affair.html">Jensen Huang Said to Have Had Relationship With Nvidia ...</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#AI`, `#Semiconductor`, `#Leadership`, `#Geopolitics`

---

<a id="item-tech-news-4"></a>
### [Protomaps makes self-hosting map tiles cheap and easy](https://bruceroettgers.eu/blog/protomaps/) ⭐️ 7.0/10

A blog post by Bruce Roettgers explains how Protomaps, an open-source vector tile format and tooling, has made self-hosting map tiles inexpensive and straightforward. Protomaps uses the PMTiles format — a single-file archive of vector tiles — that can be stored on object storage like Cloudflare R2 and served via edge workers, eliminating per-request API fees from providers such as Mapbox or Google Maps. The author demonstrates that a global base map fits in tens of gigabytes and costs pennies to host, enabling side projects and privacy-sensitive applications to run their own map infrastructure.

hackernews · bcye · Nov 15, 19:26 · [Discussion](https://news.ycombinator.com/item?id=50509837)

**「Background」** Traditional web maps rely on raster or vector tiles served from commercial APIs that charge per map load and require API keys. OpenStreetMap provides the underlying geographic data, but generating and hosting tiles has historically required significant server resources. Protomaps packages OpenStreetMap data into PMTiles — a single SQLite-based file per region or the whole planet — that can be served statically from cheap object storage with HTTP Range requests, removing the need for a tile server.

**「Impact」** Developers can now build map-based applications — such as a Wikipedia walking game that renders live street maps on printed cards — without incurring recurring API costs or exposing user location data to third parties. The approach also reduces load on public tile infrastructure and gives full control over styling, access control, and offline availability.

**「Community discussion」** Commenters note OpenFreeMap as a similar free hosted alternative with no API keys or limits. One developer reports using Cloudflare R2 and Workers for the same self-hosted pattern, and mentions the &\#x27;gloss&\#x27; CLI tool for inspecting PMTiles files. A limitation raised is that high-resolution satellite imagery grows to hundreds of terabytes at zoom levels beyond 17, making full global offline coverage impractical for small budgets. Cloudflare&\#x27;s improved Range request support is cited as a recent enabler.

**Tags**: `#self-hosting`, `#open-source`, `#mapping`, `#web-development`, `#infrastructure`

---

<a id="item-tech-news-5"></a>
### [Datasette 1.0a43 adds streaming renderers and view transitions](https://simonwillison.net/2026/Nov/15/datasette/) ⭐️ 7.0/10

Datasette 1.0a43 adds streaming support for output renderers, enabling the built‑in TSV and CSV export mechanisms to stream rows via the new Response.stream\(\) method and allowing plugins to register streaming renderers. The release also includes security fixes, including a GitHub‑advisory‑listed issue where private stored queries could be exposed, revealing their titles and SQL. Additionally, CSS multi‑page view transitions have been added, providing smoother navigation on Safari and Chrome, with Firefox support expected in Firefox 162 on December 8 2026. The 1.0 milestone is now 53 % complete.

rss · Simon Willison · Nov 15, 23:20

**「Background」** Datasette 1.0a43 moves the project closer to its 1.0 milestone by adding streaming support for output renderers, letting plugins register via Response.stream\(\) to emit rows in one go for TSV/CSV exports, and also provides CSS cross‑document view transitions for multi‑page navigation while patching a security advisory that could leak private query titles and SQL strings. The release also includes dozens of bug fixes, a new datasette-copy-button Web Component for copy‑schema, and improved JSON row representation.

**「Impact」** Developers can now register plugins that stream entire tables, reducing memory usage for large CSV/TSV exports, and the security fix prevents accidental disclosure of private stored queries. Users on Safari and Chrome will see smoother page transitions, while Firefox users must wait for Firefox 162 to benefit.

**Tags**: `#datasette`, `#streaming`, `#open source`, `#software engineering`, `#data tools`

---

<a id="item-tech-news-6"></a>
### [Interactive Airflow 3 ML orchestration tutorial published in English and Spanish](https://www.reddit.com/r/MachineLearning/comments/1xxa13x/handson_ml_orchestration_tutorial_with_airflow3_p/) ⭐️ 7.0/10

Reddit user /u/Total\_Firefighter\_59 has published a self-made, interactive tutorial on ML orchestration with Airflow 3, available in English and Spanish. It reworks Made With ML&\#x27;s orchestration lesson, which the author says was written for Airflow 2, and adds hands-on exercises in some sections along with material the author says is not in the original. According to the post, the first draft was generated with Claude and then took much longer to review and fix than expected. This is a community resource announced on Reddit rather than an official Airflow project release, and the post does not name a specific Airflow 3 point release, a license, or where the material is hosted beyond the Reddit link.

reddit · r/MachineLearning · /u/Total\_Firefighter\_59 · Nov 15, 23:28

**「Airflow 3 launch and interactive ML orchestration tutorial」** Apache Airflow 3.0 is the major release following Airflow 2.x, introducing a fundamental architectural shift to support generative AI and new workflows while preserving Helm chart compatibility with prior Airflow 2 versions. Many users who migrated from Airflow 2 notice that the new APIs and scheduling model differ from their previous setup, so an updated, interactive tutorial with practical exercises was created to teach ML orchestration on Airflow 3.

**「Impact」** Learners following Made With ML&\#x27;s MLOps course now have a bilingual, exercise-based option aimed at Airflow 3, which matters because the author states Airflow 3 differs from the Airflow 2 material that course uses. Because the content is an AI-generated draft that one author reviewed and corrected, and the post does not state which Airflow 3 version the exercises were run against, readers should check the DAG code against official Airflow 3 documentation rather than assume it matches their own deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.astronomer.io/blog/intro-to-airflow-3/">Introducing Apache Airflow ® 3 : the most significant release in...</a></li>
<li><a href="https://www.linkedin.com/pulse/apache-airflow-30-here-fatih-aktas-9p50f">Apache Airflow 3 .0 Is Here!</a></li>

</ul>
</details>

**Tags**: `#ml-orchestration`, `#airflow`, `#tutorial`, `#interactive`, `#mlopts`

---

<a id="item-tech-news-7"></a>
### [Meituan open-sources LongCat-2.5, claims training without Nvidia GPUs](https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/) ⭐️ 7.0/10

Meituan&\#x27;s LongCat team has published the weights for LongCat-2.5, a 1.6-trillion-parameter model aimed at agentic, long-horizon multi-step work such as coding, one week after the model was first announced. The company states that training ran entirely on Chinese chips — Huawei Ascend accelerators — and never on Nvidia GPUs; this is a vendor claim and has not been independently verified. Each token activates roughly 48 billion parameters, the model accepts text, image and video input, and the weights are released under the MIT licence, permitting commercial use. Meituan reports a Terminal Bench v2.1 score of 88.4, slightly below the 89.1 it lists for Claude Opus 5.

telegram · zaihuapd · Nov 15, 11:08

**「Prerequisite context」** LongCat-2.5 is a mixture-of-experts model: of its 1.6 trillion total parameters, roughly 48 billion are activated per token, and it accepts text, image, and video input for agentic, multi-step tasks, especially coding. Terminal Bench v2.1, on which it scored 88.4 versus Claude Opus 5&\#x27;s 89.1, evaluates AI agents on completing real tasks in a terminal environment. The training claim stands out because the team says the entire run used Huawei Ascend accelerators rather than NVIDIA GPUs, which remain the dominant hardware for large-model training.

**「Meituan&\#x27;s Open LongCat-2.5」** The open-source release gives developers and organizations an openly licensed, multimodal option for long-horizon agent and repository-level coding work, with Meituan reporting a Terminal Bench v2.1 score of 88.4. Because the model was described as trained entirely on Huawei Ascend rather than NVIDIA GPUs, it could serve as an alternative for groups building agent pipelines around domestic Chinese AI hardware, though the score trails Claude Opus 5&\#x27;s 89.1. Deployment may also require attention because Huawei Ascend, MetaX, and Muxi reportedly announced inference compatibility.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ainchina.com/blog/meituan-longcat-2-trillion-domestic-chips-china-ai-independence-2026/">How Meituan Built a Trillion-Parameter AI Model on 50,000 Domestic...</a></li>
<li><a href="https://lmspeed.net/model/longcat-2-5">LongCat - 2 . 5 API Pricing &amp; Benchmarks | LMSpeed</a></li>

</ul>
</details>

**Tags**: `#Meituan`, `#LongCat-2.5`, `#Open Source`, `#NVIDIA GPU`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Lutnick faces ethics scrutiny as Cantor cuts Nvidia stake](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 7.0/10

Cantor Fitzgerald, led by Commerce Secretary Howard Lutnick&\#x27;s sons, reported a nearly 50% decline in its Nvidia holdings between September 2025 and March 2026, according to securities filings, while Lutnick resisted White House pressure to crack down on companies suspected of funneling Nvidia chips to China.

rss · CNBC Finance · Nov 15, 19:58

**「Background」** Lutnick became Commerce Secretary in February 2025 after departing Cantor Fitzgerald, which his sons Brandon and Kyle now lead, and the firm had disclosed more than 3.5 million Nvidia shares by the end of 2024, making it one of its largest reported positions.

**Tags**: `#Nvidia`, `#export controls`, `#government ethics`, `#Cantor Fitzgerald`, `#China tech policy`

---

<a id="item-finance-news-2"></a>
### [Electric Bike Certification Pause Limits Consumer Registration](https://www.peopleapp.com/column/30053564254-500007786629) ⭐️ 7.0/10

Some electric bicycles from major brands, including Ninebot, Yade, Aima, Xinneng and Talin, cannot be registered after their 3C certification was suspended, leaving consumers in places such as Guangzhou and Wuhan unable to complete approval. China&\#x27;s new electric bicycle rules took effect on November 1 with stricter &quot;one vehicle, one charging pile, one code&quot; supervision.

telegram · zaihuapd · Nov 15, 06:08

**「Background」** China&\#x27;s market regulator inspected 201 e-bike makers and found violations such as unauthorized component changes and built-in speed-limit overrides, prompting certification bodies to suspend 3C certificates \(China&\#x27;s mandatory safety mark\); new rules effective November 1 further tightened post-certification oversight with a &quot;one vehicle, one battery, one charger, one code&quot; tracking system.

**「Impact」** The suspension is blocking consumer registration and can leave stores refusing refunds, while brands have not announced a timeline for certification reinstatement.

**Tags**: `#electric bicycles`, `#3C certification`, `#regulation`, `#consumer protection`, `#China`

---

<a id="item-finance-news-3"></a>
### [美法官驳回美光三星等 DRAM 价格操纵案撤诉动议](https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge) ⭐️ 7.0/10

A US judge allowed a DRAM price-fixing class action against Micron, Samsung, and SK Hynix to proceed, citing plausible evidence of coordinated supply restrictions that allegedly drove prices up 500%.

telegram · zaihuapd · Nov 15, 16:39

**Tags**: `#antitrust`, `#DRAM`, `#semiconductors`, `#price-fixing`, `#class-action`

---