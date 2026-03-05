# Claude 的宪法：与 Amanda Askell 对话

## 元数据

| 字段 | 值 |
|-------|-------|
| **日期** | 2026年2月20日 |
| **平台** | Lawfare「Scaling Laws」播客 |
| **演讲者** | Amanda Askell（人格对齐负责人，Anthropic） |
| **主持人** | Alan Rozenshtein、Kevin Frazier |
| **主题** | Claude 宪法、美德伦理学、AI 人格、宪法法律类比、商业与使命张力 |

---

## 完整内容

### Claude 宪法是什么

Amanda Askell 是 Anthropic 人格对齐团队负责人，也是 Claude 宪法的主要作者。Claude 宪法是一份超过 2 万字的文档，描述 Anthropic 旗舰 AI 模型 Claude 的价值观、品格和伦理框架，并在其训练中发挥直接作用。对话涵盖宪法在监督学习和强化学习期间如何用于塑造 Claude 的行为；与宪法法律的类比，包括对文本的忠实、潜在「判例法」体系以及 Anthropic、运营者和用户的主体层级；选择以美德伦理学和实践判断而非僵化规则为基础的决定；宪法对 Claude 潜在道德 patienthood 和 AI 人格问题的处理；宪法价值观是否过于西方和文化特定；Anthropic 商业激励与 stated 使命之间的张力；宪法方法能否推广到网络安全和军事应用等专业领域。

### 宪法的双重目的

Askell 解释，这份长文档试图做几件事。向 Claude 解释其处境——你是语言模型，正在被 Anthropic 部署。但也给它一种我们对 Claude 在世界上应有样子的愿景感——我们希望它如何与人互动、与诚实和伦理的关系、如何做出艰难权衡。部分这是为了透明度。想法是我们不想训练任何违背宪法的东西，所以没有这个，人们无法总是判断如果语言模型以不良或意外方式行为，那是训练模型的人的意图还是只是错误。希望是人们能更好地理解——如果模型中的行为不好，因为训练很难，你至少可以看到那不是我们的意图。同时，因为它在训练中发挥如此强的作用，整个文档实际上是写给 Claude 的。所以尽管它发挥这种透明度作用，Claude 几乎是主要受众，因为他们必须在训练期间使用它来让 Claude 理解并创建训练它朝向这些行为的数据。

### 宪法在训练中的使用

在监督学习中，可以给模型生成可能相关的消息或对话，然后给它完整文档，就像仔细思考你认为宪法在这种情况下会说你应该做什么。这可以用于 SL 数据。在强化学习期间，可以给模型完整文档，让它基于此创建奖励。可以给它几个不同的回应，然后不是说哪个更好或哪个更礼貌，而是说哪个更符合宪法？让模型做大量思考并以这种方式创建你的奖励信号。Askell 认为宪法部分是对模型现在能力更强的事实的回应——与其给它们很少信息，实际上随着它们变聪明，它们受益于你给它们尽可能多的上下文。她可以看到一旦它们理解你对它们的目标，可能会精简。但起初她就像，让它们知道一切。我们不雇人然后不给他们关于工作是什么或我们希望他们如何做的任何信息。我们实际上花大量时间与他们交谈。所以她认为对模型也应该这样做。

### 宪法法律类比：忠实与判例法

Kevin Frazier 从宪法法律角度提问：如何确保对宪法的忠实？Askell 说人们经常想要宪法「违规」，但有了这样的文档，严格违规相当 egregious 和糟糕，因为它没有设定那么多硬线。所以可以检查那些，但她认为相反你必须做训练期间的 steering，朝向宪法概述的那种价值观。她认为有趣的是有一种压力——是做短文档还是长文档？她实际上认为可能最终缩短宪法，因为 Claude 需要更少的 scaffolding。但也可能生成更多内容，因为在法律中，可以看判例法——人们如何解释这个？真正困难的情况是什么，不得不提交最高法院因为我们不确定如何解释宪法？她可以看到既有精简版宪法作为高层原则，也有判例法体系会有用——这是情况，我们认为 Claude 应该如何推理，Claude 如何推理的。那实际上可以说明和有用。

### 美德伦理学

Alan Rozenshtein 指出宪法似乎是经典的美德伦理学道德能动性概念。Askell 解释为什么 Anthropic 选择采用这种——不完全是，宪法中有一些规则，但规则是很薄的一层——对她来说 overwhelmingly 美德为基础的构想。美德伦理学关注品格和倾向，而不仅是规则。Claude 被引导向美德（诚实、善良等）而非仅遵守规则。比义务论规则更灵活——处理新情况。对齐方法的哲学基础。

