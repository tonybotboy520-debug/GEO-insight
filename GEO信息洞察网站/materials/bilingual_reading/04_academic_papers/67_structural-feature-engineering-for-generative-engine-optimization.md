# Structural Feature Engineering for Generative Engine Optimization

- ID: 67
- 类型: pdf
- 分类: 04_academic_papers
- 主题: content structure and citation probability
- 原文链接: https://arxiv.org/pdf/2603.29979
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

Structural Feature Engineering for Generative Engine Optimization: How Content Structure Shapes Citation Behavior 1st Junwei Yu The University of Tokyo Tokyo, Japan yujw@satolab.itc.u-tokyo.ac.jp 2nd Yang MuFeng University of Tsukuba Ibaraki, Japan s2321728@u.tsukuba.ac.jp 3rd Yepeng Ding Hiroshima University Hiroshima, Japan yepengd@acm.org 4th Hiroyuki Sato The University of Tokyo / National Institute of Informatics Tokyo, Japan schuko@nii.ac.jp Abstract—The proliferation of AI-powered search engines has shifted information discovery from link-based results to direct answer generation with selective source citation, creating urgent demand for Generative Engine Optimization (GEO) strategies.

**中文**

生成式引擎优化的结构特征工程：内容结构如何塑造引文行为 第一届 Junwei Yu 东京大学 日本东京 yujw@satolab.itc.u-tokyo.ac.jp 第二届 杨木峰 筑波大学茨城县，日本 s2321728@u.tsukuba.ac.jp 第三届 Yepeng Ding 广岛大学 日本广岛yepengd@acm.org 第四届 Hiroyuki Sato 东京大学/国家信息研究所 日本东京 schuko@nii.ac.jp 摘要：人工智能驱动的搜索引擎的激增已将信息发现从基于链接的结果转变为通过选择性源引用直接生成答案，从而对生成式引擎优化 (GEO) 策略产生了迫切需求。

### 段落 2 · Page 1

**EN**

While existing GEO research focuses on semantic content modification, the systematic influence of structural features on citation behavior remains unexplored, leaving content creators without scientific guidance for structural optimization. We introduce GEO-SFE (Structural Feature Engineering for Generative Engine Optimization), a framework that quantifies how content structure, independent of semantic content, affects citation performance. Our methodology decomposes structure into three hierarchical levels: macro-structure (document architecture), meso-structure (information chunking), and micro-structure (visual emphasis).

**中文**

虽然现有的GEO研究侧重于语义内容修改，但结构特征对引用行为的系统影响仍未被探索，导致内容创作者缺乏结构优化的科学指导。我们介绍 GEO-SFE（生成式引擎优化的结构特征工程），这是一个框架，可以量化独立于语义内容的内容结构如何影响引文性能。我们的方法将结构分解为三个层次级别：宏观结构（文档架构）、中观结构（信息分块）和微观结构（视觉重点）。

### 段落 3 · Page 1

**EN**

We develop architecture-agnostic optimization algorithms with semantic preservation constraints and establish predictive models for citation outcomes. Evaluation across six generative engines demonstrates consistent 17.3% citation improvements, with subjective assessments revealing 18.5% average enhancement in perceptual quality. This work establishes the first systematic, data-driven methodology for structural GEO, transforming content optimization from intuition-based practices to engineering principles. Index Terms—Large Language Model, Generative Engine Optimization, Content Structure, Feature Engineering, Human-AI Interaction I.

**中文**

我们开发具有语义保留约束的与架构无关的优化算法，并建立引文结果的预测模型。对六个生成式引擎的评估显示，引文持续提高了 17.3%，主观评估显示感知质量平均提高了 18.5%。这项工作为结构 GEO 建立了第一个系统的、数据驱动的方法，将内容优化从基于直觉的实践转变为工程原理。索引词——大语言模型、生成式引擎优化、内容结构、特征工程、人机交互 I.

### 段落 4 · Page 1

**EN**

INTRODUCTION The proliferation of LLM-powered generative engines has fundamentally transformed information discovery from traditional link-based search results to direct answer generation with selective source attribution [1], [2]. Unlike conventional search engines that present ranked lists of documents, generative engines such as ChatGPT, Google’s Search Generative Experience, and Perplexity.ai synthesize information from multiple sources to produce coherent responses while embedding citations within generated content [3].

**中文**

简介 LLM 支持的生成式引擎的激增从根本上将信息发现从传统的基于链接的搜索结果转变为通过选择性来源归因直接生成答案 [1], [2]。与提供文档排名列表的传统搜索引擎不同，ChatGPT、Google 的搜索生成体验和 Perplexity.ai 等生成式引擎综合来自多个来源的信息以产生连贯的响应，同时在生成的内容中嵌入引用 [3]。

### 段落 5 · Page 1

**EN**

This paradigm shift has created an urgent transformation in content visibility economics: the traditional ”clicks” model has evolved into a ”citations” economy where being referenced in LLM-generated responses becomes more valuable than website traffic [4]. While existing GEO research has demonstrated content modification strategies yielding up to 40% improvements in citation rates, current approaches primarily focus on semantic content alterations, such as adding statistics, quotations, and authoritative language, rather than systematic structural optimization [5].

**中文**

这种范式转变导致了内容可见性经济学的紧急转变：传统的“点击”模型已经演变成“引用”经济，其中法学硕士生成的回复中的引用变得比网站流量更有价值[4]。虽然现有的 GEO 研究已证明内容修改策略可将引用率提高高达 40%，但当前的方法主要侧重于语义内容更改，例如添加统计数据、引文和权威语言，而不是系统的结构优化 [5]。

### 段落 6 · Page 1

**EN**

However, the black-box nature of LLM citation decisions poses fundamental challenges for content creators seeking predictable optimization strategies. Unlike traditional SEO where ranking factors can be reverse-engineered through systematic experimentation, LLM systems employ complex multi-layer attention mechanisms across ensemble models, making citation behavior difficult to predict or control through conventional content modification approaches alone. The critical gap in existing GEO research lies in the systematic analysis of content structural features and their quantifiable impact on LLM citation performance.

**中文**

然而，LLM 引文决策的黑箱性质给寻求可预测优化策略的内容创建者带来了根本性挑战。与可以通过系统实验对排名因素进行逆向工程的传统 SEO 不同，LLM 系统在集成模型中采用复杂的多层注意力机制，使得引用行为难以仅通过传统的内容修改方法来预测或控制。现有 GEO 研究的关键差距在于对内容结构特征及其对 LLM 引用表现的可量化影响的系统分析。

### 段落 7 · Page 1

**EN**

Emerging evidence from LLM system research indicates that content structure, independent of semantic content, significantly influences large language model processing and output generation [6], [7]. Hierarchical information organization, visual emphasis patterns, and content chunking strategies have demonstrated measurable effects on LLM comprehension and response quality in controlled studies.

**中文**

LLM 系统研究的新证据表明，独立于语义内容的内容结构显着影响大型语言模型处理和输出生成 [6]、[7]。在对照研究中，分层信息组织、视觉强调模式和内容分块策略已证明对法学硕士理解和回答质量具有可衡量的影响。

### 段落 8 · Page 1

**EN**

Yet no systematic framework exists for quantifying how these structural features specifically influence citation behavior across different LLM platforms, leaving content creators without scientific guidance for structural optimization strategies that could complement existing semantic GEO approaches. We introduce GEO-SFE (Structural Feature Engineering for Generative Engine Optimization), the first systematic arXiv:2603.29979v1 [cs.CL] 31 Mar 2026

**中文**

然而，目前还没有系统框架来量化这些结构特征如何具体影响不同 LLM 平台上的引用行为，从而使内容创建者缺乏可以补充现有语义 GEO 方法的结构优化策略的科学指导。我们介绍 GEO-SFE（生成式引擎优化的结构特征工程），第一个系统化的 arXiv:2603.29979v1 [cs.CL] 2026 年 3 月 31 日

### Page 2

### 段落 9 · Page 2

**EN**

framework for quantifying and optimizing content structural features to enhance LLM citation performance. This work establishes the first engineering approach to GEO structural optimization, transforming content visibility strategies from intuition-based practices to data-driven methodologies with immediate practical applications for the growing community of content creators navigating LLM-powered information ecosystems. II. RELATED WORK A. Generative Engine Architecture Generative engines represent a distinct class of information retrieval systems that integrate large language models with real-time web search capabilities.

**中文**

用于量化和优化内容结构特征以提高 LLM 引用性能的框架。这项工作建立了第一个 GEO 结构优化的工程方法，将内容可见性策略从基于直觉的实践转变为数据驱动的方法，并为不断增长的内容创建者社区在 LLM 支持的信息生态系统中提供直接的实际应用。二.相关工作 A. 生成式引擎架构 生成式引擎代表了一类独特的信息检索系统，它将大型语言模型与实时网络搜索功能集成在一起。

### 段落 10 · Page 2

**EN**

Unlike traditional search engines that return ranked lists of documents, these systems synthesize information from multiple sources to generate comprehensive responses with inline citations. Modern generative engines employ diverse retrieval and generation strategies, each with distinct implications for content optimization. Table I categorizes the primary architectural approaches based on their query processing methods, retrieval pipelines, and citation mechanisms. Standard generative engines decompose complex queries into sub-queries, retrieve relevant documents, and synthesize multi-source responses with direct URL citations [8].

**中文**

与返回排序的文档列表的传统搜索引擎不同，这些系统综合来自多个来源的信息，以生成带有内联引用的综合响应。现代生成式引擎采用不同的检索和生成策略，每种策略对内容优化都有不同的影响。表 I 根据查询处理方法、检索管道和引用机制对主要架构方法进行了分类。标准生成式引擎将复杂查询分解为子查询，检索相关文档，并通过直接 URL 引用合成多源响应 [8]。

### 段落 11 · Page 2

**EN**

Web-enhanced RAG systems augment this process by incorporating fresh web content to ensure temporal relevance [9], while RAG-Fusion architectures generate multiple query variants and apply Reciprocal Rank Fusion (RRF) to combine results from parallel searches [10], [11]. B. Generative Engine Optimization Recent industry analysis reveals that organic click-through rates have declined from 28% to 19% for position-one results due to AI Overviews [18], while zero-click searches now comprise over 58% of all queries [19].

**中文**

Web 增强的 RAG 系统通过合并新鲜的 Web 内容来增强此过程，以确保时间相关性 [9]，而 RAG-Fusion 架构生成多个查询变体并应用倒数排名融合 (RRF) 来组合并行搜索的结果 [10]、[11]。 B. 生成式引擎优化 最近的行业分析表明，由于人工智能概述 [18]，第一名结果的自然点击率已从 28% 下降到 19%，而零点击搜索现在占所有查询的 58% 以上 [19]。

### 段落 12 · Page 2

**EN**

The transition from traditional Search Engine Optimization (SEO) to Generative Engine Optimization (GEO) represents a fundamental paradigm shift in content discovery and visibility strategies. The emergence of LLM-powered search engines has rendered many traditional SEO metrics irrelevant, as user behavior shifts from link-clicking to information consumption within LLM-generated summaries [20], [21]. Aggarwal et al.

