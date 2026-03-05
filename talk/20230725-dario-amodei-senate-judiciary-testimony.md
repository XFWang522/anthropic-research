# AI 监管：监管原则

**日期：** 2023年7月25日

**平台/场合：** 美国参议院司法委员会隐私、技术与法律小组委员会

**演讲者：** 达里奥·阿莫迪，Anthropic 首席执行官

**时长：** 完整听证会（多名证人）

## 中文摘要

达里奥·阿莫迪在参议院司法委员会隐私、技术与法律小组委员会作证，作为题为「AI 监管：监管原则」的听证会的一部分。阿莫迪的口头证词聚焦于中期风险——特别是 AI 赋能生物武器滥用的威胁。他警告称，对当前系统进行简单外推，2-3 年内 AI 可能填补所有缺失环节，使更多行为体能够实施大规模生物攻击，构成对美国国家安全的严重威胁。他提出三项建议：保障 AI 供应链安全、建立新模型的测试与审计制度、资助测量与测量研究。阿莫迪还讨论了选举中的 misinformation、deepfakes、watermarking 以及 AI 在诈骗中的滥用等问题。完整听证会记录可在 GovInfo 获取。

---

# English Original

---

# Oversight of A.I.: Principles for Regulation

**Date:** July 25, 2023

**Platform/Venue:** U.S. Senate Judiciary Subcommittee on Privacy, Technology, and the Law

**Speaker:** Dario Amodei, CEO of Anthropic

**Duration:** Full hearing (multiple witnesses)

## Full Oral Testimony of Dario Amodei

**Mr. Amodei:** Chairman Blumenthal, Ranking Member Hawley, and Members of the Committee, thank you for the opportunity to discuss the risks and oversight of AI with you. Anthropic is a public benefit corporation that aims to lead by example in developing and publishing techniques to make AI systems safer and more controllable and by deploying these safety techniques in state-of-the-art models.

Research conducted by Anthropic includes constitutional AI, a method for training AI systems to behave according to an explicit set of principles; early work on red teaming, or adversarial testing of AI systems to uncover bad behavior; and foundational work in AI interpretability, the science of trying to understand why AI systems behave the way they do. This month, after extensive testing, we were proud to launch our AI model Claude 2 for U.S. users. Claude 2 puts many of these safety improvements into practice. While we're the first to admit that our measures are still far from perfect, we believe they're an important step forward in a race to the top on safety. We hope we can inspire other researchers and companies to do even better.

AI will help our country accelerate progress in medical research, education, and many other areas. As you said in your opening remarks, the benefits are great. I would not have founded Anthropic if I did not believe AI's benefits could outweigh its risks. However, it is very critical that we address the risks.

My written testimony covers three categories of risks: short-term risks that we face right now, such as bias, privacy, misinformation; medium-term risks related to misuse of AI systems as they become better at science and engineering tasks; and long-term risks related to whether models might threaten humanity as they become truly autonomous, which you also mentioned in your opening testimony.

In these short remarks, I want to focus on the medium-term risks, which present an alarming combination of imminence and severity.

Specifically, Anthropic is concerned that AI could empower a much larger set of actors to misuse biology. Over the last 6 months, Anthropic, in collaboration with world-class biosecurity experts, has conducted an intensive study of the potential for AI to contribute to the misuse of biology.

Today, certain steps in bioweapons production involve knowledge that can't be found on Google or in textbooks and requires a high level of specialized expertise, this being one of the things that currently keeps us safe from attacks.

We've found that today's AI tools can fill in some of these steps, albeit incompletely and unreliably. In other words, they are showing the first nascent signs of danger. However, a straightforward extrapolation of today's systems to those we expect to see in 2 to 3 years suggests a substantial risk that AI systems will be able to fill in all the missing pieces, enabling many more actors to carry out large-scale biological attacks. We believe this represents a grave threat to U.S. national security.

We have instituted mitigations against these risks in our own deployed models; briefed a number of U.S. Government officials, all of whom found the results disquieting; and are piloting a responsible disclosure process with other AI companies, to share information on this and similar risks. However, private action is not enough. This risk, and many others like it, requires a systemic policy response.

We recommend three broad classes of actions.

First, the U.S. must secure the AI supply chain in order to maintain its lead while keeping these technologies out of the hands of bad actors. This supply chain runs from semiconductor manufacturing equipment to chips and even the security of AI models stored on the servers of companies like ours.

