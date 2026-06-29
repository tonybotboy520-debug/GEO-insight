# CiteFix: Enhancing RAG Accuracy Through Post-Processing Citation Correction

- ID: 73
- 类型: pdf
- 分类: 04_academic_papers
- 主题: citation accuracy correction in RAG products
- 原文链接: https://arxiv.org/pdf/2504.15629
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

arXiv:2504.15629v2 [cs.IR] 11 Jun 2025 CiteFix: Enhancing RAG Accuracy Through Post-Processing Citation Correction Harsh Maheshwari mahhars@amazon.com Srikanth Tenneti stenneti@amazon.com Alwarappan Nakkiran nakkiran@amazon.com Abstract Retrieval Augmented Generation (RAG) has emerged as a powerful application of Large Language Models (LLMs), revolutionizing information search and consumption. RAG systems combine traditional search capabilities with LLMs to generate comprehensive answers to user queries, ideally with accurate citations.

**中文**

arXiv:2504.15629v2 [cs.IR] 2025 年 6 月 11 日 CiteFix：通过后处理引文更正提高 RAG 准确性 Harsh Maheshwari mahhars@amazon.com Srikanth Tenneti stenneti@amazon.com Alwarappan Nakkiran nakkiran@amazon.com 摘要检索增强生成 (RAG) 已成为一种大型语言模型 (LLM) 的强大应用，彻底改变了信息搜索和消费。 RAG 系统将传统搜索功能与法学硕士相结合，为用户查询生成全面的答案，最好能提供准确的引用。

### 段落 2 · Page 1

**EN**

However, in our experience of developing a RAG product, LLMs often struggle with source attribution, aligning with other industry studies reporting citation accuracy rates of only about 74% for popular generative search engines. To address this, we present efficient post-processing algorithms to improve citation accuracy in LLM-generated responses, with minimal impact on latency and cost. Our approaches cross-check generated citations against retrieved articles using methods including keyword + semantic matching, fine tuned model with BERTScore, and a lightweight LLM-based technique.

**中文**

然而，根据我们开发 RAG 产品的经验，法学硕士经常在来源归因方面遇到困难，与其他行业研究报告的流行生成式搜索引擎的引文准确率仅为 74% 左右相一致。为了解决这个问题，我们提出了高效的后处理算法，以提高法学硕士生成的回复的引用准确性，同时对延迟和成本的影响最小。我们的方法使用关键字+语义匹配、BERTScore 微调模型以及基于 LLM 的轻量级技术等方法，对检索到的文章生成的引文进行交叉检查。

### 段落 3 · Page 1

**EN**

Our experimental results demonstrate a relative improvement of 15.46% in the overall accuracy metrics of our RAG system. This significant enhancement potentially enables a shift from our current larger language model to a relatively smaller model that is approximately 12x more cost-effective and 3x faster in inference time, while maintaining comparable performance. This research contributes to enhancing the reliability and trustworthiness of AI-generated content in information retrieval and summarization tasks which is critical to gain customer trust especially in commercial products.

**中文**

我们的实验结果表明，我们的 RAG 系统的整体精度指标相对提高了 15.46%。这一显着增强可能使我们能够从当前较大的语言模型转变为相对较小的模型，该模型的成本效益提高约 12 倍，推理时间加快 3 倍，同时保持可比较的性能。这项研究有助于提高人工智能生成的内容在信息检索和摘要任务中的可靠性和可信度，这对于赢得客户的信任至关重要，尤其是在商业产品中。

### 段落 4 · Page 1

**EN**

1 Introduction Recent advancements in AI infrastructure and methodologies have enabled training Large Language Models (LLMs) over internet-scale data. These models demonstrate impressive competence in answering a wide range of general queries. However, when applied to specialized domains such as addressing questions based on internal company documents, off-the-shelf LLMs exhibit significant limitations. They often lack access to latest information, have difficulty interpreting domain specific language, struggle with source attribution, are prone to hallucinations (Ji et al., 2023), and are prone to overly broad responses.

**中文**

1 简介 人工智能基础设施和方法论的最新进展使得能够通过互联网规模的数据训练大型语言模型 (LLM)。这些模型在回答各种一般查询方面表现出令人印象深刻的能力。然而，当应用于专业领域（例如根据公司内部文件解决问题）时，现成的法学硕士表现出很大的局限性。他们通常无法获取最新信息，难以解释特定领域的语言，难以确定来源，容易产生幻觉（Ji et al., 2023），并且容易做出过于广泛的反应。

### 段落 5 · Page 1

**EN**

To overcome these challenges, two broad strategies have emerged. The first involves fine-tuning LLMs on domain-specific data. However, this approach is not only resource-intensive and requires frequent updates, but also risks unintended consequences such as catastrophic forgetting, where the model loses previously acquired general knowledge, thereby increasing the overall system complexity. The second, often more practical method is Retrieval-Augmented Generation (RAG). RAG is a process that combines information retrieval with text generation.

**中文**

为了克服这些挑战，出现了两大战略。第一个涉及对特定领域数据的法学硕士进行微调。然而，这种方法不仅占用资源并且需要频繁更新，而且还存在意外后果的风险，例如灾难性遗忘，其中模型丢失了先前获得的一般知识，从而增加了整个系统的复杂性。第二种通常更实用的方法是检索增强生成（RAG）。 RAG 是一个将信息检索与文本生成相结合的过程。

### 段落 6 · Page 1

**EN**

It typically involves the following steps: (1) indexing a knowledge base of relevant information, (2) using a retrieval system to find content specifically relevant to a given user query, (3) providing the user query and the retrieved content to an LLM, instructing it to generate a response based on the retrieved content. RAG offers numerous benefits, including real-time access to up-to-date information, improved token generation (Khandelwal et al., 2019), reduced hallucinations, better source attribution (Gao et al., 2023a; Hsu et al., 2024) and overall superior response generation (Shuster et al., 2021; Béchard and Ayala, 2024).

**中文**

它通常涉及以下步骤：（1）索引相关信息的知识库，（2）使用检索系统查找与给定用户查询特别相关的内容，（3）向法学硕士提供用户查询和检索到的内容，指示其根据检索到的内容生成响应。 RAG 提供了许多好处，包括实时访问最新信息、改进令牌生成（Khandelwal 等人，2019）、减少幻觉、更好的源归因（Gao 等人，2023a；Hsu 等人，2024）以及整体卓越的响应生成（Shuster 等人，2021；Béchard 和 Ayala，2024）。

### 段落 7 · Page 1

**EN**

Additionally, RAG tends to be more cost-effective and transparent than full model fine-tuning. Examples of RAG-based products include Perplexity.ai (Perplexity AI, 2024), bing search, GPT Search etc. Despite enabling a novel information retrieval experience for users, RAG systems today face key limitations. Table 1 illustrates results of a Subject Matter Expert based auditing of a RAG based system. Shown is a metric "Relative Mean Question Level Accuracy", which captures relevancy of cited chunks, correctness and completeness of the

**中文**

此外，RAG 往往比完整模型微调更具成本效益和透明。基于 RAG 的产品示例包括 Perplexity.ai（Perplexity AI，2024）、bing 搜索、GPT 搜索等。尽管为用户提供了新颖的信息检索体验，但如今的 RAG 系统仍面临关键限制。表 1 说明了基于主题专家对基于 RAG 的系统进行审核的结果。显示的是“相对平均问题级别准确性”指标，它捕获了引用块的相关性、问题的正确性和完整性。

### Page 2

### 段落 8 · Page 2

**EN**

Figure 1: Improvements in RAG accuracy for various LLMs after employing our proposed citation correction methods. Results are shown as percentage improvements in Mean Question Level Accuracy(MQLA) over Model C baseline performance without citation correction. MQLA is a metric designed to capture relevancy, correctness and completeness (see Sec. 4.1). answer(Sec. 4.1), relative to Model C 1 accuracy. A prevalent form of error that contributes to lower performance is that of unverifiable facts in LLMs’ responses. Unverifiable facts are the facts in LLM response which cannot be validated by cited reference.

