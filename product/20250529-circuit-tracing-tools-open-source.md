# 电路追踪工具开源发布

**日期：** 2025年5月29日  
**类型：** 开源发布

## 描述

Anthropic 开源了 circuit-tracer Python 库和 Neuronpedia 前端，使机械可解释性工具向更广泛的研究社区开放。这些工具使研究人员能够追踪语言模型中的激活模式、探索 Scaling Monosemanticity 的特征，并进行电路级分析。

## 技术细节

- **Circuit-Tracer：** 用于追踪和分析语言模型电路的 Python 库
  - 激活追踪
  - 特征归因
  - 电路发现
  - 与稀疏自编码器特征集成

- **Neuronpedia：** 用于探索模型特征的基于 Web 的前端
  - 浏览 Claude 3 Sonnet 的 3400 万+ 特征
  - 搜索和过滤特征
  - 可视化特征激活
  - 社区标注和分析

- **集成：** 与 Scaling Monosemanticity 特征、Constitutional Classifiers 配合使用
- **许可：** 研究用途开源

## 意义与影响

- **研究民主化：** 使 Anthropic 以外的可解释性研究成为可能
- **透明度：** 展示了在 AI 安全中开放科学的承诺
- **生态：** Neuronpedia 成为特征探索和分享的中心
- **教育：** 工具帮助培养下一代可解释性研究人员
- **安全：** 社区可以审计和分析模型特征

---

# English Original

---

# Circuit Tracing Tools Open Source Release

**Date:** May 29, 2025  
**Type:** Open Source Release

## Description

Anthropic open-sourced the circuit-tracer Python library and Neuronpedia frontend, making mechanistic interpretability tools available to the broader research community. These tools enabled researchers to trace activation patterns through language models, explore features from Scaling Monosemanticity, and conduct circuit-level analysis.

## Technical Details

- **Circuit-Tracer:** Python library for tracing and analyzing circuits in language models
  - Activation tracing
  - Feature attribution
  - Circuit discovery
  - Integration with sparse autoencoder features

- **Neuronpedia:** Web-based frontend for exploring model features
  - Browse 34M+ features from Claude 3 Sonnet
  - Search and filter features
  - Visualize feature activations
  - Community annotations and analysis

- **Integration:** Works with Scaling Monosemanticity features, Constitutional Classifiers
- **License:** Open source for research use

## Significance & Impact

- **Research Democratization:** Enabled interpretability research beyond Anthropic
- **Transparency:** Demonstrated commitment to open science in AI safety
- **Ecosystem:** Neuronpedia became hub for feature exploration and sharing
- **Education:** Tools helped train next generation of interpretability researchers
- **Safety:** Community could audit and analyze model features
