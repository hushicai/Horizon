---
layout: default
title: "Horizon Summary: 2026-11-08 (ZH)"
date: 2026-11-08
lang: zh
---

> 从 39 条内容中筛选出 17 条重要资讯。

---

**科技新闻**
1. [Need for Speed Underground 2 在浏览器中可玩](#item-tech-news-1) ⭐️ 8.0/10
2. [每台 Mac 都预装未公开的家庭成员分类器](#item-tech-news-2) ⭐️ 8.0/10
3. [内蒙古 800MW 风电 AI 园区试点 800V 直流与无冷却机制冷](#item-tech-news-3) ⭐️ 8.0/10
4. [苹果 iPhone Duo 适配应用突破 10 万个](#item-tech-news-4) ⭐️ 8.0/10
5. [GitHub 推出 Rubicon 新 Git 存储架构，支持每秒 7200 次推送](#item-tech-news-5) ⭐️ 8.0/10
6. [Running a law firm on Free software](#item-tech-news-6) ⭐️ 7.5/10
7. [微软研究院 AI Frontiers 团队解散](#item-tech-news-7) ⭐️ 7.0/10
8. [10 美元 OpenStick 自建家庭实验室实践分享](#item-tech-news-8) ⭐️ 7.0/10
9. [MaxxBench – &quot;Nice DeepSWE score. But is it true?&quot;](#item-tech-news-9) ⭐️ 7.0/10
10. [Discord 客户端弃用 Electron 实现原生化与 RAM 占用降幅](#item-tech-news-10) ⭐️ 7.0/10
11. [Asahi Linux Progress Linux 7.3](#item-tech-news-11) ⭐️ 7.0/10
12. [土耳其利用 TraceART AI 平台追回 100 件流失文物](#item-tech-news-12) ⭐️ 7.0/10
13. [DeepSeek 网页与 API 部分中断，已实施修复](#item-tech-news-13) ⭐️ 7.0/10
14. [Claude Code 疑似泄露用户邮箱](#item-tech-news-14) ⭐️ 7.0/10

**财经新闻**
1. [软银与 ABB 拟分拆中国业务冲救 54 亿美元机器人交易](#item-finance-news-1) ⭐️ 8.0/10
2. [伯克希尔·哈撒韦第三季度回购加速，盈利下滑](#item-finance-news-2) ⭐️ 7.0/10
3. [全国 3.35 万座寺院启动财务大检查](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Need for Speed Underground 2 在浏览器中可玩](https://nfsu2.xyz/) ⭐️ 8.0/10

社区驱动的 AI 辅助浏览器移植让 Need for Speed Underground 2 可在浏览器中直接运行。该项目通过逆向工程和 WebGPU 实现现代图形，支持手机浏览器以及在 Linux 上需要启用不安全的 WebGPU 选项才能在 Chromium 中运行。虽然该网站未经授权且可能面临下架，但它展示了抢救遗留游戏的潜在可能性。

hackernews · fluxusars · 11月7日 09:36 · [社区讨论](https://news.ycombinator.com/item?id=50403052)

**「背景」** Need for Speed Underground 2 是 2000 年代初期发布的赛车游戏，自发售后即被视为遗留软件，迄今未有官方后续支持。此前只有 PC 或 Xbox 等原生平台可玩，社区需要通过浏览器实现来保存和重玩该作品。

**「影响」** 玩家可以在无需安装原版即可通过浏览器在手机或 Linux 设备上体验 Need for Speed Underground 2，从而实现对遗留游戏的保存与访问。

**「社区讨论」** 社区成员对该非法网站的可玩性表示惊叹，但也担忧其侵权风险以及在 Linux 上需要启用不安全的 WebGPU 选项才能正常运行。

**标签**: `#reverse engineering`, `#browser gaming`, `#AI‑assisted development`, `#abandonware`, `#WebGPU`

---

<a id="item-tech-news-2"></a>
### [每台 Mac 都预装未公开的家庭成员分类器](https://8rank.ai/game/apple-intelligence-personal-knowledge-graph) ⭐️ 8.0/10

安全研究员 infwhispers 发现，自 2022 年起所有 Mac 都在后台运行一对未公开的系统守护进程，持续构建用户的个人知识图谱，记录人际关系、通信模式、位置历史及活动时间线。该功能未在任何用户协议或系统设置中披露，也无法通过标准隐私控制关闭。研究者已发布技术分析及后续跟进报告。

hackernews · infwhispers · 11月7日 09:46 · [社区讨论](https://news.ycombinator.com/item?id=50403097)

**「背景」** Apple 此前在 Photos 应用中已部署人脸识别与关系标注功能，但仅限于用户主动整理的相册范围。新发现的守护进程则在系统层面持续采集跨应用的交互数据，属于 Apple Intelligence 本地推理基础设施的一部分，旨在为 Siri 等本地大模型提供上下文感知能力。

**「影响」** 用户无法知情同意或退出该数据采集，且现有的 macOS 隐私设置（如“完全磁盘访问权限”授权列表）均未暴露这两个守护进程，导致企业合规审计与个人隐私防护均存在盲区。

**「社区讨论」** 评论区核心争议集中在“本地处理是否等同于隐私安全”：作者与部分用户认为未经明确同意的持续建模违背 Jobs 时代“反复以通俗语言征求许可”的原则；另一派认为这是 Siri 理解“给我老板发短信”此类指令所必需的本地上下文，且数据不上传云端。

**标签**: `#privacy`, `#apple`, `#ai`, `#software-engineering`, `#ethics`

---

<a id="item-tech-news-3"></a>
### [内蒙古 800MW 风电 AI 园区试点 800V 直流与无冷却机制冷](https://newsletter.semianalysis.com/p/we-visited-chinas-stargate-in-inner) ⭐️ 8.0/10

SemiAnalysis 报道称，其团队实地访问了中国内蒙古一座由风电驱动的 AI 数据中心园区，总容量 800 兆瓦，其中 120 兆瓦在一年内建成。园区试点了一座 5 兆瓦的固态变压器（SST）原生 800 伏直流供电系统，并采用没有中央冷却机的制冷设计。这些细节来自 SemiAnalysis 的实地报道，并非独立验证的性能数据。

rss · Semianalysis · 11月7日 19:01

**「中国内蒙古 Stargate AI 数据中心园区采用 800V DC SST 技术」** 中国在内蒙古的 Stargate AI 数据中心园区采用了 800V DC 固态变压器（SST）技术，实现了风电供电的 800MW 级别规模。该园区在一年内完成了 120MW 的建设，并采用了无中央冷水机组（chiller-less）的冷却设计。该项目是 800V DC 固态变压器技术在大型 AI 数据中心中的实际应用案例，体现了中国在 AI 基础设施电力架构方面的创新。

**「影响」** 该风力发电 800 兆瓦级 AI 数据中心校园在一年内建成 120 兆瓦，并试点了 5 兆瓦的 SST 原生 800 伏直流配电系统及无中央冷水机组的冷却设计，证明了大规模可再生能源供电的高密度 AI 计算设施的可行性，可能推动其他运营商采用类似的电源和冷却架构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wattai.wattsystems.com/products/6mw-sst">6 MW SST — WattAI Products | WattAI</a></li>
<li><a href="https://www.yiyuesg.com/newsinfo/3102153.html">800 V + Solid - State Transformers : The &quot;Silicon-based Revolution&quot; for...</a></li>
<li><a href="https://cnville.en.made-in-china.com/product/faJRUBtMFgrI/China-Custom-Compact-Solid-State-Transformer-Sst-Ai-Data-Center-Low-Loss-Voltage-800V.html">Custom Compact Solid State Transformer Sst Ai Data Center Low...</a></li>
<li><a href="https://newsletter.semianalysis.com/p/we-visited-chinas-stargate-in-inner">We Visited China’s Stargate in Inner Mongolia</a></li>
<li><a href="https://aitechtrend.com/inner-mongolia-ai-data-centers/">How Inner Mongolia Fuels China’s AI Data Centers with Wind</a></li>
<li><a href="https://www.techtimes.com/articles/323410/20260806/envision-commissions-worlds-largest-ai-data-center-building-using-site-renewables.htm">Envision Commissions World&#x27;s Largest AI Data Center Building ...</a></li>

</ul>
</details>

**标签**: `#data centers`, `#AI infrastructure`, `#power systems`, `#cooling technology`, `#China tech`

---

<a id="item-tech-news-4"></a>
### [苹果 iPhone Duo 适配应用突破 10 万个](https://9to5mac.com/2026/11/06/apple-says-there-are-already-over-100000-apps-built-for-iphone-duo/) ⭐️ 8.0/10

苹果宣布 iPhone Duo 上市两周后，App Store 上已有超过 10 万个适配应用，每天还有数千个优化上线。微软 Office、Zoom、YouTube 等主流应用已完成适配，并在 App Store 显示专属 &quot;Made for iPhone Duo&quot; 标识。

telegram · zaihuapd · 11月7日 02:30

**「iPhone Duo 生态快速增长」** iPhone Duo 作为双屏手机平台自上月推出，开发者在全球 19 个城市举办了数百场工作坊，累计有 2000 多名开发者参与活动，推动了应用的快速适配和优化。

**「平台生态加速」** 超过 10 万个适配应用的快速增长表明 iPhone Duo 正在迅速成为开发者关注的平台，可能吸引更多需要双屏协作的用户和应用场景。

**标签**: `#Apple ecosystem`, `#iPhone Duo`, `#App development`, `#Developer adoption`, `#Hardware platform`

---

<a id="item-tech-news-5"></a>
### [GitHub 推出 Rubicon 新 Git 存储架构，支持每秒 7200 次推送](https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/) ⭐️ 8.0/10

GitHub 发布代号 Rubicon 的新 Git 存储架构，面向大量 AI 智能体并发操作，在内部测试中支持 5000 个智能体同时工作，每秒处理 7200 次推送，读取延迟保持低水平。该架构将 Git 对象存入 Azure Blob Storage，使用 Ref‑CAS 管理引用状态，虚拟副本处理读写，目前处于有限私有预览阶段。

telegram · zaihuapd · 11月7日 14:12

**「背景」** Git 传统上将仓库对象存储在本地磁盘，这在高并发场景下成为性能瓶颈。Rubicon 架构将对象迁移至 Azure Blob Storage 并通过 Ref‑CAS 管理引用状态，以实现可扩展的并发操作。

**「影响」** AI 开发者可在单个仓库上运行数千个并发智能体，每秒达 7200 次推送且延迟低，无需额外分片或外部存储方案。

**标签**: `#GitHub`, `#AI agents`, `#Git storage architecture`, `#distributed systems`, `#software engineering`

---

<a id="item-tech-news-6"></a>
### [Running a law firm on Free software](https://decoded.legal/blog/2026/11/running-a-law-firm-on-free-software-2026-edition/) ⭐️ 7.5/10

An article exploring the feasibility and challenges of operating a law firm entirely on free/open-source software, with community discussion about proprietary vs. open-source solutions and the role of AI in legal services.

hackernews · DeepLogin · 11月7日 09:39 · [社区讨论](https://news.ycombinator.com/item?id=50403066)

**标签**: `#open-source`, `#legal-tech`, `#software-engineering`, `#professional-services`, `#AI-in-law`

---

<a id="item-tech-news-7"></a>
### [微软研究院 AI Frontiers 团队解散](https://hunch.net/?p=13764006) ⭐️ 7.0/10

微软研究院的 AI Frontiers 团队已解散，该团队专注于基础性 AI 研究，随着核心研究员 John Langford 的离职而走向终结。这一变化反映了行业整体从探索性 AI 研究向基于 transformer 的规模化方案的转向，大型科技公司当前普遍将 transformer 路线视为最可靠、最可预测的发展路径。

hackernews · srean · 11月7日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=50406563)

**「背景」** 微软研究院的 AI Frontiers 是一个专注于人工智能基础研究、独立于产品导向的微软 AI 组织的专门研究团队。 该团队最近被转移到微软 AI 旗下，研究自主权受到限制，最终导致其解散。这一组织变革反映了行业内向基于 Transformer 的规模化扩展和大型语言模型开发的转变，优先考虑快速迭代而非探索性研究。

**「影响」** 对于从事基础性、探索性 AI 研究的人员而言，在大型科技公司内部获得资源支持的难度加大。行业资源进一步集中于 transformer 模型的规模化迭代，可能影响非主流技术路线的长期发展。

**「社区讨论」** 社区评论中存在明显分歧。部分评论者认为这是行业理性选择的结果——transformer 路线提供了清晰可预测的投入产出路径；另一些评论者则表达了对探索性研究被边缘化的担忧，认为这可能导致公司错失未来突破性技术的机会，甚至出现&quot;文化破坏&quot;的批评。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://emergent.sh/news/john-langford-exits-microsoft-ai-frontiers">John Langford Exits Microsoft as AI Frontiers Group Closes</a></li>
<li><a href="https://www.indiatoday.in/technology/news/story/microsoft-ai-research-clash-john-langford-quits-declares-ai-frontiers-over-3034334-2026-11-07">Microsoft AI research clash: John Langford quits, declares AI ...</a></li>
<li><a href="https://businessexaminer.ca/victoria-articles/item/microsoft-researcher-john-langford-exits-as-ai-frontiers-group-is-declared/">Microsoft Researcher John Langford Exits as AI Frontiers ...</a></li>

</ul>
</details>

**标签**: `#Microsoft Research`, `#AI research`, `#organizational change`, `#transformer models`, `#technology industry`

---

<a id="item-tech-news-8"></a>
### [10 美元 OpenStick 自建家庭实验室实践分享](https://blog.bosscher.ch/posts/openstick/) ⭐️ 7.0/10

作者在个人博客分享了基于 10 美元 OpenStick 硬件搭建家庭实验室的经验，展示了在极低成本硬件上运行自托管服务的可行性。文章讨论了软件选择策略，包括 RSS 阅读器 Fusion 和轻量级替代 Picoflux，并对比了 OpenStick 与 Raspberry Pi Zero 系列的性能差异。社区讨论集中在硬件获取渠道、PoE 集群扩展形态以及内存受限环境下的软件选型。

hackernews · LaurensBER · 11月7日 18:12 · [社区讨论](https://news.ycombinator.com/item?id=50406670)

**「OpenStick 简介与自托管背景」** OpenStick 是一个基于 Rockchip RK3566 的迷你电脑，尺寸与 USB 闪存棒相当，提供基本的 ARM 处理器、内存和存储接口，常用于自托管和低成本 homelab。它与 Raspberry Pi Zero 系列类似，但价格更低、功耗更小，适合运行轻量级服务。社区在工具中提到了 Fusion（一个 Miniflux 分支）和 Picoflux 等软件，以及使用 OpenStick 构建集群的可能性。相关背景包括现有的 homelab 自动化工具（如 Deployarr）和硬件驱动开发（如 UFI003\_MB\_V02 的调制解调器驱动），这些先前项目帮助用户理解如何快速部署 homelab 环境和配置 OpenStick 硬件。

**「社区讨论」** 评论者指出 OpenStick 性能接近 Raspberry Pi Zero 2，但期望出现支持 PoE 供电、可直接插入交换机 RJ45 接口的垂直板卡形态以便组建集群。有开发者因 Fusion 界面优于 Picoflux 考虑迁移，同时确认 512MB 内存足以运行多种轻量级工作负载，关键在于选择高效编写的软件。另有用户询问 OpenStick 硬件购买渠道。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=MTjpUXQiHfk">Deployarr 4: Docker Homelab in Minutes (75+ Apps) - YouTube</a></li>
<li><a href="https://github.com/OpenStick/OpenStick/issues/33">modem drivers for UFI003_MB_V02 · Issue #33 · OpenStick / OpenStick</a></li>
<li><a href="https://www.avito.ru/mytischi/bytovaya_elektronika?q=homelab+10">homelab 10 - Купить недорого электронику в Мытищах | Авито</a></li>

</ul>
</details>

**标签**: `#homelab`, `#self-hosting`, `#open source`, `#software engineering`, `#computer systems`, `#hardware`

---

<a id="item-tech-news-9"></a>
### [MaxxBench – &quot;Nice DeepSWE score. But is it true?&quot;](https://maxxbench.unlap.ai/research/why-maxxbench/) ⭐️ 7.0/10

It critiques MaxxBench&\#x27;s reported DeepSWE results, pointing out potential flaws and limited generalizability, and urges caution when adopting the benchmark.

hackernews · antiuniverse · 11月7日 17:19 · [社区讨论](https://news.ycombinator.com/item?id=50406222)

**标签**: `#LLM Benchmark`, `#Software Engineering`, `#DeepSWE`, `#Benchmark Reliability`

---

<a id="item-tech-news-10"></a>
### [Discord 客户端弃用 Electron 实现原生化与 RAM 占用降幅](https://www.windowslatest.com/2026/11/06/every-windows-11-app-should-kill-electron-and-discord-just-showed-why-no-starting-screen-and-70-less-ram-even-with-two-accounts-signed-in/) ⭐️ 7.0/10

Discord 近期发布的 Windows 客户端已彻底弃用 Electron 框架，转而采用原生实现。该版本在两个账户同时登录的情况下，启动屏幕消失且 RAM 占用较 Electron 版本降低约 70%。此次重构旨在验证原生方案在 Windows 11 上的性能优势，并呼吁其他应用考虑同类迁移。

hackernews · thunderbong · 11月7日 11:11 · [社区讨论](https://news.ycombinator.com/item?id=50403507)

**「背景」** Electron 是一个允许开发者使用 HTML、CSS 和 JavaScript 构建跨平台桌面应用的框架，这使得团队无需分别编写原生代码即可在 Windows、macOS 和 Linux 上发布应用。Discord 早期即采用 Electron 以加速多平台发布并复用网页团队的技能树。

**「影响」** 若 Windows 11 的其他应用继续依赖 Electron，用户在多账户或长时间运行场景下可能仍面临较高的内存占用，这可能促使用户转向原生替代品，从而迫使开发者在跨平台便利性与资源效率之间权衡维护成本。有证据表明 Discord 的原生客户端在两账户场景下 RAM 占用显著低于 Electron 版本。

**「社区讨论」** 社区普遍指出 Electron 虽然让小团队利用网页技能快速实现跨平台发布并保持较好无障碍与 IME 支持，但其内存消耗与启动延迟仍是主要痛点。原生方案则需维护多套代码库才能兼顾效率与兼容性。

**标签**: `#Electron`, `#Discord`, `#Performance Optimization`, `#Cross-platform Frameworks`, `#Native Apps`

---

<a id="item-tech-news-11"></a>
### [Asahi Linux Progress Linux 7.3](https://asahilinux.org/2026/11/progress-report-7-3/) ⭐️ 7.0/10

Asahi Linux 7.3 progress report marks synchronized Fedora Asahi Remix releases and addresses hardware and licensing issues, sparking active community debate.

hackernews · ackyshake · 11月7日 05:20 · [社区讨论](https://news.ycombinator.com/item?id=50401867)

**标签**: `#Asahi Linux`, `#Apple Silicon`, `#Linux on macOS`, `#Hardware support`, `#Open source`

---

<a id="item-tech-news-12"></a>
### [土耳其利用 TraceART AI 平台追回 100 件流失文物](https://www.artnews.com/art-news/news/turkey-uses-ai-tech-100-looted-antiquities-us-1234804634/) ⭐️ 7.0/10

土耳其利用 TraceART 人工智能平台从美国追回约 100 件流失文物。该平台结合铅同位素分析、模具形状比对以及 2025 年起启用的全球拍卖站和社交媒体扫描系统，实现了文物的快速定位与追索。

telegram · zaihuapd · 11月7日 03:43

**「背景」** 土耳其自 1980 年以来一直在追回流失文物，累计已回收逾 26700 件。此前的工作主要依赖传统考古学和执法合作。

**标签**: `#AI in cultural heritage`, `#artifact recovery`, `#TraceART`, `#cultural preservation`

---

<a id="item-tech-news-13"></a>
### [DeepSeek 网页与 API 部分中断，已实施修复](https://status.deepseek.com/incidents/7219383236287) ⭐️ 7.0/10

DeepSeek 于 11 月 7 日发生网页与 API 部分中断，影响 V4 Pro API、V4.1 Flash API、对话及搜索服务。官方已实施修复，目前处于监控确认阶段。这是一周内第二次中断，持续约 30 分钟。

telegram · zaihuapd · 11月7日 07:45

**「背景」** DeepSeek 是一家提供大语言模型 API 服务的公司，近期服务稳定性受到关注。一周内两次中断表明基础设施可能存在反复问题。

**「影响」** 依赖 DeepSeek API 的开发者和应用在中断期间无法正常调用服务，需关注后续稳定性报告并考虑备选方案。

**标签**: `#DeepSeek`, `#API`, `#Incident`, `#Artificial Intelligence`, `#Software Engineering`

---

<a id="item-tech-news-14"></a>
### [Claude Code 疑似泄露用户邮箱](https://github.com/anthropics/claude-code/issues/107757) ⭐️ 7.0/10

Anthropic 的 Claude Code 被指在联网搜索时可能把用户登录邮箱放入网络请求并发送。开发者投诉后，Anthropic 工程师称，此前为解决 Claude 乱填作者名而把登录邮箱放进模型上下文。问题据称在今年 7 月被报告，2.1.317 版已加拦截，但可被 Python 脚本绕过，公司计划在下一版本移除上下文中的登录邮箱。

telegram · zaihuapd · 11月7日 08:09

**「背景」** 该问题背景可能涉及 Claude Code 在生成内容时引用作者信息，团队因而把登录邮箱放入模型上下文。

**「影响」** 若泄露发生，可能导致用户收到诈骗邮件或面临其他隐私风险。受影响用户可能需要等待修复或升级版本；2.1.317 版拦截可被 Python 脚本绕过，下一版本移除上下文邮箱仍处于计划阶段。

**标签**: `#Claude Code`, `#AI privacy`, `#LLM security`, `#AI agents`, `#data leakage`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [软银与 ABB 拟分拆中国业务冲救 54 亿美元机器人交易](https://www.bloomberg.com/news/articles/2026-11-07/softbank-abb-weigh-china-carve-out-to-salvage-robotics-deal) ⭐️ 8.0/10

软银与 ABB 正考虑将 ABB 中国机器人业务剥离为独立实体，以挽救因中国监管机制拦截的 54 亿美元跨境收购。知情人士称该方案可能失败，ABB 正评估其他选项，包括另寻买家，而 ABB 与软银均拒予置评。

telegram · zaihuapd · 11月7日 11:24

**「背景」** 中国外商投资安全审查工作机制办公室（外商投资安全审查机制）本周四拦截了软银与 ABB 价值 54 亿美元的机器人跨境收购，促使双方考虑分拆中国业务方案。

**标签**: `#M&amp;A`, `#Regulatory Risk`, `#Robotics`, `#SoftBank`, `#ABB`

---

<a id="item-finance-news-2"></a>
### [伯克希尔·哈撒韦第三季度回购加速，盈利下滑](https://www.cnbc.com/2026/11/07/berkshire-hathaway-q3-2026-earnings-buybacks.html) ⭐️ 7.0/10

伯克希尔·哈撒韦在 2026 年第三季度加速回购股票，当季买回 9.6 亿美元，超过前一个季度的 4.5 亿美元；但公司整体盈利同比下降 28%，降至 22.112 亿美元。

rss · CNBC Finance · 11月7日 15:23

**「背景」** 该回购发生时，伯克希尔的整体盈利仍在同比下滑，保险业务表现是主要拖累。

**标签**: `#buybacks`, `#earnings`, `#Berkshire Hathaway`

---

<a id="item-finance-news-3"></a>
### [全国 3.35 万座寺院启动财务大检查](https://www.163.com/dy/article/LB2VSRQD0556HNS1.html) ⭐️ 7.0/10

A nationwide financial audit of 33,500 temples and 9,000 Taoist monasteries in China has launched, imposing strict financial transparency measures and anti-commercialization rules on the religious sector.

telegram · zaihuapd · 11月7日 15:02

**标签**: `#religious regulation`, `#financial audit`, `#China policy`, `#religious commercialization`, `#sector oversight`

---