# Constitutional Classifiers：通过可解释特征实现可扩展安全

**日期：** 2025年2月3日  
**类型：** 研究论文  
**arXiv：** 2501.18837

## 描述

Constitutional Classifiers 将稀疏自编码器特征（来自 Scaling Monosemanticity）与 Constitutional AI 原则相结合，创建了可解释、可扩展的安全分类器。183 名参与者参与的漏洞赏金计划未能找到通用越狱方法，而越狱成功率从 86% 降至 4.4%。

该方法证明机械可解释性可以直接改善生产系统中的 AI 安全。

## 技术细节

- **架构：** 分类器基于可解释的 SAE 特征而非原始模型激活
- **宪法原则：** 安全标准源自 CAI 原则——可解释的拒绝标准
- **漏洞赏金：** 183 名参与者尝试寻找越狱方法；**未发现通用越狱**
- **有效性：** 使用 Constitutional Classifiers 越狱成功率**86% → 4.4%**
- **可解释性：** 每个分类决策可追溯到特定特征和原则
- **可扩展性：** 方法随特征数量扩展（可用 3400 万+ 特征）

## 意义与影响

- **可解释性→安全：** 可解释性改善生产安全的首次重大展示
- **漏洞赏金验证：** 183 名参与者无法找到通用越狱证明了鲁棒性
- **显著改进：** 86% 到 4.4% 代表了数量级的安全提升
- **基础：** 催生了进一步改进的 Constitutional Classifiers++
- **研究整合：** 在单一系统中统一 Scaling Monosemanticity + Constitutional AI

---

# English Original

---

# Constitutional Classifiers: Scalable Safety via Interpretable Features

**Date:** February 3, 2025  
**Type:** Research Paper  
**arXiv:** 2501.18837

## Description

Constitutional Classifiers combined sparse autoencoder features (from Scaling Monosemanticity) with Constitutional AI principles to create interpretable, scalable safety classifiers. A bug bounty with 183 participants failed to find a universal jailbreak, while jailbreak success rate dropped from 86% to 4.4%.

The approach demonstrated that mechanistic interpretability could directly improve AI safety in production systems.

## Technical Details

- **Architecture:** Classifiers built on interpretable SAE features rather than raw model activations
- **Constitutional Principles:** Safety criteria derived from CAI principles—interpretable refusal criteria
- **Bug Bounty:** 183 participants attempted to find jailbreaks; **no universal jailbreak** discovered
- **Effectiveness:** **86% → 4.4%** jailbreak success rate with Constitutional Classifiers
- **Interpretability:** Each classification decision traceable to specific features and principles
- **Scalability:** Approach scales with feature count (34M+ features available)

## Significance & Impact

- **Interpretability → Safety:** First major demonstration of interpretability improving production safety
- **Bug Bounty Validation:** 183 participants unable to find universal jailbreak demonstrated robustness
- **Dramatic Improvement:** 86% to 4.4% represented order-of-magnitude safety gain
- **Foundation:** Led to Constitutional Classifiers++ with further improvements
- **Research Integration:** Unified Scaling Monosemanticity + Constitutional AI in single system
