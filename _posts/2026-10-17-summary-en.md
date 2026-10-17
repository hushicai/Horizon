---
layout: default
title: "Horizon Summary: 2026-10-17 (EN)"
date: 2026-10-17
lang: en
---

> From 41 items, 15 important content pieces were selected

---

**Technology News**
1. [Claude reveals ECDSA curve origins](#item-tech-news-1) ⭐️ 9.0/10
2. [Apple ML Research: Muse Spark Open with MLX on Mac Studio](#item-tech-news-2) ⭐️ 8.0/10
3. [90% of US working hours are spent on tasks not covered well by AI benchmarks](#item-tech-news-3) ⭐️ 8.0/10
4. [\[Research\] 2,788 tokens/s on a single RTX 5090 with a diffusion LLM — Introducing ORL \(fully open source\) \[R\]](#item-tech-news-4) ⭐️ 8.0/10
5. [\[P\] my rust framework trains nanoGPT with the exact same bits as pytorch. worth continuing? \[P\]](#item-tech-news-5) ⭐️ 7.5/10
6. [Llama.cpp ports to jailbroken PS5 for GGUF inference](#item-tech-news-6) ⭐️ 7.0/10
7. [JPEG XL vs AVIF: Trade-offs in Web Image Compression](#item-tech-news-7) ⭐️ 7.0/10
8. [Anthropic&\#x27;s Claude Code Team Launches AI-Powered Code Review System](#item-tech-news-8) ⭐️ 7.0/10
9. [Home Assistant Supervisor Password Scanning Fix](#item-tech-news-9) ⭐️ 7.0/10
10. [Big Fish: Exploiting a 37-Year-Old Kernel Bug in OpenBSD](#item-tech-news-10) ⭐️ 7.0/10
11. [Market selloff and rising rates pause AirTrunk, Firmus, and SB Energy data center listings](#item-tech-news-11) ⭐️ 7.0/10
12. [StepFun releases Step 5 Preview, a 600B sparse MoE agent model](#item-tech-news-12) ⭐️ 7.0/10
13. [Telegram Discloses User Data to U.S. Government Under Court Orders](#item-tech-news-13) ⭐️ 7.0/10
14. [Nvidia RTX 5090 Supply Shift to Workstation GPUs Drives Price Surge](#item-tech-news-14) ⭐️ 7.0/10

**Financial News**
1. [U.S. presses China on Mastercard, Citigroup market access in bilateral Bangkok talks, official says](#item-finance-news-1) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Claude reveals ECDSA curve origins](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Claude uncovered that NIST&\#x27;s P‑192, P‑224, P‑256, P‑384, and P‑521 curve seeds originated from a timestamp‑seeded lrand48 RNG rather than a secure hash.

hackernews · ahlCVA · Oct 16, 18:55 · [Discussion](https://news.ycombinator.com/item?id=50122800)

**Tags**: `#Cryptography`, `#Security`, `#Random Number Generation`, `#Standards`, `#ECDSA`

---

<a id="item-tech-news-2"></a>
### [Apple ML Research: Muse Spark Open with MLX on Mac Studio](https://machinelearning.apple.com/research/mlx-distributed-inference) ⭐️ 8.0/10

Apple’s MLX release enables running a near‑trillion‑parameter Muse Spark Open model on Mac Studio clusters, achieving high token throughput and demonstrating practical large‑model inference on consumer hardware.

hackernews · antipaul · Oct 16, 13:43 · [Discussion](https://news.ycombinator.com/item?id=50118320)

**Tags**: `#MLX`, `#Mac Studio`, `#Large Language Models`, `#Distributed Inference`, `#AI Research`

---

<a id="item-tech-news-3"></a>
### [90% of US working hours are spent on tasks not covered well by AI benchmarks](https://www.mercor.com/research/labor-index/benchmark-map/) ⭐️ 8.0/10

A research study reveals that 90% of US working hours involve tasks poorly covered by current AI benchmarks, challenging assumptions about AI&\#x27;s ability to handle real-world professional work.

hackernews · speckx · Oct 16, 17:08 · [Discussion](https://news.ycombinator.com/item?id=50121179)

**Tags**: `#AI benchmarks`, `#labor economics`, `#artificial intelligence`, `#software engineering`

---

<a id="item-tech-news-4"></a>
### [\[Research\] 2,788 tokens/s on a single RTX 5090 with a diffusion LLM — Introducing ORL \(fully open source\) \[R\]](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 8.0/10

Researchers introduce ORL, an open-source technique boosting diffusion LLM inference to 2,788 tokens/s on a single RTX 5090 with comparable or better quality.

reddit · r/MachineLearning · /u/arty\_photography · Oct 16, 20:03

**Tags**: `#diffusion language models`, `#ORL`, `#inference acceleration`, `#RTX 5090`, `#open source`

---

<a id="item-tech-news-5"></a>
### [\[P\] my rust framework trains nanoGPT with the exact same bits as pytorch. worth continuing? \[P\]](https://www.reddit.com/r/MachineLearning/comments/1x7ojxo/p_my_rust_framework_trains_nanogpt_with_the_exact/) ⭐️ 7.5/10

A new Rust framework \(DenseCore\) demonstrates bit-for-bit parity with PyTorch&\#x27;s nanoGPT, enabling equivalent model training across different backends including dropout and custom CUDA operations, bridging Rust and the dominant ML ecosystem.

reddit · r/MachineLearning · /u/Mental-Feature-2377 · Oct 16, 18:49

**Tags**: `#rust`, `#machine-learning`, `#deep-learning-framework`, `#AI`, `#open-source`

---

<a id="item-tech-news-6"></a>
### [Llama.cpp ports to jailbroken PS5 for GGUF inference](https://github.com/cobanov/PS5LM) ⭐️ 7.0/10

The PS5LM project ports Llama.cpp to a jailbroken PlayStation 5, enabling native inference of any GGUF language model on the console. It requires a modified system with custom firmware and provides a low‑cost edge AI platform for owners. The hack currently runs models such as Qwen 3.8 27B at 2‑bit quantization, delivering roughly 2 million tokens per day at about $0.70 in electricity.

hackernews · Anon84 · Oct 16, 18:32 · [Discussion](https://news.ycombinator.com/item?id=50122431)

**「Background」** Llama.cpp is an open‑source inference library that supports the GGUF quantized model format across many hardware platforms. Jailbreaking a PS5 gives users root access and the ability to load unsigned code, making it possible to compile and run custom software like Llama.cpp. The PS5’s custom AMD APU provides GPU and CPU resources that can be leveraged for continuous AI tasks.

**「Impact」** PS5 owners can now run always‑on AI inference for tasks such as server‑error monitoring, security‑footage analysis, or plant‑growth tracking at a cost of roughly $0.70 per day for up to 2 million tokens, turning a gaming console into an affordable edge AI device.

**「Community discussion」** Commenters warn that hosting the project on GitHub may lead to takedown by Sony and recommend a custom domain, while others note the technique could also apply to similar hardware like the BC250 mining boards.

**Tags**: `#Hardware hacking`, `#Edge AI`, `#LLM inference`, `#Console computing`, `#Open source tools`

---

<a id="item-tech-news-7"></a>
### [JPEG XL vs AVIF: Trade-offs in Web Image Compression](https://jakearchibald.com/2026/jpeg-xl-vs-avif/) ⭐️ 7.0/10

The discussion compares JPEG XL and AVIF for web use-cases, highlighting trade-offs in compression quality and encoding speed. JPEG XL&\#x27;s libjxl at maximum effort produces files 2–7% smaller for photos and ~25% smaller for screenshots and illustrations, but takes 9–46 seconds—50–180x longer than its default setting. The slow speed at efforts above 7 is attributed to an iterative evaluation-optimization loop of the Butteraugli perceptual error metric. Meanwhile, AVIF can achieve 10x+ smaller file sizes with good quality using specific ffmpeg settings and supports PNG transparency, though some users report quality issues with highlights.

hackernews · farlight · Oct 16, 16:12 · [Discussion](https://news.ycombinator.com/item?id=50120224)

**「Background」** JPEG XL and AVIF are both modern image compression formats designed for the web, aiming to replace legacy formats like JPEG and PNG with better compression efficiency. The comparison centers on practical trade-offs that matter to web developers: encoding speed, file size reduction, visual quality, and tooling support.

**「Impact」** Web developers choosing between these formats must weigh encoding speed against compression efficiency, as JPEG XL&\#x27;s highest quality settings may be impractical for real-time encoding while AVIF&\#x27;s aggressive compression can introduce visible artifacts in highlights.

**「Community Discussion」** The comments reveal a split: Metricon advocates for AVIF in production with specific ffmpeg settings achieving 10x compression, while PaulHoule argues AVIF erases highlights on certain images, using an F1 car photo as evidence. yhjc2692 provides technical detail on JPEG XL&\#x27;s encoding speed trade-offs, and ezst cautions against declaring a winner too early, drawing parallels to the MP3/LAME era and WebP&\#x27;s initial claims.

**Tags**: `#image compression`, `#web performance`, `#JPEG XL`, `#AVIF`, `#web development`

---

<a id="item-tech-news-8"></a>
### [Anthropic&\#x27;s Claude Code Team Launches AI-Powered Code Review System](https://claude.dev/blog/solving-code-review-at-anthropic/) ⭐️ 7.0/10

Anthropic&\#x27;s Claude Code team has deployed an AI-powered code review workflow that automatically performs routine checks while reserving human review for high-risk changes, aiming to improve efficiency and maintain SOC2 compliance.

hackernews · pretext · Oct 16, 19:04 · [Discussion](https://news.ycombinator.com/item?id=50122951)

**「Context: AI-Assisted Development and Compliance」** This initiative builds on broader trends in AI-assisted software development and addresses the need for scalable code review processes within large engineering teams. The system combines machine learning models for initial analysis with human judgment for critical modifications.

**「Operational Efficiency and Compliance Balance」** For Anthropic&\#x27;s engineering organization, the system reduces repetitive review workload while ensuring that risky changes undergo human scrutiny, supporting SOC2 compliance requirements. External users are unlikely to see direct changes, as this appears to be an internal tooling solution.

**「Team Perspectives on Automation and Job Security」** Commenters like mk12 observed that &\#x27;most of the path is automated&\#x27; with human intervention reserved for risky changes, while gaal\_dornick raised questions about SOC2 compliance given the mandatory human review requirement. Another commenter, vb-8448, doubted the scalability of keeping up with 30k daily PRs under full human supervision.

**Tags**: `#code review`, `#AI-assisted development`, `#internal tooling`, `#compliance`, `#Anthropic`

---

<a id="item-tech-news-9"></a>
### [Home Assistant Supervisor Password Scanning Fix](https://github.com/home-assistant/home-assistant.io/issues/49314) ⭐️ 7.0/10

Home Assistant&\#x27;s Supervisor feature was scanning user passwords for pwned detection without opt-in, but a recent fix allows users to disable the check entirely using \`ha security options --pwned=false\`.

hackernews · trvrprkr · Oct 16, 20:33 · [Discussion](https://news.ycombinator.com/item?id=50124251)

**「Privacy concern in Home Assistant Supervisor」** The issue arose because the Supervisor component had been checking application passwords against a pwned database for years without requiring explicit user consent, raising significant privacy concerns among users.

**Tags**: `#privacy`, `#security`, `#home-automation`, `#password-management`, `#open-source`

---

<a id="item-tech-news-10"></a>
### [Big Fish: Exploiting a 37-Year-Old Kernel Bug in OpenBSD](https://calif.io/research/big-fish) ⭐️ 7.0/10

Discovery of a 37‑year‑old OpenBSD kernel bug, with analysis of its persistence and detection techniques.

hackernews · rs\_rs\_rs\_rs\_rs · Oct 16, 14:44 · [Discussion](https://news.ycombinator.com/item?id=50118977)

**Tags**: `#OpenBSD`, `#kernel security`, `#vulnerability research`, `#static analysis`, `#bug discovery`

---

<a id="item-tech-news-11"></a>
### [Market selloff and rising rates pause AirTrunk, Firmus, and SB Energy data center listings](https://www.kitco.com/news/off-the-wire/2026-10-15/market-selloff-rising-rates-test-ai-data-centre-deal-boom) ⭐️ 7.0/10

AirTrunk&\#x27;s REIT listing, NVIDIA-backed Firmus&\#x27;s offering, and SoftBank-backed SB Energy&\#x27;s listing were withdrawn or suspended in the past week as a market selloff and rising interest rates pressured AI data center deals. Investors are now requiring companies to demonstrate they can absorb higher interest rates and compute costs before backing infrastructure. Dealogic data shows Asia data center M&amp;A reached $21.3 billion this year, about double full-year 2025&\#x27;s $10 billion, while equity financing fell 4.6% year over year. Analysts said capital has not exited the sector, but investors are prioritizing quality over volume.

telegram · zaihuapd · Oct 16, 05:10

**「Why financing conditions matter」** Data center construction is capital-intensive and typically depends on debt and equity markets, so higher interest rates raise borrowing costs and can delay or cancel listings. REITs and equity offerings are common ways operators such as AirTrunk, Firmus, and SB Energy raise infrastructure funding.

**「Consequence for affected operators」** Withdrawn and suspended listings mean affected operators must secure alternative financing or delay projects until they can demonstrate returns that cover elevated interest rates and compute costs; equity investors are applying stricter quality screens to new data center deals.

**Tags**: `#AI`, `#data centers`, `#investment`, `#market trends`, `#hardware`

---

<a id="item-tech-news-12"></a>
### [StepFun releases Step 5 Preview, a 600B sparse MoE agent model](https://huggingface.co/stepfun-ai/Step-5-Preview) ⭐️ 7.0/10

StepFun made Step 5 Preview, a 600‑billion‑parameter sparse MoE multimodal model, available on Hugging Face for agent workflows. The model uses a total of 600 B parameters with 27 B active units, supports up to 1 M token context, and accepts text, image, and video inputs. It is licensed under the StepFun Model License 1.0 and can be deployed via OpenAI‑compatible APIs using vLLM or SGLang. The announcement claims strong performance in software engineering, long‑cycle agent execution, and financial tasks, though no benchmark data or independent verification is provided.

telegram · zaihuapd · Oct 16, 06:36

**「Sparse MoE and long-context agent models」** Step 5 Preview follows the established trend of sparse Mixture-of-Experts \(MoE\) architectures, which activate only a subset of parameters per token to scale total model size while keeping compute costs manageable. The 1 million token context length aligns with recent efforts to extend context windows for agentic workloads that require retaining long execution traces and documents. StepFun previously released earlier Step series models, establishing a lineage of Chinese-language flagship models before this agent-oriented preview release.

**「Impact」** Developers can now integrate the model into existing OpenAI‑API‑compatible pipelines, but must comply with the StepFun Model License 1.0 and ensure their deployment environment supports vLLM or SGLang for the 600 B‑parameter model.

<details><summary>References</summary>
<ul>
<li><a href="https://www.eesel.ai/blog/stepfun-step-5">StepFun Step 5 Preview : specs, pricing, benchmarks, and... | eesel AI</a></li>
<li><a href="https://www.deai.org/news/stepfun-step-5-preview-api-open-weights-oct-15">StepFun &#x27;s Step 5 Preview API ships; open weights promised October ...</a></li>
<li><a href="https://openrouter.ai/stepfun/step-5-preview">Step 5 Preview - API Pricing &amp; Providers | OpenRouter</a></li>

</ul>
</details>

**Tags**: `#large-language-models`, `#multimodal-models`, `#agent-systems`, `#software-engineering`, `#sparse-mixture-of-experts`

---

<a id="item-tech-news-13"></a>
### [Telegram Discloses User Data to U.S. Government Under Court Orders](https://www.404media.co/heres-what-telegram-giving-data-to-the-u-s-government-looks-like/) ⭐️ 7.0/10

Newly unsealed court documents reveal Telegram provided phone numbers, user IDs, and IP addresses for thousands of users to U.S. law enforcement in response to court orders. Telegram characterized the disclosures as voluntary and stated it does not acknowledge U.S. jurisdiction. As of January 2026, the company had supplied data for 2,253 users, including information related to a defendant accused of involvement in the October 7, 2023 attacks on Israel.

telegram · zaihuapd · Oct 16, 14:57

**「Background」** Telegram has historically positioned itself as a privacy-focused messaging platform with end-to-end encryption available for secret chats, though standard chats are encrypted only in transit and stored on Telegram&\#x27;s servers. The platform has previously resisted government data requests, notably refusing to comply with Russian authorities in 2018, which led to a temporary ban in that country.

**「Impact」** Users relying on Telegram for sensitive communications should understand that standard \(non-secret\) chats and associated metadata — including phone numbers and IP addresses — are accessible to Telegram and can be disclosed under legal compulsion. Developers building on Telegram&\#x27;s platform or advising on secure communications must account for this data disclosure capability in threat models.

**Tags**: `#Telegram`, `#data privacy`, `#law enforcement`, `#user data`, `#404 Media`

---

<a id="item-tech-news-14"></a>
### [Nvidia RTX 5090 Supply Shift to Workstation GPUs Drives Price Surge](https://www.techpowerup.com/353578/nvidia-reportedly-ending-the-rtx-5090-reserves-gb202-silicon-for-workstation-gpus) ⭐️ 7.0/10

Rumors claim Nvidia has ended RTX 5090/V2 production for the GeForce consumer line and redirected GB202 wafer supply to the higher-margin RTX PRO workstation product line, where the same chip carries an official per-unit price of $4,500–$6,000+ versus the original $1,999 consumer MSRP. Nvidia&\#x27;s Senior VP Jeff Fisher publicly denied the discontinuation on October 16, 2026, calling the claims &quot;not true,&quot; but acknowledged constrained supply. Retail reality diverges from the official denial: the US online store has removed the RTX 5090 product page, Micro Center has switched its sales status to &quot;no longer sold,&quot; and multiple physical stores report sold-out inventory. Domestic 32 GB spot prices in China have climbed from approximately 35,000 RMB in early September 2026 to roughly 54,000 RMB by mid-October, a rise of over 50%. The consumer flagship position now falls to the RTX 5080 24 GB, which uses the smaller GB203 core with less than half the die scale of the GB202 but remains priced at the flagship tier, creating a generational step-down in specifications at the top of the consumer stack.

telegram · zaihuapd · Oct 17, 00:02

**「Prerequisite Context」** The RTX 5090 is Nvidia&\#x27;s flagship consumer GPU built on the GB202 die, positioned as the highest-performance card in the GeForce lineup. When manufacturing capacity for a given silicon substrate is reallocated from lower-margin consumer SKUs to higher-margin professional or workstation products, the direct effect is reduced consumer availability and upward pressure on street prices. The RTX 5080 24 GB, based on the smaller GB203 core, serves as the fallback consumer flagship in this scenario.

**「Concrete Consequence」** Consumers, software engineers, and AI/ML practitioners who depend on top-tier consumer GPU availability now face a sharply narrowed supply window and a steeper cost floor. The domestic spot price of the RTX 5090 32 GB rose from roughly 35,000 RMB to about 54,000 RMB in under two months, and the downgrade to the RTX 5080 24 GB as the consumer flagship means less raw compute for the same flagship-tier spend.

**Tags**: `#GPU market`, `#Nvidia RTX 5090`, `#Hardware supply chain`, `#AI/ML hardware`, `#Consumer pricing`

---

## Financial News

<a id="item-finance-news-1"></a>
### [U.S. presses China on Mastercard, Citigroup market access in bilateral Bangkok talks, official says](https://www.cnbc.com/2026/10/16/us-china-mastercard-citigroup-market-access.html) ⭐️ 8.0/10

U.S. Treasury officials reported that U.S. companies including Mastercard and Citigroup were discussed for market access in China during bilateral meetings in Bangkok, with regulatory approvals tied to recent U.S.-China presidential interactions.

rss · CNBC Finance · Oct 16, 16:46

**Tags**: `#financial regulation`, `#market access`, `#cross-border capital flows`, `#China financial sector`

---