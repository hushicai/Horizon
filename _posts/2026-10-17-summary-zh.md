---
layout: default
title: "Horizon Summary: 2026-10-17 (ZH)"
date: 2026-10-17
lang: zh
---

> 从 41 条内容中筛选出 15 条重要资讯。

---

**科技新闻**
1. [Claude reveals ECDSA curve origins](#item-tech-news-1) ⭐️ 9.0/10
2. [Apple ML Research: Muse Spark Open with MLX on Mac Studio](#item-tech-news-2) ⭐️ 8.0/10
3. [90% of US working hours are spent on tasks not covered well by AI benchmarks](#item-tech-news-3) ⭐️ 8.0/10
4. [\[Research\] 2,788 tokens/s on a single RTX 5090 with a diffusion LLM — Introducing ORL \(fully open source\) \[R\]](#item-tech-news-4) ⭐️ 8.0/10
5. [\[P\] my rust framework trains nanoGPT with the exact same bits as pytorch. worth continuing? \[P\]](#item-tech-news-5) ⭐️ 7.5/10
6. [Llama.cpp 移植到破解 PS5，运行任意 GGUF 模型](#item-tech-news-6) ⭐️ 7.0/10
7. [JPEG XL 与 AVIF 的网络应用权衡](#item-tech-news-7) ⭐️ 7.0/10
8. [Anthropic Claude Code 团队使用 AI 自动化代码审查](#item-tech-news-8) ⭐️ 7.0/10
9. [Home Assistant Supervisor 未经同意扫描密码进行泄露检测](#item-tech-news-9) ⭐️ 7.0/10
10. [Big Fish: Exploiting a 37-Year-Old Kernel Bug in OpenBSD](#item-tech-news-10) ⭐️ 7.0/10
11. [AI 数据中心投资因市场回调与利率上升被撤回或暂停](#item-tech-news-11) ⭐️ 7.0/10
12. [阶跃星辰发布 Step 5 Preview 智能体旗舰模型](#item-tech-news-12) ⭐️ 7.0/10
13. [Telegram 向美政府提供 2253 名用户数据细节曝光](#item-tech-news-13) ⭐️ 7.0/10
14. [英伟达否认 RTX 5090 停产，RTX 5080 接任消费级旗舰](#item-tech-news-14) ⭐️ 7.0/10

**财经新闻**
1. [U.S. presses China on Mastercard, Citigroup market access in bilateral Bangkok talks, official says](#item-finance-news-1) ⭐️ 8.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Claude reveals ECDSA curve origins](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Claude uncovered that NIST&\#x27;s P‑192, P‑224, P‑256, P‑384, and P‑521 curve seeds originated from a timestamp‑seeded lrand48 RNG rather than a secure hash.

hackernews · ahlCVA · 10月16日 18:55 · [社区讨论](https://news.ycombinator.com/item?id=50122800)

**标签**: `#Cryptography`, `#Security`, `#Random Number Generation`, `#Standards`, `#ECDSA`

---

<a id="item-tech-news-2"></a>
### [Apple ML Research: Muse Spark Open with MLX on Mac Studio](https://machinelearning.apple.com/research/mlx-distributed-inference) ⭐️ 8.0/10

Apple’s MLX release enables running a near‑trillion‑parameter Muse Spark Open model on Mac Studio clusters, achieving high token throughput and demonstrating practical large‑model inference on consumer hardware.

hackernews · antipaul · 10月16日 13:43 · [社区讨论](https://news.ycombinator.com/item?id=50118320)

**标签**: `#MLX`, `#Mac Studio`, `#Large Language Models`, `#Distributed Inference`, `#AI Research`

---

<a id="item-tech-news-3"></a>
### [90% of US working hours are spent on tasks not covered well by AI benchmarks](https://www.mercor.com/research/labor-index/benchmark-map/) ⭐️ 8.0/10

A research study reveals that 90% of US working hours involve tasks poorly covered by current AI benchmarks, challenging assumptions about AI&\#x27;s ability to handle real-world professional work.

hackernews · speckx · 10月16日 17:08 · [社区讨论](https://news.ycombinator.com/item?id=50121179)

**标签**: `#AI benchmarks`, `#labor economics`, `#artificial intelligence`, `#software engineering`

---

<a id="item-tech-news-4"></a>
### [\[Research\] 2,788 tokens/s on a single RTX 5090 with a diffusion LLM — Introducing ORL \(fully open source\) \[R\]](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 8.0/10

Researchers introduce ORL, an open-source technique boosting diffusion LLM inference to 2,788 tokens/s on a single RTX 5090 with comparable or better quality.

reddit · r/MachineLearning · /u/arty\_photography · 10月16日 20:03

**标签**: `#diffusion language models`, `#ORL`, `#inference acceleration`, `#RTX 5090`, `#open source`

---

<a id="item-tech-news-5"></a>
### [\[P\] my rust framework trains nanoGPT with the exact same bits as pytorch. worth continuing? \[P\]](https://www.reddit.com/r/MachineLearning/comments/1x7ojxo/p_my_rust_framework_trains_nanogpt_with_the_exact/) ⭐️ 7.5/10

A new Rust framework \(DenseCore\) demonstrates bit-for-bit parity with PyTorch&\#x27;s nanoGPT, enabling equivalent model training across different backends including dropout and custom CUDA operations, bridging Rust and the dominant ML ecosystem.

reddit · r/MachineLearning · /u/Mental-Feature-2377 · 10月16日 18:49

**标签**: `#rust`, `#machine-learning`, `#deep-learning-framework`, `#AI`, `#open-source`

---

<a id="item-tech-news-6"></a>
### [Llama.cpp 移植到破解 PS5，运行任意 GGUF 模型](https://github.com/cobanov/PS5LM) ⭐️ 7.0/10

PS5LM 项目将 Llama.cpp 移植到已破解的 PlayStation 5，使任意 GGUF 格式的语言模型都能在游戏机上原生运行。它需要一台已破解的 PS5，提供极低的运行成本（约 0.70 美元/天），能够使用量化到 2 位的 Qwen 3.8 27B 等模型生成约 200 万 tokens/天，适合持续的本地 AI 任务。该项目为开源代码，托管在 GitHub 上。

hackernews · Anon84 · 10月16日 18:32 · [社区讨论](https://news.ycombinator.com/item?id=50122431)

**「背景」** Llama.cpp 是一个用于执行 GGUF 格式语言模型的开源 C++ 库，而 PlayStation 5 配备了定制的 AMD APU。破解游戏机可以移除软件限制，从而允许加载和运行任意代码，包括 Llama.cpp。结合这两点后，PS5 成为了一个用于本地边缘 AI 推理的平台。

**「影响」** 拥有已破解 PS5 的用户现在可以以每天约 0.70 美元的电费成本进行本地 AI 推断，每天可生成约 200 万 tokens，足以支持服务器错误监控、安全监控回放或植物生长追踪等应用，而无需支付云服务费用。但该功能仍需依赖于已破解的系统，且高分辨率模型受内存限制。

**「社区讨论」** Rabbit504030201 认为该项目不应托管在 GitHub 上，因为索尼可能随时删除页面，建议使用自定义域名；shiftpgdn 则指出该技术可能也适用于 BC250 挖矿主板，因为它们使用了与 PS5 相似的“Cyan Skillfish” APU 裁剪版。这反映出关于托管方式和硬件扩展性的讨论。

**标签**: `#Hardware hacking`, `#Edge AI`, `#LLM inference`, `#Console computing`, `#Open source tools`

---

<a id="item-tech-news-7"></a>
### [JPEG XL 与 AVIF 的网络应用权衡](https://jakearchibald.com/2026/jpeg-xl-vs-avif/) ⭐️ 7.0/10

这篇文章对 JPEG XL 和 AVIF 这两种新兴网络图像格式进行了技术比较，指出了在压缩效率和编码速度之间的权衡。作者发现 JPEG XL 仅在极高的编码努力下能实现 modest 的大小减少（照片缩小 2–7 %，截图/插图缩小约 25 %），但需要 9–46 秒，远慢于默认设置；而 AVIF 则能以较快的编码速度实现 10 倍以上的文件缩小，同时保持较好的质量并支持透明度。文章提醒开发者，两者均在不断成熟中，需根据具体需求选择合适的格式。

hackernews · farlight · 10月16日 16:12 · [社区讨论](https://news.ycombinator.com/item?id=50120224)

**「背景」** 网络图像需在质量与加载速度间取得平衡，传统 JPEG/WebP 已被 newer 格式 AVIF（基于 AV1 视频编码）和 JPEG XL（基于改进的 JPEG 架构）取代。AVIF 提供高效压缩和硬件加速解码，而 JPEG XL 则支持无损和可可视化传输。了解这些技术的差异有助于开发者优化网页性能。

**「影响」** 因此，开发者通常会选择 AVIF 进行生产环境图像优化，以获得显著的体积节省和合理的编码时间，而避免 JPEG XL 的高努力设置，因为其极慢的编码速度可能影响工作流程。文章还建议在需要透明度时使用特定的 AVIF 参数，确保质量与文件大小的最佳平衡。

**「社区讨论」** 社区意见两极分化：部分开发者赞扬 AVIF 的压缩效果和透明度支持，并分享了使用 ffmpeg 实现最佳设置的实践方法；另一些人则指出 AVIF 在处理高亮细节时存在明显失真，并警告这两项新编码器尚未完全成熟，引用 WebP 早期被夸大的表现作为警示。

**标签**: `#image compression`, `#web performance`, `#JPEG XL`, `#AVIF`, `#web development`

---

<a id="item-tech-news-8"></a>
### [Anthropic Claude Code 团队使用 AI 自动化代码审查](https://claude.dev/blog/solving-code-review-at-anthropic/) ⭐️ 7.0/10

Anthropic’s Claude Code team launched an AI‑driven code review workflow that automatically runs routine checks on pull requests. Human reviewers are limited to a single person in the loop, who may be the author, and are only needed for high‑risk changes, while the system is claimed to be SOC2 compliant.

hackernews · pretext · 10月16日 19:04 · [社区讨论](https://news.ycombinator.com/item?id=50122951)

**「背景」** The team needed a scalable way to review the large volume of pull requests in Anthropic’s development pipeline. By automating most checks with AI and limiting human oversight to high‑risk changes, they aimed to meet SOC2 compliance and reduce manual effort.

**「影响」** Developers can merge most pull requests without waiting for a human reviewer, speeding delivery while maintaining SOC2 compliance, but they must still perform manual review for high‑risk changes.

**「社区讨论」** Commenters worry that AI‑driven reviews may threaten job security and code quality, while others note the team’s claim of SOC2 compliance and limited human involvement, raising questions about audit readiness.

**标签**: `#code review`, `#AI-assisted development`, `#internal tooling`, `#compliance`, `#Anthropic`

---

<a id="item-tech-news-9"></a>
### [Home Assistant Supervisor 未经同意扫描密码进行泄露检测](https://github.com/home-assistant/home-assistant.io/issues/49314) ⭐️ 7.0/10

Home Assistant 的 Supervisor 组件在未经用户明确同意的情况下，将用户密码的前 5 个字符（哈希处理后）发送至 Have I Been Pwned（HIBP）数据库进行泄露检测。该功能已存在多年，检查被标记为密码的应用选项。近期版本修复了暴露此行为的警告提示，导致用户最近才注意到这一问题。开发者 Frenck 在 GitHub 问题中道歉，并指出用户可通过 \`ha security options --pwned=false\` 命令关闭此检查。该行为引发了隐私争议，社区批评其默认开启且未提供 opt-in 机制。

hackernews · trvrprkr · 10月16日 20:33 · [社区讨论](https://news.ycombinator.com/item?id=50124251)

**「背景」** Have I Been Pwned 的 k-anonymity 密码检测是一种安全实践，通过仅发送密码哈希的前 5 个字符来查询已知泄露密码数据库，以在不暴露完整密码的前提下检测密码安全性。Home Assistant 将此功能集成到 Supervisor 中，但实现方式为默认开启且未征得用户同意，这与隐私保护的基本原则相悖。近期版本修复了显示该检查的警告信息，使这一长期存在的行为被用户发现。

**「影响」** Home Assistant 用户若重视隐私，需手动执行 \`ha security options --pwned=false\` 关闭此检查。默认行为意味着任何配置了密码选项的用户，其密码哈希片段都会在未经明确同意的情况下被发送至第三方服务，这可能违反部分地区的隐私法规。对于已信任 HIBP 服务的用户，该功能仍可提供密码安全检测，但默认开启的方式引发了信任问题。

**「社区讨论」** 社区成员对这一行为表达了强烈批评。eranation 认为任何产品都不应在未经 opt-in 的情况下发送用户数据，即使已做哈希处理。jollymonATX 强调应默认以隐私为先。janice1999 将此归咎于开发者个人，并链接至 NixOS 和 Hacker News 的相关讨论。开发者 Frenck 虽然道歉并提供了关闭方法，但其最初在问题中的回复被批评为过于 dismissive。jackpepsi 则从哲学角度讨论了数学安全性证明与用户主观感受之间的张力。整体上，社区共识倾向于认为此类检查应默认关闭并需用户明确同意。

**标签**: `#privacy`, `#security`, `#home-automation`, `#password-management`, `#open-source`

---

<a id="item-tech-news-10"></a>
### [Big Fish: Exploiting a 37-Year-Old Kernel Bug in OpenBSD](https://calif.io/research/big-fish) ⭐️ 7.0/10

Discovery of a 37‑year‑old OpenBSD kernel bug, with analysis of its persistence and detection techniques.

hackernews · rs\_rs\_rs\_rs\_rs · 10月16日 14:44 · [社区讨论](https://news.ycombinator.com/item?id=50118977)

**标签**: `#OpenBSD`, `#kernel security`, `#vulnerability research`, `#static analysis`, `#bug discovery`

---

<a id="item-tech-news-11"></a>
### [AI 数据中心投资因市场回调与利率上升被撤回或暂停](https://www.kitco.com/news/off-the-wire/2026-10-15/market-selloff-rising-rates-test-ai-data-centre-deal-boom) ⭐️ 7.0/10

AI 数据中心投资因市场回调与利率上升被撤回或暂停。AirTrunk 的 REIT 上市计划以及英伟达支持的 Firmus 和软银支持的 SB Energy 的 IPO 安排均被撤回或暂停，投资者要求企业证明能消化升高的利率与算力成本。Dealogic 数据显示，今年亚洲数据中心并购交易已达 213 亿美元，约为 2025 年全年 100 亿美元的两倍，而股权融资同比下降 4.6%。

telegram · zaihuapd · 10月16日 05:10

**「背景」** 过去几年 AI 数据中心融资呈现快速增长，受惠于对人工智能算力需求的乐观预期。利率上升使此类高资本密集项目面临更大融资成本，导致投资者更加审慎。

**「影响」** 开发者可能因资金撤离而面临 AI 基础设施部署延迟和融资成本上升，需重新调整项目时间表和预算。

**标签**: `#AI`, `#data centers`, `#investment`, `#market trends`, `#hardware`

---

<a id="item-tech-news-12"></a>
### [阶跃星辰发布 Step 5 Preview 智能体旗舰模型](https://huggingface.co/stepfun-ai/Step-5-Preview) ⭐️ 7.0/10

阶跃星辰在 Hugging Face 发布了面向智能体工作的旗舰模型 Step 5 Preview。该模型采用稀疏 MoE 架构，总参数 6000 亿、激活参数 270 亿，支持最高 100 万 token 上下文，并可接收文本、图像和视频输入。厂商称其在软件工程、长周期智能体执行和金融等专业知识任务上表现领先，但发布未提供详细基准、方法论或独立验证。模型可通过 OpenAI 兼容 API 配合 vLLM 或 SGLang 部署，并采用 StepFun Model License 1.0 许可。

telegram · zaihuapd · 10月16日 06:36

**「StepFun Step 5 Preview 旗舰模型发布背景」** 阶跃星辰（StepFun）发布了 Step 5 Preview 智能体旗舰模型，该模型采用稀疏 MoE 架构，总参数量 6000 亿、激活参数量 2700 亿，支持最高 100 万 token 上下文，可接收文本、图像和视频输入。该模型专为智能体工作流设计，在软件工程和金融领域表现突出，并可通过 OpenAI 兼容 API 与 vLLM/SGLang 部署，且采用 StepFun Model License 1.0 许可。

**「影响」** 开发者可使用 OpenAI 兼容客户端接入该模型，并通过 vLLM 或 SGLang 部署，但需自行评估其在软件工程和金融任务上的实际表现，因为厂商未公布详细基准或独立测试结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.eesel.ai/blog/stepfun-step-5">StepFun Step 5 Preview : specs, pricing, benchmarks, and... | eesel AI</a></li>
<li><a href="https://www.deai.org/news/stepfun-step-5-preview-api-open-weights-oct-15">StepFun &#x27;s Step 5 Preview API ships; open weights promised October ...</a></li>
<li><a href="https://openrouter.ai/stepfun/step-5-preview">Step 5 Preview - API Pricing &amp; Providers | OpenRouter</a></li>

</ul>
</details>

**标签**: `#large-language-models`, `#multimodal-models`, `#agent-systems`, `#software-engineering`, `#sparse-mixture-of-experts`

---

<a id="item-tech-news-13"></a>
### [Telegram 向美政府提供 2253 名用户数据细节曝光](https://www.404media.co/heres-what-telegram-giving-data-to-the-u-s-government-looks-like/) ⭐️ 7.0/10

新公开的法院文件显示，Telegram 在回应美国法院命令时，向执法部门提供了用户的手机号、用户 ID 和 IP 地址。Telegram 在随附信函中称此行为系「自愿」提供，同时声称不承认受美国司法管辖。截至 2026 年 1 月，Telegram 已向美方提供 2253 名用户的数据。该案涉及被控参与 2023 年 10 月 7 日袭击以色列事件的 Mahmoud Al-Muhtadi。

telegram · zaihuapd · 10月16日 14:57

**「背景」** 美国法院命令要求科技平台在执法调查中提供用户数据，而 Telegram 的注册地和管辖权主张使其对这类要求的回应方式备受关注。此次公开的文件揭示了 Telegram 在实际操作中如何配合美方的数据请求。

**「影响」** 2253 名用户的手机号、用户 ID 和 IP 地址已暴露给美国执法部门，Telegram 以「自愿」名义在不承认美国司法管辖的情况下配合数据共享，可能削弱用户对其隐私保护承诺的信任，并使平台面临在不同司法管辖区间平衡合规与用户隐私的持续争议。

**标签**: `#Telegram`, `#data privacy`, `#law enforcement`, `#user data`, `#404 Media`

---

<a id="item-tech-news-14"></a>
### [英伟达否认 RTX 5090 停产，RTX 5080 接任消费级旗舰](https://www.techpowerup.com/353578/nvidia-reportedly-ending-the-rtx-5090-reserves-gb202-silicon-for-workstation-gpus) ⭐️ 7.0/10

围绕 RTX 5090 的停产传闻与零售现实出现分歧：供应链消息称英伟达已停止向 GeForce 供应 GB202 晶圆，并将产能转投高毛利的 RTX PRO 工作站产品线，但英伟达个人运算业务资深副总裁 Jeff Fisher 于 2026 年 10 月 16 日公开否认，称 RTX 5090 是核心产品并将持续供货，仅承认产能受限。尽管官方否认停产，美国官方商城已移除产品页面，Micro Center 将其标记为“不再销售”，多家门店售罄，国内 32 GB 版现货价从 9 月初约 3.5 万元涨至 10 月中旬约 5.4 万元。消费级新旗舰由基于 GB203 核心、核心规模不足 RTX 5090 一半的 RTX 5080 24 GB 接棒，其定价仍处旗舰档位，形成型号降格、规格缩水但价格未降的断代格局。

telegram · zaihuapd · 10月17日 00:02

**「背景」** Nvidia 通常将同一代图形核心分为消费级 GeForce 和工作站 RTX PRO 两条产品线，前者面向游戏与创作者，后者主打专业可视化与 AI 工作负载并定价更高。RTX 5090 采用 GB202 核心，而消费级次旗舰 RTX 5080 则基于较小的 GB203 核心。

**「影响」** 依赖 32 GB 显存消费级卡进行 AI/ML 或专业渲染的用户面临显著成本上升：国内 32 GB RTX 5090 现货价已从 9 月初约 3.5 万元涨至 10 月中旬约 5.4 万元，而替代方案 RTX 5080 仅提供 24 GB 显存，可能不满足大模型推理或微调的显存需求。

**标签**: `#GPU market`, `#Nvidia RTX 5090`, `#Hardware supply chain`, `#AI/ML hardware`, `#Consumer pricing`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [U.S. presses China on Mastercard, Citigroup market access in bilateral Bangkok talks, official says](https://www.cnbc.com/2026/10/16/us-china-mastercard-citigroup-market-access.html) ⭐️ 8.0/10

U.S. Treasury officials reported that U.S. companies including Mastercard and Citigroup were discussed for market access in China during bilateral meetings in Bangkok, with regulatory approvals tied to recent U.S.-China presidential interactions.

rss · CNBC Finance · 10月16日 16:46

**标签**: `#financial regulation`, `#market access`, `#cross-border capital flows`, `#China financial sector`

---