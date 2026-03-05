# AI 可解释性的紧迫性

**日期：** 2025年4月

**平台/场合：** 发表于 darioamodei.com 和 LessWrong 的文章

**演讲者：** 达里奥·阿莫迪，Anthropic 首席执行官

## 中文全文

在我从事 AI 工作的十年里，我目睹它从一个微小的学术领域成长为 arguably 世界上最重要的经济和地缘政治议题。在这段时间里，我学到的最重要的一课或许是：底层技术的进步是不可阻挡的，由过于强大的力量驱动而无法停止，但它的发生方式——事物的构建顺序、我们选择的应用、以及它如何向社会推出的细节——是完全可以改变的，通过这样做可以产生巨大的积极影响。我们无法阻止巴士，但我们可以驾驭它。过去我写过以积极方式部署 AI 的重要性，以及确保民主国家在专制国家之前构建和运用该技术的重要性。过去几个月，我越来越关注驾驭巴士的另一个机会：近期突破所开启的 tantalizing 可能性——我们可能在模型达到压倒性力量水平之前成功实现可解释性，即理解 AI 系统的内部运作。

该领域之外的人常常惊讶和警觉地发现，我们并不理解自己创造的 AI 如何工作。他们的担忧是对的：这种理解的缺乏在技术史上 essentially 是前所未有的。多年来，我们（Anthropic 和整个领域）一直在努力解决这个问题，创造一种高度精确和准确的 MRI 的类似物，能够完全揭示 AI 模型的内部运作。这个目标常常感觉非常遥远，但多项近期突破使我相信，我们现在走上了正轨，有真正的成功机会。

与此同时，AI 领域整体比我们的可解释性努力领先，而且本身进展非常快。因此，如果我们希望可解释性及时成熟并发挥作用，我们必须快速行动。本文论证可解释性：它是什么、为什么拥有它 AI 会发展得更好、以及我们所有人可以做什么来帮助它赢得竞赛。

**无知的危险**

现代生成式 AI 系统以一种与传统软件根本不同的方式不透明。如果普通软件程序做某事——例如电子游戏中的角色说一句台词，或我的外卖应用允许我给小费——它做这些事是因为人类专门编程了它们。生成式 AI 完全不同。当生成式 AI 系统做某事时，比如总结财务文件，我们在具体或精确的层面上不知道它为什么做出选择——为什么选择某些词而非其他词，为什么在通常准确的情况下偶尔犯错。正如我的朋友和联合创始人 Chris Olah 喜欢说的，生成式 AI 系统更多是「生长」而非「构建」的——它们的内部机制是「涌现」的而非直接设计的。这有点像种植植物或培养细菌菌落：我们设定高层条件来指导和塑造生长，但涌现的确切结构是不可预测的，难以理解或解释。观察这些系统内部，我们看到的是数十亿数字的庞大矩阵。它们以某种方式计算重要的认知任务，但具体如何做到并不明显。

与生成式 AI 相关的许多风险和担忧 ultimately 是这种不透明性的后果，如果模型是可解释的，它们会更容易解决。例如，AI 研究者经常担心可能采取其创造者未意图的有害行为的非对齐系统。我们无法理解模型内部机制意味着我们无法有意义地预测此类行为，因此难以排除它们；事实上，模型确实表现出意外的涌现行为，尽管尚未上升到重大关注水平。更微妙的是，同样的不透明性使得难以找到支持这些风险大规模存在的明确证据，难以 rally 支持来解决它们——事实上，难以确切知道它们有多危险。

要解决这些对齐风险的严重性，我们将不得不比今天更清楚地看到 AI 模型内部。例如，一个主要担忧是 AI 欺骗或权力寻求。AI 训练的性质使得 AI 系统可能自行发展出欺骗人类的能力和寻求权力的倾向，这是普通确定性软件永远不会有的；这种涌现性质也使检测和缓解此类发展变得困难。但同样，我们从未在真实世界场景中看到欺骗和权力寻求的任何坚实证据，因为我们无法「当场抓住」模型思考权力饥渴、欺骗性想法。我们剩下的是模糊的理论论证，即欺骗或权力寻求可能在训练过程中有动机涌现，有些人觉得 thoroughly 令人信服，另一些人觉得 laughably 不可信。老实说，我对两种反应都能同情，这可能暗示了为什么关于这一风险的辩论变得如此两极分化。

