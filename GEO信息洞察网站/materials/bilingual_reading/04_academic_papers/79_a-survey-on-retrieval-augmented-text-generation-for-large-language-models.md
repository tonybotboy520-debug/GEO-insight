# A Survey on Retrieval-Augmented Text Generation for Large Language Models

- ID: 79
- 类型: pdf
- 分类: 04_academic_papers
- 主题: RAG survey
- 原文链接: https://arxiv.org/pdf/2404.10981
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models YIZHENG HUANG and JIMMY X. HUANG, York University, Canada Retrieval-Augmented Generation (RAG) merges retrieval methods with deep learning advancements to address the static limitations of large language models (LLMs) by enabling the dynamic integration of up-to-date external information. This methodology, focusing primarily on the text domain, provides a cost-effective solution to the generation of plausible but possibly incorrect responses by LLMs, thereby enhancing the accuracy and reliability of their outputs through the use of real-world data.

**中文**

大型语言模型中的检索增强文本生成调查 加拿大约克大学的 YIZHENG HUANG 和 JIMMY X. HUANG 检索增强生成 (RAG) 将检索方法与深度学习进步相结合，通过动态集成最新外部信息来解决大型语言模型 (LLM) 的静态限制。这种方法主要关注文本领域，为法学硕士生成看似合理但可能不正确的答案提供了一种经济高效的解决方案，从而通过使用真实世界的数据来提高其输出的准确性和可靠性。

### 段落 2 · Page 1

**EN**

As RAG grows in complexity and incorporates multiple concepts that can influence its performance, this paper organizes the RAG paradigm into four categories: pre-retrieval, retrieval, post-retrieval, and generation, offering a detailed perspective from the retrieval viewpoint. It outlines RAG’s mechanics and discusses the field’s progression through the analysis of significant studies. Additionally, the paper introduces evaluation methods for RAG, addressing the challenges faced and proposing future research directions.

**中文**

随着 RAG 变得越来越复杂，并融入了多种影响其性能的概念，本文将 RAG 范式分为四类：检索前、检索、检索后和生成，从检索的角度提供了详细的视角。它概述了 RAG 的机制，并通过对重要研究的分析讨论了该领域的进展。此外，本文还介绍了 RAG 的评估方法，解决了其面临的挑战并提出了未来的研究方向。

### 段落 3 · Page 1

**EN**

By offering an organized framework and categorization, the study aims to consolidate existing research on RAG, clarify its technological underpinnings, and highlight its potential to broaden the adaptability and applications of LLMs. CCS Concepts: •Computing methodologies → Natural language generation; •Information systems → Information retrieval. Additional Key Words and Phrases: retrieval-augmented generation, information retrieval, large language model ACM Reference Format: Yizheng Huang and Jimmy X. Huang. 2018. The Survey of Retrieval-Augmented Text Generation in Large Language Models.

**中文**

通过提供一个有组织的框架和分类，该研究旨在巩固 RAG 的现有研究，阐明其技术基础，并强调其扩大法学硕士适应性和应用的潜力。 CCS概念： •计算方法→自然语言生成； •信息系统→信息检索。其他关键词和短语：检索增强生成、信息检索、大语言模型 ACM 参考格式：Yizheng Huang 和 Jimmy X. Huang。 2018.大型语言模型中检索增强文本生成的调查。

### 段落 4 · Page 1

**EN**

In Proceedings of Make sure to enter the correct conference title from your rights confirmation emai (Conference acronym ’XX). ACM, New York, NY, USA, 37 pages. https://doi.org/XXXXXXX.XXXXXXX 1 Introduction The advent of ChatGPT has significantly impacted both academia and industry due to its interactive capabilities and widespread application, establishing itself as a leading artificial intelligence tool [55, 60, 77].

**中文**

在会议记录中，请确保从您的权利确认 emai（会议缩写“XX”）中输入正确的会议标题。 ACM，美国纽约州纽约市，37 页。 https://doi.org/XXXXXXX.XXXXXXX 1 简介 ChatGPT 的出现因其交互能力和广泛的应用而对学术界和工业界产生了重大影响，使其成为领先的人工智能工具[55,60,77]。

### 段落 5 · Page 1

**EN**

At the core of ChatGPT is the large language model (LLM) GPT-4, as detailed by [1], which has seen numerous enhancements to its predecessors, showcasing exceptional abilities in a variety of Natural Language Processing (NLP) tasks [ 78]. Despite these advancements, the adoption of LLMs has highlighted several critical issues primarily due to their reliance on extensive datasets. This reliance restricts their ability to incorporate new information post-training, leading to three primary challenges. First, the focus on broad and general data to maximize accessibility and applicability results in subpar performance in specialized areas.

**中文**

ChatGPT 的核心是大语言模型 (LLM) GPT-4，如 [1] 所详述，它对其前身进行了许多增强，在各种自然语言处理 (NLP) 任务中展示了卓越的能力 [78]。尽管取得了这些进步，但法学硕士的采用凸显了几个关键问题，这主要是由于它们对广泛数据集的依赖。这种依赖限制了他们在培训后吸收新信息的能力，导致了三个主要挑战。首先，注重广泛和一般数据以最大限度地提高可访问性和适用性会导致专业领域的绩效不佳。

### 段落 6 · Page 1

**EN**

Second, the rapid creation of online data, combined with the significant resources required for data annotation and model training, Authors’ Contact Information: Yizheng Huang, hyz@yorku.ca; Jimmy X. Huang, jhuang@yorku.ca, York University, Toronto, Ontario, Canada. Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. Copyrights for components of this work owned by others than the author(s) must be honored.

**中文**

其次，在线数据的快速创建，结合数据标注和模型训练所需的大量资源，作者联系方式：Yizheng Huang，hyz@yorku.ca； Jimmy X. Huang，jhuang@yorku.ca，约克大学，加拿大安大略省多伦多市。允许免费制作本作品全部或部分内容的数字或硬拷贝以供个人或课堂使用，前提是制作或分发副本不是为了盈利或商业利益，并且副本在首页上附有此通知和完整引用。必须尊重作者以外的其他人拥有的本作品组件的版权。

### 段落 7 · Page 1

**EN**

Abstracting with credit is permitted. To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee. Request permissions from permissions@acm.org. Conference acronym ’XX, June 03–05, 2018, Woodstock, NY © 2018 Copyright held by the owner/author(s). Publication rights licensed to ACM. ACM ISBN 978-1-4503-XXXX-X/18/06 https://doi.org/XXXXXXX.XXXXXXX , Vol. 1, No. 1, Article . Publication date: August 2018. arXiv:2404.10981v2 [cs.IR] 23 Aug 2024

**中文**

允许以信用方式提取。要以其他方式复制、重新发布、发布到服务器上或重新分发到列表，需要事先获得特定许可和/或付费。从permissions@acm.org 请求权限。会议缩写‘XX，2018 年 6 月 3 日至 5 日，纽约州伍德斯托克 © 2018 版权归所有者/作者所有。出版权授权给 ACM。 ACM ISBN 978-1-4503-XXXX-X/18/06 https://doi.org/XXXXXXX.XXXXXXX，卷。 1、第1条。发布日期：2018 年 8 月。arXiv:2404.10981v2 [cs.IR] 2024 年 8 月 23 日

### Page 2

### 段落 8 · Page 2

**EN**

2 Huang et al. Fig. 1. An example of RAG benefits ChatGPT resolves questions that cannot be answered beyond the scope of the training data and generates correct results. hinders LLMs’ ability to stay updated. Third, LLMs are susceptible to generating convincing yet inaccurate responses, known as “hallucinations”, which can mislead users. Addressing these challenges is crucial for LLMs to be effectively utilized across various domains.

**中文**

2 黄等人。图 1. RAG 优势示例 ChatGPT 解决了训练数据范围之外无法回答的问题，并生成正确的结果。阻碍了法学硕士保持更新的能力。第三，法学硕士很容易产生令人信服但不准确的反应，称为“幻觉”，这可能会误导用户。解决这些挑战对于法学硕士在各个领域的有效利用至关重要。

### 段落 9 · Page 2

**EN**

A promising solution is the integration of Retrieval-Augmented Generation (RAG) technology, which supplements models by fetching external data in response to queries, thus ensuring more accurate and current outputs. Figure 1 illustrates how RAG can enable ChatGPT to provide precise answers beyond its initial training data. Since its introduction by Lewis et al. [83] in 2020, RAG has seen rapid development, especially with the rise of models like ChatGPT.

**中文**

一个有前途的解决方案是集成检索增强生成（RAG）技术，该技术通过获取外部数据来响应查询来补充模型，从而确保更准确和最新的输出。图 1 说明了 RAG 如何使 ChatGPT 能够提供超出其初始训练数据的精确答案。自从 Lewis 等人提出以来。 [83] 2020年，RAG得到了快速发展，特别是随着ChatGPT等模型的兴起。

### 段落 10 · Page 2

**EN**

Despite these advancements, there remains a noticeable gap in the literature regarding a comprehensive analysis of the mechanisms underlying RAG and the progress achieved by subsequent studies. Moreover, the field suffers from fragmented research focuses and inconsistent terminology for similar methods, leading to confusion. This survey seeks to bridge this gap by offering a structured overview of RAG, categorizing various approaches, and providing an in-depth understanding of the current research landscape, with a focus on textual applications given their prominence in recent research.

**中文**

尽管取得了这些进展，但在对 RAG 机制的综合分析以及后续研究取得的进展方面，文献中仍然存在明显的差距。此外，该领域的研究重点分散，类似方法的术语不一致，导致混乱。本调查旨在通过提供 RAG 的结构化概述、对各种方法进行分类以及对当前研究领域的深入了解来弥合这一差距，并重点关注文本应用，因为它们在最近的研究中占据突出地位。

### 段落 11 · Page 2

**EN**

To provide clarity and structure, this paper is organized as follows: Section 2 outlines the overall RAG workflow, dividing the methodologies into pre-retrieval, retrieval, post-retrieval, and generation phases. Sections 3 through 6 explore the core techniques within each phase. Section 7 focuses on the evaluation methodologies for RAG. Section 8 summarizes the reviewed studies, detailing the retrievers and generators used, while Section 9 discusses challenges and future research directions, extending beyond text-based studies to include multimodal data applications. The paper concludes with Section 10.

**中文**

为了提供清晰度和结构，本文的组织如下：第 2 节概述了整个 RAG 工作流程，将方法分为检索前、检索、检索后和生成阶段。第 3 节到第 6 节探讨了每个阶段的核心技术。第 7 节重点介绍 RAG 的评估方法。第 8 节总结了回顾的研究，详细介绍了所使用的检索器和生成器，而第 9 节讨论了挑战和未来的研究方向，超越基于文本的研究，包括多模式数据应用。本文以第 10 节结束。

### 段落 12 · Page 2

**EN**

Other related surveys provide valuable insights into the evolving RAG landscape from different angles. Gao et al. [38] identified three key stages in RAG development: pre-training enhancement, inference, and fine-tuning. Zhao et al. [162] focused on the diverse applications of RAG, including text, code, image, and video generation, emphasizing augmented intelligence in generative tasks. Meanwhile, Hu et al. [48] explored Retrieval-Augmented Language Models (RALMs), examining how interactions between retrievers, language models, and augmentations influence model architectures and applications.

**中文**

其他相关调查从不同角度提供了对不断发展的 RAG 格局的宝贵见解。高等人。 [38]确定了 RAG 开发的三个关键阶段：预训练增强、推理和微调。赵等人。 [162]专注于 RAG 的多种应用，包括文本、代码、图像和视频生成，强调生成任务中的增强智能。与此同时，胡等人。 [48] 探索了检索增强语言模型（RALM），研究了检索器、语言模型和增强之间的交互如何影响模型架构和应用程序。

### 段落 13 · Page 2

**EN**

In this paper, we aim to offer a comprehensive and unified framework for understanding RAG from an information retrieval (IR) perspective, identifying key challenges and areas for improvement. We delve into the core technologies that drive RAG, assessing their effectiveness in addressing retrieval and generation tasks. Additionally, this survey introduces the evaluation methods employed in RAG research, highlights current limitations, and proposes promising avenues for future exploration. , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

在本文中，我们的目标是提供一个全面、统一的框架，从信息检索 (IR) 的角度理解 RAG，确定关键挑战和需要改进的领域。我们深入研究驱动 RAG 的核心技术，评估它们在解决检索和生成任务方面的有效性。此外，本次调查介绍了 RAG 研究中采用的评估方法，强调了当前的局限性，并提出了未来探索的有希望的途径。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 3

### 段落 14 · Page 3

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 3 Fig. 2. The unified RAG core concepts with basic workflow. 2 RAG Framework The hallucinations are largely attributed to LLMs’ inability to access up-to-date information. This limitation stems from the models’ reliance on their training datasets. RAG proposes a solution to this issue by supplementing the LLM’s training data with current information from external sources through a retrieval model, thereby enabling the generation of accurate responses.

**中文**

大型语言模型中检索增强文本生成的综述 3 图 2. 具有基本工作流程的统一 RAG 核心概念。 2 RAG框架 幻觉很大程度上归因于法学硕士无法获取最新信息。这种限制源于模型对其训练数据集的依赖。 RAG 提出了解决这个问题的方法，通过检索模型用外部来源的当前信息补充法学硕士的训练数据，从而能够生成准确的答案。

### 段落 15 · Page 3

**EN**

RAG presents a more cost-effective alternative to the extensive training and fine-tuning processes typically required for LLMs. It allows for the dynamic incorporation of fresh information via traditional retrieval methods or pre-trained LMs, without the need to directly integrate this new data into the LLM. This feature makes RAG both flexible and scalable, facilitating its application across different LLMs for various purposes. The information retrieved through RAG is derived from real-world data, authored by humans, which not only simplifies the generation process but also increases the reliability of the generated responses.

**中文**

RAG 为法学硕士通常所需的广泛培训和微调流程提供了一种更具成本效益的替代方案。它允许通过传统检索方法或预先训练的 LM 动态合并新信息，而无需直接将这些新数据集成到 LLM 中。此功能使 RAG 既灵活又可扩展，便于其在不同的法学硕士中出于各种目的进行应用。通过 RAG 检索的信息源自人类编写的真实世界数据，这不仅简化了生成过程，而且还提高了生成响应的可靠性。

### 段落 16 · Page 3

**EN**

Research by Khandelwal et al. [72] demonstrates that accessing relevant information from the training dataset itself can significantly improve LLM performance, highlighting the effectiveness of RAG. Over time, RAG has evolved from a means of providing supplementary information to enabling multiple interactions between the retrieval and generation components. This involves conducting several rounds of retrieval to refine the accuracy of the information retrieved and iteratively improve the quality of the generated output.

**中文**

Khandelwal 等人的研究。 [72] 表明，从训练数据集本身访问相关信息可以显着提高 LLM 性能，突出了 RAG 的有效性。随着时间的推移，RAG 已经从一种提供补充信息的方式发展为支持检索和生成组件之间的多种交互。这涉及进行多轮检索，以提高检索信息的准确性，并迭代地提高生成输出的质量。

### 段落 17 · Page 3

**EN**

Toolkits such as LangChain1 and LlamaIndex2 have modularized the RAG approach, enhancing its adaptability and expanding its range of applications. Despite these toolkits employing diverse methodologies to tackle different aspects of RAG—from multiple search iterations to iterative generation—they maintain adherence to the fundamental RAG workflow. This consistency is crucial for understanding their operation and pinpointing opportunities for further development. 2.1 Basic RAG Workflow Figure 2 represents the unified RAG core concepts with basic workflow. The workflow of RAG begins with the creation of an index comprising external sources.

**中文**

LangChain1和LlamaIndex2等工具包对RAG方法进行了模块化，增强了其适应性并扩展了其应用范围。尽管这些工具包采用不同的方法来解决 RAG 的不同方面（从多次搜索迭代到迭代生成），但它们仍然坚持基本的 RAG 工作流程。这种一致性对于理解他们的运作和确定进一步发展的机会至关重要。 2.1 RAG 基本工作流程 图2 展示了统一的RAG 核心概念和基本工作流程。 RAG 的工作流程从创建包含外部源的索引开始。

### 段落 18 · Page 3

**EN**

This index serves as the basis for retrieving relevant information through a retriever model based on a specific query. The final step 1https://www.langchain.com 2https://www.llamaindex.ai , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

该索引充当通过基于特定查询的检索器模型检索相关信息的基础。最后一步 1https://www.langchain.com 2https://www.llamaindex.ai , Vol. 1、第1条。出版日期：2018 年 8 月。

### Page 4

### 段落 19 · Page 4

**EN**

4 Huang et al. involves a generator model, which combines the retrieved information with the query to produce the desired output. 2.1.1 Indexing. Efficient retrieval begins with comprehensive indexing, where data preparation is key. This stage involves text normalization processes such as tokenization, stemming, and the removal of stop words to enhance the text’s suitability for indexing [98]. Text segments are then organized into sentences or paragraphs to facilitate more focused searches, allowing for the pinpointing of segments containing pertinent keywords.

**中文**

4 黄等人。涉及生成器模型，它将检索到的信息与查询相结合以产生所需的输出。 2.1.1 索引。高效检索始于全面索引，其中数据准备是关键。此阶段涉及文本规范化过程，例如标记化、词干提取和删除停用词，以增强文本对索引的适用性[98]。然后，文本片段被组织成句子或段落，以促进更有针对性的搜索，从而可以精确定位包含相关关键字的片段。

### 段落 20 · Page 4

**EN**

The integration of deep learning has revolutionized indexing through the use of pretrained LMs for generating semantic vector representations of texts. These vectors are stored, enabling rapid and precise retrieval from extensive data collections, significantly enhancing retrieval efficiency. 2.1.2 Retrieval. While traditional retrieval methods, such as the BM25 algorithm [44], focus on term frequency and presence for document ranking, they often overlook the semantic information of queries. Current strategies leverage pretrained LMs like BERT [29], which capture the semantic essence of queries more effectively.

**中文**

深度学习的集成通过使用预训练的 LM 来生成文本的语义向量表示，彻底改变了索引。这些向量被存储起来，可以从大量的数据集合中快速、精确地检索，显着提高检索效率。 2.1.2 检索。虽然传统的检索方法，例如 BM25 算法 [44]，关注文档排名的术语频率和存在性，但它们经常忽略查询的语义信息。当前的策略利用像 BERT [29] 这样的预训练 LM，它可以更有效地捕获查询的语义本质。

### 段落 21 · Page 4

**EN**

These models improve search accuracy by considering synonyms and the structure of phrases, thereby refining document ranking through the detection of semantic similarities. This is typically achieved by measuring vector distances between documents and queries, combining traditional retrieval metrics with semantic understanding to yield search results that are both relevant and aligned with user intent. 2.1.3 Generation. The generation phase is tasked with producing text that is both relevant to the query and reflective of the information found in the retrieved documents.

**中文**

这些模型通过考虑同义词和短语结构来提高搜索准确性，从而通过检测语义相似性来完善文档排名。这通常是通过测量文档和查询之间的向量距离，将传统检索指标与语义理解相结合来实现的，以产生既相关又符合用户意图的搜索结果。 2.1.3 生成。生成阶段的任务是生成与查询相关并反映检索到的文档中找到的信息的文本。

### 段落 22 · Page 4

**EN**

The usual method involves concatenating the query with the retrieved information, which is then fed into an LLM for text generation [ 85]. Although ensuring the generated text’s alignment and accuracy with the retrieved content presents challenges, it is also essential to strike a balance between adhering closely to the source material and infusing the output with creativity. The generated text should accurately convey the information from the retrieved documents and align with the query’s intent, while also offering the flexibility to introduce new insights or perspectives not explicitly contained within the retrieved data.

**中文**

通常的方法是将查询与检索到的信息连接起来，然后将其输入到 LLM 中进行文本生成 [85]。尽管确保生成的文本与检索内容的一致性和准确性存在挑战，但在紧密遵循源材料和为输出注入创造力之间取得平衡也很重要。生成的文本应准确传达检索到的文档中的信息并与查询的意图保持一致，同时还可以灵活地引入检索到的数据中未明确包含的新见解或观点。

### 段落 23 · Page 4

**EN**

2.2 RAG Paradigm The RAG paradigm organizes research within the domain, offering a straightforward yet robust framework to enhance LLM performance. Central to RAG is its search mechanism, crucial for generating high-quality outcomes. Therefore, this paradigm is structured into four main phases from a retrieval perspective: pre-retrieval, retrieval, post-retrieval, and generation. Both single-hop and multi-hop retrieval approaches, encompassing iterative retrieve-generate cycles, follow this four-phase structure. Figure 3 is the taxonomy tree of RAG’s core techniques. 2.2.1 Pre-Retrieval.

**中文**

2.2 RAG 范式 RAG 范式组织了该领域内的研究，提供了一个简单而强大的框架来提高法学硕士的表现。 RAG 的核心是其搜索机制，对于生成高质量结果至关重要。因此，从检索的角度来看，该范式被构造为四个主要阶段：检索前、检索、检索后和生成。单跳和多跳检索方法（包含迭代检索生成循环）都遵循这种四阶段结构。图3是RAG核心技术的分类树。 2.2.1 预检索。

### 段落 24 · Page 4

**EN**

The pre-retrieval phase of retrieval-augmented generation lays the foundation for successful data and query preparation, ensuring efficient information retrieval. This phase includes essential tasks to prepare for effective data access. Indexing. The process starts with indexing, which establishes an organized system to enable fast and accurate retrieval of information. The specificity of indexing depends on the task and data type.

**中文**

检索增强生成的预检索阶段为成功的数据和查询准备奠定了基础，确保高效的信息检索。此阶段包括为有效数据访问做好准备的基本任务。索引。该过程从索引开始，索引建立一个有组织的系统，以实现快速、准确的信息检索。索引的特殊性取决于任务和数据类型。

### 段落 25 · Page 4

**EN**

For example, sentence-level indexing is beneficial for question-answering systems to precisely locate answers, while document-level indexing is more appropriate for summarizing documents to understand their main concepts and ideas. Query Manipulation. After indexing, query manipulation is performed to adjust user queries for a better match with the indexed data. This involves query reformulation [61, 155], which rewrites , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

例如，句子级索引有利于问答系统精确定位答案，而文档级索引更适合总结文档以了解其主要概念和思想。查询操作。建立索引后，将执行查询操作来调整用户查询，以便更好地匹配索引数据。这涉及查询重构 [61, 155]，重写 , Vol. 1。 1、第1条。出版日期：2018 年 8 月。

### Page 5

### 段落 26 · Page 5

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 5 the query to align more closely with the user’s intention; query expansion [51], which extends the query to capture more relevant results through synonyms or related terms; and query normalization, which resolves differences in spelling or terminology for consistent query matching. Data Modification. Data modification is also critical in enhancing retrieval efficiency.

**中文**

大型语言模型中检索增强文本生成的调查 5 查询更符合用户的意图；查询扩展[51]，扩展查询以通过同义词或相关术语捕获更多相关结果；查询规范化，解决拼写或术语的差异，以实现一致的查询匹配。数据修改。数据修改对于提高检索效率也至关重要。

### 段落 27 · Page 5

**EN**

This step includes preprocessing techniques like removing irrelevant or redundant information to improve the quality of results and enriching the data with additional information such as metadata to boost the relevance and diversity of the retrieved content [6]. 2.2.2 Retrieval. Search & Ranking. The retrieval stage is the combination of search and ranking. It focuses on selecting and prioritizing documents from a dataset to enhance the quality of the generation model’s outputs. This stage employs search algorithms to navigate through the indexed data, finding documents that match a user’s query.

**中文**

此步骤包括预处理技术，例如删除不相关或冗余信息以提高结果质量，并使用元数据等附加信息丰富数据以提高检索内容的相关性和多样性[6]。 2.2.2 检索。搜索和排名。检索阶段是搜索和排序的结合。它专注于从数据集中选择文档并确定其优先级，以提高生成模型输出的质量。此阶段使用搜索算法来浏览索引数据，查找与用户查询匹配的文档。

### 段落 28 · Page 5

**EN**

After identifying relevant documents, the process of initially ranking these documents starts to sort them according to their relevance to the query. 2.2.3 Post-Retrieval. The post-retrieval phase serves to refine the initially retrieved documents to improve the quality of text generation. This phase consists of re-ranking and filtering, each aimed at optimizing the document selection for the final generation task. Re-Ranking. In the re-ranking step, the documents previously retrieved are reassessed, scored, and reorganized.

**中文**

识别相关文档后，对这些文档进行初始排名的过程开始根据它们与查询的相关性对它们进行排序。 2.2.3 检索后。检索后阶段用于细化最初检索的文档，以提高文本生成的质量。此阶段包括重新排序和过滤，每个阶段都旨在优化最终生成任务的文档选择。重排。在重新排序步骤中，先前检索到的文档将被重新评估、评分和重新组织。

### 段落 29 · Page 5

**EN**

The objective is to more accurately highlight the documents most relevant to the query and diminish the importance of the less relevant ones. This step involves incorporating additional metrics and external knowledge sources to enhance precision. In this context, pre-trained models with superior accuracy but lower efficiency can be effectively employed due to the limited set of candidate documents available [54]. Filtering. Filtering aims to remove documents that fail to meet specified quality or relevance standards [56, 74].

**中文**

目的是更准确地突出显示与查询最相关的文档，并降低不太相关的文档的重要性。此步骤涉及合并额外的指标和外部知识源以提高精度。在这种情况下，由于可用的候选文档集有限，可以有效地使用精度较高但效率较低的预训练模型[54]。过滤。过滤的目的是删除不符合指定质量或相关性标准的文档 [56, 74]。

### 段落 30 · Page 5

**EN**

This can be done through several approaches, such as establishing a minimum relevance score threshold to exclude documents below a certain relevance level. Furthermore, the use of feedback from users or prior relevance evaluations assists in adjusting the filtering process, guaranteeing that only the most relevant documents are retained for text generation. 2.2.4 Generation. The generation stage is a crucial component of the RAG process, responsible for leveraging retrieved information to enhance the quality of the generated response.

**中文**

这可以通过多种方法来完成，例如建立最小相关性分数阈值以排除低于特定相关性级别的文档。此外，使用用户反馈或先前的相关性评估有助于调整过滤过程，保证只保留最相关的文档用于文本生成。 2.2.4 生成。生成阶段是 RAG 流程的重要组成部分，负责利用检索到的信息来提高生成响应的质量。

### 段落 31 · Page 5

**EN**

This stage encompasses several sub-steps aimed at producing content that is readable, engaging, and informative. Enhancing. At the heart of the generation phase is the enhancement step, where the objective is to merge the retrieved information with the user’s query to create a coherent and relevant response. This includes the process of elaboration, adding extra details to the retrieved content to enrich it. Efforts are focused on improving the output’s quality by increasing its clarity, coherence, and stylistic appeal through methods such as rephrasing and restructuring.

**中文**

此阶段包含几个子步骤，旨在生成可读、有吸引力且信息丰富的内容。增强。生成阶段的核心是增强步骤，其目标是将检索到的信息与用户的查询合并，以创建连贯且相关的响应。这包括详细阐述的过程，向检索到的内容添加额外的细节以丰富它。努力的重点是通过改写和重组等方法提高清晰度、连贯性和风格吸引力，从而提高产出的质量。

### 段落 32 · Page 5

**EN**

Information from various sources is combined to offer a comprehensive perspective, and verification is conducted to ensure the accuracy and relevance of the content. Customization. Customization is user-centric. It encompasses tailoring content in two primary ways. First, it aligns the generated output with relevant information retrieved in earlier stages, ensuring consistency and accuracy by incorporating key knowledge. Second, it adapts the content to suit user-specific factors such as intended audience, situational context, and personal preferences, shaping the response to be both contextually relevant and user-centric.

**中文**

综合各种来源的信息以提供全面的视角，并进行验证以确保内容的准确性和相关性。定制。定制是以用户为中心的。它包括以两种主要方式定制内容。首先，它将生成的输出与早期阶段检索到的相关信息结合起来，通过纳入关键知识来确保一致性和准确性。其次，它会调整内容以适应特定于用户的因素，例如目标受众、情境背景和个人偏好，从而使响应既与情境相关又以用户为中心。

### 段落 33 · Page 5

**EN**

This dual focus on , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

这双重关注，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 6

### 段落 34 · Page 6

6 Huang et al.

### 段落 35 · Page 6

**EN**

RAG Pre-Retrieval Indexing REALM [42];kNN-LMs [72];RAG [83];Webgpt [100];RETRO [9];MEMWALKER [13];Atlas [94];Chameleon [63];AiSAQ [126];PipeRAG [64];LRUS-CoverTree [93] Query Ma-nipulation Webgpt [100];DSP [73];CoK [86];IRCOT [131];Query2doc [137];Step-Back [163];PROMPTAGATOR [27];KnowledGPT [140];Rewrite-Retrieve-Read [94];FLARE [65];RQ-RAG [12];RARG [159];DRAGIN [124] Data Modification RA-DIT [89];RECITE [125];UPRISE [20];GENREAD [156];KnowledGPT [140];Selfmem [21];RARG [159] Retrieval Search & Ranking REALM [42];kNN-LMs [72];RAG [83];FiD [58];Webgpt [100];RETRO [9];ITRG [34];RA-DIT [89];SURGE [70];PRCA [151];AAR [157];ITER-RETGEN [121];UPR

**中文**

RAG 预检索索引 REALM [42];kNN-LMs [72];RAG [83];Webgpt [100];RETRO [9];MEMWALKER [13];Atlas [94];Chameleon [63];AiSAQ [126];PipeRAG [64];LRUS-CoverTree [93] 查询操作 Webgpt [100];DSP [73];CoK [86];IRCOT [131];Query2doc [137];Step-Back [163];PROMPTAGATOR [27];KnowledGPT [140];Rewrite-Retrieve-Read [94];FLARE [65];RQ-RAG [12];RARG [159];DRAGIN [124] 数据修改RA-DIT [89];RECITE [125];UPRISE [20];GENREAD [156];KnowledGPT [140];Selfmem [21];RARG [159] 检索搜索和排名 REALM [42];kNN-LMs [72];RAG [83];FiD [58];Webgpt [100];RETRO [9];ITRG [34];RA-DIT [89];SURGE [70];PRCA [151];AAR [157];ITER-RETGEN [121];UPR

### 段落 36 · Page 6

**EN**

ISE [20];MEMWALKER [13];Atlas [94];FLARE [65];PlanRAG [81] Post-Retrieval Re-Ranking Re2G [40];DSP [73];CoK [86];FiD-TF [5];ITER-RETGEN [121];PROMPTAGATOR [27];Selfmem [21];DKS-RAC [53];In-ContextRALM [112];Fid-light [47];GenRT [148] Filtering Webgpt [100];Self-RAG [4];FiD-TF [5];PROMPTAGATOR [27];RECOMP [147];DKS-RAC [53];CoK [86];FILCO [141];BlendFilter [135];CRAG [149] Generation Enhancing FiD [58];Webgpt [100];DSP [73];IRCOT [131];ITRG [34];RA-DIT [89];PRCA [151];RECITE [125];UPRISE [20];GENREAD [156];Selfmem [21];MEMWALKER [13];Atlas [94] Customization LAPDOG [52];PersonaRAG [160];ERAGent [123];ROPG [118] Fig.

**中文**

ISE [20];MEMWALKER [13];Atlas [94];FLARE [65];PlanRAG [81] 检索后重排序 Re2G [40];DSP [73];CoK [86];FiD-TF [5];ITER-RETGEN [121];PROMPTAGATOR [27];Selfmem [21];DKS-RAC [53];In-ContextRALM [112];Fid-light [47];GenRT [148]过滤Webgpt [100];Self-RAG [4];FiD-TF [5];PROMPTAGATOR [27];RECOMP [147];DKS-RAC [53];CoK [86];FILCO [141];BlendFilter [135];CRAG [149] 生成增强 FiD [58];Webgpt [100];DSP [73];IRCOT [131];ITRG [34];RA-DIT [89];PRCA [151];RECITE [125];UPRISE [20];GENREAD [156];Selfmem [21];MEMWALKER [13];Atlas [94] 定制 LAPDOG [52]；PersonaRAG [160]；ERAGent [123]；ROPG [118]

### 段落 37 · Page 6

**EN**

3. Taxonomy tree of RAG’s core techniques integrating relevant knowledge and adjusting to diverse contextual demands forms the basis of effective customization in RAG. 3 Pre-Retrieval 3.1 Indexing One of the most commonly used indexing structures in traditional information retrieval systems is the inverted index. This structure associates documents with words to form a vocabulary list, allowing users to quickly locate references where a specific word appears within a collection of documents.

**中文**

3. RAG核心技术的分类树整合了相关知识并适应不同的上下文需求，构成了RAG有效定制的基础。 3 预检索 3.1 索引 传统信息检索系统中最常用的索引结构之一是倒排索引。这种结构将文档与单词关联起来形成词汇列表，使用户可以快速找到文档集合中出现特定单词的参考。

### 段落 38 · Page 6

**EN**

The vocabulary list here refers to the set of all unique words present in the document collection, while the reference includes the documents where the word appears, along with the word’s position and weight within those documents. However, traditional indexing structures struggle to retrieve documents that are semantically related to a user’s query but do not contain the exact query terms. To address this limitation, retrieval methods using dense vectors generated by deep learning models have become the preferred choice.

**中文**

这里的词汇列表是指文档集合中存在的所有唯一单词的集合，而参考包括该单词出现的文档，以及该单词在这些文档中的位置和权重。然而，传统的索引结构很难检索与用户查询语义相关但不包含确切查询术语的文档。为了解决这一限制，使用深度学习模型生成的密集向量的检索方法已成为首选。

### 段落 39 · Page 6

**EN**

These vectors, also known as embeddings, capture the semantic meaning of words and documents, allowing for more flexible and accurate retrieval. Dense vector-based indexing methods can be categorized into three main types: graphs, product quantization (PQ) [62], and locality-sensitive hashing (LSH) [28]. Since generating dense vectors with large language models requires substantial resources, and the document collections to be searched are typically vast, the core strategy of these indexing methods is based on approximate nearest neighbor search (ANNS) [3].

**中文**

这些向量（也称为嵌入）捕获单词和文档的语义，从而实现更灵活、更准确的检索。基于密集向量的索引方法可以分为三种主要类型：图、乘积量化（PQ）[62]和局部敏感哈希（LSH）[28]。由于使用大型语言模型生成密集向量需要大量资源，并且要搜索的文档集合通常非常庞大，因此这些索引方法的核心策略是基于近似最近邻搜索（ANNS）[3]。

### 段落 40 · Page 6

**EN**

This approach significantly speeds up the search process at the cost of a slight reduction in search accuracy. Graph. Using graphs to build indexes is a common practice in RAG. By indexing vectors with a graph structure, the range of nodes where distances need to be computed during retrieval can be limited to a local subgraph, thereby enhancing search speed. Several prominent methods and tools have been developed using this approach. For example, k-nearest neighbor language models kNN-LMs [72], as demonstrated by Khandelwal et al., integrate the kNN algorithm with pre-trained language models.

**中文**

这种方法显着加快了搜索过程，但代价是搜索精度略有下降。图形。使用图构建索引是 RAG 中的常见做法。通过图结构对向量进行索引，可以将检索时需要计算距离的节点范围限制在局部子图内，从而提高搜索速度。使用这种方法开发了几种著名的方法和工具。例如，K-近邻语言模型 kNN-LMs [72]，如 Khandelwal 等人所证明的，将 kNN 算法与预训练的语言模型集成。

### 段落 41 · Page 6

**EN**

This method employs a datastore created from collections of texts to dynamically retrieve contextually relevant examples, enhancing model performance without requiring additional training. FAISS [68], a tool widely adopted for indexing in many studies [72, 73, 83], integrates enhancements like the Hierarchical Navigable Small World (HNSW) approximation , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

该方法采用从文本集合创建的数据存储来动态检索上下文相关的示例，从而增强模型性能，而无需额外的训练。 FAISS [68] 是许多研究中广泛采用的索引工具 [72,73,83]，它集成了诸如分层可导航小世界 (HNSW) 近似等增强功能，第 1 卷。 1、第1条。出版日期：2018 年 8 月。

### Page 7

### 段落 42 · Page 7

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 7 [97] to further speed up retrieval [83]. WebGPT [100] showcases another practical application by utilizing the Bing API3 for indexing based on actual user search histories, which illustrates the potential of integrating real-world user data into the retrieval process. Additionally, other methods like MEMWALKER [13] introduces innovative approaches to overcome limitations such as context window size in large language models. It creates a memory tree from input text, segmenting the text into smaller pieces and summarizing these segments into a hierarchical structure.