**中文**

图 1：采用我们提出的引文更正方法后，各种法学硕士的 RAG 准确性有所提高。结果显示为平均问题级别准确度 (MQLA) 相对于没有引文更正的模型 C 基线性能的百分比改进。 MQLA 是一个旨在捕获相关性、正确性和完整性的指标（参见第 4.1 节）。答案（第 4.1 节），相对于模型 C 1 精度。导致绩效下降的一种常见错误形式是法学硕士的回答中存在无法验证的事实。无法验证的事实是LLM回复中无法通过引用的参考文献进行验证的事实。

### 段落 9 · Page 2

**EN**

In our analysis for Model C, notably around 80% of these unverifiable facts were not pure hallucinations, but rather errors in the model’s ability to cite the correct reference from which it generated the given factual point. These observations align with industry studies (Liu et al., 2023) reporting citation accuracy rates of only about 74% for popular generative search engines. Incorrect citations not only reduce the actionability of the responses, but also dent customer trust, especially for commercial products. This paper focuses on this issue and proposes methods to address it.

**中文**

在我们对模型 C 的分析中，值得注意的是，这些无法验证的事实中大约 80% 并不是纯粹的幻觉，而是模型引用生成给定事实点的正确参考的能力存在错误。这些观察结果与行业研究（Liu 等人，2023）一致，该研究报告流行的生成式搜索引擎的引文准确率仅为 74% 左右。不正确的引用不仅会降低回复的可操作性，还会削弱客户的信任，特别是对于商业产品。本文重点讨论这个问题并提出解决方法。

### 段落 10 · Page 2

**EN**

While previous studies have explored attributable text generation ((Nakano et al., 2022); (Gao et al., 2023b)) and simple prompting techniques for citation incorporation ((Malaviya et al., 2024; Sun et al., 2024; Li et al., 2024)), systematic evaluations reveal significant performance gaps (Gao et al., 2023b). Recent work (Huang et al., 2024) has only scratched the surface by demonstrating attribution quality degradation from ChatGPT to Llama 2 7B, leaving a critical need for deeper analysis and practical solutions. This paper offers two contributions: 1Model names are anonymized following standard practice for proprietary/pre-release models.

**中文**

虽然之前的研究探索了归因文本生成（（Nakano et al., 2022）；（Gao et al., 2023b））和用于引用合并的简单提示技术（（Malaviya et al., 2024；Sun et al., 2024；Li et al., 2024）），但系统评估揭示了显着的性能差距（Gao et al., 2023b）。最近的工作（Huang 等人，2024）仅展示了从 ChatGPT 到 Llama 2 7B 的归因质量下降的表面，因此迫切需要更深入的分析和实用的解决方案。本文提供了两个贡献： 1按照专有/预发布模型的标准做法对模型名称进行匿名化。

### 段落 11 · Page 2

**EN**

Publicly available models retain their original names. Model A, Model B and Model C are sufficiently large and powerful language model. With number of parameters in decreasing order for A, B and C.

**中文**

公开可用的模型保留其原始名称。模型 A、模型 B 和模型 C 是足够大且强大的语言模型。 A、B 和 C 的参数数量按降序排列。

### 段落 12 · Page 2

**EN**

Model B however is the model trained on latest data with better methodologies Model Cents per 1K Relative Mean Question% of factual % of factual points % of factual pointsO/P tokens Level Accuracypoints unverifiable incorrectly cited purely hallucinatedModel A +1100% +7.9% (+12%)Base (Base) 90.8% (65%) 9.1% (35%)Model B +220% +21.1% (+21.1%)Base (Base) 66.6% (66.6%) 34.4% (-33.4%)Model C Base Base (+15.4%)Base (Base) 80.6% (33.3%) 19.4%(-66.6%)Qwen 14-B open source +10.5% (+15.8%)Base (Base) 76.2% (70.8%) -13.8% (29.2%)Qwen 2-B open source -39% (NA)NA NA NA Table 1: Motivating the need for CiteFix: This table shows the prevalence of incorrect citations across LLMs and our method’s impact.

**中文**

然而，模型 B 是使用更好的方法在最新数据上训练的模型 每 1K 模型美分 相对平均问题 % 事实 % 事实点 % 事实点 O/P 代币 级别 准确度点 无法验证 错误引用 纯粹是幻觉 模型 A +1100% +7.9% (+12%) 基础 (Base) 90.8% (65%) 9.1% (35%) 模型 B +220% +21.1% (+21.1%)Base (基础) 66.6% (66.6%) 34.4% (-33.4%)Model C Base (+15.4%)Base (基础) 80.6% (33.3%) 19.4%(-66.6%)Qwen 14-B 开源 +10.5% (+15.8%)Base (基础) 76.2% (70.8%) -13.8% (29.2%)Qwen 2-B 开源 -39% (NA)NA NA NA 表 1：激发对 CiteFix 的需求：此表显示了法学硕士中错误引用的普遍程度以及我们方法的影响。

### 段落 13 · Page 2

**EN**

Model C is the baseline for cost and accuracy columns. For the last three columns, the baseline is each model’s total percentage of unverifiable factual points. Numbers outside (inside) parentheses show performance before (after) CiteFix. Initially, incorrect citations significantly outnumber hallucinations. CiteFix balances this ratio and in absolute terms it drastically reduces incorrect citations. Qwen 2-B was excluded from detailed audit due to inconsistent citation generation. 1. Demonstrating the existence and extent of the incorrect citations issue across multiple LLMs, and highlighting the need to address the same. 2.

**中文**

模型 C 是成本和准确性列的基线。对于最后三列，基线是每个模型不可验证的事实点的总百分比。括号外（内）的数字显示 CiteFix 之前（之后）的性能。最初，错误引用的数量明显多于幻觉。 CiteFix 平衡了这一比率，从绝对值来看，它大大减少了错误引用。由于引文生成不一致，Qwen 2-B 被排除在详细审核之外。 1. 证明多个法学硕士中不正确引用问题的存在和程度，并强调解决该问题的必要性。 2.

### 段落 14 · Page 2

**EN**

Proposing six computationally light weight methods to address this issue, ranging from simple heuristic methods to more sophisticated learning-based solutions. Through extensive experimentation, we show that different citation correction approaches may be optimal for different LLMs - for instance, hybrid (lexical + semantic) matching works best with Model A, while fine-tuned BERTScore performs better with Model B. We provide detailed comparisons of their effectiveness and practical applicability.

**中文**

提出六种计算轻量级方法来解决这个问题，从简单的启发式方法到更复杂的基于学习的解决方案。通过广泛的实验，我们表明不同的引文校正方法可能对不同的法学硕士来说是最佳的 - 例如，混合（词汇+语义）匹配在模型 A 中效果最好，而微调的 BERTScore 在模型 B 中表现更好。我们提供了它们的有效性和实际适用性的详细比较。

### 段落 15 · Page 2

**EN**

As seen in Fig 1 and Table 1, our method resulted in an improvement of upto 15.46% relative improvement in accuracy when tested across four different LLMs. Through this work, we aim to not only advance the understanding of citation accuracy challenges in LLMs, but also provide practical low cost solutions for improving attribution in real-world applications. Sec. 2 presents an overview of related work. Sec. 3 details our proposed algorithms. Sec. 4 presents evaluation results. Sec. 5 concludes, along with a discussion of the limitations of our work and plans for addressing them going forward.

**中文**

如图 1 和表 1 所示，在四个不同的法学硕士中进行测试时，我们的方法使准确度相对提高了高达 15.46%。通过这项工作，我们的目标不仅是加深对法学硕士引用准确性挑战的理解，而且还提供实用的低成本解决方案，以改善实际应用中的归因。秒。图 2 概述了相关工作。秒。 3 详细介绍了我们提出的算法。秒。图4给出了评价结果。秒。 5 总结，同时讨论了我们工作的局限性以及未来解决这些局限性的计划。

