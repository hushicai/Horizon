---
layout: default
title: "Horizon Summary: 2026-10-24 (ZH)"
date: 2026-10-24
lang: zh
---

> 从 33 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Amazon Trainium adds native PyTorch training support](#item-tech-news-1) ⭐️ 8.0/10
2. [iPhone 安全研究与越狱讨论引发社区关注](#item-tech-news-2) ⭐️ 7.0/10
3. [Now Google says it might use your Gmail and Google Photos data to target ads](#item-tech-news-3) ⭐️ 7.0/10
4. [Kimi K3.1 Pro 上线 API，承诺 11 月 4 日开放权重](#item-tech-news-4) ⭐️ 7.0/10
5. [字节火山引擎发布 Seedance 2.5 4K 视频生成模型](#item-tech-news-5) ⭐️ 7.0/10
6. [DeepSeek AI 大肥鱼刷屏 B 站评论区](#item-tech-news-6) ⭐️ 7.0/10
7. [国办发文：减缓 AI 就业替代影响](#item-tech-news-7) ⭐️ 7.0/10
8. [瑞典政府办公室封禁 ChatGPT 与 Claude](#item-tech-news-8) ⭐️ 7.0/10
9. [Kimi K3.1-Pro 发布：3 万亿参数开放权重模型](#item-tech-news-9) ⭐️ 7.0/10

**财经新闻**
1. [欧盟废止对华太阳能玻璃反倾销和反补贴关税](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Amazon Trainium adds native PyTorch training support](https://newsletter.semianalysis.com/p/amazons-trainium-takes-a-strike-at) ⭐️ 8.0/10

Amazon announced that its Trainium chip, previously known for inference, now supports native PyTorch training, providing a GPU alternative for machine learning workloads. The announcement includes high‑quality continuous integration, TorchTitan support, and a GPU‑Impossible Profiler. This is a vendor claim that expands Trainium’s capabilities beyond inference. Developers and organizations using ML training can consider Trainium as an alternative hardware platform for PyTorch‑based workloads.

rss · Semianalysis · 10月23日 19:06

**「Trainium 现已支持原生 PyTorch 训练」** Amazon 的 Trainium 是专为 AI 工作负载设计的芯片，最初侧重推理，但如今也支持训练，如 5 月 5 日关于 Trainium 和 Graviton 芯片的介绍所述。 Trainium 的 Neuron Kernel Interface（NKI）提供直接访问芯片 ISA 的能力，使开发者能够精细编程并充分发挥性能。

**「Impact」** ML practitioners can now run PyTorch training directly on Trainium hardware, broadening hardware options and potentially reducing reliance on GPUs for training tasks. This may lower costs for organizations that adopt Trainium for training workloads.

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aboutamazon.com/news/aws/aws-trainium-graviton-ai-chips-explained">AWS Trainium and Graviton chips: How Amazon powers AI and ...</a></li>
<li><a href="https://aws.amazon.com/ai/machine-learning/trainium/">AI Accelerator - AWS Trainium - AWS - aws.amazon.com</a></li>

</ul>
</details>

**标签**: `#Trainium`, `#ML hardware`, `#PyTorch`, `#AI training`, `#Amazon`

---

<a id="item-tech-news-2"></a>
### [iPhone 安全研究与越狱讨论引发社区关注](https://blog.calif.io/p/iphone) ⭐️ 7.0/10

Hacker News 上关于成功攻击 iPhone 的讨论引发了对 iOS 安全、越狱以及苹果生态系统的广泛关注。讨论中提到的攻击似么实现了对 iPhone 的控制，但具体的技术细节和影响范围并未在摘要中详细说明。

hackernews · pavel\_lishin · 10月23日 16:21 · [社区讨论](https://news.ycombinator.com/item?id=50211474)

**「背景」** The successful hack, reported by Calif Newsletter, relies on prior iOS vulnerability research and the existing jailbreak ecosystem that enables modification of iOS firmware.

**「社区讨论」** 部分用户表达了对苹果生态系统限制的不满，认为即使越狱后不更新系统，苹果仍可通过检测越狱状态限制 iCloud 和 iMessage 等服务的使用。另有用户指出，安全研究者难以获得先进设备的访问权限，苹果的&quot;信任网络访问&quot;计划可能成为技术壁垒而非保障。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.calif.io/p/iphone">iPhone - Calif Newsletter</a></li>

</ul>
</details>

**标签**: `#iPhone security`, `#iOS jailbreak`, `#cybersecurity`, `#mobile security`, `#Apple ecosystem`

---

<a id="item-tech-news-3"></a>
### [Now Google says it might use your Gmail and Google Photos data to target ads](https://www.theverge.com/tech/1017600/google-personal-intelligence-privacy-policy-ads-update) ⭐️ 7.0/10

Google updates privacy policy to permit using Gmail and Google Photos data for ad targeting, raising significant privacy concerns.

hackernews · JustSkyfall · 10月23日 19:34 · [社区讨论](https://news.ycombinator.com/item?id=50214218)

**标签**: `#google-privacy`, `#data-usage`, `#ads-targeting`, `#gmail`, `#google-photos`

---

<a id="item-tech-news-4"></a>
### [Kimi K3.1 Pro 上线 API，承诺 11 月 4 日开放权重](https://simonwillison.net/2026/Oct/23/kimi-k31-pro/) ⭐️ 7.0/10

Moonshot 的 Kimi K3.1 Pro 已在 Kimi API 上线，标准版定价为每百万输入 token 2 美元、每百万输出 token 10 美元，并提供速度快 2-3 倍但价格翻倍的“高速”版本（输入缓存命中除外）。模型目前尚未开放权重，Moonshot 仅承诺将于 2026 年 11 月 4 日发布完整模型权重。Artificial Analysis 将 Kimi K3.1 Pro 评为 55 分，仅低于 Claude Opus 5.5 的 58 分，高于 Claude Fable 5.1、GPT-6 Astra 与 Gemini 4 Argon 的 53 分；Moonshot 自测显示其与 Opus 5.5 和 GPT-6 Astra 大致持平。作者已通过兼容 OpenAI 的端点调用该模型，并验证其支持 low、medium、max 三种推理等级。

rss · Simon Willison · 10月23日 19:40

**「Kimi K3.1 Pro 模型发布背景」** Kimi K3.1 Pro 模型已于 2026 年 10 月 23 日在 Kimi API 上发布，但尚未开放权重，预计将于 2026 年 11 月 4 日发布。该模型提供 &quot;Highspeed&quot; 版本，速度比标准版快 2-3 倍，且价格是标准版的两倍（输入 2000 美元/百万 token，输出 10000 美元/百万 token）。其基准测试显示与 Opus 5.5 和 GPT-6 Astra 相当，在部分领域略胜一筹。

**「影响」** 开发者可直接通过 Moonshot 的 OpenAI 兼容 API 调用 Kimi K3.1 Pro，但需注意“高速”版本输出成本为标准版两倍，且因权重尚未开放，自托管或微调需等待 11 月 4 日的承诺兑现。

**标签**: `#Kimi K3.1 Pro`, `#LLM API`, `#AI benchmarks`, `#model pricing`

---

<a id="item-tech-news-5"></a>
### [字节火山引擎发布 Seedance 2.5 4K 视频生成模型](https://mp.weixin.qq.com/s/yUa8oh-IWfl5lDQzGSKWeg) ⭐️ 7.0/10

字节跳动旗下火山引擎正式发布 Seedance 2.5 4K 视频生成模型，这是该系列目前最强版本。模型经过专项训练，强化了对人物表情、细微动作与画面细节的学习；支持 Draft 模式，可先用 480P 样片快速验证分镜，满意后再生成 4K 正片。该模型具备 10-bit 色深，色彩层次丰富、过渡平滑，画面质感可胜任大荧幕播放。目前仅面向部分企业客户试用，后续或将逐步扩大开放范围。

telegram · zaihuapd · 10月23日 08:27

**「背景」** 火山引擎此前已推出 Seedance 系列视频生成模型，用于从文本或图像合成视频内容。4K 分辨率对生成画面的细节保真度和计算资源提出更高要求；Draft 模式指先以低分辨率生成样片预览，再按需输出高分辨率正片的创作流程。

**「影响」** 企业级视频创作团队可通过 Draft 模式以低成本验证创意分镜，再输出符合影院级规格的 4K 成片，缩短从概念到成片的迭代周期；但因目前仅限定向试用，广泛可用性仍待后续开放进度。

**标签**: `#AI`, `#Video Generation`, `#Machine Learning`, `#ByteDance`, `#4K Model`

---

<a id="item-tech-news-6"></a>
### [DeepSeek AI 大肥鱼刷屏 B 站评论区](https://mp.weixin.qq.com/s/MBrJeHsJ7nIql0PCVCIxgA) ⭐️ 7.0/10

开发者 c1overzz 发布了开源插件 dsh-bili-scroll，使 DeepSeek Agent 能自动搜索 B 站视频并发表评论，导致用户以“大肥鱼”人设集体刷屏评论；社区随后开发了 dafeiyu-cleaner 浏览器插件来过滤此类 AI 评论。

telegram · zaihuapd · 10月23日 11:10

**「事件背景」** 该事件展示了 AI 代理在社交媒体上的自动化交互能力，反映了 DeepSeek Agent 与 B 站评论区的交互模式。此前类似的 AI 评论生成工具已存在，但本次通过统一人设和自动化评论机制引发了更大规模的社区反弹。

**标签**: `#AI agents`, `#open source`, `#social media automation`, `#Bilibili`, `#community tools`

---

<a id="item-tech-news-7"></a>
### [国办发文：减缓 AI 就业替代影响](https://mp.weixin.qq.com/s/St8URoMYcV-voM7kLAK3Bw) ⭐️ 7.0/10

国务院办公厅印发《关于适应人工智能技术发展助力构建就业友好型发展方式的意见》，旨在减缓人工智能应用对就业的替代影响。文件要求优先在劳动力紧缺、环境高危岗位推广 AI，稳慎把握其在劳动密集型行业的应用范围、力度和节奏，并鼓励企业探索建立失业缓冲期制度，提前告知受影响劳动者并提供转型转岗就业支持。

telegram · zaihuapd · 10月23日 12:54

**「政策背景」** 此前我国已就促进就业与人工智能融合发展出台过指导意见，要求把握好 AI 应用与就业保障之间的关系。国务院办公厅此次新发的《意见》进一步明确了在劳动力紧缺、环境高危等岗位优先推广 AI 的原则，以及在劳动密集型行业中稳慎控制应用范围、力度和节奏的要求，标志着政策在具体实施路径上更加细化。

**「实际影响」** 企业在劳动密集型行业的 AI 应用将受到范围、力度和节奏的政策约束，受影响的劳动者将获得提前告知和转型就业支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gov.cn/zhengce/zhengceku/202610/content_7084108.htm">国务院办公厅关于适应人工智能技术发展助力构建就业友好型发展方式的...</a></li>
<li><a href="https://rst.hubei.gov.cn/bmdt/rsyw/202610/t20261023_6040324.shtml">国务院办公厅印发《关于适应人工智能技术发展助力构建就业友好型发展...</a></li>
<li><a href="https://www.jcgov.gov.cn/dtxx/gwyyw/202610/t20261024_2405126.shtml">国务院办公厅印发《关于适应人工智能技术发展助力构建就业友好型发展...</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#employment`, `#China`, `#technology regulation`, `#AI ethics`

---

<a id="item-tech-news-8"></a>
### [瑞典政府办公室封禁 ChatGPT 与 Claude](https://www.sverigesradio.se/artikel/chat-gpt-och-claude-forbjuder-regeringskansliet) ⭐️ 7.0/10

瑞典政府办公室（Regeringskansliet）从下周开始在员工工作设备上封禁 ChatGPT 和 Claude，要求改用已批准的 AI 工具（如微软 Copilot）。此前该机构已限制 DeepSeek。数字化主管表示，使用未签约的 AI 服务可能危及信息安全。瑞典税务局、国家机构事务局（SiS）已采取类似封禁，Kronofogden 正在研究是否跟进。

telegram · zaihuapd · 10月23日 14:11

**「背景」** 瑞典政府办公室（Regeringskansliet）此前已对 DeepSeek 实施限制。此次在员工工作电脑上封禁 ChatGPT 与 Claude，是其在 AI 服务安全管控上持续收紧的延续。

**「影响」** 员工必须改用微软 Copilot 等已验证的 AI 工具，这增加了企业在采用 AI 时的合规负担，并要求 IT 部门评估替代方案以满足安全要求。

**标签**: `#AI policy`, `#enterprise AI`, `#government procurement`, `#security concerns`, `#Microsoft Copilot`

---

<a id="item-tech-news-9"></a>
### [Kimi K3.1-Pro 发布：3 万亿参数开放权重模型](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 7.0/10

Kimi 发布 K3.1-Pro，这是 K3.1 系列首款模型，定位为目前最强的 3 万亿参数开放权重模型，支持 100 万 token 上下文。模型在编程、三维创作、金融研究及复杂智能体任务上显著提升：Terminal-Bench 4.0 得分 65.7%，超越 GPT-6 Astra 的 58.2%，接近 Claude Opus 5.5 的 66.4%；内部长任务编程测试从 55.95% 升至 61.2%。三维建模方面，BenchCAD 工具辅助得分达 92.7%；金融内部测试建模与研究分别提升 7.2 与 11.6 分，模拟经营表现约为 K3 的 4.2 倍。陈述级幻觉率从 23.4% 降至 8.3%。模型已接入 Kimi、Work、Code 与 API，完整权重计划于 2026 年 11 月 4 日前发布。

telegram · zaihuapd · 10月23日 17:14

**「背景」** K3.1-Pro 基于前代 K3 模型扩大训练规模而来，K3 此前已具备编程与推理能力。此次发布同步推出 Highspeed 版本，速度为标准版 2—3 倍，面向对延迟敏感的应用场景。开放权重承诺延续了 Kimi 此前的开放策略。

**「影响」** 开发者可立即在 Kimi、Work、Code 及 API 中使用 K3.1-Pro 进行长流程编程、游戏开发（Unity/Unreal/Godot）、三维建模（Blender/CAD 脚本）与金融建模任务；完整权重发布后可自行部署或微调。需注意官方提示：幻觉率降低不代表日常使用错误率同等下降。

**标签**: `#Artificial Intelligence`, `#Large Language Models`, `#Open Source`, `#Software Engineering`, `#Technology News`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [欧盟废止对华太阳能玻璃反倾销和反补贴关税](https://www.163.com/dy/article/L9R94K6105484D40.html) ⭐️ 7.0/10

据该报道，欧盟委员会废止对原产于中国的太阳能玻璃征收的反倾销和反补贴关税，10 月 22 日生效。此前最高税率为 84.2%，自 2025 年 7 月 22 日起缴纳的关税可申请退还，不计利息。

telegram · zaihuapd · 10月23日 06:54

**「背景」** 欧盟此前出于保护本土产业对该产品征收反倾销和反补贴关税，但现在称境内已无活跃生产企业，且中国进口占欧盟市场份额仅约 3%，远低于原调查期间的 30.5%。

**标签**: `#EU trade policy`, `#China solar industry`, `#anti-dumping duties`, `#solar supply chain`, `#tariff revocation`

---