# Maths, CS & AI Compendium（中文版）

<img src="images/logo.png" alt="Logo" style="border-radius: 30px; width: 100%;">

**在线阅读**: [dengxuhui.github.io/maths-cs-ai-compendium_CN](https://dengxuhui.github.io/maths-cs-ai-compendium_CN/)

## 项目简介
很多教材会把关键思想埋在密集符号里，弱化直觉解释，默认你已经掌握一半背景知识；而在 AI 这样变化极快的领域，内容也很容易过时。本项目是一本开放、非传统、强调直觉优先的教材，从零开始系统覆盖数学、计算机科学与人工智能，面向希望真正理解原理、而不仅是应付考试或面试的学习者。

## 背景
这是上游项目 `HenryNdubuaku/maths-cs-ai-compendium` 的中文 fork。该仓库的核心目标是持续提供高质量中文内容，帮助中文读者更系统地建立数学、计算机与 AI 的知识图谱。

## MCP Server
本仓库内置 MCP 服务器，可让 AI 助手（如 Claude Code、Cursor、VS Code 等）把本教材作为知识库进行调用。使用时需要本地克隆仓库，工具涵盖目录浏览、章节读取、关键词搜索、内容推荐与示例提取等教育场景。

## 内容大纲

| # | 章节 | 内容摘要 | 状态 |
|---|---|---|---|
| 01 | [向量（Vectors）](chapter%2001%3A%20vectors/01.%20vector%20spaces.md) | 空间、模长、方向、范数与度量、点积/叉积/外积、基与对偶 | Available |
| 02 | [矩阵（Matrices）](chapter%2002%3A%20matrices/01.%20matrix%20properties.md) | 矩阵性质、特殊矩阵、运算、线性变换、分解（LU/QR/SVD） | Available |
| 03 | [微积分（Calculus）](chapter%2003%3A%20calculus/01.%20differential%20calculus.md) | 导数、积分、多元微积分、泰勒近似、优化与梯度下降 | Available |
| 04 | [统计学（Statistics）](chapter%2004%3A%20statistics/01.%20fundamentals.md) | 描述统计、抽样、中心极限定理、假设检验、置信区间 | Available |
| 05 | [概率论（Probability）](chapter%2005%3A%20probability/01.%20counting.md) | 计数、条件概率、分布、贝叶斯方法、信息论 | Available |
| 06 | [机器学习（Machine Learning）](chapter%2006%3A%20machine%20learning/01.%20classical%20machine%20learning.md) | 经典机器学习、梯度方法、深度学习、强化学习、分布式训练 | Available |
| 07 | [计算语言学（Computational Linguistics）](chapter%2007%3A%20computational%20linguistics/01.%20linguistic%20foundations.md) | 语法语义语用、NLP、语言模型、RNN/CNN/注意力/Transformer、现代 LLM 架构与评测 | Available |
| 08 | [计算机视觉（Computer Vision）](chapter%2008%3A%20computer%20vision/01.%20image%20fundamentals.md) | 图像处理、检测与分割、视频处理、SLAM、CNN、视觉 Transformer、扩散与流匹配 | Available |
| 09 | [语音与音频（Audio & Speech）](chapter%2009%3A%20audio%20and%20speech/01.%20digital%20signal%20processing.md) | DSP、ASR、TTS、语音活动检测、说话人分离、降噪、WaveNet、Conformer | Available |
| 10 | [多模态学习（Multimodal Learning）](chapter%2010%3A%20multimodal%20learning/01.%20multimodal%20representations.md) | 融合策略、对比学习、CLIP、VLM、图像/视频 token 化、跨模态生成、统一架构 | Available |
| 11 | [自主系统（Autonomous Systems）](chapter%2011%3A%20autonomous%20systems/01.%20perception.md) | 感知、机器人学习、VLA、自动驾驶、航天机器人 | Available |
| 12 | [图神经网络（Graph Neural Networks）](chapter%2012%3A%20graph%20neural%20networks/01.%20geometric%20deep%20learning.md) | 几何深度学习、图论、GNN、图注意力、Graph Transformer、3D 等变网络 | Available |
| 13 | [计算与操作系统（Computing & OS）](chapter%2013%3A%20computing%20and%20OS/01.%20discrete%20maths.md) | 离散数学、计算机体系结构、操作系统、并发并行、编程语言 | Available |
| 14 | [数据结构与算法（Data Structures & Algorithms）](chapter%2014%3A%20data%20structures%20and%20algorithms/00.%20foundations.md) | Big O、递归、回溯、动态规划、数组、哈希、链表、栈、树、图、排序、二分 | Available |
| 15 | [生产级软件工程（Production Software Engineering）](chapter%2015%3A%20production%20software%20engineering/01.%20linux%20and%20CMD.md) | Linux、Git、代码库设计、测试、CI/CD、Docker、模型服务、MLOps、监控 | Available |
| 16 | [SIMD 与 GPU 编程（SIMD & GPU Programming）](chapter%2016%3A%20SIMD%20and%20GPU%20programming/00.%20why%20C%2B%2B%20and%20how%20ML%20frameworks%20work.md) | 面向 ML 的 C++、框架原理、硬件基础、ARM NEON、x86 AVX、CUDA、Triton、TPU 等 | Available |
| 17 | [AI 推理（AI Inference）](chapter%2017%3A%20AI%20inference/01.%20quantisation.md) | 量化、高效架构、服务化与批处理、边缘推理、投机解码、成本优化 | Available |
| 18 | [ML 系统设计（ML Systems Design）](chapter%2018%3A%20ML%20systems%20design/01.%20systems%20design%20fundamentals.md) | 系统基础、云计算、分布式系统、ML 生命周期、A/B 测试、推荐/搜索/广告案例 | Available |
| 19 | Applied AI | 金融、医疗、蛋白质设计、药物发现等应用方向 | Coming |
| 20 | Bleeding Edge AI | 量子 ML、类脑计算、去中心化 AI、太空数据中心、脑机接口 | Coming |

## 前言

人的学习过程与神经网络训练有许多相似之处：持续输入、反复反馈、长期迭代。天赋会影响起点与学习速度，但高质量知识输入与足够的训练强度，通常才是决定上限的关键。

这本教材的目标，是把数学、计算机和 AI 的知识链路打通，帮助不同基础的学习者建立更完整、更可迁移的理解框架。你只需要具备初等数学和基础 Python 编程能力，其余内容可以在阅读与实践中逐步掌握。

## 如何更高效学习

我推荐两阶段学习法：

**阶段 1：课后累计式阅读**  
每次上课后复读当日内容，并在下一次学习时从开头快速回顾到当前进度；对薄弱点补充检索和笔记，让知识网络不断加密。

**阶段 2：考前影子阅读（主动回忆）**  
先看标题再合上资料，用自己的话复述概念与推导；只重读遗漏部分，并尽量用代码或练习题实现关键思想，形成可调用的“肌肉记忆”。

## 关于原作者

本项目原作者为 Henry Ndubuaku，中文版在保留核心知识体系的基础上进行中文化维护与持续更新。

## 引用
```bibtex
@book{ndubuaku2025compendium,
  title     = {Maths, CS & AI Compendium},
  author    = {Henry Ndubuaku},
  year      = {2026},
  publisher = {GitHub},
  url       = {https://dengxuhui.github.io/maths-cs-ai-compendium_CN/}
}
```
