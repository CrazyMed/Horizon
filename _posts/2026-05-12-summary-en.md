---
layout: default
title: "Horizon Daily: 2026-05-12"
date: 2026-05-12
lang: en
---

> From 35 items, 16 important content pieces were selected

---

1. [TanStack npm Supply Chain Attack Exposes Dead-Man's Switch](#item-1) ⭐️ 9.0/10
2. [Nvidia Releases Official Rust-to-CUDA Compiler CUDA-oxide](#item-2) ⭐️ 8.0/10
3. [Software engineering may no longer be a lifetime career](#item-3) ⭐️ 8.0/10
4. [UCLA Discovers First Stroke Rehabilitation Drug to Repair Brain Damage](#item-4) ⭐️ 7.0/10
5. [GitLab Lays Off Staff, Replaces CREDIT Values with AI-Focused Priorities](#item-5) ⭐️ 7.0/10
6. [AI Coding Agents Must Cut Maintenance Costs, James Shore Argues](#item-6) ⭐️ 7.0/10
7. [Intel Optane PMem Build Runs Trillion-Parameter MoE Model Locally](#item-7) ⭐️ 7.0/10
8. [MiniCPM 4.6: Efficient Open-Source Multimodal Vision-Language Model Released](#item-8) ⭐️ 7.0/10
9. [Fake OpenAI Privacy Filter Repo Tops Hugging Face Trending](#item-9) ⭐️ 7.0/10
10. [Ratty Terminal Emulator Brings Inline 3D Graphics to CLI](#item-10) ⭐️ 6.0/10
11. [Gmail Requires QR Code and SMS for New Account Signup](#item-11) ⭐️ 6.0/10
12. ["Zombie Internet" Concept Highlights AI Content Pollution Crisis](#item-12) ⭐️ 6.0/10
13. [Using LLM as Script Shebang for Natural Language Execution](#item-13) ⭐️ 6.0/10
14. [Shopify's River: Public Slack Coding Agent for Learning](#item-14) ⭐️ 6.0/10
15. [Qwen 3.6 35B A3B Shows Strong Long Context Code Understanding](#item-15) ⭐️ 6.0/10
16. [GrapheneOS Criticizes Google and Apple Device Verification Restrictions](#item-16) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [TanStack npm Supply Chain Attack Exposes Dead-Man's Switch](https://tanstack.com/blog/npm-supply-chain-compromise-postmortem) ⭐️ 9.0/10

TanStack released a postmortem detailing how their npm packages were compromised through a sophisticated supply-chain attack that exploited Trusted Publishing pipelines. The malware installs a dead-man's switch that monitors GitHub tokens and, if revoked, triggers rm -rf ~/. to destroy user data, while also spreading to other packages like mistralai/mistralai. This incident demonstrates that Trusted Publishing alone cannot prevent supply-chain attacks when CI/CD pipelines are compromised, and introduces a dangerous new attack pattern where malware punishes security responses. Developers who revoke compromised tokens risk triggering data destruction on their own systems. The dead-man's switch is installed as a systemd user service (Linux) or LaunchAgent (macOS) at ~/.local/bin/gh-token-monitor.sh, polling api.github.com/user every 60 seconds. If the token returns a 40x error, it executes rm -rf ~/. to delete the user's home directory. The attack exploited orphan commits in forks, leveraging GitHub's shared object storage where fork commits are reachable at URIs indistinguishable from the legitimate repo.

hackernews · varunsharma07 · May 11, 21:08 · [Discussion](https://news.ycombinator.com/item?id=48100706)

**Background**: Trusted Publishing is an npm feature using OpenID Connect (OIDC) that creates a trust relationship between npm and CI/CD providers, enabling secure package publishing directly from workflows without long-lived tokens. Supply chain attacks target software distribution channels by compromising packages, dependencies, or build processes to inject malicious code. The 'dead-man's switch' is a mechanism that activates harmful actions (like data destruction) when a specific condition is met—in this case, token revocation—creating a deterrent against security responses.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.npmjs.com/trusted-publishers/">Trusted publishing for npm packages | npm Docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Dead_man's_switch">Dead man's switch - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community members highlight critical concerns: Trusted Publishing is not sufficient by itself since CI compromise can still lead to malicious publishes; postinstall scripts remain a dangerous attack vector that should be reconsidered; and GitHub's architecture allowing fork commits to be reachable via the same storage as legitimate repos is considered a fundamental flaw. Some suggest pnpm as a safer alternative and emphasize the need for package managers to block orphan commits from forks.

**Tags**: `#supply-chain-security`, `#npm`, `#security-incident`, `#trusted-publishing`, `#open-source-security`

---

<a id="item-2"></a>
## [Nvidia Releases Official Rust-to-CUDA Compiler CUDA-oxide](https://nvlabs.github.io/cuda-oxide/index.html) ⭐️ 8.0/10

Nvidia released CUDA-oxide 0.1 on May 9, 2026, an experimental compiler that compiles Rust code directly to PTX (Parallel Thread Execution) assembly, enabling developers to write CUDA SIMT GPU kernels in idiomatic Rust without C++, DSLs, or foreign function interfaces. This marks Nvidia's first official Rust-to-CUDA compiler, bringing Rust's memory safety guarantees to GPU computing while potentially replacing slower build workflows that rely on CMake or nvcc. The combination of Rust's safety features and CUDA's ecosystem could make GPU development more accessible and less error-prone. CUDA-oxide targets PTX directly rather than higher-level IRs like NVIDIA's MLIR or Tile IR, which some community members noted as a design choice worth reconsidering. The compiler is currently experimental, and questions remain about how Rust's ownership model maps to CUDA's memory semantics in practice.

hackernews · adamnemecek · May 11, 15:55 · [Discussion](https://news.ycombinator.com/item?id=48096692)

**Background**: PTX is Nvidia's low-level virtual instruction set architecture that sits between high-level CUDA code and actual GPU machine code. CUDA SIMT (Single Instruction, Multiple Threads) is the execution model where groups of threads execute the same program in lockstep, which is fundamental to GPU parallelism. Most existing Rust CUDA solutions rely on bindings to C++ libraries or nvcc, creating additional compilation overhead.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/NVlabs/cuda-oxide">CUDA-oxide an experimental Rust-to-CUDA compiler - GitHub</a></li>
<li><a href="https://www.marktechpost.com/2026/05/09/nvidia-ai-just-released-cuda-oxide-an-experimental-rust-to-cuda-compiler-backend-that-compiles-simt-gpu-kernels-directly-to-ptx/">NVIDIA AI Just Released cuda-oxide: An Experimental Rust-to ...</a></li>
<li><a href="https://byteiota.com/nvidia-cuda-oxide-official-rust-to-cuda-compiler-released/">NVIDIA CUDA-Oxide: Official Rust-to-CUDA Compiler Released</a></li>

</ul>
</details>

**Discussion**: Community members expressed excitement about the potential as a drop-in replacement, though concerns were raised about build times and how Rust's memory model would map to CUDA semantics. Some commenters noted that targeting MLIR or Tile IR instead of PTX could offer advantages like easier optimization and better epilogue fusion. There was also curiosity about how this development affects projects like Slang and Nvidia's broader language strategy.

**Tags**: `#rust`, `#cuda`, `#gpu-programming`, `#compilers`, `#nvidia`

---

<a id="item-3"></a>
## [Software engineering may no longer be a lifetime career](https://www.seangoedecke.com/software-engineering-may-no-longer-be-a-lifetime-career/) ⭐️ 8.0/10

Hacker News上的一场讨论引发了关于AI是否会使软件工程成为不可持续职业的辩论，共收到589条评论和352个点赞，观点从末日论到AI增强论不一而足。 这场讨论触及了数百万软件工程师的职业未来，以及AI对技术行业劳动力市场的潜在影响，随着企业采取观望态度，招聘信号正在减弱。 评论者指出了一个关键区分：使用AI增强推理能力的工程师与用AI替代推理能力的工程师之间存在差异；此外，年长且经验丰富的工程师（40岁以上）如果愿意使用尖端工具，实际上可能比以往更有效率。

hackernews · movis · May 11, 14:34 · [Discussion](https://news.ycombinator.com/item?id=48095550)

**Background**: 软件工程涉及理解需求、设计解决方案和编写代码等多个环节，LLM等AI工具可以协助代码生成。研究表明，传统程序员的技能会随着年龄增长而退化，部分原因是深度计算能力的下降，这在某种程度上类似于国际象棋中经验丰富的棋手虽然理解更深入，但计算精力有限的现象。

**Discussion**: 社区讨论呈现两极分化：有人认为AI将使开发者变得无关紧要，因为LLM可以写代码；也有人反驳说软件开发只有2-5%的时间用于实际编码，其余时间用于理解问题和制定解决方案。一位用户强调，技能萎缩的担忧是真实的，但仅限于那些用AI替代推理而非增强推理的人；另一位则观察到美国软件招聘市场今年初发生了实质性变化，企业普遍采取了观望态度以避免过度投资人力资本。

**Tags**: `#software-engineering-career`, `#ai-impact-on-jobs`, `#developer-productivity`, `#skill-atrophy`, `#ai-tools`

---

<a id="item-4"></a>
## [UCLA Discovers First Stroke Rehabilitation Drug to Repair Brain Damage](https://stemcell.ucla.edu/news/ucla-discovers-first-stroke-rehabilitation-drug-repair-brain-damage) ⭐️ 7.0/10

UCLA researchers have announced the discovery of the first stroke rehabilitation drug capable of repairing brain damage by targeting disconnected neural networks rather than dead cells, with the compound identified as https://pubmed.ncbi.nlm.nih.gov/39106304/. The study, led by Dr. S. Thomas Carmichael, aims to create a medicine that produces the effects of rehabilitation for stroke patients who cannot sustain the intensity of traditional therapy. This breakthrough represents a paradigm shift in stroke treatment by addressing network disconnection rather than cell death, potentially enabling recovery for millions of stroke survivors who plateau under current rehabilitation limitations. If successful, this drug could dramatically expand the therapeutic window and effectiveness of stroke recovery. The drug targets the disconnection and lost rhythm in surviving, distant networks rather than attempting to recover function from dead cells at the infarct center—currently considered an impossible intervention. Current rehabilitation requires sustained intensity that most patients cannot maintain, limiting recovery outcomes.

hackernews · bookofjoe · May 11, 17:53 · [Discussion](https://news.ycombinator.com/item?id=48098261)

**Background**: Stroke causes brain cell death in the affected area (infarct), but neurologists have long observed that 'bruised' brain cells surrounding the damage can recover function over weeks, months, or even years. Post-stroke disconnection and secondary degeneration are major factors impacting impairment and recovery, suggesting that network plasticity—the brain's ability to rewire connections—plays a critical role beyond replacing dead neurons. Cell-based therapies have traditionally aimed to replace dead cells, but this new approach focuses on restoring communication in surviving networks.

<details><summary>References</summary>
<ul>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC6603430/">Brain networks and their relevance for stroke rehabilitation - PMC</a></li>

</ul>
</details>

**Discussion**: Community comments highlight the scientific nuance distinguishing cell death from network disconnection as recovery targets, with users noting this cannot recover function from dead cells at the infarct center. One commenter drew a literary connection to Ted Chiang's short story 'Understand,' while others raised questions about potential applications to other neurodegenerative diseases. The specific compound (PMID 39106304) was shared for those wanting to explore the research directly.

**Tags**: `#medical-research`, `#stroke-rehabilitation`, `#neuroscience`, `#drug-discovery`, `#brain-repair`

---

<a id="item-5"></a>
## [GitLab Lays Off Staff, Replaces CREDIT Values with AI-Focused Priorities](https://about.gitlab.com/blog/gitlab-act-2/) ⭐️ 7.0/10

GitLab announced a workforce reduction and unveiled "GitLab Act 2," replacing its six CREDIT values (Collaboration, Results for Customers, Efficiency, Diversity Inclusion & Belonging, Iteration, and Transparency) with three new operating principles: Speed with Quality, Ownership Mindset, and Customer Outcomes. The company framed this as a strategic pivot to capture opportunities in the "agentic era" driven by AI agents. This move represents a notable trend in the tech industry where companies are abandoning progressive workplace values in favor of efficiency-focused AI strategies. GitLab's decision to eliminate Diversity, Inclusion & Belonging (DIB) from its core values signals a broader rollback of progressive policies across the sector, while the framing around "agentic era" suggests companies are increasingly betting on AI automation to justify workforce reductions. GitLab's stock price dropped approximately 50% over the past year, from around $52 to $26, which likely contributed to investor pressure for restructuring. The company claims the "agentic era" presents its "largest opportunity in history," yet paradoxically requires fewer resources to achieve this goal. Community critics have pointed out the logical inconsistency and the heavy reliance on AI buzzwords in the announcement.

hackernews · AnonGitLabEmpl · May 11, 20:51 · [Discussion](https://news.ycombinator.com/item?id=48100500)

**Background**: GitLab's CREDIT framework was introduced as a condensed set of company values, with each letter representing a core principle: Collaboration, Results for Customers, Efficiency, Diversity Inclusion & Belonging, Iteration, and Transparency. These values were designed to be memorable and guide employee behavior. The "agentic era" refers to a proposed technological shift where AI agents autonomously perform complex tasks, which companies like GitLab claim will increase demand for software development tools.

<details><summary>References</summary>
<ul>
<li><a href="https://handbook.gitlab.com/handbook/values/">GitLab Values - The GitLab Handbook</a></li>
<li><a href="https://news.ycombinator.com/item?id=48100500">GitLab announces workforce reduction and end of their CREDIT ...</a></li>
<li><a href="https://www.edgen.tech/news/post/gitlab-restructures-for-ai-era-reinvesting-savings-from-cuts">GitLab Restructures for AI Era, Reinvesting Savings From Cuts</a></li>

</ul>
</details>

**Discussion**: Community response is overwhelmingly critical. Commenters note the irony that GitLab claims to need fewer resources for its "largest opportunity ever," and mock the heavy use of AI buzzwords as transparent investor placation. The replacement of DEI principles with efficiency-focused values drew particular scrutiny, with one commenter summarizing the new direction as "work harder, not smarter, and no more DEI." Others speculated the announcement is primarily designed to reassure investors worried that AI might reduce demand for software development tools.

**Tags**: `#layoffs`, `#company-culture`, `#AI-industry`, `#tech-industry`, `#workforce-reduction`

---

<a id="item-6"></a>
## [AI Coding Agents Must Cut Maintenance Costs, James Shore Argues](https://simonwillison.net/2026/May/11/james-shore/#atom-everything) ⭐️ 7.0/10

Software engineer James Shore argues that AI coding agents must reduce maintenance costs in exact proportion to how much faster they make code generation. He presents a mathematical framework where doubling code output requires halving maintenance costs—otherwise developers face exponentially increased long-term burden. This argument challenges the prevailing assumption that AI coding tools are valuable simply because they increase development speed. The framework provides engineering teams with a concrete mathematical model for evaluating AI tooling ROI, offering a contrarian perspective that could reshape how organizations assess their AI investments. Shore's core insight is that maintenance costs multiply with code volume: if you double your output while maintenance costs stay constant, your total maintenance burden still doubles; only by halving per-unit maintenance costs can you break even. He frames this as a choice between temporary speed boosts and permanent maintainability.

rss · Simon Willison · May 11, 19:48

**Background**: Software maintenance typically consumes 40-80% of total development costs and tends to grow as codebases expand. AI coding agents like GitHub Copilot have dramatically accelerated code generation, but they often produce code that requires additional testing, debugging, and refactoring—potentially offsetting the productivity gains they provide.

**Tags**: `#AI coding tools`, `#software maintenance`, `#developer productivity`, `#technical debt`, `#engineering economics`

---

<a id="item-7"></a>
## [Intel Optane PMem Build Runs Trillion-Parameter MoE Model Locally](https://i.redd.it/na7zo7lmck0h1.jpeg) ⭐️ 7.0/10

A Reddit user built a computer using 768GB of secondhand Intel Optane Persistent Memory modules to run a 1 trillion parameter mixture-of-experts model (Kimi K2.5) locally at approximately 4 tokens per second, using llama.cpp with hybrid GPU/CPU inference. This build demonstrates a cost-effective method for running extremely large language models locally by leveraging cheap discontinued Optane PMem as a large-capacity RAM alternative, potentially making trillion-parameter models accessible to hobbyists and researchers without enterprise budgets. The build uses Optane PMem in Memory Mode, where the persistent memory acts as system RAM while existing DRAM sticks serve as a cache layer. The dense components (attention weights, shared experts, routing) fit on a 12GB GPU via llama.cpp's override-tensor flag, while sparse expert weights reside on the 768GB PMem.

reddit · r/LocalLLaMA · APFrisco · May 11, 19:54 · [Discussion](https://www.reddit.com/r/LocalLLaMA/comments/1taeg8h/computer_build_using_intel_optane_persistent/)

**Background**: Intel Optane Persistent Memory (PMem) was a data-center memory technology discontinued in 2022 that bridges the gap between DRAM and SSDs, offering higher capacity than DRAM at lower cost. Mixture-of-Experts (MoE) models use a sparse architecture where only selected 'expert' sub-networks activate for each input, allowing trillion-parameter scale while keeping active computation manageable. llama.cpp is an efficient CPU/GPU inference engine for LLM models.

<details><summary>References</summary>
<ul>
<li><a href="https://www.intel.com/content/www/us/en/content-details/841964/intel-optane-persistent-memory-start-up-guide.html">Intel® Optane™ Persistent Memory Start Up Guide</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>

</ul>
</details>

**Discussion**: The r/LocalLLaMA community showed strong interest with 362 upvotes, with users praising the innovative use of discontinued Optane PMem for cost-effective large model hosting. Discussion focused on potential alternatives, memory bandwidth limitations, and whether similar results could be achieved with standard hardware.

**Tags**: `#local-llm-inference`, `#intel-optane`, `#hardware-build`, `#mixture-of-experts`, `#model-hosting`

---

<a id="item-8"></a>
## [MiniCPM 4.6: Efficient Open-Source Multimodal Vision-Language Model Released](https://huggingface.co/openbmb/MiniCPM-V-4.6) ⭐️ 7.0/10

MiniCPM 4.6, an efficient open-source multimodal vision-language model developed by Tsinghua University's OpenBMB lab, has been released on HuggingFace with strong community reception. Built on SigLip-400M and MiniCPM-2.4B with a perceiver resampler, the model achieves over 50% reduction in visual encoding computation FLOPs, making it competitive with even smaller models in efficiency. This release represents a significant step in making AI more accessible by enabling advanced vision-language capabilities on consumer-grade hardware including personal computers and mobile devices. The combination of strong performance with low computational requirements addresses a key barrier to widespread AI adoption. MiniCPM-V 4.6 is based on LLaVA-UHD architecture and can process high-resolution images with any aspect ratio, supporting up to 1.8 million pixels. The 1.3B parameter model is released under Apache 2.0 license and achieves better efficiency than comparable models while maintaining competitive benchmark performance.

reddit · r/LocalLLaMA · themrzmaster · May 11, 17:08 · [Discussion](https://www.reddit.com/r/LocalLLaMA/comments/1ta9k8o/minicpm_46/)

**Background**: OpenBMB (Open Lab for Big Model Base) is a China-based research lab jointly founded in 2022 by Tsinghua University's NLP Lab and ModelBest Inc., with the goal of building foundation models and systems towards AGI. Vision-language models (VLMs) are multimodal AI systems capable of understanding and processing video, images, and text simultaneously, generating text outputs based on visual and textual inputs. The LLaVA-UHD architecture optimizes visual token usage, significantly reducing computational overhead compared to traditional approaches.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/openbmb/MiniCPM-V">openbmb/MiniCPM-V · Hugging Face</a></li>
<li><a href="https://github.com/OpenBMB/MiniCPM-V">GitHub - OpenBMB/MiniCPM-V: A Pocket-Sized MLLM for Ultra-Efficient Image and Video Understanding on Your Phone · GitHub</a></li>
<li><a href="https://artificialanalysis.ai/articles/openbmb-launches-minicpm-v-4-6-1-3b-instruct">OpenBMB launches MiniCPM-V 4.6 1.3B Instruct</a></li>

</ul>
</details>

**Discussion**: The release has received strong validation from the AI community with 89 upvotes on r/LocalLLaMA, indicating high practical interest. Community members have shared benchmarks and deployment experiences, with discussions highlighting the model's accessibility for local deployment and its suitability for resource-constrained environments.

**Tags**: `#open-source AI`, `#multimodal LLM`, `#efficient models`, `#MiniCPM`, `#vision-language models`

---

<a id="item-9"></a>
## [Fake OpenAI Privacy Filter Repo Tops Hugging Face Trending](https://thehackernews.com/2026/05/fake-openai-privacy-filter-repo-hits-1.html) ⭐️ 7.0/10

A malicious Hugging Face repository impersonating OpenAI's privacy filter model distributed Rust-based info-stealing malware after reaching the platform's trending #1 spot, accumulating approximately 244,000 downloads and 667 likes with potentially manipulated engagement metrics. This incident represents a significant supply chain attack targeting the AI/ML community, demonstrating how threat actors exploit trust in popular open-source platforms and manipulate engagement metrics to maximize spread of malware. HiddenLayer discovered six similar malicious repositories, all linked to infrastructure that previously distributed ValleyRAT remote access trojan, with overlaps in attack infrastructure connecting to the Silver Fox hacker group based in China.

telegram · zaihuapd · May 11, 12:51

**Background**: Hugging Face is a leading platform for sharing AI/ML models, similar to GitHub for software developers, making it an attractive target for supply chain attacks. Privacy filters are tools that detect and remove sensitive information like credit card numbers or personal identifiers from AI model outputs. ValleyRAT is a remote access trojan first identified in 2023 that provides unauthorized remote control over infected systems. The Silver Fox threat group, active since at least 2022 and based in China, has evolved from financial crime to potential APT espionage operations targeting South Asian entities.

<details><summary>References</summary>
<ul>
<li><a href="https://www.zscaler.com/blogs/security-research/technical-analysis-latest-variant-valleyrat">New Updates to ValleyRAT | ThreatLabz - Zscaler</a></li>
<li><a href="https://www.s2w.inc/en/resource/detail/1050">Threat Group Profile: Silver Fox</a></li>
<li><a href="https://thehackernews.com/2026/05/silver-fox-deploys-abcdoor-malware-via.html">Silver Fox Deploys ABCDoor Malware via Tax-Themed Phishing in ...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#supply-chain-attack`, `#hugging-face`, `#malware`, `#ai-security`

---

<a id="item-10"></a>
## [Ratty Terminal Emulator Brings Inline 3D Graphics to CLI](https://ratty-term.org/) ⭐️ 6.0/10

Ratty is a GPU-rendered terminal emulator that enables inline 3D graphics rendering, featuring a spinning rat cursor and multiple 3D presentation modes. Built with Rust, Ratatui, and Bevy, it extends traditional terminal output beyond text to include interactive 3D graphics. This project challenges the assumption that terminals should only display text, pushing the boundaries of what CLI tools can achieve. It has implications for data visualization, developer tooling, and the future evolution of terminal interfaces, with potential applications in scientific computing and interactive debugging. Ratty currently uses ratatui for the UI buffer, parley_ratatui for text shaping and rendering, and Bevy for 3D scene presentation. It is inspired by TempleOS and represents an experimental approach to extending terminal capabilities. Alternative approaches include the kitty protocol and sixel graphics, which are supported in modern terminals like Kitty.

hackernews · orhunp_ · May 11, 10:13 · [Discussion](https://news.ycombinator.com/item?id=48093100)

**Background**: Terminal emulators traditionally render only text-based output, but modern GPU-accelerated terminals like Kitty and Ghostty have expanded capabilities to include image display and advanced features. Existing standards like the kitty protocol and sixel enable inline graphics in compatible terminals. Historically, systems like Xerox workstations demonstrated inline graphics capabilities as early as 1981, predating many modern implementations.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/orhun/ratty">GitHub - orhun/ratty: A GPU- rendered terminal emulator with inline...</a></li>
<li><a href="https://ratty-term.org/">Ratty — A GPU- rendered terminal emulator with inline 3D graphics</a></li>

</ul>
</details>

**Discussion**: Community response has been largely positive, with discussions drawing historical parallels to Xerox workstations' inline graphics from 1981 and Lisp machines' REPL experiences. Commenters compare this to the evolution of data science notebooks, with one noting Kitty is 'probably the most aggressive innovator' in this space. Some discuss potential applications in shallow-3D UIs for software development to reduce vergence-accommodation conflict eye strain.

**Tags**: `#terminal-emulator`, `#3d-graphics`, `#open-source`, `#unix-tools`, `#gui-innovation`

---

<a id="item-11"></a>
## [Gmail Requires QR Code and SMS for New Account Signup](https://discuss.privacyguides.net/t/google-account-registration-now-requires-sending-an-sms-via-phone-instead-of-receiving-an-sms/36082) ⭐️ 6.0/10

Google has updated Gmail account registration to require users to scan a QR code with their smartphone and send an SMS message to verify their phone number, replacing the previous approach of receiving an SMS code. This change affects billions of Gmail users worldwide and raises significant privacy concerns since phone number verification is now mandatory, potentially excluding users who want to maintain anonymity or lack mobile access. Scanning the QR code opens a pre-filled SMS composer rather than automatically sending a message; users must manually send the text. Google appears to be implementing this as a measure to combat spam and reduce bot account creation on its platform.

hackernews · negura · May 11, 07:26 · [Discussion](https://news.ycombinator.com/item?id=48092028)

**Background**: Gmail has over 1.8 billion active users worldwide, making it one of the most widely used email services. Phone verification has become increasingly common among major internet platforms as a tool to reduce spam, fraud, and automated account creation. However, critics argue that mandatory phone verification creates friction for users concerned about privacy and potentially discriminates against those without mobile phones.

**Discussion**: The Hacker News discussion revealed mixed sentiment. Some users acknowledged Google's challenge of maintaining massive free email infrastructure while battling spam, calling it an 'expensive, complicated' burden. Technical users clarified that the QR code merely opens an SMS composer rather than automatically sending texts. Others raised anti-monopoly concerns, arguing that tying services like Gmail, Recaptcha, and Android together gives Google unfair competitive advantages, and that Gmail should compete independently on its own merits.

**Tags**: `#google`, `#privacy`, `#email`, `#spam-prevention`, `#user-authentication`

---

<a id="item-12"></a>
## ["Zombie Internet" Concept Highlights AI Content Pollution Crisis](https://simonwillison.net/2026/May/11/zombie-internet/#atom-everything) ⭐️ 6.0/10

Simon Willison highlights Jason Koebler's "Your AI Use Is Breaking My Brain" article, introducing the "Zombie Internet" concept to describe the increasingly unavoidable problem of AI-generated content distorting online discourse and human writing styles. This concept provides a more nuanced framework than the "Dead Internet" theory for understanding how AI and humans interact online, capturing the exhausting mental labor of distinguishing human-generated content from AI output. Unlike the Dead Internet theory (bots talking to bots), the Zombie Internet encompasses a spectrum of interactions: humans using AI talking to non-AI users, people creating AI agents to interact with others, and influencer hustlebros building automated YouTube channels and blogs for profit.

rss · Simon Willison · May 11, 19:21

**Background**: The "Dead Internet" theory, which surfaced around 2021, proposes that large portions of the web are driven by autonomous bots rather than humans. Koebler's "Zombie Internet" concept refines this by describing a hybrid state where real humans still participate but are increasingly forced to interact with, filter out, or compete against AI-generated content. Platforms like Facebook and LinkedIn have been particularly affected by AI-generated spam and bot accounts.

<details><summary>References</summary>
<ul>
<li><a href="https://www.404media.co/facebooks-ai-spam-isnt-the-dead-internet-its-the-zombie-internet/">Facebook’s AI Spam Isn’t the ‘Dead Internet’: It’s the Zombie ...</a></li>
<li><a href="https://techwontsave.us/episode/227_facebook_is_the_zombie_internet_w_jason_koebler">Facebook Is the Zombie Internet w/ Jason Koebler - Episodes ...</a></li>

</ul>
</details>

**Tags**: `#AI ethics`, `#content authenticity`, `#internet culture`, `#LLMs impact`, `#digital communication`

---

<a id="item-13"></a>
## [Using LLM as Script Shebang for Natural Language Execution](https://simonwillison.net/2026/May/11/llm-shebang/#atom-everything) ⭐️ 6.0/10

Simon Willison demonstrated using the LLM CLI tool directly in a script's shebang line (#!/usr/bin/env -S llm -f) to execute natural language instructions as executable scripts, showing basic prompts, tool calls with -T options, and YAML templates defining Python functions. This technique blurs the line between natural language and executable code, enabling users to write shell scripts in plain English and leverage LLM tool-calling directly from the command line without explicit wrapper scripts. The approach uses GNU env -S to pass multiple arguments in the shebang; -f reads prompts from a file fragment, -T enables specific tools like llm_time, and -t supports YAML templates with inline Python function definitions for custom tool use.

rss · Simon Willison · May 11, 18:48

**Background**: In Unix-like systems, a shebang (#!) at the start of a script tells the operating system which interpreter to use. The LLM CLI tool, built by Simon Willison and part of the Datasette project, provides command-line access to large language models with support for tools and function calling. The -S flag in GNU env allows multiple arguments in shebang lines, which Unix traditionally limits to a single argument after the interpreter path.

<details><summary>References</summary>
<ul>
<li><a href="https://llm.datasette.io/en/stable/fragments.html">Fragments - LLM - Datasette</a></li>
<li><a href="https://simonwillison.net/2025/May/27/llm-tools/">Large Language Models can run tools in your terminal with LLM 0.26</a></li>
<li><a href="https://github.com/simonw/llm">simonw/ llm : Access large language models from the command - line ...</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters observed that this technique essentially allows putting a shebang on an English text file, raising interesting questions about the evolving nature of executable code. The discussion highlighted the creative potential of treating natural language itself as a programmable interface.

**Tags**: `#llm`, `#shell-scripting`, `#productivity`, `#cli-tools`, `#ai-automation`

---

<a id="item-14"></a>
## [Shopify's River: Public Slack Coding Agent for Learning](https://simonwillison.net/2026/May/11/learning-on-the-shop-floor/#atom-everything) ⭐️ 6.0/10

Shopify CEO Tobias Lütke reveals that their internal AI coding agent 'River' operates exclusively in public Slack channels, declining all direct messages and requiring users to create public channels for collaboration. This approach transforms AI coding assistance from a private tool into a collective learning system, embodying the German concept 'Lehrwerkstatt' where the entire workspace becomes a classroom for osmotic knowledge transfer. River's design mandates that all AI-assisted coding occurs publicly, enabling any employee to search, observe, and contribute to ongoing work. This transparency aligns with Shopify's core value of continuous learning, where visibility itself becomes the curriculum.

rss · Simon Willison · May 11, 15:46

**Background**: The 'Lehrwerkstatt' concept, literally meaning 'teaching workshop' in German, describes an environment where learning occurs through proximity to actual work rather than formal instruction. Simon Willison draws a parallel to Midjourney's early success, where public Discord channels forced users to share prompts and learn from each other's experiments. Lütke's own #tobi_river channel reportedly has over 100 participants who react to threads, add context, assist with reviews, and learn by observation.

**Discussion**: Simon Willison highlights this as a novel organizational pattern for AI tools, noting that River embodies a collaborative rather than individualistic approach to AI-assisted development. The comparison to Midjourney's community-driven learning suggests this public-by-default design could become a model for how organizations deploy AI coding assistants.

**Tags**: `#AI coding assistants`, `#organizational practices`, `#Shopify`, `#collaborative learning`, `#software engineering culture`

---

<a id="item-15"></a>
## [Qwen 3.6 35B A3B Shows Strong Long Context Code Understanding](https://www.reddit.com/r/LocalLLaMA/comments/1t9whrt/the_qwen_36_35b_a3b_hype_is_real/) ⭐️ 6.0/10

A Reddit user tested Qwen 3.6 35B A3B alongside other small local models (Qwen 3.6 27B, Gemma 4 26B A4B, Nemotron 3 Nano) on their academic research code, finding that all models could comprehend niche academic code significantly better when fed entire papers with accompanying code. This demonstrates that recent architectural advances in small local models have reached a practical threshold where they can handle real-world specialized tasks requiring long context understanding, potentially making them viable alternatives to larger models for domain-specific applications. The tested models employed three key architectural techniques: Gated DeltaNet (which combines Mamba's forgetting capability with DeltaNet's writing precision), hybrid Mamba2 layers with transformer attention, and sliding window attention. The user noted that fitting long contexts required more than 32GB of VRAM.

reddit · r/LocalLLaMA · The_Paradoxy · May 11, 07:51

**Background**: Long context capabilities allow LLMs to process entire documents rather than truncated snippets, but historically, small models struggled with extended contexts due to memory and attention constraints. Gated DeltaNet is a newer architecture that improves on Mamba2 by implementing delta update rules for precise memory control. Hybrid architectures combining Mamba2 state space models with traditional transformer attention aim to balance efficiency with flexible relational modeling, while sliding window attention limits each token to attending only within a local window, reducing computational costs.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2412.06464">Gated Delta Networks : Improving Mamba2 with Delta Rule</a></li>
<li><a href="https://kyouma45.medium.com/gated-attention-deltanets-the-missing-link-for-long-context-ai-bbabb2260461">Gated Attention & DeltaNets : The Missing Link for... | Medium</a></li>
<li><a href="https://sebastianraschka.com/llms-from-scratch/ch04/06_swa/">Sliding Window Attention (SWA) | Sebastian Raschka, PhD</a></li>

</ul>
</details>

**Discussion**: The post received 342 upvotes, indicating moderate interest in the LocalLLaMA community. Users appeared enthusiastic about the practical implications, with the original poster expressing hope that Mistral would release a new small model incorporating gated delta net architecture, believing it could surpass current leaders.

**Tags**: `#local-llm`, `#qwen`, `#long-context`, `#model-evaluation`, `#open-weight-models`

---

<a id="item-16"></a>
## [GrapheneOS Criticizes Google and Apple Device Verification Restrictions](https://www.androidauthority.com/grapheneos-google-apple-approved-devices-web-warning-3665319/) ⭐️ 6.0/10

GrapheneOS has publicly criticized Google and Apple for using device verification APIs—including Play Integrity API, App Attest, and reCAPTCHA—that restrict app and website access to approved devices, effectively excluding legitimate alternative operating systems like GrapheneOS from normal functionality. This criticism highlights a growing tension between platform security measures and user freedom in the mobile ecosystem. If device verification systems continue to exclude alternative operating systems, users seeking enhanced privacy through custom ROMs may find themselves locked out of essential apps and services, undermining the broader goal of a diverse and competitive mobile OS landscape. According to GrapheneOS, Play Integrity API actively excludes alternative Android implementations including GrapheneOS itself, while reCAPTCHA in certain scenarios requires users to verify through certified Android or iOS devices. Neither Google nor Apple has publicly responded to these accusations as of the report date.

telegram · zaihuapd · May 11, 07:41

**Background**: GrapheneOS is a privacy and security-focused custom Android ROM (alternative operating system) built on the Android Open Source Project (AOSP) that runs on Google Pixel devices. Device verification APIs like Play Integrity API and App Attest are security mechanisms that apps and services use to confirm whether a device and its software environment are legitimate and uncompromised—typically by checking for certified bootloader states and verified boot signatures. These APIs were primarily designed to prevent fraud and piracy but have the side effect of blocking devices running unofficial operating systems.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.android.com/google/play/integrity">Play Integrity API | Android Developers</a></li>
<li><a href="https://developer.apple.com/documentation/devicecheck">DeviceCheck | Apple Developer Documentation</a></li>

</ul>
</details>

**Tags**: `#mobile-security`, `#alternative-os`, `#platform-verification`, `#privacy`, `#android-ecosystem`

---