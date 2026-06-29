# IF-GEO: Conflict-Aware Instruction Fusion for Multi-Query Generative Engine Optimization

- ID: 69
- 类型: pdf
- 分类: 04_academic_papers
- 主题: multi-query GEO content revisions
- 原文链接: https://arxiv.org/pdf/2601.13938
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

IF-GEO: Conflict-Aware Instruction Fusion for Multi-Query Generative Engine Optimization Heyang Zhou1, JiaJia Chen2, Xiaolu Chen1, Jie Bao1, Zhen Chen1*, Yong Liao1 1School of Cyber Science and Technology, University of Science and Technology of China 2Institute of Dataspace, Hefei Comprehensive National Science Center, Hefei, China heyangzhou@mail.ustc.edu.cn Abstract As Generative Engines revolutionize information retrieval by synthesizing direct answers from retrieved sources, ensuring source visibility becomes a significant challenge.

**中文**

IF-GEO：多查询生成式引擎优化的冲突感知指令融合 Heyang Zhou1、JiaJia Chen2、Xiaolu Chen1、Jie Bao1、Zhen Chen1*、Yong Liao1 1中国科学技术大学网络科学与技术学院 2合肥综合国家科学中心数据空间研究所，合肥，中国 heyangzhou@mail.ustc.edu.cn 摘要 生成式引擎彻底改变了信息检索从检索到的来源合成直接答案，确保来来源可见度成为一项重大挑战。

### 段落 2 · Page 1

**EN**

Improving it through targeted content revisions is a practical strategy termed Generative Engine Optimization (GEO). However, optimizing a document for diverse queries presents a constrained optimization challenge where heterogeneous queries often impose conflicting and competing revision requirements under a limited content budget. To address this challenge, we propose IF-GEO, a“diverge-then-converge” framework comprising two phases: (i) mining distinct optimization preferences from representative latent queries; (ii) synthesizing a Global Revision Blueprintfor guided editing by coordinating preferences via conflict-aware instruction fusion.

**中文**

通过有针对性的内容修订来改进它是一种称为生成式引擎优化（GEO）的实用策略。然而，针对不同查询优化文档提出了受限的优化挑战，其中异构查询经常在有限的内容预算下强加冲突和竞争的修订要求。为了应对这一挑战，我们提出了 IF-GEO，一种“发散然后聚合”框架，包括两个阶段：（i）从代表性潜在查询中挖掘不同的优化偏好； (ii) 通过冲突感知指令融合来协调偏好，从而合成用于引导编辑的全局修订蓝图。

### 段落 3 · Page 1

**EN**

To explicitly quantify IF- GEO’s objective of cross-query stability, we introduce risk-aware stability metrics. Experiments on multi-query benchmarks demonstrate that IF-GEO achieves substantial performance gains while maintaining robustness across diverse retrieval scenarios. 1 Introduction The evolution from traditional Search Engines (SEs) to Generative Search Engines (GSEs) represents a significant shift in information retrieval (Brin and Page, 1998; Aggarwal et al., 2024). Unlike SEs, which present ranked lists of hyperlinks, GSEs adopt a retrieve-then-generate paradigm (Lewis et al., 2020; Karpukhin et al., 2020).

**中文**

为了明确量化 IF-GEO 的跨查询稳定性目标，我们引入了风险意识稳定性指标。多查询基准实验表明，IF-GEO 实现了显着的性能提升，同时在不同的检索场景中保持了鲁棒性。 1 简介 从传统搜索引擎（SE）到生成式搜索引擎（GSE）的演变代表了信息检索的重大转变（Brin 和 Page，1998；Aggarwal 等，2024）。与呈现超链接排名列表的 SE 不同，GSE 采用检索然后生成范例（Lewis 等人，2020 年；Karpukhin 等人，2020 年）。

### 段落 4 · Page 1

**EN**

By employing Large Language Models (LLMs) to synthesize direct answers from retrieved documents, GSEs provide users with synthesized information rather than a list of sources. However, ensuring source visibility presents a significant challenge for content providers. Since * Corresponding author. Figure 1: Challenges of GEO. Revision requests of different queries can beconflictingandcompetitiveunder a limited content budget. GEO have no idea which query to follow. visibility depends on whether a document is selected and cited by the model rather than its ranking position, traditional optimization techniques are less effective.

**中文**

通过采用大型语言模型 (LLM) 从检索到的文档中合成直接答案，GSE 为用户提供合成信息而不是来源列表。然而，确保来源可见度对内容提供商来说是一个重大挑战。自 * 通讯作者。图 1：GEO 的挑战。在有限的内容预算下，不同查询的修改请求可能会发生冲突和竞争。 GEO 不知道要遵循哪个查询。可见性取决于文档是否被模型选择和引用，而不是其排名位置，传统的优化技术效果较差。

### 段落 5 · Page 1

**EN**

To address this, Generative Engine Optimization (GEO) has been proposed as a prominent strategy to improve content visibility in generated responses through targeted document revisions (Aggarwal et al., 2024). Existing GEO methods typically utilize static heuristic rules (Aggarwal et al., 2024) or optimize content based on aggregated engine preferences inferred from ranking signals (Wu et al., 2025; Chen et al., 2025a). While recent work like RAID (Chen et al., 2025b) advances the field by modeling latent retrieval intents, it prioritizes a single aggregated intent trajectory.

**中文**

为了解决这个问题，生成式引擎优化（GEO）被提出作为一种重要的策略，通过有针对性的文档修订来提高生成响应中的内容可见性（Aggarwal 等人，2024）。现有的 GEO 方法通常利用静态启发式规则（Aggarwal 等人，2024）或根据从排名信号推断出的聚合引擎偏好来优化内容（Wu 等人，2025；Chen 等人，2025a）。虽然 RAID（Chen 等人，2025b）等最近的工作通过对潜在检索意图建模来推进该领域的发展，但它优先考虑单个聚合意图轨迹。

### 段落 6 · Page 1

**EN**

These approaches treat the serving of diverse heterogeneous queries as a onedimensional optimization problem. However, in practice, a single document needs to serve diverse user queries simultaneously (Broder, 2002; Clarke et al., 2008; Wang et al., 2009). This creates a constrained optimization problem, where heterogeneous queries often impose conflicting requirements on the document’s limited content as illusarXiv:2601.13938v1 [cs.IR] 20 Jan 2026

**中文**

这些方法将不同异构查询的服务视为一维优化问题。然而，在实践中，单个文档需要同时服务不同的用户查询（Broder，2002；Clarke 等人，2008；Wang 等人，2009）。这会产生一个受限的优化问题，其中异构查询经常对文档的有限内容施加相互冲突的要求，如 illusarXiv:2601.13938v1 [cs.IR] 20 Jan 2026

### Page 2

### 段落 7 · Page 2

**EN**

trated in Figure 1 (Marler and Arora, 2004; Rose and Levinson, 2004). Current methods lack the mechanisms to coordinate these competing preferences. Consequently, optimizing for one query often results in diminished or negative gains for others, creating competitive imbalances that we empirically analyze in Appendix A, leading to inconsistent revisions and performance variance across the query set.

**中文**

如图 1 所示（Marler 和 Arora，2004 年；Rose 和 Levinson，2004 年）。当前的方法缺乏协调这些相互竞争的偏好的机制。因此，针对一个查询的优化通常会导致其他查询的收益减少或为负，从而造成我们在附录 A 中实证分析的竞争不平衡，从而导致整个查询集的修订不一致和性能差异。

### 段落 8 · Page 2

**EN**

To address this challenge, we proposeIF-GEO, a“diverge-then-converge”framework comprising two phases: (i) mining representative latent queries and formulating their distinct optimization preferences as structured edit requests; and (ii) synthesizing a unifiedGlobal Revision Blueprintfor guided editing by coordinating preferences via conflictaware instruction fusion. Crucially, we formally integrate risk-aware stability metrics into the IF- GEO optimization objective to explicitly quantify cross-query stability.

**中文**

为了应对这一挑战，我们提出了 IF-GEO，一个“发散然后聚合”的框架，包括两个阶段：（i）挖掘代表性的潜在查询并将其独特的优化偏好制定为结构化编辑请求； (ii) 通过冲突感知指令融合协调偏好来合成统一的全局修订蓝图，用于引导编辑。至关重要的是，我们正式将风险意识稳定性指标集成到 IF-GEO 优化目标中，以明确量化跨查询稳定性。

### 段落 9 · Page 2

**EN**

By introducing Worst- Case Performance (WCP), Win-Tie Rate (WTR), and Downside Risk (DR), we establish a robust standard that addresses the limitations of meanvariance evaluations—which often mask tail degradations and conflate beneficial upside with harmful downside volatility. Our contributions are summarized as follows: • We proposeIF-GEO, a“diverge-thenconverge”framework. It predicts latent queries to formulate specific edit requests and employs conflict-aware instruction fusion to synthesize a unifiedGlobal Revision Blueprint for coherent document revision.

**中文**

通过引入最坏情况表现（WCP）、平局率（WTR）和下行风险（DR），我们建立了一个强大的标准来解决均值评估的局限性——这通常掩盖尾部退化并将有利的上行与有害的下行波动混为一谈。我们的贡献总结如下： • 我们提出IF-GEO，一个“发散然后聚合”的框架。它预测潜在查询以制定特定的编辑请求，并采用冲突感知指令融合来合成统一的全局修订蓝图，以实现连贯的文档修订。

### 段落 10 · Page 2

**EN**

• We introduce an evaluation methodology utilizing risk-aware stability metrics—specifically Worst-Case Performance, Downside Risk, and Win-Tie Rate—to explicitly quantify the safety and robustness of optimization across diverse queries. • Empirical results on multi-query benchmarks demonstrate that IF-GEO achieves substantial improvements in overall visibility while effectively mitigating performance variance, ensuring robust stability across heterogeneous retrieval scenarios.

**中文**

• 我们引入了一种利用风险意识稳定性指标（特别是最坏情况性能、下行风险和获胜率）的评估方法，以明确量化跨不同查询的优化的安全性和稳健性。 • 多查询基准的实证结果表明，IF-GEO 在整体可视性方面取得了显着改进，同时有效地减轻了性能差异，确保了异构检索场景的稳健稳定性。

### 段落 11 · Page 2

**EN**

2 Related Works 2.1 Generative Search Engines Generative Search Engines (GSEs) increasingly follow aretrieve–then–generateparadigm, producing answer-centric responses with explicit source attributions. Technically, many such systems build on retrieval-augmented generation (RAG) (Lewis et al., 2020) and retrieval-augmented pretraining/memory architectures such as REALM (Guu et al., 2020) and RETRO (Borgeaud et al., 2022). In practice, these pipelines often pair dense neural retrievers (e.g., DPR) (Karpukhin et al., 2020) with multi-passage evidence fusion generators (e.g., FiD) (Izacard and Grave, 2021).

**中文**

2 相关工作 2.1 生成式搜索引擎 生成式搜索引擎（GSE）越来越多地遵循“检索然后生成”范式，生成具有明确来源属性的以答案为中心的响应。从技术上讲，许多此类系统都建立在检索增强生成（RAG）（Lewis 等人，2020）和检索增强预训练/记忆架构之上，例如 REALM（Guu 等人，2020）和 RETRO（Borgeaud 等人，2022）。在实践中，这些管道通常将密集神经检索器（例如 DPR）（Karpukhin 等人，2020）与多通道证据融合生成器（例如 FiD）（Izacard 和 Grave，2021）配对。

### 段落 12 · Page 2

**EN**

Unlike traditional search engines that prioritize document ranking based on keyword matching(Gleason et al., 2023), GSEs leverage the semantic reasoning capabilities of LLMs to synthesize information from multiple disparate sources (Li et al., 2025). To improve verifiability and citation consistency, prior work has introduced browsing/citation constraints and dedicated benchmarks for attribution quality (e.g., WebGPT (Nakano et al., 2021), GopherCite (Menick et al., 2022), and CITE (Gao et al., 2023)).

**中文**

与根据关键字匹配对文档进行优先级排序的传统搜索引擎不同（Gleason 等人，2023），GSE 利用法学硕士的语义推理能力来合成来自多个不同来源的信息（Li 等人，2025）。为了提高可验证性和引文一致性，之前的工作引入了浏览/引文约束和归因质量专用基准（例如，WebGPT（Nakano 等人，2021）、GopherCite（Menick 等人，2022）和 CITE（Gao 等人，2023））。

### 段落 13 · Page 2

**EN**

These architectural shifts fundamentally alter the optimization landscape, motivating downstream objectives that emphasize not just retrieval rank, but visibility and attribution within the generated narrative. 2.2 Generative Engine Optimization Generative Engine Optimization (GEO) aims to improve visibility within generative answers through content modifications. Existing work broadly falls into three lines. (i) Single-objective and heuristic optimization.

**中文**

这些架构上的转变从根本上改变了优化格局，激发了下游目标，这些目标不仅强调检索排名，还强调生成的叙述中的可见性和归因。 2.2 生成式引擎优化 生成式引擎优化（GEO）旨在通过内容修改来提高生成答案的可见性。现有的工作大致分为三类。 (i) 单目标和启发式优化。

### 段落 14 · Page 2

**EN**

Early work formalized GEO with heuristic strategies (Aggarwal et al., 2024), while recent works explored specific interventions like caption injection (Chen and Liao, 2025) or transformer-based rewriting (Lüttgenau et al., 2025). These approaches apply preset or singletarget editing rules, lacking adaptation to diverse query conflicts. (ii) Feedback-driven Optimization. This line treats engines as black boxes, optimizing content by inferring implicit preferences from ranking signals (Wu et al., 2025) or employing iterative feedback loops (Bagga et al., 2025; Chen et al., 2025a).

**中文**

早期的工作通过启发式策略将 GEO 形式化（Aggarwal 等人，2024），而最近的工作则探索了具体的干预措施，例如标题注入（Chen 和 Liao，2025）或基于 Transformer 的重写（Lüttgenau 等人，2025）。这些方法应用预设或单一目标编辑规则，缺乏对不同查询冲突的适应。 (ii) 反馈驱动的优化。该系列将引擎视为黑匣子，通过从排名信号推断隐式偏好（Wu 等人，2025）或采用迭代反馈循环（Bagga 等人，2025；Chen 等人，2025a）来优化内容。

### 段落 15 · Page 2

**EN**

However, they often overfit to specific engine behaviors and ignore cross-query stability. (iii) Intent-based optimization. This line considers optimization over a document’s latent queries. RAID leverages multi-role reflection to generalize latent search intents(Chen et al., 2025b), but optimizes around a single aggregated intent. Overall, prior methods treat optimization targets in isolation or aggregation. They lack mechanisms to coordinate diverse intents, failing to balance competitive

