# SearchRAG: Can Search Engines Be Helpful for LLM-based Medical Question Answering?

- ID: 74
- 类型: pdf
- 分类: 04_academic_papers
- 主题: search-engine-backed RAG and answer generation
- 原文链接: https://arxiv.org/pdf/2502.13233
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

SearchRAG: Can Search Engines Be Helpful for LLM-based Medical Question Answering? Yucheng Shi1, Tianze Yang1, Canyu Chen2, Quanzheng Li3, Tianming Liu1, Xiang Li3, Ninghao Liu1, 1University of Georgia, 2Illinois Institute of Technology, 3Massachusetts General Hospital and Harvard Medical School, Abstract Large Language Models (LLMs) have shown remarkable capabilities in general domains but often struggle with tasks requiring specialized knowledge.

**中文**

SearchRAG：搜索引擎对法学硕士的医学问答有帮助吗？ Yu Cheng Shi1、Tianze Yang1、Canyu Chen2、Quanzheng Li3、Tianming Liu1、Xiang Li3、Ninghao Liu1、1佐治亚大学、2伊利诺伊理工学院、3麻省总医院和哈佛医学院，抽象大语言模型（LLM）在一般领域表现出了卓越的能力，但常常在需要专业知识的任务中遇到困难。

### 段落 2 · Page 1

**EN**

Conventional Retrieval- Augmented Generation (RAG) techniques typically retrieve external information from static knowledge bases, which can be outdated or incomplete, missing fine-grained clinical details essential for accurate medical question answering. In this work, we propose SearchRAG, a novel framework that overcomes these limitations by leveraging real-time search engines.

**中文**

传统的检索增强生成（RAG）技术通常从静态知识库中检索外部信息，这些信息可能过时或不完整，缺少准确的医学问题回答所必需的细粒度临床细节。在这项工作中，我们提出了 SearchRAG，这是一种通过利用实时搜索引擎克服这些限制的新颖框架。

### 段落 3 · Page 1

**EN**

Our method employs synthetic query generation to convert complex medical questions into search-engine-friendly queries and utilizes uncertainty-based knowledge selection to filter and incorporate the most relevant and informative medical knowledge into the LLM’s input. Experimental results demonstrate that our method significantly improves response accuracy in medical question answering tasks, particularly for complex questions requiring detailed and up-to-date knowledge. 1 Introduction Large language models (LLMs) have shown proficiency in handling general-domain question answering tasks (Brown et al., 2020).

**中文**

我们的方法采用合成查询生成将复杂的医学问题转换为搜索引擎友好的查询，并利用基于不确定性的知识选择来过滤最相关和信息最丰富的医学知识并将其合并到法学硕士的输入中。实验结果表明，我们的方法显着提高了医学问答任务的响应准确性，特别是对于需要详细和最新知识的复杂问题。 1 简介 大型语言模型 (LLM) 已表现出处理通用领域问答任务的能力（Brown 等人，2020）。

### 段落 4 · Page 1

**EN**

However, they often face challenges when dealing with specialized fields that require up-to-date or domainspecific knowledge, such as medical question answering (Jin et al., 2021; Pal et al., 2022). The limitation arises because the LLM parameters remain fixed after training, preventing the model from incorporating new medical knowledge essential for precise decision-making.

**中文**

然而，在处理需要最新或特定领域知识的专业领域（例如医学问答）时，他们经常面临挑战（Jin 等人，2021；Pal 等人，2022）。之所以出现这种限制，是因为 LLM 参数在训练后保持固定，导致模型无法纳入精确决策所必需的新医学知识。

### 段落 5 · Page 1

**EN**

Retrieval-Augmented Generation (RAG) methods have been proposed to address this issue by incorporating external knowledge sources into the LLMs’ input, thereby enhancing performance with additional context (Guu et al., 2020; Wang et al., MedMCQA MMLU_Med MedQA 50 60 70 80 90Accuracy (%) 56.0 74.5 65.9 55.9 75.0 64.9 56.8 74.7 69.0 65.1 84.7 71.5 Performance on Medical QA Benchmarks (LLaMA 8B) CoT MedRAG i-MedRAG Ours Figure 1: Performance comparison of different methods on medical QA benchmarks using LLaMA 8B.

**中文**

人们提出了检索增强生成（RAG）方法来解决这个问题，通过将外部知识源纳入法学硕士的输入，从而通过额外的上下文来提高性能（Guu等人，2020；Wang等人，MedMCQA MMLU_Med MedQA 50 60 70 80 90准确度（％）56.0 74.5 65.9 55.9 75.0 64.9 56.8 74.7 69.0 65.1 84.7 71.5 医疗 QA 基准的性能 (LLaMA 8B) CoT MedRAG i-MedRAG 我们的 图 1：使用 LLaMA 8B 的医疗 QA 基准上不同方法的性能比较。

### 段落 6 · Page 1

**EN**

Our proposed method consistently outperforms baseline approaches (CoT), conventional RAG (MedRAG), and iterative RAG (i-MedRAG) across all three datasets (MedMCQA, MMLU_Med, and MedQA), demonstrating significant improvements in accuracy. 2021). Traditional RAG approaches typically retrieve information from static knowledge bases or knowledge graphs (Shi et al., 2023; Xiong et al., 2024a). However, these approaches face significant limitations. Recent studies (Xiong et al., 2024a) show that RAG performance is heavily dependent on the quality and coverage of the knowledge corpus used.

**中文**

我们提出的方法在所有三个数据集（MedMCQA、MMLU_Med 和 MedQA）上始终优于基线方法 (CoT)、传统 RAG (MedRAG) 和迭代 RAG (i-MedRAG)，证明了准确性的显着提高。 2021）。传统的 RAG 方法通常从静态知识库或知识图谱中检索信息（Shi 等人，2023；Xiong 等人，2024a）。然而，这些方法面临很大的局限性。最近的研究（Xiong 等人，2024a）表明，RAG 性能在很大程度上取决于所使用的知识库的质量和覆盖范围。

### 段落 7 · Page 1

**EN**

In many instances, using RAG actually reduces accuracy because the used knowledge bases is outdated or incomplete, missing fine-grained details critical for accurate medical decision-making (Xiong et al., 2024a). In this work, we propose to tackle these challenges by utilizing search engines to enhance RAG systems. Search engines play a vital role for medical professionals, who rely on them to access clinical and medical knowledge that supports informed medical decision-making (Lykke et al., 2012).

**中文**

在许多情况下，使用 RAG 实际上会降低准确性，因为所使用的知识库已过时或不完整，缺少对准确医疗决策至关重要的细粒度细节（Xiong 等人，2024a）。在这项工作中，我们建议通过利用搜索引擎增强 RAG 系统来应对这些挑战。搜索引擎对于医疗专业人员来说发挥着至关重要的作用，他们依靠搜索引擎来获取临床和医学知识，以支持明智的医疗决策（Lykke 等，2012）。

### 段落 8 · Page 1

**EN**

By leveraging search engines, we can equip LLMs with real-time access to peer-reviewed research, clinical trial data, and up-to-date treatment protocols that are essential for effective medical decision support (Yoran et al., 2023). arXiv:2502.13233v1 [cs.CL] 18 Feb 2025

**中文**

通过利用搜索引擎，我们可以让法学硕士能够实时访问同行评审的研究、临床试验数据和最新的治疗方案，这对于有效的医疗决策支持至关重要（Yoran 等人，2023）。 arXiv:2502.13233v1 [cs.CL] 2025 年 2 月 18 日

### Page 2

### 段落 9 · Page 2

**EN**

However, directly using the original medical questions or LLM-written queries as search engine input often yields suboptimal results. This is because original medical questions typically contain redundant contextual information that can mislead the search focus. Moreover, current LLMs are not trained to align with search engines; therefore, they lack the inherent capability to generate queries optimized for search engines, which require specific structures and operators like Boolean logic and MeSH terms to function effectively (Google, 2022; Ahrefs, 2024).

**中文**

然而，直接使用原始医学问题或法学硕士编写的查询作为搜索引擎输入通常会产生次优结果。这是因为原始医学问题通常包含冗余的上下文信息，可能会误导搜索焦点。此外，目前的法学硕士没有接受过与搜索引擎保持一致的培训；因此，它们缺乏生成针对搜索引擎优化的查询的固有能力，而搜索引擎需要特定的结构和运算符（例如布尔逻辑和 MeSH 术语）才能有效发挥作用（Google，2022；Ahrefs，2024）。

### 段落 10 · Page 2

**EN**

This misalignment between the LLM-written queries and the requirements of search engines leads to the retrieval of irrelevant or low-quality information, ultimately degrading the RAG performance (Cuconasu et al., 2024). This raises a critical research question: How to help current LLMs with search engines for effective medical knowledge retrieval? To address this challenge, we propose SearchRAG, a novel retrieval-augmented generation framework that enhances the alignment between LLMs and search engines in inferencetime through synthetic query generation and uncertainty-based query selection.

**中文**

LLM 编写的查询与搜索引擎的要求之间的这种不一致会导致检索不相关或低质量的信息，最终降低 RAG 性能（Cuconasu 等人，2024）。这就提出了一个关键的研究问题：如何帮助当前的法学硕士利用搜索引擎进行有效的医学知识检索？为了应对这一挑战，我们提出了 SearchRAG，这是一种新颖的检索增强生成框架，它通过合成查询生成和基于不确定性的查询选择来增强 LLM 和搜索引擎在推理时间内的一致性。

### 段落 11 · Page 2

**EN**

Our approach first utilizes an LLM to generate a large and diverse set of search queries by repeatedly sampling with high temperature, based on the original medical question. These synthetic queries are designed to capture different aspects of the medical question in a search-engine friendly form. While not all generated queries are optimal, the diversity and scale of queries ensure that some candidates will effectively capture the clinical intent. Then, to identify the most effective queries, our framework employs an uncertainty-based selection mechanism that evaluates the knowledge snippets retrieved by each query.

**中文**

我们的方法首先利用法学硕士根据原始医学问题，通过高温重复采样来生成大量多样化的搜索查询。这些综合查询旨在以搜索引擎友好的形式捕获医学问题的不同方面。虽然并非所有生成的查询都是最佳的，但查询的多样性和规模确保了一些候选者能够有效地捕捉临床意图。然后，为了识别最有效的查询，我们的框架采用基于不确定性的选择机制来评估每个查询检索到的知识片段。

### 段落 12 · Page 2

**EN**

By measuring the LLM’s uncertainty reduction when incorporating different knowledge snippets, we retain only those that contribute the most to improving model confidence. Through extensive experiments on medical QA benchmarks (Figure 1), we demonstrate three key contributions: • Search Engine-Aligned Query Generation : We propose SearchRAG, a novel method that bridges the gap between LLM capabilities and search engine requirements through synthetic query generation, specifically optimized for medical information retrieval.

**中文**

通过测量法学硕士在合并不同知识片段时的不确定性降低程度，我们只保留那些对提高模型置信度贡献最大的知识片段。通过对医疗 QA 基准的广泛实验（图 1），我们展示了三个关键贡献： • 搜索引擎对齐的查询生成：我们提出了 SearchRAG，这是一种新颖的方法，通过合成查询生成来弥合法学硕士能力和搜索引擎要求之间的差距，专门针对医疗信息检索进行了优化。

### 段落 13 · Page 2

**EN**

• Uncertainty-Based Query Selection : We develop a selection mechanism that uses the LLM’s internal entropy to identify and prioritize the most clinically relevant information from multiple retrieval candidates. • Effective Performance Improvement: We empirically show that our framework improves the LLaMA 8B model by an average 12.61% compared to baseline methods in answer accuracy in medical QA tasks.

**中文**

• 基于不确定性的查询选择：我们开发了一种选择机制，使用法学硕士的内部熵来识别多个检索候选者中最临床相关的信息并对其进行优先级排序。 • 有效的性能改进：我们的经验表明，与基线方法相比，我们的框架在医疗 QA 任务中的答案准确性平均提高了 LLaMA 8B 模型 12.61%。

### 段落 14 · Page 2

**EN**

The paper is structured as follows: Section 2 details our dual-component architecture for query generation and knowledge selection, Section 3 presents comparative evaluations across multiple medical benchmarks, Section 4 discusses related work, and Section 5 concludes our paper. 2 Methodology In this section, we introduce SearchRAG, an innovative RAG framework aimed at enhancing LLMs’ ability to effectively use search engines for knowledge retrieval, especially when addressing complex and specialized medical questions.

**中文**

本文的结构如下：第 2 部分详细介绍了我们用于查询生成和知识选择的双组件架构，第 3 部分介绍了多个医学基准的比较评估，第 4 部分讨论了相关工作，第 5 部分总结了我们的论文。 2 方法论 在本节中，我们介绍 SearchRAG，这是一种创新的 RAG 框架，旨在增强法学硕士有效使用搜索引擎进行知识检索的能力，特别是在解决复杂且专业的医学问题时。

### 段落 15 · Page 2

**EN**

2.1 Problem Formulation and Overview Retrieval-Augmented Generation (RAG) integrates external knowledge into the input of LLMs to enhance their responses (Guu et al., 2020; Wang et al., 2021). Formally, given an input prompt x, RAG retrieves a set of knowledge snippets K = {K1, K2, . . . ,Kn} using a retrieval function fret: K = fret(x), and generates a response y using model fLLM conditioned on both the input and the retrieved knowledge: y = fLLM(x, K). (1) However, when dealing with complex and verbose medical questions, such as the one shown in Figure 2, directly using x for retrieval can lead to suboptimal results.

**中文**

