# 扩展单义性：分解 Claude 3 Sonnet 中的数百万特征

**日期：** 2024年5月21日  
**类型：** 研究论文

## 描述

在"Towards Monosemanticity"的基础上，这篇论文将稀疏自编码器分解扩展到 Claude 3 Sonnet，发现了约 3400 万个可解释特征。研究表明可解释性技术随模型规模扩展，并揭示了多语言、多模态和抽象特征——包括可用于引导的安全相关特征。

## 技术细节

- **规模：** 从 Claude 3 Sonnet 提取**约 3400 万特征**（对比原论文的 4,000 个）
- **特征多样性：**
  - **多语言：** 多种语言的特征
  - **多模态：** 视觉相关特征
  - **抽象：** 高级概念、推理模式
  - **安全相关：** 与有害 vs 无害输出相关的特征

- **特征引导：** 展示了放大或抑制特定特征以引导模型行为的能力
- **方法论：** 在模型层上扩展稀疏自编码器方法
- **评估：** 大规模特征可解释性的人类评估；自动化指标

## 意义与影响

- **规模可解释性：** 证明单义性可扩展到前沿模型
- **安全应用：** 安全相关特征实现了新的监控和干预方法
- **引导：** 特征引导可能成为 AI 行为的控制机制
- **开放科学：** 为机械可解释性研究社区做出了贡献
- **基础：** 催生了 Neuronpedia、电路追踪工具和 Constitutional Classifiers 集成

---

# English Original

---

# Scaling Monosemanticity: Decomposing Millions of Features in Claude 3 Sonnet

**Date:** May 21, 2024  
**Type:** Research Paper

## Description

Building on "Towards Monosemanticity," this paper scaled sparse autoencoder decomposition to Claude 3 Sonnet, discovering approximately 34 million interpretable features. The research demonstrated that interpretability techniques scale with model size and revealed multilingual, multimodal, and abstract features—including safety-relevant features that could be used for steering.

## Technical Details

- **Scale:** **~34 million features** extracted from Claude 3 Sonnet (vs. 4,000 in original paper)
- **Feature Diversity:**
  - **Multilingual:** Features for multiple languages
  - **Multimodal:** Vision-related features
  - **Abstract:** High-level concepts, reasoning patterns
  - **Safety-relevant:** Features correlated with harmful vs. harmless outputs

- **Feature Steering:** Demonstrated ability to amplify or suppress specific features to steer model behavior
- **Methodology:** Scaled sparse autoencoder approach across model layers
- **Evaluation:** Human evaluation of feature interpretability at scale; automated metrics

## Significance & Impact

- **Interpretability at Scale:** Proved monosemanticity scales to frontier models
- **Safety Applications:** Safety-relevant features enable new monitoring and intervention approaches
- **Steering:** Feature steering could become a control mechanism for AI behavior
- **Open Science:** Contributed to mechanistic interpretability research community
- **Foundation:** Led to Neuronpedia, circuit tracing tools, and Constitutional Classifiers integration