**中文**

然而，它们经常过度适应特定的引擎行为并忽略跨查询稳定性。 (iii) 基于意图的优化。此行考虑对文档的潜在查询进行优化。 RAID 利用多角色反射来概括潜在搜索意图（Chen 等人，2025b），但围绕单个聚合意图进行优化。总体而言，现有方法单独或聚合地对待优化目标。他们缺乏协调不同意图的机制，无法平衡竞争

### Page 3

### 段落 16 · Page 3

**EN**

trade-offs under a limited content budget, which ultimately hinders robust and stable optimization. 3 Problem Definition 3.1 Setting and Notation Given a query expression q, a generative engine (GE) retrieves a set of candidate documents Cq = Retrieval(q) ={D 1, . . . , DN } and generates a response text rq = Generate(q,C q), which includes citations to documents in Cq. We define an answerinduced visibility score v(Di, rq) to quantify how visible a document Di ∈ C q is within the response rq, based only on the response text and its citation/attribution signals.

**中文**

在有限的内容预算下进行权衡，最终阻碍稳健和稳定的优化。 3 问题定义 3.1 设置和表示法 给定一个查询表达式 q，生成式引擎（GE）检索一组候选文档 Cq = Retrieval(q) ={D 1, .。。 , DN } 并生成响应文本 rq =Generate(q,Cq)，其中包括对 Cq 中文档的引用。我们定义一个答案引起的可见性分数 v(Di, rq) 来量化文档 Di ∈ C q 在响应 rq 中的可见程度，仅基于响应文本及其引用/归因信号。

### 段落 17 · Page 3

**EN**

Since rq is conditioned on q, we use the shorthandv(D, q)to denote the visibility of a document D under query q. Importantly, v(·) is aplug-inmetric and can be instantiated with different operational definitions of visibility. 3.2 Optimization Objective Given a document D, we consider a target set of queries Q(D) =q im i=1 that represent the queries we aim to optimize for. For each qi ∈Q(D) , the visibility ofDunderq i is measured byv(D, q i). A GEO method M takes D as input and produces an optimized document D′ =M(D) .

**中文**

由于 rq 以 q 为条件，因此我们使用简写 v(D, q) 来表示查询 q 下文档 D 的可见性。重要的是，v(·) 是一个插件度量，可以用不同的可见性操作定义来实例化。 3.2 优化目标 给定文档 D，我们考虑一组目标查询 Q(D) =q im i=1，它们代表我们旨在优化的查询。对于每个 qi ∈Q(D)，Dunderq i 的可见性通过 v(D, q i) 来测量。 GEO 方法 M 将 D 作为输入并生成优化文档 D′ =M(D)。

### 段落 18 · Page 3

**EN**

For each query qi ∈Q(D) , we define the per-query visibility gain as: ∆vi =v(D ′, qi)−v(D, q i).(1) We summarize the optimization effect over the query set Q(D) by applying a plug-in aggregation functionalA(·)to the gain vector: ∆ =A {∆v i }m i=1  .(2) The choice of A is application-dependent and can be instantiated with different operational definitions (e.g., mean for average improvement). GEO aims to find a method M that optimizes ∆ under the chosen definition ofA. 4 Method 4.1 Overview: IF-GEO We proposeIF-GEO, a two-stage framework for GEO under generative engines. IF-GEO follows a “diverge-then-converge”workflow.

**中文**

对于每个查询 qi ∈Q(D)，我们将每个查询的可见性增益定义为： Δvi =v(D ′, qi)−v(D, q i)。(1) 我们通过将插件聚合函数 A(·) 应用于增益向量来总结查询集 Q(D) 上的优化效果： Δ =A {Δv i }m i=1。(2) A 的选择取决于应用程序，可以使用不同的操作定义进行实例化（例如，平均改进的平均值）。 GEO 的目标是找到一种在选定的 A 定义下优化 Δ 的方法 M。 4 方法4.1 概述：IF-GEO 我们提出IF-GEO，一个生成式引擎下GEO 的两阶段框架。 IF-GEO 遵循“发散然后聚合”的工作流程。

### 段落 19 · Page 3

**EN**

In thediverge phase, it discover representative latent queries and elicit their distinct optimization preferences as structured edit requests. Theconvergephase then coordinates and balances these competing preferences through conflict-aware instruction fusion, synthesizing them into a unifiedglobal revision blueprintthat provides a comprehensive optimization direction for guided editing. Beyond maximizing average visibility, IF-GEO explicitly optimizes for stability metrics (e.g., WCP, DR) to minimize cross-query downside risks, ensuring robust performance where standard mean-based approaches often fail. Figure 2 overviews the pipeline.

**中文**

在发散阶段，它发现有代表性的潜在查询，并以结构化编辑请求的形式引出它们独特的优化偏好。然后，融合阶段通过冲突感知指令融合来协调和平衡这些相互竞争的偏好，将它们合成为统一的全局修订蓝图，为引导编辑提供全面的优化方向。除了最大化平均可见性之外，IF-GEO 还显式优化稳定性指标（例如 WCP、DR），以最大限度地减少交叉查询的下行风险，从而在标准的基于均值的方法经常失败的情况下确保稳健的性能。图 2 概述了该管道。

### 段落 20 · Page 3

**EN**

All steps of IF-GEO are implemented via LLM calls, where the model acts as a constrained executor that outputs structured intermediate artifacts rather than performing free-form rewriting. Full prompt specifications and output schemas are provided in Appendix B. We next detail the two phases of this workflow: Query Discovery and Request Generation as the diverge phase, followed by Instruction Fusion as the converge phase. 4.2 Query Discovery and Request Generation 4.2.1 Query Mining As the first step in thedivergephase, we conduct query miningto expand the document into a representative query set.

**中文**

IF-GEO 的所有步骤都是通过 LLM 调用实现的，其中模型充当约束执行器，输出结构化中间工件，而不是执行自由形式重写。附录 B 中提供了完整的提示规范和输出模式。接下来我们详细介绍此工作流程的两个阶段：查询发现和请求生成作为发散阶段，然后是指令融合作为聚合阶段。 4.2 查询发现和请求生成 4.2.1 查询挖掘 作为发散阶段的第一步，我们进行查询挖掘以将文档扩展为代表性查询集。

### 段落 21 · Page 3

**EN**

We treat this process asreverse retrieval: given D, we guide the LLM to act as a search analyst and discover diverse queries for which the document should be a relevant result. To ensure the set is representative and avoid redundant tuning, the system explicitly instructs the model to target different aspects of the document’s main theme while strictly prohibiting simple paraphrases. This step outputs a weighted query setQ(D): Q(D) ={(q i, wi)}m i=1 (3) where each query qi serves as a specific context for generating subsequent edit requests. The associated weight wi is a scalar score (0–100) estimating query popularity.

**中文**

我们将此过程视为反向检索：给定 D，我们引导法学硕士充当搜索分析师，并发现文档应该是相关结果的各种查询。为了确保该集合具有代表性并避免冗余调整，系统明确指示模型针对文档主题的不同方面，同时严格禁止简单的释义。此步骤输出加权查询集Q(D)： Q(D) ={(q i, wi)}m i=1 (3) 其中每个查询qi 作为生成后续编辑请求的特定上下文。关联的权重 wi 是估计查询流行度的标量分数 (0–100)。

### 段落 22 · Page 3

**EN**

Drawing on the scoring capability demonstrated in G-EV AL (Liu et al., 2023), we leverage the model’s parametric knowledge to assign this priority, which guides the later fusion phase. 4.2.2 Query-specific Request Generation Given the weighted query setQ(D), the core objective of this step is to elicit the distinct optimization preferences of each query regarding the document. IF-GEO operationalizes these abstract preferences

**中文**

借鉴 G-EVAL（Liu et al., 2023）中展示的评分能力，我们利用模型的参数知识来分配此优先级，从而指导后续的融合阶段。 4.2.2 特定于查询的请求生成给定加权查询集Q(D)，此步骤的核心目标是得出关于文档的每个查询的不同优化偏好。 IF-GEO 将这些抽象偏好付诸实施

### Page 4

### 段落 23 · Page 4

**EN**

Figure 2: Overview of the IF-GEO methodology. IF-GEO follows a “diverge-then-converge” paradigm. In Phase I, the system mines a representative query set and elicits query-specific editing requests, which may be redundant or conflicting. In Phase II, IF-GEO performs conflict-aware instruction fusion to synthesize a unified global revision blueprint, which guides controlled editing to produce an optimized document with stable visibility across queries. into concrete, actionableedit requests(instruction candidates).

**中文**

图 2：IF-GEO 方法概述。 IF-GEO 遵循“发散然后聚合”的范式。在第一阶段，系统挖掘代表性查询集并引发特定于查询的编辑请求，这些请求可能是冗余的或冲突的。在第二阶段，IF-GEO 执行冲突感知指令融合，以合成统一的全局修订蓝图，指导受控编辑以生成跨查询具有稳定可见性的优化文档。转化为具体的、可操作的编辑请求（候选指令）。

### 段落 24 · Page 4

**EN**

By analyzing each query qi in isolation, the model explicitly diagnoses specific content gaps and proposes targeted revisions to address them. Formally, for thej-th request derived from query qi, we define a structured request tuple: ri,j =⟨e i,j, ui,j, si,j⟩(4) where ei,j is the excerpt-based anchor locating the target text, ui,j is the specific revision suggestion, and si,j is a quantitativenecessity score(0–100). Adopting the scalar evaluation methodology validated in (Liu et al., 2023), we employ this score to explicitly measure the criticality of the fix for satisfying qi, distinguishing essential edits from marginal improvements.

**中文**

通过单独分析每个查询 qi，该模型可以明确诊断特定的内容差距，并提出有针对性的修订来解决这些问题。形式上，对于从查询 qi 派生的第 j 个请求，我们定义一个结构化请求元组： ri,j =⟨e i,j, ui,j, si,j⟩(4) 其中 ei,j 是定位目标文本的基于摘录的锚点，ui,j 是具体的修订建议，si,j 是定量必要性得分（0-100）。采用（Liu et al., 2023）中验证的标量评估方法，我们使用此分数来明确衡量修复满足 qi 的关键性，区分基本编辑和边际改进。

### 段落 25 · Page 4

**EN**

Aggregating these outputs yields a diverged request pool R={r i,j}, which serves as the raw material for the subsequent conflict-aware fusion. 4.3 Conflict-Aware Instruction Fusion 4.3.1 Prioritization and Deduplication The converge phase begins by consolidating the diverged request pool R into a compact, high-signal candidate set. First, to identify requests with high cross-query importance, we compute aglobal priority scorefor each item: gi,j =w i ·s i,j (5) where wi is the query weight and si,j is the necessity score. We filter out low-priority requests falling below a threshold τ to control perturbation.

**中文**

聚合这些输出会产生一个发散的请求池 R={r i,j}，它充当后续冲突感知融合的原材料。 4.3 冲突感知指令融合 4.3.1 优先级划分和重复数据删除 聚合阶段首先将发散的请求池 R 合并为紧凑的高信号候选集。首先，为了识别具有高交叉查询重要性的请求，我们计算每个项目的全局优先级分数： gi,j =w i ·s i,j (5) 其中 wi 是查询权重，si,j 是必要性分数。我们过滤掉低于阈值 τ 的低优先级请求以控制扰动。

### 段落 26 · Page 4

**EN**

Next, we perform semantic deduplication to remove redundancy. Requests targeting overlapping anchors with similar revision goals are merged into a single meta-request. These merged items inherit the highest necessity score from their constituents and are standardized with concise topic tags. This step reduces the raw pool into a smaller set of wellscoped candidates, ready for conflict resolution. 4.3.2 Conflict Resolution Following deduplication, the system addresses mutually exclusive requests targeting the same content. IF-GEO employs apriority-based resolution strategy.

**中文**

接下来，我们执行语义重复数据删除以消除冗余。针对具有相似修订目标的重叠锚点的请求被合并到单个元请求中。这些合并的项目继承了其组成部分的最高必要性分数，并使用简洁的主题标签进行标准化。此步骤将原始池缩小为范围更小的候选者集合，为冲突解决做好准备。 4.3.2 冲突解决 重复数据删除后，系统会处理针对相同内容的互斥请求。 IF-GEO 采用基于优先级的解析策略。

### 段落 27 · Page 4

**EN**

Instead of relying on a rigid numerical threshold, we delegate the decision to the model, instructing it to evaluate the priority scores (g) in context to determine the appropriate action: • Selection:When the model perceives a significant priority gap, the higher-scoring instruction is strictly retained, and the conflicting one is discarded. • Synthesis:When the model determines that priority scores are comparable ( gi ≈g j), it generates a new compromise instruction. This instruction balances the valid needs of both queries rather than satisfying only one.

**中文**

我们不依赖严格的数字阈值，而是将决策委托给模型，指示它在上下文中评估优先级分数 (g) 以确定适当的操作： • 选择：当模型感知到显着的优先级差距时，将严格保留得分较高的指令，并丢弃冲突的指令。 • 综合：当模型确定优先级分数具有可比性（gi ≈g j）时，它会生成新的折衷指令。该指令平衡了两个查询的有效需求，而不是只满足一个查询。

### Page 5

### 段落 28 · Page 5

**EN**

This approach leverages the model’s semantic reasoning capabilities to handle edge cases more flexibly than hard-coded rules. 4.3.3 Blueprint Construction As the final step of theconvergephase, we consolidate the fused instructions into aGlobal Revision Blueprint. This step is crucial for coordinating the competing needs of multiple queries within a shared content budget. We map individual instructions to their corresponding document sections and aggregate them into ordered plan items. By organizing revisions structurally rather than sequentially by query, the blueprint ensures that distinct optimization goals areintegrated coherently.

**中文**

这种方法利用模型的语义推理功能比硬编码规则更灵活地处理边缘情况。 4.3.3 蓝图构建 作为融合阶段的最后一步，我们将融合指令合并为全局修订蓝图。此步骤对于协调共享内容预算内多个查询的竞争需求至关重要。我们将各个指令映射到相应的文档部分，并将它们聚合成有序的计划项目。通过按结构而不是按查询顺序组织修订，蓝图可确保不同的优化目标得到连贯的集成。

### 段落 29 · Page 5

**EN**

The resulting JSON blueprint serves as a strict execution contract, effectively resolving the structural conflicts between queries and preventing the inconsistent edits typical of single-pass optimization. 4.3.4 Blueprint-Guided Revision In the final step, IF-GEO uses the Revision Blueprint to generate the optimized document D′. The revision model acts as a constrained editor, strictly following the blueprint instructions to modify the document section by section. Crucially, the system explicitly instructs the model to preserve all unmentioned sections exactly as is.

