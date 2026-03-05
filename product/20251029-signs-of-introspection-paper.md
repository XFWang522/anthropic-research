# 语言模型中的内省迹象

**日期：** 2025年10月29日  
**类型：** 研究论文

## 描述

这篇论文研究了语言模型是否表现出"内省"——准确报告自身内部状态、信念或推理的能力。使用概念注入实验，研究发现 Claude Opus 4 和 4.1 在测试模型中表现出最强的内省迹象。

然而，该论文得出结论认为这种内省"高度不可靠且有限"，为解释模型自我报告提供了重要警示。

## 技术细节

- **概念注入：** 将特定概念/知识注入模型上下文并测试模型是否能报告其"信念"的方法
- **测试模型：** Claude Opus 4 和 4.1 表现出最强效果；与其他模型比较
- **发现：** Opus 4/4.1 展示了报告内部状态的某些能力
- **警示：** **"高度不可靠且有限"**——内省不能信任用于高风险应用
- **影响：** 模型自我报告（例如"我不确定"）可能无法准确反映内部状态

## 意义与影响

- **可解释性：** 促进了对模型自我意识/自我报告的理解
- **信任校准：** 警告不要过度依赖模型不确定性陈述
- **研究诚信：** Anthropic 发布自身模型的局限性
- **对齐：** 与理解模型是否能准确报告错位相关
- **方法论：** 概念注入加入探测模型内部的工具包

---

# English Original

---

# Signs of Introspection in Language Models

**Date:** October 29, 2025  
**Type:** Research Paper

## Description

This paper investigated whether language models exhibit "introspection"—the ability to accurately report on their own internal states, beliefs, or reasoning. Using concept injection experiments, the research found that Claude Opus 4 and 4.1 showed the strongest signs of introspection among tested models.

However, the paper concluded that such introspection was "highly unreliable and limited," providing important caveats about interpreting model self-reports.

## Technical Details

- **Concept Injection:** Method to inject specific concepts/knowledge into model context and test if model can report on its "beliefs"
- **Models Tested:** Claude Opus 4 and 4.1 showed strongest effects; other models compared
- **Finding:** Opus 4/4.1 demonstrated some ability to report on internal states
- **Caveat:** **"Highly unreliable and limited"**—introspection could not be trusted for high-stakes applications
- **Implications:** Model self-reports (e.g., "I'm uncertain") may not accurately reflect internal state

## Significance & Impact

- **Interpretability:** Contributed to understanding model self-awareness/self-reporting
- **Trust Calibration:** Warned against over-relying on model uncertainty statements
- **Research Honesty:** Anthropic publishing limitations of own models
- **Alignment:** Relevant for understanding whether models can accurately report misalignment
- **Methodology:** Concept injection added to toolkit for probing model internals