### 段落 16 · Page 2

**EN**

2 Related Work Accurate attribution of information to sources remains a critical challenge in building trustworthy AI systems, particularly for Large Language

**中文**

2 相关工作 信息来源的准确归属仍然是构建值得信赖的人工智能系统的关键挑战，特别是对于大语言

### Page 3

### 段落 17 · Page 3

**EN**

Models (LLMs) and Retrieval-Augmented Generation (RAG) systems. The challenge of accurate attribution in AI-generated content has been approached from multiple angles in the literature. Some researchers have focused on developing models specifically designed for attributable text generation (Nakano et al., 2022), while others have explored the effectiveness of prompt engineering techniques for citation accuracy (Malaviya et al., 2024; Li et al., 2024).

**中文**

模型（LLM）和检索增强生成（RAG）系统。文献中已经从多个角度解决了人工智能生成内容准确归因的挑战。一些研究人员专注于开发专门为归因文本生成而设计的模型（Nakano et al., 2022），而其他研究人员则探索了即时工程技术对引文准确性的有效性（Malaviya et al., 2024；Li et al., 2024）。

### 段落 18 · Page 3

**EN**

However, a comprehensive study (Gao et al., 2023b) has highlighted that significant challenges remain, particularly in maintaining consistent attribution accuracy across different types of queries and document structures. These findings underscore the need for more robust and versatile approaches to citation/attribution in AI systems. Recent work has focused on the automatic evaluation of attribution by LLMs (Yue et al., 2023) and factual entailment for hallucination detection (Rawte et al., 2024), primarily assessing whether generated content is present in cited references.

**中文**

然而，一项综合研究（Gao 等人，2023b）强调，仍然存在重大挑战，特别是在不同类型的查询和文档结构之间保持一致的归因准确性方面。这些发现强调了人工智能系统中需要更强大、更通用的引用/归因方法。最近的工作重点是法学硕士归因的自动评估（Yue 等人，2023）和幻觉检测的事实蕴含（Rawte 等人，2024），主要评估生成的内容是否存在于引用的参考文献中。

### 段落 19 · Page 3

**EN**

However, there is a notable gap in research specifically addressing citation correction. Many existing methods, including those finetuning T5 models (Gao et al., 2023c; Song et al., 2024; Honovich et al., 2022), are limited by context lengths of around 512 tokens. This constraint poses significant challenges when dealing with longer documents or multiple sources, which is often the case in practical RAG systems. Our proposed solution for citation correction is designed to handle larger context lengths, addressing a critical limitation in current approaches.

**中文**

然而，专门针对引文更正的研究存在显着差距。许多现有方法，包括那些微调 T5 模型（Gao 等人，2023c；Song 等人，2024；Honovich 等人，2022），都受到大约 512 个标记的上下文长度的限制。在处理更长的文档或多源时，这种限制带来了重大挑战，这在实际的 RAG 系统中很常见。我们提出的引文更正解决方案旨在处理更大的上下文长度，解决当前方法的关键限制。

### 段落 20 · Page 3

**EN**

Furthermore, our research distinguishes itself by focusing on not just detecting citation errors but actively working towards correcting them. This shift from identification to correction represents a significant step forward in improving the usefulness of AI-generated content in RAG systems. We introduce a range of citation correction methods, including lexical matching, hybrid (lexical + semantic) approaches, and lightweight LLM-based attribution. One method builds on BERT Score (Zhang et al., 2020), leveraging pre-trained contextual embeddings from BERT (Devlin et al., 2019).

**中文**

此外，我们的研究的独特之处在于不仅关注检测引用错误，而且积极致力于纠正它们。这种从识别到纠正的转变代表着在提高 RAG 系统中人工智能生成内容的实用性方面向前迈出了重要一步。我们介绍了一系列引文更正方法，包括词汇匹配、混合（词汇+语义）方法和基于 LLM 的轻量级归因。一种方法基于 BERT Score（Zhang 等人，2020），利用 BERT 的预训练上下文嵌入（Devlin 等人，2019）。

### 段落 21 · Page 3

**EN**

Initial experiments with an off-the-shelf model (Beltagy et al., 2020) showed improvements, but fine-tuning on in-domain data yielded better results. This led us to explore ColBERT (Khattab, 2020), a neural retrieval model designed for fine-grained contex- Figure 2: Overview of the workflow of the proposed methods using a sample question. Once the RAG system’s response generating LLM generates an answer, we split the answer into distinct factual points (shown in dotted lines above). For each factual point, we use its similarity scores with the retrieved documents to detect citation errors and correct them. See Section 3 for details.

**中文**

使用现成模型（Beltagy 等人，2020）的初步实验显示出改进，但对域内数据的微调产生了更好的结果。这促使我们探索 ColBERT（Khattab，2020），这是一种专为细粒度上下文设计的神经检索模型 - 图 2：使用示例问题概述所提出方法的工作流程。一旦 RAG 系统的响应生成 LLM 生成答案，我们就把答案分成不同的事实点（如上面的虚线所示）。对于每个事实点，我们使用其与检索到的文档的相似度分数来检测引用错误并进行纠正。详细信息请参见第 3 节。

### 段落 22 · Page 3

**EN**

Question used is for illustration purpose only tual late interaction. By combining BERT Score’s semantic similarity assessment with ColBERT’s fine-tuning capabilities, we developed a more robust and accurate citation correction method, which we detail in the next section. We detail these methods in the next section. 3 Proposed Methodology Our goal is to improve the overall citation accuracy, while having minimal impact on latency and costs. Towards this, we propose a suite of algorithms that leverage various techniques, ranging from simple heuristics to sophisticated machine learning models.

**中文**

使用的问题仅供说明之用，仅供后期互动之用。通过将 BERT Score 的语义相似性评估与 ColBERT 的微调功能相结合，我们开发了一种更稳健、更准确的引文纠正方法，我们将在下一节中详细介绍。我们将在下一节中详细介绍这些方法。 3 提议的方法 我们的目标是提高整体引用准确性，同时对延迟和成本的影响最小。为此，我们提出了一套利用各种技术的算法，从简单的启发式到复杂的机器学习模型。

### 段落 23 · Page 3

**EN**

Our algorithms are streaming-compatible postprocessing techniques, meaning that they operate on an LLM’s response as it is being generated. The general framework of our proposed methods is depicted in Figure 2. We will now go into its details. Let us denote the query that the user asks the RAG system as q. Let the set of documents retrieved by the Retriever module in RAG be {ˆxi}R−1 i=0 . Let A denote the answer generated by the LLM. Our algorithms involve the following steps: 1. We first split the LLM’s responseA into distinct "factual points" {xi}L−1 i=0 .

**中文**

我们的算法是流兼容的后处理技术，这意味着它们在生成法学硕士响应时对其进行操作。我们提出的方法的总体框架如图 2 所示。我们现在将详细介绍它。让我们将用户向 RAG 系统提出的查询表示为 q。令 RAG 中的 Retriever 模块检索到的文档集为 {ˆxi}R−1 i=0。让 A 表示法学硕士生成的答案。我们的算法涉及以下步骤： 1. 我们首先将 LLM 的响应 A 分成不同的“事实点”{xi}L−1 i=0。

### 段落 24 · Page 3

**EN**

A factual point is defined as a section within A that the LLM attributes to a particular set of retrieved documents via citations. In our use case, the LLMs were instructed to include citations at the end of each factual statement in their response. We use simple regular expressions to segment the LLM’s response into "factual points", delimited by citations. See Fig. 2 for example.

**中文**

事实点被定义为 A 中的一个部分，法学硕士通过引用将其归因于一组特定的检索文档。在我们的用例中，法学硕士被要求在其回复中的每个事实陈述的末尾添加引用。我们使用简单的正则表达式将法学硕士的回答分割为“事实点”，并以引文分隔。例如见图2。

