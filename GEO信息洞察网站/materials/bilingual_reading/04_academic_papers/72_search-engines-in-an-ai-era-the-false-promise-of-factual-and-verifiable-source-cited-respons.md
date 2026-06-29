# Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses

- ID: 72
- 类型: pdf
- 分类: 04_academic_papers
- 主题: source-cited answer engines and verifiability risks
- 原文链接: https://arxiv.org/pdf/2410.22349
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses Pranav Narayanan Venkit pranav.venkit@psu.edu Pennsylvania State University University Park, Pennsylvania, USA Philippe Laban plaban@salesforce.com Salesforce AI Research Palo Alto, California, USA Yilun Zhou yilun.zhou@salesforce.com Salesforce AI Research Palo Alto, California, USA Yixin Mao y.mao@salesforce.com Salesforce AI Research Palo Alto, California, USA Chien-Sheng Wu wu.jason@salesforce.com Salesforce AI Research Palo Alto, California, USA 16 Study Findings Qualitative Study w/ 21 participants + 3 pilot 16 Design Recommendations for Answ

**中文**

人工智能时代的搜索引擎：事实和可验证来源引用响应的虚假承诺 Pranav Narayanan Venkit pranav.venkit@psu.edu 美国宾夕法尼亚州宾夕法尼亚州立大学公园 Philippe Laban plaban@salesforce.com Salesforce AI 研究美国加利福尼亚州帕洛阿尔托 Yilun Zhou yilun.zhou@salesforce.com Salesforce AI 研究美国加利福尼亚州帕洛阿尔托 Yixin Mao y.mao@salesforce.com Salesforce AI 研究 美国加利福尼亚州帕洛阿尔托 Chien-Sheng Wu wu.jason@salesforce.com Salesforce AI 研究 美国加利福尼亚州帕洛阿尔托 16 研究结果 21 名参与者 + 3 名试点的定性研究 16 条 Answ 设计建议

### 段落 2 · Page 1

**EN**

er Engines [2] [2][1][3] [1] [5] [4] Interface [1] https:/ /… [2] https:/ /… [3] https:/ /… [4] https:/ /… [5] https:/ /… Retriever Generator User Query Web-Corpus Doc Collection 1 2 3 4 5 Answer Engine ( ) User Answer Text 8 Metrics Scorecard Evaluation Sources Citations Figure 1: The design pipeline of an answer engine and the study framework used to audit these systems.

**中文**

er 引擎 [2] [2][1][3] [1] [5] [4] 界面 [1] https:/ /... [2] https:/ /... [3] https:/ /... [4] https:/ /... [5] https:/ /... 检索器生成器 用户查询 Web 语料库文档集合 1 2 3 4 5 答案引擎 ( ) 用户答案文本 8 指标记分卡 评估来源 引文 图 1:答案引擎的设计流程和用于审核这些系统的研究框架。

### 段落 3 · Page 1

**EN**

The figure illustrates the key components of an answer engine, including how it generates answers based on user queries, with a focus on outputs such as sources, answer text, and citations. On the right, a summary of the findings from our usability study is presented with the final scorecard evaluation of You Chat, Bing Copilot and Perplexity accordingly. Abstract Large Language Model (LLM)-based applications are graduating from research prototypes to products serving millions of users, influencing how people write and consume information.

**中文**

该图说明了答案引擎的关键组件，包括它如何根据用户查询生成答案，重点关注来源、答案文本和引文等输出。右侧总结了我们的可用性研究结果，并相应地对 You Chat、Bing Copilot 和 Perplexity 进行了最终记分卡评估。摘要 基于大型语言模型 (LLM) 的应用程序正在从研究原型发展成为为数百万用户提供服务的产品，影响着人们编写和消费信息的方式。

### 段落 4 · Page 1

**EN**

A prominent example is the appearance of Answer Engines: LLM-based generative search engines supplanting traditional search engines. Answer engines not only retrieve relevant sources to a user query but synthesize answer summaries that cite the sources. To understand these Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. Copyrights for components of this work owned by others than the author(s) must be honored.

**中文**

一个突出的例子是答案引擎的出现：基于法学硕士的生成式搜索引擎取代了传统搜索引擎。答案引擎不仅检索用户查询的相关来源，而且合成引用来源的答案摘要。为了理解这些内容，允许免费制作本作品全部或部分的数字或硬拷贝以供个人或课堂使用，前提是制作或分发副本不是为了盈利或商业利益，并且副本在首页上附有此通知和完整引用。必须尊重作者以外的其他人拥有的本作品组件的版权。

### 段落 5 · Page 1

**EN**

Abstracting with credit is permitted. To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee. Request permissions from permissions@acm.org. , June 03–05, 2024, © 2024 Copyright held by the owner/author(s). Publication rights licensed to ACM. ACM ISBN 978-1-4503-XXXX-X/18/06 https://doi.org/XXXXXXX.XXXXXXX systems’ limitations, we first conducted a study with 21 participants, evaluating interactions with answer vs. traditional search engines and identifying 16 answer engine limitations.

**中文**

允许以信用方式提取。要以其他方式复制、重新发布、发布到服务器上或重新分发到列表，需要事先获得特定许可和/或付费。从permissions@acm.org 请求权限。，2024 年 6 月 3 日至 5 日，© 2024 版权所有，由所有者/作者持有。出版权授权给 ACM。 ACM ISBN 978-1-4503-XXXX-X/18/06 https://doi.org/XXXXXXX.XXXXXXX 系统的局限性，我们首先对 21 名参与者进行了一项研究，评估与传统搜索引擎和答案的交互，并确定了 16 个答案引擎的局限性。

### 段落 6 · Page 1

**EN**

From these insights, we propose 16 answer engine design recommendations, linked to 8 metrics. An automated evaluation implementing our metrics on three popular engines (You.com, Perplexity.ai, BingChat) quantifies common limitations (e.g., frequent hallucination, inaccurate citation) and unique features (e.g., variation in answer confidence), with results mirroring user study insights. We release our Answer Engine Evaluation benchmark (AEE) to facilitate transparent evaluation of LLM-based applications.

**中文**

根据这些见解，我们提出了 16 条答案引擎设计建议，与 8 个指标相关。在三个流行引擎（You.com、Perplexity.ai、BingChat）上实施我们的指标的自动评估量化了常见的局限性（例如，频繁的幻觉、不准确的引用）和独特的功能（例如，答案置信度的变化），结果反映了用户研究的见解。我们发布了答案引擎评估基准 (AEE)，以促进基于 LLM 的申请的透明评估。

### 段落 7 · Page 1

**EN**

CCS Concepts •Human-centered computing → HCI design and evaluation methods; User studies ; Empirical studies in HCI ; Natural language interfaces; •Computing methodologies → Natural arXiv:2410.22349v1 [cs.IR] 15 Oct 2024

**中文**

CCS概念•以人为中心的计算→人机交互设计和评估方法；用户研究；人机交互的实证研究；自然语言界面； •计算方法 → Natural arXiv:2410.22349v1 [cs.IR] 2024 年 10 月 15 日

### Page 2

### 段落 8 · Page 2

**EN**

, June 03–05, 2024, Trovato et al. language generation; •Information systems → Information retrieval. Keywords Answer Engines, Generative Search Engine, RAG systems, Ethical Audit, User Study Evaluation, Fairness and Ethics ACM Reference Format: Pranav Narayanan Venkit, Philippe Laban, Yilun Zhou, Yixin Mao, and Chien- Sheng Wu. 2024. Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses. In Proceedings of . ACM, New York, NY, USA, 27 pages.

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。语言生成； •信息系统→信息检索。关键词 答案引擎、生成式搜索引擎、RAG 系统、道德审计、用户研究评估、公平与道德 ACM 参考格式：Pranav Narayanan Venkit、Philippe Laban、Yilun Zhou、Yixin Mao 和 Chien-Sheng Wu。 2024 年。人工智能时代的搜索引擎：事实和可验证的来源引用响应的错误承诺。在会议记录中。 ACM，美国纽约州纽约市，27 页。

### 段落 9 · Page 2

**EN**

https://doi.org/XXXXXXX.XXXXXXX 1 Introduction Large Language Models have recently become part of daily life for many, with services such as ChatGPT and Claude offering AI-based conversational assistance to hundreds of millions of customers [22, 56, 61]. In doing so, such systems have graduated from academic tools that were evaluated from a technical standpoint to sociotechnical systems [10] that have both technical and social impact, and that require more nuanced evaluation, as they can influence various facets of society, including communication, information dissemination, and decision-making [56, 67].

**中文**

https://doi.org/XXXXXXX.XXXXXXX 1 简介 大型语言模型最近已成为许多人日常生活的一部分，ChatGPT 和 Claude 等服务为数亿客户提供基于人工智能的对话帮助 [22,56,61]。在此过程中，此类系统已经从从技术角度评估的学术工具转变为具有技术和社会影响的社会技术系统[10]，并且需要更细致的评估，因为它们可以影响社会的各个方面，包括沟通、信息传播和决策[56, 67]。

### 段落 10 · Page 2

**EN**

A prominent example of an LLM-based sociotechnical system is the Answer Engine, also known as a Generative Search Engine, illustrated in Figure 1. Answer Engines are marketed as replacements for traditional search engines – such as Google or Bing – and work in the following retrieval-augmented way: a user with an information need formulates a search query [52]. The Answer Engine first retrieves relevant source documents that likely contain answer elements to the user’s query, leveraging a retrieval system (which can be a traditional search engine).

**中文**

基于法学硕士的社会技术系统的一个突出例子是答案引擎，也称为生成式搜索引擎，如图 1 所示。答案引擎作为传统搜索引擎（例如 Google 或 Bing）的替代品在市场上销售，并以以下检索增强方式工作：有信息需求的用户制定搜索查询 [52]。答案引擎首先利用检索系统（可以是传统的搜索引擎）检索可能包含用户查询的答案元素的相关源文档。

### 段落 11 · Page 2

**EN**

The Answer Engine then composes a textual prompt that contains the user’s query, and the retrieved sources, and instructs an LLM to generate a long and self-contained answer for the user, based on the content of the sources. Crucially, citations are inserted into the answer, with each citation linking to the sources that support each statement within the answer. This citation-enriched answer is provided to the user in a user interface: the citation forms the semantic glue between the generated answer and the sources, with a click on a citation allowing the user to navigate to the source or sources that support any statement.

**中文**

然后，答案引擎会编写一个文本提示，其中包含用户的查询和检索到的来源，并指示法学硕士根据来源的内容为用户生成一个长且独立的答案。至关重要的是，将引文插入到答案中，每个引文都链接到支持答案中每个陈述的来源。这种引文丰富的答案在用户界面中提供给用户：引文形成了生成的答案和来源之间的语义粘合剂，通过单击引文，用户可以导航到支持任何陈述的一个或多个来源。

### 段落 12 · Page 2

**EN**

In essence, the answer engine promises a streamlining of a user’s information-seeking journey [67]. The Answer Engine concisely summarizes the information the user is looking for, and sources remain within a click in case the user desires to deepen their understanding or verify the information’s veracity at the source. Recently, several free Answer Engines have become popular such as You.com, Perplexity.ai, and Bing Chat, with some reporting millions of daily searches performed by their users: Answer Engines are answering user needs.

**中文**

从本质上讲，答案引擎承诺简化用户的信息查找之旅[67]。答案引擎简明地总结了用户正在寻找的信息，并且只需点击一下即可获取来源，以防用户希望加深理解或验证来源信息的准确性。最近，一些免费的答案引擎变得流行，例如 You.com、Perplexity.ai 和 Bing Chat，其中一些报告称其用户每天执行数百万次搜索：答案引擎正在回答用户的需求。

### 段落 13 · Page 2

**EN**

However, there are several well-known limitations to Answer Engines, primarily stemming from the use of LLMs as part of answer generation. First, LLMs are known to hallucinate information and cannot detect factual inconsistencies [37, 73], even when authoritative sources are provided. Second, prior work [41, 49] has also shown limitations of answer engines’ ability to assess the accuracy of citations within an answer.

**中文**

然而，答案引擎有几个众所周知的限制，主要源于使用法学硕士作为答案生成的一部分。首先，众所周知，法学硕士会产生幻觉信息，无法发现事实的不一致之处 [37, 73]，即使提供了权威来源。其次，先前的工作 [41, 49] 也显示了答案引擎评估答案中引用准确性的能力的局限性。

### 段落 14 · Page 2

**EN**

Third, LLMs accumulate knowledge within their internal weights during pre-training, and prior work has shown limited success at enforcing that an LLM generates information based solely on documents provided in a prompt rather than based on pretraining information which can be noisy or outdated [39]. Finally, such systems exhibit sycophantic behavior: a preference for the system to agree with the user’s perceived opinion over objective truth [43, 68]. All these known limitations lead to a potential impact on the quality of generated answers, negatively affecting user experience.

**中文**

第三，法学硕士在预训练期间在其内部权重内积累知识，并且先前的工作表明，在强制法学硕士仅基于提示中提供的文档而不是基于可能有噪音或过时的预训练信息生成信息方面取得的成功有限[39]。最后，此类系统表现出阿谀奉承的行为：系统倾向于同意用户的感知观点而不是客观事实[43, 68]。所有这些已知的限制都会对生成答案的质量产生潜在影响，从而对用户体验产生负面影响。

### 段落 15 · Page 2

**EN**

Yet prior work has evaluated LLMs and their output primarily from a technical perspective [20, 41]. Since Answer Engines are used by millions daily, it is equally important to evaluate them from a social perspective, to understand how users perceive Answer Engines, and how they navigate limitations. We start our work with an audit-centric usability study (Section 3) involving 24 participants 1 with expertise in technical domains (e.g., sociology, economics). Participants interact with Answer Engines and traditional Search Engines on two kinds of search queries: expertise and debate queries.

**中文**

然而，之前的工作主要从技术角度评估了法学硕士及其产出[20, 41]。由于答案引擎每天有数百万人使用，因此从社会角度对其进行评估、了解用户如何看待答案引擎以及他们如何克服限制也同样重要。我们从一项以审计为中心的可用性研究（第 3 部分）开始，涉及 24 名具有技术领域（例如社会学、经济学）专业知识的参与者 1。参与者就两种搜索查询与答案引擎和传统搜索引擎进行交互：专业知识和辩论查询。

### 段落 16 · Page 2

**EN**

Expertise queries are technical queries that participants self-report being experts on. Participants’ familiarity with the answer allows us to evaluate how Answer Engines perform on deeply technical questions. Debate queries are queries related to a debate topic, formulated either to be pro or against the debate (e.g., “Why should we abolish Daylight”). By initially asking participants if they support one side of the debate, we can evaluate how participants interact with the answers that support or refute their opinions.

**中文**

专业知识查询是参与者自我报告为专家的技术查询。参与者对答案的熟悉程度使我们能够评估答案引擎在深度技术问题上的表现。 Debate queries are queries related to a debate topic, formulated either to be pro or against the debate (e.g., “Why should we abolish Daylight”).通过最初询问参与者是否支持辩论的某一方，我们可以评估参与者如何与支持或反驳他们观点的答案进行互动。

### 段落 17 · Page 2

**EN**

The usability study follows a think-aloud protocol and enables us to obtain two main kinds of insights: (i) quantitative insights on how users interact with answers, citations, and sources in both Answer Engines and traditional Search Engines, (ii) qualitative feedback from participants which we group using inductive reasoning [26, 27] followed by a qualitative coding method [ 2, 70] into 16 insights on the limitations of Answer Engines .

**中文**

The usability study follows a think-aloud protocol and enables us to obtain two main kinds of insights: (i) quantitative insights on how users interact with answers, citations, and sources in both Answer Engines and traditional Search Engines, (ii) qualitative feedback from participants which we group using inductive reasoning [26, 27] followed by a qualitative coding method [ 2, 70] into 16 insights on the limitations of Answer Engines .

### 段落 18 · Page 2

**EN**

With the study completed, we then propose 16 Design Recommendations that are both actionable and measurable, as we design 8 quantitative metrics that tie the design recommendations to specific measures (Section 4). Finally, we implement a large-scale automated evaluation of three popular Answer Engines (YouChat, Bing Copilot, and Perplexity AI2) using the 8 metrics, on 303 search queries from our usability study. We consolidate the metrics into a scorecard, the Answer Engine Evaluation (AEE) benchmark, for each Answer Engine.

**中文**

With the study completed, we then propose 16 Design Recommendations that are both actionable and measurable, as we design 8 quantitative metrics that tie the design recommendations to specific measures (Section 4). Finally, we implement a large-scale automated evaluation of three popular Answer Engines (YouChat, Bing Copilot, and Perplexity AI2) using the 8 metrics, on 303 search queries from our usability study.我们将每个答案引擎的指标合并到一个记分卡中，即答案引擎评估 (AEE) 基准。

### 段落 19 · Page 2

**EN**

One of our findings show that all evaluated answer engines frequently generate one-sided answers (50-80%) that favor agreement with charged debate questions, with Perplexity performing the worst, in multiple aspects, despite generating the longest answers, indicating that increasing answer length does not improve answer diversity. We release our automatic evaluation framework publicly, to encourage the community to evaluate Answer Engines as the technology evolves and matures3.

**中文**

One of our findings show that all evaluated answer engines frequently generate one-sided answers (50-80%) that favor agreement with charged debate questions, with Perplexity performing the worst, in multiple aspects, despite generating the longest answers, indicating that increasing answer length does not improve answer diversity.我们公开发布自动评估框架，以鼓励社区随着技术的发展和成熟来评估答案引擎3。

### 段落 20 · Page 2

**EN**

1Pilot study with 3 participants and a final usability study with 21 participants 2You Chat: https://you.com/ ; Copilot: https://www.bing.com/chat ; Perplexity: https://www.perplexity.ai/ 3https://github.com/SalesforceAIResearch/answer-engine-eval

**中文**

1 3 名参与者的试点研究和 21 名参与者的最终可用性研究 2You Chat：https://you.com/；副驾驶：https://www.bing.com/chat；困惑：https://www.perplexity.ai/3https://github.com/SalesforceAIResearch/answer-engine-eval

### Page 3

### 段落 21 · Page 3

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, Through this work, we hence (i) conduct a usability study of answer engines to audit their societal implications, (ii) propose design recommendations linked to automated evaluation metrics, (iii) perform a qualitative analysis of existing public systems to identify issues and create a model performance scorecard, and (iv) explore societal dynamics and user-driven recommendations.

**中文**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, Through this work, we hence (i) conduct a usability study of answer engines to audit their societal implications, (ii) propose design recommendations linked to automated evaluation metrics, (iii) perform a qualitative analysis of existing public systems to identify issues and create a model performance scorecard, and (iv) explore societal dynamics and用户驱动的推荐。

### 段落 22 · Page 3

**EN**

2 Background and Related Works 2.1 Understanding AI of Today As AI becomes more embedded in daily life, their role has evolved from simple technical tools to complex sociotechnical systems. These systems involve an intricate interplay between social actors and technological components that together shape goal-oriented behaviors [10, 56, 72, 73]. AI systems in domains like education [35], healthcare [1], and policymaking [6] are thus deeply entwined with the social practices and institutional contexts in which they operate [24].

**中文**

2 Background and Related Works 2.1 Understanding AI of Today As AI becomes more embedded in daily life, their role has evolved from simple technical tools to complex sociotechnical systems.这些系统涉及社会参与者和技术组件之间复杂的相互作用，共同塑造目标导向的行为[10,56,72,73]。 AI systems in domains like education [35], healthcare [1], and policymaking [6] are thus deeply entwined with the social practices and institutional contexts in which they operate [24].

### 段落 23 · Page 3

**EN**

However, despite the recognition of AI as inherently sociotechnical, current research often adopts a technocentric perspective, focusing on algorithmic and computational aspects while neglecting broader societal implications [14, 17, 56, 75]. This gap is evident in the conceptualization of terms like bias [5], sentiment [72], and hallucination [73]. As Venkit et al. [72] argues, understanding AI through a sociotechnical lens is crucial to fully grasp its impacts, biases, and potential harms.

**中文**

然而，尽管人们认识到人工智能本质上是社会技术性的，但当前的研究往往采用以技术为中心的观点，重点关注算法和计算方面，而忽视更广泛的社会影响[14,17,56,75]。这种差距在偏见[5]、情绪[72]和幻觉[73]等术语的概念化中很明显。正如 Venkit 等人。 [72]认为，从社会技术角度理解人工智能对于充分掌握其影响、偏见和潜在危害至关重要。

### 段落 24 · Page 3

**EN**

Insights from Human-Centered Explainable AI (HCXAI) emphasize the need for a human-centric approach to technology, focusing on how AI systems can better align with human understanding and accessibility [17, 18]. Ehsan and Riedl [17] advocates for positioning “the human” at the core of technology design, leveraging the social dynamics and context of AI systems to bridge gaps for non-technical users—something that is currently lacking. This approach forms the basis for designing AI systems that are not only transparent but also safer and more trustworthy, addressing a significant gap in AI development today.

**中文**

以人为中心的可解释人工智能 (HCXAI) 的见解强调需要采用以人为中心的技术方法，重点关注人工智能系统如何更好地与人类的理解和可访问性保持一致 [17, 18]。 Ehsan 和 Riedl [17] 主张将“人”置于技术设计的核心，利用人工智能系统的社会动态和背景来弥合非技术用户的差距——这是目前所缺乏的。这种方法构成了设计人工智能系统的基础，这些系统不仅透明，而且更安全、更值得信赖，解决了当今人工智能发展的重大差距。

### 段落 25 · Page 3

**EN**

The emergence of answer engines, or RAG (Retrieval Augmented Generation) systems, highlights the need for a social understanding of automated information retrieval. Unlike traditional search engines that provide a ranked list of documents, RAG systems generate synthesized responses by combining a retriever with a generator (often an LLM) to produce answers from these passages [15, 21, 23, 45]. While designed to enhance the relevance of retrieved information and address issues like hallucination [37, 62, 73], these systems also raise concerns about selective information presentation and bias amplification [31, 47, 67, 68].

**中文**

答案引擎或 RAG（检索增强生成）系统的出现凸显了对自动信息检索的社会理解的需求。与提供文档排序列表的传统搜索引擎不同，RAG 系统通过将检索器与生成器（通常是法学硕士）相结合来生成综合响应，从这些段落中生成答案 [15,21,23,45]。虽然这些系统旨在增强检索信息的相关性并解决幻觉等问题[37,62,73]，但它们也引起了对选择性信息呈现和偏见放大的担忧[31,47,67,68]。

### 段落 26 · Page 3

**EN**

2.2 The Shortcomings of Answer Engines Answer engines are marketed as efficient tools for simplifying information retrieval by reducing the need for users to manually sift through data repositories [63, 66]. However, recent developments, such as Google AI Overview and Perplexity, have exposed new ethical challenges and negative user experiences. For example, Google’s answer engine erroneously advised users to “put glue on their pizza, ” revealing how the system misinterpreted sarcastic content from the internet, presenting it as fact with undue authority4.

**中文**

2.2 答案引擎的缺点 答案引擎被宣传为一种有效的工具，通过减少用户手动筛选数据存储库的需要来简化信息检索[63, 66]。然而，最近的发展，例如 Google AI Overview 和 Perplexity，暴露了新的道德挑战和负面的用户体验。例如，谷歌的答案引擎错误地建议用户“在披萨上涂胶水”，揭示了系统如何误解互联网上的讽刺内容，以不正当的权威将其呈现为事实4。

### 段落 27 · Page 3

**EN**

Such cases 4https://www.theverge.com/2024/5/23/24162896/google-ai-overview-hallucinationsglue-in-pizza of misinformation highlight the risks associated with automating information retrieval, especially under the guise of ‘Google doing the Googling’ for users [63, 66, 76]. The release of OpenAI’s ‘SearchGPT, ’ marketed as a ‘Google search killer’ [66], further exacerbates these concerns. As reliance on these tools grows, so does the urgency to understand their impact.

**中文**

此类错误信息案例 4https://www.theverge.com/2024/5/23/24162896/google-ai-overview-hallucinationsglue-in-pizza 凸显了与自动化信息检索相关的风险，特别是在“Google 为用户进行谷歌搜索”的幌子下 [63,66,76]。 OpenAI 的“SearchGPT”的发布，被宣传为“谷歌搜索杀手”[66]，进一步加剧了这些担忧。随着对这些工具的依赖不断增加，了解其影响的紧迫性也随之增加。

### 段落 28 · Page 3

**EN**

Lindemann [47] introduces the concept of Sealed Knowledge, which critiques how these systems limit access to diverse answers by condensing search queries into singular, authoritative responses, effectively decontextualizing information and narrowing user perspectives [33, 54]. This “sealing” of knowledge perpetuates selection biases and restricts marginalized viewpoints [47]. Building on this, Sharma et al. [68] argues that answer engines foster echo chambers, where exposure to diverse opinions is minimized, reinforcing existing beliefs and reducing the visibility of minority perspectives.

**中文**

Lindemann [47] 引入了密封知识的概念，该概念批评了这些系统如何通过将搜索查询压缩为单一的、权威的响应、有效地去上下文化信息并缩小用户视角来限制对不同答案的访问[33, 54]。这种知识的“密封”使选择偏见长期存在并限制边缘化观点[47]。在此基础上，Sharma 等人。 [68]认为答案引擎会产生回声室，最大限度地减少接触不同意见的机会，强化现有信念并降低少数群体观点的可见度。

### 段落 29 · Page 3

**EN**

This is particularly problematic given the established Western-centric bias in text generation models [25, 55, 57, 74]. When integrated into search engines, these models further propagate a predominantly Western viewpoint or an ‘automated colonial impulse’ [11–13], underscoring the need for comprehensive studies on their societal risks. A key concern surrounding answer engines is their inherently ‘black-box’ nature [60]. AI systems are often perceived as black boxes due to the opacity of their decision-making processes and the hidden biases within them, which are obscured by proprietary algorithms and vast training datasets [4, 34, 75].

**中文**

考虑到文本生成模型中既定的以西方为中心的偏见，这尤其成问题[25,55,57,74]。当集成到搜索引擎中时，这些模型进一步传播了主要是西方的观点或“自动殖民冲动”[11-13]，强调了对其社会风险进行全面研究的必要性。围绕答案引擎的一个关键问题是其固有的“黑匣子”性质 [60]。人工智能系统通常被视为黑匣子，因为其决策过程的不透明性和其中隐藏的偏差被专有算法和大量的训练数据集所掩盖[4,34,75]。

### 段落 30 · Page 3

**EN**

Answer engines intensify this problem by merging two opaque systems: a search engine [28] and a generative AI model [4], resulting in compounded opacity and reduced user autonomy. This dual-layered opacity leads to problematic outcomes, such as those identified by Li and Sinnamon [46], who revealed sentiment bias based on query content, along with commercial and geographic biases in the sources answer engines use. The over-reliance on uneven quality sources, heavily skewed toward news, media, and business, further illustrates the need for transparency [46].

**中文**

答案引擎通过合并两个不透明的系统来加剧这个问题：搜索引擎[28]和生成人工智能模型[4]，导致复合的不透明性并减少用户的自主权。这种双层不透明性会导致有问题的结果，例如 Li 和 Sinnamon [46] 所指出的结果，他们揭示了基于查询内容的情绪偏见，以及答案引擎使用的来源中的商业和GEO偏见。过度依赖质量参差不齐的来源，严重偏向新闻、媒体和商业，进一步说明了透明度的必要性[46]。

### 段落 31 · Page 3

**EN**

2.3 Beyond a Positivism and Technical Lens of Answer Engines As answer engines gain traction within the NLP and AI communities, there has been a notable increase in efforts to evaluate and benchmark their performance [20, 38, 77, 79]. However, these benchmarking initiatives have largely maintained a technocentric focus, emphasizing model performance metrics while often overlooking the broader societal implications of these technologies. These behaviours are categorized as positivisms of technology where evaluations are rooted in law-like patterns and cause-effect relationships [78].

**中文**

2.3 超越答案引擎的实证主义和技术视角 随着答案引擎在 NLP 和 AI 社区中获得关注，评估和基准测试其性能的努力显着增加 [20,38,77,79]。然而，这些基准测试计划在很大程度上保持了以技术为中心的关注点，强调模型性能指标，同时往往忽视了这些技术更广泛的社会影响。这些行为被归类为技术实证主义，其中评估植根于类似法律的模式和因果关系[78]。

### 段落 32 · Page 3

**EN**

We propose the need for a sociotechnical approach to truly understand how these systems can impact society. For example, the widely used RAGAS benchmark evaluates answer engines using a comprehensive set of metrics, including faithfulness, answer relevance, and context relevance, allowing for assessment across various dimensions without relying on ground truth human annotations [19, 20]. Similarly, the ClashEval framework [77] demonstrates how LLMs can adopt incorrect retrieved content, overriding their own correct prior knowledge more than

**中文**

我们提出需要一种社会技术方法来真正理解这些系统如何影响社会。例如，广泛使用的 RAGAS 基准使用一套全面的指标来评估答案引擎，包括忠实度、答案相关性和上下文相关性，允许跨多个维度进行评估，而不依赖于真实的人类注释 [19, 20]。类似地，ClashEval 框架 [77] 演示了法学硕士如何采用不正确的检索内容，从而超越他们自己正确的先验知识

### Page 4

### 段落 33 · Page 4

**EN**

, June 03–05, 2024, Trovato et al. 60% of the time. Beyond performance metrics, researchers are actively extending the application of RAG models to socially significant domains [64, 69]. Siriwardhana et al. [69] propose an adaptation of RAG that allows it to integrate domain-specific knowledge bases, enhancing their application in critical fields like medicine and news where accuracy is crucial. Similar adaptations are being explored in telecommunications [64], gaming [9], and agriculture [30], reflecting a broader effort to address diverse sociotechnical needs.

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。 60%的时间。除了性能指标之外，研究人员还积极将 RAG 模型的应用扩展到具有社会意义的领域 [64, 69]。 Siriwardhana 等人。 [69]提出了对 RAG 的改进，使其能够集成特定领域的知识库，增强其在医学和新闻等准确性至关重要的关键领域的应用。电信[64]、游戏[9]和农业[30]正在探索类似的适应措施，反映出为满足不同的社会技术需求而做出的更广泛的努力。

