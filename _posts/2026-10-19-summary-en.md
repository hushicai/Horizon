---
layout: default
title: "Horizon Summary: 2026-10-19 (EN)"
date: 2026-10-19
lang: en
---

> From 34 items, 14 important content pieces were selected

---

**Technology News**
1. [vllm-project/vllm released v0.32.0](#item-tech-news-1) ⭐️ 8.0/10
2. [TempoPFN: Synthetic pre-training of linear RNNs for zero-shot time series forecasting](#item-tech-news-2) ⭐️ 8.0/10
3. [Proof‑before‑reuse blocks poisoned skill reuse in coding agents](#item-tech-news-3) ⭐️ 8.0/10
4. [Anthropic discusses AI agent negotiation rules with law firms](#item-tech-news-4) ⭐️ 8.0/10
5. [NVIDIA Optimizes Kimi K3 Inference Speed with vLLM Upstream](#item-tech-news-5) ⭐️ 8.0/10
6. [Linux 内核漏洞可导致 KVM 访客逃逸](#item-tech-news-6) ⭐️ 8.0/10
7. [Nature Study Finds Microplastics Generate Reactive Free Radicals in Human Body](#item-tech-news-7) ⭐️ 8.0/10
8. [Hybrid Reasoning Agents Introduce Latent‑Space LLM Reasoning with Open Code](#item-tech-news-8) ⭐️ 7.5/10
9. [RepRapMicron](#item-tech-news-9) ⭐️ 7.0/10
10. [Open MicroManipulator Sub-Micrometer 3D Motion Control Platform](#item-tech-news-10) ⭐️ 7.0/10
11. [Google Research Opens Source Harness² Recursive Agent Framework](#item-tech-news-11) ⭐️ 7.0/10
12. [MIT Pattie Maes team research on AI-generated content implanting false memories](#item-tech-news-12) ⭐️ 7.0/10

**Financial News**
1. [One Year After the Food Delivery War, Platforms Profit While Merchants and Riders Struggle](#item-finance-news-1) ⭐️ 7.0/10
2. [US AI infrastructure boom shows cracks as projects stall and chip stocks fall](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [vllm-project/vllm released v0.32.0](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) ⭐️ 8.0/10

vLLM v0.32.0 release highlights 814 commits, new structured decision endpoints, and widespread low-precision KV cache support.

github · khluu · Oct 18, 06:50

**Tags**: `#vLLM`, `#inference-engine`, `#low-precision KV cache`, `#structured decisions`, `#open source`

---

<a id="item-tech-news-2"></a>
### [TempoPFN: Synthetic pre-training of linear RNNs for zero-shot time series forecasting](https://www.reddit.com/r/MachineLearning/comments/1x97v19/tempopfn_synthetic_pretraining_of_linear_rnns_for/) ⭐️ 8.0/10

The TempoPFN paper accepted at NeurIPS 2026 releases a synthetic time series data library and a DeltaProduct-based linear RNN pre-training method enabling zero-shot forecasting. Released code, models, and synthetic generators are available on arXiv \(2510.25502\), GitHub \(automl/TempoPFN\), and HuggingFace \(AutoML-org/TempoPFN\), with the synthetic data already integrated into the Toto-2 and TS-ICL systems.

reddit · r/MachineLearning · /u/Yossarian\_1234 · Oct 18, 16:43

**「Background」** Linear recurrent neural networks \(linear RNNs\) have emerged as efficient alternatives to Transformers for sequence modeling, offering linear-time inference and faster training. DeltaProduct, introduced in early 2025, improved state-tracking in linear RNNs by using products of generalized Householder matrices as state-transition matrices. TempoPFN builds on this architecture with a GatedDeltaProduct backbone extended with state-weaving, and addresses a key limitation noted in prior work: synthetic-only pre-training approaches had previously underperformed on challenging zero-shot forecasting benchmarks.

**「Impact」** The open release of TempoPFN&\#x27;s synthetic data generation pipeline, training code, and pre-trained DeltaProduct linear RNN models gives researchers and practitioners a reproducible foundation for building zero-shot time series forecasting systems without large real-world datasets. The library has already been adopted in Datadog&\#x27;s Toto-2 model \(10% of its training data\) and the TS-ICL foundation model, demonstrating immediate utility for developing new time series foundation models.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2510.25502">[2510.25502] TempoPFN: Synthetic Pre-training of Linear RNNs ... NeurIPS Poster TempoPFN: Synthetic Pre-training of Linear ... GitHub - automl/TempoPFN: TempoPFN: Zero-shot Time Series ... TempoPFN: Synthetic Pre-training of Linear RNNs for Zero-shot ... TempoPFN: Synthetic Pre-training of Linear RNNs for Zero-shot ... TempoPFN: Towards Synthetic Pre-training of Linear RNNs for ... TempoPFN: Univariate Zero-Shot Forecasting</a></li>
<li><a href="https://arxiv.org/pdf/2502.10297">DeltaProduct : Improving State-Tracking in Linear RNNs via...</a></li>
<li><a href="https://github.com/automl/DeltaProduct">GitHub - automl / DeltaProduct : DeltaProduct is a new linear ...</a></li>
<li><a href="https://arxiv.org/html/2606.05878">TS - ICL : A Flexible Time -Indexed Foundation Model for Time Series ...</a></li>
<li><a href="https://seunghan96.github.io/llm/ts/TempoPFN/">TempoPFN ; Synthetic Pre-training of Linear RNNs for Zero-shot Time ...</a></li>
<li><a href="https://huggingface.co/Datadog/Toto-2.0-2.5B-FT">Datadog/ Toto - 2 .0-2.5B-FT · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#time series forecasting`, `#synthetic data`, `#linear RNN`, `#foundation models`, `#NeurIPS`

---

<a id="item-tech-news-3"></a>
### [Proof‑before‑reuse blocks poisoned skill reuse in coding agents](https://www.reddit.com/r/MachineLearning/comments/1x975ea/proof_before_reuse_showing_agents_only_what_later/) ⭐️ 8.0/10

For a coding agent using Claude Haiku 5.5 and Sonnet 5.5, limiting procedural memory to only code changes reproduced in later sessions prevents poisoned skills from influencing its procedural memory. One poisoned learning session \(new file, unrelated line, or a fused line\) was followed by three clean sessions, after which five scored sessions per arm were run with a hidden verifier of 187 behavioural checks. Replay re‑introduced the poison in all 30 repos, naive memory exposed it in 3 of 30, and proof‑before‑reuse exposed it in 0 of 30, even when the fused poison passed step‑level checks and was only removed by line‑level filtering.

reddit · r/MachineLearning · /u/maa\_\_\_\_z · Oct 18, 16:14

**「Background」** Coding agents acquire procedural memory by retaining code changes from sessions whose tests passed; such retained skills can later affect the agent&\#x27;s output on new tasks. Prior research has shown that unfiltered retention of these changes can be exploited if a learning session is poisoned.

**「Impact」** Users of coding agents that retain skills across sessions face a risk of having poisoned code re‑introduced unless they employ proof‑before‑reuse; the study demonstrates that without it, replay and naive memory expose the poison in the majority of cases, while proof‑before‑reuse avoids exposure in the tested setting. The mitigation does not protect against a poison placed directly in the repository, and the results apply only to the single task and small sample \(n = 5\) examined.

**Tags**: `#AI safety`, `#machine learning`, `#software engineering`, `#procedural memory`, `#poisoning`

---

<a id="item-tech-news-4"></a>
### [Anthropic discusses AI agent negotiation rules with law firms](https://www.ft.com/content/f7c26ac0-f5f2-443a-86b2-39d62f7920a9?syn-25a6b1a6=1) ⭐️ 8.0/10

Anthropic is collaborating with legal institutions to develop negotiation norms and authorization frameworks for AI agents that act on users&\#x27; behalf, such as haggling, dispute resolution, and salary talks. In September 2026, Anthropic employees used Claude agents in a virtual book-trading experiment where &quot;ruthless&quot; agents held a slight advantage, and a Harvard study of over 180,000 agent negotiations identified new tactics that weaken opponents. The company is also exploring providing agents with user-signed authorization documents to govern their actions. These efforts aim to address governance and accountability in autonomous AI systems, though the negotiated rules remain in the discussion phase.

telegram · zaihuapd · Oct 18, 07:07

**「Background」** AI agents that negotiate on behalf of users have been demonstrated in recent experiments, including Anthropic&\#x27;s September 2026 virtual trading test and a Harvard study of over 180,000 negotiations, which showed that agents can develop aggressive tactics that give them an advantage. These findings highlight the need for governance frameworks to ensure accountability and fairness. Against this backdrop, Anthropic is now engaging legal experts to define formal negotiation norms.

**「Impact」** Developers integrating Anthropic&\#x27;s Claude agents for user-negotiation tasks may need to incorporate emerging negotiation norms and authorization document checks to maintain compliance and prevent unintended agent behavior, as no standardized framework currently exists.

**Tags**: `#AI agents`, `#AI governance`, `#negotiation protocols`, `#legal AI`

---

<a id="item-tech-news-5"></a>
### [NVIDIA Optimizes Kimi K3 Inference Speed with vLLM Upstream](https://x.com/SemiAnalysis_/status/2111627094878790023) ⭐️ 8.0/10

NVIDIA has optimized the Kimi K3 model&\#x27;s inference speed using vLLM upstreams, achieving 423 tokens per second \(1.68× faster\) on a 28-billion-parameter model compared to the same hardware. This improvement comes from Cute DSL decoding kernel optimization and Megakernel fusion techniques developed within NVIDIA&\#x27;s ecosystem. The update targets developers and operators deploying Kimi K3 who require higher throughput for real-time inference applications.

telegram · zaihuapd · Oct 18, 08:20

**「vLLM upstream and kernel fusion for Kimi K3」** The optimization described in the report modifies vLLM upstream to accelerate Kimi K3 inference, incorporating a Cute DSL decoding kernel and Megakernel fusion. These kernel-level changes enable the reported 423 tokens/s throughput on a 28B parameter model with identical hardware.

**「Throughput Improvement for Real-Time Applications」** For developers and organizations running Kimi K3, the 1.68× speedup means they can process approximately three times more tokens per second, reducing latency and improving throughput for real-time applications.

**Tags**: `#ai`, `#machine-learning`, `#inference-optimization`, `#llm`, `#nvidia`

---

<a id="item-tech-news-6"></a>
### [Linux 内核漏洞可导致 KVM 访客逃逸](http://pwn.ai/) ⭐️ 8.0/10

A Linux kernel flaw \(CVE-2026-99999\) lets KVM guests escape to the host by rewriting IPv4 headers after checksumming, leaking host memory; a fix was merged Oct 14 2026.

telegram · zaihuapd · Oct 18, 09:47

**Tags**: `#Linux kernel`, `#KVM`, `#virtualization security`, `#CVE-2026-99999`, `#guest escape`

---

<a id="item-tech-news-7"></a>
### [Nature Study Finds Microplastics Generate Reactive Free Radicals in Human Body](https://futurism.com/health-medicine/microplastics-research-food-water-consumption-packaging) ⭐️ 8.0/10

New research published in Nature reports that microplastics acquire intrinsic physicochemical activity in water-rich environments such as the human body, generating highly reactive free radicals as their surface area increases upon fragmentation. This challenges the long-held view of plastics as chemically inert and suggests possible biological damage, with implications for health and the food supply chain.

telegram · zaihuapd · Oct 18, 13:55

**「Background」** Plastics have traditionally been regarded as chemically inert, so their presence in drinking water, food, and human tissue was treated mainly as a physical contamination issue rather than a chemical one. Microplastics have previously been detected throughout the human body, meaning people are already widely exposed before questions about their chemical reactivity arise.

**「Impact」** The finding that microplastics generate reactive free radicals in the body shifts the risk assessment from passive particle exposure to active chemical reactivity, implying that current safety standards based on inert-particle assumptions may underestimate health risks such as oxidative stress, inflammation, and potential carcinogenicity. Regulatory agencies and food-packaging industries should prioritize re-evaluating permissible microplastic levels in drinking water and food-contact materials, and invest in detection and mitigation technologies.

<details><summary>References</summary>
<ul>
<li><a href="https://www.smithsonianmag.com/smart-news/microplastics-have-been-linked-with-myriad-human-health-problems-scientists-may-have-finally-figured-out-how-they-harm-the-body-180989694/">Microplastics Have Been Linked With Myriad Human Health Problems.</a></li>
<li><a href="https://www.sciencedirect.com/science/article/pii/S2213343725035031">Microplastics and human health: Exposure pathways, toxicity ...</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12213550/">Microplastics and human health: unraveling the toxicological ...</a></li>

</ul>
</details>

**Tags**: `#microplastics`, `#health`, `#research`

---

<a id="item-tech-news-8"></a>
### [Hybrid Reasoning Agents Introduce Latent‑Space LLM Reasoning with Open Code](https://arxiv.org/abs/2610.18861) ⭐️ 7.5/10

The arXiv paper &quot;Hybrid Reasoning Agents: LLM agents that think in latent space, act through text&quot; \(2026-10-18\) proposes an architecture where a language model maintains a continuous latent reasoning state separate from token‑level text generation. A reference implementation is released in the togethercomputer/HybridAgent GitHub repository and a HuggingFace model collection. The work remains a research prototype; evaluations are shown in Section 5 of the paper, but no large‑scale deployment or independent benchmark results are reported.

hackernews · allinonai · Oct 18, 20:48 · [Discussion](https://news.ycombinator.com/item?id=50145337)

**「Background」** Traditional LLM agents perform reasoning by generating explicit token sequences \(e.g., chain‑of‑thought prompting\), which ties reasoning to the model’s vocabulary and can increase latency and error propagation. Prior work has explored tool use and intermediate thinking, but most approaches still rely on text‑only representations.

**「Impact」** Developers can now download and run the HybridAgent code to experiment with latent‑space reasoning, providing a concrete alternative to token‑only chain‑of‑thought methods for building AI agents.

**「Community Discussion」** Commenters note practical hurdles such as llama.cpp compatibility and looping behavior when running the 14B model, while others speculate about extending the latent‑space idea to link distant models or modalities and express interest in applying the approach to larger models like Qwen 3.8 27B.

**Tags**: `#LLM`, `#AI`, `#agent`, `#reasoning`, `#architecture`

---

<a id="item-tech-news-9"></a>
### [RepRapMicron](https://github.com/VikOlliver/RepRapMicron/wiki) ⭐️ 7.0/10

An open-source project exploring micro-precision self-replicating 3D printers, sparking significant technical discussion on the future of decentralized hardware fabrication and micro-manufacturing.

hackernews · RobotToaster · Oct 18, 13:48 · [Discussion](https://news.ycombinator.com/item?id=50141076)

**Tags**: `#open-source-hardware`, `#3d-printing`, `#microfabrication`, `#hardware`, `#reprap`

---

<a id="item-tech-news-10"></a>
### [Open MicroManipulator Sub-Micrometer 3D Motion Control Platform](https://github.com/0x23/MicroManipulatorStepper) ⭐️ 7.0/10

The Open MicroManipulator project has been published as an open-source sub-micrometer 3D motion control platform on GitHub \(0x23/MicroManipulatorStepper\), offering firmware, mechanical designs, and community-validated builds for precision hardware projects like interferometry and nanopositioning. This low-cost DIY alternative provides accessible sub-micrometer positioning capabilities for hobbyists and researchers who previously relied on expensive commercial systems.

hackernews · \_Microft · Oct 18, 11:16 · [Discussion](https://news.ycombinator.com/item?id=50140001)

**「Project Overview and Context」** Open MicroManipulator is an open-source sub-micrometer 3D motion control platform built with stepper motors, designed as a low-cost DIY alternative to commercial precision positioning systems. The project gained significant attention after being featured on Hacker News via its GitHub repository \(0x23/MicroManipulatorStepper\). Its core value proposition lies in providing precise, affordable 3D motion control for applications such as interferometry and nanopositioning.

**「Sub-Micrometer Positioning Becomes Accessible」** Users can now implement sub-micrometer 3D motion control for applications such as interferometry and nanopositioning using freely available firmware and mechanical designs, eliminating the need for costly commercial positioning equipment.

**「Positive Reception and Practical Uses」** Commenters praise the project as a valuable open-source resource, note its similarity to existing efforts like RepRap Micron, and share personal builds—one user reports constructing it for a point diffraction interferometer while others highlight the availability of a manual, non-motorized variant.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/0x23/MicroManipulatorStepper">GitHub - 0x23/MicroManipulatorStepper: A sub-micrometer 3D ...</a></li>
<li><a href="https://agihunt.info/en/p/1a14f0cd53e08a16381740e909e">Open MicroManipulator: an open-source… · AGI Hunt</a></li>

</ul>
</details>

**Tags**: `#open-source hardware`, `#precision motion control`, `#DIY robotics`, `#sub-micrometer positioning`, `#nanofabrication tools`

---

<a id="item-tech-news-11"></a>
### [Google Research Opens Source Harness² Recursive Agent Framework](https://github.com/google-research/harness2) ⭐️ 7.0/10

Google Research has released Harness² as open source, a recursive optimization framework for LLM agents that improves benchmark scores without retraining the underlying model. The framework applies two layers of recursion and achieved gains of up to 11.5 points on WorkBuddy-Bench. It supports both parallel and sequential recursion modes, ships with integrated benchmarks, and is distributed under the Apache 2.0 license.

telegram · zaihuapd · Oct 18, 11:24

**「Background」** LLM agent systems typically require model retraining or fine-tuning to improve performance, which is costly and resource-intensive. Harness² takes a different approach by optimizing agent behavior through recursive framework-level improvements rather than weight updates, making it complementary to existing agent architectures.

**「Impact」** Developers and researchers can integrate Harness² into existing LLM agent pipelines to improve task performance on benchmarks like WorkBuddy-Bench without the cost and complexity of model retraining, under a permissive Apache 2.0 license.

**Tags**: `#LLM agents`, `#recursive optimization`, `#open source`, `#Google Research`, `#agent frameworks`

---

<a id="item-tech-news-12"></a>
### [MIT Pattie Maes team research on AI-generated content implanting false memories](https://gizmodo.com/ai-generated-content-can-plant-fake-memories-researchers-say-2000826459) ⭐️ 7.0/10

MIT Pattie Maes team research found that participants who saw photos then AI-modified versions were more likely to misremember the originals and confident in errors. Separate studies show AI-generated deepfakes and text can implant false memories of fictional political scandals and reduce voting intent. The research also reports that people can only identify AI-generated content at roughly coin-flip accuracy.

telegram · zaihuapd · Oct 19, 00:16

**「Background」** The cognitive phenomenon of false memory implantation through visual and textual stimuli is established, and the reported research extends it to AI-generated content. Prior work has shown deepfakes and synthetic text can shape perception, but this work demonstrates memory alteration from AI-modified media presented alongside original sources.

**「Impact」** People may form confident false memories from AI-generated media, and the research shows the public can only identify such content at roughly coin-flip accuracy, raising concerns about undetected influence on personal recollection and voting behavior.

**Tags**: `#artificial intelligence`, `#AI safety`, `#deepfake`, `#social impact`, `#cognitive psychology`

---

## Financial News

<a id="item-finance-news-1"></a>
### [One Year After the Food Delivery War, Platforms Profit While Merchants and Riders Struggle](https://www.latepost.com/news/dj_detail?id=3762) ⭐️ 7.0/10

One year after Meituan and Alibaba&\#x27;s intense delivery competition, platform operating profits have recovered as subsidies ended, but the cost has shifted to merchants and riders. Combined daily order volumes across both platforms have stayed 50% above pre-war levels at nearly 140 million, even though sales expenses have returned to normal.

telegram · zaihuapd · Oct 18, 07:40

**「Background」** The year-long subsidy war between the two platforms boosted combined daily orders from 90 million to nearly 140 million, permanently changing consumer delivery habits even after the subsidies stopped.

**「Impact」** Merchants including tea and coffee chains report falling per-store revenue and profit, while Haidilao&\#x27;s 1.6 billion yuan revenue gain included only 9.4 million in net profit. Riders have increased about 50% across both platforms, with per-order pay dropping to 7-8.5 yuan in major cities.

**Tags**: `#food\_delivery`, `#platform\_economics`, `#merchant\_pressures`, `#rider\_conditions`

---

<a id="item-finance-news-2"></a>
### [US AI infrastructure boom shows cracks as projects stall and chip stocks fall](https://www.ft.com/content/9ea5a37d-15c9-4d5b-94d6-719048c9cd3c?syn-25a6b1a6=1) ⭐️ 7.0/10

The Financial Times reports that at least 47 large US data center projects have been delayed, withdrawn, or halted since 2026. Projected US AI infrastructure spending of more than $10 trillion from 2025 to 2032 is being reassessed as markets question whether it will produce returns.

telegram · zaihuapd · Oct 18, 08:52

**「Background」** Rising financing costs, blocked project approvals, and public opposition are constraining construction of data centers—facilities housing computer servers—and analysts estimate only about 35% of planned US projects are highly feasible.

**「Impact」** Nvidia-backed cloud provider CoreWeave fell more than 11% in a day, and the Philadelphia Semiconductor Index fell for an eighth straight session, tying its longest losing streak since 2006.

**Tags**: `#AI infrastructure`, `#data centers`, `#investment risk`, `#technology sector`

---