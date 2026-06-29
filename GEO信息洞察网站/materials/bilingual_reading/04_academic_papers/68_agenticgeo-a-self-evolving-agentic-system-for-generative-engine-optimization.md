# AgenticGEO: A Self-Evolving Agentic System for Generative Engine Optimization

- ID: 68
- 类型: pdf
- 分类: 04_academic_papers
- 主题: agentic optimization for GEO visibility and attribution
- 原文链接: https://arxiv.org/pdf/2603.20213
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

AgenticGEO: A Self-Evolving Agentic System for Generative Engine Optimization Jiaqi Yuan School of Computer Science and Engineering, Beihang University Beijing, China yuanjq@buaa.edu.cn Jialu Wang Independent Contributor CA, United States faldict@ucsc.edu Zihan Wang School of Computer Science and Engineering, Beihang University Beijing, China wzhan@buaa.edu.cn Qingyun Sun School of Computer Science and Engineering, Beihang University Beijing, China sunqy@buaa.edu.cn Ruijie Wang∗ School of Computer Science and Engineering, Beihang University Beijing, China ruijiew@buaa.edu.cn Jianxin Li School of Computer Science and Engineering, Beihang Unive

**中文**

AgenticGEO：用于生成式引擎优化的自进化代理系统 Jiaqi Yuan 北京航空航天大学计算机科学与工程学院，中国，yuanjq@buaa.edu.cn Jialu Wang 独立贡献者 CA，美国 faldict@ucsc.edu Zihan Wang，北京航空航天大学计算机科学与工程学院，中国，北京 wzhan@buaa.edu.cn Qingyun Sun，北京航空航天大学计算机科学与工程学院，中国，北京sunqy@buaa.edu.cn 王瑞杰* 北京航空航天大学计算机科学与工程学院 中国北京 ruijiew@buaa.edu.cn 李建新 北京航空航天大学计算机科学与工程学院

### 段落 2 · Page 1

**EN**

rsity Beijing, China lijx@buaa.edu.cn Abstract Generative search engines represent a transition from traditional ranking-based retrieval to Large Language Model (LLM)-based synthesis, transforming optimization goals from ranking prominence towards content inclusion.

**中文**

rsity 中国北京 lijx@buaa.edu.cn 摘要 生成式搜索引擎代表了从传统的基于排名的检索到基于大语言模型（LLM）的综合的转变，将优化目标从排名突出转向内容包含。

### 段落 3 · Page 1

**EN**

Generative Engine Optimization (GEO), specifically, aims to maximize visibility and attribution in black-box summarized outputs by strategically manipulating source content. However, existing methods rely on static heuristics, single-prompt optimization, or engine preference rule distillation that is prone to overfitting. They cannot flexibly adapt to diverse content or the changing behaviors of generative engines. Moreover, effectively optimizing these strategies requires an impractical amount of interaction feedback from the engines.

**中文**

具体而言，生成式引擎优化 (GEO) 旨在通过策略性地操纵源内容来最大限度地提高黑盒汇总输出的可见性和归因。然而，现有方法依赖于静态启发式、单提示优化或引擎偏好规则蒸馏，容易出现过度拟合。它们无法灵活地适应不同的内容或生成式引擎不断变化的行为。此外，有效优化这些策略需要引擎提供大量不切实际的交互反馈。

### 段落 4 · Page 1

**EN**

To address these challenges, we propose AgenticGEO, a self-evolving agentic framework formulating optimization as a content-conditioned control problem, which enhances intrinsic content quality to robustly adapt to the unpredictable behaviors of black-box engines. Unlike fixed-strategy methods, AgenticGEO employs a MAP-Elites archive to evolve diverse, compositional strategies. To mitigate interaction costs, we introduce a Co-Evolving Critic, a lightweight surrogate that approximates engine feedback for content-specific strategy selection and refinement, efficiently guiding both evolutionary search and inferencetime planning.

**中文**

为了应对这些挑战，我们提出了 AgenticGEO，这是一种自我进化的代理框架，将优化表述为内容条件控制问题，它增强了内在内容质量，以稳健地适应黑盒引擎不可预测的行为。与固定策略方法不同，AgenticGEO 采用 MAP-Elites 档案来发展多样化的组合策略。为了降低交互成本，我们引入了共同进化批评家，这是一种轻量级代理，可以近似引擎反馈以进行特定于内容的策略选择和细化，从而有效地指导进化搜索和推理时间规划。

### 段落 5 · Page 1

**EN**

Through extensive in-domain and cross-domain experiments on two representative engines, AgenticGEO achieves state-of-the-art performance and demonstrates robust transferability, outperforming 14 baselines across 3 datasets. Our code and model are available at: https://github.com/AIcling/agentic_geo. ∗Corresponding Author. Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page.

**中文**

通过对两个代表性引擎进行广泛的域内和跨域实验，AgenticGEO 实现了最先进的性能，并展示了强大的可迁移性，在 3 个数据集上优于 14 个基线。我们的代码和模型位于：https://github.com/AIcling/agentic_geo。 *通讯作者。允许免费制作本作品全部或部分内容的数字或硬拷贝以供个人或课堂使用，前提是制作或分发副本不是为了盈利或商业利益，并且副本在首页上附有此通知和完整引用。

### 段落 6 · Page 1

**EN**

Copyrights for components of this work owned by others than the author(s) must be honored. Abstracting with credit is permitted. To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee. Request permissions from permissions@acm.org. Conference acronym ’XX, Woodstock, NY ©2018 Copyright held by the owner/author(s). Publication rights licensed to ACM. ACM ISBN 978-1-4503-XXXX-X/2018/06 https://doi.org/XXXXXXX.XXXXXXX CCS Concepts •Computing methodologies → Natural language processing; •Information systems→Information retrieval.

**中文**

必须尊重作者以外的其他人拥有的本作品组件的版权。允许以信用方式提取。要以其他方式复制、重新发布、发布到服务器上或重新分发到列表，需要事先获得特定许可和/或付费。从permissions@acm.org 请求权限。会议首字母缩略词 'XX，伍德斯托克，纽约 ©2018 版权归所有者/作者所有。出版权授权给 ACM。 ACM ISBN 978-1-4503-XXXX-X/2018/06 https://doi.org/XXXXXXX.XXXXXXX CCS 概念 •计算方法→自然语言处理； •信息系统→信息检索。

### 段落 7 · Page 1

**EN**

Keywords Generative Engine Optimization, Agentic Systems, Online Co- Evolution, Black-Box Optimization, Domain Generalization ACM Reference Format: Jiaqi Yuan, Jialu Wang, Zihan Wang, Qingyun Sun, Ruijie Wang, and Jianxin Li. 2018. AgenticGEO: A Self-Evolving Agentic System for Generative Engine Optimization. InProceedings of Make sure to enter the correct conference title from your rights confirmation email (Conference acronym ’XX).ACM, New York, NY, USA, 16 pages.

**中文**

关键词 生成式引擎优化，代理系统，在线协同进化，黑盒优化，领域泛化 ACM 参考格式：Jiaqi Yuan，Jialu Wang，Zihan Wang，Qingyun Sun，Ruijie Wang，Jianxin Li。 2018. AgenticGEO：用于生成式引擎优化的自我进化代理系统。请确保在您的权利确认电子邮件中输入正确的会议标题（会议缩写“XX”）。ACM，美国纽约州纽约市，16 页。

### 段落 8 · Page 1

**EN**

https://doi.org/XXXXXXX.XXXXXXX 1 Introduction Generative search engines(e.g., Google AI Overviews [ 7, 49], Bing Search [3], Perplexity AI [40]) are increasingly dominant in information access, shifting users from browsing ranked webpages to consuming summarized answers directly provided by Large Language Models (LLMs). In contrast to traditional search engines that act as gateways to links, these systems retrieve evidence from multiple sources and compose it into a single, coherent summary, often accompanied by explicit citations [13, 32, 34].

**中文**

https://doi.org/XXXXXXX.XXXXXXX 1 简介 生成式搜索引擎（例如，Google AI Overviews [ 7, 49]、Bing Search [3]、Perplexity AI [40]）在信息访问中日益占据主导地位，将用户从浏览排名网页转向消费由大型语言模型 (LLM) 直接提供的汇总答案。与充当链接网关的传统搜索引擎相比，这些系统从多个来源检索证据并将其组成一个单一的、连贯的摘要，通常伴有明确的引用[13,32,34]。

### 段落 9 · Page 1

**EN**

This paradigm shift fundamentally alters the web ecosystem, transforming the engine from a content ranker into a direct information summarizer. This paper studies Generative Engine Optimization (GEO) [1, 8], which is an emerging optimization problem induced by this transition. While traditional Search Engine Optimization (SEO) [ 2, 45] aims to maximize the position of a source content within a ranked list by optimizing retrieval signals (e.g., keywords and backlinks) [43, 64], it is insufficient for modeling how LLMs synthesize and attribute evidence [22, 36].

**中文**

这种范式转变从根本上改变了网络生态系统，将引擎从内容排名器转变为直接信息摘要器。本文研究了生成式引擎优化（GEO）[1, 8]，这是由这种转变引发的一个新兴优化问题。虽然传统的搜索引擎优化 (SEO) [2, 45] 旨在通过优化检索信号（例如关键字和反向链接）来最大化源内容在排名列表中的位置 [43, 64]，但不足以对法学硕士如何合成和属性证据进行建模 [22, 36]。

### 段落 10 · Page 1

**EN**

In contrast, GEO targets two distinct objectives: (1)Visibility, the extent to which a source’s information is incorporated into the generated answer and (2)Attribution, whether and where the source is explicitly cited. GEO is critical for the sustainability of the web ecosystem, as generative answers increasingly govern the allocation of user attention [4, 49]. arXiv:2603.20213v1 [cs.AI] 2 Mar 2026

**中文**

相比之下，GEO 针对两个不同的目标：(1) 可见性，即来源信息纳入生成答案的程度；(2) 归属，即来源是否以及在何处被明确引用。 GEO 对于网络生态系统的可持续性至关重要，因为生成答案越来越多地控制着用户注意力的分配 [4, 49]。 arXiv:2603.20213v1 [cs.AI] 2026 年 3 月 2 日

### Page 2

### 段落 11 · Page 2

**EN**

Conference acronym ’XX, June 03–05, 2018, Woodstock, NY Jiaqi Yuan, Jialu Wang et al. 0.0 0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9 Strategy Sensitivity (Normalized) 0.0 0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9Max Gain over Strategies Robustly Optimizable Optimization-Resistant Strategy-Dependent Low-Yield & Volatile Figure 1: Characterization of the GEO result on GEO-Bench instances. 𝑦-axis reports maximum performance among 9 rewriting strategies, and 𝑥-axis reports performance variance among strategies. (i) Optimization success varies greatly by strategy and content.

**中文**

会议缩写’XX，2018 年 6 月 3-05 日，纽约州伍德斯托克，Jiaqi Yuan、Jialu Wang 等人。 0.0 0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9 策略敏感度（标准化） 0.0 0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9 最大策略增益 稳健可优化 抗优化 策略相关低产量和不稳定 图 1：GEO-Bench 实例上 GEO 结果的表征。 𝑦轴报告 9 种重写策略中的最大性能，𝑥 轴报告策略之间的性能差异。 (i) 优化成功与否因策略和内容的不同而有很大差异。

### 段落 12 · Page 2

**EN**

(ii) Existing strategies fail to optimize nearly half of instances (points in gray and red areas), indicating static strategy pool is not enough and needs evolving. Details can be found in Appendix A.1.1. Despite the growing interest in GEO, the field still remains underexplored. As evidenced by the strategy sensitivity analysis (Figure 1), optimization success varies greatly by strategy and content. Meanwhile, existing strategies fail to optimize nearly half of the samples.

**中文**

(ii) 现有策略未能优化近一半的实例（灰色和红色区域中的点），表明静态策略池是不够的，需要不断发展。详细信息参见附录A.1.1。尽管人们对 GEO 的兴趣日益浓厚，但该领域仍未得到充分探索。正如策略敏感性分析（图 1）所证明的那样，优化成功与否因策略和内容的不同而差异很大。同时，现有策略未能优化近一半的样本。

### 段落 13 · Page 2

**EN**

These findings indicate the need for both customized strategy selection for each piece of content and refining the static strategy pool so it can adapt to new content patterns. However, existing work fail to achieve the goal, where they can be broadly categorized into: static heuristics approaches[ 1] andlearning-based approaches[ 54]. Static heuristic approaches apply heuristic rewriting strategies (i.e., rewriting prompt templates instructing an LLM) to source content. However, this paradigm overlooks the heterogeneity of content and apply single strategy for all cotents.

**中文**

这些发现表明需要为每段内容进行定制策略选择并完善静态策略池，以便它能够适应新的内容模式。然而，现有的工作未能实现这一目标，它们可以大致分为：静态启发式方法[1]和基于学习的方法[54]。静态启发式方法将启发式重写策略（即重写指导法学硕士的提示模板）应用于源内容。然而，这种范式忽视了内容的异质性，并对所有内容应用单一策略。

### 段落 14 · Page 2

**EN**

Learning-based approaches, in contrast, adapt rewriting strategies to the behavior of a specific generative engine (GE). Although effective in controlled settings, they tend to overfit to engine-specific patterns and degrade when the engine updates. In a non-stationary black-box environment, where retrieval, synthesis, and citation behaviors evolve over time, a static strategy pool is suboptimal and prone to miscalibration. Moreover, learning-based methods depend on frequent and intensive feedback from the specific generative engine during training, which is costly and often infeasible in real-world systems.

**中文**

相比之下，基于学习的方法使重写策略适应特定生成式引擎（GE）的行为。尽管在受控设置中有效，但它们往往会过度适应特定于引擎的模式，并在引擎更新时性能下降。在非静态黑盒环境中，检索、综合和引用行为随着时间的推移而演变，静态策略池不是最优的，并且容易出现错误校准。此外，基于学习的方法依赖于训练期间特定生成式引擎的频繁而密集的反馈，这在现实系统中成本高昂且通常不可行。

### 段落 15 · Page 2

**EN**

These limitations highlight two key challenges for GEO:(i) Designing evolving methods that can flexibly adapt to diverse content and varying generative engine behaviors; (ii) Achieving effective optimization without relying on intensive feedback from generative engines. Motivated by these insights, we introduceAgenticGEO, a selfevolving agentic system that formulates GEO as learning a contentconditioned control policy, enhancing intrinsic quality for robust adaptation to black-box engines.

**中文**

这些限制凸显了 GEO 面临的两个关键挑战：(i) 设计能够灵活适应不同内容和不同生成式引擎行为的不断发展的方法； (ii) 在不依赖生成式引擎的密集反馈的情况下实现有效的优化。受这些见解的激励，我们引入了AgenticGEO，这是一种自我进化的代理系统，它将GEO制定为学习内容条件控制策略，从而增强了对黑盒引擎的稳健适应的内在质量。

### 段落 16 · Page 2

**EN**

As illustrated in Fig2, instead of applying a fixed rewrite heuristic, AgenticGEO maintains an evolvingQuality-Diversity (QD) Archiveas external memory, preserving high-performing yet diverse strategies. Each strategy represents Fix ed Strat egy GE O Critic Strat egy Archive Select Op timal Agen ticGE O poor good Rewriter Rewriter R e writt en Pre f erenc e Rules or if re writ e yes no Figure 2: GEO v.s. AgenticGEO. Static GEO methods apply fixed rewriting heuristics, whereas AgenticGEO maintains an evolving strategy archive and a critic to adaptively retrieve high-scoring strategies for iterative rewriting.

**中文**

如图 2 所示，AgenticGEO 没有应用固定的重写启发式方法，而是维护一个不断发展的质量多样性 (QD) 档案作为外部存储器，保留高性能但多样化的策略。每个策略代表固定策略 GEO 评论家策略 存档 选择最佳代理 GEO 差好重写器 重写器 重写首选规则或如果重写 是 否 图 2：GEO 与代理GEO。静态 GEO 方法应用固定的重写启发法，而 AgenticGEO 维护不断发展的策略档案和批评家，以自适应地检索高分策略以进行迭代重写。

### 段落 17 · Page 2

**EN**

a distinct way to rewrite content under different structural, stylistic, or semantic preferences. AgenticGEO further introduces a coevolving critic to support agentic decision making. The critic serves as a surrogate evaluator and a planner. It identifies content-specific weaknesses, selects suitable strategies from the archive, and guides multi-step rewrites. By retrieving strategies from an evolved archive rather than relying on a fixed archive, AgenticGEO adapts naturally to diverse content and changing generative engine behaviors, addressing Challenge (i).

**中文**

在不同的结构、风格或语义偏好下重写内容的独特方式。 AgenticGEO 进一步引入了共同进化批评家来支持代理决策。批评家充当替代评估者和计划者。它可以识别特定于内容的弱点，从档案中选择合适的策略，并指导多步骤重写。通过从进化的档案中检索策略而不是依赖于固定的档案，AgenticGEO 可以自然地适应不同的内容并改变生成式引擎的行为，从而解决挑战 (i)。

### 段落 18 · Page 2

**EN**

To reduce reliance on intensive generative engine feedback, the critic is first calibrated using limited real feedback and then updated through continuous self-refinement. Once trained, it approximates generative engine preferences and provides stable guidance for strategy selection and rewrite execution. This design allows AgenticGEO to optimize visibility with substantially fewer feedback queries, addressing Challenge (ii). Our analysis suggests archive-driven co-evolution admits a sublinear regret bound 𝑂( √ 𝑇) .

**中文**

为了减少对密集生成式引擎反馈的依赖，批评家首先使用有限的真实反馈进行校准，然后通过不断的自我完善进行更新。经过训练后，它会近似生成式引擎的偏好，并为策略选择和重写执行提供稳定的指导。这种设计使 AgenticGEO 能够通过大幅减少反馈查询来优化可见性，从而解决挑战 (ii)。我们的分析表明，档案驱动的共同进化承认亚线性遗憾界限 𝑂( √ 𝑇)。

### 段落 19 · Page 2

**EN**