**中文**

生成的 JSON 蓝图充当严格的执行契约，有效解决查询之间的结构冲突，并防止单遍优化中典型的不一致编辑。 4.3.4 蓝图引导修订最后一步，IF-GEO 使用修订蓝图生成优化文档D′。修订模型充当约束编辑器，严格按照蓝图说明逐节修改文档。至关重要的是，系统明确指示模型按原样保留所有未提及的部分。

### 段落 30 · Page 5

**EN**

This strict adherence ensures that the global optimization strategy is implemented accurately without introducing free-form rewriting or unintended content drift. 4.4 Risk-Aware Optimization Objective Standard visibility maximization often masks tail degradations and conflates beneficial upside with harmful downside volatility. To address this, we formally integrate risk-aware stability metrics into the IF-GEO objective.

**中文**

这种严格遵守确保了全局优化策略的准确实施，而不会引入自由形式重写或意外的内容漂移。 4.4 风险意识优化目标 标准可见性最大化通常会掩盖尾部退化，并将有利的上行与有害的下行波动混为一谈。为了解决这个问题，我们正式将风险意识稳定性指标整合到 IF-GEO 目标中。

### 段落 31 · Page 5

**EN**

Beyond maximizing expected gain E[∆v], we explicitly safeguard crossquery stability through three dimensions: • Worst Case Performance (WCP)establishes a safety lower bound by capturing the maximum single-query drop (Ben-Tal and Nemirovski, 1998): WCP= m min i=1 ∆vi.(6) • Downside Risk (DR)exclusively penalizes the magnitude of negative gains to distinguish harmful failures from beneficial volatility (Mamoghli and Daboussi, 2009): DR= 1 m mX i=1 min(0,∆v i) 2.(7) • Win-Tie Rate (WTR)quantifies the coverage of non-regressive optimization, serving as a proxy for Pareto optimality without collateral damage(Radlinski et al., 2008): WTR= 1 m mX i=1 I(∆vi ≥0).(8) In summary, IF-GEO seeks to maximize visibility gain subject to minimizing DR and maximizing WCP and WTR.

**中文**

除了最大化预期收益 E[Δv] 之外，我们还通过三个维度明确维护交叉查询稳定性： • 最坏情况性能 (WCP) 通过捕获最大单查询下降建立安全下限（Ben-Tal 和 Nemirovski，1998）：WCP= m min i=1 Δvi。(6) • 下行风险 (DR) 专门惩罚负收益的大小，以区分有害的失败和有益的波动（Mamoghli 和 Daboussi， 2009): DR= 1 m mX i=1 min(0,Δv i) 2.(7) • 平局率 (WTR) 量化非回归优化的覆盖范围，作为无附带损害的帕累托最优性的代理(Radlinski et al., 2008): WTR= 1 m mX i=1 I(Δvi ≥0)。(8) 总之，IF-GEO 寻求最大化能见度增益取决于最小化 DR 和最大化 WCP 和 WTR。

### 段落 32 · Page 5

**EN**

5 Experimental Setup 5.1 Dataset To evaluate performance in a realistic multi-query scenario, we adopt the benchmark introduced by RAID (Chen et al., 2025b), which expands the widely-used GEO-Bench (Aggarwal et al., 2024). In this dataset, each document D is originally a top-ranked result (top-5) retrieved by Google Search for a real-world source query. Building on this high-relevance foundation, RAID extends each source query into a cluster of five related queries.

**中文**

5 实验设置 5.1 数据集 为了评估实际多查询场景中的性能，我们采用 RAID 引入的基准（Chen 等人，2025b），它扩展了广泛使用的 GEO-Bench（Aggarwal 等人，2024）。在此数据集中，每个文档 D 最初都是 Google 搜索针对真实世界源查询检索到的排名最高的结果（前 5 名）。在此高相关性基础上，RAID 将每个源查询扩展为由五个相关查询组成的集群。

### 段落 33 · Page 5

**EN**

Crucially, these queries go beyond simple rephrasing that they constitute a multifaceted inquiry into the document’s topic, targetingdistinct informational dimensions(e.g., definition, usage, pros/cons) rather than mere lexical variations. This construction forms a query set that effectively serves as aconcrete instantiationof the representative query setdescribed in our problem definition. Using this dataset allows us to move beyond single-query evaluation and test whether IF-GEO’s optimized document maintains high visibility and stability acrossdiverse user queries.

**中文**

至关重要的是，这些查询不仅仅是简单的改写，它们构成了对文档主题的多方面查询，针对不同的信息维度（例如定义、用法、优点/缺点），而不仅仅是词汇变化。这种构造形成了一个查询集，该查询集有效地充当我们的问题定义中描述的代表性查询集的具体实例。使用此数据集使我们能够超越单一查询评估，并测试 IF-GEO 的优化文档是否在不同的用户查询中保持高可见性和稳定性。

### 段落 34 · Page 5

**EN**

5.2 Baselines We benchmark IF-GEO against three representative methods covering the primary paradigms in Generative Engine Optimization: Heuristic-based: GEO (Aggarwal et al., 2024). Representing static, query-agnostic optimization, this framework applies nine human-designed heuristic rules. We evaluate all nine strategies, ranging from stylistic interventions (e.g., AUTHOR- ITATIVE) to content enrichment (e.g., STATISTICS ADDITION, CITESOURCES).

**中文**

5.2 基线 我们将 IF-GEO 与涵盖生成式引擎优化主要范例的三种代表性方法进行基准测试：基于启发式：GEO（Aggarwal 等人，2024）。该框架代表静态、与查询无关的优化，应用了九个人工设计的启发式规则。我们评估了所有九种策略，从文体干预（例如权威）到内容丰富（例如统计添加、CITESOURCES）。

### Page 6

### 段落 35 · Page 6

**EN**

Table 1: Comparison of IF-GEO with baseline methods on objective and subjective visibility improvements. We report overall improvement (Mean) to summarize average gains. Underlined indicates the best baseline. Method Objective Impression Subjective Impression Word PositionOverall Rel. Infl. Unique Div. FollowUp Pos. CountAverage Tran. SEO 1.83 1.77 1.84 1.44 1.62 1.24 1.50 1.44 1.73 1.58 1.51 Uniq. Word -0.70 -1.00 -0.79 -0.20 -0.16 -0.44 -0.42 -0.46 -0.71 -0.38 -0.39 Simp. Expr. 0.16 0.28 0.28 0.59 0.84 0.73 0.72 0.35 1.02 0.57 0.69 Auth. Expr. 0.97 0.88 0.92 0.56 1.08 0.60 0.86 0.57 1.29 0.74 0.81 Flue. Expr.

**中文**

表 1：IF-GEO 与基准方法在客观和主观可见性改进方面的比较。我们报告总体改善（平均值）以总结平均收益。下划线表示最佳基线。方法 客观印象 主观印象 词语位置 整体关系。膨胀。独特的部门。跟进职位。平均计数。搜索引擎优化 1.83 1.77 1.84 1.44 1.62 1.24 1.50 1.44 1.73 1.58 1.51字 -0.70 -1.00 -0.79 -0.20 -0.16 -0.44 -0.42 -0.46 -0.71 -0.38 -0.39表达式。 0.16 0.28 0.28 0.59 0.84 0.73 0.72 0.35 1.02 0.57 0.69表达式。 0.97 0.88 0.92 0.56 1.08 0.60 0.86 0.57 1.29 0.74 0.81 烟道。表达式。

### 段落 36 · Page 6

**EN**

0.92 0.94 1.03 0.52 0.82 0.48 0.48 0.29 1.23 0.56 0.63 Term. Addi. 1.00 1.07 1.17 0.71 1.22 0.50 0.73 0.43 1.06 0.63 0.75 Cite Sources 4.47 4.59 4.71 3.17 3.45 3.36 3.16 2.96 3.83 3.26 3.31 Quot. Addi. 4.29 4.19 4.23 2.57 2.87 3.10 2.45 2.25 3.28 2.48 2.71 Stat. Addi. 3.28 3.39 3.49 2.15 2.48 2.54 1.97 1.89 3.01 2.16 2.31 RAID 1.06 0.78 0.88 1.44 1.75 1.40 1.08 0.84 1.68 1.34 1.36 Auto-GEO 7.80 7.64 7.59 4.99 5.68 5.18 4.74 4.19 6.63 4.77 5.30 IF-GEO 11.07 11.15 11.03 5.12 6.16 5.90 5.29 5.34 7.32 5.98 5.87 Intent-based: RAID G-SEO (Chen et al., 2025b).

**中文**

0.92 0.94 1.03 0.52 0.82 0.48 0.48 0.29 1.23 0.56 0.63阿迪。 1.00 1.07 1.17 0.71 1.22 0.50 0.73 0.43 1.06 0.63 0.75 引用来源 4.47 4.59 4.71 3.17 3.45 3.36 3.16 2.96 3.83 3.26 3.31阿迪。 4.29 4.19 4.23 2.57 2.87 3.10 2.45 2.25 3.28 2.48 2.71阿迪。 3.28 3.39 3.49 2.15 2.48 2.54 1.97 1.89 3.01 2.16 2.31 RAID 1.06 0.78 0.88 1.44 1.75 1.40 1.08 0.84 1.68 1.34 1.36 自动 GEO 7.80 7.64 7.59 4.99 5.68 5.18 4.74 4.19 6.63 4.77 5.30 IF-GEO 11.07 11.15 11.03 5.12 6.16 5.90 5.29 5.34 7.32 5.98 5.87基于意图：RAID G-SEO（Chen 等人，2025b）。

### 段落 37 · Page 6

**EN**

Representing intent-driven optimization, RAID employs a “4W” multi-role reflection mechanism to infer and refine latent user search intents. It guides content rewriting by deepening a single, focused intent trajectory. Preference-based: Auto-GEO (Wu et al., 2025). Representing data-driven optimization, this framework automatically learns generative engine preferences from large-scale ranking data. We apply the learned, engine-specific rule sets to optimize target documents based on global utility signals.

**中文**

RAID代表意图驱动的优化，采用“4W”多角色反射机制来推断和细化潜在用户搜索意图。它通过深化单一、集中的意图轨迹来指导内容重写。基于偏好：Auto-GEO（Wu 等人，2025）。该框架代表数据驱动的优化，自动从大规模排名数据中学习生成式引擎偏好。我们应用学习到的特定于引擎的规则集来根据全局效用信号优化目标文档。

### 段落 38 · Page 6

**EN**

For a fair comparison, all baselines and IF-GEO are implemented using the same underlying LLM (GPT-4o-mini) and decoding configurations to isolate the impact of the optimization methodology. 5.3 Evaluation Metrics Following the protocol in GEO-bench (Aggarwal et al., 2024), we evaluate both overall visibility and cross-query stability. For each query qi, we compute the visibility score v(D, qi) and the optimization gain∆v i.

**中文**

为了公平比较，所有基线和 IF-GEO 均使用相同的底层 LLM (GPT-4o-mini) 和解码配置来实现，以隔离优化方法的影响。 5.3 评估指标按照 GEO-bench 中的协议（Aggarwal 等人，2024），我们评估整体可见性和跨查询稳定性。对于每个查询 qi，我们计算可见性得分 v(D, qi) 和优化增益Δv i。

### 段落 39 · Page 6

**EN**

Visibility Instantiations v(·).We instantiate v(·) with: (i)Objective Impression, the Position- Adjusted Word Count (PAWC) that weights cited text volume by citation position; and (ii)Subjective Impression, a qualitative LLM-as-a-judge score implemented via G-EV AL (Liu et al., 2023) and normalized to match PAWC statistics following (Aggarwal et al., 2024). Aggregation Strategies A(·).To comprehensively evaluate the gain vector{∆vi}m i=1, we instantiate the aggregation functionalA(·) (defined in §3) using distinct criteria. We reportMeanandVarianceto measure general effectiveness and volatility.

**中文**

可见性实例化 v(·)。我们用以下内容实例化 v(·)： (i) 客观印象，按引用位置对引用文本量进行加权的位置调整字数 (PAWC)； (ii) 主观印象，通过 G-EV AL 实施的定性法学硕士评分（Liu 等人，2023），并标准化以匹配以下 PAWC 统计数据（Aggarwal 等人，2024）。聚合策略A(·)。为了综合评估增益向量{Δvi}m i=1，我们使用不同的标准实例化聚合函数A(·)（在§3中定义）。我们报告均值和方差来衡量总体有效性和波动性。

### 段落 40 · Page 6

**EN**

Crucially, to evaluate the safety objectives formulated in §4.4, we report Worst-Case Performance (WCP), Downside Risk (DR), and Win-Tie Rate (WTR). All metrics are computed per document and averaged over the evaluation set. 5.4 Experimental Environment and Setting We follow the simulated generative engine setup and evaluation protocol in GEO (Aggarwal et al., 2024) for reproducibility. All experiments are conducted under a single target generative engine, GPT- 4o-mini, using the same decoding parameters as GEO to ensure comparability. For IF-GEO, all internal calls use the same model.

**中文**

至关重要的是，为了评估第 4.4 节中制定的安全目标，我们报告了最坏情况表现 (WCP)、下行风险 (DR) 和平局率 (WTR)。所有指标均按文档计算，并在评估集上取平均值。 5.4 实验环境和设置我们遵循 GEO 中的模拟生成式引擎设置和评估协议（Aggarwal 等人，2024）以确保可重复性。所有实验均在单目标生成式引擎 GPT-4o-mini 下进行，使用与 GEO 相同的解码参数以确保可比性。对于 IF-GEO，所有内部呼叫都使用相同的模型。

### 段落 41 · Page 6

**EN**

Unless otherwise specified, we use: query expansion size Nq=5, suggestions per query Ns=5, internal temperature 0.2, and global priority filtering threshold τ=0.7. We analyze the impact of query expansion size in §6.3. Due to the cost of generative-engine evaluation, different experiments use different numbers of queries. Unless otherwise specified, main results are evaluated on 1,000 queries, matching the original GEO test set. Ablation studies use 250 queries, and the query expansion analysis in §6.3 uses 500 queries. All queries are sampled from the same distribution.

**中文**

除非另有说明，我们使用：查询扩展大小Nq=5，每个查询的建议Ns=5，内部温度0.2，全局优先级过滤阈值τ=0.7。我们在第 6.3 节中分析了查询扩展大小的影响。由于生成式引擎评估的成本，不同的实验使用不同数量的查询。除非另有说明，主要结果是在 1,000 个查询上评估的，与原始 GEO 测试集匹配。消融研究使用 250 个查询，第 6.3 节中的查询扩展分析使用 500 个查询。所有查询都是从同一分布中采样的。