2.1 问题表述和概述检索增强生成（RAG）将外部知识整合到法学硕士的输入中，以增强他们的反应（Guu 等，2020；Wang 等，2021）。形式上，给定输入提示 x，RAG 检索一组知识片段 K = {K1, K2, .。。 ,Kn} 使用检索函数 fret：K = fret(x)，并使用以输入和检索知识为条件的模型 fLLM 生成响应 y：y = fLLM(x, K)。 (1) 然而，在处理复杂而冗长的医学问题时，如图2所示，直接使用x进行检索可能会导致结果不理想。

### 段落 16 · Page 2

**EN**

This is because such questions often include extraneous details that can mislead search engines and result in the retrieval of irrelevant information (Jin et al., 2020; Shi et al., 2023; Xiong et al., 2024a). To overcome these limitations, our proposed SearchRAG modifies the RAG framework by introducing two key components: • A Synthetic Query Generation Module that generates candidate queries by transforming original questions into search-engine-friendly form.

**中文**

这是因为此类问题通常包含无关的细节，可能会误导搜索引擎并导致检索到不相关的信息（Jin et al., 2020; Shi et al., 2023; Xiong et al., 2024a）。为了克服这些限制，我们提出的SearchRAG 通过引入两个关键组件来修改RAG 框架： • 综合查询生成模块，通过将原始问题转换为搜索引擎友好的形式来生成候选查询。

### Page 3

### 段落 17 · Page 3

**EN**

A 67-year-old man with bladder cancer reports a 2-day history of ear ringing after starting neoadjuvant chemotherapy a week ago. Pure tone audiometry reveals a 45 dB sensorineural hearing loss. The drug causing this is most likely due to which mechanism? Original Question 1. Synthetic Query Generation 2. Query Evaluation Query-writing LLMWhat is the mechanism 3.

**中文**

一名患有膀胱癌的 67 岁男性报告，一周前开始新辅助化疗后有 2 天耳鸣史。纯音测听显示感音神经性听力损失为 45 分贝。导致这种情况的药物最有可能是由于哪种机制造成的？原题 1. 综合查询生成 2. 查询评估 查询编写 LLM 机制是什么 3.

### 段落 18 · Page 3

**EN**

Retrieval Augmented Generation 𝒦𝑗 𝒦𝑖 query 1 Search the Web 𝑓SE snippet 1 query 2 snippet 2 query n snippet n 𝑓LLM Evaluator LLM 𝑓LLM 𝑞1 𝑞2 𝑞𝑛 𝒦1 𝒦2 𝒦𝑛 High Confidence Low Confidence 𝒦𝑖 Discard 𝒦𝑗 Keep 𝑥 Answer LLM 𝑓LLM 𝑥 𝑥 … … … 𝒦𝑗2 𝒦𝑗1 Final Answers … … Figure 2: Overview of SearchRAG: Our framework first transforms complex medical questions into searchoptimized synthetic queries through repeated sampling. The retrieved knowledge snippets are then filtered using uncertainty-based selection to identify the most relevant information for enhancing LLM responses.

**中文**

检索增强生成 𝒦𝑗 𝒦𝑖 查询 1 搜索网络 𝑓SE 片段 1 查询 2 片段 2 查询 n 片段 n 𝑓LLM 评估器 LLM 𝑓LLM 𝑞1 𝑞2 𝑞𝑛 𝒦1 𝒦2 𝒦𝑛 高置信度低置信度 𝒦𝑖 丢弃 𝒦𝑗 保留 𝑥 回答 LLM 𝑓LLM 𝑥 𝑥 … … … 𝒦𝑗2 𝒦𝑗1 最终答案 … … 图 2：SearchRAG 概述：我们的框架首先通过重复采样将复杂的医学问题转化为搜索优化的综合查询。然后使用基于不确定性的选择对检索到的知识片段进行过滤，以识别最相关的信息，以增强法学硕士的反应。

### 段落 19 · Page 3

**EN**

• An Uncertainty-Based Query Selection mechanism that leverages the LLM’s internal uncertainty to select the most informative knowledge snippets. By integrating these components, we enhance the retrieval of pertinent information to answer questions, ultimately improving response accuracy and relevance. 2.2 Synthetic Query Generation Module Medical questions are often too complex to be directly used as search engine queries. To address this challenge, SearchRAG proposes to use synthetic queries generated by LLMs to improve the retrieval of knowledge pertinent to answering the original question.

**中文**

• 基于不确定性的查询选择机制，利用法学硕士的内部不确定性来选择信息最丰富的知识片段。通过集成这些组件，我们增强了对回答问题的相关信息的检索，最终提高了响应的准确性和相关性。 2.2 综合查询生成模块医学问题通常过于复杂而无法直接用作搜索引擎查询。为了应对这一挑战，SearchRAG 建议使用法学硕士生成的合成查询来改进与回答原始问题相关的知识的检索。

### 段落 20 · Page 3

**EN**

The need for synthetic queries stems from two fundamental challenges in medical question answering: • Complexity of Medical Questions : Medical questions often contain specialized terminology and multi-hop clinical logic (Jin et al., 2020). A single condition may be referred to by different medical terms (e.g., "myocardial infarction" and "heart attack"), making it challenging to match relevant content comprehensively. Additionally, critical retrieval keywords may not appear explicitly in the original question, which hinders effective retrieval.

**中文**

对综合查询的需求源于医学问答中的两个基本挑战： • 医学问题的复杂性：医学问题通常包含专业术语和多跳临床逻辑（Jin 等人，2020）。单一病症可能由不同的医学术语（例如“心肌梗塞”和“心脏病发作”）来指代，这使得全面匹配相关内容具有挑战性。此外，关键检索关键词可能不会明确出现在原始问题中，这阻碍了有效检索。

### 段落 21 · Page 3

**EN**

• Constraints of Search Engine: Existing search engines employ algorithms and ranking systems that favor well-structured, concise queries with clear intent (Google, 2022). Medical questions usually fail to meet these requirements, thus preventing the retrieval of relevant medical content. Our solution leverages the same LLM we aim to enhance through RAG to generate synthetic queries, eliminating the need for additional models. We design a specialized prompt template p (detailed in the Appendix) that guides the LLM to decompose and transform the original medical question into search queries.

**中文**

• 搜索引擎的限制：现有搜索引擎采用的算法和排名系统有利于结构良好、意图明确的简洁查询（Google，2022）。医学问题通常无法满足这些要求，从而阻碍了相关医学内容的检索。我们的解决方案利用了我们旨在通过 RAG 增强的相同 LLM 来生成综合查询，从而无需额外的模型。我们设计了一个专门的提示模板p（详见附录），指导LLM将原始医学问题分解并转化为搜索查询。

### 段落 22 · Page 3

**EN**

