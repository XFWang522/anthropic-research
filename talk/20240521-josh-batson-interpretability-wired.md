# AI 是黑箱：Anthropic 找到了窥视内部的方法

## 元数据

| 字段 | 值 |
|-------|-------|
| **日期** | 2024年5月21日 |
| **平台** | WIRED、Fast Company |
| **演讲者** | Josh Batson（可解释性团队负责人，Anthropic）、Chris Olah（联合创始人，Anthropic） |
| **主题** | 机制可解释性、AI 显微镜、追踪数据模式、特征、电路 |

---

## 完整内容

### 十年执念：神经网络内部发生了什么

过去十年，AI 研究者 Chris Olah 一直痴迷于人工神经网络。一个特别的问题吸引着他，并成为他工作的中心——首先在 Google Brain，然后在 OpenAI，今天在 AI 创业公司 Anthropic，他是联合创始人。「里面发生了什么？」他说。「我们有这些系统，我们不知道里面发生了什么。这似乎很疯狂。」

### 机制可解释性如同 AI 显微镜

Josh Batson 将机制可解释性描述为「AI 显微镜」——一种窥视神经网络内部、理解其如何运作的工具。他解释了追踪数据模式的目标，能够「逐步追踪当你将提示输入模型时它为何说出下一个词」。机制可解释性允许研究者窥视模型内部、观察内部计算，揭示否则不透明的结构，实现科学理解而不仅是经验观察。

### 计算的数字无法说明「模型如何思考」

在训练期间，LLM 处理大量文本，最终根据含义和使用语境形成词语和短语的多维「地图」。模型投入使用后，它利用这张「地图」计算对用户提示最统计上可能的下一个词。Anthropic 可解释性研究者 Josh Batson 说，研究者可以看到导致输出的所有计算，但这些数字对「模型如何思考」说明不了多少。换句话说，Anthropic 研究者想了解大型 AI 模型用来将词语组织成相关回应的高阶概念。

### 中断处理并拍摄内部状态快照

Batson 说他的团队学会了如何在模型处理提示的过程中中断它，并拍摄其内部状态的快照。他们可以看到网络中哪些神经元同时激活，并且知道某些神经元集合在响应提示中相同类型的词时会同时激活。例如，Batson 说他们给模型一个提示：「在一个美丽的春日，我开车从旧金山穿过伟大的跨度前往马林……」然后中断了网络。他们看到一组神经元激活，他们知道应该代表金门大桥的概念。他们很快发现，当模型被类似暗示金门大桥的一组词（或图像）提示时，同一组神经元会激活。

### 识别数百万概念

使用同样的方法，他们开始识别其他概念。「我们学会了从模型内部识别数百万个不同的概念，我们可以告诉它何时在使用每一个，」Batson 告诉我。Batson 首先在小型简单模型上尝试了这些方法，然后花了过去八个月努力让这些方法在大型 LLM 上工作——在这种情况下是 Anthropic 的 Claude Sonnet 3。

### 安全影响：从内部引导

有了在过程中期解释模型正在思考什么的能力，研究者可能有机会将 AI 引导远离不良输出，如偏见、错误信息或制造生物武器的指示。如果研究者可以中断 LLM 对输入的处理，并向系统注入信号，就可能影响和改变过程的方向，可能朝向更理想的输出。AI 公司做了大量工作将模型引导远离有害输出，但它们主要依赖迭代过程：改变提示（输入）并研究那如何影响输出的有用性或安全性。它们从外向内解决问题，而非从内向外。Anthropic 由一群关心安全的 OpenAI 高管创立，正在推进一种通过注入数据有意影响过程、将模型引导向更好方向的方法。

### 追踪数据模式

可解释性追踪数据如何流经模型。识别哪些神经元或电路对哪些输入激活。绘制从提示到输出的「路径」。建立模型行为的因果理解。

### 逐步理解的目标

目标：「逐步追踪当你将提示输入模型时它为何说出下一个词」。每个 token 生成涉及许多内部步骤。可解释性旨在使每步可读。支持调试、安全评估和信任。

### 挑战

规模使可解释性更难——更大模型更复杂。并非所有行为都可解释。持续研究改进技术。将可解释性作为长期安全基础设施投入。

---

# English Original

---

# AI Is a Black Box. Anthropic Figured Out a Way to Look Inside

## Metadata