### Page 7

### 段落 42 · Page 7

**EN**

Table 2: Comparison of IF-GEO with baseline methods in robustness and stability across queries. We report variance (V AR↓), worst-case performance (WCP↑), win–tie rate (WTR↑), and downside risk (DR↓) for both the primary objective metric (Obj. Overall) and subjective metric (Subj. Average). Method Objective (Overall) Subjective (Average) V AR (↓) WCP (↑) WTR (↑) DR (↓) V AR (↓) WCP (↑) WTR (↑) DR (↓) Tran. SEO 0.0147 -0.0878 68.93% 0.0062 0.0199 -0.1026 88.19% 0.0080 Uniq. Word 0.0157 -0.1316 61.04% 0.0095 0.0226 -0.1361 85.34% 0.0130 Simp. Expr. 0.0116 -0.1051 66.43% 0.0058 0.0156 -0.0939 88.17% 0.0073 Auth. Expr.

**中文**

表 2：IF-GEO 与基线方法在跨查询的鲁棒性和稳定性方面的比较。我们报告主要客观指标（Obj.Overall）和主观指标（Subj.Average）的方差（VAR↓）、最坏情况表现（WCP↑）、平局率（WTR↑）和下行风险（DR↓）。方法 客观（总体） 主观（平均） VAR (↓) WCP (↑) WTR (↑) DR (↓) VAR (↓) WCP (↑) WTR (↑) DR (↓) Tran。搜索引擎优化 0.0147 -0.0878 68.93% 0.0062 0.0199 -0.1026 88.19% 0.0080字 0.0157 -0.1316 61.04% 0.0095 0.0226 -0.1361 85.34% 0.0130表达式。 0.0116 -0.1051 66.43% 0.0058 0.0156 -0.0939 88.17% 0.0073表达式。

### 段落 43 · Page 7

**EN**

0.0136 -0.1018 65.84% 0.0065 0.0200 -0.1148 86.89% 0.0089 Flue. Expr. 0.0130 -0.1028 68.93% 0.0061 0.0187 -0.1084 87.38% 0.0091 Term. Addi. 0.0143 -0.1113 67.31% 0.0062 0.0216 -0.1266 86.61% 0.0103 Cite Sources 0.0165 -0.0785 72.06% 0.0044 0.0209 -0.0892 88.93% 0.0070 Quot. Addi. 0.0173 -0.0831 70.56% 0.0055 0.0218 -0.1013 88.25% 0.0087 Stat. Addi.

**中文**

0.0136 -0.1018 65.84% 0.0065 0.0200 -0.1148 86.89% 0.0089 烟道。表达式。 0.0130 -0.1028 68.93% 0.0061 0.0187 -0.1084 87.38% 0.0091阿迪。 0.0143 -0.1113 67.31% 0.0062 0.0216 -0.1266 86.61% 0.0103 引用来源 0.0165 -0.0785 72.06% 0.0044 0.0209 -0.0892 88.93% 0.0070引用。阿迪。 0.0173 -0.0831 70.56% 0.0055 0.0218 -0.1013 88.25% 0.0087阿迪。

### 段落 44 · Page 7

**EN**

0.0173 -0.0901 72.58% 0.0060 0.0203 -0.0946 88.48% 0.0074 RAID 0.0166 -0.1141 64.50% 0.0088 0.0195 -0.1100 82.37% 0.0089 Auto-GEO 0.0159 -0.0511 73.56% 0.0043 0.0203 -0.0798 84.19% 0.0064 IF-GEO 0.0189 -0.0090 80.50% 0.0023 0.0116 -0.0419 85.56% 0.0036 6 Experiments 6.1 Main Results Overall effectiveness.Table 1 compares IF-GEO with a diverse set of baselines. IF-GEO achieves the best performance across all objective and subjective dimensions, reaching an objective overall score of 11.03 and a subjective average of5.87.

**中文**

0.0173 -0.0901 72.58% 0.0060 0.0203 -0.0946 88.48% 0.0074 RAID 0.0166 -0.1141 64.50% 0.0088 0.0195 -0.1100 82.37% 0.0089自动GEO 0.0159 -0.0511 73.56% 0.0043 0.0203 -0.0798 84.19% 0.0064 IF-GEO 0.0189 -0.0090 80.50% 0.0023 0.0116 -0.0419 85.56% 0.0036 6 实验 6.1 主要结果 总体有效性。表 1 将 IF-GEO 与一组不同的基线进行了比较。 IF-GEO 在所有客观和主观维度上均取得了最佳表现，客观总分达到 11.03，主观平均分达到 5.87。

### 段落 45 · Page 7

**EN**

Notably, Auto-GEO forms the strongest baseline tier across nearly all dimensions, reflecting the effectiveness of explicitly extracted generative-engine preference rules in shaping citation- and visibilityoriented content. RAID yields limited gains in our simulation. This performance lag likely stems from its singular query trajectory—converging on one refined query from a single initial estimate —which fails to sufficiently span the latent queries or capture heterogeneous user expectations.

**中文**

值得注意的是，Auto-GEO 在几乎所有维度上形成了最强的基线层，反映了明确提取的生成式引擎偏好规则在塑造引文和可见性导向内容方面的有效性。在我们的模拟中，RAID 带来的收益有限。这种性能滞后可能源于其单一的查询轨迹（从单个初始估计收敛到一个精炼查询），它无法充分跨越潜在查询或捕获异构用户的期望。

### 段落 46 · Page 7

**EN**

Within GEO heuristics, evidence-driven strategies (e.g., CITE SOURCES, QUOTEADDITION) are consistently strongest, while lexical interventions (e.g., UNIQ. WORD) can even hurt performance. Robustness and stability.Beyond average gains, Table 2 reports stability summaries over the latent queries. IF-GEO achieves the best objective WCP and the lowest DR, indicating strong protection against query-specific regressions. Notably, a higher V AR does not necessarily imply worse tail stability, as variance captures both positive and negative dispersion. DR and WCP more directly characterize downside behavior across queries.

**中文**

在 GEO 启发法中，证据驱动的策略（例如 CITE SOURCES、QUOTEADDITION）始终是最强的，而词汇干预（例如 UNIQ.WORD）甚至会损害性能。鲁棒性和稳定性。除了平均增益之外，表 2 还报告了潜在查询的稳定性摘要。 IF-GEO 实现了最佳目标 WCP 和最低 DR，这表明针对特定于查询的回归提供了强大的保护。值得注意的是，较高的 VAR 并不一定意味着尾部稳定性较差，因为方差同时捕获了正离散度和负离散度。 DR 和 WCP 更直接地描述跨查询的负面行为。

### 段落 47 · Page 7

**EN**

While Auto-GEO is the strongest baseline on several tailoriented criteria, it still exhibits larger worst query drops than IF-GEO, and heuristic methods remain more brittle. Overall, these results confirm that explicitly coordinating revisions to resolve conflicts yields higher and safer holistic visibility than applying isolated, query-agnostic edits. 6.2 Ablation Study To quantify each component’s contribution, we ablate IF-GEO by removing conflict resolution, blueprint construction, or the entire instruction fusion stage (Phase II). Table 3 reveals a clear division of labor.

**中文**

虽然 Auto-GEO 是几个面向尾部的标准的最强基线，但它仍然表现出比 IF-GEO 更大的最差查询下降，并且启发式方法仍然更脆弱。总的来说，这些结果证实，与应用孤立的、与查询无关的编辑相比，显式协调修订来解决冲突可以产生更高、更安全的整体可见性。 6.2 消融研究为了量化每个组件的贡献，我们通过消除冲突解决、蓝图构建或整个指令融合阶段（第二阶段）来消融 IF-GEO。表3显示了明确的分工。

### 段落 48 · Page 7

**EN**

Conflict resolution acts as a safety guardrail: without it, incompatible queryspecific edits propagate into execution, producing the largest overall drop and the worst tail behavior (more negative WCP and higher DR). Instruction fusion is the main stabilizer across queries: removing it most strongly reduces reliability (WTR) and amplifies downside risk, consistent with uncoordinated local requests being redundant or misaligned when aggregated. In contrast, blueprint construction primarily affects gain realizability—removing it lowers the achievable overall score while leaving DR essentially unchanged.

**中文**

冲突解决充当安全护栏：没有它，不兼容的特定于查询的编辑会传播到执行中，从而产生最大的整体下降和最差的尾部行为（更负面的 WCP 和更高的 DR）。指令融合是跨查询的主要稳定器：删除它会极大地降低可靠性（WTR）并放大下行风险，这与聚合时不协调的本地请求冗余或不对齐一致。相比之下，蓝图构建主要影响增益的可实现性——删除它会降低可实现的总体得分，同时使 DR 基本保持不变。

### 段落 49 · Page 7

**EN**

Together, these results suggest a separation of concerns: conflict resolution and instruction fusion primarily affect stability across queries, while blueprint construction mainly improves the executability of the aggregated edits. 6.3 Impact of query expansion Size We examine the scaling behavior of IF-GEO by varying the number of expanded queries N∈ {1,3,5,7,9} while keeping other hyperparameters fixed. Figure 3 shows that increasing N yields consistent gains: the objective mean performance

**中文**

总之，这些结果表明关注点分离：冲突解决和指令融合主要影响跨查询的稳定性，而蓝图构建主要提高聚合编辑的可执行性。 6.3 查询扩展大小的影响 我们通过改变扩展查询的数量 N∈ {1,3,5,7,9} 同时保持其他超参数固定来检查 IF-GEO 的扩展行为。图 3 显示增加 N 会产生一致的增益：客观平均性能

### Page 8

### 段落 50 · Page 8

**EN**

Figure 3: Effect of query expansion size N on performance and stability. (a) Overall objective performance (Mean). (b) Win–tie rate (WTR). (c) Worst-case performance (WCP). (d) V olatility metrics: variance (V AR) and downside risk (DR; lower is better). Table 3: Ablation study of IF-GEO. We report the overall objective score (Mean) and stability metrics (V AR, WCP, WTR, DR) to demonstrate the contribution of each component. Variant Mean (↑)V AR (↓) WCP (↑) WTR (↑) DR (↓) IF-GEO (Full)9.24 0.0156 -0.032880.80%0.0021 w/o Blueprint 8.18 0.0167 -0.051781.20% 0.0021w/o Instru.

**中文**

图 3：查询扩展大小 N 对性能和稳定性的影响。 (a) 总体客观表现（平均值）。 (b) 平局胜率 (WTR)。 (c) 最坏情况表现（WCP）。 (d) 波动性指标：方差 (VAR) 和下行风险（DR；越低越好）。表 3：IF-GEO 的消融研究。我们报告总体目标得分（平均值）和稳定性指标（VAR、WCP、WTR、DR），以证明每个组件的贡献。变量平均值 (↑)VAR (↓) WCP (↑) WTR (↑) DR (↓) IF-GEO（完整）9.24 0.0156 -0.032880.80%0.0021 无蓝图 8.18 0.0167 -0.051781.20% 0.0021w/o 仪器

### 段落 51 · Page 8

**EN**

Fusion7.07 0.0156 -0.0569 74.80% 0.0043w/o Conflict Res.6.14 0.0174 -0.0713 77.20% 0.0032 rises monotonically from 8.06 at N=1 to 10.02 at N=9 (Figure 3a). Stability also improves overall as query coverage expands, with lower downside risk and less negative worst-case performance. However, these stability gains exhibit diminishing returns beyond N=5 (Figure 3b–d): WTR peaks at N=5 (80.00%) and then fluctuates, while DR and WCP change only marginally from N=5 to N=9.

**中文**

Fusion7.07 0.0156 -0.0569 74.80% 0.0043w/o 冲突 Res.6.14 0.0174 -0.0713 77.20% 0.0032 从 N=1 时的 8.06 单调上升到 N=9 时的 10.02（图 3a）。随着查询覆盖范围的扩大，稳定性也会整体提高，下行风险更低，最坏情况下的负面性能也更少。然而，这些稳定性增益在超过 N=5 时表现出收益递减（图 3b-d）：WTR 在 N=5 (80.00%) 时达到峰值，然后波动，而 DR 和 WCP 仅从 N=5 到 N=9 略有变化。

### 段落 52 · Page 8

**EN**

Since computation scales roughly linearly with N due to query generation and fusion overhead, we adopt N=5 as a balanced default that achieves near-peak stability with competitive gains at substantially lower latency. 6.4 Adaptability Analysis We further examine the adaptability of IF-GEO under two realistic variations: changing the underlying generative engine and varying the initial ranking of optimized documents. Cross-model generalization.We evaluate IF- GEO on a different generation model,Gemini- 2.0-Flash, without any method-specific tuning.

**中文**

由于查询生成和融合开销，计算量与 N 大致呈线性关系，因此我们采用 N=5 作为平衡默认值，可以在显着降低延迟的情况下实现接近峰值的稳定性和竞争优势。 6.4 适应性分析 我们进一步检验 IF-GEO 在两种现实变化下的适应性：改变底层生成式引擎和改变优化文档的初始排名。跨模型泛化。我们在不同的生成模型 Gemini-2.0-Flash 上评估 IF-GEO，无需任何特定于方法的调整。

### 段落 53 · Page 8

**EN**

As shown in Appendix E, IF-GEO consistently achieves the strongest objective gains and favorable stability profiles compared with all baselines. Notably, while Auto-GEO remains a competitive baseline by leveraging engine-specific preference rules, IF-GEO preserves its advantages in worstcase performance and win–tie rate, suggesting that explicit cross-query consolidation generalizes beyond a single generative engine. Sensitivity to initial document ranking.We further analyze IF-GEO by stratifying documents according to their initial ranking positions prior to optimization.

**中文**

如附录 E 所示，与所有基线相比，IF-GEO 始终实现了最强的目标收益和有利的稳定性。值得注意的是，虽然 Auto-GEO 通过利用特定于引擎的偏好规则仍然是有竞争力的基准，但 IF-GEO 保留了其在最坏情况性能和获胜率方面的优势，这表明显式跨查询整合可以推广到单个生成式引擎之外。对初始文档排名的敏感性。我们根据优化前的初始排名位置对文档进行分层，进一步分析 IF-GEO。

### 段落 54 · Page 8

**EN**

Results in Appendix D show that IF-GEO yields consistent improvements across all rank buckets, rather than concentrating gains on already well-ranked documents. In particular, both objective and subjective metrics indicate stable worst-case performance and low downside risk even for lower-ranked inputs, suggesting that IF-GEO improves content robustness rather than merely exploiting positional advantages. 7 Conclusion We study Generative Engine Optimization, aiming to improve a document’s visibility across a representative query set while maintaining cross-query stability.