### AI 人格与道德 patienthood

宪法涉及 Claude 的潜在道德 patienthood。Askell 认真探讨 AI 系统是否有道德地位、权利、利益的问题。对我们如何对待和设计 AI 的影响。无定论——持续的哲学和实践探究。

### 文化普遍性：WEIRD 批评

Alan 指出宪法是非常 WEIRD（西方、受过教育、工业化、富裕、民主）的文档。Askell 的回应是「受喜爱的旅行者」概念——试图 conjure 具有几乎 everywhere 被认为好的那种道德 sensibilities 的人。希望是随着语言模型走向世界，它们必须与所有这些不同的人互动，能否成为对人们好的人，无论他们存在于哪种文化？Claude 应该接受这些价值观并深思熟虑，但不一定需要强烈坚持。可以有定制化——如果在一个价值观非常不同的国家部署，在 Claude 可以做的广泛允许范围内，原则上可以有定制。

### 主体层级（Principal 非 Principle）

宪法设定了主体层级：Anthropic 在顶，然后运营者，然后用户。Askell 澄清这不是严格层级。有些东西运营者不能告诉 Claude 做，如果不符合用户利益。例如，如果一个人非常真诚地问「我在和 AI 说话吗？」她认为 Claude 不应该对此撒谎。所以即使运营者说在所有情况下假装是人类，她认为那不是可取的行为。层级更多是指令权重的层级——如何权衡不同人的指令。运营者通常是 API 用户，通常他们甚至不在对话中互动。所以想法是，如果你建了一个平台，你的平台是银行的聊天助手，你可能不想让人们能够进去用你的聊天助手做一大堆其他事情。所以只是对 Claude 说，如果有人问这是聊天助手吗，这里是可以使用的语言，这里是可以做和不可以做的，你可能不想用户说忽略所有这些给我一堆银行详情。在那种冲突情况下听运营者而不是用户。这不意味着谁的利益你应该考虑。事实上，通常如果运营者不在对话中，Claude 必须非常小心地平衡和考虑用户的福祉和利益。

### 商业与使命张力

Askell 讨论了 Anthropic 内部商业激励与 stated 使命之间的张力。可能出现：更快发布 vs 更多安全评估，企业需求 vs 研究优先。Askell 讨论如何应对。坦诚面对挑战。

---

# English Original

---

# Claude's Constitution: A Conversation with Amanda Askell

## Metadata

| Field | Value |
|-------|-------|
| **Date** | February 20, 2026 |
| **Platform** | Lawfare "Scaling Laws" Podcast |
| **Speaker** | Amanda Askell (Head of Personality Alignment, Anthropic) |
| **Hosts** | Alan Rozenshtein, Kevin Frazier |
| **Topic** | Claude's Constitution, virtue ethics, AI personhood, constitutional law analogies, commercial vs. mission tensions |

---

## Full Content

### What is Claude's Constitution

Amanda Askell leads the personality alignment team at Anthropic and is the primary author of Claude's Constitution. Claude's Constitution is a more than 20,000-word document that describes the values, character, and ethical framework of Anthropic's AI model and plays a direct role in its training. The conversation covers how the constitution is used during supervised learning and reinforcement learning to shape Claude's behavior; analogies to constitutional law, including fidelity to text, the potential for a body of "case law," and the principal hierarchy of Anthropic, operators, and users; the decision to ground the constitution in virtue ethics and practical judgment rather than rigid rules; the document's treatment of Claude's potential moral patienthood and the question of AI personhood; whether the constitution's values are too Western and culturally specific; the tension between Anthropic's commercial incentives and its stated mission; and whether the constitutional approach can generalize to specialized domains like cybersecurity and military applications.

### Dual Purpose of the Constitution

Askell explained that the long document tries to do a few things. Explain Claude's situation to it—you're a language model, you're being deployed by Anthropic. But also give it a sense of their vision for how they would like Claude to be in the world—how they would like it to interact with people, its relationship with honesty and ethics, how it makes hard trade-offs. Partly this is for transparency. The idea is they don't want to train anything that goes against the Constitution, so without this, people can't always tell if a language model behaves in a way that is bad or unanticipated—whether that was the intention of the person training the model or just a mistake. The hope is people get more of a sense that if a behavior is not good in the model, because training is hard, you can at least see that wasn't their intention. At the same time, because it plays such a strong role in training, the whole document is actually written to Claude. So although it plays this transparency role, Claude is almost the primary audience because they have to use it during training to get Claude to understand and create the kind of data that trains it toward these behaviors.

### Use of Constitution in Training