| Field | Value |
|-------|-------|
| **Date** | May 21, 2024 |
| **Platform** | WIRED, Fast Company |
| **Speakers** | Josh Batson (Interpretability Team Lead, Anthropic), Chris Olah (Cofounder, Anthropic) |
| **Topic** | Mechanistic interpretability, AI microscope, tracing data patterns, features, circuits |

---

## Full Content

### A Decade-Long Obsession: What's Going on Inside Neural Networks

For the past decade, AI researcher Chris Olah has been obsessed with artificial neural networks. One question in particular engaged him, and has been the center of his work, first at Google Brain, then OpenAI, and today at AI startup Anthropic, where he is a cofounder. "What's going on inside of them?" he says. "We have these systems, we don't know what's going on. It seems crazy."

### Mechanistic Interpretability as AI Microscope

Josh Batson describes mechanistic interpretability as an "AI microscope"—a tool for seeing inside neural networks and understanding how they work. He explains the goal of tracing data patterns and being able to "walk through step-by-step when you put a prompt into a model why it says the next word." Mechanistic interpretability allows researchers to peer inside models and see internal computation, reveals structure that would otherwise be opaque, and enables scientific understanding, not just empirical observation.

### The Numbers Don't Say Much About "How the Model Is Thinking"

During its training, an LLM processes a huge amount of text and eventually forms a many-dimensional map of words and phrases, based on their meanings and the contexts within which they're used. After the model goes into use, it draws on this "map" to calculate the most statistically likely next word in a response to a user prompt. Researchers can see all the calculations that lead to an output, says Anthropic interpretability researcher Josh Batson, but the numbers don't say much about "how the model is thinking." The Anthropic researchers, in other words, wanted to learn about the higher-order concepts that large AI models use to organize words into relevant responses.

### Interrupting Processing and Taking a Snapshot of Internal State

Batson says his team has learned how to interrupt the model halfway through its processing of a prompt and take a snapshot of its internal state. They can see which neurons in the network are firing at the same time, and they know that certain sets of these neurons fire at the same time in response to the same types of words in a prompt. For example, Batson says they gave the models a prompt that said, "On a beautiful spring day, I was driving from San Francisco to Marin across the great span of the . . ." then interrupted the network. They saw a set of neurons firing that they knew should represent the concept of the Golden Gate Bridge. And they soon saw that the same set of neurons fired when the model was prompted by a similar set of words (or images) suggesting the Golden Gate Bridge.

### Recognizing Millions of Concepts

Using this same method, they began to identify other concepts. "We learned to recognize millions of different concepts from inside the model, and we can tell when it's using each of these," Batson says. Batson first tried its methods on a small and simple model, then spent the past eight months working to make those methods work on a big LLM, in this case Anthropic's Claude Sonnet 3.

### Safety Implications: Steering from the Inside

With the ability to interpret what a model is thinking about in the middle of its process, researchers may have an opportunity to steer the AI away from bad outputs such as bias, misinformation, or directions to create a bioweapon. If researchers can interrupt the LLM's processing of an input, and inject a signal into the system, it could influence and alter the direction of the process, possibly toward a more desirable output. AI companies do a lot of work to steer their models away from harmful outputs, but they mainly rely on an iterative process of altering the prompts (inputs) and studying how that affects the usefulness or safety of the output. They address problems from the outside in, not from the inside out. Anthropic, which was founded by a group of OpenAI executives who were concerned about safety, is advancing a means of purposefully influencing the process with the injection of data to steer the model in a better direction.

### Tracing Data Patterns

Interpretability traces how data flows through the model. Identifies which neurons or circuits activate for which inputs. Maps the "path" from prompt to output. Builds causal understanding of model behavior.

### Goal of Step-by-Step Understanding

Goal: "Walk through step-by-step when you put a prompt into a model why it says the next word." Each token generation involves many internal steps. Interpretability aims to make each step legible. Enables debugging, safety evaluation, and trust.

### Challenges

Scale makes interpretability harder—larger models have more complexity. Not all behaviors may be interpretable. Ongoing research to improve techniques. Investment in interpretability as long-term safety infrastructure.

---

## Source Attribution

- **Primary Sources**: WIRED "AI Is a Black Box. Anthropic Figured Out a Way to Look Inside"; Fast Company "Anthropic takes a look into the 'black box' of AI models"
- **Publication Date**: May 21, 2024
- **Authors**: Steven Levy (WIRED), Mark Sullivan (Fast Company)
- **Speaker**: Josh Batson, Interpretability Team Lead, Anthropic
- **Related**: Anthropic scaling monosemanticity research (transformer-circuits.pub)