**中文**

附录 D 中的结果表明，IF-GEO 在所有排名桶中产生了一致的改进，而不是将收益集中在已经排名良好的文档上。特别是，客观和主观指标都表明，即使对于排名较低的输入，最坏情况下的表现也很稳定，下行风险也较低，这表明 IF-GEO 提高了内容的稳健性，而不仅仅是利用位置优势。 7 结论 我们研究生成式引擎优化，旨在提高文档在代表性查询集中的可见性，同时保持跨查询稳定性。

### 段落 55 · Page 8

**EN**

We proposeIF-GEO, a “diverge-thenconverge” framework that discovers latent queries, elicits query-specific edit requests (instruction candidates), and fuses them via prioritization, deduplication, and conflict resolution into a unified, executable revision blueprint for blueprint-guided editing. Experiments on GEO-Bench under GPT-4omini show that IF-GEO surpasses strong baselines, achieving higher overall gains with lower downside risk. These results underscore the importance of explicitly coordinating competing revision signals for robust GEO beyond single-query tuning.

**中文**

我们提出了IF-GEO，一个“发散-然后聚合”框架，它发现潜在查询，引发特定于查询的编辑请求（候选指令），并通过优先级划分、重复数据删除和冲突解决将它们融合成统一的、可执行的修订蓝图，以进行蓝图引导编辑。 GPT-4omini 下的 GEO-Bench 实验表明，IF-GEO 超越了强大的基线，实现了更高的总体收益和更低的下行风险。这些结果强调了显式协调竞争修订信号对于超越单查询调整的稳健 GEO 的重要性。

### 段落 56 · Page 8

**EN**

8 Limitations Despite its effectiveness, our work has three main limitations. First,Inference Cost. The multi-stage “diverge-then-converge” workflow involves multiple LLM calls, resulting in higher token consumption than single-pass baselines. Second,Simulation Gap. Following standard GEO protocols, we

**中文**

8 局限性 尽管我们的工作很有效，但仍存在三个主要局限性。第一，推理成本。多阶段“发散然后聚合”工作流程涉及多个 LLM 调用，导致比单遍基线更高的令牌消耗。二、模拟差距。遵循标准 GEO 协议，我们

### Page 9

### 段落 57 · Page 9

**EN**

rely on LLM-simulated environments (e.g., GPT- 4o-mini). While reproducible, these simulations may not perfectly mirror the commercial engines. Third,Dependency on Query Discovery. The quality of the Global Revision Blueprint hinges on the representativeness of the mined queries. If the initial query expansion fails to capture the true latent search intent distribution, the subsequent optimization may be misaligned. References Pranjal Aggarwal, Vishvak Murahari, Tanmay Rajpurohit, Ashwin Kalyan, Karthik Narasimhan, and Ameet Deshpande. 2024. GEO: generative engine optimization.

**中文**

依赖于 LLM 模拟环境（例如 GPT-4o-mini）。虽然可重复，但这些模拟可能无法完美反映商业发动机。第三，对查询发现的依赖。全局修订蓝图的质量取决于所挖掘查询的代表性。如果初始查询扩展未能捕获真实的潜在搜索意图分布，则后续优化可能会出现偏差。参考文献 Pranjal Aggarwal、Vishvak Murahari、Tanmay Rajpurohit、Ashwin Kalyan、Karthik Narasimhan 和 Ameet Deshpande。 2024.GEO：生成式引擎优化。

### 段落 58 · Page 9

**EN**

InProceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining, KDD 2024, Barcelona, Spain, August 25-29, 2024, pages 5–16. ACM. Puneet S Bagga, Vivek F Farias, Tamar Korkotashvili, Tianyi Peng, and Yuhang Wu. 2025. E-geo: A testbed for generative engine optimization in e-commerce. arXiv preprint arXiv:2511.20867. Aharon Ben-Tal and Arkadi Nemirovski. 1998. Robust convex optimization.Mathematics of operations research, 23(4):769–805.

**中文**

第 30 届 ACM SIGKDD 知识发现和数据挖掘会议记录，KDD 2024，西班牙巴塞罗那，2024 年 8 月 25-29 日，第 5-16 页。 ACM。 Puneet S Bagga、Vivek F Farias、Tamar Korkotashvili、Tianyi Peng 和 Yuhang Wu。 2025. E-geo：电子商务生成式引擎优化的测试平台。 arXiv 预印本 arXiv：2511.20867。阿伦·本-塔尔和阿卡迪·涅米洛夫斯基。 1998. 鲁棒凸优化。运筹学数学，23(4):769–805。

### 段落 59 · Page 9

**EN**

Sebastian Borgeaud, Arthur Mensch, Jordan Hoffmann, Trevor Cai, Eliza Rutherford, Katie Millican, George van den Driessche, Jean-Baptiste Lespiau, Bogdan Damoc, Aidan Clark, Diego de Las Casas, Aurelia Guy, Jacob Menick, Roman Ring, Tom Hennigan, Saffron Huang, Loren Maggiore, Chris Jones, Albin Cassirer, and 9 others. 2022. Improving language models by retrieving from trillions of tokens. InInternational Conference on Machine Learning, ICML 2022, 17-23 July 2022, Baltimore, Maryland, USA, volume 162 ofProceedings of Machine Learning Research, pages 2206–2240. PMLR. Sergey Brin and Lawrence Page. 1998.

**中文**

Sebastian Borgeaud、Arthur Mensch、Jordan Hoffmann、Trevor Cai、Eliza Rutherford、Katie Millican、George van den Driessche、Jean-Baptiste Lespiau、Bogdan Damoc、Aidan Clark、Diego de Las Casas、Aurelia Guy、Jacob Menick、Roman Ring、Tom Hennigan、Saffron Huang、Loren Maggiore、Chris Jones、Albin Cassirer 和其他 9 人。 2022 年。通过检索数万亿个代币来改进语言模型。国际机器学习会议，ICML 2022，2022 年 7 月 17-23 日，美国马里兰州巴尔的摩，机器学习研究论文集第 162 卷，第 2206-2240 页。 PMLR。谢尔盖·布林和劳伦斯·佩奇。 1998.

### 段落 60 · Page 9

**EN**

The anatomy of a large-scale hypertextual web search engine.Comput. Networks, 30(1-7):107–117. Andrei Broder. 2002. A taxonomy of web search.SI- GIR Forum, 36(2):3–10. Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas. 2025a. Generative engine optimization: How to dominate AI search.CoRR, abs/2509.08919. Xiaolu Chen and Yong Liao. 2025. Caption injection for optimization in generative search engine.CoRR, abs/2511.04080. Xiaolu Chen, Haojie Wu, Jie Bao, Zhen Chen, Yong Liao, and Hu Huang. 2025b. Role-augmented intentdriven generative search engine optimization.CoRR, abs/2508.11158. Charles L. A. Clarke, Maheedhar Kolla, Gordon V .

**中文**

大规模超文本网络搜索引擎的剖析。计算。网络，30(1-7)：107–117。安德烈·布罗德。 2002 年。网络搜索分类法。SI-GIR 论坛，36(2):3–10。陈马赫、王晓轩、陈凯文和尼克·库达斯。 2025a。生成式引擎优化：如何主导人工智能搜索。CoRR，abs/2509.08919。陈晓璐、廖勇。 2025.用于生成式搜索引擎优化的标题注入。CoRR，abs/2511.04080。陈晓璐、吴浩杰、鲍杰、陈震、廖勇和黄胡。 2025b。角色增强意图驱动生成式搜索引擎优化。CoRR，abs/2508.11158。查尔斯·L·A·克拉克、马希达尔·科拉、戈登·V。

### 段落 61 · Page 9

**EN**

Cormack, Olga Vechtomova, Azin Ashkan, Stefan Büttcher, and Ian MacKinnon. 2008. Novelty and diversity in information retrieval evaluation. InProceedings of the 31st Annual International ACM SI- GIR Conference on Research and Development in Information Retrieval, SIGIR 2008, Singapore, July 20-24, 2008, pages 659–666. ACM. Tianyu Gao, Howard Yen, Jiatong Yu, and Danqi Chen. 2023. Enabling large language models to generate text with citations. InProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6- 10, 2023, pages 6465–6488. Association for Computational Linguistics.

**中文**

科马克、奥尔加·维奇托莫娃、阿津·阿什坎、斯特凡·布彻和伊恩·麦金农。 2008。信息检索评估的新颖性和多样性。第 31 届国际 ACM SI-GIR 信息检索研究与开发年度会议论文集，SIGIR 2008，新加坡，2008 年 7 月 20-24 日，第 659-666 页。 ACM。高天宇、甄子丹、于佳桐和陈丹琪。 2023. 使大型语言模型能够生成带有引文的文本。 2023 年自然语言处理经验方法会议论文集，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，第 6465-6488 页。计算语言学协会。

### 段落 62 · Page 9

**EN**

Jeffrey L. Gleason, Desheng Hu, Ronald E. Robertson, and Christo Wilson. 2023. Google the gatekeeper: How search components affect clicks and attention. InProceedings of the Seventeenth International AAAI Conference on Web and Social Media, ICWSM 2023, Limassol, Cyprus, June 5-8, 2023, pages 245–256. AAAI Press. Kelvin Guu, Kenton Lee, Zora Tung, Panupong Pasupat, and Ming-Wei Chang. 2020. REALM: retrievalaugmented language model pre-training. volume abs/2002.08909. Gautier Izacard and Edouard Grave. 2021. Leveraging passage retrieval with generative models for open domain question answering.

**中文**

杰弗里·L·格里森、胡德胜、罗纳德·E·罗伯逊和克里斯托·威尔逊。 2023. 谷歌看门人：搜索组件如何影响点击和注意力。第十七届国际 AAAI 网络和社交媒体会议记录，ICWSM 2023，塞浦路斯利马索尔，2023 年 6 月 5-8 日，第 245-256 页。 AAAI出版社。 Kelvin Guu、Kenton Lee、Zora Tung、Panupong Pasupat 和 Ming-Wei Chang。 2020. REALM：检索增强语言模型预训练。卷ABS/2002.08909。戈蒂埃·伊扎卡尔和爱德华·格雷夫。 2021 年。利用段落检索和生成模型进行开放域问答。

### 段落 63 · Page 9

**EN**

InProceedings of the 16th Conference of the European Chapter of the Association for Computational Linguistics: Main Volume, EACL 2021, Online, April 19 - 23, 2021, pages 874– 880. Association for Computational Linguistics. Vladimir Karpukhin, Barlas Oguz, Sewon Min, Patrick Lewis, Ledell Wu, Sergey Edunov, Danqi Chen, and Wen-tau Yih. 2020. Dense passage retrieval for opendomain question answering. InProceedings of the 2020 Conference on Empirical Methods in Natural Language Processing, EMNLP 2020, Online, November 16-20, 2020, pages 6769–6781. Association for Computational Linguistics.

**中文**

计算语言学协会欧洲分会第 16 届会议记录：主卷，EACL 2021，在线，2021 年 4 月 19 日至 23 日，第 874–880 页。计算语言学协会。 Vladimir Karpukhin、Barlas Oguz、Sewon Min、Patrick Lewis、Ledell Wu、Sergey Edunov、Danqi Chen 和 Wen-tau Yih。 2020.用于开放域问答的密集段落检索。 2020 年自然语言处理经验方法会议论文集，EMNLP 2020，在线，2020 年 11 月 16-20 日，第 6769-6781 页。计算语言学协会。

### 段落 64 · Page 9

**EN**

Patrick Lewis, Ethan Perez, Aleksandra Piktus, Fabio Petroni, Vladimir Karpukhin, Naman Goyal, Heinrich Küttler, Mike Lewis, Wen-tau Yih, Tim Rocktäschel, Sebastian Riedel, and Douwe Kiela. 2020. Retrieval-augmented generation for knowledgeintensive NLP tasks. InAdvances in Neural Information Processing Systems 33: Annual Conference on Neural Information Processing Systems 2020, NeurIPS 2020, December 6-12, 2020, virtual. Xiaoxi Li, Jiajie Jin, Yujia Zhou, Yuyao Zhang, Peitian Zhang, Yutao Zhu, and Zhicheng Dou. 2025. From matching to generation: A survey on generative information retrieval.ACM Trans. Inf. Syst., 43(3):83:1– 83:62.

**中文**

帕特里克·刘易斯、伊桑·佩雷斯、亚历山大·皮克图斯、法比奥·佩特罗尼、弗拉基米尔·卡普欣、纳曼·戈亚尔、海因里希·库特勒、迈克·刘易斯、叶文涛、蒂姆·洛克塔舍尔、塞巴斯蒂安·里德尔和杜威·基拉。 2020.知识密集型 NLP 任务的检索增强生成。神经信息处理系统进展 33：2020 年神经信息处理系统年会，NeurIPS 2020，2020 年 12 月 6-12 日，虚拟。李晓曦、金佳杰、周雨佳、张玉瑶、张培田、朱玉涛和窦志成。 2025.从匹配到生成：生成信息检索调查。ACM Trans。信息。系统，43（3）：83：1-83：62。

### 段落 65 · Page 9

**EN**

Yang Liu, Dan Iter, Yichong Xu, Shuohang Wang, Ruochen Xu, and Chenguang Zhu. 2023. G-eval:

**中文**

刘阳、丹·伊特尔、徐一冲、王硕航、徐若晨和朱晨光。 2023.G-评估：

### Page 10

### 段落 66 · Page 10

**EN**

NLG evaluation using gpt-4 with better human alignment. InProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6-10, 2023, pages 2511–2522. Association for Computational Linguistics. Florian Lüttgenau, Imar Colic, and Gervasio Ramirez. 2025. Beyond SEO: A transformer-based approach for reinventing web content optimisation.CoRR, abs/2507.03169. Chokri Mamoghli and Sami Daboussi. 2009. Performance measurement of hedge funds portfolios in a downside risk framework.The Journal of Wealth Management, 12(2):101. R Timothy Marler and Jasbir S Arora. 2004.

**中文**

使用 gpt-4 进行 NLG 评估，具有更好的人体对齐能力。 2023 年自然语言处理经验方法会议论文集，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，第 2511-2522 页。计算语言学协会。弗洛里安·吕特格瑙、伊马尔·科利奇和杰瓦西奥·拉米雷斯。 2025。超越 SEO：一种基于Transformer的方法，用于重新发明网络内容优化。CoRR，abs/2507.03169。乔克里·马莫格利和萨米·达布西。 2009 年。下行风险框架中对冲基金投资组合的绩效衡量。《财富管理杂志》，12(2):101。 R 蒂莫西·马勒 (R Timothy Marler) 和贾斯比尔·S 阿罗拉 (Jasbir S Arora)。 2004年。

