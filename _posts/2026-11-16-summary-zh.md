---
layout: default
title: "Horizon Summary: 2026-11-16 (ZH)"
date: 2026-11-16
lang: zh
---

> 从 87 条内容中筛选出 9 条重要资讯。

---

**AI 技术与实践**
1. [Attest 1.1: CI 可重放无模型测试](#item-ai-tech-1) ⭐️ 10.0/10
2. [拆解视觉编码：预训练可选，专属参数必需](#item-ai-tech-2) ⭐️ 9.0/10
3. [cmt tune：将 B300 的 cudaMemcpy 速度提升 5 倍](#item-ai-tech-3) ⭐️ 9.0/10
4. [tenz 0.25：无损 GGUF 压缩器，手机端也能跑，体积再降 8–13% 且字节级还原](#item-ai-tech-4) ⭐️ 8.0/10
5. [现代 LLM 的位置编码](#item-ai-tech-5) ⭐️ 7.0/10
6. [开源技能库：用确定性脚本核验引用、双循环记忆避免重复失败实验](#item-ai-tech-6) ⭐️ 7.0/10

**科技新闻**
1. [uBlock Origin 通用 XSS 漏洞已修复](#item-tech-news-1) ⭐️ 8.0/10
2. [Qwen4-Max 发布，2.4 万亿参数，成本降 58%](#item-tech-news-2) ⭐️ 8.0/10

**财经新闻**
1. [中国 10 月经济数据全面不及预期](#item-finance-news-1) ⭐️ 8.0/10

---

## AI 技术与实践

<a id="item-ai-tech-1"></a>
### [Attest 1.1: CI 可重放无模型测试](https://www.reddit.com/r/LLMDevs/comments/1xwy3xy/attest_11_capture_an_agent_run_replay_it_in_ci/) ⭐️ 10.0/10

Attest 1.1 是一个 Apache-2.0 的开源测试框架，用于捕获 LLM 代理运行并可在 CI 中无模型调用地重放。它通过循环代理记录 OpenAI 与 Anthropic 的模型交互、脱敏并模板化可变值，自动生成行为与效果合约并进行断言。框架在 CI 中以 0 次真实模型调用、0 元费用运行，并通过合约、变异测试与 LLM judge 完成行为验证。

reddit · r/LLMDevs · /u/tom\_mathews · 11月15日 15:21

**「实现方式」** 它提供 \`attest capture\` 命令，在后台通过循环代理记录所有模型请求并生成可重放的跟踪文件。重放时使用同一代理代码在 CI 中，代理调用被代理响应替代，实现零真实模型调用。框架根据捕获的跟踪生成合约（如 \`tool\_cardinality\`）并检查效果（如一次 refund），同时对工具调用进行 drop、duplicate、reorder 变异以衡量覆盖率。LLM judge 在 deterministic 层之后运行，若 judge 不可用则标记为 not evaluated。

**「工程要点」** 当你需要在 CI 中验证代理行为且希望控制成本时，Attest 1.1 适合使用，前提是能在代理前部署循环代理并定义合约。缺点包括需维护合约、对提示变更的重放失效以及对 LLM judge 的可用性依赖，可能增加构建延迟。

**标签**: `#agent-testing`, `#replay`, `#behavior-contracts`, `#mutation-testing`, `#llm-judges`

---

<a id="item-ai-tech-2"></a>
### [拆解视觉编码：预训练可选，专属参数必需](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 9.0/10

Meta FAIR 与 NYU 的这项研究把多模态视觉编码拆成三个可独立选择的部分：编码器预训练、视觉专属参数、编码器是否放在 LLM 之前。作者用 200+ 个从零训练（含 LLM）且同数据的模型，把编码器预训练计入总计算预算，在 Qwen3-1.7B/4B（0.4B 视觉容量）和 0.6B–6.4B 缩放阶梯上评测 16 个 Cambrian VQA（448px）与 12 个语言基准。结论是预训练可选、视觉专属参数必需、编码器位置可选；这些是论文报告的结果，材料未提供独立复现。

reddit · r/MachineLearning · /u/trungh98 · 11月15日 17:38

**「实验设计」** 实验逐一消融三个选择，而不是比较现成模型，以避免数据与算力差异干扰。预训练侧测试了对比学习、自监督和两种 captioning 目标，在匹配总算力下最多只能追平与 LLM 一起从零训练的编码器；即使预训练免费也无增益。把 MetaCLIP 预训练延长 6.5 倍，ImageNet 线性探针从 80.4% 升到 84.4%，但 VQA 不涨。视觉专属参数方面，无编码器模型在 0.6B–6.4B 每个尺寸都落后，约需 3 倍算力才能追上；把编码器参数转给 LLM 只提升文本，不提升 VQA。位置方面，作者提出 in-fusion：在 LLM 前 8 层加入零初始化、仅视觉 token 使用的注意力投影与 FFN，文本 token 不经过这些权重；1.7B–6.4B 上与独立编码器持平，首 token 时间低约 13%。1.7B 下，第 1–8 层视觉专属分支 VQA 为 45.0（编码器 44.4），文本共享时为 42.3，放在最后 8 层为 35.1；在预训练 LLM 的中训练阶段加入视觉也得到相同趋势。

**「工程建议」** 自研多模态 LLM 时，应优先保留视觉 token 专用的参数或分支，不必把预算押在编码器预训练上；若想省掉独立编码器，可试在 LLM 前 8 层加零初始化视觉专属权重，报告称精度持平且首 token 延迟低约 13%。前提是接受 448px、16 个 VQA 基准与不超过 6.4B 的实验范围，接入时仍需用自己的数据和延迟基准复测。

**标签**: `#multimodal`, `#vision-encoding`, `#LLM-architecture`, `#compute-efficiency`, `#model-scaling`

---

<a id="item-ai-tech-3"></a>
### [cmt tune：将 B300 的 cudaMemcpy 速度提升 5 倍](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 9.0/10

本条内容介绍了一个名为 \`cmt tune\` 的工具，用于加速 B300 GPU 上的可分页内存传输，属于交付生态层。基准测试显示，对于 1 GB 张量的 GPU 拷贝，该工具将吞吐量从基线 10.2 GB/s 提升至 51.5 GB/s，实现了约 5 倍的加速。代码和基准测试已开源，可直接应用于 AI 模型服务等场景。

reddit · r/MachineLearning · /u/makneeee · 11月15日 18:20

**「B300 pageable cudaMemcpy 加速工具 cmt tune 使用与性能提升」** cmt tune 是开源项目 cudamemcpy-tuner 提供的命令行工具，专用于优化 Nvidia B300 上的 pageable cudaMemcpy 传输。使用 1 GB uint8 张量的基准测试显示，未经调优的 pageable 传输 throughput 约为 10.2 GB/s，运行 cmt tune -- python bench.py 后提升至约 51.5 GB/s。调优过程针对 B300 的内存子系统重新配置传输参数，实现约 5 倍的速度提升。项目随附博客教程与 GitHub 源码，支持 AI 工程师在模型服务或 LLMOps 流水线中复现与集成。

**「工程要点」** 适合在 B300 上无法改用页锁定内存、却需要大批量页可迁移主存到 GPU 拷贝的推理或训练管线尝试；接入前提是能用 \`cmt tune --\` 包裹现有启动命令，并自行从 GitHub 拉取开源代码运行。目前仅有单卡 B300 上 1 GB 主存到 GPU 拷贝的基准（10.2 GB/s 提升到 51.5 GB/s），未提供其他 GPU 型号、小包传输、多卡场景及生产环境延迟与稳定性数据，属社区演示工具，非 NVIDIA 官方发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://agihunt.info/en/p/1a1e07bf9febb7c90bad763fb45">cudamemcpy-tuner speeds up pageable cudaMemcpy… · AGI Hunt</a></li>
<li><a href="https://x.com/AndrewSignalZ/status/2122141782125535543">Andrew111 on X: &quot;新工具宣称在 NVIDIA B300 上让 pageable cudaMemcp...</a></li>

</ul>
</details>

**标签**: `#cudaMemcpy`, `#gpu-optimization`, `#memory-transfer`, `#cmt-tune`, `#benchmark`

---

<a id="item-ai-tech-4"></a>
### [tenz 0.25：无损 GGUF 压缩器，手机端也能跑，体积再降 8–13% 且字节级还原](https://www.reddit.com/r/LLMDevs/comments/1xxfogf/hoarding_ggufs_in_case_hugging_face_changes_fit/) ⭐️ 8.0/10

Reddit 用户 /u/Simpli-curious 发布 tenz 0.25，一个单文件、零依赖的 C 语言无损压缩工具，专门针对 GGUF 与 safetensors 格式。它解析量化块、提取真实量化值与 scale，再用上下文模型 + 静态表 rANS 编码，解压后逐字节还原，llama.cpp、Ollama、LM Studio 可直接加载。在 Poco F5 \(Termux\) 实测：Qwen3.5-2B Q4\_K\_M 节省 8.53%（zstd -19 仅 2.07%、xz -9 仅 1.78%），9 个 Q4\_K\_M 模型平均 7.6–9.2%，Gemma-4-31B QAT Q4\_0 达 13%，BF16 甚至 34%。压缩+解压 17 秒，zstd 压缩需 4 分钟。支持 Q3\_K~Q6\_K、Q4\_0、Q8\_0、F32/F16/BF16 及 tokenizer 元数据（约 80% 更小）。提供 -q 快速模式（少 0.3~0.4 点压缩率、编码量减 44%），以及实验性 -g OpenCL GPU 解压（手机 Adreno 725 上 150 MiB/s，仍慢于 3 大核 CPU 250 MiB/s）。代码与完整基线表已开源。

reddit · r/LLMDevs · /u/Simpli-curious · 11月16日 04:03

**「tenz 的 GGUF 无损压缩机制」** tenz 0.25 是单文件 C 实现、无外部依赖的 GGUF/safetensors 无损压缩器，核心做法是先解析 GGUF 结构，把每个量化块还原成真实的量化值与 scale，再用按文件拟合的上下文模型编码，解码端使用静态表的 rANS，因此解压时不需要重新学习模型。它支持 Q3\_K、Q4\_K、Q5\_K、Q6\_K、Q4\_0、Q8\_0、F32/F16/BF16 及元数据（tokenizer 约缩小 80%），其他类型原样存储；\`-q\` 快速模式以少量压缩率换取更快编码，例如 Qwen3.5-2B 从 8.54% 降到 8.18%，Q4\_K 工作量约减少 44%。作者在 Poco F5 的 Termux 环境中测试：Qwen3.5-2B Q4\_K\_M 节省 8.53%，对比 zstd -19 --long 的 2.07% 和 xz -9 的 1.78%；9 个模型的 Q4\_K\_M 节省 7.6–9.2%，Qwen3-4B 达 13.1%，Gemma-4-31B QAT Q4\_0 为 13%，Q8\_0 约 7.5%，BF16 约 34%，在量化模型上比通用压缩器 Aqueous 多 2–8 个百分点，BF16 持平。压缩加解压在该手机上耗时 17 秒，而 zstd 仅压缩就约 4 分钟；但解压明显更慢，1.2 GB 文件约需 7 秒，因为每个值都要经模型解码。实验性的 \`-g\` OpenCL GPU 解码最佳约 150 MiB/s，仅在极小分块下接近 3 个大 CPU 核的约 250 MiB/s 且损失 2 个百分点的压缩率；该驱动存在全局内存字节写入损坏相邻字节的问题，因此写入改为对齐的 32 位存储，且首个 GPU 分段始终与 CPU 结果校验。

**「工程要点」** 适合本地或边缘设备上需要囤积大量 GGUF 模型且存储受限的场景；tenz 是单 C 文件、无依赖，解压后逐字节还原，llama.cpp、Ollama、LM Studio 可直接加载。接入前需接受解压明显慢于 zstd/Aqueous（手机上约 7 s 处理 1.2 GB），且收益主要限于量化模型文件；GPU 选项 -g 仍是实验性，在 Adreno 725 驱动上曾出现相邻字节损坏，需额外校验。

**「待解问题」** 作者呼吁桌面 GPU \(OpenCL + subgroups\) 实测数据；解压速度远慢于 zstd/Aqueous（手机上 1.2 GB 需 7 秒），是否可通过 SIMD / 多线程进一步优化尚未给出方案。

**标签**: `#GGUF`, `#lossless-compression`, `#rANS`, `#model-storage`, `#LLMops`

---

<a id="item-ai-tech-5"></a>
### [现代 LLM 的位置编码](https://magazine.sebastianraschka.com/p/understanding-positional-embeddings) ⭐️ 7.0/10

这篇已发布文章由 Sebastian Raschka 撰写，解释了现代大语言模型如何编码 token 位置，并涵盖 GPT-2 的绝对位置嵌入、RoPE 相对位置旋转和 NoPE 等方法。文章用可视化、数学和小 PyTorch 实现说明 RoPE 如何通过旋转 query 和 key 来表达相对位置。它还汇总了部分 2026 年开放权重模型的定位编码选择，但被定位主要作为模型内部知识讲解，缺少应用层 benchmark 与生产取舍。

rss · Ahead of AI \(Sebastian Raschka\) · 11月15日 12:10

**「核心方法」** 文章先说明位置信息如何进入 LLM：GPT-2 把 learned absolute position embedding 加到 token embedding，而 MiniMax-M3 等更现代的模型则在 attention 中通过 RoPE 加入位置信息。RoPE 会按位置旋转 query 和 key 的特征对，注意力得分只依赖 query 与 key 的相对偏移。作者还讨论了 Inkling 的 learned relative position bias、NoPE 以及部分 RoPE 的使用。

**「工程启示」** 对应用开发而言，这篇文章更偏向模型内部机制解释，而不是可直接落地的应用层工程指南。虽然能帮助工程师理解长上下文行为，但作者强调它缺少应用层 benchmark、生产权衡和直接实现建议。

**标签**: `#RoPE`, `#positional-embeddings`, `#long-context`, `#transformer-architecture`, `#NoPE`

---

<a id="item-ai-tech-6"></a>
### [开源技能库：用确定性脚本核验引用、双循环记忆避免重复失败实验](https://www.reddit.com/r/LLMDevs/comments/1xx1lpj/open_source_mit_how_we_stopped_coding_agents_from/) ⭐️ 7.0/10

Kalaris Labs 发布 MIT 许可的 research-agent-skills，包含 281 个模块化 SKILL.md，面向 Claude Code、Codex、Cursor 等编码 Agent。核心贡献落在「上下文检索」与「智能体系统」层：按需安装单个技能避免上下文膨胀；用零依赖 Python 脚本对 Crossref、OpenAlex、arXiv、DataCite 等元数据源做确定性引用核验，仅允许机械补全 DOI、其余需人工确认；双循环实验编排（内层快速迭代、外层维护 findings.md）记录负结果防止重复失败超参。作者自述三大痛点与对应方案，但未给出准确率、召回率、延迟、成本或对比基线等可复核指标。

reddit · r/LLMDevs · /u/ProYash239 · 11月15日 17:40

**「核心机制」** 1\) 选择性安装：\`npx skills add KalarisLabs/research-agent-skills --skill &lt;name&gt;\` 仅拉取单个 SKILL.md 与辅助脚本，避免将几十个工具定义一次性注入系统提示。2\) 引用核验流水线：对每条 .bib 条目并行查询 Crossref、OpenAlex、arXiv、DataCite，并读取 Crossref 的 Retraction Watch 关系元数据；输出分类为 verified / found-add-doi / mismatch / doi-not-found / uncertain / not-found，Agent 仅自动执行 found-add-doi，其余强制人工介入。3\) 双循环实验编排：内循环针对目标指标快速迭代；外循环维护 findings.md，假设必须写成可测试机制（&quot;X because Y, predicting Z&quot;），负结果记录 &quot;ruled out&quot; 内容。4\) 提示注入与触发路由离线扫描：每个技能经 Skill Doctor 离线扫描，并用人工审核的提示集评估触发路由准确率。

**「工程落地建议」** 若你在构建研究型 Agent 或需要可审计引用的 RAG/技术写作工作流，可直接复用「确定性脚本+外部元数据源」的核验模式，并把「仅允许机械补全、其余人工确认」作为护栏；双循环 findings.md 可移植到任何多轮实验编排中，防止上下文压缩丢失负结果。接入前提：需自行部署或调用 Crossref/OpenAlex/arXiv/DataCite API（均有速率限制），并接受人工确认带来的交互延迟；281 个技能粒度较细，建议先按需引入 citation-verification 与 autoresearch 两个核心技能验证收益，再决定是否全量采用。

**「待解问题」** 作者征求社区反馈：该核验管线在哪些边界会失效（如预印本版本冲突、非英语文献元数据缺失），以及应优先接入哪些学术 API（如 Semantic Scholar、Dimensions、PubMed Central）。目前缺乏量化评测，无法判断 mismatch 分类的假阳性/假阴性率、人工确认的平均耗时、双循环在长周期实验中的存储增长与检索效率。

**标签**: `#citation-verification`, `#context-engineering`, `#agent-skills`, `#experiment-loop`, `#prompt-injection`

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [uBlock Origin 通用 XSS 漏洞已修复](https://iter.ca/post/ubo-uxss/) ⭐️ 8.0/10

uBlock Origin 浏览器扩展存在一个通用 XSS 漏洞，源于其元素选择器界面被放置在网站 DOM 中，攻击者可通过网站驱动的元素选择功能利用该漏洞。该漏洞已在 uBlock Origin 1.75.4 版本和 uBO Lite 2026.1110.1816 版本中修复，相关技术帖子包含概念验证代码。

hackernews · zaik · 11月16日 02:04 · [社区讨论](https://news.ycombinator.com/item?id=50513160)

**「背景」** uBlock Origin 的元素选择器功能允许用户在网页上点选元素以创建过滤规则。该功能的实现方式是将选择器界面直接注入到网站的 DOM 中，这使得网页脚本能够访问和操作扩展程序的内部界面元素。GitHub 安全公告显示，该漏洞于 2026 年 11 月 1 日通过邮件报告，攻击者可利用网站驱动的元素选择器触发通用跨站脚本攻击（Universal XSS），影响数千万用户。

**「影响」** uBlock Origin（Firefox MV2 版本）和 uBO Lite（MV3 版本）的用户曾面临通用型 XSS 风险：恶意网站可诱导元素选择器向扩展添加任意受信任过滤器，从而在任意源中执行脚本。该漏洞已通过在元素选择器通信中引入密钥验证机制修复，扩展后台脚本现在会校验消息是否来自合法的选择器 iframe。受影响用户应尽快更新到已修补版本。

**「社区讨论」** 社区讨论集中在扩展将界面注入页面 DOM 的设计模式风险：ByteOfWood 指出这可能导致密码管理器等扩展泄露账户信息；akersten 建议将创建规则元素移至浏览器界面而非页面 DOM 以根本解决；forgotmypw17 提供了修复版本号供用户核对；taylorfinley 称赞作者标注 AI 生成 POC 的做法；tux 建议删除旧 Firefox 配置文件并创建新配置文件安装修复版。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/gorhill/uBlock/security/advisories/GHSA-cmqw-9r2w-6wv2">Universal XSS from website-driven element picker</a></li>
<li><a href="https://iter.ca/post/ubo-uxss/">Universal XSS in uBlock Origin from website-driven element picker</a></li>
<li><a href="https://daily.dev/posts/universal-xss-in-ublock-origin-from-website-driven-element-picker-oqxmui7ak">Universal XSS in uBlock Origin from website-driven...</a></li>

</ul>
</details>

**标签**: `#Security`, `#Browser Extensions`, `#XSS`, `#uBlock Origin`, `#Web Security`

---

<a id="item-tech-news-2"></a>
### [Qwen4-Max 发布，2.4 万亿参数，成本降 58%](https://qwen.ai/blog?id=qwen4-max) ⭐️ 8.0/10

阿里巴巴通义千问正式推出新一代旗舰模型 Qwen4-Max，该模型采用全新稀疏 MoE 架构，总参数量达 2.4 万亿，原生支持视觉理解和百万 Token 长上下文，在编程、办公及长程任务执行方面表现优异，前端编程能力在 Code Arena 盲测中位居全球前列。成本方面，Qwen4-Max 单任务平均费用从 26.58 元降至 11.16 元，降幅近 58%，Token 消耗也减少近 50%，API 定价已同步下调，目前该模型已正式上线，团队透露后续将推出规模更小的 Qwen4 系列模型并公开模型权重。

hackernews · ilreb · 11月16日 02:14 · [社区讨论](https://news.ycombinator.com/item?id=50513215)

**「背景」** Qwen4-Max 是通义千问 Max 系列的新旗舰模型，官方表示后续将推出规模更小并公开权重的 Qwen4 系列模型。该模型提供 none、low、high、xhigh 四档推理强度，使调用方可以在响应速度、Token 成本和推理深度之间进行选择。

**「对开发者与开源生态的影响」** Qwen4-Max 单个任务平均费用从 26.58 元降至 11.16 元（降幅约 58%），配合 none/low/high/xhigh 四档推理力度，让开发者在生产环境中拥有了直接的成本-质量调节杠杆。但需注意两点风险：其一，社区实测显示前代 Qwen 3.8 输出速度仅约 30 tokens/sec（对比 Opus 约 80），对延迟敏感的 Agent 类应用可能构成瓶颈；其二，开源承诺仍存疑——阿里尚未公布 Qwen4-Max 及其 sibling 模型（Flash、27B 等）的规格与权重计划，开源生态的跟进速度尚不确定。

**「社区讨论」** 社区指出 Qwen4-Max 在成本上具有优势（平均费用 $3.27 低于 GPT‑6.1 Sol 的 $0.36），但速度仍较缓慢（约 30 tokens/s），影响实时应用；部分开发者因此对其在游戏战斗系统中的应用表示遗憾，同时对后续的“Flash”和 27B 版本持乐观态度，并质疑开源模型的整体进步速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://shattered.io/qwen4-launch-alibaba-open-source-promise-doubt-470-models-2026/">Qwen 4 Launch: Alibaba Open -Source Promise in Doubt</a></li>

</ul>
</details>

**标签**: `#open-source`, `#AI models`, `#performance`, `#cost`, `#reasoning`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [中国 10 月经济数据全面不及预期](https://www.cnbc.com/2026/11/16/china-retail-sales-october-industrial-output-investment.html) ⭐️ 8.0/10

中国 10 月零售、工业和投资数据全面低于预期，其中固定资产投资同比收缩 8.1%，跌幅较预期的 7%进一步扩大。

rss · CNBC Finance · 11月16日 03:53

**「背景」** 继三季度经济触底反弹后，10 月零售、工业和投资数据再度疲软，显示中国国内需求持续承压。

**「影响」** 固定资产投资 8.1%的收缩加剧了企业投资不足，对家庭就业机会造成直接影响，尤其体现在青年失业率高企之上。

**标签**: `#China economy`, `#macroeconomic data`, `#industrial output`, `#retail sales`, `#fixed-asset investment`

---