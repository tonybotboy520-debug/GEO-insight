# Unified Ranking for Multiple Retrieval-Augmented Large Language Models

- ID: 81
- 类型: pdf
- 分类: 04_academic_papers
- 主题: search engine serving multiple RAG systems
- 原文链接: https://arxiv.org/pdf/2405.00175
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

Towards a Search Engine for Machines: Unified Ranking for Multiple Retrieval-Augmented Large Language Models Alireza Salemi University of Massachusetts Amherst Amherst, MA, United States asalemi@cs.umass.edu Hamed Zamani University of Massachusetts Amherst Amherst, MA, United States zamani@cs.umass.edu ABSTRACT This paper introduces uRAG–a framework with a unified retrieval engine that serves multiple downstream retrieval-augmented generation (RAG) systems. Each RAG system consumes the retrieval results for a unique purpose, such as open-domain question answering, fact verification, entity linking, and relation extraction.

**中文**

走向机器搜索引擎：多种检索增强大型语言模型的统一排名 Alireza Salemi 马萨诸塞州阿默斯特大学 美国马萨诸塞州阿默斯特 asalemi@cs.umass.edu Hamed Zamani 马萨诸塞州阿默斯特大学 阿默斯特美国马萨诸塞州 zamani@cs.umass.edu 摘要 本文介绍了 uRAG——一个具有统一检索引擎的框架，为多个下游检索增强型语言提供服务发电（RAG）系统。每个 RAG 系统都会出于特定目的使用检索结果，例如开放域问答、事实验证、实体链接和关系提取。

### 段落 2 · Page 1

**EN**

We introduce a generic training guideline that standardizes the communication between the search engine and the downstream RAG systems that engage in optimizing the retrieval model. This lays the groundwork for us to build a large-scale experimentation ecosystem consisting of 18 RAG systems that engage in training and 18 unknown RAG systems that use the uRAG as the new users of the search engine. Using this experimentation ecosystem, we answer a number of fundamental research questions that improve our understanding of promises and challenges in developing search engines for machines.

**中文**

我们引入了一个通用培训指南，该指南标准化了搜索引擎和参与优化检索模型的下游 RAG 系统之间的通信。这为我们建立一个大规模的实验生态系统奠定了基础，该生态系统由 18 个从事训练的 RAG 系统和 18 个使用 uRAG 作为搜索引擎新用户的未知 RAG 系统组成。利用这个实验生态系统，我们回答了许多基础研究问题，提高了我们对开发机器搜索引擎的前景和挑战的理解。

### 段落 3 · Page 1

**EN**

CCS CONCEPTS •Computing methodologies → Natural language generation; Machine learning ; • Information systems → Information retrieval; Retrieval models and ranking; Question answering. KEYWORDS Retrieval-enhanced machine learning; retrieval augmentation; neural ranking model; large language model; text generation ACM Reference Format: Alireza Salemi and Hamed Zamani. 2024. Towards a Search Engine for Machines: Unified Ranking for Multiple Retrieval-Augmented Large Language Models.

**中文**

CCS概念•计算方法→自然语言生成；机器学习； • 信息系统→信息检索；检索模型和排序；问答。关键词 检索增强型机器学习；检索增强；神经排序模型；大语言模型；文本生成 ACM 参考格式：Alireza Salemi 和 Hamed Zamani。 2024.迈向机器搜索引擎：多种检索增强大型语言模型的统一排名。

### 段落 4 · Page 1

**EN**

In Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR ’24), July 14–18, 2024, Washington, DC, USA. ACM, New York, NY, USA, 11 pages. https://doi.org/10.1145/3626772.3657733 1 INTRODUCTION The vast majority of machine learning systems, including large generative models, are designed as self-contained systems, with both knowledge and reasoning encoded in model parameters.

**中文**

第 47 届国际 ACM SIGIR 信息检索研究与开发会议 (SIGIR ’24) 会议记录，2024 年 7 月 14 日至 18 日，美国华盛顿特区。 ACM，美国纽约州纽约市，11 页。 https://doi.org/10.1145/3626772.3657733 1 简介 绝大多数机器学习系统（包括大型生成模型）都被设计为独立系统，知识和推理都编码在模型参数中。

### 段落 5 · Page 1

**EN**

However, these models cannot work effectively for tasks that require knowledge grounding [1, 48], especially in case of non-stationary Permission to make digital or hard copies of part or all of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. Copyrights for third-party components of this work must be honored. For all other uses, contact the owner/author(s). SIGIR ’24, July 14–18, 2024, Washington, DC, USA © 2024 Copyright held by the owner/author(s).

**中文**

然而，这些模型不能有效地用于需要知识基础的任务 [1, 48]，特别是在非固定的情况下。 允许免费制作部分或全部本作品的数字或硬拷贝以供个人或课堂使用，前提是制作或分发副本不是为了盈利或商业利益，并且副本在第一页上带有此通知和完整引用。必须尊重本作品第三方组件的版权。对于所有其他用途，请联系所有者/作者。 SIGIR ’24，2024 年 7 月 14 日至 18 日，美国华盛顿特区 © 2024 版权归所有者/作者所有。

### 段落 6 · Page 1

**EN**

ACM ISBN 979-8-4007-0431-4/24/07. https://doi.org/10.1145/3626772.3657733 Figure 1: A high-level overview of the uRAG ecosystem. The ecosystem consists of a shared search engine that serves multiple RAG models, each performing its own task. data where new information is actively being produced [49, 57]. As suggested by Zamani et al. [57], this issue can be addressed when machine learning systems are being enhanced with the capability of retrieving stored content .

**中文**

ACM ISBN 979-8-4007-0431-4/24/07。 https://doi.org/10.1145/3626772.3657733 图 1：uRAG 生态系统的高级概述。该生态系统由一个共享搜索引擎组成，该搜索引擎为多个 RAG 模型提供服务，每个模型执行自己的任务。正在积极产生新信息的数据[49, 57]。正如 Zamani 等人所建议的。 [57]，当机器学习系统通过检索存储内容的能力得到增强时，这个问题就可以得到解决。

### 段落 7 · Page 1

**EN**

For example, in retrieval-augmented generation (RAG), as a special case of retrieval-enhanced machine learning (REML) [57], systems consume the responses provided by a retrieval model for the purpose of text generation [25, 26]. RAG models demonstrate substantial promise across various applications, including open-domain question answering [6, 20, 25, 44, 60], fact verification [46], dialogue systems [8, 45, 53], machine translation [4], and personalized generation [37, 38].

**中文**

例如，在检索增强生成（RAG）中，作为检索增强机器学习（REML）的特例[57]，系统使用检索模型提供的响应来生成文本[25, 26]。 RAG 模型在各种应用中展现出了巨大的前景，包括开放域问答 [6,20,25,44,60]、事实验证 [46]、对话系统 [8,45,53]、机器翻译 [4] 和个性化生成 [37, 38]。

### 段落 8 · Page 1

**EN**

In the RAG literature, the retrieval component is often implemented using either of the following two approaches: (1) Employing an off-the-shelf retrieval model that does not require training for the downstream RAG system: in this category, RAG systems either use APIs from commercial web search engines [29], term matching retrieval models [11], such as TF-IDF and BM25, or neural ranking models trained on relevance annotations provided as an external resource [25]; (2) Training a retrieval model given the feedback from the downstream RAG system through knowledge distillation [15] or endto-end optimization [35].

**中文**

在 RAG 文献中，检索组件通常使用以下两种方法之一来实现：（1）采用现成的检索模型，不需要对下游 RAG 系统进行训练：在这一类别中，RAG 系统要么使用来自商业网络搜索引擎的 API [29]，要么使用术语匹配检索模型 [11]，例如 TF-IDF 和 BM25，或者使用作为外部资源提供的相关注释进行训练的神经排序模型 [25]； （2）通过知识蒸馏[15]或端到端优化[35]，根据下游RAG系统的反馈来训练检索模型。

### 段落 9 · Page 1

**EN**

As expected, the latter category offers the current state-of-theart performance for various tasks [17, 52]. From an IR perspective, in this category, the downstream RAG model is the only “user” of the search engine. This paper takes a step further by relying on an important lesson learned by the IR community since the creation of web search: achieving an effective retrieval model can be achieved through aggregating large-scale implicit feedback (e.g., clicks) obtained across users [42].

**中文**

正如预期的那样，后一类为各种任务提供了当前最先进的性能 [17, 52]。从IR的角度来看，在这个类别中，下游的RAG模型是搜索引擎的唯一“用户”。本文进一步借鉴了 IR 社区自网络搜索创建以来学到的重要经验：通过聚合跨用户获得的大规模隐式反馈（例如点击）可以实现有效的检索模型[42]。

### 段落 10 · Page 1

**EN**

Following this lesson, we aim to develop uRAG, a framework for training a single unified search engine for multiple RAG systems conducting various downstream tasks (see Figure 1). We define a training guideline, in which the search engine and its users—multiple downstream RAG systems—engage in an optimization process, in which RAG systems submit queries and the arXiv:2405.00175v1 [cs.CL] 30 Apr 2024

**中文**

继本课程之后，我们的目标是开发 uRAG，这是一个框架，用于为执行各种下游任务的多个 RAG 系统训练单个统一搜索引擎（见图 1）。我们定义了一个培训指南，其中搜索引擎及其用户（多个下游 RAG 系统）参与优化过程，其中 RAG 系统提交查询和 arXiv:2405.00175v1 [cs.CL] 2024 年 4 月 30 日

### Page 2

### 段落 11 · Page 2

**EN**

SIGIR ’24, July 14–18, 2024, Washington, DC, USA Alireza Salemi and Hamed Zamani search engine solicits feedback for a number of returned documents in their response. Each downstream RAG model identifies a utility function (any arbitrary evaluation metric; differentiable or not) and uses it for providing scalar feedback to the search engine. Using such a generic optimization guideline by uRAG, we implement a large-scale experimentation ecosystem that enables addressing important research questions in this area.

**中文**

SIGIR ’24，2024 年 7 月 14 日至 18 日，美国华盛顿特区 Alireza Salemi 和 Hamed Zamani 搜索引擎在回复中征求了一些返回文件的反馈。每个下游 RAG 模型都会识别一个效用函数（任何任意评估指标；可微分或不可微分），并使用它向搜索引擎提供标量反馈。使用 uRAG 的此类通用优化指南，我们实现了一个大规模实验生态系统，能够解决该领域的重要研究问题。

### 段落 12 · Page 2

**EN**

In more detail, we implement a set of 18 RAG systems that use different large language model (LLM) architectures, conduct different tasks, consume different number of retrieved documents, and/or trained on different datasets. We consider three diverse tasks of open-domain question answering, fact verification, and slot-filling for relation extraction. Six datasets related to these tasks from the knowledge-intensive language tasks (KILT) benchmark [ 31] are used for training and evaluation.

**中文**

更详细地说，我们实现了一组 18 个 RAG 系统，这些系统使用不同的大语言模型 (LLM) 架构、执行不同的任务、消耗不同数量的检索文档和/或在不同的数据集上进行训练。我们考虑三个不同的任务：开放域问答、事实验证和关系提取的槽填充。来自知识密集型语言任务（KILT）基准[31]的与这些任务相关的六个数据集用于训练和评估。

### 段落 13 · Page 2

**EN**

In addition to these 18 RAG models that engage with our unified search engine for optimization, we consider another set of 18 RAG models with distinct properties as thenew users of uRAG that do not engage in optimization and are partially or entirely unknown to the search engine. These models may use different LLM architectures, introduce new tasks, and/or use a new dataset for a known task. Using such a rich ecosystem, we aim at answering the following fundamental research questions that we believe are essential to understand the potential of developing search engines for machines.

**中文**

除了与我们的统一搜索引擎进行优化的这 18 个 RAG 模型之外，我们还考虑了另一组具有不同属性的 18 个 RAG 模型，作为 uRAG 的新用户，它们不参与优化，并且搜索引擎部分或完全未知。这些模型可能使用不同的 LLM 架构、引入新任务和/或对已知任务使用新数据集。利用如此丰富的生态系统，我们的目标是回答以下基础研究问题，我们认为这些问题对于了解开发机器搜索引擎的潜力至关重要。

### 段落 14 · Page 2

**EN**

Note that given the scope of these research questions and space limitation, we limit this study to reranking optimization, in which the search engine retrieves documents using BM25 and optimizes a personalized cross-encoder reranker based on the feedback received from the downstream RAG models. RQ1: How does unified reranking perform compared to training individual rerankers for each RAG model? Our experiments demonstrated that unified reranking performs either on par or significantly better than the same reranking model being trained for each downstream RAG model individually.

**中文**

请注意，考虑到这些研究问题的范围和空间限制，我们将本研究限制为重排序优化，其中搜索引擎使用 BM25 检索文档，并根据从下游 RAG 模型收到的反馈来优化个性化交叉编码器重排序器。 RQ1：与为每个 RAG 模型训练单独的重排序器相比，统一重排序的表现如何？我们的实验表明，统一重排序的性能与单独为每个下游 RAG 模型训练的相同重排序模型相当或明显更好。

### 段落 15 · Page 2

**EN**

In more detail, improvements are statistically significant for 61% of downstream models and there is no statistically significant performance degradation across the 18 RAG models that engage in the training process. This critical finding suggests that developing a unified search engine for machines is a promising research direction for the IR community to pursue further. RQ2: How does unified reranking perform compared to training rerankers using the feedback obtained from all RAG systems that use the same dataset?

**中文**

更详细地说，61% 的下游模型的改进具有统计显着性，并且参与训练过程的 18 个 RAG 模型没有统计显着的性能下降。这一重要发现表明，为机器开发统一的搜索引擎是 IR 社区进一步追求的一个有前途的研究方向。 RQ2：与使用从使用相同数据集的所有 RAG 系统获得的反馈来训练重排序器相比，统一重排序的表现如何？

### 段落 16 · Page 2

**EN**

This research question helps us understand if unification across datasets and tasks can lead to downstream performance improvement. Our experiments suggest that again training a unified reranker performs on par or significantly better than the ones that are trained based on the feedback provided by all RAG models that use the same dataset. In more detail, 39% of downstream RAG models in our experiments observe statistically significant improvement, while the majority observe no significant differences. These results are particularly important as they show knowledge transfer can occur across datasets.

**中文**

这个研究问题帮助我们了解数据集和任务之间的统一是否可以带来下游性能的提高。我们的实验表明，再次训练统一重排序器的性能与基于使用相同数据集的所有 RAG 模型提供的反馈进行训练的重排序器的性能相当或明显更好。更详细地说，我们实验中 39% 的下游 RAG 模型观察到统计上显着的改善，而大多数观察到没有显着差异。这些结果特别重要，因为它们表明知识转移可以跨数据集发生。

### 段落 17 · Page 2

**EN**

RQ3: How does “personalizing” search results for different RAG systems impact the performance? We hypothesize that different RAG systems behave differently, thus “personalizing” search results for each RAG model can be beneficial. To achieve this, we feed a task and model identifier for each RAG model to our crossencoder reranker, in addition to the query and document content. We observe that 50% of downstream RAG models observe improvements by including task and model identifiers in relevance scoring. However, in the vast majority of cases, these improvements are not statistically significant.

**中文**

RQ3：不同 RAG 系统的“个性化”搜索结果如何影响性能？我们假设不同的 RAG 系统表现不同，因此为每个 RAG 模型“个性化”搜索结果可能是有益的。为了实现这一目标，除了查询和文档内容之外，我们还向交叉编码器重新排序器提供每个 RAG 模型的任务和模型标识符。我们观察到，50% 的下游 RAG 模型通过在相关性评分中包含任务和模型标识符而获得改进。然而，在绝大多数情况下，这些改进在统计上并不显着。

### 段落 18 · Page 2

**EN**

Therefore, we do not find personalization in our experimentation ecosystem substantially useful. We must acknowledge that personalization often demonstrates its significance as the number of users increases and here we only have 18 users (i.e., the downstream RAG systems that engage in training). Therefore, this leaves several open questions for future work on exploring personalization in the context of uRAG. RQ4: How does unified reranking perform for new (unknown) RAG systems that use an observed (known) dataset? Ideally, search engines should perform effectively and robustly for new users.

**中文**

因此，我们发现我们的实验生态系统中的个性化并没有多大用处。我们必须承认，个性化往往会随着用户数量的增加而显示出其重要性，而这里我们只有 18 个用户（即参与培训的下游 RAG 系统）。因此，这为未来在 uRAG 背景下探索个性化的工作留下了几个悬而未决的问题。 RQ4：对于使用观察到的（已知）数据集的新（未知）RAG 系统，统一重排如何执行？理想情况下，搜索引擎应该对新用户有效且稳健地运行。

### 段落 19 · Page 2

**EN**

This would demonstrate the generalizability of the retrieval model to unknown agents. To address this question, we introduce three retrieval-augmented generation models based on PEGASUS [58], Mistral [18], and Llama2 [47] to our experiments. These models did not engage in the optimization pipeline of uRAG, thus are unknown to our unified reranker. We demonstrate that unified reranking significantly outperforms BM25 for all these new (unknown) RAG systems and performs comparably with a reranker that are trained on all other RAG systems that use the same dataset.

**中文**

这将证明检索模型对未知代理的通用性。为了解决这个问题，我们在实验中引入了三种基于 PEGASUS [58]、Mistral [18] 和 Llama2 [47] 的检索增强生成模型。这些模型没有参与 uRAG 的优化流程，因此我们的统一重排序器不知道这些模型。我们证明，对于所有这些新的（未知）RAG 系统，统一重排序显着优于 BM25，并且与在使用相同数据集的所有其他 RAG 系统上训练的重排序器的性能相当。

### 段落 20 · Page 2

**EN**

RQ5: How does unified reranking perform for a known RAG system on a new (unknown) dataset that is similar to the ones used during training? To address this research question, we use the open-domain variant of the SQuAD dataset [ 33] as a question answering data with short answers that is relatively similar to some of the datasets used during training. We observe that unified reranking leads to significant improvements compared to BM25 and since the dataset is new, other reranking alternatives are not applicable to this scenario. RQ6: How does unified reranking perform for a known RAG system on entirely new tasks?

**中文**

RQ5：对于已知 RAG 系统，在与训练期间使用的数据集类似的新（未知）数据集上，统一重排序如何执行？为了解决这个研究问题，我们使用 SQuAD 数据集 [33] 的开放域变体作为问答数据，其答案与训练期间使用的一些数据集相对相似。我们观察到，与 BM25 相比，统一重排带来了显着改进，并且由于数据集是新的，其他重排替代方案不适用于此场景。 RQ6：对于已知的 RAG 系统来说，统一重排序在全新任务上的表现如何？

### 段落 21 · Page 2

**EN**

