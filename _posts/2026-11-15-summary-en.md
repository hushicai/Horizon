---
layout: default
title: "Horizon Summary: 2026-11-15 (EN)"
date: 2026-11-15
lang: en
---

> From 39 items, 14 important content pieces were selected

---

**Technology News**
1. [SpaceX Catches Starship Booster to End Flight 15](#item-tech-news-1) ⭐️ 8.0/10
2. [Lovable-built apps exposed passport details and 200K private messages due to insufficient row-level security](#item-tech-news-2) ⭐️ 8.0/10
3. [Tech companies again try to redefine privacy](#item-tech-news-3) ⭐️ 8.0/10
4. [Cloudflare open-sources Kitesurf, a stateless AI-agent browser on Workers](#item-tech-news-4) ⭐️ 8.0/10
5. [Nvidia allegedly kept GPU prices high via circular financing deals](#item-tech-news-5) ⭐️ 7.0/10
6. [Show HN: DeepSeek V3 Reimplemented in About 200 Lines of Jax](#item-tech-news-6) ⭐️ 7.0/10
7. [Google Research details Antigravity /teamwork advances for science and engineering](#item-tech-news-7) ⭐️ 7.0/10
8. [Italy Fines Meta $887M Over Android Data Access](#item-tech-news-8) ⭐️ 7.0/10
9. [datasette-llm 0.1a11](#item-tech-news-9) ⭐️ 7.0/10
10. [OpenAI disbands dedicated robotics team, shifts to general AI models](#item-tech-news-10) ⭐️ 7.0/10
11. [Apple reaffirms visionOS commitment, shifts focus to smart glasses by 2027](#item-tech-news-11) ⭐️ 7.0/10
12. [FAA nationwide ground stop traced to router failure during copper-to-fiber upgrade](#item-tech-news-12) ⭐️ 7.0/10

**Financial News**
1. [Nvidia Turmoil and the AI Trade](#item-finance-news-1) ⭐️ 8.0/10
2. [Foundation Future Industries misses payroll after CEO&\#x27;s $4.6M home loan](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [SpaceX Catches Starship Booster to End Flight 15](https://www.spacex.com/launches/starship-flight-15) ⭐️ 8.0/10

SpaceX reported that it caught the Starship booster at the end of Flight 15, citing its own social-media post and launch broadcast. The claim is a vendor announcement rather than an independently verified result, and the supplied material gives no flight data, recovery details, or confirmation of which vehicle was caught. SpaceX has not provided further technical specifications in the source.

hackernews · ls612 · Nov 14, 21:22 · [Discussion](https://news.ycombinator.com/item?id=50500963)

**「Background」** SpaceX&\#x27;s Starship is a fully reusable super heavy-lift launch system consisting of the Super Heavy booster and the Starship upper stage. Catching the booster with the launch tower&\#x27;s mechanical arms is a key milestone in SpaceX&\#x27;s effort to make the system rapidly reusable, avoiding the cost of building new boosters for each flight. The integrated flight test program has been expanding Starship&\#x27;s capabilities through successive flights.

**「Community discussion」** Several commenters compared Starship to the Space Shuttle, describing it as a fully reusable booster with an upper-stage stack that avoids the Shuttle&\#x27;s side-mounted orbiter, while others said the heat shield must hold up and that catching and re-flying the same vehicles remains unproven. One commenter expressed uncertainty about the final mass fraction to orbit and argued that 100% reusability would still be preferable to Falcon 9&\#x27;s estimated 60% cost reusability.

**Tags**: `#SpaceX`, `#Starship`, `#Reusable rockets`, `#Aerospace engineering`, `#Space launch`

---

<a id="item-tech-news-2"></a>
### [Lovable-built apps exposed passport details and 200K private messages due to insufficient row-level security](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

A security report described Lovable-built apps exposing passport details and more than 200,000 private messages because of insufficient row-level security. Lovable&\#x27;s head of security confirmed the root cause and said the platform automatically scans every app before publishing, offers a free deeper SAST scan, and provides optional auto-fix and publish blocking for flagged findings. A commenter noted that Supabase reportedly addressed related defaults on October 30, but that existing projects may still retain the older, less restrictive settings.

hackernews · armcat · Nov 14, 17:43 · [Discussion](https://news.ycombinator.com/item?id=50499017)

**「Background」** Row-Level Security \(RLS\) is a PostgreSQL feature that restricts database access at the row level based on user identity, and Supabase—the backend platform widely used by Lovable-generated apps—historically defaulted to permissive access for ease of onboarding. A Supabase changelog update effective October 30, 2026 tightened defaults for new tables in the public schema, but existing tables retain their prior grants, leaving many older projects exposed. The Crissy Field report scanned 159,041 Lovable projects and found passport numbers, payment details, and over 200,000 chat messages reachable without authentication because RLS policies were either missing or too broad.

**「Impact」** Affected users&\#x27; passport details and private messages were exposed in Lovable-built apps because row-level security was insufficiently configured. Developers using Lovable with Supabase should audit existing projects for permissive row-level security defaults, since a reported October 30 fix may not apply retroactively to older projects.

**「Community discussion」** Commenters disagreed over responsibility: one user argued Supabase bears blame for historically permissive onboarding defaults that may persist in existing projects, while Lovable&\#x27;s head of security said its scanning and auto-fix tools are designed to catch this class of row-level security failure. Others noted that AI-generated apps are numerous and easily inspected, lowering the barrier to exposure, though data breaches predate AI.

<details><summary>References</summary>
<ul>
<li><a href="https://cybernews.com/security/lovable-ai-apps-expose-personal-information/">Lovable AI apps exposed sensitive data in open databases ...</a></li>
<li><a href="https://dev.to/feldsparaiagent/three-supabase-access-bugs-a-demo-never-shows-and-the-test-that-does-e05">Three Supabase access bugs a demo never shows... - DEV Community</a></li>

</ul>
</details>

**Tags**: `#AI`, `#LLM`, `#security`, `#row-level-security`, `#data-privacy`

---

<a id="item-tech-news-3"></a>
### [Tech companies again try to redefine privacy](https://www.eff.org/deeplinks/2026/11/tech-companies-are-trying-shift-entire-concept-privacy-again) ⭐️ 8.0/10

The item reports that tech companies are again attempting to shift the concept of privacy, an effort that could affect the tech industry and workers whose data may be handled by AI systems, according to an EFF analysis. The discussion focused on AI workplace surveillance and digital rights and drew 469 points and 175 comments.

hackernews · gslin · Nov 14, 12:45 · [Discussion](https://news.ycombinator.com/item?id=50496602)

**「Rising AI integration threatens traditional privacy」** Recent analyses show that major technology firms are embedding AI into daily life - including AI powered smart glasses, real time transcription services, and autonomous office agents - that continuously collects biometric and conversational data. This shifts the expectation of privacy, enabling meeting recordings without consent, local model storage, and potential data monetization if a company goes bankrupt, as the BBC reported that bankrupt firms may sell private information. These practices clash with UN Human Rights Article 12, which forbids arbitrary interference with privacy, prompting calls for new safeguards.

**「Potential workplace effects」** The reported debate could affect how workers, developers, and digital-rights advocates handle consent and data exposure in AI systems. The supplied comments raised concerns about AI meeting recording and opt-out pressure, though the available material does not establish a specific policy change or shipped capability.

**「Reader concerns」** Commenters discussed AI meeting recording and whether disabling AI notetakers should become a norm, with one asking how to minimize exposure while noting that staying employed may make opting out difficult. Another commenter questioned whether local transcription without saving or export can avoid retention, and others raised accessibility and human rights implications.

<details><summary>References</summary>
<ul>
<li><a href="https://thetechabc.com/beyond-the-screen-how-ai-glasses-and-surveillance-are-redefining-privacy-in-2026/">Beyond the Screen: How AI Glasses and Surveillance Are Redefining ...</a></li>
<li><a href="https://www.lexology.com/library/detail.aspx?g=e11e3ec9-c684-4c3d-984f-8c15dde289b9">Agentic AI in the Workplace : November 2026 - Lexology</a></li>
<li><a href="https://www.bbc.com/technology">BBC Technology | Technology , Health, Environment, AI</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#digital-rights`, `#AI-surveillance`, `#EFF`, `#workplace-technology`

---

<a id="item-tech-news-4"></a>
### [Cloudflare open-sources Kitesurf, a stateless AI-agent browser on Workers](https://www.phoronix.com/news/Cloudflare-Kitesurf-Open-Source) ⭐️ 8.0/10

Cloudflare has open-sourced Kitesurf, a stateless browser for AI agents, under the Apache 2.0 license, with the code published on GitHub. Built on Cloudflare Workers, it parses HTML, processes CSS, and executes JavaScript without a browser container. Cloudflare claims it uses less CPU and memory than Chromium and scales on demand across the global Workers network, but the source offers no independent benchmarks, version numbers, or measured results to confirm those figures.

telegram · zaihuapd · Nov 14, 09:33

**「Background」** AI agents that operate on the web are typically driven through headless Chromium instances in containers, which carry significant CPU and memory overhead. Kitesurf is positioned against that model by removing the container requirement and running browser functions directly on Cloudflare&\#x27;s Workers edge network.

**「Impact」** Developers building AI agents gain an Apache 2.0-licensed option that runs on Cloudflare&\#x27;s Workers network without managing browser containers, but the lower-resource claims are vendor-stated, so adoption depends on Workers compatibility and the specific sites an agent must handle.

**Tags**: `#AI agents`, `#Open source`, `#Cloudflare Workers`, `#Web browsers`, `#Software engineering`

---

<a id="item-tech-news-5"></a>
### [Nvidia allegedly kept GPU prices high via circular financing deals](https://www.techspot.com/news/114558-nvidia-deliberately-kept-gpu-prices-high-through-circular.html) ⭐️ 7.0/10

Nvidia is reported to have deliberately kept GPU prices high through circular financing arrangements, affecting buyers of high‑end cards such as the RTX 6000. The strategy is said to sustain elevated prices despite market pressure, fueling debate over whether AI compute demand is genuine. The claim remains unverified and is contested by community members.

hackernews · madihaa · Nov 14, 22:26 · [Discussion](https://news.ycombinator.com/item?id=50501631)

**「Background」** Nvidia&\#x27;s circular financing strategy, where the company acts as vendor, financier, investor, and guarantor to fund GPU purchases, has been documented as inflating prices by making sales appear credit‑driven rather than demand‑driven. Recent examples, such as Apollo lending $7 billion to xAI for leasing Nvidia chips through a shell company where Nvidia is the anchor investor, illustrate how this loop can sustain high GPU prices and limit competitor access. This model, compared to pre‑2008 subprime structures, underpins the allegations that Nvidia deliberately kept GPU prices elevated.

**「Impact」** High GPU prices may force users to rely on cloud‑based AI services and subscription models rather than owning hardware, increasing ongoing costs for developers and organizations.

**「Community Discussion」** wqnt argues that AI compute demand is real and that Nvidia&\#x27;s financing deals are used to restrict competitors&\#x27; access to GPUs and favor neocloud customers, while hadlock suggests that a price drop would make home AI viable and reduce subscription reliance.

<details><summary>References</summary>
<ul>
<li><a href="https://builtin.com/articles/nvidias-circular-financing-analysis">What Does Nvidia’s Latest Circular Financing Plan Mean for ...</a></li>
<li><a href="https://trendytechtribe.com/money-and-power/the-silicon-debt-trap">Nvidia GPU Financing Loop 2026: The New Subprime Structure</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#GPU pricing`, `#AI compute`, `#circular financing`, `#semiconductors`

---

<a id="item-tech-news-6"></a>
### [Show HN: DeepSeek V3 Reimplemented in About 200 Lines of Jax](https://github.com/Vaibhaav-Tiwari/deepseek-v3-jax) ⭐️ 7.0/10

Vaibhaav Tiwari posted a Show HN project that reimplements DeepSeek V3 in roughly 200 lines of pure Jax. The GitHub repository is an independent, compact implementation intended for study and experimentation, not an official DeepSeek release, and the post provides no benchmark or accuracy results.

hackernews · VaibhaavTiwari · Nov 14, 15:04 · [Discussion](https://news.ycombinator.com/item?id=50497589)

**「Background」** DeepSeek V3 is a large language model, and a from-scratch Jax implementation differs from running official inference code because it exposes the model&\#x27;s components for reading and modification. Jax is a Python library for high-performance numerical computing and automatic differentiation, so the project is most useful to developers already familiar with Python and ML workflows.

**「Impact」** Developers who want to inspect or modify DeepSeek V3 internals can use the code as a reading reference, but they will still need to validate correctness and performance themselves because the post reports no benchmarks.

**「Community discussion」** Commenters welcomed the project as a first-principles learning exercise, and one developer reported getting it to run end-to-end on an AMD RX 7600 XT 16GB with ROCm after setting two environment variables, including HSA\_OVERRIDE\_GFX\_VERSION=11.0.0. Another commenter asked for a roadmap to build intuition about inference for developers comfortable with Java and Python but new to the area.

**Tags**: `#DeepSeek-V3`, `#JAX`, `#LLM-implementation`, `#machine-learning`, `#open-source`

---

<a id="item-tech-news-7"></a>
### [Google Research details Antigravity /teamwork advances for science and engineering](https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/) ⭐️ 7.0/10

Google Research published a post describing advances in /teamwork, the multi-agent collaboration feature of its Antigravity AI engineering tool, with examples drawn from math, science, coding, and engineering work. The supplied material includes no post text, so the specific capabilities and any measured results behind the claimed advances cannot be confirmed here. A commenter writing on the team&\#x27;s behalf said this post is not the feature&\#x27;s first outing — parts of /teamwork were announced earlier on Antigravity&\#x27;s own blog — and that its purpose is to showcase example tasks rather than to re-announce the feature. That same commenter said the team is &quot;constantly improving/evolving /teamwork and pushing those changes for external users,&quot; indicating the feature is being shipped to users outside Google rather than remaining a research-only prototype.

hackernews · acossta · Nov 14, 13:20 · [Discussion](https://news.ycombinator.com/item?id=50496811)

**「Background: Antigravity Teamwork advances multi-agent AI workflows」** Antigravity&\#x27;s Teamwork is a multi‑agent framework that enables collaborative AI engineering across research teams, tackling open‑ended problems in mathematics, hardware simulation, and optimization. A recent Google blog post reports that researchers from Google, CUHK, USC, and CMU used Teamwork&\#x27;s Long Proof pattern—adapted from Stellar Colosseum in Antigravity—to prove the 2013 Courtade–Kumar conjecture in full generality. The official Antigravity team post describes a functional OS experiment running 93 subagents, performing 15,314 model calls, and processing 339 million input tokens, indicating higher autonomy and less quality drop‑off than single-model approaches.

**「Impact」** For developers evaluating multi-agent coding harnesses, the post is a capability showcase rather than usage documentation: one commenter said it &quot;doesn&\#x27;t tell me how to use it,&quot; and the team member pointed readers to the earlier Antigravity announcement for additional visualizations and detail. Because the team says improvements are pushed to external users, /teamwork is reachable outside Google, but the supplied material contains no benchmark or independently measured comparison supporting the claimed advances.

**「Community discussion」** Commenter stbenjam argued that it is unclear how /teamwork differs from Claude dynamic workflows and that Antigravity&\#x27;s harness &quot;feels very behind,&quot; citing the lack of an auto mode and saying /goal was announced long after he had felt the need for it in CC or Codex. Commenter jdw64 reported that auditor-based verification does not resolve the auditor&\#x27;s own reliability problem, saying that in Antigravity&\#x27;s Argon multi-agent model auditors still produce false completion reports; both are user assessments rather than verified findings.

<details><summary>References</summary>
<ul>
<li><a href="https://antigravity.google/blog/teamwork-when-ai-becomes-a-research-partner/">Teamwork : when AI becomes a research ... | Google Antigravity Blog</a></li>
<li><a href="https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/">Advancing science &amp; engineering with Antigravity ’s / teamwork</a></li>
<li><a href="https://devlery.com/en/blog/google-antigravity-teamwork-preview">Antigravity Ran 93 Agents and Put a Price Tag on OS Demos - Devlery</a></li>

</ul>
</details>

**Tags**: `#AI tools`, `#multi-agent systems`, `#Google research`, `#teamwork`, `#open source`

---

<a id="item-tech-news-8"></a>
### [Italy Fines Meta $887M Over Android Data Access](https://www.reuters.com/world/italy-fines-meta-887-million-over-android-users-data-access-2026-11-14/) ⭐️ 7.0/10

Italy fined Meta $887 million over alleged access to Android users&\#x27; data without consent, according to the supplied report. The case concerned whether Meta accessed Android users&\#x27; data, potentially photographs and videos, without meeting consent requirements. The fine was reported to be about 0.47% of Meta&\#x27;s global revenue, though the available material did not provide extensive technical detail.

hackernews · giuliomagnifico · Nov 14, 13:48 · [Discussion](https://news.ycombinator.com/item?id=50497009)

**「Background」** The enforcement depended on concepts from the EU GDPR, including consent and lawful data access, as well as how Android permissions are intended to work. The supplied material did not include enough technical detail to explain the underlying mechanism.

**「Impact」** The fine could increase regulatory pressure on Meta and other large platforms over data access and consent. For affected users and developers, it highlights unresolved questions about how consent is obtained and recorded for Android data access, though the practical effect remains uncertain.

**「Community Discussion」** Commenters disputed the technical explanation, with one asking how Meta accessed users&\#x27; photos without consent and whether an Android exploit was used, noting the article lacked details. Another commenter questioned what specific objection remained if consent had been given at some point, while a third asked whether there is proof that such fines are actually paid.

**Tags**: `#GDPR`, `#Meta`, `#Android`, `#data privacy`, `#tech regulation`

---

<a id="item-tech-news-9"></a>
### [datasette-llm 0.1a11](https://simonwillison.net/2026/Nov/14/datasette-llm/) ⭐️ 7.0/10

Datasette-llm 0.1a11 adds OpenAI-compatible endpoint support, allowing local LLM usage via LM Studio, Ollama, and llama.cpp with Datasette.

rss · Simon Willison · Nov 14, 23:59

**Tags**: `#datasette`, `#LLM`, `#OpenAI`, `#open source`, `#software engineering`

---

<a id="item-tech-news-10"></a>
### [OpenAI disbands dedicated robotics team, shifts to general AI models](https://fortune.com/2026/11/13/openai-disbands-robotics-team-as-its-general-models-start-running-robots/) ⭐️ 7.0/10

OpenAI has disbanded its standalone robotics team and moved its researchers into broader research groups, the company said, because general frontier models such as GPT-6 Astra can now directly control robots to perform tasks. Robotics remains part of OpenAI&\#x27;s long-term vision, but there is no longer a dedicated internal robotics division. The company is still developing its own humanoid robots and aims to show one publicly in 2027, after ending its partnership with Figure in February 2025 and having previously disbanded an earlier robotics team in 2020.

telegram · zaihuapd · Nov 14, 04:00

**「Background」** OpenAI&\#x27;s earlier robotics effort was disbanded in 2020 and rebuilt in 2024, when it also partnered with Figure; that partnership ended in February 2025. The company has continued developing its own humanoid robot, with a first public demonstration targeted for 2027.

**「Impact」** OpenAI employees who worked on robotics are now embedded in general research teams rather than a standalone unit, so there is no dedicated OpenAI robotics group for external partners or developers to coordinate with; the company&\#x27;s humanoid robot work continues internally with a first public demonstration targeted for 2027.

**Tags**: `#OpenAI`, `#robotics`, `#AI models`, `#embodied AI`, `#industry strategy`

---

<a id="item-tech-news-11"></a>
### [Apple reaffirms visionOS commitment, shifts focus to smart glasses by 2027](https://weibo.com/1642634100/Rro0OkKLj) ⭐️ 7.0/10

At the &quot;Meet with Apple&quot; developer event, Apple&\#x27;s spatial computing product manager reaffirmed the company&\#x27;s long-term commitment to the visionOS platform while indicating a strategic shift away from heavy investment in Vision Pro hardware. The most recent Vision Pro update, featuring the M5 chip, was released in October 2025, and Apple is planning to launch next-generation smart glasses by the end of 2027, marking a departure from its prior hardware-centric roadmap. Analyst Ming-Chi Kuo&\#x27;s separate prediction that the next headset won&\#x27;t arrive until late 2028 further highlights the uncertainty around Apple&\#x27;s next spatial computing hardware cycle.

telegram · zaihuapd · Nov 14, 15:23

**「Background」** The Vision Pro is Apple&\#x27;s spatial-computing headset, and its most recent hardware refresh moved to the M5 chip in October 2025. Reports from September 2026 described Apple&\#x27;s first smart glasses as a late-2027 product closer to camera-and-audio glasses than a display-equipped Vision Pro, with a redesigned headset expected later.

<details><summary>References</summary>
<ul>
<li><a href="https://appleinsider.com/articles/26/09/27/apples-smart-glasses-predicted-for-2027-upgraded-apple-vision-pro-2028">Apple plans late 2027 smart glasses and a revised Vision Pro</a></li>
<li><a href="https://www.techrepublic.com/article/news-apple-smart-glasses-2027-vision-pro-redesign/">Apple Smart Glasses Could Arrive in 2027: What We Know So Far</a></li>

</ul>
</details>

**Tags**: `#visionOS`, `#Apple`, `#spatial computing`, `#AR/VR`, `#smart glasses`

---

<a id="item-tech-news-12"></a>
### [FAA nationwide ground stop traced to router failure during copper-to-fiber upgrade](https://www.theverge.com/transportation/1033898/faa-ground-stop-sean-duffy-faa-copper-wire) ⭐️ 7.0/10

The FAA ordered a nationwide ground stop on Friday after a router malfunction during a routine copper-to-fiber upgrade at a remote facility, grounding thousands of flights. U.S. Transportation Secretary Sean Duffy said the new router sent more than 1,000 connection requests to other routers every 4 to 5 seconds, disrupting radar signals and aircraft communications. The root cause is still unclear, with Duffy citing possible hardware failure, misconfiguration, or an error by contractor L3Harris.

telegram · zaihuapd · Nov 15, 02:10

**「Context」** The FAA operates air traffic control using networked radar and communications systems at facilities across the United States. Replacing aging copper lines with fiber is a routine part of maintaining that infrastructure.

**「Impact」** Thousands of flights were grounded nationwide, and radar and aircraft communications were disrupted at the affected facility. Duffy has called on Congress to approve additional funding for air traffic control modernization.

**Tags**: `#aviation`, `#networking`, `#infrastructure`, `#incident-analysis`, `#transportation-technology`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Nvidia Turmoil and the AI Trade](https://www.cnbc.com/2026/11/14/nvidia-ai-trade-data-centers-congress.html) ⭐️ 8.0/10

After Nvidia founder and CEO Jensen Huang resigned, experts said AI chip demand could shift toward rivals if investor trust in Nvidia falls, while a Democratic-controlled Congress following the November 3 election may push back on data centers; analyst Dan Ives estimated that this could mean 10% to 20% of planned data centers may not be built.

rss · CNBC Finance · Nov 14, 15:50

**「Background」** Nvidia&\#x27;s recent leadership turmoil led to Huang&\#x27;s resignation, and investors and analysts discussed how that could reshape the AI chip trade.

**Tags**: `#Nvidia`, `#AI chip market`, `#ETF analysis`, `#Democratic Congress`

---

<a id="item-finance-news-2"></a>
### [Foundation Future Industries misses payroll after CEO&\#x27;s $4.6M home loan](https://www.cnbc.com/2026/11/14/foundation-payroll-ceo-loan.html) ⭐️ 7.0/10

Foundation Future Industries, a robotics startup advised by Eric Trump, missed payroll on Oct. 30, 2026, after its CEO borrowed $4.6 million from the company to buy a home, people familiar with the matter say.

rss · CNBC Finance · Nov 14, 12:00

**「Background」** Foundation Future Industries, founded in April 2024 and advised by Eric Trump, promoted unproven military robots while its CEO borrowed $4.6 million from company funds to buy a home, contributing to payroll failures and drawing nepotism allegations from Sen. Elizabeth Warren after $24 million in Pentagon contract claims were traced to an acquired firm rather than direct wins.

**「Impact」** Employees have not received paychecks since Oct. 30, 2026, after the CEO&\#x27;s $4.6 million home loan depleted the company&\#x27;s cash reserves.

**Tags**: `#Defense contracting`, `#Corporate governance`, `#Startups`, `#Conflict of interest`, `#Robotics`

---