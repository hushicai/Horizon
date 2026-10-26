---
layout: default
title: "Horizon Summary: 2026-10-26 (ZH)"
date: 2026-10-26
lang: zh
---

> 从 28 条内容中筛选出 6 条重要资讯。

---

**科技新闻**
1. [memt-1.0 架构解析：门控 DeltaNet-2 与混合存储实现 66 倍存储缩减](#item-tech-news-1) ⭐️ 8.0/10
2. [Brotli 高危漏洞扩展至 Python 等 HTTP 组件](#item-tech-news-2) ⭐️ 8.0/10
3. [Inception v3 beats frontier LLMs on skin cancer diagnosis](#item-tech-news-3) ⭐️ 7.0/10
4. [GPU 租赁价格全面上涨，H200 涨幅达 160%](#item-tech-news-4) ⭐️ 7.0/10
5. [GEEKCON 上海站无人机赛题引厂商报警暂停](#item-tech-news-5) ⭐️ 7.0/10

**财经新闻**
1. [2025 年中国总人口减少 339 万，接近 14 亿关口](#item-finance-news-1) ⭐️ 8.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [memt-1.0 架构解析：门控 DeltaNet-2 与混合存储实现 66 倍存储缩减](https://www.reddit.com/r/MachineLearning/comments/1xeu0ht/memt10_architecture_breakdown_gated_deltanet2/) ⭐️ 8.0/10

memt-1.0 采用内存原生架构，将记忆直接嵌入模型计算层，而非依赖外部检索或完整 KV 缓存。它通过门控 DeltaNet-2 实现稳定的逐 token 记忆更新，并结合混合存储（MOS）层扩展容量。在 128k 上下文长度下，memt-1.0-nano 相较于完整上下文 KV 缓存方案实现了约 1.86 倍的端到端推理加速和 66 倍的持久化存储缩减。其两阶段训练流程（持续预训练 + 后训练，共 34B token）在保持通用推理能力的同时，超越了现有参数化记忆基线。

reddit · r/MachineLearning · /u/Mrs-Grumpy23 · 10月25日 05:31

**「背景」** 传统智能体通常将过往执行日志作为原始文本检索，导致上下文窗口膨胀。memt-1.0 则将检索到的过程性经验在多轮任务中持续内化为模型权重或状态，从而避免上下文膨胀问题。

**「影响」** 对于构建长程智能体的开发者，memt-1.0 在 128k 上下文下提供的 1.86 倍推理加速和 66 倍存储缩减，可直接缓解 KV 缓存的内存瓶颈。但需注意其性能表现依赖于特定的两阶段训练流程与架构设计。

**标签**: `#Machine Learning`, `#AI`, `#Model Efficiency`, `#Memory Architecture`, `#Research`

---

<a id="item-tech-news-2"></a>
### [Brotli 高危漏洞扩展至 Python 等 HTTP 组件](https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) ⭐️ 8.0/10

A critical Brotli decoder vulnerability \(CVE-2026-111497\) affecting versions 1.0.3–1.2.0 impacts Node.js and Python HTTP components, enabling remote unauthenticated attacks; patched versions are available.

telegram · zaihuapd · 10月25日 02:42

**标签**: `#security`, `#vulnerability`, `#brotli`, `#python`, `#node.js`

---

<a id="item-tech-news-3"></a>
### [Inception v3 beats frontier LLMs on skin cancer diagnosis](https://lynchlab.net/llm-skin-cancer) ⭐️ 7.0/10

A fine‑tuned Inception v3 CNN achieved higher diagnostic accuracy on skin cancer than current frontier LLMs. The model was trained on 68,011 dermoscopic and clinical images from the ISIC Archive and evaluated on 200 unseen lesions, with all test images excluded from training and validation. The claim comes from a single blog post and has sparked debate about the role of specialized classifiers versus general‑purpose LLM‑based decision support in medicine.

hackernews · sungam · 10月25日 17:15 · [社区讨论](https://news.ycombinator.com/item?id=50233779)

**「Background」** Specialized convolutional neural networks have long been used for skin lesion classification, while large language models are being explored for medical reasoning and decision support. The comparison highlights that domain‑specific architectures can retain an edge over broad‑scope LLMs when the task is highly visual and well‑defined.

**「Impact」** The result suggests that for visual diagnostic tasks like skin cancer detection, a dedicated CNN fine‑tuned on a large, curated dataset can still outperform frontier LLMs, indicating a need to prioritize specialized models for such applications.

**「Community discussion」** Commenters such as snitty and tasuki argue that a purpose‑built classifier is inherently more accurate than a general‑purpose LLM, likening it to a Go‑specific engine beating a language model at the game. Others like jonex counter that LLMs could be extended with multimodal data \(journal notes, patient questions, varied image conditions\) to close the gap, noting the current study only measures a narrow benchmark.

**标签**: `#skin cancer diagnosis`, `#CNN`, `#LLM evaluation`, `#medical AI`, `#specialized models`

---

<a id="item-tech-news-4"></a>
### [GPU 租赁价格全面上涨，H200 涨幅达 160%](https://x.com/a16z/status/2113741008550990191) ⭐️ 7.0/10

根据 a16z 发布的数据，以 2026 年 1 月 1 日为基准（指数 100）的 GPU 租赁价格七日移动平均指数显示，截至 10 月 19 日，H200 指数升至约 265（涨幅 160%），B200 约 225（涨幅 120%），RTX PRO 6000 工作站版约 165（涨幅 65%），H100 SXM 约 137（涨幅 35%），即便是 2020 年发布的 A100 SXM4 指数也达约 102，略高于年初水平。这表明 AI/ML 工作负载的 GPU 租赁成本在近十个月中大幅上升，连老款机型也不例外。

telegram · zaihuapd · 10月25日 06:39

**「背景」** GPU 租赁市场价格波动直接反映 AI 算力供需关系。2026 年以来，生成式 AI 模型训练与推理需求持续增长，而新一代芯片（如 H200、B200）产能爬坡有限，导致高端 GPU 供给偏紧。a16z 作为知名风投机构，定期追踪云端 GPU 租赁价格指数，为行业提供成本基准参考。

**「影响」** AI/ML 团队在预算规划和基础设施选型时需预期更高的算力成本，尤其是依赖 H200、B200 等新一代高端 GPU 的大规模训练任务，成本压力显著增加；即便迁移至 H100 或 A100 等上一代产品，价格优势也在收窄，可能需重新评估云端与自建集群的成本效益。

**标签**: `#GPU`, `#pricing`, `#cloud-infrastructure`, `#AI-hardware`, `#a16z`

---

<a id="item-tech-news-5"></a>
### [GEEKCON 上海站无人机赛题引厂商报警暂停](https://tech.ifeng.com/c/8xSZe56UAz6) ⭐️ 7.0/10

A GEEKCON drone challenge that bypassed GPS restrictions triggered a manufacturer alarm, leading to a temporary suspension and renewed debate over research boundaries.

telegram · zaihuapd · 10月25日 13:29

**标签**: `#drone security`, `#hardware security`, `#research ethics`, `#IoT security`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [2025 年中国总人口减少 339 万，接近 14 亿关口](https://weibo.com/1796087453/5357878513767954) ⭐️ 8.0/10

2025 年末中国全国总人口为 140489 万人（约 14.05 亿），比 2024 年末减少 339 万人，面临跌破 14 亿；全年出生 792 万人，自然增长率为-2.41‰。数据据《中国统计年鉴 2026》引用，经微博及电报转发，并非国家统计局直接发布。

telegram · zaihuapd · 10月25日 12:02

**「背景」** 自然增长率是出生率减去死亡率，负值表示死亡人数多于出生人数；中国总人口此前已进入下降阶段。

**标签**: `#demographics`, `#population decline`, `#China economy`, `#economic data`, `#social policy`

---