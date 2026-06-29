# Learning to Rank for Multiple Retrieval-Augmented Models through Iterative Utility Feedback

- ID: 82
- 类型: pdf
- 分类: 04_academic_papers
- 主题: ranking optimization for RAG agents
- 原文链接: https://arxiv.org/pdf/2410.09942
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

arXiv:2410.09942v2 [cs.CL] 26 Jun 2025 Learning to Rank for Multiple Retrieval-Augmented Models through Iterative Utility Maximization Alireza Salemi University of Massachusetts Amherst Amherst, MA, United States asalemi@cs.umass.edu Hamed Zamani University of Massachusetts Amherst Amherst, MA, United States zamani@cs.umass.edu ABSTRACT This paper investigates the design of a unified search engine to serve multiple retrieval-augmented generation (RAG) agents, each with a distinct task, backbone large language model (LLM), and RAG strategy.

**中文**

arXiv:2410.09942v2 [cs.CL] 2025 年 6 月 26 日通过迭代效用最大化学习对多个检索增强模型进行排名 Alireza Salemi 马萨诸塞大学阿默斯特美国马萨诸塞州 asalemi@cs.umass.edu Hamed Zamani 马萨诸塞大学阿默斯特美国马萨诸塞州 zamani@cs.umass.edu摘要 本文研究了统一搜索引擎的设计，以服务于多个检索增强生成 (RAG) 代理，每个代理都有不同的任务、骨干大语言模型 (LLM) 和 RAG 策略。

### 段落 2 · Page 1

**EN**

We introduce an iterative approach where the search engine generates retrieval results for the RAG agents and gathers feedback on the quality of the retrieved documents during an offline phase. This feedback is then used to iteratively optimize the search engine using an expectation-maximization algorithm, with the goal of maximizing each agent’s utility function. Additionally, we adapt this to an online setting, allowing the search engine to refine its behavior based on real-time individual agents feedback to better serve the results for each of them.

**中文**

我们引入了一种迭代方法，其中搜索引擎为 RAG 代理生成检索结果，并在离线阶段收集有关检索文档质量的反馈。然后，该反馈用于使用期望最大化算法迭代优化搜索引擎，目标是最大化每个代理的效用函数。此外，我们将其适应在线设置，允许搜索引擎根据实时个体代理反馈来完善其行为，以更好地为每个代理提供结果。

### 段落 3 · Page 1

**EN**

Experiments on datasets from the Knowledge-Intensive Language Tasks (KILT) benchmark demonstrates that our approach significantly on average outperforms baselines across 18 RAG models. We demonstrate that our method effectively “personalizes” the retrieval for each RAG agent based on the collected feedback. Finally, we provide a comprehensive ablation study to explore various aspects of our method. CCS CONCEPTS •Information systems → Learning to rank; Personalization; •Computing methodologies → Natural language generation.

**中文**

对知识密集型语言任务 (KILT) 基准数据集进行的实验表明，我们的方法平均显着优于 18 个 RAG 模型的基线。我们证明，我们的方法根据收集的反馈有效地“个性化”每个 RAG 代理的检索。最后，我们提供了全面的消融研究来探索我们方法的各个方面。 CCS 概念 •信息系统→学习排名；个性化； •计算方法→自然语言生成。

### 段落 4 · Page 1

**EN**

KEYWORDS Retrieval-augmented generation; retrieval-enhanced machine learning; search engine for agents; ranking optimization ACM Reference Format: Alireza Salemi and Hamed Zamani. 2025. Learning to Rank for Multiple Retrieval-Augmented Models through Iterative Utility Maximization. In Proceedings of the 2025 International ACM SIGIR Conference on Innovative Concepts and Theories in Information Retrieval (ICTIR) (ICTIR ’25), July 18, 2025, Padua, Italy. ACM, New York, NY, USA, 12 pages. https://doi.org/10.

**中文**

关键词 检索增强生成；检索增强的机器学习；代理商搜索引擎；排名优化 ACM 参考格式：Alireza Salemi 和 Hamed Zamani。 2025。通过迭代效用最大化学习对多个检索增强模型进行排名。 2025 年国际 ACM SIGIR 信息检索创新概念和理论 (ICTIR) 会议 (ICTIR ’25) 会议记录，2025 年 7 月 18 日，意大利帕多瓦。 ACM，美国纽约州纽约市，12 页。 https://doi.org/10。

### 段落 5 · Page 1

**EN**

1145/3731120.3744584 1 INTRODUCTION Search engines have been designed mainly to serve people by providing relevant results for search queries. They are typically trained Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. Copyrights for components of this work owned by others than ACM must be honored. Abstracting with credit is permitted.

**中文**

1145/3731120.3744584 1 简介 搜索引擎的设计主要是通过为搜索查询提供相关结果来为人们服务。他们通常接受过培训，允许免费制作全部或部分作品的数字或硬拷贝以供个人或课堂使用，前提是制作或分发副本不是为了盈利或商业利益，并且副本在首页上附有此通知和完整引用。必须尊重 ACM 以外的其他人拥有的本作品组件的版权。允许以信用方式提取。

### 段落 6 · Page 1

**EN**

To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee. Request permissions from permissions@acm.org. ICTIR ’25, July 18, 2025, Padua, Italy © 2025 Association for Computing Machinery. ACM ISBN 979-8-4007-1861-8/2025/07. . . $15.00 https://doi.org/10.1145/3731120.3744584 at scale using learning-to-rank methods with implicit feedback gathered and refined over time through user interactions [11, 17, 18]. These systems often use personalization to deliver more tailored and effective search results for users [5, 48].

**中文**

要以其他方式复制、重新发布、发布到服务器上或重新分发到列表，需要事先获得特定许可和/或付费。从permissions@acm.org 请求权限。 ICTIR '25，2025 年 7 月 18 日，意大利帕多瓦 © 2025 计算机协会。 ACM ISBN 979-8-4007-1861-8/2025/07。。。 15.00 美元 https://doi.org/10.1145/3731120.3744584 使用学习排序方法大规模使用，并通过用户交互随着时间的推移收集和完善隐式反馈[11,17,18]。这些系统通常使用个性化为用户提供更加定制和有效的搜索结果 [5, 48]。

### 段落 7 · Page 1

**EN**

With the recent rise of large language models (LLMs), along with their user-friendly chat interfaces, many users now use them for a wide range of tasks [4]. Extensive studies have shown that LLMs often face challenges in tasks that require external knowledge in rapidly changing or evolving environments [32, 62]. One method to address this limitation is to enhance LLMs by retrieving information from a knowledge source, a technique known as retrieval-augmented generation (RAG) [3, 15, 27].

**中文**

随着大型语言模型 (LLM) 的兴起及其用户友好的聊天界面，许多用户现在将它们用于各种任务 [4]。广泛的研究表明，法学硕士经常面临在快速变化或不断发展的环境中需要外部知识的任务的挑战[32, 62]。解决这一限制的一种方法是通过从知识源检索信息来增强法学硕士，这种技术称为检索增强生成（RAG）[3,15,27]。

### 段落 8 · Page 1

**EN**

This marks a paradigm shift in the current landscape, where humans interact primarily with LLMs, while LLMs rely on search engines to retrieve external information [21, 45, 62]. With this paradigm shift, it is crucial to develop methods for optimizing and personalizing search engines to better serve their new users: the LLMs that depend on them. This need is further highlighted by prior work showing significant differences between the information preferences of humans and RAG agents [ 44]. In addition, different LLMs may have different information needs.

**中文**

这标志着当前格局的范式转变，人类主要与法学硕士互动，而法学硕士依靠搜索引擎检索外部信息[21,45,62]。随着这种范式的转变，开发优化和个性化搜索引擎的方法至关重要，以更好地服务于新用户：依赖于他们的法学硕士。先前的研究进一步强调了这一需求，显示人类和 RAG 智能体的信息偏好之间存在显着差异 [44]。此外，不同的法学硕士可能有不同的信息需求。

### 段落 9 · Page 1

**EN**

For example, smaller LMs with limited reasoning capabilities might prefer supporting documents that provide explicit information, while more powerful LLMs can infer details even when the information is stated vaguely. Given these variations, optimizing engines to address the unique requirements of different LLMs is essential. Prior work on RAG mostly focus on developing a RAG system (i.e., a retrieval and a language model) for each task. The recent work by Salemi and Zamani[45] represents one of the first efforts to build a centralized search engine capable of serving multiple RAG agents, each tasked with a distinct objective.

**中文**

例如，推理能力有限的较小的法学硕士可能更喜欢提供明确信息的支持文档，而更强大的法学硕士可以推断细节，即使信息表述模糊。鉴于这些变化，优化引擎以满足不同法学硕士的独特要求至关重要。之前关于 RAG 的工作主要集中在为每个任务开发 RAG 系统（即检索和语言模型）。 Salemi 和 Zamani [45] 最近的工作代表了构建能够为多个 RAG 代理提供服务的集中式搜索引擎的首批努力之一，每个 RAG 代理都有不同的目标。

### 段落 10 · Page 1

**EN**

These agents utilize different underlying LLMs and employ varying RAG techniques. To train this centralized search engine, they use its initial parameters to retrieve documents for the training queries of the agents (i.e., the LLMs utilizing the search engine). The feedback from these agents on the retrieved documents is then collected to update the parameters. This approach has a few limitations. First, it depends heavily on the initial parameters to retrieve documents for training queries. If these parameters are not well-initialized, the quality of the initial retrieval lists would be low, leading to suboptimal feedback from the LLMs.

**中文**

这些代理利用不同的底层 LLM 并采用不同的 RAG 技术。为了训练这个集中式搜索引擎，他们使用其初始参数来检索文档以用于代理的训练查询（即利用搜索引擎的法学硕士）。然后收集这些代理对检索到的文档的反馈以更新参数。这种方法有一些局限性。首先，它在很大程度上取决于初始参数来检索训练查询的文档。如果这些参数没有很好地初始化，初始检索列表的质量将会很低，导致法学硕士的反馈不理想。

### 段落 11 · Page 1

**EN**

Furthermore, since the initial documents are retrieved without any prior feedback to adapt the search engine to agent needs, they may not be relevant or useful to the agents. Consequently, the feedback provided might not reflect useful documents for the individual agents, reducing the overall effectiveness of the training process. This paper addresses these limitations by introducing an iterative approach grounded in strong theoretical foundations, designed

**中文**

此外，由于初始文档是在没有任何事先反馈以使搜索引擎适应代理需求的情况下检索的，因此它们可能与代理不相关或无用。因此，提供的反馈可能无法反映对各个代理有用的文档，从而降低了培训过程的整体有效性。本文通过引入基于强大理论基础的迭代方法来解决这些局限性，设计

### Page 2

### 段落 12 · Page 2

**EN**

ICTIR ’25, July 18, 2025, Padua, Italy Alireza Salemi and Hamed Zamani to maximize the utility functions of RAG agents. Feedback is collected over multiple iterations in an offline training procedure to progressively optimize the search engine. In each iteration, the search engine applies the parameters optimized from the previous feedback round to retrieve new documents tailored to the specific information needs of each RAG agent. Feedback on these newly retrieved documents is then collected to refine the search engine’s understanding of each agent’s preferences.

**中文**

ICTIR ’25，2025 年 7 月 18 日，意大利帕多瓦 Alireza Salemi 和 Hamed Zamani 旨在最大化 RAG 代理的效用函数。在离线训练过程中通过多次迭代收集反馈，以逐步优化搜索引擎。在每次迭代中，搜索引擎应用从前一轮反馈中优化的参数来检索适合每个 RAG 代理的特定信息需求的新文档。然后收集对这些新检索到的文档的反馈，以完善搜索引擎对每个代理偏好的理解。

### 段落 13 · Page 2

**EN**

The personalization process adapts the search engine for each RAG agent by leveraging feedback from the prior iteration, using the agents’ training queries and feedback on them. During the offline phase, feedback from all agents is aggregated to train a multi-task central search engine capable of effectively serving the diverse needs of all agents. A natural extension to the offline optimization phase is online learning in the serving phase where the retriever provides search results for the agents on test queries.

**中文**

个性化过程通过利用先前迭代的反馈、代理的训练查询和反馈来调整每个 RAG 代理的搜索引擎。在离线阶段，来自所有代理的反馈被汇总，以训练能够有效满足所有代理的不同需求的多任务中央搜索引擎。离线优化阶段的自然延伸是服务阶段的在线学习，其中检索器为测试查询的代理提供搜索结果。

### 段落 14 · Page 2

**EN**

Here, the same iterative algorithm is applied to adapt the retriever based on agent feedback obtained during active serving sessions. Specifically, the retriever first processes a batch of queries from an agent, collects feedback on these queries, and then updates its parameters to improve performance on subsequent queries within the same session for this specific agent. This optimization occurs concurrently with the serving process and is not confined to pre-defined training queries.

**中文**

这里，应用相同的迭代算法来根据活动服务会话期间获得的代理反馈来调整检索器。具体来说，检索器首先处理来自代理的一批查询，收集这些查询的反馈，然后更新其参数以提高该特定代理的同一会话内后续查询的性能。这种优化与服务过程同时发生，并且不限于预定义的训练查询。

### 段落 15 · Page 2

**EN**

Since this optimization leverages each agent’s feedback individually to further optimize itself, it enhances the personalization of the search engine for that specific agent even more, tailoring the system to better meet the unique information needs of each agent. We evaluate our approach using diverse tasks from the Knowledge- Intensive Language Tasks (KILT) benchmark [32]. Our evaluation includes three open-domain question answering datasets: Natural Questions (NQ) [24], TriviaQA [19], and HotPotQA [60]; one fact verification dataset: FEVER [53]; and two relation extraction and slot-filling datasets: zsRE [25] and T-REx [9].

**中文**

由于这种优化单独利用每个代理的反馈来进一步优化自身，因此它进一步增强了该特定代理的搜索引擎的个性化，定制系统以更好地满足每个代理的独特信息需求。我们使用知识密集型语言任务（KILT）基准[32]中的不同任务来评估我们的方法。我们的评估包括三个开放域问答数据集：Natural Questions (NQ) [24]、TriviaQA [19] 和 HotPotQA [60]；一个事实验证数据集：FEVER [53]；以及两个关系提取和槽填充数据集：zsRE [25] 和 T-REx [9]。

### 段落 16 · Page 2

**EN**

Following Salemi and Zamani [45], we test our approach with 18 different RAG agents as the users, each performing a specific task and utilizing distinct augmentation approaches and LLMs, to serve as users of the search engine. Our results demonstrate that the proposed approach for offline iterative training of the search engine significantly outperforms the state-of-the-art baseline. Additionally, combining this offline approach with our online learning yields an even greater improvement over the baselines.

**中文**

继 Salemi 和 Zamani [45] 之后，我们用 18 个不同的 RAG 代理作为用户来测试我们的方法，每个代理执行特定的任务并利用不同的增强方法和 LLM，作为搜索引擎的用户。我们的结果表明，所提出的搜索引擎离线迭代训练方法明显优于最先进的基线。此外，将这种离线方法与我们的在线学习相结合，可以比基线产生更大的改进。

### 段落 17 · Page 2

**EN**

We also conduct an extensive ablation study on various configurations of the proposed approaches to provide further insights into their effectiveness and impact. Furthermore, we show that our approach enhances the personalization of the search engine over time, addressing a limitation noted in Salemi and Zamani [45]. We observe that the correlation between the retrieval results of the agents employing different LLMs but performing the same task is very low, indicating that the results are effectively personalized. To support future research, we have open-sourced our code and models for the community.

**中文**

我们还对所提出方法的各种配置进行了广泛的消融研究，以进一步了解其有效性和影响。此外，我们表明，随着时间的推移，我们的方法增强了搜索引擎的个性化，解决了 Salemi 和 Zamani [45] 中指出的限制。我们观察到，采用不同法学硕士但执行相同任务的代理的检索结果之间的相关性非常低，表明结果是有效个性化的。为了支持未来的研究，我们向社区开源了我们的代码和模型。

### 段落 18 · Page 2

**EN**

1 2 RELATED WORK Knowledge-Intensive Language Tasks (KILT) . Contrary to standard NLP tasks like natural language understanding [55, 56] and question answering [29], where the input alone is enough to 1Our code can be found at: https://github.com/alirezasalemi7/uRAG perform the task, knowledge-intensive NLP tasks rely heavily on external knowledge sources to extract necessary information. Petroni et al. [32] introduces KILT, a benchmark designed for evaluating such tasks.

**中文**

1 2 相关工作知识密集型语言任务 (KILT)。与自然语言理解 [55, 56] 和问题回答 [29] 等标准 NLP 任务相反，仅输入就足以 1 我们的代码可以在以下位置找到：https://github.com/alirezasalemi7/uRAG 执行任务，知识密集型 NLP 任务严重依赖外部知识源来提取必要的信息。彼得罗尼等人。 [32] 引入了 KILT，这是一个为评估此类任务而设计的基准。

### 段落 19 · Page 2

**EN**

KILT encompasses a variety of tasks, including opendomain question answering, fact verification, slot filling, and entity linking, providing a benchmark for knowledge-intensive tasks. Retrieval-Augmented Generation (RAG). RAG [27] represents a framework that merges information retrieval with natural language generation to improve the quality of generated outputs by integrating external knowledge in the generation process [3, 51]. Unlike traditional LLMs that rely solely on pre-trained knowledge, RAG can dynamically retrieve information from external sources via a retriever, enabling them to produce content that is more accurate [21, 62].

**中文**

KILT 涵盖了多种任务，包括开放域问答、事实验证、槽填充和实体链接，为知识密集型任务提供了基准。检索增强生成（RAG）。 RAG [27] 代表了一个将信息检索与自然语言生成相结合的框架，通过在生成过程中集成外部知识来提高生成输出的质量 [3, 51]。与仅依赖预先训练的知识的传统法学硕士不同，RAG 可以通过检索器从外部源动态检索信息，使他们能够生成更准确的内容 [21, 62]。

### 段落 20 · Page 2

**EN**

This flexibility allows RAG to be applied in various domains, including knowledge grounding in textual [ 15, 27, 32] and multimodal [6, 10, 37, 42], personalization [23, 38–41, 43], and reducing hallucinations [2, 47]. The retriever in RAG plays a pivotal role as it sources the necessary information for the LLM to perform its task [ 27]. This is typically done using either sparse retrieval methods (e.g., TF-IDF, BM25 [35]) or dense retrieval models (e.g., DPR [20], Contriever [13], ColBERTv2 [46], E5 [58]). The retrieved information is then utilized by the large language model to complete the task.

**中文**

这种灵活性使得 RAG 能够应用于各个领域，包括文本知识基础 [15,27,32] 和多模态知识基础 [6,10,37,42]，个性化 [23,38–41,43]，以及减少幻觉 [2,47]。 RAG 中的检索器起着关键作用，因为它为 LLM 提供执行其任务所需的信息 [27]。这通常是使用稀疏检索方法（例如 TF-IDF、BM25 [35]）或密集检索模型（例如 DPR [20]、Contriever [13]、ColBERTv2 [46]、E5 [58]）来完成。然后，大型语言模型利用检索到的信息来完成任务。

### 段落 21 · Page 2

**EN**

Prominent methods in this context include In-Prompt Augmentation (IPA) and Fusion-in-Decoder (FiD) [15]. In IPA, the retrieved data is appended to the prompt, allowing the language model to incorporate it during generation. FiD encodes each retrieved document separately alongside the prompt within the encoder of an encoder-decoder architecture, combining them in the decoder to generate a cohesive answer based on the available information, as explained in Izacard and Grave [15]. A Search Engine for Machines. Research on search engines show that successful systems rely on large-scale feedback for optimization [1, 54].

