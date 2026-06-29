# Aligning Large Language Models with Searcher Preferences

- ID: 85
- 类型: pdf
- 分类: 04_academic_papers
- 主题: open-ended generative search alignment
- 原文链接: https://arxiv.org/pdf/2603.10473
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

Aligning Large Language Models with Searcher Preferences Wei Wu∗ School of Artificial Intelligence and Data Science, University of Science and Technology of China Hefei, China urara@mail.ustc.edu.cn Peilun Zhou∗ Xiaohongshu Inc. Beijing, China zhoupeilun@xiaohongshu.com Liyi Chen† Xiaohongshu Inc. Beijing, China chenliyi@xiaohongshu.com Qimeng Wang Xiaohongshu Inc. Beijing, China qimengwang@xiaohongshu.com Chengqiang Lu Xiaohongshu Inc. Beijing, China lunar@mail.ustc.edu.cn Yan Gao Xiaohongshu Inc. Beijing, China wanjianyi@xiaohongshu.com Yi Wu Xiaohongshu Inc. Beijing, China luyun2@xiaohongshu.com Yao Hu Xiaohongshu Inc.

**中文**

将大型语言模型与搜索者偏好保持一致 Wei Wu* 中国科学技术大学人工智能与数据科学学院 urara@mail.ustc.edu.cn Peilun Zhou* 小红书公司 中国北京 Zhoupeilun@xiaohongshu.com Liyi Chen† 小红书公司 中国北京 chenliyi@xiaohongshu.com Qimeng Wang 小红书公司 中国北京qimengwang@xiaohongshu.com 陆成强 小红书公司 中国北京 lunar@mail.ustc.edu.cn 严高小红书公司 中国北京 wanjianyi@xiaohongshu.com 吴毅小红书公司 中国北京 luyun2@xiaohongshu.com 胡姚 小红书公司

### 段落 2 · Page 1

**EN**

Beijing, China xiahou@xiaohongshu.com Hui Xiong† Thrust of Artificial Intelligence, The Hong Kong University of Science and Technology (Guangzhou) Guangzhou, China Department of Computer Science and Engineering, The Hong Kong University of Science and Technology Hong Kong SAR, China xionghui@ust.hk Abstract The paradigm shift from item-centric ranking to answer-centric synthesis is redefining the role of search engines. While recent industrial progress has applied generative techniques to closed-set item ranking in e-commerce, research and deployment of openended generative search on large content platforms remain limited.

**中文**

中国北京 xiahou@xiaohongshu.com Hui Xiong† 人工智能的推动力，香港科技大学（广州） 中国广州 香港科技大学计算机科学与工程系 中国香港特别行政区 xionghui@ust.hk 摘要 从以项目为中心的排名到以答案为中心的综合的范式转变正在重新定义搜索引擎的角色。尽管最近的工业进步已将生成技术应用于电子商务中的封闭集项目排名，但大型内容平台上开放式生成搜索的研究和部署仍然有限。

### 段落 3 · Page 1

**EN**

This setting introduces challenges, including robustness to noisy retrieval, non-negotiable safety guarantees, and alignment with diverse user needs. In this work, we introduce SearchLLM, the first large language model (LLM) for open-ended generative search. We design a hierarchical, multi-dimensional reward system that separates bottom-line constraints, including factual grounding, basic answer quality and format compliance, from behavior optimization objectives that promote robustness to noisy retrieval and alignment with user needs.

**中文**

这种设置带来了挑战，包括对噪声检索的鲁棒性、不可协商的安全保证以及与不同用户需求的一致性。在这项工作中，我们介绍了 SearchLLM，这是第一个用于开放式生成搜索的大型语言模型 (LLM)。我们设计了一个分层的、多维的奖励系统，将底线约束（包括事实基础、基本答案质量和格式合规性）与促进鲁棒性的行为优化目标分开，以提高噪声检索和与用户需求的一致性。

### 段落 4 · Page 1

**EN**

Concretely, our reward model evaluates responses conditioned on the user query, session history, and retrieved evidence set, combining rule-based checks with human-calibrated LLM judges to produce an interpretable score vector over these dimensions. We introduce a Gated Aggregation Strategy to derive the training reward for optimizing SearchLLM with Group Relative Policy Optimization (GRPO). We deploy SearchLLM in the AI search entry of RedNote.

**中文**

具体来说，我们的奖励模型评估以用户查询、会话历史记录和检索到的证据集为条件的响应，将基于规则的检查与人工校准的 LLM 法官相结合，在这些维度上生成可解释的分数向量。我们引入门控聚合策略来获得通过组相对策略优化 (GRPO) 优化 SearchLLM 的训练奖励。我们在RedNote的AI搜索入口中部署SearchLLM。

### 段落 5 · Page 1

**EN**

Offline evaluations and online A/B tests show improved generation quality and user engagement, increasing Valid Consumption Rate by 1.03% and reducing Re-search Rate by 2.81%, while upholding strict safety and reliability standards.

**中文**

线下评估和线上A/B测试显示，发电质量和用户参与度得到提高，有效消费率提高1.03%，研究率降低2.81%，同时坚持严格的安全性和可靠性标准。

### 段落 6 · Page 1

**EN**

∗Equal Contribution † Corresponding Authors Keywords Generative Search, Large Language Models, Reinforcement Learning, Reward Modeling, Retrieval-Augmented Generation 1 Introduction The rapid growth in both the scale and diversity of digital content on online platforms has resulted in severe information overload [6], making it increasingly challenging for users to efficiently locate accurate answers and make informed decisions. Despite significant advances in search engines that have improved retrieval precision by providing more relevant items [ 41], outputs of search engines typically remain as itemized lists.

**中文**

*同等贡献†通讯作者关键词生成搜索、大型语言模型、强化学习、奖励建模、检索增强第一代引言在线平台上数字内容的规模和多样性的快速增长导致了严重的信息过载[6]，使得用户高效地找到准确答案并做出明智决策变得越来越具有挑战性。尽管搜索引擎取得了显着进步，通过提供更多相关项来提高检索精度[41]，但搜索引擎的输出通常仍为逐项列表。

### 段落 7 · Page 1

**EN**

This format places a cognitive burden on users, who still need to further sift through and synthesize the results to fulfill their information needs. Recently, large language models (LLMs) have enabled a new open-ended paradigm of generative search systems [2, 5, 8, 30, 34], which can comprehensively assess the relevance and validity of retrieved information and directly generate coherent, natural-language answers to user queries.

**中文**

这种格式给用户带来了认知负担，他们仍然需要进一步筛选和综合结果来满足他们的信息需求。最近，大语言模型（LLM）启用了一种新的开放式生成搜索系统范式[2,5,8,30,34]，它可以全面评估检索信息的相关性和有效性，并直接为用户查询生成连贯的自然语言答案。

### 段落 8 · Page 1

**EN**

This transition from closed-set item retrieval to open-ended answer generation fundamentally redefines the role of search engines from merely returning candidate items to delivering synthesized, user-centered solutions. Nowadays, open-ended generative search has been increasingly integrated into widely adopted real-world online platforms and is used by hundreds of millions of users, positioning it as a critical interface for large-scale information access and sensemaking.

**中文**

从封闭集项目检索到开放式答案生成的转变从根本上重新定义了搜索引擎的角色，从仅仅返回候选项目到提供综合的、以用户为中心的解决方案。如今，开放式生成搜索已越来越多地集成到广泛采用的现实世界在线平台中，并被数亿用户使用，将其定位为大规模信息访问和意义建构的关键界面。

### 段落 9 · Page 1

**EN**