**中文**

大型语言模型中检索增强文本生成的调查7 [97]，以进一步加快检索速度[83]。 WebGPT [100] 展示了另一个实际应用，即利用 Bing API3 基于实际用户搜索历史进行索引，这说明了将现实世界用户数据集成到检索过程中的潜力。此外，MEMWALKER [13] 等其他方法引入了创新方法来克服大型语言模型中上下文窗口大小等限制。它根据输入文本创建一个记忆树，将文本分割成更小的片段，并将这些片段汇总成层次结构。

### 段落 43 · Page 7

**EN**

Moreover, LRUS-CoverTree method [ 93] designed another tree structure for k-Maximum Inner-Product Search (k-MIPS) and achieves performance comparable with significantly lower index construction time. These techniques facilitate efficient indexing and management of large information volumes, demonstrating the versatility and effectiveness of graph-based approaches. Product Quantization. PQ is one of the most representative methods for handling large-scale data. It accelerates searches by segmenting vectors and then clustering each part for quantization.

**中文**

此外，LRUS-CoverTree方法[93]为k-最大内积搜索（k-MIPS）设计了另一种树结构，并实现了与显着缩短索引构建时间相当的性能。这些技术有助于高效索引和管理大量信息，展示了基于图的方法的多功能性和有效性。产品量化。 PQ是处理大规模数据最具代表性的方法之一。它通过分割向量然后对每个部分进行聚类以进行量化来加速搜索。

### 段落 44 · Page 7

**EN**

Unlike graph-based methods, which speed up searches by reducing the number of vectors for distance calculation, PQ achieves faster searches by reducing the time spent on calculating word distances. Several implementations of PQ have emerged in RAG, each improving its efficiency and scalability in different ways. PipeRAG [64] integrates PQ within a pipeline-parallelism framework to enhance retrieval-augmented generation by optimizing retrieval intervals. Chameleon system [63] leverages PQ in a disaggregated accelerator environment to balance memory usage and retrieval speed in RAG tasks.

**中文**

与基于图的方法通过减少距离计算向量的数量来加速搜索不同，PQ 通过减少计算单词距离所花费的时间来实现更快的搜索。 RAG 中出现了多种 PQ 实现，每种实现都以不同的方式提高了其效率和可扩展性。 PipeRAG [64] 将 PQ 集成到管道并行框架中，通过优化检索间隔来增强检索增强生成。 Chameleon 系统 [63] 在分解的加速器环境中利用 PQ 来平衡 RAG 任务中的内存使用和检索速度。

### 段落 45 · Page 7

**EN**

AiSAQ [126] introduces an all-in-storage ANNS method that offloads PQ vectors from DRAM to storage, drastically reducing memory usage while maintaining high recall. It demonstrates that even with billion-scale datasets, memory usage can be minimized to around 10 MB with only minor latency increases, making it a highly scalable solution for RAG systems. Locality-sensitive Hashing. The core idea of LSH is to place similar vectors into the same hash bucket with high probability. LSH uses hash functions that map similar vectors to the same or nearby hash values, making it easier to find approximate nearest neighbours.

**中文**

AiSAQ [126] 引入了一种全存储 ANNS 方法，将 PQ 向量从 DRAM 卸载到存储，在保持高召回率的同时大幅减少内存使用。它表明，即使对于数十亿规模的数据集，内存使用量也可以最小化到 10 MB 左右，而延迟只增加很小，这使其成为 RAG 系统的高度可扩展的解决方案。局部敏感哈希。 LSH的核心思想是将相似的向量以高概率放入同一个哈希桶中。 LSH 使用哈希函数将相似的向量映射到相同或附近的哈希值，从而更容易找到近似的最近邻居。

### 段落 46 · Page 7

**EN**

In LSH, when a query vector is hashed, the system quickly retrieves candidate vectors that share the same hash value. This method reduces the dimensionality of the problem and can be implemented efficiently, but it may introduce some inaccuracies due to the hashing process itself. While LSH is rarely used in RAG systems compared to graph-based and PQ methods, it still offers a useful approach in scenarios where speed is prioritized over the slight loss in accuracy. 3.2 Query Manipulation Query manipulation is pivotal in enhancing the effectiveness and accuracy of modern IR systems.

**中文**

在LSH中，当查询向量被散列时，系统快速检索共享相同散列值的候选向量。该方法降低了问题的维数并且可以有效地实现，但是由于散列过程本身可能会引入一些不准确性。虽然与基于图的方法和 PQ 方法相比，LSH 很少在 RAG 系统中使用，但在速度优先于准确性轻微损失的情况下，它仍然提供了一种有用的方法。 3.2 查询操作 查询操作对于提高现代 IR 系统的有效性和准确性至关重要。

### 段落 47 · Page 7

**EN**

By refining users’ original queries, it addresses challenges such as ambiguous phrasing and vocabulary mismatches between the query and target documents. This process involves more than merely replacing words with synonyms; it requires a deep understanding of user intent and the context of the query, particularly in complex tasks like RAG. Effective query manipulation significantly boosts retrieval performance, which in turn can greatly impact the quality of generated outputs. The three primary approaches to query manipulation are query expansion, query reformulation, and prompt-based rewriting. Query Expansion.

**中文**

通过细化用户的原始查询，它解决了查询与目标文档之间的措辞不明确和词汇不匹配等挑战。这个过程不仅仅涉及用同义词替换单词；还涉及到用同义词替换单词。它需要深入了解用户意图和查询上下文，特别是在 RAG 等复杂任务中。有效的查询操作可以显着提高检索性能，从而极大地影响生成输出的质量。查询操作的三种主要方法是查询扩展、查询重构和基于提示的重写。查询扩展。

### 段落 48 · Page 7

**EN**

Query expansion involves augmenting the original query with additional terms or phrases that are related to or synonymous with the query terms. In the context of LLMs, query expansion can be more sophisticated, utilizing the model’s extensive knowledge to generate contextually relevant expansions. This technique aims to improve recall by ensuring that the retrieval process captures a broader range of relevant documents, accommodating different 3https://www.microsoft.com/en-us/bing/apis/bing-web-search-api , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

查询扩展涉及使用与查询术语相关或同义的附加术语或短语来扩充原始查询。在法学硕士的背景下，查询扩展可以更加复杂，利用模型的广泛知识来生成上下文相关的扩展。该技术旨在通过确保检索过程捕获更广泛的相关文档来提高召回率，以适应不同的3https://www.microsoft.com/en-us/bing/apis/bing-web-search-api，第 1 卷。 1、第1条。出版日期：2018 年 8 月。

### Page 8

### 段落 49 · Page 8

**EN**

8 Huang et al. terminologies or expressions. Techniques such as synonym expansion, semantic similarity, or leveraging external knowledge bases are commonly employed in query expansion. For example, the method described in FiD [ 58] expands the query by retrieving a wider range of passages using both sparse and dense retrieval techniques, enabling the model to aggregate evidence from multiple sources and thereby improving the accuracy and robustness of generated answers.

**中文**

8 黄等人。术语或表达方式。查询扩展中通常采用同义词扩展、语义相似性或利用外部知识库等技术。例如，FiD [58]中描述的方法通过使用稀疏和密集检索技术检索更广泛的段落来扩展查询，使模型能够聚合来自多个来源的证据，从而提高生成答案的准确性和鲁棒性。

### 段落 50 · Page 8

**EN**

A more advanced form of query expansion is demonstrated in Query2doc [137], where pseudo-documents generated by LLMs enhance the original query, effectively bridging the gap between the user’s input and the corpus information, which benefits both sparse and dense retrieval systems. Similarly, KnowledGPT [140] broadens the scope of information accessed during retrieval by leveraging external knowledge bases, further refining the retrieval process. The RARG [159] framework uses an evidence-driven query expansion approach, incorporating a wide array of supporting documents to generate informed and accurate counter-misinformation responses.

**中文**

Query2doc [137] 演示了一种更高级的查询扩展形式，其中由 LLM 生成的伪文档增强了原始查询，有效地弥合了用户输入和语料库信息之间的差距，这对稀疏和密集检索系统都有好处。类似地，KnowledGPT [140]通过利用外部知识库扩大了检索过程中访问信息的范围，进一步细化了检索过程。 RARG [159] 框架使用证据驱动的查询扩展方法，结合广泛的支持文档来生成知情且准确的反错误信息响应。

### 段落 51 · Page 8

**EN**

Query Reformulation. Query reformulation involves rephrasing or restructuring the original query to enhance its effectiveness. This might include making the wording more specific, removing vague terms, or adjusting the syntax to better align with the retrieval system’s requirements. With LLMs, query reformulation can be dynamically driven by understanding the user’s intent and context, allowing for more precise modifications that lead to improved retrieval results. This reformulation process can also be informed by past queries or user interactions, adapting the query to better fit the specific retrieval task.

**中文**

查询重构。查询重构涉及重新措辞或重构原始查询以增强其有效性。这可能包括使措辞更加具体、删除模糊术语或调整语法以更好地符合检索系统的要求。借助法学硕士，可以通过了解用户的意图和上下文来动态驱动查询重构，从而进行更精确的修改，从而改善检索结果。此重新制定过程还可以通过过去的查询或用户交互来了解，从而调整查询以更好地适应特定的检索任务。

### 段落 52 · Page 8

**EN**

For instance, the RQ-RAG [12] model represents an advanced form of query reformulation by rewriting, decomposing, and disambiguating queries, making it particularly effective in scenarios that demand complex query handling. This approach ensures that the refined query better matches the needed context, improving the relevance of retrieved information. Rewrite-Retrieve-Read framework [94] adjusts the original query to optimize the retrieval process, allowing the system to more effectively leverage retrieved data for generating accurate responses.

**中文**

例如，RQ-RAG [12] 模型代表了一种通过重写、分解和消除歧义查询来重构查询的高级形式，使其在需要复杂查询处理的场景中特别有效。这种方法可确保细化的查询更好地匹配所需的上下文，从而提高检索到的信息的相关性。重写-检索-读取框架[94]调整原始查询以优化检索过程，使系统能够更有效地利用检索到的数据来生成准确的响应。

### 段落 53 · Page 8

**EN**

Additionally, FLARE [65] exemplifies query reformulation through its active retrieval-augmented generation approach, which iteratively refines the query based on a feedback loop between retrieval and generation, thereby enhancing the accuracy and relevance of the retrieved information. Prompt-based Rewriting. Prompt-based rewriting, particularly in the context of LLMs, represents an innovative approach where the original query is embedded within a larger prompt or context to guide the LLM’s response.

**中文**

此外，FLARE [65]通过其主动检索增强生成方法举例说明了查询重构，该方法基于检索和生成之间的反馈循环迭代地细化查询，从而提高检索信息的准确性和相关性。基于提示的重写。基于提示的重写，特别是在法学硕士的背景下，代表了一种创新方法，其中原始查询嵌入到更大的提示或上下文中，以指导法学硕士的响应。

### 段落 54 · Page 8

**EN**

This technique harnesses the model’s ability to understand and generate language within a specific context, effectively rewriting the query to align with the desired output. Prompt-based rewriting is especially powerful in scenarios where the retrieval process is integrated into a generative workflow, allowing the system to adapt the query to various stages of retrieval and generation. This approach may also involve dynamic prompts that evolve based on interaction, further refining the retrieval process.

**中文**

该技术利用模型在特定上下文中理解和生成语言的能力，有效地重写查询以与所需的输出保持一致。基于提示的重写在检索过程集成到生成工作流程中的场景中尤其强大，允许系统使查询适应检索和生成的各个阶段。这种方法还可能涉及基于交互而演变的动态提示，从而进一步完善检索过程。

### 段落 55 · Page 8

**EN**

For example, Step-Back [163] refines the query context through carefully crafted prompts that guide the LLM’s reasoning process, ensuring that the outputs are more aligned with the user’s intent, particularly in complex reasoning tasks. The CoK [86] method focuses on dynamically adapting the knowledge source and using prompts to rewrite the context in which a query is interpreted. This approach leverages prompt-based rewriting to enable the LLM to effectively integrate and ground its responses based on various heterogeneous knowledge sources.

**中文**

例如，Step-Back [163] 通过精心设计的提示来细化查询上下文，指导法学硕士的推理过程，确保输出更符合用户的意图，特别是在复杂的推理任务中。 CoK [86]方法侧重于动态调整知识源并使用提示重写解释查询的上下文。这种方法利用基于提示的重写，使法学硕士能够有效地整合和基于各种异构知识源的响应。

### 段落 56 · Page 8

**EN**

Additionally, Promptagator [27] discusses using prompt-based techniques to adapt and rewrite the query to better align with the retrieval system’s expectations, particularly in few-shot learning scenarios. These prompts guide the model in generating or refining the query to optimize retrieval results. , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

此外，Promptagator [27] 讨论了使用基于提示的技术来调整和重写查询，以更好地符合检索系统的期望，特别是在少量学习场景中。这些提示指导模型生成或细化查询以优化检索结果。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 9

### 段落 57 · Page 9

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 9 3.3 Data Modification Document modification techniques play a critical role in enhancing retrieval performance, particularly when integrated with LLMs. These techniques can be broadly categorized into Internal Data Augmentation and External Data Enrichment. Internal Data Augmentation focuses on maximizing the value of existing information within documents or models, while External Data Enrichment introduces supplementary data from outside sources to fill gaps, provide additional context, or broaden the scope of the content. Internal Data Augmentation.

**中文**

大型语言模型中检索增强文本生成的调查 9 3.3 数据修改 文档修改技术在提高检索性能方面发挥着关键作用，特别是与法学硕士集成时。这些技术可以大致分为内部数据增强和外部数据丰富。内部数据增强侧重于最大化文档或模型中现有信息的价值，而外部数据丰富则引入来自外部来源的补充数据来填补空白、提供额外的背景或扩大内容范围。内部数据增强。

### 段落 58 · Page 9

**EN**

Internal Data Augmentation leverages information already present within documents or taps into the inherent knowledge embedded in LLMs. Techniques like paraphrasing, where content is rewritten for improved readability or multiple perspectives, and summarization, which condenses information while retaining core content, are commonly employed. Other methods involve generating supplementary content or explanations that are contextually related without introducing external data.

**中文**

内部数据增强利用文档中已有的信息或利用法学硕士中嵌入的固有知识。通常采用释义（重写内容以提高可读性或多个视角）和摘要（在保留核心内容的同时压缩信息）等技术。其他方法涉及生成上下文相关的补充内容或解释，而不引入外部数据。

### 段落 59 · Page 9

**EN**

For instance, RECITE [125] utilizes a model’s internal memory to recite relevant information before generating responses, thus enhancing performance in tasks like closed-book question answering without external data. KnowledGPT [140] similarly refines the internal knowledge embedded within LLMs, optimizing its use during generation. GENREAD [156] further demonstrates how pre-existing knowledge within LLMs can be used to generate context that enhances task performance, bypassing the need for external sources.

**中文**

例如，RECITE [125]利用模型的内部记忆在生成响应之前背诵相关信息，从而提高在没有外部数据的闭卷问答等任务中的性能。 KnowledGPT [140] 同样提炼了法学硕士中嵌入的内部知识，优化了其在生成过程中的使用。 GENREAD [156] 进一步演示了如何使用法学硕士中预先存在的知识来生成增强任务性能的上下文，从而绕过对外部资源的需求。

### 段落 60 · Page 9

**EN**

In another example, the Selfmem [21] framework allows the model to iteratively use its own outputs as memory in subsequent generation tasks. By selecting and utilizing the best internal outputs as memory, this approach boosts model performance without depending on external memory resources. External Data Enrichment. External Data Enrichment enhances document content by incorporating new information from external sources, enriching the overall context and accuracy. This process can involve integrating facts, data, or contextual knowledge from external datasets or knowledge bases.

**中文**

在另一个例子中，Selfmem [21] 框架允许模型在后续生成任务中迭代地使用自己的输出作为内存。通过选择并利用最佳的内部输出作为内存，这种方法可以在不依赖外部内存资源的情况下提高模型性能。外部数据丰富。外部数据丰富通过合并来自外部来源的新信息来增强文档内容，丰富整体背景和准确性。此过程可能涉及集成来自外部数据集或知识库的事实、数据或上下文知识。

### 段落 61 · Page 9

**EN**

For example, RA-DIT [89] augments input prompts during fine-tuning by leveraging large datasets like Wikipedia and CommonCrawl, enhancing the model’s capability in knowledgeintensive tasks. The dual instruction tuning technique optimizes both the language model and the retriever to more effectively incorporate retrieved information. UPRISE [20] demonstrates how retrieving prompts from diverse task datasets improves model generalization in zero-shot scenarios by enriching the context during inference.

**中文**

例如，RA-DIT [89] 通过利用 Wikipedia 和 CommonCrawl 等大型数据集在微调期间增强输入提示，从而增强模型在知识密集型任务中的能力。双指令调整技术优化了语言模型和检索器，以更有效地合并检索到的信息。 UPRISE [20] 演示了如何通过丰富推理过程中的上下文来从不同的任务数据集中检索提示，从而提高零样本场景中的模型泛化能力。

### 段落 62 · Page 9

**EN**

Additionally, RARG [ 159] exemplifies external data enrichment by integrating scientific evidence from academic databases to strengthen responses countering misinformation. This method involves a two-stage retrieval pipeline that identifies and ranks relevant documents, which are then used to support and enhance the factual accuracy of generated responses. 4 Retrieval 4.1 Search & Ranking The search and ranking process within RAG is crucial for improving the relevance and accuracy of generated outputs. Several methodologies have been developed to refine this process, each contributing unique strategies for enhancing retrieval and ranking.

**中文**

此外，RARG [159] 通过整合学术数据库中的科学证据来强化外部数据丰富，以加强针对错误信息的应对措施。该方法涉及一个两阶段检索管道，用于识别相关文档并对其进行排名，然后使用这些文档来支持和提高生成的响应的事实准确性。 4 检索 4.1 搜索和排名 RAG 中的搜索和排名过程对于提高生成输出的相关性和准确性至关重要。已经开发了几种方法来完善这一过程，每种方法都为增强检索和排名提供了独特的策略。

### 段落 63 · Page 9

**EN**

For example, Atlas [59] and AAR [157] both aim to improve the relevance of retrieved documents, but they approach this challenge differently. Atlas focuses on optimizing the retriever’s ability to select contextually relevant documents, especially in new domains with limited data, by employing few-shot learning techniques such as Attention Distillation and Perplexity Distillation. AAR, on the other hand, adapts retrieval preferences to better align with the requirements of LLMs, enhancing retrieval generalization across tasks by training a smaller source model. , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

例如，Atlas [59] 和 AAR [157] 都旨在提高检索到的文档的相关性，但它们以不同的方式应对这一挑战。 Atlas 专注于通过采用注意力蒸馏和困惑度蒸馏等小样本学习技术来优化检索器选择上下文相关文档的能力，特别是在数据有限的新领域。另一方面，AAR 调整检索偏好以更好地满足法学硕士的要求，通过训练较小的源模型来增强跨任务的检索泛化。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 10

### 段落 64 · Page 10

**EN**

10 Huang et al. Fig. 4. An example of a typical RAG framework with interative retrieval strategy. Additionally, IRCOT [131] and FLARE [65] introduce dynamic interactions within the retrieval process, albeit with distinct goals. IRCOT integrates retrieval with chain-of-thought (CoT) reasoning, interleaving these processes to ensure that each retrieval step supports the ongoing reasoning task. FLARE, in contrast, adopts a confidence-based active retrieval mechanism, dynamically triggering retrieval when the model generates low-confidence tokens.

**中文**

10 黄等人。图 4. 具有交互式检索策略的典型 RAG 框架示例。此外，IRCOT [131] 和 FLARE [65] 在检索过程中引入了动态交互，尽管目标不同。 IRCOT 将检索与思想链 (CoT) 推理相结合，交错这些过程以确保每个检索步骤都支持正在进行的推理任务。相比之下，FLARE 采用基于置信度的主动检索机制，当模型生成低置信度 token 时动态触发检索。

### 段落 65 · Page 10

**EN**

This approach is particularly useful in scenarios where model confidence varies, as it allows the system to fetch additional information to resolve uncertainties during the generation process. When addressing domain-specific retrieval challenges, SURGE [70] and PRCA [151] offer different solutions. SURGE uses a subgraph retriever to extract relevant subgraphs from knowledge graphs, , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

这种方法在模型置信度变化的场景中特别有用，因为它允许系统获取额外的信息来解决生成过程中的不确定性。在解决特定领域的检索挑战时，SURGE [70] 和 PRCA [151] 提供了不同的解决方案。 SURGE 使用子图检索器从知识图谱中提取相关子图，，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 11

### 段落 66 · Page 11

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 11 integrating structured data into the retrieval process to improve the contextual understanding of generated responses. The relational structure of knowledge graphs allows for more accurate and informed retrieval. PRCA, in contrast, focuses on domain-specific abstractive summarization, using a reward-driven approach to refine the retrieved content. This strategy is designed to optimize content for the generator, particularly in scenarios where the generator functions as a black box, thereby enhancing alignment between retrieval and generation.

**中文**

大型语言模型中检索增强文本生成的调查 11 将结构化数据集成到检索过程中，以提高对生成响应的上下文理解。知识图的关系结构可以实现更准确、更明智的检索。相比之下，PRCA 专注于特定领域的抽象概括，使用奖励驱动的方法来细化检索到的内容。该策略旨在优化生成器的内容，特别是在生成器充当黑匣子的情况下，从而增强检索和生成之间的一致性。

### 段落 67 · Page 11

**EN**

MEMWALKER [13] presents a unique approach to handling long-context question answering by incorporating an internal search and ranking mechanism within a memory tree structure. This method navigates extensive memory stores, ensuring that the most relevant information is retrieved and used for complex queries. Unlike other methods, MEMWALKER emphasizes efficient processing of long texts through iterative navigation and summarization, rather than solely optimizing the initial retrieval phase.

**中文**

MEMWALKER [13] 提出了一种独特的方法来处理长上下文问答，通过在内存树结构中合并内部搜索和排名机制。此方法可导航大量内存存储，确保检索最相关的信息并将其用于复杂的查询。与其他方法不同，MEMWALKER 强调通过迭代导航和摘要来有效处理长文本，而不是仅仅优化初始检索阶段。

### 段落 68 · Page 11

**EN**

4.2 Retrieval Strategy The retrieval strategies within RAG are vital for customizing the retrieval process to specific application needs, with each strategy offering distinct advantages and addressing particular challenges. In RAG, it is mostly the utilization of retrieval techniques rather than the exploration of retrieval algorithms that is involved, so it is the strategy of retrieval that is usually considered in searching and ranking.

**中文**

4.2 检索策略 RAG 中的检索策略对于根据特定应用需求定制检索过程至关重要，每种策略都提供独特的优势并解决特定的挑战。 RAG中涉及的主要是检索技术的利用，而不是检索算法的探索，因此在搜索和排序时通常考虑的是检索策略。

### 段落 69 · Page 11

**EN**

While basic RAGs are usually single-hop searches, i.e., they are retrieved only once as generated supplementary material, today’s RAGs are mostly multi-hop searches, i.e., they are searched several times through different search strategies until they are satisfied. In terms of practical applications these strategies belong to the design on the engineering pipeline. Figure 4 shows a typical case of the RAG framework with iterative retrieval strategy. There are five main retrieval strategies in RAG: Basic Retrieval Strategy.

**中文**

虽然基本 RAG 通常是单跳搜索，即它们作为生成的补充材料仅检索一次，但今天的 RAG 大多是多跳搜索，即通过不同的搜索策略对它们进行多次搜索，直到满意为止。从实际应用来看，这些策略属于工程管道的设计。图 4 显示了采用迭代检索策略的 RAG 框架的典型案例。 RAG中有五种主要的检索策略： 基本检索策略。

### 段落 70 · Page 11

**EN**

Basic retrieval strategies typically follow a linear workflow, moving sequentially through pre-retrieval, retrieval, post-retrieval, and generation phases. The Atlas [94] framework exemplifies this straightforward approach, guiding the retrieval process efficiently from start to finish without iterations or complex conditional modifications. REPLUG [122] similarly follows this basic strategy, augmenting black-box language models with retrieval in a simple manner, where the retrieved information is directly used to enhance the generation process. Iterative Retrieval Strategy.

**中文**

基本检索策略通常遵循线性工作流程，依次经历检索前、检索、检索后和生成阶段。 Atlas [94] 框架例证了这种简单的方法，从头到尾有效地指导检索过程，无需迭代或复杂的条件修改。 REPLUG [122]同样遵循这一基本策略，以简单的方式通过检索增强黑盒语言模型，其中检索到的信息直接用于增强生成过程。迭代检索策略。

### 段落 71 · Page 11

**EN**

For more complex scenarios, iterative retrieval strategies (Algorithm 1) are employed, where information is retrieved in multiple steps, each informed by previous results. IRCOT [131] exemplifies this by integrating retrieval with chain-of-thought reasoning, where the retrieval process is sequential and closely tied to reasoning steps. This method is particularly effective in scenarios requiring multi-step problem-solving, such as research assistance or complex queries that benefit from detailed exploration.

**中文**

对于更复杂的场景，采用迭代检索策略（算法 1），其中分多个步骤检索信息，每个步骤都由先前的结果通知。 IRCOT [131] 通过将检索与思想链推理相结合来证明了这一点，其中检索过程是连续的并且与推理步骤紧密相关。该方法在需要多步骤解决问题的场景中特别有效，例如研究协助或受益于详细探索的复杂查询。

### 段落 72 · Page 11

**EN**

ITER-RETGEN [121] also employs iterative retrieval, refining the process based on generated responses, allowing for continuous improvement and closer alignment between retrieval and generation. RQ-RAG [12] advances this approach by using techniques like query rewriting, decomposition, and disambiguation, refining the retrieval step-bystep to enhance the final output. PlanRAG [81] also fits within this strategy, iteratively refining the retrieval process based on generated content and feedback, ensuring that each step is better informed than the last. Recursive Retrieval Strategy.

**中文**

ITER-RETGEN [121] 还采用迭代检索，根据生成的响应改进流程，从而实现持续改进以及检索和生成之间更紧密的一致性。 RQ-RAG [12] 通过使用查询重写、分解和消歧等技术来改进这种方法，逐步改进检索以增强最终输出。 PlanRAG [81] 也适合这一策略，根据生成的内容和反馈迭代地完善检索过程，确保每一步都比上一步更明智。递归检索策略。

### 段落 73 · Page 11

**EN**

Recursive retrieval (Algorithm 2) involves retrieval that can call itself, creating a hierarchy or tree of retrievals. This method effectively handles hierarchical or layered information by breaking down complex queries into simpler sub-queries. It is particularly useful for hierarchical data exploration, knowledge base construction, and detailed information , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

递归检索（算法 2）涉及可以调用自身的检索，从而创建检索的层次结构或树。该方法通过将复杂查询分解为更简单的子查询来有效地处理分层或分层信息。它对于分层数据探索、知识库构建和详细信息特别有用，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 12

### 段落 74 · Page 12

12 Huang et al.

### 段落 75 · Page 12

**EN**

Algorithm 1 Iterative Retrieval Strategy in RAG Require: Query 𝑞, Documents 𝐷, Maximum Iterations 𝑁 , Retriever 𝑅, Generator 𝐺, Pre-retrieval Function 𝐹𝑝𝑟𝑒 , Post-retrieval Function 𝐹𝑝𝑜𝑠𝑡 Ensure: Final Output 𝑦𝑓 𝑖𝑛𝑎𝑙 1: Initialize 𝑖 ← 1 // Start iteration counter 2: while 𝑖 ≤ 𝑁 do 3: Pre-retrieval Phase 4: 𝑞′ ← 𝐹𝑝𝑟𝑒 (𝑞) // Indexing, Query Manipulation, Data Modification 5: Retrieval Phase 6: 𝐷𝑖 ← 𝑅(𝑞′, 𝐷) // Search and initial ranking of documents 7: Post-retrieval Phase 8: 𝐷 ′ 𝑖 ← 𝐹𝑝𝑜𝑠𝑡 (𝑞′, 𝐷𝑖 ) // Re-ranking and filtering to refine documents 9: Generation Phase 10: 𝑦𝑖 ← 𝐺 (𝑞′, 𝐷′ 𝑖 ) // Generate output based on refined documents 11: if sto

**中文**

RAG 中的算法 1 迭代检索策略需要：查询𝑞、文档𝐷、最大迭代次数𝑁、检索器𝑅、生成器𝐺、预检索函数𝐹𝑝𝑟𝑒、后检索函数𝐹𝑝𝑜𝑠𝑡确保：最终输出 𝑦𝑓 𝑖𝑛𝑎𝑙 1：初始化 𝑖 ← 1 // 启动迭代计数器 2：while 𝑖 ≤ 𝑁 do 3：预检索阶段 4：𝑞′ ← 𝐹𝑝𝑟𝑒 (𝑞) // 索引、查询操作，数据修改 5: 检索阶段 6: 𝐷𝑖 ← 𝑅(𝑞′, 𝐷) // 文档的搜索和初始排序 7: 检索后阶段 8: 𝐷 ′ 𝑖 ← 𝐹𝑝𝑜𝑠𝑡 (𝑞′, 𝐷𝑖 ) //重新排序和过滤以细化文档 9: 生成阶段 10: 𝑦𝑖 ← 𝐺 (𝑞′, 𝐷′ 𝑖 ) // 根据细化文档生成输出 11: if sto

### 段落 76 · Page 12

**EN**

pping condition met based on 𝑦𝑖 then 12: BREAK // Stop iterations if output is satisfactory 13: end if 14: Update 𝑞′ ← UpdateQuery(𝑞, 𝑦𝑖 ) // Refine query based on the generated output 15: 𝑖 ← 𝑖 + 1 // Increment iteration counter 16: end while 17: Final Synthesis 18: 𝑦𝑓 𝑖𝑛𝑎𝑙 ← SynthesizeResults({𝑦1, 𝑦2, .

**中文**

基于 𝑦𝑖 满足 pping 条件 then 12: BREAK // 如果输出令人满意则停止迭代 13: end if 14: Update 𝑞′ ← UpdateQuery(𝑞, 𝑦𝑖 ) // 根据生成的输出细化查询 15: 𝑖 ← 𝑖 + 1 // 递增迭代计数器 16: end while 17: 最终综合18: 𝑦𝑓 𝑖𝑛𝑎𝑙 ← SynthesizeResults({𝑦1, 𝑦2, .

### 段落 77 · Page 12

**EN**

. . , 𝑦𝑖 }) // Merge results 19: return 𝑦𝑓 𝑖𝑛𝑎𝑙 retrieval. SURGE [70] leverages this strategy through knowledge graphs, where relevant subgraphs are extracted to enhance contextual understanding. The relational structure of knowledge graphs facilitates navigating multiple layers of information, ensuring accurate and contextually relevant retrieval. MEMWALKER [13] similarly adopts a recursive approach, processing long texts by constructing a memory tree of summaries.

**中文**

。。 , 𝑦𝑖 }) // 合并结果 19: 返回 𝑦𝑓 𝑖𝑛𝑎𝑙 检索。 SURGE [70]通过知识图利用这一策略，提取相关子图以增强上下文理解。知识图的关系结构有助于导航多层信息，确保准确且与上下文相关的检索。 MEMWALKER [13]同样采用递归方法，通过构建摘要记忆树来处理长文本。

### 段落 78 · Page 12

**EN**

The system navigates through this tree to retrieve relevant information, effectively breaking down complex queries into manageable segments, which is particularly useful for handling long-context question answering. IMRAG [ 150] introduces a multi-round retrieval mechanism, where each round of retrieval is based on the model’s internal monologues, progressively refining the search with each iteration. Selfmem [21] employs a selfmemory module, enabling the system to store and retrieve information recursively, building upon previously retrieved knowledge in a hierarchical manner.

**中文**

系统通过该树导航来检索相关信息，有效地将复杂的查询分解为可管理的部分，这对于处理长上下文问答特别有用。 IMRAG [150]引入了多轮检索机制，其中每轮检索都基于模型的内部独白，通过每次迭代逐步细化搜索。 Selfmem [21] 采用自记忆模块，使系统能够递归地存储和检索信息，以分层方式构建先前检索的知识。

### 段落 79 · Page 12

**EN**

This recursive strategy enhances the system’s ability to manage and integrate vast amounts of information across multiple retrieval iterations. Conditional Retrieval Strategy. Conditional retrieval strategies (Algorithm 3) are governed by specific conditions or rules, which may be predefined or dynamically determined during the process. This method ensures that retrieval aligns with specific constraints or criteria, enhancing relevance and specificity. It is particularly useful for compliance checking, rule-based recommendation systems, and context-sensitive information retrieval.

**中文**

这种递归策略增强了系统在多个检索迭代中管理和集成大量信息的能力。条件检索策略。条件检索策略（算法3）由特定条件或规则控制，这些条件或规则可以是预定义的或在过程中动态确定的。该方法确保检索符合特定的约束或标准，从而增强相关性和特异性。它对于合规性检查、基于规则的推荐系统和上下文相关信息检索特别有用。

### 段落 80 · Page 12

**EN**

PRCA [151] is a prime example, where retrieval strategies are adapted based on reward-driven adjustments, refining the context used by large language models to enhance precision and relevance. RARG [159] similarly emphasizes retrieval based on specific evidence conditions, ensuring that the retrieval process aligns with predefined requirements, which is critical for generating factual and polite responses. CRAG [149] adds another , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

PRCA [151] 就是一个典型的例子，其中检索策略根据奖励驱动的调整进行调整，细化大型语言模型使用的上下文以提高精度和相关性。 RARG [159]同样强调基于特定证据条件的检索，确保检索过程符合预定义的要求，这对于生成事实和礼貌的回复至关重要。 CRAG [149] 添加了另一个，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 13

### 段落 81 · Page 13

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 13 Algorithm 2 Recursive Retrieval Strategy in RAG Require: Initial Query 𝑞, Documents 𝐷, Maximum Depth𝐿, Retriever 𝑅, Generator𝐺, Pre-retrieval Function 𝐹𝑝𝑟𝑒 , Post-retrieval Function 𝐹𝑝𝑜𝑠𝑡 , Sub-query Generation Function 𝐹𝑠𝑢𝑏𝑞, Hierarchical Layer Building Function 𝐹𝑏𝑢𝑖𝑙𝑑 , Hierarchical Information Operating Function 𝐹ℎ𝑖𝑒𝑟 Ensure: Final Output 𝑦𝑓 𝑖𝑛𝑎𝑙 1: Build Hierarchical Layers (Pre-retrieval) 2: 𝐻𝑖𝑒𝑟𝑎𝑟𝑐ℎ𝑦 ← 𝐹𝑏𝑢𝑖𝑙𝑑 (𝑞) // Build hierarchical layers based on the initial query 3: Initialize 𝑙 ← 0 // Start depth counter from 0 4: Initialize 𝑆𝑢𝑏_𝑞𝑢𝑒𝑟𝑖𝑒𝑠 ← [ 𝑞] // Initial

**中文**

大语言模型中检索增强文本生成的综述 13 算法 2 RAG 中的递归检索策略 需要：初始查询𝑞、文档𝐷、最大深度𝐿、检索器𝑅、生成器𝐺、预检索函数𝐹𝑝𝑟𝑒、后检索函数𝐹𝑝𝑜𝑠𝑡、子查询生成函数𝐹𝑠𝑢𝑏𝑞、分层建层函数𝐹𝑏𝑢𝑖𝑙𝑑、分层信息操作函数𝐹ℎ𝑖𝑒𝑟 确保：最终输出𝑦𝑓 𝑖𝑛𝑎𝑙 1: 构建分层图层（预检索） 2: 𝐻𝑖𝑒𝑟𝑎𝑟𝑐ℎ𝑦 ← 𝐹𝑏𝑢𝑖𝑙𝑑 (𝑞) // 构建分层基于初始查询的层 3: 初始化 𝑙 ← 0 // 从 0 开始深度计数器 4: 初始化 𝑆𝑢𝑏_𝑞𝑢𝑒𝑟𝑖𝑒𝑠 ← [ 𝑞] // 初始

### 段落 82 · Page 13

**EN**

