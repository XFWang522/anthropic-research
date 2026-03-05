# 与 Anthropic 联合创始人 Tom Brown 对话：宪法式 AI 与 LLM 改进

## 元数据

| 字段 | 值 |
|-------|-------|
| **日期** | 2023年12月19日 |
| **平台** | Salesforce Ventures（炉边对话） |
| **演讲者** | Tom Brown（联合创始人，Anthropic） |
| **主持人** | David Schmaier（Salesforce 总裁兼首席产品官） |
| **主题** | 宪法式 AI、RLHF、模型堆叠、Claude 2.1、幻觉减少、AGI 前景 |

---

## 完整内容

### 创建「无害」AI 的方法

Tom Brown 解释，许多模型使用基于人类反馈的强化学习（RLHF）进行训练。RLHF 的理念是，在关心的路径上对模型做得好或不好进行奖励和惩罚。他们让人们点赞或点踩模型执行任务的表现，这样可以让模型成为无害助手。

但随着模型变聪明，它们开始把大多数任务都做得很好。因此他们开发了宪法式 AI，将模型变成对另一个模型进行点赞或点踩的实体。一个人可以写下一份宪法，定义什么是「有用、无害、诚实」，然后模型会阅读人类与助手之间的互动，并考虑助手是否按照宪法行事。这是一种将简单文档转化为模型人格的方式。

### 「堆叠」LLM 以生成更高质量输出

Brown 讨论了将多个模型一起使用的策略。他们有 Claude 2.1（大型模型）和 Claude Instant（较小模型）。根据任务，有时会想要较小模型，因为它更快更便宜。例如，Midjourney 是他们的客户之一。每当用户在 Midjourney 输入任何提示生成文本时，会先通过 Claude Instant，Claude Instant 检查是否违反 Midjourney 的服务条款。如果认为可能违反，会给用户一条小消息说「这可能违反我们的条款。您要申诉吗？」如果用户点击是，就会转到 Claude Instant 的「上司」Claude 2.1，后者会思考更久，也许会说「抱歉，Claude Instant 完全错了，你其实没问题。」

### 构建领域特定模型

Brown 提出两种构建领域特定模型的方式。一是对大型模型进行微调，使其在特定任务上更好。二是构建在某一特定事情上表现好的窄模型。Claude Instant 比 Claude 2.1 更快更便宜，但性能较低。可以对任一进行微调，但 Claude 2.1 仍会表现更好。他认为微调大型模型是人们成功做过的事，而非让超小模型在某个窄领域表现好。

### 新 AI 用例

Brown 认为代码是模型表现出色的领域。用于质量保证的检索增强生成（RAG）是模型可以做得很好且非常有用的广泛领域。他觉得客户服务非常适合这一领域。

### 减少 AI 幻觉

他们有一系列内部幻觉率指标，并有团队全力降低该数字。Claude 2.1 在 Claude 2 发布约四个月后推出。在他们内部仪表板上，它将错误率降低了 2 倍。仍有一些幻觉，但数量是以前的一半。例如，如果现在模型准确率为 98%，需要达到 99%，可能只需四个月。如果需要达到 99.9%，可能需要一年左右。此外，任务越难，模型越可能产生幻觉或犯错。就像一个人试图同时处理多项任务时，会比只专注一件事犯更多错误。

### AGI 前景

Brown 认为他们已经有弱 AGI。可以与 ChatGPT 或 Claude 交谈，它具有一定智能，每年都在改善。现在可以提示模型建立一家成功的创业公司，它会尝试，但会卡住。但随着增加算力，模型会变聪明，模型的 IQ 会上升。因此如果模型突然停止变好会令人惊讶。然后问题是它们能变多好？他们不知道模型需要走多远才能成为能出色完成工作的 AI 创业者。但每年似乎都在获得更多 IQ 点，所以在某个时候他们会得到比他自己更擅长工程的模型。

### AI 将用于善还是恶

Brown 表示总体上谨慎乐观。人不是天使也不是魔鬼，人就是人。所以他认为人们会以各种不同方式使用 AI，作为社会我们有责任确保收益超过成本。他对最近的监管更新感到鼓舞。他一直担心政府会介入并做一些不太合理的事。但最近的 AI 行政命令似乎相当 sensible。所以他认为自己比一年半前乐观得多。

---

# English Original

---

# In Conversation With Anthropic Co-Founder Tom Brown: Constitutional AI and LLM Improvements

## Metadata