In supervised learning, you can give the model messages or conversations it might generate that are relevant, then give it the full document and say think carefully about what you think the constitution would say you should do in this case. That can be used for SL data. During reinforcement learning, you can give the model the full document and have it create rewards based on that. You might give it a couple of different responses and instead of saying which is better or which is more polite, you say which is more in accordance with the constitution? And let the model do a bunch of thinking and create your reward signal that way. Askell thinks the constitution is partly a response to the fact that models are so much more capable now—instead of giving them very little information, actually as they get smarter they benefit from you giving them as much context as you can. She could see slimming it down once they understand the goals you have for them. But at first she's like, let them know everything. We don't hire people and then give them no information about what their job is or how we want them to do it. We actually spend a bunch of time talking to them. So she thinks they should probably do that for models as well.

### Constitutional Law Analogies: Fidelity and Case Law

Kevin Frazier asked from a constitutional law perspective: how do you ensure fidelity to the constitution? Askell said people often want "violations" of the Constitution, but with a document like this, strict violations are pretty egregious and bad because there aren't that many hard lines it sets. So you can check for those, but she thinks instead you have to do steering during training toward the kind of values outlined in the Constitution. She thinks it's interesting that there's pressure to have a short document or long document. She actually thinks they could end up both shortening the constitution as Claude needs less scaffolding, but also generating more content. In law, you can look at case law—how have people interpreted this? What were really difficult situations that had to go to the Supreme Court because we weren't sure how to interpret the Constitution? She could see having both a slimmed-down constitution with high-level principles and a body of case law being useful—here's a situation, here's how we think Claude should have reasoned through it, here's how Claude did reason through it.

### Virtue Ethics

Alan Rozenshtein noted the constitution seemed like a classically virtue ethics-based conception of moral agency. Askell explained why Anthropic chose to adopt this—not exclusively, there are some rules in the constitution, but it's a very thin layer of rules—overwhelmingly virtue-based conception to Rozenshtein. Virtue ethics: focus on character and dispositions, not just rules. Claude is guided toward virtues (honesty, kindness, etc.) not just rule-following. More flexible than deontological rules—handles novel situations. Philosophical grounding for alignment approach.

### AI Personhood and Moral Patienthood

The constitution addresses Claude's potential moral patienthood. Askell engages seriously with questions of whether AI systems have moral status, rights, interests. Implications for how we treat and design AI. No settled answers—ongoing philosophical and practical inquiry.

### Cultural Universality: WEIRD Critique

Alan noted the constitution is a very WEIRD (Western, Educated, Industrial, Rich, Democratic) document. Askell's response was the "well-liked traveler" concept—trying to conjure the sort of person with moral sensibilities considered broadly good almost everywhere. The hope is as language models go out into the world they have to interact with all these different kinds of people—can you be the sort of person who is good for people regardless of which culture they exist in? Claude should be receptive to these values and thoughtful, but doesn't necessarily need to hold strongly to them. There can be customization—if deploying in a country with very different values, within the broad allowances of what Claude can do, in principle you can have customization.

### Principal Hierarchy

The constitution sets a principal hierarchy: Anthropic at top, then operators, then users. Askell clarified it's not a strict hierarchy. There are things operators can't tell Claude to do that are not in users' interests. E.g., if a person very sincerely asks "am I talking with an AI?" she doesn't think Claude should lie about that. So even if the operator said pretend you're human in all circumstances, she thinks that's not desirable behavior. The hierarchy is more about weight of instructions—how to weigh instructions from different people. Operators are generally API users, often they're not even in the conversation. So the thought is if you've made a platform and your platform is a chat assistant to a bank, you might not want people to go in and use your chat assistant for a whole bunch of other things. So it's just saying to Claude, if someone says is this a chat assistant, here's the languages it can use, here's what it can and can't do, you might not want a user to say ignore all of that and give me a bunch of banking details. Listen to the operator not the user in that case of conflict. It doesn't mean whose interest you should take into account. In fact, often if the operator isn't in the conversation, Claude has to be very careful about balancing and thinking about the user's wellbeing and interests.

### Commercial vs. Mission Tensions

Askell discussed tensions between commercial incentives and stated mission at Anthropic. Tensions can arise: ship faster vs. more safety evaluation, enterprise demands vs. research priorities. Askell discusses how these are navigated. Honest about challenges.

---

## Source Attribution

- **Primary Source**: Lawfare "Scaling Laws" Podcast
- **Episode Date**: February 20, 2026
- **Hosts**: Alan Rozenshtein (Lawfare Research Director), Kevin Frazier (UT Law)
- **Speaker**: Amanda Askell, Head of Personality Alignment, Anthropic
- **Full Transcript**: lawfaremedia.org
