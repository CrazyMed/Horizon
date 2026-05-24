---
layout: default
title: "Horizon Daily: 2026-05-24"
date: 2026-05-24
lang: en
---

> From 22 items, 9 important content pieces were selected

---

1. [Apple Open-Sources corecrypto with Quantum-Safe Formal Verification](#item-1) ⭐️ 8.0/10
2. [Microsoft Internally Promotes Anthropic's Claude Code Across Key Teams](#item-2) ⭐️ 8.0/10
3. [80386 Microcode Successfully Disassembled via Reverse Engineering](#item-3) ⭐️ 7.0/10
4. [Anthropic Project Glasswing Uncovers 10,000+ Critical Vulnerabilities](#item-4) ⭐️ 7.0/10
5. [Futu Fined 18.5B Yuan, Tiger Brokers 411M Yuan for Unlicensed China Operations](#item-5) ⭐️ 7.0/10
6. [Proper <dl> Element Usage Sparks HTML Accessibility Debate](#item-6) ⭐️ 6.0/10
7. [Texas Woman Arrested for Facebook Post on Water Contamination](#item-7) ⭐️ 6.0/10
8. [Microsoft Earnings Reveal OpenAI's ~$11.5B Quarterly Loss](#item-8) ⭐️ 6.0/10
9. [Corsair Adopts CXMT Chips for DDR5, Consumer Prices May Drop by 2027](#item-9) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Apple Open-Sources corecrypto with Quantum-Safe Formal Verification](https://security.apple.com/blog/formal-verification-corecrypto/) ⭐️ 8.0/10

Apple released the corecrypto library source code on May 22, making public its ML-KEM and ML-DSA quantum-safe algorithm implementations with end-to-end formal verification proofs. The verification mathematically proves that both the C code and hand-optimized ARM64 assembly conform strictly to NIST standards. This release brings cryptographic rigor to over 2.5 billion active devices, protecting iMessage, VPN, and other services against future quantum computer threats. By publishing verification tools and Isabelle theory libraries for independent expert review, Apple sets a new industry standard for transparency and trust in security-critical software. ML-KEM (formerly CRYSTALS-Kyber) is a key encapsulation mechanism, while ML-DSA (formerly CRYSTALS-Dilithium) is a digital signature algorithm—both standardized by NIST in August 2024. Apple's formal verification uses Isabelle/HOL proof assistant to prove mathematical correctness of the implementations, bridging the gap between abstract specifications and actual deployed code.

telegram · zaihuapd · May 23, 04:49

**Background**: Post-quantum cryptography addresses the threat that sufficiently powerful quantum computers pose to current encryption. Current RSA and elliptic curve cryptography could be broken by Shor's algorithm on a quantum computer, making lattice-based algorithms like ML-KEM and ML-DSA essential for long-term security. Formal verification uses mathematical proofs to verify that code implements specifications correctly, eliminating entire classes of bugs that testing might miss. Isabelle is a widely-used interactive theorem prover for formal mathematics and verification.

**Tags**: `#quantum-resistant cryptography`, `#formal verification`, `#open-source security`, `#Apple`, `#NIST standards`, `#post-quantum encryption`

---

<a id="item-2"></a>
## [Microsoft Internally Promotes Anthropic's Claude Code Across Key Teams](https://t.me/zaihuapd/41535) ⭐️ 8.0/10

Microsoft is broadly deploying Anthropic's Claude Code across its critical engineering teams, including CoreAI, Windows, and Microsoft 365 divisions, with non-technical employees encouraged to use it for prototyping. Software engineers are now required to install both Claude Code and GitHub Copilot while providing comparative feedback between the two AI coding tools. This development is highly significant as Microsoft, which owns GitHub Copilot, is internally promoting a direct competitor's product at scale. The mandatory comparative feedback requirement suggests Microsoft acknowledges Claude Code's competitive advantages and is using it as an internal benchmark to evaluate their own offering against a leading rival in the AI coding space. The Experience & Devices team responsible for Windows, Microsoft 365, and Outlook products have been instructed to install Claude Code. The mandate extends beyond engineers to non-technical staff, indicating Microsoft's push for AI-assisted prototyping across the organization. This internal adoption comes even as Microsoft continues selling GitHub Copilot to external customers.

telegram · zaihuapd · May 23, 06:05

**Background**: Claude Code is an agentic coding tool developed by Anthropic that reads codebases, edits files, runs commands, and integrates with development tools. Anthropic, founded in 2021 by former OpenAI researchers including Dario and Daniela Amodei, has raised over $7.3 billion in cumulative funding and was valued at approximately $61.5 billion as of 2026. GitHub Copilot is Microsoft's AI-powered code completion tool, and Microsoft's internal adoption of Claude Code represents a notable acknowledgment of competitive pressure in the enterprise AI coding market.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://code.claude.com/docs/en/overview">Overview - Claude Code Docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI coding tools`, `#Claude Code`, `#Microsoft`, `#Anthropic`, `#GitHub Copilot`, `#Enterprise AI adoption`

---

<a id="item-3"></a>
## [80386 Microcode Successfully Disassembled via Reverse Engineering](https://www.reenigne.org/blog/80386-microcode-disassembled/) ⭐️ 7.0/10

A technical blog post documents the complete reverse engineering and disassembly of Intel 80386 processor microcode. The author has achieved the extraction and analysis of the internal microprogramming that controlled how this iconic 32-bit processor executed machine instructions. This work provides unprecedented insight into the microarchitectural implementation of the 80386, preserving irreplaceable knowledge about vintage processor internals. The findings support ongoing open-source hardware projects like z386 and benefit researchers studying x86 architecture evolution. The blog details extraction techniques including the analysis of high-resolution die images to reconstruct microcode from silicon. The Hacker News discussion raises questions about whether the process outputs Verilog or requires modeling individual transistors, with the related z386 project aiming to implement an 80386 using the original microcode.

hackernews · nand2mario · May 23, 12:11 · [Discussion](https://news.ycombinator.com/item?id=48247004)

**Background**: The Intel 80386, released in 1985, was the first 32-bit processor in the x86 architecture and introduced virtual memory support and protected mode. Microcode is a firmware layer within CPUs that translates machine instructions into lower-level sequences the processor executes—essentially the internal control program of a CPU. Microprogramming was a common design technique in 1980s-90s processors, and the 80386 represents a historically significant example of this approach.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Microcode">Microcode - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/I386">i386 - Wikipedia</a></li>
<li><a href="https://www.heise.de/en/news/40-Years-of-80386-Intel-s-Most-Important-Product-10778053.html">40 Years of 80386: Intel's Most Important Product - heise online</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion (216 points, 42 comments) shows strong appreciation for the reverse engineering work, with one commenter noting the blog's 33-year history. Questions arose about how microcode can be reconstructed from high-resolution die images—whether the output is Verilog or involves transistor-level circuit modeling. A commenter shared a microprogramming textbook recommendation, and the related z386 open-source project thread generated additional interest.

**Tags**: `#reverse-engineering`, `#80386`, `#microcode`, `#vintage-hardware`, `#processor-architecture`

---

<a id="item-4"></a>
## [Anthropic Project Glasswing Uncovers 10,000+ Critical Vulnerabilities](https://www.anthropic.com/research/glasswing-initial-update) ⭐️ 7.0/10

Anthropic's Project Glasswing used Claude Mythos Preview to discover over 10,000 high-severity vulnerabilities across critical software and open source projects in one month, working with approximately 50 partners. Among 1,752 reviewed vulnerabilities, 90.6% were confirmed as true positives, with partners like Cloudflare reporting a 10x improvement in vulnerability discovery rates. This demonstrates that AI-powered vulnerability discovery has reached production-ready effectiveness, fundamentally changing the economics of security research. While vulnerability detection is no longer the bottleneck, the critical human-dependent processes of validation, disclosure, and patching cannot keep pace, creating an urgent need to restructure security workflows. Project Glasswing scanned over a thousand open source projects and identified 6,202 high-severity vulnerabilities. The Claude Security tool suite has been released to support enterprise remediation, and Anthropic has partnered with the Open Source Security Foundation (OpenSSF) to help manage the increased vulnerability reports flowing to open source maintainers.

telegram · zaihuapd · May 23, 03:16

**Background**: Project Glasswing brings together Anthropic with Apple, Google, and over 45 other organizations to apply AI to cybersecurity challenges. Claude Mythos Preview is a gated research preview model specifically designed for ambitious projects focusing on cybersecurity, autonomous coding, and long-running agents. The Open Source Security Foundation (OpenSSF) is a cross-industry initiative under the Linux Foundation that works to improve the security of open-source software ecosystems.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/glasswing-initial-update">Project Glasswing: An initial update \ Anthropic</a></li>
<li><a href="https://www.wired.com/story/anthropic-mythos-preview-project-glasswing/">Anthropic Teams Up With Its Rivals to Keep AI From Hacking ...</a></li>
<li><a href="https://www-cdn.anthropic.com/8b8380204f74670be75e81c820ca8dda846ab289.pdf">Claude Mythos Preview System Card - www-cdn.anthropic.com</a></li>

</ul>
</details>

**Discussion**: Security researchers and developers are divided on the implications. While many celebrate the 10x efficiency gain, others express concern that the human bottleneck in validation and patching could lead to dangerous accumulations of unfixed vulnerabilities. Some open source maintainers have explicitly requested that the reporting pace be slowed down, highlighting the operational strain on already resource-constrained projects.

**Tags**: `#AI Security`, `#Vulnerability Research`, `#LLM Applications`, `#Anthropic Claude`, `#Software Security`

---

<a id="item-5"></a>
## [Futu Fined 18.5B Yuan, Tiger Brokers 411M Yuan for Unlicensed China Operations](https://t.me/zaihuapd/41539) ⭐️ 7.0/10

Futu Holdings announced it received investigation notices and pre-decision administrative penalty notices from the CSRC and Shenzhen Securities Regulatory Bureau, with proposed fines totaling approximately 18.5 billion yuan for operating securities, public fund sales, and futures businesses in mainland China without required licenses. Tiger Brokers also disclosed that several subsidiaries face fines of approximately 411 million yuan for similar unlicensed cross-border securities activities. These penalties represent one of the largest regulatory enforcement actions ever taken by Chinese authorities against fintech companies, signaling a significant tightening of cross-border financial services oversight. The fines will reshape how foreign fintech platforms serve Chinese investors and could force major operational changes across the industry. In addition to corporate fines, Futu's founder and CEO Li Hua faces a personal fine of 1.25 million yuan. The announcement caused immediate stock price drops: Tiger Brokers fell approximately 31% and Futu fell approximately 35% on May 22 when US markets opened. Both companies stated the penalties remain subject to further procedures and final decisions.

telegram · zaihuapd · May 23, 10:58

**Background**: China's financial regulatory framework requires proper licensing from the CSRC and relevant authorities before any securities, fund sales, or futures business can be conducted domestically. Cross-border securities activities involving mainland Chinese investors have faced increasing scrutiny, with authorities arguing that such operations without proper authorization pose risks to investors and financial market stability. On May 22, the CSRC and seven other departments jointly issued a comprehensive rectification plan targeting illegal cross-border securities and futures activities.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.sina.com.cn/jjxw/2026-05-22/doc-inhyufhq6184315.shtml">八部门重拳整治！非法跨境证券业务全面叫停，老虎等境外券商拟被罚，...</a></li>
<li><a href="https://www.21jingji.com/article/20260523/herald/e7eb58bb6994d891f986fd9d06c85b1d.html">中国 证 监会拟对 富 途 罚款18.5亿， 老 虎 证 券 罚没4.112亿 - 21经济网</a></li>
<li><a href="https://www.guancha.cn/GuanJinRong/2026_05_22_818074.shtml">证 监会拟罚款金额公布： 富 途 被罚18.5亿， 老 虎 被罚4.112亿</a></li>

</ul>
</details>

**Tags**: `#fintech regulation`, `#securities compliance`, `#cross-border finance`, `#Chinese financial markets`, `#regulatory enforcement`

---

<a id="item-6"></a>
## [Proper <dl> Element Usage Sparks HTML Accessibility Debate](https://benmyers.dev/blog/on-the-dl/) ⭐️ 6.0/10

A 2021 blog post by Ben Myers exploring proper HTML <dl> (definition list) usage triggered significant Hacker News discussion, including a technical correction about incorrect aria-label accessibility patterns and a philosophical debate about semantic HTML limitations. This discussion highlights the ongoing tension between semantic HTML standards and practical web development needs, with accessibility implications affecting how developers structure key-value content on the web. The <dl> element has implicit ARIA roles of 'group' and 'list', meaning aria-label cannot be applied to it per W3C HTML-ARIA conformance rules. The DL-DT-DD element trio predates the web, originating from IBM's 1985 GML (Generalized Markup Language) documentation alongside GL, OL, UL, and SL list types.

hackernews · ravenical · May 23, 13:03 · [Discussion](https://news.ycombinator.com/item?id=48247325)

**Background**: The <dl> (description list) element is an HTML structure for creating lists of term-definition pairs, using <dt> for terms and <dd> for descriptions. Before HTML5, this was called a 'definition list' intended for glossaries. Semantic HTML uses elements that clearly describe their meaning to browsers and developers, improving accessibility for screen readers and SEO. The World Wide Web's first website at CERN reportedly made heavy use of <dl> elements for content structure.

<details><summary>References</summary>
<ul>
<li><a href="https://www.w3resource.com/html/definition-lists/HTML-definition-lists-dl-dt-dd-tags-elements.php">HTML definition list - dl, dt, dd tag and elements - HTML tutorials - w3resource</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/dl">HTML description list element - MDN Web Docs</a></li>
<li><a href="https://www.w3schools.com/html/html5_semantic_elements.asp">HTML Semantic Elements</a></li>

</ul>
</details>

**Discussion**: Community sentiment split between strict semantic HTML advocates and pragmatic developers. chrismorgan's technical correction about aria-label was widely acknowledged as valuable. TheodpHN's historical finding about 1985 GML origins was praised as fascinating context. However, kqp's contrarian view that semantic HTML is 'poorly designed' generated both agreement and disagreement, with some arguing that flexibility in standards leads to better long-term outcomes than settling for imperfect but functional solutions.

**Tags**: `#html`, `#semantic-markup`, `#accessibility`, `#web-development`, `#html-history`

---

<a id="item-7"></a>
## [Texas Woman Arrested for Facebook Post on Water Contamination](https://reclaimthenet.org/texas-woman-arrested-for-facebook-post-about-town-water-quality) ⭐️ 6.0/10

德州一名女子在Facebook上发帖讨论当地水质污染问题并提及居民住院情况后，根据该州禁止故意传播虚假报告的法律被逮捕和起诉。该帖子旨在收集信息并向州政府报告调查结果。 此案凸显了公民言论自由与政府监管之间的紧张关系，特别是在涉及公共健康问题时。它引发了关于个人是否有权在未经官方证实的情况下讨论环境危害的深刻质疑。 该法律要求证明当事人"故意"传播虚假报告。支持者认为她只是在转述他人告知的信息。此外，医院若向私人透露住院信息将违反HIPAA隐私法规，这意味着个人难以独立核实医疗相关说法。

hackernews · abawany · May 23, 18:02 · [Discussion](https://news.ycombinator.com/item?id=48249747)

**Background**: 美国宪法第一修正案保护言论自由，但各州也有反诽谤和禁止传播虚假信息的相关法律。在公共健康和环境安全问题上，公民常常依赖社交媒体分享第一手经验和观察，而无需具备官方调查权限。类似的法律争议以往曾引发关于公民新闻报道权利与恶意传播虚假信息之间界限的讨论。

**Discussion**: 评论者普遍认为该帖子属于受保护的言论范围，而非诽谤。有人指出医院向个人透露住院信息会违反HIPAA，因此她无法独立核实这些信息。一些人将其比作易卜生戏剧《人民公敌》，认为这是对吹哨人权利的经典考验。另有评论预测她可能获得和解赔偿，但最终由纳税人买单，而基础设施问题仍得不到解决。

**Tags**: `#free-speech`, `#legal`, `#social-media`, `#government-overreach`, `#public-health`

---

<a id="item-8"></a>
## [Microsoft Earnings Reveal OpenAI's ~$11.5B Quarterly Loss](https://t.me/zaihuapd/41537) ⭐️ 6.0/10

Microsoft's latest quarterly earnings report shows that its equity method investment in OpenAI reduced net income by $310 million for the quarter. Based on Microsoft's approximately 27% stake, OpenAI's estimated quarterly net loss is around $11.5 billion. When calculated using pre-tax losses and the actual shareholding ratio of 32.5%, the loss could exceed $12 billion. This revelation exposes the massive cash burn rate in the AI industry, showing that OpenAI's quarterly losses are nearly three times its H1 2024 revenue of $4.3 billion. For investors and industry observers, this underscores the enormous capital requirements of developing advanced AI systems and raises questions about the sustainability of current AI business models. Microsoft has invested $11.6 billion in OpenAI, representing the vast majority of its $13 billion commitment. The equity method of accounting means Microsoft records its proportional share of OpenAI's losses directly on its income statement, providing a rare window into OpenAI's financial performance. Despite the losses, a recent leaked cap table suggests Microsoft's stake may have appreciated to approximately $228.3 billion following OpenAI's $122 billion funding round at a $852 billion valuation.

telegram · zaihuapd · May 23, 07:40

**Background**: The equity method is an accounting treatment used when an investor has significant influence over a company but not full control, typically at ownership stakes of 20-50%. Under this method, the investor records its proportional share of the investee's profits or losses, adjusting the carrying value of the investment accordingly. Microsoft and OpenAI's partnership began in 2019, with Microsoft becoming the primary cloud infrastructure provider and a major investor. OpenAI's structure includes both a non-profit foundation and a capped-profit subsidiary, creating a unique governance model designed to balance commercial development with safety considerations.

<details><summary>References</summary>
<ul>
<li><a href="https://m.163.com/dy/article/KPMAHCIS0519U3I5.html">OpenAI股权结构表曝光：微软130亿美元投资升值至2283亿美元</a></li>
<li><a href="https://news.qq.com/rain/a/20260404A04FR200">网传OpenAI“股权结构表”：微软130亿美元投资已升至2283亿美元</a></li>
<li><a href="https://baike.baidu.com/item/权益法/9289851">权益法 - 百度百科 采用权益法核算的长期股权投资账务处理流程（附案例详解） 一文搞懂长期股权投资的核算方法：成本法、权益法和合并法 在阅读||#20998;... 长期股权投资 核算 方法解析 成本法与权益法区别及实务操作指南 - 会... 权益法核算的长期股权投资收益_东奥会计在线 长期股权投资权益法 (长期股权投资核算方法) - 会计百科</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#Microsoft`, `#AI Industry`, `#Financial Results`, `#Investment`

---

<a id="item-9"></a>
## [Corsair Adopts CXMT Chips for DDR5, Consumer Prices May Drop by 2027](https://thenextweb.com/news/chinese-dram-cxmt-corsair-ddr5-memory-prices) ⭐️ 6.0/10

Corsair has begun using ChangXin Memory Technologies (CXMT) chips in its DDR5 memory modules, with 6000 MT/s products already available on the market. This shift comes as global memory giants Samsung, SK Hynix, and Micron redirect their production capacity toward AI-focused High Bandwidth Memory (HBM), creating supply shortages in the consumer DDR5 market. 这一发展标志着全球内存供应链的重大转变，中国厂商如长鑫存储开始填补主要DRAM厂商优先满足AI应用需求所留下的空缺。如果长鑫存储成功扩大产能，消费者有望在2027年下半年看到因AI需求而持续高企的DDR5价格的回落。 The CXMT-powered DDR5 modules offer specifications comparable to international mainstream products at 6000 MT/s transfer rates. CXMT achieved strong Q1 2026 performance and plans to go public in 2026, while industry experts predict that as Chinese production capacity continues to expand, memory prices squeezed by AI demand may see a noticeable decline in late 2027.

telegram · zaihuapd · May 23, 11:17

**Background**: ChangXin Memory Technologies (CXMT) is a Chinese semiconductor company headquartered in Hefei, Anhui, specializing in DRAM design, R&D, manufacturing, and sales. The global DRAM market is dominated by three major players: Samsung, SK Hynix, and Micron. HBM (High Bandwidth Memory) is a specialized memory technology designed for AI applications, graphics cards, and supercomputers, offering significantly higher bandwidth and lower latency compared to conventional DDR memory. As these giants pivot production toward HBM to capture AI market share, consumer-grade DDR5 supply has tightened, opening opportunities for Chinese manufacturers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Changxin_Memory_Technologies">ChangXin Memory Technologies - Wikipedia</a></li>
<li><a href="https://www.scmp.com/tech/tech-trends/article/3353464/chinese-memory-module-makers-ramp-production-cxmt-ddr5-breakthrough-hits-market">Chinese memory module makers ramp up production with new CXMT DRAM</a></li>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#DDR5 Memory`, `#CXMT`, `#Corsair`, `#Semiconductor Supply Chain`, `#Memory Pricing`

---