Second, we recommend a testing and auditing regime for new and more powerful models. Similar to cars or airplanes, AI models of the near future will be powerful machines that possess great utility but can be lethal if designed incorrectly or misused. New AI models should have to pass a rigorous battery of safety tests before they can be released to the public at all, including tests by third parties and national security experts in Government.

Third, we should recognize that the science of testing and auditing for AI systems is in its infancy. It is not currently easy to detect all the bad behaviors an AI system is capable of without first broadly deploying it to users, which is what creates the risk. Thus, it is important to fund both measurement and research on measurement to ensure a testing and auditing regime is actually effective. Funding NIST and the National AI Research Resource are two examples of ways to ensure America leads here.

The three directions above are synergistic. Responsible supply chain policies help give America enough breathing room to impose rigorous standards on our own companies without ceding our national lead to adversaries, and funding measurement, in turn, makes these rigorous standards meaningful. The balance between mitigating AI's risks and maximizing its benefits will be a difficult one, but I'm confident that our country can rise to the challenge. Thank you.

## Key Exchange: Elections and Misinformation

**Chair Blumenthal:** Let me ask each of you what you see as the immediate threats to the integrity of our election system... I'll begin with you, Mr. Amodei.

**Mr. Amodei:** Yes. So, thanks for the question, Senator. You know, I think this is obviously a very timely thing to worry about. You know, when I think of the risks here, my mind goes to misinformation, generation of deepfakes, use of AI systems to manipulate people or produce propaganda or just do anything deceptive.

You know, I can speak a little bit about some of the things we're doing. You know, we train our model with, you know, this method called constitutional AI, where you can lay out explicit principles. It doesn't mean the model will follow the principles, but there are terms in our constitution, which is publicly available, that tells the model not to generate misinformation. The same is true in our business terms of use.

One of the commitments with the White House was to start to watermark content, particularly in the audio and the visual domain. I think that's very helpful but would also benefit from—watermarking gives you the technical capability, you know, to detect that something is AI generated, but requiring it on the side of the law to be labeled, I think, would be something that would be very helpful and timely.

## Key Exchange: Scams and Voice Cloning

**Senator Klobuchar:** Mr. Amodei, one significant concern—I just talked to some people in the banking community about this, small banks, is that they are really worried they're going to see AI used to scam people. You know, pretending to be your mom's voice or your, more likely, granddaughter's voice, actually getting that voice right, making a call for money. How can Congress ensure that companies that create AI platforms cannot be used for those deceptive platforms?

**Mr. Amodei:** Yes, Senator. So, I think these questions about deception and scams are probably closely related to these questions about misinformation. Right?... I think we need both [technical measures and policy measures] and probably, you know, this Congress can do more on the second thing, and the companies and researchers can do more on the first thing... certainly I'd be in favor of strengthened protections there.

## Key Exchange: Google Investment and Anthropic Structure

**Senator Hawley:** Google owns a significant stake in your company, doesn't it?

**Mr. Amodei:** Yes. Google was an investor in Anthropic. They don't control any board seats, but yes, Google is an investor in Anthropic.

**Senator Hawley:** The press has reported it at $300 million in investment, with at least a 10 percent stake in the company. Does that sound broadly correct?

**Mr. Amodei:** That sounds broadly correct.

**Senator Hawley:** So, there's no plans to integrate your Claude, your equivalent of ChatGPT—there's no plans to integrate that with Google Search, for example?

**Mr. Amodei:** That's not occurring at the present time.

## Key Exchange: Transparency and Interpretability

**Senator Klobuchar:** Do you agree with it, too, then [on researcher access]?

**Mr. Amodei:** Yes. I just wanted to say I think transparency is important even as a broader issue. You know, a number of our research efforts go into looking inside to see what happens inside AI systems, why they make the decisions that they make.

## Sources

- U.S. Government Publishing Office: [CHRG-118shrg53503](https://www.govinfo.gov/content/pkg/CHRG-118shrg53503/html/CHRG-118shrg53503.htm) — Full hearing transcript
- Senate Judiciary Committee: [Written testimony of Dario Amodei](https://www.judiciary.senate.gov/download/2023-07-26-testimony-amodei)
- Congressional hearing records, July 25, 2023