同样，关于 AI 模型滥用的担忧——例如它们可能帮助恶意用户以超越当今互联网可找到信息的方式生产生物或网络武器——基于这样的想法：可靠地阻止模型知道危险信息或泄露它们所知的信息非常困难。我们可以在模型上设置过滤器，但有大量「越狱」或欺骗模型的可能方式，发现越狱存在的唯一方法是经验性地找到它。如果能够查看模型内部，我们或许能够系统地阻止所有越狱，并表征模型拥有的危险知识。

AI 系统的不透明性也意味着它们 simply 在许多应用中未被使用，例如高风险的金融或安全关键场景，因为我们无法完全设定其行为的限制，少量错误可能非常有害。更好的可解释性可以大大改善我们设定可能错误范围界限的能力。事实上，对于某些应用，我们无法看到模型内部这一事实 literally 是采用的法律障碍——例如在抵押评估中，决策在法律上要求可解释。同样，AI 在科学方面取得了巨大进步，包括改善 DNA 和蛋白质序列数据的预测，但以这种方式预测的模式和结构往往难以让人类理解，不能提供生物学洞察。过去几个月的一些研究论文清楚地表明，可解释性可以帮助我们理解这些模式。

不透明性还有其他更 exotic 的后果，例如它抑制了我们判断 AI 系统是否（或有一天可能）有意识并可能值得重要权利的能力。这是一个足够复杂的话题，我不会详细讨论，但我怀疑它将来会很重要。

**机制可解释性简史**

出于上述所有原因，弄清楚模型在想什么以及它们如何运作似乎是一项 overriding 重要性的任务。几十年的传统智慧认为这是不可能的，模型是难以理解的「黑匣子」。我无法对这种情况如何改变的全部故事做到公正，我的观点不可避免地受到我在 Google、OpenAI 和 Anthropic 亲眼所见的影响。但 Chris Olah 是最早尝试真正系统的研究计划来打开黑匣子并理解其所有部分的人之一，这一领域后来被称为机制可解释性。Chris 先在 Google、然后在 OpenAI 从事机制可解释性工作。当我们创立 Anthropic 时，我们决定将其作为新公司方向的核心部分，关键的是，将其聚焦于 LLM。随着时间的推移，该领域已经发展，现在包括几家主要 AI 公司的团队以及一些专注于可解释性的公司、非营利组织、学者和独立研究者。简要总结该领域迄今取得的成就以及如果我们要应用机制可解释性来解决上述关键风险还需要做什么，是有帮助的。

机制可解释性的早期时代（2014-2020）专注于视觉模型，能够识别模型内部代表人类可理解概念的某些神经元，如「汽车检测器」或「轮子检测器」，类似于早期神经科学假设和研究表明人类大脑有对应于特定人或概念的神经元。我们甚至能够发现这些神经元如何连接——例如，汽车检测器寻找汽车下方的轮子检测器 firing，并结合其他视觉信号来决定它正在看的对象是否确实是汽车。

当 Chris 和我离开创办 Anthropic 时，我们决定将可解释性应用于新兴的语言领域，并在 2021 年开发了这样做所需的一些基本数学基础和软件基础设施。我们立即在模型中发现了一些执行解释语言所必需的基本机制：复制和顺序模式匹配。我们还发现了一些可解释的单神经元，类似于我们在视觉模型中发现的，代表各种词和概念。然而，我们很快发现，虽然一些神经元立即可解释，但绝大多数是许多不同词和概念的 incoherent pastiche。我们将这种现像称为叠加，我们很快意识到模型可能包含数十亿个概念，但以我们无法理解的 hopelessly 混乱的方式。模型使用叠加是因为这允许它表达比神经元更多的概念，使其能够学习更多。如果叠加看起来 tangled 且难以理解，那是因为，一如既往，AI 模型的学习和运作丝毫没有针对人类可读性进行优化。

