# 宪法式 AI 与规模化自监督

## 元数据

| 字段 | 值 |
|-------|-------|
| **日期** | 2023年12月19日 |
| **平台** | Salesforce Ventures（炉边对话） |
| **演讲者** | Tom Brown（联合创始人，Anthropic） |
| **主题** | 宪法式 AI、自监督、模型堆叠、Claude 2.1 |

---

## 概述

Tom Brown 解释了宪法式 AI——Anthropic 的方法，即模型使用一套原则（「宪法」）进行自我监督。他认为自监督比 RLHF（基于人类反馈的强化学习）更具可扩展性，并讨论了针对不同任务的「堆叠」模型。他强调了 Claude 2.1 将错误率降低 2 倍的成就。

---

## 要点

### 宪法式 AI

- 模型使用书面原则集——「宪法」——进行自我监督
- 宪法定义价值观：有用、诚实、无害等
- 模型根据这些原则批判和修订自己的输出
- 减少对每个决策都需要人类标注者的依赖

### 自监督比 RLHF 更具可扩展性

- RLHF 需要大量人类反馈——难以扩展
- 宪法式 AI 使用基于原则的 AI 生成反馈
- 可以更快、更大规模地迭代
- 价值观的应用更加一致

### 针对不同任务「堆叠」模型

- 不同用例使用不同模型或模型配置
- 专业化提高性能
- 简单任务可用较小模型，复杂任务用较大模型
- 高效利用算力

### Claude 2.1 性能

- Claude 2.1 与之前版本相比将错误率降低 2 倍
- 准确性和可靠性显著提升
- 展示了宪法式 AI 和迭代优化的价值
- 企业客户看到了可衡量的收益

### 扩展与安全

- 扩展改进必须与安全投入相结合
- 宪法式 AI 作为一种可扩展的安全方法
- 持续评估与优化

---

## 重要引言

> "宪法式 AI 意味着模型进行自我监督。"

> "自监督比 RLHF 更具可扩展性。"

> "我们针对不同任务堆叠模型。"

> "Claude 2.1 将错误率降低 2 倍。"

---

## 来源说明

- **主要来源**：Salesforce Ventures 炉边对话
- **活动日期**：2023年12月19日
- **演讲者**：Tom Brown，Anthropic 联合创始人

---

# English Original

---

# Constitutional AI and Self-Supervision at Scale

## Metadata

| Field | Value |
|-------|-------|
| **Date** | December 19, 2023 |
| **Platform** | Salesforce Ventures (Fireside Chat) |
| **Speaker** | Tom Brown (Co-founder, Anthropic) |
| **Topic** | Constitutional AI, self-supervision, model stacking, Claude 2.1 |

---

## Summary

Tom Brown explains Constitutional AI—Anthropic's approach where models supervise themselves using a set of principles (the "Constitution"). He argues that self-supervision scales better than RLHF (Reinforcement Learning from Human Feedback) and discusses "stacking" models for different tasks. He highlights Claude 2.1's achievement of reducing error rates by 2x.

---

## Key Points

### Constitutional AI

- Models supervise themselves using a written set of principles—the "Constitution"
- The Constitution defines values: helpfulness, honesty, harmlessness, and more
- Models critique and revise their own outputs against these principles
- Reduces reliance on human labelers for every decision

### Self-Supervision Scales Better Than RLHF

- RLHF requires extensive human feedback—doesn't scale well
- Constitutional AI uses AI-generated feedback based on principles
- Can iterate faster and at larger scale
- More consistent application of values

### "Stacking" Models for Different Tasks

- Different models or model configurations for different use cases
- Specialization improves performance
- Can use smaller models for simple tasks, larger for complex ones
- Efficient use of compute

### Claude 2.1 Performance

- Claude 2.1 reduced error rates by 2x compared to previous versions
- Significant improvement in accuracy and reliability
- Demonstrates value of Constitutional AI and iterative refinement
- Enterprise customers saw measurable benefits

### Scaling and Safety

- Scaling improvements must be paired with safety investments
- Constitutional AI as a scalable safety approach
- Continuous evaluation and refinement

---

## Notable Quotes

> "Constitutional AI means models supervise themselves."

> "Self-supervision scales better than RLHF."

> "We stack models for different tasks."

> "Claude 2.1 reduced error rates 2x."

---

## Source Attribution

- **Primary Source**: Salesforce Ventures Fireside Chat
- **Event Date**: December 19, 2023
- **Speaker**: Tom Brown, Co-founder, Anthropic
