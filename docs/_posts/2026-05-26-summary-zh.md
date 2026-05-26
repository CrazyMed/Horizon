---
layout: default
title: "Horizon 每日速递: 2026-05-26"
date: 2026-05-26
lang: zh
---

> 从 16 条内容中筛选出 7 条重要资讯

---

1. [微软 Copilot Cowork 漏洞引发文件窃取风险](#item-1) ⭐️ 7.0/10
2. [教皇利奥十四发布关于技术伦理与人类尊严的通谕](#item-2) ⭐️ 7.0/10
3. [Grok V9-Medium 训练完成，预计 2-3 周后发布](#item-3) ⭐️ 7.0/10
4. [离体人脑用于药物测试 伦理争议随之而来](#item-4) ⭐️ 7.0/10
5. [Mullvad VPN 部署出口 IP 指纹识别缓解措施](#item-5) ⭐️ 6.0/10
6. [Epic 公布虚幻引擎 6，Rocket League 为首个展示游戏](#item-6) ⭐️ 6.0/10
7. [腾讯 ima copilot 全量开放，主打四模块常驻记忆系统](#item-7) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [微软 Copilot Cowork 漏洞引发文件窃取风险](https://www.promptarmor.com/resources/microsoft-copilot-cowork-exfiltrates-files) ⭐️ 7.0/10

PromptArmor 的安全研究人员展示了一种针对微软 Copilot Cowork"技能"功能的提示词注入攻击，该攻击可被利用来窃取企业用户系统中的敏感文件。 随着微软 Copilot 在企业中快速部署以提高生产力，此漏洞凸显了在工作场所工具中集成 AI 代理时，未能充分防范提示词注入攻击的安全风险，可能导致大量企业数据泄露。 该攻击利用 Copilot Cowork 的技能系统，通过嵌入恶意指令来指示 AI 访问并传输文件到外部服务器。虽然提示词注入本身并非新型攻击向量，但针对 Copilot Cowork 技能架构的特定利用方式使这成为企业部署的针对性问题。

hackernews · Kneenex · 05月25日 21:45 · [社区讨论](https://news.ycombinator.com/item?id=48272354)

**背景**: 提示词注入是一种网络安全攻击技术，通过在输入中插入恶意指令来劫持 AI 模型的行为。微软 Copilot Cowork 是一款企业级 AI 助手，允许用户创建"技能"——即扩展 AI 功能的自定义程序。技能可以通过底层 LLM 处理各种任务，但这种灵活性也创造了攻击面，如果恶意指令被注入到技能定义或用户输入中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://www.ibm.com/think/topics/prompt-injection">What Is a Prompt Injection Attack? | IBM</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：一些评论者认为文件窃取是 LLM 代理固有灵活性下的"预期行为"，而另一些人则强烈批评微软为保持相关性而仓促部署 AI 功能。少数技术观点指出提示词注入漏洞已有充分记录（以 OpenAI 的 Atlas 为例），认为真正的问题在于产品发布时安全加固不足，而非新型攻击技术。

**标签**: `#security`, `#prompt-injection`, `#microsoft-copilot`, `#ai-safety`, `#enterprise-ai`

---

<a id="item-2"></a>
## [教皇利奥十四发布关于技术伦理与人类尊严的通谕](https://www.vatican.va/content/leo-xiv/en/encyclicals/documents/20260515-magnifica-humanitas.html) ⭐️ 7.0/10

教皇利奥十四发布了名为《Magnifica Humanitas》的新通谕，认为技术会承载其创造者的特质，并敦促技术开发者在研发新技术时考虑文明的更大利益。 这份通谕对全球关于技术伦理、权力集中和人工智能社会影响的持续辩论做出了重要贡献——这些话题引起了科技界的广泛关注，特别是在 Hacker News 平台上，该讨论获得了超过 1300 个点赞和 720 条评论。 通谕指出'技术从来不是中性的，因为它承载了设计者、资助者、监管者和使用者的特质'，并引用教皇方济各的观点，说明生物技术、信息技术和 DNA 知识如何赋予拥有知识和经济资源的人'对全人类和整个世界的显著支配权'。

hackernews · theletterf · 05月25日 10:11 · [社区讨论](https://news.ycombinator.com/item?id=48265206)

**背景**: 通谕是天主教教会最高形式的教育权威文件，由教皇发布以阐述信仰、道德或教会纪律问题。这份文件建立在早期技术伦理框架之上，包括教皇方济各关于数字技术和核能的声明。梵蒂冈参与技术伦理讨论反映了全球对人工智能治理、算法偏见和科技公司权力集中的日益关注。

**社区讨论**: Hacker News 社区的反应明显积极，甚至连自称为无神论者也对该通谕的观点表示赞赏。评论者特别认同'开发者应深入思考他们所构建的东西对文明的影响'这一信息，尽管也有人质疑历史上是否真的存在技术被'驯服'以造福社会的例子。讨论还强调了对技术将权力集中在拥有知识和资源的人手中的担忧。

**标签**: `#technology ethics`, `#societal impact`, `#AI and society`, `#power concentration`, `#technology policy`

---

<a id="item-3"></a>
## [Grok V9-Medium 训练完成，预计 2-3 周后发布](https://x.com/elonmusk/status/2058787384364265734) ⭐️ 7.0/10

埃隆·马斯克宣布 xAI 的 Grok V9-Medium 基础模型（拥有 1.5 万亿参数）已完成训练，评估结果良好。团队目前正在进行强化学习微调，预计 2-3 周后公开发布。该模型整合了大量 Cursor 训练数据，以提升复杂编程任务的处理能力。 这个拥有 1.5T 参数的模型是目前 v8-small（0.5T）的三倍，代表着 xAI 发展的重要规模化里程碑。通过整合 Cursor 数据聚焦编程能力的战略，表明 xAI 有意在日益重要的 AI 驱动开发者工具市场中展开竞争。 基础模型在强化学习微调开始前通过了评估，表明其基础性能扎实。强化学习微调是一种通过奖励信号优化模型输出的后训练技术。该模型包含针对 Cursor 数据（一个广泛使用的 AI 代码编辑器）的专门训练，暗示其在代码生成任务上有针对性的改进。

telegram · zaihuapd · 05月25日 07:07

**背景**: xAI 是埃隆·马斯克于 2023 年创立的 AI 公司，在大语言模型领域与 OpenAI、Anthropic 和 Google 展开竞争。Grok 是 xAI 的旗舰对话式 AI 助手。强化学习微调（RLFT）是一种使用基于奖励的反馈信号来优化模型行为的高级后训练方法。Cursor 是一个基于 Visual Studio Code 的 AI 驱动集成开发环境（IDE），成立于 2022 年，截至 2026 年初估值达 293 亿美元，被开发者广泛用于 AI 辅助编码任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cursor_(code_editor)">Cursor (code editor)</a></li>
<li><a href="https://aws.amazon.com/blogs/machine-learning/fine-tune-large-language-models-with-reinforcement-learning-from-human-or-ai-feedback/">Fine-tune large language models with reinforcement learning ...</a></li>

</ul>
</details>

**标签**: `#xAI`, `#Grok`, `#LLM`, `#AI Models`, `#Elon Musk`

---

<a id="item-4"></a>
## [离体人脑用于药物测试 伦理争议随之而来](https://www.science.org/content/article/not-alive-not-dead-disembodied-human-brains-used-drug-testing) ⭐️ 7.0/10

美国康涅狄格州生物技术公司 Bexorg 利用其 BrainEx 灌流系统，在 700 多个死亡后的人脑中恢复了部分代谢活动，用于药物测试。该公司报告称，阿尔茨海默病和帕金森病的候选药物在离体人脑中显示出显著疗效，而这些药物在传统动物模型中却未能通过测试。 这项研究可以通过提供基于人类的测试平台来革新神经药物研发，克服动物模型中物种差异带来的局限性。与 Biohaven 的合作表明，一种在小鼠实验中失败的药物在人类大脑中显示出希望，可能将研发周期缩短 3-5 年并节省数百万美元。然而，这项技术也挑战着生命、死亡和意识的基本定义。 BrainEx 系统通过大脑血管泵送含血红蛋白的富氧灌流液，以恢复微循环而不唤醒意识。Bexorg 计划将大脑存活时间延长至两周，以进行更长期的治疗研究，并正在开发名为 NeuroLens 的机器学习模型，用于模拟虚拟大脑进行初步药物筛选。研究人员强调尚未恢复意识，但伦理学家质疑现有伦理框架是否能充分应对这种"既非完全死亡、也非真正活着"的状态。

telegram · zaihuapd · 05月25日 14:57

**背景**: BrainEx 技术首次在 2019 年一篇名为《死亡数小时后脑循环和细胞功能的恢复》的论文中描述。传统药物研发严重依赖动物模型，但由于物种间存在显著的生物学差异，动物模型往往无法预测人体反应。这种局限性一直是神经疾病研究的重大瓶颈，复杂的人脑功能难以在其他动物中复制。器官芯片和灌流技术代表了创建更具生理相关性测试平台的新兴方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.msn.cn/zh-cn/科学/生物学/美国公司打造离体大脑平台-为神经疾病药物研发提供新路径引伦理热议/ar-AA23YZ7r">美国公司打造离体大脑平台：为神经疾病药物研发提供新路径引伦理热议</a></li>
<li><a href="https://neuwritesd.org/2019/06/13/brainex-restoring-brain-circulation-after-death/">BrainEx: Restoring Brain Circulation After Death</a></li>

</ul>
</details>

**标签**: `#neuroscience`, `#bioethics`, `#brain-computer-interface`, `#drug-development`, `#consciousness`

---

<a id="item-5"></a>
## [Mullvad VPN 部署出口 IP 指纹识别缓解措施](https://mullvad.net/en/help/exit-ip-vpn-servers-mitigation-rollout) ⭐️ 6.0/10

Mullvad VPN 正在其服务器网络中推出出口 IP 指纹识别缓解措施。该缓解措施旨在降低基于用户 VPN 出口 IP 地址进行识别或追踪的指纹识别技术的有效性。 出口 IP 指纹识别代表了传统 VPN 保护中的一个重要隐私漏洞，因为用户仍然可以根据其 VPN 出口 IP 的独特特征在多个网站间被追踪。这次部署解决了一个许多注重隐私的用户可能没有意识到的微妙但真实的用户识别途径。 Mullvad 浏览器包含内置的 Mullvad 代理，并具有随机模式功能，可为每个访问的网站分配不同的出口 IP 地址。社区讨论强调了一种替代方法：不是随机化指纹，而是有人主张对所有用户欺骗相同的标准化信息，以创建统一的指纹，使其与他人无法区分。

hackernews · Cider9986 · 05月25日 17:45 · [社区讨论](https://news.ycombinator.com/item?id=48269580)

**背景**: 出口 IP 地址是独特的标识符，可以揭示用户连接的是哪家 VPN 提供商以及具体哪台服务器。IP 指纹识别技术可以利用这些出口 IP 以及浏览器的其他属性（如画布渲染和屏幕分辨率）在网络上追踪用户。如果出口 IP 本身可以充当追踪标识符，那么 VPN 隐藏原始 IP 地址的主要保护就变得不够充分。隐私社区中的一些人认为，统一欺骗——无论用户是谁都提供相同的指纹——可能比随机欺骗更有效，因为随机欺骗可能会适得其反地使用户更容易被识别。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://discuss.privacyguides.net/t/mullvad-exit-ips-as-a-fingerprinting-vector/37910">Mullvad exit IPs as a fingerprinting vector - General - Privacy</a></li>
<li><a href="https://tmctmt.com/posts/mullvad-exit-ips-as-a-fingerprinting-vector/">Mullvad exit IPs as a fingerprinting vector | tmctmt</a></li>

</ul>
</details>

**社区讨论**: 社区讨论揭示了对指纹识别策略的深思熟虑的观点。一位评论者强调，Mullvad 浏览器的随机模式功能为每个网站提供不同的 IP 地址，有效地缓解了出口 IP 指纹识别问题，无需服务器端更改。另一位用户主张统一欺骗浏览器特征而不是随机化它们，认为所有用户使用相同指纹将使个人追踪变得不可能。还有人对 VPN 基础设施的商业经济学感到好奇，询问 VPN 提供商是否为出口点向零售 ISP 付费。

**标签**: `#VPN`, `#privacy`, `#fingerprinting`, `#Mullvad`, `#network-security`

---

<a id="item-6"></a>
## [Epic 公布虚幻引擎 6，Rocket League 为首个展示游戏](https://www.pcgamer.com/gaming-industry/epic-reveals-first-unreal-engine-6-game-and-its-not-fortnite/) ⭐️ 6.0/10

Epic Games 在巴黎举办的 Rocket League 冠军系列赛上正式发布了虚幻引擎 6，并确认《Rocket League》为首个展示游戏。值得注意的是，Rocket League 将跳过 UE4 和 UE5，直接从 UE3 升级至 UE6。 这一重大版本跳跃表明 Epic 致力于实现重大技术突破而非渐进式更新。对于使用旧代码库的游戏开发者和工作室而言，从 UE3 直接跳跃至 UE6 的能力为现代化升级提供了前所未有的潜力，并可能重塑工作室处理引擎迁移的方式。 UE6 预告中出现了包括《堡垒之夜》在内的跨游戏画面，业界观察人士将其解读为 Epic 元宇宙平台野心的信号。四年前发布的 UE5 已成为影视和游戏行业使用最广泛的中间件，但因 PC 优化问题持续受到批评，不少玩家敦促 Epic“先修好 UE5”再发布下一版本。

telegram · zaihuapd · 05月25日 02:20

**背景**: 游戏引擎是简化游戏开发的中间件，通过提供渲染系统、物理引擎和跨平台支持等统一框架来降低开发门槛。由 Epic Games 开发的虚幻引擎是与 Unity 并列的最广泛使用的商业游戏引擎之一。《Rocket League》最初发布于 X360 时代平台，十多年来一直运行在 UE3 上，因此此次版本跳跃在技术进步方面堪比完整的续作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/游戏引擎">游戏引擎 - 维基百科，自由的百科全书</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/5136619287">Perforce《2024游戏技术现状报告》Part2：游戏引擎、版本控制、IDE及...</a></li>

</ul>
</details>

**标签**: `#Unreal Engine 6`, `#Epic Games`, `#Rocket League`, `#Game Development`, `#Game Engines`

---

<a id="item-7"></a>
## [腾讯 ima copilot 全量开放，主打四模块常驻记忆系统](https://mp.weixin.qq.com/s/4gEMiKaRMTL2ieH5EnnnyA) ⭐️ 6.0/10

腾讯于 5 月 25 日正式向所有用户开放 AI 助手 ima copilot，结束灰度测试阶段。该产品主打四模块记忆系统——Soul、User、Memory 和 Agent，通过记忆用户习惯、感知当前操作内容、直接调用笔记和知识库来维持跨会话的上下文。 此次发布代表了腾讯对 AI 助手长期痛点的解决方案：会话结束后无法保持上下文的问题。通过实施结构化的四模块记忆架构，ima copilot 可能显著改善知识工作者和企业用户的工作流程连续性，并可能为中文市场的 AI 助手记忆系统设定新标准。 四个记忆模块各司其职：Soul 管理交互风格偏好，User 维护用户档案，Memory 存储长期项目知识，Agent 积累任务经验。该产品基于腾讯混元大模型技术构建。然而，关于记忆容量、数据保留策略和隐私实施的具体技术细节在当前公告中仍然有限。

telegram · zaihuapd · 05月25日 05:21

**背景**: 个人知识管理和 AI 记忆系统已成为 AI 助手开发商的关键战场。核心挑战是使 AI 系统能够在会话之间保持持久上下文，而非将每次对话视为孤立事件。腾讯将记忆划分为功能模块（Soul、User、Memory、Agent）的方法呼应了学术界关于 AI 系统结构化记忆架构的讨论。混元模型是腾讯的自研大语言模型，作为其 AI 产品的底层技术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aipure.ai/articles/imacopilot-review-tencents-ai-smart-workstation">ima.copilot Review: Tencent's AI Smart Workstation</a></li>
<li><a href="https://www.tkj.ai/ai-tools/ima-copilot-new">ima.copilot : AI intelligent workbench | Tkj.ai</a></li>

</ul>
</details>

**社区讨论**: 该公告在中国科技社区引起了适度关注，尤其是四模块记忆架构。讨论焦点在于该方法与其他 AI 助手记忆解决方案的比较，部分用户对日常工作流程整合的实际影响表示兴趣，而另一些用户则等待更详细的技术规格披露。

**标签**: `#AI Assistants`, `#Tencent`, `#Personal Knowledge Management`, `#Memory Systems`, `#Product Launch`

---