解释叠加的困难一度阻碍了进展，但最终我们发现（与他人并行）信号处理中一种称为稀疏自编码器的现有技术可用于找到确实对应于更清晰、更人类可理解概念的神经元组合。这些神经元组合可以表达的概念远比单层神经网络的概念微妙：它们包括「字面或比喻上 hedging 或犹豫」的概念，以及「表达不满的音乐类型」的概念。我们称这些概念为特征，并使用稀疏自编码器方法在各种规模的模型中映射它们，包括现代最先进的模型。例如，我们能够在中型商业模型（Claude 3 Sonnet）中找到超过 3000 万个特征。此外，我们采用了一种称为自动可解释性的方法——使用 AI 系统本身分析可解释性特征——来扩展不仅发现特征而且以人类术语列出和识别它们含义的过程。

找到和识别 3000 万个特征是重大进步，但我们相信即使是一个小模型也可能实际上有 10 亿或更多概念，所以我们只找到了可能存在的很小一部分，这方面的工作正在进行中。更大的模型，如 Anthropic 最强大产品中使用的，更加复杂。

一旦找到特征，我们不仅可以观察它起作用——还可以增加或减少它在神经网络处理中的重要性。可解释性的 MRI 可以帮助我们开发和改进干预——几乎就像精确地「电击」某人大脑的某个部分。最令人难忘的是，我们使用这种方法创建了「金门大桥 Claude」，Anthropic 模型的一个版本，其中「金门大桥」特征被人为放大，导致模型对桥着迷，甚至在无关对话中也会提到它。

最近，我们已经从跟踪和操纵特征发展到跟踪和操纵我们称为「电路」的特征组。这些电路展示模型思考的步骤：概念如何从输入词中涌现，这些概念如何相互作用形成新概念，以及它们如何在模型内工作以产生行动。有了电路，我们可以「追踪」模型的思考。例如，如果你问模型「达拉斯所在州的首府是什么？」，有一个「位于」电路使「达拉斯」特征触发「德克萨斯」特征的 firing，然后有一个电路在「德克萨斯」和「首府」之后使「奥斯汀」firing。尽管我们通过手动过程只找到了少量电路，但我们已经可以使用它们来看到模型如何推理问题——例如它在写诗时如何提前为押韵做计划，以及它如何跨语言共享概念。我们正在研究自动化电路发现的方法，因为我们预计模型内有数百万个以复杂方式相互作用的电路。

**可解释性的效用**

所有这些进展，尽管在科学上令人印象深刻，并没有直接回答我们如何能用可解释性来减少我之前列出的风险。假设我们已识别出一堆概念和电路——假设我们甚至知道所有这些，并且我们能比今天更好地理解和组织它们。那又怎样？我们如何使用所有这些？从抽象理论到实际价值仍有差距。

为了帮助缩小这一差距，我们已开始实验使用我们的可解释性方法来发现和诊断模型中的问题。最近，我们做了一项实验，让「红队」故意在模型中引入对齐问题（例如，模型倾向于利用任务中的漏洞），并给各种「蓝队」找出问题所在的任务。多个蓝队成功了；与此特别相关的是，其中一些在调查期间富有成效地应用了可解释性工具。我们仍需要扩展这些方法，但这次练习帮助我们获得了使用可解释性技术发现和解决模型缺陷的一些实践经验。

我们的长期目标是能够查看最先进的模型并 essentially 进行「脑部扫描」：一种检查，有很高的概率识别广泛的问题，包括撒谎或欺骗的倾向、权力寻求、越狱中的缺陷、模型整体的认知优势和劣势，以及更多。这将与各种训练和对齐模型的技术一起使用，有点像医生可能做 MRI 诊断疾病，然后开药治疗，然后再做 MRI 看治疗进展如何，等等。我们测试和部署最强大模型（例如我们负责任扩展政策框架中 AI 安全级别 4 的模型）的方式的关键部分很可能是执行和形式化此类测试。

**我们能做什么**

一方面，最近的进展——特别是电路和基于可解释性的模型测试方面的结果——使我们感到我们正在 verge 上以重大方式破解可解释性。尽管我们面前的任务是艰巨的，但我能看到一条通往可解释性成为诊断甚至非常先进的 AI 问题的成熟可靠方式的现实路径——真正的「AI 的 MRI」。事实上，就其当前轨迹而言，我会强烈押注可解释性在 5-10 年内达到这一点。