**中文**

这方面的著名方法包括即时增强（IPA）和解码器融合（FiD）[15]。在 IPA 中，检索到的数据被附加到提示中，允许语言模型在生成过程中合并它。 FiD 对每个检索到的文档与编码器-解码器架构的编码器内的提示一起进行单独编码，在解码器中将它们组合起来，根据可用信息生成一个有凝聚力的答案，如 Izacard 和 Grave [15] 中所述。机器搜索引擎。对搜索引擎的研究表明，成功的系统依赖于大规模反馈来进行优化 [1, 54]。

### 段落 22 · Page 2

**EN**

With LLMs as the primary users of search engines [21, 62], Salemi and Zamani [44] showed that the LLMs’ preferences about relevance of a query and document differs from humans. Salemi and Zamani [45] introduced a new problem that is training a unified search engine capable of serving multiple diverse RAG agents. They introduced uRAG, a unified ranking model designed to serve multiple RAG models while learning and optimizing based on feedback provided by these diverse RAG models.

**中文**

由于法学硕士是搜索引擎的主要用户 [21, 62]，Salemi 和 Zamani [44] 表明法学硕士对查询和文档相关性的偏好与人类不同。 Salemi 和 Zamani [45] 引入了一个新问题，即训练能够为多个不同的 RAG 代理提供服务的统一搜索引擎。他们推出了 uRAG，这是一种统一的排名模型，旨在为多个 RAG 模型提供服务，同时根据这些不同的 RAG 模型提供的反馈进行学习和优化。

### 段落 23 · Page 2

**EN**

Recently, several methods have been proposed for training retrieval models tailored to LLMs, including distillation from LLMs to retrievers [14, 16, 59], end-toend training of retrievers and LLMs [36, 61], and bandit algorithms [57]. However, most of these approaches focus on leveraging feedback from a single LLM, with the aim of aligning the retrieval with that particular LLM [45]. Here, we introduce an approach based on iterative utility maximization to train a unified retrieval model for serving multiple RAG agents, applied in both offline and online settings [7, 12] to optimize the search engine for the agents.

**中文**

最近，已经提出了几种针对 LLM 的训练检索模型的方法，包括从 LLM 到检索器的蒸馏 [14,16,59]、检索器和 LLM 的端到端训练 [36, 61] 以及 bandit 算法 [57]。然而，这些方法大多数都侧重于利用单个法学硕士的反馈，目的是使检索与特定的法学硕士保持一致[45]。在这里，我们引入了一种基于迭代效用最大化的方法来训练为多个 RAG 代理提供服务的统一检索模型，应用于离线和在线设置 [7, 12]，以优化代理的搜索引擎。

### 段落 24 · Page 2

**EN**

3 PROBLEM FORMULATION Consider the retrieval model 𝑅𝜃 , parameterized by 𝜃, whose main role is to facilitate information access from a corpus 𝐶 for a set of RAG models (a.k.a, RAG agents) denoted as 𝑀 = {𝑀𝑖 }𝑛 𝑖=1. Each 𝑀𝑖 acts as a black-box agent for𝑅𝜃 , which means that𝑅𝜃 does not have

**中文**

3 问题表述考虑由 𝜃 参数化的检索模型 𝑅𝜃，其主要作用是促进一组 RAG 模型（也称为 RAG 代理）从语料库 𝐶 访问信息，表示为 𝑀 = {𝑀𝑖 }𝑛 𝑖=1。每个𝑀𝑖充当𝑅𝜃的黑盒代理，这意味着𝑅𝜃没有

### Page 3

### 段落 25 · Page 3

**EN**

Learning to Rank for Multiple Retrieval-Augmented Models through Iterative Utility Maximization ICTIR ’25, July 18, 2025, Padua, Italy Figure 1: Iterative Utility Maximization ( IUM). This framework first iteratively trains the search engine with feedback from all agents offline, then individually iteratively trains and serves the model for each agent during the online phase. access to the models’ architecture, configuration, or parameters. Each 𝑀𝑖 is designed to perform a knowledge-intensive task 𝑇𝑖 = (𝐷train 𝑖 , 𝐷test 𝑖 , 𝜇𝑖 ) that requires external information from the corpus 𝐶 as the knowledge source.

**中文**

通过迭代效用最大化学习对多个检索增强模型进行排名 ICTIR ’25，2025 年 7 月 18 日，意大利帕多瓦 图 1：迭代效用最大化 (IUM)。该框架首先利用所有离线代理的反馈迭代训练搜索引擎，然后在在线阶段单独迭代训练并为每个代理提供模型。访问模型的架构、配置或参数。每个 𝑀𝑖 被设计用来执行知识密集型任务 𝑇𝑖 = (𝐷train 𝑖 , 𝐷test 𝑖 , 𝜇𝑖 )，需要来自语料库 𝐶 的外部信息作为知识源。

### 段落 26 · Page 3

**EN**

There is a training dataset 𝐷train 𝑖 = {(𝑥 𝑗 , 𝑦𝑗 )} |𝐷train 𝑖 | 𝑗=1 for each agent 𝑀𝑖, which can be used by the retrieval model 𝑅𝜃 for offline optimization. At inference, each agent 𝑀𝑖 operates sequentially on a test dataset 𝐷test 𝑖 = {(𝑥 ′ 𝑗 , 𝑦′ 𝑗 )} |𝐷test 𝑖 | 𝑗=1 in the same order. The end-to-end performance of the agent𝑀𝑖 can be measured by a utility function (metric) 𝜇𝑖. Each RAG agent can be simply formulated as ¯𝑦𝑀𝑖 = 𝑀𝑖 (𝑥; 𝑅𝜃 ).

**中文**

有一个训练数据集 𝐷train 𝑖 = {(𝑥 𝑗 , 𝑦𝑗 )} |𝐷train 𝑖 |每个代理𝑀𝑖𝑗=1，可以被检索模型𝑅𝜃用于离线优化。在推理时，每个代理 𝑀𝑖 按顺序对测试数据集 𝐷test 𝑖 = {(𝑥 ′ 𝑗 , 𝑦′ 𝑗 )} |𝐷test 𝑖 | 进行操作。 𝑗=1 同样的顺序。代理𝑀𝑖的端到端性能可以通过效用函数（度量）𝜇𝑖来衡量。每个 RAG 代理都可以简单地表示为 ¯𝑦𝑀𝑖 = 𝑀𝑖 (𝑥; 𝑅𝜃 )。

### 段落 27 · Page 3

**EN**

In more detail, given an input 𝑥, each RAG agent 𝑀𝑖 submits a query to the retrieval model 𝑅𝜃 for information access, and generates the output by consuming the top 𝑘 retrieved documents (i.e., R𝑘 = {𝑟1, ..., 𝑟𝑘 }). As suggested in [45], the search engine and RAG agents can engage in an offline optimization process, in which each RAG agent 𝑀𝑖 produces a feedback list for a retrieval list of size 𝑘, denoted as 𝑓𝑀𝑖 = {𝑓𝑗 }𝑘 𝑗=1 ∈ { 0, 1}1×𝑘. This feedback list indicates the usefulness of each retrieved document in the retrieval list from the agent’s perspective.

**中文**

更详细地说，给定输入 𝑥，每个 RAG 代理𝑀𝑖 向检索模型𝑅𝜃 提交查询以进行信息访问，并通过消耗顶部 𝑘 检索到的文档来生成输出（即，R𝑘 = {𝑟1, ..., 𝑟𝑘 }）。正如[45]中所建议的，搜索引擎和RAG代理可以参与离线优化过程，其中每个RAG代理𝑀𝑖为大小为𝑘的检索列表生成反馈列表，表示为𝑓𝑀𝑖 = {𝑓𝑗}𝑘𝑗=1 ∈ { 0, 1}1×𝑘。该反馈列表表明从代理的角度来看检索列表中每个检索到的文档的有用性。

### 段落 28 · Page 3

**EN**

Feedback can be computed in various ways; based on the performance of the generated output when utilizing the retrieved documents on the downstream task, e.g., using the utility function 𝜇𝑖, or based on ratings received from the users or evaluators of the RAG agent, among other methods. Without loss of generality, this paper focuses on the first case as the main method for providing feedback from the agents. In this approach, feedback is based on the agent’s downstream performance when it uses each document individually in its task.

**中文**

反馈可以通过多种方式计算；基于在下游任务中使用检索到的文档时生成的输出的性能，例如使用效用函数𝜇𝑖，或者基于从 RAG 代理的用户或评估者收到的评级等。不失一般性，本文重点关注第一种情况，作为提供代理反馈的主要方法。在这种方法中，反馈基于代理在任务中单独使用每个文档时的下游性能。

### 段落 29 · Page 3

**EN**

Therefore, the main goal of this paper is to optimize the retrieval model 𝑅𝜃 to maximize the the expected utility for all the RAG agents that use the retrieval model. 4 LEARNING TO RANK WITH ITERATIVE UTILITY MAXIMIZATION State-of-the-art commercial search engines have been trained using implicit feedback from their users, such as clicks, scrolling behavior, and dwell time [11, 17, 18]. In our setting, however, the primary users of the search engine are the RAG agents that consume the retrieval results. Therefore, their feedback on the quality of the retrieval results serves as the primary signal for optimizing the search engine.

**中文**

因此，本文的主要目标是优化检索模型𝑅𝜃，以最大化所有使用该检索模型的 RAG 代理的预期效用。 4 学习通过迭代效用最大化进行排名 最先进的商业搜索引擎已经使用来自用户的隐式反馈进行了训练，例如点击、滚动行为和停留时间[11,17,18]。然而，在我们的设置中，搜索引擎的主要用户是使用检索结果的 RAG 代理。因此，他们对检索结果质量的反馈是优化搜索引擎的主要信号。

### 段落 30 · Page 3

**EN**

Previous work [45] has explored the use of this feedback to train the model, where they employed the initial parameters of the search engine—without any prior training—to retrieve a set of documents and collect feedback for them in an offline setting to optimize the search engine. This approach has several shortcomings. First, using an untrained retrieval model to gather documents for feedback collection is suboptimal. If the parameters are not well-initialized, the quality of the initial document retrievals would be low, leading to a feedback collection process that may not yield relevant documents.

**中文**

之前的工作 [45] 探索了使用这种反馈来训练模型，他们使用搜索引擎的初始参数（无需任何事先训练）来检索一组文档并在离线设置中收集它们的反馈以优化搜索引擎。这种方法有几个缺点。首先，使用未经训练的检索模型来收集文档以进行反馈收集并不是最理想的。如果参数没有很好地初始化，初始文档检索的质量将会很低，导致反馈收集过程可能无法产生相关文档。

### 段落 31 · Page 3

**EN**

Consequently, the model might easily learn to distinguish these poorly retrieved documents from relevant ones, resulting in an inadequately trained search engine. Furthermore, since the initial documents are retrieved without any prior feedback to adapt the search engine to each agent’s information needs, they may not be relevant or useful to the agents. Additionally, relying solely on offline feedback collection limits the system, as it does not allow for continuous adaptation and improvement of the retrieval model based on real-time interactions.

**中文**

因此，该模型可能很容易学会将这些检索不佳的文档与相关文档区分开来，从而导致搜索引擎训练不充分。此外，由于初始文档的检索没有任何事先反馈以使搜索引擎适应每个代理的信息需求，因此它们可能与代理无关或无用。此外，仅仅依靠离线反馈收集会限制系统，因为它不允许基于实时交互的检索模型的持续适应和改进。

### 段落 32 · Page 3

**EN**

Implementing an online learning approach could address these issues by enabling the model to update its parameters incrementally during serving phase as new feedback is collected. This would allow the system to continuously refine its retrieval strategies, adjusting to the evolving information needs of each agent, improving personalization of the search engine for each agent. We addresses the aforementioned issues by introducing the Iterative Utility Maximization ( IUM) framework for training the retrieval model.

**中文**

实施在线学习方法可以通过使模型在服务阶段随着收集新反馈而逐步更新其参数来解决这些问题。这将使系统能够不断完善其检索策略，适应每个代理不断变化的信息需求，提高每个代理的搜索引擎的个性化。我们通过引入迭代效用最大化（IUM）框架来训练检索模型来解决上述问题。

### 段落 33 · Page 3

**EN**

This framework optimizes the retrieval model with the feedback collected from all agents during an offline phase, and it incorporates each agent’s specific feedback during an online phase, all in an iterative manner to maximizes the probability of receiving positive feedback for each served query, as shown in Figure 1. 4.1 Offline Ranking Optimization through Iterative Utility Maximization Similar to self-training of LLMs using self-generated data [ 49], we define a optimality binary variable 𝑜, where 𝑝 (𝑜 = 1|R𝑘, 𝑥) ∝ 𝑓𝑀𝑖 (R𝑘, 𝑥), meaning that variable 𝑜 = 1 indicates positive feedback and 𝑜 = 0 indicates negative feedback.

**中文**

该框架利用离线阶段从所有代理收集的反馈来优化检索模型，并结合每个代理在在线阶段的具体反馈，所有这些都以迭代的方式最大化接收每个服务查询的正反馈的概率，如图 1 所示。 4.1 通过迭代效用最大化进行离线排名优化 与使用自生成数据的 LLM 自我训练类似[49]，我们定义了一个最优二元变量 𝑜，其中𝑝 (𝑜 = 1|R𝑘, 𝑥) ∝ 𝑓𝑀𝑖 (R𝑘, 𝑥)，意味着变量 𝑜 = 1 表示正反馈，𝑜 = 0 表示负反馈。

### 段落 34 · Page 3

**EN**

Here, R𝑘 is a retrieved list of 𝑘 documents, and 𝑓𝑀𝑖 (R𝑘, 𝑥) represents the feedback for the retrieved list R𝑘 given input 𝑥 from the RAG agent 𝑀𝑖. The main goal is to maximize log-likelihood of observing 𝑜 = 1 for a given input 𝑥. Since in this process the retrieved documents affect the variable 𝑜, we can rewrite the log-likelihood as: log 𝑝 (𝑜 = 1|𝑥) =

**中文**

这里，R𝑘 是检索到的 𝑘 文档列表，𝑓𝑀𝑖 (R𝑘, 𝑥) 表示给定来自 RAG 代理𝑀𝑖 的输入 𝑥 的检索列表 R𝑘 的反馈。主要目标是最大化给定输入 𝑥 观察到 𝑜 = 1 的对数似然。由于在此过程中检索到的文档会影响变量 𝑜，因此我们可以将对数似然重写为： log 𝑝 (𝑜 = 1|𝑥) =

### Page 4

### 段落 35 · Page 4

**EN**

ICTIR ’25, July 18, 2025, Padua, Italy Alireza Salemi and Hamed Zamani logÍ R𝑘 ∈𝜋𝑘 (𝐶 ) 𝑝𝜃 (R𝑘 |𝑥)𝑝 (𝑜 = 1|𝑥, R𝑘 ), where 𝜋𝑘 (𝐶) denotes all permutations of 𝑘 documents being selected from the corpus𝐶. The summation over all possible retrieval lists R𝑘 is computationally expensive for a large corpus, 2 making the calculation infeasible. Instead of directly maximizing log 𝑝 (𝑜 = 1|𝑥), one can maximize its Evidence Lower Bound (ELBO), denoted as 𝐿(𝑝𝜃 , 𝑞), with respect to the retriever’s parameters𝜃 and a variational distribution 𝑞(R𝑘 |𝑥).

**中文**

ICTIR ’25，2025 年 7 月 18 日，意大利帕多瓦 Alireza Salemi 和 Hamed Zamani logÍ R𝑘 ε𝜋𝑘 (𝐶 ) 𝑝𝜃 (R𝑘 |𝑥)𝑝 (𝑜 = 1|𝑥, R𝑘 )，其中 𝜋𝑘 (𝐶) 表示从语料库𝐶中选择的𝑘文档的所有排列。对于大型语料库，所有可能的检索列表 R𝑘 的求和在计算上是昂贵的，2 使得计算不可行。与直接最大化 log 𝑝 (𝑜 = 1|𝑥) 不同，我们可以相对于检索器的参数 𝜃 和变分分布 𝑞(R𝑘 |𝑥) 最大化其证据下界 (ELBO)，表示为 𝐿(𝑝𝜃 , 𝑞)。

### 段落 36 · Page 4

**EN**

The variational distribution is used to approximate the latent variable R𝑘 distributions, simplifying and making the computation more efficient. Since 𝐿(𝑝𝜃 , 𝑞) is a lower bound for log 𝑝 (𝑜 = 1|𝑥), maximizing ELBO ensures increase in log 𝑝 (𝑜 = 1|𝑥).

**中文**

变分分布用于近似潜在变量 R𝑘 分布，简化计算并提高计算效率。由于 𝐿(𝑝𝜃 , 𝑞) 是 log 𝑝 (𝑜 = 1|𝑥) 的下界，因此最大化 ELBO 可确保 log 𝑝 (𝑜 = 1|𝑥) 的增加。

### 段落 37 · Page 4

**EN**

Formally: log𝑝 (𝑜 = 1|𝑥) = log ∑︁ R𝑘 ∈𝜋𝑘 (𝐶 ) 𝑝𝜃 (R𝑘 |𝑥)𝑝 (𝑜 = 1|𝑥, R𝑘 ) × 𝑞(R𝑘 |𝑥) 𝑞(R𝑘 |𝑥) = log E R𝑘 ∼𝑞 ( R𝑘 |𝑥 )  𝑝 (𝑜 = 1|𝑥, R𝑘 )𝑝𝜃 (R𝑘 |𝑥) 𝑞(R𝑘 |𝑥)  ≥ E R𝑘 ∼𝑞 ( R𝑘 |𝑥 )  log 𝑝 (𝑜 = 1|𝑥, R𝑘 )𝑝𝜃 (R𝑘 |𝑥) 𝑞(R𝑘 |𝑥)  (Jensen’s ineq.) = −𝐷KL [𝑞(R𝑘 |𝑥)|| 𝑝 (𝑜 = 1|𝑥, R𝑘 )𝑝𝜃 (R𝑘 |𝑥)] = E R𝑘 ∼𝑞 ( R𝑘 |𝑥 ) [log 𝑝 (𝑜 = 1|𝑥, R𝑘 )] − 𝐷KL [𝑞(R𝑘 |𝑥)|| 𝑝𝜃 (R𝑘 |𝑥)] ≕ 𝐿(𝑝𝜃 , 𝑞) (1) where 𝐷KL denotes the Kullback-Leibler divergence between the two given distributions. Thus, we show that log 𝑝 (𝑜 = 1|𝑥) ≥ 𝐿(𝑝𝜃 , 𝑞), which means that maximizing 𝐿(𝑝𝜃 , 𝑞) results in increasing the lower bound of log 𝑝 (𝑜 = 1|𝑥).

**中文**

