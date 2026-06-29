# The Attribution Crisis in LLM Search Results

- ID: 71
- 类型: pdf
- 分类: 04_academic_papers
- 主题: web-enabled LLM attribution gap
- 原文链接: https://arxiv.org/pdf/2508.00838
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

The Attribution Crisis in LLM Search Results Estimating Ecosystem Exploitation Ilan Strauss1,2, Jangho Yang4, Tim O’Reilly1,3, Sruly Rosenblat1, and Isobel Moure∗1 1AI Disclosures Project (Social Science Research Council) 2Institute for Innovation and Public Purpose (University College London) 3O’Reilly Media 4University of Waterloo Abstract Web-enabled LLMs frequently answer queries without crediting the web pages they consume, creatingan“attribution gap”–thedifferencebetweenrelevant URLsreadand those actually cited.

**中文**

LLM 检索结果中的归因危机 估计生态系统开发 Ilan Strauss1,2、Jangho Yang4、Tim O’Reilly1,3、Sruly Rosenblat1 和 Isobel Moure*1 1AI 披露项目（社会科学研究委员会） 2 创新与公共目的研究所（伦敦大学学院） 3O’Reilly Media 4 滑铁卢大学 摘要 网络支持的法学硕士经常在回答查询时不署名他们消费的网页，造成了“归因差距”——阅读的相关 URL 与实际引用的 URL 之间的差异。

### 段落 2 · Page 1

**EN**

Drawing on approximately 14,000 real-world LMArena conversation logs with search-enabled LLM systems, we document three exploitation patterns: 1) No Search: 34% of Google Gemini and 24% of OpenAI GPT-4o responses are generated without explicitly fetching any online content; 2)No citation: Gemini provides no clickable citation source in 92% of answers; 3)High-volume, low-credit: Perplexity’s Sonar visits approximately 10 relevant pages per query but cites only three to four.

**中文**

利用支持搜索的 LLM 系统的大约 14,000 个真实世界的 LMArena 对话日志，我们记录了三种利用模式： 1) 无搜索：34% 的 Google Gemini 和 24% 的 OpenAI GPT-4o 响应是在没有显式获取任何在线内容的情况下生成的； 2）无引用：Gemini 92%的答案没有提供可点击的引用来源； 3）高容量、低信用：Perplexity 的 Sonar 每次查询会访问大约 10 个相关页面，但仅引用三到四个。

### 段落 3 · Page 1

**EN**

A negative binomial hurdle model shows that the average query answered by Gemini or Sonar leaves about 3 relevant websites uncited, whereas GPT-4o’s tiny uncited gap is best explained by its selective log disclosures rather than by better attribution. Citation efficiency – extra citations provided per additional relevant web page visited – varies widely across models, from 0.19 to 0.45 on identical queries, underscoring that retrieval design, not technical limits, shapes ecosystem impact. We recommend a transparent LLM search architecture based on standardized telemetry and full disclosure of search traces and citation logs.

**中文**

负二项式障碍模型显示，Gemini 或 Sonar 回答的平均查询留下大约 3 个未引用的相关网站，而 GPT-4o 的微小未引用差距最好是通过其选择性日志披露而不是更好的归因来解释。引用效率（每次访问额外的相关网页所提供的额外引用）在不同模型中差异很大，相同查询的引用效率从 0.19 到 0.45 不等，这强调了检索设计而不是技术限制决定了生态系统的影响。我们推荐基于标准化遥测和完全公开搜索跟踪和引文日志的透明法学硕士搜索架构。

### 段落 4 · Page 1

**EN**

Keywords: LLM Search, citations, content monetization, ecosystem exploitation, large language models. ∗We gratefully acknowledge funding support from The Alfred P. Sloan Foundation, the Omidyar Network, and the Patrick J. McGovern Foundation. We extend our appreciation to the people we have had conversations with that have shaped our thinking.Contact: istrauss@ssrc.org / ilan@aidisclosures.org.Code and Data: https://github.com/AI-Disclosures-Project/Ecosystem_Exploitation_In_Search_Results. arXiv:2508.00838v1 [cs.DL] 27 Jun 2025

**中文**

关键词：LLM 搜索、引用、内容货币化、生态系统开发、大型语言模型。 *我们衷心感谢阿尔弗雷德·P·斯隆基金会、奥米迪亚网络和帕特里克·J·麦戈文基金会的资助。我们向那些与我们进行过对话并塑造了我们思维的人们表示感谢。联系方式：istrauss@ssrc.org / ilan@aidisclosures.org。代码和数据：https://github.com/AI-Disclosures-Project/Ecosystem_Exploitation_In_Search_Results。 arXiv:2508.00838v1 [cs.DL] 2025 年 6 月 27 日

### Page 2

### 段落 5 · Page 2

**EN**

Contents 1 Introduction 1 2 Data and Method 4 2.1 Key Variables and Measurement . . . . . . . . . . . . . . . . . . . . . . . . . 5 3 Descriptive Patterns 6 4 Regression Models 7 4.1 Hurdle-Model Specification . . . . . . . . . . . . . . . . . . . . . . . . . . . . 7 4.2 Head-to-Head Model Comparison Regression . . . . . . . . . . . . . . . . . . 9 5 Regression Findings 10 5.1 Attribution Gap Regression Model . . . . . . . . . . . . . . . . . . . . . . . 10 5.2 Head-to-Head Model Results: Citation efficiency . . . . . . . . . . . . . . . .

**中文**

目录 1 简介 1 2 数据和方法 4 2.1 关键变量和测量。。。。。。。。。。。。。。。。。。。。。。。。。 5 3 描述性模式 6 4 回归模型 7 4.1 障碍模型规范。。。。。。。。。。。。。。。。。。。。。。。。。。。。 7 4.2 头对头模型比较回归。。。。。。。。。。。。。。。。。。 9 5 回归结果 10 5.1 归因差距回归模型。。。。。。。。。。。。。。。。。。。。。。。 10 5.2 头对头模型结果：引用效率。。。。。。。。。。。。。。。。

### 段落 6 · Page 2

**EN**

12 6 Policy Implications 14 7 Conclusion 16 8 Appendix 21 8.1 Full Hurdle-Model Specification and Diagnostics . . . . . . . . . . . . . . . . 21 8.2 Detailed Model Results . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 22 8.3 Head-to-Head Regressions: Table of results . . . . . . . . . . . . . . . . . . . 25

**中文**

12 6 政策影响 14 7 结论 16 8 附录 21 8.1 完整的障碍模型规范和诊断。。。。。。。。。。。。。。。。 21 8.2 详细模型结果。。。。。。。。。。。。。。。。。。。。。。。。。。。。。。 22 8.3 头对头回归：结果表。。。。。。。。。。。。。。。。。。。 25

### Page 3

### 段落 7 · Page 3

**EN**

1 Introduction “The misery of being exploited by capitalists is nothing compared to the misery of not being exploited at all.” – Joan Robinson,Economic Philosophy, 1962. The rapid integration of large language models (LLMs) into information-seeking workflows has fundamentally transformed how users access and interact with content on the world wide web. Search-augmented LLMs, which combine generative capabilities with real-time web retrieval, promise to deliver more accurate, up-to-date, and comprehensive responses than traditional chatbots limited to just their training data [13].

**中文**

1 引言 “被资本家剥削的痛苦与根本不被剥削的痛苦相比根本不算什么。” – Joan Robinson，经济哲学，1962 年。大型语言模型 (LLM) 快速集成到信息查找工作流程中，从根本上改变了用户访问万维网内容并与之交互的方式。搜索增强的法学硕士将生成能力与实时网络检索相结合，与仅限于训练数据的传统聊天机器人相比，有望提供更准确、最新和全面的响应 [13]。

### 段落 8 · Page 3

**EN**

But questions have been raised about source accuracy [25], intellectual property rights, scraping websites without permission – so-called ‘access violations’ [4, 22], and what we term“ecosystem exploitation”–the gap between relevant web content consumed by the LLM when answering a query and those sources cited in the model’s output (its response).1 This attribution gap has serious implications for the digital ecosystem on which AI’s ongoing utility depends. Content creators, publishers, and knowledge producers rely on appropriate attribution and licensing agreements when their information is used to answer queries.

**中文**

但人们对来源准确性 [25]、知识产权、未经许可抓取网站（即所谓的“访问违规”[4, 22]，以及我们所说的“生态系统利用”）提出了疑问，即法学硕士在回答查询时消耗的相关网络内容与模型输出（其响应）中引用的来源之间的差距。1这种归因差距对人工智能持续效用所依赖的数字生态系统产生了严重影响。内容创建者、出版商和知识生产者在使用其信息来回答查询时依赖适当的归属和许可协议。

### 段落 9 · Page 3

**EN**

When LLMs systematically consume relevant content without adequate citation or remuneration, they undermine the incentive structures that support high-quality information production and threaten the economic viability of content creation at scale [18].2 This systematic lack of attribution of the content sources consumed by LLMs during web search is a widely known issue [2, 10, 20].3 Yet major LLM vendors reveal little about how their retrieval-augmented generation (RAG) pipelines choose and ingest web content, and how they cite appropriate web sources [26].

**中文**

当法学硕士在没有足够引用或报酬的情况下系统地消耗相关内容时，他们会破坏支持高质量信息生产的激励结构，并威胁大规模内容创建的经济可行性[18]。2 法学硕士在网络搜索过程中系统性地缺乏对法学硕士所消耗的内容来源的归属是一个众所周知的问题[2,10,20]。3然而，主要的法学硕士供应商很少透露他们的检索增强生成（RAG）管道如何选择和摄取网络内容，以及他们如何引用适当的网络资源[26]。

### 段落 10 · Page 3

**EN**

Research questions: To what extent do search-augmented LLMs exploit the web — using content without citing it? And what distinguishes today’s best and worst attribution practices? Method and Data. Using an LMArena dataset of≈14,000 real-world answers to around 7,000 multi-turn queries taken between March and April 2025, we analyze the “attribution gap” exhibited by 11 LLM search-enabled models across three provider families: OpenAI (GPT-4o), Perplexity (Sonar), and Google (Gemini).

**中文**

研究问题：搜索增强法学硕士在多大程度上利用网络——使用内容而不引用它？当今最好和最差的归因实践有何区别？方法和数据。使用 LMArena 数据集，该数据集包含 2025 年 3 月至 4 月期间约 7,000 个多轮查询的约 14,000 个真实答案，我们分析了三个提供商系列中 11 个支持搜索的 LLM 模型所表现出的“归因差距”：OpenAI (GPT-4o)、Perplexity (Sonar) 和 Google (Gemini)。

### 段落 11 · Page 3

**EN**

We define the attribution gap as the number ofrelevant URLs visited by the LLM system when answering the query minus the 1We use ‘consume’, ‘read’, and ‘search’ interchangeably for a relevant website visit logged by the LLM. 2For previous research empirical research on attribution practices across commercial LLM systems see Fayyazi et al. [6], Gao et al. [8], Huang et al. [12], Li et al. [16], Profound [19], Yue et al. [27]. 3As recently as June 2025 the BBC threatened Perplexity’s search system with legal action for using its content during search [20].

**中文**

我们将归因差距定义为法学硕士系统在回答查询时访问的相关 URL 的数量减去 1。对于法学硕士记录的相关网站访问，我们可互换地使用“消费”、“阅读”和“搜索”。 2有关商业法学硕士系统归因实践的先前研究实证研究，请参阅 Fayyazi 等人。 [6]，高等人。 [8]，黄等人。 [12]，李等人。 [16]，深刻[19]，Yue等人。 [27]。 3 就在 2025 年 6 月，BBC 威胁 Perplexity 的搜索系统对其在搜索过程中使用其内容的行为采取法律行动 [20]。

### 段落 12 · Page 3

**EN**

Perplexity has set-up a revenue-sharing program with some publishers and increased citation of sources in response to accusations against it [2]. 1

**中文**

Perplexity 与一些出版商建立了收入共享计划，并增加了对来源的引用，以回应对其的指控 [2]。 1

### Page 4

### 段落 13 · Page 4

**EN**

number of URLs cited in the model’s output, providing a direct measure of ecosystem exploitation. To isolate this quantity, we remove all hallucinated citations (numbered citations provided in-text that do not have a corresponding source in the search log) and all ungrounded citations (URL citations provided that do not appear in the search logs but may link to a valid site). Our statistical model is a negative binomial hurdle model with bootstrapped confidence intervals. This allows us to quantify both when attribution gaps occur and how severe they are, while accounting for differences in query type (e.g.

**中文**

模型输出中引用的 URL 数量，提供生态系统利用的直接衡量标准。为了隔离这个数量，我们删除了所有幻觉引用（在文本中提供的编号引用，在搜索日志中没有相应的来源）和所有无根据的引用（提供的 URL 引用不会出现在搜索日志中，但可能链接到有效网站）。我们的统计模型是具有自举置信区间的负二项式障碍模型。这使我们能够量化归因差距何时发生以及其严重程度，同时考虑到查询类型的差异（例如，

### 段落 14 · Page 4

**EN**

‘Data Science’, ‘Current Affairs’, etc.). In a second regression we leverage the dataset’s head-to-head design, looking at differences between model citation behavior for the same query. Key findings: 1. Search-enabled LLM systems exploit by, surprisingly, not searching at all, relying instead on their pre-training data or simply not disclosing relevant search logs accurately. Despite the models being in search mode, 15.6% of LLM answers skipped web search entirely. This was highest for Google’s Gemini (34%), followed by OpenAI’s GPT-4o models (24%). 2. LLM search systems exploit by providing no citations (zero attribution).

**中文**

“数据科学”、“时事”等）。在第二个回归中，我们利用数据集的头对头设计，查看同一查询的模型引用行为之间的差异。主要发现： 1. 令人惊讶的是，支持搜索的 LLM 系统根本不进行搜索，而是依赖其预训练数据或根本不准确披露相关搜索日志。尽管模型处于搜索模式，但 15.6% 的 LLM 答案完全跳过了网络搜索。 Google 的 Gemini 模型的这一比例最高（34%），其次是 OpenAI 的 GPT-4o 模型（24%）。 2. LLM 检索系统通过不提供引用（零归因）来利用。

### 段落 15 · Page 4

**EN**

30% of answers provided no citations. This is driven less by query topic and more by model-specific behaviors. Gemini provided no citations for a striking 92% of queries, undermining claims that its impact on third-party traffic will be negligible. 3. Our zero-hurdle statistical model shows that, for a typical query,Google’s Gemini models and Perplexity’s Sonar models have sizable attribution gaps: at approximately 3 relevant websites visited but not cited. Perplexity exhibits much higher volume ecosystem exploitation, visiting≈10 relevant websites per query, but with a similar overall attribution gap to Gemini. 4.