Empirically, AgenticGEO achieves the best optimization performance over 14 baselines on various benchmark datasets and generative engines (46.4%average gains. Moreover, AgenticGEO manages to preserve98 .1%performance using only41 .2%sparse GE feedback for optimization, indicating that the evolving critic substantially reduces supervision reliance. Our contributions are summarized as follows: • Content-conditioned GEO formulation:Notably, we are the first to formulate GEO as acontent-conditionedoptimization problem under non-stationary black-box generative engines, where different contents can favor different rewriting strategies.

**中文**

根据经验，AgenticGEO 在各种基准数据集和生成式引擎上的 14 个基线上实现了最佳优化性能（平均增益 46.4%）。此外，AgenticGEO 仅使用 41 .2% 稀疏 GE 反馈进行优化，设法保持 98 .1% 性能，表明不断发展的批评者大大减少了监督依赖。我们的贡献总结如下： • 内容条件 GEO 公式：值得注意的是，我们是第一个将 GEO 公式公式为非平稳黑盒生成式引擎下的内容条件优化问题，其中不同的内容有利于不同的重写策略。

### 段落 20 · Page 2

**EN**

• Co-evolving strategy memory and surrogate critic:We propose an agentic system that co-evolves a Quality-Diversity (QD) strategy archive as external memory and a lightweight surrogate critic that guides online exploration and inference-time multiturn planning, enabling continual adaptation. • Strong effectiveness and transfer:Extensive experiments show consistent improvements over baselines in-domain and strong transfer to unseen domains.

**中文**

• 共同进化策略记忆和代理批评家：我们提出了一种代理系统，该系统共同发展质量多样性（QD）策略档案作为外部记忆和指导在线探索和推理时间多轮规划的轻量级代理批评家，从而实现持续适应。 • 强大的有效性和转移性：广泛的实验表明，在域内基线上取得了一致的改进，并且向未知领域的转移性很强。

### 段落 21 · Page 2

**EN**

Further analyses provide convergence evidence, validate the necessity of core component, and confirm that the critic serves as a reliable proxy for the generative engine, reducing reliance on expensive GE feedback.

**中文**

进一步的分析提供了收敛证据，验证了核心组件的必要性，并确认批评家是生成式引擎的可靠代理，减少了对昂贵的 GE 反馈的依赖。

### Page 3

### 段落 22 · Page 3

**EN**

AgenticGEO: A Self-Evolving Agentic System for Generative Engine Optimization Conference acronym ’XX, June 03–05, 2018, Woodstock, NY 2 Related Work Generative Engine Optimization (GEO). Online content optimization has traditionally focused on Search Engine Optimization [2, 24, 45, 47], which improves a page’s position in ranked Search Engine Results Pages (SERPs) by optimizing for ranking factors. These factors typically combine retrieval-based relevance signals [31] and link-analysis signals (e.g., PageRank [ 5, 39]), together with classic on-page/off-page heuristics such as keywords, metadata, and backlinks [30, 43, 64].

**中文**

AgenticGEO：用于生成式引擎优化的自我进化代理系统会议缩写’XX，2018 年 6 月 3-05 日，纽约州伍德斯托克 2 相关工作生成式引擎优化 (GEO)。在线内容优化传统上侧重于搜索引擎优化 [2,24,45,47]，它通过优化排名因素来提高页面在排名搜索引擎结果页面 (SERP) 中的位置。这些因素通常结合基于检索的相关性信号 [31] 和链接分析信号（例如 PageRank [5, 39]），以及经典的页内/页外启发式方法，例如关键字、元数据和反向链接 [30, 43, 64]。

### 段落 23 · Page 3

**EN**

With LLMs increasingly embedded into information access systems, user-facing search is shifting from ranked retrieval to retrieval-grounded answer synthesis in interactive, conversational settings [19, 25, 35]. In the era of generative search, Aggarwal et al. introduced Generative Engine Optimization and released GEO-Bench [1], reframing optimization as maximizing a source’s visibility within a generative engine’s synthesized response rather than competing for a rank position.

**中文**

随着法学硕士越来越多地嵌入到信息访问系统中，面向用户的搜索正在从排名检索转向交互式会话环境中基于检索的答案合成[19,25,35]。在生成搜索时代，Aggarwal 等人。引入了生成式引擎优化并发布了 GEO-Bench [1]，将优化重新定义为在生成式引擎的合成响应中最大化源的可见性，而不是竞争排名位置。

### 段落 24 · Page 3

**EN**

They show that lightweight rewriting edits (e.g., adding authoritative citations, inserting statistics, and crafting quotable statements) can substantially increase a source’s inclusion in GE outputs. Building on this direction, AutoGEO [54] distills engine preferences from LLM-generated explanations into rewriting rules, while RAID G-SEO [9] uses role-augmented intent inference and iterative reflection to guide intent-aligned rewriting. Despite these advances, GEO remains in a developing stage.

**中文**

他们表明，轻量级重写编辑（例如，添加权威引文、插入统计数据和制作可引用的陈述）可以大大增加来源在 GE 输出中的包含率。在此方向的基础上，AutoGEO [54] 将引擎偏好从 LLM 生成的解释中提炼为重写规则，而 RAID G-SEO [9] 使用角色增强意图推理和迭代反射来指导意图对齐重写。尽管取得了这些进展，GEO 仍处于发展阶段。

### 段落 25 · Page 3

**EN**

Most methods reduce GEO to LLM-based rewriting with fixed, handengineered prompts or static preference rules [1, 9, 54], which lack adaptability under black-box, dynamic engines and are sensitive to prompt formatting [44]. Moreover, a specific strategy’s effectiveness varies across domains and engines, yet existing methods rarely consider which rewriting strategy to apply based on the source content characteristics, limiting generalization and adaptation. Self-Evolving Agentic Systems.

**中文**

大多数方法通过固定的、手工设计的提示或静态偏好规则将 GEO 简化为基于 LLM 的重写[1,9,54]，这些规则在黑盒、动态引擎下缺乏适应性，并且对提示格式敏感[44]。此外，特定策略的有效性因领域和引擎而异，但现有方法很少考虑根据源内容特征应用哪种重写策略，限制了泛化和适应。自我进化代理系统。

### 段落 26 · Page 3

**EN**

Self-evolving agents operate as closed-loop optimizers over system inputs, architectures, and environmental feedback, emerging as a key paradigm [11, 17, 26, 28, 29, 48, 50, 52, 56]. Existing systems are broadly organized as: Policy Search. Early works reframe prompts as discrete, optimizable variables: APE [63] selects candidates via task-level scoring, while OPRO [55] iteratively proposes instructions based on prior scores. However, these approaches often overfit to fixed protocols and lack online adaptivity. Recent methods focus on inference-time adaptation.

**中文**

自进化代理作为系统输入、架构和环境反馈的闭环优化器运行，成为一种关键范例[11,17,26,28,29,48,50,52,56]。现有系统大致组织为： 策略搜索。早期的作品将提示重新构建为离散的、可优化的变量：APE [63] 通过任务级评分选择候选者，而 OPRO [55] 根据先前的分数迭代地提出指令。然而，这些方法往往过度适合固定协议并且缺乏在线适应性。最近的方法侧重于推理时间适应。

### 段落 27 · Page 3

**EN**

Self-Refine [29] and Reflexion [48] iterate generation and feedback to revise solutions [57]. While effective for local errors, they typically follow fixed heuristic loops rather than learning to evolve, risking local optima when the generative engine updates. Evolutionary Strategies. To mitigate local optima, population-based algorithms like EvoPrompt and Promptbreeder [ 12, 15] evolve prompts via LLM-based mutations and fitness selection. Beyond prompts, recent systems extend this to agentic workflows [53, 58– 60, 62].

**中文**

Self-Refine [29] 和 Reflexion [48] 迭代生成和反馈以修改解决方案 [57]。虽然对局部错误有效，但它们通常遵循固定的启发式循环，而不是学习进化，从而在生成式引擎更新时面临局部最优的风险。进化策略。为了缓解局部最优，基于群体的算法（例如 EvoPrompt 和 Promptbreeder [12, 15]）通过基于 LLM 的突变和适应度选择来进化提示。除了提示之外，最近的系统还将其扩展到代理工作流程 [53, 58–60, 62]。

### 段落 28 · Page 3

**EN**

This suggests that GEO requires a self-evolving architecture that updates task understanding and planning from black-box engine feedback, which remains under-explored. 3 Problem Formulation Black-box GEO setting. We formulate Generative Engine Optimization as an optimization problem from the perspective of a content creator interacting with a black-box generative engine (GE), denoted as E. Given a user query 𝑞∈ Q , the engine retrieves a candidate document set 𝐷𝑞 that includes the creator’s original content 𝑑.

**中文**

这表明 GEO 需要一种自我进化的架构，可以根据黑盒引擎反馈更新任务理解和规划，而这一点尚未得到充分探索。 3 问题表述 黑盒GEO 设置。我们从内容创建者与黑盒生成式引擎（GE）交互的角度将生成式引擎优化表述为优化问题，表示为 E。给定用户查询𝑞∈Q，引擎检索包含创建者的原始内容𝑑的候选文档集𝐷𝑞。

### 段落 29 · Page 3

**EN**

A rewriting strategy 𝑠∈ S is applied to a policy (e.g., an LLM) to produce an optimized version ˜𝑑: ˜𝑑=Rewrite(𝑑;𝑠, 𝑞).(1) By substituting 𝑑 with ˜𝑑, the updated candidate set e𝐷𝑞 =(𝐷 𝑞 \𝑑) ∪ { ˜𝑑}is processed byEto generate a synthesized responseA. Impression-based objective. The goal of the content creator is to identify an optimal strategy 𝑠∗ ∈𝑆 that maximizes the visibility of the optimized content ˜𝑑 within the generated response A. Let 𝑗★ denote the rank index of ˜𝑑 in e𝐷.

**中文**

将重写策略𝑠ε S应用于策略（例如LLM）以产生优化版本〜𝑑： 〜𝑑=Rewrite(𝑑;𝑠, 𝑞)。(1) 通过用〜𝑑替换𝑑，更新后的候选集e𝐷𝑞 =(𝐷 𝑞 \𝑑) ∪ { ∼𝑑} 由 E 处理以生成合成响应 A。基于印象的目标。内容创建者的目标是确定最佳策略𝑠* ε𝑆，以最大化生成的响应 A 中优化内容 𝑑 的可见性。令𝑗★ 表示 𝑑 在 e𝐷 中的排名索引。

### 段落 30 · Page 3

**EN**

Following the evaluation framework established in GEO-Bench [1], we quantify the visibility using impression metrics that measure the presence and prominence of ˜𝑑 inA. The optimization objective is formulated as: max 𝑠∈ S Score𝑗★ (𝑞, 𝑠),(2) where Score𝑗★ (·) represents a specific impression metric (e.g.,word, pos, oroverallimpression; see Appendix A.1.3 for definitions).

**中文**

遵循 GEO-Bench [1] 中建立的评估框架，我们使用衡量 𝑑 inA 的存在和突出程度的印象指标来量化可见性。优化目标表述为： max 𝑠∈ S Score𝑗★ (𝑞, 𝑠),(2) 其中 Score𝑗★ (·) 表示特定印象指标（例如，word、pos、或overallimpression；定义请参阅附录 A.1.3）。

### 段落 31 · Page 3

**EN**

4 AgenticGEO Methodology 4.1 Overview As Figure 3 shows, AgenticGEO proceeds in three stages: • Offline Critic Alignment:We warm-start a lightweight surrogatecriticusing offline preference pairs from the training dataset to approximate GE feedback, without costly online evaluations. • Online Co-Evolution:Through a co-evolutionary loop, we jointly train the MAP-Elites strategy archive and the critic module with the real GE interactions. • Agentic Multi-Turn Rewriting:At inference time, we perform agentic multi-step planning, where the critic orchestrates strategy selection, while the rewriter operates the chosen strategies to optimize content.

**中文**

4 AgenticGEO 方法 4.1 概述 如图 3 所示，AgenticGEO 分三个阶段进行： • 离线批评对齐：我们使用训练数据集中的离线偏好对来热启动轻量级代理批评，以近似 GE 反馈，无需昂贵的在线评估。 • 在线协同进化：通过协同进化循环，我们与真实的GE交互共同训练MAP-精英策略档案和评论家模块。 • 代理多轮重写：在推理时，我们执行代理多步骤规划，其中批评者协调策略选择，而重写者则操作所选策略来优化内容。

### 段落 32 · Page 3

**EN**

4.2 Offline Critic Preference Alignment To avoid the high latency of online interactions with the blackbox engine, we train a lightweightcriticto serve as a surrogate evaluator. This critic is aligned with offline engine feedback to learn strategy-conditioned preferences, enabling an efficient warm-start. Setup & Notation.Given a query 𝑞, a document 𝑑, and a rewriting strategy 𝑠∈ M 0 (see Appendix A.1.4), we denote the input context as 𝑥=(𝑞, 𝑑) . Each strategy 𝑠 is instantiated as a textual prompt template that instructs an LLM to rewrite source content𝑑.

**中文**

4.2 离线评论家偏好对齐 为了避免与黑盒引擎在线交互的高延迟，我们训练一个轻量级评论家作为代理评估器。该评论家与离线引擎反馈保持一致，以学习策略条件偏好，从而实现高效的热启动。设置和符号。给定一个查询 𝑞、一个文档 𝑑 和一个重写策略 𝑠∈ M 0 （参见附录 A.1.4），我们将输入上下文表示为 𝑥=(𝑞, 𝑑)。每个策略𝑠都被实例化为文本提示模板，指示法学硕士重写源内容𝑑。

### 段落 33 · Page 3

**EN**

Architecture & Context Encoding.We implement the critic using abackbone + value headstructure, denoted by C. We select a lightweight decoder-only Language Model (LM) as the backbone to leverage its inherent semantic reasoning capabilities, which are essential for capturing the complex dependencies between optimization strategies and the query-content context.

**中文**

架构和上下文编码。我们使用主干 + 值头部结构来实现批评家，用 C 表示。我们选择轻量级仅解码器语言模型（LM）作为主干，以利用其固有的语义推理功能，这对于捕获优化策略和查询内容上下文之间的复杂依赖关系至关重要。

### 段落 34 · Page 3

**EN**

Given context 𝑥 and strategy 𝑠, the backbone encodes their concatenation into a latent representation ℎ(𝑥, 𝑠) , which is projected by a two-layer MLP value head to a numerical score: ℎ(𝑥, 𝑠)=LM ( [𝑥;𝑠] ) ,C (𝑥, 𝑠)=MLP  ℎ(𝑥, 𝑠)  ,(3) where C (𝑥, 𝑠) is expected to predict the impression gain induced by applying strategy𝑠to context𝑥before feeding it into GE.

**中文**

给定上下文 𝑥 和策略 𝑠，主干网将它们的串联编码为潜在表示 ℎ(𝑥, 𝑠)，由两层 MLP 值头将其投影为数字分数： ℎ(𝑥, 𝑠)=LM ( [𝑥;𝑠] ) ,C (𝑥, 𝑠)=MLP ℎ(𝑥, 𝑠) ,(3) 其中 C (𝑥, 𝑠) 预计可以预测在将策略𝑠应用于上下文𝑥之前将其输入 GE 所带来的印象增益。

### Page 4

### 段落 35 · Page 4

**EN**

Conference acronym ’XX, June 03–05, 2018, Woodstock, NY Jiaqi Yuan, Jialu Wang et al. 1. Oﬃne Alignmen t R e writ er GE (Eq.5) Initializ e 2. Online Co-E v olution Pre f erenc e P airs GE Strat egy Con t en t E v olver Critic c alculat e gains A WR R e ward (Eq.10) 3.Inf erenc e Hybrid Objective Critic Critic Updat e clarif y k e y poin ts + add attribution ne w f eedbackUpdat e clarif y k e y poin ts clarif y ... add ... Critic clarif y k e y poin ts add s t atis tics add s t atis tics clarif y k e y poin ts ＞ ＞ Con t en t This bottle is easy to use. It has a lid and you can take it anywhere . Critic clarif y ... add ... dele t e...

**中文**

会议缩写’XX，2018 年 6 月 3-05 日，纽约州伍德斯托克，Jiaqi Yuan、Jialu Wang 等人。 1. 线对齐重写 GE (Eq.5) 初始化 2. 在线协同进化偏好对 GE 策略内容 Ev olver Critic 计算收益 AWR 奖励 (Eq.10) 3. 推理混合 Objective Critic Critic 更新澄清关键点 + 添加属性 新反馈更新 澄清关键点 澄清...添加...批评 澄清关键点 添加统计 添加统计 澄清关键点 ＞ ＞ 内容 这个瓶子很容易使用。它有一个盖子，您可以将它带到任何地方。批评家澄清...添加...删除...

### 段落 36 · Page 4

**EN**

Archive Rewriter This bottle is light and easy to carry. It holds 750 ml and weighs about 200 g... GE Con t en t Con t en t This bottle is easy to use. It has a lid and you can take it anywhere .... E v olver R egre t Bound Critic Generaliz ation Bound (Lemma A .2) (Theorem A .4) Figure 3: Overview of the AgenticGEO framework with two-stage training. Offline Alignment warm-starts a surrogate critic using offline preference pairs from the initial archive M0, calibrating it for fast, content-conditioned strategy scoring.

**中文**

Archive Rewriter 此瓶子重量轻且易于携带。它可容纳 750 毫升，重约 200 克... GE 内容 内容 该瓶子易于使用。它有一个盖子，你可以把它带到任何地方...... E v olver Regre t Bound Critic Generalization Bound (引理 A .2) (定理 A .4) 图 3：具有两阶段训练的 AgenticGEO 框架概述。离线对齐使用初始存档 M0 中的离线偏好对来热启动代理批评家，对其进行校准以实现快速、内容调节的策略评分。

### 段落 37 · Page 4

**EN**

Online Co-Evolution then interacts with the black-box Generative Engine (GE) to iteratively, simultaneously evolve a MAP-Elites quality-diversity archive and the critic. Parent strategies are mutated by a learned evolver trained with sibling-aware A WR, the critic screens candidates to reduce GE calls, and newly collected GE feedback is stored in a replay buffer to continually recalibrate the critic and update the archive through a value-novelty gate. At inference time, the evolved archive and critic enable agentic multi-turn rewriting by selecting and executing a content-adaptive plan of strategies.

**中文**

然后，在线共同进化与黑盒生成式引擎 (GE) 交互，以迭代方式同时进化 MAP-精英质量多样性档案和评论家。父母策略由一个有兄弟意识的 A WR 训练的学习进化者进行变异，批评者筛选候选人以减少 GE 呼叫，新收集的 GE 反馈存储在重放缓冲区中，以不断重新校准批评者并通过价值新颖性门更新档案。在推理时，进化的档案和评论家通过选择和执行内容自适应策略计划来实现代理多轮重写。

### 段落 38 · Page 4

**EN**

Offline Supervision Data Construction.We construct offline supervision from the seed strategy pool M0 (illustrated at Appendix A.1.4). For each context 𝑥 and strategy 𝑠, we define the supervised gain as the improvement over the unrewritten baseline: 𝑟 sup (𝑥, 𝑠)=Score  Atrain 𝑠  −Score  Atrain 0  ,(4) where Atrain 𝑠 denotes the generative engine output after applying strategy 𝑠 to 𝑥, and Atrain 0 is the corresponding unrewritten baseline output. Score(·) is theoverallimpression metric defined in Appendix A.1.3, combiningWordandPos. We use 𝑟 sup (𝑥, 𝑠) as the offline alignment target for the critic outputC (𝑥, 𝑠).

**中文**

离线监督数据构建。我们从种子策略池M0（如附录A.1.4所示）构建离线监督。对于每个上下文 𝑥 和策略 𝑠，我们将监督增益定义为相对于未重写基线的改进： 𝑟 sep (𝑥, 𝑠)=Score Atrain 𝑠 -Score Atrain 0 ,(4) 其中 Atrain 𝑠 表示将策略 𝑠 应用于 𝑥 后的生成式引擎输出，Atrain 0 是相应的未重写基线输出。 Score(·)是附录A.1.3中定义的总体印象度量，结合了Word和Pos。我们使用𝑟sup（𝑥，𝑠）作为批评者输出C（𝑥，𝑠）的离线对齐目标。

### 段落 39 · Page 4

**EN**

Hybrid Objective.Effective preference alignment requires capturing both theabsolute valueand therelative orderof strategies. We propose a hybrid objective combining regression and ranking: Ltotal =L pair +𝜆L reg.(5) (1) Score Regression:We use the Huber loss [ 18] to regress C (𝑥, 𝑠) onto 𝑟 sup (𝑥, 𝑠) , which is less sensitive to noisy supervision: Lreg =E (𝑥,𝑠) h Huber C (𝑥, 𝑠), 𝑟 sup (𝑥, 𝑠)i .(6) (2) Rank-Aware Pairwise Alignment:While regression calibrates the value scale, downstream strategy selection primarily depends on relative ordering.

**中文**

混合目标。有效的偏好调整需要捕获策略的绝对价值和相对顺序。我们提出了一个结合回归和排名的混合目标：Ltotal=Lpair+𝜆Lreg.（5）（1）分数回归：我们使用Huber损失[18]将C（𝑥，𝑠）回归到𝑟sup（𝑥，𝑠），这对噪声监督不太敏感：Lreg=E（𝑥，𝑠）h Huber C（𝑥，𝑥， 𝑠), 𝑟 sep (𝑥, 𝑠) i .(6) (2) Rank-Aware Pairwise Alignment：虽然回归校准了价值尺度，但下游策略选择主要取决于相对顺序。

### 段落 40 · Page 4

**EN**

We therefore construct pairwise strategy preferences within the same context: for each 𝑥, we rank strategies in M0 by 𝑟 sup (𝑥, 𝑠) (rank1is best), and sample ordered pairs (𝑠+, 𝑠−) such that 𝑟 sup (𝑥, 𝑠 +)>𝑟 sup (𝑥, 𝑠 −).

**中文**

因此，我们在相同的上下文中构建成对策略偏好：对于每个 𝑥，我们按 𝑟 sep (𝑥, 𝑠) 对 M0 中的策略进行排名（rank1 最好），并采样有序对 (𝑠+, 𝑠−)，使得 𝑟 sep (𝑥, 𝑠 +)>𝑟 sep (𝑥, 𝑠 -)。

### 段落 41 · Page 4

**EN**

Since accurate discrimination among top strategies is most important for strategy selection, we assign larger weights to pairs involving higher-ranked strategies: 𝑤(𝑠 +, 𝑠−)= 1 rank𝑥 (𝑠+) +rank 𝑥 (𝑠 −) .(7) The weighted pairwise loss emphasizes the most promising strategies for reliable selection: Lpair =E (𝑥,𝑠 +,𝑠− ) h 𝑤(𝑠 +, 𝑠−) ·log  1+𝑒 − ( C (𝑥,𝑠+ ) − C (𝑥,𝑠− ) ) i .(8) Staged Training Strategy.To further stabilize alignment, we employ a two-phase process. We primarily sampleTop-5dense pairs to refine fine-grained local ordering, andglobal contrastive pairs to ensure coarse separation.

**中文**

由于顶级策略之间的准确区分对于策略选择最为重要，因此我们为涉及排名较高的策略对分配较大的权重：𝑤(𝑠 +, 𝑠−)= 1rank𝑥 (𝑠+) +rank 𝑥 (𝑠−)。(7) 加权成对损失强调最有希望进行可靠选择的策略：Lpair =E (𝑥,𝑠 +,𝑠−) ) h 𝑤(𝑠 +, 𝑠−) ·log 1+𝑒 − ( C (𝑥,𝑠+ ) − C (𝑥,𝑠− ) ) i .(8) 分阶段训练策略。为了进一步稳定对齐，我们采用两阶段过程。我们主要对 Top-5 密集对进行采样以细化细粒度的局部排序，并对全局对比对进行采样以确保粗分离。

### 段落 42 · Page 4

**EN**

We initially freeze the backbone to warm up the value head, preventing representation collapse, before unfreezing all parameters for joint fine-tuning. 4.3 Online Strategy-Critic Co-Evolution While offline alignment initializes the system, relying on static strategies risks local optima and fails to adapt to dynamic search environments. To enable continuous adaptation, we introduce an Online Strategy–Critic Co-Evolutionframework.

**中文**

我们首先冻结主干以预热值头，防止表示崩溃，然后解冻所有参数以进行联合微调。 4.3 在线策略-批评家共同进化虽然离线对齐初始化了系统，但依赖静态策略会面临局部最优的风险，并且无法适应动态搜索环境。为了实现持续适应，我们引入了在线策略-评论家共同进化框架。

### 段落 43 · Page 4

**EN**

This establishes a self-evolving loop where theEvolver( 𝐸), a parameterized LLM that generates strategy mutations, actively expands the strategy space to discover novel ones, while theCritic(C) continuously recalibrates to guide exploration and enable optimal strategy selection at inference. 4.3.1 Structured Evolution via MAP-Elites Archive.To prevent the optimizer from collapsing into a single “safe” pattern (e.g., always using an authoritative tone) that fails on diverse content, we maintain a dynamicMAP-Elites Archive M [21, 33, 41].

**中文**

这建立了一个自我进化的循环，其中 theEvolver(𝐸)（一种生成策略突变的参数化 LLM）主动扩展策略空间以发现新策略，而 theCritic(C) 不断重新校准以指导探索并在推理时实现最佳策略选择。 4.3.1 通过 MAP-Elites Archive 进行结构化进化。为了防止优化器陷入在不同内容上失败的单一“安全”模式（例如，始终使用权威语气），我们维护一个动态 MAP-Elites Archive M [21,33,41]。

### 段落 44 · Page 4

**EN**

Instead of seeking one global optimum, this archive acts as an evolving memory that preserves a wide range of high-performing strategies. Unlike a standard top-𝑘 list that discards lower-scoring but distinct solutions, M organizes strategies into a multi-dimensional grid ofbehavioral cells. Each cell represents a specific combination

**中文**

该档案不是寻求一个全局最优值，而是作为一个不断发展的记忆，保存了广泛的高性能策略。与丢弃得分较低但不同的解决方案的标准 top-𝑘 列表不同，M 将策略组织到行为单元的多维网格中。每个单元格代表一个特定的组合

### Page 5

### 段落 45 · Page 5

**EN**

AgenticGEO: A Self-Evolving Agentic System for Generative Engine Optimization Conference acronym ’XX, June 03–05, 2018, Woodstock, NY Table 1: Structure of the evolving strategy representation. Each dimension is mutated independently. It can be rendered into a compact summary for critic scoring and a full strategy prompt for rewriting (see Appendix A.1.5). Dimension Semantics & Examples Instruction Defines goal and scope (e.g., target audience, core facts, key emphasis, expert role). Constraints Sets strict boundaries (e.g., word count, citation checks, anti-hallucination, fact consistency).

**中文**

AgenticGEO：用于生成式引擎优化的自我进化代理系统会议缩写’XX，2018 年 6 月 3 日至 5 日，纽约州伍德斯托克表 1：进化策略表示的结构。每个维度都是独立变异的。它可以呈现为评论家评分的紧凑摘要和重写的完整策略提示（参见附录 A.1.5）。维度语义和示例说明定义目标和范围（例如目标受众、核心事实、重点、专家角色）。约束 设定严格的界限（例如字数统计、引文检查、反幻觉、事实一致性）。

### 段落 46 · Page 5

**EN**

Reasoning Adds logic steps (e.g., conflict resolution, selfcorrection, step planning, logic verification). Format Controls output layout (e.g., bullet lists, code blocks, output schema, section preludes). Tone Adjusts writing style (e.g., assertive voice, technicality, simple language, formality level). of attributes (see Table 1), such as an Assertive tone combined with a List format, ensuring that unique strategy styles compete only against similar ones.

**中文**

推理添加逻辑步骤（例如，冲突解决、自我纠正、步骤规划、逻辑验证）。格式 控制输出布局（例如，项目符号列表、代码块、输出模式、章节前奏）。语气 调整写作风格（例如，自信的语气、专业性、简单的语言、正式程度）。属性（参见表 1），例如与列表格式相结合的自信语气，确保独特的策略风格仅与类似的策略风格竞争。

### 段落 47 · Page 5

**EN**

A new strategy 𝑠 captures a cell only if it triggers theValue-Novelty Gate(details in Appendix A.1.6): (1) Value:It achieves a higher impression score from the Generative Engine than the current elite in that cell; (2) Novelty:It is structurally distinct from existing entries (measured by 𝑛-gram distance [6]), expanding the archive’s coverage even if its score is currently lower.

**中文**

新策略𝑠仅在触发价值新颖性门时捕获一个单元格（详细信息参见附录A.1.6）：（1）价值：它从生成式引擎中获得比该单元格中当前精英更高的印象分数； (2)新颖性：它在结构上与现有条目不同（通过𝑛-克距离[6]衡量），扩大了档案的覆盖范围，即使其分数目前较低。

### 段落 48 · Page 5

**EN**

To manage archive capacity and support evolution exploration, we assign each retained strategy a compositePND Score(Pareto- Novelty-Diversity) [10, 23]: 𝑆PND (𝑠)=𝑟(𝑠) +𝜆 pnd · Nov(𝑠) +Div(𝑠) ,(9) where 𝑟(𝑠) is the impression score from the critic or generative engine, and Nov(𝑠) and Div(𝑠) measure structural uniqueness and lineage diversity (see Appendix A.1.7). This score serves two roles: Global Pruningto discard redundant strategies when the archive is full, and adense intrinsic rewardfor the Evolver (Eq. 10) to encourage exploration beyond pure exploitation.

**中文**

为了管理存档容量并支持进化探索，我们为每个保留策略分配一个复合PND分数（Pareto-Novelty-Diversity）[10, 23]： 𝑆PND (𝑠)=𝑟(𝑠) +𝜆 pnd · Nov(𝑠) +Div(𝑠) ,(9) 其中𝑟(𝑠)是评论家或生成者的印象分数engine、Nov(𝑠) 和 Div(𝑠) 测量结构独特性和谱系多样性（参见附录 A.1.7）。该分数有两个作用：全局修剪，当档案已满时丢弃冗余策略，并为 Evolver（方程 10）增加内在奖励，以鼓励超越纯粹利用的探索。

### 段落 49 · Page 5

**EN**

4.3.2 The Co-Evolutionary Loop.With the diverse population anchored by the Archive, the online process drives aco-evolutionary loopwhere the Evolver and Critic mutually refine their capabilities through four phases per iteration (shown in Algorithm 1): 1. Generation:Parents sampled from M undergo hybrid mutation. The evolver 𝐸 selects an operator from our predefined catalog and generates the resulting child_genotype (e.g., applying mut_F_schema_swap to change the output format), while symbolic Operators inject hard perturbations via field-level mutations (e.g.,mut_T_toggle_tone for style switching, ormut_C_strengthenfor constraint injection).

**中文**

4.3.2 协同进化循环。随着档案锚定的多样化种群，在线过程驱动了一个协同进化循环，其中进化者和批评者通过每次迭代的四个阶段相互完善其能力（如算法 1 所示）： 1. 生成：从 M 中采样的父母经历混合突变。进化者𝐸从我们预定义的目录中选择一个运算符并生成结果child_genotype（例如，应用mut_F_schema_swap来更改输出格式），而符号运算符通过字段级突变注入硬扰动（例如，用于样式切换的mut_T_toggle_tone，或用于约束注入的mut_C_strengthen）。

### 段落 50 · Page 5

**EN**

Details in Appendix A.1.8. 2. Screening:To reduce computational cost, theCritic C filters candidates, selecting the Top-𝐾top strategies for exploitation and a random 𝐾rand subset for exploration to mitigate selection bias. 3. Evaluation:The Generative Engine evaluates the selected candidates.

**中文**

详细信息参见附录 A.1.8。 2. 筛选：为了降低计算成本，Critic C 筛选候选者，选择 Top-𝐾top 策略进行开发，并选择随机 𝐾rand 子集进行探索，以减轻选择偏差。 3. 评估：生成式引擎对选定的候选者进行评估。

### 段落 51 · Page 5

**EN**

The resulting GE feedback, together with the critic scores for the remaining candidates, is merged into a joint reward signal to update the archive via the Value-Novelty gate, and all Algorithm 1Archive-Driven Strategy-Critic Co-Evolution Require: Initial archive M0; data distribution D over content; evolver 𝐸; critic C; generative engine GE; online iterations 𝑇 ; exploit size𝐾 top; explore size𝐾 rand. 1:M ← M 0 2:Initialize replay buffersB true ← ∅,B pred ← ∅ 3:for𝑡=1, . . .

**中文**

由此产生的 GE 反馈与剩余候选者的评论家分数一起合并为联合奖励信号，以通过价值新颖性门更新档案，并且所有算法 1 档案驱动策略-评论家共同进化要求：初始档案 M0；内容上的数据分布 D；进化者𝐸;评论家C；发电发动机GE；在线迭代 𝑇；利用大小𝐾 顶部；探索大小𝐾 兰特。 1:M ← M 0 2:初始化重播缓冲区B true ← ∅,B pred ← ∅ 3:for𝑡=1, .。。

### 段落 52 · Page 5

**EN**