**中文**

从传统搜索引擎优化 (SEO) 到生成式引擎优化 (GEO) 的转变代表了内容发现和可见性策略的根本范式转变。 LLM 支持的搜索引擎的出现使得许多传统的 SEO 指标变得无关紧要，因为用户行为从链接点击转变为 LLM 生成的摘要中的信息消费 [20]、[21]。阿加瓦尔等人。

### 段落 13 · Page 2

**EN**

[1] pioneered the GEO paradigm by introducing systematic methods for optimizing content visibility in generative engine responses, achieving up to 40% improvements in citation rates through semantic content modifications such as adding statistics, quotations, and authoritative language. This foundational work demonstrates domain-specific optimization requirements and establishes GEO-bench as the first comprehensive evaluation framework for generative engine optimization.

**中文**

[1] 开创了 GEO 范式，引入了优化生成式引擎响应中内容可见性的系统方法，通过添加统计数据、引文和权威语言等语义内容修改，将引用率提高了 40%。这项基础工作展示了特定领域的优化要求，并将 GEO-bench 确立为第一个生成式发动机优化的综合评估框架。

### 段落 14 · Page 2

**EN**

However, current GEO research focuses primarily on semantic content alterations while treating the generative engine itself as a black box, with little attention to its underlying architecture. This limited perspective weakens the consideration of structural features and contributes to poor generalization across different contexts. C. Structured Text and LLM Processing Content structure significantly influences how large language models process and prioritize information, with direct implications for generative engine optimization. Liu et al.

**中文**

然而，当前的GEO研究主要集中在语义内容的改变上，而将生成式引擎本身视为黑匣子，很少关注其底层架构。这种有限的视角削弱了对结构特征的考虑，并导致不同背景下的概括性较差。 C. 结构化文本和法学硕士处理内容结构显着影响大型语言模型处理信息和确定信息优先级的方式，对生成式引擎优化有直接影响。刘等人。

### 段落 15 · Page 2

**EN**

[22] demonstrate through systematic analysis of multimodal language models that structured text induces focused attention patterns on semantically meaningful regions, while unstructured OCR text causes attention dispersion and performance degradation. This establishes a causal link between structural organization and LLM processing efficiency. LLMs employ specialized attention mechanisms to parse structured content at multiple levels. Yang et al. [23] reveals that Transformer models allocate distinct attention heads for different structural elements: syntactic relationships, semantic associations, and discourse structure.

**中文**

[22]通过对多模态语言模型的系统分析证明，结构化文本会引起对语义有意义区域的集中注意力模式，而非结构化 OCR 文本会导致注意力分散和性能下降。这在结构组织和法学硕士处理效率之间建立了因果关系。法学硕士采用专门的注意力机制来解析多个级别的结构化内容。杨等人。 [23]揭示了 Transformer 模型为不同的结构元素分配不同的注意力头：句法关系、语义关联和话语结构。

### 段落 16 · Page 2

**EN**

This attention head specialization [24], [25] enables targeted structural optimization, as specific hierarchical patterns can activate attention mechanisms that enhance content retrieval and citation in generative responses. Despite these capabilities, LLMs exhibit architectural constraints in processing complex structures. Guan et al. [26]. Performance also depends critically on information positioning, peaking when relevant content appears at sequence boundaries rather than middle positions [27].

**中文**

这种注意力头专业化[24]、[25]能够实现有针对性的结构优化，因为特定的层次模式可以激活注意力机制，从而增强生成响应中的内容检索和引用。尽管有这些能力，法学硕士在处理复杂结构时仍表现出架构限制。关等人。 [26]。性能还关键取决于信息定位，当相关内容出现在序列边界而不是中间位置时达到峰值[27]。

### 段落 17 · Page 2

**EN**

For practical implementation, Google recommends JSON-LD structured data with emphasis on FAQ and How-to schemas for AI search visibility [28], [29]. These findings indicate that while structural optimization can enhance LLM performance, its effectiveness within generative engine architectures remains an open research question. III. PRELIMINARIES A. Generative Engine Formulation We formalize a Generative Engine (GE) as a function that takes a user query and returns a natural language response with source attributions: fGE : (qu, PU)→r whereq u represents the user query,P U denotes personalized user information, andris the generated response.

**中文**

对于实际实施，Google 建议使用 JSON-LD 结构化数据，重点关注常见问题解答和 AI 搜索可见性的操作模式 [28]、[29]。这些发现表明，虽然结构优化可以提高法学硕士的性能，但其在生成式引擎架构中的有效性仍然是一个悬而未决的研究问题。三．准备工作 A. 生成式引擎公式 我们将生成式引擎 (GE) 形式化为一个函数，它接受用户查询并返回带有源属性的自然语言响应： fGE : (qu, PU)→r 其中 q u 表示用户查询，P U 表示个性化用户信息，ris 表示生成的响应。

### 段落 18 · Page 2

**EN**

A generative engine comprises two primary components: (1) a set of generative modelsG={G 1, G2, . . . , Gn}where eachG i serves specific functions (query reformulation, summarization, response generation), and (2) a search engineSEthat retrieves a ranked set of sourcesS={s 1, s2, . . . , sm}for a given query or sub-query. The generated responserconsists of sentences {l1, l2, . . . , lo}where each sentencel i may be supported by a citation setC i ⊆ S. The visibility (or impression) of source si in responseris quantified by the function: Vis(si, r) =f(coverage,position,influence)

**中文**

生成式引擎包含两个主要组件：（1）一组生成模型G={G 1, G2,…。。。 , Gn}其中每个G i 服务于特定功能（查询重构、摘要、响应生成），以及（2）搜索引擎SE，检索一组排序的源S={s 1, s2,...。。。 , sm}对于给定的查询或子查询。生成的响应由句子 {l1, l2, .。。 , lo}其中每个句子 i 都可以由引用集 C i ⊆ S 支持。响应中源 si 的可见性（或印象）由以下函数量化：Vis(si, r) =f(覆盖率,位置,影响力)

### Page 3

### 段落 19 · Page 3

**EN**

TABLE I COREGENERATIVEENGINEARCHITECTURES FORWEBSEARCH Architecture Type Query Processing Retrieval & Generation Pipeline Citation Mechanism GEO Target Focus Standard Generative Engine [8] Query decomposition into sub-queries{q 1...qn} Search engine retrieval→Document summarization→Multi-source synthesis Direct URL citations in response Semantic clarity, structured data Web-Enhanced RAG [9] Direct query to web search Web content retrieval→Context augmentation→Response generation Appended source list Freshness, E-E-A-T signals RAG-Fusion [10], [11] LLM generates query variants Parallel searches→RRF score fusion →Reranked document list Multi-so

**中文**

表 I Web 搜索的核心生成式引擎架构 架构类型 查询处理 检索和生成管道 引文机制 GEO 目标焦点 标准生成式引擎 [8] 查询分解为子查询{q 1...qn} 搜索引擎检索→文档摘要→多源合成 响应中直接 URL 引用 语义清晰、结构化数据 Web 增强 RAG [9] 直接查询 Web 搜索 Web 内容检索→上下文增强→响应生成 附加源列表 新鲜度，E-E-A-T 信号 RAG-Fusion [10]，[11] LLM 生成查询变体 并行搜索→RRF 分数融合→重新排序文档列表 Multi-so

### 段落 20 · Page 3

**EN**

urce attribution Query diversity coverage Hybrid Search [12] Parallel keyword + vector processing Dual retrieval paths→RRF fusion→ Unified ranking Combined lexical-semantic sources Keyword-semantic balance Query Rewriting [13] SLM-driven query optimization Rewritten queries→Web API calls →Semantic reranking Relevance-ordered citations Query intent alignment Multi-Hop Retrieval [14] Recursive query decomposition Initial search→Query refinement→ Iterative retrieval Hierarchical source layers Complex reasoning paths Graph-Web Hybrid [14] Entity recognition + graph traversal Knowledge graph + Web search parallel→Cross-validation Differentiated KG

**中文**

资源归因 查询多样性覆盖 混合搜索 [12] 并行关键词+向量处理 双检索路径→RRF融合→统一排序 词义结合源 关键词语义平衡 查询重写 [13] SLM驱动的查询优化 重写查询→Web API调用→语义重排序 相关性排序引文 查询意图对齐 多跳检索 [14] 递归查询分解 初始搜索→查询细化→迭代检索分层源层复杂推理路径图-Web混合[14]实体识别+图遍历知识图+Web搜索并行→交叉验证差异化知识图谱

### 段落 21 · Page 3

**EN**

/web sources Factual consistency Real-Time Web [15] Time-sensitive query detection Live crawling→Freshness scoring→ Latest content selection Timestamped citations Temporal relevance HyDE Web [16] Hypothetical answer generation Answer-as-query→Similarity search →Verification retrieval Authority-matched sources Answer-document alignment Vertical Domain [17] Domain classification first Targeted authoritative site search→ Terminology normalization Domain-specific (.edu, .gov) priority Expertise demonstration The interaction between the generative modelsGand the search engineSEdefines the system’s architecture.

**中文**

/web 来源 事实一致性 实时 Web [15] 时间敏感查询检测 实时抓取→新鲜度评分→最新内容选择 时间戳引用 时间相关性 HyDE Web [16] 假设答案生成 回答即查询→相似性搜索→验证检索 权威匹配源 答案文档对齐 垂直领域 [17] 领域分类优先 有针对性的权威站点搜索→术语规范化 特定领域（.edu、.gov）优先级 专业知识演示生成模型G和搜索引擎SE之间的交互定义了系统的架构。

### 段落 22 · Page 3

**EN**

Prior work can be broadly categorized into three core architectural paradigms based on the retrieval-generation interaction frequency and timing. The three architectural types are defined by their operational flow:Search-then-Synthesizerepresents the one-shot, non-interactive paradigm;Iterative Refinement introduces multi-round feedback loops to improve evidence gathering; andIntegrated Search-Generationallows for dynamic, concurrent retrieval during the response streaming process. As we will demonstrate, these distinct flows necessitate fundamentally different strategies for GEO. B.

**中文**

先前的工作可以根据检索生成交互频率和时间大致分为三个核心架构范例。这三种架构类型由其操作流程定义：搜索然后综合代表一次性、非交互式范式；迭代细化引入多轮反馈循环以改进证据收集；集成搜索生成允许在响应流处理过程中进行动态、并发检索。正如我们将证明的那样，这些不同的流动需要 GEO 采取根本不同的策略。 B.

### 段落 23 · Page 3

**EN**

Content Structure Representation We model content structure through a three-tier hierarchical decomposition: Macro-structureM: Document-level architecture M={H, N, F} whereHrepresents the heading hierarchy,Ndenotes navigational elements, andFcaptures the overall document flow. Meso-structureE: Section-level organization E={P, L, T} wherePrepresents paragraph organization (a set of words), Ldenotes list structures, andTcaptures table formatting. Micro-structureµ: Sentence-level features µ={E, K, S} whereErepresents emphasis markers,Kdenotes keyword placement, andScaptures syntactic patterns.