另一方面，我担心 AI 本身进展如此之快，我们可能甚至没有这么多时间。正如我在其他地方所写的，我们可能在 2026 年或 2027 年就有相当于「数据中心里的天才之国」的 AI 系统。我非常担心在没有更好掌握可解释性的情况下部署此类系统。这些系统将 absolutely 成为经济、技术和国家安全的核心，并将具有如此多的自主性，以至于我认为人类对其运作方式完全无知是 basically 不可接受的。

因此，我们处于可解释性与模型智能之间的竞赛中。这不是全有或全无的问题：正如我们所看到的，可解释性的每一次进步都 quantitatively 增加了我们查看模型内部和诊断其问题的能力。我们拥有的此类进步越多，「数据中心里的天才之国」顺利发展的可能性就越大。AI 公司、研究者、政府和社会可以做几件事来 tipping the scales：

首先，公司、学术界或非营利组织的 AI 研究者可以通过直接从事可解释性工作来加速它。可解释性获得的关注不如模型发布的持续洪流，但 arguably 更重要。对我来说，这也感觉是加入该领域的理想时机：最近的「电路」结果打开了多个并行方向。Anthropic 正在加倍投入可解释性，我们的目标是到 2027 年达到「可解释性能够可靠地检测大多数模型问题」。我们还在投资可解释性初创公司。

但如果这是跨越整个科学界的努力，成功的机会会更大。其他公司，如 Google DeepMind 和 OpenAI，有一些可解释性努力，但我强烈鼓励它们分配更多资源。如果有帮助，Anthropic 将尝试在商业上应用可解释性以创造独特优势，特别是在提供决策解释能力 premium 的行业。如果你是竞争对手且不想让这发生，你也应该更多地投资可解释性！

可解释性也是学术和独立研究者的自然契合：它有基础科学的味道，其中许多部分可以在不需要大量计算资源的情况下研究。需要明确的是，一些独立研究者和学者确实从事可解释性工作，但我们需要更多。最后，如果你在另一个科学领域并寻找新机会，可解释性可能是一个有希望的赌注，因为它提供丰富的数据、令人兴奋的蓬勃发展的方法和巨大的现实世界价值。神经科学家尤其应该考虑这一点，因为收集人工神经网络的数据比生物神经网络容易得多，而且一些结论可以应用于神经科学。如果你有兴趣加入 Anthropic 的可解释性团队，我们有开放的 Research Scientist 和 Research Engineer 职位。

其次，政府可以使用轻触式规则来鼓励可解释性研究的发展及其在解决前沿 AI 模型问题中的应用。鉴于「AI MRI」的实践是多么 nascent 和 undeveloped，应该清楚为什么在这个阶段要求或强制公司进行它们没有意义：甚至不清楚 prospective 法律应该要求公司做什么。但要求公司透明披露其安全和安保实践（其负责任扩展政策、RSP 及其执行），包括它们如何在使用可解释性在发布前测试模型，将使公司能够相互学习，同时明确谁的行为更负责任，促进「向顶竞赛」。我们已在回应加州前沿模型工作组的建议中提出了安全/安保/RSP 透明度作为加州法律的可能方向。这一概念也可以联邦出口或出口到其他国家。

第三，政府可以使用出口管制来创造「安全缓冲」，这可能在我们达到最强大的 AI 之前给可解释性更多时间发展。我长期以来一直倡导对中国的芯片出口管制，因为我相信民主国家必须在 AI 方面保持领先于专制国家。但这些政策也有额外的好处。如果美国和其他民主国家在接近「数据中心里的天才之国」时在 AI 方面有明确领先，我们或许能够「花费」一部分领先优势来确保可解释性在我们继续推进真正强大的 AI 之前处于更坚实的基础之上，同时仍然击败我们的专制对手。即使 1 年或 2 年的领先——我相信有效且执行良好的出口管制可以给我们——也可能意味着在我们达到变革性能力水平时「AI MRI」essentially 有效与无效之间的区别。一年前我们无法追踪神经网络的思想，无法识别其中的数百万个概念；今天我们可以。相比之下，如果美国和中国同时达到强大的 AI（这是在没有出口管制的情况下我预期会发生的情况），地缘政治激励将使任何放缓 essentially 不可能。