More specifically, the LLM first analyzes the medical question to extract key clinical entities, reformulates them using standardized medical terminology, and finally structures the queries with search-friendly syntax. Given an original prompt x and our template p, we generate a set of synthetic queries through repeated sampling: {q1, q2, . . . , qm} = m[ i=1 fLLM(x, p). (2) Here, we employ a high-temperature sampling strategy to generate a large and diverse set of candidate queries {q1, q2, . . . , qm}.

**中文**

更具体地说，法学硕士首先分析医学问题以提取关键临床实体，使用标准化医学术语重新表述它们，最后使用搜索友好的语法构建查询。给定原始提示 x 和模板 p，我们通过重复采样生成一组合成查询：{q1, q2,...。。 , qm} = m[ i=1 fLLM(x, p)。 (2) 在这里，我们采用高温采样策略来生成大量且多样化的候选查询集 {q1, q2,...。。，qm}。

### 段落 23 · Page 3

**EN**

Example queries for a question x are shown in Figure 2 with {q1:“ototoxic effects of platinum-based drugs"; q2: “mechanisms cisplatin hearing loss" ; q3: “Proteasome inhibitor drug effects on inner ear" }. These queries contain concise keywords suitable for search engines and cover multiple aspects of question x. Among them, q2 is the most informative one1. We provide more details in Section 3.3.3 1A Google search for q2 returns: “...cisplatin is retained for months to years. It can cause DNA damage, inhibit protein synthesis...", which corresponds to the correct answer:“Crosslinking of DNA".

**中文**

问题 x 的查询示例如图 2 所示，其中 {q1:“铂类药物的耳毒性作用”; q2：“顺铂听力损失的机制”； q3：“蛋白酶体抑制剂药物对内耳的影响”}。这些查询包含适合搜索引擎的简洁关键字，涵盖问题x的多个方面。其中，q2 是信息量最大的一个1。我们在第 3.3.3 1A 节中提供了更多详细信息，Google 搜索 q2 返回：“...顺铂保留数月至数年。它会导致 DNA 损伤，抑制蛋白质合成...”，这对应于正确答案：“DNA 交联”。

### 段落 24 · Page 3

**EN**

Though not mentioned in the original question, cisplatin is a well-known chemotherapy drug.

**中文**

尽管在最初的问题中没有提到，顺铂是一种众所周知的化疗药物。

### Page 4

### 段落 25 · Page 4

**EN**

and more query examples in Appendix. Our strategy is inspired by inference-time scaling law (Brown et al., 2024): while not every query can retrieve optimal information, some candidates will be more effective than others at retrieving useful knowledge. The expanded candidate pool increases the probability of obtaining high-quality knowledge snippets. To fully leverage this variability, our subsequent uncertainty-based selection mechanism (detailed in the next section) will identify and utilize the most effective ones.

**中文**

以及附录中的更多查询示例。我们的策略受到推理时间缩放定律的启发（Brown 等人，2024）：虽然并非每个查询都可以检索最佳信息，但某些候选者在检索有用知识方面会比其他候选者更有效。扩大的候选池增加了获得高质量知识片段的概率。为了充分利用这种可变性，我们随后基于不确定性的选择机制（将在下一节中详细介绍）将识别并利用最有效的选择机制。

### 段落 26 · Page 4

**EN**

2.3 Align Search Engines to LLMs via Uncertainty-Based Query Selection While we generate a large number of synthetic queries, identifying the most effective ones is a non-trivial task. To address this, we propose to leverage the LLM’s internal uncertainty as a reward signal to guide query selection. Specifically, we assess the uncertainty reduction associated with each retrieved snippet, treating it as a measure of information gain (Shi et al., 2024). Queries that retrieve knowledge leading to greater uncertainty reduction are prioritized, ensuring that only the most informative snippets contribute to RAG.

**中文**

2.3 通过基于不确定性的查询选择使搜索引擎与法学硕士保持一致 虽然我们生成了大量的综合查询，但识别最有效的查询却是一项艰巨的任务。为了解决这个问题，我们建议利用法学硕士的内部不确定性作为奖励信号来指导查询选择。具体来说，我们评估与每个检索到的片段相关的不确定性减少，将其视为信息增益的衡量标准（Shi et al., 2024）。检索知识从而更大程度地减少不确定性的查询会被优先考虑，确保只有信息最丰富的片段才会对 RAG 做出贡献。

### 段落 27 · Page 4

**EN**

Our approach aims to align search engine to LLMs by helping LLMs effectively use web search to retrieve knowledge to answer given questions. By using uncertainty as a reward, our system selects queries that maximize knowledge utility, refining the alignment process on a per-query basis. Unlike tuning-based alignment (Ma et al., 2023), our method optimizes in inference-time without modifying model parameters, making it robust to diverse retrieval sources and evolving topics. For each query qi, our search engine function fSE retrieves structured knowledge snippets: Ki = fSE(qi), i = 1, 2, . . . , m.

**中文**

我们的方法旨在通过帮助法学硕士有效地使用网络搜索来检索知识来回答给定的问题，从而使搜索引擎与法学硕士保持一致。通过使用不确定性作为奖励，我们的系统选择最大化知识效用的查询，并在每个查询的基础上完善对齐过程。与基于调整的对齐（Ma et al., 2023）不同，我们的方法在推理时间上进行优化，而不修改模型参数，使其对不同的检索源和不断发展的主题具有鲁棒性。对于每个查询 qi，我们的搜索引擎函数 fSE 都会检索结构化知识片段：Ki = fSE(qi), i = 1, 2,...。。。，米。

### 段落 28 · Page 4

**EN**

(3) The retrieved snippets are concise extracts from search engine results, including titles and short descriptions for each webpage. We provide a case study of the search engine results in the Appendix. Each retrieved snippet augments the original prompt through concatenation: x′ i = [x; Ki]. We estimate the LLM’s uncertainty in generating responses based on these augmented inputs using Shannon entropy (Cover, 1999). Let Y be the random variable representing possible responses y generated by LLMs.

**中文**

(3) 检索到的片段是从搜索引擎结果中简洁摘录的，包括每个网页的标题和简短描述。我们在附录中提供了搜索引擎结果的案例研究。每个检索到的片段都通过串联增强了原始提示：x′ i = [x;基]。我们使用香农熵（Cover，1999）估计了法学硕士在根据这些增强输入生成响应时的不确定性。令 Y 为代表 LLM 生成的可能响应 y 的随机变量。

### 段落 29 · Page 4

**EN**

Since computing the full response distribution is infeasible (Shi et al., 2024; Cover, 1999), we approximate uncertainty using the entropy of the first token, defined as: H(Y | X) = − X w∈V p(w | X) log2 p(w | X), (4) where p(w | X) is the probability of generating token w as the first token across the vocabulary V. This approximation is suitable because medical questions are formulated as multiple-choice questions in our setting. We prompt the model to directly output option labels (ABCD) as the first token.

**中文**

由于计算完整响应分布是不可行的（Shi et al., 2024；Cover, 1999），我们使用第一个标记的熵来近似不确定性，定义为： H(Y | X) = − X w∈V p(w | X) log2 p(w | X), (4) 其中 p(w | X) 是生成标记 w 作为词汇表 V 中第一个标记的概率。这种近似是合适的，因为医学问题被表述为多项选择我们环境中的问题。我们提示模型直接输出选项标签（ABCD）作为第一个标记。

### 段落 30 · Page 4

**EN**

Thus, the first token entropy directly reflects the model’s confidence in different answer choices, making this uncertainty approximation both computationally efficient and semantically meaningful for our task. For each knowledge snippet, we compute the reduction in conditional entropy: ∆Hi = H(Y | x)| {z } Original uncertainty − H(Y | x′ i)| {z } Post-retrieval uncertainty . (5) A positive value of ∆Hi indicates that the knowledge snippet Ki has reduced the model uncertainty. The most informative snippets are aggregated into a final knowledge set: K∗ = [ {Ki | ∆Hi > 0} .

**中文**

因此，第一个令牌熵直接反映了模型对不同答案选择的置信度，使得这种不确定性近似对于我们的任务来说既具有计算效率又具有语义意义。对于每个知识片段，我们计算条件熵的减少： ΔHi = H(Y | x)| {z } 原始不确定性 − H(Y | x′ i)| {z} 检索后的不确定性。 (5) ΔHi 为正值表明知识片段 Ki 降低了模型的不确定性。信息最丰富的片段被聚合成最终的知识集：K* = [ {Ki | ΔHi > 0}。

### 段落 31 · Page 4

**EN**

(6) This inference-time alignment leverages the model internal states to ensure that only the knowledge snippets capable of increasing prediction certainty are used for the final generation. 2.4 Integration into the RAG Framework The complete integration of SearchRAG’s components into the RAG framework operates as Algorithm 1. The framework begins by generating diverse search queries through repeated sampling from the LLM (line 3). Next, each query is input into a search engine to retrieve knowledge (line 5).

**中文**

(6) 这种推理时间对齐利用模型内部状态来确保只有能够提高预测确定性的知识片段才会用于最终生成。 2.4 集成到 RAG 框架中 将 SearchRAG 组件完全集成到 RAG 框架中的操作方式如算法 1 所示。该框架首先通过 LLM 的重复采样生成不同的搜索查询（第 3 行）。接下来，每个查询都被输入到搜索引擎中以检索知识（第 5 行）。

### 段落 32 · Page 4

**EN**

The system then evaluates the retrieved content by measuring how effectively each snippet reduces the model’s prediction uncertainty (line 6). Finally, confidence-filtered knowledge is aggregated for the final answer generation (lines 8, 9), ensuring that only clinically relevant information is utilized to assist the diagnosis.

**中文**

然后，系统通过测量每个片段降低模型预测不确定性的效果来评估检索到的内容（第 6 行）。最后，经过置信过滤的知识被聚合以生成最终答案（第 8、9 行），确保仅利用临床相关信息来辅助诊断。

### Page 5

### 段落 33 · Page 5

**EN**

Table 1: Comparison of knowledge source characteristics. Source Data V olume Source Diversity External Space Use External Memory Use Textbooks (Jin et al., 2021) × × △ △ PubMed (Gao et al., 2020) △ △ × × Search Engine (Google, 2025) ✓ ✓ ✓ ✓ ✓: Strong capability △: Moderate capability ×: Weak capability Algorithm 1 SearchRAG 1: Input: Original question x 2: Output: Response y 3: {q1, . . . , qm} ← fLLM(x, p) ▷ Synthetic query generation 4: for i ∈ {1, . . .

**中文**

表1：知识源特征比较。源数据量 来源多样性 外部空间使用 外部存储器使用 教科书 (Jin et al., 2021) × × △ △ PubMed (Gao et al., 2020) △ △ × × 搜索引擎 (Google, 2025) ✓ ✓ ✓ ✓ ✓：能力强 △：能力一般 ×：能力弱 算法 1 SearchRAG 1： 输入：原始问题 x 2：输出：响应 y 3: {q1, .。。 , qm} ← fLLM(x, p) ▷ 合成查询生成 4： for i ∈ {1, .。。

### 段落 34 · Page 5

**EN**

, m} do 5: Ki ← fSE(qi) ▷ Search engine retrieval 6: ∆Hi ← H(Y |X = x) − H(Y |X = [x; Ki]) ▷ Uncertainty reduction 7: end for 8: K∗ ← S {Ki | ∆Hi > 0} ▷ Knowledge selection 9: y ← fLLM(x, K∗) 10: return y 3 Experiments Our experimental evaluation addresses three key research questions (RQs): RQ1: How does SearchRAG perform compared to existing methods on medical QA tasks? RQ2: How effective is our uncertainty-based knowledge selection strategy in improving performance? RQ3: How does scaling the number of synthetic queries affect the model’s performance?

**中文**

, m} do 5: Ki ← fSE(qi) ▷ 搜索引擎检索 6: ΔHi ← H(Y |X = x) − H(Y |X = [x; Ki]) ▷ 不确定性降低 7: 8 结束：K* ← S {Ki | ΔHi > 0} ▷ 知识选择 9: y ← fLLM(x, K*) 10: return y 3 实验 我们的实验评估解决了三个关键研究问题 (RQ)： RQ1：与现有方法相比，SearchRAG 在医学 QA 任务上的表现如何？ RQ2：我们基于不确定性的知识选择策略在提高绩效方面效果如何？ RQ3：扩展合成查询的数量如何影响模型的性能？

### 段落 35 · Page 5

**EN**

We evaluate through comparative benchmarks on medical datasets, focusing on quantitative performance metrics and qualitative analysis of retrieved knowledge. 3.1 Experimental Settings We evaluate our approach against four baseline methods: one non-RAG method and three RAGbased methods. The non-RAG baseline is Chainof-Thought (CoT) prompting (Wei et al., 2022). For RAG-based methods, we compare against: MedRAG using textbooks as the knowledge source with MedCPT retriever, MedRAG using PubMed as the knowledge source with MedCPT retriever, and i-MedRAG using textbooks as the knowledge source with MedCPT retriever (Xiong et al., 2024a,b).

**中文**

我们通过医疗数据集的比较基准进行评估，重点关注定量性能指标和检索到的知识的定性分析。 3.1 实验设置 我们根据四种基线方法评估我们的方法：一种非 RAG 方法和三种基于 RAG 的方法。非 RAG 基线是 Chainof-Thought (CoT) 提示（Wei 等人，2022）。对于基于RAG的方法，我们比较了：使用教科书作为知识源的MedRAG和MedCPT检索器，使用PubMed作为知识源的MedRAG和MedCPT检索器，以及使用教科书作为知识源和MedCPT检索器的i-MedRAG（Xiong等人，2024a，b）。

### 段落 36 · Page 5

**EN**

A comparison of the different knowledge sources is shown in Table 1. Additional implementation details, including hyperparameter choices, can be found in the Appendix. We evaluate these methods on three datasets designed for medical question answering: MedQA (Jin et al., 2021), MMLU_Med (Hendrycks et al., 2020), and MedMCQA (Pal et al., 2022). MedQA consists of real-world medical licensing exam questions, MMLU_Med is a specialized subset of a larger multi-domain challenge focusing on medical topics, and MedMCQA contains multiple-choice medical questions that require domain-specific reasoning.

**中文**

表 1 显示了不同知识源的比较。其他实现细节（包括超参数选择）可以在附录中找到。我们在专为医学问答设计的三个数据集上评估这些方法：MedQA（Jin 等人，2021）、MMLU_Med（Hendrycks 等人，2020）和 MedMCQA（Pal 等人，2022）。 MedQA 由现实世界的医疗许可考试问题组成，MMLU_Med 是专注于医学主题的较大多领域挑战的专门子集，MedMCQA 包含需要特定领域推理的多项选择医学问题。

### 段落 37 · Page 5

**EN**

We follow the evaluation protocols established by MedRAG and i-MedRAG (Xiong et al., 2024a,b). For the LLMs, we experiment with two instruction-tuned variants of LLaMA 3.1, specifically the 8B and 70B parameter versions (Dubey et al., 2024). We utilize Google Search 2 as our search engine provider. For the 70B model, we employ INT4 quantization to reduce memory requirements while maintaining performance. All variants are utilized without additional fine-tuning for any baseline approach. All inference procedures are carried out on A6000 GPUs. Additional experiment details will be provided in the Appendix.

**中文**

我们遵循 MedRAG 和 i-MedRAG 制定的评估方案（Xiong 等人，2024a，b）。对于法学硕士，我们尝试了 LLaMA 3.1 的两种指令调整变体，特别是 8B 和 70B 参数版本（Dubey 等人，2024）。我们使用 Google Search 2 作为我们的搜索引擎提供商。对于 70B 模型，我们采用 INT4 量化来减少内存需求，同时保持性能。所有变体的使用都无需对任何基线方法进行额外的微调。所有推理过程均在 A6000 GPU 上执行。其他实验细节将在附录中提供。

### 段落 38 · Page 5

**EN**

3.2 RQ1: Main Results Table 2 demonstrates the effectiveness of SearchRAG across model scales and medical QA datasets. We have four findings: First, conventional RAG approaches exhibit critical sensitivity to knowledge source selection, particularly in smaller models. Our experiments reveal that PubMed-based retrieval degrades 8B model performance by 9.11% on MedMCQA compared to chain-of-thought baselines, while textbook-based retrieval provides only marginal gains (+0.62% on MMLU_Med).

**中文**

3.2 RQ1：主要结果 表 2 展示了 SearchRAG 在模型规模和医学 QA 数据集上的有效性。我们有四个发现：首先，传统的 RAG 方法对知识源选择表现出至关重要的敏感性，特别是在较小的模型中。我们的实验表明，与思想链基线相比，基于 PubMed 的检索使 MedMCQA 上的 8B 模型性能降低了 9.11%，而基于教科书的检索仅提供了边际增益（在 MMLU_Med 上+0.62%）。

### 段落 39 · Page 5

**EN**

This validates our core hypothesis that static knowledge bases struggle to provide reliable augmentation, as noted in our analysis of 2Third-party search API provider. Retrieved search snippets are used as relevant knowledge for RAG augmentation. https://serper.dev/

**中文**

这验证了我们的核心假设，即静态知识库难以提供可靠的增强，正如我们在对 2 第三方搜索 API 提供商的分析中所指出的那样。检索到的搜索片段用作 RAG 增强的相关知识。 https://serper.dev/

### Page 6

### 段落 40 · Page 6

**EN**

Table 2: Performance comparison of different methods on medical QA datasets.

**中文**

表 2：不同方法在医学 QA 数据集上的性能比较。

### 段落 41 · Page 6

**EN**

MedMCQA MMLU_Med MedQA Method Accuracy Improve Accuracy Improve Accuracy Improve LLaMA 3.1-8B CoT 55.96 - 74.52 - 65.91 - MedRAG (Textbooks) 55.89 -0.13% 74.98 0.62% 64.89 -1.55% MedRAG (PubMed) 50.87 -9.11% 71.28 -4.32% 60.41 -8.48% i-MedRAG 56.80 +1.65% 74.70 +0.25% 68.97 +5.07% Our RAG 65.14 +16.16% 84.67 +13.59% 71.49 +8.09 % LLaMA 3.1-70B CoT 69.33 - 87.53 - 78.08 - MedRAG (Textbooks) 69.23 -0.14% 86.33 -1.37% 79.34 +1.61% MedRAG (PubMed) 69.95 +0.90% 86.80 -0.85% 79.26 +1.49% i-MedRAG 69.23 -0.14% 87.17 -0.41% 79.58 +1.89% Our RAG 74.40 +7.32% 90.95 +3.92% 83.34 +6.61% search engine alignment challenges (Section 2.1).

**中文**

MedMCQA MMLU_Med MedQA 方法准确度 提高准确度 提高准确度 提高 LLaMA 3.1-8B CoT 55.96 - 74.52 - 65.91 - MedRAG (教科书) 55.89 -0.13% 74.98 0.62% 64.89 -1.55% MedRAG (PubMed) 50.87 -9.11% 71.28 -4.32% 60.41 -8.48% i-MedRAG 56.80 +1.65% 74.70 +0.25% 68.97 +5.07% 我们的 RAG 65.14 +16.16% 84.67 +13.59% 71.49 +8.09 % LLaMA 3.1-70B CoT 69.33 - 87.53 - 78.08 - MedRAG（教科书） 69.23 -0.14% 86.33 -1.37% 79.34 +1.61% MedRAG（PubMed） 69.95 +0.90% 86.80 -0.85% 79.26 +1.49% i-MedRAG 69.23 -0.14% 87.17 -0.41% 79.58 +1.89% 我们的 RAG 74.40 +7.32% 90.95 +3.92% 83.34 +6.61% 搜索引擎对齐挑战（第 2.1 节）。

### 段落 42 · Page 6

**EN**

Second, our dual-component architecture enables consistent and substantial performance improvements across all datasets and model scales. The 8B model with SearchRAG achieves absolute accuracy gains of +16.16% on MedMCQA, +13.59% on MMLU_Med, and +8.09% on MedQA compared to chain-of-thought baselines, significantly outperforming i-MedRAG’s maximum gain of +5.07% on MedQA. This performance advantage stems from our method’s unique combination of search-optimized query generation and uncertainty filtering.

**中文**

其次，我们的双组件架构可以在所有数据集和模型规模上实现一致且显着的性能改进。与思想链基线相比，采用 SearchRAG 的 8B 模型在 MedMCQA 上的绝对准确度增益为 +16.16%，在 MMLU_Med 上为 +13.59%，在 MedQA 上为 +8.09%，显着优于 i-MedRAG 在 MedQA 上的最大增益 +5.07%。这种性能优势源于我们的方法将搜索优化的查询生成和不确定性过滤的独特组合。

### 段落 43 · Page 6

**EN**

Moreover, our synthetic queries enable better handling of complex clinical reasoning, particularly evident in MedMCQA where questions require synthesizing multiple medical concepts. Third, the uncertainty-based filtering mechanism demonstrates model-agnostic effectiveness. Despite the 70B model’s stronger baseline performance (69.33% MedMCQA vs 55.96% for 8B), SearchRAG still delivers substantial gains of +7.32% on MedMCQA and +6.61% on MedQA. This confirms our theoretical framework’s scalability, rather than being subsumed by model capacity increases, our knowledge selection mechanism can continually provide complementary knowledge.

**中文**

此外，我们的综合查询能够更好地处理复杂的临床推理，在 MedMCQA 中尤其明显，其中问题需要综合多个医学概念。第三，基于不确定性的过滤机制证明了模型不可知的有效性。尽管 70B 模型的基线性能更强（MedMCQA 为 69.33%，8B 为 55.96%），SearchRAG 仍然在 MedMCQA 上实现了 +7.32% 的大幅提升，在 MedQA 上实现了 +6.61% 的大幅提升。这证实了我们的理论框架的可扩展性，我们的知识选择机制可以不断提供补充知识，而不是被模型容量的增加所包含。

### 段落 44 · Page 6

**EN**

Finally, our method shows relatively modest gains with the smaller model on MedQA (+8.09% for 8B), which often demands more intricate clinical reasoning. This discrepancy indicates that our method is particularly effective in situations where the primary limitation is the need for precise factual knowledge, rather than the ability to navigate complex reasoning chains. In summary, these results empirically validate SearchRAG’s two-stage alignment process. The significant improvements demonstrate effective search engine query optimization, while the consistent gains across model scales confirm the uncertainty filtering’s generalizability.

**中文**

最后，我们的方法在 MedQA 上显示较小模型的收益相对适度（8B 为 +8.09%），这通常需要更复杂的临床推理。这种差异表明，在主要限制是需要精确的事实知识而不是导航复杂推理链的能力的情况下，我们的方法特别有效。总之，这些结果从经验上验证了 SearchRAG 的两阶段对齐过程。显着的改进证明了有效的搜索引擎查询优化，而跨模型规模的一致增益证实了不确定性过滤的普遍性。

### 段落 45 · Page 6

**EN**

3.3 Ablation Studies 3.3.1 RQ2: Effectiveness of Knowledge Selection To validate our uncertainty-based knowledge selection mechanism, we conduct experiments on 350 randomly sampled instances from each dataset using both model variants. Contrary to the intuition that unfiltered knowledge provides richer context, Table 3 reveals that selective filtering consistently improves performance, particularly for smaller models.

**中文**

3.3 消融研究 3.3.1 RQ2：知识选择的有效性 为了验证我们基于不确定性的知识选择机制，我们使用两种模型变体对每个数据集中的 350 个随机采样实例进行实验。与未经过滤的知识提供更丰富上下文的直觉相反，表 3 表明选择性过滤持续提高性能，特别是对于较小的模型。

### 段落 46 · Page 6

**EN**

There are two key insights as follows: (1) The LLaMA 8B model shows 4-7% absolute gains across all datasets, indicating smaller models’ vulnerability to irrelevant information: unfiltered knowledge introduces distracting noise that misleads reasoning. (2) While the LLaMA 70B model exhibits more robustness, it still benefits from filtering, suggesting even powerful models cannot fully compensate for low-quality context.

**中文**

有两个关键见解如下：(1) LLaMA 8B 模型在所有数据集上显示出 4-7% 的绝对增益，这表明较小的模型容易受到不相关信息的影响：未经过滤的知识会引入分散注意力的噪声，从而误导推理。 (2) 虽然 LLaMA 70B 模型表现出更强的鲁棒性，但它仍然受益于过滤，这表明即使是强大的模型也无法完全补偿低质量的上下文。

### 段落 47 · Page 6

**EN**

This demonstrates the effectiveness of our uncertainty-based selection mechanism: By selectively presenting only the most relevant information, we help models avoid distraction from excessive content while maintaining useful knowledge signals.

**中文**

这证明了我们基于不确定性的选择机制的有效性：通过有选择地仅呈现最相关的信息，我们帮助模型避免过多内容的干扰，同时保持有用的知识信号。

### Page 7

### 段落 48 · Page 7

**EN**

Table 3: Performance comparison with/without knowledge filtering across model scales and datasets. MedMCQA MMLU_Med MedQA Model Unfiltered Filtered Unfiltered Filtered Unfiltered Filtered 8B 60.57 64.86 (+7.08%) 81.14 84.86 (+4.58%) 67.71 72.29 (+6.76%) 70B 70.86 74.57 (+5.24%) 88.29 89.71 (+1.61%) 82.57 83.43 (+1.04%) 3.3.2 RQ3: Impact of the Number of Total Generated Queries We conducted an evaluation to understand how the number of generated queries affects model performance, using 350 randomly sampled instances. The configurations tested included using 0 (the original question), 4, 16, and 32 generated queries.

**中文**

表 3：跨模型规模和数据集有/没有知识过滤的性能比较。 MedMCQA MMLU_Med MedQA 模型 未过滤 已过滤 未过滤 已过滤 未过滤 已过滤 8B 60.57 64.86 (+7.08%) 81.14 84.86 (+4.58%) 67.71 72.29 (+6.76%) 70B 70.86 74.57 (+5.24%) 88.29 89.71 (+1.61%) 82.57 83.43 (+1.04%) 3.3.2 RQ3：生成的查询总数的影响 我们使用 350 个随机采样的实例进行了评估，以了解生成的查询数量如何影响模型性能。测试的配置包括使用 0 个（原始问题）、4 个、16 个和 32 个生成的查询。

### 段落 49 · Page 7

**EN**

Figure 3 illustrates the impact of varying the number of queries on performance. Our analysis reveals two key findings: First, using only the original questions (0 query) resulted in limited RAG effectiveness, with performance even degrading compared to the non-RAG baseline, achieving only 62.9% on the MedQA. This suggests unmodified medical questions fail to effectively leverage search engines for retrieving relevant information, and the low performance confirms that these medical questions do not have direct matches in existing online knowledge sources. Second, introducing synthetic query generation led to improvements across all datasets.

**中文**

图 3 说明了不同查询数量对性能的影响。我们的分析揭示了两个关键发现：首先，仅使用原始问题（0 个查询）导致 RAG 有效性有限，与非 RAG 基线相比，性能甚至下降，在 MedQA 上仅达到 62.9%。这表明未经修改的医学问题无法有效地利用搜索引擎来检索相关信息，并且低性能证实这些医学问题在现有的在线知识源中没有直接匹配。其次，引入综合查询生成导致所有数据集的改进。

### 段落 50 · Page 7

**EN**

Performance scaled with the number of generated queries, peaking with 32 queries. This clear correlation between query count and accuracy indicates that a larger query set helps capture more diverse and relevant knowledge to enhance the RAG process. 3.3.3 Case Study This case study demonstrates how SearchRAG handles a clinical question about oral contraceptive effects. The scenario involves a 17-year-old patient prescribed contraceptive pills, examining which condition’s risk is decreased by this medication.

**中文**

性能随着生成的查询数量而变化，在 32 个查询时达到峰值。查询计数和准确性之间的这种明显相关性表明，更大的查询集有助于捕获更多样化和相关的知识，从而增强 RAG 流程。 3.3.3 案例研究 该案例研究展示了SearchRAG 如何处理有关口服避孕药效果的临床问题。该场景涉及一名 17 岁的患者服用避孕药，检查该药物可降低哪种疾病的风险。

### 段落 51 · Page 7

**EN**

Through high-temperature sampling, the model generates diverse search queries, retrieving evidence that oral contraceptives reduce ovarian cancer risk while increasing risks for cervical and breast cancers (See Facts [1][2][7]). While the system initially incorrectly suggested cervical cancer as having reduced risk, the retrieved facts enabled the model to correct its response to ovarian cancer. This case shows how SearchRAG’s query generation and knowledge selection can transform an incorrect initial assessment into an accurate, evidence-based conclusion. More cases are provided in Appendix.

**中文**

通过高温采样，该模型生成不同的搜索查询，检索口服避孕药降低卵巢癌风险同时增加宫颈癌和乳腺癌风险的证据（参见事实 [1][2][7]）。虽然系统最初错误地认为宫颈癌风险降低，但检索到的事实使模型能够纠正其对卵巢癌的反应。此案例展示了 SearchRAG 的查询生成和知识选择如何将不正确的初始评估转化为准确的、基于证据的结论。附录中提供了更多案例。

### 段落 52 · Page 7

**EN**

Case Study 1: Question: A 17-year-old girl comes to the physician because of an 8-month history of severe acne vulgaris over her face, upper back, arms, and buttocks. Treatment with oral antibiotics and topical combination therapy with benzoyl peroxide and retinoid has not completely resolved her symptoms. Examination shows oily skin with numerous comedones, pustules, and scarring over the face and upper back. Long-term therapy is started with combined oral contraceptive pills. This medication decreases the patient’s risk developing of which of the following conditions?

**中文**

案例研究 1：问题：一名 17 岁女孩因面部、上背部、手臂和臀部有 8 个月的严重寻常痤疮病史而去看医生。口服抗生素以及过氧化苯甲酰和类维生素A的局部联合治疗尚未完全缓解她的症状。检查显示油性皮肤，面部和上背部有大量粉刺、脓疱和疤痕。长期治疗从联合口服避孕药开始。这种药物可以降低患者患以下哪种疾病的风险？

### 段落 53 · Page 7

**EN**

Choices: [A.] Hypertension, [B.] Ovarian cancer, [C.] Cervical cancer, [D.] Breast cancer Ground Truth: B (Ovarian cancer) Synthetic Queries: [1] ’oral contraception use reducing ovarian cancer risk’, [2] ’risk of hormonal cancers contraceptive pills’, [3] ’Oral contraceptive pill preventive effects on cancer’, [4] ’Carcinogenic effects of estrogen therapy’, [5] ’oral contraceptive linked conditions breast cancer’, [6] ’combined oral contraceptive risk breast cancer’, [7] ’Oral contraceptive pills cancer prevention effects on patients’, [8] ’Effect of combined oral contraceptives on cancer risk’...

**中文**

选项：[A.] 高血压，[B.] 卵巢癌，[C.] 宫颈癌，[D.] 乳腺癌 基本事实：B（卵巢癌） 综合查询：[1]“使用口服避孕药可降低卵巢癌风险”，[2]“激素癌症风险避孕药”，[3]“口服避孕药对癌症的预防作用”，[4]“避孕药的致癌作用”雌激素治疗”，[5]“口服避孕药相关乳腺癌疾病”，[6]“联合口服避孕药风险乳腺癌”，[7]“口服避孕药对患者的癌症预防作用”，[8]“联合口服避孕药对癌症风险的影响”...

### 段落 54 · Page 7

**EN**

Filtered Facts: [1] Ovarian cancer: Women who have ever used oral contraceptives have a 30% to 50% lower risk of ovarian cancer than women who have never used oral contraceptives. [2] The longer a woman uses oral contraceptives, the greater the increase in her risk of cervical cancer. One study found a 10% increased risk .... [7] Combined oral contraceptives (OCs) have been associated with a reduced risk of ovarian and endometrial cancers, an increased risk of cervical cancer and liver cancers, and an increased risk of breast cancer among recent users.

**中文**

过滤事实：[1] 卵巢癌：曾经使用过口服避孕药的女性患卵巢癌的风险比从未使用过口服避孕药的女性低 30% 至 50%。 [2] 女性使用口服避孕药的时间越长，患宫颈癌的风险就越大。一项研究发现，风险增加了 10%...[7] 复方口服避孕药 (OC) 与近期使用者中卵巢癌和子宫内膜癌风险降低、宫颈癌和肝癌风险增加以及乳腺癌风险增加相关。

### 段落 55 · Page 7

**EN**

Answer Before Retrieval: The patient is a 17-year-old girl with severe acne vulgaris that ... Considering the patient’s age and sex, the most relevant condition to consider is related to reproductive health. Among the options provided, cervical cancer is a well-known risk that can be reduced with the use of oral contraceptive pills... Answer after Retrieval: To determine the correct answer, let’s analyze the information provided in the documents. 1. The patient is a 17-year-old girl with ...

**中文**

检索前答复：患者是一名17岁女孩，患有严重寻常痤疮，...考虑到患者的年龄和性别，最需要考虑的情况是与生殖健康有关。在提供的选项中，宫颈癌是一种众所周知的风险，可以通过使用口服避孕药来降低……检索后答案：为了确定正确答案，让我们分析一下文档中提供的信息。 1. 患者是一名 17 岁女孩，患有...

### Page 8

### 段落 56 · Page 8

**EN**

0 4 16 3255 60 65 57.1% 58.6% 62.9% 64.9% Generated Queries MedMCQA 0 4 16 3274 78 82 86 76.9% 79.4% 81.4% 84.9% Generated Queries MMLU_Med 0 4 16 3260 65 70 75 62.9% 63.7% 67.1% 72.3% Generated Queries Accuracy (%) MedQA Figure 3: Comparison of model accuracies for MedMCQA, MMLU_Med, and MedQA across different numbers of generated queries. Note that the 0-query baseline directly uses the original question for retrieval. As the number of generated queries increases, the performance of RAG improves significantly. 2. We need to find out which condition ... 3.

**中文**

0 4 16 3255 60 65 57.1% 58.6% 62.9% 64.9% 生成的查询 MedMCQA 0 4 16 3274 78 82 86 76.9% 79.4% 81.4% 84.9% 生成的查询 MMLU_Med 0 4 16 3260 65 70 75 62.9% 63.7% 67.1% 72.3% 生成的查询准确度 (%) MedQA 图 3：不同数量的生成查询中 MedMCQA、MMLU_Med 和 MedQA 的模型准确度比较。请注意，0 查询基线直接使用原始问题进行检索。随着生成查询数量的增加，RAG 的性能显着提高。 2. 我们需要找出哪种条件... 3.

### 段落 57 · Page 8

**EN**

According to the documents, combined oral contraceptives (OCs) have been associated with a reduced risk of ovarian cancer. 4. The documents also mention that the longer a woman uses oral contraceptives, the greater the increase in her risk of cervical cancer, but this is not a reduction in risk. 5. Additionally, OCs have been associated with an increased risk of breast cancer among recent users, but this is not a reduction in risk. 6. Finally, the documents mention that OCs have been associated with a reduced risk of ovarian and endometrial cancers, but the question specifically asks about ovarian cancer.

**中文**

根据文件，复方口服避孕药（OC）与降低卵巢癌风险有关。 4. 文件还提到，女性使用口服避孕药的时间越长，患宫颈癌的风险增加就越大，但这并不是风险降低。 5. 此外，口服避孕药与近期使用者患乳腺癌的风险增加有关，但这并不能降低风险。 6. 最后，文件提到 OC 与降低卵巢癌和子宫内膜癌的风险有关，但问题特别询问了卵巢癌。

### 段落 58 · Page 8

**EN**

Therefore, based on the information provided, the correct answer is related to ovarian cancer. : Retrieved facts utilized in the final answer. : The selected answer. 4 Related Work While large language models excel at question answering, they struggle with specialized medical knowledge (Shi et al., 2023). Traditional RAG systems have been proposed to mitigate these limitations by integrating external knowledge sources into the LLMs’ input, thereby enhancing their ability to generate accurate and contextually relevant responses (Brown et al., 2020; Guu et al., 2020).

**中文**

因此，根据提供的信息，正确答案与卵巢癌有关。：最终答案中使用的检索事实。：所选答案。 4 相关工作虽然大型语言模型擅长回答问题，但它们在专业医学知识方面却遇到了困难（Shi et al., 2023）。人们提出传统的 RAG 系统通过将外部知识源集成到法学硕士的输入中来减轻这些限制，从而增强其生成准确且与上下文相关的响应的能力（Brown 等人，2020；Guu 等人，2020）。

### 段落 59 · Page 8

**EN**

Nonetheless, these early RAG approaches predominantly relied on retrieving information from structured databases or knowledge graphs, which can be insufficient for handling the complexity and nuanced requirements of specialized medical queries (Jin et al., 2020; Xiong et al., 2024a). Recent advancements in RAG systems have focused on improving the accuracy and relevance of retrieved medical information. Xiong et al. (Xiong et al., 2024b) propose i-MedRAG, which uses iterative follow-up questions to help LLMs better understand complex medical queries through dynamic information seeking. Das et al.

**中文**

尽管如此，这些早期的 RAG 方法主要依赖于从结构化数据库或知识图中检索信息，这可能不足以处理专业医学查询的复杂性和细致入微的要求（Jin 等人，2020；Xiong 等人，2024a）。 RAG 系统的最新进展集中于提高检索到的医疗信息的准确性和相关性。熊等人。 （Xiong 等人，2024b）提出了 i-MedRAG，它使用迭代的后续问题来帮助法学硕士通过动态信息搜索更好GEO解复杂的医学查询。达斯等人。

### 段落 60 · Page 8

**EN**

(Das et al., 2024) introduce a two-layer RAG framework and use soical media data to address challenges in lowresource medical question answering scenarios. Recent work has also explored uncertainty estimation in RAG systems for various purposes (Ozaki et al., 2024; Li et al., 2024). Some approaches use uncertainty to determine when to retrieve external information (Ding et al., 2024; Liu et al., 2024), while others focus on improving robustness by reducing semantic inconsistencies from random chunking (Li et al., 2024) or enhancing decoding (Qiu et al., 2024).

**中文**

（Das 等人，2024）引入了两层 RAG 框架，并使用社交媒体数据来解决资源匮乏的医疗问答场景中的挑战。最近的工作还探索了 RAG 系统中用于各种目的的不确定性估计（Ozaki 等人，2024 年；Li 等人，2024 年）。一些方法利用不确定性来确定何时检索外部信息（Ding et al., 2024；Liu et al., 2024），而其他方法则侧重于通过减少随机分块带来的语义不一致（Li et al., 2024）或增强解码（Qiu et al., 2024）来提高鲁棒性。

### 段落 61 · Page 8

**EN**

Despite these advancements, existing RAG frameworks still struggle with retrieving fine-grained and up-to-date knowledge, particularly for complex medical questions. This is because traditional knowledge bases and graphs often lack the granularity and timeliness needed for specialized medical queries. Our approach addresses these limitations by utilizing search engines for real-time knowledge retrieval. 5 Conclusion In this paper, we presented SearchRAG, a novel retrieval-augmented generation framework designed to enhance large language models’ performance in complex medical question-answering tasks.

**中文**

尽管取得了这些进步，现有的 RAG 框架仍然难以检索细粒度和最新的知识，特别是对于复杂的医学问题。这是因为传统的知识库和图表通常缺乏专业医学查询所需的粒度和及时性。我们的方法通过利用搜索引擎进行实时知识检索来解决这些限制。 5 结论 在本文中，我们提出了 SearchRAG，一种新颖的检索增强生成框架，旨在增强大型语言模型在复杂医学问答任务中的性能。

### 段落 62 · Page 8

**EN**

Our approach integrates synthetic query generation and uncertainty-based knowledge selection to optimize the retrieval of relevant information from search engines. Through extensive experiments, we demonstrated that SearchRAG significantly improves the accuracy and coherence of the model’s responses compared to traditional RAG approaches. These findings suggest that our framework can effectively address the limitations of conventional RAG systems.

**中文**

我们的方法集成了综合查询生成和基于不确定性的知识选择，以优化从搜索引擎检索相关信息。通过大量实验，我们证明与传统 RAG 方法相比，SearchRAG 显着提高了模型响应的准确性和连贯性。这些发现表明我们的框架可以有效解决传统 RAG 系统的局限性。

### Page 9

### 段落 63 · Page 9

**EN**

6 Limitations One potential limitation of our approach is the reliance on search engines for knowledge retrieval. The results returned by search engines may sometimes include incorrect or unreliable information sources. In practical applications, it is crucial to have domain experts review the retrieved content to ensure its accuracy. Alternatively, restricting the search to a curated list of trusted websites can help mitigate this issue and improve the reliability of the information used by the model.

**中文**

6 局限性 我们方法的一个潜在局限性是依赖搜索引擎进行知识检索。搜索引擎返回的结果有时可能包括不正确或不可靠的信息源。在实际应用中，由领域专家审查检索到的内容以确保其准确性至关重要。或者，将搜索限制在受信任网站的精选列表中可以帮助缓解此问题并提高模型所使用信息的可靠性。

### 段落 64 · Page 9

**EN**

7 Ethical Impact This research utilizes the LLaMA foundation model (Dubey et al., 2024), operating within the scope of its academic licensing agreement. Our implementation strictly adheres to the academicuse provisions specified in the license, with all applications limited to scholarly research purposes. The study draws upon three medical domain datasets: MedQA (Jin et al., 2021), MMLU_Med (Hendrycks et al., 2020), and MedM- CQA (Pal et al., 2022), each employed in accordance with their respective usage guidelines and data governance frameworks.

**中文**

7 道德影响 本研究利用 LLaMA 基金会模型（Dubey 等人，2024），在其学术许可协议的范围内运作。我们的实施严格遵守许可证中指定的学术使用条款，所有应用仅限于学术研究目的。该研究利用了三个医学领域数据集：MedQA（Jin 等人，2021）、MMLU_Med（Hendrycks 等人，2020）和 MedM-CQA（Pal 等人，2022），每个数据集都根据各自的使用指南和数据治理框架进行使用。

### 段落 65 · Page 9

**EN**

We have conducted thorough reviews to ensure compliance with data protection protocols, confirming the absence of personally identifiable information such as patient names or unique identifiers. Furthermore, our data processing protocols have verified that the content is appropriate and free from inappropriate material, maintaining high standards of research ethics and data integrity. Additionally, we utilized Chat- GPT (Hurst et al., 2024) to assist with grammatical refinements during the writing process. References Ahrefs. 2024. Google advanced search operators: The complete list (42 advanced operators).

**中文**

我们进行了彻底的审查，以确保遵守数据保护协议，确认不存在患者姓名或唯一标识符等个人身份信息。此外，我们的数据处理协议已验证内容适当且不含不当材料，从而保持了高标准的研究道德和数据完整性。此外，我们还利用 Chat-GPT（Hurst 等人，2024）来协助写作过程中的语法改进。参考文献 Ahrefs. 2024. Google 高级搜索运算符：完整列表（42 个高级运算符）。

### 段落 66 · Page 9

**EN**

https://ahrefs.com/blog/ google-advanced-search-operators/ . Accessed: 2024-06-17. Bradley Brown, Jordan Juravsky, Ryan Ehrlich, Ronald Clark, Quoc V Le, Christopher Ré, and Azalia Mirhoseini. 2024. Large language monkeys: Scaling inference compute with repeated sampling. arXiv preprint arXiv:2407.21787. Tom Brown, Benjamin Mann, Nick Ryder, Melanie Subbiah, Jared D Kaplan, Prafulla Dhariwal, Arvind Neelakantan, Pranav Shyam, Girish Sastry, Amanda Askell, et al. 2020. Language models are few-shot learners. Advances in neural information processing systems, 33:1877–1901. Thomas M Cover. 1999. Elements of information theory. John Wiley & Sons.

**中文**

https://ahrefs.com/blog/google-advanced-search-operators/。访问时间：2024 年 6 月 17 日。布拉德利·布朗、乔丹·尤拉夫斯基、瑞安·埃利希、罗纳德·克拉克、Quoc V Le、克里斯托弗·雷和阿扎莉亚·米尔霍塞尼。 2024. 大语言猴子：通过重复采样扩展推理计算。 arXiv 预印本 arXiv：2407.21787。汤姆·布朗、本杰明·曼、尼克·莱德、梅兰妮·苏比亚、贾里德·D·卡普兰、普拉富拉·达里瓦尔、阿文德·尼拉坎坦、普拉纳夫·希亚姆、吉里什·萨斯特里、阿曼达·阿斯克尔等。 2020 年。语言模型是小样本学习者。神经信息处理系统的进展，33：1877-1901。托马斯·M·盖。 1999。信息论要素。约翰·威利父子。

### 段落 67 · Page 9

**EN**

Florin Cuconasu, Giovanni Trappolini, Federico Siciliano, Simone Filice, Cesare Campagnano, Yoelle Maarek, Nicola Tonellotto, and Fabrizio Silvestri. 2024. The power of noise: Redefining retrieval for rag systems. arXiv preprint arXiv:2401.14887. Sudeshna Das, Yao Ge, Yuting Guo, Swati Rajwal, JaMor Hairston, Jeanne Powell, Drew Walker, Snigdha Peddireddy, Sahithi Lakamana, Selen Bozkurt, et al. 2024. Two-layer retrieval augmented generation framework for low-resource medical question-answering: proof of concept using reddit data. arXiv preprint arXiv:2405.19519. Hanxing Ding, Liang Pang, Zihao Wei, Huawei Shen, and Xueqi Cheng. 2024.

**中文**

弗洛林·库科纳苏、乔瓦尼·特拉波利尼、费德里科·西西利亚诺、西蒙娜·菲利斯、切萨雷·坎帕尼亚诺、约尔·马雷克、尼古拉·托内洛托和法布里奇奥·西尔维斯特里。 2024. 噪音的力量：重新定义抹布系统的检索。 arXiv 预印本 arXiv：2401.14887。 Sudeshna Das、姚戈、郭雨婷、Swati Rajwal、JaMor Hairston、Jeanne Powell、Drew Walker、Sniigdha Peddireddy、Sahithi Lakamana、Selen Bozkurt 等。 2024 年。用于低资源医学问答的两层检索增强生成框架：使用 Reddit 数据进行概念验证。 arXiv 预印本 arXiv：2405.19519。丁寒星、庞亮、魏子豪、沉华伟、程学奇。 2024 年。

### 段落 68 · Page 9

**EN**

Retrieve only when it needs: Adaptive retrieval augmentation for hallucination mitigation in large language models. arXiv preprint arXiv:2402.10612. Abhimanyu Dubey, Abhinav Jauhri, Abhinav Pandey, Abhishek Kadian, Ahmad Al-Dahle, Aiesha Letman, Akhil Mathur, Alan Schelten, Amy Yang, Angela Fan, et al. 2024. The llama 3 herd of models. arXiv preprint arXiv:2407.21783. Leo Gao, Stella Biderman, Sid Black, Laurence Golding, Travis Hoppe, Charles Foster, Jason Phang, Horace He, Anish Thite, Noa Nabeshima, Shawn Presser, and Connor Leahy. 2020. The Pile: An 800gb dataset of diverse text for language modeling. arXiv preprint arXiv:2101.00027.

**中文**

仅在需要时检索：自适应检索增强，用于减轻大型语言模型中的幻觉。 arXiv 预印本 arXiv：2402.10612。 Abhimanyu Dubey、Abhinav Jauhri、Abhinav Pandey、Abhishek Kadian、Ahmad Al-Dahle、Aiesha Letman、Akhil Mathur、Alan Schelten、Amy Yang、Angela Fan 等。 2024 年。美洲驼 3 群模型。 arXiv 预印本 arXiv：2407.21783。 Leo Gau、Stella Biderman、Sid Black、Laurence Golding、Travis Hoppe、Charles Foster、Jason Phang、Horace He、Anish Thite、Noa Nabeshima、Shawn Presser 和 Connor Leahy。 2020. The Pile：用于语言建模的 800gb 不同文本数据集。 arXiv 预印本 arXiv：2101.00027。

### 段落 69 · Page 9

**EN**

Google. 2022. How we’re improving search results when you use quotes. Accessed: 2025-02-13. Google. 2025. Google Search. Accessed: 2025-02-09. Kelvin Guu, Kenton Lee, Zora Tung, Panupong Pasupat, and Mingwei Chang. 2020. Retrieval augmented language model pre-training. In International conference on machine learning, pages 3929–3938. PMLR. Dan Hendrycks, Collin Burns, Steven Basart, Andy Zou, Mantas Mazeika, Dawn Song, and Jacob Steinhardt. 2020. Measuring massive multitask language understanding. arXiv preprint arXiv:2009.03300.

**中文**

谷歌。 2022. 当您使用引号时，我们如何改进搜索结果。访问时间：2025 年 2 月 13 日。谷歌。 2025。谷歌搜索。访问时间：2025 年 2 月 9 日。 Kelvin Guu、Kenton Lee、Zora Tung、Panupong Pasupat 和 Mingwei Chang。 2020.检索增强语言模型预训练。国际机器学习会议，第 3929-3938 页。 PMLR。丹·亨德里克斯、科林·伯恩斯、史蒂文·巴沙特、安迪·邹、曼塔斯·马泽卡、道恩·宋和雅各布·斯坦哈特。 2020。测量大规模多任务语言理解。 arXiv 预印本 arXiv：2009.03300。

### 段落 70 · Page 9

**EN**

Aaron Hurst, Adam Lerer, Adam P Goucher, Adam Perelman, Aditya Ramesh, Aidan Clark, AJ Ostrow, Akila Welihinda, Alan Hayes, Alec Radford, et al. 2024. Gpt-4o system card. arXiv preprint arXiv:2410.21276. Di Jin, Eileen Pan, Nassim Oufattole, Wei-Hung Weng, Hanyi Fang, and Peter Szolovits. 2020. What disease does this patient have. A Large-scale Open Domain Question Answering Dataset from Medical Exams. arXiv [cs. CL].

**中文**

Aaron Hurst、Adam Lerer、Adam P Goucher、Adam Perelman、Aditya Ramesh、Aidan Clark、AJ Ostrow、Akila Welihinda、Alan Hayes、Alec Radford 等。 2024.Gpt-4o 系统卡。 arXiv 预印本 arXiv：2410.21276。金迪、潘艾琳、Nassim Oufattole、翁伟宏、方汉仪和彼得·索洛维茨。 2020年，这位患者得的是什么病。来自医学检查的大规模开放域问答数据集。 arXiv [cs. CL]。

### Page 10

### 段落 71 · Page 10

**EN**

Di Jin, Eileen Pan, Nassim Oufattole, Wei-Hung Weng, Hanyi Fang, and Peter Szolovits. 2021. What disease does this patient have? a large-scale open domain question answering dataset from medical exams. Applied Sciences, 11(14):6421. Zixuan Li, Jing Xiong, Fanghua Ye, Chuanyang Zheng, Xun Wu, Jianqiao Lu, Zhongwei Wan, Xiaodan Liang, Chengming Li, Zhenan Sun, et al. 2024. Uncertaintyrag: Span-level uncertainty enhanced longcontext modeling for retrieval-augmented generation. arXiv preprint arXiv:2410.02719. Huanshuo Liu, Hao Zhang, Zhijiang Guo, Kuicai Dong, Xiangyang Li, Yi Quan Lee, Cong Zhang, and Yong Liu. 2024.

**中文**

金迪、潘艾琳、Nassim Oufattole、翁伟宏、方汉仪和彼得·索洛维茨。 2021. 这位患者得的是什么病？来自医学检查的大规模开放域问答数据集。应用科学，11（14）：6421。李子轩，熊竞，叶方华，郑川阳，吴迅，陆建桥，万中伟，梁晓丹，李成明，孙哲南，等。 2024.Uncertaintyrag：跨度级别的不确定性增强了检索增强生成的长上下文建模。 arXiv 预印本 arXiv：2410.02719。刘焕硕、张浩、郭志江、董奎才、李向阳、李一泉、张聪和刘勇。 2024 年。

### 段落 72 · Page 10

**EN**

Ctrla: Adaptive retrieval-augmented generation via probe-guided control. arXiv preprint arXiv:2405.18727. Zhiyong Lu. 2011. Pubmed and beyond: a survey of web tools for searching biomedical literature. Database, 2011:baq036. Marianne Lykke, Susan Price, and Lois Delcambre. 2012. How doctors search: A study of query behaviour and the impact on search results.Information processing & management, 48(6):1151–1170. Xinbei Ma, Yeyun Gong, Pengcheng He, Hai Zhao, and Nan Duan. 2023. Query rewriting for retrievalaugmented large language models. arXiv preprint arXiv:2305.14283.

**中文**

Ctrla：通过探针引导控制进行自适应检索增强生成。 arXiv 预印本 arXiv：2405.18727。卢志勇. 2011. Pubmed 及其他：用于搜索生物医学文献的网络工具的调查。数据库，2011：baq036。玛丽安·莱克、苏珊·普莱斯和洛伊丝·德尔坎布雷。 2012. 医生如何搜索：查询行为及其对搜索结果影响的研究。信息处理与管理，48（6）：1151–1170。马新北、宫业云、何鹏程、赵海、段南。 2023. 用于检索增强大型语言模型的查询重写。 arXiv 预印本 arXiv：2305.14283。

### 段落 73 · Page 10

**EN**

Shintaro Ozaki, Yuta Kato, Siyuan Feng, Masayo Tomita, Kazuki Hayashi, Ryoma Obara, Masafumi Oyamada, Katsuhiko Hayashi, Hidetaka Kamigaito, and Taro Watanabe. 2024. Understanding the impact of confidence in retrieval augmented generation: A case study in the medical domain. arXiv preprint arXiv:2412.20309. Ankit Pal, Logesh Kumar Umapathi, and Malaikannan Sankarasubbu. 2022. Medmcqa: A large-scale multisubject multi-choice dataset for medical domain question answering. In Proceedings of the Conference on Health, Inference, and Learning, volume 174 of Proceedings of Machine Learning Research, pages 248–260. PMLR.

**中文**

尾崎慎太郎、加藤裕太、冯思源、富田正世、林一树、小原龙马、小山田雅文、林克彦、上井藤秀隆和渡边太郎。 2024。了解检索增强生成的信心的影响：医学领域的案例研究。 arXiv 预印本 arXiv：2412.20309。 Ankit Pal、Logesh Kumar Umapathi 和 Malaikannan Sankarasubbu。 2022. Medmcqa：用于医学领域问答的大规模多主题多项选择数据集。摘自《健康、推理和学习会议记录》，《机器学习研究记录》第 174 卷，第 248-260 页。 PMLR。

### 段落 74 · Page 10

**EN**

Zexuan Qiu, Zijing Ou, Bin Wu, Jingjing Li, Aiwei Liu, and Irwin King. 2024. Entropy-based decoding for retrieval-augmented large language models. arXiv preprint arXiv:2406.17519. Yucheng Shi, Qiaoyu Tan, Xuansheng Wu, Shaochen Zhong, Kaixiong Zhou, and Ninghao Liu. 2024. Retrieval-enhanced knowledge editing in language models for multi-hop question answering. In Proceedings of the 33rd ACM International Conference on Information and Knowledge Management, pages 2056–2066. Yucheng Shi, Shaochen Xu, Zhengliang Liu, Tianming Liu, Xiang Li, and Ninghao Liu. 2023. Mededit: Model editing for medical question answering with external knowledge bases.

**中文**

邱泽轩、欧紫晶、吴斌、李晶晶、刘爱伟和欧文·金。 2024. 用于检索增强大型语言模型的基于熵的解码。 arXiv 预印本 arXiv：2406.17519。史玉成、谭巧玉、吴宣胜、钟少辰、周凯雄、刘宁浩。 2024. 用于多跳问答的语言模型中的检索增强知识编辑。第 33 届 ACM 国际信息和知识管理会议记录，第 2056-2066 页。石玉成、徐少辰、刘正良、刘天明、李翔、刘宁浩。 2023. Mededit：使用外部知识库进行医学问答的模型编辑。

### 段落 75 · Page 10

**EN**

arXiv preprint arXiv:2309.16035. Xiaozhi Wang, Tianyu Gao, Zhaocheng Zhu, Zhengyan Zhang, Zhiyuan Liu, Juanzi Li, and Jian Tang. 2021. Kepler: A unified model for knowledge embedding and pre-trained language representation. Transactions of the Association for Computational Linguistics, 9:176–194. Jason Wei, Xuezhi Wang, Dale Schuurmans, Maarten Bosma, Fei Xia, Ed Chi, Quoc V Le, Denny Zhou, et al. 2022. Chain-of-thought prompting elicits reasoning in large language models. Advances in neural information processing systems, 35:24824–24837. Guangzhi Xiong, Qiao Jin, Zhiyong Lu, and Aidong Zhang. 2024a.

**中文**

arXiv 预印本 arXiv：2309.16035。王晓志、高天宇、朱兆成、张正彦、刘志远、李娟子和唐健。 2021.开普勒：知识嵌入和预训练语言表示的统一模型。计算语言学协会汇刊，9：176-194。 Jason Wei、王学智、Dale Schuurmans、Maarten Bosma、Fei Xia、Ed Chi、Quoc V Le、Denny Zhou 等。 2022. 思维链提示引发大型语言模型的推理。神经信息处理系统的进展，35：24824–24837。熊光志、金乔、卢志勇、张爱东。 2024a。

### 段落 76 · Page 10

**EN**

Benchmarking retrievalaugmented generation for medicine. arXiv preprint arXiv:2402.13178. Guangzhi Xiong, Qiao Jin, Xiao Wang, Minjia Zhang, Zhiyong Lu, and Aidong Zhang. 2024b. Improving retrieval-augmented generation in medicine with iterative follow-up questions. In Biocomputing 2025: Proceedings of the Pacific Symposium, pages 199– 214. World Scientific. Ori Yoran, Tomer Wolfson, Ori Ram, and Jonathan Berant. 2023. Making retrieval-augmented language models robust to irrelevant context. arXiv preprint arXiv:2310.01558.

**中文**

基准检索增强了医学的生成。 arXiv 预印本 arXiv：2402.13178。熊光志、金乔、王晓、张敏嘉、卢志勇、张爱东。 2024b。通过迭代的后续问题改善医学领域的检索增强生成。载于《生物计算 2025：太平洋研讨会论文集》，第 199-214 页。世界科学。奥里·约兰、托默·沃尔夫森、奥里·拉姆和乔纳森·贝兰特。 2023. 使检索增强语言模型对不相关的上下文具有鲁棒性。 arXiv 预印本 arXiv：2310.01558。

### 段落 77 · Page 10

**EN**

A Experimental Details This section provides additional details about our experimental settings, dataset sources, retriever configurations, and prompt design used throughout the paper. A.1 Model Configurations and Hyperparameters Base LLMs. We use two variants of the LLaMA 3.1 model (Dubey et al., 2024), at 8B and 70B parameter scales. Both variants are instruction-tuned but not further fine-tuned for our experiments. For the 8B model, we employ bfloat16 for inference. For the 70B model, we employ INT4 quantization to reduce memory usage. Inference Setup. All experiments run on A6000 GPUs (48GB memory).

**中文**

实验细节本节提供了有关我们的实验设置、数据集来源、检索器配置和整篇论文中使用的提示设计的更多详细信息。 A.1 模型配置和超参数基础 LLM。我们使用 LLaMA 3.1 模型的两个变体（Dubey 等人，2024），参数尺度为 8B 和 70B。两种变体都经过指令调整，但没有针对我们的实验进行进一步微调。对于8B模型，我们使用bfloat16进行推理。对于 70B 模型，我们采用 INT4 量化来减少内存使用。推理设置。所有实验都在 A6000 GPU（48GB 内存）上运行。

### 段落 78 · Page 10

**EN**

The average GPU hours for our SearchRAG is roughly 0.018 hours/per medical question. Unless noted otherwise, we set the maximum generation length to 512 tokens, with a do_sample=False. For synthetic query generation, we increase the temperature up to 2.0 to promote query diversity. We generate up to 32 candidate queries for each input question; in ablation studies, we vary this number to assess its impact.

**中文**

我们的 SearchRAG 的平均 GPU 时间约为 0.018 小时/每个医疗问题。除非另有说明，我们将最大生成长度设置为 512 个标记，并且 do_sample=False。对于合成查询生成，我们将温度提高到 2.0 以促进查询多样性。我们为每个输入问题生成最多 32 个候选查询；在消融研究中，我们改变这个数字来评估其影响。

### Page 11

### 段落 79 · Page 11

**EN**

Uncertainty Computation. In Section 3.3 of the main paper, we measure uncertainty by approximating the Shannon entropy at the first-token output distribution. We use the final layer’s logits after seeing each query-augmented context. Higher entropy implies lower confidence. The difference in entropy (∆H) between the original context and the query-augmented context determines whether to keep each snippet. A.2 Datasets MedQA. We use the benchmark from Jin et al. (2021), which contains multiple-choice questions from US medical licensing exams. We follow the standard split of 1,273 questions for evaluation.

**中文**

不确定性计算。在主论文的 3.3 节中，我们通过近似第一个令牌输出分布的香农熵来测量不确定性。在查看每个查询增强上下文后，我们使用最后一层的逻辑。较高的熵意味着较低的置信度。原始上下文和查询增强上下文之间的熵 (ΔH) 差异决定是否保留每个片段。 A.2 MedQA 数据集。我们使用 Jin 等人的基准。 （2021），其中包含美国医疗执照考试的多项选择题。我们按照 1,273 个问题的标准划分进行评估。

### 段落 80 · Page 11

**EN**

Each question has four answer choices (A–D). MMLU_Med. We use the medical subset of the Massive Multitask Language Understanding (MMLU) benchmark (Hendrycks et al., 2020), consisting of six biomedical subject areas (anatomy, clinical knowledge, professional medicine, human genetics, college medicine, and college biology), for a total of 1,089 test questions. Each question also has four multiple-choice options. MedMCQA. We adopt the dataset introduced by Pal et al. (2022), which consists of 4,183 medical multiple-choice questions from real-world medical entrance exams.

**中文**

每个问题有四个答案选择 (A–D)。 MMLU_医学。我们使用大规模多任务语言理解 (MMLU) 基准的医学子集（Hendrycks 等人，2020），由六个生物医学学科领域（解剖学、临床知识、专业医学、人类遗传学、大学医学和大学生物学）组成，共有 1,089 个测试题。每个问题还有四个多项选择题。医学质量保证 (MedMCQA)。我们采用 Pal 等人引入的数据集。 (2022)，其中包含来自现实世界医学入学考试的 4,183 道医学多项选择题。

### 段落 81 · Page 11

**EN**

Each question has four options, and we follow the official evaluation split for testing. A.3 Knowledge Sources and Retriever Setup A.3.1 PubMed Subset PubMed is a comprehensive repository of biomedical and life sciences articles (Lu, 2011). In total, it indexes over 36 million articles. For our study, we follow Xiong et al. (2024a) and utilize a curated subset of around 23.9 million entries where each entry has a valid title and abstract. A.3.2 Textbooks Collection We also incorporate a set of 18 widely-used medical textbooks that cover fundamental subjects relevant for medical board examinations (Jin et al., 2020).

**中文**

每个问题有四个选项，我们按照官方的评估划分进行测试。 A.3 知识源和检索器设置 A.3.1 PubMed 子集 PubMed 是生物医学和生命科学文章的综合存储库（Lu，2011）。它总共索引了超过 3600 万篇文章。对于我们的研究，我们遵循 Xiong 等人的研究。 (2024a) 并利用约 2390 万个条目的精选子集，其中每个条目都有有效的标题和摘要。 A.3.2 教科书收集 我们还纳入了一套 18 本广泛使用的医学教科书，涵盖与医学委员会考试相关的基础科目（Jin 等人，2020）。

### 段落 82 · Page 11

**EN**

These textbooks offer a broad range of clinically relevant facts and explanations. A.4 Retriever and Search Engine Details Retriever Implementation. For PubMed and Textbooks, we follow a standard dense retrieval approach. We encode the document chunks using a domain-adapted bi-encoder (e.g., MedCPT (Xiong et al., 2024a)) and retrieve the top-k chunks based on cosine similarity with the query vector. We typically set k = 32 in our comparisons. Web Search Interface. For the web-based retrieval, we employ a public search API3.

**中文**

这些教科书提供了广泛的临床相关事实和解释。 A.4 检索器和搜索引擎详细信息检索器实现。对于 PubMed 和教科书，我们遵循标准的密集检索方法。我们使用域适应的双编码器（例如，MedCPT（Xiong 等人，2024a））对文档块进行编码，并根据与查询向量的余弦相似度检索前 k 个块。在比较中我们通常设置 k = 32。网络搜索界面。对于基于网络的检索，我们采用公共搜索 API3。

### 段落 83 · Page 11

**EN**

For each search, we employ the retrieved knowledge graph or answer box (if returned) and the top 3 organic results (title and snippet) for each generated query. The returned snippets typically include a short paragraph (50–200 words) that we concatenate to form the context. It is worth noting that we never included any AI overview content from Google. We omit any images, ads, or sections lacking textual descriptions. By design, we do not scrape full web pages, which mitigates potential copyright concerns. Instead, we rely on the concise snippets from search results to guide the LLM.

**中文**

对于每次搜索，我们都会使用检索到的知识图或答案框（如果返回）以及每个生成的查询的前 3 个有机结果（标题和片段）。返回的片段通常包括一个短段落（50-200 个单词），我们将其连接起来形成上下文。值得注意的是，我们从未包含任何来自谷歌的人工智能概述内容。我们省略任何缺乏文字描述的图像、广告或部分。根据设计，我们不会抓取完整的网页，这减轻了潜在的版权问题。相反，我们依靠搜索结果中的简洁片段来指导法学硕士。

### 段落 84 · Page 11

**EN**

Example Response for "Apple" Knowledge Graph: • Title: Apple • Description: American multinational technology company... • Attributes: Headquarters: Cupertino, CA; CEO: Tim Cook Organic Results: 1. Apple Official Site "Discover the innovative world of Apple and shop everything iPhone, iPad..." 2. Apple Wikipedia "Apple Inc. is an American multinational technology company specializing in..." A.5 Prompt Design Synthetic Query Generation Prompt. We design a specialized template to elicit concise, searchoptimized queries from the LLM.

**中文**

“Apple”知识图的响应示例： • 标题：Apple • 描述：美国跨国科技公司... • 属性：总部：加利福尼亚州库比蒂诺； CEO：蒂姆·库克 有机结果： 1. Apple 官方网站“探索 Apple 的创新世界，购买所有 iPhone、iPad...” 2. Apple 维基百科“Apple Inc. 是一家美国跨国科技公司，专门从事...” A.5 提示设计综合查询生成提示。我们设计了一个专门的模板来从法学硕士中引出简洁、搜索优化的查询。

### 段落 85 · Page 11

**EN**

Below is a simplified illustration: 3We used a third-party provider for Google Search results, specifically https://serper.dev/

**中文**

下面是一个简化的说明： 3我们使用第三方提供商来获取 Google 搜索结果，具体为 https://serper.dev/

### Page 12

### 段落 86 · Page 12

**EN**

System Role: “You are a medical expert. Generate focused search queries that will help determine the correct relationship between medical concepts. Your queries should: • Target the specific medical association being tested • Find evidence linking concepts in the question and options • Help differentiate between answer choices Given this medical question and its answer options, identify what specific general medical knowledge is needed to correctly answer the question.

**中文**

系统角色：“您是一名医学专家。生成有针对性的搜索查询，这将有助于确定医学概念之间的正确关系。您的查询应该： • 针对正在测试的特定医学协会 • 查找链接问题和选项中的概念的证据 • 帮助区分答案选择 鉴于此医学问题及其答案选项，确定正确回答该问题需要哪些特定的一般医学知识。

### 段落 87 · Page 12

**EN**

Generate one most relevant retrieval inquiry that is: • 3–8 words long • Focused on key medical terms • Formatted like search engine input • Targeting specific associations rather than general information Output your search query after ’Search_query:’ and think step by step.” User Role: “Question: [ Original Medical Question] Possible Answers: A) . . . B) . . . C) . . . D) . . . Please provide a single short query.” We sample multiple times (with higher temperature) to produce a range of candidate queries. System Role: “You are a medical expert.

**中文**

生成一个最相关的检索查询，即： • 3-8 个单词长 • 专注于关键医学术语 • 格式类似于搜索引擎输入 • 针对特定关联而不是一般信息 在“Search_query:”之后输出您的搜索查询并逐步思考。用户角色：“问题：[原始医疗问题] 可能的答案：A) . . . B) . . . C) . . . D) . . . 请提供一个简短的查询。”我们多次采样（温度较高）以产生一系列候选查询。系统角色：“你是一名医学专家。