We take a step further and consider evaluation sets that are not closely related to our training datasets. For this purpose, we consider ELI5, an open-domain question answering dataset with long-form (passage-level) answers, as well as AY2 an entity linking dataset. Note that all datasets used during optimization target short text generation tasks. We observe that uRAG outperforms BM25 in half of the cases and differences are not statistically significant. This suggests that reranking documents using the current implementation of uRAG should only be employed when target downstream tasks are closely related to the ones used during training.

**中文**

我们更进一步，考虑与我们的训练数据集不密切相关的评估集。为此，我们考虑 ELI5，一个具有长格式（段落级）答案的开放域问答数据集，以及 AY2 一个实体链接数据集。请注意，优化过程中使用的所有数据集都针对短文本生成任务。我们观察到 uRAG 在一半的情况下优于 BM25，并且差异不具有统计显着性。这表明，仅当目标下游任务与训练期间使用的任务密切相关时，才应使用当前 uRAG 实现对文档进行重新排序。

### 段落 22 · Page 2

**EN**

RQ7: How does unified reranking perform for a new (unknown) RAG system on a new (unknown) dataset that is similar to the ones used during training? We evaluate retrievalaugmented models based on PEGASUS, Mistral, and Llama2 on SQuAD for answering this question. None of these models were employed during training and as mentioned earlier, SQuAD is similar to some of the datasets used for traininguRAG. We observe that reranking results using uRAG can lead to statistically significant improvements in this scenario. This emphasizes that the target task

**中文**

RQ7：对于新（未知）RAG 系统，在与训练期间使用的数据集类似的新（未知）数据集上，统一重排序如何执行？我们在 SQuAD 上评估基于 PEGASUS、Mistral 和 Llama2 的检索增强模型来回答这个问题。训练期间没有使用这些模型，并且如前所述，SQuAD 与用于训练 uRAG 的一些数据集类似。我们观察到，在这种情况下，使用 uRAG 对结果进行重排可以带来统计上的显着改进。这强调了目标任务

### Page 3

### 段落 23 · Page 3

**EN**

Towards a Search Engine for Machines: Unified Ranking for Multiple Retrieval-Augmented Large Language Models SIGIR ’24, July 14–18, 2024, Washington, DC, USA and data have more impact on the effectiveness ofuRAG, compared to the downstream RAG system that consumes the retrieval results. RQ8: How does unified reranking perform for a new RAG system on an entirely new (unknown) task? This is the most extreme case, where both the model architecture and the task are unknown to the search engine. We test PEGASUS, Mistral, and Llama2 on ELI5 and AY2 and observe that uRAG struggles with improving BM25 in this scenario.

**中文**

迈向机器搜索引擎：多重检索增强大型语言模型的统一排名 SIGIR’24，2024 年 7 月 14-18 日，美国华盛顿特区，与使用检索结果的下游 RAG 系统相比，数据对 uRAG 的有效性有更大的影响。 RQ8：对于全新的（未知）任务，新的 RAG 系统的统一重排序如何执行？这是最极端的情况，其中模型架构和任务对于搜索引擎来说都是未知的。我们在 ELI5 和 AY2 上测试 PEGASUS、Mistral 和 Llama2，并观察到 ​​uRAG 在这种情况下难以改善 BM25。

### 段落 24 · Page 3

**EN**

We mark the development of robust and generalizable search engines for such scenarios as an important research direction for further exploration. RQ9: How does uRAG perform when different amount of training data is provided? We plot the learning curve for all 18 RAG models that are involved in our training pipeline and observe that their performance often improves as more training data is provided. This finding suggests that as we introduce more data and more RAG systems to theuRAG framework, we expect even further performance improvement.

**中文**

我们将针对此类场景开发鲁棒且通用的搜索引擎作为进一步探索的重要研究方向。 RQ9：在提供不同数量的训练数据时，uRAG 的表现如何？我们绘制了训练流程中涉及的所有 18 个 RAG 模型的学习曲线，并观察到随着提供更多训练数据，它们的性能通常会提高。这一发现表明，随着我们向 uRAG 框架引入更多数据和更多 RAG 系统，我们预计性能会进一步提高。

### 段落 25 · Page 3

**EN**

We believe that these findings deepen our knowledge and understanding for developing effective search engines for downstream retrieval-augmented systems and smooth the path towards important developments in this area. We open-source theuRAG codebase and release our trained model parameters.1 Given the high cost of training and building such an ecosystem, we expect that this public release will substantially speed up research progress in this area. 2 RELATED WORK Knowledge-Intensive Language Tasks .

**中文**

我们相信，这些发现加深了我们对为下游检索增强系统开发有效搜索引擎的知识和理解，并为该领域的重要发展铺平道路。我们开源了 uRAG 代码库，并发布了经过训练的模型参数。1 鉴于训练和构建这样一个生态系统的成本很高，我们预计此次公开发布将大大加快该领域的研究进展。 2 相关工作知识密集型语言任务。

### 段落 26 · Page 3

**EN**

Unlike conventional NLP tasks like natural language understanding [50, 51] and question answering [28], where the task’s input alone is sufficient for task completion, knowledge-intensive NLP tasks demand access to external knowledge sources to retrieve essential information for task execution. Petroni et al. [31] established KILT as a benchmark for knowledge-intensive NLP tasks. Encompassing a wide range of tasks such as open-domain question answering, fact checking, slot filling, and entity linking, KILT provides a comprehensive evaluation framework. The experiments conducted in this paper leverage datasets sourced from the KILT benchmark.

**中文**

与自然语言理解 [50, 51] 和问题回答 [28] 等传统 NLP 任务不同，仅任务输入就足以完成任务，知识密集型 NLP 任务需要访问外部知识源以检索任务执行的基本信息。彼得罗尼等人。 [31]将KILT确立为知识密集型NLP任务的基准。 KILT 涵盖开放域问答、事实检查、槽填充和实体链接等广泛的任务，提供了一个全面的评估框架。本文进行的实验利用来自 KILT 基准的数据集。

### 段落 27 · Page 3

**EN**

Retrieval-Augmented Generation (RAG). RAG [25] is a paradigm that integrates information retrieval (IR) and natural language generation (NLG). This approach aims to enhance the quality and relevance of generated content by leveraging external knowledge sources during the generation process [ 3, 44]. Unlike traditional large language models that rely solely on knowledge learned during their pre-training, RAG systems dynamically fetch information from a knowledge source using a retriever, allowing them to generate contextually rich and factually accurate outputs [57]. RAG demonstrates versatility with numerous use cases and applications.

**中文**

检索增强生成（RAG）。 RAG [25] 是集成信息检索（IR）和自然语言生成（NLG）的范例。这种方法旨在通过在生成过程中利用外部知识源来提高生成内容的质量和相关性 [3, 44]。与仅依赖于预训练期间学习的知识的传统大型语言模型不同，RAG 系统使用检索器从知识源动态获取信息，从而使它们能够生成上下文丰富且事实上准确的输出 [57]。 RAG 展示了众多用例和应用程序的多功能性。

### 段落 28 · Page 3

**EN**

It finds application in knowledge-grounding within textual [16, 25, 31] or multi-modal [5, 12, 36, 39] problem domains. Additionally, RAG contributes to personalization efforts [ 37, 38] and addresses challenges such as reducing hallucination [2, 43]. 1https://github.com/alirezasalemi7/uRAG Figure 2: An overview of interactions between RAG models (also known as predictive models) and the unified search engine. A pivotal element in RAG systems is the retriever, tasked with obtaining the required information for the large language model to execute its task [25].

**中文**

它可应用于文本 [16,25,31] 或多模态 [5,12,36,39] 问题领域的知识基础。此外，RAG 有助于个性化工作 [37, 38] 并解决减少幻觉等挑战 [2, 43]。 1https://github.com/alirezasalemi7/uRAG 图 2：RAG 模型（也称为预测模型）与统一搜索引擎之间的交互概述。 RAG 系统中的关键元素是检索器，其任务是获取大型语言模型执行其任务所需的信息 [25]。

### 段落 29 · Page 3

**EN**

Typically, a either sparse (e.g., BM25 [34]) or dense retrieval models (e.g., DPR [20], Contriever [14], ColBERTv2 [41], etc.) is employed to efficiently retrieve information from knowledge sources. Subsequently, the large language model employs the retrieved information to accomplish its task. Notably, In-Prompt Augmentation (IPA) and Fusion-in-Decoder (FiD) [16] represent prominent approaches in this context. In IPA, the retrieved information is concatenated with the prompt, enabling the large language model to fulfill the task.

**中文**

通常，采用稀疏（例如 BM25 [34]）或密集检索模型（例如 DPR [20]、Contriever [14]、ColBERTv2 [41] 等）来有效地从知识源检索信息。随后，大语言模型利用检索到的信息来完成其任务。值得注意的是，即时增强（IPA）和解码器融合（FiD）[16]代表了这方面的突出方法。在 IPA 中，检索到的信息与提示相连接，使大语言模型能够完成任务。

### 段落 30 · Page 3

**EN**

On the other hand, FiD involves encoding each retrieved document and the prompt separately in the encoder of an encoder-decoder LLM, followed by concatenation in the decoder to generate a unified answer drawing from the information in all documents. For a more in-depth exploration of this approach, refer to the work by Izacard and Grave [16]. Optimizing Retriever in RAG pipelines. Joint training of a retriever model and a large language model has been explored in various studies.

**中文**

另一方面，FiD 涉及在编码器-解码器 LLM 的编码器中分别对每个检索到的文档和提示进行编码，然后在解码器中进行串联，以根据所有文档中的信息生成统一的答案。要更深入地探索这种方法，请参阅 Izacard 和 Grave 的工作 [16]。优化 RAG 管道中的 Retriever。各种研究都探索了检索器模型和大型语言模型的联合训练。

### 段落 31 · Page 3

**EN**

Yang and Seo [54] focuses on optimizing the retriever by leveraging the downstream performance of the LLM, using each individually retrieved document to guide the retriever towards retrieving documents with higher scores. Conversely, Izacard and Grave [15] adopts a different strategy by utilizing cross-attention weights of the LLM instead of the downstream performance to distill knowledge from the LLM to the retriever. Additionally, Sachan et al.

**中文**

Yang 和 Seo [54] 专注于通过利用 LLM 的下游性能来优化检索器，使用每个单独检索的文档来指导检索器检索具有更高分数的文档。相反，Izacard 和 Grave [15] 采用了不同的策略，利用 LLM 的交叉注意力权重而不是下游性能，将知识从 LLM 提取到检索器。此外，Sachan 等人。

### 段落 32 · Page 3

**EN**

[35] introduces EMDR2, an end-to-end approach that employs an expectation-maximization algorithm to optimize both the retriever and the LLM, maximizing the probability of generating the ground truth answer conditioned on the documents retrieved by the retriever. Moreover, Izacard et al. [17] presents a similar approach to Izacard and Grave [15] and Sachan et al. [35], utilizing the document’s posterior distribution according to the LLM, conditioned on a single document, to perform distillation. Wang et al. [52] uses a multi-armed bandit algorithm to for the joint training of a retriever and reader.

**中文**

[35] 引入了 EMDR2，这是一种端到端方法，它采用期望最大化算法来优化检索器和 LLM，最大化生成以检索器检索的文档为条件的地面真实答案的概率。此外，伊扎卡德等人。 [17] 提出了与 Izacard 和 Grave [15] 以及 Sachan 等人类似的方法。 [35]，利用根据 LLM 的文档后验分布，以单个文档为条件，进行蒸馏。王等人。 [52]使用多臂老虎机算法来联合训练检索器和阅读器。

### 段落 33 · Page 3

**EN**

Most recently, Zamani and Bendersky [56] proposes end-to-end RAG optimization through stochastic sampling without replacement, approximated by gumbel-top-k sampling. Our work diverges from prior research in two key aspects. Firstly, we operate under the assumption that LLM parameters in downstream models are not accessible to the retrieval model. This stems

**中文**

最近，Zamani 和 Bendersky [56] 提出通过无替换的随机采样进行端到端 RAG 优化，近似为gumbel-top-k 采样。我们的工作在两个关键方面与之前的研究有所不同。首先，我们假设下游模型中的 LLM 参数无法被检索模型访问。这源于

### Page 4

### 段落 34 · Page 4

**EN**

SIGIR ’24, July 14–18, 2024, Washington, DC, USA Alireza Salemi and Hamed Zamani from our conceptualization of the LLM as a user of the retrieval model, akin to how humans interact with search engines. In this analogy, search engines can only offer results to users and must rely on user feedback (e.g., clicks) to refine themselves, without altering how users engage with the results. Secondly, our focus extends beyond previous studies by considering scenarios where multiple LLMs use a shared search engine. Our objective is to optimize the search engine to enhance the collective performance of these diverse LLMs.

**中文**

SIGIR ’24，2024 年 7 月 14 日至 18 日，美国华盛顿特区 Alireza Salemi 和 Hamed Zamani 将法学硕士概念化为检索模型的用户，类似于人类与搜索引擎的交互方式。在这个类比中，搜索引擎只能向用户提供结果，并且必须依赖用户反馈（例如点击）来完善自身，而不会改变用户与结果互动的方式。其次，我们的重点超出了之前的研究范围，考虑了多个法学硕士使用共享搜索引擎的场景。我们的目标是优化搜索引擎，以提高这些不同的法学硕士的集体表现。

### 段落 35 · Page 4

**EN**

3 THE URAG ECOSYSTEM Search engines are often designed for human users who submit unstructured queries, such as keyword queries and natural language questions. However, a paradigm shift is underway with the emergence of machine learning models [57], especially large language models, possessing strong linguistic capabilities, memorization, and sometimes even reasoning to some extent [59]. In the current paradigm known as REML [57], machines, e.g., LLMs, engage in interactions with a retrieval model to acquire essential knowledge for executing their designated tasks.

**中文**

3 URAG 生态系统 搜索引擎通常是为提交非结构化查询（例如关键字查询和自然语言问题）的人类用户而设计的。然而，随着机器学习模型[57]的出现，范式转变正在发生，特别是大型语言模型，拥有强大的语言能力、记忆能力，有时甚至在某种程度上具有推理能力[59]。在当前称为 REML [57] 的范式中，机器（例如法学硕士）与检索模型进行交互，以获取执行指定任务所需的基本知识。

### 段落 36 · Page 4

**EN**

Most REML systems nowadays are in the form of retrieval-augmented text generation. Notably, with the introduction of real-world RAG systems, such as Bing Chat2 and Google Bard,3 humans now assume the role of users for these applications [40, 57], marking a transition from their previous role as users of web search engines. In this case, LLMs constitute the primary users of search engines. Exploring the design of a search engine capable of providing information to different LLMs based on their needs, each tailored for specific tasks, represents a valuable and promising research direction that this paper focuses on. uRAG Formulation.

**中文**

现在大多数 REML 系统都是检索增强文本生成的形式。值得注意的是，随着现实世界 RAG 系统（例如 Bing Chat2 和 Google Bard）的引入，3 人类现在承担了这些应用程序的用户角色 [40, 57]，标志着他们从之前作为网络搜索引擎用户的角色的转变。在这种情况下，法学硕士构成了搜索引擎的主要用户。探索能够根据不同法学硕士的需求向他们提供信息的搜索引擎的设计，每个搜索引擎都针对特定任务量身定制，代表了本文重点关注的一个有价值且有前途的研究方向。 uRAG 配方。

### 段落 37 · Page 4

**EN**

Let 𝑅𝜃 denote a search engine parameterized by 𝜃 whose goal is to provide access to information from a corpus 𝐶 to a set of 𝑛 RAG models. The set of RAG models, that are essentially the users of 𝑅𝜃 , is represented as M = {𝑀1, ..., 𝑀𝑛 }. For 𝑅𝜃 , each 𝑀𝑖 is a black-box model and the search engine does not have access to the architecture, configuration, or parameters of RAG models. Each RAG model 𝑀𝑖 is designed to perform a specific task 𝑇𝑖 that requires access to information from the corpus𝐶. These tasks are often called knowledge-intensive tasks.

**中文**

令 𝑅𝜃 表示由 𝜃 参数化的搜索引擎，其目标是提供对从语料库 𝐶 到一组 𝑛 RAG 模型的信息的访问。 RAG 模型集本质上是 𝑅𝜃 的用户，表示为 M = {𝑀1, ..., 𝑀𝑛 }。对于 𝑅𝜃，每个𝑀𝑖 都是一个黑盒模型，搜索引擎无法访问 RAG 模型的架构、配置或参数。每个 RAG 模型𝑀𝑖 旨在执行需要访问语料库𝐶 中的信息的特定任务 𝑇𝑖。这些任务通常称为知识密集型任务。

### 段落 38 · Page 4

**EN**

Each RAG model 𝑀𝑖 operates by taking the input 𝑥 and utilizing a communication link to interact with the search engine𝑅𝜃 . Through this interaction, the model produces an output denoted as ˆ𝑦𝑀𝑖 , representing the result of the prediction process for the given input 𝑥. Formally, ˆ𝑦𝑀𝑖 = 𝑀𝑖 (𝑥; 𝑅𝜃 ). Inspired by the REML framework presented in [57], Figure 2 illustrates the interactions and components in uRAG. The Optimization Guideline and Process in uRAG. For each query submitted by the RAG model 𝑀𝑖, our goal is to develop a search engine that delivers a search result that benefits the downstream task conducted by 𝑀𝑖.

**中文**

每个 RAG 模型𝑀𝑖 都通过获取输入𝑥 并利用通信链接与搜索引擎𝑅𝜃 进行交互来运行。通过这种交互，模型产生一个表示为 ˆ𝑦𝑀𝑖 的输出，表示给定输入 𝑥 的预测过程的结果。形式上， ˆ𝑦𝑀𝑖 = 𝑀𝑖 (𝑥; 𝑅𝜃 )。受 [57] 中提出的 REML 框架的启发，图 2 说明了 uRAG 中的交互和组件。 uRAG 中的优化指南和流程。对于 RAG 模型𝑀𝑖 提交的每个查询，我们的目标是开发一个搜索引擎，提供有利于𝑀𝑖 执行的下游任务的搜索结果。

### 段落 39 · Page 4

**EN**

Thus, we assume that 𝑀𝑖s engage in an optimization process with 𝑅𝜃 with a pre-defined training guideline: (1) Each RAG model 𝑀𝑖 must have a training set Di = {(𝑥1, 𝑦1), · · ·, (𝑥 |Di |, 𝑦|Di | )}, where (𝑥 𝑗 , 𝑦𝑗 ) denotes the 𝑗th input and 2https://www.bing.com/chat 3https://bard.google.com/ Table 1: A list of datasets from KILT [ 31] used in our experiments. The validation data from KILT is used as test sets. The first six datasets are used during the search engine training process. The last three datasets, on the other hand, are only introduced during inference to quantify generalizability of uRAG.