ize list of sub-queries 5: while 𝑙 ≤ 𝐿 do 6: for each 𝑞′ 𝑙 ∈ 𝑆𝑢𝑏_𝑞𝑢𝑒𝑟𝑖𝑒𝑠 do 7: Pre-retrieval Phase 8: 𝑞′ 𝑙 ← 𝐹ℎ𝑖𝑒𝑟 (𝐻𝑖𝑒𝑟𝑎𝑟𝑐ℎ𝑦, 𝑞 ′ 𝑙 ) // Adjust query based on hierarchical layers 9: 𝑞′ 𝑙 ← 𝐹𝑝𝑟𝑒 (𝑞′ 𝑙 ) // Query Manipulation, Indexing, and Data Modification 10: Retrieval Phase 11: 𝐷𝑙 ← 𝑅(𝑞′ 𝑙 , 𝐷) // Retrieve documents for the current sub-query 12: Post-retrieval Phase 13: 𝐷 ′ 𝑙 ← 𝐹𝑝𝑜𝑠𝑡 (𝑞′ 𝑙 , 𝐷𝑙 ) // Re-ranking and filtering to refine documents 14: Generation Phase 15: 𝑦𝑙 ← 𝐺 (𝑞′ 𝑙 , 𝐷′ 𝑙 ) // Generate output based on refined documents 16: Sub-query Generation (if needed) 17: if additional refinement needed based on 𝑦𝑙 then 18: 𝑆𝑢𝑏_𝑞𝑢𝑒𝑟𝑖𝑒𝑠

**中文**

调整子查询列表 5: while 𝑙 ≤ 𝐿 do 6: 对于每个𝑞′ 𝑙 ε 𝑆𝑢𝑏_𝑞𝑢𝑒𝑟𝑖𝑒𝑠 do 7: 预检索阶段 8: 𝑞′ 𝑙 ← 𝐹ℎ𝑖𝑒𝑟 (𝐻𝑖𝑒𝑟𝑎𝑟𝑐ℎ𝑦, 𝑞 ′ 𝑙 ) // 根据层级调整查询 9: 𝑞′ 𝑙 ← 𝐹𝑝𝑟𝑒 (𝑞′ 𝑙 ) // 查询操作、索引和数据修改 10: 检索阶段 11: 𝐷𝑙 ← 𝑅(𝑞′ 𝑙 , 𝐷) // 检索当前子查询的文档 12: 检索后阶段 13: 𝐷 ′ 𝑙 ← 𝐹𝑝𝑜𝑠𝑡 (𝑞′ 𝑙 , 𝐷𝑙 ) // 重新排序和过滤以细化文档 14: 生成阶段 15: 𝑦𝑙 ← 𝐺 (𝑞′ 𝑙 , 𝐷′ 𝑙 ) // 根据细化文档生成输出 16:子查询生成（如果需要） 17：如果需要基于𝑦𝑙进行额外细化，则 18：𝑆𝑢𝑏_𝑞𝑢𝑒𝑟𝑖𝑒𝑠

### 段落 83 · Page 13

**EN**

← 𝐹𝑠𝑢𝑏𝑞 (𝑦𝑙 ) // Generate new sub-queries based on current output 19: end if 20: end for 21: 𝑙 ← 𝑙 + 1 // Increment depth counter 22: end while 23: Final Synthesis 24: 𝑦𝑓 𝑖𝑛𝑎𝑙 ← SynthesizeResults({𝑦0, 𝑦1, .

**中文**

← 𝐹𝑠𝑢𝑏𝑞 (𝑦𝑙 ) // 根据当前输出生成新的子查询 19: end if 20: end for 21: 𝑙 ← 𝑙 + 1 // 递增深度计数器 22: end while 23: 最终综合 24: 𝑦𝑓 𝑖𝑛𝑎𝑙 ← SynthesizeResults({𝑦0, 𝑦1, .

### 段落 84 · Page 13

**EN**

. . , 𝑦𝑙 }) // Merge results 25: return 𝑦𝑓 𝑖𝑛𝑎𝑙 layer to this approach by incorporating a retrieval evaluator that assesses the quality of retrieved documents and triggers different actions based on confidence thresholds, ensuring that only the most relevant and accurate information is used in the generation process. Adaptive Retrieval Strategy. Adaptive retrieval (Algorithm 4) dynamically adjusts the retrieval strategy based on the context and nature of the query or the data retrieved so far.

**中文**

。。 , 𝑦𝑙 }) // 合并结果 25：通过合并检索评估器，将 𝑦𝑓 𝑖𝑛𝑎𝑙 层返回到此方法，该评估器评估检索文档的质量并根据置信度阈值触发不同的操作，确保在生成过程中仅使用最相关和最准确的信息。自适应检索策略。自适应检索（算法 4）根据查询或迄今为止检索的数据的上下文和性质动态调整检索策略。

### 段落 85 · Page 13

**EN**

This highly flexible method tailors retrieval approaches on-the-fly to optimize for relevance and precision, making it ideal for personalized search engines, adaptive learning systems, and real-time decision support. AAR [157] exemplifies adaptive retrieval by adjusting its strategy based on the preferences of LLMs, learning from a small source model and generalizing to unseen tasks. FLARE [65] takes a similar adaptive approach but focuses on dynamically fetching additional information when model confidence is low, thereby improving the relevance of generated responses.

**中文**

这种高度灵活的方法可以即时定制检索方法，以优化相关性和精度，使其成为个性化搜索引擎、自适应学习系统和实时决策支持的理想选择。 AAR [157] 通过根据 LLM 的偏好调整其策略、从小源模型学习并推广到未见过的任务来举例说明自适应检索。 FLARE [65] 采用类似的自适应方法，但重点是在模型置信度较低时动态获取附加信息，从而提高生成响应的相关性。

### 段落 86 · Page 13

**EN**

SelfRAG [4] goes further by incorporating self-reflective processes, where the retrieval strategy evolves based on critiques of the generated content. CoK [86], on the other hand, implements a dynamic mechanism that adjusts retrieval strategies based on the evolving needs of the task. The retrieval process in CoK is not static but adapts according to the specific scenario and the nature of the , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

SelfRAG [4] 更进一步，结合了自我反思过程，其中检索策略根据对生成内容的批评而发展。另一方面，CoK [86] 实现了一种动态机制，可以根据任务不断变化的需求调整检索策略。 CoK 中的检索过程不是静态的，而是根据具体场景和卷的性质进行调整。 1、第1条。出版日期：2018 年 8 月。

### Page 14

### 段落 87 · Page 14

14 Huang et al.

### 段落 88 · Page 14

**EN**

Algorithm 3 Conditional Retrieval Strategy in RAG Require: Query 𝑞, Documents 𝐷, Maximum Iterations 𝑁 , Retriever 𝑅, Generator 𝐺, Pre-retrieval Function 𝐹𝑝𝑟𝑒 , Post-retrieval Function 𝐹𝑝𝑜𝑠𝑡 , Condition Evaluation Function 𝐹𝑐𝑜𝑛𝑑 Ensure: Final Output 𝑦𝑓 𝑖𝑛𝑎𝑙 1: Initialize 𝑖 ← 1 // Start iteration counter 2: 𝑞′ ← 𝑞 // Initialize query 3: while 𝑖 ≤ 𝑁 do 4: Pre-retrieval Phase 5: 𝑞′ ← 𝐹𝑝𝑟𝑒 (𝑞′) // Perform query manipulation and data modification 6: Retrieval Phase 7: 𝐷𝑖 ← 𝑅(𝑞′, 𝐷) // Retrieve documents based on the current query 8: Post-retrieval Phase 9: 𝐷 ′ 𝑖 ← 𝐹𝑝𝑜𝑠𝑡 (𝑞′, 𝐷𝑖 ) // Re-rank and filter documents based on conditions 10: Generation Ph

**中文**

RAG中的算法3条件检索策略需要：查询𝑞、文档𝐷、最大迭代次数𝑁、检索器𝑅、生成器𝐺、预检索函数𝐹𝑝𝑟𝑒、后检索函数𝐹𝑝𝑜𝑠𝑡、条件评估函数 𝐹𝑐𝑜𝑛𝑑 确保：最终输出 𝑦𝑓 𝑖𝑛𝑎𝑙 1: 初始化 𝑖 ← 1 // 启动迭代计数器 2: 𝑞′ ← 𝑞 // 初始化查询 3: while 𝑖 ≤ 𝑁 do 4: 预检索阶段5: 𝑞′ ← 𝐹𝑝𝑟𝑒 (𝑞′) // 执行查询操作和数据修改 6: 检索阶段 7: 𝐷𝑖 ← 𝑅(𝑞′, 𝐷) // 根据当前查询检索文档 8: 检索后阶段 9: 𝐷 ′ 𝑖 ← 𝐹𝑝𝑜𝑠𝑡 (𝑞′, 𝐷𝑖 ) // 根据条件重新排序和过滤文档 10：生成 Ph

### 段落 89 · Page 14

**EN**

ase 11: 𝑦𝑖 ← 𝐺 (𝑞′, 𝐷′ 𝑖 ) // Generate output using the refined documents 12: Conditional Branching 13: if 𝐹𝑐𝑜𝑛𝑑 (𝑦𝑖, 𝐷′ 𝑖 ) is Condition A then 14: Apply Strategy A // e.g., refine the query based on feedback 15: else if 𝐹𝑐𝑜𝑛𝑑 (𝑦𝑖, 𝐷′ 𝑖 ) is Condition B then 16: Apply Strategy B // e.g., expand the scope or adjust parameters 17: else if 𝐹𝑐𝑜𝑛𝑑 (𝑦𝑖, 𝐷′ 𝑖 ) is Condition C then 18: Apply Strategy C // e.g., modify retrieval strategy or output processing 19: else 20: Continue without changes // If no conditions are met, proceed without adjustments 21: end if 22: Check Termination Condition 23: if 𝐹𝑐𝑜𝑛𝑑 (𝑦𝑖, 𝐷′ 𝑖 ) meets stopping criteria then 24:

**中文**

ase 11: 𝑦𝑖 ← 𝐺 (𝑞′, 𝐷′ 𝑖 ) // 使用精炼文档生成输出 12: 条件分支 13: if 𝐹𝑐𝑜𝑛𝑑 (𝑦𝑖, 𝐷′ 𝑖 ) 是条件 A then 14: 应用策略 A // 例如，根据反馈优化查询 15: else if 𝐹𝑐𝑜𝑛𝑑 (𝑦𝑖, 𝐷′ 𝑖 ) is Condition B then 16: Apply Strategy B // 例如，扩大范围或调整参数 17: else if 𝐹𝑐𝑜𝑛𝑑 (𝑦𝑖, 𝐷′ 𝑖 ) 是条件 C then 18: 应用策略 C // 例如，修改检索策略或输出处理 19: else 20: 继续而不做更改 // 如果不满足条件，则继续进行而不做调整 21: end if 22: 检查终止条件 23: if 𝐹𝑐𝑜𝑛𝑑 (𝑦𝑖, 𝐷′ 𝑖 ) 满足停止条件则 24：

### 段落 90 · Page 14

**EN**

BREAK // Exit the loop if the stopping condition is met 25: end if 26: 𝑖 ← 𝑖 + 1 // Increment iteration counter 27: end while 28: Final Synthesis 29: 𝑦𝑓 𝑖𝑛𝑎𝑙 ← SynthesizeResults({𝑦1, 𝑦2, .

**中文**

BREAK // 如果满足停止条件则退出循环 25: end if 26: 𝑖 ← 𝑖 + 1 // 递增迭代计数器 27: end while 28: 最终综合 29: 𝑦𝑓 𝑖𝑛𝑎𝑙 ← SynthesizeResults({𝑦1, 𝑦2, .

### 段落 91 · Page 14

**EN**

. . , 𝑦𝑖 }) // Merge results 30: return 𝑦𝑓 𝑖𝑛𝑎𝑙 information being accessed, making it highly effective for context-sensitive applications. DRAGIN [124] discusses a real-time dynamic retrieval mechanism that adapts to the evolving needs of the language model, ensuring that the retrieval strategy remains responsive and aligned with the immediate task requirements, thus optimizing the relevance and precision of the retrieved information. In summary, the choice of retrieval strategy within RAG depends on the specific requirements of the application at hand.

**中文**

。。 , 𝑦𝑖 }) // 合并结果 30: 返回正在访问的 𝑦𝑓 𝑖𝑛𝑎𝑙 信息，使其对于上下文相关的应用程序非常有效。 DRAGIN [124]讨论了一种实时动态检索机制，该机制适应语言模型不断变化的需求，确保检索策略保持响应性并与即时任务要求保持一致，从而优化检索信息的相关性和精度。总之，RAG 中检索策略的选择取决于当前应用程序的具体要求。

### 段落 92 · Page 14

**EN**

While basic retrieval strategies offer simplicity and efficiency, iterative retrieval is well-suited for tasks requiring detailed exploration and refinement. Recursive retrieval excels in managing hierarchical information, while adaptive retrieval provides flexibility in dynamic environments. Conditional retrieval ensures strict adherence to predefined criteria, making it indispensable in applications where compliance and specific constraints are critical. By carefully , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

虽然基本检索策略简单且高效，但迭代检索非常适合需要详细探索和细化的任务。递归检索擅长管理分层信息，而自适应检索则在动态环境中提供灵活性。条件检索可确保严格遵守预定义的标准，这使其在合规性和特定约束至关重要的应用程序中不可或缺。仔细地，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 15

### 段落 93 · Page 15

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 15 Algorithm 4 Adaptive Retrieval Strategy in RAG Require: Query 𝑞, Documents 𝐷, Maximum Iterations 𝑁 , Retriever 𝑅, Generator 𝐺, Pre-retrieval Function 𝐹𝑝𝑟𝑒 , Post-retrieval Function 𝐹𝑝𝑜𝑠𝑡 , Adaptive Adjustment Function 𝐹𝑎𝑑𝑎𝑝𝑡 , Feedback Function 𝐹𝑓 𝑒𝑒𝑑𝑏𝑎𝑐𝑘 Ensure: Final Output 𝑦𝑓 𝑖𝑛𝑎𝑙 1: Initialize 𝑖 ← 1 // Start iteration counter 2: 𝑞′, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ← 𝑞, ∅ // Initialize query and context 3: while 𝑖 ≤ 𝑁 do 4: Pre-retrieval Phase 5: 𝑞′, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ← 𝐹𝑝𝑟𝑒 (𝑞′, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ) // Query Manipulation, Indexing, Data Modification, and Context Setup 6: Dynamic Retrieval Phase 7: 𝐷𝑖 ← 𝑅(𝑞

**中文**

大语言模型中检索增强文本生成的综述 15 算法 4 RAG 中的自适应检索策略 要求：查询𝑞、文档𝐷、最大迭代次数𝑁、检索器𝑅、生成器𝐺、预检索函数𝐹𝑝𝑟𝑒、后检索函数𝐹𝑝𝑜𝑠𝑡，自适应调整功能 𝐹𝑎𝑑𝑎𝑝𝑡，反馈功能 𝐹𝑓 𝑒𝑒𝑑𝑏𝑎𝑐𝑘 确保：最终输出 𝑦𝑓 𝑖𝑛𝑎𝑙 1: 初始化 𝑖 ← 1 // 启动迭代计数器 2: 𝑞′, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ← 𝑞, ∅ // 初始化查询和上下文 3: while 𝑖 ≤ 𝑁 do 4: 预检索阶段5: 𝑞′, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ← 𝐹𝑝𝑟𝑒 (𝑞′, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ) // 查询操作、索引、数据修改和上下文设置 6: 动态检索阶段 7：𝐷𝑖 ← 𝑅(𝑞

### 段落 94 · Page 15

**EN**

′, 𝐷, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ) // Retrieve documents based on the current query and context 8: Adaptive Post-retrieval Phase 9: 𝐷 ′ 𝑖 ← 𝐹𝑝𝑜𝑠𝑡 (𝑞′, 𝐷𝑖, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ) // Re-ranking and filtering based on adaptive criteria 10: Generation Phase 11: 𝑦𝑖 ← 𝐺 (𝑞′, 𝐷′ 𝑖 , 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ) // Generate output using the refined documents 12: Adaptive Adjustment 13: if 𝐹𝑓 𝑒𝑒𝑑𝑏𝑎𝑐𝑘 (𝑦𝑖, 𝐷′ 𝑖 ) is negative then 14: 𝑞′, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ← 𝐹𝑎𝑑𝑎𝑝𝑡 (𝑞′, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡, 𝑦 𝑖, 𝐷′ 𝑖 ) // Dynamically adjust the query and context 15: end if 16: Feedback Integration 17: if 𝐹𝑓 𝑒𝑒𝑑𝑏𝑎𝑐𝑘 (𝑦𝑖 ) is positive then 18: BREAK // Stop iterations if output is satisfactory 19: end if 20: 𝑖 ← 𝑖 + 1 // Increment iteration co

**中文**

′, 𝐷, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ) // 根据当前查询和上下文检索文档 8: 自适应检索后阶段 9: 𝐷 ′ 𝑖 ← 𝐹𝑝𝑜𝑠𝑡 (𝑞′, 𝐷𝑖, 𝐶𝑜𝑛𝑡𝑒𝑥𝑡 ) // 根据自适应标准重新排序和过滤 10: 生成阶段 11: 𝑦𝑖 ← 𝐺 (𝑞′, 𝐷′ 𝑖 , ? 14：𝑞′，𝐶𝑜𝑛𝑡𝑒𝑥𝑡←𝐹𝑎𝑑𝑎𝑝𝑡（𝑞′，𝐶𝑜𝑛𝑡𝑒𝑥𝑡，𝑦𝑖， 𝐷′ 𝑖 ) // 动态调整查询和上下文 15: end if 16: 反馈集成 17: if 𝐹𝑓 𝑒𝑒𝑑𝑏𝑎𝑏𝑎𝑐𝑘 (𝑦𝑖 ) 为正 then 18: BREAK // 如果输出令人满意则停止迭代 19: end if 20: 𝑖 ← 𝑖 + 1 // 增量迭代 co

### 段落 95 · Page 15

**EN**

unter 21: end while 22: Final Synthesis 23: 𝑦𝑓 𝑖𝑛𝑎𝑙 ← SynthesizeResults({𝑦1, 𝑦2, .

**中文**

unter 21: 结束 while 22: 最终综合 23: 𝑦𝑓 𝑖𝑛𝑎𝑙 ← SynthesizeResults({𝑦1, 𝑦2, .

### 段落 96 · Page 15

**EN**

. . , 𝑦𝑖 }) // Merge results 24: return 𝑦𝑓 𝑖𝑛𝑎𝑙 selecting and combining these strategies, RAG systems can be tailored to effectively handle a wide range of information retrieval scenarios, leveraging the strengths of each approach to deliver robust and precise results. 5 Post-Retrieval 5.1 Re-Ranking As retrieval mechanisms often return a large number of potentially relevant documents, re-ranking methods are employed to reorder these documents, prioritizing those most likely to contribute meaningfully to the final output.

**中文**

。。 , 𝑦𝑖 }) // 合并结果 24: return 𝑦𝑓 𝑖𝑛𝑎𝑙 选择并组合这些策略，RAG 系统可以进行定制，以有效处理各种信息检索场景，利用每种方法的优势来提供稳健且精确的结果。 5 检索后 5.1 重新排序 由于检索机制经常返回大量潜在相关文档，因此采用重新排序方法对这些文档进行重新排序，优先考虑那些最有可能对最终输出做出有意义贡献的文档。

### 段落 97 · Page 15

**EN**

By leveraging various strategies, including unsupervised techniques, supervised learning, and data augmentation, re-ranking aims to optimize the alignment between the retrieved content and the desired response, thereby improving the overall effectiveness of RAG systems [165]. Unsupervised Re-ranking. Unsupervised re-rankers do not rely on labeled data for training. They use strategies such as pointwise, listwise, or pairwise methods to rank documents based on LLM outputs without the need for supervised fine-tuning. For example, In-Context RALM [112] employs , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

通过利用各种策略，包括无监督技术、监督学习和数据增强，重排旨在优化检索内容和所需响应之间的一致性，从而提高 RAG 系统的整体有效性[165]。无监督重排。无监督重排序不依赖标记数据进行训练。他们使用逐点、列表或成对方法等策略根据 LLM 输出对文档进行排名，而无需监督微调。例如，In-Context RALM [112] 采用，Vol.1。 1、第1条。出版日期：2018 年 8 月。

### Page 16

### 段落 98 · Page 16

**EN**

16 Huang et al. a zero-shot approach where an off-the-shelf language model is used to re-rank the top-k documents retrieved by a BM25 retriever. This process involves selecting the document that maximizes the likelihood of the generated text, effectively using the LM’s semantic understanding to improve document relevance without requiring additional supervised training. The paper also explores training a dedicated re-ranker using self-supervised learning to further enhance the selection of relevant documents, demonstrating that training a re-ranker with domain-specific data can be more effective than zero-shot re-ranking.

**中文**

16 黄等人。一种零样本方法，其中使用现成的语言模型对 BM25 检索器检索到的前 k 个文档进行重新排序。这个过程涉及选择最大化生成文本的可能性的文档，有效地使用 LM 的语义理解来提高文档相关性，而不需要额外的监督训练。该论文还探讨了使用自监督学习来训练专用的重新排序器，以进一步增强相关文档的选择，证明使用特定领域的数据训练重新排序器可以比零样本重新排序更有效。

### 段落 99 · Page 16

**EN**

Supervised Re-ranking. Supervised re-rankers involve fine-tuning LLMs on specific ranking datasets. This category can be further divided into models like BERT that process query-document pairs to compute relevance scores, models like T5 that treat ranking as a generation task and use generated tokens to determine relevance, and models like RankLLaMA [ 95] that employ a prompt-based approach, focusing on the last token’s representation for relevance calculation [165].

**中文**

监督重排。有监督的重排涉及在特定排名数据集上微调法学硕士。这一类别可以进一步分为 BERT 等模型，处理查询文档对以计算相关性分数；T5 等模型，将排名视为生成任务并使用生成的标记来确定相关性；以及 RankLLaMA [95] 等模型，采用基于提示的方法，重点关注最后一个标记的表示以进行相关性计算 [165]。

### 段落 100 · Page 16

**EN**

For instance, the re-ranker in Re2G [40] is based on a BERT model trained on labeled data (such as MS MARCO) and fine-tuned to improve the relevance ranking of retrieved documents. FiD-Light [47] employs a supervised approach where the model is fine-tuned on specific datasets to learn how to re-rank passages effectively using source pointers during autoregressive text generation. The model uses a listwise auto-regressive re-ranking mechanism, trained to identify and re-rank relevant passages based on the output generated during the text generation process.

**中文**

例如，Re2G [40] 中的重排序器基于在标记数据（例如 MS MARCO）上训练的 BERT 模型，并进行微调以提高检索文档的相关性排序。 FiD-Light [47] 采用监督方法，在特定数据集上对模型进行微调，以学习如何在自回归文本生成过程中使用源指针有效地对段落进行重新排序。该模型使用列表式自回归重新排序机制，经过训练，可以根据文本生成过程中生成的输出来识别相关段落并重新排序。

### 段落 101 · Page 16

**EN**

GenRT [148] utilizes a combination of an encoder to capture global list-level features and a sequential decoder to reorder documents based on relevance. The model is trained to learn relevance scores through supervised learning, guided by labeled relevance data, ensuring that the most pertinent documents are prioritized in the final reranked list. Furthermore, ITER-RETGEN [121] proposes using a more capable re-ranker, which has access to model generations, to distill knowledge into a dense retriever.

**中文**

GenRT [148]利用编码器和顺序解码器的组合来捕获全局列表级特征，并根据相关性对文档进行重新排序。该模型经过训练，可以在标记的相关性数据的指导下，通过监督学习来学习相关性分数，确保最相关的文档在最终的重新排序列表中得到优先排序。此外，ITER-RETGEN [121] 提出使用更强大的重新排序器，它可以访问模型生成，将知识提炼到密集的检索器中。

### 段落 102 · Page 16

**EN**

This knowledge distillation process optimizes the query encoder of the dense retriever, enabling it to better capture the semantic relevance of documents relative to the task input. Data Augmentation for Re-ranking. Data augmentation for re-rankers focuses on enhancing the training process by generating additional training data, such as pseudo-relevance labels, using LLMs. This data augmentation provides more varied training examples, which helps improve the performance of re-ranking models.

**中文**

这种知识蒸馏过程优化了密集检索器的查询编码器，使其能够更好地捕获文档相对于任务输入的语义相关性。用于重排的数据增强。重新排序器的数据增强侧重于通过使用 LLM 生成额外的训练数据（例如伪相关标签）来增强训练过程。这种数据增强提供了更多样的训练示例，有助于提高重新排序模型的性能。

### 段落 103 · Page 16

**EN**

For example, DKS-RAC [53] introduces methods like Dense Knowledge Similarity (DKS) and Retriever as Answer Classifier (RAC), which focus on improving the retrieval process by incorporating rich answer encodings. These methods involve generating additional training signals or utilizing enriched data representations to improve the retrieval and ranking of documents. Additionally, the PROMPTAGATOR [27] framework utilizes synthetic data generated through LLM-based query generation to enhance the training of the reranker.

**中文**

例如，DKS-RAC [53] 引入了密集知识相似性（DKS）和检索器作为答案分类器（RAC）等方法，其重点是通过合并丰富的答案编码来改进检索过程。这些方法涉及生成额外的训练信号或利用丰富的数据表示来改进文档的检索和排名。此外，PROMPTAGATOR [27] 框架利用通过基于 LLM 的查询生成生成的合成数据来增强重新排序器的训练。

### 段落 104 · Page 16

**EN**

This data augmentation approach allows the re-ranker to refine candidate passages more effectively, using a cross-attention model trained on these additional examples to boost retrieval accuracy. 5.2 Filtering Filtering and re-ranking are distinct processes in the post-retrieval stage of RAG systems. Filtering focuses on eliminating irrelevant or low-quality documents from the retrieved set, thereby reducing the document set size and improving efficiency and effectiveness in subsequent processing.

**中文**

这种数据增强方法允许重新排序器更有效地细化候选段落，使用在这些附加示例上训练的交叉注意力模型来提高检索准确性。 5.2 过滤 过滤和重新排序是 RAG 系统检索后阶段的不同过程。过滤的重点是从检索集中消除不相关或低质量的文档，从而减小文档集的大小并提高后续处理的效率和效果。

### 段落 105 · Page 16

**EN**

In contrast, re-ranking orders the remaining documents based on their relevance or utility for the task, often prioritizing those that enhance the quality of the generated output, especially in responseaware scenarios. Several filtering methods have been developed to refine document sets in RAG systems, each with unique mechanisms but sharing common goals of improving relevance and reducing computational load. Self-RAG [4] employs a self-reflection mechanism, utilizing special “reflection tokens” , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

相比之下，根据其余文档对任务的相关性或实用性重新排序，通常会优先考虑那些提高生成输出质量的文档，尤其是在响应感知场景中。已经开发了几种过滤方法来细化 RAG 系统中的文档集，每种方法都有独特的机制，但都有提高相关性和减少计算负载的共同目标。 Self-RAG [4] 采用自我反思机制，利用特殊的“反思令牌”，Vol. 1、第1条。出版日期：2018 年 8 月。

### Page 17

### 段落 106 · Page 17

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 17 generated by the model to evaluate the relevance and quality of retrieved passages and the model’s own generated outputs. This self-reflection ensures that only the most pertinent documents are retained, leveraging the model’s internal capabilities without relying on external models during inference. Similarly, BlendFilter [135] utilizes the LLM itself as the filter, assessing and removing irrelevant or less useful documents by applying filtering separately to knowledge retrieved from original, externally augmented, and internally augmented queries.

**中文**

大型语言模型中检索增强文本生成的调查 17 由模型生成，用于评估检索到的段落以及模型自身生成的输出的相关性和质量。这种自我反思确保只保留最相关的文档，在推理过程中利用模型的内部功能，而不依赖外部模型。类似地，BlendFilter [135] 利用 LLM 本身作为过滤器，通过分别对从原始、外部增强和内部增强查询检索的知识应用过滤来评估和删除不相关或不太有用的文档。

### 段落 107 · Page 17

**EN**

Both Self-RAG and BlendFilter highlight the model’s intrinsic ability to perform filtering, reducing the need for additional models and enhancing computational efficiency. In contrast, RECOMP [ 147] and CRAG [ 149] employ more external or structural strategies. RECOMP focuses on selective augmentation, where summaries generated from retrieved documents are selectively prepended to the input for the language model. If the retrieved documents are deemed irrelevant, the compressor can generate an empty summary, effectively filtering out unnecessary information.

**中文**

Self-RAG 和 BlendFilter 都强调了模型执行过滤的内在能力，减少了对额外模型的需求并提高了计算效率。相比之下，RECOMP [147] 和 CRAG [149] 采用更多的外部或结构策略。 RECOMP 专注于选择性增强，其中从检索到的文档生成的摘要被选择性地添加到语言模型的输入之前。如果检索到的文档被认为不相关，压缩器可以生成一个空的摘要，从而有效地过滤掉不必要的信息。

### 段落 108 · Page 17

**EN**

This method allows for a dynamic approach to filtering, where only helpful content is retained. CRAG, on the other hand, uses a decompose-then-recompose approach, where retrieved documents are split into finer knowledge strips. These strips are evaluated for relevance using a finetuned T5 model, and only the relevant strips are recomposed to form a refined set of information for the generation task. This granular filtering process ensures that the final document set is both relevant and concise, tailored specifically to the generation task. Dynamic filtering techniques are also employed in methods like FiD-TF [ 5] and CoK [ 86].

**中文**

此方法允许采用动态过滤方法，仅保留有用的内容。另一方面，CRAG 使用分解然后重组的方法，将检索到的文档分割成更精细的知识条。使用微调的 T5 模型评估这些条带的相关性，并且仅重新组合相关条带以形成用于生成任务的精炼信息集。这种粒度过滤过程确保最终文档集既相关又简洁，专门针对生成任务而定制。 FiD-TF [5] 和 CoK [86] 等方法中也采用了动态滤波技术。

### 段落 109 · Page 17

**EN**

FiD-TF introduces Token Filtering during the decoding process, where less relevant tokens are dynamically filtered out based on cross-attention scores. This approach reduces the computational load by eliminating tokens deemed uninformative for generating the final answer, enhancing efficiency with minimal impact on performance. CoK employs a filtering technique based on self-consistency, identifying and processing only those questions with “uncertain” answers. This method works by sampling various reasoning paths and answers, preserving only predictions with high consistency.

**中文**

FiD-TF 在解码过程中引入了 Token Filtering，根据交叉注意力分数动态过滤掉不太相关的 token。这种方法通过消除被认为对于生成最终答案无信息的标记来减少计算负载，从而在对性能影响最小的情况下提高效率。 CoK 采用基于自我一致性的过滤技术，仅识别和处理那些答案“不确定”的问题。该方法的工作原理是对各种推理路径和答案进行采样，仅保留高度一致性的预测。

### 段落 110 · Page 17

**EN**

Questions that do not meet the specified consistency threshold undergo further processing, effectively preventing the propagation of errors in the generation process. Finally, FILCO [141] implements a comprehensive filtering approach using three distinct strategies: String Inclusion (STRINC) to match exact outputs, Lexical Overlap to measure word-level similarity, and Conditional Cross-Mutual Information (CXMI) to assess how much the context improves output likelihood. FILCO applies these filtering strategies at the sentence level, refining the retrieved content for better relevance.

**中文**

不满足指定一致性阈值的问题将受到进一步处理，有效防止生成过程中错误的传播。最后，FILCO [141] 使用三种不同的策略实现了全面的过滤方法：字符串包含（STRINC）来匹配精确的输出，词汇重叠来测量单词级相似性，以及条件交叉互信息（CXMI）来评估上下文对输出可能性的改善程度。 FILCO 在句子级别应用这些过滤策略，细化检索到的内容以获得更好的相关性。

### 段落 111 · Page 17

**EN**

Additionally, FILCO trains a context filtering model using these strategies, which predicts the most useful context at inference time, thereby enhancing the accuracy and relevance of the generation model’s output. 6 Generation 6.1 Enhancing Enhancing methods are strategies aimed at improving the quality and relevance of generated outputs by integrating retrieved content in various ways. These methods differ in how they combine, aggregate, or refine retrieved information, offering multiple approaches to enrich the final output.

**中文**

此外，FILCO 使用这些策略训练上下文过滤模型，该模型可以预测推理时最有用的上下文，从而提高生成模型输出的准确性和相关性。 6 生成 6.1 增强 增强方法是旨在通过以各种方式整合检索到的内容来提高生成输出的质量和相关性的策略。这些方法的不同之处在于如何组合、聚合或提炼检索到的信息，提供多种方法来丰富最终输出。

### 段落 112 · Page 17

**EN**

Broadly, these techniques can be grouped into three categories: enhancing with queries, enhancing with ensemble approaches, and enhancing with feedback loops. Enhance with Query. This approach integrates the retrieved documents with the original query, enabling the generator to leverage both sources in producing the final output. By combining the query with the retrieved content, the generation process ensures that the response remains closely aligned with the user’s intent while being enriched by relevant information.

**中文**

从广义上讲，这些技术可以分为三类：通过查询增强、通过集成方法增强以及通过反馈循环增强。通过查询增强。这种方法将检索到的文档与原始查询集成在一起，使生成器能够利用这两个来源来生成最终输出。通过将查询与检索到的内容相结合，生成过程可确保响应与用户的意图保持紧密一致，同时通过相关信息进行丰富。

### 段落 113 · Page 17

**EN**

The focus here is on the seamless fusion of the query and context, allowing the generated output to maintain both relevance , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

这里的重点是查询和上下文的无缝融合，允许生成的输出保持相关性，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 18

### 段落 114 · Page 18

**EN**

18 Huang et al. and completeness. For instance, the RETRO [9] model enhances generation by integrating retrieved text chunks with the user’s query using a chunked cross-attention mechanism, where relevant information from the retrieved neighbors is directly injected into the generation process. This method involves first retrieving similar document chunks based on the query and then using a crossattention module to align and combine these chunks with the input sequence during generation. In-Context RALM [112] takes a comparable approach, directly prepending the retrieved documents to the input query.

**中文**

18 黄等人。和完整性。例如，RETRO [9] 模型通过使用分块交叉注意机制将检索到的文本块与用户的查询集成来增强生成，其中来自检索到的邻居的相关信息直接注入到生成过程中。该方法首先根据查询检索相似的文档块，然后在生成过程中使用交叉注意模块将这些块与输入序列对齐和组合。 In-Context RALM [112] 采用类似的方法，直接将检索到的文档添加到输入查询中。

### 段落 115 · Page 18

**EN**

In this way, the language model can generate responses conditioned on both the query and the retrieved content without requiring changes to the model’s architecture. Both examples illustrate a straightforward yet effective method: concatenating the query and retrieved documents into a single input sequence that the LLMs process together, yielding outputs that are contextually enhanced. Enhance with Ensemble. When multiple sources are synthesized, the generation process can achieve a more coherent and well-rounded response.

**中文**

通过这种方式，语言模型可以根据查询和检索的内容生成响应，而无需更改模型的架构。这两个例子都说明了一种简单而有效的方法：将查询和检索到的文档连接到一个输入序列中，由法学硕士一起处理，产生上下文增强的输出。通过 Ensemble 进行增强。当多个源被合成时，生成过程可以实现更加连贯和全面的响应。

### 段落 116 · Page 18

**EN**

Rather than relying solely on a single source, this approach aggregates information from various documents, allowing the generator to reconcile conflicting details, blend diverse perspectives, and select the most reliable or comprehensive output. The ensemble process can manifest in different ways: it may involve combining insights from several sources into a unified narrative, or generating multiple candidate outputs and choosing the best one based on criteria like consistency, relevance, or factual accuracy.

**中文**

这种方法不是仅仅依赖于单一来源，而是聚合来自各种文档的信息，使生成器能够协调冲突的细节，融合不同的观点，并选择最可靠或最全面的输出。集成过程可以以不同的方式体现：它可能涉及将多个来源的见解组合成一个统一的叙述，或者生成多个候选输出并根据一致性、相关性或事实准确性等标准选择最佳输出。

### 段落 117 · Page 18

**EN**

An instance of this strategy is seen in FiD [58], which encodes multiple retrieved passages independently before fusing them in the decoder to create a coherent answer. By treating each passage separately during encoding and then merging them during decoding, the model effectively combines evidence from multiple sources. Meanwhile, in REPLUG [ 122], an ensemble approach is adopted where each retrieved document is independently prepended to the query and processed separately. The outputs are then aggregated, with relevance scores guiding the weighting of each document’s contribution.

**中文**

FiD [58] 就是这种策略的一个例子，它对多个检索到的段落进行独立编码，然后将它们融合到解码器中以创建连贯的答案。通过在编码过程中单独处理每个段落，然后在解码过程中合并它们，该模型有效地结合了来自多个来源的证据。同时，在 REPLUG [122] 中，采用了一种集成方法，其中每个检索到的文档都独立地添加到查询中并单独处理。然后汇总输出，并用相关性分数指导每个文档贡献的权重。

