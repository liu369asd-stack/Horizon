---
layout: default
title: "Horizon Summary: 2026-10-26 (ZH)"
date: 2026-10-26
lang: zh
---

> 从 58 条内容中筛选出 5 条重要资讯。

---

**科技新闻**
1. [memt-1.0 architecture breakdown gated deltanet-2, mixture-of-storage, and 66x smaller storage footprint for agent memory \[D\]](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenAI and Anthropic cut their LLM prices by up to 80% within a few months. Why?](#item-tech-news-2) ⭐️ 7.5/10
3. [llama.cpp b11870 发布 DeepSeek-V4.1-Flash 支持](#item-tech-news-3) ⭐️ 7.0/10
4. [Cerebras Deploys Trillion-Parameter AI Models](#item-tech-news-4) ⭐️ 7.0/10
5. [Brotli 高危漏洞影响 Python 与 Node.js HTTP 组件](#item-tech-news-5) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [memt-1.0 architecture breakdown gated deltanet-2, mixture-of-storage, and 66x smaller storage footprint for agent memory \[D\]](https://www.reddit.com/r/MachineLearning/comments/1xeu0ht/memt10_architecture_breakdown_gated_deltanet2/) ⭐️ 8.0/10

The Reddit post details memt-1.0&\#x27;s gated deltanet-2 and mixture-of-storage design, achieving 1.86x speedup and 66x storage reduction in context handling.

reddit · r/MachineLearning · /u/Mrs-Grumpy23 · 10月25日 05:31

**标签**: `#AI architecture`, `#Memory efficiency`, `#Open-source`, `#Model performance`

---

<a id="item-tech-news-2"></a>
### [OpenAI and Anthropic cut their LLM prices by up to 80% within a few months. Why?](https://minimaxir.com/2026/10/cheap-llms/) ⭐️ 7.5/10

OpenAI and Anthropic have reduced LLM prices by up to 80% within a few months, raising questions about their business models and affecting accessibility for students.

hackernews · minimaxir · 10月25日 21:11 · [社区讨论](https://news.ycombinator.com/item?id=50236102)

**标签**: `#AI pricing`, `#OpenAI`, `#Anthropic`, `#LLM cost reduction`, `#student AI tools`

---

<a id="item-tech-news-3"></a>
### [llama.cpp b11870 发布 DeepSeek-V4.1-Flash 支持](https://github.com/ggml-org/llama.cpp/releases/tag/b11870) ⭐️ 7.0/10

llama.cpp 发布版本 b11870（2026 年 10 月 25 日），新增对 DeepSeek-V4.1-Flash（deepseek41）模型的本地推理支持。该版本同时引入压缩 KV cache、图内 Engram 行收集等性能优化，并移除 MXFP8、将 Engram 表转为 BF16，以及移除 DSV41\_KV\_MIRROR 开关。发布包覆盖 macOS Apple Silicon/Intel、iOS XCFramework、Linux（CPU/Vulkan/CUDA 12.8/CUDA 13.4/ROCm 10.0/OpenVINO/SYCL）、Android arm64、Windows（CPU/CUDA/Vulkan/OpenVINO/SYCL/ROCm）及 openEuler 等平台。

github · github-actions\[bot\] · 10月25日 02:15

**「背景」** DeepSeek-V4.1-Flash 是 DeepSeek 公司发布的最新开放权重大语言模型，采用多模态训练语料共 45 万亿 token，稀疏注意力在 64K 序列长度下训练，上下文窗口扩展至 100 万 token。该模型于 2026 年 10 月在 DeepSeek API 上线，宣称架构更高效、API 价格更低。llama.cpp 此前已支持多个 DeepSeek 模型系列，此次 b11870 版本首次加入对 V4.1-Flash 的原生支持及针对性能优化。

**「影响：本地开发者可在一台消费级 Apple Silicon 上运行 DeepSeek-V4.1-Flash」** 对于希望在本地运行 DeepSeek-V4.1-Flash 的开发者与研究者，b11870 提供可直接使用的 llama.cpp 二进制，无需自行适配模型格式或编译后端；此前该模型在 llama.cpp 中尚不支持，这一版本补齐了关键支持路径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.deepseek.com/en/news/deepseek-v4-1-flash/">Introducing DeepSeek - V 4 . 1 - Flash : smarter, faster, more efficient.</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash">deepseek-ai/ DeepSeek - V 4 . 1 - Flash · Hugging Face</a></li>

</ul>
</details>

**标签**: `#AI tools`, `#local inference`, `#DeepSeek`, `#llama.cpp`, `#open-source`

---

<a id="item-tech-news-4"></a>
### [Cerebras Deploys Trillion-Parameter AI Models](https://www.cerebras.ai/blog/how-we-deploy-trillion-parameter-frontier-models-on-cerebras) ⭐️ 7.0/10

Cerebras reveals how it runs trillion‑parameter frontier models on its hardware, prompting discussion on model age, speed, cost, and real‑world usability.

hackernews · gmays · 10月25日 01:33 · [社区讨论](https://news.ycombinator.com/item?id=50227356)

**标签**: `#AI hardware`, `#Large model serving`, `#Model freshness`, `#Community discussion`

---

<a id="item-tech-news-5"></a>
### [Brotli 高危漏洞影响 Python 与 Node.js HTTP 组件](https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) ⭐️ 7.0/10

Google Brotli 解码器 CVE-2026-111497 影响 1.0.3 至 1.2.0 版本，CVSS 4.0 评分 9.2，远程未认证攻击者可发送特制压缩流导致内存损坏、敏感数据泄露、进程崩溃或任意代码执行。受影响的 Python HTTP 组件需升级至 Brotli 1.2.1 及 brotlicffi 1.2.1.0，Node.js 则需升级至 22.23.4、24.22.1 或 26.12.1。该漏洞于 2 月由 OpenAI 发现并披露。

telegram · zaihuapd · 10月25日 02:42

**「Brotli 解码器漏洞背景」** Brotli 是 Google 开发的一种无损数据压缩算法，广泛应用于 HTTP 压缩中，用于减小网页传输数据的体积。该算法的解码器实现存在安全风险可能影响依赖其进行内容解压的 Web 服务器和客户端组件。

**「影响与升级建议」** 攻击者可利用 specially crafted Brotli 压缩流在 Python 和 Node.js HTTP 组件中造成内存破坏、数据泄露或远程代码执行，因此用户必须将 Python Brotli 升级至 1.2.1 并 brotlicffi 至 1.2.1.0，或将 Node.js 升级至 22.23.4、24.22.1 或 26.12.1。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://access.redhat.com/security/cve/cve-2026-111497">CVE-2026-111497 - Red Hat Customer Portal</a></li>
<li><a href="https://cvetodo.com/cve/CVE-2026-111497">CVE-2026-111497: Google Brotli Unchecked Return Value</a></li>
<li><a href="https://nvd.nist.gov/vuln/detail/cve-2026-111497">NVD-CVE-2026-111497</a></li>

</ul>
</details>

**标签**: `#brotli`, `#cve-2026-111497`, `#security`, `#python`, `#nodejs`

---