形式为： log𝑝 (𝑜 = 1|𝑥) = log Σ︁ R𝑘 ε𝜋𝑘 (𝐶 ) 𝑝𝜃 (R𝑘 |𝑥)𝑝 (𝑜 = 1|𝑥, R𝑘 ) × 𝑞(R𝑘 |𝑥) 𝑞(R𝑘 |𝑥) = log E R𝑘 ∼𝑞 ( R𝑘 |𝑥 ) 𝑝 (𝑜 = 1|𝑥, R𝑘 )𝑝𝜃 (R𝑘 |𝑥) 𝑞(R𝑘 |𝑥) ≥ E R𝑘 ∼𝑞 ( R𝑘 |𝑥 ) log 𝑝 (𝑜 = 1|𝑥, R𝑘 )𝑝𝜃 (R𝑘 |𝑥) 𝑞(R𝑘 |𝑥) (Jensen 不等式) = −𝐷KL [𝑞(R𝑘) |𝑥)|| 𝑝 (𝑜 = 1|𝑥, R𝑘 )𝑝𝜃 (R𝑘 |𝑥)] = E R𝑘 ∼𝑞 ( R𝑘 |𝑥 ) [log 𝑝 (𝑜 = 1|𝑥, R𝑘 )] − 𝐷KL [𝑞(R𝑘 |𝑥)|| 𝑝𝜃 (R𝑘 |𝑥)] ≕ 𝐿(𝑝𝜃 , 𝑞) (1) 其中 𝐷KL 表示两个给定分布之间的 Kullback-Leibler 散度。因此，我们证明 log 𝑝 (𝑜 = 1|𝑥) ≥ 𝐿(𝑝𝜃 , 𝑞)，这意味着最大化 𝐿(𝑝𝜃 , 𝑞) 会导致增加 log 𝑝 (𝑜 = 1|𝑥) 的下限。

### 段落 38 · Page 4

**EN**

To maximize 𝐿(𝑝𝜃 , 𝑞), we utilize an Expectation-Maximization (EM) algorithm as follows. Expectation Step (𝑞𝑡 +1 = arg max𝑞 𝐿(𝑝𝜃 𝑡 , 𝑞)): Maximizing 𝑞 is considered the Expectation step since it involves finding the distribution 𝑞 that best approximates the true posterior distribution of the latent variable R𝑘. Considering the formulation in Equation 1, where 𝐿(𝑝𝜃 , 𝑞) = −𝐷KL [𝑞(R𝑘 |𝑥)|| 𝑝 (𝑜 = 1|𝑥, R𝑘 )𝑝𝜃 𝑡 (R𝑘 |𝑥)], it implies that maximum of 𝐿(𝑝𝜃 , 𝑞) occurs when 𝑞𝑡 +1 = 𝑝 (𝑜 = 1|𝑥, R𝑘 )𝑝𝜃 𝑡 (R𝑘 |𝑥), because the KL divergence is non-negative and equals to zero when the given two distributions are identical.

**中文**

为了最大化 𝐿(𝑝𝜃 , 𝑞)，我们使用期望最大化 (EM) 算法，如下所示。期望步骤 (𝑞𝑡 +1 = arg max𝑞 𝐿(𝑝𝜃 𝑡 , 𝑞))：最大化 𝑞 被认为是期望步骤，因为它涉及找到最接近潜在变量 R𝑘 真实后验分布的分布 𝑞。考虑等式 1 中的公式，其中 𝐿(𝑝𝜃 , 𝑞) = −𝐷KL [𝑞(R𝑘 |𝑥)|| 𝑝 (𝑜 = 1|𝑥, R𝑘 )𝑝𝜃 𝑡 (R𝑘 |𝑥)]，这意味着当 𝑞𝑡 +1 = 𝑝 (𝑜 = 1|𝑥) 时，出现 𝐿(𝑝𝜃 , 𝑞) 的最大值， R𝑘 )𝑝𝜃 𝑡 (R𝑘 |𝑥)，因为当给定的两个分布相同时，KL 散度是非负的并且等于零。

### 段落 39 · Page 4

**EN**

Maximization Step (𝜃𝑡 +1 = arg max𝜃 𝐿(𝑝𝜃 , 𝑞𝑡 +1)): The goal of this step is to update the model parameters by maximizing the expected log-likelihood computed in the Expectation step, thereby fit the model to the observed data.

**中文**

最大化步骤 (𝜃𝑡 +1 = arg max𝜃 𝐿(𝑝𝜃 , 𝑞𝑡 +1))：此步骤的目标是通过最大化期望步骤中计算的期望对数似然来更新模型参数，从而使模型适合观测数据。

### 段落 40 · Page 4

**EN**

We re-write this step as: 𝜃𝑡 +1 = arg max 𝜃 𝐿(𝑝𝜃 , 𝑞𝑡 +1) = arg max 𝜃 −𝐷KL [𝑞𝑡 +1|| 𝑝𝜃 (R𝑘 |𝑥)] = arg max 𝜃 ∑︁ R𝑘 𝑞𝑡 +1 log 𝑝𝜃 (R𝑘 |𝑥) = arg max 𝜃 ∑︁ R𝑘 𝑝 (𝑜 = 1|𝑥, R𝑘 )𝑝𝜃 𝑡 (R𝑘 |𝑥) log 𝑝𝜃 (R𝑘 |𝑥) = arg max 𝜃 E R𝑘 ∼𝑝𝜃𝑡 ( R𝑘 |𝑥 ) [𝑝 (𝑜 = 1|𝑥, R𝑘 ) log 𝑝𝜃 (R𝑘 |𝑥)] (2) Since feedback in our case is non-negative, as assumed in Section 3, and 𝑝 (𝑜 = 1|𝑥, R𝑘 ) ∝ 𝑓𝑀𝑖 (R𝑘, 𝑥), the final objective function 2In our case, the corpus contains approximately 36 million document chunks.

**中文**

我们将这一步重写为： 𝜃𝑡 +1 = arg max 𝜃 𝐿(𝑝𝜃 , 𝑞𝑡 +1) = arg max 𝜃 −𝐷KL [𝑞𝑡 +1|| 𝑝𝜃 (R𝑘 |𝑥)] = arg 最大值 𝜃 Σ︁ R𝑘 𝑞𝑡 +1 log 𝑝𝜃 (R𝑘 |𝑥) = arg 最大值 𝜃 Σ︁ R𝑘 𝑝 (𝑜 = 1|𝑥, R𝑘) )𝑝𝜃 𝑡 (R𝑘 |𝑥) log 𝑝𝜃 (R𝑘 |𝑥) = arg max 𝜃 E R𝑘 ∼𝑝𝜃𝑡 ( R𝑘 |𝑥 ) [𝑝 (𝑜 = 1|𝑥, R𝑘 ) log 𝑝𝜃 (R𝑘 |𝑥)] (2) 由于我们案例中的反馈是非负的，如第 3 节中所假设的，并且 𝑝 (𝑜 = 1|𝑥, R𝑘 ) ∝ 𝑓𝑀𝑖 (R𝑘, 𝑥)，最终目标函数 2 在我们的案例中，语料库包含大约3600 万个文档块。

### 段落 41 · Page 4

**EN**

considering all agents to get updated parameters 𝜃𝑡 +1 is defined as: arg max 𝜃 E 𝑀𝑖 ∼𝑀 " E 𝑥∼𝐷train 𝑖 " E R𝑘 ∼𝑝𝜃𝑡 ( R𝑘 |𝑥 )  𝑓𝑀𝑖 (R𝑘, 𝑥) log 𝑝𝜃 (R𝑘 |𝑥)  ## (3) where the retrieval lists are sampled from the parameters of the retrieval model in the previous iteration ( R𝑘 ∼ 𝑝𝜃 𝑡 (R𝑘 |𝑥)). As noted by Salemi and Zamani [44], gathering agent’s feedback for an entire ranked list is computationally expensive, and collecting feedback on a per-document basis is more efficient. Additionally, Singh et al. [50]emphasize the difficulty of calculating a retrieval list probabilities.

**中文**

考虑所有智能体来获取更新参数 𝜃𝑡 +1 定义为： arg max 𝜃 E 𝑀𝑖 ∼𝑀 " E 𝑥∼𝐷train 𝑖 " E R𝑘 ∼𝑝𝜃𝑡 ( R𝑘 |𝑥 ) 𝑓𝑀𝑖 (R𝑘, 𝑥) log 𝑝𝜃 (R𝑘 |𝑥) ## (3) 其中检索列表是从上一次迭代中检索模型的参数中采样的 (R𝑘 ∼ 𝑝𝜃 𝑡 (R𝑘 |𝑥))。正如 Salemi 和 Zamani [44] 所指出的，收集代理对整个排名列表的反馈在计算上是昂贵的，并且在每个文档的基础上收集反馈效率更高。此外，辛格等人。 [50]强调计算检索列表概率的困难。

### 段落 42 · Page 4

**EN**

To simplify this, we instead use a pointwise ranking objective function [28] using the same technique. To implement this approach, two adjustments are needed: First, for pointwise learning-to-rank, sampling should be based on the probabilities of the documents, which can be approximated by their relevance to the query. Let 𝑝𝜃 𝑡 (𝑅 = 1|𝑥, 𝑑) represent the probability that document 𝑑 is relevant to query 𝑥. We assume that the more relevant a document is to a query, the higher its probability. Therefore, we have: 𝑝∗ 𝜃 𝑡 (𝑑 |𝑥) ∝ 𝑝𝜃 𝑡 (𝑅 = 1|𝑥, 𝑑).

**中文**

为了简化这一点，我们使用相同的技术使用逐点排名目标函数 [28]。为了实现这种方法，需要进行两项调整：首先，对于逐点学习排序，采样应该基于文档的概率，可以通过它们与查询的相关性来近似。令 𝑝𝜃 𝑡 (𝑅 = 1|𝑥, 𝑑) 表示文档 𝑑 与查询 𝑥 相关的概率。我们假设文档与查询越相关，其概率就越高。因此，我们有： 𝑝* 𝜃 𝑡 (𝑑 |𝑥) ∝ 𝑝𝜃 𝑡 (𝑅 = 1|𝑥, 𝑑)。

### 段落 43 · Page 4

**EN**

Additionally, we assume that any documents outside the top 𝑘, ranked by 𝑝𝜃 𝑡 (𝑅 = 1|𝑥, 𝑑), have a probability of zero. Thus, sampling from the retrieval list R𝑘 can be approximated by selecting the top 𝑘 documents based on 𝑝∗ 𝜃 𝑡 (𝑑 |𝑥) ∝ 𝑝𝜃 𝑡 (𝑅 = 1|𝑥, 𝑑). The second adjustment is that the objective function should aim to maximize the probability of documents that receive positive feedback. Thus, we can reformulate the problem by using the feedback as a relevance label, training the model to classify whether a document is relevant or not.

**中文**

此外，我们假设任何位于顶部 𝑘 之外、按 𝑝𝜃 𝑡 (𝑅 = 1|𝑥, 𝑑) 排序的文档的概率为零。因此，可以通过基于 𝑝* 𝜃 𝑡 (𝑑 |𝑥) ∝ 𝑝𝜃 𝑡 (𝑅 = 1|𝑥, 𝑑) 选择顶部 𝑘 文档来近似从检索列表 R𝑘 中进行采样。第二个调整是目标函数应该旨在最大化文档收到积极反馈的概率。因此，我们可以通过使用反馈作为相关性标签来重新表述问题，训练模型来对文档是否相关进行分类。

### 段落 44 · Page 4

**EN**

We can define the final objective to get updated parameters 𝜃𝑡 +1 as: arg max 𝜃 E 𝑀𝑖 ∼𝑀 " E 𝑥∼𝐷train 𝑖 " E 𝑑∼𝑝∗ 𝜃𝑡 (𝑑 |𝑥 )  log 𝑝𝜃 (𝑅 = 𝑓𝑀𝑖 (𝑑, 𝑥)| 𝑥, 𝑑)  ## (4) Training Procedure: To train the retrieval model 𝑅𝜃 , we assume 𝑇 expectation and maximization iterations are performed. In each iteration, the RAG agents submit their training queries to the retrieval model, which then provides them with the top results based on the given query from the corpus𝐶. In response, the agents return feedback per retrieved document.

**中文**

我们可以将获得更新参数 𝜃𝑡 +1 的最终目标定义为： arg max 𝜃 E 𝑀𝑖 ∼𝑀 " E 𝑥∼𝐷train 𝑖 " E 𝑑∼𝑝* 𝜃𝑡 (𝑑 |𝑥 ) log 𝑝𝜃 (𝑅 = 𝑓𝑀𝑖 (𝑑, 𝑥)| 𝑥, 𝑑) ## (4) 训练过程：为了训练检索模型 𝑅𝜃，我们假设执行𝑇 期望和最大化迭代。在每次迭代中，RAG 代理将其训练查询提交给检索模型，然后检索模型根据语料库中的给定查询为它们提供最佳结果。作为响应，代理返回每个检索到的文档的反馈。

### 段落 45 · Page 4

**EN**

After collecting feedback from all agents, the search engine enters an optimization phase where Equation 4 is used to optimize the model based on the provided feedback. This procedure is shown in Algorithm 1.

**中文**

在收集所有代理的反馈后，搜索引擎进入优化阶段，其中使用公式 4 根据提供的反馈来优化模型。该过程如算法 1 所示。

### Page 5

### 段落 46 · Page 5

**EN**

Learning to Rank for Multiple Retrieval-Augmented Models through Iterative Utility Maximization ICTIR ’25, July 18, 2025, Padua, Italy Algorithm 1 The Offline IUM algorithm.

**中文**

通过迭代效用最大化学习对多个检索增强模型进行排名 ICTIR ’25，2025 年 7 月 18 日，意大利帕多瓦 算法 1 离线 IUM 算法。

### 段落 47 · Page 5

**EN**

Initialize the retrieval model from a pretrained encoder checkpoint for 𝑡 = 1 to 𝑇 do 𝐷𝑡 = {} for 𝑀𝑖 in 𝑀 do for 𝑥 in 𝐷𝑖 do Retrieve 𝑘 docs from corpus 𝐶 by 𝑅𝜃 𝑡 : 𝑟 = 𝑅𝜃 𝑡 (𝑥, 𝐶, 𝑘) Collect feedback of agent 𝑀𝑖 for list 𝑟: 𝑓𝑖 = 𝑓𝑀𝑖 (𝑑𝑖, 𝑥) Add feedback to iteration𝑡 dataset: 𝐷𝑡 = 𝐷𝑡 ∪{( 𝑥, 𝑑𝑖, 𝑓𝑖 )} end for end for 𝜃𝑡 +1 = arg max𝜃 E(𝑥,𝑑,𝑓 )∼𝐷𝑡 [log 𝑝𝜃 (𝑅 = 𝑓 |𝑥, 𝑑)] end for 4.2 Online Ranking Optimization through Iterative Utility Maximization In the previous subsection,𝑅𝜃 collects feedback from all RAG agents on their respective training sets in an offline, iterative fashion, and uses their feedback for optimizing its parameters.

**中文**

从预训练编码器检查点初始化检索模型，从 𝑡 = 1 到 𝑇 do 𝐷𝑡 = {} for 𝑀𝑖 in 𝑀 do for 𝑥 in 𝐷𝑖 do Retrieve 𝑘 docs from corpus 𝐶 by 𝑅𝜃 𝑡 : 𝑟 = 𝑅𝜃 𝑡 (𝑥, 𝐶, 𝑘) 收集代理𝑀𝑖对列表𝑟的反馈： 𝑓𝑖 = 𝑓𝑀𝑖 (𝑑𝑖, 𝑥) 将反馈添加到迭代𝑡数据集： 𝐷𝑡 = 𝐷𝑡 ∪{( 𝑥, 𝑑𝑖, 𝑓𝑖 )} 端到端𝜃𝑡 +1 = arg max𝜃 E(𝑥,𝑑,𝑓 )∼𝐷𝑡 [log 𝑝𝜃 (𝑅 = 𝑓) |𝑥, 𝑑)] 4.2 通过迭代效用最大化进行在线排名优化 在上一小节中，𝑅𝜃 以离线、迭代的方式收集所有 RAG 代理关于其各自训练集的反馈，并使用他们的反馈来优化其参数。

### 段落 48 · Page 5

**EN**

However, this approach is not feasible during the serving phase3 for several reasons. First, rapid access to information is necessary for the serving phase, since agents cannot afford to wait for feedback to be collected from all other agents. Additionally, offline optimization methods typically require access to the complete set of queries for effective optimization, which is not applicable in this context, where inputs appear sequentially. Therefore, this phase must rely on online optimization of the search engine tailored for each individual agent, utilizing their specific feedback.

**中文**

然而，由于多种原因，这种方法在服务阶段并不可行。首先，服务阶段需要快速访问信息，因为代理无法等待从所有其他代理收集反馈。此外，离线优化方法通常需要访问完整的查询集才能进行有效优化，这在输入按顺序出现的情况下不适用。因此，此阶段必须依赖于利用每个代理的具体反馈，针对每个代理量身定制的搜索引擎的在线优化。

### 段落 49 · Page 5

**EN**

For this purpose, we assume that feedback for a test instance 𝑥𝑡 from the agent 𝑀𝑖 is only provided after 𝑅𝜃 has already retrieved and delivered the relevant documents to the agent, and the agent will not submit 𝑥𝑡 to the system again afterwards. In other words, the search engine has only observed and served the first 𝑡 − 1 queries and received feedback for them by the time it attempts to serve 𝑥𝑡 . Therefore, the search engine can utilize the feedback from the first 𝑡 − 1 queries to optimize its performance for serving the 𝑡th query. There are several strategies for updating the search engine parameters based on received online feedback.

**中文**

为此，我们假设代理𝑀𝑖对测试实例𝑥𝑡的反馈仅在𝑅𝜃已经检索并交付相关文档给代理之后提供，并且代理之后不会再次向系统提交𝑥𝑡。换句话说，搜索引擎仅观察并提供第一个 𝑡 − 1 个查询，并在尝试提供 𝑥𝑡 时收到反馈。因此，搜索引擎可以利用第一个 𝑡 - 1 个查询的反馈来优化其服务于第 𝑡 个查询的性能。有多种策略可用于根据收到的在线反馈来更新搜索引擎参数。

### 段落 50 · Page 5

**EN**

One possible approach is to update the search engine after each feedback to align it with the agent’s preferences. However, this method has several shortcomings: first, updating the search engine after each feedback is computationally expensive. Additionally, the feedback for a single input may be noisy, leading to noisy gradient updates. On the other hand, an alternative strategy is to observe the majority of test instances before updating the model for the remaining queries. However, this would result in using the same old parameters for most of the test instances.

**中文**

一种可能的方法是在每次反馈后更新搜索引擎，使其与代理的偏好保持一致。然而，这种方法有几个缺点：首先，每次反馈后更新搜索引擎的计算量很大。此外，单个输入的反馈可能有噪声，导致有噪声的梯度更新。另一方面，另一种策略是在更新剩余查询的模型之前观察大多数测试实例。但是，这将导致大多数测试实例使用相同的旧参数。

### 段落 51 · Page 5

**EN**

Therefore, we adopt a middle-ground approach and apply the same method as described in Section 4.1 to optimize the model over several iterations. We define an iteration as serving 𝑏4 consecutive queries and receiving the corresponding feedback. Thus, in step 𝑡 + 1, the model has access to the previous 3The serving phase refers to the period when the system is being tested. 4We call this parameter the online optimization batch size, which differs from the batch size used in gradient optimization methods. user queries 𝑄𝑡 𝑀𝑖 = {𝑥1, ..., 𝑥𝑏 ×𝑡 } (This is the Expectation Step, as defined in Section 4.1).

**中文**

因此，我们采用中间立场方法，并应用与 4.1 节中描述的相同方法通过多次迭代来优化模型。我们将迭代定义为服务 𝑏4 个连续查询并接收相应的反馈。因此，在步骤𝑡+1中，模型可以访问之前的3个服务阶段，即系统正在测试的时期。 4我们将此参数称为在线优化批量大小，它与梯度优化方法中使用的批量大小不同。用户查询 𝑄𝑡 𝑀𝑖 = {𝑥1, ..., 𝑥𝑏 ×𝑡 } （这是期望步骤，如第 4.1 节中所定义）。

### 段落 52 · Page 5

**EN**