### 段落 118 · Page 18

**EN**

Through this process, the model capitalizes on diverse information across several sources, leading to improvements in answer accuracy, coverage, and scalability as more data becomes available. Enhance with Feedback. In contrast to approaches that process retrieved information in a single pass, this method introduces iterative refinement into the generation process by incorporating feedback loops. Initially, the generator produces a draft response, which is then evaluated and adjusted based on feedback mechanisms, such as self-reflection or predefined criteria focused on factual accuracy and fluency.

**中文**

通过这个过程，该模型利用多个来源的不同信息，随着更多数据的可用，从而提高答案的准确性、覆盖范围和可扩展性。通过反馈增强。与单次处理检索到的信息的方法相比，该方法通过合并反馈循环将迭代细化引入到生成过程中。最初，生成器生成一个草稿响应，然后根据反馈机制（例如自我反思或注重事实准确性和流畅性的预定义标准）对其进行评估和调整。

### 段落 119 · Page 18

**EN**

This iterative approach aims to incrementally improve the output by identifying and correcting errors or fine-tuning content to better align with quality standards, ultimately producing a polished and reliable response. PRCA [151] offers an example by positioning itself between the retriever and generator, distilling retrieved information based on feedback from the generator. This distilled information serves as a reward model to guide context optimization, leveraging reinforcement learning and metrics like ROUGE-L scores to iteratively refine which details should be emphasized or downplayed.

**中文**

这种迭代方法旨在通过识别和纠正错误或微调内容以更好地符合质量标准来逐步改进输出，最终产生完善且可靠的响应。 PRCA [151] 提供了一个例子，将自身定位在检索器和生成器之间，根据生成器的反馈提取检索到的信息。这些经过提炼的信息可作为奖励模型来指导上下文优化，利用强化学习和 ROUGE-L 分数等指标来迭代地细化应强调或淡化哪些细节。

### 段落 120 · Page 18

**EN**

DSP [73], on the other hand, refines both queries and retrieved passages through a multi-hop retrieval process that incorporates programmatically bootstrapped feedback. Here, the language model generates intermediate queries, retrieves relevant passages, and updates the context in subsequent steps—each stage building on the last to refine the final output. Feedback-driven enhancements are also evident in models like Selfmem [21], which focus on generating self-memory. The model first produces an unbounded pool of outputs and then selects the most relevant one as memory for the next generation, guided by metrics like BLEU or ROUGE.

**中文**

另一方面，DSP [73]通过结合了编程引导反馈的多跳检索过程来完善查询和检索的段落。在这里，语言模型生成中间查询，检索相关段落，并在后续步骤中更新上下文——每个阶段都建立在最后一个阶段的基础上，以完善最终输出。反馈驱动的增强在 Selfmem [21] 等模型中也很明显，该模型专注于生成自我记忆。该模型首先生成一个无限的输出池，然后在 BLEU 或 ROUGE 等指标的指导下选择最相关的输出作为下一代的内存。

### 段落 121 · Page 18

**EN**

Finally, RECITE [ 122] integrates feedback by generating multiple recitations from the model’s internal knowledge and using self-consistency techniques to aggregate the outputs. By introducing diversity in the recitations and leveraging passage hints during generation, this approach selects the best content through majority voting. Together, these methods demonstrate , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

最后，RECITE [122]通过从模型的内部知识生成多个背诵并使用自洽技术来聚合输出来整合反馈。通过引入背诵的多样性并在生成过程中利用段落提示，这种方法通过多数投票选择最佳内容。这些方法共同证明了，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 19

### 段落 122 · Page 19

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 19 how feedback loops and iterative refinements can lead to outputs that are not only more accurate but also increasingly coherent and contextually grounded as they evolve. 6.2 Customization Customization focuses on tailoring content to the user’s personality and needs. It involves adjusting the output either to align with specific knowledge retrieved during earlier stages (content alignment) or to adapt the generated response to meet the user’s preferences, context, or audience needs (contextual adaptation).

**中文**

大型语言模型中检索增强文本生成的调查 19 反馈循环和迭代改进如何导致输出不仅更准确，而且随着它们的发展而变得越来越连贯和基于上下文。 6.2 定制 定制侧重于根据用户的个性和需求定制内容。它涉及调整输出以与早期阶段检索到的特定知识保持一致（内容对齐）或调整生成的响应以满足用户的偏好、上下文或受众需求（上下文适应）。

### 段落 123 · Page 19

**EN**

In LAPDOG [52], customization is achieved primarily through content alignment by integrating persona profiles with external stories to enrich the context used for generation. The story retriever identifies relevant narratives based on the persona, expanding the limited profiles with additional information. The generator then combines this enriched knowledge with the dialogue history, ensuring that responses align closely with the persona’s traits and background. This approach allows for a nuanced understanding of the user’s personality, making the output more engaging and contextually appropriate.

**中文**

在 LAPDOG [52] 中，定制主要是通过内容对齐来实现的，通过将角色配置文件与外部故事集成来丰富用于生成的上下文。故事检索器根据角色识别相关叙述，用附加信息扩展有限的配置文件。然后，生成器将这些丰富的知识与对话历史相结合，确保响应与角色的特征和背景紧密结合。这种方法可以对用户的个性进行细致入微的了解，从而使输出更具吸引力且更适合上下文。

### 段落 124 · Page 19

**EN**

On the other hand, PersonaRAG [160] emphasizes real-time adaptation by customizing generated content based on dynamic user profiles, session behavior, and ongoing feedback. A multi-agent system continuously analyzes user interactions to refine responses, ensuring alignment with the user’s preferences and context. By integrating personalized insights at each step, the system can adjust its output to suit specific informational needs and situational contexts. This level of responsiveness allows the system to evolve in line with the user’s changing requirements, creating more relevant and targeted responses.

**中文**

另一方面，PersonaRAG [160] 强调通过根据动态用户配置文件、会话行为和持续反馈定制生成的内容来进行实时适应。多代理系统不断分析用户交互以完善响应，确保与用户的偏好和上下文保持一致。通过在每个步骤中集成个性化见解，系统可以调整其输出以适应特定的信息需求和情境。这种级别的响应能力使系统能够根据用户不断变化的需求而发展，从而创建更相关和更有针对性的响应。

### 段落 125 · Page 19

**EN**

ERAGent [123] also focuses on customization but through the use of a Personalized LLM Reader, which adapts responses using user-specific profiles. This module integrates rewritten questions, filtered knowledge, and user preferences to tailor responses according to both content relevance and user needs. For instance, it takes into account preferences like environmental consciousness or dietary restrictions, ensuring that the generated content is not only aligned with retrieved knowledge but also personalized to the user’s particular values and requirements.

**中文**

ERAGent [123] 也专注于定制，但通过使用个性化 LLM 阅读器，该阅读器使用特定于用户的配置文件来调整响应。该模块集成了重写的问题、过滤的知识和用户偏好，以根据内容相关性和用户需求定制响应。例如，它考虑了环境意识或饮食限制等偏好，确保生成的内容不仅与检索到的知识一致，而且根据用户的特定价值观和要求进行个性化。

### 段落 126 · Page 19

**EN**

This deep level of customization ensures that the output is both relevant and personally meaningful, enhancing user engagement. ROPG [118] proposes a dynamic pre- and post-generation retriever selection model, enhancing personalization by aligning the retrieval process with both the input context and the user’s preferences. The pre-generation model determines which retrieval strategy—such as recency-based, keyword matching, or semantic retrieval—is most appropriate before generation begins.

**中文**

这种深度定制可确保输出既相关又对个人有意义，从而增强用户参与度。 ROPG [118]提出了一种动态的生成前和生成后检索器选择模型，通过将检索过程与输入上下文和用户偏好保持一致来增强个性化。预生成模型在生成开始之前确定最合适的检索策略（例如基于新近度、关键字匹配或语义检索）。

### 段落 127 · Page 19

**EN**

By tailoring the retrieval process in this way, the model ensures that the documents retrieved from the user profile closely match the current input, thereby aligning the content with relevant user-specific knowledge. Following this, the post-generation model evaluates the outputs generated by different retrieval strategies and selects the most personalized result. This selection is guided by feedback from the generated content, which is then used to adjust future retrievals.

**中文**

通过以这种方式定制检索过程，该模型确保从用户配置文件中检索的文档与当前输入紧密匹配，从而使内容与相关的用户特定知识保持一致。接下来，后生成模型评估不同检索策略生成的输出并选择最个性化的结果。这种选择是由生成内容的反馈引导的，然后用于调整未来的检索。

### 段落 128 · Page 19

**EN**

By combining content alignment (through pre-generation retrieval) with contextual adaptation (through post-generation evaluation), this approach offers a comprehensive solution for customization within RAG. 7 Evaluation in RAG To assess how effectively language models can generate more accurate, relevant, and robust responses by leveraging external knowledge, the evaluation of RAG systems has emerged as a crucial research focus.

**中文**

通过将内容对齐（通过生成前检索）与上下文适应（通过生成后评估）相结合，该方法为 RAG 内的定制提供了全面的解决方案。 7 RAG 中的评估 为了评估语言模型如何通过利用外部知识有效地生成更准确、相关和稳健的响应，RAG 系统的评估已成为一个重要的研究重点。

### 段落 129 · Page 19

**EN**

Given the rising popularity of dialogue-based interactions, much recent work has concentrated on evaluating RAG models’ performance on such downstream tasks using established metrics like Exact Match (EM) and F1 scores. These metrics have been applied across a , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

鉴于基于对话的交互越来越受欢迎，最近的许多工作都集中在使用精确匹配 (EM) 和 F1 分数等既定指标来评估 RAG 模型在此类下游任务上的性能。这些指标已应用于整个卷。 1、第1条。出版日期：2018 年 8 月。

### Page 20

### 段落 130 · Page 20

20 Huang et al.

### 段落 131 · Page 20

**EN**

Evaluation Framework Aspects Methods Metrics Datasets RAGAS [33] Quality of RAG Systems Context Relevance Extracted Sentences / Total Sentences WikiEval7Answer Relevance Average Cosine Similarity Faithfulness Supported Statements / Total Statements ARES [117] Improving RAGAS Context Relevance Confidence Intervals KILT [109]SuperGLUE [134]Answer Relevance Answer Faithfulness RECALL [91] Counterfactual Robustness Response Quality Accuracy (QA)BLEU, ROUGE-L (Generation)EventKG [41]UJ [50]Robustness Misleading Rate (QA)Mistake Reappearance Rate (Generation) RGB [14] Impact of RAG on LLMs Noise Robustness Accuracy Synthetic Negative Rejection Reje

**中文**

评估框架 方面 方法 指标 数据集 RAGAS [33] RAG 系统的质量 上下文相关性 提取的句子/总句子 WikiEval7Answer 相关性 平均余弦相似度 可信度 支持的语句/总语句 ARES [117] 提高 RAGAS 上下文相关性 置信区间 KILT [109]SuperGLUE [134]答案相关性 答案忠实回忆 [91] 反事实鲁棒性响应质量准确度 (QA)BLEU、ROUGE-L（生成）EventKG [41]UJ [50]鲁棒性误导率 (QA) 错误重现率（生成） RGB [14] RAG 对 LLM 的影响 噪声鲁棒性准确度 合成阴性拒绝拒绝

### 段落 132 · Page 20

**EN**

ction Rate Information Integration Accuracy Counterfactual RobustnessError Detection RateError Correction Rate MIRAGE [144] RAG in Medical QA Zero-Shot Learning Accuracy MMLU-Med [45]MedQA-US [66]MedMCQA [105]PubMedQA [67]BioASQ-Y/N [132] Multi-Choice Evaluation Retrieval-Augmented Generation Question-Only Retrieval eRAG [119] Retrieval Quality in RAG Downstream Task Accuracy, ROUGE KILTSet-based Precision, Recall, Hit Rate Ranking MAP, MRR, NDCG BERGEN [114] Standardizing RAG ExperimentsSurface-Based EM, F1, Precision, Recall QA Datasets [69, 76]Semantic BEM [11], LLMeval [114] Table 1.

**中文**

动作率信息集成准确度反事实鲁棒性错误检测率错误纠正率 MIRAGE [144] 医学 QA 中的 RAG 零样本学习准确度 MMLU-Med [45]MedQA-US [66]MedMCQA [105]PubMedQA [67]BioASQ-Y/N [132] 多选评估检索增强生成仅限问题检索 eRAG [119] RAG 下游任务准确性中的检索质量、基于 ROUGE KILT 集的精度、召回率、命中率排名 MAP、MRR、NDCG BERGEN [114] 标准化 RAG 实验基于表面的 EM、F1、精度、召回率 QA 数据集 [69, 76] 语义 BEM [11]、LLMeval [114]表 1.

### 段落 133 · Page 20

**EN**

The Comparison of Different RAG Evaluation Frameworks. wide array of datasets, including TriviaQA [69], HotpotQA [153], FEVER [129], Natural Questions (NQ) [76], Wizard of Wikipedia (WoW) [30], and T-REX [32], which are often used to benchmark the effectiveness of retrieval and generation components in knowledge-intensive tasks. While downstream task evaluations provide valuable insights, they fail to address the multifaceted challenges that arise as RAG systems continue to evolve.

**中文**

不同RAG评估框架的比较。广泛的数据集，包括 TriviaQA [69]、HotpotQA [153]、FEVER [129]、Natural Questions (NQ) [76]、Wizard of Wikipedia (WoW) [30] 和 T-REX [32]，这些数据集通常用于对知识密集型任务中检索和生成组件的有效性进行基准测试。虽然下游任务评估提供了有价值的见解，但它们无法解决随着 RAG 系统不断发展而出现的多方面挑战。

### 段落 134 · Page 20

**EN**

To fill this gap, recent research has proposed various frameworks and benchmarks that aim to evaluate these systems from multiple perspectives, considering not only the quality of the generated text but also the relevance of retrieved documents and the system’s resilience to misinformation, as shown in Table 1. These evaluations include metrics that assess noise robustness, negative prompting, information integration, and counterfactual robustness, all of which reflect the complex challenges RAG systems face in realworld applications.

**中文**

为了填补这一空白，最近的研究提出了各种框架和基准，旨在从多个角度评估这些系统，不仅考虑生成文本的质量，还考虑检索文档的相关性以及系统对错误信息的恢复能力，如表 1 所示。这些评估包括评估噪声稳健性、负面提示、信息集成和反事实稳健性的指标，所有这些都反映了 RAG 系统在现实应用中面临的复杂挑战。

### 段落 135 · Page 20

**EN**

The ongoing development of comprehensive evaluation frameworks and metrics is essential for advancing the field, broadening the applicability of RAG systems, and ensuring that they meet the demands of an increasingly dynamic and complex information landscape [154]. 7.1 Retrieval-based Aspect In information retrieval, standard metrics such as Mean Average Precision (MAP), Precision, Reciprocal Rank, and Normalized Discounted Cumulative Gain (NDCG) [103, 110, 115] have traditionally been used to evaluate the relevance of retrieved documents to a given query.

**中文**

综合评估框架和指标的持续开发对于推进该领域、扩大 RAG 系统的适用性并确保它们满足日益动态和复杂的信息环境的需求至关重要 [154]。 7.1 基于检索的方面 在信息检索中，传统上使用平均精度（MAP）、精度、倒数排名和归一化贴现累积增益（NDCG）[103、110、115]等标准指标来评估检索到的文档与给定查询的相关性。

### 段落 136 · Page 20

**EN**

These metrics are essential in assessing the effectiveness of traditional information retrieval systems, where the primary goal is to measure how well the retrieved documents match the user’s query. When applied to RAG systems, these retrieval-based metrics extend their focus to consider how the retrieved information contributes to the quality of the generated output. In this context, Accuracy becomes a crucial metric, assessing how precisely the retrieved documents provide correct information for answering queries.

**中文**

这些指标对于评估传统信息检索系统的有效性至关重要，其主要目标是衡量检索到的文档与用户查询的匹配程度。当应用于 RAG 系统时，这些基于检索的指标将其重点扩展到考虑检索的信息如何对生成的输出的质量做出贡献。在这种情况下，准确性成为一个关键指标，用于评估检索到的文档为回答查询提供正确信息的精确程度。

### 段落 137 · Page 20

**EN**

Additionally, Rejection Rate [14], which measures the system’s ability to decline answering when no relevant information is available, has emerged as a , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

此外，拒绝率 [14] 衡量系统在没有相关信息可用时拒绝回答的能力，已作为第 1 卷出现。 1、第1条。出版日期：2018 年 8 月。

### Page 21

### 段落 138 · Page 21

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 21 key indicator of responsible output generation. Similarly, Error Detection Rate [14] evaluates the model’s capability to identify and filter out incorrect or misleading information, ensuring that the generation process is based on trustworthy sources. Another important consideration is Context Relevance, which assesses the alignment of retrieved documents with the specific query, emphasizing the need for content directly relevant to the generation task’s context.

**中文**

大型语言模型中检索增强文本生成的调查 21 负责任的输出生成的关键指标。同样，错误检测率[14]评估模型识别和过滤不正确或误导性信息的能力，确保生成过程基于可靠的来源。另一个重要的考虑因素是上下文相关性，它评估检索到的文档与特定查询的一致性，强调需要与生成任务的上下文直接相关的内容。

### 段落 139 · Page 21

**EN**

Faithfulness [33] is also critical in determining whether the generated text accurately reflects the information found in the retrieved documents, thereby minimizing the risk of generating misleading or incorrect content. The eRAG framework [119] introduces a more refined approach to evaluating retrieval quality in RAG systems by focusing on individual documents rather than the entire retrieval process. It operates by feeding each document in the retrieval list into the LLM alongside the query and evaluating the generated output against downstream task metrics such as Accuracy.

**中文**

忠实度[33]对于确定生成的文本是否准确反映检索到的文档中的信息也至关重要，从而最大限度地减少生成误导性或不正确内容的风险。 eRAG 框架 [119] 引入了一种更精细的方法来评估 RAG 系统中的检索质量，重点关注单个文档而不是整个检索过程。它的运行方式是将检索列表中的每个文档与查询一起输入 LLM，并根据下游任务指标（例如准确性）评估生成的输出。

### 段落 140 · Page 21

**EN**

The documentlevel scores are then aggregated using ranking metrics like MAP to produce a single evaluation score. This focus on document-level contributions offers a more precise assessment of retrieval quality while being significantly more computationally efficient than traditional end-to-end evaluations. Notably, eRAG demonstrates that its document-level evaluation correlates more strongly with downstream RAG performance compared to conventional methods like human annotations or provenance labels.

**中文**

然后使用 MAP 等排名指标聚合文档级别分数以生成单个评估分数。这种对文档级贡献的关注提供了对检索质量的更精确的评估，同时比传统的端到端评估在计算效率上显着提高。值得注意的是，与人工注释或来源标签等传统方法相比，eRAG 证明其文档级评估与下游 RAG 性能的相关性更强。

### 段落 141 · Page 21

**EN**

This correlation underscores that the LLM, as the primary consumer of the retrieved results, is the most reliable judge of retrieval performance [119]. Regardless of the retrieval model or the number of retrieved documents, eRAG consistently outperforms other evaluation approaches, indicating that directly evaluating how each document supports the LLM’s output is the most effective way to measure retrieval quality in RAG systems.

**中文**

这种相关性强调了法学硕士作为检索结果的主要消费者，是检索性能最可靠的判断者[119]。无论检索模型或检索文档的数量如何，eRAG 始终优于其他评估方法，这表明直接评估每个文档如何支持 LLM 的输出是衡量 RAG 系统检索质量的最有效方法。

### 段落 142 · Page 21

**EN**

7.2 Generation-based Aspect The evaluation of text produced by large language models involves analyzing performance across a range of downstream tasks using standard metrics that assess linguistic quality, coherence, accuracy, and alignment with ground-truth data. Metrics like BLEU [107] and ROUGE-L [87] are often used to measure fluency, similarity to human-produced text, and the overlap with reference summaries, respectively, providing insights into how well the generated content captures key ideas and phrases.

**中文**

7.2 基于生成的方面 对大型语言模型生成的文本的评估涉及使用评估语言质量、连贯性、准确性以及与真实数据的一致性的标准指标来分析一系列下游任务的性能。 BLEU [107] 和 ROUGE-L [87] 等指标通常分别用于衡量流畅性、与人工生成文本的相似性以及与参考摘要的重叠度，从而深入了解生成的内容捕获关键思想和短语的程度。

### 段落 143 · Page 21

**EN**

In addition to these metrics, which focus on the quality of linguistic output, Accuracy and overlap with ground-truth data are evaluated using EM and F1 scores, which respectively measure the percentage of completely correct answers and offer a balanced view of precision and recall. This ensures that relevant answers are retrieved while inaccuracies are minimized. Beyond these standard evaluation techniques, more specialized criteria have been introduced to assess RAG systems in specific contexts. For dialogue generation, for instance, metrics like perplexity and entropy are employed to evaluate response diversity and naturalness.

**中文**

除了这些关注语言输出质量的指标之外，还使用 EM 和 F1 分数来评估准确性和与真实数据的重叠，这分别衡量完全正确答案的百分比，并提供精确度和召回率的平衡视图。这可确保检索到相关答案，同时最大限度地减少不准确性。除了这些标准评估技术之外，还引入了更专业的标准来评估特定环境下的 RAG 系统。例如，对于对话生成，采用困惑度和熵等指标来评估响应的多样性和自然度。

### 段落 144 · Page 21

**EN**

In scenarios where misinformation is a concern, metrics like Misleading Rate and Mistake Reappearance Rate [91] have been developed to measure a model’s ability to avoid generating incorrect or misleading content. Other advanced metrics include Answer Relevance [33], which assesses the precision of responses to queries, Kendall’s tau [117], used for evaluating the accuracy of system rankings, and Micro-F1 [117], which fine-tunes accuracy evaluation in tasks involving multiple correct answers.

**中文**

在存在错误信息的情况下，已经开发了诸如误导率和错误重现率[91]之类的指标来衡量模型避免生成不正确或误导性内容的能力。其他高级指标包括答案相关性[33]，用于评估查询响应的精度，Kendall’s tau [117]，用于评估系统排名的准确性，以及 Micro-F1 [117]，用于微调涉及多个正确答案的任务中的准确性评估。

### 段落 145 · Page 21

**EN**

Prediction Accuracy further complements these by directly measuring how closely the generated responses align with the expected answers, offering a clear measure of a system’s effectiveness in producing accurate content. , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

预测准确性通过直接测量生成的响应与预期答案的吻合程度来进一步补充这些内容，从而清楚地衡量系统生成准确内容的有效性。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 22

### 段落 146 · Page 22

**EN**

22 Huang et al. ResearchYearRetrieval SourceMulti-hopTraining Pre-Retrieval RetrievalPost-RetrievalGenerationInternalExternal IndexingQuery ManipulationData ModificationSearch & RankingRe-RankingFilteringEnhancingCustomizationREALM [42]2020 ! ! ! !kNN-LMs [72]2020! ! ! ! !RAG [83]2020 ! ! ! !FiD [58] 2021 ! ! !Webgpt [100]2021 ! ! ! ! ! ! ! !Re2G [40]2022! ! ! !RETRO [9]2022 ! ! ! ! !DSP [73]2022 ! ! ! ! !CoK [86]2023 ! ! ! !IRCOT [131]2023 ! ! ! !ITRG [34]2023! ! ! ! !PKG [92]2023!RA-DIT [89]2023 ! ! ! ! ! !Self-RAG [4]2023 ! ! !SURGE [70]2023! !FiD-TF [5]2023 ! ! !PRCA [151]2023 ! ! ! !REPLUG [122]2023 ! ! !AAR [157]2023 ! !

**中文**

22 黄等人。研究年份检索源多跳训练检索前检索检索后检索生成内部外部索引查询操作数据修改搜索和排名重排过滤增强定制REALM [42]2020！！！ !kNN-LM [72]2020！！！！ !RAG [83]2020 !！！ !FiD [58] 2021 !！！Webgpt [100]2021！！！！！！！！Re2G [40]2022！！！！复古 [9]2022！！！！ !DSP [73]2022 !！！！ !COK [86]2023 !！！ !IRCOT [131]2023 !！！ !ITRG [34]2023！！！！ !PKG [92]2023!RA-DIT [89]2023 !！！！！！自我RAG [4]2023！！！激增[70]2023！ !FiD-TF [5]2023 !！ !中国人民解放军[151]2023年！！！！重新插入 [122]2023！！ !AAR [157]2023 !！

### 段落 147 · Page 22

**EN**

!Query2doc [137]2023! !Step-Back [163]2023 ! ! !ITER-RETGEN [121]2023 ! ! ! !RECITE [125]2023! ! ! ! !PROMPTAGATOR [27]2023! ! ! ! !UPRISE [20]2023! ! ! ! ! !GENREAD [156]2023! ! !LAPDOG [52]2023 ! ! ! ! ! ! !KnowledGPT [140]2023 ! ! ! !Selfmem [21]2023 ! ! ! ! !MEMWALKER [13]2023 ! ! ! !RECOMP [147]2023 ! ! !Rewrite-Retrieve-Read [94]2023 ! ! !Atlas [94]2023 ! ! ! ! ! !DKS-RAC [53]2023 ! ! ! ! !In-Context RALM [112]2023 ! !Fid-light [47]2023 ! ! !FLARE [65]2023 ! ! !Chameleon [63]2023 ! ! ! !ERAGent [123]2024! ! ! ! ! ! ! !PipeRAG [64]2024 ! ! ! ! !GenRT [148]2024! ! ! !PersonaRAG [160]2024! ! ! ! ! ! ! ! !CRAG [149]2024! ! ! ! ! !

**中文**

！Query2doc [137]2023！！退一步 [163]2023！！ !ITER-雷根 [121]2023 !！！！背诵 [125]2023！！！！ !提示器 [27]2023！！！！！起义 [20]2023！！！！！ !GENREAD [156]2023！！ !拉普狗 [52]2023！！！！！！ !KnowledGPT [140]2023 !！！！自我记忆 [21]2023！！！！！MEMWALKER [13]2023！！！ !RECOMP [147]2023！！！重写-检索-读取 [94]2023！！！阿特拉斯[94]2023！！！！！ !DKS-RAC [53]2023 !！！！ !上下文中的 RALM [112]2023 ! !Fid-light [47]2023 !！ !耀斑 [65]2023！！！变色龙 [63]2023！！！ !ERAGent [123]2024！！！！！！！ !PipeRAG [64]2024！！！！！GenRT [148]2024！！！！PersonaRAG [160]2024！！！！！！！！！克拉格 [149]2024！！！！！！

### 段落 148 · Page 22

**EN**

!IMRAG [150]2024 ! ! ! ! ! !AiSAQ [126]2024! ! ! !ROPG [118]2024! ! ! ! !RQ-RAG [12]2024 ! ! ! ! !PlanRAG [81]2024 ! ! ! ! !RARG [159]2024 ! ! ! ! !DRAGIN [124]2024 ! ! ! ! !LRUS-CoverTree [93]2024! ! ! ! ! Table 2. The comprehensive summary of RAG studies. A !in the “Multi-hop” column signifies that the research involves multiple search rounds. Similarly, a !in the “Training” column indicates that the study included training phases. It is important to note that in this context, “Training” encompasses both initial model training and fine-tuning processes.

**中文**

!IMRAG [150]2024！！！！！！AiSAQ [126]2024！！！ !ROPG [118]2024！！！！ !RQ-RAG [12]2024！！！！ !PlanRAG [81]2024 !！！！！RARG [159]2024！！！！！龙 [124]2024！！！！ !LRUS-CoverTree [93]2024！！！！！表 2. RAG 研究的综合总结。 “多跳”栏中的 ! 表示该研究涉及多轮搜索。同样，“培训”列中的 ! 表示该研究包括培训阶段。值得注意的是，在这种情况下，“训练”包括初始模型训练和微调过程。

### 段落 149 · Page 22

**EN**

8 Comparisons of RAG 8.1 The Comprehensive Summary of RAG Table 2 presents a detailed analysis of the RAG studies discussed in this paper. The analysis shows that the majority of these studies have utilized external data sources to enrich the content of LLMs. A preference for multiple-hop over single-hop retrieval was noted, indicating that iterative search rounds generally yield superior results. In other words, most methods employ dense retrieval to secure higher quality candidate documents. Compared to modifying datasets in the pre-retrieval stage, more studies focus on manipulating the query to improve retrieval performance.

**中文**

8 RAG 的比较 8.1 RAG 的综合总结 表2 详细分析了本文讨论的RAG 研究。分析表明，这些研究大多数都利用了外部数据源来丰富法学硕士的内容。人们注意到多跳检索优于单跳检索，这表明迭代搜索轮次通常会产生更好的结果。换句话说，大多数方法都采用密集检索来确保更高质量的候选文档。与在检索前阶段修改数据集相比，更多的研究侧重于操纵查询以提高检索性能。

### 段落 150 · Page 22

**EN**

Additionally, there is a significant emphasis on optimizing the retrieval phase, highlighting its crucial role in the research. However, there seems to be a scarcity of studies concentrating on customization in the generation stage, pointing to this as a potential area for future exploration. Overall, while the goal of RAG is to enhance the response quality of LLMs, greater efforts have been directed towards improving retrieval aspects. , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

此外，还非常重视优化检索阶段，强调其在研究中的关键作用。然而，专注于生成阶段定制的研究似乎很少，这表明这是未来探索的潜在领域。总体而言，虽然 RAG 的目标是提高法学硕士的回答质量，但更大的努力是为了改进检索方面。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 23

### 段落 151 · Page 23

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 23 Research Year Retriever Generator REALM [42] 2020 BERT [29] Transformers [133] kNN-LMs [72] 2020 FAISS [68] Transformers RAG [83] 2020 DPR [71] BART-Large [82] FiD [58] 2021 BM25 [116], DPR T5 [111] Webgpt [100] 2021 Bing GPT-3 [10] Re2G [40] 2022 BM25, DPR BART RETRO [9] 2022 BERT Transformer DSP [73] 2022 ColBERTv2 [74] GPT-3.5 (text-davinci-002) CoK [86] 2023 LLaMA2-7B [130], ChatGPT (gpt-3.5-turbo-0613)ChatGPT (gpt-3.5-turbo-0613) IRCOT [131] 2023 BM25 GPT-3 (code-davinci-002), Flan-T5 [24] ITRG [34] 2023 Atlas [94] LLaMA-33B PKG [92] 2023 LLaMA-7B InstructGPT-3

**中文**

大型语言模型中检索增强文本生成的调查 23 研究年检索器生成器 REALM [42] 2020 BERT [29] Transformers [133] kNN-LMs [72] 2020 FAISS [68] Transformers RAG [83] 2020 DPR [71] BART-Large [82] FiD [58] 2021 BM25 [116]、DPR T5 [111] Webgpt [100] 2021 Bing GPT-3 [10] Re2G [40] 2022 BM25、DPR BART RETRO [9] 2022 BERT Transformer DSP [73] 2022 ColBERTv2 [74] GPT-3.5 (text-davinci-002) CoK [86] 2023 LLaMA2-7B [130]、ChatGPT (gpt-3.5-turbo-0613)ChatGPT (gpt-3.5-turbo-0613) IRCOT [131] 2023 BM25 GPT-3 (代码-davinci-002)、Flan-T5 [24] ITRG [34] 2023 Atlas [94] LLaMA-33B PKG [92] 2023 LLaMA-7B InstructGPT-3

### 段落 152 · Page 23

**EN**

.5 (text-davinic-002) [104] RA-DIT [89] 2023 DRAGON+ [88] LLaMA Self-RAG [4] 2023 Contriever [57] LLaMA2 (7B and 13B) , GPT-4 [1] SURGE [70] 2023 Graph Neural Networks (GNN) [43] Transformers FiD-TF [5] 2023 BM25, SBERT [115] T5 PRCA [151] 2023 BM25, DPR, Contriver, SimCSE [37], SBERT T5, Phoenix-7B [19], Vicuna-7B [22], ChatGLM [31], GPT-3.5 REPLUG [122] 2023 Contriever GPT-3 AAR [157] 2023 ANCE [146], Contriever Flan-T5, InstructGPT Query2doc [137] 2023 BM25, DPR GPT-3 (text-davinci-003) Step-Back [163] 2023 PaLM-2L [23] PaLM-2L, GPT-4 ITER-RETGEN [121] 2023 Contriever InstructGPT (text-davinci-003), LLaMA2 RECITE [125] 2023 PaLM, UL2 [127]

**中文**

.5 (text-davinic-002) [104] RA-DIT [89] 2023 DRAGON+ [88] LLaMA Self-RAG [4] 2023 Contriever [57] LLaMA2 (7B 和 13B) , GPT-4 [1] SURGE [70] 2023 图神经网络 (GNN) [43] 变形金刚FiD-TF [5] 2023 BM25、SBERT [115] T5 PRCA [151] 2023 BM25、DPR、Contriver、SimCSE [37]、SBERT T5、Phoenix-7B [19]、Vicuna-7B [22]、ChatGLM [31]、GPT-3.5 REPLUG [122] 2023 Contriever GPT-3 AAR [157] 2023 ANCE [146]、Contriever Flan-T5、InstructGPT Query2doc [137] 2023 BM25、DPR GPT-3 (text-davinci-003) 后退 [163] 2023 PaLM-2L [23] PaLM-2L、GPT-4 ITER-RETGEN [121] 2023 Contriever InstructGPT (text-davinci-003)，LLaMA2 RECITE [125] 2023 PaLM，UL2 [127]

### 段落 153 · Page 23

**EN**

, OPT [161], Codex [16] PROMPTAGATOR [27] 2023 T5 FLAN UPRISE [20] 2023 GPT-Neo-2.7B [8] BLOOM-7.1B [142], OPT-66B, GPT-3-175B GENREAD [156] 2023 InstructGPT LAPDOG [52] 2023 Contriever T5 KnowledGPT [140] 2023 GPT-4 Selfmem [21] 2023 BM25 XGLM [90], XLM-Rbase [25] MEMWALKER [13] 2023 LLaMA2 LLaMA2 RECOMP [147] 2023 BM25 T5-Large Rewrite-Retrieve-Read [94]2023 Bing T5-Large, ChatGPT(gpt-3.5-turbo), Vicuna-13B Atlas [94] 2023 Contriever T5 DKS-RAC [53] 2023 DPR BART In-Context RALM [112] 2023 BM25, BERT-base, Contriever, Spider [113] GPT-2, GPT-Neo, GPT-J [35], OPT, and LLaMA Fid-light [47] 2023 GTR-Base [101] T5 FLARE [65] 2023 BM25, Bing GPT

**中文**

，OPT [161]，Codex [16] PROMPTAGATOR [27] 2023 T5 FLAN UPRISE [20] 2023 GPT-Neo-2.7B [8] BLOOM-7.1B [142]，OPT-66B，GPT-3-175B GENREAD [156] 2023 InstructGPT LAPDOG [52] 2023 Contriever T5 KnowledGPT [140] 2023 GPT-4 Selfmem [21] 2023 BM25 XGLM [90]，XLM-Rbase [25] MEMWALKER [13] 2023 LLaMA2 LLaMA2 RECOMP [147] 2023 BM25 T5-大型重写-检索-读取[94]2023 Bing T5-Large、ChatGPT(gpt-3.5-turbo)、Vicuna-13B Atlas [94]2023 Contriever T5 DKS-RAC [53]2023 DPR BART In-Context RALM [112]2023 BM25、BERT-base、Contriever、Spider [113] GPT-2、GPT-Neo、 GPT-J [35]、OPT 和 LLaMA Fid-light [47] 2023 GTR-Base [101] T5 FLARE [65] 2023 BM25、Bing GPT

### 段落 154 · Page 23

**EN**

-3.5 (text-davinci-003) Chameleon [63] 2023 ChamVS [63] ChamLM [63] ERAGent [123] 2024 Bing GPT-3.5, Falcon 1B [108] PipeRAG [64] 2024 SBERT RETRO [9] GenRT [148] 2024 LambdaMart [2] PersonaRAG [160] 2024 BM25 GPT-3.5 CRAG [149] 2024 Contriever LLaMA2 IMRAG [150] 2024 DPR Vicuna-7B AiSAQ [126] 2024 DiskANN [106] ROPG [118] 2024 BM25, Contriever FlanT5-XXL RQ-RAG [12] 2024 DuckDuckGo8 LLaMA2-7B PlanRAG [81] 2024 GPT-4 GPT-4 RARG [159] 2024 BM25, E5 [136] LLaMA2-7B DRAGIN [124] 2024 BM25, SGPT [99] LLaMA2 (7B and 13B), Vicuna-13B LRUS-CoverTree [93] 2024 k-MIPS Table 3.