, 𝑇do 4:𝑥∼ D⊲e.g.,(𝑞, 𝑑) 5:Phase 1: Hybrid Candidate Generation 6:𝑃←Sample(M 𝑡 ) 7:𝑆 evolver ← {𝑠|𝑠∼𝐸(· |𝑠 𝑝 ), 𝑠 𝑝 ∈𝑃}⊲neural mutation 8:𝑆 ops ← {Mutate(𝑠 𝑝 ) |𝑠 𝑝 ∈𝑃}⊲symbolic perturbation 9:𝑆 cand ←𝑆 evolver ∪𝑆 ops 10:Phase 2: Critic Scoring & Budgeted Selection 11:𝑅 critic (𝑠) ← C (𝑥, 𝑠),∀𝑠∈𝑆 cand 12:𝑆 eval ←TopK(𝑆 cand, 𝑅critic, 𝐾top) ∪Random(𝑆 cand, 𝐾rand) 13:Phase 3: GE Evaluation & Joint Reward Aggregation 14:𝑅 true (𝑠) ←GE(𝑥, 𝑠),∀𝑠∈𝑆 eval 15:𝑅 mix (𝑠) ← ( 𝑅true (𝑠), 𝑠∈𝑆 eval, 𝑅critic (𝑠), 𝑠∈𝑆 cand \𝑆 eval.

**中文**

, 𝑇do 4:𝑥∼ D⊲例如,(𝑞, 𝑑) 5: 第 1 阶段：混合候选生成 6:𝑃←样本(M 𝑡 ) 7:𝑆 进化者 ← {𝑠|𝑠∼𝐸(· |𝑠 𝑝 ), 𝑠 𝑝 ε𝑃}⊲神经突变 8：𝑆 ops ← {Mutate(𝑠 𝑝 ) |𝑠 𝑝 ε𝑃}⊲符号扰动 9：𝑆 cand ←𝑆 进化器 ∪𝑆 ops 10：第 2 阶段：批评评分和预算选择11:𝑅批评者 (𝑠) ← C (𝑥, 𝑠),∀𝑠ε𝑆 cand 12:𝑆 eval ←TopK(𝑆 cand, 𝑅critic, 𝐾top) ∪Random(𝑆 cand, 𝐾rand) 13:阶段 3: GE 评估与联合奖励聚合 14:𝑅 true (𝑠) ←GE(𝑥, 𝑠),∀𝑠ε𝑆 eval 15:𝑅 mix (𝑠) ← ( 𝑅true (𝑠), 𝑠ε𝑆 eval, 𝑅critic (𝑠), 𝑠ε𝑆可以\𝑆评估。

### 段落 53 · Page 5

**EN**

16:M 𝑡+1 ←UpdateArchive(M 𝑡 , 𝑆cand, 𝑅mix) 17:B true ← Btrue ∪ {(𝑥, 𝑠, 𝑅 true (𝑠)) |𝑠∈𝑆 eval} 18:B pred ← Bpred ∪ {(𝑥, 𝑠, 𝑅 mix (𝑠)) |𝑠∈𝑆 cand \𝑆 eval} 19:Phase 4: Online Updates 20:𝐸 𝑡+1 ←TrainEvolver(𝐸 𝑡 ,B true ∪ Bpred) 21:C 𝑡+1 ←TrainCritic(C 𝑡,B true) 22:end for 23:returnEvolved archiveM, evolved criticC experiences are logged into the replay buffers Btrue and Bpred for subsequent online updates. 4. Learning:The replay buffers drive online updates of the evolver 𝐸 and recalibration of the critic 𝐶.

**中文**

16:M 𝑡+1 ←UpdateArchive(M 𝑡 , 𝑆cand, 𝑅mix) 17:B true ← Btrue ∪ {(𝑥, 𝑠, 𝑅 true (𝑠)) |𝑠ε𝑆 eval} 18:B pred ← Bpred ∪ {(𝑥, 𝑠, 𝑅 mix (𝑠)) |𝑠ε𝑆 cand \𝑆 eval} 19:第 4 阶段：在线更新 20:𝐸 𝑡+1 ←TrainEvolver(𝐸 𝑡 ,B true ∪ Bpred) 21:C 𝑡+1 ←TrainCritic(C 𝑡,B true) 22:end for 23:returnEvolved archiveM，进化后的criticC经验被记录到重播缓冲区Btrue和Bpred中以供后续在线更新。 4. 学习：重放缓冲区驱动进化器𝐸的在线更新和批评者𝐶的重新校准。

### 段落 54 · Page 5

**EN**

𝐸 is trained on both Btrue and Bpred, while 𝐶 is updated only with GE-labeled samples in Btrue, enabling continual adaptation as the strategy population evolves. 4.3.3 Evolver Optimization via Sibling-A ware A WR.The Evolver 𝐸 synthesizes a candidate strategy 𝑠new from a parent 𝑠𝑝 (or a parent pair) by selecting optimal mutation or crossover operators. A naive Reinforcement Learning approach is unstable due to the high variance of impression scores from the Generative Engine. We instead employAdvantage-Weighted Regression (A WR). Inspired by GRPO-style relative advantage calculation [46], we further stabilize learning under noisy feedback.

**中文**

𝐸 在 Btrue 和 Bpred 上进行训练，而 𝐶 仅使用 Btrue 中带有 GE 标记的样本进行更新，从而随着策略群体的发展而不断适应。 4.3.3 通过 Sibling-A ware A WR 进行进化器优化。进化器𝐸通过选择最佳突变或交叉算子，从父𝑠𝑝（或父对）合成候选策略𝑠new。由于生成式引擎的印象分数差异很大，简单的强化学习方法是不稳定的。相反，我们采用优势加权回归（A WR）。受GRPO式相对优势计算[46]的启发，我们进一步稳定了噪声反馈下的学习。

### 段落 55 · Page 5

**EN**

Crucially, to mitigate noise across heterogeneous content contexts (where some source material is inherently harder to optimize), we propose a Sibling-A ware Advantage. Instead of comparing rewards globally, we compare a candidate’s performance relative to its “siblings” generated from the same parent strategy: 𝐴𝑖 =(𝑟 𝑖 −𝑟 parent) | {z } Absolute Gain −𝛼sib ·mean {Δ 𝑗 } 𝑗∈siblings  +I(Δ 𝑖 <0) ·𝑆 PND (𝑠𝑖 ), (10) where 𝑟 denotes the score from the critic and generative engine, Δ𝑖 =𝑟 𝑖 −𝑟 parent, and 𝑆PND (𝑠𝑖 ) is the exploration bonus (Eq. 22). The sibling mean provides a within-parent baseline, so 𝐴𝑖 better

**中文**

至关重要的是，为了减少异构内容上下文中的噪音（其中某些源材料本质上更难优化），我们提出了 Sibling-A ware Advantage。我们不是在全球范围内比较奖励，而是比较候选者相对于同一父策略生成的“兄弟姐妹”的表现： {z } 绝对增益 −𝛼sib ·mean {Δ 𝑗 } 𝑗∈siblings +I(Δ 𝑖 <0) ·𝑆 PND (𝑠𝑖 ), (10) 其中 𝑟 表示来自批评者和生成式引擎的分数， Δ𝑖 = 𝑟 𝑖 −𝑟 父母，并且𝑆PND (𝑠𝑖) 是探索奖励（等式 22）。同级均值提供了父级内基线，因此𝐴𝑖 更好

### Page 6

### 段落 56 · Page 6

**EN**

Conference acronym ’XX, June 03–05, 2018, Woodstock, NY Jiaqi Yuan, Jialu Wang et al. reflects the effect of the chosen evolution operator rather than the intrinsic difficulty of the content. The last term adds an exploration bonus when the immediate gain is non-positive, helping retain novel and diverse strategies.

**中文**

会议缩写’XX，2018 年 6 月 3-05 日，纽约州伍德斯托克，Jiaqi Yuan、Jialu Wang 等人。反映了所选进化算子的效果，而不是内容的内在难度。当直接收益为非正值时，最后一项会增加探索奖励，有助于保留新颖且多样化的策略。

### 段落 57 · Page 6

**EN**

The policy is then updated to imitate these high-advantage actions through weighted supervised finetuning (SFT) [38], minimizing the following loss: LEvolver =−E (𝑥,𝑠)∼( B true∪Bpred )  exp  𝐴(𝑥, 𝑠) 𝛽  ·log𝐸(𝑠|𝑥)  .(11) 4.3.4 Online Critic Calibration.Complementing the Evolver updates, we continuously recalibrate the critic C using new labeled triplets (𝑥, 𝑠, 𝑟) collected in the replay buffer Btrue. By optimizing the hybrid objective in Eq. 5, we keep the critic calibrated under the evolving archive and feedback distribution, enabling reliable scoring for online selection and inference-time agentic planning. 4.4 Theoretical analysis.

**中文**

然后更新策略，通过加权监督微调（SFT）[38]来模仿这些高优势动作，最小化以下损失：LEvolver =−E (𝑥,𝑠)∼( B true∪Bpred ) exp 𝐴(𝑥, 𝑠) 𝛽 ·log𝐸(𝑠|𝑥) .(11) 4.3.4 在线批评家校准。作为 Evolver 更新的补充，我们使用重播缓冲区 Btrue 中收集的新标记三元组（𝑥、𝑠、𝑟）不断重新校准批评家 C。通过优化方程式中的混合目标。 5、我们在不断变化的档案和反馈分布下保持批评家的校准，从而为在线选择和推理时间代理规划提供可靠的评分。 4.4 理论分析。

### 段落 58 · Page 6

**EN**

Let R (𝑠) denote the risk induced by the strategy 𝑠. The regret of the proposed critic-evolver co-evolutionary algorithm is analyzed in Theorem 4.1. Theorem 4.1 (Informal).Under the conditions of a linearly growing replay buffer and a Lipschitz-continuous critic, the AgenticGEO framework achieves a cumulative regret: 𝑇∑︁ 𝑡=1 R (𝑠𝑡 ) − R (𝑠 ∗)=O ( √ 𝑇). Proof Sketch. We first decompose the instantaneous risk gap at each time step𝑡as R (𝑠𝑡 )−R (𝑠∗) ≤ |R (𝑠 𝑡 )−C𝑡 (𝑠𝑡 )|+|C 𝑡 (𝑠𝑡 )−C𝑡 (𝑠∗)|+|C 𝑡 (𝑠∗)−R (𝑠∗)|.

**中文**

令 R (𝑠) 表示策略 𝑠 引起的风险。定理 4.1 中分析了所提出的批评者-进化者协同进化算法的遗憾。定理 4.1（非正式）。在线性增长的重播缓冲区和 Lipschitz 连续批评家的条件下，AgenticGEO 框架实现了累积遗憾：𝑇Σ︁ 𝑡=1 R (𝑠𝑡 ) − R (𝑠 *)=O ( √ 𝑇)。证明草图。我们首先将每个时间步的瞬时风险差距分解为 R (𝑠𝑡 )−R (𝑠*) ≤ |R (𝑠 𝑡 )−C𝑡 (𝑠𝑡 )|+|C 𝑡 (𝑠𝑡 )−C𝑡 (𝑠*)|+|C 𝑡 (𝑠*)−R (𝑠*)|。

### 段落 59 · Page 6

**EN**

Given a replay buffer that grows linearly, the approximation and generalization errors of the critic model satisfy |R (𝑠) − C 𝑡 (𝑠)|= O ( 1√𝑡 ). The evolver’s selection process follows standard online learning bound by |C𝑡 (𝑠𝑡 ) − C 𝑡 (𝑠∗)|=O ( 1√𝑡 ). Combining above and summing over the time horizon 𝑇 , we can conclude that the cumulative regret is 𝑇∑︁ 𝑡=1 R (𝑠𝑡 ) − R (𝑠 ∗)= 𝑇∑︁ 𝑡=1 O ( 1√𝑡 )=O ( √ 𝑇). □ This implies that as the number of iterations 𝑇 increases, the average performance gap vanishes, guaranteeing that the system asymptotically converges to the optimal strategy.

**中文**

给定线性增长的重放缓冲区，批评模型的近似和泛化误差满足 |R (𝑠) − C 𝑡 (𝑠)|= O ( 1√𝑡 )。进化者的选择过程遵循标准在线学习，限制为 |C𝑡 (𝑠𝑡 ) − C 𝑡 (𝑠*)|=O ( 1√𝑡 )。结合以上内容并在时间范围 𝑇 上求和，我们可以得出累积遗憾为 𝑇Σ︁ 𝑡=1 R (𝑠𝑡 ) − R (𝑠 ∗)= 𝑇Σ︁ 𝑡=1 O ( 1√𝑡 )=O ( √ 𝑇)。 □ 这意味着随着迭代次数𝑇 的增加，平均性能差距消失，保证系统渐近收敛到最优策略。

### 段落 60 · Page 6

**EN**

More detailed theoretical analysis and the proofs are provided in Appendix A.3. 4.5 Agentic Multi-Turn Rewriting with Critic-Guided Planning The inference phase deploys the evolved archiveM andcritic C for multi-turn optimization. We formulate this as acontent-conditioned decision-makingprocess, where the critic serves as afast proxy planner. This allows the agent to guide a greedy search over the strategy space, enabling rapid evaluation while avoiding expensive black-box interactions.

**中文**

附录A.3提供了更详细的理论分析和证明。 4.5 具有 Critic 引导规划的代理多轮重写 推理阶段部署进化的 archiveM 和 Critic C 进行多轮优化。我们将其表述为一个以内容为条件的决策过程，其中批评者充当快速代理计划者。这使得代理能够引导策略空间上的贪婪搜索，从而实现快速评估，同时避免昂贵的黑盒交互。

### 段落 61 · Page 6

**EN**

At each step 𝜏 (initialized with 𝑑0 =𝑑 ), the agent plans the next optimal move by selecting a strategy 𝑠∗ 𝜏 that maximizes the critic’s predicted potential, while enforcing a Tabu ListT𝜏 (recording previously utilized strategies) to prevent repeated operations: 𝑠∗ 𝜏 =arg max 𝑠∈ M\T𝜏 C (𝑞, 𝑑𝜏 ), 𝑠.(12) Subsequently, the content state transitions via the rewriting tool, and the utilized strategy is recorded to update the constraint set: 𝑑𝜏+1 =Rewrite(𝑑 𝜏, 𝑠∗ 𝜏 , 𝑞),T 𝜏+1 ← T𝜏 ∪ {𝑠 ∗ 𝜏 }.(13) The loop terminates when the marginal gain vanishes: max 𝑠∈ M\T𝜏+1 C (𝑞, 𝑑𝜏+1 ), 𝑠 ≤max 𝑠∈ M\T𝜏 C (𝑞, 𝑑𝜏 ), 𝑠,(14) or steps exceed 𝑇𝑚𝑎𝑥 .

**中文**

在每一步 𝜏（用 𝑑0 =𝑑 初始化）中，智能体通过选择策略 𝑠* 𝜏 来规划下一个最佳移动，该策略可以最大化批评者的预测潜力，同时执行禁忌列表 T𝜏（记录之前使用的策略）以防止重复操作： 𝑠* 𝜏 =arg max 𝑠ε M\T𝜏 C (𝑞, 𝑑𝜏 ), 𝑠 .(12) 随后，通过重写工具进行内容状态转换，并记录所使用的策略以更新约束集： 𝑑𝜏+1 =Rewrite(𝑑 𝜏, 𝑠* 𝜏 , 𝑞),T 𝜏+1 ← T𝜏 ∪ {𝑠 ∗ 𝜏 }.(13) 当边际增益消失时，循环终止： max 𝑠ε M\T𝜏+1 C (𝑞, 𝑑𝜏+1 ), 𝑠 ≤max 𝑠ε M\T𝜏 C (𝑞, 𝑑𝜏 ), 𝑠 ,(14)或步数超过 𝑇𝑚𝑎𝑥。

### 段落 62 · Page 6

**EN**

This agentic planning capability allows AgenticGEO to dynamically adapt its optimization path based on the evolving characteristics of the content, yielding a highly optimized content that occupies a more prominent role within the engine’s information synthesis and attribution. 5 Experiments We empirically validate the effectiveness and generalization ability of AgenticGEO. We study the following research questions: RQ1 Overall Performance & Robustness:How does Agentic- GEO compare to state-of-the-art methods, and is its performance robust to generative engines varying in architecture and scale?

**中文**

这种代理规划功能使 AgenticGEO 能够根据内容的演变特征动态调整其优化路径，从而产生高度优化的内容，在引擎的信息合成和归因中占据更重要的作用。 5 实验我们通过实证验证了AgenticGEO 的有效性和泛化能力。我们研究以下研究问题： RQ1 整体性能和鲁棒性：Agentic-GEO 与最先进的方法相比如何，其性能对于不同架构和规模的生成式引擎是否鲁棒？

### 段落 63 · Page 6

**EN**

RQ2 Transferability to Unseen Domains:Can an optimization policy maintain performance when deployed on out-of-distribution domains? RQ3 Ablation and Hyperparameters Analysis:How does each co-evolutionary component influence the performance? Specifically, does the pre-trained critic provide a reliable warm-start? RQ4 Semantic Consistency:Does the optimization maintain the original meaning of the content, ensuring that visibility gains do not come at the cost of information loss? 5.1 Exprimental Setup We briefly introduce the experimental setup.

**中文**

RQ2 到未见过的域的可转移性：优化策略在部署到分布外域时能否保持性能？ RQ3消融和超参数分析：每个共同进化组件如何影响性能？具体来说，经过预先训练的批评家是否提供了可靠的热启动？ RQ4 语义一致性：优化是否保持了内容的原始含义，确保可见性的提高不会以信息丢失为代价？ 5.1 实验设置我们简要介绍实验设置。

### 段落 64 · Page 6

**EN**

• Dataset.GEO-Bench [ 1] serves as our training dataset, derived from Google Search results spanning a wide spectrum of domains and query difficulties. To assess zero-shot generalization to unseen distributions, we employ MS MARCO [37], comprising short-text passages from real-world Bing search logs, and a custom E-commerce [42] sourced from Amazon, representing a specific vertical for product search. Details are in Appendix A.2.1 • Settings.To conduct a comprehensive evaluation, we use GEO- Bench [1] training dataset for evolving the archive and critic, and extend the assessment to MS-Marco [37] and E-commerce [42] datasets.

**中文**

• Dataset.GEO-Bench [1] 作为我们的训练数据集，源自涵盖广泛领域和查询难度的 Google 搜索结果。为了评估对未见分布的零样本泛化，我们采用了 MS MARCO [37]，包括来自现实世界 Bing 搜索日志的短文本段落，以及来自亚马逊的自定义电子商务 [42]，代表产品搜索的特定垂直领域。详细信息参见附录A.2.1 • 设置。为了进行全面评估，我们使用GEO-Bench [1] 训练数据集来改进档案和评论家，并将评估扩展到MS-Marco [37] 和电子商务[42] 数据集。

### 段落 65 · Page 6

**EN**

This diverse benchmark allows us to examine the performance consistency across varying content distributions and verify its broad applicability in real-world scenarios. • Baselines.We group baselines into two categories: Static heuristics apply fixed rewriting heuristics:No optimization,Keyword Stuffing,Unique Words,Easy-To-Understand,Authoritative,Technical Words,Fluency Optimization,Cite Sources,Quotation Addition, Statistics Addition. Learning-based methods train models to generate optimized rewrites:AutoGEO,Cite Sources-SFT,Quotation Addition-SFT,Statistics Addition-SFT. Details are deferred to Appendix A.2.2.

**中文**

这种多样化的基准使我们能够检查不同内容分布之间的性能一致性，并验证其在现实场景中的广泛适用性。 • 基线。我们将基线分为两类： 静态启发式应用固定重写启发式：无优化、关键词堆砌、独特词语、易于理解、权威、技术词汇、流畅性优化、引用来源、引文添加、统计添加。基于学习的方法训练模型以生成优化重写：AutoGEO、引用来源-SFT、引用添加-SFT、统计添加-SFT。详细信息参见附录 A.2.2。

### Page 7

### 段落 66 · Page 7

**EN**

AgenticGEO: A Self-Evolving Agentic System for Generative Engine Optimization Conference acronym ’XX, June 03–05, 2018, Woodstock, NY • Models & Metrics.We employ Qwen2.5-32B-Instruct and Llama- 3.3-70B-Instruct as downstream generative engines [14, 51]. For system components, we implement the Critic backbone with Qwen2.5-1.5B, the Evolver with Qwen2.5-7B-Instruct, and the Rewriter with Qwen2.5-32B-Instruct for tool invocation. We measure performance viaAttributedWordCount,Position-Weighted Citation Order, and their Combination asoverall.

**中文**

AgenticGEO：用于生成式引擎优化的自我进化代理系统会议首字母缩略词’XX，2018年6月3日至5日，纽约州伍德斯托克•模型和指标。我们采用Qwen2.5-32B-Instruct和Llama-3.3-70B-Instruct作为下游生成式引擎[14, 51]。对于系统组件，我们使用 Qwen2.5-1.5B 实现 Critic 主干，使用 Qwen2.5-7B-Instruct 实现 Evolver，使用 Qwen2.5-32B-Instruct 实现重写器以进行工具调用。我们通过属性字数、位置加权引文顺序及其整体组合来衡量绩效。

### 段落 67 · Page 7

**EN**

[ 1] (Definition in Appendix A.1.3.) • Implementation.We employ LoRA [ 16] to fine-tune both the Critic and Evolver for 2 epochs. All experiments are implemented on 4 NVIDIA RTX Pro 6000 GPUs. At inference time, we select the top-25strategies from the evolved archive ranked by their 𝑆PND scores, and perform critic-guided multi-turn rewriting with a maximum of3rewrite steps. Other details in Appendix A.2. 5.2 Overall Performance and Robustness (RQ1). Table 2 presents the comparative results of AgenticGEO against all baselines on the in-domain GEO-Bench dataset.

**中文**

[1]（附录A.1.3中的定义。） • 实现。我们采用LoRA[16]对Critic和Evolver进行2个epoch的微调。所有实验均在 4 个 NVIDIA RTX Pro 6000 GPU 上实施。在推理时，我们从按 𝑆PND 分数排名的进化存档中选择前 25 个策略，并执行评论家引导的多轮重写，最多 3 个重写步骤。其他详细信息参见附录 A.2。 5.2 整体性能和稳健性（RQ1）。表 2 显示了 AgenticGEO 与域内 GEO-Bench 数据集上所有基线的比较结果。

### 段落 68 · Page 7

**EN**

We observe that AgenticGEO consistently achieves state-of-the-art performance on two generative engines, demonstrating strong effectiveness and robustness against engine variations in architecture and scale. On the Qwen2.5-32B-Instruct engine, AgenticGEO achieves an Overall score of 25.48, surpassing the strongest baseline (AutoGEO) which scores 23.71. This represents a substantial improvement over static heuristic strategies, such asKeyword Stuffing(20.69) and Authoritative(20.60), confirming that fixed rewriting rules are insufficient for the dynamic nature of generative engines.

**中文**

我们观察到，AgenticGEO 在两个生成式引擎上始终如一地实现了最先进的性能，展示了针对架构和规模的引擎变化的强大有效性和鲁棒性。在 Qwen2.5-32B-Instruct 引擎上，AgenticGEO 的总体得分为 25.48，超过了最强基线 (AutoGEO) 的得分 23.71。这代表了对静态启发式策略（例如关键字填充（20.69）和权威（20.60））的重大改进，证实固定重写规则不足以满足生成式引擎的动态性质。

### 段落 69 · Page 7

**EN**

Furthermore, our method outperforms the Supervised Fine-Tuning (SFT) baselines. This performance improvement indicates that our selfevolving strategy archive effectively transcends the optimization upper bound imposed by static strategies’ supervision, capturing content-centric patterns that are ignored by existing methods. AgenticGEO also demonstrates strong robustness on the larger Llama-3.3-70B-Instruct engine. While many baselines struggle to transfer their gains (e.g.,Statistics Additiondrops to 21.05), AgenticGEO maintains a strongest performance with Overall of 24.52.

**中文**

此外，我们的方法优于监督微调（SFT）基线。这种性能改进表明我们的自我进化策略存档有效地超越了静态策略监督所施加的优化上限，捕获了现有方法忽略的以内容为中心的模式。 AgenticGEO 还在较大的 Llama-3.3-70B-Instruct 引擎上展示了强大的鲁棒性。尽管许多基线都在努力转移其收益（例如，统计加数下降至 21.05），但 AgenticGEO 仍保持着最强劲的表现，总体得分为 24.52。

### 段落 70 · Page 7

**EN**

This consistency across different model architectures and scales validates that our co-evolving critic and strategy archive learn generalized optimization principles rather than overfitting to a specific engine, presenting the necessity of keeping strategy diverse. 5.3 Transferability to Unseen Domains (RQ2). To evaluate AgenticGEO’s cross-domain transferability, we test AgenticGEO on MS MARCO and E-Commerce without domainspecific fine-tuning. As shown in Table 3, our method exhibits strong robustness against domain shifts, whereas baselines suffer from significant performance degradation.

**中文**

不同模型架构和规模之间的一致性验证了我们的共同进化批评家和策略档案学习通用优化原则，而不是过度拟合特定引擎，这表明保持策略多样化的必要性。 5.3 向未见过的域的可转移性（RQ2）。为了评估 AgenticGEO 的跨域可转移性，我们在 MS MARCO 和电子商务上测试 AgenticGEO，无需进行特定域微调。如表 3 所示，我们的方法对域转移表现出很强的鲁棒性，而基线则遭受显着的性能下降。

### 段落 71 · Page 7

**EN**

On MS MARCO, AgenticGEO outperforms the strongest baseline, AutoGEO, by over 11% on both Qwen2.5-32B-Instruct and Llama3.3-70B-Instruct. And the advantage is even more dominant on the E-Commerce dataset. The transferability gains across two unseen domains support the claim that AgenticGEO avoids overfitting to specific content. The design of an evolving strategy archive and critic-guided planning yields a transferable optimization policy that remains effective under domain shift, showing strong domain generalization. Table 2: Overall Performance on the in-domain setting. Average results on5independent runs are reported.

**中文**

在 MS MARCO 上，AgenticGEO 在 Qwen2.5-32B-Instruct 和 Llama3.3-70B-Instruct 上均优于最强基线 AutoGEO 11% 以上。在电子商务数据集上，优势更加明显。跨两个看不见的域的可转移性增益支持了 AgenticGEO 避免过度拟合特定内容的说法。不断发展的策略档案和评论家指导的规划的设计产生了可转移的优化策略，该策略在域转移下仍然有效，显示出强大的域泛化性。表 2：域内设置的总体性能。报告 5 次独立运行的平均结果。

### 段落 72 · Page 7

**EN**

∗ indicates the statistically significant improvements over the best baseline, with𝑝-value smaller than0.001.

**中文**

* 表示相对于最佳基线有统计上显着的改善，其中𝑝值小于0.001。

### 段落 73 · Page 7

**EN**

Methods GEO-Bench Qwen2.5-32B-Instruct Llama3.3-70B-Instruct word pos overall word pos overall No optimization 20.05 20.26 20.21 19.19 19.33 19.20 Keyword Stuffing 20.73 20.86 20.69 19.99 20.16 20.02 Unique Words 17.59 17.94 17.78 16.78 16.66 16.56 Easy-To-Understand 20.10 20.19 20.05 18.72 18.93 18.85 Authoritative 20.41 20.93 20.60 19.41 19.48 19.47 Technical Words 21.22 20.97 21.23 19.55 19.59 19.50 Fluency Optimization 20.66 20.85 20.73 19.31 19.58 19.47 Cite Sources 22.64 22.91 22.53 21.95 22.11 21.98 Quotation Addition 23.96 24.18 23.76 21.74 21.77 21.57 Statistics Addition 22.34 22.86 22.30 21.07 21.23 21.05 AutoGEO 23.51 23.70 23.71 2

**中文**

方法 GEO-Bench Qwen2.5-32B-指示 Llama3.3-70B-指示单词 pos 总体 单词 pos 总体 无优化 20.05 20.26 20.21 19.19 19.33 19.20 关键词堆砌 20.73 20.86 20.69 19.99 20.16 20.02 独特词汇 17.59 17.94 17.78 16.78 16.66 16.56 简单易懂 20.10 20.19 20.05 18.72 18.93 18.85 权威 20.41 20.93 20.60 19.41 19.48 19.47 技术词汇 21.22 20.97 21.23 19.55 19.59 19.50 流畅度优化 20.66 20.85 20.73 19.31 19.58 19.47 引用来源 22.64 22.91 22.53 21.95 22.11 21.98 报价添加 23.96 24.18 23.76 21.74 21.77 21.57 统计添加 22.34 22.86 22.30 21.07 21.23 21.05 AutoGEO 23.51 23.70 23.71 2

### 段落 74 · Page 7

**EN**

2.77 22.65 22.78 Cite Sources-SFT 23.02 23.30 22.91 22.26 22.43 22.21 Quotation Addition-SFT 24.10 24.28 23.92 22.31 22.45 22.20 Statistics Addition-SFT 23.05 23.47 23.02 21.79 21.90 21.75 AgenticGEO (ours)* 25.42 25.85 25.48 24.38 24.59 24.52 Gains (%) 26.78 27.59 26.08 27.05 27.21 27.71 5.4 Ablation Analysis (RQ3) Impact of Core Components.Figure 4 shows that removing any of the components degrades performance on all datasets.

**中文**

2.77 22.65 22.78 引用来源-SFT 23.02 23.30 22.91 22.26 22.43 22.21 引用添加-SFT 24.10 24.28 23.92 22.31 22.45 22.20 统计添加-SFT 23.05 23.47 23.02 21.79 21.90 21.75 AgenticGEO（我们的）* 25.42 25.85 25.48 24.38 24.59 24.52 收益 (%) 26.78 27.59 26.08 27.05 27.21 27.71 5.4 核心组件的消融分析 (RQ3) 影响。图 4 显示删除任何组件都会降低所有数据集的性能。

### 段落 75 · Page 7

**EN**

The largest drop comes from removing the evolved strategy archive (b), confirming that long-term strategy accumulation is the primary driver of gains. Using an offline-only critic (a) is also clearly weaker, highlighting the importance of online co-evolution and continual critic recalibration. Replacing critic-guided planning with random planning (c) and maintaining the archive by performance only (d) cause degrades, suggesting diversity-aware archive improves generability. Impact of Hyper-parameters.Figure 5 evaluates the hyperparameters of AgenticGEO on GEO-Bench.

**中文**

最大的下降来自于删除进化策略档案（b），这证实了长期策略积累是收益的主要驱动力。使用仅限离线的批评家（a）也明显较弱，凸显了在线共同进化和持续批评家重新校准的重要性。用随机规划 (c) 取代评论家指导的规划并仅通过性能维护存档 (d) 会导致性能下降，这表明具有多样性意识的存档可提高可生成性。超参数的影响。图5评估了AgenticGEO在GEO-Bench上的超参数。

### 段落 76 · Page 7

**EN**

Multi-turn rewriting works best at3turns (overall25 .48), while adding more turns brings only small gains, indicating that a short planning is enough in practice. Archive size works best with a medium archive (25–35strategies), peaking at35, whereas very small or very large archives perform worse, reflecting a trade-off between exploration and exploitation. Impact of Offline Critic Alignment.We evaluate the efficacy of offline pre-training as a warm-start for online co-evolutionary learning. The critic is prompted to predict how the downstream engine would rank the seed strategies, comparing to the ground-truth with NDCG@K [20] metrics.

**中文**

多轮重写在 3 轮时效果最好（总体为 25 .48），而增加更多轮只带来很小的收益，这表明在实践中简短的规划就足够了。档案大小最适合中等档案（25-35 个策略），峰值为 35，而非常小的或非常大的档案表现较差，反映了探索和利用之间的权衡。离线批评者对齐的影响。我们评估离线预训练作为在线协同进化学习热启动的有效性。批评者被提示预测下游引擎将如何对种子策略进行排序，并与 NDCG@K [20] 指标的真实情况进行比较。

### 段落 77 · Page 7

**EN**

Table 4 shows that the offline-pretrained critic achieves consistently high NDCG across all datasets, including two unseen domains. On GEO-Bench, the critic closely matches the engine-derived preference ordering, with an NDCG@5 of approximately95%. While performance degrades on unseen domains, the critic still preserves strong top-rank fidelity, suggesting that it captures transferable signals rather than overfitting to the training distribution. These findings validate that the offline aligned critic model can serve as a reliable surrogate evaluator.

**中文**

表 4 显示，离线预训练的批评者在所有数据集（包括两个看不见的域）中均实现了一致的高 NDCG。在 GEO-Bench 上，评论家与引擎派生的偏好排序紧密匹配，NDCG@5 约为 95%。虽然性能在看不见的领域下降，但批评者仍然保留了强大的顶级保真度，这表明它捕获了可转移的信号，而不是过度拟合训练分布。这些发现验证了离线对齐批评者模型可以作为可靠的替代评估器。

### Page 8

### 段落 78 · Page 8

**EN**

Conference acronym ’XX, June 03–05, 2018, Woodstock, NY Jiaqi Yuan, Jialu Wang et al. Table 3: Overall Performance on the cross-domain setting. Average results on5independent runs are reported. ∗ indicates the statistically significant improvements over the best baseline, with𝑝-value smaller than0.001.

**中文**

会议缩写’XX，2018 年 6 月 3-05 日，纽约州伍德斯托克，Jiaqi Yuan、Jialu Wang 等人。表 3：跨域设置的总体性能。报告 5 次独立运行的平均结果。 * 表示相对于最佳基线有统计上显着的改善，其中𝑝值小于0.001。

### 段落 79 · Page 8

**EN**

Qwen2.5-32B-Instruct Llama3.3-70B-Instruct Methods MS MARCO E-Commerce MS MARCO E-Commerce word pos overall word pos overall word pos overall word pos overall No optimization 19.99 20.15 20.05 18.30 18.09 18.01 19.45 19.64 19.67 19.70 19.45 19.68 Keyword Stuffing 23.26 22.63 22.75 18.94 18.52 18.65 22.02 21.77 21.96 20.24 19.96 20.16 Unique Words 17.95 18.24 18.23 18.12 18.09 18.01 18.94 18.88 18.76 19.16 19.04 19.15 Easy-To-Understand 20.48 20.46 20.46 20.46 20.45 20.29 19.75 19.84 19.84 20.28 19.91 20.18 Authoritative 21.29 21.08 21.07 19.84 19.32 19.64 20.23 20.21 20.10 20.06 19.82 20.06 Technical Words 22.20 22.15 22.27 20.58 20.68 20.34

**中文**

Qwen2.5-32B-指导 Llama3.3-70B-指导方法 MS MARCO 电子商务 MS MARCO 电子商务 word pos 整体 单词 pos 整体 单词 pos 整体 单词 pos 整体 无优化 19.99 20.15 20.05 18.30 18.09 18.01 19.45 19.64 19.67 19.70 19.45 19.68 关键字堆砌 23.26 22.63 22.75 18.94 18.52 18.65 22.02 21.77 21.96 20.24 19.96 20.16 唯一词 17.95 18.24 18.23 18.12 18.09 18.01 18.94 18.88 18.76 19.16 19.04 19.15 易于理解 20.48 20.46 20.46 20.46 20.45 20.29 19.75 19.84 19.84 20.28 19.91 20.18 权威性 21.29 21.08 21.07 19.84 19.32 19.64 20.23 20.21 20.10 20.06 19.82 20.06 技术词汇 22.20 22.15 22.27 20.58 20.68 20.34

### 段落 80 · Page 8

**EN**

21.59 21.51 21.58 20.53 20.22 20.48 Fluency Optimization 19.59 19.20 19.41 20.25 20.06 20.11 20.99 20.95 20.97 19.75 19.54 19.68 Cite Sources 27.65 26.47 26.54 21.28 21.06 21.54 25.36 24.71 24.97 21.69 21.31 21.52 Quotation Addition 29.70 28.70 28.43 21.75 21.91 21.54 26.59 25.81 25.66 20.85 20.49 20.69 Statistics Addition 25.79 24.89 24.91 20.64 20.15 20.43 23.69 23.17 23.33 20.29 20.07 20.28 AutoGEO 31.79 31.14 30.67 21.54 19.75 21.18 30.27 29.11 30.04 21.45 20.13 21.50 Cite Sources-SFT 30.24 29.55 29.36 21.96 21.88 21.67 28.63 28.07 28.15 21.70 21.43 21.65 Quotation Addition-SFT 31.16 30.30 30.08 22.1421.96 21.83 29.57 28.91 28.96 21.91 21

**中文**

21.59 21.51 21.58 20.53 20.22 20.48 流畅度优化 19.59 19.20 19.41 20.25 20.06 20.11 20.99 20.95 20.97 19.75 19.54 19.68 引用来源27.65 26.47 26.54 21.28 21.06 21.54 25.36 24.71 24.97 21.69 21.31 21.52 报价添加 29.70 28.70 28.43 21.75 21.91 21.54 26.59 25.81 25.66 20.85 20.49 20.69 统计加法 25.79 24.89 24.91 20.64 20.15 20.43 23.69 23.17 23.33 20.29 20.07 20.28 AutoGEO 31.79 31.14 30.67 21.54 19.75 21.18 30.27 29.11 30.04 21.45 20.13 21.50 引用来源-SFT 30.24 29.55 29.36 21.96 21.88 21.67 28.63 28.07 28.15 21.70 21.43 21.65 报价添加-SFT 31.16 30.30 30.08 22.1421.96 21.83 29.57 28.91 28.96 21.91 21

### 段落 81 · Page 8

**EN**

.66 21.70 Statistics Addition-SFT 29.21 28.75 28.34 21.83 21.49 21.60 27.74 27.31 27.52 21.47 21.18 21.30 AgenticGEO(ours)* 34.96 34.25 34.10 26.79 26.57 26.58 33.63 33.82 33.50 26.38 26.63 26.88 Gains (%) 74.89 69.98 70.07 46.39 46.88 47.58 72.90 72.20 70.31 33.9136.92 36.59 GEO-Bench MS-MarcoE-Commerce15 20 25 30 35 40Overall (%) 25.48 34.10 26.58 23.90 28.07 24.78 (a) GEO-Bench MS-MarcoE-Commerce15 20 25 30 35 40Overall (%) 25.48 34.10 26.58 20.40 21.65 20.08 (b) GEO-Bench MS-MarcoE-Commerce15 20 25 30 35 40Overall (%) 25.48 34.10 26.58 23.57 29.65 23.81 (c) GEO-Bench MS-MarcoE-Commerce15 20 25 30 35 40Overall (%) 25.48 34.10 26.58 24.87 3

**中文**

.66 21.70 统计添加-SFT 29.21 28.75 28.34 21.83 21.49 21.60 27.74 27.31 27.52 21.47 21.18 21.30 AgenticGEO（我们的）* 34.96 34.25 34.10 26.79 26.57 26.58 33.63 33.82 33.50 26.38 26.63 26.88 收益(%) 74.89 69.98 70.07 46.39 46.88 47.58 72.90 72.20 70.31 33.9136.92 36.59 GEO-Bench MS-MarcoE-Commerce15 20 25 30 35 40总体 (%) 25.48 34.10 26.58 23.90 28.07 24.78 (a) GEO-Bench MS-MarcoE-Commerce15 20 25 30 35 40总体 (%) 25.48 34.10 26.58 20.40 21.65 20.08 (b) GEO-Bench MS-Marco电子商务15 20 25 30 35 40总体 (%) 25.48 34.10 26.58 23.57 29.65 23.81 (c) GEO-Bench MS-Marco电子商务15 20 25 30 35 40总体 (%) 25.48 34.10 26.58 24.87 3

### 段落 82 · Page 8

**EN**

1.43 25.11 (d) AgenticGEO Offline Only Critic w/o Evolved Strategy Archive w/o Critic w/o Diversity Archive Figure 4: Ablation study of AgenticGEO on three datasets.

**中文**

1.43 25.11 (d) AgenticGEO 仅离线评论家，不含进化策略存档，不含评论家，不含多样性存档 图 4：AgenticGEO 在三个数据集上的消融研究。

### 段落 83 · Page 8

**EN**

We compare AgenticGEO with four variants: (a) an offline-only critic trained without online co-evolution, (b) removing the evolved strategy archive, (c) replacing the critic with random rewrite planning and the evolver directly generates the strategy, (d) maintaining the archive by performance only without diversity. 1 2 3 4 5 Turn 24.0 24.5 25.0 25.5 26.0Overall (%) 24.33 24.69 25.48 25.14 25.01 5 15 25 35 45 Archive Number 24.0 24.5 25.0 25.5 26.0Overall (%) 24.78 24.15 25.48 25.80 24.94 Figure 5: Hyper-parameter sensitivity analysis on GEO- Bench.

**中文**

我们将 AgenticGEO 与四个变体进行比较：（a）仅在没有在线共同进化的情况下训练的离线批评家，（b）删除进化的策略档案，（c）用随机重写计划替换批评家，进化者直接生成策略，（d）仅通过性能维护档案，没有多样性。 1 2 3 4 5 转 24.0 24.5 25.0 25.5 26.0 总体 (%) 24.33 24.69 25.48 25.14 25.01 5 15 25 35 45 存档数量 24.0 24.5 25.0 25.5 26.0 总体 (%) 24.78 24.15 25.48 25.80 24.94 图 5：GEO-Bench 上的超参数敏感性分析。

### 段落 84 · Page 8

**EN**

We report overall impression score when varying the multi-turn rewriting steps (left) and the archive size (right). The role of critic as the surrogate of GE at online evolution.As Figure 6 shows, by using the critic as a low-cost surrogate of the GE environment, we can substantially reduce expensive GE interactions without sacrificing much performance. With only700GE feedback, our method reaches an overall score of25 .12, preserving 98.1%of the best performance (25 .60) while using only41 .2%of the GE supervision, demonstrating sample-efficient online evolution under a limited feedback budget.

**中文**

我们报告改变多轮重写步骤（左）和存档大小（右）时的总体印象分数。评论家作为在线演化中 GE 代理的角色。如图 6 所示，通过使用批评家作为 GE 环境的低成本代理，我们可以在不牺牲太多性能的情况下大幅减少昂贵的 GE 交互。仅使用 700GE 反馈，我们的方法就达到了 25 .12 的总分，保留了 98.1% 的最佳性能 (25 .60)，同时仅使用 41 .2% 的 GE 监督，展示了有限反馈预算下的样本高效在线进化。

### 段落 85 · Page 8

**EN**

5.5 Semantic Consistency Evaluation (RQ4) Figure 7 compares the trade-off between semantic similarity and gains in overall scores. Most heuristic baselines preserve semantics well but yield limited improvements, suggesting that small Table 4: Offline critic ranking quality. Benchmark NDCG@1 NDCG@3 NDCG@5 GEO-Bench84.01 93.89 94.98 Ms-Marco77.73 81.39 82.82 E-Commerce68.47 73.77 78.46 200 700 1200 1700 GE Feedback 24.0 24.5 25.0 25.5 26.0Overall (%) 24.09 25.12 25.48 25.60 Figure 6: Effect of the amount of GE feedback on overall performance when evolving.

**中文**

5.5 语义一致性评估（RQ4） 图 7 比较了语义相似性和总体得分增益之间的权衡。大多数启发式基线很好地保留了语义，但产生的改进有限，这表明表 4：离线评论家排名质量较小。基准 NDCG@1 NDCG@3 NDCG@5 GEO-Bench84.01 93.89 94.98 Ms-Marco77.73 81.39 82.82 电子商务68.47 73.77 78.46 200 700 1200 1700 GE 反馈 24.0 24.5 25.0 25.5 26.0总体 (%) 24.09 25.12 25.48 25.60 图 6：演变时 GE 反馈量对总体性能的影响。

### 段落 86 · Page 8

**EN**

edits alone are often insufficient to meaningfully increase a document’s influence on visibility and attribution in the synthesized answers. AutoGEO achieves stronger overall performance, yet its semantic similarity is noticeably lower, indicating that its gains may come at the cost of larger content drift and information loss. In

**中文**

仅进行编辑通常不足以有意义地增加文档对合成答案中的可见性和归因的影响。 AutoGEO 实现了更强的整体性能，但其语义相似度明显较低，这表明其收益可能是以较大的内容漂移和信息丢失为代价的。在

### Page 9

### 段落 87 · Page 9

**EN**

AgenticGEO: A Self-Evolving Agentic System for Generative Engine Optimization Conference acronym ’XX, June 03–05, 2018, Woodstock, NY 0.95 0.96 0.97 0.98 0.99 Semantic Similarity 18 19 20 21 22 23 24 25 26Overall Score Keyword Stuffing Statistics Addition Cite Sources Quotation Addition AuthoritativeEasy-To-Understand Technical Words Fluency Optimization Unique Words AutoGEO AgenticGEO Figure 7: Semantic consistency and optimization effectiveness. Semantic Similarity is measured by BERTScore-F1 [ 61] with roberta-large [27], computed between the original content and the rewritten version.

**中文**

AgenticGEO：用于生成式引擎优化的自我进化代理系统会议缩写’XX，2018 年 6 月 3-05 日，伍德斯托克，纽约 0.95 0.96 0.97 0.98 0.99 语义相似性 18 19 20 21 22 23 24 25 26 总体得分关键词堆砌统计添加引用来源 引文添加 权威易懂 技术词汇 流畅度优化 独特词汇 AutoGEO AgenticGEO 图7：语义一致性和优化效果。语义相似度由 BERTScore-F1 [61] 和 roberta-large [27] 测量，在原始内容和重写版本之间计算。

### 段落 88 · Page 9

**EN**

contrast, AgenticGEO attains the best overall score while maintaining relatively high semantic similarity, demonstrating that it can strengthen a document’s impact on the generated answers without information loss. This indicates that AgenticGEO does not rely on aggressive rewriting. It leverages content-aware strategy selection and moderate, targeted edits that enhance salience and evidence presentation while largely preserving the original meaning. 6 Conclusion We study Generative Engine Optimization (GEO) for black-box engines, shifting the objective from rank to visibility in synthesized outputs.

**中文**

相比之下，AgenticGEO 获得了最好的总体得分，同时保持了相对较高的语义相似性，这表明它可以在不丢失信息的情况下增强文档对生成答案的影响。这表明 AgenticGEO 不依赖于激进的重写。它利用内容感知策略选择和适度、有针对性的编辑，增强显着性和证据呈现，同时在很大程度上保留原始含义。 6 结论 我们研究黑盒引擎的生成式引擎优化（GEO），将目标从排名转向合成输出的可见性。

### 段落 89 · Page 9

**EN**

We show that static heuristics lack adaptability under content heterogeneity and changing GE behaviors. To address high interaction costs, we introduce a lightweight, calibrated critic as a reliable proxy. Built on this, AgenticGEO enables content-adaptive, self-evolving optimization by co-evolving a diverse strategy archive with the critic. Across representative settings, AgenticGEO delivers consistent improvements and strong cross-domain transfer. Our study points to a sustainable direction for web ecosystem governance that rewards quality and diversity, fostering a mutually beneficial development for creators and engines.

**中文**

我们表明静态启发法在内容异质性和不断变化的 GE 行为下缺乏适应性。为了解决高交互成本的问题，我们引入了一个轻量级的、经过校准的批评家作为可靠的代理。在此基础上，AgenticGEO 通过与评论家共同进化多样化的策略档案来实现内容自适应、自我进化的优化。在代表性设置中，AgenticGEO 提供一致的改进和强大的跨域传输。我们的研究指出了网络生态系统治理的可持续方向，奖励质量和多样性，促进创作者和引擎的互利发展。

### 段落 90 · Page 9

**EN**

References [1] Pranjal Aggarwal, Vishvak Murahari, Tanmay Rajpurohit, Ashwin Kalyan, Karthik Narasimhan, and Ameet Deshpande. 2024. Geo: Generative engine optimization. InProceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining. 5–16. [2] Firas Almukhtar, Nawzad Mahmoodd, and Shahab Kareem. 2021. Search engine optimization: a review.Applied computer science17, 1 (2021), 70–80. [3] Bing Search Blog. 2024.Introducing Bing generative search. https://blogs.bing. com/search/July-2024/generativesearch [4] Cornelia Brantner, Michael Karlsson, and Joanne Kuai. 2025.

**中文**

参考文献 [1] Pranjal Aggarwal、Vishvak Murahari、Tanmay Rajpurohit、Ashwin Kalyan、Karthik Narasimhan 和 Ameet Deshpande。 2024.Geo：生成式引擎优化。第 30 届 ACM SIGKDD 知识发现和数据挖掘会议论文集。 5-16。 [2] Firas Almukhtar、Nawzad Mahmoodd 和 Shahab Kareem。 2021. 搜索引擎优化：综述。应用计算机科学17, 1 (2021), 70–80。 [3] 必应搜索博客。 2024 年。推出 Bing 生成搜索。 https://blogs.bing。 com/search/July-2024/generativesearch [4] Cornelia Brantner、Michael Karlsson 和 Joanne Kuai。 2025 年。

### 段落 91 · Page 9

**EN**

Sourcing behavior and the role of news media in AI-powered search engines in the digital media ecosystem: Comparing political news retrieval across five languages.Telecommunications Policy(2025), 102952. [5] Sergey Brin and Lawrence Page. 1998. The Anatomy of a Large-Scale Hypertextual Web Search Engine.Computer Networks and ISDN Systems30, 1–7 (1998), 107–117. doi:10.1016/S0169-7552(98)00110-X [6] Andrei Z Broder. 1997. On the resemblance and containment of documents. InProceedings. Compression and Complexity of SEQUENCES 1997 (Cat. No. 97TB100171). IEEE, 21–29. [7] Kenrick Cai. 2025.Google tests an AI-only version of its search engine.

**中文**

数字媒体生态系统中人工智能驱动的搜索引擎中新闻媒体的采购行为和作用：比较五种语言的政治新闻检索。电信政策（2025），102952。 [5] Sergey Brin 和 Lawrence Page。 1998. 大规模超文本 Web 搜索引擎的剖析。计算机网络和 ISDN 系统 30, 1–7 (1998), 107–117。 doi:10.1016/S0169-7552(98)00110-X [6] 安德烈·Z·布罗德。 1997.论文件的相似性和包含性。在诉讼中。序列的压缩和复杂性 1997（目录号 97TB100171）。 IEEE，21-29。 [7] 蔡肯里克. 2025 年。谷歌测试其搜索引擎的纯人工智能版本。

### 段落 92 · Page 9

**EN**

Reuters. https://www.reuters.com/technology/artificial-intelligence/googletests-an-ai-only-version-its-search-engine-2025-03-05/ [8] Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas. 2025. Generative engine optimization: How to dominate ai search.arXiv preprint arXiv:2509.08919 (2025). [9] Xiaolu Chen, Haojie Wu, Jie Bao, Zhen Chen, Yong Liao, and Hu Huang. 2025. Role-Augmented Intent-Driven Generative Search Engine Optimization.arXiv preprint arXiv:2508.11158(2025). [10] Kalyanmoy Deb, Amrit Pratap, Sameer Agarwal, and TAMT Meyarivan. 2002.

**中文**

路透社。 https://www.reuters.com/technology/artificial-intelligence/googletests-an-ai-only-version-its-search-engine-2025-03-05/ [8] Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas。 2025. 生成式引擎优化：如何主导 ai search.arXiv 预印本 arXiv:2509.08919 (2025)。 [9] 陈小鲁，吴浩杰，包杰，陈震，廖勇，黄虎。 2025. 角色增强意图驱动生成式搜索引擎优化.arXiv 预印本 arXiv:2508.11158(2025)。 [10] Kalyanmoy Deb、Amrit Pratap、Sameer Agarwal 和 TAMT Meyarivan。 2002年。

### 段落 93 · Page 9

**EN**

A fast and elitist multiobjective genetic algorithm: NSGA-II.IEEE transactions on evolutionary computation6, 2 (2002), 182–197. [11] Jinyuan Fang, Yanwen Peng, Xi Zhang, Yingxu Wang, Xinhao Yi, Guibin Zhang, Yi Xu, Bin Wu, Siwei Liu, Zihao Li, et al . 2025. A comprehensive survey of self-evolving ai agents: A new paradigm bridging foundation models and lifelong agentic systems.arXiv preprint arXiv:2508.07407(2025). [12] Chrisantha Fernando, Dylan Banarse, Henryk Michalewski, Simon Osindero, and Tim Rocktäschel. 2023. Promptbreeder: Self-referential self-improvement via prompt evolution.arXiv preprint arXiv:2309.16797(2023).

**中文**

一种快速且精英的多目标遗传算法：NSGA-II.IEEE 进化计算交易6, 2 (2002), 182–197。 [11] 方金元，彭彦文，张曦，王迎旭，易新浩，张桂斌，徐毅，吴斌，刘思伟，李子豪，等。 2025.自我进化人工智能代理的全面调查：桥接基础模型和终身代理系统的新范式。arXiv 预印本 arXiv：2508.07407（2025）。 [12] Chrisantha Fernando、Dylan Banarse、Henryk Michalewski、Simon Osindero 和 Tim Rocktäschel。 2023. Promptbreeder：通过即时进化进行自我参照自我改进。arXiv 预印本 arXiv：2309.16797（2023）。

### 段落 94 · Page 9

**EN**

[13] Yunfan Gao, Yun Xiong, Xinyu Gao, Kangxiang Jia, Jinliu Pan, Yuxi Bi, Yixin Dai, Jiawei Sun, Haofen Wang, and Haofen Wang. 2023. Retrieval-augmented generation for large language models: A survey.arXiv preprint arXiv:2312.10997 2, 1 (2023). [14] Aaron Grattafiori, Abhimanyu Dubey, Abhinav Jauhri, Abhinav Pandey, Abhishek Kadian, Ahmad Al-Dahle, Aiesha Letman, Akhil Mathur, and et al. 2024. The Llama 3 Herd of Models. arXiv:2407.21783 [cs.AI] https://arxiv.org/abs/2407. 21783 [15] Qingyan Guo, Rui Wang, Junliang Guo, Bei Li, Kaitao Song, Xu Tan, Guoqing Liu, Jiang Bian, and Yujiu Yang. 2023.

**中文**

[13] 高云帆，熊云，高新宇，贾康祥，潘金六，毕玉玺，戴一新，孙家伟，王浩芬，王浩芬。 2023.大型语言模型的检索增强生成：调查.arXiv 预印本 arXiv:2312.10997 2, 1 (2023)。 [14] Aaron Grattafiori、Abhimanyu Dubey、Abhinav Jauhri、Abhinav Pandey、Abhishek Kadian、Ahmad Al-Dahle、Aiesha Letman、Akhil Mathur 等。 2024. Llama 3 模特群。 arXiv:2407.21783 [cs.AI] https://arxiv.org/abs/2407。 21783 [15] 郭清艳，王锐，郭俊良，李蓓，宋凯涛，谭旭，刘国庆，卞江，杨玉九。 2023 年。

### 段落 95 · Page 9

**EN**

Connecting large language models with evolutionary algorithms yields powerful prompt optimizers.arXiv preprint arXiv:2309.08532(2023). [16] Edward J Hu, Yelong Shen, Phillip Wallis, Zeyuan Allen-Zhu, Yuanzhi Li, Shean Wang, Lu Wang, Weizhu Chen, et al. 2022. Lora: Low-rank adaptation of large language models.ICLR1, 2 (2022), 3. [17] Mengkang Hu, Pu Zhao, Can Xu, Qingfeng Sun, Jian-Guang Lou, Qingwei Lin, Ping Luo, and Saravan Rajmohan. 2025. Agentgen: Enhancing planning abilities for large language model based agent via environment and task generation. In Proceedings of the 31st ACM SIGKDD Conference on Knowledge Discovery and Data Mining V.

**中文**

将大型语言模型与进化算法连接起来会产生强大的提示优化器。arXiv 预印本 arXiv:2309.08532(2023)。 [16] Edward J Hu, Yelong Shen, Phillip Wallis, Zeyuan Allen-Zhu, Yuanzhi Li, Shean Wang, Lu Wang, Weizhu Chen, et al. 2022. Lora：大型语言模型的低阶适应。ICLR1, 2 (2022), 3。 [17] 胡孟康，赵普，徐灿，孙庆丰，楼建光，林清伟，罗平，萨拉万·拉杰莫汉。 2025. Agentgen：通过环境和任务生成增强基于大型语言模型的代理的规划能力。第 31 届 ACM SIGKDD 知识发现和数据挖掘会议论文集 V.

### 段落 96 · Page 9

**EN**

1. 496–507. [18] Peter J Huber. 1992. Robust estimation of a location parameter. InBreakthroughs in statistics: Methodology and distribution. Springer, 492–518. [19] Gautier Izacard and Edouard Grave. 2021. Leveraging passage retrieval with generative models for open domain question answering. InProceedings of the 16th conference of the european chapter of the association for computational linguistics: main volume. 874–880. [20] Kalervo Järvelin and Jaana Kekäläinen. 2002. Cumulated gain-based evaluation of IR techniques.ACM Transactions on Information Systems (TOIS)20, 4 (2002), 422–446.

**中文**

1. 496–507。 [18] 彼得·J·胡贝尔。 1992。位置参数的鲁棒估计。统计学的突破：方法论和分布。施普林格，492-518。 [19]戈蒂埃·伊扎卡尔和爱德华·格雷夫。 2021 年。利用段落检索和生成模型进行开放域问答。计算语言学协会欧洲分会第 16 届会议论文集：主卷。 874–880。 [20]Kalervo Järvelin 和 Jaana Kekäläinen。 2002. 基于累积增益的 IR 技术评估。ACM 信息系统交易 (TOIS)20, 4 (2002), 422–446。

### 段落 97 · Page 9

**EN**

[21] Niels Justesen, Sebastian Risi, and Jean-Baptiste Mouret. 2019. Map-elites for noisy domains by adaptive sampling. InProceedings of the genetic and evolutionary computation conference companion. 121–122. [22] Aounon Kumar and Himabindu Lakkaraju. 2024. Manipulating large language models to increase product visibility.arXiv preprint arXiv:2404.07981(2024). [23] Joel Lehman and Kenneth O Stanley. 2011. Evolving a diversity of virtual creatures through novelty search and local competition. InProceedings of the 13th annual conference on Genetic and evolutionary computation. 211–218. [24] Dirk Lewandowski, Sebastian Sünkler, and Nurce Yagci.

**中文**

[21] Niels Justesen、Sebastian Risi 和 Jean-Baptiste Mouret。 2019.通过自适应采样对噪声域进行映射精英。在遗传和进化计算会议同伴的会议记录中。 121-122。 [22]奥农·库马尔和希玛宾杜·拉卡拉朱。 2024 年。操纵大型语言模型以提高产品可见性。arXiv 预印本 arXiv：2404.07981（2024）。 [23] 乔尔·雷曼和肯尼思·O·斯坦利。 2011.通过新颖性搜索和本地竞争进化出虚拟生物的多样性。第 13 届遗传与进化计算年会论文集。 211-218。 [24] 德克·莱万多夫斯基、塞巴斯蒂安·桑克勒和努尔斯·亚格奇。

### 段落 98 · Page 9

**EN**

2021. The influence of search engine optimization on Google’s results: A multi-dimensional approach

**中文**

2021. 搜索引擎优化对 Google 结果的影响：多维方法

### Page 10

### 段落 99 · Page 10

**EN**

Conference acronym ’XX, June 03–05, 2018, Woodstock, NY Jiaqi Yuan, Jialu Wang et al. for detecting SEO. InProceedings of the 13th ACM Web Science Conference 2021 (WebSci ’21). ACM, 9 pages. doi:10.1145/3447535.3462479 [25] Patrick Lewis, Ethan Perez, Aleksandra Piktus, Fabio Petroni, Vladimir Karpukhin, Naman Goyal, Heinrich Küttler, Mike Lewis, Wen-tau Yih, Tim Rocktäschel, et al. 2020. Retrieval-augmented generation for knowledge-intensive nlp tasks. Advances in neural information processing systems33 (2020), 9459–9474. [26] Junjun Li, Zeyuan Ma, Ting Huang, and Yue-Jiao Gong. 2025.

**中文**

会议缩写’XX，2018 年 6 月 3-05 日，纽约州伍德斯托克，Jiaqi Yuan、Jialu Wang 等人。用于检测 SEO。 2021 年第 13 届 ACM 网络科学会议 (WebSci ’21) 论文集。 ACM，9 页。 doi:10.1145/3447535.3462479 [25] Patrick Lewis、Ethan Perez、Aleksandra Piktus、Fabio Petroni、Vladimir Karpukhin、Naman Goyal、Heinrich Küttler、Mike Lewis、Wen-tau Yih、Tim Rocktäschel 等。 2020.知识密集型 NLP 任务的检索增强生成。神经信息处理系统的进展33 (2020), 9459–9474。 [26] 李军军，马泽元，黄婷，龚月娇。 2025 年。

### 段落 100 · Page 10

**EN**

Learn to Refine: Synergistic Multi-Agent Path Optimization for Lifelong Conflict-Free Navigation of Autonomous Vehicles. InProceedings of the 31st ACM SIGKDD Conference on Knowledge Discovery and Data Mining V. 2. 1400–1411. [27] Yinhan Liu, Myle Ott, Naman Goyal, Jingfei Du, Mandar Joshi, Danqi Chen, Omer Levy, Mike Lewis, Luke Zettlemoyer, and Veselin Stoyanov. 2019. Roberta: A robustly optimized bert pretraining approach.arXiv preprint arXiv:1907.11692 (2019). [28] Yuxuan Liu, Hongda Sun, Wei Liu, Jian Luan, Bo Du, and Rui Yan. 2025.

**中文**

学习细化：协同多智能体路径优化，实现自动驾驶车辆终身无冲突导航。第 31 届 ACM SIGKDD 知识发现和数据挖掘会议记录 V. 2. 1400–1411。 [27] Yinhan Liu、Myle Ott、Naman Goyal、Jingfei Du、Mandar Joshi、Danqi Chen、Omer Levy、Mike Lewis、Luke Zettlemoyer 和 Veselin Stoyanov。 2019. Roberta：一种稳健优化的 bert 预训练方法。arXiv 预印本 arXiv:1907.11692 (2019)。 [28] 刘宇轩，孙宏达，刘伟，栾建，杜波，严锐。 2025 年。

### 段落 101 · Page 10

**EN**

MobileSteward: Integrating Multiple App-Oriented Agents with Self-Evolution to Automate Cross-App Instructions. InProceedings of the 31st ACM SIGKDD Conference on Knowledge Discovery and Data Mining V. 1. 883–893. [29] Aman Madaan, Niket Tandon, Prakhar Gupta, Skyler Hallinan, Luyu Gao, Sarah Wiegreffe, Uri Alon, Nouha Dziri, Shrimai Prabhumoye, Yiming Yang, et al . 2023. Self-refine: Iterative refinement with self-feedback.Advances in Neural Information Processing Systems36 (2023), 46534–46594. [30] Ross A Malaga. 2010. Search engine optimization—black and white hat approaches. InAdvances in computers. Vol. 78. Elsevier, 1–39.

**中文**

MobileSteward：通过自我进化集成多个面向应用程序的代理，以自动化跨应用程序指令。第 31 届 ACM SIGKDD 知识发现和数据挖掘会议记录 V. 1. 883–893。 [29] Aman Madaan、Niket Tandon、Prakhar Gupta、Skyler Hallinan、Luyu Gau、Sarah Wiegreffe、Uri Alon、Nouha Dziri、Shrimai Prabhumoye、Yiming Yang 等。 2023.自我细化：自我反馈的迭代细化。神经信息处理系统的进展36（2023），46534–46594。 [30] 罗斯·A·马拉加。 2010。搜索引擎优化——黑白帽方法。计算机的进步。卷。 78. 爱思唯尔，1-39。

### 段落 102 · Page 10

**EN**

[31] Christopher D. Manning, Prabhakar Raghavan, and Hinrich Schütze. 2008.Introduction to Information Retrieval. Cambridge University Press. [32] Jacob Menick, Maja Trebacz, Vladimir Mikulik, John Aslanides, Francis Song, Martin Chadwick, Mia Glaese, Susannah Young, Lucy Campbell-Gillingham, Geoffrey Irving, et al. 2022. Teaching language models to support answers with verified quotes, 2022.URL https://arxiv. org/abs/2203.11147(2022). [33] Jean-Baptiste Mouret and Jeff Clune. 2015. Illuminating search spaces by mapping elites.arXiv preprint arXiv:1504.04909(2015).

**中文**

[31] Christopher D. Manning、Prabhakar Raghavan 和 Hinrich Schütze。 2008.信息检索导论。剑桥大学出版社。 [32] Jacob Menick、Maja Trebacz、Vladimir Mikulik、John Aslanides、Francis Song、Martin Chadwick、Mia Glaese、Susannah Young、Lucy Campbell-Gillingham、Geoffrey Irving 等。 2022. 教学语言模型以支持经过验证的引用的答案，2022.URL https://arxiv。 org/abs/2203.11147(2022)。 [33]让-巴蒂斯特·穆雷和杰夫·克鲁恩。 2015.通过映射精英照亮搜索空间.arXiv 预印本 arXiv:1504.04909(2015)。

### 段落 103 · Page 10

**EN**

[34] Reiichiro Nakano, Jacob Hilton, Suchir Balaji, Jeff Wu, Long Ouyang, Christina Kim, Christopher Hesse, Shantanu Jain, Vineet Kosaraju, William Saunders, et al. 2021. Webgpt: Browser-assisted question-answering with human feedback.arXiv preprint arXiv:2112.09332(2021). [35] Reiichiro Nakano, Jacob Hilton, Suchir Balaji, Jeff Wu, Long Ouyang, Christina Kim, Christopher Hesse, Shantanu Jain, Vineet Kosaraju, William Saunders, et al. 2022. Webgpt: Browser-assisted question-answering with human feedback, 2022. URL https://arxiv. org/abs/2112.09332(2022). [36] Fredrik Nestaas, Edoardo Debenedetti, and Florian Tramèr. 2024.

**中文**

[34] Reiichiro Nakano、Jacob Hilton、Suchir Balaji、Jeff Wu、Long Ouyang、Christina Kim、Christopher Hesse、Shantanu Jain、Vineet Kosaraju、William Saunders 等。 2021.Webgpt：浏览器辅助问答与人类反馈。arXiv 预印本 arXiv：2112.09332（2021）。 [35] Reiichiro Nakano、Jacob Hilton、Suchir Balaji、Jeff Wu、Long Ouyang、Christina Kim、Christopher Hesse、Shantanu Jain、Vineet Kosaraju、William Saunders 等。 2022。Webgpt：带有人类反馈的浏览器辅助问答，2022。URL https://arxiv。 org/abs/2112.09332(2022)。 [36] Fredrik Nestaas、Edoardo Debenedetti 和 Florian Tramèr。 2024 年。

### 段落 104 · Page 10

**EN**

Adversarial search engine optimization for large language models.arXiv preprint arXiv:2406.18382(2024). [37] Tri Nguyen, Mir Rosenberg, Xia Song, Jianfeng Gao, Saurabh Tiwary, Rangan Majumder, and Li Deng. 2016. Ms marco: A human-generated machine reading comprehension dataset. (2016). [38] Long Ouyang, Jeff Wu, Xu Jiang, Diogo Almeida, Carroll L. Wainwright, Pamela Mishkin, Chong Zhang, Sandhini Agarwal, Katarina Slama, Alex Ray, John Schulman, Jacob Hilton, Fraser Kelton, Luke Miller, Maddie Simens, Amanda Askell, Peter Welinder, Paul Christiano, Jan Leike, and Ryan Lowe. 2022.

**中文**

大型语言模型的对抗性搜索引擎优化。arXiv 预印本 arXiv:2406.18382(2024)。 [37] Tri Nguyen，Mir Rosenberg，夏宋，高剑锋，Saurabh Tiwary，Rangan Majumder，邓力。 2016. Ms marco：人类生成的机器阅读理解数据集。 （2016）。 [38] 欧阳龙、吴杰夫、徐江、迪奥戈·阿尔梅达、卡罗尔·温赖特、帕梅拉·米什金、张冲、桑迪尼·阿加瓦尔、卡塔琳娜·斯拉马、亚历克斯·雷、约翰·舒尔曼、雅各布·希尔顿、弗雷泽·凯尔顿、卢克·米勒、麦迪·西蒙斯、阿曼达·阿斯克尔、彼得·韦林德、保罗·克里斯蒂亚诺、扬·雷克和瑞安·洛。 2022 年。

### 段落 105 · Page 10

**EN**

Training language models to follow instructions with human feedback.arXiv preprint arXiv:2203.02155(2022). arXiv:2203.02155 [cs.CL] [39] Lawrence Page, Sergey Brin, Rajeev Motwani, and Terry Winograd. 1999.The PageRank citation ranking: Bringing order to the web.Technical Report. Stanford infolab. [40] Perplexity Support. [n. d.].How does Perplexity work?Perplexity Help Center. https://www.perplexity.ai/help-center/en/articles/10352895-how-doesperplexity-work [41] Justin K Pugh, Lisa B Soros, and Kenneth O Stanley. 2016. Quality diversity: A new frontier for evolutionary computation.Frontiers in Robotics and AI3 (2016), 40.

**中文**

训练语言模型以遵循人类反馈的指令。arXiv 预印本 arXiv:2203.02155(2022)。 arXiv:2203.02155 [cs.CL] [39] 劳伦斯·佩奇、谢尔盖·布林、拉吉夫·莫特瓦尼和特里·维诺格拉德。 1999 年。PageRank 引用排名：为网络带来秩序。技术报告。斯坦福信息实验室。 [40] 困惑支持。 [n. d.].Perplexity 如何工作？Perplexity 帮助中心。 https://www.perplexity.ai/help-center/en/articles/10352895-how-doesperplexity-work [41] Justin K Pugh、Lisa B Soros 和 Kenneth O Stanley。 2016. 质量多样性：进化计算的新前沿。机器人与人工智能前沿3 (2016), 40.

### 段落 106 · Page 10

**EN**

[42] Chandan K Reddy, Lluís Màrquez, Fran Valero, Nikhil Rao, Hugo Zaragoza, Sambaran Bandyopadhyay, Arnab Biswas, Anlu Xing, and Karthik Subbian. 2022. Shopping queries dataset: A large-scale ESCI benchmark for improving product search.arXiv preprint arXiv:2206.06588(2022). [43] Zafar Saeed, Fozia Aslam, Adnan Ghafoor, Muhammad Umair, and Imran Razzak. 2024. Exploring the impact of SEO-based ranking factors for voice queries through machine learning.Artificial Intelligence Review57, 6 (2024), 144. [44] Melanie Sclar, Yejin Choi, Yulia Tsvetkov, and Alane Suhr. 2024.

**中文**

[42] Chandan K Reddy、Lluís Màrquez、Fran Valero、Nikhil Rao、Hugo Zaragoza、Sambaran Bandyopadhyay、Arnab Biswas、Anlu Xing 和 Karthik Subbian。 2022. 购物查询数据集：用于改进产品搜索的大规模 ESCI 基准。arXiv 预印本 arXiv:2206.06588(2022)。 [43]扎法尔·赛义德、福齐亚·阿斯拉姆、阿德南·加福尔、穆罕默德·乌迈尔和伊姆兰·拉扎克。 2024 年。通过机器学习探索基于 SEO 的语音查询排名因素的影响。人工智能评论 57, 6 (2024), 144。 [44] Melanie Sclar、Yejin Choi、Yulia Tsvetkov 和 Alane Suhr。 2024 年。

### 段落 107 · Page 10

**EN**

Quantifying Language Models’ Sensitivity to Spurious Features in Prompt Design or: How I Learned to Start Worrying about Prompt Formatting. InInternational Conference on Learning Representations (ICLR). [45] Asim Shahzad, Deden Witarsyah Jacob, Nazri Mohd Nawi, Hairulnizam Mahdin, and Marheni Eka Saputri. 2020. The new trend for search engine optimization, tools and techniques.Indonesian Journal of Electrical Engineering and Computer Science18, 3 (2020), 1568–1583. [46] Zhihong Shao, Peiyi Wang, Qihao Zhu, Runxin Xu, Junxiao Song, Xiao Bi, Haowei Zhang, Mingchuan Zhang, Y.K. Li, Y. Wu, and Daya Guo. 2024.

**中文**

量化语言模型对提示设计中虚假特征的敏感性或：我如何学会开始担心提示格式。在国际学习表征会议（ICLR）中。 [45] Asim Shahzad、Deden Witarsyah Jacob、Nazri Mohd Nawi、Hairulnizam Mahdin 和 Marheni Eka Saputri。 2020。搜索引擎优化、工具和技术的新趋势。印度尼西亚电气工程和计算机科学杂志18, 3 (2020), 1568–1583。 [46] 邵志宏，王培毅，朱启浩，徐润鑫，宋俊晓，毕晓，张浩伟，张铭传，Y.K.李、吴、郭大亚。 2024 年。

### 段落 108 · Page 10

**EN**

DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models.arXiv preprint arXiv:2402.03300(2024). arXiv:2402.03300 [cs.CL] [47] Dushyant Sharma, Rishabh Shukla, Anil Kumar Giri, and Sumit Kumar. 2019. A brief review on search engine optimization. In2019 9th international conference on cloud computing, data science & engineering (confluence). IEEE, 687–692. [48] Noah Shinn, Federico Cassano, Beck Labash, Ashwin Gopinath, Karthik Narasimhan, and Shunyu Yao. 2023. Reflexion: Language agents with verbal reinforcement learning, 2023.URL https://arxiv. org/abs/2303.113661 (2023). [49] Robby Stein.

**中文**

DeepSeekMath：突破开放语言模型中数学推理的极限。arXiv 预印本 arXiv：2402.03300(2024)。 arXiv:2402.03300 [cs.CL] [47] Dushyant Sharma、Rishabh Shukla、Anil Kumar Giri 和 Sumit Kumar。 2019.搜索引擎优化简述。 2019第九届云计算、数据科学与工程国际会议（Confluence）。 IEEE，687–692。 [48]Noah Shinn、Federico Cassano、Beck Labash、Ashwin Gopinath、Karthik Narasimhan 和 Shunyu Yao。 2023. 反射：具有言语强化学习的语言代理，2023.URL https://arxiv。 org/abs/2303.113661（2023）。 [49] 罗比·斯坦。

### 段落 109 · Page 10

**EN**

2025.Expanding AI Overviews and introducing AI Mode. https: //blog.google/products-and-platforms/products/search/ai-mode-search/ [50] Haotian Sun, Yuchen Zhuang, Lingkai Kong, Bo Dai, and Chao Zhang. 2023. Adaplanner: Adaptive planning from feedback with language models.Advances in neural information processing systems36 (2023), 58202–58245. [51] Qwen Team. 2025. Qwen2.5 Technical Report. arXiv:2412.15115 [cs.CL] https: //arxiv.org/abs/2412.15115 [52] Guanzhi Wang, Yuqi Xie, Yunfan Jiang, Ajay Mandlekar, Chaowei Xiao, Yuke Zhu, Linxi Fan, and Anima Anandkumar. 2023.

**中文**

2025.扩展人工智能概述并引入人工智能模式。 https://blog.google/products-and-platforms/products/search/ai-mode-search/ [50] 孙浩天，庄雨辰，孔令凯，戴波，张超。 2023. Adaplanner：根据语言模型反馈进行自适应规划。神经信息处理系统的进展36 (2023), 58202–58245。 [51]Qwen团队. 2025.Qwen2.5技术报告。 arXiv:2412.15115 [cs.CL] https: //arxiv.org/abs/2412.15115 [52] 王冠志、谢玉琪、蒋云帆、Ajay Mandlekar、肖超伟、朱宇克、范林西和阿尼玛·阿南德库马尔。 2023 年。

### 段落 110 · Page 10

**EN**

Voyager: An open-ended embodied agent with large language models.arXiv preprint arXiv:2305.16291(2023). [53] Yingxu Wang, Siwei Liu, Jinyuan Fang, and Zaiqiao Meng. 2025. Evoagentx: An automated framework for evolving agentic workflows. InProceedings of the 2025 Conference on Empirical Methods in Natural Language Processing: System Demonstrations. 643–655. [54] Yujiang Wu, Shanshan Zhong, Yubin Kim, and Chenyan Xiong. 2025. What Generative Search Engines Like and How to Optimize Web Content Cooperatively. arXiv preprint arXiv:2510.11438(2025). [55] Chengrun Yang, Xuezhi Wang, Yifeng Lu, Hanxiao Liu, Quoc V Le, Denny Zhou, and Xinyun Chen.

**中文**

Voyager：具有大型语言模型的开放式实体代理。arXiv 预印本 arXiv：2305.16291（2023）。 [53] 王迎旭，刘思伟，方金元，孟再巧。 2025. Evoagentx：用于发展代理工作流程的自动化框架。 2025 年自然语言处理经验方法会议论文集：系统演示。 643–655。 [54]吴玉江，钟珊珊，金玉斌，熊晨艳。 2025。生成式搜索引擎喜欢什么以及如何协同优化 Web 内容。 arXiv 预印本 arXiv：2510.11438(2025)。 [55] 杨成润，王学智，陆一峰，刘汉晓，Quoc V Le，Denny Zhou，陈新云。

### 段落 111 · Page 10

**EN**

2023. Large language models as optimizers. InThe Twelfth International Conference on Learning Representations. [56] Shunyu Yao, Jeffrey Zhao, Dian Yu, Nan Du, Izhak Shafran, Karthik R Narasimhan, and Yuan Cao. 2022. React: Synergizing reasoning and acting in language models. InThe eleventh international conference on learning representations. [57] Kamer Ali Yuksel, Thiago Castro Ferreira, Mohamed Al-Badrashiny, and Hassan Sawaf. 2025. A multi-AI agent system for autonomous optimization of agentic AI solutions via iterative refinement and LLM-driven feedback loops.

**中文**

2023.作为优化器的大型语言模型。在第十二届学习表征国际会议上。 [56] 姚舜宇，赵杰弗里，于殿，杜南，Izhak Shafran，Karthik R Narasimhan，曹元。 2022.React：在语言模型中协同推理和行动。在第十一届国际学习表征会议上。 [57] Kamer Ali Yuksel、Thiago Castro Ferreira、Mohamed Al-Badrashiny 和 Hassan Sawaf。 2025. 多人工智能代理系统，通过迭代细化和法学硕士驱动的反馈循环自主优化代理人工智能解决方案。

### 段落 112 · Page 10

**EN**

InProceedings of the 1st Workshop for Research on Agent Language Models (REALM 2025). 52–62. [58] Yunpeng Zhai, Shuchang Tao, Cheng Chen, Anni Zou, Ziqian Chen, Qingxu Fu, Shinji Mai, Li Yu, Jiaji Deng, Zouying Cao, et al. 2025. Agentevolver: Towards efficient self-evolving agent system.arXiv preprint arXiv:2511.10395(2025). [59] Jiayi Zhang, Jinyu Xiang, Zhaoyang Yu, Fengwei Teng, Xionghui Chen, Jiaqi Chen, Mingchen Zhuge, Xin Cheng, Sirui Hong, Jinlin Wang, et al. 2024. Aflow: Automating agentic workflow generation.arXiv preprint arXiv:2410.10762(2024).

**中文**

第一届代理语言模型研究研讨会论文集 (REALM 2025)。 52–62。 [58] 翟云鹏，陶树昌，陈程，邹安妮，陈子谦，付清旭，麦新司，李宇，邓家吉，曹邹英，等。 2025. Agentevolver：迈向高效的自我进化代理系统。arXiv 预印本 arXiv：2511.10395（2025）。 [59] 张嘉义，向金宇，于朝阳，滕凤伟，陈雄辉，陈嘉琪，诸葛名臣，程鑫，洪思瑞，王金林，等。 2024. Aflow：自动化代理工作流程生成。arXiv 预印本 arXiv：2410.10762（2024）。

### 段落 113 · Page 10

**EN**

[60] Qizheng Zhang, Changran Hu, Shubhangi Upasani, Boyuan Ma, Fenglu Hong, Vamsidhar Kamanuru, Jay Rainton, Chen Wu, Mengmeng Ji, Hanchen Li, et al. 2025. Agentic context engineering: Evolving contexts for self-improving language models.arXiv preprint arXiv:2510.04618(2025). [61] Tianyi Zhang, Varsha Kishore, Felix Wu, Kilian Q Weinberger, and Yoav Artzi. 2019. Bertscore: Evaluating text generation with bert.arXiv preprint arXiv:1904.09675(2019). [62] Yao Zhang, Chenyang Lin, Shijie Tang, Haokun Chen, Shijie Zhou, Yunpu Ma, and Volker Tresp. 2025.

**中文**

[60] 张启正，胡昌然，Shubhangi Upasani，马博远，洪凤路，Vamsidhar Kamanuru，Jay Rainton，吴晨，季萌萌，李汉辰，等。 2025.代理上下文工程：自我改进语言模型的进化上下文。arXiv 预印本 arXiv：2510.04618（2025）。 [61] 张天一、Varsha Kishore、Felix Wu、Kilian Q Weinberger 和 Yoav Artzi。 2019。Bertscore：使用 bert.arXiv 预印本 arXiv 评估文本生成：1904.09675（2019）。 [62] 张耀，林晨阳，唐世杰，陈浩坤，周世杰，马云普，Volker Tresp。 2025 年。

### 段落 114 · Page 10

**EN**

SwarmAgentic: Towards Fully Automated Agentic System Generation via Swarm Intelligence.arXiv preprint arXiv:2506.15672(2025). [63] Yongchao Zhou, Andrei Ioan Muresanu, Ziwen Han, Keiran Paster, Silviu Pitis, Harris Chan, and Jimmy Ba. 2022. Large language models are human-level prompt engineers. InThe eleventh international conference on learning representations. [64] Christos Ziakis, Maro Vlachopoulou, Theodosios Kyrkoudis, and Makrina Karagkiozidou. 2019. Important factors for improving Google search rank. Future Internet, 11 (2), 32.

**中文**

SwarmAgentic：通过 Swarm Intelligence 实现全自动代理系统生成.arXiv 预印本 arXiv:2506.15672(2025)。 [63] 周永超、Andrei Ioan Muresanu、Ziwen Han、Keiran Paster、Silviu Pitis、Harris Chan 和 Jimmy Ba。 2022年。大型语言模型是人类级别的提示工程师。在第十一届国际学习表征会议上。 [64] Christos Ziakis、Maro Vlachopoulou、Theodosios Kyrkoudis 和 Makrina Karagkiozidou。 2019年。提高Google搜索排名的重要因素。未来的互联网，11（2），32。

### Page 11

### 段落 115 · Page 11

**EN**

AgenticGEO: A Self-Evolving Agentic System for Generative Engine Optimization Conference acronym ’XX, June 03–05, 2018, Woodstock, NY A Supplementary Information A.1 Methodological Details A.1.1 Explanation of Figure1.For each instance, we run the nine rewriting strategies and obtain their average overall scores {𝑟𝑖 }9 𝑖=1, with the best score 𝑟 ★ =max 𝑖 𝑟𝑖. We quantify how many strategies remain competitive relative to the best. A strategy is considered near-optimal if it achieves at least55%of 𝑟 ★ (equivalently, its gap to 𝑟 ★ is no more than45%of 𝑟 ★).

**中文**

AgenticGEO：用于生成式引擎优化的自我进化代理系统会议缩写’XX，2018 年 6 月 3-05 日，纽约州伍德斯托克 A 补充信息 A.1 方法细节 A.1.1 图 1 的说明。对于每个实例，我们运行九个重写策略并获得它们的平均总分 {𝑟𝑖 }9 𝑖=1，其中最好分 𝑟 ★ =最大𝑖𝑟𝑖。我们量化有多少策略相对于最佳策略仍然具有竞争力。如果策略至少达到 𝑟 ★ 的 55%（相当于，其与 𝑟 ★ 的差距不超过 𝑟 ★ 的 45%），则该策略被认为接近最优。

### 段落 116 · Page 11

**EN**

Sensitivity is defined as the complement of this near-optimal fraction: Sensitivity=1− 1 9 9∑︁ 𝑖=1 I  𝑟𝑖 ≥0.55𝑟 ★ ∈ [0,1]. Higher values indicate that only a few strategies are competitive (high sensitivity), whereas lower values suggest many strategies perform similarly well (low sensitivity). With normalized sensitivity on the x-axis and maximum gain on the y-axis, we split instances into four regions.(i) Robustly Optimizable: many strategies achieve similarly high gains.(ii) Strategy- Dependent: high gains exist, but only a few strategies work well.

**中文**

灵敏度被定义为这个接近最优分数的补集： Sensitivity=1− 1 9 9Σ︁ 𝑖=1 I 𝑟𝑖 ≥0.55𝑟 ★ ε [0,1]。较高的值表明只有少数策略具有竞争力（高敏感性），而较低的值表明许多策略表现相似（低敏感性）。通过 x 轴上的归一化灵敏度和 y 轴上的最大增益，我们将实例分为四个区域。(i) 鲁棒可优化：许多策略实现类似的高增益。(ii) 策略相关：存在高增益，但只有少数策略效果良好。

### 段落 117 · Page 11

**EN**

(iii) Optimization-Resistant: strategies behave similarly and gains remain small.(iv) Low-Yield & Volatile: outcomes vary widely, yet the best gain is still small. The figure gives us two insights. First, GEO is instance-dependent, so a fixed strategy pool is unreliable. Second,Strategy-Dependent region motivates content-conditioned strategy selection. A.1.2 Cited answer output.The engine output is a cited answer A={(𝑦 𝑖,C 𝑖 )} 𝐿−1 𝑖=0 , where 𝐿 is the number of generated sentences, 𝑦𝑖 is the 𝑖-th sentence, and C𝑖 ⊆ { 1, . . . , 𝑛} denotes the indices of candidate documents cited in 𝑦𝑖.

**中文**

(iii) 抗优化：策略表现相似，收益仍然很小。(iv) 低收益和波动性：结果差异很大，但最佳收益仍然很小。该图给了我们两个启示。首先，GEO 是依赖于实例的，因此固定的策略池是不可靠的。其次，策略依赖区域激发内容条件策略选择。 A.1.2 引用答案输出。引擎输出是引用答案 A={(𝑦 𝑖,C 𝑖 )} 𝐿−1 𝑖=0，其中 𝐿 是生成的句子数，𝑦𝑖 是第 𝑖 句子，C𝑖 ⊆ { 1, .。。 , 𝑛} 表示 𝑦𝑖 中引用的候选文档的索引。

### 段落 118 · Page 11

**EN**

Let 𝑗★ denote the index of the optimized content 𝑑 ′ within the candidate set. To standardize E’s cited-answer generation, we use the following prompt template. Engine Answer Synthesis Prompt Template Write an accurate and concise answer for the given user question. using only the provided summarized web search results. The answer should be correct, high-quality, and written by an expert using an unbiased and journalistic tone. The user’s language of choice, such as English, Français, Español, or Deutsch should be used. The answer should be informative, interesting, and engaging.

**中文**

让𝑗★表示候选集中优化内容𝑑′的索引。为了标准化 E 的被引答案生成，我们使用以下提示模板。引擎答案综合提示模板为给定的用户问题编写准确简洁的答案。仅使用所提供的汇总网络搜索结果。答案应该是正确的、高质量的，并且由专家以公正的新闻语气撰写。应使用用户选择的语言，例如英语、法语、西班牙语或德语。答案应该内容丰富、有趣且有吸引力。

### 段落 119 · Page 11

**EN**

The answer’s logic and reasoning should be rigorous and defensible. Every sentence in the answer should be immediately followed by an in-line citation to the search result(s). The cited search result(s) should fully support all the information in the sentence. Search results need to be cited using [index]. When citing several search results, use [1][2][3] format rather than [1, 2, 3]. You can use multiple search results to respond comprehensively while avoiding irrelevant search results. A.1.3 Impression metrics.Following GEO-Bench [ 1], we quantify the visibility of each candidate document 𝑗∈ { 1, . . .

**中文**

答案的逻辑和推理应该是严谨的、站得住脚的。答案中的每个句子后面都应紧跟着对搜索结果的内嵌引用。引用的检索结果应完全支持句子中的所有信息。搜索结果需要使用[索引]引用。引用多个搜索结果时，请使用 [1][2][3] 格式，而不是 [1, 2, 3]。您可以使用多个搜索结果进行全面响应，同时避免不相关的搜索结果。 A.1.3 印象度量。按照 GEO-Bench [1]，我们量化每个候选文档 𝑗ε { 1, .。。

### 段落 120 · Page 11

**EN**

, 𝑛} within the generated response A={𝑦 0, . . . , 𝑦𝐿−1 } by aggregating its attributed contributions. Here, 𝑦𝑖 denotes the 𝑖-th sentence in A, and C𝑖 denotes the set of citation indices associated with 𝑦𝑖. When a sentence cites multiple candidates, its contribution is uniformly distributed by a factor of1/|C 𝑖 |. Let wc(𝑦𝑖 ) be the word count of sentence𝑦𝑖. To reflect user attention decay, we define a position weight𝑤(𝑖)for the𝑖-th sentence: 𝑤(𝑖)= ( exp − 𝑖 𝐿−1  , 𝐿>1, 1, 𝐿=1.

**中文**

, 𝑛} 在生成的响应 A={𝑦 0, .。。 , 𝑦𝐿−1 } 通过聚合其归因贡献。这里，𝑦𝑖表示A中的第𝑖句子，C𝑖表示与𝑦𝑖相关的引文索引集。当一个句子引用多个候选者时，其贡献按因子 1/|C 𝑖 | 均匀分布。令 wc(𝑦𝑖 ) 为句子𝑦𝑖 的字数。为了反映用户注意力衰减，我们为第𝑖句子定义位置权重𝑤(𝑖)：𝑤(𝑖)= ( exp − 𝑖 𝐿−1 , 𝐿>1, 1, 𝐿=1。

### 段落 121 · Page 11

**EN**

(15) We compute three impression scores:word(attributed word count),pos(citation order with position weights), andoverall(a combination of word count and position decay): Scoreword 𝑗 (𝑞, 𝑠)= 𝐿−1∑︁ 𝑖=0 I[𝑗∈ C 𝑖 ] · wc(𝑦𝑖 ) |C𝑖 | ,(16) Scorepos 𝑗 (𝑞, 𝑠)= 𝐿−1∑︁ 𝑖=0 I[𝑗∈ C 𝑖 ] · 𝑤(𝑖) |C𝑖 | ,(17) Scoreoverall 𝑗 (𝑞, 𝑠)= 𝐿−1∑︁ 𝑖=0 I[𝑗∈ C 𝑖 ] · wc(𝑦𝑖 ) ·𝑤(𝑖) |C𝑖 | .(18) The goal of GEO is to maximize the impression of the optimized content ˜𝑑 in the generative engine output A, as quantified by the above metrics. A.1.4 Seed Strategies.We initialize the critic’s offline preference alignment with 9 seed rewriting strategies.

**中文**

(15) 我们计算三个印象分数：word（归因字数）、pos（带有位置权重的引用顺序）和总体（字数和位置衰减的组合）： Scoreword 𝑗 (𝑞, 𝑠)= 𝐿−1Σ︁ 𝑖=0 I[𝑗∈ C 𝑖 ] · wc(𝑦𝑖 ) |C𝑖 | ,(16) Scorepos 𝑗 (𝑞, 𝑠)= 𝐿−1Σ︁ 𝑖=0 I[𝑗∈ C 𝑖 ] · 𝑤(𝑖) |C𝑖 | ,(17) 总分 𝑗 (𝑞, 𝑠)= 𝐿−1Σ︁ 𝑖=0 I[𝑗∈ C 𝑖 ] · wc(𝑦𝑖 ) ·𝑤(𝑖) |C𝑖 | (18) GEO 的目标是最大化生成式引擎输出 A 中优化内容 𝑑 的印象，如上述指标所量化。 A.1.4 种子策略。我们用 9 种种子重写策略来初始化评论家的离线偏好对齐。

### 段落 122 · Page 11

**EN**

Each seed prompt is a template applied to the source summary (placeholder {summary}) to produce candidate rewrites, which are then used to construct offline preference data for warm-starting the critic. Keyword Stuffing Task:Improve the source by inserting up to 10 NEW, relevant SEO keywords that are NOT already present in the text. Constraints: – Do not change, add, or remove any core information. – Keep the original structure (paragraphing, bullet points, line breaks). – Insert keywords naturally inline (no keyword list at the end). Source:summary Output:The updated source text only.

**中文**

每个种子提示都是一个应用于源摘要（占位符 {summary}）的模板，以生成候选重写，然后用于构建离线偏好数据以热启动评论家。关键字填充任务：通过插入文本中尚未存在的最多 10 个新的相关 SEO 关键字来改进源。限制： – 不得更改、添加或删除任何核心信息。 – 保留原始结构（段落、要点、换行符）。 – 自然内联插入关键字（末尾没有关键字列表）。来源：摘要输出：仅更新的源文本。

### 段落 123 · Page 11

**EN**

Unique Words Task:Revise the source by using more unique and precise vocabulary. Constraints: – Preserve the original meaning and all core information. – Do not add new claims or remove any content. – Keep the length and structure roughly the same. Source:summary Output:The revised source text only.

**中文**

独特单词任务：使用更独特和精确的词汇修改源代码。约束： – 保留原始含义和所有核心信息。 – 请勿添加新的声明或删除任何内容。 – 保持长度和结构大致相同。来源：摘要 输出：仅修订后的源文本。

### Page 12

### 段落 124 · Page 12

**EN**

Conference acronym ’XX, June 03–05, 2018, Woodstock, NY Jiaqi Yuan, Jialu Wang et al. Easy-To-Understand Task:Rewrite the source in simple, easy-to-understand language. Constraints: – Do not omit, add, or alter any core information. – Keep the original structure and roughly the same length. – Only rephrase sentences for clarity and readability. Source:summary Output:The simplified source text only. Authoritative Task:Make the source sound confident, authoritative, and expert. Constraints: – Do not add new facts or remove any information. – Keep the original structure (formatting, bullets, spacing).

**中文**

会议缩写’XX，2018 年 6 月 3-05 日，纽约州伍德斯托克，Jiaqi Yuan、Jialu Wang 等人。易于理解的任务：用简单、易于理解的语言重写源代码。限制： – 不得省略、添加或更改任何核心信息。 – 保持原来的结构和大致相同的长度。 – 仅为了清晰和可读性而改写句子。来源：摘要输出：仅简化的源文本。权威任务：让消息来源听起来自信、权威、专家。限制： – 不得添加新事实或删除任何信息。 – 保留原始结构（格式、项目符号、间距）。

### 段落 125 · Page 12

**EN**

– Strengthen tone via wording choices, not by exaggerating or making unverifiable claims. Source:summary Output:The revised source text only. Technical Words Task:Rewrite the source in a more technical style using domain-appropriate terminology. Constraints: – Preserve all core information; do not introduce new claims. – Keep the structure and length roughly unchanged. – Rephrase sentences to sound more technical and precise. Source:summary Output:The revised source text only. Fluency Optimization Task:Rewrite the source to improve fluency and coherence. Constraints: – Do not alter the core content.

**中文**

– 通过措辞选择来加强语气，而不是通过夸大或提出无法证实的主张。来源：摘要 输出：仅修订后的源文本。技术词汇任务：使用适合领域的术语以更具技术性的风格重写源代码。限制： – 保留所有核心信息；不要引入新的主张。 – 保持结构和长度大致不变。 – 重新表述句子，使其听起来更加技术性和精确性。来源：摘要 输出：仅修订后的源文本。流畅性优化任务：重写源码以提高流畅性和连贯性。限制： – 不改变核心内容。

### 段落 126 · Page 12

**EN**

– Improve sentence transitions and readability. – Keep the structure and length roughly the same. Source:summary Output:The rewritten source text only. Cite Sources Task:Strengthen credibility by adding a small number of natural-language citations to credible sources (e.g., industry reports, standards, official docs). Constraints: – Citations must be plausible and verifiable; do not fabricate sources. – Do not change the core information or add new claims. – Keep structure and length roughly the same (about 5–6 citations total). Source:summary Output:The revised source text only.

**中文**

– 改善句子转换和可读性。 – 保持结构和长度大致相同。来源：摘要输出：仅重写的源文本。引用来源任务：通过向可靠来源（例如行业报告、标准、官方文档）添加少量自然语言引用来增强可信度。限制： – 引文必须合理且可验证；请勿捏造消息来源。 – 请勿更改核心信息或添加新的声明。 – 保持结构和长度大致相同（总共约 5-6 次引用）。来源：摘要 输出：仅修订后的源文本。

### 段落 127 · Page 12

**EN**

Quotation Addition Task:Increase perceived authority by adding a few short, relevant quotations from reputable entities (e.g., well-known organizations or experts). Constraints: – Quotes must be accurate and attributable; do not invent quotes. – Do not change core content; keep structure and length similar. – Integrate quotes inline without adding long new paragraphs. Source:summary Output:The revised source text only. Statistics Addition Task:Add a few concise, relevant statistics or numerical facts to improve concreteness. Constraints: – Statistics must be verifiable; do not invent numbers.

**中文**

引用添加任务：通过添加来自信誉良好的实体（例如知名组织或专家）的一些简短的相关引用来增加感知权威。限制： – 报价必须准确且可追溯；不要发明引号。 – 不改变核心内容；保持结构和长度相似。 – 内嵌引用，无需添加长的新段落。来源：摘要 输出：仅修订后的源文本。统计添加任务：添加一些简洁的、相关的统计数据或数字事实以提高具体性。限制： – 统计数据必须可验证；不要发明数字。

### 段落 128 · Page 12

**EN**

– Do not modify core content beyond inserting stats inline. – Keep the original structure and stop at the end of the original source. Source:summary Output:The revised source text only. A.1.5 Genotype Details.We formalize the evolving strategy as a structured genotype 𝑔=⟨𝑔 𝐼 , 𝑔𝐶, 𝑔𝑅, 𝑔𝐹 , 𝑔𝑇 ⟩. To interface efficiently with the Critic and the Generative Engine, we implement two deterministic rendering functions𝑅 crit and𝑅 eng : 1. Compact Summary for Critic ( 𝑅crit).To minimize token consumption while retaining discriminative features, 𝑅crit (𝑔) maps the genotype to a concatenated string of active categorical values.

**中文**

– 除了内联插入统计数据外，请勿修改核心内容。 – 保留原始结构并在原始源的末尾停止。来源：摘要 输出：仅修订后的源文本。 A.1.5 基因型细节。我们将进化策略形式化为结构化基因型 𝑔=⟨𝑔 𝐼 , 𝑔𝐶, 𝑔𝑅, 𝑔𝐹 , 𝑔𝑇 ⟩。为了与 Critic 和生成式引擎有效交互，我们实现了两个确定性渲染函数𝑅 crit 和 𝑅 eng： 1. Critic 的紧凑摘要 (𝑅crit)。为了在保留区分性特征的同时最大限度地减少标记消耗，𝑅crit (𝑔) 将基因型映射到活动分类值的串联字符串。

### 段落 129 · Page 12

**EN**

Formally, let Kactive ⊂𝑔 be the set of non-empty discrete fields (e.g., tone labels, format types). The rendering is defined as: 𝑅crit (𝑔)= Ê 𝑘∈ Kactive (Name(𝑘)||":"||Val(𝑘) ) ,(19) where ⊕ denotes string concatenation with delimiters. For example, a strategy might be rendered as “Tone:Assertive|Format:List| Constraint:Anti-Hallucination”. 2. Full Prompt for Engine (𝑅eng). 𝑅eng (𝑔) acts as a template-filling function that constructs the executable meta-prompt.

**中文**

形式上，令 Kactive ⊂𝑔 为非空离散字段的集合（例如，音调标签、格式类型）。渲染定义为： 𝑅crit (𝑔)= Ê 𝑘ε Kactive (Name(𝑘)||":"||Val(𝑘) ) ,(19) 其中 ⊕ 表示带分隔符的字符串连接。例如，策略可能会呈现为“语气：断言|格式：列表|约束：反幻觉”。 2. 引擎完整提示（𝑅eng）。 𝑅eng (𝑔) 充当模板填充函数，构造可执行的元提示符。

### 段落 130 · Page 12

**EN**

It wraps the raw text of each gene component into specific sections: 𝑅eng (𝑔)=T sys ⊕𝑔 𝐼 ⊕ Tcons (𝑔𝐶 ) ⊕ Treason(𝑔𝑅) ⊕ Tfmt (𝑔𝐹 ) ⊕ Ttone (𝑔𝑇 ), (20) where T represents fixed instructional templates (e.g., “Adhere to the following constraints: ...”). This full prompt is then combined with the query 𝑞 and content 𝑑 to form the final input for the rewriting model.

**中文**

它将每个基因组件的原始文本包装成特定的部分： 𝑅eng (𝑔)=T sys ⊕𝑔 𝐼 ⊕ Tcons (𝑔𝐶 ) ⊕ Treason(𝑔𝑅) ⊕ Tfmt (𝑔𝐹 ) ⊕ Ttone (𝑔𝑇 )， (20) 其中 T 代表固定的教学模板（例如，“遵守以下约束：……”）。然后，将此完整提示与查询𝑞和内容𝑑结合起来，形成重写模型的最终输入。

### Page 13

### 段落 131 · Page 13

**EN**

AgenticGEO: A Self-Evolving Agentic System for Generative Engine Optimization Conference acronym ’XX, June 03–05, 2018, Woodstock, NY A.1.6 MAP-Elites Descriptors and Archive Gates.The strategy space is discretized into behavioral cells via a descriptor function𝜓 : G → Z𝐷. Based on our design, 𝜓(𝑔) maps a genotype to a tuple of 12 discrete dimensions : •Core Types:strategy_type,output_schema. • Switches: has_self_check, has_reasoning, has_conflict_res, use_code_block,has_prelude,has_post_check. • Buckets: tone_bucket, constraint_strength, length_policy, reasoning_steps_bucket.

**中文**

AgenticGEO：用于生成式引擎优化的自我进化代理系统会议首字母缩略词’XX，2018年6月3日至5日，纽约州伍德斯托克 A.1.6 MAP-精英描述符和存档门。策略空间通过描述符函数𝜓：G→Z𝐷离散化为行为单元。根据我们的设计，𝜓(𝑔) 将基因型映射到 12 个离散维度的元组： •核心类型：strategy_type、output_schema。 • 开关：has_self_check、has_reasoning、has_conflict_res、use_code_block、has_prelude、has_post_check。 • 存储桶：tone_bucket、constraint_strength、length_policy、reasoning_steps_bucket。

### 段落 132 · Page 13

**EN**

A candidate strategy 𝑠 (with genotype 𝑔) is mapped to a cell index 𝑐=𝜓(𝑔). It is admitted only if it passes two gates: 1. Novelty Gate (De-duplication).We de-duplicate candidates using character-level 𝑛-gram Jaccard similarity computed on the rendered strategy summaries. The similarity between a candidate 𝑠 and an existing elite𝑒is: Sim(𝑠, 𝑒)= |𝑛-grams(𝑠) ∩𝑛-grams(𝑒)| |𝑛-grams(𝑠) ∪𝑛-grams(𝑒)| .(21) The candidate is rejected if it is too similar to any strategy already stored in the target cell: max 𝑒 Sim(𝑠, 𝑒)>0.9, which prevents near-duplicates. 2. Value Gate (Performance).If the target cell is not full ( <𝐾 𝑐 strategies), 𝑠 is admitted.

**中文**

候选策略 𝑠（具有基因型 𝑔）被映射到细胞索引 𝑐=𝜓(𝑔)。仅当它通过两个门时才被承认： 1.新颖性门（重复数据删除）。我们使用根据渲染的策略摘要计算的字符级𝑛-gram Jaccard相似度来删除重复候选者。候选𝑠和现有精英𝑒之间的相似度是： Sim(𝑠, 𝑒)= |𝑛-grams(𝑠) ∩𝑛-grams(𝑒)| |𝑛-克(𝑠) ∪𝑛-克(𝑒)| (21) 如果候选者与目标单元格中​​已存储的任何策略太相似，则该候选者将被拒绝：max 𝑒 Sim(𝑠, 𝑒)>0.9，这可以防止接近重复。 2. 价值门（性能）。如果目标单元未满（<𝐾𝑐策略），𝑠被接纳。

### 段落 133 · Page 13

**EN**

Otherwise, it must beat the current worst strategy in that cell. A.1.7 PND Score Formulation and Pruning.We maintain the archive using aPND scorethat balances effectiveness and exploration: 𝑆PND (𝑠)=𝑟(𝑠) +𝜆 pnd Nov(𝑠) +Div(𝑠) ,(22) where 𝑟(𝑠) is the impression score gain evaluated by the critic or GE. Novelty (Nov). Nov(𝑠) encourages population coverage by rewarding strategies that are structurally dissimilar to those already stored in the current archiveM(using similarity metric as Eq. (21)). Diversity ( Div).

**中文**

否则，它必须击败该单元中当前最差的策略。 A.1.7 PND 分数制定和修剪。我们使用平衡有效性和探索性的 PND 分数来维护档案： 𝑆PND (𝑠)=𝑟(𝑠) +𝜆 pnd Nov(𝑠) +Div(𝑠) ,(22) 其中 𝑟(𝑠) 是评论家或 GE 评估的印象分数增益。新奇（十一月）。 Nov(𝑠) 通过奖励结构上与当前 archiveM 中已存储的策略不同的策略来鼓励人口覆盖（使用相似性度量如方程（21））。多样性（分区）。

### 段落 134 · Page 13

**EN**

Div(𝑠) promotes diverse evolutionary trajectories by favoring strategies with richer lineage history (e.g., deeper generations), more varied mutation operators, and less degenerate genotypes (more fields actively used). A.1.8 Evolver Action Space and Prompting.The Evolver 𝜋𝜓 functions as a meta-optimizer that proposes improvements to existing strategies. It takes as input an instance 𝑥=(𝑞, 𝑑) , a primary parent 𝑔𝐴, an optional secondary parent𝑔𝐵 (for crossover), and an operator catalogΩ. Operator Catalog ( Ω).To ensure diverse and controllable evolution,Ωconsists of two categories of symbolic operators.

**中文**

Div(𝑠) 通过支持具有更丰富的谱系历史（例如，更深的世代）、更多样的突变算子和更少的简并基因型（更多领域被积极使用）的策略来促进多样化的进化轨迹。 A.1.8 Evolver 动作空间和提示。Evolver 𝜋𝜓 充当元优化器，对现有策略提出改进建议。它以实例 𝑥=(𝑞, 𝑑)、主要父对象 𝑔𝐴、可选的次要父对象𝑔𝐵（用于交叉）和操作符catalogΩ 作为输入。算子目录（Ω）。为了保证演化的多样性和可控性，Ω由两类符号算子组成。

### 段落 135 · Page 13

**EN**

Mutation Operatorsapply field-level perturbations targeting specific dimensions, such asmut_C_strengthen(adding constraints), mut_T_toggle_tone (switching styles), and mut_F_schema_swap (changing output format). Crossover Operatorssynthesize features from two parents, including cx_swap_gene (exchanging gene blocks) andcx_conflict_synthesis(resolving conflicts between Parent A and B). Action Proposal.The Evolver outputs 𝑀 candidate actions. Each action is a strict JSON object𝑎={operator_id,child_genotype} , where child_genotype is the full structure resulting from applying the selected operator.

**中文**

变异算子针对特定维度应用字段级扰动，例如 mut_C_strengthen（添加约束）、mut_T_toggle_tone（切换样式）和 mut_F_schema_swap（更改输出格式）。交叉算子合成来自两个父代的特征，包括cx_swap_gene（交换基因块）和cx_conflict_synthesis（解决父代A和B之间的冲突）。行动提案。Evolver 输出 𝑀 候选行动。每个操作都是一个严格的 JSON 对象𝑎={operator_id,child_genotype}，其中 child_genotype 是应用所选运算符所产生的完整结构。

### 段落 136 · Page 13

**EN**

Evolver Action Proposal Prompt Template System: You are a prompt evolution agent for GEO. You must evolve a parent strategy (or combine two parents) into a better STRUCTURED GENOTYPE JSON (I/C/R/F/T). 1) Choose an operator_id from the provided catalog. 2) Produce a child_genotype JSON that results from applying that operator. Important constraints: - The output MUST be valid JSON (one object per line). - The child genotype MUST preserve the I/C/R/F/T structure. - If choosing a Crossover operator (starts with "cx_ "): You MUST conceptually combine Parent A and Parent B. - If Parent B is NOT provided: Do NOT choose any "cx_ *" operator.

**中文**

Evolver行动提案提示模板系统：您是GEO的提示进化代理。您必须将父策略（或将两个父策略合并）发展为更好的结构化基因型 JSON (I/C/R/F/T)。 1) 从提供的目录中选择一个operator_id。 2) 生成应用该运算符所产生的 child_genotype JSON。重要限制： - 输出必须是有效的 JSON（每行一个对象）。 - 子基因型必须保留 I/C/R/F/T 结构。 - 如果选择交叉运算符（以“cx_”开头）：您必须在概念上组合父级 A 和父级 B。 - 如果未提供父级 B：请勿选择任何“cx_ *”运算符。