**中文**

内容结构表示 我们通过三层分层分解对内容结构进行建模： 宏观结构M：文档级架构 M={H, N, F} 其中 H 表示标题层次结构，N 表示导航元素，F 捕获整个文档流。 Meso-structE：节级组织 E={P, L, T} 其中表示段落组织（一组单词），L 表示列表结构，T 捕获表格格式。微观结构μ：句子级特征μ={E，K，S}，其中E表示强调标记，K表示关键字位置，Scaptures句法模式。

### 段落 24 · Page 3

**EN**

The complete structural feature vector for contentcis: SF(c) = [ϕM(M), ϕE(E), ϕµ(µ)](1) whereϕ M,ϕ E, andϕ µ are feature extraction functions that map structural elements to numerical representations. C. Structural Feature Engineering Objective Given contentcwith structural featuresSF(c), our optimization objective is to find the optimal structural configurationSF ∗ that maximizes citation probability across a set of queriesQ: SF∗ = arg max SF X q∈Q P(cite(c)|q,SF) whereP(cite(c)|q,SF)represents the probability that content cwith structural featuresSFwill be cited in the generative engine’s response to queryq. D.

**中文**

contentcis 的完整结构特征向量： SF(c) = [ΦM(M), ΦE(E), Φμ(μ)](1) 其中 Φ M、Φ E 和 Φ µ 是将结构元素映射到数值表示的特征提取函数。 C. 结构特征工程目标 给定带有结构特征的内容 cSF(c)，我们的优化目标是找到最优的结构配置 SF *，它可以最大化一组查询 Q 的引用概率： SF* = arg max SF X q∈Q P(cite(c)|q,SF) 其中 P(cite(c)|q,SF) 表示带有结构特征 SF 的内容 c 在生成式引擎对查询 q 的响应中被引用的概率。 D .

### 段落 25 · Page 3

**EN**

Problem Statement Structural Feature Engineering for GEO: Given a content corpusCand query distributionQ, learn a structural transformation functionT:C → C ′ such that the transformed contentC ′ ={T(c)|c∈ C}achieves maximal visibility across generative engines while preserving semantic integrity: T ∗ = arg maxT P c∈C P q∈QVis(T(c), fGE(q))s.t. Sem(T(c)) =Sem(c) (2) where Sem(·)ensures semantic equivalence between original and transformed content.

**中文**

GEO 的问题陈述结构特征工程：给定一个内容语料库和查询分布 Q，学习一个结构转换函数 T:C → C ′，使得转换后的内容 C ′ ={T(c)|c∈C} 在保持语义完整性的同时在生成式引擎中实现最大可见性：T ∗ = arg maxT P c∈C P q∈QVis(T(c), fGE(q))s.t。 Sem(T(c)) =Sem(c) (2) 其中 Sem(·) 确保原始内容和转换内容之间的语义等效性。

### Page 4

### 段落 26 · Page 4

**EN**

This mathematical framework provides the foundation for our systematic approach to structural feature engineering in generative engine optimization. The optimization objective defined in Equation 2 necessitates a comprehensive evaluation methodology to quantify citation performance improvements across structural modifications. Figure 1 demonstrates the empirical assessment framework that operationalizes the visibility function Vis(T(c), f GE(q)), illustrating how structural feature engineering translates into measurable citation performance gains through systematic evaluation of coverage, position, and influence metrics. Fig.

**中文**

这个数学框架为我们在生成式引擎优化中进行结构特征工程的系统方法奠定了基础。公式 2 中定义的优化目标需要一种全面的评估方法来量化跨结构修改的引文性能改进。图 1 展示了可操作可见性函数 Vis(T(c), f GE(q)) 的实证评估框架，说明结构特征工程如何通过覆盖率、位置和影响力指标的系统评估转化为可测量的引文绩效收益。图。

### 段落 27 · Page 4

**EN**

1.The workflow of Structural Feature Engineering Citation Performance Assessment.The workflow demonstrates the quantitative evaluation methodology for measuring optimization effectiveness, showing how the theoretical visibility function decomposes into empirically measurable components (coverage, position, influence) and their integration into final citation performance metrics. IV.

**中文**

1.结构特征工程引文绩效评估的工作流程。该工作流程演示了衡量优化有效性的定量评估方法，展示了理论可见性函数如何分解为经验可测量的组成部分（覆盖率、位置、影响力）以及它们如何集成到最终的引文绩效指标中。四．

### 段落 28 · Page 4

**EN**

STRUCTURALFEATUREENGINEERING FORGEO To address the challenge of optimizing content visibility in generative engines, we propose GEO-SFE (Structural Feature Engineering for Generative Engine Optimization), a systematic framework that quantifies and optimizes content structural features to enhance citation performance across diverse LLM-powered search architectures.

**中文**

结构特征工程 FORGEO 为了应对优化生成式引擎中内容可见性的挑战，我们提出了 GEO-SFE（生成式引擎优化的结构特征工程），这是一个系统框架，可以量化和优化内容结构特征，以增强跨法学硕士支持的各种搜索架构的引文性能。

### 段落 29 · Page 4

**EN**

Our methodology decomposes structural optimization into three hierarchical levels, macro-structure (document architecture), meso-structure (information chunking and formatting), and micro-structure (visual emphasis patterns), and develops architecture-specific optimization strategies aligned with the three core generative engine paradigms: Search-then-Synthesize, Iterative Search-Refinement, and Integrated Search-Generation. The procedural diagram in Figure 2 illustrates how GEO-SFE transforms content optimization from intuition-based practices to data-driven engineering principles.

**中文**

我们的方法将结构优化分解为三个层次，即宏观结构（文档架构）、中观结构（信息分块和格式化）和微观结构（视觉强调模式），并开发与三个核心生成式引擎范式一致的特定于架构的优化策略：搜索然后综合、迭代搜索细化和集成搜索生成。图 2 中的程序图说明了 GEO-SFE 如何将内容优化从基于直觉的实践转变为数据驱动的工程原理。

### 段落 30 · Page 4

**EN**

Unlike traditional SEO, which balances semantic content with technical and link-based factors, and unlike existing GEO approaches that focus primarily on semantic content modification, our framework treats structural organization as a first-class optimization target. This enables systematic engineering of content presentation to leverage architecture-specific attention mechanisms and citation preferences while maintaining computational tractability for large-scale optimization. A.

**中文**

与平衡语义内容与技术和基于链接的因素的传统 SEO 不同，也不同于主要关注语义内容修改的现有 GEO 方法，我们的框架将结构组织视为一流的优化目标。这使得内容呈现的系统工程能够利用特定于架构的注意力机制和引用偏好，同时保持大规模优化的计算易处理性。 A.

### 段落 31 · Page 4

**EN**

Hierarchical Structural Feature Decomposition We model content structure through three hierarchical levels, each capturing distinct aspects of document organization that influence LLM processing and citation behavior. Macro-Structure Features.Macro-structure encompasses document-level architectural elements that establish overall information hierarchy and navigation patterns, directly influencing how generative engines parse and comprehend global document organization. We quantify heading hierarchy through depth metrics dh = max(heading levels)and balance measuresb h = sections at leveli total sections .

**中文**

层次结构特征分解 我们通过三个层次级别对内容结构进行建模，每个层次捕获影响 LLM 处理和引用行为的文档组织的不同方面。宏观结构特征。宏观结构包含建立整体信息层次结构和导航模式的文档级架构元素，直接影响生成式引擎如何解析和理解全局文档组织。我们通过深度度量 dh = max(标题级别) 和平衡度量 b h = 级别上的节数 i 总节数来量化标题层次结构。

### 段落 32 · Page 4

**EN**

Navigation consistency is measured via structural regularity:R= 1− σ(section lengths) µ(section lengths) where higher values indicate more consistent organization. Logical progression is quantified through transition coherence metrics that measure semantic continuity between sections:T c = 1 n−1 Pn−1 i=1 sim(si, si+1)where sim(·) computes semantic similarity between adjacent sections. Internal linking densityL d = internal links total content units and reference distributionR d capture how well content supports exploratory reading and contextual understanding—factors crucial for LLM web search systems performing multi-step reasoning.

**中文**

导航一致性是通过结构规律性来衡量的：R= 1− σ(节长度) µ(节长度)，其中值越高表示组织越一致。逻辑级数通过测量部分之间语义连续性的转换连贯性度量来量化：T c = 1 n−1 Pn−1 i=1 sim(si, si+1) 其中 sim(·) 计算相邻部分之间的语义相似性。内部链接密度L d = 内部链接总内容单元和参考分布R d 捕获内容支持探索性阅读和上下文理解的程度——对于执行多步推理的LLM网络搜索系统至关重要的因素。

### 段落 33 · Page 4

**EN**

Meso-Structure Features.Meso-structure addresses section-level organization patterns that affect information chunking and format diversity-key factors in optimizing content for LLM synthesis processes. Paragraph organization is quantified through length variance Vp = σ(plengths) µ(plengths) and topic coherence within chunks. Optimal chunking balances information density with cognitive load, measured via entropy:H c =− P pi logp i wherep i represents topic probability within chunks. We measure structural variety through format type distribution:F d = distinct formats total content units .

**中文**

细观结构特征。细观结构解决了影响信息分块和格式多样性的部分级组织模式，这是优化法学硕士综合过程内容的关键因素。段落组织通过长度方差 Vp = σ(plengths) µ(plengths) 和块内的主题连贯性来量化。最佳分块平衡信息密度与认知负荷，通过熵测量：H c =− P pi logp i 其中p i 表示块内的主题概率。我们通过格式类型分布来衡量结构多样性：F d = 不同格式总内容单位。

### 段落 34 · Page 4

**EN**

Lists, tables, and structured elements receive special weighting as they demonstrate superior LLM parsing performance. Format transition smoothnessF s captures how naturally different presentation styles integrate within content flow. Content density metricsD= information units total tokens and distribution patterns affect LLM attention allocation. Uniform density promotes consistent engagement, while strategic density variation can guide attention to critical information. Micro-Structure Features.Micro-structure targets sentence-level and sub-sentence features that influence immediate LLM attention and comprehension processes.

**中文**

列表、表格和结构化元素具有特殊的权重，因为它们展示了卓越的 LLM 解析性能。格式转换平滑度F s 捕捉不同的呈现样式在内容流中如何自然地整合。内容密度指标D=信息单元总代币和分布模式影响LLM注意力分配。均匀的密度促进一致的参与，而战略密度的变化可以引导对关键信息的关注。微观结构特征。微观结构针对影响法学硕士即时注意力和理解过程的句子级和子句特征。

### 段落 35 · Page 4

**EN**

Emphasis marker distributionE d and strategic placement Ep quantify how visual cues guide attention. Visual marker placement is quantified through: Ed = emphasized tokens total tokens , E p = NX i=1 wi ·e i (3)

**中文**

重点标记分布E d 和策略布局Ep 量化视觉线索如何引导注意力。视觉标记放置通过以下方式量化： Ed = 强调标记 总标记 , E p = NX i=1 wi ·e i (3)

### Page 5