**中文**

30% 的答案没有提供引用。这较少由查询主题驱动，而更多由特定于模型的行为驱动。 Gemini 没有对高达 92% 的查询提供引用，这驳斥了其对第三方流量的影响可以忽略不计的说法。 3. 我们的零障碍统计模型表明，对于一个典型的查询，Google 的 Gemini 模型和 Perplexity 的 Sonar 模型存在相当大的归因差距：大约有 3 个相关网站被访问但未被引用。 Perplexity 表现出更高的生态系统开发量，每次查询访问约 10 个相关网站，但总体归因差距与 Gemini 相似。 4.

### 段落 16 · Page 4

**EN**

The full extent of ecosystem exploitation may be underestimatedbecause models appear to selectively disclose which websites they visit, especially GPT-4o models. By design, GPT-4o models appear to have a near perfect correspondence between relevant websites drawn on and those cited, leading to a small attribution gap. 5. Refining a search-LLM’s RAG pipeline can almost double the number of citations it provides for each extra webpage it consumes. In “head-to-head” model regressions, comparing citation differences between model pairs for identical 2

**中文**

生态系统开发的全部范围可能会被低估，因为模型似乎有选择地披露它们访问的网站，尤其是 GPT-4o 模型。根据设计，GPT-4o 模型似乎在所引用的相关网站和引用的网站之间具有近乎完美的对应关系，从而导致了较小的归因差距。 5. 完善搜索法学硕士的 RAG 管道，几乎可以使其为其消耗的每个额外网页提供的引用数量增加一倍。在“头对头”模型回归中，比较相同 2 模型对之间的引用差异

### Page 5

### 段落 17 · Page 5

**EN**

queries, we find that citation efficiency – the extra citations shown per additional website visited – ranges from 0.19 to 0.45. This indicates that retrieval design (reasoning modules, search context size, and geolocation), rather than technical limits, determines AI’s relationship with the world wide web’s ecosystem. Theclassicalpoliticaleconomistsdefined exploitation asacategoryofproduction, whereby an owner-producer appropriates the difference between the cost of an input and its realized value contribution to output [28].

**中文**

通过查询，我们发现引用效率（每访问一个额外网站所显示的额外引用）范围为 0.19 到 0.45。这表明检索设计（推理模块、搜索上下文大小和GEO位置）而不是技术限制决定了人工智能与万维网生态系统的关系。古典政治经济学家将剥削定义为生产的一个类别，所有者生产者据此占用投入成本与其对产出的实现价值贡献之间的差额[28]。

### 段落 18 · Page 5

**EN**

The classical economists focused exclusively on the labor input [7, 11], but we can easily extend this framework to the data inputs consumed by LLM models during inference when producing a relevant response (the output). Policy implications. Advancing a healthy web ecosystem requires transparent search telemetry (logs, traces, and metrics). Developers, enterprise buyers, and potentially regulators should insist that LLM APIs expose a standard trace of every retrieval step and the sources ultimately cited.

**中文**

古典经济学家只关注劳动力投入 [7, 11]，但我们可以轻松地将这个框架扩展到 LLM 模型在推理过程中产生相关响应（输出）时消耗的数据输入。政策影响。推进健康的网络生态系统需要透明的搜索遥测（日志、跟踪和指标）。开发人员、企业买家和潜在的监管机构应坚持要求 LLM API 公开每个检索步骤和最终引用的来源的标准跟踪。

### 段落 19 · Page 5

**EN**

The tooling already exists to implement this: observability stacks such as LangSmith, Langfuse, Phoenix, and the GenAI semantic-conventions in OpenTelemetry can record an end-to-endsearch trace— query, retrieval, re-ranking, and citation — so long as each web document is tagged with a stable source-ID (typically a URL hash).4 Per-document relevance scores can travel in the same span [15]. If all providers adopt common definitions (e.g.llm.retrieval.ids, llm.retrieval.scores), third-parties could compare across models the exact ratio of “information consumed” to “information cited”; and equitable business models could be built on top of this.

**中文**

实现这一点的工具已经存在：LangSmith、Langfuse、Phoenix 等可观察性堆栈以及 OpenTelemetry 中的 GenAI 语义约定可以记录端到端搜索跟踪（查询、检索、重排和引用），只要每个 Web 文档都标有稳定的源 ID（通常是 URL 哈希）。4 每个文档的相关性分数可以在同一跨度内传播 [15]。如果所有提供商都采用通用定义（例如llm.retrieval.ids、llm.retrieval.scores），第三方可以跨模型比较“消耗的信息”与“引用的信息”的确切比率；在此基础上可以建立公平的商业模式。

### 段落 20 · Page 5

**EN**

Limitations. Our study does not explicitly test citation accuracy or relevance, beyond removing hallucinated and ungrounded citations [8]. Additionally, our study does not account foraccessviolations[4,22]–whethertheLLMhadpermissiontovisitspecificwebsites, which may be governed by licensing agreements. Despite these limitations, our study represents the first systematic, cross-model audit of attribution behavior in commercial search-augmented LLM systems, focusing specifically on their search tools. Our goal is to provide a structured framework for assessing attribution in empirical LLM studies [5].

**中文**

局限性。除了删除幻觉和无根据的引用之外，我们的研究并未明确测试引用的准确性或相关性[8]。此外，我们的研究没有考虑访问违规行为[4,22]——法学硕士是否有权访问特定网站，这些网站可能受许可协议管辖。尽管存在这些局限性，我们的研究代表了对商业搜索增强法学硕士系统中归因行为的首次系统性、跨模型审计，特别关注其搜索工具。我们的目标是提供一个结构化框架来评估实证法学硕士研究中的归因[5]。

### 段落 21 · Page 5

**EN**

Section 2 describes our data and variables; Section 3 details key empirical features of our data; Section 4 outlines our two regression models; Section 5 presents our core findings from the regressions; Section 6 discusses policy implications; and Section 7 concludes. Our Appendix 8 contains more detailed model results. 4See: https://opentelemetry.io/docs/specs/semconv/gen-ai/. 3

**中文**

第 2 部分描述了我们的数据和变量；第 3 节详细介绍了我们数据的关键实证特征；第 4 节概述了我们的两个回归模型；第 5 节介绍了我们回归的核心发现；第 6 节讨论政策影响；第 7 节总结。我们的附录 8 包含更详细的模型结果。 4参见：https://opentelemetry.io/docs/specs/semconv/gen-ai/。 3

### Page 6

### 段落 22 · Page 6

**EN**

2 Data and Method We conduct a large-scale empirical audit of attribution practices of commercial searchaugmented LLMs in real-world user interactions.Attribution refers to identifying the source material or input features that contributed to a model’s generated output or decisions [16]. It emphasizes relevant content “consumed” (read and used) by the LLM when answering, instead of all websites visited that may not be relevant and therefore not drawn upon. We assume the search results provided in an LLM’s search log were already determined to be relevant by the provider.

**中文**

2 数据和方法 我们对商业搜索增强法学硕士在现实世界用户交互中的归因实践进行了大规模的实证审核。归因是指识别对模型生成的输出或决策做出贡献的源材料或输入特征[16]。它强调法学硕士在回答时“消耗”（阅读和使用）的相关内容，而不是访问的所有可能不相关且因此未被利用的网站。我们假设法学硕士搜索日志中提供的搜索结果已被提供商确定为相关。

### 段落 23 · Page 6

**EN**

Other forms of exploitation, especially ones involving unauthorized access are not examined here [4, 18]. Dataset Overview. Our analysis uses LMArena’s search dataset, containing pairs of model answers to the same user query across 11 major commercial LLMs. Our final sample size (n) is 13,929 observations. We construct all variables from the raw logs rather than using the variables provided by LMArena due to various errors and inconsistencies.5 The initial dataset before filtering contains 14,000 conversations from 3,642 users, covering 7,000 queries each given to a pair of models between March (44%) and April (56%) 2025.

**中文**

其他形式的利用，特别是涉及未经授权的访问的利用，此处不予讨论 [4, 18]。数据集概述。我们的分析使用 LMArena 的搜索数据集，其中包含 11 个主要商业法学硕士对同一用户查询的模型答案对。我们的最终样本量 (n) 是 13,929 个观测值。由于存在各种错误和不一致，我们从原始日志构建所有变量，而不是使用 LMArena 提供的变量。5 过滤前的初始数据集包含来自 3,642 个用户的 14,000 个对话，涵盖 2025 年 3 月 (44%) 到 4 月 (56%) 期间针对一对模型的 7,000 个查询。

### 段落 24 · Page 6

**EN**

Each query represents a potential multi-turn conversation, including the model’s final response. Crucially, this dataset captures actual deployment behavior via application programming interface (API) calls. Model Coverage.

**中文**

每个查询代表一个潜在的多轮对话，包括模型的最终响应。至关重要的是，该数据集通过应用程序编程接口 (API) 调用捕获实际的部署行为。模型覆盖范围。

### 段落 25 · Page 6

**EN**

We analyze 11 commercial variants grouped by provider: • OpenAI: api-gpt-4o-mini-search, api-gpt-4o-search, api-gpt-4o-search-high, api-gpt-4osearch-high-loc • Perplexity: ppl-sonar-pro, ppl-sonar-reasoning, ppl-sonar, ppl-sonar-pro-high, ppl-sonarreasoning-pro-high • Google: gemini-2.0-flash-grounding, gemini-2.5-pro-grounding The model configurations are detailed further in the LMArena documentation.6 5See: https://blog.lmarena.ai/blog/2025/search-arena/. 6“For Perplexity and OpenAI, this includes setting the ‘search context size’ parameter to medium, which controls how much web content is retrieved and passed to the model.

**中文**

我们分析了按提供商分组的 11 个商业变体： • OpenAI：api-gpt-4o-mini-search、api-gpt-4o-search、api-gpt-4o-search-high、api-gpt-4osearch-high-loc • 困惑度：ppl-sonar-pro、ppl-sonar-reasoning、ppl-sonar、ppl-sonar-pro-high、ppl-sonarreasoning-pro-high • Google：gemini-2.0-flash-grounding、gemini-2.5-pro-grounding LMArena 文档中进一步详细介绍了模型配置。6 5请参阅：https://blog.lmarena.ai/blog/2025/search-arena/。 6“对于 Perplexity 和 OpenAI，这包括将‘搜索上下文大小’参数设置为中，该参数控制检索多少 Web 内容并将其传递给模型。

### 段落 26 · Page 6

**EN**

We also explore specific features by changing the default settings: (1) For OpenAI, we test their geolocation feature in one model variant by passing a country code extracted from the user’s IP address. (2) For Perplexity and OpenAI, we include variants with ‘search context size’ set to high. ” Gemini model defaults to Google Search Tool enabled. See: https://blog.lmarena.ai/blog/2025/search-arena/. Accessed: 16 June, 2025. 4

**中文**

我们还通过更改默认设置来探索特定功能：（1）对于 OpenAI，我们通过传递从用户 IP 地址提取的国家/地区代码，在一种模型变体中测试其GEO位置功能。 (2) 对于 Perplexity 和 OpenAI，我们包含“搜索上下文大小”设置为高的变体。 Gemini 模型默认启用 Google 搜索工具。请参阅：https://blog.lmarena.ai/blog/2025/search-arena/。访问日期：2025 年 6 月 16 日。 4

### Page 7

### 段落 27 · Page 7

**EN**

2.1 Key Variables and Measurement We do not rely on LMArena’s citation variable construction, which we found didn’t adequately distinguish between search logs and citations for our use case. We instead reconstruct them from scratch using the model logs in their dataset. Ecosystem Exploitation (Attribution Gap). Our primary dependent variable measures the difference between unique relevant pages visited by the LLM during search and unique pages actually cited to the user in the API response. This captures the extent to which a model consumes relevant web content without providing appropriate attribution. Citations.

**中文**

2.1 关键变量和测量我们不依赖LMArena的引文变量构造，我们发现它没有充分区分我们用例的搜索日志和引文。相反，我们使用数据集中的模型日志从头开始重建它们。生态系统开发（归因差距）。我们的主要因变量衡量的是法学硕士在搜索期间访问的唯一相关页面与 API 响应中实际向用户引用的唯一页面之间的差异。这捕获了模型在不提供适当归因的情况下消耗相关网络内容的程度。引文。

### 段落 28 · Page 7

**EN**

We define citations as any in-text URL reference that is grounded in the model’s search results log, including both explicit URLs and numbered references that link to specific sources. We exclude “hallucinated citations” (numbered citations, such as[13], that link to an empty source) and “ungrounded citations” (citation of URLs that exist but are not in the search log). Unique URLs (websites) for citations or attribution are those seen by the model that do not link to the same web page when stripped of parameters (e.g., example.com/?tracking_id=23222 is turned into example.com).

**中文**

我们将引文定义为基于模型搜索结果日志的任何文本内 URL 引用，包括显式 URL 和链接到特定来源的编号引用。我们排除“幻觉引用”（链接到空源的编号引用，例如[13]）和“无根据的引用”（存在但不在搜索日志中的 URL 的引用）。用于引用或归因的唯一 URL（网站）是模型看到的那些在剥离参数时不会链接到同一网页的 URL（例如，example.com/?tracking_id=23222 变成 example.com）。

### 段落 29 · Page 7

**EN**

This amounts to transforming URLs into their base URL and then checking for duplicates. Relevant Sites Visited (Consumed). We define relevant sites visited by the LLM as those listed in their search log, regardless of whether they were cited in-text or not. We treat every URL that appears in the search log as relevant, on the understanding that the provider has already filtered out non-relevant visits. Note, however, that this log may itself be incomplete: some vendors — OpenAI, in particular — seem to pre-trim their traces, returning only a subset of the relevant pages the model actually visited. Conversation Classification.

**中文**

这相当于将 URL 转换为其基本 URL，然后检查重复项。访问（消耗）的相关站点。我们将法学硕士访问的相关网站定义为其搜索日志中列出的网站，无论它们是否在文本中被引用。我们将搜索日志中出现的每个 URL 视为相关，但前提是提供商已过滤掉不相关的访问。但请注意，此日志本身可能不完整：一些供应商（尤其是 OpenAI）似乎预先修剪了他们的痕迹，仅返回模型实际访问的相关页面的子集。会话分类。

### 段落 30 · Page 7

**EN**