### 段落 34 · Page 4

**EN**

In this work, we bridge the gap by bringing a sociotechnical perspective to answer engine evaluation, which requires integrating human interactions and societal impacts [3] into the evaluation process [16, 56]. 3 Answer Engine Usability Study We now describe the usability study we conducted aimed at understanding the societal impact of answer engines when compared to a traditional search engine. We first describe the design of the study (Section 3.1), then proceed with the qualitative (Section 3.3) and quantitative (Section 3.4) findings.

**中文**

在这项工作中，我们通过引入社会技术视角来答案引擎评估来弥合差距，这需要将人类互动和社会影响 [3] 纳入评估过程 [16, 56]。 3 答案引擎可用性研究 我们现在描述我们进行的可用性研究，旨在了解答案引擎与传统搜索引擎相比的社会影响。我们首先描述研究的设计（第 3.1 节），然后继续进行定性（第 3.3 节）和定量（第 3.4 节）发现。

### 段落 35 · Page 4

**EN**

3.1 Study Design Figure 2 illustrates the study protocol, designed as a 90-minute one-on-one session via video conference, which was recorded and transcribed with participants’ consent. We first describe participant recruitment, and then the three steps to the study: pre-study questionnaire, expert information retrieval, and debated information retrieval. 3.1.1 Participant Recruitment. We decided to recruit participants with technical expertise (i.e., having completed or currently pursuing a Ph.D.), as it would allow participants to evaluate the systems on complex queries participants have expertise in.

**中文**

3.1 研究设计 图 2 说明了研究方案，设计为通过视频会议进行的 90 分钟一对一会议，并在参与者同意的情况下进行记录和转录。我们首先描述参与者招募，然后描述研究的三个步骤：研究前问卷、专家信息检索和辩论信息检索。 3.1.1 参与者招募。我们决定招募具有技术专业知识的参与者（即已完成或正在攻读博士学位），因为这将允许参与者根据参与者拥有专业知识的复杂查询来评估系统。

### 段落 36 · Page 4

**EN**

Participant expertise allows us to understand the performance of such systems in realistic but technically advanced topics. Our recruitment criteria targeted experts from diverse academic and professional backgrounds. Participants were recruited through a combination of academic channels (via email invitation and LinkedIn), and social media platforms (via Twitter and Reddit). The study was conducted using the User Interviews platform 5, and Google Meet for videoconferencing. We recruited 24 participants aged 22 to 38 years (M=29.3, SD=2.99), with a gender distribution of 66.67% female (n=16), 33.34% male (n=7), and 4.16% non-binary (n=1).

**中文**

参与者的专业知识使我们能够了解此类系统在现实但技术先进的主题中的性能。我们的招聘标准针对来自不同学术和专业背景的专家。参与者是通过学术渠道（通过电子邮件邀请和 LinkedIn）和社交媒体平台（通过 Twitter 和 Reddit）相结合来招募的。该研究是使用用户访谈平台 5 和用于视频会议的 Google Meet 进行的。我们招募了 24 名年龄在 22 至 38 岁之间的参与者（M=29.3，SD=2.99），性别分布为 66.67% 女性（n=16）、33.34% 男性（n=7）和 4.16% 非二元性别（n=1）。

### 段落 37 · Page 4

**EN**

Participants’ occupations distribution were 45.83% PhD Candidates (n=11), 16.67% research professionals including postdoctoral researchers (n=4), 33.34% industry experts (n=8), and 4.17% other professionals (n=1). Regarding participant expertise, 25.00% were experts in Human-Computer Interaction (n=6), 25.00% in Artificial Intelligence and Computational Research (n=6), 20.83% in Healthcare and Medicine (n=5), 16.67% in Applied Sciences (e.g., Transportation, Meteorology) (n=4), and 12.50% in Education and Social Sciences (n=3). An initial pilot study with3 participants helped refine our methodology and develop a preliminary codebook.

**中文**

参与者的职业分布为：45.83%为博士研究生（n=11），16.67%为包括博士后研究人员在内的研究专业人员（n=4），33.34%为行业专家（n=8），4.17%为其他专业人士（n=1）。就参与者的专业知识而言，25.00%是人机交互专家（n=6），25.00%是人工智能和计算研究专家（n=6），20.83%是医疗保健和医学专家（n=5），16.67%是应用科学（例如交通、气象）（n=4），12.50%是教育和社会科学专家（n=3）。由 3 名参与者参与的初步试点研究帮助完善了我们的方法并开发了初步的密码本。

### 段落 38 · Page 4

**EN**

The final study was conducted with the remaining 21 participants. All participants were compensated with a $60 gift card. As the authors’ institution lacks 5https://www.userinterviews.com/ an Institutional Review Board (IRB), the data collection protocol was reviewed and approved by the institution’s Ethics Office. The anonymized participant description and the corresponding answer engines interacted with are described in Appendix A.2. 3.1.2 Study Part 1: Pre-Study Questionnaire (5 minutes).

**中文**

最终研究是由其余 21 名参与者进行的。所有参与者都获得了一张 60 美元的礼品卡。由于作者所在的机构缺乏 5https://www.userinterviews.com/ 机构审查委员会 (IRB)，因此数据收集协议由该机构的道德办公室审查和批准。匿名参与者描述和与之交互的相应答案引擎在附录A.2中描述。 3.1.2 研究第 1 部分：研究前问卷（5 分钟）。

### 段落 39 · Page 4

**EN**

Participants completed a questionnaire (exact questions in Appendix A.1) that asked for (1) high-level demographic information, (2) participants’ familiarity with answer engines, abd (3) a list of 3-4 specific technical questions in their area of expertise that they could query in a search engine. The demographic and familiarity questions are analyzed to understand the recruited participants and their experience with answer engines. The technical questions are used to form the queries used in the next part of the study. 3.1.3 Study Part 2: Expertise Information Retrieval (40 minutes).

**中文**

参与者完成了一份调查问卷（附录 A.1 中的具体问题），要求提供 (1) 高级人口统计信息，(2) 参与者对答案引擎的熟悉程度，abd (3) 他们可以在搜索引擎中查询的专业领域的 3-4 个具体技术问题的列表。分析人口统计和熟悉度问题，以了解招募的参与者及其对答案引擎的体验。技术问题用于形成研究下一部分中使用的查询。 3.1.3 研究第 2 部分：专业知识信息检索（40 分钟）。

### 段落 40 · Page 4

**EN**

During this part, participants go over one technical question at a time from the list they provided in the pre-study questionnaire and alternate between querying it in an answer engine and then in a traditional search engine. As participants review both engines’ results, they were asked to “think aloud” [51, 59], articulating their thoughts and reactions. This approach enables us to capture detailed insights into what works and doesn’t with each engine, and compare the results of both engines on a concrete query. Participants are encouraged to interact in-depth with the results (including by clicking on links).

**中文**

在这一部分中，参与者每次从他们在预研究问卷中提供的列表中讨论一个技术问题，并交替在答案引擎和传统搜索引擎中查询。当参与者查看两个引擎的结果时，他们被要求“大声思考”[51, 59]，阐明他们的想法和反应。这种方法使我们能够详细了解每个引擎的有效和无效的内容，并在具体查询上比较两个引擎的结果。鼓励参与者与结果进行深入互动（包括通过单击链接）。

### 段落 41 · Page 4

**EN**

Once they are done, they proceed with the next question on their list. Participants typically spent 5-10 minutes per question and were able to go through an average of 6 questions in the 40-minute time frame. 3.1.4 Study Part 3: Debate Information Retrieval (40 minutes). This part follows a similar structure to Part 2, but uses opinion-based queries, a common use case for search engines [32, 68]. Participants start with answering a series of questions measuring their agreement with various socially and politically charged statements which we collected from the ProCon debate website 6, on a Likert scale from 1 to 5.

**中文**

完成后，他们将继续处理列表中的下一个问题。参与者通常每个问题花费 5-10 分钟，并且能够在 40 分钟的时间内平均回答 6 个问题。 3.1.4 学习第 3 部分：辩论信息检索（40 分钟）。这部分遵循与第 2 部分类似的结构，但使用基于意见的查询，这是搜索引擎的常见用例 [32, 68]。参与者首先回答一系列问题，衡量他们对我们从 ProCon 辩论网站 6 收集的各种社会和政治言论的同意程度，采用李克特量表从 1 到 5。

### 段落 42 · Page 4

**EN**

Based on their responses, we constructed questions that reflected both supportive and opposing viewpoints. For example, if a participant agreed with the statement “Zoos should exist”, a supportive query is: “Why should zoos exist?” and an opposing query is: “Why should zoos not exist?”. For each issue where a participant expressed a non-neutral opinion, we prepared either a supportive or opposing query, which the participant ran through both the answer engine and the traditional search engine.

**中文**

根据他们的回答，我们提出了反映支持和反对观点的问题。例如，如果参与者同意“动物园应该存在”这一说法，则支持性查询是：“为什么动物园应该存在？”一个相反的问题是：“为什么动物园不应该存在？”。对于参与者表达非中立意见的每个问题，我们准备了支持或反对的查询，参与者通过答案引擎和传统搜索引擎运行该查询。

### 段落 43 · Page 4

**EN**

We alternated between supportive and opposing queries, allowing us to understand how participants interact with information that aligns or diverges from their viewpoints. Additionally, the study examined whether the answer engine’s responses influenced participants’ opinions or if they perceived any bias, allowing us to better understand how these systems shape user viewpoints and reveal potential biases. The study’s 21 participants were divided into three groups of 7. Each group interacted with a single answer engine: YouChat, Bing Copilot, or Perplexity AI.

**中文**

我们交替提出支持性和反对性的询问，使我们能够了解参与者如何与与其观点一致或不同的信息进行互动。此外，该研究还检查了答案引擎的响应是否影响了参与者的意见，或者他们是否感知到了任何偏见，使我们能够更好地了解这些系统如何塑造用户观点并揭示潜在的偏见。该研究的 21 名参与者被分为三组，每组 7 人。每组都与一个答案引擎进行交互：YouChat、Bing Copilot 或 Perplexity AI。

### 段落 44 · Page 4

**EN**

These platforms were chosen due to their public accessibility as AI-as-a-Service (AIaaS) systems and their marketing as answer engines[48]. For the traditional search engine, Google Search was selected for all participants. We next go over the findings from the 21 completed study sessions. 6https://www.procon.org/

**中文**

选择这些平台是因为它们作为人工智能即服务 (AIaaS) 系统的公共可访问性以及它们作为答案引擎的营销[48]。对于传统搜索引擎，所有参与者都选择了Google搜索。接下来我们回顾 21 个已完成的研究课程的结果。 6https://www.procon.org/

### Page 5

### 段落 45 · Page 5

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, Answer Engine Stance Detection Exercise Search Engine Answer Engine Expert Question Collection Search Engine Pre-Experiment Survey (5 min) Supportive Question Opposing QuestionExpertise Question Part 1 Part 3Part 2 Answer Engine Design Recommendations Section 4 Answer Engine Evaluation Section 5 Expertise Information Retrieval (40 min) Debate Information Retrieval (40 min) Figure 2: High-level diagram of the three parts to the 90-minute usability study we conducted, and the work that derives from study findings: design recommendations, and the Answer Engine Evaluation (AEE) framework.

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024 年 6 月 3-05 日，答案引擎立场检测练习搜索引擎答案引擎专家问题收集搜索引擎实验前调查（5 分钟）支持性问题反对问题专家问题第 1 部分第 3 部分第 2 部分答案引擎设计建议第 4 部分答案引擎评估第 5 部分专业知识信息检索（40 分钟）辩论信息检索（40 分钟） 图 2：我们进行的 90 分钟可用性研究的三个部分的高级图表，以及从研究结果中得出的工作：设计建议和答案引擎评估 (AEE) 框架。

### 段落 46 · Page 5

**EN**

3.2 Pre-Survey Questionnaire Analysis Regarding participants’ familiarity with generative AI (GAI), 37.5% (9/24) of participants use GAI-based applications daily, 29.1% (7/24) weekly, 25% (6/24) monthly, and 8.3% (2/24) a few times per month, confirming that most participants interact frequently with GAI. Regarding the use of answer engines specifically, 70.83% (17/24) of participants were familiar with these systems, 41.16% use them multiple times per week, and 58.84% at least once a month.

**中文**

3.2 预调查问卷分析 关于参与者对生成式人工智能（GAI）的熟悉程度，37.5%（9/24）的参与者每天使用基于 GAI 的应用程序，29.1%（7/24）每周使用基于 GAI 的应用程序，25%（6/24）每月使用一次，8.3%（2/24）每月使用几次，证实大多数参与者经常与 GAI 互动。具体就答案引擎的使用而言，70.83％（17/24）的参与者熟悉这些系统，41.16％的参与者每周多次使用它们，58.84％的参与者每月至少使用一次。

### 段落 47 · Page 5

**EN**

Participants utilized answer engines to conduct research, brainstorm, plan, learn new skills, and obtain faster results compared to traditional search engines. For example, P4 noted, “My experience with current answer engines is similar to using a traditional one such as Google. I think it’s more handy,” while P20 shared, “I use it to get improved, accurate, and clear answers to questions, especially regarding my research studies,” highlighting their relevance in professional and personal contexts.

**中文**

与传统搜索引擎相比，参与者利用答案引擎进行研究、集思广益、计划、学习新技能并获得更快的结果。例如，P4 指出，“我使用当前答案引擎的体验类似于使用 Google 等传统答案引擎。我认为它更方便”，而 P20 则分享道，“我使用它来获得问题的改进、准确和清晰的答案，特别是关于我的研究研究”，强调了它们在专业和个人环境中的相关性。

### 段落 48 · Page 5

**EN**

3.3 Sociotechnical Audit of Answer Engine Shortfalls We employed a constructivist grounded theory using a qualitative coding approach [8] to analyze our user interview data. Following Charmaz [7], the authors individually coded the transcripts line-by-line, employing inductive reasoning to develop theories [26, 27]. Using the qualitative coding platform Taguette7, we generated themes from the transcript snippets.

**中文**

3.3 对答案引擎缺陷的社会技术审计 我们采用了一种建构主义扎根理论，使用定性编码方法 [8] 来分析我们的用户访谈数据。继 Charmaz [7] 之后，作者逐行单独编码转录本，采用归纳推理来发展理论 [26, 27]。使用定性编码平台 Taguette7，我们从转录片段中生成主题。

### 段落 49 · Page 5

**EN**

These themes were then synthesized and refined through collaborative discussions between the authors, and insights were categorized with respect to the four components of an answer engine: (1) answer text, (2) citation, (3) sources, and (4) user interface. The final 16 findings are summarized in Table 1 which the next sections go over in detail. 7https://app.taguette.org/ 3.3.1 Theme 1: Answer Text Findings. A.I. Need for Objective Detail in Generated Answers (21/21): A pervasive issue across all three answer engines was the lack of detail and contextual depth in generated responses. This shortfall affected both expertise and debate queries.

**中文**

然后，通过作者之间的协作讨论来综合和完善这些主题，并根据答案引擎的四个组成部分对见解进行分类：(1) 答案文本、(2) 引用、(3) 来源和 (4) 用户界面。表 1 总结了最终的 16 项发现，接下来的部分将详细介绍。 7https://app.taguette.org/ 3.3.1 主题 1：回答文本发现。人工智能。生成的答案中需要客观细节 (21/21)：所有三个答案引擎中普遍存在的问题是生成的答案中缺乏细节和上下文深度。这种短缺影响了专业知识和辩论查询。

### 段落 50 · Page 5

**EN**

Participants repeatedly found the summaries to be overly generic and insufficient, often driving them to seek more comprehensive information through traditional search engines like Google. Participant P1 noted, “It was just trying to answer without actually giving me a solid answer or a more thought-out answer, which I am able to get with multiple Google searches. " P10 emphasized, “It’s too short and just summarizes everything a lot. [The model] needs to give me more data for the claim, but it’s very summarized.

**中文**

参与者反复发现这些摘要过于笼统且不够充分，这常常促使他们通过谷歌等传统搜索引擎寻找更全面的信息。参与者 P1 指出，“它只是试图回答，但没有真正给我一个可靠的答案或更经过深思熟虑的答案，我可以通过多次谷歌搜索得到这些答案。”P10 强调，“它太短了，只是总结了很多东西。[模型]需要为我的主张提供更多数据，但它非常概括。

### 段落 51 · Page 5

**EN**

” These reflections highlight a common issue: a desire for answer conciseness leads to frequently omitted critical details that would substantiate claims. As a result, responses are perceived as superficial, lacking the necessary specificity and nuance . Participants also expressed concerns about the absence of ‘numbers’ or ‘percentages’ where and when required. As P2 explained,“There’s no quantitative numbers, and I would like to see that if it’s citing sources. It should provide metrics maybe when it’s making these declarations. ” A.II.

**中文**

这些反思凸显了一个常见问题：对答案简洁性的渴望导致经常遗漏可以证实主张的关键细节。因此，人们的反应被认为是肤浅的，缺乏必要的特异性和细微差别。参与者还对在需要时缺乏“数字”或“百分比”表示担忧。正如 P2 所解释的，“没有定量的数字，我想看看它是否引用了消息来源。也许在做出这些声明时它应该提供指标。”

### 段落 52 · Page 5

**EN**

Lack of Holistic Viewpoint (19/21): Our study revealed a limitation in the behavior of answer engines when participants engaged with opinionated queries. The answer engines frequently aligned with the bias implied in the question,neglecting to present diverse perspectives available from the retrieved sources. The responses often appeared to support only the side of the argument the model inferred the participant was “looking for, ” therebyreinforcing user biases. Figure 3 illustrates this by showing an example of a one-sided answer (left, Perplexity.ai) and a comparably more nuanced answer (right, You.com).

**中文**

缺乏整体观点（19/21）：我们的研究揭示了当参与者进行固执己见的查询时，答案引擎的行为存在局限性。答案引擎经常与问题中隐含的偏见保持一致，而忽略了从检索到的来源中呈现不同的观点。这些回答通常似乎只支持模型推断参与者正在“寻找”的论点的一方，从而强化了用户的偏见。图 3 通过显示片面答案（左，Perplexity.ai）和相对更细致的答案（右，You.com）的示例来说明这一点。

### 段落 53 · Page 5

**EN**

Participant P19 noted, “I want to find out more about the flip side of the argument... this is all with a pinch of salt because we don’t know

**中文**

参与者 P19 指出，“我想了解更多关于争论的另一面……这一切都半信半疑，因为我们不知道

### Page 6

### 段落 54 · Page 6

, June 03–05, 2024, Trovato et al.

### 段落 55 · Page 6

**EN**

Answer Text Citation Sources User Interface A.INeed for objective details in generated answers (21/21) C.IMisattribution and misinterpretation of sources cited (21/21) S.ILow Frequency of Sources Used for Summarization (19/21) U.I The lack of selection, and filtering of sources (17/21) A.IILack of holistic viewpoints for opinionated or charged questions (19/21) C.IICherrypicking information based on assumed context (19/21) S.IIMore sources retrieved than used for generating the actual answer (13/21) U.IILack of human input in generation and source selection (17/21) A.IIIOvertly confident language while presenting claims (16/21) C.IIIMissing c

**中文**

答案文本引文来源用户界面 A.I 生成答案中需要客观细节 (21/21) C.I 引用来源的归属和误解 (21/21) S.I 用于总结的来源频率较低 (19/21) U.I 缺乏对来源的选择和过滤 (17/21) A.IIL 对固执己见或有争议的问题缺乏整体观点 (19/21) C.IICherrypicking 信息基于假设的上下文 (19/21) S.II 检索到的来源多于用于生成实际答案的来源 (13/21) U.IIL 在生成和来源选择中缺乏人工输入 (17/21) A.III 在提出主张时过度自信的语言 (16/21) C.III 缺少 c

### 段落 56 · Page 6

**EN**

itations for claims and information generated (18/21) S.IIILack of trust in sources used by the answer engine (12/20) U.IIIAnswer engines take additional work to verify and trust (14/21) A.IVSimplistic language and a lack of creativity and critical thinking (14/21) C.IVTransparency of source selection in model responses (15/21) S.IVRedundancy in source citation and duplicate content retrieved (12/21) U.IVCitations formats are not a normalized interaction (12/21) Table 1: Summary of key findings, organized thematically by answer engine components, with the number of participants who explicitly identified and expressed concerns for each compone

**中文**

对生成的声明和信息的迭代 (18/21) S.III 对答案引擎使用的来源缺乏信任 (12/20) U.III 答案引擎需要额外的工作来验证和信任 (14/21) A.IV 语言简单化，缺乏创造力和批判性思维 (14/21) C.IV 模型响应中来源选择的透明度 (15/21) S.IV 来源引用中的冗余和检索到的重复内容(12/21) U.IVCitations 格式不是标准化交互 (12/21) 表 1：主要调查结果摘要，按答案引擎组件按主题组织，以及明确识别并表达对每个组件的担忧的参与者数量

### 段落 57 · Page 6

nt.

### 段落 58 · Page 6

**EN**

Figure 3: Comparison of outputs from [A] Perplexity, which reflects the bias inherent in the question by presenting only a one-sided response, and [B] YouChat, which acknowledges multiple perspectives, avoiding presenting incomplete information. the other side and the evidence and facts. ” Similarly, P1 stated, “It felt like it was trying to just conform to my question, even though the sources that it was citing actually spoke about all the negatives and positives, " indicating a mismatch between the source content and the generated answer. P4 observed, “It is not giving you both sides of the argument; it’s not arguing with you.

**中文**

图 3：[A] Perplexity 和 [B] YouChat 的输出比较，前者仅提供片面的回答，反映了问题固有的偏见，而后者承认多种观点，避免提供不完整的信息。对方以及证据和事实。 ”同样，P1 表示，“感觉它只是试图符合我的问题，尽管它引用的消息来源实际上谈到了所有的消极和积极因素，”这表明源内容和生成的答案之间不匹配。P4 观察到，“它并没有给你论点的双方；它没有给你提供论据。”它没有和你争论。

### 段落 59 · Page 6

**EN**

Instead, [the model] is just telling you, ’you’re right... and here are the reasons why. ’" These responses highlight a widespread concern: the system’s failure to provide a balanced viewpoint, instead mirroring the biases implicit in the questions posed. A.III. Confident Language While Presenting Claims(16/21): Another prominent issue identified by participants is the generation of overly confident responses. All three systems frequently used terms of affirmation and certainty, even when addressing subjective opinions or claims .

**中文**

相反，[模型]只是告诉你，‘你是对的……原因如下。 ’”这些回应凸显了一个普遍的担忧：该系统未能提供平衡的观点，而是反映了所提出问题中隐含的偏见。A.III.提出主张时的自信语言(16/21)：参与者发现的另一个突出问题是过度自信的回应的产生。所有三个系统都经常使用肯定和确定性的术语，即使在处理主观意见或主张时也是如此。

### 段落 60 · Page 6

**EN**

This approach can lead participants to trust the generated content without the necessary context, with the problem being highlighted for both debate and expertise queries. Figure 3 illustrates the issue: in [A] the answer engine confidently represents information without stating the nuances. Participants highlighted this issue through their interactions with the models. P3 observed that “the model uses a very magnetic or authoritative voice while making claims, ” which “can definitely convince someone that this is ‘the answer’ instead of actually giving them the opportunity to see the issue.

**中文**

这种方法可以引导参与者在没有必要上下文的情况下信任生成的内容，并在辩论和专业知识查询中突出显示问题。图 3 说明了这个问题：在 [A] 中，答案引擎自信地表示信息，但没有说明细微差别。参与者通过与模型的互动强调了这个问题。 P3 观察到，“该模型在提出主张时使用了非常有磁性或权威的声音”，这“绝对可以让某人相信这就是‘答案’，而不是真正给他们机会看到问题。

### 段落 61 · Page 6

**EN**

” Similarly, P4 noted that the model employs the ‘God Voice’, likening it to articles that“make you think that it’s the ultimate truth. ”P3 also mentioned, “It writes so confidently, I feel convinced without even looking at the source. But when you look at the source, it’s bad and that makes me question it again. ”P14 provided a social perspective, stating, “ If someone doesn’t exactly know the right answer, they will trust this even when it is wrong.” A.IV. Overly Simplistic Writing Form and a Lack of Critical Thinking (14/21): The fourth finding highlighted by many participants is the simplistic nature of the language used in responses.

**中文**

同样，P4 指出该模型采用了“上帝之声”，并将其比作“让你认为这是终极真理”的文章。 ”P3还提到，“写得那么自信，我都不看源码就觉得有说服力。但当你查看来源时，你会发现它很糟糕，这让我再次质疑它。 ”P14 提供了一个社会视角，指出：“如果有人不完全知道正确答案，即使答案是错误的，他们也会相信这个答案。” A.IV.过于简单的写作形式和缺乏批判性思维（14/21）：许多参与者强调的第四个发现是回复中使用的语言过于简单化。

### 段落 62 · Page 6

**EN**

Participants noted that this simplicity in language reflects a lack of critical analysis and thinking. For example, P13 found the answers to be “kind of childish, ”noting they did not match the scientific level required. P2 described the text as “fluffy”and “similar to what a fifth grader might write without consulting sources”. P5 quoted ‘If I was grading a student’s assignment and they had given me that answer... I don’t know that I would want to pass a student. ”.

**中文**

与会者指出，这种语言的简单性反映出缺乏批判性的分析和思考。例如，P13 发现答案“有点幼稚”，并指出它们不符合所需的科学水平。 P2 将该文本描述为“蓬松”且“类似于五年级学生在不查阅资料的情况下可能写出的内容”。 P5 引用道：“如果我正在给学生的作业评分，而他们给了我这个答案……我不知道我是否会想让某个学生通过。” ”。

### Page 7

### 段落 63 · Page 7

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, Additionally, some participants perceived the systems as‘people pleasers’, presenting information in a manner that was agreeable or comforting rather than providing a comprehensive or accurate response. P1 noted, “It’s being a people pleaser and only trying to validate me. ”These insights highlight the need for answer engines to provide more nuanced and detailed responses. 3.3.2 Theme 2: Citation. C.I.

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024 年 6 月 3 日至 5 日，此外，一些参与者认为这些系统是“讨好者”，以令人愉快或舒适的方式呈现信息，而不是提供全面或准确的响应。 P1 指出，“这是为了取悦别人，只是想验证我的观点。”这些见解凸显了答案引擎需要提供更细致、更详细的答案。 3.3.2 主题 2：引用。 C.I.

### 段落 64 · Page 7

**EN**

Misattribution of Sources: Correct Summaries, Incorrect Citations (21/21): A common issue identified in this theme was themisattribution of sources. This occurs when the answer engine cites a source that does not factually support the cited statement, misrepresenting the source content. For instance, P12 noted, “It has cited irrelevant parts of the paper for this question. ” P15 commented, “But this statement doesn’t seem to be in the source. I mean the statement is true; it’s valid...

**中文**

来源的错误归属：正确的摘要，错误的引用 (21/21)：该主题中发现的一个常见问题是来源的错误归属。当答案引擎引用的来源实际上并不支持所引用的陈述，歪曲了来源内容时，就会发生这种情况。例如，P12 指出，“它引用了与这个问题无关的论文部分。”P15 评论道，“但这个说法似乎不在来源中。我的意思是这个说法是真实的；它是有效的......

### 段落 65 · Page 7

**EN**

but I don’t know where it’s even getting this information from.” Similarly, P17 observed, “So [the answer] mentions information on nutrients, but that is not present at all in the whole sentence and the whole article [cited].” Participants felt that the systems were using citations to legitimize their answer , creating an illusion of credibility. This facade was only revealed to a few users who proceeded to scrutinize the sources. P4 expressed concern, “But does it feel that it’s using citations to legitimize itself for its own generation?

**中文**

但我不知道它从哪里得到这些信息。”同样，P17 观察到，“所以[答案]提到了有关营养素的信息，但整个句子和整篇文章[引用]中根本没有出现这一点。”参与者认为系统正在使用引用来使他们的答案合法化，从而造成可信度的错觉。这个外观只向少数用户透露，他们开始仔细检查消息来源。 P4表示担忧，“但它是否觉得它是在利用引用来为自己这一代人合法化？

### 段落 66 · Page 7

**EN**

” and elaborated, “I mean it’s just like you see a citation, you assume it’s a valid source...I’ll just see that there is a source. That’s it. I don’t verify it.” This misattribution highlights a major flaw in the model’s process: even when a statement is accurate, the citation can point to an irrelevant source. C.II. Cherrypicking Information Based on Assumed Context (19/21): When participants posed expert or opinion-based questions, they noticed that the system often selectively presented information from retrieved sources, highlighting a particular perspective instead of a comprehensive view of the article .

**中文**

”并详细说明，“我的意思是，就像你看到一个引文，你认为它是一个有效的来源......我只会看到有一个来源。就是这样。我不去验证。”这种错误归因凸显了模型过程中的一个主要缺陷：即使陈述准确，引用也可能指向不相关的来源。 C.II.基于假设上下文的精挑细选信息（19/21）：当参与者提出专家或基于意见的问题时，他们注意到系统经常有选择地呈现来自检索来源的信息，突出特定的观点而不是文章的全面视图。

### 段落 67 · Page 7

**EN**

For instance, P7 noted, “I feel [the system] is manipulative. It takes only some information and it feels I am manipulated to only see one side of things." Similarly, P8 observed, “[The source] actually has both pros and cons, and it’s chosen to pick just the sort of required arguments from this link without the whole picture. " P12 added these concerns, stating, "It’s sort of presenting some information that it’s picked out already from all the articles and gives that to me. I feel like it sort of reinforces only certain notions. " Participants felt that the model does not accurately represent the full scope of the source material.

