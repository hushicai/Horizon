---
layout: default
title: "Horizon Summary: 2026-10-13 (ZH)"
date: 2026-10-13
lang: zh
---

> 从 52 条内容中筛选出 18 条重要资讯。

---

**科技新闻**
1. [MiniCPM-V 4.7-35B-A3B 开源 MoE 模型发布](#item-tech-news-1) ⭐️ 9.0/10
2. [Looped Diffusion Transformer: the same blocks run several times inside each denoising step, and loop depth can be changed at sampling time \[R\]](#item-tech-news-2) ⭐️ 8.5/10
3. [Hello Python 3.15, goodbye 3.10, and now I can use 3.11](#item-tech-news-3) ⭐️ 8.0/10
4. [U-Space: Uncovering When and Why Uncertainty Arises in Language Models \[R\]\[D\]](#item-tech-news-4) ⭐️ 8.0/10
5. [learnc 自动调优 C 代码常量，实现更小的 JPEG 和更高的语音活动检测 F1 分数](#item-tech-news-5) ⭐️ 8.0/10
6. [Qwen released QwenGyre - RL framework for training AI agents on extremely long complex tasks](#item-tech-news-6) ⭐️ 8.0/10
7. [Boole-1.7B 发布 1 位量化 Qwen3-1.7B 模型，内存仅 247 MB](#item-tech-news-7) ⭐️ 8.0/10
8. [Codex CLI 默认安装持久后台守护进程](#item-tech-news-8) ⭐️ 7.5/10
9. [黑客激活欧洲超市冷柜自动除霜功能](#item-tech-news-9) ⭐️ 7.0/10
10. [WiFi 7 路由器改装为 320Msps SDR 接收机](#item-tech-news-10) ⭐️ 7.0/10
11. [Muse Wonder](#item-tech-news-11) ⭐️ 7.0/10
12. [Reddit 提问当前 AI 机制能否催生通用智能](#item-tech-news-12) ⭐️ 7.0/10
13. [Decision 3.0 发布：0.6B-27B 开源多模态决策模型](#item-tech-news-13) ⭐️ 7.0/10
14. [🤖 Anthropic：蒸馏数据初步减少 90% 至 99%](#item-tech-news-14) ⭐️ 7.0/10

**财经新闻**
1. [2026 年诺贝尔经济学奖授予霍尔与伍德福德](#item-finance-news-1) ⭐️ 9.0/10
2. [美联储哈马克警告可能需要进一步加息以避免通胀预期固化](#item-finance-news-2) ⭐️ 7.0/10
3. [新能源汽车出口退税率由 13% 下调至 9%](#item-finance-news-3) ⭐️ 7.0/10
4. [税务总局发布新处罚基准 社保欠缴最高罚三倍](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [MiniCPM-V 4.7-35B-A3B 开源 MoE 模型发布](https://www.reddit.com/r/LocalLLaMA/comments/1x47taj/openbmbminicpmv4735ba3b/) ⭐️ 9.0/10

openbmb 发布 MiniCPM-V 4.7-35B-A3B，该模型是 MiniCPM-V 系列的首个开源 Mixture-of-Experts \(MoE\) 变体。该模型引入 Lookahead Expert Scheduling \(LES\) 技术，结合细粒度层-wise 量化与 DSpark speculative sampling，在 iPhone 17 Pro Max 上实现 13+ tokens/s 的解码速度，同时保持单图、多图、视频等多模态理解能力。与 Qwen3.6 35B-A3B 相比，该模型在指令模式下整体得分更高、推理时间更短，推动了多模态大模型在资源受限设备上的性能-效率帕累托前沿。

reddit · r/LocalLLaMA · /u/Skyline34rGt · 10月12日 17:16

**「背景」** MiniCPM-V 系列此前已具备单图、多图及视频理解能力，MiniCPM-V 4.7 是该系列中首个采用混合专家（MoE）架构的版本。该模型引入 intra-ViT 早期压缩技术（源自 LLaVA-UHD v4），旨在提升资源受限设备上的多模态推理能力密度。

**「开发者影响」** 开发者可以在 iPhone 17 Pro Max 等移动设备上部署 35B 参数 MoE 模型，实现每秒 13+ 个 token 的实时多模态推理，无需依赖云端服务，从而降低延迟并保护隐私。兼容 SGLang、vLLM、llama.cpp 与 Ollama 等主流推理框架，开发者可根据部署环境选择对应量化方案（GGUF、AWQ、GPTQ 或 FP8），但需注意不同量化等级可能影响模型性能与兼容性。

**标签**: `#open-source`, `#Mixture-of-Experts`, `#on-device-inference`, `#AI`, `#computer-vision`

---

<a id="item-tech-news-2"></a>
### [Looped Diffusion Transformer: the same blocks run several times inside each denoising step, and loop depth can be changed at sampling time \[R\]](https://www.reddit.com/r/MachineLearning/comments/1x49d61/looped_diffusion_transformer_the_same_blocks_run/) ⭐️ 8.5/10

A new diffusion transformer architecture that loops the same transformer blocks across denoising steps, achieving superior performance with dramatically lower compute compared to scaling up model size.

reddit · r/MachineLearning · /u/Fit-Ant2238 · 10月12日 18:13

**标签**: `#diffusion-transformer`, `#efficiency`, `#architecture`, `#scaling`

---

<a id="item-tech-news-3"></a>
### [Hello Python 3.15, goodbye 3.10, and now I can use 3.11](https://simonwillison.net/2026/Oct/12/python-3-15/) ⭐️ 8.0/10

Python 3.15 released with explicit lazy imports and other features; Simon Willison highlights the release and its impact on version support policies.

rss · Simon Willison · 10月12日 18:15

**标签**: `#Python`, `#programming languages`, `#software engineering`, `#open source`, `#release announcement`

---

<a id="item-tech-news-4"></a>
### [U-Space: Uncovering When and Why Uncertainty Arises in Language Models \[R\]\[D\]](https://www.reddit.com/r/MachineLearning/comments/1x44f9m/uspace_uncovering_when_and_why_uncertainty_arises/) ⭐️ 8.0/10

U‑Space introduces an interpretable, single‑pass uncertainty estimator for language models that identifies ambiguity, missing info, conflicting evidence, or general uncertainty without extra sampling or labeled data.

reddit · r/MachineLearning · /u/AdRevolutionary3242 · 10月12日 15:10

**标签**: `#uncertainty quantification`, `#interpretability`, `#open‑weight models`, `#AI research`, `#confidence estimation`

---

<a id="item-tech-news-5"></a>
### [learnc 自动调优 C 代码常量，实现更小的 JPEG 和更高的语音活动检测 F1 分数](https://www.reddit.com/r/MachineLearning/comments/1x4dlbm/learnc_fit_the_constants_in_existing_c_code_to/) ⭐️ 8.0/10

learnc 是一个开源（MIT 许可）工具，它能够在不修改原始 C 代码的情况下，通过用户定义的评分函数自动调整代码中命名的常量值。该工具在保持代码原样完整的前提下，将 JPEG 量化表的 BD-rate 降低了 9.1%，在 WebRTC 语音活动检测（VAD）任务上将 F1 分数提升了约 4.9 个百分点。这一成果是在已有生产级 C 代码（如 stb\_image\_write.h 的 128 个量化表）上验证的，证明了对“魔法常量”进行自动化的系统工程优化方法具有实用价值。

reddit · r/MachineLearning · /u/keep\_up\_sharma · 10月12日 20:51

**「learnc 解决的核心问题是手动调优难以扩展且容易出错」** 在软件工程实践中，许多 C/C++ 库使用大量预先设定的常量（如量化表、滤波系数等），这些常量通常需要人工调试才能达到最佳性能或效果。learnc 通过提供一个可编程的框架，让开发者只需编写一个评分函数，就能让工具自动搜索最优的常量组合，从而避免手动调参带来的时间成本和风险。

**标签**: `#compiler-optimization`, `#image-compression`, `#voice-activity-detection`, `#automated-tuning`, `#systems-engineering`

---

<a id="item-tech-news-6"></a>
### [Qwen released QwenGyre - RL framework for training AI agents on extremely long complex tasks](https://www.reddit.com/r/LocalLLaMA/comments/1x41myz/qwen_released_qwengyre_rl_framework_for_training/) ⭐️ 8.0/10

Qwen releases QwenGyre, a new RL framework enabling efficient training of AI agents on extremely long complex tasks through elastic resource management and trajectory-based sample optimization.

reddit · r/LocalLLaMA · /u/ResearchCrafty1804 · 10月12日 13:18

**标签**: `#RL framework`, `#long-horizon training`, `#AI agents`, `#efficient training`, `#trajectory processing`

---

<a id="item-tech-news-7"></a>
### [Boole-1.7B 发布 1 位量化 Qwen3-1.7B 模型，内存仅 247 MB](https://www.reddit.com/r/LocalLLaMA/comments/1x452zj/boole17b_a_1bit_qwen317b_model_that_outperforms/) ⭐️ 8.0/10

Boole-1.7B 是 Qwen3-1.7B 的 1 位量化版本，将模型权重压缩至 247 MB（比 BF16 版本小 13.9 倍），同时在 10 项任务评估中保持约 85.9% 的全精度得分。它不仅超越了现有的 1 位量化模型 Bonsai-1.7B，还几乎达到了 1.58 位量化 Bonsai-1.7B 的性能水平。该模型已通过 Precision Numerics 开源发布，提供 Hugging Face 权重、vLLM/llama.cpp 演示代码和浏览器内聊天界面，供低延迟的英语任务使用。

reddit · r/LocalLLaMA · /u/d77chong · 10月12日 15:35

**「背景」** 1 位量化技术将大型语言模型的参数压缩到单个二进制位，显著降低内存占用，但通常会造成较大的精度损失。Bonsai-1.7B 等早期项目展示了 1 位量化模型在边缘设备上的可行性，但性能与全精度模型之间仍存在明显差距。Boole-1.7B 进一步将这种技术应用于 Qwen3-1.7B 架构，通过优化量化策略，在保持较小存储空间的同时，实现了更优的精度‑大小权衡。

**「影响」** 用户现在能够在仅几百兆字节内存的设备（如笔记本电脑或浏览器）上运行相当于 Qwen3-1.7B 规模的模型，同时保留约 86% 的语言理解和生成能力，从而实现低延迟的离线推理，无需依赖云端服务。开发者可直接通过提供的 vLLM 或 llama.cpp 演示代码集成 Boole-1.7B，实现轻量级本地部署。

**标签**: `#Model Compression`, `#Quantization`, `#Open Source LLM`, `#Edge AI`, `#Performance Optimization`

---

<a id="item-tech-news-8"></a>
### [Codex CLI 默认安装持久后台守护进程](https://github.com/openai/codex/issues/48195) ⭐️ 7.5/10

OpenAI Codex CLI 现在默认安装一个持久且自动更新的后台守护进程，可能占用约 12 GB 磁盘空间并导致自动更新时的权限错误。用户可以通过在 ~/.codex/config.toml 中将 daemon\_auto\_start 设为 false 来禁用此守护进程，但该选项尚未得到广泛文档说明。守护进程在启动时会在 ~/.codex 目录下创建 pid 和锁文件。

hackernews · whimblepop · 10月12日 18:29 · [社区讨论](https://news.ycombinator.com/item?id=50060694)

**「Codex CLI 默认启用后台守护进程」** OpenAI Codex CLI 在版本 0.157.0 中将 daemon\_auto\_start 默认设置为开启状态，导致安装时自动安装一个持久化的后台守护进程（自更新），该守护进程占用约 12 GB 磁盘空间。此前该功能可通过配置项 daemon\_auto\_start = false 关闭，但现在默认行为已改变，影响了用户和开发者的使用体验。

**「影响」** 如果不进行配置，用户可能会因磁盘空间被填满或权限错误而出现系统不稳定，需要手动禁用守护进程或调整文件权限。

**「社区讨论」** 多位用户指出守护进程占用约 12 GB 空间并在此目录生成 pid 与锁文件，建议通过未公开的 daemon\_auto\_start 标志或使用链接到 /dev/null 并设为不可写入来禁用它，而另一些用户则批评 Codex 过于复杂，更倾向于使用更简约的 harness。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://codex.danielvaughan.com/2026/09/25/codex-cli-daemon-auto-start-stable-default-v0157/">Daemon Auto-Start Is Now the Stable Default in Codex CLI v0 ...</a></li>
<li><a href="https://github.com/openai/codex/issues/48195">CLI: make `daemon_auto_start` opt-in — a persistent, self ...</a></li>
<li><a href="https://www.solosoft.dev/post/codex-cli-daemon-audit/">Codex CLI Now Starts a Self-Updating Daemon by Default: 373 ...</a></li>

</ul>
</details>

**标签**: `#software\_engineering`, `#ai\_coding\_tools`, `#open\_source`, `#technology\_industry`, `#daemon\_management`

---

<a id="item-tech-news-9"></a>
### [黑客激活欧洲超市冷柜自动除霜功能](https://www.tomshardware.com/tech-industry/cyber-security/unprecedented-cyberattack-cripples-supermarket-fridges-across-europe-as-hackers-activate-automatic-defrosting-delivery-and-store-prices-also-impacted-by-incident) ⭐️ 7.0/10

一场针对欧洲超市制冷系统的网络攻击激活了冷柜的自动除霜功能，导致部分冷藏温度上升并带来食品变质风险。法国连锁超市 Intermarché 确认约 150 家门店受到影响，除温度异常外，配送系统和商店价格信息也受到波及。涉事制冷控制器被怀疑与 Danfoss 产品有关，相关安全公司已发布针对该类控制器的漏洞分析报告。

hackernews · Zeekaas · 10月12日 12:16 · [社区讨论](https://news.ycombinator.com/item?id=50055304)

**「背景信息」** 商用制冷控制器联网主要用于远程诊断和能效优化——供应商宣传称这能减少工程师上门并支持跨门店性能对比。社区评论指出涉案设备可能包括 Danfoss SM800（支持至 2021 年）和 SC355（支持至 2016 年）等已停产的旧型号。另有观点将此次攻击与 2026 年 8 月美军基地冷冻库遭入侵事件相联系，怀疑是否为同一团伙所为。

**「影响」** 门店需紧急关闭受影响冷柜以保护库存，造成运营中断与潜在的食品报废损失。此次事件突显联网工业设备的普遍问题：老款控制器在停止支持后缺乏安全审查与定期更换，而

**「社区讨论」** 评论者指出部分涉案控制器已停产多年，这类设备往往没有安全评审周期与定期更换保障。另有讨论质疑攻击是否源于 8 月美军基地冷冻库入侵事件的同一群体，或仅是受到该报道启发。

**标签**: `#cybersecurity`, `#IoT`, `#vulnerability`, `#retail`, `#supply-chain`

---

<a id="item-tech-news-10"></a>
### [WiFi 7 路由器改装为 320Msps SDR 接收机](https://github.com/h0m3us3r/w1700k-sdr) ⭐️ 7.0/10

开发者 h0m3us3r 在 GitHub 项目 w1700k-sdr 中发布了将 WiFi 7 路由器改装为 320 Msps 软件定义无线电（SDR）接收机的方法，适用于 5 GHz 信号。该项目利用路由器的硬件能力，提供一种低成本的高速射频接收方案。该改装面向硬件黑客和开源 SDR 社区，已获得显著关注。

hackernews · djfergus · 10月12日 12:41 · [社区讨论](https://news.ycombinator.com/item?id=50055593)

**「背景」** 软件定义无线电（SDR）通过软件而非专用硬件电路来处理射频信号，这使得消费级通信芯片具备被改造成接收机的潜力。在此类尝试中，已有基于 ESP32 等 Wi-Fi 微控制器的 SDR 收发器及 2.4/5 GHz 扫描项目，验证了低成本无线芯片在特定频段的可复用性。本次项目沿用了类似思路，将适用对象扩展到了采样率更高、硬件接口更开放的 WiFi 7 路由器芯片上。

**「影响」** 这为硬件黑客和开源 SDR 爱好者提供了一种以较低成本获取 320 Msps 5 GHz 接收能力的途径，降低了高速射频接收的门槛。

**「社区讨论」** 社区用户指出，该开发者此前已将 ESP32 Wi-Fi 微控制器改装为 SDR，并希望未来能在更多常见 Wi-Fi 设备上看到类似项目；另有用户认为该方案可能适用于 Banana Pi R4 等使用相同芯片组的设备。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.rtl-sdr.com/esp32-sdr-trx-use-an-esp32-s3-as-a-receiver-for-sdr-and-as-an-fm-ssb-voice-transmitter-on-13cm/esp32-sdr-trx/">esp32- sdr -trx</a></li>

</ul>
</details>

**标签**: `#software-defined-radio`, `#hardware-hacking`, `#wifi-7`, `#open-source`, `#sdr`

---

<a id="item-tech-news-11"></a>
### [Muse Wonder](https://research.meta.ai/blog/muse-wonder) ⭐️ 7.0/10

Meta&\#x27;s new Muse Wonder model prompts technical evaluation and privacy debates in the community.

hackernews · meetpateltech · 10月12日 16:48 · [社区讨论](https://news.ycombinator.com/item?id=50059115)

**标签**: `#AI models`, `#Meta AI`, `#performance benchmarks`, `#privacy`, `#multimodal AI`

---

<a id="item-tech-news-12"></a>
### [Reddit 提问当前 AI 机制能否催生通用智能](https://www.reddit.com/r/MachineLearning/comments/1x4awlk/what_is_the_strongest_mechanistic_argument_that/) ⭐️ 7.0/10

Reddit 用户 /u/Repulsive\_Twist\_9221 发起提问，寻求关于当前 AI 系统（基于 next‑token prediction 和强化学习）能否催生通用智能的最强机制论证，要求基于因果机制、计算学习理论和信息论等第一性原理，而非趋势外推。

reddit · r/MachineLearning · /u/Repulsive\_Twist\_9221 · 10月12日 19:09

**「背景」** 当前主流大语言模型（LLM）的训练范式包含两个核心阶段：首先通过海量文本语料进行下一词预测的自监督预训练，学习语言的统计规律与世界知识；随后利用基于人类反馈的强化学习（RLHF）或基于 AI 反馈的强化学习（RLAIF）进行对齐微调，使模型输出符合人类偏好与安全规范。该 Reddit 讨论聚焦于这一“预训练 + 强化学习”组合机制，从因果机制、计算学习理论、信息论等第一性原理出发，探讨其是否能在理论上支撑开放式通用智能（AGI）的涌现，而非依赖趋势外推或未来突破的假设。

**「影响」** 该提问凸显了理论界对当前学习范式能否支撑 AGI 的不确定性，可能推动研究者更注重从机制角度验证 AGI 的可行性。

**标签**: `#artificial general intelligence`, `#machine learning theory`, `#large language models`, `#reinforcement learning`, `#community discussion`

---

<a id="item-tech-news-13"></a>
### [Decision 3.0 发布：0.6B-27B 开源多模态决策模型](https://www.reddit.com/r/LocalLLaMA/comments/1x3th4p/decision_30_open_multimodal_decision_models_from/) ⭐️ 7.0/10

vLLM Semantic Router 团队发布 Decision 3.0 \(d3\) 开源多模态决策模型家族，参数量覆盖 0.6B 至 27B，采用 Apache-2.0 许可。模型基于 Qwen3.5 \(0.8B/2B/4B/9B\) 与 Qwen3.8-27B 构建，包含视觉编码器（4B 模型含 0.33B，27B 模型含 0.46B），支持文本、图像（最高 1.6 MP）与视频（2 fps 采样，最多 32 帧，每帧 0.2 MP）三种模态输入。提供 choice、yes/no、score 三类决策输出，单次前向传递可并行回答多个问题。权重为 BF16 格式，需在 Transformers 中设置 trust\_remote\_code=True 加载，训练于 AMD Instinct MI325X。官方自测显示 27B 模型在 Jev Decision Index 文本榜得 64.7 分、视觉榜得 71.6 分，均排名第一；各规模模型均领跑同级别，9B 版本 \(d3-flash\) 超越上一代 27B 模型；零样本视频任务上 27B 在 Perception Test 验证集得 77.4 分、4B 得 70.3 分。模型已上传 Hugging Face。

reddit · r/LocalLLaMA · /u/henzy123 · 10月12日 05:26

**「背景」** Decision 模型系列由 vLLM Semantic Router 团队开发，其核心特点是对候选答案直接输出概率分布而非生成文本，该系列此前已推出基于 Qwen3.5-9B 的 Decision 1.0，以及代号 Vega-27B、于 2026 年 10 月 2 日发布的 Decision 2.0。Decision 3.0 为该系列最新迭代，此次扩展支持图像和视频等多模态输入，并覆盖 0.6B 至 27B 的模型规模。

**「影响」** 开发者可直接在本地或私有部署中使用 Apache-2.0 许可的多模态决策模型，无需生成文本即可获得结构化决策概率，适合路由、分类、评分等低延迟场景；但需注意 trust\_remote\_code=True 带来的代码执行风险，且基准成绩为官方自测，尚缺独立复现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/vllm-sr/d3">vllm -sr/d3 · Hugging Face</a></li>
<li><a href="https://modelsystem.one/news/vllm-sr-decision-2-family/">vLLM Semantic Router releases Decision 2.0, open decision ...</a></li>
<li><a href="https://systemonemodels.tech/vllm-semantic-router/decision">decision : open AI decision model by vLLM Semantic Router</a></li>

</ul>
</details>

**标签**: `#multimodal`, `#decision models`, `#open source`, `#LLM`, `#evaluation`

---

<a id="item-tech-news-14"></a>
### [🤖 Anthropic：蒸馏数据初步减少 90% 至 99%](https://www.anthropic.com/research/distillation-defenses) ⭐️ 7.0/10

Anthropic reports its new anti-distillation measures reduce stolen model capabilities by 90-99%, with specific technical safeguards and low false-positive rates.

telegram · zaihuapd · 10月13日 01:25

**标签**: `#AI security`, `#model distillation`, `#Anthropic`, `#machine learning`, `#technology news`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [2026 年诺贝尔经济学奖授予霍尔与伍德福德](https://x.com/NobelPrize/status/2109581902541939046) ⭐️ 9.0/10

2026 年诺贝尔经济学奖授予罗伯特·E·霍尔和迈克尔·伍德福德，以表彰他们在宏观经济稳定的微观经济基础方面的贡献。

telegram · zaihuapd · 10月12日 10:27

**「背景」** 罗伯特·霍尔是斯坦福大学经济学教授、胡佛研究所高级研究员；迈克尔·伍德福德是哥伦比亚大学宏观经济学家兼货币理论专家。二人长期研究微观经济行为如何支撑宏观经济稳定，尤其在货币政策、通胀预期与就业波动的理论基础上贡献卓著。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Robert_Hall_%28economist%29">Robert Hall ( economist ) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Michael_Dean_Woodford">Michael Dean Woodford - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Nobel Prize`, `#Macroeconomics`, `#Monetary Policy`, `#Academic Research`, `#Economic Theory`

---

<a id="item-finance-news-2"></a>
### [美联储哈马克警告可能需要进一步加息以避免通胀预期固化](https://www.cnbc.com/2026/10/12/beth-hammack-fed-inflation-policy.html) ⭐️ 7.0/10

克利夫兰联储总裁贝丝·哈马克表示，为避免通胀心态根深蒂固，可能需要进一步收紧货币政策。她指出，2026 年 8 月个人消费支出（PCE）价格指数同比上涨 3.4%（实际数据），通胀仍高于 2%的目标。

rss · CNBC Finance · 10月13日 02:58

**「背景」** 上个月美联储时隔三年首次加息，9 月会议纪要显示官员们认为可能再次投票加息。

**标签**: `#Federal Reserve`, `#interest rates`, `#inflation`, `#monetary policy`, `#Beth Hammack`

---

<a id="item-finance-news-3"></a>
### [新能源汽车出口退税率由 13% 下调至 9%](https://www.news.cn/20261012/9709731f470b42f9a84825c2e4eb914b/c.html) ⭐️ 7.0/10

Government reduces NEV export tax rate from 13% to 9% effective April 1, 2027, and cancels VAT export tax for certain products like e-cigarette equipment.

telegram · zaihuapd · 10月12日 11:00

**标签**: `#policy`, `#automotive`, `#trade`, `#tax`, `#nev`

---

<a id="item-finance-news-4"></a>
### [税务总局发布新处罚基准 社保欠缴最高罚三倍](https://fgk.chinatax.gov.cn/zcfgk/c100012/c5252754/content.html) ⭐️ 7.0/10

国家税务总局发布《全国税务行政处罚裁量基准（2026 年版）》，自 2026 年 11 月 1 日起施行，将用人单位逾期不缴或少缴社保费纳入处罚事项，经责令限期缴纳后仍不缴纳的，最高可处欠缴金额三倍罚款，并须补缴欠费及按日万分之五滞纳金。

telegram · zaihuapd · 10月13日 02:45

**「背景」** 此前社保费征收职能已划转税务部门，新基准细化了税务部门对社保欠缴的行政处罚裁量标准。

**「影响」** 所有用人单位面临更严厉的社保合规成本，薪资核算与缴纳流程需强化合规审查以避免高额罚款。

**标签**: `#Tax policy`, `#Employment regulation`, `#Corporate compliance`, `#Social insurance`, `#China`

---