**中文**

-3.5 (text-davinci-003) Chameleon [63] 2023 ChamVS [63] ChamLM [63] ERAGent [123] 2024 Bing GPT-3.5，Falcon 1B [108] PipeRAG [64] 2024 SBERT RETRO [9] GenRT [148] 2024 LambdaMart [2] PersonaRAG [160] 2024 BM25 GPT-3.5 CRAG [149] 2024 Contriever LLaMA2 IMRAG [150] 2024 DPR Vicuna-7B AiSAQ [126] 2024 DiskANN [106] ROPG [118] 2024 BM25，Contriever FlanT5-XXL RQ-RAG [12] 2024 DuckDuckGo8 LLaMA2-7B PlanRAG [81] 2024 GPT-4 GPT-4 RARG [159] 2024 BM25，E5 [136] LLaMA2-7B DRAGIN [124] 2024 BM25，SGPT [99] LLaMA2（7B 和 13B）， Vicuna-13B LRUS-CoverTree [93] 2024 k-MIPS 表 3。

### 段落 155 · Page 23

**EN**

The summary of Retrievers and Generators. The retrieval models and pre-trained language models explicitly mentioned in these studies have been recorded. 8.2 Retriever and Generator In RAG, the retriever and generator are central components, each playing a distinct role in the system’s overall performance. Table 3 summarizes the retrievers and generators used across the studies discussed in this paper. The table reveals that while a wide range of advanced language models are employed as generators, many systems still rely on traditional retrievers like BM25, valued for their efficiency.

**中文**

检索器和生成器的摘要。这些研究中明确提到的检索模型和预训练语言模型均已记录。 8.2 检索器和生成器 在 RAG 中，检索器和生成器是核心组件，每个组件在系统的整体性能中发挥着独特的作用。表 3 总结了本文讨论的研究中使用的检索器和生成器。该表显示，虽然采用多种高级语言模型作为生成器，但许多系统仍然依赖传统的检索器，例如 BM25，其效率受到重视。

### 段落 156 · Page 23

**EN**

This highlights the continued importance of optimizing retrieval methods while balancing computational demands. Interestingly, despite the availability of powerful models such as LLaMA2, GPT-3.5, and GPT-4, these are not widely adopted as generators. Instead, models like T5 remain prevalent, while more foundational retrieval approaches, such as those based on BERT, see limited use. The relative scarcity of IR-focused LLMs in retrievers suggests a promising avenue for future research and development in this domain. , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

这凸显了优化检索方法同时平衡计算需求的持续重要性。有趣的是，尽管有 LLaMA2、GPT-3.5 和 GPT-4 等强大的模型可用，但这些模型并未被广泛用作生成器。相反，T5 等模型仍然很流行，而更基础的检索方法（例如基于 BERT 的检索方法）的使用却很有限。猎犬中以 IR 为重点的法学硕士相对稀缺，这表明该领域未来的研究和开发有一个有希望的途径。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 24

### 段落 157 · Page 24

24 Huang et al.

### 段落 158 · Page 24

**EN**

Corpus Retriever MirageBenchmark Dataset AverageMMLU-Med MedQA-US MedMCQA PubMedQA* BioASQ-Y/N None None 72.91 ±1.35 65.04±1.34 55.25±0.77 36.00±2.15 74.27±1.76 60.69 PubMed (23.9M) BM25 72.27±1.36 63.71±1.35 55.49±0.77 66.20±2.12 88.51±1.28 69.23 Contriever 71.72±1.36 63.94±1.35 54.29±0.77 65.60±2.12 85.44±1.42 68.20 SPECTER 73.19±1.34 65.20±1.34 53.12±0.77 54.80±2.23 75.73±1.72 64.41 MedCPT 73.09±1.34 66.69±1.32 54.94±0.77 66.40±2.11 85.76±1.41 69.38 RRF-2 75.57±1.30 64.34±1.34 55.34±0.77 69.00±2.07 87.06±1.35 70.26 RRF-4 73.37±1.34 64.73±1.34 54.75±0.77 67.20±2.10 88.51±1.28 69.71 Wikipedia (29.9M) BM25 73.37±1.34 63.47±1.35 54.10±0.77 26.

**中文**

Corpus Retriever MirageBenchmark 数据集 AverageMMLU-Med MedQA-US MedMCQA PubMedQA* BioASQ-Y/N 无 无 72.91 ±1.35 65.04±1.34 55.25±0.77 36.00±2.15 74.27±1.76 60.69 PubMed (23.9M) BM25 72.27±1.36 63.71±1.35 55.49±0.77 66.20±2.12 88.51±1.28 69.23 挖掘机 71.72±1.36 63.94±1.35 54.29±0.77 65.60±2.12 85.44±1.42 68.20 幽灵 73.19±1.34 65.20±1.34 53.12±0.77 54.80±2.23 75.73±1.72 64.41 MedCPT 73.09±1.34 66.69±1.32 54.94±0.77 66.40±2.11 85.76±1.41 69.38 RRF-2 75.57±1.30 64.34±1.34 55.34±0.77 69.00±2.07 87.06±1.35 70.26 RRF-4 73.37±1.34 64.73±1.34 54.75±0.77 67.20±2.10 88.51±1.28 69.71 维基百科 (29.9M) BM25 73.37±1.34 63.47±1.35 54.10±0.77 26.

### 段落 159 · Page 24

**EN**

40±1.97 71.36±1.82 57.74 Contriever 74.10±1.33 65.99±1.33 54.03±0.77 26.40±1.97 69.90±1.85 58.08 SPECTER 72.18±1.36 63.63±1.35 52.71±0.77 22.20±1.86 66.83±1.89 55.51 MedCPT 71.99±1.36 65.12±1.34 55.15±0.77 29.00±2.03 73.46±1.78 58.95 RRF-2 74.20±1.33 64.57±1.34 54.72±0.77 31.00±2.07 76.21±1.71 60.14 RRF-4 73.19±1.34 64.96±1.34 54.53±0.77 31.00±2.07 72.01±1.81 59.14 Table 4.

**中文**

40±1.97 71.36±1.82 57.74 探索者 74.10±1.33 65.99±1.33 54.03±0.77 26.40±1.97 69.90±1.85 58.08 幽灵 72.18±1.36 63.63±1.35 52.71±0.77 22.20±1.86 66.83±1.89 55.51 MedCPT 71.99±1.36 65.12±1.34 55.15±0.77 29.00±2.03 73.46±1.78 58.95 RRF-2 74.20±1.33 64.57±1.34 54.72±0.77 31.00±2.07 76.21±1.71 60.14 RRF-4 73.19±1.34 64.96±1.34 54.53±0.77 31.00±2.07 72.01±1.81 59.14 表4.

### 段落 160 · Page 24

**EN**

Part results of Accuracy (%) of GPT-3.5 across different corpora and retrievers on Mirage. Red and green highlight declines and improvements compared to CoT (first row), with shading intensity reflecting the degree of change. Data sourced from Mirage [144]. Impact of the Retriever. The results shown in Table 4 highlight the accuracy of GPT-3.5 across different corpora and retrievers on the Mirage benchmark [144]. These findings underscore how retriever performance closely depends on the alignment between training data and the target corpus.

**中文**

Mirage 上不同语料库和检索器的 GPT-3.5 准确率 (%) 的部分结果。红色和绿色突出显示与 CoT（第一行）相比的下降和改进，阴影强度反映了变化的程度。数据来源于 Mirage [144]。猎犬的影响。表 4 中显示的结果突出显示了 GPT-3.5 在 Mirage 基准上跨不同语料库和检索器的准确性 [144]。这些发现强调了检索器的性能如何密切依赖于训练数据和目标语料库之间的一致性。

### 段落 161 · Page 24

**EN**

For example, in the MEDRAG system, MedCPT—trained specifically on PubMed user logs—significantly improves retrieval performance when accessing the PubMed corpus. This illustrates the benefits of using domain-specific retrievers tailored to specialized datasets. In contrast, general-purpose retrievers like Contriever, which incorporate Wikipedia data during training, excel in retrieving information from Wikipedia, especially for tasks like MMLU-Med and MedQA-US. On the other hand, SPECTER, which focuses more on regularizing pairwise article distances than optimizing query-to-article relevance, underperforms on the MedCorp corpus.

**中文**

例如，在 MEDRAG 系统中，专门针对 PubMed 用户日志进行训练的 MedCPT 在访问 PubMed 语料库时显着提高了检索性能。这说明了使用针对专门数据集定制的特定领域检索器的好处。相比之下，像 Contriever 这样的通用检索器在训练期间结合了维基百科数据，擅长从维基百科检索信息，特别是对于 MMLU-Med 和 MedQA-US 等任务。另一方面，SPECTRE 更注重规范成对文章距离，而不是优化查询与文章的相关性，在 MedCorp 语料库上表现不佳。

### 段落 162 · Page 24

**EN**

The study also explores combining multiple retrievers using Reciprocal Rank Fusion (RRF). However, results show that adding more retrievers does not always lead to better outcomes; for instance, excluding SPECTER in RRF-2 on Wikipedia yields better results than RRF-4, indicating that simply increasing the number of retrievers is not beneficial unless their strengths align with the retrieval task.

**中文**

该研究还探索了使用倒数排名融合（RRF）组合多个检索器。然而，结果表明，添加更多的猎犬并不总是能带来更好的结果；例如，在维基百科的 RRF-2 中排除 SPECTRE 会产生比 RRF-4 更好的结果，这表明简单地增加检索器的数量并没有什么好处，除非它们的优势与检索任务相符。

### 段落 163 · Page 24

**EN**

Figure 5a illustrates how eRAG investigates the correlation between LLM performance and retrieval effectiveness on the NQ dataset using three retrievers with different characteristics: BM25 (lexical sparse), RetroMAE (dense) [143], and SPLADEv3 (learned sparse) [80]. The initial retrievals are re-ranked using a DeBERTa-v3 [79] cross-encoder. The analysis demonstrates that as retrieval quality improves, LLM performance increases significantly across various models. Notably, reranking with SPLADEv3 and DeBERTa-v3 consistently achieves the best results across datasets and metrics.

**中文**

图 5a 说明了 eRAG 如何使用具有不同特征的三个检索器在 NQ 数据集上研究 LLM 性能和检索有效性之间的相关性：BM25（词汇稀疏）、RetroMAE（密集）[143] 和 SPLADEv3（学习稀疏）[80]。使用 DeBERTa-v3 [79] 交叉编码器对初始检索进行重新排序。分析表明，随着检索质量的提高，法学硕士在各种模型中的表现显着提高。值得注意的是，使用 SPLADEv3 和 DeBERTa-v3 进行重排始终能够在数据集和指标上取得最佳结果。

### 段落 164 · Page 24

**EN**

This underscores the critical role that high-quality retrieval plays in determining overall RAG system effectiveness, suggesting that IR-focused LLMs could be a valuable asset in enhancing generation performance. Impact of the Generator. The BERGEN study [ 114] compares the performance of LLMs with gold passages (Oracle) against closed-book settings without retrieval, as shown in Figure 5b. Surprisingly, the experiments do not reveal a straightforward relationship between model size and the performance gains from retrieval. For instance, smaller models like LLaMA2-7B benefit more , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

这强调了高质量检索在确定 RAG 系统整体有效性方面所发挥的关键作用，表明以 IR 为重点的法学硕士可能是提高发电性能的宝贵资产。发电机的影响。 BERGEN 研究 [114] 将带有黄金段落 (Oracle) 的法学硕士的表现与不带检索的闭卷设置进行了比较，如图 5b 所示。令人惊讶的是，实验并没有揭示模型大小和检索性能增益之间的直接关系。例如，像 LLaMA2-7B 这样的较小模型受益更多1、第1条。出版日期：2018 年 8 月。

### Page 25

### 段落 165 · Page 25

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 25 0.6 0.7 0.8 0.9 1.0 Retrieval Performance (Recall@5) 0.60 0.65 0.70 0.75 0.80 0.85RAG Performance (LLMeval) SPLADE-v3+RR BM25 SPLADE-v3 BM25+RR Oracle RetroMAE RetroMAE+RR (a) Impact of retrieval performance on RAG performance for SOLAR-10.7B [75] on NQ with different ranking systems. RR means with additional re-ranking using DeBERTa-v3.

**中文**

大型语言模型中检索增强文本生成的调查 25 0.6 0.7 0.8 0.9 1.0 检索性能 (Recall@5) 0.60 0.65 0.70 0.75 0.80 0.85RAG 性能 (LLMeval) SPLADE-v3+RR BM25 SPLADE-v3 BM25+RR Oracle RetroMAE RetroMAE+RR (a) SOLAR-10.7B [75] 的检索性能对具有不同排名系统的 NQ 的 RAG 性能的影响。 RR 意味着使用 DeBERTa-v3 进行额外的重排。

### 段落 166 · Page 25

**EN**

TinyLlama-1.1B SOLAR-10.7B Mixtral-8x7B Llama3-8B Llama2-7B Llama2-70B LLM 0.0 0.2 0.4 0.6 0.8 1.0RAG Performance (LLMeval) +0.09 +0.03 +0.06 +0.15 +0.17 +0.15 Retriever Closed Book Oracle (b) Performance gains w/ and w/o oracle retrieval for LLMs with different sizes. Comparing closed book vs oracle passages averaged over all QA datasets in KILT. (c) The correlation between eRAG and the downstream performance of different LLM sizes. In this experiment, T5small (60M parameters) and T5-base (220M parameters) with FiD are used. The documents are retrieved using BM25. Fig. 5.

**中文**

TinyLlama-1.1B SOLAR-10.7B Mixtral-8x7B Llama3-8B Llama2-7B Llama2-70B LLM 0.0 0.2 0.4 0.6 0.8 1.0RAG 性能 (LLMeval) +0.09 +0.03 +0.06 +0.15 +0.17 +0.15 检索器Closed Book Oracle (b) 对于不同规模的 LLM，使用和不使用 Oracle 检索时的性能提升。比较 KILT 中所有 QA 数据集的闭卷与预言段落的平均值。 (c) eRAG 与不同 LLM 规模的下游性能之间的相关性。在本实验中，使用带有FiD的T5small（60M参数）和T5-base（220M参数）。使用 BM25 检索文档。图 5.

### 段落 167 · Page 25

**EN**

Retriever and generator experiment results sourced from eRAG [119] and BERGEN [114]. from retrieval than larger models like LLaMA2-70B. In fact, LLaMA2-7B with retrieval outperforms LLaMA2-70B in a closed-book setting, suggesting that retrieval augmentation can make smaller models more competitive. Similarly, results from the eRAG experiments in Figure 5c indicate that varying LLM sizes (e.g., T5-small vs. T5-base) does not significantly affect the correlation between eRAG and downstream performance.

**中文**

检索器和发生器实验结果来自 eRAG [119] 和 BERGEN [114]。与 LLaMA2-70B 等较大型号相比，检索结果更准确。事实上，具有检索功能的 LLaMA2-7B 在闭卷环境中的表现优于 LLaMA2-70B，这表明检索增强可以使较小的模型更具竞争力。同样，图 5c 中 eRAG 实验的结果表明，不同的 LLM 大小（例如，T5-small 与 T5-base）不会显着影响 eRAG 与下游性能之间的相关性。

### 段落 168 · Page 25

**EN**

These findings highlight that retrieval quality has a more substantial impact on RAG performance than the choice of generator, reinforcing the notion that investing in better retrieval strategies often yields more benefits than relying solely on larger LLMs. 9 Challenges and Future Directions The evolving landscape of RAG systems faces significant challenges that impact the quality of generated outputs, system efficiency, and the integration of multimodal data. As these systems become more prevalent across a range of applications, addressing these challenges is essential for improving their effectiveness and scalability. , Vol. 1, No.

**中文**

这些发现强调，检索质量对 RAG 性能的影响比生成器的选择更大，这强化了这样一种观念，即投资更好的检索策略通常比仅仅依赖较大的法学硕士能带来更多的好处。 9 挑战和未来方向 RAG 系统不断发展的格局面临着重大挑战，这些挑战影响生成输出的质量、系统效率和多模式数据的集成。随着这些系统在一系列应用程序中变得越来越普遍，解决这些挑战对于提高其有效性和可扩展性至关重要。，卷。 1、没有。

### 段落 169 · Page 25

**EN**

1, Article . Publication date: August 2018.

**中文**

1、文章。出版日期：2018 年 8 月。

### Page 26

### 段落 170 · Page 26

**EN**

26 Huang et al. 9.1 Retrieval Quality The quality of retrieval is fundamental to any effective RAG system, directly influencing the relevance and accuracy of the generated content [46, 119, 138, 164]. Current retrieval methods, however, frequently struggle with issues like noise, irrelevant documents, and fragmented information, all of which compromise the generation process. Noise Robustness. Irrelevant or misleading documents within the retrieved set can introduce noise, leading to hallucinations or unreliable answers.

**中文**

26 黄等人。 9.1 检索质量 检索质量是任何有效的 RAG 系统的基础，直接影响生成内容的相关性和准确性[46,119,138,164]。然而，当前的检索方法经常遇到噪声、不相关文档和碎片信息等问题，所有这些都会损害生成过程。噪声鲁棒性。检索到的文档集中不相关或具有误导性的文档可能会引入噪音，从而导致幻觉或不可靠的答案。

### 段落 171 · Page 26

**EN**

This challenge highlights the need for more sophisticated filtering and context-aware retrieval methods that can better differentiate relevant from irrelevant content. However, Cuconasu et al. [ 26] present an interesting perspective by showing that, under certain conditions, the inclusion of irrelevant documents can enhance overall accuracy. This finding challenges conventional retrieval strategies and suggests the potential for developing specialized approaches that strategically integrate noise within the retrieval process. Negative Rejection.

**中文**

这一挑战凸显了对更复杂的过滤和上下文感知检索方法的需求，这些方法可以更好地区分相关内容和不相关内容。然而，库科纳苏等人。 [26]提出了一个有趣的观点，表明在某些条件下，包含不相关的文档可以提高整体准确性。这一发现挑战了传统的检索策略，并表明了开发专门方法的潜力，该方法可以策略性地将噪声整合到检索过程中。消极拒绝。

### 段落 172 · Page 26

**EN**

When retrieval fails to return relevant results, models often attempt to generate responses regardless, increasing the risk of incorrect outputs. This issue is particularly problematic when queries are poorly expressed or lack sufficient context, making it difficult for retrieval models to surface relevant documents. Techniques like generating a pseudo-document that captures the query’s essence, as demonstrated by HyDE [36], can help bridge this gap. By allowing retrieval systems to find more relevant documents even from suboptimal queries, HyDE improves retrieval accuracy, albeit with a trade-off in computational cost.

**中文**

当检索无法返回相关结果时，模型通常会尝试无论如何生成响应，从而增加了错误输出的风险。当查询表达不佳或缺乏足够的上下文时，这个问题尤其成问题，使得检索模型难以显示相关文档。正如 HyDE [36] 所演示的，生成捕获查询本质的伪文档等技术可以帮助弥合这一差距。通过允许检索系统甚至从次优查询中找到更多相关文档，HyDE 提高了检索准确性，尽管会牺牲计算成本。

### 段落 173 · Page 26

**EN**

Future research could focus on optimizing this process to balance improved retrieval accuracy with reduced latency. Information Integration. Complex queries often require synthesizing information from multiple documents, yet fragmented or conflicting information can result in incoherent or incomplete answers. Pre- and post-retrieval techniques play a critical role in addressing this challenge. Enhancing retrieval granularity and incorporating techniques like entity-level retrieval and re-ranking can improve the cohesiveness of retrieved documents. However, many post-retrieval methods, as investigated by Zhu et al.

**中文**

未来的研究可以集中在优化这个过程，以平衡提高检索准确性和减少延迟。信息整合。复杂的查询通常需要综合多个文档中的信息，但碎片化或冲突的信息可能会导致不连贯或不完整的答案。检索前和检索后技术在应对这一挑战中发挥着关键作用。增强检索粒度并结合实体级检索和重新排序等技术可以提高检索到的文档的凝聚力。然而，正如 Zhu 等人研究的那样，许多事后检索方法。

### 段落 174 · Page 26

**EN**

[ 165], rely heavily on calling LLM APIs, which incurs significant costs. Exploring alternatives such as knowledge distillation to lightweight models could offer more scalable solutions, making advanced retrieval strategies more practical in online settings. Recent research highlights the development of generative models for search as a promising direction for improving retrieval quality. Models like GERE [15] and PARADE [84] enhance document re-ranking and fact verification by directly generating relevant document titles or evidence sentences.

**中文**

[165]，严重依赖调用 LLM API，这会产生大量成本。探索轻量级模型的知识蒸馏等替代方案可以提供更具可扩展性的解决方案，使高级检索策略在在线环境中更加实用。最近的研究强调了搜索生成模型的发展是提高检索质量的一个有前途的方向。 GERE [15] 和 PARADE [84] 等模型通过直接生成相关文档标题或证据句子来增强文档重新排序和事实验证。

### 段落 175 · Page 26

**EN**

Fine-tuning pre-trained models like RankT5 [166] for ranking-specific tasks has also demonstrated potential in boosting out-of-domain performance, which is crucial for generalizing RAG systems across diverse contexts. 9.2 System Efficiency System efficiency remains a significant bottleneck, especially as RAG systems scale to handle large datasets and real-time applications. The multi-step nature of RAG workflows—including query classification, retrieval, re-ranking, and generation—adds complexity and latency, which can hinder overall performance. Latency in Retrieval Processes.

**中文**

针对特定于排名的任务对 RankT5 [166] 等预训练模型进行微调也显示出提升域外性能的潜力，这对于跨不同环境泛化 RAG 系统至关重要。 9.2 系统效率 系统效率仍然是一个重要的瓶颈，特别是当 RAG 系统扩展以处理大型数据集和实时应用程序时。 RAG 工作流程的多步骤性质（包括查询分类、检索、重新排序和生成）增加了复杂性和延迟，这可能会影响整体性能。检索过程中的延迟。

### 段落 176 · Page 26

**EN**

As document collections grow, retrieval and re-ranking processes increasingly become sources of latency. Lightweight search methods and hybrid retrieval approaches that combine sparse and dense techniques offer potential solutions by balancing speed and accuracy. For example, indexing, a traditionally resource-intensive process, has seen innovations through , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

随着文档集合的增长，检索和重新排序过程越来越成为延迟的来源。结合稀疏和密集技术的轻量级搜索方法和混合检索方法通过平衡速度和准确性提供了潜在的解决方案。例如，索引这一传统的资源密集型流程在《2017 年第 1 卷》中得到了创新。 1、第1条。出版日期：2018 年 8 月。

### Page 27

### 段落 177 · Page 27

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 27 differentiable search indices such as DSI [128] and SEAL [7]. These methods integrate retrieval within Transformer models, enabling direct mapping of text queries to document identifiers and thereby improving both performance and retrieval efficiency. Computational Costs. The introduction of deep learning-based re-ranking models like monoT5 [102] and RankLLaMA [96] brings significant computational overhead, particularly in scenarios requiring iterative reasoning.

**中文**

大型语言模型中检索增强文本生成的调查 27 个可微搜索索引，例如 DSI [128] 和 SEAL [7]。这些方法将检索集成到 Transformer 模型中，从而能够将文本查询直接映射到文档标识符，从而提高性能和检索效率。计算成本。基于深度学习的重排序模型（如 monoT5 [102] 和 RankLLaMA [96]）的引入带来了巨大的计算开销，特别是在需要迭代推理的场景中。

### 段落 178 · Page 27

**EN**

Future research could focus on optimizing these models or developing retrieval pruning techniques that reduce the number of documents passed to the generation phase without sacrificing performance [145]. Modular Workflow Optimization. The complexity of RAG systems often stems from interdependencies between components like chunking strategies, embedding models, and re-ranking algorithms. Modular designs that enable independent optimization of each step while accounting for cross-component interactions are key to enhancing system throughput [39].

**中文**

未来的研究可以集中在优化这些模型或开发检索修剪技术，以减少传递到生成阶段的文档数量而不牺牲性能[145]。模块化工作流程优化。 RAG 系统的复杂性通常源于分块策略、嵌入模型和重新排序算法等组件之间的相互依赖性。模块化设计能够独立优化每个步骤，同时考虑跨组件交互，这是提高系统吞吐量的关键[39]。

### 段落 179 · Page 27

**EN**

Advanced chunking methods and hybrid search strategies could offer trade-offs that maximize both retrieval precision and speed. An example is the Hybrid with HyDE [139] approach, which integrates both sparse and dense retrieval to capture relevant documents from both lexical and semantic perspectives. 9.3 Multimodal RAG The expansion of RAG systems to support multimodal data—encompassing text, images, and audio—presents new challenges. Integrating diverse modalities requires not only effective retrieval but also seamless alignment and generation across different data types. Cross-Modal Alignment.

**中文**

先进的分块方法和混合搜索策略可以提供权衡，最大限度地提高检索精度和速度。一个例子是 Hybrid with HyDE [139] 方法，它集成了稀疏和密集检索，从词汇和语义的角度捕获相关文档。 9.3 多模态 RAG RAG 系统支持多模态数据（包括文本、图像和音频）的扩展提出了新的挑战。集成不同的模式不仅需要有效的检索，还需要跨不同数据类型的无缝对齐和生成。跨模式对齐。

### 段落 180 · Page 27

**EN**

Aligning multimodal documents with text-based queries remains a core challenge. The complexity of mapping diverse data types into a unified retrieval framework necessitates improved cross-modal retrieval strategies capable of simultaneously handling text, image, and potentially video or audio data. Coherent Multimodal Generation. Generating responses that meaningfully integrate information from multiple modalities is another difficult task. Advanced generation models capable of reasoning across different modalities are required to produce outputs that are both contextually relevant and visually coherent.

**中文**

将多模式文档与基于文本的查询保持一致仍然是一个核心挑战。将不同数据类型映射到统一检索框架的复杂性需要改进的跨模式检索策略，能够同时处理文本、图像以及潜在的视频或音频数据。相干多模态生成。生成有意义地整合来自多种模式的信息的响应是另一项艰巨的任务。需要能够跨不同模式进行推理的高级生成模型才能产生上下文相关且视觉上连贯的输出。

### 段落 181 · Page 27

**EN**

Recent advancements in multimodal RAG, such as MuRAG [17], REVEAL [49], and Re-ViLM [152], have shown potential in incorporating multimodal retrieval and generation into real-world applications like visual question answering [18], image captioning [120], and text-to-audio generation [158]. Moving forward, research will likely focus on refining these techniques, especially in scaling multimodal retrieval to handle larger datasets and more complex queries. Extending retrieval capabilities to include more diverse media types, such as video and speech, also represents a promising direction for the continued evolution of RAG systems.

**中文**

多模态 RAG 的最新进展，例如 MuRAG [17]、REVEAL [49] 和 Re-ViLM [152]，已经显示出将多模态检索和生成结合到实际应用中的潜力，例如视觉问答 [18]、图像字幕 [120] 和文本到音频生成 [158]。展望未来，研究可能会集中在完善这些技术上，特别是在扩展多模式检索以处理更大的数据集和更复杂的查询方面。将检索功能扩展到包括视频和语音等更多样化的媒体类型，也代表了 RAG 系统持续发展的一个有希望的方向。

### 段落 182 · Page 27

**EN**

10 Conclusions In this paper, we have presented a comprehensive framework for understanding the RAG domain, highlighting its significance in enhancing the capabilities of LLMs. Through a structured overview of RAG, categorizing various methods, and an in-depth analysis of its core technologies and evaluation methods, this study illuminates the path for future research. It identifies crucial areas for improvement and outlines potential directions for advancing RAG applications, especially in textual contexts.

**中文**

10 结论 在本文中，我们提出了一个理解 RAG 领域的综合框架，强调了它在增强法学硕士能力方面的重要性。本研究通过对RAG的结构化概述、对各种方法的分类以及对其核心技术和评估方法的深入分析，为未来的研究指明了道路。它确定了需要改进的关键领域，并概述了推进 RAG 应用程序的潜在方向，特别是在文本环境中。

### 段落 183 · Page 27

**EN**

This survey aims to elucidate the core concepts of the RAG field from a retrieval perspective, and it is intended to facilitate further exploration and innovation in the accurate retrieval and generation of information. , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

本次综述旨在从检索的角度阐明RAG领域的核心概念，以期促进在信息的精确检索和生成方面的进一步探索和创新。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 28

### 段落 184 · Page 28

**EN**

28 Huang et al. Acknowledgments This research is supported by the Natural Sciences and Engineering Research Council (NSERC) of Canada. References [1] OpenAI Josh Achiam, Steven Adler, Sandhini Agarwal, Lama Ahmad, and etc. 2023. GPT-4 Technical Report. arXiv (2023). [2] Qingyao Ai, Keping Bi, Jiafeng Guo, and W. Bruce Croft. 2018. Learning a Deep Listwise Context Model for Ranking Refinement. In The 41st International ACM SIGIR Conference on Research & Development in Information Retrieval . ACM. [3] Sunil Arya, David M. Mount, Nathan S. Netanyahu, Ruth Silverman, and Angela Y. Wu. 1998.

**中文**

28 黄等人。致谢 这项研究得到了加拿大自然科学与工程研究委员会 (NSERC) 的支持。参考文献 [1] OpenAI Josh Achiam、Steven Adler、Sandhini Agarwal、Lama Ahmad 等，2023 年。GPT-4 技术报告。 arXiv (2023)。 [2] 艾庆耀，毕克平，郭嘉峰，W. Bruce Croft。 2018.学习用于排名细化的深度列表上下文模型。第 41 届国际 ACM SIGIR 信息检索研究与开发会议。 ACM。 [3] 苏尼尔·阿亚 (Sunil Arya)、大卫·M·蒙特 (David M. Mount)、内森·S·内塔尼亚胡 (Nathan S. Netanyahu)、露丝·西尔弗曼 (Ruth Silverman) 和安吉拉·Y·吴 (Angela Y. Wu)。 1998.

### 段落 185 · Page 28

**EN**

An Optimal Algorithm for Approximate Nearest Neighbor Searching Fixed Dimensions. J. ACM 45, 6 (1998), 891–923. https://doi.org/10. 1145/293347.293348 [4] Akari Asai, Zeqiu Wu, Yizhong Wang, Avirup Sil, and Hannaneh Hajishirzi. 2024. Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection. In The Twelfth International Conference on Learning Representations , Vol. abs/2310.11511. [5] Moshe Berchansky, Peter Izsak, Avi Caciularu, Ido Dagan, and Moshe Wasserblat. 2023. Optimizing Retrievalaugmented Reader Models via Token Elimination. In Proceedings of the Conference on Empirical Methods in Natural Language Processing.

**中文**

固定维度近似最近邻搜索的最优算法。 J.ACM 45, 6 (1998), 891–923。 https://doi.org/10。 1145/293347.293348 [4] Akari Asai、Zeqiu Wu、Yizhong Wang、Avirup Sil 和 Hannaneh Hajishirzi。 2024.Self-RAG：通过自我反思学习检索、生成和批判。在第十二届学习表征国际会议，卷。绝对/2310.11511。 [5] Moshe Berchansky、Peter Izsak、Avi​​ Caciularu、Ido Dagan 和 Moshe Wasserblat。 2023.通过令牌消除优化检索的阅读器模型。自然语言处理经验方法会议论文集。

### 段落 186 · Page 28

**EN**

Association for Computational Linguistics, 1506–1524. [6] Michele Bevilacqua, Giuseppe Ottaviano, Patrick S. H. Lewis, Scott Yih, Sebastian Riedel, and Fabio Petroni. 2022. Autoregressive Search Engines: Generating Substrings as Document Identifiers. In Advances in Neural Information Processing Systems 35: Annual Conference on Neural Information Processing Systems 2022, NeurIPS 2022, New Orleans, LA, USA, November 28 - December 9, 2022 , Sanmi Koyejo, S. Mohamed, A. Agarwal, Danielle Belgrave, K. Cho, and A. Oh (Eds.).

**中文**

计算语言学协会，1506-1524。 [6] Michele Bevilacqua、Giuseppe Ottaviano、Patrick S. H. Lewis、Scott Yih、Sebastian Riedel 和 Fabio Petroni。 2022.自回归搜索引擎：生成子字符串作为文档标识符。神经信息处理系统进展 35：2022 年神经信息处理系统年会，NeurIPS 2022，美国路易斯安那州新奥尔良，2022 年 11 月 28 日至 12 月 9 日，Sanmi Koyejo、S. Mohamed、A. Agarwal、Danielle Belgrave、K. Cho 和 A. Oh（编辑）。

### 段落 187 · Page 28

**EN**

http://papers.nips.cc/paper_files/paper/2022/hash/cd88d62a2063fdaf7ce6f9068fb15dcd-Abstract- Conference.html [7] Michele Bevilacqua, Giuseppe Ottaviano, Patrick S. H. Lewis, Scott Yih, Sebastian Riedel, and Fabio Petroni. 2022. Autoregressive Search Engines: Generating Substrings as Document Identifiers. In Conference on Neural Information Processing Systems (NeurIPS). [8] Sidney Black, Stella Biderman, Eric Hallahan, Quentin Anthony, Leo Gao, Laurence Golding, Horace He, Connor Leahy, Kyle McDonell, Jason Phang, Michael Pieler, Usvsn Sai Prashanth, Shivanshu Purohit, Laria Reynolds, Jonathan Tow, Ben Wang, and Samuel Weinbach. 2022.

**中文**

http://papers.nips.cc/paper_files/paper/2022/hash/cd88d62a2063fdaf7ce6f9068fb15dcd-Abstract-Conference.html [7] Michele Bevilacqua、Giuseppe Ottaviano、Patrick S. H. Lewis、Scott Yih、Sebastian Riedel 和 Fabio Petroni。 2022.自回归搜索引擎：生成子字符串作为文档标识符。在神经信息处理系统会议 (NeurIPS) 中。 [8] 西德尼·布莱克（Sidney Black）、斯特拉·比德曼（Stella Biderman）、埃里克·哈拉汉（Eric Hallahan）、昆汀·安东尼（Quentin Anthony）、利奥·高（Leo Gau）、劳伦斯·戈尔丁（Laurence Golding）、霍勒斯·何（Horace He）、康纳·莱希（Connor Leahy）、凯尔·麦克唐纳（Kyle McDonell）、杰森·彭（Jason Phang）、迈克尔·皮勒（Michael Pieler）、Usvsn Sai Prashanth、Shivanshu Purohit、Laria Reynolds、乔纳森·托（Jonathan Tow）、本·王（Ben Wang）和塞缪尔·温巴赫（Samuel Weinbach）。 2022 年。

### 段落 188 · Page 28

**EN**

GPT-NeoX-20B: An Open-Source Autoregressive Language Model. In Proceedings of BigScience Episode #5 – Workshop on Challenges & Perspectives in Creating Large Language Models , Vol. abs/2204.06745. Association for Computational Linguistics.

**中文**

GPT-NeoX-20B：开源自回归语言模型。 《BigScience》论文集第 5 集——创建大型语言模型的挑战和前景研讨会，卷。绝对/2204.06745。计算语言学协会。

### 段落 189 · Page 28

**EN**

[9] Sebastian Borgeaud, Arthur Mensch, Jordan Hoffmann, Trevor Cai, Eliza Rutherford, Katie Millican, George van den Driessche, Jean-Baptiste Lespiau, Bogdan Damoc, Aidan Clark, Diego de Las Casas, Aurelia Guy, Jacob Menick, Roman Ring, Tom Hennigan, Saffron Huang, Loren Maggiore, Chris Jones, Albin Cassirer, Andy Brock, Michela Paganini, Geoffrey Irving, Oriol Vinyals, Simon Osindero, Karen Simonyan, Jack W. Rae, Erich Elsen, and Laurent Sifre. 2022. Improving Language Models by Retrieving from Trillions of Tokens. In International Conference on Machine Learning (ICML). 2206–2240. [10] Tom B.

**中文**

[9] Sebastian Borgeaud、Arthur Mensch、Jordan Hoffmann、Trevor Cai、Eliza Rutherford、Katie Millican、George van den Driessche、Jean-Baptiste Lespiau、Bogdan Damoc、Aidan Clark、Diego de Las Casas、Aurelia Guy、Jacob Menick、Roman Ring、Tom Hennigan、Saffron Huang、Loren Maggiore、Chris Jones、Albin Cassirer、Andy Brock、米凯拉·帕格尼尼、杰弗里·欧文、奥里奥尔·维尼亚尔斯、西蒙·奥辛德罗、凯伦·西蒙扬、杰克·W·雷、埃里希·埃尔森和洛朗·西弗雷。 2022.通过从数万亿代币中检索来改进语言模型。在国际机器学习会议（ICML）中。 2206–2240。 [10] 汤姆·B.