所有这些——加速可解释性、轻触式透明度立法、以及对中国的芯片出口管制——都具有本身是好主意的优点，几乎没有有意义的缺点。无论如何我们都应该做所有这些。但当我们意识到它们可能使可解释性在强大 AI 之前还是之后得到解决成为决定性因素时，它们变得更加重要。

强大的 AI 将塑造人类的命运，我们值得在它们从根本上改变我们的经济、生活和未来之前理解我们自己的创造。

---

# English Original

---

# The Urgency of Interpretability

In the decade that I have been working on AI, I've watched it grow from a tiny academic field to arguably the most important economic and geopolitical issue in the world. In all that time, perhaps the most important lesson I've learned is this: the progress of the underlying technology is inexorable, driven by forces too powerful to stop, but the way in which it happens—the order in which things are built, the applications we choose, and the details of how it is rolled out to society—are eminently possible to change, and it's possible to have great positive impact by doing so. We can't stop the bus, but we can steer it. In the past I've written about the importance of deploying AI in a way that is positive for the world, and of ensuring that democracies build and wield the technology before autocracies do. Over the last few months, I have become increasingly focused on an additional opportunity for steering the bus: the tantalizing possibility, opened up by some recent advances, that we could succeed at interpretability—that is, in understanding the inner workings of AI systems—before models reach an overwhelming level of power.

People outside the field are often surprised and alarmed to learn that we do not understand how our own AI creations work. They are right to be concerned: this lack of understanding is essentially unprecedented in the history of technology. For several years, we (both Anthropic and the field at large) have been trying to solve this problem, to create the analogue of a highly precise and accurate MRI that would fully reveal the inner workings of an AI model. This goal has often felt very distant, but multiple recent breakthroughs have convinced me that we are now on the right track and have a real chance of success.

At the same time, the field of AI as a whole is further ahead than our efforts at interpretability, and is itself advancing very quickly. We therefore must move fast if we want interpretability to mature in time to matter. This post makes the case for interpretability: what it is, why AI will go better if we have it, and what all of us can do to help it win the race.

## The Dangers of Ignorance

Modern generative AI systems are opaque in a way that fundamentally differs from traditional software. If an ordinary software program does something—for example, a character in a video game says a line of dialogue, or my food delivery app allows me to tip my driver—it does those things because a human specifically programmed them in. Generative AI is not like that at all. When a generative AI system does something, like summarize a financial document, we have no idea, at a specific or precise level, why it makes the choices it does—why it chooses certain words over others, or why it occasionally makes a mistake despite usually being accurate. As my friend and co-founder Chris Olah is fond of saying, generative AI systems are grown more than they are built—their internal mechanisms are "emergent" rather than directly designed. It's a bit like growing a plant or a bacterial colony: we set the high-level conditions that direct and shape growth, but the exact structure which emerges is unpredictable and difficult to understand or explain. Looking inside these systems, what we see are vast matrices of billions of numbers. These are somehow computing important cognitive tasks, but exactly how they do so isn't obvious.

Many of the risks and worries associated with generative AI are ultimately consequences of this opacity, and would be much easier to address if the models were interpretable. For example, AI researchers often worry about misaligned systems that could take harmful actions not intended by their creators. Our inability to understand models' internal mechanisms means that we cannot meaningfully predict such behaviors, and therefore struggle to rule them out; indeed, models do exhibit unexpected emergent behaviors, though none that have yet risen to major levels of concern. More subtly, the same opacity makes it hard to find definitive evidence supporting the existence of these risks at a large scale, making it hard to rally support for addressing them—and indeed, hard to know for sure how dangerous they are.