### Page 4

### 段落 25 · Page 4

**EN**

2. Let Ci be the number of citations in the LLM’s generated response A for the factual point xi. Our algorithms will estimate the "corrected citations" to be the topCi retrieved documents among {ˆxi}R−1 i=0 that maximize the following similarity metric with the factual point xi: sij = f (xi, ˆxj) (1) In the next sections, we will discuss various choices for the function f in Eq. 1. We will use the following notation: Let us denote each factual point xi as list of its individual tokens tij. Namely, xi = [ti0, ti1, . . . , tik]. Let us also denote each retrieved document ˆxi as a list of its tokens ˆxi = [ˆti0, ˆti1, . . . ,ˆtil].

**中文**

2. 令 Ci 为法学硕士生成的事实点 xi 的答案 A 中的引用次数。我们的算法将估计“更正的引文”为 {ˆxi}R−1 i=0 之间的 topCi 检索文档，最大化以下与事实点 xi 的相似性度量： sij = f (xi, ˆxj) (1) 在接下来的部分中，我们将讨论等式 1 中函数 f 的各种选择。 1. 我们将使用以下符号：让我们将每个事实点 xi 表示为其各个标记 tij 的列表。即 xi = [ti0, ti1, .。。，tik]。我们还将每个检索到的文档 ˆxi 表示为其标记列表 ˆxi = [ˆti0, ˆti1,...。。。，ˆ直到]。

### 段落 26 · Page 4

**EN**

3.1 Keyword based matching We define f in Eq. 1 as the size of the intersection between the tokens in xi and ˆxj. We also tried a term-frequency (TF) by inverse-documentfrequency type of scoring, such as done in traditional document ranking (Rousseau and Vazirgiannis, 2013; Trotman et al., 2014), but it did not yield good results. We noticed regular IDF being particularly noisy with domain specific keywords such as "yield" which have different meaning in agriculture and financial context or "drill" which have different meaning in mining and military context etc.

**中文**

3.1 基于关键词的匹配我们在等式中定义f。 1 作为 xi 和 ˆxj 中标记之间交集的大小。我们还尝试了逆文档频率评分的术语频率 (TF)，例如传统文档排名中的做法（Rousseau 和 Vazirgiannis，2013 年；Trotman 等人，2014 年），但没有产生良好的结果。我们注意到，常规 IDF 对于特定领域的关键字尤其嘈杂，例如“产量”，在农业和金融背景下具有不同含义，或“钻探”在采矿和军事背景等方面具有不同含义。

### 段落 27 · Page 4

**EN**

3.2 Keyword + Semantic Context based matching In this approach, we combine the above keyword match score with a mild contribution from the semantic similarity between the user query q and the retrieved document ˆxi. The motivation is to mildly prefer retrievals that are more relevant to the user query: f (xi, ˆxj) = λ.fkeyword (xi, ˆxj) + (1 − λ).r(q, ˆxj) (2) Where fkeyword (xi, ˆxj) is the keyword based matching score and r(q, ˆxj) is the retrieval score for document ˆxj given query q. We empirically found λ = 0.8 to perform well in our experiments.

**中文**

3.2 基于关键字+语义上下文的匹配 在这种方法中，我们将上述关键字匹配分数与用户查询 q 和检索到的文档 ˆxi 之间的语义相似度的轻微贡献相结合。动机是稍微倾向于与用户查询更相关的检索： f (xi, ˆxj) = λ.fkeyword (xi, ˆxj) + (1 − λ).r(q, ˆxj) (2) 其中 fkeyword (xi, ˆxj) 是基于关键字的匹配得分，r(q, ˆxj) 是给定查询 q 的文档 ˆxj 的检索得分。我们凭经验发现 λ = 0.8 在我们的实验中表现良好。

### 段落 28 · Page 4

**EN**

3.3 BERT Score In the previously discussed approaches, contextual meaning of the words in xi and ˆxj was not fully utilized. They also do not differentiate between cases where word matches occur in close proximity within the reference versus where they are scattered across unrelated positions. Additionally, keywordbased methods struggle to handle scenarios where the language model or response generator paraphrases the words, as these methods rely on exact word matches. BERT Score (Zhang et al., 2020) addresses these limitations by leveraging contextual embeddings to represent the tokens in the factual point xi and the reference ˆxj.

**中文**

3.3 BERT 分数 在前面讨论的方法中，xi 和 ˆxj 中单词的上下文含义没有得到充分利用。它们也不区分单词匹配在参考文献中紧邻出现的情况与分散在不相关位置的情况。此外，基于关键字的方法很难处理语言模型或响应生成器解释单词的场景，因为这些方法依赖于精确的单词匹配。 BERT Score（Zhang et al., 2020）通过利用上下文嵌入来表示事实点 xi 和参考点 ˆxj 中的标记来解决这些限制。

### 段落 29 · Page 4

**EN**

These embeddings are generated using the LongFormer model (Beltagy et al., 2020), which incorporates bi-directional attention to capture not only the token but also its surrounding context. Once the embeddings are computed, the similarity between the factual point and a retrieved document is calculated as follows: For each token in the factual point xi, we compute its maximum similarity among all tokens in the retrieved document. The mean of these maximum similarity scores among all tokens in xi is used as the final score in Eq 1: f (xi, ˆxj) = 1 |xi| X til∈xi max ˆtjk ∈ˆxj e(til)⊤e(ˆtjk ) (3) where e(t) denotes the embedding of a token t.

**中文**

这些嵌入是使用 LongFormer 模型（Beltagy 等人，2020）生成的，该模型结合了双向注意力，不仅可以捕获令牌，还可以捕获其周围的上下文。一旦计算出嵌入，事实点和检索到的文档之间的相似度计算如下：对于事实点 xi 中的每个标记，我们计算其在检索到的文档中的所有标记中的最大相似度。 xi 中所有标记之间的最大相似度得分的平均值用作方程 1 中的最终得分： f (xi, ˆxj) = 1 |xi| X til∈xi max ˆtjk εˆxj e(til)⊤e(ˆtjk ) (3) 其中 e(t) 表示标记 t 的嵌入。

### 段落 30 · Page 4

**EN**

3.4 Fine-tuned Model with Bert Score While off-the-shelf BERTScore models provide a good starting point for incorporating contextual similarity into the citation correction process, we hypothesize that fine-tuning these models specifically for this task on an in-domain dataset can further improve their performance. The key limitation of the off-the-shelf models is that they are not explicitly trained to capture the nuances of citation attribution & factual entailment. Our methodology is motivated by ColBERT (Khattab, 2020).

**中文**

3.4 使用 Bert 分数进行微调的模型 虽然现成的 BERTScore 模型为将上下文相似性纳入引文校正过程提供了一个良好的起点，但我们假设专门针对域内数据集上的此任务微调这些模型可以进一步提高其性能。现成模型的主要限制是它们没有经过明确的训练来捕捉引文归因和事实蕴涵的细微差别。我们的方法论受到 ColBERT (Khattab, 2020) 的启发。

### 段落 31 · Page 4

**EN**

During training, the input to the model is a factual point (x), a positive reference ( ˆx+) that validates the point, and a negative reference (ˆx−) that does not validate the factual point. BERTScore for the factual point, calculated using Eq. 3, is maximized for the positive reference compared to the negative reference. We used cross-entropy loss to increase the score with the positive reference compared to the negative reference. Dataset Preparation: To train the model, we need factual points, and corresponding positive and negative references. We employed an LLM for this, using two strategies: First, for each document in

**中文**

在训练期间，模型的输入是事实点 (x)、验证该点的正参考 (^x+) 和不验证事实点的负参考 (^x−)。事实点的 BERTcore，使用方程式计算。 3、与负参考相比，正参考被最大化。与负参考相比，我们使用交叉熵损失来增加正参考的分数。数据集准备：为了训练模型，我们需要事实点以及相应的正面和负面参考。为此，我们聘请了法学硕士，使用两种策略：首先，对于

