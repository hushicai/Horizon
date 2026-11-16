# AI 应用开发技术雷达

当一条内容的核心价值是**构建、交付或运维 AI 应用所需的可复用技术知识**——某一层的架构、实现、取舍、踩坑、评测或工具链——而不是行业快讯、融资消息、产品营销或纯学术理论时，使用此配置。

定位：覆盖 AI 应用开发的**全栈知识体系**，自底向上 6 层 + 3 条横切；以应用开发技术为主，「模型」作为底座并行关注。一条内容命中任一子域即可能入选。

---

## 自底向上 6 层

### L1 · 模型与算力基础（并关注模型）
- **模型选型**：开源/闭源、LLM/SLM、专业化模型（代码/推理/多语言/嵌入/重排）、能力边界与评测、价格与兼容性
- **模型能力**：reasoning / extended & interleaved thinking、长上下文、多模态原生、结构化输出（JSON schema / constrained decoding）、function calling / 并行工具调用
- **模型适配与训练**：SFT、LoRA/QLoRA、蒸馏、量化、RLHF/DPO/GRPO、推理时计算（test-time compute / self-consistency / best-of-N / verifier）、评测污染与 benchmark 可信度
- **推理与服务**：vLLM / SGLang / TensorRT-LLM、KV cache、投机解码、批处理 / 多 LoRA 服务、GPU 与部署形态（本地 / 云 / 边缘）
- **模型路由与成本**：按复杂度路由、SLM-first / cloud-on-escalation、fallback、token 经济

### L2 · 数据与知识工程
- **数据接入与管道**：数据源连接（API / DB CDC / 爬虫 / 文件系统）、增量更新、ETL、合成数据、数据清洗与标注、数据集构建
- **文档解析**：PDF / OCR / 表格 / 扫描件解析、多模态文档（Marker / unstructured / PyMuPDF）
- **分块与表示**：chunking 策略（固定 / 语义 / 递归 /  late chunking）、embedding 模型选型、元数据富化
- **索引与存储**：向量索引（HNSW / IVF）、向量库、混合稀疏+稠密索引、权限继承（ACL / 文档级 / 字段级）
- **知识工程**：知识图谱构建、实体关系抽取、实体解析与归一化、社区发现、时序知识图谱
- **语义与本体**：本体建模、OWL / RDF / SPARQL / SHACL、taxonomy / schema / 语义层、ontology alignment、神经符号与知识表示、GraphRAG / 图检索 / 双路由查询

### L3 · 上下文与检索
- **RAG 全链路**：query rewrite / 分解、混合检索、rerank（cross-encoder）、引用与溯源、多路召回、召回评测（recall@K / MRR / NDCG）
- **Agentic / 多模态 RAG**：自适应检索、多跳推理、图增强检索、多模态检索
- **RAG 评测**：faithfulness / groundedness / context precision / recall / answer relevancy（RAGAS、DeepEval）
- **上下文工程**：write / select / compress / isolate、上下文压缩（compaction / LLMLingua）、上下文失效（context rot / poisoning / distraction / confusion / clash）、上下文预算
- **提示词与 PromptOps**：system prompt / few-shot / CoT / ToT / self-consistency、提示词版本管理 / Registry / A-B / 灰度 / 审批、结构化输出校验
- **记忆**：短期/工作/情景/长期/归档分层、向量记忆（Mem0）、图记忆（Zep / Graphiti / Cognee）、自编辑记忆（Letta / MemGPT）、遗忘与隐私、跨会话一致性

### L4 · 智能体系统
- **推理与循环范式**：ReAct、Plan-and-Execute、Reflexion、Plan-and-Revise、evaluator-optimizer、generator-reflector-curator (ACE)
- **目标管理**：目标分解、目标栈、子目标 DAG、完成判据、目标状态机、goal hijacking 防护、动态/局部重规划
- **停止与预算**：step cap、token / time / cost budget、done-check、timeout、loop detection、kill switch
- **动态动作流 / 编排**：静态 DAG → 条件 DAG → 状态机 → 自适应流程 → 混合分层；条件边、循环、回退、并行扇出/汇聚；动态规划（HTN / 世界模型 / 规划器-执行器-评估器）
- **工作流模式**：prompt chaining、routing、parallelization、orchestrator-workers、evaluator-optimizer；统一状态对象 / reducer / checkpoint / durable execution / 断点恢复
- **多智能体**：supervisor-worker / hierarchical / swarm / handoff / sequential / parallel / blackboard / router / critic-refiner；共享状态 / 消息传递 / 证据契约 / 冲突策略；上下文隔离、fan-out 宽度、handoff 深度、协调成本
- **协议与身份**：MCP（agent↔tool）、A2A / Agent Card / 网关（agent↔agent）、身份 / 最小特权 / 信任边界
- **工具与运行时**：function calling / tool schema / 幂等 / 参数校验、连接器生态、沙箱 / microVM / 代码执行隔离、computer-use / GUI / 浏览器 agent、Agent Harness / Skills / 子智能体

