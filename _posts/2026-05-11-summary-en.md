---
layout: default
title: "Horizon Daily: 2026-05-11"
date: 2026-05-11
lang: en
---

> From 16 items, 7 important content pieces were selected

---

1. [EU Digital ID Wallet Creates Dependency on Google/Apple Hardware](#item-1) ⭐️ 7.0/10
2. [Rossmann Offers Legal Support for OrcaSlicer Developer Threatened by Bambu Lab](#item-2) ⭐️ 7.0/10
3. [NYT Corrects AI-Generated Fake Quote in Canada Election Article](#item-3) ⭐️ 7.0/10
4. [Local AI Needs to Become the Standard](#item-4) ⭐️ 6.0/10
5. [Fictional CVE-2024-YIKES Report Sparks Real Supply Chain Security Discussion](#item-5) ⭐️ 6.0/10
6. [Report Exposes Chinese Grey Market Claude API Scams at 90% Discount](#item-6) ⭐️ 6.0/10
7. [Chrome 148 Removes On-Device AI Privacy Wording, Google Claims No Behavioral Change](#item-7) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [EU Digital ID Wallet Creates Dependency on Google/Apple Hardware](https://grapheneos.social/@GrapheneOS/116550899908879585) ⭐️ 7.0/10

The EU Digital Identity Wallet (EUDI) requires hardware attestation exclusively from Google or Apple, effectively creating a mandatory dependency on US tech platforms for all European digital identities. The system does not implement zero-knowledge proof systems or blind signatures, leaving traceable attestation packets that can be used to link user actions to their devices. This policy decision forces EU citizens to use American-controlled hardware for official digital identity verification, raising serious questions about digital sovereignty and creating vendor lock-in that undermines open competition. Privacy advocates warn that without privacy-preserving technologies, every attestation leaves a traceable record enabling comprehensive user tracking. Hardware attestation uses cryptographic keys in device secure enclaves to verify system integrity, with certificates signed by device manufacturers. Critics note the system introduces 'indirection' through static device IDs and ephemeral identities, but this obfuscation fails to prevent linkage since attestation packets remain tied to device identity. Windows 11's TPM requirements represent another step toward requiring manufacturer-approved hardware for standard computing.

hackernews · ChuckMcM · May 10, 17:54 · [Discussion](https://news.ycombinator.com/item?id=48086190)

**Background**: Hardware attestation is a security mechanism that provides cryptographic proof a device is genuine and uncompromised, using keys stored in hardware-backed secure environments. Zero-knowledge proofs (ZKPs) are cryptographic techniques that allow one party to prove knowledge without revealing the underlying information. The concept of digital sovereignty refers to a nation's ability to control its digital infrastructure independently. Intel faced massive opposition in 1999 when it attempted to include software-readable serial numbers in CPUs, eventually reversing the decision; this historical precedent shaped debates around mandatory hardware attestation requirements.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.android.com/privacy-and-security/security-key-attestation">Verify hardware-backed key pairs with key attestation | Security | Android Developers</a></li>
<li><a href="https://spruceid.com/learn/attestation">What Is Device Attestation? | SpruceID</a></li>
<li><a href="https://medium.com/@CIFDAQ/the-rise-of-zero-knowledge-proofs-privacy-meets-scalability-4e2e00eb141d">The Rise of Zero - Knowledge Proofs : Privacy Meets... | Medium</a></li>

</ul>
</details>

**Discussion**: Community commenters express strong concerns about digital sovereignty, with one noting the irony that protecting children appears prioritized over sovereignty. A key technical critique is that without zero-knowledge proofs, attestation packets create linkable records rather than true privacy. Others draw historical parallels to Intel's abandoned Processor Serial Number, arguing that security advocates have gradually advanced similar goals through TPMs and mobile walled gardens. Some commenters clarify the argument is not that attestation itself is bad, but that it should explicitly include non-Google/Apple providers to prevent monopoly lock-in.

**Tags**: `#hardware-attestation`, `#digital-sovereignty`, `#monopoly`, `#privacy`, `#EU-regulation`

---

<a id="item-2"></a>
## [Rossmann Offers Legal Support for OrcaSlicer Developer Threatened by Bambu Lab](https://www.tomshardware.com/3d-printing/louis-rossmann-tells-3d-printer-maker-bambu-lab-to-go-bleep-yourself-over-its-lawsuit-against-enthusiast-right-to-repair-advocate-offers-to-pay-the-legal-fees-for-a-threatened-orcaslicer-developer) ⭐️ 7.0/10

Louis Rossmann, a prominent repair YouTuber and right-to-repair advocate, announced he will cover the legal fees for an OrcaSlicer developer who received a legal threat from Bambu Lab over alleged unauthorized use of the company's private cloud APIs. The dispute centers on whether a fork of the open-source slicer software improperly interacted with Bambu's non-public cloud infrastructure to impersonate Bambu Studio. This legal dispute highlights the escalating tensions between hardware manufacturers and the open-source community over software control and device access. The outcome could set a precedent for how 3D printer companies handle third-party slicer software and whether users have the right to modify or fork open-source tools that work with their own hardware. OrcaSlicer, the original slicer, already supports Bambu printers natively. The controversy reportedly involves a separate fork that allegedly connected directly to Bambu's private cloud APIs to replicate Bambu Studio functionality. Community members note this case is specifically about cloud API access rather than direct printer communication, which complicates the right-to-repair argument.

hackernews · iancmceachern · May 10, 14:47 · [Discussion](https://news.ycombinator.com/item?id=48084432)

**Background**: A slicer is essential 3D printing software that converts 3D models into machine-readable G-code instructions. OrcaSlicer is a popular open-source slicer fork known for advanced calibration and network printing capabilities. Louis Rossmann is a well-known electronics repair advocate who runs a popular YouTube channel focused on board-level repairs and right-to-repair advocacy. Right-to-repair refers to the movement advocating for consumers' ability to repair and modify products they own, including accessing software and hardware without manufacturer restrictions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.orcaslicer.com/">OrcaSlicer — Official Website & Downloads (Orca Slicer)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Slicer_(3D_printing)">Slicer (3D printing) - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The community response is largely sympathetic to the OrcaSlicer developer and critical of Bambu Lab. Multiple commenters express frustration with Bambu's history of attempting to eliminate offline access and their perception of Bambu as treating customers as "leasing" rather than owning their devices. However, some commenters note the nuance that the fork allegedly accessed private cloud APIs rather than just communicating with the printer directly, which complicates the ethical analysis. Louis Rossmann is widely praised for his consistent advocacy, with commenters acknowledging he doesn't always get it right but appreciates his authenticity.

**Tags**: `#right-to-repair`, `#3d-printing`, `#open-source`, `#bambu-lab`, `#legal-threats`

---

<a id="item-3"></a>
## [NYT Corrects AI-Generated Fake Quote in Canada Election Article](https://simonwillison.net/2026/May/10/new-york-times-editors-note/#atom-everything) ⭐️ 7.0/10

The New York Times published an editors' note admitting that a reporter used an AI tool to summarize Canadian Conservative leader Pierre Poilievre's political views. The AI returned a fabricated quotation attributing specific words to Poilievre that he never said—including referring to politicians who changed allegiances as "turncoats"—which was published before being corrected. This incident provides concrete documentation of a major newsroom publicly acknowledging that generative AI produced a fabricated quotation that made it into a published article. It serves as a cautionary case for journalism, demonstrating that AI tools used for summarizing quotes can introduce dangerous factual errors that bypass editorial scrutiny. The original article, published on April 14, 2026, covered Canada's election and Mark Carney's Liberal Party. The editors' note states the reporter "should have checked the accuracy of what the A.I. tool returned." The correction now accurately quotes from a speech Poilievre delivered in April 2026.

rss · Simon Willison · May 10, 23:58

**Background**: AI hallucination refers to instances where large language models generate plausible-sounding but entirely fabricated information presented as fact. This poses significant challenges for deploying LLMs in high-stakes scenarios like journalism, legal documentation, or medical diagnostics. Unlike human errors, AI hallucinations can be confidently stated and difficult to detect without direct verification against primary sources.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_hallucination">AI hallucination</a></li>

</ul>
</details>

**Discussion**: Simon Willison, a respected voice in the tech community, highlighted this incident as valuable documentation of AI limitations in professional settings. The discussion reinforces ongoing concerns about using AI tools for tasks requiring factual accuracy, with many noting that the core issue—the reporter's failure to verify—echoes long-standing journalistic standards that predate AI.

**Tags**: `#ai-hallucination`, `#journalism`, `#ai-ethics`, `#generative-ai`, `#fact-checking`

---

<a id="item-4"></a>
## [Local AI Needs to Become the Standard](https://unix.foo/posts/local-ai-needs-to-be-norm/) ⭐️ 6.0/10

An opinion piece argues that local AI should become the standard computing paradigm, drawing parallels to the historical open source movement and tracing the progression of AI infrastructure from large data centers to personal devices like MacBooks with 128GB VRAM. This matters because it addresses fundamental questions about AI privacy, dependency on centralized providers like Anthropic and OpenAI, and the democratization of AI capabilities. The shift to local inference could fundamentally change how individuals and organizations interact with AI. The discussion highlights a projected trajectory: from large data centers, to server clusters with multiple H100 GPUs, to consumer devices like MacBook Pros with 128GB unified memory. Commenters suggest that within the next year, the hybrid model of 'expensive remote LLM for planning, local LLM for execution' will become standard for companies.

hackernews · cylo · May 10, 17:19 · [Discussion](https://news.ycombinator.com/item?id=48085821)

**Background**: Local AI inference refers to running AI models directly on personal devices rather than remote cloud servers. This approach is closely related to edge computing, which brings computation closer to data sources to reduce latency and bandwidth costs. The open-weight model movement has made powerful models like Llama available for local deployment, enabling privacy-sensitive applications.

<details><summary>References</summary>
<ul>
<li><a href="https://localai.io/">LocalAI</a></li>
<li><a href="https://www.merciaai.com/post/what-is-local-ai-inference-and-why-it-might-change-how-you-use-ai">What Is Local AI Inference? (Privacy, Speed, Cost) | AI ...</a></li>
<li><a href="https://blog.starmorph.com/blog/local-llm-inference-tools-guide">Local LLM Inference in 2026: The Complete Guide to Tools ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Edge_computing">Edge computing - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The 231 comments reveal strong community engagement with diverse perspectives. Commenters draw parallels between local AI today and open source decades ago, highlighting how dependency on providers like Anthropic and OpenAI has become 'insane'. One commenter argues for separating private AI from local AI discussions, suggesting self-hosted solutions with tenant isolation could address privacy concerns. Others note user resistance to local inference, citing examples where users complain even about Chrome's lightweight local LLM using a few GB of storage.

**Tags**: `#local AI`, `#AI privacy`, `#AI infrastructure`, `#open source AI`, `#edge computing`

---

<a id="item-5"></a>
## [Fictional CVE-2024-YIKES Report Sparks Real Supply Chain Security Discussion](https://nesbitt.io/2026/02/03/incident-report-cve-2024-yikes.html) ⭐️ 6.0/10

A fictional incident report titled CVE-2024-YIKES describes a supply-chain attack targeting Rust's cargo ecosystem, including compromises of libraries like vulpine-lz4. While entirely fabricated, the report generates substantive community discussion about real software supply chain vulnerabilities and AI-assisted development security concerns. Despite being fictional, this incident report serves as effective social engineering awareness, prompting the Rust community to examine their dependency ecosystem. The discussion reveals genuine concerns about cargo's transitive dependencies and how agentic AI development may introduce new security risks. The fictional attack targets crates with existing build.rs scripts to avoid detection, including flate2, tar, curl-sys, and libgit2-sys as transitive dependencies of cargo itself. Community commenters note that this is "very good fiction" that nonetheless had them worried during initial reading, demonstrating its effectiveness at raising awareness.

hackernews · miniBill · May 10, 17:43 · [Discussion](https://news.ycombinator.com/item?id=48086082)

**Background**: Software supply chain attacks target the dependency ecosystem rather than final applications, compromising widely-used libraries to affect thousands of downstream projects. Rust's cargo uses crates.io as its primary package registry, with many crates having transitive dependencies that are rarely audited by most developers. Recent npm supply chain attacks compromising foundational packages affecting over 1 billion weekly downloads have heightened awareness of these vulnerabilities. AI-assisted development introduces additional concerns as developers increasingly rely on AI coding assistants, potentially introducing unvetted dependencies into projects.

<details><summary>References</summary>
<ul>
<li><a href="https://users.rust-lang.org/t/supply-chain-attack-scenarios/57097">Supply chain attack scenarios - The Rust Programming Language</a></li>
<li><a href="https://users.rust-lang.org/t/yet-another-npm-supply-chain-attack-is-cargo-any-safer/133766">Yet another npm supply-chain attack. Is Cargo any safer? -</a></li>
<li><a href="https://users.rust-lang.org/t/how-safe-is-crates-io/91290">How safe is crates.io? - community - The Rust Programming</a></li>

</ul>
</details>

**Discussion**: Community members appreciate the fictional report's effectiveness at raising awareness, with one commenter noting it "had me very worried during a brief scan" despite recognizing it as fiction. Technical contributors share specific cargo crates to monitor for potential compromise and express concerns about agentic AI development introducing new security risks. The discussion blends humor—lampooning YubiKey purchases from suspicious retailers—with substantive security analysis.

**Tags**: `#supply-chain-security`, `#fiction`, `#rust`, `#cargo`, `#security`

---

<a id="item-6"></a>
## [Report Exposes Chinese Grey Market Claude API Scams at 90% Discount](https://www.tomshardware.com/tech-industry/artificial-intelligence/chinese-grey-market-sells-claude-api-access-at-90-percent-off-through-proxy-networks-that-harvest-user-data) ⭐️ 6.0/10

A security report has exposed grey-market Claude API proxy services in China offering up to 90% discounts. These 'transfer station' services operate through stolen credit cards, batch-registered airdrop accounts, and by harvesting user prompts and outputs for model distillation. This report reveals significant security and fraud risks affecting developers who use third-party API services. The grey market not only involves credit card fraud but also threatens user intellectual property through model substitution and data harvesting for competitor model training. The report identifies three core fraud mechanisms: 1) Using stolen credit cards or recruiting workers from low-income countries to pass real-person verification; 2) Substituting cheaper or domestic models for premium Claude Opus; 3) Harvesting user prompts and code outputs to distill into competing AI models.

telegram · zaihuapd · May 10, 01:48

**Background**: Model distillation is a knowledge transfer technique that extracts 'knowledge' from large teacher models to train smaller student models. Claude Opus, Sonnet, and Haiku represent Anthropic's tiered model lineup with different capability and pricing levels. API proxy services, known as 'transfer stations' in Chinese developer communities, intermediate between users and official model providers.

<details><summary>References</summary>
<ul>
<li><a href="https://cloud.tencent.com/developer/article/2517760">一文读懂到底什么是“模型蒸馏（Model Distillation）”技术？-腾讯云开...</a></li>

</ul>
</details>

**Tags**: `#AI API`, `#Security Fraud`, `#Claude`, `#Data Privacy`, `#API Marketplace`

---

<a id="item-7"></a>
## [Chrome 148 Removes On-Device AI Privacy Wording, Google Claims No Behavioral Change](https://cybernews.com/ai-news/chrome-removes-ai-privacy-wording-google-says-data-still-stays-on-device/) ⭐️ 6.0/10

Chrome 148.0.7778.97 has removed the explicit statement that on-device AI data "won't be sent to Google servers" from its settings, which was present in Chrome 147. Google maintains that the actual processing behavior remains unchanged, but acknowledges that websites using Gemini Nano through Chrome can access model inputs and outputs under their own privacy policies. This change affects the privacy expectations of millions of Chrome users who rely on on-device AI for sensitive tasks. The removal of explicit wording, even without a behavioral change, raises concerns about transparency and user trust, particularly given that third-party websites can potentially access AI processing data in certain scenarios. The on-device AI feature in Chrome utilizes Google's Gemini Nano model for tasks like summarization. While Google states data processing remains local, the policy now indicates that websites integrating Gemini Nano via the Web AI API may have access to model inputs and outputs, each handling data according to their own privacy terms.

telegram · zaihuapd · May 10, 12:01

**Background**: On-device AI processes data locally on the user's device rather than sending it to remote servers, offering enhanced privacy for sensitive tasks. Gemini Nano is Google's smallest efficient AI model designed for on-device deployment. Chrome has been progressively integrating more AI capabilities, including the Prompt API for web developers to leverage on-device AI features directly in browser-based applications.

<details><summary>References</summary>
<ul>
<li><a href="https://thetechbriefs.com/google-to-give-app-devs-access-to-gemini-nano-for-on-device-ai/">Google to give app devs access to Gemini Nano for on-device AI</a></li>
<li><a href="https://arstechnica.com/google/2025/05/google-to-give-app-devs-access-to-gemini-nano-for-on-device-ai/">Google to give app devs access to Gemini Nano for on-device AI</a></li>
<li><a href="https://digitechbytes.com/emerging-consumer-tech-explained/on-device-ai-vs-cloud-ai/">On‑Device AI Vs Cloud AI: Differences Explained - Digitech Bytes</a></li>

</ul>
</details>

**Tags**: `#browser-privacy`, `#chrome`, `#google-ai`, `#gemini-nano`, `#on-device-ai`

---