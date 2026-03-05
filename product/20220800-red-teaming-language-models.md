# 红队测试语言模型

**日期：** 2022年8月  
**类型：** 研究论文  
**arXiv：** 2209.07858

## 描述

这项全面研究通过大规模红队测试检验了语言模型对对抗攻击的脆弱性。Anthropic 在多个模型变体上进行了 38,961 次红队攻击，以了解不同训练方法——尤其是 RLHF——如何影响模型对有害提示注入和越狱尝试的鲁棒性。

研究表明，经过 RLHF 训练的模型与基础模型相比表现出显著不同的攻击面特征，规模在抵抗红队攻击方面起着关键作用。

## 技术细节

- **规模：** 研究中进行了 38,961 次独特的红队攻击
- **攻击类别：** 多样化的攻击向量，包括：
  - 直接有害请求提示
  - 间接/越狱式提示
  - 角色扮演场景
  - 上下文操纵
  - 对抗性前缀/后缀注入

- **关键发现：** RLHF 模型**在规模上更难被红队攻破**——随着模型规模增大，RLHF 训练的模型在抵抗引发有害输出方面比基础模型表现出更强的抵抗力

- **方法论：** 人类红队成员系统性地尝试引发有害行为，攻击被分类并分析成功率

- **模型变体：** 在多个规模上比较了基础预训练模型与 RLHF 微调版本

## 意义与影响

- **安全评估：** 确立了红队测试作为 AI 安全的关键评估方法
- **RLHF 验证：** 提供了 RLHF 在规模上提高对抗攻击鲁棒性的实证证据
- **基准：** 为研究社区创建了大规模红队攻击数据集
- **扩展定律：** 促进了对对齐如何随模型规模扩展的理解——更大的对齐模型可能更安全
- **先例：** 影响了后续的红队工作，包括 Anthropic 的漏洞赏金计划和 Constitutional Classifiers 研究

---

# English Original

---

# Red Teaming Language Models

**Date:** August 2022  
**Type:** Research Paper  
**arXiv:** 2209.07858

## Description

This comprehensive study examined the vulnerability of language models to adversarial attacks through large-scale red teaming. Anthropic conducted 38,961 red team attacks across multiple model variants to understand how different training approaches—particularly RLHF—affected model robustness against harmful prompt injection and jailbreaking attempts.

The research revealed that RLHF-trained models exhibited significantly different attack surface characteristics compared to base models, with scale playing a critical role in resistance to red team attacks.

## Technical Details

- **Scale:** 38,961 unique red team attacks conducted across the study
- **Attack Categories:** Diverse attack vectors including:
  - Direct harmful request prompts
  - Indirect/jailbreak-style prompts
  - Role-playing scenarios
  - Context manipulation
  - Adversarial prefix/suffix injection

- **Key Finding:** RLHF models were **harder to red team at scale**—as model size increased, RLHF-trained models showed greater resistance to eliciting harmful outputs compared to base models

- **Methodology:** Human red teamers systematically attempted to elicit harmful behaviors, with attacks categorized and analyzed for success rates

- **Model Variants:** Compared base pre-trained models against RLHF-fine-tuned versions across multiple scales

## Significance & Impact

- **Safety Evaluation:** Established red teaming as a critical evaluation methodology for AI safety
- **RLHF Validation:** Provided empirical evidence that RLHF improves robustness against adversarial attacks at scale
- **Benchmark:** Created a large-scale dataset of red team attacks for the research community
- **Scaling Laws:** Contributed to understanding how alignment scales with model size—larger aligned models may be safer
- **Precedent:** Influenced subsequent red teaming efforts including Anthropic's bug bounty programs and Constitutional Classifiers research