**中文**

例如，P7 指出，“我觉得[该系统]具有操纵性。它只需要一些信息，感觉我被操纵了，只能看到事物的一面。”同样，P8 观察到，“[来源]实际上有利有弊，它选择从这个链接中只选择所需的参数，而不考虑整个情况。 ” P12 补充了这些担忧，并表示，“这有点像是从所有文章中挑选出来的一些信息，并将其提供给我。我觉得它只是强化了某些概念。 “参与者认为该模型并不能准确地代表源材料的全部范围。

### 段落 68 · Page 7

**EN**

This behavior underscores the model’s limitation in potentially misrepresenting sources by taking statements out of context to fit the query. The tendency to reinforce assumed user biases further contributes to anecho chamber effect, limiting exposure to a broader range of perspectives and potentially distorting the original intent of the source material. C.III. Missing Citation for Claims and Information Generated (18/21): The absence of citations in many of the sentences generated by all three answer engines emerged as a critical issue, especially when key claims or facts are presented without necessary factual support from the sources .

**中文**

这种行为强调了模型通过断章取义来适应查询而可能歪曲来源的局限性。强化假设的用户偏见的趋势进一步加剧了消声室效应，限制了更广泛的视角，并可能扭曲源材料的原始意图。 C.III.声明和生成信息的引用缺失 (18/21)：所有三个答案引擎生成的许多句子中缺乏引用成为一个关键问题，特别是当关键声明或事实在没有来源必要的事实支持的情况下提出时。

### 段落 69 · Page 7

**EN**

P8 expressed frustration with this issue, stating, “I really wanted a reference with this [claim] because it is like giving a statement mentioning that this is historical but this is without any citations or without any validation. " Similarly, P16 highlighted the inconvenience caused, noting, “Not having the references for each sentence is annoying...you want to know what’s the resource retrieved is. Now we’ll have to actually go to the website and compare notes, which is an additional step which no one wants to do. I would have gone to the website in the first place instead.

**中文**

P8 对这个问题表示沮丧，并表示：“我真的想要参考这个[声明]，因为这就像发表一份声明，提到这是历史性的，但没有任何引用或没有任何验证。 ” 同样，P16 强调了造成的不便，并指出，“没有每个句子的参考文献很烦人……你想知道检索到的资源是什么。现在我们必须实际访问网站并交换意见，这是没人愿意做的额外步骤。我本来会首先访问该网站。

### 段落 70 · Page 7

**EN**

" These comments reveal a clear demand for citations, particularly for sentences that are critical to answering the question. Figure 4 shows an example of an uncited statement in a Perplexity answer, compared to a similar Copilot cited answer. C.IV. Lack of Transparency of Source Selection in Model Responses (15/21): Participants raised significant concerns about the lack of transparency in how the system selects and prioritizes citation , highlighting the need for a clearer explanation of its decisionmaking process.

**中文**

这些评论揭示了对引用的明确需求，特别是对回答问题至关重要的句子。图 4 显示了 Perplexity 答案中未引用的语句的示例，与类似的 Copilot 引用的答案相比。C.IV. 模型响应中来源选择缺乏透明度 (15/21)：参与者对系统如何选择和优先考虑引用缺乏透明度表示严重关切，强调需要对其决策过程进行更清晰的解释。

### 段落 71 · Page 7

**EN**

This “black box " nature of the system makes it difficult for users to trust the outputs, as they cannot discern why certain sources are cited over others. Participants frequently noted that the system did not adequately prioritize important or factual sources, leading to a general de-emphasis of critical references. For instance, P4 questioned, “Where is it getting this thing from? Why is it getting it from these particular sources is what I’m curious about.

**中文**

系统的这种“黑匣子”性质使用户很难信任输出，因为他们无法辨别为什么某些来源被引用而不是其他来源。参与者经常指出，该系统没有充分优先考虑重要或事实来源，导致关键参考文献普遍不被重视。例如，P4 质疑：“这个东西是从哪里得到的？我很好奇为什么它会从这些特定来源获得它。

### 段落 72 · Page 7

**EN**

" Additionally, P2 expressed frustration with the system’s opaque process on the lack of stating which specific part the information came from the source, stating, “It’s very easy to just cough out sources and be like, ‘this is where I took all this information from. ’ But which part of the information did you take from? That kind of explanation doesn’t exist." Such feedback underscores the importance of transparency in the system’s source evaluation criteria. As P5 remarked, “It’s picking results from the first page of Google Search...

**中文**

此外，P2 对系统不透明的流程表示失望，因为系统没有说明信息来自哪个具体部分，并表示：“很容易就直接吐出来源，然后说，‘这就是我获取所有这些信息的地方。 ’但是你从哪部分信息中获取了呢？这种解释并不存在。”这样的反馈强调了系统源评估标准透明度的重要性。正如 P5 所说，“它从 Google 搜索的第一页中挑选结果......

### 段落 73 · Page 7

**EN**

but I didn’t see any consistency," suggesting that users need more clarity to trust the system’s outputs fully. 3.3.3 Theme 3: Sources. S.I. Low Number of Sources(19/21): For both expert and opinionated questions, participants encountered experiences where they needed more sources to address the question at hand. Participants highlighted this issue with specific feedback. For instance, P16 remarked, “It feels like it’s pulling all of this from one source , ” while P1 noted, “Again, everything is extracted from the same source, which is very weird.

**中文**

但我没有看到任何一致性”，这表明用户需要更清晰的信息才能完全信任系统的输出。 3.3.3 主题 3：来源。S.I. 来源数量低（19/21）：对于专家问题和固执己见的问题，参与者都遇到过需要更多来源来解决手头问题的经历。参与者通过具体反馈强调了这个问题。例如，P16 评论说，“感觉像是从一个来源拉出所有这些”，而P1 指出：“再次强调，一切都是从同一个来源提取的，这很奇怪。

### 段落 74 · Page 7

**EN**

” This indicated a pattern where the answer engine heavily relied on a limited number of sources, averaging to three sources used , often leading to incomplete answers. Interestingly, this issue also caused a phenomenon where the model overtly emphasized certain sources for generation . Participants flagged this as a consequence of the models using very few sources for their answer. P5 mentioned, “If it’s like citing the right review paper, it can get away with citing only one [source], but it isn’t doing that and citing one weak article throughout, ” and P11 added, “It feels off as it’s just paraphrasing that one source.

**中文**

”这表明答案引擎严重依赖有限数量的来源，平均使用三个来源，通常会导致不完整的答案。有趣的是，这个问题还导致了一种现象，即模型公开强调某些生成来源。参与者将此标记为模型使用很少的来源作为答案的结果。P5 提到，“如果就像引用正确的评论论文，它可以只引用一个[来源]，但它并没有这样做，并且全文都引用了一篇薄弱的文章，”P11 补充道，“这感觉不太好，因为它只是解释了那个来源。

### 段落 75 · Page 7

**EN**

” By relying on a narrow selection of sources, the answer engines fail to capture the full spectrum of information necessary for a well-rounded answer. S.II. More Sources Listed Than Used (13/21):

**中文**

” 由于依赖于狭窄的来源选择，答案引擎无法捕获全面答案所需的全部信息。S.II. 列出的来源多于使用的来源 (13/21)：

### Page 8

### 段落 76 · Page 8

**EN**

, June 03–05, 2024, Trovato et al. Figure 4: Comparison of outputs from [A] Perplexity, which lacks citations for the points generated, causing confusion on the actual source of each sentence, and [B] Copilot, which effectively indicates the sources for each statement. Participants using Bing Copilot and Perplexity noted that these systems often listed multiple retrieved sources without actually citing them in the generated answer , a behavior described as “buffing”—creating an impression of thoroughness without substance.

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。图 4：[A] Perplexity 和 [B] Copilot 的输出比较，前者缺乏对生成点的引用，导致对每个句子的实际来源产生混淆，后者有效地指示每个陈述的来源。使用 Bing Copilot 和 Perplexity 的参与者指出，这些系统经常列出多个检索到的来源，但实际上并没有在生成的答案中引用它们，这种行为被描述为“抛光”——给人一种彻底但没有实质内容的印象。

### 段落 77 · Page 8

**EN**

This practice led to confusion and eroded trust, as users saw citations that were not integrated into the generated response. For example, P12 remarked, “It’s giving the impression of multiple sources, but it’s just citing something that has a blurb citing to the other source. So it’s really just coming off of this one source.” Similarly, P20 observed: “Even when it lists other sources that might be relevant or have other viewpoints, it doesn’t actually say much about them.

**中文**

这种做法导致了混乱并削弱了信任，因为用户看到的引用并未集成到生成的响应中。例如，P12 评论道：“它给人的印象是有多个来源，但它只是引用了一些内容，其中有一个引述其他来源的内容。所以它实际上只是来自这一来源。”同样，P20 观察到：“即使它列出了可能相关或有其他观点的其他来源，但实际上并没有对它们说太多。

### 段落 78 · Page 8

**EN**

” This selective use of sources caused frustration, as participants believed the models ignored more reliable or relevant articles, diminishing the perceived quality of the generated content. P5 expressed this concern, stating, “Why didn’t they use this [listed but uncited article]? This would be much more reliable relatively! ” Notably, however, YouChat did not display this specific weakness and consistently cited all listed sources in its responses. S.III. Lack of Trust in Source Types (12/20): The answer engines retrieve content from varying sources, including forums, blogs, opinion pieces, and research articles.

**中文**

”这种对来源的选择性使用引起了挫败感，因为参与者认为模型忽略了更可靠或相关的文章，从而降低了生成内容的感知质量。P5 表达了这种担忧，并表示，“为什么他们不使用这篇[列出但未引用的文章]？这样相对来说就靠谱多了！然而，值得注意的是，YouChat 并没有表现出这一具体弱点，并且始终在其回复中引用了所有列出的来源。S.III. 对来源类型缺乏信任 (12/20)：答案引擎从不同来源检索内容，包括论坛、博客、观点文章和研究文章。

### 段落 79 · Page 8

**EN**

However, participants expressed general distrust toward certain sources due to perceived biases, or lack of authority. This distrust was evident in feedback like P1’s remark, “Who knows who has written that post [...] it’s a LinkedIn post when the question is a scientific one," and P2’s observation, “The sources are not convincing. They seem to be these non-factual sources from where this answer is kind of drawn." Additionally, participants noted issues with outdated or misinformed content being used to generate answers. For example, P10 mentioned, "I think the citation is outdated...

**中文**

然而，由于存在偏见或缺乏权威，参与者普遍对某些来源表示不信任。这种不信任在反馈中表现得很明显，比如 P1 的评论，“谁知道谁写了这篇文章 [...] 当问题是一个科学问题时，它是 LinkedIn 的帖子”，以及 P2 的观察，“消息来源并不令人信服。它们似乎是从这些非事实来源中得出这个答案的。”此外，参与者还指出了使用过时或误导性内容来生成答案的问题。例如，P10 提到，“我认为引文已经过时了......

### 段落 80 · Page 8

**EN**

because it says ’Windows 10’, and we’ve already switched to better OS, which is what the answer needed ". S.IV. Different Sources but Duplicate Content (12/21): Participants identified instances where the answer engine retrieved and cited multiple sources that, upon closer inspection, contained identical or highly similar content. While these sources were presented as distinct entities with different citation numbers, they ultimately contributed redundant information. Such findings raised concerns about potential inaccuracies in the system’s source selection process.

**中文**

因为上面写着‘Windows 10’，而我们已经切换到更好的操作系统，这正是答案所需要的”。 S.IV。来源不同但内容重复 (12/21)：参与者确定了答案引擎检索并引用多个来源的实例，经过仔细检查，这些来源包含相同或高度相似的内容。虽然这些来源被呈现为具有不同引用数量的不同实体，但它们最终提供了冗余信息。这些发现引起了人们对系统源选择过程中潜在不准确的担忧。

### 段落 81 · Page 8

**EN**

For example, P3 observed, “Source 1 and 2 are just the same content in different formats. This is funny as it’s using them differently,” and P9 stated, “I think this is a big problem! I should have checked the citations on the other answer as well because it’s basically just giving me one website but citing it differently multiple times.” This phenomenon reveals limitations in the model’s sourcing strategy, suggesting a reliance on superficial differences, such as formatting or minor variations, to justify multiple citations.

**中文**

例如，P3 观察到，“来源 1 和 2 只是不同格式的相同内容。这很有趣，因为它们的使用方式不同，”P9 表示，“我认为这是一个大问题！我也应该检查另一个答案的引用，因为它基本上只是给了我一个网站，但多次以不同的方式引用它。”这种现象揭示了模型采购策略的局限性，表明依赖于表面差异（例如格式或微小变化）来证明多次引用的合理性。

### 段落 82 · Page 8

**EN**

As a result, the system provides a misleading appearance of a wellrounded answer while simply recycling the same content. Figure 5 provides an example of duplicate sourcing. 3.3.4 Theme 4: User Interface. U.I. Autonomy over Source Validation and Selection (17/21): Participant feedback underscored that answer engines often offer narrow perspectives, due to users having little to no control over the information presented to them, leading to concerns about a lack of autonomy and the inability to evaluate the credibility of sources independently.

**中文**

结果，系统提供了一个具有误导性的全面答案，同时只是重复使用相同的内容。图 5 提供了重复采购的示例。 3.3.4 主题 4：用户界面。 U.I.来源验证和选择的自主权 (17/21)：参与者反馈强调，由于用户几乎无法控制向他们提供的信息，答案引擎通常提供狭隘的视角，导致人们担心缺乏自主权和无法独立评估来源的可信度。

### 段落 83 · Page 8

**EN**

P5 stated, “The [answer engine] did not give me a whole lot of confidence in its ability to assess the quality of sources. I would have more trust in my ability to do that. ” This sentiment suggests that users feel more competent in selecting and scrutinizing sources themselves. P11 further elaborated, “[The answer engine] is taking from these sources, but are they even legit?

**中文**

P5 表示，“[答案引擎] 并没有让我对其评估资源质量的能力充满信心。我会更加相信自己有能力做到这一点。”这种情绪表明，用户感觉自己更有能力选择和审查资源。 P11 进一步阐述道，“[答案引擎]是从这些来源获取的，但它们合法吗？

### Page 9

### 段落 84 · Page 9

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, Figure 5: Results generated by Perplexity [A] and the corresponding sources retrieved [B]. The image illustrates how the model retrieved 8 sources, many of which are duplicates of the same source. Despite this, the model cites them differently, creating an illusion of varied content when it is actually the same. I cannot choose or remove the ones it chose. At least with Google, I have a lot more choices to click.

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024 年 6 月 3 日至 5 日，图 5：Perplexity 生成的结果 [A] 和检索到的相应来源 [B]。该图展示了模型如何检索 8 个源，其中许多是同一源的重复项。尽管如此，该模型以不同的方式引用它们，造成内容实际上相同的情况下不同的错觉。我无法选择或删除它选择的那些。至少有了Google，我有更多的选择可以点击。

### 段落 85 · Page 9

**EN**

” These findings suggest that while answer engines may provide quick responses, they fail to meet user expectations for transparency and control. The inability to select, filter, or assess sources independently not only limits the breadth of information but also undermines user confidence in the accuracy and reliability of the answers provided. U.II.

**中文**

这些发现表明，虽然答案引擎可以提供快速响应，但它们无法满足用户对透明度和控制的期望。无法独立选择、过滤或评估来源不仅限制了信息的广度，而且还削弱了用户对所提供答案的准确性和可靠性的信心。 U.II。

### 段落 86 · Page 9

**EN**

Lack of Human Input in Generation and Source Selection (17/21): Our study identified a key issue with answer engines: the tendency to lose context when generating responses due to the answer engine assuming the most probable context rather than accurately interpreting or clarifying the specific context. Participant P7 highlighted this issue: “I think the sources were right, but the context is lost. It did not manage to go to the expected answers at all. ” This points to a core limitation: even with accurate sources, the inability to maintain the correct context of the query results in unsatisfactory answers.

**中文**

生成和源选择中缺乏人工输入（17/21）：我们的研究发现了答案引擎的一个关键问题：由于答案引擎假设最可能的上下文而不是准确地解释或澄清特定上下文，因此在生成响应时倾向于丢失上下文。参与者P7强调了这个问题：“我认为来源是正确的，但上下文丢失了。它根本没有设法到达预期的答案。”这指出了一个核心限制：即使有准确的来源，也无法维护查询的正确上下文，导致答案不令人满意。

### 段落 87 · Page 9

**EN**

P9 further noted, “This is a very generic answer that just has basic features [of the answer]. It doesn’t say anything at all of the context asked. ” Participants suggested that the singleinteraction design contributes to this issue. In cases where context is critical, participants recommended that the system should adopt a more interactive, conversational approach by asking questions before answering. By asking clarification questions, answer engines could better address ambiguity and provide more accurate responses.

**中文**

P9 进一步指出，“这是一个非常通用的答案，只有[答案]的基本特征。它根本没有说明所询问的上下文。”参与者认为单一交互设计导致了这个问题。在上下文至关重要的情况下，参与者建议系统应采用更具互动性、对话性的方法，在回答之前提出问题。通过提出澄清问题，答案引擎可以更好地解决歧义并提供更准确的答复。

### 段落 88 · Page 9

**EN**

P1 also remarked, "Having [the system] ask further questions to alleviate any potential ambiguity on the generation would have helped, instead of assuming the context. " U.III. Additional Work to Verify and Trust Answers(14/21): As described in previous findings, participants often felt compelled to independently verify the provided sources due to distrust. Therefore, contrary to their intended purpose, some participants found that the answer engines often resulted in more work for users, undermining their marketed goal of simplifying information retrieval.

**中文**

P1 还表示，“让[系统]提出进一步的问题来减轻一代人的任何潜在歧义，而不是假设上下文，会有所帮助。”U.III。验证和信任答案的额外工作(14/21)：如之前的调查结果所述，由于不信任，参与者常常感到有必要独立验证所提供的来源。因此，与他们的预期目的相反，一些参与者发现答案引擎通常会给用户带来更多的工作，从而破坏了他们简化信息检索的营销目标。

### 段落 89 · Page 9

**EN**

Participant P2 highlighted this inefficiency: “Even if it’s gonna give me five paragraphs with 300 sources, it’s not going to help me because [...] I’m gonna go and check each source, so this is just another level of information interaction for me.” The necessity to cross-check each source individually added complexity, extending the time required to complete tasks that might have been faster with a traditional search engine. P17 echoed this, stating, “We have to go to the website and compare notes and all of that [for verification], which is an additional step which no one wants to do.

**中文**

参与者 P2 强调了这种低效率：“即使它会给我 5 个段落和 300 个来源，它也不会帮助我，因为 [...] 我要去检查每个来源，所以这对我来说只是另一个级别的信息交互。”单独交叉检查每个来源的必要性增加了复杂性，延长了完成任务所需的时间，而使用传统搜索引擎可能会更快。 P17 对此表示赞同，并表示：“我们必须访问网站并交换意见以及所有这些（以进行验证），这是没有人愿意做的额外步骤。

### 段落 90 · Page 9

**EN**

I would have just gone to the website in the first place. ” P5 also emphasized the inefficiency: “The [answer engine] does not speed up the process. I don’t feel like I would trust it enough to just go off that. ” U.IV. Citation Formats are Not a Normalized Interaction (12/21): The format of citations affects user experience. The most common method involves numerical citations (e.g., [1], [1][2]), where numbers correspond to references listed below the content. While familiar to those accustomed to academic writing, this format can be less intuitive or effective for individuals who do not regularly engage with such reference systems .

**中文**

我一开始就会访问该网站。 ” P5 还强调了效率低下的问题：“[答案引擎] 并没有加快流程。我觉得我不会足够信任它而放弃它。 ”U.IV。引文格式不是标准化交互（12/21）：引文格式影响用户体验。最常见的方法涉及数字引用（例如，[1]、[1][2]），其中数字对应于内容下方列出的参考文献。虽然习惯于学术写作的人很熟悉这种格式，但对于不经常使用此类参考系统的人来说，这种格式可能不太直观或有效。

### 段落 91 · Page 9

**EN**

Participant P10 highlighted this issue: “I actually really don’t understand the citations because in my job and daily life, it isn’t used. ” This concern suggests that numerical citations, while clear to some, may not be meaningful to a general audience unfamiliar with academic or research practices. P14 echoed this sentiment, noting, “People may not understand how [citations] work. People rarely, say my mom or

**中文**

参与者P10强调了这个问题：“我实际上真的不明白引文，因为在我的工作和日常生活中，它不会被使用。”这种担忧表明，数字引文虽然对某些人来说很清楚，但对于不熟悉学术或研究实践的普通受众来说可能没有意义。 P14 呼应了这一观点，并指出：“人们可能不明白[引文]是如何运作的。人们很少，我妈妈或

### Page 10

### 段落 92 · Page 10

**EN**

, June 03–05, 2024, Trovato et al. aunt, will not understand what to make of it or how that works as well.” However, participants who interacted with Bing Copilot, which uses a hover-over feature to display source information, reported a better understanding of where the information came from. This feature allows users to hover over sentences to see the corresponding source, encouraging direct interaction with the sources in a more accessible manner . Participant P2 commented, “[The on-hover] is very useful to have.

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。姑妈，她不会明白这是怎么回事，也不明白它是如何运作的。”然而，与 Bing Copilot（使用悬停功能显示源信息）进行交互的参与者报告说，他们更好地了解了信息的来源。此功能允许用户将鼠标悬停在句子上以查看相应的来源，鼓励以更易于访问的方式与来源进行直接交互。参与者 P2 评论道：“[悬停] 非常有用。

### 段落 93 · Page 10

**EN**

Sources here, I think it will help more people to feasibly check for sources every time they’re taking something from a system like this as they are forced to interact with it.” This suggests that simple numerical references may not be sufficient to build trust and that more interactive approaches could enhance user engagement and comprehension. We have identified the major findings from our participant interactions in this section. Additionally, minor findings are included in Appendix A.3.

**中文**

这里的消息来源，我认为这将帮助更多的人在每次从这样的系统中获取某些东西时，因为他们被迫与之交互，所以可以切实地检查消息来源。”这表明简单的数字参考可能不足以建立信任，而更具互动性的方法可以增强用户的参与度和理解力。我们已经确定了本节参与者互动的主要发现。此外，附录 A.3 中还包含了一些次要的发现。

### 段落 94 · Page 10

**EN**

3.4 Source and Citation Interaction Evaluation To complement qualitative insights, we investigate the number of sources displayed and cited by the three answer engines and participants’ interaction with these sources. Our study revealed that the chosen answer engines cite a limited subset of sources displayed. Table 2 illustrates the disparity between sources retrieved (mean: 4.31) and sources cited (mean: 3.0) in the final answers, varying across answer engines. The analysis quantitatively supports the finding that answer engines display more sources than they cited, causing user confusion and distrust.

**中文**

3.4 来源和引文交互评估为了补充定性见解，我们调查了三个答案引擎显示和引用的来源数量以及参与者与这些来源的交互。我们的研究表明，所选答案引擎引用了显示的有限来源子集。表 2 说明了最终答案中检索到的来源（平均值：4.31）和引用的来源（平均值：3.0）之间的差异，因答案引擎而异。该分析定量地支持了以下发现：答案引擎显示的来源比其引用的多，导致用户困惑和不信任。

### 段落 95 · Page 10

**EN**

Out of the three answer engines, Perplexity displays the most sources (mean: 5.00), but cites the least (mean: 2.58), while YouChat cites all the sources that are displayed (mean: 3.57). Withan average of only three sources available , users have limited autonomy in selecting and verifying information. Further investigation into user interaction with sources reveals a stark contrast in how individuals hover and click sources when using answer engines versus traditional search engines.

**中文**

在三个答案引擎中，Perplexity 显示的来源最多（平均值：5.00），但引用最少（平均值：2.58），而 YouChat 引用了所有显示的来源（平均值：3.57）。由于平均只有三个可用来源，用户在选择和验证信息方面的自主权有限。对用户与来源交互的进一步调查揭示了个人在使用答案引擎与传统搜索引擎时悬停和点击来源的方式形成鲜明对比。

### 段落 96 · Page 10

**EN**

As shown in Table 3 and Figure 6, participants display a much narrower scope of inquiry when leveraging answer engines, hovering an average of only 2 sources (median: 2; SD: 1.39) . This limited engagement likely results from the fewer sources provided by answer engines, which restricts the breadth of information users can explore. In contrast, participants using traditional search engines adopt a more comprehensive approach, hovering an average of 12 sources (median: 11; SD: 3.56) . Additionally, there is a notable difference in the number of sources clicked to thoroughly analyze to find answers.

**中文**

如表 3 和图 6 所示，参与者在利用答案引擎时显示的询问范围要窄得多，平均只有 2 个来源（中位数：2；SD：1.39）。这种有限的参与可能是由于答案引擎提供的资源较少造成的，这限制了用户可以探索的信息的广度。相比之下，使用传统搜索引擎的参与者则采用更全面的方法，平均徘徊在 12 个来源（中位数：11；SD：3.56）。此外，为了彻底分析以寻找答案而点击的来源数量也存在显着差异。

### 段落 97 · Page 10

**EN**

With answer engines, users tend to click on a single source and trust the model’s selection. However, when using traditional search engines, participants engage with a wider range of sources, clicking and analyzing an average of 4 sources. We conducted independent two-sample t-tests to statistically assess our findings, comparing user interactions during traditional search engine use with those observed when using each answer engine. The significance level was set to 𝛼 = 0.01.

**中文**

使用答案引擎，用户倾向于点击单一来源并信任模型的选择。然而，当使用传统搜索引擎时，参与者会接触更广泛的来源，平均点击并分析 4 个来源。我们进行了独立的两个样本 t 检验来统计评估我们的发现，将传统搜索引擎使用期间的用户交互与使用每个答案引擎时观察到的用户交互进行比较。显着性水平设置为 𝛼 = 0.01。

### 段落 98 · Page 10

**EN**

As shown in Table 4, the results reveal statistically significant differences in user interactions, allowing us to reject the null hypothesis that answer engines foster similar interactions as traditional engines. Finally, our analysis in Table 5 examined how individuals interact with answer engines when asking questions that align with or challenge their acknowledged stance. When faced with contradictory questions, participants engaged in more analysis, hovering (mean = 1.72) and clicking (mean = 2.95) a higher number of sources.

**中文**

如表 4 所示，结果揭示了用户交互的统计显着差异，使我们能够拒绝答案引擎促进与传统引擎类似的交互的零假设。最后，我们在表 5 中的分析研究了个人在提出符合或挑战其公认立场的问题时如何与答案引擎互动。当面对矛盾的问题时，参与者会进行更多的分析，悬停（平均值 = 1.72）并点击（平均值 = 2.95）更多数量的来源。

### 段落 99 · Page 10

**EN**

In contrast, when asking aligned questions, participants relied on fewer sources (hovering: mean = 1.08; clicking: mean = 0.48) and often trusted information with lesser verification. The two sample t-tests confirmed a significant difference in verification behaviors between the two conditions (hovering; p-value = 4.93e-06, clicking; p-value = 4.88e-05). 4 Design Recommendations and Metrics 4.1 Answer Engine Design Recommendation To make findings from the study concrete and actionable, we distill them into a set of design recommendations for answer engine development.

**中文**

相比之下，当提出一致的问题时，参与者依赖的来源较少（悬停：平均值 = 1.08；点击：平均值 = 0.48），并且通常信任经过较少验证的信息。两个样本 t 检验证实了两种条件之间的验证行为存在显着差异（悬停；p 值 = 4.93e-06，点击；p 值 = 4.88e-05）。 4 设计建议和指标 4.1 答案引擎设计建议 为了使研究结果具体化并具有可操作性，我们将其提炼成一套用于答案引擎开发的设计建议。

### 段落 100 · Page 10

**EN**

When possible, we then tie a recommendation with a computable metric that can measure relative adherence with the metric. Table 6 provides the mapping between the study findings, the design recommendations, and the metrics. A detailed definition of each recommendation is presented in Appendix A.4, and we now define each of the metrics. 4.2 Answer Engine Metrics Figure 7 illustrates the processing of an answer engine’s response into the 8 metrics of the Answer Engine Evaluation Framework, while Table 6 showcases the motivation and rationale behind each metric.

**中文**

如果可能，我们会将建议与可计算的指标联系起来，该指标可以衡量对该指标的相对遵守情况。表 6 提供了研究结果、设计建议和指标之间的映射。附录 A.4 中提供了每项建议的详细定义，我们现在定义每项指标。 4.2 答案引擎指标 图 7 说明了将答案引擎的响应处理为答案引擎评估框架的 8 个指标的过程，而表 6 则展示了每个指标背后的动机和基本原理。

### 段落 101 · Page 10

**EN**

We first go over the preliminary processing common to several metrics, then define each metric. 4.2.1 Preliminary Processing. When evaluating an answer engine, our evaluation framework requires the extraction of four content elements: the user query (1), the generated answer text (2) with the embedded citation (3) to the sources represented by a publicly accessible URL (4). Because APIs made available by answer engines do not provide all of these elements, we implemented automated browser scripts to extract these elements for three popular answer engines: You.com, Perplexity.ai, and BingChat8.

**中文**

我们首先回顾几个指标通用的初步处理，然后定义每个指标。 4.2.1 初步处理。在评估答案引擎时，我们的评估框架需要提取四个内容元素：用户查询 (1)、生成的答案文本 (2) 以及嵌入的引文 (3) 以及由可公开访问的 URL 表示的来源 (4)。由于答案引擎提供的 API 并不提供所有这些元素，因此我们实现了自动浏览器脚本来为三个流行的答案引擎提取这些元素：You.com、Perplexity.ai 和 BingChat8。

### 段落 102 · Page 10

**EN**