Finally, the parameters for agent 𝑀𝑖 can be updated based on the following objective function (This is the Maximization Step, as defined in Section 4.1): 𝜃𝑡 +1 𝑀𝑖 = arg max 𝜃 E 𝑥∼𝑄𝑡 𝑀𝑖  E 𝑑∼𝑝∗ 𝜃𝑡 𝑀𝑖 (𝑑 |𝑥 )  log 𝑝𝜃 (𝑅 = 𝑓𝑀𝑖 (𝑑, 𝑥)|𝑥, 𝑑)   (5) where the main difference between this objective function and Equation 3 is that the optimization occurs for each individual agent based on their own feedback, with inputs sampled from the previous queries observed from the agent during the serving phase.

**中文**

最后，代理 𝑀𝑖 的参数可以基于以下目标函数进行更新（这是最大化步骤，如第 4.1 节中所定义）： 𝜃𝑡 +1 𝑀𝑖 = arg max 𝜃 E 𝑥∼𝑄𝑡 𝑀𝑖  E 𝑑∼𝑝* 𝜃𝑡 𝑀𝑖 (𝑑 |𝑥 ) log 𝑝𝜃 (𝑅 = 𝑓𝑀𝑖 (𝑑, 𝑥)|𝑥, 𝑑)  (5) 其中，该目标函数与方程 3 之间的主要区别在于，每个单独的代理都会根据其自己的反馈进行优化，输入是从代理在服务阶段观察到的先前查询中采样的。

### 段落 53 · Page 5

**EN**

Training Procedure: To optimize the search engine usingOnline IUM, we assume a specific agent submits 𝑏 queries to the search engine, which retrieves the top results from the corpus 𝐶 for the given queries and the previous iteration parameters. In response, the agent provides feedback for the retrieved documents. Following this, the search engine enters an optimization phase, updating its parameters based on the feedback received for all queries submitted thus far by that agent, using Equation 5, to get the parameters for next iteration. This procedure is shown in Algorithm 2. Algorithm 2 The Online IUM algorithm.

**中文**

训练过程：为了使用在线 IUM 优化搜索引擎，我们假设特定代理向搜索引擎提交 𝑏 查询，搜索引擎从语料库 𝐶 中检索给定查询和先前迭代参数的最佳结果。作为响应，代理提供检索到的文档的反馈。此后，搜索引擎进入优化阶段，根据该代理迄今为止提交的所有查询收到的反馈，使用公式 5 更新其参数，以获得下一次迭代的参数。该过程如算法 2 所示。 算法 2 在线 IUM 算法。

### 段落 54 · Page 5

**EN**

Initialize 𝑡 = 1 Initialize the retrieval model for agent 𝑀𝑖 from Algorithm 1 checkpoint 𝐷𝑡𝑒𝑠𝑡 𝑀𝑖 = {} while there is a query 𝑥𝑖 do Retrieve 𝑘 docs from corpus 𝐶 by 𝑅𝜃 𝑡 : 𝑟 = 𝑅𝜃 𝑡 𝑀𝑖 (𝑥𝑖, 𝐶, 𝑘) Collect feedback of agent 𝑀𝑖 for list 𝑟: 𝑓𝑗 = 𝑓𝑀𝑖 (𝑑 𝑗 , 𝑥𝑖 ) Add feedback to online dataset: 𝐷𝑡𝑒𝑠𝑡 𝑀𝑖 = 𝐷𝑡𝑒𝑠𝑡 𝑀𝑖 ∪ {( 𝑥𝑖, 𝑑𝑗 , 𝑓 𝑗 )} if |𝐷𝑡𝑒𝑠𝑡 𝑀𝑖 | dividable by 𝑏 then 𝜃𝑡 +1 𝑀𝑖 = arg max𝜃 E(𝑥,𝑑,𝑓 )∼𝐷𝑡𝑒𝑠𝑡 𝑀𝑖 [log 𝑝𝜃 (𝑅 = 𝑓 |𝑥, 𝑑)] 𝑡 = 𝑡 + 1 end if end while 4.3 The Search Engine Architecture The proposed algorithms can work for any learning-to-rank approach.

**中文**

初始化 𝑡 = 1 当存在查询 𝑥𝑖 时，从算法 1 检查点 𝐷𝑡𝑒𝑠𝑡 𝑀𝑖 = {} 初始化代理𝑀𝑖 的检索模型，同时存在查询 𝑥𝑖 执行 𝑅𝜃 从语料库 𝐶 检索 𝑘 文档𝑡 : 𝑟 = 𝑅𝜃 𝑡 𝑀𝑖 (𝑥𝑖, 𝐶, 𝑘) 收集代理𝑀𝑖对列表𝑟的反馈： 𝑓𝑗 = 𝑓𝑀𝑖 (𝑑 𝑗 , 𝑥𝑖 ) 向在线数据集添加反馈： 𝐷𝑡𝑒𝑠𝑡 𝑀𝑖 = 𝐷𝑡𝑒𝑠𝑡 𝑀𝑖 ∪ {( 𝑥𝑖, 𝑑𝑗 , 𝑓 𝑗 )}如果 |𝐷𝑡𝑒𝑠𝑡 𝑀𝑖 |可除以 𝑏 那么 𝜃𝑡 +1 𝑀𝑖 = arg max𝜃 E(𝑥,𝑑,𝑓 )∼𝐷𝑡𝑒𝑠𝑡 𝑀𝑖 [log 𝑝𝜃 (𝑅 = 𝑓 |𝑥, 𝑑)] 𝑡 = 𝑡 + 1 end if end while 4.3 搜索引擎架构所提出的算法可以适用于任何学习排序方法。

### 段落 55 · Page 5

**EN**

Following uRAG from Salemi and Zamani [45], this paper employs a two-stage cascaded retrieval system. In the first stage, BM25 [35] is used to retrieve a set of initial relevant candidate documents. Then, a fine-tuned cross-encoder model is applied to re-rank the retrieved documents. Note that all the trainable parameters𝜃 in the search engine are for the re-ranking model.

**中文**

继 Salemi 和 Zamani [45] 的 uRAG 之后，本文采用了两级级联检索系统。在第一阶段，BM25 [35]用于检索一组初始相关候选文档。然后，应用微调的交叉编码器模型对检索到的文档进行重新排序。请注意，搜索引擎中的所有可训练参数𝜃都是用于重新排序模型的。

### 段落 56 · Page 5

**EN**

Following Nogueira and Cho [31], we add a linear projection over the representation of the start token (i.e., [CLS]) of a text encoder to obtain the relevance probability of a query and document, as follows: 𝑝 (𝑅 = 1|𝑥, 𝑑) = 𝜎 (ENCODER(𝑡𝑖𝑑 ; 𝑚𝑖𝑑; 𝑥; 𝑑) ·𝑊 ) (6) where 𝑑 is a document, 𝑥 is the query, 𝑡𝑖𝑑 is an ID associated with the agent’s task,𝑚𝑖𝑑 is the ID associated with the LLM backbone used in the agent, 𝜎 is the sigmoid function, and 𝑊 ∈ R𝐷 ×1 is a

**中文**

遵循 Nogueira 和 Cho [31]，我们在文本编码器的起始标记（即 [CLS]）的表示上添加线性投影，以获得查询和文档的相关概率，如下所示： 𝑝 (𝑅 = 1|𝑥, 𝑑) = 𝜎 (ENCODER(𝑡𝑖𝑑 ; 𝑚𝑖𝑑; 𝑥; 𝑑) ·𝑊 ) (6) 其中 𝑑 是文档，𝑥 是查询，𝑡𝑖𝑑 是与代理任务关联的 ID，𝑚𝑖𝑑 是与代理中使用的 LLM 主干关联的 ID，𝜎 是 sigmoid 函数，𝑊 ∈ R𝐷 ×1 是

### Page 6

### 段落 57 · Page 6

**EN**

ICTIR ’25, July 18, 2025, Padua, Italy Alireza Salemi and Hamed Zamani linear projection, where 𝐷 represents the embedding dimensionality of the encoder. We utilize BERT5 [8] with 110M parameters and embedding dimensionality of 𝐷 = 768 as the encoder. Here, following Salemi and Zamani [45], 𝑡𝑖𝑑 and 𝑚𝑖𝑑 is used for the purpose of personalizing retrieval model for each agent. In this way, each agent provides its underlying LLM architecture and the task it is performing, represented by a task ID ( 𝑡𝑖𝑑 ) and a model ID (𝑚𝑖𝑑).

**中文**

ICTIR ’25，2025 年 7 月 18 日，意大利帕多瓦 Alireza Salemi 和 Hamed Zamani 线性投影，其中 𝐷 表示编码器的嵌入维数。我们使用具有 110M 参数和嵌入维数 𝐷 = 768 的 BERT5 [8] 作为编码器。在这里，遵循 Salemi 和 Zamani [45]，使用 𝑡𝑖𝑑 和 𝑚𝑖𝑑 来为每个代理个性化检索模型。通过这种方式，每个代理提供其底层 LLM 架构及其正在执行的任务，由任务 ID (𝑡𝑖𝑑) 和模型 ID (𝑚𝑖𝑑) 表示。

### 段落 58 · Page 6

**EN**

The search engine uses these identifiers as input and, when optimized with feedback from each user, learns both the specific preferences of individual users (presence of𝑡𝑖𝑑 and 𝑚𝑖𝑑 together in input) and the general information needs associated with each task (𝑡𝑖𝑑 ) and architecture (𝑚𝑖𝑑). This enables the search engine to better understand user preferences and provide more effective, tailored results while also learning the general preferences associated with each task and agent architecture. 5 EXPERIMENTS 5.1 Experiment Setup Datasets & Corpus. We use various tasks from the KILT benchmark [32] to evaluate our approach.

**中文**

搜索引擎使用这些标识符作为输入，并在根据每个用户的反馈进行优化时，了解各个用户的特定偏好（𝑡𝑖𝑑和𝑚𝑖𝑑一起出现在输入中）以及与每个任务（𝑡𝑖𝑑）和架构（𝑚𝑖𝑑）相关的一般信息需求。这使得搜索引擎能够更好地了解用户偏好并提供更有效、定制的结果，同时还可以了解与每个任务和代理架构相关的一般偏好。 5 实验 5.1 实验设置数据集和语料库。我们使用 KILT 基准 [32] 中的各种任务来评估我们的方法。

### 段落 59 · Page 6

**EN**

Dataset statistics is reported Table 2. We experiment with six diverse datasets, including three diverse open-domain question answering datasets: Natural Questions (NQ) [24], TriviaQA [19], and HotPotQA [60]. Notably, HotPotQA focuses on questions requiring multi-hop reasoning. Additionally, we use one fact verification dataset, FEVER [53], and two slot-filling datasets for relation extraction: zsRE [25] and T-REx [9]. Note that since the T-REx training set contains approximately 2.2 million samples, we randomly select 5% of them to train our models in order to speed up the experiments. We use the same samples as is used in [45].

**中文**

数据集统计数据如表 2 所示。我们用六个不同的数据集进行实验，包括三个不同的开放域问答数据集：Natural Questions (NQ) [24]、TriviaQA [19] 和 HotPotQA [60]。值得注意的是，HotPotQA 专注于需要多跳推理的问题。此外，我们使用一个事实验证数据集 FEVER [53] 和两个槽填充数据集进行关系提取：zsRE [25] 和 T-REx [9]。请注意，由于 T-REx 训练集包含大约 220 万个样本，因此我们随机选择其中的 5% 来训练我们的模型，以加快实验速度。我们使用与[45]中使用的相同的样本。

### 段落 60 · Page 6

**EN**

It is also important to mention that the test set labels for these datasets are not publicly available. Therefore, we directly use the validation set to evaluate the models. Note that we utilize the McNemar statistical significance test [30] in our experiments, as the metrics for the tasks—accuracy and exact match—yield binary outcomes, making this test appropriate for evaluating significant performance differences. We use the Wikipedia dump provided by the KILT benchmark as the unstructured knowledge source.6 We follow the pre-processing method outlined by Karpukhin et al.

**中文**

还需要指出的是，这些数据集的测试集标签不是公开的。因此，我们直接使用验证集来评估模型。请注意，我们在实验中使用了 McNemar 统计显着性检验 [30]，因为任务的指标（准确性和精确匹配）产生二元结果，使得该测试适合评估显着的性能差异。我们使用 KILT 基准测试提供的维基百科转储作为非结构化知识源。6 我们遵循 Karpukhin 等人概述的预处理方法。

### 段落 61 · Page 6

**EN**

[20], in which each document is split into passages with a maximum length of 100 words. Additionally, the document title is concatenated with each passage to form the entries in the retrieval corpus. Agents Configuration. Following Salemi and Zamani[45], we use 18 diverse RAG agents, as listed in Table 1. In this setting, each agent is trained on a separate dataset, with a distinct set of resources, a different underlying LLM, and retrieves a varying number of documents to perform its task. Each RAG agent is fine-tuned on the corresponding training set.

**中文**

[20]，其中每个文档被分成最大长度为100字的段落。此外，文档标题与每个段落连接起来形成检索语料库中的条目。代理配置。继 Salemi 和 Zamani[45]之后，我们使用了 18 个不同的 RAG 代理，如表 1 所列。在这种设置中，每个代理都在一个单独的数据集上进行训练，具有一组不同的资源、不同的底层 LLM，并检索不同数量的文档来执行其任务。每个 RAG 代理都在相应的训练集上进行微调。

### 段落 62 · Page 6

**EN**

Additionally, the number of retrieved documents is determined based on each agent’s LLM maximum input size. We consider two types of RAG agents: (1) Retrieval-augmented LLM (RA-X) is a language model that consumes 𝑘 documents per input via in-prompt augmentation based on the following input format: “ {input} context 1: 5Checkpoint can be find at: https://huggingface.co/google-bert/bert-base-uncased 6The retrieval corpus is available at https://dl.fbaipublicfiles.com/ur/wikipedia_split/ psgs_w100.tsv.gz Table 1: A list of RAG models used in our experiments for training and evaluation. Task Data Utility Func.

**中文**

此外，检索到的文档数量是根据每个代理的 LLM 最大输入大小确定的。我们考虑两种类型的 RAG 代理：(1) 检索增强 LLM (RA-X) 是一种语言模型，它通过基于以下输入格式的提示增强来消耗每个输入的 𝑘 文档：“ {input} context 1: 5Checkpoint 可以在以下位置找到：https://huggingface.co/google-bert/bert-base-uncased 6检索语料库可在以下位置找到： https://dl.fbaipublicfiles.com/ur/wikipedia_split/psgs_w100.tsv.gz 表 1：我们实验中用于训练和评估的 RAG 模型列表。

### 段落 63 · Page 6

**EN**

LM #Docs 𝑀1 open-domain QA NQ Exact Match RA-T5 10 𝑀2 open-domain QA NQ Exact Match RA-BART 4 𝑀3 open-domain QA NQ Exact Match FiD 10 𝑀4 open-domain QA TriviaQA Exact Match RA-T5 10 𝑀5 open-domain QA TriviaQA Exact Match RA-BART 4 𝑀6 open-domain QA TriviaQA Exact Match FiD 10 𝑀7 open-domain QA HotPotQA Exact Match RA-T5 10 𝑀8 open-domain QA HotPotQA Exact Match RA-BART 4 𝑀9 open-domain QA HotPotQA Exact Match FiD 10 𝑀10 fact verification FEVER Accuracy RA-T5 10 𝑀11 fact verification FEVER Accuracy RA-BART 4 𝑀12 fact verification FEVER Accuracy FiD 10 𝑀13 slot filling zsRE Accuracy RA-T5 10 𝑀14 slot filling zsRE Accuracy RA-BART 4 𝑀15 slot fil

**中文**

LM #Docs 𝑀1 开放域 QA NQ 精确匹配 RA-T5 10 𝑀2 开放域 QA NQ 精确匹配 RA-BART 4 𝑀3 开放域 QA NQ 精确匹配 FiD 10 𝑀4 开放域 QA TriviaQA 精确匹配 RA-T5 10 𝑀5 开放域 QA TriviaQA 精确匹配RA-BART 4 𝑀6 开放域 QA TriviaQA 精确匹配 FiD 10 𝑀7 开放域 QA HotPotQA 精确匹配 RA-T5 10 𝑀8 开放域 QA HotPotQA 精确匹配 RA-BART 4 𝑀9 开放域 QA HotPotQA 精确匹配 FiD 10 𝑀10 事实验证 FEVER 准确性RA-T5 10 𝑀11 事实验证 FEVER 精度 RA-BART 4 𝑀12 事实验证 FEVER 精度 FiD 10 𝑀13 槽填充 zsRE 精度 RA-T5 10 𝑀14 槽填充 zsRE 精度 RA-BART 4 𝑀15 槽填充

### 段落 64 · Page 6

**EN**

ling zsRE Accuracy FiD 10 𝑀16 slot filling T-REx Accuracy RA-T5 10 𝑀17 slot filling T-REx Accuracy RA-BART 4 𝑀18 slot filling T-REx Accuracy FiD 10 Table 2: A list of datasets from KILT [ 32] used in our experiments.

**中文**

ling zsRE 精度 FiD 10 𝑀16 槽填充 T-REx 精度 RA-T5 10 𝑀17 槽填充 T-REx 精度 RA-BART 4 𝑀18 槽填充 T-REx 精度 FiD 10 表 2：我们实验中使用的 KILT [32] 数据集列表。

### 段落 65 · Page 6

**EN**

The validation data from KILT is used as test sets. ∗ Given the large training set in the original T-REx dataset, we only sampled 5% of data for training our models. Dataset #train #test open-domain QA (short answer) Natural Questions 87,372 2,837 TriviaQA 61,844 5,359 HotPotQA 88,869 5,600 fact verification FEVER 104,966 10,444 slot-filling relation extraction zsRE 147,909 3,724 T-REx 114,208 ∗ 5,000 {doc1} . . . context k: {dock} ”, where {input} is 𝑥 and {doci} denotes the content of the 𝑖th retrieved document. (2) Fusion-in-Decoder (FiD) [15] uses a different augmentation approach.

**中文**

来自 KILT 的验证数据用作测试集。考虑到原始 T-REx 数据集中的训练集很大，我们只采样了 5% 的数据来训练我们的模型。数据集 #train #test 开放域 QA（简答） 自然问题 87,372 2,837 TriviaQA 61,844 5,359 HotPotQA 88,869 5,600 事实验证 FEVER 104,966 10,444 槽填充关系提取 zsRE 147,909 3,724 T-REx 114,208 * 5,000 {doc1}。。。 context k: {dock} ”，其中 {input} 是 𝑥，{doci} 表示第 𝑖 检索到的文档的内容。 (2) Fusion-in-Decoder (FiD) [15] 使用不同的增强方法。

### 段落 66 · Page 6

**EN**

Unlike RA-X that is based on in-prompt augmentation, FiD first encodes the input and each retrieved document separately and uses the concatenation of all document encodings as cross-attention for the decoder. FiD can thus only be done using encoder-decoder language models. We utilize T5-small [33] with 60M parameters and BART-base [26] with 140M parameters using the first retrieval-augmentation approach and T5-small with the FiD. We use six datasets and apply three distinct RAG models to each, resulting in 18 unique agents for our experiments. All RAG agents are fine-tuned individually.

**中文**

与基于即时增强的 RA-X 不同，FiD 首先对输入和每个检索到的文档进行单独编码，并使用所有文档编码的串联作为解码器的交叉注意力。因此，FiD 只能使用编码器-解码器语言模型来完成。我们使用具有 60M 参数的 T5-small [33] 和具有 140M 参数的 BART-base [26]，使用第一种检索增强方法，并使用带有 FiD 的 T5-small。我们使用六个数据集，并对每个数据集应用三个不同的 RAG 模型，从而为我们的实验产生 18 个独特的代理。所有 RAG 代理均单独进行微调。