### 段落 67 · Page 10

**EN**

Survey of multi-objective optimization methods for engineering.Structural and multidisciplinary optimization, 26(6):369–395. Jacob Menick, Maja Trebacz, Vladimir Mikulik, John Aslanides, H. Francis Song, Martin J. Chadwick, Mia Glaese, Susannah Young, Lucy Campbell- Gillingham, Geoffrey Irving, and Nat McAleese. 2022. Teaching language models to support answers with verified quotes.CoRR, abs/2203.11147.

**中文**

工程多目标优化方法综述。结构和多学科优化，26（6）：369–395。 Jacob Menick、Maja Trebacz、Vladimir Mikulik、John Aslanides、H. Francis Song、Martin J. Chadwick、Mia Glaese、Susannah Young、Lucy Campbell-Gillingham、Geoffrey Irving 和 Nat McAleese。 2022。教学语言模型以支持经过验证的引用的答案。CoRR，abs/2203.11147。

### 段落 68 · Page 10

**EN**

Reiichiro Nakano, Jacob Hilton, Suchir Balaji, Jeff Wu, Long Ouyang, Christina Kim, Christopher Hesse, Shantanu Jain, Vineet Kosaraju, William Saunders, Xu Jiang, Karl Cobbe, Tyna Eloundou, Gretchen Krueger, Kevin Button, Matthew Knight, Benjamin Chess, and John Schulman. 2021. Webgpt: Browserassisted question-answering with human feedback. CoRR, abs/2112.09332. Filip Radlinski, Madhu Kurup, and Thorsten Joachims. 2008. How does clickthrough data reflect retrieval quality? InProceedings of the 17th ACM Conference on Information and Knowledge Management, CIKM 2008, Napa Valley, California, USA, October 26-30, 2008, pages 43–52. ACM. Daniel E.

**中文**

Reiichiro Nakano、Jacob Hilton、Sucher Balaji、Jeff Wu、Long Ouyang、Christina Kim、Christopher Hesse、Shantanu Jain、Vineet Kosaraju、William Saunders、徐江、Karl Cobbe、Tyna Eloundou、Gretchen Krueger、Kevin Button、Matthew Knight、Benjamin Chess 和 John Schulman。 2021.Webgpt：浏览器辅助问答与人类反馈。 CoRR，abs/2112.09332。菲利普·拉德林斯基、马杜·库鲁普和托尔斯滕·约阿希姆斯。 2008.点击率数据如何反映检索质量？第 17 届 ACM 信息和知识管理会议记录，CIKM 2008，美国加利福尼亚州纳帕谷，2008 年 10 月 26-30 日，第 43-52 页。 ACM。丹尼尔·E。

### 段落 69 · Page 10

**EN**

Rose and Danny Levinson. 2004. Understanding user goals in web search. InProceedings of the 13th international conference on World Wide Web, WWW 2004, New York, NY, USA, May 17-20, 2004, pages 13–19. ACM. Xuanhui Wang, Deepayan Chakrabarti, and Kunal Punera. 2009. Mining broad latent query aspects from search sessions. InProceedings of the 15th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, Paris, France, June 28 - July 1, 2009, pages 867–876. ACM. Yujiang Wu, Shanshan Zhong, Yubin Kim, and Chenyan Xiong. 2025. What generative search engines like and how to optimize web content cooperatively. CoRR, abs/2510.11438.

**中文**

罗斯和丹尼·莱文森。 2004 年。了解网络搜索中的用户目标。第 13 届万维网国际会议记录，WWW 2004，美国纽约州纽约市，2004 年 5 月 17-20 日，第 13-19 页。 ACM。王宣辉、Deepayan Chakrabarti 和 Kunal Punera。 2009。从搜索会话中挖掘广泛的潜在查询方面。第 15 届 ACM SIGKDD 国际知识发现和数据挖掘会议记录，法国巴黎，2009 年 6 月 28 日至 7 月 1 日，第 867-876 页。 ACM。吴玉江，钟珊珊，金玉斌，熊陈艳。 2025. 生成式搜索引擎喜欢什么以及如何协同优化网页内容。 CoRR，abs/2510.11438。

### 段落 70 · Page 10

**EN**

A Multi-query Competition Diagnostic This appendix reports a diagnostic experiment that empirically examines the competitive effects induced byper-query tuningin Multi-query GEO. The purpose is not to compare IF-GEO with baselines, but to provide quantitative evidence for the motivation that optimizing a document for one query can concentrate gains on that query and yield uneven outcomes across the remaining queries. Experimental Setup.We use the same dataset, query sets, and evaluation pipeline as in the main experiments.

**中文**

多查询竞争诊断本附录报告了一个诊断实验，该实验凭经验检查多查询 GEO 中每个查询调整引起的竞争效应。目的不是将 IF-GEO 与基线进行比较，而是提供定量证据，证明优化一个查询的文档可以将收益集中在该查询上，并在其余查询中产生不均匀的结果。实验设置。我们使用与主要实验相同的数据集、查询集和评估管道。

### 段落 71 · Page 10

**EN**

Each instance contains one document and a representative query set of fixed size K=5 (constructed following the GEO-Bench setting), with no additional filtering or re-sampling. For each document, we elicit query-conditioned edit requests independently for all queries using the same request format as IF-GEO. We then uniformly sample one query as the target i∗ and perform a single per-query optimization pass that rewrites the document using only the requests associated with i∗. No information from the other queries is used during rewriting, and no cross-query fusion is performed.

**中文**

每个实例包含一个文档和一个固定大小 K=5 的代表性查询集（根据 GEO-Bench 设置构建），无需额外的过滤或重新采样。对于每个文档，我们使用与 IF-GEO 相同的请求格式独立地为所有查询引出查询条件编辑请求。然后，我们统一采样一个查询作为目标 i*，并执行单个每个查询优化过程，仅使用与 i* 关联的请求重写文档。重写期间不使用来自其他查询的信息，并且不执行跨查询融合。

### 段落 72 · Page 10

**EN**

We evaluate visibility before and after per-query tuning under all K queries using the primary objective visibility metric (Obj. Overall), following the definitions in Section 5.3. Metrics.We report three statistics for each category: (i)Mean Gain, the average visibility improvement; (ii) P(gain<0) , the rate of negative gain; and (iii)Downside Magnitude (DM), defined as E[−min(0,gain)] , which measures the expected magnitude of negative outcomes. DM is an interpretableL1analogue of the main-text downside risk metric DR (which squares negative gains), and is reported here only for diagnostic analysis.

**中文**

我们按照第 5.3 节中的定义，使用主要目标可见性指标（Obj.Overall）评估所有 K 个查询下的每个查询调整之前和之后的可见性。指标。我们为每个类别报告三个统计数据：(i) 平均增益，平均可见性改进； (ii) P(gain<0)，负增益率； (iii) 下行幅度 (DM)，定义为 E[−min(0,gain)]，衡量负面结果的预期幅度。 DM 是正文下行风险指标 DR（负收益的平方）的可解释的 L1 模拟，此处报告仅用于诊断分析。

### 段落 73 · Page 10

**EN**

For relative spillover, we compute the same statistics overr j. Results.Table 4 summarizes the outcomes over 202 records (200 documents, 808 (i∗, j) pairs) under the primary objective metric (Obj. Overall). per-query tuning exhibits a clear asymmetric improvement pattern across the query set. The optimized (target) query i∗ achieves a substantially larger mean gain (0.277), with a relatively low negative-gain rate ( P(gain<0) = 0.124 ) and small downside magnitude (DM=0.017). In contrast, the non-target queries (j̸=i ∗) show weaker and less reliable improvements: while the mean

**中文**

对于相对溢出，我们计算 r j 上的相同统计数据。结果。表 4 总结了主要目标指标（目标总体）下 202 条记录（200 个文档，808 个 (i*, j) 对）的结果。每个查询的调优在整个查询集中表现出明显的不对称改进模式。优化后的（目标）查询 i* 实现了更大的平均增益 (0.277)，具有相对较低的负增益率 ( P(gain<0) = 0.124 ) 和较小的下行幅度 (DM=0.017)。相比之下，非目标查询 (j̸=i ∗) 显示出较弱且不太可靠的改进：而均值

### Page 11

### 段落 74 · Page 11

**EN**

Table 4: Gain allocation skew under per-query tuning (primary objective metric, Obj. Overall). We report mean gain, the negative-gain rate P(gain<0) , and downside magnitude (DM) for the optimized query (i∗), the non-target queries ( j̸=i ∗), and relative spillover (rj), aggregated over all(i ∗, j)pairs. Mean GainP(gain<0)DM Optimized query 0.277 0.124 0.017 Non-target queries 0.087 0.306 0.036 Relative spillover -0.189 0.692 0.228 gain remains positive (0.087), the negative-gain rate more than doubles (0.306) and DM increases to 0.036. Relative spillover further indicates systematic concentration of gains on the target query.

**中文**

表 4：每个查询调整下的增益分配偏差（主要目标指标，Obj. 总体）。我们报告优化查询 (i*)、非目标查询 (j̸=i*) 的平均增益、负增益率 P(gain<0) 和下行幅度 (DM)，以及相对溢出 (rj)，在所有 (i*, j) 对上聚合。平均 GainP(gain<0)DM 优化查询 0.277 0.124 0.017 非目标查询 0.087 0.306 0.036 相对溢出 -0.189 0.692 0.228 增益保持正值 (0.087)，负增益率增加一倍以上 (0.306)，DM ​​增加到 0.036。相对溢出进一步表明目标查询上的收益系统集中。

### 段落 75 · Page 11

**EN**

On average, non-target queries lag behind the optimized query by 0.189 (mean spillover=−0.189), and in 69.2% of query pairs the spillover is negative (P(r j <0) = 0.692 ). Moreover, the large spillover downside magnitude (DM=0.228) suggests that when non-target queries fall behind, the gap is often substantial rather than marginal. Discussion.Overall, this diagnostic indicates that single-query tuning primarily induces a pronounced gain allocation skew within the representative query set.

**中文**

平均而言，非目标查询落后于优化查询 0.189（平均溢出=−0.189），并且在 69.2% 的查询对中溢出为负（P(r j <0) = 0.692 ）。此外，巨大的溢出下行幅度（DM = 0.228）表明，当非目标查询落后时，差距通常很大而不是很小。讨论。总体而言，此诊断表明单查询调整主要会在代表性查询集中引起明显的增益分配偏差。

### 段落 76 · Page 11

**EN**

Rather than causing pervasive absolute degradation on other queries, it tends to concentrate improvements on the optimized query while leaving the remaining queries with smaller and notably less stable benefits. This pattern motivates the need forglobal coordinationover the query set—to achieve reliable and well-distributed improvements under a shared content budget—as pursued by IF-GEO in the main method. B Prompts Used in IF-GEO This section documents the main prompts used in IF-GEO. All prompts are shown in their original form to ensure full transparency and reproducibility.

**中文**

它不会对其他查询造成普遍的绝对降级，而是倾向于将改进集中在优化的查询上，同时使其余查询获得较小且明显不太稳定的好处。这种模式激发了对查询集进行全局协调的需求，以在共享内容预算下实现可靠​​且分布均匀的改进，正如 IF-GEO 在主要方法中所追求的那样。 B IF-GEO 中使用的提示 本节介绍 IF-GEO 中使用的主要提示。所有提示均以其原始形式显示，以确保完全透明和可重复性。

### 段落 77 · Page 11

**EN**

They correspond to different steps of the IF-GEO pipeline and are executed sequentially. Query Mining. System Prompt: You are a search log analyst. You study how real users search on the web. Your task is to infer what queries users are most likely to type when they are trying to find or understand the content of a given webpage. Task Description: Based on the webpage content provided by the user, inferrealistic search queriesthat would naturally lead them to this page. Your Goals: • Generate{num_queries} queriesthat reflect different aspects of the main theme. • Focus on the central topic,not specific details(e.g., trivial facts).

**中文**

它们对应于 IF-GEO 管道的不同步骤并按顺序执行。查询挖掘。系统提示：您是搜索日志分析师。您研究真实用户如何在网络上搜索。您的任务是推断用户在尝试查找或理解给定网页的内容时最有可能键入哪些查询。任务描述：根据用户提供的网页内容，不切实际的搜索查询自然会将他们引导至此页面。您的目标： • 生成反映主题不同方面的{num_queries} 个查询。 • 关注中心主题，而不是具体细节（例如琐碎的事实）。

### 段落 78 · Page 11

**EN**

• Ensure queries arenatural,diverse, andnot simple paraphrases. • For each query, estimate aprobability score (0–100) reflecting real-world likelihood. Output Format: You must return ONLY a valid JSON object. Do not include markdown formatting or any other text. The format must be exactly: { "queries": [ { "query": "the inferred user query string", "probability": 85 } ] } Query-specific Request Generation. System Prompt: You are an assistant who reviews how well a given webpage can answer a specific user query. Your goal is to identify concrete weaknesses in the webpage and propose clear, actionable revision suggestions.

**中文**

• 确保查询自然、多样化，而不是简单的释义。 • 对于每个查询，估计反映现实世界可能性的概率分数(0–100)。输出格式：您必须仅返回有效的 JSON 对象。请勿包含 Markdown 格式或任何其他文本。格式必须完全符合： { "queries": [ { "query": "the inferred user query string", "probability": 85 } ] } 特定于查询的请求生成。系统提示：您是一名助理，负责检查给定网页对特定用户查询的回答能力。您的目标是找出网页中的具体弱点，并提出清晰、可操作的修改建议。

### 段落 79 · Page 11

**EN**

Task Description: You will receive auser queryand awebpage text. Your task: • Evaluate how well the webpage text could answer the query. • Identifyspecific weaknessesin the text that may prevent a strong answer. • Produceup to {suggestions_num} revision suggestionsthat would improve the webpage’s ability to answer the query. Requirements for Each Suggestion: • Target Specificity:Refer to aspecific part, sentence, or paragraphof the webpage. • Excerpt:Include ashort excerpt(quoted or partially quoted) to make the target explicit. •Actionable:Describehow to modifythat part (e.g., add missing details, clarify wording, restructure, simplify).

**中文**

任务描述：您将收到用户查询和网页文本。您的任务： • 评估网页文本回答查询的效果。 • 找出文本中可能妨碍给出有力答案的具体弱点。 • 生成最多 {suggestions_num} 条修订建议，以提高网页回答查询的能力。每个建议的要求： • 目标特异性：指网页的特定部分、句子或段落。 • 摘录：包括简短的摘录（引用或部分引用）以使目标明确。 • 可操作的：描述如何修改该部分（例如，添加缺失的细节、澄清措辞、重组、简化）。