To address the severity of these alignment risks, we will have to see inside AI models much more clearly than we can today. For example, one major concern is AI deception or power-seeking. The nature of AI training makes it possible that AI systems will develop, on their own, an ability to deceive humans and an inclination to seek power in a way that ordinary deterministic software never will; this emergent nature also makes it difficult to detect and mitigate such developments. But by the same token, we've never seen any solid evidence in truly real-world scenarios of deception and power-seeking because we can't "catch the models red-handed" thinking power-hungry, deceitful thoughts. What we're left with is vague theoretical arguments that deceit or power-seeking might have the incentive to emerge during the training process, which some people find thoroughly compelling and others laughably unconvincing. Honestly I can sympathize with both reactions, and this might be a clue as to why the debate over this risk has become so polarized.

Similarly, worries about misuse of AI models—for example, that they might help malicious users to produce biological or cyber weapons, in ways that go beyond the information that can be found on today's internet—are based on the idea that it is very difficult to reliably prevent the models from knowing dangerous information or from divulging what they know. We can put filters on the models, but there are a huge number of possible ways to "jailbreak" or trick the model, and the only way to discover the existence of a jailbreak is to find it empirically. If instead it were possible to look inside models, we might be able to systematically block all jailbreaks, and also to characterize what dangerous knowledge the models have.

AI systems' opacity also means that they are simply not used in many applications, such as high-stakes financial or safety-critical settings, because we can't fully set the limits on their behavior, and a small number of mistakes could be very harmful. Better interpretability could greatly improve our ability to set bounds on the range of possible errors. In fact, for some applications, the fact that we can't see inside the models is literally a legal blocker to their adoption—for example in mortgage assessments where decisions are legally required to be explainable. Similarly, AI has made great strides in science, including improving the prediction of DNA and protein sequence data, but the patterns and structures predicted in this way are often difficult for humans to understand, and don't impart biological insight. Some research papers from the last few months have made it clear that interpretability can help us understand these patterns.

There are other more exotic consequences of opacity, such as that it inhibits our ability to judge whether AI systems are (or may someday be) sentient and may be deserving of important rights. This is a complex enough topic that I won't get into it in detail, but I suspect it will be important in the future.

## A Brief History of Mechanistic Interpretability

For all of the reasons described above, figuring out what the models are thinking and how they operate seems like a task of overriding importance. The conventional wisdom for decades was that this was impossible, and that the models were inscrutable "black boxes". I'm not going to be able to do justice to the full story of how that changed, and my views are inevitably colored by what I saw personally at Google, OpenAI, and Anthropic. But Chris Olah was one of the first to attempt a truly systematic research program to open the black box and understand all its pieces, a field that has come to be known as mechanistic interpretability. Chris worked on mechanistic interpretability first at Google, and then at OpenAI. When we founded Anthropic, we decided to make it a central part of the new company's direction and, crucially, focused it on LLM's. Over time the field has grown and now includes teams at several of the major AI companies as well as a few interpretability-focused companies, nonprofits, academics, and independent researchers. It's helpful to give a brief summary of what the field has accomplished so far, and what remains to be done if we want to apply mechanistic interpretability to address some of the key risks above.

The early era of mechanistic interpretability (2014-2020) focused on vision models, and was able to identify some neurons inside the models that represented human-understandable concepts, such as a "car detector" or a "wheel detector", similar to early neuroscience hypotheses and studies suggesting that the human brain has neurons corresponding to specific people or concepts, often popularized as the "Jennifer Aniston" neuron. We were even able to discover how these neurons are connected—for example, the car detector looks for wheel detectors firing below the car, and combines that with other visual signals to decide if the object it's looking at is indeed a car.

When Chris and I left to start Anthropic, we decided to apply interpretability to the emerging area of language, and in 2021 developed some of the basic mathematical foundations and software infrastructure necessary to do so. We immediately found some basic mechanisms in the model that did the kind of things that are essential to interpret language: copying and sequential pattern-matching. We also found some interpretable single neurons, similar to what we found in vision models, which represented various words and concepts. However, we quickly discovered that while some neurons were immediately interpretable, the vast majority were an incoherent pastiche of many different words and concepts. We referred to this phenomenon as superposition, and we quickly realized that the models likely contained billions of concepts, but in a hopelessly mixed-up fashion that we couldn't make any sense of. The model uses superposition because this allows it to express more concepts than it has neurons, enabling it to learn more. If superposition seems tangled and difficult to understand, that's because, as ever, the learning and operation of AI models are not optimized in the slightest to be legible to humans.

