---
layout: default
title: "Horizon Summary: 2026-10-31 (ZH)"
date: 2026-10-31
lang: zh
---

> 从 64 条内容中筛选出 6 条重要资讯。

---

**科技新闻**
1. [基于~1GB Qwen 权重的可工作 NES 模拟器](#item-tech-news-1) ⭐️ 8.0/10
2. [llama.cpp b12014 发布，新增 macOS/iOS 构建并修复 Windows 问题](#item-tech-news-2) ⭐️ 7.0/10
3. [llama.cpp b12002 发布批量张量复制 API 和 CUDA 支持](#item-tech-news-3) ⭐️ 7.0/10
4. [Bunny CDN Security Incident](#item-tech-news-4) ⭐️ 7.0/10
5. [Multi-Token Prediction Done Right \[R\]](#item-tech-news-5) ⭐️ 7.0/10
6. [Claude 重命名 Max 套餐并取消 Ultra 五小时限制](#item-tech-news-6) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [基于~1GB Qwen 权重的可工作 NES 模拟器](https://github.com/dbreunig/nesformer) ⭐️ 8.0/10

GitHub 项目 nesformer 发布了一个基于~1 GB Qwen 模型权重的可工作 NES（任天堂娱乐系统）模拟器。该模拟器不仅模拟 CPU，还通过门控 deltaNet 架构模拟了 RAM，但运行速度仅为真实主机的 150–290 倍。项目作者使用 Opus 5.5 仅用两个提示（参考 qwenputer 博客）即生成了模型权重和代码，展示了 LLM 驱动硬件仿真的可能性。

hackernews · dbreunig · 10月30日 16:40 · [社区讨论](https://news.ycombinator.com/item?id=50306442)

**「背景」** Qwenputer 是 divagr18 在 2026 年 10 月发布的实验性模型，它将一个 32 位 RISC-V CPU 直接编译进 Qwen3.5-4B 的权重中，全部参数由编译器计算而非通过训练学习得到。nesformer 的作者在项目说明中引用了 Qwenputer 的相关文章，并在此思路基础上尝试在模型权重内模拟任天堂 NES 的 6502 处理器与内存。

**「实际影响」** 该项目验证了利用~1 GB Qwen 权重进行 NES 硬件仿真的技术可行性，但实际运行速度仅为真实主机的 150–290 倍，这凸显了 LLM 驱动仿真在计算开销上的巨大差距，提醒开发者在追求 AI 硬件仿真时需权衡性能与资源成本。

**「社区讨论」** 社区评论指出，尽管该模拟器 technical 可行，但运行速度仅为真实主机的 150–290 倍，凸显了 LLM 驱动仿真在计算效率上的巨大落后。armcat 随后提出将 VM 编译进 LLM 权重可能带来新可能，但这仍属推测性构想。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/divagr18/qwenputer">GitHub - divagr18/ qwenputer : A computer, compiled into the...</a></li>

</ul>
</details>

**标签**: `#Open-source`, `#LLM`, `#Hardware emulation`, `#NES`, `#Qwen`

---

<a id="item-tech-news-2"></a>
### [llama.cpp b12014 发布，新增 macOS/iOS 构建并修复 Windows 问题](https://github.com/ggml-org/llama.cpp/releases/tag/b12014) ⭐️ 7.0/10

llama.cpp 项目发布了 b12014 版本，该版本移除了 Windows argv 重建功能并修复了 \#26416 问题，同时提供了针对 macOS、iOS、Linux、Android、Windows、openEuler 和 UI 的预构建二进制文件。该版本包含针对 macOS Apple Silicon \(arm64\) 和 Intel \(x64\) 的二进制文件，以及 iOS XCFramework，Linux 提供了多种 CPU/GPU/加速器变体（包括 CUDA 12/13、Vulkan、ROCm、OpenVINO、SYCL）等。支持平台的用户现在可以下载相应的 tar 包或 zip 文件来运行本地 LLM 推理，无需从源码构建。

github · github-actions\[bot\] · 10月30日 15:29

**「背景」** llama.cpp 是一个用于在各种硬件上运行大型语言模型的开源 C/C++ 推理引擎。b12014 版本在此基础上进一步扩展了支持范围，并修复了一个可能导致 Windows 命令行参数重建错误的 bug。

**「影响」** macOS、iOS 或 Linux 上的开发者现在可以直接使用预构建的二进制文件运行 llama.cpp 模型，无需编译，从而节省了设置时间并避免了之前 Windows argv 重建 bug 可能引起的命令行解析错误。

**标签**: `#llama.cpp`, `#AI tools`, `#open-source`, `#platform support`

---

<a id="item-tech-news-3"></a>
### [llama.cpp b12002 发布批量张量复制 API 和 CUDA 支持](https://github.com/ggml-org/llama.cpp/releases/tag/b12002) ⭐️ 7.0/10

llama.cpp b12002 发布后，ggml 模块新增了通用批量张量复制 API，并扩展了 CUDA 对批量张量操作的支持，同时修复了批量张量 2D 检测问题。 这些改进已应用于 llama 上下文 I/O 层，并通过缓冲区类型分组批量张量操作；同时移除了异步 tensor\_n API，新增了空缓冲区钩子，并更新了测试套件以验证多后端兼容性。 该版本为 macOS、Linux、Windows、Android 等平台提供预编译二进制包，支持 Apple Silicon、Intel、CUDA 12/13、Vulkan、ROCm、OpenVINO、SYCL 等多种硬件加速器。

github · github-actions\[bot\] · 10月30日 11:00

**「背景」** llama.cpp 是一个广泛使用的开源项目，用于在本地设备上高效运行大语言模型（LLM），其核心库 ggml 负责张量计算和硬件加速。此前版本已支持逐张量的设备内存拷贝，但缺乏批量拷贝接口，导致在多张量并行传输（如上下文输入输出）时产生额外内核启动开销。

**「提升本地 LLM 推理速度」** The new CUDA‑enabled batched tensor copy API lets developers accelerate local LLM inference on NVIDIA GPUs, delivering faster performance for GPU‑based workloads.

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ggml-org/llama.cpp/releases">Releases · ggml-org/ llama . cpp · GitHub</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#batched tensor copy`, `#CUDA support`, `#AI optimization`

---

<a id="item-tech-news-4"></a>
### [Bunny CDN Security Incident](https://status.bunny.net/incidents/p6gf1by9kr7m) ⭐️ 7.0/10

Bunny CDN experienced a security incident linked to an upstream provider \(Gcore\) compromise, with Bunny taking immediate mitigation steps including traffic rerouting and TLS certificate revocation.

hackernews · SondreDag · 10月30日 19:05 · [社区讨论](https://news.ycombinator.com/item?id=50308697)

**标签**: `#CDN security`, `#Infrastructure incident`, `#Bunny`, `#Security breach`

---

<a id="item-tech-news-5"></a>
### [Multi-Token Prediction Done Right \[R\]](https://www.reddit.com/r/MachineLearning/comments/1xjnz40/multitoken_prediction_done_right_r/) ⭐️ 7.0/10

New Soft-MTP technique improves Multi-Token Prediction by extracting hidden KL distillation signals via a simple one-line code change, with practical benefits for speculative decoding and next-token prediction.

reddit · r/MachineLearning · /u/jayden\_teoh\_ · 10月30日 18:53

**标签**: `#multi-token-prediction`, `#speculative-decoding`, `#self-distillation`, `#pre-training-optimization`, `#open-source-ml`

---

<a id="item-tech-news-6"></a>
### [Claude 重命名 Max 套餐并取消 Ultra 五小时限制](https://x.com/claudeai/status/2116220869479428500) ⭐️ 7.0/10

Claude 将 Max 20x 套餐改名为 Ultra，保持每月 200 美元的价格。从 10 月 30 日起，已通过验证的 Ultra 账户不再受 5 小时使用时限，现有订阅者无需任何操作。新账户在完成验证前仍保留临时限制，用于防范欺诈和滥用，届时会收到邮件通知，而每周用量限制保持不变。

telegram · zaihuapd · 10月30日 17:44

**「Claude Max 套餐重命名及 Ultra 五小时限制取消」** Claude 重命名 Max 套餐：Max 5x 改为 Max，Max 20x 改为 Ultra，价格保持 $100 和 $200 美元不变。2026 年 10 月 30 日起，已通过验证的 Ultra 账户将不再受限于每日 5 小时的使用上限，尽管新账户在验证期间仍保留临时限制。该变更影响了 AI 订阅用户的使用限制和定价结构。

**「用户影响」** 已验证的 Ultra 用户可以从 10 月 30 日起无限制地使用 Claude，提升了连续使用的时间窗口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claude.com/pricing">Plans &amp; pricing | Claude by Anthropic</a></li>
<li><a href="https://aiweekly.co/alerts/anthropic-sued-over-claude-max-5x-and-20x-usage-claims">Anthropic Sued Over Claude Max &#x27; 5 x &#x27; and &#x27; 20 x &#x27; Usage... | AI ...</a></li>
<li><a href="https://gigazine.net/gsc_news/en/20260414-anthropic-claude-quota-limit/">There are reports that Anthropic &#x27;s Claude quickly... - GIGAZINE</a></li>

</ul>
</details>

**标签**: `#Claude`, `#pricing`, `#usage-limits`, `#AI-access`, `#Anthropic`

---