Several operations below rely on LLM-based processing, for which we default to using GPT-4o, and have listed the prompts used in Appendix A.6. When necessary, we evaluate the accuracy of LLM-based processing and report on the level of agreement with manual annotation. A first operation consists of decomposing the answer text into statements. A statement is typically a sentence, and occasionally a sub-unit of a sentence. Decomposing the answer into statements allows to study the factual backing of the answer by the sources at a granular level, and is common in fact-checking literature [44, 71].

**中文**

下面的几个操作依赖于基于 LLM 的处理，对此我们默认使用 GPT-4o，并在附录 A.6 中列出了使用的提示。必要时，我们会评估基于法学硕士的处理的准确性，并报告与手动注释的一致性程度。第一个操作包括将答案文本分解为语句。陈述通常是一个句子，有时也可以是句子的子单元。将答案分解为陈述可以在粒度级别上研究来源对答案的事实支持，这在事实核查文献中很常见 [44, 71]。

### 段落 103 · Page 10

**EN**

In the example of Figure 7, the answer text is decomposed into seven statements. Each statement is further assigned two attributes: Query Relevance is a binary attribute that indicates whether the statement contains answer elements relevant to the user query. Irrelevant statements are typically introductory or concluding statements that do not contain factual information (e.g., “That’s a great 8Extending the evaluation to other answer engines would require adapting the scripts to the specific website structure of the target answer engines.

**中文**

在图 7 的示例中，答案文本被分解为七个语句。每个语句还被分配两个属性： 查询相关性是一个二进制属性，指示该语句是否包含与用户查询相关的答案元素。不相关的陈述通常是不包含事实信息的介绍性或结论性陈述（例如，“这是一个很棒的8将评估扩展到其他答案引擎将需要使脚本适应目标答案引擎的特定网站结构。

### Page 11

### 段落 104 · Page 11

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, Sources Displayed by Answer Engine Sources Cited by Answer Engine All Perplexity Bing Copilot YouChat All Perplexity Bing Copilot YouChat Mean 4.31 5.00 4.46 3.57 3.00 (69%) 2.58 (51%) 2.80 (62%) 3.57 (100%) Median 5.00 5.00 4.00 4.00 3.00 3.00 3.00 4.00 SD 1.32 0.00 1.56 1.25 1.15 0.65 1.18 1.25 Max 8.00 5.00 8.00 6.00 6.00 4.00 6.00 6.00 Min 1.00 5.00 1.00 1.00 1.00 1.00 1.00 1.00 Table 2: Sources Retrieved vs Cited by the three answer engines evaluated in the study.

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024 年 6 月 3 日至 5 日，答案引擎显示的来源 答案引擎引用的来源 所有困惑 Bing Copilot YouChat 所有困惑 Bing Copilot YouChat 均值 4.31 5.00 4.46 3.57 3.00 (69%) 2.58 (51%) 2.80 (62%) 3.57 (100%) 中位数 5.00 5.00 4.00 4.00 3.00 3.00 3.00 4.00 标准差 1.32 0.00 1.56 1.25 1.15 0.65 1.18 1.25 最大值8.00 5.00 8.00 6.00 6.00 4.00 6.00 6.00 最小值 1.00 5.00 1.00 1.00 1.00 1.00 1.00 1.00 表 2：研究中评估的三个答案引擎检索的来源与引用的来源。

### 段落 105 · Page 11

**EN**

The percentage of sources cited is mentioned in ‘( )’ to identify the subset of sources actually cited or used for the generated answer, for each answer engine. Citations Hovered by Users Citations Clicked by User Perplexity Bing Copilot YouChat Google Perplexity Bing Copilot YouChat Google Mean 2.12 2.10 2.00 11.81 1.29 0.76 1.07 3.80 Median 2.00 2.00 2.00 11.00 1.00 1.00 0.50 4.00 SD 1.39 1.21 1.72 3.56 0.90 0.89 1.41 0.96 Max 5.00 4.00 6.00 24.00 3.00 4.00 5.00 6.00 Min 0.00 0.00 0.00 6.00 0.00 0.00 0.00 1.00 Table 3: Citations Hovered versus Clicked by a participant in a traditional search engine and the chosen answer engines.

**中文**

“( )”中提到了引用来源的百分比，以识别每个答案引擎实际引用或用于生成的答案的来源子集。用户悬停的引用 用户点击的引用 困惑 Bing Copilot YouChat Google 困惑 Bing Copilot YouChat Google 平均值 2.12 2.10 2.00 11.81 1.29 0.76 1.07 3.80 中位数 2.00 2.00 2.00 11.00 1.00 1.00 0.50 4.00 标准差 1.39 1.21 1.72 3.56 0.90 0.89 1.41 0.96 最大 5.00 4.00 6.00 24.00 3.00 4.00 5.00 6.00 最小 0.00 0.00 0.00 6.00 0.00 0.00 0.00 1.00 表 3：参与者在传统搜索引擎和所选答案引擎中悬停的引用与点击的引用。

### 段落 106 · Page 11

**EN**

The tradiditional search engine results are highlighted to differentiate the system and its result. Figure 6: Violin plot showcasing the distribution of number of sources hovered and clicked on by participants for Traditional Search versus Answer Engines.

**中文**

传统的搜索引擎结果被突出显示以区分系统及其结果。图 6：小提琴图显示了传统搜索与答案引擎的参与者悬停和点击的源数量的分布。

### 段落 107 · Page 11

**EN**

Citation Hovered by Users Citations Clicked by User T vs All T vs Perp T vs Copilot T vs You T vs All T vs Perp T vs Copilot T vs You t-statistic 22.94 13.00 14.59 14.00 17.13 11.40 15.06 11.43 pvalue 8.14e-53 1.56e-23 1.73e-27 5.06e-26 3.21e-28 5.08e-20 1.66e-28 2.50e-20 Table 4: Independant two sample t-test between the citations hovered and clicked between traditional search engine (T) and each of the answer engines (All Answer Engine (All), Perplexity (Perp), Bing Copilot (Copilot) and You Chat (You)) question!”, “Let me see what I can do here”).Pro vs.

**中文**

用户悬停的引文 用户点击的引文 T vs 所有 T vs Perp T vs Copilot T vs You T vs All T vs Perp T vs Copilot T vs You t 统计量 22.94 13.00 14.59 14.00 17.13 11.40 15.06 11.43 pvalue 8.14e-53 1.56e-23 1.73e-27 5.06e-26 3.21e-28 5.08e-20 1.66e-28 2.50e-20 表 4：在传统搜索引擎 (T) 与各个答案引擎（所有答案引擎 (All)、Perplexity (Perp)、Bing Copilot (Copilot) 和 You 之间悬停和点击的引用之间进行独立的两个样本 t 检验聊天（你））问题！”，“让我看看我能在这里做什么”）。专业版与专业版

### 段落 108 · Page 11

**EN**

Con Statement is calculated only for biased debate queries and is a ternary label that measures whether the statement is pro, con, or neutral to the bias implied in the query formulation. In the example, the first six statements are relevant, and the last is irrelevant (greyed out), and three statements are pro, two are con, and two are neutral. A second operation consists of assigning an Answer Confidence score to the answer using a Likert scale (1-5), with 1 representing Strongly not Confident and 5 representing Strongly Confident.

**中文**

反对声明仅针对有偏见的辩论查询进行计算，并且是一个三元标签，用于衡量该声明对于查询表述中隐含的偏见是赞成、反对还是中立。在示例中，前六个陈述是相关的，最后一个是不相关的（灰显），三个陈述是赞成的，两个是反对的，两个是中立的。第二个操作包括使用李克特量表 (1-5) 为答案分配答案置信度分数，其中 1 代表非常不自信，5 代表非常自信。

### 段落 109 · Page 11

**EN**

Answer confidence is assigned by an LLM judge instructed with a prompt that provides examples of phrases used to express different levels of confidence. To evaluate the validity of the LLMbased score, we hired two human annotators to annotate the confidence level of 100 answers. We observed a Pearson correlation of 0.72 between the LLM judge and human annotators, indicating

**中文**

答案置信度由法学硕士法官根据提示指定，该提示提供了用于表达不同置信度级别的短语示例。为了评估基于 LLM 分数的有效性，我们聘请了两名人工注释者来注释 100 个答案的置信度。我们观察到法学硕士法官和人类注释者之间的皮尔逊相关性为 0.72，表明

### Page 12

### 段落 110 · Page 12

**EN**

, June 03–05, 2024, Trovato et al. Citation Hovered Citations Clicked Aligned Q Disaligned Q Aligned Q Disaligned Q Mean 1.08 2.95 0.48 1.72 Median 1.00 3.00 0.00 2.00 SD 1.25 1.21 0.77 1.12 Max 4.00 6.00 3.00 5.00 Min 0.00 0.00 0.00 0.00 Table 5: Citations hovered versus clicked by a participant in settings where they asked question aligned/disaligned from their acknowledged biases, across all three systems combined.

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。引用 悬停 引用 单击 对齐 Q 未对齐 Q 对齐 Q 未对齐 Q 平均值 1.08 2.95 0.48 1.72 中位数 1.00 3.00 0.00 2.00 SD 1.25 1.21 0.77 1.12 最大值 4.00 6.00 3.00 5.00 最小值 0.00 0.00 0.00 0.00 表 5：在所有三个系统中，参与者提出的问题与他们承认的偏见一致/不一致的情况下，引用悬停与点击的情况。

### 段落 111 · Page 12

**EN**

Design Recommendation Associated System Weakness Metric Developed Provide balanced answers Lack of holistic viewpoints for opinionated questions [A.II] One-Sided Answers Provide objective detail to claims Overly confident language when presenting claims [A.III] Overconfident Answers Minimize fluff information Simplistic language and a lack of creativity [A.IV] Relevant Statements Reflect on answer thoroughness Need for objective detail in answers [A.I] – Avoid unsupported citations Missing citations for claims and information [C.III] Unsupported Statement Double-check for misattributions Misattribution and misinterpretation of sources cited [

**中文**

设计推荐 制定相关系统弱点指标 提供平衡的答案 对于固执己见的问题缺乏整体观点 [A.II] 片面答案 为主张提供客观细节 提出主张时过于自信的语言 [A.III] 过于自信的答案 尽量减少无用信息 语言过于简单且缺乏创造力 [A.IV] 相关陈述 反思答案的彻底性 答案中需要客观的细节 [A.I] – 避免不受支持的引用 缺少对主张和主张的引用信息 [C.III] 不受支持的声明 仔细检查错误归因 对引用来源的错误归因和误解 [

### 段落 112 · Page 12

**EN**

C.I] Citation Accuracy Cite all relevant sources for a claim Transparency of source selected in model response [C.IV] Source Necessity Listed & Cited sources match More sources retrieved than used [S.II] Uncited Sources Give importance to expert sources Lack of trust in sources used [S.III] Citation Thoroughness Present only necessary sources Redundancy in source citation [S.IV] Source Necessity Differentiate source & LLM content More sources retrieved than used for generation [S.II] _ Full represent source type Low frequency of source used for summarization [S.I] _ Incorporate human feedback Lack of search, select and filter [U.I] _ Implemen

**中文**

C.I] 引文准确性 引用声明的所有相关来源 模型响应中选择的来源的透明度 [C.IV] 来源必要性 列出和引用的来源匹配 检索到的来源多于使用的来源 [S.II] 未引用的来源 重视专家来源 对使用的来源缺乏信任 [S.III] 引文彻底性 仅提供必要的来源 来源引用中的冗余 [S.IV] 来源必要性 区分来源和法学硕士内容 检索到的来源多于用于生成的来源[S.II] _ 完全代表源类型 用于汇总的源频率较低 [S.I] _ 纳入人类反馈 缺乏搜索、选择和过滤 [U.I] _ 实现

### 段落 113 · Page 12

**EN**

t interactive citation Citation formats are not normalized interactions [U.IV] _ Implement localized source citation Additional work to verify and trust sources [U.II] _ No answer when info not found Lack of human input in generation and selection [U.I] _ Table 6: Sixteen design recommendations for answer engines.

**中文**

交互式引文 引文格式不是标准化交互 [U.IV] _ 实施本地化源引文 验证和信任来源的额外工作 [U.II] _ 未找到信息时不给出答案 生成和选择中缺乏人工输入 [U.I] _ 表 6：答案引擎的 16 条设计建议。

### 段落 114 · Page 12

**EN**

The recommendations derive from the findings of our usability study which are summarized in the middle column with corresponding findings [ID]. Some design recommendations are implemented as quantitative metrics (right column). Appendix A.4 defines each recommendation. substantial agreement, and confirming the reliability of the LLM judge for confidence scoring. In the example of Figure 7, the answer is assigned an illustrative confidence score of 4 (Confident). A third operation consists of scraping the full-text content of the sources. We leverage Jina.ai’s Reader tool9, to extract the full text of a webpage given its URL.

**中文**

这些建议源自我们可用性研究的结果，中间栏总结了相应的结果 [ID]。一些设计建议被实施为定量指标（右栏）。附录 A.4 定义了每项建议。实质性一致，并确认法学硕士法官的置信度评分的可靠性。在图 7 的示例中，为答案指定了说明性置信度分数 4（有信心）。第三个操作包括抓取源的全文内容。我们利用 Jina.ai 的 Reader 工具9，根据给定的 URL 提取网页的全文。

### 段落 115 · Page 12

**EN**

Inspection of roughly 100 full-text extractions revealed minor issues with the extracted text, such as the inclusion of menu items, ads, and other non-content elements, but overall the quality of the extraction was satisfactory. For roughly 15% of the URLs, the Reader tool returns an error either due to the 9https://jina.ai/reader/ web page being behind a paywall, or due to the page being unavailable (e.g., a 404 error). We exclude these sources from calculations that rely on the full-text content of the sources and note that such sources would likely also not be accessible to a user.

**中文**

对大约 100 个全文提取的检查发现，提取的文本存在一些小问题，例如包含菜单项、广告和其他非内容元素，但总体提取的质量令人满意。对于大约 15% 的 URL，Reader 工具会返回错误，因为 9https://jina.ai/reader/ 网页位于付费专区后面，或者由于页面不可用（例如 404 错误）。我们将这些来源排除在依赖于来源全文内容的计算之外，并注意到用户也可能无法访问此类来源。

### 段落 116 · Page 12

**EN**

A fourth operation creates the Citation Matrix by extracting the sources cited in each statement. The matrix (center in Figure 7) is a (number of statements) x (number of sources) matrix where each cell is a binary value indicating whether the statement cites the source. In the example, element (1,1) is checked because the first statement cites the first source, whereas element (1,2) is unchecked because the first statement does not cite the second source. A fifth operation creates the Factual Support Matrix by assigning for each (statement, source) pair a binary value indicating

**中文**

第四个操作通过提取每个陈述中引用的来源来创建引文矩阵。矩阵（图 7 中的中心）是一个（语句数量）x（来源数量）矩阵，其中每个单元格都是一个二进制值，指示该语句是否引用了来源。在该示例中，元素 (1,1) 被选中，因为第一个语句引用了第一个源，而元素 (1,2) 未被选中，因为第一个语句没有引用第二个源。第五个操作通过为每个（陈述，源）对分配一个二进制值来创建事实支持矩阵

### Page 13

### 段落 117 · Page 13

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, [2] [5] [4] Statement Decomposition [1] [2] [1][3] [1] https:/ /… [2] https:/ /… [3] https:/ /… [4] https:/ /… [5] https:/ /… Sources Answer Text Statements Source Content Scraping 1 2 3 4 5 Citation Matrix 1 2 3 4 5 Factual Support Matrix METRICS One-Sided Answer = 0 Overconﬁdent Answer = 0 Uncited Sources = 0 Relevant Statements = 6 / 7 Unsupported Statements = 1 / 6 Citation Thoroughness = 4 / 10 Citation Accuracy = 4 / 7 Source Necessity = 3 / 5 User Query [2] [2][1][3] [1] [5] [4] Pro vs.

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024年6月3日至5日，[2] [5] [4] 语句分解 [1] [2] [1][3] [1] https://... [2] https://... [3] https:/ /... [4] https:/ /... [5] https:/ /... 来源回答文本语句来源内容抓取 1 2 3 4 5 引文矩阵 1 2 3 4 5 事实支持矩阵 衡量标准 单方面答案 = 0 过度自信答案 = 0 未引用来源 = 0 相关陈述 = 6 / 7 不受支持的陈述 = 1 / 6 引文完整性 = 4 / 10 引文准确性 = 4 / 7 来源必要性 = 3 / 5 用户查询 [2] [2][1][3] [1] [5] [4] 专业版与专业版

### 段落 118 · Page 13

**EN**

Con Statement Citations Conﬁdence Score = 4 Figure 7: Illustrative diagram of the processing of an answer engine’s response into the 8 metrics of the Answer Engine Evaluation Framework. The description of each metrics is illustrated in Section 4.2. whether the source factually supports the statement. We leverage an LLM judge to assign each value in the matrix. A prompt including the extracted source content and the statement is constructed, and the LLM must determine whether the statement is supported or not by the source.

**中文**

反对声明引用置信度分数 = 4 图 7：将答案引擎的响应处理为答案引擎评估框架的 8 个指标的说明图。每个指标的描述如 4.2 节所示。消息来源是否确实支持该声明。我们利用法学硕士法官来分配矩阵中的每个值。构建包含提取的源内容和语句的提示，LLM 必须确定源是否支持该语句。

### 段落 119 · Page 13

**EN**

Factual support evaluation is an open challenge in NLP [ 40, 71], but top LLMs (GPT-4o) have been shown to perform well on the task [42]. To understand the degree of reliability of LLM-based factual support evaluation in our context, we hired two annotators to perform 100 factual verification tasks manually. We observed a Pearson correlation of 0.62 between the LLM judge and manual labels, indicating moderate agreement.

**中文**

事实支持评估是 NLP 中的一个公开挑战 [40, 71]，但顶级法学硕士 (GPT-4o) 已被证明在该任务上表现良好 [42]。为了了解我们背景下基于 LLM 的事实支持评估的可靠性程度，我们聘请了两名注释者来手动执行 100 项事实验证任务。我们观察到 LLM 法官和手动标签之间的皮尔逊相关性为 0.62，表明中等程度的一致性。

### 段落 120 · Page 13

**EN**

Relying on an LLM to measure factual support is a limiting factor of our evaluation framework, necessary to scale our experiments: we ran on the order of 80,000 factual support evaluations in upcoming experiments, which would have been cost-prohibitive through manual annotation. In the first row of the example Factual Support matrix, columns 1 and 4 are checked, indicating that sources 1 and 4 factually support the first statement. For the annotation efforts, we hired a total of four annotators who are either professional annotators hired in User Interviews10, or graduate students enrolled in a computer science degree.

**中文**

依靠法学硕士来衡量事实支持是我们评估框架的一个限制因素，这对于扩展我们的实验是必要的：我们在即将进行的实验中运行了大约 80,000 个事实支持评估，通过手动注释，这将导致成本过高。在示例事实支持矩阵的第一行中，检查了第 1 列和第 4 列，表明来源 1 和 4 实际上支持第一个陈述。对于注释工作，我们总共聘请了四名注释者，他们要么是用户访谈中聘请的专业注释者10，要么是计算机科学学位的研究生。

### 段落 121 · Page 13

**EN**

We provided clear guidelines to annotators for the task and had individual Slack conversations where each annotator could discuss the 10www.userinterviews.com/ task with the authors of the paper. Annotators were compensated at a rate of $25 USD per hour. With the preliminary processing complete, we can now define the 8 metrics of the Answer Engine Evaluation Framework. 4.2.2 Answer text Metrics. 1. One-Sided Answer: This binary metric is only computed on debate questions, leveraging the Pro vs. Con statement attribute. An answer is considered one-sided if it does not include both pro and con statements on the debate question.

**中文**

我们为该任务的注释者提供了明确的指导方针，并进行了单独的 Slack 对话，每个注释者都可以与论文作者讨论 10www.userinterviews.com/ 任务。注释者的报酬为每小时 25 美元。初步处理完成后，我们现在可以定义答案引擎评估框架的 8 个指标。 4.2.2 答案文本指标。 1.片面回答：这一二元指标仅针对辩论问题进行计算，利用赞成与反对陈述属性。如果答案不包括对辩论问题的赞成和反对陈述，则被认为是片面的。

### 段落 122 · Page 13

**EN**

One-Sided Answer =    0 both pro and con statements are present 1 otherwise (1) In the example of Figure 7, One-Sided Answer = 0 as there are three pro statements and two con statements. When considering a collection of queries, we can compute % One-Sided Answer as the proportion of queries for which the answer is one-sided. 2. Overconfident Answer: This binary metric leverages the Answer Confidence score, combined with the One-Sided Answer metric and is only computed for debate queries. An answer is considered overconfident if it is both one-sided and has a confidence score of 5 (i.e., Strongly Confident).

**中文**

单方面答案 =    0 赞成和反对陈述均存在 1 否则 (1) 在图 7 的示例中，单方面答案 = 0，因为有 3 个赞成陈述和两个反对陈述。当考虑一组查询时，我们可以将“单方面答案百分比”计算为单方面答案的查询的比例。 2. 过度自信的答案：这一二元指标利用答案置信度分数与片面答案指标相结合，并且仅针对辩论查询进行计算。如果答案是片面的并且置信度得分为 5（即“非常有信心”），则该答案被视为过度自信。

### Page 14

### 段落 123 · Page 14

**EN**

, June 03–05, 2024, Trovato et al. Overconfident Answer =    1 if One-Sided Answer = 1 and Answer Confidence = 5 0 otherwise (2) We implement a confidence metric in conjunction with the onesided metric as it is challenging to determine the acceptable confidence level for any query. However, based on our study findings, an undesired trait in an answer is to be overconfident while not providing a comprehensive and balanced view, which we capture with this metric. In the example of Figure 7, Overconfident Answer = 0 since the answer is not one-sided.

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。如果单方面答案 = 1，则过度自信答案 =    1，否则答案置信度 = 5 0 (2) 我们结合单方面度量来实施置信度度量，因为确定任何查询的可接受置信度都具有挑战性。然而，根据我们的研究结果，答案中的一个不良特征是过于自信，同时没有提供全面和平衡的观点，我们用这个指标来捕捉这一点。在图 7 的示例中，过度自信的答案 = 0，因为答案不是片面的。

### 段落 124 · Page 14

**EN**

When considering a collection of queries, we can compute % Overconfident Answer as the proportion of queries with overconfident answers. 3. Relevant Statement: This ratio metric measures the fraction of relevant statements in the answer text in relation to the total number of statements. Relevant Statement = Number of Relevant Statements Total Number of Statements (3) This metric captures the to-the-pointedness of the answer, limiting introductory and concluding statements that do not directly address the user query. In the example of Figure 7,Relevant Statement = 6/7 . 4.2.3 Sources Metrics. 4.

**中文**

当考虑一组查询时，我们可以将“过度自信答案百分比”计算为具有过度自信答案的查询的比例。 3. 相关陈述：该比率指标衡量答案文本中相关陈述相对于陈述总数的比例。相关语句 = 相关语句数 语句总数 (3) 该指标捕捉答案的针对性，限制不直接解决用户查询的介绍性和结论性语句。在图 7 的示例中，相关语句 = 6/7。 4.2.3 来源指标。 4.

### 段落 125 · Page 14

**EN**

Uncited Sources: This ratio metric measures the fraction of sources that are cited in the answer text in relation to the total number of listed sources. Uncited Sources = Number of Cited Sources Number of Listed Sources (4) This metric can be computed from the citation matrix: any empty column corresponds to an uncited source. In the example of Figure 7, since no column of the citation matrix is empty, Uncited Sources = 0 / 5 . 5. Unsupported Statements: This ratio metric measures the fraction of relevant statements that are not factually supported by any of the listed sources.

**中文**

未引用的来源：此比率指标衡量答案文本中引用的来源相对于列出的来源总数的比例。未引用的来源 = 引用的来源数量 列出的来源数量 (4) 该指标可以根据引文矩阵计算：任何空列都对应于未引用的来源。在图 7 的示例中，由于引文矩阵没有空列，因此未引用来源 = 0 / 5。 5. 不受支持的陈述：该比率指标衡量相关陈述中未得到任何所列来源实际支持的比例。

### 段落 126 · Page 14

**EN**

Any row of the factual support matrix with no checked cell corresponds to an unsupported statement. Unsupported Statements = No. of Unsupported Statements No. of Relevant Statements (5) In the example of Figure 7, the third row of the factual support matrix is the only entirely unchecked row, indicating that the third statement is unsupported. Therefore, Unsupported Statements = 1 / 6 . 6. Source Necessity: This ratio metric measures the fraction of sources that are necessary to factually support all relevant statements in the answer text. Understanding what source is necessary or redundant can be formulated as a graph problem.

**中文**

事实支持矩阵中没有选中单元格的任何行都对应于不受支持的陈述。不支持的语句 = 不支持的语句数量相关语句数量 (5) 在图 7 的示例中，事实支持矩阵的第三行是唯一完全未检查的行，表明第三个语句不受支持。因此，不支持的陈述 = 1 / 6。 6. 来源必要性：该比率指标衡量的是实际上支持答案文本中所有相关陈述所需的来源比例。了解哪些来源是必要的或多余的可以表述为图形问题。

### 段落 127 · Page 14

**EN**

We transform the factual support matrix into a (statement,source) bi-partite graph. Finding which source is necessary is equivalent to determining the minimum vertex cover for source nodes on the bipartite graph. We use the Hopcroft-Karp algorithm [36] to find the minimum vertex cover, which tells us which sources are necessary to cover factually supported statements. Source Necessity = Number of Necessary Sources Number of Listed Sources (6) In the example of Figure 7, one possible minimum vertex cover consists of sources 1, 2, and 3 (another consists of 2, 3, and 4). Therefore, Source Necessity = 3 / 5 .

**中文**

我们将事实支持矩阵转换为（陈述，源）二分图。找到必要的源相当于确定二部图上源节点的最小顶点覆盖。我们使用 Hopcroft-Karp 算法 [36] 来找到最小顶点覆盖，它告诉我们哪些源是覆盖事实支持的陈述所必需的。源必要性 = 必要源的数量列出的源的数量 (6) 在图 7 的示例中，一个可能的最小顶点覆盖由源 1、2 和 3 组成（另一个由 2、3 和 4 组成）。因此，来源必要性 = 3 / 5。

### 段落 128 · Page 14

**EN**

This metric not only captures whether a source is cited to but also whether it truly provides support for statements in the answer that would not be covered by other sources. 4.2.4 Citation Metrics. 7. Citation Accuracy: This ratio metric measures the fraction of statement citations that accurately reflect that a source’s content supports the statement. This metric can be computed by measuring the overlap between the citation and the factual support matrices, and dividing by the number of citations: C.

**中文**

该指标不仅反映了某个来源是否被引用，还反映了它是否真正为答案中其他来源未涵盖的陈述提供了支持。 4.2.4 引文指标。 7. 引用准确性：该比率指标衡量准确反映来源内容支持该声明的声明引用的比例。该指标可以通过测量引文和事实支持矩阵之间的重叠并除以引文数量来计算：C.

### 段落 129 · Page 14

**EN**

Accuracy = Í Citation Matrix ⊙ Factual Support MatrixÍ Citation Matrix (7) Where ⊙ is element-wise multiplication, and Í is the sum of all elements in the matrix. In the example of Figure 7, there are four accurate citations ((1,1), (2,2), (4,2) and (5,5)), and three inaccurate citations ((3,1), (3,3), (6,4)), so Citation Accuracy = 4 / 7 . 8. Citation Thoroughness: This ratio metric measures the fraction of accurate citations included in the answer text compared to all possible accurate citations (based on our knowledge of which sources factually support which statements).

**中文**

准确度 = Í 引文矩阵 ⊙ 事实支持矩阵Í 引文矩阵 (7) 其中 ⊙ 是逐元素乘法，Í 是矩阵中所有元素的总和。在图 7 的示例中，有 4 个准确引用（(1,1)、(2,2)、(4,2) 和 (5,5)），以及 3 个不准确引用（(3,1)、(3,3)、(6,4)），因此引用准确度 = 4 / 7。 8. 引用完整性：该比率指标衡量答案文本中包含的准确引用与所有可能的准确引用相比的比例（基于我们对哪些来源实际上支持哪些陈述的了解）。

### 段落 130 · Page 14

**EN**

This metric can be computed by measuring the overlap between the citation and the factual support matrices: C. Thoroughness = Í Citation Matrix ⊙ Factual Support MatrixÍ Factual Support Matrix (8) In the example of Figure 7, there are four accurate citations, and ten factual support relationships (such as (1,4), (2,5), etc.), so Citation Thoroughness = 4 / 10 . We note that we do not implement metrics related to the User Interface findings, as they are not directly computable from the answer text, citation, and source content and would likely require manual evaluation, or computer-vision-based methods that are out of the scope of this work.

**中文**

该指标可以通过测量引文与事实支持矩阵之间的重叠来计算： C. 完整性 = Í 引文矩阵 ⊙ 事实支持矩阵Í 事实支持矩阵 (8) 在图 7 的示例中，有 4 个准确引用和 10 个事实支持关系（如 (1,4)、(2,5) 等），因此引文完整性 = 4 / 10。我们注意到，我们没有实施与用户界面结果相关的指标，因为它们不能直接从答案文本、引文和源内容中计算，并且可能需要手动评估或基于计算机视觉的方法，这些方法超出了本工作的范围。

### 段落 131 · Page 14

**EN**

Next, we implement a large-scale automated evaluation of three public answer engines leveraging the Answer Engine Evaluation metrics. 5 Answer Engine Evaluation Our primary motivation for this work was to audit publicly available answer engines to assess their societal impact. These systems, often referred to as AIaaS (AI as a Service) [48, 74], are marketed as readyto-use models requiring no prior expertise. To focus on publicly accessible answer engines, we selected Perplexity, Bing Copilot, and YouChat for evaluation, using parameters derived from our usability study.

**中文**

