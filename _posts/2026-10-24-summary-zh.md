---
layout: default
title: "Horizon Summary: 2026-10-24 (ZH)"
date: 2026-10-24
lang: zh
---

> 从 57 条内容中筛选出 8 条重要资讯。

---

**科技新闻**
1. [Kimi 发布 K3.1-Pro：3 万亿参数开放权重模型，支持 100 万 token 上下文](#item-tech-news-1) ⭐️ 8.0/10
2. [Ollama v0.40.10 发布 Nemotron 3.5 Bolt E4B 视觉语言模型](#item-tech-news-2) ⭐️ 7.0/10
3. [ggml-org/llama.cpp released b11840](#item-tech-news-3) ⭐️ 7.0/10
4. [iOS 越狱演示引发对苹果信任访问计划的讨论](#item-tech-news-4) ⭐️ 7.0/10
5. [Dessa: the most authentic full-duplex speech model ever built](#item-tech-news-5) ⭐️ 7.0/10
6. [实践者分享用自建方案替代 15 万美元 Looker 订阅](#item-tech-news-6) ⭐️ 7.0/10
7. [OpenAI 加强前沿模型训练环境的离线隔离与红队测试](#item-tech-news-7) ⭐️ 7.0/10
8. [I just came across Next-Concept Modeling and the idea is fascinating\[R\]](#item-tech-news-8) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Kimi 发布 K3.1-Pro：3 万亿参数开放权重模型，支持 100 万 token 上下文](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

Moonshot AI 发布 Kimi K3.1-Pro，这是 K3.1 系列首款模型，定位为目前最强的 3 万亿参数开放权重模型，支持 100 万 token 上下文。模型在编程、三维创作、金融研究及复杂智能体任务上重点提升：Terminal-Bench 4.0 得分 65.7%，高于 GPT-6 Astra 的 58.2%，接近 Claude Opus 5.5 的 66.4%；BenchCAD 工具辅助得分 92.7%；内部金融建模、研究测试分别提升 7.2、11.6 分。陈述级幻觉率从 23.4% 降至 8.3%。同步推出 Highspeed 版本，速度为标准版 2-3 倍，价格为 2 倍（输入缓存命中除外）。模型已接入 Kimi、Work、Code 和 API，完整权重计划于 2026 年 11 月 4 日前发布。API 定价为输入 $2.00/百万 token、输出 $10/百万 token，与 GPT-6.1 Sol 持平，为 Claude Opus 5.5 的一半。

telegram · zaihuapd · 10月23日 17:14

**「技术背景」** 开放权重大模型的发布通常需要明确参数规模、上下文长度以及权重发布的时间承诺，这些直接影响模型的可定制性和社区使用价值。Kimi K3.1-Pro 作为 K3.1 系列的首款旗舰模型，其 3 万亿参数规模与 100 万 token 上下文长度在同类模型中具有显著性，且模型承诺将在 2026 年 11 月前发布完整权重，这为开发者和研究人员提供了明确的后续规划。

**「Kimi K3.1 Pro 发布影响」** 对开发者和 API 用户而言，Kimi K3.1 Pro 目前已通过 Kimi API 等渠道提供，但开放权重尚未发布，官方只承诺在 2026 年 11 月 4 日前发布完整权重，因此自部署或本地运行仍存在不确定性。其 API 价格为每百万输入 token 2 美元、每百万输出 token 10 美元，Highspeed 版本速度为标准版的 2 至 3 倍，但价格翻倍，输入 token cache hit 仍按原价。官方基准显示该模型在编程、三维建模和金融任务上较 K3 有提升，但这些结果来自 Moonshot AI，且内部幻觉率降幅不代表日常使用错误率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/moonshotai/kimi-k3">Kimi K3 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://k3-kimi.com/">Kimi K3: 2.8T Open-Weight Model — Benchmarks , Pricing &amp; Guides</a></li>
<li><a href="https://habr.com/ru/articles/1063742/">Kimi K3 — что реально даёт открытие весов самой большой... / Хабр</a></li>

</ul>
</details>

**标签**: `#AI model release`, `#open-weight model`, `#coding assistant`, `#3D generation`, `#long context`

---

<a id="item-tech-news-2"></a>
### [Ollama v0.40.10 发布 Nemotron 3.5 Bolt E4B 视觉语言模型](https://github.com/ollama/ollama/releases/tag/v0.40.10) ⭐️ 7.0/10

Ollama v0.40.10 新增了 NVIDIA Nemotron 3.5 Bolt E4B，这是一款基于 Gemma 4 的视觉语言模型，支持 128K-token 上下文窗口，并内置 DFlash 草稿用于推测解码。用户可通过单条命令 \`ollama run nemotron-3.5-bolt:e4b\` 在本地运行该模型，实现快速本地对话、图像理解和工具使用功能。

github · github-actions\[bot\] · 10月23日 15:03

**「Ollama v0.40.10 新增 NVIDIA Nemotron 3.5 Bolt E4B」** Ollama 发布 v0.40.10，将 NVIDIA 的 Gemma 4 基础、支持 128K 上下文的 Nemotron 3.5 Bolt E4B 视觉语言模型加入本地可运行列表，可通过 &\#x27;ollama run nemotron-3.5-bolt:e4b&\#x27; 命令直接使用。该模型提供 DFlash 换行解码支持，并依赖 NVIDIA NIM 推理微服务进行部署。

**「影响」** 开发者和研究人员可直接在本地运行 128K 上下文的多模态模型，无需依赖云端 API，降低了 multimodal 应用的部署成本和延迟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://build.nvidia.com/models">Models | Try NVIDIA NIM APIs</a></li>

</ul>
</details>

**标签**: `#ollama`, `#nemotron`, `#vision-language-model`, `#local-llm`, `#model-release`

---

<a id="item-tech-news-3"></a>
### [ggml-org/llama.cpp released b11840](https://github.com/ggml-org/llama.cpp/releases/tag/b11840) ⭐️ 7.0/10

Release b11840 adds CEIL\(f32\) and f16 versions of the ceiling operation to ggml-org/llama.cpp, improving the library&\#x27;s mathematical operations for AI applications.

github · github-actions\[bot\] · 10月23日 16:46

**标签**: `#ai-tools`, `#open-source`, `#llama-cpp`

---

<a id="item-tech-news-4"></a>
### [iOS 越狱演示引发对苹果信任访问计划的讨论](https://blog.calif.io/p/iphone) ⭐️ 7.0/10

一名名为 pavel\_lishin 的研究人员在个人博客上发布文章，声称成功实现了对 iPhone 的越狱。该文章未提供具体的技术细节、受影响的 iOS 版本号或漏洞信息。文章发布于 2026 年 10 月 23 日，引发了安全社区对苹果生态系统控制和信任访问计划的广泛讨论。

hackernews · pavel\_lishin · 10月23日 16:21 · [社区讨论](https://news.ycombinator.com/item?id=50211474)

**「iOS 越狱的历史背景」** iOS 越狱一直是安全研究的一个重要领域，苹果公司通过固件签名验证、沙盒机制和系统完整性保护等多层防护来防止越狱行为。此外，苹果的信任访问计划（TCA）允许选定的安全研究人员获取特定设备用于漏洞测试，但该计划一直被批评为门槛过高。

**「对用户和研究人员的影响」** 若越狱技术属实，普通用户可能会面临设备安全风险，同时苹果可能会加强对越狱设备的检测与限制措施。对于安全研究人员而言，此次演示凸显了苹果信任访问计划存在的不公平性问题，部分研究人员认为该计划更像是一种“护城河”而非安全保障。

**「社区反响与争论」** 社区成员对此表示褒贬不一：部分人认为越狱让人感到“美好而无助”，因为苹果可以轻易检测越狱并限制 iCloud 和 iMessage 等服务；另有研究人员批评苹果的信任访问计划只限于“内部圈子”，排斥了更多安全研究人员的参与；还有用户询问是否启用限制模式（Lockdown Mode）能抵御此类漏洞，并希望越狱后能获得持久的 root 访问权限。

**标签**: `#iOS jailbreak`, `#security research`, `#Apple ecosystem`

---

<a id="item-tech-news-5"></a>
### [Dessa: the most authentic full-duplex speech model ever built](https://block.xyz/dessa) ⭐️ 7.0/10

Dessa is presented as an authentic full-duplex speech model, drawing attention for its low-latency and local-training claims, though the discussion includes both technical excitement and skepticism about the headline.

hackernews · dsr12 · 10月23日 19:09 · [社区讨论](https://news.ycombinator.com/item?id=50213925)

**标签**: `#full-duplex speech model`, `#AI voice`, `#local AI deployment`, `#model release`, `#AI agents`

---

<a id="item-tech-news-6"></a>
### [实践者分享用自建方案替代 15 万美元 Looker 订阅](https://david.lequin.dev/blog/bi-software-is-dead/) ⭐️ 7.0/10

一篇博客文章探讨能否用一堆 HTML 文件替代每年 15 万至 30 万美元的 Looker 订阅。作者报告了用自建实现替换 Looker 的实际经历，Hacker News 社区讨论中有多位从业者验证了这种做法，其中一位工程师表示其公司正在用 Claude 赞助的工程工作替换 30 万美元/年的 Looker 订阅，且已在几周内验证核心思路。

hackernews · skadamat · 10月23日 17:15 · [社区讨论](https://news.ycombinator.com/item?id=50212320)

**「背景」** Looker 是一款企业级商业智能（BI）平台，通常按年订阅收费，价格高达数十万美元。传统 BI 工具提供语义层、数据建模、仪表板和治理功能。随着大语言模型降低代码生成成本，部分团队尝试用轻量级自建方案（如静态 HTML + SQL）替代昂贵的商业 BI 套件。

**「影响」** 对于未充分利用 Looker 高级功能的组织，自建方案可在数周内由 1-2 名工程师完成核心替换，大幅降低许可证成本。但评论指出，保证全公司指标口径一致、避免 SQL 注入等治理问题仍需投入，分析师角色难以完全被取代。

**「社区讨论」** 评论呈现两极：支持者分享十年前用 PHP+SQL 实现类似内部 BI 的经验，以及正在用 Claude 协助替换 30 万美元 Looker 的实例；反对者强调 BI 核心难点在于指标定义与治理而非制图，单纯生成图表仅占成本小头，语义层一致性、数据信任度仍需专业分析师把关。

**标签**: `#BI-tool-replacement`, `#Looker`, `#cost-reduction`, `#practitioner-experience`

---

<a id="item-tech-news-7"></a>
### [OpenAI 加强前沿模型训练环境的离线隔离与红队测试](https://openai.com/index/securing-our-frontier-model-training-environment) ⭐️ 7.0/10

OpenAI 在文章中说明，已对其前沿模型训练和评估基础设施实施安全加固，主要涉及其前沿模型开发与评估流程。具体措施包括部署离线训练环境，并开展高算力红队测试，以加强对前沿模型的限制（containment）。以上内容均来自 OpenAI 自身的工程说明，文中未披露具体实现细节，也未提供独立验证结果。

rss · OpenAI News · 10月23日 10:00

**「背景」** 前沿模型训练通常需要大规模计算资源，并在训练与评估过程中接触模型权重和敏感数据，因此需要将训练环境与外部网络隔离，以降低信息或模型能力意外泄露的风险。红队测试是在受控条件下主动探测模型安全边界与潜在滥用风险的做法。

**标签**: `#openai`, `#model-safety`, `#red-teaming`, `#training-infrastructure`

---

<a id="item-tech-news-8"></a>
### [I just came across Next-Concept Modeling and the idea is fascinating\[R\]](https://www.reddit.com/r/MachineLearning/comments/1xd7bsu/i_just_came_across_nextconcept_modeling_and_the/) ⭐️ 7.0/10

A student shares a new hierarchical discrete-code generation architecture from a paper on arXiv, claiming up to 31x faster text generation via parallel VQ-VAE-based code prediction compared to diffusion language models.

reddit · r/MachineLearning · /u/PanelReader · 10月23日 07:24

**标签**: `#hierarchical-generation`, `#discrete-code-modeling`, `#vq-vae`, `#efficient-text-generation`, `#large-language-model-architecture`

---