### 段落 67 · Page 6

**EN**

The AdamW optimizer with a weight decay of 10−2 and a learning rate of 5 × 10−5 for 10 epochs is used to train these models. A linear warmup is applied to the first 5% of training steps. The effective batch size is set to 64 through gradient accumulation. Each model is trained on varying computational resources, including up to 8 A100, 1080ti, and 2080ti Nvidia GPUs. To optimize the RAG agents, in this paper, we employ a sequence-two-sequence loss function [52] using cross-entropy between the predicted token probability and the ground truth output sequence.

**中文**

AdamW 优化器的权重衰减为 10−2，学习率为 5 × 10−5，持续 10 个周期，用于训练这些模型。线性预热应用于前 5% 的训练步骤。通过梯度累加将有效batch size设置为64。每个模型都在不同的计算资源上进行训练，包括最多 8 个 A100、1080ti 和 2080ti Nvidia GPU。为了优化 RAG 代理，在本文中，我们采用了序列-二序列损失函数 [52]，使用预测令牌概率和地面真实输出序列之间的交叉熵。

### Page 7

### 段落 68 · Page 7

**EN**

Learning to Rank for Multiple Retrieval-Augmented Models through Iterative Utility Maximization ICTIR ’25, July 18, 2025, Padua, Italy Table 3: Downstream performance of RAG models in Table 1 utilizing the search engine. Superscripts 1, 2, 3, 4, and 5 denote statistically significant improvements in the performance compared to BM25, Contriever, Rerankerindividual, Rerankerdataset, uRAG, respectively, using McNemar significance test ( 𝑝 < 0.05).

**中文**

通过迭代效用最大化学习对多个检索增强模型进行排名 ICTIR’25，2025 年 7 月 18 日，意大利帕多瓦 表 3：表 1 中 RAG 模型利用搜索引擎的下游性能。上标 1、2、3、4 和 5 分别表示使用 McNemar 显着性检验（𝑝 < 0.05）与 BM25、Contriever、Rerankerindividual、Rerankerdataset、uRAG 相比，性能有统计学上的显着改进。

### 段落 69 · Page 7

**EN**

RAG Data & Metric BM25 Contriever Reranker individual Rerankerdataset uRAG IUM Model Offline IUM Online IUM 𝑀1 NQ - EM 28.05 22.55 36.76 37.39 37.82 38.42 12 38.841234 𝑀2 NQ - EM 33.09 23.68 40.07 40.50 42.12 43.60 12345 45.1112345 𝑀3 NQ - EM 29.64 23.69 40.50 41.14 42.37 42.511234 42.471234 𝑀4 TriviaQA - EM 51.35 44.33 59.28 60.25 60.68 61.8712345 61.5912345 𝑀5 TriviaQA - EM 57.52 48.49 64.76 67.23 68.12 68.03 123 68.871234 𝑀6 TriviaQA - EM 60.48 49.30 67.44 68.63 68.74 70.2712345 70.0512345 𝑀7 HotPotQA - EM 27.51 18.80 29.92 30.91 31.33 31.41123 31.16123 𝑀8 HotPotQA - EM 31.21 20.78 35.03 34.62 34.85 35.51124 35.4112 𝑀9 HotPotQA - EM 29.48

**中文**

RAG 数据和指标 BM25 Contriever Reranker 个体 Rerankerdataset uRAG IUM 模型 离线 IUM 在线 IUM 𝑀1 NQ - EM 28.05 22.55 36.76 37.39 37.82 38.42 12 38.841234 𝑀2 NQ - EM 33.09 23.68 40.07 40.50 42.12 43.60 12345 45.1112345 𝑀3 NQ - 新兴市场 29.64 23.69 40.50 41.14 42.37 42.511234 42.471234 𝑀4 TriviaQA - EM 51.35 44.33 59.28 60.25 60.68 61.8712345 61.5912345 𝑀5 TriviaQA - EM 57.52 48.49 64.76 67.23 68.12 68.03 123 68.871234 𝑀6 TriviaQA - EM 60.48 49.30 67.44 68.63 68.74 70.2712345 70.0512345 𝑀7 HotPotQA - EM 27.51 18.80 29.92 30.91 31.33 31.41123 31.16123 𝑀8 HotPotQA - 新兴市场 31.21 20.78 35.03 34.62 34.85 35.51124 35.4112 𝑀9 HotPotQA - 新兴市场 29.48

### 段落 70 · Page 7

**EN**

20.43 32.54 32.71 33.46 33.771234 33.751234 𝑀10 FEVER - Accuracy 86.83 84.21 86.24 86.83 86.46 86.58 2 86.582 𝑀11 FEVER - Accuracy 87.54 84.37 84.38 87.54 85.99 86.17 23 87.44235 𝑀12 FEVER - Accuracy 87.04 86.74 86.02 87.04 86.55 86.98 235 87.47235 𝑀13 zsRE - Accuracy 55.37 38.77 60.39 59.98 61.09 61.22 1234 61.8912345 𝑀14 zsRE - Accuracy 51.42 29.05 59.29 58.96 60.58 60.681234 60.311234 𝑀15 zsRE - Accuracy 55.42 37.35 60.47 60.66 62.13 62.35 1234 62.431234 𝑀16 T-REx - Accuracy 70.88 56.94 73.58 72.86 72.92 73.62 12345 73.9812345 𝑀17 T-REx - Accuracy 75.16 58.30 80.04 80.18 79.94 80.3212 80.2412 𝑀18 T-REx - Accuracy 78.88 65.06 80.78 80.34 80

**中文**

20.43 32.54 32.71 33.46 33.771234 33.751234 𝑀10 发烧 - 准确度 86.83 84.21 86.24 86.83 86.46 86.58 2 86.582 𝑀11 发烧 - 准确度87.54 84.37 84.38 87.54 85.99 86.17 23 87.44235 𝑀12 发烧 - 准确度 87.04 86.74 86.02 87.04 86.55 86.98 235 87.47235 𝑀13 zsRE - 准确度 55.37 38.77 60.39 59.98 61.09 61.22 1234 61.8912345 𝑀14 zsRE - 准确度 51.42 29.05 59.29 58.96 60.58 60.681234 60.311234 𝑀15 zsRE - 准确度 55.42 37.35 60.47 60.66 62.13 62.35 1234 62.431234 𝑀16 T-REx - 准确度 70.88 56.94 73.58 72.86 72.92 73.62 12345 73.9812345 𝑀17 T-REx - 准确度 75.16 58.30 80.04 80.18 79.94 80.3212 80.2412 𝑀18 T-REx - 准确度 78.88 65.06 80.78 80.34 80

### 段落 71 · Page 7

**EN**

.24 80.88 125 81.1412345 Overall (macro-average) 55.38 45.15 59.86 60.43 60.85 61.34 12345 61.5912345 Each RAG agent is expected to provide feedback for the given retrieval list as a singal to help improving the search engine.

**中文**

.24 80.88 125 81.1412345 总体（宏观平均） 55.38 45.15 59.86 60.43 60.85 61.34 12345 61.5912345 每个 RAG 代理都应该为给定的检索列表提供反馈作为信号，以帮助改进搜索引擎。

### 段落 72 · Page 7

**EN**

For simplicity, in this paper, we consider the case where the RAG model provides feedback on a per-document basis. To generate feedback, we use the evaluation metric associated with the dataset that the model is applied to as the utility function for that model. Table 1 outlines the utility functions assigned to the RAG agents used in this study. Specifically, we employ Exact Match (EM) for question answering datasets and accuracy for the remaining tasks. For EM, we follow the post-processing procedures introduced by Rajpurkar et al. [34].

**中文**

为简单起见，在本文中，我们考虑 RAG 模型基于每个文档提供反馈的情况。为了生成反馈，我们使用与模型所应用的数据集关联的评估指标作为该模型的效用函数。表 1 概述了分配给本研究中使用的 RAG 代理的效用函数。具体来说，我们对问答数据集采用精确匹配（EM），并对其余任务采用准确性。对于 EM，我们遵循 Rajpurkar 等人介绍的后处理程序。 [34]。

### 段落 73 · Page 7

**EN**

Accordingly, the feedback for a specific retrieval list reflects the performance of the RAG agent when using only each single document in the list in its task, and is evaluated based on the utility function and downstream task expected output. Search Engine Configuration . The search engine initially retrieves 100 documents using BM25 [35]. These documents are then reranked using the appropriate reranking model based on the experimental setup. Training 𝑅𝜃 involves two phase. For the first phase of training with Offline IUM , the Adam optimizer [ 22] with a learning rate of 10−5 for two epochs is used.

**中文**

因此，特定检索列表的反馈反映了 RAG 代理在其任务中仅使用列表中的每个单个文档时的性能，并根据效用函数和下游任务预期输出进行评估。搜索引擎配置。搜索引擎最初使用 BM25 [35] 检索 100 个文档。然后根据实验设置使用适当的重新排序模型对这些文档进行重新排序。训练𝑅𝜃 涉及两个阶段。对于离线 IUM 训练的第一阶段，使用 Adam 优化器 [22]，两个时期的学习率为 10−5。

### 段落 74 · Page 7

**EN**

A linear warmup is applied to the first 5% of training steps. The effective batch size is set to 512, achieved through gradient accumulation. A consistent value of 𝑘 = 32 is used during training, and the maximum input length for this model is set to 256 tokens. We train the model for 𝑇 = 3 iterations. Note that we randomly replace the model ID and task ID with the “unk” token for 10% of the training samples for better generalization. For the second phase training using Online IUM, we set batch size 𝑏 = 256. Additionally, we utilize the same optimizer and learning rate to train the model for two epochs in each iteration.

**中文**

线性预热应用于前 5% 的训练步骤。有效batch size设置为512，通过梯度累加实现。训练期间使用一致的值 𝑘 = 32，并且该模型的最大输入长度设置为 256 个标记。我们训练模型进行 𝑇 = 3 次迭代。请注意，我们随机将 10% 的训练样本的模型 ID 和任务 ID 替换为“unk”标记，以实现更好的泛化。对于使用 Online IUM 的第二阶段训练，我们设置批量大小 𝑏 = 256。此外，我们利用相同的优化器和学习率在每次迭代中训练两个时期的模型。

### 段落 75 · Page 7

**EN**

In this case, we set the variable 𝑘 to be consistent (a) The Effect of Offline Learning Number of Iterations (b) The Effect of Online Learning Batch Size Figure 2: (a) The impact of iterations on personalized (solid) and non-personalized (dashed) Offline IUM and (b) the effect of batch size 𝑏 on Online IUM performance. with the downstream RAG agent configuration for each model in Table 1, in contrast with the offline phase, where we set a constant number of 𝑘 = 32 for all agents. Additionally, we do not replace the model ID and task ID with the “unk” token for the sake of fully personalizing the search engine for the agent.

**中文**

在这种情况下，我们将变量𝑘设置为一致（a）离线学习迭代次数的影响（b）在线学习批量大小的影响图2：（a）迭代对个性化（实线）和非个性化（虚线）离线IUM的影响以及（b）批量大小𝑏对在线IUM性能的影响。表 1 中每个模型的下游 RAG 代理配置，与离线阶段相反，我们为所有代理设置常数 𝑘 = 32。此外，为了完全个性化代理的搜索引擎，我们不会用“unk”标记替换模型 ID 和任务 ID。

### 段落 76 · Page 7

**EN**

5.2 Main Results This section addresses the following research questions, providing detailed analyses and insights based on our experimental findings. How does Offline IUM impact downstream RAG performance? We employ the baselines introduced by Salemi and Zamani [45] for comparative evaluation against our proposed approach. There are two types of baselines: (1) Single-stage retrieval and (2) Cascaded two-stage retrieval models. The single-stage retrieval baselines include BM25 [35] as a sparse retriever and Contriever

**中文**

5.2 主要结果本节讨论以下研究问题，根据我们的实验结果提供详细的分析和见解。离线 IUM 如何影响下游 RAG 性能？我们采用 Salemi 和 Zamani [45] 引入的基线与我们提出的方法进行比较评估。基线有两种类型：(1) 单阶段检索模型和 (2) 级联两阶段检索模型。单阶段检索基线包括 BM25 [35] 作为稀疏检索器和 Contriever

### Page 8

### 段落 77 · Page 8

**EN**

ICTIR ’25, July 18, 2025, Padua, Italy Alireza Salemi and Hamed Zamani Figure 3: Effect of online learning batch size 𝑏 on Online IUM on per agent performance. [13] as a dense retriever. The cascaded two-stage methods employ BM25 in the first stage, followed by a reranker.

**中文**

ICTIR ’25，2025 年 7 月 18 日，意大利帕多瓦 Alireza Salemi 和 Hamed Zamani 图 3：在线学习批量大小𝑏 对在线 IUM 对每个智能体性能的影响。 [13] 作为一种密集型猎犬。级联两阶段方法在第一阶段采用 BM25，然后进行重新排序。

### 段落 78 · Page 8

**EN**

Salemi and Zamani [45] introduces three baselines for reranking: 1) Rerankerindividual, which is a reranker trained individually for each agent based on a single round of feedback from the respective agent, 2)Rerankerdataset that is a reranker trained for each dataset similar to previous one, using feedback from all agents associated with that dataset, and 3) uRAG, which is a single reranker trained across all agents using the combined feedback from different agents.

**中文**

Salemi 和 Zamani [45] 引入了三个用于重排序的基线：1）Rerankerindividual，这是基于来自各个代理的单轮反馈为每个代理单独训练的重排序器；2）Rerankerdataset，这是使用来自与该数据集关联的所有代理的反馈，为每个数据集训练的与前一个类似的重排序器；3）uRAG，这是使用来自不同代理的组合反馈在所有代理上训练的单个重排序器。

### 段落 79 · Page 8

**EN**

The results of this experiment are presented in Table 3 and suggest that Offline IUM outperforms all baselines for 14 out of 18 RAG agents, with the performance difference being statistically significant in 4 cases from all baselines. Moreover, Offline IUM achieves statistically significant improvements over all baselines when considering the average performance across all agents. That said, the results from this experiment suggest that Offline IUM is a promising and effective approach for addressing the problem at hand. How does the number of training iterations in Offline IUM impact the performance?

**中文**

该实验的结果如表 3 所示，表明 18 种 RAG 药物中有 14 种 Offline IUM 的性能优于所有基线，其中 4 种情况与所有基线的性能差异具有统计显着性。此外，在考虑所有代理的平均性能时，Offline IUM 在所有基线上实现了统计上显着的改进。也就是说，该实验的结果表明，离线 IUM 是解决当前问题的一种有前途且有效的方法。 Offline IUM 中的训练迭代次数如何影响性能？

### 段落 80 · Page 8

**EN**

An important hyperparameter for Offline IUM is the number of iterations. To investigate its impact, we train the search engine over several iterations and evaluate its performance at each step. The outcomes of this experiment are presented in Figure 2 (a—solid lines) for the average performance and Figure 4 for per agent performance. The results in Figure 2 (a) suggest that, overall, increasing the number of iterations leads to improved performance for Offline IUM. However, the magnitude of improvement diminishes with each additional iteration.

**中文**

Offline IUM 的一个重要超参数是迭代次数。为了研究其影响，我们对搜索引擎进行了多次迭代训练，并在每一步评估其性能。该实验的结果如图 2（a—实线）所示为平均性能，图 4 为每个代理的性能。图 2 (a) 中的结果表明，总体而言，增加迭代次数可以提高离线 IUM 的性能。然而，改进的幅度随着每一次额外的迭代而减小。

### 段落 81 · Page 8

**EN**

For example, the improvement in average performance from iteration 0 to iteration 1 is 9%, while the gain from iteration 1 to 2 is 0.8%, and from iteration 2 to 3, the increase is less than 0.01%. This indicates diminishing returns as the number of iterations increases. How does “personalization” inOffline IUM training phase impact the performance? As explained in Section 4, we use task ID (tid) and model ID ( mid) to personalize the search engine for Figure 4: Impact of iteration count on personalized (solid) and non-personalized (dashed) Offline IUM plotted per agent. each agent during the Offline IUM training.

**中文**

例如，从迭代0到迭代1平均性能提升为9%，而迭代1到迭代2的增益为0.8%，而从迭代2到迭代3，提升小于0.01%。这表明随着迭代次数的增加，收益递减。离线IUM训练阶段的“个性化”如何影响性能？如第 4 节中所述，我们使用任务 ID (tid) 和模型 ID (mid) 来个性化图 4 的搜索引擎：迭代计数对每个代理绘制的个性化（实线）和非个性化（虚线）离线 IUM 的影响。离线 IUM 培训期间的每个代理。

### 段落 82 · Page 8

**EN**

In this experiment, we remove these IDs and train the search engine without them, using the same setup as Offline IUM. This allows us to examine the impact of these identifiers on personalization of the search engine during the Offline IUM training process on the overall performance. The results of this experiment are demonstrated in in Figure 2 (a) for average performance (dashed lines) and Figure 4 for per agent performance (dashed lines). The results in Figure 4 indicate that training the search engine without incorporating task and model IDs leads to a decline in the performance with increasing iterations.

**中文**

在此实验中，我们使用与离线 IUM 相同的设置删除这些 ID，并在没有它们的情况下训练搜索引擎。这使我们能够在离线 IUM 训练过程中检查这些标识符对搜索引擎个性化对整体性能的影响。图 2 (a) 中展示了该实验的平均性能（虚线），图 4 中展示了每个代理的性能（虚线）。图 4 中的结果表明，在不合并任务和模型 ID 的情况下训练搜索引擎会导致性能随着迭代次数的增加而下降。

### 段落 83 · Page 8

**EN**

Specifically, while most agents benefit from the initial training round, performance get worse for 10 out of 18 agents in the second iteration. Additionally, in Figure 2 (a), the average performance of the search engine also decreases with additional iterations. The results show that the performance gap between the personalized and non-personalized search engines widens with more iterations. Specifically, the plot reveals a growing divergence between the average performance of the personalized search engine and the non-personalized one as the number of iterations increases.

**中文**

具体来说，虽然大多数智能体从初始训练轮中受益，但在第二次迭代中，18 个智能体中有 10 个的性能变得更差。此外，在图 2 (a) 中，搜索引擎的平均性能也会随着迭代次数的增加而降低。结果表明，个性化和非个性化搜索引擎之间的性能差距随着迭代次数的增加而扩大。具体来说，该图揭示了随着迭代次数的增加，个性化搜索引擎和非个性化搜索引擎的平均性能之间的差异越来越大。

### 段落 84 · Page 8

**EN**

This suggests that incorporating personalization significantly benefits the search engine, with the performance gains becoming more pronounced over time. We believe this phenomenon is likely due to the lack of personalization in the non-personalized search engine. Without task and model IDs, the search engine retrieves more generic documents in subsequent iterations, which may not be particularly useful for specific agents. Consequently, the search engine may begin to overfit to the average preferences of all agents during the offline phase, rather than effectively addressing the unique needs of each individual agent.

**中文**

这表明，整合个性化对搜索引擎有很大好处，随着时间的推移，性能提升变得更加明显。我们认为这种现象很可能是由于非个性化搜索引擎缺乏个性化造成的。如果没有任务和模型 ID，搜索引擎将在后续迭代中检索更多通用文档，这对于特定代理可能不是特别有用。因此，在离线阶段，搜索引擎可能开始过度适应所有代理的平均偏好，而不是有效地满足每个代理的独特需求。