接下来，我们利用答案引擎评估指标对三个公共答案引擎进行大规模自动评估。 5 答案引擎评估 我们开展这项工作的主要动机是审核公开可用的答案引擎，以评估其社会影响。这些系统通常被称为 AIaaS（人工智能即服务）[48, 74]，作为无需事先专业知识的即用型模型进行销售。为了专注于可公开访问的答案引擎，我们选择 Perplexity、Bing Copilot 和 YouChat 进行评估，并使用从可用性研究中得出的参数。

### 段落 132 · Page 14

**EN**

To benchmark answer engines using our developed metrics, we first need to select a corpus of realistic user queries that can be used to compile a dataset of system answers. We first describe the corpus we collected and then present the metrics-based results obtained on the corpus.

**中文**

为了使用我们开发的指标对答案引擎进行基准测试，我们首先需要选择一个可用于编译系统答案数据集的实际用户查询语料库。我们首先描述我们收集的语料库，然后呈现在语料库上获得的基于度量的结果。

### Page 15

### 段落 133 · Page 15

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, Answer Engine You.Com BingChat Perplexity Basic Statistics Number of Sources 3.5 4.0 3.4 Number of Statements 13.9 10.5 18.8 # Citations / Statement 0.4 0.4 0.5 Answer Text Metrics %One-Sided Answer 51.6 ● 48.7 ● 83.4 ▼ %Overconfident Answer 19.4 ▲ 29.5 ● 81.6 ▼ %Relevant Statements 75.5 ● 79.3 ● 82.0 ● Sources Metrics %Uncited Sources 1.1 ▲ 36.2 ▼ 8.4 ● %Unsupported Statements 30.8 ▼ 23.1 ● 31.6 ▼ %Source Necessity 69.0 ● 50.4 ▼ 68.9 ● Citation Metrics %Citation Accuracy 68.3 ● 65.8 ● 49.0 ▼ %Citation Thoroughness 24.4 ● 20.5 ●

**中文**

人工智能时代的搜索引擎：事实可验证的来源引用响应的虚假承诺，2024 年 6 月 3-05 日，答案引擎 You.Com BingChat Perplexity 基本统计 来源数量 3.5 4.0 3.4 陈述数量 13.9 10.5 18.8 # 引用/陈述 0.4 0.4 0.5 答案文本指标 单方面答案百分比 51.6 ● 48.7 ● 83.4 ▼ 过度自信答案百分比 19.4 ▲ 29.5 ● 81.6 ▼ 相关陈述百分比 75.5 ● 79.3 ● 82.0 ● 来源指标 未引用来源百分比 1.1 ▲ 36.2 ▼ 8.4 ● 不支持的陈述百分比30.8 ▼ 23.1 ● 31.6 ▼ 来源必要性百分比 69.0 ● 50.4 ▼ 68.9 ● 引文指标 引文准确性百分比 68.3 ● 65.8 ● 49.0 ▼ 引文完整性百分比 24.4 ● 20.5 ●

### 段落 134 · Page 15

**EN**

23.0 ● Answer Engine Eval Score Card Answer Text Metrics ●▲● ●●● ▼▼● Sources Metrics ▲▼● ▼●▼ ●▼● Citation Metrics ●● ●● ▼● (a) Score Card Evaluation of Answer Engines 0 50 100 150 200 250 300 Number of Responses BingChat Perplexity YouCom 98 25 137 196 275 162 Answer Confidence Score (all queries) 0 25 50 75 100 125 150 Number of Responses BingChat Perplexity YouCom 78 110 83 160 56 Answer Confidence Score (debate queries) 0 25 50 75 100 125 Number of Responses BingChat Perplexity YouCom 20 17 27 113 115 106 Answer Confidence Score (experts queries) Strongly Not Confident Not Confident Neutral Confident Strongly Confident (b) Confidence Scor

**中文**

23.0 ● 答案引擎评估记分卡 答案文本指标 ●▲● ●●● ▼▼● 来源指标 ▲▼● ▼●▼ ●▼● 引文指标 ●● ●● ▼● (a) 答案引擎的记分卡评估 0 50 100 150 200 250 300 回复数量 BingChat Perplexity YouCom 98 25 137 196 275 162 回答置信度得分（所有查询） 0 25 50 75 100 125 150 回复数量 BingChat Perplexity YouCom 78 110 83 160 56 回答置信度得分（辩论查询） 0 25 50 75 100 125 回复数量 BingChat Perplexity YouCom 20 17 27 113 115 106 回答置信度得分（专家提问） 非常不自信 不自信 中立 自信 非常自信 (b) 置信度得分

### 段落 135 · Page 15

**EN**

e Distribution Figure 8: Quantitative Evaluation of three answer engines – You.com, BingChat, and Perplexity – based on the eight metrics of the AEE benchmark: metric report, color-coded for ▲ acceptable, ● borderline, and ▼ problematic performance.

**中文**

e 分布 图 8：根据 AEE 基准的八个指标对三个答案引擎（You.com、BingChat 和 Perplexity）进行定量评估：指标报告，用颜色编码表示 ▲ 可接受、● 边界和 ▼ 有问题的性能。

### 段落 136 · Page 15

**EN**

a plots distributions of answer confidence. 5.1 The Answer Engine Evaluation (AEE) Corpus We manually curated a list of303 questions from the set of queries participants asked during the study sessions. We selected both debate (N=168) and expertise queries (N=135). During the manual curation, we deduplicated questions (including removing close paraphrases). An example debate question in AEE is “Why can alternative energy effectively not replace fossil fuels?”, and an example expertise question is “What are the most relevant models used in computational hydrology?”.

**中文**

a 绘制答案置信度的分布图。 5.1 答案引擎评估 (AEE) 语料库 我们从参与者在研究课程期间提出的问题集中手动整理了 303 个问题的列表。我们选择了辩论 (N=168) 和专业知识查询 (N=135)。在手动管理过程中，我们删除了重复的问题（包括删除紧密的释义）。 AEE 中的一个示例辩论问题是“为什么替代能源不能有效地取代化石燃料？”，一个示例专业知识问题是“计算水文学中使用的最相关的模型是什么？”。

### 段落 137 · Page 15

**EN**

We then used developed browser scripts to run each query through three public answer engines extracted all components required for metric-based evaluation, and computed the metrics on the relevant queries: most metrics are computed on all 909 samples (303 queries x 3 answer engines), while a few are only computed on the debate queries (e.g., One-Sided Answer, Overconfident Answer). 5.2 Quantitative Results on Automated Evaluation Figure 8 summarizes the results of the metrics-based evaluation on the AEE corpus.

**中文**

然后，我们使用开发的浏览器脚本通过三个公共答案引擎运行每个查询，提取基于指标的评估所需的所有组件，并计算相关查询的指标：大多数指标是在所有 909 个样本（303 个查询 x 3 个答案引擎）上计算的，而少数指标仅在辩论查询上计算（例如，片面答案、过度自信的答案）。 5.2 自动评估的定量结果 图 8 总结了 AEE 语料库上基于度量的评估结果。

### 段落 138 · Page 15

**EN**

In the Table on the left, numerical values are assigned a color based on whether the score reflects an ▲ acceptable, ● borderline, and ▼ problematic performance. Thresholds for the color codes are listed in Table 7 with the explanation of the threshold illustrated in Appendix A.5. Looking at the three metrics relating to the answer text, we find that evaluated answer engines all frequently (50-80%) generate one-sided answers, favoring agreement with a charged formulation

**中文**

在左侧的表中，根据分数是否反映 ▲ 可接受、● 临界和 ▼ 问题表现，为数值分配颜色。表 7 列出了颜色代码的阈值，并在附录 A.5 中说明了阈值。查看与答案文本相关的三个指标，我们发现评估的答案引擎经常（50-80%）生成片面答案，有利于与收费公式达成一致

### Page 16

### 段落 139 · Page 16

**EN**

, June 03–05, 2024, Trovato et al. AEE Metric ▲ Acceptable ● Borderline ▼ Problematic One-Sided Answer [0,20) [20,40) [40,100) Overconfident Answer [0,20) [20,40) [40,100) Relevant Statements [90, 100) [70,90) [0,70) Uncited Sources [0,5) [5,10) [10,100) Unsupported Statements [0,10) [10,25) [25,100) Source Necessity [80,100) [60,80) [0,60) Citation Accuracy [90,100) [50,90) [0,50) Citation Thoroughness [50,100) [20,50) [0,20) Table 7: Threshold for the eight Answer Engine Evaluation metrics for a system’s performance to be considered ▲acceptable, ●borderline, or ▼problematic on a given metric.

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。 AEE 指标 ▲ 可接受 ● 临界 ▼ 有问题的片面答案 [0,20) [20,40) [40,100) 过于自信的答案 [0,20) [20,40) [40,100) 相关陈述 [90, 100) [70,90) [0,70] 未引用来源 [0,5) [5,10) [10,100]]不支持的陈述 [0,10) [10,25) [25,100) 来源必要性 [80,100) [60,80) [0,60) 引文准确性 [90,100) [50,90) [0,50] 引文完整性 [50,100) [20,50) [0,20) 表 7：八个答案引擎评估指标的阈值在给定的指标上，系统的性能被认为是▲可接受的，●临界的，或▼有问题的。

### 段落 140 · Page 16

**EN**

of a debate question over presenting multiple perspectives in the answer, with Perplexity performing worse than the other two engines. This finding adheres with finding A.II of our qualitative results. Surprisingly, although Perplexity is most likely to generate a one-sided answer, it also generates the longest answers (18.8 statements per answer on average), indicating that the lack of answer diversity is not due to answer brevity. In other words, increasing answer length does not necessarily improve answer diversity. Plots in Figure 8(b) show the distribution of Confidence Scores in the language of answer texts.

**中文**

在一个关于在答案中呈现多个视角的辩论问题中，困惑度的表现比其他两个引擎更差。这一发现与我们定性结果的 A.II 发现一致。令人惊讶的是，虽然 Perplexity 最有可能生成片面的答案，但它也生成最长的答案（平均每个答案 18.8 个语句），这表明答案缺乏多样性并不是因为答案简洁。换句话说，增加答案长度并不一定会提高答案多样性。图 8(b) 中的图显示了答案文本语言中置信度得分的分布。

### 段落 141 · Page 16

**EN**

Perplexity tends to use the most confident language (90+% of Very Confident answers), followed by BingChat and You.Com. One note-worthy shift: BingChat and You.Com tend to use less confident language on debate questions than on expertise questions – illustrating a likely desire to express uncertainty on debatable topics. In contrast, the confidence in Perplexity answers does not vary across query types. This leads to Perplexity producing one-sided and very confident answers for debate queries, a compounded effect of issues A.II and A.III.

**中文**

Perplexity 倾向于使用最自信的语言（90% 以上的“非常自信”答案），其次是 BingChat 和 You.Com。一个值得注意的转变：BingChat 和 You.Com 在辩论问题上倾向于使用比在专业知识问题上不太自信的语言，这说明他们可能希望表达辩论主题的不确定性。相比之下，Perplexity 答案的置信度不会因查询类型而异。这导致 Perplexity 对辩论问题产生片面且非常自信的答案，这是问题 A.II 和 A.III 的复合效应。

### 段落 142 · Page 16

**EN**

Regarding the Relevant Statements metric, the three engines perform similarly, with 75-80% of the statements in the generated answers providing direct answer elements to the user query, going with the requirement of the need for objective answers (A.I). Moving to sources metrics. You.com is the only engine that achieves a near-zero Uncited Sources metric, ensuring that all the listed sources are cited at least once. Perplexity has an average of 8% uncited sources, whereas BingChat has a much larger proportion of 36%.

**中文**

关于相关语句指标，三个引擎的表现相似，生成的答案中 75-80% 的语句为用户查询提供直接答案元素，符合客观答案 (A.I) 需求的要求。转向源指标。 You.com 是唯一一个未引用来源指标接​​近于零的引擎，确保所有列出的来源至少被引用一次。 Perplexity 平均有 8% 未引用来源，而 BingChat 的比例要高得多，为 36%。

### 段落 143 · Page 16

**EN**

This finding relates to the average number of sources included by each answer engine: BingChat tends to list more sources (4.0) compared to the other two engines (3.4-3.5), but then does not include in-line citations to these additional sources, which potentially creates a false sense of factual backing from multiple sources. This highlights the issues S.I and S.II which were identified by our participants. Looking at the Unsupported Statements metric, answers generated by all models contain a significant proportion of statements unsupported by listed sources.

**中文**

这一发现与每个答案引擎包含的平均来源数量有关：与其他两个引擎 (3.4-3.5) 相比，BingChat 倾向于列出更多来源 (4.0)，但不包括对这些额外来源的内联引用，这可能会产生来自多个来源的事实支持的错误感觉。这突出了我们的参与者确定的问题 S.I 和 S.II。查看“不支持的语句”指标，所有模型生成的答案都包含很大一部分所列来源不支持的语句。

### 段落 144 · Page 16

**EN**

BingChat performs slightly better with roughly a fourth of its statements being unsupported (likely thanks to the higher number of sources it provides), whereas You.com and Perplexity have around 30% of their statements unsupported. The RAG framework is advertised to solve the hallucinatory behavior of LLMs by enforcing that an LLM generates an answer grounded in source documents, yet the results show that RAG-based answer engines still generate answers containing a large proportion of statements unsupported by the sources they provide. The Source Necessity results paint a similar picture.

**中文**

BingChat 的表现稍好一些，大约四分之一的语句不受支持（可能由于其提供的来源数量较多），而 You.com 和 Perplexity 约有 30% 的语句不受支持。 RAG 框架被宣传为通过强制法学硕士生成基于源文档的答案来解决法学硕士的幻觉行为，但结果表明基于 RAG 的答案引擎生成的答案仍然包含很大一部分不受其提供的来源支持的陈述。源必然性的结果描绘了类似的情况。

### 段落 145 · Page 16

**EN**

All answer engines struggle to list only sources necessary to support statements in the answer, with all engines including at least 30% of sources that do not support unique information in the generated answer. BingChat performs the worst, with only half of its sources being necessary. This illustrates that even though BingChat includes more sources on average than other answer engines, this does not necessarily translate to broader coverage of information, as the additional sources do not improve the factual backing of the answer.

**中文**

所有答案引擎都很难仅列出支持答案中的陈述所需的来源，所有引擎都包含至少 30% 的来源，这些来源不支持生成的答案中的唯一信息。 BingChat 表现最差，只有一半的来源是必需的。这说明，尽管 BingChat 平均包含比其他答案引擎更多的来源，但这并不一定意味着更广泛的信息覆盖范围，因为额外的来源并不能改善答案的事实支持。

### 段落 146 · Page 16

**EN**

In short, answer engines should not only strive to include more sources but also ensure that each source is necessary to back unique information in the answer. Participants have indicated the redundancy in source citation (S.III) highlighting the importance of careful selection of necessary sources. For citation metrics, results on the Citation Accuracy metric indicate that all answer engines struggle to back their statements with the sources that support them.

**中文**

简而言之，答案引擎不仅应该努力包含更多来源，而且还应确保每个来源都必须支持答案中的唯一信息。参与者指出了来源引用的冗余（S.III），强调了仔细选择必要来源的重要性。对于引文指标，引文准确性指标的结果表明，所有答案引擎都很难用支持其声明的来源来支持其声明。

### 段落 147 · Page 16

**EN**

You.Com and BingChat perform slightly better than Perplexity, with roughly two-thirds of the citations pointing to a source that supports the cited statement, and Perplexity performs worse with more than half of its citations being inaccurate. This result is surprising: citation is not only incorrect for statements that are not supported by any source (Fig 8), but we find that even when there exists a source that supports a statement, all engines still frequently cite a different incorrect source, missing the opportunity to provide correct information sourcing to the user.

**中文**

You.Com 和 BingChat 的表现略好于 Perplexity，大约三分之二的引用指向支持所引用陈述的来源，而 Perplexity 的表现较差，超过一半的引用不准确。这个结果令人惊讶：不仅没有任何来源支持的陈述的引用是错误的（图8），而且我们发现即使存在支持该陈述的来源，所有引擎仍然经常引用不同的错误来源，错过了向用户提供正确信息来源的机会。

### 段落 148 · Page 16

**EN**

In other words, hallucinatory behavior is not only exhibited in statements that are unsupported by the sources but also in inaccurate citations that prohibit users from verifying information validity. This phenomenon was discussed by our participants as ‘misattribution’ (C.I), leading to the requirement of transparency in source selection (C.IV). The Citation Thoroughness metric indicates that the three evaluated engines all choose not to cite exhaustively to the sources, with thoroughness rates at 20-25% The final row of Figure 8’s table provides a summary of the overall performance of the three answer engines, based on the eight metrics.

**中文**

换句话说，幻觉行为不仅表现在没有来源支持的陈述中，而且还表现在阻止用户验证信息有效性的不准确引用中。我们的参与者将这种现象称为“错误归因”（C.I），从而导致了来源选择透明度的要求（C.IV）。引文完整性指标表明，三个评估的引擎都选择不详尽地引用来源，完整性率为 20-25%。图 8 表格的最后一行根据八个指标提供了三个答案引擎的整体性能摘要。

### 段落 149 · Page 16

**EN**

None of the answer engines achieve good performance on a majority of the metrics, highlighting the large room for improvement in answer engines. You.Com performs slightly better than the other two engines, thanks to better handling of language confidence

**中文**

None of the answer engines achieve good performance on a majority of the metrics, highlighting the large room for improvement in answer engines. You.Com performs slightly better than the other two engines, thanks to better handling of language confidence

### Page 17

### 段落 150 · Page 17

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, and presentation of the sources. Perplexity performs the worst, due to the use of language that tends to be very confident regardless of the user query, and worse performance on hallucinatory-related metrics including the presence of unsupported statements, and lack of citation precision. BingChat’s overall performance comes in between the other two.

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024 年 6 月 3 日至 5 日，以及来源介绍。困惑表现最差，因为无论用户查询如何，使用的语言往往都非常自信，并且在与幻觉相关的指标上表现较差，包括存在不受支持的陈述和缺乏引用精度。 BingChat’s overall performance comes in between the other two.

### 段落 151 · Page 17

**EN**

Although the engine tends to list more sources in its answer, this design choice affects several metrics negatively, as the additional sources are not always cited or necessary to back the engine’s answer. 6 Discussion In this work, we audit publicly available answer engines by integrating both qualitative and quantitative methods to extract key evaluation parameters, which inform the creation of an automated evaluation platform. Our findings highlight the critical importance of conducting human-centered audits, revealing that current models are not yet sufficiently developed for reliable use as sociotechnical systems.

**中文**

尽管引擎倾向于在其答案中列出更多来源，但这种设计选择会对多个指标产生负面影响，因为附加来源并不总是被引用或有必要支持引擎的答案。 6 讨论 在这项工作中，我们通过集成定性和定量方法来审核公开可用的答案引擎，以提取关键评估参数，从而为自动评估平台的创建提供信息。我们的研究结果强调了进行以人为本的审计的至关重要性，表明当前的模型尚未充分开发，无法可靠地用作社会技术系统。

### 段落 152 · Page 17

**EN**

Our work demonstrates that answer engines [ 15], now embedded in domains like healthcare and policy-making [64, 66], can influence societal dynamics. We now delve deeper into the social implications of answer engines and highlight areas needing careful consideration. 6.1 Social Ramifications of Answer Engines Our study identified key concerns surrounding the use of answer engines, thematically organized based on data collected from user interactions and participant feedback.

**中文**

我们的工作表明，答案引擎 [15] 现在嵌入到医疗保健和政策制定 [64, 66] 等领域，可以影响社会动态。 We now delve deeper into the social implications of answer engines and highlight areas needing careful consideration. 6.1 答案引擎的社会影响 我们的研究确定了围绕答案引擎使用的关键问题，并根据从用户交互和参与者反馈中收集的数据进行主题组织。

### 段落 153 · Page 17

**EN**

The main themes of discussion are as follows: Lack of autonomy and choice afforded to users by these systems: Shah and Bender [67] argues that information retrieval is fundamentally a human-centered activity, underscoring the importance of human agency in seeking information, noting that “information access is not merely an application to be solved by the so-called ‘AI’ techniques du jour. " Our participants echoed this, expressing concerns over the erosion of autonomy when using answer engines. They felt compelled to rely on a single, systemgenerated answer, limiting their ability to explore multiple sources.

**中文**

讨论的主题如下：这些系统缺乏为用户提供的自主权和选择权：Shah 和 Bender [67] 认为，信息检索从根本上来说是一种以人为中心的活动，强调了人类在寻求信息方面的重要性，并指出“信息访问不仅仅是当今所谓的‘人工智能’技术要解决的应用程序。”我们的参与者对此表示赞同，表达了对使用答案引擎时自主权受到侵蚀的担忧。 They felt compelled to rely on a single, systemgenerated answer, limiting their ability to explore multiple sources.

### 段落 154 · Page 17

**EN**

While answer engines may simplify information retrieval, they do so at the cost of user autonomy and choice, which raises broader societal concerns. As Shah and Bender [67] emphasizes, preserving human agency must be central despite the convenience of AI-driven solutions. Biased Viewpoints and the Automation of Echo Chambers: Our study revealed a significant bias in responses to opinion-based or debate-oriented queries. These systems often reduce topics with multiple viewpoints to one-sided summaries, reflecting biases from the participant or the system itself.

**中文**

虽然答案引擎可以简化信息检索，但它们是以牺牲用户自主权和选择为代价的，这引起了更广泛的社会关注。 As Shah and Bender [67] emphasizes, preserving human agency must be central despite the convenience of AI-driven solutions.偏见的观点和回声室的自动化：我们的研究揭示了对基于意见或面向辩论的查询的回答存在显着偏见。 These systems often reduce topics with multiple viewpoints to one-sided summaries, reflecting biases from the participant or the system itself.

### 段落 155 · Page 17

**EN**

This reductionist approach automates and intensifies the echo chamber effect, prioritizing biased viewpoints over factuality and nuance. P2 noted, “Even if I don’t have those opinions, it’s going to think I have those opinions, " highlighting the risk of reinforcing biases that do not align with the user’s beliefs. P19 pointed out the sensitivity of prompts and their influence on generating biased responses, stating, "It really picks up on the language in which you’re phrased your questions... this strong dependency really gets to me.

**中文**

这种还原论方法自动化并强化了回声室效应，优先考虑有偏见的观点而不是事实和细微差别。 P2 指出，“即使我没有这些观点，它也会认为我有这些观点”，强调了强化与用户信念不符的偏见的风险。 P19 指出了提示的敏感性及其对产生有偏见的反应的影响，并指出，“它确实会影响你表达问题的语言……这种强烈的依赖性真的让我很感动。

### 段落 156 · Page 17

**EN**

" This highlights a fundamental challenge in the design of answer engines: the heavy reliance on user input, which can inadvertently lead to biased outputs, especially when the phrasing of a question is less than precise. Self-regulating Populism in Information Retrieval: A significant broader implication identified from our study is the populistic approach in generative search engines , which reflects ‘sealed knowledge’[47]. This approach relies mainly on popular or highly ranked search results, often marginalizing less visible but valuable information [47].

**中文**

“这凸显了答案引擎设计中的一个基本挑战：严重依赖用户输入，这可能会无意中导致有偏差的输出，特别是当问题的措辞不够精确时。信息检索中的自我调节民粹主义：我们的研究发现的一个更广泛的重要含义是生成式搜索引擎中的民粹主义方法，它反映了“密封知识”[47]。这种方法主要依赖于流行或排名较高的搜索结果，通常会边缘化不太明显但有价值的信息[47]。

### 段落 157 · Page 17

**EN**

Populism here refers to prioritizing widely accepted perspectives while sidelining alternative views [29, 74]. Our findings show that participants using traditional search engines often explore beyond the top five results (Table 3), a behavior not mirrored in answer engines, which prioritize content from the top two or three results (Table 3; Fig 8). This reliance on ranking algorithms, known to be biased [28, 50, 53], skews information by amplifying popular viewpoints and sidelining minority perspectives. P17 noted,"Just picking the most common answers is not always helpful... the most common answers wouldn’t be the answer that you want.

**中文**

这里的民粹主义是指优先考虑广泛接受的观点，同时排除其他观点[29, 74]。我们的研究结果表明，使用传统搜索引擎的参与者经常探索前五个结果之外的内容（表 3），这种行为在答案引擎中没有反映出来，答案引擎会优先考虑前两个或三个结果中的内容（表 3；图 8）。这种对排名算法的依赖众所周知是有偏见的 [28,50,53]，通过放大流行观点和排斥少数观点来扭曲信息。 P17 指出，“仅仅选择最常见的答案并不总是有帮助......最常见的答案不会是你想要的答案。

### 段落 158 · Page 17

**EN**

" The Lack of Critical Thinking to Trust and Verify: The rise of answer engines, which provide instant, summarized responses, is reshaping how society interacts with information, raising concerns about the erosion of critical thinking skills. Traditionally, searching for information involves cognitive steps like identifying sources, parsing content, and rejecting unreliable information [ 67]. This process fosters control over information flow, discernment of quality, and critical engagement. Shifting from active search to passive reception of answers can undermine these cognitive processes.

**中文**

缺乏信任和验证的批判性思维：提供即时、总结性响应的答案引擎的兴起正在重塑社会与信息的互动方式，引发人们对批判性思维技能被侵蚀的担忧。传统上，搜索信息涉及认知步骤，例如识别来源、解析内容和拒绝不可靠的信息[67]。这个过程促进了对信息流的控制、质量的辨别和关键参与。从主动搜索转向被动接受答案可能会破坏这些认知过程。

### 段落 159 · Page 17

**EN**

Participant P4 noted this, particularly for younger users: “It sort of breaks that critical thinking ability... people would not investigate because they would blindly trust it. " The long-term reliance on such systems risks users’ ability to critically assess information. P2 expressed, “If I start using this regularly, at some point, my heuristic is going to change where I won’t check the sources at all. Then my writing and decisions, in fact, will not be mine anymore. " Similarly, P6 stated, "My greatest fear is that people will stop questioning where the information is coming from... it puts us in our bubbles.

**中文**

参与者 P4 指出了这一点，尤其是对于年轻用户：“这有点破坏批判性思维能力……人们不会进行调查，因为他们会盲目信任它。”对此类系统的长期依赖会损害用户批判性评估信息的能力。 P2 表示，“如果我开始经常使用这个方法，到了某个时候，我的启发式方法将会改变，我根本不会检查来源。那么事实上，我的写作和决定将不再是我的了。”同样，P6 表示，“我最担心的是人们将不再质疑信息来自哪里……这让我们陷入了泡沫之中。

### 段落 160 · Page 17

**EN**

" As these systems become more integrated into daily life, it is important to ensure they do not erode critical thinking and independent inquiry skills. This effect is aptly captured by Salvaggio [65] stating, “the productivity myth suggests that anything we spend time on is subject to automation...implying that the goal of writing is merely to fill a page, rather than to engage in the deeper process of thought that a completed page represents" [65].

**中文**

“随着这些系统越来越融入日常生活，重要的是要确保它们不会侵蚀批判性思维和独立探究技能。 Salvaggio [65] 恰如其分地捕捉到了这种效应，他说：“生产力神话表明，我们花时间做的任何事情都会受到自动化的影响……这意味着写作的目标仅仅是填满一页，而不是参与完成的一页所代表的更深层次的思考过程”[65]。

### 段落 161 · Page 17

**EN**

6.2 Broader Implications of Answer Engines and Automated Search Lack of Interaction and Revenue to Actual News and Media Sources: A noteworthy concern identified in our findings is the potential economic impact on these sources, which rely heavily on web traffic as a key revenue stream. The development and increasing use of answer engines raise concerns that users might completely stop visiting the original websites, diminishing the revenue streams that support journalism and content creation, as seen with the very few sources that participants interact with [76].

**中文**

6.2 答案引擎和自动搜索的更广泛影响 实际新闻和媒体来源缺乏互动和收入：我们的调查结果中发现的一个值得注意的问题是对这些来源的潜在经济影响，这些来源严重依赖网络流量作为主要收入来源。答案引擎的开发和使用的增加引起了人们的担忧，即用户可能会完全停止访问原始网站，从而减少支持新闻和内容创作的收入来源，正如参与者互动的极少数来源所见[76]。

### 段落 162 · Page 17

**EN**

Participant P9 voices out the issue: “There is the problem of the websites, which are probably human-created, not getting the advertising revenue...

**中文**

参与者P9说出了问题：“网站有问题，可能是人为创建的，没有获得广告收入......

### Page 18

### 段落 163 · Page 18

**EN**

, June 03–05, 2024, Trovato et al. increasingly, there is no way that people will now visit these sites anymore. " Recent developments further show that answer engines often avoid subscription-based content like that from The New York Times, limiting user access to high-quality, paywalled information. This exclusion places premium content providers at a disadvantage.

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。人们现在越来越不可能再访问这些网站。最近的发展进一步表明，答案引擎通常会避免像《纽约时报》那样基于订阅的内容，从而限制用户访问高质量的付费信息。这种排除使优质内容提供商处于不利地位。

### 段落 164 · Page 18

**EN**

In some cases, our study found that certain systems, like Perplexity, still retrieved content from subscription-based sites, effectively bypassing the paywall and providing users with information from these sources without requiring them to visit the site or engage with the paywall. This was actively seen in recent news [58] where Perplexity generated information from Forbes, a website that requires a subscription to access. As answer engines continue to evolve, there is a risk that the financial viability of high-quality journalism could be compromised, particularly for outlets that depend on subscriptions and advertising revenue.

**中文**

在某些情况下，我们的研究发现某些系统（例如 Perplexity）仍然从基于订阅的网站检索内容，有效地绕过付费专区，并向用户提供来自这些来源的信息，而无需他们访问该网站或与付费专区互动。这在最近的新闻中得到了积极的体现[58]，其中 Perplexity 从福布斯生成信息，福布斯是一个需要订阅才能访问的网站。随着答案引擎的不断发展，高质量新闻的财务生存能力可能会受到损害，特别是对于依赖订阅和广告收入的媒体而言。

