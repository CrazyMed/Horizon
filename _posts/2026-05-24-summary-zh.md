---
layout: default
title: "Horizon 每日速递: 2026-05-24"
date: 2026-05-24
lang: zh
---

> 从 22 条内容中筛选出 9 条重要资讯

---

1. [苹果开源 corecrypto 密码库，附量子安全形式化验证](#item-1) ⭐️ 8.0/10
2. [微软内部大规模推广 Anthropic 的 Claude Code](#item-2) ⭐️ 8.0/10
3. [通过逆向工程成功反汇编 80386 处理器微代码](#item-3) ⭐️ 7.0/10
4. [Anthropic Project Glasswing：AI 发现逾万高危漏洞](#item-4) ⭐️ 7.0/10
5. [富途被罚 185 亿元 老虎证券被罚没 41.1 亿元 无牌在华开展证券业务](#item-5) ⭐️ 7.0/10
6. [正确使用 <dl> 元素引发 HTML 无障碍性讨论](#item-6) ⭐️ 6.0/10
7. [德州女子因 Facebook 发布水质污染信息被捕](#item-7) ⭐️ 6.0/10
8. [微软财报意外披露 OpenAI 单季度约 115 亿美元亏损](#item-8) ⭐️ 6.0/10
9. [美商海盗船采用长鑫存储芯片，DDR5 内存价格 2027 年有望下调](#item-9) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [苹果开源 corecrypto 密码库，附量子安全形式化验证](https://security.apple.com/blog/formal-verification-corecrypto/) ⭐️ 8.0/10

苹果于 5 月 22 日发布了 corecrypto 源代码，公开了其 ML-KEM 和 ML-DSA 量子安全算法实现，并首次提供端到端的形式化验证证明。这些证明数学上验证了 C 代码和手工优化的 ARM64 汇编与 NIST 标准严格一致。 此次发布为超过 25 亿台活跃设备带来了密码学严谨性，保护 iMessage、VPN 等服务免受未来量子计算机威胁。通过发布验证工具和 Isabelle 理论库供独立专家审查，苹果为安全关键软件设定了新的透明度和信任行业标准。 ML-KEM（前身为 CRYSTALS-Kyber）是一种密钥封装机制，而 ML-DSA（前身为 CRYSTALS-Dilithium）是一种数字签名算法——两者均于 2024 年 8 月被 NIST 标准化。苹果的形式化验证使用 Isabelle/HOL 证明助手来证明实现方案的数学正确性，弥合了抽象规范与实际部署代码之间的差距。

telegram · zaihuapd · 05月23日 04:49

**背景**: 后量子密码学应对的是足够强大的量子计算机对当前加密技术的威胁。当前的 RSA 和椭圆曲线密码学可能被量子计算机上的肖尔算法破解，使得 ML-KEM 和 ML-DSA 等格密码算法对长期安全至关重要。形式化验证使用数学证明来验证代码正确实现了规范，消除了测试可能遗漏的整类错误。Isabelle 是一种广泛使用的交互式定理证明器，用于形式数学和验证。

**标签**: `#quantum-resistant cryptography`, `#formal verification`, `#open-source security`, `#Apple`, `#NIST standards`, `#post-quantum encryption`

---

<a id="item-2"></a>
## [微软内部大规模推广 Anthropic 的 Claude Code](https://t.me/zaihuapd/41535) ⭐️ 8.0/10

微软正在其核心工程团队（包括 CoreAI、Windows 和 Microsoft 365 部门）广泛部署 Anthropic 的 Claude Code，并鼓励非技术员工使用该工具进行原型设计。软件工程师现在必须同时安装 Claude Code 和 GitHub Copilot，并提供两者之间的对比反馈。 这一发展具有重大意义，因为拥有 GitHub Copilot 的微软正在大规模内部推广直接竞争对手的产品。强制要求提供对比反馈表明，微软承认 Claude Code 的竞争优势，并将其作为内部基准来评估自家产品与 AI 编程领域领先竞争对手的差距。 负责 Windows、Microsoft 365 和 Outlook 产品的体验与设备团队已被指示安装 Claude Code。该命令不仅限于工程师，还扩展到非技术员工，表明微软正在推动整个组织采用 AI 辅助原型设计。尽管如此，微软仍在继续向外部客户销售 GitHub Copilot。

telegram · zaihuapd · 05月23日 06:05

**背景**: Claude Code 是 Anthropic 开发的代理编程工具，能够读取代码库、编辑文件、运行命令并与开发工具集成。Anthropic 由包括 Dario 和 Daniela Amodei 在内的前 OpenAI 研究人员于 2021 年创立，已累计融资超过 73 亿美元，截至 2026 年估值约为 615 亿美元。GitHub Copilot 是微软的 AI 代码补全工具，微软内部采用 Claude Code 代表了其对市场竞争压力的重要认可。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://code.claude.com/docs/en/overview">Overview - Claude Code Docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI coding tools`, `#Claude Code`, `#Microsoft`, `#Anthropic`, `#GitHub Copilot`, `#Enterprise AI adoption`

---

<a id="item-3"></a>
## [通过逆向工程成功反汇编 80386 处理器微代码](https://www.reenigne.org/blog/80386-microcode-disassembled/) ⭐️ 7.0/10

一篇技术博客文章详细记录了对 Intel 80386 处理器微代码的完整逆向工程和反汇编。作者成功提取并分析了控制这款标志性 32 位处理器执行机器指令的内部微编程代码。 这项工作为深入了解 80386 的微架构实现提供了前所未有的视角，保护了关于复古处理器内部结构不可替代的知识。这些发现支持 z386 等正在进行的开源硬件项目，并使研究 x86 架构演进的研究者受益。 博客详细介绍了提取技术，包括分析高分辨率芯片图像以从硅片中重建微代码。Hacker News 讨论提出了关于该过程是否输出 Verilog 或需要建模单个晶体管的问题，相关的 z386 项目旨在使用原始微代码实现 80386 处理器。

hackernews · nand2mario · 05月23日 12:11 · [社区讨论](https://news.ycombinator.com/item?id=48247004)

**背景**: Intel 80386 于 1985 年发布，是 x86 架构中第一款 32 位处理器，引入了虚拟内存支持和保护模式。微代码是 CPU 内部的固件层，负责将机器指令翻译为处理器执行的低级序列——本质上是 CPU 的内部控制程序。微编程是 1980 年代至 90 年代处理器的常见设计技术，80386 是这种方法的一个历史性重要实例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Microcode">Microcode - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/I386">i386 - Wikipedia</a></li>
<li><a href="https://www.heise.de/en/news/40-Years-of-80386-Intel-s-Most-Important-Product-10778053.html">40 Years of 80386: Intel's Most Important Product - heise online</a></li>

</ul>
</details>

**社区讨论**: Hacker News 讨论（216 分，42 条评论）显示出对逆向工程工作的强烈赞赏，一位评论者注意到该博客已有 33 年的历史。有人提出关于如何从高分辨率芯片图像重建微代码的问题——输出是 Verilog 还是涉及晶体管级电路建模。一位评论者分享了微编程教科书的推荐，相关的 z386 开源项目帖子也引发了更多关注。

**标签**: `#reverse-engineering`, `#80386`, `#microcode`, `#vintage-hardware`, `#processor-architecture`

---

<a id="item-4"></a>
## [Anthropic Project Glasswing：AI 发现逾万高危漏洞](https://www.anthropic.com/research/glasswing-initial-update) ⭐️ 7.0/10

Anthropic 的 Project Glasswing 利用 Claude Mythos Preview 模型，在一个月内与约 50 个合作伙伴共同从关键软件和开源项目中发现了逾万高危漏洞。在经过审查的 1752 个漏洞中，90.6% 被确认为真阳性，Cloudflare 等合作伙伴报告漏洞发现速率提高了十倍以上。 这表明 AI 驱动的漏洞发现已达到生产级效率，从根本上改变了安全研究的格局。虽然漏洞检测不再是瓶颈，但验证、披露和修补等关键的人工依赖流程无法跟上步伐，迫切需要重新构建安全工作流程。 Project Glasswing 扫描了逾千个开源项目，发现了 6202 个高危漏洞。Claude Security 工具套件已发布以支持企业修复，Anthropic 还与开源安全基金会 (OpenSSF) 合作，帮助管理涌向开源维护者的漏洞报告。

telegram · zaihuapd · 05月23日 03:16

**背景**: Project Glasswing 汇集了 Anthropic 与 Apple、Google 以及其他 45 个组织，共同将 AI 应用于网络安全挑战。Claude Mythos Preview 是一款受控研究预览模型，专为聚焦网络安全、自主编码和长时间运行代理的雄心勃勃的项目而设计。开源安全基金会 (OpenSSF) 是 Linux 基金会旗下的跨行业倡议，致力于改善开源软件生态系统的安全。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/glasswing-initial-update">Project Glasswing: An initial update \ Anthropic</a></li>
<li><a href="https://www.wired.com/story/anthropic-mythos-preview-project-glasswing/">Anthropic Teams Up With Its Rivals to Keep AI From Hacking ...</a></li>
<li><a href="https://www-cdn.anthropic.com/8b8380204f74670be75e81c820ca8dda846ab289.pdf">Claude Mythos Preview System Card - www-cdn.anthropic.com</a></li>

</ul>
</details>

**社区讨论**: 安全研究人员和开发人员对这一进展的影响看法不一。许多人庆祝十倍的效率提升，但也有人担心验证和修补环节的人力瓶颈可能导致未修复漏洞的危险积累。部分开源维护者已明确请求放缓报告速度，凸显了本已资源紧张的项目面临的压力。

**标签**: `#AI Security`, `#Vulnerability Research`, `#LLM Applications`, `#Anthropic Claude`, `#Software Security`

---

<a id="item-5"></a>
## [富途被罚 185 亿元 老虎证券被罚没 41.1 亿元 无牌在华开展证券业务](https://t.me/zaihuapd/41539) ⭐️ 7.0/10

富途控股公告称，已收到中国证监会及深圳证监局的调查通知和行政罚款预通知函，因在内地无牌照开展证券、公开基金销售和期货业务，拟被罚没及罚款合计约 185 亿元人民币。老虎证券也披露，若干子公司因涉嫌无牌开展跨境证券业务，罚没金额合计约 41.1 亿元人民币。 此次处罚是中国监管机构对金融科技公司有史以来最严厉的执法行动之一，标志着跨境金融服务监管的重大收紧。这些罚款将重塑境外券商服务中国投资者的方式，并可能迫使整个行业进行重大运营调整。 除公司罚款外，富途创始人兼首席执行官李华还将面临 125 万元的个人罚款。公告发布后，两家公司股价立即暴跌：5 月 22 日美股开盘时，老虎证券下跌约 31%，富途下跌约 35%。两家公司均表示，罚款仍需经过后续程序并等待最终决定。

telegram · zaihuapd · 05月23日 10:58

**背景**: 中国金融监管框架要求任何在境内开展证券、基金销售或期货业务须获得证监会及相关部门的 proper licensing。涉及内地投资者的跨境证券业务近年来受到越来越多的监管关注，监管机构认为此类未经授权的经营活动对投资者和金融市场稳定构成风险。5 月 22 日，证监会等八部门联合印发了《综合整治非法跨境证券期货基金经营活动实施方案》。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.sina.com.cn/jjxw/2026-05-22/doc-inhyufhq6184315.shtml">八部门重拳整治！非法跨境证券业务全面叫停，老虎等境外券商拟被罚，...</a></li>
<li><a href="https://www.21jingji.com/article/20260523/herald/e7eb58bb6994d891f986fd9d06c85b1d.html">中国 证 监会拟对 富 途 罚款18.5亿， 老 虎 证 券 罚没4.112亿 - 21经济网</a></li>
<li><a href="https://www.guancha.cn/GuanJinRong/2026_05_22_818074.shtml">证 监会拟罚款金额公布： 富 途 被罚18.5亿， 老 虎 被罚4.112亿</a></li>

</ul>
</details>

**标签**: `#fintech regulation`, `#securities compliance`, `#cross-border finance`, `#Chinese financial markets`, `#regulatory enforcement`

---

<a id="item-6"></a>
## [正确使用 <dl> 元素引发 HTML 无障碍性讨论](https://benmyers.dev/blog/on-the-dl/) ⭐️ 6.0/10

2021 年，Ben Myers 的一篇博文探讨了正确使用 HTML <dl>（定义列表）元素的方法，引发了热烈的 Hacker News 讨论，其中包括关于 aria-label 无障碍模式错误的技术纠正，以及关于语义化 HTML 局限性的哲学辩论。 这场讨论凸显了语义化 HTML 标准与实际 Web 开发需求之间的持续张力，其无障碍性影响将决定开发者如何在网络上构建键值对内容的结构。 <dl> 元素具有 'group' 和 'list' 的隐式 ARIA 角色，这意味着根据 W3C HTML-ARIA 一致性规则，不能在其上应用 aria-label。DL-DT-DD 元素组合早于 Web 出现，源于 IBM 1985 年的 GML（通用标记语言）文档，与 GL、OL、UL 和 SL 列表类型并列。

hackernews · ravenical · 05月23日 13:03 · [社区讨论](https://news.ycombinator.com/item?id=48247325)

**背景**: <dl>（描述列表）元素是一种用于创建术语-定义配对列表的 HTML 结构，使用 <dt> 表示术语，<dd> 表示描述。在 HTML5 之前，这被称为"定义列表"，专门用于词汇表。语义化 HTML 使用能够清晰描述其含义的元素，以供浏览器和开发者理解，从而改善屏幕阅读器的可访问性和 SEO。据报道，万维网的第一个网站（位于 CERN）大量使用 <dl> 元素来构建内容结构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.w3resource.com/html/definition-lists/HTML-definition-lists-dl-dt-dd-tags-elements.php">HTML definition list - dl, dt, dd tag and elements - HTML tutorials - w3resource</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/dl">HTML description list element - MDN Web Docs</a></li>
<li><a href="https://www.w3schools.com/html/html5_semantic_elements.asp">HTML Semantic Elements</a></li>

</ul>
</details>

**社区讨论**: 社区情绪在严格的语义化 HTML 倡导者和务实的开发者之间产生分歧。chrismorgan 关于 aria-label 的技术纠正被广泛认为是有价值的。TheodpHN 关于 1985 年 GML 起源的历史发现被称赞为了不起的背景资料。然而，kqp 认为语义化 HTML 设计不佳的逆向观点引发了争议，一些人认为标准的灵活性比安于不完美但可用的解决方案能带来更好的长期效果。

**标签**: `#html`, `#semantic-markup`, `#accessibility`, `#web-development`, `#html-history`

---

<a id="item-7"></a>
## [德州女子因 Facebook 发布水质污染信息被捕](https://reclaimthenet.org/texas-woman-arrested-for-facebook-post-about-town-water-quality) ⭐️ 6.0/10

A Texas woman was arrested and charged under a state law prohibiting the knowing circulation of false reports after she posted on Facebook about water contamination in her town and reported that residents had been hospitalized. The post was intended to gather information and report findings to state authorities. This case highlights the tension between citizens' free speech rights and government regulation, especially on matters affecting public health. It raises profound questions about whether individuals have the right to discuss environmental hazards without official verification. The statute requires proving that the person 'knowingly' circulated a false report. Supporters argue she was simply repeating what others told her. Additionally, hospitals would violate HIPAA privacy rules by disclosing hospitalization information to private individuals, making independent verification nearly impossible for citizens.

hackernews · abawany · 05月23日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=48249747)

**背景**: The First Amendment protects free speech in the United States, but states also have laws against defamation and spreading false information. On public health and environmental safety issues, citizens often rely on social media to share firsthand experiences and observations without official investigation authority. Similar legal disputes have previously sparked discussions about the boundaries between citizen journalism and malicious misinformation.

**社区讨论**: Commenters widely view the post as protected free speech rather than defamation. Some point out that hospitals disclosing hospitalization info to individuals would violate HIPAA, preventing her from independently verifying claims. Others draw parallels to Ibsen's play 'An Enemy of the People,' seeing it as a classic test of whistleblower rights. Some predict she'll receive a settlement paid by taxpayers, while infrastructure problems remain unaddressed.

**标签**: `#free-speech`, `#legal`, `#social-media`, `#government-overreach`, `#public-health`

---

<a id="item-8"></a>
## [微软财报意外披露 OpenAI 单季度约 115 亿美元亏损](https://t.me/zaihuapd/41537) ⭐️ 6.0/10

微软最新季度财报显示，其对 OpenAI 的权益法投资导致该季度净利润减少 3.1 亿美元。基于微软持有 OpenAI 约 27%股权计算，OpenAI 该季度净亏损约为 115 亿美元。按税前损失和实际持股比例 32.5%计算，亏损可能超过 120 亿美元。 这一披露揭示了 AI 行业巨大的烧钱速度，显示 OpenAI 的季度亏损是其 2024 年上半年 43 亿美元营收的近三倍。对于投资者和行业观察者而言，这凸显了开发先进 AI 系统所需的巨额资金需求，并对当前 AI 商业模式的可持续性提出了质疑。 微软已向 OpenAI 投资 116 亿美元，占其 130 亿美元承诺投资的绝大部分。权益法会计处理意味着微软直接将其在 OpenAI 亏损中所占的份额计入损益表，这提供了一个难得的视角来了解 OpenAI 的财务表现。尽管亏损严重，最近泄露的股权结构表显示，在 OpenAI 完成 1220 亿美元融资、估值达 8520 亿美元后，微软的股份可能已升值至约 2283 亿美元。

telegram · zaihuapd · 05月23日 07:40

**背景**: 权益法是一种会计处理方法，当投资者对被投资企业具有重大影响但不具备完全控制权时使用，通常适用于 20%至 50%的持股比例。在该方法下，投资者记录其在被投资企业损益中所占的份额，并相应调整投资的账面价值。微软与 OpenAI 的合作始于 2019 年，微软成为其主要云基础设施提供商和主要投资者。OpenAI 的结构包括一个非营利基金会和一个利润上限子公司，形成了独特的治理模式，旨在平衡商业开发与安全考量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://m.163.com/dy/article/KPMAHCIS0519U3I5.html">OpenAI股权结构表曝光：微软130亿美元投资升值至2283亿美元</a></li>
<li><a href="https://news.qq.com/rain/a/20260404A04FR200">网传OpenAI“股权结构表”：微软130亿美元投资已升至2283亿美元</a></li>
<li><a href="https://baike.baidu.com/item/权益法/9289851">权益法 - 百度百科 采用权益法核算的长期股权投资账务处理流程（附案例详解） 一文搞懂长期股权投资的核算方法：成本法、权益法和合并法 在阅读||#20998;... 长期股权投资 核算 方法解析 成本法与权益法区别及实务操作指南 - 会... 权益法核算的长期股权投资收益_东奥会计在线 长期股权投资权益法 (长期股权投资核算方法) - 会计百科</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Microsoft`, `#AI Industry`, `#Financial Results`, `#Investment`

---

<a id="item-9"></a>
## [美商海盗船采用长鑫存储芯片，DDR5 内存价格 2027 年有望下调](https://thenextweb.com/news/chinese-dram-cxmt-corsair-ddr5-memory-prices) ⭐️ 6.0/10

美商海盗船已开始在其 DDR5 内存模组中使用长鑫存储（CXMT）的芯片，6000 MT/s 的产品已在市场上销售。这一转变正值三星、SK 海力士和美光等全球存储巨头将产能转向 AI 用高带宽内存（HBM），导致消费级 DDR5 市场供应短缺。 采用长鑫芯片的 DDR5 模组以 6000 MT/s 传输速率提供与国际主流产品相当的规格。长鑫存储在 2026 年第一季度实现强劲业绩，并计划于 2026 年上市。业内专家预测，随着中国产能持续扩大，受 AI 需求挤压的内存价格可能在 2027 年下半年出现明显回落。

telegram · zaihuapd · 05月23日 11:17

**背景**: 长鑫存储是一家中国半导体公司，总部位于安徽合肥，专注于 DRAM 的设计、研发、制造和销售。全球 DRAM 市场由三大厂商主导：三星、SK 海力士和美光。HBM（高带宽内存）是一种专为 AI 应用、图形显卡和超级计算机设计的专用内存技术，与传统 DDR 内存相比具有更高的带宽和更低的延迟。随着这些巨头将生产转向 HBM 以争夺 AI 市场份额，消费级 DDR5 供应收紧，为中国厂商创造了机会。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Changxin_Memory_Technologies">ChangXin Memory Technologies - Wikipedia</a></li>
<li><a href="https://www.scmp.com/tech/tech-trends/article/3353464/chinese-memory-module-makers-ramp-production-cxmt-ddr5-breakthrough-hits-market">Chinese memory module makers ramp up production with new CXMT DRAM</a></li>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>

</ul>
</details>

**标签**: `#DDR5 Memory`, `#CXMT`, `#Corsair`, `#Semiconductor Supply Chain`, `#Memory Pricing`

---