### 段落 85 · Page 8

**EN**

How doesOnline IUM impact downstream RAG performance? To investigate this question, we compare Online IUM with the previously discussed baselines. The results of this comparison are presented in Table 3. The results demonstrate that Online IUM surpasses the baselines for 13 out of 18 agents, with 6 of these differences being statistically significant. Moreover, Online IUM significantly enhances the average performance across all agents

**中文**

在线 IUM 如何影响下游 RAG 性能？为了研究这个问题，我们将在线 IUM 与之前讨论的基线进行比较。比较结果如表 3 所示。结果表明，18 种药物中，有 13 种 Online IUM 超过了基线，其中 6 种差异具有统计显着性。此外，在线 IUM 显着提高了所有代理的平均性能

### Page 9

### 段落 86 · Page 9

**EN**

Learning to Rank for Multiple Retrieval-Augmented Models through Iterative Utility Maximization ICTIR ’25, July 18, 2025, Padua, Italy Figure 5: The Kendall’s tau and Jaccard’s similarity between the retrieval lists for agents that utilize the same dataset. compared to the baseline methods. Another notable observation is that Online IUM enhances the performance of Offline IUM. Although this improvement is not statistically significant at the 95% confidence level, the p-value is quite small (p-value = 0.061), indicating a strong trend towards better performance.

**中文**

通过迭代效用最大化学习对多个检索增强模型进行排名 ICTIR’25，2025 年 7 月 18 日，意大利帕多瓦 图 5：使用相同数据集的代理的检索列表之间的 Kendall tau 和 Jaccard 相似度。与基线方法相比。另一个值得注意的观察是在线 IUM 增强了离线 IUM 的性能。尽管在 95% 置信水平下，这种改进在统计上并不显着，但 p 值相当小 (p 值 = 0.061)，表明性能改善的强烈趋势。

### 段落 87 · Page 9

**EN**

This observation suggests that applying Online IUM after Offline IUM is a promising method for the task at hand, indicating potential for further enhancing the system’s performance. How does the batch size 𝑏 in Online IUM affects the performance? One of the key hyperparameters in Online IUM is the batch size 𝑏. This parameter determines how many consecutive queries the search engine should serve using the same set of parameters, essentially defining the feedback collection interval before the model updates its parameters for the next batch.

**中文**

这一观察结果表明，在离线 IUM 之后应用在线 IUM 是完成当前任务的一种有前途的方法，表明有进一步增强系统性能的潜力。 Online IUM 中的批量大小𝑏如何影响性能？ Online IUM 中的关键超参数之一是批量大小𝑏。该参数确定搜索引擎应使用同一组参数服务多少个连续查询，本质上定义了模型更新下一批参数之前的反馈收集间隔。

### 段落 88 · Page 9

**EN**

Exploring the impact of this parameter is insightful, as shown in Figure 2 (b) for average performance and Figure 3 for per agent performance. While the optimal batch size might vary depending on the agent, the general trend suggests that increasing the batch size improves performance up to a certain point, beyond which performance starts to decline. Notably, setting a small value (e.g., 64) leads to a performance drop compared to the starting checkpoint (i.e., the checkpoint from theOffline IUM approach).

**中文**

探索此参数的影响是富有洞察力的，如图 2 (b) 所示的平均性能和图 3 所示的每个代理的性能。虽然最佳批量大小可能因代理而异，但总体趋势表明，增加批量大小可以在一定程度上提高性能，超过该点性能就会开始下降。值得注意的是，与起始检查点（即来自离线 IUM 方法的检查点）相比，设置较小的值（例如 64）会导致性能下降。

### 段落 89 · Page 9

**EN**

We believe this occurs because using a small batch size 𝑏 leads to frequent updates in the model’s parameters, making the model more susceptible to noisy feedback from the agent. These frequent updates might cause the model to overfit to specific feedback points rather than capturing generalizable patterns, thus negatively affecting performance. Does “personalization” withIUM result in different retrieval lists for different RAG agents? We compare the retrieval lists for the same query across different agents when applying IUM to personalize the search engine for them.

**中文**

我们认为发生这种情况是因为使用小批量𝑏会导致模型参数频繁更新，从而使模型更容易受到代理的噪声反馈的影响。这些频繁的更新可能会导致模型过度拟合特定的反馈点，而不是捕获可概括的模式，从而对性能产生负面影响。 IUM 的“个性化”是否会导致不同的 RAG 代理产生不同的检索列表？当应用 IUM 为他们个性化搜索引擎时，我们比较不同代理之间相同查询的检索列表。

### 段落 90 · Page 9

**EN**

To evaluate the similarity between the retrieval lists, we employ two metrics: Kendall’s tau coefficient and Jaccard’s similarity. Kendall’s tau coefficient captures how the ranking order of documents correlates between two lists, providing insights into how similarly or differently the documents are ranked for various agents. Jaccard’s similarity, on the other hand, is a set-based metric that quantifies the overlap between two sets of retrieved documents, indicating the percentage of shared documents across retrieval lists for different agents.

**中文**

为了评估检索列表之间的相似性，我们采用了两个指标：Kendall tau 系数和 Jaccard 相似度。 Kendall 的 tau 系数捕获了两个列表之间文档的排名顺序如何关联，从而深入了解不同代理的文档排名的相似或不同程度。另一方面，Jaccard 相似度是一种基于集合的度量，它量化两组检索到的文档之间的重叠，指示不同代理的检索列表中共享文档的百分比。

### 段落 91 · Page 9

**EN**

These metrics allow us to analyze both the ranking and the content of the retrieved documents across personalized search engine settings. The results of this experiment are shown in Figure 5, yielding several key insights. First, the findings suggest that, on average, about 20% of the retrieved documents differ between RAG agents for the same query. This highlights the personalization effect, where each RAG agent receives a distinct set of documents despite querying with identical input.

**中文**

这些指标使我们能够分析个性化搜索引擎设置中检索到的文档的排名和内容。该实验的结果如图 5 所示，得出了几个重要的见解。首先，研究结果表明，对于同一查询，RAG 代理之间检索到的文档平均有约 20% 存在差异。这突出了个性化效果，其中每个 RAG 代理尽管使用相同的输入进行查询，但仍收到一组不同的文档。

### 段落 92 · Page 9

**EN**

Furthermore, the low Kendall’s tau correlation indicates significant differences in the ranking of the documents retrieved for different RAG agents, demonstrating that the search engine adapts document ranking based on agent-specific preferences and behaviors. Additionally, the Jaccard’s similarity between agents employing FiD and those using in-prompt augmentation is notably lower than between agents both utilizing in-prompt augmentation. This demonstrates that the system has effectively learned to tailor document retrieval strategies according to the different retrieval-augmentation methods used by the RAG agents.

**中文**

此外，较低的 Kendall tau 相关性表明不同 RAG 代理检索到的文档排名存在显着差异，这表明搜索引擎根据代理特定的偏好和行为来调整文档排名。此外，使用 FiD 的代理和使用即时增强的代理之间的 Jaccard 相似度明显低于同时使用即时增强的代理之间的相似性。这表明系统已经有效地学会了根据 RAG 代理使用的不同检索增强方法来定制文档检索策略。

### 段落 93 · Page 9

**EN**

Another interesting observation is that the Kendall’s tau correlation is higher between agents that both using T5 or FiD with T5 than between agents where one employs BART and the other utilizes T5 or FiD with T5. This suggests that the search engine, through model ID, has identified shared information needs between agents that utilize the same backbone language model (T5), resulting in more similar retrieval outputs.

**中文**

另一个有趣的观察结果是，同时使用 T5 或 FiD 与 T5 的代理人之间的 Kendall tau 相关性高于使用 BART 和另一个使用 T5 或 FiD 与 T5 的代理人之间的相关性。这表明搜索引擎通过模型 ID 识别出使用相同主干语言模型 (T5) 的代理之间的共享信息需求，从而产生更相似的检索输出。

### 段落 94 · Page 9

**EN**

In summary, these results confirm that personalization significantly affects the retrieval lists provided to each agent, as the system learns to adapt document rankings and selections based on both the retrieval-augmentation method and the backbone LLM. 6 CONCLUSION & FUTURE WORK In this paper, we address the challenge of building a search engine tailored for multiple RAG agents, functioning similarly to how search engines serve human users, considering the paradigm shift where nowadays LLMs are the main users of the search engines.

**中文**

总之，这些结果证实，个性化会显着影响提供给每个代理的检索列表，因为系统会根据检索增强方法和主干法学硕士学习调整文档排名和选择。 6 结论和未来的工作在本文中，我们解决了构建一个为多个 RAG 代理量身定制的搜索引擎的挑战，其功能类似于搜索引擎为人类用户服务的方式，考虑到当今法学硕士是搜索引擎的主要用户的范式转变。

### 段落 95 · Page 9

**EN**

We propose IUM, an iterative framework with expectation maximization to iteratively gather feedback from RAG agents and adjust the search engine based on them in an offline and online phase. Our findings demonstrate that the proposed approach statistically significantly outperforms established baselines in terms of average agents performance. We also conducted extensive studies to analyze the impact of key factors such as the number of training iterations in Offline IUM, batch size in Online IUM, and the role of personalization in search results for each agent.

**中文**

我们提出了 IUM，一个具有期望最大化的迭代框架，用于迭代地收集来自 RAG 代理的反馈，并基于它们在离线和在线阶段调整搜索引擎。我们的研究结果表明，就平均代理性能而言，所提出的方法在统计上显着优于既定基线。我们还进行了广泛的研究来分析关键因素的影响，例如离线 IUM 中的训练迭代次数、在线 IUM 中的批量大小以及个性化在每个智能体搜索结果中的作用。

### 段落 96 · Page 9

**EN**

Overall, the proposed method exhibits promising results, showcasing its effectiveness in designing search engines for multiple RAG agents. There are several potential future directions for this work: (1) extending the current setup to optimize retrieval models rather than just reranking; (2) considering multiple utility functions per agent; (3) investigating novel regularization techniques to enhance

**中文**

总体而言，所提出的方法展现了有希望的结果，展示了其在为多个 RAG 代理设计搜索引擎方面的有效性。这项工作有几个潜在的未来方向：（1）扩展当前设置以优化检索模型而不仅仅是重排； (2) 考虑每个代理的多个效用函数； (3) 研究新的正则化技术以增强

### Page 10

### 段落 97 · Page 10

**EN**

ICTIR ’25, July 18, 2025, Padua, Italy Alireza Salemi and Hamed Zamani generalization for agents who do not participate in training; (4) exploring interleaving and counterfactual learning approaches within the context of a search engine for machines; and (5) expanding beyond text generation to address a more general REML scenario. ACKNOWLEDGMENTS This work was supported in part by the Center for Intelligent Information Retrieval, in part by NSF grant number 2402873, and in part by the Office of Naval Research contract number N000142412612.

**中文**

ICTIR ’25，2025 年 7 月 18 日，意大利帕多瓦 Alireza Salemi 和 Hamed Zamani 对不参加培训的代理人进行概括； (4) 在机器搜索引擎的背景下探索交错和反事实学习方法； (5) 扩展到文本生成之外，以解决更一般的 REML 场景。致谢 这项工作部分得到了智能信息检索中心的支持，部分得到了 NSF 拨款号 2402873 的支持，部分得到了海军研究办公室合同号 N000142412612 的支持。

### 段落 98 · Page 10

**EN**

Any opinions, findings and conclusions or recommendations expressed in this material are those of the authors and do not necessarily reflect those of the sponsors. REFERENCES [1] Eugene Agichtein, Eric Brill, and Susan Dumais. 2006. Improving web search ranking by incorporating user behavior information. In Proceedings of the 29th Annual International ACM SIGIR Conference on Research and Development in Information Retrieval (Seattle, Washington, USA) (SIGIR ’06). Association for Computing Machinery, New York, NY, USA, 19–26. https://doi.org/10.1145/ 1148170.1148177 [2] Garima Agrawal, Tharindu Kumarage, Zeyad Alghami, and Huan Liu. 2023.

**中文**

本材料中表达的任何意见、调查结果和结论或建议均为作者的观点、发现和结论或建议，并不一定反映申办者的观点。参考文献 [1] Eugene Agichtein、Eric Brill 和 Susan Dumais。 2006年。通过合并用户行为信息来提高网络搜索排名。第 29 届国际 ACM SIGIR 信息检索研究与开发年度会议（美国华盛顿州西雅图）(SIGIR ’06) 论文集。计算机协会，美国纽约州纽约市，19-26。 https://doi.org/10.1145/1148170.1148177 [2] Garima Agrawal、Tharindu Kumarage、Zeyad Alghami 和 Huan Liu。 2023 年。

### 段落 99 · Page 10

**EN**

Can Knowledge Graphs Reduce Hallucinations in LLMs? : A Survey. arXiv:2311.07914 [cs.CL] [3] Akari Asai, Zeqiu Wu, Yizhong Wang, Avirup Sil, and Hannaneh Hajishirzi. 2024. Self-RAG: Learning to Retrieve, Generate, and Critique through Self- Reflection. In The Twelfth International Conference on Learning Representations . https://openreview.net/forum?id=hSyW5go0v8 [4] Kevin Matthe Caramancion. 2024. Large Language Models vs. Search Engines: Evaluating User Preferences Across Varied Information Retrieval Scenarios. arXiv:2401.05761 [cs.IR] https://arxiv.org/abs/2401.05761 [5] Indu Chawla. 2011. An overview of personalization in web search.

**中文**

知识图谱可以减少法学硕士的幻觉吗？：一项调查。 arXiv:2311.07914 [cs.CL] [3] Akari Asai、Zeqiu Wu、Yizhong Wang、Avirup Sil 和 Hannaneh Hajishirzi。 2024.Self-RAG：通过自我反思学习检索、生成和批评。在第十二届国际学习表征会议上。 https://openreview.net/forum?id=hSyW5go0v8 [4] 凯文·马特·卡拉曼西翁。 2024.大型语言模型与搜索引擎：评估各种信息检索场景中的用户偏好。 arXiv:2401.05761 [cs.IR] https://arxiv.org/abs/2401.05761 [5] Indu Chawla。 2011 年。网络搜索个性化概述。

### 段落 100 · Page 10

**EN**

In 2011 3rd International Conference on Electronics Computer Technology , Vol. 3. 128–132. https://doi.org/10.1109/ICECTECH.2011.5941815 [6] Wenhu Chen, Hexiang Hu, Xi Chen, Pat Verga, and William Cohen. 2022. MuRAG: Multimodal Retrieval-Augmented Generator for Open Question Answering over Images and Text. InProceedings of the 2022 Conference on Empirical Methods in Natural Language Processing. Association for Computational Linguistics, Abu Dhabi, United Arab Emirates, 5558–5570. https://doi.org/10.18653/v1/2022.emnlpmain.375 [7] Ofer Dekel, Ran Gilad-Bachrach, Ohad Shamir, and Lin Xiao. 2012.

**中文**

2011年第三届电子计算机技术国际会议，卷。 3. 128-132。 https://doi.org/10.1109/ICECTECH.2011.5941815 [6] 陈文虎、胡鹤翔、陈曦、帕特·维尔加和威廉·科恩。 2022. MuRAG：用于图像和文本开放式问答的多模态检索增强生成。 2022 年自然语言处理经验方法会议论文集。计算语言学协会，阿拉伯联合酋长国阿布扎比，5558–5570。 https://doi.org/10.18653/v1/2022.emnlpmain.375 [7] Ofer Dekel，Ran Gilad-Bachrach，Ohad Shamir 和林晓。 2012年。

### 段落 101 · Page 10

**EN**

Optimal distributed online prediction using mini-batches. J. Mach. Learn. Res. 13, null (jan 2012), 165–202. [8] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. 2019. BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. In Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long and Short Papers). Association for Computational Linguistics, Minneapolis, Minnesota, 4171–4186.

**中文**

使用小批量的最佳分布式在线预测。 J.马赫.学习。资源。 13，无效（2012 年 1 月），165–202。 [8] Jacob Devlin、Ming-Wei Chang、Kenton Lee 和 Kristina Toutanova。 2019.BERT：用于语言理解的深度双向Transformer的预训练。计算语言学协会北美分会 2019 年会议记录：人类语言技术，第 1 卷（长论文和短论文）。计算语言学协会，明尼苏达州明尼阿波利斯，4171-4186。

### 段落 102 · Page 10

**EN**

https://doi.org/10.18653/v1/N19-1423 [9] Hady Elsahar, Pavlos Vougiouklis, Arslen Remaci, Christophe Gravier, Jonathon Hare, Frederique Laforest, and Elena Simperl. 2018. T-REx: A Large Scale Alignment of Natural Language with Knowledge Base Triples. In Proceedings of the Eleventh International Conference on Language Resources and Evaluation (LREC 2018), Nicoletta Calzolari, Khalid Choukri, Christopher Cieri, Thierry Declerck, Sara Goggi, Koiti Hasida, Hitoshi Isahara, Bente Maegaard, Joseph Mariani, Hélène Mazo, Asuncion Moreno, Jan Odijk, Stelios Piperidis, and Takenobu Tokunaga (Eds.).

**中文**

https://doi.org/10.18653/v1/N19-1423 [9]Hady Elsahar、Pavlos Vougiouklis、Arslen Remaci、Christophe Gravier、Jonathon Hare、Frederique Laforest 和 Elena Simperl。 2018。T-REx：自然语言与知识库三元组的大规模对齐。第十一届语言资源与评估国际会议 (LREC 2018) 论文集，Nicoletta Calzolari、Khalid Choukri、Christopher Cieri、Thierry Declerck、Sara Goggi、Koiti Hasida、Hitoshi Isahara、Bente Maegaard、Joseph Mariani、Hélène Mazo、Asuncion Moreno、Jan Odijk、Stelios Piperidis 和 Takenobu Tokunaga （编辑）。

### 段落 103 · Page 10

**EN**

European Language Resources Association (ELRA), Miyazaki, Japan. https://aclanthology.org/L18-1544 [10] Liangke Gui, Borui Wang, Qiuyuan Huang, Alexander Hauptmann, Yonatan Bisk, and Jianfeng Gao. 2022. KAT: A Knowledge Augmented Transformer for Visionand-Language. In Proceedings of the 2022 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies . Association for Computational Linguistics, Seattle, United States, 956–968. https: //doi.org/10.18653/v1/2022.naacl-main.70 [11] Katja Hofmann. 2013. Fast and reliable online learning to rank for information retrieval.

**中文**

欧洲语言资源协会 (ELRA)，日本宫崎。 https://aclanthology.org/L18-1544 [10] 桂良科、王博瑞、黄秋园、Alexander Hauptmann、Yonatan Bisk 和高剑锋。 2022.KAT：视觉和语言的知识增强Transformer。计算语言学协会北美分会 2022 年会议记录：人类语言技术。计算语言学协会，美国西雅图，956–968。 https://doi.org/10.18653/v1/2022.naacl-main.70 [11] 卡佳·霍夫曼。 2013. 快速可靠的在线学习对信息检索进行排名。

### 段落 104 · Page 10

**EN**

SIGIR Forum 47, 2 (jan 2013), 140. https://doi.org/10.1145/2568388. 2568413 [12] Steven C. H. Hoi, Doyen Sahoo, Jing Lu, and Peilin Zhao. 2018. Online Learning: A Comprehensive Survey. arXiv:1802.02871 [cs.LG] https://arxiv.org/abs/1802. 02871 [13] Gautier Izacard, Mathilde Caron, Lucas Hosseini, Sebastian Riedel, Piotr Bojanowski, Armand Joulin, and Edouard Grave. 2022. Unsupervised Dense Information Retrieval with Contrastive Learning. Transactions on Machine Learning Research (2022). https://openreview.net/forum?id=jKN1pXi7b0 [14] Gautier Izacard and Edouard Grave. 2020. Distilling Knowledge from Reader to Retriever for Question Answering.

