---
layout: default
title: "Horizon Summary: 2026-11-14 (EN)"
date: 2026-11-14
lang: en
---

> From 40 items, 9 important content pieces were selected

---

**Technology News**
1. [FAA issues national ground stop](#item-tech-news-1) ⭐️ 7.0/10
2. [ICML 2027 introduces two-stage review and authorship-linked reviewing duties](#item-tech-news-2) ⭐️ 7.0/10
3. [TorchTitan team reports 1T-parameter MoE training on 384 GH200 GPUs](#item-tech-news-3) ⭐️ 7.0/10
4. [Microsoft 365 Outlook, Teams, Copilot outage exceeds 12 hours](#item-tech-news-4) ⭐️ 7.0/10
5. [DeepSeek opens full application API suite with multimodal tool calling and V4.1-Flash](#item-tech-news-5) ⭐️ 7.0/10

**Financial News**
1. [Moonshot AI restructures for Hong Kong IPO](#item-finance-news-1) ⭐️ 8.0/10
2. [Cantor Fitzgerald&\#x27;s Nvidia Position Drops Nearly Half as Son-Led Firm Tied to Chipmaker](#item-finance-news-2) ⭐️ 7.0/10
3. [Goolsbee says Fed has work to do on inflation](#item-finance-news-3) ⭐️ 7.0/10
4. [Jensen Huang&\#x27;s resignation and the likely tightening of U.S.–China chip export controls](#item-finance-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [FAA issues national ground stop](https://www.nbcnews.com/news/us-news/faa-orders-nationwide-ground-stop-departing-flights-reasons-safety-rcna609247) ⭐️ 7.0/10

FAA&\#x27;s national ground stop, triggered by a L3Harris telecom outage, reveals vulnerabilities in critical aviation systems and spurs debate over AI integration in air traffic control.

hackernews · zulln · Nov 13, 21:05 · [Discussion](https://news.ycombinator.com/item?id=50489641)

**Tags**: `#aviation-infrastructure`, `#network-outage`, `#critical-systems`, `#AI-ATC`

---

<a id="item-tech-news-2"></a>
### [ICML 2027 introduces two-stage review and authorship-linked reviewing duties](https://www.reddit.com/r/MachineLearning/comments/1xvkxbj/icml_2027_changes_d/) ⭐️ 7.0/10

ICML 2027 will adopt a two-stage review process where area chairs decide whether papers proceed to full review, with any first-stage rejection requiring confirmation by a senior area chair and a short justification provided to authors by February 23. New constraints limit each person to 20 submissions, require every paper to name a reciprocal reviewer from its author list \(capped at six papers per reviewer\), and mandate program committee service for anyone with three or more submissions. Papers that do not comply may be desk rejected, and each author may appear on at most one paper lacking an eligible reciprocal reviewer among its coauthors.

reddit · r/MachineLearning · /u/Gravitist · Nov 13, 21:53

**「Background」** Top machine-learning conferences have faced a sustained surge in submissions, leading to reviewer burnout and concerns about review quality. ICML and other venues have previously experimented with measures such as reviewer load caps and mandatory reviewing, but the 2027 changes combine a structural two-stage filter with explicit authorship-to-reviewing obligations.

**「Impact」** Authors who frequently collaborate with non-reviewing coauthors \(such as students or researchers outside the field\) will lose the ability to include them on multiple submissions without providing a qualified reciprocal reviewer, forcing teams to adjust authorship practices or secure additional reviewing capacity.

**Tags**: `#machine-learning`, `#conference-review`, `#peer-review-process`, `#ai-research`, `#submission-management`

---

<a id="item-tech-news-3"></a>
### [TorchTitan team reports 1T-parameter MoE training on 384 GH200 GPUs](https://www.reddit.com/r/MachineLearning/comments/1xvce5h/scaling_to_1t_moe_on_torchtitan_p/) ⭐️ 7.0/10

The TorchTitan team reports training a ~1T-parameter mixture-of-experts model on 384 GH200 GPUs in the JUPITER supercomputer at about 1,300 tokens/s per GPU, a 14× improvement over its starting point. The setup uses 384-way FSDP plus 4-way expert parallelism kept within each node and deliberately skips pipeline parallelism; the team says full activation checkpointing, Grace CPU offload, Muon, FlexShard, and FP8 expert all-gather were needed to reach 64k-token sequences and cut communication. It also describes replacing FP32 reduce-scatter with BF16 all-to-all for expert gradients and moving collective temporaries to the compute stream, which eliminated allocator retries and raised throughput 21%. These are the team&\#x27;s reported results, not independently measured here.

reddit · r/MachineLearning · /u/f14-bertolotti · Nov 13, 16:28

**「Background」** TorchTitan is the PyTorch training stack the team modified; its FSDP path shards each weight across ranks and gathers the needed slices just in time, while expert parallelism assigns each GPU a subset of MoE experts and routes tokens to them. The alternative, pipeline parallelism, splits layers across GPUs but needs many microbatches to hide pipeline bubbles, which lengthens steps and slows debugging at scale.

**「Impact」** The reported TorchTitan experiment indicates that a roughly 1-trillion-parameter mixture-of-experts model can be trained to high throughput on a publicly accessible HPC system, reaching about 1,300 tokens per second per GPU across 384 GH200 GPUs. For developers, the practical consequence is that expert-parallel communication and activation management may be treated as critical bottlenecks in very large MoE training, and the reported use of FSDP plus expert parallelism rather than pipeline parallelism may guide architecture choices.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/pytorch/torchtitan">GitHub - pytorch/ torchtitan : A PyTorch native platform for training...</a></li>
<li><a href="https://arxiv.org/pdf/2410.06511">TorchTitan : One-stop PyTorch native solution for production ready...</a></li>
<li><a href="https://www.primeintellect.ai/blog/prime-mega-moe">Prime Mega MoE : Fast Fused MoE Kernels for Training</a></li>

</ul>
</details>

**Tags**: `#Mixture of Experts`, `#LLM scaling`, `#distributed training`, `#GPU clusters`, `#PyTorch`

---

<a id="item-tech-news-4"></a>
### [Microsoft 365 Outlook, Teams, Copilot outage exceeds 12 hours](https://www.reuters.com/technology/microsoft-365-outlook-down-thousands-us-users-downdetector-shows-2026-11-12/) ⭐️ 7.0/10

Microsoft&\#x27;s Outlook, Teams and Copilot remained down on November 13 for more than 12 hours, disrupting communications for enterprises and governments worldwide. Microsoft attributed the outage to a server problem, said it found no malicious activity, and reported expanding remediation with signs of stabilization. Australian, Japanese and some U.S. government agencies were affected, Euronext email was disrupted, and some Taiwanese financial institutions switched to fax to confirm transactions; it was the second Microsoft 365 outage this year.

telegram · zaihuapd · Nov 13, 12:21

**「Microsoft 365 Outage Background」** The November 13, 2026, disruption affected Microsoft 365 services including Outlook, Teams, and Copilot, and it lasted for more than 12 hours according to Reuters. Microsoft said the cause was a server problem and that no malicious activity was found, while expanding the fix and seeing signs of recovery. Because these services are cloud-based productivity tools, the outage disrupted business and government communications around the world. The reports also described it as the second Microsoft 365 outage that year.

**「Global Microsoft 365 outage impact」** The outage disrupted Microsoft 365 services including Outlook, Teams, and Copilot for more than 12 hours, affecting enterprises and government communications across more than 70 countries. For affected organizations, it meant prolonged loss of access to core email, chat, and AI-related tools, disrupting operations and prompting workarounds. Microsoft attributed the incident to a server problem, said it found no malicious activity, and reported progress toward recovery.

<details><summary>References</summary>
<ul>
<li><a href="https://www.usatoday.com/story/news/2026/11/13/microsoft-outage-outlook-teams-latest-update/92755451007/">Microsoft outage: Latest updates on Outlook, Teams - USA TODAY</a></li>
<li><a href="https://www.forbes.com/sites/kateoflahertyuk/2026/11/13/microsoft-outage-what-happened-and-what-to-do-next/">Microsoft Outage—What Happened And What To Do Next - Forbes</a></li>
<li><a href="https://time.com/article/2026/11/13/microsoft-outage-worldwide-disruption-teams-outlook-emails/">Microsoft Outage Latest News: What You Need to Know - TIME</a></li>
<li><a href="https://en.wikipedia.org/wiki/2026_Microsoft_outage">2026 Microsoft outage - Wikipedia</a></li>
<li><a href="https://www.breitbart.com/tech/2026/11/13/microsofts-email-meltdown-extends-into-second-day-company-reports-progress-towards-recovery/">Microsoft &#x27;s Email Meltdown Extends into Second Day, Company...</a></li>
<li><a href="https://www.theguardian.com/australia-news/2026/nov/13/global-microsoft-outage-what-happened-and-why">A global Microsoft 365 outage has hit millions – what... | The Guardian</a></li>

</ul>
</details>

**Tags**: `#Microsoft 365`, `#cloud outage`, `#enterprise software`, `#service reliability`

---

<a id="item-tech-news-5"></a>
### [DeepSeek opens full application API suite with multimodal tool calling and V4.1-Flash](https://mp.weixin.qq.com/s/78KBHc4-4N5b2vfL9SkutQ) ⭐️ 7.0/10

DeepSeek has opened its full suite of application APIs, allowing developers to enable deep-thinking search, file input, link reading, and voice dialogue through parameters in the existing API, with the server automatically handling tool calling and context stitching. The V4.1-Flash model is supported on three interfaces, while Search, Fetch, OCR, ASR, and TTS can be called individually. DeepSeek also open-sourced the deepseek-ai/chat-demo frontend, which can import historical conversations and be used to locally deploy the DeepSeek web interface via the API.

telegram · zaihuapd · Nov 13, 14:27

**「V4.1-Flash model context」** DeepSeek V4.1-Flash is the model that powers these newly opened application APIs. DeepSeek introduced V4.1-Flash as live on its API with native multimodal support, accessed by setting the model name to deepseek-flash, and it retired the earlier V4-Flash and V4-Flash-Vision-Exp models, so the new search, file, link, and voice tools sit on DeepSeek&\#x27;s current model line.

**「Impact」** Developers can now invoke Search, Fetch, OCR, ASR, and TTS as separate tools and run a local DeepSeek web interface using the open-sourced demo, though they must enable the relevant API parameters and V4.1-Flash is limited to three interfaces.

<details><summary>References</summary>
<ul>
<li><a href="https://www.deepseek.com/en/news/deepseek-v4-1-flash/">Introducing DeepSeek - V 4 . 1 - Flash : smarter, faster, more efficient.</a></li>

</ul>
</details>

**Tags**: `#API`, `#Multimodal`, `#LLM`, `#Tool calling`, `#Open source`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Moonshot AI restructures for Hong Kong IPO](https://www.wsj.com/tech/chinas-moonshot-ai-restructures-to-pave-way-for-ipo-49f09abb) ⭐️ 8.0/10

Moonshot AI is restructuring its ownership by moving shares into a mainland operating entity and ending its Cayman holding company to enable a Hong Kong IPO.

telegram · zaihuapd · Nov 13, 11:29

**「Background」** Like many Chinese tech startups, Moonshot AI used a Cayman Islands holding company to accept dollar investments from foreign backers while its operations remained in mainland China, and it is now unwinding that structure to meet Hong Kong listing rules.

**「Impact」** The restructuring positions Moonshot AI to list on the Hong Kong stock exchange, potentially raising capital for its AI business and affecting the Chinese AI market.

<details><summary>References</summary>
<ul>
<li><a href="https://www.wsj.com/tech/chinas-moonshot-ai-restructures-to-pave-way-for-ipo-49f09abb">China’s Moonshot AI Restructures to Pave Way for IPO</a></li>
<li><a href="https://panews.io/articles/01a1d422-1d14-773d-bf61-a76f257139c9">WSJ: Moonshot AI Undergoing Restructuring to Pave Way for IPO</a></li>

</ul>
</details>

**Tags**: `#IPO`, `#AI`, `#Corporate restructuring`, `#Hong Kong`

---

<a id="item-finance-news-2"></a>
### [Cantor Fitzgerald&\#x27;s Nvidia Position Drops Nearly Half as Son-Led Firm Tied to Chipmaker](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 7.0/10

Between September 2025 and March 2026, Cantor Fitzgerald—led by Lutnick’s sons—reported a nearly 50% decline in its Nvidia share holding, from 652 million shares valued at $652 million to 1.78 million shares valued at $310 million, while still helping arrange billions in financing for Nvidia’s business partners.

rss · CNBC Finance · Nov 13, 23:42

**「Background」** Before leaving Wall Street in February 2025, Commerce Secretary Howard Lutnick headed Cantor Fitzgerald, which later filed large Nvidia positions and facilitated billions in financing for the chipmaker amid U.S. export‑control pressure on suspected Chinese chip smugglers.

**「Impact」** The sharp drop in Cantor’s Nvidia stake and its financing role prompted Treasury, Defense, State and Trade officials to push for placing Megaspeed on the Entity List, raising questions about Lutnick’s knowledge of Nvidia.

**Tags**: `#Conflict of interest`, `#Export controls`, `#Nvidia`, `#Cantor Fitzgerald`, `#Howard Lutnick`

---

<a id="item-finance-news-3"></a>
### [Goolsbee says Fed has work to do on inflation](https://www.cnbc.com/2026/11/13/chicago-feds-goolsbee-says-central-bank-has-definitely-got-work-to-do-on-inflation.html) ⭐️ 7.0/10

Chicago Fed President Austan Goolsbee said the Federal Reserve still has work to do on inflation after the producer price index rose 6.5% in October from a year earlier, the highest annual pace since November 2022.

rss · CNBC Finance · Nov 13, 14:22

**「Background」** The producer price index measures wholesale prices, and the Fed uses inflation data to guide interest-rate decisions.

**Tags**: `#Federal Reserve`, `#inflation`, `#monetary policy`, `#PPI`, `#interest rates`

---

<a id="item-finance-news-4"></a>
### [Jensen Huang&\#x27;s resignation and the likely tightening of U.S.–China chip export controls](https://www.cnbc.com/2026/11/13/jensen-huang-nvidia-us-china-relations.html) ⭐️ 7.0/10

Former Nvidia CEO Jensen Huang resigned after reports of an affair with a Chinese spy, prompting congressional testimony and warnings that U.S. chip export rules could be tightened. Experts forecast Congress may impose stricter controls on advanced chips sold to China before year-end.

rss · CNBC Finance · Nov 13, 02:56

**「Context and prior incidents」** Intelligence said China&\#x27;s Ministry of State Security recruited businesswoman Alice Huang to gather information on then-CEO Jensen Huang, echoing earlier surveillance balloon incidents and coinciding with the November midterm elections.

**「Potential consequences for markets and industries」** If the U.S. enacts harsher export controls such as the MATCH Act or Affiliates Rule, Chinese firms could lose access to rare earth and chipmaking inputs, while U.S. chipmakers face reduced demand and higher costs, raising geopolitical tension in the U.S.-China tech race.

**Tags**: `#Nvidia`, `#U.S.-China relations`, `#semiconductor export controls`, `#geopolitical risk`, `#corporate governance`

---