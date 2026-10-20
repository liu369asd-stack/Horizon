---
layout: default
title: "Horizon Summary: 2026-10-20 (ZH)"
date: 2026-10-20
lang: zh
---

> 从 68 条内容中筛选出 7 条重要资讯。

---

**科技新闻**
1. [Mistral 发布 Timestral：面向时间序列预测的基础模型](#item-tech-news-1) ⭐️ 8.0/10
2. [Mercury 3: Diffusion at scale](#item-tech-news-2) ⭐️ 7.0/10
3. [SteerTTS：23M 参数英文 TTS，CPU 实时运行，数值控制语调](#item-tech-news-3) ⭐️ 7.0/10
4. [MiniMax 发布 M3.1 Flash，推理速度提升近 3 倍，成本降低 70%](#item-tech-news-4) ⭐️ 7.0/10
5. [美国国土安全部排除 DeepSeek 产品出联邦文职部门采购](#item-tech-news-5) ⭐️ 7.0/10
6. [Inception 发布扩散式语言模型 Mercury 3，TPS 超过 1000 tokens/秒](#item-tech-news-6) ⭐️ 7.0/10
7. [Manus 发布 AI 游戏生成器，支持文本描述创建网页游戏](#item-tech-news-7) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Mistral 发布 Timestral：面向时间序列预测的基础模型](https://mistral.ai/news/timestral/) ⭐️ 8.0/10

Mistral AI 发布了 Timestral，这是一款面向时间序列预测的基础模型，能够以零样本方式处理多个时间序列以及已知的未来协变量。与传统为每个序列单独训练模型的范式不同，Timestral 采用单一基础模型覆盖数千个序列，支持在不针对特定序列进行训练的情况下直接进行预测。该模型还允许将生产计划、天气预报等已知的未来影响因素作为条件输入，从而提升预测准确性。这一发布在 Hacker News 上引发了高度关注，获得 546 分和 104 条评论。

hackernews · groar · 10月19日 09:59 · [社区讨论](https://news.ycombinator.com/item?id=50150434)

**「背景脉络」** 时间序列预测长期依赖为每个序列单独训练专用模型的做法，这在面对成千上万个序列时变得不切实际——每个序列的历史数据有限，难以训练出稳健的模型。ChatGPT 等通用基础模型展示了跨领域零样本推理的潜力，推动了 AI 社区探索将类似范式应用于时间序列预测。传统方法如 XGBoost 虽在单序列预测中表现良好，但在多序列场景下面临数据稀疏性和规模不匹配的挑战。

**「影响」** 对于需要同时预测数千个时间序列的组织（如电力公司、零售商、制造商），Timestral 提供了统一的解决方案，可显著降低模型维护成本和基础设施开销。对于历史数据较少的长尾序列，该模型能够借助跨序列的共享信息进行预测，这是传统单序列模型无法实现的。然而，社区讨论也指出，实际部署中仍需评估模型在特定领域的准确性和可靠性，尤其是与经过大量领域数据验证的传统方法（如 XGBoost）相比。

**「社区讨论」** Hacker News 上的讨论集中在基础时间序列模型的实用性与传统方法的对比上。部分评论者质疑单一模型能否真正理解不同领域时间序列的差异，认为联合信息获取是提升准确性的关键；另一些评论者则强调，对于拥有数千个序列的组织来说，维护单一基础模型远比训练和管理数千个专用模型可行。也有评论者对量化交易公司是否已内部部署类似解决方案表示好奇，并对 Mistral 模型的实际性能表现持怀疑态度。

**标签**: `#model-release`, `#time-series`, `#forecasting`, `#mistral`, `#foundation-model`

---

<a id="item-tech-news-2"></a>
### [Mercury 3: Diffusion at scale](https://www.inceptionlabs.ai/blog/introducing-mercury-3) ⭐️ 7.0/10

Mercury 3 is a diffusion-based model release that users report as notably more capable than prior versions, offering practical utilities like HTML/UML rendering and color scheme adaptation.

hackernews · cmrdporcupine · 10月19日 17:27 · [社区讨论](https://news.ycombinator.com/item?id=50155245)

**标签**: `#diffusion`, `#AI-code-generation`, `#hands-on-tools`, `#model-release`

---

<a id="item-tech-news-3"></a>
### [SteerTTS：23M 参数英文 TTS，CPU 实时运行，数值控制语调](https://www.reddit.com/r/MachineLearning/comments/1x9okma/steertts_23mparam_english_tts_you_steer_with/) ⭐️ 7.0/10

SteerTTS 是一个开源的 23M 参数英文 TTS 系统，由 9.6M 参数声学模型（注意力 + 双向 Mamba-3，FastPitch 风格）与 Vocos 声码器组成，面向需要在对话中由 LLM 上下文调节语音的开发者。它通过相对所选音色中性语音的 z 分数提供 12 项可控参数，包括语速、响度、中值音高、音高范围、最终升降、停顿、频谱倾斜与气息相关指标，并支持 51 个风格标签、自由文本提示（解析为可检查的 JSON）以及行内标记（\*emphasis\*、\*\[pause 400ms\]\*、\*&lt;slow&gt;…&lt;/slow&gt;\*）。模型内置 2,825 个匿名音色，提供实验性零样本克隆，CPU 上无可选流式细化器时实时系数约 4–8，首段流式音频约 0.5 秒；本地测得英文集合平均 WER 约 1.8%，但并非官方排行榜提交。作者坦诚指出响度、音高与倾斜可靠，而停顿、浊音与 CPPS 控制较弱，情感标签难以被分类器区分，克隆相似度低，且仅支持英文、暂无人工评测；权重采用 CC BY-NC 4.0（非商业），代码采用 MIT，模型与评测表已在 Hugging Face 发布。

reddit · r/MachineLearning · /u/Working\_Hat5120 · 10月19日 05:36

**「背景」** 可控语音合成通常需要在推理时注入语调、语速等条件；SteerTTS 将每项控制量定义为相对所选音色中性语音的 z 分数，使其可直接从 LLM 接收数值指令。该项目声称从零实现新架构，尚未发布人工评测结果，也未在官方排行榜上提交。

**「影响」** 对于构建 LLM 驱动对话代理的开发者，CPU 上约 4–8 的实时系数和约 0.5 秒的首段音频延迟表明，该模型可在普通处理器上进行实时上下文语调调节。需要注意的限制是：仅支持英文，且权重采用 CC BY-NC 4.0 非商业许可，代码为 MIT 许可。

**标签**: `#steerable TTS`, `#open-source speech synthesis`, `#LLM-integrated audio controls`, `#real-time CPU inference`

---

<a id="item-tech-news-4"></a>
### [MiniMax 发布 M3.1 Flash，推理速度提升近 3 倍，成本降低 70%](https://mp.weixin.qq.com/s/fO9snz_lnPxVg0q55chDFg) ⭐️ 7.0/10

MiniMax released M3.1 Flash, a faster and cheaper agent/coding-focused LLM with ~70% lower claimed agent costs and plans to open weights later.

telegram · zaihuapd · 10月19日 11:27

**标签**: `#MiniMax`, `#M3.1 Flash`, `#LLM pricing`, `#AI coding agents`, `#open-weights model`

---

<a id="item-tech-news-5"></a>
### [美国国土安全部排除 DeepSeek 产品出联邦文职部门采购](https://www.federalregister.gov/public-inspection/2026-21447/order-exclusion-and-removal-of-deepseek-products-from-federal-civilian-executive-branch-information) ⭐️ 7.0/10

美国国土安全部依据《联邦采购供应链安全法》发布命令，将杭州深度求索人工智能基础技术研究有限公司（DeepSeek）及其关联实体开发的信息技术产品与服务排除出联邦文职行政部门的采购范围，并要求从文职机构的信息系统中移除所有 DeepSeek 及相关实体产品，以及使用 DeepSeek 实现的第三方产品与服务。此前，国防部与情报界已对 DeepSeek 实施过类似使用限制。

telegram · zaihuapd · 10月19日 13:32

**「供应链安全法依据」** 《联邦采购供应链安全法》旨在保护联邦信息系统免受来自不可信供应商的风险，此类法规此前已被用于限制涉及安全风险的科技产品在联邦层面的采购与使用。

**「影响范围」** 该命令将直接影响 DeepSeek 在美国联邦文职部门的业务开展，包括现有系统的清除工作，可能要求相关机构在有限时间内完成产品移除与替代工作。

**标签**: `#DeepSeek`, `#AI监管`, `#联邦采购`, `#供应链安全`

---

<a id="item-tech-news-6"></a>
### [Inception 发布扩散式语言模型 Mercury 3，TPS 超过 1000 tokens/秒](https://www.inceptionlabs.ai/blog/introducing-mercury-3) ⭐️ 7.0/10

Inception 发布大型扩散式语言模型 Mercury 3，声称生成速度超过每秒 1000 tokens。模型参数量约为 Mercury 1 的 40 倍，上下文窗口达 100 万 tokens，已在 Inception API 与 OpenRouter 上线，输入定价为每百万 tokens 0.2 美元。在多项基准测试中，其表现据称超越 GPT-6 Luna 与 Claude Haiku 5.5。

telegram · zaihuapd · 10月20日 00:29

**「背景」** 扩散式语言模型通过迭代去噪过程生成文本，区别于传统的自回归 Transformer 架构。Inception 此前已发布 Mercury 1，为该技术路线奠定了基础。Mercury 3 在此基础上显著扩大了模型规模和上下文长度。

**「影响」** 开发者可利用超过 1k TPS 的生成速度实现近实时的交互式应用，同时低至 0.2 美元/百万 tokens 的输入成本降低了长文本处理的费用。

**标签**: `#AI`, `#LLM`, `#diffusion models`, `#model release`, `#API pricing`

---

<a id="item-tech-news-7"></a>
### [Manus 发布 AI 游戏生成器，支持文本描述创建网页游戏](https://manus.im/features/game-dev) ⭐️ 7.0/10

Manus 发布了 AI 游戏生成器，用户无需编写代码，只需输入自然语言描述即可生成可在浏览器中运行的游戏。该功能已上线，提供 40 个可玩示例，并支持查看和重新编辑生成游戏背后的提示词。游戏支持分享链接到 X、Reddit、Discord，并由 Manus 负责多人游戏的服务器与部署，同时提供玩家访问数据分析。

telegram · zaihuapd · 10月20日 01:18

**「背景」** 无需代码的 AI 工具使非编程人员能够创建复杂的数字产品，这是 AI 辅助创作领域的一个进展。Manus 此前的 AI 平台已提供文本到代码的转换功能，为此次游戏生成器的发布奠定了基础。

**「影响」** 学生和爱好者现在能够通过简单的文本描述快速创建可分享的网页游戏，无需掌握编程技能，从而降低了游戏开发的门槛。

**标签**: `#AI game generator`, `#no-code tool`, `#student-friendly AI`, `#prompt engineering`, `#Manus AI`

---