### 段落 36 · Page 5

**EN**

Fig. 2.GEO-SFE Framework Architecture.GEO-SFE Framework Architecture Shows the three-tier hierarchical structure with Macro, Meso, and Micro levels, connected to feature extraction, optimization, and validation components.

**中文**

图 2.GEO-SFE 框架架构。GEO-SFE 框架架构显示了具有宏观、中观和微观级别的三层层次结构，连接到特征提取、优化和验证组件。

### 段落 37 · Page 5

**EN**

The framework follows a four-stage pipeline: (1)Feature Extraction analyzes existing content to quantify structural characteristics across all hierarchical levels, (2)Structural Analysisidentifies optimization opportunities through cross-platform citation pattern analysis, (3)Optimizationapplies algorithmic transformations to enhance structural features while preserving semantic integrity, and (4)Validationmeasures citation performance improvements across target generative engines. wheree i ∈ {0,1}indicates emphasis presence andw i represents position-dependent weights. Empirical hierarchy followsW bold > Witalic > Wunderline.

**中文**

该框架遵循四阶段流程：(1) 特征提取分析现有内容以量化所有层次结构的结构特征，(2) 结构分析通过跨平台引用模式分析识别优化机会，(3) 优化应用算法转换以增强结构特征，同时保持语义完整性，(4) 验证衡量跨目标生成式引擎的引用性能改进。其中 i ∈ {0,1} 表示强调存在，w i 表示位置相关的权重。经验层次结构如下：W 粗体 > Witalic > Wunderline。

### 段落 38 · Page 5

**EN**

Strategic keyword placement within attention-sensitive positions (sentence beginnings, emphasized text, structural boundaries) is measured through position-weighted keyword density: Kp = X i wi ·k i, w i =    2.0sentence initial 1.5section boundary 1.0standard position (4) wherek i indicates keyword presence at positioni. Parse tree depth variance and dependency patterns affect parsing efficiency. Reading ease metricsR e ensure optimization maintains human comprehension. B. Structural Feature Extraction Algorithm We proposed algorithm 1 for extracting and quantifying structural features across all hierarchical levels.

**中文**

注意力敏感位置（句子开头、强调文本、结构边界）内的战略关键词放置是通过位置加权关键词密度来衡量的： Kp = X i wi ·ki, w i =    2.0 句首 1.5 节边界 1.0 标准位置 (4) 其中 k i 表示位置 i 处的关键词存在。解析树深度方差和依赖模式影响解析效率。阅读轻松度指标确保优化保持人类理解力。 B. 结构特征提取算法 我们提出了算法 1，用于跨所有层次提取和量化结构特征。

### 段落 39 · Page 5

**EN**

The extraction process employs both rule-based and learning-based approaches to ensure comprehensive feature coverage. Feature normalization ensures comparable metrics across documents of varying lengths and domains.

**中文**

提取过程采用基于规则和基于学习的方法来确保全面的特征覆盖。特征标准化可确保不同长度和域的文档之间具有可比较的指标。

### 段落 40 · Page 5

**EN**

We employ z-score Algorithm 1Hierarchical Feature Extraction 1:Input: Content documentC 2:Output: Structural feature vectorSF(C) 3:Parse document structure using DOM/markup analysis 4:Extract macro-features: 5:→Compute heading hierarchy:d h, bh, R 6:→Analyze logical progression:T c 7:→Measure cross-reference patterns:L d, Rd 8:Extract meso-features: 9:→Quantify paragraph organization:V p, Hc 10:→Assess format diversity:F d, Fs 11:→Calculate information density:D 12:Extract micro-features: 13:→Identify emphasis patterns:E d, Ep 14:→Locate keyword positions:K p 15:→Analyze syntactic structures:R e 16:Normalize features:SF norm ←z-score(SF raw) 17:ReturnSF(C) = [M norm,E norm,µ norm] normalization for continuous features and frequency-based normalization for categorical structural elements.

**中文**

我们采用 z 分数算法 1 分层特征提取 1：输入：内容文档 C 2：输出：结构特征向量 SF(C) 3：使用 DOM/标记分析解析文档结构 4：提取宏特征： 5：→计算标题层次结构：d h、bh、R 6：→分析逻辑级数：T c 7：→测量交叉引用模式：L d、Rd 8：提取中观特征: 9:→量化段落组织:V p, Hc 10:→评估格式多样性:F d, Fs 11:→计算信息密度:D 12:提取微观特征: 13:→识别强调模式:E d, Ep 14:→定位关键词位置:K p 15:→分析句法结构:R e 16:标准化特征:SF 范数←z-score(SF raw) 17:ReturnSF(C) = [M 范数,E 范数,μ 范数] 连续特征的归一化和分类结构元素的基于频率的归一化。

### 段落 41 · Page 5

**EN**

Feature Vector Construction: The complete structural feature

**中文**

特征向量构建：完整的结构特征

### Page 6

### 段落 42 · Page 6

**EN**

vector combines all hierarchical levels with normalization: SF(c) = [Mnorm,E norm,µ norm](5) where components represent normalized macro, meso, and micro features respectively. We employ z-score transformation for continuous features and frequency-based normalization for categorical elements to ensure comparable metrics across documents. C. Architecture-Specific Citation Prediction Different generative engine architectures exhibit distinct structural preferences due to their underlying retrieval-generation mechanisms. We develop predictive models capturing architecture-specific citation behavior.

**中文**

向量将所有层次级别与归一化结合起来：SF(c) = [Mnorm,Enorm,μnorm](5) 其中组件分别表示归一化的宏观、中观和微观特征。我们对连续特征采用 z 分数转换，对分类元素采用基于频率的归一化，以确保跨文档的指标具有可比性。 C. 特定于架构的引文预测 不同的生成式引擎架构由于其底层检索生成机制而表现出不同的结构偏好。我们开发预测模型来捕获特定于架构的引用行为。

### 段落 43 · Page 6

**EN**

TABLE II ARCHITECTURE-SPECIFICGEO FEATUREWEIGHTS Architecture Feature Weight Search-then-SynthesizeMeta-structure clarity 0.45 Upfront density 0.30 Hierarchical depth 0.25 Iterative RefinementCross-reference richness 0.41 Hierarchical breadth-depth 0.35 Query-triggering keywords 0.24 Integrated Search-GenerationChunk independence 0.38 Format diversity 0.35 Aggressive chunking 0.27 Different retrieval architectures prioritize distinct optimization features (Table II). Batch retrieval emphasizes meta-structure and upfront density for initial detection. Multi-round systems favor cross-references enabling iterative refinement.

**中文**

表 II 架构特定的 GEO 特征权重 架构特征权重 搜索然后综合 元结构清晰度 0.45 前期密度 0.30 分层深度 0.25 迭代细化 交叉引用丰富度 0.41 分层广度深度 0.35 查询触发关键字 0.24 集成搜索生成块独立性 0.38格式多样性 0.35 积极分块 0.27 不同的检索架构优先考虑不同的优化功能（表 II）。批量检索强调初始检测的元结构和前期密度。多轮系统有利于交叉引用，从而实现迭代细化。

### 段落 44 · Page 6

**EN**

Real-time architectures optimize chunk independence for streaming extraction. We employ gradient boosting models to predict citation probability given structural features and architecture type: P(cite|SF,A) =σ(w T ASF+b A)(6) whereA ∈ {STS, IR, ISG}denotes architecture type andw A represents architecture-specific feature weights learned from training data. For content targeting multiple architectures, we formulate multi-objective optimization: SF∗ = arg max SF X A∈Atarget αA ·P(cite|SF,A)(7) whereα A represents architecture importance weights based on target platform distribution. D.

**中文**

实时架构优化了流式提取的块独立性。我们采用梯度提升模型来预测给定结构特征和架构类型的引用概率： P(cite|SF,A) =σ(w T ASF+b A)(6) 其中 A ∈ {STS, IR, ISG} 表示架构类型，w A 表示从训练数据中学习到的特定于架构的特征权重。对于针对多个架构的内容，我们制定多目标优化： SF* = arg max SF X A∈Atarget αA ·P(cite|SF,A)(7) 其中α A 表示基于目标平台分布的架构重要性权重。 D .

### 段落 45 · Page 6

**EN**

Structural Optimization Strategies Our optimization strategies transform structural features of content while preserving semantic integrity, employing both rule-based guidelines and algorithmic restructuring methods.

**中文**

结构优化策略我们的优化策略采用基于规则的指导方针和算法重组方法，在保留语义完整性的同时，改变内容的结构特征。

### 段落 46 · Page 6

**EN**

Optimization Objective and Constraints.Given content Cwith current structural featuresSF current, we seek optimal structural configurationSF ∗ that maximizes citation probability across target architectures while preserving semantic integrity: SF∗ = arg max SF X A∈Atarget αA ·P(cite|SF,A) subject to sim semantic(C, T(C))> τ semantic SFmin ≤SF≤SF max (8) whereT(C)represents transformed content,α A denotes architecture importance weights, andSF min,SF max define feasibility bounds ensuring human readability.

**中文**

优化目标和约束。给定内容 C 和当前的结构特征 SF 当前，我们寻求最佳的结构配置 SF *，在保持语义完整性的同时最大化目标架构的引用概率： SF* = arg max SF X A∈Atarget αA ·P(cite|SF,A) 服从 sim 语义(C, T(C))> τ 语义 SFmin ≤SF≤SF max (8) 其中 T(C) 表示转换后的内容，α A 表示架构重要性权重、SF min、SF max 定义了确保人类可读性的可行性范围。

### 段落 47 · Page 6

**EN**

Data-Driven Optimization Principles.We establish five fundamental optimization principles grounded in empirical citation analysis, each with quantitative targets derived from our cross-architecture predictive models: Principle 1: Hierarchical Clarity.Maintain heading hierarchy depthd h ∈[3,5]with balanced section distributionb h(i)≈ 0.3±0.1for non-root levels.

**中文**

数据驱动的优化原则。我们建立了基于经验引文分析的五个基本优化原则，每个原则都有从我们的跨架构预测模型中得出的定量目标：原则 1：层次清晰。保持标题层次结构深度 d h ∈[3,5]，平衡部分分布 b h(i)≈ 0.3±0.1（对于非根级别）。

### 段落 48 · Page 6

**EN**

This range emerges from analyzing attention mechanism behavior across transformer architectures: excessive depth (d h >5) causes attention dilution across too many structural tokens, while insufficient depth (d h <3) fails to provide adequate organizational cues for retrieval algorithms.

**中文**

这个范围是通过分析 Transformer 架构中的注意力机制行为得出的：深度过大 (d h >5) 会导致过多结构标记的注意力稀释，而深度不足 (d h <3) 则无法为检索算法提供足够的组织线索。

### 段落 49 · Page 6

**EN**

Principle 2: Information Chunking.Optimize paragraph length toL p ∈[150,300]words, balancing information density with attention span constraints: Lopt p = arg max Lp P(cite|L p)·coherence(L p)(9) Empirical analysis reveals that chunks exceeding 300 words exhibit 31% attention degradation in middle segments [27], while chunks below 150 words fragment information flow, reducing citation probability by 23%.

