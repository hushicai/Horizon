---
layout: default
title: "Horizon Summary: 2026-11-09 (ZH)"
date: 2026-11-09
lang: zh
---

> 从 31 条内容中筛选出 12 条重要资讯。

---

**科技新闻**
1. [Drex Max v1.1 多模态决策模型 SOTA 与帕累托前沿](#item-tech-news-1) ⭐️ 9.0/10
2. [Goldman Sachs is pulling Claude Code from its bankers and traders](#item-tech-news-2) ⭐️ 8.0/10
3. [Goodbye Claude, hello Pi](#item-tech-news-3) ⭐️ 8.0/10
4. [BLG 3:1 击败 T1 终结 LPL 13 年魔咒](#item-tech-news-4) ⭐️ 8.0/10
5. [Windows 11 测试统一应用更新页](#item-tech-news-5) ⭐️ 7.5/10
6. [KetchUp：基于 Rust 和 WebGPU 的开源 SketchUp 替代品](#item-tech-news-6) ⭐️ 7.0/10
7. [Outlook.com 开始拒绝无 DMARC 域名的邮件](#item-tech-news-7) ⭐️ 7.0/10
8. [parse\_number\(\) as a SQLite extension: C vs Rust](#item-tech-news-8) ⭐️ 7.0/10
9. [Reddit 用户提出用扩散模型生成神经网络权重的概念验证](#item-tech-news-9) ⭐️ 7.0/10
10. [索尼进博会首发无线感知跌倒检测系统](#item-tech-news-10) ⭐️ 7.0/10
11. [姚顺雨：AI 公司护城河在产品层而非模型层](#item-tech-news-11) ⭐️ 7.0/10
12. [Anthropic 报告：科学家主要用 Claude 做数据分析和写作](#item-tech-news-12) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Drex Max v1.1 多模态决策模型 SOTA 与帕累托前沿](https://www.reddit.com/r/MachineLearning/comments/1xr4hkm/artificial_analysis_multimodal_decision_model/) ⭐️ 9.0/10

2026 年 11 月 8 日，Nace 的 Alti 团队发布了 Drex Max v1.1 的更新。该多模态决策模型在 SOTA 和帕累托前沿上达成领先，提供开源权重并支持本地推理。模型拥有约 256k 文本上下文窗口（远超 Glide1.2 的 64k 与 Mammoth 的 16k），可在 macOS 上通过 Kapitsa 推理引擎运行，并采用 Open RAIL-M 许可。

reddit · r/MachineLearning · /u/m4rkGS · 11月8日 17:54

**「背景」** Drex Max 前身是 v1 版本，其权重已在 Hugging Face 上公开；v1.1 通过迭代改进实现了更大的上下文窗口和本地推理能力。Kapitsa 推理引擎允许在 macOS 上直接加载模型进行推理。论文《Towards Foundation Decision Models: Drex》（arXiv:2611.07854）详细介绍了训练流程，新版权重即将上线。

**「影响」** 开发者可直接获取 v1.1 开源权重并在本地机器上部署，降低成本约为下一代模型的 8 倍，同时提升上下文处理能力。企业可避免依赖云端服务，提升实时决策质量。需注意 Open RAIL-M 许可证对商业用途的潜在限制。

**标签**: `#multimodal decision models`, `#foundation models`, `#open source AI`, `#decision models`, `#AI systems`

---

<a id="item-tech-news-2"></a>
### [Goldman Sachs is pulling Claude Code from its bankers and traders](https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers) ⭐️ 8.0/10

Goldman Sachs removes Claude Code from bankers and traders due to security and compliance risks associated with AI agents on sensitive financial workstations.

hackernews · TheWiggles · 11月8日 18:16 · [社区讨论](https://news.ycombinator.com/item?id=50415628)

**标签**: `#finance`, `#AI`, `#security`, `#compliance`, `#LLM`, `#deployment`

---

<a id="item-tech-news-3"></a>
### [Goodbye Claude, hello Pi](https://caleb.software/posts/claude-to-pi.html) ⭐️ 8.0/10

开发者们正在从 Anthropic 的闭源模型 Claude 转向开源的 Pi 模型。Pi 是一个提供终端用户界面 \(TUI\) 和 SDK 的开源大语言模型 harness，支持 GLM 等开源权重模型，并可用于 Forgejo 等平台。迁移的主要动因为避免订阅费用、 API 限制和潜在的服务条款违规，同时利用 Pi 的灵活性和本地工作流支持。社区报告称 Pi 的 harness 在效率和定制方面表现更佳。

hackernews · karagenit · 11月8日 03:11 · [社区讨论](https://news.ycombinator.com/item?id=50410107)

**「Background」** Pi 是一个开源的大语言模型 harness，集终端用户界面 \(TUI\) 和 SDK 于一体，支持开源权重模型（如 GLM），并可用于构建 AI 代理和自动化工作流。Claude 是 Anthropic 提供的闭源聊天模型，通常需要订阅且 API 行为受限。开发者转向 Pi 主要是为了获得开源、灵活的解决方案，避免因使用第三方 harness 与闭源模型相关的服务条款风险和隐藏 API 细节。

**「Impact」** 开发者现在可以利用 Pi 的 TUI 和 SDK 在本地运行开源权重模型，摆脱对 Claude 等闭源服务的订阅依赖，并通过 GitHub Actions 等工具将 Pi 集成到 CI/CD 流程中，从而降低成本并避免潜在的服务条款违规。

**「Community discussion」** 一些用户警告说，将 Pi 与闭源模型结合使用可能导致服务条款违规和 API 兼容性问题，因为第三方 harness 需要处理 Anthropic 的自定义头部和隐藏标志；另一些用户则对 Pi 的灵活性表示赞赏，指出其开源特性使他们能够构建自定义工作流（如 GitHub Action）并在 Forgejo 等平台上使用开源权重模型。

**标签**: `#Open Source LLMs`, `#Developer Tools`, `#AI Model Migration`, `#TUI`, `#Pi Harness`

---

<a id="item-tech-news-4"></a>
### [BLG 3:1 击败 T1 终结 LPL 13 年魔咒](https://m.weibo.cn/detail/5363275916380980) ⭐️ 8.0/10

BLG 在 LPL S16 半决赛中以 3:1 战胜 T1，挺进决赛。此胜终结了 T1 在世界赛 BO5 对阵 LPL 队伍的 13 年连胜纪录。该结果让 BLG 成为本赛季 LPL 赛区的关键竞争者，对 T1 长期统治格局产生重大影响。

telegram · zaihuapd · 11月9日 01:45

**「T1 13 年连胜纪录背景」** T1 曾在 LPL 世界赛 BO5 对阵 LPL 队伍的比赛中连续 13 次获胜，保持了 13 年不败的纪录。2026 年 11 月 9 日，这一纪录被 BLG 打破，标志着 LPL 赛区的竞争格局发生重大转变。

**「决赛晋级影响」** 这一胜利让 BLG 挺进决赛，成为 LPL S16 决赛的主要对手，对 LPL 赛区的竞争格局产生深远影响。

**标签**: `#esports`, `#league-of-legends`, `#lpl`, `#s16`

---

<a id="item-tech-news-5"></a>
### [Windows 11 测试统一应用更新页](https://www.windowslatest.com/2026/11/09/for-20-years-windows-apps-like-java-have-nagged-you-with-their-own-update-pop-ups-and-windows-11-now-wants-to-end-it/) ⭐️ 7.5/10

Windows 11 正在测试一个位于“设置 &gt; 应用”中的统一应用更新页面，目标是集中管理第三方应用更新，并取代 Java 等应用各自弹出的更新提示。开发者需要注册为提供方并提供更新检查脚本，Windows 还将沿用系统更新的智能调度，结合使用状态、电量和网络条件安排安装，默认每 22 小时扫描一次。该功能仍在测试最后阶段，暂时无法使用。

telegram · zaihuapd · 11月9日 02:09

**「背景概念」** 此前，类似 Java 的应用可能自行决定更新并通过弹窗提醒用户，造成分散且重复的更新提示。Windows 系统更新智能调度则提供过基于状态、电量和网络安排安装的机制，本次测试准备借用这套思路。

**「潜在影响」** 如果该测试版本最终发布，用户可能因此减少第三方应用更新弹窗，而开发者则需要按 Windows 新流程完成注册和更新检查脚本接入。不过，由于功能仍在测试阶段，是否会改变现有更新行为以及兼容哪些应用，仍有待观察。

**标签**: `#Windows 11`, `#unified app update`, `#software updates`, `#system update`, `#Windows`

---

<a id="item-tech-news-6"></a>
### [KetchUp：基于 Rust 和 WebGPU 的开源 SketchUp 替代品](https://ketchup3d.github.io/app/) ⭐️ 7.0/10

KetchUp 是一款基于 Rust 和 WebGPU 构建的开源 3D 建模工具，定位为 SketchUp 的免费替代品，可通过 ketchup3d.github.io/app 在浏览器中使用。项目以 Rust 编写前端并使用 WebGPU 进行图形渲染，主打跨平台网页应用。供稿未披露具体版本号、支持的浏览器或操作系统，也未说明功能是否已稳定发布。

hackernews · dcoulmbe · 11月8日 22:35 · [社区讨论](https://news.ycombinator.com/item?id=50418176)

**「KetchUp 是基于 Rust 与 WebGPU 的开源 3D 建模工具」** KetchUp 是一个免费的开源 3D 建模工具，使用 Rust 和 WebGPU 实现。它可以在浏览器或桌面程序（Windows、macOS、Linux）中运行。

**「影响」** 早期评论者表示，该工具可能吸引习惯 SketchUp 8 并需要为 3D 打印设计简单外壳的爱好者；同时，有评论者反馈绘制矩形时会弹出命名对话框，这可能干扰建模流程。

**「社区讨论」** 评论者 nico 认为 AI 代理让“按需构建自己的工具”比学习现有软件更高效，而 elxr 则称赞 Rust 网页界面的文字渲染效果并建议增加功能演示。yboris 的交互反馈和 4ff618 的使用经历则分别指向具体的可用性问题与目标用户群体。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Ketchup3D/app">GitHub - Ketchup3D/app: Free, open-source 3D modeling ...</a></li>
<li><a href="https://ketchup3d.github.io/app/">KetchUp — Free 3D Woodworking &amp; Furniture Design App</a></li>

</ul>
</details>

**标签**: `#open-source`, `#rust`, `#webgpu`, `#3d-modeling`, `#cross-platform`

---

<a id="item-tech-news-7"></a>
### [Outlook.com 开始拒绝无 DMARC 域名的邮件](https://mailroute.net/blog/outlook-rejecting-email-without-dmarc) ⭐️ 7.0/10

Outlook.com 已开始拒绝来自未配置 DMARC 记录域名的邮件，这一策略变更直接影响未部署邮件认证的发件人。据 Mailroute 博客报道，微软正在悄默无声地实施基于 DMARC 的拒收，但有管理员反馈实际返回 5xx 永久投递失败而非静默丢弃。该变更凸显了 DMARC、SPF 和 DKIM 等认证机制在邮件投递中的关键地位。

hackernews · xmddmx · 11月8日 19:20 · [社区讨论](https://news.ycombinator.com/item?id=50416158)

**「Outlook.com 静默拒收无 DMARC 域邮件」** 自 2026 年 11 月 5 日起，Outlook.com 和 Hotmail 开始静默拒收（550 5.7.1）来自没有 DMARC 记录的域的邮件，影响所有使用该域的发送者，包括小型 VPS 运营者。此变更源于 Microsoft 2026 年冷邮件政策，要求对低发送评分的公司设置 p=reject 的 DMARC 策略，从隔离转为直接拒收。添加 DMARC TXT 记录并设置 p=reject 即可解决问题。

**「影响」** 依赖自建邮件服务器或未配置 DMARC 的域名发件人将面临投递失败，需尽快为发送域名发布 DMARC 记录并确保 SPF/DKIM 对齐，否则邮件将被 Outlook.com 直接拒收。

**「社区讨论」** 社区讨论集中在两点：一是微软长期以来通过不公开的黑名单拒收邮件，且难以申诉；二是关于“静默拒收”的定义存在分歧，有管理员指出实际返回 5xx 错误而非静默丢弃，也有运维者表示即使配置完整的 SPF/DKIM/DMARC 仍遭误拦。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tosend.com/articles/outlook-rejects-email-without-dmarc/">Outlook.com now rejects email from domains without DMARC</a></li>
<li><a href="https://blog.101domain.com/dmarc/microsoft-cold-email-policy-2026">Microsoft’s new cold email policy for 2026 - The 101domain Blog</a></li>

</ul>
</details>

**标签**: `#email security`, `#DMARC`, `#Outlook`, `#mail delivery`, `#authentication`

---

<a id="item-tech-news-8"></a>
### [parse\_number\(\) as a SQLite extension: C vs Rust](https://simonwillison.net/2026/Nov/8/sqlite-parse-number-c-vs-rust/) ⭐️ 7.0/10

Simon Willison explores building a SQLite parse\_number\(\) extension in C versus Rust, comparing performance, complexity, and resulting binary size.

rss · Simon Willison · 11月8日 22:26

**标签**: `#sqlite`, `#rust`, `#c`, `#extensions`, `#software-engineering`

---

<a id="item-tech-news-9"></a>
### [Reddit 用户提出用扩散模型生成神经网络权重的概念验证](https://www.reddit.com/r/MachineLearning/comments/1xqsl8d/what_if_diffusion_models_generates_neural_network/) ⭐️ 7.0/10

Reddit 用户 /u/Specific-Tax-6700 提出用扩散模型从文本提示生成神经网络权重而非图像，并在 GitHub 发布了名为 nngen 的小型概念验证实现。该项目目前仅在笔记本 CPU 上完成了 4000 步训练中的 3000 步，初步截图显示能生成简单绘图任务的网络权重。作者表示未发现类似论文，寻求社区帮助查找相关研究及贡献代码。

reddit · r/MachineLearning · /u/Specific-Tax-6700 · 11月8日 07:20

**「扩散模型生成神经网络权重的前沿研究与小规模实现」** 扩散模型已广泛应用于从文本描述生成图像，其核心原理是通过在潜空间中学习去噪过程来生成数据。近期学术界已有 D2NWG（Diffusion-based Neural Network Weights Generation）等研究提出，利用文本条件的扩散模型直接生成任务特定的网络权重，以解决模型存储和个性化部署的挑战。该 Reddit 帖子提出将这一思路扩展到实际的小规模 PoC 实现，作者使用 z.ai zcode 和 GLM 模型在 GitHub 上发布了名为 nngen 的实现，展示了从文本提示生成神经网络权重的初步可行性。

**「影响」** 对开发者和研究者而言，该帖子展示的只是一个未完成的概念验证：作者称训练只进行了一半（3000/4000 步），且在笔记本 CPU 上运行，未提供独立验证或同行评审结果，因此目前不能将其视为可直接使用的能力。相关研究已指出，用扩散模型生成神经网络权重时，标准参数表示依赖已知的权重矩阵尺寸，往往与特定网络架构绑定，想要跟进该方向的人需要先解决架构兼容性和权重空间表示的技术限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2402.18153">[2402.18153] Diffusion-Based Neural Network Weights Generation Diffusion-based Neural Network Weights Generation - arXiv.org Tina: A diffusion neural network for generating personalized ... Diffusion-based Neural Network Weights Generation Published as a conference paper at ICLR 2025 - OpenReview GitHub - TianSuya/T2W: Official Implementation of the T2W ... ICLR Poster Diffusion-based Neural Network Weights Generation</a></li>
<li><a href="https://arxiv.org/html/2402.18153v1">Diffusion-based Neural Network Weights Generation - arXiv.org Tina: A diffusion neural network for generating personalized ... Diffusion-based Neural Network Weights Generation Published as a conference paper at ICLR 2025 - OpenReview GitHub - TianSuya/T2W: Official Implementation of the T2W ... ICLR Poster Diffusion-based Neural Network Weights Generation</a></li>
<li><a href="https://www.sciencedirect.com/science/article/pii/S2666389926000802">Tina: A diffusion neural network for generating personalized ...</a></li>
<li><a href="https://github.com/NNgen/nngen">GitHub - NNgen / nngen : NNgen : A Fully-Customizable Hardware...</a></li>
<li><a href="https://arxiv.org/html/2603.00180v1">NNiT: Width-Agnostic Neural Network Generation with Structurally...</a></li>
<li><a href="https://pure.kaist.ac.kr/en/publications/diffusion-based-neural-network-weights-generation/">Diffusion -based neural network weights generation</a></li>
<li><a href="https://arxiv.org/html/2603.00180v1">NNiT: Width-Agnostic Neural Network Generation with Structurally...</a></li>

</ul>
</details>

**标签**: `#diffusion models`, `#neural network generation`, `#generative AI`, `#machine learning`

---

<a id="item-tech-news-10"></a>
### [索尼进博会首发无线感知跌倒检测系统](https://weibo.com/1642634100/RqojudB4Q) ⭐️ 7.0/10

Sony unveiled a privacy‑preserving wireless fall detection system using Wi‑Fi signals and deep learning at the Shanghai import expo.

telegram · zaihuapd · 11月8日 02:21

**标签**: `#AI`, `#Wireless Sensing`, `#Healthcare`, `#Deep Learning`

---

<a id="item-tech-news-11"></a>
### [姚顺雨：AI 公司护城河在产品层而非模型层](https://www.ithome.com/1/023/991.htm) ⭐️ 7.0/10

在 2026 年 11 月 8 日的未来科学大奖对话中，腾讯首席 AI 科学家姚顺雨提出，AI 公司的护城河更多存在于产品层而非模型层，认为真正难以替代的是理解用户背景、掌握专有数据并获得用户信任的产品能力。他以微信为例指出，AI 若内嵌微信，能了解用户日程与社交关系，即使对手拥有更聪明的模型也难以提供同等服务。张亚勤则调侃称，按此逻辑 Anthropic 未来或许不值两万亿美元。该论点将行业竞争焦点从模型性能转向产品生态与用户数据壁垒的构建。

telegram · zaihuapd · 11月8日 14:17

**「背景」** “护城河”是指企业难以被竞争对手复制的持久竞争优势。在 AI 领域，模型层通常指基础模型本身及其性能，产品层则指面向用户的应用、用户上下文、专有数据和信任等环节。姚顺雨是腾讯首席 AI 科学家，此番表述是在 2026 未来科学大奖的对话中，回应张亚勤提问时提出的。

**标签**: `#AI strategy`, `#competitive advantage`, `#product layer`, `#Tencent`, `#AI industry`

---

<a id="item-tech-news-12"></a>
### [Anthropic 报告：科学家主要用 Claude 做数据分析和写作](https://www.anthropic.com/research/how-researchers-use-claude) ⭐️ 7.0/10

Anthropic&\#x27;s research report reveals that scientists primarily use Claude for data analysis and writing, projecting significant productivity boosts, especially in computer science and mathematics.

telegram · zaihuapd · 11月9日 01:29

**标签**: `#artificial-intelligence`, `#large-language-models`, `#software-engineering`, `#research-productivity`, `#anthropic`

---