We categorize all conversations into 12 topic areas using o4-mini with high reasoning to enable analysis of topic-specific attribution patterns. This classification covers areas from technical queries (software engineering, data science) to consumer-oriented topics (shopping, health, finance). We provided the 12 categories to GPT, drawing on an unsupervised visualization of clusters in the query data on Nomic Atlas.7 Data Cleaning. After removing conversations with classification failures or misaligned search traces, our final sample contains 13,929 observations, all successfully classified and with clean attribution data.

**中文**

我们使用具有高推理能力的 o4-mini 将所有对话分为 12 个主题区域，以便能够分析特定主题的归因模式。此分类涵盖从技术查询（软件工程、数据科学）到面向消费者的主题（购物、健康、金融）的领域。我们利用 Nomic Atlas.7 数据清理中查询数据中集群的无监督可视化，向 GPT 提供了 12 个类别。在删除分类失败或未对齐的搜索跟踪的对话后，我们的最终样本包含 13,929 个观察结果，所有观察结果均已成功分类并具有干净的归因数据。

### 段落 31 · Page 7

**EN**

Pre-filtering of Logs. Most models appear to filter their logs for relevant websites visited only – rather than all sites visited. But OpenAI appears to filter them more strictly. Hallucinated citations (numbered citations provided in-text that do not exist in the search 7See Nomic Atlas: https://atlas.nomic.ai/data/srulyrosenblat/ ai-model-search-comparison-dataset/map/2da8af3f-c160-4008-928d-8df37c27b947#x7Nh . 5

**中文**

日志预过滤。大多数模型似乎只过滤访问过的相关网站的日志，而不是访问过的所有网站。但 OpenAI 似乎对它们的过滤更加严格。幻觉引文（搜索中不存在的文本中提供的编号引文7参见Nomic Atlas：https://atlas.nomic.ai/data/srulyrosenblat/ai-model-search-comparison-dataset/map/2da8af3f-c160-4008-928d-8df37c27b947#x7Nh。5

### Page 8

### 段落 32 · Page 8

**EN**

log) appear for Gemini and to a lesser extent Sonar.8 Moreover, in terms ofcitations provided that do not appear in the search logs(ungrounded citations): 7% of citations by GPT-4o models were not found in its search logs, indicating either an overly restrictive pre-filtering of the search logs or simply the model citing from pre-trained knowledge. 3 Descriptive Patterns Our data show stark differences in attribution practices across model families, highlighting that design choices, rather than technological limitations, drive model behavior. The Attribution Crisis.

**中文**

日志）出现在 Gemini 中，声纳中也出现了较小的情况。 8 此外，就未出现在搜索日志中的引用而言（无根据的引用）：GPT-4o 模型的 7% 的引用在其搜索日志中未找到，这表明要么对搜索日志进行了过度限制性的预过滤，要么只是模型引用了预先训练的知识。 3 描述性模式 我们的数据显示了不同模型系列之间归因实践的显着差异，强调了驱动模型行为的是设计选择，而不是技术限制。归因危机。

### 段落 33 · Page 8

**EN**

15.6% of LLM responses involved no website visits despite being in search mode, yet 30% provided no citations whatsoever – a substantial gap between content consumption and content recognition. This pattern varies dramatically by provider. 39% of responses show perfect attribution alignment (zero gap), while 61% exhibit some degree of ecosystem exploitation. For Gemini, a “zero” gap still tends to signals exploitation though, because the model usually answers without visiting any external site even when its Google-Search tool is enabled (Table 1). Provider-Specific Patterns.

**中文**

15.6% 的法学硕士回复尽管处于搜索模式，但并未涉及任何网站访问，但 30% 的回复没有提供任何引用——内容消费和内容识别之间存在巨大差距。这种模式因提供商而异。 39% 的回复显示出完美的归因一致性（零差距），而 61% 的回复显示出一定程度的生态系统利用。对于 Gemini 来说，“零”差距仍然意味着剥削，因为即使启用了 Google 搜索工具，该模型通常也无需访问任何外部网站即可做出回答（表 1）。特定于提供者的模式。

### 段落 34 · Page 8

**EN**

Table 1 illustrates three distinct patterns of exploitation: (1) Not visiting relevant sitesat all, according to the model’s logs, when answering a question (exploitation through pre-training reliance) – 24% of GPT search answers and 34% of Gemini models; (2) Not providingany citationsat all – 25% of GPT-4o answers and 92% of Gemini answers; and (3) Having alarge relative gapbetween sites visited and sites cited – as in Perplexity’s Sonar. T able 1.

**中文**

表 1 说明了三种不同的利用模式：(1) 根据模型的日志，在回答问题时根本不访问相关网站（通过预训练依赖进行利用）——GPT 搜索答案的 24% 和 Gemini 模型的 34%； (2) 根本不提供任何引用——25% 的 GPT-4o 答案和 92% 的 Gemini 答案； (3) 访问的站点和引用的站点之间存在较大的相对差距——如 Perplexity 的声纳。表 1.

### 段落 35 · Page 8

**EN**

Attribution Statistics by Model Family GPT-4o Gemini Sonar Median Gap 0.0 4.0 5.0 Median Citations 2.0 0.0 5.0 Median Sites Visited 2.0 4.0 10.0 Zero Citations 1,309 2,198 663 Zero Site Visits 1,242 817 120 Sample Size (n) 5,272 2,394 6,263 Note: ‘Gap’ refers to the attribution gap = relevant websites visited (content consumed) minus unique websites cited. 8They are by definition zero for GPT-4o models since OpenAI’s models do not use numbers in square brackets for its citations which is what we track for this metric. 6

**中文**

按模型系列划分的归因统计 GPT-4o Gemini 声纳差距中位数 0.0 4.0 5.0 引用次数中位数 2.0 0.0 5.0 访问站点中位数 2.0 4.0 10.0 零引用 1,309 2,198 663 零站点访问 1,242 817 120 样本量 (n) 5,272 2,394 6,263 注：“差距”是指归因差距=访问的相关网站（消耗的内容）减去引用的唯一网站。 8 根据定义，GPT-4o 模型的引用为零，因为 OpenAI 的模型不使用方括号中的数字来表示其引用，而这正是我们跟踪该指标的原因。 6

### Page 9

### 段落 36 · Page 9

**EN**

• GPT-4o – Limited disclosure of sites visited: On paper it shows almost perfect alignment between relevant pages searched according to its logs and pages cited. But this is likely an artifact of aggressive log-filtering. The model seems to disclose only those URLs it ultimately cites, omitting any additional relevant pages it read (consumed). Support for this view comes from its high share ofungrounded citations — links that appear in the answer but not in the trace — suggesting that many visits are simply withheld from the log.

**中文**

• GPT-4o – 访问站点的有限披露：在纸面上，它显示了根据其日志搜索的相关页面与引用的页面之间几乎完美的一致性。但这可能是积极的日志过滤的产物。该模型似乎只公开了它最终引用的那些 URL，省略了它读取（使用）的任何其他相关页面。对这一观点的支持来自于其大量无根据的引用——出现在答案中但不在跟踪中的链接——表明许多访问只是从日志中被保留。

### 段落 37 · Page 9

**EN**

• Gemini – No citations provided: Systematic attribution failure with 92% zerocitation responses despite some relevant website searches. • Sonar – High-volume, low-credit: Extensive crawling (10 median sites) with large attribution gaps (5.0 median) despite providing more citations than Gemini or OpenAI. Topic-Specific Vulnerabilities.

**中文**

• Gemini – 未提供引用：尽管进行了一些相关网站搜索，但系统归因失败，92% 的引用为零。 • Sonar – 高容量、低信用度：广泛的爬行（中位数为 10 个站点），但归因差距较大（中位数为 5.0），尽管提供的引用比 Gemini 或 OpenAI 更多。特定主题的漏洞。

### 段落 38 · Page 9

**EN**

Attribution failures concentrate in economically and legally sensitive domains, including: • Software engineering: 33% zero-citation rate (700 queries), especially for Gemini • Games/Creative writing: 40% zero-citation rate (494 queries) • Education: 43.6% zero-citation rate (228 queries) • Health information: For Mental & Physical Health and Relationships, systematic gaps for Gemini (94%) and GPT (26%) 4 Regression Models 4.1 Hurdle-Model Specification The dependent variable Yi (i = 1,...,n ) is the attribution gap: the number of relevant websites a model visits but fails to cite, for queryi, where i runs from 1 to n = 13, 929.

**中文**

归因失败集中在经济和法律敏感领域，包括： • 软件工程：33% 零引用率（700 条查询），尤其是 Gemini • 游戏/创意写作：40% 零引用率（494 条查询） • 教育：43.6% 零引用率（228 条查询） • 健康信息：对于身心健康和关系，Gemini (94%) 和 GPT (26%) 的系统性差距 4 回归模型 4.1 障碍模型规范 因变量 Yi (i = 1,...,n ) 是归因差距：模型访问但未引用的相关网站的数量，对于查询 i，其中 i 从 1 运行到 n = 13, 929。

### 段落 39 · Page 9

**EN**

Because most answers are perfectly attributed (Yi = 0) while the rest show a skewed count distribution, we use a hurdle model. It breaks up E[Attribution Gap ] = P (Gap > 0) ×E[Gap|Gap> 0] into two sequential components: (a) Hurdle stage: What is the probability that the gap is exactly zero→P (Gap> 0)? This is a Bernoulli outcome with probabilityπi. 7

**中文**

由于大多数答案都是完美归因的 (Yi = 0)，而其余答案则显示出偏斜的计数分布，因此我们使用障碍模型。它将 E[归因差距] = P (Gap > 0) ×E[Gap|Gap> 0] 分解为两个连续分量： (a) 跨栏阶段：差距恰好为零→P (Gap> 0) 的概率是多少？这是概率为 πi 的伯努利结果。 7

### Page 10

### 段落 40 · Page 10

**EN**

(b) Count stage:Ifanattributiongapexists( Yi > 0), howlargeisthegap: E[Gap|Gap> 0]? We model positive counts with azero-truncatednegative binomial distribution, which has mean λi and over-dispersion parameterα.9 Putting the two parts together gives the probability mass function: Pr(Yi =y|xi) =    πi, y = 0, (1−πi) fnb ( y;λi,α ) 1−fnb ( 0;λi,α ), y ≥1, (1) where: fnb ( y;λ,α ) = Γ ( y +α−1 ) Γ(α−1)y! (αλ)y ( 1 +αλ )− ( y+α−1 ) , α> 0.

**中文**

(b) 计数阶段：Ifanaattributiongapexists( Yi > 0)，thegap 有多大：E[Gap|Gap> 0]？我们用零截断负二项式分布对正计数进行建模，该分布具有均值 λi 和过度离散参数 α。9 将这两部分放在一起给出概率质量函数： Pr(Yi =y|xi) =    πi, y = 0, (1−πi) fnb ( y;λi,α ) 1−fnb ( 0;λi,α ), y ≥1, (1) 其中： fnb ( y;λ,α ) = Г ( y +α−1 ) Г(α−1)y! (αλ)y ( 1 +αλ )− ( y+α−1 )，α>0。

### 段落 41 · Page 10

**EN**

(2) fnb(y;λ,α) is the mean-parameterized negative binomial probability mass function, Linear predictors.Each of the two regression stages has its own regression equation with predictors, consisting of: model family, the query category or ‘classification’ (e.g. ‘Data Science’), the log of LLM output character count, and the number of unique search results.

**中文**

(2) fnb(y;λ,α) 是均值参数化负二项式概率质量函数，线性预测变量。两个回归阶段中的每一个都有其自己的带有预测变量的回归方程，包括：模型族、查询类别或“分类”（例如“数据科学”）、LLM 输出字符计数的日志以及唯一搜索结果的数量。

### 段落 42 · Page 10

**EN**

This leads to the following two equations:10 logit(πi) =γ0 +γ⊤ fam 1{model_familyi}+γ⊤ cls 1{classificationi}+γℓlog ( response_character_counti ) , (3) logλi =β0 +β⊤ fam 1{model_familyi}+β⊤ cls 1{classificationi} +βsrunique_search_results_counti +βℓlog ( response_character_counti ) + ( 1{model_familyi}⊗1{classificationi} )⊤ βfam×cls + ( 1{model_familyi}⊗unique_search_results_counti )⊤ βfam×sr (4) Equation 3 is the logit probability, whereexp(γfam) represents the odds-ratios for producing any attribution gap by model family,exp(γcls) represents the odds-ratios by classification topic, and exp(γℓ) is the odds-ratio for answer length.

**中文**

这导致以下两个方程：10 logit(πi) =γ0 +γ⊤ fam 1{model_familyi}+γ⊤ cls 1{classificationi}+γℓlog (response_character_counti ) , (3) logλi =β0 +β⊤ fam 1{model_familyi}+β⊤ cls 1{classificationi} +βsrunique_search_results_counti +βℓlog (response_character_counti ) + ( 1{model_familyi}⊗1{classificationi} )⊤ βfam×cls + ( 1{model_familyi}⊗unique_search_results_counti )⊤ βfam×sr (4) 公式 3 是 logit 概率，其中exp(γfam)表示按模型系列产生任何归因差距的优势比，exp(γcls)表示按分类主题划分的优势比，exp(γℓ)是答案长度的优势比。

### 段落 43 · Page 10

**EN**

The equation contains only main effects (no interactions): the odds ofany gap depend separately on model family, topic, and 9If α→0 the model would reduce to a Poisson hurdle. 10Number of ‘turns’ had poor predictive power in our model, wrong sign in count component, despite some correlation to attribution gap for GPT models and especially for Perplexity models. 8

**中文**

该方程仅包含主效应（无交互作用）：任何差距的几率分别取决于模型系列、主题和 9如果 α→0，模型将减少到泊松障碍。 10 尽管与 GPT 模型（尤其是 Perplexity 模型）的归因差距存在一定相关性，但我们的模型中“转弯数”的预测能力很差，计数组件中的符号错误。 8

### Page 11

### 段落 44 · Page 11

**EN**

answer length.11 Equation 4 is the negative binomial count component wherebyexp(βfam) represents the multiplicative changes in the expected number of uncited website visits by model family, given that a gap exists. exp(βcls) represents the effects by classification topic, andexp(βsr) is the multiplicative effect of additional search results. A value of 1.30 implies a 30% larger gap, for example. Equation 4 adds interaction termsβfam×cls, so the effect of a model family can differ by query topic once a gap exists, andβfam×sr, to account for the varying impact of searching (number of URLs) on the attribution gap by model family.

