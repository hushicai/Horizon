---
layout: default
title: "Horizon Summary: 2026-10-28 (EN)"
date: 2026-10-28
lang: en
---

> From 50 items, 24 important content pieces were selected

---

**Technology News**
1. [Anthropic 招聘经理停用编程面试](#item-tech-news-1) ⭐️ 9.0/10
2. [DeepMind announces Genie 4 world-simulation model for video and audio generation](#item-tech-news-2) ⭐️ 8.0/10
3. [Amazon Shuts Down AI Division After Sustained Failure](#item-tech-news-3) ⭐️ 8.0/10
4. [Scalable Self-Distillation with EMA Teacher Using ZeRO-3 and LoRA](#item-tech-news-4) ⭐️ 8.0/10
5. [Microsoft patches high-severity Android Authenticator token theft vulnerability](#item-tech-news-5) ⭐️ 8.0/10
6. [Classification of Finite Simple Groups Formalized in Lean](#item-tech-news-6) ⭐️ 7.5/10
7. [极客湾发布六款旗舰手机芯片能效横评](#item-tech-news-7) ⭐️ 7.5/10
8. [triton-lang/triton released v3.9.0](#item-tech-news-8) ⭐️ 7.0/10
9. [Tailscale SSH Investigation and Remediation Update](#item-tech-news-9) ⭐️ 7.0/10
10. [Survival LLM: Self-hosted emergency AI assistant with local knowledge retrieval](#item-tech-news-10) ⭐️ 7.0/10
11. [Python&\#x27;s experimental JIT to be removed](#item-tech-news-11) ⭐️ 7.0/10
12. [Wikipedia Cleans Up AI-Generated Content Amid Quality Concerns](#item-tech-news-12) ⭐️ 7.0/10
13. [Manual autograd implementation for PyTorch transformer classifier](#item-tech-news-13) ⭐️ 7.0/10
14. [Papers with Code is now open-source \[P\]](#item-tech-news-14) ⭐️ 7.0/10
15. [Ψ-0.6: Adaptive Streams of Thought in a Unified Vision-Language World Model](#item-tech-news-15) ⭐️ 7.0/10
16. [LiquidAI releases LFM3-1.7B, a 1.73B-parameter tri-hybrid model for local agents](#item-tech-news-16) ⭐️ 7.0/10
17. [LFM3-VL-2B Real-time Video Captioning Runs In-browser via WebGPU](#item-tech-news-17) ⭐️ 7.0/10
18. [Developer releases open-source Deepthink agent-swarm test-time scaling framework on GitHub](#item-tech-news-18) ⭐️ 7.0/10
19. [Chinese Team Claims 3.2 Pb/s Real-Time Optical Fiber Record with 24-Core Commercial Hardware](#item-tech-news-19) ⭐️ 7.0/10
20. [广电总局：IPTV 应开机看全屏直播，不得播放开机广告](#item-tech-news-20) ⭐️ 7.0/10
21. [波士顿动力员工联名请愿阻止向 ICE 售机器狗](#item-tech-news-21) ⭐️ 7.0/10
22. [🤖 Anthropic 确认部分内部系统遭研究人员访问，声称客户对话与模型权重未受影响](#item-tech-news-22) ⭐️ 7.0/10
23. [Google Proposes Sleep Framework for LLM Continual Learning](#item-tech-news-23) ⭐️ 7.0/10

**Financial News**
1. [Pop Mart Q3 Revenue Falls 45-50% as Labubu Demand Cools](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Anthropic 招聘经理停用编程面试](https://felixrieseberg.com/hunger-beats-tenure-advice-for-junior-engineers/) ⭐️ 9.0/10

Anthropic stops using coding interviews as Claude AI surpasses human performance, signaling a major shift in hiring and development workflows.

telegram · zaihuapd · Oct 28, 01:46

**Tags**: `#AI hiring`, `#software engineering`, `#paradigm shift`, `#developer tools`

---

<a id="item-tech-news-2"></a>
### [DeepMind announces Genie 4 world-simulation model for video and audio generation](https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/) ⭐️ 8.0/10

DeepMind announced Genie 4, a world-simulation model that generates consistent, photorealistic video and advanced audio from text prompts, including real-time visuals, environmental sound, and interactive dialogue. The system is backed by the Gemini family, with Gemini 3.8 Flash serving as a guiding agent for multi-step tasks, and outputs carry SynthID watermarks. Access begins with a research preview for trusted testers, followed by Project Genie Ultra subscribers and Gemini API and AI Studio partners. Early shared examples show limitations: details can change when objects leave and re-enter the frame, audio instruments may not match prompts, and some photorealistic requests still render like video games.

hackernews · acossta · Oct 27, 16:06 · [Discussion](https://news.ycombinator.com/item?id=50261319)

**「Background」** Genie 4 builds on Google’s earlier Genie series and the Gemini family of models, which already provide real‑time simulation anchors and multimodal reasoning. It follows recent open‑weight world models such as Tencent’s HY‑World 2.0, which demonstrated that multi‑modal world simulation can be built with a four‑stage pipeline for 3D generation. This background makes Genie 4’s claim of photorealistic, consistent video and native audio generation from text understandable.

**「Impact」** Developers and trusted testers in the research preview should verify temporal continuity for objects that exit and re-enter scenes and check generated instruments against prompts, since early user reports indicate consistency and audio mismatches that could affect production use.

**「Community discussion」** Commenters observed that Genie 4 keeps in-frame objects consistent but can alter details when they return, such as a moped rider gaining a helmet or an extra castle appearing in a dragon scene. Others reported audio mismatches, such as a saxophone prompt producing clarinet sound, and a photorealistic peacock-to-cat prompt still rendering like a video game; these are anecdotal examples, not controlled benchmark results.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/">Genie 4: A new generation of world simulation - deepmind.google</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/google-deepmind/introducing-genie-4/">We’re announcing Genie 4, our new world model for real-time ...</a></li>
<li><a href="https://techcrunch.com/2026/10/27/googles-genie-4-world-model-adds-audio-more-realistic-worlds-and-real-time-steering/">Google’s Genie 4 world model adds audio, more realistic ...</a></li>
<li><a href="https://github.com/Tencent-Hunyuan/HY-World-2.0">GitHub - Tencent-Hunyuan/HY-World-2.0: HY-World 2.0: A Multi ...</a></li>
<li><a href="https://hyworld.dev/">HY World Model 2 - AI 3D World Generator｜HY World 2 / HY-World 2...</a></li>
<li><a href="https://huggingface.co/tencent/HY-World-2.0">tencent/HY-World-2.0 · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#Genie 4`, `#World Simulation`, `#Video Generation`, `#AI Research`, `#Tencent HY-World`

---

<a id="item-tech-news-3"></a>
### [Amazon Shuts Down AI Division After Sustained Failure](https://futurism.com/artificial-intelligence/amazon-ai-division-failure-nova) ⭐️ 8.0/10

Amazon is dissolving its dedicated AI division after years of struggling to produce competitive artificial intelligence products, according to a report by Futurism. The move reflects broader challenges faced by large technology companies in building in-house AI capabilities, particularly when competing against well-funded research labs and open-source initiatives. While Amazon has previously emphasized its commitment to AI through projects like Alexa and AWS AI services, internal efforts reportedly failed to meet performance benchmarks or market expectations. The decision underscores a strategic shift toward relying on third-party models rather than developing proprietary systems.

hackernews · dpflan · Oct 27, 16:25 · [Discussion](https://news.ycombinator.com/item?id=50261589)

**「Background」** Amazon&\#x27;s AI division was created as part of a broader &quot;pivot to AI&quot; strategy that consolidated device and research teams under a unified AI effort, but internal comments indicate the initiative suffered from scattered focus, insufficient investment, and limited innovation, setting the stage for its current dismantling.

**「Community Reactions Highlight Cultural and Strategic Concerns」** Commenters on Hacker News expressed little surprise at the outcome, with one former employee noting that senior staff were laid off a year ago as part of an &\#x27;AI pivot&\#x27; strategy. Several users criticized Amazon&\#x27;s corporate culture for lacking the innovation-friendly environment needed for cutting-edge AI research, while others suggested the company may now focus on hosting third-party models for profit rather than investing in internal development.

**Tags**: `#Artificial Intelligence`, `#Cloud Computing`, `#Corporate Strategy`, `#AI Research`, `#Software Engineering`

---

<a id="item-tech-news-4"></a>
### [Scalable Self-Distillation with EMA Teacher Using ZeRO-3 and LoRA](https://www.reddit.com/r/MachineLearning/comments/1xh083s/selfdistillation_with_an_ema_teacher_at_scale/) ⭐️ 8.0/10

A new open‑source repository implements scalable self‑distillation with an Exponential Moving Average \(EMA\) teacher by combining DeepSpeed’s ZeRO‑3 optimizer with LoRA adapters. The solution shares a frozen backbone model and maintains two lightweight LoRA adapters—one for the student \(trained\) and one for the teacher \(EMA of the student adapter\)—with adapter switching to reduce memory and latency. It includes fixes for TRL and ZeRO‑3, robust SDFT implementation, EMA teacher checkpoint saving/resuming, and DeepSpeed configs that mitigate memory spikes. The repo has been tested on Qwen3.5 and ToolAlpaca and is available for plug‑and‑play use.

reddit · r/MachineLearning · /u/ifaposto · Oct 27, 18:16

**「Background」** Self‑distillation typically uses an EMA teacher to provide stable targets, but scaling this to large models is limited by the memory and communication overhead of holding both a full teacher and student on GPU. LoRA \(Low‑Rank Adaptation\) enables training only lightweight adapters while keeping the base model frozen, allowing the same backbone to serve both student and teacher. The new implementation leverages LoRA under DeepSpeed’s ZeRO‑3 and the TRL framework to make self‑distillation scalable for large models.

**「Impact」** Developers can now train large models with self‑distillation using only two LoRA adapters and ZeRO‑3 optimizations, dramatically lowering GPU memory usage and training latency compared to full‑model teacher approaches. The ability to save and resume EMA teacher checkpoints also improves experiment reproducibility and reduces training time for future iterations.

**Tags**: `#MachineLearning`, `#SelfDistillation`, `#ZeRO-3`, `#LoRA`, `#OpenSource`

---

<a id="item-tech-news-5"></a>
### [Microsoft patches high-severity Android Authenticator token theft vulnerability](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2026-80097) ⭐️ 8.0/10

Microsoft released an update for the Android version of Microsoft Authenticator that addresses CVE-2026-80097, a high‑severity vulnerability allowing malicious apps already installed on a device to obtain work account authentication tokens without requesting Android permissions. The fix is included in version 6.2606.4246, which is now available for users. Researchers said the exploit requires no further user interaction, while Microsoft notes that an attacker would still need to trick the user into completing an authentication flow. The company reported no evidence of the vulnerability being exploited in the wild.

telegram · zaihuapd · Oct 27, 12:04

**「Microsoft Authenticator Android broker component」** Microsoft Authenticator for Android operates as an account broker that stores work-account access tokens and supplies them to other apps on the device, so a flaw in its authentication logic can expose those tokens to any installed app without new permissions. Microsoft and researchers tracked the issue as CVE-2026-80097 \(CVSS 8.6\), classifying it as improper authentication in the broker component and a local elevation-of-privilege vulnerability. The exposed tokens could provide access to an account&\#x27;s email, files, and calendar data.

**「Impact」** Organizations using Microsoft Authenticator on Android must update to version 6.2606.4246 to close the token‑theft gap, as unpatched devices remain exposed to malicious apps that can harvest work account credentials without user consent.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/microsoft-authenticator-flaw-let.html">Microsoft Authenticator Flaw Let Permissionless Android Apps ...</a></li>
<li><a href="https://cybersecuritynews.com/microsoft-authenticator-flaw/">Microsoft Authenticator Flaw Lets Malicious Android Apps ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#Microsoft`, `#Android`, `#authentication`

---

<a id="item-tech-news-6"></a>
### [Classification of Finite Simple Groups Formalized in Lean](https://cfsg.axiommath.ai/) ⭐️ 7.5/10

Formalization of the Classification of Finite Simple Groups in Lean, creating a reusable library for mathematical proofs.

hackernews · pfdietz · Oct 27, 16:29 · [Discussion](https://news.ycombinator.com/item?id=50261647)

**Tags**: `#mathematical-formalization`, `#proof-assistant`, `#formal-verification`, `#computer-science`

---

<a id="item-tech-news-7"></a>
### [极客湾发布六款旗舰手机芯片能效横评](https://www.bilibili.com/video/BV1kMxM6FECM/) ⭐️ 7.5/10

A benchmark comparison of six flagship smartphone chipsets&\#x27; energy efficiency, relevant for mobile AI/ML optimization and hardware performance.

telegram · zaihuapd · Oct 27, 10:53

**Tags**: `#energy efficiency`, `#mobile chips`, `#AI on-device`, `#benchmark`, `#smartphone hardware`

---

<a id="item-tech-news-8"></a>
### [triton-lang/triton released v3.9.0](https://github.com/triton-lang/triton/releases/tag/v3.9.0) ⭐️ 7.0/10

Triton v3.9.0 introduces atomic load and store operations with proper memory ordering, broadening support for concurrent GPU kernel development.

github · warrendeng · Oct 27, 18:56

**Tags**: `#triton`, `#gpu-kernels`, `#atomic-operations`, `#parallel-programming`

---

<a id="item-tech-news-9"></a>
### [Tailscale SSH Investigation and Remediation Update](https://tailscale.com/ssh-investigation-update) ⭐️ 7.0/10

Tailscale issued an investigation and remediation update for SSH vulnerabilities that affect nodes with specific ACL configurations permitting \`tailscale ssh\` access. The update addresses conditions related to unrestricted node access paths but does not alter the fundamental ACL framework.

hackernews · figmert · Oct 27, 19:55 · [Discussion](https://news.ycombinator.com/item?id=50264857)

**「Background」** Tailscale SSH enables remote command execution into Tailnet nodes, with access governed by Access Control Lists that specify permitted users and connection paths, forming the infrastructure underlying the recent vulnerability investigation.

**「Impact」** Users who configured Tailscale SSH ACLs to permit node access without corresponding sudoers/root restrictions may be impacted by the described vulnerabilities, whereas users without such configurations are unaffected, as noted in the investigation update and community analysis.

**「Community Discussion」** Several commenters noted that the exploits only activate when ACLs allow \`tailscale ssh\` without sudoers/root paths. Multiple users recommended relying on stock OpenSSH or disabling Tailscale SSH to minimize attack surface.

**Tags**: `#tailscale`, `#ssh`, `#security`, `#vulnerability`, `#infrastructure`

---

<a id="item-tech-news-10"></a>
### [Survival LLM: Self-hosted emergency AI assistant with local knowledge retrieval](https://www.brangus.io/survival-llm) ⭐️ 7.0/10

The Survival LLM is a self-hosted AI assistant that runs locally on a user&\#x27;s computer with curated knowledge bases for emergency preparedness. It uses search-based retrieval to mitigate hallucination rather than pure generation, providing practical answers for survival scenarios. The project is available as a standalone application for offline use.

hackernews · Luc · Oct 27, 19:55 · [Discussion](https://news.ycombinator.com/item?id=50264853)

**「Background on emergency AI assistants」** The prerequisite concept is the use of LLMs as search tools for offline knowledge retrieval, particularly in emergency preparedness contexts where connectivity may be limited. This builds on the broader trend of self-hosted AI systems that prioritize privacy and local control. The project specifically addresses the need for practical, actionable advice in survival scenarios.

**「Impact on emergency preparedness users」** For emergency preparedness users, the main consequence is the ability to run an AI assistant offline with reduced hallucination risk through search-based retrieval, though they must ensure their curated knowledge bases are accurate and up-to-date. The project helps mitigate the risks of pure generative models in critical safety situations.

**「Community discussion on LLM hallucination」** The most useful argument comes from \[x3haloed\], who advocates using LLMs as search technology \(string match → semantic search → search intelligence\) for emergency scenarios, emphasizing that semantics alone cannot provide actionable safety advice without retrieval. Other comments note the project&\#x27;s value for offline work but caution about the need for well-curated knowledge bases.

**Tags**: `#self-hosted AI`, `#offline knowledge retrieval`, `#emergency preparedness`, `#LLM hallucination`

---

<a id="item-tech-news-11"></a>
### [Python&\#x27;s experimental JIT to be removed](https://lwn.net/SubscriberLink/1102102/0c00e4d550f25f8c/) ⭐️ 7.0/10

Python&\#x27;s experimental JIT compiler is being removed from CPython after failing to satisfy the requirements of a newly requested PEP. The JIT had incorporated advanced optimizations including automatic refcount operation removal, type-based specializations, and inplace math operations. Its removal is a setback for Python&\#x27;s free threading efforts, as the JIT was expected to help offset the performance penalties of free threading. The decision indicates the JIT was not ready for production use.

hackernews · f311a · Oct 27, 11:17 · [Discussion](https://news.ycombinator.com/item?id=50257419)

**「Python&\#x27;s experimental JIT compiler removed from CPython」** Python&\#x27;s experimental just-in-time \(JIT\) compiler, merged into CPython&\#x27;s main development branch in 2024 for Python 3.13 without a formal accepted PEP, is being removed after failing to meet requirements for a new PEP request. The removal is tied to the language&\#x27;s performance roadmap and the free-threading effort, where the JIT was seen as a potential counter to the performance penalty introduced by GIL removal.

**「Impact」** The removal forces developers who were experimenting with the JIT to abandon it as a performance optimization path, potentially slowing the adoption of free-threaded Python in performance-critical applications.

**「Community Discussion」** The community discussion reveals a mix of disappointment and pragmatic acceptance, with users like adrian17 lamenting the loss of a potential solution for free threading penalties, while others like xx\_ns emphasize that the PEP process ensures Python&\#x27;s stability. Alternative performance strategies were proposed, including rich\_sasha&\#x27;s inline Cython decorator and PathOfEclipse&\#x27;s comparison to Ruby and JavaScript JITs, suggesting funding and incentive differences may play a role.

<details><summary>References</summary>
<ul>
<li><a href="https://peps.python.org/pep-0744/">PEP 744 – JIT Compilation | peps.python.org</a></li>
<li><a href="https://blog.imseankim.com/python-3-14-free-threading-jit-compiler-gil-removal-2026/">Python 3.14 Free-Threading and Experimental JIT: How Python ...</a></li>
<li><a href="https://daily.dev/posts/python-s-experimental-jit-to-be-removed-2qgwrdoly">Python&#x27;s experimental JIT to be removed - daily.dev</a></li>

</ul>
</details>

**Tags**: `#Python`, `#JIT`, `#performance`, `#programming-languages`, `#software-engineering`

---

<a id="item-tech-news-12"></a>
### [Wikipedia Cleans Up AI-Generated Content Amid Quality Concerns](https://spectrum.ieee.org/wikipedia-wikiproject-ai-writing-cleanup) ⭐️ 7.0/10

Wikipedia is conducting a cleanup of AI-generated content, as reported by IEEE Spectrum, amid growing platform efforts to maintain knowledge quality. The initiative reflects broader concerns about low-quality AI contributions, including broken formatting and fabricated text. Community members report mixed experiences, with some human edits being reverted by Wikipedia&\#x27;s own AI moderation tools.

hackernews · rbanffy · Oct 27, 11:08 · [Discussion](https://news.ycombinator.com/item?id=50257326)

**「Wikipedia&\#x27;s AI Cleanup Initiative」** Wikipedia operates a WikiProject AI Cleanup that tracks and removes AI‑generated text and images, a response to the surge of machine‑written contributions since 2023. The effort, documented in an October 2026 article by Eliza Strickland, includes automated bots and manual review to preserve human‑written quality. Recent community debate reflects a shift from viewing AI solely as content to be cleaned toward using AI tools to assist editors.

**「Impact」** The cleanup highlights the difficulty of distinguishing helpful AI assistance from harmful generated content, potentially affecting volunteer editors who encounter automated reversions of legitimate corrections.

**「Community Discussion」** Commenters note that Wikipedia&\#x27;s AI bot sometimes reverts human attempts to fix AI-generated errors, while others observe that school outreach programs may inadvertently encourage low-effort AI contributions. A quoted perspective describes AI&\#x27;s role evolving from cleanup target to cleanup tool to ubiquitous infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup">Wikipedia : WikiProject AI Cleanup - Wikipedia</a></li>
<li><a href="https://tildes.net/~tech/1wkw/how_wikipedias_editors_keep_the_online_encyclopedia_human_written">How Wikipedia ’s editors keep the online encyclopedia human- written ...</a></li>

</ul>
</details>

**Tags**: `#Wikipedia`, `#AI-generated content`, `#content moderation`, `#knowledge quality`

---

<a id="item-tech-news-13"></a>
### [Manual autograd implementation for PyTorch transformer classifier](https://www.reddit.com/r/MachineLearning/comments/1xh1z1p/understanding_transformer_autograd_by_building_it/) ⭐️ 7.0/10

The author published a minimal, self-contained PyTorch implementation of manual autograd for a transformer-based classifier. The accompanying GitHub repository and Colab notebook enable hands-on inspection of gradient flow through attention blocks and custom backward passes. The resource serves as a reference for developers seeking low-level differentiation intuition without external claims of performance or benchmark results.

reddit · r/MachineLearning · /u/ifaposto · Oct 27, 19:20

**「Background」** PyTorch&\#x27;s autograd engine automatically computes gradients for tensor operations, but understanding its internal mechanics is essential for debugging custom layers and optimizing transformer models. The repository provides a minimal transformer classifier where every forward step uses custom \`torch.autograd.Function\` subclasses with hand-derived backward passes, making the gradient flow through attention blocks explicit and inspectable. This approach is commonly used in research and education to build intuition for low-level differentiation before relying on framework automation.

**「Impact」** Developers can use the provided GitHub repo and Colab notebook to experiment with custom transformer backward passes, lowering the barrier to understanding autograd flow in transformer models.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ifiaposto/transformer_custom_autograd">GitHub - ifiaposto/transformer_custom_autograd: A minimal ...</a></li>
<li><a href="https://github.com/ifiaposto/transformer_custom_autograd/tree/main">GitHub - ifiaposto/transformer_custom_autograd: A minimal ...</a></li>

</ul>
</details>

**Tags**: `#PyTorch`, `#Transformers`, `#Autograd`, `#Deep Learning`, `#Tutorial`

---

<a id="item-tech-news-14"></a>
### [Papers with Code is now open-source \[P\]](https://www.reddit.com/r/MachineLearning/comments/1xgoadu/papers_with_code_is_now_opensource_p/) ⭐️ 7.0/10

A community-driven, open-source revival of Papers with Code for tracking trending AI research and benchmarks, now available for public contribution.

reddit · r/MachineLearning · /u/NielsRogge · Oct 27, 09:54

**Tags**: `#open-source`, `#machine-learning`, `#research-tools`, `#fastapi`, `#react`

---

<a id="item-tech-news-15"></a>
### [Ψ-0.6: Adaptive Streams of Thought in a Unified Vision-Language World Model](https://www.reddit.com/r/MachineLearning/comments/1xgwq9u/%CF%8806_adaptive_streams_of_thought_in_a_unified/) ⭐️ 7.0/10

Ψ-0.6 is an open-source unified vision-language world model that adaptively reasons across text, depth, motion, camera pose, and imagined scenes, learning which representation to use via reinforcement learning. The paper reports zero-shot spatial reasoning gains on MindCube and outperforms other world models on FlowBench object-motion prediction, with sim-to-real transfer to real robot tabletops. The model functions as perceiver, VLM, world model, reasoner, and policy in a single architecture, and the authors have released code, a paper, and a demo alongside the announcement.

reddit · r/MachineLearning · /u/FaeriaManic · Oct 27, 16:09 · [Discussion](https://www.reddit.com/r/MachineLearning/comments/1xgwq9u/%CF%8806_adaptive_streams_of_thought_in_a_unified/)

**「Background」** Chain-of-thought reasoning transformed AI reasoning but remains confined to words, while capabilities such as perception, language, geometry, and simulation are typically separated across specialized models, limiting how they can be composed and jointly adapted to a task. This fragmentation motivates efforts to unify these modalities into a single model that can flexibly combine different forms of inference as a problem unfolds. Ψ-0.6 is positioned as such a unified vision-language world model that adaptively composes interleaved reasoning streams across text, depth, motion, camera pose, and imagined scenes.

**「Impact」** By unifying perception, reasoning, and policy under one model that adapts its stream of thought across modalities, Ψ-0.6 offers a concrete path toward embodied AI systems that reason about the physical world without separate pipelines for each capability. Its reported sim-to-real transfer suggests that training in simulation may be sufficient for real-world robot control, potentially reducing the cost and complexity of deploying robot policies. The open-source release enables other researchers to build on and verify these claims.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2610.32177">[2610.32177] ||Psi;$-0.6: Adaptive Streams of Thought in a ...</a></li>
<li><a href="https://github.com/awwkl/psi-0.6">Ψ-0.6: Adaptive Streams of Thought - GitHub</a></li>

</ul>
</details>

**Tags**: `#AI/ML`, `#vision-language models`, `#world models`, `#robotics`, `#open source`

---

<a id="item-tech-news-16"></a>
### [LiquidAI releases LFM3-1.7B, a 1.73B-parameter tri-hybrid model for local agents](https://www.reddit.com/r/LocalLLaMA/comments/1xgy8s3/liquidailfm317b_hugging_face/) ⭐️ 7.0/10

LiquidAI has released LFM3-1.7B, a 1.73B-parameter text-only language model built on a new tri-hybrid architecture comprising 24 layers: 13 gated short convolutions, 5 sliding-window attention, and 6 global attention. The model supports a 256K-token context window and runs at roughly 1 GB of memory at 4-bit precision, making it usable on phones and laptops. It has been post-trained for agentic harnesses including Hermes Agent, Pi, and OpenClaw, with support for tool calling and structured outputs. The model is licensed under LFM Open License v1.0 and is available on Hugging Face as a GGUF checkpoint, with llama.cpp support already merged.

reddit · r/LocalLLaMA · /u/jacek2023 · Oct 27, 17:04

**「Background」** The LFM3 family spans base, text, vision, audio, omni, and decision models, all built around LiquidAI&\#x27;s tri-hybrid architecture. LFM3-1.7B-Base, the pre-trained checkpoint behind the post-trained model, was trained on 22T tokens, with the final 3.5T tokens curated with agentic traces and tool calls to extend the context window to 256K. This release follows earlier LFM2.5-Audio and marks LiquidAI&\#x27;s push into on-device, edge-capable models across multiple modalities.

**「Impact」** For local and edge AI developers, LFM3-1.7B provides a lightweight, ~1 GB model suitable for tool calling, structured outputs, and domain-specific fine-tuning on a single GPU. However, the vendor explicitly states it is not recommended for agentic coding or complex multi-step reasoning due to its small size, which sets a clear boundary on where it can and cannot be used effectively.

**「Community Discussion」** No community comments were available on the source post, so no substantive discussion can be summarized.

**Tags**: `#llm`, `#edge-computing`, `#open-source`, `#architecture`

---

<a id="item-tech-news-17"></a>
### [LFM3-VL-2B Real-time Video Captioning Runs In-browser via WebGPU](https://www.reddit.com/r/LocalLLaMA/comments/1xh0otf/realtime_video_captioning_with_lfm3vl2b_running/) ⭐️ 7.0/10

A demo released on Hugging Face shows LFM3-VL-2B performing real-time video captioning entirely in the browser using WebGPU. The 2‑billion‑parameter vision‑language model runs locally on the client, eliminating the need for remote inference servers and preserving user privacy. This capability lets developers integrate multimodal AI features into web applications with low latency and no data upload.

reddit · r/LocalLLaMA · /u/xenovatech · Oct 27, 18:33

**「Background」** LFM3-VL-2B is part of Liquid AI&\#x27;s open-weight LFM3 family of 2B-class models built to run fast on any device across text, vision, audio, and other modalities. The vision model pairs an LFM language backbone with a SigLIP2 NaFlex image encoder for fast multimodal inference on-device. LFM3-VL-2B starts from LFM3-1.7B-Base, which was pre-trained in two stages on 22 trillion tokens in total.

**「Impact」** Developers can now build privacy‑preserving, real‑time captioning tools that run entirely client‑side, reducing latency and eliminating server costs.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/LiquidAI/LFM3-VL-2B">LiquidAI/LFM3-VL-2B · Hugging Face</a></li>
<li><a href="https://docs.liquid.ai/lfm/models/vision-models">Vision Models - Liquid Docs</a></li>
<li><a href="https://www.liquid.ai/blog/lfm3">Introducing LFM3: Every Modality for Specialized Intelligence</a></li>

</ul>
</details>

**Tags**: `#WebGPU`, `#local-inference`, `#vision-language-models`, `#browser-ai`, `#multimodal`

---

<a id="item-tech-news-18"></a>
### [Developer releases open-source Deepthink agent-swarm test-time scaling framework on GitHub](https://www.reddit.com/r/LocalLLaMA/comments/1xh4bnd/openais_major_results_over_the_last_3_months_came/) ⭐️ 7.0/10

A developer posting as /u/Ryoiki-Tokuiten has released Deepthink, an open-source GitHub repository that implements test-time compute scaling using agent swarms for smaller LLMs. The poster reports scores rising from 14% to 65% on 15 BrokenArxiv \(Matharena\) problems and from 9% to 52% on 8 DeepSWE problems on Gemma4-35B and Qwen-3.8-27B, using about 200M tokens per problem. Each run takes 50 minutes to 30 hours depending on depth and inference speed. The gains are self-reported, have not been tested on frontier or large open models because of cost, and are not independently verified.

reddit · r/LocalLLaMA · /u/Ryoiki-Tokuiten · Oct 27, 20:47

**「Background」** Test-time scaling refers to increasing compute during inference—rather than during training—to improve model performance, often by having multiple LLM agents collaborate iteratively on a problem. The Reddit post references two benchmarks: BrokenArxiv, a MathArena track that evaluates models on uncontaminated mathematics problems and reports the percentage answered correctly, and DeepSWE, a software-engineering benchmark. The author claims OpenAI&\#x27;s recent major results came from this same agent-swarm approach, though the open-source implementation has only been tested on smaller models \(Gemma 4 35B and Qwen 3.8 27B\) due to cost.

**「Impact」** Developers can experiment with the framework on Gemma4-35B or Qwen-3.8-27B-class models through the GitHub repo, but should budget 50 minutes to 30 hours per problem and treat the large benchmark improvements as unverified self-reported results not yet shown on larger or frontier models.

<details><summary>References</summary>
<ul>
<li><a href="https://matharena.ai/brokenarxiv/">BrokenArXiv - MathArena.ai</a></li>
<li><a href="https://atlas.kevinhu.io/benchmarks/brokenarxiv-02-2026-matharena">BrokenArXiv 02/2026 leaderboard — Benchmark Atlas</a></li>

</ul>
</details>

**Tags**: `#test-time scaling`, `#agent swarms`, `#open-source AI`, `#benchmark evaluation`, `#LLM inference`

---

<a id="item-tech-news-19"></a>
### [Chinese Team Claims 3.2 Pb/s Real-Time Optical Fiber Record with 24-Core Commercial Hardware](https://www.tomshardware.com/networking/3-2-pb-s-real-time-optical-fiber-transfer-speed-world-record-claimed-by-chinese-team-speed-fast-enough-to-download-more-than-20-000-4k-movies-in-one-second) ⭐️ 7.0/10

A Chinese research team has claimed a new real-time optical fiber transmission record of 3.2 petabits per second \(Pb/s\) using a 24-core commercial-compatible fiber architecture. The demonstration employs spatial division multiplexing combined with S+C+L multi-band transmission technology, surpassing the same team&\#x27;s previous 2.5 Pb/s record by nearly 30%. While laboratory records have reached 5.29 Pb/s using experimental equipment, this result is notable for using hardware compatible with commercial deployment pathways.

telegram · zaihuapd · Oct 27, 03:45

**「Chinese team sets 3.2 Pb/s real‑time optical‑fiber record」** Chinese researchers reported a real‑time optical‑fiber transmission speed of 3.2 Pb/s over a 10.3 km link using a 24‑core commercial‑compatible fiber. The achievement relied on spatial‑division multiplexing and S+C+L multi‑band transmission technology, as confirmed by the Tom’s Hardware report.

**「Impact」** The use of commercial-compatible 24-core fiber and multi-band transmission represents a practical step toward deploying ultra-high-capacity backbone networks, potentially reducing the cost and complexity barrier for next-generation internet infrastructure upgrades.

<details><summary>References</summary>
<ul>
<li><a href="https://www.notebookcheck.net/China-claims-3-2-Pb-s-optical-fiber-record-could-send-20-000-4K-movies-per-second.1434319.0.html">China claims 3 . 2 Pb / s optical fiber record... - Notebookcheck News</a></li>
<li><a href="https://www.tomshardware.com/networking/3-2-pb-s-real-time-optical-fiber-transfer-speed-world-record-claimed-by-chinese-team-speed-fast-enough-to-download-more-than-20-000-4k-movies-in-one-second">3 . 2 Petabits per second real - time optical fiber ... | Tom&#x27; s Hardware</a></li>

</ul>
</details>

**Tags**: `#optical-fiber`, `#telecommunications`, `#high-speed-networking`, `#spatial-division-multiplexing`, `#network-infrastructure`

---

<a id="item-tech-news-20"></a>
### [广电总局：IPTV 应开机看全屏直播，不得播放开机广告](https://www.nrta.gov.cn/art/2026/10/27/art_1588_74296.html) ⭐️ 7.0/10

China&\#x27;s broadcasting regulator mandates that IPTV and smart TVs boot directly to live TV without ads, forcing significant software and hardware UX updates across the consumer electronics industry.

telegram · zaihuapd · Oct 27, 05:59

**Tags**: `#IPTV`, `#Smart TV`, `#Regulation`, `#User Experience`, `#Technology Industry`

---

<a id="item-tech-news-21"></a>
### [波士顿动力员工联名请愿阻止向 ICE 售机器狗](https://arstechnica.com/ai/2026/10/boston-dynamics-employees-want-to-block-sale-of-robot-dogs-to-ice/) ⭐️ 7.0/10

Over 300 Boston Dynamics employees petitioned leadership to cancel a $1.3M DHS contract supplying four modified Spot robots to ICE for detection tasks, citing ethical concerns; management declined, stating the robots would not be weaponized.

telegram · zaihuapd · Oct 27, 09:52

**Tags**: `#robotics`, `#tech ethics`, `#employee activism`, `#government contracts`, `#Boston Dynamics`

---

<a id="item-tech-news-22"></a>
### [🤖 Anthropic 确认部分内部系统遭研究人员访问，声称客户对话与模型权重未受影响](https://www.washingtonpost.com/technology/2026/10/26/researchers-cybersecurity-start-up-cathedral-got-inside-anthropic/) ⭐️ 7.0/10

Security researchers from Cathedral accessed parts of Anthropic&\#x27;s internal systems through a third-party software vulnerability, exposing some sensitive data but not customer conversations or model weights.

telegram · zaihuapd · Oct 27, 12:43

**Tags**: `#AI security`, `#Anthropic`, `#cybersecurity`, `#data breach`, `#responsible disclosure`

---

<a id="item-tech-news-23"></a>
### [Google Proposes Sleep Framework for LLM Continual Learning](https://research.google/blog/the-sleep-framework-a-new-way-for-llms-to-retain-knowledge-in-continual-learning/) ⭐️ 7.0/10

Google Research introduces a &quot;Sleep Framework&quot; that adds an offline consolidation phase to large language models, enabling them to convert short-term context into long-term parameter updates during continual learning. The framework alternates between active interaction and offline sleep cycles, and is reported to outperform GPT-4 and supervised fine-tuning baselines on 10-million-token long-context, continual translation, and mathematical reasoning tasks.

telegram · zaihuapd · Oct 28, 01:46

**「Background」** In continual learning, large language models often suffer catastrophic forgetting, losing previously learned knowledge when acquiring new data. Researchers have explored offline consolidation and replay mechanisms to mitigate this issue. Google&\#x27;s sleep framework introduces a dedicated offline &quot;sleep&quot; phase after active interaction, simulating biological sleep to consolidate short‑term context into long‑term parameters and reduce forgetting.

**「Impact」** If validated, this approach could let developers deploy LLMs that continuously acquire new knowledge without full retraining, reducing compute costs and avoiding catastrophic forgetting in production systems that require ongoing adaptation.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ai-digest-1.com/news/google-research-unveils-sleep-framework-for-continual-learning-in-llms-19815">Google Research Unveils Sleep Framework for Continual ...</a></li>
<li><a href="https://todayforai.com/en/story/story-ac73a1ee-65e">Google Research Introduces &#x27;Sleep Phase&#x27; Framework to Fix LLM ...</a></li>
<li><a href="https://research.google/blog/">Latest News from Google Research Blog - Google Research</a></li>

</ul>
</details>

**Tags**: `#continual learning`, `#catastrophic forgetting`, `#large language models`, `#Google Research`, `#sleep framework`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Pop Mart Q3 Revenue Falls 45-50% as Labubu Demand Cools](https://asia.nikkei.com/business/consumer/pop-mart-s-revenue-halves-in-q3-as-labubu-craze-cools) ⭐️ 7.0/10

Pop Mart reported a 45-50% year-over-year revenue decline in Q3 2026, with the steepest drops in the US \(down 70-75%\), Asia-Pacific ex-China \(down 65-70%\), and Europe \(down 50-55%\), as the Labubu collectible craze faded. The company said October trends are stabilizing and full-year China growth &quot;should not be difficult,&quot; but warned H2 gross margin may narrow by up to 2 percentage points versus H1 due to a lower share of high-margin overseas sales.

telegram · zaihuapd · Oct 27, 14:30

**「Background」** Pop Mart, a Hong Kong-listed Chinese collectible toy maker, saw explosive growth in 2024-2025 driven by the Labubu character, which became a viral sensation across Asia and Western markets, lifting overseas sales to a high-margin contributor.

**「Impact」** Investors face a sharp earnings reset as the company&\#x27;s highest-margin overseas segment contracts, while the China business shows resilience with only a 5-10% offline decline, shifting the growth and margin profile toward the lower-margin domestic market.

**Tags**: `#earnings`, `#consumer goods`, `#asia markets`, `#collectibles`

---