### Page 5

### 段落 32 · Page 5

**EN**

the corpus, we determine the nth most similar document using (Amazon-Titan-V2, 2024). We then prompt LLM to provide a factual point present in the former document, but not in the latter. By varying n ∈ { 14, 11, 8, 5, 4, 3}, we get progressively hard positive and negative pairs for training. Secondly, for a list of questions, we generate answers from our RAG-based system. For each factual point present in the answer and for each retrieved document, we employ an LLM to check for if the former is grounded in the latter. We then use this information to create multiple pairs of positivenegative for a given factual point.

**中文**

在语料库中，我们使用 (Amazon-Titan-V2, 2024) 确定第 n 个最相似的文档。然后，我们提示法学硕士提供前一份文件中存在的事实观点，但后者中不存在。通过改变 n ∈ { 14, 11, 8, 5, 4, 3}，我们得到逐渐困难的正负对进行训练。其次，对于问题列表，我们从基于 RAG 的系统生成答案。对于答案中出现的每个事实点以及每个检索到的文档，我们采用法学硕士来检查前者是否以后者为基础​​。然后，我们使用这些信息为给定的事实点创建多对正负值。

### 段落 33 · Page 5

**EN**

This allows us to tune the model specifically for the citations issue for the specific LLM used within the RAG system. 3.5 LLM Based Matching An alternative approach for citation correction is to employ an LLM directly. Table 1 presents results using our best-performing prompt instructions for citation-aware response generation. Here, we explore a secondary LLM that identifies the most relevant reference for each factual point.

**中文**

这使我们能够针对 RAG 系统中使用的特定 LLM 的引文问题专门调整模型。 3.5 基于法学硕士的匹配 另一种引文更正方法是直接采用法学硕士。表 1 显示了使用我们性能最佳的提示指令生成引文感知响应的结果。在这里，我们探索了一个辅助法学硕士，它可以识别每个事实点最相关的参考文献。

### 段落 34 · Page 5

**EN**

To balance accuracy with efficiency, we use a simple prompt that requests only the reference number, avoiding complex techniques like Chain of Thought (CoT) (Wei et al., 2023), which would increase token usage, latency, and cost. This approach leverages the LLM’s ability to capture contextual and semantic nuances beyond keywordbased or rule-based methods, enabling adaptability across domains without explicit rule-crafting or fine-tuning. However, the effectiveness of this method depends on the LLM’s quality, training data, and prompt design.

**中文**

为了平衡准确性和效率，我们使用仅请求参考号的简单提示，避免了思想链 (CoT)（Wei 等人，2023）等复杂技术，这会增加令牌使用、延迟和成本。这种方法利用了法学硕士捕获基于关键字或基于规则的方法之外的上下文和语义细微差别的能力，从而无需明确的规则制定或微调即可实现跨领域的适应性。然而，这种方法的有效性取决于法学硕士的质量、培训数据和提示设计。

### 段落 35 · Page 5

**EN**

Additionally, processing each factual point individually introduces computational overhead, requiring a careful trade-off between cost, latency, and accuracy. 3.6 Reusing Attention Maps of the Base LLM The main idea here is, can we look at the attention maps of the response generating LLM itself to check which retrieved documents were used in generating each factual point in the response. We did not have enough time to fully experiment with this idea, but in Appendix 6.1, we show a simple proof of concept that demonstrates this idea. We will explore this further in our future work.

**中文**

此外，单独处理每个事实点会带来计算开销，需要在成本、延迟和准确性之间进行仔细权衡。 3.6 重用基础 LLM 的注意力图 这里的主要思想是，我们能否查看生成 LLM 本身的响应的注意力图，以检查哪些检索到的文档用于生成响应中的每个事实点。我们没有足够的时间来充分试验这个想法，但在附录 6.1 中，我们展示了一个简单的概念证明来证明这个想法。我们将在未来的工作中进一步探讨这一点。

### 段落 36 · Page 5

**EN**

4 Results In this section, we will present evaluation results of all the proposed methods on top of RAG based system. The evaluations were done by human auditors, who have prior knowledge on the topic for which RAG is used. 4.1 Metrics We developed the following metrics to evaluate RAG system performance. The uber level metric we track is called "Mean Question-Level Accuracy" (MQLA). It combines the following: • Relevancy URL: Checks if the set of citations referenced to by the LLM are relevant to the question. Calculated as the fraction of cited URLs that are relevant.

**中文**

4 结果 在本节中，我们将在基于 RAG 的系统上展示所有提出的方法的评估结果。评估由人工审核员完成，他们对使用 RAG 的主题有先验知识。 4.1 指标 我们开发了以下指标来评估 RAG 系统性能。我们跟踪的超级级别指标称为“平均问题级别准确度”(MQLA)。它结合了以下内容： • 相关性 URL：检查法学硕士引用的引文集是否与问题相关。计算为相关引用 URL 的比例。

### 段落 37 · Page 5

**EN**

• Relevancy Keywords: Checks if keywords in the LLM’s response are relevant to the question. Calculated as the ratio of keywords which are relevant by the total number of keywords present in the query. The keywords in the response are identified by humans. • Relevancy Facts: Checks if facts present in the LLM’s response are relevant to the question. Calculated as the ratio of facts which are relevant to query by the total number of facts present in the response. The facts in the response are identified by humans. • Correctness: Checks if the facts present in the LLM’s response can be verified in the citations provided.

**中文**

• 相关关键词：检查法学硕士回答中的关键词是否与问题相关。计算为相关关键字与查询中存在的关键字总数的比率。响应中的关键字由人类识别。 • 相关事实：检查法学硕士回答中的事实是否与问题相关。计算为与查询相关的事实与响应中存在的事实总数的比率。响应中的事实由人类识别。 • 正确性：检查法学硕士答复中的事实是否可以在所提供的引文中得到验证。

### 段落 38 · Page 5

**EN**

Calculated as the ratio of number of facts supported by cited references and the total number of facts. Note: The facts not supported by cited referenced can be divided into two categories 1) Hallucinated facts and 2) Incorrectly cited facts, based on whether the fact was present in any of the retrieved documents or not. • Completeness: Checks if all aspects (possible sub-questions) of the original questions are addressed in the response. The possible subquestions are identified by the humans. We calculate MQLA as described in Algorithm 1.

**中文**

计算为引用参考文献支持的事实数量与事实总数的比率。注：未引用的参考文献支持的事实可分为两类：1) 幻觉事实和 2) 错误引用的事实，具体取决于该事实是否存在于任何检索到的文档中。 • 完整性：检查原始问题的所有方面（可能的子问题）是否在响应中得到解决。可能的子问题由人类识别。我们按照算法 1 中的描述计算 MQLA。

### 段落 39 · Page 5

**EN**

4.2 Comparing Different Citation Correction Methods In Table 2, we compare different citation correction algorithms proposed in this paper on Model

**中文**

4.2 不同引文更正方法的比较 在表2中，我们在模型上比较了本文提出的不同引文更正算法

### Page 6

### 段落 40 · Page 6

**EN**

Table 2: Comparing Citation Correction Methods.

**中文**

表 2：比较引文更正方法。

### 段落 41 · Page 6

**EN**

All columns except p90 latency show relative performance Citation CorrectionMethod Response GeneratingLLM Mean QuestionLevel AccuracyRelevancy URL% of FactsCorrectly Citedp90 latency perfactual point (in sec)None Model C Base Base Base -Keyword Model C +12.7% -0.9% +12% 0.014Keyword + Semantic Context Model C +15.5% -0.9% +13.6% 0.015BERT Score Model C +2.6% -1% +3.2% 0.389Finetuned BERT Score Model C +15.8% +1.5% +13.7% 0.389LLM Based Matching (Model C) Model C +1.9% +0.9% +7% 1.586None (Baseline) Model A +7.8% +2% +5.4% - Algorithm 1 Mean Question Level Accuracy 1: Initialize totalAccuracy= 0 , n = number of questions 2: for q in questions