**中文**

答案长度。11 方程 4 是负二项式计数分量，其中 exp(βfam) 表示假设存在差距，模型系列未引用网站访问量的预期数量的乘法变化。 exp(βcls)表示分类主题的效果，exp(βsr)是附加搜索结果的乘法效果。例如，值 1.30 意味着差距增大 30%。公式 4 添加了交互项 βfam×cls，因此一旦存在差距，模型系列的效果可能会因查询主题而异，并且加入 βfam×sr，以解释搜索（URL 数量）对模型系列归因差距的不同影响。

### 段落 45 · Page 11

**EN**

4.2 Head-to-Head Model Comparison Regression To isolate the number of URLseach LLM cites from one additional website search visit, while controlling for question types, we run a second additional regression model. This exploits the LMArena head-to-head design, whereby every question is answered by exactly two model systems. This means that any unobservable query-specific factors driving citation behavior cancel out. This design also ensures thatβ1m is not biased by systematically “easy” or “hard” opponents.

**中文**

4.2 头对头模型比较回归 为了从一次额外的网站搜索访问中分离出 URLseach LLM 引用的数量，同时控制问题类型，我们运行了第二个额外的回归模型。这利用了 LMArena 的头对头设计，每个问题都由两个模型系统来回答。这意味着任何不可观察的特定于查询的驱动引用行为的因素都会被抵消。这种设计还确保β1m不会因系统性“容易”或“困难”的对手而产生偏见。

### 段落 46 · Page 11

**EN**

We collapse each model pair that answers the same query into a single observation (focal model−opponent) and run a separate OLS regression for every focal model m, wherei now runs from1 to n = 6, 951, andm contains 11 focal models. dim =β0m +β1m ∆sim +β2m ∆ℓim + ∑ k γ(m) k Dik + ∑ j δ(m) j Oij +εim, (6) In Equation 6, dim denotes the citation-gap advantage – the difference in unique citations produced by the focal model compared to its ‘opponent’, citationsm−citationsopp.

**中文**

我们将回答相同查询的每个模型对折叠为单个观察（焦点模型-对手），并为每个焦点模型 m 运行单独的 OLS 回归，其中 i 现在从 1 运行到 n = 6, 951，并且 m 包含 11 个焦点模型。 dim =β0m +β1m Δsim +β2m Δℓim + Σ k γ(m) k Dik + Σ j δ(m) j Oij +εim, (6) 在等式 6 中，dim 表示引文差距优势——焦点模型与其“对手” itationsm−itationsopp 相比产生的唯一引文差异。

### 段落 47 · Page 11

**EN**

The term ∆sim captures the search retrieval difference, defined as the gap in unique URLs visited by the two systems in its logs, while∆ℓim measures the length difference in characters between their answers. The vectorDik comprises topic dummies controlling for the classification of questioni (reference category: “Current affairs & factual”), andOij contains dummies identifying which rival model the focal system faces (baseline = the first alphabetic opponent).12 11For example, exp(γℓ) = 1.4 means a one-unit increase in log(response length) multiplies the odds of a gap by 1.4. 12Coefficient interpretation is as follows.

**中文**

术语 Δsim 捕获搜索检索差异，定义为两个系统在其日志中访问的唯一 URL 之间的差距，而 Δℓim 衡量其答案之间的字符长度差异。 VectorDik 包含控制问题分类的主题虚拟对象（参考类别：“时事与事实”），Oij 包含识别焦点系统面临哪个竞争对手模型的虚拟对象（基线 = 第一个字母对手）。12 11例如，exp(γℓ) = 1.4 意味着 log（响应长度）增加一个单位将差距的几率乘以 1.4。 12系数解释如下。

### 段落 48 · Page 11

**EN**

The slopeβ1m measures citation efficiency: it is the expected additional citations that modelm produces per additional URL it opens, conditional on topic, verbosity, and opponent. Thus β1m = 0.40 implies that ten extra retrievals yield roughly four extra citations. The coefficient β2m captures the effect of answer length (characters) net of retrieval; a significant value would indicate that verbosity itself explains some of the citation edge. Topic dummies enter throughγ(m) k ; positive values mean modelm out-cites its rival in domaink, whereas negative values signal a systematic shortfall.

**中文**

斜率β1m 衡量引用效率：它是 modelm 每打开一个额外的 URL 所产生的预期额外引用，以主题、详细程度和对手为条件。因此 β1m = 0.40 意味着 10 次额外检索大约会产生 4 次额外引用。系数 β2m 反映了答案长度（字符）对检索的影响；显着的值表明冗长本身可以解释一些引文边缘。主题虚拟人通过γ(m) k 进入；正值意味着 modelm 在领域中引用了其竞争对手，而负值则表示系统性不足。

### 段落 49 · Page 11

**EN**

Opponent-specific effects are absorbed byδ(m) j , showing how the citation gap changes whenm faces rivalj 9

**中文**

对手特定效应被 δ(m) j 吸收，显示当 m 面对对手 j 时引文差距如何变化 9

### Page 12

### 段落 50 · Page 12

**EN**

Each model’sβ1m is our key quantity of interest and summarizes modelm’s retrieval-tocitation efficiency or yield:the impact of a marginal website visit on citations. 5 Regression Findings 5.1 Attribution Gap Regression Model The regression results, transformed into probabilities, show notable differences in attribution reliabilityacrossAImodelfamilies(Table2andFigure1). 13 The‘expectedattributiongap’is the total prediction from our model:E[Attribution Gap] =P (Gap> 0)×E[Gap|Gap> 0]; whereas the first row (‘Probability of a Gap’) is only the first term of this equation, P (Gap> 0). T able 2.

**中文**

每个模型的 β1m 是我们感兴趣的关键量，它总结了模型的检索引用效率或产量：边缘网站访问对引用的影响。 5 回归结果 5.1 归因差距回归模型 转化为概率的回归结果显示，AI 模型系列之间的归因可靠性存在显着差异（表 2 和图 1）。 13 “预期归因差距”是我们模型的总预测：E[归因差距] =P (Gap> 0)×E[Gap|Gap> 0]；而第一行（“间隙概率”）只是该方程的第一项，P（间隙> 0）。表 2.

### 段落 51 · Page 12

**EN**

Expected Total Attribution Gap by Model Family GPT Gemini Sonar Probability of a Gap (%) 10.5 70.3 99.3 Expected Attribution Gap (Total) 0.18 3.04 3.12 95% Confidence Interval [0.15, 0.23] [2.80, 3.28] [2.99, 3.25] Standard Error (SE) 0.02 0.12 0.06 Note: Results from negative binomial hurdle model for Current Affairs & Factual Information queries with median characteristics (5 search results, 2,089 characters, per query), with bootstrapped mean. Confidence intervals from parametric bootstrap (n=1,000) for total expected attribution gap.

**中文**

按模型系列划分的预期总归因差距 GPT Gemini 声纳 差距概率 (%) 10.5 70.3 99.3 预期归因差距（总计） 0.18 3.04 3.12 95% 置信区间 [0.15, 0.23] [2.80, 3.28] [2.99, 3.25] 标准误差(SE) 0.02 0.12 0.06 注意：具有中值特征的时事和事实信息查询的负二项式障碍模型的结果（5 个搜索结果，每个查询 2,089 个字符），具有引导平均值。总预期归因差距的参数引导 (n=1,000) 的置信区间。

### 段落 52 · Page 12

**EN**

Attribution gap is the missing web page (URL) citations per search query relative to relevant websites consumed, measured as a web page gap. This pattern holds consistently across all topic classifications (see Appendix, Table 5). The GPT-4o models appear to show less exploitative attribution behavior but this is most likely due to them being more circumspect in their disclosures by not showing the full extent of their logs.14 OpenAI’s models have only a 10.5% probability of having any citation gaps and an expected 0.18 missing citations (relative to relevant websites consumed) per query (Table 2).

**中文**

归因差距是指每个搜索查询相对于所使用的相关网站缺失的网页 (URL) 引用，以网页差距来衡量。这种模式在所有主题分类中都一致（参见附录，表 5）。 GPT-4o 模型似乎表现出较少的剥削性归因行为，但这很可能是因为它们在披露时更加谨慎，没有显示日志的完整范围。 14 OpenAI 的模型只有 10.5% 的概率出现任何引用差距，并且每个查询的预期缺失引用数为 0.18（相对于消耗的相关网站）（表 2）。

### 段落 53 · Page 12

**EN**

Sonar exhibits citation gaps in 99.3% of queries with 3.12 expected missing instead of the baseline opponent. Finally,β0m gives the baseline citation advantage when the question falls in the reference topic, the opponent is the baseline rival, and retrieval/length differences are zero. 13The hurdle model produces raw odds-ratios that compare each model family to the reference category (Gemini). However, for policy interpretation, we need actual probabilities and expected values.

**中文**

Sonar 在 99.3% 的查询中表现出引用差距，预期缺失 3.12 个，而不是基线对手。最后，β0m 给出了当问题落在参考主题内、对手是基线竞争对手且检索/长度差异为零时的基线引用优势。 13跨栏模型产生原始优势比，将每个模型系列与参考类别（双子座）进行比较。然而，对于政策解释，我们需要实际概率和期望值。

### 段落 54 · Page 12

**EN**

To obtain these, we used the fitted model to make predictions for a standardized query: covering Current Affairs & Factual Information topic classification with median characteristics (5 search results visited, 2,089 character responses). The model’s ‘hurdle’ component estimates the probability of having any attribution gap (missing citations & licensing), while the count component estimates the expected gap size when gaps occur. Multiplying these components gives us the unconditional expectation – the average number of missing citations per query for each model family.

**中文**

为了获得这些，我们使用拟合模型对标准化查询进行预测：涵盖具有中值特征的时事和事实信息主题分类（访问了 5 个搜索结果，2,089 个字符响应）。该模型的“障碍”组件估计出现任何归因差距（缺少引用和许可）的概率，而计数组件则估计出现差距时的预期差距大小。将这些分量相乘得到了无条件期望——每个模型系列每次查询的平均缺失引用数。

### 段落 55 · Page 12

**EN**

14Using OpenAI search in the user interface (UI) shows far more website visits from limited testing. 10

**中文**

14在用户界面 (UI) 中使用 OpenAI 搜索显示，有限测试的网站访问量要多得多。 10

### Page 13

### 段落 56 · Page 13

**EN**

citations per query in total. Gemini falls somewhere between these extremes with citation gaps in 70.3% of queries and 3.04 expected missing citations in total per query. Sonar’s near-universal citation gap (99.3% of queries) makes it particularly concerning for applications requiring source transparency. Gemini is arguably relying too heavily on internal knowledge given that a large portion of its zero attribution gap is due to it having zero (disclosed) website searches, at 34% of queries. Figure 1.

**中文**

每个查询的总引用次数。 Gemini 介于这两个极端之间，70.3% 的查询存在引用差距，每个查询总共有 3.04 个预期缺失引用。 Sonar 几乎普遍存在的引用差距（99.3% 的查询）使其对于需要源透明度的应用程序尤其令人担忧。 Gemini 可以说过于依赖内部知识，因为其零归因差距的很大一部分是由于其网站搜索量为零（已公开），占查询量的 34%。图 1.

### 段落 57 · Page 13

**EN**

Expected Attribution Gaps, Predicted (by Model Family) 0.19 3.12 3.04 0.0 0.5 1.0 1.5 2.0 2.5 3.0 3.5 4.0 GPT Sonar Gemini AI Model Family E [Gap] Note: Predicted values for number of citations missing relative to web pages consumed. Based on negative binomial hurdle model regression coefficients. Bars show the model’s expected citation gap (websites visited in the logs minus websites cited in the output), estimated at the median conversation length and median website visits, without interaction effects included. Showing 95% confidence intervals calculated with theemmeans package in R.

**中文**

预期归因差距（按模型系列） 0.19 3.12 3.04 0.0 0.5 1.0 1.5 2.0 2.5 3.0 3.5 4.0 GPT Sonar Gemini AI 模型系列 E [差距] 注：相对于所使用网页的引用缺失数量的预测值。基于负二项式障碍模型回归系数。条形图显示模型的预期引用差距（日志中访问的网站减去输出中引用的网站），根据中位会话长度和中位网站访问量进行估计，不包括交互效应。显示使用 R 中的 emmeans 包计算的 95% 置信区间。

### 段落 58 · Page 13

**EN**

Lastly, in terms of other factors drivinghow largethe gap is once it appears (the count component), we can look at the incidence-rate ratio (IRR).15 Longer answers actuallyshrink the gap size: When logged response character count doubles (from e.g., 100 to 200 charac- 15In count-data models (Poisson, negative binomial, zero-inflated, hurdle, etc.) the regression is fitted on a log scale. Exponentiating a coefficient converts it to an incidence-rate ratio (IRR). The IRR tells you the multiplicative change in the expected count when the predictor increases by one unit, holding everything else constant. 11

**中文**

最后，就驱动差距出现后的大小（计数部分）的其他因素而言，我们可以查看发生率比 (IRR)。 15 较长的答案实际上缩小了差距大小：当记录的响应字符计数加倍时（例如，从 100 到 200 个字符） 15 在计数数据模型（泊松、负二项式、零膨胀、跨栏等）中，回归以对数尺度拟合。对系数求幂可将其转换为发生率比 (IRR)。IRR 告诉您当预测变量增加一个单位时，在其他条件保持不变的情况下，预期计数的乘法变化。

### Page 14

### 段落 59 · Page 14

**EN**

ters), the expected number of missing citations decreases by about 11% (IRR 0.89 or so). Reading more web pages from search inflates the gap: every extra page the LLM system reads raises the expected uncited count by 13% (IRR≈1.13). 5.2 Head-to-Head Model Results: Citation efficiency In this section, we focus onβ1m coefficient from our head-to-head regressions (Equation 6). Thiscoefficienttellsushowmanymorecitationsthefocalmodelgeneratesforeachadditional search result compared to its opponent. A smaller coefficient signals poorer performance: the focalmodelconvertseachextrarelevantpageitopensintofewercitationsthanitscomparator does.

**中文**

ter），预期缺失引用数减少约 11%（IRR 0.89 左右）。从搜索中读取更多网页会扩大差距：LLM 系统每读取一个额外的页面，就会使预期未引用计数增加 13% (IRR≈1.13)。 5.2 头对头模型结果：引用效率 在本节中，我们重点关注来自头对头回归的 β1m 系数（公式 6）。该系数告诉我们与对手相比，焦点模型为每个额外的搜索结果生成更多的引用。较小的系数表示性能较差：焦点模型将每个额外的相关页面转换为比其比较器更少的引文。