### 段落 88 · Page 12

**EN**

Please pick the most likely option among A–D directly.” User Role: “Information: [Snippet Text] Question: [Same Medical Question] Answer Choices: A) . . . B) . . . C) . . . D) . . . Answer:” Uncertainty-Based Filtering Prompt. To measure how much each snippet reduces the model’s uncertainty, we provide a short prompt to the model asking it to directly choose an answer (A–D) given the retrieved snippet. The system’s output distribution for that first token is used to compute approximate entropy. This prompt is concise. We record the model’s probability distribution over tokens to approximate entropy.

**中文**

请直接从A-D中选出最有可能的选项。”用户角色：“信息：[片段文本] 问题：[同一医疗问题] 答案选择：A) . . . B) . . . C) . . . D) . . . 答案：”基于不确定性的过滤提示。为了衡量每个片段降低模型不确定性的程度，我们向模型提供一个简短的提示，要求它根据检索到的片段直接选择答案 (A–D)。系统的第一个标记的输出分布用于计算近似熵。这个提示很简洁。我们记录模型在令牌上的概率分布以近似熵。

### 段落 89 · Page 12

**EN**

A lower resulting entropy (compared to the base question without the snippet) indicates that snippet was informative. Final Answer Prompt. After selecting informative snippets, we concatenate them and present them to the model alongside the original question. The final prompt is: System Role: “You are a helpful medical expert.” User Role: “Below are some relevant excerpts: {[Concatenated Snippets] } Here is the question: { [Medical Question]} Possible Answers: A) . . . B) . . . C) . . . D) . . . Output your final answer after ’answer_choice’:” The system then generates a reasoning chain and ultimately appends the chosen answer.