**中文**

SIGIR 论坛 47, 2（2013 年 1 月），140。https://doi.org/10.1145/2568388。 2568413 [12] Steven C. H. Hoi、Doyen Sahoo、Jing Lu 和 Peilin Zhu。 2018。在线学习：综合调查。 arXiv:1802.02871 [cs.LG] https://arxiv.org/abs/1802。 02871 [13] Gautier Izacard、Mathilde Caron、Lucas Hosseini、Sebastian Riedel、Piotr Bojanowski、Armand Joulin 和 Edouard Grave。 2022.通过对比学习进行无监督密集信息检索。机器学习研究汇刊 (2022)。 https://openreview.net/forum?id=jKN1pXi7b0 [14] Gautier Izacard 和 Edouard Grave。 2020。从读者那里提取知识以供检索器回答问题。

### 段落 105 · Page 10

**EN**

https://arxiv.org/abs/2012.04584 [15] Gautier Izacard and Edouard Grave. 2021. Leveraging Passage Retrieval with Generative Models for Open Domain Question Answering. In Proceedings of the 16th Conference of the European Chapter of the Association for Computational Linguistics: Main Volume . Association for Computational Linguistics, Online, 874–880. https://doi.org/10.18653/v1/2021.eacl-main.74 [16] Gautier Izacard, Patrick Lewis, Maria Lomeli, Lucas Hosseini, Fabio Petroni, Timo Schick, Jane Dwivedi-Yu, Armand Joulin, Sebastian Riedel, and Edouard Grave. 2023. Atlas: Few-shot Learning with Retrieval Augmented Language Models.

**中文**

https://arxiv.org/abs/2012.04584 [15]戈蒂埃·伊扎卡尔和爱德华·格雷夫。 2021。利用段落检索和生成模型进行开放域问答。计算语言学协会欧洲分会第 16 届会议记录：主卷。计算语言学协会，在线，874–880。 https://doi.org/10.18653/v1/2021.eacl-main.74 [16] Gautier Izacard、Patrick Lewis、Maria Lomeli、Lucas Hosseini、Fabio Petroni、Timo Schick、Jane Dwivedi-Yu、Armand Joulin、Sebastian Riedel 和 Edouard Grave。 2023. Atlas：利用检索增强语言模型进行小样本学习。

### 段落 106 · Page 10

**EN**

Journal of Machine Learning Research 24, 251 (2023), 1–43. http://jmlr.org/papers/ v24/23-0037.html [17] Thorsten Joachims and Filip Radlinski. 2007. Search Engines that Learn from Implicit Feedback. Computer 40, 8 (2007), 34–40. https://doi.org/10.1109/MC. 2007.289 [18] Thorsten Joachims, Adith Swaminathan, and Tobias Schnabel. 2017. Unbiased Learning-to-Rank with Biased Feedback. In Proceedings of the Tenth ACM International Conference on Web Search and Data Mining (Cambridge, United Kingdom) (WSDM ’17). Association for Computing Machinery, New York, NY, USA, 781–789.

**中文**

机器学习研究杂志 24, 251 (2023), 1–43。 http://jmlr.org/papers/v24/23-0037.html [17] 托尔斯滕·约阿希姆斯和菲利普·拉德林斯基。 2007。从隐式反馈中学习的搜索引擎。计算机 40, 8 (2007), 34–40。 https://doi.org/10.1109/MC。 2007.289 [18]托尔斯滕·约阿希姆斯、阿迪斯·斯瓦米纳坦和托比亚斯·施纳贝尔。 2017.带有偏见反馈的无偏见学习排名。第十届 ACM 国际网络搜索和数据挖掘会议（英国剑桥）会议记录 (WSDM '17)。计算机协会，美国纽约州纽约市，781–789。

### 段落 107 · Page 10

**EN**

https://doi.org/10.1145/3018661.3018699 [19] Mandar Joshi, Eunsol Choi, Daniel Weld, and Luke Zettlemoyer. 2017. TriviaQA: A Large Scale Distantly Supervised Challenge Dataset for Reading Comprehension. In Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) , Regina Barzilay and Min-Yen Kan (Eds.). Association for Computational Linguistics, Vancouver, Canada, 1601–1611. https: //doi.org/10.18653/v1/P17-1147 [20] Vladimir Karpukhin, Barlas Oguz, Sewon Min, Patrick Lewis, Ledell Wu, Sergey Edunov, Danqi Chen, and Wen-tau Yih. 2020.

**中文**

https://doi.org/10.1145/3018661.3018699 [19] Mandar Joshi、Eunsol Choi、Daniel Weld 和 Luke Zettlemoyer。 2017.TriviaQA：用于阅读理解的大规模远程监督挑战数据集。计算语言学协会第 55 届年会记录（第一卷：长论文），Regina Barzilay 和 Min-Yen Kan（编辑）。计算语言学协会，加拿大温哥华，1601-1611 年。 https://doi.org/10.18653/v1/P17-1147 [20] Vladimir Karpukhin、Barlas Oguz、Sewon Min、Patrick Lewis、Ledell Wu、Sergey Edunov、Danqi Chen 和 Wen-tau Yih。 2020.

### 段落 108 · Page 10

**EN**

Dense Passage Retrieval for Open- Domain Question Answering. In Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP) . Association for Computational Linguistics, Online, 6769–6781. https://doi.org/10.18653/v1/2020.emnlp-main.550 [21] To Eun Kim, Alireza Salemi, Andrew Drozdov, Fernando Diaz, and Hamed Zamani. 2024. Retrieval-Enhanced Machine Learning: Synthesis and Opportunities. arXiv:2407.12982 [cs.LG] https://arxiv.org/abs/2407.12982 [22] Diederik P. Kingma and Jimmy Ba. 2017. Adam: A Method for Stochastic Optimization.

**中文**

用于开放域问答的密集段落检索。 2020 年自然语言处理经验方法 (EMNLP) 会议论文集。计算语言学协会，在线，6769–6781。 https://doi.org/10.18653/v1/2020.emnlp-main.550 [21] 致 Eun Kim、Alireza Salemi、Andrew Drozdov、Fernando Diaz 和 Hamed Zamani。 2024.检索增强型机器学习：综合和机遇。 arXiv:2407.12982 [cs.LG] https://arxiv.org/abs/2407.12982 [22] Diederik P. Kingma 和 Jimmy Ba。 2017. Adam：一种随机优化方法。

### 段落 109 · Page 10

**EN**

arXiv:1412.6980 [cs.LG] [23] Ishita Kumar, Snigdha Viswanathan, Sushrita Yerra, Alireza Salemi, Ryan A. Rossi, Franck Dernoncourt, Hanieh Deilamsalehy, Xiang Chen, Ruiyi Zhang, Shubham Agarwal, Nedim Lipka, and Hamed Zamani. 2024. LongLaMP: A Benchmark for Personalized Long-form Text Generation. arXiv:2407.11016 [cs.CL] https: //arxiv.org/abs/2407.11016 [24] Tom Kwiatkowski, Jennimaria Palomaki, Olivia Redfield, Michael Collins, Ankur Parikh, Chris Alberti, Danielle Epstein, Illia Polosukhin, Jacob Devlin, Kenton Lee, Kristina Toutanova, Llion Jones, Matthew Kelcey, Ming-Wei Chang, Andrew M. Dai, Jakob Uszkoreit, Quoc Le, and Slav Petrov.

**中文**

arXiv:1412.6980 [cs.LG] [23] Ishita Kumar、Snigdha Viswanathan、Sushrita Yerra、Alireza Salemi、Ryan A. Rossi、Franck Dernoncourt、Hanieh Deilamsalehy、Xiang Chen、Ruiyi Zhu、Shubham Agarwal、Nedim Lipka 和 Hamed Zamani。 2024.LongLaMP：个性化长文本生成的基准。 arXiv:2407.11016 [cs.CL] https: //arxiv.org/abs/2407.11016 [24] Tom Kwiatkowski、Jennimaria Palomaki、Olivia Redfield、Michael Collins、Ankur Parikh、Chris Alberti、Danielle Epstein、Illia Polosukhin、Jacob Devlin、Kenton Lee、Kristina Toutanova、Llion Jones、 Matthew Kelcey、Ming-Wei Chang、Andrew M. Dai、Jakob Uszkoreit、Quoc Le 和 Slav Petrov。

### 段落 110 · Page 10

**EN**

2019. Natural Questions: A Benchmark for Question Answering Research. Transactions of the Association for Computational Linguistics 7 (2019), 452–466. https://doi.org/10.1162/tacl_a_00276 [25] Omer Levy, Minjoon Seo, Eunsol Choi, and Luke Zettlemoyer. 2017. Zero-Shot Relation Extraction via Reading Comprehension. In Proceedings of the 21st Conference on Computational Natural Language Learning (CoNLL 2017) , Roger Levy and Lucia Specia (Eds.). Association for Computational Linguistics, Vancouver, Canada, 333–342.

**中文**

2019。自然问题：问答研究的基准。计算语言学协会汇刊 7 (2019), 452–466。 https://doi.org/10.1162/tacl_a_00276 [25] Omer Levy、Minjoon Seo、Eunsol Choi 和 Luke Zettlemoyer。 2017.通过阅读理解进行零样本关系提取。在第 21 届计算自然语言学习会议 (CoNLL 2017) 的会议记录中，Roger Levy 和 Lucia Specia（编辑）。计算语言学协会，加拿大温哥华，333-342。

### 段落 111 · Page 10

**EN**

https://doi.org/10.18653/v1/K17-1034 [26] Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Veselin Stoyanov, and Luke Zettlemoyer. 2020. BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension. In Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics . Association for Computational Linguistics, Online, 7871–7880.

**中文**

https://doi.org/10.18653/v1/K17-1034 [26] Mike Lewis、Yinhan Liu、Naman Goyal、Marjan Ghazvininejad、Abdelrahman Mohamed、Omer Levy、Veselin Stoyanov 和 Luke Zettlemoyer。 2020.BART：用于自然语言生成、翻译和理解的去噪序列到序列预训练。计算语言学协会第 58 届年会论文集。计算语言学协会，在线，7871–7880。

### 段落 112 · Page 10

**EN**

https://doi.org/10.18653/v1/2020.acl-main.703 [27] Patrick Lewis, Ethan Perez, Aleksandra Piktus, Fabio Petroni, Vladimir Karpukhin, Naman Goyal, Heinrich Küttler, Mike Lewis, Wen-tau Yih, Tim Rocktäschel, Sebastian Riedel, and Douwe Kiela. 2020. Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks. In Proceedings of the 34th International Conference on Neural Information Processing Systems (Vancouver, BC, Canada) (NIPS’20). Curran Associates Inc., Red Hook, NY, USA, Article 793, 16 pages. [28] Tie-Yan Liu. 2009. Learning to Rank for Information Retrieval. Found. Trends Inf. Retr. 3, 3 (March 2009), 225–331.

**中文**

https://doi.org/10.18653/v1/2020.acl-main.703 [27] Patrick Lewis、Ethan Perez、Aleksandra Piktus、Fabio Petroni、Vladimir Karpukhin、Naman Goyal、Heinrich Küttler、Mike Lewis、Wen-tau Yih、Tim Rocktäschel、Sebastian Riedel 和 Douwe Kiela。 2020.知识密集型 NLP 任务的检索增强生成。第 34 届神经信息处理系统国际会议（加拿大不列颠哥伦比亚省温哥华）（NIPS’20）论文集。 Curran Associates Inc.，美国纽约州雷德胡克，第 793 条，16 页。 [28] 刘铁燕. 2009。学习信息检索排名。成立。趋势信息。撤回。 3, 3（2009 年 3 月），225–331。

### 段落 113 · Page 10

**EN**

https://doi.org/10.1561/1500000016 [29] Bryan McCann, Nitish Shirish Keskar, Caiming Xiong, and Richard Socher. 2019. The Natural Language Decathlon: Multitask Learning as Question Answering. https://openreview.net/forum?id=B1lfHhR9tm [30] Quinn McNemar. 1947. Note on the sampling error of the difference between correlated proportions or percentages. Psychometrika 12, 2 (1947), 153–157. https://doi.org/10.1007/BF02295996 [31] Rodrigo Nogueira and Kyunghyun Cho. 2020. Passage Re-ranking with BERT.

**中文**

https://doi.org/10.1561/1500000016 [29] Bryan McCann、Nitish Shirish Keskar、Caiming Xiong 和 Richard Socher。 2019。自然语言十项全能：多任务学习作为问答。 https://openreview.net/forum?id=B1lfHhR9tm [30] 奎因·麦克尼马尔。 1947.注意相关比例或百分比之间差异的抽样误差。心理测量 12, 2 (1947), 153–157。 https://doi.org/10.1007/BF02295996 [31] 罗德里戈·诺盖拉和曹京贤。 2020. 使用 BERT 进行段落重排。

### 段落 114 · Page 10

**EN**

arXiv:1901.04085 [cs.IR] [32] Fabio Petroni, Aleksandra Piktus, Angela Fan, Patrick Lewis, Majid Yazdani, Nicola De Cao, James Thorne, Yacine Jernite, Vladimir Karpukhin, Jean Maillard, Vassilis Plachouras, Tim Rocktäschel, and Sebastian Riedel. 2021. KILT: a Benchmark for Knowledge Intensive Language Tasks. In Proceedings of the

**中文**

arXiv:1901.04085 [cs.IR] [32] Fabio Petroni、Aleksandra Piktus、Angela Fan、Patrick Lewis、Majid Yazdani、Nicola De Cao、James Thorne、Yacine Jernite、Vladimir Karpukhin、Jean Maillard、Vassilis Plachouras、Tim Rocktäschel 和 Sebastian Riedel。 2021.KILT：知识密集型语言任务的基准。在诉讼程序中

### Page 11

### 段落 115 · Page 11

**EN**

Learning to Rank for Multiple Retrieval-Augmented Models through Iterative Utility Maximization ICTIR ’25, July 18, 2025, Padua, Italy 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies . Association for Computational Linguistics, Online, 2523–2544. https://doi.org/10.18653/v1/2021.naacl-main.200 [33] Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, and Peter J. Liu. 2020. Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer.J. Mach. Learn. Res.

**中文**

通过迭代效用最大化学习对多个检索增强模型进行排名 ICTIR’25，2025 年 7 月 18 日，意大利帕多瓦 2021 年计算语言学协会北美分会会议：人类语言技术。计算语言学协会，在线，2523–2544。 https://doi.org/10.18653/v1/2021.naacl-main.200 [33] Colin Raffel、Noam Shazeer、Adam Roberts、Katherine Lee、Sharan Narang、Michael Matena、Yanqi Zhou、Wei Li 和 Peter J. Liu。 2020。用统一的文本到文本转换器探索迁移学习的局限性。J。马赫。学习。资源。

### 段落 116 · Page 11

**EN**

21, 1, Article 140 (jan 2020), 67 pages. [34] Pranav Rajpurkar, Jian Zhang, Konstantin Lopyrev, and Percy Liang. 2016. SQuAD: 100,000+ Questions for Machine Comprehension of Text. In Proceedings of the 2016 Conference on Empirical Methods in Natural Language Processing. Association for Computational Linguistics, Austin, Texas, 2383–2392. https://doi.org/10.18653/v1/D16-1264 [35] Stephen E. Robertson, Steve Walker, Susan Jones, Micheline Hancock-Beaulieu, and Mike Gatford. 1994. Okapi at TREC-3. In Text Retrieval Conference.

**中文**

21, 1，第 140 条（2020 年 1 月），67 页。 [34] Pranav Rajpurkar，张健，康斯坦丁·洛佩列夫，珀西·梁。 2016.SQuAD：100,000 多个机器理解文本的问题。 2016 年自然语言处理经验方法会议论文集。计算语言学协会，德克萨斯州奥斯汀，2383-2392。 https://doi.org/10.18653/v1/D16-1264 [35] 斯蒂芬·E·罗伯逊、史蒂夫·沃克、苏珊·琼斯、米什琳·汉考克-博利厄和迈克·盖特福德。 1994 年。霍加狓在 TREC-3。在文本检索会议中。

### 段落 117 · Page 11

**EN**

https: //api.semanticscholar.org/CorpusID:3946054 [36] Devendra Sachan, Mostofa Patwary, Mohammad Shoeybi, Neel Kant, Wei Ping, William L. Hamilton, and Bryan Catanzaro. 2021. End-to-End Training of Neural Retrievers for Open-Domain Question Answering. In Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (Volume 1: Long Papers). Association for Computational Linguistics, Online, 6648–6662. https: //doi.org/10.18653/v1/2021.acl-long.519 [37] Alireza Salemi, Juan Altmayer Pizzorno, and Hamed Zamani. 2023.

**中文**

https://api.semanticscholar.org/CorpusID:3946054 [36] Devendra Sachan、Mostofa Patwary、Mohammad Shoeybi、Neel Kant、Wei Ping、William L. Hamilton 和 Bryan Catanzaro。 2021。开放域问答神经检索器的端到端训练。计算语言学协会第 59 届年会暨第 11 届自然语言处理国际联合会议论文集（第一卷：长论文）。计算语言学协会，在线，6648–6662。 https://doi.org/10.18653/v1/2021.acl-long.519 [37] Alireza Salemi、Juan Altmayer Pizzorno 和 Hamed Zamani。 2023 年。

### 段落 118 · Page 11

**EN**

A Symmetric Dual Encoding Dense Retrieval Framework for Knowledge-Intensive Visual Question Answering. In Proceedings of the 46th International ACM SI- GIR Conference on Research and Development in Information Retrieval (<confloc>, <city>Taipei</city>, <country>Taiwan</country>, </conf-loc>) (SIGIR ’23). Association for Computing Machinery, New York, NY, USA, 110–120. https://doi.org/10.1145/3539618.3591629 [38] Alireza Salemi, Surya Kallumadi, and Hamed Zamani. 2024. Optimization Methods for Personalizing Large Language Models through Retrieval Augmentation.

**中文**

用于知识密集型视觉问答的对称双编码密集检索框架。第 46 届国际 ACM SIGIR 信息检索研究与开发会议论文集（<confloc>、<city>Taipei</city>、<country>Taiwan</country>、</conf-loc>）（SIGIR '23）。计算机协会，美国纽约州纽约市，110–120。 https://doi.org/10.1145/3539618.3591629 [38] Alireza Salemi、Surya Kallumadi 和 Hamed Zamani。 2024。通过检索增强个性化大型语言模型的优化方法。

### 段落 119 · Page 11

**EN**

In Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval (Washington DC, USA) (SI- GIR ’24). Association for Computing Machinery, New York, NY, USA, 752–762. https://doi.org/10.1145/3626772.3657783 [39] Alireza Salemi, Julian Killingback, and Hamed Zamani. 2025. ExPerT: Effective and Explainable Evaluation of Personalized Long-Form Text Generation. arXiv:2501.14956 [cs.CL] https://arxiv.org/abs/2501.14956 [40] Alireza Salemi, Cheng Li, Mingyang Zhang, Qiaozhu Mei, Weize Kong, Tao Chen, Zhuowan Li, Michael Bendersky, and Hamed Zamani. 2025.

**中文**