**中文**

因此，我们假设 𝑀𝑖 与 𝑅𝜃 一起按照预定义的训练准则进行优化过程： (1) 每个 RAG 模型 𝑀𝑖 必须有一个训练集 Di = {(𝑥1, 𝑦1), · · ·, (𝑥 |Di |, 𝑦|Di | )}，其中 (𝑥 𝑗 , 𝑦𝑗 ）表示第 𝑗 个输入，2https://www.bing.com/chat 3https://bard.google.com/ 表 1：我们实验中使用的 KILT [31] 数据集列表。来自 KILT 的验证数据用作测试集。前六个数据集在搜索引擎训练过程中使用。另一方面，最后三个数据集仅在推理过程中引入，以量化 uRAG 的泛化能力。

### 段落 40 · Page 4

**EN**

∗ Given the large training set in the original T-REx dataset, we only sampled 5% of data for training our models. Dataset #train #test open-domain QA (short answer) Natural Questions 87,372 2,837 TriviaQA 61,844 5,359 HotPotQA 88,869 5,600 fact verification FEVER 104,966 10,444 slot-filling relation extraction zsRE 147,909 3,724 T-REx 114,208 ∗ 5,000 new data introduced during inference SQuAD 87,599 10,570 ELI5 272,634 1,507 AY2 18,395 4,784 expected output. There is no need to share the data with the search engine 𝑅𝜃 . (2) For each (𝑥, 𝑦) ∈ D𝑖, the RAG model 𝑀𝑖 must construct a query 𝑞 = QGen(𝑥) to be consumed by the search engine 𝑅𝜃 .

**中文**

考虑到原始 T-REx 数据集中的训练集很大，我们只采样了 5% 的数据来训练我们的模型。数据集 #train #test 开放域 QA（简答） 自然问题 87,372 2,837 TriviaQA 61,844 5,359 HotPotQA 88,869 5,600 事实验证 FEVER 104,966 10,444 槽填充关系提取 zsRE 147,909 3,724 T-REx 114,208 * 推理期间引入的 5,000 个新数据 SQuAD 87,599 10,570 ELI5 272,634 1,507 AY2 18,395 4,784 预期输出。无需与搜索引擎分享数据𝑅𝜃。 (2) 对于每个 (𝑥, 𝑦) ∈ D𝑖，RAG 模型𝑀𝑖 必须构造一个查询 𝑞 = QGen(𝑥) 以供搜索引擎 𝑅𝜃 使用。

### 段落 41 · Page 4

**EN**

The search engine returns a ranked list of documents in response. Let Q𝑖 = {QGen(𝑥) : ∀(𝑥, 𝑦) ∈ D𝑖 } be a set of all queries constructed from data points in D𝑖. (3) Each RAG model𝑀𝑖 must identify a utility functionUtility𝑖 that quantifies the end-to-end performance of the model in relation to its designated task𝑇𝑖 and serves as a metric to measure the effectiveness of 𝑀𝑖 in performing its downstream task. Utility𝑖 can be any arbitrary function, differentiable or not, whose outputs will be provided as feedback to𝑅𝜃 for optimization. For simplicity, this paper assumes that Utility𝑖 values are in the [0, 1] range.

**中文**

搜索引擎返回响应的文档的排名列表。设 Q𝑖 = {QGen(𝑥) : ∀(𝑥, 𝑦) ∈ D𝑖 } 是从 D𝑖 中的数据点构造的所有查询的集合。 (3) 每个 RAG 模型𝑀𝑖 必须确定一个效用函数Utility𝑖，该函数可以量化模型与其指定任务𝑇𝑖 相关的端到端性能，并作为衡量𝑀𝑖 执行下游任务有效性的指标。效用𝑖可以是任何任意函数，无论是否可微，其输出将作为反馈提供给𝑅𝜃以进行优化。为简单起见，本文假设 Utility𝑖 值在 [0, 1] 范围内。

### 段落 42 · Page 4

**EN**

According to the risk minimization framework, the primary goal of the search engine 𝑅𝜃 is to minimize the loss function defined based on the received utility values from downstream models: 𝜃 ∗ = arg min 𝜃 1 𝑛 𝑛∑︁ 𝑖=1 1 |Q𝑖 | ∑︁ 𝑞 ∈Q𝑖 𝐿(𝑅𝜃 (𝑞; 𝐶), 𝑈𝑖𝑞 ) (1) where 𝑈𝑖𝑞 is computed by 𝑀𝑖 as follows: 𝑈𝑖𝑞 B Utility𝑖 (𝑦, 𝑀𝑖 (𝑥; 𝑅𝜃 (QGen𝑖 (𝑥); 𝐶))) (2) It is important to note that various methods exist for aggregating utility across the users. For example, prioritizing utility enhancement for specific users may be more important than others. Alternatively, fairness or robustness could serve as criteria for aggregating the overall system utility.

**中文**

根据风险最小化框架，搜索引擎𝑅𝜃的主要目标是最小化根据从下游模型接收到的效用值定义的损失函数： 𝜃 ∗ = arg min 𝜃 1 𝑛 𝑛Σ︁ 𝑖=1 1 |Q𝑖 | Σ︁ 𝑞 ∈Q𝑖 𝐿(𝑅𝜃 (𝑞; 𝐶), 𝑈𝑖𝑞 ) (1) 其中 𝑈𝑖𝑞 由 𝑀𝑖 计算如下： 𝑈𝑖𝑞 B Utility𝑖 (𝑦, 𝑀𝑖 (𝑥; 𝑅𝜃 (QGen𝑖 (𝑥); 𝐶))) (2) 需要注意的是，存在多种用于聚合用户效用的方法。例如，优先考虑特定用户的效用增强可能比其他用户更重要。或者，公平性或鲁棒性可以作为聚合整个系统效用的标准。

### 段落 43 · Page 4

**EN**

However, in this particular problem, our emphasis is on expected utility across inputs and users.

**中文**

然而，在这个特定问题中，我们的重点是输入和用户之间的预期效用。

### Page 5

### 段落 44 · Page 5

**EN**

Towards a Search Engine for Machines: Unified Ranking for Multiple Retrieval-Augmented Large Language Models SIGIR ’24, July 14–18, 2024, Washington, DC, USA Table 2: A list of RAG models used in our experiments for training and evaluation. Task Data Utility Func.

**中文**

迈向机器搜索引擎：多重检索增强大型语言模型的统一排名 SIGIR ’24，2024 年 7 月 14-18 日，美国华盛顿特区 表 2：我们的训练和评估实验中使用的 RAG 模型列表。任务数据实用功能

### 段落 45 · Page 5

**EN**

LM 𝑀1 open-domain QA NQ Exact Match RA-T5 𝑀2 open-domain QA NQ Exact Match RA-BART 𝑀3 open-domain QA NQ Exact Match FiD 𝑀4 open-domain QA TriviaQA Exact Match RA-T5 𝑀5 open-domain QA TriviaQA Exact Match RA-BART 𝑀6 open-domain QA TriviaQA Exact Match FiD 𝑀7 open-domain QA HotPotQA Exact Match RA-T5 𝑀8 open-domain QA HotPotQA Exact Match RA-BART 𝑀9 open-domain QA HotPotQA Exact Match FiD 𝑀10 fact verification FEVER Accuracy RA-T5 𝑀11 fact verification FEVER Accuracy RA-BART 𝑀12 fact verification FEVER Accuracy FiD 𝑀13 slot filling zsRE Accuracy RA-T5 𝑀14 slot filling zsRE Accuracy RA-BART 𝑀15 slot filling zsRE Accuracy FiD 𝑀16 slot filling T-R

**中文**

LM 𝑀1 开放域 QA NQ 精确匹配 RA-T5 𝑀2 开放域 QA NQ 精确匹配 RA-BART 𝑀3 开放域 QA NQ 精确匹配 FiD 𝑀4 开放域 QA TriviaQA 精确匹配 RA-T5 𝑀5 开放域 QA TriviaQA 精确匹配 RA-BART 𝑀6 开放域 QA TriviaQA 精确匹配 FiD 𝑀7 开放域 QA HotPotQA 精确匹配 RA-T5 𝑀8 开放域 QA HotPotQA 精确匹配 RA-BART 𝑀9 开放域 QA HotPotQA 精确匹配 FiD 𝑀10 事实验证 FEVER 准确性 RA-T5 𝑀11 事实验证 FEVER 准确性 RA-BART 𝑀12 事实验证 FEVER 精度 FiD 𝑀13 槽填充 zsRE 精度 RA-T5 𝑀14 槽填充 zsRE 精度 RA-BART 𝑀15 槽填充 zsRE 精度 FiD 𝑀16 槽填充 T-R

### 段落 46 · Page 5

**EN**

Ex Accuracy RA-T5 𝑀17 slot filling T-REx Accuracy RA-BART 𝑀18 slot filling T-REx Accuracy FiD 4 SYSTEM IMPLEMENTATION AND SETUP 4.1 Training Data As we will discuss later, different tasks and datasets are used for training RAG models and providing feedback to 𝑅𝜃 .

**中文**

Ex 精度 RA-T5 𝑀17 槽填充 T-REx 精度 RA-BART 𝑀18 槽填充 T-REx 精度 FiD 4 系统实现和设置 4.1 训练数据 正如我们稍后将讨论的，不同的任务和数据集用于训练 RAG 模型并向 𝑅𝜃 提供反馈。

### 段落 47 · Page 5

**EN**

A list of all datasets is presented in Table 1. Three diverse open-domain question answering datasets, i.e., Natural Questions (NQ) [22], TriviaQA [19], and HotPotQA [55], are used in our experiments. The answers for all questions in these datasets are in the form of short text. Hot- PotQA focuses on questions that require multi-hop reasoning. One dataset is used for fact verification, called FEVER [46], and finally, two slot-filling datasets for relation extraction are used in our experiments; zsRE [23] and T-REx [9]. All datasets are obtained from the KILT benchmark [31].

**中文**

表 1 列出了所有数据集。我们的实验中使用了三个不同的开放域问答数据集，即 Natural Questions (NQ) [22]、TriviaQA [19] 和 HotPotQA [55]。这些数据集中所有问题的答案都是短文本的形式。 HotPotQA 专注于需要多跳推理的问题。一个数据集用于事实验证，称为 FEVER [46]，最后，我们的实验中使用两个用于关系提取的槽填充数据集； zsRE [23] 和 T-REx [9]。所有数据集均来自 KILT 基准测试 [31]。

### 段落 48 · Page 5

**EN**

Note that the last three datasets mentioned in Table 1 are not used for optimizing 𝑅𝜃 and they are primarily employed for evaluating the generalizability of approaches. Note that since the T-REx training set includes approximately 2.2 million samples, we randomly select 5% of them to train our models to speed up experiments. It is important to note that labels for test sets of these datasets are not publicly available. Therefore, as the public validation set was not used for training or hyperparameter tuning, we use the validation set directly to evaluate our models.

**中文**

请注意，表 1 中提到的最后三个数据集不用于优化 𝑅𝜃，它们主要用于评估方法的通用性。请注意，由于 T-REx 训练集包含大约 220 万个样本，因此我们随机选择其中 5% 来训练我们的模型以加快实验速度。值得注意的是，这些数据集的测试集标签不是公开的。因此，由于公共验证集不用于训练或超参数调整，因此我们直接使用验证集来评估我们的模型。

### 段落 49 · Page 5

**EN**

4.2 Downstream RAG Models for uRAG Optimization To have a comprehensive study, we consider a total of 18 diverse RAG models during training in our experiments. Different RAG models conduct different tasks, are trained using different resources, are using different underlying models, and/or are consuming different number of retrieved documents. Such diversity would enable us to evaluate the generalizability of different approaches. The downstream task conducted by models 𝑀1 to 𝑀9 is open-domain question answering. Models 𝑀10, 𝑀11, and 𝑀12 deliver fact verification functionality to their users.

**中文**

4.2 用于 uRAG 优化的下游 RAG 模型 为了进行全面的研究，我们在实验训练期间总共考虑了 18 个不同的 RAG 模型。不同的 RAG 模型执行不同的任务，使用不同的资源进行训练，使用不同的底层模型，和/或消耗不同数量的检索文档。这种多样性将使我们能够评估不同方法的普遍性。模型𝑀1至𝑀9执行的下游任务是开放域问答。模型 𝑀10、𝑀11 和 𝑀12 为其用户提供事实验证功能。

### 段落 50 · Page 5

**EN**

Finally, models 𝑀13 to 𝑀18 perform slot filling for relation extraction. All RAG models are listed in Table 2. Each of these models is trained on a different dataset or uses a different large language model. We consider three retrieval-augmented large language models: (1) Retrieval-augmented T5 (RA-T5) is a language model based on T5-small [ 32] with 60 million parameters that consumes 𝑘 documents per input via in-prompt augmentation based on the following input format: “ {input} context 1: {doc1} . . . context k: {dock} ”, where{input} is 𝑥 and {doci} denotes the content of the 𝑖th retrieved document.

**中文**

最后，模型𝑀13至𝑀18执行槽填充以进行关系提取。表 2 列出了所有 RAG 模型。每个模型都在不同的数据集上进行训练或使用不同的大型语言模型。我们考虑三种检索增强的大型语言模型：（1）检索增强的 T5（RA-T5）是一种基于 T5-small [32] 的语言模型，具有 6000 万个参数，通过基于以下输入格式的提示增强来消耗𝑘每个输入的文档：“ {input} context 1: {doc1} . . . context k: {dock} ”，其中 {input} 是𝑥 和 {doci} 表示第 𝑖 个检索到的文档的内容。

### 段落 51 · Page 5

**EN**

Our T5 model has an input length limitation of 4096 tokens. Given this limitation, we feed 𝑘 = 10 documents to this model. Each RA-T5 model is fine-tuned on the corresponding training set. For example, the RA-T5 model in 𝑀1 is trained on the Natural Questions dataset variant in KILT [31] (see data statistics in Table 1). (2) Retrieval-augmented BART (RA-BART) is BART-base [24] with 140 million parameters that uses the same augmentation approach for input format as RA-T5. BART goes under a different pre-training process than T5, thus, would exhibit a different behavior and performance.

**中文**

我们的 T5 模型的输入长度限制为 4096 个令牌。鉴于此限制，我们向该模型提供 𝑘 = 10 个文档。每个 RA-T5 模型都在相应的训练集上进行微调。例如，𝑀1 中的 RA-T5 模型是在 KILT [31] 中的自然问题数据集变体上进行训练的（参见表 1 中的数据统计）。 (2) 检索增强 BART (RA-BART) 是基于 BART 的 [24]，具有 1.4 亿个参数，使用与 RA-T5 相同的输入格式增强方法。 BART 的预训练过程与 T5 不同，因此会表现出不同的行为和性能。

### 段落 52 · Page 5

**EN**

Additionally, it has an input length limitation of 1024 tokens. Therefore, we use only 𝑘 = 4 for augmenting BART using the results returned by𝑅𝜃 . Each RA-BART model is fine-tuned on the corresponding training set. (3) Fusion-in-Decoder (FiD) [ 16] uses a different augmentation approach. Unlike RA-T5 and RA-BART that are based on inprompt augmentation, FiD first encodes the input and each retrieved document separately and uses the concatenation of all document encodings as cross-attention for the decoder. FiD can thus only be done using encoder-decoder language models, for which we used T5-small [32] in our experiments.

**中文**

此外，它的输入长度限制为 1024 个令牌。因此，我们仅使用 𝑘 = 4 来使用 𝑅𝜃 返回的结果来增强 BART。每个 RA-BART 模型都在相应的训练集上进行微调。 (3) 解码器融合 (FiD) [16] 使用不同的增强方法。与基于即时增强的 RA-T5 和 RA-BART 不同，FiD 首先对输入和每个检索到的文档进行单独编码，并使用所有文档编码的串联作为解码器的交叉注意力。因此，FiD 只能使用编码器-解码器语言模型来完成，我们在实验中使用了 T5-small [32]。

### 段落 53 · Page 5

**EN**

We use FiDsmall in our experiments. The number of augmented documents is set to 𝑘 = 10 for FiD. Similarly, each FiD model is fine-tuned on the corresponding training set. All retrieval-augmented models listed in Table 2 are fine-tuned separately. We use the AdamW optimizer with a weight decay of 10−2 and a learning rate of 5 × 10−5 for 10 epochs. Linear warmup is applied to the first 5% of training steps. The effective batch size is set to 64, achieved through gradient accumulation. Each model is trained using different computation resources, including up to 8 A100, 1080ti, and 2080ti Nvidia GPUs.

**中文**

我们在实验中使用 FiDsmall。对于 FiD，增强文档的数量设置为 𝑘 = 10。同样，每个 FiD 模型都在相应的训练集上进行微调。表 2 中列出的所有检索增强模型均单独进行微调。我们使用 AdamW 优化器，权重衰减为 10−2，学习率为 5 × 10−5，持续 10 个时期。线性预热应用于前 5% 的训练步骤。有效batch size设置为64，通过梯度累加实现。每个模型都使用不同的计算资源进行训练，包括最多 8 个 A100、1080ti 和 2080ti Nvidia GPU。

### 段落 54 · Page 5

**EN**

We employ BM25[ 34], implemented in Pyserini [27], to retrieve documents for the training of the aforementioned models. To train the models, a seq2seq loss (i.e., cross-entropy between the predicted token’s probability and the ground truth token distribution) is employed. As detailed in Section 3, each RAG model is required to define a utility function that assesses its performance. To select the utility function for our RAG models, we adhere to the recommended metrics outlined by the KILT benchmark [31]. Thus, we choose the evaluation metric of each dataset as the utility function for the models that perform their task on that dataset.

**中文**

我们使用 Pyserini [27] 中实现的 BM25[34] 来检索用于训练上述模型的文档。为了训练模型，采用了 seq2seq 损失（即预测标记的概率与地面真实标记分布之间的交叉熵）。正如第 3 节中详述的，每个 RAG 模型都需要定义一个评估其性能的效用函数。为了为我们的 RAG 模型选择效用函数，我们遵循 KILT 基准 [31] 概述的推荐指标。因此，我们选择每个数据集的评估指标作为在该数据集上执行任务的模型的效用函数。

### 段落 55 · Page 5

**EN**

Table 2 illustrates the utility functions assigned to the RAG models utilized in this paper. In general, we employ Exact Match (EM) for short-form question answering datasets, ROUGE-L for long-form question answering datasets, and accuracy as the utility function for the remaining tasks. For Exact Match, we follow the post-processing approaches introduced by Rajpurkar et al. [33].

**中文**

表 2 说明了分配给本文中使用的 RAG 模型的效用函数。一般来说，我们对短格式问答数据集采用精确匹配（EM），对长格式问答数据集采用 ROUGE-L，而将准确性作为其余任务的效用函数。对于精确匹配，我们遵循 Rajpurkar 等人引入的后处理方法。 [33]。

### Page 6

### 段落 56 · Page 6

**EN**

SIGIR ’24, July 14–18, 2024, Washington, DC, USA Alireza Salemi and Hamed Zamani 4.3 Search Engine Implementation in uRAG We adopt a two-stage cascaded retrieval pipeline for implementing 𝑅𝜃 . A wikipedia dump provided by the KILT benchmark is used as the unstructured knowledge source.4 We adhere to the preprocessing method outlined by Karpukhin et al. [20], where each document is divided into passages, each with a maximum length of 100 words. Additionally, we concatenate the document title with each passage to form the documents in the retrieval corpus. This corpus consists of approximately 36 million passages.

**中文**

SIGIR ’24，2024 年 7 月 14-18 日，美国华盛顿特区 Alireza Salemi 和 Hamed Zamani 4.3 uRAG 中的搜索引擎实现 我们采用两阶段级联检索管道来实现 𝑅𝜃。 KILT 基准测试提供的维基百科转储用作非结构化知识源。4 我们遵循 Karpukhin 等人概述的预处理方法。 [20]，其中每个文档分为多个段落，每个段落的最大长度为 100 个单词。此外，我们将文档标题与每个段落连接起来，形成检索语料库中的文档。该语料库包含大约 3600 万个段落。

### 段落 57 · Page 6

**EN**

We use Pyserini’s [27] implementation of BM25 with default parameters for implementing the first stage that takes the query string 𝑞 and retrieves 100 documents. The second stage model is a cross-encoder re-ranker that takes the query and document text as input and produces a scalar as the relevance score. To “personalize” the result of the retrieval model, we contextualize the cross-encoder representation based on 𝑀𝑖 and its downstream task 𝑇𝑖.

**中文**

我们使用 Pyserini 的 [27] BM25 实现和默认参数来实现第一阶段，该阶段采用查询字符串 𝑞 并检索 100 个文档。第二阶段模型是跨编码器重新排序器，它将查询和文档文本作为输入并生成标量作为相关性得分。为了“个性化”检索模型的结果，我们将基于 𝑀𝑖 及其下游任务 𝑇𝑖 的跨编码器表示置于上下文中。

### 段落 58 · Page 6

**EN**

Following Nogueira and Cho [30], we use a linear projection over the representation associated with the start token (i.e., [CLS]) to obtain the relevance score, as follows: 𝑠𝑑 = Encoder[CLS](tid; mid; 𝑞; 𝑑) ·𝑊 (3) where tid and mid represent the downstream task and model identifiers, respectively. The sign ; denotes concatenation with a separation token. 𝑊 ∈ R𝐷 ×1 is a linear projection layer, where 𝐷 represents the embedding dimensionality of the encoder. In this paper, we utilize the BERT-base [7] as the text encoder. Once all the 100 documents are re-ranked, the top 𝑘 documents are selected as the model’s output, denoted as𝐿𝑞.

**中文**

遵循 Nogueira 和 Cho [30]，我们在与起始标记（即 [CLS]）相关的表示上使用线性投影来获取相关性得分，如下所示： 𝑠𝑑 = Encoder[CLS](tid; mid; 𝑞; 𝑑) ·𝑊 (3) 其中 tid 和 mid 分别表示下游任务和模型标识符。标志；表示与分隔标记的串联。 𝑊 ∈ R𝐷 ×1 是线性投影层，其中𝐷表示编码器的嵌入维数。在本文中，我们利用 BERT-base [7] 作为文本编码器。对所有 100 个文档重新排序后，将选择顶部 𝑘 文档作为模型的输出，表示为 𝐿𝑞。

### 段落 59 · Page 6

**EN**

Here, the search engine logs the query and the returned results for later use, e.g., using them for optimization when the feedback from the RAG model is received. For optimization, 𝑅𝜃 solicits feedback one by one for each document 𝑑 ∈ 𝐿𝑞. We then apply a threshold𝜏 (tid,mid) to the feedback 𝑈𝑖 received for each document; the feedback higher than or equal to the threshold is considered as a positive feedback, negative otherwise. Based on these feedbacks, we create a set of positive (𝐷𝑞 pos) and negative (𝐷𝑞 neg) documents for each query.

**中文**

在这里，搜索引擎记录查询和返回的结果以供以后使用，例如，在收到来自 RAG 模型的反馈时使用它们进行优化。为了优化，𝑅𝜃 针对每个文档 𝑑 ε 𝐿𝑞 逐一征求反馈。然后，我们将阈值𝜏（tid，mid）应用于每个文档收到的反馈𝑈𝑖；高于或等于阈值的反馈被认为是正反馈，否则被认为是负反馈。根据这些反馈，我们为每个查询创建一组正面 (𝐷𝑞 pos) 和负面 (𝐷𝑞 neg) 文档。

### 段落 60 · Page 6

**EN**

We then apply a binary cross-entropy loss function to train the cross-encoder model: 𝐿 = − 1 |𝑄 | ∑︁ 𝑞 ∈𝑄 ( ∑︁ 𝑑 ∈𝐷𝑞 pos log 𝜎 (𝑠𝑑 ) + ∑︁ 𝑑 ∈𝐷𝑞 neg log 𝜎 (1 − 𝑠𝑑 )) (4) where 𝑄 is the set of all queries used for training. Note that we randomly substitute the model ID and task ID with the“unk” token for 10% of training samples. This aids the model in adapting to new tasks and models during inference. The rationale behind this approach is to train the model to correctly assign labels to samples even when it lacks information about the specific task and model being performed.

**中文**

然后，我们应用二元交叉熵损失函数来训练交叉编码器模型： 𝐿 = − 1 |𝑄 | Σ︁ 𝑞 ε𝑄 ( Σ︁ 𝑑 ε𝐷𝑞 pos log 𝜎 (𝑠𝑑 ) + Σ︁ 𝑑 ε𝐷𝑞 neg log 𝜎 (1 − 𝑠𝑑 )) (4) 其中 𝑄 是用于的所有查询的集合培训。请注意，我们随机用“unk”标记替换 10% 的训练样本的模型 ID 和任务 ID。这有助于模型在推理过程中适应新的任务和模型。这种方法背后的基本原理是训练模型正确地为样本分配标签，即使它缺乏有关正在执行的特定任务和模型的信息。

### 段落 61 · Page 6

**EN**

For training 𝑅𝜃 , we use Adam optimizer [21] with a learning rate of 10−5 for two epochs. Linear warmup is applied to the first 5% of training steps. The effective batch size is set to 512, which is achieved through gradient accumulation. Values of 𝑘 = 32 and 𝜏 (tid,mid) = 0.5 are consistently employed in all experiments. The maximum input length for this model is set to 256 tokens. 4The retrieval corpus is available at https://dl.fbaipublicfiles.com/ur/wikipedia_split/ psgs_w100.tsv.gz 5 EMPIRICAL RESULTS AND FINDINGS This section is dedicated to presenting supporting results that address the research questions outlined in Section 1.

**中文**

对于训练 𝑅𝜃，我们使用 Adam 优化器 [21]，两个时期的学习率为 10−5。线性预热应用于前 5% 的训练步骤。有效batch size设置为512，通过梯度累加实现。所有实验中均一致采用 𝑘 = 32 和 𝜏 (tid,mid) = 0.5 的值。该模型的最大输入长度设置为 256 个令牌。 4 检索语料库可在 https://dl.fbaipublicfiles.com/ur/wikipedia_split/psgs_w100.tsv.gz 上获取。 5 实证结果和发现 本节致力于呈现解决第 1 节中概述的研究问题的支持性结果。

### 段落 62 · Page 6

**EN**

RQ1: How does unified reranking perform compared to training individual rerankers for each RAG model? The results presented in Table 3 offer insights into answering this research question. It is evident all reranking models applied to BM25 lead to improved downstream performance for all 18 models we have in our experiments. The only exception is the models trained and evaluated on FEVER dataset for fact verification. As a point of reference, we also compare the results with Contriever [ 14]–an effective zero-shot dense retrieval models. Contriever consistently underperforms BM25 for all downstream models 𝑀1 to 𝑀18.

**中文**

RQ1：与为每个 RAG 模型训练单独的重排序器相比，统一重排序的表现如何？表 3 中的结果提供了回答该研究问题的见解。很明显，应用于 BM25 的所有重新排序模型都会提高我们实验中所有 18 个模型的下游性能。唯一的例外是在 FEVER 数据集上训练和评估的模型以进行事实验证。作为参考，我们还将结果与 Contriever [14]（一种有效的零样本密集检索模型）进行了比较。对于所有下游模型 𝑀1 到 𝑀18，Contriever 的表现始终低于 BM25。

### 段落 63 · Page 6

**EN**

Additionally, comparing the results obtained by Rerankerunified and Rerankerindividual in Table 3 shows that developing a unified retrieval models for all retrieval-augmented models achieves a better performance for 78% of models (i.e., 14 out of 18 models; all except 𝑀8 on HotPotQA and 𝑀16 to 𝑀18 on T-REx). For the four models that unified retrieval does not show improvement, we do not observe statistically significant differences between model performances. Thus, we can conclude unified retrieval performs on par or significantly better than individual retrieval optimization in almost all cases.

**中文**

此外，比较表 3 中 Rerankerunified 和 Rerankerindividual 获得的结果表明，为所有检索增强模型开发统一的检索模型可以为 78% 的模型实现更好的性能（即 18 个模型中的 14 个模型；除了 HotPotQA 上的𝑀8 和 T-REx 上的𝑀16 至 𝑀18 之外）。对于统一检索没有表现出改进的四个模型，我们没有观察到模型性能之间存在统计上的显着差异。因此，我们可以得出结论，在几乎所有情况下，统一检索的性能与单独检索优化相当或明显更好。

### 段落 64 · Page 6

**EN**

Statistically significant improvement has been observed in 11 out of 18 downstream models. Looking at the overall performance, we show that unified retriever leads to statistically significantly higher performance compared to individual retrievers. In conclusion, the discussion above suggests that our approach, which leverages the feedback from all RAG models across all tasks to optimize the search engine, is significantly superior to the alternative of training a single retrieval model for each RAG model, which is the current standard in developing RAG systems.

**中文**

在 18 个下游模型中，有 11 个模型观察到了统计上的显着改进。从整体性能来看，我们发现，与单个检索器相比，统一检索器在统计上具有显着更高的性能。总之，上面的讨论表明，我们的方法利用所有任务中所有 RAG 模型的反馈来优化搜索引擎，明显优于为每个 RAG 模型训练单个检索模型的替代方案，这是开发 RAG 系统的当前标准。

### 段落 65 · Page 6

**EN**

RQ2: How does unified reranking perform compared to training rerankers using the feedback obtained from all RAG systems that use the same dataset? Instead of retrieval optimization for individual models, one may suggest to train a retrieval model for the downstream models that are using the same task and dataset, which we call Rerankerdataset. Comparing the results obtained by this approach and Rerankerunified in Table 3 suggest that training a unified reranker across the feedback of all users on average statistically significantly outperforms the reranker trained on the feedbacks of models performing on the same dataset.

**中文**

RQ2：与使用从使用相同数据集的所有 RAG 系统获得的反馈来训练重排序器相比，统一重排序的表现如何？我们可能建议为使用相同任务和数据集的下游模型训练一个检索模型，而不是针对单个模型进行检索优化，我们将其称为 Rerankerdataset。比较通过这种方法获得的结果和表 3 中的 Rerankerunified 表明，平均而言，根据所有用户的反馈训练统一的重排序器在统计上显着优于根据在同一数据集上执行的模型的反馈训练的重排序器。

### 段落 66 · Page 6

**EN**

In more details, unified optimization performs better for 72% of models (i.e., 13 out of 18 models; all models except 𝑀10, 𝑀11, 𝑀12, 𝑀17, and 𝑀18, that are all performing on either FEVER or T-REx datasets). Note that there is statistically significant differences in𝑀11 and 𝑀12 users. However, in other cases, there is not a statistically significant difference between the results for 𝑀10, 𝑀17, and 𝑀18. Considering overall performance across models, we observe statistically significant improvements when using unified training.

**中文**

更详细地说，统一优化对于 72% 的模型表现更好（即 18 个模型中的 13 个；除 𝑀10、𝑀11、𝑀12、𝑀17 和 𝑀18 之外的所有模型，它们都在 FEVER 或 T-REx 数据集上执行）。请注意，𝑀11 和 𝑀12 用户在统计上存在显着差异。然而，在其他情况下，𝑀10、𝑀17 和𝑀18 的结果之间不存在统计显着差异。考虑到跨模型的整体性能，我们在使用统一训练时观察到统计上显着的改进。

### 段落 67 · Page 6

**EN**

In summary, the observations above indicate that for all downstream RAG models, leveraging feedback from all RAG models across tasks for optimizing the reranking model is either on par or significantly superior to the alternative approach of training a retrieval model for each dataset. Therefore, retrieval models can benefit from knowledge transfer across datasets and tasks for RAG.

**中文**

总之，上述观察结果表明，对于所有下游 RAG 模型，利用跨任务的所有 RAG 模型的反馈来优化重新排序模型，与为每个数据集训练检索模型的替代方法相当或显着优于其他方法。因此，检索模型可以受益于 RAG 的跨数据集和任务的知识转移。

### Page 7

### 段落 68 · Page 7

**EN**

Towards a Search Engine for Machines: Unified Ranking for Multiple Retrieval-Augmented Large Language Models SIGIR ’24, July 14–18, 2024, Washington, DC, USA Table 3: Downstream performance obtained by 18 RAG models listed in Table 2 consuming different retrieval results. The overal performance is the macro-average of the performance of 18 RAG models. Superscripts 1, 2, 3, 4, and 5 denote statistically significant improvements in the performance compared to BM25, Contriever, Rerankerindividual, Rerankerdataset, and Rerankerunified w/o personalization, respectively. We used McNemar statistical test for significant test ( 𝑝 < 0.05).

**中文**

迈向机器搜索引擎：多种检索增强大型语言模型的统一排名 SIGIR’24，2024 年 7 月 14-18 日，美国华盛顿特区 表 3：表 2 中列出的 18 个 RAG 模型使用不同检索结果获得的下游性能。整体性能是18个RAG模型性能的宏观平均。上标 1、2、3、4 和 5 分别表示与 BM25、Contriever、Rerankerindividual、Rerankerdataset 和 Rerankerunified（不带个性化）相比，性能在统计上显着提高。我们使用 McNemar 统计检验进行显着性检验（𝑝 < 0.05）。

### 段落 69 · Page 7

**EN**

RAG Data & Metric BM25 Contriever Reranker individual Rerankerdataset Rerankerunified RerankerunifiedModel w/o personalization 𝑀1 NQ - EM 28.05 22.55 36.76 37.39 37.18 37.82 12 𝑀2 NQ - EM 33.09 23.68 40.07 40.50 42.29 42.12 1234 𝑀3 NQ - EM 29.64 23.69 40.50 41.14 40.47 42.37 12345 𝑀4 TriviaQA - EM 51.35 44.33 59.28 60.25 60.30 60.68 123 𝑀5 TriviaQA - EM 57.52 48.49 64.76 67.23 67.30 68.12 123 𝑀6 TriviaQA - EM 60.48 49.30 67.44 68.63 69.14 68.74 123 𝑀7 HotPotQA - EM 27.51 18.80 29.92 30.91 31.32 31.33 123 𝑀8 HotPotQA - EM 31.21 20.78 35.03 34.62 34.10 34.85 124 𝑀9 HotPotQA - EM 29.48 20.43 32.54 32.71 32.96 33.46 1234 𝑀10 FEVER - Accuracy 86.8

**中文**

RAG 数据和指标 BM25 Contriever Reranker 个体 Rerankerdataset Rerankerunified RerankerunifiedModel 无个性化 𝑀1 NQ - EM 28.05 22.55 36.76 37.39 37.18 37.82 12 𝑀2 NQ - EM 33.09 23.68 40.07 40.50 42.29 42.12 1234 𝑀3 NQ - 新兴市场 29.64 23.69 40.50 41.14 40.47 42.37 12345 𝑀4 TriviaQA - 新兴市场 51.35 44.33 59.28 60.25 60.30 60.68 123 𝑀5 TriviaQA - 新兴市场 57.52 48.49 64.76 67.23 67.30 68.12 123 𝑀6 TriviaQA - 新兴市场 60.48 49.30 67.44 68.63 69.14 68.74 123 𝑀7 HotPotQA - 新兴市场 27.51 18.80 29.92 30.91 31.32 31.33 123 𝑀8 HotPotQA - 新兴市场 31.21 20.78 35.03 34.62 34.10 34.85 124 𝑀9 HotPotQA - EM 29.48 20.43 32.54 32.71 32.96 33.46 1234 𝑀10 FEVER - 准确度 86.8

### 段落 70 · Page 7

**EN**

3 84.21 86.24 86.83 87.02 86.46 2 𝑀11 FEVER - Accuracy 87.54 84.37 84.38 87.54 86.78 85.99 23 𝑀12 FEVER - Accuracy 87.04 86.74 86.02 87.04 87.21 86.55 23 𝑀13 zsRE - Accuracy 55.37 38.77 60.39 59.98 61.41 61.09 124 𝑀14 zsRE - Accuracy 51.42 29.05 59.29 58.96 60.92 60.58 1234 𝑀15 zsRE - Accuracy 55.42 37.35 60.47 60.66 62.08 62.13 1234 𝑀16 T-REx - Accuracy 70.88 56.94 73.58 72.86 73.70 72.92 12 𝑀17 T-REx - Accuracy 75.16 58.30 80.04 80.18 79.64 79.94 12 𝑀18 T-REx - Accuracy 78.88 65.06 80.78 80.34 80.86 80.24 12 Overall – 55.38 45.15 59.86 60.43 60.81 60.85 1234 RQ3: How does “personalizing” search results for different RAG systems impact the p

**中文**

3 84.21 86.24 86.83 87.02 86.46 2 𝑀11 发烧 - 准确度 87.54 84.37 84.38 87.54 86.78 85.99 23 𝑀12 发烧 - 准确度 87.04 86.74 86.02 87.04 87.21 86.55 23 𝑀13 zsRE - 准确度 55.37 38.77 60.39 59.98 61.41 61.09 124 𝑀14 zsRE - 准确度 51.42 29.05 59.29 58.96 60.92 60.58 1234 𝑀15 zsRE - 准确度 55.42 37.35 60.47 60.66 62.08 62.13 1234 𝑀16 T-REx - 准确度 70.88 56.94 73.58 72.86 73.70 72.92 12 𝑀17 T-REx - 准确度 75.16 58.30 80.04 80.18 79.64 79.94 12 𝑀18 T-REx - 准确度 78.88 65.06 80.78 80.34 80.86 80.24 12 总体– 55.38 45.15 59.86 60.43 60.81 60.85 1234 RQ3：不同 RAG 系统的“个性化”搜索结果如何影响 p

### 段落 71 · Page 7

erformance?

### 段落 72 · Page 7

**EN**

To assess the impact of personalization on the search engine for each RAG model, an experiment was conducted where a reranker was trained similarly to unified reranker but without incorporating task and model IDs as the input of reranker. The results of this experiment are illustrated in Table 3. The results suggest that personalization leads to an improvement on average across all users, but it is not significant. More specifically, the improvements resulting from personalization are most pronounced in the question answering tasks.

**中文**

为了评估个性化对每个 RAG 模型搜索引擎的影响，进行了一项实验，其中重新排序器的训练方式与统一重新排序器类似，但没有将任务和模型 ID 合并为重新排序器的输入。该实验的结果如表 3 所示。结果表明，个性化会导致所有用户的平均改善，但并不显着。更具体地说，个性化带来的改进在问答任务中最为明显。

### 段落 73 · Page 7

**EN**

This is attributed to the similarity among most questions in these datasets, making it challenging for the non-personalized model to discern the specific task associated with a given query. Hence, personalization aids the reranker in identifying the task for which the input is intended and subsequently reranking the documents accordingly. Conversely, the improvements in the slot filling tasks (i.e., T-REx and zsRE) are smaller and for fewer users. Additionally, personalization adversely affects performance in the FEVER dataset.

**中文**

这是由于这些数据集中大多数问题之间的相似性，使得非个性化模型难以辨别与给定查询相关的特定任务。因此，个性化有助于重新排序器识别输入所针对的任务，并随后相应地对文档进行重新排序。相反，槽填充任务（即 T-REx 和 zsRE）的改进较小，并且适用于较少的用户。此外，个性化会对 FEVER 数据集中的性能产生不利影响。

### 段落 74 · Page 7

**EN**

These observations indicate that while, on average, our approach for personalization was effective, there is potential for a further study on how to effectively personalize the search engine for RAG models, which is an important topic for future exploration. RQ4: How does unified reranking perform for new (unknown) RAG systems that use an observed (known) dataset? We design an experiment in which we incorporate three new RAG models with different architecture and pre-training process: (1) Retrieval-augmented PEGASUS (RA-PEGASUS) uses in-prompt augmentation with the PEGASUS language model [58] which has 570 million parameters.

**中文**

这些观察结果表明，虽然平均而言，我们的个性化方法是有效的，但仍有可能进一步研究如何有效地个性化 RAG 模型的搜索引擎，这是未来探索的一个重要课题。 RQ4：对于使用观察到的（已知）数据集的新（未知）RAG 系统，统一重排如何执行？我们设计了一个实验，其中结合了三种具有不同架构和预训练过程的新 RAG 模型：（1）检索增强 PEGASUS（RA-PEGASUS）使用具有 5.7 亿个参数的 PEGASUS 语言模型 [58] 进行即时增强。

### 段落 75 · Page 7

**EN**

We use the same input format as Table 4: A list of RAG models used in our experiments for evaluating generalizability of uRAG. ELI5 is also an opendomain QA dataset, but the expected outputs are longer (e.g., sentences or a paragraph) compared to other datasets. Task Data Utility Func.

**中文**

我们使用与表 4 相同的输入格式：我们实验中使用的 RAG 模型列表，用于评估 uRAG 的通用性。 ELI5 也是一个开放域 QA 数据集，但与其他数据集相比，预期输出更长（例如句子或段落）。任务数据实用功能

### 段落 76 · Page 7

**EN**

LM 𝑀19 entity linking AY2 Accuracy RA-T5 𝑀20 long-form QA ELI5 ROUGE-L RA-T5 𝑀21 open-domain QA SQuAD Exact Match RA-T5 𝑀22 entity linking AY2 Accuracy RA-BART 𝑀23 long-form QA ELI5 ROUGE-L RA-BART 𝑀24 open-domain QA SQuAD Exact Match RA-BART 𝑀25 open-domain QA NQ Exact Match RA-PEGASUS 𝑀26 open-domain QA TriviaQA Exact Match RA-PEGASUS 𝑀27 long-form QA ELI5 ROUGE-L RA-PEGASUS 𝑀28 open-domain QA SQuAD Exact Match RA-PEGASUS 𝑀29 open-domain QA NQ Exact Match RA-Mistral 𝑀30 open-domain QA TriviaQA Exact Match RA-Mistral 𝑀31 long-form QA ELI5 ROUGE-L RA-Mistral 𝑀32 open-domain QA SQuAD Exact Match RA-Mistral 𝑀33 open-domain QA NQ Exact Match RA-

**中文**

LM 𝑀19 实体链接 AY2 准确度 RA-T5 𝑀20 长格式 QA ELI5 ROUGE-L RA-T5 𝑀21 开放域 QA SQuAD 精确匹配 RA-T5 𝑀22 实体链接 AY2 准确度 RA-BART 𝑀23 长格式 QA ELI5 ROUGE-L RA-BART 𝑀24 开放域 QA SQuAD 精确匹配 RA-BART 𝑀25 开放域 QA NQ 精确匹配 RA-PEGASUS 𝑀26 开放域 QA TriviaQA 精确匹配 RA-PEGASUS 𝑀27 长格式 QA ELI5 ROUGE-L RA-PEGASUS 𝑀28 开放域 QA SQuAD 精确匹配RA-PEGASUS 𝑀29 开放域 QA NQ 精确匹配 RA-Mistral 𝑀30 开放域 QA TriviaQA 精确匹配 RA-Mistral 𝑀31 长格式 QA ELI5 ROUGE-L RA-Mistral 𝑀32 开放域 QA SQuAD 精确匹配 RA-Mistral 𝑀33 开放域 QA NQ精确匹配 RA-

### 段落 77 · Page 7

**EN**

Llama2 𝑀34 open-domain QA TriviaQA Exact Match RA-Llama2 𝑀35 long-form QA ELI5 ROUGE-L RA-Llama2 𝑀36 open-domain QA SQuAD Exact Match RA-Llama2 used by RA-T5 and RA-BART (see Section 4.2).

**中文**

Llama2 𝑀34 开放域 QA TriviaQA 精确匹配 RA-Llama2 𝑀35 长格式 QA ELI5 ROUGE-L RA-Llama2 𝑀36 开放域 QA SQuAD RA-T5 和 RA-BART 使用的精确匹配 RA-Llama2（参见第 4.2 节）。

### 段落 78 · Page 7

**EN**

PEGASUS has a 1024 maximum token limit as its input; thus we limit this model to consume 𝑘 = 4 retrieved documents. RA-PEGASUS models are also fined-tuned on the training set of the corresponding datasets. The fine-tuning details are the same as other retrieval-augmented models presented in Section 4.2. (2) Retrieval-augmented Mistral (RA-Mistral) also uses in-prompt augmentation for Mistral LLM with 7 billion parameters [18],

**中文**

PEGASUS 的输入最大代币限制为 1024 个；因此，我们限制该模型消耗 𝑘 = 4 个检索到的文档。 RA-PEGASUS 模型也在相应数据集的训练集上进行了微调。微调细节与 4.2 节中介绍的其他检索增强模型相同。 (2) 检索增强 Mistral (RA-Mistral) 还对具有 70 亿个参数的 Mistral LLM 使用即时增强 [18]，

### Page 8

### 段落 79 · Page 8

**EN**

SIGIR ’24, July 14–18, 2024, Washington, DC, USA Alireza Salemi and Hamed Zamani Table 5: The performance on downstream task obtained for new (unknown) models applied to the datasets known to 𝑅𝜃 . Superscript 1 and 2 denote statistically difference between our model and BM25 and Rerankerdataset, respectively (𝑝 < 0.05). RAG Data & Metric BM25 Rerankerdataset RerankerunifiedModel 𝑀25 NQ - EM 33.38 45.08 45.291 𝑀29 NQ - EM 15.15 21.36 21.251 𝑀33 NQ - EM 11.13 16.53 16.561 𝑀26 TQA - EM 53.53 61.74 62.391 𝑀30 TQA - EM 44.74 50.40 50.191 𝑀34 TQA - EM 25.86 29.63 29.221 with no fine-tuning.

**中文**

SIGIR ’24，2024 年 7 月 14-18 日，美国华盛顿特区 Alireza Salemi 和 Hamed Zamani 表 5：应用于已知数据集的新（未知）模型获得的下游任务性能。上标 1 和 2 分别表示我们的模型与 BM25 和 Rerankerdataset 之间的统计差异（𝑝 < 0.05）。 RAG 数据和指标 BM25 Rerankerdataset RerankerunifiedModel 𝑀25 NQ - EM 33.38 45.08 45.291 𝑀29 NQ - EM 15.15 21.36 21.251 𝑀33 NQ - EM 11.13 16.53 16.561 𝑀26 TQA - EM 53.53 61.74 62.391 𝑀30 TQA - EM 44.74 50.40 50.191 𝑀34 TQA - EM 25.86 29.63 29.221 无需微调。

### 段落 80 · Page 8

**EN**

Instead, to increase the diversity of models in our experiments, we use few-shot in-context learning for this approach, where five training examples are presented to the model in its prompt. Mistral can accept up to 32k tokens as input (including the few-shot examples). We feed 𝑘 = 5 retrieved documents to this model.5 (3) Retrieval-augmented Llama2 (RA-Llama2) uses an in-prompt augmentation approach similar to RA-Mistral, but using Llama2 with 13 billion parameters[47]. It also uses few-shot in-content learning, but with two examples instead (due to the input length limitation). Llama2 can accept up to 4096 tokens as input.

**中文**

相反，为了增加实验中模型的多样性，我们在这种方法中使用了少样本上下文学习，其中在提示中向模型提供了五个训练示例。 Mistral 最多可以接受 32k 个令牌作为输入（包括少数样本）。我们向该模型提供 𝑘 = 5 个检索到的文档。5 (3) 检索增强 Llama2 (RA-Llama2) 使用类似于 RA-Mistral 的即时增强方法，但使用具有 130 亿个参数的 Llama2[47]。它还使用少样本内容学习，但用两个示例代替（由于输入长度限制）。 Llama2 最多可以接受 4096 个令牌作为输入。

### 段落 81 · Page 8

**EN**

RA-Llama2 uses𝑘 = 3 retrieved documents.6 To address this research question, we evaluate these models on two existing datasets from our pipeline: Natural Questions (NQ) and TriviaQA (TQA). These models are denoted as 𝑀25, 𝑀26, 𝑀29, 𝑀30, 𝑀33, and 𝑀34, as is presented in Table 4. Since these models are new to our rerankers, their model and task ID is set tounknown, thus no personalization is conducted for these models. By comparing our unified reranking model with BM25 without reranking in Table 5, we observe significant improvements in all cases in comparison with BM25. The improvements range from 11% to about 50%.

**中文**

RA-Llama2 使用 𝑘 = 3 个检索到的文档。6 为了解决这个研究问题，我们在管道中的两个现有数据集上评估这些模型：自然问题 (NQ) 和 TriviaQA (TQA)。这些模型被表示为𝑀25、𝑀26、𝑀29、𝑀30、𝑀33 和𝑀34，如表 4 所示。由于这些模型对于我们的重新排序器来说是新的，因此它们的模型和任务 ID 设置为未知，因此不对这些模型进行个性化。通过将我们的统一重排序模型与表 5 中未重排序的 BM25 进行比较，我们观察到与 BM25 相比，在所有情况下都有显着改进。改进范围从 11% 到约 50%。

### 段落 82 · Page 8

**EN**

Larger improvements are observed for the models evaluated on the Natural Questions dataset, which was also the case for the models used in our training process (see Table 3). Moreover, an alternative approach involves leveraging Rerankerdataset, which has been trained using the feedbacks from multiple large language models. The results of this alternative approach are also presented in Table 5. The results reveal that, for certain users,Rerankerunified yields superior results, while for others, Rerankerdataset performs better.

**中文**

在 Natural Questions 数据集上评估的模型观察到了较大的改进，我们的训练过程中使用的模型也是如此（见表 3）。此外，另一种方法涉及利用 Rerankerdataset，该数据集已使用多个大型语言模型的反馈进行了训练。表 5 中还列出了这种替代方法的结果。结果表明，对于某些用户，Rerankerunified 会产生更好的结果，而对于其他用户，Rerankerdataset 表现更好。

### 段落 83 · Page 8

**EN**

Additionally, there is no statistically significant difference in performance between these models, suggesting comparable effectiveness in leveraging feedback from multiple large language models when it comes to serving a new large language model. RQ5: How does unified reranking perform for a known RAG system on a new (unknown) dataset that is similar to the ones used during training? To study this question, we conduct an experiment in which RA-BART and RA-T5 are employed as 5RA-Mistral uses the following prompt: <s>[INST] you are a helpful assistant.

**中文**

此外，这些模型之间的性能没有统计学上的显着差异，这表明在服务新的大型语言模型时，利用多个大型语言模型的反馈的效果相当。 RQ5：对于已知 RAG 系统，在与训练期间使用的数据集类似的新（未知）数据集上，统一重排序如何执行？为了研究这个问题，我们进行了一个实验，其中使用 RA-BART 和 RA-T5 作为 5RA-Mistral 使用以下提示：<s>[INST] 你是一个有用的助手。

### 段落 84 · Page 8

**EN**

following the answer patterns in the provided examples, answer the question concisely using the hints without any explanation. {shot 1} ... {shot𝑚 } [/INST] question: {input}? hint: {context 1} ... {context 𝑘 } answer: 6RA-Llama2 uses the following prompt:you are a helpful assistant. following the answer patterns in the provided examples, answer the question concisely using the hints without any explanation. {shot 1} ... {shot 𝑚 } question: {input}? hint: {context 1} ... {context 𝑘 } answer: Table 6: The performance for new (unknown) models applied to the new datasets.

**中文**

按照所提供示例中的回答模式，使用提示简洁地回答问题，无需任何解释。 {镜头 1} ... {镜头𝑚 } [/INST] 问题：{输入}？提示：{context 1} ... {context 𝑘 } 答案：6RA-Llama2 使用以下提示：您是一位有用的助手。按照所提供示例中的回答模式，使用提示简洁地回答问题，无需任何解释。 {镜头 1} ... {镜头 𝑚 } 问题：{输入}？提示：{context 1} ... {context 𝑘 } 答案：表 6：应用于新数据集的新（未知）模型的性能。

### 段落 85 · Page 8

**EN**

SQuAD is a question answering dataset with short answers, thus similar to the datasets used during training such as NQ and TriviaQA. ELI5 focuses on longform question answering, a task fundamentally different from datasets used during 𝑅𝜃 training. AY2 is a dataset for entity linking, which is not used for training 𝑅𝜃 . Superscript ∗ denotes significant improvement over BM25 ( 𝑝 < 0.05).

**中文**

SQuAD 是一个简短答案的问答数据集，因此类似于 NQ 和 TriviaQA 等训练期间使用的数据集。 ELI5 专注于长篇问答，这项任务与 𝑅𝜃 训练期间使用的数据集根本不同。 AY2 是实体链接的数据集，不用于训练 𝑅𝜃。上标*表示比BM25有显着改进（𝑝<0.05）。

### 段落 86 · Page 8

**EN**

RAG Data & Metric BM25 Reranker unifiedModel 𝑀21 SQuAD - EM 35.91 41.19∗ 𝑀24 SQuAD - EM 32.92 36.70∗ 𝑀19 AY2 - Accuracy 75.52 73.3 𝑀22 AY2 - Accuracy 81.98 82.08 𝑀20 ELI5 - ROUGE-L 15.40 15.42 𝑀23 ELI5 - ROUGE-L 23.42 23.24 Table 7: The performance for new (unknown) models applied to new datasets that are unknown to 𝑅𝜃 . Superscript ∗ denotes statistically significant improvement over BM25 ( 𝑝 < 0.05).

**中文**

RAG 数据和指标 BM25 Reranker 统一模型 𝑀21 SQuAD - EM 35.91 41.19* 𝑀24 SQuAD - EM 32.92 36.70* 𝑀19 AY2 - 准确度 75.52 73.3 𝑀22 AY2 - 准确度 81.98 82.08 𝑀20 ELI5 - ROUGE-L 15.40 15.42 𝑀23 ELI5 - ROUGE-L 23.42 23.24 表 7：应用于 𝑅𝜃 未知的新数据集的新（未知）模型的性能。上标 * 表示相对 BM25 具有统计显着性改善 ( 𝑝 < 0.05)。

### 段落 87 · Page 8

**EN**

RAG Data & Metric BM25 Reranker unifiedModel 𝑀28 SQuAD - EM 36.37 42.04∗ 𝑀32 SQuAD - EM 13.01 15.18∗ 𝑀36 SQuAD - EM 10.31 12.06∗ 𝑀27 ELI5 - ROUGE-L 19.84 19.79 𝑀31 ELI5 - ROUGE-L 22.03 21.98 𝑀35 ELI5 - ROUGE-L 19.16 18.77 known models to the search engine for a new dataset, SQuAD [33], which performs a known task (i.e., short-form open-domain question answering). These models are encoded as𝑀21 and 𝑀24 (see Table 4). We use the open-domain variant of SQuAD [33] where the gold passage associated to each question is unknown. The results of this experiment are presented in Table 6.

**中文**

RAG 数据和指标 BM25 Reranker 统一模型 𝑀28 SQuAD - EM 36.37 42.04* 𝑀32 SQuAD - EM 13.01 15.18* 𝑀36 SQuAD - EM 10.31 12.06* 𝑀27 ELI5 - ROUGE-L 19.84 19.79 𝑀31 ELI5 - ROUGE-L 22.03 21.98 𝑀35 ELI5 - ROUGE-L 19.16 18.77 搜索引擎的新数据集 SQuAD [33] 的已知模型，该数据集执行已知任务（即短格式开放域问答）。这些模型被编码为𝑀21和𝑀24（见表4）。我们使用 SQuAD [33] 的开放域变体，其中与每个问题相关的黄金段落都是未知的。该实验的结果如表 6 所示。

### 段落 88 · Page 8

**EN**

The results suggest that when the new task is similar to the known tasks for the search engine, as in the case of SQuAD being similar to short-form question answering datasets used during training (i.e., NQ, TQA), significant improvements can still be achieved in comparison with the baseline (i.e., BM25). Note that the selection of baselines in this experiment is influenced by the consideration that other reranker baselines listed in Table 3 are customized for specific model or dataset; they are not applicable to new models and datasets. RQ6: How does unified reranking perform for a known RAG system on entirely new tasks?

**中文**

结果表明，当新任务与搜索引擎的已知任务相似时，例如 SQuAD 与训练期间使用的简短问答数据集（即 NQ、TQA）相似的情况下，与基线（即 BM25）相比，仍然可以实现显着的改进。请注意，本实验中基线的选择受到表 3 中列出的其他重排序基线是针对特定模型或数据集定制的考虑因素的影响；它们不适用于新模型和数据集。 RQ6：对于已知的 RAG 系统来说，统一重排序在全新任务上的表现如何？

### 段落 89 · Page 8

**EN**

To study this question, we conduct an experiment in which RA-BART and RA-T5 are employed as known models to the search engine for new tasks. ELI5 [10] serves as a long-form question answering task and AY2 [13] as an entity linking dataset, which are new tasks for the search engine. These models are denoted as 𝑀19, 𝑀20, 𝑀22, and 𝑀23 (see Table 4). The results of this experiment, presented in Table 6, suggest that when tasks are considerably different from the ones observed during training, unified retrieval as implemented in this approach is not likely to help.

**中文**

为了研究这个问题，我们进行了一项实验，其中 RA-BART 和 RA-T5 被用作新任务搜索引擎的已知模型。 ELI5 [10] 作为长格式问答任务，AY2 [13] 作为实体链接数据集，这是搜索引擎的新任务。这些模型表示为 𝑀19、𝑀20、𝑀22 和 𝑀23（参见表 4）。表 6 所示的实验结果表明，当任务与训练期间观察到的任务有很大不同时，在此方法中实现的统一检索不太可能有帮助。

### 段落 90 · Page 8

**EN**

Indeed, unified retrieval model demonstrates superior performance for some users; however, there is no statistical

**中文**

事实上，统一检索模型对某些用户展示了卓越的性能；但目前尚无统计数据

### Page 9

### 段落 91 · Page 9

**EN**

Towards a Search Engine for Machines: Unified Ranking for Multiple Retrieval-Augmented Large Language Models SIGIR ’24, July 14–18, 2024, Washington, DC, USA Figure 3: The performance of unified retrieval model using different percentages of training data. The dashed line indicates that the model is trained on the full dataset. The far right plot demonstrate the overall average performance across all datasets. difference between the unified retrieval model and the baseline. This creates an important opportunity for future work to focus on generalizability and adaptability of uRAG to unknown tasks.

**中文**

迈向机器搜索引擎：多重检索增强大型语言模型的统一排名 SIGIR ’24，2024 年 7 月 14-18 日，美国华盛顿特区 图 3：使用不同百分比训练数据的统一检索模型的性能。虚线表示模型是在完整数据集上训练的。最右边的图显示了所有数据集的总体平均性能。统一检索模型与基线之间的差异。这为未来的工作重点关注 uRAG 对未知任务的通用性和适应性创造了重要的机会。

### 段落 92 · Page 9

**EN**

RQ7: How does unified reranking perform for a new (unknown) RAG system on a new (unknown) dataset that is similar to the ones used during training? To answer this question, in this experiment, we utilize RA-PEGASUS, RA-Mistral, and RA-Llama2 on SQuAD. These are models that did not exist at the time of training 𝑅𝜃 and SQuAD is a new (unknown) dataset for 𝑅𝜃 but related to NQ and TriviaQA. These models are encoded as 𝑀28, 𝑀32, and 𝑀36 (see Table 4). The results of this experiment are displayed in Table 7.

**中文**

RQ7：对于新（未知）RAG 系统，在与训练期间使用的数据集类似的新（未知）数据集上，统一重排序如何执行？为了回答这个问题，在本实验中，我们在 SQuAD 上使用 RA-PEGASUS、RA-Mistral 和 RA-Llama2。这些模型在训练 𝑅𝜃 时不存在，SQuAD 是 𝑅𝜃 的新（未知）数据集，但与 NQ 和 TriviaQA 相关。这些模型被编码为 𝑀28、𝑀32 和 𝑀36（参见表 4）。该实验的结果显示在表7中。

### 段落 93 · Page 9

**EN**

The findings indicate that when the task is similar to those encountered during model training (e.g., SQuAD in this case similar to NQ and TriviaQA in the training tasks), significant improvements over the baseline can be achieved even though the RAG model is unknown to the search engine. RQ8: How does unified reranking perform for a new RAG system on an entirely new (unknown) task? In the most extreme case, both the task and the model are unknown to the search engine. Here, we utilize RA-PEGASUS, RA-Mistral, and RA-Llama2 on ELI5 dataset as a new task that is relatively different from the tasks used during training.

**中文**

研究结果表明，当任务与模型训练期间遇到的任务类似时（例如，本例中的 SQuAD 与训练任务中的 NQ 和 TriviaQA 类似），即使 RAG 模型对于搜索引擎来说是未知的，也可以在基线上实现显着改进。 RQ8：对于全新的（未知）任务，新的 RAG 系统的统一重排序如何执行？在最极端的情况下，任务和模型对于搜索引擎来说都是未知的。在这里，我们在 ELI5 数据集上使用 RA-PEGASUS、RA-Mistral 和 RA-Llama2 作为新任务，与训练期间使用的任务相对不同。

### 段落 94 · Page 9

**EN**

These models are encoded as 𝑀27, 𝑀31, and 𝑀35. The results in Table 7 indicate that when the task is substantially different from those available during training, as is in ELI5 (i.e., long-form question answering), there is a drop in performance, though not statistically significant. RQ9: How does uRAG perform when different amount of training data is provided? We vary the amount of training data obtained from each downstream RAG model to 25%, 50%, 75%, and 100% of the data used in other experiments.

**中文**

这些模型编码为 𝑀27、𝑀31 和 𝑀35。表 7 中的结果表明，当任务与训练期间可用的任务有很大不同时，如 ELI5（即长格式问答）中的情况，性能会下降，尽管在统计上并不显着。 RQ9：在提供不同数量的训练数据时，uRAG 的表现如何？我们将从每个下游 RAG 模型获得的训练数据量更改为其他实验中使用的数据的 25%、50%、75% 和 100%。

### 段落 95 · Page 9

**EN**

The results in Figure 3 show that even using 25% of the training data, our approach is sufficiently effective to outperform the baseline trained on the full datasets (i.e., Rerankerdataset) in average. This trend continues when our approach consumes more data where it outperforms the baseline significantly when trained on the full datasets. Furthermore, for most users, augmenting the training data improves the performance. Particularly noteworthy is the fact that for the FEVER and T-REx datasets, the optimal performance is achieved when utilizing 75% of the training data.

**中文**

图 3 中的结果表明，即使使用 25% 的训练数据，我们的方法也足够有效，平均优于在完整数据集（即 Rerankerdataset）上训练的基线。当我们的方法消耗更多数据时，这种趋势会继续下去，并且在完整数据集上进行训练时，其性能显着优于基线。此外，对于大多数用户来说，增加训练数据可以提高性能。特别值得注意的是，对于 FEVER 和 T-REx 数据集，当利用 75% 的训练数据时，可以实现最佳性能。

### 段落 96 · Page 9

**EN**

Importantly, for the majority of users, excluding 𝑀1, 𝑀6, 𝑀10, 𝑀11, and 𝑀12, our approach either outperforms or performs equivalently to the baseline, trained on the full datasets, by observing 50% of the training data. This underscores the effectiveness of unified reranking, especially when confronted with limited training data, for most users. 6 CONCLUSION & FUTURE WORK We studied the promises and challenges in developing a search engine for multiple downstream RAG systems. We introduced the uRAG ecosystem that enabled us to conduct large-scale experimentation to answer some fundamental research questions in this area.

**中文**

重要的是，对于大多数用户（不包括 𝑀1、𝑀6、𝑀10、𝑀11 和 𝑀12），我们的方法通过观察 50% 的训练数据，在完整数据集上进行训练，表现优于或相当于基线。这强调了统一重排的有效性，尤其是在面对有限的训练数据时，对于大多数用户而言。 6 结论和未来工作 我们研究了为多个下游 RAG 系统开发搜索引擎的前景和挑战。我们引入了 uRAG 生态系统，使我们能够进行大规模实验来回答该领域的一些基础研究问题。

### 段落 97 · Page 9

**EN**

We showed that optimizing a unified reranker leads to significant improvements compared to the current standard recipe–i.e., learning a retrieval model per downstream RAG model. We highlighted the improvements observed by the unified reranker is generalizable to new (unknown) models that are based on known datasets or unknown datasets that are closely related to the ones used in the training procedure. We further explained the challenges in personalizing rerankers for downstream RAG models and generalizing to unknown downstream tasks. This paper opens up a wide range of future research directions.

**中文**

我们表明，与当前的标准配方相比，优化统一的重新排序器可以带来显着的改进，即根据下游 RAG 模型学习检索模型。我们强调，统一重排序器观察到的改进可以推广到基于已知数据集或与训练过程中使用的数据集密切相关的未知数据集的新（未知）模型。我们进一步解释了下游 RAG 模型的个性化重排器以及泛化到未知下游任务的挑战。本文开辟了广泛的未来研究方向。

### 段落 98 · Page 9

**EN**

Through the proposed uRAG ecosystem, future work can focus on (1) optimal aggregation of feedback from various downstream RAG models, (2) calibrating their feedback, (3) considering multiple utility functions per downstream model, (4) expanding the work to retrieval model optimization instead of reranking, (5) studying novel regularization techniques for improvinguRAG generalization, (6) studying online optimization of methods for uRAG as downstream RAG models interact with the retrieval model, (7) exploring interleaving and counterfactual learning approaches in the context of uRAG, (8) going beyond text generation and extending to a more general REML scenario, and many more.

**中文**

通过所提出的 uRAG 生态系统，未来的工作可以重点关注（1）来自各种下游 RAG 模型的反馈的最佳聚合，（2）校准其反馈，（3）考虑每个下游模型的多个效用函数，（4）将工作扩展到检索模型优化而不是重新排序，（5）研究用于改进 uRAG 泛化的新颖正则化技术，（6）研究下游 RAG 模型与检索模型交互时 uRAG 方法的在线优化，（7）探索交叉和反事实学习方法uRAG 的上下文，(8) 超越文本生成并扩展到更通用的 REML 场景，等等。

### 段落 99 · Page 9

**EN**

ACKNOWLEDGMENTS The authors would like to thank Fernando Diaz for invaluable discussions. This work was supported in part by the Center for Intelligent Information Retrieval, in part by NSF grant number 2143434, in part by the Office of Naval Research contract number N000142212688, in part by Lowe’s, and in part by an Amazon Research Award, Fall 2022 CFP. Any opinions, findings and conclusions or recommendations expressed in this material are those of the authors and do not necessarily reflect those of the sponsor.

**中文**

致谢 作者要感谢 Fernando Diaz 所做的宝贵讨论。这项工作部分得到了智能信息检索中心的支持，部分得到了 NSF 拨款号 2143434 的支持，部分得到了海军研究办公室合同号 N000142212688 的支持，部分得到了 Lowe’s 的支持，部分得到了亚马逊研究奖，2022 年秋季 CFP 的支持。本材料中表达的任何意见、调查结果和结论或建议均为作者的观点、发现和结论或建议，并不一定反映申办者的观点。

### Page 10

### 段落 100 · Page 10

**EN**

SIGIR ’24, July 14–18, 2024, Washington, DC, USA Alireza Salemi and Hamed Zamani REFERENCES [1] 2024. The ChatGPT Retrieval Plugin. https://github.com/openai/chatgptretrieval-plugin. Accessed: 2024-01-20. [2] Garima Agrawal, Tharindu Kumarage, Zeyad Alghami, and Huan Liu. 2023. Can Knowledge Graphs Reduce Hallucinations in LLMs? : A Survey. arXiv:2311.07914 [cs.CL] [3] Akari Asai, Zeqiu Wu, Yizhong Wang, Avirup Sil, and Hannaneh Hajishirzi. 2023. Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection. arXiv:2310.11511 [cs.CL] [4] Deng Cai, Yan Wang, Huayang Li, Wai Lam, and Lemao Liu. 2021.

**中文**

SIGIR ’24，2024 年 7 月 14-18 日，美国华盛顿特区 Alireza Salemi 和 Hamed Zamani 参考资料 [1] 2024。ChatGPT 检索插件。 https://github.com/openai/chatgptretrieval-plugin。访问时间：2024 年 1 月 20 日。 [2] Garima Agrawal、Tharindu Kumarage、Zeyad Alghami 和 Huan Liu。 2023.知识图谱可以减少法学硕士的幻觉吗？：一项调查。 arXiv:2311.07914 [cs.CL] [3] Akari Asai、Zeqiu Wu、Yizhong Wang、Avirup Sil 和 Hannaneh Hajishirzi。 2023.Self-RAG：通过自我反思学习检索、生成和批判。 arXiv:2310.11511 [cs.CL] [4] Deng Cai、Yan Wang、Huayang Li、Wai Lam 和 Lemao Liu。 2021 年。

### 段落 101 · Page 10

**EN**

Neural Machine Translation with Monolingual Translation Memory. In Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (Volume 1: Long Papers). Association for Computational Linguistics, Online, 7307–7318. https://doi.org/10.18653/v1/2021.acl-long.567 [5] Wenhu Chen, Hexiang Hu, Xi Chen, Pat Verga, and William Cohen. 2022. MuRAG: Multimodal Retrieval-Augmented Generator for Open Question Answering over Images and Text. InProceedings of the 2022 Conference on Empirical Methods in Natural Language Processing.

**中文**

具有单语翻译记忆库的神经机器翻译。计算语言学协会第 59 届年会暨第 11 届自然语言处理国际联合会议论文集（第一卷：长论文）。计算语言学协会，在线，7307–7318。 https://doi.org/10.18653/v1/2021.acl-long.567 [5] 陈文虎，胡鹤翔，陈曦，帕特·维尔加，威廉·科恩。 2022. MuRAG：用于图像和文本开放式问答的多模态检索增强生成。 2022 年自然语言处理经验方法会议论文集。

### 段落 102 · Page 10

**EN**

Association for Computational Linguistics, Abu Dhabi, United Arab Emirates, 5558–5570. https://doi.org/10.18653/v1/2022.emnlpmain.375 [6] Hao Cheng, Yelong Shen, Xiaodong Liu, Pengcheng He, Weizhu Chen, and Jianfeng Gao. 2021. UnitedQA: A Hybrid Approach for Open Domain Question Answering. In Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (Volume 1: Long Papers) . Association for Computational Linguistics, Online, 3080–3090.

**中文**

计算语言学协会，阿拉伯联合酋长国阿布扎比，5558–5570。 https://doi.org/10.18653/v1/2022.emnlpmain.375 [6] 程浩，沉叶龙，刘晓东，何鹏程，陈伟柱，高剑峰。 2021.UnitedQA：开放域问答的混合方法。计算语言学协会第 59 届年会暨第 11 届自然语言处理国际联合会议论文集（第一卷：长论文）。计算语言学协会，在线，3080–3090。

### 段落 103 · Page 10

**EN**

https://doi.org/10.18653/v1/2021.acl-long.240 [7] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. 2019. BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. In Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long and Short Papers). Association for Computational Linguistics, Minneapolis, Minnesota, 4171–4186. https://doi.org/10.18653/v1/N19-1423 [8] Emily Dinan, Stephen Roller, Kurt Shuster, Angela Fan, Michael Auli, and Jason Weston. 2019.

**中文**

https://doi.org/10.18653/v1/2021.acl-long.240 [7] Jacob Devlin、Ming-Wei Chang、Kenton Lee 和 Kristina Toutanova。 2019.BERT：用于语言理解的深度双向Transformer的预训练。计算语言学协会北美分会 2019 年会议记录：人类语言技术，第 1 卷（长论文和短论文）。计算语言学协会，明尼苏达州明尼阿波利斯，4171-4186。 https://doi.org/10.18653/v1/N19-1423 [8] 艾米莉·迪南、斯蒂芬·罗勒、库尔特·舒斯特、安吉拉·范、迈克尔·奥利和杰森·韦斯顿。 2019.

### 段落 104 · Page 10

**EN**

Wizard of Wikipedia: Knowledge-Powered Conversational Agents. In International Conference on Learning Representations . https://openreview.net/ forum?id=r1l73iRqKm [9] Hady Elsahar, Pavlos Vougiouklis, Arslen Remaci, Christophe Gravier, Jonathon Hare, Frederique Laforest, and Elena Simperl. 2018. T-REx: A Large Scale Alignment of Natural Language with Knowledge Base Triples.

**中文**

维基百科向导：知识驱动的对话代理。在国际学习代表会议上。 https://openreview.net/forum?id=r1l73iRqKm [9]Hady Elsahar、Pavlos Vougiouklis、Arslen Remaci、Christophe Gravier、Jonathon Hare、Frederique Laforest 和 Elena Simperl。 2018。T-REx：自然语言与知识库三元组的大规模对齐。

### 段落 105 · Page 10

**EN**

In Proceedings of the Eleventh International Conference on Language Resources and Evaluation (LREC 2018), Nicoletta Calzolari, Khalid Choukri, Christopher Cieri, Thierry Declerck, Sara Goggi, Koiti Hasida, Hitoshi Isahara, Bente Maegaard, Joseph Mariani, Hélène Mazo, Asuncion Moreno, Jan Odijk, Stelios Piperidis, and Takenobu Tokunaga (Eds.). European Language Resources Association (ELRA), Miyazaki, Japan. https://aclanthology.org/L18-1544 [10] Angela Fan, Yacine Jernite, Ethan Perez, David Grangier, Jason Weston, and Michael Auli. 2019. ELI5: Long Form Question Answering.

**中文**

第十一届语言资源与评估国际会议 (LREC 2018) 论文集，Nicoletta Calzolari、Khalid Choukri、Christopher Cieri、Thierry Declerck、Sara Goggi、Koiti Hasida、Hitoshi Isahara、Bente Maegaard、Joseph Mariani、Hélène Mazo、Asuncion Moreno、Jan Odijk、Stelios Piperidis 和 Takenobu Tokunaga （编辑）。欧洲语言资源协会 (ELRA)，日本宫崎。 https://aclanthology.org/L18-1544 [10] Angela Fan、Yacine Jernite、Ethan Perez、David Grangier、Jason Weston 和 Michael Auli。 2019. ELI5：长格式问答。

### 段落 106 · Page 10

**EN**

In Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics , Anna Korhonen, David Traum, and Lluís Màrquez (Eds.). Association for Computational Linguistics, Florence, Italy, 3558–3567. https://doi.org/10.18653/v1/P19-1346 [11] Michael Glass, Gaetano Rossiello, Md Faisal Mahbub Chowdhury, Ankita Naik, Pengshan Cai, and Alfio Gliozzo. 2022. Re2G: Retrieve, Rerank, Generate. In Proceedings of the 2022 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies , Marine Carpuat, Marie-Catherine de Marneffe, and Ivan Vladimir Meza Ruiz (Eds.).

**中文**

计算语言学协会第 57 届年会记录，Anna Korhonen、David Traum 和 Lluís Màrquez（编辑）。计算语言学协会，意大利佛罗伦萨，3558-3567。 https://doi.org/10.18653/v1/P19-1346 [11] Michael Glass、Gaetano Rossiello、Md Faisal Mahbub Chowdhury、Ankita Naik、Pengshan Cai 和 Alfio Gliozzo。 2022.Re2G：检索、重新排序、生成。计算语言学协会北美分会 2022 年会议记录：人类语言技术，Marine Carpuat、Marie-Catherine de Marneffe 和 Ivan Vladimir Meza Ruiz（主编）。

### 段落 107 · Page 10

**EN**

Association for Computational Linguistics, Seattle, United States, 2701–2715. https://doi.org/ 10.18653/v1/2022.naacl-main.194 [12] Liangke Gui, Borui Wang, Qiuyuan Huang, Alexander Hauptmann, Yonatan Bisk, and Jianfeng Gao. 2022. KAT: A Knowledge Augmented Transformer for Visionand-Language. In Proceedings of the 2022 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies . Association for Computational Linguistics, Seattle, United States, 956–968.

**中文**

计算语言学协会，美国西雅图，2701-2715。 https://doi.org/10.18653/v1/2022.naacl-main.194 [12] 桂良科，王博瑞，黄秋媛，Alexander Hauptmann，Yonatan Bisk，高剑峰。 2022.KAT：视觉和语言的知识增强Transformer。计算语言学协会北美分会 2022 年会议记录：人类语言技术。计算语言学协会，美国西雅图，956–968。

### 段落 108 · Page 10

**EN**

https: //doi.org/10.18653/v1/2022.naacl-main.70 [13] Johannes Hoffart, Mohamed Amir Yosef, Ilaria Bordino, Hagen Fürstenau, Manfred Pinkal, Marc Spaniol, Bilyana Taneva, Stefan Thater, and Gerhard Weikum. 2011. Robust Disambiguation of Named Entities in Text. In Proceedings of the 2011 Conference on Empirical Methods in Natural Language Processing , Regina Barzilay and Mark Johnson (Eds.). Association for Computational Linguistics, Edinburgh, Scotland, UK., 782–792. https://aclanthology.org/D11-1072 [14] Gautier Izacard, Mathilde Caron, Lucas Hosseini, Sebastian Riedel, Piotr Bojanowski, Armand Joulin, and Edouard Grave. 2022.

**中文**

https://doi.org/10.18653/v1/2022.naacl-main.70 [13] Johannes Hoffart、Mohamed Amir Yosef、Ilaria Bordino、Hagen Fürstenau、Manfred Pinkal、Marc Spaniol、Bilyana Taneva、Stefan Thater 和 Gerhard Weikum。 2011.文本中命名实体的鲁棒消歧。 2011 年自然语言处理经验方法会议论文集，Regina Barzilay 和 Mark Johnson（主编）。计算语言学协会，英国苏格兰爱丁堡，782-792。 https://aclanthology.org/D11-1072 [14] Gautier Izacard、Mathilde Caron、Lucas Hosseini、Sebastian Riedel、Piotr Bojanowski、Armand Joulin 和 Edouard Grave。 2022 年。

### 段落 109 · Page 10

**EN**

Unsupervised Dense Information Retrieval with Contrastive Learning. Transactions on Machine Learning Research (2022). https://openreview.net/forum?id=jKN1pXi7b0 [15] Gautier Izacard and Edouard Grave. 2020. Distilling Knowledge from Reader to Retriever for Question Answering. https://arxiv.org/abs/2012.04584 [16] Gautier Izacard and Edouard Grave. 2021. Leveraging Passage Retrieval with Generative Models for Open Domain Question Answering. In Proceedings of the 16th Conference of the European Chapter of the Association for Computational Linguistics: Main Volume . Association for Computational Linguistics, Online, 874–880.

**中文**

通过对比学习进行无监督密集信息检索。机器学习研究汇刊 (2022)。 https://openreview.net/forum?id=jKN1pXi7b0 [15] Gautier Izacard 和 Edouard Grave。 2020。从读者那里提取知识以供检索器回答问题。 https://arxiv.org/abs/2012.04584 [16]戈蒂埃·伊扎卡尔和爱德华·格雷夫。 2021。利用段落检索和生成模型进行开放域问答。计算语言学协会欧洲分会第 16 届会议记录：主卷。计算语言学协会，在线，874–880。

### 段落 110 · Page 10

**EN**

https://doi.org/10.18653/v1/2021.eacl-main.74 [17] Gautier Izacard, Patrick Lewis, Maria Lomeli, Lucas Hosseini, Fabio Petroni, Timo Schick, Jane Dwivedi-Yu, Armand Joulin, Sebastian Riedel, and Edouard Grave. 2023. Atlas: Few-shot Learning with Retrieval Augmented Language Models. Journal of Machine Learning Research 24, 251 (2023), 1–43. http://jmlr.org/papers/ v24/23-0037.html [18] Albert Q.

**中文**

https://doi.org/10.18653/v1/2021.eacl-main.74 [17] Gautier Izacard、Patrick Lewis、Maria Lomeli、Lucas Hosseini、Fabio Petroni、Timo Schick、Jane Dwivedi-Yu、Armand Joulin、Sebastian Riedel 和 Edouard Grave。 2023. Atlas：利用检索增强语言模型进行小样本学习。机器学习研究杂志 24, 251 (2023), 1–43。 http://jmlr.org/papers/v24/23-0037.html [18] Albert Q.

### 段落 111 · Page 10

**EN**

Jiang, Alexandre Sablayrolles, Arthur Mensch, Chris Bamford, Devendra Singh Chaplot, Diego de las Casas, Florian Bressand, Gianna Lengyel, Guillaume Lample, Lucile Saulnier, Lélio Renard Lavaud, Marie-Anne Lachaux, Pierre Stock, Teven Le Scao, Thibaut Lavril, Thomas Wang, Timothée Lacroix, and William El Sayed. 2023. Mistral 7B. arXiv:2310.06825 [cs.CL] [19] Mandar Joshi, Eunsol Choi, Daniel Weld, and Luke Zettlemoyer. 2017. TriviaQA: A Large Scale Distantly Supervised Challenge Dataset for Reading Comprehension.

**中文**

Jiang、Alexandre Sablayrolles、Arthur Mensch、Chris Bamford、Devendra Singh Chaplot、Diego de las Casas、Florian Bressand、Gianna Lengyel、Guillaume Lample、Lucile Saulnier、Lélio Renard Lavaud、Marie-Anne Lachaux、Pierre Stock、Teven Le Scao、Thibaut Lavril、Thomas Wang、Timothée Lacroix 和 William El Sayed。 2023 年。米斯特拉尔 7B。 arXiv:2310.06825 [cs.CL] [19] Mandar Joshi、Eunsol Choi、Daniel Weld 和 Luke Zettlemoyer。 2017.TriviaQA：用于阅读理解的大规模远程监督挑战数据集。

### 段落 112 · Page 10

**EN**

In Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) , Regina Barzilay and Min-Yen Kan (Eds.). Association for Computational Linguistics, Vancouver, Canada, 1601–1611. https: //doi.org/10.18653/v1/P17-1147 [20] Vladimir Karpukhin, Barlas Oguz, Sewon Min, Patrick Lewis, Ledell Wu, Sergey Edunov, Danqi Chen, and Wen-tau Yih. 2020. Dense Passage Retrieval for Open- Domain Question Answering. In Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP) . Association for Computational Linguistics, Online, 6769–6781.