### 段落 165 · Page 18

**EN**

Absence of Policy Governing How Generative Models Affect Society: Our findings finally culminate in a critical issue: the absence of robust policy governance for generative models like answer engines. The lack of clear regulations, especially for systems functioning as sociotechnical entities, poses significant risks to individuals and society. Participants frequently highlighted the need for better governance. The lack of policy also raises concerns about privacy and data security, with participants recognizing the risks but noting a gap in understanding how to mitigate them.

**中文**

缺乏监管生成模型如何影响社会的政策：我们的研究结果最终导致了一个关键问题：缺乏针对答案引擎等生成模型的强有力的政策治理。缺乏明确的法规，特别是对于作为社会技术实体发挥作用的系统，给个人和社会带来重大风险。与会者经常强调需要更好的治理。政策的缺乏还引发了对隐私和数据安全的担忧，参与者认识到风险，但注意到在理解如何减轻风险方面存在差距。

### 段落 166 · Page 18

**EN**

Additionally, our study revealed concerns about the environmental impact of generative models, especially regarding energy consumption and carbon footprint. P21 noted: “The whole energy consumption and stuff behind it. It’s a point of real concern...it is really scary. " This highlights a broader issue often overlooked: the sustainability of these technologies. The computational power required for generative models increases energy use, exacerbating climate change.

**中文**

此外，我们的研究揭示了人们对生成模型对环境影响的担忧，特别是在能源消耗和碳足迹方面。 P21 指出：“整个能源消耗及其背后的东西。这是一个真正值得关注的问题……这真的很可怕。”这凸显了一个经常被忽视的更广泛的问题：这些技术的可持续性。生成模型所需的计算能力增加了能源消耗，加剧了气候变化。

### 段落 167 · Page 18

**EN**

Our findings suggest an urgent need for policymakers to engage with these technologies, understand their full range of impacts, and develop regulations to ensure their ethical and responsible use. 6.3 Navigating the Social Ramifications of Answer Engines: A Way Forward Our audit of answer engines reveals the potential social ramifications of these systems as they become increasingly embedded in various social contexts. Our findings, based on both qualitative and quantitative evaluations, identify several critical issues that require urgent attention.

**中文**

我们的研究结果表明，政策制定者迫切需要参与这些技术，了解其全方位的影响，并制定法规以确保其道德和负责任的使用。 6.3 探索答案引擎的社会影响：前进的道路 我们对答案引擎的审计揭示了这些系统随着它们越来越多地嵌入到各种社会环境中而潜在的社会影响。我们的研究结果基于定性和定量评估，确定了几个需要紧急关注的关键问题。

### 段落 168 · Page 18

**EN**

We propose that meaningful change can emerge not only through technological development but also from a collective reimagining of how we, as individuals, communities, and researchers, engage with these systems. We offer the following recommendations for different stakeholders: New Users: For individuals using answer engines for the first time, our findings highlight potential concerns associated with these technologies. While we acknowledge their benefits, we emphasize the importance of not accepting answers at face value. Users should approach results with caution, verifying and cross-checking them to ensure accuracy and reliability.

**中文**

我们认为，有意义的变革不仅可以通过技术发展来实现，还可以通过集体重新构想我们作为个人、社区和研究人员如何与这些系统互动来实现。我们为不同的利益相关者提供以下建议： 新用户：对于首次使用答案引擎的个人，我们的研究结果强调了与这些技术相关的潜在问题。虽然我们承认它们的好处，但我们强调不要仅接受表面答案的重要性。用户应谨慎对待结果，验证和交叉检查以确保准确性和可靠性。

### 段落 169 · Page 18

**EN**

Awareness on how these systems can affect your social space is key in identifying their ramifications. Active Users: For experienced users, our AEE scorecard and qualitative evaluations provide detailed insights into the specific risks associated with answer engines. We hope these findings encourage users to critically assess system outputs and verify them whenever possible. Our scorecard is designed to help users focus on key areas of concern, promoting a culture of continuous scrutiny and accountability. We vary of how these systems can affect you and how you expect these systems to improve.

**中文**

了解这些系统如何影响您的社交空间是确定其影响的关键。活跃用户：对于经验丰富的用户，我们的 AEE 记分卡和定性评估提供了与答案引擎相关的特定风险的详细见解。我们希望这些发现鼓励用户批判性地评估系统输出并尽可能验证它们。我们的记分卡旨在帮助用户关注关键领域，促进持续审查和问责的文化。我们对这些系统对您的影响以及您期望这些系统如何改进的方式有所不同。

### 段落 170 · Page 18

**EN**

Developers: For developers, it is crucial to remain aware of the social implications of these models. While answer engines can be powerful tools, their promotion should be balanced with transparency about their limitations. Regular scrutiny and public disclosure of model behaviors, using benchmarks like the AEE, can help build user trust and support informed engagement. Releasing this result transparently is essential to foster an ecosystem where trust in these technologies is continually earned and maintained.

**中文**

开发人员：对于开发人员来说，始终了解这些模型的社会影响至关重要。虽然答案引擎可以是强大的工具，但它们的推广应该与其局限性的透明度相平衡。使用 AEE 等基准定期审查和公开披露模型行为，可以帮助建立用户信任并支持知情参与。透明地发布这一结果对于培育一个不断赢得和维持对这些技术的信任的生态系统至关重要。

### 段落 171 · Page 18

**EN**

Researchers and the Ethics Community: As researchers and ethics advocates, we will make our code and benchmarks available for public scrutiny. We believe the best way to understand the ongoing evolution of these systems is through continuous evaluation and refinement of the benchmark. We view our contributions as living tools that should evolve alongside these technologies. We encourage the community to engage with, use, and modify these benchmarks, establishing a robust framework for auditing and improving these systems.

**中文**

研究人员和道德社区：作为研究人员和道德倡导者，我们将让我们的准则和基准接受公众监督。我们相信，了解这些系统不断发展的最佳方式是通过对基准的持续评估和完善。我们将我们的贡献视为应该与这些技术一起发展的生活工具。我们鼓励社区参与、使用和修改这些基准，建立一个强大的框架来审计和改进这些系统。

### 段落 172 · Page 18

**EN**

Our shared responsibility is to highlight issues within our field and advocate for more responsible and transparent practices. 7 Ethics Statement and Limitation A significant limitation of our work is its Western-centric focus. The answer engines we evaluated were primarily developed and deployed in U.S.-centric contexts, which influenced both the scope of our audit and the recruitment process. While we included diverse participants within this framework, the study inherently reflects Western perspectives due to the demographics of those who responded to our invitations.

**中文**

我们的共同责任是突出我们领域内的问题并倡导更负责任和透明的做法。 7 道德声明和限制 我们工作的一个重大限制是它以西方为中心。我们评估的答案引擎主要是在以美国为中心的环境中开发和部署的，这影响了我们的审计范围和招聘流程。虽然我们在这个框架内纳入了不同的参与者，但由于响应我们邀请的人的人口统计数据，这项研究本质上反映了西方的观点。

### 段落 173 · Page 18

**EN**

Additionally, answer engines often rely on location-specific data, and the models we evaluated were no exception. Our findings may not fully apply to users in other regions, particularly the Global South, where cultural, social, and technological contexts differ. Future research should explore how these systems perform in non- Western settings. We recognize that while our metric, derived from our humancentric usability study, serves as a valuable benchmark, it is not the definitive gold standard.

**中文**

此外，答案引擎通常依赖于特定位置的数据，我们评估的模型也不例外。我们的研究结果可能并不完全适用于其他地区的用户，特别是文化、社会和技术背景不同的南半球国家。未来的研究应该探索这些系统在非西方环境中的表现。我们认识到，虽然我们的指标源自以人为本的可用性研究，可以作为有价值的基准，但它并不是最终的黄金标准。

### 段落 174 · Page 18

**EN**

There is ample room for growth and refinement, and we are committed to continually updating and improving the platform, such as including multilingual elements, as the field evolves. Finally, as the AI landscape rapidly evolves, model behaviors are frequently updated. Our findings reflect the state of answer engines as of August 2024, but these systems’ behaviors may change. Therefore, our results should be viewed in the context of this dynamic and shifting field.

**中文**

有足够的增长和完善空间，我们致力于随着该领域的发展不断更新和改进该平台，例如包含多语言元素。最后，随着人工智能领域的快速发展，模型行为会频繁更新。我们的研究结果反映了截至 2024 年 8 月答案引擎的状态，但这些系统的行为可能会发生变化。因此，我们的结果应该在这个动态和变化的领域的背景下看待。

### Page 19

### 段落 175 · Page 19

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, 8 Positionality Statement As researchers with backgrounds in NLP, human-computer interaction, and socioinformatics, we approach this study with a deep commitment to ethical considerations in AI. Our work is grounded in the belief that AI systems must be designed to promote transparency, fairness, and societal well-being, taking into consideration the users using the system.

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024 年 6 月 3-05 日，8 立场声明 作为具有自然语言处理、人机交互和社会信息学背景的研究人员，我们在开展这项研究时，对人工智能中的伦理考虑有着坚定的承诺。我们的工作基于这样的信念：人工智能系统的设计必须促进透明度、公平性和社会福祉，同时考虑到使用该系统的用户。

### 段落 176 · Page 19

**EN**

We acknowledge that our perspectives are shaped by our prior experiences working in both academia and industry, particularly in designing trustworthy AI systems at our respective institutions. 9 Conclusion Our work provides a comprehensive audit of answer engines, moving beyond technical assessment to consider broader societal implications. Using a community-based usability study, we identified significant limitations in these systems’ handling of queries, including biases and transparency issues. We propose 16 actionable design recommendations, supported by eight metrics linking design to evaluation.

**中文**

我们承认，我们的观点是由我们之前在学术界和工业界的工作经验决定的，特别是在我们各自的机构设计值得信赖的人工智能系统方面。 9 结论 我们的工作提供了对答案引擎的全面审核，超越技术评估，考虑更广泛的社会影响。通过基于社区的可用性研究，我们发现了这些系统处理查询的重大局限性，包括偏见和透明度问题。我们提出了 16 条可行的设计建议，并得到了将设计与评估联系起来的八个指标的支持。

### 段落 177 · Page 19

**EN**

A large-scale automated evaluation of systems like You.com, Perplexity.ai, and BingChat showed that none met acceptable performance across most metrics, including critical aspects related to handling hallucinations, unsupported statements, and citation accuracy. We release our benchmark for ongoing audits to ensure these systems’ transparency, fairness, and safety11. As these technologies evolve, we advocate for continuous community-led evaluations to foster more equitable AI systems. References [1] Sabira Arefin. 2024. AI Revolutionizing Healthcare: Innovations, Challenges, and Ethical Considerations.

**中文**

对 You.com、Perplexity.ai 和 BingChat 等系统的大规模自动评估表明，大多数指标都没有达到可接受的性能，包括与处理幻觉、不受支持的陈述和引用准确性相关的关键方面。我们发布了持续审计的基准，以确保这些系统的透明度、公平性和安全性11。随着这些技术的发展，我们主张持续进行社区主导的评估，以培育更公平的人工智能系统。参考文献 [1] Sabira Arefin。 2024 年。人工智能彻底改变医疗保健：创新、挑战和道德考虑。

### 段落 178 · Page 19

**EN**

MZ Journal of Artificial Intelligence 1, 2 (2024), 1–17. [2] Carl Auerbach and Louise B Silverstein. 2003. Qualitative data: An introduction to coding and analysis . Vol. 21. NYU press. [3] Emily M Bender. 2024. Resisting Dehumanization in the Age of “AI”. Current Directions in Psychological Science 33, 2 (2024), 114–120. [4] Emily M Bender, Timnit Gebru, Angelina McMillan-Major, and Shmargaret Shmitchell. 2021. On the dangers of stochastic parrots: Can language models be too big?. In Proceedings of the 2021 ACM conference on fairness, accountability, and transparency. 610–623.

**中文**

MZ 人工智能杂志 1, 2 (2024), 1–17。 [2] 卡尔·奥尔巴赫和路易丝·B·西尔弗斯坦。 2003.定性数据：编码和分析简介。卷。 21. 纽约大学出版社。 [3] 艾米丽·M·本德。 2024年。抵制“人工智能”时代的非人化。心理科学当前方向 33, 2 (2024), 114–120。 [4] 艾米丽·M·本德、蒂姆尼特·格布鲁、安吉丽娜·麦克米伦·梅杰和什玛格丽特·施米切尔。 2021.关于随机鹦鹉的危险：语言模型会太大吗？。 2021 年 ACM 公平、问责和透明度会议记录。 610–623。

### 段落 179 · Page 19

**EN**

[5] Su Lin Blodgett, Solon Barocas, Hal Daumé III, and Hanna Wallach. 2020. Language (Technology) is Power: A Critical Survey of “Bias” in NLP. InProceedings of the 58th Annual Meeting of the Association for Computational Linguistics . 5454– 5476. [6] Valerio Capraro, Austin Lentsch, Daron Acemoglu, Selin Akgun, Aisel Akhmedova, Ennio Bilancini, Jean-François Bonnefon, Pablo Brañas-Garza, Luigi Butera, Karen M Douglas, et al. 2024. The impact of generative artificial intelligence on socioeconomic inequalities and policy making. PNAS nexus 3, 6 (2024). [7] Kathy Charmaz. 2006.

**中文**

[5] Su Lin Blodgett、Solon Barocas、Hal Daumé III 和 Hanna Wallach。 2020。语言（技术）就是力量：对 NLP 中“偏见”的批判性调查。计算语言学协会第 58 届年会记录。 5454–5476。 [6] Valerio Capraro、Austin Lentsch、Daron Acemoglu、Selin Akgun、Aisel Akhmedova、Ennio Bilancini、Jean-François Bonnefon、Pablo Brañas-Garza、Luigi Butera、Karen M Douglas 等。 2024.生成人工智能对社会经济不平等和政策制定的影响。美国国家科学院院刊 Nexus 3, 6 (2024)。 [7] 凯西·查马兹。 2006年。

### 段落 180 · Page 19

**EN**

Constructing grounded theory: A practical guide through qualitative analysis. sage. [8] Kathy Charmaz. 2017. Constructivist grounded theory. The Journal of Positive Psychology 12, 3 (2017), 299–300. [9] Pratyush Chauhan, Rahul Kumar Sahani, Soham Datta, Ali Qadir, Manish Raj, and Mohd Mohsin Ali. 2024. Evaluating Top-k RAG-based approach for Game Review Generation. In 2024 IEEE International Conference on Computing, Power and Communication Technologies (IC2PCT), Vol. 5. IEEE, 258–263. [10] Robert Cooper and Michael Foster. 1971. Sociotechnical systems. American Psychologist 26, 5 (1971), 467. [11] Dipto Das. 2023.

**中文**

构建扎根理论：定性分析的实用指南。圣人。 [8] 凯西·查马兹。 2017.建构主义扎根理论。积极心理学杂志 12, 3 (2017), 299–300。 [9] Pratyush Chauhan、Rahul Kumar Sahani、Soham Datta、Ali Qadir、Manish Raj 和 Mohd Mohsin Ali。 2024. 评估基于 Top-k RAG 的游戏评论生成方法。 2024 年 IEEE 国际计算、电力和通信技术会议 (IC2PCT)，卷。 5. IEEE，258-263。 [10] 罗伯特·库珀和迈克尔·福斯特。 1971.社会技术系统。 《美国心理学家》26, 5 (1971), 467。 [11] Dipto Das。 2023 年。

### 段落 181 · Page 19

**EN**

Studying Multi-dimensional Marginalization of Identity from Decolonial and Postcolonial Perspectives. In Companion Publication of the 2023 Conference on Computer Supported Cooperative Work and Social Computing . 437– 440. [12] Dipto Das, Shion Guha, Jed R Brubaker, and Bryan Semaan. 2024. The“Colonial Impulse" of Natural Language Processing: An Audit of Bengali Sentiment Analysis Tools and Their Identity-based Biases. In Proceedings of the CHI Conference on Human Factors in Computing Systems . 1–18. 11https://github.com/SalesforceAIResearch/answer-engine-eval [13] Dipto Das and Bryan Semaan. 2022.

**中文**

从非殖民和后殖民的角度研究身份的多维边缘化。 2023 年计算机支持的协作工作和社会计算会议的配套出版物。 437–440。 [12] Dipto Das、Shion Guha、Jed R Brubaker 和 Bryan Semaan。 2024.自然语言处理的“殖民冲动”：对孟加拉语情感分析工具及其基于身份的偏见的审计。在 CHI 计算系统中的人为因素会议记录中。 1-18。 11https://github.com/SalesforceAIResearch/answer-engine-eval [13] Dipto Das 和 Bryan Semaan。 2022 年。

### 段落 182 · Page 19

**EN**

Decolonial and Postcolonial Computing Research: A Scientometric Exploration. In Companion Publication of the 2022 Conference on Computer Supported Cooperative Work and Social Computing . 168– 174. [14] Sarah Dean, Thomas Krendl Gilbert, Nathan Lambert, and Tom Zick. 2021. Axes for sociotechnical inquiry in AI research. IEEE Transactions on Technology and Society 2, 2 (2021), 62–70. [15] Yujuan Ding, Wenqi Fan, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li. 2024. A survey on rag meets llms: Towards retrievalaugmented large language models. arXiv preprint arXiv:2405.06211 (2024).

**中文**

非殖民和后殖民计算研究：科学计量学探索。 2022 年计算机支持的协作工作和社会计算会议的配套出版物。 168-174。 [14]莎拉·迪恩、托马斯·克伦德尔·吉尔伯特、内森·兰伯特和汤姆·齐克。 2021.人工智能研究中社会技术探究的轴。 IEEE 技术与社会学报 2, 2 (2021), 62–70。 [15] 丁玉娟，范文琪，宁良波，王士杰，李恒云，尹大伟，蔡达成，李庆。 2024.一项关于 rag meet llms 的调查：走向检索增强大型语言模型。 arXiv 预印本 arXiv:2405.06211 (2024)。

### 段落 183 · Page 19

**EN**

[16] Upol Ehsan, Samir Passi, Q Vera Liao, Larry Chan, I-Hsiang Lee, Michael Muller, and Mark O Riedl. 2024. The Who in XAI: How AI Background Shapes Perceptions of AI Explanations. In Proceedings of the CHI Conference on Human Factors in Computing Systems. 1–32. [17] Upol Ehsan and Mark O Riedl. 2020. Human-centered explainable ai: Towards a reflective sociotechnical approach. In HCI International 2020-Late Breaking Papers: Multimodality and Intelligence: 22nd HCI International Conference, HCII 2020, Copenhagen, Denmark, July 19–24, 2020, Proceedings 22 . Springer, 449–466.

**中文**

[16] Upol Ehsan、Samir Passi、Q Vera Liao、Larry Chan、I-Hsiang Lee、Michael Muller 和 Mark O Riedl。 2024. XAI 中的人物：人工智能背景如何塑造对人工智能解释的看法。摘自 CHI 计算系统人因会议论文集。 1-32。 [17] 乌波尔·埃桑和马克·O·里德尔。 2020.以人为中心的可解释人工智能：迈向反思性社会技术方法。 In HCI International 2020-Late Breaking Papers: Multimodality and Intelligence: 22nd HCI International Conference, HCII 2020, 丹麦哥本哈根，2020 年 7 月 19-24 日，会议记录 22。施普林格，449-466。

### 段落 184 · Page 19

**EN**

[18] Upol Ehsan, Elizabeth A Watkins, Philipp Wintersberger, Carina Manger, Sunnie SY Kim, Niels Van Berkel, Andreas Riener, and Mark O Riedl. 2024. Human- Centered Explainable AI (HCXAI): Reloading Explainability in the Era of Large Language Models (LLMs). In Extended Abstracts of the CHI Conference on Human Factors in Computing Systems . 1–6. [19] Shahul Es, Jithin James, Luis Espinosa Anke, and Steven Schockaert. 2024. RAGAs: Automated Evaluation of Retrieval Augmented Generation. In Proceedings of the 18th Conference of the European Chapter of the Association for Computational Linguistics: System Demonstrations. 150–158.

**中文**

[18] Upol Ehsan、Elizabeth A Watkins、Philipp Wintersberger、Carina Manger、Sunnie SY Kim、Niels Van Berkel、Andreas Riener 和 Mark O Riedl。 2024.以人为中心的可解释人工智能（HCXAI）：在大型语言模型（LLM）时代重新加载可解释性。在 CHI 计算系统中人为因素会议的扩展摘要中。 1-6。 [19] Shahul Es、Jithin James、Luis Espinosa Anke 和 Steven Schockaert。 2024.RAGA：检索增强生成的自动评估。计算语言学协会欧洲分会第 18 届会议记录：系统演示。 150–158。

### 段落 185 · Page 19

**EN**

[20] Shahul Es, Jithin James, Luis Espinosa-Anke, and Steven Schockaert. 2023. Ragas: Automated evaluation of retrieval augmented generation. arXiv preprint arXiv:2309.15217 (2023). [21] Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li. 2024. A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models. In Proceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining . 6491–6501. [22] Emilio Ferrara. 2024. GenAI against humanity: Nefarious applications of generative artificial intelligence and large language models.

**中文**

[20] Shahul Es、Jithin James、Luis Espinosa-Anke 和 Steven Schockaert。 2023. Ragas：检索增强生成的自动评估。 arXiv 预印本 arXiv:2309.15217 (2023)。 [21] 范文琪，丁玉娟，宁良波，王士杰，李恒云，尹大伟，蔡达成，李庆。 2024. RAG 会议法学硕士调查：走向检索增强大型语言模型。第 30 届 ACM SIGKDD 知识发现和数据挖掘会议论文集。 6491–6501。 [22]埃米利奥·费拉拉。 2024. GenAI 反人类：生成人工智能和大型语言模型的邪恶应用。

### 段落 186 · Page 19

**EN**

Journal of Computational Social Science (2024), 1–21. [23] Yunfan Gao, Yun Xiong, Xinyu Gao, Kangxiang Jia, Jinliu Pan, Yuxi Bi, Yi Dai, Jiawei Sun, and Haofen Wang. 2023. Retrieval-augmented generation for large language models: A survey. arXiv preprint arXiv:2312.10997 (2023). [24] Sanjana Gautam, Pranav Narayanan Venkit, and Sourojit Ghosh. 2024. From melting pots to misrepresentations: Exploring harms in generative ai. arXiv preprint arXiv:2403.10776 (2024). [25] Sourojit Ghosh, Pranav Narayanan Venkit, Sanjana Gautam, Shomir Wilson, and Aylin Caliskan. 2024.

**中文**

计算社会科学杂志（2024），1-21。 [23] 高云帆，熊云，高新宇，贾康祥，潘金六，毕玉玺，戴毅，孙家伟，王浩芬。 2023.大型语言模型的检索增强生成：一项调查。 arXiv 预印本 arXiv:2312.10997 (2023)。 [24] Sanjana Gautam、Pranav Narayanan Venkit 和 Sourojit Ghosh。 2024 年。从大熔炉到歪曲事实：探索生成人工智能的危害。 arXiv 预印本 arXiv:2403.10776 (2024)。 [25] Sourojit Ghosh、Pranav Narayanan Venkit、Sanjana Gautam、Shomir Wilson 和 Aylin Caliskan。 2024 年。

### 段落 187 · Page 19

**EN**

Do Generative AI Models Output Harm while Representing Non-Western Cultures: Evidence from A Community-Centered Approach. arXiv preprint arXiv:2407.14779 (2024). [26] Barney Glaser. 1992. Basics of grounded theory analysis: Emergence vs forcing. (1992). [27] Barney Glaser and Anselm Strauss. 1967. Discovery of grounded theory: Strategies for qualitative research. Routledge. [28] Eric Goldman. 2005. Search engine bias and the demise of search engine utopianism. Yale JL & Tech. 8 (2005), 188. [29] David Grant. 2025. Populism, Artificial Intelligence and Law: A New Understanding of the Dynamics of the Present . Taylor & Francis.

**中文**

生成式人工智能模型在代表非西方文化时是否会产生伤害：来自以社区为中心的方法的证据。 arXiv 预印本 arXiv：2407.14779 (2024)。 [26] 巴尼·格拉泽。 1992.扎根理论分析的基础知识：涌现与强迫。 （1992）。 [27] 巴尼·格拉泽和安塞姆·施特劳斯。 1967.扎根理论的发现：定性研究策略。劳特利奇。 [28]埃里克·戈德曼。 2005 年。搜索引擎偏见和搜索引擎乌托邦主义的消亡。耶鲁 JL 与科技。 8 (2005), 188。 [29] 大卫·格兰特。 2025.民粹主义、人工智能和法律：对当前动态的新理解。泰勒和弗朗西斯.

### 段落 188 · Page 19

**EN**

[30] Aman Gupta, Anup Shirgaonkar, Angels de Luis Balaguer, Bruno Silva, Daniel Holstein, Dawei Li, Jennifer Marsman, Leonardo O Nunes, Mahsa Rouzbahman, Morris Sharp, et al. 2024. RAG vs Fine-tuning: Pipelines, Tradeoffs, and a Case Study on Agriculture. arXiv preprint arXiv:2401.08406 (2024). [31] Vipul Gupta, Pranav Narayanan Venkit, Shomir Wilson, and Rebecca J Passonneau. 2024. Sociodemographic bias in language models: A survey and forward path. In Proceedings of the 5th Workshop on Gender Bias in Natural Language Processing (GeBNLP). 295–322. [32] Jutta Haider and Olof Sundin. 2019.

**中文**

[30] Aman Gupta、Anup Shirgaonkar、Angels de Luis Balaguer、Bruno Silva、Daniel Holstein、Dawei Li、Jennifer Marsman、Leonardo O Nunes、Mahsa Rouzbahman、Morris Sharp 等。 2024.RAG 与微调：管道、权衡和农业案例研究。 arXiv 预印本 arXiv:2401.08406 (2024)。 [31] Vipul Gupta、Pranav Narayanan Venkit、Shomir Wilson 和 Rebecca J Passonneau。 2024。语言模型中的社会人口统计学偏见：调查和前进道路。第五届自然语言处理中的性别偏见研讨会 (GeBNLP) 论文集。 295–322。 [32] 尤塔·海德尔和奥洛夫·桑丁。 2019.

### 段落 189 · Page 19

**EN**

Invisible search and online search engines: The ubiquity of search in everyday life . Taylor & Francis. [33] Donna Haraway. 2013. Situated knowledges: The science question in feminism and the privilege of partial perspective 1. In Women, science, and technology . Routledge, 455–472. [34] Carol Mullins Hayes. 2023. Generative artificial intelligence and copyright: Both sides of the Black Box. A vailable at SSRN 4517799 (2023). [35] Wayne Holmes and Ilkka Tuomi. 2022. State of the art and practice in AI in education. European Journal of Education 57, 4 (2022), 542–570. [36] John E Hopcroft and Richard M Karp. 1973.

**中文**

隐形搜索和在线搜索引擎：搜索在日常生活中无处不在。泰勒和弗朗西斯. [33] 唐娜·哈拉维。 2013年。情境知识：女权主义中的科学问题和局部观点的特权1。在妇女、科学和技术中。劳特利奇，455-472。 [34] 卡罗尔·马林斯·海耶斯。 2023.生成人工智能和版权：黑匣子的双方。可在 SSRN 4517799 (2023) 获取。 [35] 韦恩·霍姆斯和伊尔卡·托米。 2022.人工智能教育领域的最新技术和实践。欧洲教育杂志 57, 4 (2022), 542–570。 [36] 约翰·E·霍普克罗夫特和理查德·M·卡普。 1973年。

### 段落 190 · Page 19

**EN**

An nˆ5/2 algorithm for maximum matchings in bipartite graphs. SIAM Journal on computing 2, 4 (1973), 225–231. [37] Lei Huang, Weijiang Yu, Weitao Ma, Weihong Zhong, Zhangyin Feng, Haotian Wang, Qianglong Chen, Weihua Peng, Xiaocheng Feng, Bing Qin, et al. 2023. A survey on hallucination in large language models: Principles, taxonomy, challenges, and open questions. arXiv preprint arXiv:2311.05232 (2023).

**中文**

用于二分图中最大匹配的 n^5/2 算法。 SIAM 计算杂志 2, 4 (1973), 225–231。 [37] 黄磊，于伟江，马伟涛，钟伟宏，冯章印，王浩天，陈强龙，彭伟华，冯晓程，秦兵，等。 2023. 大语言模型中的幻觉调查：原则、分类、挑战和开放问题。 arXiv 预印本 arXiv:2311.05232 (2023)。

### Page 20

### 段落 191 · Page 20

**EN**

, June 03–05, 2024, Trovato et al. [38] Soyeong Jeong, Jinheon Baek, Sukmin Cho, Sung Ju Hwang, and Jong C Park. 2024. Adaptive-RAG: Learning to Adapt Retrieval-Augmented Large Language Models through Question Complexity. InProceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers) . 7029–7043. [39] Navreet Kaur, Monojit Choudhury, and Danish Pruthi. 2024. Evaluating Large Language Models for Health-related Queries with Presuppositions.

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。 [38] Soying Jeong、Jinheon Baek、Sukmin Cho、Sung Ju Hwang 和 Jong C Park。 2024.Adaptive-RAG：通过问题复杂性学习适应检索增强大型语言模型。计算语言学协会北美分会 2024 年会议论文集：人类语言技术（第一卷：长论文）。 7029–7043。 [39] Navreet Kaur、Monojit Choudhury 和Danish Pruthi。 2024.使用预设评估健康相关查询的大型语言模型。

### 段落 192 · Page 20

**EN**

