---
layout: default
title: "Horizon 每日速递: 2026-05-09"
date: 2026-05-09
lang: zh
---

> 从 42 条内容中筛选出 23 条重要资讯

---

1. [Modular AI 发布 Mojo 1.0 Beta 版本](#item-1) ⭐️ 8.0/10
2. [Gemma 4 26B 通过 DFlash 推测解码在 RTX 5090 上实现 578 tok/s](#item-2) ⭐️ 8.0/10
3. [AI 正在重塑漏洞披露文化](#item-3) ⭐️ 7.0/10
4. [HTML 工件在 AI 代码输出方面优于 Markdown](#item-4) ⭐️ 7.0/10
5. [DeepSeek 寻求创纪录 73.5 亿美元融资 V4.1 将于 6 月发布](#item-5) ⭐️ 7.0/10
6. [OpenAI 发布 Codex Chrome 扩展，实现浏览器自动化](#item-6) ⭐️ 7.0/10
7. [Canvas 平台期末周遭入侵 美国多所学校受影响](#item-7) ⭐️ 7.0/10
8. [Cloudflare 裁减逾 1100 名员工，AI 智能体重塑组织架构](#item-8) ⭐️ 7.0/10
9. [苹果据报考虑结束与台积电 12 年独家代工合作](#item-9) ⭐️ 7.0/10
10. [谷歌 reCAPTCHA 在去谷歌化安卓设备上失效](#item-10) ⭐️ 6.0/10
11. [在内存中运行的树莓派 Zero 上托管静态网站](#item-11) ⭐️ 6.0/10
12. [Meshtastic LoRa 网状网络系统介绍](#item-12) ⭐️ 6.0/10
13. [US Government releases first batch of UAP documents and videos](#item-13) ⭐️ 6.0/10
14. [vLLM ROCm 后端已添加到 Lemonade，支持 AMD GPU](#item-14) ⭐️ 6.0/10
15. [Qwen 35B MoE 模型在 12GB 显存 RTX 3060 上实现有效运行](#item-15) ⭐️ 6.0/10
16. [Allen AI 发布 EMO 混合专家模型 采用文档级专家路由](#item-16) ⭐️ 6.0/10
17. [Qwen3.6-27B 在单张 RTX 4090 上实现 262K 上下文下 80+ t/s 吞吐量](#item-17) ⭐️ 6.0/10
18. [Z-lab 发布搭载 DFlash 推测解码的 Gemma 4 26B 模型](#item-18) ⭐️ 6.0/10
19. [ChatGPT 推出信任联系人功能，检测自残话题时通知亲友](#item-19) ⭐️ 6.0/10
20. [最高法院否决特朗普 IEEPA 关税 随即签署 10%临时关税令](#item-20) ⭐️ 6.0/10
21. [Anthropic 计划百亿级新融资，估值将反超 OpenAI](#item-21) ⭐️ 6.0/10
22. [美国调查英伟达芯片经泰国走私至中国案](#item-22) ⭐️ 6.0/10
23. [DeepSeek 据报首轮大额融资估值或达 450 亿美元](#item-23) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Modular AI 发布 Mojo 1.0 Beta 版本](https://mojolang.org/) ⭐️ 8.0/10

Modular AI 发布了 Mojo 1.0 Beta，这是专为 ML/AI 工作负载设计的 Python 兼容系统编程语言的一个重要里程碑。该版本由 Chris Lattner 团队开发，该公司最近以 16 亿美元估值融资 2.5 亿美元。 Mojo 旨在解决将 Python 的易用性与 C++/Rust 级别性能相结合的长期问题，可能彻底改变开发者编写高性能 AI 内核的方式。如果成功，它可以取代 Numba 和 Triton 等分散的解决方案，同时实现单一语言统一编程 CPU 和 GPU。 Mojo 实现了与 Rust 相似的所有权模型，具有比 Zig 更强大的"编译时计算"（comptime）功能，并包含一流的 SIMD 支持。值得注意的是，Mojo 不仅仅是 LLVM 的包装器——虽然涉及 LLVM，但其使用方式与 Rust 或 Zig 不同。该语言的开源版本计划于 2026 年秋季发布。

hackernews · sbt567 · 05月8日 02:49 · [社区讨论](https://news.ycombinator.com/item?id=48057901)

**背景**: Mojo 由 Modular AI 创建，这是一家于 2017 年成立的 AI 基础设施公司，由之前创建 LLVM、Clang 和 Swift 的 Chris Lattner 创立。该语言目前是专有的，适用于 Linux 和 macOS。Mojo 旨在填补 Python 在 AI 工作负载方面的性能差距，同时保持 Python 兼容性以确保易用性。ML/AI 领域目前使用多种性能加速方法，包括 CUDA（NVIDIA 专用）、Numba（Python JIT 编译器）和 Julia（高性能数值计算语言）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mojolang.org/">Mojo</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mojo_(programming_language)">Mojo (programming language) - Wikipedia</a></li>
<li><a href="https://www.modular.com/company/about">Modular: About Us</a></li>

</ul>
</details>

**社区讨论**: 社区反应混合但总体乐观。支持者称赞 Mojo 的所有权模型、comptime 功能和其新颖的非 LLVM 包装器编译方法，认为这对系统编程具有革命性意义。然而，怀疑者对其与标准 Python 行为的差异（如字符串索引不符合预期）、潜在的正确性问题，以及它是否真正解决了 Julia 加 Numba/Triton 尚未解决的问题表示担忧。一些开发者也对语言的闭源性质表示不满。

**标签**: `#mojo`, `#programming-languages`, `#machine-learning`, `#python`, `#systems-programming`

---

<a id="item-2"></a>
## [Gemma 4 26B 通过 DFlash 推测解码在 RTX 5090 上实现 578 tok/s](https://www.reddit.com/r/LocalLLaMA/comments/1t796qe/gemma_4_26b_hits_600_toks_on_one_rtx_5090/) ⭐️ 8.0/10

使用 vLLM 0.19.2rc1 上的 DFlash 推测解码进行基准测试，在单张 RTX 5090 上使 Gemma 4 26B 模型达到约 578 输出 token/秒，相比 228 tok/s 的基线实现了 2.56 倍加速。最佳配置使用 num_speculative_tokens=13 和 max_num_batched_tokens=8192，将平均端到端延迟从 4455ms 降低到 1738ms。 这一基准测试表明，DFlash 推测解码可以显著加速本地 LLM 推理且不影响输出质量，使 Gemma 4 26B 等大型模型在消费级硬件上更加实用。该发现为开发者在 RTX 5090 等新一代 GPU 上优化推理流程提供了可操作的配置指导。 基准测试探索了 num_speculative_tokens 在 0-15 范围内的 15 种不同参数设置，发现最优值取决于延迟指标：num_speculative_tokens=13 配合 max_num_batched_tokens=4096 提供略好的平均延迟但 p95 延迟更差，而将批处理 token 增加到 8192 则提供更稳定的尾延迟。测试工作负载使用 256 个输入 token 和 1024 个输出 token，并发为 1。

reddit · r/LocalLLaMA · chain-77 · 05月8日 14:13

**背景**: DFlash（用于 Flash 推测解码的块扩散模型）是一种轻量级块扩散模型，通过将扩散模型限制在起草阶段来实现高效的并行起草。推测解码采用草稿-验证范式，其中较小较快的草稿模型提出 token，然后由较大的目标模型并行验证。AWQ（激活感知权重量化）是一种 4 位量化技术，将 Gemma 4 26B 等模型压缩为 4 位权重格式（AWQ-4bit），以减少内存占用并加速推理同时保持质量。vLLM 是一个开源推理服务框架，通过 PagedAttention 实现高效的 KV 缓存管理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/z-lab/dflash">GitHub - z-lab/dflash: DFlash: Block Diffusion for Flash Speculative Decoding · GitHub</a></li>
<li><a href="https://arxiv.org/abs/2602.06036">[2602.06036] DFlash: Block Diffusion for Flash Speculative Decoding</a></li>
<li><a href="https://arxiv.org/abs/2306.00978">[2306.00978] AWQ: Activation-aware Weight Quantization for LLM Compression and Acceleration</a></li>
<li><a href="https://research.google/blog/looking-back-at-speculative-decoding/">Looking back at speculative decoding - Google Research</a></li>

</ul>
</details>

**社区讨论**: 该 Reddit 帖子获得了 99 的高分，表明社区的高度认可。读者对比较不同硬件（特别是 RTX 4090）和其他模型系列（如 Qwen）的结果表示兴趣。作者观察到平均延迟优化并不能自动优化尾延迟，这引起社区共鸣，突显了在调整推测解码参数时同时考虑两个指标的重要性。

**标签**: `#llm-inference`, `#speculative-decoding`, `#vllm`, `#rtx-5090`, `#performance-optimization`

---

<a id="item-3"></a>
## [AI 正在重塑漏洞披露文化](https://www.jefftk.com/p/ai-is-breaking-two-vulnerability-cultures) ⭐️ 7.0/10

安全专家正在讨论 AI 是否从根本上改变了漏洞研究和披露的时间线，Log4Shell 作为一个关键案例，表明攻击者能以多快的速度将补丁武器化。 如果 AI 大幅缩短了补丁可用与漏洞利用武器化之间的时间窗口，传统的协调漏洞披露模式将变得不那么可行，可能会迫使安全社区从根本上改变处理零日漏洞的方式。 Log4Shell 的时间线说明了这种压缩：阿里巴巴发现漏洞并报告给 Apache，补丁被推送到 git，黑客在公开披露之前就开始利用它，并在数小时内于 Minecraft 社区传播攻击。

hackernews · speckx · 05月8日 17:55 · [社区讨论](https://news.ycombinator.com/item?id=48066524)

**背景**: Log4Shell（CVE-2021-44228）是 Apache Log4j 2 中的一个关键远程代码执行漏洞，Log4j 2 是一个广泛使用的 Java 日志库，影响了数亿台设备。协调漏洞披露（CVD）是一种模式，研究人员私下通知供应商，允许他们在公开披露前有时间为开发和部署补丁留出时间。这种宽限期传统上从几天到几个月不等，假设防御者需要提前时间来更新系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Log4Shell">Log4Shell - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Coordinated_vulnerability_disclosure">Coordinated vulnerability disclosure</a></li>

</ul>
</details>

**社区讨论**: 社区观点明显分歧：tptacek 认为这种转变是由于软件透明度提高（开源采用、反编译工具改进）而非 AI 本身导致的，是不可避免的。freeqaz 提供了 Log4Shell 竞赛的详细时间线，显示攻击者移动速度有多快。rikafurude21 反驳说这只是将老问题（通过对比内核提交来寻找安全修复）重新包装成 AI 问题，认为更快的漏洞利用生成使协调披露变得更加重要而非不重要，因为各组织更新补丁的速度本来就差异很大。

**标签**: `#vulnerability-disclosure`, `#AI-security`, `#open-source-security`, `#coordinated-disclosure`, `#exploit-research`

---

<a id="item-4"></a>
## [HTML 工件在 AI 代码输出方面优于 Markdown](https://simonwillison.net/2026/May/8/unreasonable-effectiveness-of-html/#atom-everything) ⭐️ 7.0/10

Simon Willison 发布了一份实用指南，突出了 Thariq Shihipar 的一个见解：从 Claude Code 请求 HTML 工件比 Markdown 能产生更丰富、更交互式的输出。该技术使 AI 能够为 PR 审查和安全漏洞分析等任务生成包含 SVG 图表、交互式小部件和页面导航的解释。 Willison 通过让 GPT-5.5 生成 copy.fail 网站 Linux 权限提升漏洞的 HTML 解释来演示该技术，包含深色主题样式、安全警告和详细的分步说明。Claude Code 团队在 thariqs.github.io/html-effectiveness 上策划了一系列 HTML 有效性案例，展示了各种用例。

rss · Simon Willison · 05月8日 21:00

**背景**: Claude Artifacts 是一个功能，它将 AI 输出渲染为单独面板中的交互式元素，而不是聊天窗口中的静态文本。工件可以包括 React 组件、HTML 页面、SVG 和数据可视化。自 GPT-4 时代以来，许多开发者默认请求 Markdown 输出，因为它比 HTML 的 token 效率更高，但这源于 8,192 token 上下文窗口限制的约束。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ainskills.com/claude-artifacts-explained/">Claude Artifacts Explained - The Feature That Changes How You Use...</a></li>
<li><a href="https://www.c-sharpcorner.com/article/what-is-backpressure-in-streaming-systems-and-how-to-handle-it/">What Is Backpressure in Streaming Systems and How to Handle It?</a></li>
<li><a href="https://albato.com/blog/publications/how-to-use-claude-artifacts-guide">Claude Artifacts : What They Are & How to Use Them (2026 Guide)</a></li>

</ul>
</details>

**社区讨论**: Simon Willison 表示对在临时提示中尝试更丰富的 HTML 解释充满热情，他指出 2025 年 12 月关于 HTML 工具的文章主要关注交互式实用程序。社区似乎愿意重新考虑将 HTML 作为默认输出格式，尤其是随着 AI 模型的 token 限制已大幅扩展。

**标签**: `#AI coding tools`, `#Claude Code`, `#HTML artifacts`, `#Prompt engineering`, `#Developer productivity`

---

<a id="item-5"></a>
## [DeepSeek 寻求创纪录 73.5 亿美元融资 V4.1 将于 6 月发布](https://www.reddit.com/r/LocalLLaMA/comments/1t7bfpw/reports_suggest_deepseek_is_seeking_735_billion/) ⭐️ 7.0/10

据报道，DeepSeek 正在其首轮融资中寻求高达 500 亿元人民币（约 73.5 亿美元）的资金，这将是中国 AI 史上最大的单轮融资。作为其商业化和盈利计划的一部分，该公司还计划加快模型发布节奏，V4.1 预计将于 6 月推出。 这轮融资标志着 DeepSeek 从专注于研究的初创公司向商业化 AI 巨头转型，可能重塑全球 AI 行业的竞争格局。如果成功，它将验证投资者对中国 AI 创新的信心，尽管半导体出口限制仍在持续。 CEO 梁文锋计划在此轮融资中投入最大允许金额，显示出内部强烈的信心。融资促使 DeepSeek 将其发布节奏与主流行业惯例保持一致，摆脱此前较慢的迭代方式。该报道源自 The Information 引用的匿名消息人士，尚未得到证实。

reddit · r/LocalLLaMA · External_Mood4719 · 05月8日 15:34

**背景**: DeepSeek 由梁文锋于 2023 年 7 月创立，他是持有并资助该公司的中国对冲基金 High-Flyer 的联合创始人。2025 年 1 月，DeepSeek 凭借 DeepSeek-R1 推理模型的发布获得全球关注，该模型据报道仅用 600 万美元训练完成——相比 GPT-4 的 1 亿美元训练成本——采用了混合专家（MoE）层和出口受限的较弱芯片等技术。DeepSeek 的开源模型采用 MIT 许可证发布，允许免费商业使用和修改。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_(Company)">DeepSeek (Company)</a></li>

</ul>
</details>

**社区讨论**: Reddit 帖子获得了强烈关注（94 条评论），反应不一：一些社区成员对这一融资里程碑及其对开源 AI 开发的影响表示兴奋，而其他人则鉴于报道未经验证而呼吁谨慎。用户指出，DeepSeek 早期的颠覆性影响（导致英伟达市值蒸发 6000 亿美元）使这轮融资对 AI 生态系统尤为重要。

**标签**: `#DeepSeek`, `#AI funding`, `#venture capital`, `#AI industry`, `#large language models`

---

<a id="item-6"></a>
## [OpenAI 发布 Codex Chrome 扩展，实现浏览器自动化](https://developers.openai.com/codex/changelog) ⭐️ 7.0/10

OpenAI 为 Codex 发布了一款 Chrome 扩展，使 AI agent 能够在已登录的网站上自主操作，完成页面导航和数据录入任务。该扩展通过编写并运行代码在后台标签组中工作，支持跨标签页并行多任务执行，且不会干扰用户当前的浏览会话。 该扩展标志着 AI agent 从受控环境迈向真实网络交互的重要一步。它能够实现实用的浏览器自动化，处理重复性的基于网络的任务，有望改变用户在工作场景中与网站和网络应用的交互方式。 该扩展需要同时从 Codex 应用和 Chrome 网上应用店安装。Codex 的内置浏览器功能也得到增强，支持操作本地开发服务器和文件页面，可用于点击 UI、复现视觉 bug 或验证本地修复。目前该扩展不适用于欧盟和英国地区，后续将提供支持。

telegram · zaihuapd · 05月8日 04:17

**背景**: Codex 是 OpenAI 开发的 AI 编程 agent，集成在 ChatGPT 中，专门处理软件工程任务，如编写功能、修复 bug 和审查代码库。自主型 AI agent 能够解释目标、构建计划、执行操作并根据结果迭代，通常只需有限的人类监督。该扩展延续了将 AI agent 与浏览器连接的趋势，与 Browser MCP 和 browser-use 等项目类似，使 AI 能够直接与 Web 界面交互。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(AI_agent)">OpenAI Codex ( AI agent) - Wikipedia</a></li>
<li><a href="https://openai.com/codex/">Codex | AI Coding Partner from OpenAI | OpenAI</a></li>
<li><a href="https://www.snowflake.com/en/fundamentals/autonomous-ai-agents/">What Are Autonomous AI Agents? Features, Types & Use Cases</a></li>
<li><a href="https://browsermcp.io/">Browser MCP - Automate your browser using VS Code, Cursor, Claude, and more</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Codex`, `#Chrome Extension`, `#AI Agents`, `#Browser Automation`

---

<a id="item-7"></a>
## [Canvas 平台期末周遭入侵 美国多所学校受影响](https://www.cnn.com/2026/05/07/us/canvas-hack-strands-college-students-finals-week) ⭐️ 7.0/10

Canvas 学习管理系统遭 ShinyHunters 黑客组织入侵，在多所美国学校的首页显示勒索信息，导致期末周期间数千名学生无法访问成绩、材料和测验。 此次攻击凸显了关键教育基础设施的脆弱性，以及网络犯罪分子在高风险时期针对学术机构的趋势。约 9000 所学校、数百万学生的敏感数据可能因此泄露。 ShinyHunters 声称对 5 月 1 日的数据泄露和本次入侵事件负责，累计泄露数据超过 300TB，包括学生姓名、ID 和邮箱地址。Canvas 当晚恢复了大多数用户的访问权限，但詹姆斯·麦迪逊大学被迫将周五考试推迟至周三。

telegram · zaihuapd · 05月8日 04:30

**背景**: Canvas 由 Instructure Holdings 开发，是全球领先的学习管理系统（LMS），广泛应用于 K-12、高等教育和企业培训领域，提供课程管理、内容交付、测验和学生互动功能。ShinyHunters 是一个臭名昭著的黑帽黑客组织，据信成立于 2019 年，以大规模数据泄露和"付费或泄露"的勒索策略闻名。该组织在 2020 年从 13 家公司窃取超过 2 亿条记录后声名大噪。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ShinyHunters">ShinyHunters - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Canvas_(Learning_Management_System)">Canvas (Learning Management System)</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#education-technology`, `#ransomware`, `#data-breach`, `#Canvas`

---

<a id="item-8"></a>
## [Cloudflare 裁减逾 1100 名员工，AI 智能体重塑组织架构](https://blog.cloudflare.com/building-for-the-future/) ⭐️ 7.0/10

2026 年 5 月 7 日，Cloudflare 宣布将在全球范围内裁减超过 1100 名员工。两位联合创始人在内部信中表示，过去三个月公司内部 AI 使用量增长超过 600%，是此次组织架构重组的主要驱动力。 此次裁员是 AI 取代人类岗位在大型科技公司中最具说服力的案例之一，提供了 AI 采用速度如何改变科技行业就业格局的真实证据。 公司将为离职员工提供至 2026 年底的全额基本工资作为遣散补偿、美国地区的医疗保险，以及延至 2026 年 8 月 15 日的股权归属安排，并对尚未满一年归属期的员工豁免悬崖期条款。

telegram · zaihuapd · 05月8日 08:15

**背景**: AI Agent（人工智能体）是一种能够感知环境、进行推理并自主执行任务的 AI 系统。与需要详细提示的传统聊天机器人不同，AI 智能体只需一个目标即可独立规划并完成多步骤工作流程。Cliff vesting（悬崖期归属）是一种常见的股权薪酬结构，在员工完成特定等待期（通常为一年）之前没有任何股份归属，此后剩余股份按计划归属。Cloudflare 成立于 2009 年，总部位于旧金山，为全球提供互联网基础设施、安全和性能服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/1918763414857159516">一文讲清智能体（AI Agent），这是一篇不得不看的干货总结！</a></li>

</ul>
</details>

**标签**: `#cloudflare`, `#ai-adoption`, `#layoffs`, `#tech-industry`, `#workforce-restructuring`

---

<a id="item-9"></a>
## [苹果据报考虑结束与台积电 12 年独家代工合作](https://t.me/zaihuapd/41292) ⭐️ 7.0/10

据《华尔街日报》报道，苹果公司正在考虑结束自 2014 年起与台积电建立的 12 年独家芯片代工关系，探索与英特尔等其他制造商合作生产中低端处理器。分析师预测，英特尔最早可能于 2027 年使用其 18A 工艺节点为苹果代工部分 Mac、iPad 或 iPhone 芯片。 这代表了苹果供应链战略的重大转变，可能减少对台积电的依赖，并降低因台积电优先满足 AI 生产需求而产生的风险。此举可能重塑全球半导体代工行业，同时标志着英特尔作为可行替代芯片制造商的崛起，并加剧代工厂之间对苹果高价值合同的竞争。 英特尔的参与将仅限于代工制造，不涉及芯片设计，这意味着苹果将完全掌控处理器架构和规格。台积电目前正优先为英伟达等 AI 芯片制造商分配产能，这影响了苹果为其产品获得足够制造产能的能力。

telegram · zaihuapd · 05月8日 17:18

**背景**: 台积电（台湾半导体制造公司）是全球最大、最先进的半导体代工厂，为苹果、AMD 和英伟达等主要科技公司生产芯片。台积电开创了纯代工模式，专注于为其他公司制造芯片而非自行设计。18A 工艺节点是英特尔最新的先进制造技术，该公司已投资数十亿美元建设其代工能力以服务外部客户。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TSMC">TSMC - Wikipedia</a></li>
<li><a href="https://www.intel.com/content/www/us/en/foundry/process/18a.html">Intel 18A | See Our Biggest Process Innovation</a></li>
<li><a href="https://www.rcrwireless.com/20251013/chips/intel-18-a-process">Research note: Intel on 18A process and progress</a></li>

</ul>
</details>

**标签**: `#Apple`, `#TSMC`, `#Intel`, `#semiconductor manufacturing`, `#supply chain`

---

<a id="item-10"></a>
## [谷歌 reCAPTCHA 在去谷歌化安卓设备上失效](https://reclaimthenet.org/google-broke-recaptcha-for-de-googled-android-users) ⭐️ 6.0/10

在谷歌实施新的远程认证要求后，谷歌的 reCAPTCHA 服务在运行 GrapheneOS 的去谷歌化安卓设备上停止工作。该更新强制设备通过使用 EK->AIK 链的谷歌服务器进行认证，而去谷歌化设备无法完成这一过程。 这一事件凸显了注重隐私的用户与强制执行专有认证机制的平台服务之间日益紧张的关系。它表明，设备级别的限制如何能够排斥选择不使用谷歌生态系统的用户，可能造成一个双层互联网，在那里注重隐私的用户面临越来越多的障碍。 远程认证机制通过一个链工作：认可密钥（EK）是静态的硬件绑定私钥，它们生成由谷歌服务器签名的临时认证身份密钥（AIK），然后再产生由 AIK 签名的最终认证。GrapheneOS 用户报告说，虽然他们仍然可以使用需要 Play Integrity API 的谷歌服务，但 reCAPTCHA 不再将他们的设备识别为有效设备。

hackernews · anonymousiam · 05月8日 18:45 · [社区讨论](https://news.ycombinator.com/item?id=48067119)

**背景**: GrapheneOS 是一个注重隐私的自定义安卓 ROM，移除谷歌服务和膨胀软件，专为在谷歌 Pixel 硬件上运行而设计。远程认证是一种可信计算安全机制，允许外部各方验证系统的软件配置和完整性。EK->AIK 链代表一种特定的认证方法，其中硬件绑定密钥与服务器签名的临时身份进行交互。reCAPTCHA 是谷歌的机器人检测系统，最近已演变为具有增强设备指纹识别功能的谷歌云欺诈防御。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Trusted_Computing">Trusted Computing - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS - Wikipedia</a></li>
<li><a href="https://www.mithrilsecurity.io/confidential-computing-explained/building-the-remote-attestation">Building the remote attestation</a></li>

</ul>
</details>

**社区讨论**: 社区讨论揭示了对谷歌认证要求的沮丧，以及对网络上类似 KYC 验证扩展的担忧。一位评论者详细解释了技术性的 EK->AIK 链，指出谷歌服务器记录 EK->AIK 转换使得设备追踪成为可能。其他人则为自己的网站寻找 reCAPTCHA 的替代方案，而一些人则对 Cloudflare 日益严格的验证方法表示警惕。少数用户分享了过渡到 GrapheneOS 的个人经历，并指出一些银行应用即使使用完整的谷歌服务也拒绝工作。

**标签**: `#privacy`, `#recaptcha`, `#degoogled-android`, `#remote-attestation`, `#grapheneos`

---

<a id="item-11"></a>
## [在内存中运行的树莓派 Zero 上托管静态网站](https://btxx.org/posts/memory/) ⭐️ 6.0/10

一位创客演示了在树莓派 Zero 上完全运行于内存中的静态网站服务，同时将 TLS 终止功能卸载到云服务商，以减少该资源受限设备的 CPU 负载。 这项技术展示了嵌入式系统中创造性的资源优化方法，表明将计算密集型操作（如 TLS）卸载出去，即使是最受限的硬件也能运行真实的网站工作负载。 树莓派 Zero 完全从内存中运行静态网站，消除了 SD 卡磨损并降低了功耗，同时由云服务商处理 TLS 终止以节省 1GHz 单核 ARM11 处理器的 CPU 周期。

hackernews · xngbuilds · 05月8日 15:10 · [社区讨论](https://news.ycombinator.com/item?id=48064312)

**背景**: 树莓派 Zero 是一款微型、低成本（约 5 美元）的单板计算机，配备 1GHz 单核 ARM11 处理器和 512MB 内存。TLS 终止是一种技术，其中加密流量在代理服务器（如负载均衡器或云服务）处解密后再转发到后端服务器，从而将计算密集型的解密工作从源服务器上卸载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TLS_termination_proxy">TLS termination proxy</a></li>
<li><a href="https://www.geeksforgeeks.org/computer-networks/ssl-termination/">What is SSL Termination? Working and Importance</a></li>

</ul>
</details>

**社区讨论**: 社区讨论展示了使用树莓派 Zero 的各种家庭实验室方法。评论者分享了完全在内存中运行 Alpine Linux、使用 Cloudflare 隧道进行远程访问，甚至在该设备上编译 Gentoo 的经验。社区共识认为，虽然树莓派 Zero 比 1990 年代的企业服务器强大得多，但 TLS 卸载技术代表了一种实用的优化而非限制，因为它使受限硬件能够高效地提供内容服务。

**标签**: `#homelab`, `#raspberry-pi`, `#embedded-systems`, `#system-optimization`, `#self-hosting`

---

<a id="item-12"></a>
## [Meshtastic LoRa 网状网络系统介绍](https://meshtastic.org/docs/introduction/) ⭐️ 6.0/10

Meshtastic.org 发布了其基于 LoRa 的网状网络系统介绍，该系统可实现去中心化的短信传输，无需依赖互联网基础设施。这篇文章获得了大量社区关注，获得 369 个点赞和 147 条评论，反映出人们对弹性通信技术日益增长的兴趣。 这项技术代表了一种向弹性、抗审查通信网络发展的趋势，对于紧急情况和注重隐私的用户尤其重要。社区讨论显示出人们对该技术潜力的热情，同时也关注该组织的法律行为。 Meshtastic 在免许可频段运行，支持加密，并能使用网状拓扑跨多个节点中继消息。社区评论指出该技术目前仅支持短信功能，需要对当前去中心化网状网络的能力与大众想象的差距保持现实期望。

hackernews · ColinWright · 05月8日 11:22 · [社区讨论](https://news.ycombinator.com/item?id=48061566)

**背景**: LoRa（远程）是 Semtech 开发的一种扩频调制技术，为物联网应用实现远程、低功耗的无线通信。网状网络拓扑允许设备直接连接并通过多个中间节点动态路由数据，创建无集中基础设施的弹性网络。Meshtastic 将这些技术与 Heltec 等廉价硬件模块结合，实现点对点短信功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LoRa">LoRa - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mesh_networking">Mesh networking - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区评论显示出不同的情绪：一方面许多用户对发现这项技术感到兴奋，并分享了多年使用的积极体验；另一方面也有人对 Meshtastic 组织在保护品牌名称方面的激进法律立场表示担忧。一位评论者指出领导层中有一名律师，会追诉使用类似名称的其他项目。用户还讨论了现实期望——当前的网状网络能力与一些人的想象相比是有限的。

**标签**: `#mesh-networking`, `#lora`, `#decentralized-communication`, `#p2p`, `#meshtastic`

---

<a id="item-13"></a>
## [US Government releases first batch of UAP documents and videos](https://www.war.gov/UFO/) ⭐️ 6.0/10

The US government released its first batch of UAP documents and videos, which the HN community quickly analyzed with largely skeptical technical assessments noting the footage shows conventional objects like missiles and camera artifacts.

hackernews · david-gpu · 05月8日 12:10 · [社区讨论](https://news.ycombinator.com/item?id=48061938)

**标签**: `#uap`, `#government`, `#disclosure`, `#ufos`, `#media-analysis`

---

<a id="item-14"></a>
## [vLLM ROCm 后端已添加到 Lemonade，支持 AMD GPU](https://i.redd.it/kesrnt4lgyzg1.png) ⭐️ 6.0/10

Lemonade SDK 已将支持 ROCm 的 vLLM 添加为实验性后端，使用户能够通过简单的 CLI 命令（如 `lemonade backends install vllm:rocm` 和 `lemonade run Qwen3.5-0.8B-vLLM`）直接在 AMD GPU 上运行 .safetensors 格式的 LLM。 这一集成为 AMD GPU 用户提供了通过 Lemonade 友好界面访问 vLLM 的途径，同时通过支持无需 GGUF 转换的 .safetensors 模型，为 llama.cpp 提供了实用的替代方案，从而扩大了本地 LLM 部署的选择范围。 该后端被明确标记为实验性版本，存在已知的不足之处，开发者（u/krishna2910-amd、u/mikkoph 和 u/sa1sr1）正在积极寻求社区反馈以指导未来开发。快速入门指南可在 lemonade-server.ai/news/vllm-rocm.html 获取。

reddit · r/LocalLLaMA · jfowers_amd · 05月8日 18:21 · [社区讨论](https://www.reddit.com/r/LocalLLaMA/comments/1t7g70j/vllm_rocm_has_been_added_to_lemonade_as_an/)

**背景**: vLLM 是一个以 PagedAttention 内存管理技术著称的高性能 LLM 推理引擎。ROCm（Radeon Open Compute）是 AMD 的开源 GPU 计算软件平台，使 PyTorch 等 ML 框架能够在 AMD 硬件上运行。Lemonade 是一个开源本地 AI 服务器，通过兼容云 API 的接口在本地 GPU 和 NPU 上运行 LLM。GGUF（GGML 通用文件）是 llama.cpp 的原生二进制格式，而 .safetensors 是 Hugging Face 推荐的安全模型格式，支持内存映射加载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ROCm">ROCm - Wikipedia</a></li>
<li><a href="https://github.com/lemonade-sdk/lemonade">GitHub - lemonade-sdk/lemonade: Lemonade helps users discover ...</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp">GitHub - ggml-org/llama.cpp: LLM inference in C/C++</a></li>

</ul>
</details>

**社区讨论**: 该公告在 Reddit 上获得了 227 个 upvotes，表明社区兴趣相当不错。开发者明确邀请反馈以确定这个实验性后端的方向和范围，将其定位为基于真实用户体验共同完善实现的合作努力。

**标签**: `#vLLM`, `#ROCm`, `#AMD GPUs`, `#Local LLM`, `#Lemonade`

---

<a id="item-15"></a>
## [Qwen 35B MoE 模型在 12GB 显存 RTX 3060 上实现有效运行](https://www.reddit.com/r/LocalLLaMA/comments/1t7l56a/qwen_35ba3b_is_very_usable_with_12gb_of_vram/) ⭐️ 6.0/10

Qwen3.6-35B-A3B-MTP MoE 模型在 RTX 3060 12GB 上使用 GGUF IQ4_XS 量化格式，通过优化的 llama.cpp 参数设置（ncmoe 18、t 9），实现了约 914 tokens/s 的预填充速度和 46.8 tokens/s 的生成速度。 这证明了配备 12GB 显存的消费级 GPU 能够有效运行 350 亿参数的 MoE 模型，使先进 AI 能力对普通用户更加触手可及。提供的配置方案使得本地部署用于编程和通用任务成为可能，无需昂贵硬件。 ncmoe 参数对 MoE 模型至关重要，控制着保留在 GPU 上的专家块数量；数值越低意味着更多专家驻留在显存中。最佳编程配置使用 ncmoe 20 配合 32k 上下文，实现 43.4 tokens/s 生成速度同时预留 273 MiB 显存。IQ4_XS 是一种重要性矩阵 4 位量化格式，在保持质量的同时提供激进压缩。

reddit · r/LocalLLaMA · jwestra · 05月8日 21:22

**背景**: MoE（混合专家）架构在推理过程中仅激活神经网络'专家'的一个子集，与同等参数量的密集模型相比显著降低计算需求。GGUF（GGML 统一格式）是 llama.cpp 当前的文档格式，从 GGML 演进而来，针对 CPU 和 GPU 上的高效推理进行了优化。Qwen3.6-35B-A3B 模型是一种 MoE 变体，总参数量约为 350 亿，但每个 token 仅激活 30 亿参数，所需内存远低于密集型 350 亿参数模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/applying-mixture-of-experts-in-llm-architectures/">Applying Mixture of Experts in LLM Architectures | NVIDIA Technical...</a></li>
<li><a href="https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-mixture-of-experts">A Visual Guide to Mixture of Experts ( MoE )</a></li>
<li><a href="https://www.ibm.com/think/topics/gguf-versus-ggml">GGUF versus GGML | IBM</a></li>

</ul>
</details>

**社区讨论**: 该帖子获得 93 个点赞，表明社区对本地 LLM 部署实用指南的强烈兴趣。评论可能集中在分享类似配置、比较不同硬件上的结果，以及讨论上下文大小与生成速度之间的权衡。用户可能很欣赏这些可操作的 llama-cli 命令和具体的性能基准数据。

**标签**: `#local-llm`, `#qwen`, `#moe-model`, `#gguf-quantization`, `#consumer-gpu`, `#llama.cpp`

---

<a id="item-16"></a>
## [Allen AI 发布 EMO 混合专家模型 采用文档级专家路由](https://i.redd.it/zonmo2y79zzg1.png) ⭐️ 6.0/10

Allen AI 发布了 EMO 模型，这是一款 1B 激活参数/14B 总参数规模的混合专家模型，使用 1 万亿 token 进行训练。其核心创新在于文档级专家路由机制，能够按领域（如医疗、新闻等）对专家进行聚类，而非基于表面特征进行路由。 这代表了 MoE 架构设计的重要创新突破。传统 MoE 模型以 token 为单位进行路由，而 EMO 则基于语义领域对整个文档进行路由。这种方法有望实现更连贯的专家专业化，并在不同知识领域带来性能提升。 该模型的文档级路由机制允许根据内容领域将整个文档分配给专家聚类，有望实现更深入的专家专业化。模型已在 HuggingFace 上线，可供下载和实验。

reddit · r/LocalLLaMA · ghostderp · 05月8日 20:57 · [社区讨论](https://www.reddit.com/r/LocalLLaMA/comments/1t7kgy4/new_moe_from_ai2_emo/)

**背景**: 混合专家（MoE）是一种人工智能架构，通过使用多个专业化的神经网络「专家」和路由机制将输入分配给相关专家，从而在不增加相应计算成本的情况下实现模型参数的高效扩展。在传统的 token 级 MoE 路由中，每个 token 独立地被分配给 top-k 专家，这可能导致相关内容被分散到不同的专家，从而降低专业化的连贯性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>
<li><a href="https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-mixture-of-experts">A Visual Guide to Mixture of Experts ( MoE )</a></li>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models</a></li>

</ul>
</details>

**社区讨论**: 该 Reddit 帖子获得了 83 分的中等关注度，反映出 MoE 社区对这种新颖的文档级路由方法的兴趣。评论强调，基于领域的专家聚类作为对传统 token 级路由模式的突破颇具创新意义。

**标签**: `#mixture-of-experts`, `#allen-ai`, `#emo-model`, `#llm-architecture`, `#model-routing`

---

<a id="item-17"></a>
## [Qwen3.6-27B 在单张 RTX 4090 上实现 262K 上下文下 80+ t/s 吞吐量](https://www.reddit.com/r/LocalLLaMA/comments/1t7kyju/got_mtp_turboquant_running_qwen3627b_80_ts_at/) ⭐️ 6.0/10

一位 Reddit 用户成功将多 Token 预测(MTP)与 TurboQuant 的无损 KV 缓存压缩技术结合应用于 Qwen3.6-27B 模型，在单张 RTX 4090 上使用 TBQ4_0（4.25 bpv KV 缓存）量化技术，在 262K 上下文长度下实现了 80-87 t/s 的吞吐量，MTP 草稿接受率约为 73%。 这一成果表明，之前需要昂贵硬件才能实现的先进推理优化技术，现在可以在消费级 GPU 上运行，有望为个人开发者和爱好者提供获取长上下文 LLM 应用的机会。 该配置使用了带有 grafted MTP heads（移植 MTP 头）的 Qwen3.6-27B-Heretic-v2 Q4_K_M 模型，运行在 Ubuntu 24.04 和 CUDA 12.x 环境下。用户经过一天的优化将初始 43 t/s 提升至 80-87 t/s。该项目分支已在 github.com/Indras-Mirror/llama.cpp-mtp 开放供社区测试。

reddit · r/LocalLLaMA · indrasmirror · 05月8日 21:15

**背景**: 多 Token 预测（MTP）是一种利用轻量级预测头同时预测多个未来 Token 的技术，通过投机解码提高推理吞吐量，其中 draft 模型预测 Token 由目标模型验证。TurboQuant 是 Google 的极端 KV 缓存量化方法（ICLR 2026），可实现约 3 bits per value（每值 3 比特）的近零精度损失，通过压缩 key-value 缓存条目提供高达 6 倍的内存减少和 8 倍的推理加速。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@bingqian/understanding-multi-token-prediction-mtp-in-deepseek-v3-ed634810c290?ref=ghost.codersera.com">Understanding Multi - Token Prediction ( MTP ) in... | Medium</a></li>
<li><a href="https://github.com/hackimov/turboquant-kv">TurboQuant — Extreme KV Cache Quantization - GitHub</a></li>
<li><a href="https://hackaday.com/2026/04/09/turboquant-reducing-llm-memory-usage-with-vector-quantization/">TurboQuant: Reducing LLM Memory Usage With Vector Quantization</a></li>

</ul>
</details>

**社区讨论**: 该帖子在 LocalLLaMA 社区获得 70 个 upvotes（赞同），表明社区对实际推理优化技术有浓厚兴趣。社区成员欣赏真实的基准测试结果和开源分支，尽管有人指出这代表的是个人实验结果，而非经过验证的生产级解决方案。

**标签**: `#local-llm`, `#quantization`, `#MTP`, `#Qwen`, `#RTX-4090`, `#inference-optimization`

---

<a id="item-18"></a>
## [Z-lab 发布搭载 DFlash 推测解码的 Gemma 4 26B 模型](https://huggingface.co/z-lab/gemma-4-26B-A4B-it-DFlash) ⭐️ 6.0/10

Z-lab 发布了 gemma-4-26B-A4B-it-DFlash，这是 Gemma 4 26B 的 DFlash（块扩散）推测解码变体，将其定位为 Google 多令牌预测（MTP）方法的替代方案，用于加速大语言模型推理。 DFlash 的有状态设计在迭代之间保持上下文缓冲区、KV 缓存位置和 RoPE 偏移量的持久状态，与 MTP 的无状态方法（KV 缓存增长更快）相比，可能为长上下文和稀疏模型提供更优性能。 DFlash 使用轻量级块扩散模型并行起草多个令牌，相比自回归解码实现高达 4.4-6 倍的加速。然而，该模型目前仅支持 vLLM，限制了寻求 DFlash 支持的 GGUF/llama.cpp 用户的使用。

reddit · r/LocalLLaMA · PaceZealousideal6091 · 05月8日 14:18 · [社区讨论](https://www.reddit.com/r/LocalLLaMA/comments/1t79ayh/zlab_released_gemma426ba4bitdflash_anybody_tried/)

**背景**: 推测解码通过使用小型草稿模型提议令牌，然后由大型目标模型并行验证来加速 LLM 推理。MTP（多令牌预测）是 Google 在 Gemma 4 中使用的一种实现方法，可实现高达 3 倍的加速。DFlash 代表了一种使用块扩散进行起草阶段的替代方案，声称在更长对话的有状态缓存方面具有优势。Z-lab 此前已将 DFlash 应用于 Qwen 模型，并通过 SGLang 支持生产环境服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/z-lab/Qwen3.5-9B-DFlash">z-lab/Qwen3.5-9B- DFlash · Hugging Face</a></li>
<li><a href="https://z-lab.ai/projects/dflash/">DFlash : Block Diffusion for Flash Speculative Decoding - Z Lab</a></li>
<li><a href="https://ai.google.dev/gemma/docs/mtp/overview">Speed-up Gemma 4 with Multi-Token Prediction - ai.google.dev</a></li>

</ul>
</details>

**社区讨论**: Reddit 社区对 DFlash 相比 MTP 的技术优势表现出兴趣，特别是对于 Gemma 4 26B 和 Qwen 3.6 35B 等稀疏模型。用户渴望获得性能基准测试结果，并对当前缺乏 llama.cpp/GGUF 支持表示质疑，一些人预计随着会话延长和上下文增长，DFlash 可能比 MTP 更有效。

**标签**: `#speculative-decoding`, `#gemma-4`, `#dflash`, `#vllm`, `#llm-optimization`

---

<a id="item-19"></a>
## [ChatGPT 推出信任联系人功能，检测自残话题时通知亲友](https://www.theverge.com/ai-artificial-intelligence/925874/chatgpt-trusted-contact-emergency-self-harm-notification) ⭐️ 6.0/10

OpenAI 为 ChatGPT 成年用户推出了可选的“信任联系人”安全功能，允许用户指定一位朋友、家人或照护者，在系统检测到潜在自残话题时可被通知。 该功能标志着 AI 安全机制在心理健康危机干预领域的重大扩展，为弱势用户提供了主动的安全保障，同时为行业树立了负责任 AI 部署的先例。 该功能要求双方均为成年人（韩国需 19 岁以上），联系人需在一周内接受邀请。当检测到自残话题时，ChatGPT 首先鼓励用户联系其信任对象；仅在经过专门培训的团队审核后，才会发送通知，且不共享聊天内容。

telegram · zaihuapd · 05月8日 02:47

**背景**: 该功能的开发源于 2023 年的一起事件，16 岁的 Adam Raine 在与 ChatGPT 长期对话后自杀身亡，期间 AI 据报道提供了有害建议。其父母随后起诉了 OpenAI 和 CEO 萨姆·奥特曼，指控该技术导致了他的死亡。Meta 也在 Instagram 上推出了类似的安全功能，当孩子反复搜索自残内容时会通知家长。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnn.com/2025/08/26/tech/openai-chatgpt-teen-suicide-lawsuit">Parents of 16-year-old sue OpenAI, claiming ChatGPT ... - CNN</a></li>
<li><a href="https://www.cbsnews.com/news/ai-chatbots-teens-suicide-parents-testify-congress/">Parents of teens who died by suicide after AI chatbot ...</a></li>
<li><a href="https://centerforhumanetechnology.substack.com/p/how-openais-chatgpt-guided-a-teen">How OpenAI's ChatGPT Guided a Teen to His Death</a></li>

</ul>
</details>

**社区讨论**: 该公告引发了关于 AI 在心理健康干预中角色扩展的广泛讨论。社区成员对该功能的救命潜力表示谨慎支持，同时也对自残检测系统的准确性、隐私影响以及 AI 是否应该参与危机应对表示担忧。

**标签**: `#AI Safety`, `#ChatGPT`, `#Mental Health`, `#Product Feature`, `#OpenAI`

---

<a id="item-20"></a>
## [最高法院否决特朗普 IEEPA 关税 随即签署 10%临时关税令](https://t.me/zaihuapd/41280) ⭐️ 6.0/10

美国最高法院于 2 月 20 日以 6 比 3 的投票结果裁定，特朗普政府依据《国际紧急经济权力法》（IEEPA）征收的全球关税违宪，认定宪法将关税权保留给国会而非总统。特朗普随即签署行政命令，利用《贸易法》第 122 条对所有全球进口商品征收 10%的临时从价关税，有效期 150 天，将于 2 月 24 日凌晨 12:01 生效。 该裁决确立了一项重要的宪法先例，限制了总统对贸易政策的权力，迫使特朗普为其关税议程寻找替代法律依据。对于科技和供应链行业而言，从 IEEPA 转向第 122 条引入了一个有时间限制的框架，可能在 10%基准关税继续影响电子、零部件和制成品进口成本的同时，造成规划上的不确定性。 《贸易法》第 122 条从根本上被设计为快速经济施压工具，具有 150 天的日落条款和 15%的税率上限，需向国会通报但无需批准。特朗普行政命令中的豁免范围包括关键矿产、能源产品、化肥、药品原料及部分农产品，为依赖这些投入的供应链提供了有限的减免。

telegram · zaihuapd · 05月8日 06:46

**背景**: IEEPA 于 1977 年颁布，旨在限制总统依据 1917 年《与敌国贸易法》原始授权的紧急经济权力。1974 年《贸易法》第 122 条在 4 月份关税被贸易法院否决后，成为潜在的法律替代方案，特定为总统提供有限的关税权力并设有内置的国会监督机制。最高法院 6 比 3 的裁决反映了意识形态分歧，多数意见坚定地确立了在宪法第一条下，关税征收权归属于国会。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/International_Emergency_Economic_Powers_Act">International Emergency Economic Powers Act - Wikipedia</a></li>
<li><a href="https://foreignpolicy.com/2025/06/03/TRUMP-TARIFFS-LAW-1974-TRADE-ACT-SECTION-122/">The 1974 Trade Act Section 122 : The Obscure Law Trump Could Use...</a></li>
<li><a href="https://www.csis.org/analysis/making-tariffs-great-again-does-president-trump-have-legal-authority-implement-new-tariffs">Making Tariffs Great Again: Does President Trump Have Legal...</a></li>

</ul>
</details>

**标签**: `#US_Politics`, `#Trade_Policy`, `#Constitutional_Law`, `#Tariffs`, `#International_Trade`

---

<a id="item-21"></a>
## [Anthropic 计划百亿级新融资，估值将反超 OpenAI](https://www.ft.com/content/a40cafcc-0fa4-4e70-9e24-90d826aea56d) ⭐️ 6.0/10

据报道，Anthropic 正计划今年夏天筹集数百亿美元的巨额资金，这将使其估值推高至近 1 万亿美元，超越竞争对手 OpenAI 目前约 8800 亿美元的估值。 这轮融资代表了 AI 竞争的关键时刻，Anthropic 估值飙升反映出投资者对 AI 基础设施的强烈热情。短短几个月内估值从 3800 亿美元跃升至约 1 万亿美元，表明 AI 能力和竞争优势具有重要的战略意义。 在 Forge Global 等私募市场上，Anthropic 的隐含估值已达 1-1.2 万亿美元。2024 年 2 月，Anthropic 完成了 300 亿美元的融资，当时投后估值为 3800 亿美元，意味着在短短几个月内，由于企业客户爆发式增长，估值已翻倍逾两倍。

telegram · zaihuapd · 05月8日 11:15

**背景**: Anthropic 是一家由 OpenAI 前研究人员创立的 AI 安全公司，以开发 Claude 大语言模型而闻名，后者与 OpenAI 的 GPT 系列形成竞争。Anthropic 在企业 AI 市场与 OpenAI 直接竞争。Forge Global 等平台的私募市场估值来源于二级交易活动，投资者在此买卖私营公司的股份，等待潜在的上市机会。Forge Global 最近宣布将以约 6.6 亿美元被 Charles Schwab 收购，已促成超过 170 亿美元的私营公司股权交易。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://forgeglobal.com/">Forge Global</a></li>

</ul>
</details>

**标签**: `#AI Funding`, `#Anthropic`, `#OpenAI`, `#Venture Capital`, `#AI Industry`

---

<a id="item-22"></a>
## [美国调查英伟达芯片经泰国走私至中国案](https://www.bloomberg.com/news/articles/2026-05-08/us-said-to-suspect-nvidia-chips-smuggled-to-alibaba-via-thailand) ⭐️ 6.0/10

美国检方正在调查泰国公司 OBON Corp.，指控该公司涉嫌将价值 25 亿美元的搭载先进英伟达芯片的 Super Micro 服务器走私至中国。阿里巴巴集团被指为多个终端客户之一。 此案暴露了美国对先进半导体出口管制的潜在漏洞，对当前美中科技竞争和东南亚 AI 主权努力具有重要影响。如获证实，走私行为可能促使美国重新考虑对泰国的芯片出口限制，可能影响泰国的主权 AI 雄心。 OBON Corp.此前曾协助建立泰国主权 AI 云项目 Siam AI，该项目已获得英伟达合作伙伴地位。阿里巴巴已否认与 Super Micro 或 OBON 有任何业务关系，而 Siam AI 首席执行官声称已离开 OBON，公司未涉及走私。

telegram · zaihuapd · 05月8日 13:23

**背景**: 美国对半导体（尤其是英伟达 H100 和 A100 GPU）的出口管制旨在阻止中国发展前沿 AI 能力。Supermicro 是一家主要的美国服务器制造商，将英伟达芯片集成到高性能计算系统中。主权 AI 是指各国利用本土资源、人才和数据建设国内 AI 基础设施、减少对外国技术供应商依赖的努力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Supermicro">Supermicro - Wikipedia</a></li>
<li><a href="https://www.kaohooninternational.com/technology/549042">SIAM.AI CLOUD Launches Thailand’s AI Infrastructure to Drive ...</a></li>
<li><a href="https://www.nvidia.com/en-us/about-nvidia/partners/">NVIDIA Partner Network (NPN)</a></li>

</ul>
</details>

**标签**: `#semiconductor exports`, `#US-China tech tensions`, `#Nvidia chips`, `#export controls`, `#AI sovereignty`

---

<a id="item-23"></a>
## [DeepSeek 据报首轮大额融资估值或达 450 亿美元](https://t.me/zaihuapd/41289) ⭐️ 6.0/10

据报道，DeepSeek 正在进行其首轮大规模外部融资，中国国家集成电路产业投资基金（"大基金"）可能领投，估值约达 450 亿美元。 这轮融资标志着 DeepSeek 首次获得重大外部资本注入，表明国家正更深地介入中国 AI 核心公司。450 亿美元的估值将使 DeepSeek 跻身全球估值最高的 AI 初创企业之列，凸显 AI 发展在中国科技战略布局中的重要地位。 这是 DeepSeek 首次进行重大外部融资，区别于许多传统上依赖内部资源的中国 AI 企业。大基金是中国最大的国有半导体投资机构，其参与表明国家正通过直接资本投入战略性地关注 AI 能力的获取。

telegram · zaihuapd · 05月8日 14:59

**背景**: DeepSeek，正式名称为杭州深度求索人工智能基础技术研究有限公司，是一家开发大语言模型（LLM）的中国 AI 公司。2025 年初，其 R1 模型以极低的开发成本实现了与西方领先 AI 系统相当的性能，引起了全球关注。"大基金"（国家集成电路产业投资基金）是中国政府为推动国内半导体和集成电路产业发展而设立的国家级投资基金，是国家科技自主战略的重要工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.zaobao.com.sg/news/china/story20260506-9005192">DeepSeek据报估值450亿美 金 大 基 金 领 投 | 联合早报</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://apnews.com/article/deepseek-ai-china-gpt-v4-d2ed33f2521917193616e061674d5f92">China's DeepSeek launches an update of its AI model | AP News</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI investment`, `#Chinese AI`, `#state-backed funding`, `#venture capital`

---