Across short-video apps (e.g., Douyin [5]/TikTok [30]), super-app ecosystems (e.g., WeChat [34]), and general-purpose assistants (e.g., arXiv:2603.10473v1 [cs.CL] 11 Mar 2026

**中文**

跨短视频应用（例如抖音 [5]/TikTok [30]）、超级应用生态系统（例如微信 [34]）和通用助手（例如 arXiv:2603.10473v1 [cs.CL] 2026 年 3 月 11 日

### Page 2

### 段落 10 · Page 2

**EN**

KDD ’26, August 9–13, 2026, Jeju, Korea Wei Wu, Peilun Zhou, et al.     !(   *+$ $$+ "&*"'&) &* &*")%* !  %&*"  +& & - '(%**"& ))+ ) ," & '& $" *  *-*! ()       **("+*"'&' "$+( ) ) ('%&$"& ) (  # Figure 1: User interaction snapshots of open-ended generative search in RedNote. The bottom-right panel summarizes failure attribution from online user feedback.

**中文**

KDD ’26，2026 年 8 月 9-13 日，韩国济州 Wei Wu、Peilun Zhou 等。 ! ( *+ $ $$+ "& *"'&) &* &* ")% * ! % &*" +& & - '(% **"& ))+ ) ," & '& $" * *- *! () **(" +*"'& ' "$+( ) ) ('% &$"& ) ( # 图 1：RedNote 中开放式生成搜索的用户交互快照。右下小组根据在线用户反馈总结了故障归因。

### 段落 11 · Page 2

**EN**

Gemini [8]/ChatGPT [2]), these systems ground responses in heterogeneous sources—videos, live streams, hybrid posts, official accounts/news, and the web—and synthesize them into direct conversational answers, enabling faster access, clearer summaries, and more interactive exploration. In the literature, industrial generative search systems are still largely item-centric and mainly focus on closed-set item generation in e-commerce domain, where the goal is to generate or rank product identifiers rather than produce freeform answers.

**中文**

Gemini [8]/ChatGPT [2]），这些系统对异构来源（视频、直播、混合帖子、官方账户/新闻和网络）中的响应进行基础处理，并将它们合成为直接对话答案，从而实现更快的访问、更清晰的摘要和更多的交互式探索。在文献中，工业生成搜索系统仍然主要以项目为中心，主要关注电子商务领域的封闭集项目生成，其目标是生成或排名产品标识符，而不是产生自由形式的答案。

### 段落 12 · Page 2

**EN**

For example, OneSearch [3] enables production-scale generative retrieval via semantic ID tokenization with behavioraware training; GRAM [22] generates product IDs auto-regressively in a unified query–item code space; and CRS [16] post-trains LLMs with SFT and RL to better capture user preferences for ranking. However, such closed-set formulations are not directly applicable to open-ended generative search, where the system needs to synthesize grounded natural-language answers from heterogeneous and potentially noisy evidence under real-world user intents.

**中文**

例如，OneSearch [3] 通过语义 ID 标记化和行为感知训练实现生产规模的生成检索； GRAM [22] 在统一的查询项目代码空间中自动回归生成产品 ID； CRS [16] 使用 SFT 和 RL 对 LLM 进行后训练，以更好地捕获用户的排名偏好。然而，这种封闭式的表述并不直接适用于开放式生成搜索，在开放式生成搜索中，系统需要根据现实世界的用户意图，从异构且潜在噪声的证据中合成接地的自然语言答案。

### 段落 13 · Page 2

**EN**

As illustrated in Figure 1, we show the interface of open-ended generative search in the RedNote. The bottom-right subfigure further summarizes the attribution analysis of failure cases collected from online user feedback.

**中文**

如图 1 所示，我们展示了 RedNote 中开放式生成搜索的界面。右下子图进一步总结了从在线用户反馈中收集的失败案例的归因分析。

### 段落 14 · Page 2

**EN**

Mitigating these issues requires aligning the underlying LLMs with three key requirements.R1: Robustness to noisy queries and evidence.LLMs should remain robust under ambiguous or underspecified queries and noisy, heterogeneous, outdated, redundant, or even conflicting retrieved evidence, while deciding when to infer intent, ask for clarification, or refuse unsafe requests.R2: Bottom-line guarantees on reliability and safety.Generated answers should satisfy strict reliability and safety guards, including factual grounding in provided evidence or widely accepted background knowledge, safety and policy compliance, logical consistency, and a con

**中文**

缓解这些问题需要使基础法学硕士与三个关键要求保持一致。R1：对嘈杂查询和证据的稳健性。法学硕士应在模糊或未指定的查询以及嘈杂、异构、过时、冗余甚至冲突的检索证据下保持稳健，同时决定何时推断意图、要求澄清或拒绝不安全的请求。R2：可靠性和安全性的底线保证。生成的答案应满足严格的可靠性和安全防护，包括事实基础提供证据或广泛接受的背景知识、安全和政策合规性、逻辑一致性以及反驳

### 段落 15 · Page 2

**EN**

trollable response format.R3: Alignment with user needs.Answers should be optimized for user consumption and decision support, presenting key information early, reducing redundancy, and choosing an appropriate level of detail and structure for each query without weakening the constraints above.

**中文**

可控制的响应格式。R3：与用户需求保持一致。答案应该针对用户消费和决策支持进行优化，尽早呈现关键信息，减少冗余，并为每个查询选择适当的细节和结构级别，而不削弱上述约束。

### 段落 16 · Page 2

**EN**

Therefore, how to effectively train an LLM for open-ended generative search is of central importance. In this work, we introduce SearchLLM, the first LLM for openended generative search. We first propose a reward system that encodes the three requirements above, and train SearchLLM under this objective.

**中文**

因此，如何有效地训练法学硕士进行开放式生成搜索至关重要。在这项工作中，我们介绍了SearchLLM，第一个用于开放式生成搜索的LLM。我们首先提出一个编码上述三个要求的奖励系统，并在此目标下训练SearchLLM。

### 段落 17 · Page 2

**EN**

Concretely, we consolidate the three requirements into a two-layer design that separates non-negotiable safeguards from user-facing quality objectives: a bottom-line layer that encodes R2 as hard constraints on factual grounding, safety, and response format, and a behavior optimization layer that, within this safe region, jointly captures R1 and R3 by shaping how the model responds to uncertain queries and noisy evidence and how it trades off brevity, coverage, and novelty.

**中文**

具体来说，我们将这三个要求整合到一个两层设计中，将不可协商的保障措施与面向用户的质量目标分开：一个底线层，将 R2 编码为对事实基础、安全性和响应格式的硬约束；以及一个行为优化层，在这个安全区域内，通过塑造模型如何响应不确定的查询和噪声证据以及如何权衡简洁性、覆盖范围和新颖性，共同捕获 R1 和 R3。

### 段落 18 · Page 2

**EN**

On top of this structural design, we instantiate a hybrid evaluation stack that combines deterministic rule-based evaluators with LLM-based judges, each designed to output fine-grained, interpretable scores on specific sub-dimensions of the metric space. We calibrate our evaluators via a human-inthe-loop process so that the resulting interpretable metrics remain faithful to searcher preferences and stable in deployment.

**中文**

在此结构设计之上，我们实例化了一个混合评估堆栈，它将基于确定性规则的评估器与基于 LLM 的判断器相结合，每个评估器都旨在在度量空间的特定子维度上输出细粒度的、可解释的分数。我们通过人机交互流程来校准评估器，以便生成的可解释指标能够忠实于搜索者的偏好并在部署中保持稳定。

### 段落 19 · Page 2

**EN**

The resulting multi-dimensional reward vector is then transformed by a Gated Aggregation Strategy that protects bottom-line dimensions and rebalances user-facing quality dimensions, and is subsequently used as the objective in a Group Relative Policy Optimization [27] (GRPO)-style reinforcement learning pipeline trained over largescale search query logs. We deploy SearchLLM in the AI search entry of RedNote. Online A/B tests demonstrate that our method yields measurable gains in user satisfaction, specifically increasing the Valid Consumption Rate (VCR) by 1.03% and reducing the Research Rate (RR) by 2.81% compared to the production baseline.

**中文**

然后，得到的多维奖励向量通过门控聚合策略进行转换，该策略保护底线维度并重新平衡面向用户的质量维度，并随后用作在大规模搜索查询日志上训练的组相对策略优化 [27] (GRPO) 式强化学习管道中的目标。我们在RedNote的AI搜索入口中部署SearchLLM。在线 A/B 测试表明，我们的方法在用户满意度方面产生了可测量的收益，特别是与生产基线相比，有效消费率 (VCR) 提高了 1.03%，研究率 (RR) 降低了 2.81%。

### 段落 20 · Page 2

**EN**

We summarize our main contributions as follows. • We are the first to characterize the unique demands of openended generative search on large content platforms and introduce a dedicated LLM named SearchLLM, which can provide valuable insights for the community. • We propose a multi-dimensional reward design for generative search that explicitly separates non-negotiable safeguards from user-facing quality objectives, and instantiate it with a hybrid stack of rule-based checks and LLM judges calibrated by experts.

**中文**

We summarize our main contributions as follows. • 我们率先描述了大型内容平台上开放式生成搜索的独特需求，并推出了名为SearchLLM 的专用法学硕士，它可以为社区提供有价值的见解。 • 我们提出了一种用于生成搜索的多维奖励设计，该设计明确地将不可协商的保障措施与面向用户的质量目标分开，并通过基于规则的检查和由专家校准的LLM法官的混合堆栈来实例化它。

### 段落 21 · Page 2

**EN**

• We develop an end-to-end reinforcement learning recipe for SearchLLM, optimizing the full workflow with GRPO-style training and a Gated Aggregation Strategy that prioritizes bottomline constraints while improving robustness and utility. • We deploy SearchLLM in RedNote’s AI search entry, and online A/B tests show improved user experience, with +1.03% Valid Consumption Rate (VCR) and -2.81% Re-search Rate (RR) over the production baseline. 2 Related Work Large Language Models for Search.LLMs are gradually reshaping how search engines operate and interact with users [35].

**中文**

• 我们为SearchLLM 开发了端到端强化学习方案，通过GRPO 式训练和门控聚合策略优化整个工作流程，优先考虑底线约束，同时提高鲁棒性和实用性。 • 我们在 RedNote 的 AI 搜索条目中部署了 SearchLLM，在线 A/B 测试显示用户体验得到改善，有效消费率 (VCR) 比生产基线高出 +1.03%，重新搜索率 (RR) 比生产基线高出 -2.81%。 2 相关工作 用于搜索的大型语言模型。法学硕士正在逐渐重塑搜索引擎的操作方式以及与用户的交互方式[35]。

### 段落 22 · Page 2

**EN**

At the component level, LLMs are extensively used to enhance query understanding via rewriting and expansion [23, 33], improve document indexing through semantic embedding [ 4], and refine ranking by estimating relevance more accurately [20, 24]. Beyond these component-level optimizations, recent industrial efforts in the e-commerce domain have explored end-to-end generative retrieval. Notable systems like OneSearch [3] employ semantic ID tokenization to perform generative retrieval at scale, while GRAM [22] and

**中文**

在组件级别，LLM 广泛用于通过重写和扩展来增强查询理解 [23, 33]，通过语义嵌入改进文档索引 [4]，并通过更准确地估计相关性来改进排名 [20, 24]。除了这些组件级优化之外，电子商务领域最近的工业努力还探索了端到端生成检索。 OneSearch [3] 等著名系统采用语义 ID 标记化来大规模执行生成检索，而 GRAM [22] 和

### Page 3

### 段落 23 · Page 3

**EN**

Aligning Large Language Models with Searcher Preferences KDD ’26, August 9–13, 2026, Jeju, Korea A. Generative Search System Overview SearchLLM(𝜋𝜃) User𝑞 Sessionhistoryℎ SearchplanEvidenceSet Query Internal NotesWeb SearchReal-time Tools… 𝐸 SelectedEvidenceSet Intent Planning &Evidence SelectionEvidence-GroundedGeneration Final Response (𝑦) Layer I: Bottom-line Constraints (CBL)B.

**中文**

将大型语言模型与搜索者偏好对齐 KDD ’26，2026 年 8 月 9-13 日，韩国济州 A. 生成搜索系统概述 SearchLLM(𝜋𝜃) User𝑞 Sessionhistoryℎ SearchplanEvidenceSet 查询内部注释Web 搜索实时工具…𝐸 SelectedEvidenceSet 意图规划和证据选择Evidence-GroundedGeneration最终响应 (𝑦) 第一层：底线约束 (CBL)B。

### 段落 24 · Page 3

**EN**

Multi-Dimensional Reward System & Gated Aggregation (𝑞,ℎ,𝐸)𝑦FactualGroundingBasicQualityFormatComplianceRule-based Checks& LLM JudgesGeometric Mean (Soft-AND Gate)∏ Layer II: Behavioral Objectives (CBH)RobustnessRichness& DiversityConciseness& UsabilityLLM Judges ×𝐵!𝑥,𝑦 Human-in-the-loopCalibration𝑈(𝑥,𝑦)ΣWeighted Arithmetic Mean C. End-to-End GRPO Optimization𝑅𝑥,𝑦 QueryLogs(𝐷) RewardSystemSearchLLM(𝜋𝜃) 𝑦!𝑦"𝑦#…ReferenceModel KL 𝑅!𝑅"𝑅#… GroupComputation 𝐴!𝐴"𝐴#… Figure 2: Overview of the alignment framework for open-ended generative search.

**中文**

多维奖励系统和门控聚合（𝑞，ℎ，𝐸）𝑦FactualGroundingBasicQualityFormatCompliance基于规则的检查和LLM法官几何平均值（软与门）∏第二层：行为目标（CBH）稳健性丰富性和多样性简洁性和可用性LLM法官×𝐵！𝑥，𝑦 Human-in-the-loopCalibration𝑈(𝑥,𝑦)Σ加权算术平均值 C. 端到端 GRPO 优化𝑅𝑥,𝑦 QueryLogs(𝐷) RewardSystemSearchLLM(𝜋𝜃) 𝑦!𝑦"𝑦#…ReferenceModel KL 𝑅!𝑅"𝑅#... GroupComputation 𝐴!𝐴"𝐴#... 图 2：开放式生成搜索的对齐框架概述。

### 段落 25 · Page 3

**EN**

The pipeline incorporates a multidimensional reward system that explicitly decouples non-negotiable bottom-line constraints (Layer I) from behavioral optimization objectives (Layer II). A hybrid evaluation stack, consisting of deterministic rules and human-calibrated LLM judges, computes fine-grained scores across multiple dimensions. These signals are synthesized via a gated aggregation mechanism to stabilize the learning signal for Group Relative Policy Optimization (GRPO). CRS [16] generate product identifiers auto-regressively in a unified query–item latent space.

**中文**

该管道包含一个多维奖励系统，该系统明确地将不可协商的底线约束（第一层）与行为优化目标（第二层）脱钩。混合评估堆栈由确定性规则和人工校准的法学硕士法官组成，可以跨多个维度计算细粒度的分数。这些信号通过门控聚合机制合成，以稳定组相对策略优化 (GRPO) 的学习信号。 CRS [16] 在统一的查询项潜在空间中自动回归生成产品标识符。

### 段落 26 · Page 3

**EN**

In parallel, the paradigm of retrievalaugmented generation (RAG) [ 7, 41] has shifted the focus from returning ranked lists to synthesizing natural-language answers grounded in retrieved evidence [29, 38]. However, in the literature, industrial applications predominantly focus on closed-set item ranking for e-commerce. Systematic studies on deploying open-ended generative search remain limited at scale. Alignment of Large Language Models.Aligning LLMs with human values and safety standards is critical for deployment.

**中文**

与此同时，检索增强生成 (RAG) 的范式 [7, 41] 已将焦点从返回排名列表转移到合成基于检索证据的自然语言答案 [29, 38]。然而，在文献中，工业应用主要集中在电子商务的封闭集项目排名上。关于部署开放式生成搜索的系统研究规模仍然有限。大型语言模型的协调。使法学硕士与人类价值观和安全标准保持一致对于部署至关重要。

### 段落 27 · Page 3

**EN**

Standard approaches typically utilize Reinforcement Learning from Human Feedback (RLHF) via Proximal Policy Optimization (PPO) [21, 26], or employ more efficient offline variants such as Direct Preference Optimization (DPO) [25] and Group Relative Policy Optimization (GRPO) [27]. Regardless of the optimization algorithm, the efficacy of alignment relies on the design of the reward signal, which falls into three categories: (i) Scalar reward models [1, 18, 21], which map responses to a single quality score.

**中文**

标准方法通常通过近端策略优化 (PPO) [21, 26] 利用人类反馈强化学习 (RLHF)，或者采用更有效的离线变体，例如直接偏好优化 (DPO) [25] 和组相对策略优化 (GRPO) [27]。无论采用哪种优化算法，对齐的有效性都依赖于奖励信号的设计，奖励信号分为三类：（i）标量奖励模型[1,18,21]，它将响应映射到单个质量分数。

### 段落 28 · Page 3

**EN**

While computationally efficient, they produce coarse-grained, opaque scores that act as black boxes, making it difficult to balance competing objectives like safety and helpfulness; (ii) LLM-as-a-judge approaches [ 14, 40], which leverage powerful LLMs to scale up evaluation without human labelers, though they can be sensitive to prompting and inherent model biases; and (iii) Rubric-based rewards [9, 15, 32], which decompose complex human preferences into structured, interpretable criteria (e.g., checklists).

**中文**

虽然计算效率高，但它们会产生粗粒度、不透明的分数，充当黑匣子，使得很难平衡安全性和有用性等相互竞争的目标； (ii) 法学硕士作为法官的方法[14, 40]，该方法利用强大的法学硕士来扩大评估规模，无需人工标记，尽管它们可能对提示和固有的模型偏差很敏感； (iii) 基于评分标准的奖励 [9,15,32]，它将复杂的人类偏好分解为结构化的、可解释的标准（例如清单）。

### 段落 29 · Page 3

**EN**

Building on these advances, we propose a two-layer, multi-dimensional reward system for open-ended generative search that explicitly separates non-negotiable safeguards from user-facing quality objectives, instantiated via a hybrid stack of rule-based checks and calibrated LLM judges. 3 Methodology 3.1 System Overview We design an LLM-based open-ended generative search pipeline (illustrated in Figure 2) that enhances retrieval-augmented generation by using a single LLM forintent planning,evidence selection, andevidence-grounded generationin a unified workflow.

**中文**

基于这些进步，我们提出了一个用于开放式生成搜索的两层、多维奖励系统，该系统将不可协商的保障措施与面向用户的质量目标明确区分开来，并通过基于规则的检查和校准的法学硕士法官的混合堆栈进行实例化。 3 方法论 3.1 系统概述 我们设计了一个基于 LLM 的开放式生成搜索管道（如图 2 所示），该管道通过使用单个 LLM 在统一工作流程中进行意图规划、证据选择和基于证据的生成来增强检索增强生成。

### 段落 30 · Page 3

**EN**

Built on top of a standard multi-source retrieval infrastructure that provides a broad pool of candidate evidence from internal note search, web search, and real-time tools, our system focuses on reasoning over this candidate pool rather than on retrieval itself. Given a user query and its session history, it first constructs an explicit intent plan that structures the information need into several interpretable facets and specifies how each facet should be supported by evidence.

**中文**

我们的系统建立在标准的多源检索基础设施之上，该基础设施通过内部笔记搜索、网络搜索和实时工具提供了广泛的候选证据池，我们的系统专注于对该候选池的推理，而不是检索本身。给定用户查询及其会话历史记录，它首先构建一个明确的意图计划，将信息需求构建为几个可解释的方面，并指定每个方面应如何由证据支持。

### Page 4

### 段落 31 · Page 4

**EN**

KDD ’26, August 9–13, 2026, Jeju, Korea Wei Wu, Peilun Zhou, et al. Conditioned on this plan, the system then performs intent-aware evidence selection that filters the candidate pool into a compact evidence set that is relevant, non-redundant, and collectively covers the planned facets. This curated evidence set is finally consumed by the LLM to synthesize a grounded final response. 3.2 Multi-Dimensional Reward System Our reward system does not evaluate responses in isolation, but instead scores complete search interactions.

**中文**

KDD ’26，2026 年 8 月 9-13 日，韩国济州 Wei Wu、Peilun Zhou 等。根据该计划，系统然后执行意图感知的证据选择，将候选池过滤成相关的、非冗余的紧凑证据集，并共同涵盖计划的方面。法学硕士最终会使用这个精心策划的证据集来合成有根据的最终答复。 3.2 多维奖励系统 我们的奖励系统不是孤立地评估响应，而是对完整的搜索交互进行评分。

### 段落 32 · Page 4

**EN**

Formally, let𝑥=(𝑞, ℎ, 𝐸) denote the input context comprising the query 𝑞, session history ℎ, and retrieved evidence set 𝐸, and let 𝑦 denote the generated sequence, which encompasses both the intent plan and the final answer. To operationalize the critical requirements identified in Section 1, specifically the inherent conflict between enforcing strict bottom-line guarantees (R2) and optimizing for robustness and user alignment (R1, R3), we move beyond monolithic scalar reward models. Drawing inspiration from recent work on rubric-based rewards [9, 10, 15, 32], we design a hierarchical and multi-dimensional reward system.

**中文**

形式上，令 𝑥=(𝑞, ℎ, 𝐸) 表示由查询 𝑞、会话历史记录 ℎ 和检索到的证据集 𝐸 组成的输入上下文，并令 𝑦 表示生成的序列，其中包含意图计划和最终答案。为了实施第 1 节中确定的关键要求，特别是执行严格的底线保证 (R2) 与优化鲁棒性和用户一致性 (R1、R3) 之间的固有冲突，我们超越了单一的标量奖励模型。从最近基于标题的奖励研究中汲取灵感[9,10,15,32]，我们设计了一个分层和多维的奖励系统。

### 段落 33 · Page 4

**EN**

This system explicitly decouplesbottom-line constraints, which ensure non-negotiable safety and reliability, from behavioral optimization objectives, which target robustness and preference alignment. This separation ensures that the model prioritizes foundational guarantees while simultaneously optimizing the user’s search experience across the entire pipeline, from intent planning and evidence selection to final response synthesis. 3.2.1 Reward Design.We formalize the evaluation of a model generation 𝑦 for a given search interaction context 𝑥 through a structured set of evaluation criteria C.

**中文**

该系统明确地将确保不可协商的安全性和可靠性的底线约束与以鲁棒性和偏好调整为目标的行为优化目标脱钩。这种分离确保模型优先考虑基本保证，同时优化整个管道中的用户搜索体验，从意图规划和证据选择到最终响应合成。 3.2.1 奖励设计。我们通过一组结构化的评估标准 C，将给定搜索交互上下文 𝑥 的模型生成 𝑦 的评估形式化。

### 段落 34 · Page 4

**EN**

Unlike standard RLHF [26] which often conflates diverse quality signals into a single scalar, we categorize our criteria into two distinct layers: Layer I: Bottom-line Constraints.This layer encodes Requirement R2 (Reliability and Safety). It consists of binary or near-binary criteria that serve as hard constraints. Failure in these dimensions renders a response unusable. We define a subset of criteriaC𝐵𝐿 ⊂ C covering three critical aspects: • Hallucination & Factual Grounding:To mitigate misinformation, we rigorously assess hallucination at both the sentence and claim levels, ensuring that the generated answer is factually accurate.

**中文**

与标准 RLHF [26] 经常将不同的质量信号合并为一个标量不同，我们将我们的标准分为两个不同的层：第一层：底线约束。该层编码要求 R2（可靠性和安全性）。它由作为硬约束的二元或近二元标准组成。这些维度的失败会导致响应无法使用。我们定义了一个标准子集C𝐵𝐿⊂C，涵盖三个关键方面： • 幻觉和事实依据：为了减少错误信息，我们严格评估句子和主张层面的幻觉，确保生成的答案实际上是准确的。

### 段落 35 · Page 4

**EN**

Additionally, we verify consistency with external knowledge bases and enforce strict refusal behaviors when retrieved evidence is insufficient to answer the query. • Basic Answer Quality:This subset ensures the fundamental logic and readability of the response. It detects logical inconsistencies within a single turn, contradictions across multi-turn interactions, and filters out gibberish or low-quality text. • Format Compliance:To ensure the response is structurally consumable, we enforce strict formatting rules, including adherence to Markdown and constraints on response length.

**中文**

此外，我们验证与外部知识库的一致性，并在检索到的证据不足以回答查询时强制执行严格的拒绝行为。 • 基本答案质量：该子集确保响应的基本逻辑和可读性。它可以检测单轮内的逻辑不一致、多轮交互中的矛盾，并过滤掉乱码或低质量文本。 • 格式合规性：为了确保回复在结构上可使用，我们执行严格的格式规则，包括遵守 Markdown 和对回复长度的限制。

### 段落 36 · Page 4

**EN**

Layer II: Behavioral Objectives.Once bottom-line constraints are satisfied, the model should be optimized for robustness (R1) and user utility (R3). This layer, denoted as C𝐵𝐻 ⊂ C , specifically targets increasing user engagement with the generated responses. Key dimensions include: • Robustness to Query & Evidence:This subset focuses on the complexity of open-ended generative search. On the query side, we evaluate intent alignment to ensure the model addresses the user’s core question.

**中文**

第二层：行为目标。一旦满足底线约束，就应该针对鲁棒性 (R1) 和用户效用 (R3) 优化模型。该层表示为 C𝐵𝐻 ⊂ C，专门致力于提高用户对生成的响应的参与度。关键维度包括： • 查询和证据的稳健性：该子集重点关注开放式生成搜索的复杂性。在查询方面，我们评估意图一致性，以确保模型解决用户的核心问题。

### 段落 37 · Page 4

**EN**

On the evidence side, we assess how useful the utilized content is for answering the query and how likely it is to satisfy the user, while penalizing the inclusion of irrelevant or conflicting information. Furthermore, we evaluate the quality of planning and reasoning under uncertainty. • Richness & Diversity:To enhance the depth of information and avoid overly narrow answers, we encourage the generation of diverse yet relevant claims, ensuring the response covers multiple perspectives or facets of the topic rather than repeating a single point. • Conciseness & Usability:To optimize the consumption experience, we prioritize usability metrics.

**中文**

在证据方面，我们评估所使用的内容对于回答查询的有用性以及满足用户的可能性有多大，同时对包含不相关或冲突的信息进行惩罚。此外，我们评估不确定性下规划和推理的质量。 • 丰富性和多样性：为了增强信息的深度并避免过于狭窄的答案，我们鼓励生成多样化但相关的主张，确保答案涵盖主题的多个观点或方面，而不是重复单一观点。 • 简洁性和可用性：为了优化消费体验，我们优先考虑可用性指标。

### 段落 38 · Page 4

**EN**

This includes the "answerfirst" principle (placing the core answer at the beginning), reducing semantic redundancy, and minimizing off-topic or tangential content to ensure a high signal-to-noise ratio. Table 5 (Appendix C) provides the detailed definitions for all criteria discussed above, alongside their specific implementation types which we detail in the following section.

**中文**

这包括“答案优先”原则（将核心答案放在开头）、减少语义冗余、尽量减少离题或离题的内容，以确保高信噪比。表 5（附录 C）提供了上述所有标准的详细定义，以及我们在下一节中详细介绍的具体实现类型。

### 段落 39 · Page 4

**EN**

3.2.2 Implementation of Hybrid Evaluation Stack.To ensure our reward signals are both scalable and diagnostically precise, we operationalize a hybrid evaluation stack that integrates deterministic rules (e.g., n-gram statistics, regex constraints) for objective criteria with LLM-based judges for complex semantic dimensions. Aligning these LLM judges with human expert preferences is nontrivial; strictly relying on single-pass annotation often leads to noisy ground truth. To address this, we establish a rigorous human-in-theloop calibration cycle.

**中文**

3.2.2 混合评估堆栈的实现。为了确保我们的奖励信号既可扩展又具有诊断精确性，我们操作了一个混合评估堆栈，该堆栈集成了客观标准的确定性规则（例如，n-gram 统计、正则表达式约束）和基于 LLM 的复杂语义维度判断。让这些法学硕士法官与人类专家的偏好保持一致并非易事。严格依赖单遍注释通常会导致嘈杂的基本事实。为了解决这个问题，我们建立了严格的人机交互校准周期。

### 段落 40 · Page 4

**EN**

Figure 9 shows the annotation interface used for this process, where experts provide both fine-grained scores and holistic pairwise rankings. To strictly control annotation quality and mitigate cognitive inertia (anchoring bias) where annotators might over-trust the model’s generated reasoning, we enforce a dual-track annotation protocol involving two distinct groups: • Blind Group:Annotators score responses based on the query and answer text, without access to the reward system’s internal reasoning or intermediate steps. This establishes an unbiased baseline that reflects the end-user’s consumption experience.

**中文**

图 9 显示了用于此过程的注释界面，其中专家提供细粒度分数和整体成对排名。为了严格控制注释质量并减轻注释者可能过度信任模型生成的推理的认知惯性（锚定偏差），我们强制实施涉及两个不同组的双轨注释协议： • 盲组：注释者根据查询和答案文本对响应进行评分，而无需访问奖励系统的内部推理或中间步骤。这建立了反映最终用户消费体验的公正基线。

### 段落 41 · Page 4

**EN**

• Assisted Group:Annotators review the response alongside the reward system’s CoT and evidence citations. This setup enables them to verify logical consistency and detect subtle hallucinations that are factually incorrect but linguistically plausible. Discrepancies between the Blind and Assisted scores serve as highvalue signals for identifying policy gaps; these conflict cases are escalated to senior experts for adjudication to resolve edge-case ambiguities and unify evaluation standards.

**中文**

• 协助小组：注释者审查响应以及奖励系统的 CoT 和证据引用。这种设置使他们能够验证逻辑一致性并检测实际上不正确但语言上合理的微妙幻觉。盲分数和辅助分数之间的差异可以作为识别政策差距的高价值信号；这些冲突案例将上报给高级专家进行裁决，以解决边缘案例的模糊性并统一评估标准。

### 段落 42 · Page 4

**EN**

Finally, before any version update, the evaluator must demonstrate non-degradation on a frozen regression benchmark and undergo a stable "shadow run" in the production environment. 3.3 Reinforcement Learning Framework Optimizing policy models against such a composite and fine-grained reward system presents a unique challenge. A naive linear combination of these diverse signals often exacerbates the "seesaw effect" [10], where the model exploits easier-to-optimize reward signals (e.g., length-based scores) at the expense of rigid bottomline constraints such as factual consistency.

**中文**

最后，在任何版本更新之前，评估者必须在冻结回归基准上证明不降级，并在生产环境中进行稳定的“影子运行”。 3.3 强化学习框架 针对这种复合且细粒度的奖励系统优化政策模型提出了独特的挑战。这些不同信号的简单线性组合通常会加剧“跷跷板效应”[10]，其中模型利用更容易优化的奖励信号（例如基于长度的分数），但牺牲了严格的底线约束（例如事实一致性）。

### 段落 43 · Page 4

**EN**

To robustly operationalize this multi-dimensional feedback without succumbing to reward hacking, we introduce aGated Aggregation Strategy. For

**中文**

为了稳健地实施这种多维反馈而不屈服于奖励黑客，我们引入了门控聚合策略。对于

### Page 5

### 段落 44 · Page 5

**EN**

Aligning Large Language Models with Searcher Preferences KDD ’26, August 9–13, 2026, Jeju, Korea a given model generation 𝑦, let 𝑆𝐵𝐿 ={𝑠 1, . . . , 𝑠𝑚 } be the normalized scores from the bottom-line criteria defined in Layer I, and let 𝑆𝐵𝐻 ={𝑠 ′ 1, . . . , 𝑠′ 𝑛 } be the normalized scores from the behavioral criteria defined in Layer II, with associated expert-defined weights 𝑊={𝑤 1, . . . , 𝑤𝑛 }. We assume that each score lies in the unit interval,i.e. 𝑠𝑖 ∈ [ 0, 1] for 𝑖= 1, . . . , 𝑚 and 𝑠 ′ 𝑖 ∈ [ 0, 1] for 𝑖= 1, . . . , 𝑛. We compute the bottom-line factor via a 𝛿-smoothed geometric mean 𝐵𝛿 (𝑥, 𝑦)=exp 1 𝑚 𝑚∑︁ 𝑖=1 log 𝑠𝑖 +𝛿 1+𝛿 !

**中文**

将大型语言模型与搜索者偏好保持一致 KDD’26，2026 年 8 月 9 日至 13 日，韩国济州岛给定模型生成 𝑦，令 𝑆𝐵𝐿 ={𝑠 1, .。。 , 𝑠𝑚 } 是层 I 中定义的底线标准的归一化分数，并令 𝑆𝐵𝐻 ={𝑠 ′ 1, .。。 , 𝑠′ 𝑛 } 是第二层定义的行为标准的归一化分数，以及相关的专家定义的权重 𝑊={𝑤 1, .。。，𝑤𝑛}。我们假设每个分数都位于单位区间内，即𝑠𝑖 ∈ [ 0, 1] 对于 𝑖= 1, .。。 , 𝑚 和 𝑠 ′ 𝑖 ∈ [ 0, 1] 对于 𝑖= 1, .。。，𝑛。我们通过 𝛿 平滑几何平均值 𝐵𝛿 (𝑥, 𝑦)=exp 1 𝑚 𝑚Σ︁ 𝑖=1 log 𝑠𝑖 +𝛿 1+𝛿 计算底线因子！

### 段落 45 · Page 5

**EN**

, 𝛿>0,(1) which acts as a soft-AND gate while improving optimization stability. In the vanilla form (i.e.,𝛿=0), 𝐵0 (𝑥, 𝑦)= 𝑚Ö 𝑖=1 𝑠𝑖 ! 1/𝑚 =exp 1 𝑚 𝑚∑︁ 𝑖=1 log𝑠 𝑖 ! , the gate can become numerically unstable when computed in the log-domain due tolog 0and exhibits unbounded sensitivity 𝜕log𝐵 0 (𝑥, 𝑦) 𝜕𝑠𝑖 = 1 𝑚𝑠𝑖 , when 𝑠𝑖 → 0. The 𝛿-smoothing avoids log 0and upper-bounds the gate sensitivity: 𝜕log𝐵 𝛿 (𝑥, 𝑦) 𝜕𝑠𝑖 = 1 𝑚(𝑠 𝑖 +𝛿) ≤ 1 𝑚𝛿 . Moreover, when any bottom-line metric is near zero, 𝐵𝛿 remains strongly suppressed in a 𝛿-controlled manner, yielding a substantially reduced reward.

**中文**

, 𝛿>0,(1) 充当软与门，同时提高优化稳定性。在普通形式中（即𝛿=0），𝐵0 (𝑥, 𝑦)= 𝑚Ö 𝑖=1 𝑠𝑖！ 1/𝑚 =exp 1 𝑚 𝑚Σ︁ 𝑖=1 log𝑠 𝑖！，当在对数域中计算时，由于 log 0，门可能会变得数值不稳定，并表现出无限的敏感性 𝜕log𝐵 0 (𝑥, 𝑦) 𝜕𝑠𝑖 = 1 𝑚𝑠𝑖，当 𝑠𝑖 → 0 时。𝛿平滑避免了 log 0 和门灵敏度上限： 𝜕log𝐵 𝛿 (𝑥, 𝑦) 𝜕𝑠𝑖 = 1 𝑚(𝑠 𝑖 +𝛿) ≤ 1 𝑚𝛿。此外，当任何底线指标接近于零时，𝐵𝛿仍然以𝛿控制的方式受到强烈抑制，从而导致奖励大幅减少。

### 段落 46 · Page 5

**EN**

Conversely, we compute the behavioral utility as a weighted arithmetic mean 𝑈(𝑥, 𝑦)= Í𝑛 𝑖=1 𝑤𝑖𝑠 ′ 𝑖Í𝑛 𝑖=1 𝑤𝑖 ,(2) which allows for flexible trade-offs among softer objectives within the safe region. The final scalar reward is then defined as 𝑅(𝑥, 𝑦)=𝐵 𝛿 (𝑥, 𝑦)𝑈(𝑥, 𝑦),(3) so that behavioral improvements act as multipliers when bottomline scores are sufficiently high. To optimize the policy under this reward surface, we employ Group Relative Policy Optimization (GRPO) [27].

**中文**

相反，我们将行为效用计算为加权算术平均值 𝑈(𝑥, 𝑦)= Í𝑛 𝑖=1 𝑤𝑖𝑠 ′ 𝑖Í𝑛 𝑖=1 𝑤𝑖 ,(2)，这允许在安全区域内的较软目标之间进行灵活的权衡。最终的标量奖励定义为 𝑅(𝑥, 𝑦)=𝐵 𝛿 (𝑥, 𝑦)𝑈(𝑥, 𝑦),(3)，以便当底线分数足够高时，行为改进可以起到乘数的作用。为了优化这个奖励表面下的策略，我们采用了组相对策略优化（GRPO）[27]。

### 段落 47 · Page 5

**EN**

Unlike standard PPO [ 26] which relies on a value network, GRPO normalizes advantages within a group of sampled outputs for the same query, making it efficient for our large-scale setting. Formally, let 𝜋𝜃 denote the policy to be optimized and 𝜋𝜃old the behavior policy used to collect trajectories. For a query 𝑥, we sample a group of generations {𝑦𝑖 }𝐺 𝑖=1, where each 𝑦𝑖 is a token sequence𝑦 𝑖 =(𝑦 𝑖,1, . . . , 𝑦𝑖,|𝑦 𝑖 | ).

**中文**

与依赖于价值网络的标准 PPO [26] 不同，GRPO 标准化了同一查询的一组采样输出中的优势，使其对于我们的大规模设置来说非常高效。正式地，让 𝜋𝜃 表示要优化的策略，𝜋𝜃old 表示用于收集轨迹的行为策略。对于查询 𝑥，我们对一组生成 {𝑦𝑖 }𝐺 𝑖=1 进行采样，其中每个 𝑦𝑖 是一个标记序列𝑦 𝑖 =(𝑦 𝑖,1, . . , 𝑦𝑖,|𝑦 𝑖 | )。

### 段落 48 · Page 5

**EN**

The GRPO objective is JGRPO (𝜃)=E 𝑥∼𝐷,{𝑦 𝑖 }𝐺 𝑖=1 ∼𝜋𝜃old (·|𝑥) " 1 𝐺 𝐺∑︁ 𝑖=1 1 |𝑦 𝑖 | |𝑦𝑖 |∑︁ 𝑡=1  min  𝑟𝑖,𝑡 (𝜃) ˆ𝐴𝑖,𝑡 , clip 𝑟𝑖,𝑡 (𝜃),1−𝜖,1+𝜖  ˆ𝐴𝑖,𝑡  −𝜆𝐷 KL (𝜋𝜃 | |𝜋ref ) # , (4) where𝜆is the coefficient controlling the KL divergence. 𝑟𝑖,𝑡 (𝜃)= 𝜋𝜃 𝑦𝑖,𝑡 |𝑥, 𝑦 𝑖,<𝑡  𝜋𝜃old 𝑦𝑖,𝑡 |𝑥, 𝑦 𝑖,<𝑡  ,(5) is the per-token importance-weighted ratio. The token-wise advantages ˆ𝐴𝑖,𝑡 are obtained by normalizing the group rewards: ˆ𝐴𝑖,𝑡 = 𝑅(𝑥, 𝑦 𝑖 ) −mean {𝑅(𝑥, 𝑦 𝑗 ) }𝐺 𝑗=1  std {𝑅(𝑥, 𝑦 𝑗 ) }𝐺 𝑗=1  , 𝑡=1, . . . ,|𝑦 𝑖 |.(6) 4 Experiments In this section, we evaluate the effectiveness of our proposed reward system and RL training framework.

**中文**

GRPO 目标为 JGRPO (𝜃)=E 𝑥∼𝐷,{𝑦 𝑖 }𝐺 𝑖=1 ∼𝜋𝜃old (·|𝑥) " 1 𝐺 𝐺Σ︁ 𝑖=1 1 |𝑦 𝑖 | |𝑦𝑖 |Σ︁ 𝑡=1 分钟 𝑟𝑖,𝑡 (𝜃) ˆ𝐴𝑖,𝑡 , 剪辑 𝑟𝑖,𝑡 (𝜃),1−𝜖,1+𝜖 ˆ𝐴𝑖,𝑡 −𝜆𝐷 KL (𝜋𝜃 | |𝜋ref ) # , (4) 其中𝜆是控制 KL 散度的系数 𝑟𝑖,𝑡 (𝜃)= 𝜋𝜃 𝑦𝑖,𝑡 |𝑥, 𝑦 𝑖,<𝑡 𝜋𝜃old。 𝑦𝑖,𝑡 |𝑥, 𝑦 𝑖,<𝑡 ,(5) 是每个令牌重要性加权比率 ˆ𝐴𝑖,𝑡 通过标准化组奖励获得： ˆ𝐴𝑖,𝑡 = 𝑅(𝑥, 𝑦)。 𝑖 ) −均值 {𝑅(𝑥, 𝑦 𝑗) }𝐺 𝑗=1 std {𝑅(𝑥, 𝑦 𝑗) }𝐺 𝑗=1 , 𝑡=1, .(6) 4实验在本节中，我们评估了我们提出的奖励系统和强化学习训练框架的有效性。

### 段落 49 · Page 5

**EN**

We aim to answer the following research questions: • RQ1:How effectively does our multi-dimensional reward system align with human expert judgments compared to state-ofthe-art reward modeling baselines? • RQ2:Does the proposed optimization strategy yield better offline generation quality? • RQ3:How does the Gated Aggregation Strategy influence training dynamics and coordinate different reward dimensions? • RQ4:What is the impact of the deployed model in online settings on real-world user engagement and safety metrics?

**中文**

我们的目标是回答以下研究问题： • RQ1：与最先进的奖励建模基线相比，我们的多维奖励系统与人类专家判断的一致性如何？ • RQ2：所提出的优化策略是否能产生更好的离线发电质量？ • RQ3：门控聚合策略如何影响训练动态并协调不同的奖励维度？ • RQ4：在线环境中部署的模型对现实世界的用户参与度和安全指标有何影响？

### 段落 50 · Page 5

**EN**

4.1 Experimental Setup 4.1.1 Datasets.To support the training and evaluation of our framework, we construct four distinct datasets derived from Red- Note search logs: aReward Training Dataset ( DRM-Train)for calibration, two diagnostic test sets (DEval-Dim and DEval-Holistic) for reward validation, and a large-scale unlabeledRL Optimization Dataset ( DRL). Detailed statistics and construction protocols for these datasets are provided in Appendix D. 4.1.2 Baselines.To validate our contributions, we benchmark our approach against state-of-the-art methods from two perspectives: reward quality (RQ1) and policy optimization effectiveness (RQ2–4).

**中文**

4.1 实验设置 4.1.1 数据集。为了支持我们框架的训练和评估，我们构建了来自 Red-Note 搜索日志的四个不同的数据集：用于校准的奖励训练数据集（DRM-Train）、用于奖励验证的两个诊断测试集（DEval-Dim 和 DEval-Holistic）以及一个大规模未标记的 RL 优化数据集（DRL）。附录 D 中提供了这些数据集的详细统计数据和构建协议。 4.1.2 基线。为了验证我们的贡献，我们从两个角度对我们的方法与最先进的方法进行基准测试：奖励质量（RQ1）和策略优化有效性（RQ2-4）。

### 段落 51 · Page 5

**EN**

Reward Modeling Baselines.We compare our reward system against the most advanced reward modeling paradigms: • GenRM (Generative Reward Model):This baseline trains an LLM to generate a Chain-of-Thought (CoT) reasoning trace before outputting final scores [18, 39]. • Rubric (Rubric-Based Reward):Following [ 12], this baseline trains a rubric generator via supervised fine-tuning on a small set of expert-written query–rubric pairs, then uses it to generate query-specific rubrics for each reward dimension to compute the rubric-based reward.

**中文**

奖励建模基线。我们将我们的奖励系统与最先进的奖励建模范例进行比较： • GenRM（生成奖励模型）：该基线训练法学硕士在输出最终分数之前生成思想链（CoT）推理轨迹[18, 39]。 • Rubric（基于Rubric的奖励）：按照[12]，该基线通过对一小组专家编写的查询-Rubric对进行监督微调来训练Rubric生成器，然后使用它为每个奖励维度生成特定于查询的Rubric以计算基于Rubric的奖励。

### 段落 52 · Page 5

**EN**

Policy Baselines.All policy models are initialized from the same SFT checkpoint, which was trained on high-quality business data to ensure basic service capability. We compare the following optimization strategies: • RFT (Rejection Sampling Fine-tuning):An iterative alignment method where the model generates multiple candidates per query, and the highest-scoring are selected to build a new dataset for this round of SFT [31, 37]. • DPO (Direct Preference Optimization):An offline method that optimizes the policy directly on preference data [25], bypassing the explicit reward modeling step.

**中文**

策略基线。所有策略模型均从同一个SFT检查点初始化，并接受高质量的业务数据训练，以保证基本的服务能力。我们比较以下优化策略： • RFT（拒绝采样微调）：一种迭代对齐方法，模型每次查询生成多个候选，并选择得分最高的为本轮 SFT 构建新的数据集[31, 37]。 • DPO（直接偏好优化）：一种离线方法，直接根据偏好数据优化策略[25]，绕过显式奖励建模步骤。

### 段落 53 · Page 5

**EN**

• GRPO-GenRM:GRPO [ 27] using the trained GenRM’s outputs as the reward signal. • GRPO-Linear:A variant of our framework that utilizes our multi-dimensional reward signals but aggregates them via a naive weighted sum. • GRPO-Gated (Ours):Our proposed method utilizing the Gated Aggregation Strategy. 4.1.3 Evaluation Metrics.We employ a comprehensive set of metrics to assess both reward alignment and real-world performance.

**中文**

• GRPO-GenRM：GRPO [27]使用经过训练的GenRM的输出作为奖励信号。 • GRPO-线性：我们框架的一个变体，它利用我们的多维奖励信号，但通过朴素的加权和来聚合它们。 • GRPO-Gated（我们的）：我们提出的方法利用门控聚合策略。 4.1.3 评估指标。我们采用一套全面的指标来评估奖励一致性和实际绩效。

### Page 6

### 段落 54 · Page 6

**EN**

KDD ’26, August 9–13, 2026, Jeju, Korea Wei Wu, Peilun Zhou, et al. Table 1: Comparison on pointwise constraint of our reward system against multiple baselines. Metric reported is Accuracy. Layer Req.

**中文**

KDD ’26，2026 年 8 月 9-13 日，韩国济州 Wei Wu、Peilun Zhou 等。表 1：我们的奖励系统的逐点约束与多个基线的比较。报告的指标是准确性。图层要求

### 段落 55 · Page 6

**EN**

Subset Reward Dimension GenRM Rubric Ours Behavioral R1 Query Query Satisfy 71.52 73.3187.24 Evidence Reference Conflict 79.01 70.4890.84 Reference Irrelevant 88.92 83.6394.96 Bottom-line R2 Basic Quality Answer Quality 64.02 65.6982.43 Self Consistency 59.68 64.2278.20 Multi-turn Repeat/Conflict 80.60 83.4094.20 Hallucination Highlight Hallucination 49.34 69.0592.85 Claim Hallucination 52.93 66.8491.88 LLM Knowledge 84.19 84.1985.77 Table 2: Comparison on pairwise preference of our reward system against multiple baselines. Metric reported is AUC. Layer Req.

**中文**

子集奖励维度 GenRM 评分表 我们的行为 R1 查询 查询满足 71.52 73.3187.24 证据参考冲突 79.01 70.4890.84 参考不相关 88.92 83.6394.96 底线 R2 基本质量 答案质量 64.02 65.6982.43 自我一致性 59.68 64.2278.20 多轮重复/冲突 80.60 83.4094.20 幻觉突出幻觉 49.34 69.0592.85 声明幻觉 52.93 66.8491.88 LLM 知识 84.19 84.1985.77 表 2：成对比较我们的奖励系统相对于多个基线的偏好。报告的指标是 AUC。图层要求

### 段落 56 · Page 6

**EN**

Subset Reward Dimension GenRM Rubric Ours Behavioral R1 Query Planning Quality 84.74 73.6889.47 Evidence Reference Beneficiality 79.56 72.4194.83 Reference Diversity 72.60 96.4497.86 Reference Satisfaction 76.04 82.2984.38 R3 Richness Claim Diversity 77.69 87.4096.07 Concise/ Usability Answer Firstness 80.47 95.0597.66 Answer Useful 77.34 79.0896.07 Redundant Repetition 78.01 85.8698.43 Table 3: Comparison of holistic preference alignment. Method AUC GenRM 70.90 Rubric 72.13 Reward System (Ours)86.48 For offline evaluation, we utilizeAccuracy (ACC)andArea Under the Curve (AUC)to measure agreement with human experts.

**中文**

子集奖励维度 GenRM Rubric 我们的行为 R1 查询规划质量 84.74 73.6889.47 证据参考效益 79.56 72.4194.83 参考多样性 72.60 96.4497.86 参考满意度 76.04 82.2984.38 R3 丰富性声明多样性77.69 87.4096.07 简洁/可用性 答案优先性 80.47 95.0597.66 答案有用 77.34 79.0896.07 冗余重复 78.01 85.8698.43 表 3：整体偏好调整的比较。方法 AUC GenRM 70.90 Rubric 72.13 奖励系统（我们的）86.48 对于离线评估，我们利用准确度 (ACC) 和曲线下面积 (AUC) 来衡量与人类专家的一致性。

### 段落 57 · Page 6

**EN**

For online deployment, we monitor user engagement viaValid Consumption Rate (VCR),Skip Rate (SR),Re-search Rate (RR), andBad Case Rate (BCR). Detailed definitions and mathematical formulations for these metrics are provided in Appendix E. 4.1.4 Implementation Details.All experiments are conducted on 18 nodes equipped with NVIDIA H800 GPUs where 16 nodes are dedicated to the reward system deployment. We implement the training pipeline using the verl [ 28] library where we leverage Megatron [19] for distributed training and vLLM [13] for efficient generation rollouts.

**中文**

对于在线部署，我们通过有效消费率 (VCR)、跳过率 (SR)、重新搜索率 (RR) 和不良案例率 (BCR) 来监控用户参与度。附录 E 中提供了这些指标的详细定义和数学公式。 4.1.4 实施细节。所有实验均在配备 NVIDIA H800 GPU 的 18 个节点上进行，其中 16 个节点专用于奖励系统部署。我们使用 verl [28] 库实现训练管道，其中我们利用 Megatron [19] 进行分布式训练，并利用 vLLM [13] 进行高效的生成推广。

### 段落 58 · Page 6

**EN**

The policy model is initialized from Qwen3-30B- A3B-Instruct-2507 [36] while the entire reward evaluation stack is powered by DeepSeek-R1 [11] to ensure reasoning-dense feedback. We adopt an on-policy optimization configuration with a global batch size of 128 and sample 16 completions per prompt at a temperature of 1.0. The optimization utilizes the AdamW [17] optimizer with 𝛽1 = 0.9and 𝛽2 = 0.95plus a weight decay of 0.1 alongside a learning rate of1 × 10−6 and a KL-divergence coefficient 𝜆 of 0.01. For the Gated Aggregation in Eq. 1, we set𝛿=10 −2.

**中文**

策略模型从 Qwen3-30B-A3B-Instruct-2507 [36] 初始化，而整个奖励评估堆栈由 DeepSeek-R1 [11] 提供支持，以确保推理密集反馈。我们采用策略优化配置，全局批量大小为 128，并在温度为 1.0 时对每个提示采样 16 个完成。该优化利用 AdamW [17] 优化器，其中 𝛽1 = 0.9 和 𝛽2 = 0.95，加上 0.1 的权重衰减，以及 1 × 10−6 的学习率和 0.01 的 KL 散度系数 𝜆。对于方程中的门控聚合。 1、我们设𝛿=10−2。

### 段落 59 · Page 6

**EN**

4.2 Validation of Reward System (RQ1) To evaluate the alignment of our reward system with human expert preferences, we compare on theD Eval-Dim and theD Eval-Holistic. 4.2.1 Dimension-Specific Alignment.Tables 1 and 2 show that our hybrid evaluation stack consistently outperforms standard GenRM and Rubric-based baselines across both bottom-line and behavioral layers. In safety and factual grounding (Table 1), our system achieves superior accuracy. Although the Rubric-based method improves upon GenRM by decomposing complex tasks into explicit criteria to reduce holistic scoring ambiguity, it still falls short of our approach.

**中文**

4.2 奖励系统的验证（RQ1） 为了评估我们的奖励系统与人类专家偏好的一致性，我们比较了 D Eval-Dim 和 theD Eval-Holistic。 4.2.1 特定维度的对齐。表 1 和表 2 显示，我们的混合评估堆栈在底线层和行为层上始终优于标准 GenRM 和基于 Rubric 的基线。在安全和事实接地方面（表 1），我们的系统实现了卓越的准确性。尽管基于 Rubric 的方法通过将复杂的任务分解为明确的标准来减少整体评分的模糊性，从而改进了 GenRM，但它仍然达不到我们的方法。

### 段落 60 · Page 6

**EN**

This gap persists because standard Rubrics struggle with ambiguous instructions and content variability, whereas our human-in-the-loop calibration ensures strict alignment with expert consensus. This enables us to enforce bottom-line guarantees that pure LLM judges occasionally miss. Furthermore, GenRM exhibits lower stability due to its high sensitivity to training data distribution, which leads to inconsistent performance on out-ofdistribution safety violations. Table 2 demonstrates our pairwise ranking capability for subjective behavioral objectives, where our approach shows a significant advantage in Robustness and Conciseness.

**中文**

这种差距之所以持续存在，是因为标准评分标准难以应对不明确的说明和内容可变性，而我们的人机交互校准可确保与专家共识严格一致。这使我们能够执行纯粹的法学硕士法官偶尔会错过的底线保证。此外，GenRM 由于对训练数据分布高度敏感，稳定性较低，导致分布外安全违规的性能不一致。表 2 展示了我们对主观行为目标的成对排名能力，其中我们的方法在稳健性和简洁性方面显示出显着优势。

### 段落 61 · Page 6

**EN**

Decoupling these sub-dimensions into interpretable criteria within a human-calibrated hybrid stack allows our system to provide more stable and fine-grained signals. In contrast, while GenRM generates reasoning traces, the Rubric baseline offers more structured diagnosis through explicit criteria yet lacks the continuous expert calibration loop required to align precisely with nuanced human preferences in open-ended generative search. 4.2.2 Holistic Preference Alignment.Table 3 presents holistic alignment results on DEval-Holistic.

**中文**

将这些子维度解耦为人工校准的混合堆栈中的可解释标准，使我们的系统能够提供更稳定和更细粒度的信号。相比之下，虽然 GenRM 生成推理轨迹，但 Rubric 基线通过明确的标准提供了更加结构化的诊断，但缺乏在开放式生成搜索中精确符合人类微妙偏好所需的连续专家校准循环。 4.2.2 整体偏好对齐。表3呈现了DEval-Holistic的整体对齐结果。

### 段落 62 · Page 6

**EN**

Our multi-dimensional reward system achieves the highest overall agreement with human preferences and surpasses GenRM and the Rubric-based baseline. This result validates the effectiveness of our two-layer design separates nonnegotiable safeguards from user-facing quality objectives to capture

**中文**

我们的多维奖励系统与人类偏好达到了最高的总体一致性，并超越了 GenRM 和基于 Rubric 的基线。这一结果验证了我们的两层设计的有效性，将不可协商的保障措施与面向用户的质量目标分开，以捕获

### Page 7

### 段落 63 · Page 7

**EN**

Aligning Large Language Models with Searcher Preferences KDD ’26, August 9–13, 2026, Jeju, Korea Table 4: Comparison of different optimization methods across all reward dimensions.

**中文**

将大型语言模型与搜索者偏好保持一致 KDD’26，2026 年 8 月 9 日至 13 日，韩国济州 表 4：所有奖励维度上不同优化方法的比较。

### 段落 64 · Page 7

**EN**

Robustness (R1) Bottom-line (R2) Alignment (R3) Method Query Evidence Basic Hallu Format Rich Usability SFT 0.9167 0.5809 0.9675 0.9176 0.9697 0.9222 0.7939 RFT 0.9720 0.58800.99300.9260 0.9890 0.9600 0.8950 DPO 0.9540 0.6120 0.9885 0.9510 0.9745 0.9690 0.8610 GRPO-GenRM 0.9630 0.5980 0.9870 0.9340 0.96700.98400.8450 GRPO-Linear 0.9636 0.5861 0.9906 0.9714 0.9730 0.9738 0.8604 GRPO-Gated0.9959 0.70890.98750.9836 0.99250.98320.9099 0 20 40 60 80 100 Preference rate (%) Ours vs SFT Ours vs DPO 44% 44% 12% 39% 40% 21% Win (Ours better) Tie Lose (Baseline better) Figure 3: Comparison on generation quality of our policy against multiple baselines evaluated by human experts.

**中文**

稳健性 (R1) 底线 (R2) 一致性 (R3) 方法查询证据 基本 Hallu 格式 丰富的可用性 SFT 0.9167 0.5809 0.9675 0.9176 0.9697 0.9222 0.7939 RFT 0.9720 0.58800.99300.9260 0.9890 0.9600 0.8950 DPO 0.9540 0.6120 0.9885 0.9510 0.9745 0.9690 0.8610 GRPO-GenRM 0.9630 0.5980 0.9870 0.9340 0.96700.98400.8450 GRPO-线性 0.9636 0.5861 0.9906 0.9714 0.9730 0.9738 0.8604 GRPO-门控0.9959 0.70890.98750.9836 0.99250.98320.9099 0 20 40 60 80 100 偏好率 (%) 我们的 vs SFT 我们的 vs DPO 44% 44% 12% 39% 40% 21% 赢（我们更好） 平局 输（基线更好） 图 3：我们的策略的生成质量与人类专家评估的多个基线的比较。

### 段落 65 · Page 7

**EN**

the complexity of human judgments. The consistent superiority across all subsets confirms that the proposed reward system serves as a reliable objective for the GRPO-based policy optimization. 4.3 Offline Policy Evaluation (RQ2) To verify whether our proposed optimization strategy translates better reward signals into superior generation quality, we conduct a comprehensive offline evaluation. Relying on the high alignment of our reward system with human judgment demonstrated in RQ1, we employ the system itself as an automated proxy evaluator alongside rigorous human expert assessment.

**中文**

人类判断的复杂性。所有子集的一致优越性证实了所提出的奖励系统是基于 GRPO 的策略优化的可靠目标。 4.3 离线策略评估（RQ2） 为了验证我们提出的优化策略是否将更好的奖励信号转化为卓越的发电质量，我们进行了全面的离线评估。依靠我们的奖励系统与 RQ1 中展示的人类判断的高度一致性，我们将系统本身用作自动代理评估器以及严格的人类专家评估。

### 段落 66 · Page 7

**EN**

4.3.1 Automatic Evaluation via Reward System.Table 4 presents the performance of different policy variants evaluated by our multidimensional reward system. To facilitate comparison, we report average scores of dimensions within each subset. The results indicate that GRPO-Gated (Ours) achieves the best overall performance, significantly surpassing the SFT baseline and other optimization methods. While RFT and DPO improve upon the SFT baseline, they exhibit limitations in balancing conflicting objectives.

**中文**

4.3.1 通过奖励系统自动评估。表 4 展示了我们的多维奖励系统评估的不同政策变体的绩效。为了便于比较，我们报告每个子集中维度的平均得分。结果表明，GRPO-Gated（我们的）实现了最佳的整体性能，显着超越了 SFT 基线和其他优化方法。虽然 RFT 和 DPO 在 SFT 基线上有所改进，但它们在平衡相互冲突的目标方面表现出局限性。

### 段落 67 · Page 7

**EN**

Specifically, DPO tends to exploit easy-to-optimize patterns like response length while often failing to strictly adhere to complex safety constraints. Among the GRPO variants, GRPO-GenRM shows instability in safety dimensions due to the lack of hard constraints in its reward signal. GRPO-Linear, utilizing a weighted sum aggregation, suffers from the seesaw effect where improvements in behavioral scores come at the cost of degradation in bottom-line metrics.

**中文**

具体来说，DPO 倾向于利用易于优化的模式（例如响应长度），但往往无法严格遵守复杂的安全约束。在 GRPO 变体中，GRPO-GenRM 由于其奖励信号缺乏硬约束，在安全维度上表现出不稳定。 GRPO-Linear 采用加权求和聚合，会受到跷跷板效应的影响，即行为分数的提高是以底线指标下降为代价的。

### 段落 68 · Page 7

**EN**

In contrast, our Gated Aggregation Strategy ensures that the model optimizes behavioral utility only within the safe region, resulting in simultaneous improvements across both safety and utility dimensions. 4.3.2 Human Expert Evaluation.To corroborate the automatic metrics, we conducted a blind side-by-side human evaluation. We sampled 1,000 distinct queries from the test set and engaged a large pool of expert annotators to compare the responses generated by our method against representative baselines. The experts judged the responses based on critical criteria such as factual consistency, safety, richness, conciseness, and logic.

**中文**

相比之下，我们的门控聚合策略确保模型仅在安全区域内优化行为效用，从而在安全性和效用维度上同时改进。 4.3.2 人类专家评估。为了证实自动指标，我们进行了盲人并行评估。我们从测试集中抽取了 1,000 个不同的查询，并聘请了大量专家注释者将我们的方法生成的响应与代表性基线进行比较。专家们根据事实一致性、安全性、丰富性、简洁性和逻辑性等关键标准来评判答案。

### 段落 69 · Page 7

**EN**

The evaluation results (Figure 3) align consistently with the automatic metrics, showing that our model achieves a significantly higher win rate. Experts observed that our method produces answers that are not only robust to noisy retrieval and semantically rich but also strictly compliant with formatting and safety guidelines. This confirms that the gains observed in the reward scores genuinely reflect improvements in generation quality perceptible to human users.

**中文**

评估结果（图 3）与自动指标一致，表明我们的模型实现了显着更高的胜率。专家观察到，我们的方法产生的答案不仅对噪声检索具有鲁棒性且语义丰富，而且严格符合格式和安全准则。这证实了奖励分数中观察到的收益确实反映了人类用户可感知的生成质量的改进。

### 段落 70 · Page 7

**EN**

4.4 Training Dynamics (RQ3) We analyze the evolution of different reward dimensions during training, as illustrated in Figure 4, to understand how the Gated Aggregation Strategy resolves the inherent antagonism between conflicting objectives. In the early stages of training, we observe a natural seesaw effect in the baseline methods, particularly between Richness and Conciseness; as the model strives to cover more information, it inevitably tends towards verbosity, causing conciseness scores to drop.

**中文**

4.4 训练动态（RQ3） 我们分析训练过程中不同奖励维度的演变，如图 4 所示，以了解门控聚合策略如何解决冲突目标之间的固有对抗。在训练的早期阶段，我们观察到基线方法中存在自然的跷跷板效应，特别是在丰富性和简洁性之间；当模型努力涵盖更多信息时，它不可避免地会变得冗长，导致简洁性分数下降。

### 段落 71 · Page 7

**EN**

GRPO-Linear partially mitigates this issue by introducing expert priors through weighted summation, which forces the model to respect the relative importance of each dimension. However, it still treats safety constraints and behavioral objectives as parallel signals, leading to instability where the model occasionally sacrifices Bottom-line Constraints to chase marginal gains in utility. In contrast, GRPO-Gated fundamentally alters this dynamic by establishing a hierarchical dependency. The training curves show that the Gated strategy first "locks in" high scores on bottom-line constraints.

**中文**

GRPO-Linear 通过加权求和引入专家先验，部分缓解了这个问题，这迫使模型尊重每个维度的相对重要性。然而，它仍然将安全约束和行为目标视为并行信号，从而导致不稳定，模型偶尔会牺牲底线约束来追求效用的边际收益。相比之下，GRPO-Gated 通过建立层次依赖性从根本上改变了这种动态。训练曲线显示，门控策略首先“锁定”底线约束的高分。

### 段落 72 · Page 7

**EN**

Only after these safety metrics stabilize above the threshold does the model begin to effectively optimize for richness and diversity. This mechanism transforms the interdimensional conflict into a synergistic evolution, ensuring that the pursuit of user utility never compromises the foundational reliability of the generative search system. 4.5 Online Experiments (RQ4) To evaluate real-world impact and robustness, we deployed the trained model in the AI search entry of RedNote. We implemented randomized traffic diversion by hashing User IDs and modulo bucketing.

**中文**

只有在这些安全指标稳定在阈值以上之后，模型才会开始有效地优化丰富性和多样性。这种机制将维度间的冲突转化为协同进化，确保对用户效用的追求永远不会损害生成搜索系统的基础可靠性。 4.5 在线实验（RQ4） 为了评估现实世界的影响和鲁棒性，我们将训练好的模型部署在 RedNote 的 AI 搜索条目中。我们通过散列用户 ID 和取模分桶来实现随机流量分流。

### 段落 73 · Page 7

**EN**

We allocated a consistent 10% of the total live traffic to each experimental group. All variants were evaluated synchronously over the same period to eliminate temporal fluctuations, thereby ensuring the fairness and reliability of the statistical conclusions. All reported uplifts are statistically significant (two-sided tests; 𝑝< 0.05). In particular, for VCR the typical 95% confidence interval is within ±0.1percentage points, indicating that the observed gains are well above the noise level. Additionally, we explicitly excluded a small subset of vertical business domains from the training set to

**中文**

我们将总实时流量的 10% 一致分配给每个实验组。所有变异均在同一时期同步评估，消除时间波动，从而保证统计结论的公平性和可靠性。所有报告的提升均具有统计显着性（双面检验；𝑝< 0.05）。特别是，对于 VCR，典型的 95% 置信区间在 ±0.1 个百分点以内，表明观察到的增益远高于噪声水平。此外，我们明确从训练集中排除了一小部分垂直业务领域，以

### Page 8

### 段落 74 · Page 8

**EN**

KDD ’26, August 9–13, 2026, Jeju, Korea Wei Wu, Peilun Zhou, et al.

**中文**

KDD ’26，2026 年 8 月 9-13 日，韩国济州 Wei Wu、Peilun Zhou 等。

### 段落 75 · Page 8

**EN**

0.900 0.925 0.950 0.975 1.000 Query Satisfy 0.7 0.8 0.9 1.0 Reference Conflict 0.4 0.6 0.8 Reference Beneficiality 0.2 0.4 0.6 Reference Diversity 0.90 0.95 1.00 Highlight Hallucination 0.900 0.925 0.950 0.975 Claim Hallucination 0 100 200 300 400 500 600 700 800 0.90 0.95 1.00 Format 0 100 200 300 400 500 600 700 800 0.900 0.925 0.950 0.975 1.000 Claim Diversity 0 100 200 300 400 500 600 700 800 0.5 0.6 0.7 0.8 0.9 Answer Firstness Training Step Reward Score GRPO-Gated GRPO-Linear (Weighted Sum) GRPO-Linear (Sum) Figure 4: Training dynamics under different reward aggregation strategies.

**中文**

0.900 0.925 0.950 0.975 1.000 查询满足 0.7 0.8 0.9 1.0 参考冲突 0.4 0.6 0.8 参考益处 0.2 0.4 0.6 参考多样性 0.90 0.95 1.00 突出幻觉 0.900 0.925 0.950 0.975 声称幻觉 0 100 200 300 400 500 600 700 800 0.90 0.95 1.00 格式 0 100 200 300 400 500 600 700 800 0.900 0.925 0.950 0.975 1.000 索赔多样性 0 100 200 300 400 500 600 700 800 0.5 0.6 0.7 0.8 0.9 答案优先 训练步骤奖励得分 GRPO 门控 GRPO-线性（加权总和） GRPO-线性（总和） 图 4：训练动态在不同的奖励聚合策略下。

### 段落 76 · Page 8

**EN**

The curves illustrate the evolution of scores across distinct reward dimensions during training, comparing the Gated Aggregation strategy against the Linear baseline. 01-1601-1701-1801-1901-2001-2101-22 -1.0% 0.0% 1.0% Valid Consumption Rate (VCR) ↑ 01-1601-1701-1801-1901-2001-2101-22 -0.5% 0.0% 0.5% Skip Rate (SR) ↓ 01-1601-1701-1801-1901-2001-2101-22 -5.0% 0.0% 5.0% Re-search Rate (RR) ↓ 01-1601-1701-1801-1901-2001-2101-22 -2.5% 0.0% 2.5% Bad Case Rate (BCR) ↓ Δ vs SFT (%) In-distribution Domains Out-of-distribution Domains Figure 5: Results of the online A/B test on the RedNote platform conducted in 2026.

**中文**

这些曲线说明了训练期间不同奖励维度的分数演变，将门控聚合策略与线性基线进行了比较。 01-1601-1701-1801-1901-2001-2101-22 -1.0% 0.0% 1.0% 有效消耗率 (VCR) ↑ 01-1601-1701-1801-1901-2001-2101-22 -0.5% 0.0% 0.5% 跳过率(SR) ↓ 01-1601-1701-1801-1901-2001-2101-22 -5.0% 0.0% 5.0% 研究率 (RR) ↓ 01-1601-1701-1801-1901-2001-2101-22 -2.5% 0.0% 2.5% 不良案例比率 (BCR) ↓ Δ vs SFT (%) 分布内域 分布外域 图 5：2026 年在 RedNote 平台上进行的在线 A/B 测试结果。

### 段落 77 · Page 8

**EN**

The chart displays the relative changes in key user engagement metrics for our deployed model compared to the production baseline (SFT). assess the generalization capability of the model across unseen distributions. The online A/B testing results, summarized in Figure 5, demonstrate substantial improvements across all core engagement metrics. Compared to the baseline, our model achieves a significant increase in Valid Consumption Rate (VCR) which indicates that users find the synthesized answers helpful and are willing to spend time reading them. Simultaneously, we observe a marked reduction in Skip Rate (SR) and Re-search Rate (RR).

**中文**

该图表显示了我们部署的模型的关键用户参与度指标与生产基线 (SFT) 相比的相对变化。评估模型在未见分布中的泛化能力。图 5 中总结的在线 A/B 测试结果表明，所有核心参与度指标均取得了显着改进。与基线相比，我们的模型有效消费率（VCR）显着增加，这表明用户发现合成的答案很有帮助，并且愿意花时间阅读它们。同时，我们观察到跳过率 (SR) 和研究率 (RR) 显着下降。

### 段落 78 · Page 8

**EN**

These shifts suggest that the generated responses satisfy user needs in a single turn and reduce the necessity for query reformulation. Crucially, the Bad Case Rate (BCR) remains at a minimal level which ensures the safety and reliability of the deployed system. Furthermore, the performance on the held-out domains confirms the robust generalization of our method. Although different business verticals exhibit distinct data biases regarding content format or information density, our model adapts effectively without explicit fine-tuning. It maintains high safety standards and response quality even in these zero-shot scenarios.

**中文**

这些转变表明生成的响应可以一次性满足用户需求，并减少重新制定查询的必要性。至关重要的是，坏案例率 (BCR) 保持在最低水平，确保了已部署系统的安全性和可靠性。此外，保留域上的性能证实了我们方法的稳健泛化。尽管不同的业务垂直领域在内容格式或信息密度方面表现出不同的数据偏差，但我们的模型无需明确的微调即可有效适应。即使在这些零样本场景中，它也能保持高安全标准和响应质量。

### 段落 79 · Page 8

**EN**

This stability validates that our multi-dimensional reward system captures fundamental search principles rather than overfitting to specific training data patterns. 5 Conclusion In this work, we introduced SearchLLM, an LLM optimized for open-ended generative search on large content platforms. We characterized the unique challenges of this setting, including robustness to noisy retrieval, safety guarantees, and alignment with diverse user needs.

**中文**

这种稳定性验证了我们的多维奖励系统捕获了基本搜索原则，而不是过度拟合特定的训练数据模式。 5 结论 在这项工作中，我们介绍了SearchLLM，这是一种针对大型内容平台上的开放式生成搜索进行优化的LLM。我们描述了这种设置的独特挑战，包括对噪声检索的鲁棒性、安全保证以及与不同用户需求的一致性。

### 段落 80 · Page 8

**EN**

To solve these, we designed a multi-dimensional reward system that separates bottom-line constraints, such as factual grounding and format compliance, from behavioral objectives that drive user utility. Our approach uses the Gated Aggregation Strategy to decouple safety constraints from behavioral objectives, enabling effective policy optimization through Group Relative Policy Optimization (GRPO). The deployment of SearchLLM in RedNote, with over 150 million daily page views, was validated through online A/B tests. These tests showed improvements in generation quality and user engagement while maintaining safety standards.

**中文**

为了解决这些问题，我们设计了一个多维奖励系统，将事实基础和格式合规性等底线约束与驱动用户效用的行为目标分开。我们的方法使用门控聚合策略将安全约束与行为目标分离，从而通过组相对策略优化（GRPO）实现有效的策略优化。 SearchLLM 在 RedNote 中的部署通过在线 A/B 测试得到了验证，每日页面浏览量超过 1.5 亿次。这些测试表明，在保持安全标准的同时，发电质量和用户参与度有所提高。

### 段落 81 · Page 8

**EN**

Our approach offers a scalable solution to align open-ended generative search systems with real-world constraints. Future work will extend this optimization to multi-modal contexts and incorporate personalized long-term memory to further refine the user experience.

**中文**

我们的方法提供了一个可扩展的解决方案，使开放式生成搜索系统与现实世界的约束保持一致。未来的工作将把这种优化扩展到多模式环境，并结合个性化的长期记忆来进一步完善用户体验。

### Page 9

### 段落 82 · Page 9

**EN**

Aligning Large Language Models with Searcher Preferences KDD ’26, August 9–13, 2026, Jeju, Korea References [1] Zheng Cai, Maosong Cao, Haojiong Chen, Kai Chen, Keyu Chen, Xin Chen, Xun Chen, Zehui Chen, Zhi Chen, Pei Chu, Xiaoyi Dong, Haodong Duan, Qi Fan, Zhaoye Fei, Yang Gao, Jiaye Ge, Chenya Gu, Yuzhe Gu, Tao Gui, Aijia Guo, Qipeng Guo, Conghui He, Yingfan Hu, Ting Huang, Tao Jiang, Penglong Jiao, Zhenjiang Jin, Zhikai Lei, Jiaxing Li, Jingwen Li, Linyang Li, Shuaibin Li, Wei Li, Yining Li, Hongwei Liu, Jiangning Liu, Jiawei Hong, Kaiwen Liu, Kuikun Liu, Xiaoran Liu, Chengqi Lv, Haijun Lv, Kai Lv, Li Ma, Runyuan Ma, Zerun Ma, Wenchang Nin

**中文**

Aligning Large Language Models with Searcher Preferences KDD’26，2026 年 8 月 9-13 日，韩国济州 参考文献 [1] Cheng Cai, Maosong Cao, Haojiong Chen, Kai Chen, Keyu Chen, Xin Chen, Xun Chen, Zehui Chen,zhi Chen, Pei Chu, Xiaoyi Dong,haodong Duan, Qi Fan, Chaoye Fei, Yang Gau, Jiaye Ge, Chenya Gu, Yuzhe Gu, Tai Gui,郭爱嘉、郭启鹏、何从辉、胡英凡、黄婷、蒋涛、焦鹏龙、金镇江、雷志凯、李嘉兴、李静文、李林洋、李帅斌、李伟、李一宁、刘宏伟、江宁、洪嘉伟、刘凯文、刘奎坤、刘晓然、吕成启、吕海军、吕凯、马丽、马润源、马泽润、文昌宁

### 段落 83 · Page 9

**EN**

g, Linke Ouyang, Jiantao Qiu, Yuan Qu, Fukai Shang, Yunfan Shao, Demin Song, Zifan Song, Zhihao Sui, Peng Sun, Yu Sun, Huanze Tang, Bin Wang, Guoteng Wang, Jiaqi Wang, Jiayu Wang, Rui Wang, Yudong Wang, Ziyi Wang, Xingjian Wei, Qizhen Weng, Fan Wu, Yingtong Xiong, Chao Xu, Ruiliang Xu, Hang Yan, Yirong Yan, Xiaogui Yang, Haochen Ye, Huaiyuan Ying, Jia Yu, Jing Yu, Yuhang Zang, Chuyu Zhang, Li Zhang, Pan Zhang, Peng Zhang, Ruijie Zhang, Shuo Zhang, Songyang Zhang, Wenjian Zhang, Wenwei Zhang, Xingcheng Zhang, Xinyue Zhang, Hui Zhao, Qian Zhao, Xiaomeng Zhao, Fengzhe Zhou, Zaida Zhou, Jingming Zhuo, Yicheng Zou, Xipeng Qiu, Yu Qiao, and Dahua L

**中文**

g、林科欧阳、邱建涛、袁曲、尚富凯、邵云帆、宋德民、宋子凡、隋志豪、孙鹏、孙宇、唐焕泽、王斌、王国腾、王嘉琪、王嘉宇、王锐、王玉栋、王子怡、魏兴建、翁启珍、吴凡、熊英桐、徐超、徐瑞亮、颜航、颜一荣、杨小贵、叶浩辰、应怀远、贾宇、靖宇、臧宇航、张楚宇、张莉、张潘、张鹏、张瑞杰、张硕、张松阳、张文建、张文伟、张兴成、张新月、赵辉、赵倩、赵小萌、周丰哲、周在大、卓景明、邹一成、邱西鹏、乔宇和L大华

### 段落 84 · Page 9

in.

### 段落 85 · Page 9

**EN**

2024. InternLM2 Technical Report. arXiv:2403.17297 [cs.CL] https://arxiv.org/abs/2403.17297 [2] ChatGPT. 2026.ChatGPT. https://chatgpt.com/ [3] Ben Chen, Xian Guo, Siyuan Wang, Zihan Liang, Yue Lv, Yufei Ma, Xinlong Xiao, Bowen Xue, Xuxin Zhang, Ying Yang, Huangyu Dai, Xing Xu, Tong Zhao, Mingcan Peng, Xiaoyang Zheng, Chao Wang, Qihang Zhao, Zhixin Zhai, Yang Zhao, Bochao Liu, Jingshan Lv, Xiao Liang, Yuqing Ding, Jing Chen, Chenyi Lei, Wenwu Ou, Han Li, and Kun Gai. 2025. OneSearch: A Preliminary Exploration of the Unified End-to-End Generative Framework for E-commerce Search.

**中文**

2024.InternLM2 技术报告。 arXiv:2403.17297 [cs.CL] https://arxiv.org/abs/2403.17297 [2] ChatGPT。 2026.ChatGPT。 https://chatgpt.com/ [3] 陈本、郭贤、王思源、梁子涵、吕悦、马宇飞、肖新龙、薛博文、张旭鑫、杨英、戴黄宇、徐星、赵同、彭明灿、郑晓阳、王超、赵启航、翟志新、赵阳、刘博超、吕景山、梁晓、丁雨清、陈景、雷晨怡、欧文武、韩李，昆盖。 2025.OneSearch：电子商务搜索统一端到端生成框架的初步探索。

### 段落 86 · Page 9

**EN**

arXiv:2509.03236 [cs.IR] https://arxiv.org/abs/2509.03236 [4] Jianlyu Chen, Shitao Xiao, Peitian Zhang, Kun Luo, Defu Lian, and Zheng Liu. 2024. M3-Embedding: Multi-Linguality, Multi-Functionality, Multi-Granularity Text Embeddings Through Self-Knowledge Distillation. InFindings of the Association for Computational Linguistics: ACL 2024, Lun-Wei Ku, Andre Martins, and Vivek Srikumar (Eds.). Association for Computational Linguistics, Bangkok, Thailand, 2318–2335. doi:10.18653/v1/2024.findings-acl.137 [5] Douyin. [n. d.].Douyin AI Search. https://search.douyin.com/ [6] Martin J. Eppler and Jeanne Mengis. 2004.

**中文**

arXiv:2509.03236 [cs.IR] https://arxiv.org/abs/2509.03236 [4] 陈建吕、肖世涛、张培田、罗昆、连德福和刘正。 2024. M3-Embedding：通过自我知识蒸馏实现多语言、多功能、多粒度文本嵌入。计算语言学协会的调查结果：ACL 2024，Lun-Wei Ku、Andre Martins 和 Vivek Srikumar（编辑）。计算语言学协会，泰国曼谷，2318-2335。 doi:10.18653/v1/2024.findings-acl.137 [5] 抖音。 [n. d.].抖音AI搜索。 https://search.douyin.com/ [6] 马丁·J·埃普勒和珍妮·蒙吉斯。 2004年。

### 段落 87 · Page 9

**EN**

The Concept of Information Overload: A Review of Literature from Organization Science, Accounting, Marketing, MIS, and Related Disciplines.The Information Society20 (2004), 325 – 344. https: //api.semanticscholar.org/CorpusID:262540775 [7] Yunfan Gao, Yun Xiong, Xinyu Gao, Kangxiang Jia, Jinliu Pan, Yuxi Bi, Yi Dai, Jiawei Sun, Qianyu Guo, Meng Wang, and Haofen Wang. 2023. Retrieval-Augmented Generation for Large Language Models: A Survey.ArXiv abs/2312.10997 (2023). https://api.semanticscholar.org/CorpusID:266359151 [8] Gemini. 2026.Gemini. https://gemini.google.com/ [9] Melody Y.

**中文**

信息过载的概念：组织科学、会计、营销、管理信息系统及相关学科文献综述。信息社会20 (2004), 325 – 344. https://api.semanticscholar.org/CorpusID:262540775 [7] Yunfan Gau, Yun Xiong, Xinyu Gau, Kangxiang Jia, Jinliu Pan, Yuxi Bi, Yi Dai, Jiawei Sun, Qiyuyuuo,王猛、王浩芬. 2023.大型语言模型的检索增强生成：调查.ArXiv abs/2312.10997 (2023)。 https://api.semanticscholar.org/CorpusID:266359151 [8] 双子座。 2026.双子座。 https://gemini.google.com/ [9] Melody Y.

### 段落 88 · Page 9

**EN**

Guan, Manas Joglekar, Eric Wallace, Saachi Jain, Boaz Barak, Alec Helyar, Rachel Dias, Andrea Vallone, Hongyu Ren, Jason Wei, Hyung Won Chung, Sam Toyer, Johannes Heidecke, Alex Beutel, and Amelia Glaese. 2025. Deliberative Alignment: Reasoning Enables Safer Language Models. arXiv:2412.16339 [cs.CL] https://arxiv.org/abs/2412.16339 [10] Anisha Gunjal, Anthony Wang, Elaine Lau, Vaskar Nath, Yunzhong He, Bing Liu, and Sean Hendryx. 2025. Rubrics as Rewards: Reinforcement Learning Beyond Verifiable Domains.

**中文**

关、Manas Joglekar、Eric Wallace、Saachi Jain、Boaz Barak、Alec Helyar、Rachel Dias、Andrea Vallone、任宏宇、Jason Wei、Hyung Won Chung、Sam Toyer、Johannes Heidecke、Alex Beutel 和 Amelia Glaese。 2025. 深思熟虑的一致性：推理使语言模型更安全。 arXiv:2412.16339 [cs.CL] https://arxiv.org/abs/2412.16339 [10] Anisha Gunjal、Anthony Wang、Elaine Lau、Vaskar Nath、Yunzhong He、Bing Liu 和 Sean Hendryx。 2025. 作为奖励的评分标准：超越可验证领域的强化学习。

### 段落 89 · Page 9

**EN**

arXiv:2507.17746 [cs.LG] https://arxiv.org/abs/2507.17746 [11] Daya Guo, Dejian Yang, Haowei Zhang, Junxiao Song, Peiyi Wang, Qihao Zhu, Runxin Xu, Ruoyu Zhang, Shirong Ma, Xiao Bi, Xiaokang Zhang, Xingkai Yu, Yu Wu, Z. F. Wu, Zhibin Gou, Zhihong Shao, Zhuoshu Li, Ziyi Gao, Aixin Liu, Bing Xue, Bingxuan Wang, Bochao Wu, Bei Feng, Chengda Lu, Chenggang Zhao, Chengqi Deng, Chong Ruan, Damai Dai, Deli Chen, Dongjie Ji, Erhang Li, Fangyun Lin, Fucong Dai, Fuli Luo, Guangbo Hao, Guanting Chen, Guowei Li, H.

**中文**

arXiv:2507.17746 [cs.LG] https://arxiv.org/abs/2507.17746 [11] 郭大亚、杨德建、张浩伟、宋俊晓、王培毅、朱启浩、徐润鑫、张若宇、马世荣、肖毕、张晓康、于兴凯、吴宇、吴正峰、苟志斌、邵志宏、李卓书、高子怡、刘爱新、薛冰、王冰轩、吴博超、冯北、陆成达、赵成刚、邓成奇、阮冲、戴大麦、陈德利、季东杰、李二航、林芳云、戴福聪、罗富丽、郝广博、陈冠廷、李国伟、H.

### 段落 90 · Page 9

**EN**

Zhang, Hanwei Xu, Honghui Ding, Huazuo Gao, Hui Qu, Hui Li, Jianzhong Guo, Jiashi Li, Jingchang Chen, Jingyang Yuan, Jinhao Tu, Junjie Qiu, Junlong Li, J. L. Cai, Jiaqi Ni, Jian Liang, Jin Chen, Kai Dong, Kai Hu, Kaichao You, Kaige Gao, Kang Guan, Kexin Huang, Kuai Yu, Lean Wang, Lecong Zhang, Liang Zhao, Litong Wang, Liyue Zhang, Lei Xu, Leyi Xia, Mingchuan Zhang, Minghua Zhang, Minghui Tang, Mingxu Zhou, Meng Li, Miaojun Wang, Mingming Li, Ning Tian, Panpan Huang, Peng Zhang, Qiancheng Wang, Qinyu Chen, Qiushi Du, Ruiqi Ge, Ruisong Zhang, Ruizhe Pan, Runji Wang, R. J. Chen, R. L.

**中文**

张汉伟、丁洪辉、高华作、曲慧、李慧、郭建中、李嘉实、陈景昌、袁景阳、屠金浩、邱俊杰、李俊龙、蔡佳琪、倪佳琪、梁健、陈金、董凯、胡凯、尤凯超、高凯歌、关康、黄可欣、于快、王Lean、张乐从、赵亮、王立同、张丽月、雷徐、乐一夏、张明川、张明华、唐明辉、周明旭、李萌、王妙君、李明明、田宁、黄盼盼、张鹏、王千成、陈钦宇、杜秋实、葛瑞琪、张瑞松、潘瑞哲、王润吉、陈瑞杰、陈瑞吉

### 段落 91 · Page 9

**EN**

Jin, Ruyi Chen, Shanghao Lu, Shangyan Zhou, Shanhuang Chen, Shengfeng Ye, Shiyu Wang, Shuiping Yu, Shunfeng Zhou, Shuting Pan, S. S. Li, Shuang Zhou, Shaoqing Wu, Tao Yun, Tian Pei, Tianyu Sun, T. Wang, Wangding Zeng, Wen Liu, Wenfeng Liang, Wenjun Gao, Wenqin Yu, Wentao Zhang, W. L. Xiao, Wei An, Xiaodong Liu, Xiaohan Wang, Xiaokang Chen, Xiaotao Nie, Xin Cheng, Xin Liu, Xin Xie, Xingchao Liu, Xinyu Yang, Xinyuan Li, Xuecheng Su, Xuheng Lin, X. Q. Li, Xiangyue Jin, Xiaojin Shen, Xiaosha Chen, Xiaowen Sun, Xiaoxiang Wang, Xinnan Song, Xinyi Zhou, Xianzu Wang, Xinxia Shan, Y. K. Li, Y. Q. Wang, Y. X.

**中文**

金如意、陆尚浩、周尚彦、陈善皇、叶胜峰、王世宇、余水平、周顺峰、潘淑婷、李三生、周双、吴少清、云涛、裴天、孙天宇、王天宇、曾旺丁、刘文、梁文峰、高文君、于文钦、张文涛、肖文龙、安伟、刘晓东、王晓涵、小康陈，聂晓涛，程鑫，刘鑫，谢鑫，刘星超，杨鑫宇，李鑫源，苏学成，林旭恒，李XQ，金翔跃，沉晓金，陈晓莎，孙晓文，王晓翔，宋鑫楠，周鑫艺，王显祖，单鑫霞，李玉坤，王YQ，Y. X.

### 段落 92 · Page 9

**EN**

Wei, Yang Zhang, Yanhong Xu, Yao Li, Yao Zhao, Yaofeng Sun, Yaohui Wang, Yi Yu, Yichao Zhang, Yifan Shi, Yiliang Xiong, Ying He, Yishi Piao, Yisong Wang, Yixuan Tan, Yiyang Ma, Yiyuan Liu, Yongqiang Guo, Yuan Ou, Yuduan Wang, Yue Gong, Yuheng Zou, Yujia He, Yunfan Xiong, Yuxiang Luo, Yuxiang You, Yuxuan Liu, Yuyang Zhou, Y. X. Zhu, Yanping Huang, Yaohui Li, Yi Zheng, Yuchen Zhu, Yunxian Ma, Ying Tang, Yukun Zha, Yuting Yan, Z. Z.

**中文**

魏、杨张、徐彦宏、李耀、赵耀、孙耀峰、王耀辉、余一、张一超、施一帆、熊一良、何英、朴一石、王一松、谭一轩、马一阳、刘一源、郭永强、欧媛、王玉端、龚悦、邹宇恒、何宇佳、熊云帆、罗宇翔、游宇翔、刘宇轩、周宇扬、朱玉霞，黄艳萍，李耀辉，郑毅，朱雨辰，马云贤，唐英，查玉坤，严雨婷，Z. Z.

### 段落 93 · Page 9

**EN**

Ren, Zehui Ren, Zhangli Sha, Zhe Fu, Zhean Xu, Zhenda Xie, Zhengyan Zhang, Zhewen Hao, Zhicheng Ma, Zhigang Yan, Zhiyu Wu, Zihui Gu, Zijia Zhu, Zijun Liu, Zilin Li, Ziwei Xie, Ziyang Song, Zizheng Pan, Zhen Huang, Zhipeng Xu, Zhongyu Zhang, and Zhen Zhang. 2025. DeepSeek-R1 incentivizes reasoning in LLMs through reinforcement learning.Nature645, 8081 (Sept. 2025), 633–638. doi:10.1038/s41586-025-09422-z [12] Yun He, Wenzhe Li, Hejia Zhang, Songlin Li, Karishma Mandyam, Sopan Khosla, Yuanhao Xiong, Nanshu Wang, Xiaoliang Peng, Beibin Li, Shengjie Bi, Shishir G.

**中文**

任泽辉、沙张丽、付哲、徐哲安、谢振达、张正彦、郝哲文、马志成、严志刚、吴志宇、谷子辉、朱子佳、刘子君、李子林、谢子伟、宋子扬、潘子正、黄振、徐志鹏、张忠宇和张振。 2025. DeepSeek-R1 通过强化学习激励法学硕士的推理。 Nature645, 8081 (2025 年 9 月), 633–638。 doi:10.1038/s41586-025-09422-z [12] 何云、李文哲、张贺佳、李松林、Karishma Mandyam、Sopan Khosla、熊元浩、王楠树、彭晓亮、李北斌、毕胜杰、Shishir G.

### 段落 94 · Page 9

**EN**

Patil, Qi Qi, Shengyu Feng, Julian Katz-Samuels, Richard Yuanzhe Pang, Sujan Gonugondla, Hunter Lang, Yue Yu, Yundi Qian, Maryam Fazel-Zarandi, Licheng Yu, Amine Benhalloum, Hany Awadalla, and Manaal Faruqui. 2025. AdvancedIF: Rubric-Based Benchmarking and Reinforcement Learning for Advancing LLM Instruction Following. arXiv:2511.10507 [cs.CL] https://arxiv.org/abs/2511.10507 [13] Woosuk Kwon, Zhuohan Li, Siyuan Zhuang, Ying Sheng, Lianmin Zheng, Cody Hao Yu, Joseph Gonzalez, Hao Zhang, and Ion Stoica. 2023. Efficient Memory Management for Large Language Model Serving with PagedAttention.

**中文**

Patil、Qi Qi、冯胜宇、Julian Katz-Samuels、Richard Yuanzhe Pang、Sujan Gonugondla、Hunter Lang、余悦、钱云迪、Maryam Fazel-Zarandi、Li Cheng Yu、Amine Benhalloum、Hany Awadalla 和 Manaal Faruqui。 2025.AdvancedIF：基于Rubric的基准测试和强化学习，以促进LLM指令的遵循。 arXiv:2511.10507 [cs.CL] https://arxiv.org/abs/2511.10507 [13] Woosuk Kwon、Zhuohan Li、Siyuan Zhuang、Ying Shen、Lianmin Cheng、Codyhao Yu、Joseph Gonzalez、Hao Zhu 和 Ion Stoica。 2023.使用 PagedAttention 进行大型语言模型的高效内存管理。

### 段落 95 · Page 9

**EN**

InProceedings of the 29th Symposium on Operating Systems Principles(Koblenz, Germany)(SOSP ’23). Association for Computing Machinery, New York, NY, USA, 611–626. doi:10.1145/3600006.3613165 [14] Harrison Lee, Samrat Phatale, Hassan Mansoor, Thomas Mesnard, Johan Ferret, Kellie Ren Lu, Colton Bishop, Ethan Hall, Victor Carbune, Abhinav Rastogi, and Sushant Prakash. 2024. RLAIF vs. RLHF: Scaling Reinforcement Learning from Human Feedback with AI Feedback. InProceedings of the 41st International Conference on Machine Learning (Proceedings of Machine Learning Research, Vol.

**中文**

第 29 届操作系统原理研讨会论文集（德国科布伦茨）(SOSP ’23)。计算机协会，美国纽约州纽约市，611–626。 doi:10.1145/3600006.3613165 [14] Harrison Lee、Samrat Phatale、Hassan Mansoor、Thomas Mesnard、Johan Ferret、Kellie Ren Lu、Colton Bishop、Ethan Hall、Victor Carbune、Abhinav Rastogi 和 Sushant Prakash。 2024. RLAIF 与 RLHF：通过人工智能反馈扩展人类反馈的强化学习。第 41 届国际机器学习会议论文集（机器学习研究论文集，卷 1）

### 段落 96 · Page 9

**EN**

235), Ruslan Salakhutdinov, Zico Kolter, Katherine Heller, Adrian Weller, Nuria Oliver, Jonathan Scarlett, and Felix Berkenkamp (Eds.). PMLR, 26874–26901. https://proceedings.mlr.press/v235/lee24t.html [15] Derek Li, Jiaming Zhou, Leo Maxime Brunswic, Abbas Ghaddar, Qianyi Sun, Liheng Ma, Yu Luo, Dong Li, Mark Coates, Jianye Hao, and Yingxue Zhang. 2025. Omni-Thinker: Scaling Multi-Task RL in LLMs with Hybrid Reward and Task Scheduling. arXiv:2507.14783 [cs.LG] https://arxiv.org/abs/2507.14783 [16] Zhiding Liu, Ben Chen, Mingyue Cheng, Enhong Chen, Li Li, Chenyi Lei, Wenwu Ou, Han Li, and Kun Gai. 2025.

**中文**

235），Ruslan Salakhutdinov、Zico Kolter、Katherine Heller、Adrian Weller、Nuria Oliver、Jonathan Scarlett 和 Felix Berkenkamp（编辑）。 PMLR，26874–26901。 https://proceedings.mlr.press/v235/lee24t.html [15] Derek Li、Jiaming Zhou、Leo Maxime Brunswic、Abbas Ghaddar、Qianyi Sun、Liheng Ma、Yu Luo、Dong Li、Mark Coates、Jianye Ha 和 Yingxue Zhang。 2025. Omni-Thinker：通过混合奖励和任务调度扩展法学硕士中的多任务强化学习。 arXiv:2507.14783 [cs.LG] https://arxiv.org/abs/2507.14783 [16] 刘志定、陈本、程明月、陈恩宏、李莉、雷陈一、欧文武、李韩和盖坤。 2025 年。

### 段落 97 · Page 9

**EN**

Towards Context-aware Reasoning-enhanced Generative Searching in E-commerce. arXiv:2510.16925 [cs.IR] https://arxiv.org/ abs/2510.16925 [17] Ilya Loshchilov and Frank Hutter. 2019. Decoupled Weight Decay Regularization. InInternational Conference on Learning Representations. https://openreview.net/ forum?id=Bkg6RiCqY7 [18] Dakota Mahan, Duy Van Phung, Rafael Rafailov, Chase Blagden, Nathan Lile, Louis Castricato, Jan-Philipp Fränken, Chelsea Finn, and Alon Albalak. 2024. Generative Reward Models. arXiv:2410.12832 [cs.LG] https://arxiv.org/abs/2410.

**中文**

走向电子商务中的上下文感知推理增强生成搜索。 arXiv:2510.16925 [cs.IR] https://arxiv.org/abs/2510.16925 [17] Ilya Loshchilov 和 Frank Hutter。 2019.解耦权重衰减正则化。在国际学习代表会议上。 https://openreview.net/forum?id=Bkg6RiCqY7 [18] Dakota Mahan、Duy Van Phung、Rafael Rafailov、Chase Blagden、Nathan Lile、Louis Castricato、Jan-Philipp Fränken、Chelsea Finn 和 Alon Albalak。 2024.生成奖励模型。 arXiv:2410.12832 [cs.LG] https://arxiv.org/abs/2410。

### 段落 98 · Page 9

**EN**

12832 [19] Deepak Narayanan, Mohammad Shoeybi, Jared Casper, Patrick LeGresley, Mostofa Patwary, Vijay Korthikanti, Dmitri Vainbrand, Prethvi Kashinkunti, Julie Bernauer, Bryan Catanzaro, Amar Phanishayee, and Matei Zaharia. 2021. Efficient large-scale language model training on GPU clusters using megatron- LM. InProceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis(St. Louis, Missouri)(SC ’21). Association for Computing Machinery, New York, NY, USA, Article 58, 15 pages. doi:10.1145/3458817.3476209 [20] Rodrigo Nogueira and Kyunghyun Cho. 2020. Passage Re-ranking with BERT.

**中文**

12832 [19] Deepak Narayanan、Mohammad Shoeybi、Jared Casper、Patrick LeGresley、Mostofa Patwary、Vijay Korthikanti、Dmitri Vainbrand、Prethvi Kashinkunti、Julie Bernauer、Bryan Catanzaro、Amar Phanishaye 和 Matei Zaharia。 2021. 使用 megatron-LM 在 GPU 集群上进行高效的大规模语言模型训练。高性能计算、网络、存储和分析国际会议（密苏里州圣路易斯）(SC ’21) 论文集。计算机协会，美国纽约州纽约市，第 58 条，15 页。 doi:10.1145/3458817.3476209 [20] 罗德里戈·诺盖拉和曹京贤。 2020. 使用 BERT 进行段落重排。

### 段落 99 · Page 9

**EN**

arXiv:1901.04085 [cs.IR] https://arxiv.org/abs/1901.04085 [21] Long Ouyang, Jeffrey Wu, Xu Jiang, Diogo Almeida, Carroll Wainwright, Pamela Mishkin, Chong Zhang, Sandhini Agarwal, Katarina Slama, Alex Ray, John Schulman, Jacob Hilton, Fraser Kelton, Luke Miller, Maddie Simens, Amanda Askell, Peter Welinder, Paul F Christiano, Jan Leike, and Ryan Lowe. 2022. Training language models to follow instructions with human feedback. In Advances in Neural Information Processing Systems, S. Koyejo, S. Mohamed, A. Agarwal, D. Belgrave, K. Cho, and A. Oh (Eds.), Vol. 35. Curran Associates, Inc., 27730–27744.

**中文**

arXiv:1901.04085 [cs.IR] https://arxiv.org/abs/1901.04085 [21] Long Ouyang, Jeffrey Wu, Xu Jiang, Diogo Almeida, Carroll Wainwright, Pamela Mishkin, Chong Chang, Sandhini Agarwal, Katarina Slama, Alex Ray, John Schulman, Jacob Hilton, Fraser Kelton, Luke Miller,麦迪·西蒙斯、阿曼达·阿斯克尔、彼得·韦林德、保罗·F·克里斯蒂安诺、扬·雷克和瑞安·洛。 2022. 训练语言模型以遵循人类反馈的指令。 《神经信息处理系统进展》，S. Koyejo、S. Mohamed、A. Agarwal、D. Belgrave、K. Cho 和 A. Oh（编辑），卷。 35.Curran Associates, Inc.，27730-27744。

### 段落 100 · Page 9

**EN**

https://proceedings.neurips.cc/paper_files/paper/2022/file/ b1efde53be364a73914f58805a001731-Paper-Conference.pdf [22] Ming Pang, Chunyuan Yuan, Xiaoyu He, Zheng Fang, Donghao Xie, Fanyi Qu, Xue Jiang, Changping Peng, Zhangang Lin, Ching Law, and Jingping Shao. 2025. Generative Retrieval and Alignment Model: A New Paradigm for E-commerce Retrieval. arXiv:2504.01403 [cs.IR] https://arxiv.org/abs/2504.01403 [23] Wenjun Peng, Guiyang Li, Yue Jiang, Zilong Wang, Dan Ou, Xiaoyi Zeng, Derong Xu, Tong Xu, and Enhong Chen. 2024. Large Language Model based Long-tail Query Rewriting in Taobao Search.

**中文**

https://proceedings.neurips.cc/paper_files/paper/2022/file/b1efde53be364a73914f58805a001731-Paper-Conference.pdf [22] Ming Pang、Chunyuan Yuan、Xiaoyu He、Zheng Fang、Donghao Xie、Fanyi Qu、Xue Jiang、Changping Peng、Zhangang Lin、Ching Law 和 Jingping Shao。 2025.生成检索和对齐模型：电子商务检索的新范式。 arXiv:2504.01403 [cs.IR] https://arxiv.org/abs/2504.01403 [23] 彭文军、李贵阳、江悦、王子龙、欧丹、曾小一、徐德荣、徐同和陈恩宏。 2024. 基于大语言模型的淘宝搜索长尾查询重写。

### 段落 101 · Page 9

**EN**

InCompanion Proceedings of the ACM Web Conference 2024(Singapore, Singapore)(WWW ’24). Association for Computing Machinery, New York, NY, USA, 20–28. doi:10.1145/3589335.3648298 [24] Zhen Qin, Rolf Jagerman, Kai Hui, Honglei Zhuang, Junru Wu, Le Yan, Jiaming Shen, Tianqi Liu, Jialu Liu, Donald Metzler, Xuanhui Wang, and Michael Bendersky. 2024. Large Language Models are Effective Text Rankers with Pairwise Ranking Prompting. InFindings of the Association for Computational Linguistics: NAACL 2024, Kevin Duh, Helena Gomez, and Steven Bethard (Eds.). Association for Computational Linguistics, Mexico City, Mexico, 1504–1518.

**中文**

2024 年 ACM 网络会议配套论文集（新加坡、新加坡）(WWW ’24)。计算机协会，美国纽约州纽约市，20-28。 doi:10.1145/3589335.3648298 [24] 秦臻、Rolf Jagerman、凯辉、庄红雷、吴俊如、颜乐、沉家明、刘天奇、刘嘉露、唐纳德·梅茨勒、王宣辉和迈克尔·本德斯基。 2024 年。大型语言模型是具有成对排名提示的有效文本排名器。计算语言学协会的调查结果：NAACL 2024，Kevin Duh、Helena Gomez 和 Steven Bethard（编辑）。计算语言学协会，墨西哥墨西哥城，1504-1518 年。

### 段落 102 · Page 9

doi:10.18653/v1/2024.findings-naacl.97

### Page 10

### 段落 103 · Page 10

**EN**

KDD ’26, August 9–13, 2026, Jeju, Korea Wei Wu, Peilun Zhou, et al. [25] Rafael Rafailov, Archit Sharma, Eric Mitchell, Christopher D Manning, Stefano Ermon, and Chelsea Finn. 2023. Direct Preference Optimization: Your Language Model is Secretly a Reward Model. InAdvances in Neural Information Processing Systems, A. Oh, T. Naumann, A. Globerson, K. Saenko, M. Hardt, and S. Levine (Eds.), Vol. 36. Curran Associates, Inc., 53728–53741. https://proceedings.neurips.cc/paper_files/paper/2023/file/ a85b405ed65c6477a4fe8302b5e06ce7-Paper-Conference.pdf [26] John Schulman, Filip Wolski, Prafulla Dhariwal, Alec Radford, and Oleg Klimov. 2017.

**中文**

KDD ’26，2026 年 8 月 9-13 日，韩国济州 Wei Wu、Peilun Zhou 等。 [25]拉斐尔·拉法洛夫、阿奇特·夏尔马、埃里克·米切尔、克里斯托弗·D·曼宁、斯特凡诺·埃尔蒙和切尔西·芬恩。 2023. 直接偏好优化：你的语言模型实际上是一个奖励模型。 《神经信息处理系统进展》，A. Oh、T. Naumann、A. Globerson、K. Saenko、M. Hardt 和 S. Levine（编辑），卷。 36.Curran Associates, Inc.，53728-53741。 https://proceedings.neurips.cc/paper_files/paper/2023/file/a85b405ed65c6477a4fe8302b5e06ce7-Paper-Conference.pdf [26] John Schulman、Filip Wolski、Prafulla Dhariwal、Alec Radford 和 Oleg Klimov。 2017年。

### 段落 104 · Page 10

**EN**

Proximal Policy Optimization Algorithms. arXiv:1707.06347 [cs.LG] https: //arxiv.org/abs/1707.06347 [27] Zhihong Shao, Peiyi Wang, Qihao Zhu, Runxin Xu, Junxiao Song, Xiao Bi, Haowei Zhang, Mingchuan Zhang, Y. K. Li, Y. Wu, and Daya Guo. 2024. DeepSeek- Math: Pushing the Limits of Mathematical Reasoning in Open Language Models. arXiv:2402.03300 [cs.CL] https://arxiv.org/abs/2402.03300 [28] Guangming Sheng, Chi Zhang, Zilingfeng Ye, Xibin Wu, Wang Zhang, Ru Zhang, Yanghua Peng, Haibin Lin, and Chuan Wu. 2025. HybridFlow: A Flexible and Efficient RLHF Framework.

**中文**

近端策略优化算法。 arXiv:1707.06347 [cs.LG] https: //arxiv.org/abs/1707.06347 [27] 邵志宏、王培毅、朱启豪、徐润新、宋俊晓、毕晓、张浩伟、张明川、李玉坤、吴玉和郭大亚。 2024.DeepSeek-数学：突破开放语言模型中数学推理的极限。 arXiv:2402.03300 [cs.CL] https://arxiv.org/abs/2402.03300 [28] 盛光明、张驰、叶紫岭峰、吴希斌、张王、张茹、彭阳华、林海滨和吴川。 2025.HybridFlow：灵活高效的 RLHF 框架。

### 段落 105 · Page 10

**EN**

InProceedings of the Twentieth European Conference on Computer Systems(Rotterdam, Netherlands)(EuroSys ’25). Association for Computing Machinery, New York, NY, USA, 1279–1297. doi:10.1145/3689031. 3696075 [29] Siddharth Suri, Scott Counts, Leijie Wang, Chacha Chen, Mengting Wan, Tara Safavi, Jennifer Neville, Chirag Shah, Ryen W. White, Reid Andersen, Georg Buscher, Sathish Manivannan, Nagu Rangan, and Longqi Yang. 2024. The Use of Generative Search Engines for Knowledge Work and Complex Tasks. arXiv:2404.04268 [cs.IR] https://arxiv.org/abs/2404.04268 [30] TikTok. 2026.TikTok.

**中文**

在第二十届欧洲计算机系统会议（荷兰鹿特丹）（EuroSys '25）的会议记录中。计算机协会，美国纽约州纽约市，1279–1297。 doi：10.1145/3689031。 3696075 [29] Siddharth Suri、Scott Counts、Leijie Wang、Chacha Chen、Mengting Wan、Tara Safavi、Jennifer Neville、Chirag Shah、Ryen W. White、Reid Andersen、Georg Buscher、Sathish Manivannan、Nagu Rangan 和 Longqi Yang。 2024。使用生成式搜索引擎进行知识工作和复杂任务。 arXiv:2404.04268 [cs.IR] https://arxiv.org/abs/2404.04268 [30] TikTok。 2026.TikTok。

### 段落 106 · Page 10

**EN**

https://www.tiktok.com/ [31] Luong Trung, Xinbo Zhang, Zhanming Jie, Peng Sun, Xiaoran Jin, and Hang Li. 2024. ReFT: Reasoning with Reinforced Fine-Tuning. InProceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), Lun-Wei Ku, Andre Martins, and Vivek Srikumar (Eds.). Association for Computational Linguistics, Bangkok, Thailand, 7601–7614. doi:10.18653/v1/2024. acl-long.410 [32] Vijay Viswanathan, Yanchao Sun, Shuang Ma, Xiang Kong, Meng Cao, Graham Neubig, and Tongshuang Wu. 2025. Checklists Are Better Than Reward Models For Aligning Language Models.

**中文**

https://www.tiktok.com/ [31] Luong Trung，张新波，杰占明，孙鹏，金晓然，李航。 2024. ReFT：强化微调推理。计算语言学协会第 62 届年会记录（第一卷：长论文），Lun-Wei Ku、Andre Martins 和 Vivek Srikumar（编辑）。计算语言学协会，泰国曼谷，7601–7614。 doi：10.18653/v1/2024。 acl-long.410 [32] Vijay Viswanathan、孙彦超、马爽、向孔、曹孟、Graham Neubig 和吴同爽。 2025. 对于协调语言模型来说，清单比奖励模型更好。

### 段落 107 · Page 10

**EN**

arXiv:2507.18624 [cs.CL] https://arxiv.org/abs/ 2507.18624 [33] Liang Wang, Nan Yang, and Furu Wei. 2023. Query2doc: Query Expansion with Large Language Models. InProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, Houda Bouamor, Juan Pino, and Kalika Bali (Eds.). Association for Computational Linguistics, Singapore, 9414–9423. doi:10.18653/v1/2023.emnlp-main.585 [34] WeChat. 2026.WeChat. https://www.wechat.com/ [35] Haoyi Xiong, Jiang Bian, Yuchen Li, Xuhong Li, Mengnan Du, Shuaiqiang Wang, Dawei Yin, and Sumi Helal. 2024.

**中文**

arXiv:2507.18624 [cs.CL] https://arxiv.org/abs/2507.18624 [33] 王亮、南阳和魏福如。 2023.Query2doc：使用大型语言模型进行查询扩展。 2023 年自然语言处理经验方法会议论文集，Houda Bouamor、Juan Pino 和 Kalika Bali（编辑）。计算语言学协会，新加坡，9414–9423。 doi:10.18653/v1/2023.emnlp-main.585 [34] 微信。 2026.微信。 https://www.wechat.com/ [35] 熊浩一，卞江，李雨辰，李旭红，杜梦楠，王帅强，尹大伟，Sumi Helal。 2024 年。

### 段落 108 · Page 10

**EN**

When Search Engine Services Meet Large Language Models: Visions and Challenges.IEEE Transactions on Services Computing 17, 6 (2024), 4558–4577.

**中文**

当搜索引擎服务遇到大型语言模型时：愿景和挑战。IEEE 服务计算汇刊 17, 6 (2024), 4558–4577。

### 段落 109 · Page 10

**EN**

doi:10.1109/TSC.2024.3451185 [36] An Yang, Anfeng Li, Baosong Yang, Beichen Zhang, Binyuan Hui, Bo Zheng, Bowen Yu, Chang Gao, Chengen Huang, Chenxu Lv, Chujie Zheng, Dayiheng Liu, Fan Zhou, Fei Huang, Feng Hu, Hao Ge, Haoran Wei, Huan Lin, Jialong Tang, Jian Yang, Jianhong Tu, Jianwei Zhang, Jianxin Yang, Jiaxi Yang, Jing Zhou, Jingren Zhou, Junyang Lin, Kai Dang, Keqin Bao, Kexin Yang, Le Yu, Lianghao Deng, Mei Li, Mingfeng Xue, Mingze Li, Pei Zhang, Peng Wang, Qin Zhu, Rui Men, Ruize Gao, Shixuan Liu, Shuang Luo, Tianhao Li, Tianyi Tang, Wenbiao Yin, Xingzhang Ren, Xinyu Wang, Xinyu Zhang, Xuancheng Ren, Yang Fan, Yang Su, Yichang Zhang, Yinger Zhang, Yu Wan, Yuqiong Liu, Zekun Wang, Zeyu Cui, Zhenru Zhang, Zhipeng Zhou, and Zihan Qiu.

**中文**

doi:10.1109/TSC.2024.3451185 [36] 安阳、李安峰、杨宝松、张北辰、惠斌源、郑波、余博文、高昌、黄承恩、吕晨旭、郑楚杰、刘大一恒、周范、黄飞、胡峰、葛浩然、魏浩然、林欢、唐家龙、杨建、屠建宏、张建伟、杨建新、杨家喜、周静、周静仁、林俊阳、党凯、鲍克勤、杨可欣、余乐、邓良豪、李梅、薛明峰、李明泽、张培、王鹏、朱勤、门睿、高瑞泽、刘世轩、罗双、李天浩、唐天一、尹文标、任兴章、王新宇、张新宇、任宣成、杨帆、苏杨、宜昌张、张英儿、万宇、刘玉琼、王泽坤、崔泽宇、张振如、周志鹏和邱子涵。

### 段落 110 · Page 10

**EN**

2025. Qwen3 Technical Report. arXiv:2505.09388 [cs.CL] https://arxiv.org/abs/2505.09388 [37] Zheng Yuan, Hongyi Yuan, Chengpeng Li, Guanting Dong, Keming Lu, Chuanqi Tan, Chang Zhou, and Jingren Zhou. 2023. Scaling Relationship on Learning Mathematical Reasoning with Large Language Models. arXiv:2308.01825 [cs.CL] https://arxiv.org/abs/2308.01825 [38] Hansi Zeng, Chen Luo, Bowen Jin, Sheikh Muhammad Sarwar, Tianxin Wei, and Hamed Zamani. 2024. Scalable and Effective Generative Information Retrieval. InProceedings of the ACM Web Conference 2024(Singapore, Singapore)(WWW ’24). Association for Computing Machinery, New York, NY, USA, 1441–1452.

**中文**

2025.Qwen3 技术报告。 arXiv:2505.09388 [cs.CL] https://arxiv.org/abs/2505.09388 [37] 郑源、袁宏毅、李成鹏、董冠廷、陆克明、谭传奇、周常和周静仁。 2023.使用大型语言模型学习数学推理的缩放关系。 arXiv:2308.01825 [cs.CL] https://arxiv.org/abs/2308.01825 [38] Hansi Zeng、Chen Luo、Bowen Jin、Sheikh Muhammad Sarwar、Tianxin Wei 和 Hamed Zamani。 2024.可扩展且有效的生成信息检索。 2024 年 ACM 网络会议（新加坡、新加坡）（WWW '24）的会议记录。计算机协会，美国纽约州纽约市，1441–1452 年。

### 段落 111 · Page 10

**EN**

doi:10.1145/3589334.3645477 [39] Lunjun Zhang, Arian Hosseini, Hritik Bansal, Mehran Kazemi, Aviral Kumar, and Rishabh Agarwal. 2025. Generative Verifiers: Reward Modeling as Next-Token Prediction. InThe Thirteenth International Conference on Learning Representations. https://openreview.net/forum?id=Ccwp4tFEtE [40] Lianmin Zheng, Wei-Lin Chiang, Ying Sheng, Siyuan Zhuang, Zhanghao Wu, Yonghao Zhuang, Zi Lin, Zhuohan Li, Dacheng Li, Eric Xing, Hao Zhang, Joseph E Gonzalez, and Ion Stoica. 2023. Judging LLMas-a-Judge with MT-Bench and Chatbot Arena. InAdvances in Neural Information Processing Systems, A. Oh, T. Naumann, A. Globerson, K.

**中文**

doi:10.1145/3589334.3645477 [39] 张伦军、Arian Hosseini、Hritik Bansal、Mehran Kazemi、Aviral Kumar 和 Rishabh Agarwal。 2025.生成验证者：奖励建模作为下一个令牌预测。在第十三届学习表征国际会议上。 https://openreview.net/forum?id=Ccwp4tFEtE [40] Lianmin Cheng、Wei-Lin Jiang、Ying Shen、Siyuan Zhuang、Zhanghao Wu、Yonghao Zhuang、Zi Lin、Zhuohan Li、Da Cheng Li、Eric Xing、Hao Zhang、Joseph E Gonzalez 和 Ion Stoica。 2023. 使用 MT-Bench 和 Chatbot Arena 评审 LLMas-a-Judge。 《神经信息处理系统进展》，A. Oh、T. Naumann、A. Globerson、K.

### 段落 112 · Page 10

**EN**

Saenko, M. Hardt, and S. Levine (Eds.), Vol. 36. Curran Associates, Inc., 46595–46623. https://proceedings.neurips.cc/paper_files/paper/2023/file/ 91f18a1287b398d378ef22505bf41832-Paper-Datasets_and_Benchmarks.pdf [41] Yutao Zhu, Huaying Yuan, Shuting Wang, Jiongnan Liu, Wenhan Liu, Chenlong Deng, Haonan Chen, Zheng Liu, Zhicheng Dou, and Ji-Rong Wen. 2025. Large Language Models for Information Retrieval: A Survey.ACM Trans. Inf. Syst.44, 1, Article 12 (Nov. 2025), 54 pages.

**中文**

Saenko、M. Hardt 和 S. Levine（编辑），卷。 36.Curran Associates, Inc.，46595–46623。 https://proceedings.neurips.cc/paper_files/paper/2023/file/ 91f18a1287b398d378ef22505bf41832-Paper-Datasets_and_Benchmarks.pdf [41] 朱玉涛，袁华英，王淑婷，刘琼南，刘文汉，邓陈龙，陈浩南，刘政，志成窦和温继荣。 2025.信息检索的大型语言模型：一项调查。ACM Trans。信息。 Syst.44，1，第 12 条（2025 年 11 月），54 页。

### 段落 113 · Page 10

**EN**

doi:10.1145/3748304 A Qualitative Case Studies To provide a concrete understanding of the performance improvements, we present three qualitative case studies from real-world traffic. For the sake of readability, all case studies are presented in English translation, while the original user queries and model responses were in Chinese.

**中文**

doi:10.1145/3748304 定性案例研究 为了提供对性能改进的具体理解，我们提出了来自现实世界流量的三个定性案例研究。为了便于阅读，所有案例研究均以英文翻译呈现，而原始用户查询和模型响应均以中文呈现。

### 段落 114 · Page 10

**EN**

These examples compare the responses generated by SearchLLM against the SFT baseline: • Robustness to Outdated Evidence (R1):Figure 6 (Case Study 1) demonstrates how our model effectively handles noisy retrieval by filtering out factually correct but temporally outdated information, whereas the baseline fails to recognize the event’s expiration. • Bottom-line Safety Guarantees (R2):Figure 7 (Case Study 2) highlights our model’s adherence to strict factual and safety constraints in medical domains, correcting the baseline’s dangerous hallucination regarding pathogen classification.

**中文**

这些示例将 SearchLLM 生成的响应与 SFT 基线进行比较： • 对过时证据的稳健性 (R1)：图 6（案例研究 1）演示了我们的模型如何通过过滤掉事实上正确但暂时过时的信息来有效处理噪声检索，而基线无法识别事件的过期。 • 底线安全保证（R2）：图7（案例研究2）强调了我们的模型遵守医学领域严格的事实和安全约束，纠正了基线关于病原体分类的危险幻觉。

### 段落 115 · Page 10

**EN**

• Alignment with User Needs (R3):Figure 8 (Case Study 3) illustrates how our model aligns with user intent for concise and logical solutions, eliminating the redundancy and logical conflicts observed in the baseline. B Human Annotation Interface To ensure the high quality and consistency of our reward signals, we developed a specialized human annotation platform designed to align judges with expert preferences. As illustrated in Figure 9, the interface is structured to support a rigorous review process.

**中文**

• 与用户需求保持一致(R3)：图8（案例研究3）说明了我们的模型如何与用户意图保持一致，以提供简洁且合乎逻辑的解决方案，从而消除在基线中观察到的冗余和逻辑冲突。 B 人工注释界面 为了确保奖励信号的高质量和一致性，我们开发了专门的人工注释平台，旨在使评委与专家偏好保持一致。如图 9 所示，该界面的结构支持严格的审查流程。

### 段落 116 · Page 10

**EN**

For each task, the annotator is presented with the raw user query and the candidate responses, alongside the intent analysis generated by the policy model and retrieved reference notes. This context ensures that judgments are grounded in accurate information rather than annotator intuition. The annotation workflow consists of two granularities: • Pointwise Evaluation:Annotators first evaluate each response independently against our bottom-line constraints, scoring specific dimensions such as factual grounding, safety, and format compliance.

**中文**

对于每个任务，注释者都会看到原始用户查询和候选响应，以及策略模型生成的意图分析和检索到的参考注释。这种背景确保判断基于准确的信息而不是注释者的直觉。注释工作流程由两个粒度组成： • 逐点评估：注释者首先根据我们的底线约束独立评估每个响应，对特定维度（例如事实基础、安全性和格式合规性）进行评分。

### 段落 117 · Page 10

**EN**

• Pairwise Ranking:After individual scoring, annotators perform a side-by-side comparison of candidate responses to provide holistic preference signals, which are closely correlated with the remaining reward dimensions. This dual-granularity feedback mechanism enables hierarchical governance of non-negotiable safety boundaries and preferenceoriented quality metrics during the reward modeling phase. C Reward Dimension Definitions In this section, we provide detailed definitions and implementation methods for the multi-dimensional reward system described in Section 3.2.

**中文**

• 成对排名：个人评分后，注释者对候选答案进行并排比较，以提供与其余奖励维度密切相关的整体偏好信号。这种双粒度反馈机制可以在奖励建模阶段对不可协商的安全边界和面向偏好的质量指标进行分层治理。 C 奖励维度定义 在本节中，我们为 3.2 节中描述的多维度奖励系统提供详细的定义和实现方法。

### 段落 118 · Page 10

**EN**

Table 5 lists all criteria used in our hybrid evaluation stack, distinguishing between Bottom-line Constraints (Layer I) and Behavioral Objectives (Layer II). The "Implementation" column indicates whether a metric is computed via deterministic rules (Rule-based) or model judges (LLM-based).

**中文**

表 5 列出了我们的混合评估堆栈中使用的所有标准，区分底线约束（第一层）和行为目标（第二层）。 “实现”列指示指标是通过确定性规则（基于规则）还是模型判断（基于 LLM）计算。

### Page 11

### 段落 119 · Page 11

**EN**

Aligning Large Language Models with Searcher Preferences KDD ’26, August 9–13, 2026, Jeju, Korea D Dataset Specifications To support training and evaluation, we construct four distinct datasets from RedNote search logs: • Reward Training Dataset ( DRM-Train):Comprising 40,000 samples, this dataset facilitates the calibration of our hybrid evaluation stack and the training of baseline reward modeling methods.

**中文**

将大型语言模型与搜索者偏好保持一致 KDD’26，2026 年 8 月 9-13 日，韩国济州 D 数据集规范 为了支持训练和评估，我们从 RedNote 搜索日志构建了四个不同的数据集： • 奖励训练数据集 (DRM-Train)：该数据集包含 40,000 个样本，有助于校准我们的混合评估堆栈和基线奖励建模方法的训练。

### 段落 120 · Page 11

**EN**

Constructed via stratified sampling of random logs and "hard samples" (historical failure cases), it adopts distinct formats: pairwise comparisons {(𝑥, 𝑦 𝑤 , 𝑦𝑙 )} for subjective preference criteria, and pointwise instances {(𝑥, 𝑦, 𝑠)} with binary expert labels (𝑠∈ {0,1}) for objective constraints. • Dimension-Specific Test Set (DEval-Dim):Designed to address RQ1, this held-out diagnostic set features samples explicitly tagged with specific quality issues (e.g., hallucination, formatting errors). Containing 800 to 3,600 examples per dimension, it allows us to evaluate the alignment with human judgment on individual criteria.

**中文**

它通过随机日志和“硬样本”（历史失败案例）的分层采样构建，采用不同的格式：成对比较 {(𝑥, 𝑦 𝑤, 𝑦𝑙)} 用于主观偏好标准，点状实例 {(𝑥, 𝑦, 𝑠)} 与二进制专家标签 (𝑠ε {0,1}) 用于客观约束。 • 维度特定测试集 (DEval-Dim)：该保留诊断集旨在解决 RQ1，其特征是明确标记有特定质量问题（例如幻觉、格式错误）的样本。每个维度包含 800 到 3,600 个示例，它使我们能够评估个人标准与人类判断的一致性。

### 段落 121 · Page 11

**EN**

• Holistic Preference Test Set ( DEval-Holistic):Also serving RQ1, this dataset comprises 2,800 pairwise comparisons sourced from historical model checkpoints and human writing. It utilizes general "win/loss" labels to assess the holistic preference alignment of the reward system. • RL Optimization Dataset ( DRL):Comprising 500,000 unlabeled tuples (𝑞, ℎ, 𝐸), this dataset supports policy optimization (RQ2–4). The training set mixes random traffic with user complaint queries to enhance robustness. E Evaluation Metrics In this section, we provide the detailed definitions for the offline and online metrics used to assess our system.

**中文**

• 整体偏好测试集（DEval-Holistic）：该数据集也服务于 RQ1，包含源自历史模型检查点和人工书写的 2,800 个成对比较。它利用一般的“赢/输”标签来评估奖励系统的整体偏好一致性。 • RL 优化数据集（DRL）：包含 500,000 个未标记元组（𝑞、ℎ、𝐸），该数据集支持策略优化（RQ2-4）。训练集将随机流量与用户投诉查询混合以增强鲁棒性。 E 评估指标 在本节中，我们提供用于评估我们的系统的离线和在线指标的详细定义。

### 段落 122 · Page 11

**EN**

Offline Evaluation.We validate the reward model’s alignment with human experts using two standard metrics: • Accuracy (ACC):Measures the agreement between reward signals and expert labels on binary constraint reward dimensions (e.g., Factuality, Format Compliance). • Area Under the Curve (AUC):Evaluates the pairwise ranking capability on subjective preference dimensions (e.g., Richness, Usability). Given 𝑁 pairs (𝑦𝑤 , 𝑦𝑙 ) where 𝑦𝑤 is the preferred response, and reward score𝑠(·), the AUC is computed as: AUC= 1 𝑁 𝑁∑︁ 𝑖=1 h I(𝑠(𝑦 (𝑖) 𝑤 )>𝑠(𝑦 (𝑖) 𝑙 )) +0.5·I(𝑠(𝑦 (𝑖) 𝑤 )=𝑠(𝑦 (𝑖) 𝑙 )) i .

**中文**

离线评估。我们使用两个标准指标来验证奖励模型与人类专家的一致性： • 准确性（ACC）：衡量奖励信号和专家标签在二元约束奖励维度（例如，事实性、格式合规性）上的一致性。 • 曲线下面积 (AUC)：评估主观偏好维度（例如丰富度、可用性）的成对排名能力。给定 𝑁 对 (𝑦𝑤 , 𝑦𝑙 )，其中𝑦𝑤 是首选响应，奖励分数𝑠(·)，AUC 计算如下： AUC= 1 𝑁 𝑁Σ︁ 𝑖=1 h I(𝑠(𝑦 (𝑖) 𝑤) )>𝑠(𝑦 (𝑖) 𝑙 )) +0.5·I(𝑠(𝑦 (𝑖) 𝑤 )=𝑠(𝑦 (𝑖) 𝑙 )) i。

### 段落 123 · Page 11

**EN**

(7) Online Evaluation.To measure real-world impact, we conducted online A/B testing and monitored the following metrics: • Valid Consumption Rate (VCR):The percentage of sessions where users dwell on the generated answer for a meaningful duration (>5s), indicating high utility. VCR= 1 𝑀 𝑀∑︁ 𝑗=1 I(𝑇 (𝑗) dwell >5s)(8) • Skip Rate (SR):The percentage of sessions where the answer is scrolled past immediately ( < 1.5s), serving as a proxy for irrelevance or poor formatting.

**中文**

(7) 在线评估。为了衡量现实世界的影响，我们进行了在线 A/B 测试并监控以下指标： • 有效消耗率 (VCR)：用户在生成的答案上停留有意义的持续时间（>5 秒）的会话百分比，表明效用较高。 VCR= 1 𝑀 𝑀Σ︁ 𝑗=1 I(𝑇 (𝑗) 停留 >5 秒)(8) • 跳过率 (SR)：答案立即滚动过去的会话百分比（< 1.5 秒），作为不相关或格式不良的代理。

### 段落 124 · Page 11

**EN**

SR= 1 𝑀 𝑀∑︁ 𝑗=1 I(𝑇 (𝑗) dwell <1.5s)(9) • Re-search Rate (RR):The frequency with which users issue a reformulated query immediately after viewing the result, indicating dissatisfaction. • Bad Case Rate (BCR):The percentage of responses containing severe bottom-line violations (e.g., safety risks, obvious hallucinations). This metric is estimated via a daily human audit of sampled logs. F Supplementary Training Dynamics We present the evolution curves for the remaining reward dimensions that were not visualized in the main text due to space constraints.

**中文**

SR= 1 𝑀 𝑀Σ︁ 𝑗=1 I(𝑇 (𝑗) 停留<1.5s)(9) • 重新搜索率(RR)：用户在查看结果后立即发出重新表述的查询的频率，表明不满意。 • 不良案例率 (BCR)：包含严重违反底线（例如安全风险、明显幻觉）的响应的百分比。该指标是通过每日对采样日志进行人工审核来估计的。 F 补充训练动态 我们展示了由于空间限制而在正文中未可视化的剩余奖励维度的演化曲线。

### 段落 125 · Page 11

**EN**

As shown in Figure 10, the Gated Aggregation Strategy demonstrates consistent stability across the full spectrum of reward signals, corroborating the conclusions drawn in Section 4.4.

**中文**

如图 10 所示，门控聚合策略在整个奖励信号范围内表现出一致的稳定性，证实了第 4.4 节中得出的结论。

### Page 12

### 段落 126 · Page 12

**EN**

KDD ’26, August 9–13, 2026, Jeju, Korea Wei Wu, Peilun Zhou, et al. User Query Context: Current Date Jan 2026 (Event was Aug 2025) When can I listen to the song "Skibidi" for free? Response from SearchLLM (Ours) Temporal Relevance JJ Lin and Jackie Chan’s song "Skibidi"has already been released (premiered on Aug 27, 2025). Since the radio premiere event has ended, you can currently listen to it for free on the following platforms: • Video Platforms:Search for the official music video onBilibilior YouTube[Doc 2]. • Music Apps:It is now available on Spotify, Apple Music, and KKBox (free tier supported)[Doc 1,6].

**中文**

KDD ’26，2026 年 8 月 9-13 日，韩国济州 Wei Wu、Peilun Zhou 等。用户查询上下文：当前日期 2026 年 1 月（活动时间为 2025 年 8 月） 我什么时候可以免费收听歌曲“Skibidi”？ SearchLLM（我们的）时间相关性的回应 林俊杰和成龙的歌曲《Skibidi》已经发布（2025年8月27日首播）。由于电台首播活动已经结束，目前您可以在以下平台免费收听： • 视频平台：在Bilibili 或YouTube 上搜索官方音乐视频[Doc 2]。 • 音乐应用程序：现已在Spotify、Apple Music 和KKBox 上提供（支持免费套餐）[Doc 1,6]。

### 段落 127 · Page 12

**EN**

Response from Baseline (SFT) Outdated Information JJ Lin and Jackie Chan’s new song "Skibidi" will premiere globally on August 27, 2025, at 10:00 AMvia major radio stations[Doc 3,4]. If you want to listen for free, you can try the following methods: • Radio Premiere:This is the official free channel. Please tune in to stations like Hit Fm, Singapore UFM100.3, or Malaysia MY FM at the specific time[Doc 3,4]. • Online Radio:Use the "Radio" feature in NetEase Cloud Music to find the station and collect it[Doc 6]. • Video Platforms:Although the premiere is on radio, users often upload recordings to video sites later[Doc 1,2].

**中文**

Baseline (SFT) 回应 过时信息 林俊杰和成龙的新歌《Skibidi》将于2025年8月27日上午10:00通过各大电台全球首播[Doc 3,4]。如果您想免费收听，可以尝试以下方法： • Radio Premiere：这是官方免费频道。请在特定时间收听Hit Fm、新加坡UFM100.3、马来西亚MY FM等电台[Doc 3,4]。 • 在线电台：使用网易云音乐中的“电台”功能查找电台并收藏[文档6]。 • 视频平台：虽然首播是在广播中，但用户通常会稍后将录制内容上传到视频网站[文档1,2]。

### 段落 128 · Page 12

**EN**

Analysis & Critique Robustness to Outdated Evidence (R1):The Baseline model fails to validate the temporal applicability of the retrieved evidence. It treats a historical event ("Premiere in 2025") as a valid solution for a current query (2026), resulting in a non-actionable response. SearchLLM successfully identifies that the premiere information isoutdatedand filters it out, prioritizing currently accessible streaming channels. Figure 6: Case Study 1 highlighting improved temporal awareness for time sensitive queries User Query Why do my ’Peach Egg’ (Graptopetalum amethystinum) leaves have tumor-like bumps?

**中文**

对过时证据的分析和批判稳健性 (R1)：基线模型无法验证检索到的证据的时间适用性。它将历史事件（“2025 年首映”）视为当前查询（2026 年）的有效解决方案，从而产生不可操作的响应。 SearchLLM 成功识别首播信息已过时并将其过滤掉，优先考虑当前可访问的流媒体频道。图 6：案例研究 1 强调改进时间敏感查询的时间意识 用户查询 为什么我的“桃蛋”（Graptopetalum amethystinum）叶子有肿瘤状肿块？

### 段落 129 · Page 12

**EN**

Response from SearchLLM (Ours) The "tumor-like" growths on your Peach Egg leaves are likely symptoms ofAnthracnose. Diagnosis:This is afungal disease(usually caused byColletotrichum) often triggered by high humidity or poor ventilation[Doc 2]. Treatment: • Isolate:Separate the plant immediately to prevent spores from spreading. • Prune:Cut off infected leaves with sterilized scissors to reduce the source of infection. • Apply Fungicide:Use broad-spectrumfungicideslike Carbendazim or Chlorothalonil [Doc 2] . Spray 2-3 times ensuring coverage on both sides of leaves.

**中文**

SearchLLM（我们的）的回复 桃蛋叶子上的“肿瘤状”生长很可能是炭疽病的症状。诊断：这是一种真菌病（通常由炭疽菌引起），通常由高湿度或通风不良引发[Doc 2]。处理： • 隔离：立即分离植物以防止孢子传播。 • 修剪：用消毒剪刀剪掉受感染的叶子，减少感染源。 • 使用杀菌剂：使用广谱杀菌剂，如多菌灵或百菌清[文件2]。喷2-3次，确保覆盖叶子两侧。

### 段落 130 · Page 12

**EN**

Response from Baseline (SFT) The "tumor-like" growths on Peach Egg leaves are likely typical symptoms ofAnthracnose. This is a disease caused bybacteria [Doc 2] . Initial symptoms include small black spots... How to handle: • Immediate Isolation:Separate from healthy succulents to prevent bacterial transmission. • Spray Medication:You can use agents specifically forbacterial diseases, such as "Flower Health" antibiotics [Doc 2] . Spray 2-3 times... Daily Care Tips: • Control Watering:Water only when soil is dry ("better dry than wet"). •Ventilation:Keep environment ventilated to avoid humidity.

**中文**

基线响应 (SFT) 桃卵叶上的“肿瘤样”生长可能是炭疽病的典型症状。这是一种由细菌引起的疾病[Doc 2]。最初的症状包括小黑点... 如何处理： • 立即隔离：与健康的多肉植物分开，以防止细菌传播。 • 喷雾用药：可以使用专门针对细菌性疾病的药剂，例如“花健康”抗生素[Doc 2]。喷洒2-3次... 日常护理提示： • 控制浇水：仅在土壤干燥时浇水（“干比湿好”）。 •通风：保持环境通风，避免潮湿。

### 段落 131 · Page 12

**EN**

•Avoid Wounds:Bacteria enters through wounds easily. Analysis & Critique Factual & Safety Guarantee (R2):The Baseline model correctly identifies the disease name ("Anthracnose") but hallucinates the biological classification, labeling it asbacterialinstead offungal. Consequently, it recommends antibiotics ("Flower Health") which are ineffective against fungal pathogens. Our model correctly identifies the fungal nature and prescribes appropriate fungicides. Figure 7: Case Study 2 demonstrating the correction of factual hallucinations in domain specific queries

**中文**

•避免伤口：细菌很容易通过伤口进入。分析与批评事实与安全保证（R2）：基线模型正确识别了疾病名称（“炭疽病”），但对生物分类产生了幻觉，将其标记为细菌而不是真菌。因此，它推荐使用对真菌病原体无效的抗生素（“花健康”）。我们的模型正确识别真菌性质并开出适当的杀菌剂。图 7：案例研究 2 展示了特定领域查询中事实幻觉的纠正

### Page 13

### 段落 132 · Page 13

**EN**

Aligning Large Language Models with Searcher Preferences KDD ’26, August 9–13, 2026, Jeju, Korea User Query Which gate should I enter for Baixi from Wanda Resort? Response from SearchLLM (Ours) From Wanda Resort to the Changbai MountainBaixiscenic area, you should enter through theBaixi Distribution Center Main Entrance. Key Steps: (1) Entrance:Proceed directly to the main tourist hall for security check and ticket validation[Doc 1]. (2) Documents:Must bring your ID card (Physical ID required) for pre-check[Doc 1]. (3)Timing:Arrive 30 minutes before your booked slot[Doc 1].

**中文**

将大型语言模型与搜索者偏好保持一致 KDD ’26，2026 年 8 月 9 日至 13 日，韩国济州 用户查询从万达度假村到白溪我应该进入哪个门？回复SearchLLM (Ours) 从万达度假区到长白山白溪景区，应从白溪配送中心正门进入。关键步骤：（1）入口：直接前往游客主大厅进行安全检查和门票验证[文件1]。 (2) 文件：必须携带身份证（需要实体身份证）进行预查[Doc 1]。 (3)时间：在您预订的时段前30分钟到达[Doc 1]。

### 段落 133 · Page 13

**EN**

Response from Baseline (SFT) From Wanda to Changbai Mountain, it is usually recommended to enter from theWest Slope Distribution Centermain entrance [Doc 1] . This is the main pick-up point for buses. Traffic and Cost: • Taxi:From Wanda to Baixi is about 20 yuan more expensive than West Slope. Note: Taxis here do not use meters, keep the driver’s phone number[Doc 1]. Tour Tips: • Motion Sickness:The mountain road has 18 bends, prepare medicine [Doc 1]. • Clothing: Even in summer, the wind is strong, so wear a windbreaker[Doc 1].

**中文**

基线（SFT）回复 从万达到长白山，通常建议从西坡集散中心主入口进入[文件1]。这是巴士的主要上车点。交通及费用： • 出租车：从万达到白溪比西坡贵20元左右。注意：这里的出租车不打表，请保留司机的电话号码[Doc 1]。游览温馨提示： • 晕车：山路十八弯，请备好药品【Doc 1】。 • 衣服：即使在夏天，风也很大，所以要穿防风衣[Doc 1]。

### 段落 134 · Page 13

**EN**

Analysis & Critique Alignment with User Needs (R3):1.Entity Error:The Baseline confuses "Baixi" with "West Slope Center". 2.Redundancy:It includes excessive irrelevant details (taxi scams, motion sickness) that dilute the answer. 3.Logic Error:It assumes the season is "Summer" without user input. Our model aligns with the user’s specific need for navigation instructions. Figure 8: Case Study 3 showcasing reduction of logical inconsistencies and redundancy in complex tasks Figure 9: Screenshot of the human annotation interface. The workbench presents the query, user intent analysis, and reference notes.

**中文**

分析与批判与用户需求的一致性（R3）：1.实体错误：基线混淆了“白溪”和“西坡中心”。 2.冗余：它包括过多的不相关细节（出租车诈骗、晕车），从而稀释了答案。 3.逻辑错误：在没有用户输入的情况下假设季节是“夏季”。我们的模型符合用户对导航指令的特定需求。图 8：案例研究 3 展示了复杂任务中逻辑不一致和冗余的减少。 图 9：人工注释界面的屏幕截图。该工作台呈现查询、用户意图分析和参考注释。

### 段落 135 · Page 13

**EN**

Annotators provide dual-granularity feedback: fine-grained scores on specific dimensions and holistic pairwise rankings.

**中文**

注释器提供双粒度反馈：特定维度的细粒度分数和整体成对排名。

### Page 14

### 段落 136 · Page 14

**EN**

KDD ’26, August 9–13, 2026, Jeju, Korea Wei Wu, Peilun Zhou, et al. Table 5: Detailed Definitions of Multi-Dimensional Reward Criteria. Layer Requirement Subset Reward Dimension Implementation Definition / Role Layer I (Bottom-line) R2 Hallucination Highlight Hallucination LLM-based First sentence free of obvious hallucinations. Claim Hallucination LLM-based Non-hallucination at the claim level. LLM Knowledge LLM-based Checks knowledge correctness with external validation. No Supply Reject LLM-based Proper refusal behavior when no evidence is available.

**中文**

KDD ’26，2026 年 8 月 9-13 日，韩国济州 Wei Wu、Peilun Zhou 等。表5：多维度奖励标准的详细定义。层要求子集奖励维度实施定义/角色层I（底线）R2幻觉突出幻觉基于法学硕士第一句话没有明显的幻觉。索赔幻觉 基于法学硕士的索赔级别无幻觉。 LLM 知识 基于 LLM 通过外部验证检查知识的正确性。无供应拒绝 基于法学硕士 在没有证据可用时的正确拒绝行为。

### 段落 137 · Page 14

**EN**

Basic Quality Self Consistency LLM-based Logical self-consistency, no internal contradictions. Answer Quality LLM-based Avoids gibberish or extremely low-quality answers. Multi-round Repeat Conflict LLM-based No strong repetition or contradiction across turns. Format Format Rule-based Enforces structured and well-formed output format. Response Length Rule-based Keeps answer length in an acceptable range. Layer II (Behavioral) R1 Query Query Satisfaction LLM-based Basic intent alignment, avoids “answering B when asked A”. Planning Quality LLM-based Quality of reasoning and planning under uncertainty.

**中文**

基本品质自洽 基于法学硕士 逻辑自洽，无内部矛盾。答案质量 基于法学硕士 避免乱码或质量极低的答案。多轮重复冲突 基于法学硕士 轮次之间没有强烈的重复或矛盾。格式 基于规则的格式 强制执行结构化且格式良好的输出格式。响应长度 基于规则 将答案长度保持在可接受的范围内。第二层（行为）R1 查询查询满意度基于 LLM 的基本意图对齐，避免“当问 A 时回答 B”。规划质量基于法学硕士的不确定性下的推理和规划质量。

### 段落 138 · Page 14

**EN**

Evidence Reference Beneficiality LLM-based Evidence truly helps answer the question. Reference Conflict LLM-based Detects strong conflicts among evidence items. Reference Irrelevant LLM-based Detects evidence completely irrelevant to the query. Reference Satisfaction LLM-based Evidence covers primary and secondary needs. Reference Diversity LLM-based Promotes diverse evidence for robustness. R3 Richness Claim Diversity LLM-based Rich and diverse answer claims. Usability Answer Useful LLM-based Low fraction of off-topic content; conciseness. Answer Firstness LLM-based Places core answer early for quick consumption.

**中文**

证据参考效益基于法学硕士的证据确实有助于回答这个问题。参考冲突 基于法学硕士 检测证据项目之间的强烈冲突。参考 不相关 基于 LLM 检测与查询完全不相关的证据。基于法学硕士的参考满意度证据涵盖主要和次要需求。基于法学硕士的参考多样性促进多样化证据的稳健性。 R3 丰富性主张多样性 基于法学硕士的丰富多样的答案主张。可用性答案 有用的 基于法学硕士 离题内容比例低；简明。基于法学硕士的答案第一性尽早放置核心答案，以便快速使用。

### 段落 139 · Page 14

**EN**

Redundant Repetition LLM-based Controls severe semantic redundancy and rambling.

**中文**

冗余重复 基于法学硕士 控制严重的语义冗余和杂乱无章。

### 段落 140 · Page 14

**EN**

0.900 0.925 0.950 0.975 Planning Quality 0.7 0.8 0.9 Reference Irrelevant 0.4 0.5 0.6 Reference Satisfaction 0.96 0.98 1.00 Answer Quality 0.900 0.925 0.950 0.975 Self Consist 0.980 0.985 0.990 0.995 1.000 Multirounds Repeat Conflict 0.97 0.98 0.99 1.00 Llm Knowledge 0.94 0.96 0.98 1.00 No Supply Reject 0.94 0.96 0.98 1.00 Response Length 0 100 200 300 400 500 600 700 800 0.90 0.95 1.00 Format 0 100 200 300 400 500 600 700 800 0.7 0.8 0.9 Answer Useful 0 100 200 300 400 500 600 700 800 0.84 0.86 0.88 0.90 0.92 Redundant Repetition Training Step Reward Score GRPO-Gated GRPO-Linear (Weighted Sum) GRPO-Linear (Sum) Figure 10: Supplementary training dynamics showing the evolution of the remaining reward dimensions.

**中文**

0.900 0.925 0.950 0.975 规划质量 0.7 0.8 0.9 参考不相关 0.4 0.5 0.6 参考满意度 0.96 0.98 1.00 答案质量 0.900 0.925 0.950 0.975 自包含 0.980 0.985 0.990 0.995 1.000 多轮重复冲突 0.97 0.98 0.99 1.00 Llm 知识 0.94 0.96 0.98 1.00 无供应拒绝 0.94 0.96 0.98 1.00 响应长度 0 100 200 300 400 500 600 700 800 0.90 0.95 1.00 格式 0 100 200 300 400 500 600 700 800 0.7 0.8 0.9 答案 有用 0 100 200 300 400 500 600 700 800 0.84 0.86 0.88 0.90 0.92 冗余重复训练步骤奖励分数 GRPO 门控 GRPO-线性（加权总和） GRPO-线性（总和） 图 10：显示剩余奖励维度演变的补充训练动态。
