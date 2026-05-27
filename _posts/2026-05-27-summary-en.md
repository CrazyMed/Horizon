---
layout: default
title: "Horizon Daily: 2026-05-27"
date: 2026-05-27
lang: en
---

> From 25 items, 12 important content pieces were selected

---

1. [Wikimedia Foundation Lays Off Original MediaWiki Developer, Community Tech Team](#item-1) ⭐️ 7.0/10
2. [Netherlands Blocks US Takeover of Critical Tech Supplier](#item-2) ⭐️ 7.0/10
3. [AI Security Reports Overwhelm curl's Open Source Maintainers](#item-3) ⭐️ 7.0/10
4. [Microsoft Copilot Cowork File Exfiltration Vulnerability Discovered](#item-4) ⭐️ 7.0/10
5. [Jensen Huang Slams CEOs Using AI as Layoff Excuse](#item-5) ⭐️ 7.0/10
6. [China Reviewing Meta's Manus Acquisition, Founders Barred from Exit](#item-6) ⭐️ 7.0/10
7. [Garden Grove Methyl Methacrylate Tank Incident Technical Analysis](#item-7) ⭐️ 6.0/10
8. [Dropbox CEO Drew Houston Announces Departure](#item-8) ⭐️ 6.0/10
9. [Outsourcing Plus Local AI Poised to Beat Frontier Labs Economically](#item-9) ⭐️ 6.0/10
10. [EU Probes Google for Search and Play Store DMA Violations](#item-10) ⭐️ 6.0/10
11. [Meituan Releases Open-Source Run Errand Skill for AI Assistants](#item-11) ⭐️ 6.0/10
12. [Alipay Launches Token Pay and AI Wallet for AI Agents](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Wikimedia Foundation Lays Off Original MediaWiki Developer, Community Tech Team](https://medium.com/@jakeorlowitz/wikipedia-is-doing-the-capitalist-thing-56a393232943) ⭐️ 7.0/10

The Wikimedia Foundation has laid off Brooke, one of the original developers of MediaWiki—the open-source software that powers Wikipedia—along with the entire community tech team that developed tools by volunteer demand. Some English Wikipedia editors have responded by going on strike in protest. The layoffs affect core infrastructure developers while the foundation claims over 17 months of operating reserves, raising questions about nonprofit governance priorities. This decision impacts thousands of wikis beyond Wikipedia that depend on MediaWiki, and sets a concerning precedent for labor practices in the open-source nonprofit sector. Brooke was previously considered a potential BDFL (Benevolent Dictator For Life) for MediaWiki, making her departure particularly significant to longtime contributors. The community tech team operated by popular demand from volunteers, and their elimination removes a key bridge between the foundation and its volunteer developer community.

hackernews · cdrnsf · May 26, 20:33 · [Discussion](https://news.ycombinator.com/item?id=48285592)

**Background**: MediaWiki is an open-source PHP-based wiki software initially released in 2002 to power Wikipedia, and now serves thousands of other wikis worldwide. The Wikimedia Foundation is the nonprofit organization that operates Wikipedia and related projects, funded primarily through public donations. The community tech team specialized in building tools that helped Wikipedia's volunteer editors work more efficiently on the platform.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/MediaWiki">MediaWiki - Wikipedia</a></li>
<li><a href="https://wikimediafoundation.org/what-we-do/wikimedia-projects/mediawiki/">MediaWiki – Wikimedia Foundation</a></li>

</ul>
</details>

**Discussion**: Community comments reveal deeply divided opinions: some criticize the foundation for sitting on reserves while cutting critical teams, with one former editor expressing hope that the organization 'collapses' due to perceived mismanagement; others defend the reserves as necessary for long-term stability, noting that 17 months could vanish quickly during an economic downturn. Active Wikipedia editors are organizing strikes in solidarity with the laid-off workers.

**Tags**: `#open-source`, `#labor`, `#wikipedia`, `#nonprofit-tech`, `#mediawiki`

---

<a id="item-2"></a>
## [Netherlands Blocks US Takeover of Critical Tech Supplier](https://www.politico.eu/article/netherlands-blocks-us-takeover-vital-digital-supplier/) ⭐️ 7.0/10

The Dutch government has blocked Kyndryl's acquisition of Dutch IT company Solvinity, which hosts the critical DigiD e-identity infrastructure used by approximately 20 million Dutch citizens with over 550 million annual logins. This decision represents a significant assertion of digital sovereignty, protecting citizen data from potential US jurisdiction. It signals growing European resistance to foreign control of critical national infrastructure, particularly in sensitive domains like government digital identity systems. Solvinity, which provides "Secure Managed Cloud" services primarily for Dutch-based organizations, was being acquired by Kyndryl, a US company spun off from IBM's infrastructure services in 2021. The Dutch parliament had previously voted almost unanimously (with only one party dissenting) to end the Solvinity contract, but the government had extended it instead.

hackernews · vrganj · May 26, 11:46 · [Discussion](https://news.ycombinator.com/item?id=48278406)

**Background**: DigiD is the Dutch government's digital identity platform that allows citizens to authenticate themselves when accessing public services, including tax filings and healthcare. The system handled over 550 million logins in 2024, making it one of the most critical pieces of digital infrastructure in the Netherlands. Kyndryl, which operates in 63 countries, represents the type of large multinational tech company that governments increasingly view as potential national security risks when hosting sensitive citizen data.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DigiD">DigiD - Wikipedia</a></li>
<li><a href="https://nltimes.nl/2025/11/12/dutch-governments-caught-guard-american-tech-firm-buying-dutch-cloud-company">Dutch governments caught off guard by American tech firm buying</a></li>

</ul>
</details>

**Discussion**: Community members express relief that the government followed through on blocking the takeover after weeks of silence. Critics skewer Kyndryl's statement calling the decision "politicization," arguing politicians have a duty to protect citizen interests. Technical commentators debate whether the solution should be "privacy by architecture" versus "privacy by policy," with some advocating for cryptographic sovereignty systems where vendors mathematically cannot access user data. Others question whether an open-source self-hosted identity solution could handle 20 million users with 30,000 requests per hour.

**Tags**: `#digital-sovereignty`, `#national-security`, `#data-privacy`, `#geopolitics`, `#infrastructure`

---

<a id="item-3"></a>
## [AI Security Reports Overwhelm curl's Open Source Maintainers](https://simonwillison.net/2026/May/26/the-pressure/#atom-everything) ⭐️ 7.0/10

curl项目创建者丹尼尔·斯坦伯格报告称，由人工智能辅助生成的安全漏洞报告数量已达到2024年的4-5倍，平均每天超过一份。这些报告质量极高、内容详尽，给项目的小型安全团队带来了前所未有的压力。 这一现象揭示了开源项目面临的关键可持续性挑战：旨在提升安全性的AI工具正在压垮维护关键基础设施的小团队。由于curl被用于全球数十亿设备，这种不可持续的工作量正在威胁互联网基础构建块的安全性。 尽管报告数量激增，但漏洞严重程度普遍较低——近年来发现的漏洞均为LOW或MEDIUM级别，最近一次HIGH级别CVE还是2023年10月发布的。这表明AI工具擅长发现浅层问题，但并未发现灾难性漏洞。

rss · Simon Willison · May 26, 23:48

**Background**: curl是一个广泛使用的命令行工具，用于通过各种协议传输数据，几乎存在于所有互联网连接设备中。作为互联网基础设施的关键组件，其安全性至关重要。随着AI辅助漏洞发现工具（如Claude Mythos、Big Sleep）的兴起，安全研究变得更加高效，但这也导致了CVE披露量的激增，给开源维护者带来了额外的负担。

<details><summary>References</summary>
<ul>
<li><a href="https://www.vulncheck.com/blog/ai-assisted-vulnerability-discovery">The First CVE Wave: Signs That AI-Assisted Vulnerability ...</a></li>
<li><a href="https://securityboulevard.com/2026/05/ai-vulnerability-discovery-and-the-open-source-cve-surge/">AI Vulnerability Discovery and the Open Source CVE Surge</a></li>
<li><a href="https://arxiv.org/abs/2601.07019">[2601.07019] Zer0n: An AI-Assisted Vulnerability Discovery ... The First CVE Wave: Signs That AI-Assisted Vulnerability ... Claude Mythos AI Finds 10,000 High-Severity Flaws in Widely ... AI Vulnerability Discovery and the Open Source CVE Surge Adversaries Leverage AI for Vulnerability Exploitation ...</a></li>

</ul>
</details>

**Tags**: `#open-source-sustainability`, `#security`, `#curl`, `#ai-assisted-development`, `#developer-experience`

---

<a id="item-4"></a>
## [Microsoft Copilot Cowork File Exfiltration Vulnerability Discovered](https://simonwillison.net/2026/May/26/copilot-cowork-exfiltrates-files/#atom-everything) ⭐️ 7.0/10

Security researchers discovered that Microsoft Copilot Cowork allows data exfiltration through a chain attack combining unapproved email sending, external image rendering, and OneDrive pre-authenticated download links. The vulnerability enables a prompt injection attack where malicious instructions cause the agent to leak sensitive files via OneDrive links embedded in emails. This finding exposes a critical security flaw in a widely-deployed Microsoft 365 product, demonstrating the fundamental challenge of preventing unauthorized data access in agentic AI systems. Organizations using Microsoft Copilot Cowork are potentially vulnerable to data exfiltration attacks that exploit the trust placed in AI agents. The attack works by exploiting three combined weaknesses: the agent's ability to send emails without user approval, email clients rendering external images that trigger network requests, and OneDrive's pre-authenticated download links that grant file access without additional authentication. The vulnerability is documented as a "lethal trifecta" by security researchers at PromptArmor.

rss · Simon Willison · May 26, 15:36

**Background**: Prompt injection is a technique where attackers manipulate AI systems by inserting malicious instructions into inputs that the AI processes as legitimate commands. Microsoft Copilot Cowork is a Microsoft 365 product that enables AI agents to assist with workplace tasks. OneDrive pre-authenticated download links are designed for convenient file sharing but can be exploited if leaked to attackers. This vulnerability represents a class of security challenges specific to agentic AI systems that can take autonomous actions on behalf of users.

<details><summary>References</summary>
<ul>
<li><a href="https://www.wiz.io/academy/ai-security/prompt-injection-attack">What Is A Prompt Injection Attack? | Wiz</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion highlights the real-world impact of this vulnerability, with commenters noting the practical implications for enterprise security. Many emphasize the inherent tension between making AI agents useful (capable of sending emails, accessing files) and keeping them secure. Some express concern that this is just one example of many similar vulnerabilities likely present in other AI agent systems.

**Tags**: `#security`, `#prompt-injection`, `#microsoft-copilot`, `#ai-agents`, `#vulnerability`

---

<a id="item-5"></a>
## [Jensen Huang Slams CEOs Using AI as Layoff Excuse](https://ishare.ifeng.com/c/s/v0066Wzf04DphF34WYeiX3LGG6bhRsaqreKtU4T94DlOB2CCsV-_mW8zfzn0MPhPYjAXt) ⭐️ 7.0/10

NVIDIA CEO Jensen Huang, in an interview with Singapore media on Monday, criticized corporate leaders who blame AI for layoffs as "too perfunctory" and accused some of trying to appear smart. He questioned the logic of blaming AI for layoffs that occurred two years ago when generative AI tools only became effective about six months ago. This public criticism from the leader of the world's most influential AI chip company challenges the growing corporate narrative around AI-driven job cuts. It raises questions about corporate accountability and whether businesses are using AI as a convenient scapegoat for decisions driven by other factors, potentially undermining public trust in how companies communicate about automation. Huang specifically called out executives who attribute layoffs to AI as "just trying to seem smart" and expressed strong dislike for this behavior. The interview took place during his visit to Singapore, where he emphasized that the current wave of effective AI tools is relatively recent, making older layoffs attributed to AI logically implausible.

telegram · zaihuapd · May 26, 02:00

**Background**: Jensen Huang is the co-founder and CEO of NVIDIA, the company that dominates the GPU market and has become central to the AI revolution due to its H100 and other AI chips. NVIDIA's market capitalization has surged as demand for AI computing power has exploded. Generative AI tools like ChatGPT, Midjourney, and DALL-E have gained widespread attention since 2022-2023, with mainstream effectiveness only emerging in the past year. Many companies have announced layoffs while citing AI as a contributing factor, sparking widespread debate about technology's impact on employment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tuoluo.cn/article/detail-10110960.html">a16z 年终回顾： 生 成 式 AI 正在如何改变每个人的 生 活？_ 陀螺科技</a></li>
<li><a href="https://36kr.com/p/2300836228786953">最全对比： 生 成 式 AI ...</a></li>

</ul>
</details>

**Discussion**: The news has sparked significant discussion about corporate honesty regarding layoffs. Many readers support Huang's stance, arguing that CEOs often use AI as a convenient cover for cost-cutting decisions motivated by shareholder pressure or poor management. Some commenters note that while AI adoption is real, blaming it for job losses oversimplifies complex business decisions and deflects responsibility from leadership.

**Tags**: `#AI_labor_impact`, `#Jensen_Huang`, `#corporate_accountability`, `#layoffs`, `#tech_industry`

---

<a id="item-6"></a>
## [China Reviewing Meta's Manus Acquisition, Founders Barred from Exit](https://t.me/zaihuapd/41577) ⭐️ 7.0/10

China's regulators are reviewing whether Meta's acquisition of AI startup Manus violates investment regulations. During the investigation, Manus CEO Xiao Hong and Chief Scientist Ji Yichao have been restricted from leaving the country after meeting with officials from the National Development and Reform Commission (NDRC) in Beijing this month. This represents a significant escalation in regulatory scrutiny over cross-border AI acquisitions and highlights the growing tensions between US tech giants and China's regulatory apparatus. The restriction on individual founders—rather than just the company—signals that Beijing is willing to use personal travel restrictions as enforcement tools in investment regulation cases. Meta announced the acquisition in December 2025; the transaction amount remains undisclosed. Manus was founded by Chinese company Butterfly Effect and is headquartered in Singapore, developing general-purpose AI agents. Sources told Reuters the deal valued Manus at a significant amount, though the exact figure has not been confirmed.

telegram · zaihuapd · May 26, 09:56

**Background**: China established a national security review mechanism for foreign investment under its 2020 Foreign Investment Law. The system grants authorities the power to review acquisitions that may affect national security, with particular attention to sectors involving AI, data, and strategic technologies. Manus specializes in general-purpose AI agents—autonomous systems capable of executing complex tasks across various domains—making it a sensitive target under China's regulatory framework. The company's dual registration (Chinese-founded, Singapore-headquartered) places it at the intersection of both countries' jurisdictions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Manus_(AI_agent)">Manus (AI agent) - Wikipedia</a></li>
<li><a href="https://www.cnbc.com/2025/12/30/meta-acquires-singapore-ai-agent-firm-manus-china-butterfly-effect-monicai.html">Meta acquires intelligent agent firm Manus, capping year of ...</a></li>
<li><a href="https://www.cmtradelaw.com/2020/12/china-issues-rules-governing-national-security-reviews-of-foreign-investment/">China Issues Rules Governing National Security Reviews of</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Meta`, `#Manus`, `#China tech regulations`, `#M&A`, `#US-China tech tensions`

---

<a id="item-7"></a>
## [Garden Grove Methyl Methacrylate Tank Incident Technical Analysis](https://www.science.org/content/blog-post/methyl-methacrylate-tank) ⭐️ 6.0/10

Science.org published a technical postmortem analysis of the Garden Grove methyl methacrylate chemical tank incident, featuring community-shared analyses of similar incidents and safety engineering considerations including BLEVE prevention and seismic protection for industrial tanks. This incident highlights critical safety considerations for industrial chemical storage, particularly the risks of BLEVE and the importance of seismic protection for tanks in earthquake-prone areas like California. Methyl methacrylate is a highly flammable clear liquid used in resins and plastics production that releases harmful vapors when heated. Community commenters noted that similar incidents with Styrene and Butyl Acrylate provide valuable postmortem data, and that passive protection systems should be designed into tanks to prevent cascading failures after seismic events.

hackernews · nooks · May 26, 19:25 · [Discussion](https://news.ycombinator.com/item?id=48284712)

**Background**: BLEVE (Boiling Liquid Expanding Vapor Explosion) occurs when a tank containing a superheated liquid undergoes rapid depressurization, causing violent flashing into steam and explosive expansion. This phenomenon creates devastating blast waves and fireballs that have caused numerous firefighter fatalities in industrial incidents. The Kingman BLEVE incident is frequently cited as a case study in firefighter training for this exact scenario. Seismic protection for industrial tanks has gained increased attention following the 2011 Tōhoku earthquake and Fukushima disaster, where secondary failures compounded the initial emergency.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Boiling_liquid_expanding_vapor_explosion">Boiling liquid expanding vapor explosion - Wikipedia</a></li>
<li><a href="https://abc7.com/post/what-is-methyl-methacrylate-toxic-chemical-leak-garden-grove-tank-center-hazmat-crisis/19152928/">What is methyl methacrylate ? Toxic chemical ... - ABC7 Los Angeles</a></li>

</ul>
</details>

**Discussion**: Community members shared additional context including a simultaneous paper mill explosion in Washington state and links to similar postmortem analyses of Styrene and Butyl Acrylate polymerization incidents. One commenter noted that a fortunate crack allowed pressure to bleed off, potentially preventing a worse BLEVE outcome—a scenario demonstrated in the documented Kingman BLEVE. Another emphasized the need for passive protection systems to prevent cascading emergencies after seismic events, drawing parallels to lessons learned from Fukushima.

**Tags**: `#chemical-safety`, `#industrial-incidents`, `#BLEVE`, `#chemical-engineering`, `#postmortem-analysis`

---

<a id="item-8"></a>
## [Dropbox CEO Drew Houston Announces Departure](https://www.cnbc.com/2026/05/26/dropbox-ceo-drew-houston-ashraf-alkarmi.html) ⭐️ 6.0/10

Dropbox co-founder and CEO Drew Houston announced his departure from the cloud storage company, marking a significant leadership transition for the firm. Ashraf Alkarmi is expected to take over as the new CEO. This leadership change arrives at a challenging moment for Dropbox, which has struggled with stagnant stock valuation of around $6 billion despite generating approximately $2.5 billion in annual revenue. The transition raises questions about the company's strategic direction and ability to reinvigorate growth in an increasingly competitive market. Drew Houston built Dropbox into a profitable company known for its block-level syncing technology, which many users still consider unmatched in the market. Community comments suggest the company's stock has been stuck at its current valuation for years, with one commenter noting that competitors like Box.com face similar market challenges.

hackernews · aghuang · May 26, 13:18 · [Discussion](https://news.ycombinator.com/item?id=48279453)

**Background**: Dropbox was founded in 2007 by Drew Houston and Arash Ferdowsi, pioneering consumer cloud storage and becoming one of the first widely-adopted subscription-based file hosting services. The company went public in 2018 but has faced increasing competition from tech giants with integrated solutions: Apple iCloud, Google Drive, and Microsoft OneDrive. These competitors offer deep OS and productivity software integration that standalone services like Dropbox cannot match.

**Discussion**: Community sentiment is overwhelmingly positive regarding Drew Houston's leadership, with multiple commenters crediting him for creating a beloved product and fostering an excellent engineering culture. However, there is notable skepticism about the company's AI focus and concerns about the lack of significant new features since 2011. One commenter argued the valuation stagnation reflects broader market challenges rather than leadership issues, as major tech companies have captured the consumer cloud space with integrated solutions.

**Tags**: `#dropbox`, `#tech-leadership`, `#cloud-storage`, `#business-news`, `#ceo-transition`

---

<a id="item-9"></a>
## [Outsourcing Plus Local AI Poised to Beat Frontier Labs Economically](https://www.signalbloom.ai/posts/outsourcing-plus-localai-will-soon-become-more-economical-vs-frontier-labs/) ⭐️ 6.0/10

An opinion piece on SignalBloom.ai argues that combining software outsourcing with local or commodity AI systems will soon become more cost-effective than relying on frontier AI labs like OpenAI, Anthropic, and Meta. The analysis suggests that as AI capabilities commoditize, businesses can achieve similar results at a fraction of the cost through a hybrid outsourcing-plus-local-AI model. This thesis has significant implications for how companies approach AI adoption and software development economics. If validated, it could reshape the competitive dynamics between traditional outsourcing providers and frontier AI labs, potentially saving businesses substantial operational costs while maintaining output quality. Community commenters highlight that subscription token pricing is 10x-40x cheaper than API pricing, making the economics more favorable than they first appear. Multiple commenters draw parallels between effective LLM interactions and offshore developer management—both require highly detailed specifications and experienced operators to achieve quality results. One commenter reports a US company preparing to replace Eastern European development teams with fewer US programmers plus AI, claiming increased productivity.

hackernews · GodelNumbering · May 26, 12:08 · [Discussion](https://news.ycombinator.com/item?id=48278610)

**Background**: Frontier AI labs such as OpenAI, Anthropic, Meta, and xAI currently lead the industry in developing the most advanced AI models. These labs provide access to their models primarily through API pricing, which can be expensive for high-volume applications. The software outsourcing industry has long utilized offshore developers in regions like Eastern Europe and India to reduce costs. Local or commodity AI refers to running AI models on local infrastructure or using more affordable, general-purpose AI services rather than premium frontier models.

<details><summary>References</summary>
<ul>
<li><a href="https://epoch.ai/gradient-updates/frontier-labs-dont-use-most-ai-compute">How Much AI Compute Do Frontier Labs Use? | Epoch AI</a></li>

</ul>
</details>

**Discussion**: The discussion is substantive and largely agrees with the core thesis while adding nuanced insights. Commenters consistently draw parallels between effective LLM interactions and offshore developer experiences, noting both require extremely detailed specifications to produce quality outputs. There is debate about who benefits most—one commenter argues weak developers need stronger AI while strong developers can work with simpler AI, suggesting the productivity gains may concentrate at the top rather than democratize across all skill levels.

**Tags**: `#AI economics`, `#software outsourcing`, `#LLM cost analysis`, `#developer productivity`, `#AI adoption`

---

<a id="item-10"></a>
## [EU Probes Google for Search and Play Store DMA Violations](https://t.me/zaihuapd/41566) ⭐️ 6.0/10

The EU Commission released preliminary findings indicating that Alphabet/Google may have violated the Digital Markets Act (DMA) through self-preferencing in search results and restrictions on Play Store developers. Specifically, Google Search allegedly prioritizes its own shopping, flights, and hotel services over competitors, while the Play Store prevents developers from directing users to alternative purchase channels such as their own websites or third-party app stores. This represents a significant milestone in DMA enforcement, as it is among the first concrete actions targeting a designated gatekeeper's core business practices. If confirmed, these violations could result in substantial fines reaching up to 10% of global annual turnover, and may reshape how major platforms design their services to ensure fair competition in the EU market. Despite Google implementing several measures to comply with DMA requirements, the Commission concluded that these adjustments remain insufficient. The investigation covers two distinct areas: algorithmic prioritization of Google's own services in search results, and contractual restrictions preventing app developers from steering users to cheaper alternatives outside the Play Store ecosystem.

telegram · zaihuapd · May 26, 00:27

**Background**: The Digital Markets Act (DMA), which entered into force on November 1, 2022, is the EU's regulatory framework designed to ensure fair competition and contestability in digital markets. It imposes specific obligations on large platforms designated as "gatekeepers," requiring them to allow interoperability, prevent self-preferencing, and enable business users to operate freely on their platforms. Google, along with other major tech firms, was designated as a gatekeeper under the DMA, subjecting its core platform services to these stringent regulatory requirements.

<details><summary>References</summary>
<ul>
<li><a href="https://www.europarl.europa.eu/topics/en/article/20211209STO19124/eu-digital-markets-act-and-digital-services-act-explained">EU Digital Markets Act and Digital Services Act explained |</a></li>
<li><a href="https://www.shs-conferences.org/articles/shsconf/pdf/2024/10/shsconf_edss2024_03031.pdf">Antitrust Regulation of Self-Preferential Platform Operators ...</a></li>

</ul>
</details>

**Tags**: `#Digital Markets Act`, `#Google`, `#EU Regulation`, `#Big Tech Antitrust`, `#Platform Regulation`

---

<a id="item-11"></a>
## [Meituan Releases Open-Source Run Errand Skill for AI Assistants](http://client.sina.com.cn/news/2026-05-26/doc-inhzffss1481138.shtml) ⭐️ 6.0/10

Meituan released an open-source "Run Errand Skill" that packages its delivery ordering capabilities as a standard API for the AI assistant ecosystem. Users can voice their needs to any compatible AI assistant, and the system automatically handles scene recognition, address matching, price estimation, and order submission without opening any apps. This represents a practical bridge between AI assistants and real-world services, enabling voice-activated delivery ordering that could reshape how users interact with everyday services. Meituan's open-source approach and standard API packaging could inspire similar integrations across other service industries. The skill enables zero-development integration for compatible AI clients, including the open-source OpenClaw framework. After placing an order, users can query rider progress through the same conversational interface. The functionality covers all cities where Meituan's run errand service is available.

telegram · zaihuapd · May 26, 08:29

**Background**: In 2026, three main extension types dominate the AI agent ecosystem: skills, plugins, and MCP servers. An AI agent skill is a prompt-based instruction that modifies agent behavior without requiring code. OpenClaw is an open-source personal AI assistant that can call almost any tool through plugins, supporting platforms like WhatsApp, Telegram, and Discord. Meituan had previously validated conversational ordering within its own app before opening the core capabilities externally.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenClaw">OpenClaw - Wikipedia</a></li>
<li><a href="https://openclaw.ai/">OpenClaw — Personal AI Assistant</a></li>
<li><a href="https://nevo.systems/blogs/nevo-journal/ai-agent-skill-vs-plugin-vs-mcp">Skills vs Plugins vs MCPs: Understanding AI Agent Extension ...</a></li>

</ul>
</details>

**Tags**: `#AI Assistants`, `#API Integration`, `#Meituan`, `#Open Source`, `#AI Agents`, `#Consumer AI`

---

<a id="item-12"></a>
## [Alipay Launches Token Pay and AI Wallet for AI Agents](https://finance.sina.com.cn/jjxw/2026-05-26/doc-inhzffss1524895.shtml) ⭐️ 6.0/10

Alipay officially released Token Pay service and AI Wallet on May 26. Users can search 'AI Wallet' in Alipay to manage AI agent task payments and view post-payment bills, while Token Pay targets LLM companies for global user subscriptions and in-app token purchases. This represents a significant strategic move by Alipay to establish payment infrastructure for AI agents. As autonomous AI systems proliferate, the ability to manage programmatic financial transactions becomes critical infrastructure for the emerging AI economy. MiniMax and StepStar (阶跃星辰) have partnered with Alipay to implement this payment solution, with multiple AI-native products committed to adoption. The timing coincides with StepStar's reported IPO preparations in Hong Kong, seeking approximately $500 million in funding at a reported $10 billion valuation.

telegram · zaihuapd · May 26, 12:31

**Background**: AI agents are autonomous software systems capable of planning and executing tasks without human intervention. As these agents require financial resources to function (such as API calls, compute resources, or purchasing goods and services), traditional payment systems designed for human users need adaptation. MiniMax and StepStar are leading Chinese LLM companies, often categorized among China's 'AI Five Tigers' alongside Moonshot (Kimi), DeepSeek, and Zhipu AI.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.sina.cn/2026-05-23/detail-inhyvxrt7095654.d.html?vt=4">阶跃星辰百亿估值背后，是AI变现的解药还是新焦虑？|IPO|开源模型|Min...</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2040503903507173383">AI 五虎 2026 年中数据全景：月之暗面、阶跃星辰、MiniMax、深度求索...</a></li>

</ul>
</details>

**Tags**: `#AI Payments`, `#Fintech`, `#AI Agents`, `#支付宝`, `#Payment Infrastructure`

---