第 47 届国际 ACM SIGIR 信息检索研究与开发会议（美国华盛顿）（SI-GIR '24）论文集。计算机协会，美国纽约州纽约市，752–762。 https://doi.org/10.1145/3626772.3657783 [39] Alireza Salemi、Julian Killingback 和 Hamed Zamani。 2025.ExperT：个性化长文本生成的有效且可解释的评估。 arXiv:2501.14956 [cs.CL] https://arxiv.org/abs/2501.14956 [40] Alireza Salemi、Cheng Li、Mingyang Zhang、Qiaozhu Mei、Weize Kong、Tao Chen、Zhuowan Li、Michael Bendersky 和 ​​Hamed Zamani。 2025 年。

### 段落 120 · Page 11

**EN**

Reasoning-Enhanced Self-Training for Long-Form Personalized Text Generation. arXiv:2501.04167 [cs.CL] https://arxiv.org/abs/2501.04167 [41] Alireza Salemi, Sheshera Mysore, Michael Bendersky, and Hamed Zamani. 2024. LaMP: When Large Language Models Meet Personalization. In Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) , Lun-Wei Ku, Andre Martins, and Vivek Srikumar (Eds.). Association for Computational Linguistics, Bangkok, Thailand, 7370–7392. https://aclanthology.org/2024.acl-long.399 [42] Alireza Salemi, Mahta Rafiee, and Hamed Zamani. 2023.

**中文**

长格式个性化文本生成的推理增强自我训练。 arXiv:2501.04167 [cs.CL] https://arxiv.org/abs/2501.04167 [41] Alireza Salemi、Sheshera Mysore、Michael Bendersky 和 ​​Hamed Zamani。 2024. LaMP：当大型语言模型遇到个性化时。计算语言学协会第 62 届年会记录（第一卷：长论文），Lun-Wei Ku、Andre Martins 和 Vivek Srikumar（编辑）。计算语言学协会，泰国曼谷，7370–7392。 https://aclanthology.org/2024.acl-long.399 [42] Alireza Salemi、Mahta Rafiee 和 Hamed Zamani。 2023 年。

### 段落 121 · Page 11

**EN**

Pre-Training Multi- Modal Dense Retrievers for Outside-Knowledge Visual Question Answering. In Proceedings of the 2023 ACM SIGIR International Conference on Theory of Information Retrieval (Taipei, Taiwan) (ICTIR ’23). Association for Computing Machinery, New York, NY, USA, 169–176. https://doi.org/10.1145/3578337.3605137 [43] Alireza Salemi and Hamed Zamani. 2024. Comparing Retrieval-Augmentation and Parameter-Efficient Fine-Tuning for Privacy-Preserving Personalization of Large Language Models. arXiv:2409.09510 [cs.CL] https://arxiv.org/abs/2409.09510 [44] Alireza Salemi and Hamed Zamani. 2024.

**中文**

用于外部知识视觉问答的预训练多模态密集检索器。 2023 年 ACM SIGIR 国际信息检索理论会议（台湾台北）会议记录 (ICTIR ’23)。计算机协会，美国纽约州纽约市，169–176。 https://doi.org/10.1145/3578337.3605137 [43] Alireza Salemi 和 Hamed Zamani。 2024。比较检索增强和参数高效微调以实现大型语言模型的隐私保护个性化。 arXiv:2409.09510 [cs.CL] https://arxiv.org/abs/2409.09510 [44] Alireza Salemi 和 Hamed Zamani。 2024 年。

### 段落 122 · Page 11

**EN**

Evaluating Retrieval Quality in Retrieval-Augmented Generation. In Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval (Washington DC, USA) (SIGIR ’24). Association for Computing Machinery, New York, NY, USA, 2395–2400. https://doi.org/10.1145/3626772.3657957 [45] Alireza Salemi and Hamed Zamani. 2024. Towards a Search Engine for Machines: Unified Ranking for Multiple Retrieval-Augmented Large Language Models. In Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval (Washington DC, USA) (SI- GIR ’24).

**中文**

评估检索增强生成中的检索质量。第 47 届国际 ACM SIGIR 信息检索研究与开发会议（美国华盛顿）（SIGIR '24）论文集。计算机协会，美国纽约州纽约市，2395–2400。 https://doi.org/10.1145/3626772.3657957 [45] Alireza Salemi 和 Hamed Zamani。 2024.迈向机器搜索引擎：多种检索增强大型语言模型的统一排名。第 47 届国际 ACM SIGIR 信息检索研究与开发会议（美国华盛顿）（SI-GIR '24）论文集。

### 段落 123 · Page 11

**EN**

Association for Computing Machinery, New York, NY, USA, 741–751. https://doi.org/10.1145/3626772.3657733 [46] Keshav Santhanam, Omar Khattab, Jon Saad-Falcon, Christopher Potts, and Matei Zaharia. 2022. ColBERTv2: Effective and Efficient Retrieval via Lightweight Late Interaction. In Proceedings of the 2022 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies . Association for Computational Linguistics, Seattle, United States, 3715–3734. https://doi.org/10.18653/v1/2022.naacl-main.272 [47] Kurt Shuster, Spencer Poff, Moya Chen, Douwe Kiela, and Jason Weston. 2021.

**中文**

计算机协会，美国纽约州纽约市，741–751。 https://doi.org/10.1145/3626772.3657733 [46] Keshav Santhanam、Omar Khattab、Jon Saad-Falcon、Christopher Potts 和 Matei Zaharia。 2022. ColBERTv2：通过轻量级后期交互进行有效且高效的检索。计算语言学协会北美分会 2022 年会议记录：人类语言技术。计算语言学协会，美国西雅图，3715–3734。 https://doi.org/10.18653/v1/2022.naacl-main.272 [47] Kurt Shuster、Spencer Poff、Moya Chen、Douwe Kiela 和 Jason Weston。 2021 年。

### 段落 124 · Page 11

**EN**

Retrieval Augmentation Reduces Hallucination in Conversation. In Findings of the Association for Computational Linguistics: EMNLP 2021 . Association for Computational Linguistics, Punta Cana, Dominican Republic, 3784–3803. https: //doi.org/10.18653/v1/2021.findings-emnlp.320 [48] Ahu Sieg, Bamshad Mobasher, and Robin Burke. 2007. Web search personalization with ontological user profiles. In Proceedings of the Sixteenth ACM Conference on Conference on Information and Knowledge Management (Lisbon, Portugal) (CIKM ’07). Association for Computing Machinery, New York, NY, USA, 525–534.

**中文**

检索增强减少谈话中的幻觉。计算语言学协会的调查结果：EMNLP 2021。计算语言学协会，多米尼加共和国蓬塔卡纳，3784-3803。 https://doi.org/10.18653/v1/2021.findings-emnlp.320 [48] Ahu Sieg、Bamshad Mobasher 和 Robin Burke。 2007. 使用本体用户配置文件的网络搜索个性化。第十六届 ACM 信息和知识管理会议（葡萄牙里斯本）会议记录（CIKM ’07）。计算机协会，美国纽约州纽约市，525–534。

### 段落 125 · Page 11

**EN**

https://doi.org/10.1145/1321440.1321515 [49] Avi Singh, John D Co-Reyes, Rishabh Agarwal, Ankesh Anand, Piyush Patil, Xavier Garcia, Peter J Liu, James Harrison, Jaehoon Lee, Kelvin Xu, Aaron T Parisi, Abhishek Kumar, Alexander A Alemi, Alex Rizkowsky, Azade Nova, Ben Adlam, Bernd Bohnet, Gamaleldin Fathy Elsayed, Hanie Sedghi, Igor Mordatch, Isabelle Simpson, Izzeddin Gur, Jasper Snoek, Jeffrey Pennington, Jiri Hron, Kathleen Kenealy, Kevin Swersky, Kshiteej Mahajan, Laura A Culp, Lechao Xiao, Maxwell Bileschi, Noah Constant, Roman Novak, Rosanne Liu, Tris Warkentin, Yamini Bansal, Ethan Dyer, Behnam Neyshabur, Jascha Sohl-Dickstein, and Noah Fiedel.

**中文**

https://doi.org/10.1145/1321440.1321515 [49] Avi Singh、John D Co-Reyes、Rishabh Agarwal、Ankesh Anand、Piyush Patil、Xavier Garcia、Peter J Liu、James Harrison、Jaehoon Lee、Kelvin Xu、Aaron T Parisi、Abhishek Kumar、Alexander A Alemi、Alex里兹科夫斯基、阿扎德·诺瓦、本·阿德拉姆、贝恩德·博内特、加马雷丁·法西·艾尔赛义德、哈妮·塞吉、伊戈尔·莫达奇、伊莎贝尔·辛普森、伊兹丁·古尔、贾斯帕·斯诺克、杰弗里·潘宁顿、吉里·赫隆、凯瑟琳·肯尼利、凯文·斯沃斯基、克希提·马哈詹、劳拉·卡尔普、肖乐超、马克斯韦尔·比莱斯奇、诺亚·康斯坦特、罗曼·诺瓦克、Rosanne Liu、Tris Warkentin、Yamini Bansal、Ethan Dyer、Behnam Neyshabur、Jascha Sohl-Dickstein 和 Noah Fiedel。

### 段落 126 · Page 11

**EN**

2024. Beyond Human Data: Scaling Self-Training for Problem-Solving with Language Models. Transactions on Machine Learning Research (2024). https: //openreview.net/forum?id=lNAyUngGFK Expert Certification. [50] Devendra Singh, Siva Reddy, Will Hamilton, Chris Dyer, and Dani Yogatama. 2021. End-to-End Training of Multi-Document Reader and Retriever for Open- Domain Question Answering. In Advances in Neural Information Processing Systems, M. Ranzato, A. Beygelzimer, Y. Dauphin, P.S. Liang, and J. Wortman Vaughan (Eds.), Vol. 34. Curran Associates, Inc., 25968–25981. https://proceedings.neurips.

**中文**

2024.超越人类数据：利用语言模型扩展自我训练以解决问题。机器学习研究汇刊 (2024)。 https://openreview.net/forum?id=lNAyUngGFK 专家认证。 [50]德文德拉·辛格、西瓦·雷迪、威尔·汉密尔顿、克里斯·戴尔和丹尼·瑜伽塔玛。 2021。开放域问答的多文档阅读器和检索器的端到端培训。 《神经信息处理系统进展》，M. Ranzato、A. Beygelzimer、Y. Dauphin、P.S.梁，和 J. Wortman Vaughan（编辑），卷。 34.Curran Associates, Inc.，25968–25981。 https://proceedings.neurips。

### 段落 127 · Page 11

**EN**

cc/paper_files/paper/2021/file/da3fde159d754a2555eaa198d2d105b2-Paper.pdf [51] Shamane Siriwardhana, Rivindu Weerasekera, Elliott Wen, Tharindu Kaluarachchi, Rajib Rana, and Suranga Nanayakkara. 2023. Improving the Domain Adaptation of Retrieval Augmented Generation (RAG) Models for Open Domain Question Answering. Transactions of the Association for Computational Linguistics 11 (2023), 1–17. https://doi.org/10.1162/tacl_a_00530 [52] Ilya Sutskever, Oriol Vinyals, and Quoc V. Le. 2014. Sequence to sequence learning with neural networks.

**中文**

cc/paper_files/paper/2021/file/da3fde159d754a2555eaa198d2d105b2-Paper.pdf [51] Shamane Siriwardhana、Rivindu Weerasekera、Elliott Wen、Tharindu Kaluarachchi、Rajib Rana 和 Suranga Nanayakkara。 2023。改进开放域问答的检索增强生成（RAG）模型的域适应。计算语言学协会汇刊 11 (2023), 1–17。 https://doi.org/10.1162/tacl_a_00530 [52] Ilya Sutskever、Oriol Vinyals 和 Quoc V. Le。 2014. 使用神经网络进行序列到序列学习。

### 段落 128 · Page 11

**EN**

InProceedings of the 27th International Conference on Neural Information Processing Systems - Volume 2 (Montreal, Canada) (NIPS’14). MIT Press, Cambridge, MA, USA, 3104–3112. [53] James Thorne, Andreas Vlachos, Christos Christodoulopoulos, and Arpit Mittal. 2018. FEVER: a Large-scale Dataset for Fact Extraction and VERification. In Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers). Association for Computational Linguistics, New Orleans, Louisiana, 809–819.

**中文**

第 27 届神经信息处理系统国际会议记录 - 第 2 卷（加拿大蒙特利尔）(NIPS’14)。麻省理工学院出版社，美国马萨诸塞州剑桥，3104–3112。 [53] 詹姆斯·索恩、安德烈亚斯·弗拉科斯、克里斯托·克里斯托杜洛普洛斯和阿尔皮特·米塔尔。 2018。FEVER：用于事实提取和验证的大规模数据集。计算语言学协会北美分会 2018 年会议记录：人类语言技术，第 1 卷（长论文）。计算语言学协会，路易斯安那州新奥尔良，809-819。

### 段落 129 · Page 11

**EN**

https://doi.org/10.18653/v1/N18-1074 [54] Nuno Vasconcelos and Andrew Lippman. 1999. Learning from User Feedback in Image Retrieval Systems. In Advances in Neural Information Processing Systems , S. Solla, T. Leen, and K. Müller (Eds.), Vol. 12. MIT Press. https://proceedings.neurips.cc/paper_files/paper/1999/file/ 7283518d47a05a09d33779a17adf1707-Paper.pdf [55] Alex Wang, Yada Pruksachatkun, Nikita Nangia, Amanpreet Singh, Julian Michael, Felix Hill, Omer Levy, and Samuel R. Bowman. 2019.SuperGLUE: a stickier benchmark for general-purpose language understanding systems . Curran Associates Inc., Red Hook, NY, USA.

**中文**

https://doi.org/10.18653/v1/N18-1074 [54] 努诺·瓦斯康塞洛斯和安德鲁·利普曼。 1999。从图像检索系统中的用户反馈中学习。 《神经信息处理系统进展》，S. Solla、T. Leen 和 K. Müller（编辑），卷。 12. 麻省理工学院出版社。 https://proceedings.neurips.cc/paper_files/paper/1999/file/7283518d47a05a09d33779a17adf1707-Paper.pdf [55] Alex Wang、Yada Pruksachatkun、Nikita Nangia、Amanpreet Singh、Julian Michael、Felix Hill、Omer Levy 和 Samuel R. Bowman。 2019.SuperGLUE：通用语言理解系统的更具粘性的基准。 Curran Associates Inc.，美国纽约州雷德胡克。

### 段落 130 · Page 11

**EN**

[56] Alex Wang, Amanpreet Singh, Julian Michael, Felix Hill, Omer Levy, and Samuel Bowman. 2018. GLUE: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding. In Proceedings of the 2018 EMNLP Workshop BlackboxNLP: Analyzing and Interpreting Neural Networks for NLP . Association for Computational Linguistics, Brussels, Belgium, 353–355. https://doi.org/10. 18653/v1/W18-5446 [57] Dingmin Wang, Qiuyuan Huang, Matthew Jackson, and Jianfeng Gao. 2024. Retrieve What You Need: A Mutual Learning Framework for Open-domain Question Answering. Transactions of the Association for Computational Linguistics 12 (2024), 247–263.

**中文**

[56] Alex Wang、Amanpreet Singh、Julian Michael、Felix Hill、Omer Levy 和 Samuel Bowman。 2018. GLUE：自然语言理解的多任务基准和分析平台。 2018 年 EMNLP 研讨会 BlackboxNLP 论文集：分析和解释 NLP 神经网络。计算语言学协会，比利时布鲁塞尔，353-355。 https://doi.org/10。 18653/v1/W18-5446 [57] 王鼎民，黄秋园，马修·杰克逊，高剑峰。 2024.检索您需要的东西：开放域问答的相互学习框架。计算语言学协会汇刊 12 (2024), 247–263。

### 段落 131 · Page 11

**EN**

https://doi.org/10.1162/tacl_a_00646 [58] Liang Wang, Nan Yang, Xiaolong Huang, Binxing Jiao, Linjun Yang, Daxin Jiang, Rangan Majumder, and Furu Wei. 2024. Text Embeddings by Weakly-Supervised Contrastive Pre-training. arXiv:2212.03533 [cs.CL] https://arxiv.org/abs/2212. 03533 [59] Sohee Yang and Minjoon Seo. 2020. Is Retriever Merely an Approximator of Reader? arXiv:2010.10999 [cs.CL] [60] Zhilin Yang, Peng Qi, Saizheng Zhang, Yoshua Bengio, William Cohen, Ruslan Salakhutdinov, and Christopher D. Manning. 2018. HotpotQA: A Dataset for Diverse, Explainable Multi-hop Question Answering.

**中文**

https://doi.org/10.1162/tacl_a_00646 [58] 王亮，杨南，黄晓龙，焦斌兴，杨林军，姜大新，Rangan Majumder，魏福如。 2024.弱监督对比预训练的文本嵌入。 arXiv:2212.03533 [cs.CL] https://arxiv.org/abs/2212。 03533 [59] Sohee Yang 和 Minjoon Seo。 2020. Retriever 仅仅是 Reader 的近似器吗？ arXiv:2010.10999 [cs.CL] [60] 杨志林、齐鹏、张赛正、Yoshua Bengio、William Cohen、Ruslan Salakhutdinov 和 Christopher D. Manning。 2018.HotpotQA：多样化、可解释的多跳问答数据集。

### 段落 132 · Page 11

**EN**

In Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing , Ellen Riloff, David Chiang, Julia Hockenmaier, and Jun’ichi Tsujii (Eds.). Association for Computational Linguistics, Brussels, Belgium, 2369–2380. https://doi.org/10. 18653/v1/D18-1259 [61] Hamed Zamani and Michael Bendersky. 2024. Stochastic RAG: End-to-End Retrieval-Augmented Generation through Expected Utility Maximization. In Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval (Washington DC, USA) (SIGIR ’24). Association for Computing Machinery, New York, NY, USA, 2641–2646.

**中文**

2018 年自然语言处理经验方法会议论文集，Ellen Riloff、David Jiang、Julia Hockenmaier 和 Jun’ichi Tsujii（编辑）。计算语言学协会，比利时布鲁塞尔，2369-2380。 https://doi.org/10。 18653/v1/D18-1259 [61] 哈米德·扎马尼和迈克尔·本德斯基。 2024.随机 RAG：通过预期效用最大化实现端到端检索增强生成。第 47 届国际 ACM SIGIR 信息检索研究与开发会议（美国华盛顿）（SIGIR '24）论文集。计算机协会，美国纽约州纽约市，2641–2646。

### 段落 133 · Page 11

**EN**

https: //doi.org/10.1145/3626772.3657923 [62] Hamed Zamani, Fernando Diaz, Mostafa Dehghani, Donald Metzler, and Michael Bendersky. 2022. Retrieval-Enhanced Machine Learning. InProceedings of the 45th International ACM SIGIR Conference on Research and Development in Information

**中文**

https://doi.org/10.1145/3626772.3657923 [62] Hamed Zamani、Fernando Diaz、Mostafa Dehghani、Donald Metzler 和 Michael Bendersky。 2022。检索增强机器学习。第 45 届国际 ACM SIGIR 信息研究与发展会议论文集

### Page 12

### 段落 134 · Page 12

**EN**

ICTIR ’25, July 18, 2025, Padua, Italy Alireza Salemi and Hamed Zamani Retrieval (, Madrid, Spain,) (SIGIR ’22). Association for Computing Machinery, New York, NY, USA, 2875–2886. https://doi.org/10.1145/3477495.3531722

**中文**

ICTIR ’25，2025 年 7 月 18 日，意大利帕多瓦 Alireza Salemi 和 Hamed Zamani 检索（西班牙马德里）（SIGIR ’22）。计算机协会，美国纽约州纽约市，2875–2886。 https://doi.org/10.1145/3477495.3531722