**中文**

计算语言学协会第 55 届年会记录（第一卷：长论文），Regina Barzilay 和 Min-Yen Kan（编辑）。计算语言学协会，加拿大温哥华，1601-1611 年。 https://doi.org/10.18653/v1/P17-1147 [20] Vladimir Karpukhin、Barlas Oguz、Sewon Min、Patrick Lewis、Ledell Wu、Sergey Edunov、Danqi Chen 和 Wen-tau Yih。 2020.用于开放域问答的密集段落检索。 2020 年自然语言处理经验方法 (EMNLP) 会议论文集。计算语言学协会，在线，6769–6781。

### 段落 113 · Page 10

**EN**

https://doi.org/10.18653/v1/2020.emnlp-main.550 [21] Diederik P. Kingma and Jimmy Ba. 2017. Adam: A Method for Stochastic Optimization. arXiv:1412.6980 [cs.LG] [22] Tom Kwiatkowski, Jennimaria Palomaki, Olivia Redfield, Michael Collins, Ankur Parikh, Chris Alberti, Danielle Epstein, Illia Polosukhin, Jacob Devlin, Kenton Lee, Kristina Toutanova, Llion Jones, Matthew Kelcey, Ming-Wei Chang, Andrew M. Dai, Jakob Uszkoreit, Quoc Le, and Slav Petrov. 2019. Natural Questions: A Benchmark for Question Answering Research. Transactions of the Association for Computational Linguistics 7 (2019), 452–466.