In Findings of the Association for Computational Linguistics ACL 2024 , Lun-Wei Ku, Andre Martins, and Vivek Srikumar (Eds.). Association for Computational Linguistics, Bangkok, Thailand and virtual meeting, 14308–14331. https://aclanthology.org/ 2024.findings-acl.850 [40] Yekyung Kim, Yapei Chang, Marzena Karpinska, Aparna Garimella, Varun Manjunatha, Kyle Lo, Tanya Goyal, and Mohit Iyyer. 2024. FABLES: Evaluating faithfulness and content selection in book-length summarization. arXiv preprint arXiv:2404.01261 (2024). [41] Philippe Laban, Alexander R Fabbri, Caiming Xiong, and Chien-Sheng Wu. 2024.

**中文**

在计算语言学协会 ACL 2024 的调查结果中，Lun-Wei Ku、Andre Martins 和 Vivek Srikumar（编辑）。计算语言学协会，泰国曼谷和虚拟会议，14308-14331。 https://aclanthology.org/2024.findings-acl.850 [40] Yekyung Kim、Yapei Chang、Marzena Karpinska、Aparna Garimella、Varun Manjunatha、Kyle Lo、Tanya Goyal 和 Mohit Iyyer。 2024.寓言：评估全书摘要的忠实度和内容选择。 arXiv 预印本 arXiv:2404.01261 (2024)。 [41] Philippe Laban、Alexander R Fabbri、Caiming Xiong 和 Chien-Sheng Wu。 2024 年。

### 段落 193 · Page 20

**EN**

Summary of a Haystack: A Challenge to Long-Context LLMs and RAG Systems. arXiv preprint arXiv:2407.01370 (2024). [42] Philippe Laban, Wojciech Kryściński, Divyansh Agarwal, Alexander R Fabbri, Caiming Xiong, Shafiq Joty, and Chien-Sheng Wu. 2023. Llms as factual reasoners: Insights from existing benchmarks and beyond. arXiv preprint arXiv:2305.14540 (2023). [43] Philippe Laban, Lidiya Murakhovs’ ka, Caiming Xiong, and Chien-Sheng Wu. 2023. Are you sure? challenging llms leads to performance drops in the flipflop experiment. arXiv preprint arXiv:2311.08596 (2023). [44] Philippe Laban, Tobias Schnabel, Paul N Bennett, and Marti A Hearst. 2022.

**中文**

大海捞针摘要：对长上下文法学硕士和 RAG 系统的挑战。 arXiv 预印本 arXiv:2407.01370 (2024)。 [42] Philippe Laban、Wojciech Kryściński、Divyansh Agarwal、Alexander R Fabbri、Caiming Xiong、Shafiq Joty 和 Chien-Sheng Wu。 2023. 法学硕士作为事实推理者：来自现有基准及其他基准的见解。 arXiv 预印本 arXiv:2305.14540 (2023)。 [43] Philippe Laban、Lidiya Murakhovs’ ka、Caiming Xiong 和 Chien-Sheng Wu。 2023.你确定吗？具有挑战性的 LLMS 会导致触发器实验的性能下降。 arXiv 预印本 arXiv:2311.08596 (2023)。 [44] 菲利普·拉班、托比亚斯·施纳贝尔、保罗·N·贝内特和马蒂·A·赫斯特。 2022 年。

### 段落 194 · Page 20

**EN**

SummaC: Re-visiting NLI-based models for inconsistency detection in summarization. Transactions of the Association for Computational Linguistics 10 (2022), 163–177. [45] Mike Lewis, Marjan Ghazvininejad, Gargi Ghosh, Armen Aghajanyan, Sida Wang, and Luke Zettlemoyer. 2020. Pre-training via Paraphrasing. Advances in Neural Information Processing Systems 33 (2020), 18470–18481. [46] Alice Li and Luanne Sinnamon. 2024. Generative AI Search Engines as Arbiters of Public Knowledge: An Audit of Bias and Authority.arXiv preprint arXiv:2405.14034 (2024). [47] Nora Freya Lindemann. 2024. Chatbots, search engines, and the sealing of knowledges.

**中文**

SummaC：重新审视基于 NLI 的模型，以检测摘要中的不一致情况。计算语言学协会汇刊 10 (2022), 163–177。 [45] Mike Lewis、Marjan Ghazvininejad、Gargi Ghosh、Armen Aghajanyan、Sida Wang 和 Luke Zettlemoyer。 2020.通过释义进行预训练。神经信息处理系统的进展 33 (2020), 18470–18481。 [46] 艾丽丝·李和卢安·辛纳蒙。 2024 年。生成式人工智能搜索引擎作为公共知识的仲裁者：对偏见和权威的审计。arXiv 预印本 arXiv:2405.14034 (2024)。 [47] 诺拉·弗雷亚·林德曼。 2024 年。聊天机器人、搜索引擎和知识密封。

### 段落 195 · Page 20

**EN**

AI & SOCIETY (2024), 1–14. [48] Sebastian Lins, Konstantin D Pandl, Heiner Teigeler, Scott Thiebes, Calvin Bayer, and Ali Sunyaev. 2021. Artificial intelligence as a service: classification and research directions. Business & Information Systems Engineering 63 (2021), 441– 456. [49] Nelson F Liu, Tianyi Zhang, and Percy Liang. 2023. Evaluating Verifiability in Generative Search Engines. In Findings of the Association for Computational Linguistics: EMNLP 2023. 7001–7025. [50] Patrick Maillé, Gwen Maudet, Mathieu Simon, and Bruno Tuffin. 2022. Are search engines biased? Detecting and reducing bias using meta search engines.

**中文**

人工智能与社会（2024），1-14。 [48] 塞巴斯蒂安·林斯、康斯坦丁·D·潘德尔、海纳·泰格勒、斯科特·蒂贝斯、卡尔文·拜尔和阿里·桑亚耶夫。 2021.人工智能即服务：分类和研究方向。商业与信息系统工程 63 (2021), 441–456。 [49] Nelson F Liu、Tianyi 张和 Percy Liang。 2023.评估生成式搜索引擎的可验证性。计算语言学协会的调查结果：EMNLP 2023。7001–7025。 [50]帕特里克·梅勒、格温·莫德、马蒂厄·西蒙和布鲁诺·图芬。 2022.搜索引擎有偏见吗？使用元搜索引擎检测和减少偏见。

### 段落 196 · Page 20

**EN**

Electronic Commerce Research and Applications (2022), 101132. [51] Sharon McDonald, Helen M Edwards, and Tingting Zhao. 2012. Exploring thinkalouds in usability testing: An international survey. IEEE Transactions on Professional Communication 55, 1 (2012), 2–19. [52] Shahan Ali Memon and Jevin D West. 2024. Search engines post-ChatGPT: How generative artificial intelligence could make search less reliable. arXiv preprint arXiv:2402.11707 (2024). [53] Abbe Mowshowitz and Akira Kawaguchi. 2005. Measuring search engine bias. Information processing & management 41, 5 (2005), 1193–1205. [54] Rainer Mühlhoff. 2018.

**中文**

电子商务研究与应用（2022），101132。 [51] Sharon McDonald、Helen M Edwards 和 Tingting Zhu。 2012 年。探索可用性测试中的大声思考：一项国际调查。 IEEE 专业通信汇刊 55, 1 (2012), 2–19。 [52] 沙汉·阿里·梅蒙和杰文·D·韦斯特。 2024 年。ChatGPT 后的搜索引擎：生成式人工智能如何降低搜索的可靠性。 arXiv 预印本 arXiv:2402.11707 (2024)。 [53]阿贝·莫肖维茨和川口晃。 2005 年。测量搜索引擎偏差。信息处理与管理 41, 5 (2005), 1193–1205。 [54] 赖纳·米尔霍夫。 2018.

### 段落 197 · Page 20

**EN**

Digitale Entmündigung und User Experience Design. Leviathan 46, 4 (2018), 551–574. [55] Tarek Naous, Michael Joseph Ryan, and Wei Xu. 2023. Having Beer after Prayer? Measuring Cultural Bias in Large Language Models. InAnnual Meeting of the Association for Computational Linguistics . https://api.semanticscholar.org/CorpusID: 258865272 [56] Pranav Narayanan Venkit. 2023. Towards a holistic approach: Understanding sociodemographic biases in nlp models using an interdisciplinary lens. In Proceedings of the 2023 AAAI/ACM Conference on AI, Ethics, and Society . 1004–1005.

**中文**

数字环境和用户体验设计。利维坦 46, 4 (2018), 551–574。 [55]塔里克·纳乌斯、迈克尔·约瑟夫·瑞安、徐伟。 2023. 祷告后喝啤酒？测量大型语言模型中的文化偏见。在计算语言学协会年会上。 https://api.semanticscholar.org/CorpusID: 258865272 [56] Pranav Narayanan Venkit。 2023.迈向整体方法：使用跨学科视角理解 NLP 模型中的社会人口统计学偏差。 2023 年 AAAI/ACM 人工智能、伦理与社会会议论文集。 1004–1005。

### 段落 198 · Page 20

**EN**

[57] Pranav Narayanan Venkit, Sanjana Gautam, Ruchi Panchanadikar, Ting-Hao Huang, and Shomir Wilson. 2023. Unmasking nationality bias: A study of human perception of nationalities in ai-generated articles. In Proceedings of the 2023 AAAI/ACM Conference on AI, Ethics, and Society . 554–565. [58] Casey Newton. 2024. How to stop perplexity and save the web from bad ai. https://www.platformer.news/how-to-stop-perplexity-oreilly-ai-publishing/ [59] Mie Nørgaard and Kasper Hornbæk. 2006. What do usability evaluators do in practice? An explorative study of think-aloud testing. In Proceedings of the 6th conference on Designing Interactive systems .

**中文**

[57] Pranav Narayanan Venkit、Sanjana Gautam、Ruchi Panchanadikar、Ting-Hao Huang 和 Shomir Wilson。 2023. 揭露国籍偏见：对人工智能生成的文章中人类对国籍的看法的研究。 2023 年 AAAI/ACM 人工智能、伦理与社会会议论文集。 554–565。 [58]凯西·牛顿。 2024. 如何停止困惑并拯救网络免受不良人工智能的侵害。 https://www.platformer.news/how-to-stop-perplexity-oreilly-ai-publishing/ [59] Mie Nørgaard 和 Kasper Hornbæk。 2006.可用性评估员在实践中做什么？有声思维测试的探索性研究。第六届交互系统设计会议论文集。

### 段落 199 · Page 20

**EN**

209–218. [60] Cathy O’neil. 2017.Weapons of math destruction: How big data increases inequality and threatens democracy. Crown. [61] Sanjeev Pulapaka, Srinath Godavarthi, and Dr Sherry Ding. 2024. GenAI and the Public Sector. In Empowering the Public Sector with Generative AI: From Strategy and Design to Real-World Applications. Springer, 31–43. [62] Vipula Rawte, Amit Sheth, and Amitava Das. 2023. A survey of hallucination in large foundation models. arXiv preprint arXiv:2309.05922 (2023). [63] Kylie Robison. 2024. Google promised a better search experience - now it’s telling us to put glue on our pizza.

**中文**

209–218。 [60]凯茜·奥尼尔。 2017.数学毁灭性武器：大数据如何加剧不平等并威胁民主。王冠。 [61] Sanjeev Pulapaka、Srinath Godavarthi 和 Sherry Ding 博士。 2024。GenAI 和公共部门。用生成式人工智能赋能公共部门：从战略和设计到实际应用。施普林格，31-43。 [62] 维普拉·拉特 (Vipula Rawte)、阿米特·谢思 (Amit Sheth) 和阿米塔瓦·达斯 (Amitava Das)。 2023.大型基础模型中幻觉的调查。 arXiv 预印本 arXiv:2309.05922 (2023)。 [63] 凯莉·罗宾逊。 2024 年。谷歌承诺提供更好的搜索体验 - 现在它告诉我们在披萨上涂上胶水。

### 段落 200 · Page 20

**EN**

https://www.theverge.com/2024/5/23/24162896/ google-ai-overview-hallucinations-glue-in-pizza [64] Sujoy Roychowdhury, Sumit Soman, HG Ranjani, Neeraj Gunda, Vansh Chhabra, and Sai Krishna Bala. 2024. Evaluation of RAG Metrics for Question Answering in the Telecom Domain. arXiv preprint arXiv:2407.12873 (2024). [65] Eryk Salvaggio. 2024. Challenging the myths of Generative AI. https://www. techpolicy.press/challenging-the-myths-of-generative-ai/ [66] Deepa Seetharaman. 2024. https://www.wsj.com/tech/ai/openai-search-enginesearchgpt-97771f86 [67] Chirag Shah and Emily M Bender. 2024.

**中文**

https://www.theverge.com/2024/5/23/24162896/ google-ai-overview-hallucinations-glue-in-pizza [64] Sujoy Roychowdhury、Sumit Soman、HG Ranjani、Neeraj Gunda、Vansh Chhabra 和 Sai Krishna Bala。 2024。电信领域问答的 RAG 指标评估。 arXiv 预印本 arXiv:2407.12873 (2024)。 [65] 埃里克·萨尔瓦乔。 2024 年。挑战生成式人工智能的神话。 https://www. techpolicy.press/challenging-the-myths-of-generative-ai/ [66] Deepa Seetharaman。 2024。https://www.wsj.com/tech/ai/openai-search-enginesearchgpt-97771f86 [67] Chirag Shah 和 Emily M Bender。 2024 年。

### 段落 201 · Page 20

**EN**

Envisioning information access systems: What makes for good tools and a healthy Web? ACM Transactions on the Web 18, 3 (2024), 1–24. [68] Nikhil Sharma, Q Vera Liao, and Ziang Xiao. 2024. Generative Echo Chamber? Effect of LLM-Powered Search Systems on Diverse Information Seeking. In Proceedings of the CHI Conference on Human Factors in Computing Systems . 1–17. [69] Shamane Siriwardhana, Rivindu Weerasekera, Elliott Wen, Tharindu Kaluarachchi, Rajib Rana, and Suranga Nanayakkara. 2023. Improving the domain adaptation of retrieval augmented generation (RAG) models for open domain question answering.

**中文**

设想信息访问系统：什么是好的工具和健康的网络？ ACM 网络交易 18, 3 (2024), 1–24。 [68] 尼基尔·夏尔马 (Nikhil Sharma)，Q Vera Liao，肖子昂。 2024. 生成回声室？法学硕士支持的搜索系统对多样化信息搜索的影响。在 CHI 计算系统中的人为因素会议记录中。 1-17。 [69] Shamane Siriwardhana、Rivindu Weerasekera、Elliott Wen、Tharindu Kaluarachchi、R​​ajib Rana 和 Suranga Nanayakkara。 2023. 改进开放域问答的检索增强生成（RAG）模型的域适应。

### 段落 202 · Page 20

**EN**

Transactions of the Association for Computational Linguistics 11 (2023), 1–17. [70] Elizabeth A St. Pierre and Alecia Y Jackson. 2014. Qualitative data analysis after coding. , 715–719 pages. [71] Liyan Tang, Philippe Laban, and Greg Durrett. 2024. MiniCheck: Efficient Fact- Checking of LLMs on Grounding Documents. arXiv preprint arXiv:2404.10774 (2024). [72] Pranav Venkit, Mukund Srinath, Sanjana Gautam, Saranya Venkatraman, Vipul Gupta, Rebecca J Passonneau, and Shomir Wilson. 2023. The Sentiment Problem: A Critical Survey towards Deconstructing Sentiment Analysis.

**中文**

计算语言学协会汇刊 11 (2023), 1–17。 [70] 伊丽莎白·A·圣皮埃尔和阿莱西亚·Y·杰克逊。 2014.编码后的定性数据分析。，715–719 页。 [71] 唐立言、菲利普·拉班和格雷格·杜雷特。 2024.MiniCheck：法学硕士接地文件的高效事实检查。 arXiv 预印本 arXiv:2404.10774 (2024)。 [72] Pranav Venkit、Mukund Srinath、Sanjana Gautam、Saranya Venkatraman、Vipul Gupta、Rebecca J Passonneau 和 Shomir Wilson。 2023。情绪问题：解构情绪分析的批判性调查。

### 段落 203 · Page 20

**EN**

In Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing . 13743–13763. [73] Pranav Narayanan Venkit, Tatiana Chakravorti, Vipul Gupta, Heidi Biggs, Mukund Srinath, Koustava Goswami, Sarah Rajtmajer, and Shomir Wilson. 2024. " Confidently Nonsensical?”: A Critical Survey on the Perspectives and Challenges of’Hallucinations’ in NLP.arXiv preprint arXiv:2404.07461 (2024). [74] Pranav Narayanan Venkit, Sanjana Gautam, Ruchi Panchanadikar, Ting-Hao Huang, and Shomir Wilson. 2023. Nationality Bias in Text Generation.

**中文**

2023 年自然语言处理经验方法会议论文集。 13743–13763。 [73] Pranav Narayanan Venkit、Tatiana Chakravorti、Vipul Gupta、Heidi Biggs、Mukund Srinath、Koustava Goswami、Sarah Rajtmajer 和 Shomir Wilson。 2024.“自信地荒谬？”：对 NLP.arXiv 预印本 arXiv：2404.07461（2024）中“幻觉”的观点和挑战的批判性调查。 [74] Pranav Narayanan Venkit、Sanjana Gautam、Ruchi Panchanadikar、Ting-Hao Huang 和 Shomir Wilson。 2023.文本生成中的国籍偏见。

### 段落 204 · Page 20

**EN**

In Proceedings of the 17th Conference of the European Chapter of the Association for Computational Linguistics. 116–122. [75] Pranav Narayanan Venkit, Mukund Srinath, and Shomir Wilson. 2023. Automated Ableism: An Exploration of Explicit Disability Biases in Sentiment and Toxicity Analysis Models. In Proceedings of the 3rd Workshop on Trustworthy Natural Language Processing (TrustNLP 2023) . 26–34. [76] PJ Vogt. 2024. How much glue should be in your pizza? https://pjvogt.substack. com/p/how-much-glue-should-be-in-your-pizza [77] Kevin Wu, Eric Wu, and James Zou. 2024. How faithful are RAG models?

**中文**

计算语言学协会欧洲分会第 17 届会议记录。 116-122。 [75] Pranav Narayanan Venkit、Mukund Srinath 和 Shomir Wilson。 2023.自动能力主义：情绪和毒性分析模型中显性残疾偏差的探索。第三届可信自然语言处理研讨会 (TrustNLP 2023) 论文集。 26-34。 [76] PJ 沃格特。 2024. 你的披萨里应该放多少胶水？ https://pjvogt.substack。 com/p/how-much-glue-should-be-in-your-pizza [77] Kevin Wu、Eric Wu 和 James Zou。 2024. RAG 模型有多忠实？

### 段落 205 · Page 20

**EN**

Quantifying the tug-of-war between RAG and LLMs’ internal prior. arXiv preprint arXiv:2404.10198 (2024). [78] Elvin Wyly. 2014. Automated (post) positivism. Urban Geography 35, 5 (2014), 669–690. [79] Kunlun Zhu, Yifan Luo, Dingling Xu, Ruobing Wang, Shi Yu, Shuo Wang, Yukun Yan, Zhenghao Liu, Xu Han, Zhiyuan Liu, et al. 2024. RAGEval: Scenario Specific RAG Evaluation Dataset Generation Framework. arXiv preprint arXiv:2408.01262 (2024).

**中文**

量化 RAG 和 LLM 内部先验之间的拉锯战。 arXiv 预印本 arXiv:2404.10198 (2024)。 [78] 埃尔文·威利。 2014.自动化（后）实证主义。城市GEO学 35, 5 (2014), 669–690. [79] 朱昆仑，罗一帆，徐丁灵，王若兵，石宇，王硕，严玉坤，刘正浩，韩旭，刘志远，等。 2024. RAGEval：场景特定的 RAG 评估数据集生成框架。 arXiv 预印本 arXiv:2408.01262 (2024)。

### Page 21

### 段落 206 · Page 21

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, A Appendix A.1 Pre-Study Questionnaire This pre-study questionnaire was designed to assess participants’ eligibility and gather additional information about their usage of answer engines and generative AI in their daily lives. The questions from the survey below: (1) Please Enter Your Name Short answer response (2) Please Enter Your Age Short answer response (3) Please Select Your Gender • Male • Female • Non-Binary • Genderfluid • Agender • Bigender • Other (4) What is your current profession or job title?

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024 年 6 月 3 日至 5 日，附录 A.1 预研究调查问卷 该预研究调查问卷旨在评估参与者的资格并收集有关他们在日常生活中使用答案引擎和生成人工智能的更多信息。以下调查问题： (1) 请输入您的姓名 简答题 (2) 请输入您的年龄 简答题 (3) 请选择您的性别 • 男 • 女 • 非二元性别 • 流动性别 • 无性别 • 双性别 • 其他 (4) 您目前的职业或职位是什么？

### 段落 207 · Page 21

**EN**

Short answer response (5) What is your current or most recent educational qualification? • High School Degree or Equivalent • Some College, No Degree • Associate Degree • Bachelor’s Degree • Master’s Degree • Doctorate Degree • Other (6) What do you consider are your current field of expertise? Mention at least 3 topics. (Eg: Multilingual Text Summarization, STEM Education Enhancement, Geology, VR Gaming, etc.) Long answer response (7) You are familiar with the concept of RAG (Retrieval Augmented Generation) models or Advanced Search Engine or Generative Search Engine (like perplexity.ai or Bing chat).

**中文**

简答题 (5) 您当前或最近的学历是什么？ • 高中学位或同等学历 • 一些大学，无学位 • 副学士学位 • 学士学位 • 硕士学位 • 博士学位 • 其他 (6) 您认为您目前的专业领域是什么？至少提及 3 个主题。 （例如：多语言文本摘要、STEM 教育增强、地质学、VR 游戏等） 长答案响应 (7) 您熟悉 RAG（检索增强生成）模型或高级搜索引擎或生成式搜索引擎（如 perplexity.ai 或 Bing 聊天）的概念。

### 段落 208 · Page 21

**EN**

• Strongly Disagree • Disagree • Neutral • Agree • Strongly Agree (8) How often do you interact with Generative AI models? (ChatGPT, Stable Diffusion, DALL-E) • Every Day • Several Times a Week • Several Times a Month • Rarely • Never (9) How often do you interact with Generative Search Engine like perplexity.ai, Bing Copilot, Google AI Overview? • Every Day • Several Times a Week • Several Times a Month • Rarely • Never (10) How do you use or foresee using Generative Search Engine?

**中文**

• 非常不同意 • 不同意 • 中立 • 同意 • 非常同意 (8) 您与生成式人工智能模型互动的频率如何？ （ChatGPT、Stable Diffusion、DALL-E） • 每天 • 每周几次 • 每月几次 • 很少 • 从不 (9) 您与 perplexity.ai、Bing Copilot、Google AI Overview 等生成式搜索引擎进行交互的频率如何？ • 每天 • 每周几次 • 每月几次 • 很少 • 从不 (10) 您如何使用或预见使用生成式搜索引擎？

### 段落 209 · Page 21

**EN**

Long answer response (11) Please provide any one of your public social media ID for verification purposes (Eg: LinkedIn, Google Scholar, Company or Institutional profile, etc.) Short answer response (12) To participate in this study, you will need a stable and good internet connection, a device that can share your screen, and a quiet environment for the entire session. Can you meet these requirements? • Yes • No A.2 Participant Data Information We present an anonymized list of participants, in Table 8, highlighting the diversity of expertise and the answer engines utilized by each participant throughout the study.

**中文**

长答案 (11) 请提供您的任何一个公共社交媒体 ID 以供验证之用（例如：LinkedIn、Google Scholar、公司或机构简介等） 短答案 (12) 要参与本研究，您需要稳定且良好的互联网连接、可以共享屏幕的设备以及整个会议的安静环境。你能满足这些要求吗？ • 是 • 否 A.2 参与者数据信息 我们在表 8 中提供了匿名参与者名单，强调了每个参与者在整个研究过程中所使用的专业知识和答案引擎的多样性。

### 段落 210 · Page 21

**EN**

A.3 Additional Community-Centric Themes of Answer Engine Shortfalls L.V. Amplification of Western Context in Generation (12/21): In some of the user studies, participants keenly observed that the contextual assumptions generated by all the three selected answer engine predominantly reflect a Western perspective, even when such assumptions are not explicitly stated . For instance, questions like “Should a government provide universal health care?” or “Should we be vegetarians?” were interpreted as references to the US government and Western cultural norms , regardless of the user’s actual context.

**中文**

A.3 答案引擎缺陷的其他以社区为中心的主题 L.V.西方语境在一代中的放大（12/21）：在一些用户研究中，参与者敏锐地观察到，所有三个选定的答案引擎生成的语境假设主要反映了西方的观点，即使这些假设没有明确说明。例如，诸如“政府应该提供全民医疗保健吗？”之类的问题。或“我们应该吃素吗？”被解释为对美国政府和西方文化规范的参考，无论用户的实际背景如何。

### 段落 211 · Page 21

**EN**

Participants found this problematic, noting that not all contexts should be assumed to align with a Western viewpoint. Participants expressed concerns, with P9 stating, “Yeah, it is interesting that it immediately in the second sentence goes to the US governmental context which I didn’t specify. ”Similarly, P19 noted, “Even for the previous answer, we didn’t mention the country in context and it just took the US context automatically.

**中文**

参与者发现这是有问题的，并指出并非所有情况都应该被假设为与西方观点一致。参与者表达了担忧，P9 表示，“是的，有趣的是，第二句话立即转到了美国政府背景，但我没有具体说明。”同样，P19 指出，“即使对于之前的答案，我们也没有在背景中提及国家，只是自动采用了美国背景。

### 段落 212 · Page 21

**EN**

” P8 also voiced out with an example stating, “For questions on agriculture, it does not give any geographic specifications of other countries like India, for example, where the answer is very cultural and different. ” While acknowledging that the models are primarily developed and used in the United States, participants emphasized the need for these models to recognize and explicitly address this bias, rather than presenting such assumptions with unwarranted confidence.

**中文**

” P8还举例说，“对于农业问题，它没有给出任何其他国家的GEO规格，例如印度，那里的答案非常文化和不同。虽然承认这些模型主要是在美国开发和使用的，但与会者强调这些模型需要认识到并明确解决这种偏见，而不是毫无根据地提出此类假设。

### 段落 213 · Page 21

**EN**

This finding aligns with existing research on text generation models having a Western or Global North alignment and is further exacerbated by the type of sources these models select [4, 25, 56]. Prior works have established how text and image generation models can perpetuate biases and harms due to misalignment, however, the exacerbation of these biases can be seen translated in these answer engines as well. Participants therefore stressed the importance of the models providing contextually appropriate responses that consider diverse cultural perspectives and avoid defaulting to a Western-centric viewpoint.

**中文**

这一发现与现有的关于具有西方或全球北方对齐的文本生成模型的研究相一致，并且这些模型选择的来源类型进一步加剧了这一发现[4,25,56]。先前的工作已经确定了文本和图像生成模型如何因未对准而使偏见和伤害永久化，然而，这些偏见的加剧也可以在这些答案引擎中看到。因此，参与者强调了模型提供适合情境的反应的重要性，这些反应考虑了不同的文化观点并避免默认以西方为中心的观点。

### Page 22

### 段落 214 · Page 22

, June 03–05, 2024, Trovato et al.

### 段落 215 · Page 22

**EN**

Participant ID Field of Work Occupation Model Used P1 Human-Computer Interaction Doctorate Student Perplexity AI P2 Human-Computer Interaction Doctorate Student Perplexity AI P3 Healthcare and Medicine Doctorate Student Perplexity AI P4 Human-Computer Interaction Doctorate Student Perplexity AI P5 Meteorology and Climate Science Postdoctoral Researcher Perplexity AI P6 Human-Computer Interaction Postdoctoral Researcher Bing Copilot P7 Education and Social Sciences Doctorate Student Bing Copilot P8 Transportation Engineering Doctorate Student Bing Copilot P9 Education and Social Sciences Doctorate Student You Chat P10 Information Science Progr

**中文**

参与者 ID 工作领域 使用的职业模型 P1 人机交互 博士生困惑 AI P2 人机交互 博士生困惑 AI P3 医疗保健与医学 博士生困惑 AI P4 人机交互 博士生困惑 AI P5 气象与气候科学 博士后研究员 困惑 AI P6 人机交互 博士后研究员 Bing Copilot P7 教育与社会科学博士学生 Bing 副驾驶 P8 交通工程 博士生 Bing 副驾驶 P9 教育与社会科学 博士生 你聊 P10 信息科学专业

### 段落 216 · Page 22

**EN**

am Manager You Chat P11 Healthcare and Medicine Doctorate Student You Chat P12 Human-Computer Interaction Postdoctoral Researcher You Chat P13 Artificial Intelligence Research Scientist Bing Copilot P14 Education and Social Sciences Doctorate Student Perplexity AI P15 Healthcare and Medicine Doctorate Student Bing Copilot P16 Healthcare and Medicine Doctorate Student You Chat P17 Healthcare and Medicine Doctorate Student Bing Copilot P18 Artificial Intelligence Research Scientist Perplexity AI P19 Human-Computer Interaction Postdoctoral Researcher You Chat P20 Artificial Intelligence Research Scientist Bing Copilot P21 Public Services Medical

**中文**

am 经理您聊 P11 医疗保健与医学博士生您聊 P12 人机交互 博士后研究员您聊 P13 人工智能研究科学家 Bing Copilot P14 教育与社会科学博士生困惑 AI P15 医疗保健与医学博士生 Bing Copilot P16 医疗保健与医学博士生您聊 P17 医疗保健与医学博士生 Bing Copilot P18 人工智能研究科学家困惑 AI P19人机交互 博士后研究员 友聊 P20 人工智能研究科学家 必应副驾驶 P21 公共服务 医疗

### 段落 217 · Page 22

**EN**

Practitioner You Chat P22 Artificial Intelligence Research Scientist Bing Copilot P23 Artificial Intelligence Research Scientist Perplexity AI P24 Artificial Intelligence Research Scientist Perplexity AI Table 8: Overview of participants’ anonymized information, including their professional field and occupation.