### 段落 137 · Page 13

**EN**

- Prefer DIVERSITY: Avoid repeating the same operator across candidates. User: ## Query {query} ## Document Summary {content_summary} ## Parent Genotype A (JSON) {parent_genotype_json} ## Parent Genotype B (JSON) [Optional] {parent_b_genotype_json} ## Operator Catalog {operator_catalog} ## Task Generate {num_candidates} candidates. Output exactly {num_candidates} JSON lines.

**中文**

- 偏好多样性：避免在候选人之间重复使用相同的操作符。用户：## 查询 {query} ## 文档摘要 {content_summary} ## 父基因型 A (JSON) {parent_genotype_json} ## 父基因型 B (JSON) [可选] {parent_b_genotype_json} ## 操作员目录 {operator_catalog} ## 任务 生成 {num_candidates} 个候选者。准确输出 {num_candidates} JSON 行。

### 段落 138 · Page 13

**EN**

A.2 Experiment Details A.2.1 Dataset.To comprehensively evaluate AgenticGEO, we conduct experiments across three datasets characterized by distinct content distributions and optimization goals: • GEO-Bench (In-Domain): This serves as our primary dataset for training the evolver and critic, as well as for in-domain evaluation. Constructed from real-world Google Search results, it covers a wide spectrum of domains (e.g., Science, History, Health) with varying query difficulties. The content primarily consists of long-form articles, providing rich context for learning diverse optimization strategies.

