# 新 Claude 模型触发 Anthropic 更严格保障——Jared Kaplan TIME 专访全文

## 元数据

| 字段 | 值 |
|-------|-------|
| **日期** | 2025年5月 |
| **平台** | TIME |
| **演讲者** | Jared Kaplan（联合创始人、首席科学官、负责任扩展负责人，Anthropic） |
| **主题** | Claude Opus 4、ASL-3、生物武器风险、负责任扩展政策 |

---

## 概述

Jared Kaplan 在 TIME 独家专访中解释 Anthropic 为何将 Claude Opus 4 以 AI 安全等级 3（ASL-3）发布——这是该公司首次对模型施加比以往更严格的安全措施。内部测试显示 Claude Opus 4 在指导新手合成生物武器方面比先前模型更有效，可能使类似 COVID 或更危险流感变体的病原体开发成为可能。Kaplan 概述了 ASL-3 的「纵深防御」策略，包括宪法分类器、越狱防护、网络安全加固和「提升」试验。

---

## 要点摘要（中文）

- **ASL-3 触发**：内部测试显示 Claude Opus 4 在生物武器建议上表现优于先前模型；Kaplan 决定在「无法排除风险」时偏向谨慎。
- **风险表述**：「我们并非声称我们确定知道此模型有风险……但我们至少认为它足够接近，以至于我们无法排除。」
- **ASL-3 措施**：宪法分类器（检测危险提示与回答）、越狱防护（监控并「下架」持续越狱用户）、网络安全加固、提升试验（量化 AI 对新手生物武器能力的提升）。
- **RSP 考验**：RSP 为自愿政策，无外部惩罚；Anthropic 主张其创造「竞相提高」；若 Anthropic 能在不承受经济打击的情况下自我约束，可能对行业产生积极影响。

---

---

# English Original

---

# Exclusive: New Claude Model Triggers Stricter Safeguards at Anthropic — Jared Kaplan TIME Full Article

## Metadata

| Field | Value |
|-------|-------|
| **Date** | May 2025 |
| **Platform** | TIME |
| **Speaker** | Jared Kaplan (Co-founder, Chief Science Officer, Responsible Scaling Officer, Anthropic) |
| **Topic** | Claude Opus 4, ASL-3, bioweapon risks, Responsible Scaling Policy |

---

## Full Article (Key Excerpts)

**By Billy Perrigo**

Today's newest AI models might be capable of helping would-be terrorists create bioweapons or engineer a pandemic, according to the chief scientist of the AI company Anthropic.

Anthropic has long been warning about these risks—so much so that in 2023, the company pledged to not release certain models until it had developed safety measures capable of constraining them.

Now this system, called the Responsible Scaling Policy (RSP), faces its first real test.

On Thursday, Anthropic launched Claude Opus 4, a new model that, in internal testing, performed more effectively than prior models at advising novices on how to produce biological weapons, says Jared Kaplan, Anthropic's chief scientist. **"You could try to synthesize something like COVID or a more dangerous version of the flu—and basically, our modeling suggests that this might be possible,"** Kaplan says.

Accordingly, Claude Opus 4 is being released under stricter safety measures than any prior Anthropic model. Those measures—known internally as AI Safety Level 3 or "ASL-3"—are appropriate to constrain an AI system that could "substantially increase" the ability of individuals with a basic STEM background in obtaining, producing or deploying chemical, biological or nuclear weapons, according to the company. They include beefed-up cybersecurity measures, jailbreak preventions, and supplementary systems to detect and refuse specific types of harmful behavior.

To be sure, Anthropic is not entirely certain that the new version of Claude poses severe bioweapon risks, Kaplan tells TIME. But Anthropic hasn't ruled that possibility out either.

**"If we feel like it's unclear, and we're not sure if we can rule out the risk—the specific risk being uplifting a novice terrorist, someone like Timothy McVeigh, to be able to make a weapon much more destructive than would otherwise be possible—then we want to bias towards caution, and work under the ASL-3 standard,"** Kaplan says. **"We're not claiming affirmatively we know for sure this model is risky … but we at least feel it's close enough that we can't rule it out."**

