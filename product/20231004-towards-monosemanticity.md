# 迈向单义性：使用稀疏自编码器分解语言模型

**日期：** 2023年10月4日  
**类型：** 研究论文

## 描述

这篇论文开创性地使用稀疏自编码器将神经网络激活分解为可解释的"特征"——朝着理解语言模型中单个神经元或特征方向代表什么迈进。研究表明，512 个神经元的层可以被分解为 4000+ 个跨越不同概念的可解释特征。

单义性（一个特征 = 一个概念）代表了机械可解释性和理解模型内部的重要一步。

## 技术细节

- **方法：** 训练稀疏自编码器将模型激活重建为"字典"特征的稀疏线性组合
- **规模：** 512 神经元层 → 发现**4000+ 可解释特征**
- **识别的特征类型：**
  - **DNA 序列：** 特定遗传模式
  - **法律语言：** 合同条款、法律术语
  - **编程：** 代码模式、语法
  - **实体：** 人物、地点、概念
  - **抽象概念：** 各种语义类别

- **架构：** 自编码器学习过完备基，其中每个特征在狭窄、可解释的输入集上激活
- **评估：** 人类对特征可解释性的评估；稀疏性和重建质量的自动化指标

## 意义与影响

- **可解释性：** 开辟了理解模型"知道"什么以及知识如何表示的道路
- **安全：** 能够检测可被监控或消融的有害或欺骗性特征
- **扩展：** 为"Scaling Monosemanticity"（2024）奠定了基础，后者扩展到 3400 万特征
- **研究方向：** 影响了机械可解释性社区；催生了 Neuronpedia 和电路追踪工具
- **特征引导：** 后来通过放大/抑制特定特征实现引导模型行为

---

# English Original

---

# Towards Monosemanticity: Decomposing Language Models with Sparse Autoencoders

**Date:** October 4, 2023  
**Type:** Research Paper

## Description

This paper pioneered the use of sparse autoencoders to decompose neural network activations into interpretable "features"—moving toward understanding what individual neurons or feature directions represent in language models. The research demonstrated that a 512-neuron layer could be decomposed into 4000+ interpretable features spanning diverse concepts.

Monosemanticity (one feature = one concept) represented a major step toward mechanistic interpretability and understanding model internals.

## Technical Details

- **Method:** Sparse autoencoders trained to reconstruct model activations as sparse linear combinations of "dictionary" features
- **Scale:** 512-neuron layer → **4000+ interpretable features** discovered
- **Feature Types Identified:**
  - **DNA sequences:** Specific genetic patterns
  - **Legal language:** Contract clauses, legal terminology
  - **Programming:** Code patterns, syntax
  - **Entities:** People, places, concepts
  - **Abstract concepts:** Various semantic categories

- **Architecture:** Autoencoder learns an overcomplete basis where each feature activates on a narrow, interpretable set of inputs
- **Evaluation:** Human evaluation of feature interpretability; automated metrics for sparsity and reconstruction quality

## Significance & Impact

- **Interpretability:** Opened path to understanding what models "know" and how knowledge is represented
- **Safety:** Enables detection of harmful or deceptive features that could be monitored or ablated
- **Scaling:** Foundation for "Scaling Monosemanticity" (2024) which extended to 34M features
- **Research Direction:** Influenced mechanistic interpretability community; led to Neuronpedia and circuit tracing tools
- **Feature Steering:** Later enabled steering model behavior by amplifying/suppressing specific features