### 段落 190 · Page 28

**EN**

Brown, Benjamin Mann, Nick Ryder, Melanie Subbiah, Jared Kaplan, Prafulla Dhariwal, Arvind Neelakantan, Pranav Shyam, Girish Sastry, Amanda Askell, Sandhini Agarwal, Ariel Herbert-Voss, Gretchen Krueger, Tom Henighan, Rewon Child, Aditya Ramesh, Daniel M. Ziegler, Jeffrey Wu, Clemens Winter, Christopher Hesse, Mark Chen, Eric Sigler, Mateusz Litwin, Scott Gray, Benjamin Chess, Jack Clark, Christopher Berner, Sam McCandlish, Alec Radford, Ilya Sutskever, and Dario Amodei. 2020. Language Models are Few-Shot Learners. InConference on Neural Information Processing Systems (NeurIPS), Vol. abs/2005.14165.

**中文**

布朗、本杰明·曼、尼克·莱德、梅兰妮·苏比亚、贾里德·卡普兰、普拉富拉·达里瓦尔、阿文德·尼拉坎坦、普拉纳夫·希亚姆、吉里什·萨斯特里、阿曼达·阿斯克尔、桑迪尼·阿加瓦尔、阿里尔·赫伯特-沃斯、格雷琴·克鲁格、汤姆·赫尼汉、Rewon Child、阿迪亚·拉梅什、丹尼尔·M·齐格勒、杰弗里·吴、克莱门斯·温特、克里斯托弗Hesse、Mark Chen、Eric Sigler、Mateusz Litwin、Scott Gray、Benjamin Chess、Jack Clark、Christopher Berner、Sam McCandlish、Alec Radford、Ilya Sutskever 和 Dario Amodei。 2020 年。语言模型是少样本学习者。神经信息处理系统会议 (NeurIPS)，卷。绝对/2005.14165。

### 段落 191 · Page 28

**EN**

[11] Jannis Bulian, Christian Buck, Wojciech Gajewski, Benjamin Börschinger, and Tal Schuster. 2022. Tomayto, Tomahto. Beyond Token-level Answer Equivalence for Question Answering Evaluation.. In Conference on Empirical Methods in Natural Language Processing (EMNLP) . 291–305. [12] Chi-Min Chan, Chunpu Xu, Ruibin Yuan, Hongyin Luo, Wei Xue, Yike Guo, and Jie Fu. 2024. RQ-RAG: Learning to Refine Queries for Retrieval Augmented Generation. arXiv abs/2404.00610 (2024). [13] Howard Chen, Ramakanth Pasunuru, Jason Weston, and Asli Celikyilmaz. 2023. Walking Down the Memory Maze: Beyond Context Limit through Interactive Reading.

**中文**

[11] Jannis Bulian、Christian Buck、Wojciech Gajewski、Benjamin Börschinger 和 Tal Schuster。 2022.托马托，托马托。超越问答评估的令牌级答案等价性。在自然语言处理经验方法会议（EMNLP）中。 291–305。 [12] 陈志敏，徐春璞，袁瑞斌，罗宏银，薛伟，郭一科，付杰。 2024.RQ-RAG：学习细化检索增强生成的查询。 arXiv abs/2404.00610 (2024)。 [13] Howard Chen、Ramakanth Pasunuru、Jason Weston 和 Asli Celikylmaz。 2023. 走入记忆迷宫：通过互动阅读超越语境限制。

### 段落 192 · Page 28

**EN**

arXiv abs/2310.05029 (2023). [14] Jiawei Chen, Hongyu Lin, Xianpei Han, and Le Sun. 2024. Benchmarking Large Language Models in Retrieval- Augmented Generation. Proceedings of the AAAI Conference on Artificial Intelligence 38, 16 (2024), 17754–17762. [15] Jiangui Chen, Ruqing Zhang, Jiafeng Guo, Yixing Fan, and Xueqi Cheng. 2022. GERE: Generative Evidence Retrieval for Fact Verification. In Proceedings of the 45th International ACM SIGIR Conference on Research and Development in , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

arXiv abs/2310.05029 (2023)。 [14] 陈家伟，林宏宇，韩先培，孙乐。 2024.检索增强生成中大型语言模型的基准测试。 AAAI 人工智能会议论文集 38, 16 (2024), 17754–17762。 [15]陈建贵，张如清，郭家峰，范艺兴，程学奇。 2022. GERE：用于事实验证的生成证据检索。第 45 届国际 ACM SIGIR 研究与开发会议论文集，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 29

### 段落 193 · Page 29

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 29 Information Retrieval. ACM.

**中文**

大型语言模型中检索增强文本生成的调查 29 信息检索。 ACM。

### 段落 194 · Page 29

**EN**

[16] Mark Chen, Jerry Tworek, Heewoo Jun, Qiming Yuan, Henrique Pondé de Oliveira Pinto, Jared Kaplan, Harrison Edwards, Yuri Burda, Nicholas Joseph, Greg Brockman, Alex Ray, Raul Puri, Gretchen Krueger, Michael Petrov, Heidy Khlaaf, Girish Sastry, Pamela Mishkin, Brooke Chan, Scott Gray, Nick Ryder, Mikhail Pavlov, Alethea Power, Lukasz Kaiser, Mohammad Bavarian, Clemens Winter, Philippe Tillet, Felipe Petroski Such, Dave Cummings, Matthias Plappert, Fotios Chantzis, Elizabeth Barnes, Ariel Herbert-Voss, William Hebgen Guss, Alex Nichol, Alex Paino, Nikolas Tezak, Jie Tang, Igor Babuschkin, Suchir Balaji, Shantanu Jain, William Saunders, Christopher Hesse, Andrew N.

**中文**

[16] Mark Chen、Jerry Tworek、Heewoo Jun、袁启明、Henrique Pondé de Oliveira Pinto、Jared Kaplan、Harrison Edwards、Yuri Burda、Nicholas Joseph、Greg Brockman、Alex Ray、Raul Puri、Gretchen Krueger、Michael Petrov、Heidy Khlaaf、Girish Sastry、Pamela Mishkin、Brooke Chan、Scott Gray、Nick Ryder、Mikhail巴甫洛夫、Alethea Power、卢卡斯·凯撒、穆罕默德·巴伐利亚、克莱门斯·温特、菲利普·蒂莱、费利佩·彼得罗斯基·萨奇、戴夫·卡明斯、马蒂亚斯·普拉珀特、福蒂奥斯·尚齐斯、伊丽莎白·巴恩斯、阿里尔·赫伯特-沃斯、威廉·赫伯根·格斯、亚历克斯·尼科尔、亚历克斯·帕诺、尼古拉斯·特扎克、唐杰、伊戈尔·巴布什金、苏奇尔·巴拉吉、尚塔努·杰恩、威廉·桑德斯、克里斯托弗·黑塞、安德鲁·N.

### 段落 195 · Page 29

**EN**

Carr, Jan Leike, Joshua Achiam, Vedant Misra, Evan Morikawa, Alec Radford, Matthew Knight, Miles Brundage, Mira Murati, Katie Mayer, Peter Welinder, Bob McGrew, Dario Amodei, Sam McCandlish, Ilya Sutskever, and Wojciech Zaremba. 2021. Evaluating Large Language Models Trained on Code. arXiv abs/2107.03374 (2021). [17] Wenhu Chen, Hexiang Hu, Xi Chen, Pat Verga, and William Cohen. 2022. MuRAG: Multimodal Retrieval-Augmented Generator for Open Question Answering over Images and Text. In Proceedings of the Conference on Empirical Methods in Natural Language Processing (EMNLP) . [18] Wenhu Chen, Hexiang Hu, Chitwan Saharia, and William W. Cohen.

**中文**

卡尔、简·雷克、约书亚·阿希亚姆、韦丹特·米斯拉、埃文·森川、亚历克·雷德福、马修·奈特、迈尔斯·布伦戴奇、米拉·穆拉蒂、凯蒂·梅耶尔、彼得·韦林德、鲍勃·麦格鲁、达里奥·阿莫代、萨姆·麦坎迪什、伊利亚·苏茨克弗和沃伊切赫·扎伦巴。 2021。评估在代码上训练的大型语言模型。 arXiv abs/2107.03374 (2021)。 [17] 陈文虎，胡鹤翔，陈曦，帕特·维尔加，威廉·科恩。 2022. MuRAG：用于图像和文本开放式问答的多模态检索增强生成。自然语言处理经验方法会议 (EMNLP) 会议记录。 [18] 陈文虎，胡鹤翔，Chitwan Saharia，William W. Cohen。

### 段落 196 · Page 29

**EN**

2023. Re-Imagen: Retrieval-Augmented Text-to- Image Generator. In International Conference on Learning Representations (ICLR) . [19] Zhihong Chen, Feng Jiang, Junying Chen, Tiannan Wang, Fei Yu, Guiming Chen, Hongbo Zhang, Juhao Liang, Chen Zhang, Zhiyi Zhang, Jianquan Li, Xiang Wan, Benyou Wang, and Haizhou Li. 2023. Phoenix: Democratizing ChatGPT across Languages. arXiv abs/2304.10453 (2023). [20] Daixuan Cheng, Shaohan Huang, Junyu Bi, Yuefeng Zhan, Jianfeng Liu, Yujing Wang, Hao Sun, Furu Wei, Weiwei Deng, and Qi Zhang. 2023. UPRISE: Universal Prompt Retrieval for Improving Zero-Shot Evaluation.

**中文**

2023.Re-Imagen：检索增强的文本到图像生成器。在国际学习表征会议（ICLR）中。 [19] 陈志宏，蒋峰，陈俊英，王天南，于飞，陈桂明，张宏波，梁巨豪，张陈，张志毅，李建全，万向，王本友，李海洲。 2023. Phoenix：跨语言的 ChatGPT 民主化。 arXiv abs/2304.10453 (2023)。 [20] 程代轩，黄少涵，毕俊宇，詹跃峰，刘剑锋，王玉静，孙浩，魏福如，邓伟伟，张琪。 2023. UPRISE：用于改进零样本评估的通用提示检索。

### 段落 197 · Page 29

**EN**

In Proceedings of the Conference on Empirical Methods in Natural Language Processing . Association for Computational Linguistics, 12318–12337. [21] Xin Cheng, Di Luo, Xiuying Chen, Lemao Liu, Dongyan Zhao, and Rui Yan. 2023. Lift Yourself Up: Retrieval-augmented Text Generation with Self-Memory.. In Conference on Neural Information Processing Systems (NeurIPS) . [22] Wei-Lin Chiang, Zhuohan Li, Zi Lin, Ying Sheng, Zhanghao Wu, Hao Zhang, Lianmin Zheng, Siyuan Zhuang, Yonghao Zhuang, Joseph E. Gonzalez, Ion Stoica, and Eric P. Xing. 2023. Vicuna: An Open-Source Chatbot Impressing GPT-4 with 90%* ChatGPT Quality.

**中文**

自然语言处理经验方法会议论文集。计算语言学协会，12318–12337。 [21] 程新，罗迪，陈秀英，刘乐茂，赵冬艳，严锐。 2023 年。提升自己：利用自我记忆进行检索增强文本生成。在神经信息处理系统 (NeurIPS) 会议上。 [22] 蒋伟林、李卓涵、林子、盛英、吴张浩、张浩、郑联民、庄思源、庄永浩、Joseph E. Gonzalez、Ion Stoica 和 Eric P. Xing。 2023.Vicuna：一款开源聊天机器人，以 90%* ChatGPT 质量给 GPT-4 留下深刻印象。

### 段落 198 · Page 29

**EN**

https://lmsys.org/blog/2023-03-30-vicuna/ [23] Aakanksha Chowdhery, Sharan Narang, Jacob Devlin, Maarten Bosma, Gaurav Mishra, Adam Roberts, Paul Barham, Hyung Won Chung, Charles Sutton, Sebastian Gehrmann, Parker Schuh, Kensen Shi, Sasha Tsvyashchenko, Joshua Maynez, Abhishek Rao, Parker Barnes, Yi Tay, Noam Shazeer, Vinodkumar Prabhakaran, Emily Reif, Nan Du, Ben Hutchinson, Reiner Pope, James Bradbury, Jacob Austin, Michael Isard, Guy Gur-Ari, Pengcheng Yin, Toju Duke, Anselm Levskaya, Sanjay Ghemawat, Sunipa Dev, Henryk Michalewski, Xavier Garcia, Vedant Misra, Kevin Robinson, Liam Fedus, Denny Zhou, Daphne Ippolito, David Luan, Hyeontaek Lim, Barret Zoph, Alexander Spiridonov, Ryan Sepassi, David Dohan, Shivani Agrawal, Mark Omernick, Andrew M.

**中文**

https://lmsys.org/blog/2023-03-30-vicuna/ [23] Aakanksha Chowdhery、Sharan Narang、Jacob Devlin、Maarten Bosma、Gaurav Mishra、Adam Roberts、Paul Barham、Hyung Won Chung、Charles Sutton、Sebastian Gehrmann、Parker Schuh、Kensen Shi、Sasha Tsvyashchenko、Joshua Maynez、Abhishek Rao、帕克·巴恩斯、Yi Tay、诺姆·沙泽尔、维诺库马尔·普拉巴卡兰、艾米丽·莱夫、Nan Du、本·哈钦森、莱纳·波普、詹姆斯·布拉德伯里、雅各布·奥斯汀、迈克尔·伊萨德、盖伊·古尔-阿里、彭城尹、Toju Duke、安塞姆·列夫斯卡亚、桑杰·格马瓦特、苏尼帕·戴夫、亨利克·米查莱夫斯基、泽维尔·加西亚、韦丹特·米斯拉、凯文Robinson、Liam Fedus、Denny Zhou、Daphne Ippolito、David Luan、Hyeontaek Lim、Barret Zoph、Alexander Spiridonov、Ryan Sepassi、David Dohan、Shivani Agrawal、Mark Omernick、Andrew M.

### 段落 199 · Page 29

**EN**

Dai, Thanumalayan Sankaranarayana Pillai, Marie Pellat, Aitor Lewkowycz, Erica Moreira, Rewon Child, Oleksandr Polozov, Katherine Lee, Zongwei Zhou, Xuezhi Wang, Brennan Saeta, Mark Diaz, Orhan Firat, Michele Catasta, Jason Wei, Kathy Meier-Hellstern, Douglas Eck, Jeff Dean, Slav Petrov, and Noah Fiedel. 2023. PaLM: Scaling Language Modeling with Pathways. Journal of Machine Learning Research (JMLR) 24 (2023), 240:1–240:113.

**中文**

Dai、Thanumalayan Sankaranarayana Pillai、Marie Pellat、Aitor Lewkowycz、Erica Moreira、Rewon Child、Oleksandr Polozov、Katherine Lee、Zongwei Zhou、Xuezhi Wang、Brennan Saeta、Mark Diaz、Orhan Firat、Michele Catasta、Jason Wei、Kathy Meier-Hellstern、Douglas Eck、Jeff Dean、Slav Petrov 和诺亚·菲德尔. 2023.PaLM：通过路径扩展语言建模。机器学习研究杂志 (JMLR) 24 (2023), 240:1–240:113。

### 段落 200 · Page 29

**EN**

[24] Hyung Won Chung, Le Hou, Shayne Longpre, Barret Zoph, Yi Tay, William Fedus, Yunxuan Li, Xuezhi Wang, Mostafa Dehghani, Siddhartha Brahma, Albert Webson, Shixiang Shane Gu, Zhuyun Dai, Mirac Suzgun, Xinyun Chen, Aakanksha Chowdhery, Alex Castro-Ros, Marie Pellat, Kevin Robinson, Dasha Valter, Sharan Narang, Gaurav Mishra, Adams Yu, Vincent Zhao, Yanping Huang, Andrew Dai, Hongkun Yu, Slav Petrov, Ed H. Chi, Jeff Dean, Jacob Devlin, Adam Roberts, Denny Zhou, Quoc V. Le, and Jason Wei. 2022. Scaling Instruction-Finetuned Language Models. arXiv abs/2210.11416 (2022).

**中文**

[24] Hyung Won Chung、Le Hou、Shayne Longpre、Barret Zoph、Yi Tay、William Fedus、李云轩、Xuezhi Wang、Mostafa Dehghani、Siddhartha Brahma、Albert Webson、Shiyang Shane Gu、Zhuyun Dai、Mirac Suzgun、Xinyun Chen、Aakanksha Chowdhery、Alex Castro-Ros、Marie Pellat、Kevin Robinson、Dasha Valter、Sharan Narang、Gaurav Mishra、Adams Yu、Vincent Zhao、Yanping Huang、Andrew Dai、hongkun Yu、Slav Petrov、Ed H. Chi、Jeff Dean、Jacob Devlin、Adam Roberts、Denny Zhou、Quoc V. Le 和 Jason Wei。 2022.扩展指令微调语言模型。 arXiv abs/2210.11416 (2022)。

### 段落 201 · Page 29

**EN**

[25] Alexis Conneau, Kartikay Khandelwal, Naman Goyal, Vishrav Chaudhary, Guillaume Wenzek, Francisco Guzmán, Edouard Grave, Myle Ott, Luke Zettlemoyer, and Veselin Stoyanov. 2020. Unsupervised Cross-lingual Representation Learning at Scale. InProceedings of the 58th Annual Meeting of the Association for Computational Linguistics. Association for Computational Linguistics, 8440–8451. [26] Florin Cuconasu, Giovanni Trappolini, Federico Siciliano, Simone Filice, Cesare Campagnano, Yoelle Maarek, Nicola Tonellotto, and Fabrizio Silvestri. 2024. The Power of Noise: Redefining Retrieval for RAG Systems.

**中文**

[25] Alexis Conneau、Kartikay Khandelwal、Naman Goyal、Vishrav Chaudhary、Guillaume Wenzek、Francisco Guzmán、Edouard Grave、Myle Ott、Luke Zettlemoyer 和 Veselin Stoyanov。 2020。大规模无监督跨语言表示学习。计算语言学协会第 58 届年会记录。计算语言学协会，8440–8451。 [26] Florin Cuconasu、Giovanni Trappolini、Federico Siciliano、Simone Filice、Cesare Campagnano、Yoelle Maarek、Nicola Tonellotto 和 Fabrizio Silvestri。 2024 年。噪声的力量：重新定义 RAG 系统的检索。

### 段落 202 · Page 29

**EN**

In Annual International ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR), Vol. abs/2401.14887. [27] Zhuyun Dai, Vincent Y. Zhao, Ji Ma, Yi Luan, Jianmo Ni, Jing Lu, Anton Bakalov, Kelvin Guu, Keith B. Hall, and Ming-Wei Chang. 2023. Promptagator: Few-shot Dense Retrieval From 8 Examples. In International Conference on Learning Representations (ICLR). [28] Mayur Datar, Nicole Immorlica, Piotr Indyk, and Vahab S. Mirrokni. 2004. Locality-sensitive hashing scheme based on p-stable distributions.. In International Symposium on Computational Geometry (SoCG) . 253–262. , Vol. 1, No. 1, Article .

**中文**

在年度国际 ACM SIGIR 信息检索研究与开发会议 (SIGIR) 中，卷。绝对/2401.14887。 [27]戴竹云、赵文森、马季、栾毅、倪建模、陆静、安东·巴卡洛夫、顾凯文、基思·B·霍尔、张明伟。 2023. Promptagator：8 个示例的少样本密集检索。在国际学习表征会议（ICLR）中。 [28] Mayur Datar、Nicole Immorlica、Piotr Indyk 和 Vahab S. Mirrokni。 2004年。基于p稳定分布的局部敏感哈希方案。在国际计算几何研讨会（SoCG）中。 253–262。，卷。 1、第1条。

### 段落 203 · Page 29

**EN**

Publication date: August 2018.

**中文**

出版日期：2018 年 8 月。

### Page 30

### 段落 204 · Page 30

**EN**

30 Huang et al. [29] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. 2019. BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. InProceedings of the Conference of the North. Association for Computational Linguistics, 4171–4186. [30] Emily Dinan, Stephen Roller, Kurt Shuster, Angela Fan, Michael Auli, and Jason Weston. 2019. Wizard of Wikipedia: Knowledge-Powered Conversational Agents. In International Conference on Learning Representations (ICLR) . [31] Zhengxiao Du, Yujie Qian, Xiao Liu, Ming Ding, Jiezhong Qiu, Zhilin Yang, and Jie Tang. 2022.

**中文**

30 黄等人。 [29] Jacob Devlin、Ming-Wei Chang、Kenton Lee 和 Kristina Toutanova。 2019.BERT：用于语言理解的深度双向Transformer的预训练。在北方会议记录中。计算语言学协会，4171–4186。 [30] 艾米丽·迪南、斯蒂芬·罗勒、库尔特·舒斯特、安吉拉·范、迈克尔·奥利和杰森·韦斯顿。 2019. 维基百科向导：知识驱动的对话代理。在国际学习表征会议（ICLR）中。 [31] 杜正晓，钱玉杰，刘晓，丁明，邱杰中，杨志林，唐杰。 2022 年。

### 段落 205 · Page 30

**EN**

GLM: General Language Model Pretraining with Autoregressive Blank Infilling. In Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) . Association for Computational Linguistics. [32] Hady ElSahar, Pavlos Vougiouklis, Arslen Remaci, Christophe Gravier, Jonathon S. Hare, Frédérique Laforest, and Elena Simperl. 2018. T-REx: A Large Scale Alignment of Natural Language with Knowledge Base Triples. In International Conference on Language Resources and Evaluation (LREC) . [33] Shahul ES, Jithin James, Luis Espinosa Anke, and Steven Schockaert. 2023.

**中文**

GLM：具有自回归空白填充的通用语言模型预训练。计算语言学协会第 60 届年会论文集（第一卷：长论文）。计算语言学协会。 [32]Hady ElSahar、Pavlos Vougiouklis、Arslen Remaci、Christophe Gravier、Jonathon S. Hare、Frédérique Laforest 和 Elena Simperl。 2018。T-REx：自然语言与知识库三元组的大规模对齐。在国际语言资源与评估会议（LREC）中。 [33] Shahul ES、Jithin James、Luis Espinosa Anke 和 Steven Schockaert。 2023 年。

### 段落 206 · Page 30

**EN**

RAGAs: Automated Evaluation of Retrieval Augmented Generation. Conference of the European Chapter of the Association for Computational Linguistics abs/2309.15217 (2023). [34] Zhangyin Feng, Xiaocheng Feng, Dezhi Zhao, Maojin Yang, and Bing Qin. 2024. Retrieval-Generation Synergy Augmented Large Language Models. In IEEE International Conference on Acoustics, Speech, and Signal Processing , Vol. abs/2310.05149. IEEE. [35] Leo Gao, Stella Biderman, Sid Black, Laurence Golding, Travis Hoppe, Charles Foster, Jason Phang, Horace He, Anish Thite, Noa Nabeshima, Shawn Presser, and Connor Leahy. 2021.

**中文**

RAGA：检索增强生成的自动评估。计算语言学协会欧洲分会会议abs/2309.15217 (2023)。 [34] 冯章印，冯晓成，赵德志，杨茂金，秦冰。 2024.检索生成协同增强大型语言模型。在 IEEE 国际声学、语音和信号处理会议，卷。绝对/2310.05149。 IEEE。 [35] Leo Gau、Stella Biderman、Sid Black、Laurence Golding、Travis Hoppe、Charles Foster、Jason Phang、Horace He、Anish Thite、Noa Nabeshima、Shawn Presser 和 Connor Leahy。 2021 年。

### 段落 207 · Page 30

**EN**

The Pile: An 800GB Dataset of Diverse Text for Language Modeling. arXiv abs/2101.00027 (2021). [36] Luyu Gao, Xueguang Ma, Jimmy Lin, and Jamie Callan. 2023. Precise Zero-Shot Dense Retrieval without Relevance Labels. In Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers). Association for Computational Linguistics, 1762–1777. [37] Tianyu Gao, Xingcheng Yao, and Danqi Chen. 2021. SimCSE: Simple Contrastive Learning of Sentence Embeddings. In Proceedings of the Conference on Empirical Methods in Natural Language Processing . Association for Computational Linguistics, 6894–6910.

**中文**

The Pile：用于语言建模的 800GB 不同文本数据集。 arXiv abs/2101.00027 (2021)。 [36] 高鲁宇，马雪光，林吉米，杰米·卡伦。 2023.无需相关标签的精确零样本密集检索。计算语言学协会第 61 届年会论文集（第一卷：长论文）。计算语言学协会，1762-1777。 [37] 高天宇，姚兴成，陈丹琪。 2021.SimCSE：句子嵌入的简单对比学习。自然语言处理经验方法会议论文集。计算语言学协会，6894–6910。

### 段落 208 · Page 30

**EN**

[38] Yunfan Gao, Yun Xiong, Xinyu Gao, Kangxiang Jia, Jinliu Pan, Yuxi Bi, Yi Dai, Jiawei Sun, Meng Wang, and Haofen Wang. 2023. Retrieval-Augmented Generation for Large Language Models: A Survey. arXiv abs/2312.10997 (2023). [39] Yunfan Gao, Yun Xiong, Meng Wang, and Haofen Wang. 2024. Modular RAG: Transforming RAG Systems into LEGO-like Reconfigurable Frameworks. arXiv (2024). [40] Michael Glass, Gaetano Rossiello, Md Faisal Mahbub Chowdhury, Ankita Naik, Pengshan Cai, and Alfio Gliozzo. 2022. Re2G: Retrieve, Rerank, Generate.

**中文**

[38] 高云帆，熊云，高新宇，贾康祥，潘金六，毕玉玺，戴毅，孙家伟，王猛，王浩芬。 2023.大型语言模型的检索增强生成：一项调查。 arXiv abs/2312.10997 (2023)。 [39] 高云帆，熊云，王猛，王浩芬。 2024. 模块化 RAG：将 RAG 系统转变为类似乐高的可重构框架。 arXiv (2024)。 [40] Michael Glass、Gaetano Rossiello、Md Faisal Mahbub Chowdhury、Ankita Naik、Pengshan Cai 和 Alfio Gliozzo。 2022.Re2G：检索、重新排序、生成。

### 段落 209 · Page 30

**EN**

In Proceedings of the Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies . Association for Computational Linguistics, 2701–2715. [41] Simon Gottschalk and Elena Demidova. 2018. EventKG: A Multilingual Event-Centric Temporal Knowledge Graph . Springer International Publishing. 272–287 pages. [42] Kelvin Guu, Kenton Lee, Zora Tung, Panupong Pasupat, and Ming-Wei Chang. 2020. Retrieval Augmented Language Model Pre-Training. In International Conference on Machine Learning (ICML) . 3929–3938. [43] William L. Hamilton. 2020. Graph representation learning.

**中文**

计算语言学协会北美分会会议记录：人类语言技术。计算语言学协会，2701-2715。 [41] 西蒙·戈特沙克和埃琳娜·德米多娃。 2018.EventKG：以事件为中心的多语言时态知识图。施普林格国际出版社。 272–287 页。 [42] Kelvin Guu、Kenton Lee、Zora Tung、Panupong Pasupat 和 Ming-Wei Chang。 2020.检索增强语言模型预训练。在国际机器学习会议（ICML）中。 3929–3938。 [43] 威廉·L·汉密尔顿。 2020.图表示学习。

### 段落 210 · Page 30

**EN**

Springer International Publishing. [44] Micheline Hancock-Beaulieu, Mike Gatford, Xiangji Huang, Stephen E. Robertson, Steve Walker, and P. W. Williams. 1996. Okapi at TREC-5. In Proceedings of The Fifth Text REtrieval Conference, TREC 1996, Gaithersburg, Maryland, USA, November 20-22, 1996 (NIST Special Publication, Vol. 500-238) , Ellen M. Voorhees and Donna K. Harman (Eds.). National Institute of Standards and Technology (NIST). http://trec.nist.gov/pubs/trec5/papers/city.procpaper.ps.gz [45] Dan Hendrycks, Collin Burns, Steven Basart, Andy Zou, Mantas Mazeika, Dawn Song, and Jacob Steinhardt. 2021.

**中文**

施普林格国际出版社。 [44] Micheline Hancock-Beaulieu、Mike Gatford、Xiangji Huang、Stephen E. Robertson、Steve Walker 和 P. W. Williams。 1996. 霍加狓在 TREC-5。第五届文本检索会议记录，TREC 1996，美国马里兰州盖瑟斯堡，1996 年 11 月 20-22 日（NIST 特别出版物，第 500-238 卷），Ellen M. Voorhees 和 Donna K. Harman（编辑）。美国国家标准与技术研究院 (NIST)。 http://trec.nist.gov/pubs/trec5/papers/city.procpaper.ps.gz [45] Dan Hendrycks、Collin Burns、Steven Basart、Andy Zou、Mantas Mazeika、Dawn Song 和 Jacob Steinhardt。 2021 年。

### 段落 211 · Page 30

**EN**

Measuring Massive Multitask Language Understanding.. In International Conference on Learning Representations (ICLR). [46] Enrique HerreraViedma, Gabriella Pasi, Antonio G. LopezHerrera, and Carlos Porcel. 2006. Evaluating the information quality of Web sites: A methodology based on fuzzy computing with words. Journal of the American Society for Information Science and Technology 57, 4 (2006), 538–549. [47] Sebastian Hofstätter, Jiecao Chen, Karthik Raman, and Hamed Zamani. 2023. Fid-light: Efficient and effective retrievalaugmented text generation.

**中文**

测量大规模多任务语言理解。在国际学习表示会议 (ICLR) 中。 [46] Enrique HerreraViedma、Gabriella Pasi、Antonio G. LopezHerrera 和 Carlos Porcel。 2006.评估网站的信息质量：基于文字模糊计算的方法。美国信息科学与技术学会杂志 57, 4 (2006), 538–549。 [47] Sebastian Hofstätter、Jiecao Chen、Karthik Raman 和 Hamed Zamani。 2023.Fid-light：高效且有效的检索增强文本生成。

### 段落 212 · Page 30

**EN**

InProceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval. 1437–1447. [48] Yucheng Hu and Yuxing Lu. 2024. RAG and RAU: A Survey on Retrieval-Augmented Language Model in Natural Language Processing. arXiv abs/2404.19543 (2024). [49] Ziniu Hu, Ahmet Iscen, Chen Sun, Zirui Wang, Kai-Wei Chang, Yizhou Sun, Cordelia Schmid, David A. Ross, and Alireza Fathi. 2023. Reveal: Retrieval-Augmented Visual-Language Pre-Training with Multi-Source Multimodal Knowledge Memory. In 2023 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR) . IEEE, 23369– 23379. , Vol. 1, No. 1, Article .

**中文**

第 46 届国际 ACM SIGIR 信息检索研究与发展会议论文集。 1437–1447。 [48] 胡玉成，陆玉兴. 2024. RAG 和 RAU：自然语言处理中检索增强语言模型的调查。 arXiv abs/2404.19543 (2024)。 [49] 胡紫牛，艾哈迈德·伊森，孙晨，王自瑞，张凯伟，孙一舟，Cordelia Schmid，David A. Ross，Alireza Fathi。 2023.揭示：利用多源多模态知识记忆进行检索增强视觉语言预训练。 2023 年 IEEE/CVF 计算机视觉与模式识别会议 (CVPR)。 IEEE，23369–23379。，卷。 1、第1条。

### 段落 213 · Page 30

**EN**

Publication date: August 2018.

**中文**

出版日期：2018 年 8 月。

### Page 31

### 段落 214 · Page 31

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 31 [50] Jie Huang, Hanyin Shao, Kevin Chen-Chuan Chang, Jinjun Xiong, and Wen-mei Hwu. 2022. Understanding Jargon: Combining Extraction and Generation for Definition Modeling. In Proceedings of the Conference on Empirical Methods in Natural Language Processing . Association for Computational Linguistics. [51] Jimmy Xiangji Huang, Jun Miao, and Ben He. 2013. High performance query expansion using adaptive co-training. Inf. Process. Manag. 49, 2 (2013), 441–453.

**中文**

大型语言模型中检索增强文本生成的综述 31 [50] Jie Huang，Hanyin Shao，Kevin Chen-Chuan Chang，Jinjun Xiong 和 Wen-mei Hwu。 2022。理解行话：结合提取和生成进行定义建模。自然语言处理经验方法会议论文集。计算语言学协会。 [51] 黄向吉，苗军，何本。 2013。使用自适应协同训练的高性能查询扩展。信息。过程。马纳格。 49、2（2013）、441-453。

### 段落 215 · Page 31

**EN**

https://doi.org/10.1016/J.IPM.2012.08.002 [52] Qiushi Huang, Shuai Fu, Xubo Liu, Wenwu Wang, Tom Ko, Yu Zhang, and Lilian H. Y. Tang. 2023. Learning Retrieval Augmentation for Personalized Dialogue Generation.. In Conference on Empirical Methods in Natural Language Processing (EMNLP). 2523–2540. [53] Wenyu Huang, Mirella Lapata, Pavlos Vougiouklis, Nikos Papasarantopoulos, and Jeff Z Pan. 2023. Retrieval Augmented Generation with Rich Answer Encoding. Proc. of IJCNLP-AACL 2023 (2023). [54] Xiangji Huang and Qinmin Hu. 2009. A bayesian learning approach to promoting diversity in ranking for biomedical information retrieval.

**中文**

https://doi.org/10.1016/J.IPM.2012.08.002 [52] 黄秋实，付帅，刘旭波，王文武，Tom Ko，张宇，Lilian H. Y. Tang。 2023 年。个性化对话生成的学习检索增强。自然语言处理经验方法会议 (EMNLP)。 2523–2540。 [53] 黄文宇、Mirella Lapata、Pavlos Vougiouklis、Nikos Papasarantopoulos 和 Jeff Z Pan。 2023.具有丰富答案编码的检索增强生成。过程。 IJCNLP-AACL 2023 (2023)。 [54] 黄向吉，胡钦民。 2009.促进生物医学信息检索排名多样性的贝叶斯学习方法。

### 段落 216 · Page 31

**EN**

In Proceedings of the 32nd Annual International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2009, Boston, MA, USA, July 19-23, 2009 , James Allan, Javed A. Aslam, Mark Sanderson, ChengXiang Zhai, and Justin Zobel (Eds.). ACM, 307–314. https://doi.org/10.1145/1571941.1571995 [55] Yizheng Huang and Jimmy Huang. 2024. Exploring ChatGPT for Next-generation Information Retrieval: Opportunities and Challenges. CoRR abs/2402.11203 (2024). https://doi.org/10.48550/ARXIV.2402.11203 arXiv:2402.11203 [56] Yizheng Huang and Jimmy X. Huang. 2023.

**中文**

第 32 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR 2009，美国马萨诸塞州波士顿，2009 年 7 月 19-23 日，James Allan、Javed A. Aslam、Mark Sanderson、ChengXiang Zhai 和 Justin Zobel（编辑）。 ACM，307-314。 https://doi.org/10.1145/1571941.1571995 [55] 黄一正和吉米黄。 2024 年。探索下一代信息检索的 ChatGPT：机遇与挑战。 CoRR 绝对/2402.11203 (2024)。 https://doi.org/10.48550/ARXIV.2402.11203 arXiv:2402.11203 [56] Yizheng Huang 和 Jimmy X. Huang。 2023 年。

### 段落 217 · Page 31

**EN**

Diversified Prior Knowledge Enhanced General Language Model for Biomedical Information Retrieval. In ECAI 2023 - 26th European Conference on Artificial Intelligence, September 30 - October 4, 2023, Kraków, Poland - Including 12th Conference on Prestigious Applications of Intelligent Systems (PAIS 2023) (Frontiers in Artificial Intelligence and Applications, Vol. 372) , Kobi Gal, Ann Nowé, Grzegorz J. Nalepa, Roy Fairstein, and Roxana Radulescu (Eds.). IOS Press, 1109–1115. https://doi.org/10.3233/FAIA230385 [57] Gautier Izacard, Mathilde Caron, Lucas Hosseini, Sebastian Riedel, Piotr Bojanowski, Armand Joulin, and Edouard Grave. 2022.

**中文**

