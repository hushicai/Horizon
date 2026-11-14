---
layout: default
title: "Horizon Summary: 2026-11-14 (ZH)"
date: 2026-11-14
lang: zh
---

> 从 40 条内容中筛选出 9 条重要资讯。

---

**科技新闻**
1. [FAA issues national ground stop](#item-tech-news-1) ⭐️ 7.0/10
2. [ICML 2027 调整论文审稿流程](#item-tech-news-2) ⭐️ 7.0/10
3. [TorchTitan 团队扩展 1T MoE 到 JUPITER](#item-tech-news-3) ⭐️ 7.0/10
4. [微软 Outlook、Teams、Copilot 全球宕机超 12 小时](#item-tech-news-4) ⭐️ 7.0/10
5. [DeepSeek 开放全家桶应用 API，支持多模态与 V4.1-Flash](#item-tech-news-5) ⭐️ 7.0/10

**财经新闻**
1. [月之暗面重组架构，为赴港 IPO 铺路](#item-finance-news-1) ⭐️ 8.0/10
2. [卢特尼克因儿子公司与英伟达关系面临伦理质疑](#item-finance-news-2) ⭐️ 7.0/10
3. [芝加哥联储古尔斯比：美联储在通胀上“肯定还有工作要做”](#item-finance-news-3) ⭐️ 7.0/10
4. [黄仁勋辞职事件令美中芯片出口管制风险上升](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [FAA issues national ground stop](https://www.nbcnews.com/news/us-news/faa-orders-nationwide-ground-stop-departing-flights-reasons-safety-rcna609247) ⭐️ 7.0/10

FAA&\#x27;s national ground stop, triggered by a L3Harris telecom outage, reveals vulnerabilities in critical aviation systems and spurs debate over AI integration in air traffic control.

hackernews · zulln · 11月13日 21:05 · [社区讨论](https://news.ycombinator.com/item?id=50489641)

**标签**: `#aviation-infrastructure`, `#network-outage`, `#critical-systems`, `#AI-ATC`

---

<a id="item-tech-news-2"></a>
### [ICML 2027 调整论文审稿流程](https://www.reddit.com/r/MachineLearning/comments/1xvkxbj/icml_2027_changes_d/) ⭐️ 7.0/10

ICML 2027 据该帖子称，引入了两阶段审稿流程，并加入了针对作者署名、相互审稿和项目委员会服务的新限制，以应对提交数量上升和审稿人负担增加。该流程中，区域负责人会决定论文是否进入全流程审查，并由资深区域负责人确认第一阶段可能拒绝；作者会在 2 月 23 日前收到简短说明。帖子还提到，任何人不得加入多于 20 篇提交的论文，每篇论文必须指定作者名单中的相互审稿人，且每位审稿人最多承担 6 篇论文审查；拥有 3 篇或以上提交者可能需要服务于项目委员会，不符合要求的论文可能被直接拒绝。

reddit · r/MachineLearning · /u/Gravitist · 11月13日 21:53

**「背景」** ICML 的审稿改革通常围绕如何管理审稿任务展开。此前，随着提交量上升，审稿人负载和作者参与审稿的问题变得更受关注，因此这次两阶段流程和相互审稿限制被描述为相关调整。

**「影响」** 这意味着作者可能因为合作对象缺乏可审的相互审稿人而失去审稿名额，并可能面临被要求参与项目委员会或论文被直接拒绝的风险。

**标签**: `#machine-learning`, `#conference-review`, `#peer-review-process`, `#ai-research`, `#submission-management`

---

<a id="item-tech-news-3"></a>
### [TorchTitan 团队扩展 1T MoE 到 JUPITER](https://www.reddit.com/r/MachineLearning/comments/1xvce5h/scaling_to_1t_moe_on_torchtitan_p/) ⭐️ 7.0/10

2026 年 11 月 13 日的 Reddit 更新称，TorchTitan 团队已经能够在 JUPITER 超级计算机上训练约一万亿参数的 Mixture-of-Experts 模型，并使用 384-way FSDP 加上 4-way EP 来实现更高吞吐。该更新报告了每 GPU 约 1300 tokens/s 的吞吐量，比团队最初的基准高出约 14 倍。团队还描述了全量激活检查点、Muon、专家并行分片和通信优化等方法，并指出 InfiniBand 等互连成为瓶颈。

reddit · r/MachineLearning · /u/f14-bertolotti · 11月13日 16:28

**「背景」** 这篇报道讨论的是混合专家模型的大规模训练。其背景概念是，MoE 把不同参数部分交给不同专家模块，因此比把普通语言模型复制到多张 GPU 上训练更复杂，必须先讨论参数分片方式。TorchTitan 团队随后在 JUPITER 上尝试把约 1 万亿参数的 MoE 扩展到 384 张 GPU，并选择了 FSDP 加专家并行、跳过流水线并行。

**「万亿参数 MoE 训练的可复用优化与兼容风险」** 对在 JUPITER 或同类 GH200 集群上训练万亿参数 MoE 的团队，文中措施可直接复用：按整专家切分的 FlexShard、在 GPU 上运行 Newton-Schulz（作者称已向 TorchTitan 贡献修复）、梯度改用 bf16 all-to-all 而非 fp32 reduce-scatter、FP8 专家 all-gather，以及把侧流分配移回计算流；作者称这些改动合计带来约 14 倍吞吐提升（~1,300 tokens/s/GPU，384 卡）。需要注意两点：allocator 修复依赖 FSDP2 的私有标志 unshard\_async\_op，该标志尚在转为公共 API 的过程中，当前版本行为可能变化；组限制路由虽带来 +7% 吞吐，但作者明确表示早期运行显示其可能损害训练，结论未定。此外，吞吐数字为团队自报，未见独立复现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/pytorch/torchtitan">GitHub - pytorch/ torchtitan : A PyTorch native platform for training...</a></li>

</ul>
</details>

**标签**: `#Mixture of Experts`, `#LLM scaling`, `#distributed training`, `#GPU clusters`, `#PyTorch`

---

<a id="item-tech-news-4"></a>
### [微软 Outlook、Teams、Copilot 全球宕机超 12 小时](https://www.reuters.com/technology/microsoft-365-outlook-down-thousands-us-users-downdetector-shows-2026-11-12/) ⭐️ 7.0/10

微软 Outlook、Teams 和 Copilot 在 11 月 13 日出现全球性宕机，故障持续超过 12 小时，影响全球企业与政府通信。微软称问题源于服务器故障，未发现恶意活动，已扩大修复范围并看到回稳迹象。澳大利亚、日本和美国部分政府机构、欧洲泛交所（Euronext）邮件以及台湾部分金融机构受影响，部分机构改用传真确认交易。这是微软 365 服务今年的第二次中断。

telegram · zaihuapd · 11月13日 12:21

**「微软 Outlook、Teams 全球宕机背景」** 微软 Outlook、Teams 与 Copilot 在 11 月 13 日仍处宕机状态，故障持续超过 12 小时，导致全球企业和政府通信中断，原因是服务器问题，未发现恶意活动。

**「对全球企业与政府通信的实际影响」** 此次宕机导致全球超过 70 个国家、数百万企业与政府用户无法使用 Outlook、Teams 和 Copilot，通信中断持续超过 12 小时。具体后果包括：欧交所 Euronext 邮件服务受阻，台湾部分金融机构被迫改用传真确认交易，澳大利亚、日本和美国的政府机构也受到波及。这是微软 365 服务今年第二次长时间中断，进一步加剧了企业客户对微软云服务可靠性的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.usatoday.com/story/news/2026/11/13/microsoft-outage-outlook-teams-latest-update/92755451007/">Microsoft outage: Latest updates on Outlook, Teams - USA TODAY</a></li>
<li><a href="https://en.wikipedia.org/wiki/2026_Microsoft_outage">2026 Microsoft outage - Wikipedia</a></li>
<li><a href="https://www.breitbart.com/tech/2026/11/13/microsofts-email-meltdown-extends-into-second-day-company-reports-progress-towards-recovery/">Microsoft &#x27;s Email Meltdown Extends into Second Day, Company...</a></li>
<li><a href="https://www.theguardian.com/australia-news/2026/nov/13/global-microsoft-outage-what-happened-and-why">A global Microsoft 365 outage has hit millions – what... | The Guardian</a></li>

</ul>
</details>

**标签**: `#Microsoft 365`, `#cloud outage`, `#enterprise software`, `#service reliability`

---

<a id="item-tech-news-5"></a>
### [DeepSeek 开放全家桶应用 API，支持多模态与 V4.1-Flash](https://mp.weixin.qq.com/s/78KBHc4-4N5b2vfL9SkutQ) ⭐️ 7.0/10

DeepSeek 正式开放全家桶应用 API，开发者在原有 API 中开启对应参数，即可获得深度搜索、文件输入、链接阅读及语音等多模态对话能力，服务端会自动完成工具调用与上下文拼接。V4.1-Flash 模型已在三个接口得到支持，且 Search、Fetch、OCR、ASR、TTS 等工具可单独调用。此外，官方开源了前端 Demo（deepseek-ai/chat-demo），支持导入历史对话并进行本地部署。

telegram · zaihuapd · 11月13日 14:27

**「DeepSeek 应用 API 扩展」** DeepSeek 此次通过开放应用 API，把深度思考搜索、文件输入、链接阅读、语音等能力接入对话，开发者开启对应参数后即可获得，服务端自动完成工具调用与上下文拼接。同期，DeepSeek V4.1-Flash 已在 API 上线并支持原生多模态，旧的 V4-Flash 与 V4-Flash-Vision-Exp 已退役，官方也开源了支持导入历史对话的 chat demo。

**「降低多模态 AI 应用开发门槛」** 开发者无需自行构建复杂的工具调度与多模态上下文拼接逻辑，直接通过 DeepSeek API 即可集成搜索、文件读取、OCR、语音等全套能力，从而显著降低多模态 AI 应用的开发与集成成本。开源的本地部署 Demo 也提供了便捷的测试环境。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.deepseek.com/en/news/deepseek-v4-1-flash/">Introducing DeepSeek - V 4 . 1 - Flash : smarter, faster, more efficient.</a></li>
<li><a href="https://api-docs.deepseek.com/news/news261113/">The full DeepSeek App experience, now via API | DeepSeek API Docs</a></li>

</ul>
</details>

**标签**: `#API`, `#Multimodal`, `#LLM`, `#Tool calling`, `#Open source`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [月之暗面重组架构，为赴港 IPO 铺路](https://www.wsj.com/tech/chinas-moonshot-ai-restructures-to-pave-way-for-ipo-49f09abb) ⭐️ 8.0/10

中国 AI 初创公司月之暗面（Moonshot AI）正在调整公司架构，把开曼群岛控股公司停用、将早期美元投资人持股转至中国内主要运营实体，据知情人士和《华尔街日报》报道，以此为赴港上市做准备。

telegram · zaihuapd · 11月13日 11:29

**「背景」** 月之暗面（Moonshot AI）是人工智能助手 Kimi 的开发商，公司业务主要在中国，但持股公司注册在开曼群岛，早期美元投资人曾在该境外实体持股。此次重组将股份转至境内运营实体，以符合香港上市架构要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wsj.com/tech/chinas-moonshot-ai-restructures-to-pave-way-for-ipo-49f09abb">China’s Moonshot AI Restructures to Pave Way for IPO</a></li>
<li><a href="https://aiweekly.co/alerts/moonshot-ai-unwinds-cayman-vehicle-for-50b-hong-kong-ipo">Moonshot AI Unwinds Cayman Vehicle for $50B Hong Kong IPO</a></li>

</ul>
</details>

**标签**: `#IPO`, `#AI`, `#Corporate restructuring`, `#Hong Kong`

---

<a id="item-finance-news-2"></a>
### [卢特尼克因儿子公司与英伟达关系面临伦理质疑](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 7.0/10

CNBC 对证券申报的分析称，美国商务部长霍华德·卢特尼克因其子管理的坎托·菲茨杰拉德与英伟达的持仓和融资关系面临利益冲突质疑；该公司申报的英伟达持仓价值在 2025 年 9 月至 2026 年 3 月间从 6.52 亿美元降至 3.10 亿美元。

rss · CNBC Finance · 11月13日 23:42

**「背景」** 坎托·菲茨杰拉德是卢特尼克此前执掌、现由其子管理的华尔街公司；英伟达是美国 AI 芯片龙头，其先进芯片对华出口正受出口管制和走私调查关注。

**标签**: `#Conflict of interest`, `#Export controls`, `#Nvidia`, `#Cantor Fitzgerald`, `#Howard Lutnick`

---

<a id="item-finance-news-3"></a>
### [芝加哥联储古尔斯比：美联储在通胀上“肯定还有工作要做”](https://www.cnbc.com/2026/11/13/chicago-feds-goolsbee-says-central-bank-has-definitely-got-work-to-do-on-inflation.html) ⭐️ 7.0/10

芝加哥联储主席古尔斯比 11 月 13 日表示，美联储在通胀问题上“肯定还有工作要做”；此前公布的 10 月生产者价格指数（PPI）同比上涨 6.5%，为 2022 年 11 月以来最高。据 CME Group 的 FedWatch，市场目前完全计入 12 月 8-9 日会议加息 25 个基点。

rss · CNBC Finance · 11月13日 14:22

**「背景」** 美联储的通胀目标为 2%，而古尔斯比称通胀已近六年高于该目标，近期没有取得进展。

**标签**: `#Federal Reserve`, `#inflation`, `#monetary policy`, `#PPI`, `#interest rates`

---

<a id="item-finance-news-4"></a>
### [黄仁勋辞职事件令美中芯片出口管制风险上升](https://www.cnbc.com/2026/11/13/jensen-huang-nvidia-us-china-relations.html) ⭐️ 7.0/10

英伟达前 CEO 黄仁勋在承认婚外情后辞职，并同意在 11 月 26 日感恩节前赴美国国会作证；该婚外情对象被指为中国间谍，但相关指控尚未得到证实。分析人士预测，这一事件削弱了反对美国对华芯片出口管制的主要企业游说力量，国会可能在年底前收紧相关规则。

rss · CNBC Finance · 11月13日 02:56

**「背景」** 美国自 2022 年起限制英伟达向中国出售先进芯片，特朗普政府则在 2025 年放宽了拜登时期的许多限制。

**「影响」** 分析人士警告，若美国国会收紧出口管制，英伟达等美国芯片企业对华销售将直接受影响，北京也可能以限制稀土或芯片制造材料供应作为反制，但这些后果目前仍是预测。

**标签**: `#Nvidia`, `#U.S.-China relations`, `#semiconductor export controls`, `#geopolitical risk`, `#corporate governance`

---