**中文**

较低的结果熵（与没有片段的基本问题相比）表明该片段信息丰富。最终答案提示。选择信息片段后，我们将它们连接起来并将它们与原始问题一起呈现给模型。最后的提示是：系统角色：“您是一位乐于助人的医学专家。”用户角色：“以下是一些相关摘录：{[串联片段]}这是问题：{[医学问题]}可能的答案：A) . . . B) . . . C) . . . D) . . . 在‘answer_choice’之后输出您的最终答案：”然后系统生成推理链并最终附加所选答案。

### 段落 90 · Page 12

**EN**

In our experiments, we parse out that final selection to compare with the correct label. More details can be found in our code. A.6 Additional Notes and Practical Considerations Ethical, Privacy, and Data Protection Considerations. A critical concern when handling medical questions is avoiding patient data exposure. Directly inputting raw patient information into language models for retrieval risks potential data leakage and privacy violations. Our query rewriting approach addresses this by extracting only diseaserelated keywords and conceptual terms from the original question, rather than processing sensitive patient details.

**中文**

在我们的实验中，我们解析出最终选择以与正确的标签进行比较。更多详细信息可以在我们的代码中找到。 A.6 附加说明和实际注意事项 道德、隐私和数据保护注意事项。处理医疗问题时的一个关键问题是避免患者数据暴露。直接将原始患者信息输入到语言模型中进行检索可能存在潜在的数据泄露和隐私侵犯的风险。我们的查询重写方法通过从原始问题中仅提取与疾病相关的关键字和概念术语来解决这个问题，而不是处理敏感的患者详细信息。

