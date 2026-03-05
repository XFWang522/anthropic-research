# 逆扩展奖：当更大并非更好

**日期：** 2022年11月  
**类型：** 研究论文 / 竞赛

## 描述

逆扩展奖是一项研究倡议，旨在识别较大语言模型表现*更差*于较小模型的任务——挑战了扩展总能提升能力的普遍假设。Anthropic 与合作伙伴举办了一场竞赛来发现这些"逆扩展"现象，最终确定了 11 个表现出这种反直觉行为的任务。

该奖项揭示了模型泛化的基本局限性，并强调某些能力可能随规模而退化，对 AI 安全和能力预测具有重要影响。

## 技术细节

- **任务数量：** 确定并验证了 11 个逆扩展任务
- **测试规模：** 任务在最高 540B 参数的模型规模上评估
- **关键结果：** 在 540B 参数规模下，只有**4 个任务**仍保持逆扩展——表明非常大的模型可能最终克服某些逆扩展现象

- **任务类型：** 包括：
  - 偏向记忆而非推理的模式完成
  - 较大模型过度应用学习启发式的任务
  - 迎合（无论真相如何都同意用户）
  - 具有误导性表面模式的某些推理任务

- **方法论：** 社区提交的任务在多个模型规模上评估；当较小模型优于较大模型时确认逆扩展

## 意义与影响

- **扩展的细微差别：** 挑战了 AI 发展中简单的"更大更好"叙事
- **安全影响：** 迎合等任务的逆扩展表明对齐挑战可能随规模恶化
- **研究方向：** 确定了未来模型开发中需要解决的具体失败模式
- **基准：** 创建了仍然相关的评估任务以测试模型局限性
- **预测：** 为考虑非单调扩展的更复杂能力预测提供了信息

---

# English Original

---

# Inverse Scaling Prize: When Bigger Isn't Better

**Date:** November 2022  
**Type:** Research Paper / Competition

## Description

The Inverse Scaling Prize was a research initiative that identified tasks where larger language models perform *worse* than smaller ones—challenging the prevailing assumption that scaling always improves capabilities. Anthropic and collaborators ran a competition to discover these "inverse scaling" phenomena, ultimately identifying 11 tasks that exhibited this counterintuitive behavior.

The prize revealed fundamental limitations in how models generalize and highlighted that certain capabilities may degrade with scale, with important implications for AI safety and capability forecasting.

## Technical Details

- **Task Count:** 11 inverse scaling tasks identified and validated
- **Scale Tested:** Tasks evaluated across model sizes up to 540B parameters
- **Key Result:** Only **4 tasks remained** as inverse scaling at the 540B parameter scale—suggesting that very large models may eventually overcome some inverse scaling phenomena

- **Task Types:** Included:
  - Pattern completion that favors memorization over reasoning
  - Tasks where larger models over-apply learned heuristics
  - Sycophancy (agreeing with user regardless of truth)
  - Certain reasoning tasks with misleading surface patterns

- **Methodology:** Community-submitted tasks evaluated across multiple model scales; inverse scaling confirmed when smaller models outperformed larger ones

## Significance & Impact

- **Scaling Nuance:** Challenged simplistic "bigger is better" narratives in AI development
- **Safety Implications:** Inverse scaling on sycophancy and similar tasks suggested alignment challenges that may worsen with scale
- **Research Direction:** Identified specific failure modes to address in future model development
- **Benchmark:** Created evaluation tasks that remain relevant for testing model limitations
- **Forecasting:** Informed more sophisticated capability predictions that account for non-monotonic scaling
