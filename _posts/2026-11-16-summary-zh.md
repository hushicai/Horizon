---
layout: default
title: "Horizon Summary: 2026-11-16 (ZH)"
date: 2026-11-16
lang: zh
---

> 从 36 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Meta FAIR 与 NYU 研究《Unbundling Multimodal Vision Encoding》：编码器预训练可省，视觉专属参数不可省](#item-tech-news-1) ⭐️ 8.0/10
2. [cudamemcpy-tuner 在 B300 上加速分页 cudaMemcpy](#item-tech-news-2) ⭐️ 8.0/10
3. [黄仁勋据报考虑回归英伟达 CEO](#item-tech-news-3) ⭐️ 8.0/10
4. [Protomaps: 自托管地图瓦片更便宜、更容易](#item-tech-news-4) ⭐️ 7.0/10
5. [Datasette 1.0a43 发布：输出渲染器流式支持与安全修复](#item-tech-news-5) ⭐️ 7.0/10
6. [Airflow 3 交互式机器学习编排教程](#item-tech-news-6) ⭐️ 7.0/10
7. [美团 LongCat-2.5 开源：1.6 万亿参数模型声称仅用华为升腾训练](#item-tech-news-7) ⭐️ 7.0/10

**财经新闻**
1. [美国商务部长卢特尼克因英伟达股份变动面临道德质疑](#item-finance-news-1) ⭐️ 7.0/10
2. [部分电动自行车 3C 认证被暂停，消费者上牌受阻](#item-finance-news-2) ⭐️ 7.0/10
3. [美法官驳回美光三星等 DRAM 价格操纵案撤诉动议](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Meta FAIR 与 NYU 研究《Unbundling Multimodal Vision Encoding》：编码器预训练可省，视觉专属参数不可省](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR 与纽约大学在预印本《Unbundling Multimodal Vision Encoding》中报告（Reddit 帖文作者声明系合著者之一）：他们从零训练 200 多个 MLLM，LLM 也从零开始，统一数据且编码器预训练计入同一算力预算，把标准视觉编码器捆绑的三项选择拆开测试，发现单独预训练可选、视觉专属参数必需、放在 LLM 之前可选。主要对比用 Qwen3-1.7B 与 4B 配置（0.4B 视觉参数），扩展阶梯覆盖 0.6B–6.4B 骨干，评估为 Cambrian 的 16 个 VQA 基准（448px）和 12 个语言基准；四种预训练目标（对比、自监督、两种描述）最多与随 LLM 从头训练的编码器打平，MetaCLIP 预训练延长 6.5 倍只把 ImageNet 线性探针从 80.4% 提到 84.4%，VQA 不变。无编码器的模型在每个规模都落后、约需 3 倍算力追平；把编码器参数转给 LLM 只改善文本、不改善 VQA。“In-fusion”在 LLM 前 8 层加入零初始化、仅视觉 token 使用的注意力投影与 FFN 权重，1.7B–6.4B 与编码器持平（1.7B 时 VQA 45.0 对 44.4；文本共享时 42.3，放最后 8 层时 35.1），首 token 时间约降 13%，在预训练 LLM 中期训练加入视觉时同样成立。

reddit · r/MachineLearning · /u/trungh98 · 11月15日 17:38

**「背景」** 标准视觉编码器把三个选择捆绑在一起：单独预训练、仅视觉 token 使用的参数、以及放在 LLM 之前。各实验室目前做法不一——Gemma 4 12B 去掉编码器、Kimi K3 从头训练编码器、Inkling 2 Small 又把编码器加回——但已发布模型在数据与算力上各不相同，也很少把编码器预训练计入成本，因此无法裁决这一争论。

**「影响」** 对多模态架构设计者而言，该研究支持在统一算力预算内取消单独编码器预训练，并采用 in-fusion 把视觉权重并入 LLM 前 8 层以降低约 13% 首 token 时间，但前提是保留仅视觉 token 使用的参数，否则需约 3 倍算力才能追平。结论限于 448px 输入、Cambrian VQA 与所列语言基准，且为作者自报的受控实验，迁移到其他数据、分辨率或已发布模型前需谨慎。

**标签**: `#multimodal LLMs`, `#vision encoders`, `#architecture search`, `#empirical study`, `#Meta FAIR`

---

<a id="item-tech-news-2"></a>
### [cudamemcpy-tuner 在 B300 上加速分页 cudaMemcpy](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 8.0/10

作者发布了开源工具 cudamemcpy-tuner，用于加速 NVIDIA B300 上的分页主机内存 cudaMemcpy。其给出的 PyTorch 基准显示，将 1 GB uint8 张量从 CPU 拷贝到 GPU 的速度从 10.2 GB/s 提升到 51.5 GB/s，约 5 倍；该路径是 PyTorch 默认的分页传输，无需改用 pinned memory。该结果来自作者提供的基准和博客，尚未见独立复现。

reddit · r/MachineLearning · /u/makneeee · 11月15日 18:20

**「背景」** cudaMemcpy 是 CUDA 中在主机与设备间传输数据的核心 API。默认情况下 PyTorch 等框架使用可分页主机内存，传输时驱动需先将数据拷贝到内核固定的固定内存再发起 DMA，导致带宽远低于显式分配的固定内存。NVIDIA 官方文档指出固定内存可显著提升传输速率，但需要显式调用 cudaMallocHost 或 cudaHostAlloc。B300 基于 Blackwell 架构，引入了新的内存子系统和更高的 PCIe / NVLink 带宽，但可分页传输的默认路径仍受限于驱动内部的临时缓冲区大小与调度策略。

**「影响」** 使用 PyTorch 在 B300 上进行主机-设备数据传输的开发者，可以尝试通过 \`cmt tune -- &lt;命令&gt;\` 包装基准或训练命令，以减少默认分页拷贝带来的开销；不过收益需在自己的工作负载和硬件上验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/how-optimize-data-transfers-cuda-cc/">How to Optimize Data Transfers in CUDA C/C++ | NVIDIA Technical...</a></li>
<li><a href="https://cuda.live/tutorials/memory-model">CUDA Memory : Global, Shared, Constant &amp; Pinned Memory</a></li>
<li><a href="https://habr.com/ru/companies/cloud4y/articles/1026692/">Сравнение GPU NVIDIA : от V100 до B 300 / Хабр</a></li>

</ul>
</details>

**标签**: `#cuda`, `#gpu-optimization`, `#memory-transfer`, `#pytorch`, `#blackwell-architecture`

---

<a id="item-tech-news-3"></a>
### [黄仁勋据报考虑回归英伟达 CEO](https://www.ft.com/content/0f30a230-4d66-481b-a4fd-3a4ed0c45855) ⭐️ 8.0/10

《金融时报》援引消息人士报道，英伟达创始人黄仁勋正与亲信讨论回归 CEO 职位，但这目前仅是考虑，尚未正式复职。黄仁勋上周四因两段婚外情曝光而辞职，其中一人被怀疑为中国间谍，引发外界对美国对华 AI 芯片出口的担忧。其盟友正组建硅谷高管“作战室”游说董事会并寻求白宫支持，支持者请愿签名已超过 15.6 万。董事会同时已接触 Arm CEO Rene Haas 作为潜在继任者。

telegram · zaihuapd · 11月16日 01:06

**「背景」** 近期报道证实，黄仁勋因涉及婚外情及一名被美国情报界认定为中国间谍的女性丑闻而于上周辞去英伟达 CEO 一职，公司随即任命首席财务官科特勒·克雷斯为代理 CEO。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tech.yahoo.com/general/breaking-news/article/nvidia-ceo-jensen-huang-resigns-after-extramarital-affairs-raise-national-security-concerns-140401302.html">Nvidia CEO Jensen Huang resigns after extramarital affairs ...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI`, `#Semiconductor`, `#Leadership`, `#Geopolitics`

---

<a id="item-tech-news-4"></a>
### [Protomaps: 自托管地图瓦片更便宜、更容易](https://bruceroettgers.eu/blog/protomaps/) ⭐️ 7.0/10

Protomaps 让自托管地图瓦片变得更便宜且更容易部署，提供了在 Cloudflare R2 上运行自己的地图基础设施（如 PMTiles 命令行工具或网页界面）的方案。它基于开源数据（如 OpenStreetMap）并引入了 ntmaps 库，帮助开发者快速构建无需注册、无 API 密钥的自定义地图展示。例如，作者提到可以用它为个人项目（如维基百科走路游戏）提供可行的路径。

hackernews · bcye · 11月15日 19:26 · [社区讨论](https://news.ycombinator.com/item?id=50509837)

**「背景」** 自托管地图瓦片是指用户自己管理地图瓦片存储和服务，避免依赖第三方平台，如 Mapbox 或 Google Maps。前期免费的 OpenFreeMap 虽然允许无限制的展示，但缺少瓦片技术栈和托管解决方案；而 Protomaps 通过使用 Cloudflare R2 等私有基础设施降低成本，并提供 CLI（gloss）和网页拖拽入口。该项目依托开源数据（OSM）和 Golang 库 ntmaps，旨在让小型项目（如 Wikipedia 走路游戏）能够低成本、低门槛地实现实时街道渲染。

**「影响」** 用户和组织可以以私有方式托管高分辨率瓦片，减轻公共基础设施负载并降低运营费用，但当缩放级别超过 z17 时存储需求可能达到数十 TB，且部分大瓦片（&gt;128M）加载存在问题，需要进一步优化 URL 加载。开发者应关注存储容量和瓦片大小，必要时考虑压缩或分块策略。

**「社区讨论」** 评论提到 OpenFreeMap 免费但无瓦片技术，而 neomantra 计划在 Cloudflare R2 上实现类似功能并提供 PMTiles CLI；motoroco 指出高分辨率卫星图像会快速膨胀存储，z17 可能成为上限；X-Cubed 则表示 Cloudflare 已改善范围请求支持。

**标签**: `#self-hosting`, `#open-source`, `#mapping`, `#web-development`, `#infrastructure`

---

<a id="item-tech-news-5"></a>
### [Datasette 1.0a43 发布：输出渲染器流式支持与安全修复](https://simonwillison.net/2026/Nov/15/datasette/) ⭐️ 7.0/10

Datasette 1.0a43 为开发者和插件作者发布，增加了输出渲染器的流式输出支持：内置的 TSV 和 CSV 导出机制已改用该机制，插件可通过新的 Response.stream\(\) 方法注册能够一次性流式传输整张表格每一行的能力。该版本还修复了安全问题，其中一项已获 GitHub 安全通告（GHSA-mw6v-83vp-7c4c），私有存储查询的标题和 SQL 可能被泄露，但无法执行该查询。此外，行页面的 JSON 表达式已达到 1.0 设计标准，并新增 &lt;datasette-copy-button&gt; Web 组件、列中 JSON 美化打印以及 DatasetteModal.confirm\(\) 等改进。1.0 里程碑目前完成 53%。

rss · Simon Willison · 11月15日 23:20

**「Datasette 1.0a43 背景」** 在 Datasette 1.0 发布之前，内置的 CSV 和 TSV 导出以及插件输出渲染器主要依赖一次性响应来处理数据；1.0a43 引入了 Response.stream\(\)，才使流式输出和插件流式渲染成为可能。

**「影响」** 插件作者如需为输出渲染器提供逐行流式导出，应使用新的 Response.stream\(\) 接口进行注册；使用 Datasette 的组织应尽快升级，以修复私有存储查询标题和 SQL 可能被泄露的安全问题。CSS 多页面视图过渡目前仅在 Safari 和 Chrome 生效，Firefox 支持预计在 12 月 8 日的 Firefox 162 中到来。

**标签**: `#datasette`, `#streaming`, `#open source`, `#software engineering`, `#data tools`

---

<a id="item-tech-news-6"></a>
### [Airflow 3 交互式机器学习编排教程](https://www.reddit.com/r/MachineLearning/comments/1xxa13x/handson_ml_orchestration_tutorial_with_airflow3_p/) ⭐️ 7.0/10

该教程为想学习机器学习编排的用户提供了基于 Airflow 3 的交互式学习体验，包含实际练习和代码示例。它弥补了以往仅针对 Airflow 2 的 Made With ML 教程的不足，使用户能够直接在 Airflow 3 环境中操作。

reddit · r/MachineLearning · /u/Total\_Firefighter\_59 · 11月15日 23:28

**「Airflow 3 背景」** Apache Airflow 3 被介绍为相较 2.x 系列的重要版本，其架构因生成式 AI 等新用例而发生根本性变化。对从 Airflow 2 迁移的工程师而言，3.0 被视为提升编排能力的版本，因此旧版教程可能无法覆盖新版本差异。

**「影响」** 用户可以通过动手完成的练习快速熟悉 Airflow 3 的新特性，提升 MLOps 工作流的效率，并降低因教程过时而需额外查找资源的成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.astronomer.io/blog/intro-to-airflow-3/">Introducing Apache Airflow ® 3 : the most significant release in...</a></li>
<li><a href="https://www.linkedin.com/pulse/apache-airflow-30-here-fatih-aktas-9p50f">Apache Airflow 3 .0 Is Here!</a></li>

</ul>
</details>

**标签**: `#ml-orchestration`, `#airflow`, `#tutorial`, `#interactive`, `#mlopts`

---

<a id="item-tech-news-7"></a>
### [美团 LongCat-2.5 开源：1.6 万亿参数模型声称仅用华为升腾训练](https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/) ⭐️ 7.0/10

美团旗下 LongCat 团队发布 1.6 万亿参数大模型 LongCat-2.5，专为智能体自主完成冗长多步骤任务（尤其是编程）而设计，并开源其权重，许可证为 MIT，允许商用。官方声称该模型全程使用华为升腾加速卡训练，从未使用 NVIDIA GPU；每个 token 激活约 480 亿参数，支持文本、图像和视频输入。在 Terminal Bench v2.1 基准测试中得 88.4 分，略低于 Claude Opus 5 的 89.1 分。

telegram · zaihuapd · 11月15日 11:08

**「背景说明」** LongCat 是美团旗下的大模型团队，本次发布的模型总参数达 1.6 万亿，但每个 token 仅激活约 480 亿参数，属于稀疏激活的专家混合（MoE）架构，因此参数量不能与稠密模型直接类比。Terminal Bench 是衡量智能体自主完成多步骤、冗长任务（尤其编程任务）能力的基准测试。华为升腾是国产 AI 加速芯片系列，在英伟达高端 GPU 受限的背景下常被视为替代训练算力。

**「对使用者的实际影响」** MIT 许可证意味着开发者可以商用、修改并自托管 LongCat-2.5，但 1.6 万亿总参数、每 token 激活约 480 亿的体量使自建推理仍需可观算力，因此多数团队更可能经由第三方 API 调用（Models.dev 已列出 4 家提供商）。同时，官方“训练全程使用华为升腾、未用英伟达 GPU”的说法目前仅为厂商声明，尚无独立验证，计划据此评估非英伟达算力路线的机构应将其视为待核实的前提。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://models.dev/models/meituan/longcat-2.5/">LongCat - 2 . 5 pricing, providers, and specs | Models.dev</a></li>

</ul>
</details>

**标签**: `#Meituan`, `#LongCat-2.5`, `#Open Source`, `#NVIDIA GPU`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美国商务部长卢特尼克因英伟达股份变动面临道德质疑](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 7.0/10

美国商务部长霍华德·卢特尼克因其儿子管理的坎托·菲茨杰拉德在 2025 年 9 月至 2026 年 3 月将英伟达持股减少近 50%（从 350 万股降至 178 万股），而他在同期抵制白宫和情报机构打击涉嫌向中国走私英伟达芯片的公司，引发道德审查；目前无证据显示存在不当行为。

rss · CNBC Finance · 11月15日 19:58

**「背景」** 卢特尼克于 2025 年 2 月出任商务部长前曾任坎托 CEO，现由其子布兰登和凯尔领导；特朗普于 2025 年 11 月 5 日第三次授权对涉嫌走私芯片公司实施出口管制，英伟达 CEO 黄仁勋于 2026 年 11 月 13 日辞职，此前卢特尼克收到机密情报警告黄与疑似中国间谍有关联。

**「影响」** 伦理专家指外观不佳，参议员跨党派敦促重审英伟达出口许可，财长贝森特披露财政、国防、国务及贸易部门数月前均支持将涉嫌走私公司列入实体清单，但商务部未执行，显示政府内部出现分歧。

**标签**: `#Nvidia`, `#export controls`, `#government ethics`, `#Cantor Fitzgerald`, `#China tech policy`

---

<a id="item-finance-news-2"></a>
### [部分电动自行车 3C 认证被暂停，消费者上牌受阻](https://www.peopleapp.com/column/30053564254-500007786629) ⭐️ 7.0/10

广州、武汉等地消费者反映，九号、雅迪、爱玛、新日、台铃等品牌电动自行车因 3C 认证证书被暂停无法登记，门店售前曾承诺可上牌，事后仅让等待或以车辆已激活为由拒退。市场监管总局此前对全国 201 家企业检查，认证机构据此停证，各品牌客服称暂无恢复时间表。

telegram · zaihuapd · 11月15日 06:08

**「背景」** 3C 认证是中国对电动自行车等产品实施的强制性安全认证，缺少有效证书的车辆无法登记上牌。此次暂停源于市场监管总局此前对全国 201 家企业的检查，发现更换关键部件、预留解限空间等问题，认证机构据此停证。

**标签**: `#electric bicycles`, `#3C certification`, `#regulation`, `#consumer protection`, `#China`

---

<a id="item-finance-news-3"></a>
### [美法官驳回美光三星等 DRAM 价格操纵案撤诉动议](https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge) ⭐️ 7.0/10

A US judge allowed a DRAM price-fixing class action against Micron, Samsung, and SK Hynix to proceed, citing plausible evidence of coordinated supply restrictions that allegedly drove prices up 500%.

telegram · zaihuapd · 11月15日 16:39

**标签**: `#antitrust`, `#DRAM`, `#semiconductors`, `#price-fixing`, `#class-action`

---