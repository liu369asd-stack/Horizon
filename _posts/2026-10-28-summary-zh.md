---
layout: default
title: "Horizon Summary: 2026-10-28 (ZH)"
date: 2026-10-28
lang: zh
---

> 从 96 条内容中筛选出 14 条重要资讯。

---

**科技新闻**
1. [ggml-org/llama.cpp released b11946](#item-tech-news-1) ⭐️ 8.0/10
2. [ggml-org/llama.cpp released b11928](#item-tech-news-2) ⭐️ 8.0/10
3. [Anthropic Opus 5.5 与 Claude 平台：AI Agent 工程与“大脑—手”分离](#item-tech-news-3) ⭐️ 8.0/10
4. [Anthropic 如何安全部署世界顶尖 LLM：将大脑与手分离](#item-tech-news-4) ⭐️ 8.0/10
5. [Papers with Code 发布 Apache 2.0 开源](#item-tech-news-5) ⭐️ 8.0/10
6. [Ψ-0.6: 自适应多模推理世界模型发布](#item-tech-news-6) ⭐️ 8.0/10
7. [OpenAI Codex Rust v0.165.0 发布，新增 Vertex AI 提供商和 GPT-6.1 Terra 支持](#item-tech-news-7) ⭐️ 7.0/10
8. [Genie 4 世界模拟与视频生成的最新进展](#item-tech-news-8) ⭐️ 7.0/10
9. [Survival LLM：可在本地运行的离线 AI 助手](#item-tech-news-9) ⭐️ 7.0/10
10. [使用 OpenCode、Ollama 和 Qwen 搭建离线 AI 编码代理](#item-tech-news-10) ⭐️ 7.0/10
11. [LFM3 专用多模态模型构建](#item-tech-news-11) ⭐️ 7.0/10
12. [First 6-step LoRA adapters with no upsampling step, ~5x faster \[N\]](#item-tech-news-12) ⭐️ 7.0/10
13. [🤖 Google 发布世界模型 Genie 4，实时生成画面音频与对话](#item-tech-news-13) ⭐️ 7.0/10
14. [Google 提出睡眠框架，助大模型持续学习不遗忘](#item-tech-news-14) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [ggml-org/llama.cpp released b11946](https://github.com/ggml-org/llama.cpp/releases/tag/b11946) ⭐️ 8.0/10

llama.cpp b11946 introduces a self-contained /v1/realtime endpoint for realtime conversation and transcription, making voice-style AI interactions possible on a self-hosted server.

github · github-actions\[bot\] · 10月28日 01:58

**标签**: `#llama.cpp`, `#realtime API`, `#open-source`, `#LLM inference`, `#self-hosted`

---

<a id="item-tech-news-2"></a>
### [ggml-org/llama.cpp released b11928](https://github.com/ggml-org/llama.cpp/releases/tag/b11928) ⭐️ 8.0/10

Adds MiniCPM-OCR-Jev OCR support to llama.cpp, enabling image-based text scoring on Qwen3.5-VL models through the MCP ecosystem.

github · github-actions\[bot\] · 10月27日 12:30

**标签**: `#OCR`, `#llama.cpp`, `#minicpm-ocr-jev`, `#multimodal`, `#open-source`

---

<a id="item-tech-news-3"></a>
### [Anthropic Opus 5.5 与 Claude 平台：AI Agent 工程与“大脑—手”分离](https://latent.space/p/opus55/) ⭐️ 8.0/10

swyx.ai 于 2026 年 10 月 27 日发布技术深度文章，邀请 Anthropic 的 Katelyn Lesse 和 Angela Jiang 讨论 Opus 5.5 与 Claude 平台，重点阐述 AI Agent 的工程实现。文章以“大脑与手分离”为框架，探讨如何将模型推理与执行操作解耦以交付 Claude。由于来源仅提供访谈标题与简短描述，未披露具体版本、发布状态或可验证的性能数据，具体技术细节仍需以原文为准。

rss · Latent Space · 10月27日 18:53

**「背景」** Anthropic 的 Claude 是其大语言模型产品，Opus 5.5 是文中讨论的平台或模型版本。AI Agent 工程通常需要在模型推理与实际操作执行之间建立接口，即所谓的“大脑”与“手”的分离。本文属于工程实践分享，而非产品发布公告或独立基准测试。

**标签**: `#Anthropic`, `#AI agents`, `#platform engineering`, `#Claude`, `#AI tools`

---

<a id="item-tech-news-4"></a>
### [Anthropic 如何安全部署世界顶尖 LLM：将大脑与手分离](https://latent.space/p/how_anthropic_ships_the_1_llm_in_the_world_safely_separating_the_brain_from_the_hands/) ⭐️ 8.0/10

Anthropic 发布 Opus 5.5，通过将模型的‘脑’与代理的‘手’分离，并扩展 API 基础设施，实现了更安全的大规模部署。该架构将模型推理与代理动作解耦，旨在提升可靠性和安全性。该变更旨在为 Claude 平台的管理代理提供更可预测的行为边界。

rss · Latent Space · 10月27日 18:40

**「背景」** 以往 LLM 部署中，模型推理往往直接驱动外部代理动作，缺乏中间层隔离，可能导致不可预测的行为风险。此前的系统多为统一架构，难以在同一模型实例中灵活分离推理与执行。

**「影响」** 使用 Claude 平台的开发者可利用 Opus 5.5 的脑-手分离架构，在代理任务中获得更可预测的行为边界，从而降低因模型自主动作导致的安全风险。但迁移至新架构可能需要调整现有代理代码以适配新的脑-手接口。

**标签**: `#LLM`, `#AI safety`, `#Opus 5.5`, `#Agent architecture`, `#API scaling`

---

<a id="item-tech-news-5"></a>
### [Papers with Code 发布 Apache 2.0 开源](https://www.reddit.com/r/MachineLearning/comments/1xgoadu/papers_with_code_is_now_opensource_p/) ⭐️ 8.0/10

Papers with Code 已根据 Apache 2.0 许可开源，使其完整的全栈平台可供公众使用。该复兴项目包括一个 Python FastAPI 后端、一个 React 前端和一个 MCP 服务器，所有代码均托管在一个 Hetzner 虚拟服务器上的单一仓库中，并可通过 https://github.com/huggingface/paperswithcode 访问。这恢复了被 Meta 收购后下线的原始 AI 研究追踪网站，允许社区进行贡献和自托管。

reddit · r/MachineLearning · /u/NielsRogge · 10月27日 09:54

**「背景」** 原始的 Papers with Code 网站是一个为社区提供 AI 研究论文、基准测试和最先进结果追踪的服务。Meta 收购该项目后将其下线，导致开放 AI 研究发现工具出现空白。新开源版本旨在填补这一空白，提供一个协作式、全栈式平台。

**「影响」** Apache 2.0 许可和公开的代码仓库使学生和研究人员能够 fork、修改和托管自己的实例，将该平台转变为一个可供贡献的 AI 基准测试资源。

**标签**: `#open-source`, `#AI research tracking`, `#MCP ecosystem`, `#community contribution`

---

<a id="item-tech-news-6"></a>
### [Ψ-0.6: 自适应多模推理世界模型发布](https://www.reddit.com/r/MachineLearning/comments/1xgwq9u/%CF%8806_adaptive_streams_of_thought_in_a_unified/) ⭐️ 8.0/10

Ψ-0.6 是一个开源统一世界模型，它学习自适应多模推理流，并在空间推理（MindCube）和动力学预测（FlowBench）中表现出色，同时实现了从仿真到真实机器人桌面操作的迁移。该模型能够在文本、深度、运动、相机姿态和想象场景之间自适应推理，并使用强化学习选择合适的表示方式。论文、代码和网站均已公开。

reddit · r/MachineLearning · /u/FaeriaManic · 10月27日 16:09 · [社区讨论](https://www.reddit.com/r/MachineLearning/comments/1xgwq9u/%CF%8806_adaptive_streams_of_thought_in_a_unified/)

**「背景」** 思维链推理通过将复杂问题分解为连续的文本步骤，改变了 AI 问题解决方式，但仍局限于语言本身。Ψ-0.6 通过引入跨多模态的自适应思维流来解决这一局限——包括文本、深度图、运动模式、相机姿态和想象场景——并使用强化学习来学习在给定任务中通过哪种表示进行推理。这建立在先前统一视觉-语言模型和具身 AI 世界模型的工作基础上，将推理从文本扩展到物理世界。

**「影响」** 对于跟踪多模态智能体和具身人工智能工具的学生和研究者来说，Ψ-0.6 提供了一个实用的开源解决方案，可用于空间推理和机器人控制等任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/datasets/MLL-Lab/MindCube">MLL- Lab / MindCube · Datasets at Hugging Face</a></li>
<li><a href="https://www.epfl.ch/labs/schrimpflab/">EPFL NeuroAI Lab ‐ EPFL</a></li>
<li><a href="https://github.com/chung-neuroai-lab">chung- neuroai - lab · GitHub</a></li>

</ul>
</details>

**标签**: `#world-models`, `#multimodal-reasoning`, `#robotics`, `#open-source`, `#embodied-ai`

---

<a id="item-tech-news-7"></a>
### [OpenAI Codex Rust v0.165.0 发布，新增 Vertex AI 提供商和 GPT-6.1 Terra 支持](https://github.com/openai/codex/releases/tag/rust-v0.165.0) ⭐️ 7.0/10

OpenAI Codex Rust 版本 v0.165.0 发布，新增内置 Google Cloud Vertex AI 提供商和 GPT-6.1 Terra 模型支持，并优化了会话选择器、代理命令中心及记忆功能。版本还修复了 TUI 会话默认审核人处理、MCP 工具请求取消及 marketplace URL 验证等多个问题。

github · github-actions\[bot\] · 10月27日 20:09

**「背景」** OpenAI Codex 是一个用于 AI 代码生成的 Rust 项目，提供模型供应商目录、会话管理和代理功能。此次发布基于 v0.164.0 版本，进一步扩展了供应商支持并改善了用户体验。

**「影响」** 开发者现在可直接通过 \`model\_provider = &quot;gcp&quot;\` 配置使用 Google Cloud Vertex AI 模型，简化了多云环境下的部署，同时新用户默认获得 Memory v2 版本，提升了对话记忆的持久性。

**标签**: `#openai-codex`, `#ai-coding-tools`, `#agents`, `#model-releases`

---

<a id="item-tech-news-8"></a>
### [Genie 4 世界模拟与视频生成的最新进展](https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/) ⭐️ 7.0/10

Google DeepMind 的 Genie 4 在世界模拟和视频生成方面取得了改进，使得帧内一致性更好、视频更具写实感。但该模型仍在帧外一致性、音频质量以及对特定提示的敏感性上表现不佳，例如音频常出现口琴而非萨克斯的错误。此外，开源竞争者 HY-World 2.0 的权重模型也未受到同等关注。

hackernews · acossta · 10月27日 16:06 · [社区讨论](https://news.ycombinator.com/item?id=50261319)

**「背景」** 世界模拟的核心挑战是保持多个连续帧中对象的形态和位置一致。Genie 4 在此基础上改进了帧内一致性，但仍未解决帧外一致性和音频质量等问题。

**「影响」** 开发者在使用 Genie 4 进行高质量视频生成时，需要额外校正帧外细节和音频，或在提示中加入更具体的约束，否则输出可能出现视觉或音频不一致的情况。

**「社区讨论」** 评论员表示 Genie 4 在帧外细节和音频质量上仍有明显问题，如人物细节在离开画面后改变或出现口琴而非萨克斯的错误，而其他用户则认为其帧内一致性已显著提升。

**标签**: `#world-simulation`, `#video-generation`, `#open-source-competition`

---

<a id="item-tech-news-9"></a>
### [Survival LLM：可在本地运行的离线 AI 助手](https://www.brangus.io/survival-llm) ⭐️ 7.0/10

Survival LLM 是一款可在用户本机运行、面向离线与紧急场景的 AI 助手和资料库，由 Luc 介绍，并通过社区测试与真实工作流场景展示使用。社区成员在本机部署后测试了弓钻生火等问题，模型部分答案正确，但在关键步骤上出现错误，说明离线运行并未消除幻觉限制。该项目定位为在无网络环境下检索与使用自有知识的工具，而非可完全信赖的专业建议来源。

hackernews · Luc · 10月27日 19:55 · [社区讨论](https://news.ycombinator.com/item?id=50264853)

**「背景」** 常见的 AI 助手通常运行在云端服务器上，使用时需要联网，且用户的提问会发送到第三方。本地大语言模型（Local LLM）则将模型和资料库直接安装在用户自己的计算机中，支持离线运行，数据不离开设备。Survival LLM 采用这种本地化方式，将紧急求生知识装在用户电脑里，以便在断网或紧急情况下查阅。

**「影响」** 没有稳定移动网络的用户可以将本地模型与自行整理的书籍、文章配合使用，在断网时支持工作；但社区测试显示模型在生存技能等关键问题上仍可能出错，用户不应将其作为未经核实的紧急建议来源。

**「社区讨论」** 评论者 x3haloed 认为，LLM 应当被当作语义搜索与信息检索工具使用，而不应盲信其给出的具体建议，尤其在用户不知道该问什么时更有用；另一位评论者 wanderingbit 则通过亲测弓钻生火说明，模型可能在关键步骤上出错，印证了不能完全依赖其输出的局限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.brangus.io/survival-llm">Survival LLM</a></li>
<li><a href="https://github.com/anonnerdfrenzy/survival-llm">anonnerdfrenzy/ survival - llm : A free AI assistant and survival library ...</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#offline-ai`, `#practical-ai-tools`, `#open-source-ai`

---

<a id="item-tech-news-10"></a>
### [使用 OpenCode、Ollama 和 Qwen 搭建离线 AI 编码代理](https://latent.space/p/offline-coding/) ⭐️ 7.0/10

本文提供了使用 OpenCode、Ollama 和 Qwen 搭建离线 AI 编码代理的教程。文章面向希望在离线环境中进行 AI 辅助开发的开发者。

rss · Latent Space · 10月27日 14:41

**「离线 AI 代码代理的背景」** OpenCode 是一个开源的 AI 代码助手，可通过 Ollama 与本地大语言模型集成，使开发者能够在本地硬件上运行 AI 代理，而无需依赖云端服务。Ollama 提供了一个运行和管理开源模型的平台，Qwen 则是专为代码任务优化的语言模型家族。借助这些工具，开发者可以构建一个完全离线的代码代理，既保护了代码隐私，又降低了延迟。

**「影响」** 本指南使开发者能够在无网络环境下搭建和运行 AI 编程助手，对于网络基础设施薄弱或受限的偏远地区开发者（如喜马拉雅山区），意味着可以本地部署开源工具链（OpenCode、Ollama、Qwen）进行编程辅助，无需依赖云端服务或支付订阅费用。这降低了 AI 编程工具的使用门槛，使离线环境下的开发者也能受益于 AI 辅助编程，回应了 AI Agent 部署中延迟和连接依赖的普遍挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=HOQkuYRwlVI">Qwen 3.5 + OpenCode + Ollama : Easy Setup Guide for... - YouTube</a></li>
<li><a href="https://www.kdnuggets.com/seeing-whats-possible-with-opencode-ollama-qwen3-coder">Seeing What’s Possible with OpenCode + Ollama + Qwen 3- Coder</a></li>
<li><a href="https://dev.to/ferdousulhaque/opencode-for-agentic-development-with-local-llms-2h4k">Opencode for Agentic Development with Local LLMs - DEV Community</a></li>
<li><a href="https://www.langchain.com/stateofaiagents">LangChain State of AI Agents Report: 2024 Trends</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#offline AI`, `#open-source AI tools`, `#local LLMs`

---

<a id="item-tech-news-11"></a>
### [LFM3 专用多模态模型构建](https://huggingface.co/blog/LiquidAI/lfm3) ⭐️ 7.0/10

Hugging Face Blog 于 2026-10-27 发布了一篇关于 Liquid AI LFM3 多模态模型的文章，介绍如何构建专用的多模态模型。文章面向开发者和研究人员，但元数据未公开模型权重、开放许可、具体教程或性能数据，读者需自行评估适用性。

rss · Hugging Face Blog · 10月27日 17:16

**「背景：液态神经网络与 LFM 系列模型」** Liquid AI 基于液态神经网络架构开发基础模型，该架构采用连续时间动力学系统，能根据输入自适应调整计算。此前发布的 LFM 系列（如 LFM-1B、LFM-3B、LFM-40B）在语言任务上展现了参数效率优势。LFM3 将这一架构扩展至多模态领域。

**「本地单 GPU 微调多模态模型」** LFM‑3 发布了一套六个开源的 20 亿参数多模态模型，开发者可以在单 GPU 上微调每个模型，从而在消费级设备和边缘硬件上本地运行专业化的多模态 AI，无需依赖云端资源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.liquid.ai/blog/lfm3">Introducing LFM 3 : Every Modality for Specialized Intelligence | Liquid AI</a></li>
<li><a href="https://mozgi.io/news/auto-mvr1xe7v-fg3p/?lang=en">Liquid AI has released the LFM 3 model family with 2 billion parameters</a></li>
<li><a href="https://www.marktechpost.com/2026/10/27/liquid-ai-lfm3-open-weight-2b-multimodal-models/">Liquid AI Releases LFM 3 : 6 Open-Weight 2B-Class Multimodal ...</a></li>

</ul>
</details>

**标签**: `#LFM3`, `#multimodal models`, `#foundation model release`, `#model specialization`

---

<a id="item-tech-news-12"></a>
### [First 6-step LoRA adapters with no upsampling step, ~5x faster \[N\]](https://www.reddit.com/r/MachineLearning/comments/1xgye14/first_6step_lora_adapters_with_no_upsampling_step/) ⭐️ 7.0/10

Announcement of 6-step LoRA adapters for Qwen-Image-2.1 that remove the upsampling step, offering ~5x speedup for image generation and editing.

reddit · r/MachineLearning · /u/sdiazlor · 10月27日 17:09

**标签**: `#AI image generation`, `#LoRA`, `#open-source`, `#diffusion models`

---

<a id="item-tech-news-13"></a>
### [🤖 Google 发布世界模型 Genie 4，实时生成画面音频与对话](https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/) ⭐️ 7.0/10

Google DeepMind released Genie 4, a world model that generates real-time video, audio, and interactive dialogue controllable by natural language, now in research preview for trusted testers.

telegram · zaihuapd · 10月27日 16:28

**标签**: `#world models`, `#real-time generation`, `#Gemini`, `#interactive AI`, `#research preview`

---

<a id="item-tech-news-14"></a>
### [Google 提出睡眠框架，助大模型持续学习不遗忘](https://research.google/blog/the-sleep-framework-a-new-way-for-llms-to-retain-knowledge-in-continual-learning/) ⭐️ 7.0/10

Google Research 发布了一种名为“睡眠框架”的新方法，用于大语言模型的持续学习。该框架通过在主动交互与离线巩固之间交替训练，在 1000 万 token 长上下文、持续翻译和数学推理等任务上表现优于 GPT-4 和 SFT 等基线，旨在缓解灾难性遗忘问题。该方法从人类睡眠中的记忆巩固机制获得灵感，通过离线阶段将短期上下文固化为长期参数，目前还未开放源代码或可直接使用的工具。

telegram · zaihuapd · 10月28日 01:46

**「背景」** 大语言模型在持续学习过程中容易出现灾难性遗忘，即新任务训练会抹去先前学到的知识。睡眠框架借鉴了睡眠期间的记忆巩固现象，引入离线巩固阶段以稳定模型参数。

**「影响」** 对于研究人员和工程团队而言，这一框架提供了一种新的手段来减少模型在持续学习中的遗忘，并在长上下文理解和数学推理等任务上取得更优表现，但目前仍停留在研究阶段，尚未形成可直接部署的工具。

**标签**: `#LLM continual learning`, `#catastrophic forgetting`, `#Google Research`, `#sleep framework`, `#AI research`

---