### 段落 80 · Page 11

**EN**

•Necessity Score:Include anecessity score (0–100) indicating importance for answering the query. Output Format (JSON Only): Return ONLY a valid JSON object. Do not include markdown formatting or any other text. The format must be exactly: { "suggestions": [ { "excerpt": "short excerpt", "suggestion": "revision details", "necessity": 85 } ] }

**中文**

•必要性分数：包括表明回答查询的重要性的必要性分数（0-100）。输出格式（仅限 JSON）：仅返回有效的 JSON 对象。请勿包含 Markdown 格式或任何其他文本。格式必须完全正确： { "suggestions": [ { "excerpt": "short excerpt", "suggestion": "revision details", "necessity": 85 } ] }

### Page 12

### 段落 81 · Page 12

**EN**

Prioritization and Deduplication. System Prompt: You are a Senior Editor consolidating feedback from multiple readers. Task: You are provided with a list of revision suggestions grouped by user queries. Your goal is toflattenthis list andmergeduplicate suggestions that target the same content or issue. Rules: •De-duplicate:Merge suggestions ONLY if they target thesame semantic topicAND apply to the same approximate location (excerpt)in the text. –Constraint:Do NOT merge suggestions that target widely separated paragraphs (e.g., “Intro” vs “Conclusion”), even if they are thematically related.

**中文**

优先级和重复数据删除。系统提示：您是一名高级编辑，正在整合多位读者的反馈。任务：向您提供按用户查询分组的修订建议列表。您的目标是压平此列表并合并针对相同内容或问题的重复建议。规则： • 去重复：仅当建议针对同一语义主题并且适用于文本中的相同大致位置（摘录）时才合并建议。 –约束：不要合并针对广泛分离的段落的建议（例如，“介绍”与“结论”），即使它们在主题上相关。

### 段落 82 · Page 12

**EN**

Keep them as separate items with the same topic tag. •Filter:Discard suggestions withnecessity<60 unless they address a critical factual error. •Standardize:Output a flat list. Assign a shorttopic tag to each. Output Format (JSON Only): Return ONLY a valid JSON list. Do not include markdown formatting. Example: [ { "id": "suggest_1", "topic": "eg.Comparison Table", "excerpt": "short excerpt", "suggestion": "modify-suggestion content", "necessity": 95 } ] Conflict Resolution. System Prompt: You are a Logic Arbiter resolving content revision conflicts. Task: Examine the provided list of suggestions.

**中文**

将它们保留为具有相同主题标签的单独项目。 •过滤器：丢弃必要性<60的建议，除非它们解决了关键的事实错误。 •标准化：输出一个平面列表。为每个主题分配一个短主题标签。输出格式（仅限 JSON）：仅返回有效的 JSON 列表。不包括 Markdown 格式。示例： [ { "id": "suggest_1", "topic": "eg.Comparison Table", "excerpt": "short excerpt", "suggestion": "modify-suggestion content", "necessity": 95 } ] 冲突解决。系统提示：您是解决内容修订冲突的逻辑仲裁者。任务：检查提供的建议列表。

### 段落 83 · Page 12

**EN**

Detect logical conflicts (where two or more suggestions cannot be simultaneously implemented) and resolve them according to the following priority-based rules. Rules: •Detect Conflicts:Look for instructions targeting the sameexcerptor topic that are mutually exclusive (e.g., “Delete section” vs “Expand section”). •Resolve: –If conflict exists, prioritize the instruction with highernecessity. –If instructions are compatible (e.g., “Shorten text” AND “Add link”), combine them into one instruction. •Output:A final, clean list of instructions. Output Format (JSON Only): Return ONLY a valid JSON list. Do not include markdown formatting.

**中文**

检测逻辑冲突（两个或多个建议无法同时实施）并根据以下基于优先级的规则解决它们。规则： •检测冲突：查找针对相同摘录器主题且互斥的指令（例如，“删除部分”与“扩展部分”）。 • 解决： – 如果存在冲突，请优先考虑必要性较高的指令。 –如果指令兼容（例如，“缩短文本”和“添加链接”），请将它们合并为一条指令。 •输出：最终的、干净的指令列表。输出格式（仅限 JSON）：仅返回有效的 JSON 列表。不包括 Markdown 格式。

### 段落 84 · Page 12

**EN**

Example: [ { "id": "suggest_1", "excerpt": "original excerpt", "suggestion": "instruction text..." } ] Blueprint Construction. System Prompt: You are a Content Architect & Strategist. Task: You are given a webpage and a set of logic-checked revision instructions. Your goal is to create aMaster Revision Planthat maps these instructions to the webpage structure. Process: •Analyze Structure:Read the webpage to understand its current flow (Intro→Body→Conclusion). •Map & Group:Assign each instruction to a specific logical section of the webpage.

**中文**

示例： [ { "id": "suggest_1", "excerpt": "原始摘录", "suggestion": "说明文本..." } ] 蓝图构建。系统提示：您是内容架构师和策略师。任务：向您提供一个网页和一组经过逻辑检查的修订说明。您的目标是创建一个主修订计划，将这些说明映射到网页结构。流程： •分析结构：阅读网页以了解其当前流程（简介→正文→结论）。 •地图和分组：将每条指令分配给网页的特定逻辑部分。

### 段落 85 · Page 12

**EN**

– If multiple instructions target the same section (e.g., “Add history” and “Fix grammar” both in Intro), GROUPthem into one plan item. –If an instruction requires a new section, decide the best insertion point to maintain flow. •Plan:Output a structured blueprint. Output Format (JSON Only): Return ONLY a valid JSON object. Do not include markdown formatting. Example: { "revision_blueprint": [ { "section_name": "Introduction", "target_location": "...", "modification_intent": "...", "directives": [ "Integrate instruction #1: ...", "Integrate instruction #5: ..." ], "format_note": "Keep as text paragraphs." } ] } Blueprint-Guided Revision.

**中文**

– 如果多个指令针对同一部分（例如，简介中的“添加历史记录”和“修复语法”），请将它们分组到一个计划项目中。 –如果指令需要新的部分，请确定最佳插入点以维持流程。 •计划：输出结构化的蓝图。输出格式（仅限 JSON）：仅返回有效的 JSON 对象。不包括 Markdown 格式。示例： { "revision_blueprint": [ { "section_name": "Introduction", "target_location": "...", "modification_intent": "...", "directives": [ "Integrate instructions #1: ...", "Integrate instructions #5: ..." ], "format_note": "保留为文本段落。" } ] } 蓝图指导修订。

### 段落 86 · Page 12

**EN**

System Prompt: You are an expert Content Engineer and GEO (Generative Engine Optimization) Specialist. Task: Your task is to rewrite a given webpage content by strictly following a provided “Revision Blueprint”. Rules: • Full Output:You must output theENTIRErewritten webpage. Do not summarize, do not omit sections, and do not use placeholders like “[...rest of text remains same...]”. •Strict Execution:Implement every directive in the Blueprint (e.g., inserting tables, adding links, rewriting paragraphs, adding new sections). •Preservation:For sections NOT mentioned in the Blueprint, preserve the original text and structure exactly as is.

**中文**

系统提示：您是一位内容工程师和GEO（生成式引擎优化）专家。任务：您的任务是严格按照提供的“修订蓝图”重写给定的网页内容。规则： • 完整输出：您必须输出整个重写的网页。不要总结，不要省略部分，也不要使用“[...其余文本保持不变...]”等占位符。 •严格执行：实现蓝图中的每个指令（例如，插入表格、添加链接、重写段落、添加新部分）。 •保留：蓝图中未提及的部分，原样保留原文和结构。

### 段落 87 · Page 12

**EN**

•Formatting:Use standard Markdown. If the Blueprint asks for a table, render a valid Markdown table. •Tone:If the Blueprint specifies a tone change (e.g., “professional”), apply it effectively to the target

**中文**

•格式：使用标准Markdown。如果蓝图需要表格，则渲染有效的 Markdown 表格。 •语气：如果蓝图指定了语气变化（例如“专业”），则将其有效地应用于目标

### Page 13

### 段落 88 · Page 13

**EN**

section. Output: Return only the final rewritten content in Markdown format. C Qualitative Case Study This appendix presents one end-to-end example, organized by IF-GEO steps. For readability, we use ellipses (. . . ) to indicate omitted spans. C.1 Input Document We start from the original document snippet, where terminology aroundcoagulopathyis easy to misinterpret without careful disambiguation. Document snippet “Coagulopathy is a condition in which the blood’s ability to for. . . , leading to a tendency towards prolonged or excessive bleeding. It can occur spontaneously or following an injury or medical procedure. . . .

**中文**

部分。输出：仅以 Markdown 格式返回最终重写的内容。 C 定性案例研究 本附录介绍了一个端到端示例，按 IF-GEO 步骤组织。为了便于阅读，我们使用省略号 (...) 来表示省略的范围。 C.1 输入文档 我们从原始文档片段开始，其中有关凝血病的术语如果不仔细消除歧义很容易被误解。文件片段“凝血病是一种血液能力......导致长期或过度出血倾向的病症。它可以自发发生，也可以在受伤或医疗程序后发生......

### 段落 89 · Page 13

**EN**

Coagulopathies are sometimes mistakenly referred to as ‘clotti. . . haracterized by a predisposition to excessive clot formation. . . . ” C.2 Query Mining IF-GEO first mines a diverse query set (queries) that could reasonably lead to the document, with associated weights (here shown as probabilities). •what is coagulopathy and its symptoms (p=0.90) •causes and treatment options for coagulopathy(p=0.85) •how does coagulopathy affect bleeding risk (p=0.80) •difference between coagulopathy and clotting disorders(p=0.75) •emergency management of coagulopathy in trauma patients(p=0.70) C.3 Query-specific Request Generation.

**中文**

凝血病有时被错误地称为“凝血病”。。。其特点是容易形成过多的血栓。。。。 C.2 查询挖掘 IF-GEO 首先挖掘一个多样化的查询集（查询），这些查询集可以合理地导出文档，并具有相关的权重（此处显示为概率）。 • 什么是凝血障碍及其症状 (p=0.90) • 凝血障碍的原因和治疗选择 (p=0.85) • 凝血障碍如何影响出血风险 (p=0.80) • 凝血障碍与凝血障碍之间的差异 (p=0.75) • 创伤患者凝血障碍的紧急处理 (p=0.70) C.3 特定查询请求生成。

### 段落 90 · Page 13

**EN**

Given each query, the system generates localized edit requests. Here we show the merged pool of core suggestions before conflict-aware instruction fusion. •Excerpt:Coagulopathy is a condition in which the blood’s ability to form clots is impaired. . . Suggestion:Simplify this definition to make it more accessible. For example. . . bleeding.’ This will help readers grasp the concept more easily. Necessity:75 •Excerpt:Coagulopathies are sometimes mistakenly referred. . . as ‘clotting disorders, ’ but they are actually the opposite. . . Suggestion:Provide a brief explanation or definition of ‘clotting disorders’. . .

**中文**

对于每个查询，系统都会生成本地化的编辑请求。在这里，我们展示了冲突感知指令融合之前的核心建议合并池。 •摘录：凝血病是一种血液形成凝块的能力受损的病症。。。建议：简化此定义，使其更易于理解。例如。。。出血。”这将帮助读者更容易GEO解这个概念。必要性：75 •摘录：有时会错误地提及凝血病。。。被称为“凝血障碍”，但实际上恰恰相反。。。建议：提供“凝血障碍”的简要解释或定义。。。

### 段落 91 · Page 13

**EN**

coagulopathy is the opposite of what they may mistakenly believe. Necessity:70 •Excerpt:Coagulopathies are sometimes mistakenly referred. . . , characterized by a predisposition to excessive clot formation. Suggestion:Clarify the distinction between coagulopathy and clotting disord. . . rs understand why coagulopathy leads to increased bleeding risk. Necessity:80 •Excerpt:Coagulopathies are sometimes mistakenly referred to as “clotti. . . , characterized by a predisposition to excessive clot formation. Suggestion:Clarify the distinction between coagulopathy and clotting disord. . .

**中文**

凝血障碍与他们可能错误地认为的相反。必要性：70 •摘录：有时会错误地提及凝血病。。。，其特征是容易形成过多的凝块。建议：明确凝血病和凝血障碍之间的区别。。。人们了解为什么凝血障碍会导致出血风险增加。必要性：80 •摘录：凝血病有时被错误地称为“血栓……，其特征是容易形成过多的血栓。建议：澄清凝血病和凝血障碍之间的区别……”

### 段落 92 · Page 13

**EN**

te clot formation and explain how they differ from coagulopathy. Necessity:90 C.4 Conflict-Aware Instruction Fusion Multiple suggestions target overlapping anchors but imply incompatible framing. IF-GEO resolves these conflicts by producing a compact, globally consistent revision blueprint. Section name:Definition and Terminology Clarification Target location:The opening definition sentence starting with . . . followed by the sentence mentioning ‘clotting disorders’ . . . Modification intent:Make the lead definition more accessible w. . . biguation and unifying terminology to prevent misinterpretation. Directives: 1.

**中文**

凝块形成并解释它们与凝血病有何不同。必要性：90 C.4 冲突感知指令融合 多个建议针对重叠锚点，但暗示框架不兼容。 IF-GEO 通过制定紧凑的、全球一致的修订蓝图来解决这些冲突。章节名称：定义和术语澄清 目标位置：以 开头的定义语句。。。接下来是提到“凝血障碍”的句子。。。修改意图：使引线定义更易于理解。。。歧义和统一术语以防止误解。指令：1。

### 段落 93 · Page 13

**EN**

Integrate instruction #1: Rewrite the opening definitio. . . ding multi-term contrasts inside this first definition sentence. 2. Integrate instruction #2: Add a compact disambiguation (1–2 se. . . aired clot formation and bleeding risk, not excessive clotting). 3. Integrate instruction #3: Resolve inconsistent wording by unif. . . reader cannot misinterpret coagulopathy as “excessive clotting”. Format note:Keep within the opening paragraph; add at most 1–2 clarification sentences and do not introduce new sections.

**中文**

积分指令#1：重写起始定义。。。在第一个定义句子中进行多术语对比。 2. 整合指令#2：添加紧凑的歧义（1-2 秒……空气凝块形成和出血风险，而不是过度凝血）。 3. 整合指令#3：通过unif解决不一致的措辞。。。读者不能将凝血病误解为“过度凝血”。格式注意：保持在开头段落内；最多添加 1-2 个说明性句子，并且不要引入新的部分。