**中文**

原理 2：信息分块。将段落长度优化为 L p ∈[150,300]个单词，平衡信息密度与注意力广度约束： Lopt p = arg max Lp P(cite|L p)·coherence(L p)(9) 经验分析表明，超过 300 个单词的块在中间段表现出 31% 的注意力退化 [27]，而低于 150 个单词的块会碎片化信息流，从而降低引用概率23%。

### 段落 50 · Page 6

**EN**

Principle 3: Format Integration.Maintain structured element proportionF d ∈[0.25,0.35]to optimize LLM parsing performance: Fd = P i∈{list, table, code} ni Ntotal (10) Structured formats (lists, tables) demonstrate 43% higher extraction accuracy than equivalent prose in our experiments, but excessive structure (F d >0.35) disrupts reading flow and reduces human comprehension scores.

**中文**

原则 3：格式整合。维持结构化元素比例 F d ∈[0.25,0.35]，以优化 LLM 解析性能： Fd = P i∈{list, table, code} ni Ntotal (10) 在我们的实验中，结构化格式（列表、表格）的提取精度比同等散文高 43%，但过多的结构（F d >0.35）会扰乱阅读流程并降低人类理解分数。

### 段落 51 · Page 6

**EN**

Principle 4: Strategic Emphasis.Apply visual markers toE d ∈ [0.05,0.10]of content with position-weighted distribution: Ep = NX i=1 wi ·e i, w i =    2.0sentence initial 1.5section boundary 1.0standard position (11) Position weights reflect empirically measured attention magnitude differences, with sentence-initial positions receiving 2× attention compared to mid-sentence positions. Principle 5: Navigation Density.Maintain internal linking densityL d ∈[0.15,0.20]enabling multi-hop reasoning: Ld = Ninternal links Nconcepts , ℓ avg <3(12)

**中文**

原则 4：战略重点。将视觉标记应用于具有位置加权分布的内容 E d ∈ [0.05,0.10]： Ep = NX i=1 wi ·e i, w i =    2.0 句首 1.5 节边界 1.0 标准位置 (11) 位置权重反映了经验测量的注意力程度差异，与句首位置与句子中间的位置相比，受到 2 倍的关注。原则5：导航密度。维持内部链接密度L d ∈[0.15,0.20]启用多跳推理：Ld = Ninternal links Nconcepts , ℓ avg <3(12)

### Page 7

### 段落 52 · Page 7

**EN**

whereℓ avg represents average path length in the concept graph. This range supports exploratory traversal without creating excessive navigational complexity.

**中文**

其中ℓ avg 表示概念图中的平均路径长度。该范围支持探索性遍历，而不会产生过多的导航复杂性。

### 段落 53 · Page 7

**EN**

Hierarchical Transformation Framework.Optimization proceeds hierarchically from macro to micro levels, with each level’s transformations constrained by semantic preservation requirements: Algorithm 2Unified Structural Optimization Require:ContentC, target featuresSF target, architecture weights{α A} Ensure:Optimized contentC ∗ with preserved semantics 1:Extract current features:SF current ←extract(C) 2:Compute optimization gaps:∆ level ← ∥SF level target − SFlevel current∥2 3:Initialize:C ′ ←C, valid←true 4:if∆ macro > θmacro then 5:C ′ ←OptimizeMacroStructure(C ′,SF macro target ) 6:ifsem sim(C, C′)< τ doc then 7:C ′ ←C, valid←false 8:ifvali

**中文**

层次化转换框架。优化从宏观到微观层次分层次进行，每个层次的转换受到语义保留要求的约束：算法2统一结构优化要求：ContentC，目标特征SF目标，架构权重{αA}确保：保留语义的优化内容C*1：提取当前特征：SF当前←提取（C）2：计算优化间隙：Δ级别←∥SF级别目标- SFlevel current∥2 3:初始化:C ′ ←C, valid←true 4:ifΔ macro > θmacro then 5:C ′ ←OptimizeMacroStructure(C ′,SF 宏目标) 6:ifsem sim(C, C′)< τ doc then 7:C ′ ←C, valid←false 8:ifvali

### 段落 54 · Page 7

**EN**

d∧∆ meso > θmeso then 9:C ′ ←OptimizeMesoStructure(C ′,SF meso target) 10:ifsem sim(C, C′)< τ para then 11:Rollback to last valid state 12:ifvalid∧(∆ micro > θmicro)then 13:C ′ ←OptimizeMicroStructure(C ′,SF micro target) 14:ifsem sim(C, C′)< τ sent then 15:Rollback to last valid state 16:Compute architecture-weighted visibility:V← P A αA · VisA(C ′) 17:returnC ∗ with maximumVsatisfying all constraints Macro-Structure Optimization.Document-level transformations target heading hierarchy and cross-reference patterns: The algorithm employs semantic clustering for merging and topic diversity analysis for splitting, ensuring all transformations ma

**中文**

d∧Δ meso > θmeso then 9:C ′ ←OptimizeMesoStructure(C ′,SF meso target) 10:ifsem sim(C, C′)< τ para then 11:回滚到最后的有效状态 12:ifvalid∧(Δ micro > θmicro)then 13:C ′ ←OptimizeMicroStructure(C ′,SF micro target) 14:ifsem sim(C, C′)< τ 发送，然后 15:回滚到最后一个有效状态 16:计算架构加权可见性：V← P A αA · VisA(C ′) 17:返回 C *，最大 V 满足所有约束 宏观结构优化。文档级转换目标标题层次结构和交叉引用模式：该算法采用语义聚类进行合并和主题多样性分析分裂，确保所有转换都可以

### 段落 55 · Page 7

**EN**

intain logical coherence.

**中文**

保持逻辑连贯性。

### 段落 56 · Page 7

**EN**

Cross-reference optimization creates small-world network properties with average path lengthℓ <3, supporting multi-hop reasoning across all generative engine architectures. Meso-Structure Optimization.Section-level transformations address paragraph organization and format diversity: Format conversion employs pattern recognition to identify convertible content. And conversion decisions optimize: scoreconvert =w 1 ·parseability+w 2 ·density−w 3 ·disruption (13) wherew 1 = 0.5(LLM extraction accuracy),w 2 = 0.3(information concentration),w 3 = 0.2(reading flow interruption).

**中文**

交叉引用优化创建平均路径长度ℓ<3的小世界网络属性，支持跨所有生成式引擎架构的多跳推理。细观结构优化。节级转换解决段落组织和格式多样性问题：格式转换采用模式识别来识别可转换内容。转换决策优化：scoreconvert=w 1 ·可解析性+w 2 ·密度−w 3 ·中断 (13) 其中w 1 = 0.5（LLM提取精度），w 2 = 0.3（信息集中度），w 3 = 0.2（阅读流中断）。

### 段落 57 · Page 7

**EN**

Micro-Structure Optimization.Sentence-level transformations target emphasis distribution and keyword positioning: Importance scoring integrates multiple signals: TF-IDF captures term significance, centrality measures discourse Algorithm 3Macro-Structure Optimization Require:ContentC, target macro featuresSF macro target Ensure:ContentC ′ with optimized macro-structure 1:H←ExtractHierarchy(C) 2:d current h ←MaxDepth(H),d target h ←SF macro target .dh 3:whiled current h ̸=d target h do 4:ifd current h > dtarget h then 5:sections←GetSectionsAtDepth(H, d current h ) 6:scores←ComputeCoherence(sections) 7:Merge section pair with highest coherence s

**中文**

微观结构优化。句子级转换目标强调分布和关键词定位：重要性评分整合多个信号：TF-IDF捕获术语重要性，中心性衡量话语算法3宏观结构优化要求：ContentC，目标宏特征SF宏目标确保：ContentC′具有优化的宏结构1：H←ExtractHierarchy（C）2：d当前h←MaxDepth（H），d目标h←SF宏target .dh 3:whiled current h ̸=d target h do 4:ifd current h > dtarget h then 5:sections←GetSectionsAtDepth(H, d current h ) 6:scores←ComputeCoherence(sections) 7:合并具有最高相干性 s 的节对

### 段落 58 · Page 7

**EN**

core 8:else 9:sections←GetSectionsAtDepth(H, d current h ) 10:scores←ComputeTopicDiversity(sections) 11:Split section with highest topic diversity 12:d current h ←MaxDepth(H) 13:Balance section distribution: 14:min P i(ni −¯n)2 s.t.

**中文**

core 8:else 9:sections←GetSectionsAtDepth(H, d current h ) 10:scores←ComputeTopicDiversity(sections) 11:以最高主题多样性分割部分 12:d current h ←MaxDepth(H) 13:平衡部分分布： 14:min P i(ni −¯n)2 s.t.

### 段落 59 · Page 7

**EN**

sim(s i, si+1)> τ coherence 15:Optimize cross-references to achieveL d ∈[0.15,0.20]: 16:foreach concept pair(c i, cj)with sim(c i, cj)>0.7do 17:ifPathLength(c i, cj)>2then 18:Add internal link ifL d <0.20 19:returnReconstructContent(H) connectivity, and position rewards section-initial sentences. Emphasis weights (W bold = 1.8> W italic = 1.3> Wunderline = 1.0) reflect empirically measured attention magnitude differences.

**中文**

sim(s i, si+1)> τ 一致性 15:优化交叉引用，实现L d ∈[0.15,0.20]: 16:foreach 概念对(ci, cj)与 sim(ci, cj)>0.7do 17:ifPathLength(ci, cj)>2then 18:添加内部链接 ifL d <0.20 19：returnReconstructContent(H)连接性，位置奖励节首句。重点权重（W 粗体 = 1.8> W 斜体 = 1.3> Wunderline = 1.0）反映了经验测量的注意力程度差异。

### 段落 60 · Page 7

**EN**

Semantic Preservation Constraints.All transformations satisfy hierarchical semantic integrity constraints:    Sentence: e(s)·e(s ′) ∥e(s)∥∥e(s′)∥ > τsent = 0.95 Paragraph: 1 n−1 Pn−1 i=1 sim(pi, pi+1)> τ para = 0.70 Document: JS-divergence(d(C),d(C ′))< ϵ= 0.15 (14) wheree(·)denotes sentence embeddings (Bge-m3 [30]), d(·)represents topic distributions (LDA), and thresholds reflect transformation granularity.

**中文**

语义保留约束。所有转换满足分层语义完整性约束：    句子： e(s)·e(s ′) ∥e(s)∥∥e(s′)∥ > τsent = 0.95 段落：1 n−1 Pn−1 i=1 sim(pi, pi+1)> τ para = 0.70 文档：JS-divergence(d(C),d(C ′))< ϵ= 0.15 (14) 其中e(·)表示句子嵌入（Bge-m3 [30]），d(·)表示主题分布（LDA），阈值反映变换粒度。

### 段落 61 · Page 7

**EN**

