---
layout: default
title: "Horizon Summary: 2026-10-26 (EN)"
date: 2026-10-26
lang: en
---

> From 28 items, 6 important content pieces were selected

---

**Technology News**
1. [memt-1.0 architecture: gated deltanet-2, mixture-of-storage, 66x smaller agent memory footprint](#item-tech-news-1) ⭐️ 8.0/10
2. [Brotli 高危漏洞扩展至 Python 等 HTTP 组件](#item-tech-news-2) ⭐️ 8.0/10
3. [Ten-year-old CNN surpasses frontier LLMs in skin cancer diagnosis](#item-tech-news-3) ⭐️ 7.0/10
4. [GPU rental prices surge H200 +160%, A100 models rise since Jan 2026 index](#item-tech-news-4) ⭐️ 7.0/10
5. [GEEKCON 上海站无人机赛题引厂商报警暂停](#item-tech-news-5) ⭐️ 7.0/10

**Financial News**
1. [China&\#x27;s 2025 Population Fell by 3.39 Million](#item-finance-news-1) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [memt-1.0 architecture: gated deltanet-2, mixture-of-storage, 66x smaller agent memory footprint](https://www.reddit.com/r/MachineLearning/comments/1xeu0ht/memt10_architecture_breakdown_gated_deltanet2/) ⭐️ 8.0/10

memt-1.0 is a memory-native architecture that internalizes agent memory into model computation instead of appending past execution logs to the context window or relying on external RAG. It pairs gated deltanet-2 with a token-level memory update mechanism each turn and adds a mixture-of-storage layer for capacity. The post reports that memt-1.0-nano at 128k context delivers roughly 1.86x end-to-end inference speedup and a 66x reduction in persistent storage versus a full-context KV cache, while a two-stage training pipeline over 34b tokens aims to preserve general reasoning. These figures come from the Reddit post rather than independent measurement.

reddit · r/MachineLearning · /u/Mrs-Grumpy23 · Oct 25, 05:31

**「Background」** Typical long-horizon agents store past execution logs as raw text in the prompt or fetch them through external RAG pipelines, which inflates the context window as history accumulates. Full-context KV caches also grow linearly with context length, creating storage and inference pressure during multi-turn tasks. memt-1.0 addresses this by internalizing procedural experience into model weights and states during computation.

**「Impact」** Developers building long-horizon agents could cut persistent storage by 66x and improve end-to-end inference speed by roughly 1.86x at 128k context if the memt-1.0-nano results hold. Because only the nano variant is cited and the figures are not independently measured, applicability to larger models or production workloads remains unconfirmed.

**Tags**: `#Machine Learning`, `#AI`, `#Model Efficiency`, `#Memory Architecture`, `#Research`

---

<a id="item-tech-news-2"></a>
### [Brotli 高危漏洞扩展至 Python 等 HTTP 组件](https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) ⭐️ 8.0/10

A critical Brotli decoder vulnerability \(CVE-2026-111497\) affecting versions 1.0.3–1.2.0 impacts Node.js and Python HTTP components, enabling remote unauthenticated attacks; patched versions are available.

telegram · zaihuapd · Oct 25, 02:42

**Tags**: `#security`, `#vulnerability`, `#brotli`, `#python`, `#node.js`

---

<a id="item-tech-news-3"></a>
### [Ten-year-old CNN surpasses frontier LLMs in skin cancer diagnosis](https://lynchlab.net/llm-skin-cancer) ⭐️ 7.0/10

A decade-old CNN model reportedly outperformed frontier large language models on skin cancer diagnosis, according to a single study and blog post. The result has sparked discussion about the relative value of specialized medical AI models versus general-purpose LLM-driven decision systems.

hackernews · sungam · Oct 25, 17:15 · [Discussion](https://news.ycombinator.com/item?id=50233779)

**「Background」** Skin cancer diagnosis with AI typically involves training convolutional neural networks on dermoscopic image datasets to classify lesions, while large language models aim to generalize across diverse medical tasks through broad training data. This comparison highlights the trade-off between specialized image models and general-purpose systems.

**「Community Discussion」** A commenter who fine-tuned Inception v3 on 68,011 ISIC images suggested the result reflects benchmark optimization, noting the test lesions were excluded from training data. Others emphasized that specialized models inherently outperform general LLMs on narrow diagnostic tasks, though real-world image variability remains a concern.

**Tags**: `#skin cancer diagnosis`, `#CNN`, `#LLM evaluation`, `#medical AI`, `#specialized models`

---

<a id="item-tech-news-4"></a>
### [GPU rental prices surge H200 +160%, A100 models rise since Jan 2026 index](https://x.com/a16z/status/2113741008550990191) ⭐️ 7.0/10

GPU rental prices have surged sharply since January 2026, with the H200 up 160% and the A100 SXM4 reaching approximately 102 on an index that started at 100 on Jan 1, 2026, through October 19, 2026, reflecting increased costs for AI/ML practitioners. Even older A100 models show modest increases, reflecting broad cost pressure. The a16z index, tracked through October 2026, shows H200 at ~265, B200 at ~225, RTX PRO 6000 workstation at ~165, and H100 SXM at ~137.

telegram · zaihuapd · Oct 25, 06:39

**「Background」** The a16z GPU rental price index was established on January 1, 2026, with a baseline of 100, to track monthly moving-average rental costs for key AI accelerator models. It enables comparison of price changes across generations such as H200, B200, H100, and older A100 models.

**「Impact」** The 160% H200 price increase and 35% H100 rise from the January 2026 baseline directly raise operational costs for AI/ML workloads, prompting teams to adjust budgets and consider mixed-generation or on-premises hardware alternatives.

**Tags**: `#GPU`, `#pricing`, `#cloud-infrastructure`, `#AI-hardware`, `#a16z`

---

<a id="item-tech-news-5"></a>
### [GEEKCON 上海站无人机赛题引厂商报警暂停](https://tech.ifeng.com/c/8xSZe56UAz6) ⭐️ 7.0/10

A GEEKCON drone challenge that bypassed GPS restrictions triggered a manufacturer alarm, leading to a temporary suspension and renewed debate over research boundaries.

telegram · zaihuapd · Oct 25, 13:29

**Tags**: `#drone security`, `#hardware security`, `#research ethics`, `#IoT security`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s 2025 Population Fell by 3.39 Million](https://weibo.com/1796087453/5357878513767954) ⭐️ 8.0/10

China&\#x27;s year-end 2025 population fell by 3.39 million to 1.40489 billion, with a natural growth rate of -2.41‰, according to the China Statistical Yearbook 2026.

telegram · zaihuapd · Oct 25, 12:02

**「Background」** The decline continues China&\#x27;s demographic contraction, with only seven provinces maintaining positive natural growth rates, concentrated in western and southern China.

**「Impact」** The shrinking population carries implications for labor markets, pension systems, and economic growth, with northeastern provinces experiencing the most severe demographic decline.

**Tags**: `#demographics`, `#population decline`, `#China economy`, `#economic data`, `#social policy`

---