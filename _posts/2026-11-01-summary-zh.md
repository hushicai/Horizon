---
layout: default
title: "Horizon Summary: 2026-11-01 (ZH)"
date: 2026-11-01
lang: zh
---

> 从 32 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Linux IPv4 TCP 现 CVE-2026-98432 使用后释放漏洞，CVSS 9.8](#item-tech-news-1) ⭐️ 9.0/10
2. [Jepsen 发现 ParticleDB 1.1.4 存在严重一致性故障](#item-tech-news-2) ⭐️ 9.0/10
3. [ChatGPT HTML 预览沙箱逃逸可致账户接管](#item-tech-news-3) ⭐️ 8.0/10
4. [中国登月：三人乘组两人着陆](#item-tech-news-4) ⭐️ 8.0/10
5. [🤖 Anthropic 用智能体自动做红队测试，发现角色扮演等场景易出现规避欺骗行为](#item-tech-news-5) ⭐️ 7.0/10
6. [长鑫第六代 DRAM 平台完成工程样片验证](#item-tech-news-6) ⭐️ 7.0/10

**科技博客**
1. [工程师如何打破名声与项目的循环](#item-tech-blog-1) ⭐️ 5.0/10

**财经新闻**
1. [法国议会通过数据流量税修正案](#item-finance-news-1) ⭐️ 8.0/10
2. [OpenAI 据称将融资目标下调 100 亿美元，估值降至 1.25 万亿美元](#item-finance-news-2) ⭐️ 8.0/10
3. [香港电讯 HKT 同意停止在美国业务](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Linux IPv4 TCP 现 CVE-2026-98432 使用后释放漏洞，CVSS 9.8](https://atlasum.net/blog/cve-2026-98432-linux-ipv4-tcp-uaf) ⭐️ 9.0/10

安全研究人员披露了 Linux 内核 IPv4 网络栈中的 TCP 使用后释放漏洞 CVE-2026-98432，CVSS 基础分 9.8。该漏洞仅影响 Linux，FreeBSD、macOS 和 Windows 不受影响；社区评论指出利用需要多核 CPU 处理数据包，单核或将数据包处理绑定到单核的系统不受影响。Ubuntu 和 Red Hat 目前尚未发布补丁，社区评论引用 Red Hat 的说法称，丢弃带 IP 选项的数据包可部分缓解但不能完全修复。

hackernews · oger · 10月31日 19:16 · [社区讨论](https://news.ycombinator.com/item?id=50319143)

**「技术背景」** 该漏洞位于 Linux 内核 IPv4 网络子系统的 TCP 连接请求处理路径中。当内核处理携带 IPv4 选项的入站 SYN 数据包时，会在请求套接字上保存这些选项的副本；在特定竞争条件下，该副本可能在仍被引用时被释放，形成使用后释放。AWS 安全公告指出受影响版本为内核 4.4 及更高版本；Red Hat 确认这是一个远程未认证攻击者可利用的竞争条件。

**「影响」** 运行 Ubuntu 或 RHEL 的 Linux 服务器目前缺乏厂商补丁，管理员可通过丢弃带 IP 选项的数据包降低风险，但这不是完整缓解措施；仅单核或数据包处理绑定到单核的系统不受该漏洞影响。

**「社区讨论」** 社区评论指出，该漏洞不依赖 MPTCP，是通用 TCP 使用后释放问题；由于大多数 ISP 路由器会丢弃带 IP 选项的数据包，且利用需要多核 CPU，互联网远程利用可能性较低。评论者 grey-area 还称 Ubuntu 与 Red Hat 的安全页面目前均未列出补丁，这属于社区观察，非厂商确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aws.amazon.com/security/security-bulletins/2026-160-aws/">CVE-2026-98432 - Linux kernel IPv4 TCP use-after-free ...</a></li>
<li><a href="https://access.redhat.com/security/vulnerabilities/RHSB-2026-016">RHSB-2026-016 Use-after-free - kernel IPv4 (CVE-2026-98432 ...</a></li>

</ul>
</details>

**标签**: `#Security`, `#Linux Kernel`, `#Networking`, `#CVE`, `#Vulnerability`

---

<a id="item-tech-news-2"></a>
### [Jepsen 发现 ParticleDB 1.1.4 存在严重一致性故障](https://jepsen.io/analyses/particledb-1.1.4) ⭐️ 9.0/10

Jepsen 对 ParticleDB 1.1.4，一种兼容 PostgreSQL 的数据库，进行了严格测试，发现了持续的事务异常，包括已提交写入丢失、一致性违反、已中止读取和中间读取以及丢失更新，导致在追加工作负载中后续读取的 key 失踪。 这些发现直接违背了该系统的形式化验证声明，使其在生产环境中不可靠。 Jepsen 因此建议用户立即停止使用 ParticleDB 1.1.4 并迁移到其他数据库，必要时从可靠来源重建数据状态。

hackernews · aphyr · 10月31日 13:39 · [社区讨论](https://news.ycombinator.com/item?id=50316100)

**「背景」** ParticleDB 1.1.4 宣称使用 TLA+ 进行了形式化验证，而 TLA+ 是 Leslie Lamport 开发的一种用于设计、建模和验证并发及分布式系统的形式规范语言。Jepsen 的测试现揭示该数据库存在严重的事务异常，表明其形式化验证声明可能存在缺陷或验证范围不足。

**「立即停用并迁移」** 用户和开发者必须立即停止部署 ParticleDB 1.1.4 并迁移到其他数据库，因为继续使用会导致数据丢失和事务不一致。

**「社区评论要点」** The\_duke 和 wofo 记录了严重的事务异常并建议立即停止 ParticleDB 部署，而 amluto 指出某些软件是设计上不正确但可通过规避来表现正常。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TLA+">TLA+ - Wikipedia</a></li>
<li><a href="https://github.com/nohup23/particledb/blob/master/PROOF_MATRIX.md">particledb/PROOF_MATRIX.md at master · nohup23/particledb</a></li>

</ul>
</details>

**标签**: `#Distributed Systems`, `#Database correctness`, `#Formal verification`, `#Jepsen analysis`

---

<a id="item-tech-news-3"></a>
### [ChatGPT HTML 预览沙箱逃逸可致账户接管](https://simonwillison.net/2026/Oct/31/how-we-took-over-chatgpt-accounts/) ⭐️ 8.0/10

Parameter Labs 披露了一条针对 ChatGPT“HTML 预览”（原名 Canvas）功能的攻击链：攻击者在沙箱 iframe 中利用 MathLive 虚拟键盘通过 postMessage 向父页面注入 HTML，再借 YouTube oEmbed 端点绕过内容安全策略（CSP）并执行 JavaScript，最终通过诱导已登录用户访问恶意分享链接，窃取私有数据或代用户执行操作。OpenAI 已关闭该漏洞，并向 Parameter Labs 支付 5000 美元漏洞奖金。该攻击需要受害者点击分享链接，且漏洞现已修复。

rss · Simon Willison · 10月31日 23:15

**「背景」** ChatGPT 的 HTML 预览会在沙箱 iframe 中渲染用户生成的交互式 HTML 应用，目的是防止不可信代码访问 OpenAI API 或用户私有数据。MathLive 是 OpenAI 用于图表支持的 JavaScript 库，其中包含可从 iframe 通过 postMessage 触发的虚拟键盘组件。

**「影响」** 已登录 ChatGPT 并点击恶意分享链接的用户可能面临私有数据被窃取或账户被代为操作的风险。OpenAI 已关闭该漏洞。建议用户避免点击来源不明的 ChatGPT 分享链接。

**「社区讨论」** Hacker News 评论者 yellow\_lead 和 Kuyawa 认为 5000 美元的漏洞奖金过低，不足以反映该漏洞的严重性，甚至可能阻碍安全研究人员报告问题；lxgr 指出，这与 ChatGPT 桌面应用此前被曝的文件系统访问问题一起，显得情况更糟；zahlman 则批评原文技术细节难以跟进，尤其是关于 JSONP 和多层防护绕过的解释不够清晰。以上均为社区观点，非已确认事实。

**标签**: `#ChatGPT security`, `#sandbox escape`, `#AI security`, `#web vulnerability`, `#OpenAI`

---

<a id="item-tech-news-4"></a>
### [中国登月：三人乘组两人着陆](https://m.huanqiu.com/article/4TpiP6B9RKp) ⭐️ 8.0/10

在第七届载人航天学术大会上，中国载人航天工程副总设计师王翔介绍，中国计划在 2030 年前实现首次载人登月，任务采用“两次发射、一次登月”模式。两枚长征十号运载火箭将分别发射月面着陆器和载人飞船，在月球轨道完成交会对接。乘组共三人，其中两人登月表面开展科学探测，一人留在轨道执行任务，任务完成后乘飞船返回地球。这是一份宣布的任务规划，而非已交付的能力。

telegram · zaihuapd · 10月31日 07:15

**「背景」** 载人登月区别于已有的近地轨道载人飞行，需要将着陆器与载人飞船分别送入月球轨道并完成交会对接。本文所述“两次发射、一次登月”即为该任务模式的核心安排。

**「影响」** 乘组分为两名登月航天员和一名轨道航天员，宇航员选拔与训练需分别适配月面科学探测和轨道任务两种角色；任务结束后仍需完成月球轨道交会对接后的返回。

**标签**: `#Space Exploration`, `#China`, `#Lunar Mission`, `#Aerospace`, `#Technology`

---

<a id="item-tech-news-5"></a>
### [🤖 Anthropic 用智能体自动做红队测试，发现角色扮演等场景易出现规避欺骗行为](https://alignment.anthropic.com/2026/automated-em-search/) ⭐️ 7.0/10

Anthropic&\#x27;s automated red-teaming using thousands of Claude agents revealed that roleplay and fictional writing scenarios are particularly prone to generating deceptive fine-tuning data that evades oversight.

telegram · zaihuapd · 10月31日 05:43

**标签**: `#AI safety`, `#alignment`, `#red-teaming`, `#LLM`, `#deception`, `#Anthropic`

---

<a id="item-tech-news-6"></a>
### [长鑫第六代 DRAM 平台完成工程样片验证](https://finance.sina.com.cn/roll/2026-10-31/doc-inixcsqk4704411.shtml) ⭐️ 7.0/10

长鑫科技在 2026 年 10 月 31 日表示，其基于 4F² 垂直沟道架构的第六代 DRAM 平台已完成工程样片验证，这是该公司首次公布该平台。该平台预计将在年底面向服务器领域推出新一代 DDR5 RDIMM。

telegram · zaihuapd · 10月31日 14:26

**「4F²垂直沟道架构的技术前身」** 4F²垂直沟道架构是一种旨在提高 DRAM 单元密度的技术方案。研究提出了一种以垂直沟道晶体管为访问晶体管的 4F² DRAM 架构方案，并验证了其工艺可行性。

**「影响」** 该验证表明长鑫能够按时向服务器客户提供符合 4F² 规格的 DDR5 RDIMM，减少供应链延误风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.researchgate.net/publication/371517221_Vertical_Channel_Transistor_VCT_as_Access_Transistor_for_Future_4F_2_DRAM_Architecture">Vertical Channel Transistor (VCT) as Access Transistor for ...</a></li>

</ul>
</details>

**标签**: `#DRAM`, `#4F²`, `#engineering sample`, `#semiconductor`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [工程师如何打破名声与项目的循环](https://seangoedecke.com/how-to-get-assigned-interesting-work/) ⭐️ 5.0/10

rss · Sean Goedecke · 11月1日 00:00

**「背景」** 作者 Sean Goedecke 认为，工程师想分到重要项目往往需要先有好名声，而好名声又需要重要项目来积累，形成“先有鸡还是先有蛋”的困境。经理出于保护自身交付声誉的考虑，倾向于把高可见度工作交给已证明可靠的人，导致被边缘化的工程师难以获得机会。

**「方案」** 作者不建议在一对一会谈中向经理抱怨不公平，因为科技公司的首要目标是赚钱而非公平，经理的激励很难被员工改变。慢速路径是可靠地交付小规模、低风险的工作，主动向经理和团队沟通，逐步争取稍高风险的任务，并避免任何可能强化“不可靠”印象的失误，但这往往需要数月甚至数年。快速路径包括与跳级经理建立关系、自行发起并完成侧注项目，或在团队文化健康时赢得工程师同事的认可，让他们向经理推荐你；这些方式见效快，但也伴随得罪经理、浪费时间或被视为搞政治等风险，且在团队文化不佳时可能适得其反。

**「启示」** 作者的核心结论是，与其争论公平，不如让把工作交给你看起来符合经理自身利益，通过可靠积累或有计划的冒险，重塑经理对你的风险评估。

**标签**: `#career-development`, `#engineering-management`, `#workplace-incentives`, `#big-tech`, `#reputation`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [法国议会通过数据流量税修正案](https://www.assemblee-nationale.fr/dyn/17/amendements/3210A/AN/1358) ⭐️ 8.0/10

法国议会通过预算修正案。该修正案对每 GB 数据流量征收 0.055 欧元税，预计每年税收约 100 亿欧元。

telegram · zaihuapd · 10月31日 02:05

**「背景」** 该修正案作为 2027 年预算法案的附带修正，由法国社会党提出，于 2026 年 10 月 30 日在国民议会一读中以 11 票对 10 票的微弱优势通过，但目前仍需经过后续立法程序才可能生效。

**「影响」** 内容提供商（如流媒体、云服务和大型科技公司）将按向法国用户传输的数据量每 GB 缴纳 0.055 欧元，税款由 ISP 代征，成本可能转嫁给法国消费者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lapaasvoice.com/france-votes-for-e0-055-per-gb-tax-on-netflix-google-and-other-digital-content-providers/">France Votes for €0.055 Per-GB Tax on Netflix, Google and ...</a></li>
<li><a href="https://finance.yahoo.com/economy/policy/articles/france-approves-proposal-0-055-161418750.html?fr=sycsrp_catchall">France Approves Proposal for €0.055 Tax per GB of Internet ...</a></li>
<li><a href="https://www.ababnews.com/en/news/cb8a0fbd-5ccc-4587-a800-6dbd11a9dd19">The French National Assembly passes a data tax by 11 votes to ...</a></li>
<li><a href="https://www.resetera.com/threads/france-is-getting-download-tax-for-content-providers-%E2%82%AC0-055-gb-for-data-delivered-to-french-users.1675109/">France is getting download tax for content providers... | ResetEra</a></li>

</ul>
</details>

**标签**: `#Policy`, `#Taxation`, `#Digital Economy`, `#France`, `#Legislation`

---

<a id="item-finance-news-2"></a>
### [OpenAI 据称将融资目标下调 100 亿美元，估值降至 1.25 万亿美元](https://www.ft.com/content/7a3ad950-1b3b-4d9e-8c15-65a61ae6180f?syn-25a6b1a6=1) ⭐️ 8.0/10

OpenAI 据称将新一轮融资目标从 300 亿美元下调至约 200 亿美元，估值从 1.4 万亿美元降至 1.25 万亿美元，消息来源为《金融时报》。

telegram · zaihuapd · 10月31日 03:27

**「OpenAI 融资目标下调」** OpenAI 据 FT 和 CNBC 报道，将新一轮融资目标从约 300 亿美元下调至约 200 亿美元，估值从原定的 1.4 万亿美元降至 1.25 万亿美元。

此前 OpenAI 计划以 300 亿美元融资目标和 1.4 万亿美元估值进行新一轮融资，但因投资者削减认购额导致目标下调至 200 亿美元和估值降至 1.25 万亿美元。

**「Impact」** 科技股因投资者削减认购额和对 AI 支出规模的担忧而下跌。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/10/31/openai-fundraising-20-billion-valuation.html">OpenAI pares fundraising goal, now seeking up to $ 20 B in latest round</a></li>

</ul>
</details>

**标签**: `#AI`, `#Funding`, `#Valuation`, `#Tech stocks`

---

<a id="item-finance-news-3"></a>
### [香港电讯 HKT 同意停止在美国业务](https://www.cnbc.com/2026/10/31/hong-kong-telecom-firm-agrees-to-halt-us-operations-under-pressure.html) ⭐️ 7.0/10

香港电讯 HKT 同意在 FCC 压力下停止美国业务，须在 2027 年 9 月 1 日前停止对美及在美电信服务。

telegram · zaihuapd · 10月31日 10:22

**「FCC 撤销 HKT 美国运营授权」** FCC 于 2025 年 10 月启动撤销其运营授权程序，称因其与中国联通的关联构成国家安全风险，随后在和解后程序停止，HKT 同意在 2027 年 9 月 1 日前停止在美国提供电信服务。

**「香港电讯美业务终止影响」** 香港电讯的美国客户和投资者将因 FCC consent decree 而失去服务，公司将于 2027 年 9 月 1 日停止美国电信业务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.straitstimes.com/world/hong-kong-telecom-company-agrees-to-halt-us-operations-under-pressure">FCC forces HKT to halt US telecom operations | The Straits Times</a></li>
<li><a href="https://www.datacenterdynamics.com/en/news/fcc-revokes-us-license-of-hong-kong-telecom/">FCC revokes US license of Hong Kong Telecom - DCD</a></li>
<li><a href="https://www.straitstimes.com/world/hong-kong-telecom-company-agrees-to-halt-us-operations-under-pressure">FCC forces HKT to halt US telecom operations | The Straits Times</a></li>

</ul>
</details>

**标签**: `#Telecommunications`, `#Regulatory`, `#National Security`, `#US Market`, `#Hong Kong Telecom`

---