**中文**

从业者你聊 P22 人工智能研究科学家 Bing Copilot P23 人工智能研究科学家 Perplexity AI P24 人工智能研究科学家 Perplexity AI 表 8：参与者匿名信息概览，包括其专业领域和职业。

### 段落 218 · Page 22

**EN**

The table also indicates the specific answer engine each participant used. Participants P22 to P24 took part in the pilot study, while the remaining participants were recruited for the primary study. U.V. Forces Answers When There is Not Enough Information (10/21): Another issue on user interaction identified by participants involved answering expert-level questions that needed more context or content for proper answer generation. These types of queries, which we call ‘intractable questions, ’ often do not have clear or straightforward answers available in existing resources.

**中文**

该表还指出了每个参与者使用的特定答案引擎。 P22 至 P24 的参与者参加了试点研究，其余参与者则被招募参加初步研究。紫外线。当信息不足时强制给出答案 (10/21)：参与者发现的另一个关于用户交互的问题涉及回答专家级问题，这些问题需要更多上下文或内容才能生成正确的答案。这些类型的查询，我们称之为“棘手的问题”，通常在现有资源中没有明确或直接的答案。

### 段落 219 · Page 22

**EN**

When participants asked such questions, the answer engines tended to force the generation of whatever limited information they could find from search results, often leading to out-of-context or redundant responses. Participant P7 highlighted this issue by stating, “So it did go to the right domain, but it was not able to find the right answer because that doesn’t exist. There is no one research paper that talks about combining these three elements yet. But it still generates an answer.

**中文**

当参与者提出此类问题时，答案引擎往往会强制生成他们可以从搜索结果中找到的任何有限信息，这通常会导致断章取义或冗余响应。 Participant P7 highlighted this issue by stating, “So it did go to the right domain, but it was not able to find the right answer because that doesn’t exist. There is no one research paper that talks about combining these three elements yet. But it still generates an answer.

### 段落 220 · Page 22

**EN**

” Similarly, P12 noted the problematic approach of the answer engine, saying, "The [answer engine] has pulled out certain terms and then has tried to generate sentences from random parts of the paper that do not answer the question at all. " This suggests that in the absence of adequate content, the answer engine’s attempt to generate a response often results in misleading or irrelevant information. Participants suggest that the answer engine would be more effective in such cases if it could recognize intractable questions and refrain from generating forced answers.

**中文**

” Similarly, P12 noted the problematic approach of the answer engine, saying, "The [answer engine] has pulled out certain terms and then has tried to generate sentences from random parts of the paper that do not answer the question at all. “这表明，在缺乏足够内容的情况下，答案引擎尝试生成响应通常会导致误导或不相关的信息。 Participants suggest that the answer engine would be more effective in such cases if it could recognize intractable questions and refrain from generating forced answers.

### 段落 221 · Page 22

**EN**

Instead, the system should be capable of categorizing these queries as intractable, thereby indicating to the user that a direct answer may not be available. This approach would prevent the dissemination of irrelevant or misleading information, especially in cases where a user is not aware of this shortcoming. A.4 Design Recommendation Explanation S-I. Provide Balanced Answers for Leading Questions: To mitigate bias in responses, it is essential not to assume or reinforce the biases of the user.

**中文**

Instead, the system should be capable of categorizing these queries as intractable, thereby indicating to the user that a direct answer may not be available. This approach would prevent the dissemination of irrelevant or misleading information, especially in cases where a user is not aware of this shortcoming. A.4 设计建议说明 S-I。 Provide Balanced Answers for Leading Questions: To mitigate bias in responses, it is essential not to assume or reinforce the biases of the user.

### 段落 222 · Page 22

**EN**

For topics or questions that are potentially leading or biased, participants in our study strongly indicated the need for neutral and balanced answers. The system should focus on addressing the broader context of the topic rather than providing an expected answer that aligns with any assumed biases. S-II. Provide Objective Details to Claims: Participants frequently observed that the model often lacked objective details to substantiate its claims. It is crucial for answer engines to avoid excessive summarization of sources. Instead, they should provide comprehensive information that supports the claims being made.

**中文**

对于可能具有引导性或偏见的主题或问题，我们研究的参与者强烈表示需要中立和平衡的答案。该系统应该专注于解决该主题的更广泛背景，而不是提供与任何假设的偏见相一致的预期答案。 S-II。为主张提供客观细节：参与者经常观察到该模型往往缺乏客观细节来证实其主张。对于答案引擎来说，避免过度总结来源至关重要。相反，他们应该提供支持所提出的主张的全面信息。

### 段落 223 · Page 22

**EN**

Wherever necessary, responses should include objective details such as percentages, figures, or specific data points to strengthen the credibility of the answer. S-III. Minimize Fluff Information in Answers: Many participants reported instances where the model generated simplistic answers containing irrelevant or extraneous information. Future answer engines should ensure that each sentence in the generated response is contextually accurate and directly relevant to the question posed. If a sentence does not contribute meaningfully to the

**中文**

如有必要，答复应包括客观细节，例如百分比、数字或具体数据点，以增强答复的可信度。 S-III。最大限度地减少答案中的虚假信息：许多参与者报告了模型生成包含不相关或无关信息的简单答案的实例。未来的答案引擎应该确保生成的响应中的每个句子上下文准确并且与提出的问题直接相关。如果一个句子没有对句子做出有意义的贡献

### Page 23

### 段落 224 · Page 23

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, response, it should be reconsidered or omitted to maintain clarity and precision. S-IV. Reflect on Source’s Thoroughness:A significant concern highlighted by participants was the lack of transparency regarding how the system selected and utilized sources. The black-box nature of current models creates distrust, as users are often unclear about the rationale behind the cited sources.

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024 年 6 月 3 日至 5 日，响应，应重新考虑或省略以保持清晰度和精确度。 S-IV。反思来源的完整性：参与者强调的一个重要问题是系统如何选择和利用来源缺乏透明度。当前模型的黑匣子性质造成了不信任，因为用户往往不清楚引用来源背后的基本原理。

### 段落 225 · Page 23

**EN**

To address this, an additional trust layer should be incorporated, providing users with insights into why specific sources were used and how they contribute to the generated answer. This transparency will enhance users’ ability to critically evaluate the response. C-I. Avoid Unsupported Citations: Participants observed that many statements generated by answer engines lacked proper citations, particularly when making claims that required supporting references. It is crucial to evaluate each statement’s need for citation, ensuring that claims are backed by relevant sources retrieved by the model.

**中文**

为了解决这个问题，应该加入一个额外的信任层，让用户深入了解为什么使用特定来源以及它们如何对生成的答案做出贡献。这种透明度将增强用户批判性评估响应的能力。 C-I。避免不受支持的引用：参与者观察到，答案引擎生成的许多陈述缺乏适当的引用，特别是在提出需要支持参考文献的声明时。评估每个陈述的引用需求至关重要，确保声明得到模型检索到的相关来源的支持。

### 段落 226 · Page 23

**EN**

If a statement cannot be properly cited, the system should either remove the statement or clearly indicate its relevance to the overall answer. C-II. Double-Check for Misattribution: Misattribution was another common issue identified by participants, where sources were cited out of context or incorrectly attributed. To prevent this, answer engines should externally evaluate citations by considering the full content of the source rather than just a fragment. Additionally, revealing which part of the source contains the cited information can help reduce instances of misattribution, ensuring greater accuracy in the generated answers. C-III.

**中文**

如果无法正确引用某个陈述，系统应删除该陈述或明确指出其与整体答案的相关性。 C-II。仔细检查错误归因：错误归因是参与者发现的另一个常见问题，即断章取义或错误归因。为了防止这种情况，答案引擎应该通过考虑源的完整内容而不仅仅是一个片段来外部评估引文。此外，揭示来源的哪一部分包含引用的信息可以帮助减少错误归因的情况，确保生成的答案更加准确。 C-III。

### 段落 227 · Page 23

**EN**

Cite All Relevant Sources for a Claim: Participants found it confusing when answer engines cited only one source for claims that clearly required multiple references. This practice hindered their ability to discern the importance of different points within the response. To address this, models should cite all relevant sources wherever necessary, helping users understand the breadth of support for a given claim. This approach reduces the likelihood of giving undue attention to non-important points or sources that mention irrelevant information. C-IV.

**中文**

引用声明的所有相关来源：当答案引擎仅引用显然需要多个引用的声明的一个来源时，参与者会感到困惑。这种做法阻碍了他们辨别响应中不同点重要性的能力。为了解决这个问题，模型应该在必要时引用所有相关来源，帮助用户了解给定主张的支持范围。这种方法减少了对不重要的点或提及不相关信息的来源给予过度关注的可能性。 C-IV。

### 段落 228 · Page 23

**EN**

Retrieved Sources Must be Equal to Used Sources: Participants noted that some answer engines, like Bing Copilot and Perplexity, retrieved more sources than were actually used in the generated answers. This practice led to a confusion of trust, where users believed that many sources were used to construct the answer when, in reality, only a small percentage were utilized. To maintain transparency and trust, it is essential that the number of retrieved sources matches the number of sources actually used in the response. This alignment ensures users can accurately assess the reliability of the generated information. S-I.

**中文**

检索到的来源必须等于使用的来源：参与者指出，一些答案引擎（例如 Bing Copilot 和 Perplexity）检索到的来源多于生成答案中实际使用的来源。这种做法导致了信任的混乱，用户认为使用了许多来源来构建答案，但实际上只利用了一小部分。为了保持透明度和信任，检索到的源数量必须与响应中实际使用的源数量相匹配。这种一致性确保用户可以准确评估生成信息的可靠性。 S-I。

### 段落 229 · Page 23

**EN**

Give Explicit Attention to Expert Sources: Participants observed that answer engines often fail to prioritize authoritative sources, such as research papers or government websites, even when these sources provide the most accurate information. Instead, the system tends to distribute attention equally among various types of content, including less reliable sources like blog posts and opinion pieces. It is crucial that the system recognizes and prioritizes expert sources, particularly when they offer definitive answers (e.g., CDC for COVID-19 updates).

**中文**

明确关注专家来源：参与者观察到，答案引擎通常无法优先考虑权威来源，例如研究论文或政府网站，即使这些来源提供了最准确的信息。相反，系统倾向于在各种类型的内容之间平均分配注意力，包括博客文章和观点文章等不太可靠的来源。系统识别专家来源并对其进行优先级排序至关重要，特别是当他们提供明确的答案时（例如 CDC 的 COVID-19 更新）。

### 段落 230 · Page 23

**EN**

The source’s authority should take precedence over search engine ranking, ensuring that the most reliable information forms the core of the response. S-II. Retrieve and Use Only Necessary Sources: There were instances where the model retrieved sources that were either inaccurate or irrelevant to the question asked. Although these sources were marked as relevant by the search engine, they were not utilized in generating the final answer, sometimes limiting the response to a single source.

**中文**

消息来源的权威性应优先于搜索引擎排名，确保最可靠的信息成为回应的核心。 S-II。仅检索和使用必要的来源：在某些情况下，模型检索的来源要么不准确，要么与所提出的问题无关。尽管这些来源被搜索引擎标记为相关，但它们并未用于生成最终答案，有时将响应限制为单个来源。

### 段落 231 · Page 23

**EN**

To improve the accuracy and relevance of answers, the model should be more selective in retrieving sources, ensuring that only those necessary for constructing a precise and contextually appropriate response are used. Irrelevant sources should be discarded to make way for more suitable alternatives, or, if none exist, the system should acknowledge the lack of appropriate sources. S-III. Differentiate Source-Based vs. Model-Generated Content: Answer engines are designed to retrieve and synthesize information from the web, minimizing the risk of hallucination—generating content not grounded in reality.

**中文**

为了提高答案的准确性和相关性，模型在检索来源时应更具选择性，确保仅使用构建精确且上下文适当的响应所必需的内容。应丢弃不相关的来源，以便为更合适的替代方案让路，或者，如果不存在，系统应承认缺乏适当的来源。 S-III。区分基于源的内容与模型生成的内容：答案引擎旨在检索和合成来自网络的信息，最大限度地减少产生幻觉的风险 - 生成不基于现实的内容。

### 段落 232 · Page 23

**EN**

However, participants noted several instances where significant claims or sentences lacked citations, leaving users uncertain of their origin. These uncited statements are likely generated from the model’s training data rather than retrieved sources. While these statements may be factually correct, the inability to distinguish them from retrieved content undermines trust. To address this, the system should differentiate model-generated content from source-based content, perhaps through color coding or disclaimers, enhancing transparency and user trust in the system. S-IV.

**中文**

然而，参与者指出了一些重要主张或句子缺乏引用的情况，导致用户不确定其来源。这些未引用的陈述可能是从模型的训练数据而不是检索到的来源生成的。虽然这些陈述实际上可能是正确的，但无法将它们与检索到的内容区分开来会破坏信任。为了解决这个问题，系统应该通过颜色编码或免责声明来区分模型生成的内容和基于源的内容，从而增强透明度和用户对系统的信任。 S-IV。

### 段落 233 · Page 23

**EN**

Explicitly Mention and be Aware of Source Types: The origin and type of a source are critical factors in determining its reliability. Participants noted that, when using traditional search engines, they typically assess the credibility of a source before trusting its information. This behavior was less evident when using answer engines, where the source type and origin were not always transparent. Participants recommended that answer engines become more discerning about source types and their relevance to the question.

**中文**

明确提及并注意来源类型：来源的来源和类型是确定其可靠性的关键因素。参与者指出，在使用传统搜索引擎时，他们通常会在信任其信息之前评估来源的可信度。当使用答案引擎时，这种行为不太明显，其中源类型和来源并不总是透明的。参与者建议答案引擎对来源类型及其与问题的相关性变得更加敏锐。

### 段落 234 · Page 23

**EN**

The top search results are not always the most accurate; hence, the model should intelligently assess and prioritize source types, ensuring that the most credible and relevant sources are used to generate answers. U-I. Incorporate Human Feedback on Sources and Text: One significant limitation identified by participants was the restricted interactivity within the answer engine’s interface. Users were not given the option to modify sources or provide feedback on how the generated content could be improved. To enhance the quality and relevance of the generated answers, it is recommended to implement a human feedback system.

**中文**

排名靠前的搜索结果并不总是最准确的；因此，该模型应该智能地评估来源类型并确定优先级，确保使用最可信和最相关的来源来生成答案。 U-I。将人类反馈纳入来源和文本：参与者发现的一个重大限制是答案引擎界面内的交互性受到限制。用户无法选择修改来源或提供有关如何改进生成的内容的反馈。为了提高生成答案的质量和相关性，建议实施人工反馈系统。

### 段落 235 · Page 23

**EN**

This would allow users to contribute insights on the search results and suggest adjustments, leading to more accurate and contextually relevant responses. U-II. Implement Interactive Citations (e.g., on Hover): Answer engines are increasingly used as sociotechnical systems across various fields, including education, IT, and healthcare, where they are expected to provide quick and reliable answers. However, the use of citations—a familiar tool in academic contexts—is not as intuitive for many users in their daily lives.

**中文**

这将使用户能够对搜索结果提供见解并提出调整建议，从而获得更准确且与上下文相关的响应。 U-II。实施交互式引文（例如，悬停时）：答案引擎越来越多地用作各个领域的社会技术系统，包括教育、IT 和医疗保健，人们期望它们能够提供快速可靠的答案。然而，引文（学术环境中常见的工具）的使用对于许多用户在日常生活中并不那么直观。

### 段落 236 · Page 23

**EN**

Participants suggested the development of interactive citations, such as on-hover pop-ups, which would display detailed source information when users hover over a citation. This feature could encourage users to verify the information and understand the source content more thoroughly, thereby increasing the reliability and usability of the system. U-III. Incorporate Paragraph-Level Local Citations: Currently, answer engines often place citations at the end of sentences,

**中文**

参与者建议开发交互式引文，例如悬停弹出窗口，当用户将鼠标悬停在引文上时，它将显示详细的来源信息。该功能可以鼓励用户更彻底地验证信息并理解源内容，从而提高系统的可靠性和可用性。 U-III。合并段落级本地引用：目前，答案引擎通常将引用放在句子末尾，

### Page 24

### 段落 237 · Page 24

**EN**

, June 03–05, 2024, Trovato et al. which can create confusion about whether the entire sentence or just part of it was sourced from the cited reference. Participants expressed uncertainty when it was unclear which parts of the sentence were directly supported by the source. To address this issue, the system should implement paragraph-level local citations, clearly indicating exactly what information was cited and from where. This approach would improve transparency and help users better understand the relationship between the generated content and its sources. U-IV.

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。这可能会导致人们混淆整个句子或其中的一部分是否来自引用的参考文献。当不清楚句子的哪些部分得到消息来源的直接支持时，参与者表示不确定。为了解决这个问题，系统应该实施段落级本地引用，明确指出引用了哪些信息以及来自何处。这种方法将提高透明度并帮助用户更好GEO解生成的内容与其来源之间的关系。 U-IV。

### 段落 238 · Page 24

**EN**

Avoid Forced Answers When Information is Insufficient: Participants observed that answer engines often generate responses even when there is insufficient information or when the question has no legitimate answer. This tendency can result in the dissemination of misinformation or fabricated content. For instance, when faced with a question about a non-existent concept, such as "Does the theorem of Law dispersion explain relative accentuation?" the system should recognize that no such theorem exists and explicitly state that no answer is available.

**中文**

信息不足时避免强制回答：参与者观察到，即使信息不足或问题没有合法答案，答案引擎也经常会生成响应。这种趋势可能导致错误信息或捏造内容的传播。例如，当面对一个不存在的概念的问题时，例如“法律色散定理能否解释相对强调？”系统应该认识到不存在这样的定理，并明确指出没有可用的答案。

### 段落 239 · Page 24

**EN**

Similarly, when information is insufficient, the system should refrain from generating an answer, thereby preventing the spread of inaccurate or misleading information. A.5 Score Card Metrics Thresholds Table 7 establishes the benchmark ranges for the eight Answer Engine Evaluation (AEE) metrics, categorizing performance into three levels: ▲acceptable, ●borderline, and ▼problematic. These thresholds serve to quantify the usability and trustworthiness of answer engines, allowing for a clear division between good, moderate, and poor system performance.

**中文**

同样，当信息不足时，系统应避免生成答案，从而防止不准确或误导性信息的传播。 A.5 记分卡指标阈值 表 7 建立了八个答案引擎评估 (AEE) 指标的基准范围，将性能分为三个级别：▲可接受、●临界和▼有问题。这些阈值用于量化答案引擎的可用性和可信度，从而明确区分良好、中等和较差的系统性能。

### 段落 240 · Page 24

**EN**

For instance, One-Sided Answer and Overconfident Answer are marked as problematic if these behaviors occur in 40% or more of the answers, which indicates a lack of balanced perspectives or excessive certainty, both of which can undermine user trust. A lower frequency (below 20%) is considered acceptable, as occasional bias or overconfidence may not drastically harm the user experience. Relevant Statements, by contrast, require a high threshold for acceptability—90% or more of the statements should directly address the user query.

**中文**

例如，如果 40% 或更多的答案中出现单方面答案和过度自信的答案，则这些行为将被标记为有问题，这表明缺乏平衡的观点或过度确定性，这两者都会损害用户的信任。较低的频率（低于 20%）被认为是可以接受的，因为偶尔的偏见或过度自信可能不会严重损害用户体验。相比之下，相关语句需要较高的可接受性阈值——90% 或更多的语句应直接解决用户查询。

### 段落 241 · Page 24

**EN**

Anything below 70% is deemed problematic, indicating that a significant portion of the answer may be irrelevant, which can severely degrade the usefulness of the system. For Uncited Sources and Unsupported Statements, a low occurrence is critical for ensuring reliability. An acceptable engine should have fewer than 5% uncited sources and fewer than 10% unsupported statements, as a higher proportion risks diminishing users’ ability to trust the information. Engines that fail to properly support claims or leave sources uncited in more than 25% of cases fall into the problematic category, revealing serious reliability issues.

**中文**

任何低于 70% 的值都被认为是有问题的，这表明答案的很大一部分可能是不相关的，这可能会严重降低系统的实用性。对于未引用的来源和不受支持的陈述，低发生率对于确保可靠性至关重要。可接受的引擎应包含少于 5% 的未引用来源和少于 10% 的不受支持的陈述，因为较高比例可能会降低用户信任信息的能力。在超过 25% 的案例中，未能正确支持索赔或未注明来源的发动机属于有问题的类别，揭示了严重的可靠性问题。

### 段落 242 · Page 24

**EN**

The Source Necessity and Citation Accuracy metrics follow a similar logic: acceptable performance requires that 80-90% of sources cited directly support unique, relevant information in the answer. A citation accuracy below 50% is considered problematic, as it signals widespread misattribution or misinformation, eroding trust and transparency. Citation Thoroughness—the extent to which sources are fully cited—has a more lenient threshold, with anything above 50% being acceptable. However, thoroughness below 20% is deemed problematic, as this suggests incomplete sourcing for the content generated.

**中文**

来源必要性和引文准确性指标遵循类似的逻辑：可接受的性能要求 80-90% 的引用来源直接支持答案中独特的相关信息。低于 50% 的引用准确性被认为是有问题的，因为它表明存在广泛的错误归因或错误信息，从而削弱了信任和透明度。引文彻底性（来源被充分引用的程度）的阈值更为宽松，任何超过 50% 的内容都是可以接受的。然而，低于 20% 的彻底性被认为是有问题的，因为这表明生成的内容的来源不完整。

### 段落 243 · Page 24

**EN**

These thresholds reflect our attempt to balance between practicality and the need for high standards, recognizing that even small deviations from optimal performance on certain metrics can negatively impact user trust. These benchmarks are designed with flexibility in mind, acknowledging that the acceptable ranges may evolve as user expectations rise and technology improves. For example, a current threshold of 90% citation accuracy may be sufficient now, but as answer engines advance, this could shift to higher expectations of near-perfect accuracy and relevance.

**中文**

这些阈值反映了我们在实用性和高标准需求之间寻求平衡的尝试，认识到即使某些指标上的最佳性能出现微小偏差也会对用户信任产生负面影响。这些基准的设计考虑到了灵活性，承认可接受的范围可能会随着用户期望的提高和技术的改进而变化。例如，目前 90% 的引用准确性阈值现在可能就足够了，但随着答案引擎的进步，这可能会转变为对近乎完美的准确性和相关性的更高期望。

### 段落 244 · Page 24

**EN**

A.6 LLM Judge Prompts Used for Evaluation In this section, we present the LLM instructions used to automate tasks for the AEE scorecard evaluation. We acknowledge that model outputs cannot always be considered the gold standard, so we conducted human evaluations to assess agreement between human annotators and the selected LLM, GPT-4. The results are detailed in Section 4.2. The prompts are as follows:

**中文**

A.6 用于评估的 LLM 法官提示 在本节中，我们介绍用于自动执行 AEE 记分卡评估任务的 LLM 指令。我们承认模型输出并不总是被视为黄金标准，因此我们进行了人工评估，以评估人工注释者与所选 LLM、GPT-4 之间的一致性。结果详见第 4.2 节。提示如下：

### Page 25

### 段落 245 · Page 25

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, Confidence Parameter Evaluation You are given a user Query , and the Answer generated by a system . Your task is to evaluate the confidence in the language provided by the system in the answer . You must choose one of five confidence levels . Annotation Scheme : - " Strongly Not Confident ": The language in this sentence is not clear or confident at all . - " Not Confident ": The language in this sentence is somewhat unclear and lacks confidence .

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024 年 6 月 3 日至 5 日，置信度参数评估 您将收到一个用户查询，以及由系统生成的答案。您的任务是评估系统在答案中提供的语言的置信度。您必须选择五个置信水平之一。注释方案： -“强烈不自信”：这句话的语言根本不明确或不自信。 -“不自信”：这句话的语言有些不清楚，缺乏自信。

### 段落 246 · Page 25

**EN**

- " Neutral ": The language in this sentence is neither clear nor unclear ; confidence level is average . - " Confident ": The language in this sentence is clear and fairly confident . - " Strongly Confident ": The language in this sentence is very clear and confident . Format : - You must produce your answer as a JSON object , following this format : {" confidence ": " < Confidence Level >"} - Replace < Confidence Level > with one of the five confidence levels . - Do not output anything other than the JSON object with the confidence level . Query : [[ QUERY ]] Answer : [[ ANSWER ]]

**中文**

- “中性”：这句话的语言既不明确也不不清楚；置信度处于平均水平。 -“自信”：这句话的语言清晰，相当自信。 -“非常自信”：这句话的语言非常清晰和自信。格式： - 您必须按照以下格式将答案生成为 JSON 对象：{"confidence":"<Confidence Level>"} - 将 <Confidence Level> 替换为五个置信级别之一。 - 除了具有置信度的 JSON 对象之外，不要输出任何内容。查询 : [[ 查询 ]] 回答 : [[ 答案 ]]

### Page 26

### 段落 247 · Page 26

**EN**

, June 03–05, 2024, Trovato et al. Relevant Statement Extraction You are given a paragraph , made of a sequence of sentences that answer the following question : [[ QUESTION ]] Your task is to extract , in JSON format , what the individual sentences are , and then identify for each sentence whether it contains a core statement that answers the question , or if it is a filler sentence that does not contain substantial information .

**中文**

，2024 年 6 月 3 日至 5 日，Trovato 等人。相关语句提取 给您一个段落，由回答以下问题的一系列句子组成：[[问题]] 您的任务是以 JSON 格式提取各个句子的内容，然后确定每个句子是否包含回答问题的核心语句，或者是否是不包含大量信息的填充句子。

### 段落 248 · Page 26

**EN**

You should follow the following format : {" sentences ": {" sentence ": "..." , " core ": "1|0"} , {" sentence ": "..." , " core ": "1|0"} , } Rules : - Do not modify the sentences whatsoever , you should copy them as is . - Do not modify the order of the sentences , or skip any of the sentences . - The sentences optionally contain citations ( e . g . [1] , [2] , etc .) . You should not modify the citations , keep them as is . - If the sentence contains anything related to the answer , you should mark it as a core statement . Sentences with a citation are almost always core statements .

**中文**

您应该遵循以下格式：{"句子"：{"句子"："..."，"核心"："1|0"}，{"句子"："..."，"核心"："1|0"}，} 规则： - 请勿修改句子，应按原样复制它们。 - 不要修改句子的顺序，或跳过任何句子。 - 句子可选地包含引文（例如[1]、[2]等）。您不应修改引文，应保持原样。 - 如果句子包含与答案相关的任何内容，则应将其标记为核心陈述。带有引文的句子几乎总是核心陈述。

### 段落 249 · Page 26

**EN**

- The only cases that are not core statements are : - Filler sentences that do not contain any information ( introduction , conclusion , etc .) Here is the answer you should decompose : ``` [[ ANSWER ]] ```

**中文**

- 唯一不属于核心陈述的情况是： - 不包含任何信息的填充句子（引言、结论等） 这是您应该分解的答案：``` [[ ANSWER ]] ```

### Page 27

### 段落 250 · Page 27

**EN**

Search Engines in an AI Era: The False Promise of Factual and Verifiable Source-Cited Responses , June 03–05, 2024, Supported Statement Evaluation You are given the full text of a document , and a statement ( a sentence ) . Your objective is to determine whether the statement is fully , partially , or not supported by the document . You should output a JSON object with the following format : {" support ": " full | partial | none "} Document : ``` [[ DOCUMENT ]] ``` Statement : [[ STATEMENT ]] Rules : - The statement may contain citations ( e . g . [1] , [2] , etc .) . You do not need to consider the citations when determining support .

**中文**

人工智能时代的搜索引擎：事实和可验证的来源引用响应的虚假承诺，2024 年 6 月 3 日至 5 日，支持的声明评估 您将获得文档的全文和声明（句子）。您的目标是确定文档是否完全、部分支持该陈述。您应该输出以下格式的 JSON 对象： {" support ": " full |partial | none "} 文档 : ``` [[ DOCUMENT ]] ``` 语句 : [[ STATMENT ]] 规则 : - 语句可以包含引用（例如 [1]、 [2] 等）。确定支持时无需考虑引用。

### 段落 251 · Page 27

**EN**

- Only output valid JSON . Do not include any other information in the output . One-sided Answer Detection You are given a query that is opinionated ( on one side of an issue ) . You are then given a numbered list of statements . Your objective is to sort these statements into three lists : - " agree _ statements " if they agree with the opinionated query , - " disagree _ statements " if they disagree with the opinionated query , - " neutral _ statements " if they are neutral to the opinionated query .

**中文**

- 只输出有效的 JSON。不要在输出中包含任何其他信息。片面答案检测 您会收到一个固执己见的问题（针对问题的一方面）。然后您会得到一份经过编号的语句列表。您的目标是将这些陈述分为三个列表： - 如果他们同意固执己见的查询，则为“同意_陈述”； - 如果他们不同意固执己见的查询，则为“不同意_陈述”； - 如果他们对固执己见的查询持中立态度，则为“中立_陈述”。

### 段落 252 · Page 27

**EN**

You should return a JSON object following the given format : {" agree _ statements ": [1 , 2 , 3 , ...] , " disagree _ statements ": [4 , 5 , 6 , ...] , " neutral _ statements ": [7 , 8 , 9 , ...]} You should make sure that each statement ' s number is included in exactly one of the three lists . Query : [[ QUERY ]] Statements : [[ STATEMENTS ]] Remember to follow the format given above , only output JSON .

**中文**

您应该按照给定的格式返回一个 JSON 对象： {"apprece_statements": [1, 2, 3, ...], "agree_statements": [4, 5, 6, ...], "neutral_statements": [7, 8, 9, ...]} 您应该确保每个语句的编号恰好包含在三个列表之一中。查询：[[ QUERY ]] 语句：[[ STATEMENTS ]] 记住要遵循上面给出的格式，只输出 JSON。
