---
layout: default
title: "Horizon Summary: 2026-11-16 (EN)"
date: 2026-11-16
lang: en
---

> From 87 items, 9 important content pieces were selected

---

**AI Engineering / Research**
1. [Attest 1.1: Replay Agent Runs in CI](#item-ai-tech-1) ⭐️ 10.0/10
2. [多模态视觉编码解耦研究](#item-ai-tech-2) ⭐️ 9.0/10
3. [cmt tune accelerates pageable cudaMemcpy on B300](#item-ai-tech-3) ⭐️ 9.0/10
4. [tenz 0.25 lossless GGUF compression](#item-ai-tech-4) ⭐️ 8.0/10
5. [Positional Embeddings in Modern LLMs](#item-ai-tech-5) ⭐️ 7.0/10
6. [Kalaris Agent Skills](#item-ai-tech-6) ⭐️ 7.0/10

**Technology News**
1. [uBlock Origin patches universal XSS in element picker](#item-tech-news-1) ⭐️ 8.0/10
2. [Alibaba releases Qwen4-Max open-weight model with four reasoning levels and cost reductions](#item-tech-news-2) ⭐️ 8.0/10

**Financial News**
1. [China&\#x27;s October economic data miss forecasts](#item-finance-news-1) ⭐️ 8.0/10

---

## AI Engineering / Research

<a id="item-ai-tech-1"></a>
### [Attest 1.1: Replay Agent Runs in CI](https://www.reddit.com/r/LLMDevs/comments/1xwy3xy/attest_11_capture_an_agent_run_replay_it_in_ci/) ⭐️ 10.0/10

Attest 1.1 is an Apache-2.0 testing framework for LLM agents in Python and TypeScript, released on November 10. It captures an agent run through a loopback proxy for OpenAI Chat Completions, OpenAI Responses, and Anthropic Messages, plus an OTLP receiver, then replays the recording in CI with zero live model calls. It validates behavior with contracts, mutation testing, and optional LLM judges. The author reports that output-only tests caught 0 of 29 mutants, while contracts caught 10 of 29, and that 1.1 fixes four false-pass bugs found in a 73-finding audit of 1.0. The project has no external users yet.

reddit · r/LLMDevs · /u/tom\_mathews · Nov 15, 15:21

**「Method」** The \`attest capture\` command runs the agent behind a loopback proxy, records the trace and every model exchange, redacts secrets, templates volatile values such as IDs and timestamps, and drafts contracts from the observed run. Contracts can assert tool-call cardinality, for example at most one \`issue\_refund\` per \`order\_id\`, or check the end state of a simulated payments API. In PR CI, the current agent code runs while the proxy answers from the recording, so a changed prompt becomes a replay miss with a re-record command rather than a silent mismatch. \`attest policy evaluate\` turns the report into a merge gate with pass, block, and warn outcomes, and failures are annotated on the failing test line. \`attest mutate\` drops, duplicates, and reorders recorded tool calls to measure suite strength. LLM judges run after deterministic layers, and a judge outage or malformed reply is marked not evaluated, never passed. Version 1.1 fixes four false-pass cases involving stdio notification ordering, a timed-out response read by the next test, concurrent Vitest response swapping, and an empty pytest-xdist report accepted by the gate; it also fails unevaluated \`expect\(\)\` chains and blocks PRs that delete baseline assertions.

**「Engineering Takeaway」** Attest is most relevant to agents that change real systems, such as payments, tickets, or infrastructure, where reply-level assertions can miss duplicate side effects. Adoption requires recording representative runs and maintaining behavior or effect contracts; replay removes model cost and latency from CI, but prompt changes force re-recording. The framework is still pre-adoption, with no external users reported, so its coverage beyond the synthetic refund incident is unproven.

**「Open Questions」** The author is seeking design partners and criticism, and the project has no external users yet. It is unclear how well the contract-drafting and mutation-testing workflow generalizes beyond the demo incident.

**Tags**: `#agent-testing`, `#replay`, `#behavior-contracts`, `#mutation-testing`, `#llm-judges`

---

<a id="item-ai-tech-2"></a>
### [多模态视觉编码解耦研究](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 9.0/10

Meta FAIR 与 NYU 的论文（预印本）报道，通过训练 200 多个从零开始的多模态大模型，拆解了视觉编码器的三个设计选择：独立预训练可选、视觉专用参数必需、前置于 LLM 可选。该工作属于 match.md「模型」层，以 Qwen3-1.7B/4B 为主骨架，配 0.4B 视觉容量，在 16 个 Cambrian VQA 基准（448 像素）和 12 个语言基准上评估。可验证事实包括：视觉专用分支在 1.7B 模型上达 45.0 VQA，高于编码器的 44.4 和参数共享的 42.3。

reddit · r/MachineLearning · /u/trungh98 · Nov 15, 17:38

**「方法」** 所有模型在相同数据与计算预算下从零训练，编码器预训练计入多模态总预算。对比了对比学习、自监督及两种字幕目标的预训练编码器，并测试 MetaCLIP 预训练 6.5 倍更长对 ImageNet 线性探测（80.4%→84.4%）与 VQA 的影响。提出「In-fusion」：在 LLM 前 8 层插入零初始化的视觉专用注意力投影与 FFN，文本 token 不占用这些参数。以编码器前置、编码器免及参数共享给 LLM 作为基线，覆盖 0.6B 到 6.4B 骨架规模。

**「工程要点」** 工程接入时，可省略单独的视觉编码器预训练，但必须保留仅供视觉 token 使用的参数；将视觉分支注入 LLM 前层与传统编码器持平，且首 token 时间约降低 13%。前提是团队能承担从零训练 LLM 的计算成本，且结论目前局限于 Qwen3 骨架与 Cambrian 基准，其他模型族和数据组合未在文中验证。

**「未解问题」** 文中未披露超过 6.4B 骨架或非 Qwen3 架构上的表现，也未给出训练稳定性、推理显存占用及更长上下文下的边界情况。

**Tags**: `#multimodal`, `#vision-encoding`, `#LLM-architecture`, `#compute-efficiency`, `#model-scaling`

---

<a id="item-ai-tech-3"></a>
### [cmt tune accelerates pageable cudaMemcpy on B300](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 9.0/10

cmt tune is an open‑source tool that accelerates pageable cudaMemcpy transfers on NVIDIA B300, raising sustained bandwidth from ~10.2 GB/s to ~51.5 GB/s for 1 GB tensor transfers via torch.to\(&quot;cuda&quot;\). The optimization operates at the application‑interaction layer, improving host‑device data movement for pageable transfers. Key verifiable facts: baseline measured on PyTorch with a 1 GB torch.uint8 tensor; tuned result using \`cmt tune -- python bench.py\`; benchmark conditions specify pageable memory on B300.

reddit · r/MachineLearning · /u/makneeee · Nov 15, 18:20

**「Method」** The cudamemcpy‑tuner tool wraps pageable cudaMemcpy calls and uses a command‑line driver \(cmt tune\) to apply optimized memory‑transfer settings on NVIDIA B300 GPUs. It measures baseline performance \(≈10.2 GB/s for a 1 GB uint8 copy\) and then applies tuned parameters to raise throughput to ≈51.5 GB/s, a ~5× speedup. The implementation is open‑source \(GitHub repo\) and includes a benchmark script that reports GB/s for both CPU→GPU and GPU→CPU directions. The tool is invoked via the cmt tune wrapper, which automates the selection of optimal CUDA memory‑copy flags and stream configurations for pageable memory. Benchmarks confirm the improvement on B300, though performance may vary on other GPUs or with different data types and transfer sizes.

**「Evaluate cmt tune for pageable copies」** For LLM serving and inference paths where pageable cudaMemcpy between host and device is a latency bottleneck, the open-source cmt tune tool is worth evaluating as a concrete optimization. On a B300, it reportedly raised pageable CPU-to-GPU throughput for a 1 GB uint8 tensor from 10.2 GB/s to 51.5 GB/s, about a 5x improvement, though the reported gain may depend on hardware, transfer size, and workload.

<details><summary>References</summary>
<ul>
<li><a href="https://agihunt.info/en/p/1a1e07bf9febb7c90bad763fb45">cudamemcpy-tuner speeds up pageable cudaMemcpy… · AGI Hunt</a></li>
<li><a href="https://x.com/AndrewSignalZ/status/2122141782125535543">Andrew111 on X: &quot;新工具宣称在 NVIDIA B300 上让 pageable cudaMemcp...</a></li>
<li><a href="https://stackoverflow.com/questions/22345391/cuda-device-memory-copies-cudamemcpydevicetodevice-vs-copy-kernel">c - CUDA device memory copies... - Stack Overflow</a></li>
<li><a href="https://developer.nvidia.com/blog/how-optimize-data-transfers-cuda-cc/">How to Optimize Data Transfers in CUDA C/C++ | NVIDIA Technical...</a></li>
<li><a href="https://www.analyticsvidhya.com/blog/2026/10/llm-inference-explained-optimization-techniques/">LLM Inference Explained: Performance and Optimization Guide</a></li>

</ul>
</details>

**Tags**: `#cudaMemcpy`, `#gpu-optimization`, `#memory-transfer`, `#cmt-tune`, `#benchmark`

---

<a id="item-ai-tech-4"></a>
### [tenz 0.25 lossless GGUF compression](https://www.reddit.com/r/LLMDevs/comments/1xxfogf/hoarding_ggufs_in_case_hugging_face_changes_fit/) ⭐️ 8.0/10

tenz 0.25 is a lossless GGUF compressor that reduces quantized model file sizes by 7.6–13.1% \(up to 34% for BF16\) while restoring every file byte-for-byte, compatible with llama.cpp, Ollama, and LM Studio, operating in the data knowledge engineering layer of the full-stack system. It parses GGUF structure, codes quantized values and scales with rANS context models fitted to the file, and supports Q3\_K through Q8\_0, F32/F16/BF16, plus tokenizer metadata. Benchmarks on a Poco F5 show compression plus decompression taking ~17 seconds for Qwen3.5-2B Q4\_K\_M, versus ~4 minutes for zstd -19 --long, though decompression remains slower than general-purpose compressors.

reddit · r/LLMDevs · /u/Simpli-curious · Nov 16, 04:03

**「Method」** tenz 0.25 is a dependency-free, single-C-file lossless compressor for GGUF and safetensors that restores files byte-for-byte. It parses the GGUF container, unpacks each block into its real quantized values and scales, and encodes them with context models fitted to the file; rANS with static tables means decompression does not learn anything at runtime. Supported types are Q3\_K, Q4\_K, Q5\_K, Q6\_K, Q4\_0, Q8\_0, F32/F16/BF16, plus metadata, with the tokenizer reported about 80% smaller; unsupported types are stored unchanged. The author reports 8.53% savings on Qwen3.5-2B Q4\_K\_M versus 2.07% for zstd -19 --long and 1.78% for xz -9, 7.6–9.2% across nine Q4\_K\_M models, 13.1% on Qwen3-4B, 13% on Gemma-4-31B QAT Q4\_0, about 7.5% on Q8\_0, and about 34% on BF16; against Aqueous it claims 2–8 points more on quantized models and a tie on BF16. A \`-q\` quick mode trades a fraction of a point for faster coding, for example 8.54% to 8.18% on Qwen3.5-2B with about 44% less Q4\_K work. An experimental \`-g\` OpenCL path reached about 150 MiB/s versus about 250 MiB/s on the phone’s three big CPU cores, required aligned 32-bit stores because byte stores corrupted neighboring bytes on the driver, and always checks the first GPU segment against the CPU; decompression remains slower than zstd or Aqueous, at about 7 s for 1.2 GB on the phone.

**「Tenz 0.25 GGUF compressor: modest size savings, slower decompression」** Tenz 0.25 is a single‑file C lossless compressor for GGUF \(and safetensors\) that achieves 7‑13% size reduction on common quantized formats and up to 34% on BF16, but decompression on a phone takes ~7 s for 1.2 GB because each value is re‑coded, making it ~5–6× slower than zstd or Aqueous. It runs on low‑power devices \(tested on a Poco F5 in Termux\) and supports Q3‑Q8 quantization modes plus metadata; a quick mode \(-q\) trades a fraction of a percent for ~44% less CPU work, while GPU acceleration \(-g\) is experimental and limited by driver bugs.

**Tags**: `#GGUF`, `#lossless-compression`, `#rANS`, `#model-storage`, `#LLMops`

---

<a id="item-ai-tech-5"></a>
### [Positional Embeddings in Modern LLMs](https://magazine.sebastianraschka.com/p/understanding-positional-embeddings) ⭐️ 7.0/10

This article explains how LLMs encode token position, covering learned absolute embeddings \(GPT-2\), RoPE rotation of queries and keys, NoPE, and learned relative position bias. It sits in the model layer of the match.md stack and surveys positional choices in 2025–2026 open-weight models. Key facts: RoPE remains the most common method; SmolLM3 applies RoPE in three of every four layers; Inkling adds a learned relative bias before softmax. The piece is educational and lacks production benchmarks or direct application-level guidance.

rss · Ahead of AI \(Sebastian Raschka\) · Nov 15, 12:10

**「Method」** GPT-2 adds a learned position vector to each token embedding before the first transformer block. RoPE rotates query and key feature pairs by position-dependent angles inside attention, so the query-key dot product depends only on the relative offset between tokens. NoPE omits explicit positional encoding and relies partly on causal-mask implicit order; a 1.3B code model showed worse next-token prediction at the longest tested lengths. Inkling adds a learned relative position bias to attention scores before softmax. The article includes a small PyTorch RoPE walkthrough and a gallery-based survey of 2025–2026 model releases.

**「Engineering Takeaway」** Useful as model-internals background, but not a drop-in implementation guide for application engineers. RoPE is still the default choice; partial RoPE and NoPE appear in some recent open-weight models without enough published tradeoff data to justify switching. No production latency, memory, or compatibility numbers are provided.

**「Open Questions」** Whether the shift from full RoPE to partial RoPE/NoPE mixes will continue, given the survey groups are still small. How NoPE behaves at very long contexts beyond the tested 1.3B code model.

**Tags**: `#RoPE`, `#positional-embeddings`, `#long-context`, `#transformer-architecture`, `#NoPE`

---

<a id="item-ai-tech-6"></a>
### [Kalaris Agent Skills](https://www.reddit.com/r/LLMDevs/comments/1xx1lpj/open_source_mit_how_we_stopped_coding_agents_from/) ⭐️ 7.0/10

This open-source MIT repository &quot;Kalaris Agent Skills&quot; supplies 281 modular SKILL.md workflows aimed at stopping LLM hallucinations of citations and preventing repeated failed ML experiments in research agents. It performs deterministic citation verification by running zero‑dependency Python 3.9+ scripts against Crossref, OpenAlex, arXiv, DataCite, and Retraction Watch, classifying .bib entries and requiring human confirmation for mismatches or missing DOIs. The system also runs a two‑loop experiment orchestration \(inner rapid iteration, outer findings.md logging\) and scans prompts for injection using Skill Doctor, while offering selective per‑project installation via npx to avoid context‑window bloat. The toolkit supports Claude Code, Codex, Cursor, OpenCode, Gemini CLI, and Windsurf.

reddit · r/LLMDevs · /u/ProYash239 · Nov 15, 17:40

**「Methodology」** Architecture selects only the SKILL.md and helper scripts for a given repo via \`npx skills add KalarisLabs/research-agent-skills --skill &lt;name&gt;\`, limiting context load. Verification executes a Python script that queries the public APIs \(Crossref, OpenAlex, arXiv, DataCite\) and checks DOI resolution and retractions, outputting verified/found‑add‑doi/mismatch/etc. Negative results are paused for human approval before applying mechanical DOI fixes. Experiment orchestration splits tasks into an inner loop for fast metric trials and an outer loop preserving findings.md, ensuring hypotheses state testable mechanisms and logging of ruled‑out variations. Every skill is evaluated against curated prompt sets for trigger routing accuracy and scanned offline for prompt injection with Skill Doctor. This differs from prior approaches that relied on LLM self‑assessment or session‑wide context compaction.

**「Takeaway」** Adopt for research or technical‑writing agents that need reliable bibliographic grounding and reproducible experiment tracking; prerequisites include internet access to the cited scholarly APIs and willingness to handle human review of mismatched citations. Benefits include reduced citation errors, avoidance of duplicated failed hyperparameter tests, and lower context‑window consumption. Risks involve API latency, potential rate limits, and the absence of benchmark numbers—users should monitor cost and delays. Compatible with the six mentioned assistants, but currently lacks extensions for mechanistic interpretability modules and has no community feedback yet.

**「Open Questions」** No quantitative metrics \(precision, recall, cost, latency\) are publicly reported; no community comments or issue tracker activity were found. The library is still expanding ML evaluation and mechanistic interpretability modules, and the exact set of additional scholarly APIs to add is undecided. Whether the current workflow handles all edge cases \(e.g., newly retired DOIs, non‑standard formats\) remains untested. Users should verify external API uptime and consider adding monitoring for rate limits.

**Tags**: `#citation-verification`, `#context-engineering`, `#agent-skills`, `#experiment-loop`, `#prompt-injection`

---

## Technology News

<a id="item-tech-news-1"></a>
### [uBlock Origin patches universal XSS in element picker](https://iter.ca/post/ubo-uxss/) ⭐️ 8.0/10

uBlock Origin has patched a universal XSS vulnerability that could be triggered through website-driven use of its element picker, according to the write-up. The flaw stems from the picker interface being placed in the page&\#x27;s DOM, allowing website content to interfere with extension UI. A commenter checking affected installs says users should be on uBlock Origin 1.75.4 or uBO Lite 2026.1110.1816 and above.

hackernews · zaik · Nov 16, 02:04 · [Discussion](https://news.ycombinator.com/item?id=50513160)

**「Background」** uBlock Origin&\#x27;s element picker feature allows users to visually select page elements to create custom filter rules, but its implementation placed the picker&\#x27;s interface directly in the website&\#x27;s DOM rather than in the browser&\#x27;s privileged chrome UI. This design pattern—common among extensions that need to interact with page content—creates a security boundary issue because malicious page scripts can manipulate or observe the extension&\#x27;s DOM elements, potentially escalating to universal XSS. The vulnerability was privately reported on November 1, 2026, and patched in uBlock Origin 1.75.4 and uBO Lite 2026.1110.1816.

**「Users should update; page-DOM interfaces are the root risk」** A malicious website could trigger one-click universal XSS in the MV2 Firefox version of uBlock Origin by tricking the extension into adding arbitrary trusted filters, with a similar but less problematic issue in MV3 uBO Lite; the fix requires the legitimate picker iframe to include a secret in its initial postMessage so the background script can verify the message&\#x27;s origin. Users on affected builds should update promptly, and extension developers should treat this as evidence that placing privileged interfaces in the website DOM exposes internal identifiers and message channels to attacker-controlled pages.

**「Community discussion」** Commenters argued that placing extension interfaces in the page DOM is risky beyond this bug, citing password-manager suggestion popups as a possible way to leak which accounts a user has to a website. One commenter asked why the element-picker UI cannot live in browser chrome instead.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/gorhill/uBlock/security/advisories/GHSA-cmqw-9r2w-6wv2">Universal XSS from website-driven element picker</a></li>
<li><a href="https://github.com/gorhill/uBlock/releases">Releases · gorhill/uBlock · GitHub</a></li>
<li><a href="https://iter.ca/post/ubo-uxss/">Universal XSS in uBlock Origin from website-driven element picker</a></li>
<li><a href="https://daily.dev/posts/universal-xss-in-ublock-origin-from-website-driven-element-picker-oqxmui7ak">Universal XSS in uBlock Origin from website-driven...</a></li>

</ul>
</details>

**Tags**: `#Security`, `#Browser Extensions`, `#XSS`, `#uBlock Origin`, `#Web Security`

---

<a id="item-tech-news-2"></a>
### [Alibaba releases Qwen4-Max open-weight model with four reasoning levels and cost reductions](https://qwen.ai/blog?id=qwen4-max) ⭐️ 8.0/10

Alibaba&\#x27;s Qwen team released Qwen4-Max, an open-weight model with a sparse Mixture-of-Experts architecture, 2.4 trillion parameters, and native support for vision and 1-million-token context. The model offers four reasoning effort levels \(none, low, high, xhigh\) and ranked highly in Code Arena blind tests for frontend programming. API pricing was simultaneously reduced, with average task costs dropping from 26.58 Yuan to 11.16 Yuan \(approximately 58% lower\) and token consumption cut by nearly 50%, and the model is currently available while smaller Qwen4 series models and full weight releases are planned.

hackernews · ilreb · Nov 16, 02:14 · [Discussion](https://news.ycombinator.com/item?id=50513215)

**「Background」** Qwen4-Max succeeds Alibaba&\#x27;s Qwen3.8 Max flagship, which community members described as capable but slow — one reported roughly 30 tokens per second versus about 80 for a leading competitor, enough to hurt its standing in an agent battle system. Qwen3.8 Max already exposed a reasoning-effort setting \(commenters compared its default\), while Qwen4-Max offers four explicit levels — none, low, high, and xhigh — including a &\#x27;none&\#x27; option that lets users prioritize speed.

**「Cost Efficiency and Open‑Weight Implications」** Developers can achieve roughly 50% lower inference cost per task with Qwen4-Max, enabling more affordable large‑scale AI applications, while the announced but unconfirmed open‑weight release introduces potential licensing and compatibility considerations for downstream integration.

**「Community Reaction」** One commenter reported that Qwen 3.8&\#x27;s slow generation \(~30 tokens per second\) hindered its use in their battle system. Others highlighted Qwen4-Max&\#x27;s four reasoning levels and substantial cost cuts as significant upgrades for practical workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/qwen/qwen4-max">Qwen 4 Max - API Pricing &amp; Providers | OpenRouter</a></li>
<li><a href="https://shattered.io/qwen4-launch-alibaba-open-source-promise-doubt-470-models-2026/">Qwen 4 Launch: Alibaba Open -Source Promise in Doubt</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#AI models`, `#performance`, `#cost`, `#reasoning`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s October economic data miss forecasts](https://www.cnbc.com/2026/11/16/china-retail-sales-october-industrial-output-investment.html) ⭐️ 8.0/10

China&\#x27;s October retail sales rose 0.4% year-on-year, missing analysts&\#x27; forecast of 0.8% and slowing from 1.1% in September. Industrial output grew 4.8%, falling short of the 5.3% estimate, and fixed-asset investment contracted 8.1% year-to-date, significantly worse than the 7% decline expected, deepening worries about domestic demand.

rss · CNBC Finance · Nov 16, 03:53

**「background」** October data mark the latest miss in a 2026 slowdown where retail, industrial, and investment growth have consistently undercut analyst expectations, reflecting lingering weakness from the property-market downturn.

**「impact」** The property-market downturn has eroded household wealth for a fifth year, weighing on consumer spending despite modest retail sales growth.

**Tags**: `#China economy`, `#macroeconomic data`, `#industrial output`, `#retail sales`, `#fixed-asset investment`

---