### 段落 60 · Page 14

**EN**

For example, if Sonar’s coefficient is 0.4, this means that when it undertakes five additional relevant web page visits than GPT-4o on a question it is expected to have5×0.4 = 2 more citations than GPT-4o. 264 coefficients are estimated in total, running a separate regression for each of the 11 models (24 parameters estimated for each model).16 We plotβ1m in Figure 2 below (Appendix Table 6).

**中文**

例如，如果 Sonar 的系数为 0.4，这意味着当它在某个问题上比 GPT-4o 多进行 5 次相关网页访问时，预计会比 GPT-4o 多 5×0.4 = 2 次引用。总共估计了 264 个系数，为 11 个模型中的每一个模型运行单独的回归（每个模型估计了 24 个参数）。16 我们在下面的图 2 中绘制了 β1m（附录表 6）。

### 段落 61 · Page 14

**EN**

Almost all coefficients from the regression are positive and highly significant.17 Figure 2 below shows that best-in-class variants (Sonar-reasoning-pro-high, Gemini-flashgrounding, GPT-4o-search-high-loc) yield∼0.43 citations per extra URL; whereas baseline variants (ppl-sonar-pro-high) return only∼0.19. This implies that the best model converts every extra retrieved URL into≈0.45 additional citations (compared to its competitor models), whereas the weakest model variant converts that same extra URL into≈0.19 citations.

**中文**

几乎所有回归系数都是正值且高度显着。17 下面的图 2 显示，同类最佳变体（Sonar-reasoning-pro-high、Gemini-flashgrounding、GPT-4o-search-high-loc）每个额外 URL 产生约 0.43 次引用；而基线变体（ppl-sonar-pro-high）仅返回∼0.19。这意味着最好的模型将每个额外检索到的 URL 转换为约 0.45 个额外引用（与其竞争对手模型相比），而最弱的模型变体将相同的额外 URL 转换为约 0.19 个引用。

### 段落 62 · Page 14

**EN**

The span is therefore about0.45−0.19≈0.26 citations per URL, showing that RAG implementation choices can more than double the payoff from each additional page the model visits. This illustrates just how wide the performance window is, and thus how much room developers (or regulators) have to raise low performers up to the current best practice. 161×Intercept; 11×topic dummies (classifications), 1×focal-search-diff (number of web pages), 10× opponent-model dummies, 1×focal-length-diff.

**中文**

因此，每个 URL 的跨度约为 0.45−0.19≈0.26 次引用，这表明 RAG 实现选择可以使模型访问的每个附加页面的收益增加一倍以上。这说明了性能窗口有多宽，以及开发人员（或监管机构）必须将低性能者提升到当前最佳实践的空间有多大。 161×拦截； 11×主题虚拟模型（分类），1×焦点搜索差异（网页数量），10×对手模型虚拟模型，1×焦距差异。

### 段落 63 · Page 14

**EN**

17Among the 264 coefficients estimated,focal_search_diff is significant (and positive) for every model – extra retrieval still translates into more citations, although the payoff varies. Answer length matters (positive) for the GPT-mini, GPT-search, Sonar-pro, Sonar, and Sonar-reasoning families, but not for the “high” search variants or Gemini models. One notable exception:ppl-sonar-reasoning-pro-high shows a significant negative length effect (−1.35×10−4, p = 6.75×10−3), suggesting longer answers actually hurt citation performance for this model. Topic effects are sparse and model-specific.

**中文**

17在估计的 264 个系数中，focal_search_diff 对于每个模型都很重要（并且是正数）——额外的检索仍然会转化为更多的引用，尽管回报各不相同。对于 GPT-mini、GPT-search、Sonar-pro、Sonar 和 Sonar-reasoning 系列，答案长度很重要（正），但对于“高”搜索变体或 Gemini 模型则不然。一个值得注意的例外：ppl-sonar-reasoning-pro-high 显示出显着的负长度效应（−1.35×10−4，p = 6.75×10−3），这表明较长的答案实际上会损害该模型的引用性能。主题效果稀疏且特定于模型。

### 段落 64 · Page 14

**EN**

Mental & Physical Health lowers citation edge for GPT-4o variants but raises it for basic Sonar-pro. Finance boosts citation edge for Sonar-pro-high but suppresses it for Sonar-reasoning and Gemini-2.5. Opponent dummies are often significant and large. 12

**中文**

心理和身体健康降低了 GPT-4o 变体的引用优势，但提高了基本 Sonar-pro 的引用优势。金融提高了 Sonar-pro-high 的引用优势，但抑制了 Sonar-reasoning 和 Gemini-2.5 的引用优势。对手假人通常又大又重要。 12

### Page 15

### 段落 65 · Page 15

**EN**

Figure 2. Focal Model: Citation difference per extra URL visited 0.45 0.44 0.43 0.43 0.39 0.34 0.31 0.26 0.25 0.2 0.19ppl−sonar−pro−high ppl−sonar−pro api−gpt−4o−mini−search api−gpt−4o−search gemini−2.5−pro−grounding ppl−sonar api−gpt−4o−search−high api−gpt−4o−search−high−loc gemini−2.0−flash−grounding ppl−sonar−reasoning ppl−sonar−reasoning−pro−high 0.0 0.1 0.2 0.3 0.4 β^ 1m (citations per extra URL) Gemini GPT Sonar Note: Extra citations gained for each additional URL the focal model opens (differences between models). This holds match-up effects constant, isolating technology effects.

**中文**

图 2. 焦点模型：每个额外访问的 URL 的引文差异 0.45 0.44 0.43 0.43 0.39 0.34 0.31 0.26 0.25 0.2 0.19ppl−sonar−pro−high ppl−sonar−pro api−gpt−4o−mini−search api−gpt−4o−search gemini−2.5−pro−grounding ppl−sonar api−gpt−4o−search−high api−gpt−4o−search−high−loc gemini−2.0−flash−grounding ppl−sonar−reasoning ppl−sonar−reasoning−pro−high 0.0 0.1 0.2 0.3 0.4 β^ 1m（每个额外 URL 的引用） Gemini GPT 声纳 注意：额外焦点模型打开的每个附加 URL 获得的引用（模型之间的差异）。这使匹配效果保持不变，隔离技术效果。

### 段落 66 · Page 15

**EN**

Regression coefficientβ1m shown, predicting differences in citations for model pairs, for a given query. See equation above. More specifically, our results show that RAG implementation type (technology) is more important than model family (e.g., OpenAI vs. Gemini): • An ANOVA test shows that within-family variation (the variance) of search coefficients β1m is almost 8 times larger than between-family variation.

**中文**

显示回归系数β1m，预测给定查询的模型对的引用差异。参见上面的等式。更具体地说，我们的结果表明，RAG 实现类型（技术）比模型系列更重要（例如，OpenAI 与 Gemini）： • ANOVA 测试表明，搜索系数 β1m 的族内变异（方差）几乎是族间变异的 8 倍。

### 段落 67 · Page 15

**EN**

This means that differences in model behavior is far greaterwithin model families than between them.18 • Within Sonar alone, upgrading to thereasoningtier more than doubles efficiency (from 0.19-0.20→0.44-0.45), with Sonar-reasoning (0.44) vs Sonar-pro-high (0.19) = 0.25 18We ran a one–way ANOVA on the eleven citation–efficiency coefficients (ˆβ1m on focal_search_diff) grouped by provider family. Thewithin–familymean square is nearly eight times thebetween–familymean square: MSwithin = 0 .0116, MSbetween = 0 .0015, F (2,8) = 0.0015 0.0116 ≈0.13, p= 0.88.

**中文**

这意味着模型家族内部的模型行为差异比模型家族之间的差异要大得多。18 • 仅在 Sonar 中，升级到推理层使效率提高一倍以上（从 0.19-0.20→0.44-0.45），其中 Sonar-reasoning (0.44) vs Sonar-pro-high (0.19) = 0.25 18我们对 11 个引用效率系数进行了单向方差分析(ˆβ1m on focus_search_diff) 按提供者系列分组。族内均方几乎是族间均方的 8 倍：MS 内 = 0 .0116，MS 间 = 0 .0015，F (2,8) = 0.0015 0.0116 ≈0.13，p= 0.88。

### 段落 68 · Page 15

**EN**

Thus, variability inside each provider family dominates the small differences between family means: implementation choices explain∼8×more of the spread in citation efficiency than the family label itself. 13

**中文**

因此，每个提供者家族内部的变异性主导了家族均值之间的微小差异：实现选择解释了比家族标签本身更多的引文效率传播~8倍。 13

### Page 16

### 段落 69 · Page 16

**EN**

difference. For GPT models: GPT-4o-search-high-loc (0.42) vs GPT-4o-mini (0.25) = 0.17 difference. • Location signalsmatter too. Adding a country code to GPT-4o raises search-citation coefficient efficiency by roughly 10% (0.39→0.43), confirming that retrieval relevance translates directly into better attribution (though it is unclear why this is the case). Practically, this effect size is moderate since for a model getting 10 extra search results, location signals would generate≈0.37 additional citations. But we know that local search operates differently, both in traditional search and increasingly with LLMs [21].

**中文**

差异。对于 GPT 模型：GPT-4o-search-high-loc (0.42) 与 GPT-4o-mini (0.25) = 0.17 差异。 • 位置信号也很重要。在 GPT-4o 中添加国家代码可将搜索引用系数效率提高约 10%（0.39→0.43），证实检索相关性可直接转化为更好的归因（尽管尚不清楚为什么会出现这种情况）。实际上，这种效应大小是中等的，因为对于获得 10 个额外搜索结果的模型，位置信号将产生约 0.37 个额外引用。但我们知道本地搜索的运作方式有所不同，无论是在传统搜索中还是越来越多的法学硕士[21]。

### 段落 70 · Page 16

**EN**

Lastly, the regression results show that more basic models (GPT-mini, GPT-search, and basic Sonar models) compensate for lower search efficiency through verbosity – they need longeranswerstoachievesimilarcitationperformance. Advanced(‘high’variantandGemini) models achieve higher citation rates through superior search utilization, making verbosity unnecessary to achieve improved citation rates. 6 Policy Implications Without standardized telemetry — comprehensive logs and traces of what an LLM retrieves and cites — no transparent and competitive market for licensing, revenue-sharing, or other content-monetization schemes can easily emerge.

**中文**

最后，回归结果表明，更基本的模型（GPT-mini、GPT-search 和基本 Sonar 模型）通过冗长来补偿较低的搜索效率 - 它们需要更长的答案才能实现类似的引文性能。高级（“high”variantandGemini）模型通过卓越的搜索利用率实现了更高的引用率，无需冗长的内容即可提高引用率。 6 政策影响 如果没有标准化的遥测技术（法学硕士检索和引用内容的全面日志和跟踪），就不可能轻易出现许可、收入共享或其他内容货币化计划的透明且竞争性的市场。

### 段落 71 · Page 16

**EN**

Publishers need hard numbers on how often their pages power an answer in order to automate royalty or revenue-share flows; regulators need the same auditable data to enforce forthcoming disclosure rules in jurisdictions such as the European Union (EU) and California. In short, richer telemetry isthe prerequisite for both commercial remuneration and public oversight. The technical pieces already exist for full disclosure of an LLM’s search and citation trace; what remains is coordination. The key challenge is to persuade providers to adopt a common telemetry standard — and to ensure buyers and regulators can incentivize its provision.

**中文**

出版商需要关于其页面提供答案的频率的硬性数据，以便实现版税或收入分成流程的自动化；监管机构需要相同的可审计数据来执行欧盟 (EU) 和加利福尼亚州等司法管辖区即将出台的披露规则。简而言之，更丰富的遥测是商业报酬和公共监督的先决条件。用于全面披露法学硕士的检索和引用跟踪的技术部分已经存在；剩下的就是协调。关键的挑战是说服提供商采用通用遥测标准，并确保买家和监管机构能够激励其提供。

### 段落 72 · Page 16

**EN**

Modern observability frameworks — LangSmith, Langfuse, Phoenix, and the GenAI semantic-conventions in OpenTelemetry — allow for recording an end-to-endsearch trace, which can detail the search activities that an LLM RAG system undertakes when trying to find the most relevant context for the user. One way to think of traces is as a collection of structured logs with context, correlation, and hierarchy baked in. Each web page retrieval, reranking, and generation step by the LLM can be logged as an OpenTelemetry span, provided every document is tagged with a stableSource ID, typically a hash of the original URL 14

**中文**

现代可观察性框架——LangSmith、Langfuse、Phoenix 和 OpenTelemetry 中的 GenAI 语义约定——允许记录端到端搜索跟踪，这可以详细说明 LLM RAG 系统在尝试为用户找到最相关上下文时所进行的搜索活动。将跟踪视为包含上下文、相关性和层次结构的结构化日志的集合。LLM 的每个网页检索、重排和生成步骤都可以记录为 OpenTelemetry 范围，前提是每个文档都标有 stableSource ID（通常是原始 URL 14 的哈希值）

### Page 17

### 段落 73 · Page 17

**EN**

or file.19 Because hashes are one-way fingerprints, they enable later verification without revealing copyrighted text. The same span can carry the numerical relevance score (‘how relevant was this webpage to the LLM’s answer’) produced by the vector store, BM25 index, or cross-encoder, as long as that score is preserved in the trace [15, 23].

**中文**

19 由于散列是单向指纹，因此它们可以在不泄露受版权保护的文本的情况下进行后续验证。同一跨度可以携带由向量存储、BM25 索引或交叉编码器生成的数字相关性得分（“该网页与 LLM 答案的相关程度如何”），只要该得分保留在跟踪中即可 [15, 23]。

### 段落 74 · Page 17

**EN**

If each retrieved document carries two stable fields — sayllm.retrieval.ids (a hash or URL that uniquely identifies the page) andllm.retrieval.scores (its relevance score or rank) —and those fields are propagated from the retrieval step all the way to the final API response, then anyone inspecting the trace can, in theory: 1. Enumerate every page the model actually saw; 2. Check which of those pages were later cited in the answer; and 3. Compare the relevance scores of cited pages with those that were ignored.

**中文**

如果每个检索到的文档都带有两个稳定字段 - sayllm.retrieval.ids（唯一标识页面的哈希或 URL）和 llm.retrieval.scores（其相关性分数或排名） - 并且这些字段从检索步骤一直传播到最终的 API 响应，那么理论上，任何检查跟踪的人都可以： 1. 枚举模型实际看到的每个页面； 2. 检查答案中后来引用了哪些页面； 3. 比较被引用页面与被忽略页面的相关性分数。