When transformations violate constraints, we employ cascading fallback: C ∗ =    Tfull(C)if all constraints satisfied Tpartial(C)if high-impact features satisfy constraints Tminimal(C)if only micro-level satisfies constraints Cotherwise (15) This ensures graceful degradation: if comprehensive optimization violates semantics, we progressively reduce scope until constraints are satisfied, preferring partial optimization over semantic corruption. Architecture-Weighted Target Computation.While optimization algorithms are architecture-agnostic, target

**中文**

当转换违反约束时，我们采用级联后备： C ∗ =    Tfull(C)如果所有约束都满足 Tpartial(C)如果高影响力特征满足约束 Tminimal(C)如果只有微观层面满足约束 Cotherwise (15) 这确保了优雅的降级：如果综合优化违反语义，我们逐渐缩小范围，直到约束满意，更喜欢部分优化而不是语义损坏。架构加权目标计算。虽然优化算法与架构无关，但目标

### Page 8

### 段落 62 · Page 8

**EN**

Algorithm 4Meso-Structure Optimization Require:ContentC, target meso featuresSF meso target Ensure:ContentC ′ with optimized meso-structure 1:P ←ExtractParagraphs(C) 2:L target p ←SF meso target.Lp 3:foreach paragraphp∈ Pdo 4:if|p|>(L target p +σ)then 5:boundaries←DetectTopicShifts(p) 6:if|boundaries|>0then 7:Split at boundaries maintaining coherence> 0.7 8:else 9:Identify least cohesive sentence cluster for split point 10:else if|p|<(L target p −σ)then 11:adjacent←GetAdjacentParagraphs(p) 12:p best ←arg max p′∈adjacent sim(p, p′) 13:ifsim(p, p best)>0.65then 14:Mergepwithp best 15:F current d ←ComputeFormatDiversity(C ′) 16:F target d ←SF me

**中文**

算法 4 中观结构优化 要求：ContentC，目标中观特征 SF 中观目标 确保：具有优化中观结构的 ContentC ′ 1:P ←ExtractParagraphs(C) 2:L 目标 p ←SF 中观目标.Lp 3:foreach paragraphp∈ Pdo 4:if|p|>(L target p +σ)then 5:boundaries←DetectTopicShifts(p) 6:if|boundaries|>0then 7:在边界处分割，保持连贯性> 0.7 8:else 9:识别分割点的最不内聚的句子簇 10:else if|p|<(L target p −σ)then 11:adjacent←GetAdjacentParagraphs(p) 12:p best ←arg max p′∈adjacent sim(p, p′) 13:ifsim(p, p best)>0.65then 14:Mergepwithp best 15:F 当前 d ←ComputeFormatDiversity(C ′) 16:F 目标 d ←SF me

### 段落 63 · Page 8

**EN**

so target.Fd 17:ifF current d < F target d then 18:candidates←IdentifyConvertibleContent(C ′) 19:foreach candidatecin order of conversion scoredo 20:ifF current d < F target d then 21:Convert to structured format (list/table/code block) 22:F current d ←ComputeFormatDiversity(C ′) 23:returnC ′ feature values incorporate architecture-specific preferences as correction weights: SFtarget =SF base + X A∈Atarget αA ·δ A (16) whereSF base represents universal optimal features (from Principles 1-5),δ A denotes architecture-specific deviations (from Section 4.3), andα A weights architectures by importance.

**中文**

so target.Fd 17:ifF current d < F target d then 18:candidates←IdentifyConvertibleContent(C ′) 19:foreach Candidatescin 转换顺序 Scoredo 20:ifF current d < F target d then 21:转换为结构化格式（列表/表格/代码块） 22:F current d ←ComputeFormatDiversity(C ′) 23:returnC ′ feature值将特定于架构的偏好作为校正权重： SFtarget = SF base + X A∈Atarget αA·δ A (16) 其中 SF base 表示通用最优特征（来自原则 1-5），δ A 表示特定于架构的偏差（来自第 4.3 节），α A 按重要性对架构进行加权。

### 段落 64 · Page 8

**EN**

For example, heading depth targets: dtarget h = 4.0 +αSTS ·(+0.5) +α IR ·(0.0) +α ISG ·(−0.5)(17) reflecting Search-then-Synthesize preference for deeper hierarchies (d h ≈4.5), Iterative Refinement neutrality (dh ≈4.0), and Integrated Search-Generation preference for shallower structures (d h ≈3.5). This formulation separates core structural principles (universal across architectures) from architectural adaptations (correction parameters), maintaining generalizability while enabling targeted optimization.

**中文**

例如，航向深度目标：dtarget h = 4.0 +αSTS ·(+0.5) +α IR ·(0.0) +α ISG ·(−0.5)(17) 反映了对更深层次结构的“搜索然后综合”偏好 (d h ≈4.5)、迭代细化中立性 (dh ≈4.0) 以及对较浅结构的集成搜索生成偏好 (d h ≈3.5)。该公式将核心结构原则（跨架构通用）与架构调整（校正参数）分开，在保持通用性的同时实现有针对性的优化。

### 段落 65 · Page 8

**EN**

In summary, the proposed framework of structural feature engineering offers a scientifically grounded, data-driven methodology that empowers content creators to optimize content visibility in generative engine responses Algorithm 5Micro-Structure Optimization Require:ContentC, target micro featuresSF micro target, keyword setK Ensure:ContentC ′ with optimized micro-structure 1:S ←ExtractSentences(C) 2:Compute sentence importance: 3:score(s) = 0.5·TF-IDF(s) + 0.3·centrality(s) + 0.2· position(s) 4:ranked←Sort(S,by score descending) 5:E target d ←SF micro target.Ed 6:n emphasize ← ⌊E target d × |S|⌋ 7:fori= 1ton emphasize do 8:s←ranked[i] 9:key

**中文**

总之，所提出的结构特征工程框架提供了一种有科学依据的、数据驱动的方法，使内容创建者能够优化生成式引擎响应中的内容可见性算法5微结构优化要求：ContentC，目标微特征SF微目标，关键字集K确保：具有优化微结构的ContentC′1：S←ExtractSentences（C）2：计算句子重要性：3：分数= 0.5·TF-IDF(s) + 0.3·中心性(s) + 0.2·位置 4:ranked←排序(S,按分数降序) 5:E target d ←SF micro target.Ed 6:n 强调 ← ⌊E target d × |S|⌋ 7:fori= 1ton 强调 do 8:s←ranked[i] 9:key

### 段落 66 · Page 8

**EN**

words←ExtractKeyTerms(s,K) 10:foreach keywordk∈keywordsdo 11:pos←PositionInSentence(k, s) 12:weight←w pos ▷2.0 initial, 1.5 boundary, 1.0 standard 13:ifweight≥1.5then 14:Apply bold emphasis tok 15:else 16:Apply italic emphasis tok 17:Verify reading ease:R e ←FleschKincaid(C ′) 18:ifR e < Rmin e then 19:Simplify complex sentences via syntax tree pruning 20:Resolve dense subordinate clauses 21:returnC ′ without compromising semantic integrity or cross-platform consistency.

**中文**

Words←ExtractKeyTerms(s,K) 10:foreach keyk∈keywordsdo 11:pos←PositionInSentence(k, s) 12:weight←w pos ▷2.0 初始、1.5 边界、1.0 标准 13:ifweight≥1.5then 14:应用粗体强调 tok 15:else 16:应用斜体强调 tok 17:验证阅读轻松度：R e ←FleschKincaid(C ′) 18:ifR e < Rmin e then 19:通过语法树修剪简化复杂句子 20:解决密集的从句 21:returnC ′，而不影响语义完整性或跨平台一致性。

### 段落 67 · Page 8

**EN**

V. EXPERIMENTALEVALUATION A. Experimental Setup Dataset.We construct our evaluation dataset by sampling 200 articles (approximately 33 per domain) from GEO-bench [1], a dataset specifically designed for generative engine optimization evaluation. Our sample covers six diverse domains (Biography, Health, Technology, Finance, Travel, Science) to ensure generalizability across the full domain spectrum. These articles are paired with 377 real-world queries, with an average article length of 2,547 words.

**中文**

V. 实验评估 A. 实验设置数据集。我们通过从 GEO-bench [1] 中采样 200 篇文章（每个领域大约 33 篇）来构建我们的评估数据集，这是一个专门为生成式引擎优化评估而设计的数据集。我们的样本涵盖六个不同的领域（传记、健康、技术、金融、旅游、科学），以确保在整个领域范围内的普遍性。这些文章与 377 个现实世界的查询配对，平均文章长度为 2,547 个单词。

### 段落 68 · Page 8

**EN**

Semantic preservation verified via sentence embeddings (Bge-m3 [30]): mean similarity = 0.843, confirming structural changes preserve content meaning. Platforms.We evaluate across six mainstream generative engines, categorized by architectural paradigm: TABLE III EVALUATEDGENERATIVEENGINEPLATFORMS Architecture Platforms Characteristics Search-then-Syn Google SGE, Bing Chat Batch retrieval Iterative Refine Perplexity AI, Phind Multi-round search Integrated S-G ChatGPT, Claude Real-time retrieval

**中文**

通过句子嵌入验证语义保留（Bge-m3 [30]）：平均相似度 = 0.843，确认结构变化保留内容含义。我们评估了六种主流生成式引擎，按架构范式分类： 表 III EVALUATEDGENERATIVEENGINEPLATFORMS 架构平台 特征 Search-then-Syn Google SGE、Bing Chat 批量检索 迭代精炼 Perplexity AI、Phind 多轮搜索 集成 S-G ChatGPT、Claude 实时检索

### Page 9

### 段落 69 · Page 9

**EN**

Total evaluation: 200 articles × 6 platforms × 2 versions = 2,400 test cases. Objective Metrics.Our evaluation framework comprises primary and secondary metrics. The primary metrics are formally defined as: CR= # queries citing content total queries (18) VS= 0.4·Coverage+ 0.3·Position+ 0.3·Influence (19) where CR denotes Citation Rate and VS denotes Visibility Score. Secondary metrics include: (1)Citation Depth, measuring the average number of facts extracted per citation, and (2)First Position, indicating the average position of the first citation in responses.

**中文**

总评估：200篇文章×6个平台×2个版本=2,400个测试用例。客观指标。我们的评估框架包括主要指标和次要指标。主要指标的正式定义为： CR= 引用内容的查询数 总查询数 (18) VS= 0.4·覆盖率+ 0.3·位置+ 0.3·影响力 (19) 其中 CR 表示引用率，VS 表示可见度得分。次要指标包括：(1) 引用深度，衡量每次引用提取的事实的平均数量，以及 (2) 第一个位置，指示响应中第一个引用的平均位置。

### 段落 70 · Page 9

**EN**

Subjective Evaluation.Beyond objective metrics, we employ G-Eval [31] to assess seven subjective dimensions using Gemini 2.5 Pro: Relevance, Influence, Uniqueness, Subjective Position, Subjective Count, Click Probability, and Diversity. Scores are normalized to match the Position-Adjusted Word Count distribution for cross-metric comparison. Each evaluation uses median scores from 5 samples at temperature 0.3. B. Experimental Results Citation Performance.Table IV presents aggregated results demonstrating consistent citation improvements from structural optimization. TABLE IV CITATIONPERFORMANCE: BASELINE VS.

