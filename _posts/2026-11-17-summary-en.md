---
layout: default
title: "Horizon Summary: 2026-11-17 (EN)"
date: 2026-11-17
lang: en
---

> From 65 items, 8 important content pieces were selected

---

**AI Engineering / Research**
1. [Real-Time Jazz Partner via Sampling-Time Steering of Pretrained Transformer](#item-ai-tech-1) ⭐️ 10.0/10
2. [Marimba: Frozen ASR System for Audio Q&amp;A](#item-ai-tech-2) ⭐️ 8.0/10
3. [Neo4j Virtual Graph GA](#item-ai-tech-3) ⭐️ 7.0/10

**Technology News**
1. [vLLM v0.34.0 adds 10 new models, default extensible KV cache, and performance gains](#item-tech-news-1) ⭐️ 8.0/10
2. [CMU Launches Free CS Lectures on YouTube](#item-tech-news-2) ⭐️ 8.0/10
3. [Compromised Optimizely snippet served malware across Zoom, GitLab, CNN, BBC](#item-tech-news-3) ⭐️ 8.0/10
4. [OpenAI begins embedded assessments with four independent evaluators](#item-tech-news-4) ⭐️ 7.0/10

**Financial News**
1. [Nvidia Leadership Crisis and Democratic Congress Could Reshape AI Trade](#item-finance-news-1) ⭐️ 8.0/10

---

## AI Engineering / Research

<a id="item-ai-tech-1"></a>
### [Real-Time Jazz Partner via Sampling-Time Steering of Pretrained Transformer](https://www.reddit.com/r/MachineLearning/comments/1xxkyh3/steering_a_pretrained_music_transformer_at/) ⭐️ 10.0/10

Duetto is a real-time jazz accompaniment system that steers the pretrained Anticipatory Music Transformer \(Thickstun et al., 2023\) at sampling time without fine-tuning. A rule layer masks and biases logits to enforce musical constraints \(register, rhythm, chord tones\) and inject phrases from the Weimar Jazz Database, yielding ~61% of solo notes from quoted material. The system maintains ~1 second of lookahead, resampling on user input, achieving 12–18 ms/note on an RTX 3080 Ti and ~90 ms/note on a Jetson Orin Nano. Key limitations include drift from the human player, unpredictable responses, and a fragile bias–rule balance.

reddit · r/MachineLearning · /u/GGAllin43 · Nov 16, 09:19

**「Method」** The project, duetto, uses a pretrained Anticipatory Music Transformer \(Thickstun et al., 2023\) without fine-tuning and treats the human player&\#x27;s MIDI notes and the model&\#x27;s notes as one event sequence that is generated one note at a time with onset, duration, and pitch. Before each sampling step, a rule layer edits the model logits by masking disallowed events, such as notes for a hand that must wait, pitches outside a register, or bass notes off the beat, and by biasing likely events, such as current chord tones, a guide tone on the downbeat, or the next note of a quoted phrase. The phrase material comes from the Weimar Jazz Database, segmented at soloists&\#x27; breaths, transposed to the tune&\#x27;s chords, and developed over a chorus; in the demo, about 61% of solo notes came from quoted phrases or the theme, while the rest came from the model. To keep interaction responsive, the server samples about one second of music ahead and resamples the unplayed portion whenever the player plays, allowing the model to plan while preserving low latency. The author reports roughly 12 ms per note for the medium model and 18 ms per note for the large model on a 3080 Ti, and about 90 ms per note for the large model on a Jetson Orin Nano, which was still usable live, but also notes drift from the player, unpredictable responses, and a fragile balance between model-generated material and rule-based bias.

**「Engineering Takeaway」** Sampling-time steering is a viable, low-barrier alternative to fine-tuning for interactive symbolic music: duetto ships a real-time jazz partner that runs the pretrained Anticipatory Music Transformer \(Thickstun et al., 2023\) untouched and moves all control into a rule layer that edits logits before each sample. The architecture is straightforward to replicate — the player&\#x27;s and model&\#x27;s notes form one event sequence continued one note at a time, with masking for physical constraints \(waiting hands, register, bass on the beat\) and biasing for musical ones \(chord tones, guide tones, phrase continuation\) — and it runs comfortably on consumer hardware, at ~12 ms/note \(medium\) and ~18 ms/note \(large\) on an RTX 3080 Ti, with the large model still usable live at ~90 ms/note on a Jetson Orin Nano. Latency is managed by keeping ~1 s of music sampled ahead and resampling the unplayed portion whenever the player acts, which lets the model &quot;plan&quot; without blocking on interactivity. The reusable ingredients are the phrase library \(Weimar Jazz Database solos, segmented at breath points and transposed to the tune&\#x27;s chords\) and the bias-balancing knob that interpolates between model logits and rule scores. The honest caveats, which matter more than the headline numbers, are that the system can drift from the player, its responses are hard to predict, and the balance between the model&\#x27;s own ideas and the rules is fragile — too much bias collapses it into a phrase book, too little removes the jazz character — so expect to tune this per tune and per player rather than set it once. If you are building an interactive generative system and want to avoid the cost and data requirement of fine-tuning, this is worth prototyping on, provided you accept that steering quality is a per-session tuning problem, not a one-time setup.

**「Open Questions」** The author asks whether sampling-time steering hits a ceiling compared to fine-tuning for interactive symbolic music, and how to mitigate drift, unpredictability, and the brittle trade-off between rule-based guidance and model creativity.

**Tags**: `#sampling-time-steering`, `#constrained-decoding`, `#music-transformer`, `#phrase-library`, `#real-time-generation`

---

<a id="item-ai-tech-2"></a>
### [Marimba: Frozen ASR System for Audio Q&amp;A](https://www.reddit.com/r/MachineLearning/comments/1xxsqro/marimba_a_system_one_model_for_speech_r/) ⭐️ 8.0/10

Marimba is a frozen Qwen3‑ASR‑0.6B based system that answers typed questions about 8‑second audio windows using a single encoder pass and lightweight task‑specific readouts. It provides zero‑shot term spotting with Platt calibration, language identification, turn‑end detection, and speaker change/count estimation, and reports benchmarks on public data \(e.g., 100 % language ID on 300 FLEURS clips, AUROC 0.966‑0.980 for speaker change, and 6/9 tests matching or beating Qwen3‑Omni \(30B‑A3B\)\). The system includes open‑source code, weights, and a demo, but its turn‑end readout is trained on Smart Turn data and does not generalize to unseen tasks such as CochlScene. This work falls under the \*\*model / data knowledge engineering\*\* layer of the match.md fullstack.

reddit · r/MachineLearning · /u/solanotodesch · Nov 16, 15:47

**「Method」** The architecture uses a single frozen Qwen3‑ASR‑0.6B encoder per 8‑second audio window, followed by task‑specific readouts on frozen layers 18 \(turn‑end\) and 12 \(speaker change/count\). Term spotting is performed zero‑shot by scoring the decoder’s greedy and four beam hypotheses and applying Platt calibration; language ID uses the ASR model’s own language scores. Turn‑end detection is a small readout on layer 18 trained on Smart Turn data, while speaker change and count readouts are on layer 12. The system is evaluated on a set of 1,000 public questions, on FLEURS, AMI, VoxConverse, Smart Turn, ICSI, and CochlScene datasets, and includes baselines such as Qwen3‑Omni \(30B‑A3B\), ECAPA, and pyannote 3.1.

**「Engineering Takeaway」** If you need a fast, single‑pass speech‑understanding pipeline for typed questions about audio windows, Marimba provides a ready‑to‑use, frozen ASR model with calibrated term spotting and lightweight readouts for language ID, turn‑end, and speaker tasks. The main caveat is that the turn‑end readout is in‑distribution on Smart Turn data and does not generalize to other turn‑end datasets, and the system does not handle unseen tasks like scene classification. The code and weights are Apache‑2.0 licensed and can be installed via pip install marimba‑audio.

**「Open Questions」** Is scoring ASR hypotheses plus Platt calibration a fair baseline for term spotting compared to a dedicated keyword‑spotting model? How can turn‑end detection be evaluated beyond the Smart Turn data distribution?

**Tags**: `#speech`, `#ASR`, `#audio-question-answering`, `#calibration`, `#multimodal`

---

<a id="item-ai-tech-3"></a>
### [Neo4j Virtual Graph GA](https://neo4j.com/blog/news/neo4j-virtual-graph-is-now-generally-available/) ⭐️ 7.0/10

Neo4j announced that Virtual Graph is now generally available in Neo4j Aura on Google Cloud, with AWS and Azure support planned soon. The GA product creates a zero-copy and zero-ETL graph abstraction over existing warehouse data from Snowflake, Databricks, Google BigQuery, and Apache Iceberg. It translates Cypher queries into SQL that runs in the customer warehouse, keeps data in place, and preserves governance. The source describes deterministic Cypher-to-SQL translation, support for GraphRAG, agent context, and analytics, and notes trade-offs involving read-only latency and Cypher coverage limits.

rss · Neo4j Blog · Nov 16, 17:25

**「Method」** Implementation involves creating a data source in the Aura console, providing warehouse credentials, and choosing a graph model manually, generated from the database schema, or generated from table metadata. The proposed model can be reviewed, edited, named, and saved before use. Virtual Graph compiles Cypher into SQL and pushes it down to the warehouse, with deterministic translation and unsupported queries returning GQL error code 42NG1 rather than failing silently. The announcement highlights quantified path patterns for bounded traversal and EXPLAIN support. GA also lists Aura API, Aura Agents, Graph Analytics, Bloom, AI dashboards, monitoring and logs, pause and resume, and Private Link, while upcoming capabilities include external IdP providers, Aura MCP servers, and multi-source Virtual Graphs via Composite.

**「Engineering Takeaway」** For application developers, Virtual Graph is most relevant when an existing warehouse already holds the data and a read-only analytical graph layer is acceptable. It can support GraphRAG, fraud detection, supply chain, and agent grounding without copying data, but latency depends on warehouse compute and SQL complexity and is often measured in seconds to minutes. Cypher coverage is incomplete, including unsupported OPTIONAL MATCH, EXISTS subqueries, shortest-path syntax, and unbounded variable-length patterns, though bounded quantified paths may help. Teams needing sub-second response times or native graph writes should consider AuraDB or a native Neo4j deployment.

**「Open Questions」** The source did not provide firm dates for AWS and Azure availability, Neo4j Enterprise Edition GA, or the planned Q1 2027 timeline. It also left questions about the scope of Cypher-to-SQL coverage improvements and the rollout of unsupported features.

**Tags**: `#GraphRAG`, `#context-engineering`, `#agentic-ux`, `#governance`, `#zero-ETL`

---

## Technology News

<a id="item-tech-news-1"></a>
### [vLLM v0.34.0 adds 10 new models, default extensible KV cache, and performance gains](https://github.com/vllm-project/vllm/releases/tag/v0.34.0) ⭐️ 8.0/10

vLLM v0.34.0, released on 2026-11-16, adds support for ten new models including Mistral Large 4 and MiniMax-M3.1-Flash, enables the extensible KV cache by default, and removes Model Runner V1. The release delivers up to 1.95× decode speedup on Blackwell/GB200 and 1.6× throughput on GLM-5.3-Flash, while requiring huggingface\_hub ≥ 2.0.0, ROCm 10.0, and a default block size of 64. Users must adjust the block size or use --block-size 16 to retain old behavior, and ROCm 7.2 images are no longer available.

github · khluu · Nov 16, 23:22

**「Background」** Before v0.34.0, the KV cache was allocated from a fixed estimate and Model Runner V1 was the sole GPU execution engine, with ROCm 7.2 support and a default block size of 16. Earlier releases provided basic model support and performance optimizations, but the default extensible KV cache and removal of V1 were not yet available.

**「Impact」** Developers must update to huggingface\_hub ≥ 2.0.0 and ROCm 10.0 and set the block size to 64 or use --block-size 16, otherwise their deployments will fail to start.

**Tags**: `#vLLM`, `#release`, `#performance`, `#model support`, `#KV cache`

---

<a id="item-tech-news-2"></a>
### [CMU Launches Free CS Lectures on YouTube](https://www.cs.cmu.edu/learn/) ⭐️ 8.0/10

Carnegie Mellon University has launched CS Learn, a free YouTube channel featuring full semester-long lectures from current computer science courses. The videos are produced using an automated pipeline built by students, allowing a small team to handle production. One course debuts each day this week, with additional courses planned for January, covering subjects such as AI, probability, and systems.

hackernews · pcompeau · Nov 16, 20:43 · [Discussion](https://news.ycombinator.com/item?id=50522980)

**「Open courseware precedent」** Universities have shared course materials online for years, and a commenter noted that MIT preceded CMU by roughly 25 years. CS Learn builds on that precedent by publishing full-semester lecture videos directly to YouTube, produced with student-built automation tools.

**「Impact」** Software engineers and AI practitioners gain free, timely access to advanced coursework from a top-tier program, potentially accelerating their learning. However, the initial release lacks courseware like projects and feedback mechanisms, which may limit its effectiveness for some learners.

**「Community Discussion」** The author, Phillip Compeau, argues that learning fundamentals makes AI a power tool rather than a replacement. Commenters expressed excitement for specific courses like Probability and Computing and ML Systems, while requesting others such as Intermediate Statistics and Distributed Systems. Some noted that lectures alone are insufficient without accompanying projects and feedback.

**Tags**: `#Free Online Courses`, `#Computer Science Education`, `#CMU CS Learn`, `#AI Fundamentals`

---

<a id="item-tech-news-3"></a>
### [Compromised Optimizely snippet served malware across Zoom, GitLab, CNN, BBC](https://blog.report-uri.com/worlds-largest-brands-infected-with-malware-via-optimizely/) ⭐️ 8.0/10

A compromised Optimizely snippet served malware to visitors of major websites including Zoom, GitLab, CNN, and BBC, according to a Report URI blog report. The incident is described as a supply-chain attack through Optimizely&\#x27;s tag-management system, and the report, as quoted in the discussion, states that Optimizely&\#x27;s CDN served exactly what it was given — this was not a CDN cache-poisoning attack. How the attacker gained write access to so many unrelated customer projects remains unexplained, and Optimizely&\#x27;s own sites \(www.optimizely.com and login.optimizely.com\) also carried the malicious code.

hackernews · kristjansson · Nov 16, 23:00 · [Discussion](https://news.ycombinator.com/item?id=50524767)

**「Background」** Optimizely operates a web experimentation and personalization platform that injects JavaScript snippets into customer websites via a tag management system, a common pattern where marketing teams add third-party code without engineering deployment cycles. Supply-chain attacks targeting such platforms have previously compromised widely embedded scripts, allowing malicious code to reach visitors of high-traffic sites including Zoom, GitLab, CNN, and BBC.

**「Impact」** The incident gives site operators a concrete reason to re-evaluate tag-management practices: because marketing teams can add tags without engineering review, one compromised vendor can inject malware across many unrelated customer sites at once. Commenters argue that large sites should vendor scripts rather than load them from vendors, and that both Optimizely and its customers need internal cool-downs, phased rollouts, and automatic security checks to catch a release like this.

**「Community discussion」** The most substantive exchange clarified the mechanics: eax-eip quoted the report that Optimizely&\#x27;s CDN served exactly what it was given, so this was not CDN cache-poisoning, and that the access vector across unrelated customer projects remains unknown. Others debated accountability and prevention — mcoliver argued Optimizely and major sites should have cool-downs, phased rollouts, and automatic security checks and should vendor scripts rather than serve from vendors, while stickfigure tied the risk to Google Tag Manager&\#x27;s design of letting marketing add tags without engineering, and thought-gap suggested NoScript to reduce exposure.

<details><summary>References</summary>
<ul>
<li><a href="https://gizmodo.com/sprawling-malware-attack-reportedly-affects-zoom-cnn-fox-news-peacock-and-170-others-2000840831">Sprawling Malware Attack Reportedly Affects Zoom and Other Major...</a></li>

</ul>
</details>

**Tags**: `#security`, `#supply-chain-attack`, `#web-development`, `#javascript`, `#tag-management`

---

<a id="item-tech-news-4"></a>
### [OpenAI begins embedded assessments with four independent evaluators](https://openai.com/index/our-first-phase-of-embedded-assessments) ⭐️ 7.0/10

OpenAI has launched its first phase of embedded assessments, engaging Apollo Research, METR, Transluce, and Goodfire to independently evaluate model alignment, safeguards, and monitoring systems. The announcement provides no further detail on the scope, methodology, timeline, or criteria for these assessments, nor what OpenAI will do with the findings.

rss · OpenAI News · Nov 16, 08:00

**「Background」** OpenAI&\#x27;s announcement introduces &\#x27;embedded assessments,&\#x27; a program that grants external research groups deep access to its models for independent safety testing. This follows earlier internal alignment evaluations and recent safety disclosures, such as the CSAM classifier rollout, reflecting a shift toward third‑party oversight of model alignment and safeguards. The participating groups—Apollo Research, METR, Transluce, and Goodfire—have prior experience in AI safety research and auditing.

**「Impact」** If the assessments are substantive and their findings are made public, this could improve external oversight of OpenAI&\#x27;s alignment practices. However, the announcement itself does not establish any concrete consequences, commitments, or timelines, so the actual impact remains uncertain until more information is released.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/our-first-phase-of-embedded-assessments/">Our first phase of embedded assessments - OpenAI</a></li>
<li><a href="https://cellcog.ai/blog/openai-embedded-assessments/">OpenAI Lets Four Outside Groups Test Its Models | CellCog</a></li>
<li><a href="https://aiweekly.co/alerts/openai-embeds-apollo-metr-transluce-goodfire-in-safety-audit">OpenAI Embeds Apollo , METR , Transluce , Goodfire in Safety ...</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#model alignment`, `#independent evaluation`, `#OpenAI`, `#AI monitoring`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Nvidia Leadership Crisis and Democratic Congress Could Reshape AI Trade](https://www.cnbc.com/2026/11/14/nvidia-ai-trade-data-centers-congress.html) ⭐️ 8.0/10

Nvidia founder and CEO Jensen Huang resigned after a tumultuous week, prompting Yorkville Ives to cut its price target to $225 from $300 while keeping a buy rating as the stock closed at $162.85. With Democrats winning control of Congress, analysts estimate 10% to 20% of planned data centers may not be built, even as demand still outstrips supply four to one.

rss · CNBC Finance · Nov 16, 12:13

**「Background」** The broader AI trade saw rotation into alternative chip makers, with AMD finishing up nearly 13% and the Nasdaq posting its best week since August, while Nvidia&\#x27;s interim CEO and CFO Colette Kress prepares for her first earnings report next Tuesday. The Roundhill Neocloud ETF remains down 39% since its August 2026 launch, amid concerns about balance sheet strength among smaller AI cloud companies.

**「Impact」** Alternative AI chip suppliers like AMD and Broadcom stand to gain if investors lose confidence in Nvidia, while existing hyperscale data centers may become more valuable as the overall compute supply tightens.

**Tags**: `#Nvidia`, `#AI chips`, `#ETF`, `#Congress policy`, `#Market analysis`

---