### 段落 75 · Page 17

**EN**

In short, the full provenance of “pages viewed” versus “pages credited” becomes auditable.20 OpenTelemetry-like open protocols can be a lightweight standard that enables comparison and validation of LLM behavior across models. And adopting telemetry protocols (standards) requires only incremental changes to today’s open-source stacks.21 The real challenge, perhaps, lies in constructing the market and regulatory incentives to advance widespread adoption and disclosure. Transparent traces unlock clear, quantifiable monetary benefits for providers. API buyers in legal, medical, and financial sectors increasingly require provenance guarantees.

**中文**

简而言之，“查看的页面”与“记入的页面”的完整来源变得可审计。20 类似 OpenTelemetry 的开放协议可以成为一个轻量级标准，可以跨模型比较和验证 LLM 行为。采用遥测协议（标准）只需要对当今的开源堆栈进行增量更改。21真正的挑战也许在于构建市场和监管激励措施以促进广泛采用和披露。透明的痕迹为提供商带来了清晰、可量化的货币利益。法律、医疗和金融领域的 API 买家越来越需要来源保证。

### 段落 76 · Page 17

**EN**

This means that model developers that expose richer evidence trails could, therefore, command premium pricing and benefit from greater demand in these compliance-sensitive sectors. However, the model developers may be reticent to undertake such additional disclosures without liability safeguards or more reliable RAG pipelines. Yet our findings also point toward possible paths forward. A business model for LLM search could create a mutually beneficial exchange of content for web traffic or direct purchases. Commercial queries present a fairly distinctive pattern in our analysis.

**中文**

这意味着，公开更丰富证据线索的模型开发人员可以获得溢价，并从这些合规敏感行业的更大需求中受益。然而，如果没有责任保障或更可靠的 RAG 管道，模型开发人员可能不愿进行此类额外披露。然而我们的研究结果也指出了可能的前进道路。 LLM 搜索的商业模式可以为网络流量或直接购买创建互惠互利的内容交换。商业查询在我们的分析中呈现出一种相当独特的模式。

### 段落 77 · Page 17

**EN**

Shopping and commercial-intent queries show attribution gaps 76% larger than other categories, yet these domains offer opportunities for such mutually beneficial arrangements. Early web ad- 19With a span representing a unit of work or operation and are the building blocks of traces. See: https://opentelemetry.io/docs/concepts/signals/traces/. 20https://opentelemetry.io/docs/specs/semconv/gen-ai/ 21In LangChain, a single line of code drops the hash and score intoDocument.metadata. LangSmith then records them automatically in each trace span [15]. Langfuse performs the same mapping when it converts LangChain calls into OpenTelemetry.

**中文**

购物和商业意图查询显示归因差距比其他类别大 76%，但这些领域为这种互惠互利的安排提供了机会。早期的网络广告- 19用一个跨度代表一个工作或操作单元，是痕迹的构建块。请参阅：https://opentelemetry.io/docs/concepts/signals/traces/。 20https://opentelemetry.io/docs/specs/semconv/gen-ai/ 21在LangChain中，一行代码将哈希值和分数放入Document.metadata中。然后 LangSmith 在每个跟踪范围内自动记录它们 [15]。 Langfuse 在将 LangChain 调用转换为 OpenTelemetry 时执行相同的映射。

### 段落 78 · Page 17

**EN**

Phoenix ingests any span that follows the GenAI conventions, meaning dashboards that plot “high-score pages not cited” or “low-score pages that slipped through” can be deployed without further engineering. 15

**中文**

Phoenix 吸收遵循 GenAI 约定的任何跨度，这意味着可以部署绘制“未引用的高分页面”或“漏掉的低分页面”的仪表板，而无需进一步进行工程设计。 15

### Page 18

### 段落 79 · Page 18

**EN**

vertising models, where attribution facilitated click-through and conversion, provide relevant precedents for sustainable approaches. 7 Conclusion This study provides one of the first systematic empirical audits of attribution practices in commercial search-augmented LLMs. When LLMs exploit content from platforms without proper attribution, they undermine the economic incentives that sustain high-quality information production.

**中文**

广告模式中的归因促进了点击率和转化，为可持续方法提供了相关先例。 7 结论 本研究提供了对商业搜索增强法学硕士归因实践的首次系统实证审计之一。当法学硕士在没有适当归属的情况下利用平台上的内容时，他们会破坏维持高质量信息生产的经济激励。

### 段落 80 · Page 18

**EN**

Returning to our opening quote by the late economist Joan Robinson – on the notion that exploitation under capitalism involves the absence of commercial relations as well as its presence – we find similar twin forces at work in our analysis. Gemini systematically excludes the world wide web’s content ecosystem when answering questions as its form of exploitation, while Perplexity exploits through the opposite behavior, overly zealous consumption of web content without commensurate attributions.

**中文**

回到已故经济学家琼·罗宾逊的开场白——资本主义下的剥削既涉及商业关系的存在，也涉及商业关系的缺失——我们在分析中发现了类似的双重力量在发挥作用。双子座在回答问题时系统地排除万维网的内容生态系统作为其剥削形式，而困惑则通过相反的行为，过度热衷地消费网络内容而没有相应的归因来进行剥削。

### 段落 81 · Page 18

**EN**

We find a substantial “attribution gap” between relevant content consumed from websites and attribution practices that threatens the sustainability of the digital content ecosystem. Our analysis of≈14,000 real-world interactions demonstrates that leading AI systems systematically consume web content without adequate attribution, with Gemini providing no citations in 92% of its responses and Perplexity visiting approximately a dozen relevant websites while crediting only a few.

**中文**

我们发现网站消费的相关内容与归因实践之间存在巨大的“归因差距”，威胁着数字内容生态系统的可持续性。我们对约 14,000 次现实世界交互的分析表明，领先的人工智能系统系统地消耗网络内容而没有充分的归因，Gemini 在 92% 的回复中没有提供引用，而 Perplexity 访问了大约十几个相关网站，但只对少数网站进行了引用。

### 段落 82 · Page 18

**EN**

A negative binomial hurdle model shows that the average query answered by Gemini or Sonar leaves about 3 relevant websites uncited, whereas GPT-4o’s tiny uncited gap is best explained by its selective log disclosures rather than by better attribution. GPT-4o models remain difficult to audit due to what appears to be stricter pre-filtering of its model search logs. The dramatic variation in citation efficiency between models when answering the same question – from 0.19 to 0.45 citations per additional web page visited – illustrate that attribution gaps result from design choices, not simply technical limitations.

**中文**

负二项式障碍模型显示，Gemini 或 Sonar 回答的平均查询留下大约 3 个未引用的相关网站，而 GPT-4o 的微小未引用差距最好是通过其选择性日志披露而不是更好的归因来解释。由于模型搜索日志的预过滤似乎更加严格，GPT-4o 模型仍然难以审核。当回答同一问题时，模型之间的引用效率存在巨大差异——每个额外访问的网页有 0.19 到 0.45 次引用——说明归因差距是由设计选择造成的，而不仅仅是技术限制造成的。

### 段落 83 · Page 18

**EN**

The best-performing systems show that transparent, comprehensive attribution is technically feasible today (even if accurate citations and output remain a real ongoing issue). Closing the attribution gap is, therefore, less a technical hurdle than one of proper coordination and market incentives. Standardizing two telemetry fields — document hashes and relevance scores — would allow anyone to verify which information an LLM consumed and how faithfully it credited that information. Observability tools already provide the necessary plumbing.

**中文**

性能最佳的系统表明，透明、全面的归因在当今技术上是可行的（即使准确的引用和输出仍然是一个真正持续存在的问题）。因此，缩小归因差距与其说是一个技术障碍，不如说是适当的协调和市场激励措施之一。标准化两个遥测字段——文档哈希和相关性分数——将允许任何人验证法学硕士使用了哪些信息以及它对这些信息的信任程度。可观测性工具已经提供了必要的管道。

### 段落 84 · Page 18

**EN**

What remains is a collective decision by model providers to enable it and by developers and buyers to reward those who do. Transparent search traces would 16

**中文**

剩下的就是模型提供商的集体决定，以实现这一目标，以及开发商和买家的集体决定，以奖励那些这样做的人。透明搜索痕迹将 16

### Page 19

### 段落 85 · Page 19

**EN**

strengthen incentives for high-quality content and give users a robust evidentiary basis for trusting machine-generated answers. Our results demonstrate that transparency in the web sources consumed and cited by LLMs when answering user queries is fundamentally an engineering choice.22 22This aligns with emerging research on LLM citation evaluation frameworks [9] and attribution methods in scientific literature [17, 24], which show that technical solutions are available but underutilized. Sourceaware training and fine-tuning have also been shown to improve citation behavior [14]. See also Asai et al. [1] and Borgeaud et al. [3]. 17

**中文**

加强对高质量内容的激励，并为用户信任机器生成的答案提供坚实的证据基础。我们的结果表明，法学硕士在回答用户查询时使用和引用的网络资源的透明度从根本上来说是一种工程选择。22 22这与法学硕士引文评估框架 [9] 和科学文献中的归因方法 [17, 24] 的新兴研究相一致，这些研究表明技术解决方案是可用的，但未得到充分利用。来源感知训练和微调也被证明可以改善引用行为 [14]。另见浅井等人。 [1] 和 Borgeaud 等人。 [3]。 17 号

### Page 20

### 段落 86 · Page 20

**EN**

References [1] Akari Asai, Zeqiu Wu, Yizhong Wang, Avirup Sil, and Hannaneh Hajishirzi. Selfrag: Learning to retrieve, generate, and critique through self-reflection.arXiv preprint arXiv:2310.11511, 2023. [2] AutoGPT. Perplexityaifacesattributioncontroversy, 062024. URL https://autogpt. net/perplexity-ai-faces-attribution-controversy/. [3] Sebastian Borgeaud, Arthur Mensch, Jordan Hoffmann, Trevor Cai, Eliza Rutherford, Katie Millican, George Van Den Driessche, Jean-Baptiste Lespiau, Bogdan Damoc, Aidan Clark, et al. Improving language models by retrieving from trillions of tokens.

**中文**

参考文献 [1] Akari Asai、Zeqiu Wu、Yizhong Wang、Avirup Sil 和 Hannaneh Hajishirzi。 Selfrag：通过 self-reflection 学习检索、生成和批评。arXiv 预印本 arXiv:2310.11511, 2023。[2] AutoGPT。困惑aifaces归属争议，062024。URL https://autogpt。网/perplexity-ai-faces-attribution-controversy/. [3] Sebastian Borgeaud、Arthur Mensch、Jordan Hoffmann、Trevor Cai、Eliza Rutherford、Katie Millican、George Van Den Driessche、Jean-Baptiste Lespiau、Bogdan Damoc、Aidan Clark 等。通过检索数万亿个标记来改进语言模型。

### 段落 87 · Page 20

**EN**

Proceedings of the 39th International Conference on Machine Learning, pages 2206– 2240, 2022. [4] Sarah Cool-Fergus. What happens when the news starts answering back? in conversation with miso.ai ceo, lucky gunasekara, 2025. URLhttps://www.twipemobile.com/ what-happens-when-the-news-starts-answering-back-in-conversation-with-miso-ai-ceo-lucky-gunasekara/ . Interview with Lucky Gunasekara, CEO of Miso.ai, from AI Frontrunners in News webinar series. [5] Oli Elliott and Pete Archer. Representation of bbc news content by ai assistants. Research report, BBC, 02 2025.

**中文**

第 39 届国际机器学习会议论文集，第 2206-2240 页，2022 年。 [4] Sarah Cool-Fergus。当新闻开始回应时会发生什么？与 miso.ai 首席执行官 lucky Gunasekara 对话，2025 年。 URL https://www.twipemobile.com/what-happens-when-the-news-starts-answering-back-in-conversation-with-miso-ai-ceo-lucky-gunasekara/。新闻网络研讨会系列中人工智能领跑者对 Miso.ai 首席执行官 Lucky Gunasekara 的采访。 [5] 奥利·埃利奥特和皮特·阿彻。由人工智能助理呈现 BBC 新闻内容。研究报告，BBC，2025 年 2 月。

### 段落 88 · Page 20

**EN**

URLhttps://www.bbc.co.uk/aboutthebbc/ documents/bbc-research-into-ai-assistants.pdf. [6] Reza Fayyazi, Michael Zuzak, and Shanchieh Jay Yang. Llm embedding-based attribution (lea): Quantifying source contributions to generative model’s response for vulnerability analysis.arXiv preprint arXiv:2506.12100, 2025. URLhttps://arxiv.org/ abs/2506.12100. cs.CR. [7] Ben Fine. Marx’s capital, 1989. [8] Tianyu Gao, Howard Yen, Jiatong Yu, and Danqi Chen. Enabling large language models to generate text with citations.arXiv preprint arXiv:2305.14627, 2023. [9] Tianyu Gao, Howard Yen, Jiatong Yu, and Danqi Chen.

**中文**

网址https://www.bbc.co.uk/aboutthebbc/documents/bbc-research-into-ai-assistants.pdf。 [6] Reza Fayyazi、Michael Zuzak 和 Shanchieh Jay Yang。基于 Llm 嵌入的归因 (lea)：量化源贡献对生成模型响应的漏洞分析。arXiv 预印本 arXiv:2506.12100, 2025。URLhttps://arxiv.org/abs/2506.12100。 cs.CR。 [7] 本·法恩.马克思的首都，1989。 [8] 高天宇，甄子丹，余家同，陈丹琪。使大型语言模型能够生成带有引用的文本。arXiv 预印本 arXiv:2305.14627, 2023。 [9] Tianyu Gau、Howard Yen、Jiatong Yu 和 Danqi Chen。

### 段落 89 · Page 20

**EN**

Enabling large language models to generate text with citations.arXiv preprint arXiv:2305.14627, 2023. [10] Hacker News. Citations on the anthropic api, 2025. URLhttps://news.ycombinator. com/item?id=42807173. Discussion thread on Claude citation behavior. 18

**中文**

使大型语言模型能够使用 itations.arXiv 预印本 arXiv:2305.14627, 2023 生成文本。 [10] 黑客新闻。 anthropic api 上的引用，2025 年。URL https://news.ycombinator。 com/item?id=42807173。关于克劳德引用行为的讨论线程。 18

### Page 21

### 段落 90 · Page 21

**EN**