**中文**

除 p90 延迟外的所有列均显示相对性能 引文更正方法 响应生成LLM 平均问题级别准确性相关性 URL% 事实正确引用 p90 延迟每事实点（以秒为单位）无 模型 C 基础 基础 基础 - 关键字模型 C +12.7% -0.9% +12% 0.014 关键字 + 语义上下文 模型 C +15.5% -0.9% +13.6% 0.015BERT 分数模型 C +2.6% -1% +3.2% 0.389 微调 BERT 分数模型 C +15.8% +1.5% +13.7% 0.389LLM 基于匹配（模型 C） 模型 C +1.9% +0.9% +7% 1.586 无（基线） 模型 A +7.8% +2% +5.4% - 算法1 平均问题级别准确度 1: 初始化totalAccuracy= 0 , n = 问题数 2: 对于问题中的 q

### 段落 42 · Page 6

**EN**

do 3: Initialize accuracy= 0 4: if all(relevancyUrl, relevancyKeyword, relevancyFacts, correctness, completeness ≥ 0.8) and hallucinatedFacts ≤ 1 then 5: accuracy= 1 6: end if 7: totalAccuracy + = accuracy 8: end for 9: meanAccuracy = totalAccuracy / n 10: return meanAccuracy C’s responses.

**中文**

do 3: 初始化准确度= 0 4: 如果 all(relevancyUrl, relevancyKeyword, relevancyFacts, 正确性, 完整性 ≥ 0.8) 且幻觉事实 ≤ 1 then 5: 准确度= 1 6: 结束 if 7:totalAccuracy + = 准确度 8: 结束 for 9:meanAccuracy =totalAccuracy / n 10: 返回meanAccuracy C 的响应。

### 段落 43 · Page 6

**EN**

We used a set of 50 representative questions for evaluation, incurring an audit time of 2.5 days by 2 humans per row of Table 2. The table includes p90 latency per factual point for each citation correction method, which adds negligible overhead (except LLM method) to our system’s time to first token p90 latency. The latency is computed on g5.4xlarge instance. Results for Model A, a model that is 12x more expensive and about 3x slower are also shown for reference. The impact of our techniques Keyword + Semantic Context based and Fine-tuned BERT Score is evident, taking Model C’s MQLA higher than Model A.

**中文**

我们使用一组 50 个代表性问题进行评估，表 2 中每行 2 人需要 2.5 天的审核时间。该表包括每种引文更正方法的每个事实点的 p90 延迟，这对我们系统的第一个令牌 p90 延迟时间增加了可忽略不计的开销（LLM 方法除外）。延迟是在 g5.4xlarge 实例上计算的。还显示了模型 A 的结果，该模型的价格贵 12 倍，速度慢约 3 倍，以供参考。我们的技术基于关键字+语义上下文和微调的 BERT 分数的影响是显而易见的，模型 C 的 MQLA 高于模型 A。

### 段落 44 · Page 6

**EN**

4.3 Evaluating Impact Across Different LLMs In Table 3, we evaluated the two best performing citation correction methods from Table 2 for four different LLMs (using the same dataset as in Sec. 4.2). Interestingly, different LLMs may pair optimally with different citation correction strategies. The impact of our methods is strongly evident for Model C, Model A and Qwen 2.5 14-B. Model B seems to be inherently much better at citations, but we see some mild improvements in the relevancy of cited URLs when paired with our fine-tuned BERT Score method. These results demonstrate potentially wide applicability of our proposed methods.

**中文**

4.3 评估不同法学硕士的影响 在表 3 中，我们针对四个不同的法学硕士评估了表 2 中表现最佳的两种引文更正方法（使用与第 4.2 节中相同的数据集）。有趣的是，不同的法学硕士可能与不同的引文更正策略进行最佳搭配。我们的方法对模型 C、模型 A 和 Qwen 2.5 14-B 的影响非常明显。模型 B 似乎本质上在引用方面要好得多，但当与我们微调的 BERT 评分方法配合使用时，我们发现被引用 URL 的相关性有一些轻微的改进。这些结果证明了我们提出的方法的潜在广泛适用性。

### 段落 45 · Page 6

**EN**

Table 3: This table shows the effectiveness of our two best citation correction approaches with various LLMs.

**中文**

表 3：该表显示了我们两种最佳引文更正方法对各种法学硕士的有效性。

### 段落 46 · Page 6

**EN**

KSC represents Keyword+Semantic context and FBS represents Finetuned BERT Score ResponseGeneratorCitationCorrectorMQLARelevancyURL % of factsCorrectly CitedModel C None base base baseModel C KSC +15.5% -0.9% +13.6%Model C FBS +15.8% +1.5% +13.7%Model B None +21% +1.5% +14.9%Model B KSC +10.5% +1.5% +10.7%Model B FBS +21% +2% +15%Model A None +7.9% +2% +5.4%Model A KSC +21% -1.3% +16%Model A FBS +10.5% +2% +9.8%Qwen 2.5 14b None +10.5%+2% +8.4%Qwen 2.5 14bKSC 15.8% +2% +9.7%Qwen 2.5 14b FBS 13.1% +1.3% +8.7% 5 Conclusion This paper addresses the critical challenge of citation accuracy in RAG systems, demonstrating its impact across multiple LLMs and its effect on AI-generated content trustworthiness.

**中文**

KSC 代表关键字+语义上下文，FBS 代表微调 BERT 分数响应生成器引用校正器MQLA相关性 URL % 事实正确引用模型 C 无 基础 基础 基础模型 C KSC +15.5% -0.9% +13.6%模型 C FBS +15.8% +1.5% +13.7%模型 B 无 +21% +1.5% +14.9%模型 B KSC +10.5% +1.5% +10.7%B 型 FBS +21% +2% +15%A 型 无 +7.9% +2% +5.4%A 型 KSC +21% -1.3% +16%A 型 FBS +10.5% +2% +9.8%Qwen 2.5 14b 无 +10.5%+2% +8.4%Qwen 2.5 14bKSC 15.8% +2% +9.7%Qwen 2.5 14b FBS 13.1% +1.3% +8.7% 5 结论 本文解决了 RAG 系统中引文准确性的关键挑战，展示了其对多个法学硕士的影响及其对人工智能生成内容可信度的影响。

### 段落 47 · Page 6

**EN**

Our key contribution is the development of efficient postprocessing algorithms for citation correction, improving relative accuracy by up to 15.46% while maintaining minimal computational overhead. Notably, we found that optimal citation correction methods vary across LLMs, emphasizing the importance of model-specific approach selection. Our findings, while promising, represent early steps in addressing this challenge. Future research areas include exploring attention-map-based methods for more precise attributions and developing sophisticated dataset preparation techniques.

**中文**

我们的主要贡献是开发了用于引文校正的高效后处理算法，将相对准确性提高了 15.46%，同时保持了最小的计算开销。值得注意的是，我们发现不同法学硕士的最佳引文更正方法有所不同，这强调了特定模型方法选择的重要性。我们的研究结果虽然很有希望，但代表了应对这一挑战的早期步骤。未来的研究领域包括探索基于注意力图的方法以实现更精确的归因，并开发复杂的数据集准备技术。

### 段落 48 · Page 6

**EN**

While newer LLMs (Model B) have improved citation accuracy, attribution issues persist to a lesser extent, suggesting the need for more sophisticated correction algorithms. Additionally, our framework’s ability to establish relationships between factual points and source documents opens up interesting applications, such as determining appropriate contexts for content insertion (e.g., advertisement placement) based on document similarity and factual relevance.

**中文**

