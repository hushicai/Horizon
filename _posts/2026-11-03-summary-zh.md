---
layout: default
title: "Horizon Summary: 2026-11-03 (ZH)"
date: 2026-11-03
lang: zh
---

> 从 47 条内容中筛选出 17 条重要资讯。

---

**科技新闻**
1. [vLLM v0.33.0rc3 发布，升级 PyTorch 2.14 并迁移 CUDA 13.0](#item-tech-news-1) ⭐️ 8.0/10
2. [Ubuntu 仍未修复关键 Linux 内核漏洞近三周](#item-tech-news-2) ⭐️ 8.0/10
3. [LightMIS: 超轻量级医学影像分割模型适配边缘设备](#item-tech-news-3) ⭐️ 8.0/10
4. [🤖 ChatGPT 分享链接漏洞可致账号被接管](#item-tech-news-4) ⭐️ 8.0/10
5. [400 多个 AI 应用隐藏色情深伪功能被曝光](#item-tech-news-5) ⭐️ 8.0/10
6. [OpenAI 向 2028 美国总统潜在参选人发送 AI 治理备忘录](#item-tech-news-6) ⭐️ 8.0/10
7. [SGLang v0.5.23 发布：新增 10 款模型，DeepSeek-V4.1 性能提升 1.5 倍](#item-tech-news-7) ⭐️ 7.0/10
8. [Subvocal 智能眼镜：用射频传感实现无声语音输入](#item-tech-news-8) ⭐️ 7.0/10
9. [Cloudflare 有针对性 DNS 区域构建：延迟减半、内存降 85%](#item-tech-news-9) ⭐️ 7.0/10
10. [美国人口普查局因行政令将 AI 调查改为&quot;超级智能&quot;](#item-tech-news-10) ⭐️ 7.0/10
11. [呈现无法复现的基线结果的建议](#item-tech-news-11) ⭐️ 7.0/10
12. [瑞典 ICA 门店冷柜被远程设为 50°C，多家门店暂停营业](#item-tech-news-12) ⭐️ 7.0/10

**科技博客**
1. [LLMs aren&\#x27;t superhuman at reading neural network weights](#item-tech-blog-1) ⭐️ 8.0/10
2. [观众捕获：当心代理指标陷阱](#item-tech-blog-2) ⭐️ 8.0/10

**财经新闻**
1. [Anthropic 前三季度营收 332.4 亿美元，净亏损 1040 亿美元](#item-finance-news-1) ⭐️ 9.0/10
2. [中盘股市大幅波动：甲骨文、SpaceX、Tempus AI、Rivian 等](#item-finance-news-2) ⭐️ 7.0/10
3. [英国拟将多数移民定居年限延至 10 年](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [vLLM v0.33.0rc3 发布，升级 PyTorch 2.14 并迁移 CUDA 13.0](https://github.com/vllm-project/vllm/releases/tag/v0.33.0rc3) ⭐️ 8.0/10

vLLM v0.33.0rc3 发布，升级到 PyTorch 2.14.0、Triton 3.8.0，并弃用 CUDA 12.9 支持（仅发布 CUDA 13.0 版本），同时引入 libtorch ABI 稳定的 CUDA  wheels，并新增 11 种模型支持，包括 Reflection Beam-1.0（501B MoE）、Yandex AliceAI-Foundation-80B-A3B、Recursive Flint（40B MoE）等。发布还带来了 AWS EFA 镜像、ROCm 10.0 默认支持、Speculative Decoding 改进（XPress 精炼器、FLy 验证策略等）以及 Medusa 和 MLP 推测器等功能的移除。CUDA 12.9 版本的 wheels 和 \`-cu129\` 镜像不再发布，用户需迁移到新的 CUDA 13.0 制品。

github · khluu · 11月2日 10:10

**「背景」** vLLM 是一个用于高效 LLM 推理的开源引擎，长期支持多种 CUDA 版本和 PyTorch 版本。此次发布通过升级 PyTorch 2.14 和 CUDA 13.0，并新增多项基础设施改进（如 ABI 稳定的 wheels、EFA 镜像和 ROCm 10.0），同时扩展了模型生态，以满足生产环境对性能和兼容性的需求。

**「影响」** 使用 CUDA 12.9 wheels 或 \`-cu129\` 镜像的组织必须迁移到新的 CUDA 13.0 制品，否则将无法获取更新和错误修复；同时，依赖 Medusa 或 MLP 推测器的用户需要更新其配置以适应移除的功能。

**标签**: `#vLLM`, `#LLM-inference`, `#PyTorch`, `#CUDA`, `#model-support`

---

<a id="item-tech-news-2"></a>
### [Ubuntu 仍未修复关键 Linux 内核漏洞近三周](https://freenode.net/article/ubuntu-lts-kernels-still-unfixed-for-critical-cve-2026-98432) ⭐️ 8.0/10

Ubuntu 仍未为关键 Linux 内核漏洞 CVE-2026-98432 发布补丁，已超过三周。该漏洞是远程代码执行 \(RCE\) 漏洞，影响 Ubuntu LTS 发行版的内核。社区指出可通过 iptables/nftables 在 PREROUTING 中添加 u32 过滤规则阻止利用，但官方未提供正式缓解措施。

hackernews · majorchord · 11月2日 18:39 · [社区讨论](https://news.ycombinator.com/item?id=50341462)

**「背景」** CVE‑2026‑98432 是一个 Linux 内核中针对 IPv4 TCP 连接建立过程的用后释放漏洞，CVSS 评分高达 9.8，攻击者无需权限或用户交互即可通过网络远程利用。虽然 AlmaLinux 等发行版已在测试通道中提供补丁，且 Red Hat 发布了缓解措施，但 Ubuntu LTS 内核版本迄今仍未发布官方修复，导致该关键漏洞持续存在近三周。

**「影响」** 用户和组织在三周内仍面临被利用该漏洞的风险，若未采取 iptables 阻断规则等临时防护，系统可能被远程攻击。

**「社区讨论」** 评论者质疑 Ubuntu 延迟补丁的原因，并提出通过 iptables 在 PREROUTING 中添加 u32 过滤规则可在官方补丁发布前降低 exploit 风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.penligent.ai/hackinglabs/cve-2026-98432/">CVE - 2026 - 98432 Linux TCP Flaw, Ubuntu Patch and Mitigation Status</a></li>
<li><a href="https://github.com/soroushneshati/cve-2026-98432-ubuntu-mitigation">GitHub - soroushneshati/ cve - 2026 - 98432 - ubuntu -mitigation: Check an...</a></li>
<li><a href="https://almalinux.org/blog/2026-10-30-cve-2026-98432/">CVE - 2026 - 98432 : Patched kernels available in testing | AlmaLinux OS</a></li>

</ul>
</details>

**标签**: `#security`, `#Linux`, `#kernel`, `#vulnerability`, `#open source`

---

<a id="item-tech-news-3"></a>
### [LightMIS: 超轻量级医学影像分割模型适配边缘设备](https://www.reddit.com/r/MachineLearning/comments/1xm8dbo/lightmis_ultralightweight_medical_image/) ⭐️ 8.0/10

LightMIS 是一个仅含 131K 参数的超轻量级 2D 医学影像分割模型，通过直接聚合多尺度编码器特征而无需学习式逐阶段解码器，在六个数据集和五种成像模态上实现了与 nnWNet 相近的跨模态宏平均 Dice 和 IoU。在相同 nnU-Net v2.3.1 协议下训练和评估，LightMIS 参数量减少 98.14%，计算量减少 94.58%。在 Arm Mali-G52 MC2 GPU 边缘设备上，完整 LightMIS 模型的推理速度比 nnWNet 快约 10.5 倍，且所有变体均实现 100% GPU 算子覆盖，无 CPU 回退。源代码、检查点和复现细节已公开发布于 GitHub。

reddit · r/MachineLearning · /u/OkLion2068 · 11月2日 20:22

**「背景」** 医学影像分割领域长期依赖 nnU-Net 等 heavyweight 模型，但边缘设备的部署需求推动了轻量化研究。LightMIS 的提出正是为了在保持分割精度的同时，大幅降低模型复杂度和推理延迟。

**「影响」** LightMIS 使边缘设备上的实时医学影像分割成为可能，为资源受限环境下的临床辅助诊断提供了实用方案。

**标签**: `#Medical Imaging`, `#Model Efficiency`, `#Edge AI`, `#Machine Learning`, `#Open Source`

---

<a id="item-tech-news-4"></a>
### [🤖 ChatGPT 分享链接漏洞可致账号被接管](https://www.parameter.ai/labs/we-found-a-gap-at-openai) ⭐️ 8.0/10

A severe ChatGPT share‑link vulnerability enabling account takeover was disclosed and quickly patched by OpenAI.

telegram · zaihuapd · 11月2日 10:24

**标签**: `#security`, `#chatgpt`, `#vulnerability`, `#ai`

---

<a id="item-tech-news-5"></a>
### [400 多个 AI 应用隐藏色情深伪功能被曝光](https://www.wired.com/story/hundreds-of-mundane-ai-apps-are-hiding-abusive-deepfake-features/) ⭐️ 8.0/10

WIRED 调查发现，超过 400 个关联的 AI 应用和网站在以宠物画像、语言学习等普通功能为掩护，在特定触发条件下加载色情深度伪造界面，允许用户上传他人照片生成露骨图像或视频。研究人员通过代码、域名和广告追踪将这些应用与中文开发者及一家香港注册公司关联。苹果在收到线索后下架了 19 款应用，称开发者在审核通过后替换远程网页内容；谷歌在被联系前已移除大部分应用；Meta 则阻止了 209 款应用投放广告。

telegram · zaihuapd · 11月2日 12:45

**「背景」** 深度伪造技术已使得从用户上传照片生成非自愿色情内容成为可能，而应用商店政策长期禁止在未获同意的情况下分发色情内容。

**「影响」** 这些措施使得相关应用失去分发渠道，迫使开发者面临下架或重新审查，并提示平台加强对 AI 应用内容审核的力度。

**标签**: `#AI deepfakes`, `#non-consensual deepfakes`, `#app store moderation`, `#AI safety`, `#technology industry`

---

<a id="item-tech-news-6"></a>
### [OpenAI 向 2028 美国总统潜在参选人发送 AI 治理备忘录](https://www.politico.com/news/2026/11/02/openai-is-already-pitching-2028-hopefuls-on-how-to-talk-about-ai-01144821) ⭐️ 8.0/10

OpenAI 首席游说官克里斯·莱恩向约六名 2028 年美国总统潜在参选人发送了 AI 治理备忘录，要求他们发布完整的 AI 治理主张，而非仅限竞选热点。备忘录警告阻碍数据中心建设可能让中国在 AI 上超越美国，并将其比作 2002 年伊拉克战争投票。OpenAI 拒绝置评。

telegram · zaihuapd · 11月3日 03:30

**「背景」** 随着 2028 年美国大选进入关键阶段，AI 治理已成为候选人阵营关注的议题之一。

**「影响」** 这可能促使 2028 年美国总统候选人在竞选纲领中明确阐述 AI 治理立场，进而影响未来联邦层面的 AI 监管政策走向。

**标签**: `#AI governance`, `#OpenAI`, `#US politics`, `#Technology policy`, `#AI regulation`

---

<a id="item-tech-news-7"></a>
### [SGLang v0.5.23 发布：新增 10 款模型，DeepSeek-V4.1 性能提升 1.5 倍](https://github.com/sgl-project/sglang/releases/tag/v0.5.23) ⭐️ 7.0/10

SGLang v0.5.23 正式发布，由 257 位贡献者合并了 1007 个 PR。本次更新新增了 10 款 LLM、VLM 和扩散模型支持，包括 Muse Spark Open、Beam-1.0、MiniMax-M3.1-Flash、MiniCPM-V 4.7、Kev、Cosmos3-Nano-Sim、FastH3 Omni、FLUX.3 Image Klein、HY-Nomas 和 MOSS-Image。在性能方面，DeepSeek-V4.1 在 GB300 上的预填充吞吐量提升最高达 1.5 倍，32K 至 64K 提示词的首词元延迟降低约 28%；低延迟模式下，NVIDIA megakernel 和 AMD monokernel 插件可使 DeepSeek-V4.1-Flash 解码速度提升 44%（GB300）和 75%（MI350X）。此外，该版本引入了 Paged Experts 功能，可在单张消费级 GPU 上运行超出显存的 MoE 模型（比 CPU 卸载快 30 倍），并新增对 Google TPU7x 的支持。

github · Fridge003 · 11月2日 22:14

**「背景」** SGLang 是一个面向大语言模型和多模态模型的开源推理引擎，由 LMSYS 组织维护。其前序版本持续迭代，v0.5.23 是一次大规模更新，反映了社区活跃的贡献和开发速度。

**「影响」** 对于 AI 工程师和开发者而言，SGLang v0.5.23 提供了更广泛的模型支持和更强的推理性能。Paged Experts 功能使得在消费级 GPU 上运行超大 MoE 模型成为可能，显著降低了硬件门槛。新增的 TPU 支持和 LoRA 引擎也扩展了部署和微调的灵活性。

**标签**: `#artificial intelligence`, `#machine learning`, `#open source`, `#software engineering`, `#developer tools`

---

<a id="item-tech-news-8"></a>
### [Subvocal 智能眼镜：用射频传感实现无声语音输入](https://news.ycombinator.com/item?id=50340088) ⭐️ 7.0/10

YC F26 批次的 Subvocal Company 展示了一款基于射频（RF）传感的智能眼镜，可在不发出声音的情况下将默读时的唇舌运动解码为文本，输入速度可达正常语速。该设备发射类似蓝牙的无线电波，穿透面部后在经过舌头、嘴唇和软腭时被无声口型调制，再通过大规模预训练的基础模型将这些扰动解码为文字。目前产品处于早期阶段，已开放 500 台首批预购（享受 200 美元折扣），计划于 2027 年第一季度发货，但准确率、延迟、鲁棒性等关键指标尚未经过独立验证。

hackernews · aarushyadav · 11月2日 17:16

**「背景」** 该项目源于两位 Georgia Tech 计算机科学学生在 2 月 Stanford TreeHacks 黑客松期间的尝试，他们最初使用肌电图（EMG）电极贴脸捕捉肌肉电信号来复刻 MIT Media Lab 的 AlterEgo 系统，但因汗液干扰、电信号干扰、放置不稳定以及用户体验差等问题，最终转向射频方案。

**「影响」** 对于需要在公共场所（如图书馆、办公室）使用语音输入但又不想打扰他人或暴露隐私的用户，该技术提供了一种潜在的静默交互方式。然而，目前产品仍处于早期预购阶段，准确率、延迟、鲁棒性和发货时间均未经独立验证，消费者需承担较高的早期采用风险。

**「社区讨论」** 社区反馈中，有用户关注产品的佩戴适配性（如鼻梁高度对眼镜位置的影响），质疑是否需要专用硬件（认为笔记本电脑摄像头可能足够），以及注意到创始人之一与 MIT AlterEgo 项目的工程师同名。这些讨论反映出用户对技术可行性、产品设计和实用性的多重关切。

**标签**: `#silent-speech-interface`, `#wearable-computing`, `#accessibility`, `#human-computer-interaction`, `#radio-frequency-sensing`

---

<a id="item-tech-news-9"></a>
### [Cloudflare 有针对性 DNS 区域构建：延迟减半、内存降 85%](https://blog.cloudflare.com/dns-targeted-zone-builds/) ⭐️ 7.0/10

Cloudflare 表示，通过引入“有针对性的区域构建”（targeted zone builds），将其 DNS 区域构建延迟减半，并将内存使用降低了 85%。该优化作用于 Cloudflare 管理的 DNS 区域构建流程，但博文未披露具体版本、发布时间表或兼容性条件。上述数据来自 Cloudflare 自身的技术描述，尚未有独立验证。

hackernews · wondersky · 11月2日 14:47 · [社区讨论](https://news.ycombinator.com/item?id=50337558)

**「Cloudflare 目标化 DNS 构建优化」** Cloudflare 通过引入目标化 DNS 构建规划器和统一调度器，仅重建变更部分的 DNS 区域，而非整个区域。该方案将完整构建减少了约 40%，峰值内存使用量降低了 85%，并将中位构建延迟减半。该技术基于之前 Cloudflare 传统的全量重建 DNS 区域的做法，改进了构建策略以提高资源利用率和响应速度。

**「影响」** Cloudflare 的 DNS 基础设施团队及其客户受益：针对性构建计划器仅重建区域中变更的部分，使完整区域构建下降约 40%、92.95% 的构建避免完全重建，峰值内存降低 85%，构建延迟减半。区域设置变更的传播延迟因此降低；公开说明中未提及现有 DNS 接口或记录格式的兼容性变更，用户无需主动调整配置即可获得更快的构建和更低的内存占用。

**「社区讨论」** 评论者 InsidiousWombat 质疑每秒 700 次变更在 Cloudflare 规模下是否偏低，thephyber 探讨降低内存占用的研发投入回报率，JulianPaul 好奇关系型模型切换前后的 bug 趋势。以上均为社区个人看法，并非博文证实的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/dns-targeted-zone-builds/">How we halved DNS build delay and cut memory use by 85%</a></li>
<li><a href="https://daily.dev/posts/how-we-halved-dns-build-delay-and-cut-memory-use-by-85--jhnmypmtx">How we halved DNS build delay and cut memory use by 85%</a></li>
<li><a href="https://runtimewire.com/article/cloudflare-dns-targeted-zone-builds-memory-delay">Cloudflare stops rebuilding 20-million-record DNS zones to ...</a></li>
<li><a href="https://blog.cloudflare.com/dns-targeted-zone-builds/">How we halved DNS build delay and cut memory use by 85%</a></li>
<li><a href="https://daily.dev/posts/how-we-halved-dns-build-delay-and-cut-memory-use-by-85--jhnmypmtx">How we halved DNS build delay and cut memory use by 85%</a></li>

</ul>
</details>

**标签**: `#DNS`, `#infrastructure`, `#systems engineering`, `#performance optimization`

---

<a id="item-tech-news-10"></a>
### [美国人口普查局因行政令将 AI 调查改为&quot;超级智能&quot;](https://simonwillison.net/2026/Nov/2/census-bureau-super-intelligence/) ⭐️ 7.0/10

西蒙·威利森发现，美国人口普查局的商业趋势与展望调查（BTOS）因行政令 14434 号（&quot;开启超级智能时代&quot;）而第三次修改 AI 采用率调查措辞。2025 年 11 月前询问企业是否在&quot;生产商品或服务&quot;中使用 AI；2025 年 12 月改为&quot;任何业务职能&quot;; 2026 年 10 月 19 日起进一步改为&quot;超级智能或 SI（原称 AI\)&quot;。这种措辞变更导致不同时期数据不可直接比较，最新数据显示 250 人以上企业在&quot;任何业务职能&quot;口径下 AI 使用率达 40.7%。

rss · Simon Willison · 11月2日 13:31

**「背景」** 人口普查局每两周向 20 万家企业发放 BTOS 调查，每家企业每 12 周填写一次。此前威利森曾用 2025 年 9 月数据演示 GPT-5 和 Claude 代码解析器分析 AI 采用率图表，当时显示大企业采用率约 12%并呈下降趋势。问题措辞的两次变更（2025 年 11 月和 2026 年 10 月）在图表中形成明显断点，官方明确标注&quot;序列不可比&quot;。

**「影响」** 研究人员和政策制定者在追踪美国企业 AI 采用趋势时，必须按问题措辞版本分段分析数据，不能将 2025 年 11 月前、2025 年 12 月至 2026 年 10 月、2026 年 10 月后三个时期的数据直接连接。首批&quot;超级智能&quot;措辞的调查结果即将发布，可能进一步扭曲纵向对比。

**标签**: `#AI adoption`, `#executive order`, `#Census Bureau`, `#data analysis`, `#AI policy`

---

<a id="item-tech-news-11"></a>
### [呈现无法复现的基线结果的建议](https://www.reddit.com/r/MachineLearning/comments/1xm64of/couldnt_reproduce_a_published_papers_numbers_with/) ⭐️ 7.0/10

一位机器学习研究者在论文中使用原文公开的代码和列出的超参数尝试复现已发表的基线方法。 在三个随机种子下，两个基准的性能明显低于原文，尽管其他基准结果与原文相符。 作者计划在论文中同时展示原文数值和自身复现结果，并询问如何让复现过程更具说服力。

reddit · r/MachineLearning · /u/InsectActive95 · 11月2日 19:00

**「背景」** 可复现性是机器学习研究被评审接受的基本前提，研究者需提供可复制的实验设置以确保结果可信。 此前已有多份工作探讨在不同硬件或环境下复现差异的处理方式。

**「影响」** 如果未能说服审稿人，论文可能因基线复现不一致而被拒，导致作者需要额外说明实验设置或提供补充复现材料。

**标签**: `#reproducibility`, `#machine-learning`, `#research-methodology`, `#software-engineering`, `#peer-review`

---

<a id="item-tech-news-12"></a>
### [瑞典 ICA 门店冷柜被远程设为 50°C，多家门店暂停营业](https://x.com/InsiderGeo/status/2117164877701595165) ⭐️ 7.0/10

瑞典连锁超市 ICA 表示，多家门店夜间遭网络攻击，冷藏柜和冷冻柜被远程设定为 50°C，斯约博、托梅利拉等地门店受影响。受影响门店上午暂停营业，预计当地时间 9 点重开，ICA 已向顾客致歉。该攻击可能导致大量食品变质；近几周法国、美国也曾出现针对企业的类似网络攻击，但来源未说明两者是否关联。

telegram · zaihuapd · 11月2日 13:52

**「背景」** 零售连锁通常将冷藏和冷冻设备接入集中管理系统，以便远程监控与调节温度。一旦这些设备的控制通道被入侵，攻击者即可远程更改温度设定值，导致食品变质和门店停业。

**「影响」** 受影响门店需在重新营业前核查冷柜温度并评估食品是否变质，否则可能面临食品安全风险和商品损失。

**标签**: `#cybersecurity`, `#IoT`, `#retail`, `#food safety`, `#incident`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [LLMs aren&\#x27;t superhuman at reading neural network weights](https://seangoedecke.com/llms-are-not-superhuman-at-reading-and-writing-neural-network-weights/) ⭐️ 8.0/10

rss · Sean Goedecke · 11月3日 00:00

**「背景」** 近期一项论文声称前沿大语言模型能直接读写神经网络权重，表现“超越人类或常规算法”，引发对 AI 自我改进能力的担忧。但该能力实际可由熟练人类研究员借助既有方法完成，并非真正超人类。

**「方案」** 作者通过机制可解释性拆解该论文的“超人类”结果：识别游戏只需计算第一层权重的 L2 范数并生成热力图，人类即可凭直觉判断；修复 Qwen 模型 32k token 循环问题则使用了与 Heretic 消融相同的“编写对比文本→测量权重贡献→裁剪”流程。这些任务本质上是标准研究操作，而非全新能力。

**「启示」** LLM 直接操作权重的能力应被视为对现有训练方法的补充而非颠覆，评估此类声明时应区分“超人类计算”与“超人类研究能力”，避免高估 AI 辅助 AI 研究的潜力。

**标签**: `#LLM capabilities`, `#mechanistic interpretability`, `#model editing`, `#AI research automation`, `#weight manipulation`

---

<a id="item-tech-blog-2"></a>
### [观众捕获：当心代理指标陷阱](https://seangoedecke.com/audience-capture/) ⭐️ 8.0/10

rss · Sean Goedecke · 11月3日 00:00

**「背景」** 在互联网写作和工程工作中，平台机制极易诱导人们追求浏览量、互动率等表面指标。作者 Sean Goedecke 指出，过度优化这些“代理指标”会导致“观众捕获”，吸引来大量只看标题、不看内容的“点击者”，而流失了真正能深度思考和交流的目标读者。

**「方案」** 作者区分了“代理游戏”（如追逐浏览量、完成 Jira 工单）与“真实游戏”（如赢得同行尊重、做出引以为傲的技术工作）。他主张有意识地选择“真实游戏”，聚焦于那 5% 愿意深度阅读和思考的读者。即使为了现实利益偶尔妥协，也必须保持清醒，避免习惯性地在无意义的妥协中出卖自己的真实目标。

**「启示」** 核心启示在于，创作者和技术人员应时刻警惕被不想要的观众或表面指标所绑架。只有清醒地定义并坚守自己的核心目标，避免在盲目的指标优化中迷失，才能实现真正的技术价值和个人声誉。

**标签**: `#audience capture`, `#proxy metrics`, `#engineering culture`, `#writing strategy`, `#goal alignment`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [Anthropic 前三季度营收 332.4 亿美元，净亏损 1040 亿美元](https://www.cnbc.com/2026/11/02/anthropic-ant-s-1-quarter-financials.html) ⭐️ 9.0/10

根据公司 IPO 招股书披露，Anthropic 前三季度营收达 332.4 亿美元，同比增长约 1200%，而净亏损达 1040 亿美元，远高于去年同期的 251 亿美元。

telegram · zaihuapd · 11月2日 15:12

**「背景」** 该公司在最新 IPO 招股书更新中披露了此前的亏损为 251 亿美元，本次财报显示营收快速增长但净亏损显著扩大。

**「影响」** 该巨额亏损可能削弱投资者对 AI 初创公司的信心，影响后续融资和行业投资规模。

**标签**: `#AI`, `#Anthropic`, `#Financial Results`, `#Tech Industry`

---

<a id="item-finance-news-2"></a>
### [中盘股市大幅波动：甲骨文、SpaceX、Tempus AI、Rivian 等](https://www.cnbc.com/2026/11/02/stocks-making-the-biggest-moves-midday-orcl-spcx-tem-rivn.html) ⭐️ 7.0/10

周一多只股票中盘出现显著波动，波动与财报、融资计划和重大科技收购有关；其中马威科技同意以 1150 亿美元全股票交易收购 Lumentum，交易预计 2028 年上半年完成。

rss · CNBC Finance · 11月2日 20:00

**「背景」** 这些盘中波动反映了最近的企业行动：甲骨文公司为人工智能基础设施扩张计划筹资 200 亿美元（包括 100 亿美元新股和 100 亿美元高级债券 ） 、 马维尔科技以 1150 亿美元现金收购了 Lumentum 公司，以及 SpaceX 正在谈判收购或使用 Dish 网络的 Boost 移动业务以进入无线市场。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://joyrandels.medium.com/just-a-6am-email-and-goodbye-oracles-brutal-ai-reckoning-c8983e3eb061">Just a 6AM Email and Goodbye - Oracle ’s Brutal AI Reckoning | Medium</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-02/oracle-is-offering-10-billion-of-high-grade-dollar-bonds">Oracle Launches $10 Billion Sale of US Investment... - Bloomberg</a></li>
<li><a href="https://247wallst.com/investing/2026/06/05/the-tech-stock-everyone-wrote-off-just-quietly-built-a-553-billion-backlog/">The Tech Stock Everyone Wrote Off Just Quietly Built a $553 Billion ...</a></li>
<li><a href="https://www.techpowerup.com/354410/marvell-acquires-lumentum-for-usd-115-billion-all-stock-deal">Marvell Acquires Lumentum for $ 115 Billion All - Stock Deal</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-02/marvell-reaches-115-billion-deal-for-lumentum-holdings">Marvell to Acquire Lumentum in $ 115 Billion All - Stock Deal ...</a></li>
<li><a href="https://www.kucoin.com/news/flash/marvell-to-acquire-lumentum-in-115-billion-all-stock-deal">Marvell to Acquire Lumentum in $ 115 Billion All - Stock Deal | KuCoin</a></li>
<li><a href="https://en.wikipedia.org/wiki/Dish_Network">Dish Network - Wikipedia</a></li>
<li><a href="https://www.marketwatch.com/story/in-the-hunt-for-1-trillion-of-revenue-spacex-reportedly-targets-boost-mobile-for-a-deal-7eb4ea49">SpaceX has big wireless dreams — and Boost Mobile ... - MarketWatch</a></li>
<li><a href="https://shiftdelete.net/en/spacex-boost-mobile">SpaceX Boost Mobile Talks May Give Starlink a Phone Network</a></li>

</ul>
</details>

**标签**: `#Earnings`, `#M&amp;A`, `#Tech\_Stocks`, `#Market\_Movement`

---

<a id="item-finance-news-3"></a>
### [英国拟将多数移民定居年限延至 10 年](https://www.gov.uk/government/news/home-secretary-unveils-new-rules-for-migrants-settling-in-the-uk) ⭐️ 7.0/10

The UK government proposes raising the standard migrant settlement period from five to ten years, with faster paths for high earners and public-service workers and a 30-year bar for illegal entrants.

telegram · zaihuapd · 11月2日 23:50

**标签**: `#UK immigration`, `#settlement policy`, `#permanent residence`, `#Home Office`, `#labor market`

---