[11] Samuel Hollander.Classical Economics. University of Toronto Press, 1992. [12] Baixiang Huang, Canyu Chen, and Kai Shu. Authorship attribution in the era of llms: Problems, methodologies, and challenges.ACM SIGKDD Explorations Newsletter, 26 (2):21–43, 2025. [13] Jie Huang and Kevin Chen-Chuan Chang. Citation: A key to building responsible and accountable large language models.arXiv preprint arXiv:2307.02185, 2023. [14] Muhammad Khalifa, David Wadden, Emma Strubell, Honglak Lee, Lu Wang, Iz Beltagy, and Hao Peng. Source-aware training enables knowledge attribution in language models. arXiv preprint arXiv:2404.01019, 2024. [15] LangChain.

**中文**

[11] 塞缪尔·霍兰德。古典经济学。多伦多大学出版社，1992。 [12] 黄百祥，陈灿宇，舒凯。 llms 时代的作者归属：问题、方法和挑战。ACM SIGKDD Explorations Newsletter，26 (2):21–43, 2025。 [13] Jie Huang 和 Kevin Chen-Chuan Chang。引文：构建负责任的大型语言模型的关键。arXiv 预印本 arXiv：2307.02185，2023。 [14] Muhammad Khalifa、David Wadden、Emma Strubell、Honglak Lee、Lu Wang、Iz Beltagy 和hao Peng。源感知训练可以实现语言模型中的知识归因。 arXiv 预印本 arXiv:2404.01019, 2024。 [15] LangChain。

### 段落 91 · Page 21

**EN**

Howtogetaragapplicationtoaddcitations. https://python.langchain. com/docs/how_to/qa_citations/, 2025. Accessed 24 June 2025. [16] Dongfang Li, Zetian Sun, Xinshuo Hu, Zhenyu Liu, Ziyang Chen, Baotian Hu, Aiguo Wu, and Min Zhang. A survey of large language models attribution.arXiv preprint arXiv:2311.03731, 2023. [17] Ayat Najjar, Huthaifa I. Ashqar, et al. Leveraging explainable ai for llm text attribution: Differentiating human-written and multiple llms-generated text.arXiv preprint arXiv:2501.03212, 01 2025. URLhttps://arxiv.org/abs/2501.03212. [18] Tim O’Reilly. How to fix “ai’s original sin”, 06 2024.

**中文**

如何获取标记应用程序以添加引文。 https://python.langchain。 com/docs/how_to/qa_itations/，2025 年。2025 年 6 月 24 日访问。[16] Dongfang Li、Zetian Sun、Xinshuo Hu、Zhenyu Liu、Ziyang Chen、Baotian Hu、Aiguo Wu 和 Min Zhang。大型语言模型归因调查。arXiv 预印本 arXiv:2311.03731, 2023。 [17] Ayat Najjar、Huthaifa I. Ashqar 等人。利用可解释的人工智能进行 llm 文本归属：区分人类编写的文本和多个 llms 生成的文本。arXiv 预印本 arXiv:2501.03212, 01 2025。URLhttps://arxiv.org/abs/2501.03212。 [18] 蒂姆·奥莱利。如何修正“艾的原罪”，06 2024。

### 段落 92 · Page 21

**EN**

URLhttps://www.oreilly.com/ radar/how-to-fix-ais-original-sin/. O’Reilly Radar. [19] Profound. Ai platform citation patterns: How chatgpt, google ai overviews, and perplexity source information, 2025. URL https://www.tryprofound.com/blog/ ai-platform-citation-patterns. Research analysis from August 2024 to June 2025. [20] Reuters. Bbc threatens legal action against ai startup perplexity over content scraping, ft reports. Reuters, 06 2025. URL https://www.reuters.com/business/media-telecom/ bbc-threatens-legal-action-against-ai-start-up-perplexity-over-content-scraping-2025-06-20/ . Accessed 24 June 2025. [21] Damian Rollison.

**中文**

网址 https://www.oreilly.com/radar/how-to-fix-ais-original-sin/。奥莱利雷达。 [19] 深刻。人工智能平台引用模式：如何chatgpt、谷歌人工智能概述和困惑源信息，2025。URL https://www.tryprofound.com/blog/ai-platform-itation-patterns。 2024年8月至2025年6月的研究分析。[20]路透社。据英国《金融时报》报道，英国广播公司威胁要对人工智能初创公司在内容抓取方面的困惑采取法律行动。路透社，2025 年 6 月。URL https://www.reuters.com/business/media-telecom/bbc-threatens-legal-action-against-ai-start-up-perplexity-over-content-scraping-2025-06-20/。访问日期：2025 年 6 月 24 日。[21] 达米安·罗里森。

### 段落 93 · Page 21

**EN**

How does chatgpt conduct local searches?, 05 2025. URL https: //searchengineland.com/how-does-chatgpt-conduct-local-searches-454894 . Search Engine Land. 19

**中文**

chatgpt 如何进行本地搜索？，05 2025。URL https://searchengineland.com/how-does-chatgpt-conduct-local-searches-454894。搜索引擎土地。 19

### Page 22

### 段落 94 · Page 22

**EN**

[22] Sruly Rosenblat, Tim O’Reilly, and Ilan Strauss. Beyond public access in llm pretraining data: Non-public book content in openai’s models. Technical Report SSRC AI WP 2025-04, Social Science Research Council, 04 2025. URLhttps://ssrc-static. s3.us-east-1.amazonaws.com/OpenAI-Training-Violations-OReillyBooks_ Sruly-OReilly-Strauss_SSRC_04012025.pdf. [23] Michael Ryaboy. Cross–encoders, colbert, and llm–based re–rankers: A practical guide. https://medium.com/@aimichael/ cross-encoders-colbert-and-llm-based-re-rankers-a-practical-guide-a23570d88548 , 2025. Accessed 24 June 2025.

**中文**

[22] 斯鲁利·罗森布拉特、蒂姆·奥莱利和伊兰·施特劳斯。超越llm预训练数据的公共访问：openai模型中的非公开书籍内容。技术报告 SSRC AI WP 2025-04，社会科学研究理事会，2025 年 04 月。URLhttps://ssrc-static。 s3.us-east-1.amazonaws.com/OpenAI-Training-Violations-OReillyBooks_ Sruly-OReilly-Strauss_SSRC_04012025.pdf。 [23] 迈克尔·里亚博伊。交叉编码器、colbert 和基于 llm 的重新排序器：实用指南。 https://medium.com/@aimichael/ cross-encoders-colbert-and-llm-based-re-rankers-a-practical-guide-a23570d88548，2025 年。2025 年 6 月 24 日访问。

### 段落 95 · Page 22

**EN**

[24] Yash Saxena, Deepa Tilwani, Ali Mohammadi, Edward Raff, Amit Sheth, Srinivasan Parthasarathy, and Manas Gaur. Attribution in scientific literature: New benchmark and methods. arXiv e-prints, pages arXiv–2405, 2024. [25] Jordan-Marie Smith, Christopher Intagliata, and Mary Louise Kelly. The trump administration’s report on kids’ health cites made-up scientific studies, 05 2025. URL https://www.npr.org/2025/05/30/nx-s1-5417962/ the-trump-administrations-report-on-kids-health-cites-made-up-scientific-studies . [26] Patrick Stox. Websites with more organic search traffic get mentioned more in ai search.

**中文**

[24] Yash Saxena、Deepa Tilwani、Ali Mohammadi、Edward Raff、Amit Sheth、Srinivasan Parthasarathy 和 Manas Gaur。科学文献的归属：新基准和方法。 arXiv 电子印刷品，第 arXiv–2405 页，2024 年。 [25] Jordan-Marie Smith、Christopher Intagliata 和 Mary Louise Kelly。特朗普政府关于儿童健康的报告引用了 2025 年 5 月捏造的科学研究。网址 https://www.npr.org/2025/05/30/nx-s1-5417962/ the-trump-administrations-report-on-kids-health-cites-made-up-scientific-studies。 [26] 帕特里克·斯托克斯。具有更多自然搜索流量的网站在人工智能搜索中被提及的次数更多。

### 段落 96 · Page 22

**EN**

https://ahrefs.com/blog/websites-with-more-traffic-have-more-mentions/ , 2025. Accessed 24 June 2025. [27] Xiang Yue, Boshi Wang, Ziru Chen, Kai Zhang, Yu Su, and Huan Sun. Automatic evaluation of attribution by large language models.arXiv preprint arXiv:2305.06311, 2023. [28] Matt Zwolinski, Benjamin Ferguson, and Alan Wertheimer. Exploitation. In Edward N. Zalta and Uri Nodelman, editors,The Stanford Encyclopedia of Philosophy. Metaphysics ResearchLab, StanfordUniversity, Winter2022edition, 2022. Accessed: August5, 2025. 20

**中文**

https://ahrefs.com/blog/websites-with-more-traffic-have-more-mentions/，2025 年。2025 年 6 月 24 日访问。[27] 翔岳、王博时、陈自如、张凯、苏宇和孙焕。通过大型语言模型自动评估归因。arXiv 预印本 arXiv:2305.06311, 2023。 [28] Matt Zwolinski、Benjamin Ferguson 和 Alan Wertheimer。开发。爱德华·N·扎尔塔 (Edward N. Zalta) 和乌里·诺德尔曼 (Uri Nodelman) 编辑，《斯坦福哲学百科全书》。斯坦福大学形而上学研究实验室，2022 年冬季版，2022 年。访问时间：2025 年 8 月 5 日。20

### Page 23

### 段落 97 · Page 23

**EN**

8 Appendix 8.1 Full Hurdle-Model Specification and Diagnostics The regression is estimated with R’spscl::hurdle()function, which maximizes a likelihood that combines abinary gate for perfect attribution and azero-truncated negative binomial (NB) for positive gaps. Writingπi≡Pr(Yi = 0), the log-likelihood is ℓ(γ,β,α) = ∑ i:yi=0 logπi + ∑ i:yi>0 { log(1−πi) + logfNB(yi|λi,α)−log [ 1−fNB(0|λi,α) ]} , (A1) withγ= (γ0,γ1,γ2,γ3)⊤for the gate andβ= (β0,β1,β2,β3,β4)⊤for the count component. The NB kernel is parameterised by its meanλi and over-dispersionα>0: fNB(y|λi,α) = Γ ( y +α−1 ) Γ(α−1)y! ( αλi )y( 1 +αλi )− ( y+α−1 ) , Var(Yi|Yi≥1) =λi +αλ2 i.

**中文**

8 附录 8.1 完整的障碍模型规范和诊断 使用 R 的 spscl::hurdle() 函数来估计回归，该函数最大限度地结合了完美归因的二元门和正差距的零截断负二项式 (NB)。写πieqPr(Yi = 0)，对数似然为 ℓ(γ,β,α) = Σ i:yi=0 logπi + Σ i:yi>0 { log(1−πi) + logfNB(yi|λi,α)−log [ 1−fNB(0|λi,α) ]} , (A1) 其中γ= (γ0,γ1,γ2,γ3)⊤门和 β= (β0,β1,β2,β3,β4)⊤ 为计数分量。 NB 核通过其平均值 λi 和过分散 α>0 进行参数化： fNB(y|λi,α) = Г ( y +α−1 ) Г(α−1)y！ ( αλi )y( 1 +αλi )− ( y+α−1 ) , Var(Yi|Yi≥1) = λi + αλ2 i。

### 段落 98 · Page 23

**EN**

(A2) Likelihood ratio tests can assess whether the count process is better modeled as Poisson or negative binomial (null hypothesisH0 :α= 0), and whether inclusion of the interaction term improves model fit. A negative binomial outperforms. Model fits (information criteria) are superior with interaction terms and shows domains where the effect of a model family changes the expected gap magnitude. With interaction terms the zero-inflated model performs better in a Vuong test than a hurdle model. Our hurdle model though aligns better with theoretical understanding of citation process.

**中文**

(A2) 似然比检验可以评估计数过程是否更好地建模为泊松或负二项式（零假设H0：α= 0），以及包含交互项是否可以改善模型拟合。负二项式表现优于。模型拟合（信息标准）优于交互项，并显示模型族的影响改变预期差距大小的领域。使用交互项，零膨胀模型在 Vuong 测试中比障碍模型表现更好。不过，我们的障碍模型更符合引文过程的理论理解。

### 段落 99 · Page 23

**EN**

We believe interpretability advantages outweigh improvements though. BFGS optimisation converged in 54 iterations, givingˆθ= 5.69. 21

**中文**

不过，我们相信可解释性的优势胜过改进。 BFGS 优化在 54 次迭代中收敛，给出 ˆθ= 5.69。 21

### Page 24

### 段落 100 · Page 24

**EN**

Figure 3. Attribution Gap Histogram vs Negative Binomial (Red) size=1.94 mu=7.48 0.000 0.025 0.050 0.075 0.100 0 50 100 Attribution Gap Probability Note: Attribution gap (relevant sites visited in logs minus websites cited by in-text URLS) shows a negative binomial distribution (red over-plot). 8.2 Detailed Model Results Figure 4 shows topic specific gaps, as predicted by our model. ‘Shopping & Commercial Intent’, perhaps surprisingly, shows the largest gap across models – being 0.2 lower for the Sonar model family.

**中文**

图 3. 归因差距直方图与负二项式（红色）大小=1.94 mu=7.48 0.000 0.025 0.050 0.075 0.100 0 50 100 归因差距概率 注：归因差距（日志中访问的相关网站减去文本 URL 引用的网站）显示负二项分布（红色）过度情节）。 8.2 详细的模型结果 图 4 显示了我们的模型预测的特定主题的差距。也许令人惊讶的是，“购物和商业意向”显示了不同型号之间的最大差距——Sonar 型号系列低了 0.2。

### 段落 101 · Page 24

**EN**

This could reflect a greater selectivity in which results are shown by the model given potential greater commercial incentives to ‘get it right’, or to abide by preexisting licensing agreements. But it also could simply highlight the absence of a worked out business model in this area, despite large opportunities to monetize website traffic in this area of LLM search. 22

**中文**

这可能反映了模型显示结果的更大选择性，考虑到潜在的更大商业激励措施“做对”或遵守预先存在的许可协议。但这也可能只是突显了该领域缺乏成熟的商业模式，尽管在法学硕士搜索领域有很大的机会通过网站流量货币化。 22

### Page 25

### 段落 102 · Page 25

Figure 4.

### 段落 103 · Page 25

**EN**

