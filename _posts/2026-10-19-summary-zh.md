---
layout: default
title: "Horizon Summary: 2026-10-19 (ZH)"
date: 2026-10-19
lang: zh
---

> 从 62 条内容中筛选出 7 条重要资讯。

---

**科技新闻**
1. [TempoPFN: 线性 RNN 合成预训练实现零-shot 时间序列预测](#item-tech-news-1) ⭐️ 8.0/10
2. [Google 开源 Harness² 递归框架 提升 LLM 智能体性能](#item-tech-news-2) ⭐️ 8.0/10
3. [llm-echo 0.5 增加 reasoning tokens 支持并完善 token 计数](#item-tech-news-3) ⭐️ 7.5/10
4. [Hybrid Reasoning Agents: LLM agents that think in latent space, act through text](#item-tech-news-4) ⭐️ 7.0/10
5. [DeepSeek announces $0.75 per 1000 search API pricing](#item-tech-news-5) ⭐️ 7.0/10
6. [Sphinx：AI 代码推送前的验证钩子](#item-tech-news-6) ⭐️ 7.0/10
7. [asmsense 发布 22.8 万条带源标签的 x86-64 函数数据集和 Qwen3-8B 微调模型](#item-tech-news-7) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [TempoPFN: 线性 RNN 合成预训练实现零-shot 时间序列预测](https://www.reddit.com/r/MachineLearning/comments/1x97v19/tempopfn_synthetic_pretraining_of_linear_rnns_for/) ⭐️ 8.0/10

TempoPFN 是一篇被 NeurIPS 2026 接收的论文，介绍了一种使用合成数据预训练线性 RNN（基于 DeltaProduct 架构）以实现零-shot 时间序列预测的方法。论文提供了一个合成时间序列生成器和增强策略的库，并已在 Toto-2 和 TS-ICL 等项目中使用。相关代码已在 GitHub（https://github.com/automl/TempoPFN）和 HuggingFace（https://huggingface.co/AutoML-org/TempoPFN）上发布，论文预印本可在 arXiv（https://arxiv.org/abs/2510.25502）访问。

reddit · r/MachineLearning · /u/Yossarian\_1234 · 10月18日 16:43

**「背景介绍」** 时间序列基础模型的训练通常需要大量真实数据，这在许多领域（如工业监控或金融）中难以获取。合成数据生成作为一种替代方案，能够减少对真实数据的依赖。TempoPFN 通过构建多样化的合成时间序列生成器和数据增强策略，为线性 RNN 的预训练提供了可扩展且可重用的解决方案。

**「影响与意义」** 该方法降低了时间序列基础模型训练对真实数据的需求，特别适用于数据稀缺的场景。提供的开源库和预训练模型使研究人员和开发者能够更便捷地构建和测试零-shot 预测系统，推动时间序列领域基础模型的研究与应用。

**标签**: `#time-series-foundation-models`, `#synthetic-data-generation`, `#linear-rnn-pretraining`, `#neural-network-pre-training`

---

<a id="item-tech-news-2"></a>
### [Google 开源 Harness² 递归框架 提升 LLM 智能体性能](https://github.com/google-research/harness2) ⭐️ 8.0/10

Google Research 开源了 Harness²，一个通过两层递归在不调整模型权重的情况下提升 LLM 智能体性能的框架。在 WorkBuddy-Bench 等基准测试中，该框架最高可带来 11.5 分的性能提升。Harness² 支持并行与顺序递归模式，已集成多款基准测试，并采用 Apache 2.0 许可证开源。

telegram · zaihuapd · 10月18日 11:24

**「背景」** 构建高效的 LLM 智能体通常需要进行模型微调或依赖外部工具链，这增加了开发成本和复杂度。递归优化思路曾被探索用于在推理阶段反复改进代理行为，但此前缺乏统一、易用的开源实现。

**「影响」** 开发者可以直接使用 Harness² 在不重新训练模型的情况下，在 WorkBuddy-Bench 等测试中获得最高 11.5 分的性能提升，从而加快 AI 代理的原型制作和实验迭代。

**标签**: `#AI agents`, `#recursive optimization`, `#open-source framework`, `#LLM tools`, `#Google Research`

---

<a id="item-tech-news-3"></a>
### [llm-echo 0.5 增加 reasoning tokens 支持并完善 token 计数](https://github.com/simonw/llm-echo/releases/tag/0.5) ⭐️ 7.5/10

simonw 发布了 llm-echo 0.5，该版本要求依赖 LLM 0.36 或更高版本。新增对 reasoning tokens 的支持，使得工具能够识别和计算模型推理过程中的 token。同时改进了模拟 token 用量统计，现在包含工具调用、推理文本以及系统提示词的 token 数。这些变化使得开发者在使用带有工具调用的大语言模型时可以获得更准确的 token 成本估算。

github · simonw · 10月18日 23:16

**「背景信息」** llm-echo 是 Simon Willison 开发的一个工具，用于模拟和测试 LLM（大语言模型）的交互行为。它依赖于同作者的 LLM Python 库，此次 0.5 版本要求 LLM &gt;= 0.36。该工具主要用于开发者在不调用真实 API 的情况下，模拟模型响应、工具调用和 token 计数等场景。

**「影响」** 开发者可以通过 llm-echo 0.5 更精确地预估使用带 reasoning 和 tool calls 的模型的 token 消耗，从而避免超额费用。

**标签**: `#ai-tools`, `#open-source`, `#llm-echo`, `#reasoning-tokens`

---

<a id="item-tech-news-4"></a>
### [Hybrid Reasoning Agents: LLM agents that think in latent space, act through text](https://arxiv.org/abs/2610.18861) ⭐️ 7.0/10

A paper from Together Computer proposing LLM agents that reason in latent space while acting through text, with open-source code and models available on GitHub and HuggingFace.

hackernews · allinonai · 10月18日 20:48 · [社区讨论](https://news.ycombinator.com/item?id=50145337)

**标签**: `#LLM agents`, `#reasoning`, `#latent space`, `#open-source`, `#arXiv paper`

---

<a id="item-tech-news-5"></a>
### [DeepSeek announces $0.75 per 1000 search API pricing](https://api-docs.deepseek.com/guides/search/) ⭐️ 7.0/10

DeepSeek announced a new search‑and‑fetch API priced at $0.75 per 1,000 successful requests, targeting developers and students building AI agents. The pricing is significantly lower than existing alternatives such as Brave Search API \($5 per 1,000\) and Kagi API \($12 per 1,000\). The service is currently an announced plan and not yet generally available.

hackernews · fagnerbrack · 10月18日 06:50 · [社区讨论](https://news.ycombinator.com/item?id=50138531)

**「Background」** AI agents often need real‑time web search, which is provided via search APIs. Competitors like Brave and Kagi have set higher rates, making search a notable cost for developers. DeepSeek’s lower price aims to reduce that expense.

**「Impact」** Developers, especially students building AI agents, can cut their search costs by up to ~85 % compared with Brave or Kagi, making web‑search integration more affordable.

**「Community discussion」** Some users point out that free, self‑hosted alternatives such as searxng‑ai‑kit already provide cost‑free search, while others highlight the stark price gap—$0.75 vs. $5 \(Brave\) and $12 \(Kagi\)—as a major competitive advantage.

**标签**: `#AI search API`, `#pricing`, `#agent tools`, `#cost comparison`

---

<a id="item-tech-news-6"></a>
### [Sphinx：AI 代码推送前的验证钩子](https://sphinx-six-theta.vercel.app/) ⭐️ 7.0/10

Sphinx 是一个新开源的钩子工具，可插入现有的编码智能体工作流，在每次推送到生产环境前弹出问卷，检查开发者是否理解所推送代码的工作原理。该工具面向使用 AI 编程工具的开发者，尤其是学生群体，旨在帮助他们在部署前确保对生成代码有充分理解。目前项目已在 Vercel 部署演示并开源。

hackernews · critiquebrowser · 10月18日 04:33 · [社区讨论](https://news.ycombinator.com/item?id=50137950)

**「背景」** 随着 AI 编程工具（如 Claude Code）的普及，开发者往往直接接受 AI 生成的代码而不深入理解其原理，这可能导致生产环境中的隐蔽问题。Sphinx 正是针对这一痛点而设计，它在 CI/CD 流程的推送环节增加了一道验证关卡，迫使开发者在部署前面对并回答关于代码行为的问题。

**「影响」** Sphinx 若被采用，可能迫使开发者在推送前花时间理解 AI 生成代码，从而减少因盲目信任 AI 而导致的生产事故。然而，它也可能成为开发流程中的额外摩擦点，如果问卷设计不当，可能降低团队效率。

**「社区讨论」** 社区评论中，开发者们对 AI 编程带来的“不读代码”问题表示认同，有人分享了因未审查 AI 输出而导致项目中途切换技术栈的经历。也有观点认为写一份高质量的 PR 描述是更自然的理解方式，而另一些人则质疑这类工具是否只是为现有工作流添加表面解决方案，而非根本解决问题。

**标签**: `#AI coding tools`, `#Open-source`, `#Developer workflow`, `#Student learning`, `#AI verification`

---

<a id="item-tech-news-7"></a>
### [asmsense 发布 22.8 万条带源标签的 x86-64 函数数据集和 Qwen3-8B 微调模型](https://www.reddit.com/r/MachineLearning/comments/1x91a47/p_asmsense_228k_stripped_x8664_functions_with/) ⭐️ 7.0/10

asmsense 开源项目发布了一个包含 228,177 条 x86-64 函数的带源标签数据集，并配套提供了基于 Qwen3-8B 的微调模型，用于为 stripped 状态的二进制文件命名函数。该数据集涵盖 341 个 C 项目，编译选项从 -O0 到 -Os，支持英文和土耳其文描述，目前仅支持 clang/Mach-O 平台（macOS），缺少 ARM64、RISC-V、MIPS 等架构及 GCC/ELF 构建。代码和数据均可在 GitHub 仓库获取。

reddit · r/MachineLearning · /u/luxurycashew · 10月18日 11:49

**「背景」** 在 stripped 状态下反汇编函数名一直是逆向工程和二进制分析中的难题，现有方法通常依赖启发式规则或小规模数据集。asmsense 通过汇集大量真实源代码项目和对应的反汇编结果，为模型提供了大规模的监督学习资源。

**「影响」** 研究人员和安全分析人员现在可以直接使用 asmsense 数据集和微调后的模型进行函数命名任务，但需要注意其当前仅支持 macOS/clang 环境，如果需要支持其他架构或链接器，还需等待项目补充相关数据。

**标签**: `#ai-tools`, `#open-source`, `#binary-analysis`, `#ml-research`

---