**中文**

https://doi.org/10.18653/v1/2020.emnlp-main.550 [21] Diederik P. Kingma 和 Jimmy Ba。 2017. Adam：一种随机优化方法。 arXiv:1412.6980 [cs.LG] [22] Tom Kwiatkowski、Jennimaria Palomaki、Olivia Redfield、Michael Collins、Ankur Parikh、Chris Alberti、Danielle Epstein、Illia Polosukhin、Jacob Devlin、Kenton Lee、Kristina Toutanova、Llion Jones、Matthew Kelcey、Ming-Wei Chang、Andrew M. Dai、Jakob乌什科雷特、库克·勒和斯拉夫·彼得罗夫。 2019。自然问题：问答研究的基准。计算语言学协会汇刊 7 (2019), 452–466。

### 段落 114 · Page 10

**EN**

https://doi.org/10.1162/tacl_a_00276 [23] Omer Levy, Minjoon Seo, Eunsol Choi, and Luke Zettlemoyer. 2017. Zero-Shot Relation Extraction via Reading Comprehension. In Proceedings of the 21st Conference on Computational Natural Language Learning (CoNLL 2017) , Roger Levy and Lucia Specia (Eds.). Association for Computational Linguistics, Vancouver, Canada, 333–342. https://doi.org/10.18653/v1/K17-1034 [24] Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Veselin Stoyanov, and Luke Zettlemoyer. 2020.