### 段落 91 · Page 12

**EN**

When retrieving web snippets, we further minimize risks by using only short search engine excerpts (titles and summaries) rather than full documents. This dual protection - question sanitization through rewriting andrestricted snippet usage - prevents sensitive health information from entering the model’s processing pipeline while avoiding unintended use of copyrighted materials. B Case Study

**中文**

在检索网页片段时，我们仅使用简短的搜索引擎摘录（标题和摘要）而不是完整的文档，进一步将风险降到最低。这种双重保护 - 通过重写和限制片段使用进行问题清理 - 防止敏感的健康信息进入模型的处理管道，同时避免意外使用受版权保护的材料。 B 案例研究

### Page 13

### 段落 92 · Page 13

**EN**

Case Study 2: Question: A healthy 23-year-old male is undergoing an exercise stress test as part of his physiology class. If blood were to be sampled at different locations before and after the stress test, which area of the body would contain the lowest oxygen content at both time points?

**中文**

案例研究 2：问题：一名健康的 23 岁男性正在接受运动压力测试，作为生理学课程的一部分。如果在压力测试之前和之后在不同位置采集血液样本，那么在两个时间点身体的哪个区域的含氧量最低？

### 段落 93 · Page 13

**EN**

Choices: [A.] Inferior vena cava, [B.] Coronary sinus, [C.] IV Pulmonary artery, [D.] Pulmonary vein Ground Truth: B (Coronary sinus) Synthetic Queries: [1] ‘anatomical variation oxygen levels blood sampled’, [2] ’Oxygen content in different body compartments during exercise’, [3] ’Oxygen levels during exercise in pulmonary circulation’, [4] ’Oxygen content in various body veins during exercise’, 5] ’Oxygen content blood different body locations’, [6] ’blood oxygen content vs venous return areas’, [7] ’Blood oxygen content after exercise physiology’, [8] ’oxygen content gradient in coronary circulation’.

