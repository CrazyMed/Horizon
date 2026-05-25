---
layout: default
title: "Horizon Daily: 2026-05-25"
date: 2026-05-25
lang: en
---

> From 26 items, 10 important content pieces were selected

---

1. [Constraint Decay: LLM Agents Struggle with Architectural Rules](#item-1) ⭐️ 8.0/10
2. [Memory Now Constitutes Nearly Two-Thirds of AI Chip Costs](#item-2) ⭐️ 7.0/10
3. [Microsoft Open-Sources Earliest Known DOS Source Code](#item-3) ⭐️ 7.0/10
4. [Greg Brockman Interview Sparks OpenAI Governance Debate](#item-4) ⭐️ 7.0/10
5. [Scammers Abuse Microsoft Internal Domain for Spam Campaigns](#item-5) ⭐️ 7.0/10
6. [16-Byte Demo Amazes Hacker News with Extreme Code Golf](#item-6) ⭐️ 7.0/10
7. [AMD Drops Linux Support from Vivado Free Tier, Sparking Backlash](#item-7) ⭐️ 7.0/10
8. [APKPure Telegram Found Trojanized with DataCollector Spy Framework](#item-8) ⭐️ 7.0/10
9. [Armin Ronacher Critiques AI-Generated Bug Reports](#item-9) ⭐️ 6.0/10
10. [Shenzhou 23 Crew Announced with First Hong Kong Payload Expert](#item-10) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Constraint Decay: LLM Agents Struggle with Architectural Rules](https://arxiv.org/abs/2605.06445) ⭐️ 8.0/10

Researchers published findings on arxiv (paper 2605.06445) revealing that LLM coding agents experience 'constraint decay'—their assertion pass rate drops approximately 30 percentage points when generating multi-file backend code under accumulated architectural, ORM, and framework constraints. This finding directly challenges the reliability of AI coding assistants for production-grade backend development, indicating that while these tools excel at rapid prototyping, they remain unsuitable for complex systems requiring strict adherence to architectural conventions. The performance degradation concentrates most heavily on convention-heavy frameworks, and the study's authors acknowledge a limitation: frontier models were not fully tested due to cost constraints. The loss of reliability occurs as constraints accumulate rather than appearing in isolated rule violations.

hackernews · wek · May 24, 12:55 · [Discussion](https://news.ycombinator.com/item?id=48256912)

**Background**: LLM agents are AI systems that use large language models to autonomously perform coding tasks, often generating multiple files and coordinating complex development workflows. 'Constraint decay' refers to the phenomenon where these agents successfully complete unconstrained coding tasks but progressively fail as explicit architectural rules, framework conventions, and database patterns are introduced. This is particularly relevant for backend development, which typically involves multiple interconnected components with strict structural requirements.

<details><summary>References</summary>
<ul>
<li><a href="https://www.alphaxiv.org/overview/2605.06445v1">Constraint Decay : The Fragility of LLM Agents in Backend... | alphaXiv</a></li>
<li><a href="https://agentpatterns.ai/verification/constraint-decay-backend-agents/">Constraint Decay in Backend Code Generation - AgentPatterns.ai</a></li>
<li><a href="https://news.ycombinator.com/item?id=48256912">Constraint Decay : The Fragility of LLM Agents in Back... | Hacker News</a></li>

</ul>
</details>

**Discussion**: The research sparked significant discussion, with commenters validating the findings against their own experiences. One practitioner noted they've observed similar "calcification" effects where architectural patterns become entrenched in codebases. Others highlighted that structured agent orchestrators can help but still require 5-10 review-fix cycles to ensure implementations match specifications. The consensus acknowledges the limitation is real for production use, though some argue LLMs still outperform humans for long-horizon programming tasks compared to other disciplines.

**Tags**: `#llm-agents`, `#code-generation`, `#constraint-decay`, `#ai-reliability`, `#software-engineering`

---

<a id="item-2"></a>
## [Memory Now Constitutes Nearly Two-Thirds of AI Chip Costs](https://epoch.ai/data-insights/ai-chip-component-cost-shares) ⭐️ 7.0/10

According to Epoch AI data, memory now accounts for nearly two-thirds (approximately 65%) of total AI chip component costs, representing a major shift in AI hardware economics and supply chain dynamics. This cost rebalancing makes memory the primary cost driver for AI accelerators, significantly impacting infrastructure planning and potentially creating a path to substantial hardware cost reductions if DRAM supply catches up with demand. High Bandwidth Memory (HBM), the 3D-stacked memory technology used in AI accelerators like NVIDIA GPUs, is the primary driver of this cost shift. Community analysts suggest that waiting for DRAM supply normalization could yield approximately 3x hardware cost reductions without any technical innovation, though memory capacity growth rates of 20-25% annually may lag behind AI demand growth.

hackernews · intelkishan · May 24, 16:31 · [Discussion](https://news.ycombinator.com/item?id=48258684)

**Background**: High Bandwidth Memory (HBM) is a 3D-stacked synchronous dynamic random-access memory technology developed by Samsung, AMD, and SK Hynix that uses Through-Silicon Vias (TSVs) to interconnect stacked memory dies. HBM provides significantly higher bandwidth and lower power consumption compared to traditional DRAM, making it essential for AI training and inference workloads. The HBM market, currently dominated by SK Hynix following Samsung's leadership loss, is projected to reach $58 billion by 2026, driven entirely by AI accelerator requirements.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://introl.com/blog/hbm-evolution-hbm3-hbm3e-hbm4-memory-ai-gpu-2025">HBM evolution: from HBM3 to HBM4 and the AI memory war</a></li>
<li><a href="https://www.linkedin.com/pulse/high-bandwidth-memory-hbm-ai-crossroads-customization-czfdc">High Bandwidth Memory ( HBM ) at the AI Crossroads: Customization...</a></li>

</ul>
</details>

**Discussion**: The community discussion reveals a mix of optimism and frustration. One commenter highlighted that waiting for DRAM supply normalization could enable ~3x hardware cost reductions and ~2x total cost reductions without any technical breakthroughs. However, others expressed frustration over consumer RAM prices (one user noted 96GB RAM jumping from $250 to $1200), with some refusing to upgrade until prices become reasonable. Concerns were raised about whether 20-25% annual memory capacity growth can keep pace with AI demands, with skepticism about whether manufacturers will risk oversupply.

**Tags**: `#AI chips`, `#hardware costs`, `#memory/DRAM`, `#AI infrastructure`, `#supply chain`

---

<a id="item-3"></a>
## [Microsoft Open-Sources Earliest Known DOS Source Code](https://arstechnica.com/gadgets/2026/04/microsoft-open-sources-the-earliest-dos-source-code-discovered-to-date/) ⭐️ 7.0/10

Microsoft has open-sourced the earliest known DOS source code discovered to date, which was recovered using OCR technology from decades-old paper printouts by a dedicated team of historians and preservationists led by Yufeng Gao and Rich Cini. The code, stored in a GitHub repository under the DOS Disassembly Group, represents a significant milestone in software archaeology and digital preservation. This release makes a critical piece of computing heritage accessible to developers, historians, and retro-computing enthusiasts, preserving the technical foundations of the PC era for future generations. It also highlights how Microsoft's entry into operating systems was largely accidental, stemming from IBM's failed negotiations with Digital Research for CP/M. The recovery process was particularly challenging because the source code predated digital storage, existing only as paper printouts from developer Tim Paterson. Modern OCR software struggled with the degraded quality of the decades-old documents, requiring manual transcription work by the preservation team. Microsoft also open-sourced the accompanying BASIC code, which commenters note was actually Microsoft's primary business focus, with DOS serving as the contract that launched their OS business.

hackernews · DamnInteresting · May 24, 01:21 · [Discussion](https://news.ycombinator.com/item?id=48253386)

**Background**: Software archaeology is the systematic recovery and analysis of legacy software systems, particularly those with incomplete or absent documentation, involving reverse engineering and various tools for extracting program structure. DOS (Disk Operating System) was the operating system Microsoft provided to IBM for the original PC in 1981, eventually becoming the foundation for the dominant PC operating system ecosystem. The Paris Call for Software Source Code as Heritage, adopted by UNESCO experts in 2018, recognized source code preservation as an important component of sustainable digital heritage.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Software_archaeology">Software archaeology</a></li>
<li><a href="https://www.unesco.org/en/articles/experts-call-greater-recognition-software-source-code-heritage-sustainable-development">Experts call for greater recognition of software source code ...</a></li>

</ul>
</details>

**Discussion**: The community response is overwhelmingly positive, with commenters praising Microsoft for the release while highlighting the historical significance of BASIC as Microsoft's true focus. One commenter notes jealousy at the simplicity of launching a successful company with just thousands of lines of assembly, while another explains the pivotal negotiation story where IBM turned to Microsoft after Digital Research refused to sign their NDA for CP/M. The OCR recovery process from paper printouts is repeatedly mentioned as a remarkable preservation achievement.

**Tags**: `#open-source`, `#software-history`, `#DOS`, `#Microsoft`, `#retro-computing`

---

<a id="item-4"></a>
## [Greg Brockman Interview Sparks OpenAI Governance Debate](https://fs.blog/knowledge-project-podcast/greg-brockman/) ⭐️ 7.0/10

Greg Brockman, President of OpenAI, appeared on the Knowledge Project podcast to discuss the company's history, governance structure, and the 2023 leadership crisis that briefly ousted CEO Sam Altman. The interview generated 166 points and 157 comments on Hacker News, with community members debating whether Brockman provided sufficient depth on unresolved questions about the Ilya Sutskever firing incident. As one of the original co-founders of OpenAI alongside Altman and Musk, Brockman's insider perspective is valuable for understanding the tensions between the company's nonprofit origins and its $100 billion commercial enterprise. The interview arrives amid ongoing scrutiny of OpenAI's governance model and recent proposals to reduce the nonprofit board's oversight role. Commenters noted that the interview largely covers well-known events rather than providing new revelations, with one user questioning why no one asked what 'happened in Ilya's mind' during the crisis. The discussion also referenced Musk's lawsuit against OpenAI, which included Brockman's personal diary containing entries like 'Financially what will take me to $1B?'

hackernews · prakashqwerty · May 24, 08:29 · [Discussion](https://news.ycombinator.com/item?id=48255593)

**Background**: OpenAI was founded in 2015 as a Delaware nonprofit with the mission to build safe AGI that benefits humanity. In 2019, it created a capped-profit subsidiary to attract capital, and by 2025 converted this subsidiary into a Public Benefit Corporation (PBC) 26% owned by the nonprofit. In November 2023, OpenAI's board unexpectedly fired CEO Sam Altman in what Reuters described as a 'board coup' led by chief scientist Ilya Sutskever over AI safety concerns. Sutskever later expressed deep regret for his participation in the decision, and Altman was reinstated within days.

<details><summary>References</summary>
<ul>
<li><a href="https://arstechnica.com/information-technology/2023/11/report-sutskever-led-board-coup-at-openai-that-ousted-altman-over-ai-safety-concerns/">Details emerge of surprise board coup that ousted CEO Sam Altman ...</a></li>
<li><a href="https://www.axios.com/2023/11/20/sam-altman-fired-openai-board-illya-sutsever-regrets">OpenAI chief scientist says he regrets board’s firing of Sam Altman</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI">OpenAI - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community reaction was mixed, with some commenters dismissing the interview as surface-level coverage of corporate drama akin to 'techie reality TV,' while others raised substantive concerns about whether OpenAI's nonprofit structure was merely a favorable legal designation rather than a meaningful commitment. The dominant critique focused on the interview's lack of depth on unresolved questions, particularly regarding Sutskever's motivations and the broader governance implications.

**Tags**: `#openai`, `#ai-safety`, `#interview`, `#tech-leadership`, `#governance`

---

<a id="item-5"></a>
## [Scammers Abuse Microsoft Internal Domain for Spam Campaigns](https://techcrunch.com/2026/05/21/scammers-are-abusing-an-internal-microsoft-account-to-send-spam/) ⭐️ 7.0/10

Security researchers discovered that scammers are exploiting an internal Microsoft domain to send phishing emails and spam links. The attack leverages Microsoft's own domain infrastructure, making the malicious emails appear legitimate since they originate from Microsoft's trusted infrastructure. This incident exposes critical vulnerabilities in enterprise domain management and email authentication systems. Organizations relying on domain-based email verification may find their security assumptions undermined when trusted providers themselves become sources of malicious traffic. The exploitation leverages Microsoft's sprawling domain portfolio and complex internal infrastructure. Community members noted that Microsoft owns numerous domains across different services, making it nearly impossible for users to verify legitimate senders without a comprehensive registry.

hackernews · spike021 · May 24, 00:51 · [Discussion](https://news.ycombinator.com/item?id=48253186)

**Background**: Enterprise email security relies on protocols like SPF (Sender Policy Framework), DKIM (DomainKeys Identified Mail), and DMARC (Domain-based Message Authentication, Reporting, and Conformance) to prevent email spoofing. These technologies verify that emails originate from authorized servers and help recipients identify fraudulent messages. However, when attackers abuse internal infrastructure or trusted domains, these authentication mechanisms may fail to block malicious messages since they technically originate from legitimate sources.

<details><summary>References</summary>
<ul>
<li><a href="https://cwe.mitre.org/data/definitions/290.html">CWE - CWE-290: Authentication Bypass by Spoofing (4.20)</a></li>
<li><a href="https://www.sentinelone.com/cybersecurity-101/cybersecurity/enterprise-email-security/">Enterprise Email Security: Importance and Best Practices</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion revealed widespread frustration with Microsoft's domain management practices. Commenters noted that Microsoft's use of numerous separate domains (like microsoftonline.com) makes verification nearly impossible for average users. One user reported Authenticator app anomalies showing sign-in notifications from unknown locations while the login history remained empty, raising concerns about authentication transparency. Others highlighted visual spoofing vulnerabilities where characters like 'm' and 'rn' appear nearly identical in certain fonts, suggesting domain-based verification alone is insufficient for security.

**Tags**: `#security`, `#phishing`, `#microsoft`, `#email-spoofing`, `#cybersecurity`

---

<a id="item-6"></a>
## [16-Byte Demo Amazes Hacker News with Extreme Code Golf](https://hellmood.111mb.de/wake_up_16b_writeup.html) ⭐️ 7.0/10

A Hacker News user shared a 16-byte generative demo, creating an audiovisual presentation through extreme code size optimization that impressed the community with 408 points and 31 comments. 这一成就突破了x86汇编优化的极限，展示了仅用16字节就能创作出有意义的生成艺术。它彰显了demo场景文化的持久魅力——程序员们在这里竞争谁能用最少的代码实现最大的效果。 The demo runs in only 16 bytes, likely utilizing undocumented x86 instructions or side effects of certain opcodes to generate its output. Commenters noted this surpasses their expectations of a 32-byte demo that 'was the limit of how small the binary can get and still look good.'

hackernews · MaximilianEmel · May 24, 00:30 · [Discussion](https://news.ycombinator.com/item?id=48253060)

**Background**: The demoscene is an international computer art subculture dating back to the 1980s, where programmers create self-contained audiovisual presentations to demonstrate technical skill. Code golf is a recreational programming competition where participants strive to write the shortest possible source code that solves a problem. The demo scene traditionally features competitions like 64k intros and 4k intros, making 16 bytes an extraordinary achievement that pushes size restrictions to their absolute minimum.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Demoscene">Demoscene</a></li>
<li><a href="https://en.wikipedia.org/wiki/Code_golf">Code golf</a></li>

</ul>
</details>

**Discussion**: The community response was overwhelmingly positive, with commenters expressing awe at the craftsmanship. One user declared 'Witch!' in admiration, while another shared that this sent them on a one-hour rabbit hole ending with building a Sierpinski triangle using recursive PowerPoint presentations. The consensus view called it 'a masterpiece to retire after' while noting it could inspire similar pursuits on other architectures.

**Tags**: `#demo-scene`, `#code-golf`, `#x86`, `#code-size-optimization`, `#assembly`

---

<a id="item-7"></a>
## [AMD Drops Linux Support from Vivado Free Tier, Sparking Backlash](https://adaptivesupport.amd.com/s/question/0D5Pd00001YQLdMKAX/why-is-vivado-20261-dropping-linux-support-for-free-tier-?language=en_US) ⭐️ 7.0/10

AMD/Xilinx announced that Vivado 2026.1 will remove Linux support from its free "WebPACK" tier, forcing Linux users to either pay for licensing or switch platforms. The change drew 174+ substantive comments and 295 engagement points, with community members citing frustration about alienating students, hobbyists, and enterprise developers. This decision could reshape the FPGA ecosystem by pushing developers toward competitors like Lattice, which offers free software tools for all basic chips. Removing Linux support undermines AMD's strategy to grow adoption among the open-source community, where Linux is the dominant platform for development. The Basic/WebPACK tier previously supported both Windows and Linux development; after this change, only Windows will be available for free. One commenter noted that AMD's own documentation recommends Linux for certain tools, making this policy inconsistency particularly frustrating. Users report that Lattice's free toolchain covers ECP5 and Certus chips without paid licensing.

hackernews · zdw · May 24, 04:14 · [Discussion](https://news.ycombinator.com/item?id=48254309)

**Background**: FPGAs (Field-Programmable Gate Arrays) are reprogrammable integrated circuits that allow engineers to design custom hardware without manufacturing custom chips. Vivado Design Suite is AMD/Xilinx's primary toolchain for programming their FPGA and SoC products. The free "WebPACK" tier has historically been crucial for students, hobbyists, and small teams to learn and prototype with Xilinx hardware before committing to commercial licensing.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Field-programmable_gate_array">Field - programmable gate array - Wikipedia</a></li>
<li><a href="https://www.amd.com/en/products/software/adaptive-socs-and-fpgas/vivado.html">AMD Vivado™ Design Suite</a></li>

</ul>
</details>

**Discussion**: Community members expressed strong frustration, with long-term enterprise users noting they have spent "several hundred thousand" on Xilinx hardware but are annoyed by licensing bureaucracy for new computers and CI systems. Multiple commenters recommended switching to Lattice, citing better documentation and no licensing hassles. An ex-Altera user warned that AMD appears to be repeating Intel's mistake of shutting down community engagement after acquisition, noting that Xilinx's strong hobbyist community was a key competitive advantage.

**Tags**: `#FPGA`, `#Vivado`, `#AMD/Xilinx`, `#Linux`, `#Developer Tools`

---

<a id="item-8"></a>
## [APKPure Telegram Found Trojanized with DataCollector Spy Framework](https://x.com/EricParker/status/2058411298195661221) ⭐️ 7.0/10

Security researchers discovered a malicious version of Telegram 12.6.5 distributed through the APKPure app store. The trojanized app contains a sophisticated spy framework called DataCollector embedded in a classes3.dex file with over 3,000 lines of code, capable of exfiltrating messages, contacts, media, location, and SIM data to C2 server 38.190.225.166. This represents a serious supply chain attack targeting users who rely on third-party app stores instead of official channels. The malware's advanced capabilities—including encrypted data exfiltration and comprehensive data harvesting—pose significant privacy and security risks to potentially millions of affected users who downloaded the app believing it was legitimate. The trojanized Telegram was re-signed and repackaged with the malicious DataCollector framework. Stolen data is encrypted using AES-GCM before being sent to the command-and-control server. The compromised component resides in classes3.dex, which is the standard Android Dalvik executable format containing compiled application code that runs on the Android Runtime.

telegram · zaihuapd · May 24, 11:38

**Background**: APKPure is a popular third-party Android app store that allows users to download APK files for apps not available on Google Play or to access older versions of applications. The .dex file format (Dalvik Executable) is used by Android to store compiled application code. Supply chain attacks involving repackaged legitimate applications are particularly dangerous because they exploit user trust in familiar apps and can bypass casual security checks by appearing functional while secretly harvesting data.

<details><summary>References</summary>
<ul>
<li><a href="https://alternativeto.net/software/apk-pure/">Best APKPure Alternatives : Top App Stores in 2025 | AlternativeTo</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apk_(file_format)">apk (file format ) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Block_cipher_mode_of_operation">Block cipher mode of operation - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The security community has expressed concern about the growing sophistication of supply chain attacks targeting third-party app stores. Eric Parker's disclosure was shared widely, with other researchers highlighting the use of AES-GCM encryption as evidence of a professional-grade operation. Some users questioned why they downloaded from APKPure instead of official sources, while others emphasized the importance of verifying app signatures.

**Tags**: `#supply-chain-attack`, `#malware-analysis`, `#mobile-security`, `#spyware`, `#telegram`

---

<a id="item-9"></a>
## [Armin Ronacher Critiques AI-Generated Bug Reports](https://simonwillison.net/2026/May/24/armin-ronacher/#atom-everything) ⭐️ 6.0/10

Open source developer Armin Ronacher published a critique of AI-generated issue reports, calling them inaccurate but confidently stated "guesswork" that wastes maintainer time. He proposes a simple four-step structured format: what command was run, what was expected, what actually happened, and the exact error log. As AI-assisted development tools proliferate, open source maintainers increasingly receive low-quality submissions filled with fabricated minimal repros and wrong root cause analyses. This critique addresses a growing pain point affecting project sustainability and developer productivity across the ecosystem. The critique specifically mentions "clanker," a derogatory slang term in developer communities for AI chatbots and robots. These AI-generated issues typically contain fake minimal reproductions, incorrect code analogies, and confident but wrong conclusions—a pattern Ronacher has observed on his terminal emulator project Pi.

rss · Simon Willison · May 24, 18:46

**Background**: Armin Ronacher is a well-known open source developer best known for creating Flask and Jinja2, two foundational Python web development tools. He maintains several influential Python projects and writes regularly about software development practices. "Clanker" is informal slang among developers for AI systems, often used pejoratively to describe automated outputs that lack genuine understanding.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Clanker">Clanker - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#bug-reporting`, `#AI-limitations`, `#developer-experience`, `#software-maintenance`

---

<a id="item-10"></a>
## [Shenzhou 23 Crew Announced with First Hong Kong Payload Expert](https://t.me/zaihuapd/41554) ⭐️ 6.0/10

China has announced the Shenzhou 23 crew composition featuring Zhu Yangzhu as commander, Zhang Zhiyuan as spacecraft pilot, and Li Jiaying as payload expert—the first female payload specialist from Hong Kong or Macau. The crew marks the first mission entirely composed of third and fourth batch astronauts, with launch scheduled for May 24, 2026 at 23:08 Beijing time. This mission represents multiple milestones for China's space program, demonstrating the operational readiness of its newer astronaut cohorts and marking Hong Kong and Macau's first direct participation in crewed spaceflight. Li Jiaying's selection as a payload expert underscores Beijing's effort to integrate regional talent into national space endeavors. Zhu Yangzhu, a flight engineer who previously flew on Shenzhou 16, becomes the first flight engineer to serve as crew commander. Li Jiaying is the first fourth-batch astronaut to execute a flight mission and the first female payload expert selected from Hong Kong or Macau. One crew member will undertake a one-year orbital mission.

telegram · zaihuapd · May 24, 15:13

**Background**: China has selected four batches of astronauts totaling 49 individuals, with 26 having completed at least one crewed mission as of May 2026. The fourth batch, selected in 2024, includes 10 reserve astronauts—8 spacecraft pilots and 2 payload experts, with one payload expert each from Hong Kong and Macau regions. Payload specialists are scientists or engineers with expertise in specific experiments who support scientific and technical operations aboard spacecraft.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Payload_specialist">Payload specialist - Wikipedia</a></li>
<li><a href="https://zh.wikipedia.org/zh-hans/中国航天员列表">中国航天员列表 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.gov.cn/yaowen/liebiao/202406/content_6956704.htm">我国第四批预备航天员选拔工作顺利完成 港澳地区各有1人入选__中国政...</a></li>

</ul>
</details>

**Tags**: `#China Space Program`, `#Shenzhou`, `#Human Spaceflight`, `#Hong Kong`, `#Astronaut Corps`

---