**中文**

主观评估。除了客观指标之外，我们还采用 G-Eval [31] 来使用 Gemini 2.5 Pro 评估七个主观维度：相关性、影响力、独特性、主观位置、主观计数、点击概率和多样性。分数被标准化以匹配位置调整字数分布以进行跨指标比较。每次评估均使用 5 个样品在温度 0.3 下的中值分数。 B. 实验结果引用性能。表 IV 提供了汇总结果，证明结构优化带来的一致引用改进。表 IV 引文表现：基线与实际结果

### 段落 71 · Page 9

**EN**

GEO-SFE Architecture Citation Rate (%) Visibility Score Improve Base Opt Base Opt(%) Search-then-Syn 43.7 52.1 0.401 0.481 +19.2* Iterative Refine 52.3 59.6 0.474 0.541 +14.0* Integrated S-G 39.1 46.8 0.358 0.428 +19.7* Overall 45.0 52.8 0.411 0.483 +17.3* *p <0.001, paired t-test,n= 200, Cohen’s d = 0.64 Structural optimization yielded significant improvements across all architectures 14-20% (mean: 17.3%,p <0.001), with higher gains in Search-then-Synthesize and Integrated Search-Generation reflecting their structural sensitivity.

**中文**

GEO-SFE 架构引用率 (%) 可见性得分 提高 Base Opt Base Opt(%) Search-then-Syn 43.7 52.1 0.401 0.481 +19.2* 迭代细化 52.3 59.6 0.474 0.541 +14.0* 集成 S-G 39.1 46.8 0.358 0.428 +19.7* 总体 45.0 52.8 0.411 0.483 +17.3* *p <0.001，配对 t 检验，n= 200，Cohen d = 0.64 结构优化在所有架构中产生了 14-20% 的显着改进（平均值：17.3%，p <0.001），收益更高在“搜索然后综合”和“集成搜索生成”中反映了它们的结构敏感性。

### 段落 72 · Page 9

**EN**

Iterative Refinement architectures, despite having higher baseline citation rates due to exhaustive multi-round search, still demonstrated meaningful improvements (14.0%) from cross-reference network optimization. The medium-to-large effect size (Cohen’sd= 0.64) indicates practical significance. Subjective Impression.Table V presents the G-Eval assessment results across all subjective dimensions.

**中文**

迭代细化架构尽管由于详尽的多轮搜索而具有更高的基线引用率，但仍然通过交叉引用网络优化展示了有意义的改进（14.0％）。中到大的效应量（Cohen’sd= 0.64）表明了实际意义。主观印象。表 V 展示了所有主观维度的 G-Eval 评估结果。

### 段落 73 · Page 9

**EN**

Structural optimization yields significant improvements across all subjective dimensions (average: +18.5%).Influence (+32.0%) andClick Probability(+31.4%) demonstrate the largest gains, reflecting how macro-structural clarity enhances narrative authority and meso-structural formatting improves visual appeal. TABLE V G-EVALSUBJECTIVEIMPRESSIONMETRICS Metric Baseline GEO-SFE Improvement (%) Relevance 18.7±2.8 22.3±2.5 +19.3 Influence 17.5±3.2 23.1±2.7 +32.0 Uniqueness 21.3±2.2 23.6±2.0 +10.8 Subj. Position 19.1±2.9 22.8±2.6 +19.4 Subj.

**中文**

结构优化在所有主观维度上都带来了显着改善（平均：+18.5%）。影响力（+32.0%）和点击概率（+31.4%）显示出最大的收益，反映了宏观结构清晰度如何增强叙事权威，中观结构格式如何提高视觉吸引力。表 V G-评估主观印象指标 指标基线 GEO-SFE 改进 (%) 相关性 18.7±2.8 22.3±2.5 +19.3 影响 17.5±3.2 23.1±2.7 +32.0 独特性 21.3±2.2 23.6±2.0 +10.8位置 19.1±2.9 22.8±2.6 +19.4

### 段落 74 · Page 9

**EN**

Count 20.8±2.5 23.4±2.3 +12.5 Click Probability 17.2±3.4 22.6±2.9 +31.4 Diversity 22.1±2.1 23.7±1.9 +7.2 Overall Average19.5±1.7 23.1±1.4 +18.5 All improvements significant atp <0.001(paired t-test,n= 200) C. Ablation Analysis To isolate structural feature contributions, we systematically remove each hierarchical level from optimization.

**中文**

计数 20.8±2.5 23.4±2.3 +12.5 点击概率 17.2±3.4 22.6±2.9 +31.4 多样性 22.1±2.1 23.7±1.9 +7.2 总体平均值 19.5±1.7 23.1±1.4 +18.5 所有改进显着 atp <0.001（配对） t-test,n= 200) C. 消融分析 为了隔离结构特征贡献，我们系统地从优化中删除每个层次级别。

### 段落 75 · Page 9

**EN**

TABLE VI HIERARCHICALFEATUREABLATION Configuration CR (%) VS Drop Contrib Full Optimization 52.8 0.483 — 100% w/o Macro 49.3 0.451 -3.5 44.9% w/o Meso 49.7 0.455 -3.1 39.7% w/o Micro 51.6 0.473 -1.2 15.4% Baseline 45.0 0.411 -7.8 — Ablation analysis reveals that macro-structure contributes 44.9% of total gains, meso-structure 39.7%, and micro-structure 15.4%, with individual contributions summing to 100.0% indicating these structural levels operate largely independently in their optimization impact.

**中文**

表 VI 分层特征 配置 CR (%) VS Drop Contrib 全面优化 52.8 0.483 — 100%，不含宏观 49.3 0.451 -3.5 44.9%，不含中观 49.7 0.455 -3.1 39.7%，不含微观 51.6 0.473 -1.2 15.4% 基线 45.0 0.411 -7.8 — 消融分析显示，宏观结构贡献了总收益的 44.9%，中观结构贡献了 39.7%，微观结构贡献了 15.4%，个人贡献总计为 100.0%，表明这些结构水平在优化影响方面很大程度上独立运作。

### 段落 76 · Page 9

**EN**

Experimental results demonstrate that GEO-SFE achieves significant citation improvements (17.3%,p <0.001) through hierarchical structural features that operate independently and complement semantic methods effectively. Subjective evaluations further validate the approach, showing substantial gains in narrative influence (+32.0%) and user engagement (+31.4% click probability), with an overall 18.5% improvement across perceptual dimensions.

**中文**

实验结果表明，GEO-SFE 通过独立运行并有效补充语义方法的分层结构特征，实现了显着的引用改进（17.3％，p <0.001）。主观评估进一步验证了该方法，显示叙事影响力 (+32.0%) 和用户参与度 (+31.4% 点击概率) 显着提高，感知维度总体提高 18.5%。

### 段落 77 · Page 9

**EN**

The framework maintains superior semantic integrity while enabling combined performance gains and generalizes robustly across content domains, validating structural optimization as a foundational GEO framework. VI. CONCLUSION The GEO-SFE framework proposed in this paper represents a systematic approach to optimizing content visibility in LLM-powered generative engines through structural feature engineering.

**中文**

该框架保持了卓越的语义完整性，同时实现了综合性能增益，并在内容领域中稳健地推广，验证了结构优化作为基础 GEO 框架的有效性。六．结论 本文提出的 GEO-SFE 框架代表了一种通过结构特征工程优化 LLM 驱动的生成式引擎中内容可见性的系统方法。

### 段落 78 · Page 9

**EN**

By decomposing content structure into three hierarchical levels, including macro-structure (document architecture), meso-structure (information chunking), and micro-structure (visual emphasis), we establish quantifiable metrics for structural optimization independent of semantic content modifications. Experimental evaluation across six mainstream generative engines demonstrates consistent citation improvements of 17.3% (p <0.001), complemented

**中文**

通过将内容结构分解为三个层次结构，包括宏观结构（文档架构）、中观结构（信息分块）和微观结构（视觉强调），我们建立了独立于语义内容修改的结构优化的量化指标。对六种主流生成式引擎的实验评估表明，引用率持续提高 17.3% (p <0.001)，补充

### Page 10

### 段落 79 · Page 10

**EN**

by 18.5% average gains in subjective perceptual quality. Ablation analysis reveals independent contributions from each structural level, underscoring the practical applicability and generalizability of the proposed framework across diverse content domains and architectural paradigms. This work establishes structural feature engineering as a foundational component of the GEO discipline, providing content creators with scientifically grounded methodologies for navigating the emerging ”citations economy” where visibility depends on algorithmic comprehension rather than traditional ranking metrics. REFERENCES [1] P. Aggarwal, V . Murahari, T.

**中文**

主观感知质量平均提高 18.5%。消融分析揭示了每个结构级别的独立贡献，强调了所提出的框架在不同内容领域和架构范式中的实际适用性和普遍性。这项工作将结构特征工程确立为 GEO 学科的基础组成部分，为内容创建者提供有科学依据的方法，以驾驭新兴的“引文经济”，其中可见性取决于算法理解而不是传统的排名指标。参考文献 [1] P. Aggarwal, V.穆拉哈里，T.

### 段落 80 · Page 10

**EN**

Rajpurohit, A. Kalyan, K. Narasimhan, and A. Deshpande, “Geo: Generative engine optimization,” inProceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining, 2024, pp. 5–16. [2] P. Lewis, E. Perez, A. Piktus, F. Petroni, V . Karpukhin, N. Goyal, H. K ¨uttler, M. Lewis, W.-t. Yih, T. Rockt ¨aschel, S. Riedel, and D. Kiela, “Retrieval-augmented generation for knowledge-intensive nlp tasks,”Advances in neural information processing systems, vol. 33, pp. 9459–9474, 2020. [3] R. Nakano, J. Hilton, S. Balaji, J. Wu, L. Ouyang, C. Kim, C. Hesse, S. Jain, V . Rint, A. Askell, S. Kadavath, A. Jones, D. Drain, S. Anna, Z.

**中文**

Rajpurohit、A. Kalyan、K. Narasimhan 和 A. Deshpande，“Geo：生成式引擎优化”，第 30 届 ACM SIGKDD 知识发现和数据挖掘会议记录，2024 年，第 5-16 页。 [2] P. Lewis、E. Perez、A. Piktus、F. Petroni、V。卡普欣，N.戈亚尔，H.库特勒，M.刘易斯，W.-t。 Yih，T. Rockt ¡aschel，S. Riedel 和 D. Kiela，“知识密集型 NLP 任务的检索增强生成”，神经信息处理系统进展，卷。 33，第 9459–9474 页，2020 年。 [3] R. Nakano、J. Hilton、S. Balaji、J. Wu、L. Ouyang、C. Kim、C. Hesse、S. Jain、V . Rint，A.阿斯克尔，S.卡达瓦斯，A.琼斯，D.排水，S.安娜，Z。

### 段落 81 · Page 10

**EN**