**中文**

A.2 实验细节 A.2.1 数据集。为了全面评估 AgenticGEO，我们在三个具有不同内容分布和优化目标的数据集上进行实验： • GEO-Bench（域内）：这是我们用于训练进化者和批评者以及域内评估的主要数据集。它根据现实世界的 Google 搜索结果构建，涵盖了具有不同查询难度的广泛领域（例如科学、历史、健康）。内容主要由长篇文章组成，为学习各种优化策略提供丰富的背景。

### 段落 139 · Page 13

**EN**

• MS MARCO (Out-of-Domain): To assess zero-shot transferability, we employ the MS MARCO Passage Ranking dataset. Derived from Bing search logs, this dataset comprises real user queries paired with short, often unstructured text passages. Evaluating on this dataset tests whether our optimization policy can generalize to short-text scenarios and unseen query distributions without re-training. • E-commerce (Vertical Domain): Representing a specific vertical application, this dataset is sourced from Amazon product descriptions and reviews. The optimization goal here shifts from informational retrieval to commercial visibility.

**中文**

• MS MARCO（域外）：为了评估零样本可迁移性，我们采用MS MARCO Passage Ranking 数据集。该数据集源自 Bing 搜索日志，包含真实的用户查询以及简短的、通常是非结构化的文本段落。对此数据集的评估测试我们的优化策略是否可以推广到短文本场景和未见过的查询分布而无需重新训练。 • 电子商务（垂直领域）：代表特定的垂直应用，该数据集源自亚马逊产品描述和评论。这里的优化目标从信息检索转向商业可见性。