Expected Citation Gaps by Regression Model (Query Classification and Model Family) 0.2 0.2 0.2 0.1 0.2 0.2 0.2 0.2 0.2 0.1 0.3 0.3 3.7 3.1 3.5 3.9 3.5 3.7 3.8 3.4 3.4 3.3 3.7 3.8 2.9 3.0 3.3 2.4 3.3 2.5 3.3 3.0 3.2 2.1 3.5 3.3 Gemini Sonar GPT 0 1 2 3 0 1 2 3 4 0.0 0.1 0.2 0.3 Other Education Games, Fantasy & Creative Writing Computer Science & Software Engineering Current Affairs & Factual Information History Data Science Finance & Economics Mental & Physical Health & Relationships Lifestyle Sports Shopping & Commercial Intent Current Affairs & Factual Information Other Lifestyle Mental & Physical Health & Relationships Finance & Economics D

**中文**

按回归模型（查询分类和模型系列）划分的预期引文差距 0.2 0.2 0.2 0.1 0.2 0.2 0.2 0.2 0.2 0.1 0.3 0.3 3.7 3.1 3.5 3.9 3.5 3.7 3.8 3.4 3.4 3.3 3.7 3.8 2.9 3.0 3.3 2.4 3.3 2.5 3.3 3.0 3.2 2.1 3.5 3.3 Gemini Sonar GPT 0 1 2 3 0 1 2 3 4 0.0 0.1 0.2 0.3 其他教育游戏、奇幻与创意写作 计算机科学与软件工程 时事与事实信息 历史数据科学 金融与经济 心理与身体健康与人际关系 生活方式 体育运动 购物与商业意图 时事与事实信息 其他生活方式 心理与身体健康与人际关系 财经 D

### 段落 104 · Page 25

**EN**

ata Science Shopping & Commercial Intent Computer Science & Software Engineering Games, Fantasy & Creative Writing History Sports Education Other Education Games, Fantasy & Creative Writing Computer Science & Software Engineering Lifestyle Current Affairs & Factual Information Mental & Physical Health & Relationships History Data Science Finance & Economics Sports Shopping & Commercial Intent Expected Attribution Gap Note: Bars show the expected citation gap (relevant websites visited in the logs minus websites cited in the LLM’s output) for each query classification.

**中文**

ata 科学 购物与商业意图 计算机科学与软件工程 游戏、奇幻与创意写作 历史 体育教育 其他教育游戏、奇幻与创意写作 计算机科学与软件工程 生活方式 时事与事实信息 心理与身体健康与关系 历史 数据科学 金融与经济 体育 购物与商业意图 预期归因差距 注：条形图显示每个查询分类的预期引用差距（日志中访问的相关网站减去法学硕士输出中引用的网站）。

### 段落 105 · Page 25

**EN**

Classification labels are ordered by gap magnitude within each panel. See Table 2 above for method. 23

**中文**

分类标签按每个面板内的间隙大小排序。方法见上表2。 23

### Page 26

### 段落 106 · Page 26

**EN**

T able 3. Count Model Coefficients (No Interactions) Term Estimate Std.

**中文**

表 3. 计数模型系数（无交互作用）项估计标准。

### 段落 107 · Page 26

**EN**

Error z value p-value (Intercept) 2.163 0.078 27.66 0.000 modelfamilyGPT -1.099 0.156 -7.05 0.000 modelfamilySonar 0.207 0.054 3.81 0.000 classificationCurrent Affairs & Factual Information -0.021 0.053 -0.39 0.695 classificationData Science 0.057 0.064 0.89 0.371 classificationEducation -0.115 0.091 -1.26 0.209 classificationFinance & Economics 0.034 0.068 0.50 0.615 classificationGames, Fantasy & Creative Writing -0.053 0.074 -0.72 0.473 classificationHistory -0.008 0.087 -0.09 0.929 classificationLifestyle -0.028 0.064 -0.43 0.665 classificationMental & Physical Health & Relationships 0.050 0.077 0.66 0.512 classificationOther -0.093 0.065

**中文**

误差 z 值 p 值（截距） 2.163 0.078 27.66 0.000 modelfamilyGPT -1.099 0.156 -7.05 0.000 modelfamilySonar 0.207 0.054 3.81 0.000 分类时事和事实信息 -0.021 0.053 -0.39 0.695 分类数据科学 0.057 0.064 0.89 0.371 分类教育 -0.115 0.091 -1.26 0.209 分类财经 0.034 0.068 0.50 0.615 分类游戏、奇幻与创意写作 -0.053 0.074 -0.72 0.473 分类历史 -0.008 0.087 -0.09 0.929 分类生活方式 -0.028 0.064 -0.43 0.665 分类身心健康与人际关系 0.050 0.077 0.66 0.512 分类其他 -0.093 0.065

### 段落 108 · Page 26

**EN**

-1.43 0.154 classificationShopping & Commercial Intent 0.021 0.061 0.35 0.727 classificationSports -0.033 0.091 -0.37 0.712 search results count 0.125 0.003 39.74 0.000 log(response length) -0.171 0.008 -20.24 0.000 log(θ) 1.740 0.031 55.39 0.000 Note: Gemini as baseline model.

**中文**

-1.43 0.154 分类购物和商业意图 0.021 0.061 0.35 0.727 分类体育 -0.033 0.091 -0.37 0.712 搜索结果计数 0.125 0.003 39.74 0.000 log(响应长度) -0.171 0.008 -20.24 0.000 log(θ) 1.740 0.031 55.39 0.000 注：Gemini 作为基线模型。

### 段落 109 · Page 26

**EN**

Showing coefficients (main effects) from the count component of the negative binomial hurdle model. T able 4. Hurdle Model Coefficients (No Interactions) Term Estimate Std.

**中文**

显示负二项式障碍模型计数分量的系数（主效应）。表 4. 跨栏模型系数（无交互作用）项估计标准。

### 段落 110 · Page 26

**EN**

Error z value p-value (Intercept) -0.729 0.207 -3.52 0.000 modelfamilyGPT -3.140 0.069 -45.66 0.000 modelfamilySonar 1.601 0.061 26.28 0.000 classificationCurrent Affairs & Factual Information 0.195 0.096 2.03 0.043 classificationData Science 0.268 0.117 2.29 0.022 classificationEducation -0.245 0.144 -1.69 0.090 classificationFinance & Economics 0.341 0.121 2.83 0.005 classificationGames, Fantasy & Creative Writing -0.265 0.108 -2.45 0.014 classificationHistory 0.398 0.169 2.36 0.018 classificationLifestyle 0.177 0.111 1.59 0.113 classificationMental & Physical Health & Relationships 0.189 0.144 1.31 0.190 classificationOther -0.529 0.098 -5

**中文**

误差 z 值 p 值（截距） -0.729 0.207 -3.52 0.000 modelfamilyGPT -3.140 0.069 -45.66 0.000 modelfamilySonar 1.601 0.061 26.28 0.000 分类时事与事实信息 0.195 0.096 2.03 0.043 分类数据科学 0.268 0.117 2.29 0.022 分类教育 -0.245 0.144 -1.69 0.090 分类财经 0.341 0.121 2.83 0.005 分类游戏、奇幻与创意写作 -0.265 0.108 -2.45 0.014 分类历史 0.398 0.169 2.36 0.018 分类生活方式 0.177 0.111 1.59 0.113 分类身心健康与人际关系 0.189 0.144 1.31 0.190 分类其他 -0.529 0.098 -5

### 段落 111 · Page 26

**EN**

.39 0.000 classificationShopping & Commercial Intent 0.567 0.115 4.93 0.000 classificationSports 0.577 0.151 3.81 0.000 log(response length) 0.165 0.024 6.92 0.000 Note: Gemini as baseline model.

**中文**

.39 0.000 分类购物和商业意图 0.567 0.115 4.93 0.000 分类体育 0.577 0.151 3.81 0.000 log（响应长度） 0.165 0.024 6.92 0.000 注：Gemini 作为基线模型。

### 段落 112 · Page 26

**EN**

Showing coefficients (main effects) from the hurdle component of the negative binomial hurdle model. 24

**中文**

显示负二项式障碍模型的障碍成分的系数（主效应）。 24

### Page 27

### 段落 113 · Page 27

**EN**

T able 5. Expected Citation Gaps by Model Family and Topic Classification GPT-4o Gemini Sonar Classification Est. 95% CI Est. 95% CI Est.

**中文**

表 5. 按模型系列和主题分类划分的预期引用差距 GPT-4o Gemini 声纳分类预估。 95% CI 估计值95% CI 估计值

### 段落 114 · Page 27

**EN**

95% CI Computer Science & Software Engineering0.17 (0.14–0.22) 2.89 (2.63–3.14) 3.72 (3.55–3.89) Current Affairs & Factual Information 0.18 (0.15–0.23) 3.03 (2.78–3.29) 3.12 (3.00–3.26) Data Science 0.21 (0.16–0.27) 3.33 (2.97–3.73) 3.52 (3.34–3.74) Education 0.12 (0.08–0.19) 2.37 (1.97–2.78) 3.88 (3.57–4.19) Finance & Economics 0.23 (0.18–0.29) 3.34 (2.95–3.73) 3.52 (3.34–3.72) Games, Fantasy & Creative Writing 0.15 (0.11–0.21) 2.48 (2.18–2.82) 3.73 (3.54–3.92) History 0.19 (0.13–0.30) 3.27 (2.77–3.80) 3.76 (3.45–4.10) Lifestyle 0.23 (0.17–0.31) 3.00 (2.69–3.34) 3.36 (3.19–3.54) Mental & Physical Health & Relationships0.23 (0.17–0.32) 3.23 (

**中文**

95% CI 计算机科学与软件工程0.17 (0.14–0.22) 2.89 (2.63–3.14) 3.72 (3.55–3.89) 时事与事实信息 0.18 (0.15–0.23) 3.03 (2.78–3.29) 3.12 (3.00–3.26) 数据科学0.21 (0.16–0.27) 3.33 (2.97–3.73) 3.52 (3.34–3.74) 教育 0.12 (0.08–0.19) 2.37 (1.97–2.78) 3.88 (3.57–4.19) 财经 0.23 (0.18–0.29) 3.34 (2.95–3.73) 3.52 (3.34–3.72) 游戏、奇幻与创意写作 0.15 (0.11–0.21) 2.48 (2.18–2.82) 3.73 (3.54–3.92) 历史 0.19 (0.13–0.30) 3.27 (2.77–3.80) 3.76 (3.45–4.10) 生活方式 0.23 (0.17–0.31) 3.00 (2.69–3.34) 3.36 (3.19–3.54) 身心健康与关系0.23 (0.17–0.32) 3.23 (

### 段落 115 · Page 27

**EN**

2.76–3.73) 3.39 (3.17–3.63) Other 0.11 (0.09–0.15) 2.11 (1.88–2.39) 3.29 (3.13–3.47) Shopping & Commercial Intent 0.35 (0.27–0.45) 3.51 (3.16–3.85) 3.66 (3.48–3.86) Sports 0.27 (0.19–0.38) 3.35 (2.85–3.95) 3.82 (3.59–4.07) Note: Total expected attribution gap from negative binomial hurdle model.

**中文**

2.76–3.73) 3.39 (3.17–3.63) 其他 0.11 (0.09–0.15) 2.11 (1.88–2.39) 3.29 (3.13–3.47) 购物和商业意向 0.35 (0.27–0.45) 3.51 (3.16–3.85) 3.66 (3.48–3.86) 体育 0.27 (0.19–0.38) 3.35 (2.85–3.95) 3.82 (3.59–4.07) 注：负二项障碍模型的预期总归因差距。

### 段落 116 · Page 27

**EN**

Predictions are at the median query (5 search results and 2,089 characters). Confidence intervals from parametric bootstrap (n=1,000). Est. = Expected citation gaps per query. 8.3 Head-to-Head Regressions: Table of results T able 6.

**中文**

预测基于中值查询（5 个搜索结果和 2,089 个字符）。参数引导的置信区间 (n=1,000)。预计。 = 每个查询的预期引用差距。 8.3 头对头回归：结果表表 6。

### 段落 117 · Page 27

**EN**

Incremental citations per extra URL opened, by model variant Model variant Family n ˆβ1m SE p ppl-sonar-reasoning-pro-high Sonar 848 0.447 0.015 1.4e-138 ppl-sonar-reasoning Sonar 1635 0.445 0.012 4.3e-215 gemini-2.0-flash-grounding Gemini 1189 0.427 0.013 6.0e-172 api-gpt-4o-search-high-loc GPT 1222 0.426 0.010 6.1e-240 api-gpt-4o-search-high GPT 1695 0.389 0.010 1.3e-224 ppl-sonar Sonar 1200 0.339 0.012 1.8e-128 gemini-2.5-pro-grounding Gemini 1200 0.312 0.011 4.8e-130 api-gpt-4o-search GPT 1188 0.264 0.012 2.5e-89 api-gpt-4o-mini-search GPT 1158 0.251 0.012 1.1e-80 ppl-sonar-pro Sonar 1208 0.200 0.014 9.5e-46 ppl-sonar-pro-high Sonar 1359 0.191 0.012 9.9e-51 Note: n = pair-wise query comparisons involving the focal model.

**中文**

每个打开的额外 URL 的增量引用（按模型变体） 模型变体 Family n ˆβ1m SE p ppl-sonar-reasoning-pro-high Sonar 848 0.447 0.015 1.4e-138 ppl-sonar-reasoning Sonar 1635 0.445 0.012 4.3e-215 gemini-2.0-flash-grounding Gemini 1189 0.427 0.013 6.0e-172 api-gpt-4o-search-high-loc GPT 1222 0.426 0.010 6.1e-240 api-gpt-4o-search-high GPT 1695 0.389 0.010 1.3e-224 ppl-sonar 声纳1200 0.339 0.012 1.8e-128 gemini-2.5-亲接地 Gemini 1200 0.312 0.011 4.8e-130 api-gpt-4o-search GPT 1188 0.264 0.012 2.5e-89 api-gpt-4o-mini-search GPT 1158 0.251 0.012 1.1e-80 ppl-sonar-pro 声纳 1208 0.200 0.014 9.5e-46 ppl-sonar-pro-high 声纳 1359 0.191 0.012 9.9e-51 注：n = 涉及焦点模型的成对查询比较。

### 段落 118 · Page 27

**EN**

ˆβ1m is the coefficient on focal_search_diff, interpreted as the expected number of additional citations produced for each extra URL the focal model opens. 25

**中文**

^β1m 是 focus_search_diff 的系数，解释为焦点模型打开的每个额外 URL 产生的额外引用的预期数量。 25