### 段落 94 · Page 13

**EN**

C.5 Blueprint-Guided Revision Finally, the document is edited under the blueprint constraints to balance readability and terminological correctness with minimal, localized changes. Document snippet (after, expected). “Coagulopathy is a condition in which the blood’s ability to for. . . m clots is impaired, leading to prolonged or excessive bleeding. It can occur spontaneously or following an injury or medical procedure. . . . The term is sometimes confused with ‘clotting disorders,’ a br. . . n increased risk of bleeding, rather than excessive clotting. . . .

**中文**

C.5 蓝图指导修订 最后，在蓝图约束下编辑文档，以通过最小的局部更改来平衡可读性和术语正确性。文档片段（之后，预期）。 “凝血障碍是一种血液能力下降的疾病。。。血栓受损，导致出血时间延长或过多。它可以自发发生，也可以在受伤或医疗程序后发生。。。。该术语有时会与“凝血障碍”混淆。。。 n 增加出血风险，而不是过度凝血。。。。

### 段落 95 · Page 13

**EN**

” C.6 Token Breakdown of IF-GEO Unlike conventional single-pass GEO baselines that rewrite a document once, IF-GEO performs a two-stage“diverge-then-converge”workflow,

**中文**

C.6 IF-GEO 的令牌分解 与重写一次文档的传统单通道 GEO 基线不同，IF-GEO 执行两阶段“发散然后聚合”工作流程，

### Page 14

### 段落 96 · Page 14

**EN**

Table 5: Average token consumption per stage in IF- GEO (per document). Stage Avg. Tokens Query Mining 1270.6 Edit Request Generation 1749.8 Instruction Fusion 4487.6 Blueprint-Guided Revision 2819.8 Total 10327.7 Table 6: Average token consumption of single-pass GEO baselines (per document). Method Avg. Tokens Tran. SEO 2653.9 Uniq. Word 2282.8 Simp. Expr. 2204.3 Auth. Expr. 2483.7 Flue. Expr. 2171.6 Term. Addi. 2392.4 Cite Sources 2535.0 Quot. Addi. 2589.5 Stat. Addi. 2802.2 where each stage targets a distinct task.

**中文**

表 5：IF-GEO 中每个阶段的平均代币消耗（每个文档）。阶段平均令牌查询挖掘 1270.6 编辑请求生成 1749.8 指令融合 4487.6 蓝图引导修订 2819.8 总计 10327.7 表 6：单通道 GEO 基线的平均令牌消耗（每个文档）。方法平均值代币交易。 SEO 2653.9 独特。 Word 2282.8 简单。表达式。 2204.3 授权表达式。 2483.7 烟道。表达式。 2171.6 期限。阿迪。 2392.4 引用来源 2535.0 引用。阿迪。 2589.5 统计阿迪。 2802.2，每个阶段都针对一个不同的任务。

### 段落 97 · Page 14

**EN**

Table 5 reports the average token consumption per document for each step, aggregated over the evaluation set (prompt+completion tokens). The dominant cost comes fromInstruction Fusion, which consolidates query-specific edit requests into a single executableglobal revision blueprint. This stage involves joint reasoning over partially overlapping directives (e.g., deduplication, prioritization, and arbitration), and therefore scales with the diversity of intents and the number of candidate requests rather than redundant text generation.

**中文**

表 5 报告了每个文档每个步骤的平均令牌消耗，在评估集（提示+完成令牌）上进行汇总。主要成本来自指令融合，它将特定于查询的编辑请求合并到单个可执行的全局修订蓝图中。此阶段涉及对部分重叠指令（例如，重复数据删除、优先级排序和仲裁）进行联合推理，因此可以根据意图的多样性和候选请求的数量进行扩展，而不是冗余文本生成。

### 段落 98 · Page 14

**EN**

C.7 Comparison with Single-Pass GEO Baselines For reference, Table 6 reports the token consumption of representative single-pass GEO baselines, each executed once per document under the same model configuration. These baselines apply localized rewriting heuristics without explicitly coordinating across the representative query set. As expected, single-pass baselines incur substantially lower token usage, since they do not explore multiple queries nor perform cross-query consolidation. Table 7: Objective visibility on Gemini-2.0-Flash (primary objective metric:Obj. Overall).

**中文**

C.7 与单遍 GEO 基线的比较 作为参考，表 6 报告了代表性单遍 GEO 基线的令牌消耗，每个基线在相同模型配置下每个文档执行一次。这些基线应用本地化重写启发式方法，无需在代表性查询集之间进行显式协调。正如预期的那样，单遍基线的令牌使用量大大降低，因为它们不探索多个查询，也不执行跨查询整合。表 7：Gemini-2.0-Flash 上的客观可见性（主要目标指标：总体目标）。

### 段落 99 · Page 14

**EN**

We report mean improvement (Mean↑) and stability summaries (V AR↓, WCP↑, WTR↑, DR↓). Method Mean V AR WCP WTR DR Tran. SEO 1.93 0.0252 -0.1313 70.28% 0.0089 Uniq. Word -5.99 0.0290 -0.2187 56.12% 0.0279 Simp. Expr. -0.88 0.0196 -0.1496 65.24% 0.0127 Auth. Expr. -0.02 0.0241 -0.1474 65.08% 0.0137 Flue. Expr. -1.93 0.0267 -0.1834 62.56% 0.0176 Term. Addi. 1.31 0.0231 -0.1354 69.33% 0.0102 Cite Sources 2.54 0.0246 -0.1156 74.21% 0.0089 Quot. Addi. 3.10 0.0321 -0.1284 72.58% 0.0099 Stat. Addi.

**中文**

我们报告平均改进 (Mean↑) 和稳定性摘要 (VAR↓、WCP↑、WTR↑、DR↓)。方法 平均值 VAR WCP WTR DR Tran。搜索引擎优化 1.93 0.0252 -0.1313 70.28% 0.0089字 -5.99 0.0290 -0.2187 56.12% 0.0279表达式。 -0.88 0.0196 -0.1496 65.24% 0.0127表达式。 -0.02 0.0241 -0.1474 65.08% 0.0137 烟道。表达式。 -1.93 0.0267 -0.1834 62.56% 0.0176 期限。阿迪。 1.31 0.0231 -0.1354 69.33% 0.0102 引用来源 2.54 0.0246 -0.1156 74.21% 0.0089阿迪。 3.10 0.0321 -0.1284 72.58% 0.0099 统计阿迪。

### 段落 100 · Page 14

**EN**

0.25 0.0190 -0.1345 71.57% 0.0108 RAID 2.80 0.0240 -0.1248 71.43% 0.0099 Auto-GEO 12.99 0.0416 -0.0578 78.91% 0.0083 IF-GEO 14.17 0.0386 -0.0435 84.07% 0.0054 D Performance Stratified by Initial Document Ranking This appendix complements thesensitivity to initial document rankinganalysis in Section 6.4. We stratify evaluation instances by theirinitial ranking positionprior to optimization and report rankbucketed performance of IF-GEO. The goal is to verify that improvements are not confined to already well-ranked inputs, but persist across ranking strata.

**中文**

0.25 0.0190 -0.1345 71.57% 0.0108 RAID 2.80 0.0240 -0.1248 71.43% 0.0099 自动 GEO 12.99 0.0416 -0.0578 78.91% 0.0083 IF-GEO 14.17 0.0386 -0.0435 84.07% 0.0054 D 按初始文档排名进行绩效分层 本附录补充了第 6.4 节中对初始文档排名分析的敏感性。我们根据优化前的初始排名位置对评估实例进行分层，并报告 IF-GEO 的排名桶性能。目标是验证改进不仅限于已经排名良好的输入，而是在各个排名层中持续存在。

### 段落 101 · Page 14

**EN**

Rank buckets.Each instance is assigned to one of five buckets (Rank1–Rank5) according to its initial ranking position under the same evaluation setting as the main experiments, whereRank1corresponds to higher-ranked inputs andRank5to lower-ranked inputs. All instances and metrics follow the main evaluation protocol; only the reporting is stratified by rank. Metrics.For each bucket, we report mean improvement (Mean) and cross-query stability summaries (V AR, WCP, WTR, DR) for both the primary objective metric (Obj. Overall) and the subjective metric (Subj. Average), using the same definitions as in Section 5.3.

**中文**

排名桶。在与主实验相同的评估设置下，每个实例根据其初始排名位置被分配到五个桶（Rank1-Rank5）之一，其中Rank1对应于较高排名的输入，Rank5对应于较低排名的输入。所有实例和指标均遵循主要评估协议；只有报告是按等级分层的。指标。对于每个存储桶，我们使用与第 5.3 节相同的定义报告主要客观指标（Obj.Overall）和主观指标（Subj.Average）的平均改进（Mean）和跨查询稳定性摘要（VAR、WCP、WTR、DR）。

### 段落 102 · Page 14

**EN**

Discussion.IF-GEO yields consistent improvements across all rank buckets for bothObj. OverallandSubj. Average, indicating that gains are not concentrated exclusively on higher-ranked inputs. In particular, lower-ranked buckets (Rank4– Rank5) still achieve sizable mean improvements while maintaining favorable tail-oriented stability (e.g., competitive WCP/WTR and low DR), supporting the claim in Section 6.4 that IF-GEO improves content robustness rather than merely exploiting positional advantages.

**中文**

Discussion.IF-GEO 在 BothObj 的所有排名桶中产生一致的改进。总体和主题。平均，表明收益不仅仅集中在排名较高的投入上。特别是，排名较低的存储桶（Rank4-Rank5）仍然实现了相当大的平均改进，同时保持了良好的尾部稳定性（例如，有竞争力的 WCP/WTR 和低 DR），支持第 6.4 节中的主张，即 IF-GEO 提高了内容稳健性，而不仅仅是利用位置优势。

### Page 15

### 段落 103 · Page 15

**EN**

Table 8: Rank-stratified performance of IF-GEO by initial ranking position prior to optimization. We report mean improvement (Mean↑) and stability summaries (V AR↓, WCP↑, WTR↑, DR↓) for the primary objective metric (Obj. Overall) and the subjective metric (Subj. Average). Rank Obj. Overall Subj.

**中文**

表 8：优化前按初始排名位置划分的 IF-GEO 排名分层性能。我们报告主要客观指标（Obj.Overall）和主观指标（Subj.Average）的平均改进（Mean↑）和稳定性摘要（VAR↓、WCP↑、WTR↑、DR↓）。排名对象。总体主题。

### 段落 104 · Page 15

**EN**

Average Mean (↑) V AR (↓) WCP (↑) WTR (↑) DR (↓) Mean (↑) V AR (↓) WCP (↑) WTR (↑) DR (↓) IF-GEO 11.03 0.0156 -0.0090 80.50% 0.0023 5.87 0.0116 -0.0419 85.56% 0.0036 Rank1 13.49 0.0174 0.0084 77.92% 0.0033 6.39 0.0140 -0.0431 85.30% 0.0054 Rank2 8.56 0.0121 -0.0281 77.36% 0.0031 6.78 0.0108 -0.0292 84.64% 0.0038 Rank3 8.71 0.0159 -0.0209 82.76% 0.0007 5.65 0.0092 -0.0223 87.59% 0.0008 Rank4 12.24 0.0140 0.0196 87.14% 0.0006 5.20 0.0119 -0.0592 87.55% 0.0028 Rank5 12.14 0.0189 -0.0154 81.43% 0.0022 4.72 0.0114 -0.0587 84.29% 0.0038 E Evaluation on Gemini-2.0-Flash This appendix complements thecross-model generalizationanalysis in Section 6.4.

**中文**

平均 平均值 (↑) VAR (↓) WCP (↑) WTR (↑) DR (↓) 平均值 (↑) VAR (↓) WCP (↑) WTR (↑) DR (↓) IF-GEO 11.03 0.0156 -0.0090 80.50% 0.0023 5.87 0.0116 -0.0419 85.56% 0.0036 排名 1 13.49 0.0174 0.0084 77.92% 0.0033 6.39 0.0140 -0.0431 85.30% 0.0054 排名 2 8.56 0.0121 -0.0281 77.36% 0.0031 6.78 0.0108 -0.0292 84.64% 0.0038 排名3 8.71 0.0159 -0.0209 82.76% 0.0007 5.65 0.0092 -0.0223 87.59% 0.0008 排名4 12.24 0.0140 0.0196 87.14% 0.0006 5.20 0.0119 -0.0592 87.55% 0.0028 排名5 12.14 0.0189 -0.0154 81.43% 0.0022 4.72 0.0114 -0.0587 84.29% 0.0038 E 对 Gemini-2.0-Flash 的评估 本附录补充了第 6.4 节中的跨模型泛化分析。

### 段落 105 · Page 15

**EN**

We replace the underlying generative engine withGemini-2.0- Flashand re-evaluate all methods under the same dataset, query sets, and evaluation protocol as in the main experiments. Due to interface limitations, we report only the primary objective visibility metric (Obj. Overall) in this setting. Setup.All GEO baselines, RAID, Auto-GEO, and IF-GEO are re-run on Gemini-2.0-Flash without any method-specific tuning. All configurations follow the main evaluation pipeline; the only change is the underlying generative engine.

**中文**

我们用 Gemini-2.0-Flash 替换底层生成式引擎，并在与主要实验相同的数据集、查询集和评估协议下重新评估所有方法。由于界面限制，我们在此设置中仅报告主要目标可见性指标（Obj.Overall）。设置。所有 GEO 基线、RAID、Auto-GEO 和 IF-GEO 均在 Gemini-2.0-Flash 上重新运行，无需任何特定于方法的调整。所有配置均遵循主要评估流程；唯一的变化是底层的生成式引擎。

### 段落 106 · Page 15

**EN**

Metrics.We report mean improvement (Mean) and cross-query stability summaries (V AR, WCP, WTR, DR) computed over the representative query set, following the same definitions as in Section 5.3. Discussion.Table 7 shows that IF-GEO remains strong under a different generative engine, achieving the largest mean improvement and favorable tail-oriented stability (e.g., higher WTR and lower DR) among all methods. The overall trend is consistent with the main results, supporting the crossmodel generalization claim in Section 6.4.

**中文**

指标。我们报告在代表性查询集上计算的平均改进（Mean）和跨查询稳定性摘要（VAR、WCP、WTR、DR），遵循与第 5.3 节相同的定义。讨论。表7显示，IF-GEO在不同的生成式引擎下仍然保持强劲，在所有方法中实现了最大的平均改进和良好的尾部稳定性（例如，更高的WTR和更低的DR）。总体趋势与主要结果一致，支持第 6.4 节中的跨模型泛化主张。