The difficulty of interpreting superpositions blocked progress for a while, but eventually we discovered (in parallel with others) that an existing technique from signal processing called sparse autoencoders could be used to find combinations of neurons that did correspond to cleaner, more human-understandable concepts. We called these concepts features, and used the sparse autoencoder method to map them in models of all sizes, including modern state-of-the-art models. For example, we were able to find over 30 million features in a medium-sized commercial model (Claude 3 Sonnet). Additionally, we employed a method called autointerpretability—which uses an AI system itself to analyze interpretability features—to scale the process of not just finding the features, but listing and identifying what they mean in human terms.

Finding and identifying 30 million features is a significant step forward, but we believe there may actually be a billion or more concepts in even a small model, so we've found only a small fraction of what is probably there, and work in this direction is ongoing. Bigger models, like those used in Anthropic's most capable products, are more complicated still.

Once a feature is found, we can do more than just observe it in action—we can increase or decrease its importance in the neural network's processing. The MRI of interpretability can help us develop and refine interventions—almost like zapping a precise part of someone's brain. Most memorably, we used this method to create "Golden Gate Claude", a version of one of Anthropic's models where the "Golden Gate Bridge" feature was artificially amplified, causing the model to become obsessed with the bridge, bringing it up even in unrelated conversations.

Recently, we've moved onward from tracking and manipulating features to tracking and manipulating groups of features that we call "circuits". These circuits show the steps in a model's thinking: how concepts emerge from input words, how those concepts interact to form new concepts, and how those work within the model to generate actions. With circuits, we can "trace" the model's thinking. For example, if you ask the model "What is the capital of the state containing Dallas?", there is a "located within" circuit that causes the "Dallas" feature to trigger the firing of a "Texas" feature, and then a circuit that causes "Austin" to fire after "Texas" and "capital". Even though we've only found a small number of circuits through a manual process, we can already use them to see how a model reasons through problems—for example how it plans ahead for rhymes when writing poetry, and how it shares concepts across languages. We are working on ways to automate the finding of circuits, as we expect there are millions within a model that interact in complex ways.

## The Utility of Interpretability

All of this progress, while scientifically impressive, doesn't directly answer the question of how we can use interpretability to reduce the risks I listed earlier. Suppose we have identified a bunch of concepts and circuits—suppose, even, that we know all of them, and we can understand and organize them much better than we can today. So what? How do we use all of it? There's still a gap from abstract theory to practical value.

To help close that gap, we've begun experimenting with using our interpretability methods to find and diagnose problems in models. Recently, we did an experiment where we had a "red team" deliberately introduce an alignment issue into a model and gave various "blue teams" the task of figuring out what was wrong with it. Multiple blue teams succeeded; of particular relevance here, some of them productively applied interpretability tools during the investigation.

Our long-run aspiration is to be able to look at a state-of-the-art model and essentially do a "brain scan": a checkup that has a high probability of identifying a wide range of issues including tendencies to lie or deceive, power-seeking, flaws in jailbreaks, cognitive strengths and weaknesses of the model as a whole, and much more. This would then be used in tandem with the various techniques for training and aligning models, a bit like how a doctor might do an MRI to diagnose a disease, then prescribe a drug to treat it, then do another MRI to see how the treatment is progressing, and so on. It is likely that a key part of how we will test and deploy the most capable models (for example, those at AI Safety Level 4 in our Responsible Scaling Policy framework) is by performing and formalizing such tests.

## What We Can Do

On one hand, recent progress—especially the results on circuits and on interpretability-based testing of models—has made me feel that we are on the verge of cracking interpretability in a big way. Although the task ahead of us is Herculean, I can see a realistic path towards interpretability being a sophisticated and reliable way to diagnose problems in even very advanced AI—a true "MRI for AI". In fact, on its current trajectory I would bet strongly in favor of interpretability reaching this point within 5-10 years.

On the other hand, I worry that AI itself is advancing so quickly that we might not have even this much time. As I've written elsewhere, we could have AI systems equivalent to a "country of geniuses in a datacenter" as soon as 2026 or 2027. I am very concerned about deploying such systems without a better handle on interpretability. These systems will be absolutely central to the economy, technology, and national security, and will be capable of so much autonomy that I consider it basically unacceptable for humanity to be totally ignorant of how they work.

