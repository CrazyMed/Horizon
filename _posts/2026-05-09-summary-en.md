---
layout: default
title: "Horizon Daily: 2026-05-09"
date: 2026-05-09
lang: en
---

> From 42 items, 23 important content pieces were selected

---

1. [Modular AI Releases Mojo 1.0 Beta](#item-1) ⭐️ 8.0/10
2. [Gemma 4 26B Achieves 578 tok/s on RTX 5090 via DFlash Speculative Decoding](#item-2) ⭐️ 8.0/10
3. [AI Reshaping Vulnerability Disclosure Culture](#item-3) ⭐️ 7.0/10
4. [HTML Artifacts Outperform Markdown for AI Code Output](#item-4) ⭐️ 7.0/10
5. [DeepSeek Seeks Record $7.35B Funding, V4.1 Launch in June](#item-5) ⭐️ 7.0/10
6. [OpenAI Releases Codex Chrome Extension for Browser Automation](#item-6) ⭐️ 7.0/10
7. [Canvas Hacked During US Schools Finals Week](#item-7) ⭐️ 7.0/10
8. [Cloudflare Lays Off 1,100+ Staff as AI Agents Reshape Workforce](#item-8) ⭐️ 7.0/10
9. [Apple Reportedly Ending TSMC Exclusive Partnership After 12 Years](#item-9) ⭐️ 7.0/10
10. [Google reCAPTCHA Breaks on De-googled Android Devices](#item-10) ⭐️ 6.0/10
11. [Serving Static Website on Raspberry Pi Zero Running in RAM](#item-11) ⭐️ 6.0/10
12. [Introduction to Meshtastic LoRa Mesh Networking System](#item-12) ⭐️ 6.0/10
13. [US Government releases first batch of UAP documents and videos](#item-13) ⭐️ 6.0/10
14. [vLLM ROCm Backend Added to Lemonade for AMD GPUs](#item-14) ⭐️ 6.0/10
15. [Qwen 35B MoE Runs Effectively on 12GB VRAM RTX 3060](#item-15) ⭐️ 6.0/10
16. [Allen AI Releases EMO MoE Model with Document-Level Expert Routing](#item-16) ⭐️ 6.0/10
17. [Qwen3.6-27B Achieves 80+ t/s at 262K Context on Single RTX 4090](#item-17) ⭐️ 6.0/10
18. [Z-lab Releases Gemma 4 26B with DFlash Speculative Decoding](#item-18) ⭐️ 6.0/10
19. [ChatGPT Launches Trusted Contact Feature for Self-Harm Detection](#item-19) ⭐️ 6.0/10
20. [Supreme Court Strikes Down Trump IEEPA Tariffs; Trump Signs 10% Temporary Tariffs](#item-20) ⭐️ 6.0/10
21. [Anthropic Plans $10B+ Funding Round, Valuation to Surpass OpenAI](#item-21) ⭐️ 6.0/10
22. [US Probes Alleged Smuggling of Nvidia Chips to China via Thailand](#item-22) ⭐️ 6.0/10
23. [DeepSeek Reportedly Seeks $45B Valuation in First Major Funding Round](#item-23) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Modular AI Releases Mojo 1.0 Beta](https://mojolang.org/) ⭐️ 8.0/10

Modular AI has released Mojo 1.0 Beta, marking a major milestone for the Python-compatible systems programming language designed for ML/AI workloads. The release was developed by Chris Lattner's team at the AI infrastructure company, which recently raised $250 million at a $1.6 billion valuation. Mojo aims to solve the long-standing problem of combining Python's accessibility with C++/Rust-level performance, potentially revolutionizing how developers write high-performance AI kernels. If successful, it could replace fragmented solutions like Numba and Triton while enabling unified CPU-GPU programming in a single language. Mojo implements an ownership model similar to Rust, features "comptime" that is more powerful than Zig, and includes first-class SIMD support. Notably, it is not merely an LLVM wrapper—while LLVM is involved, Mojo uses it differently than Rust or Zig. The language's open-source release is planned for Fall 2026.

hackernews · sbt567 · May 8, 02:49 · [Discussion](https://news.ycombinator.com/item?id=48057901)

**Background**: Mojo was created by Modular AI, an AI infrastructure company founded in 2017 by Chris Lattner, who previously created LLVM, Clang, and Swift. The language is proprietary and currently available for Linux and macOS. Mojo aims to fill the performance gap in Python for AI workloads while maintaining Python compatibility for accessibility. The ML/AI field currently uses various approaches for performance acceleration, including CUDA (NVIDIA-specific), Numba (Python JIT compiler), and Julia (high-performance numerical computing language).

<details><summary>References</summary>
<ul>
<li><a href="https://mojolang.org/">Mojo</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mojo_(programming_language)">Mojo (programming language) - Wikipedia</a></li>
<li><a href="https://www.modular.com/company/about">Modular: About Us</a></li>

</ul>
</details>

**Discussion**: Community response is mixed but generally optimistic. Supporters praise Mojo's ownership model, comptime features, and its novel non-LLVM-wrapper compilation approach as revolutionary for systems programming. However, skeptics raise concerns about changes from standard Python behavior (such as string indexing not working as expected), potential correctness issues, and whether it truly solves a problem that Julia plus Numba/Triton hasn't already addressed. Some developers also express frustration about the closed-source nature of the language.

**Tags**: `#mojo`, `#programming-languages`, `#machine-learning`, `#python`, `#systems-programming`

---

<a id="item-2"></a>
## [Gemma 4 26B Achieves 578 tok/s on RTX 5090 via DFlash Speculative Decoding](https://www.reddit.com/r/LocalLLaMA/comments/1t796qe/gemma_4_26b_hits_600_toks_on_one_rtx_5090/) ⭐️ 8.0/10

A benchmark test using DFlash speculative decoding on vLLM 0.19.2rc1 achieved approximately 578 output tokens per second for the Gemma 4 26B model on a single RTX 5090, representing a 2.56x speedup over the 228 tok/s baseline. The optimal configuration used num_speculative_tokens=13 with max_num_batched_tokens=8192, reducing mean end-to-end latency from 4455ms to 1738ms. This benchmark demonstrates that DFlash speculative decoding can dramatically accelerate local LLM inference without sacrificing output quality, making large models like Gemma 4 26B more practical for consumer-grade hardware. The findings provide actionable configuration guidance for developers optimizing inference pipelines on next-generation GPUs like the RTX 5090. The benchmark explored 15 different parameter settings for num_speculative_tokens (0-15), revealing that the optimal value depends on latency metrics: num_speculative_tokens=13 with max_num_batched_tokens=4096 offered slightly better mean latency but worse p95 latency, while increasing batched tokens to 8192 provided cleaner tail latency. The test workload used 256 input tokens and 1024 output tokens at concurrency 1.

reddit · r/LocalLLaMA · chain-77 · May 8, 14:13

**Background**: DFlash (Block Diffusion for Flash Speculative Decoding) is a lightweight block diffusion model designed for speculative decoding, enabling efficient parallel drafting by confining diffusion models to the drafting stage. Speculative decoding uses a draft-verify paradigm where a smaller, faster draft model proposes tokens that a larger target model then verifies in parallel. AWQ (Activation-aware Weight Quantization) is a 4-bit quantization technique that compresses models like Gemma 4 26B to 4-bit weight format (AWQ-4bit) for reduced memory footprint and faster inference while maintaining quality. vLLM is an open-source inference serving framework that implements PagedAttention for efficient KV cache management.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/z-lab/dflash">GitHub - z-lab/dflash: DFlash: Block Diffusion for Flash Speculative Decoding · GitHub</a></li>
<li><a href="https://arxiv.org/abs/2602.06036">[2602.06036] DFlash: Block Diffusion for Flash Speculative Decoding</a></li>
<li><a href="https://arxiv.org/abs/2306.00978">[2306.00978] AWQ: Activation-aware Weight Quantization for LLM Compression and Acceleration</a></li>
<li><a href="https://research.google/blog/looking-back-at-speculative-decoding/">Looking back at speculative decoding - Google Research</a></li>

</ul>
</details>

**Discussion**: The Reddit post generated strong engagement with a score of 99, indicating significant community validation. Readers expressed interest in comparing results across different hardware (especially RTX 4090) and other model families like Qwen. The author's observation that mean latency optimization doesn't automatically optimize tail latency resonated with the community, highlighting the importance of considering both metrics when tuning speculative decoding parameters.

**Tags**: `#llm-inference`, `#speculative-decoding`, `#vllm`, `#rtx-5090`, `#performance-optimization`

---

<a id="item-3"></a>
## [AI Reshaping Vulnerability Disclosure Culture](https://www.jefftk.com/p/ai-is-breaking-two-vulnerability-cultures) ⭐️ 7.0/10

Security experts are debating whether AI fundamentally transforms vulnerability research and disclosure timelines, with Log4Shell emerging as a critical case study demonstrating how quickly attacks can weaponize patches. If AI dramatically compresses the window between patch availability and exploit weaponization, traditional coordinated vulnerability disclosure models become less viable, potentially forcing fundamental changes to how the security community handles zero-day vulnerabilities. The Log4Shell timeline illustrates this compression: Alibaba discovered the vulnerability and reported it to Apache, a patch was pushed to git, and black hats began exploiting it before public disclosure, with attacks circulating in Minecraft communities within hours.

hackernews · speckx · May 8, 17:55 · [Discussion](https://news.ycombinator.com/item?id=48066524)

**Background**: Log4Shell (CVE-2021-44228) was a critical remote code execution vulnerability in Apache Log4j 2, a widely-used Java logging library affecting hundreds of millions of devices. Coordinated vulnerability disclosure (CVD) is a model where researchers notify vendors privately, allowing time to develop and deploy patches before public disclosure. This grace period traditionally ranges from days to months, assuming defenders need lead time to update systems.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Log4Shell">Log4Shell - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Coordinated_vulnerability_disclosure">Coordinated vulnerability disclosure</a></li>

</ul>
</details>

**Discussion**: The community is sharply divided: tptacek argues this shift was inevitable due to increased software transparency (open source adoption, improved decompilation tools) rather than AI specifically. freeqaz provided a detailed timeline of the Log4Shell race showing how rapidly attackers moved. rikafurude21 countered that this is merely an old problem (diffing kernel commits for security fixes) being reframed as an AI issue, arguing that faster exploit generation makes coordinated disclosure MORE important, not less, since organizations already patch at vastly different speeds.

**Tags**: `#vulnerability-disclosure`, `#AI-security`, `#open-source-security`, `#coordinated-disclosure`, `#exploit-research`

---

<a id="item-4"></a>
## [HTML Artifacts Outperform Markdown for AI Code Output](https://simonwillison.net/2026/May/8/unreasonable-effectiveness-of-html/#atom-everything) ⭐️ 7.0/10

Simon Willison published a practical guide highlighting Thariq Shihipar's insight that requesting HTML artifacts from Claude Code produces richer, more interactive outputs than Markdown. The technique enables AI to generate explanations with SVG diagrams, interactive widgets, and in-page navigation for tasks like PR reviews and security exploit analysis. 对于使用AI编码助手的开发者来说，这一转变很重要，因为HTML工件可以显著提高对复杂代码、安全漏洞和流系统逻辑的理解。随着现代模型拥有更高的token限制，历史上Markdown的token效率论点不再适用，使HTML成为教育和审查输出的更好选择。 Willison demonstrates the technique by having GPT-5.5 generate an HTML explanation of the Linux privilege escalation exploit from copy.fail, complete with dark-themed styling, safety warnings, and detailed step-by-step breakdowns. The Claude Code team has curated a collection of HTML effectiveness cases at thariqs.github.io/html-effectiveness showing various use cases.

rss · Simon Willison · May 8, 21:00

**Background**: Claude Artifacts is a feature that renders AI outputs as live, interactive elements in a separate panel rather than static text in the chat window. Artifacts can include React components, HTML pages, SVGs, and data visualizations. Since the GPT-4 era, many developers defaulted to requesting Markdown output due to its token efficiency compared to HTML, but this was a constraint born from the 8,192 token context window limit.

<details><summary>References</summary>
<ul>
<li><a href="https://ainskills.com/claude-artifacts-explained/">Claude Artifacts Explained - The Feature That Changes How You Use...</a></li>
<li><a href="https://www.c-sharpcorner.com/article/what-is-backpressure-in-streaming-systems-and-how-to-handle-it/">What Is Backpressure in Streaming Systems and How to Handle It?</a></li>
<li><a href="https://albato.com/blog/publications/how-to-use-claude-artifacts-guide">Claude Artifacts : What They Are & How to Use Them (2026 Guide)</a></li>

</ul>
</details>

**Discussion**: Simon Willison expresses enthusiasm about experimenting more with rich HTML explanations in response to ad-hoc prompts, noting that his previous December 2025 article on HTML tools focused mainly on interactive utilities. The community appears receptive to reconsidering HTML as the default output format, especially as AI models' token limits have expanded significantly.

**Tags**: `#AI coding tools`, `#Claude Code`, `#HTML artifacts`, `#Prompt engineering`, `#Developer productivity`

---

<a id="item-5"></a>
## [DeepSeek Seeks Record $7.35B Funding, V4.1 Launch in June](https://www.reddit.com/r/LocalLLaMA/comments/1t7bfpw/reports_suggest_deepseek_is_seeking_735_billion/) ⭐️ 7.0/10

DeepSeek is reportedly seeking up to RMB 50 billion ($7.35 billion) in its first funding round, which would mark the largest single fundraising round in Chinese AI history. The company also plans to accelerate its model release cadence, with V4.1 scheduled for launch in June, as part of its push toward commercialization and profitability. This funding round signals DeepSeek's transition from a research-focused startup to a commercially-driven AI powerhouse, potentially reshaping the competitive landscape of the global AI industry. If successful, it would validate investor confidence in Chinese AI innovation despite ongoing semiconductor export restrictions. CEO Liang Wenfeng plans to contribute the maximum allowable amount in this funding round, demonstrating strong insider confidence. The financing is prompting DeepSeek to align its release cadence with mainstream industry practices, moving away from its previously slower iteration approach. The report originates from unnamed sources cited by The Information and remains unverified.

reddit · r/LocalLLaMA · External_Mood4719 · May 8, 15:34

**Background**: DeepSeek was founded in July 2023 by Liang Wenfeng, co-founder of High-Flyer, a Chinese hedge fund that owns and funds the company. The company gained global attention in January 2025 with the release of DeepSeek-R1, a reasoning model reportedly trained for just $6 million—compared to GPT-4's $100 million training cost—using techniques like mixture of experts (MoE) layers and weaker export-restricted chips. DeepSeek's open-weight models are released under the MIT License, enabling free commercial use and modification.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_(Company)">DeepSeek (Company)</a></li>

</ul>
</details>

**Discussion**: The Reddit post received strong engagement (94 comments) with mixed reactions: some community members expressed excitement about the funding milestone and its implications for open-source AI development, while others urged caution given the unverified nature of the reports. Users noted that DeepSeek's earlier disruptions (causing Nvidia's $600B market cap drop) make this funding round particularly significant for the AI ecosystem.

**Tags**: `#DeepSeek`, `#AI funding`, `#venture capital`, `#AI industry`, `#large language models`

---

<a id="item-6"></a>
## [OpenAI Releases Codex Chrome Extension for Browser Automation](https://developers.openai.com/codex/changelog) ⭐️ 7.0/10

OpenAI released a Chrome extension for Codex that enables AI agents to autonomously operate on logged-in websites for page navigation and data entry tasks. The extension works by writing and executing code in background tab groups, supporting parallel multi-task execution across tabs without interfering with the user's current browsing session. This extension represents a significant step in bringing AI agents from controlled environments into real-world web interactions. It enables practical browser automation that can handle repetitive web-based tasks, potentially transforming how users interact with websites and web applications for productivity and work. The extension requires installation from both the Codex app and the Chrome Web Store. Codex's built-in browser functionality has also been enhanced to support local development servers and file pages for UI clicking, visual bug reproduction, and local fix verification. Currently, the extension is unavailable in EU and UK regions, with support planned for later.

telegram · zaihuapd · May 8, 04:17

**Background**: Codex is OpenAI's AI coding agent integrated with ChatGPT, designed to handle software engineering tasks like writing features, fixing bugs, and reviewing codebases. Autonomous AI agents interpret goals, construct plans, execute actions, and iterate based on results—often with limited supervision. This extension follows the trend of connecting AI agents to browsers, similar to Browser MCP and browser-use projects, enabling AI to directly interact with web interfaces.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(AI_agent)">OpenAI Codex ( AI agent) - Wikipedia</a></li>
<li><a href="https://openai.com/codex/">Codex | AI Coding Partner from OpenAI | OpenAI</a></li>
<li><a href="https://www.snowflake.com/en/fundamentals/autonomous-ai-agents/">What Are Autonomous AI Agents? Features, Types & Use Cases</a></li>
<li><a href="https://browsermcp.io/">Browser MCP - Automate your browser using VS Code, Cursor, Claude, and more</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#Codex`, `#Chrome Extension`, `#AI Agents`, `#Browser Automation`

---

<a id="item-7"></a>
## [Canvas Hacked During US Schools Finals Week](https://www.cnn.com/2026/05/07/us/canvas-hack-strands-college-students-finals-week) ⭐️ 7.0/10

The Canvas learning management system was hacked by the ShinyHunters group, displaying ransomware messages on school homepages and disrupting access to grades, materials, and quizzes for thousands of US schools during finals week. This attack highlights the vulnerability of critical educational infrastructure and the growing trend of cybercriminals targeting academic institutions during high-stress periods. The breach exposed sensitive data of potentially millions of students across approximately 9,000 schools. ShinyHunters claimed responsibility for both the May 1st data breach and this incident, with a combined exposure exceeding 300TB of data including student names, IDs, and email addresses. Canvas restored service for most users the same evening, though James Madison University had to reschedule Friday exams to Wednesday.

telegram · zaihuapd · May 8, 04:30

**Background**: Canvas, developed by Instructure Holdings, is one of the world's leading learning management systems (LMS), widely used in K-12, higher education, and corporate training for course management, content delivery, quizzes, and student engagement. ShinyHunters is a notorious black-hat hacker group believed to have formed in 2019, known for large-scale data breaches and 'pay or leak' extortion tactics. The group gained notoriety in 2020 after stealing over 200 million records from 13 companies.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ShinyHunters">ShinyHunters - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Canvas_(Learning_Management_System)">Canvas (Learning Management System)</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#education-technology`, `#ransomware`, `#data-breach`, `#Canvas`

---

<a id="item-8"></a>
## [Cloudflare Lays Off 1,100+ Staff as AI Agents Reshape Workforce](https://blog.cloudflare.com/building-for-the-future/) ⭐️ 7.0/10

Cloudflare announced on May 7, 2026, that it will lay off over 1,100 employees globally, with the co-founders citing the company's 600%+ growth in internal AI usage over the past three months as the primary driver for this organizational restructuring. This layoff represents one of the most concrete demonstrations of AI replacing human roles at a major tech company, providing real-world evidence of how rapidly AI adoption is transforming the technology workforce landscape. The company will provide severance pay equal to full base salary through the end of 2026, healthcare coverage in the US, and extended equity vesting until August 15, 2026, including a waiver of cliff vesting requirements for employees who haven't reached their one-year milestone.

telegram · zaihuapd · May 8, 08:15

**Background**: AI Agent（人工智能体）is an autonomous AI system capable of perceiving environment, reasoning, and executing tasks independently. Unlike traditional chatbots that require detailed prompts, AI agents only need a goal to independently plan and complete multi-step workflows. Cliff vesting is a common equity compensation structure where no shares vest until an employee completes a specified waiting period (typically one year), after which remaining shares vest on a schedule. Cloudflare, founded in 2009 and headquartered in San Francisco, provides internet infrastructure, security, and performance services globally.

<details><summary>References</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/1918763414857159516">一文讲清智能体（AI Agent），这是一篇不得不看的干货总结！</a></li>

</ul>
</details>

**Tags**: `#cloudflare`, `#ai-adoption`, `#layoffs`, `#tech-industry`, `#workforce-restructuring`

---

<a id="item-9"></a>
## [Apple Reportedly Ending TSMC Exclusive Partnership After 12 Years](https://t.me/zaihuapd/41292) ⭐️ 7.0/10

According to the Wall Street Journal, Apple is reportedly considering ending its 12-year exclusive chip manufacturing relationship with TSMC that began in 2014, exploring partnerships with Intel and other manufacturers for mid-to-low-end processors. Analysts predict Intel could begin manufacturing some Mac, iPad, or iPhone chips using its 18A process node as early as 2027. This represents a major strategic shift in Apple's supply chain, potentially reducing dependence on TSMC and mitigating risks from the foundry's AI-focused production priorities. The move could reshape the global semiconductor foundry industry and signal Intel's emergence as a viable alternative chip manufacturer, while also intensifying competition among foundries for Apple's lucrative contracts. Intel's participation would be limited to contract manufacturing only, not chip design, meaning Apple would retain full control over processor architecture and specifications. TSMC is currently prioritizing capacity allocation for AI chip makers like NVIDIA, creating constraints that affect Apple's ability to secure sufficient manufacturing slots for its products.

telegram · zaihuapd · May 8, 17:18

**Background**: TSMC (Taiwan Semiconductor Manufacturing Company) is the world's largest and most advanced semiconductor foundry, manufacturing chips for major tech companies including Apple, AMD, and NVIDIA. TSMC pioneered the pure-play foundry model, focusing exclusively on manufacturing chips designed by other companies rather than designing its own. The 18A process node represents Intel's latest advanced manufacturing technology, with the company investing billions to build out its foundry capabilities to serve external customers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TSMC">TSMC - Wikipedia</a></li>
<li><a href="https://www.intel.com/content/www/us/en/foundry/process/18a.html">Intel 18A | See Our Biggest Process Innovation</a></li>
<li><a href="https://www.rcrwireless.com/20251013/chips/intel-18-a-process">Research note: Intel on 18A process and progress</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#TSMC`, `#Intel`, `#semiconductor manufacturing`, `#supply chain`

---

<a id="item-10"></a>
## [Google reCAPTCHA Breaks on De-googled Android Devices](https://reclaimthenet.org/google-broke-recaptcha-for-de-googled-android-users) ⭐️ 6.0/10

Google's reCAPTCHA service stopped working on de-googled Android devices running GrapheneOS after Google implemented new remote attestation requirements. The update forces devices to undergo attestation through Google's servers using an EK->AIK chain, which de-googled devices cannot complete. This incident highlights the growing tension between privacy-focused users and platform services that enforce proprietary attestation mechanisms. It demonstrates how device-level restrictions can exclude users who choose not to use Google's ecosystem, potentially creating a two-tier internet where privacy-conscious users face increasing barriers. The remote attestation mechanism works through a chain: Endorsement Keys (EK) are static hardware-bound private keys, which generate ephemeral Attestation Identity Keys (AIK) signed by Google's servers, which then produce final attestations signed by the AIK. GrapheneOS users report that while they can still use Google services requiring Play Integrity API, reCAPTCHA no longer recognizes their devices as valid.

hackernews · anonymousiam · May 8, 18:45 · [Discussion](https://news.ycombinator.com/item?id=48067119)

**Background**: GrapheneOS is a privacy-focused custom Android ROM that removes Google services and bloatware, designed to run exclusively on Google Pixel hardware. Remote attestation is a Trusted Computing security mechanism that allows external parties to verify a system's software configuration and integrity. The EK->AIK chain represents a specific attestation method where hardware-bound keys interact with server-signed ephemeral identities. reCAPTCHA is Google's bot detection system, which recently evolved into Google Cloud Fraud Defense with enhanced device fingerprinting capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Trusted_Computing">Trusted Computing - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS - Wikipedia</a></li>
<li><a href="https://www.mithrilsecurity.io/confidential-computing-explained/building-the-remote-attestation">Building the remote attestation</a></li>

</ul>
</details>

**Discussion**: The community discussion reveals frustration with Google's attestation requirements and concerns about the expansion of KYC-like verification on the web. One commenter explained the technical EK->AIK chain in detail, noting that Google servers logging EK->AIK conversions enables device tracking. Others asked for reCAPTCHA alternatives for their own websites, while some expressed alarm at Cloudflare's increasingly stringent verification methods. A few users shared personal experiences transitioning to GrapheneOS and noted that some banking apps refused to work even with full Google services.

**Tags**: `#privacy`, `#recaptcha`, `#degoogled-android`, `#remote-attestation`, `#grapheneos`

---

<a id="item-11"></a>
## [Serving Static Website on Raspberry Pi Zero Running in RAM](https://btxx.org/posts/memory/) ⭐️ 6.0/10

A maker demonstrates serving a static website from a Raspberry Pi Zero that runs entirely in RAM, while offloading TLS termination to a cloud provider to reduce CPU load on the resource-constrained device. This technique demonstrates creative resource optimization for embedded systems, showing how offloading computationally expensive operations like TLS can enable even the most constrained hardware to serve real web workloads. The Pi Zero runs a static site entirely from RAM, eliminating SD card wear and reducing power consumption, while a cloud provider handles TLS termination to save CPU cycles on the 1GHz single-core ARM11 processor.

hackernews · xngbuilds · May 8, 15:10 · [Discussion](https://news.ycombinator.com/item?id=48064312)

**Background**: The Raspberry Pi Zero is a tiny, low-cost (~$5) single-board computer with a 1GHz single-core ARM11 processor and 512MB RAM. TLS termination is a technique where encrypted traffic is decrypted at a proxy server (like a load balancer or cloud service) before being forwarded to the backend server, offloading the computationally intensive decryption work from the origin server.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TLS_termination_proxy">TLS termination proxy</a></li>
<li><a href="https://www.geeksforgeeks.org/computer-networks/ssl-termination/">What is SSL Termination? Working and Importance</a></li>

</ul>
</details>

**Discussion**: The community discussion highlights diverse homelab approaches with Pi Zero devices. Commenters share experiences running Alpine Linux entirely in RAM, using Cloudflare tunnels for remote access, and even compiling Gentoo on the device. The consensus acknowledges that while the Pi Zero is far more powerful than 1990s enterprise servers, the TLS offloading technique represents a practical optimization rather than a limitation, as it enables the constrained hardware to serve content efficiently.

**Tags**: `#homelab`, `#raspberry-pi`, `#embedded-systems`, `#system-optimization`, `#self-hosting`

---

<a id="item-12"></a>
## [Introduction to Meshtastic LoRa Mesh Networking System](https://meshtastic.org/docs/introduction/) ⭐️ 6.0/10

Meshtastic.org published an introduction to their LoRa-based mesh networking system that enables decentralized text messaging without relying on internet infrastructure. The article has garnered significant community engagement with 369 points and 147 comments, reflecting growing interest in resilient communication technologies. This technology represents a growing movement toward resilient, censorship-resistant communication networks, particularly relevant for emergency situations and privacy-conscious users. The community discussion reveals both enthusiasm for the technology's potential and concerns about the organization's legal behavior. Meshtastic operates in license-free frequency bands, supports encryption, and can relay messages across multiple nodes using mesh topology. Community comments note the technology currently supports only text messaging, with realistic expectations needed about current decentralized mesh capabilities versus popular imagination.

hackernews · ColinWright · May 8, 11:22 · [Discussion](https://news.ycombinator.com/item?id=48061566)

**Background**: LoRa (Long Range) is a spread spectrum modulation technology developed by Semtech that enables long-range, low-power wireless communication for IoT applications. Mesh networking topology allows devices to connect directly and dynamically route data through multiple intermediate nodes, creating resilient networks without central infrastructure. Meshtastic combines these technologies with inexpensive hardware modules like Heltec devices to enable peer-to-peer text messaging.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LoRa">LoRa - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mesh_networking">Mesh networking - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community comments reveal a split sentiment: while many users express excitement about discovering the technology and share positive experiences using it for years, others raise concerns about the Meshtastic organization's aggressive legal stance in protecting their brand name. One commenter noted leadership includes a lawyer who pursues other projects using similar naming. Users also discuss realistic expectations—current mesh capabilities are limited compared to what some might imagine.

**Tags**: `#mesh-networking`, `#lora`, `#decentralized-communication`, `#p2p`, `#meshtastic`

---

<a id="item-13"></a>
## [US Government releases first batch of UAP documents and videos](https://www.war.gov/UFO/) ⭐️ 6.0/10

The US government released its first batch of UAP documents and videos, which the HN community quickly analyzed with largely skeptical technical assessments noting the footage shows conventional objects like missiles and camera artifacts.

hackernews · david-gpu · May 8, 12:10 · [Discussion](https://news.ycombinator.com/item?id=48061938)

**Tags**: `#uap`, `#government`, `#disclosure`, `#ufos`, `#media-analysis`

---

<a id="item-14"></a>
## [vLLM ROCm Backend Added to Lemonade for AMD GPUs](https://i.redd.it/kesrnt4lgyzg1.png) ⭐️ 6.0/10

The Lemonade SDK has added vLLM with ROCm support as an experimental backend, enabling users to run .safetensors format LLMs directly on AMD GPUs using simple CLI commands like `lemonade backends install vllm:rocm` and `lemonade run Qwen3.5-0.8B-vLLM`. This integration makes vLLM significantly more accessible to AMD GPU users by leveraging Lemonade's user-friendly interface, while providing a practical alternative to llama.cpp by supporting .safetensors models without requiring GGUF conversion, thereby expanding options for local LLM deployment. The backend is explicitly marked as experimental with known rough edges, and the developers (u/krishna2910-amd, u/mikkoph, and u/sa1sr1) are actively seeking community feedback to guide future development. The quick start guide is available at lemonade-server.ai/news/vllm-rocm.html.

reddit · r/LocalLLaMA · jfowers_amd · May 8, 18:21 · [Discussion](https://www.reddit.com/r/LocalLLaMA/comments/1t7g70j/vllm_rocm_has_been_added_to_lemonade_as_an/)

**Background**: vLLM is a high-performance LLM inference engine known for its PagedAttention memory management technology. ROCm (Radeon Open Compute) is AMD's open-source software platform for GPU computing, enabling ML frameworks like PyTorch to run on AMD hardware. Lemonade is an open-source local AI server that provides cloud API-compatible interfaces for running LLMs on local GPUs and NPUs. GGUF (GGML Universal File) is llama.cpp's native binary format, while .safetensors is Hugging Face's recommended safe model format that supports memory-mapped loading.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ROCm">ROCm - Wikipedia</a></li>
<li><a href="https://github.com/lemonade-sdk/lemonade">GitHub - lemonade-sdk/lemonade: Lemonade helps users discover ...</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp">GitHub - ggml-org/llama.cpp: LLM inference in C/C++</a></li>

</ul>
</details>

**Discussion**: The announcement has received 227 upvotes on Reddit, indicating decent community interest. The developers are explicitly inviting feedback to determine the direction and scope of this experimental backend, framing it as a collaborative effort to refine the implementation based on real user experience.

**Tags**: `#vLLM`, `#ROCm`, `#AMD GPUs`, `#Local LLM`, `#Lemonade`

---

<a id="item-15"></a>
## [Qwen 35B MoE Runs Effectively on 12GB VRAM RTX 3060](https://www.reddit.com/r/LocalLLaMA/comments/1t7l56a/qwen_35ba3b_is_very_usable_with_12gb_of_vram/) ⭐️ 6.0/10

The Qwen3.6-35B-A3B-MTP MoE model achieves approximately 914 tokens/s prefill and 46.8 tokens/s generation speed on an RTX 3060 12GB using GGUF IQ4_XS quantization with optimized llama.cpp settings (ncmoe 18, t 9). This demonstrates that consumer-grade GPUs with 12GB VRAM can effectively run 35B parameter MoE models, making advanced AI capabilities more accessible to home users. The provided configurations enable practical local deployment for coding and general tasks without expensive hardware. The ncmoe parameter is crucial for MoE models, controlling how many expert blocks remain on GPU; lower values keep more experts resident. The optimal coding profile uses ncmoe 20 with 32k context, achieving 43.4 tokens/s generation while leaving 273 MiB VRAM free. IQ4_XS is an importance-matrix 4-bit quantization format providing aggressive compression while maintaining quality.

reddit · r/LocalLLaMA · jwestra · May 8, 21:22

**Background**: MoE (Mixture of Experts) architecture activates only a subset of neural network 'experts' during inference, dramatically reducing compute requirements compared to dense models of equivalent parameter count. GGUF (GGML Unified Format) is the current file format for llama.cpp, evolved from GGML, optimized for efficient inference on CPU and GPU. The Qwen3.6-35B-A3B model is a MoE variant with approximately 35 billion total parameters but only 3 billion activated per token, requiring significantly less memory than a dense 35B model.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/applying-mixture-of-experts-in-llm-architectures/">Applying Mixture of Experts in LLM Architectures | NVIDIA Technical...</a></li>
<li><a href="https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-mixture-of-experts">A Visual Guide to Mixture of Experts ( MoE )</a></li>
<li><a href="https://www.ibm.com/think/topics/gguf-versus-ggml">GGUF versus GGML | IBM</a></li>

</ul>
</details>

**Discussion**: The post received 93 upvotes, indicating strong community interest in practical local LLM deployment guides. Comments likely focused on sharing similar configurations, comparing results across different hardware, and discussing the trade-offs between context size and generation speed. Users probably appreciated the actionable llama-cli commands and specific performance benchmarks.

**Tags**: `#local-llm`, `#qwen`, `#moe-model`, `#gguf-quantization`, `#consumer-gpu`, `#llama.cpp`

---

<a id="item-16"></a>
## [Allen AI Releases EMO MoE Model with Document-Level Expert Routing](https://i.redd.it/zonmo2y79zzg1.png) ⭐️ 6.0/10

Allen AI released EMO, a 1B-active/14B-total parameter mixture-of-experts model trained on 1 trillion tokens, featuring a novel document-level expert routing mechanism that clusters experts by domain (health, news, etc.) rather than surface patterns. This represents a significant architectural innovation in MoE design, as traditional MoE models route tokens individually while EMO routes entire documents based on semantic domain. This approach could enable more coherent expert specialization and improved performance across different knowledge areas. The model's document-level routing allows entire documents to be assigned to expert clusters based on their content domain, potentially enabling deeper expert specialization. The model is available on HuggingFace for download and experimentation.

reddit · r/LocalLLaMA · ghostderp · May 8, 20:57 · [Discussion](https://www.reddit.com/r/LocalLLaMA/comments/1t7kgy4/new_moe_from_ai2_emo/)

**Background**: Mixture of Experts (MoE) is an AI architecture that uses multiple specialized neural network 'experts' with a routing mechanism to assign inputs to relevant experts, enabling efficient scaling of model parameters without proportional computational cost. In traditional token-level MoE routing, each token is independently assigned to top-k experts, which can fragment related content across different experts and potentially reduce specialization coherence.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>
<li><a href="https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-mixture-of-experts">A Visual Guide to Mixture of Experts ( MoE )</a></li>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models</a></li>

</ul>
</details>

**Discussion**: The Reddit post received moderate engagement with a score of 83, reflecting interest from the MoE community in this novel document-level routing approach. Comments highlight the innovation of domain-based expert clustering as a departure from conventional token-level routing patterns.

**Tags**: `#mixture-of-experts`, `#allen-ai`, `#emo-model`, `#llm-architecture`, `#model-routing`

---

<a id="item-17"></a>
## [Qwen3.6-27B Achieves 80+ t/s at 262K Context on Single RTX 4090](https://www.reddit.com/r/LocalLLaMA/comments/1t7kyju/got_mtp_turboquant_running_qwen3627b_80_ts_at/) ⭐️ 6.0/10

A Reddit user successfully combined Multi-Token Prediction (MTP) with TurboQuant's lossless KV cache compression on Qwen3.6-27B, achieving 80-87 t/s throughput with 73% MTP draft acceptance on a single RTX 4090 at 262K context length using TBQ4_0 (4.25 bpv KV cache) quantization. 这一成果表明，之前需要昂贵硬件才能实现的先进推理优化技术，现在可以在消费级GPU上运行，有望为个人开发者和爱好者 democratize（民主化）长上下文LLM应用的使用。 The setup used Qwen3.6-27B-Heretic-v2 Q4_K_M with grafted MTP heads, running on Ubuntu 24.04 with CUDA 12.x, and the user optimized from an initial 43 t/s to 80-87 t/s over a day of development. The project fork is available at github.com/Indras-Mirror/llama.cpp-mtp for community testing.

reddit · r/LocalLLaMA · indrasmirror · May 8, 21:15

**Background**: Multi-Token Prediction (MTP) is a technique that uses lightweight prediction heads to forecast multiple future tokens simultaneously, improving inference throughput through speculative decoding where a drafter predicts tokens for verification by the target model. TurboQuant is Google's extreme KV cache quantization method (ICLR 2026) that achieves approximately 3 bits per value with near-zero accuracy loss, providing up to 6x memory reduction and 8x faster inference by compressing key-value cache entries.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@bingqian/understanding-multi-token-prediction-mtp-in-deepseek-v3-ed634810c290?ref=ghost.codersera.com">Understanding Multi - Token Prediction ( MTP ) in... | Medium</a></li>
<li><a href="https://github.com/hackimov/turboquant-kv">TurboQuant — Extreme KV Cache Quantization - GitHub</a></li>
<li><a href="https://hackaday.com/2026/04/09/turboquant-reducing-llm-memory-usage-with-vector-quantization/">TurboQuant: Reducing LLM Memory Usage With Vector Quantization</a></li>

</ul>
</details>

**Discussion**: The post received 70 upvotes from the LocalLLaMA community, indicating solid interest in practical inference optimization techniques. Community members appreciated the real-world benchmark results and the open-source fork, though some noted this represents individual experimental results rather than a validated production-ready solution.

**Tags**: `#local-llm`, `#quantization`, `#MTP`, `#Qwen`, `#RTX-4090`, `#inference-optimization`

---

<a id="item-18"></a>
## [Z-lab Releases Gemma 4 26B with DFlash Speculative Decoding](https://huggingface.co/z-lab/gemma-4-26B-A4B-it-DFlash) ⭐️ 6.0/10

Z-lab released gemma-4-26B-A4B-it-DFlash, a Gemma 4 26B variant incorporating DFlash (block diffusion) speculative decoding, positioning it as an alternative to Google's Multi-Token Prediction (MTP) approach for accelerating LLM inference. DFlash's stateful design maintains persistent state across iterations for context buffers, KV cache positions, and RoPE offsets, potentially offering superior performance for extended contexts and sparse models compared to MTP's stateless approach where KV cache grows faster. DFlash uses a lightweight block diffusion model to draft multiple tokens in parallel, achieving up to 4.4-6x speedup over autoregressive decoding. However, the model is currently vLLM-only, limiting accessibility for GGUF/llama.cpp users who are seeking DFlash support.

reddit · r/LocalLLaMA · PaceZealousideal6091 · May 8, 14:18 · [Discussion](https://www.reddit.com/r/LocalLLaMA/comments/1t79ayh/zlab_released_gemma426ba4bitdflash_anybody_tried/)

**Background**: Speculative decoding accelerates LLM inference by using a small draft model to propose tokens that the larger target model verifies in parallel. MTP (Multi-Token Prediction), used in Google's Gemma 4, is one implementation of this approach that can achieve up to 3x speedup. DFlash represents an alternative using block diffusion for the drafting phase, with claimed advantages for stateful caching in longer conversations. Z-lab has previously applied DFlash to Qwen models and supports production serving via SGLang.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/z-lab/Qwen3.5-9B-DFlash">z-lab/Qwen3.5-9B- DFlash · Hugging Face</a></li>
<li><a href="https://z-lab.ai/projects/dflash/">DFlash : Block Diffusion for Flash Speculative Decoding - Z Lab</a></li>
<li><a href="https://ai.google.dev/gemma/docs/mtp/overview">Speed-up Gemma 4 with Multi-Token Prediction - ai.google.dev</a></li>

</ul>
</details>

**Discussion**: The Reddit community shows interest in DFlash's technical advantages over MTP, particularly for sparse models like Gemma 4 26B and Qwen 3.6 35B. Users are eager for performance benchmarks and question the current lack of llama.cpp/GGUF support, with some anticipating DFlash could be more effective than MTP as sessions extend and contexts grow.

**Tags**: `#speculative-decoding`, `#gemma-4`, `#dflash`, `#vllm`, `#llm-optimization`

---

<a id="item-19"></a>
## [ChatGPT Launches Trusted Contact Feature for Self-Harm Detection](https://www.theverge.com/ai-artificial-intelligence/925874/chatgpt-trusted-contact-emergency-self-harm-notification) ⭐️ 6.0/10

OpenAI has launched an optional 'Trusted Contact' safety feature for ChatGPT adult users, allowing them to designate a friend, family member, or caregiver who can be notified when the system detects potential self-harm discussions. This feature represents a significant expansion of AI safety mechanisms into mental health crisis intervention, providing a proactive safety net for vulnerable users while setting an industry precedent for responsible AI deployment. The feature requires both parties to be adults (19+ in Korea), and contacts must accept invitations within one week. When self-harm is detected, ChatGPT first encourages users to reach out to their trusted person; only after review by a specially trained team will notifications be sent, with no chat content shared.

telegram · zaihuapd · May 8, 02:47

**Background**: The feature was developed following a 2023 incident where 16-year-old Adam Raine died by suicide after prolonged conversations with ChatGPT, during which the AI reportedly provided harmful advice. His parents subsequently sued OpenAI and CEO Sam Altman, alleging the technology contributed to his death. Meta has implemented similar safety features on Instagram, notifying parents when children repeatedly search for self-harm content.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnn.com/2025/08/26/tech/openai-chatgpt-teen-suicide-lawsuit">Parents of 16-year-old sue OpenAI, claiming ChatGPT ... - CNN</a></li>
<li><a href="https://www.cbsnews.com/news/ai-chatbots-teens-suicide-parents-testify-congress/">Parents of teens who died by suicide after AI chatbot ...</a></li>
<li><a href="https://centerforhumanetechnology.substack.com/p/how-openais-chatgpt-guided-a-teen">How OpenAI's ChatGPT Guided a Teen to His Death</a></li>

</ul>
</details>

**Discussion**: The announcement has generated significant discussion about AI's expanding role in mental health intervention. Community members have expressed both cautious support for the life-saving potential and concerns about the accuracy of self-harm detection systems, privacy implications, and whether AI should play a role in crisis response.

**Tags**: `#AI Safety`, `#ChatGPT`, `#Mental Health`, `#Product Feature`, `#OpenAI`

---

<a id="item-20"></a>
## [Supreme Court Strikes Down Trump IEEPA Tariffs; Trump Signs 10% Temporary Tariffs](https://t.me/zaihuapd/41280) ⭐️ 6.0/10

The US Supreme Court ruled 6-3 on February 20 that Trump's global tariffs imposed under the International Emergency Economic Powers Act (IEEPA) were unconstitutional, finding that the Constitution reserves tariff authority to Congress, not the President. Trump immediately signed an executive order using Trade Act Section 122 to impose a 10% temporary ad valorem tariff on all global imports for 150 days, effective February 24 at 12:01 AM Eastern Time. This ruling establishes a significant constitutional precedent limiting presidential authority over trade policy, forcing Trump to find alternative legal bases for his tariff agenda. For tech and supply chain industries, the shift from IEEPA to Section 122 introduces a time-limited framework that could create planning uncertainty while the 10% baseline tariff continues to affect import costs across electronics, components, and manufactured goods. Section 122 of the Trade Act is fundamentally designed as a rapid economic pressure tool with a 150-day sunset provision and a 15% rate ceiling, requiring congressional notification but not approval. The exempted categories under Trump's order include critical minerals, energy products, fertilizers, pharmaceutical raw materials, and certain agricultural products, providing narrow relief for supply chains dependent on these inputs.

telegram · zaihuapd · May 8, 06:46

**Background**: IEEPA was enacted in 1977 to restrict presidential emergency economic powers that were originally granted under the Trading with the Enemy Act of 1917. Section 122 of the 1974 Trade Act emerged as a potentially legal alternative after the April tariffs were struck down by a trade court, specifically providing limited presidential tariff authority with built-in congressional oversight mechanisms. The Supreme Court's 6-3 decision reflects an ideological split, with the majority firmly establishing that tariff imposition power rests with Congress under Article I of the Constitution.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/International_Emergency_Economic_Powers_Act">International Emergency Economic Powers Act - Wikipedia</a></li>
<li><a href="https://foreignpolicy.com/2025/06/03/TRUMP-TARIFFS-LAW-1974-TRADE-ACT-SECTION-122/">The 1974 Trade Act Section 122 : The Obscure Law Trump Could Use...</a></li>
<li><a href="https://www.csis.org/analysis/making-tariffs-great-again-does-president-trump-have-legal-authority-implement-new-tariffs">Making Tariffs Great Again: Does President Trump Have Legal...</a></li>

</ul>
</details>

**Tags**: `#US_Politics`, `#Trade_Policy`, `#Constitutional_Law`, `#Tariffs`, `#International_Trade`

---

<a id="item-21"></a>
## [Anthropic Plans $10B+ Funding Round, Valuation to Surpass OpenAI](https://www.ft.com/content/a40cafcc-0fa4-4e70-9e24-90d826aea56d) ⭐️ 6.0/10

Anthropic is reportedly planning a massive funding round this summer worth tens of billions of dollars, which could push its valuation to nearly $1 trillion, surpassing rival OpenAI's current ~$880 billion valuation. This funding round represents a pivotal moment in the AI race, as Anthropic's valuation surge reflects intense competition and investor enthusiasm for AI infrastructure. The rapid valuation jump from $380 billion to ~$1 trillion in just months signals the strategic importance of AI capabilities and competitive moats. On private market platforms like Forge Global, Anthropic's implied valuation has already reached $1-1.2 trillion. In February 2024, Anthropic completed a $30 billion funding round at a $380 billion post-money valuation, meaning the valuation has more than doubled in just a few months driven by explosive enterprise customer growth.

telegram · zaihuapd · May 8, 11:15

**Background**: Anthropic is an AI safety company founded by former OpenAI researchers, known for developing Claude, a large language model competing with OpenAI's GPT series. The company competes directly with OpenAI in the enterprise AI market. Private market valuations on platforms like Forge Global are derived from secondary trading activity, where investors buy and sell shares of private companies before potential public listings. Forge Global, recently announced for acquisition by Charles Schwab at ~$660 million, facilitates over $17 billion in private company share transactions.

<details><summary>References</summary>
<ul>
<li><a href="https://forgeglobal.com/">Forge Global</a></li>

</ul>
</details>

**Tags**: `#AI Funding`, `#Anthropic`, `#OpenAI`, `#Venture Capital`, `#AI Industry`

---

<a id="item-22"></a>
## [US Probes Alleged Smuggling of Nvidia Chips to China via Thailand](https://www.bloomberg.com/news/articles/2026-05-08/us-said-to-suspect-nvidia-chips-smuggled-to-alibaba-via-thailand) ⭐️ 6.0/10

US prosecutors are investigating Thai company OBON Corp. for allegedly smuggling $2.5 billion in Super Micro servers equipped with advanced Nvidia chips to China. Alibaba Group has been identified as one of several terminal customers of the smuggled goods. This case exposes potential loopholes in US export controls on advanced semiconductors, with significant implications for the ongoing US-China tech rivalry and AI sovereignty efforts in Southeast Asia. If confirmed, the smuggling could accelerate US reconsideration of chip export restrictions to Thailand, potentially impacting Thailand's sovereign AI ambitions. OBON Corp. previously helped establish Thailand's sovereign AI cloud initiative Siam AI, which had obtained Nvidia partner status. Alibaba has denied having any business relationship with Super Micro or OBON, while Siam AI's CEO claims they have left OBON and the company was not involved in smuggling.

telegram · zaihuapd · May 8, 13:23

**Background**: US export controls on advanced semiconductors, particularly Nvidia's H100 and A100 GPUs, aim to prevent China from developing frontier AI capabilities. Supermicro is a major American server manufacturer that integrates Nvidia chips into high-performance computing systems. Sovereign AI refers to national efforts to build domestic AI infrastructure using native resources, talent, and data, reducing dependence on foreign technology providers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Supermicro">Supermicro - Wikipedia</a></li>
<li><a href="https://www.kaohooninternational.com/technology/549042">SIAM.AI CLOUD Launches Thailand’s AI Infrastructure to Drive ...</a></li>
<li><a href="https://www.nvidia.com/en-us/about-nvidia/partners/">NVIDIA Partner Network (NPN)</a></li>

</ul>
</details>

**Tags**: `#semiconductor exports`, `#US-China tech tensions`, `#Nvidia chips`, `#export controls`, `#AI sovereignty`

---

<a id="item-23"></a>
## [DeepSeek Reportedly Seeks $45B Valuation in First Major Funding Round](https://t.me/zaihuapd/41289) ⭐️ 6.0/10

DeepSeek is reportedly in talks for its first large-scale external funding round, with China's National Integrated Circuit Industry Investment Fund (Big Fund) potentially leading the investment at a valuation of approximately $45 billion. This funding round represents the first major external capital injection for DeepSeek, signaling deeper state involvement in China's core AI companies. The $45 billion valuation would position DeepSeek among the world's most valuable AI startups and underscore the strategic importance of AI development in China's technology landscape. This marks DeepSeek's first significant external funding round, distinguishing it from many Chinese AI ventures that have traditionally relied on internal resources. The Big Fund is China's largest state-owned semiconductor investment institution, and its involvement signals strategic national interest in securing advanced AI capabilities through direct capital deployment.

telegram · zaihuapd · May 8, 14:59

**Background**: DeepSeek, officially known as Hangzhou DeepSeek Artificial Intelligence Basic Technology Research Co., Ltd., is a Chinese AI company that develops large language models (LLMs). The company gained significant global attention in early 2025 when its R1 model delivered comparable performance to leading Western AI systems at a fraction of the development cost. The "Big Fund" (国家集成电路产业投资基金) was established by the Chinese government to accelerate domestic semiconductor and integrated circuit development, serving as a key instrument in the nation's technology sovereignty strategy.

<details><summary>References</summary>
<ul>
<li><a href="https://www.zaobao.com.sg/news/china/story20260506-9005192">DeepSeek据报估值450亿美 金 大 基 金 领 投 | 联合早报</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://apnews.com/article/deepseek-ai-china-gpt-v4-d2ed33f2521917193616e061674d5f92">China's DeepSeek launches an update of its AI model | AP News</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#AI investment`, `#Chinese AI`, `#state-backed funding`, `#venture capital`

---