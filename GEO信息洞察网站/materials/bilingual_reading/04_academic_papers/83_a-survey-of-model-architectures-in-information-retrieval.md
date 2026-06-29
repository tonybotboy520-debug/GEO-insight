# A Survey of Model Architectures in Information Retrieval

- ID: 83
- 类型: pdf
- 分类: 04_academic_papers
- 主题: modern IR architecture survey
- 原文链接: https://arxiv.org/pdf/2502.14822
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

Published in Transactions on Machine Learning Research (02/2026) A Survey of Model Architectures in Information Retrieval Zhichao Xu zhichao.xu@utah.edu Kahlert School of Computing University of Utah Fengran Mo fengran.mo@umontreal.ca University of Montreal Zhiqi Huang zhiqi.huang@capitalone.com Capital One Crystina Zhangxinyucrystina.zhang@uwaterloo.ca University of Waterloo Puxuan Yu puxuan.yu@snowflake.com Snowflake Inc.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 信息检索模型架构综述 徐志超 zhichao.xu@utah.edu 卡勒特计算学院 犹他大学 Fengran Mo fengran.mo@umontreal.ca 蒙特利尔大学 黄志奇 zhiqi.huang@capitalone.com 第一资本 Crystina Zhangxinyucrystina.zhang@uwaterloo.ca 滑铁卢大学于璞轩 puxuan.yu@snowflake.com 雪花公司

### 段落 2 · Page 1

**EN**

Bei Wang beiwang@sci.utah.edu Kahlert School of Computing Scientific Computing and Imaging (SCI) Institute University of Utah Jimmy Lin jimmylin@uwaterloo.ca University of Waterloo Vivek Srikumar svivek@cs.utah.edu Kahlert School of Computing University of Utah Reviewed on OpenReview:https: // openreview. net/ forum? id= xAIbTbHRrX Abstract The period from 2019 to the present marks one of the most significant paradigm shifts in information retrieval (IR) and natural language processing (NLP), culminating in the emergence of powerful large language models (LLMs) from 2022 onward.

**中文**

Bei Wang beiwang@sci.utah.edu Kahlert 计算学院 犹他大学科学计算与成像 (SCI) 研究所 Jimmy Lin jimmylin@uwaterloo.ca 滑铁卢大学 Vivek Srikumar svivek@cs.utah.edu 犹他大学 Kahlert 计算学院 OpenReview 已审阅：https://openreview。网/论坛？ id= xAIbTbHRrX 摘要 2019 年至今标志着信息检索 (IR) 和自然语言处理 (NLP) 领域最重大的范式转变之一，最终导致从 2022 年起强大的大型语言模型 (LLM) 的出现。

### 段落 3 · Page 1

**EN**

Methods based on pretrained encoder-only architectures (e.g., BERT) as well as decoder-only generative LLMs have outperformed many earlier approaches, demonstrating particularly strong performance in zero-shot scenarios and complex reasoning tasks. This survey examines the evolution of model architectures in IR, with a focus on two key aspects: backbone models for feature extraction and end-to-end system architectures for relevance estimation. To maintain analytical clarity, we deliberately separate architectural design from training methodologies, enabling a focused examination of structural innovations in IR systems.

**中文**

基于预训练的仅编码器架构（例如 BERT）以及仅解码器的生成 LLM 的方法优于许多早期方法，在零样本场景和复杂推理任务中表现出特别强大的性能。本次调查研究了 IR 模型架构的演变，重点关注两个关键方面：用于特征提取的骨干模型和用于相关性估计的端到端系统架构。为了保持分析的清晰度，我们特意将架构设计与培训方法分开，从而能够对 IR 系统的结构创新进行重点检查。

### 段落 4 · Page 1

**EN**

We trace the progression from traditional term-based retrieval models to modern neural approaches, highlighting the transformative impact of transformer-based architectures and subsequent LLM developments. The survey concludes with a forward-looking discussion of open challenges and emerging research directions, including architectural optimization for efficiency and scalability, robust handling of multimodal and multilingual data, and adaptation to novel application domains such as autonomous search agents, which may represent the next paradigm in IR. 1 arXiv:2502.14822v3 [cs.IR] 15 Mar 2026

**中文**

我们追溯了从传统的基于术语的检索模型到现代神经方法的进展，强调了基于 Transformer 的架构和后续法学硕士发展的变革性影响。该调查最后对开放挑战和新兴研究方向进行了前瞻性讨论，包括效率和可扩展性的架构优化、多模式和多语言数据的稳健处理，以及适应新的应用领域，例如自主搜索代理，这可能代表信息检索的下一个范例。 1 arXiv:2502.14822v3 [cs.IR] 2026 年 3 月 15 日

### Page 2

### 段落 5 · Page 2

**EN**

Published in Transactions on Machine Learning Research (02/2026) 1 Introduction Figure 1: High-level overview of the survey structure and scope. 2

**中文**

发表于机器学习研究汇刊 (02/2026) 1 简介 图 1：调查结构和范围的高级概述。 2

### Page 3

### 段落 6 · Page 3

**EN**

Published in Transactions on Machine Learning Research (02/2026) Information Retrieval (IR) aims to retrieve relevant information sources to satisfy users’ information needs. In the past decades, IR has become indispensable for efficiently and effectively accessing vast amounts of information across various applications. Beyond its traditional role, IR now also plays a critical role in assisting large language models (LLMs) to generate grounded and factual responses under the generative AI era.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 信息检索（IR）旨在检索相关信息源以满足用户的信息需求。在过去的几十年里，IR 已成为高效、有效地访问各种应用程序中的大量信息所不可或缺的。除了其传统作用之外，IR 现在还在生成人工智能时代协助大型语言模型 (LLM) 生成扎根和事实的响应方面发挥着关键作用。

### 段落 7 · Page 3

**EN**

Research in IR primarily centers on two key aspects: (1)extracting better query and document feature representations, and (2)developing more accurate relevance estimators. Extracting better query and document feature representations focuses on modeling textual content so that queries and documents can be compared in a meaningful space, ranging from early term-frequency vectors (e.g., TF–IDF (Sparck Jones, 1972) and BM25 (Robertson & Zaragoza, 2009)) to modern contextual embeddings derived from pre-trained language models.

**中文**

IR 的研究主要集中在两个关键方面：（1）提取更好的查询和文档特征表示，以及（2）开发更准确的相关性估计器。提取更好的查询和文档特征表示侧重于对文本内容进行建模，以便可以在有意义的空间中比较查询和文档，范围从早期的术语频率向量（例如 TF-IDF (Sparck Jones, 1972) 和 BM25 (Robertson & Zaragoza, 2009)）到从预训练语言模型派生的现代上下文嵌入。

### 段落 8 · Page 3

**EN**

Developing more accurate relevance estimators then builds on these representations to assess how well a document satisfies an information need, using scoring functions or learned ranking models such as BM25, neural interaction models, or later learning-to-rank frameworks that combine multiple signals.

**中文**

然后，使用评分函数或学习排名模型（例如 BM25、神经交互模型或后来结合多个信号的学习排名框架），在这些表示的基础上开发更准确的相关性估计器，以评估文档满足信息需求的程度。

### 段落 9 · Page 3

**EN**

The approaches for extracting query and document features have evolved from traditional term-based methods, such as boolean logic (Radecki, 1979; Kraft & Buell, 1983) and vector space models (Salton et al., 1975), to modern solutions such as dense retrieval based on pre-trained language models (Lee et al., 2019; Karpukhin et al., 2020; Logeswaran et al., 2019; Lin et al., 2022,inter alia). Relevance estimators have evolved alongside advances in feature representations. Early approaches, including probabilistic and statistical language models, computed relevance with simple similarity functions based on term-based features.

**中文**

提取查询和文档特征的方法已经从传统的基于术语的方法（例如布尔逻辑（Radecki，1979；Kraft & Buell，1983）和向量空间模型（Salton 等人，1975））发展到现代解决方案，例如基于预训练语言模型的密集检索（Lee 等人，2019；Karpukhin 等人，2020；Logeswaran 等人， 2019；林等人，2022，等等）。相关性估计器随着特征表示的进步而发展。早期的方法，包括概率和统计语言模型，使用基于术语的特征的简单相似性函数来计算相关性。

### 段落 10 · Page 3

**EN**

Learning-to-rank (LTR) techniques later emerged, incorporating machine learning models like support vector machines (Cortes & Vapnik, 1995), boosting methods (Kearns & Valiant, 1994; Freund & Schapire, 1995) as well as multi-layer neural networks for relevance estimation (Li, 2011). The success of LTR methods can be largely attributed to their extensive use of manually engineered features, derived from both statistical properties of text terms and user behavior data collected from web browsing traffic (Qin & Liu, 2013).

**中文**

后来出现了学习排名（LTR）技术，结合了支持向量机（Cortes & Vapnik，1995）等机器学习模型、Boosting 方法（Kearns & Valiant，1994；Freund & Schapire，1995）以及用于相关性估计的多层神经网络（Li，2011）。 LTR 方法的成功很大程度上归功于其对手动设计特征的广泛使用，这些特征源自文本术语的统计属性和从网络浏览流量中收集的用户行为数据（Qin & Liu，2013）。

### 段落 11 · Page 3

**EN**

In the 2010s, a vast literature explored neural rerankers in different architectures to capture the semantic similarity between queries and documents (Pang et al., 2016; Guo et al., 2016a; Xiong et al., 2017; Dai et al., 2018,inter alia).

**中文**

在 2010 年代，大量文献探索了不同架构中的神经重新排序器，以捕获查询和文档之间的语义相似性（Pang 等人，2016；Guo 等人，2016a；Xiong 等人，2017；Dai 等人，2018，等等）。

### 段落 12 · Page 3

**EN**

Then pre-trained transformers, represented byBERT(Devlin et al., 2019) and its variants (Liu et al., 2019; Sun et al., 2019; Lan et al., 2020; Beltagy et al., 2020), quickly revolutionized the model design, leading to an era where retrieval and ranking models adopt simpler architectures for relevance estimation, such as dot product operations and MLP prediction heads, which operate on learned neural representations (MacAvaney et al., 2019b; Lee et al., 2019; Karpukhin et al., 2020; Nogueira et al., 2020; Lin et al., 2022; Formal et al., 2021b;a).

**中文**

然后，以 BERT（Devlin 等人，2019）及其变体（Liu 等人，2019；Sun 等人，2019；Lan 等人，2020；Beltagy 等人，2020）为代表的预训练 Transformer 迅速彻底改变了模型设计，导致检索和排序模型采用更简单的架构进行相关性估计，例如点积运算和 MLP 预测头，这些架构在学习神经表征（MacAvaney 等人，2019b；Lee 等人，2019；Karpukhin 等人，2020；Nogueira 等人，2020；Lin 等人，2022；Formal 等人，2021b；a）。

### 段落 13 · Page 3

**EN**

Recent advancements in LLMs have revolutionized applied machine learning (ML) communities, including IR. One intriguing property of modern instruction-following LLMs (e.g., ChatGPT OpenAI (2022)) is that they can be used for feature extraction and relevance estimation, achieving strong performance without extensive training (Ni et al., 2022a; Neelakantan et al., 2022; BehnamGhader et al., 2024; Sun et al., 2023; Qin et al., 2024b,inter alia).

**中文**

法学硕士的最新进展彻底改变了应用机器学习 (ML) 社区，包括 IR。现代指令跟踪法学硕士（例如 ChatGPT OpenAI (2022)）的一个有趣特性是它们可以用于特征提取和相关性估计，无需大量训练即可实现强大的性能（Ni 等人，2022a；Neelakantan 等人，2022；BehnamGhader 等人，2024；Sun 等人，2023；Qin 等人， 2024b，等等）。

### 段落 14 · Page 3

**EN**

The rise of these models builds upon a rich foundation of neural architectures, including the classical Transformer architecture with multi-head attention (MHA, Vaswani et al., 2017), Recurrent Neural Networks (RNN, Elman, 1990), attention mechanisms (Bahdanau et al., 2014), and pretrained static word representations like Word2Vec (Mikolov et al., 2013) and GloVe (Pennington et al., 2014) (Collobert et al., 2011; Le & Mikolov, 2014,inter alia). This work reviews the evolution of model architectures in IR (with an overview in Figure 1).

**中文**

这些模型的兴起建立在丰富的神经架构基础上，包括具有多头注意力的经典 Transformer 架构（MHA，Vaswani 等，2017）、循环神经网络（RNN，Elman，1990）、注意力机制（Bahdanau 等，2014）以及预训练的静态单词表示，如 Word2Vec（Mikolov 等，2013）和 GloVe （Pennington 等人，2014 年）（Collobert 等人，2011 年；Le & Mikolov，2014 年等）。这项工作回顾了 IR 模型架构的演变（图 1 中的概述）。

### 段落 15 · Page 3

**EN**

Here, the meaning of model architecture is twofold: it describes (1) backbone models for extracting query and document feature representations, and (2) end-to-end system architectures that process raw inputs, perform feature extraction, and estimate relevance. Different from prior works and surveys (Lin et al., 2022; Zhu et al., 2023), we intentionally separate our discussion of model architectures from training methodologies and deployment best practices to deliver a focused architectural analysis. This analysis centers on the core components of AI infrastructure in the LLM era.

**中文**

在这里，模型架构的含义是双重的：它描述了（1）用于提取查询和文档特征表示的骨干模型，以及（2）处理原始输入、执行特征提取和估计相关性的端到端系统架构。与之前的工作和调查不同（Lin et al., 2022；Zhu et al., 2023），我们有意将模型架构的讨论与训练方法和部署最佳实践分开，以提供有针对性的架构分析。本次分析重点关注LLM时代AI基础设施的核心组成部分。

### 段落 16 · Page 3

**EN**

The shift towards neural architectures, particularly Transformer-based models, has fundamentally transformed IR by enabling rich, contextualized representations and improved capacity for handling complex queries. While this evolution enhanced retrieval performance, it also presents new challenges, especially with the development of LLMs. These challenges include the need for architectural innovations to optimize performance and scalability, handle multimodal and multilingual data, and understand complex instructions. Moreover, as IR systems are increasingly integrated into diverse applica- 3

**中文**

向神经架构的转变，特别是基于 Transformer 的模型，通过实现丰富的上下文化表示和提高处理复杂查询的能力，从根本上改变了 IR。虽然这种演变提高了检索性能，但它也带来了新的挑战，特别是随着法学硕士的发展。这些挑战包括需要进行架构创新来优化性能和可扩展性、处理多模式和多语言数据以及理解复杂的指令。此外，随着红外系统越来越多地集成到不同的应用中，3

### Page 4

### 段落 17 · Page 4

**EN**

Published in Transactions on Machine Learning Research (02/2026) tions—from robotics (Xie et al., 2024b), protein structure discovery (Jumper et al., 2021) to autonomous agents (Wu et al., 2023a; Chen et al., 2025; Hu et al., 2025; OpenAI, 2025; Wu et al., 2025b,inter alia) that are capable of reasoning and search—the field must evolve beyond traditional search paradigms. We conclude this survey by examining these challenges and discussing their implications for the future of IR model architectures research. 2 Background and Terminology We focus on the classicalad hocretrieval task, which forms the foundation for many modern IR applications.

**中文**

发表在《机器学习研究汇刊》(02/2026) 中——从机器人技术（Xie 等人，2024b）、蛋白质结构发现（Jumper 等人，2021）到自主代理（Wu 等人，2023a；Chen 等人，2025；Hu 等人，2025；OpenAI，2025；Wu 等人， 2025b，尤其是）能够推理和搜索——该领域必须发展超越传统的搜索范式。我们通过研究这些挑战并讨论它们对 IR 模型架构研究的未来的影响来结束本次调查。 2 背景和术语 我们关注经典的临时检索任务，它构成了许多现代 IR 应用的基础。

### 段落 18 · Page 4

**EN**

In this section, we define the core task, introduce key system architectures and evaluation paradigms, and clarify the scope of our architectural review. Task Definition and Evaluation.Given a queryQ, the task is to find a ranked list ofkdocuments, denotedas{D1,D 2,...,Dk}, thatexhibitthehighestrelevancetoQ. Thisisachievedeitherbyretrievingtopkdocuments from a large collectionC(|C|≫k), which typically comprises millions or billions of documents, orbyrerankingthetop-kcandidatesreturnedbyaretriever. Systemperformanceismeasuredusingstandard, list-wise IR metrics.

**中文**

在本节中，我们定义核心任务，介绍关键系统架构和评估范式，并阐明架构审查的范围。任务定义和评估。给定一个查询 Q，任务是找到 k 个文档的排序列表，表示为 {D1,D 2,...,Dk}，与 Q 表现出最高的相关性。这是通过从大型集合 C(|C|≫k)（通常包含数百万或数十亿个文档）中检索 topk 文档，或者通过对检索器返回的 top-k 候选进行重排来实现的。系统性能是使用标准的列表式 IR 指标来衡量的。

### 段落 19 · Page 4

**EN**

Common metrics include: •Mean Reciprocal Rank (MRR):Measures the rank of the first relevant document. It is particularly useful for tasks where finding one correct answer is the primary goal (e.g., question answering). •Recall@k:Measures the fraction of all relevant documents that are found within the top-kresults. It emphasizes the system’s ability to find all relevant items. •Normalized Discounted Cumulative Gain (nDCG@k):A sophisticated metric that evaluates the quality of the ranking over the top-kdocuments.

**中文**

常见指标包括： • 平均倒数排名(MRR)：衡量第一个相关文档的排名。它对于以找到正确答案为主要目标的任务（例如回答问题）特别有用。 •Recall@k：衡量在顶级k 结果中找到的所有相关文档的比例。它强调系统查找所有相关项目的能力。 •标准化贴现累积增益(nDCG@k)：一种复杂的指标，用于评估前k 个文档的排名质量。

### 段落 20 · Page 4

**EN**

It gives higher scores for ranking highly relevant documents at the top of the list and uses a logarithmic discount to penalize relevant documents that appear lower in the ranking. It is the de facto standard for evaluating ranked lists with graded relevance judgments. The Multi-Stage “Retrieve-then-Rerank” Architecture.Modern large-scale IR systems almost universally operate on a multi-stage pipeline, commonly known as the “retrieve-then-rerank” architecture. This design balances the tradeoff between efficiency and effectiveness.

**中文**

它对于将高度相关的文档排名在列表顶部给出更高的分数，并使用对数折扣来惩罚排名较低的相关文档。它是评估具有分级相关性判断的排名列表的事实上的标准。多级“检索然后重新排序”架构。现代大型红外系统几乎普遍在多级管道上运行，通常称为“检索然后重新排序”架构。这种设计平衡了效率和效果之间的权衡。

### 段落 21 · Page 4

**EN**

1.Retrieval(orFirst-StageRanking):Inthefirststage, acomputationallyefficientbutlessprecise model scans the entire collectionC(potentially billions of documents) to quickly identify an initial set of several hundred or thousand candidate documents. These models, often calledretrievers, must be extremely fast. Examples include traditional models like BM25 (Section 3) or modern bi-encoder models (Section 6). 2.Reranking (or Second-Stage Ranking):In the second stage, a more powerful but computationally expensive model, known as areranker, is applied only to the small candidate set returned by the retriever.

**中文**

1.检索（或第一阶段排名）：在第一阶段，计算效率高但不太精确的模型扫描整个集合C（可能是数十亿个文档），以快速识别初始的数百或数千个候选文档集。这些模型通常称为检索器，必须非常快。示例包括 BM25（第 3 节）等传统模型或现代双编码器模型（第 6 节）。 2.Reranking（或Second-Stage Ranking）：在第二阶段，一个更强大但计算成本昂贵的模型，称为areranker，仅应用于检索器返回的小候选集。

### 段落 22 · Page 4

**EN**

This model can afford to perform deep, fine-grained analysis of the interaction between the query and each candidate document to produce a more accurate final ranking. Examples include Learning-to-Rank models (Section 4) and modern cross-encoder transformers (Section 6). This two-stage process is a central architectural pattern in IR, and much of the evolution discussed in this survey can be understood as developing more advanced models for each of these stages. Query and Document.Aqueryexpresses an information need and serves as input to thead hocretrieval system. We denotedocumentas the atomic unit for retrieval and ranking.

**中文**

该模型可以对查询和每个候选文档之间的交互进行深入、细粒度的分析，以产生更准确的最终排名。示例包括 Learning-to-Rank 模型（第 4 节）和现代交叉编码器转换器（第 6 节）。这个两阶段过程是 IR 的核心架构模式，本次调查中讨论的大部分演变可以理解为为每个阶段开发更高级的模型。查询和文档。查询表达信息需求并作为临时检索系统的输入。我们将文档表示为检索和排序的原子单元。

### 段落 23 · Page 4

**EN**

Our discussions are primarily based on text-based documents, but a document can also refer to a webpage or an email, depending on the actual IR application of interest. 4

**中文**

我们的讨论主要基于文本文档，但文档也可以指网页或电子邮件，具体取决于感兴趣的实际 IR 应用。 4

### Page 5

### 段落 24 · Page 5

**EN**

Published in Transactions on Machine Learning Research (02/2026) Disentangling Model Architecture from Training Strategies.Similar to other applied ML domains, the performance of an IR system is a product of its model architecture, its training methodology (e.g., loss functions, data augmentation, optimization algorithms), and deployment best practices (e.g., indexing, quantization, parallelization, algorithm-hardware co-design). In this survey, we intentionally seek to disentangle these aspects to provide a focused analysis on theevolution of model architecture.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) Disentangling Model Architecture from Training Strategies。与其他应用的 ML 领域类似，IR 系统的性能是其模型架构、训练方法（例如损失函数、数据增强、优化算法）和部署最佳实践（例如索引、量化、并行化、算法硬件协同设计）的产物。在本次调查中，我们有意试图理清这些方面，以便对模型架构的演变进行集中分析。

### 段落 25 · Page 5

**EN**

This focus allows for a clearer narrative on how the core components for representation learning and relevance estimation have changed over time, from term-based logic to deep neural networks. We refer readers to dedicated surveys for in-depth reviews of training strategies and other related topics (Schütze et al., 2008; Lin et al., 2022; Song et al., 2023). 3 Traditional IR Models In this section, we briefly review traditional Information Retrieval (IR) models prior to neural methods, with a focus on theBoolean model,vector space model,probabilistic model, andstatistical language model.

**中文**

这种关注可以更清晰地叙述表示学习和相关性估计的核心组件如何随着时间的推移而变化，从基于术语的逻辑到深度神经网络。我们建议读者查阅专门调查，以深入审查培训策略和其他相关主题（Schütze 等人，2008 年；Lin 等人，2022 年；Song 等人，2023 年）。 3 传统IR模型在本节中，我们简要回顾一下神经方法之前的传统信息检索（IR）模型，重点关注布尔模型、向量空间模型、概率模型和统计语言模型。

### 段落 26 · Page 5

**EN**

These models, which serve as the foundation for later developments in IR (Sections 4 to 7), are built upon the basic unit of a “term” in their representations (Nie, 2010). Boolean Model.In the Boolean Model, a documentDis represented by a set of terms it contains, i.e., D={t1,t 2,...,tn}, and a queryQis represented as a similar boolean expression of terms. A document is considered relevant to a query only if a logical implicationD→Qholds, i.e., the document representation logically implies the query expression.

**中文**

这些模型是后来 IR 发展的基础（第 4 节到第 7 节），建立在其表示中“术语”的基本单位之上（Nie，2010）。布尔模型。在布尔模型中，文档Dis由其包含的一组术语表示，即D={t1,t 2,...,tn}，而查询Q则表示为术语的类似布尔表达式。仅当逻辑蕴含 D → Q 成立时，即文档表示在逻辑上暗示查询表达式时，文档才被视为与查询相关。

### 段落 27 · Page 5

**EN**

This basic model can be extended by incorporating term weighting, allowing both queries and documents to be represented as sets of weighted terms. Consequently, the logical implicationD→Qis also weighted. Common approaches for this include using a fuzzy set extension of Boolean logic (Radecki, 1979; Kraft & Buell, 1983) and thep-norm (Salton et al., 1983). Vector Space Model.In Vector Space Models (VSMs, Salton et al., 1975), the queries and documents are represented by vectors, e.g.,Q=< q 1,q 2,...,qn >andD=< d 1,d 2,...,dn >.

**中文**

这个基本模型可以通过合并术语权重来扩展，允许查询和文档都表示为加权术语集。因此，逻辑蕴涵D→Q也被加权。常见的方法包括使用布尔逻辑的模糊集扩展（Radecki，1979；Kraft & Buell，1983）和 p 范数（Salton 等人，1983）。向量空间模型。在向量空间模型（VSM，Salton 等，1975）中，查询和文档由向量表示，例如，Q=< q 1,q 2,...,qn > 和 D=< d 1,d 2,...,dn >。

### 段落 28 · Page 5

**EN**

The vector space is defined by a vocabulary of termsV=< t 1,t 2,...,tn >and each element (q i ord i,1≤i≤n) in the vectors represents the weight of the corresponding term in the query or the document. The weightsqi ord i could be binary, representing presence or absence. Given the vector representations, the relevance score is estimated by a similarity function between the queryQand the documentD. The weightsqi ord i can be determined by more sophisticated schema (Salton & Buckley, 1988), such as TF-IDF (Sparck Jones, 1972) and BM25 (Robertson & Zaragoza, 2009; Robertson et al., 1995).

**中文**

向量空间由术语词汇表 V=< t 1,t 2,...,tn > 定义，向量中的每个元素 (q i ord i,1≤i≤n) 表示查询或文档中相应术语的权重。权重 qi 或 i 可以是二进制的，表示存在或不存在。给定向量表示，相关性得分通过查询Q和文档D之间的相似性函数来估计。权重 i​​ ord i 可以通过更复杂的模式（Salton & Buckley，1988）确定，例如 TF-IDF（Sparck Jones，1972）和 BM25（Robertson & Zaragoza，2009；Robertson 等人，1995）。

### 段落 29 · Page 5

**EN**

This allows for more abundant features that can improve the capacity and accuracy of the models. Besides, given the vector representations of query Qand documentD, the most commonly used is cosine similarity, defined as: sim(Q,D) = Q·D |Q|×|D|, whereQ·Dis the dot product and|Q|,|D|denotes the length of the vector. Probabilistic Model.In the probabilistic model, the relevance score of a documentDto a queryQ depends on a set of events{xi}n 1 representing the occurrence of termti in this document.

**中文**

这允许更丰富的特征，可以提高模型的容量和准确性。此外，给定查询Q和文档D的向量表示，最常用的是余弦相似度，定义为：sim(Q,D) = Q·D |Q|×|D|，其中Q·Dis是点积，|Q|,|D|表示向量的长度。概率模型。在概率模型中，文档D与查询Q的相关性得分取决于表示termti在该文档中出现的一组事件{xi}n 1。

### 段落 30 · Page 5

**EN**

The simplest probabilistic model is the binary independence retrieval model (Robertson & Jones, 1976), which assumes terms are independent so onlyxi = 1andx i = 0exist in the representation. Given a set of sample documents whose relevance is judged, the estimation of the relevance score can be derived as Score(Q,D)∝ ∑ (xi=1)∈D logri(T−ni−R+ri) (R−ri)(ni−ri) whereTandRare the total number of sampled judged documents and relevant samples, andn i andr i denote the number of samples and relevant samples containingti, respectively.

**中文**

最简单的概率模型是二元独立检索模型（Robertson & Jones，1976），它假设项是独立的，因此表示中仅存在 xi = 1 和 x i = 0。给定一组进行相关性判断的样本文档，相关性得分的估计可以导出为 Score(Q,D)∝ Σ (xi=1)εD logri(T−ni−R+ri) (R−ri)(ni−ri) 其中 T 和 Ra 分别是样本判断文档和相关样本的总数，n i 和 r i 分别表示包含 ti 的样本和相关样本的数量。

### 段落 31 · Page 5

**EN**

In contrast, a line of statistical retrieval functions such as TF-IDF (Sparck Jones, 1972) move beyond binary term indicators by incorporating term frequency (TF) and inverse document frequency (IDF), allowing 5

**中文**

相比之下，诸如 TF-IDF（Sparck Jones，1972）之类的一系列统计检索函数通过合并术语频率 (TF) 和逆文档频率 (IDF) 超越了二进制术语指标，允许 5

### Page 6

### 段落 32 · Page 6

**EN**

Published in Transactions on Machine Learning Research (02/2026) more nuanced term weighting while still assuming term independence. We illustrate the famous BM25 algorithm (Robertson et al., 1995): BM25(Q,D) = ∑ ti∈Q∩D IDF(ti)· fi·(k1 + 1) fi +k 1· ( 1−b+b·|D| avgdl ), wheref i is the frequency of termti in documentD,|D|is the length of the document, avgdl is the average document length in the collection, andk1 andbare hyperparameters typically set between[1.2,2.0]and [0.5,0.8], respectively.

**中文**

发表在《机器学习研究汇刊》(02/2026) 中，在仍然假设术语独立性的同时，更细致地术语权重。我们举例说明著名的 BM25 算法 (Robertson et al., 1995)： BM25(Q,D) = Σ ti∈Q∩D IDF(ti)· fi·(k1 + 1) fi +k 1· ( 1−b+b·|D| avgdl )，其中 fi 是 documentD 中 termti 的频率，|D| 是文档的长度，avgdl 是文档 D 中 termti 的频率，avgdl 是文档 D 中 termti 的频率，avgdl 是文档 D 中 termti 的频率。集合、k1 和裸超参数通常分别设置在 [1.2,2.0] 和 [0.5,0.8] 之间。

### 段落 33 · Page 6

**EN**

The inverse document frequency term is computed as IDF(ti) = log N−ni+0.5 ni+0.5 ,where Nis the total number of documents in the collection andni is the number of documents containing termti. The smoothing mechanisms (Baeza-Yates & Ribeiro-Neto, 1999) are necessary to deal with zero occurrences oft i. Except for the binary independence retrieval model, more sophisticated probabilistic models have been proposed in the literature (Wong & Yao, 1989; Fuhr, 1992), such as the inter-dependency between terms (Van Rijsbergen, 1979).

**中文**

逆文档频率项计算为 IDF(ti) = log N−ni+0.5 ni+0.5，其中 Ni 是集合中文档的总数，ni 是包含 termti 的文档数。平滑机制（Baeza-Yates & Ribeiro-Neto，1999）对于处理 i 的零出现是必要的。除了二元独立检索模型之外，文献中还提出了更复杂的概率模型（Wong & Yao，1989；Fuhr，1992），例如术语之间的相互依赖性（Van Rijsbergen，1979）。

### 段落 34 · Page 6

**EN**

Statistical Language Model.The general idea of a statistical language model is to estimate the relevance score of a documentDto a queryQviaP(D|Q)(Ponte & Croft, 1998). Based on Bayes’ Rule,P(D|Q) can be derived as directly proportional toP(Q|D)P(D). For simplification, most studies assume a uniform distribution forP(D). The main focus is on modelingP(Q|D)as a ranking function. By treating the query as a set of independent termsQ={ti}n i=1, we haveP(Q|D) =∏ ti∈QP(ti|D).The probabilityP(ti|D) is determined using a statistical language modelθD that represents the document.

**中文**

统计语言模型。统计语言模型的总体思想是通过 P(D|Q) 估计文档 D 与查询 QQ 的相关性得分（Ponte & Croft，1998）。根据贝叶斯法则，P(D|Q) 可以导出为与 P(Q|D)P(D) 成正比。为了简化起见，大多数研究假设 P(D) 呈均匀分布。主要重点是将 P(Q|D) 建模为排序函数。通过将查询视为一组独立术语 Q={ti}n i=1，我们有 P(Q|D) =∏ ti∈QP(ti|D)。概率 P(ti|D) 使用表示文档的统计语言模型 θD 来确定。

### 段落 35 · Page 6

**EN**

The relevance is then estimated by log-likelihood: Score(Q,D) = logP(Q|θD) =∑ ti∈QlogP(ti|θD),where the estimation of the language modelθD is usually achieved by maximum likelihood. The statistical language models for IR (Miller et al., 1999; Berger & Lafferty, 1999; Song & Croft, 1999; Hiemstra & Kraaij, 1999) also encounter the problem of zero occurrences of a query termt i, i.e., the probabilityP(Q|θD)becomes zero if a query termti does not appear in the document. This is too restrictive for IR, as a document can still be relevant even if it contains only some of the query terms.

**中文**

然后通过对数似然估计相关性：Score(Q,D) = logP(Q|θD) =Σ ti∈QlogP(ti|θD)，其中语言模型θD的估计通常通过最大似然来实现。 IR 的统计语言模型 (Miller et al., 1999; Berger & Lafferty, 1999; Song & Croft, 1999; Hiemstra & Kraaij, 1999) 也遇到查询项 i 出现次数为零的问题，即如果查询项 ti 没有出现在文档中，则概率 P(Q|θD) 变为零。这对于 IR 来说限制太大，因为即使文档仅包含一些查询术语，它仍然可能是相关的。

### 段落 36 · Page 6

**EN**

To address this zero-probability issue, smoothing techniques are applied, assigning small probabilities to terms that do not appear in the document. The principle behind smoothing is that any text used to model a language capturesonlyalimitedsubsetofitslinguisticpatterns(orterms, inthiscase). Thecommonlyusedsmoothing methods (Zhai & Lafferty, 2004; Zhai et al., 2008) include Jelinek-Mercer smoothing (Jelinek, 1980), Dirichlet smoothing (MacKay & Peto, 1995), etc. These foundational models, while useful, share a common characteristic: they rely on heuristic-based scoring functions derived from statistical properties of terms.

**中文**

为了解决这个零概率问题，应用了平滑技术，为文档中未出现的术语分配小概率。平滑背后的原理是，任何用于对语言建模的文本仅捕获其语言模式（或本例中的术语）的有限子集。常用的平滑方法（Zhai & Lafferty，2004；Zhai et al.，2008）包括 Jelinek-Mercer 平滑（Jelinek，1980）、Dirichlet 平滑（MacKay & Peto，1995）等。这些基础模型虽然有用，但有一个共同的特征：它们依赖于从术语的统计特性导出的基于启发式的评分函数。

### 段落 37 · Page 6

**EN**

Although their parameters can be tuned (e.g.,k1 andbin BM25), the functional form of the model is fixed. A natural evolution is to frame ranking as a supervised machine learning task, where a model learns to combine various signals of relevance automatically from labeled data. This approach allows for the systematic combination of not only scores from traditional models like BM25 but also a multitude of other features describing the query, the document, and their interaction. This paradigm shift from hand-crafted formulas to learned functions is the core idea behind Learning-to-Rank models, which we discuss next.

**中文**

尽管它们的参数可以调整（例如，k1 和 bin BM25），但模型的函数形式是固定的。自然的演变是将排名构建为监督机器学习任务，其中模型学习自动组合来自标记数据的各种相关信号。这种方法不仅可以系统地组合 BM25 等传统模型的分数，还可以系统地组合描述查询、文档及其交互的大量其他特征。这种从手工公式到学习函数的范式转变是学习排序模型背后的核心思想，我们接下来将讨论这一点。

### 段落 38 · Page 6

**EN**

4 Learning-to-Rank Model Architectures Different from traditional IR models that rely on heuristic-based scoring formulas (Section 3), Learningto-Rank (LTR) frames ranking as a supervised machine learning problem (Liu, 2009). The core idea is to train a model that can optimally combine a wide array of signals, or “features”, to predict the relevance of documents to a query. For each query-document pair(Qi,Di), ak-dimensional feature vectorx i∈Rk is extracted, and a relevance labelyi (e.g., from human judgments) is provided.

**中文**

4 Learning-to-Rank 模型架构 与依赖启发式评分公式（第 3 节）的传统 IR 模型不同，Learningto-Rank (LTR) 将排名框架视为监督机器学习问题（Liu，2009）。核心思想是训练一个模型，该模型可以最佳地组合各种信号或“特征”，以预测文档与查询的相关性。对于每个查询文档对（Qi，Di），提取ak维特征向量x i∈Rk，并提供相关性标签yi（例如，来自人类判断）。

### 段落 39 · Page 6

**EN**

The goal is to learn a ranking modelfparameterized byθthat minimizes an empirical lossl(·)on a labeled training setΨ: L= 1 |Ψ| ∑ (xi,yi)∈Ψ l(fθ(xi),y i). 6

**中文**

目标是学习一个由 θ 参数化的排序模型 f，该模型最小化标记训练集 Ψ 上的经验损失 l(·)：L= 1 |Ψ| Σ (xi,yi)∈Ψ l(fθ(xi),y i)。 6

### Page 7

### 段落 40 · Page 7

**EN**

Published in Transactions on Machine Learning Research (02/2026) Table 1: A list of learning-to-rank works and their model architectures.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 表 1：学习排名作品及其模型架构列表。

### 段落 41 · Page 7

**EN**

Name Backbone Architecture Loss Function MART(Friedman, 2001) Boosting Pointwise RankBoost(Freund et al., 2003) Boosting Pairwise RankNet(Burges et al., 2005) Neural Network Pairwise RankSVM(Joachims, 2006) SVM Pairwise LambdaRank(Burges et al., 2006) Neural Network Pairwise ListNet(Cao et al., 2007) Neural Network Listwise SoftRank(Taylor et al., 2008) Neural Network Listwise ListMLE(Xia et al., 2008) Linear Listwise LambdaMART(Burges, 2010) GBDT Listwise ApproxNDCG(Qin et al., 2010) Linear Listwise DLCM(Ai et al., 2018a) Neural Network Listwise GSF(Ai et al., 2019) Neural Network Listwise ApproxNDCG(Bruch et al., 2019) Neural Network Listwi

**中文**

名称 主干架构损失函数 MART(Friedman, 2001) Boosting Pointwise RankBoost(Freund et al., 2003) Boosting Pairwise RankNet(Burges et al., 2005) 神经网络 Pairwise RankSVM(Joachims, 2006) SVM Pairwise LambdaRank(Burges et al., 2006) 神经网络 Pairwise ListNet(Cao et al., 2007) 神经网络 Listwise SoftRank(Taylor et al., 2008) 神经网络 Listwise ListMLE(Xia et al., 2008) Linear Listwise LambdaMART(Burges, 2010) GBDT Listwise ApproxNDCG(Qin et al., 2010) Linear Listwise DLCM(Ai et al., 2018a)神经网络 Listwise GSF(Ai et al., 2019) 神经网络 Listwise ApproxNDCG(Bruch et al., 2019) 神经网络 Listwi

### 段落 42 · Page 7

**EN**

se SetRank(Pang et al., 2020) Self Attention Blocks Listwise LTR methods are typically categorized into three main approaches based on their input and loss function: pointwise, pairwise, and listwise.

**中文**

se SetRank(Pang et al., 2020) 自注意力块列表 LTR 方法通常根据其输入和损失函数分为三种主要方法：点式、成对式和列表式。

### 段落 43 · Page 7

**EN**

Feature Engineering in LTR.A cornerstone of traditional LTR is the meticulous engineering of the feature vectorxi. These features are designed to capture diverse aspects of relevance and can be grouped into several categories: (1)Query-based features, such as the number of terms in the query; (2)Documentbased features, which are query-independent, such as document length, PageRank (Brin & Page, 1998), or the number of incoming URL links; and (3)Query-document interaction features, which form the largest and most critical group.

**中文**

LTR 中的特征工程。传统 LTR 的基石是特征向量xi 的细致工程。这些特征旨在捕获相关性的各个方面，并且可以分为几类：（1）基于查询的特征，例如查询中的术语数量； （2）基于文档的特征，与查询无关，例如文档长度、PageRank（Brin & Page，1998）或传入 URL 链接的数量； (3)查询-文档交互特征，这是最大、最关键的一组。

### 段落 44 · Page 7

**EN**

This category includes scores from traditional IR models like BM25 and language models, counts of matching terms, proximity features measuring how close query terms are in the document, and various TF-IDF-related statistics. The power of LTR lies in its ability to learn complex, non-linear combinations of these diverse signals, moving beyond what a single hand-tuned formula could achieve. 4.1 Pointwise, Pairwise, and Listwise Approaches with ML Models The pointwise approach is the simplest, treating each document independently.

**中文**

此类别包括传统 IR 模型（如 BM25 和语言模型）的分数、匹配术语的计数、衡量查询术语在文档中的接近程度的邻近特征以及各种 TF-IDF 相关统计数据。 LTR 的强大之处在于它能够学习这些不同信号的复杂、非线性组合，这超出了单个手动调整公式所能实现的范围。 4.1 ML 模型的逐点、成对和列表方法 逐点方法是最简单的，独立处理每个文档。

### 段落 45 · Page 7

**EN**

It frames the problem as a regression or classification task, where the modelf(xi)aims to predict the exact relevance labelyi. While straightforward, this approach ignores the crucial fact that ranking is about the relative order of documents, not their absolute scores (Burges, 2010). The pairwise approach addresses this by focusing on the relative order of document pairs. Given two documentsD i andD j for the same query, the goal is to predict which one is more relevant. This transforms ranking into a binary classification problem.

**中文**

它将问题描述为回归或分类任务，其中 modelf(xi) 旨在预测确切的相关性 labelyi。虽然简单，但这种方法忽略了一个重要事实，即排名是关于文档的相对顺序，而不是它们的绝对分数（Burges，2010）。成对方法通过关注文档对的相对顺序来解决这个问题。给定同一查询的两个文档D i 和D j，目标是预测哪一个更相关。这将排序问题转化为二元分类问题。

### 段落 46 · Page 7

**EN**

Seminal pairwise models includeRankSVM(Joachims, 2006), which adapts the Support Vector Machine framework to maximize the number of correctly ordered pairs, andRankNet(Burges et al., 2005), which uses a neural network and a probabilistic cost function based on pairwise logistic loss. While more aligned with the nature of ranking than the pointwise approach, pairwise methods still do not directly optimize the list-based evaluation metrics (e.g., nDCG, MRR) that are standard in IR evaluation. The listwise approach directly tackles this issue by defining the loss function over an entire list of documents for a given query.

**中文**

开创性的成对模型包括RankSVM（Joachims，2006），它采用支持向量机框架来最大化正确排序对的数量，以及RankNet（Burges et al.，2005），它使用神经网络和基于成对逻辑损失的概率成本函数。虽然比逐点方法更符合排名的本质，但成对方法仍然不能直接优化 IR 评估标准的基于列表的评估指标（例如，nDCG、MRR）。列表方法通过为给定查询的整个文档列表定义损失函数来直接解决这个问题。

### 段落 47 · Page 7

**EN**

These methods aim to directly optimize ranking metrics. A pivotal line of work began with LambdaRank(Burges et al., 2006), which observed that for gradient-based optimization, one only needs the gradients of the loss function. It introduced “Lambda gradients”, which are derived from the change in an IR metric (like nDCG) when two documents in a ranked list are swapped. This technique was then combined with Multiple Additive Regression Trees (MART), a Gradient Boosted Decision Tree (GBDT) 7

**中文**

这些方法旨在直接优化排名指标。一项关键的工作始于 LambdaRank（Burges 等，2006），它观察到对于基于梯度的优化，只需要损失函数的梯度。它引入了“Lambda 梯度”，它源自交换排名列表中的两个文档时 IR 指标（如 nDCG）的变化。然后将该技术与多重加性回归树 (MART)、梯度提升决策树 (GBDT) 7 相结合

### Page 8

### 段落 48 · Page 8

**EN**

Published in Transactions on Machine Learning Research (02/2026) customized deep network relevance score word embeddings where is whitemarsh island the strategy of island ... word embeddings customized deep network (a) Representation-based neural reranker word embeddings where is whitemarsh island the strategy of island ... word embeddings customized deep network relevance score (b) Interaction-based neural reranker Figure 2: Illustration on neural ranking models. Brown boxes indicate uncontextualized word embeddings (e.g., Word2vec). algorithm (Friedman, 2001), to createLambdaMART(Wu et al., 2010).

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 定制深度网络相关性评分词嵌入 定制深度网络 (a) 基于表示的神经重排序词嵌入 定制深度网络相关性评分 (b) 基于交互的神经重排序 图 2：神经排序模型图示。棕色框表示无上下文的词嵌入（例如，Word2vec）。算法（Friedman，2001），创建 LambdaMART（Wu 等人，2010）。

### 段落 49 · Page 8

**EN**

Due to its strong performance and robustness,LambdaMARTbecame a dominant industry standard for many years (Ke et al., 2017). 4.2 Neural LTR Models WhileLambdaMARTrepresents a peak for GBDT-based LTR, early works also explored neural networks for the ranking functionfθ.RankNetandLambdaRankboth parameterized the LTR model with neural networks. More recent works such asGSF(Ai et al., 2019) andApproxNDCG(Bruch et al., 2019) have continued this trend, using multiple fully connected layers and designing differentiable approximations of IR metrics.

**中文**

由于其强大的性能和稳健性，LambdaMART 多年来成为主导行业标准（Ke et al., 2017）。 4.2 神经LTR模型虽然LambdaMART代表了基于GBDT的LTR的顶峰，但早期的工作也探索了排序函数fθ的神经网络。RankNet和LambdaRank都用神经网络参数化了LTR模型。最近的工作，如 GSF（Ai 等人，2019）和 ApproxNDCG（Bruch 等人，2019）延续了这一趋势，使用多个全连接层并设计 IR 度量的可微近似。

### 段落 50 · Page 8

**EN**

Other architectures likeDLCM(Ai et al., 2018a), based on RNNs, andSetRank(Pang et al., 2020), using self-attention, explore ways to model the entire document list jointly. A rigorous benchmark by Qin et al. (2021) compared the performance of these modern neural ranking models against strong GBDT-based baselines. A summary of LTR models and their backbone architectures is provided in Table 1. 4.3 Orthogonal Directions Beyond core model architectures, LTR research has explored many other important directions.

**中文**

其他架构如基于 RNN 的 DLCM（Ai et al., 2018a）和 SetRank（Pang et al., 2020），使用自注意力机制，探索联合建模整个文档列表的方法。秦等人的严格基准。 (2021) 将这些现代神经排序模型的性能与基于 GBDT 的强大基线进行了比较。表 1 总结了 LTR 模型及其主干架构。 4.3 正交方向 除了核心模型架构之外，LTR 研究还探索了许多其他重要方向。

### 段落 51 · Page 8

**EN**

A significant portion of the literature focuses on loss functions and feature transformations (Qin et al., 2021; Bruch et al., 2019; Burges, 2010). Other critical areas include developing methods for unbiased relevance estimation from biased user feedback (e.g., clicks) (Joachims et al., 2017; Ai et al., 2018b; Wang et al., 2018; Hu et al., 2019) and jointly optimizing for both effectiveness and fairness in ranking systems (Singh & Joachims, 2018; Biega et al., 2018; Yang et al., 2023b;a;c). We omit detailed discussions here and refer readers to the original papers and prior surveys (Liu, 2009; Li, 2011).

**中文**

文献的很大一部分集中在损失函数和特征转换上（Qin 等人，2021；Bruch 等人，2019；Burges，2010）。其他关键领域包括开发根据有偏见的用户反馈（例如点击）进行无偏见相关性估计的方法（Joachims 等人，2017 年；Ai 等人，2018b；Wang 等人，2018 年；Hu 等人，2019 年）以及联合优化排名系统的有效性和公平性（Singh 和 Joachims，2018 年；Biega 等人，2018 年；Yang 等人）等人，2023b；a；c)。我们在此省略详细讨论，请读者参考原始论文和之前的调查（Liu，2009；Li，2011）。

### 段落 52 · Page 8

**EN**

Despite their success, traditional LTR models have a fundamental ceiling. Their reliance on handcrafted features prevents them from operating in an end-to-end manner and, more importantly, limits their ability to bridge thelexical gap—the difference between the words in a query and the semantically related words in a relevant document. Their understanding is based on pre-defined statistical signals, not the underlying meaning of the text. This limitation created a clear need for a new class of models capable of learning semantic representations directly from raw text, setting the stage for the rise of neural ranking (Section 5).

**中文**

尽管取得了成功，传统的 LTR 模型仍然存在根本性的上限。它们对手工特征的依赖阻止了它们以端到端的方式操作，更重要的是，限制了它们弥合词汇差距（查询中的单词与相关文档中语义相关单词之间的差异）的能力。他们的理解基​​于预先定义的统计信号，而不是文本的潜在含义。这种限制显然需要一类能够直接从原始文本学习语义表示的新型模型，为神经排序的兴起奠定了基础（第 5 节）。

### 段落 53 · Page 8

**EN**

5 Neural Ranking Models Neural ranking models emerged to directly address the key limitations of LTR (Section 4). By learning semantic representations directly from raw text, they could automatically bridge the lexical gap—for instance, recognizing that a query for “computer” is conceptually related to a document about a “PC” without relying on term overlap. This end-to-end approach simultaneously eliminated the laborious process of manual 8

**中文**

5 神经排序模型 神经排序模型的出现是为了直接解决 LTR 的关键局限性（第 4 节）。通过直接从原始文本学习语义表示，他们可以自动弥合词汇差距，例如，认识到对“计算机”的查询在概念上与有关“PC”的文档相关，而不依赖于术语重叠。这种端到端方法同时消除了手动 8 的繁琐过程

### Page 9

### 段落 54 · Page 9

**EN**

Published in Transactions on Machine Learning Research (02/2026) feature engineering, shifting the paradigm from engineering statistical signals to learning semantic patterns from data.1 Depending on how queries interact with documents during network processing, neural ranking models can be roughly divided intorepresentation-based modelsandinteraction-based models(Guo et al., 2016a). This division reflects a fundamental tradeoff between efficiency and matching depth. Representation-based models pre-encode documents into vectors offline, enabling highly efficient retrieval suitable for first-pass ranking.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 特征工程，将范式从工程统计信号转变为从数据中学习语义模式。1 根据网络处理过程中查询与文档的交互方式，神经排序模型可以大致分为基于表示的模型和基于交互的模型（Guo et al., 2016a）。这种划分反映了效率和匹配深度之间的基本权衡。基于表示的模型将文档离线预编码为向量，从而实现适合首次通过排序的高效检索。

### 段落 55 · Page 9

**EN**

In contrast, interaction-based models process the query and document together, allowing for deeper and more precise matching at a higher computational cost, making them ideal for reranking a smaller set of candidates. 5.1 Representation-Based Models ThisgenreofmodelscanberegardedasanextensionofVectorSpaceModels(Section3), whichindependently encodequeriesanddocumentsintoasharedlatentvectorspace, whererelevanceisdeterminedthroughsimple comparison functions such as cosine similarity or dot product, as illustrated in Figure 2a.

**中文**

相比之下，基于交互的模型一起处理查询和文档，允许以更高的计算成本进行更深入、更精确的匹配，这使得它们非常适合对较小的候选集进行重排。 5.1 基于表示的模型 这种类型的模型可以被视为向量空间模型（第 3 节）的扩展，它将查询和文档独立地编码到共享的潜在向量空间中，其中相关性是通过简单的比较函数（例如余弦相似度或点积）确定的，如图 2a 所示。

### 段落 56 · Page 9

**EN**

This approach maintains clear separation between query and document processing, with no interaction occurring during the encoding procedure. The core architectural challenge is designing an encoder network that transforms a variable-length sequence of term embeddings into a single, fixed-size semantic vector. The Deep Structured Semantic Model (DSSM,Huang et al., 2013; Gao et al., 2014) is an early example.

**中文**

这种方法在查询和文档处理之间保持清晰的分离，在编码过程中不会发生交互。核心架构挑战是设计一个编码器网络，将可变长度的术语嵌入序列转换为单个固定大小的语义向量。深层结构化语义模型（DSSM，Huang et al., 2013；Gao et al., 2014）是一个早期的例子。

### 段落 57 · Page 9

**EN**

It utilizes word hashing (a technique to manage large vocabularies by grouping words into a smaller number of hash buckets) and multilayer perceptrons (MLPs) to independently encode term vectors of queries and documents, enabling the computation of ranking scores based on the cosine similarity of their embeddings. Later works modifyDSSM’s encoder network to better capture richer semantic and contextual information. ConvolutionalDSSM(C-DSSM, Shen et al., 2014a) leverages a convolutional neural network (CNN) architecture.

**中文**

它利用单词哈希（一种通过将单词分组到较少数量的哈希桶中来管理大型词汇表的技术）和多层感知器 (MLP) 来独立编码查询和文档的术语向量，从而能够根据其嵌入的余弦相似度计算排名分数。后来的工作修改了 DSSM 的编码器网络，以更好地捕获更丰富的语义和上下文信息。卷积 DSSM（C-DSSM，Shen 等人，2014a）利用卷积神经网络 (CNN) 架构。

### 段落 58 · Page 9

**EN**

Specifically, it applies 1D convolutions over the sequence of word embeddings, allowing the model to learn representations for n-grams and local phrases. A max-pooling layer then selects the most salient local features to form the final document vector. Another variant ofDSSMreplaces MLPs with recurrent layers such as Long Short-Term Memory (LSTM) network (Hochreiter & Schmidhuber, 1997; Palangi et al., 2016; Wan et al., 2016; Cohen & Croft, 2016) or tree-structured networks (Tai et al., 2015).

**中文**

具体来说，它对词嵌入序列应用一维卷积，使模型能够学习 n 元语法和局部短语的表示。然后，最大池层选择最显着的局部特征来形成最终的文档向量。 DSSM 的另一种变体用循环层替换 MLP，例如长短期记忆 (LSTM) 网络 (Hochreiter & Schmidhuber, 1997; Palangi et al., 2016; Wan et al., 2016; Cohen & Croft, 2016) 或树结构网络 (Tai et al., 2015)。

### 段落 59 · Page 9

**EN**

The LSTM processes the text sequentially, and its recurrent nature allows it to capture word order and long-range dependencies across the entire text, with the final hidden state often used as the comprehensive representation for the query or document. Based on the assumption of documents’ hierarchical structure, Yang et al. (2016b); Song et al. (2018); Zhu et al. (2019) use attention (Bahdanau et al., 2014) to model token, phrase and sentence representations for enhanced document/passage representations. In line with these works, the NLP community has also extensively investigated passage/document representations.

**中文**

LSTM 按顺序处理文本，其循环性质使其能够捕获整个文本中的词序和长程依赖性，最终的隐藏状态通常用作查询或文档的综合表示。基于文档层次结构的假设，Yang 等人。 （2016b）；宋等人。 （2018）；朱等人。 (2019) 使用注意力机制 (Bahdanau et al., 2014) 对标记、短语和句子表示进行建模，以增强文档/段落表示。与这些工作一致，NLP 社区还广泛研究了段落/文档表示。

### 段落 60 · Page 9

**EN**

Le & Mikolov (2014) proposed Paragraph Vectors (Doc2Vec), an unsupervised algorithm that learns fixed-length feature representations from variable-length pieces of texts, which is based on single-hidden-layer neural network. Kim (2014) studied CNN for sentence representations, while Wieting et al. (2016) proposed to use LSTM network. Arora et al. (2017) reported a weighted average of pre-trained word embeddings fine-tuned with unsupervised random walk algorithm can outperform more complex neural networks on the sentence similarity task.

**中文**

Le & Mikolov (2014) 提出了段落向量 (Doc2Vec)，这是一种基于单隐藏层神经网络的无监督算法，可以从可变长度的文本片段中学习固定长度的特征表示。 Kim (2014) 研究了 CNN 的句子表示，而 Wieting 等人。 (2016) 提出使用 LSTM 网络。阿罗拉等人。 (2017) 报道了使用无监督随机游走算法微调的预训练词嵌入的加权平均值可以在句子相似性任务上胜过更复杂的神经网络。

### 段落 61 · Page 9

**EN**

However, weighted averaging word embeddings ignores the word order, which fails to capture the rich, contextual information in longer, more complex documents. To summarize, representation-based models excel in scenarios requiring global semantic understanding and offer significant computational advantages through their ability to pre-compute document representations offline (Guo et al., 2020).

**中文**

然而，加权平均词嵌入忽略了词序，这无法捕获更长、更复杂的文档中丰富的上下文信息。总而言之，基于表示的模型在需要全局语义理解的场景中表现出色，并通过其离线预先计算文档表示的能力提供显着的计算优势（Guo et al., 2020）。

### 段落 62 · Page 9

**EN**

However, these approaches also face inherent limitations due to their reliance on fixed-size embedding vectors, which can struggle to capture all relevant information from the original text and may not effectively handle precise lexical matching requirements. These limitations are the focus of interaction-based models. 1For structural clarity, this section focuses on neural information retrieval, covering neural network–based retrieval models developed prior to the advent of pre-trained transformers. For a more comprehensive treatment, we refer readers to the dedicated surveys (Onal et al., 2018; Mitra et al., 2018; Xu et al., 2018). 9

**中文**

然而，这些方法也面临着固有的局限性，因为它们依赖于固定大小的嵌入向量，这可能很难从原始文本中捕获所有相关信息，并且可能无法有效地处理精确的词汇匹配要求。这些限制是基于交互的模型的焦点。 1为了结构清晰，本节重点介绍神经信息检索，涵盖在预训练 Transformer 出现之前开发的基于神经网络的检索模型。为了获得更全面的处理，我们建议读者参阅专门的调查（Onal 等人，2018 年；Mitra 等人，2018 年；Xu 等人，2018 年）。 9

### Page 10

### 段落 63 · Page 10

**EN**

Published in Transactions on Machine Learning Research (02/2026) 5.2 Interaction-Based Models Different from representation-based models, interaction-based models (Figure 2b) process queries and documents jointly through neural networks. Instead of compressing each text into a single vector, they first build a detailed, low-level interaction representation between the query and the document, and then use neural networks to learn hierarchical matching patterns from this representation. The model’s output is typically a scalar relevance score of the input query-document pair.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 5.2 基于交互的模型 与基于表示的模型不同，基于交互的模型（图 2b）通过神经网络联合处理查询和文档。他们没有将每个文本压缩为单个向量，而是首先在查询和文档之间构建详细的低级交互表示，然后使用神经网络从该表示中学习分层匹配模式。该模型的输出通常是输入查询-文档对的标量相关性得分。

### 段落 64 · Page 10

**EN**

Various network architectures have been proposed under this paradigm.MatchPyramid(Pang et al., 2016) employs CNN over the interaction matrix between query and document terms. The interaction matrix is treated as an image, allowing the CNN with its 2D filters to capture local matching patterns (e.g., phrases or bigrams matching) through convolution and pooling operations (Hu et al., 2014). Building upon the concept of interaction-focused models, Guo et al. (2016a) highlighted the importance of exact term matches in neural ranking models and proposed the Deep Relevance Matching Model (DRMM).

**中文**

在这种范式下，已经提出了各种网络架构。MatchPyramid（Pang et al., 2016）在查询和文档术语之间的交互矩阵上采用 CNN。交互矩阵被视为图像，允许 CNN 及其 2D 滤波器通过卷积和池化操作捕获局部匹配模式（例如，短语或二元组匹配）（Hu et al., 2014）。基于以交互为中心的模型的概念，Guo 等人。 (2016a) 强调了神经排序模型中精确术语匹配的重要性，并提出了深度相关性匹配模型 (DRMM)。

### 段落 65 · Page 10

**EN**

Rather than a single interaction matrix,DRMMcreates a matching histogram for each query term. This histogram discretizes the similarity scores against all document terms into bins, effectively capturing the distribution of matching signals (e.g., how many terms in the document are an exact match, a strong semantic match, or a weak match to a given query term). An MLP then learns the relevance contribution from these histogram features. Kernel-Based Neural Ranking Model (K-NRM, Xiong et al., 2017) further advances interaction-based approaches.

**中文**

DRMM 不是单个交互矩阵，而是为每个查询项创建一个匹配直方图。该直方图将所有文档术语的相似度分数离散化为箱，有效地捕获匹配信号的分布（例如，文档中有多少术语与给定的查询术语完全匹配、强语义匹配或弱匹配）。然后 MLP 从这些直方图特征中学习相关性贡献。基于内核的神经排序模型（K-NRM，Xiong 等人，2017）进一步推进了基于交互的方法。

### 段落 66 · Page 10

**EN**

It employs radial basis function (RBF) kernels to transform the query-document interaction matrix into a more informative feature representation. Each kernel corresponds to a certain similarity level (e.g., “exact match”, “strong match”, “weak match”). The model uses these kernels to produce “soft-TF” counts for each query term—counting how many document words match the query term at each similarity level. These soft-match features are then aggregated and fed into a simple feed-forward network to compute the final relevance score.

**中文**

它采用径向基函数（RBF）内核将查询-文档交互矩阵转换为信息更丰富的特征表示。每个内核对应于一定的相似性级别（例如，“完全匹配”、“强匹配”、“弱匹配”）。该模型使用这些内核为每个查询项生成“软 TF”计数，即计算每个相似度级别上有多少文档单词与查询项匹配。然后，这些软匹配特征被聚合并输入到一个简单的前馈网络中，以计算最终的相关性得分。

### 段落 67 · Page 10

**EN**

This kernel-based mechanism enables models to capture nuanced matching features, enhancing their ability to model complex query-document interactions.Conv-KNRM(Dai et al., 2018) later extends it to convolutional kernels to capture n-gram level soft matches, further improving matching granularity. In line with these works, the interaction matrix-based approach have been explored for short text matching (Lu & Li, 2013; Yin et al., 2016; Yang et al., 2016a) as well as long document ranking (Mitra et al., 2017; Hui et al., 2017; 2018,inter alia).

**中文**

这种基于内核的机制使模型能够捕获细致入微的匹配特征，从而增强模型复杂查询-文档交互的能力。Conv-KNRM（Dai et al., 2018）后来将其扩展到卷积内核以捕获 n-gram 级别的软匹配，进一步提高匹配粒度。与这些工作一致，基于交互矩阵的方法已经被探索用于短文本匹配（Lu＆Li，2013；Yin等人，2016；Yang等人，2016a）以及长文档排名（Mitra等人，2017；Hui等人，2017；2018等）。

### 段落 68 · Page 10

**EN**

Multi-Perspective CNN approaches compare sentences via diverse pooling functions and filter widths to capture multiple perspectives between texts He et al. (2015).aNMM(Yang et al., 2016a), as an example of attention-based methods, computes passage terms’ attention weights over query terms using a query attention network and achieves performance improvement compared to CNNbased baseline (Severyn & Moschitti, 2015). Term adjacency and positional information represent another important dimension of interaction modeling.

**中文**

多视角 CNN 方法通过不同的池化函数和过滤器宽度来比较句子，以捕获文本之间的多个视角。 (2015).aNMM(Yang et al., 2016a) 作为基于注意力的方法的一个例子，使用查询注意力网络计算段落术语相对于查询术语的注意力权重，并与基于 CNN 的基线相比实现了性能改进 (Severyn & Moschitti, 2015)。术语邻接和位置信息代表交互建模的另一个重要维度。

### 段落 69 · Page 10

**EN**

Models such asMatchPyramid,PACRR, andConvKNRM capture term adjacency patterns and position-dependent interactions (Pang et al., 2016; Hui et al., 2017; Dai et al., 2018). The interaction functions in these models can be categorized as either non-parametric (using traditional similarity measures like cosine similarity, dot product, or binary indicators) or parametric (learning similarity functions from data through neural networks) (Dong et al., 2022b).

**中文**

MatchPyramid、PACRR 和 ConvKNRM 等模型捕获项邻接模式和位置相关的交互（Pang 等人，2016；Hui 等人，2017；Dai 等人，2018）。这些模型中的交互函数可以分为非参数（使用传统的相似性度量，如余弦相似性、点积或二元指标）或参数（通过神经网络从数据中学习相似性函数）（Dong 等人，2022b）。

### 段落 70 · Page 10

**EN**

While interaction-focused models require one forward pass through the entire model for each potentially relevant document, making them computationally more expensive than representation-focused approaches, they typically achieve superior ranking quality due to their ability to capture fine-grained matching signals. We list some representative works in Table 2 and direct readers to these works for architectural details.

**中文**

虽然以交互为中心的模型需要对每个潜在相关文档对整个模型进行一次前向传递，这使得它们在计算上比以表示为中心的方法更昂贵，但由于它们能够捕获细粒度的匹配信号，它们通常会实现卓越的排名质量。我们在表2中列出了一些代表性作品，并引导读者查看这些作品以了解建筑细节。

### 段落 71 · Page 10

**EN**

5.3 Hybrid Models Recognizing the complementary strengths of representation-focused and interaction-focused architectures, researchers have proposed hybrid models that combine the efficiency of representation-based methods with the effectiveness of interaction-based approaches. These models represent a third category in neural ranking architectures, alongside the two primary approaches. 10

**中文**

5.3 混合模型认识到以表示为中心和以交互为中心的架构的互补优势，研究人员提出了混合模型，将基于表示的方法的效率与基于交互的方法的有效性结合起来。除了两种主要方法之外，这些模型代表了神经排序架构中的第三类。 10

### Page 11

### 段落 72 · Page 11

**EN**

Published in Transactions on Machine Learning Research (02/2026) Table 2: A list of neural ranking models and their model architectures. Name Architecture Backbone Embeddings DSSM(Huang et al., 2013) Representation-based MLP Semantic Hashing CDSSM(Shen et al., 2014a) Representation-based CNN Semantic Hashing CLSM(Shen et al., 2014b) Representation-based CNN Semantic Hashing ARC-I(Hu et al., 2014) Representation-based CNN Word2Vec Tai et al.

**中文**

发表于机器学习研究交易 (02/2026) 表 2：神经排序模型及其模型架构的列表。名称 架构骨干嵌入 DSSM(Huang et al., 2013) 基于表示的 MLP 语义哈希 CDSSM(Shen et al., 2014a) 基于表示的 CNN 语义哈希 CLSM(Shen et al., 2014b) 基于表示的 CNN 语义哈希 ARC-I(Hu et al., 2014) 基于表示的 CNN Word2Vec Tai 等人。

### 段落 73 · Page 11

**EN**

(2015) Representation-based Tree-structured LSTM GloVe LSTM-RNN(Palangi et al., 2016) Representation-based LSTM Randomly Initialized MV-LSTM(Wan et al., 2016) Representation-based Bi-LSTM Word2Vec DESMNalisnick et al.

**中文**

(2015) 基于表示的树结构 LSTM GloVe LSTM-RNN(Palangi et al., 2016) 基于表示的 LSTM 随机初始化 MV-LSTM(Wan et al., 2016) 基于表示的 Bi-LSTM Word2Vec DESMNalisnick 等。

### 段落 74 · Page 11

**EN**

(2016) Representation-based MLP Randomly Initialized Lu & Li (2013) Representation-based MLP Randomly Initialized ARC-II(Hu et al., 2014) Interaction-based CNN Word2Vec MatchPyramid(Pang et al., 2016)Interaction-based CNN Randomly Initialized DRMM(Guo et al., 2016a) Interaction-based MLP Word2Vec ABCNN(Yin et al., 2016) Interaction-based CNN + Attention Word2Vec aNMM(Yang et al., 2016a) Interaction-based Attention Word2Vec DESM(Nalisnick et al., 2016) Interaction-based MLP Word2Vec K-NRM(Xiong et al., 2017) Interaction-based MLP + RBF kernels Word2Vec Conv-KNRM(Dai et al., 2018) Interaction-based CNN Word2Vec PACRR(Hui et al., 2017) Interacti

**中文**

(2016) 基于表示的 MLP 随机初始化 Lu & Li (2013) 基于表示的 MLP 随机初始化 ARC-II(Hu et al., 2014) 基于交互的 CNN Word2Vec MatchPyramid(Pang et al., 2016) 基于交互的 CNN 随机初始化 DRMM(Guo et al., 2016a) 基于交互的 MLP Word2Vec ABCNN(Yin et al., 2016) 基于交互的 CNN + Attention Word2Vec aNMM(Yang et al., 2016a) 基于交互的 Attention Word2Vec DESM(Nalisnick et al., 2016) 基于交互的 MLP Word2Vec K-NRM(Xiong et al., 2017) 基于交互的 MLP + RBF 内核Word2Vec Conv-KNRM(Dai et al., 2018) Interaction-based CNN Word2Vec PACRR(Hui et al., 2017) Interacti

### 段落 75 · Page 11

**EN**

on-based CNN + RNN Word2Vec Co-PACRR(Hui et al., 2018) Interaction-based CNN Word2Vec TK(Hofstätter et al., 2020c) Interaction-based Transformer + Kernel GloVe TKL(Hofstätter et al., 2020a) Interaction-based Transformer + Kernel GloVe NDRM(Mitra et al., 2021) Interaction-based Conformer + Kernel BERT The most notable example isDUET(Mitra et al., 2017), which employs two separate deep neural networks operating in parallel.

**中文**

on-based CNN + RNN Word2Vec Co-PACRR(Hui et al., 2018) 基于交互的 CNN Word2Vec TK(Hofstätter et al., 2020c) 基于交互的 Transformer + Kernel GloVe TKL(Hofstätter et al., 2020a) 基于交互的 Transformer + Kernel GloVe NDRM(Mitra et al., 2020a) 2021）基于交互的Conformer + Kernel BERT 最值得注意的例子是DUET（Mitra et al., 2017），它采用两个并行运行的独立深度神经网络。

### 段落 76 · Page 11

**EN**

One network performs local interaction-based matching similar to interaction-focused models, while the other learns distributed representations for query and document separately, similar to representation-focused approaches. The term interaction matrix between query and document feeds into the exact matching layers, while term embeddings of the input sequence enter the semantic matching layers. The outputs from both networks are then combined using a fully connected network to produce the final ranking score.

**中文**

一个网络执行基于本地交互的匹配，类似于以交互为中心的模型，而另一个网络则分别学习查询和文档的分布式表示，类似于以表示为中心的方法。查询和文档之间的术语交互矩阵馈入精确匹配层，而输入序列的术语嵌入进入语义匹配层。然后使用完全连接的网络组合两个网络的输出以产生最终的排名分数。

### 段落 77 · Page 11

**EN**

Different from the metric learning theme of representation-based models, a line of works formulates the ranking problem as a classification problem (commonly referred to asExtreme Label Classification, or XMC), where the input is the query, and the output is a probability distribution over the corpus, where each document is a unique “class” or “label”. Instead of optimizing the similarity between query and document representations, XMC models aim to predict the correct subset of relevant document IDs (Prabhu & Varma, 2014; Jain et al., 2016; Liu et al., 2017; Jain et al., 2019).

**中文**

与基于表示的模型的度量学习主题不同，一系列工作将排名问题表述为分类问题（通常称为极端标签分类，或 XMC），其中输入是查询，输出是语料库上的概率分布，其中每个文档是唯一的“类”或“标签”。 XMC 模型不是优化查询和文档表示之间的相似性，而是旨在预测相关文档 ID 的正确子集（Prabhu & Varma，2014；Jain 等人，2016；Liu 等人，2017；Jain 等人，2019）。

### 段落 78 · Page 11

**EN**

In the inference time, XMC methods use tree-based hierarchies or cluster-based sampling to quickly narrow down the search path to the likely labels without scanning every candidates (Prabhu et al., 2018; You et al., 2019).AttentionXML(You et al., 2019) uses an attention mechanism to focus on specific parts of the input text that are most relevant to the label’s semantic meaning, and thus can be considered a hybrid model. We refer readers to (Dasgupta et al., 2023) for a comprehensive review of XMC methods.

**中文**

在推理时，XMC 方法使用基于树的层次结构或基于集群的采样来快速缩小可能标签的搜索路径，而无需扫描每个候选标签（Prabhu et al., 2018；You et al., 2019）。AttentionXML（You et al., 2019）使用注意力机制来关注输入文本中与标签语义最相关的特定部分，因此可以被视为混合模型。我们建议读者参考（Dasgupta 等人，2023）对 XMC 方法进行全面回顾。

### 段落 79 · Page 11

**EN**

This hybrid architecture demonstrates that combining distributed representations with traditional local representations is favorable, with the combined approach significantly outperforming either neural network individually. More recent hybrid approaches have focused on reducing computational costs while maintaining effectiveness, with some models incorporating cached token-level representations to enable faster querydocument interactions when document representations are pre-computed (Wrzalik & Krechel, 2021).

**中文**

这种混合架构表明，将分布式表示与传统本地表示相结合是有利的，组合方法的性能显着优于单独的神经网络。最近的混合方法侧重于降低计算成本，同时保持有效性，一些模型结合了缓存的令牌级表示，以便在预先计算文档表示时实现更快的查询文档交互（Wrzalik＆Krechel，2021）。

### 段落 80 · Page 11

**EN**

The success of hybrid models has established that interaction-based and representation-based approaches can be effectively combined for further improvements in ranking performance (Liu et al., 2018). 11

**中文**

混合模型的成功表明，基于交互和基于表示的方法可以有效地结合起来，以进一步提高排名性能（Liu et al., 2018）。 11

### Page 12

### 段落 81 · Page 12

**EN**

Published in Transactions on Machine Learning Research (02/2026) 5.4 Orthogonal Directions In addition to the development of network architecture, pre-trained embeddings (Salakhutdinov & Hinton, 2009; Mikolov et al., 2013; Pennington et al., 2014; Le & Mikolov, 2014) provide semantic-based term representations to enable neural ranking models to focus on learning relevance matching patterns, improving training convergence and retrieval performance on both representation-based and interaction-based models (Levy et al., 2015).

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 5.4 正交方向 除了网络架构的发展之外，预训练嵌入（Salakhutdinov & Hinton, 2009; Mikolov et al., 2013; Pennington et al., 2014; Le & Mikolov, 2014）提供基于语义的术语表示，使神经排序模型能够聚焦学习相关性匹配模式，提高基于表示和基于交互的模型的训练收敛和检索性能（Levy 等，2015）。

### 段落 82 · Page 12

**EN**

Both GloVe (Pennington et al., 2014) and Word2Vec (Mikolov et al., 2013) learn dense vector representations for each vocabulary term from large-scale text corpora. By initializing the embedding layer with these pre-trained vectors, models start with a strong semantic foundation, which proved crucial for performance, especially on smaller training datasets (Guo et al., 2016b). Interaction-based models with cross-lingual word embeddings (Joulin et al., 2018) for cross-lingual reranking have also been explored (Yu & Allan, 2020). Table 2 shows a list of neural ranking models and backbone architectures.

**中文**

GloVe (Pennington et al., 2014) 和 Word2Vec (Mikolov et al., 2013) 都从大规模文本语料库中学习每个词汇术语的密集向量表示。通过使用这些预训练向量初始化嵌入层，模型从强大的语义基础开始，事实证明这对于性能至关重要，尤其是在较小的训练数据集上（Guo 等人，2016b）。还探索了用于跨语言重排的基于交互的跨语言词嵌入模型（Joulin 等人，2018）（Yu & Allan，2020）。表 2 显示了神经排序模型和主干架构的列表。

### 段落 83 · Page 12

**EN**

Researchers have explored different backbone neural network architectures in this era, including Convolutional Neural Network (CNN, LeCun et al., 1989), Long Short Term Memory (LSTM, Hochreiter & Schmidhuber, 1997) and kernel methods (Vert et al., 2004; Chang et al., 2010; Xiong et al., 2017). Notably, a line of research explores integrating kernel methods with the Transformer architecture (Vaswani et al., 2017).

**中文**

研究人员探索了这个时代不同的骨干神经网络架构，包括卷积神经网络（CNN，LeCun等，1989）、长短期记忆（LSTM，Hochreiter＆Schmidhuber，1997）和核方法（Vert等，2004；Chang等，2010；Xiong等，2017）。值得注意的是，一系列研究探索了将内核方法与 Transformer 架构集成（Vaswani 等人，2017）。

### 段落 84 · Page 12

**EN**

The main distinction between this line of research and the models discussed in Section 6 is that the transformer modules here are not pre-trained on large-scale corpora like Wikipedia and C4 (Devlin et al., 2019; Raffel et al., 2020). We consider this line of research as an intersection between neural ranking models (Section 5) and retrieval with pre-trained transformers (Section 6).TK(Hofstätter et al., 2020c) uses a shallow transformer neural network (up to 3 layers) to encode the queryQand documentDseparately.

**中文**

这一研究方向与第 6 节中讨论的模型之间的主要区别在于，这里的 Transformer 模块没有在维基百科和 C4 等大型语料库上进行预训练（Devlin 等人，2019 年；Raffel 等人，2020 年）。我们将这一研究方向视为神经排序模型（第 5 节）和使用预训练 Transformer 进行检索（第 6 节）之间的交叉点。TK（Hofstätter et al., 2020c）使用浅层 Transformer 神经网络（最多 3 层）对 queryQ 和 documentD 分别进行编码。

### 段落 85 · Page 12

**EN**

After encoding, the contextualized representations are input to an interaction module inspired by K-NRM, where RBF kernels are used to create soft-match features from the contextualized embeddings. This fusion of a transformer encoder with a kernel-based interaction mechanism allowed the model to achieve better performance-efficiency tradeoff compared toBERT-based reranker (Nogueira et al., 2019b).

**中文**

编码后，上下文表示被输入到受 K-NRM 启发的交互模块，其中 RBF 内核用于从上下文嵌入创建软匹配特征。与基于 BERT 的重排序器相比，Transformer 编码器与基于内核的交互机制的融合使模型能够实现更好的性能效率权衡（Nogueira 等人，2019b）。

### 段落 86 · Page 12

**EN**

The main bottleneck of applying transformer architectures to long document reranking isO(n 2)time complexity, wherendenotes the document length.TKL(Hofstätter et al., 2020b) further improves uponTKwith a local attention mechanism and leads to performance improvement on long document ranking. The neural ranking models described above, particularly later developments likeTKandTKL, demonstrated the potential of the transformer’s attention mechanism for modeling relevance.

**中文**

将 Transformer 架构应用于长文档重排序的主要瓶颈是 O(n 2) 时间复杂度，其中 n 表示文档长度。TKL（Hofstätter et al., 2020b）通过局部注意力机制进一步改进了 TK，并提高了长文档排序的性能。上面描述的神经排序模型，特别是后来的发展，如 TK 和 TKL，证明了 Transformer 注意力机制在建模相关性方面的潜力。

### 段落 87 · Page 12

**EN**

However, the true paradigm shift occurred when the IR community moved from using these architectures trained from scratch to leveraging massive, pre-trained transformer models like BERT (Devlin et al., 2019) and its variants (Liu et al., 2019; Sun et al., 2019; Lan et al., 2020; Beltagy et al., 2020). This marked a fundamental change in approach: instead of designing novel, task-specific network backbones (e.g., CNNs, LSTMs) on top of static word embeddings, research shifted to fine-tuning a single, powerful, and deeply contextualized architecture for IR tasks.

**中文**

然而，当 IR 社区从使用这些从头开始训练的架构转向利用大规模的预训练 Transformer 模型（如 BERT（Devlin 等人，2019）及其变体（Liu 等人，2019；Sun 等人，2019；Lan 等人，2020；Beltagy 等人，2020）时，真正的范式转变发生了。这标志着方法的根本性变化：研究不再是在静态词嵌入之上设计新颖的、特定于任务的网络主干（例如 CNN、LSTM），而是转向为 IR 任务微调单一、强大且深度上下文化的架构。

### 段落 88 · Page 12

**EN**

This new foundation did not eliminate the core architectural tradeoffs but rather recast them in a more powerful form, leading to the development of cross-encoder rerankers and bi-encoder retrievers, which we explore next. 6 IR with Pre-Trained Transformers BERT(Devlin et al., 2019) revolutionized research in both natural language processing (NLP) and information retrieval (IR).

**中文**

这个新的基础并没有消除核心架构的权衡，而是以更强大的形式重新构建它们，从而导致了跨编码器重新排序器和双编码器检索器的开发，我们接下来将对此进行探讨。 6 IR 与预训练 Transformers BERT（Devlin 等人，2019）彻底改变了自然语言处理（NLP）和信息检索（IR）领域的研究。

### 段落 89 · Page 12

**EN**

Its success is largely attributed to two key factors: (1) the Multi-Head Attention (MHA) architecture (Vaswani et al., 2017), which enables high-dimensional, contextualized token representations; and (2) large-scale pre-training, which equipsBERTwith the ability to capture rich semantics and world knowledge. The expressive power ofBERThas been extensively analyzed in prior work, e.g., (Rogers et al., 2020; Tenney et al., 2019; Clark et al., 2019).

**中文**

它的成功很大程度上归功于两个关键因素：（1）多头注意力（MHA）架构（Vaswani 等人，2017），它支持高维、上下文化的令牌表示； (2)大规模预训练，使BERT具备捕获丰富语义和世界知识的能力。 BER 的表达能力在之前的工作中已被广泛分析，例如（Rogers 等人，2020；Tenney 等人，2019；Clark 等人，2019）。

### 段落 90 · Page 12

**EN**

High-level architectural families.Before discussing specific IR modeling architectures, it is useful to understand the architectural families of transformers, as they have distinct implications for IR tasks: •Encoder-only models(e.g.,BERT(Devlin et al., 2019),RoBERTa(Liu et al., 2019)) use a bidirectional self-attention mechanism, allowing each token’s representation to be informed by the 12

**中文**

高级架构系列。在讨论特定的 IR 建模架构之前，了解 Transformer 的架构系列很有用，因为它们对 IR 任务有不同的影响： •仅编码器模型（例如，BERT（Devlin 等人，2019）、RoBERTa（Liu 等人，2019））使用双向自注意力机制，允许每个令牌的表示由 12 个令牌通知

### Page 13

### 段落 91 · Page 13

**EN**

Published in Transactions on Machine Learning Research (02/2026) (a) Transformer-based reranker (b) Learned dense retrieval. (ware token-level scalar weights) (c) Learned sparse retriever (d) Multi-vector representations Figure 3: Illustration on transformer-based retrieval and reranking models. Yellow boxes indicate pretrained Transformers (e.g., BERT). Query text, embeddings, and associated weights are color-coded in orange, whereas document representations are color-coded in blue. entire input sequence (both left and right context). This deep contextual understanding makes them naturally suited for representation-focused tasks.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) (a) 基于 Transformer 的重新排序器 (b) 学习密集检索。 （软件标记级标量权重） (c) 学习稀疏检索器 (d) 多向量表示 图 3：基于转换器的检索和重新排序模型的图示。黄色框表示预训练的 Transformer（例如 BERT）。查询文本、嵌入和相关权重以橙色进行颜色编码，而文档表示以蓝色进行颜色编码。整个输入序列（左右上下文）。这种深入的上下文理解使它们自然适合以表示为中心的任务。

### 段落 92 · Page 13

**EN**

In IR, they have been the workhorses for building powerful bi-encoder retrievers and cross-encoder rerankers. •Decoder-only models(e.g., proprietaryGPTseries (Radford et al., 2019; Brown et al., 2020; OpenAI et al., 2024), open-weightLlama(Touvron et al., 2023),Mistral(Jiang et al., 2023a)) use a unidirectional (causal) self-attention mechanism, where each token can only attend to previous tokens in the sequence. This architecture is optimized for next-token prediction and, by extension, text generation.

**中文**

在 IR 领域，它们一直是构建强大的双编码器检索器和跨编码器重排序器的主力。仅解码器模型（例如，专有GPTseries（Radford等人，2019；Brown等人，2020；OpenAI等人，2024），open-weightLlama（Touvron等人，2023），Mistral（Jiang等人，2023a））使用单向（因果）自注意力机制，其中每个令牌只能关注之前的序列中的标记。该架构针对下一个标记预测以及文本生成进行了优化。

### 段落 93 · Page 13

**EN**

Their application to representation tasks like retrieval is less direct and often requires architectural adaptations to create meaningful summary vectors from their unidirectional hidden states. •Encoder-decoder models(e.g.,T5(Raffel et al., 2020),BART(Lewis et al., 2020a)) combine both architectures. The encoder processes the input sequence bidirectionally to create a rich representation, which then conditions the decoder to generate an output sequence autoregressively. This “sequence-to-sequence” design makes them highly versatile.

**中文**

它们在检索等表示任务中的应用不太直接，并且通常需要进行架构调整才能从其单向隐藏状态创建有意义的摘要向量。 •编码器-解码器模型（例如，T5（Raffel et al., 2020）、BART（Lewis et al., 2020a））结合了两种架构。编码器双向处理输入序列以创建丰富的表示，然后条件解码器自回归生成输出序列。这种“序列到序列”的设计使它们具有高度的通用性。

### 段落 94 · Page 13

**EN**

In IR, they can be framed as rerankers (generating a “relevant” or “irrelevant” token), or as generative retrievers that directly generate document identifiers. This section discusses IR architectures based on pre-trained transformers, with a focus onBERT-type encoder models, which is to be distinct from encoder-decoder models and decoder-only models covered 13

**中文**

在 IR 中，它们可以被构建为重新排序器（生成“相关”或“不相关”标记），或直接生成文档标识符的生成检索器。本节讨论基于预训练 Transformer 的 IR 架构，重点是 BERT 型编码器模型，这与编码器-解码器模型和仅解码器模型不同 13

### Page 14

### 段落 95 · Page 14

**EN**

Published in Transactions on Machine Learning Research (02/2026) in Section 7. We structure our review around the fundamental architectural tradeoff between interaction depth and computational efficiency. These constraints necessitate two primary paradigms: 1.Cross-Encoder (Deep Interaction):A single model processes the concatenated query and document as one sequence, allowing every query token to interact deeply with every document token. This provides state-of-the-art ranking quality but is computationally expensive, making it suitable only for reranking.

**中文**

发表在机器学习研究交易 (02/2026) 的第 7 节中。我们围绕交互深度和计算效率之间的基本架构权衡构建我们的评论。这些约束需要两个主要范例： 1. 交叉编码器（深度交互）：单一模型将连接的查询和文档作为一个序列进行处理，允许每个查询标记与每个文档标记进行深度交互。这提供了最先进的排名质量，但计算成本较高，因此仅适合重排。

### 段落 96 · Page 14

**EN**

2.Bi-Encoder (Separable Pre-computation):Separate encoders process the query and document independently to create fixed-size vectors. Since document vectors can be pre-computed offline, this architecture enables extremely fast similarity search suitable for first-stage retrieval. We first discuss the crucial training strategies used to optimize these two architectures. We then detail the cross-encoder models that perform deep, full interaction, followed by the separable bi-encoder architectures thatprioritizeefficiency, exploringtheirdense, sparse, andmulti-vectorvariants.

**中文**

2.Bi-Encoder（可分离预计算）：单独的编码器独立处理查询和文档以创建固定大小的向量。由于文档向量可以离线预先计算，因此该架构可以实现非常快速的相似性搜索，适合第一阶段检索。我们首先讨论用于优化这两种架构的关键训练策略。然后，我们详细介绍执行深度、全面交互的交叉编码器模型，然后是优先考虑效率的可分离双编码器架构，探索其密集、稀疏和多向量变体。

### 段落 97 · Page 14

**EN**

Finally, wediscussadvanced hybrid models and orthogonal improvements such as continual training and interpretability. 6.1 Training Strategies for Transformer-Based IR Although we aim to disentangle model architectures from training strategies, the co-evolvement of these two areas is a defining pattern of this era. The architectural dichotomy (cross-encoder vs. bi-encoder) has an impactful influence the training methodology, extending the loss function categories discussed in Section 4 into the deep learning paradigm.

**中文**

最后，我们讨论了先进的混合模型和正交改进，例如持续训练和可解释性。 6.1 基于 Transformer 的 IR 的训练策略 虽然我们的目标是将模型架构与训练策略分开，但这两个领域的共同进化是这个时代的定义模式。架构二分法（跨编码器与双编码器）对训练方法产生了重大影响，将第 4 节中讨论的损失函数类别扩展到深度学习范式。

### 段落 98 · Page 14

**EN**

Contrastive and Listwise Objectives.The application of contrastive learning builds on the principle of the InfoNCE loss (Oord et al., 2018), which is derived from Noise-Contrastive Estimation (Gutmann & Hyvärinen, 2012). The general goal is to learn a model that distinguishes a “positive” sample from a set of “negative” samples. The InfoNCE framework is primarily used to optimizebi-encodersin the dense retrieval setting. In this context, the relevance scorefis a simple similarity function (e.g., dot product) between the query and document vectors,f(Q,D) = sim(v Q,vD).

**中文**

对比和列表目标。对比学习的应用建立在 InfoNCE 损失 (Oord et al., 2018) 的原理之上，该原理源自噪声对比估计 (Gutmann & Hyvärinen, 2012)。总体目标是学习一个能够区分“正”样本和一组“负”样本的模型。 InfoNCE 框架主要用于优化密集检索设置中的双编码器。在这种情况下，相关性得分是查询向量和文档向量之间的简单相似性函数（例如点积），f(Q,D) = sim(v Q,vD)。

### 段落 99 · Page 14

**EN**

For a queryQi, a positive documentD+ i , and a set of negative documentsD− i , the bi-encoder is trained to minimize the negative log probability of correctly classifying the positive document: LInfoNCE =−1 |S| ∑ (Qi,D+ i )∈S log expfθ(Qi,D + i ) expfθ(Qi,D + i ) + ∑ D− j∈D− i expfθ(Qi,D− j ) whereSis the training set andD − i is the set of sampled negative documents.

**中文**

对于查询Qi、正文档D+ i 和一组负文档D− i，训练双编码器以最小化正确分类正文档的负对数概率： LInfoNCE =−1 |S| Σ (Qi,D+ i )∈S log expfθ(Qi,D + i ) expfθ(Qi,D + i ) + Σ D− j∈D− i expfθ(Qi,D− j ) 其中S是训练集，D − i是采样的负文档集。

### 段落 100 · Page 14

**EN**

Forcross-encoders, which compute relevance over a concatenated list, the objective is also listwise but often simplified to a standard Negative Log-Likelihood (NLL) loss over the final softmax probabilities of the candidates, minimizing the distance between the predicted distribution and the ground truth relevance distribution for the entire list. Hard Negative Mining.A critical challenge in training bi-encoders is generating sufficiently difficult negative examples, as random sampling typically yields easy negatives that do not challenge the model effectively. This is where Hard Negative Mining (HNM) becomes essential.

**中文**

对于计算连接列表上的相关性的交叉编码器，目标也是列表式的，但通常简化为候选者最终 softmax 概率的标准负对数似然 (NLL) 损失，从而最小化整个列表的预测分布与地面真实相关性分布之间的距离。硬负例挖掘。训练双编码器的一个关键挑战是生成足够困难的负例，因为随机采样通常会产生简单的负例，而不会有效地挑战模型。这就是硬负挖掘（HNM）变得至关重要的地方。

### 段落 101 · Page 14

**EN**

HNM strategies ensure that the model is exposed to challenging cases where positive and negative document features are difficult to distinguish. Key strategies include: 1.In-Batch Negatives (IBN):Leveraging other queries’ positive documents within the same minibatch as negative examples for the current query. IBN provides a balance of efficiency and difficulty. 2.Lexical Negatives:Using documents highly ranked by a traditional sparse model (e.g., BM25) but not labeled as relevant. 14

**中文**

HNM 策略确保模型能够应对难以区分正面和负面文档特征的挑战性情况。关键策略包括： 1.批内负例（IBN）：利用同一小批量内其他查询的正例文档作为当前查询的负例。 IBN 提供了效率和难度的平衡。 2.词汇否定：使用传统稀疏模型（例如 BM25）排名较高但未标记为相关的文档。 14

### Page 15

### 段落 102 · Page 15

**EN**

Published in Transactions on Machine Learning Research (02/2026) 3.Iterative Hard Negative Mining:Employing an existing dense retriever to periodically mine difficult negatives from the collection (i.e., documents that the current model mistakenly ranks highly). Seminal methods likeANCE(Xiong et al., 2020) andADORE(Zhan et al., 2021) use this iterative approach to continually feed the model better training data. Knowledge Distillation.To further narrow the effectiveness gap between efficient bi-encoders and powerful cross-encoders, the community widely adopted Knowledge Distillation (KD) (Buciluă et al., 2006; Hinton et al., 2015).

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 3.迭代硬负例挖掘：使用现有的密集检索器定期从集合中挖掘困难负例（即当前模型错误排名较高的文档）。像 ANCE（Xiong 等人，2020）和 ADORE（Zhan 等人，2021）这样的开创性方法使用这种迭代方法不断地为模型提供更好的训练数据。知识蒸馏。为了进一步缩小高效双编码器和强大交叉编码器之间的有效性差距，社区广泛采用知识蒸馏（KD）（Buciluă et al., 2006; Hinton et al., 2015）。

### 段落 103 · Page 15

**EN**

KD is a technique for training a smaller, efficient “student” model by transferring knowledge from a larger, more capable “teacher” model (Hinton et al., 2015; Gou et al., 2021). In IR, KD is used to create fast rerankers or retrievers that approximate the performance of slower, larger models, which is critical for production systems (Hofstätter et al., 2020a; 2021a; Chen et al., 2021; Kim et al., 2023; Xu et al., 2025c; Zhang et al., 2025b; Vera et al., 2025). Letf t denote the teacher model (typically a cross-encoder) andfs denote the student model (typically a biencoder or a smaller cross-encoder).

**中文**

KD 是一种通过从更大、更有能力的“教师”模型转移知识来训练更小、更高效的“学生”模型的技术（Hinton 等人，2015 年；Gou 等人，2021 年）。在 IR 中，KD 用于创建快速重排器或检索器，以近似较慢、较大模型的性能，这对于生产系统至关重要（Hofstätter 等人，2020a；2021a；Chen 等人，2021；Kim 等人，2023；Xu 等人，2025c；Zhang 等人，2025b；Vera 等人，2025）。令f t 表示教师模型（通常是交叉编码器），fs 表示学生模型（通常是双编码器或更小的交叉编码器）。

### 段落 104 · Page 15

**EN**

For a given queryQand a list of candidate textsD={D1,D 2,...,Dk}, we first compute relevance scores (logits) from both models: zt = [ft(Q,D 1),ft(Q,D 2),...,ft(Q,Dk)] zs = [fs(Q,D 1),fs(Q,D 2),...,fs(Q,Dk)] The student modelf s is trained to mimic the teacher’s output distribution over the candidate texts by minimizing the Kullback-Leibler (KL) divergence between the two softened probability distributions: LKD =D KL ( softmax (zt T )⏐⏐⏐⏐softmax (zs T )) whereTis the temperature hyperparameter. A higher temperature creates a softer probability distribution, which can help in transferring more nuanced information from the teacher.

**中文**

对于给定的查询 Q 和候选文本列表 D={D1,D 2,...,Dk}，我们首先计算两个模型的相关性分数 (logits)： zt = [ft(Q,D 1),ft(Q,D 2),...,ft(Q,Dk)] zs = [fs(Q,D 1),fs(Q,D 2),...,fs(Q,Dk)] 学生模型 f s 被训练为通过最小化两个软化概率分布之间的 Kullback-Leibler (KL) 散度来模拟教师对候选文本的输出分布： LKD =D KL ( softmax (zt T )⏐⏐⏐⏐softmax (zs T )) 其中T是温度超参数。较高的温度会产生更柔和的概率分布，这有助于从老师那里传递更多细致的信息。

### 段落 105 · Page 15

**EN**

KD thus provides an essential bridge, allowing the efficiency of bi-encoders to approach the effectiveness ceiling set by cross-encoders. 6.2 Deep Interaction Models: The Cross-Encoder for Reranking The most effective application of transformers in IR involves full, deep interaction between query and document tokens. This architecture, known as a cross-encoder (Humeau et al., 2020), takes the concatenated sequenceof(Q,D)asasingleinput. Nogueiraetal.(2019b)firstemployedthisapproachintheirmonoBERT model for reranking candidate passages from a first-stage retriever.

**中文**

因此，KD 提供了一个重要的桥梁，使双编码器的效率能够接近交叉编码器设定的效率上限。 6.2 深度交互模型：用于重排序的交叉编码器 IR 中转换器最有效的应用涉及查询和文档标记之间的全面、深度交互。这种架构称为交叉编码器（Humeau et al., 2020），将 (Q,D) 的串联序列作为单个输入。 Nogueiraetal（2019b）首先在他们的 monoBERT 模型中采用了这种方法，对第一阶段检索器的候选段落进行重新排序。

### 段落 106 · Page 15

**EN**

The model outputs a relevance score svia a linear layer on top of the finalBERTrepresentation, typically from a linear layer using the[CLS] token’s representation (Figure 3a). Conceptually similar to pre-Transformer interaction-based neural ranking models, this schema has proven effective across various pre-trained encoders (Zhang et al., 2021b), as well as other transformer architectures (Section 7).

**中文**

该模型通过最终 BERT 表示之上的线性层输出相关性分数，通常来自使用 [CLS] 令牌表示的线性层（图 3a）。在概念上类似于 Transformer 之前基于交互的神经排序模型，该模式已被证明在各种预训练编码器（Zhang 等人，2021b）以及其他 Transformer 架构（第 7 节）中有效。

### 段落 107 · Page 15

**EN**

However, this cross-encoder schema faces two primary challenges: (1) the fixed context length of models likeBERT(e.g., 512 tokens) makes processing long documents difficult, and (2) relying on a single token’s fixed-dimensional representation (e.g., 768-dimensional representation forBERT) may limit the model’s expressive power.

**中文**

然而，这种跨编码器模式面临两个主要挑战：（1）BERT 等模型的固定上下文长度（例如 512 个 token）使得处理长文档变得困难，（2）依赖单个 token 的固定维度表示（例如 BERT 的 768 维表示）可能会限制模型的表达能力。

### 段落 108 · Page 15

**EN**

Handling Long Documents.Corresponding mitigations for these two challenges have been extensively investigated in literature.Chunk-and-aggregateapproaches represent a practical solution to handle long documents that exceed BERT’s input constraints by decomposing the ranking problem into passage-level scoringfollowedbyaggregation(Gao&Callan,2022). Thefundamentalstrategyinvolvessplittingdocuments into fixed-length passages or sentences, applyingBERT-based cross-encoders to score each query-passage pair independently, then combining these scores to produce a final document-level relevance score.

**中文**

处理长文档。针对这两个挑战的相应缓解措施已在文献中进行了广泛研究。分块聚合方法代表了一种实用的解决方案，通过将排名问题分解为段落级评分，然后进行聚合来处理超出 BERT 输入限制的长文档（Gao＆Callan，2022）。基本策略包括将文档分割成固定长度的段落或句子，应用基于 BERT 的交叉编码器对每个查询-段落对进行独立评分，然后将这些分数组合起来产生最终的文档级相关性分数。

### 段落 109 · Page 15

**EN**

Early work in this direction explored sentence-level aggregation, whereBERTscores computed at the sentence level were shown to be effective for document ranking (MacAvaney et al., 2020; Yilmaz et al., 2019). The BERT-MaxP (Dai & Callan, 2019a) approach became particularly influential, where documents are split into fixed-length passages and the maximum passage score serves as the document score. 15

**中文**

这个方向的早期工作探索了句子级聚合，其中在句子级计算的 BERTscore 被证明对文档排名有效（MacAvaney 等人，2020；Yilmaz 等人，2019）。 BERT-MaxP（Dai & Callan，2019a）方法变得特别有影响力，其中文档被分成固定长度的段落，最大段落分数作为文档分数。 15

### Page 16

### 段落 110 · Page 16

**EN**

Published in Transactions on Machine Learning Research (02/2026) Two primary aggregation strategies have emerged: (1) score-pooling and (2) representation aggregation. Score-pooling methods apply simple operations like maximum, sum, or first passage scores to combine passage-levelrelevancescores(Dai&Callan,2019a). Incontrast, representationaggregationmethodsaddress both the long-document problem and the single-vector expressiveness limitation. Instead of collapsing each passage’s signal into a single scalar score, these approaches gather the rich, low-dimensional[CLS]token representations from each passage.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 出现了两种主要聚合策略：(1) 分数池和 (2) 表示聚合。分数池方法应用简单的操作（例如最大、总和或第一个段落分数）来组合段落级别的相关性分数（Dai＆Callan，2019a）。相反，表示聚合方法可以解决长文档问题和单向量表达能力限制。这些方法不是将每个段落的信号分解为单个标量分数，而是从每个段落中收集丰富的低维[CLS]标记表示。

### 段落 111 · Page 16

**EN**

This collection of vectors forms a more comprehensive and expressive document-level feature set, which is then processed by additional neural networks (MacAvaney et al., 2020). Notable systems likePARADE(Li et al., 2023a) employ CNNs and transformers for aggregation, while CEDR(MacAvaney et al., 2019b) pioneered joint approaches that combine BERT outputs with existing neural IR models through averaging.

**中文**

该向量集合形成了更全面、更具表现力的文档级特征集，然后由其他神经网络进行处理（MacAvaney 等人，2020）。 PARADE（Li et al., 2023a）等著名系统采用 CNN 和 Transformer 进行聚合，而 CEDR（MacAvaney et al., 2019b）则开创了通过平均将 BERT 输出与现有神经 IR 模型相结合的联合方法。

### 段落 112 · Page 16

**EN**

While chunk-and-aggregate approaches successfully handle long documents, they fundamentally limit querydocument interactions to the passage level, creating information bottlenecks where passage scores or lowdimensional representations constrain the model’s ability to capture document-wide relevance patterns. Hofstätter et al. (2021b) argue that this tradeoff between scalability and interaction richness remains a defining characteristic of this approach.

**中文**

虽然块聚合方法成功地处理长文档，但它们从根本上将查询文档交互限制在段落级别，从而造成信息瓶颈，其中段落分数或低维表示限制了模型捕获文档范围相关模式的能力。霍夫斯塔特等人。 (2021b) 认为，可扩展性和交互丰富性之间的这种权衡仍然是这种方法的一个决定性特征。

### 段落 113 · Page 16

**EN**

6.3 Efficient Pre-Computation Models: The Bi-Encoder Architecture While cross-encoders offer state-of-the-art effectiveness, their computational cost—requiring a full transformer pass for every(Q,D)pair—makes them infeasible for retrieval over large collections. This limitation motivated the development of bi-encoder architectures, which are conceptually similar to representationbased neural ranking models (Section 5).2 A bi-encoder uses a backbone network (typically a transformer) to encode the queryQand documentD separately.

**中文**

6.3 高效的预计算模型：双编码器架构 虽然交叉编码器提供了最先进的有效性，但它们的计算成本（需要对每个（Q，D）对进行完整的Transformer传递）使得它们无法在大型集合上进行检索。这种限制促进了双编码器架构的开发，其在概念上类似于基于表示的神经排序模型（第 5 节）。2 双编码器使用骨干网络（通常是Transformer）来分别编码 queryQ 和 documentD。

### 段落 114 · Page 16

**EN**

The resulting dense vector representations are then used to compute a relevance score with a simple similarity function like dot product or cosine similarity (Xiong et al., 2020; Karpukhin et al., 2020; Gao et al., 2021b). The key advantage of this separation is efficiency: the entire document collection can be encoded into a vector index offline. At query time, retrieval becomes a fast approximate nearest neighbor (ANN) search problem (Johnson et al., 2019; Malkov & Yashunin, 2018) or search with an inverted index data structure (Zobel et al., 1998), avoiding costly neural network inference.

**中文**

然后使用所得的密集向量表示，通过简单的相似性函数（如点积或余弦相似性）计算相关性得分（Xiong 等人，2020；Karpukhin 等人，2020；Gao 等人，2021b）。这种分离的主要优点是效率：整个文档集合可以离线编码为向量索引。在查询时，检索变成快速近似最近邻（ANN）搜索问题（Johnson et al., 2019；Malkov & Yashunin, 2018）或使用倒排索引数据结构进行搜索（Zobel et al., 1998），从而避免昂贵的神经网络推理。

### 段落 115 · Page 16

**EN**

A notable insight from Lin (2021) is that the bi-encoder framework provides a unifying lens for understanding diverse retrieval approaches. Dense retrieval models, learned sparse retrieval models, and traditional bagof-words approaches such as BM25 can all be interpreted as parametric variations of this architecture. They differ primarily along two axes: (1) the representational basis (dense semantic embeddings versus sparse lexical vectors), and (2) whether those representations are learned from data or manually engineered.

**中文**

Lin（2021）的一个值得注意的见解是，双编码器框架为理解不同的检索方法提供了一个统一的视角。密集检索模型、学习稀疏检索模型和传统的词袋方法（例如 BM25）都可以解释为该架构的参数变体。它们主要在两个方面有所不同：（1）表示基础（密集语义嵌入与稀疏词汇向量），以及（2）这些表示是从数据中学习的还是手动设计的。

### 段落 116 · Page 16

**EN**

Existing methods based on this bi-encoder architecture vary primarily in their representation format (dense versus sparse), pooling strategies, and training methodologies. 6.3.1 Learned Dense Retrieval Dense retrieval models typically adopt a standardized dual-encoder architecture built on pre-trained transformer models, most commonly BERT in this context. The standard formulation uses separate BERT encoders for queries and documents, with a layer-normalized linear projection applied to the token representation: Encoder(·) =Linear ( BERT(·) ) . The encoder weights can be separate or shared between query and document sides.

**中文**

基于这种双编码器架构的现有方法主要在表示格式（密集与稀疏）、池化策略和训练方法方面有所不同。 6.3.1 学习密集检索密集检索模型通常采用基于预训练 Transformer 模型构建的标准化双编码器架构，在这种情况下最常见的是 BERT。标准公式对查询和文档使用单独的 BERT 编码器，并对标记表示应用层归一化线性投影： Encoder(·) =Linear ( BERT(·) )。编码器权重可以在查询端和文档端之间分开或共享。

### 段落 117 · Page 16

**EN**

The core architectural principle involves encoding queries and documents into low-dimensional dense vectors, typically 768 dimensions matchingBERT’s hidden size. Rather than using all hidden representations, most models compress the sequence information using a reduction function, usually the token representation or mean pooling of the final transformer layer outputs. This creates a single dense vector representation per text sequence that captures semantic information beyond simple lexical matching. 2The term “bi-encoder” is also known as a two-tower architecture or an embedding model.

**中文**

核心架构原理涉及将查询和文档编码为低维密集向量，通常为 768 维，与 BERT 的隐藏大小相匹配。大多数模型不是使用所有隐藏表示，而是使用归约函数（通常是最终Transformer层输出的令牌表示或均值池）来压缩序列信息。这会为每个文本序列创建一个单一的密集向量表示，捕获超出简单词汇匹配的语义信息。 2术语“双编码器”也称为双塔架构或嵌入模型。

### 段落 118 · Page 16

**EN**

We use “bi-encoder” to contrast with “cross-encoder”, which takes concatenated input. 16

**中文**

我们使用“双编码器”与“交叉编码器”进行对比，后者采用串联输入。 16

### Page 17

### 段落 119 · Page 17

**EN**

Published in Transactions on Machine Learning Research (02/2026) Relevance scoring in dense retrieval is performed through simple similarity functions, most commonly dot product or cosine similarity between query and document vectors. This design enables efficient ANN search over pre-computed document representations (Johnson et al., 2019), making dense retrieval practical for large-scale collections while maintaining the semantic understanding capabilities of transformer models.

**中文**

发表于机器学习研究交易 (02/2026) 密集检索中的相关性评分是通过简单的相似性函数（最常见的是查询向量和文档向量之间的点积或余弦相似性）来执行。这种设计可以在预先计算的文档表示上实现高效的 ANN 搜索（Johnson 等人，2019），使密集检索适用于大规模集合，同时保持 Transformer 模型的语义理解能力。

### 段落 120 · Page 17

**EN**

The success of this architecture stems from its ability to learn semantic representations that address the vocabulary mismatch problem inherent in traditional sparse retrieval methods (Lee et al., 2019; Karpukhin et al., 2020; Xiong et al., 2020; Reimers & Gurevych, 2019). Dense retrieval models have demonstrated notable effectiveness improvements over BM25 baselines across various tasks including open-domain question answering and web search.

**中文**

该架构的成功源于其学习语义表示的能力，从而解决传统稀疏检索方法中固有的词汇不匹配问题（Lee et al., 2019; Karpukhin et al., 2020; Xiong et al., 2020; Reimers & Gurevych, 2019）。密集检索模型在各种任务（包括开放域问答和网络搜索）中表现出比 BM25 基线显着的有效性改进。

### 段落 121 · Page 17

**EN**

6.3.2 Learned Sparse Retrieval Learned sparse retrieval (LSR, Figure 3c) employs the same bi-encoder architecture as dense retrieval but produces fundamentally different representations.3 While sharing the transformer backbone, sparse retrieval models encode queries and documents into high-dimensional sparse vectors whose dimensionality typically matches the vocabulary size of the underlying pre-trained model, often containing tens of thousands of dimensions.

**中文**

6.3.2 学习稀疏检索 学习稀疏检索（LSR，图 3c）采用与密集检索相同的双编码器架构，但产生根本不同的表示。 3 在共享Transformer主干的同时，稀疏检索模型将查询和文档编码为高维稀疏向量，其维度通常与底层预训练模型的词汇大小相匹配，通常包含数万个维度。

### 段落 122 · Page 17

**EN**

Each dimension corresponds to a specific vocabulary term, creating an interpretable representation where non-zero weights indicate term importance (Formal et al., 2021b;a; Nguyen et al., 2023). Three key architectural constraints distinguish sparse encoders from their dense counterparts. First, sparsity is enforced through explicit regularization techniques, ensuring most term weights remain zero to maintain efficiency (Formal et al., 2021b; Xu et al., 2025b; 2026). Second, all weights must be non-negative to maintain compatibility with traditional inverted index software designed for lexical search systems like Lucene.

**中文**

每个维度对应于一个特定的词汇术语，创建一个可解释的表示，其中非零权重表示术语重要性（Formal 等人，2021b；a；Nguyen 等人，2023）。三个关键的架构约束将稀疏编码器与密集编码器区分开来。首先，通过显式正则化技术强制执行稀疏性，确保大多数项权重保持为零以保持效率（Formal 等人，2021b；Xu 等人，2025b；2026）。其次，所有权重必须是非负的，以保持与为 Lucene 等词汇搜索系统设计的传统倒排索引软件的兼容性。

### 段落 123 · Page 17

**EN**

Third, the high-dimensional vocabulary-aligned vectors enable integration with existing inverted index infrastructure and optimization algorithms (Turtle & Flood, 1995; Broder et al., 2003; Bruch et al., 2024). Notably, inference-free learned sparse retrieval methods such asSPLADE-Doc(Formal et al., 2021a; Shen et al., 2025) eliminates requirement of specialized accelerators such as GPUs, making them highly efficient for inference on multi-core CPU machines.

**中文**

第三，高维词汇对齐向量能够与现有倒排索引基础设施和优化算法集成（Turtle & Flood，1995；Broder 等，2003；Bruch 等，2024）。值得注意的是，诸如 SPLADE-Doc（Formal 等人，2021a；Shen 等人，2025）等免推理学习稀疏检索方法消除了对 GPU 等专用加速器的需求，使其在多核 CPU 机器上进行高效推理。

### 段落 124 · Page 17

**EN**

At a conceptual level, learned sparse retrieval can be viewed as a sophisticated evolution of traditional term weighting schemes, learning context-aware token importance scores from data rather than relying on heuristic formulas (Zamani et al., 2018; Dai & Callan, 2019b; Mallia et al., 2021; Yu et al., 2024a; Xu et al., 2025b; 2026). This approach inherits desirable properties from bag-of-words models such as exact term matching while leveraging the semantic understanding capabilities of pretrained transformers.

**中文**

在概念层面上，学习稀疏检索可以被视为传统术语权重方案的复杂演变，从数据中学习上下文感知的标记重要性分数，而不是依赖启发式公式（Zamani et al., 2018; Dai & Callan, 2019b; Mallia et al., 2021; Yu et al., 2024a; Xu et al., 2025b; 2026）。这种方法继承了词袋模型的理想属性，例如精确的术语匹配，同时利用预训练Transformer的语义理解能力。

### 段落 125 · Page 17

**EN**

Notable implementations includeSPLADE(Formal et al., 2021a),DeepImpact(Mallia et al., 2021), and uniCOIL(Lin & Ma, 2021), which demonstrate that transformer-based sparse representations can achieve effectiveness comparable to dense retrieval while maintaining the efficiency benefits of inverted indexes. 6.4 Bridging the Gap: Advanced Interaction and Hybrid Models The standard bi-encoder’s lack of term-level interaction is a performance bottleneck compared to crossencoders. Several lines of research aim to bridge this gap by introducing more granular representations or by combining different retrieval paradigms.

**中文**

值得注意的实现包括 SPLADE（Formal et al., 2021a）、DeepImpact（Mallia et al., 2021）和 uniCOIL（Lin & Ma, 2021），它们证明基于 Transformer 的稀疏表示可以实现与密集检索相当的有效性，同时保持倒排索引的效率优势。 6.4 弥合差距：高级交互和混合模型 与交叉编码器相比，标准双编码器缺乏术语级交互是一个性能瓶颈。一些研究旨在通过引入更细粒度的表示或结合不同的检索范式来弥补这一差距。

### 段落 126 · Page 17

**EN**

6.4.1 Multi-Vector Representations To re-introduce query-document interaction without the full cost of a cross-encoder, multi-vector models represent queries and documents using multiple vectors.Poly-Encoder(Humeau et al., 2020) computes a fixed number of vectors per query and aggregates them with softmax attention over document vectors.ME- BERT(Luan et al., 2021) represents documents withmvectors and uses the maximum similarity between any query and document vector to estimate relevance.

**中文**

6.4.1 多向量表示 为了在不产生交叉编码器全部成本的情况下重新引入查询-文档交互，多向量模型使用多个向量表示查询和文档。Poly-Encoder（Humeau 等人，2020）计算每个查询的固定数量的向量，并通过对文档向量的 Softmax 关注来聚合它们。MEBERT（Luan 等人，2021）表示具有 m 向量的文档，并使用任何向量之间的最大相似度查询和文档向量来估计相关性。

### 段落 127 · Page 17

**EN**

3We focus on learned sparse retrieval within the bi-encoder formulation, thereby excluding approaches based on learned document expansion (e.g., Nogueira et al. (2019a); Zbib et al. (2019)) and document term reweighting (e.g.,DeepCT(Dai & Callan, 2019b)). For a unified treatment of learned sparse retrieval that encompasses these lines of work, see Mallia et al. (2021); Basnet et al. (2024). 17

**中文**

3我们专注于双编码器公式中的学习稀疏检索，从而排除基于学习文档扩展的方法（例如，Nogueira 等人（2019a）；Zbib 等人（2019））和文档术语重新加权（例如，DeepCT（Dai & Callan，2019b））。对于包含这些工作的学习稀疏检索的统一处理，请参阅 Mallia 等人。 （2021）；巴斯内特等人。 （2024）。 17 号

### Page 18

### 段落 128 · Page 18

**EN**

Published in Transactions on Machine Learning Research (02/2026) In line with this idea,ColBERT(Khattab & Zaharia, 2020; Santhanam et al., 2022; Hofstätter et al., 2022) represents each token in the query and document as a contextualized vector. It then performs a “late interaction” step where each query vector is compared against all document vectors via a MaxSim operator, and the final score is the sum of these maximum similarities. This late interaction scheme (Figure 3d) allows ColBERTfor end-to-end training to achieve strong performance while still achieving efficient retrieval through a dedicated index structure.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 根据这一想法，ColBERT（Khattab & Zaharia, 2020; Santhanam et al., 2022; Hofstätter et al., 2022）将查询和文档中的每个标记表示为上下文化向量。然后，它执行“后期交互”步骤，其中通过 MaxSim 运算符将每个查询向量与所有文档向量进行比较，最终得分是这些最大相似度的总和。这种后期交互方案（图 3d）使 ColBERTfor 端到端训练能够实现强大的性能，同时仍然通过专用索引结构实现高效检索。

### 段落 129 · Page 18

**EN**

On the other hand, it also leads to drastically increased index size, which has been the focus in later studies (Santhanam et al., 2022; Hofstätter et al., 2022,inter alia). We should also note that multi-vector retrieval can be viewed as a special case of dense retrieval where the learned feature representation is a matrix of sizen×h, withnvectors of hidden dimensionh. This matrix can be conceptually flattened into a single dense vector, showing its connection to the vanilla singlevector retrieval.

**中文**

另一方面，它也导致索引大小的急剧增加，这一直是后来研究的重点（Santhanam et al., 2022; Hofstätter et al., 2022等）。我们还应该注意到，多向量检索可以被视为密集检索的特殊情况，其中学习的特征表示是大小为n×h的矩阵，其中隐藏维度为h的n个向量。该矩阵在概念上可以扁平化为单个密集向量，显示其与普通单向量检索的联系。

### 段落 130 · Page 18

**EN**

The key difference lies not in the representation itself but in the richer relevance estimation strategy: instead of applying a simple linear relevance like dot product, models likeColBERTaggregate fine-grained token-level interactions to compute a relevance score. 6.4.2 Hybrid Retrieval Another direction combines the strengths of different retrieval systems. A simple yet effective approach is ranklist fusion (e.g., Reciprocal Rank Fusion, Cormack et al., 2009), which merges ranked lists from sparse (e.g., BM25) and dense retrievers post-retrieval without architectural changes.

**中文**

关键区别不在于表示本身，而在于更丰富的相关性估计策略：ColBERT 等模型不是应用点积等简单的线性相关性，而是通过细粒度标记级交互来计算相关性得分。 6.4.2 混合检索 另一个方向是结合不同检索系统的优点。一种简单而有效的方法是排名列表融合（例如，Reciprocal Rank Fusion，Cormack 等人，2009），它在检索后合并来自稀疏检索器（例如 BM25）和密集检索器的排名列表，而无需更改架构。

### 段落 131 · Page 18

**EN**

More integrated models combine signals at a deeper level.COIL(Gao et al., 2021a) enhances traditional bag-of-words retrieval with semantic embeddings from aBERTencoder.uniCOIL(Lin & Ma, 2021) simplifies this by reducing the semantic embedding to a single dimension, effectively learning a term weight akin to LSR models like SPLADE(Formal et al., 2021a;b). A few works fall into the intersection of learned sparse retrieval and multivector representations.

**中文**

更集成的模型在更深层次上组合信号。COIL（Gao et al., 2021a）通过 aBERTencoder 的语义嵌入增强了传统的词袋检索。uniCOIL（Lin & Ma, 2021）通过将语义嵌入减少到单一维度来简化这一过程，有效地学习类似于 SPLADE 等 LSR 模型的术语权重（Formal et al., 2021a;b）。一些工作属于学习稀疏检索和多向量表示的交叉点。

### 段落 132 · Page 18

**EN**

For example,SLIM(Li et al., 2023c) first maps each contextualized token vector to a sparse, high-dimensional lexical space before performing late interaction between these sparse token embeddings.SPLATE(Formal et al., 2024) takes an alternative approach to first encode contextualized token vectors, then map these token vectors to a sparse vocabulary space with a partially learnedSPLADE module. Both models achieve performance improvement compared to learned sparse retrieval baselines such asSPLADE.

**中文**

例如，SLIM（Li et al., 2023c）首先将每个上下文化标记向量映射到稀疏的高维词汇空间，然后再在这些稀疏标记嵌入之间执行后期交互。SPLATE（Formal et al., 2024）采用另一种方法，首先对上下文化标记向量进行编码，然后使用部分学习的 SPLADE 模块将这些标记向量映射到稀疏词汇空间。与学习的稀疏检索基线（例如 SPLADE）相比，这两种模型都实现了性能改进。

### 段落 133 · Page 18

**EN**

6.5 Orthogonal Improvements and Analysis Beyond architectural innovations, performance can be enhanced through improvements to the underlying modelsandadeeperanalysisoftheirbehavior. Weshowalistofmodelsandtheircorrespondingarchitectures in Table 3, a majority of which useBERT(Devlin et al., 2019) as the backbone, with exceptions using DistilBERT(Sanh et al., 2019),RoBERTa(Liu et al., 2019), andT5(Raffel et al., 2020; Sanh et al., 2022; Mo et al., 2023; Chung et al., 2024).

**中文**

6.5 正交改进和分析 除了架构创新之外，还可以通过改进底层模型和对其行为进行深入分析来增强性能。我们在表 3 中展示了模型列表及其相应的架构，其中大多数使用 BERT（Devlin et al., 2019）作为主干，除了使用 DistilBERT（Sanh et al., 2019）、RoBERTa（Liu et al., 2019）和 T5（Raffel et al., 2020; Sanh et al., 2022; Mo等人，2023；Chung 等人，2024）。

### 段落 134 · Page 18

**EN**

Continual Training and Adaptation.Instead of modifying the retrieval architecture, this line of work enhances the backbone language model itself through domain adaptation or continued pre-training, a proven strategy in NLP (Howard & Ruder, 2018; Gururangan et al., 2020). For instance, Lee et al.

**中文**

持续训练和适应。这一系列工作不是修改检索架构，而是通过领域适应或持续预训练来增强主干语言模型本身，这是 NLP 中经过验证的策略（Howard & Ruder，2018；Gururangan 等人，2020）。例如，李等人。

### 段落 135 · Page 18

**EN**

(2019) pretrainBERTwith an Inverse-Cloze Task (Taylor, 1953) for better text representations.Condenser(Gao & Callan, 2021) proposes a dedicated pre-training architecture to “condense” text representations into the [CLS]token.COCO-DR(Yu et al., 2022c) extendsCondenserby using a technique named Distributionally Robust Optimization to mitigate distribution shifts in dense retrieval. A line of works have also explored other pre-training objectives such as masked auto-encoders (Xiao et al., 2022; Wu et al., 2023b) and bag-of-words prediction (Ma et al., 2024a).

**中文**

(2019) 使用逆完形填空任务 (Taylor, 1953) 来预训练 BERT，以获得更好的文本表示。Condenser(Gao & Callan, 2021) 提出了一种专用的预训练架构，将文本表示“压缩”为 [CLS]token。COCO-DR(Yu et al., 2022c) 使用名为分布式鲁棒优化的技术来扩展Condenser，以减轻分布情况密集检索的转变。一系列工作还探索了其他预训练目标，例如屏蔽自动编码器（Xiao 等人，2022；Wu 等人，2023b）和词袋预测（Ma 等人，2024a）。

### 段落 136 · Page 18

**EN**

Recent works (Wang et al., 2023a; Nussbaum et al., 2025; Yu et al., 2024b,inter alia) have employed a “middle-stage” training on large-scale unlabeled text pairs, between pretrained encoder models and supervised fine-tuning on labeled text pairs, and have demonstrated the corresponding performance improvement compared to the traditional two-stage pipeline. We refer readers to the original papers for details. Interpretability and Explainability.A few works have attempted to interpret what transformer-based models learn, i.e., mechanistic interpretability (Elhage et al., 2021; Saphra & Wiegreffe, 2024). MacAvaney 18

**中文**

最近的工作（Wang et al., 2023a; Nussbaum et al., 2025; Yu et al., 2024b等）在大规模未标记文本对上采用了预训练编码器模型和标记文本对监督微调之间的“中间阶段”训练，并证明了与传统两阶段管道相比相应的性能改进。我们建议读者参阅原始论文以了解详细信息。可解释性和可解释性。一些作品试图解释基于 Transformer 的模型学习的内容，即机械可解释性（Elhage 等人，2021；Saphra 和 Wiegreffe，2024）。麦克卡瓦尼 18

### Page 19

### 段落 137 · Page 19

**EN**

Published in Transactions on Machine Learning Research (02/2026) Table 3: Summary of IR model architecture for passage retrieval and passage ranking based on pre-trained transformers. Dense Retrieval and LSR denote learned dense retrieval and learned sparse retrieval, respectively.DeepCT(Dai & Callan, 2019b) is trained without labeled training set. Contrastive Learning and in-batch negatives means listwise loss function is used.SentenceBERT(Reimers & Gurevych, 2019) is originally designed for the symmetrical sentence similarity tasks, but is quickly expanded to asymmetrical retrieval tasks.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 表 3：基于预训练 Transformer 的段落检索和段落排名的 IR 模型架构摘要。密集检索和LSR分别表示学习密集检索和学习稀疏检索。DeepCT（Dai & Callan，2019b）在没有标记训练集的情况下进行训练。对比学习和批量否定意味着使用列表损失函数。SentenceBERT(Reimers & Gurevych, 2019)最初是为对称句子相似性任务设计的，但很快扩展到不对称检索任务。

### 段落 138 · Page 19

**EN**

Name Model Architecture Backbone LM Training strategy monoBERT(Nogueira et al., 2019b) Reranking Cross-encoderBERT Classification CEDR(MacAvaney et al., 2019b) Reranking Cross-encoderBERT Contrastive Learning BERT-MaxP(Dai & Callan, 2019a) Reranking Cross-encoderBERT Pairwise Loss Gao et al.

**中文**

名称 模型架构 Backbone LM 训练策略 monoBERT(Nogueira et al., 2019b) 重新排序交叉编码器BERT 分类 CEDR(MacAvaney et al., 2019b) 重新排序交叉编码器BERT 对比学习 BERT-MaxP(Dai & Callan, 2019a) 重新排序交叉编码器BERT Pairwise Loss 高等人。

### 段落 139 · Page 19

**EN**

(2020) Reranking Cross-encoderBERT Distillation TART-full(Asai et al., 2023) Reranking Cross-encoderFlan-T5-EncInstruction Tuning ODQA(Lee et al., 2019) Dense Retrieval Bi-encoder BERT Unsupervised SentenceBERT(Reimers & Gurevych, 2019)Dense Retrieval Bi-encoder BERT Triplet DPR(Karpukhin et al., 2020) Dense Retrieval Bi-encoder BERT Contrastive Learning ANCE(Xiong et al., 2020) Dense Retrieval Bi-encoder RoBERTa Contrastive Learning RepBERT(Zhan et al., 2020) Dense Retrieval Bi-encoder BERT In-batch negatives Margin-MSE(Hofstätter et al., 2020a)Dense Retrieval Bi-encoder DistilBERT Distillation TAS-B(Hofstätter et al., 2021a) Dense Retrieval

**中文**

(2020) 重新排序交叉编码器BERT Distillation TART-full(Asai et al., 2023) 重新排序交叉编码器Flan-T5-EncInstruction Tuning ODQA(Lee et al., 2019) 密集检索双编码器 BERT 无监督句子BERT(Reimers & Gurevych, 2019) 密集检索双编码器 BERT Triplet DPR(Karpukhin et al., 2020) 密集检索双编码器 BERT 对比学习 ANCE(Xiong et al., 2020) 密集检索双编码器 RoBERTa 对比学习 RepBERT(Zhan et al., 2020) 密集检索双编码器 BERT 批量负数Margin-MSE（Hofstätter et al., 2020a）密集检索双编码器 DistilBERT Distillation TAS-B（Hofstätter et al., 2021a）密集检索

### 段落 140 · Page 19

**EN**

Bi-encoder BERT Distillation RocketQA(Qu et al., 2020) Dense Retrieval Bi-encoder ERNIE Contrastive Learning RocketQA-v2(Ren et al., 2021) Dense Retrieval Bi-encoder ERNIE Distillation GTR(Ni et al., 2022b) Dense Retrieval Bi-encoder EncT5 Contrastive Learning TART-dual(Asai et al., 2023) Dense Retrieval Bi-encoder Contriever Instruction Tuning E5(Wang et al., 2022a) Dense Retrieval Bi-encoder BERT Contrastive Learning GTE(Li et al., 2023d) Dense Retrieval Bi-encoder BERT Contrastive Learning Poly-encoder(Humeau et al., 2020) Multi-vector Misc BERT In-batch Negatives ME-BERT(Luan et al., 2021) Multi-vector Bi-encoder BERT Contrastive Learnin

**中文**

双编码器 BERT Distillation RocketQA(Qu et al., 2020) 密集检索双编码器 ERNIE 对比学习 RocketQA-v2(Ren et al., 2021) 密集检索双编码器 ERNIE Distillation GTR(Ni et al., 2022b) 密集检索双编码器 EncT5 对比学习 TART-dual(Asai et al., 2023) 密集检索双编码器 Contriever 指令调优 E5(Wang et al., 2022a) 密集检索双编码器 BERT 对比学习 GTE(Li et al., 2023d) 密集检索双编码器 BERT 对比学习多编码器(Humeau et al., 2020) 多向量 Misc BERT In-batch Negatives ME-BERT(Luan et al., 2021) 多向量双编码器 BERT 对比学习

### 段落 141 · Page 19

**EN**

g ColBERT(Khattab & Zaharia, 2020)Multi-vector Bi-encoder BERT Pairwise Loss COIL(Gao et al., 2021a) Multi-vector Bi-encoder BERT Contrastive Learning ColBERT-v2(Santhanam et al., 2022)Multi-vector Bi-encoder BERT Distillation ColBERTer(Hofstätter et al., 2022) Multi-vector Bi-encoder BERT Distillation DeepCT(Dai & Callan, 2019b) LSR Bi-encoder BERT Unsupervised SparTerm(Bai et al., 2020) LSR Bi-encoder BERT Contrastive Learning SPLADE(Formal et al., 2021b) LSR Bi-encoder BERT Contrastive Learning SPLADE-v2(Formal et al., 2021a) LSR Bi-encoder BERT Distillation DeepImpact(Mallia et al., 2021) LSR Bi-encoder BERT Contrastive Learning uniCOILLi

**中文**

g ColBERT(Khattab & Zaharia, 2020)多向量双编码器 BERT Pairwise Loss COIL(Gao et al., 2021a) 多向量双编码器 BERT 对比学习 ColBERT-v2(Santhanam et al., 2022)多向量双编码器 BERT Distillation ColBERTer(Hofstätter et al., 2022)多向量双编码器 BERT 蒸馏 DeepCT(Dai & Callan, 2019b) LSR 双编码器 BERT 无监督 SparTerm(Bai et al., 2020) LSR 双编码器 BERT 对比学习 SPLADE(Formal 等人, 2021b) LSR 双编码器 BERT 对比学习 SPLADE-v2(Formal 等人, 2021a) LSR 双编码器 BERT 蒸馏 DeepImpact（Mallia 等人，2021）LSR 双编码器 BERT 对比学习 uniCOILLi

### 段落 142 · Page 19

**EN**

n & Ma (2021) LSR Bi-encoder BERT Contrastive Learning SparseEmbed(Kong et al., 2023) LSR Bi-encoder BERT Contrastive Learning SLIM(Li et al., 2023c) LSR + Multi-vectorBi-encoder BERT Contrastive Learning SLIM++(Li et al., 2023c) LSR + Multi-vectorBi-encoder BERT Distillation SPLATE(Formal et al., 2024) LSR + Multi-vectorBi-encoder BERT Distillation et al.

**中文**

n & Ma (2021) LSR 双编码器 BERT 对比学习 SparseEmbed(Kong et al., 2023) LSR 双编码器 BERT 对比学习 SLIM(Li et al., 2023c) LSR + 多向量双编码器 BERT 对比学习 SLIM++(Li et al., 2023c) LSR + 多向量双编码器 BERT Distillation SPLATE（Formal et al., 2024）LSR + 多向量双编码器 BERT Distillation et al.

### 段落 143 · Page 19

**EN**

(2022) showed that neural models rely less on exact match signals and instead encode rich semantic information. Ram et al. (2023a) connected dense and sparse retrieval by projecting a dense retriever’s intermediate representations into the vocabulary space. Separately, other work focuses on designing systems that provide model-agnostic explanations (Rahimi et al., 2021; Yu et al., 2022b; Xu et al., 2024c) to satisfy desiderata like faithfulness (Jacovi & Goldberg, 2020; Xu et al., 2023). As IR systems become integral to other applied ML domains, we believe it is important to study and design interpretable, truthful, and trustworthy IR models.

**中文**

（2022）表明神经模型较少依赖于精确匹配信号，而是编码丰富的语义信息。拉姆等人。 （2023a）通过将密集检索器的中间表示投影到词汇空间中来连接密集检索和稀疏检索。另外，其他工作侧重于设计提供与模型无关的解释的系统（Rahimi 等人，2021；Yu 等人，2022b；Xu 等人，2024c）以满足诸如忠诚度之类的需求（Jacovi & Goldberg，2020；Xu 等人，2023）。随着 IR 系统成为其他应用 ML 领域不可或缺的一部分，我们认为研究和设计可解释、真实且值得信赖的 IR 模型非常重要。

### 段落 144 · Page 19

**EN**

The architectural innovations discussed in this section highlight a mature research field dedicated to harnessing pre-trained transformers for information retrieval. The central theme has been the architectural tradeoff between interaction depth and computational cost, giving rise to a spectrum of models from highly effective cross-encoder rerankers to efficient bi-encoder retrievers. By developing advanced representations—whether dense, sparse, or multi-vector—and hybridizing these approaches, the community has pushed the boundaries of the classic “retrieve-then-rank” paradigm.

**中文**

本节讨论的架构创新突出了一个致力于利用预先训练的Transformer进行信息检索的成熟研究领域。中心主题是交互深度和计算成本之间的架构权衡，从而产生了从高效的交叉编码器重新排序器到高效的双编码器检索器的一系列模型。通过开发高级表示（无论是密集的、稀疏的还是多向量的）并混合这些方法，社区已经突破了经典的“检索然后排序”范式的界限。

### 段落 145 · Page 19

**EN**

However, these models still primarily function as specialized components for representation and scoring. The next wave of innovation emerged from models capable not only of understanding text but also of generating it, marking the beginning of the era of Large Language Models. 19

**中文**

然而，这些模型仍然主要用作表示和评分的专用组件。下一波创新浪潮源于不仅能够理解文本而且能够生成文本的模型，标志着大型语言模型时代的开始。 19

### Page 20

### 段落 146 · Page 20

**EN**

Published in Transactions on Machine Learning Research (02/2026) 7 Large Language Models for IR Thenaturalevolutionfrompre-trainedencodersistherecentascendanceofLargeLanguageModels(LLMs). 4 While building on the same transformer principles discussed in Section 6, the sheer scale and generative capabilities of modern instruction-following LLMs are reshaping the architectural landscape of IR. These models are not just larger backbones for feature extraction; their proficiency in language understanding, generation, and instruction-following allows them to take on entirely new roles.

**中文**

发表于《机器学习研究汇刊》(02/2026) 7 IR 的大型语言模型 预训练编码器的自然进化是大型语言模型 (LLM) 的近期崛起。 4 虽然建立在第 6 节中讨论的相同Transformer原理的基础上，但现代指令型法学硕士的庞大规模和生成能力正在重塑 IR 的架构景观。这些模型不仅是特征提取的更大骨干；他们在语言理解、生成和遵循指令方面的熟练程度使他们能够承担全新的角色。

### 段落 147 · Page 20

**EN**

Trained to align with human preferences (OpenAI et al., 2023; Gemini Team Google et al., 2023; Bai et al., 2022), LLMs can perform complex tasks such as reasoning (Wei et al., 2022; OpenAI et al., 2024; Guo et al., 2025), tool usage (Schick et al., 2023; Patil et al., 2024b; Qin et al., 2024a; Patil et al., 2024a) and planning (Song et al., 2023; Huang et al., 2024a). In this section, we review how these powerful models—spanningdecoder-onlyand encoder-decoderarchitectures—are being adapted for IR tasks, moving beyond established paradigms into new frontiers of retrieval, reranking, and direct generation.

**中文**

经过训练以符合人类偏好（OpenAI 等人，2023；Gemini Team Google 等人，2023；Bai 等人，2022），法学硕士可以执行复杂的任务，例如推理（Wei 等人，2022；OpenAI 等人，2024；Guo 等人，2025）、工具使用（Schick 等人，2023；Patil 等人， 2024b；Qin 等人，2024a；Patil 等人，2024a）和规划（Song 等人，2023；Huang 等人，2024a）。在本节中，我们将回顾这些强大的模型（仅限解码器和编码器-解码器架构）如何适应 IR 任务，超越既定范例进入检索、重新排序和直接生成的新领域。

### 段落 148 · Page 20

**EN**

7.1 LLM as Retriever A straightforward yet highly effective application of LLMs is to serve as the backbone for bi-encoder retrieval models. We categorize these developments into backbone scaling, architectural adaptation, and unified modeling. We show a shortlist of works in Table 5. Scaling Bi-Encoders.The dramatic increase in parameter count and training data provides LLMs with richer world knowledge and a more nuanced understanding of semantics compared to their smaller BERTsized predecessors. This directly translates to performance improvements. Neelakantan et al.

**中文**

7.1 LLM 作为检索器 LLM 的一个简单而高效的应用是作为双编码器检索模型的支柱。我们将这些开发分为骨干扩展、架构适应和统一建模。我们在表 5 中展示了一份工作清单。扩展双编码器。与规模较小的 BERT 前辈相比，参数数量和训练数据的急剧增加为法学硕士提供了更丰富的世界知识和对语义更细致的理解。这直接转化为性能改进。尼拉坎坦等人。

### 段落 149 · Page 20

**EN**

(2022) finetuned a series of off-the-shelfGPTmodels towards text and code representation. They empirically verified that the bi-encoder retriever’s performance can benefit from increased backbone language model capacity. Muennighoff (2022); Ma et al. (2024b) empirically verified the effectiveness of scaling the size of dense retrievers with open-weight models such asGPT-J(Wang & Komatsuzaki, 2021) andLlama-2(Touvron et al., 2023).

**中文**

(2022) 针对文本和代码表示微调了一系列现成的 GPT 模型。他们凭经验验证，双编码器检索器的性能可以受益于骨干语言模型容量的增加。穆尼尼霍夫 (2022)；马等人。 (2024b) 凭经验验证了使用开放权重模型（例如 GPT-J（Wang & Komatsuzaki，2021）和 Llama-2（Touvron 等人，2023））缩放密集检索器大小的有效性。

### 段落 150 · Page 20

**EN**

Today, common text retrieval benchmarks like BEIR (Thakur et al., 2021) and MTEB (Muennighoff et al., 2023) are dominated by proprietary and open-source LLM-based embedding models (Wang et al., 2023a; Li et al., 2023d; Lee et al., 2025; Zhang et al., 2025b; Muennighoff et al., 2025,inter alia). Decoder-OnlyAdaptation.Aparallellineofresearchfocusesonadaptingtheunidirectionalarchitecture of decoder-only LLMs (e.g.,Llama) to better suit the needs of bidirectional text representation. Standard decoder-only models are optimized for next-token prediction, which may not be ideal for creating a single summary vector for a whole text.

**中文**

如今，BEIR（Thakur 等人，2021）和 MTEB（Muennighoff 等人，2023）等常见文本检索基准主要由基于 LLM 的专有和开源嵌入模型主导（Wang 等人，2023a；Li 等人，2023d；Lee 等人，2025；Zhang 等人，2025b；Muennighoff 等人）等人，2025 年等）。仅解码器适配。并行研究重点是调整仅解码器 LLM（例如 Llama）的单向架构，以更好地满足双向文本表示的需求。标准的仅解码器模型针对下一个标记预测进行了优化，这对于为整个文本创建单个摘要向量可能并不理想。

### 段落 151 · Page 20

**EN**

To address this,LLM2Vec(BehnamGhader et al., 2024) enables bidirectional attention and further trainsLlama-2 (Touvron et al., 2023) with specific unsupervised and supervised adaptive tasks. Similarly,NV-Embed(Lee et al., 2025) introduces a new latent attention mechanism to produce improved representations, leading to improved performance on the MTEB benchmark compared to directly enabling bi-directional attention.

**中文**

为了解决这个问题，LLM2Vec（BehnamGhader 等人，2024）实现了双向注意力，并通过特定的无监督和监督自适应任务进一步训练 Llama-2（Touvron 等人，2023）。同样，NV-Embed（Lee et al., 2025）引入了一种新的潜在注意力机制来产生改进的表示，与直接启用双向注意力相比，从而提高了 MTEB 基准上的性能。

### 段落 152 · Page 20

**EN**

Unified Modeling.GritLM(Muennighoff et al., 2025) fine-tunesMistralfamily models with both dense retrieval task and text generation task with different attention mechanisms and demonstrate the potential of unifying retrieval and generation with one single foundation model. 7.2 LLM as Reranker The reranking task has also been significantly advanced by LLMs, which introduce new capabilities beyond the cross-encoder architecture discussed in Section 6. This evolution can be categorized into two main architectural approaches: fine-tuning and zero-shot prompting. We show a shortlist of works that use LLM as rerankers in Table 6.

**中文**

Unified Modeling.GritLM（Muennighoff et al., 2025）对具有不同注意机制的密集检索任务和文本生成任务的 Mistralfamily 模型进行了微调，并展示了用一个基础模型统一检索和生成的潜力。 7.2 LLM 作为重排序器 LLM 也显着推进了重排序任务，它引入了超越第 6 节中讨论的跨编码器架构的新功能。这种演变可以分为两种主要的架构方法：微调和零样本提示。我们在表 6 中展示了使用 LLM 作为重新排序器的作品的候选名单。

### 段落 153 · Page 20

**EN**

4The term “Large Language Model” lacks a precise, universally accepted definition in the literature. In this survey, we use the term to refer to models with over one billion parameters that are pre-trained with a text generation objective, such as text infilling (e.g.,T5) or causal language modeling (e.g., theGPTseries), and are often optionally post-trained for instruction following and human preference alignment. 20

**中文**

4“大语言模型”一词在文献中缺乏精确的、普遍接受的定义。在本次调查中，我们使用该术语来指代具有超过 10 亿个参数的模型，这些模型使用文本生成目标进行了预训练，例如文本填充（例如 T5）或因果语言模型（例如 GPT 系列），并且通常可以选择进行后训练以进行指令跟踪和人类偏好对齐。 20

### Page 21

### 段落 154 · Page 21

**EN**

Published in Transactions on Machine Learning Research (02/2026) Fine-Tuned Rerankers.First, LLMs can be fine-tuned as powerful rerankers. Extending earlier work onBERT-type models, researchers have applied similar techniques to larger encoder-decoder models like T5(Raffel et al., 2020) and decoder-only models likeLlama(Touvron et al., 2023). •Pointwise and Pairwise:Nogueira et al.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 微调重排序器。首先，LLM 可以作为强大的重排序器进行微调。扩展早期关于 BERT 型模型的工作，研究人员将类似的技术应用于更大的编码器-解码器模型，如 T5（Raffel 等人，2020）和仅解码器模型，如 Llama（Touvron 等人，2023）。 •逐点和成对：Nogueira 等人。

### 段落 155 · Page 21

**EN**

(2020) fine-tunedT5with a classification loss, treating rerankingasabinaryrelevancedecision.RankT5(Zhuangetal.,2023a)tookamoredirectapproach by fine-tuningT5to output a numerical relevance score, optimizing the model with established ranking losses likeRankNet(Burges, 2010). Further, Zhuang et al. (2023a) also investigated the impact of language model architectures (T5encoder-decoder versusT5encoder), loss functions (pointwise, pairwise, listwise), and pooling strategies to ranking performance.

**中文**

(2020) 对 T5 进行了分类损失的微调，将重排视为二进制相关性决策。RankT5 (Zhuangetal.,2023a) 采用了更直接的方法，通过微调 T5 来输出数值相关性得分，并使用已建立的排名损失（如 RankNet（Burges，2010））优化模型。此外，庄等人。 (2023a) 还研究了语言模型架构（T5 编码器-解码器与 T5 编码器）、损失函数（逐点、成对、列表）以及池化策略对性能排名的影响。

### 段落 156 · Page 21

**EN**

•Listwise:Instead of scoring documents individually,ListT5(Yoon et al., 2024) adopts a Fusionin-Decoder architecture (Izacard & Grave, 2021) to process and rank an entire list of candidate documents in a single forward pass. More specifically, the architecture consists of an encoder and decoder, where the encoder takes a query and multiple passages as input in parallel, and the decoder outputs a sorted list of input passages in the decreasing order of relevance, achieving better reranking efficiency compared to pointwise methods. Yang et al.

**中文**

•Listwise：ListT5（Yoon 等人，2024）采用 Fusionin-Decoder 架构（Izacard & Grave，2021），而不是单独对文档进行评分，在一次前向传递中对整个候选文档列表进行处理和排名。更具体地说，该架构由编码器和解码器组成，其中编码器并行地将查询和多个段落作为输入，解码器以相关性降序输出输入段落的排序列表，与逐点方法相比，实现了更好的重排序效率。杨等人。

### 段落 157 · Page 21

**EN**

(2025b) fine-tunedQwQ-32B (Qwen Team, 2025) for listwise reranking where multiple passages are concatenated together as input and achieved better performance than pointwise reranking, leveraging the reasoning and long context capability of the strong base model. •Long-Context Reranking:The long-context capabilities of modern LLMs have also enabled a new reranking paradigm.RankLlama(Ma et al., 2024b) demonstrated superior pointwise reranking performance compared toBERTandT5-based rerankers for long document reranking where the input is truncated at 4,096 tokens.

**中文**

(2025b) 微调QwQ-32B（Qwen Team，2025）用于列表重新排序，其中多个段落作为输入连接在一起，并利用强基础模型的推理和长上下文能力，实现了比逐点重新排序更好的性能。 •长上下文重排序：现代法学硕士的长上下文功能也启用了新的重排序范例。RankLlama（Ma et al., 2024b）在长文档重排序（输入被截断为 4,096 个标记）中，与基于 BERT 和 T5 的重排序器相比，表现出了卓越的逐点重排序性能。

### 段落 158 · Page 21

**EN**

Zero-Shot / Few-Shot Prompting.Second, the instruction-following ability of modern LLMs has unlocked zero-shot and few-shot reranking via prompting. This paradigm requires no task-specific fine-tuning. Instead, the LLM is prompted with a query and a list of candidate documents and asked to identify the most relevant ones (Ma et al., 2023; Zhang et al., 2023c; Pradeep et al., 2023b;c; Sun et al., 2023). This listwise approach is a natural fit for the long context windows of models like GPT-4. To mitigate the high computational cost and context length limitations of processing full documents, Liu et al.

**中文**

零样本/少样本提示。其次，现代法学硕士的指令跟踪能力通过提示解锁了零样本和少样本重排。该范例不需要针对特定​​任务进行微调。相反，法学硕士会收到查询和候选文档列表的提示，并被要求识别最相关的文档（Ma et al., 2023；Zhang et al., 2023c；Pradeep et al., 2023b;c；Sun et al., 2023）。这种列表方式非常适合 GPT-4 等模型的长上下文窗口。为了减轻处理完整文档的高计算成本和上下文长度限制，Liu 等人。

### 段落 159 · Page 21

**EN**

(2024b) proposed using passage embeddings as compact document representations for the LLM, training a specialized reranker that operates on these embeddings to improve efficiency. As this line of research primarily involves prompt engineering rather than architectural changes, we refer readers to a recent survey (Zhu et al., 2023) for further details. 7.3 Generative Retrieval Perhaps the most radical architectural shift enabled by LLMs is generative retrieval. Traditional IR systems follow the “retrieve-then-rerank” paradigm (Schütze et al., 2008; Asai et al., 2024a; Xu et al., 2025c).

**中文**

（2024b）建议使用段落嵌入作为法学硕士的紧凑文档表示，训练一个专门的重新排序器来对这些嵌入进行操作以提高效率。由于这一领域的研究主要涉及即时工程而不是架构变更，因此我们建议读者参阅最近的一项调查（Zhu et al., 2023）以了解更多详细信息。 7.3 生成检索 也许法学硕士带来的最根本的架构转变是生成检索。传统的 IR 系统遵循“检索然后重新排序”范式（Schütze 等人，2008；Asai 等人，2024a；Xu 等人，2025c）。

### 段落 160 · Page 21

**EN**

Generative retrieval fundamentally challenges this by reframing retrieval as a sequence-to-sequence task. Instead of searching an index, an autoregressive language model is trained to directly generate the unique document identifiers (DocIDs) of relevant documents in response to a query. Evolution of the Paradigm.The foundational work in generative retrieval emerged from the entity linking domain with Generation of ENtity REtrieval (GENRE, De Cao et al., 2021).

**中文**

生成检索通过将检索重新定义为序列到序列的任务，从根本上挑战了这一点。自回归语言模型不是搜索索引，而是经过训练直接生成相关文档的唯一文档标识符 (DocID) 以响应查询。范式的演变。生成检索的基础工作源自实体链接域和 Generation of ENtity REtrieval (GENRE, De Cao et al., 2021)。

### 段落 161 · Page 21

**EN**

Rather than treating entity retrieval as a classification problem over atomic labels with dense representations, GENRE reframed it as a generative task where an encoder-decoder model produces entity names autoregressively, token-bytoken, conditioned on the input context. Building on GENRE’s success, DSI introduced generative retrieval to the broader document retrieval domain (Tay et al., 2022).

**中文**

GENRE 没有将实体检索视为具有密集表示的原子标签的分类问题，而是将其重新构建为生成任务，其中编码器-解码器模型以输入上下文为条件，逐个令牌地自回归生成实体名称。在 GENRE 成功的基础上，DSI 将生成检索引入了更广泛的文档检索领域（Tay 等人，2022）。

### 段落 162 · Page 21

**EN**

The core innovation was fully parameterizing traditional “retrieve-then-rerank” pipelines within a single neural model, where all corpus information is encoded in the model parameters rather than external indices (Tay et al., 2022; Pradeep et al., 2023a). DSI operates through two fundamental sequence-to-sequence tasks that can be trained jointly or sequentially (He et al., 2024): the indexing task (Learn to Index) and the retrieval task (Learn to Retrieve). 21

**中文**

核心创新是在单个神经模型中完全参数化传统的“检索然后重新排序”管道，其中所有语料库信息都编码在模型参数中而不是外部索引中（Tay 等人，2022；Pradeep 等人，2023a）。 DSI 通过两个基本的序列到序列任务进行操作，这些任务可以联合或顺序训练（He et al., 2024）：索引任务（Learn to Index）和检索任务（Learn to Retrieve）。 21

### Page 22

### 段落 163 · Page 22

**EN**

Published in Transactions on Machine Learning Research (02/2026) Table 4: Taxonomy of identifier types in Generative Retrieval. The choice of identifier is a key architectural distinction. Identifier Type Description Atomic IdentifiersUnique integers assigned to documents. Simple but lacks semantic generalization. String IdentifiersNatural language strings (titles, URLs). Leverages pre-trained knowledge but can be ambiguous. Semantic IdentifiersStructured IDs derived from clustering embeddings. Enables semantic generalization in the ID space. Table 5: Summary of IR model architecture utilizing large language models as retrieval backbone.

**中文**

发表于机器学习研究交易 (02/2026) 表 4：生成检索中标识符类型的分类。标识符的选择是一个关键的架构区别。标识符类型 描述 原子标识符 分配给文档的唯一整数。简单但缺乏语义概括。字符串标识符自然语言字符串（标题、URL）。利用预先训练的知识，但可能不明确。语义标识符源自聚类嵌入的结构化 ID。启用 ID 空间中的语义泛化。表 5：利用大型语言模型作为检索主干的 IR 模型架构摘要。

### 段落 164 · Page 22

**EN**

Name Architecture Backbone LM Training strategy CPT-Text(Neelakantan et al., 2022)LLM EncoderGPT-3 Listwise Loss SGPT-BE(Muennighoff, 2022) LLM EncoderGPT-J&GPT-NeoX Listwise Loss GTR(Ni et al., 2022b) LLM EncoderT5 Listwise Loss RepLlama(Ma et al., 2024b) LLM EncoderLlama Listwise Loss E5-Mistral(Wang et al., 2023a)LLM EncoderMistral Synthetic Data + Listwise Loss LLaRA(Li et al., 2023b) LLM EncoderLlama Adaptation + Contrastive Training MambaRetriever(Zhang et al., 2024)LLM EncoderMamba Listwise Loss LLM2Vec(BehnamGhader et al., 2024)LLM EncoderLlama&Mistral Adaptation + Contrastive Pre-training Grit-LM(Muennighoff et al., 2025)LLM Mistral&

**中文**

名称 架构 Backbone LM 训练策略 CPT-Text(Neelakantan et al., 2022)LLM EncoderGPT-3 Listwise Loss SGPT-BE(Muennighoff, 2022) LLM EncoderGPT-J&GPT-NeoX Listwise Loss GTR(Ni et al., 2022b) LLM EncoderT5 Listwise Loss RepLlama(Ma et al., 2024b) LLM EncoderLlama Listwise Loss E5-Mistral(Wang et al., 2023a)LLM EncoderMistral Synthetic Data + Listwise Loss LLaRA(Li et al., 2023b) LLM EncoderLlama Adaptation + Contrastive Training MambaRetriever(Zhang et al., 2024)LLM EncoderMamba Listwise Loss LLM2Vec(BehnamGhader et al., 2024)LLM EncoderLlama&Mistral Adaptation + 对比预训练 Grit-LM(Muennighoff et al., 2025)LLM Mistral&

### 段落 165 · Page 22

**EN**

Mixtral 8x7BGenerative/Embedding Joint Training NVEmbed(Lee et al., 2025) LLM EncoderMistral Adaptation + Synthetic Data + Listwise Loss GTE-Qwen2-Instruct(Li et al., 2023d)LLM EncoderQwen Adaptation + Synthetic Data + Listwise Loss Qwen3-Retriever(Zhang et al., 2025b)LLM EncoderQwen3 Synthetic Data + Listwise Loss Taxonomy of Identifiers.A critical design choice in DSI involves document identifier representation (summarized in Table 4).

**中文**

Mixtral 8x7B生成/嵌入联合训练 NVEmbed(Lee et al., 2025) LLM EncoderMistral Adaptation + Synthetic Data + Listwise Loss GTE-Qwen2-Instruct(Li et al., 2023d)LLM EncoderQwen Adaptation + Synthetic Data + Listwise Loss Qwen3-Retriever(Zhang et al., 2025b)LLM EncoderQwen3 合成数据 + 标识符的列表损失分类法。DSI 中的一个关键设计选择涉及文档标识符表示（表 4 中总结）。

### 段落 166 · Page 22

**EN**

•Atomic and String Identifiers:Early work explored atomic identifiers (unique integers) and simple string identifiers (titles, URLs) (Chen et al., 2023a). DSI can be implemented in two variants: classification-based approaches that use a classification layer to output atomic document identifiers, and generative approaches that autoregressively generate identifier strings (Mehta et al., 2023). More sophisticated methods have introduced n-gram-based identifiers (Bevilacqua et al., 2022). •Semantic Identifiers:Semantically structured identifiers created through clustering algorithms proved most effective (Zhu et al., 2023).

**中文**

•原子和字符串标识符：早期工作探索了原子标识符（唯一整数）和简单字符串标识符（标题、URL）（Chen 等人，2023a）。 DSI 可以通过两种变体实现：使用分类层输出原子文档标识符的基于分类的方法，以及自回归生成标识符字符串的生成方法（Mehta 等人，2023）。更复杂的方法引入了基于 n 元语法的标识符（Bevilacqua 等人，2022）。 •语义标识符：通过聚类算法创建的语义结构标识符被证明是最有效的（Zhu et al., 2023）。

### 段落 167 · Page 22

**EN**

This often involves hierarchical representations using techniques like residual quantization (Zeng et al., 2024), where the model learns to associate document content with corresponding semantically meaningful document identifiers (Kishore et al., 2023). Inference and Constraints.The technical implementation of generative retrieval systems centers on sequence-to-sequence modeling. A critical technical requirement is ensuring only valid document identifiers are generated during inference. This is typically achieved through constrained beam search over a prefix tree (trie) constructed from all valid document identifiers (Tang et al., 2023).

**中文**

这通常涉及使用残差量化等技术的分层表示（Zeng 等人，2024），其中模型学习将文档内容与相应的语义上有意义的文档标识符相关联（Kishore 等人，2023）。推理和约束。生成检索系统的技术实现以序列到序列建模为中心。一项关键的技术要求是确保在推理过程中仅生成有效的文档标识符。这通常是通过在由所有有效文档标识符构建的前缀树 (trie) 上进行约束波束搜索来实现的（Tang 等人，2023）。

### 段落 168 · Page 22

**EN**

Alternative approaches include constrained greedy search and FM-index structures (Tang et al., 2023). TheT5model backbone (Raffel et al., 2020) serves as the foundation for most DSI implementations, trained with cross-entropy loss on both indexing and retrieval objectives. Challenges.Generative retrieval faces significant challenges in dynamic environments. The tight coupling between index and retrieval modules makes updating the corpus computationally expensive, typically requiring full model retraining (Mehta et al., 2023).

**中文**

替代方法包括约束贪婪搜索和 FM 索引结构（Tang 等人，2023）。 T5 模型主干（Raffel 等人，2020）是大多数 DSI 实现的基础，在索引和检索目标上通过交叉熵损失进行训练。挑战。生成检索在动态环境中面临重大挑战。索引和检索模块之间的紧密耦合使得更新语料库的计算成本高昂，通常需要完整的模型重新训练（Mehta 等人，2023）。

### 段落 169 · Page 22

**EN**

Scalability poses a major challenge; most research has focused on relatively small collections, as the memory and computational requirements grow substantially as corpus size increases. Generative retrieval is an active and rapidly evolving research area; we direct interested readers to a dedicated survey (Li et al., 2025d) for a comprehensive review. 22

**中文**

可扩展性是一个重大挑战；大多数研究都集中在相对较小的集合上，因为随着语料库大小的增加，内存和计算需求也会大幅增长。生成检索是一个活跃且快速发展的研究领域；我们引导感兴趣的读者进行专门调查（Li et al., 2025d）进行全面审查。 22

### Page 23

### 段落 170 · Page 23

**EN**

Published in Transactions on Machine Learning Research (02/2026) Table 6: Summary of IR model architecture utilizing large language models for reranking. Nogueira dos Santos et al. (2020) and Zhuang et al. (2021) revisit the statistic language model problem with modern transformer-based models, includingBART(Lewis et al., 2020a),T5(Raffel et al., 2020), andGPT- 2(Radford et al., 2019). We use Seq2Seq LLM to refer to encoder-decoder architecture language models such asT5andBART, and Casual LLM to refer to modern LLMs with causal language model architecture likeGPTfamily models.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 表 6：利用大型语言模型进行重新排序的 IR 模型架构摘要。诺盖拉·多斯桑托斯等人。 （2020）和庄等人。 (2021) 重新审视现代基于 Transformer 的模型的统计语言模型问题，包括 BART（Lewis 等人，2020a）、T5（Raffel 等人，2020）和 GPT-2（Radford 等人，2019）。我们使用Seq2Seq LLM来指代编码器-解码器架构语言模型，例如T5和BART，使用Casual LLM来指代具有因果语言模型架构的现代LLM，例如GPT系列模型。

### 段落 171 · Page 23

**EN**

Name Architecture Backbone LM Training / Prompting Strategy Fine-tune LLM for Reranking monoT5(Nogueira et al., 2020)Seq2Seq LM T5 Classification Nogueira dos Santos et al.

**中文**

名称 Architecture Backbone LM Training / Prompting Strategy Fine-tune LLM for Reranking monoT5(Nogueira et al., 2020)Seq2Seq LM T5 Classification Nogueira dos Santos et al.

### 段落 172 · Page 23

**EN**

(2020)Seq2Seq LLM BART Unlikelihood QLM-T5(Zhuang et al., 2021)Seq2Seq LLM T5 Language Modeling duoT5(Pradeep et al., 2021)Seq2Seq LLM T5 Pairwise Loss RankT5(Zhuang et al., 2023a)Seq2Seq LLM Encoder + Prediction LayerT5 Listwise Loss ListT5(Yoon et al., 2024) Fusion-in-decoder T5 Listwise Loss SGPT-CE(Muennighoff, 2022)Causal LLM GPT-J&GPT-NeoListwise Loss RankLlama(Ma et al., 2024b)Casual LLM Encoder + Prediction LayerLlama Listwise Loss RankMamba(Xu, 2024) Causal LLM Encoder + Prediction LayerMamba Listwise Loss RankVicuna(Pradeep et al., 2023b)Causal LLM Vicuna Listwise RankZephyr(Pradeep et al., 2023c)Causal LLM Zephyr Listwise Zhang et al.

**中文**

(2020)Seq2Seq LLM BART Likelihood QLM-T5(Zhuang et al., 2021)Seq2Seq LLM T5 Language Modeling duoT5(Pradeep et al., 2021)Seq2Seq LLM T5 Pairwise Loss RankT5(Zhuang et al., 2023a)Seq2Seq LLM Encoder + Prediction LayerT5 Listwise Loss ListT5(Yoon et al., 2024) Fusion-in-decoder T5 Listwise Loss SGPT-CE(Muennighoff, 2022)Causal LLM GPT-J&GPT-NeoListwise Loss RankLlama(Ma et al., 2024b)Casual LLM Encoder + Prediction LayerLlama Listwise Loss RankMamba(Xu, 2024) Causal LLM 编码器 + 预测层Mamba Listwise Loss RankVicuna(Pradeep et al., 2023b)Causal LLM Vicuna Listwise RankZephyr(Pradeep et al., 2023c)Causal LLM Zephyr Listwise Zhang et al.

### 段落 173 · Page 23

**EN**

(2023c) Causal LLM Code-LLaMA-InstructListwise Liu et al. (2024b) Embedding + Causal LLM Mistral Listwise Qwen3-Reranker(Zhang et al., 2025b)Causal LLM Qwen3 Synthetic Data + Pairwise Loss Prompt LLM for Reranking Zhuang et al. (2023b) Causal LLM Multiple Pointwise Prompting Zhuang et al. (2024a) Causal LLM Flan-PaLM-S Pointwise Prompting UPR(Sachan et al., 2022) Seq2Seq LM & Causal LLM T5&GPT-Neo Pointwise Prompting PRP(Qin et al., 2024b) Seq2Seq LM Flan-UL2 Pairwise Prompting Yan et al. (2024) Seq2Seq LM Flan-UL2 Pairwise Prompting Zhuang et al.

**中文**

(2023c) 因果法学硕士代码-LLaMA-InstructListwise Liu 等人。 (2024b) Embedding + Causal LLM Mistral Listwise Qwen3-Reranker(Zhang et al., 2025b)Causal LLM Qwen3 Synthetic Data + Pairwise Loss Prompt LLM for Reranking Zhuang et al. (2023b) 因果法学硕士多点提示 Zhuang 等人。 (2024a) Causal LLM Flan-PaLM-S Pointwise Prompting UPR(Sachan et al., 2022) Seq2Seq LM & Causal LLM T5&GPT-Neo Pointwise Prompting PRP(Qin et al., 2024b) Seq2Seq LM Flan-UL2 Pairwise Prompting Yan 等人。 (2024) Seq2Seq LM Flan-UL2 成对提示 Zhuang 等人。

### 段落 174 · Page 23

**EN**

(2024b) Seq2Seq LM Flan-T5 Pairwise & Setwise Prompting LRL(Ma et al., 2023) Casual LLM GPT-3 Listwise Prompting RankGPT-3.5(Sun et al., 2023)Causal LLM GPT-3.5 Listwise Prompting RankGPT-4(Sun et al., 2023)Causal LLM GPT-4 Listwise Prompting 7.4 Broader Ecosystem and Concluding Remarks Beyond core architectural changes, LLMs are influencing the entire IR ecosystem. Their advanced generative and understanding capabilities are being harnessed for crucial supporting tasks: •Data Synthesis:Modern IR systems require extensive labeled data for training, which is expensive to create.

**中文**

(2024b) Seq2Seq LM Flan-T5 Pairwise & Setwise Prompting LRL(Ma et al., 2023) Casual LLM GPT-3 Listwise Prompting RankGPT-3.5(Sun et al., 2023)Causal LLM GPT-3.5 Listwise Prompting RankGPT-4(Sun et al., 2023)Causal LLM GPT-4 Listwise 提示 7.4 更广泛的生态系统和结束语 除了核心架构变化之外，法学硕士正在影响整个 IR 生态系统。他们先进的生成和理解能力被用于关键的支持任务： •数据合成：现代红外系统需要大量标记数据进行培训，而创建这些数据的成本很高。

### 段落 175 · Page 23

**EN**

A promising line of work is to use LLMs to synthesize high-quality training data (e.g., queries, relevant passages, and hard negatives) (Bonifacio et al., 2022; Boytsov et al., 2024; Dai et al., 2023; Lee et al., 2024; Mo et al., 2024a;c; Zhang et al., 2025b). •Evaluation:From an evaluation perspective, LLMs’ language understanding has led to research on using them as proxies for human relevance judges, which could dramatically accelerate the evaluation cycle (Faggioli et al., 2023; 2024; Clarke & Dietz, 2024).

**中文**

一个有前途的工作是使用法学硕士来合成高质量的训练数据（例如查询、相关段落和硬阴性）（Bonifacio et al., 2022; Boytsov et al., 2024; Dai et al., 2023; Lee et al., 2024; Mo et al., 2024a;c; Zhu et al., 2025b）。 •评估：从评估的角度来看，法学硕士的语言理解引发了将其用作人类相关性法官代理的研究，这可以大大加快评估周期（Faggioli et al., 2023; 2024; Clarke & Dietz, 2024）。

### 段落 176 · Page 23

**EN**

We also point readers to a comprehensive survey on conversational information retrieval (Mo et al., 2024b), another area being reshaped by LLMs. In conclusion, the adoption of LLMs in IR represents more than a simple increase in model scale. While they certainly serve as more powerful feature extractors within existing bi-encoder and cross-encoder frameworks, their unique generative and instruction-following abilities are forging entirely new architectural paradigms like generative retrieval and zero-shot listwise reranking.

**中文**

我们还向读者推荐一项关于会话信息检索的综合调查（Mo et al., 2024b），这是法学硕士正在重塑的另一个领域。总之，IR 中法学硕士的采用不仅仅意味着模型规模的简单增加。虽然它们确实在现有的双编码器和交叉编码器框架中充当更强大的特征提取器，但它们独特的生成和指令跟踪能力正在打造全新的架构范例，例如生成检索和零样本列表重排序。

### 段落 177 · Page 23

**EN**

However, the advancement of IR architecture is not driven solely by the pursuit of superior semantic matching capabilities. The practical deployment of these systems — ranging from lightweight encoders to massive LLMs — necessitates architectures that can withstand rigorous efficiency constraints, handle diverse data modalities, and ensure reliability. We examine these cross-cutting architectural adaptations in the following section. 23

**中文**

然而，IR 架构的进步并不仅仅由追求卓越的语义匹配能力驱动。这些系统（从轻量级编码器到大规模法学硕士）的实际部署需要能够承受严格的效率约束、处理不同数据模式并确保可靠性的架构。我们将在下一节中研究这些跨领域的架构调整。 23

### Page 24

### 段落 178 · Page 24

**EN**

Published in Transactions on Machine Learning Research (02/2026) 8 Architectures for Diverse Scenarios and Constraints The evolution of IR models described in previous sections — from vector space models to LLMs — primarily traces the pursuit of better semantic matching for English text. However, deploying these models in realworld environments requires navigating complex scenarios and constraints beyond pure textual relevance. These include handling diverse data modalities and languages, balancing the inherent tradeoff between accuracy and latency, and ensuring model reliability through calibration.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 8 适用于不同场景和约束的架构 前面几节中描述的 IR 模型的演变（从向量空间模型到法学硕士）主要追溯了对英语文本更好的语义匹配的追求。然而，在现实环境中部署这些模型需要超越纯粹的文本相关性的复杂场景和约束。其中包括处理不同的数据模式和语言，平衡准确性和延迟之间的固有权衡，以及通过校准确保模型的可靠性。

### 段落 179 · Page 24

**EN**

In this section, we review how IR architectures are adapted to meet these specific requirements. Across these settings, architectural choices such as representation granularity and modularity, serve as the primary mechanisms to balance task-specific constraints with scalable retrieval. 8.1 Architectures for Multimodal and Multilingual Data 8.1.1 Multilingual and Cross-Lingual Architectures Problem Definitions and Retrieval Settings.Although often used interchangeably, Multilingual Information Retrieval (MLIR) and Cross-Lingual Information Retrieval (CLIR) correspond to distinct retrieval scenarios.

**中文**

在本节中，我们将回顾如何调整 IR 架构来满足这些特定要求。在这些设置中，表示粒度和模块化等架构选择充当平衡特定于任务的约束与可扩展检索的主要机制。 8.1 多模态和多语言数据的体系结构 8.1.1 多语言和跨语言体系结构 问题定义和检索设置。虽然经常互换使用，但多语言信息检索（MLIR）和跨语言信息检索（CLIR）对应于不同的检索场景。

### 段落 180 · Page 24

**EN**

CLIR refers to the setting in which a user issues a query in a source language and retrieves documents written in a different target language (Oard & Dorr, 1998; Fluhr et al., 1999). This distinction has direct architectural implications: CLIR requires explicit cross-language alignment at query time, whereas MLIR emphasizes building shared or interoperable representations during indexing. The central architectural challenge in CLIR is bridging the lexical and semantic gap between the query and document language spaces (Goworek et al., 2025).

**中文**

CLIR 是指用户以源语言发出查询并检索以不同目标语言编写的文档的设置（Oard & Dorr，1998；Fluhr 等，1999）。这种区别具有直接的架构含义：CLIR 需要在查询时显式跨语言对齐，而 MLIR 强调在索引期间构建共享或可互操作的表示。 CLIR 的核心架构挑战是弥合查询和文档语言空间之间的词汇和语义差距（Goworek 等人，2025）。

### 段落 181 · Page 24

**EN**

In contrast, MLIR is a broader paradigm in which a system indexes and searches over document collections containing multiple languages, potentially serving queries in any of them (Oard & Dorr, 1996; Oard et al., 1999; Fluhr et al., 1999). Architecturally, CLIR can be viewed as a special case of MLIR that explicitly requires cross-language alignment at retrieval time. Early Translation-Centric Architectures.The architectural foundations of cross-lingual retrieval date back to early work on the Vector Space Model (Salton et al., 1975), where cross-language retrieval was framed as a synonymy problem.

**中文**

相比之下，MLIR 是一种更广泛的范例，其中系统对包含多种语言的文档集合进行索引和搜索，可能以其中任何一种语言提供查询服务（Oard & Dorr，1996；Oard 等人，1999；Fluhr 等人，1999）。从架构上来说，CLIR 可以被视为 MLIR 的一个特例，它明确要求在检索时进行跨语言对齐。早期以翻译为中心的架构。跨语言检索的架构基础可以追溯到向量空间模型的早期工作（Salton 等人，1975），其中跨语言检索被视为同义词问题。

### 段落 182 · Page 24

**EN**

Early systems relied on bilingual thesauri to map query terms into a shared conceptual space prior to retrieval, treating translation as a distinct pre-processing step (Salton, 1969; 1970). Architecturally, these systems isolated linguistic complexity into a separate translation component, leaving the retrieval engine itself unchanged and monolingual. When high-quality thesauri were available, such architectures could approach monolingual retrieval performance; however, they were brittle due to limited vocabulary coverage, poor handling of polysemy, and an inability to model multi-word expressions or contextual meaning.

**中文**

早期系统依靠双语同义词库在检索之前将查询术语映射到共享概念空间，将翻译视为独特的预处理步骤（Salton，1969；1970）。从架构上来说，这些系统将语言复杂性隔离到一个单独的翻译组件中，而检索引擎本身保持不变并且是单语言的。当高质量同义词库可用时，这种架构可以接近单语言检索性能；然而，由于词汇覆盖范围有限、多义词处理不当以及无法对多词表达或上下文含义进行建模，它们很脆弱。

### 段落 183 · Page 24

**EN**

Statistical and Representation-Based Cross-Lingual Models.The availability of large parallel corpora in the 1990s, such as the Canadian Hansards5, enabled a shift from static dictionaries to statistically grounded architectures. A major departure from direct translation was introduced by Cross-Language Latent Semantic Indexing (CL-LSI), which projected documents and queries from different languages into a shared, language-independent latent space using Singular Value Decomposition over parallel data (Dumais et al., 1997).

**中文**

基于统计和表示的跨语言模型。20 世纪 90 年代大型并行语料库（例如加拿大 Hansards5）的出现，实现了从静态词典到统计基础架构的转变。跨语言潜在语义索引（CL-LSI）引入了与直接翻译的重大区别，它使用并行数据上的奇异值分解将来自不同语言的文档和查询投影到共享的、独立于语言的潜在空间中（Dumais 等人，1997）。

### 段落 184 · Page 24

**EN**

In parallel, Statistical Machine Translation (SMT) became a dominant architectural component in CLIR systems, with retrieval pipelines adopting either query translation or document translation using probabilistic alignment models such as the IBM Models (Brown et al., 1993). Both CL-LSI and SMT-based pipelines preserved monolingual retrieval backends, differing primarily in whether cross-lingual alignment was achieved through latent semantic projection or probabilistic translation.

**中文**

与此同时，统计机器翻译 (SMT) 成为 CLIR 系统中的主要架构组件，检索管道采用查询翻译或使用概率对齐模型（例如 IBM 模型）的文档翻译（Brown 等人，1993）。 CL-LSI 和基于 SMT 的管道都保留了单语言检索后端，主要区别在于跨语言对齐是通过潜在语义投影还是概率翻译来实现。

### 段落 185 · Page 24

**EN**

These systems established the translation-based retrieval paradigm, where the retrieval engine itself remained monolingual and linguistic complexity was isolated within the translation module. Multilingual Transformers and End-to-End Retrieval.The introduction of multilingual pre-trained transformers, including mBERT and XLM-R, marked a fundamental architectural shift away from explicit 5https://en.wikipedia.org/wiki/Hansard 24

**中文**

这些系统建立了基于翻译的检索范例，其中检索引擎本身仍然是单语言的，并且语言复杂性被隔离在翻译模块内。多语言 Transformers 和端到端检索。多语言预训练 Transformer 的引入，包括 mBERT 和 XLM-R，标志着从显式架构的根本转变 5https://en.wikipedia.org/wiki/Hansard 24

### Page 25

### 段落 186 · Page 25

**EN**

Published in Transactions on Machine Learning Research (02/2026) translation toward shared semantic representation learning (Devlin et al., 2019; Conneau et al., 2020a; MacAvaney et al., 2019a). Trained on large-scale multilingual corpora, these models enabled a single encoder to represent queries and documents across languages, substantially reducing dependence on parallel data (Conneau et al., 2020b; Feng et al., 2022; Shi et al., 2020; Goswami et al., 2021).

**中文**

发表于机器学习研究交易 (02/2026) 向共享语义表示学习的翻译（Devlin 等人，2019；Conneau 等人，2020a；MacAvaney 等人，2019a）。这些模型经过大规模多语言语料库的训练，使单个编码器能够表示跨语言的查询和文档，从而大大减少了对并行数据的依赖（Conneau 等人，2020b；Feng 等人，2022；Shi 等人，2020；Goswami 等人，2021）。

### 段落 187 · Page 25

**EN**

However, general-purpose multilingual encoders often underperform in retrieval settings due to insufficient cross-lingual alignment induced during pretraining (Zhang et al., 2022; Elmahdy et al., 2024), which has been the focus of subsequent research works. Per-Language Modules.To improve the performance of multilingual pre-trained transformers on lowresource languages, a line of works proposed to add language-specific adapters to enable zero-shot or few-shot cross-lingualtransfer.

**中文**

然而，由于预训练期间引起的跨语言对齐不足，通用多语言编码器通常在检索设置中表现不佳（Zhang et al., 2022；Elmahdy et al., 2024），这一直是后续研究工作的重点。每语言模块。为了提高多语言预训练转换器在低资源语言上的性能，一系列工作提出添加特定于语言的适配器以实现零样本或少样本跨语言传输。

### 段落 188 · Page 25

**EN**

Earlyexplorations inNLPcommunity focus onclassicalNLPtaskssuch asdependency parsing and named entity recognition (Üstün et al., 2020; Pfeiffer et al., 2020; Artetxe et al., 2020; Pfeiffer et al., 2021). In the context of IR, Litschko et al. (2022) compared the performance of adapter-based approaches and Sparse-Fine-Tuning Masks (Ansell et al., 2022) to NMT-based approaches and reported their efficacy in both performance and training efficiency.

**中文**

NLP 社区的早期探索侧重于经典 NLP 任务，例如依存句法分析和命名实体识别（Üstün 等人，2020；Pfeiffer 等人，2020；Artetxe 等人，2020；Pfeiffer 等人，2021）。在IR的背景下，Litschko等人。 (2022) 将基于适配器的方法和稀疏微调掩模 (Ansell et al., 2022) 的性能与基于 NMT 的方法进行了比较，并报告了它们在性能和训练效率方面的功效。

### 段落 189 · Page 25

**EN**

Alignment-Focused and Modern Architectures.Tackling the same challenge of per-language modules approaches, specialized multilingual retrieval models such as LaREQA, InfoXLM, and LaBSE enforce tighter alignment between semantically equivalent cross-lingual pairs using parallel corpora and contrastive objectives (Roy et al., 2020; Chi et al., 2021; Feng et al., 2022; Huang et al., 2024b). Notably, these approaches typically preserve the standard transformer backbone, focusing architectural innovation on representation learning objectives rather than structural redesign.

**中文**

以对齐为中心的现代架构。为了解决每种语言模块方法的相同挑战，专门的多语言检索模型（例如 LaREQA、InfoXLM 和 LaBSE）使用并行语料库和对比目标在语义等效的跨语言对之间实施更紧密的对齐（Roy 等人，2020；Chi 等人，2021；Feng 等人，2022；Huang 等人，2024b）。值得注意的是，这些方法通常保留标准Transformer骨干，将架构创新重点放在表示学习目标上，而不是结构重新设计上。

### 段落 190 · Page 25

**EN**

Recent work further refines end-to-end multilingual retrieval through improved data curation, supervision, and knowledge distillation, continuing the shift away from multi-stage translation pipelines toward unified models that directly match meaning across languages (Zhang et al., 2023d; Yang et al., 2024).

**中文**

最近的工作通过改进数据管理、监督和知识提炼进一步完善了端到端多语言检索，继续从多阶段翻译管道转向直接匹配跨语言含义的统一模型（Zhang 等人，2023d；Yang 等人，2024）。

### 段落 191 · Page 25

**EN**

8.1.2 Multimodal Architectures From Shallow Fusion to Deep Joint Embeddings.Early multimodal retrieval architectures relied on modality-specific feature extraction followed by shallow fusion, with text typically represented using bagof-words models and images encoded via hand-crafted descriptors such as scale-invariant feature transform (SIFT) (Lowe, 1999).

**中文**

8.1.2 从浅层融合到深度联合嵌入的多模态架构。早期的多模态检索架构依赖于特定模态的特征提取，然后进行浅层融合，文本通常使用词袋模型表示，图像通过手工制作的描述符（例如尺度不变特征变换（SIFT））编码（Lowe，1999）。

### 段落 192 · Page 25

**EN**

To enable cross-modal comparison, projection-based methods such as canonical correlation analysis (CCA) (Hotelling, 1992) mapped heterogeneous features into a shared embedding space, establishing the foundational principle that multimodal retrieval requires learning semantic correspondences across modalities rather than treating them independently (Rasiwasia et al., 2010; Sharma et al., 2012; Gong et al., 2014; Ranjan et al., 2015).

**中文**

为了实现跨模态比较，基于投影的方法，例如典型相关分析（CCA）（Hotelling，1992）将异构特征映射到共享嵌入空间，建立了多模态检索需要学习跨模态语义对应关系而不是独立处理它们的基本原则（Rasiwasia 等人，2010；Sharma 等人，2012；Gong 等人，2014；Ranjan 等人， 2015）。

### 段落 193 · Page 25

**EN**

The transition to deep learning replaced manual feature engineering with end-to-end representation learning, exemplified by early visual-semantic embedding models such asDe- ViSE(Frome et al., 2013; Wang et al., 2016). Sentence encoders incorporating syntactic structure, including Dependency Tree Recursive Neural Networks (DT-RNNs), further improved alignment by modeling relational semantics (Socher et al., 2014).

**中文**

向深度学习的过渡用端到端表示学习取代了手动特征工程，例如 De-ViSE 等早期视觉语义嵌入模型（Frome 等人，2013 年；Wang 等人，2016 年）。结合句法结构的句子编码器，包括依赖树递归神经网络（DT-RNN），通过建模关系语义进一步改进了对齐（Socher et al., 2014）。

### 段落 194 · Page 25

**EN**

Fragment-level architectures extended this paradigm by decomposing images and sentences into finer-grained units and aligning them with structured max-margin objectives, enabling both global and local cross-modal reasoning (Karpathy et al., 2014). Adversarial frameworks such as ACMRsubsequently refined joint embeddings by introducing nonlinear projections and modality-invariant regularization (Wang et al., 2017). We refer to Wang et al. (2024b) for a comprehensive survey.

**中文**

片段级架构通过将图像和句子分解为更细粒度的单元并将它们与结构化最大边缘目标对齐来扩展了这种范式，从而实现了全局和局部跨模态推理（Karpathy et al., 2014）。 ACMR 等对抗性框架随后通过引入非线性投影和模态不变正则化来完善联合嵌入（Wang 等人，2017）。我们参考王等人。 （2024b）进行全面调查。

### 段落 195 · Page 25

**EN**

Dual-Encoder Contrastive Models and Controlled Interaction.Large-scale vision–language datasets enabled a paradigm shift toward bi-encoder architectures trained with contrastive objectives.CLIP andALIGNindependently encoded images and text and aligned them through contrastive learning on hundreds of millions to billions of image–text pairs, establishing scalable and efficient retrieval backbones (Radford et al., 2021; Jia et al., 2021; Wei et al., 2025).

**中文**

双编码器对比模型和受控交互。大规模视觉语言数据集实现了向使用对比目标训练的双编码器架构的范式转变。CLIP 和 ALIGN 独立编码图像和文本，并通过对数亿至数十亿图像文本对的对比学习来对齐它们，建立可扩展且高效的检索主干（Radford 等人，2021；Jia 等人，2021；Wei 等人， 2025）。

### 段落 196 · Page 25

**EN**

This architectural separation facilitated efficient indexing and retrieval and rapidly generalized to additional modalities including video, audio, depth, and sensor data (Girdhar et al., 2023; Chen et al., 2023b; Kong et al., 2025). Subsequent refinements explored the efficiency–expressivity tradeoff within this paradigm, most notably through late-interaction architectures such asColBERT, which replaced single-vector embeddings with multi-vector representations to enable 25

**中文**

这种架构分离促进了高效的索引和检索，并快速推广到其他模式，包括视频、音频、深度和传感器数据（Girdhar 等人，2023；Chen 等人，2023b；Kong 等人，2025）。随后的改进探索了该范式中的效率与表达力的权衡，最显着的是通过后期交互架构，例如 ColBERT，它用多向量表示取代了单向量嵌入，以实现 25

### Page 26

### 段落 197 · Page 26

**EN**

Published in Transactions on Machine Learning Research (02/2026) token-level matching while preserving much of the efficiency of bi-encoders (Khattab & Zaharia, 2020; Faysse et al., 2025; Wan et al., 2025). Together, these models established a dominant architectural family centered on modality-separated encoding with limited but scalable interaction. Rich Fusion, Hierarchical Interaction, and Unified Architectures.Beyond bi-encoders, multimodal retrieval architectures increasingly incorporated sophisticated mechanisms to support complex reasoning, particularly in video–text retrieval (Chen et al., 2020a).

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 标记级匹配，同时保留双编码器的大部分效率（Khattab & Zaharia，2020；Faysse 等人，2025；Wan 等人，2025）。这些模型共同建立了一个以模态分离编码为中心的主导架构系列，具有有限但可扩展的交互。丰富的融合、分层交互和统一架构。除了双编码器之外，多模态检索架构越来越多地结合复杂的机制来支持复杂的推理，特别是在视频文本检索中（Chen 等人，2020a）。

### 段落 198 · Page 26

**EN**

Transformer-based and hierarchical models decomposed alignment into global-to-local or multi-granular stages, combining cross-modal attention with temporal and semantic structure (Gabeur et al., 2020; Liu et al., 2021; Zhang et al., 2023b; Gorti et al., 2022). Hybrid designs integrated CLIP-style encoders with cross-modal fusion or temporal alignment modules, balancing pretrained representations with task-specific interaction (Portillo-Quintero et al., 2021; Fang et al., 2021). These architectures substantially increase computational cost, often restricting their use to reranking or small candidate sets.

**中文**

基于 Transformer 的分层模型将对齐分解为全局到局部或多粒度阶段，将跨模态注意力与时间和语义结构相结合（Gabeur 等人，2020；Liu 等人，2021；Zhang 等人，2023b；Gorti 等人，2022）。混合设计将 CLIP 式编码器与跨模态融合或时间对齐模块集成，平衡预训练表示与特定任务的交互（Portillo-Quintero 等人，2021；Fang 等人，2021）。这些架构大大增加了计算成本，通常限制其使用于重新排序或小型候选集。

### 段落 199 · Page 26

**EN**

Recent architectures further differentiate between multi-encoder designs that preserve modality-specific encoders and single-encoder models employing full cross-attention at higher computational cost (Li et al., 2019; 2022b; Zhai et al., 2023; Kim et al., 2025). At the same time, multimodal large language models (MLLMs) and multi-agent retrieval frameworks unify retrieval, reasoning, and generation within a single system, while modality-preserving and any-to-any architectures emphasize flexible interaction without collapsing modality structure (Liu et al., 2023; Xie et al., 2024a; Liu et al., 2025b; Xu et al., 2025a; Ju et al., 2025).

**中文**

最近的架构进一步区分了保留特定模态编码器的多编码器设计和以较高计算成本采用完全交叉注意力的单编码器模型（Li et al., 2019; 2022b; Zhai et al., 2023; Kim et al., 2025）。同时，多模态大语言模型（MLLM）和多智能体检索框架将检索、推理和生成统一在一个系统内，而模态保留和任意对任意架构则强调灵活的交互而不破坏模态结构（Liu et al., 2023; Xie et al., 2024a; Liu et al., 2025b; Xu et al., 2025a; Ju et al., 2025）。

### 段落 200 · Page 26

**EN**

Remarks.From a structural perspective, multimodal retrieval architectures can be broadly grouped into: (1) shallow fusion and projection-based models, (2) deep joint-embedding architectures with global or fragment-level alignment, (3) contrastively trained dual-encoder models emphasizing scalability, (4) lateinteraction hybrids balancing efficiency and expressivity, and (5) cross-attention and MLLM-centric architectures enabling deep fusion and unified multimodal reasoning. This progression reflects a recurring architectural tension between interaction richness and computational efficiency.

**中文**

备注：从结构角度来看，多模态检索架构可大致分为：（1）浅层融合和基于投影的模型，（2）具有全局或片段级对齐的深层联合嵌入架构，（3）强调可扩展性的对比训练双编码器模型，（4）平衡效率和表达能力的后期交互混合模型，以及（5）支持深度融合和统一多模态推理的交叉注意和以MLLM为中心的架构。这一进展反映了交互丰富性和计算效率之间反复出现的架构张力。

### 段落 201 · Page 26

**EN**

8.2 Performance-Efficiency Tradeoffs and the Role of Architectural Choices Retrieval systems face a fundamental tradeoff between effectiveness (e.g., recall, MRR, nDCG) and resource efficiency (latency, throughput, memory footprint, and index/update cost). Architectural choices—how queries and documents are represented, how similarity is computed, and how candidates are staged and scored—drive where a method falls on this tradeoff curve.

**中文**

8.2 性能效率权衡和架构选择的作用检索系统面临着有效性（例如召回率、MRR、nDCG）和资源效率（延迟、吞吐量、内存占用和索引/更新成本）之间的基本权衡。架构选择（如何表示查询和文档、如何计算相似性以及如何对候选人进行分级和评分）决定了方法在此权衡曲线上的位置。

### 段落 202 · Page 26

**EN**

Modern neural retrievers demonstrated that learned dense embeddings can substantially improve effectiveness over classic lexical baselines, but achieving that gain requires extra compute and index engineering compared to lightweight lexical methods. A common high-performance design is the bi-encoder (single-vector) architecture (Sections 6 and 7): queries and documents are encoded independently into compact vectors and approximate nearest-neighbor search (ANN) retrieves candidates quickly.

**中文**

现代神经检索器证明，学习的密集嵌入可以大大提高经典词汇基线的有效性，但与轻量级词汇方法相比，实现这种增益需要额外的计算和索引工程。常见的高性能设计是双编码器（单向量）架构（第 6 节和第 7 节）：查询和文档被独立编码为紧凑向量，并且近似最近邻搜索 (ANN) 快速检索候选者。

### 段落 203 · Page 26

**EN**

This architecture is attractive for strict latency budgets and large corpora because it enables highly optimized ANN indexes (e.g., HNSW (Malkov & Yashunin, 2018)) that deliver millisecond-scale queries at large scale; however, single-vector representations can miss fine-grained token-level matches that matter for some queries. To improve effectiveness, researchers have pursued richer interaction patterns.

**中文**

这种架构对于严格的延迟预算和大型语料库很有吸引力，因为它支持高度优化的 ANN 索引（例如，HNSW (Malkov & Yashunin, 2018)），可以大规模提供毫秒级查询；然而，单向量表示可能会错过对某些查询很重要的细粒度标记级别匹配。为了提高有效性，研究人员追求更丰富的交互模式。

### 段落 204 · Page 26

**EN**

Late-interaction or multivector models (e.g.,ColBERTandColPali(Khattab & Zaharia, 2020; Faysse et al., 2025)) keep tokengranular signals and aggregate local token similarities, which raises effectiveness but increases index size and per-query compute; compression and residual quantization techniques can reduce the space/latency penalty but do not eliminate it entirely. Similarly, learned sparse/lexical models (e.g.,SPLADE(Formal et al., 2021a;b)) produce high-dimensional but sparse representations that recover lexical signals and interpretability while trading off somewhat higher compute or indexing complexity versus classical BM25.

**中文**

后期交互或多向量模型（例如，ColBERT 和 ColPali（Khattab & Zaharia，2020；Faysse 等人，2025））保留令牌粒度信号并聚合本地令牌相似性，这提高了有效性，但增加了索引大小和每次查询计算；压缩和残余量化技术可以减少空间/延迟损失，但不能完全消除它。类似地，学习的稀疏/词汇模型（例如，SPLADE（Formal et al., 2021a;b））产生高维但稀疏的表示，可以恢复词汇信号和可解释性，同时权衡与经典 BM25 相比更高的计算或索引复杂性。

### 段落 205 · Page 26

**EN**

These architectural variants illustrate the spectrum: more expressive interactions often translates to better quality, typically at higher memory and latency cost (unless mitigated by compression). A pragmatic pattern in production is staged (two- or multi-stage) retrieval: a fast, coarse first-stage (BM25 or compact dense ANN) produces a small candidate set, and a more expensive cross-encoder or interaction- 26

**中文**

这些架构变体说明了这一范围：更具表现力的交互通常会转化为更好的质量，通常会带来更高的内存和延迟成本（除非通过压缩来缓解）。生产中的实用模式是分阶段（两阶段或多阶段）检索：快速、粗略的第一阶段（BM25 或紧凑密集 ANN）产生一个小的候选集，以及更昂贵的交叉编码器或交互 - 26

### Page 27

### 段落 206 · Page 27

**EN**

Published in Transactions on Machine Learning Research (02/2026) based reranker refines the top results (Huang et al., 2020; Su et al., 2025). This cascade yields most of the accuracy of expensive models while preserving throughput, but it requires careful budgeting (how many candidates to pass) and engineering (batching, caching, and efficient GPU/CPU placement). Indexing and compression techniques (e.g., product quantization, pruning, residual quantization), along with hybrid lexical–dense pipelines, are commonly employed to navigate the tradeoff curve as operational constraints evolve.

**中文**

发表在 Transactions on Machine Learning Research (02/2026) 上，基于重排序器细化了顶级结果（Huang 等人，2020；Su 等人，2025）。这种级联产生了昂贵模型的大部分准确性，同时保留了吞吐量，但它需要仔细的预算（要通过多少候选）和工程（批处理、缓存和高效的 GPU/CPU 放置）。随着操作约束的发展，索引和压缩技术（例如，乘积量化、修剪、残差量化）以及混合词汇密集管道通常用于引导权衡曲线。

### 段落 207 · Page 27

**EN**

Architectural Design Heuristics.Adopt a single-vector dual-encoder with efficient ANN search when low latency, low cost, and frequent updates are the primary constraints. Favor multi-vector or interactionintensive models when top-tier ranking quality is required and computational budget permits. To balance these objectives, employ a two-stage pipeline comprising coarse retrieval followed by a specialized reranker. In large-scale deployments, the effectiveness-efficiency operating point is chiefly adjusted through index compression techniques, hybrid lexical-dense signals, and careful calibration of candidate set size.

**中文**

启发式架构设计。当低延迟、低成本和频繁更新是主要限制时，采用具有高效 ANN 搜索的单向量双编码器。当需要顶级排名质量并且计算预算允许时，优先考虑多向量或交互密集型模型。为了平衡这些目标，采用两阶段管道，包括粗略检索和专门的重新排序器。在大规模部署中，有效性-效率操作点主要通过索引压缩技术、混合词汇密集信号以及候选集大小的仔细校准来调整。

### 段落 208 · Page 27

**EN**

8.3 Calibration and Confidence Estimation Calibration in IR aims to align model scores with true probabilities of relevance, such that confidence faithfully reflects correctness. Unlike traditional deterministic rankers that output single relevance scores, calibrated IR models explicitly represent uncertainty, often as a distribution over scores whose mean encodes relevance belief and whose variance captures uncertainty (Cohen et al., 2021). This distinction is architecturally significant: uncertainty-aware scoring exposes information that is otherwise hidden in standard ranking pipelines.

**中文**

8.3 校准和置信度估计 IR 中的校准旨在将模型得分与真实的相关概率对齐，从而使置信度忠实地反映正确性。与输出单一相关性分数的传统确定性排名器不同，校准后的 IR 模型明确表示不确定性，通常作为分数的分布，其平均值编码相关性信念，其方差捕获不确定性（Cohen 等人，2021）。这种区别在架构上具有重要意义：不确定性感知评分公开了隐藏在标准排名管道中的信息。

### 段落 209 · Page 27

**EN**

The importance of calibration is formalized by the Probability Ranking Principle (PRP), which guarantees optimal ranking only when relevance probabilities are well calibrated and reported with certainty (Penha & Hauff, 2021). However, modern neural rankers frequently violate these assumptions, motivating calibration-aware architectural design. Neural Architectures and Uncertainty Modeling.Calibration properties in IR are strongly dependent on architectural choices, with empirical studies showing mixed calibration behavior across neural model families (Guo et al., 2017; Minderer et al., 2021).

**中文**

校准的重要性由概率排名原则 (PRP) 形式化，只有在相关概率得到良好校准并确定报告时才能保证最佳排名（Penha & Hauff，2021）。然而，现代神经排序器经常违反这些假设，从而激发了校准感知架构设计。神经架构和不确定性建模。IR 中的校准属性在很大程度上取决于架构选择，实证研究显示神经模型系列中存在混合校准行为（Guo 等人，2017 年；Minderer 等人，2021 年）。

### 段落 210 · Page 27

**EN**

Transformer-based rankers, includingBERTvariants, are often poorly calibrated, with calibration quality varying by model scale and design (Dan & Roth, 2021; Li et al., 2022a). Introducing stochasticity at the architectural level—through stochastic inference or approximate Bayesian formulations—consistently improves calibration compared to deterministic counterparts, while adding only modest computational overhead (Penha & Hauff, 2021; Cohen et al., 2021). These findings position stochastic and Bayesian architectures as principled mechanisms for embedding uncertainty directly into relevance estimation.

**中文**

基于 Transformer 的排序器（包括 BERT 变体）通常校准不佳，校准质量因模型规模和设计而异（Dan & Roth，2021；Li 等人，2022a）。与确定性对应物相比，通过随机推理或近似贝叶斯公式，在架构级别引入随机性始终可以改善校准，同时仅增加适度的计算开销（Penha & Hauff，2021；Cohen 等人，2021）。这些发现将随机和贝叶斯架构定位为将不确定性直接嵌入到相关性估计中的原则机制。

### 段落 211 · Page 27

**EN**

Calibration in Multi-Component Retrieval Systems.Calibration challenges are amplified in multistage retrieval architectures, such as the “retrieve-then-rerank” pipeline, where hard top-kretrieval steps break differentiability and preclude end-to-end calibration. Architectural interventions, including differentiable sampling mechanisms based on Gumbel approximations, restore gradient flow and enable joint calibration of retriever and reader components (Dhuliawala et al., 2022).

**中文**

多组件检索系统中的校准。在多级检索架构中，校准挑战被放大，例如“检索然后重新排序”管道，其中硬顶检索步骤破坏了可微性并排除了端到端校准。架构干预措施，包括基于 Gumbel 近似的可微分采样机制，恢复梯度流并实现检索器和读取器组件的联合校准（Dhuliawala 等人，2022）。

### 段落 212 · Page 27

**EN**

Jointly calibrated systems produce more reliable confidence estimates than calibrating individual modules in isolation, underscoring how calibration requirements can directly shape architectural design in complex IR pipelines. Modularity and Calibration-Aware Computation.Beyond end-to-end design, modular architectures enable calibration to be treated as an attachable component rather than an intrinsic model property. Universal post-hoc calibrators can be applied across heterogeneous retrieval architectures without modifying their internals, offering scalable and architecture-agnostic improvements (Zhang et al., 2021a).

**中文**

联合校准的系统比单独校准各个模块产生更可靠的置信度估计，这强调了校准要求如何直接塑造复杂红外管道中的架构设计。模块化和校准感知计算。除了端到端设计之外，模块化架构还使校准能够被视为可附加组件，而不是固有的模型属性。通用事后校准器可以跨异构检索架构应用，而无需修改其内部结构，从而提供可扩展且与架构无关的改进（Zhang 等人，2021a）。

### 段落 213 · Page 27

**EN**

When uncertainty is explicitly modeled, calibration becomes operational rather than merely diagnostic: confidence estimates can guide adaptive computation, such as selective reranking or deferred inference for ambiguous queries, improving both efficiency and robustness (Cohen et al., 2021; Yoon et al., 2025). Recent evidence further suggests that architectural specialization—e.g., modeling relevance across multiple criteria instead of a single scalar score—can inherently reduce calibration error, reinforcing calibration as a first-class archi- 27

**中文**

当不确定性被明确建模时，校准变得可操作而不仅仅是诊断：置信度估计可以指导自适应计算，例如对不明确查询的选择性重新排序或延迟推理，从而提高效率和鲁棒性（Cohen 等人，2021；Yoon 等人，2025）。最近的证据进一步表明，架构专业化（例如，跨多个标准而不是单个标量分数进行相关性建模）可以本质上减少校准误差，从而增强作为一流架构的校准27

### Page 28

### 段落 214 · Page 28

**EN**

Published in Transactions on Machine Learning Research (02/2026) tectural consideration in IR system design (Penha & Hauff, 2021; Javdan et al., 2025). To summarize, how to incorporate calibration into modern retrieval systems is still an open question in the IR community. 8.4 Domain-Specific Applications General Web Search.General-purpose web search has historically been dominated by the “retrievethen-rerank” paradigm, built around inverted indexes and multi-stage cascade ranking to ensure efficiency at web scale (Shen et al., 2014a; Mitra et al., 2016; Qin et al., 2022; Zhang et al., 2025a).

**中文**

发表于 Transactions on Machine Learning Research (02/2026) IR 系统设计中的结构考虑（Penha & Hauff，2021；Javdan 等人，2025）。总而言之，如何将校准纳入现代检索系统仍然是 IR 界的一个悬而未决的问题。 8.4 特定领域应用通用网络搜索。通用网络搜索历来以“检索-重新排序”范式为主导，围绕倒排索引和多级级联排名构建，以确保网络规模的效率（Shen 等人，2014a；Mitra 等人，2016；Qin 等人，2022；Zhang 等人，2025a）。

### 段落 215 · Page 28

**EN**

These architectures decompose retrieval into heterogeneous components for query understanding, candidate generation, ranking, and re-ranking, each optimized independently (Wang & Na, 2023). As web content diversified, search engines incorporated additional signals such as anchor text, hyperlinks, and layout-based features to enrich document representations beyond plain text (Oliveira & Teixeira Lopes, 2023). While highly effective, these pipelines impose rigid, predefined information flows that limit adaptability.

**中文**

这些架构将检索分解为异构组件，用于查询理解、候选生成、排名和重排，每个组件都独立优化（Wang & Na，2023）。随着网络内容多样化，搜索引擎纳入了锚文本、超链接和基于布局的功能等附加信号，以丰富纯文本之外的文档表示形式（Oliveira & Teixeira Lopes，2023）。虽然非常有效，但这些管道强加了严格的、预定义的信息流，限制了适应性。

### 段落 216 · Page 28

**EN**

The recent generative retrieval (Section 7.3) thus explores replacing this modular pipeline with model-centric architectures, where a single LLM performs indexing, retrieval, and ranking end-to-end. Domain-Specific and Thematic Retrieval.Domain-specific search engines target focused corpora such as scientific literature, medicinal chemistry databases, and job postings, leveraging domain knowledge to improve relevance beyond general web search. These applications share architectural challenges arising from specialized terminology, underspecified expert queries, and narrowly scoped user intents (Wang & Na, 2023; Kang et al., 2024).

**中文**

因此，最近的生成检索（第 7.3 节）探索用以模型为中心的架构取代这种模块化管道，其中单个 LLM 执行端到端的索引、检索和排名。特定领域和主题检索。特定领域搜索引擎针对科学文献、药物化学数据库和职位发布等重点语料库，利用领域知识来提高一般网络搜索之外的相关性。这些应用程序都面临着由专业术语、未指定的专家查询和范围狭窄的用户意图带来的架构挑战（Wang & Na，2023；Kang 等人，2024）。

### 段落 217 · Page 28

**EN**

Generic pretrained models often fail to capture domain-specific semantics without architectural support for structured knowledge. Traditional solutions rely on query expansion, lexical analysis, and large task-specific training sets, but suffer from scalability and complexity limitations (Xu et al., 2025f). In response, modern architectures increasingly integrate entity- and relation-centric representations to better align retrieval with domain semantics (Dong et al., 2022a). As a result, domain-specific IR architectures emphasize knowledge-aware representations and domain adaptation over purely generic pretrained models.

**中文**

如果没有结构化知识的架构支持，通用预训练模型通常无法捕获特定领域的语义。传统解决方案依赖于查询扩展、词法分析和大型特定于任务的训练集，但受到可扩展性和复杂性限制（Xu 等人，2025f）。作为回应，现代架构越来越多地集成以实体和关系为中心的表示，以更好地使检索与领域语义保持一致（Dong 等人，2022a）。因此，特定领域的 IR 架构强调知识感知表示和领域适应，而不是纯粹的通用预训练模型。

### 段落 218 · Page 28

**EN**

Medical and Legal Information Retrieval.Medical and legal search systems represent high-stakes instantiations of domain-specific retrieval, imposing stricter architectural constraints. Medical IR must operate over long temporal records that combine unstructured clinical notes with structured diagnoses, laboratory values, and medications, motivating architectures that integrate information extraction, faceted search, and structured database querying (Sonntag & Profitlich, 2018). These systems must additionally handle specialized medical terminology, clinical documentation standards, and stringent privacy requirements.

**中文**

医疗和法律信息检索。医疗和法律搜索系统代表了特定领域检索的高风险实例，施加了更严格的体系结构约束。医学 IR 必须对长期记录进行操作，将非结构化临床记录与结构化诊断、实验室值和药物相结合，从而激发集成信息提取、分面搜索和结构化数据库查询的架构（Sonntag & Profitlich，2018）。这些系统还必须处理专门的医学术语、临床文档标准和严格的隐私要求。

### 段落 219 · Page 28

**EN**

Legal IR faces analogous challenges due to highly specialized language, complex document structures, and limited labeled relevance data (Althammer et al., 2020). Despite recent efforts to adapt pretrained language models such asBERT, neural approaches often fail to consistently outperform strong lexical baselines like BM25, reinforcing the continued relevance of hybrid and lexically grounded architectures in legally specialized domains (de Araujo et al., 2014; Althammer et al., 2020).

**中文**

由于高度专业化的语言、复杂的文档结构和有限的标记相关数据，法律 IR 面临着类似的挑战（Althammer 等人，2020）。尽管最近努力适应 BERT 等预训练语言模型，但神经方法通常无法始终优于 BM25 等强大的词汇基线，从而增强了法律专业领域中混合和词汇基础架构的持续相关性（de Araujo 等人，2014 年；Althammer 等人，2020 年）。

### 段落 220 · Page 28

**EN**

E-commerce Search.E-commerce search systems operate over structured product catalogs rather than unstructured web pages, fundamentally shaping their architectures (Wang & Na, 2023; Ren et al., 2024). The dominant approach employs embedding-based retrieval using the bi-encoder architecture combined with approximate nearest neighbor search (Nigam et al., 2019; Lin et al., 2024).

**中文**

电子商务搜索。电子商务搜索系统在结构化产品目录而不是非结构化网页上运行，从根本上塑造了其架构（Wang & Na，2023；Ren 等人，2024）。主要方法采用基于嵌入的检索，使用双编码器架构与近似最近邻搜索相结合（Nigam 等人，2019；Lin 等人，2024）。

### 段落 221 · Page 28

**EN**

These systems must address severe vocabulary mismatch between customer queries and product descriptions, motivating query rewriting and semantic bridging components, often implemented using LLMs trained with contrastive or instruction-based objectives (Peng et al., 2024b). Ads Ranking.Ads ranking is another important industrial IR application scenario. Modern advertising recommendation systems face the fundamental challenge of processing massive candidate sets while maintaining strict latency requirements and ranking quality.

**中文**

这些系统必须解决客户查询和产品描述之间严重的词汇不匹配问题，激发查询重写和语义桥接组件，通常使用经过对比或基于指令的目标训练的法学硕士来实现（Peng 等人，2024b）。广告排名。广告排名是IR另一个重要的行业应用场景。现代广告推荐系统面临着处理大量候选集同时保持严格的延迟要求和排名质量的根本挑战。

### 段落 222 · Page 28

**EN**

The traditional approach employs multi-stage cascading architectures that decompose the Ad ranking problem into sequential stages: retrieval, pre-ranking (or lightweight ranking), ranking (or heavyweight ranking), and auction (Gallagher et al., 2019; Wang et al., 2023b; Zheng et al., 2024a; Yang et al., 2025d), where the research focus is similar to that of ad hoc retrieval. 28

**中文**

传统方法采用多阶段级联架构，将广告排名问题分解为连续阶段：检索、预排名（或轻量级排名）、排名（或重量级排名）和拍卖（Gallagher等，2019；Wang等，2023b；Zheng等，2024a；Yang等，2025d），其研究重点与即席检索类似。 28

### Page 29

### 段落 223 · Page 29

**EN**

Published in Transactions on Machine Learning Research (02/2026) In the context of Ads ranking, the XMC formulation described in Section 5 has been shown to improve ranking quality of tail items/Ads (Jain et al., 2019; Dahiya et al., 2021; Yu et al., 2022a; Dahiya et al., 2023; Gupta et al., 2024b), which is often critical for revenue maximization. However, it also comes with higher engineering complexity and often requires retraining of the models when new items/Ads are added.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 在广告排名的背景下，第 5 节中描述的 XMC 公式已被证明可以提高尾部项目/广告的排名质量（Jain 等人，2019；Dahiya 等人，2021；Yu 等人，2022a；Dahiya 等人，2023；Gupta 等人，2024b），这是通常对于收入最大化至关重要。然而，它也具有更高的工程复杂性，并且在添加新项目/广告时通常需要重新训练模型。

### 段落 224 · Page 29

**EN**

The recent breakthrough of LLMs has catalyzed a paradigm shift toward generative recommendation frameworks that can directly generate personalized item sequences from user interaction histories. These approaches index items with meaningful IDs using vector quantization algorithms and generate items from the entire item set for recommendation, conceptualizing online advertising systems as a unified generative process that eliminates inherent goal conflicts between different pipeline stages (Rajput et al., 2023; Zheng et al., 2023; Zhai et al., 2024).

**中文**

法学硕士最近的突破促进了向生成推荐框架的范式转变，该框架可以直接从用户交互历史中生成个性化项目序列。这些方法使用矢量量化算法对具有有意义 ID 的项目进行索引，并从整个项目集中生成项目进行推荐，将在线广告系统概念化为统一的生成过程，消除不同管道阶段之间固有的目标冲突（Rajput 等人，2023 年；Zheng 等人，2023 年；Zhai 等人，2024 年）。

### 段落 225 · Page 29

**EN**

Given space constraints, we refer readers to the cited works for a more in-depth treatment of the field. Cross-Application IR.Across applications, several architectural trends are reshaping IR system design. Retrieval-augmented generation (RAG) architectures combine dense vector search with LLMs to support search, reasoning, and synthesis over structured and unstructured data (Asai et al., 2024c). Modular and multi-agent retrieval frameworks further decouple retrieval functions into interoperable components, enabling dynamic adaptation to application-specific requirements (Chang et al., 2025; Zhang et al., 2025a).

**中文**

鉴于篇幅限制，我们建议读者参考引用的著作，以便更深入地探讨该领域。跨应用 IR。跨应用，多种架构趋势正在重塑 IR 系统设计。检索增强生成 (RAG) 架构将密集向量搜索与 LLM 相结合，以支持结构化和非结构化数据的搜索、推理和综合（Asai 等人，2024c）。模块化和多代理检索框架进一步将检索功能解耦为可互操作的组件，从而能够动态适应特定于应用程序的需求（Chang 等人，2025；Zhang 等人，2025a）。

### 段落 226 · Page 29

**EN**

Finally, contextual personalization and the convergence of search and recommendation architectures reflect a broader shift toward unified representations of users, documents, and intent (Zamani & Croft, 2018). Taken together, the diversity of application-driven architectures underscores that modern IR systems are no longer optimized solely for static relevance ranking, but must increasingly adapt to new roles, constraints, and integration patterns that give rise to emerging architectural directions and open challenges.

**中文**

最后，上下文个性化以及搜索和推荐架构的融合反映了向用户、文档和意图的统一表示的更广泛转变（Zamani & Croft，2018）。总而言之，应用程序驱动架构的多样性强调了现代 IR 系统不再仅仅针对静态相关性排名进行优化，而是必须不断适应新的角色、约束和集成模式，从而产生新兴的架构方向和开放挑战。

### 段落 227 · Page 29

**EN**

9 Emerging Directions and Challenges IR systems have become crucial across diverse domains, from retrieval-augmented language modeling (Khandelwal et al., 2020; Borgeaud et al., 2022) to applications in agents (Wu et al., 2023a; Wang et al., 2024a; 2025a), code generation (Wang et al., 2025b; Zhang et al., 2023a), robotics (Anwar et al., 2024), medicine (Jeong et al., 2024), and protein research (Jumper et al., 2021),inter alia. These developments present new challenges for IR research. Drawing from the evolution of IR architectures (Sections 3 to 8), we examine emerging trends, open problems, and potential research directions.

**中文**

9 新兴方向和挑战 IR 系统在不同领域已变得至关重要，从检索增强语言模型（Khandelwal 等人，2020；Borgeaud 等人，2022）到代理应用（Wu 等人，2023a；Wang 等人，2024a；2025a）、代码生成（Wang 等人，2025b；Zhang 等人， 2023a）、机器人技术（Anwar 等人，2024）、医学（Jeong 等人，2024）和蛋白质研究（Jumper 等人，2021）等。这些发展给红外研究带来了新的挑战。根据 IR 架构的演变（第 3 节到第 8 节），我们研究了新兴趋势、开放问题和潜在的研究方向。

### 段落 228 · Page 29

**EN**

Our discussion is structured around three key areas: advancing the core components of IR models, adapting to the new paradigm of retrieval for AI, and tackling the pragmatic challenges of real-world deployment. 9.1 Advancing the Core Components of IR Models At the heart of any IR system are the models that extract features and estimate relevance. As IR moves toward more compute-intensive practices, we identify key areas for improving these fundamental components.

**中文**

我们的讨论围绕三个关键领域：推进 IR 模型的核心组件、适应人工智能检索的新范式以及解决现实世界部署的务实挑战。 9.1 推进 IR 模型的核心组件 任何 IR 系统的核心都是提取特征和估计相关性的模型。随着 IR 走向计算密集型实践，我们确定了改进这些基本组件的关键领域。

### 段落 229 · Page 29

**EN**

More Powerful and Efficient Foundation Models.Scaling has been a winning recipe for modern neural networks (Kaplan et al., 2020; Hoffmann et al., 2022; Dehghani et al., 2023; Fang et al., 2024; Shao et al., 2024,inter alia). However, for IR to leverage this trend sustainably, several challenges in model design and training must be addressed: •Data and training efficiency.Current transformer-based IR models demand extensive training data (Fang et al., 2024), making them impractical for many real-world applications. Developing architectures that can learn effectively from limited data or in a few-shot/zero-shot setting remains crucial.

**中文**

更强大、更高效的基础模型。扩展一直是现代神经网络的致胜秘诀（Kaplan 等人，2020；Hoffmann 等人，2022；Dehghani 等人，2023；Fang 等人，2024；Shao 等人，2024，等等）。然而，为了可持续地利用这一趋势，IR 必须解决模型设计和训练中的几个挑战： • 数据和训练效率。当前基于Transformer的 IR 模型需要大量的训练数据（Fang 等人，2024），这使得它们对于许多实际应用来说不切实际。开发能够从有限数据或在少数样本/零样本设置中有效学习的架构仍然至关重要。

### 段落 230 · Page 29

**EN**

Additionally, models should support parallel processing and low-precision training to reduce costs and accelerate convergence (Pool et al., 2021; Fishman et al., 2024; Liu et al., 2024a). •Inference optimization.Real-time applications like conversational search (Mo et al., 2024b) and agent-based systems (Yao et al., 2023) require efficient handling of variable-length queries, necessitating advanced compression and optimization techniques for both retriever backbones and 29

**中文**

此外，模型应支持并行处理和低精度训练，以降低成本并加速收敛（Pool et al., 2021；Fishman et al., 2024；Liu et al., 2024a）。 •推理优化。诸如会话搜索（Mo 等人，2024b）和基于代理的系统（Yao 等人，2023）等实时应用程序需要有效处理可变长度查询，因此需要针对检索器主干和 29 进行高级压缩和优化技术。

### Page 30

### 段落 231 · Page 30

**EN**

Published in Transactions on Machine Learning Research (02/2026) index structures (Dettmers & Zettlemoyer, 2023; Kumar et al., 2024; Xu et al., 2024b; Warner et al., 2025; Bruch et al., 2024; Xu et al., 2025b,inter alia). •Better lite foundation models.IR models need to process queries in real time, and using compact-sized foundation models is often a practical solution. Warner et al. (2025) presented an interesting study on wide-and-shallow versus deep-and-narrow architecture in the context of training a “modern”BERTmodel.

**中文**

发表于机器学习研究交易 (02/2026) 索引结构（Dettmers & Zettlemoyer，2023；Kumar 等人，2024；Xu 等人，2024b；Warner 等人，2025；Bruch 等人，2024；Xu 等人，2025b，等等）。 •更好的精简基础模型。IR 模型需要实时处理查询，使用紧凑型基础模型通常是一个实用的解决方案。华纳等人。 (2025) 在训练“现代”BERT 模型的背景下，提出了一项关于宽浅架构与深窄架构的有趣研究。

### 段落 232 · Page 30

**EN**

Recent works (Günther et al., 2024; Fu et al., 2023; Portes et al., 2023) studied training efficientBERTmodel that supports longer context length, while Nussbaum & Duderstadt (2025) investigated the efficacy of a mixture-of-expertBERT-style encoder model. The best recipe for lite foundational models for IR applications remains an open question. •Transformer alternatives.While transformers havedominated recent IRresearch, their quadratic complexity in attention computation remains a significant bottleneck.

**中文**

最近的工作（Günther 等人，2024；Fu 等人，2023；Portes 等人，2023）研究了训练支持更长上下文长度的高效 BERT 模型，而 Nussbaum 和 Duderstadt（2025）研究了混合专家 BERT 风格编码器模型的功效。红外应用的精简基础模型的最佳配方仍然是一个悬而未决的问题。 • Transformer 替代方案。虽然 Transformer 主导了最近的 IR 研究，但它们在注意力计算中的二次复杂度仍然是一个重大瓶颈。

### 段落 233 · Page 30

**EN**

Recent advances in linear RNNs (Peng et al., 2023; 2024a; Qin et al., 2024c), state space models (Gu & Dao, 2024; Dao & Gu, 2024), and linear attention (Katharopoulos et al., 2020; Yang et al., 2025c) offer alternatives with theoretical linear complexity. Although preliminary studies (Xu, 2024; Zhang et al., 2024; Xu et al., 2025e;c) show limited gains compared to optimized transformers, developing efficient alternative architectures for transformers could revolutionize large-scale IR. Ultimately, strong foundation models have proven crucial for IR performance (Neelakantan et al., 2022; Ma et al., 2024b,inter alia).

**中文**

线性 RNN（Peng 等人，2023；2024a；Qin 等人，2024c）、状态空间模型（Gu & Dao，2024；Dao & Gu，2024）和线性注意力（Katharopoulos 等人，2020；Yang 等人，2025c）的最新进展提供了具有理论线性复杂性的替代方案。尽管初步研究（Xu，2024；Zhang 等人，2024；Xu 等人，2025e；c）显示与优化Transformer相比增益有限，但开发高效的Transformer替代架构可能会彻底改变大规模 IR。最终，事实证明，强大的基础模型对于 IR 性能至关重要（Neelakantan 等人，2022 年；Ma 等人，2024b 等）。

### 段落 234 · Page 30

**EN**

As IR applications expand, developing foundation models that balance computational efficiency with robust performance across tasks and modalities emerges as a key research priority. Flexible and Scalable Relevance Estimators.As discussed in Section 6, cross-encoders provide complex non-linear relevance estimation but are computationally expensive. In contrast, bi-encoder architectures used in dense and sparse retrieval rely on linear similarity functions (e.g., inner product) to enable fast retrieval through nearest neighbor search and inverted indexing.

**中文**

随着 IR 应用的扩展，开发平衡计算效率与跨任务和模式的稳健性能的基础模型成为一个关键的研究优先事项。灵活且可扩展的相关性估计器。如第 6 节中所讨论的，交叉编码器提供复杂的非线性相关性估计，但计算成本较高。相比之下，密集和稀疏检索中使用的双编码器架构依赖于线性相似函数（例如内积）来通过最近邻搜索和倒排索引实现快速检索。

### 段落 235 · Page 30

**EN**

Balancing complex relevance matching and scalable retrieval remains challenging.ColBERT(Khattab & Zaharia, 2020) addresses this by using document representation matrices with MaxSim operations, while recent work (Killingback et al., 2025) explores Hypernetworks (Ha et al., 2022) to generate query-specific neural networks for relevance estimation. The design of flexible yet scalable relevance estimators remains an active research direction. 9.2 The Shifting Paradigm: From Search for Humans to Retrieval for AI The integration of IR systems into other research domains presents new challenges.

**中文**

平衡复杂的相关性匹配和可扩展检索仍然具有挑战性。ColBERT（Khattab & Zaharia，2020）通过使用带有 MaxSim 操作的文档表示矩阵解决了这个问题，而最近的工作（Killingback 等人，2025）探索了超网络（Ha 等人，2022）来生成查询特定的神经网络以进行相关性估计。灵活且可扩展的相关性估计器的设计仍然是一个活跃的研究方向。 9.2 范式的转变：从人类搜索到人工智能检索 将红外系统集成到其他研究领域提出了新的挑战。

### 段落 236 · Page 30

**EN**

We discuss key implications for future IR modeling research as the primary “user” of retrieval shifts from humans to AI models. The End “User” of Retrieval.While traditional IR systems focus on providing search results to humans, retrieval is increasingly used to support ML models, particularly LLMs, in tasks such as generation (Gao et al., 2023), reasoning (Yao et al., 2024; Islam et al., 2024), tool usage (Schick et al., 2023; Patil et al., 2024b; Qin et al., 2024a; Patil et al., 2024a) and planning (Song et al., 2023).

**中文**

随着检索的主要“用户”从人类转向人工智能模型，我们讨论了对未来 IR 建模研究的关键影响。检索的最终“用户”。虽然传统的 IR 系统专注于向人类提供搜索结果，但检索越来越多地用于支持 ML 模型，特别是 LLM，例如生成（Gao 等人，2023）、推理（Yao 等人，2024；Islam 等人，2024）、工具使用（Schick 等人，2023；Patil 等人，2024b；Qin 等人）等任务等人，2024a；Patil 等人，2024a）和规划（Song 等人，2023）。

### 段落 237 · Page 30

**EN**

This shifting paradigm raises fundamental questions about task formulation, evaluation, and system optimization: •Current IR research is grounded in human information-seeking behavior (Wilson, 2000; Marchionini, 2006; White & Roth, 2009,inter alia). When the end user becomes another ML model, we must reconsider how to define and assessrelevance. For example, a document might be irrelevant to a human but contain a key factual nugget that an LLM needs to answer a question. This suggests a need for flexible, data-efficient models that are adaptable to various downstream tasks.

**中文**

这种范式的转变提出了有关任务制定、评估和系统优化的基本问题： • 当前的信息检索研究以人类信息寻求行为为基础（Wilson，2000；Marchionini，2006；White & Roth，2009，等等）。当最终用户成为另一个机器学习模型时，我们必须重新考虑如何定义和评估相关性。例如，一份文档可能与人类无关，但包含法学硕士回答问题所需的关键事实信息。这表明需要灵活、数据高效的模型，以适应各种下游任务。

### 段落 238 · Page 30

**EN**

•Traditional IR metrics, which are designed for human-centric evaluation, may not align with downstream task performance in retrieval-augmented systems (Lewis et al., 2020b; Petroni et al., 2021; Asai et al., 2024c). Future IR models should support end-to-end system optimization rather than focusing solely on ranking metrics (OpenAI, 2025; Huang et al., 2025). 30

**中文**

•传统的IR指标是为以人为中心的评估而设计的，可能与检索增强系统中的下游任务绩效不一致（Lewis等人，2020b；Petroni等人，2021；Asai等人，2024c）。未来的 IR 模型应该支持端到端系统优化，而不是仅仅关注排名指标（OpenAI，2025；Huang 等人，2025）。 30

### Page 31

### 段落 239 · Page 31

**EN**

Published in Transactions on Machine Learning Research (02/2026) Retrieval Augmented Generation.Retrieval Augmented Generation (RAG) refers to architectures that combine an external retrieval module with a generative model, enabling the system to access and condition on external knowledge before producing output.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 检索增强生成。检索增强生成 (RAG) 是指将外部检索模块与生成模型相结合的架构，使系统能够在生成输出之前访问和调节外部知识。

### 段落 240 · Page 31

**EN**

Early RAG formulations separate retrieval and generation as distinct components: a dense or sparse retriever extracts relevant passages for a given input, and a generator (usually an LLM) conditions on those retrieved results to produce text (Lewis et al., 2020b; Ram et al., 2023b; Mallen et al., 2023; Asai et al., 2024c; Chen et al., 2020b; Xu & Cohen, 2023). This architectural decoupling allows retrieval to be optimized independently from generation, which is useful for modularity and scalability.

**中文**

早期的 RAG 公式将检索和生成作为不同的组件分开：密集或稀疏检索器提取给定输入的相关段落，生成器（通常是法学硕士）根据检索结果生成文本（Lewis 等人，2020b；Ram 等人，2023b；Mallen 等人，2023；Asai 等人，2024c；Chen 等人，2020b；Xu 等人）科恩，2023）。这种架构解耦允许独立于生成来优化检索，这对于模块化和可扩展性非常有用。

### 段落 241 · Page 31

**EN**

A typical RAG pipeline comprises: •Corpus embedding and indexing (vector stores or sparse indexes) for fast retrieval; •Retriever model (dense vectors or hybrid techniques) that returns top-krelevant items; •Fusion mechanism that combines retrieved content with the query (e.g., concatenation or crossattention) before passing it to the generator; •Generator that produces the final answer based on fused context. This simple architecture improves factual accuracy and reduces hallucination by grounding generation on external context.

**中文**

典型的 RAG 管道包括： 用于快速检索的语料库嵌入和索引（向量存储或稀疏索引）； •返回最相关项目的检索器模型（密集向量或混合技术）； •融合机制，在将检索到的内容传递给生成器之前将其与查询相结合（例如串联或交叉注意）； •根据融合上下文生成最终答案的生成器。这种简单的架构通过将生成基于外部环境来提高事实准确性并减少幻觉。

### 段落 242 · Page 31

**EN**

However, it also introduces key engineering and modeling considerations: •Retriever-Generator Coupling: The architectural choice of where and how to combine retrieval results can affect quality and efficiency. Early approaches rely on simple concatenation of text passages into the generator’s context window (Lewis et al., 2020b; Ram et al., 2023b), which do not alter the architecture of the generator. More advanced designs use cross-attention layers or rerankers to improve precision (Izacard & Grave, 2021; Park et al., 2023; An et al., 2025b).

**中文**

然而，它还引入了关键的工程和建模注意事项： • 检索器-生成器耦合：组合检索结果的位置和方式的架构选择会影响质量和效率。早期的方法依赖于将文本段落简单串联到生成器的上下文窗口中（Lewis 等人，2020b；Ram 等人，2023b），这不会改变生成器的架构。更先进的设计使用交叉注意力层或重新排序器来提高精度（Izacard & Grave，2021；Park 等人，2023；An 等人，2025b）。

### 段落 243 · Page 31

**EN**

•Multi-Modal and Structured Retrieval: Recent work explores RAG variants that extend beyond plain text. For example, GraphRAG and related graph-enhanced frameworks integrate structured knowledge sources, enabling retrieval of relational paths not easily captured by vector similarity alone (Edge et al., 2025; Li et al., 2025a). These architectures introduce additional components like graph encoders and reasoning layers, allowing the system to extract multi-hop or entity-centric context before generation.

**中文**

•多模式和结构化检索：最近的工作探索了超越纯文本的RAG 变体。例如，GraphRAG 和相关的图增强框架集成了结构化知识源，能够检索仅通过向量相似性难以捕获的关系路径（Edge 等人，2025；Li 等人，2025a）。这些架构引入了图形编码器和推理层等附加组件，允许系统在生成之前提取多跳或以实体为中心的上下文。

### 段落 244 · Page 31

**EN**

•Adaptive Retrieval: Newer RAG pipelines incorporate reasoning capabilities into the generator, to dynamically decide whether to retrieval or to generate answer (Trivedi et al., 2023; Jiang et al., 2023b; Asai et al., 2024b). These architectural choices have direct implications: strong retrieval can reduce generation errors but may increase pipeline complexity and latency; graph-aware models can support structured reasoning at the cost of larger indexes and additional components; adaptive retrieval strategies can improve effectiveness but require careful task planning and retrieval coordination.

**中文**

自适应检索：较新的 RAG 管道将推理功能合并到生成器中，以动态决定是检索还是生成答案（Trivedi 等人，2023；Jiang 等人，2023b；Asai 等人，2024b）。这些架构选择具有直接影响：强大的检索可以减少生成错误，但可能会增加管道复杂性和延迟；图感知模型可以支持结构化推理，但需要更大的索引和额外的组件；自适应检索策略可以提高效率，但需要仔细的任务规划和检索协调。

### 段落 245 · Page 31

**EN**

Overall, RAG architectures represent a spectrum from simple retrieval-plus-generation pipelines to complex multi-component systems that integrate heterogeneous knowledge representations and adaptive retrieval planning to improve both relevance and reasoning capability. We refer readers to (Gao et al., 2023; Li et al., 2025e; Mei et al., 2025) for more comprehensive reviews of this topic.

**中文**

总体而言，RAG 架构代表了从简单的检索加生成管道到复杂的多组件系统的范围，这些系统集成了异构知识表示和自适应检索规划以提高相关性和推理能力。我们建议读者参考（Gao et al., 2023; Li et al., 2025e; Mei et al., 2025），以获取对此主题的更全面的评论。

### 段落 246 · Page 31

**EN**

The Rise of Autonomous Search Agents.Complex tasks often require retrieving long-tail knowledge using lengthy, complex queries (Soudani et al., 2024; Su et al., 2024), demanding retrieval models capable of instruction following (Weller et al., 2025a; Ravfogel et al., 2024) and reasoning (Su et al., 2024; Shao et al., 2025; Liang et al., 2025). This has spurred the development of autonomous search agents. Existing attempts can be divided into two main directions. One line of work focuses on training more capable retrievers and rerankers.

**中文**

自主搜索代理的兴起。复杂的任务通常需要使用冗长、复杂的查询来检索长尾知识 (Soudani et al., 2024; Su et al., 2024)，要求检索模型能够遵循指令 (Weller et al., 2025a; Ravfogel et al., 2024) 和推理 (Su et al., 2024; Shao et al., 2025;梁等人，2025）。这刺激了自主搜索代理的发展。现有的尝试可以分为两个主要方向。其中一项工作重点是训练更有能力的检索器和重新排序器。

### 段落 247 · Page 31

**EN**

This involves creating new data pipelines to synthesize instruction-following and reasoningfocused training data (Oh et al., 2024; Weller et al., 2024; Shao et al., 2025,inter alia) and leveraging 31

**中文**

这涉及创建新的数据管道来合成指令跟踪和推理为重点的训练数据（Oh et al., 2024; Weller et al., 2024; Shao et al., 2025等）并利用 31

### Page 32

### 段落 248 · Page 32

**EN**

Published in Transactions on Machine Learning Research (02/2026) strong backbone language models such as the proprietary GPT-4 family models (OpenAI et al., 2023) and open-weightQwen(Yang et al., 2025a) to imbue the retriever with reasoning capabilities. Another line of work treats the search/retrieval system as a static tool and focuses on improving a large reasoning model’s (LRM) ability to use the retrieval tool to improve reasoning and handle in-context memory (Jin et al., 2025; Yu et al., 2025; Gao et al., 2025; Xu et al., 2025d,inter alia).

**中文**

发表于《机器学习研究汇刊》(02/2026) 强大的骨干语言模型，例如专有的 GPT-4 系列模型 (OpenAI et al., 2023) 和 open-weightQwen (Yang et al., 2025a)，为检索器赋予推理能力。另一项工作将搜索/检索系统视为静态工具，并专注于提高大型推理模型（LRM）使用检索工具来改进推理和处理上下文记忆的能力（Jin 等人，2025；Yu 等人，2025；Gao 等人，2025；Xu 等人，2025d 等）。

### 段落 249 · Page 32

**EN**

In this setup, the LRM decides when, where, and how to conduct a search, and the results subsequently influence its further reasoning and decision-making (Nakano et al., 2021; He et al., 2025). This line of work, commonly referred to asDeep Research Agents, represents a paradigm shift fromretrieval as the end goaltoretrieval as tools for LLMs. Formally, we use the definition from Huang et al. (2025): deep research agents refer to AI agents powered by LLMs, integrating dynamic reasoning, adaptive planning, multi-iteration external data retrieval and tool use, and comprehensive analytical report generation for informational research tasks.

**中文**

在这种设置中，LRM 决定何时、何地以及如何进行搜索，结果随后影响其进一步的推理和决策（Nakano et al., 2021；He et al., 2025）。这一系列工作通常被称为深度研究代理，代表了从作为最终目标的检索到作为法学硕士工具的检索的范式转变。正式地，我们使用 Huang 等人的定义。 (2025)：深度研究代理是指由法学硕士支持的人工智能代理，集成了动态推理、自适应规划、多次迭代外部数据检索和工具使用以及信息研究任务的综合分析报告生成。

### 段落 250 · Page 32

**EN**

From the retrieval perspective, the retrieval usage of deep research agents can be broadly categorized into two types: (1) API-based search engines which interact with structured data sources, such as search engine APIs or scientific database APIs; (2) browser-based search engines, which simulate human-like interactions with web pages and enable real-time extraction of dynamic or unstructured content leveraging LLMs’ longcontext, code understanding and multimodality capabilities. Both formulations have strengths and weaknesses.

**中文**

从检索的角度来看，深度研究代理的检索使用大致可分为两类：（1）基于API的搜索引擎，与结构化数据源交互，例如搜索引擎API或科学数据库API； (2) 基于浏览器的搜索引擎，它模拟人类与网页的交互，并利用法学硕士的长上下文、代码理解和多模态功能，实时提取动态或非结构化内容。两种配方都有优点和缺点。

### 段落 251 · Page 32

**EN**

API-based retrieval, in line with traditional IR literature, is a fast, efficient, structured and scalable method to enable deep research agents’ access to external knowledge (Schütze et al., 2008; Singh et al., 2025b). Browser-based retrieval (Nakano et al., 2021; OpenAI, 2025) offers the advantage of simulating real-time, interactive information-seeking behavior— conceptually similar to that of human users. However, it incurs additional latency and token consumption, and introduces further complexity arising from the web-browsing environment.

**中文**

基于 API 的检索与传统的 IR 文献一致，是一种快速、高效、结构化和可扩展的方法，使深度研究代理能够访问外部知识（Schütze 等人，2008；Singh 等人，2025b）。基于浏览器的检索（Nakano et al., 2021；OpenAI, 2025）提供了模拟实时、交互式信息查找行为的优势——概念上与人类用户类似。然而，它会带来额外的延迟和令牌消耗，并引入网络浏览环境带来的进一步复杂性。

### 段落 252 · Page 32

**EN**

Given the current landscape of retrieval integration within deep research agents, a central open question is how to design a hybrid retrieval architecture that combines the strengths of both paradigms to achieve a superior performance-efficiency tradeoff. From the model training perspective, recent efforts have abstracted away the details of retrieval models, treating retrieval as static tools and instead focusing on improving the capabilities of LLM-based search agents.

**中文**

考虑到当前深度研究代理内部检索集成的情况，一个核心的开放问题是如何设计一种混合检索架构，结合两种范式的优势，以实现卓越的性能与效率权衡。从模型训练的角度来看，最近的努力抽象了检索模型的细节，将检索视为静态工具，而是专注于提高基于 LLM 的搜索代理的能力。

### 段落 253 · Page 32

**EN**

For example, many recent efforts aim to train LRMs to use search tools more effectively via reinforcement learning or specialized fine-tuning (Li et al., 2025b; Jin et al., 2025; Li et al., 2025c; Chen et al., 2025; Wu et al., 2025b;a,inter alia). This approach is central to agentic frameworks that orchestrate tool use for complex task completion (Wu et al., 2023a; Shinn et al., 2023; Asai et al., 2024b). Despite this exciting progress, key limitations remain. To enable retrievers’ reasoning capability often requires strong backbone models (e.g., 7B scale), which can be infeasible for production systems.

**中文**

例如，最近的许多努力旨在通过强化学习或专门的微调来训练LRM更有效地使用搜索工具（Li等人，2025b；Jin等人，2025；Li等人，2025c；Chen等人，2025；Wu等人，2025b；a等）。这种方法是协调工具使用以完成复杂任务的代理框架的核心（Wu 等人，2023a；Shinn 等人，2023；Asai 等人，2024b）。尽管取得了这些令人兴奋的进展，但关键的局限性仍然存在。为了实现检索器的推理能力，通常需要强大的骨干模型（例如 7B 规模），这对于生产系统来说是不可行的。

### 段落 254 · Page 32

**EN**

Even larger models (e.g., 32B scale) augmented with retrieval and trained via expensive reinforcement learning (Jin et al., 2025; Chen et al., 2025) still sometimes underperform simpler baselines with query decomposition and chain-of-thought prompting (Khot et al., 2023; Trivedi et al., 2023). A key open question is how to endow retrievers with strong reasoning capabilities using lightweight, scalable models. Another challenge lies in the joint optimization of retrievers and language models within a unified, reasoning-aware framework. Lastly, the human factors of applying such autonomous search agents remain to be studied.

**中文**

即使是更大的模型（例如 32B 规模）通过检索增强并通过昂贵的强化学习进行训练（Jin 等人，2025 年；Chen 等人，2025 年）有时仍然不如具有查询分解和思想链提示的简单基线（Khot 等人，2023 年；Trivedi 等人，2023 年）。一个关键的悬而未决的问题是如何使用轻量级、可扩展的模型赋予检索器强大的推理能力。另一个挑战在于在统一的推理感知框架内联合优化检索器和语言模型。最后，应用这种自主搜索代理的人为因素仍有待研究。

### 段落 255 · Page 32

**EN**

We refer readers to (Singh et al., 2025a; Liang et al., 2025; Xi et al., 2025; Lin et al., 2025) for more comprehensive reviews of this topic. 9.3 Retrieval Beyond Simple Relevance: Instruction-Following and Reasoning-Aware Retrieval Instruction-Following Retrieval.Instruction-following retrieval extends the standard query-document formulation by conditioning the retriever on a natural-language instruction.

**中文**

我们建议读者参考（Singh et al., 2025a；Liang et al., 2025；Xi et al., 2025；Lin et al., 2025），以获得对此主题更全面的评论。 9.3 超越简单相关性的检索：指令跟随和推理感知检索 指令跟随检索。指令跟随检索通过在自然语言指令上调节检索器来扩展标准查询文档表述。

### 段落 256 · Page 32

**EN**

Architecturally, this is typically implemented by jointly encoding the instruction and the query in a shared bi-encoder, for example through simple concatenation or lightweight attention layers, so that the query representation adapts to task intent (Weller et al., 2025a; Oh et al., 2024). Training objectives often use contrastive learning with instruction-conditioned positives and hard negatives, allowing the model to capture fine-grained task semantics without large cross-encoder computations (Weller et al., 2024).

**中文**

从架构上讲，这通常是通过在共享双编码器中联合编码指令和查询来实现的，例如通过简单的串联或轻量级关注层，以便查询表示适应任务意图（Weller 等人，2025a；Oh 等人，2024）。训练目标通常使用具有指令条件的正值和硬负值的对比学习，使模型能够捕获细粒度的任务语义，而无需进行大量的跨编码器计算（Weller 等人，2024）。

### 段落 257 · Page 32

**EN**

Instruction-aware retrievers benefit from curated or synthetic datasets pairing instructions, queries, and relevant passages, which improves robustness to paraphrasing and query phrasing variations. These design choices preserve scalability while improving performance on instruction-heavy tasks. Hybrid pipelines may further combine instruction-conditioned re- 32

**中文**

指令感知检索器受益于配对指令、查询和相关段落的策划或合成数据集，这提高了释义和查询短语变化的稳健性。这些设计选择保留了可扩展性，同时提高了指令密集型任务的性能。混合流水线可以进一步结合指令条件重构 32

### Page 33

### 段落 258 · Page 33

**EN**

Published in Transactions on Machine Learning Research (02/2026) trieval with downstream rerankers or fusion mechanisms, ensuring that retrieved evidence aligns with the specific needs of generation or reasoning tasks (Shao et al., 2024; Weller et al., 2025b). Reasoning-Aware Retrieval.Reasoning-aware retrieval aims to retrieve evidence that supports multistep inference and complex reasoning (Su et al., 2024). One line of work usesgraph-based architectures, where the retriever constructs and encodes relational graphs or multi-hop chains of passages.

**中文**

发表在机器学习研究交易 (02/2026) 中，使用下游重新排序器或融合机制进行 trieval，确保检索到的证据符合生成或推理任务的特定需求（Shao 等人，2024 年；Weller 等人，2025b）。推理感知检索。推理感知检索旨在检索支持多步推理和复杂推理的证据（Su et al., 2024）。其中一项工作使用基于图的架构，其中检索器构建并编码关系图或多跳段落链。

### 段落 259 · Page 33

**EN**

These components—graph construction, encoding, path selection, and ranking—allow the retriever to return connected evidence that reflects reasoning dependencies (Liu et al., 2025a; Edge et al., 2025). While effective for compositional queries, these approaches increase system complexity, latency, and index size. A different line of work, exemplified byReasonIR(Shao et al., 2025) andRankR1(Zhuang et al., 2025), improves reasoning capability throughdata curation and task-aligned trainingrather than altering the underlying “retrieve-then-rerank” pipeline.

**中文**

这些组件（图构建、编码、路径选择和排序）允许检索器返回反映推理依赖关系的关联证据（Liu 等人，2025a；Edge 等人，2025）。虽然这些方法对于组合查询有效，但会增加系统复杂性、延迟和索引大小。以 ReasonIR（Shao 等人，2025）和 RankR1（Zhuang 等人，2025）为代表的不同工作线通过数据管理和任务对齐训练来提高推理能力，而不是改变底层的“检索然后重新排序”管道。

### 段落 260 · Page 33

**EN**

By generating multi-step reasoning datasets or instruction-guided examples, thesemethodsteachstandardretrieversandrerankerstoprioritizeevidencethatisusefulfordownstream reasoning, achieving stronger performance without introducing graph-based components. From an evaluation perspective, reasoning-aware retrieval highlights the need for task-centered metrics that measure downstream reasoning success, emphasizing the tight connection between architectural or training choices and reasoning effectiveness.

**中文**

通过生成多步骤推理数据集或指令引导的示例，这些方法可以教授标准检索器并重新排序对下游推理有用的证据，从而在不引入基于图形的组件的情况下实现更强的性能。从评估的角度来看，推理感知检索强调需要以任务为中心的指标来衡量下游推理的成功，强调架构或培训选择与推理有效性之间的紧密联系。

### 段落 261 · Page 33

**EN**

9.4 Deployment, Robustness, and Trustworthiness As modern IR systems become more powerful and integrated into high-stakes applications, ensuring their practical deployability and reliability is paramount. The Efficiency-Effectiveness Tradeoff at Scale.Traditional retrieval systems face significant challenges when scaling to web-scale document corpus, and deploying such systems requires a blend of science and engineering expertise (Dean, 2009; Huang et al., 2020; Li et al., 2021).

**中文**

9.4 部署、稳健性和可信性 随着现代 IR 系统变得更加强大并集成到高风险应用中，确保其实际的可部署性和可靠性至关重要。大规模的效率与效果权衡。传统检索系统在扩展到网络规模的文档语料库时面临着重大挑战，并且部署此类系统需要结合科学和工程专业知识（Dean，2009；Huang 等人，2020；Li 等人，2021）。

### 段落 262 · Page 33

**EN**

In recent years, retrieval-augmented generation, conversational search, and agentic systems with memory have been widely adopted for information access (Guu et al., 2020; Lewis et al., 2020b; Nayak, 2019; OpenAI, 2024; Google, 2024,inter alia). These applications often require multiple rounds of retrieval and operate on dynamic corpuses, urging for efficient and effective retrieval. Mainstream inference optimization frameworks such as vLLM (Kwon et al., 2023) and SGLang (Zheng et al., 2024b) have provided support for embedding models.

**中文**

近年来，检索增强生成、会话搜索和具有记忆的代理系统已被广泛用于信息访问（Guu et al., 2020; Lewis et al., 2020b; Nayak, 2019; OpenAI, 2024; Google, 2024等）。这些应用往往需要多轮检索并在动态语料库上进行操作，迫切需要高效、有效的检索。 vLLM (Kwon et al., 2023) 和 SGLang (Zheng et al., 2024b) 等主流推理优化框架都为嵌入模型提供了支持。

### 段落 263 · Page 33

**EN**

From the modeling perspective, an open question is to design and pre-train models explicitly for retrieval purposes (Warner et al., 2025; Nussbaum et al., 2025; Günther et al., 2024). Ensuring Robustness in a Noisy and Adversarial World.We discuss a few challenges in IR models’ deployment in noisy environments, especially when used in retrieval-augmented generation systems. We should note that while these challenges have been studied by prior works, it remains an open question on how to mitigate these challenges from the perspective of IR modeling and architectures.

**中文**

从建模的角度来看，一个悬而未决的问题是为了检索目的而明确设计和预训练模型（Warner et al., 2025；Nussbaum et al., 2025；Günther et al., 2024）。确保噪声和对抗性世界中的鲁棒性。我们讨论了 IR 模型在噪声环境中部署的一些挑战，特别是在检索增强生成系统中使用时。我们应该注意到，虽然之前的工作已经研究了这些挑战，但如何从 IR 建模和架构的角度缓解这些挑战仍然是一个悬而未决的问题。

### 段落 264 · Page 33

**EN**

•Robustness to AI-generated content.With the advent of LLMs, the amount of AI-generated content is also increasing. Dai et al. (2024) showed that neural retrievers are biased towards AIgenerated documents. Xu et al. (2024a) showed that similar problems persist in text-image retrieval models. Future IR modeling research should also consider the robustness of models to AI-generated content.

**中文**

•人工智能生成内容的稳健性。随着法学硕士的出现，人工智能生成内容的数量也在增加。戴等人。 (2024) 表明神经检索器偏向于人工智能生成的文档。徐等人。 （2024a）表明，文本图像检索模型中也存在类似的问题。未来的 IR 建模研究还应该考虑模型对人工智能生成内容的鲁棒性。

### 段落 265 · Page 33

**EN**

•Robustness to adversarial attacks.Recent works on ad hoc retrieval and RAG LLM safety have discussedBERT-based models’ brittleness to adversarial attacks (Wang et al., 2022b), as well as the threat of corpus poisoning where injected harmful documents lead to unsafe RAG system outputs (Zhong et al., 2023; Xiang et al., 2024a; Deng et al., 2024,inter alia). This topic is also relevant to the safety of LLM agents using tools (Deng et al., 2025; Tian et al., 2023; Xiang et al., 2024b), noting the importance of IR models being robust to adversarial attacks for downstream applications. 33

**中文**

针对对抗性攻击的鲁棒性。最近关于临时检索和 RAG LLM 安全性的工作讨论了基于 BERT 的模型对对抗性攻击的脆弱性（Wang 等人，2022b），以及注入有害文档导致不安全的 RAG 系统输出的语料库中毒威胁（Zhong 等人，2023；Xiang 等人，2024a；Deng 等人， 2024 年等）。该主题还与使用工具的 LLM 代理的安全性相关（Deng 等人，2025；Tian 等人，2023；Xiang 等人，2024b），指出 IR 模型对下游应用程序的对抗性攻击具有鲁棒性的重要性。 33

### Page 34

### 段落 266 · Page 34

**EN**

Published in Transactions on Machine Learning Research (02/2026) •Robustness to bias and toxicity.As noted by a recent work (An et al., 2025a), documents that contain biases and toxic materials can potentially jailbreak aligned LLMs. This observation highlights the importance for IR models to be robust to bias and toxic content. •Robustness to imperfect retrieval results.Different works have pointed out that existing RAG systems show performance degradation when the retrieval results contain irrelevant documents (Yoran et al., 2024; Chang et al., 2025; Yu et al., 2024c,inter alia).

**中文**

发表于《机器学习研究汇刊》(02/2026) •对偏见和毒性的鲁棒性。正如最近的一项工作（An 等人，2025a）所指出的，包含偏见和有毒材料的文档可能会越狱对齐的法学硕士。这一观察结果凸显了 IR 模型对偏差和有毒内容具有鲁棒性的重要性。 •对不完美检索结果的鲁棒性。不同的研究指出，当检索结果包含不相关文档时，现有的RAG系统会表现出性能下降（Yoran等人，2024；Chang等人，2025；Yu等人，2024c等）。

### 段落 267 · Page 34

**EN**

Therefore, the RAG paradigm demands more precise results from the retrieval models. •Robustness to out-of-distribution input.Given the fact that modern neural retrieval models are trained with data-driven approaches, perhaps it is not surprising to find their performance may vary with different linguistic properties of the queries and documents, i.e., out-of-distribution input from the training data. Several works have reported cross-encoder rerankers’ performance drops on out-of-domain datasets (Mokrii et al., 2021; Thakur et al., 2021). In the context of retrievalaugmented generation, Cao et al.

**中文**

因此，RAG 范式要求检索模型得到更精确的结果。对分布外输入的鲁棒性。考虑到现代神经检索模型是用数据驱动的方法进行训练的，因此发现它们的性能可能会随着查询和文档的不同语言属性（即来自训练数据的分布外输入）而变化，这也许并不奇怪。一些研究报告了跨编码器重排序器在域外数据集上的性能下降（Mokrii 等人，2021 年；Thakur 等人，2021 年）。在检索增强生成的背景下，曹等人。

### 段落 268 · Page 34

**EN**

(2025) conducted a rigorous benchmarking, and found that formality, readability, politeness and grammatical correctness—fundamental aspects of real-world user- LLM queries—can lead to significant performance variances of retrievers and RAG systems. This observation highlights the importance of retrieval models’ robustness to out-of-distribution (OOD) input (Gupta et al., 2024a). We refer readers for more detailed discussions on IR models’ robustness to dedicated surveys (Asai et al., 2024c; Liu et al., 2025c; Zhou et al., 2024).

**中文**

(2025) 进行了严格的基准测试，发现形式、可读性、礼貌和语法正确性（现实世界用户 LLM 查询的基本方面）可能会导致检索器和 RAG 系统的显着性能差异。这一观察结果强调了检索模型对分布外（OOD）输入的鲁棒性的重要性（Gupta 等人，2024a）。我们建议读者更详细地讨论 IR 模型对专门调查的稳健性（Asai 等人，2024c；Liu 等人，2025c；Zhou 等人，2024）。

### 段落 269 · Page 34

**EN**

Addressing these robustness issues at the model architecture level is a critical and underexplored direction for future research. 10 Conclusions and Closing Thoughts The journey of IR model architectures, as we have charted, is a story of escalating abstraction and semantic depth. Beginning with the foundational principles of term-based matching in Boolean, vector space, and probabilistic models, the field systematically evolved. Learning-to-Rank introduced the power of machine learning to combine diverse statistical features, but it was the advent of neural networks that marked the first major leap toward semantic understanding.

**中文**

在模型架构层面解决这些鲁棒性问题是未来研究的一个关键且尚未充分探索的方向。 10 个结论和结束语 正如我们所描绘的，IR 模型架构的旅程是一个不断升级的抽象和语义深度的故事。从布尔、向量空间和概率模型中基于术语的匹配的基本原理开始，该领域系统地发展。 Learning-to-Rank 引入了机器学习结合不同统计特征的能力，但神经网络的出现标志着语义理解的第一次重大飞跃。

### 段落 270 · Page 34

**EN**

These neural ranking models, with their ability to learn representations directly from text, began to bridge the lexical gap that had long constrained traditional methods. The arrival of pre-trained transformers likeBERTthen catalyzed a paradigm shift, providing a powerful, universal foundation for both highly-effective cross-encoder rerankers and efficient bi-encoder retrievers. Most recently, the ascent of LLMs has not only scaled up these existing architectures but has also introduced entirely new paradigms, such as generative retrieval and zero-shot listwise reranking, fundamentally reshaping what a retrieval system can do.

**中文**

这些神经排序模型具有直接从文本中学习表示的能力，开始弥合长期限制传统方法的词汇差距。像 BERT 这样的预训练 Transformer 的出现促进了范式转变，为高效的交叉编码器重排器和高效的双编码器检索器提供了强大的通用基础。最近，法学硕士的崛起不仅扩大了这些现有架构的规模，还引入了全新的范式，例如生成检索和零样本列表重排序，从根本上重塑了检索系统的功能。

### 段落 271 · Page 34

**EN**

Throughout this evolution, a core architectural tension has persisted: the tradeoff between effectiveness and efficiency. This is the fundamental conflict between deep, fine-grained interaction models (like interactionbased neural rankers and cross-encoders) that offer high accuracy, and scalable representation-based models (like vector space models, dense retrievers) that enable fast, pre-computable search over massive collections. The enduring “retrieve-then-rerank” pipeline is a direct architectural answer to this tradeoff.

**中文**

在整个演变过程中，核心架构的张力一直存在：有效性和效率之间的权衡。这是深度、细粒度的交互模型（如基于交互的神经排名器和交叉编码器）之间的根本冲突，这些模型提供高精度和可扩展的基于表示的模型（如向量空间模型、密集检索器），从而能够在大量集合上进行快速、可预计算的搜索。持久的“检索然后重新排序”管道是对这种权衡的直接架构答案。

### 段落 272 · Page 34

**EN**

Innovations like multi-vector models (e.g.,ColBERT) and hybrid sparse-dense systems represent sophisticated attempts to find a better balance on this spectrum, pushing the Pareto frontier of what is possible. Today, we stand at another inflection point. The primary “user” of IR is shifting from a human at a search bar to an AI model within a larger system. IR is no longer just a tool for finding documents; it is becoming a critical cognitive component for retrieval-augmented generation, autonomous agents, and complex reasoning systems. This shift, as outlined in Section 9, forces us to re-evaluate our core assumptions.

**中文**

多向量模型（例如 ColBERT）和混合稀疏-密集系统等创新代表了在该范围内找到更好平衡的复杂尝试，推动了可能性的帕累托前沿。今天，我们正站在另一个转折点。 IR 的主要“用户”正在从搜索栏上的人类转变为更大系统中的人工智能模型。 IR 不再只是查找文档的工具；它正在成为检索增强生成、自主代理和复杂推理系统的关键认知组件。正如第 9 节所述，这种转变迫使我们重新评估我们的核心假设。

### 段落 273 · Page 34

**EN**

Relevance is no longer solely about satisfying human information needs but about providing the precise factual or contextual information an AI needs to complete a downstream task. This demands new model architectures that are not only powerful and efficient but also instruction-aware, contextually flexible, and seamlessly integrable into end-to-end differentiable systems. 34

**中文**

相关性不再仅仅是满足人类信息需求，而是提供人工智能完成下游任务所需的精确事实或上下文信息。这需要新的模型架构不仅功能强大、高效，而且具有指令感知能力、上下文灵活，并且能够无缝集成到端到端可微分系统中。 34

### Page 35

### 段落 274 · Page 35

**EN**

Published in Transactions on Machine Learning Research (02/2026) Looking ahead, the future of IR model architecture will be defined by its ability to meet these new demands. The grand challenges lie in building foundation models that are multimodal, multilingual, and computationally sustainable; in designing systems that are robust, trustworthy, and resistant to adversarial manipulation; and in developing autonomous search agents that can reason, plan, and interact with the world’s information on our behalf.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) 展望未来，IR 模型架构的未来将取决于其满足这些新需求的能力。巨大的挑战在于建立多模式、多语言且计算上可持续的基础模型；设计稳健、值得信赖且能抵抗对抗性操纵的系统；开发能够代表我们推理、规划世界信息并与之交互的自主搜索代理。

### 段落 275 · Page 35

**EN**

As IR becomes ever more deeply embedded in the fabric of artificial intelligence, its continued evolution will be crucial, not just for the future of search, but for the future of intelligent systems themselves. Acknowledgments This work was partially supported by grants from NSF (DMS 2134223 and IIS 2205418). References Qingyao Ai, Keping Bi, Jiafeng Guo, and W. Bruce Croft. Learning a deep listwise context model for ranking refinement. InProceedings of the 41st International ACM SIGIR Conference on Research & Development in Information Retrieval, pp. 135–144, 2018a. Qingyao Ai, Jiaxin Mao, Yiqun Liu, and W. Bruce Croft.

**中文**

随着IR越来越深入地嵌入人工智能的结构中，它的持续发展将变得至关重要，不仅对于搜索的未来，而且对于智能系统本身的未来。致谢 这项工作得到了 NSF 资助的部分支持（DMS 2134223 和 IIS 2205418）。参考文献 Qingyao Ai、Keping Bi、Jiafenguo 和 W. Bruce Croft。学习深度列表上下文模型以进行排名细化。第 41 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 135-144 页，2018a。艾清耀、毛嘉欣、刘逸群和 W. Bruce Croft。

### 段落 276 · Page 35

**EN**

Unbiased learning to rank: Theory and practice. InProceedings of the 27th ACM International Conference on Information and Knowledge Management, CIKM ’18, pp. 2305–2306, New York, NY, USA, 2018b. Association for Computing Machinery. doi: 10.1145/3269206.3274274. Qingyao Ai, Xuanhui Wang, Sebastian Bruch, Nadav Golbandi, Michael Bendersky, and Marc Najork. Learning groupwise multivariate scoring functions using deep neural networks. InProceedings of the 2019 ACM SIGIR International Conference on Theory of Information Retrieval, pp. 85–92, 2019. Sophia Althammer, Sebastian Hofstätter, and Allan Hanbury.

**中文**

无偏见学习排名：理论与实践。第 27 届 ACM 国际信息和知识管理会议论文集，CIKM ’18，第 2305–2306 页，美国纽约州纽约，2018b。计算机器协会。号码：10.1145/3269206.3274274。艾清耀、王选辉、塞巴斯蒂安·布鲁赫、纳达夫·戈尔班迪、迈克尔·本德斯基和马克·纳约克。使用深度神经网络学习分组多元评分函数。 2019 年 ACM SIGIR 信息检索理论国际会议论文集，第 85-92 页，2019 年。Sophia Althammer、Sebastian Hofstätter 和 Allan Hanbury。

### 段落 277 · Page 35

**EN**

Cross-domain retrieval in the legal and patent domains: a reproducability study. InEuropean Conference on Information Retrieval, 2020. BangAn, ShiyueZhang, andMarkDredze. RAGLLMsarenotsafer: Asafetyanalysisofretrieval-augmented generationforlargelanguagemodels. InLuisChiruzzo, AlanRitter, andLuWang(eds.),Proceedings of the 2025 Conference of the Nations of the Americas Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers), pp. 5444–5474, Albuquerque, New Mexico, April 2025a. Association for Computational Linguistics. URLhttps://aclanthology.org/2025.naacl-long. 281/.

**中文**

法律和专利领域的跨域检索：可重复性研究。欧洲信息检索会议，2020 年。BangAn、ShiyueZhang 和 Mark Dredze。 RAGLLM 并不安全：大型语言模型检索增强生成的安全分析。 In Luis Chiruzzo、Alan Ritter 和 LuWang（编辑），计算语言学协会美洲国家分会 2025 年会议记录：人类语言技术（第一卷：长论文），第 5444-5474 页，新墨西哥州阿尔伯克基，2025 年 4 月a。计算语言学协会。网址https://aclanthology.org/2025.naacl-long。 281/。

### 段落 278 · Page 35

**EN**

YuweiAn, YihuaCheng, SeoJinPark, andJunchenJiang. HyperRAG:Enhancingquality-efficiencytradeoffs in retrieval-augmented generation with reranker kv-cache reuse.arXiv preprint arXiv:2504.02921, 2025b. Alan Ansell, Edoardo Ponti, Anna Korhonen, and Ivan Vulić. Composable sparse fine-tuning for crosslingual transfer. In Smaranda Muresan, Preslav Nakov, and Aline Villavicencio (eds.),Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp. 1778–1796, Dublin, Ireland, May 2022. Association for Computational Linguistics. doi: 10.18653/v1/2022. acl-long.125.

**中文**

Yuwei An、Yihua Cheng、Seo Jin Park 和 Junchen Jiang。 HyperRAG：通过重新排序器 kv 缓存重用增强检索增强生成中的质量与效率权衡。arXiv 预印本 arXiv：2504.02921，2025b。艾伦·安塞尔、爱德华多·庞蒂、安娜·科尔霍宁和伊万·武利奇。用于跨语言迁移的可组合稀疏微调。 Smaranda Muresan、Preslav Nakov 和 Aline Villavicencio（编辑），计算语言学协会第 60 届年会论文集（第一卷：长论文），第 1778-1796 页，爱尔兰都柏林，2022 年 5 月。计算语言学协会。 doi：10.18653/v1/2022。 acl-long.125。

### 段落 279 · Page 35

**EN**

URLhttps://aclanthology.org/2022.acl-long.125/. Abrar Anwar, John Welsh, Joydeep Biswas, Soha Pouya, and Yan Chang. Remembr: Building and reasoning over long-horizon spatio-temporal memory for robot navigation.arXiv preprint arXiv:2409.13682, 2024. Sanjeev Arora, Yingyu Liang, and Tengyu Ma. A simple but tough-to-beat baseline for sentence embeddings. InInternational Conference on Learning Representations, 2017. URLhttps://openreview.net/forum? id=SyK00v5xx. Mikel Artetxe, Sebastian Ruder, and Dani Yogatama. On the cross-lingual transferability of monolingual representations.

**中文**

网址https://aclanthology.org/2022.acl-long.125/。阿布拉尔·安瓦尔、约翰·威尔士、乔伊迪普·比斯瓦斯、索哈·普亚和张彦。记住：用于机器人导航的长视野时空记忆的构建和推理。arXiv 预印本 arXiv:2409.13682, 2024。Sanjeev Arora、Yingyu Liang 和 Tengyu Ma。一个简单但难以超越的句子嵌入基线。见国际学习表征会议，2017。网址https://openreview.net/forum? id=SyK00v5xx。米克尔·阿泰克斯、塞巴斯蒂安·鲁德和丹尼·瑜伽塔玛。关于单语表示的跨语言可迁移性。

### 段落 280 · Page 35

**EN**

In Dan Jurafsky, Joyce Chai, Natalie Schluter, and Joel Tetreault (eds.),Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics, pp. 4623–4637, Online, July 2020. Association for Computational Linguistics. doi: 10.18653/v1/2020.acl-main.421. URLhttps: //aclanthology.org/2020.acl-main.421/. 35

**中文**

载于 Dan Jurafsky、Joyce Chai、Natalie Schluter 和 Joel Tetreault（编辑），计算语言学协会第 58 届年会论文集，第 4623-4637 页，在线，2020 年 7 月。计算语言学协会。 doi：10.18653/v1/2020.acl-main.421。网址https://aclanthology.org/2020.acl-main.421/。 35

### Page 36

### 段落 281 · Page 36

**EN**

Published in Transactions on Machine Learning Research (02/2026) AkariAsai, TimoSchick, PatrickLewis, XilunChen, GautierIzacard, SebastianRiedel, HannanehHajishirzi, and Wen-tau Yih. Task-aware retrieval with instructions. In Anna Rogers, Jordan Boyd-Graber, and Naoaki Okazaki (eds.),Findings of the Association for Computational Linguistics: ACL 2023, pp. 3650– 3675, Toronto, Canada, July 2023. Association for Computational Linguistics. doi: 10.18653/v1/2023. findings-acl.225. URLhttps://aclanthology.org/2023.findings-acl.225/.

**中文**

发表于机器学习研究汇刊 (02/2026) AkariAsai、TimoSchick、PatrickLewis、XilunChen、GautierIzacard、SebastianRiedel、HannanehHajishirzi 和 Wen-tau Yih。带指令的任务感知检索。载于 Anna Rogers、Jordan Boyd-Graber 和 Naoaki Okazaki（编辑），计算语言学协会的调查结果：ACL 2023，第 3650–3675 ​​页，加拿大多伦多，2023 年 7 月。计算语言学协会。 doi：10.18653/v1/2023。调查结果-acl.225。网址https://aclanthology.org/2023.findings-acl.225/。

### 段落 282 · Page 36

**EN**

Akari Asai, Jacqueline He, Rulin Shao, Weijia Shi, Amanpreet Singh, Joseph Chee Chang, Kyle Lo, Luca Soldaini, Sergey Feldman, Mike D’arcy, et al. OpenScholar: Synthesizing scientific literature with retrievalaugmented LMs.arXiv preprint arXiv:2411.14199, 2024a. Akari Asai, Zeqiu Wu, Yizhong Wang, Avirup Sil, and Hannaneh Hajishirzi. Self-RAG: Learning to retrieve, generate, and critique through self-reflection. InThe 12th International Conference on Learning Representations, 2024b. URLhttps://openreview.net/forum?id=hSyW5go0v8. Akari Asai, Zexuan Zhong, Danqi Chen, Pang Wei Koh, Luke Zettlemoyer, Hannaneh Hajishirzi, and Wen-tau Yih.

**中文**

Akari Asai、Jacqueline He、Rulin Shao、Weijia Shi、Amanpreet Singh、Joseph Chee Chang、Kyle Lo、Luca Soldaini、Sergey Feldman、Mike D’arcy 等。 OpenScholar：利用检索增强的 LMs 综合科学文献。arXiv 预印本 arXiv:2411.14199, 2024a。 Akari Asai、Zeqiu Wu、Yizhong Wang、Avirup Sil 和 Hannaneh Hajishirzi。 Self-RAG：通过自我反思学习检索、生成和批判。在第 12 届学习表征国际会议，2024b。网址https://openreview.net/forum?id=hSyW5go0v8。 Akari Asai、Zexuanzhong、Danqi Chen、Pang Wei Koh、Luke Zettlemoyer、Hannaneh Hajishirzi 和 Wen-tau Yih。

### 段落 283 · Page 36

**EN**

Reliable, adaptable, and attributable language models with retrieval.arXiv preprint arXiv:2403.03187, 2024c. Ricardo Baeza-Yates and Berthier Ribeiro-Neto.Modern Information Retrieval. ACM Press; Addison- Wesley, 1st edition, 1999. Dzmitry Bahdanau, Kyunghyun Cho, and Yoshua Bengio. Neural machine translation by jointly learning to align and translate.arXiv preprint arXiv:1409.0473, 2014. Yang Bai, Xiaoguang Li, Gang Wang, Chaoliang Zhang, Lifeng Shang, Jun Xu, Zhaowei Wang, Fangshan Wang, and Qun Liu. SparTerm: Learning term-based sparse representation for fast text retrieval.arXiv preprint arXiv:2010.00768, 2020.

**中文**

具有检索功能的可靠、适应性强且可归因的语言模型。arXiv 预印本 arXiv:2403.03187, 2024c。 Ricardo Baeza-Yates 和 Berthier Ribeiro-Neto。现代信息检索。 ACM出版社； Addison-Wesley，第 1 版，1999 年。Dzmitry Bahdanau、Kyunghyun Cho 和 Yoshua Bengio。通过联合学习对齐和翻译进行神经机器翻译。arXiv 预印本 arXiv:1409.0473, 2014。Yang Bai、Xiaoguang Li、Gang Wang、Chaoliang Zhang、Lifeng Shang、Jun Xu、Zhaowei Wang、Fangshan Wang 和 Qun Liu。 SparTerm：学习基于术语的稀疏表示以实现快速文本检索。arXiv 预印本 arXiv：2010.00768，2020。

### 段落 284 · Page 36

**EN**

Yuntao Bai, Saurav Kadavath, Sandipan Kundu, Amanda Askell, Jackson Kernion, Andy Jones, Anna Chen, Anna Goldie, Azalia Mirhoseini, Cameron McKinnon, et al. Constitutional AI: Harmlessness from AI feedback.arXiv preprint arXiv:2212.08073, 2022. Soyuj Basnet, Jerry Gou, Antonio Mallia, and Torsten Suel. Deeperimpact: Optimizing sparse learned index structures.arXiv preprint arXiv:2405.17093, 2024. Parishad BehnamGhader, Vaibhav Adlakha, Marius Mosbach, Dzmitry Bahdanau, Nicolas Chapados, and Siva Reddy. LLM2Vec: Large language models are secretly powerful text encoders. In1st Conference on Language Modeling, 2024.

**中文**

白云涛、Saurav Kadavath、Sandipan Kundu、Amanda Askell、Jackson Kernion、Andy Jones、Anna Chen、Anna Goldie、Azalia Mirhoseini、Cameron McKinnon 等。宪法人工智能：人工智能反馈的无害性。arXiv 预印本 arXiv：2212.08073，2022。Soyuj Basnet、Jerry Gou、Antonio Mallia 和 Torsten Suel。 Deeperimpact：优化稀疏学习索引结构。arXiv 预印本 arXiv：2405.17093，2024。Parishad BehnamGhader、Vaibhav Adlakha、Marius Mosbach、Dzmitry Bahdanau、Nicolas Chapados 和 Siva Reddy。 LLM2Vec：大型语言模型是秘密的强大文本编码器。第一届语言建模会议，2024 年。

### 段落 285 · Page 36

**EN**

URLhttps://openreview.net/forum?id=IW1PR7vEBf. Iz Beltagy, Matthew E. Peters, and Arman Cohan. Longformer: The long-document transformer.arXiv preprint arXiv:2004.05150, 2020. Adam Berger and John Lafferty. Information retrieval as statistical translation. InProceedings of the 22nd Annual International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 222–229, 1999. Michele Bevilacqua, Giuseppe Ottaviano, Patrick Lewis, Scott Yih, Sebastian Riedel, and Fabio Petroni. Autoregressive search engines: Generating substrings as document identifiers. In Alice H.

**中文**

网址https://openreview.net/forum?id=IW1PR7vEBf。伊兹·贝尔塔吉 (Iz Beltagy)、马修·E·彼得斯 (Matthew E. Peters) 和阿曼·科汉 (Arman Cohan)。 Longformer：长文档 Transformer.arXiv 预印本 arXiv:2004.05150, 2020。Adam Berger 和 John Lafferty。作为统计翻译的信息检索。 InProceedings of the 22nd Annual International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 222–229, 1999. Michele Bevilacqua、Giuseppe Ottaviano、Patrick Lewis、Scott Yih、Sebastian Riedel 和 Fabio Petroni。自回归搜索引擎：生成子字符串作为文档标识符。在爱丽丝·H.

### 段落 286 · Page 36

**EN**

Oh, Alekh Agarwal, Danielle Belgrave, and Kyunghyun Cho (eds.),Advances in Neural Information Processing Systems, 2022. URLhttps://openreview.net/forum?id=Z4kZxAjg8Y. Asia J. Biega, Krishna P. Gummadi, and Gerhard Weikum. Equity of attention: Amortizing individual fairness in rankings. InThe 41st International ACM SIGIR Conference on Research & Development in Information Retrieval, pp. 405–414, 2018. Luiz Bonifacio, Hugo Abonizio, Marzieh Fadaee, and Rodrigo Nogueira. InPars: Unsupervised dataset generation for information retrieval.

**中文**

哦，Alekh Agarwal、Danielle Belgrave 和 Kyunghyun Cho（编辑），神经信息处理系统的进展，2022 年。URL https://openreview.net/forum?id=Z4kZxAjg8Y。阿莎·J·比加 (Asia J. Biega)、克里希纳·P·古马迪 (Krishna P. Gummadi) 和格哈德·维库姆 (Gerhard Weikum)。注意力公平：在排名中摊销个人公平性。载于第 41 届国际 ACM SIGIR 信息检索研究与开发会议，第 405-414 页，2018 年。Luiz Bonifacio、Hugo Abonizio、Marzieh Fadaee 和 Rodrigo Nogueira。 InPars：用于信息检索的无监督数据集生成。

### 段落 287 · Page 36

**EN**

InProceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 2387–2392, 2022. 36

**中文**

第 45 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 2387-2392 页，2022 年。 36

### Page 37

### 段落 288 · Page 37

**EN**

Published in Transactions on Machine Learning Research (02/2026) Sebastian Borgeaud, Arthur Mensch, Jordan Hoffmann, Trevor Cai, Eliza Rutherford, Katie Millican, George Bm Van Den Driessche, Jean-Baptiste Lespiau, Bogdan Damoc, Aidan Clark, et al. Improving language models by retrieving from trillions of tokens. InInternational Conference on Machine Learning, pp. 2206–2240. PMLR, 2022. Leonid Boytsov, Preksha Patel, Vivek Sourabh, Riddhi Nisar, Sayani Kundu, Ramya Ramanathan, and Eric Nyberg. InPars-Light: Cost-effective unsupervised training of efficient rankers.Transactions on Machine Learning Research, 2024. Sergey Brin and Lawrence Page.

**中文**

发表于《机器学习研究汇刊》(02/2026) Sebastian Borgeaud、Arthur Mensch、Jordan Hoffmann、Trevor Cai、Eliza Rutherford、Katie Millican、George Bm Van Den Driessche、Jean-Baptiste Lespiau、Bogdan Damoc、Aidan Clark 等人。通过检索数万亿个标记来改进语言模型。国际机器学习会议，第 2206-2240 页。 PMLR，2022。Leonid Boytsov、Preksha Patel、Vivek Sourabh、Riddhi Nisar、Sayani Kundu、Ramya Ramanathan 和 Eric Nyberg。 InPars-Light：高效排名者的经济有效的无监督训练。机器学习研究交易，2024 年。Sergey Brin 和 Lawrence Page。

### 段落 289 · Page 37

**EN**

The anatomy of a large-scale hypertextual web search engine.Computer Networks, 30:107–117, 1998. URLhttp://www-db.stanford.edu/~backrub/google.html. Andrei Z. Broder, David Carmel, Michael Herscovici, Aya Soffer, and Jason Zien. Efficient query evaluation using a two-level retrieval process. InProceedings of the 12th International Conference on Information and Knowledge Management, pp. 426–434, 2003. Peter F. Brown, Stephen A. Della Pietra, Vincent J. Della Pietra, and Robert L. Mercer. The mathematics of statistical machine translation: Parameter estimation.Computational linguistics, 19(2):263–311, 1993.

**中文**

大规模超文本网络搜索引擎的剖析。计算机网络，30:107–117, 1998。URLhttp://www-db.stanford.edu/~backrub/google.html。安德烈·Z·布罗德、大卫·卡梅尔、迈克尔·赫斯科维奇、阿雅·索弗和杰森·齐恩​​。使用两级检索过程进行有效的查询评估。第 12 届国际信息和知识管理会议论文集，第 426-434 页，2003 年。Peter F. Brown、Stephen A. Della Pietra、Vincent J. Della Pietra 和 Robert L. Mercer。统计机器翻译的数学：参数估计。计算语言学，19(2):263–311, 1993。

### 段落 290 · Page 37

**EN**

Tom Brown, Benjamin Mann, Nick Ryder, Melanie Subbiah, Jared D. Kaplan, Prafulla Dhariwal, Arvind Neelakantan, Pranav Shyam, Girish Sastry, Amanda Askell, et al. Language models are few-shot learners. Advances in neural information processing systems, 33:1877–1901, 2020. Sebastian Bruch, Masrour Zoghi, Michael Bendersky, and Marc Najork. Revisiting approximate metric optimization in the age of deep neural networks. InProceedings of the 42nd International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 1241–1244, 2019. Sebastian Bruch, Franco Maria Nardini, Cosimo Rulli, and Rossano Venturini.

**中文**

Tom Brown、Benjamin Mann、Nick Ryder、Melanie Subbiah、Jared D. Kaplan、Prafulla Dhariwal、Arvind Neelakantan、Pranav Shyam、Girish Sastry、Amanda Askell 等。语言模型是小样本学习者。神经信息处理系统的进展，33：1877-1901，2020。Sebastian Bruch、Masrour Zoghi、Michael Bendersky 和 ​​Marc Najork。重新审视深度神经网络时代的近似度量优化。第 42 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 1241-1244 页，2019 年。Sebastian Bruch、Franco Maria Nardini、Cosimo Rulli 和 Rossano Venturini。

### 段落 291 · Page 37

**EN**

Efficient inverted indexes for approximate retrieval over learned sparse representations. InProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 152–162, 2024. Cristian Buciluă, Rich Caruana, and Alexandru Niculescu-Mizil. Model compression. InProceedings of the 12th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, pp. 535–541, 2006. Chris Burges, Tal Shaked, Erin Renshaw, Ari Lazier, Matt Deeds, Nicole Hamilton, and Greg Hullender. Learning to rank using gradient descent. InProceedings of the 22nd International Conference on Machine Learning, pp.

**中文**

用于对学习的稀疏表示进行近似检索的高效倒排索引。第 47 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 152-162 页，2024 年。Cristian Buciluă、Rich Caruana 和 Alexandru Niculescu-Mizil。模型压缩。第 12 届 ACM SIGKDD 国际知识发现和数据挖掘会议记录，第 535-541 页，2006 年。Chris Burges、Tal Shaked、Erin Renshaw、Ari Lazier、Matt Deeds、Nicole Hamilton 和 Greg Hullender。学习使用梯度下降进行排名。载于第 22 届国际机器学习会议论文集，第 22 页。

### 段落 292 · Page 37

**EN**

89–96, 2005. Christopher Burges, Robert Ragno, and Quoc Le. Learning to rank with nonsmooth cost functions.Advances in neural information processing systems, 19, 2006. Christopher J.C. Burges. From ranknet to lambdarank to lambdamart: An overview.Learning, 11(23-581): 81, 2010. Tianyu Cao, Neel Bhandari, Akhila Yerukola, Akari Asai, and Maarten Sap. Out of style: RAG’s fragility to linguistic variation.arXiv preprint arXiv:2504.08231, 2025. Zhe Cao, Tao Qin, Tie-Yan Liu, Ming-Feng Tsai, and Hang Li. Learning to rank: from pairwise approach to listwise approach. InProceedings of the 24th International Conference on Machine Learning, pp.

**中文**

89–96, 2005。克里斯托弗·伯吉斯、罗伯特·拉格诺和夸克·勒。学习使用非平滑成本函数进行排名。神经信息处理系统的进展，2006 年 19 日。Christopher J.C. Burges。从ranknet到lambdarank再到lambdamart：概述。学习，11(23-581): 81, 2010。Tianyu Cao、Neel Bhandari、Akhila Yerukola、Akari Asai 和 Maarten Sap。过时：RAG 对语言变异的脆弱性。arXiv 预印本 arXiv:2504.08231, 2025。曹哲、秦涛、刘铁岩、蔡明峰和李航。学习排序：从成对方法到列表方法。载于第 24 届国际机器学习会议论文集，第 123 页。

### 段落 293 · Page 37

**EN**

129–136, 2007. Chia-Yuan Chang, Zhimeng Jiang, Vineeth Rakesh, Menghai Pan, Chin-Chia Michael Yeh, Guanchu Wang, Mingzhi Hu, Zhichao Xu, Yan Zheng, Mahashweta Das, and Na Zou. MAIN-RAG: Multi-agent filtering retrieval-augmented generation. In Wanxiang Che, Joyce Nabende, Ekaterina Shutova, and Mohammad Taher Pilehvar (eds.),Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp. 2607–2622, Vienna, Austria, July 2025. Association for Computational Linguistics. doi: 10.18653/v1/2025.acl-long.131. URLhttps://aclanthology.org/2025. acl-long.131/. 37

**中文**

129–136, 2007。张嘉源、蒋志猛、Vineeth Rakesh、潘梦海、叶钦嘉、王冠初、胡明志、徐志超、郑严、Mahashweta Das 和邹娜。 MAIN-RAG：多代理过滤检索增强生成。载于 Wanyang Che、Joyce Nabende、Ekaterina Shutova 和 Mohammad Taher Pilehvar（编），计算语言学协会第 63 届年会论文集（第一卷：长论文），第 2607-2622 页，奥地利维也纳，2025 年 7 月。计算语言学协会。 doi：10.18653/v1/2025.acl-long.131。网址https://aclanthology.org/2025。 acl-long.131/。 37

### Page 38

### 段落 294 · Page 38

**EN**

Published in Transactions on Machine Learning Research (02/2026) Yin-Wen Chang, Cho-Jui Hsieh, Kai-Wei Chang, Michael Ringgaard, and Chih-Jen Lin. Training and testing low-degree polynomial data mappings via linear svm.Journal of Machine Learning Research, 11 (48):1471–1490, 2010. URLhttp://jmlr.org/papers/v11/chang10a.html. Jiangui Chen, Ruqing Zhang, Jiafeng Guo, M. de Rijke, Wei Chen, Yixing Fan, and Xueqi Cheng. Continual learning for generative retrieval over dynamic corpora.Proceedings of the 32nd ACM International Conference on Information and Knowledge Management, 2023a.

**中文**

发表于机器学习研究汇刊 (02/2026) Yin-Wen Chang、Cho-Jui Hsieh、Kai-Wei Chang、Michael Ringgaard 和 Chih-Jen Lin。通过线性 svm 训练和测试低次多项式数据映射。机器学习研究杂志，11 (48):1471–1490, 2010。URLhttp://jmlr.org/papers/v11/chang10a.html。陈建贵、张如青、郭家峰、M. de Rijke、陈伟、范宜兴和程学奇。动态语料库生成检索的持续学习。第 32 届 ACM 国际信息和知识管理会议论文集，2023a。

### 段落 295 · Page 38

**EN**

Mingyang Chen, Tianpeng Li, Haoze Sun, Yijie Zhou, Chenzheng Zhu, Haofen Wang, Jeff Z. Pan, Wen Zhang, Huajun Chen, Fan Yang, et al. Learning to reason with search for LLMs via reinforcement learning.arXiv preprint arXiv:2503.19470, 2025. Shizhe Chen, Yida Zhao, Qin Jin, and Qi Wu. Fine-grained video-text retrieval with hierarchical graph reasoning.2020 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), pp. 10635– 10644, 2020a. Sihan Chen, Handong Li, Qunbo Wang, Zijia Zhao, Ming-Ting Sun, Xinxin Zhu, and J. Liu.

**中文**

陈明阳、李天鹏、孙浩泽、周一杰、朱陈正、王浩芬、潘杰夫、张文、陈华军、杨帆等。通过强化学习搜索法学硕士来学习推理。arXiv 预印本 arXiv:2503.19470, 2025。陈士哲、赵一达、金勤和吴奇。使用分层图推理进行细粒度视频文本检索。2020 年 IEEE/CVF 计算机视觉和模式识别会议 (CVPR)，第 10635–10644 页，2020a。陈思涵、李汉东、王群波、赵自佳、孙明廷、朱欣欣和刘杰。

### 段落 296 · Page 38

**EN**

VAST: A vision-audio-subtitle-text omni-modality foundation model and dataset.ArXiv preprint arXiv:2305.18500, 2023b. Wei-Fan Chen, Shahbaz Syed, Benno Stein, Matthias Hagen, and Martin Potthast. Abstractive snippet generation. InProceedings of the Web Conference 2020, WWW ’20, pp. 1309–1319, New York, NY, USA, 2020b. Association for Computing Machinery. ISBN 9781450370233. doi: 10.1145/3366423.3380206. URL https://doi.org/10.1145/3366423.3380206. Xuanang Chen, Ben He, Kai Hui, Le Sun, and Yingfei Sun. Simplified TinyBERT: Knowledge distillation for document retrieval. InEuropean Conference on Information Retrieval, pp. 241–248.

**中文**

VAST：视觉-音频-字幕-文本全模态基础模型和数据集。ArXiv 预印本 arXiv:2305.18500, 2023b。陈伟凡、Shahbaz Syed、Benno Stein、Matthias Hagen 和 Martin Potthast。抽象片段生成。 2020 年网络会议记录，WWW '20，第 1309–1319 页，美国纽约州纽约，2020b。计算机器协会。 ISBN 9781450370233。doi：10.1145/3366423.3380206。网址 https://doi.org/10.1145/3366423.3380206。陈轩昂、何奔、凯辉、孙乐和孙英飞。简化的 TinyBERT：用于文档检索的知识蒸馏。欧洲信息检索会议，第 241-248 页。

### 段落 297 · Page 38

**EN**

Springer, 2021. ZewenChi, LiDong, FuruWei, NanYang, SakshamSinghal, WenhuiWang, XiaSong, Xian-LingMao, Heyan Huang, and Ming Zhou. InfoXLM: An information-theoretic framework for cross-lingual language model pre-training. In Kristina Toutanova, Anna Rumshisky, Luke Zettlemoyer, Dilek Hakkani-Tur, Iz Beltagy, Steven Bethard, Ryan Cotterell, Tanmoy Chakraborty, and Yichao Zhou (eds.),Proceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, pp. 3576–3588, Online, June 2021. Association for Computational Linguistics. doi: 10.18653/v1/2021.naacl-main.280.

**中文**

Springer，2021。ZewenChi、LiDong、FuruWei、NanYang、SakshamSinghal、WenhuiWang、XiaSong、Xian-LingMao、Heyan Huang 和 Ming Zhou。 InfoXLM：跨语言语言模型预训练的信息理论框架。载于 Kristina Toutanova、Anna Rumshisky、Luke Zettlemoyer、Dilek Hakkani-Tur、Iz Beltagy、Steven Bethard、Ryan Cotterell、Tanmoy Chakraborty 和 Yichao Zhou（编辑），计算语言学协会北美分会 2021 年会议记录：人类语言技术，第 3576-3588 页，在线，2021 年 6 月。计算语言学协会。 doi：10.18653/v1/2021.naacl-main.280。

### 段落 298 · Page 38

**EN**

URLhttps://aclanthology.org/2021.naacl-main.280/. Hyung Won Chung, Le Hou, Shayne Longpre, Barret Zoph, Yi Tay, William Fedus, Yunxuan Li, Xuezhi Wang, Mostafa Dehghani, Siddhartha Brahma, et al. Scaling instruction-finetuned language models. Journal of Machine Learning Research, 25(70):1–53, 2024. Kevin Clark, Urvashi Khandelwal, Omer Levy, and Christopher D. Manning. What does BERT look at? An Analysis of BERT’s Attention. In Tal Linzen, Grzegorz Chrupała, Yonatan Belinkov, and Dieuwke Hupkes (eds.),Proceedings of the 2019 ACL Workshop BlackboxNLP: Analyzing and Interpreting Neural Networks for NLP, pp.

**中文**

网址https://aclanthology.org/2021.naacl-main.280/。 Hyung Won Chung、Le Hou、Shayne Longpre、Barret Zoph、Yi Tay、William Fedus、Yunxuan Li、Xuezhi Wang、Mostafa Dehghani、Siddhartha Brahma 等。扩展指令微调语言模型。机器学习研究杂志，25(70):1–53，2024。Kevin Clark、Urvashi Khandelwal、Omer Levy 和 Christopher D. Manning。 BERT 关注什么？ BERT 注意力分析。载于 Tal Linzen、Grzegorz Chrupała、Yonatan Belinkov 和 Dieuwke Hupkes（编），2019 年 ACL 研讨会 BlackboxNLP 论文集：分析和解释 NLP 神经网络，第 123 页。

### 段落 299 · Page 38

**EN**

276–286, Florence, Italy, August 2019. Association for Computational Linguistics. doi: 10.18653/v1/W19-4828. URLhttps://aclanthology.org/W19-4828/. Charles L. A. Clarke and Laura Dietz. LLM-based relevance assessment still can’t replace human relevance assessment.arXiv preprint arXiv:2412.17156, 2024. Daniel Cohen and W. Bruce Croft. End to end long short term memory networks for non-factoid question answering. InProceedings of the 2016 ACM International Conference on the Theory of Information Retrieval, ICTIR ’16, pp. 143–146, New York, NY, USA, 2016. Association for Computing Machinery. doi: 10.1145/2970398.2970438.

**中文**

276–286，意大利佛罗伦萨，2019 年 8 月。计算语言学协会。 doi：10.18653/v1/W19-4828。网址https://aclanthology.org/W19-4828/。查尔斯·L·A·克拉克和劳拉·迪茨。基于 LLM 的相关性评估仍然无法取代人类相关性评估。arXiv 预印本 arXiv:2412.17156, 2024。Daniel Cohen 和 W. Bruce Croft。用于非事实问答的端到端长短期记忆网络。 2016 年 ACM 国际信息检索理论会议论文集，ICTIR ’16，第 143–146 页，美国纽约州纽约市，2016 年。计算机协会。号码：10.1145/2970398.2970438。

### 段落 300 · Page 38

**EN**

Daniel Cohen, Bhaskar Mitra, Oleg Lesota, Navid Rekabsaz, and Carsten Eickhoff. Not all relevance scores are equal: Efficient uncertainty and calibration modeling for deep retrieval models.Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, 2021. 38

**中文**

丹尼尔·科恩、巴斯卡·米特拉、奥列格·莱索塔、纳维德·雷卡布萨兹和卡斯滕·艾克霍夫。并非所有相关性分数都相同：深度检索模型的高效不确定性和校准建模。第 44 届国际 ACM SIGIR 信息检索研究与发展会议论文集，2021 年。 38

### Page 39

### 段落 301 · Page 39

**EN**

Published in Transactions on Machine Learning Research (02/2026) Ronan Collobert, Jason Weston, Léon Bottou, Michael Karlen, Koray Kavukcuoglu, and Pavel Kuksa. Natural language processing (almost) from scratch.Journal of machine learning research, 12(7), 2011. Alexis Conneau, Kartikay Khandelwal, Naman Goyal, Vishrav Chaudhary, Guillaume Wenzek, Francisco Guzmán, Edouard Grave, Myle Ott, Luke Zettlemoyer, and Veselin Stoyanov. Unsupervised crosslingual representation learning at scale. InProceedings of the 58th Annual Meeting of the Association for Computational Linguistics, pp. 8440–8451, 2020a. doi: 10.18653/v1/2020.acl-main.747.

**中文**

发表于机器学习研究汇刊 (02/2026) Ronan Collobert、Jason Weston、Léon Bottou、Michael Karlen、Koray Kavukcuoglu 和 Pavel Kuksa。自然语言处理（几乎）从头开始。机器学习研究杂志，12(7)，2011。Alexis Conneau、Kartikay Khandelwal、Naman Goyal、Vishrav Chaudhary、Guillaume Wenzek、Francisco Guzmán、Edouard Grave、Myle Ott、Luke Zettlemoyer 和 Veselin Stoyanov。大规模无监督跨语言表示学习。计算语言学协会第 58 届年会记录，第 8440–8451 页，2020a。 doi：10.18653/v1/2020.acl-main.747。

### 段落 302 · Page 39

**EN**

URL https://aclanthology.org/2020.acl-main.747/. Alexis Conneau, Shijie Wu, Haoran Li, Luke Zettlemoyer, and Veselin Stoyanov. Emerging cross-lingual structure in pretrained language models. In Dan Jurafsky, Joyce Chai, Natalie Schluter, and Joel Tetreault (eds.),Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics, pp. 6022– 6034, Online, July 2020b. Association for Computational Linguistics. doi: 10.18653/v1/2020.acl-main.536. URLhttps://aclanthology.org/2020.acl-main.536/. Gordon V. Cormack, Charles L. A. Clarke, and Stefan Buettcher.

**中文**

网址 https://aclanthology.org/2020.acl-main.747/。 Alexis Conneau、吴世杰、李浩然、Luke Zettlemoyer 和 Veselin Stoyanov。预训练语言模型中新兴的跨语言结构。载于 Dan Jurafsky、Joyce Chai、Natalie Schluter 和 Joel Tetreault（编辑），计算语言学协会第 58 届年会记录，第 6022-6034 页，在线，2020 年 7 月b。计算语言学协会。 doi：10.18653/v1/2020.acl-main.536。网址https://aclanthology.org/2020.acl-main.536/。戈登·V·科马克、查尔斯·L·A·克拉克和斯特凡·布彻。

### 段落 303 · Page 39

**EN**

Reciprocal rank fusion outperforms condorcet and individual rank learning methods. InProceedings of the 32nd International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’09, pp. 758–759, New York, NY, USA, 2009. Association for Computing Machinery. doi: 10.1145/1571941.1572114. Corinna Cortes and Vladimir Vapnik. Support-vector networks.Machine learning, 20(3):273–297, 1995. Kunal Dahiya, Ananye Agarwal, Deepak Saini, Jian Jiao, Amit Singh, Sumeet Agarwal, Purushottam Kar, Manik Varma, et al. Siamesexml: Siamese networks meet extreme classifiers with 100m labels.

**中文**

互惠等级融合优于Condorcet 和个体等级学习方法。 InProceedings of the 32nd International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’09, pp. 758–759, New York, NY, USA, 2009. 计算机协会。号码：10.1145/1571941.1572114。科琳娜·科尔特斯和弗拉基米尔·瓦普尼克。支持向量网络。机器学习，20(3):273–297, 1995。 Kunal Dahiya、Ananye Agarwal、Deepak Saini、Jian Jiao、Amit Singh、Sumeet Agarwal、Purushottam Kar、Manik Varma 等。 Siamesexml：Siamese 网络满足具有 100m 个标签的极端分类器。

### 段落 304 · Page 39

**EN**

InInternational Conference on Machine Learning, pp. 2330–2340. PMLR, 2021. Kunal Dahiya, Sachin Yadav, Sushant Sondhi, Deepak Saini, Sonu Mehta, Jian Jiao, Sumeet Agarwal, Purushottam Kar, and Manik Varma. Deep encoders with auxiliary parameters for extreme classification. InProceedings of the 29th ACM SIGKDD Conference on Knowledge Discovery and Data Mining, pp. 358–367, 2023. Sunhao Dai, Yuqi Zhou, Liang Pang, Weihao Liu, Xiaolin Hu, Yong Liu, Xiao Zhang, Gang Wang, and Jun Xu. Neural retrievers are biased towards LLM-generated content. InProceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining, pp.

**中文**

国际机器学习会议，第 2330-2340 页。 PMLR，2021。Kunal Dahiya、Sachin Yadav、Sushant Sondhi、Deepak Saini、Sonu Mehta、Jian Jiao、Sumeet Agarwal、Purushottam Kar 和 Manik Varma。具有辅助参数的深度编码器，用于极端分类。 InProceedings of the 29th ACM SIGKDD Conference on Knowledge Discovery and Data Mining, pp. 358–367, 2023. Sunhao Dai、Yuqi Zhou、Liang Pang、Weihao Liu、Xiaolin Hu、Yong Liu、Xiao Zhu、Gang Wang 和 Jun Xu。神经检索器偏向于法学硕​​士生成的内容。第 30 届 ACM SIGKDD 知识发现和数据挖掘会议论文集，第 30 页。

### 段落 305 · Page 39

**EN**

526–537, 2024. Zhuyun Dai and Jamie Callan. Deeper text understanding for ir with contextual neural language modeling.Proceedings of the 42nd International ACM SIGIR Conference on Research and Development in Information Retrieval, 2019a. Zhuyun Dai and Jamie Callan. Context-aware sentence/passage term importance estimation for 1st stage retrieval.arXiv preprint arXiv:1910.10687, 2019b. Zhuyun Dai, Chenyan Xiong, Jamie Callan, and Zhiyuan Liu. Convolutional neural networks for softmatching n-grams in ad-hoc search. InProceedings of the 11th ACM International Conference on Web Search and Data Mining, WSDM ’18, pp.

**中文**

526–537, 2024。戴竹云和杰米·卡伦。通过上下文神经语言建模对 ir 进行更深入的文本理解。第 42 届国际 ACM SIGIR 信息检索研究与发展会议论文集，2019a。戴朱云和杰米·卡兰。第一阶段检索的上下文感知句子/段落术语重要性估计。arXiv 预印本 arXiv:1910.10687, 2019b。戴朱云、熊陈彦、杰米·卡兰和刘志远。用于即席搜索中软匹配 n 元语法的卷积神经网络。第 11 届 ACM 国际网络搜索和数据挖掘会议论文集，WSDM '18，第 18 页。

### 段落 306 · Page 39

**EN**

126–134, New York, NY, USA, 2018. Association for Computing Machinery. doi: 10.1145/3159652.3159659. Zhuyun Dai, Vincent Y. Zhao, Ji Ma, Yi Luan, Jianmo Ni, Jing Lu, Anton Bakalov, Kelvin Guu, Keith Hall, and Ming-Wei Chang. Promptagator: Few-shot dense retrieval from 8 examples. InThe 11th International Conference on Learning Representations, 2023. Soham Dan and Dan Roth. On the effects of transformer size on in- and out-of-domain calibration. In Marie-Francine Moens, Xuanjing Huang, Lucia Specia, and Scott Wen-tau Yih (eds.),Findings of the Association for Computational Linguistics: EMNLP 2021, pp.

**中文**

126–134，美国纽约州纽约市，2018 年。计算机协会。号码：10.1145/3159652.3159659。戴竹云、赵文森、马季、栾毅、倪建模、卢静、Anton Bakalov、Kelvin Guu、Keith Hall 和 Ming-Wei Chang。 Promptagator：从 8 个示例中进行少样本密集检索。在第 11 届学习表征国际会议，2023 年。Soham Dan 和 Dan Roth。关于Transformer尺寸对域内和域外校准的影响。摘自 Marie-Francine Moens、Xuanjing Huang、Lucia Specia 和 Scott Wen-tau Yih（编辑），计算语言学协会的调查结果：EMNLP 2021，第 127 页。

### 段落 307 · Page 39

**EN**

2096–2101, Punta Cana, Dominican Republic, November 2021. Association for Computational Linguistics. doi: 10.18653/v1/2021.findings-emnlp.180. URLhttps://aclanthology.org/2021.findings-emnlp.180/. 39

**中文**

2096–2101，多米尼加共和国蓬塔卡纳，2021 年 11 月。计算语言学协会。 doi：10.18653/v1/2021.findings-emnlp.180。网址https://aclanthology.org/2021.findings-emnlp.180/。 39

### Page 40

### 段落 308 · Page 40

**EN**

Published in Transactions on Machine Learning Research (02/2026) Tri Dao and Albert Gu. Transformers are SSMs: Generalized models and efficient algorithms through structured state space duality.Proceedings of the 41st International Conference on Machine Learning, pp. 10041 – 10071, 2024. Arpan Dasgupta, Siddhant Katyan, Shrutimoy Das, and Pawan Kumar. Review of extreme multilabel classification.arXiv preprint arXiv:2302.05971, 2023. Denis Andrei de Araujo, Carolina Müller, Rove Chishman, and Sandro José Rigo.

**中文**

发表于机器学习研究汇刊 (02/2026) Tri Dao 和 Albert Gu。 Transformers 是 SSM：通过结构化状态空间对偶性实现的广义模型和高效算法。第 41 届国际机器学习会议论文集，第 10041 – 10071 页，2024 年。Arpan Dasgupta、Siddhant Katyan、Shrutimoy Das 和 Pawan Kumar。极端多标签分类回顾。arXiv 预印本 arXiv：2302.05971，2023。Denis Andrei de Araujo、Carolina Müller、Rove Chishman 和 Sandro José Rigo。

### 段落 309 · Page 40

**EN**

Information extraction for legal knowledge representation–a review of approaches and trends.Revista Brasileira de Computação Aplicada, 6(2):2–19, 2014. Nicola De Cao, G. Izacard, S. Riedel, and F. Petroni. Autoregressive entity retrieval. InICLR 2021-9th International Conference on Learning Representations, volume 2021. ICLR, 2021. Jeffrey Dean. Challenges in building large-scale information retrieval systems: invited talk. InProceedings of the 2nd ACM International Conference on Web Search and Data Mining, 2009. doi: 10.1145/1498759. 1498761.

**中文**

法律知识表示的信息提取——方法和趋势回顾。Revista Brasileira de Computação Aplicada, 6(2):2–19, 2014。Nicola De Cao、G. Izacard、S. Riedel 和 F. Petroni。自回归实体检索。 InICLR 2021-第 9 届学习表征国际会议，第 2021 卷。ICLR，2021。杰弗里·迪恩。构建大规模信息检索系统的挑战：邀请演讲。第二届 ACM 国际网络搜索和数据挖掘会议论文集，2009 年。doi：10.1145/1498759。 1498761。

### 段落 310 · Page 40

**EN**

Mostafa Dehghani, Josip Djolonga, Basil Mustafa, Piotr Padlewski, Jonathan Heek, Justin Gilmer, Andreas Peter Steiner, Mathilde Caron, Robert Geirhos, Ibrahim Alabdulmohsin, et al. Scaling vision transformers to 22 billion parameters. InInternational Conference on Machine Learning, pp. 7480–7512. PMLR, 2023. Gelei Deng, Yi Liu, Kailong Wang, Yuekang Li, Tianwei Zhang, and Yang Liu. Pandora: Jailbreak GPTs by retrieval augmented generation poisoning.arXiv preprint arXiv:2402.08416, 2024. Zehang Deng, Yongjian Guo, Changzhou Han, Wanlun Ma, Junwu Xiong, Sheng Wen, and Yang Xiang.

**中文**

Mostafa Dehghani、Josip Djolonga、Basil Mustafa、Piotr Padlewski、Jonathan Heek、Justin Gilmer、Andreas Peter Steiner、Mathilde Caron、Robert Geirhos、Ibrahim Alabdulmohsin 等。将视觉转换器扩展到 220 亿个参数。国际机器学习会议，第 7480–7512 页。 PMLR，2023。Gelei Deng、Yi Liu、Kailong Wang、Yuekang Li、Tianwei Zhang 和 Yang Liu。潘多拉：通过检索增强代中毒来越狱 GPT。arXiv 预印本 arXiv：2402.08416，2024。Zehang Deng、YongjianGuo、ChangzhouHan、WanlunMa、JunwuXiong、ShengWen 和 YangXiang。

### 段落 311 · Page 40

**EN**

AI agents under threat: A survey of key security challenges and future pathways.ACM Computing Surveys, 57(7):1–36, 2025. Tim Dettmers and Luke Zettlemoyer. The case for 4-bit precision: k-bit inference scaling laws. InInternational Conference on Machine Learning, pp. 7750–7774. PMLR, 2023. Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. BERT: Pre-training of deep bidirectionaltransformersforlanguageunderstanding.

**中文**

受到威胁的人工智能代理：关键安全挑战和未来路径的调查。ACM 计算调查，57(7):1–36, 2025。Tim Dettmers 和 Luke Zettlemoyer。 4 位精度的情况：k 位推理缩放定律。国际机器学习会议，第 7750–7774 页。 PMLR，2023。Jacob Devlin、Ming-Wei Chang、Kenton Lee 和 Kristina Toutanova。 BERT：用于语言理解的深度双向Transformer的预训练。

### 段落 312 · Page 40

**EN**

InJillBurstein, ChristyDoran, andThamarSolorio(eds.), Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long and Short Papers), pp. 4171–4186, Minneapolis, Minnesota, June 2019. Association for Computational Linguistics. doi: 10.18653/v1/N19-1423. URLhttps://aclanthology.org/N19-1423/. Shehzaad Dhuliawala, Leonard Adolphs, Rajarshi Das, and Mrinmaya Sachan. Calibration of machine reading systems at scale.

**中文**

InJillBurstein、ChristyDoran 和 ThamarSolorio（编辑），计算语言学协会北美分会 2019 年会议记录：人类语言技术，第 1 卷（长论文和短论文），第 4171-4186 页，明尼苏达州明尼阿波利斯，2019 年 6 月。计算语言学协会。 doi：10.18653/v1/N19-1423。网址https://aclanthology.org/N19-1423/。谢扎德·杜利亚瓦拉、伦纳德·阿道夫、拉贾什·达斯和姆林玛雅·萨尚。大规模校准机器阅读系统。

### 段落 313 · Page 40

**EN**

In Smaranda Muresan, Preslav Nakov, and Aline Villavicencio (eds.),Findings of the Association for Computational Linguistics: ACL 2022, pp. 1682–1693, Dublin, Ireland, May 2022. Association for Computational Linguistics. doi: 10.18653/v1/2022.findings-acl.133. URL https://aclanthology.org/2022.findings-acl.133/. Qian Dong, Yiding Liu, Suqi Cheng, Shuaiqiang Wang, Zhicong Cheng, Shuzi Niu, and Dawei Yin. Incorporating explicit knowledge in pre-trained language models for passage re-ranking.Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval, 2022a.

**中文**

Smaranda Muresan、Preslav Nakov 和 Aline Villavicencio（编辑），计算语言学协会的调查结果：ACL 2022，第 1682–1693 页，爱尔兰都柏林，2022 年 5 月。计算语言学协会。 doi：10.18653/v1/2022.findings-acl.133。网址 https://aclanthology.org/2022.findings-acl.133/。董干，刘一丁，程苏奇，王帅强，程志聪，牛树子，尹大伟。将显性知识纳入预先训练的语言模型中以进行段落重新排序。第 45 届国际 ACM SIGIR 信息检索研究与发展会议论文集，2022a。

### 段落 314 · Page 40

**EN**

Qian Dong, Shuzi Niu, Tao Yuan, and Yucheng Li. Disentangled graph recurrent network for document ranking.Data Science and Engineering, 7:30 – 43, 2022b. SusanT.Dumais, ToddA.Letsche, MichaelL.Littman, andThomasK.Landauer. Automaticcross-language retrieval using latent semantic indexing. InAAAI Spring Symposium on Cross-Language Text and Speech Retrieval, volume 15, pp. 21, 1997. Darren Edge, Ha Trinh, Newman Cheng, Joshua Bradley, Alex Chao, Apurva Mody, Steven Truitt, Dasha Metropolitansky, Robert Osazuwa Ness, and Jonathan Larson.

**中文**

董干，牛树子，袁涛，李玉成。用于文档排名的解缠结图循环网络。数据科学与工程，7:30 – 43，2022b。苏珊·T·杜迈斯、托德·A·莱切、迈克尔·L·利特曼和托马斯·K·兰道尔。使用潜在语义索引的自动跨语言检索。 InAAAI 跨语言文本和语音检索春季研讨会，第 15 卷，第 21 页，1997 年。Darren Edge、Ha Trinh、Newman Cheng、Joshua Bradley、Alex Chao、Apurva Mody、Steven Truitt、Dasha Metropolitansky、Robert Osazuwa Ness 和 Jonathan Larson。

### 段落 315 · Page 40

**EN**

From local to global: A graph RAG approach to query-focused summarization.arXiv preprint arXiv:2404.16130, 2025. 40

**中文**

从局部到全局：以查询为中心的摘要的图 RAG 方法。arXiv 预印本 arXiv:2404.16130, 2025. 40

### Page 41

### 段落 316 · Page 41

**EN**

Published in Transactions on Machine Learning Research (02/2026) Nelson Elhage, Neel Nanda, Catherine Olsson, Tom Henighan, Nicholas Joseph, Ben Mann, Amanda Askell, Yuntao Bai, Anna Chen, Tom Conerly, Nova DasSarma, Dawn Drain, Deep Ganguli, Zac Hatfield-Dodds, Danny Hernandez, Andy Jones, Jackson Kernion, Liane Lovitt, Kamal Ndousse, Dario Amodei, Tom Brown, Jack Clark, Jared Kaplan, Sam McCandlish, and Chris Olah. A mathematical framework for transformer circuits.Transformer Circuits Thread, 2021. URLhttps://transformer-circuits.pub/ 2021/framework/index.html. Adel Elmahdy, Sheng-Chieh Lin, and Amin Ahmad.

**中文**

发表于《机器学习研究汇刊》(02/2026) Nelson Elhage、Neel Nanda、Catherine Olsson、Tom Henighan、Nicholas Joseph、Ben Mann、Amanda Askell、Yuntao Bai、Anna Chen、Tom Conerly、Nova DasSarma、Dawn Drain、Deep Ganguli、Zac Hatfield-Dodds、Danny Hernandez、Andy Jones、Jackson Kernion、Liane洛维特、卡迈勒·恩杜斯、达里奥·阿莫代、汤姆·布朗、杰克·克拉克、贾里德·卡普兰、山姆·麦坎德利什和克里斯·奥拉。Transformer电路的数学框架。Transformer Circuits Thread，2021。URLhttps://transformer- Circuits.pub/2021/framework/index.html。阿德尔·埃尔马迪、林胜杰和阿明·艾哈迈德。

### 段落 317 · Page 41

**EN**

Synergistic approach for simultaneous optimization of monolingual, cross-lingual, and multilingual information retrieval.arXiv preprint arXiv:2408.10536, 2024. Jeffrey L. Elman. Finding structure in time.Cognitive Science, 14(2):179–211, 1990. doi: 10.1016/ 0364-0213(90)90002-E. Guglielmo Faggioli, Laura Dietz, Charles L. A. Clarke, Gianluca Demartini, Matthias Hagen, Claudia Hauff, Noriko Kando, Evangelos Kanoulas, Martin Potthast, Benno Stein, et al. Perspectives on large language models for relevance judgment. InProceedings of the 2023 ACM SIGIR International Conference on Theory of Information Retrieval, pp. 39–50, 2023.

**中文**

同时优化单语、跨语言和多语言信息检索的协同方法。arXiv 预印本 arXiv:2408.10536, 2024。Jeffrey L. Elman。寻找时间结构。认知科学，14(2):179–211, 1990。doi: 10.1016/ 0364-0213(90)90002-E。 Guglielmo Faggioli、Laura Dietz、Charles L. A. Clarke、Gianluca Demartini、Matthias Hagen、Claudia Hauff、Noriko Kando、Evangelos Kanoulas、Martin Potthast、Benno Stein 等。对相关性判断的大语言模型的看法。 2023 年 ACM SIGIR 信息检索理论国际会议论文集，第 39-50 页，2023 年。

### 段落 318 · Page 41

**EN**

Guglielmo Faggioli, Laura Dietz, Charles L. A. Clarke, Gianluca Demartini, Matthias Hagen, Claudia Hauff, NorikoKando, EvangelosKanoulas, MartinPotthast, BennoStein, etal. Whodetermineswhatisrelevant? humans or AI? why not both?Communications of the ACM, 67(4):31–34, 2024. Han Fang, Pengfei Xiong, Luhui Xu, and Yu Chen. CLIP2Video: Mastering video-text retrieval via image CLIP.ArXiv preprint arXiv:2106.11097, 2021. Yan Fang, Jingtao Zhan, Qingyao Ai, Jiaxin Mao, Weihang Su, Jia Chen, and Yiqun Liu. Scaling laws for dense retrieval.

**中文**

Guglielmo Faggioli、Laura Dietz、Charles L. A. Clarke、Gianluca Demartini、Matthias Hagen、Claudia Hauff、NorikoKando、EvangelosKanoulas、MartinPotthast、BennoStein 等。谁决定什么是相关的？人类还是人工智能？为什么不两者都呢？ACM 通讯，67(4):31–34, 2024。韩芳、熊鹏飞、徐鲁辉和陈宇。 CLIP2Video：通过图像掌握视频文本检索 CLIP.ArXiv 预印本 arXiv:2106.11097, 2021。Yan Fang、Jingtao Zhan、Qingyao Ai、Jiaxin Mao、Weihang Su、Jia Chen 和 Yiqun Liu。密集检索的缩放法则。

### 段落 319 · Page 41

**EN**

InProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 1339–1349, 2024. Manuel Faysse, Hugues Sibille, Tony Wu, Bilel Omrani, Gautier Viaud, Céline Hudelot, and Pierre Colombo. ColPali: Efficient document retrieval with vision language models.arXiv preprint arXiv:2407.01449, 2025. Fangxiaoyu Feng, Yinfei Yang, Daniel Cer, Naveen Arivazhagan, and Wei Wang. Language-agnostic BERT sentence embedding. In Smaranda Muresan, Preslav Nakov, and Aline Villavicencio (eds.),Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp.

**中文**

第 47 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 1339-1349 页，2024 年。Manuel Faysse、Hugues Sibille、Tony Wu、Bilel Omrani、Gautier Viaud、Céline Hudelot 和 Pierre Colombo。 ColPali：使用视觉语言模型进行高效文档检索。arXiv 预印本 arXiv：2407.01449，2025。Fangxiaoyu Feng、Yinfei Yang、Daniel Cer、Naveen Arivazhagan 和 Wei Wang。与语言无关的 BERT 句子嵌入。 Smaranda Muresan、Preslav Nakov 和 Aline Villavicencio（编辑），计算语言学协会第 60 届年会论文集（第一卷：长论文），第 173 页。

### 段落 320 · Page 41

**EN**

878–891, Dublin, Ireland, May 2022. Association for Computational Linguistics. doi: 10.18653/v1/2022. acl-long.62. URLhttps://aclanthology.org/2022.acl-long.62/. Maxim Fishman, Brian Chmiel, Ron Banner, and Daniel Soudry. Scaling fp8 training to trillion-token LLMs. arXiv preprint arXiv:2409.12517, 2024. Christian Fluhr, Robert E. Frederking, Doug Oard, Akitoshi Okumura, Kai Ishikawa, and Kenji Satoh. Multilingual (or cross-lingual) information retrieval.Proceedings of the Multilingual Information Management: Current Levels and Future Abilities, pp. 10–13, 1999. Thibault Formal, Carlos Lassance, Benjamin Piwowarski, and Stéphane Clinchant.

**中文**

878–891，爱尔兰都柏林，2022 年 5 月。计算语言学协会。 doi：10.18653/v1/2022。 acl-long.62。网址https://aclanthology.org/2022.acl-long.62/。马克西姆·菲什曼、布莱恩·奇米尔、罗恩·班纳和丹尼尔·苏德里。将 FP8 训练扩展到万亿代币的 LLM。 arXiv 预印本 arXiv：2409.12517，2024。Christian Fluhr、Robert E. Frederking、Doug Oard、Akitoshi Okumura、Kai Ishikawa 和 Kenji Satoh。多语言（或跨语言）信息检索。多语言信息管理论文集：当前水平和未来能力，第 10-13 页，1999 年。Thibault Formal、Carlos Lassance、Benjamin Piwowarski 和 Stéphane Clinchant。

### 段落 321 · Page 41

**EN**

SPLADE v2: Sparse lexical and expansion model for information retrieval.arXiv preprint arXiv:2109.10086, 2021a. Thibault Formal, Benjamin Piwowarski, and Stéphane Clinchant. SPLADE: Sparse lexical and expansion model for 1st stage ranking. InProceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 2288–2292, New York, NY, USA, 2021b. Association for Computing Machinery. doi: 10.1145/3404835.3463098. Thibault Formal, Stéphane Clinchant, Hervé Déjean, and Carlos Lassance. SPLATE: Sparse late interaction retrieval.

**中文**

SPLADE v2：用于信息检索的稀疏词汇和扩展模型。arXiv 预印本 arXiv：2109.10086，2021a。蒂博·福尔莫尔、本杰明·皮沃瓦尔斯基和斯特凡·克林尚。 SPLADE：第一阶段排名的稀疏词汇和扩展模型。第 44 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 2288-2292 页，美国纽约州纽约市，2021 年 b。计算机器协会。号码：10.1145/3404835.3463098。 Thibault Formal、Stéphane Clinchant、Hervé Déjean 和 Carlos Lassance。 SPLATE：稀疏后期交互检索。

### 段落 322 · Page 41

**EN**

InProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 2635–2640, 2024. doi: 10.1145/3626772.3657968. YoavFreundandRobertESchapire. Adesicion-theoreticgeneralizationofon-linelearningandanapplication to boosting. InEuropean Conference on Computational Learning Theory, pp. 23–37. Springer, 1995. 41

**中文**

第 47 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 2635–2640 页，2024 年。doi：10.1145/3626772.3657968。约夫·弗罗因德和罗伯特·沙皮尔。在线学习的决策理论概括及其在提升中的应用。欧洲计算学习理论会议，第 23-37 页。施普林格，1995。41

### Page 42

### 段落 323 · Page 42

**EN**

Published in Transactions on Machine Learning Research (02/2026) Yoav Freund, Raj Iyer, Robert E. Schapire, and Yoram Singer. An efficient boosting algorithm for combining preferences.Journal of machine learning research, 4:933–969, 2003. Jerome H. Friedman. Greedy function approximation: a gradient boosting machine.Annals of statistics, pp. 1189–1232, 2001. Andrea Frome, Greg S Corrado, Jon Shlens, Samy Bengio, Jeff Dean, Marc'Aurelio Ranzato, and Tomas Mikolov. DeViSE: A deep visual-semantic embedding model. In C.J. Burges, L. Bottou, M. Welling, Z. Ghahramani, and K.Q.

**中文**

发表于机器学习研究汇刊 (02/2026) Yoav Freund、Raj Iyer、Robert E. Schapire 和 Yoram Singer。一种用于组合偏好的有效提升算法。机器学习研究杂志，4:933–969, 2003。Jerome H. Friedman。贪婪函数逼近：梯度增强机。统计年鉴，第 1189–1232 页，2001 年。Andrea Frome、Greg S Corrado、Jon Shlens、Samy Bengio、Jeff Dean、Marc'Aurelio Ranzato 和 Tomas Mikolov。 DeViSE：深度视觉语义嵌入模型。 C.J. Burges、L. Bottou、M. Welling、Z. Ghahramani 和 K.Q.

### 段落 324 · Page 42

**EN**

Weinberger (eds.),Advances in Neural Information Processing Systems, volume 26. Curran Associates, Inc., 2013. Dan Fu, Simran Arora, Jessica Grogan, Isys Johnson, Evan Sabri Eyuboglu, Armin Thomas, Benjamin Spector, Michael Poli, Atri Rudra, and Christopher Ré. Monarch Mixer: A simple sub-quadratic GEMMbased architecture.Advances in Neural Information Processing Systems, 36:77546–77603, 2023. Norbert Fuhr. Probabilistic models in information retrieval.The computer journal, 35(3):243–255, 1992. Valentin Gabeur, Chen Sun, Alahari Karteek, and Cordelia Schmid. Multi-modal transformer for video retrieval.arXiv preprint arXiv: 2007.10639, 2020.

**中文**

Weinberger（编辑），《神经信息处理系统进展》，第 26 卷。Curran Associates, Inc.，2013。Dan Fu、Simran Arora、Jessica Grogan、Isys Johnson、Evan Sabri Eyuboglu、Armin Thomas、Benjamin Spector、Michael Poli、Atri Rudra 和 Christopher Ré。 Monarch Mixer：一种简单的基于次二次 GEMM 的架构。神经信息处理系统的进展，36：77546–77603，2023。Norbert Fuhr。信息检索中的概率模型。计算机杂志，35(3):243–255, 1992。Valentin Gabeur、Chen Sun、Alahari Karteek 和 Cordelia Schmid。用于视频检索的多模态转换器。arXiv 预印本 arXiv：2007.10639，2020。

### 段落 325 · Page 42

**EN**

Luke Gallagher, Ruey-Cheng Chen, Roi Blanco, and J. Shane Culpepper. Joint optimization of cascade ranking models.Proceedings of the 12th ACM International Conference on Web Search and Data Mining, 2019. Jianfeng Gao, Patrick Pantel, Michael Gamon, Xiaodong He, and Li Deng. Modeling interestingness with deep neural networks. InProceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 2–13, 2014. Jiaxuan Gao, Wei Fu, Minyang Xie, Shusheng Xu, Chuyi He, Zhiyu Mei, Banghua Zhu, and Yi Wu. Beyond ten turns: Unlocking long-horizon agentic search with large-scale asynchronous rl, 2025.

**中文**

Luke Gallagher、Ruey-Cheng Chen、Roi Blanco 和 J. Shane Culpepper。级联排名模型的联合优化。第12届ACM网络搜索与数据挖掘国际会议论文集，2019。Jianfeng Gau，Patrick Pantel，Michael Gamon，Xiaodong He，Li Deng。使用深度神经网络对兴趣度进行建模。 2014 年自然语言处理经验方法会议 (EMNLP) 论文集，第 2-13 页，2014 年。Jiaxuan Gau、Wei Fu、Minyang Xie、Shusheng Xu、Chuyi He、Zhiyu Mei、Banghua Zhu 和 Yi Wu。超越十转：通过大规模异步强化学习解锁长视野代理搜索，2025 年。

### 段落 326 · Page 42

**EN**

URLhttps: //arxiv.org/abs/2508.07976. Luyu Gao and Jamie Callan. Condenser: a pre-training architecture for dense retrieval. In Marie-Francine Moens, Xuanjing Huang, Lucia Specia, and Scott Wen-tau Yih (eds.),Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing, pp. 981–993, Online and Punta Cana, Dominican Republic, November 2021. Association for Computational Linguistics. doi: 10.18653/v1/2021.emnlp-main. 75. URLhttps://aclanthology.org/2021.emnlp-main.75/. Luyu Gao and Jamie Callan.

**中文**

网址https://arxiv.org/abs/2508.07976。高鲁豫和杰米·卡兰。 Condenser：用于密集检索的预训练架构。收录于 Marie-Francine Moens、Xuanjing Huang、Lucia Specia 和 Scott Wen-tau Yih（编辑），2021 年自然语言处理经验方法会议论文集，第 981-993 页，在线和多米尼加共和国蓬塔卡纳，2021 年 11 月。计算语言学协会。 doi：10.18653/v1/2021.emnlp-main。 75.网址https://aclanthology.org/2021.emnlp-main.75/。高鲁豫和杰米·卡兰。

### 段落 327 · Page 42

**EN**

Long document re-ranking with modular re-ranker.Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval, 2022. Luyu Gao, Zhuyun Dai, and Jamie Callan. Understanding BERT rankers under distillation. InProceedings of the 2020 ACM SIGIR on International Conference on Theory of Information Retrieval, pp. 149–152, 2020. Luyu Gao, Zhuyun Dai, and Jamie Callan. COIL: Revisit exact lexical match in information retrieval with contextualized inverted list.

**中文**

使用模块化重新排序器对长文档进行重新排序。第 45 届国际 ACM SIGIR 信息检索研究与开发会议论文集，2022 年。Luyu Gau、Zhuyun Dai 和 Jamie Callan。了解蒸馏下的 BERT 排序器。 2020 年 ACM SIGIR 信息检索理论国际会议论文集，第 149-152 页，2020 年。Luyu Gau、Zhuyun Dai 和 Jamie Callan。 COIL：使用上下文倒排列表重新审视信息检索中的精确词汇匹配。

### 段落 328 · Page 42

**EN**

In Kristina Toutanova, Anna Rumshisky, Luke Zettlemoyer, Dilek Hakkani-Tur, Iz Beltagy, Steven Bethard, Ryan Cotterell, Tanmoy Chakraborty, and Yichao Zhou (eds.), Proceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, pp. 3030–3042, Online, June 2021a. Association for Computational Linguistics. doi: 10.18653/v1/2021.naacl-main.241. URLhttps://aclanthology.org/2021. naacl-main.241/. Tianyu Gao, Xingcheng Yao, and Danqi Chen. SimCSE: Simple contrastive learning of sentence embeddings.

**中文**

载于 Kristina Toutanova、Anna Rumshisky、Luke Zettlemoyer、Dilek Hakkani-Tur、Iz Beltagy、Steven Bethard、Ryan Cotterell、Tanmoy Chakraborty 和 Yichao Zhou（编），计算语言学协会北美分会 2021 年会议记录：人类语言技术，第 3030-3042 页，在线，2021 年 6 月a。计算语言学协会。 doi：10.18653/v1/2021.naacl-main.241。网址https://aclanthology.org/2021。 naacl-main.241/。高天宇、姚兴成、陈丹琪。 SimCSE：句子嵌入的简单对比学习。

### 段落 329 · Page 42

**EN**

In Marie-Francine Moens, Xuanjing Huang, Lucia Specia, and Scott Wen-tau Yih (eds.),Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing, pp. 6894–6910, Online and Punta Cana, Dominican Republic, November 2021b. Association for Computational Linguistics. doi: 10.18653/v1/2021.emnlp-main.552. URLhttps://aclanthology.org/2021.emnlp-main.552/. 42

**中文**

收录于 Marie-Francine Moens、Xuanjing Huang、Lucia Specia 和 Scott Wen-tau Yih（编辑），2021 年自然语言处理经验方法会议论文集，第 6894-6910 页，在线和多米尼加共和国蓬塔卡纳，2021 年 11 月b。计算语言学协会。 doi：10.18653/v1/2021.emnlp-main.552。网址https://aclanthology.org/2021.emnlp-main.552/。 42

### Page 43

### 段落 330 · Page 43

**EN**

Published in Transactions on Machine Learning Research (02/2026) Yunfan Gao, Yun Xiong, Xinyu Gao, Kangxiang Jia, Jinliu Pan, Yuxi Bi, Yi Dai, Jiawei Sun, and Haofen Wang. Retrieval-augmented generation for large language models: A survey.arXiv preprint arXiv:2312.10997, 2023. Gemini Team Google, Rohan Anil, Sebastian Borgeaud, Jean-Baptiste Alayrac, Jiahui Yu, Radu Soricut, Johan Schalkwyk, Andrew M. Dai, Anja Hauth, Katie Millican, et al. Gemini: A family of highly capable multimodal models.arXiv preprint arXiv:2312.11805, 2023.

**中文**

发表于《机器学习研究汇刊》(02/2026) Yunfan Gau、Yun Xiong、Xinyu Gau、Kangxiang Jia、Jinliu Pan、Yuxi Bi、Yi Dai、Jiawei Sun 和 Haofen Wang。大型语言模型的检索增强生成：一项调查。arXiv 预印本 arXiv:2312.10997, 2023。Gemini 团队 Google、Rohan Anil、Sebastian Borgeaud、Jean-Baptiste Alayrac、Jiahui Yu、Radu Soricut、Johan Schalkwyk、Andrew M. Dai、Anja Hauth、Katie Millican 等。 Gemini：一系列高性能多模式模型。arXiv 预印本 arXiv：2312.11805，2023。

### 段落 331 · Page 43

**EN**

Rohit Girdhar, Alaaeldin El-Nouby, Zhuang Liu, Mannat Singh, Kalyan Vasudev Alwala, Armand Joulin, and Ishan Misra. ImageBind one embedding space to bind them all.2023 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), pp. 15180–15190, 2023. Yunchao Gong, Qifa Ke, Michael Isard, and Svetlana Lazebnik. A multi-view embedding space for modeling internet images, tags, and their semantics.International journal of computer vision, 106(2):210–233, 2014. Google. Grounding with google search.https://ai.google.dev/gemini-api/docs/grounding?lang= python, 2024.

**中文**

Rohit Girdhar、Alaaeldin El-Nouby、Zhuang Liu、Mannat Singh、Kalyan Vasudev Alwala、Armand Joulin 和 Ishan Misra。 ImageBind 一个嵌入空间将它们全部绑定。2023 年 IEEE/CVF 计算机视觉和模式识别会议 (CVPR)，第 15180–15190 页，2023 年。Yunchao Kong、Qifa Ke、Michael Isard 和 Svetlana Lazebnik。用于建模互联网图像、标签及其语义的多视图嵌入空间。国际计算机视觉杂志，106(2):210–233, 2014。谷歌。以谷歌搜索为基础。https://ai.google.dev/gemini-api/docs/grounding?lang= python, 2024。

### 段落 332 · Page 43

**EN**

Satya Krishna Gorti, Noël Vouitsis, Junwei Ma, Keyvan Golestan, Maksims Volkovs, Animesh Garg, and Guangwei Yu. X-Pool: Cross-modal language-video attention for text-video retrieval.2022 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), pp. 4996–5005, 2022. Koustava Goswami, Sourav Dutta, Haytham Assem, Theodorus Fransen, and John P. McCrae. Crosslingual sentence embedding using multi-task learning. In Marie-Francine Moens, Xuanjing Huang, Lucia Specia, and Scott Wen-tau Yih (eds.),Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing, pp.

**中文**

Satya Krishna Gorti、Noël Vouitsis、Junwei Ma、Keyvan Golestan、Maksims Volkovs、Animesh Garg 和Guangwei Yu。 X-Pool：用于文本视频检索的跨模态语言视频注意力。2022 年 IEEE/CVF 计算机视觉和模式识别会议 (CVPR)，第 4996–5005 页，2022 年。Koustava Goswami、Sourav Dutta、Haytham Assem、Theodorus Fransen 和 John P. McCrae。使用多任务学习的跨语言句子嵌入。收录于 Marie-Francine Moens、Xuanjing Huang、Lucia Specia 和 Scott Wen-tau Yih（编），《2021 年自然语言处理经验方法会议论文集》，第 174 页。

### 段落 333 · Page 43

**EN**

9099–9113, Online and Punta Cana, Dominican Republic, November 2021. Association for Computational Linguistics. doi: 10.18653/v1/2021.emnlp-main.716. URL https://aclanthology.org/2021.emnlp-main.716/. Jianping Gou, Baosheng Yu, Stephen J. Maybank, and Dacheng Tao. Knowledge distillation: A survey. International journal of computer vision, 129(6):1789–1819, 2021. Roksana Goworek, Olivia Macmillan-Scott, and Eda B. Özyiğit. Bridging language gaps: Advances in cross-lingual information retrieval with multilingual LLMs.arXiv preprint arXiv:2510.00908, 2025. AlbertGuandTriDao. Mamba: Linear-timesequencemodelingwithselectivestatespaces.

**中文**

9099–9113，在线和多米尼加共和国蓬塔卡纳，2021 年 11 月。计算语言学协会。 doi：10.18653/v1/2021.emnlp-main.716。网址 https://aclanthology.org/2021.emnlp-main.716/。苟建平、于宝胜、史蒂芬·J·梅班克和陶大成。知识蒸馏：一项调查。国际计算机视觉杂志，129(6)：1789–1819，2021。Roksana Goworek、Olivia Macmillan-Scott 和 Eda B. Özyiğit。弥合语言差距：多语言 LLM 的跨语言信息检索进展。arXiv 预印本 arXiv:2510.00908, 2025。AlbertGuandTriDao。 Mamba：具有选择性状态空间的线性时序建模。

### 段落 334 · Page 43

**EN**

In1st Conference on Language Modeling, 2024. Michael Günther, Jackmin Ong, Isabelle Mohr, Alaeddine Abdessalem, Tanguy Abel, Mohammad Kalim Akram, Susana Guzman, Georgios Mastrapas, Saba Sturua, Bo Wang, Maximilian Werk, Nan Wang, and Han Xiao. Jina Embeddings 2: 8192-token general-purpose text embeddings for long documents. arXiv preprint arXiv:2310.19923, 2024. Chuan Guo, Geoff Pleiss, Yu Sun, and Kilian Q. Weinberger. On calibration of modern neural networks. arXiv preprint arXiv:1706.04599, 2017. Daya Guo, Dejian Yang, Haowei Zhang, Junxiao Song, Ruoyu Zhang, Runxin Xu, Qihao Zhu, Shirong Ma, Peiyi Wang, Xiao Bi, et al.

**中文**

第一届语言建模会议，2024 年。Michael Günther、Jackmin Ong、Isabelle Mohr、Alaeddine Abdessalem、Tanguy Abel、Mohammad Kalim Akram、Susana Guzman、Georgios Mastrapas、Saba Sturua、Bo Wang、Maximilian Werk、Nan Wang 和 Han Xiao。 Jina Embeddings 2：8192 个令牌的长文档通用文本嵌入。 arXiv 预印本 arXiv:2310.19923, 2024。Chuanuo、Geoff Pleiss、Yu Sun 和 Kilian Q. Weinberger。现代神经网络的校准。 arXiv 预印本 arXiv:1706.04599, 2017。郭大亚、杨德建、张浩伟、宋俊晓、张若宇、徐润新、朱启浩、马世荣、王培毅、毕晓等。

### 段落 335 · Page 43

**EN**

DeepSeek-R1: Incentivizing reasoning capability in LLMs via reinforcement learning.arXiv preprint arXiv:2501.12948, 2025. Jiafeng Guo, Yixing Fan, Qingyao Ai, and W. Bruce Croft. A deep relevance matching model for ad-hoc retrieval. InProceedings of the 25th ACM International on Conference on Information and Knowledge Management, CIKM ’16, pp. 55–64, New York, NY, USA, 2016a. Association for Computing Machinery. doi: 10.1145/2983323.2983769. Jiafeng Guo, Yixing Fan, Qingyao Ai, and W. Bruce Croft. Semantic matching by non-linear word transportation for information retrieval.

**中文**

DeepSeek-R1：通过强化学习激励法学硕士的推理能力。arXiv 预印本 arXiv:2501.12948, 2025。JiafengGuo、YixingFan、QingyaoAi 和 W.BruceCroft。用于即席检索的深度相关性匹配模型。第 25 届 ACM 国际信息和知识管理会议论文集，CIKM ’16，第 55-64 页，美国纽约州纽约，2016a。计算机器协会。号码：10.1145/2983323.2983769。郭嘉峰、范宜兴、艾庆耀和 W. Bruce Croft。通过非线性词传输进行语义匹配以进行信息检索。

### 段落 336 · Page 43

**EN**

InProceedings of the 25th ACM International on Conference on Information and Knowledge Management, CIKM ’16, pp. 701–710, New York, NY, USA, 2016b. Association for Computing Machinery. doi: 10.1145/2983323.2983768. 43

**中文**

第 25 届 ACM 国际信息和知识管理会议论文集，CIKM '16，第 701-710 页，美国纽约州纽约，2016b。计算机器协会。号码：10.1145/2983323.2983768。 43

### Page 44

### 段落 337 · Page 44

**EN**

Published in Transactions on Machine Learning Research (02/2026) Jiafeng Guo, Yixing Fan, Liang Pang, Liu Yang, Qingyao Ai, Hamed Zamani, Chen Wu, W Bruce Croft, and Xueqi Cheng. A deep look into neural ranking models for information retrieval.Information Processing & Management, 57(6):102067, 2020. Ashim Gupta, Rishanth Rajendhran, Nathan Stringham, Vivek Srikumar, and Ana Marasovic. Whispers of doubt amidst echoes of triumph in NLP robustness.

**中文**

发表于《机器学习研究汇刊》(02/2026) Jiafenguo、Yixing Fan、Liang Pang、Liu Yang、Qingyao Ai、Hamed Zamani、Chen Wu、W Bruce Croft 和 Xueqi Cheng。深入研究信息检索的神经排序模型。信息处理与管理，57(6):102067, 2020。Ashim Gupta、Rishanth Rajendhran、Nathan Stringham、Vivek Srikumar 和 Ana Marasovic。在 NLP 鲁棒性的胜利回响中，质疑声不断。

### 段落 338 · Page 44

**EN**

In Kevin Duh, Helena Gomez, and Steven Bethard (eds.),Proceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers), pp. 5533–5590, Mexico City, Mexico, June 2024a. Association for Computational Linguistics. doi: 10.18653/v1/2024.naacl-long.310. URLhttps://aclanthology.org/2024.naacl-long.310/. Nilesh Gupta, Fnu Devvrit, Ankit Singh Rawat, Srinadh Bhojanapalli, Prateek Jain, and Inderjit S. Dhillon. Dual-encoders for extreme multi-label classification. InThe 12th International Conference on Learning Representations, 2024b.

**中文**

载于 Kevin Duh、Helena Gomez 和 Steven Bethard（编），计算语言学协会北美分会 2024 年会议记录：人类语言技术（第一卷：长论文），第 5533-5590 页，墨西哥墨西哥城，2024 年 6 月a。计算语言学协会。 doi：10.18653/v1/2024.naacl-long.310。网址https://aclanthology.org/2024.naacl-long.310/。 Nilesh Gupta、Fnu Devvrit、Ankit Singh Rawat、Srinadh Bhojanapalli、Prateek Jain 和 Inderjit S. Dhillon。用于极端多标签分类的双编码器。在第 12 届学习表征国际会议，2024b。

### 段落 339 · Page 44

**EN**

URLhttps://openreview.net/forum?id=dNe1T0Ahby. Suchin Gururangan, Ana Marasović, Swabha Swayamdipta, Kyle Lo, Iz Beltagy, Doug Downey, and Noah A. Smith. Don‘t stop pretraining: Adapt language models to domains and tasks. In Dan Jurafsky, Joyce Chai, Natalie Schluter, and Joel Tetreault (eds.),Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics, pp. 8342–8360, Online, July 2020. Association for Computational Linguistics. doi: 10.18653/v1/2020.acl-main.740. URLhttps://aclanthology.org/2020.acl-main.740/. Michael U. Gutmann and Aapo Hyvärinen.

**中文**

网址https://openreview.net/forum?id=dNe1T0Ahby。 Suchin Gururangan、Ana Marasović、Swabha Swayamdipta、Kyle Lo、Iz Beltagy、Doug Downey 和 Noah A. Smith。不要停止预训练：使语言模型适应领域和任务。载于 Dan Jurafsky、Joyce Chai、Natalie Schluter 和 Joel Tetreault（编辑），计算语言学协会第 58 届年会论文集，第 8342-8360 页，在线，2020 年 7 月。计算语言学协会。 doi：10.18653/v1/2020.acl-main.740。网址https://aclanthology.org/2020.acl-main.740/。迈克尔·U·古特曼 (Michael U. Gutmann) 和阿波·海瓦里宁 (Aapo Hyvärinen)。

### 段落 340 · Page 44

**EN**

Noise-contrastive estimation of unnormalized statistical models, with applications to natural image statistics.The journal of machine learning research, 13(1):307–361, 2012. Kelvin Guu, Kenton Lee, Zora Tung, Panupong Pasupat, and Mingwei Chang. Retrieval augmented language model pre-training. InInternational Conference on Machine Learning, pp. 3929–3938. PMLR, 2020. David Ha, Andrew M. Dai, and Quoc V. Le. Hypernetworks. InInternational Conference on Learning Representations, 2022. Hua He, Kevin Gimpel, and Jimmy Lin. Multi-perspective sentence similarity modeling with convolutional neural networks.

**中文**

非归一化统计模型的噪声对比估计及其在自然图像统计中的应用。机器学习研究杂志，13(1):307–361, 2012。Kelvin Guu、Kenton Lee、Zora Tung、Panupong Pasupat 和 Mingwei Chang。检索增强语言模型预训练。国际机器学习会议，第 3929-3938 页。 PMLR，2020。David Ha、Andrew M. Dai 和 Quoc V. Le。超网络。学习表征国际会议，2022 年。Hua He、Kevin Gimpel 和 Jimmy Lin。使用卷积神经网络的多视角句子相似度建模。

### 段落 341 · Page 44

**EN**

In Lluís Màrquez, Chris Callison-Burch, and Jian Su (eds.),Proceedings of the 2015 Conference on Empirical Methods in Natural Language Processing, pp. 1576–1586, Lisbon, Portugal, September 2015. Association for Computational Linguistics. doi: 10.18653/v1/D15-1181. URL https://aclanthology.org/D15-1181/. Yichen He, Guanhua Huang, Peiyuan Feng, Yuan Lin, Yuchen Zhang, Hang Li, et al. PaSa: An LLM agent for comprehensive academic paper search.arXiv preprint arXiv:2501.10120, 2025. Zhankui He, Zhouhang Xie, Harald Steck, Dawen Liang, Rahul Jha, Nathan Kallus, and Julian McAuley.

**中文**

载于 Lluís Màrquez、Chris Callison-Burch 和Jian Su（编），2015 年自然语言处理经验方法会议论文集，第 1576-1586 页，葡萄牙里斯本，2015 年 9 月。计算语言学协会。 doi：10.18653/v1/D15-1181。网址 https://aclanthology.org/D15-1181/。何一尘，黄冠华，冯培源，林渊，张雨辰，李航，等。 PaSa：综合学术论文检索的法学硕士代理。arXiv 预印本 arXiv:2501.10120, 2025。Zhankui He、Zhouhang Xie、Harald Steck、Dawen Liang、Rahul Jha、Nathan Kallus 和 Julian McAuley。

### 段落 342 · Page 44

**EN**

Reindex-then-adapt: Improving large language models for conversational recommendation.Proceedings of the 18th ACM International Conference on Web Search and Data Mining, 2024. Djoerd Hiemstra and Wessel Kraaij. Twenty-one at TREC-7: Ad-hoc and cross-language track. In7th Text REtrieval Conference, TREC-7 1998, pp. 227–238. National Institute of Standards and Technology, 1999. Geoffrey Hinton, Oriol Vinyals, and Jeff Dean. Distilling the knowledge in a neural network.stat, 1050:9, 2015. S. Hochreiter and J. Schmidhuber. Long short-term memory.Neural Computation MIT-Press, 1997.

**中文**

Reindex-then-adapt：改进会话推荐的大型语言模型。第 18 届 ACM 国际网络搜索和数据挖掘会议论文集，2024 年。Djoerd Hiemstra 和 Wessel Kraaij。 TREC-7 的二十一：临时和跨语言轨道。第七届文本检索会议，TREC-7 1998，第 227-238 页。美国国家标准与技术研究所，1999 年。Geoffrey Hinton、Oriol Vinyals 和 Jeff Dean。在神经网络中提炼知识。stat，1050:9，2015。S. Hochreiter 和 J. Schmidhuber。长短期记忆。神经计算麻省理工学院出版社，1997 年。

### 段落 343 · Page 44

**EN**

Jordan Hoffmann, Sebastian Borgeaud, Arthur Mensch, Elena Buchatskaya, Trevor Cai, Eliza Rutherford, Diego de Las Casas, Lisa Anne Hendricks, Johannes Welbl, Aidan Clark, et al. Training compute-optimal large language models.arXiv preprint arXiv:2203.15556, 2022. Sebastian Hofstätter, Sophia Althammer, Michael Schröder, Mete Sertkan, and Allan Hanbury. Improving efficient neural ranking models with cross-architecture knowledge distillation.arXiv preprint arXiv:2010.02666, 2020a. 44

**中文**

乔丹·霍夫曼、塞巴斯蒂安·博尔若、阿瑟·门施、埃琳娜·布查茨卡娅、特雷弗·蔡、伊丽莎·卢瑟福、迭戈·德拉斯·卡萨斯、丽莎·安妮·亨德里克斯、约翰内斯·韦尔布尔、艾丹·克拉克等。训练计算最优的大型语言模型。arXiv 预印本 arXiv：2203.15556，2022。Sebastian Hofstätter、Sophia Althammer、Michael Schröder、Mete Sertkan 和 Allan Hanbury。通过跨架构知识蒸馏改进高效的神经排序模型。arXiv 预印本 arXiv:2010.02666, 2020a。 44

### Page 45

### 段落 344 · Page 45

**EN**

Published in Transactions on Machine Learning Research (02/2026) Sebastian Hofstätter, Hamed Zamani, Bhaskar Mitra, Nick Craswell, and Allan Hanbury. Local self-attention over long text for efficient document retrieval. InProceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 2021–2024, 2020b. Sebastian Hofstätter, Markus Zlabinger, and Allan Hanbury. Interpretable & time-budget-constrained contextualization for re-ranking. InECAI 2020, pp. 513–520. IOS Press, 2020c. Sebastian Hofstätter, Sheng-Chieh Lin, Jheng-Hong Yang, Jimmy Lin, and Allan Hanbury.

**中文**

发表于机器学习研究汇刊 (02/2026) Sebastian Hofstätter、Hamed Zamani、Bhaskar Mitra、Nick Craswell 和 Allan Hanbury。对长文本进行本地自注意力，以实现高效的文档检索。第 43 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 2021-2024 页，2020b。塞巴斯蒂安·霍夫斯塔特、马库斯·兹拉宾格和艾伦·汉伯里。可解释且时间预算受限的重排情境化。 InECAI 2020，第 513-520 页。 IOS 出版社，2020c。塞巴斯蒂安·霍夫斯塔特、林胜杰、杨正宏、林吉米和艾伦·汉伯里。

### 段落 345 · Page 45

**EN**

Efficiently teaching an effective dense retriever with balanced topic aware sampling. InProceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 113– 122, 2021a. Sebastian Hofstätter, Bhaskar Mitra, Hamed Zamani, Nick Craswell, and Allan Hanbury. Intra-document cascading: Learning to select passages for neural document ranking.Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, 2021b. Sebastian Hofstätter, Omar Khattab, Sophia Althammer, Mete Sertkan, and Allan Hanbury.

**中文**

通过平衡的主题感知采样有效地教授有效的密集检索器。第 44 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 113-122 页，2021a。塞巴斯蒂安·霍夫斯塔特、巴斯卡·米特拉、哈米德·扎马尼、尼克·克拉斯韦尔和艾伦·汉伯里。文档内级联：学习选择神经文档排序的段落。第 44 届国际 ACM SIGIR 信息检索研究与发展会议论文集，2021b。塞巴斯蒂安·霍夫斯塔特、奥马尔·哈塔布、索菲亚·阿尔萨默、梅特·塞特坎和艾伦·汉伯里。

### 段落 346 · Page 45

**EN**

Introducing neural bag of whole-words with ColBERTer: Contextualized late interactions using enhanced reduction. InProceedings of the 31st ACM International Conference on Information & Knowledge Management, pp. 737–747, 2022. Harold Hotelling. Relations between two sets of variates. InBreakthroughs in Statistics: Methodology and Distribution, pp. 162–190. Springer, 1992. Jeremy Howard and Sebastian Ruder. Universal language model fine-tuning for text classification.arXiv preprint arXiv:1801.06146, 2018. Baotian Hu, Zhengdong Lu, Hang Li, and Qingcai Chen. Convolutional neural network architectures for matching natural language sentences.

**中文**

使用 ColBERTer 引入全词神经包：使用增强还原进行上下文化后期交互。第 31 届 ACM 国际信息与知识管理会议论文集，第 737-747 页，2022 年。Harold Hotelling。两组变量之间的关系。统计突破：方法论和分布，第 162-190 页。施普林格，1992 年。杰里米·霍华德和塞巴斯蒂安·鲁德。用于文本分类的通用语言模型微调。arXiv 预印本 arXiv:1801.06146, 2018。Baotian Hu、Zhengdong Lu、Hang Li 和 Qingcai Chen。用于匹配自然语言句子的卷积神经网络架构。

### 段落 347 · Page 45

**EN**

InProceedings of the 28th International Conference on Neural Information Processing Systems - Volume 2, NIPS’14, pp. 2042–2050, Cambridge, MA, USA, 2014. MIT Press. Mengkang Hu, Yuhang Zhou, Wendong Fan, Yuzhou Nie, Bowei Xia, Tao Sun, Ziyu Ye, Zhaoxuan Jin, Yingru Li, Qiguang Chen, et al. OWL: Optimized workforce learning for general multi-agent assistance in real-world task automation.arXiv preprint arXiv:2505.23885, 2025. Ziniu Hu, Yang Wang, Qu Peng, and Hang Li. Unbiased LambdaMART: An unbiased pairwise learning-torank algorithm. InThe World Wide Web Conference, pp. 2830–2836, 2019.

**中文**

第 28 届神经信息处理系统国际会议论文集 - 第 2 卷，NIPS’14，第 2042–2050 页，美国马萨诸塞州剑桥，2014 年。麻省理工学院出版社。胡孟康，周宇航，范文东，聂宇周，夏博伟，孙涛，叶子宇，金兆轩，李英儒，陈其光，等。 OWL：优化劳动力学习，以实现现实世界任务自动化中的一般多智能体协助。arXiv 预印本 arXiv：2505.23885，2025。Ziniu Hu、Yang Wang、Qu Peng 和 Hang Li。无偏 LambdaMART：一种无偏的成对学习排序算法。 《万维网会议》，第 2830–2836 页，2019 年。

### 段落 348 · Page 45

**EN**

Jui-Ting Huang, Ashish Sharma, Shuying Sun, Li Xia, David Zhang, Philip Pronin, Janani Padmanabhan, Giuseppe Ottaviano, and Linjun Yang. Embedding-based retrieval in facebook search. InProceedings of the 26th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, pp. 2553–2561, 2020. Po-Sen Huang, Xiaodong He, Jianfeng Gao, Li Deng, Alex Acero, and Larry Heck. Learning deep structured semantic models for web search using clickthrough data. InProceedings of the 22nd ACM International Conference on Information & Knowledge Management, CIKM ’13, pp. 2333–2338, New York, NY, USA, 2013. Association for Computing Machinery.

**中文**

Jui-Ting Huang、Ashish Sharma、Shuying Sun、Li Xia、David 张、Philip Pronin、Janani Padmanabhan、Giuseppe Ottaviano 和 Linjun Yang。 Facebook 搜索中基于嵌入的检索。第 26 届 ACM SIGKDD 国际知识发现与数据挖掘会议论文集，第 2553-2561 页，2020 年。Po-Sen Huang、Xiaodong He、Jianfeng Gau、Li Deng、Alex Acero 和 Larry Heck。使用点击数据学习网络搜索的深度结构化语义模型。 InProceedings of the 22nd ACM International Conference on Information & Knowledge Management, CIKM '13, pp. 2333–2338, New York, NY, USA, 2013. 计算机协会。

### 段落 349 · Page 45

**EN**

doi: 10.1145/2505515.2505665. Xu Huang, Weiwen Liu, Xiaolong Chen, Xingmei Wang, Hao Wang, Defu Lian, Yasheng Wang, Ruiming Tang, and Enhong Chen. Understanding the planning of LLM agents: A survey.arXiv preprint arXiv:2402.02716, 2024a. Yuxuan Huang, Yihang Chen, Haozheng Zhang, Kang Li, Meng Fang, Linyi Yang, Xiaoguang Li, Lifeng Shang, Songcen Xu, Jianye Hao, et al. Deep research agents: A systematic examination and roadmap. arXiv preprint arXiv:2506.18096, 2025. 45

**中文**

号码：10.1145/2505515.2505665。黄旭、刘伟文、陈小龙、王星梅、王浩、连德福、王亚生、唐瑞明和陈恩宏。了解 LLM 代理的规划：调查.arXiv 预印本 arXiv:2402.02716, 2024a。黄宇轩，陈一航，张浩政，李康，方孟，杨林一，李晓光，尚立峰，徐松岑，郝建业，等。深度研究代理：系统检查和路线图。 arXiv 预印本 arXiv:2506.18096, 2025. 45

### Page 46

### 段落 350 · Page 46

**EN**

Published in Transactions on Machine Learning Research (02/2026) ZhiqiHuang, PuxuanYu, ShauliRavfogel, andJamesAllan. Languageconcepterasureforlanguage-invariant dense retrieval. In Yaser Al-Onaizan, Mohit Bansal, and Yun-Nung Chen (eds.),Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, pp. 13261–13273, Miami, Florida, USA, November 2024b. Association for Computational Linguistics. doi: 10.18653/v1/2024.emnlp-main.736. URLhttps://aclanthology.org/2024.emnlp-main.736/. Kai Hui, Andrew Yates, Klaus Berberich, and Gerard de Melo. PACRR: A position-aware neural IR model for relevance matching.

**中文**

发表在《机器学习研究汇刊》(02/2026) 上：ZhiqiHuang、PuxuanYu、ShauliRavfogel 和 JamesAllan。用于语言不变密集检索的语言概念擦除。载于 Yaser Al-Onaizan、Mohit Bansal 和 Yun-Nung Chen（编辑），2024 年自然语言处理经验方法会议论文集，第 13261–13273 页，美国佛罗里达州迈阿密，2024 年 11 月b。计算语言学协会。 doi：10.18653/v1/2024.emnlp-main.736。网址https://aclanthology.org/2024.emnlp-main.736/。凯惠、安德鲁·耶茨、克劳斯·贝尔贝里奇和杰拉德·德·梅洛。 PACRR：用于相关性匹配的位置感知神经 IR 模型。

### 段落 351 · Page 46

**EN**

In Martha Palmer, Rebecca Hwa, and Sebastian Riedel (eds.),Proceedings of the 2017 Conference on Empirical Methods in Natural Language Processing, pp. 1049–1058, Copenhagen, Denmark, September 2017. Association for Computational Linguistics. doi: 10.18653/v1/D17-1110. URL https://aclanthology.org/D17-1110/. Kai Hui, Andrew Yates, Klaus Berberich, and Gerard de Melo. Co-PACRR: A context-aware neural ir model for ad-hoc retrieval. InProceedings of the 11th ACM International Conference on Web Search and Data Mining, WSDM ’18, pp. 279–287, New York, NY, USA, 2018. Association for Computing Machinery. doi: 10.1145/3159652.3159689.

**中文**

玛莎·帕尔默 (Martha Palmer)、丽贝卡·华 (Rebecca Hwa) 和塞巴斯蒂安·里德尔 (Sebastian Riedel)（编辑），《2017 年自然语言处理经验方法会议论文集》，第 1049–1058 页，丹麦哥本哈根，2017 年 9 月。计算语言学协会。 doi：10.18653/v1/D17-1110。网址 https://aclanthology.org/D17-1110/。凯惠、安德鲁·耶茨、克劳斯·贝尔贝里奇和杰拉德·德·梅洛。 Co-PACRR：用于即席检索的上下文感知神经 IR 模型。第 11 届 ACM 国际网络搜索和数据挖掘会议论文集，WSDM ’18，第 279–287 页，美国纽约州纽约市，2018 年。计算机协会。号码：10.1145/3159652.3159689。

### 段落 352 · Page 46

**EN**

Samuel Humeau, Kurt Shuster, Marie-Anne Lachaux, and Jason Weston. Poly-encoders: Architectures and pre-training strategies for fast and accurate multi-sentence scoring. InInternational Conference on Learning Representations, 2020. URLhttps://openreview.net/forum?id=SkxgnnNFvH. Shayekh Bin Islam, Md Asib Rahman, K. S. M. Tozammel Hossain, Enamul Hoque, Shafiq Joty, and Md Rizwan Parvez. Open-RAG: Enhanced retrieval augmented reasoning with open-source large language models. In Yaser Al-Onaizan, Mohit Bansal, and Yun-Nung Chen (eds.),Findings of the Association for Computational Linguistics: EMNLP 2024, pp.

**中文**

塞缪尔·休莫、库尔特·舒斯特、玛丽-安妮·拉肖和杰森·韦斯顿。多编码器：用于快速准确的多句子评分的架构和预训练策略。在国际学习表征会议，2020。URLhttps://openreview.net/forum?id=SkxgnnNFvH。 Shayekh Bin Islam、Md Asib Rahman、K.S.M. Tozammel Hossain、Enamul Hoque、Shafiq Joty 和 Md Rizwan Parvez。 Open-RAG：使用开源大型语言模型增强检索增强推理。载于 Yaser Al-Onaizan、Mohit Bansal 和 Yun-Nung Chen（编辑），计算语言学协会的调查结果：EMNLP 2024，第 123 页。

### 段落 353 · Page 46

**EN**

14231–14244, Miami, Florida, USA, November 2024. Association for Computational Linguistics. doi: 10.18653/v1/2024.findings-emnlp.831. URLhttps:// aclanthology.org/2024.findings-emnlp.831/. Gautier Izacard and Edouard Grave. Leveraging passage retrieval with generative models for open domain question answering. In Paola Merlo, Jorg Tiedemann, and Reut Tsarfaty (eds.),Proceedings of the 16th Conference of the European Chapter of the Association for Computational Linguistics: Main Volume, pp. 874–880, Online, April 2021. Association for Computational Linguistics. doi: 10.18653/v1/2021.eacl-main. 74.

**中文**

14231–14244，美国佛罗里达州迈阿密，2024 年 11 月。计算语言学协会。 doi：10.18653/v1/2024.findings-emnlp.831。网址https://aclanthology.org/2024.findings-emnlp.831/。戈蒂埃·伊扎卡尔和爱德华·格雷夫。利用段落检索和生成模型进行开放域问答。见 Paola Merlo、Jorg Tiedemann 和 Reut Tsarfaty（编辑），计算语言学协会欧洲分会第 16 届会议论文集：主卷，第 874-880 页，在线，2021 年 4 月。计算语言学协会。 doi：10.18653/v1/2021.eacl-main。 74.

### 段落 354 · Page 46

**EN**

URLhttps://aclanthology.org/2021.eacl-main.74/. Alon Jacovi and Yoav Goldberg. Towards faithfully interpretable NLP systems: How should we define and evaluate faithfulness? In Dan Jurafsky, Joyce Chai, Natalie Schluter, and Joel Tetreault (eds.), Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics, pp. 4198–4205, Online, July 2020. Association for Computational Linguistics. doi: 10.18653/v1/2020.acl-main.386. URL https://aclanthology.org/2020.acl-main.386/. Himanshu Jain, Yashoteja Prabhu, and Manik Varma.

**中文**

网址https://aclanthology.org/2021.eacl-main.74/。阿隆·雅科维和约夫·戈德堡。迈向忠实可解释的 NLP 系统：我们应该如何定义和评估忠实度？载于 Dan Jurafsky、Joyce Chai、Natalie Schluter 和 Joel Tetreault（编辑），计算语言学协会第 58 届年会论文集，第 4198-4205 页，在线，2020 年 7 月。计算语言学协会。 doi：10.18653/v1/2020.acl-main.386。网址 https://aclanthology.org/2020.acl-main.386/。希曼舒·贾因 (Himanshu Jain)、雅舒特贾·帕布 (Yashoteja Prabhu) 和马尼克·瓦尔玛 (Manik Varma)。

### 段落 355 · Page 46

**EN**

Extreme multi-label loss functions for recommendation, tagging, ranking & other missing label applications. InProceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, pp. 935–944, 2016. Himanshu Jain, Venkatesh Balasubramanian, Bhanu Chunduri, and Manik Varma. Slice: Scalable linear extreme classifiers trained on 100 million labels for related searches. InProceedings of the 12th ACM International Conference on Web Search and Data Mining, pp. 528–536, 2019. doi: 10.1145/3289600. 3290979. Soroush Javdan, Pragash Krishnamoorthy, and Olga Baysal.

**中文**

用于推荐、标记、排名和其他缺失标签应用的极端多标签损失函数。第 22 届 ACM SIGKDD 国际知识发现和数据挖掘会议记录，第 935-944 页，2016 年。Himanshu Jain、Venkatesh Balasubramanian、Bhanu Chunduri 和 Manik Varma。 Slice：可扩展的线性极限分类器，经过 1 亿个标签的相关搜索训练。第 12 届 ACM 国际网络搜索和数据挖掘会议论文集，第 528-536 页，2019 年。doi：10.1145/3289600。 3290979。Soroush Javdan、Pragash Krishnamoorthy 和 Olga Baysal。

### 段落 356 · Page 46

**EN**

CREST: Improving interpretability and effectiveness of troubleshooting at ericsson through criterion-specific trouble report retrieval.arXiv preprint arXiv:2511.17417, 2025. Frederick Jelinek. Interpolated estimation of Markov source parameters from sparse data. InProceedings of Workshop on Pattern Recognition in Practice, 1980. Minbyul Jeong, Jiwoong Sohn, Mujeen Sung, and Jaewoo Kang. Improving medical reasoning through retrieval and self-reflection with retrieval-augmented large language models.Bioinformatics, 40 (Supplement_1):i119–i129, 2024. doi: 10.1093/bioinformatics/btae238. 46

**中文**

CREST：通过特定标准的故障报告检索提高爱立信故障排除的可解释性和有效性。arXiv 预印本 arXiv:2511.17417, 2025。Frederick Jelinek。从稀疏数据中插值估计马尔可夫源参数。模式识别实践研讨会论文集，1980 年。Minbyul Jeong、Jiwoong Sohn、Mujeen Sung 和 Jaewoo Kang。通过检索增强大语言模型的检索和自我反思来改进医学推理。生物信息学，40（补充_1）：i119–i129，2024。doi：10.1093/bioinformatics/btae238。 46

### Page 47

### 段落 357 · Page 47

**EN**

Published in Transactions on Machine Learning Research (02/2026) Chao Jia, Yinfei Yang, Ye Xia, Yi-Ting Chen, Zarana Parekh, Hieu Pham, Quoc V. Le, Yun-Hsuan Sung, Zhen Li, and Tom Duerig. Scaling up visual and vision-language representation learning with noisy text supervision. InInternational Conference on Machine Learning, 2021.

**中文**

发表于机器学习研究汇刊 (02/2026) Chao Jia、Yinfei Yang、Ye Xia、Yi-Ting Chen、Zarana Parekh、Hieu Pham、Quoc V. Le、Yun-Hsuan Sung、Zhen Li 和 Tom Duerig。通过嘈杂的文本监督扩大视觉和视觉语言表示学习。在国际机器学习会议，2021。

### 段落 358 · Page 47

**EN**

Albert Qiaochu Jiang, Alexandre Sablayrolles, Arthur Mensch, Chris Bamford, Devendra Singh Chaplot, Diego de Las Casas, Florian Bressand, Gianna Lengyel, Guillaume Lample, Lucile Saulnier, L’elio Renard Lavaud, Marie-Anne Lachaux, Pierre Stock, Teven Le Scao, Thibaut Lavril, Thomas Wang, Timothée Lacroix, and William El Sayed. Mistral 7B.arXiv preprint arXiv:2310.06825, 2023a. Zhengbao Jiang, Frank F. Xu, Luyu Gao, Zhiqing Sun, Qian Liu, Jane Dwivedi-Yu, Yiming Yang, Jamie Callan, and Graham Neubig. Active retrieval augmented generation. InProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, pp.

**中文**

Albert Qiaochu Jiang、Alexandre Sablayrolles、Arthur Mensch、Chris Bamford、Devendra Singh Chaplot、Diego de Las Casas、Florian Bressand、Gianna Lengyel、Guillaume Lample、Lucile Saulnier、L’elio Renard Lavaud、Marie-Anne Lachaux、Pierre Stock、Teven Le Scao、Thibaut Lavril、Thomas Wang、Timothée Lacroix 和 William埃尔·赛义德. Mistral 7B.arXiv 预印本 arXiv:2310.06825, 2023a。蒋正宝、Frank F. Xu、高鲁宇、孙志清、刘谦、Jane Dwivedi-Yu、Yiming Yang、Jamie Callan 和 Graham Neubig。主动检索增强了生成。 2023 年自然语言处理经验方法会议论文集，第 123 页。

### 段落 359 · Page 47

**EN**

7969–7992, 2023b. Bowen Jin, Hansi Zeng, Zhenrui Yue, Jinsung Yoon, Sercan Arik, Dong Wang, Hamed Zamani, and Jiawei Han. Search-R1: Training LLMs to reason and leverage search engines with reinforcement learning.arXiv preprint arXiv:2503.09516, 2025. Thorsten Joachims. Training linear SVMs in linear time. InProceedings of the 12th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, KDD ’06, pp. 217–226, New York, NY, USA, 2006. Association for Computing Machinery. doi: 10.1145/1150402.1150429. Thorsten Joachims, Adith Swaminathan, and Tobias Schnabel. Unbiased learning-to-rank with biased feedback.

**中文**

7969–7992, 2023b。 Bowen Jin、Hansi Zeng、Zhenrui Yue、Jinsung Yoon、Sercan Arik、Dong Wang、Hamed Zamani 和 Jiawei Han。 Search-R1：通过强化学习训练法学硕士推理和利用搜索引擎。arXiv 预印本 arXiv:2503.09516, 2025。Thorsten Joachims。在线性时间内训练线性 SVM。第 12 届 ACM SIGKDD 国际知识发现和数据挖掘会议记录，KDD ’06，第 217–226 页，美国纽约州纽约市，2006 年。计算机协会。 DOI：10.1145/1150402.1150429。托尔斯滕·约阿希姆斯、阿迪斯·斯瓦米纳坦和托比亚斯·施纳贝尔。无偏见的学习排名和有偏见的反馈。

### 段落 360 · Page 47

**EN**

InProceedings of the 10th ACM International Conference on Web Search and Data Mining, pp. 781–789, 2017. Jeff Johnson, Matthijs Douze, and Hervé Jégou. Billion-scale similarity search with gpus.IEEE Transactions on Big Data, 7(3):535–547, 2019. Armand Joulin, Piotr Bojanowski, Tomáš Mikolov, Hervé Jégou, and Édouard Grave. Loss in translation: Learning bilingual word mapping with a retrieval criterion. InProceedings of the 2018 Conference on Empirical Methods in Natural Language Processing, pp. 2979–2984, 2018. Yeong-Joon Ju, Ho-Joong Kim, and Seong-Whan Lee.

**中文**

第十届 ACM 国际网络搜索和数据挖掘会议论文集，第 781-789 页，2017 年。Jeff Johnson、Matthijs Douze 和 Hervé Jégou。使用 GPU 进行十亿级相似性搜索。IEEE 大数据汇刊，7(3):535–547, 2019。Armand Joulin、Piotr Bojanowski、Tomáš Mikolov、Hervé Jégou 和 Édouard Grave。翻译损失：使用检索标准学习双语单词映射。 2018 年自然语言处理经验方法会议论文集，第 2979-2984 页，2018 年。Yeong-Joon Ju、Ho-Joong Kim 和 Seong-Whan Lee。

### 段落 361 · Page 47

**EN**

MIRe: Enhancing multimodal queries representation via fusion-free modality interaction for multimodal retrieval. In Wanxiang Che, Joyce Nabende, Ekaterina Shutova, andMohammadTaherPilehvar(eds.),Findings of the Association for Computational Linguistics: ACL 2025, pp. 5350–5363, Vienna, Austria, July 2025. Association for Computational Linguistics. doi: 10.18653/v1/2025.findings-acl.279. URLhttps://aclanthology.org/2025.findings-acl.279/. John Jumper, Richard Evans, Alexander Pritzel, Tim Green, Michael Figurnov, Olaf Ronneberger, Kathryn Tunyasuvunakool, Russ Bates, Augustin Žídek, Anna Potapenko, et al.

**中文**

MIRe：通过多模态检索的无融合模态交互增强多模态查询表示。载于 Wanyang Che、Joyce Nabende、Ekaterina Shutova 和 MohammadTaherPilehvar（编辑），计算语言学协会的调查结果：ACL 2025，第 5350–5363 页，奥地利维也纳，2025 年 7 月。计算语言学协会。 doi：10.18653/v1/2025.findings-acl.279。网址https://aclanthology.org/2025.findings-acl.279/。约翰·詹珀、理查德·埃文斯、亚历山大·普里策尔、蒂姆·格林、迈克尔·菲格诺夫、奥拉夫·罗纳伯格、凯瑟琳·图尼亚苏瓦纳库尔、拉斯·贝茨、奥古斯丁·齐德克、安娜·波塔彭科等。

### 段落 362 · Page 47

**EN**

Highly accurate protein structure prediction with AlphaFold.Nature, 596(7873):583–589, 2021. SeongKu Kang, Shivam Agarwal, Bowen Jin, Dongha Lee, Hwanjo Yu, and Jiawei Han. Improving retrieval in theme-specific applications using a corpus topical taxonomy.Proceedings of the ACM Web Conference 2024, 2024. Jared Kaplan, Sam McCandlish, Tom Henighan, Tom B. Brown, Benjamin Chess, Rewon Child, Scott Gray, Alec Radford, Jeffrey Wu, and Dario Amodei. Scaling laws for neural language models.arXiv preprint arXiv:2001.08361, 2020. Andrej Karpathy, Armand Joulin, and Li Fei-Fei.

**中文**

使用 AlphaFold.Nature 进行高精度蛋白质结构预测，596(7873):583–589, 2021。SeongKu Kang、Shivam Agarwal、Bowen Jin、Dongha Lee、Hwanjo Yu 和 Jiawei Han。使用语料库主题分类法改进特定主题应用程序中的检索。2024 年、2024 年 ACM 网络会议论文集。Jared Kaplan、Sam McCandlish、Tom Henighan、Tom B. Brown、Benjamin Chess、Rewon Child、Scott Gray、Alec Radford、Jeffrey Wu 和 Dario Amodei。神经语言模型的缩放定律。arXiv 预印本 arXiv:2001.08361, 2020。Andrej Karpathy、Armand Joulin 和 Li Fei-Fei。

### 段落 363 · Page 47

**EN**

Deep fragment embeddings for bidirectional image sentence mapping.Advances in neural information processing systems, 27, 2014. Vladimir Karpukhin, Barlas Oğuz, Sewon Min, Patrick Lewis, Ledell Yu Wu, Sergey Edunov, Danqi Chen, and Wen tau Yih. Dense passage retrieval for open-domain question answering.arXiv preprint arXiv:2004.04906, 2020. Angelos Katharopoulos, Apoorv Vyas, Nikolaos Pappas, and François Fleuret. Transformers are RNNs: Fast autoregressive transformers with linear attention. InInternational Conference on Machine Learning, pp. 5156–5165. PMLR, 2020. 47

**中文**

用于双向图像句子映射的深度片段嵌入。神经信息处理系统的进展，27，2014。Vladimir Karpukhin、Barlas Oğuz、Sewon Min、Patrick Lewis、Ledell Yu Wu、Sergey Edunov、Danqi Chen 和 Wen tau Yih。开放域问答的密集段落检索。arXiv 预印本 arXiv:2004.04906, 2020。Angelos Katharopoulos、Apoorv Vyas、Nikolaos Pappas 和 François Fleuret。 Transformer 是 RNN：具有线性注意力的快速自回归 Transformer。国际机器学习会议，第 5156–5165 页。 PMLR，2020。 47

### Page 48

### 段落 364 · Page 48

**EN**

Published in Transactions on Machine Learning Research (02/2026) Guolin Ke, Qi Meng, Thomas Finley, Taifeng Wang, Wei Chen, Weidong Ma, Qiwei Ye, and Tie-Yan Liu. Lightgbm: A highly efficient gradient boosting decision tree.Advances in neural information processing systems, 30, 2017. Michael Kearns and Leslie Valiant. Cryptographic limitations on learning boolean formulae and finite automata.Journal of the ACM (JACM), 41(1):67–95, 1994. Urvashi Khandelwal, Omer Levy, Dan Jurafsky, Luke Zettlemoyer, and Mike Lewis. Generalization through memorization: Nearest neighbor language models.

**中文**

发表在《机器学习研究汇刊》(02/2026) 柯郭林、孟奇、托马斯·芬利、王泰峰、陈伟、马卫东、叶奇伟和刘铁岩。 Lightgbm：一种高效的梯度提升决策树。神经信息处理系统的进展，30，2017。Michael Kearns 和 Leslie Valiant。学习布尔公式和有限自动机的密码学限制。ACM 杂志 (JACM), 41(1):67–95, 1994。Urvashi Khandelwal、Omer Levy、Dan Jurafsky、Luke Zettlemoyer 和 Mike Lewis。通过记忆进行泛化：最近邻语言模型。

### 段落 365 · Page 48

**EN**

InInternational Conference on Learning Representations, 2020. URLhttps://openreview.net/forum?id=HklBjCEKvH. Omar Khattab and Matei Zaharia. ColBERT: Efficient and effective passage search via contextualized late interaction over BERT. InProceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 39–48, 2020. Tushar Khot, Harsh Trivedi, Matthew Finlayson, Yao Fu, Kyle Richardson, Peter Clark, and Ashish Sabharwal. Decomposed prompting: A modular approach for solving complex tasks. InThe 11th International Conference on Learning Representations, 2023.

**中文**

在国际学习表征会议，2020。URLhttps://openreview.net/forum?id=HklBjCEKvH。奥马尔·哈塔布和马泰·扎哈里亚。 ColBERT：通过 BERT 上的上下文化后期交互进行高效且有效的段落搜索。第 43 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 39-48 页，2020 年。Tushar Khot、Harsh Trivedi、Matthew Finlayson、Yao Fu、Kyle Richardson、Peter Clark 和 Ashish Sabharwal。分解提示：解决复杂任务的模块化方法。在第 11 届学习表征国际会议，2023 年。

### 段落 366 · Page 48

**EN**

URLhttps://openreview.net/forum?id=_nGgzQjzaRy. Julian Killingback, Hansi Zeng, and Hamed Zamani. Hypencoder: Hypernetworks for information retrieval. arXiv preprint arXiv:2502.05364, 2025. Seungyeon Kim, Ankit Singh Rawat, Manzil Zaheer, Sadeep Jayasumana, Veeranjaneyulu Sadhanala, Wittawat Jitkrittum, Aditya Krishna Menon, Rob Fergus, and Sanjiv Kumar. EmbedDistill: A geometric knowledge distillation for information retrieval.arXiv preprint arXiv:2301.12005, 2023. Sungyeon Kim, Xinliang Zhu, Xiaofan Lin, Muhammet Bastan, Douglas Gray, and Suha Kwak.

**中文**

网址https://openreview.net/forum?id=_nGgzQjzaRy。 Julian Killingback、Hansi Zeng 和 Hamed Zamani。 Hypencoder：用于信息检索的超网络。 arXiv 预印本 arXiv：2502.05364，2025。Seungyeon Kim、Ankit Singh Rawat、Manzil Zaheer、Sadeep Jayasumana、Veeranjaneyulu Sadhanala、Wittawat Jitkrittum、Aditya Krishna Menon、Rob Fergus 和 Sanjiv Kumar。 EmbedDistill：信息检索的几何知识蒸馏。arXiv 预印本 arXiv：2301.12005，2023。Sungyeon Kim、Xinliang Zhu、Xiaofan Lin、Muhammet Bastan、Douglas Gray 和 Suha Kwak。

### 段落 367 · Page 48

**EN**

GENIUS: A generative framework for universal multimodal search.2025 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), pp. 19659–19669, 2025. Yoon Kim. Convolutional neural networks for sentence classification. In Alessandro Moschitti, Bo Pang, and Walter Daelemans (eds.),Proceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 1746–1751, Doha, Qatar, October 2014. Association for Computational Linguistics. doi: 10.3115/v1/D14-1181. URLhttps://aclanthology.org/D14-1181/. Varsha Kishore, Chao Wan, Justin Lovelace, Yoav Artzi, and Kilian Q. Weinberger.

**中文**

GENIUS：通用多模态搜索的生成框架。2025 年 IEEE/CVF 计算机视觉和模式识别会议 (CVPR)，第 19659–19669 页，2025 年。Yoon Kim。用于句子分类的卷积神经网络。载于 Alessandro Moschitti、Bo Pang 和 Walter Daelemans（编辑），2014 年自然语言处理经验方法 (EMNLP) 会议论文集，第 1746–1751 页，卡塔尔多哈，2014 年 10 月。计算语言学协会。 doi：10.3115/v1/D14-1181。网址https://aclanthology.org/D14-1181/。 Varsha Kishore、Chao Wan、Justin Lovelace、Yoav Artzi 和 Kilian Q. Weinberger。

### 段落 368 · Page 48

**EN**

Incdsi: Incrementally updatabledocumentretrieval. InInternational Conference on Machine Learning, pp.17122–17134.PMLR, 2023. Fanheng Kong, Jingyuan Zhang, Yahui Liu, Hongzhi Zhang, Shi Feng, Xiaocui Yang, Daling Wang, Yu Tian, Qi Wang, Fuzheng Zhang, and Guorui Zhou. Modality curation: Building universal embeddings for advanced multimodal information retrieval.arXiv preprint arXiv:2505.19650, 2025. Weize Kong, Jeffrey M. Dudek, Cheng Li, Mingyang Zhang, and Michael Bendersky. Sparseembed: Learning sparse lexical representations with contextual embeddings for retrieval.

**中文**

Incdsi：增量可更新文档检索。国际机器学习会议，第 17122–17134 页。PMLR，2023。Fanheng Kong、Jingyuan 张、Yahui Liu、Hongzhi 张、Shi Feng、Xiaocui Yang、Daling Wang、Yu Tian、Qi Wang、Fuzheng Zhang 和 Guorui Zhou。模态管理：为高级多模态信息检索构建通用嵌入。arXiv 预印本 arXiv:2505.19650, 2025。Weize Kong、Jeffrey M. Dudek、Cheng Li、Mingyang Zhu 和 Michael Bendersky。 Sparseembed：通过上下文嵌入学习稀疏词汇表示以进行检索。

### 段落 369 · Page 48

**EN**

InProceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 2399–2403, 2023. Donald H. Kraft and Duncan A. Buell. Fuzzy sets and generalized boolean retrieval systems.International journal of man-machine studies, 19(1):45–56, 1983. Tanishq Kumar, Zachary Ankner, Benjamin F. Spector, Blake Bordelon, Niklas Muennighoff, Mansheej Paul, Cengiz Pehlevan, Christopher Ré, and Aditi Raghunathan. Scaling laws for precision.arXiv preprint arXiv:2411.04330, 2024. Woosuk Kwon, Zhuohan Li, Siyuan Zhuang, Ying Sheng, Lianmin Zheng, Cody Hao Yu, Joseph Gonzalez, Hao Zhang, and Ion Stoica.

**中文**

第 46 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 2399-2403 页，2023 年。Donald H. Kraft 和 Duncan A. Buell。模糊集和广义布尔检索系统。国际人机研究杂志，19(1):45–56, 1983。Tanishq Kumar、Zachary Ankner、Benjamin F. Spector、Blake Bordelon、Niklas Muennighoff、Mansheej Paul、Cengiz Pehlevan、Christopher Ré 和 Aditi Raghunathan。精度的缩放定律。arXiv 预印本 arXiv:2411.04330, 2024。Woosuk Kwon、Zhuohan Li、Siyuan Zhuang、Ying Shen、Lianmin Cheng、Codyhao Yu、Joseph Gonzalez、Hao Zhu 和 Ion Stoica。

### 段落 370 · Page 48

**EN**

Efficient memory management for large language model serving with pagedattention. InProceedings of the 29th Symposium on Operating Systems Principles, pp. 611–626, 2023. 48

**中文**

通过 pagedattention 服务的大型语言模型的高效内存管理。第 29 届操作系统原理研讨会论文集，第 611–626 页，2023 年。 48

### Page 49

### 段落 371 · Page 49

**EN**

Published in Transactions on Machine Learning Research (02/2026) Zhenzhong Lan, Mingda Chen, Sebastian Goodman, Kevin Gimpel, Piyush Sharma, and Radu Soricut. AL- BERT: A lite BERT for self-supervised learning of language representations. InInternational Conference on Learning Representations, 2020. URLhttps://openreview.net/forum?id=H1eA7AEtvS. Quoc Le and Tomas Mikolov. Distributed representations of sentences and documents.Proceedings of the 31st International Conference on Machine Learning, PMLR, 32(2):1188–1196, 22–24 Jun 2014. URL https://proceedings.mlr.press/v32/le14.html. Yann LeCun, Bernhard Boser, John S.

**中文**

发表在《机器学习研究汇刊》(02/2026) 上：Zhenzhong Lan、Mingda Chen、Sebastian Goodman、Kevin Gimpel、Piyush Sharma 和 Radu Soricut。 ALBERT：一个精简版 BERT，用于语言表示的自我监督学习。在国际学习表征会议，2020。URLhttps://openreview.net/forum?id=H1eA7AEtvS。库克·勒和托马斯·米科洛夫。句子和文档的分布式表示。第 31 届国际机器学习会议论文集，PMLR，32(2)：1188–1196，2014 年 6 月 22–24 日。URL https://proceedings.mlr.press/v32/le14.html。扬·勒昆 (Yann LeCun)、伯恩哈德·博瑟 (Bernhard Boser)、约翰·S.

### 段落 372 · Page 49

**EN**

Denker, Donnie Henderson, Richard E. Howard, Wayne Hubbard, and Lawrence D. Jackel. Backpropagation applied to handwritten zip code recognition.Neural computation, 1(4):541–551, 1989. Chankyu Lee, Rajarshi Roy, Mengyao Xu, Jonathan Raiman, Mohammad Shoeybi, Bryan Catanzaro, and WeiPing. NV-embed: Improved techniquesfor training LLMs asgeneralist embedding models. InThe 13th International Conference on Learning Representations, 2025. URLhttps://openreview.net/forum?id= lgsyLSsDRe. Jinhyuk Lee, Zhuyun Dai, Xiaoqi Ren, Blair Chen, Daniel Cer, Jeremy R. Cole, Kai Hui, Michael Boratko, Rajvi Kapadia, Wen Ding, et al.

**中文**

丹克尔、唐尼·亨德森、理查德·E·霍华德、韦恩·哈伯德和劳伦斯·D·杰克尔。反向传播应用于手写邮政编码识别。神经计算，1(4):541–551, 1989。Chankyu Lee、Rajarshi Roy、Mengyao Xu、Jonathan Raiman、Mohammad Shoeybi、Bryan Catanzaro 和 WeiPing。 NV-embed：改进了将法学硕士训练为通用嵌入模型的技术。在第 13 届学习表征国际会议，2025 年。 URL https://openreview.net/forum?id= lgsyLSsDRe。 Jinhyuk Lee、Zhuyun Dai、Xiaoqi Ren、Blair Chen、Daniel Cer、Jeremy R. Cole、Kai Hui、Michael Boratko、Rajvi Kapadia、Wen Ding 等。

### 段落 373 · Page 49

**EN**

Gecko: Versatile text embeddings distilled from large language models. arXiv preprint arXiv:2403.20327, 2024. Kenton Lee, Ming-Wei Chang, and Kristina Toutanova. Latent retrieval for weakly supervised open domain question answering.arXiv preprint arXiv:1906.00300, 2019. Omer Levy, Yoav Goldberg, and Ido Dagan. Improving distributional similarity with lessons learned from word embeddings.Transactions of the Association for Computational Linguistics, 3:211–225, 2015. doi: 10.1162/tacl_a_00134. URLhttps://aclanthology.org/Q15-1016/.

**中文**

Gecko：从大型语言模型中提取的多功能文本嵌入。 arXiv 预印本 arXiv:2403.20327, 2024。Kenton Lee、Ming-Wei Chang 和 Kristina Toutanova。弱监督开放域问答的潜在检索。arXiv 预印本 arXiv:1906.00300, 2019。Omer Levy、Yoav Goldberg 和 Ido Dagan。利用词嵌入的经验教训提高分布相似性。计算语言学协会汇刊，3:211–225, 2015。doi: 10.1162/tacl_a_00134。网址https://aclanthology.org/Q15-1016/。

### 段落 374 · Page 49

**EN**

Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Veselin Stoyanov, and Luke Zettlemoyer. BART: Denoising sequence-to-sequence pre-training for natural language generation, translation, and comprehension. In Dan Jurafsky, Joyce Chai, Natalie Schluter, and Joel Tetreault (eds.),Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics, pp. 7871–7880, Online, July 2020a. Association for Computational Linguistics. doi: 10.18653/v1/2020. acl-main.703. URLhttps://aclanthology.org/2020.acl-main.703/.

**中文**

Mike Lewis、Yinhan Liu、Naman Goyal、Marjan Ghazvininejad、Abdelrahman Mohamed、Omer Levy、Veselin Stoyanov 和 Luke Zettlemoyer。 BART：用于自然语言生成、翻译和理解的序列到序列去噪预训练。载于 Dan Jurafsky、Joyce Chai、Natalie Schluter 和 Joel Tetreault（编辑），计算语言学协会第 58 届年会记录，第 7871-7880 页，在线，2020 年 7 月a。计算语言学协会。 doi：10.18653/v1/2020。 acl-main.703。网址https://aclanthology.org/2020.acl-main.703/。

### 段落 375 · Page 49

**EN**

Patrick Lewis, Ethan Perez, Aleksandra Piktus, Fabio Petroni, Vladimir Karpukhin, Naman Goyal, Heinrich Küttler, Mike Lewis, Wen-tau Yih, Tim Rocktäschel, et al. Retrieval-augmented generation for knowledgeintensive nlp tasks.Advances in neural information processing systems, 33:9459–9474, 2020b. Canjia Li, Andrew Yates, Sean MacAvaney, Ben He, and Yingfei Sun. PARADE: Passage representation aggregation fordocument reranking.ACM Transactions on Information Systems, 42(2), September 2023a. doi: 10.1145/3600088. Chaofan Li, Zheng Liu, Shitao Xiao, and Yingxia Shao.

**中文**

Patrick Lewis、Ethan Perez、Aleksandra Piktus、Fabio Petroni、Vladimir Karpukhin、Naman Goyal、Heinrich Küttler、Mike Lewis、Wen-tau Yih、Tim Rocktäschel 等。知识密集型 NLP 任务的检索增强生成。神经信息处理系统的进展，33：9459–9474，2020b。李灿嘉、安德鲁·耶茨、肖恩·麦克卡瓦尼、何本和孙英飞。 PARADE：用于文档重新排序的段落表示聚合。ACM 信息系统交易，42(2)，2023 年 9 月a。 doi：10.1145/3600088。李超凡、刘峥、肖世涛、邵迎霞。

### 段落 376 · Page 49

**EN**

Making large language models a better foundation for dense retrieval.arXiv preprint arXiv:2312.15503, 2023b. Dongfang Li, Baotian Hu, and Qingcai Chen. Calibration meets explanation: A simple and effective approach for model confidence estimates. In Yoav Goldberg, Zornitsa Kozareva, and Yue Zhang (eds.),Proceedings of the 2022 Conference on Empirical Methods in Natural Language Processing, pp. 2775–2784, Abu Dhabi, United Arab Emirates, December 2022a. Association for Computational Linguistics. doi: 10.18653/v1/ 2022.emnlp-main.178. URLhttps://aclanthology.org/2022.emnlp-main.178/. Gen Li, Nan Duan, Yuejian Fang, Daxin Jiang, and Ming Zhou.

**中文**

让大型语言模型成为密集检索的更好基础。arXiv 预印本 arXiv:2312.15503, 2023b。李东方，胡宝田，陈庆才。校准与解释：一种简单有效的模型置信度估计方法。载于 Yoav Goldberg、Zornitsa Kozareva 和 Yue Zhu（编辑），2022 年自然语言处理经验方法会议论文集，第 2775-2784 页，阿拉伯联合酋长国阿布扎比，2022 年 12 月a。计算语言学协会。 doi：10.18653/v1/2022.emnlp-main.178。网址https://aclanthology.org/2022.emnlp-main.178/。李根，段南，方跃建，蒋大新，周明。

### 段落 377 · Page 49

**EN**

Unicoder-VL: A universal encoder for vision and language by cross-modal pre-training. InAAAI Conference on Artificial Intelligence, 2019. Hang Li. Learning for ranking aggregation. InLearning to Rank for Information Retrieval and Natural Language Processing, pp. 33–35. Springer, 2011. 49

**中文**

Unicoder-VL：通过跨模态预训练实现视觉和语言的通用编码器。 InAAAI人工智能大会，2019。李航。学习排名聚合。 《信息检索和自然语言处理的学习排名》，第 33-35 页。施普林格，2011。49

### Page 50

### 段落 378 · Page 50

**EN**

Published in Transactions on Machine Learning Research (02/2026) JunnanLi, DongxuLi, CaimingXiong, andStevenHoi. BLIP:Bootstrappinglanguage-imagepre-trainingfor unified vision-language understanding and generation. InInternational Conference on Machine Learning, pp. 12888–12900. PMLR, 2022b. Minghan Li, Sheng-Chieh Lin, Xueguang Ma, and Jimmy Lin. SLIM: Sparsified late interaction for multivector retrieval with inverted indexes. InProceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’23, pp. 1954–1959, New York, NY, USA, 2023c. Association for Computing Machinery.

**中文**

发表于机器学习研究汇刊 (02/2026) JunnanLi、DongxuLi、CaimingXiong 和 StevenHoi。 BLIP：引导语言图像预训练，以实现统一的视觉语言理解和生成。国际机器学习会议，第 12888–12900 页。 PMLR，2022b。李明汉、林胜杰、马学光、林吉米。 SLIM：使用倒排索引进行多向量检索的稀疏后期交互。第 46 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR ’23，第 1954-1959 页，美国纽约州纽约，2023c。计算机器协会。

### 段落 379 · Page 50

**EN**

doi: 10.1145/3539618.3591977. Mufei Li, Siqi Miao, and Pan Li. Simple is effective: The roles of graphs and large language models in knowledge-graph-based retrieval-augmented generation. InThe 13th International Conference on Learning Representations, 2025a. URLhttps://openreview.net/forum?id=JvkuZZ04O7. SenLi, FuyuLv, TaiweiJin, GuliLin, KepingYang, XiaoyiZeng, Xiao-MingWu, andQianliMa. Embeddingbased product retrieval in taobao search. InProceedings of the 27th ACM SIGKDD Conference on Knowledge Discovery & Data Mining, pp. 3181–3189, 2021.

**中文**

号码：10.1145/3539618.3591977。李慕飞，苗思琪，李潘。简单就是有效：图和大型语言模型在基于知识图的检索增强生成中的作用。在第 13 届学习表征国际会议，2025a。网址https://openreview.net/forum?id=JvkuZZ04O7。 SenLi、FuyuLv、Taiwei Jin、GuliLin、KepingYang、XiaoyiZeng、Xiao-MingWu 和 QianliMa。淘宝搜索中基于嵌入的产品检索第 27 届 ACM SIGKDD 知识发现和数据挖掘会议论文集，第 3181-3189 页，2021 年。

### 段落 380 · Page 50

**EN**

Xiaoxi Li, Guanting Dong, Jiajie Jin, Yuyao Zhang, Yujia Zhou, Yutao Zhu, Peitian Zhang, and Zhicheng Dou. Search-o1: Agentic search-enhanced large reasoning models.arXiv preprint arXiv:2501.05366, 2025b. Xiaoxi Li, Jiajie Jin, Guanting Dong, Hongjin Qian, Yutao Zhu, Yongkang Wu, Ji-Rong Wen, and Zhicheng Dou. Webthinker: Empowering large reasoning models with deep research capability.arXiv preprint arXiv:2504.21776, 2025c. Xiaoxi Li, Jiajie Jin, Yujia Zhou, Yuyao Zhang, Peitian Zhang, Yutao Zhu, and Zhicheng Dou.

**中文**

李晓西、董冠廷、金家杰、张玉瑶、周玉嘉、朱玉涛、张培田和窦志成。 Search-o1：代理搜索增强型大型推理模型。arXiv 预印本 arXiv：2501.05366，2025b。李晓西、金佳杰、董冠廷、钱宏进、朱玉涛、吴永康、文继荣和窦志成。 Webthinker：通过深度研究能力增强大型推理模型。arXiv 预印本 arXiv:2504.21776, 2025c。李晓曦、金佳杰、周雨佳、张玉瑶、张培田、朱玉涛和窦志成。

### 段落 381 · Page 50

**EN**

From matching to generation: A survey on generative information retrieval.ACM Transactions on Information Systems, 43(3), May 2025d. doi: 10.1145/3722552. Yangning Li, Weizhi Zhang, Yuyao Yang, Wei-Chieh Huang, Yaozu Wu, Junyu Luo, Yuanchen Bei, Henry Peng Zou, Xiao Luo, Yusheng Zhao, et al. Towards agentic RAG with deep reasoning: A survey of RAG-reasoning systems in LLMs.arXiv preprint arXiv:2507.09477, 2025e. Zehan Li, Xin Zhang, Yanzhao Zhang, Dingkun Long, Pengjun Xie, and Meishan Zhang. Towards general text embeddings with multi-stage contrastive learning.arXiv preprint arXiv:2308.03281, 2023d.

**中文**

从匹配到生成：生成信息检索调查。ACM 信息系统汇刊，43(3)，2025 年 5 月d。 doi：10.1145/3722552。李阳宁，张伟志，杨宇耀，黄伟杰，吴耀祖，罗俊宇，贝元辰，邹亨利，罗晓，赵宇胜，等。走向具有深度推理的代理 RAG：LLMs.arXiv 预印本 arXiv:2507.09477, 2025e 中 RAG 推理系统的调查。李泽涵、张鑫、张艳照、龙定坤、谢鹏军和张美山。通过多阶段对比学习实现一般文本嵌入。arXiv 预印本 arXiv:2308.03281, 2023d。

### 段落 382 · Page 50

**EN**

Jintao Liang, Gang Su, Huifeng Lin, You Wu, Rui Zhao, and Ziyue Li. Reasoning RAG via system 1 or system 2: A survey on reasoning agentic retrieval-augmented generation for industry challenges.arXiv preprint arXiv:2506.10408, 2025. Jimmy Lin. A proposed conceptual framework for a representational approach to information retrieval.ACM SIGIR Forum, 55:1–29, 2021. Jimmy Lin and Xueguang Ma. A few brief notes on DeepImpact, COIL, and a conceptual framework for information retrieval techniques.arXiv preprint arXiv:2106.14807, 2021. Jimmy Lin, Rodrigo Nogueira, and Andrew Yates.Pretrained transformers for text ranking: BERT and beyond.

**中文**

梁金涛、苏刚、林慧峰、吴友、赵锐、李子跃。通过系统 1 或系统 2 进行推理 RAG：针对行业挑战的推理代理检索增强生成的调查。arXiv 预印本 arXiv：2506.10408，2025。Jimmy Lin。信息检索表征方法的拟议概念框架。ACM SIGIR 论坛，55:1–29, 2021。吉米·林和学光·马。关于 DeepImpact、COIL 和信息检索技术概念框架的一些简短说明。arXiv 预印本 arXiv:2106.14807, 2021。Jimmy Lin、Rodrigo Nogueira 和 Andrew Yates。用于文本排名的预训练转换器：BERT 及其他。

### 段落 383 · Page 50

**EN**

Springer Nature, 2022. Juexin Lin, Sachin Yadav, Feng Liu, Nicholas Rossi, Praveen Reddy Suram, Satya Chembolu, Prijith Chandran, Hrushikesh Mohapatra, Tony Lee, Alessandro Magnani, and Ciya Liao. Enhancing relevance of embedding-based retrieval at Walmart.Proceedings of the 33rd ACM International Conference on Information and Knowledge Management, 2024. Minhua Lin, Zongyu Wu, Zhichao Xu, Hui Liu, Xianfeng Tang, Qi He, Charu Aggarwal, Hui Liu, Xiang Zhang, and Suhang Wang.

**中文**

施普林格自然，2022。Juexin Lin、Sachin Yadav、Feng Liu、Nicholas Rossi、Praveen Reddy Suram、Satya Chembolu、Prijith Chandran、Hrushikesh Mohapatra、Tony Lee、Alessandro Magnani 和 Ciya Liao。增强沃尔玛基于嵌入的检索的相关性。第 33 届 ACM 国际信息与知识管理会议论文集，2024 年。Minhua Lin、Zongyu Wu、Zhichao Xu、Hui Liu、Xianfeng Tang、Qi He、Charu Aggarwal、Hui Liu、Xiang Zhu 和 Suhang Wang。

### 段落 384 · Page 50

**EN**

A comprehensive survey on reinforcement learning-based agentic search: Foundations, roles, optimizations, evaluations, and applications.arXiv preprint arXiv:2510.16724, 2025. 50

**中文**

基于强化学习的代理搜索的综合调查：基础、角色、优化、评估和应用。arXiv 预印本 arXiv:2510.16724, 2025。 50

### Page 51

### 段落 385 · Page 51

**EN**

Published in Transactions on Machine Learning Research (02/2026) Robert Litschko, Ivan Vulić, and Goran Glavaš. Parameter-efficient neural reranking for cross-lingual and multilingual retrieval. In Nicoletta Calzolari, Chu-Ren Huang, Hansaem Kim, James Pustejovsky, Leo Wanner, Key-Sun Choi, Pum-Mo Ryu, Hsin-Hsi Chen, Lucia Donatelli, Heng Ji, Sadao Kurohashi, Patrizia Paggio, Nianwen Xue, Seokhwan Kim, Younggyun Hahm, Zhong He, Tony Kyungil Lee, Enrico Santus, Francis Bond, and Seung-Hoon Na (eds.),Proceedings of the 29th International Conference on Computational Linguistics, pp. 1071–1082, Gyeongju, Republic of Korea, October 2022.

**中文**

发表于机器学习研究汇刊 (02/2026) Robert Litschko、Ivan Vulić 和 Goran Glavaš。用于跨语言和多语言检索的参数高效神经重新排序。 Nicoletta Calzolari、Chu-Ren Huang、Hansaem Kim、James Pustejovsky、Leo Wanner、Key-Sun Choi、Pum-Mo Ryu、Hsin-Hsi Chen、Lucia Donatelli、Heng Ji、Sadao Kurohashi、Patrizia Paggio、Nianwen Xu、Seokhwan Kim、Younggyun Hahm、Zhong He、Tony Kyungil Lee、Enrico Santus、Francis Bond 和Seung-Hoon Na（编辑），第 29 届国际计算语言学会议论文集，第 1071-1082 页，韩国庆州，2022 年 10 月。

### 段落 386 · Page 51

**EN**

International Committee on Computational Linguistics. URLhttps://aclanthology.org/2022.coling-1.90/. Aixin Liu, Bei Feng, Bing Xue, Bingxuan Wang, Bochao Wu, Chengda Lu, Chenggang Zhao, Chengqi Deng, Chenyu Zhang, Chong Ruan, et al. DeepSeek-v3 technical report.arXiv preprint arXiv:2412.19437, 2024a. Hao Liu, Zhengren Wang, Xi Chen, Zhiyu Li, Feiyu Xiong, Qinhan Yu, and Wentao Zhang. HopRAG: Multihopreasoningforlogic-awareretrieval-augmentedgeneration. InWanxiangChe, JoyceNabende, Ekaterina Shutova, andMohammadTaherPilehvar(eds.),Findings of the Association for Computational Linguistics: ACL 2025, pp. 1897–1913, Vienna, Austria, July 2025a.

**中文**

国际计算语言学委员会。网址https://aclanthology.org/2022.coling-1.90/。刘爱新，冯北，薛冰，王冰轩，吴伯超，陆成达，赵成刚，邓成奇，张晨宇，阮冲，等。 DeepSeek-v3 技术报告.arXiv 预印本 arXiv:2412.19437, 2024a。刘浩、王正仁、陈曦、李志宇、熊飞宇、于钦汉和张文涛。 HopRAG：逻辑感知检索增强生成的多重推理。载于 Wanyang Che、Joyce Nabende、Ekaterina Shutova 和 Mohammad Taher Pilehvar（编辑），计算语言学协会的调查结果：ACL 2025，第 1897-1913 页，奥地利维也纳，2025 年 7 月a。

### 段落 387 · Page 51

**EN**

Association for Computational Linguistics. doi: 10.18653/v1/2025.findings-acl.97. URLhttps://aclanthology.org/2025.findings-acl.97/. Haotian Liu, Chunyuan Li, Qingyang Wu, and Yong Jae Lee. Visual instruction tuning.arXiv preprint arXiv:2304.08485, 2023. Jingzhou Liu, Wei-Cheng Chang, Yuexin Wu, and Yiming Yang. Deep learning for extreme multi-label text classification. InProceedings of the 40th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 115–124, 2017. Pei Liu, Xin Liu, Ruoyu Yao, Junming Liu, Siyuan Meng, Ding Wang, and Jun Ma.

**中文**

计算语言学协会。 doi：10.18653/v1/2025.findings-acl.97。网址https://aclanthology.org/2025.findings-acl.97/。刘昊天、李春元、吴庆阳、李永杰。视觉指令调优.arXiv 预印本 arXiv:2304.08485, 2023。Jingzhou Liu、Wei-Cheng Chang、Yuexin Wu 和 Yiming Yang。用于极端多标签文本分类的深度学习。第 40 届国际 ACM SIGIR 信息检索研究与发展会议论文集，第 115-124 页，2017 年。 Pei Liu、Xin Liu、Ruoyu Yao、Junming Liu、Siyuan Meng、Ding Wang 和 Jun Ma。

### 段落 388 · Page 51

**EN**

Hm-RAG: Hierarchical multi-agent multimodal retrieval augmented generation.Proceedings of the 33rd ACM International Conference on Multimedia, 2025b. Qi Liu, Bo Wang, Nan Wang, and Jiaxin Mao. Leveraging passage embeddings for efficient listwise reranking with large language models. InProceedings of the ACM on Web Conference 2025, 2024b. doi: 10.1145/ 3696410.3714554. Song Liu, Haoqi Fan, Shengsheng Qian, Yiru Chen, Wenkui Ding, and Zhongyuan Wang. HiT: Hierarchical transformer with momentum contrast for video-text retrieval.2021 IEEE/CVF International Conference on Computer Vision (ICCV), pp. 11895–11905, 2021. Tie-Yan Liu.

**中文**

Hm-RAG：分层多智能体多模式检索增强生成。第 33 届 ACM 国际多媒体会议论文集，2025b。刘奇、王博、王楠和毛嘉欣。利用段落嵌入对大型语言模型进行高效的列表重新排序。 ACM 网络会议 2025、2024b 论文集。号码：10.1145/3696410.3714554。刘松，范浩琪，钱胜胜，陈一如，丁文奎，王中远。 HiT：用于视频文本检索的具有动量对比的分层变换器。2021 IEEE/CVF 国际计算机视觉会议 (ICCV)，第 11895–11905 页，2021。Tie-Yan Liu。

### 段落 389 · Page 51

**EN**

Learning to rank for information retrieval.Foundations and Trends in Information Retrieval, 3(3):225–331, March 2009. doi: 10.1561/1500000016. Yinhan Liu, Myle Ott, Naman Goyal, Jingfei Du, Mandar Joshi, Danqi Chen, Omer Levy, Mike Lewis, Luke Zettlemoyer, and Veselin Stoyanov. RoBERTa: A robustly optimized BERT pretraining approach.arXiv preprint arXiv:1907.11692, 2019. Yu-An Liu, Ruqing Zhang, Jiafeng Guo, and Maarten de Rijke. Robust information retrieval. InProceedings of the 18th ACM International Conference on Web Search and Data Mining, pp. 1008–1011, 2025c. Zhenghao Liu, Chenyan Xiong, Maosong Sun, and Zhiyuan Liu.

**中文**

学习信息检索排名。信息检索的基础和趋势，3(3):225–331，2009 年 3 月。doi: 10.1561/1500000016。 Yinhan Liu、Myle Ott、Naman Goyal、Jingfei Du、Mandar Joshi、Danqi Chen、Omer Levy、Mike Lewis、Luke Zettlemoyer 和 Veselin Stoyanov。 RoBERTa：一种稳健优化的 BERT 预训练方法。arXiv 预印本 arXiv：1907.11692，2019。Yu-An Liu、Ruqing Zhang、JiafengGuo 和 Maarten de Rijke。强大的信息检索。第 18 届 ACM 国际网络搜索和数据挖掘会议论文集，第 1008–1011 页，2025c。刘正浩、熊陈彦、孙茂松、刘志远。

### 段落 390 · Page 51

**EN**

Entity-duet neural ranking: Understanding the role of knowledge graph semantics in neural information retrieval. InProceedings of the 56th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp. 2395–2405, 2018. Lajanugen Logeswaran, Ming-Wei Chang, Kenton Lee, Kristina Toutanova, Jacob Devlin, and Honglak Lee. Zero-shot entity linking by reading entity descriptions. In Anna Korhonen, David Traum, and Lluís Màrquez (eds.),Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics, pp. 3449–3460, Florence, Italy, July 2019. Association for Computational Linguistics.

**中文**

实体二重奏神经排序：理解知识图语义在神经信息检索中的作用。计算语言学协会第 56 届年会记录（第一卷：长论文），第 2395–2405 页，2018 年。Lajanugen Logeswaran、Ming-Wei Chang、Kenton Lee、Kristina Toutanova、Jacob Devlin 和 Honglak Lee。通过读取实体描述进行零样本实体链接。载于 Anna Korhonen、David Traum 和 Lluís Màrquez（编），计算语言学协会第 57 届年会论文集，第 3449-3460 页，意大利佛罗伦萨，2019 年 7 月。计算语言学协会。

### 段落 391 · Page 51

**EN**

doi: 10.18653/v1/ P19-1335. URLhttps://aclanthology.org/P19-1335/. David G. Lowe. Object recognition from local scale-invariant features. InProceedings of the 7th IEEE International Conference on Computer Vision, volume 2, pp. 1150–1157, 1999. 51

**中文**

doi：10.18653/v1/P19-1335。网址https://aclanthology.org/P19-1335/。大卫·G·洛 (David G. Lowe)从局部尺度不变特征进行对象识别。第七届 IEEE 国际计算机视觉会议论文集，第 2 卷，第 1150–1157 页，1999 年。 51

### Page 52

### 段落 392 · Page 52

**EN**

Published in Transactions on Machine Learning Research (02/2026) Zhengdong Lu and Hang Li. A deep architecture for matching short texts.Advances in neural information processing systems, 26, 2013. Yi Luan, Jacob Eisenstein, Kristina Toutanova, and Michael Collins. Sparse, dense, and attentional representations for text retrieval.Transactions of the Association for Computational Linguistics, 9:329–345, 2021. Guangyuan Ma, Xing Wu, Zijia Lin, and Songlin Hu. Drop your decoder: Pre-training with bag-of-word prediction for dense passage retrieval.

**中文**

发表于《机器学习研究汇刊》(02/2026) 卢正东和李航。用于匹配短文本的深层架构。神经信息处理系统的进展，26，2013。Yi Luan、Jacob Eisenstein、Kristina Toutanova 和 Michael Collins。用于文本检索的稀疏、密集和注意表示。计算语言学协会汇刊，9:329–345, 2021。Guangyuan Ma、Xing Wu、Zijia Lin 和 Songlin Hu。放下解码器：使用词袋预测进行预训练，以实现密集段落检索。

### 段落 393 · Page 52

**EN**

InProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 1818–1827, 2024a. Xueguang Ma, Xinyu Zhang, Ronak Pradeep, and Jimmy Lin. Zero-shot listwise document reranking with a large language model.arXiv preprint arXiv: 2305.02156, 2023. Xueguang Ma, Liang Wang, Nan Yang, Furu Wei, and Jimmy Lin. Fine-tuning LLaMA for multi-stage text retrieval. InProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 2421–2425, 2024b. Sean MacAvaney, Luca Soldaini, and Nazli Goharian.

**中文**

第 47 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 1818-1827 页，2024a。马学光、张新宇、罗纳克·普拉迪普和林吉米。使用大型语言模型进行零样本列表文档重排序。arXiv 预印本 arXiv：2305.02156，2023。Xueguang Ma、Liang Wang、Nan Yang、Furu Wei 和 Jimmy Lin。微调 LLaMA 以进行多阶段文本检索。第 47 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 2421-2425 页，2024b。肖恩·麦克卡瓦尼、卢卡·索尔戴尼和纳兹利·戈哈里安。

### 段落 394 · Page 52

**EN**

Teaching a new dog old tricks: Resurrecting multilingual retrieval using zero-shot learning.Advances in Information Retrieval, 12036:246 – 254, 2019a. Sean MacAvaney, Andrew Yates, Arman Cohan, and Nazli Goharian. CEDR: Contextualized embeddings for document ranking. InProceedings of the 42nd International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 1101–1104, 2019b. Sean MacAvaney, Franco Maria Nardini, R. Perego, Nicola Tonellotto, Nazli Goharian, and Ophir Frieder.

**中文**

教新狗老把戏：使用零样本学习复活多语言检索。信息检索进展，12036：246 – 254，2019a。肖恩·麦克卡瓦尼、安德鲁·耶茨、阿曼·科汉和纳兹利·戈哈里安。 CEDR：用于文档排名的上下文嵌入。第 42 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 1101–1104 页，2019b。肖恩·麦克卡瓦尼、弗朗哥·玛丽亚·纳尔迪尼、R·佩雷戈、尼古拉·托内洛托、纳兹利·戈哈里安和奥菲尔·弗里德。

### 段落 395 · Page 52

**EN**

Efficient document re-ranking for transformers by precomputing term representations.Proceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval, 2020. Sean MacAvaney, Sergey Feldman, Nazli Goharian, Doug Downey, and Arman Cohan. ABNIRML: Analyzing the behavior of neural IR models.Transactions of the Association for Computational Linguistics, 10:224– 239, 2022. doi: 10.1162/tacl_a_00457. URLhttps://aclanthology.org/2022.tacl-1.13/. David J. C. MacKay and Linda C. Bauman Peto. A hierarchical Dirichlet language model.Natural language engineering, 1(3):289–308, 1995. Yu A. Malkov and Dmitry A.

**中文**

通过预计算术语表示对 Transformer 进行高效文档重新排序。第 43 届国际 ACM SIGIR 信息检索研究与开发会议论文集，2020 年。Sean MacAvaney、Sergey Feldman、Nazli Goharian、Doug Downey 和 Arman Cohan。 ABNIRML：分析神经 IR 模型的行为。计算语言学协会汇刊，10:224–239, 2022。doi: 10.1162/tacl_a_00457。网址https://aclanthology.org/2022.tacl-1.13/。大卫·J·C·麦凯和琳达·C·鲍曼·皮托。分层狄利克雷语言模型。自然语言工程，1(3):289–308, 1995。Yu A. Malkov 和 Dmitry A.

### 段落 396 · Page 52

**EN**

Yashunin. Efficient and robust approximate nearest neighbor search using hierarchical navigable small world graphs.IEEE transactions on pattern analysis and machine intelligence, 42(4):824–836, 2018. Alex Mallen, Akari Asai, Victor Zhong, Rajarshi Das, Daniel Khashabi, and Hannaneh Hajishirzi. When not to trust language models: Investigating effectiveness of parametric and non-parametric memories. In Anna Rogers, Jordan Boyd-Graber, and Naoaki Okazaki (eds.),Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp. 9802–9822, Toronto, Canada, July 2023.

**中文**

亚舒宁。使用分层可导航小世界图进行高效、鲁棒的近似最近邻搜索。IEEE 模式分析和机器智能交易，42(4):824–836, 2018。Alex Mallen、Akari Asai、Victor Zhu、Rajarshi Das、Daniel Khashabi 和 Hannaneh Hajishirzi。何时不信任语言模型：研究参数和非参数记忆的有效性。载于 Anna Rogers、Jordan Boyd-Graber 和 Naoaki Okazaki（编辑），计算语言学协会第 61 届年会论文集（第 1 卷：长论文），第 9802-9822 页，加拿大多伦多，2023 年 7 月。

### 段落 397 · Page 52

**EN**

Association for Computational Linguistics. doi: 10.18653/v1/2023.acl-long.546. URL https://aclanthology.org/2023.acl-long.546/. Antonio Mallia, Omar Khattab, Torsten Suel, and Nicola Tonellotto. Learning passage impacts for inverted indexes. InProceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 1723–1727, 2021. Gary Marchionini. Exploratory search: from finding to understanding.Communications of the ACM, 49(4): 41–46, April 2006. doi: 10.1145/1121949.1121979.

**中文**

计算语言学协会。 doi：10.18653/v1/2023.acl-long.546。网址 https://aclanthology.org/2023.acl-long.546/。安东尼奥·马利亚、奥马尔·哈塔布、托斯顿·苏尔和尼古拉·托内洛托。学习段落对倒排索引的影响。第 44 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 1723-1727 页，2021 年。Gary Marchionini。探索性搜索：从发现到理解。Communications of the ACM，49(4)：41–46，2006 年 4 月。doi：10.1145/1121949.1121979。

### 段落 398 · Page 52

**EN**

Sanket Vaibhav Mehta, Jai Gupta, Yi Tay, Mostafa Dehghani, Vinh Q Tran, Jinfeng Rao, Marc Najork, Emma Strubell, and Donald Metzler. DSI++: Updating transformer memory with new documents. In Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, pp. 8198–8213, 2023. 52

**中文**

Sanket Vaibhav Mehta、Jai Gupta、Yi Tay、Mostafa Dehghani、Vinh Q Tran、Jinfeng Rao、Marc Najork、Emma Strubell 和 Donald Metzler。 DSI++：使用新文档更新Transformer内存。 2023 年自然语言处理经验方法会议论文集，第 8198–8213 页，2023 年。 52

### Page 53

### 段落 399 · Page 53

**EN**

Published in Transactions on Machine Learning Research (02/2026) Lang Mei, Siyu Mo, Zhihan Yang, and Chong Chen. A survey of Multimodal Retrieval-Augmented Generation. arXiv preprint arXiv:2504.08748, 2025. Tomas Mikolov, Kai Chen, Greg Corrado, and Jeffrey Dean. Efficient estimation of word representations in vector space.arXiv preprint arXiv:1301.3781, 2013. David R. H. Miller, Tim Leek, and Richard M. Schwartz. A hidden markov model information retrieval system. InProceedings of the 22nd Annual International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 214–221, 1999.

**中文**

发表于机器学习研究汇刊 (02/2026) Lang Mei、Siyu Mo、Zhihan Yang 和 Chong Chen。多模态检索增强生成的调查。 arXiv 预印本 arXiv：2504.08748，2025。Tomas Mikolov、Kai Chen、Greg Corrado 和 Jeffrey Dean。向量空间中单词表示的高效估计。arXiv 预印本 arXiv:1301.3781, 2013。David R. H. Miller、Tim Leek 和 Richard M. Schwartz。隐马尔可夫模型信息检索系统。第 22 届国际 ACM SIGIR 信息检索研究与开发年度会议论文集，第 214-221 页，1999 年。

### 段落 400 · Page 53

**EN**

Matthias Minderer, Josip Djolonga, Rob Romijnders, Frances Ann Hubis, Xiaohua Zhai, Neil Houlsby, Dustin Tran, and Mario Lucic. Revisiting the calibration of modern neural networks.arXiv preprint arXiv:2106.07998, 2021. Bhaskar Mitra, Eric Nalisnick, Nick Craswell, and Rich Caruana. A dual embedding space model for document ranking.arXiv preprint arXiv:1602.01137, 2016. Bhaskar Mitra, Fernando Diaz, and Nick Craswell. Learning to match using local and distributed representations of text for web search. InProceedings of the 26th International Conference on World Wide Web, WWW ’17, pp. 1291–1299, Republic and Canton of Geneva, CHE, 2017.

**中文**

马蒂亚斯·明德勒、乔西普·德乔隆加、罗布·罗明德斯、弗朗西斯·安·胡比斯、翟晓华、尼尔·霍尔斯比、达斯汀·特兰和马里奥·卢西奇。重新审视现代神经网络的校准。arXiv 预印本 arXiv:2106.07998, 2021。Bhaskar Mitra、Eric Nalisnick、Nick Craswell 和 Rich Caruana。用于文档排名的双嵌入空间模型。arXiv 预印本 arXiv:1602.01137, 2016。Bhaskar Mitra、Fernando Diaz 和 Nick Craswell。学习使用本地和分布式文本表示进行网络搜索匹配。第 26 届万维网国际会议记录，WWW ’17，第 1291–1299 页，日内瓦共和国和州，CHE，2017 年。

### 段落 401 · Page 53

**EN**

International World Wide Web Conferences Steering Committee. doi: 10.1145/3038912.3052579. Bhaskar Mitra, Nick Craswell, et al. An introduction to neural information retrieval.Foundations and Trends in Information Retrieval, 13(1):1–126, 2018. Bhaskar Mitra, Sebastian Hofstätter, Hamed Zamani, and Nick Craswell. Improving transformer-kernel ranking model using conformer and query term independence. InProceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 1697–1702, 2021. Fengran Mo, Kelong Mao, Yutao Zhu, Yihong Wu, Kaiyu Huang, and Jian-Yun Nie.

**中文**

国际万维网会议指导委员会。 DOI：10.1145/3038912.3052579。巴斯卡·米特拉、尼克·克拉斯韦尔等人。神经信息检索简介。信息检索的基础和趋势，13(1):1–126, 2018。Bhaskar Mitra、Sebastian Hofstätter、Hamed Zamani 和 Nick Craswell。使用一致性和查询项独立性改进Transformer内核排名模型。第 44 届国际 ACM SIGIR 信息检索研究与发展会议论文集，第 1697-1702 页，2021 年。Fengran Mo、Kelong Mao、Yutao Zhu、Yihong Wu、Kaiyu Huang 和 Jen-Yun Nie。

### 段落 402 · Page 53

**EN**

ConvGQR: Generative query reformulation for conversational search. InProceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp. 4998–5012, 2023. Fengran Mo, Abbas Ghaddar, Kelong Mao, Mehdi Rezagholizadeh, Boxing Chen, Qun Liu, and Jian-Yun Nie. CHIQ: Contextual history enhancement for improving query rewriting in conversational search.arXiv preprint arXiv:2406.05013, 2024a. Fengran Mo, Kelong Mao, Ziliang Zhao, Hongjin Qian, Haonan Chen, Yiruo Cheng, Xiaoxi Li, Yutao Zhu, Zhicheng Dou, and Jian-Yun Nie. A survey of conversational search.arXiv preprint arXiv:2410.15576, 2024b.

**中文**

ConvGQR：对话式搜索的生成查询重构。计算语言学协会第 61 届年会记录（第一卷：长论文），第 4998–5012 页，2023 年。莫枫然、Abbas Ghaddar、毛克龙、Mehdi Rezagholizadeh、陈博星、刘群和聂建云。 CHIQ：上下文历史记录增强，用于改进会话搜索中的查询重写。arXiv 预印本 arXiv：2406.05013，2024a。莫枫然、毛克龙、赵子良、钱宏进、陈浩南、程一若、李晓西、朱玉涛、窦志成和聂建云。对话式搜索调查。arXiv 预印本 arXiv:2410.15576, 2024b。

### 段落 403 · Page 53

**EN**

Fengran Mo, Bole Yi, Kelong Mao, Chen Qu, Kaiyu Huang, and Jian-Yun Nie. ConvSDG: Session data generation for conversational search. InCompanion Proceedings of the ACM on Web Conference 2024, pp. 1634–1642, 2024c. Iurii Mokrii, Leonid Boytsov, and Pavel Braslavski. A systematic evaluation of transfer learning and pseudolabeling with BERT-based ranking models. InProceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’21, pp. 2081–2085, New York, NY, USA, 2021. Association for Computing Machinery. doi: 10.1145/3404835.3463093. NiklasMuennighoff.

**中文**

莫枫然、易伯乐、毛克龙、曲陈、黄凯宇、聂建云。 ConvSDG：用于会话搜索的会话数据生成。 In Companion Proceedings of the ACM on Web Conference 2024，第 1634–1642 页，2024c。尤里·莫克里、列昂尼德·博伊佐夫和帕维尔·布拉斯拉夫斯基。使用基于 BERT 的排序模型对迁移学习和伪标签进行系统评估。 InProceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR '21, pp. 2081–2085, New York, NY, USA, 2021. 计算机协会。号码：10.1145/3404835.3463093。尼克拉斯·穆尼尼霍夫。

### 段落 404 · Page 53

**EN**

SGPT:GPTsentenceembeddingsforsemanticsearch.arXiv preprint arXiv:2202.08904, 2022. Niklas Muennighoff, Nouamane Tazi, Loic Magne, and Nils Reimers. MTEB: Massive text embedding benchmark. In Andreas Vlachos and Isabelle Augenstein (eds.),Proceedings of the 17th Conference of the European Chapter of the Association for Computational Linguistics, pp. 2014–2037, Dubrovnik, Croatia, May 2023. Association for Computational Linguistics. doi: 10.18653/v1/2023.eacl-main.148. URLhttps: //aclanthology.org/2023.eacl-main.148/. 53

**中文**

SGPT:GPTsentenceembeddingsforsemanticsearch.arXiv 预印本 arXiv:2202.08904, 2022。Niklas Muennighoff、Nouamane Tazi、Loic Magne 和 Nils Reimers。 MTEB：海量文本嵌入基准。 In Andreas Vlachos 和 Isabelle Augenstein（编辑），计算语言学协会欧洲分会第 17 届会议论文集，第 2014-2037 页，克罗地亚杜布罗夫尼克，2023 年 5 月。计算语言学协会。 doi：10.18653/v1/2023.eacl-main.148。网址https://aclanthology.org/2023.eacl-main.148/。 53

### Page 54

### 段落 405 · Page 54

**EN**

Published in Transactions on Machine Learning Research (02/2026) Niklas Muennighoff, Hongjin Su, Liang Wang, Nan Yang, Furu Wei, Tao Yu, Amanpreet Singh, and Douwe Kiela. Generative representational instruction tuning. InThe 13th International Conference on Learning Representations, 2025. URLhttps://openreview.net/forum?id=BC4lIvfSzv. Reiichiro Nakano, Jacob Hilton, Suchir Balaji, Jeff Wu, Long Ouyang, Christina Kim, Christopher Hesse, Shantanu Jain, Vineet Kosaraju, William Saunders, et al. WebGPT: Browser-assisted question-answering with human feedback.arXiv preprint arXiv:2112.09332, 2021.

**中文**

发表于机器学习研究汇刊 (02/2026) Niklas Muennighoff、Hongjin Su、Liang Wang、Nan Yang、Furu Wei、Tao Yu、Amanpreet Singh 和 Douwe Kiela。生成代表性指令调整。在第 13 届学习表征国际会议，2025 年。网址 https://openreview.net/forum?id=BC4lIvfSzv。 Reiichiro Nakano、Jacob Hilton、Sucher Balaji、Jeff Wu、Long Ouyang、Christina Kim、Christopher Hesse、Shantanu Jain、Vineet Kosaraju、William Saunders 等。 WebGPT：具有人类反馈的浏览器辅助问答。arXiv 预印本 arXiv：2112.09332，2021。

### 段落 406 · Page 54

**EN**

Eric Nalisnick, Bhaskar Mitra, Nick Craswell, and Rich Caruana. Improving document ranking with dual word embeddings. InProceedings of the 25th International Conference Companion on World Wide Web, WWW ’16 Companion, pp. 83–84, Republic and Canton of Geneva, CHE, 2016. International World Wide Web Conferences Steering Committee. doi: 10.1145/2872518.2889361. Pandu Nayak. Understanding searches better than ever before.https://blog.google/products/search/ search-language-understanding-bert/, 2019. Arvind Neelakantan, Tao Xu, Raul Puri, Alec Radford, Jesse Michael Han, Jerry Tworek, Qiming Yuan, NikolasTezak, JongWookKim, ChrisHallacy, etal.

**中文**

埃里克·纳利斯尼克、巴斯卡·米特拉、尼克·克拉斯韦尔和里奇·卡鲁阿纳。通过双词嵌入提高文档排名。 InProceedings of the 25th International Conference Companion on World Wide Web，WWW '16 Companion，第 83-84 页，日内瓦共和国和州，CHE，2016 年。国际万维网会议指导委员会。号码：10.1145/2872518.2889361。潘杜·纳亚克。比以往更好GEO解搜索。https://blog.google/products/search/search-language-understanding-bert/，2019。Arvind Neelakantan、Tao Xu、Raul Puri、Alec Radford、Jesse Michael Han、Jerry Tworek、Qiming Yuan、NikolasTezak、JongWookKim、ChrisHallacy 等。

### 段落 407 · Page 54

**EN**

Textandcodeembeddingsbycontrastivepre-training. arXiv preprint arXiv:2201.10005, 2022. Thong Nguyen, Sean MacAvaney, and Andrew Yates. A unified framework for learned sparse retrieval. In European Conference on Information Retrieval, pp. 101–116. Springer, 2023. Jianmo Ni, Gustavo Hernandez Abrego, Noah Constant, Ji Ma, Keith Hall, Daniel Cer, and Yinfei Yang. Sentence-T5: Scalable sentence encoders from pre-trained text-to-text models. In Smaranda Muresan, Preslav Nakov, and Aline Villavicencio (eds.),Findings of the Association for Computational Linguistics: ACL 2022, pp. 1864–1874, Dublin, Ireland, May 2022a.

**中文**

通过对比预训练进行文本和代码嵌入。 arXiv 预印本 arXiv:2201.10005, 2022。Thong Nguyen、Sean MacAvaney 和 Andrew Yates。用于学习稀疏检索的统一框架。欧洲信息检索会议，第 101-116 页。施普林格，2023。倪建模、古斯塔沃·埃尔南德斯·阿布雷戈、诺亚·康斯坦特、马吉、基思·霍尔、丹尼尔·塞尔和杨银飞。 Sentence-T5：来自预先训练的文本到文本模型的可扩展句子编码器。 Smaranda Muresan、Preslav Nakov 和 Aline Villavicencio（编辑），计算语言学协会的调查结果：ACL 2022，第 1864–1874 页，爱尔兰都柏林，2022 年 5 月a。

### 段落 408 · Page 54

**EN**

Association for Computational Linguistics. doi: 10.18653/v1/2022.findings-acl.146. URLhttps://aclanthology.org/2022.findings-acl.146/. Jianmo Ni, Chen Qu, Jing Lu, Zhuyun Dai, Gustavo Hernandez Abrego, Ji Ma, Vincent Zhao, Yi Luan, Keith Hall, Ming-Wei Chang, and Yinfei Yang. Large dual encoders are generalizable retrievers. In Yoav Goldberg, Zornitsa Kozareva, and Yue Zhang (eds.),Proceedings of the 2022 Conference on Empirical Methods in Natural Language Processing, pp. 9844–9855, Abu Dhabi, United Arab Emirates, December 2022b. Association for Computational Linguistics. doi: 10.18653/v1/2022.emnlp-main.669.

**中文**

计算语言学协会。 doi：10.18653/v1/2022.findings-acl.146。网址https://aclanthology.org/2022.findings-acl.146/。倪建模、曲陈、陆静、戴竹云、Gustavo Hernandez Abrego、马季、赵文森、栾毅、Keith Hall、张明伟和杨银飞。大型双编码器是通用的检索器。载于 Yoav Goldberg、Zornitsa Kozareva 和 Yue Zhu（编辑），2022 年自然语言处理经验方法会议论文集，第 9844-9855 页，阿拉伯联合酋长国阿布扎比，2022 年 12 月b。计算语言学协会。 doi：10.18653/v1/2022.emnlp-main.669。

### 段落 409 · Page 54

**EN**

URLhttps: //aclanthology.org/2022.emnlp-main.669/. Jian-Yun Nie.Cross-language information retrieval. Morgan & Claypool Publishers, 2010. Priyank Nigam, Yiwei Song, Vijai Mohan, Vihan Lakshman, Weitian Ding, Ankit Shingavi, Choon Hui Teo, Hao Gu, and Bing Yin. Semantic product search.Proceedings of the 25th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, 2019. Rodrigo Nogueira, Jimmy Lin, and A. I. Epistemic. From doc2query to docTTTTTquery.Online preprint, 6(2), 2019a. Rodrigo Nogueira, Wei Yang, Kyunghyun Cho, and Jimmy Lin. Multi-stage document ranking with BERT. arXiv preprint arXiv:1910.14424, 2019b.

**中文**

网址https://aclanthology.org/2022.emnlp-main.669/。聂建云. 跨语言信息检索。 Morgan & Claypool Publishers，2010。Priyank Nigam、Yiwei Song、Vijai Mohan、Vihan Lakshman、Weitian Ding、Ankit Shingavi、Choon Hui Teo、Hao Gu 和 Bing Yin。语义产品搜索。第 25 届 ACM SIGKDD 国际知识发现与数据挖掘会议论文集，2019 年。Rodrigo Nogueira、Jimmy Lin 和 A. I. Epistemic。从 doc2query 到 docTTTTTquery。在线预印本，6(2)，2019a。罗德里戈·诺盖拉、杨伟、曹京贤和林志颖。使用 BERT 进行多阶段文档排名。 arXiv 预印本 arXiv:1910.14424, 2019b。

### 段落 410 · Page 54

**EN**

Rodrigo Nogueira, Zhiying Jiang, and Jimmy Lin. Document ranking with a pretrained sequence-to-sequence model. arXiv preprint arXiv:2003.06713, 2020. Cicero Nogueira dos Santos, Xiaofei Ma, Ramesh Nallapati, Zhiheng Huang, and Bing Xiang. Beyond [CLS] through ranking by generation. In Bonnie Webber, Trevor Cohn, Yulan He, and Yang Liu (eds.), Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 1722–1727, Online, November 2020. Association for Computational Linguistics. doi: 10.18653/v1/2020. emnlp-main.134. URLhttps://aclanthology.org/2020.emnlp-main.134/. Zach Nussbaum and Brandon Duderstadt.

**中文**

罗德里戈·诺盖拉、蒋志英和林志颖。使用预训练的序列到序列模型进行文档排名。 arXiv 预印本 arXiv:2003.06713, 2020。Cicero Nogueira dos Santos、Xiaofei Ma、Ramesh Nallapati、Zhiheng Huang 和 Bing Xing。通过逐代排名超越[CLS]。收录于 Bonnie Webber、Trevor Cohn、Yulan He 和 Yang Liu（编辑），2020 年自然语言处理经验方法 (EMNLP) 会议论文集，第 1722-1727 页，在线，2020 年 11 月。计算语言学协会。 doi：10.18653/v1/2020。 emnlp-main.134。网址https://aclanthology.org/2020.emnlp-main.134/。扎克·努斯鲍姆和布兰登·杜德施塔特。

### 段落 411 · Page 54

**EN**

Training sparse mixture of experts text embedding models. arXiv preprint arXiv:2502.07972, 2025. 54

**中文**

训练专家文本嵌入模型的稀疏混合。 arXiv 预印本 arXiv:2502.07972, 2025. 54

### Page 55

### 段落 412 · Page 55

**EN**

Published in Transactions on Machine Learning Research (02/2026) Zach Nussbaum, John Xavier Morris, Andriy Mulyar, and Brandon Duderstadt. Nomic Embed: Training a reproducible long context text embedder.Transactions on Machine Learning Research, 2025. URL https://openreview.net/forum?id=IPmzyQSiQE. Douglas Oard, Carol Peters, Miguel Ruiz, Robert Frederking, Judith Klavans, and Paraic Sheridan. Multilingual Information Discovery and AccesS (MIDAS).D-Lib Magazine, 5(10), 1999. doi: 10.1045/ october99-oard. Douglas W. Oard and Bonnie J. Dorr. A survey of multilingual text retrieval.

**中文**

发表于机器学习研究汇刊 (02/2026) Zach Nussbaum、John Xavier Morris、Andriy Mulyar 和 Brandon Duderstadt。 Nomic Embed：训练可重复的长上下文文本嵌入器。机器学习研究交易，2025。URL https://openreview.net/forum?id=IPmzyQSiQE。道格拉斯·奥德、卡罗尔·彼得斯、米格尔·鲁伊斯、罗伯特·弗雷德金、朱迪思·克拉万斯和帕里克·谢里登。多语言信息发现和访问 (MIDAS)。D-Lib 杂志，5(10)，1999。doi：10.1045/october99-oard。道格拉斯·W·奥德 (Douglas W. Oard) 和邦妮·J·多尔 (Bonnie J. Dorr)。多语言文本检索调查。

### 段落 413 · Page 55

**EN**

Technical Report UMIACS- TR-96-19 CS-TR-3615, University of Maryland Institute for Advanced Computer Studies, 1996. Douglas W. Oard and Bonnie J. Dorr. Evaluating cross-language text filtering effectiveness. InCross- Language Information Retrieval, pp. 151–161. Springer, 1998. Hanseok Oh, Hyunji Lee, Seonghyeon Ye, Haebin Shin, Hansol Jang, Changwook Jun, and Minjoon Seo. INSTRUCTIR: A benchmark for instruction following of information retrieval models.arXiv preprint arXiv:2402.14334, 2024. Bruno Oliveira and Carla Teixeira Lopes.

**中文**

技术报告 UMIACS-TR-96-19 CS-TR-3615，马里兰大学高级计算机研究所，1996 年。Douglas W. Oard 和 Bonnie J. Dorr。评估跨语言文本过滤的有效性。 《跨语言信息检索》，第 151–161 页。 Springer，1998。Hanseok Oh、Hyunji Lee、Seonghyeon Ye、Haebin Shin、Hansol Jang、Changwook Jun 和 Minjoon Seo。 INSTRUCTIR：信息检索模型指令跟踪的基准。arXiv 预印本 arXiv：2402.14334，2024。Bruno Oliveira 和 Carla Teixeira Lopes。

### 段落 414 · Page 55

**EN**

From 10 blue links pages to feature-full search engine results pages - analysis of the temporal evolution of SERP features. InProceedings of the 2023 Conference on Human Information Interaction and Retrieval, pp. 338–345. ACM, March 2023. doi: 10.1145/3576840.3578307. Kezban Dilek Onal, Ye Zhang, Ismail Sengor Altingovde, Md Mustafizur Rahman, Pinar Karagoz, Alex Braylan, Brandon Dang, Heng-Lu Chang, Henna Kim, Quinten McNamara, et al. Neural information retrieval: At the end of the early years.Information Retrieval Journal, 21:111–182, 2018. Aaron van den Oord, Yazhe Li, and Oriol Vinyals.

**中文**

从 10 个蓝色链接页面到功能齐全的搜索引擎结果页面 - SERP 功能的时间演变分析。 2023 年人类信息交互与检索会议记录，第 338-345 页。 ACM，2023 年 3 月。doi：10.1145/3576840.3578307。 Kezban Dilek Onal、张晔、Ismail Sengor Altingovde、Md Mustafizur Ra​​hman、Pinar Karagoz、Alex Braylan、Brandon Dang、Heng-Lu Chang、Henna Kim、Quinten McNamara 等。神经信息检索：早年末期。《信息检索杂志》，21:111–182, 2018。Aaron van den Oord、Yazhe Li 和 Oriol Vinyals。

### 段落 415 · Page 55

**EN**

Representation learning with contrastive predictive coding.arXiv preprint arXiv:1807.03748, 2018. OpenAI. Introducing ChatGPT.https://openai.com/index/chatgpt/, 2022. OpenAI. Introducing ChatGPT search.https://openai.com/index/introducing-chatgpt-search/, 2024. OpenAI. Introducing deep research.https://openai.com/index/introducing-deep-research/, 2025. OpenAI, Josh Achiam, Steven Adler, Sandhini Agarwal, Lama Ahmad, Ilge Akkaya, et al. GPT-4 technical report.arXiv preprint arXiv:2303.08774, 2023. OpenAI, Aaron Hurst, Adam Lerer, Adam P. Goucher, Adam Perelman, Aditya Ramesh, et al. GPT-4o system card. arXiv preprint arXiv:2410.21276, 2024.

**中文**

使用对比预测编码进行表示学习。arXiv 预印本 arXiv:1807.03748, 2018。OpenAI。 ChatGPT 简介。https://openai.com/index/chatgpt/，2022。OpenAI。 ChatGPT 搜索简介。https://openai.com/index/introducing-chatgpt-search/，2024。OpenAI。介绍深度研究。https://openai.com/index/introducing-deep-research/，2025。OpenAI、Josh Achiam、Steven Adler、Sandhini Agarwal、Lama Ahmad、Ilge Akkaya 等。 GPT-4 技术报告.arXiv 预印本 arXiv:2303.08774, 2023。OpenAI、Aaron Hurst、Adam Lerer、Adam P. Goucher、Adam Perelman、Aditya Ramesh 等人。 GPT-4o 系统卡。 arXiv 预印本 arXiv:2410.21276, 2024。

### 段落 416 · Page 55

**EN**

Hamid Palangi, Li Deng, Yelong Shen, Jianfeng Gao, Xiaodong He, Jianshu Chen, Xinying Song, and Rabab Ward. Deep sentence embedding using long short-term memory networks: analysis and application to information retrieval.IEEE Transactions on Audio, Speech and Language Processing, 24(4):694–707, 2016. doi: 10.1109/TASLP.2016.2520371. Liang Pang, Yanyan Lan, Jiafeng Guo, Jun Xu, Shengxian Wan, and Xueqi Cheng. Text matching as image recognition. InProceedings of the 30th AAAI Conference on Artificial Intelligence, AAAI’16, pp. 2793–2799. AAAI Press, 2016. Liang Pang, Jun Xu, Qingyao Ai, Yanyan Lan, Xueqi Cheng, and Ji-Rong Wen.

**中文**

Hamid Palangi、邓力、沉叶龙、高剑峰、何晓东、陈建树、宋欣颖和 Rabab Ward。使用长短期记忆网络的深度句子嵌入：信息检索的分析和应用。IEEE 音频、语音和语言处理交易，24(4):694–707, 2016。doi: 10.1109/TASLP.2016.2520371。庞亮、兰岩岩、郭家峰、徐军、万胜贤、程学奇。文本匹配作为图像识别。第 30 届 AAAI 人工智能会议论文集，AAAI’16，第 2793-2799 页。 AAAI 出版社，2016。庞亮，徐军，艾清耀，兰岩岩，程学奇，温继荣。

### 段落 417 · Page 55

**EN**

SetRank: Learning a permutation-invariant ranking model for information retrieval. InProceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 499–508, 2020. Eunhwan Park, Sung-Min Lee, Dearyong Seo, Seonhoon Kim, Inho Kang, and Seung-Hoon Na. RINK: Reader-inherited evidence reranker for table-and-text open domain question answering authors. InProceedings of the AAAI Conference on Artificial Intelligence, volume 37, pp. 13446–13456, 2023. 55

**中文**

SetRank：学习用于信息检索的排列不变排序模型。第 43 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 499-508 页，2020 年。Eunhwan Park、Sung-Min Lee、Dearyong Seo、Seonhoon Kim、Inho Kang 和 Seung-Hoon Na。 RINK：针对表格和文本开放域问答作者的读者继承的证据重新排序器。载于 AAAI 人工智能会议记录，第 37 卷，第 13446–13456 页，2023 年。 55

### Page 56

### 段落 418 · Page 56

**EN**

Published in Transactions on Machine Learning Research (02/2026) Shishir G. Patil, Huanzhi Mao, Charlie Cheng-Jie Ji, Fanjia Yan, Vishnu Suresh, Ion Stoica, and Joseph E. Gonzalez. The berkeley function calling leaderboard (BFCL): From tool use to agentic evaluation of large language models. InAdvances in Neural Information Processing Systems, 2024a. Shishir G. Patil, Tianjun Zhang, Xin Wang, and Joseph E. Gonzalez. Gorilla: Large Language Model connected with massive APIs. InThe 38th Annual Conference on Neural Information Processing Systems, 2024b. URLhttps://openreview.net/forum?id=tBRNC6YemY.

**中文**

发表于《机器学习研究汇刊》(02/2026) Shishir G. Patil、Huanzhi Mao、Charlie Cheng-Jie Ji、Fanjia Yan、Vishnu Suresh、Ion Stoica 和 Joseph E. Gonzalez。伯克利函数调用排行榜 (BFCL)：从工具使用到大型语言模型的代理评估。神经信息处理系统进展，2024a。 Shishir G. Patil、张天军、王鑫和 Joseph E. Gonzalez。 Gorilla：与大量 API 连接的大型语言模型。在第 38 届神经信息处理系统年会，2024b。网址https://openreview.net/forum?id=tBRNC6YemY。

### 段落 419 · Page 56

**EN**

Bo Peng, Eric Alcaide, Quentin Anthony, Alon Albalak, Samuel Arcadinho, Stella Biderman, Huanqi Cao, Xin Cheng, Michael Chung, Leon Derczynski, Xingjian Du, Matteo Grella, Kranthi Gv, Xuzheng He, Haowen Hou, Przemyslaw Kazienko, Jan Kocon, Jiaming Kong, Bartłomiej Koptyra, Hayden Lau, Jiaju Lin, Krishna Sri Ipsit Mantri, Ferdinand Mom, Atsushi Saito, Guangyu Song, Xiangru Tang, Johan Wind, Stanisław Woźniak, Zhenyuan Zhang, Qinghua Zhou, Jian Zhu, and Rui-Jie Zhu. RWKV: Reinventing RNNs for the transformer era. In Houda Bouamor, Juan Pino, and Kalika Bali (eds.),Findings of the Association for Computational Linguistics: EMNLP 2023, pp.

**中文**

彭博、埃里克·阿尔凯德、昆汀·安东尼、阿隆·阿尔巴拉克、塞缪尔·阿卡迪尼奥、斯特拉·比德曼、曹焕奇、程鑫、迈克尔·钟、莱昂·德尔钦斯基、杜行建、马泰奥·格雷拉、Kranthi Gv、何旭正、侯浩文、普热米斯瓦夫·卡津科、扬·科孔、孔家明、巴特沃米耶·科普蒂拉、刘海登、林家驹、 Krishna Sri Ipsit Mantri、Ferdinand Mom、Atsushi Saito、Guangyu Song、Xiangru Tang、Johan Wind、Stanisław Wozniak、Zhenyuan 张、Qinghua Zhou、Jian Zhu 和 Rui-Jie Zhu。 RWKV：为 Transformer 时代重新发明 RNN。载于 Houda Bouamor、Juan Pino 和 Kalika Bali（编辑），计算语言学协会的调查结果：EMNLP 2023，第 143 页。

### 段落 420 · Page 56

**EN**

14048–14077, Singapore, 2023. Association for Computational Linguistics. doi: 10.18653/v1/2023.findings-emnlp.936. URLhttps://aclanthology. org/2023.findings-emnlp.936/. Bo Peng, Daniel Goldstein, Quentin Anthony, Alon Albalak, Eric Alcaide, Stella Biderman, Eugene Cheah, Xingjian Du, Teddy Ferdinan, Haowen Hou, et al. Eagle and finch: RWKV with matrix-valued states and dynamic recurrence.arXiv preprint arXiv:2404.05892, 2024a. Wenjun Peng, Guiyang Li, Yue Jiang, Zilong Wang, Dan Ou, Xiaoyi Zeng, Derong Xu, Tong Xu, and Enhong Chen. Large language model based long-tail query rewriting in Taobao search.

**中文**

14048–14077，新加坡，2023 年。计算语言学协会。 doi：10.18653/v1/2023.findings-emnlp.936。网址https://aclanthology. org/2023.findings-emnlp.936/。彭波、丹尼尔·戈尔茨坦、昆汀·安东尼、阿隆·阿尔巴拉克、埃里克·阿尔凯德、斯特拉·比德曼、尤金·谢、杜行健、泰迪·费迪南、侯浩文等。 Eagle 和 Finch：具有矩阵值状态和动态递归的 RWKV。arXiv 预印本 arXiv：2404.05892，2024a。彭文军、李贵阳、江悦、王子龙、欧丹、曾小毅、徐德荣、徐童和陈恩宏。基于大语言模型的淘宝搜索长尾查询重写

### 段落 421 · Page 56

**EN**

InCompanion Proceedings of the ACM Web Conference 2024, WWW ’24, pp. 20–28, New York, NY, USA, 2024b. Association for Computing Machinery. doi: 10.1145/3589335.3648298. Gustavo Penha and Claudia Hauff. On the calibration and uncertainty of neural learning to rank models for conversational search. In Paola Merlo, Jorg Tiedemann, and Reut Tsarfaty (eds.),Proceedings of the 16th Conference of the European Chapter of the Association for Computational Linguistics: Main Volume, pp. 160–170, Online, April 2021. Association for Computational Linguistics. doi: 10.18653/v1/2021.eacl-main. 12. URLhttps://aclanthology.org/2021.eacl-main.12/.

**中文**

InCompanion Proceedings of the ACM Web Conference 2024，WWW '24，第 20-28 页，美国纽约州纽约，2024b。计算机器协会。号码：10.1145/3589335.3648298。古斯塔沃·佩尼亚和克劳迪娅·豪夫。关于神经学习对会话搜索模型进行排序的校准和不确定性。见 Paola Merlo、Jorg Tiedemann 和 Reut Tsarfaty（编辑），计算语言学协会欧洲分会第 16 届会议记录：主卷，第 160-170 页，在线，2021 年 4 月。计算语言学协会。 doi：10.18653/v1/2021.eacl-main。 12.网址https://aclanthology.org/2021.eacl-main.12/。

### 段落 422 · Page 56

**EN**

Jeffrey Pennington, Richard Socher, and Christopher Manning. GloVe: Global vectors for word representation. In Alessandro Moschitti, Bo Pang, and Walter Daelemans (eds.),Proceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 1532–1543, Doha, Qatar, October 2014. Association for Computational Linguistics. doi: 10.3115/v1/D14-1162. URL https://aclanthology.org/D14-1162/. Fabio Petroni, Aleksandra Piktus, Angela Fan, Patrick Lewis, Majid Yazdani, Nicola De Cao, James Thorne, Yacine Jernite, Vladimir Karpukhin, Jean Maillard, et al. KILT: a benchmark for knowledge intensive language tasks.

**中文**

杰弗里·彭宁顿、理查德·索彻和克里斯托弗·曼宁。 GloVe：用于单词表示的全局向量。载于 Alessandro Moschitti、Bo Pang 和 Walter Daelemans（编辑），2014 年自然语言处理经验方法 (EMNLP) 会议论文集，第 1532–1543 页，卡塔尔多哈，2014 年 10 月。计算语言学协会。 doi：10.3115/v1/D14-1162。网址 https://aclanthology.org/D14-1162/。 Fabio Petroni、Aleksandra Piktus、Angela Fan、Patrick Lewis、Majid Yazdani、Nicola De Cao、James Thorne、Yacine Jernite、Vladimir Karpukhin、Jean Maillard 等。 KILT：知识密集型语言任务的基准。

### 段落 423 · Page 56

**EN**

InProceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, pp. 2523–2544, 2021. Jonas Pfeiffer, Ivan Vulić, Iryna Gurevych, and Sebastian Ruder. MAD-X: An Adapter-Based Framework for Multi-Task Cross-Lingual Transfer. In Bonnie Webber, Trevor Cohn, Yulan He, and Yang Liu (eds.), Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 7654–7673, Online, November 2020. Association for Computational Linguistics. doi: 10.18653/v1/2020. emnlp-main.617. URLhttps://aclanthology.org/2020.emnlp-main.617/.

**中文**

计算语言学协会北美分会 2021 年会议记录：人类语言技术，第 2523-2544 页，2021 年。Jonas Pfeiffer、Ivan Vulić、Iryna Gurevych 和 Sebastian Ruder。 MAD-X：基于适配器的多任务跨语言传输框架。收录于 Bonnie Webber、Trevor Cohn、Yulan He 和 Yang Liu（编），2020 年自然语言处理经验方法 (EMNLP) 会议论文集，第 7654–7673 页，在线，2020 年 11 月。计算语言学协会。 doi：10.18653/v1/2020。 emnlp-main.617。网址https://aclanthology.org/2020.emnlp-main.617/。

### 段落 424 · Page 56

**EN**

Jonas Pfeiffer, Aishwarya Kamath, Andreas Rücklé, Kyunghyun Cho, and Iryna Gurevych. AdapterFusion: Non-destructivetaskcompositionfortransferlearning. InPaolaMerlo, JorgTiedemann, andReutTsarfaty (eds.),Proceedings of the 16th Conference of the European Chapter of the Association for Computational Linguistics: Main Volume, pp. 487–503, Online, April 2021. Association for Computational Linguistics. doi: 10.18653/v1/2021.eacl-main.39. URLhttps://aclanthology.org/2021.eacl-main.39/. Jay M. Ponte and W. Bruce Croft. A language modeling approach to information retrieval.

**中文**

乔纳斯·菲佛、艾西瓦娅·卡马斯、安德烈亚斯·吕克莱、曹景贤和伊琳娜·古列维奇。 AdapterFusion：用于迁移学习的非破坏性任务组合。 InPaola Merlo、JorgTiedemann 和 ReutTsarfaty（编辑），计算语言学协会欧洲分会第 16 届会议记录：主卷，第 487-503 页，在线，2021 年 4 月。计算语言学协会。 doi：10.18653/v1/2021.eacl-main.39。网址https://aclanthology.org/2021.eacl-main.39/。杰伊·M·庞特 (Jay M. Ponte) 和 W·布鲁斯·克罗夫特 (W. Bruce Croft)。信息检索的语言建模方法。

### 段落 425 · Page 56

**EN**

InProceedings of the 21st Annual International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 275–281, 1998. 56

**中文**

第 21 届国际 ACM SIGIR 信息检索研究与开发年会论文集，第 275-281 页，1998 年。 56

### Page 57

### 段落 426 · Page 57

**EN**

Published in Transactions on Machine Learning Research (02/2026) JeffPool, AbhishekSawarkar, andJayRodge. AcceleratinginferencewithsparsityusingtheNVIDIAAmpere architecture and NVIDIA TensorRT. NVIDIA Technical Blog, July 2021. URLhttps://developer. nvidia.com/blog/accelerating-inference-with-sparsity-using-ampere-and-tensorrt/. Jacob Portes, Alexander Trott, Sam Havens, Daniel King, Abhinav Venigalla, Moin Nadeem, Nikhil Sardana, Daya Khudia, and Jonathan Frankle. MosaicBERT: A bidirectional encoder optimized for fast pretraining. Advances in Neural Information Processing Systems, 36:3106–3130, 2023.

**中文**

发表于《机器学习研究汇刊》(02/2026) JeffPool、AbhishekSawarkar 和 JayRodge。使用 NVIDIA Ampere 架构和 NVIDIA Tensor RT 加速稀疏推理。 NVIDIA 技术博客，2021 年 7 月。URLhttps://developer。 nvidia.com/blog/acceleating-inference-with-sparsity-using-ampere-and-tensorrt/。雅各布·波特斯、亚历山大·特洛特、萨姆·哈文斯、丹尼尔·金、阿比纳夫·维尼加拉、莫因·纳迪姆、尼基尔·萨达纳、达亚·库迪亚和乔纳森·弗兰克尔。 MosaicBERT：针对快速预训练而优化的双向编码器。神经信息处理系统的进展，36：3106–3130，2023 年。

### 段落 427 · Page 57

**EN**

Jes’us Andr’es Portillo-Quintero, José carlos Ortíz-Bayliss, and Hugo Terashima-Mar’in. A straightforward framework for video retrieval using CLIP. InMexican Conference on Pattern Recognition, 2021. Yashoteja Prabhu and Manik Varma. FastXML: A fast, accurate and stable tree-classifier for extreme multi-label learning. InProceedings of the 20th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, pp. 263–272, 2014. Yashoteja Prabhu, Anil Kag, Shrutendra Harsola, Rahul Agrawal, and Manik Varma. Parabel: Partitioned label trees for extreme classification with application to dynamic search advertising.

**中文**

Jes’us Andr’es Portillo-Quintero、José carlos Ortíz-Bayliss 和 Hugo Terashima-Mar’in。使用 CLIP 进行视频检索的简单框架。墨西哥模式识别会议，2021 年。Yashoteja Prabhu 和 Manik Varma。 FastXML：一种快速、准确且稳定的树分类器，用于极端多标签学习。第 20 届 ACM SIGKDD 国际知识发现和数据挖掘会议论文集，第 263-272 页，2014 年。Yashoteja Prabhu、Anil Kag、Shrutendra Harsola、Rahul Agrawal 和 Manik Varma。 Parabel：用于极端分类的分区标签树，应用于动态搜索广告。

### 段落 428 · Page 57

**EN**

InProceedings of the 2018 World Wide Web Conference, pp. 993–1002, 2018. Ronak Pradeep, Rodrigo Nogueira, and Jimmy Lin. The Expando-Mono-Duo design pattern for text ranking with pretrained sequence-to-sequence models.arXiv preprint arXiv:2101.05667, 2021. Ronak Pradeep, Kai Hui, Jai Gupta, Adam Lelkes, Honglei Zhuang, Jimmy Lin, Donald Metzler, and Vinh Tran. How does generative retrieval scale to millions of passages? In Houda Bouamor, Juan Pino, and Kalika Bali (eds.),Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, pp. 1305–1321, Singapore, December 2023a. Association for Computational Linguistics.

**中文**

2018 年万维网会议记录，第 993-1002 页，2018 年。Ronak Pradeep、Rodrigo Nogueira 和 Jimmy Lin。使用预训练序列到序列模型进行文本排名的 Expando-Mono-Duo 设计模式。arXiv 预印本 arXiv:2101.05667, 2021。Ronak Pradeep、Kai Hui、Jai Gupta、Adam Lelkes、honglei Zhuang、Jimmy Lin、Donald Metzler 和 Vinh Tran。生成检索如何扩展到数百万个段落？载于 Houda Bouamor、Juan Pino 和 Kalika Bali（编辑），2023 年自然语言处理经验方法会议论文集，第 1305-1321 页，新加坡，2023 年 12 月a。计算语言学协会。

### 段落 429 · Page 57

**EN**

doi: 10.18653/v1/2023.emnlp-main.83. URLhttps://aclanthology.org/2023.emnlp-main.83/. Ronak Pradeep, Sahel Sharifymoghaddam, and Jimmy Lin. RankVicuna: Zero-shot listwise document reranking with open-source large language models.arXiv preprint arXiv:2309.15088, 2023b. Ronak Pradeep, Sahel Sharifymoghaddam, and Jimmy Lin. RankZephyr: Effective and robust zero-shot listwise reranking is a breeze!arXiv preprint arXiv: 2312.02724, 2023c. JiaruiQin, JiachenZhu, BoChen, ZhirongLiu, WeiwenLiu, RuimingTang, RuiZhang, YongYu, andWeinan Zhang.

**中文**

doi：10.18653/v1/2023.emnlp-main.83。网址https://aclanthology.org/2023.emnlp-main.83/。罗纳克·普拉迪普 (Ronak Pradeep)、萨赫勒·沙里菲莫加达姆 (Sahel Sharifymoghaddam) 和林志颖 (Jimmy Lin)。 RankVicuna：使用开源大语言模型进行零样本列表文档重排序。arXiv 预印本 arXiv：2309.15088，2023b。罗纳克·普拉迪普 (Ronak Pradeep)、萨赫勒·沙里菲莫加达姆 (Sahel Sharifymoghaddam) 和林志颖 (Jimmy Lin)。 RankZephyr：有效且强大的零样本列表重排轻而易举！arXiv 预印本 arXiv：2312.02724，2023c。秦嘉瑞、朱嘉辰、陈博、刘志荣、刘伟文、唐瑞明、张瑞、宇勇和张伟南。

### 段落 430 · Page 57

**EN**

RankFlow: Joint optimization of multi-stage cascade ranking systems as flows.Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval, 2022. Tao Qin and Tie-Yan Liu. Introducing LETOR 4.0 datasets.arXiv preprint arXiv:1306.2597, 2013. Tao Qin, Tie-Yan Liu, and Hang Li. A general approximation framework for direct optimization of information retrieval measures.Information retrieval, 13:375–397, 2010.

**中文**

RankFlow：多阶段级联排名系统作为流的联合优化。第 45 届国际 ACM SIGIR 信息检索研究与发展会议论文集，2022 年。Tao Qing 和 Tie-Yan Liu。介绍 LETOR 4.0 数据集。arXiv 预印本 arXiv:1306.2597, 2013。Tao Qing、Tie-Yan Liu 和 Hang Li。用于直接优化信息检索措施的通用近似框架。信息检索，13：375–397，2010。

### 段落 431 · Page 57

**EN**

Yujia Qin, Shihao Liang, Yining Ye, Kunlun Zhu, Lan Yan, Yaxi Lu, Yankai Lin, Xin Cong, Xiangru Tang, Bill Qian, Sihan Zhao, Lauren Hong, Runchu Tian, Ruobing Xie, Jie Zhou, Mark Gerstein, dahai li, Zhiyuan Liu, and Maosong Sun. ToolLLM: Facilitating large language models to master 16000+ realworld APIs. InThe 12th International Conference on Learning Representations, 2024a. URLhttps: //openreview.net/forum?id=dHng2O0Jjr. Zhen Qin, Le Yan, Honglei Zhuang, Yi Tay, Rama Kumar Pasumarthi, Xuanhui Wang, Michael Bendersky, and Marc Najork. Are neural rankers still outperformed by gradient boosted decision trees?

**中文**

秦雨佳、梁世豪、叶一宁、朱昆仑、颜蓝、陆亚熙、林彦凯、丛欣、唐相如、钱比尔、赵思涵、洪劳伦、田润初、谢若冰、周杰、马克·格斯坦、李大海、刘志远和孙茂松。 ToolLLM：促进大型语言模型掌握 16000 多个真实世界的 API。在第 12 届学习表征国际会议，2024a。网址https://openreview.net/forum?id=dHng2O0Jjr。秦臻、颜乐、庄红雷、Yi Tay、Rama Kumar Pasumarthi、王宣辉、Michael Bendersky 和 ​​Marc Najork。梯度提升决策树的性能是否仍优于神经排序器？

### 段落 432 · Page 57

**EN**

In International Conference on Learning Representations, 2021. Zhen Qin, Rolf Jagerman, Kai Hui, Honglei Zhuang, Junru Wu, Le Yan, Jiaming Shen, Tianqi Liu, Jialu Liu, Donald Metzler, Xuanhui Wang, and Michael Bendersky. Large language models are effective text rankers with pairwise ranking prompting. In Kevin Duh, Helena Gomez, and Steven Bethard (eds.),Findings of the Association for Computational Linguistics: NAACL 2024, pp. 1504–1518, Mexico City, Mexico, June 2024b. Association for Computational Linguistics. doi: 10.18653/v1/2024.findings-naacl.97. URL https://aclanthology.org/2024.findings-naacl.97/. 57

**中文**

学习表征国际会议，2021。Zhen Qing、Rolf Jagerman、Kai Hui、honglei Zhuang、Junru Wu、Le Yan、Jiaming Shen、Tianqi Liu、Jialu Liu、Donald Metzler、Xuanhui Wang 和 Michael Bendersky。大型语言模型是具有成对排名提示的有效文本排名器。载于 Kevin Duh、Helena Gomez 和 Steven Bethard（编辑），计算语言学协会的调查结果：NAACL 2024，第 1504–1518 页，墨西哥墨西哥城，2024 年 6 月b。计算语言学协会。 doi：10.18653/v1/2024.findings-naacl.97。网址 https://aclanthology.org/2024.findings-naacl.97/。 57

### Page 58

### 段落 433 · Page 58

**EN**

Published in Transactions on Machine Learning Research (02/2026) Zhen Qin, Songlin Yang, and Yiran Zhong. Hierarchically gated recurrent neural network for sequence modeling.Advances in Neural Information Processing Systems, 36, 2024c. Yingqi Qu, Yuchen Ding, Jing Liu, Kai Liu, Ruiyang Ren, Xin Zhao, Daxiang Dong, Hua Wu, and Haifeng Wang. RocketQA: An optimized training approach to dense passage retrieval for open-domain question answering. InNorth American Chapter of the Association for Computational Linguistics, 2020. Qwen Team. QwQ-32B: Embracing the power of reinforcement learning.https://qwenlm.github.io/ blog/qwq-32b/, March 2025.

**中文**

发表于《机器学习研究汇刊》(02/2026) 秦臻、杨松林和钟怡然。用于序列建模的分层门控循环神经网络。神经信息处理系统进展，36，2024c。曲英奇、丁雨辰、刘静、刘凯、任瑞阳、赵新、董大向、吴华和王海峰。 RocketQA：一种针对开放域问答的密集段落检索的优化训练方法。计算语言学协会北美分会，2020 年。Qwen 团队。 QwQ-32B：拥抱强化学习的力量。https://qwenlm.github.io/blog/qwq-32b/，2025 年 3 月。

### 段落 434 · Page 58

**EN**

Tadeusz Radecki. Fuzzy set theoretical approach to document retrieval.Information Processing & Management, 15(5):247–259, 1979. Alec Radford, Jeffrey Wu, Rewon Child, David Luan, Dario Amodei, and Ilya Sutskever. Language models are unsupervised multitask learners.https://cdn.openai.com/better-language-models/ language-models.pdf, 2019. Alec Radford, Jong Wook Kim, Chris Hallacy, Aditya Ramesh, Gabriel Goh, Sandhini Agarwal, Girish Sastry, Amanda Askell, Pamela Mishkin, Jack Clark, Gretchen Krueger, and Ilya Sutskever. Learning transferable visual models from natural language supervision. InInternational Conference on Machine Learning, 2021.

**中文**

塔德乌什·拉德茨基文档检索的模糊集理论方法。信息处理与管理，15(5):247–259, 1979。Alec Radford、Jeffrey Wu、Rewon Child、David Luan、Dario Amodei 和 Ilya Sutskever。语言模型是无监督的多任务学习者。https://cdn.openai.com/better-language-models/ language-models.pdf，2019。Alec Radford、Jong Wook Kim、Chris Hallacy、Aditya Ramesh、Gabriel Goh、Sandhini Agarwal、Girish Sastry、Amanda Askell、Pamela Mishkin、Jack Clark、Gretchen Krueger 和 Ilya Sutskever。从自然语言监督中学习可迁移的视觉模型。在国际机器学习会议，2021。

### 段落 435 · Page 58

**EN**

Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, and Peter J. Liu. Exploring the limits of transfer learning with a unified text-to-text transformer. Journal of Machine Learning Research, 21(140):1–67, 2020. URLhttp://jmlr.org/papers/v21/20-074. html. Razieh Rahimi, Youngwoo Kim, Hamed Zamani, and James Allan. Explaining documents’ relevance to search queries.arXiv preprint arXiv:2111.01314, 2021. Shashank Rajput, Nikhil Mehta, Anima Singh, Raghunandan H. Keshavan, Trung Hieu Vu, Lukasz Heldt, Lichan Hong, Yi Tay, Vinh Q. Tran, Jonah Samost, Maciej Kula, Ed H.

**中文**

Colin Raffel、Noam Shazeer、Adam Roberts、Katherine Lee、Sharan Narang、Michael Matena、Yanqi Zhou、Wei Li 和 Peter J. Liu。使用统一的文本到文本转换器探索迁移学习的局限性。机器学习研究杂志，21(140):1–67, 2020。URLhttp://jmlr.org/papers/v21/20-074。 html。拉齐耶·拉希米、Youngwoo Kim、哈米德·扎马尼和詹姆斯·艾伦。解释文档与搜索查询的相关性。arXiv 预印本 arXiv:2111.01314, 2021。Shashank Rajput, Nikhil Mehta, Anima Singh, Raghunandan H. Keshavan, Trung Hieu Vu, Lukasz Heldt, Lichan Hong, Yi Tay, Vinh Q. Tran, Jonah Samost, Maciej Kula, Ed H.

### 段落 436 · Page 58

**EN**

Chi, and Maheswaran Sathiamoorthy. Recommender systems with generative retrieval.arXiv preprint arXiv:2305.05065, 2023. Ori Ram, Liat Bezalel, Adi Zicher, Yonatan Belinkov, Jonathan Berant, and Amir Globerson. What are you token about? Dense retrieval as distributions over the vocabulary. In Anna Rogers, Jordan Boyd-Graber, and Naoaki Okazaki (eds.),Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp. 2481–2498, Toronto, Canada, July 2023a. Association for Computational Linguistics. doi: 10.18653/v1/2023.acl-long.140. URLhttps: //aclanthology.org/2023.acl-long.140/.

**中文**

Chi 和 Maheswaran Sathiamoorthy。具有生成检索功能的推荐系统。arXiv 预印本 arXiv:2305.05065, 2023。Ori Ram、Liat Bezalel、Adi Zicher、Yonatan Belinkov、Jonathan Berant 和 Amir Globerson。你的令牌是什么？密集检索作为词汇表的分布。载于 Anna Rogers、Jordan Boyd-Graber 和 Naoaki Okazaki（编），计算语言学协会第 61 届年会论文集（第 1 卷：长论文），第 2481-2498 页，加拿大多伦多，2023 年 7 月a。计算语言学协会。 doi：10.18653/v1/2023.acl-long.140。网址https://aclanthology.org/2023.acl-long.140/。

### 段落 437 · Page 58

**EN**

Ori Ram, Yoav Levine, Itay Dalmedigos, Dor Muhlgay, Amnon Shashua, Kevin Leyton-Brown, and Yoav Shoham. In-context retrieval-augmented language models.Transactions of the Association for Computational Linguistics, 11:1316–1331, 2023b. Viresh Ranjan, Nikhil Rasiwasia, and C. V. Jawahar. Multi-label cross-modal retrieval. InProceedings of the IEEE International Conference on Computer Vision, pp. 4094–4102, 2015. Nikhil Rasiwasia, Jose Costa Pereira, Emanuele Coviello, Gabriel Doyle, Gert R. G. Lanckriet, Roger Levy, and Nuno Vasconcelos. A new approach to cross-modal multimedia retrieval.

**中文**

Ori Ram、Yoav Levine、Itay Dalmedigos、Dor Muhlgay、Amnon Shashua、Kevin Leyton-Brown 和 Yoav Shoham。上下文检索增强语言模型。计算语言学协会汇刊，11：1316–1331，2023b。 Viresh Ranjan、Nikhil Rasiwasia 和 C. V. Jawahar。多标签跨模态检索。 IEEE 国际计算机视觉会议论文集，第 4094-4102 页，2015 年。Nikhil Rasiwasia、Jose Costa Pereira、Emanuele Coviello、Gabriel Doyle、Gert R. G. Lanckriet、Roger Levy 和 Nuno Vasconcelos。跨模式多媒体检索的新方法。

### 段落 438 · Page 58

**EN**

InProceedings of the 18th ACM International Conference on Multimedia, pp. 251–260, 2010. Shauli Ravfogel, Valentina Pyatkin, Amir David Nissan Cohen, Avshalom Manevich, and Yoav Goldberg. Description-based text similarity. In1st Conference on Language Modeling, 2024. URLhttps: //openreview.net/forum?id=W8Rv1jVycX. Nils Reimers and Iryna Gurevych. Sentence-BERT: Sentence embeddings using Siamese BERT-networks. In Kentaro Inui, Jing Jiang, Vincent Ng, and Xiaojun Wan (eds.),Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on 58

**中文**

第 18 届 ACM 国际多媒体会议记录，第 251-260 页，2010 年。Shauli Ravfogel、Valentina Pyatkin、Amir David Nissan Cohen、Avshalom Manevich 和 Yoav Goldberg。基于描述的文本相似度。第一届语言建模会议，2024 年。URLhttps://openreview.net/forum?id=W8Rv1jVycX。尼尔斯·雷默斯和伊琳娜·古列维奇。 Sentence-BERT：使用 Siamese BERT 网络的句子嵌入。见Kentaro Inui、Jing Jiang、Vincent Ng和Xiaojun Wan（编辑），2019年自然语言处理经验方法会议和第9届58国际联合会议论文集

### Page 59

### 段落 439 · Page 59

**EN**

Published in Transactions on Machine Learning Research (02/2026) Natural Language Processing (EMNLP-IJCNLP), pp. 3982–3992, Hong Kong, China, November 2019. Association for Computational Linguistics. doi: 10.18653/v1/D19-1410. URLhttps://aclanthology. org/D19-1410/. Ruiyang Ren, Yingqi Qu, Jing Liu, Wayne Xin Zhao, QiaoQiao She, Hua Wu, Haifeng Wang, and Ji- Rong Wen. RocketQAv2: A joint training method for dense passage retrieval and passage re-ranking. In Marie-Francine Moens, Xuanjing Huang, Lucia Specia, and Scott Wen-tau Yih (eds.),Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing, pp.

**中文**

发表于《机器学习研究汇刊》(02/2026) 自然语言处理 (EMNLP-IJCNLP)，第 3982–3992 页，中国香港，2019 年 11 月。计算语言学协会。 doi：10.18653/v1/D19-1410。网址https://aclanthology. org/D19-1410/。任瑞阳、曲英奇、刘静、赵鑫、佘巧巧、吴华、王海峰和温继荣。 RocketQAv2：一种用于密集段落检索和段落重新排序的联合训练方法。收录于 Marie-Francine Moens、Xuanjing Huang、Lucia Specia 和 Scott Wen-tau Yih（编），《2021 年自然语言处理经验方法会议论文集》，第 174 页。

### 段落 440 · Page 59

**EN**

2825–2835, Online and Punta Cana, Dominican Republic, November 2021. Association for Computational Linguistics. doi: 10.18653/v1/2021.emnlp-main.224. URLhttps://aclanthology.org/2021.emnlp-main.224/. ZhaochunRen, XiangnanHe, DaweiYin, andM.deRijke. Informationdiscoveryine-commerce.Foundations and Trends in Information Retrieval, 18:417–690, 2024. Stephen Robertson and Hugo Zaragoza. The probabilistic relevance framework: BM25 and beyond.Foundations and Trends in Information Retrieval, 3(4):333–389, April 2009. doi: 10.1561/1500000019. Stephen E. Robertson and K. Sparck Jones.

**中文**

2825–2835，在线和多米尼加共和国蓬塔卡纳，2021 年 11 月。计算语言学协会。 doi：10.18653/v1/2021.emnlp-main.224。网址https://aclanthology.org/2021.emnlp-main.224/。任兆春，何向南，尹大伟，M.deRijke。信息发现商务。信息检索的基础和趋势，18:417–690, 2024。斯蒂芬·罗伯逊和雨果·萨拉戈萨。概率相关性框架：BM25 及以后。信息检索的基础和趋势，3(4):333–389，2009 年 4 月。doi: 10.1561/1500000019。斯蒂芬·E·罗伯逊和 K·斯帕克·琼斯。

### 段落 441 · Page 59

**EN**

Relevance weighting of search terms.Journal of the American Society for Information science, 27(3):129–146, 1976. Stephen E. Robertson, Steve Walker, Susan Jones, Micheline M. Hancock-Beaulieu, and Mike Gatford. Okapi at TREC-3. InProceedings of the 3rd Text REtrieval Conference (TREC-3), NIST Special Publication, pp. 109–126. National Institute of Standards & Technology, 1995. Anna Rogers, Olga Kovaleva, and Anna Rumshisky. A primer in BERTology: What we know about how BERT works.Transactions of the Association for Computational Linguistics, 8:842–866, 2020. doi: 10. 1162/tacl_a_00349. URLhttps://aclanthology.org/2020.tacl-1.54/.

**中文**

搜索词的相关性加权。美国信息科学学会杂志，27(3):129–146, 1976。Stephen E. Robertson、Steve Walker、Susan Jones、Micheline M. Hancock-Beaulieu 和 Mike Gatford。霍加狓在 TREC-3。第三届文本检索会议 (TREC-3) 论文集，NIST 特别出版物，第 109-126 页。美国国家标准与技术研究所，1995 年。安娜·罗杰斯、奥尔加·科瓦列娃和安娜·拉姆希斯基。 BERT 学入门：我们对 BERT 工作原理的了解。计算语言学协会汇刊，8:842–866, 2020。doi: 10. 1162/tacl_a_00349。网址https://aclanthology.org/2020.tacl-1.54/。

### 段落 442 · Page 59

**EN**

Uma Roy, Noah Constant, Rami Al-Rfou, Aditya Barua, Aaron Phillips, and Yinfei Yang. LAReQA: Language-agnostic answer retrieval from a multilingual pool. In Bonnie Webber, Trevor Cohn, Yulan He, and Yang Liu (eds.),Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 5919–5930, Online, November 2020. Association for Computational Linguistics. doi: 10.18653/v1/2020.emnlp-main.477. URLhttps://aclanthology.org/2020.emnlp-main.477/. Devendra Sachan, Mike Lewis, Mandar Joshi, Armen Aghajanyan, Wen-tau Yih, Joelle Pineau, and Luke Zettlemoyer.

**中文**

Uma Roy、Noah Constant、Rami Al-Rfou、Aditya Barua、Aaron Phillips 和 Yinfei Yang。 LAReQA：从多语言池中检索与语言无关的答案。收录于 Bonnie Webber、Trevor Cohn、Yulan He 和 Yang Liu（编），2020 年自然语言处理经验方法 (EMNLP) 会议论文集，第 5919-5930 页，在线，2020 年 11 月。计算语言学协会。 doi：10.18653/v1/2020.emnlp-main.477。网址https://aclanthology.org/2020.emnlp-main.477/。 Devendra Sachan、Mike Lewis、Mandar Joshi、Armen Aghajanyan、Wen-tau Yih、Joelle Pineau 和 Luke Zettlemoyer。

### 段落 443 · Page 59

**EN**

Improving passage retrieval with zero-shot question generation. In Yoav Goldberg, Zornitsa Kozareva, and Yue Zhang (eds.),Proceedings of the 2022 Conference on Empirical Methods in Natural Language Processing, pp. 3781–3797, Abu Dhabi, United Arab Emirates, December 2022. Association for Computational Linguistics. doi: 10.18653/v1/2022.emnlp-main.249. URLhttps://aclanthology.org/ 2022.emnlp-main.249/. Ruslan Salakhutdinov and Geoffrey Hinton. Semantic hashing.International Journal of Approximate Reasoning, 50(7):969–978, 2009. Gerard Salton. Interactive information retrieval. Technical report, Cornell University, 1969. Gerard Salton.

**中文**

通过零样本问题生成改进段落检索。载于 Yoav Goldberg、Zornitsa Kozareva 和 Yue Zhang（编辑），2022 年自然语言处理经验方法会议论文集，第 3781-3797 页，阿拉伯联合酋长国阿布扎比，2022 年 12 月。计算语言学协会。 doi：10.18653/v1/2022.emnlp-main.249。网址https://aclanthology.org/2022.emnlp-main.249/。鲁斯兰·萨拉胡迪诺夫和杰弗里·辛顿。语义散列。国际近似推理杂志，50(7):969–978, 2009。杰拉德·索尔顿。交互式信息检索。技术报告，康奈尔大学，1969 年。杰拉德·索尔顿。

### 段落 444 · Page 59

**EN**

Automatic processing of foreign language documents.Journal of the American Society for Information Science, 21(3):187–194, 1970. Gerard Salton and Christopher Buckley. Term-weighting approaches in automatic text retrieval.Information processing & management, 24(5):513–523, 1988. Gerard Salton, Anita Wong, and Chung-Shu Yang. A vector space model for automatic indexing.Communications of the ACM, 18(11):613–620, 1975. Gerard Salton, Edward A. Fox, and Harry Wu. Extended Boolean information retrieval.Communications of the ACM, 26(11):1022–1036, 1983. Victor Sanh, Lysandre Debut, Julien Chaumond, and Thomas Wolf.

**中文**

外语文档的自动处理。美国信息科学学会杂志，21(3):187–194, 1970。杰拉德·索尔顿和克里斯托弗·巴克利。自动文本检索中的术语权重方法。信息处理与管理，24(5):513–523, 1988。Gerard Salton、Anita Wong 和 Chung-Shu Yang。自动索引的向量空间模型。Communications of the ACM, 18(11):613–620, 1975。Gerard Salton、Edward A. Fox 和 Harry Wu。扩展布尔信息检索。ACM 通讯，26(11):1022–1036, 1983。Victor Sanh、Lysandre Debut、Julien Chaumond 和 Thomas Wolf。

### 段落 445 · Page 59

**EN**

DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter.arXiv preprint arXiv:1910.01108, 2019. 59

**中文**

DistilBERT，BERT 的精炼版本：更小、更快、更便宜、更轻。arXiv 预印本 arXiv:1910.01108, 2019. 59

### Page 60

### 段落 446 · Page 60

**EN**

Published in Transactions on Machine Learning Research (02/2026) Victor Sanh, Albert Webson, Colin Raffel, Stephen Bach, Lintang Sutawika, Zaid Alyafeai, Antoine Chaffin, Arnaud Stiegler, Arun Raja, Manan Dey, et al. Multitask prompted training enables zero-shot task generalization. InInternational Conference on Learning Representations, 2022. Keshav Santhanam, Omar Khattab, Jon Saad-Falcon, Christopher Potts, and Matei Zaharia. ColBERTv2: Effective and efficient retrieval via lightweight late interaction.

**中文**

发表于《机器学习研究汇刊》(02/2026) Victor Sanh、Albert Webson、Colin Raffel、Stephen Bach、Lintang Sutawika、Zaid Alyafeai、Antoine Chaffin、Arnaud Stiegler、Arun Raja、Manan Dey 等人。多任务提示训练可实现零样本任务泛化。国际学习表征会议，2022 年。Keshav Santhanam、Omar Khattab、Jon Saad-Falcon、Christopher Potts 和 Matei Zaharia。 ColBERTv2：通过轻量级后期交互进行有效且高效的检索。

### 段落 447 · Page 60

**EN**

In Marine Carpuat, Marie-Catherine de Marneffe, and Ivan Vladimir Meza Ruiz (eds.),Proceedings of the 2022 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, pp. 3715–3734, Seattle, United States, July 2022. Association for Computational Linguistics. doi: 10.18653/v1/2022.naacl-main.272. URLhttps://aclanthology.org/2022.naacl-main.272/. Naomi Saphra and Sarah Wiegreffe. Mechanistic?arXiv preprint arXiv:2410.09087, 2024. Timo Schick, Jane Dwivedi-Yu, Roberto Dessì, Roberta Raileanu, Maria Lomeli, Eric Hambro, Luke Zettlemoyer, Nicola Cancedda, and Thomas Scialom.

**中文**

载于 Marine Carpuat、Marie-Catherine de Marneffe 和 Ivan Vladimir Meza Ruiz（编辑），计算语言学协会北美分会 2022 年会议记录：人类语言技术，第 3715-3734 页，美国西雅图，2022 年 7 月。计算语言学协会。 doi：10.18653/v1/2022.naacl-main.272。网址https://aclanthology.org/2022.naacl-main.272/。内奥米·萨芙拉和莎拉·维格莱夫。 Mechanistic?arXiv 预印本 arXiv:2410.09087, 2024。 Timo Schick、Jane Dwivedi-Yu、Roberto Dessì、Roberta Raileanu、Maria Lomeli、Eric Hambro、Luke Zettlemoyer、Nicola Cancedda 和 Thomas Scialom。

### 段落 448 · Page 60

**EN**

Toolformer: Language models can teach themselves to use tools.Advances in Neural Information Processing Systems, 36:68539–68551, 2023. Hinrich Schütze, Christopher D. Manning, and Prabhakar Raghavan.Introduction to information retrieval, volume 39. Cambridge University Press Cambridge, 2008. Aliaksei Severyn and Alessandro Moschitti. Learning to rank short text pairs with convolutional deep neural networks. InProceedings of the 38th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 373–382, 2015.

**中文**

Toolformer：语言模型可以自学使用工具。神经信息处理系统的进展，36:68539–68551, 2023。Hinrich Schütze、Christopher D. Manning 和 Prabhakar Raghavan。信息检索导论，第 39 卷。剑桥大学出版社剑桥，2008 年。Aliaksei Severyn 和 Alessandro Moschitti。学习使用卷积深度神经网络对短文本对进行排名。第 38 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 373-382 页，2015 年。

### 段落 449 · Page 60

**EN**

Rulin Shao, Jacqueline He, Akari Asai, Weijia Shi, Tim Dettmers, Sewon Min, Luke Zettlemoyer, and Pang Wei Koh. Scaling retrieval-based language models with a trillion-token datastore. InThe 38th Annual Conference on Neural Information Processing Systems, 2024. Rulin Shao, Rui Qiao, Varsha Kishore, Niklas Muennighoff, Xi Victoria Lin, Daniela Rus, Bryan Kian Hsiang Low, Sewon Min, Wen tau Yih, Pang Wei Koh, and Luke Zettlemoyer. ReasonIR: Training retrievers for reasoning tasks. In2nd Conference on Language Modeling, 2025. URLhttps://openreview.net/forum? id=kkBCNLMbGj. Abhishek Sharma, Abhishek Kumar, Hal Daume, and David W. Jacobs.

**中文**

Rulin Shao、Jacqueline He、Akari Asai、Weijia Shi、Tim Dettmers、Sewon Min、Luke Zettlemoyer 和 Pang Wei Koh。使用万亿令牌数据存储扩展基于检索的语言模型。在第 38 届神经信息处理系统年会上，2024 年。Rulin Shao、Rui Qiao、Varsha Kishore、Niklas Muennighoff、Xi Victoria Lin、Daniela Rus、Bryan Kian Hsiang Low、Sewon Min、Wen tau Yih、Pang Wei Koh 和 Luke Zettlemoyer。 ReasonIR：训练检索器进行推理任务。 In2nd Conference on Language Modeling，2025。URLhttps://openreview.net/forum? id=kkBCNLMbGj。阿布舍克·夏尔马、阿布舍克·库马尔、哈尔·道梅和大卫·W·雅各布斯。

### 段落 450 · Page 60

**EN**

Generalized multiview analysis: A discriminative latent space. In2012 IEEE Conference on Computer Vision and Pattern Recognition, pp. 2160–2167. IEEE, 2012. Xinjie Shen, Zhichao Geng, and Yang Yang. Exploring l0 sparsification for inference-free sparse retrievers. InProceedings of the 48th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’25, pp. 2572–2576, New York, NY, USA, 2025. Association for Computing Machinery. doi: 10.1145/3726302.3730192. Yelong Shen, Xiaodong He, Jianfeng Gao, Li Deng, and Grégoire Mesnil.

**中文**

广义多视图分析：判别性潜在空间。 2012 年 IEEE 计算机视觉和模式识别会议，第 2160-2167 页。 IEEE，2012。沉新杰、耿志超和杨阳。探索无推理稀疏检索器的 l0 稀疏化。 InProceedings of the 48th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR '25, pp. 2572–2576, New York, NY, USA, 2025. 计算机协会。号码：10.1145/3726302.3730192。沉业龙、何晓东、高剑峰、邓力、格雷瓜尔·梅尼尔。

### 段落 451 · Page 60

**EN**

Learning semantic representations using convolutional neural networks for web search. InProceedings of the 23rd International Conference on World Wide Web, WWW ’14 Companion, pp. 373–374, New York, NY, USA, 2014a. Association for Computing Machinery. doi: 10.1145/2567948.2577348. Yelong Shen, Xiaodong He, Jianfeng Gao, Li Deng, and Grégoire Mesnil. A latent semantic model with convolutional-pooling structure for information retrieval. InProceedings of the 23rd ACM International Conference on Conference on Information and Knowledge Management, CIKM ’14, pp. 101–110, New York, NY, USA, 2014b. Association for Computing Machinery.

**中文**

使用卷积神经网络学习用于网络搜索的语义表示。第 23 届万维网国际会议记录，WWW ’14 Companion，第 373–374 页，美国纽约州纽约，2014a。计算机器协会。号码：10.1145/2567948.2577348。沉业龙、何晓东、高剑峰、邓力、格雷瓜尔·梅尼尔。用于信息检索的具有卷积池结构的潜在语义模型。第 23 届 ACM 国际信息和知识管理会议论文集，CIKM ’14，第 101–110 页，美国纽约州纽约，2014b。计算机器协会。

### 段落 452 · Page 60

**EN**

doi: 10.1145/2661829.2661935. Peng Shi, He Bai, and Jimmy Lin. Cross-lingual training of neural models for document ranking. In Trevor Cohn, Yulan He, and Yang Liu (eds.),Findings of the Association for Computational Linguistics: EMNLP 2020, pp. 2768–2773, Online, November 2020. Association for Computational Linguistics. doi: 10.18653/v1/2020.findings-emnlp.249. URLhttps://aclanthology.org/2020.findings-emnlp.249/. 60

**中文**

号码：10.1145/2661829.2661935。彭石、何白、林志颖。用于文档排名的神经模型的跨语言训练。 Trevor Cohn、Yulan He 和 Yang Liu（编辑），计算语言学协会的调查结果：EMNLP 2020，第 2768–2773 页，在线，2020 年 11 月。计算语言学协会。 doi：10.18653/v1/2020.findings-emnlp.249。网址https://aclanthology.org/2020.findings-emnlp.249/。 60

### Page 61

### 段落 453 · Page 61

**EN**

Published in Transactions on Machine Learning Research (02/2026) Noah Shinn, Federico Cassano, Ashwin Gopinath, Karthik Narasimhan, and Shunyu Yao. Reflexion: Language agents with verbal reinforcement learning.Advances in Neural Information Processing Systems, 36: 8634–8652, 2023. Aditi Singh, Abul Ehtesham, Saket Kumar, and Tala Talaei Khoei. Agentic retrieval-augmented generation: A survey on agentic RAG.arXiv preprint arXiv:2501.09136, 2025a. Amanpreet Singh, Joseph Chee Chang, Dany Haddad, Aakanksha Naik, Jena D. Hwang, Rodney Kinney, Daniel S Weld, Doug Downey, and Sergey Feldman.

**中文**

发表于机器学习研究汇刊 (02/2026) Noah Shinn、Federico Cassano、Ashwin Gopinath、Karthik Narasimhan 和 Shunyu Yao。反射：具有言语强化学习的语言代理。神经信息处理系统进展，36：8634–8652，2023。Aditi Singh、Abul Ehtesham、Saket Kumar 和 Tala Talaei Khoei。 Agentic 检索增强生成：Agentic RAG.arXiv 预印本 arXiv:2501.09136, 2025a 的调查。 Amanpreet Singh、Joseph Chee Chang、Dany Haddad、Aakanksha Naik、Jena D. Hwang、Rodney Kinney、Daniel S Weld、Doug Downey 和 Sergey Feldman。

### 段落 454 · Page 61

**EN**

Ai2 scholar QA: Organized literature synthesis with attribution. In Pushkar Mishra, Smaranda Muresan, and Tao Yu (eds.),Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (Volume 3: System Demonstrations), pp. 513– 523, Vienna, Austria, July 2025b. Association for Computational Linguistics. doi: 10.18653/v1/2025. acl-demo.49. URLhttps://aclanthology.org/2025.acl-demo.49/. Ashudeep Singh and Thorsten Joachims. Fairness of exposure in rankings. InProceedings of the 24th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, pp. 2219–2228, 2018.

**中文**

Ai2学者QA：有组织的文献综合与归属。载于 Pushkar Mishra、Smaranda Muresan 和 Tai Yu（编辑），计算语言学协会第 63 届年会论文集（第 3 卷：系统演示），第 513-523 页，奥地利维也纳，2025 年 7 月b。计算语言学协会。 doi：10.18653/v1/2025。 acl-demo.49。网址https://aclanthology.org/2025.acl-demo.49/。阿舒德普·辛格和托尔斯滕·约阿希姆斯。排名曝光的公平性。第 24 届 ACM SIGKDD 国际知识发现与数据挖掘会议论文集，第 2219-2228 页，2018 年。

### 段落 455 · Page 61

**EN**

Richard Socher, Andrej Karpathy, Quoc Le, Christopher D. Manning, and Andrew Y. Ng. Grounded compositional semantics for finding and describing images with sentences.Transactions of the association for computational linguistics, 2:207–218, 2014. Chan Hee Song, Jiaman Wu, Clayton Washington, Brian M. Sadler, Wei-Lun Chao, and Yu Su. LLMplanner: Few-shot grounded planning for embodied agents with large language models. InProceedings of the IEEE/CVF International Conference on Computer Vision, pp. 2998–3009, 2023. Fei Song and W. Bruce Croft. A general language model for information retrieval.

**中文**

Richard Socher、Andrej Karpathy、Quoc Le、Christopher D. Manning 和 Andrew Y. Ng。用句子查找和描述图像的基础组合语义。计算语言学协会的交易，2:207–218, 2014。Chan Hee Song、Jiaman Wu、Clayton Washington、Brian M. Sadler、Wei-Lun Chao 和 Yu Su。 LLMplanner：针对具有大型语言模型的具体代理的少样本基础规划。 IEEE/CVF 国际计算机视觉会议论文集，第 2998-3009 页，2023 年。Fei Song 和 W. Bruce Croft。用于信息检索的通用语言模型。

### 段落 456 · Page 61

**EN**

InProceedings of the 8th International Conference on Information and Knowledge Management, pp. 316–321, 1999. Meina Song, Qing Liu, and E. Haihong. Deep hierarchical attention networks for text matching in information retrieval.2018 International Conference on Information Systems and Computer Aided Education (ICISCAE), pp. 476–481, 2018. Daniel Sonntag and Hans-Jürgen Profitlich. An architecture of open-source tools to combine textual information extraction, faceted search and information visualisation.Artificial intelligence in Medicine, 93: 13–28, 2018. Heydar Soudani, Evangelos Kanoulas, and Faegheh Hasibi. Fine tuning vs.

**中文**

第八届国际信息与知识管理会议论文集，第 316-321 页，1999 年。Meina Song、Qing Liu 和 E. Haihong。用于信息检索中文本匹配的深度层次注意力网络。2018 年信息系统和计算机辅助教育国际会议 (ICISCAE)，第 476–481 页，2018。Daniel Sonntag 和 Hans-Jürgen Profitlich。一种结合文本信息提取、分面搜索和信息可视化的开源工具架构。医学人工智能，93：13-28，2018。Heydar Soudani、Evangelos Kanoulas 和 Faegheh Hasibi。微调对比

### 段落 457 · Page 61

**EN**

retrieval augmented generation for less popular knowledge. InProceedings of the 2024 Annual International ACM SIGIR Conference on Research and Development in Information Retrieval in the Asia Pacific Region, SIGIR-AP 2024, pp. 12–22, New York, NY, USA, 2024. Association for Computing Machinery. doi: 10.1145/3673791.3698415. Karen Sparck Jones. A statistical interpretation of term specificity and its application in retrieval.Journal of documentation, 28(1):11–21, 1972. Hongjin Su, Howard Yen, Mengzhou Xia, Weijia Shi, Niklas Muennighoff, Han-yu Wang, Haisu Liu, Quan Shi, Zachary S. Siegel, Michael Tang, et al.

**中文**

检索增强了不太流行的知识的生成。 2024 年国际 ACM SIGIR 亚太地区信息检索研究与开发年度会议论文集，SIGIR-AP 2024，第 12-22 页，美国纽约州纽约，2024 年。计算机协会。号码：10.1145/3673791.3698415。凯伦·斯帕克·琼斯。术语特异性的统计解释及其在检索中的应用。文献杂志，28（1）：11-21，1972。 Hongjin Su，Howard Yen，Mengzhou Xia，Weijia Shi，Niklas Muennighoff，Han-yu Wang，Haisu Liu，Quan Shi，Zachary S. Siegel，Michael Tang，等。

### 段落 458 · Page 61

**EN**

BRIGHT: A realistic and challenging benchmark for reasoningintensive retrieval.arXiv preprint arXiv:2407.12883, 2024. Yongye Su, Zeya Zhang, Jane Kou, Cheng Ju, Shubhojeet Sarkar, Yamin Wang, Ji Liu, and Shengbo Guo. Modernizing facebook scoped search: Keyword and embedding hybrid retrieval with LLM evaluation. arXiv preprint arXiv:2509.13603, 2025. Weiwei Sun, Lingyong Yan, Xinyu Ma, Shuaiqiang Wang, Pengjie Ren, Zhumin Chen, Dawei Yin, and Zhaochun Ren. Is ChatGPT good at search? investigating large language models as re-ranking agents. InProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, pp.

**中文**

BRIGHT：推理密集型检索的现实且具有挑战性的基准。arXiv 预印本 arXiv：2407.12883，2024。Yongye Su、Zeya 张、Jane Kou、Cheng Ju、Shubhojeet Sarkar、Yamin Wang、Ji Liu 和 Shenbouo。现代化 Facebook 范围搜索：关键字和嵌入混合检索与法学硕士评估。 arXiv 预印本 arXiv:2509.13603, 2025。Weiwei Sun、Lingyong Yan、Xinyu Ma、Shuaiqiang Wang、Pengjie Ren、Zhumin Chen、Dawei Yin 和 Zachun Ren。 ChatGPT 擅长搜索吗？研究大型语言模型作为重新排序代理。 2023 年自然语言处理经验方法会议论文集，第 123 页。

### 段落 459 · Page 61

**EN**

14918– 14937, 2023. Yu Sun, Shuohuan Wang, Yukun Li, Shikun Feng, Xuyi Chen, Han Zhang, Xin Tian, Danxiang Zhu, Hao Tian, and Hua Wu. ERNIE: Enhanced representation through knowledge integration.arXiv preprint arXiv:1904.09223, 2019. 61

**中文**

14918–14937, 2023。孙宇、王硕环、李玉琨、冯世琨、陈煦一、张涵、田鑫、朱丹香、田浩、吴华。 ERNIE：通过知识整合增强表征。arXiv 预印本 arXiv:1904.09223, 2019. 61

### Page 62

### 段落 460 · Page 62

**EN**

Published in Transactions on Machine Learning Research (02/2026) Kai Sheng Tai, Richard Socher, and Christopher D. Manning. Improved semantic representations from treestructured long short-term memory networks. In Chengqing Zong and Michael Strube (eds.),Proceedings of the 53rd Annual Meeting of the Association for Computational Linguistics and the 7th International Joint Conference on Natural Language Processing (Volume 1: Long Papers), pp. 1556–1566, Beijing, China, July 2015. Association for Computational Linguistics. doi: 10.3115/v1/P15-1150. URLhttps: //aclanthology.org/P15-1150/.

**中文**

发表于《机器学习研究汇刊》(02/2026) Kai Shen Tai、Richard Socher 和 Christopher D. Manning。改进了树结构长短期记忆网络的语义表示。载于 Chengqing Zong 和 Michael Strube（编辑），计算语言学协会第 53 届年会和第七届自然语言处理国际联合会议论文集（第一卷：长论文），第 1556-1566 页，中国北京，2015 年 7 月。计算语言学协会。 doi：10.3115/v1/P15-1150。网址https://aclanthology.org/P15-1150/。

### 段落 461 · Page 62

**EN**

Yubao Tang, Ruqing Zhang, Jiafeng Guo, and Maarten de Rijke. Recent advances in generative information retrieval.Companion Proceedings of the ACM Web Conference 2024, 2023. Yi Tay, Vinh Q. Tran, Mostafa Dehghani, Jianmo Ni, Dara Bahri, Harsh Mehta, Zhen Qin, Kai Hui, Zhe Zhao, Jai Gupta, Tal Schuster, William W. Cohen, and Donald Metzler. Transformer memory as a differentiable search index. In Alice H. Oh, Alekh Agarwal, Danielle Belgrave, and Kyunghyun Cho (eds.), Advances in Neural Information Processing Systems, 2022. URLhttps://openreview.net/forum?id= Vu-B0clPfq. Michael Taylor, John Guiver, Stephen Robertson, and Tom Minka.

**中文**

唐玉宝、张如清、郭嘉峰、Maarten de Rijke。生成信息检索的最新进展。2024 年、2023 年 ACM 网络会议配套论文集。Yi Tay、Vinh Q. Tran、Mostafa Dehghani、Jianmo Ni、Dara Bahri、Harsh Mehta、Zhen Qing、Kai Hui、Zhe Zhu、Jai Gupta、Tal Schuster、William W. Cohen 和 Donald Metzler。Transformer内存作为可微搜索索引。摘自 Alice H. Oh、Alekh Agarwal、Danielle Belgrave 和 Kyunghyun Cho（编辑），《神经信息处理系统进展》，2022 年。URL https://openreview.net/forum?id= Vu-B0clPfq。迈克尔·泰勒、约翰·吉弗、斯蒂芬·罗伯逊和汤姆·明卡。

### 段落 462 · Page 62

**EN**

Softrank: optimizing non-smooth rank metrics. InProceedings of the 2008 International Conference on Web Search and Data Mining, pp. 77–86, 2008. Wilson L. Taylor. “Cloze Procedure”: A new tool for measuring readability.Journalism & Mass Communication Quarterly, 30:415 – 433, 1953. Ian Tenney, Dipanjan Das, and Ellie Pavlick. BERT rediscovers the classical NLP pipeline. In Anna Korhonen, David Traum, and Lluís Màrquez (eds.),Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics, pp. 4593–4601, Florence, Italy, July 2019. Association for Computational Linguistics. doi: 10.18653/v1/P19-1452.

**中文**

Softrank：优化非平滑排名指标。 2008 年网络搜索和数据挖掘国际会议论文集，第 77-86 页，2008 年。Wilson L. Taylor。 “完形填空程序”：衡量可读性的新工具。新闻与大众传播季刊，30:415 – 433，1953。Ian Tenney、Dipanjan Das 和 Ellie Pavlick。 BERT 重新发现了经典的 NLP 流程。载于 Anna Korhonen、David Traum 和 Lluís Màrquez（编），计算语言学协会第 57 届年会论文集，第 4593-4601 页，意大利佛罗伦萨，2019 年 7 月。计算语言学协会。 doi：10.18653/v1/P19-1452。

### 段落 463 · Page 62

**EN**

URLhttps://aclanthology.org/P19-1452/. Nandan Thakur, Nils Reimers, Andreas Rücklé, Abhishek Srivastava, and Iryna Gurevych. BEIR: A heterogeneous benchmark for zero-shot evaluation of information retrieval models. In35th Conference on Neural Information Processing Systems Datasets and Benchmarks Track (Round 2), 2021. Yu Tian, Xiao Yang, Jingyuan Zhang, Yinpeng Dong, and Hang Su. Evil geniuses: Delving into the safety of LLM-based agents.arXiv preprint arXiv:2311.11855, 2023. Hugo Touvron, Louis Martin, Kevin Stone, Peter Albert, Amjad Almahairi, Yasmine Babaei, Nikolay Bashlykov, Soumya Batra, Prajjwal Bhargava, Shruti Bhosale, et al.

**中文**

网址https://aclanthology.org/P19-1452/。南丹·塔库尔、尼尔斯·雷默斯、安德烈亚斯·吕克尔、阿布舍克·斯里瓦斯塔瓦和伊琳娜·古列维奇。 BEIR：信息检索模型零样本评估的异构基准。第 35 届神经信息处理系统数据集和基准测试会议（第 2 轮），2021 年。Yu Tian、Xiao Yang、Jingyuan Zhang、Yinpeng Dong 和 Hang Su。邪恶天才：深入研究 LLM 特工的安全。arXiv 预印本 arXiv:2311.11855, 2023。Hugo Touvron、Louis Martin、Kevin Stone、Peter Albert、Amjad Almahairi、Yasmine Babaei、Nikolay Bashlykov、Soumya Batra、Prajjwal Bhargava、Shruti Bhosale 等。

### 段落 464 · Page 62

**EN**

LLaMA 2: Open foundation and fine-tuned chat models.arXiv preprint arXiv:2307.09288, 2023. Harsh Trivedi, Niranjan Balasubramanian, Tushar Khot, and Ashish Sabharwal. Interleaving retrieval with chain-of-thought reasoning for knowledge-intensive multi-step questions. In Anna Rogers, Jordan Boyd-Graber, and Naoaki Okazaki (eds.),Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp. 10014–10037, Toronto, Canada, July 2023. Association for Computational Linguistics. doi: 10.18653/v1/2023.acl-long.557. URLhttps: //aclanthology.org/2023.acl-long.557/. Howard Turtle and James Flood.

**中文**

LLaMA 2：开放基础和微调聊天模型。arXiv 预印本 arXiv：2307.09288，2023。Harsh Trivedi、Niranjan Balasubramanian、Tushar Khot 和 Ashish Sabharwal。将检索与思想链推理交叉用于知识密集型多步骤问题。载于 Anna Rogers、Jordan Boyd-Graber 和 Naoaki Okazaki（编），计算语言学协会第 61 届年会论文集（第一卷：长论文），第 10014–10037 页，加拿大多伦多，2023 年 7 月。计算语言学协会。 doi：10.18653/v1/2023.acl-long.557。网址https://aclanthology.org/2023.acl-long.557/。霍华德·海龟和詹姆斯·弗拉德。

### 段落 465 · Page 62

**EN**

Query evaluation: strategies and optimizations.Information Processing & Management, 31(6):831–850, 1995. Ahmet Üstün, Arianna Bisazza, Gosse Bouma, and Gertjan van Noord. UDapter: Language adaptation for truly Universal Dependency parsing. In Bonnie Webber, Trevor Cohn, Yulan He, and Yang Liu (eds.), Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 2302–2315, Online, November 2020. Association for Computational Linguistics. doi: 10.18653/v1/2020. emnlp-main.180. URLhttps://aclanthology.org/2020.emnlp-main.180/. C. Van Rijsbergen. Information retrieval: theory and practice.

**中文**

查询评估：策略和优化。信息处理与管理，31(6):831–850, 1995。Ahmet Üstün、Arianna Bisazza、Gosse Bouma 和 Gertjan van Noord。 UDapter：真正通用依赖解析的语言适配。收录于 Bonnie Webber、Trevor Cohn、Yulan He 和 Yang Liu（编辑），2020 年自然语言处理经验方法 (EMNLP) 会议论文集，第 2302-2315 页，在线，2020 年 11 月。计算语言学协会。 doi：10.18653/v1/2020。 emnlp-main.180。网址https://aclanthology.org/2020.emnlp-main.180/。 C.范·里斯贝尔根。信息检索：理论与实践。

### 段落 466 · Page 62

**EN**

InProceedings of the Joint IBM/University of Newcastle Upon Tyne Seminar on Data Base Systems, volume 79, pp. 1–14, 1979. 62

**中文**

IBM/纽卡斯尔大学数据库系统联合研讨会论文集，第 79 卷，第 1-14 页，1979 年。 62

### Page 63

### 段落 467 · Page 63

**EN**

Published in Transactions on Machine Learning Research (02/2026) AshishVaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Ł ukasz Kaiser, and Illia Polosukhin. Attention is all you need. In I. Guyon, U. Von Luxburg, S. Bengio, H. Wallach, R. Fergus, S. Vishwanathan, and R. Garnett (eds.),Advances in Neural Information Processing Systems, volume30.CurranAssociates, Inc., 2017. URLhttps://proceedings.neurips.cc/paper_files/paper/ 2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf. Henrique Schechter Vera, Sahil Dua, Biao Zhang, Daniel Salz, Ryan Mullins, Sindhu Raghuram Panyam, et al.

**中文**

发表于机器学习研究汇刊 (02/2026) AshishVaswani、Noam Shazeer、Niki Parmar、Jakob Uszkoreit、Llion Jones、Aidan N. Gomez、Ł ukasz Kaiser 和 Illia Polosukhin。您所需要的就是关注。载于 I. Guyon、U. Von Luxburg、S. Bengio、H. Wallach、R. Fergus、S. Vishwanathan 和 R. Garnett（编辑），神经信息处理系统进展，第 30 卷。CurranAssociates, Inc.，2017 年。 URL https://proceedings.neurips.cc/paper_files/paper/ 2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf。 Henrique Schechter Vera、Sahil Dua、Biao 张、Daniel Salz、Ryan Mullins、Sindhu Raghuram Panyam 等。

### 段落 468 · Page 63

**EN**

EmbeddingGemma: Powerful and lightweight text representations.arXiv preprint arXiv:2509.20354, 2025. Jean-Philippe Vert, Koji Tsuda, and Bernhard Schölkopf. A primer on kernel methods. InKernel Methods in Computational Biology, pp. 35–70. MIT press, 2004. David Wan, Han Wang, Elias Stengel-Eskin, Jaemin Cho, and Mohit Bansal. CLaMR: Contextualized late-interaction for multimodal content retrieval.arXiv preprint arXiv:2506.06144, 2025. Shengxian Wan, Yanyan Lan, Jiafeng Guo, Jun Xu, Liang Pang, and Xueqi Cheng. A deep architecture for semantic matching with multiple positional sentence representations.

**中文**

EmbeddingGemma：强大且轻量级的文本表示。arXiv 预印本 arXiv：2509.20354，2025。Jean-Philippe Vert、Koji Tsuda 和 Bernhard Schölkopf。内核方法入门。计算生物学中的核方法，第 35-70 页。麻省理工学院出版社，2004 年。David Wan、Han Wang、Elias Stengel-Eskin、Jaemin Cho 和 Mohit Bansal。 CLaMR：多模态内容检索的情境化后期交互。arXiv 预印本 arXiv：2506.06144，2025。Shengxian Wan、Yanyan Lan、JiafengGuo、Jun Xu、Liang Pang 和 Xueqi Cheng。具有多个位置句子表示的语义匹配的深层架构。

### 段落 469 · Page 63

**EN**

InProceedings of the 30th AAAI Conference on Artificial Intelligence, AAAI’16, pp. 2835–2841. AAAI Press, 2016. Ben Wang and Aran Komatsuzaki. GPT-J-6B: A 6 Billion Parameter Autoregressive Language Model. https://github.com/kingoflolz/mesh-transformer-jax, May 2021. Bokun Wang, Yang Yang, Xing Xu, Alan Hanjalic, and Heng Tao Shen. Adversarial cross-modal retrieval. InProceedings of the 25th ACM International Conference on Multimedia, pp. 154–162, 2017. Haixun Wang and Taesik Na. Rethinking e-commerce search.ACM SIGIR Forum, 57:1–19, 2023.

**中文**

第 30 届 AAAI 人工智能会议论文集，AAAI’16，第 2835-2841 页。 AAAI 出版社，2016 年。Ben Wang 和 Aran Komatsuzaki。 GPT-J-6B：60 亿参数的自回归语言模型。 https://github.com/kingoflolz/mesh-transformer-jax，2021 年 5 月。Bokun Wang、Yang Yang、Xing Xu、Alan Hanjalic 和 Heng Tao Shen。对抗性跨模态检索。第 25 届 ACM 国际多媒体会议论文集，第 154-162 页，2017 年。Haixun Wang 和 Taesik Na。重新思考电子商务搜索。ACM SIGIR 论坛，57:1–19, 2023。

### 段落 470 · Page 63

**EN**

Jiongxiao Wang, Qiaojing Yan, Yawei Wang, Yijun Tian, Soumya Smruti Mishra, Zhichao Xu, Megha Gandhi, Panpan Xu, and Lin Lee Cheong. Reinforcement learning for self-improving agent with skill library, 2025a. URLhttps://arxiv.org/abs/2512.17102. Kaiye Wang, Qiyue Yin, Wei Wang, Shu Wu, and Liang Wang. A comprehensive survey on cross-modal retrieval.arXiv preprint arXiv:1607.06215, 2016. Lei Wang, Chen Ma, Xueyang Feng, Zeyu Zhang, Hao Yang, Jingsen Zhang, Zhiyuan Chen, Jiakai Tang, Xu Chen, Yankai Lin, et al. A survey on large language model based autonomous agents.Frontiers of Computer Science, 18(6):186345, 2024a.

**中文**

Jiongxiao Wang、Qiaojing Yan、Yawei Wang、Yijun Tian、Soumya Smruti Mishra、Zhichao Xu、Megha Gandhi、Panpan Xu 和 Lin Lee Cheong。具有技能库的自我改进代理的强化学习，2025a。网址https://arxiv.org/abs/2512.17102。王凯业、殷启月、王伟、吴树、王亮。跨模态检索综合综述.arXiv 预印本 arXiv:1607.06215, 2016。 王雷，马晨，冯雪阳，张泽宇，杨浩，张景森，陈志远，唐家凯，陈旭，林彦凯，等。基于大语言模型的自主代理调查。计算机科学前沿，18(6):186345, 2024a。

### 段落 471 · Page 63

**EN**

Liang Wang, Nan Yang, Xiaolong Huang, Binxing Jiao, Linjun Yang, Daxin Jiang, Rangan Majumder, and Furu Wei. Text embeddings by weakly-supervised contrastive pre-training.arXiv preprint arXiv:2212.03533, 2022a. Liang Wang, Nan Yang, Xiaolong Huang, Linjun Yang, Rangan Majumder, and Furu Wei. Improving text embeddings with large language models.arXiv preprint arXiv:2401.00368, 2023a. Tianshi Wang, Fengling Li, Lei Zhu, Jingjing Li, Zheng Zhang, and Heng Tao Shen. Cross-modal retrieval: A systematic review of methods and future directions.arXiv preprint arXiv:2308.14263, 2024b.

**中文**

王亮、杨南、黄小龙、焦滨兴、杨林军、姜大新、Rangan Majumder 和 Furu Wei。通过弱监督对比预训练进行文本嵌入。arXiv 预印本 arXiv:2212.03533, 2022a。王亮、杨南、黄小龙、杨林军、Rangan Majumder 和 Furu Wei。使用大型语言模型改进文本嵌入。arXiv 预印本 arXiv:2401.00368, 2023a。王天石、李风玲、朱雷、李晶晶、张正、沉恒涛。跨模态检索：方法和未来方向的系统回顾。arXiv 预印本 arXiv:2308.14263, 2024b。

### 段落 472 · Page 63

**EN**

Xuanhui Wang, Nadav Golbandi, Michael Bendersky, Donald Metzler, and Marc Najork. Position bias estimation for unbiased learning to rank in personal search. InProceedings of the 11th ACM International Conference on Web Search and Data Mining, pp. 610–618, 2018. Xuewei Wang, Qiang Jin, Shengyu Huang, Min Zhang, Xi Liu, Zhengli Zhao, Yukun Chen, Zhengyu Zhang, Jiyan Yang, Ellie Wen, Sagar Chordia, Wenlin Chen, and Qin Huang. Towards the better ranking consistency: A multi-task learning framework for early stage ads ranking.arXiv preprint arXiv:2307.11096, 2023b. 63

**中文**

王选辉、纳达夫·戈尔班迪、迈克尔·本德斯基、唐纳德·梅茨勒和马克·纳约克。位置偏差估计，用于无偏差学习在个人搜索中排名。第 11 届 ACM 国际网络搜索和数据挖掘会议论文集，第 610-618 页，2018 年。Xuewei Wang、Qiang Jin、Shengyu Huang、Min Zhang、Xi Liu、Zhengli Zhao、Yukun Chen、Zhengyu Zhu、Jiyan Yang、Ellie Wen、Sagar Chordia、Wenlin Chen 和 Qin Huang。迈向更好的排名一致性：早期广告排名的多任务学习框架。arXiv 预印本 arXiv:2307.11096, 2023b。 63

### Page 64

### 段落 473 · Page 64

**EN**

Published in Transactions on Machine Learning Research (02/2026) Yumeng Wang, Lijun Lyu, and Avishek Anand. BERT rankers are brittle: A study using adversarial document perturbations. InProceedings of the 2022 ACM SIGIR International Conference on Theory of Information Retrieval, ICTIR ’22, pp. 115–120, New York, NY, USA, 2022b. Association for Computing Machinery. doi: 10.1145/3539813.3545122. Zhenduo Wang, Zhichao Xu, Vivek Srikumar, and Qingyao Ai. An in-depth investigation of user response simulation for conversational search. InProceedings of the ACM on Web Conference 2024, pp. 1407–1418, 2024c.

**中文**

发表于机器学习研究汇刊 (02/2026) Yumeng Wang、Lijun Lyu 和 Avishek Anand。 BERT 排名器很脆弱：一项使用对抗性文档扰动的研究。 2022 年 ACM SIGIR 信息检索理论国际会议论文集，ICTIR ’22，第 115–120 页，美国纽约州纽约，2022b。计算机器协会。号码：10.1145/3539813.3545122。王振铎、徐志超、Vivek Srikumar 和艾庆耀。对话式搜索的用户响应模拟的深入研究。 InProceedings of ACM on Web Conference 2024，第 1407-1418 页，2024c。

### 段落 474 · Page 64

**EN**

Zora Zhiruo Wang, Akari Asai, Xinyan Velocity Yu, Frank F. Xu, Yiqing Xie, Graham Neubig, and Daniel Fried. CodeRAG-bench: Can retrieval augment code generation? In Luis Chiruzzo, Alan Ritter, and Lu Wang (eds.),Findings of the Association for Computational Linguistics: NAACL 2025, pp. 3199–3214, Albuquerque, New Mexico, April 2025b. Association for Computational Linguistics. doi: 10.18653/v1/ 2025.findings-naacl.176. URLhttps://aclanthology.org/2025.findings-naacl.176/.

**中文**

Zorazhiruo Wang、Akari Asai、Xinyan Velocity Yu、Frank F. Xu、Yiqing Xie、Graham Neubig 和 Daniel Fried。 CodeRAG-bench：检索可以增强代码生成吗？载于 Luis Chiruzzo、Alan Ritter 和 Lu Wang（编辑），计算语言学协会的调查结果：NAACL 2025，第 3199-3214 页，新墨西哥州阿尔伯克基，2025 年 4 月b。计算语言学协会。 doi：10.18653/v1/2025.findings-naacl.176。网址https://aclanthology.org/2025.findings-naacl.176/。

### 段落 475 · Page 64

**EN**

Benjamin Warner, Antoine Chaffin, Benjamin Clavié, Orion Weller, Oskar Hallström, Said Taghadouini, Alexis Gallagher, Raja Biswas, Faisal Ladhak, Tom Aarsen, Griffin Thomas Adams, Jeremy Howard, and Iacopo Poli. Smarter, better, faster, longer: A modern bidirectional encoder for fast, memory efficient, and long context finetuning and inference. In Wanxiang Che, Joyce Nabende, Ekaterina Shutova, and Mohammad Taher Pilehvar (eds.),Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp. 2526–2547, Vienna, Austria, July 2025. Association for Computational Linguistics.

**中文**

本杰明·沃纳、安托万·查芬、本杰明·克拉维、奥利安·韦勒、奥斯卡·霍尔斯特罗姆、赛义德·塔哈杜伊尼、亚历克西斯·加拉格尔、拉贾·比斯瓦斯、费萨尔·拉达克、汤姆·阿尔森、格里芬·托马斯·亚当斯、杰里米·霍华德和亚科波·波利。更智能、更好、更快、更长：现代双向编码器，可实现快速、内存高效、长上下文微调和推理。载于 Wanyang Che、Joyce Nabende、Ekaterina Shutova 和 Mohammad Taher Pilehvar（编），计算语言学协会第 63 届年会论文集（第一卷：长论文），第 2526-2547 页，奥地利维也纳，2025 年 7 月。计算语言学协会。

### 段落 476 · Page 64

**EN**

doi: 10.18653/v1/2025.acl-long.127. URL https://aclanthology.org/2025.acl-long.127/. Cong Wei, Yang Chen, Haonan Chen, Hexiang Hu, Ge Zhang, Jie Fu, Alan Ritter, and Wenhu Chen. UniIR: Training and benchmarking universal multimodal information retrievers. InComputer Vision – ECCV 2024, volume 15145 ofLecture Notes in Computer Science, pp. 387–404. Springer, Cham, 2025. doi: 10.1007/978-3-031-73021-4_23. JasonWei, XuezhiWang, DaleSchuurmans, MaartenBosma, FeiXia, EdChi, QuocV.Le, DennyZhou, etal. Chain-of-thought prompting elicits reasoning in large language models.Advances in neural information processing systems, 35:24824–24837, 2022.

**中文**

doi：10.18653/v1/2025.acl-long.127。网址 https://aclanthology.org/2025.acl-long.127/。丛伟、陈杨、陈浩南、胡鹤翔、张戈、付杰、艾伦·里特和陈文虎。 UniIR：通用多模式信息检索器的培训和基准测试。计算机视觉 – ECCV 2024，计算机科学讲义第 15145 卷，第 387-404 页。施普林格，Cham，2025。doi：10.1007/978-3-031-73021-4_23。 JasonWei，王学智，DaleSchuurmans，MaartenBosma，FeiXia，EdChi，QuocV.Le，DennyZhou，等。思想链提示引发大型语言模型中的推理。神经信息处理系统的进展，35：24824–24837，2022。

### 段落 477 · Page 64

**EN**

Orion Weller, Benjamin Van Durme, Dawn Lawrie, Ashwin Paranjape, Yuhao Zhang, and Jack Hessel. Promptriever: Instruction-trained retrievers can be prompted like language models.arXiv preprint arXiv:2409.11136, 2024. Orion Weller, Benjamin Chang, Sean MacAvaney, Kyle Lo, Arman Cohan, Benjamin Van Durme, Dawn Lawrie, and Luca Soldaini. FollowIR: Evaluating and teaching information retrieval models to follow instructions.

**中文**

Orion Weller、Benjamin Van Durme、Dawn Lawrie、Ashwin Paranjape、张宇豪和 Jack Hessel。 Promptriever：经过指令训练的检索器可以像语言模型一样进行提示。arXiv 预印本 arXiv:2409.11136, 2024。Orion Weller、Benjamin Chang、Sean MacAvaney、Kyle Lo、Arman Cohan、Benjamin Van Durme、Dawn Lawrie 和 Luca Soldaini。 FollowIR：评估和教授信息检索模型以遵循指令。

### 段落 478 · Page 64

**EN**

In Luis Chiruzzo, Alan Ritter, and Lu Wang (eds.),Proceedings of the 2025 Conference of the Nations of the Americas Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers), pp. 11926–11942, Albuquerque, New Mexico, April 2025a. Association for Computational Linguistics. doi: 10.18653/v1/2025.naacl-long.597. URL https://aclanthology.org/2025.naacl-long.597/. Orion Weller, Kathryn Ricci, Eugene Yang, Andrew Yates, Dawn Lawrie, and Benjamin Van Durme. Rank1: Test-time compute for reranking in information retrieval. In2nd Conference on Language Modeling, 2025b.

**中文**

载于 Luis Chiruzzo、Alan Ritter 和 Lu Wang（编），计算语言学协会美洲国家分会 2025 年会议记录：人类语言技术（第一卷：长论文），第 11926-11942 页，新墨西哥州阿尔伯克基，2025 年 4 月a。计算语言学协会。 doi：10.18653/v1/2025.naacl-long.597。网址 https://aclanthology.org/2025.naacl-long.597/。 Orion Weller、Kathryn Ricci、Eugene Yang、Andrew Yates、Dawn Lawrie 和 Benjamin Van Durme。 Rank1：信息检索中重排的测试时计算。第二届语言建模会议，2025b。

### 段落 479 · Page 64

**EN**

URLhttps://openreview.net/forum?id=Pg0PAvbhGv. Ryen W. White and Resa A. Roth.Exploratory search: Beyond the query-response paradigm. Morgan & Claypool Publishers, 2009. John Wieting, Mohit Bansal, Kevin Gimpel, and Karen Livescu. Towards universal paraphrastic sentence embeddings.arXiv preprint arXiv:1511.08198, 2016. Thomas D. Wilson. Human information behavior.Informing science, 3:49, 2000. S. K. Michael Wong and Y. Y. Yao. A probability distribution model for information retrieval.Information Processing & Management, 25(1):39–53, 1989. 64

**中文**

网址https://openreview.net/forum?id=Pg0PAvbhGv。 Ryen W. White 和 Resa A. Roth。探索性搜索：超越查询-响应范式。 Morgan & Claypool 出版社，2009 年。John Wieting、Mohit Bansal、Kevin Gimpel 和 Karen Livescu。迈向通用释义句子嵌入。arXiv 预印本 arXiv:1511.08198, 2016。Thomas D. Wilson。人类信息行为。信息科学，3:49，2000。S.K. Michael Wong 和 Y. Y. Yao。信息检索的概率分布模型。信息处理与管理，25(1):39–53, 1989。 64

### Page 65

### 段落 480 · Page 65

**EN**

Published in Transactions on Machine Learning Research (02/2026) Marco Wrzalik and Dirk Krechel. CoRT: Complementary rankings from transformers. InProceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, pp. 4194–4204, 2021. Jialong Wu, Baixuan Li, Runnan Fang, Wenbiao Yin, Liwen Zhang, Zhengwei Tao, Dingchu Zhang, Zekun Xi, YongJiang, PengjunXie, FeiHuang, andJingrenZhou. WebDancer: Towardsautonomousinformation seeking agency.arXiv preprint arXiv:2505.22648, 2025a.

**中文**

发表于《机器学习研究汇刊》(02/2026) Marco Wrzalik 和 Dirk Krechel。 CoRT：变形金刚的补充排名。计算语言学协会北美分会 2021 年会议记录：人类语言技术，第 4194–4204 页，2021 年。吴嘉龙、李百轩、方润南、尹文彪、张立文、陶正伟、张鼎初、奚泽坤、江勇、谢鹏军、黄飞和周景仁。 WebDancer：迈向自主信息寻求机构.arXiv 预印本 arXiv:2505.22648, 2025a。

### 段落 481 · Page 65

**EN**

Jialong Wu, Wenbiao Yin, Yong Jiang, Zhenglin Wang, Zekun Xi, Runnan Fang, Linhai Zhang, Yulan He, Deyu Zhou, Pengjun Xie, and Fei Huang. WebWalker: Benchmarking LLMs in web traversal. In Wanxiang Che, Joyce Nabende, Ekaterina Shutova, and Mohammad Taher Pilehvar (eds.),Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp. 10290–10305, Vienna, Austria, July 2025b. Association for Computational Linguistics. URLhttps: //aclanthology.org/2025.acl-long.508/. Qiang Wu, Christopher J.C. Burges, Krysta M. Svore, and Jianfeng Gao.

**中文**

吴家龙、尹文标、蒋勇、王正林、奚泽坤、方润南、张林海、何玉兰、周德宇、谢鹏军和黄飞。 WebWalker：网络遍历方面的法学硕士基准测试。载于 Wanyang Che、Joyce Nabende、Ekaterina Shutova 和 Mohammad Taher Pilehvar（编辑），计算语言学协会第 63 届年会论文集（第一卷：长论文），第 10290–10305 页，奥地利维也纳，2025 年 7 月b。计算语言学协会。网址https://aclanthology.org/2025.acl-long.508/。吴强、Christopher J.C. Burges、Krysta M. Svore 和高剑峰。

### 段落 482 · Page 65

**EN**

Adapting boosting for information retrieval measures.Information Retrieval, 13:254–270, 2010. Qingyun Wu, Gagan Bansal, Jieyu Zhang, Yiran Wu, Shaokun Zhang, Erkang Zhu, Beibin Li, Li Jiang, Xiaoyun Zhang, and Chi Wang. AutoGen: Enabling next-gen LLM applications via multi-agent conversation. arXiv preprint arXiv:2308.08155, 2023a. Xing Wu, Guangyuan Ma, Meng Lin, Zijia Lin, Zhongyuan Wang, and Songlin Hu. Contextual masked auto-encoder for dense passage retrieval.Proceedings of the AAAI Conference on Artificial Intelligence, 37(4):4738–4746, 2023b.

**中文**

适应信息检索措施的提升。信息检索，13:254–270, 2010。Qingyun Wu、Gagan Bansal、Jieyu Zhu、Yiran Wu、Shakun Zhang、Erkang Zhu、Beibin Li、Li Jiang、Xiaoyun Zhu 和 Chi Wang。 AutoGen：通过多代理对话启用下一代 LLM 应用程序。 arXiv 预印本 arXiv:2308.08155, 2023a。吴兴，马光远，林猛，林子佳，王中远，胡松林。用于密集段落检索的上下文屏蔽自动编码器。AAAI 人工智能会议论文集，37(4):4738–4746, 2023b。

### 段落 483 · Page 65

**EN**

Yunjia Xi, Jianghao Lin, Yongzhao Xiao, Zheli Zhou, Rong Shan, Te Gao, Jiachen Zhu, Weiwen Liu, Yong Yu, and Weinan Zhang. A survey of LLM-based deep search agents: Paradigm, optimization, evaluation, and challenges.arXiv preprint arXiv:2508.05668, 2025. Fen Xia, Tie-Yan Liu, Jue Wang, Wensheng Zhang, and Hang Li. Listwise approach to learning to rank: theory and algorithm. InProceedings of the 25th International Conference on Machine Learning, pp. 1192–1199, 2008. Chong Xiang, Tong Wu, Zexuan Zhong, David Wagner, Danqi Chen, and Prateek Mittal. Certifiably robust RAG against retrieval corruption.arXiv preprint arXiv:2405.15556, 2024a.

**中文**

奚云嘉、林江浩、肖永照、周哲丽、山蓉、高特、朱嘉辰、刘伟文、余勇和张伟南。基于 LLM 的深度搜索代理的调查：范式、优化、评估和挑战。arXiv 预印本 arXiv:2508.05668, 2025。Fen Xia、Tie-Yan Liu、Jue Wang、Wensheng Zhang 和 Hang Li。学习排序的列表方法：理论和算法。第 25 届国际机器学习会议论文集，第 1192-1199 页，2008 年。Chong Xian、Tong Wu、Zexuanzhong、David Wagner、Danqi Chen 和 Prateek Mittal。可证明稳健的 RAG，可防止检索损坏。arXiv 预印本 arXiv:2405.15556, 2024a。

### 段落 484 · Page 65

**EN**

Zhen Xiang, Linzhi Zheng, Yanjie Li, Junyuan Hong, Qinbin Li, Han Xie, Jiawei Zhang, Zidi Xiong, Chulin Xie, Carl Yang, et al. GuardAgent: Safeguard LLM agents by a guard agent via knowledge-enabled reasoning.arXiv preprint arXiv:2406.09187, 2024b. Shitao Xiao, Zheng Liu, Yingxia Shao, and Zhao Cao. RetroMAE: Pre-training retrieval-oriented language models via masked auto-encoder. In Yoav Goldberg, Zornitsa Kozareva, and Yue Zhang (eds.),Proceedings of the 2022 Conference on Empirical Methods in Natural Language Processing, pp. 538–548, Abu Dhabi, United Arab Emirates, December 2022. Association for Computational Linguistics.

**中文**

翔、郑林志、李艳杰、洪俊元、李勤斌、谢涵、张嘉伟、熊子迪、谢楚林、杨卡尔等。 GuardAgent：由警卫代理通过知识推理来保护 LLM 代理。arXiv 预印本 arXiv:2406.09187, 2024b。肖世涛，刘峥，邵迎霞，赵操。 RetroMAE：通过屏蔽自动编码器预训练面向检索的语言模型。载于 Yoav Goldberg、Zornitsa Kozareva 和 Yue Zhang（编），2022 年自然语言处理经验方法会议论文集，第 538-548 页，阿拉伯联合酋长国阿布扎比，2022 年 12 月。计算语言学协会。

### 段落 485 · Page 65

**EN**

doi: 10.18653/v1/ 2022.emnlp-main.35. URLhttps://aclanthology.org/2022.emnlp-main.35/. Jinheng Xie, Weijia Mao, Zechen Bai, David Junhao Zhang, Weihao Wang, Kevin Qinghong Lin, Yuchao Gu, Zhijie Chen, Zhenheng Yang, and Mike Zheng Shou. Show-o: One single transformer to unify multimodal understanding and generation.arXiv preprint arXiv:2408.12528, 2024a. Quanting Xie, So Yeon Min, Tianyi Zhang, Kedi Xu, Aarav Bajaj, Russ Salakhutdinov, Matthew Johnson- Roberson, and Yonatan Bisk. Embodied-RAG: General non-parametric embodied memory for retrieval and generation. InLanguage Gamification - NeurIPS 2024 Workshop, 2024b. URLhttps://openreview.

**中文**

doi：10.18653/v1/2022.emnlp-main.35。网址https://aclanthology.org/2022.emnlp-main.35/。谢金恒、毛伟佳、白泽辰、张俊豪、王伟豪、林庆红、顾玉超、陈志杰、杨振恒和寿正。 Show-o：统一多模态理解和生成的单一转换器。arXiv 预印本 arXiv:2408.12528, 2024a。 Quanting Xie、So Yeon Min、Tianyi 张、Kedi Xu、Aarav Bajaj、Russ Salakhutdinov、Matthew Johnson-Roberson 和 Yonatan Bisk。 Embodied-RAG：用于检索和生成的通用非参数体现内存。 InLanguage 游戏化 - NeurIPS 2024 研讨会，2024b。网址https://openreview.

### 段落 486 · Page 65

**EN**

net/forum?id=U8p8zpK3jL. Chenyan Xiong, Zhuyun Dai, Jamie Callan, Zhiyuan Liu, and Russell Power. End-to-end neural ad-hoc ranking with kernel pooling. InProceedings of the 40th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’17, pp. 55–64, New York, NY, USA, 2017. Association for Computing Machinery. doi: 10.1145/3077136.3080809. 65

**中文**

网/论坛？id=U8p8zpK3jL。熊陈彦、戴朱云、杰米·卡兰、刘志远和拉塞尔·鲍尔。使用内核池进行端到端神经临时排名。 InProceedings of the 40th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’17, pp. 55–64, New York, NY, USA, 2017. 计算机协会。号码：10.1145/3077136.3080809。 65

### Page 66

### 段落 487 · Page 66

**EN**

Published in Transactions on Machine Learning Research (02/2026) Lee Xiong, Chenyan Xiong, Ye Li, Kwok-Fung Tang, Jialin Liu, Paul N. Bennett, Junaid Ahmed, and Arnold Overwijk. Approximate nearest neighbor negative contrastive learning for dense text retrieval. arXiv preprint arXiv:2007.00808, 2020. Jun Xu, Xiangnan He, and Hang Li. Deep learning for matching in search and recommendation. InThe 41st International ACM SIGIR Conference on Research & Development in Information Retrieval, pp. 1365–1368, 2018.

**中文**

发表于《机器学习研究汇刊》(02/2026) Lee Xiong、Chenyan Xiong、Ye Li、Kwok-Fung Tang、Jialin Liu、Paul N. Bennett、Junaid Ahmed 和 Arnold Overwijk。用于密集文本检索的近似最近邻负对比学习。 arXiv 预印本 arXiv:2007.00808, 2020。Jun Xu、Xiangnan He 和 Hang Li。用于搜索和推荐匹配的深度学习。载于第 41 届国际 ACM SIGIR 信息检索研究与开发会议，第 1365–1368 页，2018 年。

### 段落 488 · Page 66

**EN**

Mengyao Xu, Wenfei Zhou, Yauhen Babakhin, Gabriel De Souza Pereira Moreira, Ronay Ak, Radek Osmulski, Bo Liu, Even Oldridge, and Benedikt Schifferer. Omni-Embed-Nemotron: A unified multimodal retrieval model for text, image, audio, and video.arXiv preprint arXiv:2510.03458, 2025a. Shicheng Xu, Danyang Hou, Liang Pang, Jingcheng Deng, Jun Xu, Huawei Shen, and Xueqi Cheng. Invisible relevance bias: Text-image retrieval models prefer AI-generated images. InProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’24, pp. 208–217, New York, NY, USA, 2024a.

**中文**

徐梦瑶、周文飞、Yauhen Babakhin、Gabriel De Souza Pereira Moreira、Ronay Ak、Radek Osmulski、Bo Liu、Even Oldridge 和 Benedikt Schifferer。 Omni-Embed-Nemotron：文本、图像、音频和视频的统一多模态检索模型。arXiv 预印本 arXiv:2510.03458, 2025a。徐世成、侯丹阳、庞亮、邓景成、徐军、沉华为和程学奇。看不见的相关性偏差：文本图像检索模型更喜欢人工智能生成的图像。第 47 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR ’24，第 208–217 页，美国纽约州纽约，2024a。

### 段落 489 · Page 66

**EN**

Association for Computing Machinery. doi: 10.1145/3626772.3657750. Zhichao Xu. Context-aware decoding reduces hallucination in query-focused summarization, 2023. URL https://arxiv.org/abs/2312.14335. Zhichao Xu. RankMamba: Benchmarking Mamba’s document ranking performance in the era of transformers.arXiv preprint arXiv:2403.18276, 2024. Zhichao Xu and Daniel Cohen. A lightweight constrained generation alternative for query-focused summarization. InProceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’23, pp. 1745–1749, New York, NY, USA, 2023.

**中文**

计算机器协会。号码：10.1145/3626772.3657750。徐志超.上下文感知解码减少了以查询为中心的摘要中的幻觉，2023 年。URL https://arxiv.org/abs/2312.14335。徐志超. RankMamba：对 Transformers 时代的 Mamba 文档排名性能进行基准测试。arXiv 预印本 arXiv:2403.18276, 2024。Zhichao Xu 和 Daniel Cohen。用于以查询为中心的摘要的轻量级约束生成替代方案。第 46 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR ’23，第 1745–1749 页，美国纽约州纽约，2023 年。

### 段落 490 · Page 66

**EN**

Association for Computing Machinery. ISBN 9781450394086. doi: 10.1145/3539618.3591936. URLhttps: //doi.org/10.1145/3539618.3591936. Zhichao Xu and Jiepu Jiang. Multi-dimensional evaluation of empathetic dialogue responses. In Yaser Al-Onaizan, Mohit Bansal, and Yun-Nung Chen (eds.),Findings of the Association for Computational Linguistics: EMNLP 2024, pp. 2066–2087, Miami, Florida, USA, November 2024. Association for Computational Linguistics. doi: 10.18653/v1/2024.findings-emnlp.113. URLhttps://aclanthology.org/ 2024.findings-emnlp.113/. Zhichao Xu, Yi Han, Tao Yang, Anh Tran, and Qingyao Ai.

**中文**

计算机器协会。 ISBN 9781450394086。doi：10.1145/3539618.3591936。网址https://doi.org/10.1145/3539618.3591936。徐志超、姜杰璞。同理心对话反应的多维度评估。载于 Yaser Al-Onaizan、Mohit Bansal 和 Yun-Nung Chen（编辑），计算语言学协会的调查结果：EMNLP 2024，第 2066-2087 页，美国佛罗里达州迈阿密，2024 年 11 月。计算语言学协会。 doi：10.18653/v1/2024.findings-emnlp.113。网址https://aclanthology.org/2024.findings-emnlp.113/。徐志超、韩毅、杨涛、陈英和艾庆耀。

### 段落 491 · Page 66

**EN**

Learning to rank rationales for explainable recommendation, 2022a. URLhttps://arxiv.org/abs/2206.05368. Zhichao Xu, Anh Tran, Tao Yang, and Qingyao Ai. Reinforcement learning to rank with coarse-grained labels.arXiv preprint arXiv:2208.07563, 2022b. Zhichao Xu, Hansi Zeng, Juntao Tan, Zuohui Fu, Yongfeng Zhang, and Qingyao Ai. A reusable modelagnostic framework for faithfully explainable recommendation and system scrutability.ACM Transactions on Information Systems, 42(1):1–29, 2023. Zhichao Xu, Ashim Gupta, Tao Li, Oliver Bentham, and Vivek Srikumar. Beyond perplexity: Multidimensional safety evaluation of LLM compression.

**中文**

学习对可解释的建议的理由进行排序，2022a。网址https://arxiv.org/abs/2206.05368。徐志超、陈英、杨涛、艾庆耀。强化学习使用粗粒度标签进行排名。arXiv 预印本 arXiv:2208.07563, 2022b。徐志超、曾汉思、谭俊涛、付作辉、张永峰、艾庆耀。一个可重用的模型不可知框架，可忠实解释推荐和系统可审查性。ACM Transactions on Information Systems，42(1):1–29, 2023。Zhichao Xu、Ashim Gupta、Tao Li、Oliver Bentham 和 Vivek Srikumar。超越困惑：LLM压缩的多维安全评估。

### 段落 492 · Page 66

**EN**

In Yaser Al-Onaizan, Mohit Bansal, and Yun-Nung Chen (eds.),Findings of the Association for Computational Linguistics: EMNLP 2024, pp. 15359–15396, Miami, Florida, USA, November 2024b. Association for Computational Linguistics. doi: 10.18653/v1/ 2024.findings-emnlp.901. URLhttps://aclanthology.org/2024.findings-emnlp.901/. Zhichao Xu, Hemank Lamba, Qingyao Ai, Joel Tetreault, and Alex Jaimes. CFE2: Counterfactual editing for search result explanation. InProceedings of the 2024 ACM SIGIR International Conference on Theory of Information Retrieval, pp. 145–155, 2024c. Zhichao Xu, Aosong Feng, Yijun Tian, Haibo Ding, and Lin Lee Cheong.

**中文**

载于 Yaser Al-Onaizan、Mohit Bansal 和 Yun-Nung Chen（编辑），计算语言学协会的调查结果：EMNLP 2024，第 15359–15396 页，美国佛罗里达州迈阿密，2024 年 11 月b。计算语言学协会。 doi：10.18653/v1/2024.findings-emnlp.901。网址https://aclanthology.org/2024.findings-emnlp.901/。徐志超、Hemank Lamba、艾清耀、Joel Tetreault 和 Alex Jaimes。 CFE2：搜索结果解释的反事实编辑。 2024 年 ACM SIGIR 国际信息检索理论会议论文集，第 145-155 页，2024c。徐志超、冯敖松、田一军、丁海波和林利昌。

### 段落 493 · Page 66

**EN**

CSPLADE: Learned sparse retrieval with causal language models. In Kentaro Inui, Sakriani Sakti, Haofen Wang, Derek F. Wong, Pushpak Bhattacharyya, Biplab Banerjee, Asif Ekbal, Tanmoy Chakraborty, and Dhirendra Pratap Singh 66

**中文**

CSPLADE：使用因果语言模型学习稀疏检索。 Kentaro Inui、Sakriani Sakti、Haofen Wang、Derek F. Wong、Pushpak Bhattacharyya、Biplab Banerjee、Asif Ekbal、Tanmoy Chakraborty 和 Dhirendra Pratap Singh 66

### Page 67

### 段落 494 · Page 67

**EN**

Published in Transactions on Machine Learning Research (02/2026) (eds.),Proceedings of the 14th International Joint Conference on Natural Language Processing and the 4th Conference of the Asia-Pacific Chapter of the Association for Computational Linguistics, pp. 99– 114, Mumbai, India, December 2025b. The Asian Federation of Natural Language Processing and The Association for Computational Linguistics. URLhttps://aclanthology.org/2025.ijcnlp-long.7/. Zhichao Xu, Zhiqi Huang, Shengyao Zhuang, and Vivek Srikumar. Distillation versus contrastive learning: How to train your rerankers. In Kentaro Inui, Sakriani Sakti, Haofen Wang, Derek F.

**中文**

发表于机器学习研究汇刊 (02/2026)（编），第 14 届自然语言处理国际联合会议和计算语言学协会亚太分会第四届会议论文集，第 99-114 页，印度孟买，2025 年 12 月b。亚洲自然语言处理联合会和计算语言学协会。网址https://aclanthology.org/2025.ijcnlp-long.7/。徐志超、黄志奇、庄胜耀和 Vivek Srikumar。蒸馏与对比学习：如何训练您的重排者。干太郎、Sakriani Sakti、王浩芬、Derek F.

### 段落 495 · Page 67

**EN**

Wong, Pushpak Bhattacharyya, Biplab Banerjee, Asif Ekbal, Tanmoy Chakraborty, and Dhirendra Pratap Singh (eds.), Proceedings of the 14th International Joint Conference on Natural Language Processing and the 4th Conference of the Asia-Pacific Chapter of the Association for Computational Linguistics, pp. 564–578, Mumbai, India, December 2025c. The Asian Federation of Natural Language Processing and The Association for Computational Linguistics. URLhttps://aclanthology.org/2025.findings-ijcnlp.33/. Zhichao Xu, Minheng Wang, Yawei Wang, Wenqian Ye, Yuntao Du, Yunpu Ma, and Yijun Tian.

**中文**

Wong、Pushpak Bhattacharyya、Biplab Banerjee、Asif Ekbal、Tanmoy Chakraborty 和 Dhirendra Pratap Singh（编），第 14 届自然语言处理国际联合会议和计算语言学协会亚太分会第四届会议论文集，第 564-578 页，印度孟买，12 月2025c。亚洲自然语言处理联合会和计算语言学协会。网址https://aclanthology.org/2025.findings-ijcnlp.33/。徐志超、王敏恒、王亚伟、叶文谦、杜云涛、马云璞和田一君。

### 段落 496 · Page 67

**EN**

Recon: Reasoning with condensation for efficient retrieval-augmented generation, 2025d. URLhttps://arxiv. org/abs/2510.10448. Zhichao Xu, Jinghua Yan, Ashim Gupta, and Vivek Srikumar. State space models are strong text rerankers. In Vaibhav Adlakha, Alexandra Chronopoulou, Xiang Lorraine Li, Bodhisattwa Prasad Majumder, Freda Shi, and Giorgos Vernikos (eds.),Proceedings of the 10th Workshop on Representation Learning for NLP (RepL4NLP-2025), pp.152–169, Albuquerque, NM,May2025e.AssociationforComputationalLinguistics. URLhttps://aclanthology.org/2025.repl4nlp-1.12/.

**中文**

侦察：通过凝结推理实现高效检索增强生成，2025d。网址https://arxiv. org/abs/2510.10448。徐志超、严京华、Ashim Gupta 和 Vivek Srikumar。状态空间模型是强大的文本重新排序器。载于 Vaibhav Adlakha、Alexandra Chronopoulou、Xiang Lorraine Li、Bodhisattwa Prasad Majumder、Freda Shi 和 Giorgos Vernikos（编辑），第 10 届 NLP 表征学习研讨会论文集 (RepL4NLP-2025)，第 152-169 页，阿尔伯克基，新墨西哥州，2025 年 5 月e。计算语言学协会。网址https://aclanthology.org/2025.repl4nlp-1.12/。

### 段落 497 · Page 67

**EN**

Zhichao Xu, Shengyao Zhuang, Xueguang Ma, Bingsen Chen, Yijun Tian, Fengran Mo, Jie Cao, and Vivek Srikumar. Rethinking on-policy optimization for query augmentation.arXiv preprint arXiv:2510.17139, 2025f. Zhichao Xu, Shengyao Zhuang, Crystina Zhang, Xueguang Ma, Yijun Tian, Maitrey Mehta, Jimmy Lin, and Vivek Srikumar. LACONIC: Dense-level effectiveness for scalable sparse retrieval via a two-phase training curriculum.arXiv preprint arXiv:2601.01684, 2026. Le Yan, Zhen Qin, Honglei Zhuang, Rolf Jagerman, Xuanhui Wang, Michael Bendersky, and Harrie Oosterhuis.

**中文**

徐志超、庄盛耀、马雪光、陈丙森、田一君、莫枫然、曹杰和 Vivek Srikumar。重新思考查询增强的策略优化.arXiv 预印本 arXiv:2510.17139, 2025f。徐志超、庄胜耀、张克里斯蒂娜、马雪光、田一君、Maitrey Mehta、Jimmy Lin 和 Vivek Srikumar。 LACONIC：通过两阶段培训课程实现可扩展稀疏检索的密集级有效性。arXiv 预印本 arXiv：2601.01684，2026。Le Yan、Zhen Qi、honglei Zhuang、Rolf Jagerman、Xuanhui Wang、Michael Bendersky 和 ​​Harrie Oosterhuis。

### 段落 498 · Page 67

**EN**

Consolidating ranking and relevance predictions of large language models through postprocessing. In Yaser Al-Onaizan, Mohit Bansal, and Yun-Nung Chen (eds.),Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, pp. 410–423, Miami, Florida, USA, November 2024. Association for Computational Linguistics. doi: 10.18653/v1/2024.emnlp-main.25. URL https://aclanthology.org/2024.emnlp-main.25/. An Yang, Anfeng Li, Baosong Yang, Beichen Zhang, Binyuan Hui, Bo Zheng, Bowen Yu, Chang Gao, Chengen Huang, Chenxu Lv, et al. Qwen3 technical report.arXiv preprint arXiv:2505.09388, 2025a. Eugene Yang, Dawn J.

**中文**

通过后处理整合大型语言模型的排名和相关性预测。载于 Yaser Al-Onaizan、Mohit Bansal 和 Yun-Nung Chen（编辑），2024 年自然语言处理经验方法会议论文集，第 410-423 页，美国佛罗里达州迈阿密，2024 年 11 月。计算语言学协会。 doi：10.18653/v1/2024.emnlp-main.25。网址 https://aclanthology.org/2024.emnlp-main.25/。安阳，李安峰，杨宝松，张北辰，惠斌源，郑波，于博文，高昌，黄承恩，吕晨旭，等。 Qwen3 技术报告.arXiv 预印本 arXiv:2505.09388, 2025a。尤金·杨，黎明·J.

### 段落 499 · Page 67

**EN**

Lawrie, and James Mayfield. Distillation for multilingual information retrieval.Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, 2024. Eugene Yang, Andrew Yates, Kathryn Ricci, Orion Weller, Vivek Chari, Benjamin Van Durme, and Dawn Lawrie. Rank-K: Test-time reasoning for listwise reranking.arXiv preprint arXiv:2505.14432, 2025b. Liu Yang, Qingyao Ai, Jiafeng Guo, and W. Bruce Croft. aNMM: Ranking short answer texts with attentionbased neural matching model. InProceedings of the 25th ACM International on Conference on Information and Knowledge Management, CIKM ’16, pp.

**中文**

劳里和詹姆斯·梅菲尔德。多语言信息检索蒸馏。第 47 届国际 ACM SIGIR 信息检索研究与发展会议论文集，2024 年。Eugene Yang、Andrew Yates、Kathryn Ricci、Orion Weller、Vivek Chari、Benjamin Van Durme 和 Dawn Lawrie。 Rank-K：列表重排的测试时推理。arXiv 预印本 arXiv:2505.14432, 2025b。刘洋、艾清耀、郭嘉峰和 W. 布鲁斯·克罗夫特。 aNMM：使用基于注意力的神经匹配模型对简答文本进行排名。第 25 届 ACM 国际信息和知识管理会议论文集，CIKM '16，第 16 页。

### 段落 500 · Page 67

**EN**

287–296, New York, NY, USA, 2016a. Association for Computing Machinery. doi: 10.1145/2983323.2983818. Songlin Yang, Jan Kautz, and Ali Hatamizadeh. Gated Delta networks: Improving Mamba2 with Delta rule. InThe 13th International Conference on Learning Representations, 2025c. URLhttps://openreview. net/forum?id=r8H7xhYPwz. 67

**中文**

287–296，美国纽约州纽约市，2016a。计算机器协会。号码：10.1145/2983323.2983818。杨松林、扬·考茨和阿里·哈塔米扎德。门控 Delta 网络：使用 Delta 规则改进 Mamba2。在第 13 届学习表征国际会议，2025c。网址https://openreview.网/论坛？id=r8H7xhYPwz。 67

### Page 68

### 段落 501 · Page 68

**EN**

Published in Transactions on Machine Learning Research (02/2026) Tao Yang, Zhichao Xu, and Qingyao Ai. Vertical allocation-based fair exposure amortizing in ranking. InProceedings of the Annual International ACM SIGIR Conference on Research and Development in Information Retrieval in the Asia Pacific Region, pp. 234–244, 2023a. Tao Yang, Zhichao Xu, Zhenduo Wang, and Qingyao Ai. FARA: Future-aware ranking algorithm for fairness optimization. InProceedings of the 32nd ACM International Conference on Information and Knowledge Management, pp. 2906–2916, 2023b. Tao Yang, Zhichao Xu, Zhenduo Wang, Anh Tran, and Qingyao Ai.

**中文**

发表于机器学习研究汇刊 (02/2026) 杨涛、徐志超和艾庆耀。基于垂直分配的公平风险摊销排名。国际 ACM SIGIR 亚太地区信息检索研究与开发年度会议论文集，第 234-244 页，2023a。杨涛，徐志超，王振铎，艾庆耀。 FARA：用于公平优化的未来感知排名算法。第 32 届 ACM 国际信息和知识管理会议论文集，第 2906-2916 页，2023b。杨涛、徐志超、王振铎、Anh Tran 和艾庆耀。

### 段落 502 · Page 68

**EN**

Marginal-certainty-aware fair ranking algorithm. InProceedings of the 16th ACM International Conference on Web Search and Data Mining, pp. 24–32, 2023c. Xiao Yang, Peifeng Yin, Abe Engle, Jinfeng Zhuang, and Ling Leng. MTMD: A multi-task multi-domain framework for unified ad lightweight ranking at pinterest.arXiv preprint arXiv:2510.09857, 2025d. Zichao Yang, Diyi Yang, Chris Dyer, Xiaodong He, Alex Smola, and Eduard Hovy. Hierarchical attention networks for document classification.

**中文**

边际确定性感知公平排名算法。第 16 届 ACM 国际网络搜索和数据挖掘会议论文集，第 24-32 页，2023c。肖阳、尹培峰、Abe Engle、庄金峰和冷凌。 MTMD：用于统一广告轻量级排名的多任务多域框架，位于 pinterest.arXiv 预印本 arXiv:2510.09857，2025d。杨子超、杨迪伊、克里斯·戴尔、何晓东、亚历克斯·斯莫拉和爱德华·霍维。用于文档分类的分层注意网络。

### 段落 503 · Page 68

**EN**

In Kevin Knight, Ani Nenkova, and Owen Rambow (eds.),Proceedings of the 2016 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, pp. 1480–1489, San Diego, California, June 2016b. Association for Computational Linguistics. doi: 10.18653/v1/N16-1174. URLhttps://aclanthology.org/N16-1174/. Shunyu Yao, Jeffrey Zhao, Dian Yu, Nan Du, Izhak Shafran, Karthik R. Narasimhan, and Yuan Cao. ReAct: Synergizing reasoning and acting in language models. InThe 11th International Conference on Learning Representations, 2023. URLhttps://openreview.net/forum?id=WE_vluYUL-X.

**中文**

载于 Kevin Knight、Ani Nenkova 和 Owen Rambow（编辑），计算语言学协会北美分会 2016 年会议记录：人类语言技术，第 1480–1489 页，加利福尼亚州圣地亚哥，2016 年 6 月b。计算语言学协会。 doi：10.18653/v1/N16-1174。网址https://aclanthology.org/N16-1174/。姚顺宇、赵杰弗里、余殿、杜南、伊扎克·沙夫兰、卡蒂克·R·纳拉西姆汉和曹元。 ReAct：在语言模型中协同推理和行动。在第 11 届学习表征国际会议，2023 年。URL https://openreview.net/forum?id=WE_vluYUL-X。

### 段落 504 · Page 68

**EN**

Zonghai Yao, Aditya Parashar, Huixue Zhou, Won Seok Jang, Feiyun Ouyang, Zhichao Yang, and Hong Yu. MCQG-SRefine: Multiple choice question generation and evaluation with iterative self-critique, correction, and comparison feedback.arXiv preprint arXiv:2410.13191, 2024. Zeynep Akkalyoncu Yilmaz, Wei Yang, Haotian Zhang, and Jimmy Lin. Cross-domain modeling of sentencelevel evidence for document retrieval. InConference on Empirical Methods in Natural Language Processing, 2019. Wenpeng Yin, Hinrich Schütze, Bing Xiang, and Bowen Zhou.

**中文**

姚宗海、Aditya Parashar、周惠学、Won Seok Jang、欧阳飞云、杨志超和洪宇。 MCQG-SRefine：通过迭代自我批评、纠正和比较反馈进行多项选择题生成和评估。arXiv 预印本 arXiv:2410.13191, 2024。Zeynep Akkalyoncu Yilmaz、Wei Yang、Haotian Zhang 和 Jimmy Lin。用于文档检索的句子级证据的跨域建模。自然语言处理经验方法会议，2019 年。Wenpeng Yin、Hinrich Schütze、Bing Xian 和 Bowen Zhou。

### 段落 505 · Page 68

**EN**

ABCNN: Attention-based convolutional neural network for modeling sentence pairs.Transactions of the Association for computational linguistics, 4:259–272, 2016. Soyoung Yoon, Eunbi Choi, Jiyeon Kim, Hyeongu Yun, Yireun Kim, and Seung-won Hwang. ListT5: Listwise reranking with fusion-in-decoder improves zero-shot retrieval. In Lun-Wei Ku, Andre Martins, and Vivek Srikumar (eds.),Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pp. 2287–2308, Bangkok, Thailand, 2024. Association for Computational Linguistics. doi: 10.18653/v1/2024.acl-long.125.

**中文**

ABCNN：用于建模句子对的基于注意力的卷积神经网络。计算语言学协会交易，4:259–272, 2016。Soyoung Yoon、Eunbi Choi、Jiyeon Kim、Hyungu Yun、Yireun Kim 和 Seung-won Hwang。 ListT5：使用解码器融合进行列表重排序改进了零样本检索。见 Lun-Wei Ku、Andre Martins 和 Vivek Srikumar（编），计算语言学协会第 62 届年会论文集（第一卷：长论文），第 2287-2308 页，泰国曼谷，2024 年。计算语言学协会。 doi：10.18653/v1/2024.acl-long.125。

### 段落 506 · Page 68

**EN**

URLhttps://aclanthology.org/2024.acl-long.125/. Soyoung Yoon, Gyuwan Kim, Gyu-Hwung Cho, and Seung won Hwang. AcuRank: Uncertainty-aware adaptive computation for listwise reranking.arXiv preprint arXiv:2505.18512, 2025. Ori Yoran, Tomer Wolfson, Ori Ram, and Jonathan Berant. Making retrieval-augmented language models robust to irrelevant context. InICLR 2024 Workshop on Large Language Model (LLM) Agents, 2024. Ronghui You, Zihan Zhang, Ziye Wang, Suyang Dai, Hiroshi Mamitsuka, and Shanfeng Zhu. AttentionXML: Label tree-based attention-aware deep model for high-performance extreme multi-label text classification.

**中文**

网址https://aclanthology.org/2024.acl-long.125/。 Soyoung Yoon、Gyuwan Kim、Gyu-Hwung Cho 和 Seung won Hwang。 AcuRank：用于列表重排的不确定性自适应计算。arXiv 预印本 arXiv：2505.18512，2025。Ori Yoran、Tomer Wolfson、Ori Ram 和 Jonathan Berant。使检索增强语言模型对不相关的上下文具有鲁棒性。 InICLR 2024大型语言模型（LLM）智能体研讨会，2024年。Ronghui You、Zihan Zhang、Ziye Wang、Suyang Dai、Hiroshi Mamitsuka 和 Shanfeng Zhu。 AttentionXML：基于标签树的注意力感知深度模型，用于高性能极端多标签文本分类。

### 段落 507 · Page 68

**EN**

Advances in neural information processing systems, 32, 2019. Hongli Yu, Tinghong Chen, Jiangtao Feng, Jiangjie Chen, Weinan Dai, Qiying Yu, Ya-Qin Zhang, Wei- Ying Ma, Jingjing Liu, Mingxuan Wang, and Hao Zhou. Memagent: Reshaping long-context llm with multi-conv rl-based memory agent, 2025. URLhttps://arxiv.org/abs/2507.02259. Hsiang-Fu Yu, Kai Zhong, Jiong Zhang, Wei-Cheng Chang, and Inderjit S. Dhillon. PECOS: Prediction for enormous and correlated output spaces.Journal of Machine Learning Research, 23(98):1–32, 2022a. 68

**中文**

神经信息处理系统进展，32，2019。于红利，陈廷红，冯江涛，陈江杰，戴伟南，余启英，张亚勤，马伟英，刘晶晶，王明轩，周浩。 Memagent：使用基于多卷积 rl 的内存代理重塑长上下文 llm，2025。URLhttps://arxiv.org/abs/2507.02259。于祥福、钟凯、张炯、张伟成和 Inderjit S. Dhillon。 PECOS：对巨大且相关的输出空间的预测。机器学习研究杂志，23（98）：1-32，2022a。 68

### Page 69

### 段落 508 · Page 69

**EN**

Published in Transactions on Machine Learning Research (02/2026) Puxuan Yu and James Allan. A study of neural matching models for cross-lingual IR. InProceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 1637–1640, 2020. Puxuan Yu, Razieh Rahimi, and James Allan. Towards explainable search results: a listwise explanation generator. InProceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 669–680, 2022b. Puxuan Yu, Antonio Mallia, and Matthias Petri. Improved learned sparse retrieval with corpus-specific vocabularies.

**中文**

发表于机器学习研究汇刊 (02/2026) Puxuan Yu 和 James Allan。跨语言IR神经匹配模型的研究。第 43 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 1637-1640 页，2020 年。Puxuan Yu、Razieh Rahimi 和 James Allan。走向可解释的搜索结果：列表解释生成器。第 45 届国际 ACM SIGIR 信息检索研究与开发会议论文集，第 669-680 页，2022b。于璞轩、安东尼奥·马利亚和马蒂亚斯·佩特里。使用语料库特定词汇改进学习稀疏检索。

### 段落 509 · Page 69

**EN**

InEuropean Conference on Information Retrieval, pp. 181–194. Springer, 2024a. Puxuan Yu, Luke Merrick, Gaurav Nuti, and Daniel Campos. Arctic-Embed 2.0: Multilingual retrieval without compromise.arXiv preprint arXiv:2412.04506, 2024b. Wenhao Yu, Hongming Zhang, Xiaoman Pan, Peixin Cao, Kaixin Ma, Jian Li, Hongwei Wang, and Dong Yu. Chain-of-Note: Enhancing robustness in retrieval-augmented language models. In Yaser Al-Onaizan, Mohit Bansal, and Yun-Nung Chen (eds.),Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, pp. 14672–14685, Miami, Florida, USA, November 2024c.

**中文**

欧洲信息检索会议，第 181-194 页。施普林格，2024a。于璞轩、卢克·梅里克、高拉夫·努蒂和丹尼尔·坎波斯。 Arctic-Embed 2.0：不妥协的多语言检索。arXiv 预印本 arXiv:2412.04506, 2024b。于文浩、张洪明、潘小曼、曹培新、马开心、李健、王宏伟和于东。 Chain-of-Note：增强检索增强语言模型的稳健性。载于 Yaser Al-Onaizan、Mohit Bansal 和 Yun-Nung Chen（编辑），2024 年自然语言处理经验方法会议论文集，第 14672-14685 页，美国佛罗里达州迈阿密，2024 年 11 月c。

### 段落 510 · Page 69

**EN**

Association for Computational Linguistics. doi: 10.18653/v1/2024.emnlp-main.813. URLhttps://aclanthology.org/ 2024.emnlp-main.813/. Yue Yu, Chenyan Xiong, Si Sun, Chao Zhang, and Arnold Overwijk. COCO-DR: Combating the distribution shift in zero-shot dense retrieval with contrastive and distributionally robust learning. In Yoav Goldberg, Zornitsa Kozareva, and Yue Zhang (eds.),Proceedings of the 2022 Conference on Empirical Methods in Natural Language Processing, pp. 1462–1479, Abu Dhabi, United Arab Emirates, December 2022c. Association for Computational Linguistics. doi: 10.18653/v1/2022.emnlp-main.95.

**中文**

计算语言学协会。 doi：10.18653/v1/2024.emnlp-main.813。网址https://aclanthology.org/2024.emnlp-main.813/。于悦、熊陈彦、孙思、张超和阿诺德·奥弗韦克。 COCO-DR：通过对比和分布鲁棒学习来对抗零样本密集检索中的分布变化。载于 Yoav Goldberg、Zornitsa Kozareva 和 Yue Zhu（编辑），2022 年自然语言处理经验方法会议论文集，第 1462-1479 页，阿拉伯联合酋长国阿布扎比，2022 年 12 月c。计算语言学协会。 doi：10.18653/v1/2022.emnlp-main.95。

### 段落 511 · Page 69

**EN**

URL https://aclanthology.org/2022.emnlp-main.95/. Hamed Zamani and W. Bruce Croft. Joint modeling and optimization of search and recommendation. In Biennial Conference on Design of Experimental Search & Information Retrieval Systems, 2018. Hamed Zamani, Mostafa Dehghani, W. Bruce Croft, Erik Learned-Miller, and Jaap Kamps. From neural re-ranking to neural ranking: Learning a sparse representation for inverted indexing. InProceedings of the 27th ACM International Conference on Information and Knowledge Management, pp. 497–506, 2018.

**中文**

网址 https://aclanthology.org/2022.emnlp-main.95/。哈米德·扎马尼 (Hamed Zamani) 和 W·布鲁斯·克罗夫特 (W. Bruce Croft)。搜索和推荐的联合建模和优化。实验搜索和信息检索系统设计双年度会议，2018 年。Hamed Zamani、Mostafa Dehghani、W. Bruce Croft、Erik Learned-Miller 和 Jaap Kamps。从神经重新排序到神经排序：学习倒排索引的稀疏表示。第 27 届 ACM 国际信息和知识管理会议论文集，第 497-506 页，2018 年。

### 段落 512 · Page 69

**EN**

Rabih Zbib, Lingjun Zhao, Damianos Karakos, William Hartmann, Jay DeYoung, Zhongqiang Huang, Zhuolin Jiang, Noah Rivkin, Le Zhang, Richard Schwartz, et al. Neural-network lexical translation for cross-lingual ir from text and speech. InProceedings of the 42nd International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 645–654, 2019. Hansi Zeng, Chen Luo, Bowen Jin, Sheikh Muhammad Sarwar, Tianxin Wei, and Hamed Zamani. Scalable and effective generative information retrieval. InProceedings of the ACM Web Conference 2024, WWW ’24, pp. 1441–1452, New York, NY, USA, 2024. Association for Computing Machinery.

**中文**

Rabih Zbib、赵令军、Damianos Karakos、William Hartmann、Jay DeYoung、黄忠强、蒋卓林、Noah Rivkin、张乐、Richard Schwartz 等。用于文本和语音跨语言的神经网络词汇翻译。第 42 届国际 ACM SIGIR 信息检索研究与发展会议论文集，第 645-654 页，2019 年。Hansi Zeng、Chen Luo、Bowen Jin、Sheikh Muhammad Sarwar、Tianxin Wei 和 Hamed Zamani。可扩展且有效的生成信息检索。 2024 年 ACM 网络会议记录，WWW '24，第 1441–1452 页，美国纽约州纽约市，2024 年。计算机协会。

### 段落 513 · Page 69

**EN**

doi: 10.1145/ 3589334.3645477. ChengXiang Zhai and John Lafferty. A study of smoothing methods for language models applied to information retrieval.ACM Transactions on Information Systems (TOIS), 22(2):179–214, 2004. ChengXiang Zhai et al. Statistical language models for information retrieval a critical review.Foundations and Trends in Information Retrieval, 2(3):137–213, 2008. Jiaqi Zhai, Lucy Liao, Xing Liu, Yueming Wang, Rui Li, Xuan Cao, Leon Gao, Zhaojie Gong, Fangda Gu, Michael He, Yin-Hua Lu, and Yu Shi.

**中文**

号码：10.1145/3589334.3645477。翟成祥和约翰·拉弗蒂。应用于信息检索的语言模型平滑方法的研究。ACM Transactions on Information Systems (TOIS), 22(2):179–214, 2004。ChengXiang Zhai 等。信息检索统计语言模型批判性评论。信息检索基础与趋势，2(3):137–213, 2008。Jiaqi Zhai、Lucy Liao、Xing Liu、Yueming Wang、Rui Li、Xuan Cao、Leon Gau、Zhaojie Kong、Fangda Gu、Michael He、Yin-Hua Lu 和 Yu Shi。

### 段落 514 · Page 69

**EN**

Actions speak louder than words: Trillion-parameter sequential transducers for generative recommendations.arXiv preprint arXiv:2402.17152, 2024. Xiaohua Zhai, Basil Mustafa, Alexander Kolesnikov, and Lucas Beyer. Sigmoid loss for language image pre-training. InProceedings of the IEEE/CVF International Conference on Computer Vision, pp. 11975– 11986, 2023. 69

**中文**

行动胜于雄辩：用于生成建议的万亿参数顺序传感器。arXiv 预印本 arXiv:2402.17152, 2024。Xiaohua Zhai、Basil Mustafa、Alexander Kolesnikov 和 Lucas Beyer。语言图像预训练的 Sigmoid 损失。 IEEE/CVF 国际计算机视觉会议论文集，第 11975–11986 页，2023 年。 69

### Page 70

### 段落 515 · Page 70

**EN**

Published in Transactions on Machine Learning Research (02/2026) Jingtao Zhan, Jiaxin Mao, Yiqun Liu, Min Zhang, and Shaoping Ma. RepBERT: Contextualized text embeddings for 1st-stage retrieval.arXiv preprint arXiv:2006.15498, 2020. Jingtao Zhan, Jiaxin Mao, Yiqun Liu, Jiafeng Guo, Min Zhang, and Shaoping Ma. Optimizing dense retrieval model training with hard negatives. InProceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, pp. 1503–1512, 2021. Fengji Zhang, Bei Chen, Yue Zhang, Jacky Keung, Jin Liu, Daoguang Zan, Yi Mao, Jian-Guang Lou, and Weizhu Chen.

**中文**

发表于机器学习研究汇刊 (02/2026) Jingtao Zhan、Jiaxin Mao、Yiqun Liu、Min 张和 Shaoping Ma。 RepBERT：第一阶段检索的上下文文本嵌入。arXiv 预印本 arXiv：2006.15498，2020。Jingtao Zhan、Jiaxin Mao、Yiqun Liu、JiafengGuo、MinZhang 和 ShaopingMa。使用硬负例优化密集检索模型训练。第 44 届国际 ACM SIGIR 信息检索研究与发展会议论文集，第 1503-1512 页，2021 年。Fengji Zhang、Bei Chen、Yue Zhu、Jacky Keung、Jin Liu、Daoguang Zan、Yi Mao、Jian-Guang Lou 和 Weizhu Chen。

### 段落 516 · Page 70

**EN**

RepoCoder: Repository-level code completion through iterative retrieval and generation. In Houda Bouamor, Juan Pino, and Kalika Bali (eds.),Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, pp. 2471–2484, Singapore, December 2023a. Association for Computational Linguistics. doi: 10.18653/v1/2023.emnlp-main.151. URLhttps://aclanthology.org/ 2023.emnlp-main.151/. Hanqi Zhang, Chong Chen, Lang Mei, Qi Liu, and Jiaxin Mao. Mamba retriever: Utilizing Mamba for effective and efficient dense retrieval. InProceedings of the 33rd ACM International Conference on Information and Knowledge Management, pp.

**中文**

RepoCoder：通过迭代检索和生成来完成存储库级代码。载于 Houda Bouamor、Juan Pino 和 Kalika Bali（编辑），2023 年自然语言处理经验方法会议论文集，第 2471-2484 页，新加坡，2023 年 12 月a。计算语言学协会。 doi：10.18653/v1/2023.emnlp-main.151。网址https://aclanthology.org/2023.emnlp-main.151/。张涵琪、陈冲、梅郎、刘奇、毛嘉欣。曼巴检索器：利用曼巴进行有效且高效的密集检索。第 33 届 ACM 国际信息与知识管理会议论文集，第 33 页。

### 段落 517 · Page 70

**EN**

4268–4272, 2024. Huaiwen Zhang, Yang Yang, Fan Qi, Shengsheng Qian, and Changsheng Xu. Debiased video-text retrieval via soft positive sample calibration.IEEE Transactions on Circuits and Systems for Video Technology, 33:5257–5270, 2023b. Shujian Zhang, Chengyue Gong, and Eunsol Choi. Knowing more about questions can help: Improving calibration in question answering. In Chengqing Zong, Fei Xia, Wenjie Li, and Roberto Navigli (eds.), Findings of the Association for Computational Linguistics: ACL-IJCNLP 2021, pp. 1958–1970, Online, August 2021a. Association for Computational Linguistics. doi: 10.18653/v1/2021.findings-acl.172.

**中文**

4268–4272, 2024。张怀文，杨阳，范琪，钱胜胜，徐长胜。通过软正样本校准进行去偏视频文本检索。IEEE Transactions on Circuits and Systems for Video Technology, 33:5257–5270, 2023b。张书建，龚成跃，崔恩索尔。了解更多有关问题的信息可以帮助： 提高回答问题的校准能力。载于 Chengqing Zong、Fei Xia、Wenjie Li 和 Roberto Navigli（编辑），计算语言学协会的发现：ACL-IJCNLP 2021，第 1958-1970 页，在线，2021 年 8 月a。计算语言学协会。 doi：10.18653/v1/2021.findings-acl.172。

### 段落 518 · Page 70

**EN**

URL https://aclanthology.org/2021.findings-acl.172/. Weinan Zhang, Junwei Liao, Ning Li, Kounianhua Du, and Jianghao Lin. Agentic information retrieval. arXiv preprint arXiv:2410.09713, 2025a. XinyuZhang, AndrewYates, andJimmyLin. Comparingscoreaggregationapproachesfordocumentretrieval with pretrained transformers. In Djoerd Hiemstra, Marie-Francine Moens, Josiane Mothe, Raffaele Perego, Martin Potthast, and Fabrizio Sebastiani (eds.),Advances in Information Retrieval, pp. 150–163, Cham, 2021b. Springer International Publishing. Xinyu Zhang, Kelechi Ogueji, Xueguang Ma, and Jimmy Lin.

**中文**

网址 https://aclanthology.org/2021.findings-acl.172/。张伟南、廖俊伟、李宁、杜口年华、林江浩。代理信息检索。 arXiv 预印本 arXiv:2410.09713, 2025a。张新宇、安德鲁·耶茨和吉米·林。将文档检索的分数聚合方法与预训练的Transformer进行比较。载于 Djoerd Hiemstra、Marie-Francine Moens、Josiane Mothe、Raffaele Perego、Martin Potthast 和 Fabrizio Sebastiani（编辑），《信息检索进展》，第 150-163 页，Cham，2021b。施普林格国际出版社。张新宇、Kelechi Ogueji、马学光和林吉米。

### 段落 519 · Page 70

**EN**

Toward best practices for training multilingual dense retrieval models.ACM Transactions on Information Systems, 42:1–33, 2022. Xinyu Zhang, Sebastian Hofstätter, Patrick Lewis, Raphael Tang, and Jimmy Lin. Rank-without-GPT: Building GPT-independent listwise rerankers on open-source large language models.arXiv preprint arXiv:2312.02969, 2023c. Xinyu Zhang, Nandan Thakur, Odunayo Ogundepo, Ehsan Kamalloo, David Alfonso-Hermelo, Xiaoguang Li, Qun Liu, Mehdi Rezagholizadeh, and Jimmy Lin. MIRACL: A multilingual retrieval dataset covering 18 diverse languages.Transactions of the Association for Computational Linguistics, 11:1114–1131, 2023d.

**中文**

走向训练多语言密集检索模型的最佳实践。ACM Transactions on Information Systems，42:1–33, 2022。Xinyu Zhang、Sebastian Hofstätter、Patrick Lewis、Raphael Tang 和 Jimmy Lin。 Rank-without-GPT：在开源大型语言模型上构建独立于 GPT 的列表重排序器。arXiv 预印本 arXiv：2312.02969，2023c。张馨予、南丹·塔库尔、Odunayo Ogundepo、Ehsan Kamalloo、David Alfonso-Hermelo、李晓光、刘群、Mehdi Rezagholizadeh 和 Jimmy Lin。 MIRACL：涵盖 18 种不同语言的多语言检索数据集。计算语言学协会汇刊，11：1114–1131，2023d。

### 段落 520 · Page 70

**EN**

Yanzhao Zhang, Mingxin Li, Dingkun Long, Xin Zhang, Huan Lin, Baosong Yang, Pengjun Xie, An Yang, Dayiheng Liu, Junyang Lin, et al. Qwen3 embedding: Advancing text embedding and reranking through foundation models.arXiv preprint arXiv:2506.05176, 2025b. Bowen Zheng, Yupeng Hou, Hongyu Lu, Yu Chen, Wayne Xin Zhao, and Ji rong Wen. Adapting large language models by integrating collaborative semantics for recommendation.2024 IEEE 40th International Conference on Data Engineering (ICDE), pp. 1435–1448, 2023. Kai Zheng, Haijun Zhao, Rui Huang, Beichuan Zhang, Na Mou, Yanan Niu, Yang Song, Hongning Wang, and Kun Gai.

**中文**

张艳照，李明欣，龙定坤，张鑫，林焕，杨宝松，谢鹏军，安阳，刘大一恒，林俊阳，等。 Qwen3 嵌入：通过基础模型推进文本嵌入和重排。arXiv 预印本 arXiv:2506.05176, 2025b。郑博文、侯玉鹏、卢宏宇、陈宇、赵鑫、文吉荣。通过集成协作语义来调整大型语言模型以进行推荐。2024 年 IEEE 第 40 届国际数据工程会议 (ICDE)，第 1435–1448 页，2023 年。郑凯、赵海军、黄锐、张北川、牟娜、牛亚楠、宋阳、王洪宁和盖坤。

### 段落 521 · Page 70

**EN**

Full stage learning to rank: A unified framework for multi-stage systems.Proceedings of the ACM Web Conference 2024, 2024a. 70

**中文**

全阶段学习排名：多阶段系统的统一框架。2024 年 ACM 网络会议记录，2024a。 70

### Page 71

### 段落 522 · Page 71

**EN**

Published in Transactions on Machine Learning Research (02/2026) Lianmin Zheng, Liangsheng Yin, Zhiqiang Xie, Chuyue Livia Sun, Jeff Huang, Cody Hao Yu, Shiyi Cao, Christos Kozyrakis, Ion Stoica, Joseph E. Gonzalez, et al. SGLang: Efficient execution of structured language model programs.Advances in Neural Information Processing Systems, 37:62557–62583, 2024b. Zexuan Zhong, Ziqing Huang, Alexander Wettig, and Danqi Chen. Poisoning retrieval corpora by injecting adversarial passages. In Houda Bouamor, Juan Pino, and Kalika Bali (eds.),Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, pp.

**中文**

发表于 Transactions on Machine Learning Research (02/2026) Lianmin Cheng、Liangsheng Yin、Zhiqiang Xie、Chuyue Livia Sun、Jeff Huang、Codyhao Yu、Shiyi Cao、Christos Kozyrakis、Ion Stoica、Joseph E. Gonzalez 等。 SGLang：结构化语言模型程序的高效执行。神经信息处理系统的进展，37：62557–62583，2024b。钟泽轩、黄子清、亚历山大·韦蒂格和陈丹琪。通过注入对抗性段落来毒害检索语料库。载于 Houda Bouamor、Juan Pino 和 Kalika Bali（编），《2023 年自然语言处理经验方法会议论文集》，第 174 页。

### 段落 523 · Page 71

**EN**

13764–13775, Singapore, December 2023. Association for Computational Linguistics. doi: 10.18653/v1/2023.emnlp-main.849. URLhttps: //aclanthology.org/2023.emnlp-main.849/. Yujia Zhou, Yan Liu, Xiaoxi Li, Jiajie Jin, Hongjin Qian, Zheng Liu, Chaozhuo Li, Zhicheng Dou, Tsung- Yi Ho, and Philip S. Yu. Trustworthiness in retrieval-augmented generation systems: A survey.arXiv preprint arXiv:2409.10102, 2024. Ming Zhu, Aman Ahuja, Wei Wei, and Chandan K. Reddy. A hierarchical attention retrieval model for healthcare question answering. InThe World Wide Web Conference, pp. 2472–2482, 2019.

**中文**

13764–13775，新加坡，2023 年 12 月。计算语言学协会。 doi：10.18653/v1/2023.emnlp-main.849。网址https://aclanthology.org/2023.emnlp-main.849/。周宇佳、刘岩、李小西、金家杰、钱宏进、刘正、李超卓、窦志成、何宗义和 Philip S. Yu。检索增强生成系统的可信度：一项调查。arXiv 预印本 arXiv:2409.10102, 2024。Ming Zhu、Aman Ahuja、Wei Wei 和 Chandan K. Reddy。用于医疗保健问答的分层注意力检索模型。 《万维网会议》，第 2472–2482 页，2019 年。

### 段落 524 · Page 71

**EN**

Yutao Zhu, Huaying Yuan, Shuting Wang, Jiongnan Liu, Wenhan Liu, Chenlong Deng, Haonan Chen, Zheng Liu, Zhicheng Dou, and Ji-Rong Wen. Large language models for information retrieval: A survey.arXiv preprint arXiv:2308.07107, 2023. Honglei Zhuang, Zhen Qin, Rolf Jagerman, Kai Hui, Ji Ma, Jing Lu, Jianmo Ni, Xuanhui Wang, and Michael Bendersky. RankT5: Fine-tuning T5 for text ranking with ranking losses. InProceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’23, pp. 2308–2313, New York, NY, USA, 2023a. Association for Computing Machinery. doi: 10.1145/3539618.3592047.

**中文**

朱玉涛、袁华英、王淑婷、刘琼南、刘文涵、邓陈龙、陈浩南、刘峥、窦志成和温继荣。用于信息检索的大型语言模型：调查.arXiv 预印本 arXiv:2308.07107, 2023。 Honglei Zhuang、Zhen Qi、Rolf Jagerman、Kai Hui、Ji Ma、Jing Lu、Jianmo Ni、Xuanhui Wang 和 Michael Bendersky。 RankT5：微调 T5 以进行文本排名，但有排名损失。第 46 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR ’23，第 2308–2313 页，美国纽约州纽约，2023a。计算机器协会。号码：10.1145/3539618.3592047。

### 段落 525 · Page 71

**EN**

Honglei Zhuang, Zhen Qin, Kai Hui, Junru Wu, Le Yan, Xuanhui Wang, and Michael Bendersky. Beyond yes and no: Improving zero-shot LLM rankers via scoring fine-grained relevance labels. In Kevin Duh, Helena Gomez, and Steven Bethard (eds.),Proceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 2: Short Papers), pp. 358–370, Mexico City, Mexico, June 2024a. Association for Computational Linguistics. doi: 10.18653/v1/2024.naacl-short.31. URLhttps://aclanthology.org/2024.naacl-short.31/. Shengyao Zhuang, Hang Li, and Guido Zuccon.

**中文**

庄红雷、秦真、惠凯、吴君如、颜乐、王宣辉和迈克尔·本德斯基。超越是与否：通过对细粒度的相关性标签进行评分来改进零样本法学硕士排名。载于 Kevin Duh、Helena Gomez 和 Steven Bethard（编辑），计算语言学协会北美分会 2024 年会议记录：人类语言技术（第 2 卷：短论文），第 358-370 页，墨西哥墨西哥城，2024 年 6 月a。计算语言学协会。 doi：10.18653/v1/2024.naacl-short.31。网址https://aclanthology.org/2024.naacl-short.31/。庄胜耀，李航，Guido Zuccon。

### 段落 526 · Page 71

**EN**

Deep query likelihood model for information retrieval. In Advances in Information Retrieval: 43rd European Conference on IR Research, ECIR 2021, Virtual Event, March 28–April 1, 2021, Proceedings, Part II 43, pp. 463–470. Springer, 2021. Shengyao Zhuang, Bing Liu, Bevan Koopman, and Guido Zuccon. Open-source large language models are strong zero-shot query likelihood models for document ranking. In Houda Bouamor, Juan Pino, and Kalika Bali (eds.),Findings of the Association for Computational Linguistics: EMNLP 2023, pp. 8807– 8817, Singapore, December 2023b. Association for Computational Linguistics. doi: 10.18653/v1/2023. findings-emnlp.590.

**中文**

用于信息检索的深度查询似然模型。信息检索进展：第 43 届欧洲 IR 研究会议，ECIR 2021，虚拟活动，2021 年 3 月 28 日至 4 月 1 日，会议记录，第 II 部分 43，第 463-470 页。 Springer，2021。Shengyao Zhuang、Bing Liu、Bevan Koopman 和 Guido Zuccon。开源大型语言模型是用于文档排名的强大的零样本查询似然模型。载于 Houda Bouamor、Juan Pino 和 Kalika Bali（编辑），计算语言学协会的调查结果：EMNLP 2023，第 8807-8817 页，新加坡，2023 年 12 月b。计算语言学协会。 doi：10.18653/v1/2023。调查结果-emnlp.590。

### 段落 527 · Page 71

**EN**

URLhttps://aclanthology.org/2023.findings-emnlp.590/. Shengyao Zhuang, Honglei Zhuang, Bevan Koopman, and Guido Zuccon. A setwise approach for effective and highly efficient zero-shot ranking with large language models. InProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’24, pp. 38–47, New York, NY, USA, 2024b. Association for Computing Machinery. doi: 10.1145/3626772.3657813. Shengyao Zhuang, Xueguang Ma, Bevan Koopman, Jimmy Lin, and Guido Zuccon. Rank-R1: Enhancing reasoning in LLM-based document rerankers via reinforcement learning.arXiv preprint arXiv:2503.06034, 2025.

**中文**

网址https://aclanthology.org/2023.findings-emnlp.590/。庄盛耀、庄红雷、Bevan Koopman 和 Guido Zuccon。一种使用大型语言模型进行有效且高效的零样本排名的集合方法。第 47 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR ’24，第 38-47 页，美国纽约州纽约，2024b。计算机器协会。号码：10.1145/3626772.3657813。庄圣耀、马雪光、Bevan Koopman、Jimmy Lin 和 Guido Zuccon。 Rank-R1：通过强化学习增强基于 LLM 的文档重排序器中的推理。arXiv 预印本 arXiv：2503.06034，2025。

### 段落 528 · Page 71

**EN**

Justin Zobel, Alistair Moffat, and Kotagiri Ramamohanarao. Inverted files versus signature files for text indexing.ACM Transactions on Database Systems (TODS), 23(4):453–490, 1998. 71

**中文**

贾斯汀·佐贝尔、阿利斯泰尔·莫法特和科塔吉里·拉莫哈纳劳。用于文本索引的倒排文件与签名文件。ACM 数据库系统事务 (TODS), 23(4):453–490, 1998。 71