多样化的先验知识增强了生物医学信息检索的通用语言模型。 ECAI 2023 - 第 26 届欧洲人工智能会议，2023 年 9 月 30 日至 10 月 4 日，波兰克拉科夫 - 包括第 12 届智能系统著名应用会议 (PAIS 2023)（人工智能和应用前沿，第 372 卷），Kobi Gal、Ann Nowé、Grzegorz J. Nalepa、Roy Fairstein 和 Roxana拉杜列斯库（编辑）。 IOS 出版社，1109–1115。 https://doi.org/10.3233/FAIA230385 [57] Gautier Izacard、Mathilde Caron、Lucas Hosseini、Sebastian Riedel、Piotr Bojanowski、Armand Joulin 和 Edouard Grave。 2022 年。

### 段落 218 · Page 31

**EN**

Unsupervised Dense Information Retrieval with Contrastive Learning. Transactions on Machine Learning Research (TMLR) 2022 (2022). [58] Gautier Izacard and Edouard Grave. 2021. Leveraging Passage Retrieval with Generative Models for Open Domain Question Answering. In Proceedings of the 16th Conference of the European Chapter of the Association for Computational Linguistics: Main Volume. Association for Computational Linguistics, 874–880. [59] Gautier Izacard, Patrick S. H. Lewis, Maria Lomeli, Lucas Hosseini, Fabio Petroni, Timo Schick, Jane Dwivedi-Yu, Armand Joulin, Sebastian Riedel, and Edouard Grave. 2023.

**中文**

通过对比学习进行无监督密集信息检索。机器学习研究汇刊 (TMLR) 2022 (2022)。 [58]戈蒂埃·伊扎卡尔和爱德华·格雷夫。 2021。利用段落检索和生成模型进行开放域问答。计算语言学协会欧洲分会第 16 届会议记录：主卷。计算语言学协会，874–880。 [59] Gautier Izacard、Patrick S. H. Lewis、Maria Lomeli、Lucas Hosseini、Fabio Petroni、Timo Schick、Jane Dwivedi-Yu、Armand Joulin、Sebastian Riedel 和 Edouard Grave。 2023 年。

### 段落 219 · Page 31

**EN**

Atlas: Few-shot Learning with Retrieval Augmented Language Models. Journal of Machine Learning Research (JMLR) 24 (2023), 251:1–251:43. [60] Israt Jahan, Md. Tahmid Rahman Laskar, Chun Peng, and Jimmy Xiangji Huang. 2023. Evaluation of ChatGPT on Biomedical Tasks: A Zero-Shot Comparison with Fine-Tuned Generative Transformers. CoRR abs/2306.04504 (2023). https://doi.org/10.48550/ARXIV.2306.04504 arXiv:2306.04504 [61] Bernard J. Jansen, Danielle L. Booth, and Amanda Spink. 2009. Patterns of query reformulation during Web searching. J. Assoc. Inf. Sci. Technol. 60, 7 (2009), 1358–1371.

**中文**

Atlas：使用检索增强语言模型进行少样本学习。机器学习研究杂志 (JMLR) 24 (2023), 251:1–251:43。 [60] Israt Jahan、Md. Tahmid Rahman Laskar、Chun Peng 和 Jimmy Shangji Huang。 2023. ChatGPT 在生物医学任务上的评估：与微调生成Transformer的零样本比较。 CoRR 绝对/2306.04504 (2023)。 https://doi.org/10.48550/ARXIV.2306.04504 arXiv:2306.04504 [61] Bernard J. Jansen、Danielle L. Booth 和 Amanda Spink。 2009 年。网络搜索期间查询重构的模式。 J.副教授。信息。科学。技术。 60, 7 (2009), 1358–1371。

### 段落 220 · Page 31

**EN**

https://doi.org/10.1002/ASI.21071 [62] H Jégou, M Douze, and C Schmid. 2011. Product Quantization for Nearest Neighbor Search. IEEE Transactions on Pattern Analysis and Machine Intelligence 33, 1 (2011), 117–128. [63] Wenqi Jiang, Marco Zeller, Roger Waleffe, Torsten Hoefler, and Gustavo Alonso. 2023. Chameleon: a Heterogeneous and Disaggregated Accelerator System for Retrieval-Augmented Language Models. arXiv abs/2310.09949 (2023). [64] Wenqi Jiang, Shuai Zhang, Boran Han, Jie Wang, Bernie Wang, and Tim Kraska. 2024. PipeRAG: Fast Retrieval- Augmented Generation via Algorithm-System Co-design. arXiv abs/2403.05676 (2024).

**中文**

https://doi.org/10.1002/ASI.21071 [62] H Jégou、M Douze 和 C Schmid。 2011。最近邻搜索的产品量化。 IEEE 模式分析和机器智能汇刊 33, 1 (2011), 117–128。 [63] 蒋文琪、Marco Zeller、Roger Waleffe、Torsten Hoefler 和 Gustavo Alonso。 2023.Chameleon：用于检索增强语言模型的异构和分解加速器系统。 arXiv abs/2310.09949 (2023)。 [64]姜文琪，张帅，韩博兰，王杰，Bernie Wang，Tim Kraska。 2024.PipeRAG：通过算法系统协同设计快速检索-增强生成。 arXiv abs/2403.05676 (2024)。

### 段落 221 · Page 31

**EN**

[65] Zhengbao Jiang, Frank F. Xu, Luyu Gao, Zhiqing Sun, Qian Liu, Jane Dwivedi-Yu, Yiming Yang, Jamie Callan, and Graham Neubig. 2023. Active Retrieval Augmented Generation. In Conference on Empirical Methods in Natural Language Processing (EMNLP). 7969–7992. [66] Di Jin, Eileen Pan, Nassim Oufattole, Wei-Hung Weng, Hanyi Fang, and Peter Szolovits. 2021. What Disease Does This Patient Have? A Large-Scale Open Domain Question Answering Dataset from Medical Exams. Applied Sciences 11, 14 (2021), 6421. [67] Qiao Jin, Bhuwan Dhingra, Zhengping Liu, William W. Cohen, and Xinghua Lu. 2019.

**中文**

[65] 姜正宝，Frank F. Xu，高鲁宇，孙志清，刘谦，Jane Dwivedi-Yu，杨一鸣，Jamie Callan，Graham Neubig。 2023.主动检索增强生成。在自然语言处理经验方法会议（EMNLP）中。 7969–7992。 [66] 金迪，潘艾琳，Nassim Oufattole，翁伟宏，方汉仪，Peter Szolovits。 2021. 这位患者得什么病？来自医学检查的大规模开放域问答数据集。应用科学 11, 14 (2021), 6421。 [67] Qiao Jin、Bhuwan Dhingra、Zhengping Liu、William W. Cohen 和 Xinghua Lu。 2019.

### 段落 222 · Page 31

**EN**

PubMedQA: A Dataset for Biomedical Research Question Answering.. In Conference on Empirical Methods in Natural Language Processing (EMNLP). 2567–2577. [68] Jeff Johnson, Matthijs Douze, and Hervé Jégou. 2021. Billion-Scale Similarity Search with GPUs. IEEE Transactions on Big Data 7, 3 (2021), 535–547. https://doi.org/10.1109/TBDATA.2019.2921572 [69] Mandar Joshi, Eunsol Choi, Daniel Weld, and Luke Zettlemoyer. 2017. TriviaQA: A Large Scale Distantly Supervised Challenge Dataset for Reading Comprehension. In Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) .

**中文**

PubMedQA：生物医学研究问答数据集。自然语言处理经验方法会议 (EMNLP)。 2567–2577。 [68] 杰夫·约翰逊、马蒂斯·杜兹和埃尔韦·杰古。 2021 年。使用 GPU 进行十亿级相似性搜索。 IEEE 大数据汇刊 7, 3 (2021), 535–547。 https://doi.org/10.1109/TBDATA.2019.2921572 [69] Mandar Joshi、Eunsol Choi、Daniel Weld 和 Luke Zettlemoyer。 2017.TriviaQA：用于阅读理解的大规模远程监督挑战数据集。计算语言学协会第 55 届年会论文集（第一卷：长论文）。

### 段落 223 · Page 31

**EN**

Association for Computational Linguistics, 1601–1611. [70] Minki Kang, Jin Myung Kwak, Jinheon Baek, and Sung Ju Hwang. 2023. Knowledge Graph-Augmented Language Models for Knowledge-Grounded Dialogue Generation. arXiv abs/2305.18846 (2023). , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

计算语言学协会，1601-1611。 [70] Minki Kang、Jin Myung Kwak、Jinheon Baek 和 Sung Ju Hwang。 2023.用于知识基础对话生成的知识图增强语言模型。 arXiv abs/2305.18846 (2023)。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 32

### 段落 224 · Page 32

**EN**

32 Huang et al. [71] Vladimir Karpukhin, Barlas Oguz, Sewon Min, Patrick S. H. Lewis, Ledell Wu, Sergey Edunov, Danqi Chen, and Wen-tau Yih. 2020. Dense Passage Retrieval for Open-Domain Question Answering.. In Conference on Empirical Methods in Natural Language Processing (EMNLP) . 6769–6781. [72] Urvashi Khandelwal, Omer Levy, Dan Jurafsky, Luke Zettlemoyer, and Mike Lewis. 2020. Generalization through Memorization: Nearest Neighbor Language Models. In International Conference on Learning Representations (ICLR) . [73] Omar Khattab, Keshav Santhanam, Xiang Lisa Li, David Hall, Percy Liang, Christopher Potts, and Matei Zaharia. 2022.

**中文**

32 黄等人。 [71] Vladimir Karpukhin、Barlas Oguz、Sewon Min、Patrick S. H. Lewis、Ledell Wu、Sergey Edunov、Danqi Chen 和 Wen-tau Yih。 2020.用于开放域问答的密集段落检索..在自然语言处理经验方法会议（EMNLP）中。 6769–6781。 [72] Urvashi Khandelwal、Omer Levy、Dan Jurafsky、Luke Zettlemoyer 和 Mike Lewis。 2020。通过记忆进行泛化：最近邻语言模型。在国际学习表征会议（ICLR）中。 [73] Omar Khattab、Keshav Santhanam、Xiang Lisa Li、David Hall、Percy Liang、Christopher Potts 和 Matei Zaharia。 2022 年。

### 段落 225 · Page 32

**EN**

Demonstrate-Search-Predict: Composing retrieval and language models for knowledge-intensive NLP. arXiv abs/2212.14024 (2022). [74] Omar Khattab and Matei Zaharia. 2020. ColBERT - Efficient and Effective Passage Search via Contextualized Late Interaction over BERT. In Proceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval. ACM, 39–48. [75] Sanghoon Kim, Dahyun Kim, Chanjun Park, Wonsung Lee, Wonho Song, Yunsu Kim, Hyeonwoo Kim, Yungi Kim, Hyeonju Lee, Jihoo Kim, Changbae Ahn, Seonghoon Yang, Sukyung Lee, Hyunbyung Park, Gyoungjin Gim, Mikyoung Cha, Hwalsuk Lee, and Sunghun Kim. 2024.

**中文**

演示-搜索-预测：为知识密集型 NLP 构建检索和语言模型。 arXiv abs/2212.14024 (2022)。 [74] 奥马尔·哈塔布和马泰·扎哈里亚。 2020. ColBERT - 通过 BERT 上的上下文化后期交互实现高效且有效的段落搜索。第 43 届国际 ACM SIGIR 信息检索研究与开发会议论文集。 ACM，39-48。 [75] Sanghoon Kim、Dahyun Kim、Chanjun Park、Wonsung Lee、Wonho Song、Yunsu Kim、Hyeonwoo Kim、Yungi Kim、Hyeonju Lee、Jihoo Kim、Changbae Ahn、Seonghoon Yang、Sukyung Lee、Hyunbyung Park、Gyoungjin Gim、Mikyoung Cha、Hwalsuk Lee和Sunghun Kim。 2024 年。

### 段落 226 · Page 32

**EN**

SOLAR 10.7B: Scaling Large Language Models with Simple yet Effective Depth Up-Scaling. In Proceedings of the Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 6: Industry Track) , Vol. abs/2312.15166. Association for Computational Linguistics. [76] Tom Kwiatkowski, Jennimaria Palomaki, Olivia Redfield, Michael Collins, Ankur Parikh, Chris Alberti, Danielle Epstein, Illia Polosukhin, Jacob Devlin, Kenton Lee, Kristina Toutanova, Llion Jones, Matthew Kelcey, Ming-Wei Chang, Andrew M. Dai, Jakob Uszkoreit, Quoc Le, and Slav Petrov. 2019.

**中文**

SOLAR 10.7B：通过简单而有效的深度扩展来扩展大型语言模型。计算语言学协会北美分会会议记录：人类语言技术（第 6 卷：行业轨道），第 1 卷。绝对/2312.15166。计算语言学协会。 [76] Tom Kwiatkowski、Jennimaria Palomaki、Olivia Redfield、Michael Collins、Ankur Parikh、Chris Alberti、Danielle Epstein、Illia Polosukhin、Jacob Devlin、Kenton Lee、Kristina Toutanova、Llion Jones、Matthew Kelcey、Ming-Wei Chang、Andrew M. Dai、Jakob Uszkoreit、Quoc Le 和 Slav Petrov。 2019.

### 段落 227 · Page 32

**EN**

Natural Questions: A Benchmark for Question Answering Research. Transactions of the Association for Computational Linguistics 7 (2019), 453–466. [77] Md. Tahmid Rahman Laskar, M. Saiful Bari, Mizanur Rahman, Md Amran Hossen Bhuiyan, Shafiq Joty, and Jimmy Xiangji Huang. 2023. A Systematic Study and Comprehensive Evaluation of ChatGPT on Benchmark Datasets. CoRR abs/2305.18486 (2023). https://doi.org/10.48550/ARXIV.2305.18486 arXiv:2305.18486 [78] Md. Tahmid Rahman Laskar, Enamul Hoque, and Jimmy X. Huang. 2020. Query Focused Abstractive Summarization via Incorporating Query Relevance and Transfer Learning with Transformer Models.

**中文**

自然问题：问答研究的基准。计算语言学协会汇刊 7 (2019), 453–466。 [77] Md. Tahmid Rahman Laskar、M. Saiful Bari、Mizanur Ra​​hman、Md Amran Hossen Bhuiyan、Shafiq Joty 和 Jimmy Shangji Huang。 2023. ChatGPT 在基准数据集上的系统研究和综合评价。 CoRR 绝对/2305.18486 (2023)。 https://doi.org/10.48550/ARXIV.2305.18486 arXiv:2305.18486 [78] Md. Tahmid Rahman Laskar、Enamul Hoque 和 Jimmy X. Huang。 2020。通过将查询相关性和迁移学习与 Transformer 模型相结合，实现以查询为中心的抽象摘要。

### 段落 228 · Page 32

**EN**

In Advances in Artificial Intelligence - 33rd Canadian Conference on Artificial Intelligence, Canadian AI 2020, Ottawa, ON, Canada, May 13-15, 2020, Proceedings (Lecture Notes in Computer Science, Vol. 12109) , Cyril Goutte and Xiaodan Zhu (Eds.). Springer, 342–348. https://doi.org/10.1007/978-3-030-47358-7_35 [79] Carlos Lassance and Stéphane Clinchant. 2022. Naver Labs Europe (SPLADE) @ TREC NeuCLIR 2022.. In Text Retrieval Conference (TREC). [80] Carlos Lassance, Hervé Déjean, Thibault Formal, and Stéphane Clinchant. 2024. SPLADE-v3: New baselines for SPLADE. arXiv abs/2403.06789 (2024). [81] Myeonghwa Lee, Seonho An, and Min-Soo Kim.

**中文**

人工智能进展 - 第 33 届加拿大人工智能会议，加拿大 AI 2020，加拿大安大略省渥太华，2020 年 5 月 13-15 日，论文集（计算机科学讲义，第 12109 卷），Cyril Goutte 和 Xudan Zhu（编辑）。施普林格，342-348。 https://doi.org/10.1007/978-3-030-47358-7_35 [79] 卡洛斯·拉桑斯和斯特凡·克林尚。 2022. Naver Labs Europe (SPLADE) @ TREC NeuCLIR 2022.. 在文本检索会议 (TREC) 中。 [80] 卡洛斯·拉桑斯、埃尔韦·德让、蒂博·福尔莫尔和斯特凡·克林尚。 2024. SPLADE-v3：SPLADE 的新基线。 arXiv abs/2403.06789 (2024)。 [81] 李明华、安善浩、金敏秀。

### 段落 229 · Page 32

**EN**

2024. PlanRAG: A Plan-then-Retrieval Augmented Generation for Generative Large Language Models as Decision Makers. InProceedings of the Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers) . Association for Computational Linguistics. [82] Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Veselin Stoyanov, and Luke Zettlemoyer. 2020. BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension.

**中文**

2024. PlanRAG：用于生成大型语言模型作为决策者的计划然后检索增强生成。计算语言学协会北美分会会议论文集：人类语言技术（第一卷：长论文）。计算语言学协会。 [82] Mike Lewis、Yinhan Liu、Naman Goyal、Marjan Ghazvininejad、Abdelrahman Mohamed、Omer Levy、Veselin Stoyanov 和 Luke Zettlemoyer。 2020.BART：用于自然语言生成、翻译和理解的去噪序列到序列预训练。

### 段落 230 · Page 32

**EN**

In Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics. Association for Computational Linguistics, 7871–7880. [83] Patrick S. H. Lewis, Ethan Perez, Aleksandra Piktus, Fabio Petroni, Vladimir Karpukhin, Naman Goyal, Heinrich Küttler, Mike Lewis, Wen-tau Yih, Tim Rocktäschel, Sebastian Riedel, and Douwe Kiela. 2020. Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks.. In Conference on Neural Information Processing Systems (NeurIPS) . [84] Canjia Li, Andrew Yates, Sean MacAvaney, Ben He, and Yingfei Sun. 2024. PARADE: Passage Representation Aggregation forDocument Reranking.

**中文**

计算语言学协会第 58 届年会记录。计算语言学协会，7871–7880。 [83] Patrick S. H. Lewis、Ethan Perez、Aleksandra Piktus、Fabio Petroni、Vladimir Karpukhin、Naman Goyal、Heinrich Küttler、Mike Lewis、Wen-tau Yih、Tim Rocktäschel、Sebastian Riedel 和 Douwe Kiela。 2020.知识密集型 NLP 任务的检索增强生成。神经信息处理系统会议 (NeurIPS)。 [84] 李灿嘉，安德鲁·耶茨，肖恩·麦克卡瓦尼，何本，孙英飞。 2024. PARADE：用于文档重新排序的段落表示聚合。

### 段落 231 · Page 32

**EN**

ACM Transactions on Information Systems 42, 2 (2024), 1–26. [85] Huayang Li, Yixuan Su, Deng Cai, Yan Wang, and Lemao Liu. 2022. A Survey on Retrieval-Augmented Text Generation. arXiv abs/2202.01110 (2022). [86] Xingxuan Li, Ruochen Zhao, Yew Ken Chia, Bosheng Ding, Shafiq R. Joty, Soujanya Poria, and Lidong Bing. 2024. Chain-of-Knowledge: Grounding Large Language Models via Dynamic Knowledge Adapting over Heterogeneous Sources. In The Twelfth International Conference on Learning Representations . [87] Chin-Yew Lin. 2004. ROUGE: A Package for Automatic Evaluation of Summaries. In Text Summarization Branches Out.

**中文**

ACM 信息系统汇刊 42, 2 (2024), 1–26。 [85] 李华阳，苏逸轩，蔡邓，王岩，刘乐茂。 2022.检索增强文本生成调查。 arXiv abs/2202.01110 (2022)。 [86] 李星轩，赵若辰，Yew Ken Chia，丁博胜，Shafiq R. Joty，Soujanya Poria，和 Lidong Bing。 2024.知识链：通过异构源的动态知识适应奠定大型语言模型的基础。在第十二届国际学习表征会议上。 [87]林钦友。 2004. ROUGE：自动评估摘要的包。在文本摘要中分支出来。

### 段落 232 · Page 32

**EN**

Association for Computational Linguistics, Barcelona, Spain, 74–81. https://aclanthology.org/W04-1013 [88] Sheng-Chieh Lin, Akari Asai, Minghan Li, Barlas Oguz, Jimmy Lin, Yashar Mehdad, Wen-tau Yih, and Xilun Chen. 2023. How to Train Your Dragon: Diverse Augmentation Towards Generalizable Dense Retrieval. In Findings of the Association for Computational Linguistics: EMNLP 2023 . Association for Computational Linguistics, 6385–6400. , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

计算语言学协会，西班牙巴塞罗那，74-81。 https://aclanthology.org/W04-1013 [88] Shen-Chieh Lin、Akari Asai、Minghan Li、Barlas Oguz、Jimmy Lin、Yashar Mehdad、Wen-tau Yih 和 Xilun Chen。 2023.如何训练你的龙：对可推广密集检索的多样化增强。计算语言学协会的调查结果：EMNLP 2023。计算语言学协会，6385–6400。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 33

### 段落 233 · Page 33

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 33 [89] Xi Victoria Lin, Xilun Chen, Mingda Chen, Weijia Shi, Maria Lomeli, Richard James, Pedro Rodriguez, Jacob Kahn, Gergely Szilvasy, Mike Lewis, Luke Zettlemoyer, and Wen-tau Yih. 2024. RA-DIT: Retrieval-Augmented Dual Instruction Tuning. In The Twelfth International Conference on Learning Representations , Vol. abs/2310.01352.

**中文**

大型语言模型中检索增强文本生成的调查 33 [89] Xi Victoria Lin、Xilun Chen、Mingda Chen、Weijia Shi、Maria Lomeli、Richard James、Pedro Rodriguez、Jacob Kahn、Gergely Szilvasy、Mike Lewis、Luke Zettlemoyer 和 Wen-tau Yih。 2024.RA-DIT：检索增强双指令调优。在第十二届学习表征国际会议，卷。绝对/2310.01352。

### 段落 234 · Page 33

**EN**

[90] Xi Victoria Lin, Todor Mihaylov, Mikel Artetxe, Tianlu Wang, Shuohui Chen, Daniel Simig, Myle Ott, Naman Goyal, Shruti Bhosale, Jingfei Du, Ramakanth Pasunuru, Sam Shleifer, Punit Singh Koura, Vishrav Chaudhary, Brian O’Horo, Jeff Wang, Luke Zettlemoyer, Zornitsa Kozareva, Mona Diab, Veselin Stoyanov, and Xian Li. 2022. Few-shot Learning with Multilingual Generative Language Models. In Proceedings of the Conference on Empirical Methods in Natural Language Processing. Association for Computational Linguistics. [91] Yi Liu, Lianzhe Huang, Shicheng Li, Sishuo Chen, Hao Zhou, Fandong Meng, Jie Zhou, and Xu Sun. 2023.

**中文**

[90] Xi Victoria Lin、Todor Mihaylov、Mikel Artetxe、Tianlu Wang、Shuohui Chen、Daniel Simig、Myle Ott、Naman Goyal、Shruti Bhosale、Jingfei Du、Ramakanth Pasunuru、Sam Shleifer、Punit Singh Koura、Vishrav Chaudhary、Brian O’Horo、Jeff Wang、Luke Zettlemoyer、Zornitsa Kozareva、Mona迪亚布、维塞林·斯托亚诺夫和李贤。 2022. 使用多语言生成语言模型进行小样本学习。自然语言处理经验方法会议论文集。计算语言学协会。 [91] 刘毅，黄连哲，李世成，陈斯硕，周浩，孟凡东，周杰，孙旭。 2023 年。

### 段落 235 · Page 33

**EN**

RECALL: A Benchmark for LLMs Robustness against External Counterfactual Knowledge. arXiv abs/2311.08147 (2023). [92] Ziyang Luo, Can Xu, Pu Zhao, Xiubo Geng, Chongyang Tao, Jing Ma, Qingwei Lin, and Daxin Jiang. 2023. Augmented Large Language Models with Parametric Knowledge Guiding. arXiv abs/2305.04757 (2023). [93] Hengzhao Ma, Jianzhong Li, and Yong Zhang. 2024. Reconsidering Tree based Methods for k-Maximum Inner-Product Search: The LRUS-CoverTree. In 2024 IEEE 40th International Conference on Data Engineering (ICDE) . IEEE. [94] Xinbei Ma, Yeyun Gong, Pengcheng He, Hai Zhao, and Nan Duan. 2023.

**中文**

回忆：法学硕士针对外部反事实知识的稳健性基准。 arXiv abs/2311.08147 (2023)。 [92] 罗紫阳，徐灿，赵璞，耿秀波，陶重阳，马敬，林庆伟，蒋大新。 2023.具有参数化知识指导的增强型大型语言模型。 arXiv abs/2305.04757 (2023)。 [93]马恒兆，李建中，张勇。 2024.重新考虑基于树的 k 最大内积搜索方法：LRUS-CoverTree。 2024年IEEE第40届国际数据工程会议（ICDE）。 IEEE。 [94]马新贝，宫业云，何鹏程，赵海，段南。 2023 年。

### 段落 236 · Page 33

**EN**

Query Rewriting in Retrieval-Augmented Large Language Models. In Proceedings of the Conference on Empirical Methods in Natural Language Processing . Association for Computational Linguistics, 5303–5315. [95] Xueguang Ma, Liang Wang, Nan Yang, Furu Wei, and Jimmy Lin. 2024. Fine-Tuning LLaMA for Multi-Stage Text Retrieval. In Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, Vol. 1. ACM, 2421–2425. [96] Xueguang Ma, Liang Wang, Nan Yang, Furu Wei, and Jimmy Lin. 2024. Fine-Tuning LLaMA for Multi-Stage Text Retrieval.

**中文**

检索增强大型语言模型中的查询重写。自然语言处理经验方法会议论文集。计算语言学协会，5303–5315。 [95]马雪光，王亮，杨南，魏福如，林吉米。 2024. 微调 LLaMA 以实现多阶段文本检索。第 47 届国际 ACM SIGIR 信息检索研究与发展会议论文集，卷。 1.ACM，2421-2425。 [96]马雪光，王亮，杨南，魏福如，林吉米。 2024. 微调 LLaMA 以实现多阶段文本检索。

### 段落 237 · Page 33

**EN**

In Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2024, Washington DC, USA, July 14-18, 2024 , Grace Hui Yang, Hongning Wang, Sam Han, Claudia Hauff, Guido Zuccon, and Yi Zhang (Eds.). ACM, 2421–2425. https://doi.org/10.1145/3626772.3657951 [97] Yu A. Malkov and D. A. Yashunin. 2020. Efficient and Robust Approximate Nearest Neighbor Search Using Hierarchical Navigable Small World Graphs. IEEE Transactions on Pattern Analysis and Machine Intelligence 42, 4 (2020), 824–836. https://doi.org/10.1109/TPAMI.2018.2889473 [98] Christopher D.

**中文**

第 47 届国际 ACM SIGIR 信息检索研究与开发会议记录，SIGIR 2024，美国华盛顿特区，2024 年 7 月 14-18 日，Grace Hui Yang、Hongning Wang、Sam Han、Claudia Hauff、Guido Zuccon 和 Yi Zhu（编辑）。 ACM，2421–2425。 https://doi.org/10.1145/3626772.3657951 [97] Yu A. Malkov 和 D. A. Yashunin。 2020。使用分层可导航小世界图进行高效且鲁棒的近似最近邻搜索。 IEEE 模式分析和机器智能汇刊 42, 4 (2020), 824–836。 https://doi.org/10.1109/TPAMI.2018.2889473 [98] 克里斯托弗·D.

### 段落 238 · Page 33

**EN**

Manning, Prabhakar Raghavan, and Hinrich Schütze. 2008. Introduction to information retrieval . Cambridge University Press. https://doi.org/10.1017/CBO9780511809071 [99] Niklas Muennighoff. 2022. SGPT: GPT Sentence Embeddings for Semantic Search. arXiv abs/2202.08904 (2022). [100] Reiichiro Nakano, Jacob Hilton, Suchir Balaji, Jeff Wu, Long Ouyang, Christina Kim, Christopher Hesse, Shantanu Jain, Vineet Kosaraju, William Saunders, Xu Jiang, Karl Cobbe, Tyna Eloundou, Gretchen Krueger, Kevin Button, Matthew Knight, Benjamin Chess, and John Schulman. 2021. WebGPT: Browser-assisted question-answering with human feedback.

**中文**

曼宁、普拉巴卡尔·拉加万和辛里奇·许茨。 2008.信息检索简介。剑桥大学出版社。 https://doi.org/10.1017/CBO9780511809071 [99] Niklas Muennighoff。 2022.SGPT：用于语义搜索的 GPT 句子嵌入。 arXiv abs/2202.08904 (2022)。 [100] Reiichiro Nakano、Jacob Hilton、Sucher Balaji、Jeff Wu、Long Ouyang、Christina Kim、Christopher Hesse、Shantanu Jain、Vineet Kosaraju、William Saunders、徐江、Karl Cobbe、Tyna Eloundou、Gretchen Krueger、Kevin Button、Matthew Knight、Benjamin Chess 和 John Schulman。 2021.WebGPT：浏览器辅助问答与人工反馈。

### 段落 239 · Page 33

**EN**

arXiv abs/2112.09332 (2021). [101] Jianmo Ni, Chen Qu, Jing Lu, Zhuyun Dai, Gustavo Hernandez Abrego, Ji Ma, Vincent Zhao, Yi Luan, Keith Hall, Ming- Wei Chang, and Yinfei Yang. 2022. Large Dual Encoders Are Generalizable Retrievers. InProceedings of the Conference on Empirical Methods in Natural Language Processing . Association for Computational Linguistics, 9844–9855. [102] Rodrigo Nogueira, Zhiying Jiang, Ronak Pradeep, and Jimmy Lin. 2020. Document Ranking with a Pretrained Sequence-to-Sequence Model. In Findings of the Association for Computational Linguistics: EMNLP 2020 . Association for Computational Linguistics.

**中文**

arXiv abs/2112.09332 (2021)。 [101] 倪建模，曲陈，卢静，戴竹云，古斯塔沃·埃尔南德斯·阿布雷戈，马吉，赵文森，栾毅，Keith Hall，张明伟，杨银飞。 2022.大型双编码器是可通用的检索器。自然语言处理经验方法会议论文集。计算语言学协会，9844–9855。 [102] 罗德里戈·诺盖拉、蒋志英、罗纳克·普拉迪普和吉米·林。 2020。使用预训练的序列到序列模型进行文档排序。计算语言学协会的调查结果：EMNLP 2020。计算语言学协会。

### 段落 240 · Page 33

**EN**

[103] Rodrigo Nogueira, Wei Yang, Kyunghyun Cho, and Jimmy Lin. 2019. Multi-stage document ranking with BERT.CoRR abs/1910.14424 (2019). [104] Long Ouyang, Jeffrey Wu, Xu Jiang, Diogo Almeida, Carroll L. Wainwright, Pamela Mishkin, Chong Zhang, Sandhini Agarwal, Katarina Slama, Alex Ray, John Schulman, Jacob Hilton, Fraser Kelton, Luke Miller, Maddie Simens, Amanda Askell, Peter Welinder, Paul F. Christiano, Jan Leike, and Ryan Lowe. 2022. Training language models to follow instructions with human feedback. In Conference on Neural Information Processing Systems (NeurIPS) . [105] Ankit Pal, Logesh Kumar Umapathi, and Malaikannan Sankarasubbu.

**中文**

[103] 罗德里戈·诺盖拉，杨伟，Kyunghyun Cho，和吉米·林。 2019。使用 BERT.CoRR abs/1910.14424 (2019) 进行多阶段文档排名。 [104] Long Ouyang、Jeffrey Wu、徐江、Diogo Almeida、Carroll L. Wainwright、Pamela Mishkin、Chong Chang、Sandhini Agarwal、Katarina Slama、Alex Ray、John Schulman、Jacob Hilton、Fraser Kelton、Luke Miller、Maddie Simens、Amanda Askel、Peter Welinder、Paul F. Christiano、Jan Leike 和 Ryan Lowe。 2022. 训练语言模型以遵循人类反馈的指令。在神经信息处理系统会议 (NeurIPS) 中。 [105] Ankit Pal、Logesh Kumar Umapathi 和 Malaikannan Sankarasubbu。

### 段落 241 · Page 33

**EN**

2022. MedMCQA: A Large-scale Multi-Subject Multi-Choice Dataset for Medical domain Question Answering.. In Conference on Health, Inference, and Learning (CHIL). 248–260. [106] Yu Pan, Jianxin Sun, and Hongfeng Yu. 2023. LM-DiskANN: Low Memory Footprint in Disk-Native Dynamic Graph-Based ANN Indexing. In 2023 IEEE International Conference on Big Data (BigData) . IEEE. [107] Kishore Papineni, Salim Roukos, Todd Ward, and Wei-Jing Zhu. 2002. BLEU: a method for automatic evaluation of machine translation. In Proceedings of the 40th Annual Meeting on Association for Computational Linguistics (Philadelphia, Pennsylvania) (ACL ’02).

**中文**

2022. MedMCQA：用于医学领域问答的大规模多主题多选择数据集。在健康、推理和学习会议 (CHIL) 中。 248–260。 [106] 潘宇，孙建新，于洪峰。 2023. LM-DiskANN：磁盘原生动态基于图的 ANN 索引中的低内存占用。 2023年IEEE国际大数据会议（BigData）。 IEEE。 [107] Kishore Papineni、Salim Roukos、Todd Ward 和 Wei-Jing Zhu。 2002. BLEU：一种机器翻译自动评估方法。计算语言学协会第 40 届年会（宾夕法尼亚州费城）(ACL ’02) 论文集。

### 段落 242 · Page 33

**EN**

Association for Computational Linguistics, USA, 311–318. https://doi.org/10. 3115/1073083.1073135 [108] Guilherme Penedo, Quentin Malartic, Daniel Hesslow, Ruxandra Cojocaru, Hamza Alobeidli, Alessandro Cappelli, Baptiste Pannier, Ebtesam Almazrouei, and Julien Launay. 2023. The RefinedWeb Dataset for Falcon LLM: Outperforming , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

美国计算语言学协会，311-318。 https://doi.org/10。 3115/1073083.1073135 [108] Guilherme Penedo、Quentin Malartic、Daniel Hesslow、Ruxandra Cojocaru、Hamza Alobeidli、Alessandro Cappelli、Baptiste Pannier、Ebtesam Almazrouei 和 Julien Launay。 2023. Falcon LLM 的 RefinedWeb 数据集：表现出色，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 34

### 段落 243 · Page 34

**EN**

34 Huang et al. Curated Corpora with Web Data Only.. In Conference on Neural Information Processing Systems (NeurIPS) . [109] Fabio Petroni, Aleksandra Piktus, Angela Fan, Patrick Lewis, Majid Yazdani, Nicola De Cao, James Thorne, Yacine Jernite, Vladimir Karpukhin, Jean Maillard, Vassilis Plachouras, Tim Rocktäschel, and Sebastian Riedel. 2021. KILT: a Benchmark for Knowledge Intensive Language Tasks. In Proceedings of the Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies . Association for Computational Linguistics, 2523–2544. [110] Filip Radlinski and Nick Craswell. 2010.

**中文**

34 黄等人。仅包含 Web 数据的精选语料库。在神经信息处理系统 (NeurIPS) 会议上。 [109] Fabio Petroni、Aleksandra Piktus、Angela Fan、Patrick Lewis、Majid Yazdani、Nicola De Cao、James Thorne、Yacine Jernite、Vladimir Karpukhin、Jean Maillard、Vassilis Plachouras、Tim Rocktäschel 和 Sebastian Riedel。 2021.KILT：知识密集型语言任务的基准。计算语言学协会北美分会会议记录：人类语言技术。计算语言学协会，2523-2544。 [110] 菲利普·拉德林斯基和尼克·克拉斯韦尔。 2010年。

### 段落 244 · Page 34

**EN**

Comparing the sensitivity of information retrieval metrics.. In Annual International ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR) . 667–674. [111] Colin Raffel, Noam M. Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, and Peter J. Liu. 2020. Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer. Journal of Machine Learning Research (JMLR) 21 (2020), 140:1–140:67. [112] Ori Ram, Yoav Levine, Itay Dalmedigos, Dor Muhlgay, Amnon Shashua, Kevin Leyton-Brown, and Yoav Shoham. 2023. In-Context Retrieval-Augmented Language Models.

**中文**

比较信息检索指标的敏感性。在年度国际 ACM SIGIR 信息检索研究与发展会议 (SIGIR) 中。 667–674。 [111] Colin Raffel、Noam M. Shazeer、Adam Roberts、Katherine Lee、Sharan Narang、Michael Matena、Yanqi Zhou、Wei Li 和 Peter J. Liu。 2020。使用统一的文本到文本转换器探索迁移学习的局限性。机器学习研究杂志 (JMLR) 21 (2020), 140:1–140:67。 [112] Ori Ram、Yoav Levine、Itay Dalmedigos、Dor Muhlgay、Amnon Shashua、Kevin Leyton-Brown 和 Yoav Shoham。 2023.上下文检索增强语言模型。