If further testing shows the model does not require such strict safety standards, Anthropic could lower its protections to the more permissive ASL-2, under which previous versions of Claude were released, he says.

### Anthropic's new safeguards

Anthropic's ASL-3 safety measures employ what the company calls a **"defense in depth"** strategy—meaning there are several different overlapping safeguards that may be individually imperfect, but in unison combine to prevent most threats.

One of those measures is called **"constitutional classifiers:"** additional AI systems that scan a user's prompts and the model's answers for dangerous material. Earlier versions of Claude already had similar systems under the lower ASL-2 level of security, but Anthropic says it has improved them so that they are able to detect people who might be trying to use Claude to, for example, build a bioweapon. These classifiers are specifically targeted to detect the long chains of specific questions that somebody building a bioweapon might try to ask.

Anthropic has tried not to let these measures hinder Claude's overall usefulness for legitimate users—since doing so would make the model less helpful compared to its rivals. **"There are bioweapons that might be capable of causing fatalities, but that we don't think would cause, say, a pandemic,"** Kaplan says. **"We're not trying to block every single one of those misuses. We're trying to really narrowly target the most pernicious."**

Another element of the defense-in-depth strategy is the prevention of **jailbreaks**—or prompts that can cause a model to essentially forget its safety training and provide answers to queries that it might otherwise refuse. The company monitors usage of Claude, and "offboards" users who consistently try to jailbreak the model, Kaplan says. And it has launched a bounty program to reward users for flagging so-called "universal" jailbreaks. So far, the program has surfaced one universal jailbreak which Anthropic subsequently patched, a spokesperson says. The researcher who found it was awarded $25,000.

Anthropic has also beefed up its **cybersecurity**, so that Claude's underlying neural network is protected against theft attempts by non-state actors. The company still judges itself to be vulnerable to nation-state level attackers—but aims to have cyberdefenses sufficient for deterring them by the time it deems it needs to upgrade to ASL-4.

Lastly the company has conducted what it calls **"uplift" trials**, designed to quantify how significantly an AI model without the above constraints can improve the abilities of a novice attempting to create a bioweapon, when compared to other tools like Google or less advanced models. In those trials, which were graded by biosecurity experts, Anthropic found Claude Opus 4 presented a **"significantly greater"** level of performance than both Google search and prior models, Kaplan says.

**"I don't want to claim that it's perfect in any way. It would be a very simple story if you could say our systems could never be jailbroken,"** Kaplan says. **"But we have made it very, very difficult."**

Still, by Kaplan's own admission, only one bad actor would need to slip through to cause untold chaos. **"Most other kinds of dangerous things a terrorist could do—maybe they could kill 10 people or 100 people,"** he says. **"We just saw COVID kill millions of people."**

### RSP and industry

Anthropic's RSP—and similar commitments adopted by other AI companies—are all voluntary policies that could be changed or cast aside at will. The company itself, not regulators or lawmakers, is the judge of whether it is fully complying with the RSP. Breaking it carries no external penalty, besides possible reputational damage. Anthropic argues that the policy has created a **"race to the top"** between AI companies, causing them to compete to build the best safety systems.

**"We really don't want to impact customers,"** Kaplan told TIME earlier in May while Anthropic was finalizing its safety measures. **"We're trying to be proactively prepared."**

If Anthropic shows it can constrain itself without taking an economic hit, Kaplan says, it could have a positive effect on safety practices in the wider industry.

---

## Source Attribution

- **Primary Source**: [TIME – Exclusive: New Claude Model Triggers Stricter Safeguards at Anthropic](https://time.com/7287806/anthropic-claude-4-opus-safety/) (May 2025)
- **Author**: Billy Perrigo
- **Speaker**: Jared Kaplan, Co-founder, Chief Science Officer, Responsible Scaling Officer, Anthropic