| Field | Value |
|-------|-------|
| **Date** | December 19, 2023 |
| **Platform** | Salesforce Ventures (Fireside Chat) |
| **Speaker** | Tom Brown (Co-founder, Anthropic) |
| **Moderator** | David Schmaier (President and Chief Product Officer, Salesforce) |
| **Topic** | Constitutional AI, RLHF, model stacking, Claude 2.1, hallucination reduction, AGI prospects |

---

## Full Content

### On Anthropic's Approach to Creating 'Harmless' AI

Tom Brown explained that many models are trained using reinforcement learning from human feedback (RLHF). The idea behind RLHF is you reward and punish the model for doing well or not doing well on the paths you care about. They had people upvoting or downvoting how well the model does a task. That's how you can make the model become a harmless assistant.

He thinks they noticed that as the models were getting smarter, they started to do most tasks well. They developed constitutional AI to turn a model into the entity that upvotes or downvotes another model. A person can write up a constitution of what it means to be helpful, harmless, and honest, and then a model will read the interactions between the human and the assistant and consider if the assistant is acting in accordance with the constitution. This is a way to take a simple document and turn it into a model personality.

### On the Impact of 'Stacking' LLMs to Generate Higher-Quality Outputs

Brown discussed using multiple models together. They have Claude 2.1, which is a large model, and Claude Instant, which is a smaller model. Depending on the task, sometimes you'll want a smaller model because it's faster and cheaper. For example, Midjourney is one of their customers. Whenever you put any prompt into Midjourney to generate text, it'll pass it through Claude Instant and Claude Instant checks if it's violating Midjourney's terms of service. And if it thinks it might be, it'll give a little message to the user saying 'this might be against our terms. Do you want to appeal it?' And if you hit yes, it goes to Claude Instant's boss, which is Claude 2.1, who thinks about it a little bit longer, and maybe says, 'Sorry, Claude Instant was totally wrong. You're fine actually.'

### On Building Domain-Specific Models

Brown said there are two different ways to think about building a domain-specific model. One is that you take a large model and fine tune it to make it better at a specific task. The other is you build a narrow model that's good at one specific thing. Claude Instant is faster and cheaper than Claude 2.1, but less performant. You can fine tune either one, but Claude 2.1 will still do better. So he thinks that's his normal mental model for what's going on with fine tuning. You could imagine someone building a very narrow model that's very good at one specific thing, but it feels like fine tuning a larger model is the thing people have successfully done rather than making a super small model good at some narrow field.

### On New AI Use Cases

Brown thinks code is a place where the models do great. Retrieval augmented generation (RAG) for quality assurance is a broad area that the models can do and be really useful at. He feels like customer service is an area that fits that very well.

### On Cutting Down on AI Hallucinations

They have a bunch of internal metrics for hallucination rates that they measure and a team that's fully focused on bringing that number down. Claude 2.1 came out last month, about four months after Claude 2. On their internal dashboards it reduced the error rate by 2x. It still has some hallucinations, but there are half as many as there used to be. So if, for example, you're seeing 98% accuracy with your model now and you need to get to 99%, maybe it'll only take four months. If you need to get 99.9%, it might take a year or something like that. Also, if it's a harder task, the model is more likely to hallucinate or make a mistake. It's the same as if a person is trying to juggle a bunch of tasks at once. You'll make more mistakes than if you're just focused on one thing.

### On the Prospect of AGI

Brown thinks they already have weak AGI. You can talk with ChatGPT or Claude and it's somewhat intelligent, and with each year it's improving. Right now you may prompt the model to build a successful startup. It'll try to do it, but it'll get stuck. But as they add more compute, the model gets smarter. The model's IQ goes up. So he thinks it would be surprising if the models suddenly stopped getting better. And then it's a question of how much better can they get? One thing they don't know is how far the model has to go for it to be an AI entrepreneur that could do a great job. But every year it seems like they're getting more IQ points so at some point he thinks they'll get models that are better at engineering than he is.

### On Whether AI Will Be Used for Good or Evil

Brown feels cautiously optimistic in general. People aren't angels and people aren't devils. People are people. So he thinks people will use AI for all sorts of different stuff and it's up to us as a society to make sure that the benefits outweigh the costs. He's been really heartened by the recent regulatory updates. He's always worried that the government would get involved and do things that don't quite make sense. But the recent AI executive order seems quite sensible. So he thinks he's much more optimistic now than he was a year and a half ago.

---

## Source Attribution

- **Primary Source**: Salesforce Ventures, "In Conversation With Anthropic Co-Founder Tom Brown"
- **Event Date**: December 19, 2023
- **Moderator**: David Schmaier, President and Chief Product Officer, Salesforce
- **Speaker**: Tom Brown, Co-founder, Anthropic