### 段落 245 · Page 34

**EN**

Transactions of the Association for Computational Linguistics 11 (2023), 1316–1331. [113] Ori Ram, Gal Shachaf, Omer Levy, Jonathan Berant, and Amir Globerson. 2022. Learning to Retrieve Passages without Supervision. In Proceedings of the Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies. Association for Computational Linguistics. [114] David Rau, Hervé Déjean, Nadezhda Chirkova, Thibault Formal, Shuai Wang, Vassilina Nikoulina, and Stéphane Clinchant. 2024. BERGEN: A Benchmarking Library for Retrieval-Augmented Generation. arXiv abs/2407.01102 (2024).

**中文**

计算语言学协会汇刊 11 (2023), 1316–1331。 [113] 奥里·拉姆、加尔·沙查夫、奥马尔·利维、乔纳森·贝兰特和阿米尔·格洛伯森。 2022. 学习在没有监督的情况下检索段落。计算语言学协会北美分会会议记录：人类语言技术。计算语言学协会。 [114] David Rau、Hervé Déjean、Nadezhda Chirkova、Thibault Formal、Shuai Wang、Vassilina Nikoulina 和 Stéphane Clinchant。 2024. BERGEN：检索增强生成的基准库。 arXiv abs/2407.01102 (2024)。

### 段落 246 · Page 34

**EN**

[115] Nils Reimers and Iryna Gurevych. 2019. Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks. In Proceedings of the Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP) . Association for Computational Linguistics, 3980–3990. [116] Stephen Robertson and Hugo Zaragoza. 2009. The Probabilistic Relevance Framework: BM25 and Beyond.Foundations and Trends® in Information Retrieval 3, 4 (2009), 333–389. [117] Jon Saad-Falcon, O. Khattab, Christopher Potts, and Matei Zaharia. 2023.

**中文**

[115] 尼尔斯·赖默斯和伊琳娜·古列维奇。 2019.Sentence-BERT：使用 Siamese BERT 网络的句子嵌入。自然语言处理经验方法会议和第九届国际自然语言处理联合会议（EMNLP-IJCNLP）的会议记录。计算语言学协会，3980-3990。 [116] 斯蒂芬·罗伯逊和雨果·萨拉戈萨。 2009. 概率相关性框架：BM25 及以后。信息检索的基础和趋势® 3, 4 (2009), 333–389。 [117] Jon Saad-Falcon、O. Khattab、Christopher Potts 和 Matei Zaharia。 2023 年。

### 段落 247 · Page 34

**EN**

ARES: An Automated Evaluation Framework for Retrieval-Augmented Generation Systems. In North American Chapter of the Association for Computational Linguistics, Vol. abs/2311.09476. [118] Alireza Salemi, Surya Kallumadi, and Hamed Zamani. 2024. Optimization Methods for Personalizing Large Language Models through Retrieval Augmentation. In Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval . ACM, 752–762. [119] Alireza Salemi and Hamed Zamani. 2024. Evaluating Retrieval Quality in Retrieval-Augmented Generation.

**中文**

ARES：检索增强生成系统的自动评估框架。在计算语言学协会北美分会，卷。绝对/2311.09476。 [118] Alireza Salemi、Surya Kallumadi 和 Hamed Zamani。 2024。通过检索增强个性化大型语言模型的优化方法。第 47 届国际 ACM SIGIR 信息检索研究与开发会议论文集。 ACM，752–762。 [119]阿里雷扎·萨莱米和哈米德·扎马尼。 2024.评估检索增强生成中的检索质量。

### 段落 248 · Page 34

**EN**

In Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval , Vol. 21. ACM, 2395–2400. [120] Sara Sarto, Marcella Cornia, Lorenzo Baraldi, and Rita Cucchiara. 2022. Retrieval-Augmented Transformer for Image Captioning. In International Conference on Content-based Multimedia Indexing . ACM. [121] Zhihong Shao, Yeyun Gong, Yelong Shen, Minlie Huang, Nan Duan, and Weizhu Chen. 2023. Enhancing Retrieval- Augmented Large Language Models with Iterative Retrieval-Generation Synergy. In Findings of the Association for Computational Linguistics: EMNLP 2023 .

**中文**

第 47 届国际 ACM SIGIR 信息检索研究与发展会议论文集，卷。 21.ACM，2395–2400。 [120] 萨拉·萨托、马塞拉·科尼亚、洛伦佐·巴拉尔迪和丽塔·库奇亚拉。 2022. 用于图像字幕的检索增强Transformer。在基于内容的多媒体索引国际会议上。 ACM。 [121] 邵志红，宫业云，沉业龙，黄敏烈，段南，陈伟珠。 2023.通过迭代检索生成协同作用增强检索增强型大型语言模型。计算语言学协会的调查结果：EMNLP 2023。

### 段落 249 · Page 34

**EN**

Association for Computational Linguistics, 9248–9274. [122] Weijia Shi, Sewon Min, Michihiro Yasunaga, Minjoon Seo, Rich James, M. Lewis, Luke Zettlemoyer, and Wen-tau Yih. 2023. REPLUG: Retrieval-Augmented Black-Box Language Models. In North American Chapter of the Association for Computational Linguistics, Vol. abs/2301.12652. [123] Yunxiao Shi, Xing Zi, Zijing Shi, Haimin Zhang, Qiang Wu, and Min Xu. 2024. ERAGent: Enhancing Retrieval- Augmented Language Models with Improved Accuracy, Efficiency, and Personalization. arXiv abs/2405.06683 (2024). [124] Weihang Su, Yichen Tang, Qingyao Ai, Zhijing Wu, and Yiqun Liu. 2024.

**中文**

计算语言学协会，9248–9274。 [122] Weijia Shi、Sewon Min、Michihiro Yasunaga、Minjoon Seo、Rich James、M. Lewis、Luke Zettlemoyer 和 Wen-tau Yih。 2023.REPLUG：检索增强的黑盒语言模型。在计算语言学协会北美分会，卷。绝对/2301.12652。 [123]史云晓，子星，石子静，张海民，吴强，徐敏。 2024.ERAGent：增强检索增强语言模型，提高准确性、效率和个性化。 arXiv abs/2405.06683 (2024)。 [124] 苏伟航，唐一辰，艾庆耀，吴志静，刘逸群。 2024 年。

### 段落 250 · Page 34

**EN**

DRAGIN: Dynamic Retrieval Augmented Generation based on the Real-time Information Needs of Large Language Models. arXiv abs/2403.10081 (2024). [125] Zhiqing Sun, Xuezhi Wang, Yi Tay, Yiming Yang, and Denny Zhou. 2023. Recitation-Augmented Language Models. In International Conference on Learning Representations (ICLR) . [126] Kento Tatsuno, Daisuke Miyashita, Taiga Ikeda, Kiyoshi Ishiyama, Kazunari Sumiyoshi, and Jun Deguchi. 2024. AiSAQ: All-in-Storage ANNS with Product Quantization for DRAM-free Information Retrieval. arXiv abs/2404.06004 (2024). [127] Yi Tay, Mostafa Dehghani, Vinh Q.

**中文**

DRAGIN：基于大型语言模型实时信息需求的动态检索增强生成。 arXiv abs/2403.10081 (2024)。 [125] 孙志清，王学智，泰伊，杨一鸣，周丹尼。 2023.背诵增强语言模型。在国际学习表征会议（ICLR）中。 [126]辰野贤人、宫下大辅、池田大河、石山清、住吉一成、出口淳。 2024. AiSAQ：具有产品量化功能的全存储 ANN，用于无 DRAM 信息检索。 arXiv abs/2404.06004 (2024)。 [127] Yi Tay、Mostafa Dehghani、Vinh Q.

### 段落 251 · Page 34

**EN**

Tran, Xavier Garcia, Jason Wei, Xuezhi Wang, Hyung Won Chung, Dara Bahri, Tal Schuster, Huaixiu Steven Zheng, Denny Zhou, Neil Houlsby, and Donald Metzler. 2023. UL2: Unifying Language Learning Paradigms. In International Conference on Learning Representations (ICLR) . [128] Yi Tay, Vinh Tran, Mostafa Dehghani, Jianmo Ni, Dara Bahri, Harsh Mehta, Zhen Qin, Kai Hui, Zhe Zhao, Jai Prakash Gupta, Tal Schuster, William W. Cohen, and Donald Metzler. 2022. Transformer Memory as a Differentiable Search Index. In Conference on Neural Information Processing Systems (NeurIPS) . , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

Tran、Xavier Garcia、Jason Wei、Xuezhi Wang、Hyung Won Chung、Dara Bahri、Tal Schuster、Huaixiu Steven Cheng、Denny Zhou、Neil Houlsby 和 Donald Metzler。 2023.UL2：统一语言学习范式。在国际学习表征会议（ICLR）中。 [128] Yi Tay、Vinh Tran、Mostafa Dehghani、Jianmo Ni、Dara Bahri、Harsh Mehta、Zhen Qing、Kai Hui、Zhe Zhu、Jai Prakash Gupta、Tal Schuster、William W. Cohen 和 Donald Metzler。 2022.Transformer内存作为可微搜索索引。在神经信息处理系统会议 (NeurIPS) 中。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 35

### 段落 252 · Page 35

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 35 [129] James Thorne, Andreas Vlachos, Christos Christodoulopoulos, and Arpit Mittal. 2018. FEVER: a Large-scale Dataset for Fact Extraction and VERification. In Proceedings of the Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers) . Association for Computational Linguistics, 809–819.

**中文**

大型语言模型中检索增强文本生成的调查 35 [129] James Thorne、Andreas Vlachos、Christos Christodoulopoulos 和 Arpit Mittal。 2018。FEVER：用于事实提取和验证的大规模数据集。计算语言学协会北美分会会议记录：人类语言技术，第 1 卷（长论文）。计算语言学协会，809-819。

### 段落 253 · Page 35

**EN**

[130] Hugo Touvron, Louis Martin, Kevin Stone, Peter Albert, Amjad Almahairi, Yasmine Babaei, Nikolay Bashlykov, Soumya Batra, Prajjwal Bhargava, Shruti Bhosale, Dan Bikel, Lukas Blecher, Cristian Canton Ferrer, Moya Chen, Guillem Cucurull, David Esiobu, Jude Fernandes, Jeremy Fu, Wenyin Fu, Brian Fuller, Cynthia Gao, Vedanuj Goswami, Naman Goyal, Anthony Hartshorn, Saghar Hosseini, Rui Hou, Hakan Inan, Marcin Kardas, Viktor Kerkez, Madian Khabsa, Isabel Kloumann, Artem Korenev, Punit Singh Koura, Marie-Anne Lachaux, Thibaut Lavril, Jenya Lee, Diana Liskovich, Yinghai Lu, Yuning Mao, Xavier Martinet, Todor Mihaylov, Pushkar Mishra, Igor Molyb

**中文**

[130] Hugo Touvron、Louis Martin、Kevin Stone、Peter Albert、Amjad Almahairi、Yasmine Babaei、Nikolay Bashlykov、Soumya Batra、Prajjwal Bhargava、Shruti Bhosale、Dan Bikel、Lukas Blecher、Cristian Canton Ferrer、Moya Chen、Guillem Cucurull、David Esiobu、Jude Fernandes、Jeremy Fu、傅文音、布莱恩·富勒、辛西娅·高、维达努吉·戈斯瓦米、纳曼·戈亚尔、安东尼·哈茨霍恩、萨加尔·侯赛尼、侯瑞、哈坎·伊南、马辛·卡达斯、维克多·科克兹、马迪安·哈布萨、伊莎贝尔·克鲁曼、阿特姆·科热涅夫、普尼特·辛格·库拉、玛丽-安妮·拉乔、蒂博·拉夫里尔、珍雅·李、戴安娜Liskovich、陆英海、毛宇宁、Xavier Martinet、Todor Mihaylov、Pushkar Mishra、Igor Molyb

### 段落 254 · Page 35

**EN**

og, Yixin Nie, Andrew Poulton, Jeremy Reizenstein, Rashi Rungta, Kalyan Saladi, Alan Schelten, Ruan Silva, Eric Michael Smith, Ranjan Subramanian, Xiaoqing Ellen Tan, Binh Tang, Ross Taylor, Adina Williams, Jian Xiang Kuan, Puxin Xu, Zheng Yan, Iliyan Zarov, Yuchen Zhang, Angela Fan, Melanie Kambadur, Sharan Narang, Aurelien Rodriguez, Robert Stojnic, Sergey Edunov, and Thomas Scialom.

**中文**

og、聂一心、安德鲁·波尔顿、杰里米·雷森斯坦、拉什·朗塔、卡利安·萨拉迪、艾伦·谢尔顿、阮·席尔瓦、埃里克·迈克尔·史密斯、兰詹·萨勃拉曼尼安、晓晴艾伦·谭、平·唐、罗斯·泰勒、阿迪娜·威廉姆斯、健翔宽、徐普欣、严正、伊利扬·扎罗夫、张雨辰、安吉拉·范、梅兰妮·坎巴杜尔、夏兰·纳朗、Aurelien罗德里格斯、罗伯特·斯托伊尼克、谢尔盖·埃杜诺夫和托马斯·夏洛姆。

### 段落 255 · Page 35

**EN**

2023. Llama 2: Open Foundation and Fine-Tuned Chat Models. arXiv abs/2307.09288 (2023). [131] Harsh Trivedi, Niranjan Balasubramanian, Tushar Khot, and Ashish Sabharwal. 2023. Interleaving Retrieval with Chain-of-Thought Reasoning for Knowledge-Intensive Multi-Step Questions. InProceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) . Association for Computational Linguistics, 10014–10037.

**中文**

2023. Llama 2：开放基础和微调聊天模型。 arXiv abs/2307.09288 (2023)。 [131] Harsh Trivedi、Niranjan Balasubramanian、Tushar Khot 和 Ashish Sabharwal。 2023.知识密集型多步骤问题的交叉检索与思想链推理。计算语言学协会第61届年会论文集（第一卷：长论文）。计算语言学协会，10014–10037。

### 段落 256 · Page 35

**EN**

[132] George Tsatsaronis, Georgios Balikas, Prodromos Malakasiotis, Ioannis Partalas, Matthias Zschunke, Michael R Alvers, Dirk Weissenborn, Anastasia Krithara, Sergios Petridis, Dimitris Polychronopoulos, Yannis Almirantis, John Pavlopoulos, Nicolas Baskiotis, Patrick Gallinari, Thierry Artiéres, Axel-Cyrille Ngonga Ngomo, Norman Heino, Eric Gaussier, Liliana Barrio-Alvers, Michael Schroeder, Ion Androutsopoulos, and Georgios Paliouras. 2015. An overview of the BIOASQ large-scale biomedical semantic indexing and question answering competition. BMC Bioinformatics 16, 1 (2015). [133] Ashish Vaswani, Noam M.

**中文**

[132] George Tsatsaronis、Georgios Balikas、Prodromos Malakasiotis、Ioannis Partalas、Matthias Zschunke、Michael R Alvers、Dirk Weissenborn、Anastasia Krithara、Sergios Petridis、Dimitris Polychronopoulos、Yannis Almirantis、John Pavlopoulos、Nicolas Baskiotis、Patrick Gallinari、Thierry Artiéres，阿克塞尔-西里尔·恩贡加·恩戈莫、诺曼·海诺、埃里克·高西尔、莉莉安娜·巴里奥-阿尔弗斯、迈克尔·施罗德、扬·安德鲁索普洛斯和乔治斯·帕利乌拉斯。 2015. BIOASQ 大规模生物医学语义索引与问答竞赛概述。 BMC 生物信息学 16, 1 (2015)。 [133] 阿什什·瓦斯瓦尼，诺姆·M.

### 段落 257 · Page 35

**EN**

Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Lukasz Kaiser, and Illia Polosukhin. 2017. Attention is All you Need. In Neural Information Processing Systems . 5998–6008. [134] Alex Wang, Yada Pruksachatkun, Nikita Nangia, Amanpreet Singh, Julian Michael, Felix Hill, Omer Levy, and Samuel R. Bowman. 2019. SuperGLUE: A Stickier Benchmark for General-Purpose Language Understanding Systems. In Conference on Neural Information Processing Systems (NeurIPS) . 3261–3275. [135] Haoyu Wang, Tuo Zhao, and Jing Gao. 2024.

**中文**

Shazeer、Niki Parmar、Jakob Uszkoreit、Llion Jones、Aidan N. Gomez、Lukasz Kaiser 和 Illia Polosukhin。 2017 年。您所需要的就是注意力。在神经信息处理系统中。 5998–6008。 [134] Alex Wang、Yada Pruksachatkun、Nikita Nangia、Amanpreet Singh、Julian Michael、Felix Hill、Omer Levy 和 Samuel R. Bowman。 2019。SuperGLUE：通用语言理解系统的更具粘性的基准。在神经信息处理系统会议 (NeurIPS) 中。 3261–3275。 [135]王浩宇，赵拓，高靖。 2024 年。

### 段落 258 · Page 35

**EN**

BlendFilter: Advancing Retrieval-Augmented Large Language Models via Query Generation Blending and Knowledge Filtering. arXiv abs/2402.11129 (2024). [136] Liang Wang, Nan Yang, Xiaolong Huang, Binxing Jiao, Linjun Yang, Daxin Jiang, Rangan Majumder, and Furu Wei. 2022. Text Embeddings by Weakly-Supervised Contrastive Pre-training. arXiv abs/2212.03533 (2022). [137] Liang Wang, Nan Yang, and Furu Wei. 2023. Query2doc: Query Expansion with Large Language Models. InProceedings of the Conference on Empirical Methods in Natural Language Processing . Association for Computational Linguistics, 9414–9423.

**中文**

BlendFilter：通过查询生成混合和知识过滤推进检索增强大型语言模型。 arXiv abs/2402.11129 (2024)。 [136] 王亮，杨南，黄小龙，焦滨兴，杨林军，姜大新，Rangan Majumder，魏福如。 2022.弱监督对比预训练的文本嵌入。 arXiv abs/2212.03533 (2022)。 [137] 王亮，杨南，魏福如。 2023.Query2doc：使用大型语言模型进行查询扩展。自然语言处理经验方法会议论文集。计算语言学协会，9414–9423。

### 段落 259 · Page 35

**EN**

[138] Qifan Wang, Yi Fang, Anirudh Ravula, Fuli Feng, Xiaojun Quan, and Dongfang Liu. 2022. WebFormer: The Web-page Transformer for Structure Information Extraction. In Proceedings of the ACM Web Conference 2022 . ACM. [139] Xiaohua Wang, Zhenghua Wang, Xuan Gao, Feiran Zhang, Yixin Wu, Zhibo Xu, Tianyuan Shi, Zhengyuan Wang, Shizheng Li, Qi Qian, Ruicheng Yin, Changze Lv, Xiaoqing Zheng, and Xuanjing Huang. 2024. Searching for Best Practices in Retrieval-Augmented Generation. arXiv abs/2407.01219 (2024). [140] Xintao Wang, Qianwen Yang, Yongting Qiu, Jiaqing Liang, Qianyu He, Zhouhong Gu, Yanghua Xiao, and Wei Wang. 2023.

**中文**

[138] 王起帆，方毅，Anirudh Ravula，冯富丽，全晓军，刘东方。 2022.WebFormer：用于结构信息提取的网页转换器。 2022 年 ACM 网络会议论文集。 ACM。 [139] 王晓华、王正华、高轩、张斐然、吴一欣、徐志波、施天元、王正元、李世政、钱琪、殷瑞成、吕长泽、郑小青、黄选景。 2024。寻找检索增强生成的最佳实践。 arXiv abs/2407.01219 (2024)。 [140]王新涛，杨干文，邱永廷，梁嘉庆，何千宇，谷周红，肖阳华，王伟。 2023 年。

### 段落 260 · Page 35

**EN**

KnowledGPT: Enhancing Large Language Models with Retrieval and Storage Access on Knowledge Bases. arXiv abs/2308.11761 (2023). [141] Zhiruo Wang, Jun Araki, Zhengbao Jiang, Md. Rizwan Parvez, and Graham Neubig. 2023. Learning to Filter Context for Retrieval-Augmented Generation. arXiv abs/2311.08377 (2023). [142] BigScience Workshop, :, Teven Le Scao, Angela Fan, Christopher Akiki, and etc. 2022. BLOOM: A 176B-Parameter Open-Access Multilingual Language Model. arXiv abs/2211.05100 (2022). [143] Shitao Xiao, Zheng Liu, Yingxia Shao, and Zhao Cao. 2022. RetroMAE: Pre-Training Retrieval-oriented Language Models Via Masked Auto-Encoder..

**中文**

KnowledGPT：通过知识库的检索和存储访问增强大型语言模型。 arXiv abs/2308.11761 (2023)。 [141] 王志若、荒木俊、江正宝、Rizwan Parvez 博士和 Graham Neubig。 2023.学习过滤上下文以进行检索增强生成。 arXiv abs/2311.08377 (2023)。 [142] BigScience Workshop，：，Teven Le Scao，Angela Fan，Christopher Akiki 等，2022。BLOOM：176B 参数开放访问多语言语言模型。 arXiv abs/2211.05100 (2022)。 [143] 肖世涛，刘峥，邵迎霞，赵操。 2022.RetroMAE：通过屏蔽自动编码器预训练面向检索的语言模型..

### 段落 261 · Page 35

**EN**

In Conference on Empirical Methods in Natural Language Processing (EMNLP) . 538–548. [144] Guangzhi Xiong, Qiao Jin, Zhiyong Lu, and Aidong Zhang. 2024. Benchmarking Retrieval-Augmented Generation for Medicine. arXiv abs/2402.13178 (2024). [145] Jie Xiong, Li Yu, Xi Niu, and Youfang Leng. 2023. XRR: Extreme multi-label text classification with candidate retrieving and deep ranking. Information Sciences 622 (2023), 115–132. , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

在自然语言处理经验方法会议（EMNLP）中。 538–548。 [144] 熊光志，金巧，陆志勇，张爱东。 2024. 医学基准检索增强生成。 arXiv abs/2402.13178 (2024)。 [145] 熊杰，李宇，西牛，冷有方。 2023. XRR：具有候选检索和深度排名的极端多标签文本分类。信息科学 622 (2023), 115–132。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 36

### 段落 262 · Page 36

**EN**

36 Huang et al. [146] Lee Xiong, Chenyan Xiong, Ye Li, Kwok-Fung Tang, Jialin Liu, Paul N. Bennett, Junaid Ahmed, and Arnold Overwijk. 2021. Approximate Nearest Neighbor Negative Contrastive Learning for Dense Text Retrieval. In International Conference on Learning Representations (ICLR) . [147] Fangyuan Xu, Weijia Shi, and Eunsol Choi. 2024. RECOMP: Improving Retrieval-Augmented LMs with Context Compression and Selective Augmentation. In The Twelfth International Conference on Learning Representations , Vol. abs/2310.04408. [148] Shicheng Xu, Liang Pang, Jun Xu, Huawei Shen, and Xueqi Cheng. 2024.

**中文**

36 黄等人。 [146] Lee Xiong、Chenyan Xiong、Ye Li、Kwok-Fung Tang、Jialin Liu、Paul N. Bennett、Junaid Ahmed 和 Arnold Overwijk。 2021.密集文本检索的近似最近邻负对比学习。在国际学习表征会议（ICLR）中。 [147] 徐方圆，施维佳，崔恩索尔。 2024.RECOMP：通过上下文压缩和选择性增强改进检索增强型语言模型。在第十二届学习表征国际会议，卷。绝对/2310.04408。 [148] 徐世成，庞亮，徐军，沉华伟，程学奇。 2024 年。

### 段落 263 · Page 36

**EN**

List-aware Reranking-Truncation Joint Model for Search and Retrieval-augmented Generation. In Proceedings of the ACM on Web Conference 2024 , Vol. 21. ACM, 1330–1340. [149] Shi-Qi Yan, Jia-Chen Gu, Yun Zhu, and Zhen-Hua Ling. 2024. Corrective Retrieval Augmented Generation. arXiv abs/2401.15884 (2024). [150] Diji Yang, Jinmeng Rao, Kezhen Chen, Xiaoyuan Guo, Yawen Zhang, Jie Yang, and Yi Zhang. 2024. IM-RAG: Multi- Round Retrieval-Augmented Generation Through Learning Inner Monologues. InProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval , Vol. 33. ACM, 730–740.

**中文**

用于搜索和检索增强生成的列表感知重排序-截断联合模型。 2024 年 ACM 网络会议论文集，卷。 21.ACM，1330–1340。 [149] 严世奇，顾嘉晨，朱云，凌振华。 2024.纠正检索增强生成。 arXiv abs/2401.15884 (2024)。 [150] 杨迪吉，饶金猛，陈克振，郭晓媛，张亚文，杨杰，张毅。 2024.IM-RAG：通过学习内心独白进行多轮检索增强生成。第 47 届国际 ACM SIGIR 信息检索研究与发展会议论文集，卷。 33.ACM，730-740。

### 段落 264 · Page 36

**EN**

[151] Haoyan Yang, Zhitao Li, Yong Zhang, Jianzong Wang, Ning Cheng, Ming Li, and Jing Xiao. 2023. PRCA: Fitting Black-Box Large Language Models for Retrieval Question Answering via Pluggable Reward-Driven Contextual Adapter. In Proceedings of the Conference on Empirical Methods in Natural Language Processing . Association for Computational Linguistics, 5364–5375. [152] Zhuolin Yang, Wei Ping, Zihan Liu, Vijay Korthikanti, Weili Nie, De-An Huang, Linxi Fan, Zhiding Yu, Shiyi Lan, Bo Li, Mohammad Shoeybi, Ming-Yu Liu, Yuke Zhu, Bryan Catanzaro, Chaowei Xiao, and Anima Anandkumar. 2023.

**中文**

[151] 杨浩彦，李志涛，张勇，王建宗，程宁，李明，肖静。 2023. PRCA：通过可插入奖励驱动的上下文适配器拟合黑盒大型语言模型以进行检索问答。自然语言处理经验方法会议论文集。计算语言学协会，5364–5375。 [152] 杨卓林、平伟、刘子涵、Vijay Korthikanti、聂伟力、黄德安、范林西、余志鼎、兰世一、李波、Mohammad Shoeybi、刘明宇、朱宇科、Bryan Catanzaro、肖超伟和 Anima Anandkumar。 2023 年。

### 段落 265 · Page 36

**EN**

Re-ViLM: Retrieval-Augmented Visual Language Model for Zero and Few-Shot Image Captioning. In Findings of the Association for Computational Linguistics: EMNLP 2023 . Association for Computational Linguistics, 11844–11857. [153] Zhilin Yang, Peng Qi, Saizheng Zhang, Yoshua Bengio, William Cohen, Ruslan Salakhutdinov, and Christopher D. Manning. 2018. HotpotQA: A Dataset for Diverse, Explainable Multi-hop Question Answering. In Proceedings of the Conference on Empirical Methods in Natural Language Processing . Association for Computational Linguistics, 2369–2380. [154] Hao Yu, Aoran Gan, Kai Zhang, Shiwei Tong, Qi Liu, and Zhaofeng Liu. 2024.

**中文**

Re-ViLM：用于零镜头和少镜头图像字幕的检索增强视觉语言模型。计算语言学协会的调查结果：EMNLP 2023。计算语言学协会，11844–11857。 [153] 杨志林、齐鹏、张赛正、Yoshua Bengio、William Cohen、Ruslan Salakhutdinov 和 Christopher D. Manning。 2018.HotpotQA：多样化、可解释的多跳问答数据集。自然语言处理经验方法会议论文集。计算语言学协会，2369–2380。 [154] 于浩，甘傲然，张凯，童世伟，刘奇，刘兆峰。 2024 年。

### 段落 266 · Page 36

**EN**

Evaluation of Retrieval-Augmented Generation: A Survey. arXiv abs/2405.07437 (2024). [155] Shi Yu, Jiahua Liu, Jingqin Yang, Chenyan Xiong, Paul N. Bennett, Jianfeng Gao, and Zhiyuan Liu. 2020. Few- Shot Generative Conversational Query Rewriting. In Proceedings of the 43rd International ACM SIGIR conference on research and development in Information Retrieval, SIGIR 2020, Virtual Event, China, July 25-30, 2020 , Jimmy X. Huang, Yi Chang, Xueqi Cheng, Jaap Kamps, Vanessa Murdock, Ji-Rong Wen, and Yiqun Liu (Eds.). ACM, 1933–1936.

**中文**

检索增强生成的评估：一项调查。 arXiv abs/2405.07437 (2024)。 [155]石宇，刘家华，杨敬勤，熊晨燕，Paul N. Bennett，高剑峰，刘志远。 2020.Few-Shot 生成会话查询重写。第 43 届国际 ACM SIGIR 信息检索研究与开发会议记录，SIGIR 2020，虚拟活动，中国，2020 年 7 月 25-30 日，Jimmy X. Huang、Yi Chang、Xueqi Cheng、Jaap Kamps、Vanessa Murdock、Ji-Rong Wen 和 Yiqun Liu（编辑）。 ACM，1933-1936。

### 段落 267 · Page 36

**EN**

https://doi.org/10.1145/3397271.3401323 [156] Wenhao Yu, Dan Iter, Shuohang Wang, Yichong Xu, Mingxuan Ju, Soumya Sanyal, Chenguang Zhu, Michael Zeng, and Meng Jiang. 2023. Generate rather than Retrieve: Large Language Models are Strong Context Generators. In International Conference on Learning Representations (ICLR) . [157] Zichun Yu, Chenyan Xiong, Shi Yu, and Zhiyuan Liu. 2023. Augmentation-Adapted Retriever Improves Generalization of Language Models as Generic Plug-In. In Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) . Association for Computational Linguistics, 2421–2436.

**中文**

https://doi.org/10.1145/3397271.3401323 [156] 于文浩，丹·伊特尔，王硕航，徐宜冲，鞠明轩，Soumya Sanyal，朱晨光，迈克尔·曾，孟江。 2023.生成而不是检索：大型语言模型是强大的上下文生成器。在国际学习表征会议（ICLR）中。 [157]于子春，熊陈艳，石宇，刘志远。 2023. 增强自适应检索器提高了语言模型作为通用插件的泛化能力。计算语言学协会第 61 届年会论文集（第一卷：长论文）。计算语言学协会，2421–2436。

### 段落 268 · Page 36

**EN**

[158] Yi Yuan, Haohe Liu, Xubo Liu, Qiushi Huang, Mark D. Plumbley, and Wenwu Wang. 2024. Retrieval-Augmented Text-to-Audio Generation. In ICASSP - IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), Vol. abs/2309.08051. IEEE. [159] Zhenrui Yue, Huimin Zeng, Yimeng Lu, Lanyu Shang, Yang Zhang, and Dong Wang. 2024. Evidence-Driven Retrieval Augmented Response Generation for Online Misinformation. In North American Chapter of the Association for Computational Linguistics, Vol. abs/2403.14952. [160] Saber Zerhoudi and Michael Granitzer. 2024.

**中文**

[158] Yi Yuan，Haohe Liu，Xubo Liu，Qieshi Huang，Mark D. Plumbley，和 Wenwu Wang。 2024.检索增强的文本到音频生成。在 ICASSP - IEEE 国际声学、语音和信号处理会议 (ICASSP)，卷。绝对/2309.08051。 IEEE。 [159]岳振瑞，曾慧敏，路一猛，商兰宇，张阳，王栋。 2024. 证据驱动的检索增强在线错误信息的响应生成。在计算语言学协会北美分会，卷。绝对/2403.14952。 [160] 萨贝尔·泽胡迪和迈克尔·格拉尼泽。 2024 年。

### 段落 269 · Page 36

**EN**

PersonaRAG: Enhancing Retrieval-Augmented Generation Systems with User-Centric Agents. arXiv (2024). [161] Susan Zhang, Stephen Roller, Naman Goyal, Mikel Artetxe, Moya Chen, Shuohui Chen, Christopher Dewan, Mona T. Diab, Xian Li, Xi Victoria Lin, Todor Mihaylov, Myle Ott, Sam Shleifer, Kurt Shuster, Daniel Simig, Punit Singh Koura, Anjali Sridhar, Tianlu Wang, and Luke Zettlemoyer. 2022. OPT: Open Pre-trained Transformer Language Models. arXiv abs/2205.01068 (2022). [162] Penghao Zhao, Hailin Zhang, Qinhan Yu, Zhengren Wang, Yunteng Geng, Fangcheng Fu, Ling Yang, Wentao Zhang, Jie Jiang, and Bin Cui. 2024.

**中文**

PersonaRAG：使用以用户为中心的代理增强检索增强生成系统。 arXiv (2024)。 [161] Susan 张、Stephen Roller、Naman Goyal、Mikel Artetxe、Moya Chen、Shuohui Chen、Christopher Dewan、Mona T. Diab、Xian Li、Xi Victoria Lin、Todor Mihaylov、Myle Ott、Sam Shleifer、Kurt Shuster、Daniel Simig、Punit Singh Koura、Anjali Sridhar、Tianlu Wang 和 Luke Zettlemoyer。 2022. OPT：开放预训练的 Transformer 语言模型。 arXiv abs/2205.01068 (2022)。 [162] 赵鹏浩，张海林，于勤瀚，王正仁，耿云腾，付方成，杨凌，张文涛，姜杰，崔斌。 2024 年。

### 段落 270 · Page 36

**EN**

Retrieval-Augmented Generation for AI-Generated Content: A Survey. arXiv abs/2402.19473 (2024). [163] Huaixiu Steven Zheng, Swaroop Mishra, Xinyun Chen, Heng-Tze Cheng, Ed H. Chi, Quoc V Le, and Denny Zhou. 2024. Take a Step Back: Evoking Reasoning via Abstraction in Large Language Models. In The Twelfth International Conference on Learning Representations , Vol. abs/2310.06117. , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

人工智能生成内容的检索增强生成：一项调查。 arXiv abs/2402.19473 (2024)。 [163] Huaxiu Steven Cheng、Swaroop Mishra、Xinyun Chen、Heng-Tze Cheng、Ed H. Chi、Quoc V Le 和 Denny Zhou。 2024.退一步：通过大型语言模型中的抽象引发推理。在第十二届学习表征国际会议，卷。绝对/2310.06117。，卷。 1、第1条。出版日期：2018 年 8 月。

### Page 37

### 段落 271 · Page 37

**EN**

The Survey of Retrieval-Augmented Text Generation in Large Language Models 37 [164] Ning Zhong, Yuefeng Li, and Sheng-Tang Wu. 2012. Effective Pattern Discovery for Text Mining. IEEE Transactions on Knowledge and Data Engineering 24, 1 (2012), 30–44. [165] Yutao Zhu, Huaying Yuan, Shuting Wang, Jiongnan Liu, Wenhan Liu, Chenlong Deng, Zhicheng Dou, and Ji-Rong Wen. 2023. Large Language Models for Information Retrieval: A Survey. arXiv abs/2308.07107 (2023). [166] Honglei Zhuang, Zhen Qin, Rolf Jagerman, Kai Hui, Ji Ma, Jing Lu, Jianmo Ni, Xuanhui Wang, and Michael Bendersky. 2023. RankT5: Fine-Tuning T5 for Text Ranking with Ranking Losses.

**中文**

大型语言模型中检索增强文本生成的调查37 [164] Ningzhong，Yuefeng Li，和Sheng-Tang Wu。 2012。文本挖掘的有效模式发现。 IEEE 知识与数据工程汇刊 24, 1 (2012), 30–44。 [165]朱玉涛，袁华英，王淑婷，刘琼南，刘文汉，邓陈龙，窦志成，文继荣。 2023. 用于信息检索的大型语言模型：一项调查。 arXiv abs/2308.07107 (2023)。 [166]庄红雷，秦臻，Rolf Jagerman，凯辉，季马，陆静，倪建模，王宣辉，Michael Bendersky。 2023.RankT5：微调 T5 以进行具有排名损失的文本排名。

### 段落 272 · Page 37

**EN**

In Proceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval . ACM. Received 20 February 2007; revised 12 March 2009; accepted 5 June 2009 , Vol. 1, No. 1, Article . Publication date: August 2018.

**中文**

第 46 届国际 ACM SIGIR 信息检索研究与开发会议论文集。 ACM。 2007 年 2 月 20 日收到； 2009 年 3 月 12 日修订； 2009 年 6 月 5 日接受，卷。 1、第1条。出版日期：2018 年 8 月。