Li, K. Tran, N. Durmus, Y . Gan, P. Christiano, and J. Leike, “Webgpt: Browser-assisted question-answering with human feedback,” arXiv preprint arXiv:2112.09332, 2021. [4] R. Thoppilan, D. De Freitas, J. Hall, N. Shazeer, A. Kulshreshtha, H.-T. Cheng, A. Jin, T. Bos, L. Baker, Y . Duet al., “Lamda: Language models for dialog applications,”arXiv preprint arXiv:2201.08239, 2022. [5] A. Kumar and H. Lakkaraju, “Manipulating large language models to increase product visibility,”arXiv preprint arXiv:2404.07981, 2024. [6] Z. Yang, D. Yang, C. Dyer, X. He, A. Smola, and E.

**中文**

Li，K. Tran，N. Durmus，Y。 Gan、P. Christiano 和 J. Leike，“Webgpt：带有人类反馈的浏览器辅助问答”，arXiv 预印本 arXiv：2112.09332，2021。 [4] R. Thoppilan、D. De Freitas、J. Hall、N. Shazeer、A. Kulshreshtha、H.-T。 Cheng，A. Jin，T. Bos，L. Baker，Y。 Duet al.，“Lamda：对话应用程序的语言模型”，arXiv 预印本 arXiv：2201.08239，2022。 [5] A. Kumar 和 H. Lakkaraju，“操纵大型语言模型以提高产品可见性”，arXiv 预印本 arXiv：2404.07981，2024。 [6] Z. Yang、D. Yang、C. Dyer、X.他、A.斯莫拉和E.

### 段落 82 · Page 10

**EN**

Hovy, “Hierarchical attention networks for document classification,” inProceedings of the 2016 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, K. Knight, A. Nenkova, and O. Rambow, Eds. San Diego, California: Association for Computational Linguistics, June 2016, pp. 1480–1489. [Online]. Available: https://aclanthology.org/N16-1174/ [7] A. Vaswani, N. Shazeer, N. Parmar, J. Uszkoreit, L. Jones, A. N. Gomez, Ł. Kaiser, and I. Polosukhin, “Attention is all you need,”Advances in neural information processing systems, vol. 30, 2017. [8] S.

**中文**

Hovy，“用于文档分类的分层注意力网络”，载于计算语言学协会北美分会 2016 年会议记录：人类语言技术，K. Knight、A. Nenkova 和 O. Rambow，编辑。加利福尼亚州圣地亚哥：计算语言学协会，2016 年 6 月，第 1480–1489 页。 [在线的]。可用：https://aclanthology.org/N16-1174/ [7] A. Vaswani、N. Shazeer、N. Parmar、J. Uszkoreit、L. Jones、A. N. Gomez、Ł。 Kaiser 和 I. Polosukhin，“注意力就是你所需要的”，神经信息处理系统的进展，卷。 2017年3月30日。 [8] S.

### 段落 83 · Page 10

**EN**

Ray, “How generative engines are rewriting search - literally!” Medium, May 2025. [9] Weka Team, “Retrieval augmented generation: Everything you need to know about RAG in AI,”Weka.io, October 2024. [10] D. Tank, “Understanding RAG-Fusion: Next-level retrieval-augmented generation,”Medium, April 2025. [11] Z. Rackauckas, “RAG-Fusion: A new take on retrieval-augmented generation,” arXiv preprint arXiv:2402.03367, Tech. Rep., 2024. [12] Microsoft Cloud Team, “Common retrieval augmented generation (RAG) techniques explained,” Microsoft Corporation, Tech. Rep., June 2025.

**中文**

Ray，“生成式引擎如何重写搜索——字面上！” Medium，2025 年 5 月。[9] Weka Team，“检索增强生成：关于 AI 中的 RAG 你需要了解的一切”，Weka.io，2024 年 10 月。[10] D. Tank，“理解 RAG-Fusion：下一级检索增强生成”，Medium，2025 年 4 月。[11] Z. Rackauckas，“RAG-Fusion：一种新的看法”检索增强生成”，arXiv 预印本 arXiv:2402.03367，Tech。 Rep.，2024 年。[12] Microsoft 云团队，“常见检索增强生成 (RAG) 技术的解释”，Microsoft Corporation，Tech。众议员，2025 年 6 月。

### 段落 84 · Page 10

**EN**

[13] Azure AI Team, “Raising the bar for RAG excellence: Introducing generative query rewriting and new ranking model,” Microsoft Azure, Tech. Rep., November 2024. [14] e. a. Xu, “Retrieval-augmented generation: A comprehensive survey of architectures, enhancements, and robustness frontiers,”arXiv preprint arXiv:2506.00054, May 2025. [15] OpenAI, “ChatGPT browse and real-time web access,” 2025, platform documentation. [16] Azure Architecture Center, “Develop a RAG solution—information-retrieval phase,” Microsoft Corporation, Tech. Rep., 2025. [17] Consensus and Elicit, “Vertical domain search implementations,” 2025, academic search platforms.

**中文**

[13] Azure AI 团队，“提高 RAG 卓越标准：引入生成查询重写和新的排名模型”，Microsoft Azure，技术。众议员，2024 年 11 月。[14] e．一个。 Xu，“检索增强生成：架构、增强和鲁棒性前沿的全面调查”，arXiv 预印本 arXiv:2506.00054，2025 年 5 月。 [15] OpenAI，“ChatGPT 浏览和实时 Web 访问”，2025 年，平台文档。 [16] Azure 架构中心，“开发 RAG 解决方案 - 信息检索阶段”，Microsoft Corporation，Tech。 Rep.，2025。 [17] Consensus and Elicit，“垂直领域搜索实现”，2025，学术搜索平台。

### 段落 85 · Page 10

**EN**

[18] Aqueous Digital, “An overview of google’s search generative experience (sge),” Aqueous Digital Blog, July 8 2025, blog post. [19] D. Sullivan, “How to create an effective seo strategy in 2025,” Backlinko, February 2025, blog post. [20] Immwit, “Generative search optimization updates 2025 timeline,” Immwit News, May 7 2025, news article. [21] Direct Online Marketing, “Google sge rollout: What it means for seo in 2025,” DOM Blog, January 2025, sEO analysis. [22] C. Liu, H. Chen, Y . Cai, H. Wu, Q. Ye, M.-H. Yang, and Y . Wang, “Structured attention matters to multimodal llms in document understanding,” 2025, submitted on 19 Jun 2025.

**中文**

[18] Aqueous Digital，“谷歌搜索生成体验 (sge) 概述”，Aqueous Digital 博客，2025 年 7 月 8 日，博客文章。 [19] D. Sullivan，“如何在 2025 年制定有效的 SEO 策略”，Backlinko，2025 年 2 月，博客文章。 [20] Immwit，“生成式搜索优化更新 2025 年时间表”，Immwit 新闻，2025 年 5 月 7 日，新闻文章。 [21] 直接在线营销，“Google sge 推出：2025 年对 seo 意味着什么”，DOM 博客，2025 年 1 月，sEO 分析。 [22] 刘春，陈华，Y．蔡红武，叶强，M.-H。杨，Y。 Wang，“文档理解中多模式 LLMS 的结构性关注问题”，2025 年，于 2025 年 6 月 19 日提交。

### 段落 86 · Page 10

**EN**

[Online]. Available: https://arxiv.org/abs/2506.21600 [23] Z. Babar, “Hierarchical processing patterns for managing context in llms,” Medium, April 21 2024, blog post. [24] Z. Guan, J. Wang, S. Chen, X. Li, and Y . Zhang, “Attention mechanisms perspective: Exploring llm processing of graph-structured data,” 2025. [25] X. Wang, Y . Li, H. Chen, M. Liu, and Q. Zhang, “Attention heads of large language models: A survey,”ScienceDirect, February 6 2025, survey article. [26] Y . Sui, M. Zhou, M. Zhou, S. Han, and D. Zhang, “Table meets llm: Can large language models understand structured table data?

**中文**

[在线]。可用：https://arxiv.org/abs/2506.21600 [23] Z. Babar，“管理 llms 中上下文的分层处理模式”，Medium，2024 年 4 月 21 日，博客文章。 [24] 管子，王建，陈世，李晓，Y。张，“注意力机制视角：探索图结构数据的 llm 处理”，2025 年。 [25] X. Wang, Y。 Li、H. Chen、M. Liu 和 Q. Zhang，“大型语言模型的注意力头：一项调查”，ScienceDirect，2025 年 2 月 6 日，调查文章。 [26] Y. Sui、M. Zhou、M. Zhou、S. Han 和 D. Zhang，“表遇见 llm：大型语言模型能否理解结构化表数据？

### 段落 87 · Page 10

**EN**

a benchmark and empirical study,” inProceedings of the 17th ACM International Conference on Web Search and Data Mining. ACM, 2024, pp. 645–654. [Online]. Available: https://arxiv.org/abs/2305.13062 [27] N. F. Liu, K. Lin, J. Hewitt, A. Paranjape, M. Bevilacqua, F. Petroni, and P. Liang, “Lost in the middle: How language models use long contexts,”arXiv preprint arXiv:2307.03172, 2023. [Online]. Available: https://arxiv.org/abs/2307.03172 [28] Google, “Introduction to how structured data markup works,” Google Search Central, Tech. Rep., 2025. [29] KI Company, “Schema markup for GEO: How to optimize your content for AI,”KI Company Blog, 2025.

**中文**

基准和实证研究，”第 17 届 ACM 国际网络搜索和数据挖掘会议论文集。 ACM，2024 年，第 645–654 页。 [在线的]。可用：https://arxiv.org/abs/2305.13062 [27] N. F. Liu、K. Lin、J. Hewitt、A. Paranjape、M. Bevilacqua、F. Petroni 和 P. Liang，“迷失在中间：语言模型如何使用长上下文”，arXiv 预印本 arXiv：2307.03172，2023 年。[在线]。可用：https://arxiv.org/abs/2307.03172 [28] Google，“结构化数据标记如何工作​​的简介”，Google 搜索中心，技术。 Rep.，2025 年。[29] KI Company，“GEO 的架构标记：如何优化 AI 内容”，KI 公司博客，2025 年。

### 段落 88 · Page 10

**EN**

[30] J. Chen, S. Xiao, P. Zhang, K. Luo, D. Lian, and Z. Liu, “Bge m3-embedding: Multi-lingual, multi-functionality, multi-granularity text embeddings through self-knowledge distillation,”arXiv preprint arXiv:2402.03216, 2024. [31] Y . Liu, D. Iter, Y . Xu, S. Wang, R. Xu, and C. Zhu, “G-eval: Nlg evaluation using gpt-4 with better human alignment,”arXiv preprint arXiv:2303.16634, 2023.

**中文**

[30] J. Chen、S. Xiao、P. Zhu、K. Luo、D. Lian 和 Z. Liu，“Bge m3 嵌入：通过自我知识蒸馏实现多语言、多功能、多粒度文本嵌入”，arXiv 预印本 arXiv:2402.03216, 2024。 [31] Y .刘，D.伊特，Y。 Xu、S. Wang、R. Xu 和 C. Zhu，“G-eval：使用 gpt-4 进行 Nlg 评估，具有更好的人类对齐能力”，arXiv 预印本 arXiv：2303.16634，2023。
