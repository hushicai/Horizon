---
layout: default
title: "Horizon Summary: 2026-10-13 (EN)"
date: 2026-10-13
lang: en
---

> From 52 items, 18 important content pieces were selected

---

**Technology News**
1. [MiniCPM-V 4.7 35B-A3B: First open-source MoE model with on-device inference](#item-tech-news-1) ⭐️ 9.0/10
2. [Looped Diffusion Transformer: the same blocks run several times inside each denoising step, and loop depth can be changed at sampling time \[R\]](#item-tech-news-2) ⭐️ 8.5/10
3. [Hello Python 3.15, goodbye 3.10, and now I can use 3.11](#item-tech-news-3) ⭐️ 8.0/10
4. [U-Space: Uncovering When and Why Uncertainty Arises in Language Models \[R\]\[D\]](#item-tech-news-4) ⭐️ 8.0/10
5. [learnc: Auto-tunes C constants for 9.1% JPEG gain, +4.9 F1 on WebRTC VAD](#item-tech-news-5) ⭐️ 8.0/10
6. [Qwen released QwenGyre - RL framework for training AI agents on extremely long complex tasks](#item-tech-news-6) ⭐️ 8.0/10
7. [Boole-1.7B: 1‑bit Qwen3‑1.7B model released, outperforms prior 1‑bit models](#item-tech-news-7) ⭐️ 8.0/10
8. [OpenAI Codex CLI Installs Persistent Background Daemon by Default](#item-tech-news-8) ⭐️ 7.5/10
9. [Hackers activate automatic defrosting in supermarket fridges across Europe](#item-tech-news-9) ⭐️ 7.0/10
10. [Turn a WiFi 7 Router into a 320 Msps SDR Receiver](#item-tech-news-10) ⭐️ 7.0/10
11. [Muse Wonder](#item-tech-news-11) ⭐️ 7.0/10
12. [Reddit post seeks mechanistic argument for AGI from next-token + RL](#item-tech-news-12) ⭐️ 7.0/10
13. [Decision 3.0 releases open multimodal decision models from 0.6B to 27B](#item-tech-news-13) ⭐️ 7.0/10
14. [🤖 Anthropic：蒸馏数据初步减少 90% 至 99%](#item-tech-news-14) ⭐️ 7.0/10

**Financial News**
1. [2026 Nobel Economics Prize Awarded to Hall and Woodford](#item-finance-news-1) ⭐️ 9.0/10
2. [Cleveland Fed President Signals Possible Further Rate Hikes to Combat Inflation](#item-finance-news-2) ⭐️ 7.0/10
3. [新能源汽车出口退税率由 13% 下调至 9%](#item-finance-news-3) ⭐️ 7.0/10
4. [China to fine employers up to triple unpaid social‑insurance contributions starting Nov 2026](#item-finance-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [MiniCPM-V 4.7 35B-A3B: First open-source MoE model with on-device inference](https://www.reddit.com/r/LocalLLaMA/comments/1x47taj/openbmbminicpmv4735ba3b/) ⭐️ 9.0/10

OpenBMB released MiniCPM-V 4.7 35B-A3B, the first open-source Mixture-of-Experts model in the MiniCPM-V series, featuring Lookahead Expert Scheduling, fine-grained layer-wise quantization, and DSpark speculative sampling integration. The model achieves 13+ tokens/s decoding speed on iPhone 17 Pro Max for on-device multimodal inference while maintaining performance, and supports GGUF, FP8, and quantized variants across iOS, Android, and HarmonyOS via frameworks including SGLang, vLLM, llama.cpp, and Ollama.

reddit · r/LocalLLaMA · /u/Skyline34rGt · Oct 12, 17:16

**「Background on MiniCPM-V-4.7-35B-A3B Release」** The MiniCPM-V series represents a family of mixture-of-experts \(MoE\) large language models designed for efficient on-device inference. MiniCPM-V-4.7-35B-A3B marks the first open-source MoE model in this series, introducing Lookahead Expert Scheduling \(LES\) alongside fine-grained layer-wise quantization and DSpark speculative sampling. This enables smooth on-device operation at 13+ tokens/s on high-end mobile hardware like the iPhone 17 Pro Max, establishing a new performance-efficiency Pareto frontier for resource-constrained deployments.

**「Impact」** Developers can deploy MiniCPM-V 4.7 35B-A3B on iPhone 17 Pro Max at 13+ tokens/s using GGUF or FP8 quantization, enabling real-time on-device multimodal inference without cloud dependency and expanding edge AI capabilities for mobile applications.

**Tags**: `#open-source`, `#Mixture-of-Experts`, `#on-device-inference`, `#AI`, `#computer-vision`

---

<a id="item-tech-news-2"></a>
### [Looped Diffusion Transformer: the same blocks run several times inside each denoising step, and loop depth can be changed at sampling time \[R\]](https://www.reddit.com/r/MachineLearning/comments/1x49d61/looped_diffusion_transformer_the_same_blocks_run/) ⭐️ 8.5/10

A new diffusion transformer architecture that loops the same transformer blocks across denoising steps, achieving superior performance with dramatically lower compute compared to scaling up model size.

reddit · r/MachineLearning · /u/Fit-Ant2238 · Oct 12, 18:13

**Tags**: `#diffusion-transformer`, `#efficiency`, `#architecture`, `#scaling`

---

<a id="item-tech-news-3"></a>
### [Hello Python 3.15, goodbye 3.10, and now I can use 3.11](https://simonwillison.net/2026/Oct/12/python-3-15/) ⭐️ 8.0/10

Python 3.15 released with explicit lazy imports and other features; Simon Willison highlights the release and its impact on version support policies.

rss · Simon Willison · Oct 12, 18:15

**Tags**: `#Python`, `#programming languages`, `#software engineering`, `#open source`, `#release announcement`

---

<a id="item-tech-news-4"></a>
### [U-Space: Uncovering When and Why Uncertainty Arises in Language Models \[R\]\[D\]](https://www.reddit.com/r/MachineLearning/comments/1x44f9m/uspace_uncovering_when_and_why_uncertainty_arises/) ⭐️ 8.0/10

U‑Space introduces an interpretable, single‑pass uncertainty estimator for language models that identifies ambiguity, missing info, conflicting evidence, or general uncertainty without extra sampling or labeled data.

reddit · r/MachineLearning · /u/AdRevolutionary3242 · Oct 12, 15:10

**Tags**: `#uncertainty quantification`, `#interpretability`, `#open‑weight models`, `#AI research`, `#confidence estimation`

---

<a id="item-tech-news-5"></a>
### [learnc: Auto-tunes C constants for 9.1% JPEG gain, +4.9 F1 on WebRTC VAD](https://www.reddit.com/r/MachineLearning/comments/1x4dlbm/learnc_fit_the_constants_in_existing_c_code_to/) ⭐️ 8.0/10

learnc is an open-source \(MIT\) tool that automatically optimizes named constants in existing, unmodified C code against a user-defined C score function, then writes the updated values back to the same source file. Evaluated on held-out data, it achieved a 9.1% BD-rate reduction at equal SSIM for JPEG quantization tables in stb\_image\_write.h \(128 entries, tuned on 12 Kodak images, tested on 12 others\), independently verified with libjpeg and scikit-image; mozjpeg&\#x27;s hand-tuned tables yield 2.7%. On Google&\#x27;s WebRTC VAD \(all constants in vad\_core.c, tuned on LibriParty dev\), F1 improved from 0.810 to 0.859 on LibriParty eval. The author notes no JPEG gain below 1 bpp and that the method suits tens to hundreds of constants, not large weight sets.

reddit · r/MachineLearning · /u/keep\_up\_sharma · Oct 12, 20:51

**「Background」** Systems code often contains &quot;magic constants&quot; — quantization tables, thresholds, heuristic parameters — that are hand-tuned by engineers. Automated constant tuning has been explored in compiler optimization and auto-tuning frameworks, but learnc targets unmodified production C files directly, using a user-supplied scoring function rather than requiring code instrumentation or a separate build step. The JPEG and WebRTC VAD codebases are widely deployed reference implementations, making them realistic testbeds.

**「Impact」** Developers can drop learnc into existing C projects to improve compression quality or detection accuracy without rewriting algorithms; the 9.1% BD-rate gain over stb\_image\_write&\#x27;s default tables \(and 2.7% over mozjpeg&\#x27;s\) is immediately usable in any pipeline that embeds that header. The +0.049 F1 on WebRTC VAD translates to fewer missed speech segments in voice-activity detection. The tool&\#x27;s limitation to tens–hundreds of constants means it complements, rather than replaces, gradient-based learning for large parameter spaces.

**「Community Discussion」** No community comments were available at the time of collection.

**Tags**: `#compiler-optimization`, `#image-compression`, `#voice-activity-detection`, `#automated-tuning`, `#systems-engineering`

---

<a id="item-tech-news-6"></a>
### [Qwen released QwenGyre - RL framework for training AI agents on extremely long complex tasks](https://www.reddit.com/r/LocalLLaMA/comments/1x41myz/qwen_released_qwengyre_rl_framework_for_training/) ⭐️ 8.0/10

Qwen releases QwenGyre, a new RL framework enabling efficient training of AI agents on extremely long complex tasks through elastic resource management and trajectory-based sample optimization.

reddit · r/LocalLLaMA · /u/ResearchCrafty1804 · Oct 12, 13:18

**Tags**: `#RL framework`, `#long-horizon training`, `#AI agents`, `#efficient training`, `#trajectory processing`

---

<a id="item-tech-news-7"></a>
### [Boole-1.7B: 1‑bit Qwen3‑1.7B model released, outperforms prior 1‑bit models](https://www.reddit.com/r/LocalLLaMA/comments/1x452zj/boole17b_a_1bit_qwen317b_model_that_outperforms/) ⭐️ 8.0/10

Boole-1.7B, a 1‑bit quantized version of Qwen3‑1.7B, was released with packed weights of 247 MB, making it 13.9× smaller than the BF16 baseline. In a 10‑task evaluation it achieved 85.9 % of the BF16 model’s average score, surpassing the existing 1‑bit Bonsai‑1.7B and approaching the performance of the 1.58‑bit Bonsai‑1.7B. The model is available for local use via browser demo, vLLM, or llama.cpp, targeting low‑latency English inference.

reddit · r/LocalLLaMA · /u/d77chong · Oct 12, 15:35

**「Background」** 1‑bit quantization reduces each weight to a single binary value, drastically cutting model size but often degrading accuracy. Qwen3‑1.7B is a 1.7‑billion‑parameter language model from Alibaba’s Qwen series, serving as the base for this compression. Prior work such as Bonsai‑1.7B demonstrated 1‑bit and 1.58‑bit variants, establishing a baseline for comparison.

**「Impact」** By fitting into ~247 MB, Boole‑1.7B enables running a 1.7B‑parameter LLM on memory‑constrained devices \(e.g., consumer GPUs or CPUs\) and in‑browser with low latency, expanding access to local AI applications.

**Tags**: `#Model Compression`, `#Quantization`, `#Open Source LLM`, `#Edge AI`, `#Performance Optimization`

---

<a id="item-tech-news-8"></a>
### [OpenAI Codex CLI Installs Persistent Background Daemon by Default](https://github.com/openai/codex/issues/48195) ⭐️ 7.5/10

OpenAI&\#x27;s Codex CLI installs a persistent, self-updating background daemon by default, a behavior users are raising on the project&\#x27;s GitHub issue tracker. Reports indicate the daemon accumulates old versions, consuming roughly 12GB of disk space on some systems, and can trigger permission errors during automatic updates that block task execution. Although a feature flag exists to disable the daemon \(\`daemon\_auto\_start = false\` in \`~/.codex/config.toml\`\), users note it is not documented in available settings.

hackernews · whimblepop · Oct 12, 18:29 · [Discussion](https://news.ycombinator.com/item?id=50060694)

**「Background」** OpenAI’s Codex CLI previously required users to enable a background daemon explicitly via the \`daemon\_auto\_start\` flag, treating it as an advanced configuration. In version 0.157.0 \(Sep 25 2026\), a brief pull request flipped that flag to default‑on, making the self‑updating daemon the stable default behavior. This change means the daemon now runs persistently by default, consuming disk space and potentially causing system instability unless users manually disable it.

**「Impact」** The default installation adds persistent maintenance overhead through automatic updates and version storage, requiring manual configuration edits or filesystem attribute changes for users who need control over disk usage and background processes.

**「Community Discussion」** Commenters described inconsistent experiences, with some reporting disk bloat and update-related permission errors while others pointed to the undocumented flag as the fix. One user expressed a preference for a minimal alternative harness, citing Codex as &quot;overengineered&quot; compared to lighter implementations.

<details><summary>References</summary>
<ul>
<li><a href="https://codex.danielvaughan.com/2026/09/25/codex-cli-daemon-auto-start-stable-default-v0157/">Daemon Auto-Start Is Now the Stable Default in Codex CLI v0 ...</a></li>
<li><a href="https://www.solosoft.dev/post/codex-cli-daemon-audit/">Codex CLI Now Starts a Self-Updating Daemon by Default: 373 ...</a></li>

</ul>
</details>

**Tags**: `#software\_engineering`, `#ai\_coding\_tools`, `#open\_source`, `#technology\_industry`, `#daemon\_management`

---

<a id="item-tech-news-9"></a>
### [Hackers activate automatic defrosting in supermarket fridges across Europe](https://www.tomshardware.com/tech-industry/cyber-security/unprecedented-cyberattack-cripples-supermarket-fridges-across-europe-as-hackers-activate-automatic-defrosting-delivery-and-store-prices-also-impacted-by-incident) ⭐️ 7.0/10

Hackers activated automatic defrosting in supermarket refrigeration systems across Europe, causing temperature fluctuations that likely spoiled perishable inventory. The attack also disrupted delivery operations and altered store pricing displays. French supermarket chain Intermarche was among the affected retailers, with approximately 150 stores targeted. The incident exploited vulnerabilities in internet-connected refrigeration controllers, particularly older Danfoss models including the SM800 \(EOS 2021\) and SC355 \(EOS 2016\), which remained in service despite known security flaws.

hackernews · Zeekaas · Oct 12, 12:16 · [Discussion](https://news.ycombinator.com/item?id=50055304)

**「Background」** Modern supermarket refrigeration systems increasingly rely on internet-connected controllers for remote monitoring, diagnostics, and automated functions like defrost cycles. These IoT devices enable centralized management across store estates but introduce network security risks. Security researchers at Claroty previously identified critical vulnerabilities in Danfoss refrigeration controllers, demonstrating how attackers could manipulate temperature settings and defrost functions remotely. The European attack appears to have exploited these same or similar weaknesses in legacy controller firmware that remained unpatched across retail installations.

**「Impact」** The attack likely resulted in significant inventory losses as repeated defrost cycles raised refrigerator temperatures, spoiling perishable goods. Delivery operations were disrupted, and incorrect pricing information displayed on store shelves may have caused customer confusion and revenue impact. Retailers face costs for emergency controller replacements, security audits, and potential regulatory scrutiny over food safety compliance. The incident underscores the risk of legacy IoT devices in critical infrastructure where security patches are often not applied due to operational constraints.

**「Community Discussion」** Commenters debated why refrigeration systems are connected to the internet at all, with some noting that remote connectivity enables cost savings through predictive maintenance and centralized efficiency monitoring. Others pointed out that many organizations lack the resources for regular security reviews and hardware replacement cycles, leaving legacy devices exposed. Several observers drew parallels to a suspected similar attack on U.S. military base freezers in August 2026, though no definitive link has been established between the incidents.

**Tags**: `#cybersecurity`, `#IoT`, `#vulnerability`, `#retail`, `#supply-chain`

---

<a id="item-tech-news-10"></a>
### [Turn a WiFi 7 Router into a 320 Msps SDR Receiver](https://github.com/h0m3us3r/w1700k-sdr) ⭐️ 7.0/10

The GitHub repository w1700k-sdr shows how to repurpose a Wi‑Fi 7 router into a 320 Msps software‑defined radio receiver for 5 GHz signals. Using the router’s built‑in RF front‑end and firmware modifications, the system can capture and process 5 GHz Wi‑Fi traffic at full 320 Msps without additional hardware. The approach is aimed at hobbyists and hardware hackers seeking low‑cost, high‑speed SDR capability.

hackernews · djfergus · Oct 12, 12:41 · [Discussion](https://news.ycombinator.com/item?id=50055593)

**「Repurposing WiFi Hardware for SDR」** Software-defined radio \(SDR\) traditionally relies on dedicated hardware like the RTL2832U USB dongles, which are limited in bandwidth and frequency range. Recent projects have demonstrated that commodity WiFi chips can be repurposed as SDR receivers by exploiting their direct sampling capabilities, bypassing the need for traditional RF front-ends. This approach builds on earlier efforts such as using ESP32 microcontrollers for basic SDR functions, but leverages the higher clock speeds and wider bandwidth of WiFi 7 chipsets to achieve significantly improved performance.

**「Impact」** This enables hobbyists and developers to create affordable 5 GHz SDR receivers using readily available Wi‑Fi 7 routers, reducing the cost barrier for high‑speed radio experimentation.

**「Discussion」** Commenters highlight that the same chipset may work on the Banana Pi R4 and that the design offers a cheap 320 Msps receiver, contrasting with phone manufacturers’ contractual limits on SDR radios.

<details><summary>References</summary>
<ul>
<li><a href="https://radiohooligan.ru/hdsdr-dlya-rtl-sdr/">HDSDR — установка и настройка программы для приемника...</a></li>
<li><a href="https://www.rtl-sdr.com/esp32-sdr-trx-use-an-esp32-s3-as-a-receiver-for-sdr-and-as-an-fm-ssb-voice-transmitter-on-13cm/esp32-sdr-trx/">esp32- sdr -trx</a></li>

</ul>
</details>

**Tags**: `#software-defined-radio`, `#hardware-hacking`, `#wifi-7`, `#open-source`, `#sdr`

---

<a id="item-tech-news-11"></a>
### [Muse Wonder](https://research.meta.ai/blog/muse-wonder) ⭐️ 7.0/10

Meta&\#x27;s new Muse Wonder model prompts technical evaluation and privacy debates in the community.

hackernews · meetpateltech · Oct 12, 16:48 · [Discussion](https://news.ycombinator.com/item?id=50059115)

**Tags**: `#AI models`, `#Meta AI`, `#performance benchmarks`, `#privacy`, `#multimodal AI`

---

<a id="item-tech-news-12"></a>
### [Reddit post seeks mechanistic argument for AGI from next-token + RL](https://www.reddit.com/r/MachineLearning/comments/1x4awlk/what_is_the_strongest_mechanistic_argument_that/) ⭐️ 7.0/10

The Reddit post by u/Repulsive\_Twist\_9221 on r/MachineLearning \(2026-10-12\) requests rigorous, first-principles mechanistic arguments explaining how next-token prediction and reinforcement learning could produce general intelligence, grounding the question in computational learning theory and information theory rather than trend extrapolation. It targets AI researchers and engineers seeking operational-effectiveness explanations grounded in causal mechanisms, not philosophical debates or future-discovery appeals. The post provides no new capabilities or measured results, but frames a focused inquiry into theoretical pathways from current system architectures to AGI.

reddit · r/MachineLearning · /u/Repulsive\_Twist\_9221 · Oct 12, 19:09

**「Prerequisite concepts」** The post assumes familiarity with how modern large language models are trained primarily by next‑token prediction \(autoregressive language modeling\) and how reinforcement learning techniques such as RLHF or PPO are subsequently used to shape model behavior. It asks for a rigorous, first‑principles mechanistic explanation of why continuing to scale and refine these two learning objectives could, in theory, yield open‑ended general intelligence. No additional external facts are introduced beyond the Reddit discussion itself.

**Tags**: `#artificial general intelligence`, `#machine learning theory`, `#large language models`, `#reinforcement learning`, `#community discussion`

---

<a id="item-tech-news-13"></a>
### [Decision 3.0 releases open multimodal decision models from 0.6B to 27B](https://www.reddit.com/r/LocalLLaMA/comments/1x3th4p/decision_30_open_multimodal_decision_models_from/) ⭐️ 7.0/10

Decision 3.0 \(d3\) is an open‑source family of multimodal decision models ranging from 0.6B to 27B parameters, released under Apache‑2.0 and built on Qwen3.5 \(0.8B/2B/4B/9B\) and Qwen3.8‑27B backbones. The models accept text, images \(up to 1.6 MP each\) and video \(sampled at 2 fps, ≤32 frames, ≤0.2 MP per frame\) and output probabilities for choice, yes/no and score decisions without generating text, allowing multiple questions per input in a single call. According to the developers’ evaluation using the official Jev 0.3 kit, the 27B variant scores 64.7 on text and 71.6 on vision, ranking \#1 on both Jev Decision Index boards, while each size leads its class and the 9B “d3‑flash” outperforms the previous‑generation 27B Decision 2.0.

reddit · r/LocalLLaMA · /u/henzy123 · Oct 12, 05:26

**「Decision 2.0 predecessor &amp; Jev Index」** Decision 3.0 is the latest open-source multimodal decision model family from the vLLM Semantic Router team, directly following Decision 2.0, released in October 2026 \(tool-1-2\). Decision 2.0 established the Jev Decision Index framework for measuring text and vision accuracy on choice, yes/no, and score tasks across model sizes. Decision 3.0 expands the parameter range to 0.6B–27B and adds video input support, building on the index&\#x27;s evaluation structure.

**「Impact」** The release provides developers with a freely available, high‑performing multimodal decision model that achieves zero‑shot video understanding scores of 77.4 \(27B\) and 70.3 \(4B\) on the Perception Test validation set, enabling efficient deployment of vision‑language decision tasks without fine‑tuning.

<details><summary>References</summary>
<ul>
<li><a href="https://modelsystem.one/news/vllm-sr-decision-2-family/">vLLM Semantic Router releases Decision 2.0, open decision ...</a></li>

</ul>
</details>

**Tags**: `#multimodal`, `#decision models`, `#open source`, `#LLM`, `#evaluation`

---

<a id="item-tech-news-14"></a>
### [🤖 Anthropic：蒸馏数据初步减少 90% 至 99%](https://www.anthropic.com/research/distillation-defenses) ⭐️ 7.0/10

Anthropic reports its new anti-distillation measures reduce stolen model capabilities by 90-99%, with specific technical safeguards and low false-positive rates.

telegram · zaihuapd · Oct 13, 01:25

**Tags**: `#AI security`, `#model distillation`, `#Anthropic`, `#machine learning`, `#technology news`

---

## Financial News

<a id="item-finance-news-1"></a>
### [2026 Nobel Economics Prize Awarded to Hall and Woodford](https://x.com/NobelPrize/status/2109581902541939046) ⭐️ 9.0/10

The Royal Swedish Academy of Sciences awarded the 2026 Nobel Memorial Prize in Economic Sciences to Robert E. Hall and Michael Woodford for their contributions to the microeconomic foundations of macroeconomic stability.

telegram · zaihuapd · Oct 12, 10:27

**「Background」** Robert Hall, a Stanford professor and Hoover Institution fellow, and Michael Woodford, a Columbia University macroeconomist and monetary theorist, have shaped modern understanding of how microeconomic behavior underpins macroeconomic stability and monetary policy.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Robert_Hall_%28economist%29">Robert Hall ( economist ) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Michael_Dean_Woodford">Michael Dean Woodford - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Nobel Prize`, `#Macroeconomics`, `#Monetary Policy`, `#Academic Research`, `#Economic Theory`

---

<a id="item-finance-news-2"></a>
### [Cleveland Fed President Signals Possible Further Rate Hikes to Combat Inflation](https://www.cnbc.com/2026/10/12/beth-hammack-fed-inflation-policy.html) ⭐️ 7.0/10

Cleveland Fed President Beth Hammack, a voting member, said tighter monetary policy may be needed to bring inflation down to the 2% target and warned that persistently elevated inflation risks entrenching an &quot;inflationary mindset&quot; in the economy.

rss · CNBC Finance · Oct 13, 02:58

**「Background」** The Fed raised rates last month for the first time in three years; PCE inflation was 3.4% year-over-year in August with core at 3%, and traders see a 78% chance of no change at the next meeting but an 88% chance of a hike in December.

**「Impact」** If the Fed follows through with additional hikes, borrowing costs for households and businesses would rise further, increasing the cost of mortgages, auto loans, and corporate credit.

**Tags**: `#Federal Reserve`, `#interest rates`, `#inflation`, `#monetary policy`, `#Beth Hammack`

---

<a id="item-finance-news-3"></a>
### [新能源汽车出口退税率由 13% 下调至 9%](https://www.news.cn/20261012/9709731f470b42f9a84825c2e4eb914b/c.html) ⭐️ 7.0/10

Government reduces NEV export tax rate from 13% to 9% effective April 1, 2027, and cancels VAT export tax for certain products like e-cigarette equipment.

telegram · zaihuapd · Oct 12, 11:00

**Tags**: `#policy`, `#automotive`, `#trade`, `#tax`, `#nev`

---

<a id="item-finance-news-4"></a>
### [China to fine employers up to triple unpaid social‑insurance contributions starting Nov 2026](https://fgk.chinatax.gov.cn/zcfgk/c100012/c5252754/content.html) ⭐️ 7.0/10

China&\#x27;s State Administration of Taxation will enforce new penalty guidelines from 1 November 2026 that allow fines of up to three times the amount of unpaid social‑insurance contributions for employers who still do not pay after being ordered to do so.

telegram · zaihuapd · Oct 13, 02:45

**「Background」** Previously, late or underpayment of social‑insurance fees was not treated as a tax violation and therefore did not incur tax penalties.

**「Impact」** Employers who miss the payment deadline after notice will have to pay the arrears, a daily late fee of 0.05% of the unpaid amount, and possibly a fine equal to up to three times the arrears.

**Tags**: `#Tax policy`, `#Employment regulation`, `#Corporate compliance`, `#Social insurance`, `#China`

---