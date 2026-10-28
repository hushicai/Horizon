---
layout: default
title: "Horizon Summary: 2026-10-28 (ZH)"
date: 2026-10-28
lang: zh
---

> 从 50 条内容中筛选出 24 条重要资讯。

---

**科技新闻**
1. [Anthropic 招聘经理停用编程面试](#item-tech-news-1) ⭐️ 9.0/10
2. [DeepMind 发布 Genie 4 世界模型](#item-tech-news-2) ⭐️ 8.0/10
3. [亚马逊因持续失败裁撤 AI 部门](#item-tech-news-3) ⭐️ 8.0/10
4. [基于 ZeRO-3 与 LoRA 的大规模自蒸馏开源方案](#item-tech-news-4) ⭐️ 8.0/10
5. [微软修复 Authenticator 安卓版高危漏洞 CVE-2026-80097](#item-tech-news-5) ⭐️ 8.0/10
6. [Classification of Finite Simple Groups Formalized in Lean](#item-tech-news-6) ⭐️ 7.5/10
7. [极客湾发布六款旗舰手机芯片能效横评](#item-tech-news-7) ⭐️ 7.5/10
8. [triton-lang/triton released v3.9.0](#item-tech-news-8) ⭐️ 7.0/10
9. [Tailscale SSH 安全调查与修复更新](#item-tech-news-9) ⭐️ 7.0/10
10. [Survival LLM：本地化应急知识检索系统](#item-tech-news-10) ⭐️ 7.0/10
11. [Python 实验性 JIT 编译器被移除](#item-tech-news-11) ⭐️ 7.0/10
12. [维基百科清理 AI 生成内容引发社区讨论](#item-tech-news-12) ⭐️ 7.0/10
13. [手动实现 Transformer 反向传播教程在 PyTorch 中发布](#item-tech-news-13) ⭐️ 7.0/10
14. [Papers with Code is now open-source \[P\]](#item-tech-news-14) ⭐️ 7.0/10
15. [Ψ-0.6：统一视觉语言世界模型引入自适应思维流](#item-tech-news-15) ⭐️ 7.0/10
16. [LiquidAI 发布 LFM3-1.7B 三混合架构模型](#item-tech-news-16) ⭐️ 7.0/10
17. [LFM3-VL-2B 在浏览器 WebGPU 上实现实时视频字幕](#item-tech-news-17) ⭐️ 7.0/10
18. [开源测试时扩展与代理群实现，模拟 OpenAI 最新成果](#item-tech-news-18) ⭐️ 7.0/10
19. [中国团队称光纤实时传输速率达 3.2 Pb/s](#item-tech-news-19) ⭐️ 7.0/10
20. [广电总局：IPTV 应开机看全屏直播，不得播放开机广告](#item-tech-news-20) ⭐️ 7.0/10
21. [波士顿动力员工联名请愿阻止向 ICE 售机器狗](#item-tech-news-21) ⭐️ 7.0/10
22. [🤖 Anthropic 确认部分内部系统遭研究人员访问，声称客户对话与模型权重未受影响](#item-tech-news-22) ⭐️ 7.0/10
23. [Google 睡眠框架助大模型持续学习缓解遗忘](#item-tech-news-23) ⭐️ 7.0/10

**财经新闻**
1. [泡泡玛特三季度营收近腰斩，Labubu 热度消退](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Anthropic 招聘经理停用编程面试](https://felixrieseberg.com/hunger-beats-tenure-advice-for-junior-engineers/) ⭐️ 9.0/10

Anthropic stops using coding interviews as Claude AI surpasses human performance, signaling a major shift in hiring and development workflows.

telegram · zaihuapd · 10月28日 01:46

**标签**: `#AI hiring`, `#software engineering`, `#paradigm shift`, `#developer tools`

---

<a id="item-tech-news-2"></a>
### [DeepMind 发布 Genie 4 世界模型](https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/) ⭐️ 8.0/10

DeepMind 于 2026 年 10 月发布 Genie 4，一种能够从文本提示生成一致、逼真视频和音频的下一代世界模型，现向可信测试者开放研究预览，随后面向 Project Genie Ultra 订阅者以及 Gemini API 和 AI Studio 合作伙伴提供，生成内容带有 SynthID 水印。该模型依赖 Gemini 3.8 Flash 作为引导 Agent，负责拆解多步任务，旨在生成包含环境音和可交互对话的多模态内容。社区反馈指出，模型在保持画面内一致性方面表现良好，但当物体移出画面或出现细节变化时，一致性会下降，且音频生成偶尔出现错误（如提示 saxophone 却生成 clarinet），这削弱了其“强世界模型”方面的宣称。

hackernews · acossta · 10月27日 16:06 · [社区讨论](https://news.ycombinator.com/item?id=50261319)

**「背景」** DeepMind 的 Genie 4 构建在 Gemini 家族模型之上，利用 Gemini Omni 和 Gemini 3.8 Flash 实现实时交互式世界模拟，从文本提示生成逼真的视频和原生音频 Earlier world‑simulation efforts such as Tencent&\#x27;s open‑weight HY‑World 2.0 and previous Genie versions demonstrated the feasibility of multi‑modal 3D environment generation, providing the foundation for Genie 4&\#x27;s enhanced consistency, physics, and steering capabilities.

**「影响」** 开发者可以通过 Gemini API 调用 Genie 4 生成带水印的多模态视频和音频，但需注意模型在画面外变化时的一致性问题，这可能限制其在需要严格连续性的应用中的使用。

**「社区讨论」** 有评论者指出，Genie 4 在保持画面内一致性方面尚可，但当物体移出画面或出现细节变化时，生成结果会出现错误（如第二座城堡出现、骑车人头盔出现），这质疑了其被宣称的‘强世界模型’能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/">Genie 4: A new generation of world simulation - deepmind.google</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/google-deepmind/introducing-genie-4/">We’re announcing Genie 4, our new world model for real-time ...</a></li>
<li><a href="https://techcrunch.com/2026/10/27/googles-genie-4-world-model-adds-audio-more-realistic-worlds-and-real-time-steering/">Google’s Genie 4 world model adds audio, more realistic ...</a></li>
<li><a href="https://github.com/Tencent-Hunyuan/HY-World-2.0">GitHub - Tencent-Hunyuan/HY-World-2.0: HY-World 2.0: A Multi ...</a></li>
<li><a href="https://hyworld.dev/">HY World Model 2 - AI 3D World Generator｜HY World 2 / HY-World 2...</a></li>
<li><a href="https://huggingface.co/tencent/HY-World-2.0">tencent/HY-World-2.0 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#Genie 4`, `#World Simulation`, `#Video Generation`, `#AI Research`, `#Tencent HY-World`

---

<a id="item-tech-news-3"></a>
### [亚马逊因持续失败裁撤 AI 部门](https://futurism.com/artificial-intelligence/amazon-ai-division-failure-nova) ⭐️ 8.0/10

该条目称亚马逊因持续失败正在裁撤其 AI 部门。受影响的具体团队、人员规模、裁撤时间表及后续 AI 战略等细节未在提供的来源中说明。由于原文内容不可用，上述裁撤计划尚未得到独立验证。

hackernews · dpflan · 10月27日 16:25 · [社区讨论](https://news.ycombinator.com/item?id=50261589)

**「背景」** 亚马逊作为全球主要的科技企业，长期在人工智能领域进行研发和投资。近期其 AI 部门面临持续的项目交付与商业化挑战，导致内部组织调整。

**「社区讨论」** 评论者 Foxhuls 指出该文章实际发表于 7 月 29 日，与条目所示日期不一致，提示读者注意时效性。评论者 bondolo 称自己曾作为 Amazon Devices 团队成员在“转向 AI”策略下被裁，并认为除 Graviton/Trainium 工作外，亚马逊的 AI 努力分散且投入不足；以上均为个人观点或经历，非已证实事实。

**标签**: `#Artificial Intelligence`, `#Cloud Computing`, `#Corporate Strategy`, `#AI Research`, `#Software Engineering`

---

<a id="item-tech-news-4"></a>
### [基于 ZeRO-3 与 LoRA 的大规模自蒸馏开源方案](https://www.reddit.com/r/MachineLearning/comments/1xh083s/selfdistillation_with_an_ema_teacher_at_scale/) ⭐️ 8.0/10

发布了一个开源仓库，实现了在 ZeRO-3 和 LoRA（PEFT）环境下可扩展的 EMA 教师自蒸馏（Self-distillation）技术。该方法通过共享并冻结主干模型，仅维护两个轻量级适配器（学生适配器和作为其指数移动平均的教师适配器），解决了大规模模型中同时持有教师和学生模型带来的显存和延迟问题。该仓库提供了稳健的 SDFT 实现、适配器切换机制、EMA 教师检查点保存与恢复功能，并配置了优化后的 DeepSpeed 配置以减少显存峰值。项目已在 Qwen3.5 和 ToolAlpaca 上进行了测试验证。

reddit · r/MachineLearning · /u/ifaposto · 10月27日 18:16

**「背景」** 传统的自蒸馏方法通常依赖指数移动平均（EMA）教师来提供同步且稳定的评判信号。然而，随着模型规模扩大，在 GPU 上同时驻留完整的教师模型和学生模型会导致显著的显存开销、通信延迟和训练吞吐量下降。为解决这一瓶颈，参数高效微调（PEFT，如 LoRA）技术被引入，但将其与 ZeRO-3 分布式训练及 EMA 教师机制无缝结合需要特定的工程支持。

**「影响」** 该开源仓库降低了在大规模模型上应用自蒸馏技术的工程门槛，开发者可以通过即插即用的方式在 ZeRO-3 集成环境下高效训练 LoRA 适配器，显著减少显存占用。但需要注意的是，该方案依赖于特定的 TRL 和 DeepSpeed 框架版本，用户在集成到现有流水线时需关注适配器切换与检查点恢复的兼容性。

**标签**: `#MachineLearning`, `#SelfDistillation`, `#ZeRO-3`, `#LoRA`, `#OpenSource`

---

<a id="item-tech-news-5"></a>
### [微软修复 Authenticator 安卓版高危漏洞 CVE-2026-80097](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2026-80097) ⭐️ 8.0/10

微软已发布 Microsoft Authenticator 安卓版 6.2606.4246 修复高危漏洞 CVE-2026-80097。该漏洞允许已安装的恶意应用在无需申请安卓权限的情况下，窃取已登录工作账户的令牌。研究人员指出攻击无需用户进一步操作，但微软认为攻击者仍需诱使用户完成身份验证。微软首次公告时表示未发现该漏洞被实际利用。

telegram · zaihuapd · 10月27日 12:04

**「漏洞背景」** Microsoft Authenticator 是 Android 设备上广泛使用的身份验证应用，支持工作账户和个人账户的单点登录。其 broker 组件负责处理身份验证令牌的分发与管理。此前类似漏洞（如 CVE-2024-6387 等）也曾影响身份验证应用的令牌安全机制。

**「影响」** 企业 IT 和用户应尽快更新至 6.2606.4246 或更高版本，以防止恶意应用在无权限情况下获取工作账户令牌。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://windowsforum.com/news/cve-2026-80097-update-microsoft-authenticator-for-android-to-block-work-token-theft.450026/">CVE-2026-80097: Update Microsoft Authenticator for Android to ...</a></li>
<li><a href="https://thehackernews.com/2026/10/microsoft-authenticator-flaw-let.html">Microsoft Authenticator Flaw Let Permissionless Android Apps ...</a></li>
<li><a href="https://cybersecuritynews.com/microsoft-authenticator-flaw/">Microsoft Authenticator Flaw Lets Malicious Android Apps ...</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#Microsoft`, `#Android`, `#authentication`

---

<a id="item-tech-news-6"></a>
### [Classification of Finite Simple Groups Formalized in Lean](https://cfsg.axiommath.ai/) ⭐️ 7.5/10

Formalization of the Classification of Finite Simple Groups in Lean, creating a reusable library for mathematical proofs.

hackernews · pfdietz · 10月27日 16:29 · [社区讨论](https://news.ycombinator.com/item?id=50261647)

**标签**: `#mathematical-formalization`, `#proof-assistant`, `#formal-verification`, `#computer-science`

---

<a id="item-tech-news-7"></a>
### [极客湾发布六款旗舰手机芯片能效横评](https://www.bilibili.com/video/BV1kMxM6FECM/) ⭐️ 7.5/10

A benchmark comparison of six flagship smartphone chipsets&\#x27; energy efficiency, relevant for mobile AI/ML optimization and hardware performance.

telegram · zaihuapd · 10月27日 10:53

**标签**: `#energy efficiency`, `#mobile chips`, `#AI on-device`, `#benchmark`, `#smartphone hardware`

---

<a id="item-tech-news-8"></a>
### [triton-lang/triton released v3.9.0](https://github.com/triton-lang/triton/releases/tag/v3.9.0) ⭐️ 7.0/10

Triton v3.9.0 introduces atomic load and store operations with proper memory ordering, broadening support for concurrent GPU kernel development.

github · warrendeng · 10月27日 18:56

**标签**: `#triton`, `#gpu-kernels`, `#atomic-operations`, `#parallel-programming`

---

<a id="item-tech-news-9"></a>
### [Tailscale SSH 安全调查与修复更新](https://tailscale.com/ssh-investigation-update) ⭐️ 7.0/10

Tailscale 发布了针对 SSH 漏洞的安全调查和修复更新，该漏洞影响使用特定 ACL 配置的节点。更新说明该漏洞仅在 ACL 允许通过 Tailscale SSH 访问节点但未授予 sudo/root 权限时才适用；完全没有 SSH 访问权限的节点不会受到影响。Tailscale 建议应用修复并审查 ACL 策略以降低风险。

hackernews · figmert · 10月27日 19:55 · [社区讨论](https://news.ycombinator.com/item?id=50264857)

**「背景」** Tailscale SSH 提供基于 Tailscale 网络的远程 SSH 访问，依赖 ACL 控制哪些用户可以连接到目标节点。ACL 配置决定了用户在获得 SSH 权限后是否能进一步获得 sudo 或 root 权限，这是本次漏洞评估的关键点。

**「影响」** 使用 Tailscale SSH 并配置了允许 SSH 访问但未授予 sudo 权限的 ACL 的组织可能面临权限提升攻击；应用 Tailscale 提供的修复并调整 ACL 设置是必要的缓解措施。

**「社区讨论」** 一名资深用户（minimaltom）指出漏洞仅影响 ACL 允许 SSH 访问但未授予 sudo 权限的节点；其他用户（modeless、andix 等）则认为 Tailscale SSH 增加了攻击面，建议禁用该功能并依赖传统的 OpenSSH 实现。

**标签**: `#tailscale`, `#ssh`, `#security`, `#vulnerability`, `#infrastructure`

---

<a id="item-tech-news-10"></a>
### [Survival LLM：本地化应急知识检索系统](https://www.brangus.io/survival-llm) ⭐️ 7.0/10

Survival LLM 是一个自托管的本地化 AI 助手，配备了针对应急场景的精选知识库，通过基于检索的搜索而非纯生成来生成实用建议，从而降低幻觉风险。该项目目前为开源工具，用户可直接在个人电脑上运行，无需云服务。社区讨论中，用户报告称其在离线时能提供部分正确的应急指导，但也指出生成内容可能存在错误。

hackernews · Luc · 10月27日 19:55 · [社区讨论](https://news.ycombinator.com/item?id=50264853)

**「背景」** 自托管 LLM 使 AI 模型能够在无网络环境下运行，但纯文本生成易产生幻觉。搜索式检索系统通过将查询与 curated 知识库匹配，将 LLM 转变为信息检索工具，而非答案生成器。类似的离线 AI 工作流（如 Project Nomad）和本地运行的模型（如 Granite、Qwen）已在低连接场景中得到应用。

**「影响」** 对于信号弱或无信号的地区用户而言，该系统提供了一个可信的离线应急指南，减少了因 LLM 错误而导致的安全风险。开发者可以利用其检索架构构建其他领域的离线知识应用，而无需完全依赖生成式 AI 的输出。

**「社区讨论」** 评论者就 LLM 作为搜索工具而非权威来源的适用性展开了辩论。一些用户赞赏其将 LLM 用于语义搜索以发现相关资料，而另一些人则警告纯生成内容可能存在严重缺陷。也有人提到他们使用 Granite 和 Qwen 等模型结合 curated 资源，实现了类似的离线工作流程。

**标签**: `#self-hosted AI`, `#offline knowledge retrieval`, `#emergency preparedness`, `#LLM hallucination`

---

<a id="item-tech-news-11"></a>
### [Python 实验性 JIT 编译器被移除](https://lwn.net/SubscriberLink/1102102/0c00e4d550f25f8c/) ⭐️ 7.0/10

Python 的实验性即时编译器（JIT）将被移除，因其未能满足新 PEP 提案的要求。该 JIT 曾被寄望能抵消自由线程带来的性能损耗，并包含自动引用计数操作消除、基于类型的特化优化等高级优化。LWN 报道称，这一决定标志着 Python 性能路线图的一个实验分支终结。

hackernews · f311a · 10月27日 11:17 · [社区讨论](https://news.ycombinator.com/item?id=50257419)

**「背景」** Python 的实验性 JIT 编译器在 2024 年被合入 CPython 3.13，但从未通过 PEP 744 的正式审议，因此被视为实验特性。 它的移除意味着开发者将失去该特性带来的潜在性能提升，尤其是在免锁线程的 CPU 密集工作负载上。

**「影响」** 依赖实验性 JIT 进行性能优化的开发者需转向 Cython 等成熟工具，或等待后续官方性能改进方案；自由线程特性的性能表现将在没有 JIT 辅助的情况下面临更大挑战。

**「社区讨论」** 社区讨论集中在替代方案：有人建议通过装饰器内联 Cython 代码以获得 C 级速度；也有开发者质疑为何 Ruby 和 JavaScript 能成功实现 JIT 而 Python 多次失败，认为可能涉及资金投入和语言设计复杂度的差异。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://peps.python.org/pep-0744/">PEP 744 – JIT Compilation | peps.python.org</a></li>
<li><a href="https://daily.dev/posts/python-s-experimental-jit-to-be-removed-2qgwrdoly">Python&#x27;s experimental JIT to be removed - daily.dev</a></li>

</ul>
</details>

**标签**: `#Python`, `#JIT`, `#performance`, `#programming-languages`, `#software-engineering`

---

<a id="item-tech-news-12"></a>
### [维基百科清理 AI 生成内容引发社区讨论](https://spectrum.ieee.org/wikipedia-wikiproject-ai-writing-cleanup) ⭐️ 7.0/10

维基百科正在开展清理 AI 生成内容的行动，社区成员对此既有支持也有争议。一位用户报告称，自己尝试修复维基百科上的低质量 AI 编辑后，修改被维基百科自己的 AI 机器人立即回滚。评论中提到，AI 已从需要清理的对象转变为帮助清理的工具，但其在平台上的角色仍在演变中。由于原始报道内容不可用，以上信息主要来自社区评论。

hackernews · rbanffy · 10月27日 11:08 · [社区讨论](https://news.ycombinator.com/item?id=50257326)

**「背景」** 维基百科自 2022 年起通过 WikiProject AI Cleanup 等社区组织应对 AI 生成内容的质量问题，包括自动检测和清理 AI 撰写的条目。tool-1-1 中记录的 VWF bot log 等自动化工具显示，维基百科已建立起系统化的 AI 内容监测机制。tool-1-2 报道的 IEEE Spectrum 文章（Strickland 执笔，2026 年 10 月 21 日发布）进一步说明了维基百科编辑社区在保持人工撰写内容的同时，逐步将 AI 纳入清理流程的政策演变。

**「影响」** 维基百科使用 AI 工具进行清理可能与人工编辑产生冲突，如一位用户修复 AI 内容后被 AI 机器人回滚的案例所示，这可能影响志愿者的编辑积极性和人机协作的平衡。

**「社区讨论」** 评论中有人欣赏维基百科清理 AI 内容的努力，但也有人分享了被 AI 机器人回滚编辑的挫折经历，反映出自动化清理与人工判断之间的张力。还有评论指出，某些教育项目中的参与者可能无意中引入了大量低质量 AI 内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup">Wikipedia : WikiProject AI Cleanup - Wikipedia</a></li>
<li><a href="https://tildes.net/~tech/1wkw/how_wikipedias_editors_keep_the_online_encyclopedia_human_written">How Wikipedia ’s editors keep the online encyclopedia human- written ...</a></li>

</ul>
</details>

**标签**: `#Wikipedia`, `#AI-generated content`, `#content moderation`, `#knowledge quality`

---

<a id="item-tech-news-13"></a>
### [手动实现 Transformer 反向传播教程在 PyTorch 中发布](https://www.reddit.com/r/MachineLearning/comments/1xh1z1p/understanding_transformer_autograd_by_building_it/) ⭐️ 7.0/10

用户 /u/ifaposto 发布了一个最小化且自包含的 PyTorch 实现项目，手动实现了基于 Transformer 的分类器的自动微分功能。该项目包含 GitHub 代码仓库（https://github.com/ifiaposto/transformer\_custom\_autograd/tree/main）和 Google Colab 笔记本（https://colab.research.google.com/drive/1Lt7JDYG44p7YHJ76eRH\_8QFOPkkoIwhn），旨在帮助开发者理解自动微分在 Transformer 模型中的运行机制，包括自定义反向传播和梯度在注意力块中的流动方式。

reddit · r/MachineLearning · /u/ifaposto · 10月27日 19:20

**「Transformer 手动自动微分的背景」** 在常规的 PyTorch Transformer 训练中，梯度通常由自动微分机制在反向传播时自动计算。理解这一过程的前提，是知道如何让自定义算子或模块接入 torch.autograd.Function 并编写手写反向过程。该项目提供了一个极简、自包含的手写自动微分实现，用于 Transformer 分类器，并附带 GitHub 代码与可运行 Colab 笔记本，目的是帮助用户理解注意力模型中 autograd 的底层行为和梯度流动。

**「影响」** 该教程为 AI 从业者提供了一个实践参考，有助于深入理解 Transformer 模型的梯度流动机制，特别适用于需要编写自定义反向传播的开发者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ifiaposto/transformer_custom_autograd">GitHub - ifiaposto/transformer_custom_autograd: A minimal ...</a></li>

</ul>
</details>

**标签**: `#PyTorch`, `#Transformers`, `#Autograd`, `#Deep Learning`, `#Tutorial`

---

<a id="item-tech-news-14"></a>
### [Papers with Code is now open-source \[P\]](https://www.reddit.com/r/MachineLearning/comments/1xgoadu/papers_with_code_is_now_opensource_p/) ⭐️ 7.0/10

A community-driven, open-source revival of Papers with Code for tracking trending AI research and benchmarks, now available for public contribution.

reddit · r/MachineLearning · /u/NielsRogge · 10月27日 09:54

**标签**: `#open-source`, `#machine-learning`, `#research-tools`, `#fastapi`, `#react`

---

<a id="item-tech-news-15"></a>
### [Ψ-0.6：统一视觉语言世界模型引入自适应思维流](https://www.reddit.com/r/MachineLearning/comments/1xgwq9u/%CF%8806_adaptive_streams_of_thought_in_a_unified/) ⭐️ 7.0/10

研究人员和开发者现在可以使用开源的 Ψ-0.6，这是一个统一的视觉语言世界模型，能够在文本、深度、运动、相机姿态和想象场景之间自适应推理。该模型在 MindCube 空间推理和 FlowBench 运动预测基准测试中超越现有开源模型，并从模拟室环境转移到真实机械臂桌面任务。代码和演示已在 GitHub（https://github.com/neuroailab/psi-0.6）和官网提供。

reddit · r/MachineLearning · /u/FaeriaManic · 10月27日 16:09 · [社区讨论](https://www.reddit.com/r/MachineLearning/comments/1xgwq9u/%CF%8806_adaptive_streams_of_thought_in_a_unified/)

**「背景」** 链式思维（Chain-of-Thought）最初是通过在语言模型生成推理步骤来改善文本推理能力，但它仅限于符号化的词语推理，无法直接处理物理世界的感知和运动信息。近年来，统一的视觉-语言世界模型旨在将感知、语言和几何推理整合到单一架构中，但如何让模型自主选择使用哪种推理模态（如深度、运动、相机姿态或想象场景）仍然是长期悬而未决的课题。Ψ-0.6 声称通过强化学习机制学习自适应地组合多种推理流，从而在空间推理和物体运动预测等任务上取得进展。

**「影响」** 开发者可直接下载 Ψ-0.6 代码并集成以实现跨模态感知与机器人桌面任务的零-shot 仿真到现实转移，但性能提升基于作者报告的基准测试结果，尚未经独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2610.32177">[2610.32177] ||Psi;$-0.6: Adaptive Streams of Thought in a ...</a></li>
<li><a href="https://huggingface.co/papers/2610.32177">Ψ-0.6: Adaptive Streams of Thought in a Unified Vision ...</a></li>
<li><a href="https://github.com/awwkl/psi-0.6">Ψ-0.6: Adaptive Streams of Thought - GitHub</a></li>

</ul>
</details>

**标签**: `#AI/ML`, `#vision-language models`, `#world models`, `#robotics`, `#open source`

---

<a id="item-tech-news-16"></a>
### [LiquidAI 发布 LFM3-1.7B 三混合架构模型](https://www.reddit.com/r/LocalLLaMA/comments/1xgy8s3/liquidailfm317b_hugging_face/) ⭐️ 7.0/10

LiquidAI 于 2026 年 10 月发布 LFM3-1.7B，基于其新提出的 tri-hybrid（三混合）架构，包含 24 层：13 个门控短卷积、5 个滑动窗口注意力、6 个全局注意力，上下文窗口 256K tokens，词表 128K，支持英、中、阿、法、德、意、日、韩、葡、西、越、泰、印尼、印地、俄、波等语言。在 4-bit 精度下约占用 1GB 内存，适合手机或笔记本运行；已通过 llama.cpp 的 GGUF 支持合并。该模型定位为本地智能体、工具调用和领域微调，不建议用于复杂多步推理或 agentic coding。

reddit · r/LocalLLaMA · /u/jacek2023 · 10月27日 17:04

**「LFM3 系列与 tri-hybrid 架构背景」** LiquidAI 在 Hugging Face 上同步发布了 LFM3 系列多个子模型：LFM3-VL-2B（视觉语言，首个支持视频输入的 LFM 视觉模型）、LFM3-Audio-2B（音频模型，引入 LiquidCodec 音频分词器）、LFM3-Omni-2B（全模态模型）、d1-Omni-2B（决策模型，单前向输出校准答案）、d1-2B（基于 LFM3-VL-2B 的决策模型）。LFM3-1.7B-Base 为预训练检查点，训练数据包含 22T tokens，其中最后 3.5T 为人工筛选的 agentic trace 与工具调用数据，并扩展了上下文窗口至 256K。

**「对本地/边缘 AI 社区的影响」** 该模型为本地智能体、工具调用和领域微调提供了轻量起点，4-bit 下约 1GB 内存使其可在手机或笔记本上运行，降低了本地部署门槛。但作者明确提示该模型不适合复杂多步推理或 agentic coding，用户需注意适用边界。llama.cpp GGUF 支持已合并，进一步降低了本地推理的工程门槛。

**标签**: `#llm`, `#edge-computing`, `#open-source`, `#architecture`

---

<a id="item-tech-news-17"></a>
### [LFM3-VL-2B 在浏览器 WebGPU 上实现实时视频字幕](https://www.reddit.com/r/LocalLLaMA/comments/1xh0otf/realtime_video_captioning_with_lfm3vl2b_running/) ⭐️ 7.0/10

LiquidAI 的 LFM3-VL-2B 视觉语言模型已通过 Hugging Face Spaces 的 WebML 社区演示，在浏览器本地完成实时视频字幕生成，全程无需后端。该演示基于 Hugging Face 上的模型集合与 WebGPU 推理环境。

reddit · r/LocalLLaMA · /u/xenovatech · 10月27日 18:33

**「LFM3-VL-2B 的模型背景」** LFM3-VL-2B 是 Liquid AI 新发布的 LFM3 开放权重模型家族中的视觉语言模型，该家族主打在任意设备上快速运行。它将 LFM 语言主干与 SigLIP2 NaFlex 图像编码器配对，专为设备端快速多模态推理设计；其语言主干 LFM3-1.7B-Base 经两阶段预训练，总计使用 22T 个 token。

**「影响」** 对希望隐私优先、低延迟的多模态本地 AI 应用的开发者而言，该演示表明浏览器端 WebGPU 推理已能承载 2B 级视觉语言模型的实时视频理解工作负载，降低了部署门槛。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/LiquidAI/LFM3-VL-2B">LiquidAI/LFM3-VL-2B · Hugging Face</a></li>
<li><a href="https://docs.liquid.ai/lfm/models/vision-models">Vision Models - Liquid Docs</a></li>
<li><a href="https://www.liquid.ai/blog/lfm3">Introducing LFM3: Every Modality for Specialized Intelligence</a></li>

</ul>
</details>

**标签**: `#WebGPU`, `#local-inference`, `#vision-language-models`, `#browser-ai`, `#multimodal`

---

<a id="item-tech-news-18"></a>
### [开源测试时扩展与代理群实现，模拟 OpenAI 最新成果](https://www.reddit.com/r/LocalLLaMA/comments/1xh4bnd/openais_major_results_over_the_last_3_months_came/) ⭐️ 7.0/10

作者发布了一个基于 agent swarms 的测试时扩展开源框架，声称在 Gemma4-35B 和 Qwen-3.8-27B 上对 BrokenArxiv 基准得分从 14%提升至 65%，在 DeepSWE 上从 9%提升至 52%。推理耗时可从 50 分钟至 30 小时不等，且因成本高未在前沿或大型开源模型上进行测试。

reddit · r/LocalLLaMA · /u/Ryoiki-Tokuiten · 10月27日 20:47

**「背景」** 测试时扩展（test-time scaling）是指在推理阶段通过增加计算量——例如让多个代理协作、重复采样或延长推理时间——来提升模型答案质量的技术。OpenAI 此前曾在 ExploitGym 基准框架上让大量 LLM 代理完成其描述为“不可能任务”的测试，而 BrokenArXiv 是 MathArena 上的基准赛道，得分以答对题目的百分比表示。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/security/2026/08/how-openai-let-a-mob-of-llm-agents-game-a-test-and-ransack-hugging-face/">How OpenAI let a mob of LLM agents game a test and... - Ars Technica</a></li>
<li><a href="https://atlas.kevinhu.io/benchmarks/brokenarxiv-02-2026-matharena">BrokenArXiv 02/2026 leaderboard — Benchmark Atlas</a></li>

</ul>
</details>

**标签**: `#test-time scaling`, `#agent swarms`, `#open-source AI`, `#benchmark evaluation`, `#LLM inference`

---

<a id="item-tech-news-19"></a>
### [中国团队称光纤实时传输速率达 3.2 Pb/s](https://www.tomshardware.com/networking/3-2-pb-s-real-time-optical-fiber-transfer-speed-world-record-claimed-by-chinese-team-speed-fast-enough-to-download-more-than-20-000-4k-movies-in-one-second) ⭐️ 7.0/10

中国团队宣布，使用 24 芯商用兼容光纤实现了每秒 3.2 Pb 的实时传输速率，足以在一秒内传输超过 2 万部 4K 电影，较其今年早前的 2.5 Pb/s 纪录提升约 30%。该实验验证了空分复用以及 S+C+L 多波段技术，而非依赖实验性设备。

telegram · zaihuapd · 10月27日 03:45

**「中国团队刷新光纤实时传输速率纪录」** 中国团队在 10.3 公里长的 24 芯光纤上实现了 3.2 Pb/s 的实时传输速率，超过其去年创下的 2.5 Pb/s 纪录近 30%。该成绩验证了空分复用及 S+C+L 多波段传输技术在商用兼容硬件上的可行性。

**「设备兼容性要求」** 该速率表明当前光纤交换和传输硬件必须能够处理数十倍的带宽，迫使设备厂商在短期内升级或替换其产品以支持如此高速的实时传输。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.notebookcheck.net/China-claims-3-2-Pb-s-optical-fiber-record-could-send-20-000-4K-movies-per-second.1434319.0.html">China claims 3 . 2 Pb / s optical fiber record... - Notebookcheck News</a></li>
<li><a href="https://www.tomshardware.com/networking/3-2-pb-s-real-time-optical-fiber-transfer-speed-world-record-claimed-by-chinese-team-speed-fast-enough-to-download-more-than-20-000-4k-movies-in-one-second">3 . 2 Petabits per second real - time optical fiber ... | Tom&#x27; s Hardware</a></li>

</ul>
</details>

**标签**: `#optical-fiber`, `#telecommunications`, `#high-speed-networking`, `#spatial-division-multiplexing`, `#network-infrastructure`

---

<a id="item-tech-news-20"></a>
### [广电总局：IPTV 应开机看全屏直播，不得播放开机广告](https://www.nrta.gov.cn/art/2026/10/27/art_1588_74296.html) ⭐️ 7.0/10

China&\#x27;s broadcasting regulator mandates that IPTV and smart TVs boot directly to live TV without ads, forcing significant software and hardware UX updates across the consumer electronics industry.

telegram · zaihuapd · 10月27日 05:59

**标签**: `#IPTV`, `#Smart TV`, `#Regulation`, `#User Experience`, `#Technology Industry`

---

<a id="item-tech-news-21"></a>
### [波士顿动力员工联名请愿阻止向 ICE 售机器狗](https://arstechnica.com/ai/2026/10/boston-dynamics-employees-want-to-block-sale-of-robot-dogs-to-ice/) ⭐️ 7.0/10

Over 300 Boston Dynamics employees petitioned leadership to cancel a $1.3M DHS contract supplying four modified Spot robots to ICE for detection tasks, citing ethical concerns; management declined, stating the robots would not be weaponized.

telegram · zaihuapd · 10月27日 09:52

**标签**: `#robotics`, `#tech ethics`, `#employee activism`, `#government contracts`, `#Boston Dynamics`

---

<a id="item-tech-news-22"></a>
### [🤖 Anthropic 确认部分内部系统遭研究人员访问，声称客户对话与模型权重未受影响](https://www.washingtonpost.com/technology/2026/10/26/researchers-cybersecurity-start-up-cathedral-got-inside-anthropic/) ⭐️ 7.0/10

Security researchers from Cathedral accessed parts of Anthropic&\#x27;s internal systems through a third-party software vulnerability, exposing some sensitive data but not customer conversations or model weights.

telegram · zaihuapd · 10月27日 12:43

**标签**: `#AI security`, `#Anthropic`, `#cybersecurity`, `#data breach`, `#responsible disclosure`

---

<a id="item-tech-news-23"></a>
### [Google 睡眠框架助大模型持续学习缓解遗忘](https://research.google/blog/the-sleep-framework-a-new-way-for-llms-to-retain-knowledge-in-continual-learning/) ⭐️ 7.0/10

Google Research 提出「睡眠框架」，在大语言模型的持续学习中引入离线巩固阶段，让模型将短期上下文转化为长期参数，以此缓解灾难性遗忘。该框架在 1000 万 token 长上下文、持续翻译与数学推理等测试中，相较于 GPT-4 与 SFT 等基线展示了性能提升。模型在主动交互与离线睡眠间周期切换，以实现知识的离线巩固。这是一个研究级提案，目前的性能报告为 Google Research 的内部评估结果。

telegram · zaihuapd · 10月28日 01:46

**「背景：持续学习中的灾难性遗忘」** 大语言模型在持续学习（continual learning）中面临一个核心难题：当模型不断吸收新知识时，往往会发生“灾难性遗忘”（catastrophic forgetting），即新学到的内容会覆盖或削弱 previously 掌握的旧知识。传统的静态模型训练完成后知识即固化，而持续学习要求模型在部署后仍能不断更新参数，这使得新旧知识之间的冲突尤为突出。Google Research 提出的“睡眠框架”正是受人类睡眠中记忆巩固机制的启发，通过在主动交互与离线巩固之间周期性切换，让模型在“睡眠”阶段将短期上下文转化为长期参数，从而在不遗忘的前提下持续学习。这一思路并非首次将生物机制引入 AI，但将其系统化为可部署的框架并在大规模测试中验证，是该方向的重要推进。

**「影响」** 据 Google Research 称，该框架在 1000 万 token 长上下文、持续翻译与数学推理等测试中相较于 GPT-4 与 SFT 等基线展现出更强的性能，这意味着开发者在使用该框架进行持续微调时，可潜在地降低重训成本，但该结果为内部评估，尚未通过独立实验验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ai-digest-1.com/news/google-research-unveils-sleep-framework-for-continual-learning-in-llms-19815">Google Research Unveils Sleep Framework for Continual ...</a></li>
<li><a href="https://todayforai.com/en/story/story-ac73a1ee-65e">Google Research Introduces &#x27;Sleep Phase&#x27; Framework to Fix LLM ...</a></li>
<li><a href="https://research.google/blog/">Latest News from Google Research Blog - Google Research</a></li>

</ul>
</details>

**标签**: `#continual learning`, `#catastrophic forgetting`, `#large language models`, `#Google Research`, `#sleep framework`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [泡泡玛特三季度营收近腰斩，Labubu 热度消退](https://asia.nikkei.com/business/consumer/pop-mart-s-revenue-halves-in-q3-as-labubu-craze-cools) ⭐️ 7.0/10

泡泡玛特于 10 月 27 日向港交所提交三季度报告，营收同比下降 45%至 50%，Labubu 热度消退导致营收近乎腰斩。

telegram · zaihuapd · 10月27日 14:30

**「背景」** 泡泡玛特是香港上市的设计玩具及盲盒公司，以 Labubu 等角色 IP 闻名。

**「影响」** 公司预计下半年毛利率较上半年收窄最多 2 个百分点，可能影响投资者对全年利润的预期。

**标签**: `#earnings`, `#consumer goods`, `#asia markets`, `#collectibles`

---