虽然较新的法学硕士（模型 B）提高了引文准确性，但归因问题在较小程度上仍然存在，这表明需要更复杂的校正算法。此外，我们的框架在事实点和源文档之间建立关系的能力开辟了有趣的应用，例如根据文档相似性和事实相关性确定内容插入的适当上下文（例如广告投放）。

### Page 7

### 段落 49 · Page 7

**EN**

References Amazon-Titan-V2. 2024. Amazon titan foundation models. Accessed: 2025-01-15. Patrice Béchard and Orlando Marquez Ayala. 2024. Reducing hallucination in structured outputs via retrieval-augmented generation. arXiv preprint arXiv:2404.08189. Iz Beltagy, Matthew E. Peters, and Arman Cohan. 2020. Longformer: The long-document transformer. Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. 2019. Bert: Pre-training of deep bidirectional transformers for language understanding. Tianyu Gao, Howard Yen, Jiatong Yu, and Danqi Chen. 2023a. Enabling large language models to generate text with citations.

**中文**

参考文献 Amazon-Titan-V2。 2024 年。亚马逊泰坦基金会模特。访问时间：2025 年 1 月 15 日。帕特里斯·贝查德和奥兰多·马克斯·阿亚拉。 2024.通过检索增强生成减少结构化输出中的幻觉。 arXiv 预印本 arXiv：2404.08189。伊兹·贝尔塔吉 (Iz Beltagy)、马修·E·彼得斯 (Matthew E. Peters) 和阿曼·科汉 (Arman Cohan)。 2020.Longformer：长文档转换器。雅各布·德夫林、张明伟、肯顿·李和克里斯蒂娜·图塔诺娃。 2019. Bert：用于语言理解的深度双向Transformer的预训练。高天宇、甄子丹、于佳桐和陈丹琪。 2023a。使大型语言模型能够生成带有引文的文本。

### 段落 50 · Page 7

**EN**

arXiv preprint arXiv:2305.14627. Tianyu Gao, Howard Yen, Jiatong Yu, and Danqi Chen. 2023b. Enabling large language models to generate text with citations. In Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, pages 6465–6488, Singapore. Association for Computational Linguistics. Tianyu Gao, Howard Yen, Jiatong Yu, and Danqi Chen. 2023c. Enabling large language models to generate text with citations. Or Honovich, Roee Aharoni, Jonathan Herzig, Hagai Taitelbaum, Doron Kukliansy, Vered Cohen, Thomas Scialom, Idan Szpektor, Avinatan Hassidim, and Yossi Matias. 2022.

**中文**

arXiv 预印本 arXiv：2305.14627。高天宇、甄子丹、于佳桐和陈丹琪。 2023b。使大型语言模型能够生成带有引文的文本。 2023 年自然语言处理经验方法会议论文集，第 6465-6488 页，新加坡。计算语言学协会。高天宇、甄子丹、于佳桐和陈丹琪。 2023c。使大型语言模型能够生成带有引文的文本。或者 Honovich、Roee Aharoni、Jonathan Herzig、Hagai Taitelbaum、Doron Kukliansy、Vered Cohen、Thomas Scialom、Idan Szpektor、Avinatan Hassidim 和 Yossi Matias。 2022 年。

### 段落 51 · Page 7

**EN**

True: Re-evaluating factual consistency evaluation. I Hsu, Zifeng Wang, Long T Le, Lesly Miculicich, Nanyun Peng, Chen-Yu Lee, Tomas Pfister, et al. 2024. Calm: Contrasting large and small language models to verify grounded generation. arXiv preprint arXiv:2406.05365. Chengyu Huang, Zeqiu Wu, Yushi Hu, and Wenya Wang. 2024. Training language models to generate text with citations via fine-grained rewards. Ziwei Ji, Nayeon Lee, Rita Frieske, Tiezheng Yu, Dan Su, Yan Xu, Etsuko Ishii, Ye Jin Bang, Andrea Madotto, and Pascale Fung. 2023. Survey of hallucination in natural language generation. ACM Computing Surveys, 55(12):1–38.

**中文**

True：重新评估事实一致性评估。 I Hsu、Zifeng Wang、Long T Le、Lesly Miculicich、Nanyun Peng、Chen-Yu Lee、Tomas Pfister 等。 2024. Calm：对比大小语言模型来验证接地生成。 arXiv 预印本 arXiv：2406.05365。黄成宇、吴泽秋、胡雨诗和王文雅。 2024 年。训练语言模型通过细粒度奖励生成带有引用的文本。 Ziwei Ji、Nayeon Lee、Rita Frieske、Tiezheng Yu、Dan Su、Yan Xu、Etsuko Ishii、Ye Jin Bang、Andrea Madotto 和 Pascale Fung。 2023.自然语言生成中的幻觉调查。 ACM 计算调查，55(12)：1–38。

### 段落 52 · Page 7

**EN**

Urvashi Khandelwal, Omer Levy, Dan Jurafsky, Luke Zettlemoyer, and Mike Lewis. 2019. Generalization through memorization: Nearest neighbor language models. arXiv preprint arXiv:1911.00172. Omar Khattab. 2020. Colbert: Efficient and effective passage search via contextualized late interaction over bert. Xinze Li, Yixin Cao, Liangming Pan, Yubo Ma, and Aixin Sun. 2024. Towards verifiable generation: A benchmark for knowledge-aware language model attribution. Nelson F. Liu, Tianyi Zhang, and Percy Liang. 2023. Evaluating verifiability in generative search engines.

**中文**

乌尔瓦希·坎德尔瓦尔、奥马尔·利维、丹·尤拉夫斯基、卢克·泽特尔莫耶和迈克·刘易斯。 2019.通过记忆进行泛化：最近邻语言模型。 arXiv 预印本 arXiv：1911.00172。奥马尔·哈塔布。 2020. Colbert：通过 bert 上的上下文化后期交互进行高效且有效的段落搜索。李新泽、曹一新、潘良明、马玉波、孙爱新。 2024.迈向可验证的一代：知识感知语言模型归因的基准。纳尔逊·F·刘、张天一和梁珀西。 2023.评估生成式搜索引擎的可验证性。

### 段落 53 · Page 7

**EN**

Chaitanya Malaviya, Subin Lee, Sihao Chen, Elizabeth Sieber, Mark Yatskar, and Dan Roth. 2024. Expertqa: Expert-curated questions and attributed answers. Reiichiro Nakano, Jacob Hilton, Suchir Balaji, Jeff Wu, Long Ouyang, Christina Kim, Christopher Hesse, Shantanu Jain, Vineet Kosaraju, William Saunders, Xu Jiang, Karl Cobbe, Tyna Eloundou, Gretchen Krueger, Kevin Button, Matthew Knight, Benjamin Chess, and John Schulman. 2022. Webgpt: Browserassisted question-answering with human feedback. Perplexity AI. 2024. Perplexity AI: AI-powered search engine. Accessed: November 21, 2024. Vipula Rawte, S.

**中文**

Chaitanya Malaviya、Subin Lee、Sihao Chen、Elizabeth Sieber、Mark Yatskar 和 Dan Roth。 2024. Expertqa：专家策划的问题和归因答案。 Reiichiro Nakano、Jacob Hilton、Sucher Balaji、Jeff Wu、Long Ouyang、Christina Kim、Christopher Hesse、Shantanu Jain、Vineet Kosaraju、William Saunders、徐江、Karl Cobbe、Tyna Eloundou、Gretchen Krueger、Kevin Button、Matthew Knight、Benjamin Chess 和 John Schulman。 2022.Webgpt：浏览器辅助问答与人类反馈。困惑人工智能。 2024. Perplexity AI：人工智能驱动的搜索引擎。访问日期：2024 年 11 月 21 日。Vipula Rawte, S.

### 段落 54 · Page 7

**EN**

