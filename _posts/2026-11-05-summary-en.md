---
layout: default
title: "Horizon Summary: 2026-11-05 (EN)"
date: 2026-11-05
lang: en
---

> From 45 items, 23 important content pieces were selected

---

**Technology News**
1. [AMD projects Q4 sales to surpass Intel for first time](#item-tech-news-1) ⭐️ 9.0/10
2. [Go releases encoding/json/v2 major overhaul](#item-tech-news-2) ⭐️ 8.0/10
3. [Tencent Hy4](#item-tech-news-3) ⭐️ 8.0/10
4. [NKI Layer Megakernels for GLM-5.3-Flash on AWS Trainium2](#item-tech-news-4) ⭐️ 8.0/10
5. [Anthropic Open-Sources FlashProve for AI Model Identity Verification](#item-tech-news-5) ⭐️ 8.0/10
6. [Oracle cancels $7 billion AI chip lease with Tencent after US pressure](#item-tech-news-6) ⭐️ 8.0/10
7. [Moonshot AI Open-Sources Kimi K3.1 Pro Weights](#item-tech-news-7) ⭐️ 8.0/10
8. [X&\#x27;s new web version cuts slow-network first-post time to 2.7 seconds](#item-tech-news-8) ⭐️ 8.0/10
9. [OpenAI Research Eliminates Thousand Kernel Privilege Escalation Paths](#item-tech-news-9) ⭐️ 7.0/10
10. [GitHub Incident Disrupts Pull Requests, Git Operations, and Issues](#item-tech-news-10) ⭐️ 7.0/10
11. [Looped Transformers Reduce HBM Traffic? Profiling on B200](#item-tech-news-11) ⭐️ 7.0/10
12. [Hydrogen-1.0 claims lower cost and modest gains on scientific benchmarks](#item-tech-news-12) ⭐️ 7.0/10
13. [Chinese Tech Firms Release AI Agent Self-Discipline Convention](#item-tech-news-13) ⭐️ 7.0/10
14. [Claude Code Updates Game Generation Rules](#item-tech-news-14) ⭐️ 7.0/10
15. [Huawei tells customers to source HBM3E memory for Ascend 960DT](#item-tech-news-15) ⭐️ 7.0/10
16. [Cloudflare Launches Personal AI Agent Traffic Analysis and Tiered Controls](#item-tech-news-16) ⭐️ 7.0/10
17. [macOS 27.3 Beta Adds Quick Look Markdown Preview](#item-tech-news-17) ⭐️ 7.0/10
18. [Bluetooth HDT Adopted, Raises LE Rate to 7.5 Mbps](#item-tech-news-18) ⭐️ 7.0/10
19. [Apple to scan iCloud public links for harmful content in iOS 27.3 and later](#item-tech-news-19) ⭐️ 7.0/10

**Financial News**
1. [Stocks Make Biggest Moves After Hours on Earnings and Guidance](#item-finance-news-1) ⭐️ 8.0/10
2. [Premarket Stock Moves: Election Results and Earnings Drive Moves in Trump Media, Tesla, and More](#item-finance-news-2) ⭐️ 8.0/10
3. [Democrats win U.S. House and Senate in 2026 midterms, item reports; Trump congratulates them](#item-finance-news-3) ⭐️ 8.0/10
4. [Treasury yields and oil prices fall after Democratic midterm victories](#item-finance-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [AMD projects Q4 sales to surpass Intel for first time](https://www.tomshardware.com/pc-components/cpus/amd-expects-to-outsell-intel-in-q4-for-the-first-time-in-history-usd17b-guidance-would-exceed-intels-projections) ⭐️ 9.0/10

AMD says it expects to outsell Intel in Q4 for the first time, based on a $17 billion sales guidance that would exceed Intel’s projections. The forecast marks a shift in the CPU/GPU market, though it remains a forward‑looking statement rather than realized sales. AMD attributes the growth partly to strong demand for its Instinct accelerators, while Intel’s Arc line has seen negligible sales.

hackernews · rbanffy · Nov 4, 15:38 · [Discussion](https://news.ycombinator.com/item?id=50367125)

**「AMD&\#x27;s data‑center growth drives Q4 revenue surge」** AMD&\#x27;s Q4 revenue guidance of about $17 billion reflects a sharp expansion of its data‑center business, where Instinct accelerators and Epyc server CPUs have doubled sales, offsetting a decline in gaming; Intel’s Q4 guidance of $15‑$16 billion is lower, marking the first time AMD is projected to outsell Intel. \(Source: tool-1-1, tool-1-2, tool-1-3\)

**「Impact」** If realized, AMD’s $17 B Q4 guidance will likely prompt organizations and distributors to adjust procurement plans, favoring AMD CPUs and accelerators for the holiday season and reshaping near‑term supply‑chain decisions.

**「Community discussion」** dlcarrier notes that AMD’s high Instinct sales, contrasted with Intel’s lack of sales for its Arc accelerators, may be the primary driver of AMD’s projected Q4 lead.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/pc-components/cpus/amd-expects-to-outsell-intel-in-q4-for-the-first-time-in-history-usd17b-guidance-would-exceed-intels-projections">AMD expects to outsell Intel in Q4 for the first time in ...</a></li>
<li><a href="https://wccftech.com/amd-is-set-to-out-earn-intel-for-the-first-time-in-its-history-guiding-to-17-billion-in-q4-revenue-against-intels-15-5-billion-midpoint-projection/">AMD Is Set To Out-Earn Intel For The First Time In Its ...</a></li>
<li><a href="https://arstechnica.com/gadgets/2026/11/amds-record-quarter-data-center-business-doubles-while-gaming-craters/">AMD’s record quarter: Data center business doubles, while ...</a></li>

</ul>
</details>

**Tags**: `#hardware`, `#market-competition`, `#AMD`, `#Intel`

---

<a id="item-tech-news-2"></a>
### [Go releases encoding/json/v2 major overhaul](https://go.dev/blog/jsonv2) ⭐️ 8.0/10

Go has released encoding/json/v2, a new major version of its standard library JSON package that adds streaming API support, deterministic output, and an options-based ergonomics overhaul. The release addresses long-standing limitations of the original encoding/json, such as the lack of streaming parsing and non-deterministic marshaling, and provides a compatibility package for migration. The change affects virtually all Go backend and cloud service development, as the package is a core standard library dependency.

hackernews · olexsmir · Nov 4, 17:52 · [Discussion](https://news.ycombinator.com/item?id=50369106)

**「Go&\#x27;s encoding/json/v2 standard library update」** Go 1.27 ships \`encoding/json/v2\`, a major overhaul of the standard library JSON package that adds streaming, deterministic output, improved error handling, and an options pattern. The v2 API addresses long-standing limitations of the original \`encoding/json\` package, including non-deterministic key ordering and awkward error messages. The \`GOEXPERIMENT=jsonv2\` flag enables it for existing projects, with migration guidance available from ImportStatic and Stackademic.

**「Migration impact for Go developers」** Go developers using the standard encoding/json package must migrate to the v2 API to access streaming and deterministic output features; the release includes a compatibility package but requires code adjustments to marshaling and unmarshaling patterns. Some teams have adopted third-party parsers like jsontext for specific error-handling needs.

**「Community reaction to JSON v2」** Some users welcome the new encoding/json/v2 API for its streaming and deterministic output, but note that migrating from MarshalIndent is complicated and non-obvious. Others recommend third-party packages like jsontext for precise error handling and performance.

<details><summary>References</summary>
<ul>
<li><a href="https://importstatic.com/go/go-json-v2-migration">Go JSON v 2 Migration: What Breaks in Go 1.27 | ImportStatic</a></li>
<li><a href="https://blog.stackademic.com/golangs-new-proposal-for-the-encoding-or-json-or-v2-package-code-thursday-6e1498684739">Go encoding / json / v 2 | Stackademic</a></li>
<li><a href="https://tonybai.com/2025/05/15/go-json-v2/">手把手带你玩转GOEXPERIMENT=jsonv2： Go 下一代 JSON ... | Tony Bai</a></li>

</ul>
</details>

**Tags**: `#go`, `#standard-library`, `#json`, `#api-design`, `#backend`

---

<a id="item-tech-news-3"></a>
### [Tencent Hy4](https://hy.tencent.ai/research/hy4) ⭐️ 8.0/10

Tencent releases Hy4 and open‑sources two foundation models \(HyCell, HyPDE\) with game‑engine support, marking a significant open‑source AI contribution.

hackernews · Philpax · Nov 4, 14:11 · [Discussion](https://news.ycombinator.com/item?id=50365780)

**Tags**: `#open-source AI`, `#foundation models`, `#single-cell representation`, `#physical field modeling`, `#game development`

---

<a id="item-tech-news-4"></a>
### [NKI Layer Megakernels for GLM-5.3-Flash on AWS Trainium2](https://www.reddit.com/r/MachineLearning/comments/1xo0yuq/p_nki_layer_megakernels_for_glm53flash_on_aws/) ⭐️ 8.0/10

RunAnywhere open-sourced an inference engine that serves GLM-5.3-Flash \(320B MoE, 1M-token context\) on a single AWS Trainium2 trn2.48xlarge instance. The team rewrote each layer half as a single NKI megakernel following three rules: keep the working set on the 28 MiB SBUF per NeuronCore, split the weight stream across both physical cores of a logical core, and move collectives inside the kernel to overlap with independent work. On a batch-8 decode step, the rewrite cut latency from 32.2 ms to 24.2 ms, with the fused sparse-attention layer saving 3.2 ms and the KDA plus MoE kernels saving another 3.2 ms. Of the remaining 24.2 ms, only 6.1 ms is the memory floor; the rest is engine busy time, waits, and exposed collectives.

reddit · r/MachineLearning · /u/WildCard727 · Nov 4, 21:47

**「Background」** GLM-5.3-Flash is a 320B-parameter Mixture-of-Experts model with a 1M-token context window. AWS Trainium2 is an AI accelerator where each logical core has two physical NeuronCores, each with 28 MiB of on-chip SBUF memory, and the hardware requires careful management of HBM bandwidth and collective operations. In an early build, the actual math in a linear attention layer was only 2% of the attention half&\#x27;s time, with the rest consumed by pre-projections, XLA glue, transposes, and other overhead.

**「Impact」** The open-sourced implementation achieves up to 28.9 agent requests per minute on a single trn2.48xlarge box, with median decode at 35.9 tokens/s at 16 agents on SemiAnalysis&\#x27;s AgentX benchmark. Because no stock-AWS baseline supports GLM-5.3-Flash \(vLLM&\#x27;s Neuron plugin registers no GLM model and NxD Inference is in maintenance mode\), these numbers represent the first publicly available Trainium2 throughput for this model. The code is released at github.com/RunanywhereAI/trnrt with commands to rerun every reported number.

**Tags**: `#hardware-optimization`, `#inference-engine`, `#aws-trainium`, `#nki`, `#large-language-models`

---

<a id="item-tech-news-5"></a>
### [Anthropic Open-Sources FlashProve for AI Model Identity Verification](https://assets.claude.com/8e1d181a83015078581c92d896757041713f0160.pdf) ⭐️ 8.0/10

Anthropic has open-sourced FlashProve, a cryptographic system that lets users verify whether a specific AI model generated a given output. The system works by having model publishers release cryptographic fingerprints that can be matched against outputs, without revealing model weights, and verification runs locally on the user&\#x27;s device. Anthropic has published the technical specification and code on GitHub, but the research remains in progress with no deployment timeline announced.

telegram · zaihuapd · Nov 4, 10:16

**「Background」** Model provenance and supply-chain trust have become practical concerns as AI models are deployed through third-party APIs and platforms where substitution or modification can occur without user awareness. Cryptographic fingerprinting offers a way to bind outputs to a specific model release without exposing proprietary weights, complementing existing approaches like model cards and transparency reports.

**「Impact」** Developers and organizations evaluating AI vendors can now experiment with a local, weight-private verification method to detect model substitution in their supply chain, though production use awaits further research and a deployment decision from Anthropic.

**Tags**: `#AI security`, `#model verification`, `#cryptography`, `#Anthropic`, `#open source`

---

<a id="item-tech-news-6"></a>
### [Oracle cancels $7 billion AI chip lease with Tencent after US pressure](https://www.tradingview.com/news/seekingalpha:e51e68f4d094b:0-oracle-cancels-7b-ai-chip-lease-with-tencent-amid-us-concerns-ft/) ⭐️ 8.0/10

Oracle has cancelled a roughly $7 billion, five-year agreement under which Tencent would have leased about 100,000 advanced AI chips through Oracle&\#x27;s Southeast Asian data centers. The cancellation followed concerns raised by US officials and pressure from the Trump administration, according to the report. Tencent had signed the lease this year to obtain chips unavailable in China, with an initial down payment of about 30 percent. The report describes the deal as cancelled and does not independently verify the chips&\#x27; specifications or delivery status.

telegram · zaihuapd · Nov 4, 11:01

**「US export controls enable chip leasing」** US export control policies that restrict the transfer of advanced AI chips to Chinese entities created a market for leasing such chips through third‑party data centers, as seen in Oracle’s five‑year, $7 billion lease with Tencent. Earlier agreements between chipmakers and cloud providers demonstrated that leasing was a viable workaround to bypass direct sales bans.

**「Impact」** Tencent loses access to roughly 100,000 advanced AI chips it intended to rent outside China, so it must find alternative sources or scale back that capacity plan. Oracle also gives up the roughly $7 billion five-year lease.

**Tags**: `#AI chips`, `#Oracle`, `#Tencent`, `#US export controls`, `#cloud infrastructure`

---

<a id="item-tech-news-7"></a>
### [Moonshot AI Open-Sources Kimi K3.1 Pro Weights](http://platform.kimi.ai/) ⭐️ 8.0/10

Moonshot AI \(月之暗面\) has released open weights for Kimi K3.1 Pro on Hugging Face, a native multimodal agent model with 2.8 trillion total parameters, 104 billion activated parameters, and approximately 1 million token context length. This is the first model in the K3.1 series. The company also opened an official API at platform.kimi.ai under the name kimi-k3.1-pro, which is compatible with OpenAI and Anthropic interfaces. The weights are distributed in MXFP4 quantized format.

telegram · zaihuapd · Nov 4, 15:47

**「Kimi K3.1 Pro Background」** For context, an open-weight release means the model parameters can be accessed and potentially used beyond a hosted API. Moonshot AI&\#x27;s Kimi K3.1 Pro is described as a native multimodal agent model with about 2.8 trillion total parameters, 104 billion activation parameters, and roughly a one-million-token context, and it is the first model in the K3.1 series. The source adds that the weights were published in MXFP4 quantization and that the accompanying API is compatible with OpenAI and Anthropic interfaces.

**「Kimi K3.1 Pro API and Benchmark Release」** Kimi K3.1 Pro is available today via the Kimi API and platforms \(Kimi.ai, Kimi Work, Kimi Code\), and benchmark results across 14 evaluations are now public, providing developers with data to assess the model for coding, science, and knowledge-work tasks. The internal benchmark, however, emphasizes expert-curated vulnerability discovery and exploitation tasks, which may limit direct relevance for general developers.

**「Community Discussion」** Commenters note the model&\#x27;s high hardware requirements, with one estimating an 8x B300 node is needed to run it locally. Some dispute the &quot;open-weight&quot; label, while others debate whether the model is &quot;benchmaxxed&quot; \(over-optimized for benchmarks\) compared to competitors like DeepSeek V4.1 Flash and Opus 5.5. Third-party inference providers such as OpenRouter, Together, and Modal are already hosting the model, with reports that Together and Modal offer higher throughput than Moonshot&\#x27;s own endpoint at the same price.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.ai/blog/kimi-k3-1-pro">Kimi K 3 . 1 Pro Tech Blog: Advancing Open Intelligence</a></li>
<li><a href="https://huggingface.co/moonshotai/Kimi-K3.1-Pro">moonshotai/ Kimi - K 3 . 1 - Pro · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#Kimi K3.1 Pro`, `#open-source weights`, `#multimodal agent`, `#large-scale language model`

---

<a id="item-tech-news-8"></a>
### [X&\#x27;s new web version cuts slow-network first-post time to 2.7 seconds](http://x.com/) ⭐️ 8.0/10

X&\#x27;s new x.com web version now serves logged-out users and shortens the time to show the first post on slow networks from over 22 seconds to 2.7 seconds, according to X. The new build uses one server for visitors, search crawlers, and link previews, and streams HTML so content appears earlier. X says the comparison comes from lab tests and that real-world performance varies by device and network. Logged-in users are being moved to the new version country by country; the old version keeps running during the migration and will be retired afterward.

telegram · zaihuapd · Nov 4, 23:32

**「Background」** Time to first post measures how long a page takes to display the first item of content; on slow networks this is often limited by round trips and client-side JavaScript. Streaming HTML lets a server send usable markup incrementally instead of waiting for a full client-side render, which can make content visible sooner.

**「Impact」** Logged-out visitors and search crawlers on slow connections should see the first post far sooner in lab conditions, though actual times will depend on device and network. During the staged migration, logged-in users may still receive the old version, and X can adjust traffic with edge routing and feature flags before shutting the old version down.

**Tags**: `#Web Performance`, `#Software Engineering`, `#Networking`, `#Social Media`

---

<a id="item-tech-news-9"></a>
### [OpenAI Research Eliminates Thousand Kernel Privilege Escalation Paths](https://openai.com/index/a-thousand-fewer-paths-to-root/) ⭐️ 7.0/10

OpenAI&\#x27;s security research team has identified and eliminated approximately a thousand privilege escalation paths in the Linux kernel, significantly reducing the attack surface for local root exploits. The work, published on November 4, 2026, details systematic vulnerability discovery and mitigation, with the team noting they are hiring for cyber roles. The research addresses long-standing concerns about kernel complexity and the prevalence of local escalation vulnerabilities.

hackernews · dangelosaurus · Nov 4, 23:33 · [Discussion](https://news.ycombinator.com/item?id=50372929)

**「Local privilege escalation and kernel attack surface」** Local privilege-escalation vulnerabilities allow an attacker with existing user access on a system to gain higher privileges, potentially reaching root or full kernel control. Each such flaw can serve as a “path to root” from an unprivileged account to complete system compromise. OpenAI reported that its autonomous pipeline found, validated, and generated patches for 948 local privilege-escalation vulnerabilities in the Linux kernel.

**「Impact」** This reduction in privilege escalation paths directly benefits system administrators, cloud providers, and end-users by lowering the risk of local root compromise on Linux systems. Developers and security teams should review the findings to understand the mitigated vulnerability classes and apply relevant kernel updates.

**「Community Discussion」** Commenters questioned how the kernel accumulated so many privilege escalation vulnerabilities and whether complexity or security model flaws are to blame. One user expressed shock at the count of 948 vulnerabilities, while another highlighted mitigating factors that prevent widespread exploitation. The author confirmed the work is from their team and invited questions.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/a-thousand-fewer-paths-to-root/">A thousand fewer paths to root | OpenAI</a></li>

</ul>
</details>

**Tags**: `#kernel security`, `#privilege escalation`, `#software engineering`, `#cybersecurity`

---

<a id="item-tech-news-10"></a>
### [GitHub Incident Disrupts Pull Requests, Git Operations, and Issues](https://www.githubstatus.com/incidents/smtdswd1h2w4) ⭐️ 7.0/10

GitHub recorded an incident on November 4, 2026 that disrupted pull requests, Git operations, and issues for users of the platform. Some users reported that the status page did not immediately reflect the disruption, forcing them to investigate whether the problem was in GitHub&\#x27;s services or their own systems. A commenter linked the timing to a scheduled brownout removing ssh-rsa SHA-1 signatures and the diffie-hellman-group-exchange-sha256 key exchange, but GitHub has not confirmed this as the cause.

hackernews · kevcampb · Nov 4, 10:00 · [Discussion](https://news.ycombinator.com/item?id=50363378)

**「Background」** On November 4, 2026, GitHub experienced a two‑hour outage that impaired pull requests and core Git operations, an incident later linked to a scheduled brownout for deprecated SSH key types \(ssh‑rsa signatures and the diffie‑hellman‑group‑exchange‑sha256 key exchange\). The outage highlighted reliability concerns with GitHub’s status page, which initially failed to reflect the disruption. This context follows a prior two‑hour incident reported on 2026‑11‑04 that similarly affected pull‑request functionality.

**「Impact」** Teams lost productive time troubleshooting because the status page did not match observed symptoms, requiring them to independently verify whether GitHub or their own pipelines were at fault.

**「Community discussion」** gophigure argued that the status page&\#x27;s failure to show the outage created unnecessary toil, while a-squirrel-comm suggested the incident may relate to a scheduled brownout removing ssh-rsa SHA-1 signatures and diffie-hellman-group-exchange-sha256 key exchange. eknkc described deployments tied to GitHub Actions as a liability and asked about alternatives for private repositories, though no alternative was recommended.

<details><summary>References</summary>
<ul>
<li><a href="https://dzen.ru/a/ausjCz4ouU8pqlrg">GitHub закрыл двухчасовой инцидент, затронувший пять... | Дзен</a></li>

</ul>
</details>

**Tags**: `#github`, `#gitops`, `#ssh`, `#status-page`

---

<a id="item-tech-news-11"></a>
### [Looped Transformers Reduce HBM Traffic? Profiling on B200](https://www.reddit.com/r/MachineLearning/comments/1xnskvt/do_looped_transformers_save_hbm_traffic_profiling/) ⭐️ 7.0/10

Researchers profiling looped transformers \(Huginn\) on an NVIDIA B200 showed that weight sharing reduces storage but does not eliminate HBM traffic. A chain of eight matmuls with a shared 72 MiB weight ran 24 % faster and read negligible HBM, while larger weights or full cores showed no speedup and eight‑fold higher memory traffic.

reddit · r/MachineLearning · /u/2dayyy6 · Nov 4, 16:26

**「Background」** Looped transformers reuse the same weight tensors across iterations, a design intended to lower parameter count and memory footprint.

**「Impact」** Developers optimizing GPU memory must keep weights resident on‑chip across iterations, otherwise memory bandwidth remains unchanged and the performance benefit of weight sharing disappears on B200.

**Tags**: `#looped-transformers`, `#GPU-profiling`, `#HBM`, `#ML-systems`, `#Huginn`

---

<a id="item-tech-news-12"></a>
### [Hydrogen-1.0 claims lower cost and modest gains on scientific benchmarks](https://www.reddit.com/r/MachineLearning/comments/1xnjhdd/hydrogen10_openweight_scientific_model_beats_gpt6/) ⭐️ 7.0/10

Deep Principle released Hydrogen-1.0, an open‑weight model post‑trained from GLM‑5.3 for chemistry, materials science, and life sciences. In the team’s self‑reported evaluations, Hydrogen‑1.0 achieved a 38.3% pass rate on FrontierScience Research versus 33.3% for GPT‑6 Astra \(max thinking\) and an estimated output cost of $0.25 per problem versus $0.88 for Astra, representing roughly a 72% reduction under their evaluation setup. The model also outperformed Astra on internal scientific computing \(+5.13 points\) and reaction prediction \(+4.76 points\) but lagged on NMR structure elucidation \(−3.33 points\). These results are limited to the team’s internal benchmarks and have not been independently verified.

reddit · r/MachineLearning · /u/AKAMA199 · Nov 4, 09:00

**「Base model context」** GLM-5.3 is Z.ai&\#x27;s flagship open-weight model with 753B parameters, noted for strong coding and long-horizon agentic task capabilities, which serves as the base for Hydrogen-1.0&\#x27;s post-training. The model improves upon GLM-5.2 with a 50% gain in coding performance and requires reasoning\_effort configuration for complex tasks.

**「Impact」** Developers and researchers considering open‑weight scientific LLMs should treat Hydrogen‑1.0’s claimed cost savings and modest performance gains as preliminary, verifying the results on their own data before relying on the model for production or critical research tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/zai-org/GLM-5.3">Text Generation model with 753B parameters. Download, explore files...</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.3">GLM - 5 . 3 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>
<li><a href="https://ollama.com/library/glm-5.3">glm - 5 . 3</a></li>

</ul>
</details>

**Tags**: `#open-source AI`, `#scientific machine learning`, `#LLM evaluation`, `#model cost`

---

<a id="item-tech-news-13"></a>
### [Chinese Tech Firms Release AI Agent Self-Discipline Convention](https://www.cls.cn/detail/2524879) ⭐️ 7.0/10

On November 4, twenty Chinese technology units, including CAICT, Huawei, Alibaba, Tencent, and Xiaomi, jointly released the AI Agent Development Self-Discipline Convention. The release addressed building AI agent interconnection infrastructure and improving registration and resolution, capability description and discovery, protocol compatibility and mutual recognition, and cross-domain discovery and connection costs. It also proposed low-threshold agent development and deployment tools and cooperation on agents for real-world work scenarios that could be embedded into existing production systems and business flows.

telegram · zaihuapd · Nov 4, 08:45

**「AI Agent Self-Discipline Convention」** AI agent interoperability previously lacked a shared implementation foundation, so integrating agents into production systems often involved fragmented protocols and costly discovery and connection work. The November 4 joint release of the AI Agent Development Self-Discipline Convention by about 20 Chinese technology units, including CAICT, Huawei, Alibaba, Tencent, and Xiaomi, offered an early attempt to address that prerequisite through proposals for interconnection infrastructure, registration and parsing, capability description and discovery, protocol compatibility and mutual recognition, and low-threshold development and deployment tools.

**「Potential Integration Impact」** The convention could give developers and organizations a shared starting point for agent interoperability and capability description, potentially easing later integration of AI agents into production systems. Its practical effect will depend on implementation, adoption, and how the proposed technical and standards work are used.

**Tags**: `#AI Agents`, `#Industry Standards`, `#AI Infrastructure`, `#China Tech`, `#Software Engineering`

---

<a id="item-tech-news-14"></a>
### [Claude Code Updates Game Generation Rules](https://x.com/addyosmani/status/2117848568535106001) ⭐️ 7.0/10

For Claude Code users and developers, Claude Code 2.1.317 revised its game-generation restriction behavior to be more nuanced. The earlier Opus 5.5 prompt rule was intended to avoid replicating existing games but could also block users who mentioned a game only to describe the gameplay they wanted. The update now builds an original game of the type identified by that description and offers alternatives when the request is to copy an existing game.

telegram · zaihuapd · Nov 4, 13:19

**「Earlier Game Guard」** The update responds to an earlier game-generation guard in Claude Code that was added to prevent replication of existing games. That guard was broader than intended because a game name used descriptively could trigger a refusal. The 2.1.317 release adjusts the rule into a more conditional approach.

**「User Impact」** For developers using Claude Code to prototype games, the update may reduce false refusals when they use a game name to describe a desired genre or play style. It may also change how the assistant handles requests to copy a game by proposing similar alternatives instead of blocking them. The team said it will continue improving the behavior and welcomes feedback about incorrectly rejected projects.

**Tags**: `#game generation`, `#AI`, `#software engineering`, `#tool update`

---

<a id="item-tech-news-15"></a>
### [Huawei tells customers to source HBM3E memory for Ascend 960DT](https://thenextweb.com/news/huawei-hbm-smuggling-samsung-sk-hynix-ascend-960dt) ⭐️ 7.0/10

Huawei has told certain customers that the forthcoming Ascend 960DT flagship AI processor will require them to obtain HBM3E memory independently. The directive stems from insufficient HBM production capacity among Chinese manufacturers, prompting customers to source the memory from Samsung or SK Hynix. This requirement has spurred a gray‑market smuggling chain in which modules are shipped via Hong Kong and carried into mainland China, with prices rising from a few hundred dollars a year ago to roughly $4,000 per unit.

telegram · zaihuapd · Nov 4, 14:52

**「HBM Supply Context」** HBM \(High Bandwidth Memory\) is a critical, high-performance memory type tightly coupled with AI accelerators to meet their data throughput demands. China&\#x27;s domestic HBM production capacity has remained limited, forcing AI chip designers like Huawei to rely on foreign suppliers such as Samsung and SK Hynix for memory integration. This supply constraint underlies Huawei&\#x27;s instruction to Ascend 960DT customers to secure HBM independently.

**「HBM3E Cost Burden for Ascend 960DT」** Ascend 960DT customers are required to self-procure HBM3E memory due to China&\#x27;s domestic supply shortage, resulting in black-market prices of approximately $4,000 per unit and total memory costs reaching $32,000 per chip. This forces buyers into cross-border smuggling routes, exposing them to legal compliance risks and significantly inflating total cost of ownership.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ic.work/article/huawei-ascend-960dt-buyers-source-black-market-hbm3e-memory">华为 Ascend 960DT 买芯片竟要客户自备 HBM3E 内存，单卡黑市成本飙至...</a></li>
<li><a href="https://www.sohu.com/a/1020489321_120426565">HBM3E 半年暴涨 300%：AI 算力 “存力危机” 全面爆发_供需_价格_垄断</a></li>

</ul>
</details>

**Tags**: `#AI芯片供应链`, `#华为昇腾`, `#HBM内存`, `#灰色市场`, `#芯片走私`

---

<a id="item-tech-news-16"></a>
### [Cloudflare Launches Personal AI Agent Traffic Analysis and Tiered Controls](https://blog.cloudflare.com/personal-agents-visibility-control/) ⭐️ 7.0/10

Cloudflare has introduced per-agent traffic analysis and tiered access control for personal AI agents, enabling teams to inspect request metrics and apply granular allow/block rules. The new &quot;Personal Assistant&quot; category and per-agent statistics \(request counts, paths, status codes\) provide operational visibility into agent-driven traffic patterns. This feature supports software engineering teams in managing resource consumption by personal AI agents.

telegram · zaihuapd · Nov 4, 15:42

**「Previous robot analysis and top statistics foundation」** Cloudflare previously offered basic robot analysis and top statistics, but the recent update adds a dedicated &quot;Personal Assistant&quot; category and per-agent metrics. The new tiered policies allow teams to set agents to allow, block on ad pages, or block entirely, with user attribution enabled through Account Abuse Protection.

**「Enhanced visibility and control for AI agent teams」** Engineering teams can now apply granular access policies to personal AI agents, inspecting per-agent request counts, paths, and status codes while enforcing tiered controls \(allow, block on ad pages, or block entirely\) to better manage resource consumption.

**「No community feedback provided」** No community comments were available for this announcement.

**Tags**: `#cloudflare`, `#ai-agents`, `#traffic-analysis`, `#access-control`

---

<a id="item-tech-news-17"></a>
### [macOS 27.3 Beta Adds Quick Look Markdown Preview](https://www.macrumors.com/2026/11/04/macos-27-3-makes-markdown-files-easier-to-read/) ⭐️ 7.0/10

The first developer beta of macOS 27.3 adds native Markdown rendering to Quick Look, allowing users to preview .md files with titles, bold text, lists, and links directly in the Finder by selecting a file and pressing the space bar. This feature eliminates the need for a separate editor or Quick Look extension to view Markdown formatting. The change is part of Apple’s expanding Markdown support across its platforms, following similar additions in iOS 26 and iOS 27.

telegram · zaihuapd · Nov 4, 16:36

**「Background」** Quick Look is macOS’s built‑in preview system that shows file contents without opening an application, and Markdown is a lightweight markup language used for formatted text. Apple has been incrementally adding Markdown capabilities to its operating systems, such as import/export in iOS 26’s Notes app and copy‑paste support in iOS 27. The new Quick Look Markdown preview builds on this trend by integrating rendering directly into the file‑browser interface.

**「Impact」** Developers and power users can now inspect the visual appearance of Markdown files instantly in the Finder, streamlining workflows that previously required an external editor. The feature is only available in the macOS 27.3 developer beta, so public users will need to wait for a future stable release to benefit.

**Tags**: `#macOS`, `#Markdown`, `#Apple`, `#Software Engineering`

---

<a id="item-tech-news-18"></a>
### [Bluetooth HDT Adopted, Raises LE Rate to 7.5 Mbps](https://www.bluetooth.com/press/bluetooth-high-data-throughput-opens-a-new-chapter-in-wireless-performance/) ⭐️ 7.0/10

The Bluetooth SIG adopted Bluetooth High Data Throughput, raising the maximum Bluetooth LE rate from 2 Mbps to 7.5 Mbps, a nearly fourfold increase. The adoption was intended to improve capacity, efficiency, and reliability and was seen as a step toward lossless wireless audio. The first standardized lossless or high-resolution audio applications using HDT were expected around 2027.

telegram · zaihuapd · Nov 5, 01:39

**「Background」** Bluetooth Low Energy previously topped out at 2 Mbps under the LE 2M PHY introduced in Bluetooth 5.0. The new High Data Throughput \(HDT\) feature is an optional part of the Bluetooth Core 7.0 specification and raises that ceiling to 7.5 Mbps while maintaining backward compatibility with existing devices.

**「Wireless audio impact」** For wireless audio and low-energy developers, the concrete near-term consequence is limited because the first standardized lossless or high-resolution audio applications were expected around 2027, while device support for the optional HDT feature in Bluetooth Core 7.0 remained a key deployment requirement.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bluetooth.com/press/bluetooth-high-data-throughput-opens-a-new-chapter-in-wireless-performance/">Bluetooth® High Data Throughput opens a new chapter in ...</a></li>

</ul>
</details>

**Tags**: `#Bluetooth`, `#BluetoothLowEnergy`, `#WirelessAudio`, `#LosslessAudio`, `#TechStandards`

---

<a id="item-tech-news-19"></a>
### [Apple to scan iCloud public links for harmful content in iOS 27.3 and later](https://9to5mac.com/2026/11/04/with-ios-27-3-apple-will-start-checking-icloud-public-links-for-harmful-content/) ⭐️ 7.0/10

Starting with iOS 27.3, iPadOS 27.3, macOS 27.3, and visionOS 27.3, Apple will scan iCloud content shared with &\#x27;Anyone with the link&\#x27; for harmful content. Content shared only with specific recipients is excluded from this check. If content is deemed harmful, Apple may move, refuse, modify, or delete it, and may limit or disable the user&\#x27;s account, potentially involving law enforcement.

telegram · zaihuapd · Nov 5, 02:11

**「iCloud Public Link Content Check」** Apple will start checking iCloud public links that are shared with “anyone with the link” for harmful content, beginning with iOS 27.3 and rolling out to iPadOS, macOS, and visionOS. If the content is flagged as harmful, Apple may move, reject, modify, or delete it and may restrict the uploader’s account.

**「Impact」** iCloud public link sharers risk having their content moved, modified, or deleted, and their accounts limited or disabled if Apple classifies the content as harmful, with potential law enforcement referral.

<details><summary>References</summary>
<ul>
<li><a href="https://www.macrumors.com/">MacRumors: Apple News and Rumors</a></li>

</ul>
</details>

**Tags**: `#iOS`, `#Security`, `#Privacy`, `#Apple`, `#Cloud`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Stocks Make Biggest Moves After Hours on Earnings and Guidance](https://www.cnbc.com/2026/11/04/stocks-making-the-biggest-moves-after-hours-cohr-app-expe-more.html) ⭐️ 8.0/10

After-hours trading saw sharp stock moves tied to mixed earnings and guidance, led by Qualcomm’s nearly 6% slide despite a slight earnings beat, as it forecast adjusted earnings of $2.15 to $2.35 per share for the current quarter versus the $2.26 per share analysts expected.

rss · CNBC Finance · Nov 4, 22:04

**「Background」** The after-hours swings follow earnings reports and guidance updates from companies such as Qualcomm, AppLovin, and Zillow.

**Tags**: `#After-hours trading`, `#Earnings reports`, `#Stock price movements`, `#Technology stocks`, `#Consumer discretionary`

---

<a id="item-finance-news-2"></a>
### [Premarket Stock Moves: Election Results and Earnings Drive Moves in Trump Media, Tesla, and More](https://www.cnbc.com/2026/11/04/stocks-making-the-biggest-moves-premarket-djt-tsla-crwv-nvo.html) ⭐️ 8.0/10

A CNBC premarket roundup highlights notable stock moves driven by election results, data center concerns, and earnings beats. Trump Media shares fell 11% after Democrats won control of Congress, while Novo Nordisk gained over 6% after reporting earnings of 5.79 Danish kroner per share, beating the 5.10 kroner estimate, and raising its fiscal 2026 outlook.

rss · CNBC Finance · Nov 4, 13:32

**「Background」** Democrats taking control of Congress in the U.S. midterm elections adds a check on the president&\#x27;s policies and creates hurdles for data center expansion.

**Tags**: `#premarket`, `#earnings`, `#election impact`, `#data center`, `#healthcare`

---

<a id="item-finance-news-3"></a>
### [Democrats win U.S. House and Senate in 2026 midterms, item reports; Trump congratulates them](https://apnews.com/live/midterm-election-2026) ⭐️ 8.0/10

A Telegram item citing AP and CBS reports that Democrats won the U.S. House and Senate in the 2026 midterms, taking at least seven Senate seats and flipping House districts where Trump led by up to 18 percentage points in 2024. Trump congratulated Democrats and said he would work with them for the country&\#x27;s benefit.

telegram · zaihuapd · Nov 4, 08:00

**「Background」** Midterm elections determine control of Congress, which writes federal laws, confirms presidential appointments, and oversees the executive branch.

---

<a id="item-finance-news-4"></a>
### [Treasury yields and oil prices fall after Democratic midterm victories](https://www.cnbc.com/2026/11/03/treasury-yields-fall-as-democrats-win-big-in-us-midterm-elections.html) ⭐️ 7.0/10

10-year Treasury yields fell more than 6 basis points to 4.884% on Wednesday as Democrats secured majorities in both the House and Senate following U.S. midterm elections. JPMorgan traders said the outcome reduces the likelihood of deficit spending, potentially improving the fiscal outlook.

rss · CNBC Finance · Nov 4, 21:18

**「Background」** The source reported that Democrats won majorities in both the U.S. House and Senate in the November 2026 midterm elections, a result that could make it harder for the White House to push spending legislation through Congress.

**「Impact」** The Democratic victory may limit deficit spending, improving the fiscal outlook and supporting Treasury yields, while oil prices fell on concerns about Iran‑related supply risks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.fxstreet.com/news/breaking-democrats-win-control-of-senate-202611040532">Breaking: Democrats win both House and the Senate</a></li>
<li><a href="https://www.fundssociety.com/en/news/markets/the-blue-wave-leaves-a-divided-government-implications-and-market-reactions/">Divided Government Market Impact US Midterms</a></li>
<li><a href="https://en.wikipedia.org/wiki/Economic_impact_of_the_2026_Iran_war">Economic impact of the 2026 Iran war - Wikipedia</a></li>
<li><a href="https://www.morganstanley.com/insights/articles/iran-war-oil-inflation-stock-market-2026">Iran Conflict: Oil Price Impacts and Inflation | Morgan Stanley</a></li>
<li><a href="https://taceconomics.com/en/2026-iranian-oil-shock-global-stagflation/">2026 Iranian Oil Shock: Inflation, Growth and Global ...</a></li>

</ul>
</details>

**Tags**: `#U.S. midterm elections`, `#Treasury yields`, `#Oil prices`, `#Fiscal policy`, `#Market reaction`

---