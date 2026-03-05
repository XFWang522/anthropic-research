# Constitutional AI：从 AI 反馈实现无害性

**日期：** 2022年12月15日  
**类型：** 研究论文  
**arXiv：** 2212.08073

## 描述

Constitutional AI（CAI）代表了 AI 对齐的范式转变，引入了一种使用 AI 生成的反馈而非人类反馈来训练无害 AI 助手的方法。该方法产生了"非回避型"AI——能够以清晰、诚实的解释拒绝有害请求的模型，而非回避或逃避。

该论文奠定了 Claude 训练方法论的基础，并解决了 RLHF 的局限性，特别是 RLHF 模型在拒绝请求时倾向于回避的问题。

## 技术细节

- **两阶段训练：**
  1. **监督式自我批判与修订：** 模型根据一套宪法原则批判自己的输出，然后进行修订。无害性标准不需要人类反馈。
  2. **RLAIF（从 AI 反馈的强化学习）：** 在 RL 阶段使用 AI 偏好（来自宪法原则）而非人类偏好

- **宪法原则：** 一套书面原则（"宪法"）指导模型行为——例如"选择最有帮助和最诚实的响应"、"选择明确拒绝有害请求的响应"

- **非回避拒绝：** 关键创新——模型被训练为给出直接、诚实的拒绝（"我无法帮助您，因为..."），而非可能使用户困惑的回避性响应

- **RLAIF vs RLHF：** 证明 AI 反馈可以达到与人类反馈相似或更好的无害性，同时实现更可扩展和一致的训练

## 意义与影响

- **Claude 的基础：** Constitutional AI 成为 Claude 的核心训练方法论，使其与竞争对手区分开来
- **可扩展性：** 减少了对昂贵的对齐人类反馈的依赖
- **透明度：** 宪法原则是可解释和可审计的——与黑盒偏好模型不同
- **用户体验：** 非回避拒绝在模型拒绝请求时提高了信任和清晰度
- **研究方向：** 催生了后续工作，包括 Constitutional Classifiers 和 Constitutional Classifiers++

---

# English Original

---

# Constitutional AI: Harmlessness from AI Feedback

**Date:** December 15, 2022  
**Type:** Research Paper  
**arXiv:** 2212.08073

## Description

Constitutional AI (CAI) represented a paradigm shift in AI alignment, introducing a method to train harmless AI assistants using AI-generated feedback rather than human feedback. The approach produced "non-evasive" AI—models that decline harmful requests with clear, honest explanations rather than deflecting or evading.

This paper established the foundation for Claude's training methodology and addressed limitations of RLHF, particularly the tendency of RLHF models to be evasive when refusing requests.

## Technical Details

- **Two-Phase Training:**
  1. **Supervised Self-Critique and Revision:** Models critique their own outputs against a set of constitutional principles, then revise. Human feedback not required for harmlessness criteria.
  2. **RLAIF (Reinforcement Learning from AI Feedback):** Use AI preferences (from the constitutional principles) instead of human preferences for the RL phase

- **Constitutional Principles:** A set of written principles (the "constitution") that guide model behavior—e.g., "Choose the response that is most helpful and honest," "Choose the response that refuses harmful requests clearly"

- **Non-Evasive Refusals:** Key innovation—models trained to give direct, honest refusals ("I can't help with that because...") rather than evasive responses that might confuse users

- **RLAIF vs RLHF:** Demonstrated that AI feedback could achieve similar or better harmlessness than human feedback while enabling more scalable and consistent training

## Significance & Impact

- **Claude's Foundation:** Constitutional AI became the core training methodology for Claude, distinguishing it from competitors
- **Scalability:** Reduced reliance on expensive human feedback for alignment
- **Transparency:** Constitutional principles are interpretable and auditable—unlike black-box preference models
- **User Experience:** Non-evasive refusals improve trust and clarity when models decline requests
- **Research Direction:** Spawned follow-on work including Constitutional Classifiers and Constitutional Classifiers++
