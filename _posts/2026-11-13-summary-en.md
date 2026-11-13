---
layout: default
title: "Horizon Summary: 2026-11-13 (EN)"
date: 2026-11-13
lang: en
---

> From 44 items, 22 important content pieces were selected

---

**Technology News**
1. [Rust 1.100 stabilizes never type, custom allocators, and dependency cooldowns](#item-tech-news-1) ⭐️ 9.0/10
2. [PostgreSQL Type Confusion Escalated to Remote Code Execution \(CVE-2026-6460\)](#item-tech-news-2) ⭐️ 8.0/10
3. [Project reports 16B LLM inference on sub-1GB devices](#item-tech-news-3) ⭐️ 8.0/10
4. [Anthropic files for proposed Nasdaq IPO under ticker ANT](#item-tech-news-4) ⭐️ 8.0/10
5. [UMAP 0.6 released with faster nearest-neighbor search, new initialization, and opt-in optimizers](#item-tech-news-5) ⭐️ 8.0/10
6. [US Commerce finalizing rule to block Chinese AI firms&\#x27; remote chip access](#item-tech-news-6) ⭐️ 8.0/10
7. [👁️ 突发: 黄仁勋辞任英伟达 CEO，CFO 克雷斯任临时 CEO](#item-tech-news-7) ⭐️ 8.0/10
8. [tamserve open-source video tracker shares model weights across cameras, cuts RTX 4090 costs 2x](#item-tech-news-8) ⭐️ 7.5/10
9. [Gemini 4 Hydrogen and Orchestrator](#item-tech-news-9) ⭐️ 7.0/10
10. [Microsoft 365 outage disrupts Outlook and Exchange Online email](#item-tech-news-10) ⭐️ 7.0/10
11. [Talking Zen 6 with Mike Clark at AMD In-Depth](#item-tech-news-11) ⭐️ 7.0/10
12. [NVIDIA&\#x27;s exposure to export controls and supply chain risks](#item-tech-news-12) ⭐️ 7.0/10
13. [Independent audit questions TRIBE v2 topographic maps](#item-tech-news-13) ⭐️ 7.0/10
14. [知情人士：「腾讯裁员 50%」系谣言误读](#item-tech-news-14) ⭐️ 7.0/10
15. [Japan to Impose Security Obligations on AI Practitioners](#item-tech-news-15) ⭐️ 7.0/10
16. [Apple details Secure Exclaves audio/video isolation and recording-indicator checks](#item-tech-news-16) ⭐️ 7.0/10
17. [Samsung patents UWB radar + BIA for Galaxy Watch visceral fat measurement](#item-tech-news-17) ⭐️ 7.0/10
18. [Telegram Widgets RCE Vulnerability in Bot API 10.4](#item-tech-news-18) ⭐️ 7.0/10
19. [Google releases Gemini 4 Hydrogen model for fast coding and agent workflows](#item-tech-news-19) ⭐️ 7.0/10
20. [研究称六款中国 AI 模型留下 Blackwell 芯片指纹](#item-tech-news-20) ⭐️ 7.0/10

**Financial News**
1. [Oil prices rise after Trump comments on Iran](#item-finance-news-1) ⭐️ 7.0/10
2. [Eli Lilly&\#x27;s oral weight-loss drug approved in China](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Rust 1.100 stabilizes never type, custom allocators, and dependency cooldowns](https://blog.rust-lang.org/2026/11/12/Rust-1.100.0/) ⭐️ 9.0/10

Rust 1.100, released on November 12, 2026, stabilizes the never type \(\`\!\`\), custom allocators, and Cargo dependency cooldowns based on minimum publish age \(RFC 3923\). Cargo now warns by default about unused dependencies through \`cargo::unused\_dependencies\`, and \`cargo install\` uses the lockfile bundled in \`.crate\` tarballs by default, making \`--locked\` a no-op. Commenters also identified additional stabilized standard-library APIs, including \`bool::toggle\(\)\` and \`Box::map\(\)\`, that were not highlighted in the release post.

hackernews · mbStavola · Nov 12, 18:39 · [Discussion](https://news.ycombinator.com/item?id=50472038)

**「Background」** The never type represents computations that never produce a value, such as a function that always panics or loops forever, and custom allocators allow a program to replace its default memory allocation strategy. Both were previously unstable or nightly-only features, so this release makes them available in stable Rust without opt-in feature flags. Dependency cooldowns introduce a configurable minimum age for crate versions considered by the resolver unless already present in \`Cargo.lock\`.

**「Impact」** Existing Cargo projects will start seeing \`warning: unused dependency\` diagnostics by default, as shown for \`tracing-subscriber\`, which may require updates to \`Cargo.toml\` to silence or remove flagged crates. Projects that enable dependency cooldowns will have resolvers ignore newly published crate versions unless those versions are already locked, potentially delaying automatic updates to recent releases.

**「Community discussion」** Commenter nirinor called the never type, custom allocators, and dependency cooldowns personal favorites, while ammar\_az argued that the release post omitted useful stabilizations such as \`bool::toggle\(\)\`, \`Box::map\(\)\`, and \`str::trim\_prefix\(\)\`. Separately, jadbox questioned whether the release improves compiler speed or reduces the need for daily \`cargo clean\` to clear large temporary build directories, a concern not addressed by the release notes.

**Tags**: `#rust`, `#programming-languages`, `#systems-programming`, `#open-source`, `#compiler`

---

<a id="item-tech-news-2"></a>
### [PostgreSQL Type Confusion Escalated to Remote Code Execution \(CVE-2026-6460\)](https://mehmetince.net/part-3-6-how-i-ended-up-turning-a-22-year-old-postgresql-type-confusion-primitive-into-rce-cve-2026-6460/) ⭐️ 8.0/10

Researchers showed that a long‑standing PostgreSQL internal datum type confusion—where a small‑integer id stored separately might point to the wrong value—can be abused to gain full remote code execution. The resulting vulnerability, CVE‑2026‑6460, lets an attacker who already has a PostgreSQL database account run arbitrary commands on the server, achieving server‑level compromise. The finding affects all PostgreSQL installations that use this internal datum mechanism, including single‑user and multi‑tenant environments.

hackernews · ozirus · Nov 12, 18:22 · [Discussion](https://news.ycombinator.com/item?id=50471761)

**「Background」** The vulnerability \(CVE-2026-6460\) stems from a long-standing type confusion issue in PostgreSQL&\#x27;s internal Datum representation, where a Datum value can be either a direct value or a pointer depending on its associated type OID. The PostgreSQL project has historically tracked typed values with separate type identifiers, creating a risk that the type OID could become desynchronized from the actual Datum content. Red Hat&\#x27;s advisory confirms that an authenticated user with permissions to create or alter database objects can exploit this by executing specific data definition commands such as ALTER TABLE ... ALTER COLUMN TYPE, leading to arbitrary code execution as the database operating system user.

**「Remote Code Execution via PostgreSQL Type Confusion」** A recent PostgreSQL core vulnerability \(CVE‑2026‑6460 and related CVE‑2026‑14680\) creates a type‑confusion primitive that lets an object creator invoke arbitrary OS commands via ALTER … SET DATA TYPE or by supplying malformed internal arguments, granting the attacker full remote code execution as the database user. This zero‑day, uncovered months after initial detection, enables takeover of the server and is especially risky in multi‑tenant or managed PostgreSQL deployments.

**「Community Takeaways」** Users noted differing views: one commenter argued these are primarily privilege‑escalation attacks rather than true RCE and require existing remote access, while another called it a &\#x27;code smell&\#x27; leading to reek. Amluto highlighted the role of the internal datum pointer and warned that misbound ids make the primitive risky. Overall, the consensus leans toward treating it as a serious privilege‑escalation vector that can pivot to full system control.

<details><summary>References</summary>
<ul>
<li><a href="https://access.redhat.com/security/cve/cve-2026-6460">CVE-2026-6460 - Red Hat Customer Portal</a></li>
<li><a href="https://www.postgresql.org/support/security/CVE-2026-6460/">PostgreSQL: CVE-2026-6460: PostgreSQL type confusion after ...</a></li>
<li><a href="https://www.postgresql.org/support/security/CVE-2026-14680/">PostgreSQL: CVE-2026-14680: PostgreSQL type confusion via ...</a></li>
<li><a href="https://mehmetince.net/part-3-6-how-i-ended-up-turning-a-22-year-old-postgresql-type-confusion-primitive-into-rce-cve-2026-6460/">Part 3/6 | How I Ended Up Turning a 22-Year-Old PostgreSQL ...</a></li>

</ul>
</details>

**Tags**: `#PostgreSQL`, `#security`, `#vulnerability-research`, `#RCE`, `#database-internals`

---

<a id="item-tech-news-3"></a>
### [Project reports 16B LLM inference on sub-1GB devices](https://github.com/hyperionaidev/smolmaxxing/) ⭐️ 8.0/10

The author of the open-source smolmaxxing project reports running 16B-parameter LLMs on an iPad Air 1st generation and a Xiaomi TV box, each with less than 1GB of usable memory, and says the setup reaches decent speeds for the hardware. The project is releasing custom kernels and modified models on Hugging Face, along with results the author says others can reproduce. These are the author&\#x27;s claims; the supplied item does not include independent benchmarks or source documentation.

hackernews · mrashad74 · Nov 12, 15:23 · [Discussion](https://news.ycombinator.com/item?id=50468888)

**「Background」** LLM inference is constrained by memory because model weights and runtime state must fit on the device, and a 16B-parameter model is far larger than the sub-1GB budget these devices provide. The project relies on extreme quantization and custom kernel development to shrink that footprint, an approach that typically involves trade-offs in speed, accuracy, or portability.

**「Impact」** Developers can inspect the kernels and download the modified models from Hugging Face to try reproducing the setup, but the results depend on project-specific kernels and converted weights, so portability to other devices or stock runtimes is not established.

**「Community discussion」** One commenter argued that modern coding agents can already produce an inference engine from a single prompt, making access to old hardware the harder part of the task. Others welcomed the work as demoscene-style optimization for aging GPUs and small local models, while the author framed it as an open-source effort others can extend.

**Tags**: `#llm-optimization`, `#edge-computing`, `#quantization`, `#kernel-development`, `#open-source`

---

<a id="item-tech-news-4"></a>
### [Anthropic files for proposed Nasdaq IPO under ticker ANT](https://ipo.anthropic.com/us/) ⭐️ 8.0/10

Anthropic has opened a filing page indicating a proposed initial public offering on Nasdaq under the ticker ANT, dated November 12, 2026. Community members citing the linked documents report a share price range of $70–$78 and an implied market capitalization of roughly $968 billion at the $74 midpoint, alongside a combined IPO and private placement of approximately $85.3 billion. The same excerpts attribute $17.0 billion in Q3 2026 revenue and $900.9 billion in compute commitments scheduled through 2045 to the company.

hackernews · josephljohnston · Nov 12, 11:46 · [Discussion](https://news.ycombinator.com/item?id=50465829)

**「Background」** An initial public offering allows a privately held firm to sell equity to public investors for the first time, often to fund large-scale capital projects. Anthropic previously raised money through private rounds, including a Series F reported at a $61.5 billion valuation in March 2025, which the proposed public pricing would significantly exceed.

**「Impact」** If priced at the low end of the range, the offering could leave Anthropic&\#x27;s prior Series H round underwater, according to community analysis. Conversely, the raised capital appears intended to back the company&\#x27;s multi-year compute commitments, though some observers argue the liquidity push may precede clear market dominance.

**「Community Discussion」** Participants divided on the rationale, with some arguing venture capitalists should have delayed the IPO to allow for further private funding or profits, while others noted that cheaper local models may limit the addressable market for frontier AI APIs.

**Tags**: `#artificial-intelligence`, `#ipo`, `#ai-industry`, `#machine-learning`, `#technology-finance`

---

<a id="item-tech-news-5"></a>
### [UMAP 0.6 released with faster nearest-neighbor search, new initialization, and opt-in optimizers](https://www.reddit.com/r/MachineLearning/comments/1xudaah/umap_06_new_initialization_new_optimizers_and/) ⭐️ 8.0/10

UMAP 0.6 has been released, introducing faster nearest-neighbor search, a new recursive initialization scheme, and new optimizers for the Python dimensionality-reduction library. Neighbor search is about 4x faster through better use of PyNNDescent, and on 3 million arXiv papers the new version finishes in under five minutes while UMAP 0.5 had not yet completed nearest-neighbor search. The new initialization and optimizers are opt-in via \`compatibility\_layout=False\` because they change the output; they will become the default in a future version. A seeded run is now reproducible across all cores, whereas a seeded UMAP 0.5 run was single-threaded and took 52 minutes.

reddit · r/MachineLearning · /u/lmcinnes · Nov 12, 13:51

**「Background」** UMAP is a Python library for dimensionality reduction that lays out high-dimensional data in a low-dimensional embedding. Its layout is produced by an initialization step followed by an optimizer that refines the embedding; UMAP 0.5 is the prior release used as the speed and quality baseline in this announcement.

**「Impact」** Users can install UMAP 0.6 via \`pip install -U umap-learn\` or conda-forge. The new initialization and optimizers are opt-in through \`compatibility\_layout=False\` because they change the output, so workflows relying on exact layout reproducibility should validate the new behavior before adopting it as the default.

**Tags**: `#UMAP`, `#dimensionality-reduction`, `#machine-learning`, `#Python`, `#performance`

---

<a id="item-tech-news-6"></a>
### [US Commerce finalizing rule to block Chinese AI firms&\#x27; remote chip access](https://www.theinformation.com/articles/commerce-department-finalizing-long-awaited-ai-remote-access-rule) ⭐️ 8.0/10

The U.S. Commerce Department is finalizing a rule that would bar Chinese AI companies from remotely using advanced AI chips through overseas data centers, with publication possible as early as this month. The controls would extend existing semiconductor export restrictions to seven countries including Malaysia, Singapore and Thailand, aiming to close remote-access and chip-smuggling gaps, according to The Information. The department is consulting other government agencies before finalizing the rule. The White House has asked Congress to legislate a requirement for the rule, and Nvidia has lobbied against closing the remote-access gap, arguing that U.S. AI infrastructure needs to win globally.

telegram · zaihuapd · Nov 12, 03:42

**「Background」** The U.S. has maintained escalating semiconductor export controls on China since 2022, restricting direct shipments of advanced AI chips to Chinese entities. These controls created a remote-access loophole: Chinese AI companies could circumvent restrictions by leasing computing power from overseas data centers where the chips were legally deployed. The White House previously urged Congress to pass legislation mandating the Commerce Department close this gap, while NVIDIA lobbied against the rule, arguing it would harm U.S. AI infrastructure competitiveness.

**「Impact」** The finalized rules close the remote-access loophole through which Chinese AI companies reached restricted advanced chips via data centers in Singapore, Malaysia, and five other covered Southeast Asian nations. Operators previously facilitating this access face direct compliance and enforcement consequences, exemplified by Megaspeed, which U.S. officials are investigating for potentially diverting chips illegally into China \[tool-2-1\]. Developers relying on these overseas data centers may lose access to frontier training compute as the export controls expand to cover remote connections across these jurisdictions \[tool-2-2\].

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/11/11/business/economy/nvidia-affair-spy-bessent-lutnick.html">Trump Officials Clashed Over Megaspeed, Firm at Heart of Nvidia Affair</a></li>
<li><a href="https://aipolicydaily.org/archive/daily/2026-11-10/">Commerce chip probe went to DOJ | WH seeks chip remote access ...</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#semiconductor export controls`, `#US‑China tech rivalry`, `#remote AI access`, `#Southeast Asia`

---

<a id="item-tech-news-7"></a>
### [👁️ 突发: 黄仁勋辞任英伟达 CEO，CFO 克雷斯任临时 CEO](https://nvidianews.nvidia.com/news/nvidia-announces-ceo-transition) ⭐️ 8.0/10

Jensen Huang steps down as NVIDIA CEO, with CFO Colette Kress appointed interim CEO and Harvey C. Jones named board chair, while the company continues its planned Q3 earnings release.

telegram · zaihuapd · Nov 12, 13:52

**Tags**: `#leadership-change`, `#nvidia`, `#ai-hardware`, `#executive-news`, `#tech-industry`

---

<a id="item-tech-news-8"></a>
### [tamserve open-source video tracker shares model weights across cameras, cuts RTX 4090 costs 2x](https://www.reddit.com/r/MachineLearning/comments/1xuvxke/i_built_tamserve_to_make_realtime_video_tracking/) ⭐️ 7.5/10

tamserve is a free, open-source real-time video tracking system for multi-camera live video that shares one model copy across all cameras, keeping GPU memory flat so it can run indefinitely rather than exhausting memory within minutes. The author reports up to 3.8x speedup over Meta&\#x27;s SAM 2-style tracking code with the same accuracy, and RTX 4090 costs of $1.07 per camera per day at 30 fps versus $2.40 with Meta&\#x27;s code \($0.36 versus $0.74 at 10 fps; $0.18 versus $0.44 at 5 fps\). It supports automatic camera reconnection, adding or dropping objects on any frame, and multi-GPU scaling, and is available on GitHub and Google Colab; the performance and cost figures are the author&\#x27;s reported results.

reddit · r/MachineLearning · /u/Chunkymunkey642069 · Nov 13, 02:23

**「Background」** SAM 2-style trackers such as SAM 2.1 and EdgeTAM let users point at an object once and track its exact outline on every frame, but they are expensive on live cameras because Meta&\#x27;s reference code retains every frame it processes and exhausts GPU memory within minutes. tamserve addresses this by sharing one model instance across cameras instead of keeping per-frame state.

**「Impact」** Users tracking live cameras on one RTX 4090 can cut per-camera daily cost roughly in half at 30 fps \($1.07 versus $2.40 with Meta&\#x27;s code\) and run indefinitely instead of hitting GPU memory limits within minutes, though they should verify the reported speedup and costs on their own deployments.

**Tags**: `#real-time video tracking`, `#computer vision`, `#open source`, `#machine learning`, `#AI systems`

---

<a id="item-tech-news-9"></a>
### [Gemini 4 Hydrogen and Orchestrator](https://antigravity.google/blog/gemini-4-hydrogen-in-google-antigravity/) ⭐️ 7.0/10

A Hacker News discussion of Google&\#x27;s Gemini 4 Hydrogen model and Orchestrator, with commenters debating model naming, performance, and multi-model pipeline design.

hackernews · jonbaer · Nov 12, 18:52 · [Discussion](https://news.ycombinator.com/item?id=50472260)

**Tags**: `#Gemini`, `#LLM orchestration`, `#Google`, `#AI models`, `#developer tools`

---

<a id="item-tech-news-10"></a>
### [Microsoft 365 outage disrupts Outlook and Exchange Online email](https://status.cloud.microsoft/) ⭐️ 7.0/10

Microsoft 365 users worldwide reported a severe service degradation on November 12, 2026, with Outlook and Exchange Online email most affected. Downdetector showed about 130,000 user reports for Outlook, while Microsoft said the issue mainly involved Exchange Online. Some administrators reported email delays or outages lasting hours, while Teams chat and meetings remained usable for them. Microsoft later said it had validated an alternative health-check method on a subset of affected infrastructure and was applying it more broadly while preparing automated recovery.

hackernews · dkpk · Nov 12, 18:20 · [Discussion](https://news.ycombinator.com/item?id=50471731)

**「Background」** Microsoft 365 is a cloud productivity suite, and Exchange Online is the service that provides hosted email for Outlook and other clients. When Exchange Online degrades, organizations can lose mail flow even if other Microsoft 365 services such as Teams remain available. Microsoft&\#x27;s service health status page and third-party trackers such as Downdetector are commonly used to monitor such incidents.

**「Impact」** Organizations affected by the Exchange Online degradation may need to rely on Teams or other communication channels for time-sensitive messages while email is delayed or unavailable. IT teams should monitor Microsoft 365 status updates, including the RSS feed when the status page is unreliable, because recovery was being applied progressively rather than restored all at once.

**「Community discussion」** Hacker News commenters reported practical impact, including email down for hours for a 15,000-employee organization while Teams and Azure remained usable, and described it as worse than typical AWS US-East-1 issues. One commenter blamed Microsoft&\#x27;s AI focus and underinvestment, but that is an opinion rather than a verified cause.

**Tags**: `#microsoft-365`, `#outage`, `#cloud-services`, `#enterprise-it`

---

<a id="item-tech-news-11"></a>
### [Talking Zen 6 with Mike Clark at AMD In-Depth](https://chipsandcheese.com/p/talking-zen-6-with-mike-clark-at) ⭐️ 7.0/10

An in-depth interview with AMD&\#x27;s Mike Clark covers technical details of the Zen 6 CPU architecture.

hackernews · dverlaeckt80 · Nov 12, 14:12 · [Discussion](https://news.ycombinator.com/item?id=50467460)

**Tags**: `#CPU architecture`, `#AMD Zen`, `#computer hardware`, `#microarchitecture`, `#semiconductor design`

---

<a id="item-tech-news-12"></a>
### [NVIDIA&\#x27;s exposure to export controls and supply chain risks](https://newsletter.semianalysis.com/p/nvidia-and-the-world-without-jensen) ⭐️ 7.0/10

The article analyzes how upcoming export controls and supply chain dependencies could affect NVIDIA and its customers. It highlights NVIDIA&\#x27;s reliance on Chinese manufacturing and the potential for restricted access to advanced GPUs in key markets. The piece also examines RASA and open source implications amid these geopolitical pressures.

rss · Semianalysis · Nov 12, 18:06

**「Prior U.S. Chip Export Policy」** The Trump administration had previously negotiated terms allowing sales of Nvidia&\#x27;s H200 chips to China under a 25% tariff, creating an earlier policy framework for U.S.-China semiconductor exports. The current article assesses how export controls, open-source implications, and supply chain dependencies have evolved beyond that prior arrangement.

**「Impact」** If export controls restrict NVIDIA&\#x27;s chip shipments, organizations that rely on its GPUs for AI training may face supply disruptions and need to adopt alternative hardware or open source solutions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.axios.com/2026/11/11/trump-lutnick-nvidia-china-chip-export-controls">Trump backed Nvidia chip controls aimed at China 3 times as Lutnick...</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#Export Controls`, `#Open Source`, `#Supply Chain`, `#Geopolitics`

---

<a id="item-tech-news-13"></a>
### [Independent audit questions TRIBE v2 topographic maps](https://www.reddit.com/r/MachineLearning/comments/1xuillf/does_metas_brainresponse_model_tribe_v2_actually/) ⭐️ 7.0/10

An independent Reddit analysis reports that Meta’s TRIBE v2, a model that predicts fMRI responses from video, audio, and text, does not recover classic retinotopic or tonotopic maps when tested with standard mapping stimuli. The author reports no retinotopic map \(d=0.05, n.s.\) or tonotopic map \(ρ=-0.07, n.s.\), but sharp motion selectivity in MT+ \(d=4.31, 52× chance enrichment\); an eccentricity effect became significant only under three stimulus-geometry controls and was attributed to image statistics rather than a true positional code. These are provisional, self-published results from a solo project, not peer-reviewed findings or a vendor-confirmed capability.

reddit · r/MachineLearning · /u/Own\_Tank1283 · Nov 12, 17:16

**「Background」** TRIBE v2 is a multimodal brain-response model that predicts fMRI activity from video, audio, and text, while classic fMRI mapping paradigms test whether models recover known cortical organization such as retinotopy, tonotopy, and motion selectivity. The post notes that TRIBE v2’s methods spatially average video features before prediction, a step that can remove the positional information needed for retinotopic mapping.

**「Impact」** For researchers using or evaluating TRIBE v2, the reported null retinotopy and tonotopy results mean the model should not be assumed to encode spatial or frequency-topographic organization without direct testing, and eccentricity-related interpretations should be checked against stimulus-geometry confounds.

**Tags**: `#computational neuroscience`, `#fMRI`, `#model evaluation`, `#Meta TRIBE v2`, `#retinotopy`

---

<a id="item-tech-news-14"></a>
### [知情人士：「腾讯裁员 50%」系谣言误读](https://finance.sina.com.cn/roll/2026-11-12/doc-iniymwrm3902520.shtml) ⭐️ 7.0/10

A source denies the claim that Tencent is laying off 50% of employees, stating instead that the firm is accelerating AI-native initiatives while keeping core operations.

telegram · zaihuapd · Nov 12, 04:23

**Tags**: `#Tencent`, `#Artificial Intelligence`, `#Layoffs`, `#Corporate Strategy`, `#Technology`

---

<a id="item-tech-news-15"></a>
### [Japan to Impose Security Obligations on AI Practitioners](https://mainichi.jp/articles/20261112/ddm/002/010/086000c) ⭐️ 7.0/10

Japan&\#x27;s government announced it will require AI developers and service providers to assume security‑assurance duties and face new fines for non‑compliance, aiming to curb cyber‑attack abuse and uncontrolled AI behavior. The proposal, discussed in a non‑public working group on AI law, will be formalized in a system‑wide revision to be published by the end of the year, with the exact scope of applicable entities still under review. If finalized, the obligations could extend to large U.S. IT companies, affecting their AI deployment practices.

telegram · zaihuapd · Nov 12, 06:04

**「Background」** Japan’s proposal is being developed within a non-public working group on AI legislation, with the full framework, including possible legal amendments, expected to be published by the end of the year. The measure would create security-assurance duties and new penalties for AI-related businesses, but the exact scope, including whether large U.S. IT companies are covered, remains under consideration.

**「Impact」** Developers and firms will need to implement security controls and risk‑management processes to avoid fines, altering their AI development workflows.

**Tags**: `#AI`, `#Cybersecurity`, `#Regulation`, `#Japan`

---

<a id="item-tech-news-16"></a>
### [Apple details Secure Exclaves audio/video isolation and recording-indicator checks](https://security.apple.com/blog/secure-exclaves/) ⭐️ 7.0/10

Apple published a Nov. 12 post detailing Secure Exclaves, an isolated security environment for audio and video processing in which the main system and apps in environment-awareness mode receive only necessary recognition results rather than raw data. Apple says the architecture is used in HomeView face and sound recognition and in the iPhone 18 Pro privacy indicator. On iPhone 18 Pro, Apple says dedicated hardware verifies the microphone indicator dot&\#x27;s color, brightness, and visibility before allowing audio into the main system, and Siri audio sessions must keep the dot continuously visible for at least three seconds in total.

telegram · zaihuapd · Nov 12, 09:13

**「Secure Exclaves Explained」** The reported Apple effort builds on Secure Exclaves, a security architecture that uses protected and compartmentalized runtimes to process camera and microphone data separately from the rest of the system. Apple said that isolation features added across many core components of the silicon work in tandem to protect the Secure Enclaves and keep them segregated from the rest of the system, and that data processed and analyzed in a Secure Enclave cannot be accessed by the main system or apps.

**「Impact」** Developers integrating these environment-aware features must design around derived recognition results rather than raw audio or video, and iPhone 18 Pro audio capture depends on the hardware-verified indicator remaining visible.

<details><summary>References</summary>
<ul>
<li><a href="https://security.apple.com/blog/secure-exclaves">Secure Exclaves and Ambient Sensing - Apple Security Research</a></li>
<li><a href="https://www.macrumors.com/2026/11/12/apple-homeview-secure-exclaves/">Apple Explains How HomeView Keeps Camera Data Private</a></li>
<li><a href="https://cyberinsider.com/apple-secure-exclaves-homeview-iphone-privacy-security/">Apple isolates HomeView camera and mic data with Secure Exclaves</a></li>

</ul>
</details>

**Tags**: `#Apple Secure Exclaves`, `#privacy engineering`, `#security architecture`, `#audio/video privacy`, `#hardware security`

---

<a id="item-tech-news-17"></a>
### [Samsung patents UWB radar + BIA for Galaxy Watch visceral fat measurement](https://www.androidheadlines.com/2026/11/samsung-galaxy-watch-visceral-fat-patent.html) ⭐️ 7.0/10

Samsung published a patent describing a method that combines UWB radar with bioimpedance sensing to estimate visceral and subcutaneous fat on future Galaxy Watch models. The system would use height, weight, age, and gender inputs, improving upon the Galaxy Watch 4&\#x27;s BIA-only capability that could only estimate overall body composition. However, the patent does not specify a ship date or specific model, and the technology requires UWB radar hardware not yet confirmed in released watches.

telegram · zaihuapd · Nov 12, 11:05

**「Background」** The Galaxy Watch 4, launched in 2021, introduced bioimpedance analysis \(BIA\) sensors to estimate overall body fat percentage but could not separately measure visceral fat. Samsung&\#x27;s new patent builds on that existing BIA foundation by adding ultra-wideband radar to the sensing approach.

**「Impact」** Galaxy Watch users and developers should expect that visceral fat measurement via UWB radar will not be available on current devices, and future compatibility depends on Samsung releasing compatible hardware and software updates. Existing Galaxy Watch models lack the required UWB radar component.

**Tags**: `#Samsung`, `#Galaxy Watch`, `#UWB radar`, `#visceral fat`

---

<a id="item-tech-news-18"></a>
### [Telegram Widgets RCE Vulnerability in Bot API 10.4](https://x.com/telegram/status/2120502876728680765?a=qTsR6dLMSgt3RHbYYO0&amp;amp;s=46) ⭐️ 7.0/10

A remote code execution \(RCE\) vulnerability was discovered in Telegram&\#x27;s Bot API Widgets feature \(introduced in Bot API 10.4 on 2026-11-09\), allowing JavaScript execution in chat messages through embedded HTML/CSS/JS. Although Telegram claims the issue has been fixed, community testing indicates the vulnerability still exists on some devices, posing a security risk to users and developers who interact with unsanitized bot messages.

telegram · zaihuapd · Nov 13, 01:02

**「Telegram Widgets feature and sandbox vulnerability」** Telegram Widgets is a Bot API feature that enables bots to embed interactive HTML, CSS, and JavaScript within chat messages. The vulnerability stems from a security flaw in the client-side sandbox implementation that allows arbitrary JavaScript execution when bots embed code, which Telegram has reportedly addressed but some users report remain exploitable.

**Tags**: `#Security`, `#Telegram`, `#RCE`, `#Bot API`, `#Vulnerability`

---

<a id="item-tech-news-19"></a>
### [Google releases Gemini 4 Hydrogen model for fast coding and agent workflows](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-hydrogen/) ⭐️ 7.0/10

Google announced Gemini 4 Hydrogen, a model aimed at developers, enterprises and general users, offering coding and agent workflow acceleration. It is priced at $1.5 per million input tokens and $7.5 per million output tokens, and claims to be 2.5 times faster than Gemini 3.8 Flash. Its Terminal‑Bench 4.1 score rose from 18.2% to 57% and its Artificial Analysis index surpasses Argon.

telegram · zaihuapd · Nov 13, 02:02

**「Background」** Gemini 4 Hydrogen succeeds Gemini 3.8 Flash, which it now replaces across Google&\#x27;s products; Ars Technica reports that Hydrogen&\#x27;s access limits are more relaxed than those applied to 3.8 Flash at general availability. Google is also rolling out Hydrogen in Google Antigravity alongside an Orchestrator option that pairs it with Gemini 4 Carbon.

**「Impact」** Developers can execute coding tasks more cheaply and quickly, lowering latency and cost for agent‑driven applications.

<details><summary>References</summary>
<ul>
<li><a href="https://antigravity.google/blog/gemini-4-hydrogen-in-google-antigravity/">Gemini 4 Hydrogen and Orchestrator | Google Antigravity Blog</a></li>
<li><a href="https://arstechnica.com/google/2026/11/google-rolls-out-gemini-4-hydrogen-finally-replacing-3-8-flash/">Google rolls out Gemini 4 Hydrogen , finally replacing... - Ars Technica</a></li>

</ul>
</details>

**Tags**: `#Google`, `#Gemini`, `#AI models`, `#coding agents`, `#benchmarks`

---

<a id="item-tech-news-20"></a>
### [研究称六款中国 AI 模型留下 Blackwell 芯片指纹](https://unemploymentlabs.com/checkpoint-forensics) ⭐️ 7.0/10

Unemployment Labs claims six Chinese AI models contain Blackwell chip fingerprints, suggesting possible Blackwell use in training.

telegram · zaihuapd · Nov 13, 02:42

**Tags**: `#NVIDIA Blackwell`, `#AI model training`, `#China AI`, `#model weight forensics`, `#machine learning hardware`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Oil prices rise after Trump comments on Iran](https://www.cnbc.com/2026/11/12/oil-prices-jump-after-trump-says-no-iran-deal-needed-weve-got-their-strait.html) ⭐️ 7.0/10

U.S. oil prices rose Thursday after President Donald Trump said in a Truth Social post that no Iran deal was needed and that the U.S. had the Strait of Hormuz, with Brent crude settling 3.3% higher at $95.82 per barrel and West Texas Intermediate futures up 2.6% at $88.74 per barrel.

rss · CNBC Finance · Nov 13, 00:01

**「Background」** The Strait of Hormuz is a narrow shipping lane between Iran and Oman through which about 20 million barrels of oil and oil products passed daily in 2025, roughly one-fifth of global oil consumption. The U.S. and Iran have been at war, with both sides reporting shipping hits in or near the strait, so renewed doubts about a deal or transit security can affect oil prices.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/c78n6p09pzno">Iran war: What is the Strait of Hormuz and why does it matter?</a></li>

</ul>
</details>

**Tags**: `#oil prices`, `#Iran geopolitics`, `#Strait of Hormuz`, `#energy markets`, `#supply risk`

---

<a id="item-finance-news-2"></a>
### [Eli Lilly&\#x27;s oral weight-loss drug approved in China](https://www.reuters.com/business/healthcare-pharmaceuticals/china-approves-eli-lillys-weight-loss-pill-orforglipron-2026-11-12/) ⭐️ 7.0/10

China&\#x27;s National Medical Products Administration approved Eli Lilly&\#x27;s oral GLP-1 weight-loss drug orforglipron on Nov. 12, making it the country&\#x27;s first oral GLP-1 obesity treatment. The once-daily pill is cleared for adults with obesity or overweight plus at least one weight-related comorbidity, while price and launch timing were not disclosed.

telegram · zaihuapd · Nov 12, 10:09

**「Background」** GLP-1 drugs are a class of weight-loss treatments; the approval introduces an oral option against weekly injectable products from Novo Nordisk, Pfizer and Innovent in China.

**「Impact」** The approval gives patients and clinicians in China a non-injectable obesity treatment option and increases competition in the country&\#x27;s weight-loss drug market.

**Tags**: `#Pharmaceuticals`, `#Regulatory Approval`, `#GLP-1 weight loss`, `#China market`, `#Eli Lilly`

---