**中文**

https://doi.org/10.1162/tacl_a_00276 [23] Omer Levy、Minjoon Seo、Eunsol Choi 和 Luke Zettlemoyer。 2017.通过阅读理解进行零样本关系提取。在第 21 届计算自然语言学习会议 (CoNLL 2017) 的会议记录中，Roger Levy 和 Lucia Specia（编辑）。计算语言学协会，加拿大温哥华，333-342。 https://doi.org/10.18653/v1/K17-1034 [24] Mike Lewis、Yinhan Liu、Naman Goyal、Marjan Ghazvininejad、Abdelrahman Mohamed、Omer Levy、Veselin Stoyanov 和 Luke Zettlemoyer。 2020.

### 段落 115 · Page 10

**EN**

BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension. In Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics . Association for Computational Linguistics, Online, 7871–7880. https://doi.org/10.18653/v1/2020.acl-main.703 [25] Patrick Lewis, Ethan Perez, Aleksandra Piktus, Fabio Petroni, Vladimir Karpukhin, Naman Goyal, Heinrich Küttler, Mike Lewis, Wen-tau Yih, Tim Rocktäschel, Sebastian Riedel, and Douwe Kiela. 2020. Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks.

**中文**

BART：用于自然语言生成、翻译和理解的去噪序列到序列预训练。计算语言学协会第 58 届年会论文集。计算语言学协会，在线，7871–7880。 https://doi.org/10.18653/v1/2020.acl-main.703 [25] Patrick Lewis、Ethan Perez、Aleksandra Piktus、Fabio Petroni、Vladimir Karpukhin、Naman Goyal、Heinrich Küttler、Mike Lewis、Wen-tau Yih、Tim Rocktäschel、Sebastian Riedel 和 Douwe Kiela。 2020.知识密集型 NLP 任务的检索增强生成。

