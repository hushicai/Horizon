---
layout: default
title: "Horizon Summary: 2026-11-17 (ZH)"
date: 2026-11-17
lang: zh
---

> 从 65 条内容中筛选出 8 条重要资讯。

---

**AI 技术与实践**
1. [采样时引导爵士伴奏模型](#item-ai-tech-1) ⭐️ 10.0/10
2. [Marimba 一模全能语音问答](#item-ai-tech-2) ⭐️ 8.0/10
3. [Neo4j Virtual Graph 正式发布：零 ETL 图抽象层上线 GCP](#item-ai-tech-3) ⭐️ 7.0/10

**科技新闻**
1. [vLLM v0.34.0 更新：新模型、扩展 KV 缓存、移除 Model Runner V1](#item-tech-news-1) ⭐️ 8.0/10
2. [CMU 在 YouTube 免费发布完整学期计算机科学课程](#item-tech-news-2) ⭐️ 8.0/10
3. [Optimizely 供应链恶意脚本感染 Zoom、GitLab 等网站](#item-tech-news-3) ⭐️ 8.0/10
4. [OpenAI 首阶段嵌入评估](#item-tech-news-4) ⭐️ 7.0/10

**财经新闻**
1. [英伟达 CEO 辞职与国会变局或重塑 AI 交易](#item-finance-news-1) ⭐️ 8.0/10

---

## AI 技术与实践

<a id="item-ai-tech-1"></a>
### [采样时引导爵士伴奏模型](https://www.reddit.com/r/MachineLearning/comments/1xxkyh3/steering_a_pretrained_music_transformer_at/) ⭐️ 10.0/10

该项目展示了 duetto：一个面向 MIDI 键盘的实时爵士伴奏系统，可在不微调模型的情况下，使用预训练 Anticipatory Music Transformer（Thickstun et al., 2023）进行采样时控制。系统把玩家演奏与模型生成合并为同一事件序列，并在每次采样前通过规则层修改 logits：屏蔽不允许的音符或节奏，同时偏置当前和弦音、强拍引导音以及引用乐句的下一音。乐句来自 Weimar Jazz Database，按独奏者呼吸位置切分、转调并在一个 chorus 内展开；演示中约 61% 的独奏音符来自引用乐句或主题，其余由模型生成。工程上，服务器提前约 1 秒采样，并在玩家演奏时重采样未播放部分，以降低延迟；作者报告在 3080 Ti 上 medium 模型约 12 ms/note、large 约 18 ms/note，在 Jetson Orin Nano 上 large 约 90 ms/note，仍可支持现场演奏。

reddit · r/MachineLearning · /u/GGAllin43 · 11月16日 09:19

**「采样时规则引导音乐 Transformer」** duetto 不微调模型，而是把玩家 MIDI 音符与模型生成音符合并为单一事件序列，由预训练 Anticipatory Music Transformer 逐音符续写。每次采样前，规则层会修改 logits：屏蔽不允许的事件，例如必须等待的手、音域外音高、非拍点贝斯；同时偏置应更可能的事件，例如当前和弦音、强拍 guide tone、引用乐句的下一音。乐句来自 Weimar Jazz Database，按独奏者呼吸位置切分，并转调到当前曲目和弦、跨 chorus 发展；演示中约 61% 独奏音符来自引用乐句或主题，其余由模型生成。为降低实时延迟，服务器预采样约 1 秒音乐，并在玩家演奏时重采样未播放部分；3080 Ti 上 medium 约 12 ms/note、large 约 18 ms/note，Jetson Orin Nano 上 large 约 90 ms/note。作者也指出当前边界：系统可能偏离玩家、响应难预测，规则偏置过强会像乐句书，过弱则不够爵士。

**「工程要点」** 适合在不微调预训练音乐模型的前提下，构建低延迟的实时伴奏或即兴互动系统。接入前提是能够读取并修改模型采样时的 logits，并配套和弦进行、音域限制与短语库等规则层。主要代价是模型自发性与规则约束的平衡脆弱，过强偏置会沦为短语集，过弱则失去爵士风格，且存在漂移与不可预测性；3080 Ti 上约 12–18 ms/note，Jetson Orin Nano 上大模型约 90 ms/note，可作为延迟参考。

**「未解问题」** 作者尚未解决系统会偏离玩家、响应难以预测，以及模型生成与规则偏置之间平衡脆弱的问题：偏置过强会像乐句库，偏置过弱则不够爵士。作者也公开询问，采样时引导是否能作为微调替代方案，还是会遇到能力上限。

**标签**: `#sampling-time-steering`, `#constrained-decoding`, `#music-transformer`, `#phrase-library`, `#real-time-generation`

---

<a id="item-ai-tech-2"></a>
### [Marimba 一模全能语音问答](https://www.reddit.com/r/MachineLearning/comments/1xxsqro/marimba_a_system_one_model_for_speech_r/) ⭐️ 8.0/10

Marimba 提出一种使用冻结 Qwen3-ASR-0.6B 编码器对 8 秒音频窗口一次前向传播，并通过轻量读出和 Platt 校准实现对多种语音问答任务的即时回答。在 1,000 条公开问题上，它在 6/9 测试中与或超过 Qwen3‑Omni（30B）的性能，尤其在说话人变更 AUROC（0.966‑0.980）和说话人计数上胜过 Pyannote 3.1，但 turn‑end 检测在 Smart Turn 数据集上表现不足，且在未见任务如场景分类上表现随机。

reddit · r/MachineLearning · /u/solanotodesch · 11月16日 15:47

**「实现方式」** 系统采用单一冻结 Qwen3‑ASR‑0.6B 对每个 8 秒窗口进行一次编码，解码假设通过贪婪或 4‑beam 搜索生成，词汇检测使用 Platt 校准后的概率，语言识别直接使用 ASR 的语言得分，turn‑end 使用冻结层 18 的小读出，说话人变更与计数使用层 12 的读出；实验在 1,000 条公开问题上与 Qwen3‑Omni 对比，并提供代码、模型权重和演示。

**「工程要点」** 适合需要一次前向传播即可回答多种 typed 问题的高效语音应用，前提是音频窗口长度可控且任务在训练数据（turn‑end、说话人变更、词汇检测）中已有对应读出；缺点包括对未见任务的泛化差、turn‑end 读出受限于 Smart Turn 数据，以及词汇检测的校准是否等价于专用 KWS 仍需验证。

**「未解问题」** 词汇检测是否应与专用关键词 spotting 模型比较，以及 turn‑end 检测在其他会议或现实音频数据上的评估方法尚未明确。

**标签**: `#speech`, `#ASR`, `#audio-question-answering`, `#calibration`, `#multimodal`

---

<a id="item-ai-tech-3"></a>
### [Neo4j Virtual Graph 正式发布：零 ETL 图抽象层上线 GCP](https://neo4j.com/blog/news/neo4j-virtual-graph-is-now-generally-available/) ⭐️ 7.0/10

Neo4j Virtual Graph 在 Aura（GCP）正式发布，提供零复制/零 ETL 的图抽象层，直接在 Snowflake、Databricks、BigQuery、Iceberg 表上运行 Cypher 查询。核心机制是确定性 Cypher→SQL 翻译，数据不出仓，保留原有治理。适用于 GraphRAG、欺诈/供应链分析、Agent 上下文注入等只读分析场景。延迟在秒/分钟级，Cypher 覆盖不全（无 OPTIONAL MATCH、最短路、无界变长、向量/全文搜索），不替代原生 AuraDB 的 OLTP/HTAP 需求。

rss · Neo4j Blog · 11月16日 17:25

**「核心机制」** 三步建模：手动定义、从 Schema 生成、AI 从表元数据生成。查诼时将 Cypher 确性翻译为 SQL 下推仓库执行，结果经 Bolt 返回图结构。引入量化路径模式（QPP）支持有界跳数遍历（如 \{1,4\}），编译为递归 CTE/数组聚合 SQL。集成 Aura 全栈：Agents、Bloom、Graph Analytics、Dashboards、API v2beta1、监控/EXPLAIN、暂停恢复、Private Link。Enterprise Edition 预览版额外支持 DuckDB、SQLite、PostgreSQL 及 BYOD JDBC。

**「工程落地建议」** 适合：已有数仓、需快速上图的 GraphRAG/分析/Agent 场景，且能接受秒级延迟、只读、Cypher 受限。接入前提：Aura 组织启用 AI、仓库账号具备行级权限、数据模型可映射为图。坑点：无界变长需改写为 QPP 显式上界；向量/全文搜索需另接原生库；高并发低延迟走 AuraDB。同模型/数据源可一键迁移至 Data Importer 做全量导入，平滑过渡到原生图。

**「待解问题」** GA 版仍缺外部 IdP、Aura MCP Server、多源合成（Composite）支持，官方称「即将推出」但无时间表。Enterprise Edition 单实例限制、配置文件方式、无图算法，GA 预计 2027 Q1，生产可用性待验证。

**标签**: `#GraphRAG`, `#context-engineering`, `#agentic-ux`, `#governance`, `#zero-ETL`

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [vLLM v0.34.0 更新：新模型、扩展 KV 缓存、移除 Model Runner V1](https://github.com/vllm-project/vllm/releases/tag/v0.34.0) ⭐️ 8.0/10

vLLM v0.34.0 于 2026 年 11 月 16 日发布，引入了 10 个新模型（如 Mistral Large 4、MiniMax-M3.1-Flash 等），并将扩展式 KV 缓存默认开启，使模型在内存空闲后自动调整 KV 缓存大小，从而提升吞吐量和 TTFT。该版本取消 Model Runner V1，只保留 Model Runner V2 作为 GPU 运行器，并在 Blackwell、Hopper 和 AMD MI350/MI355X 上实现最高 1.95× 解码加速（Step5 on GB200）和 1.6× 输出吞吐（GLM-5.3-Flash）。升级前需修改环境变量（如去掉 VLLM\_USE\_V2\_MODEL\_RUNNER=0）、设置默认块大小为 64（原 16）、满足 huggingface\_hub ≥2.0.0、ROCm 10.0 图片以及 ROCm 7.2 已移除等依赖。

github · khluu · 11月16日 23:22

**「背景」** vLLM 是基于 GPU 核的 LLM 推理框架，之前的版本提供独立的模型运行器且不支持默认扩展式 KV 缓存；默认块大小为 16，且发布 ROCm 7.2 镜像。v0.34.0 将 KV 缓存扩展成为默认选项，切换到 Model Runner V2，统一依赖 ROCm 10.0、CUDA 13.0 以及 huggingface\_hub ≥2.0.0，旨在兼容最新硬件并提高推理效率。

**「影响」** 用户升级后会获得更大的 KV 缓存带来的吞吐提升，但在某些模型上单 token 解码延迟可能增加 6-18%，可通过 --gpu-memory-utilization 0.9 或 --no-enable-extensible-kv-cache 关闭。AMD ROCm 用户必须使用 ROCm 10.0 包和图片，旧版 ROCm 7.2 已不再提供。此外，新加入的模型如 Mistral Large 4、DeepSeek-V4 等扩展了支持范围，开发者需要更新配置文件并检查已移除的组件（如 QuTLASS、fp\_quant、Marlin W4A8、Keye-VL）。

**标签**: `#vLLM`, `#release`, `#performance`, `#model support`, `#KV cache`

---

<a id="item-tech-news-2"></a>
### [CMU 在 YouTube 免费发布完整学期计算机科学课程](https://www.cs.cmu.edu/learn/) ⭐️ 8.0/10

卡内基梅隆大学格里芬计算机科学学院推出免费 YouTube 频道 CS Learn，发布当前计算机科学课程的完整学期讲座。频道现已上线，本周每天首映一门课程，更多课程计划于 1 月发布，内容涵盖人工智能、概率与系统等领域。讲座由学生开发的自动化制作工具生成，小型团队即可完成制作。目前仅提供视频讲座，课件、项目作业和反馈机制尚未提供。

hackernews · pcompeau · 11月16日 20:43 · [社区讨论](https://news.ycombinator.com/item?id=50522980)

**「背景」** 高校计算机课程视频此前常分散在课程网站、单门课程页面或零散录播中，学习者难以按学期连续跟课。CMU 的 CS Learn 将当前课程的完整学期讲座集中发布到 YouTube，并借助自动化工具降低制作和发布成本。

**「影响」** 自学者和软件工程师可免费获取卡内基梅隆大学当前课程的完整讲座，但目前仅有视频，缺少课件、项目和反馈，完整学习体验可能受限，学习者可能需要自行寻找配套练习。

**「社区讨论」** 评论者 JSR\_FDED 认为学好基础才能让 AI 成为助力工具，而非被其取代。校友 fwx 期待 Tianqi Chen 的机器学习系统课程并请求增设其他课程，ecshafer 则指出缺少课件、项目和反馈时，单靠讲座视频学习效果有限。

**标签**: `#Free Online Courses`, `#Computer Science Education`, `#CMU CS Learn`, `#AI Fundamentals`

---

<a id="item-tech-news-3"></a>
### [Optimizely 供应链恶意脚本感染 Zoom、GitLab 等网站](https://blog.report-uri.com/worlds-largest-brands-infected-with-malware-via-optimizely/) ⭐️ 8.0/10

2026 年 11 月 16 日，Optimizely 的第三方标签管理片段（snippet）因供应链漏洞被入侵，部署到多个主流网站上，导致 Zoom、GitLab、CNN、BBC 等平台上的用户可能被恶意脚本感染。该攻击利用 Optimizely 的标签系统与 Google Tag Manager 提供的 JavaScript，攻击者通过已被入侵的 Optimizely 账户或跨客户凭证获得写权限，而非 CDN 缓存污染。影响范围包括 Optimizely 官方站点 www.optimizely.com 及登录页面 login.optimizely.com，以及其他依赖该服务的客户项目。社区讨论指出缺乏内部安全检查、发布阶段的缓冲和自动安全扫描，以及第三方标签未经充分审计的问题。

hackernews · kristjansson · 11月16日 23:00 · [社区讨论](https://news.ycombinator.com/item?id=50524767)

**「Optimizely 代码被篡改导致恶意软件感染」** 第三方 JavaScript 标签管理系统如 Optimizely 允许非工程团队直接部署代码，这增加了供应链被篡改的风险。报告指出，通过 Optimizely 传播的恶意脚本已影响 Zoom、BBC、CNN 等主要网站 \(tool-1-1\)。

**「影响与建议」** 受害者可能遭遇恶意代码执行，导致网站被劫持或数据泄露。对开发者而言，需要重新审查所有引入的第三方标签，确保代码完整性；对组织而言，应考虑将关键页面 vendored 或加强供应商管理，并要求 Optimizely 实施分阶段发布和自动安全检查。

**「社区讨论要点」** 评论中，mcoliver 强调当前缺乏可追责机制，建议网站应自行 vendoring 而非依赖外部供应商；stickfigure 提到 Google Tag Manager 可能带来约 10 MB 的 JavaScript 负载，并希望重新评估；eax-eip 澄清攻击并非 CDN 缓存污染，而是 Optimizely 系统本身的泄露，具体来源待进一步解释；skybrian 询问是否涉及加密货币或信用卡处理；thought-gap 推荐使用 NoScript 减少潜在危害。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gizmodo.com/sprawling-malware-attack-reportedly-affects-zoom-cnn-fox-news-peacock-and-170-others-2000840831">Sprawling Malware Attack Reportedly Affects Zoom and Other Major...</a></li>

</ul>
</details>

**标签**: `#security`, `#supply-chain-attack`, `#web-development`, `#javascript`, `#tag-management`

---

<a id="item-tech-news-4"></a>
### [OpenAI 首阶段嵌入评估](https://openai.com/index/our-first-phase-of-embedded-assessments) ⭐️ 7.0/10

OpenAI 开始其首阶段嵌入评估，并邀请 Apollo Research、METR、Transluce 和 Goodfire 等组织，在模型对齐、保障措施和监控系统方面独立评估。该消息显示 OpenAI 正尝试借助外部合作伙伴进行关键 AI 安全检查，但源内容较为简短，技术细节仍然有限。

rss · OpenAI News · 11月16日 08:00

**「嵌入式评估简介与 OpenAI 合作行动」** 嵌入式评估（embedded assessments）是指外部组织直接获得 OpenAI 内部模型和系统的访问权限，以实时检验模型对齐、安全护栏和监控机制。2026 年 11 月 16 日，OpenAI 宣布与 Apollo Research、METR、Transluce 和 Goodfire 等机构合作，将深度访问给其内部模型以独立评估对齐与安全系统。此举旨在提升 AI 系统的透明度和可信度，同时与当周其他安全相关披露（如 NCMEC 图像分类器）同步推进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/our-first-phase-of-embedded-assessments/">Our first phase of embedded assessments - OpenAI</a></li>
<li><a href="https://cellcog.ai/blog/openai-embedded-assessments/">OpenAI Lets Four Outside Groups Test Its Models | CellCog</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#model alignment`, `#independent evaluation`, `#OpenAI`, `#AI monitoring`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [英伟达 CEO 辞职与国会变局或重塑 AI 交易](https://www.cnbc.com/2026/11/14/nvidia-ai-trade-data-centers-congress.html) ⭐️ 8.0/10

英伟达 CEO 黄仁勋辞职，且民主党在 11 月 3 日选举后掌控国会，ETF 专家认为 AI 交易可能转向大型科技公司和其他芯片商；Yorkville Ives 将英伟达目标价从 300 美元下调至 225 美元，维持买入评级。

rss · CNBC Finance · 11月16日 12:13

**「背景」** 黄仁勋辞职前，英伟达刚经历动荡一周，公司任命首席财务官 Colette Kress 为临时 CEO，并计划于下周二公布第三季度财报。

**「影响」** Yorkville Ives 的 Dan Ives 估计，国会放缓数据中心建设可能使原计划项目的 10%无法落地，悲观情形为 15%-20%，但 AI 算力需求仍约为供应的四倍。

**标签**: `#Nvidia`, `#AI chips`, `#ETF`, `#Congress policy`, `#Market analysis`

---