**中文**

选项：[A.] 下腔静脉，[B.] 冠状窦，[C.] IV 肺动脉，[D.] 肺静脉 基本事实：B（冠状窦） 综合查询：[1]“血液采样的解剖变化氧水平”，[2]“运动期间不同身体部位的氧含量”，[3]“运动期间肺循环中的氧水平”，[4] “运动期间身体各个静脉中的氧含量”，5]“不同身体部位的血液氧含量”，[6]“血氧含量与静脉回流区域”，[7]“运动生理学后的血氧含量”，[8]“冠脉循环中的氧含量梯度”。

### 段落 94 · Page 13

**EN**

Retrieved Fact: [1] Oxygen Saturation - StatPearls - NCBI Bookshelf - In the case of hypoxemia, a physician should always consider whether an arterial blood sample would provide a more accurate measure of oxygen saturation than ... Pattern Analysis of Oxygen Saturation Variability in Healthy Individuals - Pulse oximetry is routinely used for monitoring patients’ oxygen saturation levels with little regard to the variability of this physiological ... ABG, VBG, and pulse oximetry - EMCrit Project - The oxygen extraction of the hand isn’t very high, so avenous sample will often have only a slightly lower oxygen level than the arterial blood ...

**中文**

检索到的事实：[1] 氧饱和度 - StatPearls - NCBI 书架 - 在低氧血症的情况下，医生应始终考虑动脉血样本是否能提供比健康个体的氧饱和度变异性模式分析更准确的氧饱和度测量 - 脉搏血氧饱和度通常用于监测患者的氧饱和度水平，而很少考虑这种生理变化... ABG、VBG 和脉搏血氧饱和度 - EMCrit 项目 - 手的氧气提取量不是很高，因此静脉样本的氧气含量通常仅比动脉血略低......

