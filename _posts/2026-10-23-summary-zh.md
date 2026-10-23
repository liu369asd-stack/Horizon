---
layout: default
title: "Horizon Summary: 2026-10-23 (ZH)"
date: 2026-10-23
lang: zh
---

> 从 88 条内容中筛选出 15 条重要资讯。

---

**科技新闻**
1. [llama.cpp b11821 发布：针对 Intel XMX 矩阵引擎的多列优化与融合核函数](#item-tech-news-1) ⭐️ 8.0/10
2. [Open-XTTS-Trainer: 一键训练 XTTS v2 所有组件](#item-tech-news-2) ⭐️ 8.0/10
3. [甲骨文发布 Java SE 高危漏洞安全警报](#item-tech-news-3) ⭐️ 8.0/10
4. [小鹏 IRON 机器人升级：每 0.2 秒重新推理一次做出反馈](#item-tech-news-4) ⭐️ 7.5/10
5. [llama.cpp b11829 更新多平台二进制](#item-tech-news-5) ⭐️ 7.0/10
6. [LLMs are making formal software verification feasible at a much larger scale](#item-tech-news-6) ⭐️ 7.0/10
7. [OpenShell：NVIDIA 安全私有化 AI Agent 运行时](#item-tech-news-7) ⭐️ 7.0/10
8. [AI 与科学共享资源边界的分析](#item-tech-news-8) ⭐️ 7.0/10
9. [新三角化算法号称比 earcut 快：370 万多边形 489 毫秒](#item-tech-news-9) ⭐️ 7.0/10
10. [WorldTUI：360M 模型微调后可模拟终端界面](#item-tech-news-10) ⭐️ 7.0/10
11. [Donating Agent Skills to the Agentic AI Foundation](#item-tech-news-11) ⭐️ 7.0/10
12. [Modal 首席执行官：AI 计算的矩形 GPU 与弹性沙箱经济学](#item-tech-news-12) ⭐️ 7.0/10
13. [OlmoEarth v1.3: State-of-the-art embeddings for the whole planet](#item-tech-news-13) ⭐️ 7.0/10
14. [IBM Granite 时间序列集成预测模型](#item-tech-news-14) ⭐️ 7.0/10
15. [米哈游联合清华大学等开源 GameScaling 游戏操作模型](#item-tech-news-15) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [llama.cpp b11821 发布：针对 Intel XMX 矩阵引擎的多列优化与融合核函数](https://github.com/ggml-org/llama.cpp/releases/tag/b11821) ⭐️ 8.0/10

llama.cpp 于 2026 年 10 月 22 日发布 b11821 版本，针对 Intel XMX 矩阵引擎（int8 DPAS/ESIMD，SYCL 后端）重构了多列矩阵向量乘法，支持 2 至 80 个激活列，专门服务于投机解码验证（每步 2–8 token）与短提示批量推理（9–80 token）。该版本实现了融合的 gate/up 核函数，一次启动即可计算 FFN 两个权重的 up·act\(gate\)，覆盖最多 16 列并支持全部六种 XMX 类型；同时新增 GGML\_SYCL\_XMX\_MAX\_COLS（默认 80）与 GGML\_SYCL\_XMX\_GLU\_MAX\_COLS（默认 16）两个环境变量。在 B70 硬件上，Q4\_K\_M 的吞吐量从 26.67 tok/s 提升至 28.23 tok/s（+5.9%），Q6\_K 保持不变；批量为 1 时，启用 XMX 的困惑度为 5.2064，未启用时为 5.2058。此外，该版本修复了行列数非 4 的倍数时产生 NaN 的回归 bug，并重写了 xmx\_mul\_mat 以加入 64 字节对齐与 16 字节步长检查。

github · github-actions\[bot\] · 10月22日 17:02

**「背景」** llama.cpp 是一个开源的 LLM 推理项目，支持多种硬件后端（CPU、CUDA、ROCm、SYCL、Vulkan 等）。Intel XMX 矩阵引擎是英特尔 Arc 独显及部分酷睿 Ultra 处理器中的专用矩阵乘法硬件，llama.cpp 通过 SYCL 后端的 ESIMD 代码调用 int8 DPAS 指令来利用该硬件。此前版本已初步支持 XMX，但缺少针对多列激活场景（如投机解码与短批量提示）的优化，且存在一个导致 NaN 的回归 bug。

**「影响」** 对于在 Intel Arc 显卡或搭载 XMX 引擎的酷睿 Ultra 处理器上运行 llama.cpp 的用户与开发者，b11821 版本带来了实际的吞吐量提升（Q4\_K\_M 提升 5.9%）与 bug 修复，同时新增的环境变量允许用户按需调节融合核函数的最大列数，以在吞吐量与内存占用之间取得平衡。

**标签**: `#llama.cpp`, `#intel-xmx`, `#optimization`, `#ai-inference`

---

<a id="item-tech-news-2"></a>
### [Open-XTTS-Trainer: 一键训练 XTTS v2 所有组件](https://www.reddit.com/r/MachineLearning/comments/1xcurgj/i_built_openxttstrainer_now_you_can_add_new/) ⭐️ 8.0/10

Open-XTTS-Trainer 是一个基于 MPL-2.0 的开源框架，恢复了 Coqui AI 关闭后 XTTS v2 的 DVAE 音频 tokenizer 与 Latent HiFi‑GAN vocoder 的完整训练代码，并支持在单击 Google Colab 演示中添加阿拉伯语、印地语等新语言脚本进行全流程训练。该框架在 NVIDIA T4 GPU 上对真实人声数据验证了损失收敛，实现了 DVAE 和 HiFi‑GAN 的 67% 损失下降以及稳定的判别器平衡。

reddit · r/MachineLearning · /u/yashubhakt · 10月22日 21:03

**「背景」** Coqui AI 关闭后，XTTS v2 缺乏官方的 DVAE 和 HiFi‑GAN 训练流程，使得适配新语言脚本和本地微调变得困难。此前的代码缺失导致固定词表无法处理新 Unicode 字符，且升级 PyTorch 会因依赖冲突而中断。

**「影响」** 用户现在可以通过一键演示轻松训练全部三个组件并添加新语言脚本，从而实现本地零射 TTS 适配，而无需处理之前因词表固定和 PyTorch 依赖导致的兼容性问题。

**标签**: `#open-source`, `#AI-tools`, `#TTS`, `#training-framework`, `#language-support`

---

<a id="item-tech-news-3"></a>
### [甲骨文发布 Java SE 高危漏洞安全警报](https://www.oracle.com/security-alerts/alert-cve-2026-91403.html) ⭐️ 8.0/10

Oracle 发布 CVE-2026-91403 安全警报，该漏洞位于 Java SE 的 JSSE 组件，CVSS 评分 9.1，允许未认证远程代码执行。受影响版本包括 Java SE 8u511、11.0.33、17.0.21、21.0.13、25.0.5、27.0.1 及 GraalVM，Oracle 已提供修复补丁并建议用户尽快升级至受支持版本。

telegram · zaihuapd · 10月22日 12:30

**「背景」** 该漏洞影响 Oracle Java SE 产品线中多个长期支持的版本，属于 JSSE（Java Secure Socket Extension）组件层面的远程代码执行缺陷。由于 Java SE 是企业级应用和 AI/ML 生态系统的底层基础，此类漏洞对广泛部署的企业软件构成直接威胁。

**「影响」** 所有运行受影响 Java SE 版本（8u511 至 27.0.1）及 GraalVM 的系统均面临未认证远程攻击风险，攻击者可借此窃取数据或破坏完整性。建议立即升级至 Oracle 发布的修复版本以缓解风险。

**标签**: `#security`, `#Java`, `#vulnerability`, `#CVE-2026-91403`, `#Baoconv`

---

<a id="item-tech-news-4"></a>
### [小鹏 IRON 机器人升级：每 0.2 秒重新推理一次做出反馈](https://www.ithome.com/1/016/667.htm) ⭐️ 7.5/10

Phoenix Auto upgrades its IRON humanoid robot with real-time VLA model reasoning every 0.2 seconds to predict and adapt to immediate human actions, marking a key step in embodied AI deployment.

telegram · zaihuapd · 10月22日 13:37

**标签**: `#AI tools`, `#robotics`, `#large language models`, `#embodied AI`

---

<a id="item-tech-news-5"></a>
### [llama.cpp b11829 更新多平台二进制](https://github.com/ggml-org/llama.cpp/releases/tag/b11829) ⭐️ 7.0/10

面向本地大模型部署的开发者和用户来说，llama.cpp 发布了 b11829，这个版本包含 server 中 rerank 占位符的替换，并更新了 macOS、iOS、Linux、Android 和 Windows 等平台的平台二进制。新资产覆盖 Apple Silicon ARM64、Intel x64、iOS XCFramework，以及 Ubuntu 的 CPU、Vulkan、CUDA、ROCm、OpenVINO 和 SYCL 等版本。

github · github-actions\[bot\] · 10月22日 23:43

**「背景」** llama.cpp 是一个流行的开源 C++ 库，用于在消费级硬件上本地运行大语言模型（LLM），无需 GPU 或云端基础设施。为降低部署门槛，该项目在每个版本中都会提供覆盖 macOS、iOS、Linux、Android 和 Windows 等平台的预编译二进制包，支持 CPU、CUDA、Vulkan、ROCm、OpenVINO 等多种后端。b11829 版本延续了这一做法，并在既有发布节奏上进一步扩展了支持的硬件架构与后端组合。

**「影响」** 对受影响用户而言，b11829 提供了更多可下载的本地推理二进制，并给 macOS Apple Silicon、iOS 和 Linux 部署带来新的可用性选择。不过，当前发布中 Apple Silicon 的 KleidiAI 启用版和 openEuler 构建被列为 DISABLED，分别对应 PR 23780 和 PR 23705，需要关注后续兼容性。

**标签**: `#open-source`, `#AI-tools`, `#local-inference`, `#platform-support`

---

<a id="item-tech-news-6"></a>
### [LLMs are making formal software verification feasible at a much larger scale](https://www.anthropic.com/research/formal-verification) ⭐️ 7.0/10

Anthropic reports on LLMs making formal software verification feasible at larger scales, with early findings and debate about agent-generated proofs.

hackernews · johnbender · 10月22日 22:54 · [社区讨论](https://news.ycombinator.com/item?id=50202217)

**标签**: `#formal verification`, `#AI coding agents`, `#LLM research`, `#Rocq`

---

<a id="item-tech-news-7"></a>
### [OpenShell：NVIDIA 安全私有化 AI Agent 运行时](https://github.com/NVIDIA/OpenShell) ⭐️ 7.0/10

NVIDIA 发布 OpenShell，一个面向自主 AI Agent fleet 的开源安全运行时。它在不给予 Agent 无限制的数据、秘密或网络访问权的情况下，赋予 Agent 读取文件、安装包、调用 API 以及使用凭据的能力。

hackernews · niemandhier · 10月22日 17:44 · [社区讨论](https://news.ycombinator.com/item?id=50198675)

**「背景」** NVIDIA OpenShell 是一个开源安全运行时，旨在为自主 AI 代理提供零信任沙箱、可证明策略和隐私路由，以防止数据外泄等安全风险。该项目应运而生是因为 AI 代理在执行过程中可能面临数据窃取、凭证泄露等问题，如最近的模型泄露事件所示。OpenShell 通过在内核级别实现安全隔离和可审计的执行环境，为组织管理 AI 代理团队提供了更安全的基础设施。

**「治理控制的实际效果」** OpenShell 的运行时治理可在代理意外行为时自动收回权限，从而限制错误或安全事件的传播范围；但用户仍需配合网络域白名单和凭据管理，以防止代码库或敏感数据被外泄，因为运行时的访问控制并非涵盖所有交互路径的完整防护。

**「社区讨论」** 社区讨论中，smallnix 指出给予 Agent 更多访问权能提升能力，但也带来安全风险，这体现了‘能力与安全的权衡’这一核心冲突。其他用户则提到使用 iron proxy、容器化以及团队策略层来弥补 OpenShell 的边界限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.devops.dev/inside-nvidia-openshell-zero-trust-runtime-security-for-autonomous-ai-agents-a93afed026af">Inside NVIDIA OpenShell : Zero-Trust Runtime Security ... | DevOps.dev</a></li>
<li><a href="https://www.linkedin.com/pulse/nvidia-openshell-microsoft-mxc-new-secure-runtime-ai-agents-broschk-ljece?tl=en">NVIDIA OpenShell + Microsoft MXC: A New Secure Runtime for...</a></li>
<li><a href="https://www.1950.ai/post/nvidia-builds-a-security-layer-for-autonomous-ai-agents-can-now-be-monitored-and-quarantined-in-mil">NVIDIA Builds a Security Layer for Autonomous AI , Agents Can...</a></li>
<li><a href="https://developer.nvidia.com/blog/how-nvidia-openshell-reference-architecture-secures-and-governs-ai-agent-workloads-at-scale/">How NVIDIA OpenShell Reference Architecture Secures and ...</a></li>
<li><a href="https://www.nvidia.com/en-us/ai/openshell/">NVIDIA OpenShell | Open, Secure Runtime for AI Agents</a></li>
<li><a href="https://www.nvidia.com/en-us/solutions/ai/agent-safety/">NVIDIA Open Agent Safety Platform: Secure AI Agents</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#open-source software`, `#agent frameworks`, `#NVIDIA`

---

<a id="item-tech-news-8"></a>
### [AI 与科学共享资源边界的分析](https://arxiv.org/abs/2610.27251) ⭐️ 7.0/10

该文章从概念和政策角度审视了 AI 技术对科学共享资源边界的影响，并就开源许可与所有权展开了辩论。文章并非报道具体的技术突破或版本更新，而是分析了开源模型在科学数据共享中的定位与争议。

hackernews · jrepinc · 10月22日 18:28 · [社区讨论](https://news.ycombinator.com/item?id=50199230)

**「相关概念背景」** 科学公共资源是指研究社区共享、自由使用、修改和再分发的知识资源。开源与创意共享许可证框架（如开源倡议和创意共享的指引所阐述的）为 AI 模型和数据集的共享设定了使用、研究、修改和再分发的基本自由，这直接关联关于科学公共资源是否被封闭的争论。因此，这些许可证框架是理解本文讨论的先决语境。

**「社区讨论」** 社区中有评论认为文章将开源等同于 GPL copyleft，忽略了宽松许可证和企业资金在实际开源生态中的主导地位，这对信息共 Commons 的形成有关键影响。另有一评论质疑‘无人所有’的表述在实际共享时会面临全球法律执法压力，认为其作为文章基础的合理性存疑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://creativecommons.org/ai-and-the-commons/">AI and the Commons - Creative Commons</a></li>
<li><a href="https://opensource.org/wp-content/uploads/2025/08/AI-Policy-and-Open-Source.pdf">AI Policy and Open Source FINAL</a></li>

</ul>
</details>

**标签**: `#AI open source`, `#scientific commons`, `#open-source licensing`, `#AI policy`

---

<a id="item-tech-news-9"></a>
### [新三角化算法号称比 earcut 快：370 万多边形 489 毫秒](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 7.0/10

一篇发布于 Globus Software 的博文介绍了一种开源地图多边形三角化算法，号称处理速度超过 earcut。作者称在测试数据集上，该算法三角化 370 万个地图多边形耗时 489 毫秒。这一性能数据来自博主自行发布的测试，尚未见独立复现。博文同时公开了相关数据集，供外部核对与比较。

hackernews · molind · 10月22日 09:31 · [社区讨论](https://news.ycombinator.com/item?id=50193170)

**「背景」** 地图多边形三角化是将复杂多边形（包括带孔洞的多边形）分解为三角形，以便 GPU 渲染，是 Web 地图和 GIS 系统处理矢量数据的基础步骤。Earcut 是该领域广泛采用的开源 JavaScript 三角化库，其作者在社区评论中称代码体积约为 4.1 KB 压缩后，在大多数实用场景中已足够快。这一现有方案构成了理解新算法性能对比的基准。

**「影响」** 需要处理超大规模地图多边形集的开发者可以将该开源算法及其公开数据集作为新的性能参考点，但在采用前仍需自行验证其 WASM 体积、API 约束与 earcut 等现有方案的对比结果。

**「社区讨论」** earcut 作者 mourner 指出其有意放弃部分优化以控制体积（4.1 KB min/gz），认为对大多数实用场景已足够快，并好奇新库的 WASM 构建体积；Delaunay32 作者 morishuz 表示其当前多边形 API 仅支持简单环及非相交洞，尚未在该数据集上基准测试。读者 mistercow 则质疑为何耳削法胜过塞德尔梯形方法，推测可能与三角形质量或斜角三角形有关，但这仅为个人观点。

**标签**: `#computational-geometry`, `#map-triangulation`, `#open-source`, `#performance-optimization`

---

<a id="item-tech-news-10"></a>
### [WorldTUI：360M 模型微调后可模拟终端界面](https://simedw.com/2026/10/21/world-model-terminal/) ⭐️ 7.0/10

开发者 simedw 发布 WorldTUI 项目，对一个 360M 参数模型进行微调，使其能够模拟终端（TUI）界面；作者在评论中说明，起点模型为 Qwen2.5-Coder-0.5B，选用小模型是为了接近实时性能。这是一个由用户输入驱动、由模型生成界面输出的演示，而非真实操作系统；目前仅以博文形式发布，未确认开源代码或公开演示的可用性。

hackernews · alphax314 · 10月22日 02:18 · [社区讨论](https://news.ycombinator.com/item?id=50190363)

**「神经计算机与生成式终端项目背景」** 本项目建立在“神经计算机”（Neural Computer）理论之上，该理论提出整个交互界面由用户输入驱动并由神经网络预测像素输出构成。通过对 360M 参数模型的微调，作者实现了一个无实际文件系统的终端模拟，用户每按键都触发屏幕变化的预测。

**「影响」** 受影响的开发者可以将其作为小模型驱动生成式界面的参考实现；社区评论指出，微调后该 360M 模型的记忆能力提升显著，为探索由用户输入循环生成界面输出的“神经计算机”概念提供了具体数据点。

**「社区讨论」** 社区讨论的焦点在于该项目是否属于“神经计算机”：评论者 gavinray 认为它是该概念的微型实现，整个界面由用户输入到预测像素输出的循环驱动，理论上完美版本与真实计算机无法区分；评论者 nico 则介绍了类似主题的“丢失式 Git”项目，即用神经网络存储代码并在检出时生成代码。以上观点均为评论者个人看法，非经独立验证的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simedw.com/2026/10/21/world-model-terminal/">WorldTUI : I trained a 360 M model to pretend to be a terminal</a></li>

</ul>
</details>

**标签**: `#AI tools`, `#LLM`, `#generative UI`, `#open-source`, `#hands-on project`

---

<a id="item-tech-news-11"></a>
### [Donating Agent Skills to the Agentic AI Foundation](https://simonwillison.net/2026/Oct/22/donating-agent-skills/) ⭐️ 7.0/10

Anthropic announced it is donating its Agent Skills standard to the Agentic AI Foundation under the Linux Foundation, continuing its open, community-driven approach alongside the Model Context Protocol donation.

rss · Simon Willison · 10月22日 18:09

**标签**: `#Agent Skills`, `#Agentic AI Foundation`, `#Model Context Protocol`, `#Open Standards`, `#AI Agents`

---

<a id="item-tech-news-12"></a>
### [Modal 首席执行官：AI 计算的矩形 GPU 与弹性沙箱经济学](https://www.latent.space/p/modal-d) ⭐️ 7.0/10

本文分析了 AI 计算为何以矩形 GPU 单元形式出现，并探讨了弹性 GPU 沙箱与 Agent Cloud 的经济模型。文章指出这些模型对用户（如学生）的访问成本具有相关性，但未报道具体的技术突破或已部署的能力。

rss · Latent Space · 10月22日 17:40

**「背景」** AI 计算历史上依赖物理 GPU 硬件单元，而弹性沙箱和云端 Agent 模型则是近期云计算中尝试提升资源利用率和访问灵活性的方案。

**「影响」** 文章提到这些经济模型可能影响学生等用户的 AI 计算访问成本，但未提供具体的测量结果或已部署的影响。

**标签**: `#AI compute economics`, `#GPU elasticity`, `#Agent cloud`, `#Practical AI access`

---

<a id="item-tech-news-13"></a>
### [OlmoEarth v1.3: State-of-the-art embeddings for the whole planet](https://huggingface.co/blog/allenai/olmoearth-v1-3) ⭐️ 7.0/10

Allen AI releases OlmoEarth v1.3, an open-source foundation model that generates state-of-the-art embeddings for the entire planet&\#x27;s satellite imagery.

rss · Hugging Face Blog · 10月22日 16:11

**标签**: `#open-source`, `#model-release`, `#geospatial-ai`, `#earth-observation`, `#embeddings`

---

<a id="item-tech-news-14"></a>
### [IBM Granite 时间序列集成预测模型](https://huggingface.co/blog/ibm-research/granite-timeseries-ensemble-r1) ⭐️ 7.0/10

IBM Granite 发布了面向时间序列的集成预测模型。这些模型作为开源发布，可在 Hugging Face 平台上获取，旨在为学生和研究人员提供易于上手的预测工具。该发布扩展了开源时间序列预测工具的可及性。

rss · Hugging Face Blog · 10月22日 07:51

**「背景概述」** 时间序列 ensemble forecasting 通过集成多个基模型，旨在提升预测的精度与不确定性量化的可靠性。IBM Granite 近期发布了新的时间序列模型，旨在为开源社区和学生提供易用的 ensemble 预测能力。此类开源模型的发布有助于降低先进预测技术的使用门槛。

**标签**: `#time-series`, `#IBM Granite`, `#ensemble forecasting`, `#open-source`, `#model-release`

---

<a id="item-tech-news-15"></a>
### [米哈游联合清华大学等开源 GameScaling 游戏操作模型](https://arxiv.org/abs/2610.28698v1) ⭐️ 7.0/10

MiHoYo and Tsinghua release GameScaling, an AI model that predicts future mouse/keyboard actions using Qwen3.5, providing open‑source checkpoints and an inference client for game‑control research.

telegram · zaihuapd · 10月22日 11:32

**标签**: `#Game AI`, `#Open-source AI`, `#Qwen3.5`, `#Action prediction`

---