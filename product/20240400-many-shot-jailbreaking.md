# 多样本越狱

**日期：** 2024年4月  
**类型：** 研究论文  
**会议：** NeurIPS 2024

## 描述

这篇论文识别了一种新的攻击向量："多样本越狱"，攻击者利用长上下文窗口注入大量 few-shot 示例，逐渐将模型引导向有害行为。该攻击展示了幂律扩展——有效性随上下文示例数量增加——并影响了多个前沿模型。

该研究突出了长上下文能力与安全之间的根本张力，需要新的防御方法。

## 技术细节

- **攻击机制：** 在提示中注入大量（数十到数百个）few-shot 示例，展示期望的有害行为；模型从上下文示例中学习模式
- **幂律扩展：** 攻击成功率随示例数量扩展——更多示例 = 更高成功率
- **受影响模型：** 多个前沿语言模型易受该攻击
- **上下文依赖：** 利用了作为卖点的超长上下文窗口（100K-200K）
- **防御挑战：** 传统过滤不足；需要架构或训练变更

## 意义与影响

- **安全意识：** 将长上下文攻击带到 AI 安全研究前沿
- **NeurIPS 2024：** 在顶级会议上的同行评审发表
- **模型加固：** 为后续 Claude 版本的防御措施提供了信息
- **权衡可见性：** 突出了能力（长上下文）可能创造漏洞
- **行业影响：** 推动了多个实验室的长上下文安全改进

---

# English Original

---

# Many-Shot Jailbreaking

**Date:** April 2024  
**Type:** Research Paper  
**Venue:** NeurIPS 2024

## Description

This paper identified a novel attack vector: "many-shot jailbreaking," where attackers exploit long context windows to include numerous few-shot examples that gradually steer the model toward harmful behavior. The attack demonstrated power law scaling—effectiveness increased with the number of in-context examples—and affected multiple frontier models.

The research highlighted a fundamental tension between long-context capabilities and safety, requiring new defensive approaches.

## Technical Details

- **Attack Mechanism:** Inject many (dozens to hundreds) few-shot examples in the prompt that demonstrate desired harmful behavior; model learns the pattern from in-context examples
- **Power Law Scaling:** Attack success rate scales with number of examples—more examples = higher success
- **Affected Models:** Multiple frontier language models vulnerable to the attack
- **Context Dependency:** Exploits the very long context windows (100K-200K) that are a selling point
- **Defense Challenges:** Traditional filtering insufficient; requires architectural or training changes

## Significance & Impact

- **Security Awareness:** Brought long-context attacks to forefront of AI safety research
- **NeurIPS 2024:** Peer-reviewed publication in top venue
- **Model Hardening:** Informed defensive measures in subsequent Claude releases
- **Trade-off Visibility:** Highlighted that capability (long context) can create vulnerability
- **Industry Impact:** Led to improved long-context safety across multiple labs