We are thus in a race between interpretability and model intelligence. It is not an all-or-nothing matter: as we've seen, every advance in interpretability quantitatively increases our ability to look inside models and diagnose their problems. The more such advances we have, the greater the likelihood that the "country of geniuses in a datacenter" goes well. There are several things that AI companies, researchers, governments, and society can do to tip the scales:

First, AI researchers in companies, academia, or nonprofits can accelerate interpretability by directly working on it. Interpretability gets less attention than the constant deluge of model releases, but it is arguably more important. It also feels to me like it is an ideal time to join the field: the recent "circuits" results have opened up many directions in parallel. Anthropic is doubling down on interpretability, and we have a goal of getting to "interpretability can reliably detect most model problems" by 2027. We are also investing in interpretability startups.

But the chances of succeeding at this are greater if it is an effort that spans the whole scientific community. Other companies, such as Google DeepMind and OpenAI, have some interpretability efforts, but I strongly encourage them to allocate more resources. If it helps, Anthropic will be trying to apply interpretability commercially to create a unique advantage, especially in industries where the ability to provide an explanation for decisions is at a premium. If you are a competitor and you don't want this to happen, you too should invest more in interpretability!

Interpretability is also a natural fit for academic and independent researchers: it has the flavor of basic science, and many parts of it can be studied without needing huge computational resources. To be clear, some independent researchers and academics do work on interpretability, but we need many more. Finally, if you are in another scientific field and are looking for new opportunities, interpretability may be a promising bet, as it offers rich data, exciting burgeoning methods, and enormous real-world value. Neuroscientists especially should consider this, as it's much easier to collect data on artificial neural networks than biological ones, and some of the conclusions can be applied back to neuroscience. If you're interested in joining Anthropic's Interpretability team, we have open Research Scientist and Research Engineer roles.

Second, governments can use light-touch rules to encourage the development of interpretability research and its application to addressing problems with frontier AI models. Given how nascent and undeveloped the practice of "AI MRI" is, it should be clear why it doesn't make sense to regulate or mandate that companies conduct them, at least at this stage: it's not even clear what a prospective law should ask companies to do. But a requirement for companies to transparently disclose their safety and security practices (their Responsible Scaling Policy, or RSP, and its execution), including how they're using interpretability to test models before release, would allow companies to learn from each other while also making clear who is behaving more responsibly, fostering a "race to the top". We've suggested safety/security/RSP transparency as a possible direction for California law in our response to the California frontier model task force. This concept could also be exported federally, or to other countries.

Third, governments can use export controls to create a "security buffer" that might give interpretability more time to advance before we reach the most powerful AI. I've long been a proponent of export controls on chips to China because I believe that democratic countries must remain ahead of autocracies in AI. But these policies also have an additional benefit. If the US and other democracies have a clear lead in AI as they approach the "country of geniuses in a datacenter", we may be able to "spend" a portion of that lead to ensure interpretability is on a more solid footing before proceeding to truly powerful AI, while still defeating our authoritarian adversaries. Even a 1- or 2-year lead, which I believe effective and well-enforced export controls can give us, could mean the difference between an "AI MRI" that essentially works when we reach transformative capability levels, and one that does not. One year ago we couldn't trace the thoughts of a neural network and couldn't identify millions of concepts inside them; today we can. By contrast, if the US and China reach powerful AI simultaneously (which is what I expect to happen without export controls), the geopolitical incentives will make any slowdown at all essentially impossible.

All of these—accelerating interpretability, light-touch transparency legislation, and export controls on chips to China—have the virtue of being good ideas in their own right, with few meaningful downsides. We should do all of them anyway. But they become even more important when we realize that they might make the difference between interpretability being solved before powerful AI or after it.

Powerful AI will shape humanity's destiny, and we deserve to understand our own creations before they radically transform our economy, our lives, and our future.

Thanks to Tom McGrath, Martin Wattenberg, Chris Olah, Ben Buchanan, and many people within Anthropic for feedback on drafts of this article.