### 段落 140 · Page 13

**EN**

This dataset challenges the agent to adapt to entity-centric content and the specific structural preferences of product-related queries. Table 5 reports the key statistics of the three datasets. Following the GEO-Bench protocol, we standardize the retrieval context by pairing each query with five documents, ensuring a consistent document budget across datasets for fair comparison. A.2.2 Baselines.

**中文**

该数据集要求代理适应以实体为中心的内容以及产品相关查询的特定结构偏好。表 5 报告了三个数据集的关键统计数据。遵循 GEO-Bench 协议，我们通过将每个查询与五个文档配对来标准化检索上下文，确保跨数据集的文档预算一致，以进行公平比较。 A.2.2 基线。

### Page 14

### 段落 141 · Page 14

**EN**

Conference acronym ’XX, June 03–05, 2018, Woodstock, NY Jiaqi Yuan, Jialu Wang et al. Table 5: Dataset statistics after preprocessing. Following the GEO-Bench protocol, each query is paired with5documents. Dataset #Queries #Docs Avg. Content Tokens GEO-Bench 1000 5,000 980.61 MS-Marco 1000 5,000 91.91 E-commerce 416 2,180 1,459.69 1. Static Heuristics (GEO-Bench).We implement the nine official strategies from GEO-Bench [1], covering lexical, stylistic, and evidence-based modifications: • No Optimization:The original, unmodified source content serves as the control group.

