---
layout: default
title: "Horizon 每日速递: 2026-05-25"
date: 2026-05-25
lang: zh
---

> 从 26 条内容中筛选出 10 条重要资讯

---

1. [约束衰减：大型语言模型智能体在架构规则下的脆弱性](#item-1) ⭐️ 8.0/10
2. [内存成本占 AI 芯片组件成本近三分之二](#item-2) ⭐️ 7.0/10
3. [微软开源迄今发现最早的 DOS 源代码](#item-3) ⭐️ 7.0/10
4. [Greg Brockman 采访引发 OpenAI 治理结构热议](#item-4) ⭐️ 7.0/10
5. [诈骗者滥用微软内部域名发送垃圾邮件](#item-5) ⭐️ 7.0/10
6. [16 字节程序震撼 Hacker News：极限代码优化展示](#item-6) ⭐️ 7.0/10
7. [AMD 取消 Vivado 免费版 Linux 支持，引发社区强烈反对](#item-7) ⭐️ 7.0/10
8. [APKPure 上的 Telegram 被植入 DataCollector 间谍框架](#item-8) ⭐️ 7.0/10
9. [Armin Ronacher 批评 AI 生成的 Bug 报告](#item-9) ⭐️ 6.0/10
10. [神舟二十三号乘组公布 首位港澳载荷专家入选](#item-10) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [约束衰减：大型语言模型智能体在架构规则下的脆弱性](https://arxiv.org/abs/2605.06445) ⭐️ 8.0/10

研究人员发表在 arxiv 上的论文（编号 2605.06445）揭示了大型语言模型编码智能体存在"约束衰减"现象——当在累积的建筑、ORM 和框架约束下生成多文件后端代码时，断言通过率下降约 30 个百分点。 这一发现直接挑战了人工智能编码助手在生产级后端开发中的可靠性，表明尽管这些工具在快速原型设计方面表现出色，但对于需要严格遵守架构约定的复杂系统仍不适用。 性能下降在惯例密集型框架上表现得最为严重，研究作者承认了一个局限性：由于成本原因，未能对前沿模型进行全面测试。可靠性的丧失发生在约束累积的过程中，而非表现为孤立的规则违反。

hackernews · wek · 05月24日 12:55 · [社区讨论](https://news.ycombinator.com/item?id=48256912)

**背景**: 大型语言模型智能体是使用大型语言模型自主执行编码任务的人工智能系统，通常生成多个文件并协调复杂的开发工作流程。"约束衰减"指的是这些智能体能够成功完成无约束的编码任务，但随着显式架构规则、框架约定和数据库模式的引入而逐渐失败的现象。这对于后端开发尤其重要，因为后端开发通常涉及具有严格结构要求的多个互联组件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.alphaxiv.org/overview/2605.06445v1">Constraint Decay : The Fragility of LLM Agents in Backend... | alphaXiv</a></li>
<li><a href="https://agentpatterns.ai/verification/constraint-decay-backend-agents/">Constraint Decay in Backend Code Generation - AgentPatterns.ai</a></li>
<li><a href="https://news.ycombinator.com/item?id=48256912">Constraint Decay : The Fragility of LLM Agents in Back... | Hacker News</a></li>

</ul>
</details>

**社区讨论**: 这项研究引发了热烈讨论，评论者根据自身经验验证了这些发现。一位实践者指出，他们观察到了类似的"钙化"效应，即架构模式在代码库中变得根深蒂固。其他人强调，结构化智能体编排器可能有所帮助，但仍然需要 5-10 轮审查修复周期来确保实现符合规范。共识认为该局限性在生产环境中确实存在，尽管一些人认为与其他学科相比，大型语言模型在长期编程任务中仍优于人类。

**标签**: `#llm-agents`, `#code-generation`, `#constraint-decay`, `#ai-reliability`, `#software-engineering`

---

<a id="item-2"></a>
## [内存成本占 AI 芯片组件成本近三分之二](https://epoch.ai/data-insights/ai-chip-component-cost-shares) ⭐️ 7.0/10

根据 Epoch AI 数据，内存现在占 AI 芯片组件总成本的近三分之二（约 65%），这代表了 AI 硬件经济学和供应链动态的重大转变。 这种成本再平衡使内存成为 AI 加速器的主要成本驱动因素，对基础设施规划产生了重大影响，并为 DRAM 供应赶上需求时实现大幅硬件成本降低创造了可能。 高带宽内存（HBM）是用于 NVIDIA GPU 等 AI 加速器中的 3D 堆叠内存技术，是这一成本转变的主要驱动因素。社区分析师指出，等待 DRAM 供应正常化可能带来约 3 倍的硬件成本降低，但内存容量每年 20-25%的增长速率可能跟不上 AI 需求的增长。

hackernews · intelkishan · 05月24日 16:31 · [社区讨论](https://news.ycombinator.com/item?id=48258684)

**背景**: 高带宽内存（HBM）是一种 3D 堆叠式同步动态随机存取存储器技术，由三星、AMD 和 SK 海力士联合开发，使用硅通孔（TSV）技术连接堆叠的内存芯片。与传统 DRAM 相比，HBM 提供更高的带宽和更低的功耗，使其成为 AI 训练和推理工作负载的关键组件。在 SK 海力士取代三星成为市场领导者后，HBM 市场预计到 2026 年将达到 580 亿美元，完全由 AI 加速器需求驱动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://introl.com/blog/hbm-evolution-hbm3-hbm3e-hbm4-memory-ai-gpu-2025">HBM evolution: from HBM3 to HBM4 and the AI memory war</a></li>
<li><a href="https://www.linkedin.com/pulse/high-bandwidth-memory-hbm-ai-crossroads-customization-czfdc">High Bandwidth Memory ( HBM ) at the AI Crossroads: Customization...</a></li>

</ul>
</details>

**社区讨论**: 社区讨论显示出乐观与沮丧并存的情绪。一位评论者指出，等待 DRAM 供应正常化可能实现约 3 倍的硬件成本降低和约 2 倍的总成本降低，无需任何技术突破。然而，其他人则对消费级内存价格的上涨表示不满（一位用户注意到 96GB 内存从 250 美元涨到 1200 美元），有些人表示在价格合理之前拒绝升级。人们对每年 20-25%的内存容量增长是否能跟上 AI 需求表示担忧，并对制造商是否愿意冒险过度供应持怀疑态度。

**标签**: `#AI chips`, `#hardware costs`, `#memory/DRAM`, `#AI infrastructure`, `#supply chain`

---

<a id="item-3"></a>
## [微软开源迄今发现最早的 DOS 源代码](https://arstechnica.com/gadgets/2026/04/microsoft-open-sources-the-earliest-dos-source-code-discovered-to-date/) ⭐️ 7.0/10

微软已开源迄今发现最早的 DOS 源代码，这批代码由以 Yufeng Gao 和 Rich Cini 为首的历史学家和文物保护团队通过 OCR 技术从数十年前的打印稿中恢复而来。该代码存储在 GitHub 仓库中，隶属于 DOS 反编译小组（DOS Disassembly Group），标志着软件考古学和数字文物保护领域的重要里程碑。 此次发布使开发者、历史学家和复古计算爱好者能够接触到这一关键的计算遗产，为后代保护 PC 时代的技术基础。这也凸显了微软进入操作系统领域的偶然性——起因是 IBM 与数字研究公司（Digital Research）关于 CP/M 的谈判失败。 恢复过程极具挑战性，因为源代码早于数字存储时代，仅以开发者 Tim Paterson 的纸质打印稿形式存在。现代 OCR 软件难以识别这些数十年前文件的老化质量，文物保护团队不得不进行大量手动转录工作。微软同时开源了配套的 BASIC 代码，评论者指出 BASIC 才是微软的核心业务，DOS 只是为其赢得了操作系统合同的敲门砖。

hackernews · DamnInteresting · 05月24日 01:21 · [社区讨论](https://news.ycombinator.com/item?id=48253386)

**背景**: 软件考古学是对遗留软件系统进行系统化恢复和分析的学科，特别适用于文档不完整或缺失的软件，涉及逆向工程和多种用于提取程序结构的工具。DOS（磁盘操作系统）是微软在 1981 年为 IBM 原始 PC 提供的操作系统，最终成为主导 PC 操作系统生态系统的基础。2018 年，联合国教科文组织专家通过的《软件源代码作为遗产促进可持续发展的巴黎呼吁》将源代码保护认定为可持续数字遗产的重要组成部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Software_archaeology">Software archaeology</a></li>
<li><a href="https://www.unesco.org/en/articles/experts-call-greater-recognition-software-source-code-heritage-sustainable-development">Experts call for greater recognition of software source code ...</a></li>

</ul>
</details>

**社区讨论**: 社区反应非常积极，评论者们称赞微软的这次发布，同时强调 BASIC 作为微软真正核心的历史重要性。一位评论者表达了对仅凭数千行汇编代码就能成功创业的羡慕，另一位则解释了 IBM 在数字研究公司拒绝签署 CP/M 保密协议后转向微软的关键谈判故事。从纸质打印稿进行 OCR 恢复的过程被反复提及为一项卓越的保护成就。

**标签**: `#open-source`, `#software-history`, `#DOS`, `#Microsoft`, `#retro-computing`

---

<a id="item-4"></a>
## [Greg Brockman 采访引发 OpenAI 治理结构热议](https://fs.blog/knowledge-project-podcast/greg-brockman/) ⭐️ 7.0/10

OpenAI 总裁 Greg Brockman 在 Knowledge Project 播客节目中亮相，讨论了公司历史、治理结构以及导致 CEO Sam Altman 短暂被董事会罢免的 2023 年领导层危机。该采访在 Hacker News 上获得了 166 个点赞和 157 条评论，社区成员就 Brockman 是否对 Ilya Sutskever 解雇事件等悬而未决的问题提供了足够的深度展开了辩论。 作为 Altman 和 Musk 的原始联合创始人之一，Brockman 的内部视角对于理解公司非营利起源与价值千亿美元商业企业之间的紧张关系具有重要价值。此采访正值 OpenAI 治理模式受到持续审查、以及最近减少非营利董事会监督权的提案之际发布。 评论者指出，采访内容很大程度上是已熟知的事件，并未提供新的爆料，一位用户质疑为何无人追问危机期间"Ilya 心里到底在想什么"。讨论还涉及 Musk 对 OpenAI 的诉讼，该诉讼公开了 Brockman 的私人日记，其中包含"经济上什么能让我达到 10 亿美元？"等条目。

hackernews · prakashqwerty · 05月24日 08:29 · [社区讨论](https://news.ycombinator.com/item?id=48255593)

**背景**: OpenAI 于 2015 年作为特拉华州非营利组织成立，使命是构建造福人类的安全通用人工智能(AGI)。2019 年，它创建了一个利润上限子公司以吸引资金，到 2025 年将该子公司转换为公共利益公司(PBC)，由非营利组织持有 26%股份。2023 年 11 月，OpenAI 董事会突然罢免 CEO Sam Altman，Reuters 将其描述为首席科学家 Ilya Sutskever 因 AI 安全问题领导的"董事会政变"。Sutskever 后来对参与该决定表示深感后悔，Altman 在几天内复职。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/information-technology/2023/11/report-sutskever-led-board-coup-at-openai-that-ousted-altman-over-ai-safety-concerns/">Details emerge of surprise board coup that ousted CEO Sam Altman ...</a></li>
<li><a href="https://www.axios.com/2023/11/20/sam-altman-fired-openai-board-illya-sutsever-regrets">OpenAI chief scientist says he regrets board’s firing of Sam Altman</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI">OpenAI - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一，部分评论者将采访斥为"科技现实电视"式的肤浅企业八卦报道，而另一些人则对 OpenAI 非营利结构是否只是有利的法律称号而非真正承诺提出了实质性担忧。主流批评集中在采访对悬而未决问题缺乏深度，尤其是关于 Sutskever 的动机和更广泛治理影响的问题。

**标签**: `#openai`, `#ai-safety`, `#interview`, `#tech-leadership`, `#governance`

---

<a id="item-5"></a>
## [诈骗者滥用微软内部域名发送垃圾邮件](https://techcrunch.com/2026/05/21/scammers-are-abusing-an-internal-microsoft-account-to-send-spam/) ⭐️ 7.0/10

安全研究人员发现，诈骗者正在利用微软的一个内部域名发送钓鱼邮件和垃圾链接。此次攻击利用了微软自己的域名基础设施，使恶意邮件看起来合法，因为它们来自微软的可信基础设施。 这一事件暴露了企业域名管理和邮件认证系统中的关键漏洞。当可信的服务提供商本身成为恶意流量的来源时，依靠域名验证邮件的组织可能会发现他们的安全假设被颠覆。 攻击者利用了微软庞大的域名组合和复杂的内部基础设施。社区成员指出，微软在不同的服务中拥有众多域名，使用户几乎无法在没有完整清单的情况下验证合法的发件人。

hackernews · spike021 · 05月24日 00:51 · [社区讨论](https://news.ycombinator.com/item?id=48253186)

**背景**: 企业邮件安全依赖于 SPF（发件人策略框架）、DKIM（域名密钥识别邮件）和 DMARC（基于域名的消息认证、报告和一致性）等协议来防止邮件欺骗。这些技术验证邮件是否来自授权服务器，帮助收件人识别欺诈信息。然而，当攻击者滥用内部基础设施或可信域名时，这些认证机制可能无法阻止恶意邮件，因为它们在技术上来自合法来源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cwe.mitre.org/data/definitions/290.html">CWE - CWE-290: Authentication Bypass by Spoofing (4.20)</a></li>
<li><a href="https://www.sentinelone.com/cybersecurity-101/cybersecurity/enterprise-email-security/">Enterprise Email Security: Importance and Best Practices</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论显示出社区对微软域名管理实践的广泛不满。评论者指出，微软使用大量独立域名（如 microsoftonline.com）使得普通用户几乎无法进行验证。一位用户报告了 Authenticator 应用程序的异常行为，显示来自未知位置的登录通知，但登录历史记录却为空，这引发了对认证透明性的担忧。还有人强调了视觉欺骗漏洞，在某些字体中'm'和'rn'看起来几乎相同，表明仅依靠域名验证不足以保证安全。

**标签**: `#security`, `#phishing`, `#microsoft`, `#email-spoofing`, `#cybersecurity`

---

<a id="item-6"></a>
## [16 字节程序震撼 Hacker News：极限代码优化展示](https://hellmood.111mb.de/wake_up_16b_writeup.html) ⭐️ 7.0/10

一位 Hacker News 用户分享了一个仅 16 字节的生成式演示程序，通过极致的代码大小优化创造出视听效果，获得了 408 个赞同和 31 条评论的社区关注。 该演示程序仅占用 16 字节，很可能利用了未文档化的 x86 指令或某些操作码的副作用来生成输出。评论者指出，这超出了他们对 32 字节演示的预期——他们曾认为那已经是"能保持视觉效果的最小组件大小极限"。

hackernews · MaximilianEmel · 05月24日 00:30 · [社区讨论](https://news.ycombinator.com/item?id=48253060)

**背景**: Demo 场景是一个可追溯到 1980 年代的国际计算机艺术亚文化，程序员们创作独立的视听展示来展示技术实力。代码高尔夫是一种休闲编程竞赛，参与者努力用最短的源代码解决问题。Demo 场景传统上设有 64k intro 和 4k intro 等竞赛类别，因此 16 字节是一个非凡的成就，将大小限制推向了绝对极限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Demoscene">Demoscene</a></li>
<li><a href="https://en.wikipedia.org/wiki/Code_golf">Code golf</a></li>

</ul>
</details>

**社区讨论**: 社区反应非常积极，评论者们对这项工艺表示惊叹。一位用户赞叹道" Witch!"（太神奇了！），另一位则分享说这个演示让他陷入了一个小时的探索之旅，最终和另一个人一起用递归 PowerPoint 制作了一个谢尔宾斯基三角形。社区的共识是称其为"退休后可供纪念的杰作"，同时认为这可能激励在其他架构上进行类似的追求。

**标签**: `#demo-scene`, `#code-golf`, `#x86`, `#code-size-optimization`, `#assembly`

---

<a id="item-7"></a>
## [AMD 取消 Vivado 免费版 Linux 支持，引发社区强烈反对](https://adaptivesupport.amd.com/s/question/0D5Pd00001YQLdMKAX/why-is-vivado-20261-dropping-linux-support-for-free-tier-?language=en_US) ⭐️ 7.0/10

AMD/Xilinx 宣布 Vivado 2026.1 将取消免费版"WebPACK"的 Linux 支持，迫使 Linux 用户要么付费购买许可，要么更换平台。此举引发了 174 条以上实质性评论和 295 个互动点，社区成员表示此举疏远了学生、爱好者和企业开发者。 这一决定可能重塑 FPGA 生态系统，推动开发者转向 Lattice 等竞争对手，后者为所有基础芯片提供免费软件工具。取消 Linux 支持削弱了 AMD 在开源社区中扩大采用率的战略，而 Linux 是开发领域的主导平台。 Basic/WebPACK 层级之前同时支持 Windows 和 Linux 开发；此次变更后，免费版将仅支持 Windows。有评论者指出，AMD 自己的文档建议在某些工具上使用 Linux，使这一政策矛盾特别令人沮丧。用户反映 Lattice 的免费工具链覆盖 ECP5 和 Certus 芯片，无需付费许可。

hackernews · zdw · 05月24日 04:14 · [社区讨论](https://news.ycombinator.com/item?id=48254309)

**背景**: FPGA（现场可编程门阵列）是一种可重新编程的集成电路，允许工程师在不制造定制芯片的情况下设计自定义硬件。Vivado Design Suite 是 AMD/Xilinx 用于编程其 FPGA 和 SoC 产品的主要工具链。免费版"WebPACK"历来对学生、爱好者和小型团队至关重要，他们可以在购买商业许可之前学习和原型设计 Xilinx 硬件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Field-programmable_gate_array">Field - programmable gate array - Wikipedia</a></li>
<li><a href="https://www.amd.com/en/products/software/adaptive-socs-and-fpgas/vivado.html">AMD Vivado™ Design Suite</a></li>

</ul>
</details>

**社区讨论**: 社区成员表达了强烈不满，企业长期用户指出他们在 Xilinx 硬件上花费了"数十万美元"，但对新电脑和 CI 系统的许可流程感到恼火。多位评论者建议转向 Lattice，称其文档更好且没有许可麻烦。一位前 Altera 用户警告说，AMD 似乎正在重蹈英特尔收购后关闭社区互动的错误，并指出 Xilinx 强大的爱好者社区是一个关键竞争优势。

**标签**: `#FPGA`, `#Vivado`, `#AMD/Xilinx`, `#Linux`, `#Developer Tools`

---

<a id="item-8"></a>
## [APKPure 上的 Telegram 被植入 DataCollector 间谍框架](https://x.com/EricParker/status/2058411298195661221) ⭐️ 7.0/10

安全研究人员发现，APKPure 应用商店分发了一个恶意版本的 Telegram 12.6.5。该木马应用包含一个名为 DataCollector 的复杂间谍框架，嵌入在超过 3000 行的 classes3.dex 文件中，能够窃取消息、联系人、媒体文件、位置和 SIM 卡数据，并上传至 C2 服务器 38.190.225.166。 这是一次针对依赖第三方应用商店而非官方渠道的用户的严重供应链攻击。该恶意软件的先进功能——包括加密数据传输和全面数据收集——对可能数百万受影响用户构成重大隐私和安全风险，这些用户下载该应用时相信它是合法的。 被植入木马的 Telegram 经过重新签名和打包，携带恶意 DataCollector 框架。被窃取的数据在使用 AES-GCM 加密后才发送到命令与控制服务器。恶意代码位于 classes3.dex 中，这是标准的 Android Dalvik 可执行文件格式，包含在 Android 运行时上运行的编译应用程序代码。

telegram · zaihuapd · 05月24日 11:38

**背景**: APKPure 是一个流行的第三方 Android 应用商店，允许用户下载 Google Play 上未提供或旧版本的应用程序 APK 文件。.dex 文件格式（Dalvik 可执行文件）用于存储 Android 的编译应用程序代码。涉及重新打包合法应用程序的供应链攻击特别危险，因为它们利用用户对熟悉应用的信任，并且在秘密收集数据的同时看起来运行正常，可以绕过普通的安全检查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://alternativeto.net/software/apk-pure/">Best APKPure Alternatives : Top App Stores in 2025 | AlternativeTo</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apk_(file_format)">apk (file format ) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Block_cipher_mode_of_operation">Block cipher mode of operation - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 安全社区对针对第三方应用商店的供应链攻击日益复杂化表示担忧。Eric Parker 的披露被广泛传播，其他研究人员强调使用 AES-GCM 加密是专业级操作的证据。一些用户质疑为什么从 APKPure 而非官方来源下载，而另一些人则强调验证应用签名的重要性。

**标签**: `#supply-chain-attack`, `#malware-analysis`, `#mobile-security`, `#spyware`, `#telegram`

---

<a id="item-9"></a>
## [Armin Ronacher 批评 AI 生成的 Bug 报告](https://simonwillison.net/2026/May/24/armin-ronacher/#atom-everything) ⭐️ 6.0/10

开源开发者 Armin Ronacher 发表了一篇文章批评 AI 生成的 issue 报告，称这些报告是不准确但充满自信的"猜测"，浪费维护者的时间。他提出了一个简单的四步结构化格式：运行了什么命令、期望发生什么、实际发生了什么，以及确切的错误日志。 随着 AI 辅助开发工具的普及，开源项目维护者越来越多地收到包含虚假最小可复现示例和错误根本原因分析的低质量提交。这篇批评文章针对的是影响整个生态系统中项目可持续性和开发者生产力的问题。 这篇批评特别提到了"clanker"，这是开发者社区中对 AI 聊天机器人和机器人的贬义俚语。这些 AI 生成的 issue 通常包含虚假的最小可复现示例、错误的代码类比，以及自信但错误的结论——Ronacher 在他的终端模拟器项目 Pi 上观察到了这种模式。

rss · Simon Willison · 05月24日 18:46

**背景**: Armin Ronacher 是一位知名的开源开发者，以创建 Flask 和 Jinja2 这两个 Python Web 开发基础工具而闻名。他维护着多个有影响力的 Python 项目，并经常撰写关于软件开发实践的文章。"Clanker" 是开发者之间对 AI 系统的非正式俚语，通常用作贬义词来形容缺乏真正理解的自动化输出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Clanker">Clanker - Wikipedia</a></li>

</ul>
</details>

**标签**: `#open-source`, `#bug-reporting`, `#AI-limitations`, `#developer-experience`, `#software-maintenance`

---

<a id="item-10"></a>
## [神舟二十三号乘组公布 首位港澳载荷专家入选](https://t.me/zaihuapd/41554) ⭐️ 6.0/10

中国公布了神舟二十三号乘组组成，由朱杨柱担任指令长、张志远担任航天驾驶员、黎家盈担任载荷专家，其中黎家盈是首位来自香港或澳门的女性载荷专家。该乘组是我国首个全部由第三批和第四批航天员组成的任务，飞船计划于 2026 年 5 月 24 日 23 时 08 分发射。 此次任务代表中国航天计划的多个里程碑，表明新一代航天员已具备执行任务的能力，也标志着香港和澳门首次直接参与载人航天任务。黎家盈被选为载荷专家凸显了北京将区域人才纳入国家航天事业的努力。 朱杨柱曾执行过神舟十六号任务，此次成为首位担任指令长的航天飞行工程师。黎家盈是首位执行飞行任务的第四批航天员，也是面向港澳选拔的首位女性载荷专家。乘组中有一人将执行一年期飞行任务。

telegram · zaihuapd · 05月24日 15:13

**背景**: 截至 2026 年 5 月，中国共选拔了四批共 49 名航天员，其中 26 人已有过至少一次执行载人航天飞行任务的经历。第四批预备航天员于 2024 年选拔完成，共有 10 名预备航天员入选，包括 8 名航天驾驶员和 2 名载荷专家（香港、澳门地区各 1 名）。载荷专家是具备特定实验专业知识的科学家或工程师，负责在航天器上执行综合性航天实验任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Payload_specialist">Payload specialist - Wikipedia</a></li>
<li><a href="https://zh.wikipedia.org/zh-hans/中国航天员列表">中国航天员列表 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.gov.cn/yaowen/liebiao/202406/content_6956704.htm">我国第四批预备航天员选拔工作顺利完成 港澳地区各有1人入选__中国政...</a></li>

</ul>
</details>

**标签**: `#China Space Program`, `#Shenzhou`, `#Human Spaceflight`, `#Hong Kong`, `#Astronaut Corps`

---