### 段落 95 · Page 13

**EN**

[6] Venous Oxygen Saturation - StatPearls - NCBI Bookshelf - Venous oxygen saturation (SvO2) measures the blood’s oxygen content returning to the right side of the heart after perfusing the entire body. Arteriovenous Oxygen Difference - an overview | ScienceDirect Topics - The arteriovenous oxygen difference is a measure of the amount of oxygen taken up from the blood by the tissues. Relating oxygen partial pressure, saturation and content - Consequently, the blood “reserve” of oxygen is diminished and the venous oxygen content, saturation and partial pressure are all less than normal.

**中文**

[6] 静脉氧饱和度 - StatPearls - NCBI 书架 - 静脉氧饱和度 (SvO2) 测量灌注整个身体后返回心脏右侧的血液氧含量。动静脉血氧差 - 概述 | ScienceDirect 主题 - 动静脉氧差是组织从血液中吸收的氧气量的量度。与氧分压、饱和度和含量相关 - 因此，血液中的氧“储备”减少，静脉氧含量、饱和度和分压均低于正常值。

### 段落 96 · Page 13

**EN**

[8] Physiology, Alveolar to Arterial Oxygen Gradient - StatPearls - NCBI - The A-a gradient, or the alveolar-arterial gradient, measures the difference between the oxygen concentration in the alveoli and arterial system. Regulation of Coronary Blood Flow - PMC - PubMed Central - In a typical adult heart, baseline/resting left coronary blood flow typically ranges between 0.5 and 1.0 mL/min/g (270, 331, 918, 919). In contrast, right ... Coronary Artery Pressure - an overview | ScienceDirect Topics - The high extraction reduces the oxygen content from 195 ml/litre in arterial blood to only 50–70 ml/litre in coronary sinus blood.

**中文**

[8] 生理学，肺泡到动脉氧气梯度 - StatPearls - NCBI - A-a 梯度或肺泡动脉梯度测量肺泡和动脉系统中的氧气浓度之间的差异。冠状动脉血流量的调节 - PMC - PubMed Central - 在典型的成人心脏中，基线/静息左冠状动脉血流量通常在 0.5 至 1.0 mL/min/g 之间 (270, 331, 918, 919)。相比之下，右...冠状动脉压力 - 概述 | ScienceDirect 主题 - 高提取量将动脉血中的氧含量从 195 毫升/升降低到冠状窦血液中的 50-70 毫升/升。

### 段落 97 · Page 13

**EN**

Answer Before Retrieval: To determine which area of the body would contain the lowest oxygen content at both time points before and after the stress test, we need to consider the path of oxygen in the body during exercise. The oxygen content in the blood is typically highest in the pulmonary artery, as it is the point of entry of oxygenated blood from the lungs. As the blood travels through the body, the oxygen content decreases due to the extraction of oxygen by the tissues.

**中文**

检索前回答：为了确定压力测试前后两个时间点身体哪个部位的含氧量最低，我们需要考虑运动时氧气在体内的路径。血液中的氧含量通常在肺动脉中最高，因为它是含氧血液从肺部进入的点。当血液流经身体时，由于组织吸收氧气，氧气含量减少。

### 段落 98 · Page 13

**EN**

The coronary sinus, which is the collection of blood from the myocardium, would have a lower oxygen content than the pulmonary artery because the myocardium extracts oxygen from the blood. The inferior vena cava, which carries deoxygenated blood from the body back to the heart, would have an even lower oxygen content than the coronary sinus. The pulmonary vein, which carries oxygenated blood from the heart to the lungs, would have a higher oxygen content than the pulmonary artery. Therefore, the area of the body that would contain the lowest oxygen content at both time points before and after the stress test is the inferior vena cava.

**中文**

冠状窦是从心肌收集血液的地方，其含氧量比肺动脉低，因为心肌从血液中提取氧气。下腔静脉将脱氧的血液从身体输送回心脏，其含氧量甚至比冠状窦还要低。肺静脉将含氧血液从心脏输送到肺部，其含氧量高于肺动脉。因此，压力测试前后两个时间点含氧量最低的身体区域是下腔静脉。

### 段落 99 · Page 13

**EN**

Answer after Retrieval: To determine which area of the body would contain the lowest oxygen content at both time points, we need to consider the oxygen content gradient in different parts of the body. 1. First, we need to understand that the oxygen content in the blood decreases as it moves from the arterial system to the venous system due to the extraction of oxygen by the tissues. This is known as the arteriovenous oxygen difference. 2. Next, we need to consider the oxygen content in different venous return areas.

**中文**

检索后回答：为了确定两个时间点身体哪个部位的含氧量最低，我们需要考虑身体不同部位的含氧量梯度。 1. 首先，我们需要了解，由于组织吸取氧气，血液从动脉系统流向静脉系统时，血液中的氧含量会降低。这称为动静脉氧差。 2.接下来，我们需要考虑不同静脉回流区域的氧气含量。

### 段落 100 · Page 13

**EN**

The venous oxygen saturation (SvO2) measures the blood’soxygen content returning to the right side of the heart after perfusing the entire body. However, the oxygen content in the venous blood can vary depending on the location of the sampling site. 3. We are given information about the oxygen content in the coronary sinus, which is the venous blood returning from the heart muscle itself. The oxygen content in the coronary sinus is significantly lower than in other venous return areas, with a value of only 50-70 ml/litre compared to 195 ml/litre in arterial blood. 4.

**中文**

静脉血氧饱和度（SvO2）测量灌注全身后返回心脏右侧的血液含氧量。然而，静脉血中的氧含量可能会根据采样点的位置而变化。 3. 我们获得有关冠状窦中氧含量的信息，冠状窦是从心肌本身返回的静脉血。冠状窦中的氧含量明显低于其他静脉回流区域，其数值仅为50-70毫升/升，而动脉血中的氧含量为195毫升/升。 4.

### 段落 101 · Page 13

**EN**

Considering the information provided, we can conclude that the area of the body that would contain the lowest oxygen content at both time points is the coronary sinus, as it has the lowest oxygen content among the given options. 5. Therefore, the correct answer is the area that has the lowest oxygen content, which is the coronary sinus.

**中文**

考虑到所提供的信息，我们可以得出结论，在两个时间点氧含量最低的身体区域是冠状窦，因为它在给定选项中氧含量最低。 5. 因此，正确答案是含氧量最低的区域，即冠状窦。

### Page 14

### 段落 102 · Page 14

**EN**

Case Study 3: Question: A 37-year-old man with no significant past medical history is rear-ended in a motor vehicle accident. He reported significant neck pain to emergency responders, but otherwise denies weakness, numbness or tingling in his extremities. His vitals on presentation to the ED are HR 90, BP 140/80, RR 20, SpO2 98%. What is the most appropriate next step upon presentation to the emergency room?

**中文**

案例研究3：问题：一名37岁的男子，无重大既往病史，在一场机动车事故中被追尾。他向紧急救援人员报告了明显的颈部疼痛，但否认四肢无力、麻木或刺痛。向急诊科报告的他的生命体征为 HR 90、BP 140/80、RR 20、SpO2 98%。送往急诊室后最合适的下一步是什么？

### 段落 103 · Page 14

**EN**

Choices: [A.] Lateral cervical film, [B.] Cervical immobilization, [C.] IV methylprednisolone, [D.] Observation overnight Ground Truth: B (Cervical immobilization) Retrieved Queries: [1] ‘Acute trauma cervical spine care guidelines’, [2] ’Cervical spine injury ED management guidelines’, [3] ’whiplash injury cervical spine trauma protocol’, [4] ’Emergency management after motor vehicle accidents’, [5] ’trauma c-spine emergency department protocols’, [6] ’Emergency treatment motor vehicle accident spinal injury’, [7] ’Motor vehicle cervical spine emergency evaluation guidelines’, [8] ’Emergency cervical spine injury management’ Retrieved Fact:

**中文**

选项：[A.] 颈椎侧位片，[B.] 颈椎固定，[C.] 静脉注射甲泼尼龙，[D.] 过夜观察 事实真相：B（颈椎固定） 检索到的查询：[1] ‘急性创伤颈椎护理指南’，[2] ‘颈椎损伤急诊处理指南’，[3] ‘颈椎扭伤损伤方案’，[4] ‘紧急处理机动车事故后》、[5]《颈椎外伤急救方案》、[6]《机动车事故脊柱损伤急救处理》、[7]《机动车颈椎急救评估指南》、[8]《颈椎损伤急救处理》检索事实：

### 段落 104 · Page 14

**EN**

[1] Primary survey and immobilization of the cervical spine1 in rigid cervical collar with full spine precautions, which includes placing the patient on a flat surface and log-rolling the patient when needed.

**中文**

[1] 颈椎的初步检查和固定在刚性颈托中，并采取全面的脊柱预防措施，包括将患者放在平坦的表面上，并在需要时滚动患者。

### 段落 105 · Page 14

**EN**

[6] Treating spinal cord injuries. At an accident scene, if SCI is suspected, emergency personnel will place a rigid collar around the neck and carefully place the person on a backboard to prevent further damage to the spinal cord. They may use sedatives to relax the person and prevent movement. [8] If you suspect someone has a spinal injury: Call 911 or emergency medical help. Keep the person still. Place heavy towels or rolled sheets on both sides of the neck or hold the head and neck to prevent movement. Avoid moving the head or neck.

**中文**

[6] 治疗脊髓损伤。在事故现场，如果怀疑有脊髓损伤，急救人员会在颈部套上硬质项圈，并小心地将伤者放在背板上，以防止脊髓进一步受损。他们可能会使用镇静剂来放松患者并防止运动。 [8] 如果您怀疑有人脊椎受伤：请致电 911 或紧急医疗帮助。保持人不动。将重毛巾或卷床单放在颈部两侧或托住头部和颈部以防止移动。避免移动头部或颈部。

### 段落 106 · Page 14

**EN**

Answer Before Retrieval: The patient is a 37-year-old man with no significant past medical history who was rear-ended in a motor vehicle accident. He reports significant neck pain but denies weakness, numbness, or tingling in his extremities. The initial assessment of his vitals is within normal limits. Given the mechanism of injury and the patient’s symptoms, the primary concern is for potential cervical spine injury. The Canadian C-Spine Rule is a widely used clinical decision rule for determining the need for cervical spine imaging in patients with acute trauma.

**中文**

检索前答复：患者为一名37岁男性，无重大既往病史，因车祸被追尾。他报告有明显的颈部疼痛，但否认四肢无力、麻木或刺痛。他的生命体征初步评估在正常范围内。考虑到损伤机制和患者的症状，首要关注的是潜在的颈椎损伤。加拿大 C 脊柱规则是一种广泛使用的临床决策规则，用于确定急性创伤患者是否需要进行颈椎成像。

### 段落 107 · Page 14

**EN**

According to the rule, patients who meet any of the following criteria should undergo imaging: age 65 or older, dangerous mechanism of injury, paresthesias in the extremities, or a high-risk injury (e.g., fall from a height, axial load to the head or neck). The patient does not meet any of these criteria, but it is still important to consider the possibility of a cervical spine injury. The most appropriate next step is to perform a careful physical examination, including a thorough assessment of the patient’s neck and spine. This should include a log roll examination to assess for any signs of cervical spine injury.

**中文**

根据该规则，符合以下任一标准的患者应接受影像学检查：年龄在 65 岁或以上、危险的损伤机制、四肢感觉异常或高风险损伤（例如，从高处坠落、头部或颈部承受轴向负荷）。患者不符合任何这些标准，但考虑颈椎损伤的可能性仍然很重要。最合适的下一步是进行仔细的体检，包括对患者的颈部和脊柱进行彻底评估。这应包括滚轴检查，以评估颈椎损伤的任何迹象。

### 段落 108 · Page 14

**EN**

If the examination is normal, the patient can be considered for observation. However, if there are any signs of cervical spine injury, such as tenderness, deformity, or neurological deficits, imaging should be obtained. In this case, the patient’s symptoms and examination are normal, so the most appropriate next step is to observe him overnight and repeat the examination in the morning. Answer after Retrieval: The patient is suspected to have a cervical spine injury due to the motor vehicle accident. The most appropriate initial step is to prevent further damage to the spinal cord.

**中文**

如果检查正常，可以考虑对患者进行观察。然而，如果有颈椎损伤的任何迹象，例如压痛、畸形或神经功能缺损，则应进行影像学检查。在这种情况下，患者的症状和检查都正常，所以下一步最合适的就是观察他一夜，早上再重复检查。经检索答复：患者疑似因车祸造成颈椎损伤。最合适的初始步骤是防止脊髓进一步受损。

### 段落 109 · Page 14

**EN**

According to the provided documents, emergency personnel should place a rigid collar around the neck and carefully place the person on a backboard to prevent further damage to the spinal cord. This is also supported by the acute trauma cervical spine care guidelines, which emphasize the importance of immobilization of the cervical spine in a rigid cervical collar with full spine precautions. Therefore, the next step upon presentation to the emergency room should be to ensure the patient’scervical spine is immobilized.

**中文**

根据提供的文件，急救人员应在颈部套上坚硬的项圈，并小心地将伤者放在背板上，以防止脊髓进一步受损。这也得到了急性创伤颈椎护理指南的支持，该指南强调了将颈椎固定在刚性颈托中并采取全面脊柱预防措施的重要性。因此，送往急诊室后的下一步应该是确保患者的颈椎固定。
