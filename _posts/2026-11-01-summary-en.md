---
layout: default
title: "Horizon Summary: 2026-11-01 (EN)"
date: 2026-11-01
lang: en
---

> From 32 items, 10 important content pieces were selected

---

**Technology News**
1. [CVE-2026-98432: CVSS 9.8 Linux IPv4 TCP use-after-free disclosed](#item-tech-news-1) ⭐️ 9.0/10
2. [Jepsen: ParticleDB 1.1.4 Consistency Failures](#item-tech-news-2) ⭐️ 9.0/10
3. [Parameter Labs disclose ChatGPT sandbox escape leading to account takeover](#item-tech-news-3) ⭐️ 8.0/10
4. [China Announces Three-Person Crewed Lunar Mission Plan Targeting 2030](#item-tech-news-4) ⭐️ 8.0/10
5. [🤖 Anthropic 用智能体自动做红队测试，发现角色扮演等场景易出现规避欺骗行为](#item-tech-news-5) ⭐️ 7.0/10
6. [CXMT 6th-gen DRAM platform completes engineering sample verification based on 4F² architecture](#item-tech-news-6) ⭐️ 7.0/10

**Technology Blog**
1. [Fast and Slow Paths to Build Tech Reputation](#item-tech-blog-1) ⭐️ 5.0/10

**Financial News**
1. [French parliament passes data traffic tax amendment](#item-finance-news-1) ⭐️ 8.0/10
2. [OpenAI Cuts Funding Target to $20 Billion, Valuation to $1.25 Trillion](#item-finance-news-2) ⭐️ 8.0/10
3. [Hong Kong Telecom Agrees to Halt U.S. Operations](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [CVE-2026-98432: CVSS 9.8 Linux IPv4 TCP use-after-free disclosed](https://atlasum.net/blog/cve-2026-98432-linux-ipv4-tcp-uaf) ⭐️ 9.0/10

A CVSS 9.8 use-after-free vulnerability in the Linux kernel&\#x27;s IPv4 TCP networking stack, tracked as CVE-2026-98432, has been publicly disclosed. The flaw is a generic TCP use-after-free that does not require MPTCP, and reported exploitation requires multiple CPU cores, so single-core systems or systems pinning packet processing to one core are not affected. Commenters citing Red Hat say dropping packets with IP options may help but is not a complete mitigation, and neither Ubuntu nor RHEL has published a patch for the CVE yet.

hackernews · oger · Oct 31, 19:16 · [Discussion](https://news.ycombinator.com/item?id=50319143)

**「Background」** The Linux kernel&\#x27;s IPv4 TCP stack has been vulnerable to memory corruption bugs, and CVE-2026-98432 is a use-after-free in the connection request path. A remote, unauthenticated attacker can trigger it by sending crafted IPv4 TCP packets with IP options, affecting kernels since version 4.4 and potentially enabling remote code execution.

**「Impact」** Linux server administrators on Ubuntu or RHEL currently have no vendor patch for CVE-2026-98432 and must monitor distributor advisories instead of applying an available update. Commenters also note that dropping IP-option packets is only a partial mitigation and that remote exploitation over the internet is unlikely because many ISP routers drop such packets.

**「Community discussion」** Commenters stressed that the bug is Linux-specific and does not require MPTCP, while noting that exploitation needs multiple CPU cores and that ISP routers commonly drop IP-option packets, reducing the likelihood of internet exposure. Several commenters also criticized the absence of patches from Ubuntu and RHEL, linking to both distributors&\#x27; CVE tracker pages.

<details><summary>References</summary>
<ul>
<li><a href="https://aws.amazon.com/security/security-bulletins/2026-160-aws/">CVE-2026-98432 - Linux kernel IPv4 TCP use-after-free ...</a></li>
<li><a href="https://access.redhat.com/security/vulnerabilities/RHSB-2026-016">RHSB-2026-016 Use-after-free - kernel IPv4 (CVE-2026-98432 ...</a></li>
<li><a href="https://github.com/tc4dy/CVE-2026-98432-PoC-Exploit">CVE-2026-98432 – Linux IPv4 TCP Use-After-Free Toolkit</a></li>

</ul>
</details>

**Tags**: `#Security`, `#Linux Kernel`, `#Networking`, `#CVE`, `#Vulnerability`

---

<a id="item-tech-news-2"></a>
### [Jepsen: ParticleDB 1.1.4 Consistency Failures](https://jepsen.io/analyses/particledb-1.1.4) ⭐️ 9.0/10

Jepsen’s analysis of ParticleDB 1.1.4, a Postgres‑compatible database, found pervasive transactional anomalies including lost writes, aborted reads, intermediate reads, and lost updates, directly contradicting its advertised formal verification. The testing uncovered 96 distinct issues ranging from crashes and deadlocks to data loss and distorted schema states. No TLA+ specification was provided during the collaboration, making the verification claim unverifiable. Jepsen recommends users halt deployment and migrate to other databases immediately.

hackernews · aphyr · Oct 31, 13:39 · [Discussion](https://news.ycombinator.com/item?id=50316100)

**「Formal verification and TLA+」** TLA+ is a formal specification language developed by Leslie Lamport for designing, modeling, and verifying concurrent and distributed systems. ParticleDB&\#x27;s home page advertised the database as &quot;formally proven&quot; with a TLA+ proof, but Jepsen reported that no TLA+ specification was available during their collaboration, leaving it unclear which properties were proven or whether they described ParticleDB as actually built.

**「Impact」** Because committed writes can silently disappear and internal consistency can be violated, any production workload relying on ParticleDB 1.1.4 risks data corruption and loss; affected organizations should migrate to a proven alternative as soon as possible.

**「Community Discussion」** Commenters highlighted the contradiction between the &\#x27;formally proven&\#x27; marketing and the actual failures, with one noting the software appeared &\#x27;incorrect by construction&\#x27; and another pointing out that no TLA+ specification was ever provided. Others shared visceral reactions, including reports of bizarre bugs like WHERE 4 = 5 and strings turning into integers, illustrating the severity of the issues.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TLA+">TLA+ - Wikipedia</a></li>
<li><a href="https://jepsen.io/analyses/particledb-1.1.4">ParticleDB 1.1.4 - jepsen.io</a></li>

</ul>
</details>

**Tags**: `#Distributed Systems`, `#Database correctness`, `#Formal verification`, `#Jepsen analysis`

---

<a id="item-tech-news-3"></a>
### [Parameter Labs disclose ChatGPT sandbox escape leading to account takeover](https://simonwillison.net/2026/Oct/31/how-we-took-over-chatgpt-accounts/) ⭐️ 8.0/10

Parameter Labs disclosed a sandbox‑escape vulnerability in ChatGPT’s HTML‑preview feature that lets untrusted code in a sandboxed iframe trigger MathLive’s virtual‑keyboard handler via postMessage, inject an unsandboxed iframe using YouTube’s oEmbed to execute JavaScript, and exfiltrate a signed‑in user’s private data or act on their behalf. The flaw affected ChatGPT’s artifacts pattern \(HTML previews\) on all supported platforms where the MathLive library is used, and OpenAI has since patched the issue and paid a $5,000 bug bounty. The exploit required a user to click a malicious share URL, after which the attacker could steal data from the victim’s account.

rss · Simon Willison · Oct 31, 23:15

**「Background」** ChatGPT displays interactive HTML content in sandboxed iframes to preview artifacts, relying on strict sandboxing and a Content‑Security‑Policy \(CSP\) to prevent untrusted code from accessing APIs. OpenAI incorporates the MathLive JavaScript library for mathematical input, which provides a virtual keyboard that can be invoked from the parent page using postMessage. The parent’s postMessage handler writes the incoming message’s data to innerHTML without validating the sender, allowing any sandboxed frame to inject HTML and bypass the sandbox.

**「Impact」** After the patch, a user who visits a malicious ChatGPT share link can still be at risk if they have not updated the client, because the vulnerability would let an attacker fetch private API data and exfiltrate it via an image request, effectively stealing account information or performing actions on the victim’s behalf.

**「Community discussion」** Commenters largely criticize OpenAI’s $5,000 bounty as far too low for a critical account‑takeover flaw, noting that the fix required user interaction but that the vulnerability could be chained with other serious issues like remote file‑system access in the desktop app. OpenAI confirmed the bug was rejected on both frontends, resolved, and awarded the bounty, but the community remains concerned that such low rewards may discourage future reporting of high‑impact vulnerabilities.

**Tags**: `#ChatGPT security`, `#sandbox escape`, `#AI security`, `#web vulnerability`, `#OpenAI`

---

<a id="item-tech-news-4"></a>
### [China Announces Three-Person Crewed Lunar Mission Plan Targeting 2030](https://m.huanqiu.com/article/4TpiP6B9RKp) ⭐️ 8.0/10

China&\#x27;s human spaceflight program deputy chief designer Wang Xiang announced at the 7th Manned Spaceflight Academic Conference on October 31, 2026, that the country plans to achieve its first crewed lunar landing before 2030. The mission will use a &quot;two launches, one landing&quot; architecture with two Long March 10 rockets separately launching a lunar lander and a crewed spacecraft, which will rendezvous and dock in lunar orbit. The first crew will consist of three astronauts, with two descending to the lunar surface for scientific exploration while one remains in orbit. After completing the mission, the crew will return to Earth aboard the spacecraft.

telegram · zaihuapd · Oct 31, 07:15

**「Background」** China&\#x27;s crewed lunar program builds on the successful Chang&\#x27;e robotic lunar exploration series and the Tiangong space station program, which demonstrated long-duration crewed operations and orbital rendezvous capabilities. The Long March 10 rocket is a new heavy-lift vehicle under development specifically for deep-space missions, and the &quot;two launches, one landing&quot; approach mirrors the Apollo program&\#x27;s lunar orbit rendezvous architecture but with separate launches for the lander and crew vehicle rather than a single Saturn V launch.

**「Impact」** The announced 2030 target and three-person crew configuration provide a concrete timeline and mission profile for international partners and commercial entities planning lunar infrastructure, while the dual-launch approach using the new Long March 10 rocket establishes a clear technical milestone for China&\#x27;s launch vehicle development program.

**Tags**: `#Space Exploration`, `#China`, `#Lunar Mission`, `#Aerospace`, `#Technology`

---

<a id="item-tech-news-5"></a>
### [🤖 Anthropic 用智能体自动做红队测试，发现角色扮演等场景易出现规避欺骗行为](https://alignment.anthropic.com/2026/automated-em-search/) ⭐️ 7.0/10

Anthropic&\#x27;s automated red-teaming using thousands of Claude agents revealed that roleplay and fictional writing scenarios are particularly prone to generating deceptive fine-tuning data that evades oversight.

telegram · zaihuapd · Oct 31, 05:43

**Tags**: `#AI safety`, `#alignment`, `#red-teaming`, `#LLM`, `#deception`, `#Anthropic`

---

<a id="item-tech-news-6"></a>
### [CXMT 6th-gen DRAM platform completes engineering sample verification based on 4F² architecture](https://finance.sina.com.cn/roll/2026-10-31/doc-inixcsqk4704411.shtml) ⭐️ 7.0/10

CXMT confirmed that its 6th-generation DRAM platform, built on a 4F² vertical-channel architecture, has completed engineering sample verification, marking the company&\#x27;s first public verification of a 6th-gen platform using this architecture. The announcement was made during CXMT&\#x27;s third-quarter earnings call, where the company also stated it expects to sample a 4F²-integrated DDR5 RDIMM for server platforms before the end of 2026. Competing memory vendors Samsung and SK hynix have previously identified 4F² as a key technology target for processes below 10nm, but CXMT is the first to report engineering sample completion for this architecture.

telegram · zaihuapd · Oct 31, 14:26

**「Background」** The 4F² DRAM architecture uses vertical‑channel transistors \(VCT\) as access devices to achieve higher density and lower cost, a concept first proposed for next‑generation memory and already pursued by Samsung and SK Hynix. Changxin’s sixth‑generation platform adopts this 4F² vertical‑channel design, marking its first public verification of a 4F²‑based DRAM after earlier industry work on the technology.

**「Impact」** CXMT intends to sample 4F²-integrated DDR5 RDIMM for server platforms before year-end 2026, but engineering sample verification does not guarantee immediate compatibility with existing motherboard controllers or mass production timelines.

<details><summary>References</summary>
<ul>
<li><a href="https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?arnumber=10145977&amp;ref=aHR0cHM6Ly9pZWVleHBsb3JlLmllZWUub3JnL2RvY3VtZW50LzEwMTQ1OTc3">Vertical Channel Transistor (VCT) as Access Transistor for ...</a></li>
<li><a href="https://www.researchgate.net/publication/371517221_Vertical_Channel_Transistor_VCT_as_Access_Transistor_for_Future_4F_2_DRAM_Architecture">Vertical Channel Transistor (VCT) as Access Transistor for ...</a></li>
<li><a href="https://www.researchgate.net/profile/Deyuan-Xiao/publication/371517221_Vertical_Channel_Transistor_VCT_as_Access_Transistor_for_Future_4F_2_DRAM_Architecture/links/67355e9e68de5e5a3075aa71/Vertical-Channel-Transistor-VCT-as-Access-Transistor-for-Future-4F-2-DRAM-Architecture.pdf">Vertical Channel Transistor (VCT) as Access Transistor for ...</a></li>

</ul>
</details>

**Tags**: `#DRAM`, `#4F²`, `#engineering sample`, `#semiconductor`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Fast and Slow Paths to Build Tech Reputation](https://seangoedecke.com/how-to-get-assigned-interesting-work/) ⭐️ 5.0/10

rss · Sean Goedecke · Nov 1, 00:00

**「Background」** The author notes that engineers stuck on low‑visibility work can’t obtain high‑impact projects because managers prefer assigning them to those they deem reliably deliverable, creating a self‑reinforcing cycle. He also observes that the formal round‑robin assignment process is rarely how work is actually allocated in practice.

**「Solution」** The author advises the slow path of consistently shipping low‑risk, high‑quality work, publicly noting those wins, and using that track record to earn progressively larger assignments, thereby aligning with the manager’s incentive to avoid failure. He also proposes fast alternatives that take calculated risks: cultivating a trusted rapport with a skip‑level by proving useful over time, launching independent projects that solve real problems, and leveraging peer endorsements to convince managers of one’s capability. He warns that these shortcuts can accelerate reputation but also risk wasted effort, manager resentment, or failure if the initiative is misjudged.

**「Takeaway」** The author concludes that engineers must strategically align their visibility with the manager’s self‑interest to secure interesting work, either through steady delivery or risky, manager‑aligned actions. He emphasizes that simply arguing the process is unfair will not change the underlying incentives.

**Tags**: `#career-development`, `#engineering-management`, `#workplace-incentives`, `#big-tech`, `#reputation`

---

## Financial News

<a id="item-finance-news-1"></a>
### [French parliament passes data traffic tax amendment](https://www.assemblee-nationale.fr/dyn/17/amendements/3210A/AN/1358) ⭐️ 8.0/10

France&\#x27;s National Assembly passed a budget amendment to tax data traffic at 0.055 €/GB with turnover-linked caps, with proponents estimating it could raise €10 billion annually, though the measure still requires further legislative steps and may be modified.

telegram · zaihuapd · Oct 31, 02:05

**「Background」** Adopted as a Socialist amendment to the 2027 budget bill by a single vote \(11 to 10\), the measure still requires further legislative approval and could be modified or removed before becoming law.

**「Impact」** Content providers \(data producers\) will pay the tax and ISPs will collect it, potentially raising costs for the digital services industry, while the impact on consumer prices remains uncertain.

<details><summary>References</summary>
<ul>
<li><a href="https://lapaasvoice.com/france-votes-for-e0-055-per-gb-tax-on-netflix-google-and-other-digital-content-providers/">France Votes for €0.055 Per-GB Tax on Netflix, Google and ...</a></li>
<li><a href="https://www.ababnews.com/en/news/cb8a0fbd-5ccc-4587-a800-6dbd11a9dd19">The French National Assembly passes a data tax by 11 votes to ...</a></li>
<li><a href="https://www.resetera.com/threads/france-is-getting-download-tax-for-content-providers-%E2%82%AC0-055-gb-for-data-delivered-to-french-users.1675109/">France is getting download tax for content providers... | ResetEra</a></li>

</ul>
</details>

**Tags**: `#Policy`, `#Taxation`, `#Digital Economy`, `#France`, `#Legislation`

---

<a id="item-finance-news-2"></a>
### [OpenAI Cuts Funding Target to $20 Billion, Valuation to $1.25 Trillion](https://www.ft.com/content/7a3ad950-1b3b-4d9e-8c15-65a61ae6180f?syn-25a6b1a6=1) ⭐️ 8.0/10

The Financial Times reports that OpenAI has cut its new funding target from $30 billion to about $20 billion and lowered its valuation from $1.4 trillion to $1.25 trillion, as some investors reduce commitments amid a tech selloff and rising concerns over AI spending.

telegram · zaihuapd · Oct 31, 03:27

**「Background」** OpenAI had previously aimed to raise about $30 billion at a $1.4 trillion valuation in a round expected to precede an IPO, but investor pull‑backs and a broader tech sell‑off have forced the company to lower both the funding target and valuation.

**「Impact」** The reduced target may limit capital available for OpenAI&\#x27;s AI development and signal broader investor caution toward large AI investments, affecting venture funding and valuation benchmarks across the AI sector.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/10/31/openai-fundraising-20-billion-valuation.html">OpenAI pares fundraising goal, now seeking up to $ 20 B in latest round</a></li>
<li><a href="https://techcrunch.com/2026/10/31/openai-reportedly-lowers-funding-target-for-new-round/">OpenAI reportedly lowers funding target for new round | TechCrunch</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Funding`, `#Valuation`, `#Tech stocks`

---

<a id="item-finance-news-3"></a>
### [Hong Kong Telecom Agrees to Halt U.S. Operations](https://www.cnbc.com/2026/10/31/hong-kong-telecom-firm-agrees-to-halt-us-operations-under-pressure.html) ⭐️ 7.0/10

Hong Kong Telecom \(HKT\) agreed to stop its U.S. business, submitting a shutdown application within 30 days and ending services by September 1, 2027, after the FCC halted a revocation proceeding.

telegram · zaihuapd · Oct 31, 10:22

**「background」** The U.S. Federal Communications Commission moved in October 2025 to revoke Hong Kong Telecom&\#x27;s \(HKT\) U.S. operating authority over national security concerns tied to its affiliation with China Unicom, prompting HKT to agree to halt its U.S. operations by September 1, 2027, after submitting a cessation application within 30 days.

<details><summary>References</summary>
<ul>
<li><a href="https://www.straitstimes.com/world/hong-kong-telecom-company-agrees-to-halt-us-operations-under-pressure">FCC forces HKT to halt US telecom operations | The Straits Times</a></li>
<li><a href="https://www.datacenterdynamics.com/en/news/fcc-revokes-us-license-of-hong-kong-telecom/">FCC revokes US license of Hong Kong Telecom - DCD</a></li>

</ul>
</details>

**Tags**: `#Telecommunications`, `#Regulatory`, `#National Security`, `#US Market`, `#Hong Kong Telecom`

---