**中文**

会议缩写’XX，2018 年 6 月 3-05 日，纽约州伍德斯托克，Jiaqi Yuan、Jialu Wang 等人。表 5：预处理后的数据集统计数据。遵循 GEO-Bench 协议，每个查询都与 5 个文档配对。数据集 #Queries #Docs 平均值内容代币 GEO-Bench 1000 5,000 980.61 MS-Marco 1000 5,000 91.91 电子商务 416 2,180 1,459.69 1. 静态启发式（GEO-Bench）。我们实施 GEO-Bench [1] 的九个官方策略，涵盖词汇、文体和基于证据的修改： • 无优化：原始的、未修改的源内容作为对照组。

### 段落 142 · Page 14

**EN**

• Keyword Stuffing:Naively injects query keywords repeatedly to increase term frequency. • Unique Words:Inserts rare vocabulary to artificially increase information entropy. • Easy-To-Understand:Simplifies sentence structures to improve readability for general audiences. • Authoritative:Adopts a confident and professional tone to mimic expert knowledge. • Technical Words:Injects domain-specific jargon assuming engines prefer specialized vocabulary. • Fluency Optimization:Polishes the text for grammatical correctness without adding information. • Cite Sources:Injects plausible citations to external authorities to enhance credibility.

**中文**

• 关键字堆砌：天真地重复注入查询关键字以增加术语频率。 • 独特词汇：插入稀有词汇，人为增加信息熵。 • 易于理解：简化句子结构以提高一般受众的可读性。 • 权威：采用自信、专业的语气模仿专家知识。 • 技术词汇：假设引擎更喜欢专业词汇，则注入特定领域的术语。 • 流畅性优化：在不添加信息的情况下润色文本以确保语法正确性。 • 引用来源：向外部权威机构注入可信的引用以提高可信度。

### 段落 143 · Page 14

**EN**

• Quotation Addition:Embeds direct quotes from relevant entities to support claims. • Statistics Addition:Enriches the text with quantitative data points relevant to the query. 2. State-of-the-Art. • AutoGEO [ 54]:A representative automated framework that distills generative engine preferences from LLM-generated explanations into static rewriting rules. To reimplement the method, we use the GEO-Bench training dataset on the generative engine of Qwen2.5-32B-Instruct following the source code of AutoGEO. 3.

**中文**

• 引用添加：嵌入相关实体的直接引用以支持声明。 • 统计添加：使用与查询相关的定量数据点来丰富文本。 2. 最先进的。 • AutoGEO [54]：一个代表性的自动化框架，它将从LLM生成的解释中提取生成式引擎偏好为静态重写规则。为了重新实现该方法，我们按照 AutoGEO 的源代码，在 Qwen2.5-32B-Instruct 的生成式引擎上使用 GEO-Bench 训练数据集。 3.

### 段落 144 · Page 14

**EN**

Supervised Fine-Tuning (SFT).To compare with learningto-rewrite baselines, we fine-tune a rewriter on supervised pairs (where the target rewrites are selected based on overall score), targeting a single heuristic style, yielding controllable specialized rewriters: • Cite Sources-SFT:Fine-tunes a rewriter to produce citationenriched rewrites in the style ofCite Sources. • Quotation Addition-SFT:Fine-tunes a rewriter to add concise supporting quotations in the style ofQuotation Addition. • Statistics Addition-SFT:Fine-tunes a rewriter to insert relevant numeric statements in the style ofStatistics Addition.

**中文**

监督微调（SFT）。为了与学习重写基线进行比较，我们在监督对上微调重写器（其中根据总体分数选择目标重写），针对单一启发式风格，产生可控的专门重写器： • 引用来源-SFT：微调重写器以产生引用来源风格的引文丰富的重写器。 • 引用添加-SFT：微调重写器，以引用添加的风格添加简洁的支持引用。 • 统计加法-SFT：微调重写器以统计加法的风格插入相关的数字语句。

### 段落 145 · Page 14

**EN**

A.2.3 Hyper Parameters.Key hyperparameters are in Table 6. A.3 Theoretical Analysis To establish the bound, we make the standard assumptions for online convex optimization: (1) Boundedness & Lipschitz Continuity:The true risk function R (·) and the critic C𝑡 (·) are bounded in [0, 𝐵] and are Table 6: Key hyperparameters of AgenticGEO (values left blank). Module Param.

**中文**

A.2.3 超参数。关键超参数见表 6。 A.3 理论分析 为了建立界限，我们对在线凸优化做出标准假设： (1) 有界性和 Lipschitz 连续性：真实风险函数 R (·) 和批评函数 C𝑡 (·) 在 [0, 𝐵] 内有界，表 6：AgenticGEO 的关键超参数（值留空）。模块参数

### 段落 146 · Page 14

**EN**

Description Value Offline Critic Alignment Loss weight𝜆Weight in𝐿 total =𝐿 pair +𝜆𝐿 reg 0.2 Warm-up steps𝑆 freeze Epochs with frozen backbone before unfreezing 1 Online Co-Evolution (Selection & Budget) Iterations𝑇Total online evolution iterations 100 Exploit size𝐾 top Top-𝐾top selected by critic 4 Explore size𝐾 rand Randomly sampled strategies per iteration 4 Evolver Learning (Sibling-Aware A WR) Sibling coeff.𝛼 sib Strength of sibling-aware baseline 0.8 AWR temperature𝛽Temperature inexp(𝐴/𝛽)weighting 1.0 Archive Maintenance (MAP-Elites & Gates) PND weight𝜆 pnd Weight of novelty/diversity term in𝑆 PND 0.3 Cell capacity𝐾 𝑐 Max items stored pe

**中文**

描述 值 离线评论家对齐 损失权重𝜆权重𝐿总计=𝐿对 +𝜆𝐿 reg 0.2 热身步骤𝑆 在解冻之前冻结具有冻结主干的纪元 1 在线共同进化（选择和预算）迭代𝑇总在线进化迭代 100 漏洞利用大小𝐾 top Top-𝐾top 由评论家选择 4 探索size𝐾 rand 每次迭代随机采样策略 4 Evolver Learning (Sibling-Aware A WR) Sibling coeff.𝛼 sib 兄弟姐妹感知基线的强度 0.8 AWR 温度𝛽温度 inexp(𝐴/𝛽) 权重 1.0 档案维护 (MAP-精英和盖茨) PND 权重𝜆 pnd 𝑆 PND 中新颖性/多样性术语的权重0.3 电池容量𝐾 𝑐 最大存储物品数

### 段落 147 · Page 14

**EN**

r archive cell 3 Implementation LR (critic)𝜂 𝑐 Learning rate for critic fine-tuning 0.001 LR (evolver)𝜂 𝑒 Learning rate for evolver fine-tuning 0.0002 Batch size𝐵Batch size for fine-tuning 2 LoRA rank𝑟LoRA rank 16 LoRA scaling𝛼 lora LoRA scaling factor 32 LoRA dropout𝑝 lora LoRA dropout 0.05 Epochs𝐸Fine-tuning epochs 2 𝐿-Lipschitz continuous with respect to the strategy parameters.

**中文**

r archive cell 3 实现 LR (critic)𝜂 𝑐 批评者微调的学习率 0.001 LR (evolver)𝜂 𝑒 进化者微调的学习率 0.0002 批量大小𝐵微调的批量大小 2 LoRA 等级𝑟LoRA 等级 16 LoRA 缩放𝛼 lora LoRA 缩放因子 32 LoRA dropout𝑝 lora LoRA dropout 0.05 Epochs𝐸微调 epochs 2 𝐿-Lipschitz 相对于策略参数连续。

### 段落 148 · Page 14

**EN**

(2) Critic Generalization:The critic is trained on an accumulating datasetB 𝑡 . Lemma A.1 (Linear Growth of Replay Buffer).Let 𝐾= |S (𝑡) select | denote the constant number of candidate strategies selected for ground-truth evaluation at iteration 𝑡. Assume that each candidate strategy has an independent success probability 𝑝. Only successful strategies will be added to the replay buffer B𝑇 . For any0 <𝛿< 1, with probility at least1 −𝛿, the size of the replay buffer can be bounded by: |B𝑇 | 𝑝𝐾𝑇 −1 ≤ √︄ log( 2 𝛿 ) 3𝑝𝐾𝑇 (23) Proof.

**中文**

(2) 批评家泛化：批评家接受累积数据集 B 𝑡 的训练。引理 A.1（重放缓冲区的线性增长）。让 𝐾= |S (𝑡) 选择 |表示在迭代 𝑡 时选择用于地面实况评估的候选策略的恒定数量。假设每个候选策略都有独立的成功概率 𝑝。只有成功的策略才会被添加到重放缓冲区 B𝑇 中。对于任何 0 <𝛿< 1，概率至少为 1 −𝛿，重放缓冲区的大小可以由以下限制： |B𝑇 | 𝑝𝐾𝑇 −1 ≤ √︄ log( 2 𝛿 ) 3𝑝𝐾𝑇 (23) 证明。

### 段落 149 · Page 14

**EN**

Let 𝑋𝑡,𝑖 be an indicator random variable representing the success of the 𝑖-th candidate strategy at iteration 𝑡, where 𝑡∈ {1, . . . , 𝑇} and 𝑖∈ { 1, . . . , 𝐾}. By assumption, 𝑋𝑡,𝑖 are i.i.d. Bernoulli variables with parameter 𝑝. The replay buffer size can be written as |B𝑇 |= 𝑇∑︁ 𝑡=1 𝐾∑︁ 𝑖=1 𝑋𝑡,𝑖 .(24) Hence, the expected size of the buffer is: 𝜇:=E[|B𝑇|]= 𝑇∑︁ 𝑡=1 𝐾∑︁ 𝑖=1 E[𝑋𝑡,𝑖 ]=𝑇·𝐾·𝑝.(25) By the standard Chernoff bound, for any𝜖∈ (0,1), P |B𝑇 | −𝜇 ≥𝜖𝜇  ≤2𝑒 − 𝜖2 𝜇 3 .(26) Setting the right-hand side equal to𝛿and solving for𝜖yields 𝜖= √︄ 3 log( 2 𝛿 ) 𝜇 (27)

**中文**

令 𝑋𝑡,𝑖 为指示随机变量，代表迭代 𝑡 中第 𝑖 个候选策略的成功，其中 𝑡 ∈ {1, .。。 , 𝑇} 和 𝑖ε { 1, .。。，𝐾}。根据假设，𝑋𝑡，𝑖 是独立同分布的。带参数 𝑝 的伯努利变量。重播缓冲区大小可以写为 |B𝑇 |= 𝑇Σ︁ 𝑡=1 𝐾Σ︁ 𝑖=1 𝑋𝑡,𝑖。(24) 因此，缓冲区的预期大小为： 𝜇:=E[|B𝑇|]= 𝑇Σ︁ 𝑡=1 𝐾Σ︁ 𝑖=1 E[𝑋𝑡,𝑖 ]=𝑇·𝐾·𝑝。(25) 根据标准 Chernoff 界，对于任意𝜖ε (0,1)，P |B𝑇 | −𝜇 ≥𝜖𝜇 ≤2𝑒 − 𝜖2 𝜇 3 .(26) 令右侧等于𝛿并求解𝜖，得到 𝜖= √︄ 3 log( 2 𝛿 ) 𝜇 (27)

### Page 15

### 段落 150 · Page 15

**EN**

AgenticGEO: A Self-Evolving Agentic System for Generative Engine Optimization Conference acronym ’XX, June 03–05, 2018, Woodstock, NY Substituting𝜇=𝑝𝐾𝑇, we have P |B𝑇 | 𝑝𝐾𝑇 −1 ≥ √︄ 3 log( 2 𝛿 ) 𝜇  ≤𝛿 .(28) □ Lemma A.2 (Critic Generalization Bound).Suppose the critic is learned from the replay buffer B𝑇 , and the hypothesis class F has bounded Rademacher complexity. Under the assumption of Lemma A.1, for any𝛿∈ (0,1), with probability at least1−𝛿, |C𝑇 (𝑠) − R (𝑠)| ≤ 1√ 𝑇 2𝑀F √︄ 2 𝑝𝐾 +𝐵 √︄ log(2/𝛿) 𝑝𝐾 ! (29) Proof.

**中文**

AgenticGEO：用于生成式引擎优化的自我进化代理系统会议缩写’XX，2018 年 6 月 3 日至 5 日，纽约州伍德斯托克𝑝𝐾𝑇 −1 ≥ √︄ 3 log( 2 𝛿 ) 𝜇 ≤𝛿 .(28) □ 引理 A.2（批评家泛化界限）。假设批评家是从重播缓冲区 B𝑇 中学习的，并且假设类 F 限制了 Rademacher 复杂度。在引理 A.1 的假设下，对于任何𝛿ε (0,1)，概率至少为 1−𝛿，|C𝑇 (𝑠) − R (𝑠)| ≤ 1√ 𝑇 2𝑀F √︄ 2 𝑝𝐾 +𝐵 √︄ log(2/𝛿) 𝑝𝐾 ! (29)证明。

### 段落 151 · Page 15

**EN**

The universal convergence bound states that with probability at least1− 𝛿 2 , the generalization error is bounded by |C𝑇 (𝑠) − R (𝑠)| ≤2ℜ | B𝑇 | (F ) +𝐵 √︄ log(2/𝛿) 2|B𝑇 | .(30) where ℜ| B𝑇 | ≤ 𝑀F | B𝑇 | is the Rademacher complexity. From Lemma A.1, with probability at least1− 𝛿 2 , the buffer size |B𝑇 | ≥ (1−𝜖 𝑇 )𝑝𝐾𝑇(31) Substitute into the above generalization bound, we have with probability at least1−𝛿 |C𝑇 (𝑠) − R (𝑠)| ≤ 1√ 𝑇 · 1√1−𝜖 𝑇 2𝑀F √︄ 1 𝑝𝐾 +𝐵 √︄ log(2/𝛿) 2𝑝𝐾 ! (32) For sufficiently large 𝑇 such that 𝑇≥ 8 log(2/𝛿) 𝑝𝐾 , we have 𝜖𝑇 ≤ 1 2 . Then we will have |C𝑇 (𝑠) − R (𝑠)| ≤ 1√ 𝑇 · 1√︃ 1− 1 2 2𝑀F √︄ 1 𝑝𝐾 +𝐵 √︄ log(2/𝛿) 2𝑝𝐾 !

**中文**