### L5 · 应用与交互
- **应用形态**：research / deep research、coding agent、客服、GUI agent、Text2SQL / 数据分析、RPA / 流程自动化、内容创作、垂直行业（医疗 / 金融 / 法律 / 教育 / 工业 / 具身）
- **多模态交互**：实时语音（ASR / TTS / VAD / barge-in / speech-to-speech / Realtime API）、视觉理解、文档 AI、视频理解、媒体生成、模态融合、可访问性
- **Agentic UX**：流式输出 / 首 token 延迟、可见规划、流式推理与工具调用展示、审批门 / 权限确认、置信度与不确定性提示、inline diff / 撤销 / 可中断 / 可引导、ambient agent、HITL / HOTL / 委托三种协作模式、透明与溯源 UI、失败态设计
- **框架与交付**：LangGraph / CrewAI / AutoGen / OpenAI Agents SDK / Claude Agent SDK / Google ADK / Semantic Kernel / Mastra、低代码（Dify / Coze / n8n）→ 工程化、SDK / 网关 / 前端集成

### L6 · 交付与生态
- **技术栈选型与迁移**：框架/向量库/网关生态存续度、功能趋同下的选型维度、迁移成本与锁定
- **开源生态**：开放权重、许可协议、模型/数据/MCP 供应链、社区活跃度
- **单位经济**：cost per completed task、质量-成本-延迟权衡、ROI
- **评测与基准生态**：leaderboard、benchmark 方法论与污染、评测标准组织、领域/语言覆盖

---

## 3 条横切（贯穿全栈）

### X1 · 评测与可观测
- 三层评测（final-answer / trajectory / per-turn）、离线（golden dataset / 回归门禁 / CI）/ 在线（采样）/ A-B / 影子
- 评分器（确定性检查、LLM-as-judge rubric + anchors + 固定裁判模型 + 人工校准、trajectory match、simulation）
- 指标（task completion、tool-call accuracy、step / loop count、cost / latency、groundedness、human escalation、用户纠正率）
- 基准工程含义（SWE-bench / GAIA / τ-bench / WebArena / LiveCodeBench、污染与饱和）
- Tracing / 观测栈（Langfuse / LangSmith / Phoenix / Braintrust / OpenTelemetry GenAI / OpenLLMetry）
- EDD 评估驱动开发、线上故障反哺评测集

### X2 · 可靠性 / LLMOps / 成本
- 幂等 / 重试退避 / 熔断 / 降级 / fallback 模型、超时 / 并发 / 队列 / 限流
- AI 网关（路由 / 重试 / 成本 / 限流 / 脱敏 / 策略）、Provider 抽象
- Prompt / 模型 / 数据集版本管理与 Registry、CI/CD for prompts、灰度 / 金丝雀 / 特征开关 / 秒级回滚
- 漂移检测、事件溯源、可观测与事件响应 runbook
- 缓存（精确 / 语义 / prompt caching）、成本归属 / 预算上限 / FinOps / denial-of-wallet 防护

### X3 · 安全 / 治理 / 合规
- OWASP Agentic Top 10 2026（ASI01 goal hijack、ASI02 tool misuse、ASI03 identity abuse、ASI05 意外代码执行、ASI06 记忆/上下文投毒、ASI07 不安全智能体间通信、ASI08 级联故障、ASI09 人-Agent 信任利用、ASI10 失控代理）
- 间接提示注入 / 越狱 / 不可信内容隔离 / 输出过滤 / XSS via AI
- 最小特权 / 工具白名单 / 参数校验 / 凭证隔离 / egress 控制 / 供应链审计（MCP server / 模型权重）
- Guardrails / 红队 / PII 脱敏 / 数据投毒防护 / 记忆投毒防护
- HITL 审批闸门 / kill switch / 审计日志 / 可追溯
- 隐私 / 遗忘权 / 版权 / 合成数据合规；合规框架（EU AI Act / NIST AI RMF / MITRE ATLAS / 《人工智能安全治理框架》）

---

## 典型载体
工程复盘与技术博客、数据/检索/RAG 管道实践、开源项目 README / 设计文档 / 含实现细节的 release、含代码或实验数据的深度分析、SDK / 框架 / 网关用法与迁移经验、评测与观测实战、生产事故复盘、带实测细节的社区技术讨论。论文仅在给出可落地做法或工程结论时使用本配置。

## 不使用此配置
纯资讯快讯、融资 / 估值 / 人事消息、无技术细节的产品发布、营销软文、只罗列提示词清单而无原理与证据的内容、纯趋势预测、以理论推导为主且无工程含义的论文，以及以完整长篇通用工程论证为唯一价值的文章（用 tech-blog）。