M Towhidul Islam Tonmoy, Krishnav Rajbangshi, Shravani Nag, Aman Chadha, Amit P. Sheth, and Amitava Das. 2024. Factoid: Factual entailment for hallucination detection. François Rousseau and Michalis Vazirgiannis. 2013. Composition of tf normalizations: new insights on scoring functions for ad hoc ir. In Proceedings of the 36th international ACM SIGIR conference on Research and development in information retrieval, pages 917–920. Kurt Shuster, Spencer Poff, Moya Chen, Douwe Kiela, and Jason Weston. 2021. Retrieval augmentation reduces hallucination in conversation. arXiv preprint arXiv:2104.07567.

**中文**

M Towhidul Islam Tonmoy、Krishnav Rajbangshi、Shravani Nag、Aman Chadha、Amit P. Sheth 和 Amitava Das。 2024. Factoid：幻觉检测的事实蕴涵。弗朗索瓦·卢梭和米哈利斯·瓦齐吉安尼斯。 2013. tf 标准化的组成：对 ad hoc IR 评分函数的新见解。第 36 届国际 ACM SIGIR 信息检索研究与开发会议记录，第 917-920 页。库尔特·舒斯特、斯宾塞·波夫、莫雅·陈、杜威·基拉和杰森·韦斯顿。 2021. 检索增强减少了对话中的幻觉。 arXiv 预印本 arXiv：2104.07567。

### 段落 55 · Page 7

**EN**

Maojia Song, Shang Hong Sim, Rishabh Bhardwaj, Hai Leong Chieu, Navonil Majumder, and Soujanya Poria. 2024. Measuring and enhancing trustworthiness of llms in rag through grounded attributions and learning to refuse. Hao Sun, Hengyi Cai, Bo Wang, Yingyan Hou, Xiaochi Wei, Shuaiqiang Wang, Yan Zhang, and Dawei Yin. 2024. Towards verifiable text generation with evolving memory and self-reflection. Andrew Trotman, Antti Puurula, and Blake Burgess. 2014. Improvements to bm25 and language models examined. In Proceedings of the 19th Australasian Document Computing Symposium, pages 58–65.

**中文**

Maojia Song、Shang Hong Sim、Rishabh Bhardwaj、Hai Leong Chieu、Navonil Majumder 和 Soujanya Poria。 2024. 通过扎根归因和学习拒绝来衡量和增强 rag 中的 LLMS 的可信度。孙浩、蔡恒逸、王波、侯英艳、魏晓池、王帅强、张岩和尹大伟。 2024 年。通过不断发展的记忆和自我反思来生成可验证的文本。安德鲁·特罗特曼、安蒂·普鲁拉和布莱克·伯吉斯。 2014 年。检查了 bm25 和语言模型的改进。第 19 届澳大利亚文档计算研讨会论文集，第 58-65 页。

### 段落 56 · Page 7

**EN**

Jason Wei, Xuezhi Wang, Dale Schuurmans, Maarten Bosma, Brian Ichter, Fei Xia, Ed Chi, Quoc Le, and Denny Zhou. 2023. Chain-of-thought prompting elicits reasoning in large language models. Xiang Yue, Boshi Wang, Ziru Chen, Kai Zhang, Yu Su, and Huan Sun. 2023. Automatic evaluation of attribution by large language models. Tianyi Zhang, Varsha Kishore, Felix Wu, Kilian Q. Weinberger, and Yoav Artzi. 2020. Bertscore: Evaluating text generation with bert.

**中文**

Jason Wei、王学智、Dale Schuurmans、Maarten Bosma、Brian Ichter、Fei Xia、Ed Chi、Quoc Le 和 Denny Zhou。 2023. 思维链提示引发大型语言模型的推理。向月、王博士、陈自如、张凯、苏宇和孙焕。 2023.大型语言模型的归因自动评估。张天一、Varsha Kishore、Felix Wu、Kilian Q. Weinberger 和 Yoav Artzi。 2020. Bertscore：使用 bert 评估文本生成。

### Page 8

### 段落 57 · Page 8

**EN**

Figure 3: Visualisation of Attention Score. See Appendix 6.1 for details. 6 Appendix 6.1 Using Attention map for attribution In a RAG based system, the response generating LLM is given a set of relevant document in response to a user query. It then understands information from these different documents to answer the question at hand. Here, we want to explore if can we leverage attention scores within the LLM to understand which document in the prompt it is focusing on while generating a particular fact in its response. We did a small toy experiment with Qwen 2.5B - 2B to test the same.

**中文**

图 3：注意力分数的可视化。详见附录6.1。 6 附录 6.1 使用注意力图进行归因 在基于 RAG 的系统中，生成 LLM 的响应会得到一组相关文档以响应用户查询。然后它从这些不同的文档中理解信息来回答当前的问题。在这里，我们想探讨是否可以利用 LLM 中的注意力分数来了解其关注提示中的哪个文档，同时在其响应中生成特定事实。我们用 Qwen 2.5B - 2B 做了一个小玩具实验来测试同样的情况。

### 段落 58 · Page 8

**EN**

We use the below prompt: Hi , you are an assistant who has access to the following < documents > about cricket . Please answer the < user query > at the end using only the information provided in the < documents >. Do not output any information not contained in the < documents >. Do not output any information that is not relevant to answering the < user query >. If the < user query > cannot be answered with the given < documents > , please say so . < documents > <doc > Axx is a tall batsman . </ doc > <doc > Byy can bat with a broken bat as well . </ doc > <doc > Czz is a very funny umpire . </ doc > <doc > Dii is a fast bowler from Mumbai .

**中文**

我们使用以下提示：嗨，您是一名助理，可以访问以下有关板球的<文档>。请仅使用<文档>中提供的信息回答最后的<用户查询>。不输出<文档>中未包含的任何信息。不要输出任何与回答<用户查询>无关的信息。如果给定的<文档>无法回答<用户查询>，请说明。 <文档> <文档> Axx 是一名高个子击球手。 </doc> <doc>Byy 也可以用破损的球棒击球。 </doc> <doc> Czz 是一位非常有趣的裁判。 </doc> <doc> Dii 是来自孟买的快速投球手。

### 段落 59 · Page 8

**EN**

</ doc > </ documents > < user query > QUESTION </ user query > We asked the following questions to the LLM: • Name a batsman who is not particularly short • Name a batsman who can bat with a damaged bat • Name an umpire who makes people smile • Who is a player from Mumbai? and visualised the attention scores in 3 (Blue, Orange, Green and Red lines for the above four questions respectively). The x-axis in the figure is the token position within the prompt. The y-axis is the sum of the attentions scores for all tokens in the output, across all layers of the LLM at that particular input token location.

**中文**

</ doc > </ 文件> < 用户查询> 问题</ 用户查询> 我们向法学硕士提出了以下问题： • 一位不是特别矮的击球手的名字 • 一位可以用损坏的球棒击球的击球手的名字 • 一位让人微笑的裁判的名字 • 谁是来自孟买的球员？并可视化 3 中的注意力分数（蓝线、橙线、绿线和红线分别对应上述四个问题）。图中的 x 轴是提示中的标记位置。 y 轴是输出中所有标记的注意力分数的总和，跨越 LLM 在该特定输入标记位置的所有层。

### 段落 60 · Page 8

**EN**

A higher value of this sum at a particular location of the input token indicates that that input token was taken into account by the LLM in generating the response. You will see that for first question the peak of attention score is before the second question which is in line with where the necessary information is present in the prompt. Likewise, the peak of attention for second question is before the third one, and so on. This small proof of concept shows that we may be able to leverage the LLM’s internal attention maps to correct citations.

**中文**

输入令牌特定位置处的总和值较高，表示 LLM 在生成响应时考虑了该输入令牌。您将看到，对于第一个问题，注意力分数的峰值位于第二个问题之前，这与提示中出现的必要信息一致。同样，第二个问题的注意力高峰在第三个问题之前，依此类推。这个小小的概念证明表明，我们也许能够利用法学硕士的内部注意力图来纠正引用。