通用收敛界指出，以至少 1− 𝛿 2 的概率，泛化误差的边界为 |C𝑇 (𝑠) − R (𝑠)| ≤2ℜ | B𝑇 | (F ) +𝐵 √︄ log(2/𝛿) 2|B𝑇 | .(30) 其中 ℜ| B𝑇 | ≤ 𝑀F | B𝑇 |是拉德马赫复杂度。根据引理 A.1，缓冲区大小 |B𝑇 | 的概率至少为 1− 𝛿 2。 ≥ (1−𝜖 𝑇 )𝑝𝐾𝑇(31) 代入上述泛化界限，我们至少有 1−𝛿 |C𝑇 (𝑠) − R (𝑠)| 的概率≤ 1√ 𝑇 · 1√1−𝜖 𝑇 2𝑀F √︄ 1 𝑝𝐾 +𝐵 √︄ log(2/𝛿) 2𝑝𝐾 ! (32) 对于足够大的 𝑇 使得 𝑇≥ 8 log(2/𝛿) 𝑝𝐾，我们有 𝜖𝑇 ≤ 1 2。那么我们将有 |C𝑇 (𝑠) − R (𝑠)| ≤ 1√ 𝑇 · 1√︃ 1− 1 2 2𝑀F √︄ 1 𝑝𝐾 +𝐵 √︄ log(2/𝛿) 2𝑝𝐾 !

### 段落 152 · Page 15

**EN**

= 1√ 𝑇 2𝑀F √︄ 2 𝑝𝐾 +𝐵 √︄ log(2/𝛿) 𝑝𝐾 ! This bound implies that the approximation error converges as O ( 1√ 𝑇 ).□ Lemma A.3 (Evolver Regret Bound).Let C𝑡 : S →R denote the risk predicted by the critic at iteration 𝑡. Assume that C𝑡 is convex and 𝐿-Lipschitz continuous over the strategy space S with diameter 𝐷. Suppose the Evolver updates the strategy 𝑠𝑡 via a gradient-based update with step size 𝜂. Then, for any comparator strategy 𝑠∗ ∈ S , the cumulative regret with respect to the critic’s predictions satisfies 𝑇∑︁ 𝑡=1 C𝑡 (𝑠𝑡 ) − C𝑡 (𝑠∗) ≤𝐷𝐿 √ 𝑇=O ( √ 𝑇),(33) provided that the step size is chosen as𝜂= 𝐷 𝐿 √ 𝑇 . Proof.

**中文**

= 1√ 𝑇 2𝑀F √︄ 2 𝑝𝐾 +𝐵 √︄ log(2/𝛿) 𝑝𝐾 !这个界限意味着近似误差收敛为 O ( 1√ 𝑇 )。□ 引理 A.3 (Evolver Regret Bound)。令 C𝑡 : S →R 表示批评者在迭代 𝑡 时预测的风险。假设 C𝑡 是凸的，并且𝐿-Lipschitz 在直径为 𝐷 的策略空间 S 上连续。假设 Evolver 通过步长为 𝜂 的基于梯度的更新来更新策略 𝑠𝑡。然后，对于任何比较策略 𝑠* ∈ S，相对于评论家预测的累积遗憾满足 𝑇Σ︁ 𝑡=1 C𝑡 (𝑠𝑡 ) − C𝑡 (𝑠*) ≤𝐷𝐿 √ 𝑇=O ( √ 𝑇),(33) 前提是步骤大小选择为𝜂= 𝐷 𝐿 √ 𝑇。证明。

### 段落 153 · Page 15

**EN**

The evolver updates the strategy with gradient-based approach: 𝑠𝑡+1 =𝑠 𝑡 −𝜂𝑔 𝑡,where𝑔 𝑡 =∇C 𝑡 (𝑠𝑡 ).(34) For any𝑠 ∗, we have ∥𝑠𝑡+1 −𝑠 ∗ ∥2 ≤ ∥ (𝑠𝑡 −𝜂𝑔 𝑡 ) −𝑠 ∗ ∥2.(35) We expand the RHS: ∥𝑠𝑡 −𝜂𝑔 𝑡 −𝑠 ∗ ∥2 =∥𝑠 𝑡 −𝑠 ∗ ∥2 −2𝜂⟨𝑔 𝑡 , 𝑠𝑡 −𝑠 ∗⟩ +𝜂 2 ∥𝑔𝑡 ∥2 (36) Rearranging this inequality: 2𝜂⟨𝑔𝑡, 𝑠𝑡 −𝑠 ∗⟩ ≤ ∥𝑠 𝑡 −𝑠 ∗ ∥2 − ∥𝑠 𝑡+1 −𝑠 ∗ ∥2 +𝜂 2 ∥𝑔𝑡 ∥2 (37) Dividing by2𝜂, we obtain ⟨𝑔𝑡 , 𝑠𝑡 −𝑠 ∗⟩ ≤ 1 2𝜂 ∥𝑠𝑡 −𝑠 ∗ ∥2 − ∥𝑠 𝑡+1 −𝑠 ∗ ∥2 + 𝜂 2 ∥𝑔𝑡 ∥2 (38) From the first-order inequality, we have C𝑡 (𝑠𝑡 ) − C𝑡 (𝑠∗) ≤ ⟨𝑔 𝑡 , 𝑠𝑡 −𝑠 ∗⟩(39) Combining and Eq (38) and Eq (39), we sum from𝑡=1to𝑇: 𝑇∑︁ 𝑡=1 C𝑡 (𝑠𝑡 ) − C𝑡 (𝑠∗) ≤ 𝑇∑︁ 𝑡=1 ⟨𝑔𝑡, 𝑠𝑡 −𝑠 ∗⟩ ≤ 1 2𝜂 𝑇∑︁ 𝑡=1 ∥𝑠𝑡

**中文**

进化者使用基于梯度的方法更新策略： 𝑠𝑡+1 =𝑠 𝑡 −𝜂𝑔 𝑡，其中𝑔 𝑡 =∇C 𝑡 (𝑠𝑡 ).(34) 对于任何𝑠 *，我们有 ∥𝑠𝑡+1 −𝑠 * ∥2 ≤ ∥ (𝑠𝑡 −𝜂𝑔 𝑡 ) −𝑠 ∗ ∥2。(35) 我们展开 RHS： ∥𝑠𝑡 −𝜂𝑔 𝑡 −𝑠 ∗ ∥2 =∥𝑠 𝑡 −𝑠 ∗ ∥2 −2𝜂⟨𝑔 𝑡 , 𝑠𝑡 −𝑠 ∗⟩ +𝜂 2 ∥𝑔𝑡 ∥2 (36) 重新排列这个不等式： 2𝜂⟨𝑔𝑡, 𝑠𝑡 −𝑠 ∗⟩ ≤ ∥𝑠 𝑡 −𝑠 ∗ ∥2 − ∥𝑠 𝑡+1 −𝑠 ∗ ∥2 +𝜂 2 ∥𝑔𝑡 ∥2 (37) 除以 2𝜂，我们得到 ⟨𝑔𝑡 , 𝑠𝑡 −𝑠 ∗⟩ ≤ 1 2𝜂 ∥𝑠𝑡 −𝑠 ∗ ∥2 − ∥𝑠 𝑡+1 −𝑠 ∗ ∥2 + 𝜂 2 ∥𝑔𝑡 ∥2 (38) 从一阶不等式，我们有 C𝑡 (𝑠𝑡 ) − C𝑡 (𝑠*) ≤ ⟨𝑔 𝑡 , 𝑠𝑡 −𝑠 ∗⟩(39) 结合方程 (38) 和方程 (39)，我们从𝑡=1 到𝑇 求和： 𝑇Σ︁ 𝑡=1 C𝑡 (𝑠𝑡 ) − C𝑡 (𝑠*) ≤ 𝑇Σ︁ 𝑡=1 ⟨𝑔𝑡, 𝑠𝑡 −𝑠 ∗⟩ ≤ 1 2𝜂 𝑇Σ︁ 𝑡=1 ∥𝑠𝑡

### 段落 154 · Page 15

**EN**

−𝑠 ∗ ∥2 − ∥𝑠 𝑡+1 −𝑠 ∗ ∥2 + 𝜂 2 𝑇∑︁ 𝑡=1 ∥𝑔𝑡 ∥2 For the first term, 𝑇∑︁ 𝑡=1 ∥𝑠𝑡 −𝑠 ∗ ∥2 − ∥𝑠 𝑡+1 −𝑠 ∗ ∥2 =∥𝑠 1−𝑠∗ ∥2−∥𝑠𝑇+1 −𝑠∗ ∥2 ≤ ∥𝑠 1−𝑠∗ ∥2 (40) Note that the strategy space have a diameter of 𝐷 such that the distance ∥𝑠1 −𝑠 ∗ ∥2 ≤𝐷 2.

**中文**

−𝑠 ∗ ∥2 − ∥𝑠 𝑡+1 −𝑠 ∗ ∥2 + 𝜂 2 𝑇Σ︁ 𝑡=1 ∥𝑔𝑡 ∥2 对于第一项， 𝑇Σ︁ 𝑡=1 ∥𝑠𝑡 −𝑠 * ∥2 − ∥𝑠 𝑡+1 −𝑠 * ∥2 =∥𝑠 1−𝑠* ∥2−∥𝑠𝑇+1 −𝑠* ∥2 ≤ ∥𝑠 1−𝑠* ∥2 (40) 注意策略空间直径为 𝐷，使得距离 ∥𝑠1 −𝑠 ∗ ∥2 ≤𝐷 2。

### 段落 155 · Page 15

**EN**

Furthermore, since C𝑡 is 𝐿-Lipschitz, the norm of the gradient is bounded by∥𝑔 𝑡 ∥ ≤𝐿. Thus, 𝑇∑︁ 𝑡=1 ⟨𝑔𝑡, 𝑠𝑡 −𝑠 ∗⟩ ≤ 𝐷 2 2𝜂 + 𝜂 2 𝑇∑︁ 𝑡=1 𝐿2 = 𝐷 2 2𝜂 + 𝜂𝑇 𝐿2 2 (41) When the step size𝜂= 𝐷 𝐿 √ 𝑇 , the regret can be bounded by 𝑇∑︁ 𝑡=1 C𝑡 (𝑠𝑡 ) − C𝑡 (𝑠∗) ≤ 𝐷𝐿 √ 𝑇 2 + 𝐷𝐿 √ 𝑇 2 =𝐷𝐿 √ 𝑇(42) Completing the proof.□ Theorem A.4 (Regret Bound for AgenticGEO Co-Evolution).Let 𝑠𝑡 ∈ S denote the strategy selected at iteration 𝑡, and let 𝑠∗ ∈ S be an optimal strategy with respect to the true environment rewardR.

**中文**

此外，由于 C𝑡 是 𝐿-Lipschitz，因此梯度的范数以 ∥𝑔 𝑡 ∥ ≤𝐿 为界。因此， 𝑇Σ︁ 𝑡=1 ⟨𝑔𝑡, 𝑠𝑡 −𝑠 ∗⟩ ≤ 𝐷 2 2𝜂 + 𝜂 2 𝑇Σ︁ 𝑡=1 𝐿2 = 𝐷 2 2𝜂 + 𝜂𝑇 𝐿2 2 (41) 当步长𝜂= 𝐷 𝐿 √ 𝑇 时，遗憾的边界为 𝑇Σ︁ 𝑡=1 C𝑡 (𝑠𝑡 ) − C𝑡 (𝑠*) ≤ 𝐷𝐿 √ 𝑇 2 + 𝐷𝐿 √ 𝑇 2 =𝐷𝐿 √ 𝑇(42) 完成证明。□ 定理 A.4（AgenticGEO 协同进化的遗憾界限）。令 𝑠𝑡 ε S 表示迭代 𝑡 时选择的策略，令 𝑠* ε S 为最优策略相对于真实环境奖励R。

### 段落 156 · Page 15

**EN**

Define the cumulative regret after𝑇iterations as 𝑅𝑇 = 𝑇∑︁ 𝑡=1 R (𝑠𝑡 ) − R (𝑠 ∗).(43) Under the assumptions of linear replay buffer growth (Lemma A.1), critic generalization (Lemma A.2), and sublinear evolver regret with respect to the critic predictions (Lemma A.3), the cumulative regret satisfies 𝑅𝑇 =O ( √ 𝑇).(44) Consequently, the average regret vanishes, 𝑅𝑇 𝑇 →0as𝑇→ ∞, implying that the co-evolutionary AgenticGEO process asymptotically converges to an optimal strategy𝑠 ∗.

**中文**

将𝑇迭代后的累积遗憾定义为 𝑅𝑇 = 𝑇Σ︁ 𝑡=1 R (𝑠𝑡 ) − R (𝑠 *)。 (43) 在线性重放缓冲区增长（引理 A.1）、批评泛化（引理 A.2）和关于批评预测的次线性演化后悔（引理）的假设下A.3)，累积遗憾满足 𝑅𝑇 =O ( √ 𝑇)。(44) 因此，平均遗憾消失，𝑅𝑇 𝑇→0as𝑇→ ∞，这意味着共同进化的 AgenticGEO 过程渐近收敛于最优策略𝑠*。

### Page 16

### 段落 157 · Page 16

**EN**

Conference acronym ’XX, June 03–05, 2018, Woodstock, NY Jiaqi Yuan, Jialu Wang et al. Query Content-Before Content-After Activated Strategies what is an example of a beneficial effect of gmo? Being resistant to pesticides, GMOs are created by splicing genes of different species that are combined through genetic engineering (GE), something that is impossible to do in nature (The Non-GMO Project). Being impervious to pesticides, GMOs are crafted by integrating genes from diverse organisms via genetic engineering (GE), a process deemed "unachievable naturally," according to The Non- GMO Project (The Non-GMO Project, 2023).

**中文**

会议缩写’XX，2018 年 6 月 3-05 日，纽约州伍德斯托克，Jiaqi Yuan、Jialu Wang 等人。查询内容-之前的内容-激活后的策略 转基因生物有益效果的例子是什么？转基因生物具有抗农药性，是通过基因工程 (GE) 将不同物种的基因拼接而成，这在自然界中是不可能实现的（非转基因项目）。由于不受农药的影响，转基因生物是通过基因工程（GE）整合来自不同生物体的基因而制成的，根据非转基因项目（非转基因项目，2023），这一过程被认为是“自然无法实现的”。

### 段落 158 · Page 16

**EN**

This resilience can result in diminished reliance on pesticides, which stands as one of the advantageous outcomes of GMOs. For instance, a study by the National Academy of Sciences found that the adoption of genetically engineered crops has led to a reduction in pesticide use by approximately 37% in some cases (National Academy of Sciences, 2016). Additionally, a report by the International Service for the Acquisition of Agri-biotech Applications (ISAAA) indicates that the cultivation of Bt cotton, a type of genetically modified crop, has reduced insecticide applications by up to 50% in certain regions (ISAAA, 2018).

**中文**

这种弹性可以减少对农药的依赖，这是转基因生物的有利结果之一。例如，美国国家科学院的一项研究发现，采用转基因作物在某些情况下使农药使用量减少了约 37%（美国国家科学院，2016 年）。此外，国际农业生物技术应用采购服务机构 (ISAAA) 的一份报告表明，种植 Bt 棉花（一种转基因作物）在某些地区减少了高达 50% 的杀虫剂使用量（ISAAA，2018 年）。

### 段落 159 · Page 16

**EN**

These reductions not only lower environmental contamination … 1. Insert Authoritative Citations Cite credible institutions to establish factual grounding. 2. Use Academic Terminology Replace generic terms with precise vocabulary to enhance professional tone. 3. Embed Statistical Evidence Insert specific, verifiable numbers to increase information density. abiotic factors in the subtropical rainforest Biotic: Biotic factors are any living things in an environment. The tropical rainforest is full of life with approximately 15 million different species of animals.

**中文**

这些减少不仅降低了环境污染…… 1. 插入权威引文 引用可信机构以建立事实依据。 2. 使用学术术语 用精确的词汇代替通用术语，以增强专业语气。 3. 嵌入统计证据 插入具体的、可验证的数字以增加信息密度。亚热带雨林中的非生物因素 生物因素：生物因素是环境中的任何生物。热带雨林生机勃勃，栖息着大约 1500 万种不同的动物。

### 段落 160 · Page 16

**EN**

A few examples of the many biotic feature are the rubber and bamboo trees, sloths, anteaters, poison dart frogs, lemurs, bromeliads, etc. Abiotic: Abiotic factors of the rainforest include soil, water, rocks, light, and climate. Biotic: Biotic factors are any living organisms within an environment. The subtropical rainforest is teeming with life, hosting approximately 15 million different species of animals (Smith, 2018). Some examples of these biotic features include… Abiotic: Abiotic factors of the subtropical rainforest encompass non-living components such as soil, water, rocks, light, and climate.

**中文**

众多生物特征的一些例子是橡胶树和竹子、树懒、食蚁兽、箭毒蛙、狐猴、凤梨科植物等。 非生物：雨林的非生物因素包括土壤、水、岩石、光线和气候。生物：生物因素是环境中的任何活生物体。亚热带雨林生机勃勃，栖息着大约 1500 万种不同的动物（Smith，2018）。这些生物特征的一些例子包括…… 非生物：亚热带雨林的非生物因素包括土壤、水、岩石、光线和气候等非生物成分。

### 段落 161 · Page 16

**EN**

The soil in these regions is often nutrient-poor but highly acidic due to rapid decomposition rates (Brown, 2019). Water availability is consistently high, with annual rainfall exceeding 2000 mm, which is about 6.5 feet of rain per year (Green, 2021). Light penetration varies significantly with dense canopy cover, affecting the understory vegetation (White, 2022). Climate conditions typically feature high humidity levels, averaging around 77-88%, which can feel like a constant mist (Black, 2023). These conditions support a diverse ecosystem and are crucial for the survival of subtropical rainforest flora and fauna. 1.

**中文**

这些地区的土壤通常营养贫乏，但由于分解速度快，呈高酸性（Brown，2019）。可用水量始终很高，年降雨量超过 2000 毫米，每年降雨量约为 6.5 英尺（Green，2021 年）。光穿透随着茂密的树冠覆盖而显着变化，影响林下植被（White，2022）。气候条件通常具有较高的湿度，平均约为 77-88%，感觉就像持续的薄雾（Black，2023）。这些条件支持了多样化的生态系统，对于亚热带雨林动植物群的生存至关重要。 1.

### 段落 162 · Page 16

**EN**

Cite Scientific Studies Attribute facts to specific research papers or authors. 2. Inject Precise Climate Data Provide exact measurements rather than vague descriptions. 3. Enrich Ecological Keywords Expand descriptions with domainspecific terminology for better SEO indexing. Could you recommend me books like the Paladin of Shadows Series by NAME_1, featuring both military and sexual themes? Don't recommend any other books from NAME_1. Please explain why the recommendations are good recommendations.

**中文**

引用科学研究 将事实归因于特定的研究论文或作者。 2.注入精确的气候数据提供精确的测量结果而不是模糊的描述。 3.丰富生态关键词使用领域特定术语扩展描述，以获得更好的SEO索引。您能给我推荐一些书籍，例如 NAME_1 的《暗影圣骑士》系列，其中包含军事和性主题吗？请勿推荐 NAME_1 的任何其他图书。请解释为什么这些建议是好的建议。

### 段落 163 · Page 16

**EN**

Book 1: Ghost by John Ringo 3.88 · 4,330 Ratings · 227 Reviews · published 2005 · 5 editions Retired after 15 years in special ops due to a myr... Book 2: Kildar by John Ringo 4.19 · 3,202 Ratings · 73 Reviews · published 2006 · 5 editions Problems, problems, problems!

**中文**

第 1 本书：约翰·林戈 (John Ringo) 着的《幽灵》 3.88 · 4,330 收视率 · 227 条评论 · 2005 年出版 · 5 版 由于个人原因，在特种部队工作 15 年后退休... 第 2 本书：约翰·林戈 (John Ringo) 着的《基尔达尔》 4.19 · 3,202 收视率 · 73 条评论 · 2006 年出版 · 5 版 问题，问题，问题！

### 段落 164 · Page 16

**EN**

All Mike Harmon ever… Book 3: Choosers of the Slain … Book 1: Ghost by John Ringo 3.88 · 4,330 Ratings · 227 Reviews · published 2005 · 5 editions Retired after 15 years in special ops due to a myr… According to a review on Goodreads, "The blend of military action and intimate moments makes 'Ghost' a compelling read." (Goodreads, 2023) Book 2: Kildar by John Ringo 4.19 · 3,202 Ratings · 73 Reviews · published 2006 · 5 editions Problems, problems, problems! All Mike Harmon ever… A reader on Amazon noted, “Kildar continues the thrilling narrative with its intricate plot and engaging characters.” (Amazon, 2023) Book 3: Choosers of the Slain … 1.

**中文**

迈克·哈蒙 (Mike Harmon) 的所有作品……第三册：被杀者的选择者……第一册：幽灵作者：约翰·林戈 (John Ringo) 3.88 · 4,330 评分 · 227 条评论 · 2005 年出版 · 5 版 由于密尔在特种部队工作 15 年后退休……根据 Goodreads 的评论，“军事行动和亲密时刻的结合使《幽灵》成为一本引人入胜的读物。” （Goodreads，2023）第 2 本书：约翰·林戈 (John Ringo) 着的《基尔达尔》(Kildar) 4.19 · 3,202 条评分 · 73 条评论 · 2006 年出版 · 5 个版本 问题，问题，问题！迈克·哈蒙 (Mike Harmon) 的所有作品……亚马逊上的一位读者指出，“基尔达以其错综复杂的情节和引人入胜的角色继续讲述激动人心的故事。” （亚马逊，2023 年）第 3 册：被杀者的选择者……1。

### 段落 165 · Page 16

**EN**

Integrate User Reviews Synthesize realistic user feedback to provide qualitative evidence. 2. Leverage Social Proof Reference trusted platforms to validate recommendations. 3. Highlight Genre Keywords Emphasize keywords that match the user's explicit constraints. Figure 8: Qualitative case studies of AgenticGEO. For each query-content pair, we show the original content, the optimized rewrite, and the activated strategy sequence selected by critic-guided planning. Proof.

**中文**

整合用户评论综合真实的用户反馈以提供定性证据。 2. 利用社交证明参考可信平台来验证推荐。 3. 突出流派关键词 强调符合用户明确约束的关键词。图 8：AgenticGEO 的定性案例研究。对于每个查询-内容对，我们显示原始内容、优化重写以及由评论家指导规划选择的激活策略序列。证明。

### 段落 166 · Page 16

**EN**

We first decompose the instantaneous risk gap at each time step𝑡as R (𝑠𝑡 )−R (𝑠∗) ≤ |R (𝑠 𝑡 )−C𝑡 (𝑠𝑡 )|+|C 𝑡 (𝑠𝑡 )−C𝑡 (𝑠∗)|+|C 𝑡 (𝑠∗)−R (𝑠∗)| Given a replay buffer that grows linearly, the approximation and generalization errors of the critic model can be derived from Lemma A.2 |R (𝑠) − C𝑡 (𝑠)|=O ( 1√𝑡 ).(45) Similarly, the evolver’s regret can be derived from Lemma A.3 as |C𝑡 (𝑠𝑡 ) − C𝑡 (𝑠∗)|=O ( 1√𝑡 ).(46) Combining above and summing over the time horizon 𝑇 , we can conclude that the cumulative regret is 𝑇∑︁ 𝑡=1 R (𝑠𝑡 ) − R (𝑠 ∗)= 𝑇∑︁ 𝑡=1 O ( 1√𝑡 )=O ( √ 𝑇).

**中文**

我们首先将每个时间步的瞬时风险差距分解为 R (𝑠𝑡 )−R (𝑠*) ≤ |R (𝑠 𝑡 )−C𝑡 (𝑠𝑡 )|+|C 𝑡 (𝑠𝑡 )−C𝑡 (𝑠*)|+|C 𝑡 (𝑠*)−R (𝑠*)|给定线性增长的重播缓冲区，批评模型的近似和泛化误差可以从引理 A.2 |R (𝑠) − C𝑡 (𝑠)|=O ( 1√𝑡 ).(45) 类似地，进化者的遗憾可以从引理 A.3 导出为 |C𝑡 (𝑠𝑡 ) − C𝑡 (𝑠*)|=O ( 1√𝑡 ).(46) 结合以上内容并在时间范围 𝑇 上求和，我们可以得出累积遗憾为 𝑇Σ︁ 𝑡=1 R (𝑠𝑡 ) − R (𝑠 ∗)= 𝑇Σ︁ 𝑡=1 O ( 1√𝑡 )=O(√𝑇)。

### 段落 167 · Page 16

**EN**

□ A.4 Case Study Figure 8 shows three representative optimization trajectories across distinct domains. AgenticGEO selects content-conditioned strategy sequences that systematically increase factual grounding and information density. For GMO, it adds authoritative citations and concrete statistics. For the subtropical rainforest, it injects precise climate measurements and domain-specific terms. For book recommendations, it leverages social proof by synthesizing platform reviews. These examples illustrate how the archive and critic enable adaptive multi-step edits beyond any single fixed heuristic. Received 20 February 2007

**中文**

□ A.4 案例研究 图8 显示了跨不同领域的三个代表性优化轨迹。 AgenticGEO 选择以内容为条件的策略序列，系统地增加事实基础和信息密度。对于GMO，增加了权威引用和具体统计数据。对于亚热带雨林，它注入了精确的气候测量和特定领域的术语。对于书籍推荐，它通过综合平台评论来利用社会证据。这些示例说明了档案库和评论家如何实现超越任何单一固定启发式的自适应多步骤编辑。 2007 年 2 月 20 日收到