### 段落 116 · Page 10

**EN**

In Proceedings of the 34th International Conference on Neural Information Processing Systems (Vancouver, BC, Canada) (NIPS’20). Curran Associates Inc., Red Hook, NY, USA, Article 793, 16 pages. [26] Huayang Li, Yixuan Su, Deng Cai, Yan Wang, and Lemao Liu. 2022. A Survey on Retrieval-Augmented Text Generation. arXiv:2202.01110 [cs.CL] [27] Jimmy Lin, Xueguang Ma, Sheng-Chieh Lin, Jheng-Hong Yang, Ronak Pradeep, and Rodrigo Nogueira. 2021. Pyserini: A Python Toolkit for Reproducible Information Retrieval Research with Sparse and Dense Representations.

**中文**

第 34 届神经信息处理系统国际会议（加拿大不列颠哥伦比亚省温哥华）（NIPS’20）论文集。 Curran Associates Inc.，美国纽约州雷德胡克，第 793 条，16 页。 [26] 李华阳，苏逸轩，蔡邓，王岩，刘乐茂。 2022.检索增强文本生成调查。 arXiv:2202.01110 [cs.CL] [27] Jimmy Lin、Xueguang Ma、Sheng-Chieh Lin、Jheng-Hong Yang、Ronak Pradeep 和 Rodrigo Nogueira。 2021. Pyserini：用于具有稀疏和密集表示的可重复信息检索研究的 Python 工具包。

### 段落 117 · Page 10

**EN**

In Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval (, Virtual Event, Canada,) (SIGIR ’21). Association for Computing Machinery, New York, NY, USA, 2356–2362. https: //doi.org/10.1145/3404835.3463238 [28] Bryan McCann, Nitish Shirish Keskar, Caiming Xiong, and Richard Socher. 2019. The Natural Language Decathlon: Multitask Learning as Question Answering.

**中文**

第 44 届国际 ACM SIGIR 信息检索研究与开发会议论文集（虚拟活动，加拿大）（SIGIR '21）。计算机协会，美国纽约州纽约市，2356–2362。 https://doi.org/10.1145/3404835.3463238 [28] Bryan McCann、Nitish Shirish Keskar、Caiming Xiong 和 Richard Socher。 2019。自然语言十项全能：多任务学习作为问答。

### 段落 118 · Page 10

**EN**

https://openreview.net/forum?id=B1lfHhR9tm [29] Reiichiro Nakano, Jacob Hilton, Suchir Balaji, Jeff Wu, Long Ouyang, Christina Kim, Christopher Hesse, Shantanu Jain, Vineet Kosaraju, William Saunders, Xu Jiang, Karl Cobbe, Tyna Eloundou, Gretchen Krueger, Kevin Button, Matthew Knight, Benjamin Chess, and John Schulman. 2022. WebGPT: Browser-assisted question-answering with human feedback. arXiv:2112.09332 [cs.CL] [30] Rodrigo Nogueira and Kyunghyun Cho. 2020. Passage Re-ranking with BERT.

**中文**

https://openreview.net/forum?id=B1lfHhR9tm [29] Reiichiro Nakano、Jacob Hilton、Suchir Balaji、Jeff Wu、Long Ouyang、Christina Kim、Christopher Hesse、Shantanu Jain、Vineet Kosaraju、William Saunders、徐江、Karl Cobbe、Tyna Eloundou、Gretchen Krueger、Kevin Button、Matthew Knight、Benjamin Chess 和 John舒尔曼。 2022.WebGPT：浏览器辅助问答与人工反馈。 arXiv:2112.09332 [cs.CL] [30] 罗德里戈·诺盖拉 (Rodrigo Nogueira) 和 Kyunghyun Cho。 2020. 使用 BERT 进行段落重排。

### 段落 119 · Page 10

**EN**

arXiv:1901.04085 [cs.IR] [31] Fabio Petroni, Aleksandra Piktus, Angela Fan, Patrick Lewis, Majid Yazdani, Nicola De Cao, James Thorne, Yacine Jernite, Vladimir Karpukhin, Jean Maillard, Vassilis Plachouras, Tim Rocktäschel, and Sebastian Riedel. 2021. KILT: a Benchmark for Knowledge Intensive Language Tasks. In Proceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies . Association for Computational Linguistics, Online, 2523–2544.

**中文**

arXiv:1901.04085 [cs.IR] [31] Fabio Petroni、Aleksandra Piktus、Angela Fan、Patrick Lewis、Majid Yazdani、Nicola De Cao、James Thorne、Yacine Jernite、Vladimir Karpukhin、Jean Maillard、Vassilis Plachouras、Tim Rocktäschel 和 Sebastian Riedel。 2021.KILT：知识密集型语言任务的基准。计算语言学协会北美分会 2021 年会议记录：人类语言技术。计算语言学协会，在线，2523–2544。

### 段落 120 · Page 10

**EN**

https://doi.org/10.18653/v1/2021.naacl-main.200 [32] Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, and Peter J. Liu. 2020. Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer.J. Mach.

**中文**

https://doi.org/10.18653/v1/2021.naacl-main.200 [32] Colin Raffel、Noam Shazeer、Adam Roberts、Katherine Lee、Sharan Narang、Michael Matena、Yanqi Zhou、Wei Li 和 Peter J. Liu。 2020。用统一的文本到文本转换器探索迁移学习的局限性。J。马赫。

### Page 11

### 段落 121 · Page 11

**EN**

Towards a Search Engine for Machines: Unified Ranking for Multiple Retrieval-Augmented Large Language Models SIGIR ’24, July 14–18, 2024, Washington, DC, USA Learn. Res. 21, 1, Article 140 (jan 2020), 67 pages. [33] Pranav Rajpurkar, Jian Zhang, Konstantin Lopyrev, and Percy Liang. 2016. SQuAD: 100,000+ Questions for Machine Comprehension of Text. In Proceedings of the 2016 Conference on Empirical Methods in Natural Language Processing. Association for Computational Linguistics, Austin, Texas, 2383–2392. https://doi.org/10.18653/v1/D16-1264 [34] Stephen E. Robertson, Steve Walker, Susan Jones, Micheline Hancock-Beaulieu, and Mike Gatford.

**中文**

迈向机器搜索引擎：多种检索增强大型语言模型的统一排名 SIGIR ’24，2024 年 7 月 14 日至 18 日，美国华盛顿特区学习。资源。 21, 1，第 140 条（2020 年 1 月），67 页。 [33] Pranav Rajpurkar，张健，康斯坦丁·洛佩列夫，珀西·梁。 2016.SQuAD：100,000 多个机器理解文本的问题。 2016 年自然语言处理经验方法会议论文集。计算语言学协会，德克萨斯州奥斯汀，2383-2392。 https://doi.org/10.18653/v1/D16-1264 [34] 斯蒂芬·E·罗伯逊、史蒂夫·沃克、苏珊·琼斯、米什琳·汉考克-博利厄和迈克·盖特福德。

### 段落 122 · Page 11

**EN**

1994. Okapi at TREC-3. In Text Retrieval Conference. https: //api.semanticscholar.org/CorpusID:3946054 [35] Devendra Sachan, Mostofa Patwary, Mohammad Shoeybi, Neel Kant, Wei Ping, William L. Hamilton, and Bryan Catanzaro. 2021. End-to-End Training of Neural Retrievers for Open-Domain Question Answering. In Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (Volume 1: Long Papers). Association for Computational Linguistics, Online, 6648–6662.

**中文**

1994 年。霍加狓在 TREC-3。在文本检索会议中。 https://api.semanticscholar.org/CorpusID:3946054 [35] Devendra Sachan、Mostofa Patwary、Mohammad Shoeybi、Neel Kant、Wei Ping、William L. Hamilton 和 Bryan Catanzaro。 2021。开放域问答神经检索器的端到端训练。计算语言学协会第 59 届年会暨第 11 届自然语言处理国际联合会议论文集（第一卷：长论文）。计算语言学协会，在线，6648–6662。

### 段落 123 · Page 11

**EN**

https: //doi.org/10.18653/v1/2021.acl-long.519 [36] Alireza Salemi, Juan Altmayer Pizzorno, and Hamed Zamani. 2023. A Symmetric Dual Encoding Dense Retrieval Framework for Knowledge-Intensive Visual Question Answering. In Proceedings of the 46th International ACM SI- GIR Conference on Research and Development in Information Retrieval (<confloc>, <city>Taipei</city>, <country>Taiwan</country>, </conf-loc>) (SIGIR ’23). Association for Computing Machinery, New York, NY, USA, 110–120. https://doi.org/10.1145/3539618.3591629 [37] Alireza Salemi, Surya Kallumadi, and Hamed Zamani. 2024.

**中文**

https://doi.org/10.18653/v1/2021.acl-long.519 [36] Alireza Salemi、Juan Altmayer Pizzorno 和 Hamed Zamani。 2023. 用于知识密集型视觉问答的对称双编码密集检索框架。第 46 届国际 ACM SIGIR 信息检索研究与开发会议论文集（<confloc>、<city>Taipei</city>、<country>Taiwan</country>、</conf-loc>）（SIGIR '23）。计算机协会，美国纽约州纽约市，110–120。 https://doi.org/10.1145/3539618.3591629 [37] Alireza Salemi、Surya Kallumadi 和 Hamed Zamani。 2024 年。

### 段落 124 · Page 11

**EN**

Optimization Methods for Personalizing Large Language Models through Retrieval Augmentation. In Proceedings of the 47th Annual International ACM SIGIR Conference on Research and Development in Information Retrieval (Washington, DC, USA) (SIGIR ’24). (to appear). [38] Alireza Salemi, Sheshera Mysore, Michael Bendersky, and Hamed Zamani. 2024. LaMP: When Large Language Models Meet Personalization. arXiv:2304.11406 [cs.CL] [39] Alireza Salemi, Mahta Rafiee, and Hamed Zamani. 2023. Pre-Training Multi- Modal Dense Retrievers for Outside-Knowledge Visual Question Answering. arXiv:2306.16478 [cs.IR] [40] Alireza Salemi and Hamed Zamani. 2024.

**中文**

通过检索增强个性化大型语言模型的优化方法。第 47 届国际 ACM SIGIR 信息检索研究与开发年度会议（美国华盛顿）（SIGIR '24）论文集。 （出现）。 [38] Alireza Salemi、Sheshera Mysore、Michael Bendersky 和 ​​Hamed Zamani。 2024. LaMP：当大型语言模型遇到个性化时。 arXiv:2304.11406 [cs.CL] [39] Alireza Salemi、Mahta Rafiee 和 Hamed Zamani。 2023.用于外部知识视觉问答的多模态密集检索器的预训练。 arXiv:2306.16478 [cs.IR] [40] Alireza Salemi 和 Hamed Zamani。 2024 年。

### 段落 125 · Page 11

**EN**

Evaluating Retrieval Quality in Retrieval-Augmented Generation. In Proceedings of the 47th Annual International ACM SIGIR Conference on Research and Development in Information Retrieval (Washington, DC, USA) (SIGIR ’24). (to appear). [41] Keshav Santhanam, Omar Khattab, Jon Saad-Falcon, Christopher Potts, and Matei Zaharia. 2022. ColBERTv2: Effective and Efficient Retrieval via Lightweight Late Interaction. In Proceedings of the 2022 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies . Association for Computational Linguistics, Seattle, United States, 3715–3734.

**中文**

评估检索增强生成中的检索质量。第 47 届国际 ACM SIGIR 信息检索研究与开发年度会议（美国华盛顿）（SIGIR '24）论文集。 （出现）。 [41] Keshav Santhanam、Omar Khattab、Jon Saad-Falcon、Christopher Potts 和 Matei Zaharia。 2022. ColBERTv2：通过轻量级后期交互进行有效且高效的检索。计算语言学协会北美分会 2022 年会议记录：人类语言技术。计算语言学协会，美国西雅图，3715–3734。

### 段落 126 · Page 11

**EN**

https://doi.org/10.18653/v1/2022.naacl-main.272 [42] Xuehua Shen, Bin Tan, and ChengXiang Zhai. 2005. Context-sensitive information retrieval using implicit feedback. In Proceedings of the 28th Annual International ACM SIGIR Conference on Research and Development in Information Retrieval (Salvador, Brazil) (SIGIR ’05). Association for Computing Machinery, New York, NY, USA, 43–50. https://doi.org/10.1145/1076034.1076045 [43] Kurt Shuster, Spencer Poff, Moya Chen, Douwe Kiela, and Jason Weston. 2021. Retrieval Augmentation Reduces Hallucination in Conversation. In Findings of the Association for Computational Linguistics: EMNLP 2021 .

**中文**

https://doi.org/10.18653/v1/2022.naacl-main.272 [42] 沉雪华，谭斌，翟成祥。 2005。使用隐式反馈的上下文相关信息检索。第 28 届国际 ACM SIGIR 信息检索研究与开发年度会议（巴西萨尔瓦多）（SIGIR '05）论文集。计算机协会，美国纽约州纽约市，43-50。 https://doi.org/10.1145/1076034.1076045 [43] Kurt Shuster、Spencer Poff、Moya Chen、Douwe Kiela 和 Jason Weston。 2021.检索增强减少对话中的幻觉。计算语言学协会的调查结果：EMNLP 2021。

### 段落 127 · Page 11

**EN**

Association for Computational Linguistics, Punta Cana, Dominican Republic, 3784–3803. https: //doi.org/10.18653/v1/2021.findings-emnlp.320 [44] Shamane Siriwardhana, Rivindu Weerasekera, Elliott Wen, Tharindu Kaluarachchi, Rajib Rana, and Suranga Nanayakkara. 2023. Improving the Domain Adaptation of Retrieval Augmented Generation (RAG) Models for Open Domain Question Answering. Transactions of the Association for Computational Linguistics 11 (2023), 1–17. https://doi.org/10.1162/tacl_a_00530 [45] Yiping Song, Cheng-Te Li, Jian-Yun Nie, Ming Zhang, Dongyan Zhao, and Rui Yan. 2018.

**中文**

计算语言学协会，多米尼加共和国蓬塔卡纳，3784-3803。 https://doi.org/10.18653/v1/2021.findings-emnlp.320 [44] Shamane Siriwardhana、Rivindu Weerasekera、Elliott Wen、Tharindu Kaluarachchi、R​​ajib Rana 和 Suranga Nanayakkara。 2023。改进开放域问答的检索增强生成（RAG）模型的域适应。计算语言学协会汇刊 11 (2023), 1–17。 https://doi.org/10.1162/tacl_a_00530 [45]宋一平，李成特，聂建云，张明，赵东艳，严锐。 2018.

### 段落 128 · Page 11

**EN**

An Ensemble of Retrieval-Based and Generation-Based Human-Computer Conversation Systems. In Proceedings of the Twenty-Seventh International Joint Conference on Artificial Intelligence, IJCAI-18. International Joint Conferences on Artificial Intelligence Organization, 4382–4388. https://doi.org/10.24963/ijcai. 2018/609 [46] James Thorne, Andreas Vlachos, Christos Christodoulopoulos, and Arpit Mittal. 2018. FEVER: a Large-scale Dataset for Fact Extraction and VERification. In Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers).

**中文**

基于检索和基于生成的人机对话系统的集合。第二十七届国际人工智能联合会议论文集，IJCAI-18。人工智能组织国际联合会议，4382–4388。 https://doi.org/10.24963/ijcai。 2018/609 [46] 詹姆斯·索恩、安德烈亚斯·弗拉科斯、克里斯托斯·克里斯托杜洛普洛斯和阿尔皮特·米塔尔。 2018。FEVER：用于事实提取和验证的大规模数据集。计算语言学协会北美分会 2018 年会议记录：人类语言技术，第 1 卷（长论文）。

### 段落 129 · Page 11

**EN**

Association for Computational Linguistics, New Orleans, Louisiana, 809–819. https://doi.org/10.18653/v1/N18-1074 [47] Hugo Touvron et al . 2023. Llama 2: Open Foundation and Fine-Tuned Chat Models. arXiv:2307.09288 [cs.CL] [48] Karthik Valmeekam, Matthew Marquez, Sarath Sreedharan, and Subbarao Kambhampati. 2023. On the Planning Abilities of Large Language Models - A Critical Investigation. arXiv 2305.15771 (2023). [49] Tu Vu, Mohit Iyyer, Xuezhi Wang, Noah Constant, Jerry Wei, Jason Wei, Chris Tar, Yun-Hsuan Sung, Denny Zhou, Quoc Le, and Thang Luong. 2023. FreshLLMs: Refreshing Large Language Models with Search Engine Augmentation.

**中文**

计算语言学协会，路易斯安那州新奥尔良，809-819。 https://doi.org/10.18653/v1/N18-1074 [47] Hugo Touvron 等人。 2023. Llama 2：开放基础和微调聊天模型。 arXiv:2307.09288 [cs.CL] [48] Karthik Valmeekam、Matthew Marquez、Sarath Sreedharan 和 Subbarao Kambhampati。 2023.关于大型语言模型的规划能力——一项批判性调查。 arXiv 2305.15771 (2023)。 [49] Tu Vu、Mohit Iyyer、Xuezhi Wang、Noah Constant、Jerry Wei、Jason Wei、Chris Tar、Yun-Hsuan Sung、Denny Zhou、Quoc Le 和 Thang Luong。 2023.FreshLLM：通过搜索引擎增强刷新大型语言模型。

### 段落 130 · Page 11

**EN**

In arXiv. [50] Alex Wang, Yada Pruksachatkun, Nikita Nangia, Amanpreet Singh, Julian Michael, Felix Hill, Omer Levy, and Samuel R. Bowman. 2019.SuperGLUE: a stickier benchmark for general-purpose language understanding systems . Curran Associates Inc., Red Hook, NY, USA. [51] Alex Wang, Amanpreet Singh, Julian Michael, Felix Hill, Omer Levy, and Samuel Bowman. 2018. GLUE: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding. In Proceedings of the 2018 EMNLP Workshop BlackboxNLP: Analyzing and Interpreting Neural Networks for NLP . Association for Computational Linguistics, Brussels, Belgium, 353–355.

**中文**

在 arXiv 中。 [50] Alex Wang、Yada Pruksachatkun、Nikita Nangia、Amanpreet Singh、Julian Michael、Felix Hill、Omer Levy 和 Samuel R. Bowman。 2019.SuperGLUE：通用语言理解系统的更具粘性的基准。 Curran Associates Inc.，美国纽约州雷德胡克。 [51] Alex Wang、Amanpreet Singh、Julian Michael、Felix Hill、Omer Levy 和 Samuel Bowman。 2018. GLUE：自然语言理解的多任务基准和分析平台。 2018 年 EMNLP 研讨会 BlackboxNLP 论文集：分析和解释 NLP 神经网络。计算语言学协会，比利时布鲁塞尔，353-355。

### 段落 131 · Page 11

**EN**

https://doi.org/10. 18653/v1/W18-5446 [52] Dingmin Wang, Qiuyuan Huang, Matthew Jackson, and Jianfeng Gao. 2023. NLP Agent - Retrieve What You Need: A Mutual Learning Framework for Open-domain Question Answering. Proceedings of Transactions of the Association for Computational Linguistics (TACL) (May 2023). https://www.microsoft.com/en-us/research/publication/retrieve-what-youneed-a-mutual-learning-framework-for-open-domain-question-answering/ [53] Jason Weston, Emily Dinan, and Alexander Miller. 2018. Retrieve and Refine: Improved Sequence Generation Models For Dialogue.

**中文**

https://doi.org/10。 18653/v1/W18-5446 [52] 王鼎民，黄秋园，马修·杰克逊，高剑峰。 2023. NLP 代理 - 检索您需要的内容：开放域问答的相互学习框架。计算语言学协会 (TACL) 交易记录（2023 年 5 月）。 https://www.microsoft.com/en-us/research/publication/retrieve-what-youneed-a-mutual-learning-framework-for-open-domain-question-answering/ [53] 杰森·韦斯顿、艾米丽·迪南和亚历山大·米勒。 2018。检索和细化：改进的对话序列生成模型。

### 段落 132 · Page 11

**EN**

In Proceedings of the 2018 EMNLP Workshop SCAI: The 2nd International Workshop on Search-Oriented Conversational AI. Association for Computational Linguistics, Brussels, Belgium, 87–92. https://doi.org/10.18653/v1/W18-5713 [54] Sohee Yang and Minjoon Seo. 2020. Is Retriever Merely an Approximator of Reader? arXiv:2010.10999 [cs.CL] [55] Zhilin Yang, Peng Qi, Saizheng Zhang, Yoshua Bengio, William Cohen, Ruslan Salakhutdinov, and Christopher D. Manning. 2018. HotpotQA: A Dataset for Diverse, Explainable Multi-hop Question Answering.

**中文**

2018 年 EMNLP 研讨会 SCAI 论文集：第二届面向搜索的对话式人工智能国际研讨会。计算语言学协会，比利时布鲁塞尔，87-92。 https://doi.org/10.18653/v1/W18-5713 [54] Sohee Yang 和 Minjoon Seo。 2020. Retriever 仅仅是 Reader 的近似器吗？ arXiv:2010.10999 [cs.CL] [55] 杨志林、齐鹏、张赛正、Yoshua Bengio、William Cohen、Ruslan Salakhutdinov 和 Christopher D. Manning。 2018.HotpotQA：多样化、可解释的多跳问答数据集。

### 段落 133 · Page 11

**EN**

In Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing , Ellen Riloff, David Chiang, Julia Hockenmaier, and Jun’ichi Tsujii (Eds.). Association for Computational Linguistics, Brussels, Belgium, 2369–2380. https://doi.org/10. 18653/v1/D18-1259 [56] Hamed Zamani and Michael Bendersky. 2024. Stochastic RAG: End-to-End Retrieval-Augmented Generation through Expected Utility Maximization. In Proceedings of the 47th Annual International ACM SIGIR Conference on Research and Development in Information Retrieval (Washington, DC, USA) (SIGIR ’24). (to appear).

**中文**

2018 年自然语言处理经验方法会议论文集，Ellen Riloff、David Jiang、Julia Hockenmaier 和 Jun’ichi Tsujii（编辑）。计算语言学协会，比利时布鲁塞尔，2369-2380。 https://doi.org/10。 18653/v1/D18-1259 [56] 哈米德·扎马尼和迈克尔·本德斯基。 2024.随机 RAG：通过预期效用最大化实现端到端检索增强生成。第 47 届国际 ACM SIGIR 信息检索研究与开发年度会议（美国华盛顿）（SIGIR '24）论文集。 （出现）。

### 段落 134 · Page 11

**EN**

[57] Hamed Zamani, Fernando Diaz, Mostafa Dehghani, Donald Metzler, and Michael Bendersky. 2022. Retrieval-Enhanced Machine Learning. InProceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval (, Madrid, Spain,) (SIGIR ’22). Association for Computing Machinery, New York, NY, USA, 2875–2886. https://doi.org/10.1145/3477495.3531722 [58] Jingqing Zhang, Yao Zhao, Mohammad Saleh, and Peter J. Liu. 2020. PEGASUS: Pre-Training with Extracted Gap-Sentences for Abstractive Summarization. In Proceedings of the 37th International Conference on Machine Learning (ICML’20) .

**中文**

[57] Hamed Zamani、Fernando Diaz、Mostafa Dehghani、Donald Metzler 和 Michael Bendersky。 2022。检索增强机器学习。第 45 届国际 ACM SIGIR 信息检索研究与开发会议论文集（西班牙马德里）（SIGIR '22）。计算机协会，美国纽约州纽约市，2875–2886。 https://doi.org/10.1145/3477495.3531722 [58] 张景清，赵耀，穆罕默德·萨利赫，彼得·J·刘。 2020. PEGASUS：使用提取的间隙句进行抽象总结的预训练。第 37 届国际机器学习会议 (ICML’20) 论文集。

### 段落 135 · Page 11

**EN**

JMLR.org, Article 1051, 12 pages. [59] Wayne Xin Zhao, Kun Zhou, Junyi Li, Tianyi Tang, Xiaolei Wang, Yupeng Hou, Yingqian Min, Beichen Zhang, Junjie Zhang, Zican Dong, Yifan Du, Chen Yang, Yushuo Chen, Zhipeng Chen, Jinhao Jiang, Ruiyang Ren, Yifan Li, Xinyu Tang, Zikang Liu, Peiyu Liu, Jian-Yun Nie, and Ji-Rong Wen. 2023. A Survey of Large Language Models. arXiv:2303.18223 [cs.CL] [60] Fengbin Zhu, Wenqiang Lei, Chao Wang, Jianming Zheng, Soujanya Poria, and Tat-Seng Chua. 2021. Retrieving and Reading: A Comprehensive Survey on Open-domain Question Answering. arXiv:2101.00774 [cs.AI]

**中文**

JMLR.org，第 1051 条，12 页。 [59] 赵鑫、周昆、李俊毅、唐天一、王小雷、侯宇鹏、民英前、张北辰、张俊杰、董子灿、杜一凡、陈阳、陈玉硕、陈志鹏、蒋金浩、任瑞阳、李一凡、唐新宇、刘子康、刘佩玉、聂建云、温继荣。 2023.大型语言模型调查。 arXiv:2303.18223 [cs.CL] [60] Fengbin Zhu、Wenqiang Lei、Chao Wang、Jianming Cheng、Soujanya Poria 和 Tat-Seng Chua。 2021.检索与阅读：开放域问答综合调查。 arXiv:2101.00774 [cs.AI]
