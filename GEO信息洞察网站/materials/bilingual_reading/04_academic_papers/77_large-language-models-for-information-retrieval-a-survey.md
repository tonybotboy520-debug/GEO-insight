# Large Language Models for Information Retrieval: A Survey

- ID: 77
- 类型: pdf
- 分类: 04_academic_papers
- 主题: LLMs in IR survey
- 原文链接: https://arxiv.org/pdf/2308.07107
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

1 Large Language Models for Information Retrieval: A Survey Yutao Zhu, Huaying Yuan, Shuting Wang, Jiongnan Liu, Wenhan Liu, Chenlong Deng Haonan Chen, Zheng Liu, Zhicheng Dou, and Ji-Rong Wen Abstract—As a primary means of information acquisition, information retrieval (IR) systems, such as search engines, have integrated themselves into our daily lives. These systems also serve as components of dialogue, question-answering, and recommender systems. The trajectory of IR has evolved dynamically from its origins in term-based methods to its integration with advanced neural models.

**中文**

1 信息检索的大型语言模型：综述 朱玉涛、袁华英、王淑婷、刘琼南、刘文汉、邓晨龙 陈浩南、刘正、窦志成、温继荣 摘要：作为信息获取的主要手段，信息检索（IR）系统（例如搜索引擎）已经融入我们的日常生活。这些系统还充当对话、问答和推荐系统的组件。 IR 的发展轨迹从基于术语的方法的起源动态发展到与先进神经模型的集成。

### 段落 2 · Page 1

**EN**

While the neural models excel at capturing complex contextual signals and semantic nuances, thereby reshaping the IR landscape, they still face challenges such as data scarcity, interpretability, and the generation of contextually plausible yet potentially inaccurate responses. This evolution requires a combination of both traditional methods (such as term-based sparse retrieval methods with rapid response) and modern neural architectures (such as language models with powerful language understanding capacity).

**中文**

虽然神经模型擅长捕获复杂的上下文信号和语义细微差别，从而重塑 IR 景观，但它们仍然面临数据稀缺、可解释性以及生成上下文合理但可能不准确的响应等挑战。这种演变需要传统方法（例如具有快速响应的基于术语的稀疏检索方法）和现代神经架构（例如具有强大语言理解能力的语言模型）的结合。

### 段落 3 · Page 1

**EN**

Meanwhile, the emergence of large language models (LLMs), typified by ChatGPT and GPT -4, has revolutionized natural language processing due to their remarkable language understanding, generation, generalization, and reasoning abilities. Consequently, recent research has sought to leverage LLMs to improve IR systems. Given the rapid evolution of this research trajectory, it is necessary to consolidate existing methodologies and provide nuanced insights through a comprehensive overview. In this survey, we delve into the confluence of LLMs and IR systems, including crucial aspects such as query rewriters, retrievers, rerankers, and readers.

**中文**

与此同时，以ChatGPT和GPT -4为代表的大型语言模型（LLM）的出现，由于其卓越的语言理解、生成、泛化和推理能力，彻底改变了自然语言处理。因此，最近的研究试图利用法学硕士来改进 IR 系统。鉴于这一研究轨迹的快速发展，有必要巩固现有的方法论，并通过全面的概述提供细致入微的见解。在本次调查中，我们深入研究了法学硕士和 IR 系统的融合，包括查询重写器、检索器、重新排序器和阅读器等关键方面。

### 段落 4 · Page 1

**EN**

Additionally, we explore promising directions, such as search agents, within this expanding field. Index Terms—Large Language Models; Information Retrieval; Query Rewriter; Reranking; Reader; Fine-tuning; Prompting; Agent ✦ 1 INTRODUCTION I NFORMATIONaccess is one of the fundamental daily needs of human beings. To fulfill the need for rapid acquisition of desired information, various information retrieval (IR) systems have been developed [1–4].

**中文**

此外，我们还在这个不断扩展的领域中探索有前途的方向，例如搜索代理。索引术语——大型语言模型；信息检索；查询重写器；重排；读者;微调;提示； Agent ✦ 1 简介信息 访问是人类基本的日常需求之一。为了满足快速获取所需信息的需求，人们开发了各种信息检索（IR）系统[1-4]。

### 段落 5 · Page 1

**EN**

Prominent examples include search engines such as Google, Bing, and Baidu, which serve as IR systems on the Internet, adept at retrieving relevant web pages in response to user queries, and provide convenient and efficient access to information on the Internet. It is worth noting that IR extends beyond web page retrieval. In dialogue systems (chatbots) [1, 5– 8], such as Microsoft Xiaoice [2], Apple Siri, 1 and Google Assistant,2 IR systems play a crucial role in retrieving appropriate responses to user input utterances, thereby producing natural and fluent human-machine conversations.

**中文**

突出的例子包括谷歌、必应和百度等搜索引擎，它们作为互联网上的IR系统，擅长根据用户查询检索相关网页，并提供便捷高效的互联网信息访问。值得注意的是，IR 不仅仅局限于网页检索。在对话系统（聊天机器人）[1, 5–8] 中，例如 Microsoft 小冰 [2]、Apple Siri、1 和 Google Assistant2，IR 系统在检索对用户输入话语的适当响应，从而产生自然流畅的人机对话方面发挥着至关重要的作用。

### 段落 6 · Page 1

**EN**

Similarly, in question-answering systems [3, 9], IR systems are employed to select relevant clues essential for addressing user questions effectively. In image search engines [4], IR systems excel at returning images that align with user input queries. Given the exponential growth of information, research and industry have become increasingly interested in the development of effective IR systems. The core function of an IR system is retrieval, which aims to determine the relevance between a user-issued query and the content to be retrieved, including various types of information such as texts, images, music, and more.

**中文**

类似地，在问答系统中 [3, 9]，IR 系统被用来选择有效解决用户问题所必需的相关线索。在图像搜索引擎 [4] 中，IR 系统擅长返回与用户输入查询相符的图像。鉴于信息的指数级增长，研究和工业界对开发有效的红外系统越来越感兴趣。 IR系统的核心功能是检索，旨在确定用户发出的查询与要检索的内容之间的相关性，包括文本、图像、音乐等各种类型的信息。

### 段落 7 · Page 1

**EN**

For All authors except Zheng Liu are from Gaoling School of Artificial Intelligence and School of Information, Renmin University of China. Zheng Liu is from Beijing Academy of Artificial Intelligence, China. Contact e-mail: yutaozhu94@gmail.com, dou@ruc.edu.cn 1. Apple Siri, https://www.apple.com/siri/ 2. Google Assistant, https://assistant.google.com/ the scope of this survey, we concentrate solely on reviewing those text retrieval systems, in which query-document relevance is commonly measured by their matching score.

**中文**

除刘峥外，所有作者均来自中国人民大学高陵人工智能学院和信息学院。刘峥来自中国北京人工智能研究院。联系电子邮件：yutaozhu94@gmail.com，dou@ruc.edu.cn 1. Apple Siri，https://www.apple.com/siri/ 2. Google Assistant，https://assistant.google.com/ 在本次调查的范围内，我们仅专注于审查那些文本检索系统，其中查询与文档的相关性通常通过其匹配分数来衡量。

### 段落 8 · Page 1

**EN**

3 Given that IR systems operate on extensive repositories, the efficiency of retrieval algorithms becomes of paramount importance. To improve the user experience, the retrieval performance is enhanced from both the upstream (query reformulation) and downstream (reranking and reading) perspectives. As an upstream technique, query reformulation is designed to refine user queries so that they are more effective at retrieving relevant documents [10, 11]. With the recent surge in the popularity of conversational search, this technique has received increasing attention.

**中文**

3 鉴于 IR 系统在广泛的存储库上运行，检索算法的效率变得至关重要。为了改善用户体验，从上游（查询重构）和下游（重新排序和阅读）角度增强检索性能。作为一种上游技术，查询重构旨在细化用户查询，以便更有效地检索相关文档 [10, 11]。随着最近对话式搜索的流行，这项技术受到了越来越多的关注。

### 段落 9 · Page 1

**EN**

On the downstream side, reranking approaches are developed to further adjust the document ranking [12–14]. In contrast to the retrieval stage, reranking is performed only on a limited set of relevant documents, already retrieved by the retriever. Under this circumstance, the emphasis is placed on achieving higher performance rather than keeping higher efficiency, allowing for the application of more complex approaches in the reranking process. Additionally, reranking can accommodate other specific requirements, such as personalization [15–18] and diversification [19–22].

**中文**

在下游方面，开发了重排方法来进一步调整文档排名[12-14]。与检索阶段相反，重新排序仅对检索器已检索的一组有限的相关文档执行。在这种情况下，重点放在实现更高的性能而不是保持更高的效率，从而允许在重新排序过程中应用更复杂的方法。此外，重排可以满足其他特定要求，例如个性化[15-18]和多样化[19-22]。

### 段落 10 · Page 1

**EN**

Following the retrieval and reranking stages, a reading component is incorporated to summarize the retrieved documents and deliver a concise document to users [23, 24]. While traditional IR systems typically require users to gather and organize relevant information themselves; however, the reading com- 3. The term “document” will henceforth refer to any text-based content subject to retrieve, including both long articles and short passages. arXiv:2308.07107v5 [cs.CL] 17 Sep 2025

**中文**

在检索和重新排序阶段之后，合并了一个阅读组件来总结检索到的文档并向用户提供简洁的文档 [23, 24]。虽然传统的红外系统通常需要用户自己收集和组织相关信息； 3. 术语“文档”今后将指任何可检索的基于文本的内容，包括长文章和短段落。 arXiv:2308.07107v5 [cs.CL] 2025 年 9 月 17 日

### Page 2

### 段落 11 · Page 2

**EN**

2 Rewriter Retriever Reranker New Queries CandidateDocumentsSelectedDocuments Reader Large Language Models ChatGPTLLaMAGLM Flan-T5 … BLOOMResponse Search Context Query𝑛 Query1 Response1 ⋯ Traditional IR Components Search Agent Query2 Response2 (1) (2) Fig. 1. Overview of existing studies that apply LLMs into IR. (1) LLMs can be used to enhance traditional IR components, such as query rewriter, retriever, reranker, and reader. (2) LLMs can also be used as search agents to perform multiple IR tasks. ponent is an integral part of new IR systems such as New Bing,4 improving users’ browsing experience and saving valuable time.

**中文**

2 Rewriter Retriever Reranker New Queries CandidateDocumentsSelectedDocuments Reader Large Language Models ChatGPTLLaMAGLM Flan-T5 … BLOOMResponse 搜索上下文 Query𝑛 Query1 Response1 ⋯ 传统 IR 组件 Search Agent Query2 Response2 (1) (2) 图 1. 将 LLM 应用到 IR 的现有研究概述。 (1) LLM 可用于增强传统的 IR 组件，例如查询重写器、检索器、重排序器和读取器。 (2) LLM 还可以用作搜索代理来执行多项 IR 任务。 ponent 是 New Bing 等新 IR 系统的组成部分，4 改善了用户的浏览体验并节省了宝贵的时间。

### 段落 12 · Page 2

**EN**

The trajectory of IR has traversed a dynamic evolution, transitioning from its origins in term-based methods to the integration of neural models. Initially, IR was anchored in term-based methods [25] and Boolean logic, focusing on keyword matching for document retrieval. The paradigm gradually shifted with the introduction of vector space models [26], unlocking the potential to capture nuanced semantic relationships between terms. This progression continued with statistical language models [27, 28], refining relevance estimation through contextual and probabilistic considerations.

**中文**

IR 的发展轨迹经历了动态演变，从基于术语的方法的起源过渡到神经模型的集成。最初，IR 锚定于基于术语的方法 [25] 和布尔逻辑，重点关注文档检索的关键字匹配。随着向量空间模型[26]的引入，范式逐渐发生转变，释放了捕获术语之间细微语义关系的潜力。这一进展在统计语言模型中得以延续 [27, 28]，通过上下文和概率考虑来完善相关性估计。

### 段落 13 · Page 2

**EN**

The influential BM25 algorithm [29] played an important role during this phase, revolutionizing relevance ranking by accounting for term frequency and document length variations. The most recent chapter in IR’s journey is marked by the ascendancy of neural models [3, 30– 32]. These models excel at capturing intricate contextual cues and semantic nuances, reshaping the landscape of IR. However, these neural models still face challenges such as data scarcity, interpretability, and the potential generation of plausible yet inaccurate responses.

**中文**

有影响力的 BM25 算法 [29] 在此阶段发挥了重要作用，通过考虑术语频率和文档长度变化彻底改变了相关性排名。 IR 旅程的最新章节以神经模型的优势为标志 [3, 30–32]。这些模型擅长捕捉复杂的上下文线索和语义细微差别，重塑 IR 的景观。然而，这些神经模型仍然面临着数据稀缺、可解释性以及可能产生看似合理但不准确的反应等挑战。

### 段落 14 · Page 2

**EN**

Thus, the evolution of IR continues to be a journey of balancing traditional strengths (such as the BM25 algorithm’s high efficiency) with the remarkable capability (such as semantic understanding) brought about by modern neural architectures. Large language models (LLMs) have recently emerged as transformative forces across various research fields, such as natural language processing (NLP) [33–35], recommender systems [36–39], finance [40], and even molecule discovery [41].

**中文**

因此，IR的进化仍然是一个平衡传统优势（例如BM25算法的高效率）与现代神经架构带来的卓越能力（例如语义理解）的旅程。大语言模型（LLM）最近已成为各个研究领域的变革力量，例如自然语言处理（NLP）[33-35]、推荐系统[36-39]、金融[40]，甚至分子发现[41]。

### 段落 15 · Page 2

**EN**

These cutting-edge LLMs are primarily based on the Transformer architecture and undergo extensive pretraining on diverse textual sources, including web pages, research articles, books, and codes. As their scale continues to expand (including both model size and data volume), LLMs have demonstrated remarkable advances in their capabilities. On the one hand, LLMs have exhibited unprecedented proficiency in language understanding and generation, resulting in responses that are more human-like and better aligned with human intentions. On the other hand, 4.

**中文**

这些前沿的法学硕士主要基于 Transformer 架构，并接受了不同文本源的广泛预训练，包括网页、研究文章、书籍和代码。随着其规模不断扩大（包括模型大小和数据量），法学硕士在其能力方面表现出了显着的进步。一方面，法学硕士在语言理解和生成方面表现出了前所未有的熟练程度，从而产生了更接近人类、更符合人类意图的反应。另一方面，4。

### 段落 16 · Page 2

**EN**

New Bing, https://www.bing.com/new the larger LLMs have shown impressive emergent abilities when dealing with complex tasks [42], such as generalization and reasoning skills. Leveraging the impressive power of LLMs can undoubtedly improve the performance of IR systems. By incorporating these advanced language models, IR systems can provide users with more accurate responses, ultimately reshaping the landscape of information access and retrieval. Initial efforts have been made to utilize the potential of LLMs in the development of novel IR systems.

**中文**

New Bing，https://www.bing.com/new 较大的法学硕士在处理复杂任务时表现出了令人印象深刻的新兴能力[42]，例如泛化和推理技能。利用法学硕士的强大力量无疑可以提高红外系统的性能。通过整合这些先进的语言模型，IR 系统可以为用户提供更准确的响应，最终重塑信息访问和检索的格局。我们已初步努力利用法学硕士在开发新型红外系统方面的潜力。

### 段落 17 · Page 2

**EN**

Notably, in terms of practical applications, New Bing is designed to improve the users’ experience of using search engines by extracting information from disparate web pages and condensing it into concise summaries that serve as responses to user-generated queries. In the research community, LLMs have proven useful within specific modules of IR systems (such as retrievers), thereby enhancing the overall performance of these systems. Due to the rapid evolution of LLMenhanced IR systems, it is essential to comprehensively review their most recent advancements and challenges.

**中文**

值得注意的是，在实际应用方面，New Bing 旨在通过从不同的网页中提取信息并将其压缩为简洁的摘要来响应用户生成的查询，从而改善用户使用搜索引擎的体验。在研究界，法学硕士已被证明在红外系统的特定模块（例如检索器）中很有用，从而提高了这些系统的整体性能。由于 LLEnhanced IR 系统的快速发展，有必要全面回顾其最新的进展和挑战。

### 段落 18 · Page 2

**EN**

Our survey provides an insightful exploration of the intersection between LLMs and IR systems, covering key perspectives such as query rewriters, retrievers, rerankers, and readers (as shown in Figure 1). 5 We also include some recent studies that leverage LLMs as search agents to perform various IR tasks. This analysis enhances our understanding of LLMs’ potential and limitations in advancing the IR field. For this survey, we create a Github repository by collecting the relevant papers and resources about applying LLMs for IR tasks (LLM4IR). 6 We will continue to update the repository with newer papers.

**中文**

我们的调查对法学硕士和 IR 系统之间的交叉点进行了深入的探索，涵盖了查询重写器、检索器、重新排序器和阅读器等关键观点（如图 1 所示）。 5 我们还纳入了一些最近的研究，这些研究利用法学硕士作为搜索代理来执行各种 IR 任务。这一分析增强了我们对法学硕士在推进国际关系领域的潜力和局限性的理解。对于本次调查，我们通过收集有关将法学硕士应用于 IR 任务 (LLM4IR) 的相关论文和资源来创建一个 Github 存储库。 6 我们将继续用新论文更新存储库。

### 段落 19 · Page 2

**EN**

This survey will also be periodically updated according to the development of this area. We notice that there are several surveys for PLMs, LLMs, and their applications (e.g., AIGC or recommender systems) [43–49]. Compared with them, we focus on the techniques and methods for developing and applying LLMs for IR systems. In addition, we suggest reading the strategy 5. As yet, there has not been a formal definition for LLMs. In this paper, we mainly focus on models with more than 1B parameters.

**中文**

该调查还将根据该领域的发展情况定期更新。我们注意到有一些针对 PLM、LLM 及其应用（例如 AIGC 或推荐系统）的调查[43-49]。与它们相比，我们专注于开发和应用红外系统法学硕士的技术和方法。此外，我们建议阅读策略5。到目前为止，LLM还没有正式的定义。在本文中，我们主要关注参数超过 1B 的模型。

### 段落 20 · Page 2

**EN**

We also notice that some methods do not rely on such strictly defined LLMs, but due to their representativeness, we still include an introduction to them in this survey. 6. https://github.com/RUC-NLPIR/LLM4IR-Survey

**中文**

我们还注意到，有些方法并不依赖于如此严格定义的法学硕士，但由于其代表性，我们仍然在本次调查中对其进行介绍。 6. https://github.com/RUC-NLPIR/LLM4IR-Survey

### Page 3

### 段落 21 · Page 3

**EN**

3 report from the Chinese IR community [50], which discusses the opportunity and future directions of IR in the era of LLMs, and we think it is an excellent supplement to this survey. The remaining part of this survey is organized as follows: Section 2 introduces the background for IR and LLMs. Section 3, 4, 5, 6 respectively review recent progress from the four perspectives of query rewriter, retriever, reranker, and reader, which are four key components of an IR system. Section 7 introduces recent studies of search agents. Then, Section 8 discusses some potential directions in future research.

**中文**

中国IR界的第3份报告[50]，讨论了LLM时代IR的机遇和未来方向，我们认为这是对本次调查的一个很好的补充。本次调查的其余部分组织如下：第 2 部分介绍 IR 和 LLM 的背景。第3、4、5、6节分别从查询重写器、检索器、重排序器和读取器四个角度回顾了最新进展，这是IR系统的四个关键组成部分。第 7 节介绍了搜索代理的最新研究。然后，第 8 节讨论了未来研究的一些潜在方向。

### 段落 22 · Page 3

**EN**

Finally, we conclude the survey in Section 9 by summarizing the major findings. 2 BACKGROUND 2.1 Information Retrieval Information retrieval (IR), as an essential branch of computer science, aims to efficiently retrieve information relevant to user queries from a large repository. Generally, users interact with an IR system by submitting their queries in textual form. Subsequently, IR systems undertake the task of matching and ranking these user-supplied queries against an indexed database, thereby facilitating the retrieval of the most pertinent results.

**中文**

最后，我们在第 9 节中总结了主要发现来结束调查。 2 背景 2.1 信息检索 信息检索（IR）作为计算机科学的一个重要分支，旨在从大型存储库中有效地检索与用户查询相关的信息。通常，用户通过以文本形式提交查询来与 IR 系统交互。随后，IR 系统承担根据索引数据库对这些用户提供的查询进行匹配和排序的任务，从而促进最相关结果的检索。

### 段落 23 · Page 3

**EN**

The field of IR has witnessed significant advancement with the emergence of various models over time. One such early model is the Boolean model, which employs Boolean logic operators to combine query terms and retrieve documents that satisfy specific conditions [25]. Based on the “bag-of-words” assumption, the vector space model [26] represents documents and queries as vectors in term-based space. Relevance estimation is then performed by assessing the lexical similarity between the query and document vectors. The efficiency of this model is further improved through the effective organization of text content using the inverted index.

**中文**

随着时间的推移，随着各种模型的出现，IR 领域取得了显着的进步。布尔模型就是这样一种早期模型，它使用布尔逻辑运算符来组合查询项并检索满足特定条件的文档[25]。基于“词袋”假设，向量空间模型[26]将文档和查询表示为基于术语的空间中的向量。然后通过评估查询向量和文档向量之间的词汇相似性来执行相关性估计。通过使用倒排索引对文本内容进行有效组织，进一步提高了该模型的效率。

### 段落 24 · Page 3

**EN**

Moving towards more sophisticated approaches, statistical language models have been introduced to estimate the likelihood of term occurrences and incorporate context information, leading to more accurate and context-aware retrieval [27, 51]. In recent years, the neural IR paradigm has gained considerable attention in the research community [30, 52, 53]. By harnessing the powerful representation capabilities of neural networks, this paradigm can capture semantic relationships between queries and documents, thereby significantly enhancing retrieval performance.

**中文**

朝着更复杂的方法发展，统计语言模型被引入来估计术语出现的可能性并合并上下文信息，从而实现更准确和上下文感知的检索[27, 51]。近年来，神经IR范式在研究界获得了相当多的关注[30,52,53]。通过利用神经网络强大的表示能力，该范式可以捕获查询和文档之间的语义关系，从而显着提高检索性能。

### 段落 25 · Page 3

**EN**

Researchers have identified several challenges with implications for the performance and effectiveness of IR systems, such as query ambiguity and retrieval efficiency. In light of these challenges, researchers have directed their attention toward crucial modules within the retrieval process, aiming to address specific issues and effectuate corresponding enhancements. The pivotal role of these modules in ameliorating the IR pipeline and elevating system performance cannot be overstated. In this survey, we focus on the following four modules, which have been greatly enhanced by LLMs.

**中文**

研究人员已经确定了对 IR 系统的性能和有效性有影响的几个挑战，例如查询歧义和检索效率。鉴于这些挑战，研究人员将注意力转向检索过程中的关键模块，旨在解决具体问题并实现相应的增强。这些模块在改善 IR 管道和提升系统性能方面的关键作用怎么强调也不为过。在本次调查中，我们重点关注以下四个模块，这些模块已通过法学硕士得到了极大的增强。

### 段落 26 · Page 3

**EN**

Query Rewriteris an essential IR module that seeks to improve the precision and expressiveness of user queries. Positioned at the early stage of the IR pipeline, this module assumes the crucial role of refining or modifying the initial query to align more accurately with the user’s information requirements. As an integral part of query rewriter, query expansion techniques, with pseudo relevance feedback being a prominent example, represent the mainstream approach to achieving query expression refinement.

**中文**

查询重写器是一个重要的 IR 模块，旨在提高用户查询的精度和表现力。该模块位于 IR 管道的早期阶段，承担着细化或修改初始查询以更准确地满足用户信息需求的关键作用。作为查询重写器的一个组成部分，查询扩展技术（以伪相关反馈为突出例子）代表了实现查询表达式细化的主流方法。

### 段落 27 · Page 3

**EN**

In addition to its utility in improving search effectiveness across general scenarios, the query rewriter finds application in diverse specialized retrieval contexts, such as personalized search and conversational search, thus further demonstrating its significance. Retriever, as discussed here, is typically employed in the early stages of IR for document recall. The evolution of retrieval technologies reflects a constant pursuit of more effective and efficient methods to address the challenges posed by ever-growing text collections.

**中文**

除了在提高一般场景的搜索效率方面的实用性之外，查询重写器还可以应用于各种专业检索上下文，例如个性化搜索和会话搜索，从而进一步证明了其重要性。正如此处所讨论的，检索器通常在 IR 的早期阶段用于文档调用。检索技术的发展反映了人们对更有效、更高效的方法的不断追求，以应对不断增长的文本集合带来的挑战。

### 段落 28 · Page 3

**EN**

In numerous experiments on IR systems over the years, the classical “bagof-words” model BM25 [29] has demonstrated its robust performance and high efficiency. In the wake of the neural IR paradigm’s ascendancy, prevalent approaches have primarily revolved around projecting queries and documents into high-dimensional vector spaces, and subsequently computing their relevance scores through inner product calculations. This paradigmatic shift enables a more efficient understanding of query-document relationships, leveraging the power of vector representations to capture semantic similarities.

**中文**

在多年来对红外系统的大量实验中，经典的“bagof-words”模型BM25[29]已经证明了其强大的性能和高效率。随着神经 IR 范式的崛起，流行的方法主要围绕将查询和文档投影到高维向量空间中，然后通过内积计算来计算它们的相关性分数。这种范式转变可以更有效GEO解查询-文档关系，利用向量表示的力量来捕获语义相似性。

### 段落 29 · Page 3

**EN**

Reranker, as another crucial module in the retrieval pipeline, primarily focuses on fine-grained reordering of documents within the retrieved document set. Different from the retriever, which emphasizes the balance of efficiency and effectiveness, the reranker module places a greater emphasis on the quality of document ranking. In pursuit of enhancing the search result quality, researchers delve into more complex matching methods than the traditional vector inner product, thereby furnishing richer matching signals to the reranker.

**中文**

Reranker 作为检索管道中的另一个关键模块，主要关注检索到的文档集中文档的细粒度重新排序。与检索器强调效率和效果的平衡不同，reranker模块更注重文档排序的质量。为了提高搜索结果质量，研究人员深入研究比传统向量内积更复杂的匹配方法，从而为重排序器提供更丰富的匹配信号。

### 段落 30 · Page 3

**EN**

Moreover, the reranker facilitates the adoption of specialized ranking strategies tailored to meet distinct user requirements, such as personalized and diversified search results. By integrating domain-specific objectives, the reranker module can deliver tailored and purposeful search results, enhancing the overall user experience. Readerhas evolved as a crucial module with the rapid development of LLM technologies. Its ability to comprehend real-time user intent and generate dynamic responses based on the retrieved text has revolutionized the presentation of IR results.

**中文**

此外，重排器有助于采用专门的排名策略，以满足不同的用户需求，例如个性化和多样化的搜索结果。通过集成特定领域的目标，重新排序模块可以提供定制的、有目的的搜索结果，从而增强整体用户体验。随着LLM技术的快速发展，Reader已经成为一个重要的模块。它能够理解实时用户意图并根据检索到的文本生成动态响应，彻底改变了 IR 结果的呈现方式。

### 段落 31 · Page 3

**EN**

In comparison to presenting a list of candidate documents, the reader module organizes answer texts more intuitively, simulating the natural way humans access information. To enhance the credibility of generated responses, the integration of references into generated responses has been an effective technique of the reader module. Furthermore, researchers explore unifying the above modules to develop a novel LLM-driven search model known as theSearch Agent. The search agent is distinguished by its simulation of an automated search and result understanding process, which furnishes users with accurate

**中文**

与呈现候选文档列表相比，阅读器模块更直观地组织答案文本，模拟人类访问信息的自然方式。为了提高生成的响应的可信度，将参考文献集成到生成的响应中一直是阅读器模块的有效技术。此外，研究人员探索统一上述模块来开发一种新颖的法学硕士驱动的搜索模型，称为搜索代理。该搜索代理的特点是模拟自动搜索和结果理解过程，为用户提供准确的信息

### Page 4

### 段落 32 · Page 4

**EN**

4 and readily comprehensible answers. WebGPT [24] serves as a pioneering work in this category, which models the search process as a sequence of actions of an LLM-based agent within a search engine environment, autonomously accomplishing the whole search pipeline. By integrating the existing search stack, search agents have the potential to become a new paradigm in future IR. 2.2 Large Language Models Language models (LMs) are designed to understand or generate human language by taking into account the contextual information from word sequences.

**中文**

4、答案通俗易懂。 WebGPT [24] 是这一领域的开创性工作，它将搜索过程建模为搜索引擎环境中基于 LLM 的代理的一系列动作，自主完成整个搜索管道。通过集成现有的搜索堆栈，搜索代理有可能成为未来信息检索的新范例。 2.2 大型语言模型 语言模型（LM）旨在通过考虑单词序列的上下文信息来理解或生成人类语言。

### 段落 33 · Page 4

**EN**

The evolution from statistical language modelstoneural language models makes it feasible to utilize LMs for representation learning beyond mere word sequence modeling. Peters et al. [54] first proposed to learn contextualized word representations through pre-training a bidirectional LSTM (biLSTM) network on large-scale corpora, followed by fine-tuning on specific downstream tasks. Similarly, Devlin et al. [55] proposed to pre-train a Transformer [56] encoder with a specially designed Masked Language Modeling (MLM) task and Next Sentence Prediction (NSP) task on large corpora.

**中文**

统计语言模型石化语言模型的演变使得利用语言模型进行表示学习而不仅仅是单词序列建模变得可行。彼得斯等人。 [54]首先提出通过在大规模语料库上预训练双向LSTM（biLSTM）网络来学习上下文单词表示，然后对特定的下游任务进行微调。同样，德夫林等人。 [55]提出在大型语料库上使用专门设计的掩码语言建模（MLM）任务和下一句预测（NSP）任务来预训练 Transformer [56]编码器。

### 段落 34 · Page 4

**EN**

These studies initiated a new era ofpre-trained language models(PLMs), with the “pre-training then fine-tuning” paradigm emerging as the prevailing learning approach. Along this line, numerous generative PLMs (e.g., GPT-2 [33], BART [57], and T5 [58]) have been developed for text generation problems including summarization, machine translation, and dialogue generation. Recently, researchers have observed that increasing the scale of PLMs (e.g., model size or data amount) can consistently improve their performance on downstream tasks (a phenomenon commonly referred to as thescaling law[59, 60]).

**中文**

这些研究开创了预训练语言模型（PLM）的新时代，“预训练然后微调”范式成为流行的学习方法。沿着这条线，许多生成式 PLM（例如 GPT-2 [33]、BART [57] 和 T5 [58]）已被开发用于文本生成问题，包括摘要、机器翻译和对话生成。最近，研究人员观察到，增加 PLM 的规模（例如模型大小或数据量）可以持续提高其在下游任务上的性能（这种现象通常称为缩放定律[59, 60]）。

### 段落 35 · Page 4

**EN**

Moreover, large-sized PLMs exhibit promising abilities (termedemergent abilities[42]) in addressing complex tasks, which are not evident in their smaller counterparts. Therefore, the research community refers to these large-sized PLMsas large language models (LLMs). Owing to their vast number of parameters, fine-tuning LLMs for specific tasks, such as IR, is often deemed impractical. Consequently, two prevailing methods for applying LLMs have been established: in-context learning (ICL) and parameter-efficient fine-tuning.

**中文**

此外，大型 PLM 在处理复杂任务方面表现出有前途的能力（称为新兴能力[42]），而这在小型 PLM 中并不明显。因此，研究界将这些大型 PLM 称为大型语言模型 (LLM)。由于参数数量巨大，针对特定任务（例如 IR）进行微调 LLM 通常被认为是不切实际的。因此，建立了两种应用法学硕士的流行方法：上下文学习（ICL）和参数高效微调。

### 段落 36 · Page 4

**EN**

ICL is one of the emergent abilities of LLMs [34] empowering them to comprehend and furnish answers based on the provided input context, rather than relying merely on their pre-training knowledge. This method requires only the formulation of the task description and demonstrations in natural language, which are then fed as input to the LLM. Notably, parameter tuning is not required for ICL. Additionally, the efficacy of ICL can be further augmented through the adoption of chain-of-thought prompting, involving multiple demonstrations (describe the chain of thought examples) to guide the model’s reasoning process.

**中文**

ICL 是法学硕士的新兴能力之一[34]，使他们能够根据所提供的输入上下文理解并提供答案，而不仅仅是依赖于他们的训练前知识。这种方法只需要用自然语言表述任务描述和演示，然后将其作为法学硕士的输入。值得注意的是，ICL 不需要参数调整。此外，通过采用思维链提示，包括多个演示（描述思维链示例）来指导模型的推理过程，可以进一步增强 ICL 的功效。

### 段落 37 · Page 4

**EN**

ICL is the most commonly used method for applying LLMs to IR. Parameter-efficient fine-tuning [61–63] aims to reduce the number of trainable parameters while maintaining satisfactory performance. LoRA [61], for example, has been widely applied to open-source LLMs (e.g., LLaMA and BLOOM) for this purpose.

**中文**

ICL 是将法学硕士应用于 IR 的最常用方法。参数高效微调[61-63]旨在减少可训练参数的数量，同时保持令人满意的性能。例如，LoRA [61] 已被广泛应用于开源 LLM（例如 LLaMA 和 BLOOM）。

### 段落 38 · Page 4

**EN**

Recently, QLoRA [64] has been proposed to further reduce memory usage by lever- Write a passage to answer the given query:Query: what state is this zip code 85282Passage:WelcometoTEMPE,AZ85282.85282isaruralzipcodeinTempe,Arizona.Thepopulationisprimarilywhite...Query:when was pokemon green released?Passage: 𝑁× PokemonGreenwasreleasedinJapanonFebruary27th,1996.ItwasthefirstinthePokemonseriesofgamesandservedasthebasisforPokemonRedandBlue,whichwerereleasedintheUSin1998.TheoriginalPokemonGreenremainsabelovedclassicamongfansoftheseries Large Language Models Instruction Demonstrations Input (context) Generatedpassage IR systems Fig. 2.

**中文**

最近，QLoRA [64]被提出通过杠杆进一步减少内存使用 - 写一段话来回答给定的查询：查询：这个邮政编码85282是什么状态Passage：WelcometoTEMPE，AZ85282.85282isaruralzipcodeinTempe，Arizona.Thepopulationisprimarilywhite...查询：when was pokemon greenreleased？Passage：𝑁× Pokemon Green 于 1996 年 2 月 27 日在日本发布。它是 Pokemon 系列游戏中的第一款，并作为 Pokemon Red 和 Blue 的基础，后者于 1998 年在美国发布。最初的 Pokemon Green 仍然是该系列粉丝喜爱的经典大语言模型指令演示输入（上下文）生成的通道 IR 系统图 2。

### 段落 39 · Page 4

**EN**

An example of LLM-based query rewriter for ad-hoc search. The example is cited from the Query2Doc paper [65]. LLMs are used to generate a passage to supplement the original query, whereN= 0andN >0correspond to zero-shot and few-shot scenarios. aging a frozen 4-bit quantized LLM for gradient computation. Despite the exploration of parameter-efficient finetuning for various NLP tasks, its implementation in IR tasks remains relatively limited, representing a potential avenue for future research.

**中文**

用于即席搜索的基于 LLM 的查询重写器的示例。该示例引用自 Query2Doc 论文 [65]。 LLM 用于生成一段段落来补充原始查询，其中 N= 0 且 N >0 对应于零样本和少样本场景。老化冻结的 4 位量化 LLM 以进行梯度计算。尽管对各种 NLP 任务的参数高效微调进行了探索，但其在 IR 任务中的实现仍然相对有限，这代表了未来研究的潜在途径。

### 段落 40 · Page 4

**EN**

Recently, research has focused on enhancing LLM capabilities by improving their reasoning and inference-time processes.Large reasoning models(LRMs) are an evolution of LLMs specifically designed to excel at complex logical tasks such as mathematics and coding. These models often employ advanced training methodologies, including reinforcement learning, to develop sophisticated self-reflection and planning mechanisms. They are designed to generate a detailed “thinking process” before providing a final answer, which has shown improved performance on reasoning benchmarks.

**中文**

最近，研究的重点是通过改进推理和推理时间过程来增强法学硕士的能力。大型推理模型（LRM）是法学硕士的演变，专门设计用于擅长数学和编码等复杂的逻辑任务。这些模型通常采用先进的训练方法，包括强化学习，来开发复杂的自我反思和规划机制。它们旨在在提供最终答案之前生成详细的“思考过程”，这在推理基准测试中表现出了改进的性能。

### 段落 41 · Page 4

**EN**

This focus on improving the reasoning process is highly relevant to test-time scaling, a paradigm that allocates additional computational resources during inference to improve model performance without increasing model size during pre-training. This can involve generating multiple outputs in parallel and selecting the best one, or employing sequential methods where the model iteratively refines its own output. By achieving promising results on expert-level human challenges, these LRMs provide a new paradigm for IR systems.

**中文**

这种对改进推理过程的关注与测试时间缩放高度相关，测试时间缩放是一种在推理过程中分配额外计算资源以提高模型性能而无需在预训练期间增加模型大小的范例。这可能涉及并行生成多个输出并选择最佳输出，或者采用顺序方法，其中模型迭代地完善其自身的输出。通过在专家级人类挑战上取得有希望的结果，这些 LRM 为 IR 系统提供了新的范例。

### 段落 42 · Page 4

**EN**

3 QUERYREWRITER Query rewriter, functioning as an essential preprocessing component for search engines, increases the accuracy of retrieval systems through the refinement of initial queries [66]. This mechanism, also known as query expansion or reformulation, holds a pivotal position in search engine operations. In the context of ad-hoc retrieval, the design of a query rewriter aims to mitigate the vocabulary mismatch problem by enriching original queries with semantically related terms. As conversational search evolves, query rewriters have evolved to interpret user intent and previous

**中文**

3 QUERYREWRITER 查询重写器作为搜索引擎的重要预处理组件，通过细化初始查询来提高检索系统的准确性[66]。这种机制也称为查询扩展或重构，在搜索引擎操作中占有举足轻重的地位。在即席检索的背景下，查询重写器的设计旨在通过使用语义相关术语丰富原始查询来减轻词汇不匹配问题。随着对话式搜索的发展，查询重写器已经发展到能够解释用户意图和之前的意图

### Page 5

### 段落 43 · Page 5

**EN**

5 TABLE 1. Overview of existing LLM-based query rewriting methods. “Knowledge” denotes the source of information the method employs for query rewriting. “SFT” and “RL” denotes supervised fine-tuning and reinforcement learning, respectively. “Q”, “K”, and “A” refer to question, keyword, and answer-incorporated passages, respectively. Scenario Knowledge Approach Format Method Ad-hoc LLMs PromptingAHyDE [75] LLM PromptingAJagerman et al. [76] LLM PromptingAQuery2Doc [65] LLM PromptingABaek et al. [77] LLM PromptingQAlaofi et al. [78] LLM PromptingKLi et al. [79] LLM RLKMa et al.

**中文**

5 表 1. 现有基于 LLM 的查询重写方法概述。 “知识”表示该方法用于查询重写的信息源。 “SFT”和“RL”分别表示监督微调和强化学习。 “Q”、“K”和“A”分别指问题、关键词和答案合并的段落。场景知识方法格式方法临时 LLM PromptingAHyDE [75] LLM PromptingAJagerman 等人。 [76] LLM PromptingAQuery2Doc [65] LLM PromptingABaek 等人。 [77] 法学硕士提示QAlaofi 等人。 [78] 法学硕士提示KLi 等人。 [79] 法学硕士 RLKMa 等。

### 段落 44 · Page 5

**EN**

[80] LLM SFT & RLKBEQUE [81] LLM + Corpora PromptingKGRF+PRF [82] LLM + Corpora PromptingAGRM [83] LLM + Corpora PromptingAInteR [84] LLM + Corpora PromptingALameR [85] LLM + Corpora PromptingACSQE [86] LLM + Corpora PromptingQCAR [87] LLM + Corpora SFT & RLQRaFe [88] Conversational LLM PromptingQLLMCS [89] LLM PromptingQCONVERSER [90] LLM PromptingQYe et al. [91] dialogues, thereby enabling context-sensitive queries. In this survey, the term “query rewriter” is used to refer to any technique that improves retrieval performance through query modification.

**中文**

[80] 法学硕士 SFT 和 RLBBEQUE [81] 法学硕士 + 语料库提示 KGRF+PRF [82] 法学硕士 + 语料库提示AGRM [83] 法学硕士 + 语料库提示AInteR [84] 法学硕士 + 语料库提示ALameR [85] 法学硕士 + 语料库提示ACSQE [86] 法学硕士 + 语料库提示QCAR [87] 法学硕士 + 语料库 SFT & RLQRaFe [88] 会话式 LLM PromptingQLLMCS [89] LLM PromptingQCONVERSER [90] LLM PromptingQYe 等人。 [91]对话，从而实现上下文相关的查询。在本次调查中，术语“查询重写器”用于指通过查询修改来提高检索性能的任何技术。

### 段落 45 · Page 5

**EN**

Traditional query rewriting strategies primarily include techniques such as utilizing lexical knowledge bases [67– 71] and pseudo-relevance feedback [72–74]. However, these methods are limited due to the inadequate capabilities of knowledge models and the presence of noisy signals from coarse matching between the query and the top-k retrieved documents. LLMs, pretrained on vast datasets, demonstrate considerable advancements in the breadth of knowledge and language understanding, positioning them as an excellent resource for query rewriting tasks.

**中文**

传统的查询重写策略主要包括利用词汇知识库[67-71]和伪相关反馈[72-74]等技术。然而，由于知识模型的能力不足以及查询和前 k 个检索到的文档之间的粗匹配存在噪声信号，这些方法受到限制。在大量数据集上进行预训练的法学硕士在知识广度和语言理解方面表现出了相当大的进步，将其定位为查询重写任务的优秀资源。

### 段落 46 · Page 5

**EN**

In the subsequent sections, we provide a comprehensive review of recent research that applies LLMs to query rewriting. 3.1 Rewriting Scenarios In the realm of IR, a query rewriter is primarily designed to serve two distinct scenarios: ad-hoc retrieval and conversational search. Ad-hoc retrieval aims to bridge the semantic gap between a user’s query and the potential documents. LLMs, with their extensive inherent knowledge, have proven effective in replacing traditional lexical knowledge databases [67–71].

**中文**

在后续部分中，我们将全面回顾最近将法学硕士应用于查询重写的研究。 3.1 重写场景 在 IR 领域，查询重写器主要设计用于服务两种不同的场景：即席检索和会话搜索。即席检索旨在弥合用户查询和潜在文档之间的语义差距。法学硕士凭借其广泛的固有知识，已被证明可以有效替代传统的词汇知识数据库[67-71]。

### 段落 47 · Page 5

**EN**

For conversational search, query rewriters aim to refine a query within a conversation’s context, transforming it into isolated queries based on historical dialogues. A crucial requirement for conversational query rewriters is to address coreference resolution. Traditional query rewriting methods, trained on limited data, have shown suboptimal performance, as conversational search sessions tend to be diverse and long-tailed [92, 93]. This is particularly the case in more complex conversational search sessions.

**中文**

对于对话式搜索，查询重写器的目标是在对话上下文中细化查询，将其转换为基于历史对话的孤立查询。会话查询重写器的一个关键要求是解决共指解析问题。传统的查询重写方法在有限的数据上进行训练，表现出次优的性能，因为会话搜索会话往往是多样化的和长尾的 [92, 93]。在更复杂的会话搜索会话中尤其如此。

### 段落 48 · Page 5

**EN**

However, LLMs, with their robust context understanding capabilities, Reformulate the current question into a de-contextualized rewrite under the multi-turn information-seeking dialog context and generate a correct response.Turn 1:Question: What should I consider when buying a phone?Rewrite: This is the first turn. So, the question should be rewritten as: What should I consider when buying a phone? Response: The design of the phone and the overall ...Turn 2:Question: Cool. Which one would you recommend?Rewrite: Based on Turn 1, you are inquiring about what should be considered when buying a phone. So, the question should be rewritten as: Cool.

**中文**

然而，法学硕士凭借其强大的上下文理解能力，将当前问题重新表述为多轮信息搜索对话上下文下的去上下文化重写，并生成正确的响应。第1轮：问题：购买手机时我应该考虑什么？重写：这是第一个轮。那么，问题应该改写为：购买手机时应该考虑什么？回应：手机的设计和整体...转2：问题：酷。您会推荐哪一款？重写：根据第 1 回合，您询问购买手机时应考虑什么。所以，这个问题应该改写为：酷。

### 段落 49 · Page 5

**EN**

Which smartphone would you recommend for me?Response: Just because a phone has everything ...Turn 1: Question: What was the basis of the Watergate scandal? Rewrite: ... Response: ... Turn 2: … 𝑁× Turn t: Question: So, what happened to Nixon? Rewrite: Based on all previous turns, Nixon was badly involved in the Watergate scandal. So, the question should be rewritten as: So, what happened to Nixon after the events of the Watergate scandal? Response: With the mounting evidence and loss... Large Language Models Generatedquery IR systems Fig. 3. An example of LLM-based query rewriter for conversational search (cited from LLMCS [89]) .

**中文**

您会为我推荐哪款智能手机？回应：仅仅因为手机拥有一切...第 1 回合：问题：水门丑闻的基础是什么？重写：... 响应：... 第 2 轮：... 𝑁× 转 t：问题：那么，尼克松出了什么事？重写：根据之前的所有转折，尼克松严重卷入了水门丑闻。所以，这个问题应该改写为：那么，水门丑闻事件发生后，尼克松发生了什么？回应：随着越来越多的证据和损失...大型语言模型生成的查询 IR 系统 图 3. 用于会话搜索的基于 LLM 的查询重写器的示例（引自 LLMCS [89]）。

### 段落 50 · Page 5

**EN**

An LLM is used to generate a query and system response based on the demonstrations and previous search context.N= 0 andN >0correspond to zero-shot and few-shot scenarios respectively. have demonstrated significant advantages in conversational query rewriting [89, 90]. Beyond traditional retrieval scenarios, query rewriting is also widely used in a variety of practical domains. In the context of agents, effectively identifying the most relevant tools for a given task becomes a key bottleneck as the toolset size grows, hindering reliable tool utilization.

**中文**

LLM 用于根据演示和先前的搜索上下文生成查询和系统响应。N= 0 和 N >0 分别对应于零样本和少样本场景。在会话查询重写方面表现出了显着的优势[89, 90]。除了传统的检索场景之外，查询重写还广泛应用于各种实际领域。在代理的背景下，随着工具集大小的增长，有效地识别给定任务最相关的工具成为一个关键瓶颈，阻碍了工具的可靠利用。

### 段落 51 · Page 5

**EN**

To address this, current study [94] propose generating a diverse set of synthetic queries that comprehensively cover different aspects of the query space associated with each tool document during the tool indexing phase. On the other hand, in clinical terminology normalization, recent study [95] also leverage large language models to decompose and reconstruct complex diagnostic mentions, improving the mapping to standard terms through a ”retrieve-and-rank” framework to enhance overall performance.

**中文**

为了解决这个问题，当前的研究[94]建议生成一组多样化的综合查询，这些查询全面覆盖在工具索引阶段与每个工具文档关联的查询空间的不同方面。另一方面，在临床术语标准化方面，最近的研究[95]还利用大型语言模型来分解和重​​建复杂的诊断提及，通过“检索和排名”框架改进到标准术语的映射，以提高整体性能。

### 段落 52 · Page 5

**EN**

By leveraging the capabilities of LLMs, researchers have been able to generate a variety of formats for rewritten queries, such as questions [78, 80, 88–91, 96, 97], answerincorporated passages [65, 75–77, 83–85, 87, 98], and keywords [80–82, 99]. Comprehensive details for each format are available in the following part. 3.2 Formats of Rewritten Queries The intended format for rewritten queries can vary widely based on the specific needs and the downstream retrieval

**中文**

通过利用法学硕士的功能，研究人员已经能够生成各种格式的重写查询，例如问题 [78, 80, 88–91, 96, 97]、答案合并段落 [65, 75–77, 83–85, 87, 98] 和关键字 [80–82, 99]。以下部分提供了每种格式的全面详细信息。 3.2 重写查询的格式重写查询的预期格式可以根据具体需求和下游检索而有很大不同

### Page 6

### 段落 53 · Page 6

**EN**

6 system. The ultimate goal is to improve the effectiveness of IR. Typically, the formats include questions, keywords, and answer-incorporated passages. 3.2.1 Questions Rewriting original queries into similar form questions are a natural idea of query rewriting [78, 88, 91]. Query rewriters modify original queries to new questions to make it more precise, understandable, and aligned with the user’s actual search intent. This can involve rephrasing, expanding, or simplifying the query. Recent research [78] has demonstrated the potential of using LLMs to generate query variants.

**中文**

6系统。最终目标是提高IR的有效性。通常，格式包括问题、关键字和包含答案的段落。 3.2.1 问题 将原始查询重写为类似形式的问题是查询重写的自然想法[78,88,91]。查询重写器将原始查询修改为新问题，使其更加精确、易于理解并符合用户的实际搜索意图。这可能涉及重新措辞、扩展或简化查询。最近的研究 [78] 证明了使用 LLM 生成查询变体的潜力。

### 段落 54 · Page 6

**EN**

Although these variants cannot cover the full range of human-generated ones, they do produce highly similar sets of relevant documents. 3.2.2 Keywords Keywords serve as a high-level abstraction of the concepts contained within a query. Rewriting queries into keywords proves particularly effective when the downstream retriever is a sparse retriever. With specific instructions, LLMs can produce high-quality keywords or concepts for query rewriting [76, 80–82]. For example, BEQUE [81] formulates new queries as keywords for effective product searches, and Li et al.

**中文**

尽管这些变体不能涵盖人类生成的全部范围，但它们确实产生了高度相似的相关文档集。 3.2.2 关键字 关键字充当查询中包含的概念的高级抽象。当下游检索器是稀疏检索器时，将查询重写为关键字被证明特别有效。通过具体说明，法学硕士可以生成高质量的关键字或概念以进行查询重写 [76, 80–82]。例如，BEQUE [81] 将新查询制定为有效产品搜索的关键字，Li 等人。

### 段落 55 · Page 6

**EN**

[79] introduce a two-round query rewriting process, which first generates a set of high-quality seed keywords, then utilizes these keywords to enhance the query. 3.2.3 Answer-incorporated Passages The semantic gap between short-form queries and longform documents has been a persistent challenge. The advent of LLMs with their inherent question-answering capabilities has introduced a novel approach to query rewriting. This approach involves initially utilizing LLMs to generate comprehensive answers to the given queries.

**中文**

[79]引入了两轮查询重写过程，首先生成一组高质量的种子关键字，然后利用这些关键字来增强查询。 3.2.3 包含答案的段落 短格式查询和长格式文档之间的语义差距一直是一个持续的挑战。法学硕士的出现及其固有的问答能力引入了一种新颖的查询重写方法。这种方法首先涉及利用法学硕士来生成给定查询的全面答案。

### 段落 56 · Page 6

**EN**

These detailed answers are then employed to retrieve relevant passages from the corpus, thereby effectively bridging the semantic divide between short queries and long candidate documents. The prompt employed for this mechanism is typically structured as follows: “Given a question query and its potential answer passages passages, compose a passage that provides an answer to the question” [84, 85]. This approach enables a more nuanced and contextually relevant retrieval of information, enhancing the overall effectiveness of the query rewriting process [65, 75–77, 83–85].

**中文**

然后使用这些详细答案从语料库中检索相关段落，从而有效地弥合短查询和长候选文档之间的语义鸿沟。这种机制所采用的提示通常结构如下：“给定一个问题查询及其潜在的答案段落，撰写一个提供问题答案的段落”[84, 85]。这种方法可以实现更细致且与上下文相关的信息检索，从而提高查询重写过程的整体有效性[65,75–77,83–85]。

### 段落 57 · Page 6

**EN**

3.3 Approaches The utilization of LLMs in query rewriting can be categorized into three primary methodologies:prompting,supervised fine-tuning, andreinforcement learning. The prompting approaches employ specific prompts to guide the LLM’s output, providing flexibility and interpretability. The supervised fine-tuning techniques adapt pre-trained LLMs to the specific task of query rewriting. However, the scarcity of training data for query rewriting often poses a challenge. To address this issue, reinforcement learning methods utilize feedback from downstream applications, thereby improving the performance of query rewriters.

**中文**

3.3 方法 LLM 在查询重写中的应用可以分为三种主要方法：提示、监督微调和强化学习。提示方法采用特定的提示来指导法学硕士的输出，提供灵活性和可解释性。监督微调技术使预训练的 LLM 适应查询重写的特定任务。然而，用于查询重写的训练数据的稀缺通常会带来挑战。为了解决这个问题，强化学习方法利用下游应用程序的反馈，从而提高查询重写器的性能。

### 段落 58 · Page 6

**EN**

In the following section, we will introduce these three methods in detail. TABLE 2. Examples of different prompting methods in query rewriter. Methods Prompts Zero-shot HyDE [75] Please write a passage to answer the question. Question:{#Question}Passage: LameR [85] Give a question{#Question}and its possible answering passages: A.{#Passage 1}B.{#Passage 2} C.{#Passage 3}... Please write a correct answering passage. Few-shot Query2Doc [65] Write a passage that answers the given query: Query:{#Query 1} Passage:{#Passage 1} ...

**中文**

在下面的部分中，我们将详细介绍这三种方法。表 2. 查询重写器中不同提示方法的示例。方法提示零样本 HyDE [75] 请写一篇文章来回答问题。问题：{#Question}段落：LameR [85] 给出一个问题{#Question}及其可能的回答段落：A.{#Passage 1}B.{#Passage 2} C.{#Passage 3}...请写出正确的回答段落。 Few-shot Query2Doc [65] 编写一段回答给定查询的段落： Query:{#Query 1} Passage:{#Passage 1} ...

### 段落 59 · Page 6

**EN**

Query:{#Query} Passage: Chain-of-Thought CoT [76] Answer the following query based on the context: Context:{#PRF doc 1} {#PRF doc 2} {#PRF doc 3} Query:{#Query} Give the rationale before answering 3.3.1 Prompting Prompting in LLMs refers to the technique of providing a specific instruction or context to guide the model’s generation of text. The prompt serves as a conditioning signal and influences the language generation process of the model. Existing prompting strategies can be roughly categorized into three groups: zero-shot prompting, few-shot prompting, and chain-of-thought (CoT) prompting [100].

**中文**

查询：{#Query} 段落：思想链 CoT [76] 根据上下文回答以下查询： 上下文：{#PRF doc 1} {#PRF doc 2} {#PRF doc 3} 查询：{#Query} 在回答之前给出基本原理 3.3.1 提示 法学硕士中的提示是指提供特定指令或上下文来指导模型生成文本的技术。提示充当条件信号并影响模型的语言生成过程。现有的提示策略可以大致分为三类：零样本提示、少样本提示和思想链（CoT）提示[100]。

### 段落 60 · Page 6

**EN**

•Zero-shot prompting.Zero-shot prompting involves instructing the model to generate texts on a specific topic without any prior exposure to training examples in that domain or topic. The model relies on its pre-existing knowledge and language understanding to generate coherent and contextually relevant expanded terms for original queries. Experiments show that zero-shot prompting is a simple yet effective method for query rewriter [76, 78, 82, 84, 85, 101].

**中文**

•零样本提示。零样本提示涉及指示模型生成特定主题的文本，而无需事先接触该领域或主题的训练示例。该模型依靠其预先存在的知识和语言理解来为原始查询生成连贯且上下文相关的扩展术语。实验表明，零样本提示是一种简单而有效的查询重写方法[76,78,82,84,85,101]。

### 段落 61 · Page 6

**EN**

•Few-shot prompting.Few-shot prompting, also known as in-context learning, involves providing the model with a limited set of examples or demonstrations related to the desired task or domain [65, 76, 78, 101]. These examples serve as a form of explicit instruction, allowing the model to adapt its language generation to specific tasks or domains. Query2Doc [65] prompts LLMs to write a document that answers the query with some demo query-document pairs provided by the ranking dataset, such as MSMARCO [102] and NQ [103]. This work experiments with a single prompt.

**中文**

•少样本提示。少样本提示，也称为上下文学习，涉及为模型提供与所需任务或领域相关的一组有限的示例或演示[65,76,78,101]。这些示例作为显式指令的一种形式，允许模型使其语言生成适应特定的任务或领域。 Query2Doc [65] 提示法学硕士编写一个文档，用排名数据集提供的一些演示查询文档对来回答查询，例如 MSMARCO [102] 和 NQ [103]。这项工作以单一提示进行实验。

### 段落 62 · Page 6

**EN**

To further study the impact of different prompt designing, recent works [76] have explored eight different prompts, such as prompting LLMs to generate query expansion terms instead of entire pseudo documents and CoT prompting. Some illustrative prompts are shown in Table 2. The experiments validate that Query2Doc is more effective than many other prompt-based methods. •Chain-of-thought prompting.CoT prompting [100] is a strategy that involves iterative prompting, where the model is provided with a sequence of instructions or partial outputs [76, 78, 104, 105]. In conversational search, the pro-

**中文**

为了进一步研究不同提示设计的影响，最近的工作[76]探索了八种不同的提示，例如提示LLM生成查询扩展项而不是整个伪文档和CoT提示。表 2 显示了一些说明性提示。实验验证了 Query2Doc 比许多其他基于提示的方法更有效。 •思想链提示。CoT提示[100]是一种涉及迭代提示的策略，其中为模型提供一系列指令或部分输出[76,78,104,105]。在对话式搜索中，亲

### Page 7

### 段落 63 · Page 7

**EN**

7 cess of query rewriting is multi-turn, which means queries should be refined step-by-step with the interaction between search engines and users. This process naturally coincides with the CoT process. As shown in Figure 3, users can conduct the CoT process by adding some instructions during each turn, such as “Based on all previous turns, xxx”. While in ad-hoc search, there is only one round in query rewriting, so CoT could only be accomplished in a simple and coarse way. For example, as shown in Table 2, researchers add “Give the rationale before answering” in the instructions to prompt LLMs to think deeply [76].

**中文**

7 查询重写的过程是多轮的，这意味着查询应该在搜索引擎和用户之间的交互中逐步细化。这个过程自然与CoT过程重合。如图3所示，用户可以通过在每个回合中添加一些指令来进行CoT过程，例如“基于所有先前的回合，xxx”。而在ad-hoc搜索中，查询重写只有一轮，因此CoT只能以简单粗暴的方式完成。例如，如表2所示，研究人员在说明中添加“回答前给出理由”，以促使法学硕士深入思考[76]。

### 段落 64 · Page 7

**EN**

3.3.2 Supervised Fine-tuning Prompting methods directly leverage LLMs’ strong capabilities to expand or rewrite queries. Though prompting method is effective, LLMs are not naturally designed for query rewriting task. To further tailor LLMs for this task, supervised fine-tuning (SFT) has emerged as a promising approach. A crucial aspect of this methodology is the creation of an appropriate training dataset. The process of gathering this dataset varies significantly depending on the application scenario. In the context of e-commerce search, a wealth of supervised training data for query rewriting is naturally available.

**中文**

3.3.2 有监督的微调提示方法直接利用LLM强大的能力来扩展或重写查询。尽管提示方法是有效的，但法学硕士并不是天生为查询重写任务而设计的。为了进一步定制法学硕士来完成这项任务，监督微调（SFT）已成为一种有前景的方法。该方法的一个重要方面是创建适当的训练数据集。收集此数据集的过程根据应用场景的不同而有很大差异。在电子商务搜索的背景下，自然可以获得大量用于查询重写的监督训练数据。

### 段落 65 · Page 7

**EN**

This data, sourced from the previous-generation rewriting policies of the e-commerce system, significantly simplifies the construction of the SFT dataset [81]. Conversely, in an ad-hoc retrieval scenario, the acquisition of query rewrite training data is often a challenge. To address this issue, researchers usually employ implicit feedback and reinforcement learning to train the query rewriter. 3.3.3 Reinforcement Learning Query rewriters typically serve as intermediaries for retrieval systems, and as such, they lack a dedicated or independent loss function for optimization.

**中文**

该数据来源于电子商务系统的上一代重写策略，显着简化了SFT数据集的构建[81]。相反，在临时检索场景中，查询重写训练数据的获取通常是一个挑战。为了解决这个问题，研究人员通常采用隐式反馈和强化学习来训练查询重写器。 3.3.3 强化学习 查询重写器通常充当检索系统的中介，因此，它们缺乏用于优化的专用或独立损失函数。

### 段落 66 · Page 7

**EN**

In this context, reinforcement learning (RL) presents an alternative training paradigm. The query rewriter can receive feedback signals from donwstream components, such as ranking models [88] or LLM readers [80]. For instance, ranking scores can be utilized to construct good-bad pairs for direct preference optimization [106] training. Similarly, Ma et al. [80] propose to generate answers from LLMs and then uses the results of a QA evaluation as training signals. Another approach, BEQUE [81], introduces an offline feedback system that assigns a quality score to each query based on the set of products it retrieves.

**中文**

在这种背景下，强化学习（RL）提出了另一种训练范式。查询重写器可以接收来自下游组件的反馈信号，例如排名模型[88]或LLM阅读器[80]。例如，排名分数可用于构建好坏对以进行直接偏好优化[106]训练。同样，马等人。 [80]建议从 LLM 生成答案，然后使用 QA 评估的结果作为训练信号。另一种方法 BEQUE [81] 引入了一个离线反馈系统，该系统根据每个查询检索到的产品集为其分配质量分数。

### 段落 67 · Page 7

**EN**

Recently, inspired by the rule-based reward system proposed by DeepSeek-R1 [107], some studies have explored using retrieval metrics as the reward to optimize query generators. For example, DeepRetrieval [108] proposes a RL approach that trains LLMs for query generation by using retrieval metrics as rewards without the need for supervised data. This method reinforces the query generator to produce queries that maximize retrieval performance. These RL mechanisms align the objective of query rewriters more closely with the goals of downstream tasks, thereby enhancing the overall performance of the system.

**中文**

最近，受到 DeepSeek-R1 [107] 提出的基于规则的奖励系统的启发，一些研究探索使用检索指标作为优化查询生成器的奖励。例如，DeepRetrieval [108] 提出了一种 RL 方法，通过使用检索指标作为奖励来训练 LLM 进行查询生成，而不需要监督数据。此方法增强查询生成器以生成最大化检索性能的查询。这些强化学习机制使查询重写器的目标与下游任务的目标更加紧密地结合起来，从而提高系统的整体性能。

### 段落 68 · Page 7

**EN**

3.4 Limitations Despite the potential of LLMs in query rewriting, they still suffer from several limitations. We discuss two primary challenges that arise with their use in this context. 3.4.1 Concept Drifts One significant issue is the introduction of unrelated information, or concept drift, which may occur due to the LLM’s vast knowledge base and propensity to generate detailed yet sometimes redundant content. While this can potentially enrich the query, it may also lead to irrelevant or off-target results. This issue has been reported in various studies [81, 87, 96].

**中文**

3.4 局限性 尽管法学硕士在查询重写方面具有潜力，但它们仍然受到一些限制。我们讨论了在这种情况下使用它们所带来的两个主要挑战。 3.4.1 概念漂移 一个重要的问题是引入不相关的信息或概念漂移，这可能是由于法学硕士庞大的知识库和生成详细但有时冗余的内容的倾向而发生的。虽然这可能会丰富查询，但也可能导致不相关或偏离目标的结果。各种研究都报道了这个问题[81,87,96]。

### 段落 69 · Page 7

**EN**

These works emphasize the necessity for a balanced approach to LLM-based query rewriting, maintaining the core and focus of the original query while utilizing the LLM’s capabilities to enhance and clarify it. This balance is critical for effective search and IR applications. 3.4.2 Correlation between Retrieval Performance and Expansion Effects A recent comprehensive study [109] has investigated various expansion techniques and downstream ranking models, revealing a significant negative correlation between retrieval performance and expansion benefits.

**中文**

这些工作强调了基于 LLM 的查询重写的平衡方法的必要性，保持原始查询的核心和焦点，同时利用 LLM 的功能来增强和澄清它。这种平衡对于有效的搜索和红外应用至关重要。 3.4.2 检索性能和扩展效果之间的相关性 最近的一项综合研究[109]调查了各种扩展技术和下游排序模型，揭示了检索性能和扩展收益之间存在显着的负相关关系。

### 段落 70 · Page 7

**EN**

Specifically, expansion tends to improve the scores of weaker models but adversely affects stronger ones. This finding suggests a strategic approach: only using expansions with weaker models or when the target dataset significantly varies in format from the training corpus. In other situations, it may be more beneficial to refrain from expansions to preserve the clarity of the relevance signal. 4 RETRIEVER In an IR system, the retriever serves as the first-pass document filter to collect broadly relevant documents for user queries.

**中文**

具体来说，扩展往往会提高较弱模型的分数，但会对较强模型产生不利影响。这一发现提出了一种战略方法：仅使用较弱模型的扩展或当目标数据集在格式上与训练语料库显着不同时使用扩展。在其他情况下，避免扩展以保持相关信号的清晰度可能更有利。 4 检索器 在 IR 系统中，检索器充当首轮文档过滤器，收集广泛相关的文档以供用户查询。

### 段落 71 · Page 7

**EN**

Given the enormous amounts of documents in an IR system, the retriever’s efficiency in locating relevant documents is essential for maintaining search engine performance. Meanwhile, a high recall is also important for the retriever, as the retrieved documents are then fed into the ranker to generate final results for users, which determines the ranking quality of search engines. In recent years, retrieval models have shifted from relying on statistic algorithms [29] to neural models [3, 31]. The latter approaches exhibit superior semantic capability and excel at understanding complicated user intent.

**中文**

鉴于 IR 系统中存在大量文档，检索器定位相关文档的效率对于维持搜索引擎性能至关重要。同时，高召回率对于检索器也很重要，因为检索到的文档随后被输入到排名器中，为用户生成最终结果，这决定了搜索引擎的排名质量。近年来，检索模型已经从依赖统计算法 [29] 转向神经模型 [3, 31]。后一种方法表现出卓越的语义能力，并且擅长理解复杂的用户意图。

### 段落 72 · Page 7

**EN**

The success of neural retrievers relies on two key factors:dataand model. From the data perspective, a large amount of highquality training data is essential. This enables retrievers to acquire comprehensive knowledge and accurate matching patterns. Furthermore, the intrinsic quality of search data, i.e., issued queries and document corpus, significantly influences retrieval performance. From the model perspective, a strongly representational neural architecture allows retrievers to effectively store and apply knowledge obtained from the training data.

**中文**

神经检索器的成功依赖于两个关键因素：数据和模型。从数据角度来看，大量高质量的训练数据至关重要。这使得检索者能够获得全面的知识和准确的匹配模式。此外，搜索数据的内在质量，即发出的查询和文档语料库，显着影响检索性能。从模型的角度来看，强代表性的神经架构允许检索器有效地存储和应用从训练数据中获得的知识。

### 段落 73 · Page 7

**EN**

Unfortunately, there are some long-term challenges that hinder the advancement of retrieval models. First, user queries are usually short and ambiguous, making it difficult

**中文**

不幸的是，存在一些阻碍检索模型进步的长期挑战。首先，用户查询通常简短且含糊不清，这使得查询变得困难

### Page 8

### 段落 74 · Page 8

**EN**

8 to precisely understand the user’s search intents for retrievers. Second, documents typically contain lengthy content and substantial noise, posing challenges in encoding long documents and extracting relevant information for retrieval models. Additionally, the collection of human-annotated relevance labels is time-consuming and costly. It restricts the retrievers’ knowledge boundaries and their ability to generalize across different application domains. Moreover, existing model architectures, primarily built on BERT [55], exhibit inherent limitations, thereby constraining the performance potential of retrievers.

**中文**

8 准确理解用户对检索器的搜索意图。其次，文档通常包含冗长的内容和大量的噪音，这给长文档编码和为检索模型提取相关信息带来了挑战。此外，收集人工注释的相关性标签既耗时又昂贵。它限制了检索器的知识边界及其跨不同应用领域进行泛化的能力。此外，主要基于 BERT [55] 构建的现有模型架构表现出固有的局限性，从而限制了检索器的性能潜力。

### 段落 75 · Page 8

**EN**

Recently, LLMs have exhibited extraordinary abilities in language understanding, text generation, and reasoning. This has motivated researchers to use these abilities to tackle the aforementioned challenges and aid in developing superior retrieval models. Roughly, these studies can be categorized into two groups: (1) leveraging LLMs to generate search data, and (2) employing LLMs to enhance model architecture. 4.1 Leveraging LLMs to Generate Search Data In light of the quality and quantity of search data, there are two prevalent perspectives on how to improve retrieval performance via LLMs.

**中文**

最近，法学硕士在语言理解、文本生成和推理方面表现出了非凡的能力。这促使研究人员利用这些能力来应对上述挑战并帮助开发卓越的检索模型。粗略地说，这些研究可以分为两类：（1）利用法学硕士来生成搜索数据，以及（2）利用法学硕士来增强模型架构。 4.1 利用法学硕士生成搜索数据 根据搜索数据的质量和数量，对于如何通过法学硕士提高检索性能有两种普遍的观点。

### 段落 76 · Page 8

**EN**

The first perspective revolves around search data refinement methods, which concentrate on reformulating input queries to precisely present user intents. The second perspective involves training data augmentation methods, which leverage LLMs’ generation ability to enlarge the training data for dense retrieval models, particularly in zero- or few-shot scenarios. 4.1.1 Search Data Refinement Typically, input queries consist of short sentences or keyword-based phrases that may be ambiguous and contain multiple possible user intents. Accurately determining the specific user intent is essential in such cases.

**中文**

第一个视角围绕搜索数据细化方法，该方法专注于重新制定输入查询以精确呈现用户意图。第二个角度涉及训练数据增强方法，该方法利用法学硕士的生成能力来扩大密集检索模型的训练数据，特别是在零或少样本场景中。 4.1.1 搜索数据细化 通常，输入查询由短句或基于关键字的短语组成，这些短语可能不明确并包含多种可能的用户意图。在这种情况下，准确确定特定的用户意图至关重要。

### 段落 77 · Page 8

**EN**

Moreover, documents usually contain redundant or noisy information, which poses a challenge for retrievers to extract relevance signals between queries and documents. Leveraging the strong text understanding and generation capabilities of LLMs offers a promising solution to these challenges. As yet, research efforts in this domain primarily concentrate on employing LLMs as query rewriters, aiming to refine input queries for more precise expressions of the user’s search intent. Section 3 has provided a comprehensive overview of these studies, so this section refrains from further elaboration.

**中文**

此外，文档通常包含冗余或噪声信息，这对检索器提取查询和文档之间的相关性信号提出了挑战。利用法学硕士强大的文本理解和生成能力，为这些挑战提供了一个有前景的解决方案。迄今为止，该领域的研究工作主要集中在使用法学硕士作为查询重写器，旨在细化输入查询以更准确地表达用户的搜索意图。第 3 节对这些研究进行了全面概述，因此本节不再进一步阐述。

### 段落 78 · Page 8

**EN**

In addition to query rewriter, an intriguing avenue for exploration involves using LLMs to enhance the effectiveness of retrieval by refining lengthy documents. This intriguing area remains open for further investigation and advancement. 4.1.2 Training Data Augmentation Due to the expensive economic and time costs of humanannotated labels, a common problem in training neural retrieval models is the lack of training data. Fortunately, the excellent capability of LLMs in text generation offers a potential solution.

**中文**

除了查询重写器之外，一个有趣的探索途径包括使用法学硕士通过精炼冗长的文档来提高检索的效率。这个有趣的领域仍然有待进一步研究和推进。 4.1.2 训练数据增强 由于人工标注标签昂贵的经济和时间成本，训练神经检索模型的一个常见问题是缺乏训练数据。幸运的是，法学硕士在文本生成方面的出色能力提供了一个潜在的解决方案。

### 段落 79 · Page 8

**EN**

A key research focus lies in devising strategies to leverage LLMs’ capabilities to generate pseudorelevant signals and augment the training dataset for the retrieval task. Why do we need data augmentation?Previous studies of neural retrieval models focused on supervised learning, namely training retrieval models using labeled data from specific domains. For example, MS MARCO [102] provides a vast repository, containing a million passages, more than 200,000 documents, and 100,000 queries with humanannotated relevance labels, which has greatly facilitated the development of supervised retrieval models.

**中文**

一个关键的研究重点在于制定策略，利用法学硕士的能力来生成伪相关信号并增强检索任务的训练数据集。为什么我们需要数据增强？以前对神经检索模型的研究主要集中在监督学习，即使用来自特定领域的标记数据来训练检索模型。例如，MS MARCO [102] 提供了一个巨大的存储库，包含一百万个段落、超过 200,000 个文档和 100,000 个带有人工注释相关标签的查询，这极大地促进了监督检索模型的开发。

### 段落 80 · Page 8

**EN**

However, this paradigm inherently constrains the retriever’s generalization ability for out-of-distribution data from other domains. The application spectrum of retrieval models varies from natural question-answering to biomedical IR, and it is expensive to annotate relevance labels for data from different domains. As a result, there is an emerging need for zero-shot and few-shot learning models to address this problem [120]. A common practice to improve the models’ effectiveness in a target domain without adequate label signals is through data augmentation.

**中文**

然而，这种范式本质上限制了检索器对来自其他领域的分布外数据的泛化能力。检索模型的应用范围从自然问答到生物医学IR，并且为不同领域的数据注释相关性标签的成本很高。因此，迫切需要零样本和少样本学习模型来解决这个问题[120]。在没有足够标签信号的情况下提高模型在目标域中的有效性的常见做法是通过数据增强。

### 段落 81 · Page 8

**EN**

How to apply LLMs for data augmentation?In the scenario of IR, it is easy to collect numerous documents. However, the challenging and costly task lies in gathering real user queries and labeling the relevant documents accordingly. Considering the strong text generation capability of LLMs, many researchers [110, 112] suggest using LLM-driven processes to create pseudo queries or relevance labels based on existing collections. These approaches facilitate the construction of relevant query-document pairs, enlarging the training data for retrieval models.

**中文**

如何应用LLM进行数据增强？在IR的场景下，很容易收集大量的文档。然而，具有挑战性和成本高昂的任务在于收集真实的用户查询并相应地标记相关文档。考虑到法学硕士强大的文本生成能力，许多研究人员[110, 112]建议使用法学硕士驱动的流程基于现有集合创建伪查询或相关性标签。这些方法有助于构建相关的查询-文档对，扩大检索模型的训练数据。

### 段落 82 · Page 8

**EN**

According to the type of generated data, there are three mainstream approaches that complement the LLM-based data augmentation for retrieval models,i.e., pseudo query generation, relevance label generation, and complete example generation. Their frameworks are visualized in Figure 4. •Pseudo query generation.Given the abundance of documents, a straightforward idea is to use LLMs for generating their corresponding pseudo queries. One such illustration is presented by inPairs [110], which leverages the in-context learning capability of GPT-3. This method employs a collection of query-document pairs as demonstrations.

**中文**

根据生成数据的类型，有三种主流方法可以补充基于LLM的检索模型数据增强，即伪查询生成、相关标签生成和完整示例生成。它们的框架如图 4 所示。 • 伪查询生成。考虑到文档的丰富性，一个简单的想法是使用 LLM 来生成相应的伪查询。 inPairs [110] 提出了这样一个例子，它利用了 GPT-3 的上下文学习能力。该方法使用查询-文档对的集合作为演示。

### 段落 83 · Page 8

**EN**

These pairs are combined with a document and presented as input to GPT-3, which subsequently generates possible relevant queries for the given document. By combining the same demonstration with various documents, it is easy to create a vast pool of synthetic training samples and support the finetuning of retrievers on specific target domains. To enhance the diversity of generated examples, Gecko [117] prompts LLMs to first generate a task description, and then generate pseudo queries according to the task.

**中文**

这些对与文档组合并作为 GPT-3 的输入呈现，GPT-3 随后为给定文档生成可能的相关查询。通过将相同的演示与各种文档相结合，可以轻松创建大量的合成训练样本，并支持检索器在特定目标域上的微调。为了增强生成示例的多样性，Gecko [117] 提示 LLM 首先生成任务描述，然后根据任务生成伪查询。

### 段落 84 · Page 8

**EN**

Considering the false negative problems, it further develops an LLM-based positive and negative mining strategy to discover potential relevant and hard negative documents from the corpus for generated queries, which significantly enhance the retrieval performance. Recent studies [111] have also leveraged opensourced LLMs, such as Alpaca-LLaMA and tk-Instruct, to produce sufficient pseudo queries and applied curriculum learning to pre-train dense retrievers. To enhance the reliability of these synthetic samples, a fine-tuned model (e.g., a monoT5-3B model fine-tuned on MSMARCO [112]) is employed to filter the generated queries.

**中文**

考虑到假阴性问题，它进一步开发了基于LLM的正负挖掘策略，从生成的查询的语料库中发现潜在的相关文档和硬负文档，从而显着提高检索性能。最近的研究 [111] 还利用开源法学硕士（例如 Alpaca-LLaMA 和 tk-Instruct）来产生足够的伪查询和应用课程学习来预训练密集检索器。为了增强这些合成样本的可靠性，采用微调模型（例如，在 MSMARCO [112] 上微调的 monoT5-3B 模型）来过滤生成的查询。

### 段落 85 · Page 8

**EN**

Only the top pairs with the highest estimated relevance scores are kept for

**中文**

仅保留具有最高估计相关性分数的顶部对

### Page 9

### 段落 86 · Page 9

**EN**

9 Example 1: Document: …If you are pregnant, limit caffeine to 200 milligrams each day. This is about the amount in 1½ 8 ounce cups of coffee or one 12 -ounce cup of coffee. Relevant Query: Is a little caffeine ok during pregnancy? … Example 𝑁: Document: Passiflora herbertiana. A rare passion fruit native to Australia... Relevant Query: What fruit is native to Australia? Example 𝑁 + 1: Document: {#Document} Relevant Query: Few-shot prompt Zero-shot prompt Write a Question answered by the given passage.

**中文**

9 示例 1：文档：……如果您怀孕了，请将每天的咖啡因摄入量限制在 200 毫克。这大约是 1.5 杯 8 盎司咖啡或一杯 12 盎司咖啡的含量。相关咨询：怀孕期间喝一点咖啡因可以吗？ …示例𝑁：文档：Passiflora herbertiana。澳大利亚原产一种稀有的百香果...相关查询：澳大利亚原产什么水果？示例 𝑁 + 1：文档：{#Document} 相关查询：少样本提示 零样本提示 写一个由给定段落回答的问题。

### 段落 87 · Page 9

**EN**

Passage: {#Passage} Query: Prompts & Document text LLM Filter Augmented Training Corpus Question Retriever LLM-based Relevance Estimator Augmented Training Corpus (a) Framework of pseudo query generation (2) Framework of relevance label generation Filtered Relevant Queries Pseudo Queries Soft Relevance Labels Retrieved Passages Diverse Task descriptions LLM Postprocess Augmented Training Corpus (3) Framework of complete example generation Query-PosD-NegD Triplets LLM Diversity Controller Example 1: Provided a scientific claim as query, retrieve documents that help verify or refute the claim. ?

**中文**

段落：{#Passage} 查询：提示和文档文本 LLM 过滤增强训练语料库问题检索器 基于 LLM 的相关性估计器增强训练语料库 (a) 伪查询生成框架 (2) 相关性标签生成框架 过滤相关查询 伪查询 软相关性标签 检索段落 多样化任务描述 LLM 后处理增强训练语料库 (3) 完整示例生成框架Query-PosD-NegD Triplets LLM Diversity Controller 示例 1：提供科学主张作为查询，检索有助于验证或反驳该主张的文档。？

### 段落 88 · Page 9

**EN**

… Example 𝑁: Search for documents that answer a FAQ -style query on children's nutrition. Brainstorm prompt Brainstorm a list of potentially useful text retrieval tasks. Please adhere to the following guidelines: - Specify what the query is, and what the desired documents are. - Each retrieval task should cover a wide range of queries, and should not be too specific. Your output should always be a Python list of strings only, with about 20 elements, and each element corresponds to a distinct retrieval task in one sentence. Do not explain yourself or output anything else. Be creative!

**中文**

…示例𝑁：搜索回答有关儿童营养的常见问题解答式查询的文档。头脑风暴提示 头脑风暴出一系列可能有用的文本检索任务。请遵守以下准则： - 指定查询是什么以及所需的文档是什么。 - 每个检索任务应涵盖广泛的查询范围，并且不应过于具体。您的输出应该始终只是一个 Python 字符串列表，包含大约 20 个元素，每个元素对应于一个句子中的一个不同的检索任务。不要解释自己或输出任何其他内容。有创意！

### 段落 89 · Page 9

**EN**

Generation prompt You have been assigned a retrieval task: {#Task} Your mission is to write one text retrieval example for this task in JSON format. The JSON object must contain the following keys: - "user_query": a string, a random user search query specified by the retrieval task. - "positive_document": a string, a relevant document for the user query. - "hard_negative_document": a string, a hard negative document that only appears relevant to the query. Please adhere to the following guidelines: - The "user_query" should be {#Query_type}, {#Query_length}, {#Clarity}, and diverse in topic.

**中文**

生成提示 您被分配了一项检索任务：{#Task} 您的任务是为此任务编写一个 JSON 格式的文本检索示例。 JSON 对象必须包含以下键： - “user_query”：一个字符串，由检索任务指定的随机用户搜索查询。 - “positive_document”：一个字符串，用户查询的相关文档。 - “hard_negative_document”：一个字符串，一个仅与查询相关的硬负文档。请遵守以下准则： - “user_query”应为 {#Query_type}、{#Query_length}、{#Clarity}，且主题多样。

### 段落 90 · Page 9

**EN**

- All documents should be at least {# Num_words} words long. - Both the query and documents should be in {#Language}. Your output must always be a JSON object only, do not explain yourself or output anything else. Be creative! Fig. 4. Three typical frameworks for LLM-based data augmentation in the retrieval task (right), along with their prompt examples (left). Note that the methods of relevance label generation do not treat questions as inputs but regard their generation probabilities conditioned on the retrieved passages as soft relevance labels. training.

**中文**

- 所有文档的长度应至少为 {# Num_words} 个字。 - 查询和文档都应采用{#Language}。您的输出必须始终只是 JSON 对象，不要解释自己或输出任何其他内容。有创意！图 4. 检索任务中基于 LLM 的数据增强的三种典型框架（右）及其提示示例（左）。请注意，相关性标签生成方法并不将问题视为输入，而是将其以检索到的段落为条件的生成概率视为软相关性标签。训练。

### 段落 91 · Page 9

**EN**

This “generating-then-filtering” paradigm can be conducted iteratively in a round-trip filtering manner,i.e., by first fine-tuning a retriever on the generated samples and then filtering the generated samples using this retriever. Repeating these EM-like steps until convergence can produce high-quality training sets [113]. Furthermore, by adjusting the prompt given to LLMs, they can generate queries of different types. This capability allows for a more accurate simulation of real queries with various patterns [114]. In practice, it is costly to generate a substantial number of pseudo queries through LLMs.

**中文**

这种“生成然后过滤”范例可以以往返过滤的方式迭代进行，即首先在生成的样本上微调检索器，然后使用该检索器过滤生成的样本。重复这些类似 EM 的步骤直到收敛可以产生高质量的训练集 [113]。此外，通过调整给法学硕士的提示，他们可以生成不同类型的查询。此功能允许更准确地模拟具有各种模式的真实查询[114]。实际上，通过 LLM 生成大量伪查询的成本很高。

### 段落 92 · Page 9

**EN**

Balancing the generation costs and the quality of generated samples has become an urgent problem. To tackle this, UDAPDR [115] is proposed, which first produces a limited set of synthetic queries using LLMs for the target domain. These high-quality examples are subsequently used as prompts for a smaller model to generate a large number of queries, thereby constructing the training set for that specific domain. It is worth noting that the aforementioned studies primarily rely on fixed LLMs with frozen parameters. Empirically, optimizing LLMs’ parameters can significantly improve their performance on downstream tasks.

**中文**

平衡生成成本和生成样本的质量已成为一个紧迫的问题。为了解决这个问题，提出了 UDAPDR [115]，它首先使用目标域的 LLM 生成一组有限的合成查询。这些高质量的示例随后被用作较小模型的提示，以生成大量查询，从而构建该特定领域的训练集。值得注意的是，上述研究主要依赖于具有冻结参数的固定法学硕士。根据经验，优化 LLM 的参数可以显着提高其下游任务的性能。

### 段落 93 · Page 9

**EN**

Unfortunately, this pursuit is impeded by the prohibitively high demand for computational resources. To overcome this obstacle, SPTAR [116] introduces a soft prompt tuning technique that only optimizes the prompts’ embedding layer during the training process. This approach allows LLMs to better adapt to the task of generating pseudo-queries, striking a favorable balance between training cost and generation quality. In addition to the above studies, pseudo query generation methods are also introduced in other application scenarios, such as conversational dense retrieval [90] and multilingual dense retrieval [121].

**中文**

不幸的是，这种追求因对计算资源的过高需求而受到阻碍。为了克服这个障碍，SPTAR [116]引入了一种软提示调整技术，该技术仅在训练过程中优化提示的嵌入层。这种方法使法学硕士能够更好地适应生成伪查询的任务，在训练成本和生成质量之间取得良好的平衡。除了上述研究之外，伪查询生成方法也被引入到其他应用场景中，例如会话密集检索[90]和多语言密集检索[121]。

### 段落 94 · Page 9

**EN**

•Relevance label generation.In some downstream tasks of retrieval, such as question-answering, the collection of questions is also sufficient. However, the relevance labels connecting these questions with the passages of supporting evidence are very limited. In this context, leveraging the capability of LLMs for relevance label generation is a promising approach that can augment the training corpus for retrievers. A recent method, ART [118], exemplifies this approach. It first retrieves the top-relevant passages for each question.

**中文**

•相关性标签生成。在一些检索的下游任务中，例如问答，问题的收集也足够了。然而，将这些问题与支持证据段落联系起来的相关性标签非常有限。在这种情况下，利用法学硕士的能力进行相关标签生成是一种很有前景的方法，可以增强检索器的训练语料库。最近的方法 ART [118] 例证了这种方法。它首先检索每个问题最相关的段落。

### 段落 95 · Page 9

**EN**

Then, it employs an LLM to produce the generation probabilities of the question conditioned on these top passages. After a normalization process, these probabilities serve as soft relevance labels for the training of the retriever. •Complete example generation.Recent study [119] further investigates approaches to directly utilize LLMs to generate

**中文**

然后，它使用法学硕士来生成以这些顶部段落为条件的问题的生成概率。经过归一化过程后，这些概率充当检索器训练的软相关标签。 •完成示例生成。最近的研究[119]进一步研究了直接利用法学硕士生成的方法

### Page 10

### 段落 96 · Page 10

**EN**

10 TABLE 3. The comparison of existing data augmentation methods powered by LLMs for training retrieval models. Methods # Examples Generator Synthetic Data Filter Method LLMs’ tuning InPairs [110] 3 Curie Relevant query Generation probability Fixed Ma et al.

**中文**

10 表 3. 由法学硕士支持的用于训练检索模型的现有数据增强方法的比较。方法 # 示例 生成器 合成数据 过滤器方法 法学硕士的调整 InPairs [110] 3 Curie 相关查询 生成概率 固定 Ma 等人。

### 段落 97 · Page 10

**EN**

[111] 0-2 Alpaca-LLaMA & tk-Instruct Relevant query - Fixed InPairs-v2 [112] 3 GPT-J Relevant query Relevance score from fine-tuned monoT5-3B Fixed PROMPTAGATOR [113] 0-8 FLAN Relevant query Round-trip filtering Fixed TQGen [114] 0 T0 Relevant query Generation probability Fixed UDAPDR [115] 0-3 GPT3 & FLAN-T5-XXL Relevant query Round-trip filtering Fixed SPTAR [116] 1-2 LLaMA-7B & Vicuna-7B Relevant query BM25 filtering Soft Prompt tuning Gecko [117] few-shot Unkown Relevant query - Fixed ART [118] 0 T5-XL & T5-XXL Soft relevance labels - Fixed Wang et al.

**中文**

[111] 0-2 Alpaca-LLaMA & tk-Instruct 相关查询 - 固定 InPairs-v2 [112] 3 GPT-J 相关查询 微调 monoT5-3B 的相关性分数 固定 PROMPTAGATOR [113] 0-8 FLAN 相关查询 往返过滤 固定 TQGen [114] 0 T0 相关查询 生成概率 固定 UDAPDR [115] 0-3 GPT3 & FLAN-T5-XXL 相关查询 往返过滤 固定 SPTAR [116] 1-2 LLaMA-7B & Vicuna-7B 相关查询 BM25 过滤 软提示调整 Gecko [117] 少量未知相关查询 - 固定 ART [118] 0 T5-XL & T5-XXL 软相关标签 - 固定 Wang 等人。

### 段落 98 · Page 10

**EN**

[119] 2 GPT-4 Q-PosD-NegD triplet - fixed synthetic queries and documents, hence providing tremendous diverse training examples across varied tasks and languages. This work proposes a two-stage generation pipeline, where the first stage prompts the LLM to brainstorm various retrieval tasks, and then the second stage generates corresponding “(query, positive document, negative document)” triplets to build synthetic training data. Researchers further control the length, languages, and semantic relationships of queries and documents to produce diverse training samples.

**中文**

[119] 2 GPT-4 Q-PosD-NegD 三元组 - 修复了合成查询和文档，因此提供了跨不同任务和语言的大量多样化训练示例。这项工作提出了一个两阶段生成管道，其中第一阶段提示法学硕士集思广益各种检索任务，然后第二阶段生成相应的“（查询，正文档，负文档）”三元组来构建合成训练数据。研究人员进一步控制查询和文档的长度、语言和语义关系，以产生多样化的训练样本。

### 段落 99 · Page 10

**EN**

The generated triplets, after post-processing,e.g., deduplication and JSON-format filtering, are used as training examples for optimizing dense retrievers. Additionally, to highlight the similarities and differences among the corresponding methods, we present a comparative result in Table 3. It compares the aforementioned methods from various perspectives, including the number of examples, the generator employed, the type of synthetic data produced, the method applied to filter synthetic data, and whether LLMs are fine-tuned. This table serves to facilitate a clearer understanding of the landscape of these methods.

**中文**

生成的三元组经过后处理（例如重复数据删除和 JSON 格式过滤）后，用作优化密集检索器的训练示例。此外，为了突出相应方法之间的异同，我们在表3中提供了比较结果。它从各个角度比较了上述方法，包括示例数量、使用的生成器、生成的合成数据的类型、用于过滤合成数据的方法以及LLM是否进行微调。该表有助于更清楚地了解这些方法的概况。

### 段落 100 · Page 10

**EN**

4.2 Leveraging LLMs as Retrievers’ Backbone Thanks to the superior text representation capability, LLMs excel at comprehending the underlying semantics of queries and documents. Therefore, it becomes increasingly popular to apply such large-scale models as the backbone of text retrievers, leading to substantial improvements over the conventional methods based on smaller-sized models [55]. 4.2.1 Dense Retriever The application of LLMs brings about two major impacts on dense retrieval.

**中文**

4.2 利用法学硕士作为检索器的骨干由于卓越的文本表示能力，法学硕士擅长理解查询和文档的底层语义。因此，应用这种大规模模型作为文本检索器的骨干变得越来越流行，这使得基于小型模型的传统方法有了实质性的改进[55]。 4.2.1 密集检索器 LLM的应用给密集检索带来了两大影响。

### 段落 101 · Page 10

**EN**

On one hand, it advances the ongoing progress of the existing methods, making substantial improvements in terms of both in-domain accuracy and outof-domain generalizability. On the other hand, it extends the boundaries of current methods, introducing new capabilities such as instruction following and in-context learning. Improved Existing Capacities.Dense retrieval needs to fine-tune pre-trained text encoders such that queries and documents can be transformed into semantic-rich embeddings. Therefore, the downstream retrieval performance can benefit from the utilization of stronger foundations.

**中文**

一方面，它推动了现有方法的不断进步，在域内准确性和域外泛化性方面都取得了实质性改进。另一方面，它扩展了当前方法的边界，引入了新的功能，例如指令跟踪和上下文学习。改进现有能力。密集检索需要微调预先训练的文本编码器，以便查询和文档可以转换为语义丰富的嵌入。因此，下游检索性能可以受益于使用更坚固的基础。

### 段落 102 · Page 10

**EN**

With preliminary progresses achieved by early forms of pretrained models (e.g., BERT [55] and T5 [58]), people moved on to take advantage of LLMs for dense retrieval. In this direction, a pioneer work is made by OpenAI, where a series of GPT models were fine-tuned towards text and code representation [122]. It is the first time where decodingonly transformers were effectively applied for dense retrieval. Importantly, it empirically validates that the retrieval performance can be consistently improved from the increased model size and embedding dimension.

**中文**

随着早期形式的预训练模型（例如 BERT [55] 和 T5 [58]）取得的初步进展，人们开始利用 LLM 进行密集检索。在这个方向上，OpenAI 做出了开创性的工作，其中一系列 GPT 模型针对文本和代码表示进行了微调[122]。这是第一次将仅解码Transformer有效地应用于密集检索。重要的是，它凭经验验证了通过增加模型大小和嵌入维度可以持续提高检索性能。

### 段落 103 · Page 10

**EN**

Besides, the LLM-based retrievers also exhibit superior generalizability [123, 124], as notable improvements can be achieved for not only the targeted scenario but also a variety of general tasks beyond the fine-tuned domain. Recently, the development of LLM-based dense retrievers have gotten dramatically promoted as powerful LLMs, e.g., LLaMA [35], Vicuna [125], Mistral [126], Phi [127], and Gemma [128], are made publicly available.

**中文**

此外，基于LLM的检索器还表现出卓越的泛化性[123, 124]，因为不仅可以针对目标场景，而且可以针对微调领域之外的各种一般任务实现显着的改进。最近，随着强大的 LLM（例如 LLaMA [35]、Vicuna [125]、Mistral [126]、Phi [127] 和 Gemma [128]）的公开发布，基于 LLM 的密集检索器的发展得到了极大的促进。

### 段落 104 · Page 10

**EN**

Remarkably, RepLLaMA [129], the first fine-tuned embedder on top of open-source LLM (LLaMA-2-7B), brings forth major improvements on a variety of benchmarks, including MSMARCO passage/doc retrieval [102] and BEIR [120]. Despite extra computation costs due to the expanded model scale, the first-stage retrieval accuracy with RepLLaMA alone already surpasses the multi-stage retrieval accuracy resulted from conventional methods, indicating the its potential value for real-world application.

**中文**

值得注意的是，RepLLaMA [129] 是开源 LLM (LLaMA-2-7B) 之上的第一个微调嵌入器，在各种基准上带来了重大改进，包括 MSMARCO 段落/文档检索 [102] 和 BEIR [120]。尽管模型规模扩大导致了额​​外的计算成本，但仅使用 RepLLaMA 的第一阶段检索精度就已经超过了传统方法的多阶段检索精度，表明其在实际应用中的潜在价值。

### 段落 105 · Page 10

**EN**

After that, people make exploration of other alternatives for dense retrieval, where additional improvements are continually achieved with adoption of more advanced LLMs [119, 130, 131]. To date, LLM-based embedders have dominated all major text retrieval benchmarks,e.g., currently, the leading methods on MTEB [132] are all back-ended by LLMs. In addition to the above methods which directly finetune LLMs, there are also parallel works on adapting generic LLMs as better foundations for dense retrieval.

**中文**

之后，人们探索密集检索的其他替代方案，通过采用更先进的法学硕士来不断实现额外的改进[119,130,131]。迄今为止，基于 LLM 的嵌入器已经主导了所有主要的文本检索基准，例如，目前 MTEB [132] 上的领先方法都是由 LLM 后端的。除了上述直接微调 LLM 的方法之外，还有一些平行的工作将通用 LLM 用作密集检索的更好基础。

### 段落 106 · Page 10

**EN**

For example, Llama2Vec [133] performs post pre-training of LLaMA-2 with two new pretext tasks: EBAE (embedding based autoencoding) and EBAR (embedding based auto-regression). With moderate scale of training on unlabeled corpus, it results in substantial improvements of retrieval performance over the basic Llama-2 model. Besides, NV-Embed modifies LLM’s architecture by introducing latent attention layer and bidirectional attention [134]. Both modifications contribute to the improved performance on MTEB benchmark.

**中文**

例如，Llama2Vec [133] 使用两个新的借口任务执行 LLaMA-2 的后预训练：EBAE（基于嵌入的自动编码）和 EBAR（基于嵌入的自动回归）。通过对未标记语料库进行中等规模的训练，与基本 Llama-2 模型相比，检索性能有了显着提高。此外，NV-Embed 通过引入潜在注意力层和双向注意力来修改 LLM 的架构[134]。这两项修改都有助于提高 MTEB 基准测试的性能。

### 段落 107 · Page 10

**EN**

Despite the above preliminary progresses, there are still many open challenges about LLM-based embedders, such as efficiency and adaptability, which need to be addressed in the future. Introducing New Capacities.Compared to conventional methods that use small-scale pre-trained models, LLM-

**中文**

尽管取得了上述初步进展，基于 LLM 的嵌入器仍然存在许多开放的挑战，例如效率和适应性，这些都需要在未来解决。引入新能力。与使用小规模预训练模型的传统方法相比，LLM-

### Page 11

### 段落 108 · Page 11

**EN**

11 based embedders introduce new capabilities that enhance the usability and accuracy of dense retrieval. One notable example is their ability to follow instructions, allowing LLM-based embedders to be trained for various semantic matching tasks based on user demands. For instance, an LLM-based embedder can perform document retrieval when prompted with “retrieve relevant docs for the input question”, and can be adapted for duplicate question retrieval with the prompt “retrieve questions with the same meaning as input”.

**中文**

基于 11 的嵌入器引入了新功能，可增强密集检索的可用性和准确性。一个值得注意的例子是它们遵循指令的能力，允许基于 LLM 的嵌入器根据用户需求接受各种语义匹配任务的培训。例如，基于 LLM 的嵌入器可以在提示“检索输入问题的相关文档”时执行文档检索，并且可以适用于提示“检索与输入具有相同含义的问题”的重复问题检索。

### 段落 109 · Page 11

**EN**

Although BERT-based retrievers are also fine-tuned to follow instructions [135, 136], they do not support unseen instructions as effectively as LLM-based embedders [137]. ChatRetriever [138] further leverages dialog-based instruction tuning to build LLM-based conversational embedders, enhancing their conversational retrieval capabilities. In addition to instructions, the LLM-based embedders can also be adapted through in-context learning, where the retrieval function can be updated by demonstration examples of user’s interested tasks [139].

**中文**

尽管基于 BERT 的检索器也经过微调以遵循指令 [135, 136]，但它们不像基于 LLM 的嵌入器 [137] 那样有效地支持看不见的指令。 ChatRetriever [138] 进一步利用基于对话的指令调整来构建基于 LLM 的会话嵌入器，增强其会话检索能力。除了指令之外，基于 LLM 的嵌入器还可以通过上下文学习进行调整，其中检索功能可以通过用户感兴趣的任务的演示示例进行更新[139]。

### 段落 110 · Page 11

**EN**

Another advantage of LLMbased embedders is their length-generalizable capacity, which allows them to effectively handle much longer texts than those in their training examples [137]. This makes it possible to manage retrieval applications across various text lengths while maintaining a feasible training cost. 4.2.2 Generative Retriever Traditional IR systems typically follow the “index-retrievalrank” paradigm to locate relevant documents based on user queries. Though, this approach has proven its effective in practice, it usually consist of three separate modules: the index module, the retrieval module, and the reranking module.

**中文**

基于 LLM 的嵌入器的另一个优点是它们的长度泛化能力，这使得它们能够有效地处理比训练示例中的文本长得多的文本 [137]。这使得管理各种文本长度的检索应用程序成为可能，同时保持可行的培训成本。 4.2.2 生成检索器 传统的 IR 系统通常遵循“索引检索排名”范例，根据用户查询来定位相关文档。虽然这种方法在实践中证明了其有效性，但它通常由三个独立的模块组成：索引模块、检索模块和重排序模块。

### 段落 111 · Page 11

**EN**

Optimizing these modules collectively can be challenging, potentially resulting in sub-optimal retrieval outcomes. Additionally, this paradigm demands additional storage space for pre-built indexes, further burdening storage resources. Recently, generative model-based retrieval methods [140–142] have emerged to address these challenges. These methods move away from the traditional “indexretrieval-rank” paradigm and instead use a unified model to directly generate document identifiers (i.e., DocIDs) relevant to the queries.

**中文**

共同优化这些模块可能具有挑战性，可能会导致检索结果次优。此外，这种范例需要额外的存储空间来存储预构建的索引，进一步加重了存储资源的负担。最近，基于生成模型的检索方法[140-142]的出现来解决这些挑战。这些方法摆脱了传统的“索引检索排名”范式，而是使用统一的模型直接生成与查询相关的文档标识符（即 DocID）。

### 段落 112 · Page 11

**EN**

In these generative retrieval methods, the knowledge of the document corpus is stored in the model parameters, eliminating the need for additional storage space for a separate index. Existing works have investigated the approaches of generating document identifiers through fine-tuning and prompting of LLMs [143, 144] Fine-tuning LLMs.Given the vast amount of world knowledge contained in LLMs, it is intuitive to leverage them to build generative retrievers. DSI [143] is a typical method that fine-tunes the pre-trained T5 models on retrieval datasets.

**中文**

在这些生成检索方法中，文档语料库的知识存储在模型参数中，无需为单独的索引提供额外的存储空间。现有的工作已经研究了通过 LLM 的微调和提示来生成文档标识符的方法 [143, 144] 微调 LLM。鉴于 LLM 中包含的大量世界知识，利用它们来构建生成检索器是直观的。 DSI [143] 是一种在检索数据集上微调预训练 T5 模型的典型方法。

### 段落 113 · Page 11

**EN**

The approach involves encoding queries and decoding document identifiers directly to perform retrieval. They explore multiple techniques for generating document identifiers and find that constructing semantically structured identifiers yields optimal results. In this strategy, DSI applies hierarchical clustering to group documents according to their semantic embeddings and assigns a semantic DocID to each document based on its hierarchical group. To ensure the output DocIDs are valid and do represent actual documents in the corpus, DSI constructs a trie using TABLE 4. The comparison of retrievers that leverage LLMs as the foundation.

**中文**

该方法涉及直接编码查询和解码文档标识符以执行检索。他们探索了多种生成文档标识符的技术，并发现构建语义结构化标识符可以产生最佳结果。在此策略中，DSI 根据文档的语义嵌入应用层次聚类对文档进行分组，并根据其层次组为每个文档分配语义 DocID。为了确保输出 DocID 有效并且确实代表语料库中的实际文档，DSI 使用表 4 构建了一个 trie。利用 LLM 作为基础的检索器的比较。

### 段落 114 · Page 11

**EN**

“KD” is short for “Knowledge Distillation”. Methods Backbone Architecture LLM’s tuning cpt-text [122] GPT-series Dense Pre-training & Fine-tuning GTR [123] T5 Dense Pre-training & Fine-tuning RepLLaMA [129] LLAMA Dense Fine-tuning TART-full [136] T0 & Flan-T5 Dense Fine-tuning & Prompting TART-dual [136] Contriever Dense KD & Prompting DSI [143] T5 Generative Fine-tuning LLM-URL [144] GPT-3 Generative Prompting CorpusLM [148] T5-base & Llama2-7B-Chat Generative Fine-tuning all DocIDs and utilizes a constraint beam search during the decoding process.

**中文**

“KD”是“知识蒸馏”的缩写。方法 Backbone Architecture LLM 的调整 cpt-text [122] GPT 系列密集预训练和微调 GTR [123] T5 密集预训练和微调 RepLLaMA [129] LLAMA 密集微调 TART-full [136] T0 和 Flan-T5 密集微调和提示 TART-dual [136] Contriever Dense KD 和提示 DSI [143] T5 生成式微调 LLM-URL [144] GPT-3 生成式提示 CorpusLM [148] T5-base 和 Llama2-7B-Chat 生成式微调所有 DocID 并在解码过程中使用约束束搜索。

### 段落 115 · Page 11

**EN**

Furthermore, this approach observes that the scaling law, which suggests that larger LMs lead to improved performance, is also applied to generative retrievers. Though various generative retrievers have been proposed [143, 145, 146], most of them mainly focus on fine-tuning size-limited LMs on small-size document corpus (usually a subset of MSMARCO [102]). To analyze how the model size and document-corpus size impact the effectiveness of generative retrievers, Pradeep et al. [147] conducted a comprehensive analysis by scaling up corpus size from 100k to 8.8M and scaling model size up to 11B (T5-XXL).

**中文**

此外，这种方法观察到缩放法则也适用于生成检索器，该法则表明较大的 LM 可以提高性能。尽管已经提出了各种生成检索器[143、145、146]，但它们中的大多数主要集中在小尺寸文档语料库（通常是 MSMARCO [102] 的子集）上微调大小受限的 LM。为了分析模型大小和文档语料库大小如何影响生成检索器的有效性，Pradeep 等人。 [147]通过将语料库大小从 100k 扩大到 8.8M，并将模型大小扩大到 11B (T5-XXL) 进行了全面分析。

### 段落 116 · Page 11

**EN**

The primary findings are three-fold: (1) It is still challenging for generative retrievers to cover large-scale document corpus. (2) More model parameters often bring better performance. (3) Introducing synthetic queries generated from documents to expand training samples could significantly enhance the retrieval performance. CorpusLM [148] further explores combining the retrieval and answering tasks together based on LLMs, making the two mutually reinforcing.

**中文**

主要发现有三个方面：（1）生成检索器覆盖大规模文档语料库仍然具有挑战性。 (2)更多的模型参数往往带来更好的性能。 (3)引入从文档生成的综合查询来扩展训练样本可以显着提高检索性能。 CorpusLM[148]在LLM的基础上进一步探索将检索任务和回答任务结合在一起，使两者相辅相成。

### 段落 117 · Page 11

**EN**

Researchers devise various training tasks,e.g., DocID list generation, closed-book answers generation, and RAG generation, to sufficiently leverage and enhance the world knowledge of LLMs, improving the performance of these generation tasks. Prompting LLMs.In addition to fine-tuning LLMs for retrieval, it has been found that LLMs (e.g., GPT-series models) can directly generate relevant web URLs for user queries with a few in-context demonstrations [144]. This unique capability of LLMs is believed to arise from their training exposure to various HTML resources.

**中文**

研究人员设计了各种训练任务，例如DocID列表生成、闭卷答案生成和RAG生成，以充分利用和增强LLM的世界知识，提高这些生成任务的性能。提示LLM。除了微调LLM以进行检索之外，人们还发现LLM（例如GPT系列模型）可以通过一些上下文演示直接为用户查询生成相关的Web URL [144]。法学硕士的这种独特能力被认为源于他们对各种 HTML 资源的培训接触。

### 段落 118 · Page 11

**EN**

As a result, LLMs can naturally serve as generative retrievers that directly generate document identifiers to retrieve relevant documents for input queries. To achieve this, an LLM-URL [144] model is proposed. It utilizes the GPT-3text-davinci-003model to yield candidate URLs. Furthermore, it designs regular expressions to extract valid URLs from these candidates to locate the retrieved documents. To provide a comprehensive understanding of this topic, Table 4 summarizes the common and unique characteristics of the LLM-based retrievers discussed above.

**中文**

因此，法学硕士自然可以充当生成检索器，直接生成文档标识符以检索输入查询的相关文档。为了实现这一点，提出了 LLM-URL [144] 模型。它利用 GPT-3text-davinci-003 模型来生成候选 URL。此外，它还设计了正则表达式来从这些候选者中提取有效的 URL，以定位检索到的文档。为了让您全面了解本主题，表 4 总结了上述基于 LLM 的检索器的共同特征和独特特征。

### Page 12

### 段落 119 · Page 12

**EN**

12 4.3 Limitations Though some efforts have been made for LLM-augmented retrieval, there are still many areas that require more detailed investigation. For example, a critical requirement for retrievers is fast response, while the main problem of existing LLMs is the huge model parameters and overlong inference time. Addressing this limitation of LLMs to ensure the response time of retrievers is a critical task. Moreover, even when employing LLMs to augment datasets (a context with lower inference time demands), the potential mismatch between LLM-generated texts and real user queries could impact retrieval effectiveness.

**中文**

12 4.3 局限性 尽管 LLM 增强检索已经做出了一些努力，但仍有许多领域需要更详细的研究。例如，检索器的关键要求是快速响应，而现有LLM的主要问题是模型参数庞大和推理时间过长。解决法学硕士的这一限制以确保检索器的响应时间是一项关键任务。此外，即使使用 LLM 来扩充数据集（推理时间要求较低的上下文），LLM 生成的文本与真实用户查询之间潜在的不匹配也可能会影响检索效率。

### 段落 120 · Page 12

**EN**

Furthermore, as LLMs usually lack domain-specific knowledge, they need to be finetuned on task-specific datasets before applying them to downstream tasks. Therefore, developing efficient strategies to fine-tune these LLMs with numerous parameters emerges as a key concern. 5 RERANKER Reranker, as the second-pass document filter in IR, aims to rerank a document list retrieved by the retriever (e.g., BM25) based on the query-document relevance.

**中文**

此外，由于法学硕士通常缺乏特定领域的知识，因此在将其应用于下游任务之前，需要对特定任务的数据集进行微调。因此，制定有效的策略来微调这些具有众多参数的法学硕士成为一个关键问题。 5 RERANKER Reranker作为IR中的第二遍文档过滤器，旨在根据查询文档相关性对检索器（例如BM25）检索到的文档列表进行重新排序。

### 段落 121 · Page 12

**EN**

According to the usage of LLMs, existing LLM-based reranking methods can be divided into four paradigms: utilizing LLMs as supervised rerankers, utilizing LLMs as unsupervised rerankers, utilizing LLMs for training data augmentation and reasoning-intensive rerankers. These paradigms are summarized in Table 5 and will be introduced in the following sections. Recall that we will use the termdocumentto refer to the text retrieved in general IR scenarios, including instances such as passages (e.g., passages in MS MARCO passage ranking dataset [102]).

**中文**

根据LLM的用途，现有的基于LLM的重排序方法可以分为四种范式：利用LLM作为监督重排序器、利用LLM作为无监督重排序器、利用LLM作为训练数据增强和推理密集型重排序器。表 5 总结了这些范例，并将在以下各节中介绍。回想一下，我们将使用术语“文档”来指代在一般 IR 场景中检索的文本，包括段落等实例（例如，MS MARCO 段落排名数据集中的段落 [102]）。

### 段落 122 · Page 12

**EN**

5.1 Utilizing LLMs as Supervised Rerankers Supervised fine-tuning is an important step in applying pre-trained LLMs to a reranking task. Due to the lack of awareness of ranking during pre-training, LLMs cannot appropriately measure the query-document relevance and fully understand the reranking tasks. By fine-tuning LLMs on task-specific ranking datasets, such as the MS MARCO passage ranking dataset [102], which includes signals of both relevance and irrelevance, LLMs can adjust their parameters to yield better performance in the reranking tasks.

**中文**

5.1 利用 LLM 作为监督重排序器 监督微调是将预训练的 LLM 应用于重排序任务的重要一步。由于在预训练期间缺乏排名意识，法学硕士无法正确衡量查询与文档的相关性并充分理解重排任务。通过对特定于任务的排名数据集（例如包含相关性和不相关信号的 MS MARCO 段落排名数据集 [102]）的 LLM 进行微调，LLM 可以调整其参数以在重排任务中产生更好的性能。

### 段落 123 · Page 12

**EN**

Based on the backbone model structure, we can categorize existing supervised rerankers as: (1) encoder-only, (2) encoder-decoder, and (3) decoder-only. 5.1.1 Encoder-only The encoder-based rerankers represent a significant turning point in applying LLMs to document reranking tasks. They demonstrate how some pre-trained language models (e.g., BERT [55]) can be fine-tuned to deliver highly accurate relevance predictions.

**中文**

根据主干模型结构，我们可以将现有的监督重排序器分类为：（1）仅编码器，（2）编码器-解码器，以及（3）仅解码器。 5.1.1 仅编码器 基于编码器的重排序器代表了将 LLM 应用于文档重排序任务的一个重要转折点。他们演示了如何微调一些预训练的语言模型（例如 BERT [55]）以提供高度准确的相关性预测。

### 段落 124 · Page 12

**EN**

A representative approach is monoBERT [12], which transforms a query-document pair into a sequence “[CLS]query[SEP]document[SEP]” as the model input and calculates the relevance score by feeding the “[CLS]” representation into a linear layer. The reranking model is optimized based on the cross-entropy loss. TABLE 5. Summary of existing LLM-based re-ranking methods. “Enc” and “Dec” denote encoder and decoder, respectively. Paradigm Type Method Supervised Rerankers Enc-only monoBERT [12] Enc-dec monoT5 [13], Ju et al. [149], DuoT5 [150], RankT5 [151], ListT5 [152] Dec-only RankLLaMA [129], TSARankLLM [153], Q-PEFT [154], Zhang et al.

**中文**

一种代表性方法是 monoBERT [12]，它将查询-文档对转换为序列“[CLS]查询[SEP]文档[SEP]”作为模型输入，并通过将“[CLS]”表示输入线性层来计算相关性得分。重排序模型基于交叉熵损失进行优化。表 5.现有基于 LLM 的重排方法的摘要。 “Enc”和“Dec”分别表示编码器和解码器。范式类型方法监督重排序 Enc-only monoBERT [12] Enc-dec monoT5 [13]，Ju 等人。 [149]、DuoT5 [150]、RankT5 [151]、ListT5 [152] 仅 Dec RankLLaMA [129]、TSARankLLM [153]、Q-PEFT [154]、Zhang 等人。

### 段落 125 · Page 12

**EN**

[155], PE- Rank [156] Unsupervised Rerankers Pointwise Liang et al. [157], Zhuang et al. [158], Guo et al. [159], Sachan et al. [160], Zhuang et al. [161], Sun et al. [162], Co-Prompt [163], DemoRank [164], PA- RADE [165] Listwise RankGPT [166], Liu et al. [167], CoRanking [168], Ma et al. [169], Tang et al. [170], TourRank [171], Parry et al. [172], APEER [173] Pairwise PRP [174], Zhuang et al. [175], PRP- Graph [176], Yan et al. [177] Data Augmentation – ExaRanker [178], ExaRanker-Open [179], InPars-Light [180], Askari et al. [181], Askari et al. [182], RankVicuna [183], RankZephyr [184], Sun et al.

**中文**

[155]，PE-Rank [156] 无监督重排序 Pointwise Liang 等人。 [157]，庄等人。 [158]，郭等人。 [159]，萨尚等人。 [160]，庄等人。 [161]，孙等人。 [162]、Co-Prompt [163]、DemoRank [164]、PA-RADE [165] Listwise RankGPT [166]、Liu 等人。 [167]，CoRanking [168]，Ma 等人。 [169]，唐等人。 [170]，TourRank [171]，Parry 等人。 [172]，APEER [173] 成对 PRP [174]，Zhang 等人。 [175]，PRP-Graph [176]，Yan 等人。 [177] 数据增强 – ExaRanker [178]、ExaRanker-Open [179]、InPars-Light [180]、Askari 等人。 [181]，阿斯卡里等人。 [182]、RankVicuna [183]​​、RankZephyr [184]、Sun 等人。

### 段落 126 · Page 12

**EN**

[185] Reasoningintensive Rerankers – ReasonRank [186], Rank1 [187], Rank- K [188], Rearank [189], Rank-R1 [190], TFRank [191] 5.1.2 Encoder-Decoder In this field, existing studies mainly formulate document reranking as a generation task and optimize an encoderdecoder-based reranking model [13, 149–151]. Specifically, given the query and the document, reranking models are usually fine-tuned to generate a single token, such as “true” or “false”. During inference, the query-document relevance score is determined based on the logit of the generated token.

**中文**

[185] Reasoningintense Rerankers – ReasonRank [186]、Rank1 [187]、Rank-K [188]、Rearank [189]、Rank-R1 [190]、TFRank [191] 5.1.2 Encoder-Decoder 在这一领域，现有研究主要将文档重排序制定为生成任务，并优化基于编码器解码器的重排序模型[13， 149–151]。具体来说，给定查询和文档，重排模型通常经过微调以生成单个标记，例如“true”或“false”。在推理过程中，查询-文档相关性分数是根据生成的 token 的 logit 确定的。

### 段落 127 · Page 12

**EN**

For example, a T5 model can be fine-tuned to generate classification tokens for relevant or irrelevant querydocument pairs [13]. At inference time, a softmax function is applied to the logits of “true” and “false” tokens, and the relevance score is calculated as the probability of the “true” token. The following method [149] involves a multi-view learning approach based on the T5 model. This approach simultaneously considers two tasks: generating classification tokens for a given query-document pair and generating the corresponding query conditioned on the provided document.

**中文**

例如，可以微调 T5 模型来为相关或不相关的查询文档对生成分类标记 [13]。在推理时，将 softmax 函数应用于“真”和“假”标记的逻辑，并将相关性得分计算为“真”标记的概率。以下方法[149]涉及基于T5模型的多视图学习方法。这种方法同时考虑两个任务：为给定的查询-文档对生成分类标记，并根据所提供的文档生成相应的查询。

### 段落 128 · Page 12

**EN**

DuoT5 [150] considers a triple(q, d i, dj)as the input of the T5 model and is fine-tuned to generate token “true” if documentd i is more relevant to queryq i than documentd j, and “false” otherwise. During inference, for each document di, it enumerates all other documentsd j and uses global aggregation functions to generate the relevance scores i for documentd i (e.g.,s i = P j pi,j, wherep i,j represents the probability of generating “true” when taking(q, d i, dj)as the model input). Beyond the aforementioned studies, several studies have also explored different training losses and model architectures for reranker training.

**中文**

DuoT5 [150]将三元组（q，d i，dj）视为T5模型的输入，并进行微调，如果记录的i与查询q i比记录的j更相关，则生成标记“真”，否则生成“假”。在推理过程中，对于每个文档di，它枚举所有其他文档dj，并使用全局聚合函数生成文档di的相关性分数i（例如，s i = P j pi,j，其中p i,j表示以（q，di，dj）作为模型输入时生成“true”的概率）。除了上述研究之外，一些研究还探索了用于重排序训练的不同训练损失和模型架构。

### 段落 129 · Page 12

**EN**

For example, RankT5 [151] is proposed to directly yield a numerical relevance score for each query-document pair during training and optimize the

**中文**

例如，RankT5 [151]被提议在训练期间直接生成每个查询文档对的数值相关性得分，并优化

### Page 13

### 段落 130 · Page 13

**EN**

13 ranking performance with “pairwise” or “listwise” ranking losses. It differs significantly from the previous studies that optimize rerankers by generating text tokens and using a generation loss, and the use of ranking loss (e.g., RankNet [192]) is more reasonable and aligns better with the inherent nature of the ranking task. Besides, Yoon et al. [152] propose ListT5, a listwise reranker based on Fusionin-decoder architecture. It jointly takes multiple documents as input and directly generates a reranked document list during training and inference.

**中文**

13 排名表现出现“成对”或“列表”排名损失。它与之前通过生成文本标记和使用生成损失来优化重排器的研究有很大不同，并且排名损失（例如RankNet [192]）的使用更合理，并且更好地符合排名任务的固有性质。此外，尹等人。 [152]提出了ListT5，一种基于Fusionin解码器架构的列表重排序器。它联合将多个文档作为输入，并在训练和推理过程中直接生成重新排序的文档列表。

### 段落 131 · Page 13

**EN**

5.1.3 Decoder-only Recently, there have been some attempts [129, 153–156] to rerank documents by fine-tuning decoder-only models (such as LLaMA). For example, RankLLaMA [129] proposes formatting the query-document pair into a prompt “query:{query}document:{document}[EOS]” and utilizes the last token representation for relevance calculation. Besides, TSARankLLM [153] has been proposed to bridge the gap between LLMs’ conventional training objectives and the specific needs of document reranking through two-stage training.

**中文**

5.1.3 仅解码器 最近，有人尝试通过微调仅解码器模型（例如 LLaMA）来对文档进行重新排序[129, 153–156]。例如，RankLLaMA [129]建议将查询-文档对格式化为提示“query:{query}document:{document}[EOS]”，并利用最后一个标记表示进行相关性计算。此外，TSARankLLM [153] 被提出来弥合法学硕士的传统培训目标和通过两阶段培训进行文档重新排序的特定需求之间的差距。

### 段落 132 · Page 13

**EN**

The first stage involves continuously pretraining LLMs using a large number of relevant text pairs collected from web resources, helping the LLMs to naturally generate queries relevant to the input document. The second stage focuses on improving the model’s text ranking performance using high-quality supervised data and well-designed loss functions. Peng et al. [154] propose a query-dependent parameter efficient fine-tuning (Q-PEFT) approach for ranking, which helps the LLM generate true queries based on given documents. Different from these pointwise rerankers [129, 153, 154], Zhang et al. [155] and Liu et al.

**中文**

第一阶段涉及使用从网络资源收集的大量相关文本对持续预训练法学硕士，帮助法学硕士自然生成与输入文档相关的查询。第二阶段的重点是使用高质量的监督数据和精心设计的损失函数来提高模型的文本排名性能。彭等人。 [154]提出了一种用于排名的查询相关参数高效微调（Q-PEFT）方法，这有助于法学硕士根据给定文档生成真实的查询。与这些逐点重新排序器不同[129,153,154]，Zhang 等人。 [155]和刘等人。

### 段落 133 · Page 13

**EN**

[156] proposes to train a listwise reranker that directly outputs a reranked document list. Specifically, Zhang et al. [155] first demonstrate that existing pointwise datasets (such as MS MARCO [102]), which only contain binary query-document labels, are insufficient for training efficient listwise rerankers. Then, they propose to use the ranking results of existing ranking systems (such as Cohere rerank API) as gold rankings to train a listwise reranker based on Code-LLaMA-Instruct. Liu et al.

**中文**

[156]建议训练一个列表重排序器，直接输出重排序的文档列表。具体来说，张等人。 [155]首先证明现有的逐点数据集（例如 MS MARCO [102]）仅包含二进制查询文档标签，不足以训练有效的列表重排序器。然后，他们建议使用现有排名系统（例如 Cohere rerank API）的排名结果作为黄金排名来训练基于 Code-LLaMA-Instruct 的 listwise reranker。刘等人。

### 段落 134 · Page 13

**EN**

[156] propose PE-Rank, which compresses each document in the list into a single embedding and then inputs these document embeddings into reranker, which significantly reduces the input length and improves the efficiency of reranker. 5.2 Utilizing LLMs as Unsupervised Rerankers As the size of LLMs scales up (e.g., exceeding 10 billion parameters), it becomes increasingly difficult to fine-tune the reranking model. Addressing this challenge, recent efforts have attempted to prompt LLMs to directly enhance document reranking in an unsupervised way.

**中文**

[156]提出PE-Rank，将列表中的每个文档压缩为单个嵌入，然后将这些文档嵌入输入到reranker中，这显着减少了输入长度并提高了reranker的效率。 5.2 利用 LLM 作为无监督重排序器 随着 LLM 规模的扩大（例如，超过 100 亿个参数），微调重排序模型变得越来越困难。为了应对这一挑战，最近的努力试图促使法学硕士以无监督的方式直接增强文档重排。

### 段落 135 · Page 13

**EN**

In general, these prompting strategies can be divided into three categories: pointwise, listwise, and pairwise methods. A comprehensive exploration of these strategies follows in the subsequent sections. 5.2.1 Pointwise methods The pointwise methods measure the relevance between a query and a single document, and can be categorized into two types: relevance generation [157–159, 164] and query generation [160, 161, 163]. The upper part in Figure 5 (a) shows an example of relevance generation based on a given prompt, where LLMs output a binary label (“Yes” or “No”) based on whether the document is relevant to the query.

**中文**

一般来说，这些提示策略可以分为三类：逐点法、列表法和成对法。后续章节将全面探讨这些策略。 5.2.1 逐点方法 逐点方法测量查询和单个文档之间的相关性，可以分为两种类型：相关性生成[157-159, 164]和查询生成[160,161,163]。图 5 (a) 的上半部分显示了基于给定提示的相关性生成示例，其中 LLM 根据文档是否与查询相关输出二进制标签（“是”或“否”）。

### 段落 136 · Page 13

**EN**

Following [13], the querydocument relevance scoref(q, d)can be calculated based on the log-likelihood of token “Yes” and “No” with a softmax function: f(q, d) = exp(SY ) exp(SY ) +exp(S N ) ,(1) whereS Y andS N represent the LLM’s log-likelihood scores of “Yes” and “No” respectively. In addition to binary labels, Zhuang et al. [158] propose to incorporate fine-grained relevance labels (e.g., “highly relevant”, “somewhat relevant” and “not relevant”) into the prompt, which helps LLMs more effectively differentiate among documents with varying levels of relevance to a query. Guo et al.

**中文**

按照[13]，查询文档相关性得分f(q, d)可以基于标记“是”和“否”的对数似然性，使用softmax函数计算：f(q, d) = exp(SY ) exp(SY ) +exp(S N ) ,(1) 其中S Y 和S N 分别表示LLM的“是”和“否”的对数似然得分。除了二进制标签之外，Zhang 等人。 [158]建议将细粒度的相关性标签（例如“高度相关”、“有些相关”和“不相关”）合并到提示中，这有助于法学硕士更有效地区分与查询相关程度不同的文档。郭等人。

### 段落 137 · Page 13

**EN**

[159] discuss the issues of inconsistent and biased relevance assessments of existing pointwise rerankers and introduce MCRanker that generates relevance scores based on a series of criteria from multiple perspectives. As for the query generation shown in the lower part of Figure 5 (a), the query-document relevance score is determined by the average log-likelihood of generating the actual query tokens based on the document: score= 1 |q| X i logp(q i|q<i, d,P),(2) where|q|denotes the token number of queryq,ddenotes the document, andPrepresents the provided prompt. The documents are then reranked based on their relevance scores.

**中文**

[159]讨论了现有逐点重排序器的相关性评估不一致和有偏差的问题，并引入了 MCRanker，它根据一系列标准从多个角度生成相关性分数。对于图5（a）下半部分所示的查询生成，查询-文档相关性得分由基于文档生成实际查询标记的平均对数似然确定：score= 1 |q| X i logp(q i|q<i, d,P),(2) 其中|q|表示查询q的标记编号，d表示文档，表示提供的提示。然后根据文档的相关性分数对文档进行重新排序。

### 段落 138 · Page 13

**EN**

It has been proven that some LLMs (such as T0) yield significant performance in zero-shot document reranking based on the query generation method [160]. Recently, research [161] has also shown that the LLMs that are pre-trained without any supervised instruction fine-tuning (such as LLaMA) also yield robust zero-shot ranking ability. Although effective, these methods primarily rely on a handcrafted prompt (e.g., “Please write a query based on this document”), which may not be optimal. Previous study [162] has shown that prompt has a significant impact on the performance of LLM reranker.

**中文**

事实证明，一些 LLM（例如 T0）在基于查询生成方法的零样本文档重排序中具有显着的性能[160]。最近，研究[161]还表明，在没有任何监督指令微调的情况下预训练的LLM（例如LLaMA）也能产生强大的零样本排名能力。虽然有效，但这些方法主要依赖于手工提示（例如，“请根据此文档编写查询”），这可能不是最佳的。之前的研究[162]表明提示对LLM reranker的性能有显着影响。

### 段落 139 · Page 13

**EN**

Thus, how to design appropriate prompts for ranking task is an important problem. Along this line, a discrete prompt optimization method Co-Prompt [163] is proposed for better prompt generation in reranking tasks. Besides, PaRaDe [165] proposes a difficulty-based method to select the most difficultkincontext demonstrations to include in the prompt, proving improvements compared with zero-shot performance.

**中文**

因此，如何为排序任务设计合适的提示是一个重要的问题。沿着这条线，提出了一种离散提示优化方法 Co-Prompt [163]，以便在重新排序任务中更好地生成提示。此外，PaRaDe [165] 提出了一种基于难度的方法来选择最困难的上下文演示以包含在提示中，证明与零样本性能相比有所改进。

### 段落 140 · Page 13

**EN**

Nevertheless, the experiments in the paper indicate that such difficulty-based selection does not even show a significant advantage compared to random selection, showing that the demonstration selection in ranking task is a very challenging problem. The main challenge lies in the complex nature of query-document relationship, which requires effectively combining multiple demonstrations to help the LLM understand such relationship. Aiming to select more effective demonstrations for ranking task, Liu et al. [164] propose DemoRank, an effective demonstration selection framework.

**中文**

然而，论文中的实验表明，与随机选择相比，这种基于难度的选择甚至没有表现出显着的优势，这表明排序任务中的示范选择是一个非常具有挑战性的问题。主要挑战在于查询-文档关系的复杂性，这需要有效地结合多个演示来帮助LLM理解这种关系。为了为排名任务选择更有效的演示，Liu 等人。 [164]提出了 DemoRank，一种有效的演示选择框架。

### Page 14

### 段落 141 · Page 14

**EN**

14 Prompt Yes / No Prompt Output (Relevance Generation) (Query Generation) #{query} Output (a) Pointwise method Prompt [2] > [3] > [1] > … Output Prompt Document 1 / Document 2 Output (b) Listwise method (c) Pairwise method [Demonstrations] Document: Tea helps with weight loss… Query: Benefits of tea? Does the document answer the query? Yes [Input] Document: #{document} Query: #{query} Does the document answer the query? [Demonstrations] Please write a query based on this document. Document: Tea helps with weight loss... Query: Benefits of tea? [Input] Please write a query based on this document.

**中文**

14 提示 是/否 提示输出 (相关性生成) (查询生成) #{query} 输出 (a) 逐点法 提示 [2] > [3] > [1] > … 输出 提示文档 1 / 文档 2 输出 (b) 列表法 (c) 成对法 [演示] 文档：茶有助于减肥... 查询：茶的好处？该文档是否回答了查询？是 [输​​入] 文档：#{document} 查询：#{query} 该文档是否回答了查询？ 【演示】请根据该文档写出一个查询。文件：茶有助于减肥...询问：茶的好处？ [输入] 请根据该文档编写一个查询。

### 段落 142 · Page 14

**EN**

Document: #{document} Query: [Demonstrations] The following are documents related to query “Benefits of tea?” [1] Tea helps with weight loss… Rank these documents based on their relevance to the query. [1] > [3] > [2] > … [Input] The following are documents related to query #{query}. [1] #{document_1} [2] … Rank these documents based on their relevance to the query. …… … [Demonstrations] Given a query “Benefits of tea”, which of the following two documents is more relevant to the query?

**中文**

文档：#{document} 查询：[演示] 以下是与查询“茶的好处？”相关的文档[1] 茶有助于减肥……根据这些文档与查询的相关性对这些文档进行排名。 [1] > [3] > [2] > … [输入] 以下是与查询#{query}相关的文档。 [1] #{document_1} [2] ...根据这些文档与查询的相关性对这些文档进行排名。 ………… 【演示】给定一个查询“茶的好处”，以下两个文档中哪一个与该查询更相关？

### 段落 143 · Page 14

**EN**

Document 1: “Tea helps with … ”; Document 2: “Tea is popular …” Output Document 1 or Document 2: Document 1 [Input] Given a query #{query}, which of the following two documents is more relevant to the query? Document 1: #{document_1}; Document 2: #{document_2} Output Document 1 or Document 2:… Fig. 5. Three types of unsupervised reranking methods: (a) pointwise methods that consist of relevance generation (upper) and query generation (lower), (b) listwise methods, and (c) pairwise methods. The “Demonstrations” represents the fewshot demonstrations whose format are same as the current input.

**中文**

文件 1：“茶有助于……”；文档 2：“茶很受欢迎……” 输出 文档 1 或文档 2：文档 1 [输入] 给定一个查询 #{query}，以下两个文档中哪一个与该查询更相关？文档 1：#{document_1}；文档 2：#{document_2} 输出文档 1 或文档 2：… 图 5. 三种无监督重排序方法：(a) 由相关性生成（上）和查询生成（下）组成的点式方法、(b) 列表方法和 (c) 成对方法。 “Demonstrations”代表少数几个演示，其格式与当前输入相同。

### 段落 144 · Page 14

**EN**

The core component of DemoRank is a dependency-aware demonstration reranker, which reranks a list of demonstrations (usually obtained by a demonstration retriever) so that the combination of top-ranked demonstrations can yield better performance. An efficient method is proposed to construct the training samples for such demonstration reranker and a novel list-pairwise training loss is designed for optimization. 5.2.2 Listwise Methods Listwise methods [166, 169] aim to directly rank a list of documents (see Figure 5 (b)).

**中文**

DemoRank 的核心组件是一个依赖项感知演示重排序器，它对演示列表（通常由演示检索器获取）进行重新排序，以便排名靠前的演示的组合可以产生更好的性能。提出了一种有效的方法来构造此类演示重排序器的训练样本，并设计了一种新颖的列表成对训练损失来进行优化。 5.2.2 Listwise 方法 Listwise 方法[166, 169]旨在直接对文档列表进行排序（见图 5 (b)）。

### 段落 145 · Page 14

**EN**

These methods insert the query and a document list into the prompt and instruct the LLMs to output the reranked document identifiers. Due to the limited input length of LLMs, it is not feasible to insert all candidate documents into the prompt. To alleviate this issue, these methods employ a sliding window strategy to rerank a subset of candidate documents each time. This strategy involves ranking from back to front using a sliding window, re-ranking only the documents within the window at a time.

**中文**

这些方法将查询和文档列表插入到提示中，并指示 LLM 输出重新排序的文档标识符。由于LLM的输入长度有限，将所有候选文档插入到提示中是不可行的。为了缓解这个问题，这些方法采用滑动窗口策略每次对候选文档的子集进行重新排序。该策略涉及使用滑动窗口从后到前进行排名，一次仅对窗口内的文档进行重排。

### 段落 146 · Page 14

**EN**

Although listwise methods have yielded promising performance, they still suffer from some weaknesses: (1) The performance of listwise methods is highly sensitive to the document order in the prompt. When the document order is randomly shuffled, listwise methods perform even worse than BM25 [166], revealing positional bias issues in the listwise ranking of LLMs. (2) The use of sliding windows limits the number of documents that can be ranked each time, and the dependency between adjacent windows prevents parallelization of LLM inference, thereby reducing the efficiency of reranking.

**中文**

尽管列表方法已经取得了良好的性能，但它们仍然存在一些弱点：（1）列表方法的性能对提示中的文档顺序高度敏感。当文档顺序随机打乱时，列表方法的表现甚至比 BM25 [166] 更差，揭示了 LLM 列表排名中的位置偏差问题。 （2）滑动窗口的使用限制了每次可以排序的文档数量，并且相邻窗口之间的依赖关系阻碍了LLM推理的并行化，从而降低了重排序的效率。

### 段落 147 · Page 14

**EN**

Recently, some studies have attempted to mitigate these issues. Tang et al. [170] introduce a permutation self-consistency method, which involves shuffling the list in the prompt and aggregating the generated results to achieve a more accurate and a positionally unbiased ranking. Chen et al. [171] introduce a tournament mechanism into listwise ranking and propose TourRank, which parallelizes the reranking process through intelligent grouping and use a tournament-like points system to reduce the impact of the initial document order. Parry et al.

**中文**

最近，一些研究试图缓解这些问题。唐等人。 [170]引入了一种排列自一致性方法，该方法涉及对提示中的列表进行混洗并聚合生成的结果，以实现更准确且位置无偏的排名。陈等人。 [171]将锦标赛机制引入列表排序并提出TourRank，它通过智能分组并行化重新排序过程，并使用类似锦标赛的积分系统来减少初始文档顺序的影响。帕里等人。

### 段落 148 · Page 14

**EN**

[172] propose a parallelizable partitioning algorithm for listwise ranking, which also aims at mitigating efficiency issues. Reddy et al. [194] propose a novel listwise reranking approach which leverages the output logits of the first generated identifier to accelerating reranking process. To optimize the listwise

**中文**

[172]提出了一种用于列表排序的可并行分区算法，该算法也旨在减轻效率问题。雷迪等人。 [194]提出了一种新颖的列表重排序方法，该方法利用第一个生成的标识符的输出逻辑来加速重排序过程。优化列表

### Page 15

### 段落 149 · Page 15

**EN**

15 TABLE 6. The comparison between different LLM-based reranking methods.Ndenotes the number of documents to rerank. The “complexity”, “logits”, and “batch” represent the computational complexity, whether accesses LLM’s logits, and whether allows batch inference respectively.kis the constant in sliding windows strategy. As for the performance, we use NDCG@10 as a metric, and the results are calculated by reranking the top-100 documents retrieved by BM25 on TREC-DL2019 and TREC-DL2020. The best model is in bold while the second-best is underlined. The results come from previous study [174].

**中文**

15 表 6. 不同基于 LLM 的重新排序方法之间的比较。N 表示要重新排序的文档数量。 “complexity”、“logits”、“batch”分别表示计算复杂度、是否访问LLM的logits、是否允许批量推理。ki是滑动窗口策略中的常数。至于性能，我们使用 NDCG@10 作为指标，结果是通过对 TREC-DL2019 和 TREC-DL2020 上 BM25 检索到的前 100 个文档进行重排来计算的。最好的模型以粗体显示，而次佳的模型则带有下划线。结果来自之前的研究[174]。

### 段落 150 · Page 15

**EN**

*Since the parameters of ChatGPT have not been released, its model parameters are based on public estimates [193].

**中文**

*由于ChatGPT的参数尚未公布，其模型参数基于公开估计[193]。

### 段落 151 · Page 15

**EN**

Method LLM Size Properties Performance Complexity Logits Batching TREC-DL19 -DL20 Initial Retriever BM25 - - - - - 50.58 47.96 Supervised monoBERT [12] BERT 340M -✓ ✓70.50 67.28 monoT5 [13] T5 220M -✓ ✓71.48 66.99 RankT5 [151] T5 3B -✓ ✓71.22 69.49 Unsupervised Pointwise Query Generation [160] FLAN-UL2 20BO(N)✓ ✓58.95 60.02 Relevance Generation [157] FLAN-UL2 20BO(N)✓ ✓64.61 65.39 Unsupervised Listwise RankGPT3.5 [166] ChatGPT 154B*O(k∗N)65.80 62.91 RankGPT4 [166] GPT-4 1T*O(k∗N)75.5970.56 Unsupervised Pairwise PRP-Allpair [174] FLAN-UL2 20BO(N 2)✓ ✓72.42 70.68 PRP-Heapsort [174] FLAN-UL2 20BO(N∗logN)✓71.88 69.43 reranking prompt, Jin et al.

**中文**

方法 LLM 大小 属性 性能 复杂性 Logits 批处理 TREC-DL19 -DL20 初始检索器 BM25 - - - - - 50.58 47.96 监督 monoBERT [12] BERT 340M -✓ ✓70.50 67.28 monoT5 [13] T5 220M -✓ ✓71.48 66.99 RankT5 [151] T5 3B -✓ ✓71.22 69.49 无监督逐点查询生成 [160] FLAN-UL2 20BO(N)✓ ✓58.95 60.02 相关性生成 [157] FLAN-UL2 20BO(N)✓ ✓64.61 65.39 无监督列表 RankGPT3.5 [166] ChatGPT 154B*O(k*N)65.80 62.91 RankGPT4 [166] GPT-4 1T*O(k*N)75.5970.56 无监督成对 PRP-全对 [174] FLAN-UL2 20BO(N 2)✓ ✓72.42 70.68 PRP 堆排序 [174] FLAN-UL2 20BO(N*logN)✓71.88 69.43 重排提示，Jin 等人。

### 段落 152 · Page 15

**EN**

[173] propose a novel automatic prompt engineering algorithm APEER, which generates prompts through feedback and preference optimization. Liu et al. [167] comprehensively discuss the benefits of longcontext LLMs for listwise ranking and introduce a novel full reranker which performs better than the sliding window reranker while also being more efficient and having lower API cost. Liu et al. [168] propose a collaborative ranking framework CoRanking which combines small and large listwise rerankers for more efficient and effective passage ranking.

**中文**

[173]提出了一种新颖的自动提示工程算法APEER，它通过反馈和偏好优化来生成提示。刘等人。 [167]全面讨论了长上下文LLM对列表排序的好处，并引入了一种新颖的完整重排序器，其性能比滑动窗口重排序器更好，同时也更高效且具有更低的API成本。刘等人。 [168]提出了一种协作排名框架 CoRanking，它将小型和大型列表重排器结合起来，以实现更高效和有效的段落排名。

### 段落 153 · Page 15

**EN**

They also design a novel passage order adjuster to mitigate the sensitivity of listwise reranker to the input document order. 5.2.3 Pairwise Methods In pairwise methods, LLMs are given a prompt that consists of a query and a document pair (see Figure 5 (c)). Then, they are instructed to generate the identifier of the document with higher relevance. To rerank all candidate documents, aggregation methods like AllPairs are used [174]. AllPairs first generates all possible document pairs, yields discrete judgments for each pair (e.g., Document 1 or Document 2), and aggregates a final relevance score for each document.

**中文**

他们还设计了一种新颖的段落顺序调整器，以减轻列表重排序器对输入文档顺序的敏感性。 5.2.3 成对方法 在成对方法中，LLM 会收到一个由查询和文档对组成的提示（见图 5 (c)）。然后，指示他们生成具有更高相关性的文档的标识符。为了重新排列所有候选文档，使用 AllPairs 等聚合方法[174]。 AllPairs 首先生成所有可能的文档对，对每对（例如文档 1 或文档 2）产生离散判断，并汇总每个文档的最终相关性得分。

### 段落 154 · Page 15

**EN**

Efficient sorting algorithms, such as heap sort and bubble sort, are employed to speed up the ranking process. These sorting algorithms utilize efficient data structures to compare document pairs selectively and elevate the most relevant documents to the top of the ranking list, which is particularly useful in top-kranking. Experimental results show the state-of-the-art performance on the standard benchmarks using moderate-size LLMs (e.g., Flan-UL2 with 20B parameters), which are much smaller than those typically employed in listwise methods (e.g., GPT3.5).

**中文**

采用堆排序和冒泡排序等高效排序算法来加速排序过程。这些排序算法利用高效的数据结构来有选择地比较文档对，并将最相关的文档提升到排名列表的顶部，这在顶级排名中特别有用。实验结果显示，使用中等大小的 LLM（例如，具有 20B 参数的 Flan-UL2）在标准基准上具有最先进的性能，该 LLM 比列表方法中通常采用的那些小得多（例如，GPT3.5）。

### 段落 155 · Page 15

**EN**

Building on the pairwise prompting approach, several ranking method variants have been proposed. Luo et al. [176] introduce an innovative scoring unit that leverages the generation probability of judgments instead of discrete judgments, and further design a graph-based aggregation approach to obtain a final relevance score for each document. Sinhababu et al. [195] and propose to utilize few-shot in-context demonstrations to improve the performance of pairwise ranking. Yan et al. [177] utilize the pairwise comparison as a post-processing step to adjust the relevance scores generated by the pointwise LLM reranker.

**中文**

基于成对提示方法，已经提出了几种排序方法变体。罗等人。 [176]引入了一种创新的评分单元，利用判断的生成概率而不是离散判断，并进一步设计基于图的聚合方法来获得每个文档的最终相关性得分。辛哈巴布等人。 [195]并建议利用少镜头上下文演示来提高成对排名的性能。严等人。 [177]利用成对比较作为后处理步骤来调整逐点LLM重新排序器生成的相关性分数。

### 段落 156 · Page 15

**EN**

Although effective, pairwise methods still suffer from high time complexity. To alleviate the efficiency problem, a setwise approach [175] has been proposed to compare a set of documents at a time and select the most relevant one from them. This approach allows the sorting algorithms (such as heap sort) to compare more than two documents at each step, thereby reducing the total number of comparisons and speeding up the sorting process. 5.2.4 Comparison and Discussion We compare different unsupervised methods from various aspects to better illustrate the strengths and weaknesses of each method, which is summarized in Table 6.

**中文**

尽管有效，但成对方法仍然存在时间复杂度较高的问题。为了缓解效率问题，提出了一种集合方法[175]来一次比较一组文档并从中选择最相关的一个。这种方法允许排序算法（例如堆排序）在每个步骤中比较两个以上的文档，从而减少比较的总数并加快排序过程。 5.2.4 比较与讨论 我们从各个方面比较不同的无监督方法，以更好地说明每种方法的优缺点，总结如表6。

### 段落 157 · Page 15

**EN**

The representative methods [157, 160, 166, 174] in pointwise, listwise, and pairwise ranking, and some supervised methods [12, 13, 151] mentioned in Section 5.1 are selected for performance comparison. The pointwise methods (query generation and relevance generation) judge the relevance of each query-document pair independently, thus offering lower time complexity and enabling batch inference. However, compared to other methods, it does not have an advantage in terms of performance. The listwise method yields significant performance especially when calling GPT-4, but suffers from expensive API cost and non-reproducibility [183].

**中文**

选择点式、列表式和成对排序中的代表性方法[157、160、166、174]以及5.1节中提到的一些监督方法[12、13、151]进行性能比较。逐点方法（查询生成和相关性生成）独立判断每个查询-文档对的相关性，从而提供较低的时间复杂度并实现批量推理。然而，与其他方法相比，它在性能方面并不具有优势。列表方法可以产生显着的性能，特别是在调用 GPT-4 时，但会受到昂贵的 API 成本和不可重复性的影响 [183]​​。

### 段落 158 · Page 15

**EN**

Compared with the listwise method, the pairwise method shows competitive results based on a much smaller model FLAN-UL2 (20B). Stemming from the necessity to compare an extensive number of document pairs, its primary drawback is low efficiency. 5.3 Utilizing LLMs for Training Data Augmentation Furthermore, in the realm of reranking, researchers have explored the integration of LLMs for training data augmen-

**中文**

与列表方法相比，成对方法基于更小的模型 FLAN-UL2 (20B) 显示出有竞争力的结果。由于需要比较大量的文档对，其主要缺点是效率低。 5.3 利用 LLM 进行训练数据增强 此外，在重排领域，研究人员已经探索了 LLM 的集成以增强训练数据。

### Page 16

### 段落 159 · Page 16

**EN**

16 tation [178, 180, 181, 183–185]. For example, ExaRanker [178] and ExaRanker-Open [179] generate explanations for querypassage pairs using GPT-3.5 and open-source LLMs respectively, and subsequently trains a seq2seq ranking model to generate relevance labels along with corresponding explanations. InPars-Light [180] is proposed as a cost-effective method to synthesize queries for documents by prompting LLMs. Askari et al. [181] proposes to generate synthetic documents based on LLMs in response to user queries. Furthermore, Askari et al.

**中文**

16 [178, 180, 181, 183–185]。例如，ExaRanker [178] 和 ExaRanker-Open [179] 分别使用 GPT-3.5 和开源 LLM 生成查询段落对的解释，然后训练 seq2seq 排名模型以生成相关性标签以及相应的解释。 InPars-Light [180] 被提出作为一种经济高效的方法，通过提示 LLM 来合成文档查询。阿斯卡里等人。 [181]建议基于LLM生成合成文档以响应用户查询。此外，阿斯卡里等人。

### 段落 160 · Page 16

**EN**

[182] propose to utilize reinforcement learning to improve the quality of synthetic documents generated by LLMs. Recently, many studies [183–185] have also attempted to distill the document reranking capability of LLMs into a specialized model. RankVicuna [183] proposes to use the ranking list of RankGPT 3.5 [166] as the gold list to train a 7B parameter Vicuna model. RankZephyr [184] introduces a two-stage training strategy for distillation: initially applying the RankVicuna recipe to train Zephyrγin the first stage, and then further finetuning it in the second stage with the ranking results from RankGPT4.

**中文**

[182]建议利用强化学习来提高法学硕士生成的合成文档的质量。最近，许多研究[183-185]也尝试将法学硕士的文档重新排序能力提炼成专门的模型。 RankVicuna [183]​​提出使用RankGPT 3.5 [166]的排名表作为金榜来训练7B参数Vicuna模型。 RankZephyr[184]引入了一种两阶段蒸馏训练策略：首先在第一阶段应用RankVicuna配方训练Zephyrγ，然后在第二阶段根据RankGPT4的排名结果进一步对其进行微调。

### 段落 161 · Page 16

**EN**

These two studies not only demonstrate competitive results but also alleviate the issue of ranking results non-reproducibility of black-box LLMs. Besides, researchers [185] have also tried to distill the ranking ability of a pairwise ranker, which is computationally demanding, into a simpler but more efficient pointwise ranker. 5.4 Reasoning-intensive Rerankers Recent breakthroughs in Large Reasoning Models (LRMs) like DeepSeek-R1 [107] have demonstrated exceptional capabilities across many NLP tasks.

**中文**

这两项研究不仅展示了有竞争力的结果，而且缓解了黑盒法学硕士排名结果不可重复性的问题。此外，研究人员[185]还尝试将计算要求较高的成对排序器的排序能力提炼为更简单但更高效的逐点排序器。 5.4 推理密集型重排序 最近在 DeepSeek-R1 [107] 等大型推理模型 (LRM) 方面取得的突破已经在许多 NLP 任务中展示了卓越的能力。

### 段落 162 · Page 16

**EN**

These models significantly improve the answer accuracy in many complex NLP tasks (e.g., math and coding) through explicit step-by-step reasoning chains during inference. This capability holds particular promise for document reranking, where precise understanding of query intent and cross-document comparison are critical for relevance assessment. Motivated by these advancements, emerging research has explored injecting reasoning ability into document rerankers. For example, Weller et al. [187] and Yang et al. [188] propose to apply DeepSeek-R1 as a teacher model to distill its reasoning process into smaller rerankers. Zhang et al.

**中文**

这些模型通过推理过程中明确的逐步推理链，显着提高了许多复杂 NLP 任务（例如数学和编码）的答案准确性。此功能特别适用于文档重排，其中准确理解查询意图和跨文档比较对于相关性评估至关重要。受这些进步的推动，新兴研究探索将推理能力注入文档重新排序器中。例如，韦勒等人。 [187]和杨等人。 [188]建议应用 DeepSeek-R1 作为教师模型，将其推理过程提炼为更小的重排序器。张等人。

### 段落 163 · Page 16

**EN**

[189] and Zhuang et al. [190] propose to use reinforcement learning algorithm to optimize reranker based on rule-based reward. TFRank [191] introduces a “think-free” pointwise ranker that leverages reasoning during training while eliminating intermediate reasoning steps at inference, significantly improving the reasoning efficiency. While effective, these rerankers are primarily trained on traditional web search data MSMARCO, making them difficult to generalize to many complex and reasoningintensive ranking benchmarks [196]. To address the scarcity of reasoning-intensive training data, Liu et al.

**中文**

[189]和庄等人。 [190]提出使用强化学习算法来优化基于规则的奖励的重排器。 TFRank[191]引入了一种“无思考”的逐点排序器，它在训练期间利用推理，同时消除推理时的中间推理步骤，显着提高推理效率。虽然有效，但这些重排器主要是在传统网络搜索数据 MSMARCO 上进行训练的，这使得它们很难推广到许多复杂且推理密集的排名基准 [196]。为了解决推理密集型训练数据的稀缺问题，Liu 等人。

### 段落 164 · Page 16

**EN**

[186] propose an automated data synthesis framework and generate 13K high-quality reasoning-intensive training data covering diverse search scenarios. They further propose a twostage “SFT+RL” training framework, to empower LLM with strong reasoning and ranking abilities. Their ReasonRank model has achieved state-of-the-art performance on many reasoning-intensive IR benchmarks such as BRIGHT [196] and R2MED [197]. 5.5 Limitations Although recent research on utilizing LLMs for document reranking has made significant progress, it still has some limitations.

**中文**

[186]提出了一种自动化数据合成框架，并生成涵盖不同搜索场景的13K高质量推理密集型训练数据。他们进一步提出了两阶段的“SFT+RL”训练框架，赋予LLM强大的推理和排序能力。他们的 ReasonRank 模型在许多推理密集型 IR 基准测试（例如 BRIGHT [196] 和 R2MED [197]）上取得了最先进的性能。 5.5 局限性 尽管最近关于利用法学硕士进行文档重新排序的研究已经取得了重大进展，但它仍然存在一些局限性。

### 段落 165 · Page 16

**EN**

First, due to the reliance on API calls and a large number of parameters, the process of LLM ranking could be expensive and inefficient. Therefore, achieving a tradeoff between the cost/efficiency and performance of LLMs is a topic worth discussing. Along this line, Rashid et al. [198] propose a budget-aware ranking solution which maximizes the LLM’s performance within a given budget. Notably, Chen et al. [199] introduce in-context re-ranking (ICR), an attention-based method that achieves superior efficiency by eliminating generative overhead through O(1) forward passes. Besides, Meng et al.

**中文**

首先，由于依赖API调用和大量参数，LLM排名过程可能成本高昂且效率低下。因此，实现LLM成本/效率和性能之间的权衡是一个值得讨论的话题。沿着这条线，拉希德等人。 [198]提出了一种预算敏感的排名解决方案，可以在给定的预算内最大化法学硕士的表现。值得注意的是，陈等人。 [199]引入了上下文重排序（ICR），这是一种基于注意力的方法，通过 O(1) 前向传递消除生成开销，从而实现卓越的效率。此外，孟等人。

### 段落 166 · Page 16

**EN**

[200] systematically discuss the improvements in ranking efficiency and effectiveness brought by the rank list truncation technique. Second, while existing studies mainly focus on applying LLMs to opendomain datasets (such as MSMARCO [102]) or relevancebased text ranking tasks, their adaptability to in-domain datasets [120], non-standard ranking datasets [201] and reasoning-intensive datasets [196] remains an area that demands more comprehensive exploration.

**中文**

[200]系统地讨论了排名表截断技术带来的排名效率和有效性的改进。其次，虽然现有的研究主要集中于将LLM应用于开放域数据集（例如MSMARCO [102]）或基于相关性的文本排序任务，但它们对域内数据集[120]、非标准排序数据集[201]和推理密集型数据集[196]的适应性仍然是一个需要更全面探索的领域。

### 段落 167 · Page 16

**EN**

6 READER With the impressive capabilities of LLMs in understanding, extracting, and processing textual data, researchers explore expanding the scope of IR systems beyond content ranking to answer generation. In this evolution, a reader module has been introduced to generate answers based on the document corpus in IR systems. By integrating a reader module, IR systems can directly present conclusive passages to users. Compared with providing a list of documents, users can simply comprehend the answering passages instead of analyzing the ranking list in this new paradigm.

**中文**

6 读者 凭借法学硕士在理解、提取和处理文本数据方面令人印象深刻的能力，研究人员探索将 IR 系统的范围从内容排名扩展到答案生成。在这一演变中，引入了阅读器模块，用于根据 IR 系统中的文档语料库生成答案。通过集成阅读器模块，红外系统可以直接向用户呈现结论性的段落。与提供文档列表相比，在这种新范式中，用户可以简单GEO解答案段落，而不用分析排名列表。

### 段落 168 · Page 16

**EN**

Furthermore, by repeatedly providing documents to LLMs based on their generating texts, the final generated answers can potentially be more accurate and information-rich than the original retrieved lists. A naive strategy for implementing this function is to heuristically provide LLMs with documents relevant to the user queries or the previously generated texts to support the following generation. However, this passive approach limits LLMs to merely collecting documents from IR systems without active engagement. An alternative solution is to train LLMs to interact proactively with search engines.

**中文**

此外，通过根据法学硕士生成的文本向法学硕士重复提供文档，最终生成的答案可能比原始检索到的列表更准确、信息更丰富。实现此功能的一个简单策略是启发式地向法学硕士提供与用户查询或先前生成的文本相关的文档以支持下一代。然而，这种被动的方法限制了法学硕士只能从 IR 系统收集文件，而没有积极参与。另一种解决方案是培训法学硕士主动与搜索引擎交互。

### 段落 169 · Page 16

**EN**

For example, LLMs can formulate their own queries instead of relying solely on user queries or generated texts for references. According to the way LLMs utilize IR systems in the reader module, we can categorize them intopassive readersandactive readers. Each approach has its advantages and challenges for implementing LLM-powered answer generation in IR systems. Furthermore, since the documents provided by upstream IR systems are sometimes too long to directly feed as input for LLMs, some compression modules are proposed to extractively or abstractively compress the

**中文**

例如，法学硕士可以制定自己的查询，而不是仅仅依赖用户查询或生成的文本作为参考。根据法学硕士在阅读器模块中使用红外系统的方式，我们可以将其分为被动阅读器和主动阅读器。在 IR 系统中实施 LLM 支持的答案生成时，每种方法都有其优点和挑战。此外，由于上游 IR 系统提供的文档有时太长而无法直接作为 LLM 的输入，因此提出了一些压缩模块来提取或抽象地压缩

### Page 17

### 段落 170 · Page 17

**EN**

17 TABLE 7. The comparison of existing representative methods that have a passive reader module. REALM and RAG do not use LLMs, but their frameworks have been widely applied in many following approaches. Methods Backbone models Where to incorporate retrieval When to retrieve How to use LLMs REALM [202] BERT Input layer In the beginning Fine-tuning RAG [203] BART Input layer In the beginning Fine-tuning REPLUG [204] GPT Input layer In the beginning Fine-tuning Atlas [205] T5 Input layer In the beginning Fine-tuning Lazaridou et al. [206] Gopher Input layer In the beginning Prompting He et al.

**中文**

17 表 7. 具有无源读取器模块的现有代表性方法的比较。 REALM 和 RAG 不使用 LLM，但它们的框架已广泛应用于以下许多方法中。方法 骨干模型 在哪里合并检索 何时检索 如何使用 LLM REALM [202] BERT 输入层 在开始时微调 RAG [203] BART 输入层 在开始时微调 REPLUG [204] GPT 输入层 在开始时微调 Atlas [205] T5 输入层 在开始时微调 Lazaridou 等人。 [206] Gopher 输入层 开头提示 He 等人。

### 段落 171 · Page 17

**EN**

[207] GPT Input layer In the beginning Prompting Chain-of-Note [208] LLaMA Input layer In the beginning Fine-tuning RALM [209] LLaMA & OPT & GPT Input layer During generation (everyntokens) Prompting RETRO [23] Transformer Attention layer During generation (everyntokens) Training from scratch ITERGEN [210] GPT Input layer During generation (every answer) Prompting IRCoT [211] Flan-T5 & GPT Input layer During generation (every sentence) Prompting FLARE [212] GPT Input layer During generation (aperiodic) Prompting Self-RAG [213] LLaMA Input layer During generation (aperiodic) Fine-tuning retrieved contexts for LLMs to understand and generate answers for queries.

**中文**

[207] GPT 输入层 在开始时提示 Chain-of-Note [208] LLaMA 输入层 在开始时微调 RALM [209] LLaMA & OPT & GPT 输入层 在生成期间（everyntokens）提示 RETRO [23] Transformer 注意层 在生成期间（everyntokens） 从头开始训练 ITERGEN [210] GPT 输入层 在生成期间（每个答案）提示IRCoT [211] Flan-T5 & GPT 输入层 生成期间（每个句子） 提示 FLARE [212] GPT 输入层 生成期间（非周期性）提示 Self-RAG [213] LLaMA 输入层 生成期间（非周期性） 微调检索到的上下文，以便法学硕士理解并生成查询答案。

### 段落 172 · Page 17

**EN**

We will present these reader and compressor modules in the following parts and briefly introduce the existing analysis work on retrieval-augmented generation (RAG) strategy and their applications. 6.1 Passive Reader To generate answers for users, a straightforward strategy is to supply the retrieved documents according to the queries or previously generated texts from IR systems as inputs to LLMs for creating passages [23, 202–207, 209, 211, 212, 214– 218]. By this means, these approaches use the LLMs and IR systems separately, with LLMs functioning as passive recipients of documents from the IR systems.

**中文**

我们将在下面的部分中介绍这些阅读器和压缩器模块，并简要介绍现有的检索增强生成（RAG）策略的分析工作及其应用。 6.1 被动阅读器 为了为用户生成答案，一个简单的策略是根据查询或先前从 IR 系统生成的文本提供检索到的文档，作为 LLM 的输入来创建段落 [23, 202–207, 209, 211, 212, 214–218]。通过这种方式，这些方法分别使用法学硕士和IR系统，法学硕士充当IR系统文档的被动接收者。

### 段落 173 · Page 17

**EN**

The strategies for utilizing LLMs within IR systems’ reader modules can be categorized into the following three groups according to the frequency of retrieving documents for LLMs. 6.1.1 Once-Retrieval Reader To obtain useful references for LLMs to generate responses for user queries, an intuitive way is to retrieve the top documents based on the queries themselves in the beginning. For example, REALM [202] adopts this strategy by directly attending the document contents to the original queries to predict the final answers based on masked language modeling. RAG [203] follows this strategy but applies the generative language modeling paradigm.

**中文**

根据法学硕士检索文档的频率，在 IR 系统阅读器模块中利用法学硕士的策略可以分为以下三组。 6.1.1 一次检索阅读器 为了获得法学硕士生成用户查询响应的有用参考，一种直观的方法是从一开始就根据查询本身来检索顶级文档。例如，REALM [202]采用这种策略，通过直接将文档内容关注到原始查询，以基于掩码语言建模来预测最终答案。 RAG [203]遵循这一策略，但应用了生成语言建模范式。

### 段落 174 · Page 17

**EN**

However, these two approaches only use language models with limited parameters, such as BERT and BART. Recent approaches such as REPLUG [204] and Atlas [205] have improved them by leveraging LLMs such as GPTs, T5s, and LLaMAs for response generation. To yield better answer generation performances, these models usually fine-tune LLMs on QA tasks. However, due to the limited computing resources, many methods [206, 207, 215, 219] choose to prompt LLMs for generation as they could use larger LMs in this way.

**中文**

然而，这两种方法仅使用参数有限的语言模型，例如 BERT 和 BART。 REPLUG [204] 和 Atlas [205] 等最近的方法通过利用 GPT、T5 和 LLaMA 等 LLM 来生成响应，从而改进了它们。为了产生更好的答案生成性能，这些模型通常会针对 QA 任务对 LLM 进行微调。然而，由于计算资源有限，许多方法[206、207、215、219]选择提示LLM生成，因为它们可以通过这种方式使用更大的LM。

### 段落 175 · Page 17

**EN**

Furthermore, to improve the quality of the generated answers, several approaches [208, 220] also try to train or prompt the LLMs to generate contexts such as citations or notes in addition to the answers to force LLMs to understand and assess the relevance of retrieved passages to the user queries. ActiveRAG [221] and PG-RAG [222] improve them by using knowledge construction during the answer generation process. Some approaches [216, 223] evaluate the importance of each retrieved reference using policy gradients to indicate which reference is more useful for generating.

**中文**

此外，为了提高生成答案的质量，几种方法 [208, 220] 还尝试训练或提示法学硕士生成除了答案之外的上下文，例如引文或注释，以迫使法学硕士理解和评估检索到的段落与用户查询的相关性。 ActiveRAG [221] 和 PG-RAG [222] 通过在答案生成过程中使用知识构建来改进它们。一些方法[216, 223]使用策略梯度来评估每个检索到的参考的重要性，以指示哪个参考对于生成更有用。

### 段落 176 · Page 17

**EN**

Specifically, [223] utilize LLMs themselves to provide importance for different references which also supply additional training signals. Besides, researchers explore instruction tuning LLMs such LLaMAs to improve their abilities to generate conclusive passages relying on retrieved knowledge [224–226]. During the training of LLMbased readers, some approaches [227] explore the strategy of contrastive learning by augmenting training data by removing and replacing retrieved passages to improve the generating performances.

**中文**

具体来说，[223]利用LLM本身来提供不同参考的重要性，这些参考也提供额外的训练信号。此外，研究人员探索了 LLM 的教学调整，例如 LLaMA，以提高他们依靠检索到的知识生成结论性段落的能力 [224-226]。在基于 LLM 的读者的训练过程中，一些方法 [227] 通过删除和替换检索到的段落来增强训练数据来探索对比学习策略，以提高生成性能。

### 段落 177 · Page 17

**EN**

Additionally, SPRING [228] inserts several trainable tokens between the retrieved documents and issued questions for better optimization of the reader. R2AG [229] extracts features from retrieval models and attaches them to the reference contents to overcome the semantic gaps between LLMs and retrievers. Yoran et al. [230] also propose to generate noisy training data to help LLMs generate correct answers while irrelevant contents are included in the retrieved contexts. RAAT [231] and ATM [232] further solve the noisy problem by introducing the adversarial training strategy.

**中文**

此外，SPRING [228] 在检索到的文档和发出的问题之间插入了几个可训练的标记，以更好地优化读者。 R2AG [229]从检索模型中提取特征并将其附加到参考内容中，以克服法学硕士和检索器之间的语义差距。约兰等人。 [230]还建议生成噪声训练数据，以帮助法学硕士生成正确的答案，同时检索到的上下文中包含不相关的内容。 RAAT[231]和ATM[232]通过引入对抗性训练策略进一步解决了噪声问题。

### 段落 178 · Page 17

**EN**

6.1.2 Periodic-Retrieval Reader However, while generating long conclusive answers, it is shown [23, 209] that only using the references retrieved by the original user intents as in once-retrieval readers may be inadequate. For example, when providing a passage about “Barack Obama”, language models may need additional knowledge about his university, which may not be included in the results of simply searching the initial query. In conclusion, language models may need extra references to support the following generation during the generating process, where multiple retrieval processes may be required.

**中文**

6.1.2 定期检索阅读器然而，在生成长的结论性答案时，[23, 209]表明仅使用由原始用户意图检索的引用（如在一次检索阅读器中）可能是不够的。例如，当提供有关“Barack Obama”的段落时，语言模型可能需要有关他的大学的额外知识，这些知识可能不会包含在简单搜索初始查询的结果中。总之，语言模型在生成过程中可能需要额外的引用来支持下一代，其中可能需要多个检索过程。

### 段落 179 · Page 17

**EN**

To address this, solutions such as RETRO [23] and RALM [209] have emerged, emphasizing the periodic collection of documents based on both the original queries and the concurrently generated texts (triggering a retrieval everyngenerated tokens). In this manner, when generating the text about the university career of Barack Obama, the LLM can receive additional documents as supplementary materials. This need for additional references highlights the necessity for multiple retrieval iterations to ensure robustness in subsequent answer generation. Notably, RETRO [23] introduces a novel approach incorporating cross-attention

**中文**

为了解决这个问题，出现了 RETRO [23] 和 RALM [209] 等解决方案，强调基于原始查询和同时生成的文本（触发每个生成的标记的检索）定期收集文档。这样，在生成有关巴拉克·奥巴马大学生涯的文本时，法学硕士可以收到额外的文件作为补充材料。对额外参考的需求凸显了多次检索迭代的必要性，以确保后续答案生成的稳健性。值得注意的是，RETRO [23] 引入了一种结合交叉注意力的新颖方法

### Page 18

### 段落 180 · Page 18

**EN**

18 between the generating texts and the references within the Transformer attention calculation, as opposed to directly embedding references into the input texts of LLMs. Since it involves additional cross-attention modules in the Transformer’s structure, RETRO trains this model from scratch. However, these two approaches mainly rely on the successiventokens to separate generation and retrieve documents, which may not be semantically continuous and may cause the collected references noisy and useless.

**中文**

18 在 Transformer 注意力计算中的生成文本和参考文献之间，而不是直接将参考文献嵌入到法学硕士的输入文本中。由于 Transformer 结构中涉及额外的交叉注意力模块，因此 RETRO 从头开始​​训练该模型。然而，这两种方法主要依靠连续的标记来分离文档的生成和检索，这在语义上可能不连续，并且可能导致收集的参考文献有噪声且无用。

### 段落 181 · Page 18

**EN**

To solve this problem, some approaches such as IRCoT [211] also explore retrieving documents for every generated sentence, which is a more complete semantic structure. Furthermore, researchers find that the whole generated passages can be considered as conclusive contexts for current queries and can be used to find more relevant knowledge to generate more thorough answers. Consequently, many recent approaches [210, 233–236] have also tried to extend this periodic-retrieval paradigm to iteratively using the whole generated passages to retrieve references to re-generate the answers, until the iterations reach a pre-defined limitation.

**中文**

为了解决这个问题，IRCoT [211]等一些方法还探索为每个生成的句子检索文档，这是一个更完整的语义结构。此外，研究人员发现，整个生成的段落可以被视为当前查询的结论性上下文，并且可以用于查找更多相关知识以生成更彻底的答案。因此，许多最近的方法 [210, 233–236] 也尝试扩展这种周期性检索范式，以迭代地使用整个生成的段落来检索引用以重新生成答案，直到迭代达到预定义的限制。

### 段落 182 · Page 18

**EN**

Particularly, these methods can be regarded as special periodic-retrieval readers that retrieve passages when every answer is (re)-generated. Since the LLMs can receive more comprehensive and relevant references with the iterations increase, these methods that combine RAG and generationaugmented retrieval strategies can generate more accurate answers but consume more computation costs. 6.1.3 Aperiodic-Retrieval Reader In the above strategy, the retrieval systems supply documents to LLMs in a periodic manner. However, retrieving documents in a mandatory frequency may mismatch the retrieval timing and can be costly.

**中文**

特别是，这些方法可以被视为特殊的周期性检索阅读器，它们在（重新）生成每个答案时检索段落。由于随着迭代次数的增加，法学硕士可以获得更全面、更相关的参考文献，因此这些结合 RAG 和生成增强检索策略的方法可以生成更准确的答案，但会消耗更多的计算成本。 6.1.3 非周期性检索阅读器 在上述策略中，检索系统以周期性方式向法学硕士提供文献。然而，以强制频率检索文档可能与检索时间不匹配并且成本高昂。

### 段落 183 · Page 18

**EN**

Recently, FLARE [212] has addressed this problem by automatically determining the timing of retrieval according to the probability of generating texts. Since the probability can serve as an indicator of LLMs’ confidence during text generation [237, 238], a low probability for a generated term could suggest that LLMs require additional knowledge. Specifically, when the probability of a term falls below a predefined threshold, FLARE employs IR systems to retrieve references in accordance with the ongoing generated sentences, while removing these low-probability terms.

**中文**

最近，FLARE [212]通过根据生成文本的概率自动确定检索时机来解决这个问题。由于概率可以作为法学硕士在文本生成过程中信心的指标[237, 238]，生成术语的低概率可能表明法学硕士需要额外的知识。具体来说，当某个术语的概率低于预定义的阈值时，FLARE 使用 IR 系统根据正在生成的句子检索引用，同时删除这些低概率术语。

### 段落 184 · Page 18

**EN**

FLARE adopts this strategy of prompting LLMs for answer generation solely based on the probabilities of generating terms, avoiding the need for finetuning while still maintaining effectiveness. Besides, self- RAG [213] tends to solve this problem by training LLMs such as LlaMA to generate specific tokens when they need additional knowledge to support following generations. Another critical model is introduced to judge whether the retrieved references are beneficial for generating.

**中文**

FLARE 采用这种策略，提示法学硕士仅根据生成术语的概率来生成答案，避免了微调的需要，同时仍然保持有效性。此外，self-RAG [213] 倾向于通过训练 LlaMA 等 LLM 在需要额外知识来支持后代时生成特定令牌来解决这个问题。引入另一个关键模型来判断检索到的参考是否有利于生成。

### 段落 185 · Page 18

**EN**

We summarize representative passive reader approaches in Table 7, considering various aspects such as the backbone language models, the insertion point for retrieved references, the timing of using retrieval models, and the tuning strategy employed for LLMs. 6.2 Active Reader However, the passive reader-based approaches separate IR systems and generative language models. This signifies that LLMs can only submissively utilize references provided by IR systems and are unable to interactively engage with the IR systems in a manner akin to human interaction such as issuing queries to seek information.

**中文**

我们在表 7 中总结了代表性的被动阅读器方法，考虑了各个方面，例如主干语言模型、检索参考文献的插入点、使用检索模型的时机以及法学硕士采用的调整策略。 6.2 主动阅读器 然而，基于被动阅读器的方法将 IR 系统和生成语言模型分开。这意味着法学硕士只能顺从地利用 IR 系统提供的参考，而无法以类似于人类交互的方式与 IR 系统交互，例如发出查询来寻求信息。

### 段落 186 · Page 18

**EN**

To allow LLMs to actively use search engines, Self- Ask [239], DSP [240], and PlanRAG [241] try to employ fewshot prompts for LLMs, triggering them to search queries when they believe it is required. For example, in a scenario where the query is“When was the existing tallest wooden lattice tower built?”, these prompted LLMs can decide to search a query“What is the existing tallest wooden lattice tower”to gather necessary references as they find the query cannot be directly answered.

**中文**

为了允许法学硕士积极使用搜索引擎，SelfAsk [239]、DSP [240] 和 PlanRAG [241] 尝试为法学硕士使用少镜头提示，在他们认为需要时触发他们搜索查询。例如，在查询“现有最高的木格子塔何时建成？”的场景中，这些提示的法学硕士可以决定搜索查询“现有最高的木格子塔是什么”，以收集必要的参考资料，因为他们发现查询无法直接回答。

### 段落 187 · Page 18

**EN**

Once acquired information about the tower, they can iteratively query IR systems for more details until they determine to generate the final answers instead of asking questions. To alleviate the problem of insufficient manually annotated data for fine-tuning, LPKG [242] constructs high-quality active retrieval-augmented reasoning paths from existing knowledge graphs. Notably, these methods involve IR systems to construct a single reasoning chain for LLMs. MRC [243] further improves these methods by prompting LLMs to explore multiple reasoning chains and subsequently combining all generated answers using LLMs.

**中文**

一旦获得有关塔的信息，他们就可以迭代查询红外系统以获取更多详细信息，直到他们决定生成最终答案而不是提出问题。为了缓解用于微调的手动注释数据不足的问题，LPKG [242]从现有知识图谱构建了高质量的主动检索增强推理路径。值得注意的是，这些方法涉及 IR 系统来为法学硕士构建单一推理链。 MRC [243] 通过提示法学硕士探索多个推理链并随后使用法学硕士组合所有生成的答案，进一步改进了这些方法。

### 段落 188 · Page 18

**EN**

6.3 Compressor Existing LLMs, especially open-sourced ones, such as LLaMA and Flan-T5, have limited input lengths (usually 4,096 or 8,192 tokens). However, the documents or web pages retrieved by upstream IR systems are usually long. Therefore, it is difficult to concatenate all the retrieved documents and feed them into LLMs to generate answers. Though some approaches manage to solve these problems by aggregating the answers supported by each reference as the final answers, this strategy neglects the potential relations between retrieved passages.

**中文**

6.3 压缩器 现有的LLM，尤其是开源的LLM，例如LLaMA 和Flan-T5，输入长度有限（通常为4,096 或8,192 个令牌）。然而，上游IR系统检索到的文档或网页通常很长。因此，很难将所有检索到的文档连接起来并将其输入 LLM 中以生成答案。尽管一些方法设法通过将每个参考文献支持的答案聚合为最终答案来解决这些问题，但这种策略忽略了检索到的段落之间的潜在关系。

### 段落 189 · Page 18

**EN**

A more straightforward way is to directly compress the retrieved documents into short input tokens or even dense vectors [244–250]. To compress the retrieved references, an intuitive idea is to extract the most usefulKsentences from the retrieved documents. LeanContext [244] applies this method and trains a small model by reinforcement learning (RL) to select the topKsimilar sentences to the queries. The researchers also augment this strategy by using a free open-sourced text reduction method for the rest sentences as a supplement.

**中文**

一种更直接的方法是直接将检索到的文档压缩为短输入标记甚至密集向量[244-250]。为了压缩检索到的参考文献，一个直观的想法是从检索到的文档中提取最有用的句子。 LeanContext [244]应用这种方法并通过强化学习（RL）训练一个小模型来选择与查询最相似的句子。研究人员还通过对其余句子使用免费的开源文本缩减方法作为补充来增强这一策略。

### 段落 190 · Page 18

**EN**

Instead of using RL-based methods, RECOMP [245] directly uses the probability or the match ratio of the generated answers to the golden answers as signals to build training datasets and tune the compressor model. For example, the sentence corresponding to the highest generating probability is the positive one while others are negative ones.

**中文**

RECOMP [245]没有使用基于强化学习的方法，而是直接使用生成的答案与黄金答案的概率或匹配比作为信号来构建训练数据集并调整压缩器模型。例如，生成概率最高的句子为正句子，其他句子为负句子。

### 段落 191 · Page 18

**EN**

Furthermore, FILCO [246] applies the “hindsight” methods, which directly align the prior distribution (the predicted importance probability distribution of sentences without knowing the gold answer) to the posterior distribution (the same distribution of sentences within knowing the gold answer) to tune language models to select sentences. However, these extractive methods may lose potential intent among all references. Therefore, abstractive methods are proposed to summarize retrieved documents into short but concise summaries for downstream generation. These

**中文**

此外，FILCO [246]应用“后见之明”方法，直接将先验分布（在不知道黄金答案的情况下预测句子的重要性概率分布）与后验分布（在知道黄金答案的情况下句子的相同分布）进行调整来调整语言模型来选择句子。然而，这些提取方法可能会失去所有参考文献中的潜在意图。因此，提出了抽象方法将检索到的文档总结为简短而简洁的摘要，以供下游生成。这些

### Page 19

### 段落 192 · Page 19

**EN**

19 methods [245, 247] usually distill the summarizing abilities of LLMs to small models. For example, TCRA [247] leverages GPT-3.5-turbo to build abstractive compression datasets for MT5 model. Recently, xRAG [249] proposes to use a freeze sentence encoder and tunes a projector to comprise retrieved passage into a dense vector. 6.4 Analysis With the rapid development of the above reader approaches, many researchers have begun to analyze the characteristics of retrieval-augmented LLMs: •Liu et al. [251] find that the position of the relevant/golden reference has significant influences on the final generation performance.

**中文**

19 种方法 [245, 247] 通常将法学硕士的总结能力提炼成小模型。例如，TCRA [247] 利用 GPT-3.5-turbo 为 MT5 模型构建抽象压缩数据集。最近，xRAG [249] 提出使用冻结句子编码器并调整投影仪以将检索到的段落组成密集向量。 6.4 分析 随着上述阅读器方法的快速发展，许多研究人员开始分析检索增强法学硕士的特征： [251]发现相关/黄金参考的位置对最终生成性能有显着影响。

### 段落 193 · Page 19

**EN**

The performance is always better when the relevant reference is at the beginning or the end, which indicates the necessity of introducing a ranking module to order the retrieved knowledge. •Ren et al. [252] observe that by applying retrieval augmentation generation strategy, LLMs can have a better awareness of their knowledge boundaries. •Liu et al. [253] analyze different strategies of integrating retrieval systems and LLMs such as concatenate (i.e., concatenating all references for answer generation) and post fusion (i.e., aggregating the answers corresponding to each reference).

**中文**

当相关参考文献位于开头或结尾时，性能总是更好，这表明有必要引入排序模块来对检索到的知识进行排序。 •任等人。 [252]观察到，通过应用检索增强生成策略，法学硕士可以更好地了解其知识边界。 •刘等人。 [253]分析了集成检索系统和法学硕士的不同策略，例如连接（即连接所有参考文献以生成答案）和后融合（即聚合与每个参考文献相对应的答案）。

### 段落 194 · Page 19

**EN**

They also explore several ways of combining these two strategies. •Aksitov et al. [254] demonstrate that there exists an attribution and fluency tradeoff for retrieval-augmented LLMs: with more received references, the attribution of generated answers increases while the fluency decreases. •Mallen et al. [255] argue that always retrieving references to support LLMs to generate answers hurts the question-answering performance. The reason is that LLMs themselves may have adequate knowledge while answering questions about popular entities and the retrieved noisy passages may interfere and bias the answering process.

**中文**

他们还探索了结合这两种策略的几种方法。 •阿克西托夫等人。 [254]证明检索增强法学硕士存在归因和流畅性权衡：随着收到的参考文献越多，生成答案的归因增加，而流畅性下降。 •马伦等人。 [255] 认为总是检索参考文献来支持法学硕士生成答案会损害问答性能。原因是法学硕士本身在回答有关热门实体的问题时可能拥有足够的知识，而检索到的嘈杂段落可能会干扰和偏差回答过程。

### 段落 195 · Page 19

**EN**

To overcome this challenge, they devise a simple strategy that only retrieves references while the popularity of entities in the query is quite low. By this means, the efficacy and efficiency of RAG both improve. Ding et al. [256] pay attention to the same phenomenon and propose to paraphrase several perturbed questions for LLMs to answer according to their internal knowledge and perform a consistency check to decide whether to retrieve external information. [257–259] also focus on this problem using triplets extracted from the knowledge graph and the confidence of LLMs.

**中文**

为了克服这一挑战，他们设计了一种简单的策略，仅检索引用，而查询中实体的流行度相当低。通过这种方式，RAG的功效和效率都得到提高。丁等人。 [256]关注相同的现象，并建议转述几个受扰动的问题，让法学硕士根据其内部知识回答，并进行一致性检查以决定是否检索外部信息。 [257-259]也使用从知识图谱中提取的三元组和法学硕士的置信度来关注这个问题。

### 段落 196 · Page 19

**EN**

[260, 261] solve this problem by training LLMs or small language models to judge whether the questions are known by LLMs. •Jin et al. [262] analyze the impacts of knowledge conflict among retrieved references and LLM’s internal knowledge. and find that LLMs follow the majority rule while facing this phenomenon. •Cho et al. [263], Xue et al. [264], and Chaudhari et al. [265] explore the attacking technique towards LLM-based retrieval augmented generation by poisoning retrieved passages. They find that even introducing some typos in the references may also affect the answer generation. •Wang et al.

**中文**

[260, 261]通过训练LLM或小语言模型来判断问题是否被LLM知道来解决这个问题。 •金等人。 [262]分析检索到的参考文献和法学硕士内部知识之间知识冲突的影响。并发现法学硕士在面对这种现象时遵循多数原则。 •Cho等人。 [263]，薛等人。 [264]和Chaudhari等人。 [265]通过毒害检索到的段落探索对基于LLM的检索增强生成的攻击技术。他们发现，即使在参考文献中引入一些拼写错误也可能会影响答案的生成。 •王等人。

### 段落 197 · Page 19

**EN**

[266] construct an in-domain reader evaluation dataset. They deeply analyze the effectiveness of the retrieval augmented generation paradigm under the longtail and in-domain situations. •Cuconasu et al. [267] compare the performances between readers based on base LLMs and “instructed” LLMs. Different from previous popular belief, They find base models outperform their corresponding instruction-tuned versions. 6.5 Applications Recently, researchers [268–274] have applied the RAG strategy to areas such as clinical QA, medical QA, and financial QA to enhance LLMs with external knowledge and to develop domain-specific applications.

**中文**

[266]构建域内读者评估数据集。他们深入分析了长尾和域内情况下检索增强生成范式的有效性。 •Cuconasu 等人。 [267]比较基于基础法学硕士和“指导”法学硕士的读者之间的表现。与之前流行的看法不同，他们发现基础模型的性能优于相应的指令调整版本。 6.5 应用最近，研究人员[268-274]已将RAG策略应用于临床QA、医学QA和财务QA等领域，以利用外部知识增强法学硕士并开发特定领域的应用程序。

### 段落 198 · Page 19

**EN**

For example, ATLANTIC [269] adapts Atlas to the scientific domain to derive a science QA system. Besides, some approaches [275] also apply techniques in federated learning such as multiparty computation to perform personal RAG with privacy protection. Furthermore, to better facilitate the deployment of these RAG systems, some tools or frameworks are proposed [214, 276, 277]. For example, RETA-LLM [214] breaks down the whole complex generation task into several simple modules in the reader pipeline.

**中文**

例如，ATLANTIC [269] 将 Atlas 应用于科学领域，从而衍生出科学 QA 系统。此外，一些方法[275]还应用联邦学习中的技术，例如多方计算来执行具有隐私保护的个人RAG。此外，为了更好地促进这些 RAG 系统的部署，提出了一些工具或框架[214,276,277]。例如，RETA-LLM [214] 将整个复杂的生成任务分解为读取器管道中的几个简单模块。

### 段落 199 · Page 19

**EN**

These modules include a query rewriter module for refining query intents, a passage extraction module for aligning reference lengths with LLM limitations, and a fact verification module for confirming the absence of fabricated information in the generated answers. Jin et al. [278] release the FlashRAG toolkit for the reproduction and development of RAG research, which includes 32 pre-processed benchmark datasets and 14 state-of-the-art algorithms. 6.6 Limitations Several IR systems applying the RAG strategy, such as New Bing and Langchain, have already entered commercial use.

**中文**

这些模块包括用于细化查询意图的查询重写器模块、用于根据 LLM 限制调整参考长度的段落提取模块，以及用于确认生成的答案中不存在捏造信息的事实验证模块。金等人。 [278]发布了用于再现和开发 RAG 研究的 FlashRAG 工具包，其中包括 32 个预处理的基准数据集和 14 个最先进的算法。 6.6 局限性 New Bing、Langchain 等采用 RAG 策略的 IR 系统已经投入商用。

### 段落 200 · Page 19

**EN**

However, there are also some challenges in this novel retrieval-augmented content generation system. These include challenges such as effective query reformulation, optimal retrieval frequency, correct document comprehension, accurate passage extraction, and effective content summarization. It is crucial to address these challenges to effectively realize the potential of LLMs in this paradigm. 7 SEARCHAGENT The emergence of large reasoning models (LRMs) has ushered in a new era for IR systems, with a growing focus on developing LRM-based intelligent agents.

**中文**

然而，这种新颖的检索增强内容生成系统也存在一些挑战。其中包括有效的查询重构、最佳检索频率、正确的文档理解、准确的段落提取和有效的内容摘要等挑战。解决这些挑战对于有效发挥法学硕士在此范式中的潜力至关重要。 7 SEARCHAGENT 大型推理模型（LRM）的出现开创了 IR 系统的新时代，人们越来越关注开发基于 LRM 的智能代理。

### 段落 201 · Page 19

**EN**

This paradigm shift seeks to replicate human-like reasoning and retrieval processes, thereby augmenting the capacity of LLM-powered IR models to tackle complex, real-world problems. Leveraging their advanced natural language understanding, reasoning, and generation capabilities, these agents can autonomously search, interpret, and synthesize information from diverse sources. Initial research in this domain focused on static pipelinebased architectures, where an information-seeking task is broken down into a series of modules, each with a predefined role [279–285].

**中文**

这种范式转变旨在复制类人推理和检索过程，从而增强法学硕士支持的 IR 模型解决复杂的现实问题的能力。利用其先进的自然语言理解、推理和生成能力，这些代理可以自主搜索、解释和合成来自不同来源的信息。该领域的初步研究集中在基于静态管道的架构，其中信息查找任务被分解为一系列模块，每个模块都有一个预定义的角色[279​​-285]。

### 段落 202 · Page 19

**EN**

While these systems demonstrate a foundational approach, their fixed workflows limit their ability to adapt to the dynamic and complex interactions inherent in real-world scenarios. This inflexibility constrains

**中文**

虽然这些系统展示了一种基本方法，但它们固定的工作流程限制了它们适应现实场景中固有的动态和复杂交互的能力。这种不灵活性限制了

### Page 20

### 段落 203 · Page 20

**EN**

20 their overall performance and hinders their effectiveness in advanced reasoning and problem-solving. Recently, the development of LRMs has enabled the development of a new class of autonomous search agents. These agents move beyond static pipelines by allowing the LLM to actively and dynamically explore the web. This is achieved by enabling the model to decide its next action based on real-time feedback from the environment or humans. This shift towards flexible, self-guided behavior makes these agents more adaptable and more closely aligned with human-like problem-solving.

**中文**

20 他们的整体表现并阻碍了他们高级推理和解决问题的效率。最近，LRM 的发展使得新型自主搜索代理的开发成为可能。这些代理超越了静态管道，允许法学硕士主动、动态地探索网络。这是通过使模型能够根据环境或人类的实时反馈来决定下一步行动来实现的。这种向灵活、自我引导行为的转变使这些智能体的适应性更强，并且更接近于像人类一样解决问题。

### 段落 204 · Page 20

**EN**

In this section, we will comprehensively introduce the studies about search agents from the following four aspects: (1) architecture of search agents, (2) information seeking module, (3) optimization of search agents, and (4) benchmarks and resources. 7.1 Architecture of Search Agent The design of a search agent’s architecture is a foundational step that establishes its core operational mechanism. Existing approaches can be broadly categorized into two main paradigms:single-agent frameworksandmulti-agent frameworks.

**中文**

在本节中，我们将从以下四个方面全面介绍搜索代理的研究：（1）搜索代理的体系结构，（2）信息查找模块，（3）搜索代理的优化，（4）基准和资源。 7.1 搜索Agent的架构 搜索Agent的架构设计是建立其核心运行机制的基础步骤。现有的方法可以大致分为两个主要范例：单代理框架和多代理框架。

### 段落 205 · Page 20

**EN**

A single-agent framework utilizes a single LLM to handle all aspects of the task, including reasoning, interaction, and answer generation. In contrast, a multi-agent framework distributes these responsibilities among multiple LLMs, which act as collaborative agents to achieve the target. 7.1.1 Single-Agent Frameworks In a single-agent framework, a single LLM with strong reasoning capabilities serves as the central decision-maker and task executor. This LLM dynamically determines the next action based on the current information state and environmental context, managing the entire reasoning and interaction process.

**中文**

单代理框架利用单个 LLM 来处理任务的所有方面，包括推理、交互和答案生成。相比之下，多代理框架将这些职责分配给多个法学硕士，这些法学硕士充当协作代理来实现目标。 7.1.1 单代理框架 在单代理框架中，具有强大推理能力的单个LLM充当中央决策者和任务执行者。该LLM根据当前信息状态和环境上下文动态确定下一步行动，管理整个推理和交互过程。

### 段落 206 · Page 20

**EN**

For example, Search-R1 [286] and Re- Search [287] adopt a ReAct-style mechanism, enabling the LLM policy to automatically generate actions such as “think”, “search”, and “answer”. This allows the agent to iteratively interact with search tools to resolve complex multi-hop questions. To optimize the performance of these single-agent systems, researchers have employed various reinforcement learning (RL) techniques. The GRPO algorithm [288] has been commonly utilized to enhance performance. In a more refined approach, R1-Searcher [289] introduces a two-stage GRPO-based RL optimization.

**中文**

例如，Search-R1[286]和Re-Search[287]采用ReAct式的机制，使LLM策略能够自动生成“思考”、“搜索”和“回答”等动作。这允许代理与搜索工具迭代交互，以解决复杂的多跳问题。为了优化这些单代理系统的性能，研究人员采用了各种强化学习（RL）技术。 GRPO 算法[288]已被广泛用于增强性能。在更精细的方法中，R1-Searcher [289] 引入了基于 GRPO 的两阶段 RL 优化。

### 段落 207 · Page 20

**EN**

The first stage assigns rewards based on retrieval frequency and output format correctness, while the second stage rewards answer accuracy and the final output format. To further improve reasoning and exploration, Li et al. [290] propose START, which introduces a hint-infer mechanism that manually inserts hint strings during inference. This encourages the LLM to self-reflect and make better use of external tools. They also design Hint-RFT, a method that performs rejection sampling and revises reasoning trajectories to support the supervised fine-tuning of search agents.

**中文**

第一阶段根据检索频率和输出格式正确性分配奖励，第二阶段奖励答案准确性和最终输出格式。为了进一步提高推理和探索，Li 等人。 [290]提出了START，它引入了一种提示推断机制，可以在推断过程中手动插入提示字符串。这鼓励法学硕士自我反思并更好地利用外部工具。他们还设计了 Hint-RFT，这是一种执行拒绝采样并修改推理轨迹以支持搜索代理的监督微调的方法。

### 段落 208 · Page 20

**EN**

More recently, Atom-Searcher [291] has been proposed to decompose the holistic “thinking” process into several finer-grained “atomthinking” actions. These actions are guided by reasoning reward models, which provide precise feedback on reasoning trajectories, going beyond simple outcome-based rewards. The main advantage of the single-agent framework lies in its simplicity, as it can be trained end-to-end via RL. This allows researchers to explore the reasoning limits of a single model using carefully designed optimization algorithms.

**中文**

最近，Atom-Searcher [291]被提议将整体“思考”过程分解为几个更细粒度的“原子思考”动作。这些行动由推理奖励模型指导，该模型提供推理轨迹的精确反馈，超越了简单的基于结果的奖励。单代理框架的主要优点在于其简单性，因为它可以通过 RL 进行端到端训练。这使得研究人员能够使用精心设计的优化算法来探索单个模型的推理极限。

### 段落 209 · Page 20

**EN**

However, a single agent often struggles with highly complex queries that require extensive tool use and long-context reasoning. To address this limitation, multi-agent frameworks have been explored, where multiple agents collaborate to complete complex search and reasoning tasks. 7.1.2 Multi-Agent Frameworks Multi-agent frameworks utilize multiple, specialized LLMs that collaborate to complete complex search and reasoning tasks. This approach enables a division of labor, where each agent focuses on a distinct function, leading to improved system effectiveness and efficiency.

**中文**

然而，单个代理通常会难以处理高度复杂的查询，这些查询需要大量的工具使用和长上下文推理。为了解决这个限制，人们探索了多代理框架，其中多个代理协作完成复杂的搜索和推理任务。 7.1.2 多代理框架 多代理框架利用多个专门的 LLM 协作完成复杂的搜索和推理任务。这种方法实现了劳动分工，每个代理专注于不同的功能，从而提高系统的有效性和效率。

### 段落 210 · Page 20

**EN**

For example, KwaiAgents [292] separates reasoning and summarization into two distinct agents. The reasoning agent is equipped with capabilities such as query understanding, external documents referencing, memory management, and task execution via a hybrid search–browse toolkit. Similarly, Mei et al. [293] propose decoupling the search agent into a search planner and a generator, with optimization efforts primarily on the planner. Building on this, MindSearch [294] introduces a multi-agent framework inspired by human cognitive processes for web retrieval. Its architecture consists of aWeb- Plannerand multipleWebSearchers.

**中文**

例如，KwaiAgents [292]将推理和总结分离为两个不同的代理。推理代理配备了查询理解、外部文档引用、内存管理和通过混合搜索浏览工具包执行任务等功能。同样，梅等人。 [293]建议将搜索代理解耦为搜索规划器和生成器，主要针对规划器进行优化。在此基础上，MindSearch [294] 引入了一个受人类网络检索认知过程启发的多代理框架。其体系结构由一个Web Planner 和多个Web Searchers 组成。

### 段落 211 · Page 20

**EN**

The WebPlanner acts as a high-level controller, decomposing user queries into atomic sub-questions and designing the reasoning process. The WebSearchers then perform hierarchical retrieval over the web, guided by these sub-questions. By employing a coarse-to-fine selection strategy, they efficiently filter valuable information from a large pool of web pages, thereby alleviating the information overload that often hinders LLMs. Alita [295] advances this idea by incorporating self-evolving capabilities through a dynamic MCP box.

**中文**

WebPlanner 充当高级控制器，将用户查询分解为原子子问题并设计推理过程。然后，网络搜索者在这些子问题的指导下通过网络执行分层检索。通过采用从粗到细的选择策略，他们可以有效地从大量网页中过滤出有价值的信息，从而减轻经常阻碍法学硕士的信息过载。 Alita [295] 通过动态 MCP 盒整合自我进化功能，推进了这一想法。

### 段落 212 · Page 20

**EN**

Its manager agent handles central task planning and MCP brainstorming, deciding whether to generate new MCP tools for emerging tasks. The web agent, in turn, is responsible for browsing and retrieving external information. Similarly, OWL [296] further decouples central planning and task execution to improve generalization across different domains. OWL consists of a domain-agnostic planner agent for high-level task decomposition, a coordinator agent for managing task assignments and dependencies, and a set of specialized agents with domain-specific toolkits that execute subtasks and report results.

**中文**

其管理代理负责处理中心任务规划和 MCP 集思广益，决定是否为新出现的任务生成新的 MCP 工具。反过来，网络代理负责浏览和检索外部信息。类似地，OWL [296]进一步解耦中央规划和任务执行，以提高跨不同领域的泛化能力。 OWL 由用于高级任务分解的与域无关的规划器代理、用于管理任务分配和依赖性的协调器代理以及一组具有执行子任务和报告结果的特定于域的工具包的专用代理组成。

### 段落 213 · Page 20

**EN**

This modular design allows researchers to focus optimization efforts on the planner, enhancing its adaptability while minimizing training complexity for other components. The primary advantage of the multi-agent framework is that it allows individual agents to specialize in distinct tasks, enhancing overall system effectiveness and efficiency. However, it introduces challenges in jointly optimizing multiple agents through RL. Current approaches often limit optimization to the core planner agent, which plays the most critical role in coordinating the framework.

**中文**

这种模块化设计使研究人员能够将优化工作集中在规划器上，增强其适应性，同时最大限度地减少其他组件的训练复杂性。多代理框架的主要优点是它允许各个代理专门从事不同的任务，从而提高整体系统的有效性和效率。然而，它给通过强化学习联合优化多个智能体带来了挑战。当前的方法通常将优化限制在核心规划器代理上，而核心规划器代理在协调框架中起着最关键的作用。

### 段落 214 · Page 20

**EN**

Therefore, developing more stable and efficient RL strategies for multiagent search systems remains a promising direction for future research.

**中文**

因此，为多智能体搜索系统开发更稳定、更高效的强化学习策略仍然是未来研究的一个有前途的方向。

### Page 21

### 段落 215 · Page 21

**EN**

21 7.2 Information Seeking Module To handle atomic queries or complete sub-tasks from an upstream planner, a search agent typically relies on an information-seeking module that locates, collects, and synthesizes relevant information. These approaches can be roughly categorized into two types: API-based and browsing-based methods. API-based methods use search engine APIs to retrieve information, while browsing-based methods construct sandboxes or virtual environments that enable agents to simulate human-like web interactions.

**中文**

21 7.2 信息查找模块 为了处理原子查询或完成来自上游规划器的子任务，搜索代理通常依赖于定位、收集和综合相关信息的信息查找模块。这些方法大致可以分为两类：基于 API 的方法和基于浏览的方法。基于 API 的方法使用搜索引擎 API 来检索信息，而基于浏览的方法则构建沙箱或虚拟环境，使代理能够模拟类人的 Web 交互。

### 段落 216 · Page 21

**EN**

7.2.1 API-based Information Seeking The most straightforward information-seeking strategy is to leverage search engine and scientific database APIs as external tools. Many commercial applications, such as Gemini DeepResearch and Grok DeepSearch, 7 rely on APIs like Google Search, Bing Search, and X Search to access external knowledge. In the research community, Cognitive Kernel- Pro [297] uses the free DuckDuckGo search interface to create a fully open-source pipeline, while CoSearch-Agent [298] integrates SerpApi for real-time search within Slack-based environments.

**中文**

7.2.1 基于API 的信息检索 最直接的信息检索策略是利用搜索引擎和科学数据库API 作为外部工具。许多商业应用程序（例如 Gemini DeepResearch 和 Grok DeepSearch）7 依赖 Google 搜索、Bing 搜索和 X 搜索等 API 来访问外部知识。在研究社区中，Cognitive Kernel-Pro [297] 使用免费的 DuckDuckGo 搜索接口来创建完全开源的管道，而 CoSearch-Agent [298] 集成了 SerpApi，以便在基于 Slack 的环境中进行实时搜索。

### 段落 217 · Page 21

**EN**

Beyond basic search APIs, other systems incorporate specialized APIs to refine the retrieval process. For example, Search-o1 [299] and Agent Laboratory [300] use Jina Reader API to extract and refine web passages for downstream reasoning, and the arXiv API to obtain academic metadata. Similarly, AI Scientist [301] employs the Semantic Scholar API to verify citation relationships. While simple and accessible, API-based approaches often struggle with complex, dynamic content rendered by JavaScript, interactive components, or information gated behind authentication.

**中文**

除了基本的搜索 API 之外，其他系统还包含专门的 API 来改进检索过程。例如，Search-o1 [299]和Agent Laboratory [300]使用Jina Reader API来提取和提炼网络段落以进行下游推理，并使用arXiv API来获取学术元数据。类似地，AI Scientist [301] 使用 Semantic Sc​​holar API 来验证引用关系。虽然简单且易于访问，但基于 API 的方法常常难以应对由 JavaScript、交互式组件或身份验证背后的信息呈现的复杂动态内容。

### 段落 218 · Page 21

**EN**

7.2.2 Browsing-based Information Seeking In contrast to API-based methods, browsing-based information-seeking approaches provide search agents with interactive environments that simulate human-web interactions. For example, Manus AI’s browsing agent creates a sandboxed Chromium instance for each subtask, 8 while AutoGLM 9 sequentially opens web pages, reads content, and generates refined reports. In research, AutoAgent [302] uses the BrowserGym environment to perform scrolling and interaction with webpage components.

**中文**

7.2.2 基于浏览的信息搜索 与基于 API 的方法相比，基于浏览的信息搜索方法为搜索代理提供了模拟人机交互的交互环境。例如，Manus AI 的浏览代理为每个子任务创建一个沙盒 Chromium 实例 8，而 AutoGLM 9 则依次打开网页、读取内容并生成精致的报告。在研究中，AutoAgent [302]使用BrowserGym环境来执行滚动以及与网页组件的交互。

### 段落 219 · Page 21

**EN**

SimpleDeepSearcher [303] and Tool-star [304] further compress retrieved content from both browsing and API-based extraction to generate condensed references for answer generation. While browsing-based approaches are better suited for retrieving real-time and deeply nested content, they typically incur higher latency and resource costs. To address the high costs associated with real search APIs, some recent works explore alternative approaches. For example, ZeroSearch [305] trains LLMs to simulate search engine behavior without making actual API calls, thereby significantly reducing training costs.

**中文**

SimpleDeepSearcher [303] 和 Tool-star [304] 进一步压缩从浏览和基于 API 的提取中检索到的内容，以生成用于答案生成的压缩参考。虽然基于浏览的方法更适合检索实时和深度嵌套的内容，但它们通常会产生更高的延迟和资源成本。为了解决与实际搜索 API 相关的高成本问题，最近的一些工作探索了替代方法。例如，ZeroSearch [305] 训练 LLM 来模拟搜索引擎行为，而无需进行实际的 API 调用，从而显着降低了培训成本。

### 段落 220 · Page 21

**EN**

Additionally, some methods, such as Alita [295], propose to dynamically create new MCP tools during the agent’s reasoning process, enabling a 7. Gemini DeepResearch: https://gemini.google/overview/ deep-research/, Grok DeepSearch: https://x.ai/news/grok-3 8. Manus AI: https://manus.im/ 9. AutoGLM: https://autoglm-research.zhipuai.cn/ self-evolving capability that reduces reliance on pre-defined toolkits and further optimizes computation costs. 7.3 Optimization To transform general-purpose LLMs into specialized search agents, researchers have explored various optimization and fine-tuning methods.

**中文**

此外，一些方法，例如 Alita [295]，建议在智能体推理过程中动态创建新的 MCP 工具，从而实现 7. Gemini DeepResearch：https://gemini.google/overview/deep-research/，Grok DeepSearch：https://x.ai/news/grok-3 8. Manus AI：https://manus.im/ 9. AutoGLM：https://autoglm-research.zhipuai.cn/自我进化能力可减少对预定义工具包的依赖并进一步优化计算成本。 7.3 优化 为了将通用的法学硕士转变为专门的搜索代理，研究人员探索了各种优化和微调方法。

### 段落 221 · Page 21

**EN**

These approaches aim to internalize advanced search skills, such as planning, reasoning, and tool usage into the model’s parametric knowledge. The ultimate goal is to enable agents to perform exploratory information acquisition. Based on the progressive levels of search capabilities, this section categorizes mainstream agent tuning methods into three paradigms: strategic retrieval optimization, iterative search tuning, and autonomous open-web search. 7.3.1 Strategic Retrieval Optimization In basic search scenarios, agents must first learn when to retrieve information and how to formulate high-quality queries.

**中文**

这些方法旨在将高级搜索技能（例如规划、推理和工具使用）内化到模型的参数知识中。最终目标是使智能体能够执行探索性信息获取。根据搜索能力的递进水平，本节将主流代理调优方法分为三种范式：策略检索优化、迭代搜索调优和自主开放网络搜索。 7.3.1 策略检索优化 在基本搜索场景中，代理必须首先学习何时检索信息以及如何制定高质量的查询。

### 段落 222 · Page 21

**EN**

Early RAG methods typically follow a fixed and passive pipeline: given a question, the system directly performs a search and then generates an answer based on the results. This approach is often inefficient, as it can lead to redundant searches and struggles to handle irrelevant information. Recent studies have introduced strategic retrieval optimization techniques that enable agents to explicitly model retrieval decisions, thereby balancing search costs against the potential benefit of new information.

**中文**

早期的 RAG 方法通常遵循固定且被动的流程：给定一个问题，系统直接执行搜索，然后根据结果生成答案。这种方法通常效率低下，因为它可能导致冗余搜索并难以处理不相关的信息。最近的研究引入了策略检索优化技术，使代理能够明确地对检索决策进行建模，从而平衡搜索成本与新信息的潜在收益。

### 段落 223 · Page 21

**EN**

For example, Open-RAG [306] proposes a “hybrid adaptive retrieval” mechanism that learns to generate specific tokens to control its retrieval behavior. This work also introduces a constructive learning paradigm, which actively injects distracting information into training data to enhance the model’s robustness and discrimination capabilities against noisy or irrelevant search results. Similarly, DeepRAG [307] models retrieval decisions as a Markov decision process, using imitation learning to train models to weigh the benefits of relying on internal knowledge versus performing an external search at each reasoning step.

**中文**

例如，Open-RAG [306]提出了一种“混合自适应检索”机制，该机制学习生成特定的令牌来控制其检索行为。这项工作还引入了一种建设性学习范式，该范式主动将分散注意力的信息注入训练数据中，以增强模型的鲁棒性和对噪声或不相关搜索结果的辨别能力。类似地，DeepRAG [307] 将检索决策建模为马尔可夫决策过程，使用模仿学习来训练模型，以权衡依赖内部知识与在每个推理步骤执行外部搜索的好处。

### 段落 224 · Page 21

**EN**

This provide the model with the dynamic ability to decide when to retrieve. ATLAS [308] takes a different approach by applying gradient backpropagation only on “critical steps” within expert trajectories. In search tasks, these steps correspond to key decisions such as initiating a search or formulating a core query. By focusing the training signal on these strategic points, this method improves the agent’s core decisionmaking and generalization ability. 7.3.2 Iterative Retrieval Tuning For complex tasks that cannot be solved with a single retrieval, search agents require multi-step reasoning and iterative information acquisition.

**中文**

这为模型提供了决定何时检索的动态能力。 ATLAS [308] 采用了不同的方法，仅在专家轨迹内的“关键步骤”上应用梯度反向传播。在搜索任务中，这些步骤对应于关键决策，例如启动搜索或制定核心查询。通过将训练信号集中在这些战略点上，该方法提高了智能体的核心决策和泛化能力。 7.3.2 迭代检索调优 对于单次检索无法解决的复杂任务，搜索代理需要多步推理和迭代信息获取。

### 段落 225 · Page 21

**EN**

These capabilities are crucial for applications such as multi-hop question answering and open-domain problem solving, where agents must converge on an answer through a dynamic cycle of “think-searchintegrate-rethink”. Research in this area has leveraged both supervised and reinforcement learning paradigms. Supervised learning trains models by providing expert trajectories that include all intermediate reasoning and retrieval steps. CoRAG [309] exemplifies this approach by

**中文**

这些功能对于多跳问答和开放域问题解决等应用至关重要，在这些应用中，智能体必须通过“思考-搜索-整合-重新思考”的动态循环来汇聚答案。该领域的研究利用了监督学习和强化学习范式。监督学习通过提供包括所有中间推理和检索步骤的专家轨迹来训练模型。 CoRAG [309] 通过以下方式举例说明了这种方法

### Page 22

### 段落 226 · Page 22

**EN**

22 automatically generating retrieval chains with intermediate sub-queries and sub-answers for existing datasets. Through rejection sampling, it enables models to explicitly learn multi-step retrieval patterns. Similarly, Auto-RAG [310] focuses on synthesizing instruction data that contains retrieval decision processes, allowing models to master autonomous multi-round retrieval logic through SFT. Reinforcement learning allows agents to autonomously explore and learn optimal dynamic search strategies through interaction with an environment.

**中文**

22 自动生成带有现有数据集的中间子查询和子答案的检索链。通过拒绝采样，它使模型能够显式地学习多步骤检索模式。类似地，Auto-RAG [310]专注于合成包含检索决策过程的指令数据，允许模型通过 SFT 掌握自主多轮检索逻辑。强化学习允许智能体通过与环境的交互来自主探索和学习最佳的动态搜索策略。

### 段落 227 · Page 22

**EN**

Works such as ReSearch [287], R1-Searcher [289], and Search-R1 [286] all adopt RL frameworks, defining search as a learnable action within the reasoning process. Agents learn when and how to intersperse search queries by maximizing rewards from task success. Among these, R1-Searcher designs a twostage RL training pipeline that effectively decouples the objectives of learning to use tools from learning to solve problems with tools. At the algorithmic level, ARPO [311] optimizes training efficiency for iterative agents by proposing an entropy-based adaptive exploration mechanism.

**中文**

ReSearch [287]、R1-Searcher [289] 和 Search-R1 [286] 等作品都采用了 RL 框架，将搜索定义为推理过程中的可学习动作。代理通过最大化任务成功的奖励来学习何时以及如何散布搜索查询。其中，R1-Searcher 设计了一个两阶段的强化学习训练流程，有效地将学习使用工具的目标与学习使用工具解决问题的目标分开。在算法层面，ARPO[311]通过提出基于熵的自适应探索机制来优化迭代代理的训练效率。

### 段落 228 · Page 22

**EN**

This method increases exploration intensity at critical decision points where models show high uncertainty, significantly reducing training costs. 7.3.3 Autonomous Open-Web Search At the highest level, search agents must be able to operate autonomously within open and dynamic web environments. This capability requires models to handle complex challenges such as noisy data, conflicting information from multiple sources, and a lack of explicit supervision. To succeed, they must possess advanced skills in information planning, cross-validation, and multimodal understanding.

**中文**

该方法增加了模型表现出高度不确定性的关键决策点的探索强度，从而显着降低了培训成本。 7.3.3 自主开放网络搜索 在最高级别，搜索代理必须能够在开放和动态网络环境中自主运行。这种能力要求模型能够处理复杂的挑战，例如噪声数据、来自多个来源的冲突信息以及缺乏明确的监督。为了取得成功，他们必须拥有信息规划、交叉验证和多模式理解方面的高级技能。

### 段落 229 · Page 22

**EN**

Recent studies show that end-to-end RL is an effective path for endowing models with autonomous research capabilities. WebAgent-R1 [312] and DeepResearcher [313] use sparse reward training in real browser environments, enabling agents to autonomously plan search paths, verify information, and integrate knowledge from various sources. WebThinker [314] proposes an “Think-Search-and-Draft” strategy, using iterative online direct preference optimization (DPO) to enable agents to seamlessly switch between information collection, reasoning, and content generation. Subsequent research has focused on building more systematic training methodologies.

**中文**

最近的研究表明，端到端强化学习是赋予模型自主研究能力的有效途径。 WebAgent-R1 [312] 和 DeepResearcher [313] 在真实的浏览器环境中使用稀疏奖励训练，使代理能够自主规划搜索路径、验证信息并整合来自各种来源的知识。 WebThinker [314]提出了一种“思考-搜索-草稿”策略，使用迭代在线直接偏好优化（DPO）使代理能够在信息收集、推理和内容生成之间无缝切换。随后的研究重点是建立更系统的培训方法。

### 段落 230 · Page 22

**EN**

Works such as Web- Dancer [315], WebSailor [316], and WebShaper [317] demonstrate that a combination of high-quality data synthesis and hybrid training strategies is an effective path for training advanced agents. These works have made important innovations at the data level. For example, WebShaper proposes a “formalization-driven” data synthesis framework that generates logically consistent data from a task’s reasoning structure.

**中文**

WebDancer [315]、WebSailor [316] 和 WebShaper [317] 等作品表明，高质量数据合成和混合训练策略的结合是训练高级智能体的有效途径。这些工作在数据层面做出了重要创新。例如，WebShaper 提出了一种“形式化驱动”的数据合成框架，该框架可以根据任务的推理结构生成逻辑一致的数据。

### 段落 231 · Page 22

**EN**

WebWatcher [318] further advances this filed by incorporating visual information during training, enabling models to understand and utilize both images and texts on web pages, thereby moving toward human-like research capabilities. Through these methods, search agents are gradually evolving into research-oriented agents capable of autonomous exploration and information integration on the open web. 7.4 Benchmarks and Resources To effectively evaluate and advance search agents, a diverse set of benchmarks and resources is essential.

**中文**

WebWatcher [318] 通过在训练过程中结合视觉信息，使模型能够理解和利用网页上的图像和文本，从而进一步发展这一领域，从而向类似人类的研究能力迈进。通过这些方法，搜索代理逐渐演变为能够在开放网络上自主探索和信息集成的研究型代理。 7.4 基准和资源 为了有效地评估和推进搜索代理，一套多样化的基准和资源是必不可少的。

### 段落 232 · Page 22

**EN**

Current evaluation methodologies can be broadly categorized into two main paradigms: QA-style benchmarks, which assess the agent’s ability to answer complex questions, and taskoriented benchmarks, which measure its capacity for planning, tool use, and environmental interaction. Additionally, a growing number of agent platforms and datasets serve as valuable resources for both evaluation and model training. 7.4.1 QA Benchmarks QA benchmarks are designed to evaluate problem-solving and reasoning capabilities of search agents. They range from simple factual recall to multi-hop reasoning and expert-level challenges.

**中文**

当前的评估方法可大致分为两个主要范例：QA 式基准，评估智能体回答复杂问题的能力；以及面向任务的基准，衡量其规划、工具使用和环境交互的能力。此外，越来越多的代理平台和数据集可作为评估和模型训练的宝贵资源。 7.4.1 QA 基准 QA 基准旨在评估搜索代理解决问题和推理的能力。它们的范围从简单的事实回忆到多跳推理和专家级挑战。

### 段落 233 · Page 22

**EN**

Single-hop QA.It involves questions that can be answered by retrieving information from a single document or source. These benchmarks, such as TriviaQA [319], SimpleQA [320], PopQA [321], and Natural Questions (NQ) [103], primarily test a model’s ability to perform open-domain factual retrieval and reading comprehension. For example, NQ provides anonymized Google search queries paired with human-annotated answers and Wikipedia evidence. Multi-hop QA.It requires models to reason over and combine information from multiple sources to find the answer. A typical multi-hop QA dataset is HotpotQA [322].

**中文**

单跳 QA。它涉及可以通过从单个文档或来源检索信息来回答的问题。这些基准测试，例如 TriviaQA [319]、SimpleQA [320]、PopQA [321] 和 Natural Questions (NQ) [103]，主要测试模型执行开放域事实检索和阅读理解的能力。例如，NQ 提供匿名的 Google 搜索查询以及人工注释的答案和维基百科证据。多跳问答。它需要模型推理并组合来自多个来源的信息来找到答案。典型的多跳 QA 数据集是 HotpotQA [322]。

### 段落 234 · Page 22

**EN**

It focuses on multi-hop reasoning by providing questions that require chaining evidence across multiple Wikipedia pages. 2WikiMultiHopQA [323] extends this by mixing structured knowledge and unstructured text and providing explicit reasoning paths for a more fine-grained evaluation of multistep inference. Expert-level Challenges.They are designed to be extremely difficult, often requiring deep domain knowledge and complex reasoning to push the limits of advanced models. Humanity’s Last Exam (HLE) [324] assembles thousands of hard, expert-crafted questions to stress test models across broad domains.

**中文**

它通过提供需要跨多个维基百科页面链接证据的问题来专注于多跳推理。 2WikiMultiHopQA [323] 通过混合结构化知识和非结构化文本并为多步推理的更细粒度评估提供显式推理路径来扩展这一点。专家级挑战。它们被设计得极其困难，通常需要深厚的领域知识和复杂的推理来突破高级模型的极限。 Humanity’s Last Exam (HLE) [324] 汇集了数千个专家精心设计的难题，以对广泛领域的模型进行压力测试。

### 段落 235 · Page 22

**EN**

Benchmarks like BrowseComp [325] attempt to force genuine web-based retrieval by filtering out items solvable from parametric memory. However, even with these efforts, top-performing systems can still exploit internal knowledge, which may overstate their true research capability. 7.4.2 Task-oriented Benchmarks Task-oriented benchmarks assess an agent’s practical skills in planning, tool use, and interaction with various environments. General Assistant Workflows.GAIA [326], Assistant- Bench [327], and Magnetic-One [328] cover broad assistant tasks that require planning across dialogue, retrieval, and simple tool calls.

**中文**

像 BrowseComp [325] 这样的基准试图通过过滤掉参数内存中可解决的项目来强制进行真正的基于网络的检索。然而，即使做出这些努力，性能最佳的系统仍然可以利用内部知识，这可能夸大了它们真正的研究能力。 7.4.2 面向任务的基准 面向任务的基准评估智能体在规划、工具使用以及与各种环境交互方面的实际技能。一般助理工作流程。GAIA [326]、Assistant- Bench [327] 和 Magnetic-One [328] 涵盖了需要跨对话、检索和简单工具调用进行规划的广泛助理任务。

### 段落 236 · Page 22

**EN**

GAIA, for instance, measures an agent’s end-to-end task management, while Magnetic-One emphasizes robustness across diverse domains and chained subtasks. Code and Research.SWE-bench [329], HumanEvalFix [330], MLE-bench [331], and MLAgentBench [332] probe pipelines

**中文**

例如，GAIA 衡量代理的端到端任务管理，而 Magnetic-One 则强调跨不同领域和链式子任务的稳健性。 Code and Research.SWE-bench [329]、HumanEvalFix [330]、MLE-bench [331] 和 MLAgentBench [332] 探测管道

### Page 23

### 段落 237 · Page 23

**EN**

23 centered on software engineering and research. They require agents to perform tasks like code implementation, debugging, experiment setup, and hyperparameter tuning. Multi-Agent Coordination.RE-Bench [333] and RE- SEARCHTOWN [334] stress multi-agent collaboration, role assignment, and iterative refinement on shared research goals. GUI Control.WebArena [335] and SpaBench [336] extend evaluation to include direct interface manipulation, measuring an agent’s ability to control web UIs or simulated devices and handle noisy, stateful environments.

**中文**

23 以软件工程和研究为中心。它们需要代理执行代码实现、调试、实验设置和超参数调整等任务。多智能体协调。RE-Bench [333] 和 RESEARCHTOWN [334] 强调多智能体协作、角色分配和共同研究目标的迭代细化。 GUI Control.WebArena [335] 和 SpaBench [336] 将评估扩展到包括直接界面操作，测量代理控制 Web UI 或模拟设备以及处理嘈杂、有状态环境的能力。

### 段落 238 · Page 23

**EN**

7.4.3 Agent Datasets and Platforms Beyond static benchmarks, several projects offer comprehensive resources that bundle evaluation suites with datageneration pipelines and agent toolkits. These resources serve as both benchmarks and valuable training corpora for agent research. The Alibaba-NLP WebAgent repository is a notable example, packaging a web-traversal benchmark (WebWalkerQA [337]) with agent models and data tools (Web- Dancer [315], WebShaper [317], and WebSailor [316]).

**中文**

7.4.3 代理数据集和平台 除了静态基准之外，多个项目还提供将评估套件与数据生成管道和代理工具包捆绑在一起的综合资源。这些资源既可以作为代理研究的基准，也可以作为有价值的培训语料库。阿里巴巴-NLP WebAgent 存储库是一个著名的例子，它将网络遍历基准（WebWalkerQA [337]）与代理模型和数据工具（WebDancer [315]、WebShaper [317] 和 WebSailor [316]）打包在一起。

### 段落 239 · Page 23

**EN**

Specifically, WebWalkerQA [337] probes an agent’s ability to traverse sites and extract evidence across multiple subpages, emphasizing structured navigation over single-turn retrieval. WebDancer [315] implements a four-stage training paradigm and releases both models and browsing trajectories, enabling reproducible, end-to-end evaluation. Web- Shaper [317] provides a “formalization-driven” data synthesis pipeline that systematically generates informationseeking instances, making it valuable for cold-starting agents and for studying data-centric training strategies.

**中文**

具体来说，WebWalkerQA [337] 探测代理遍历站点并跨多个子页面提取证据的能力，强调结构化导航而不是单轮检索。 WebDancer [315] 实现了四阶段训练范例并发布了模型和浏览轨迹，从而实现了可重复的端到端评估。 WebShaper [317] 提供了一个“形式化驱动”的数据合成管道，可以系统地生成信息搜索实例，这对于冷启动代理和研究以数据为中心的训练策略很有价值。

### 段落 240 · Page 23

**EN**

The recent model releases from WebSailor [316] demonstrate how post-training and specialized agent tuning can yield stronger navigation and planning behaviors on these benchmarks. 8 FUTUREDIRECTION In this survey, we comprehensively reviewed recent advancements in LLM-enhanced IR systems and discussed their limitations. Since the integration of LLMs into IR systems is still in its early stages, there are still many opportunities and challenges. In this section, we summarize the potential future directions in terms of the four modules in an IR system we just discussed, namely query rewriter, retriever, reranker, and reader.

**中文**

WebSailor [316] 最近发布的模型展示了训练后和专门的代理调整如何在这些基准上产生更强大的导航和规划行为。 8 未来方向 在本次调查中，我们全面回顾了法学硕士增强型 IR 系统的最新进展，并讨论了它们的局限性。由于法学硕士与IR系统的整合仍处于早期阶段，因此仍然存在许多机遇和挑战。在本节中，我们根据刚刚讨论的 IR 系统中的四个模块（即查询重写器、检索器、重排序器和读取器）总结了未来的潜在方向。

### 段落 241 · Page 23

**EN**

In addition, as evaluation has also emerged as an important aspect, we will also introduce the corresponding research problems that need to be addressed in the future. Another discussion about important research topics on applying LLMs to IR can be found in a recent perspective paper [50]. 8.1 Query Rewriter LLMs have enhanced query rewriter for both ad-hoc and conversational search scenarios. Most of the existing methods rely on prompting LLMs to generate new queries. While yielding remarkable results, the refinement of rewriting quality and the exploration of potential application scenarios require further investigation.

**中文**

此外，由于评价也成为一个重要的方面，我们也会介绍相应的未来需要解决的研究问题。关于将法学硕士应用于 IR 的重要研究主题的另一个讨论可以在最近的一篇观点论文中找到 [50]。 8.1 查询重写器 法学硕士已针对即席搜索和对话式搜索场景增强了查询重写器。大多数现有方法依赖于提示法学硕士生成新的查询。在取得显着成果的同时，重写质量的细化和潜在应用场景的探索还需要进一步研究。

### 段落 242 · Page 23

**EN**

•Rewriting queries according to ranking performance.A typical paradigm of prompting-based methods is providing LLMs with several ground-truth rewriting cases (optional) and the task description of query rewriter. Despite LLMs being capable of identifying potential user intents of the query [338], they lack awareness of the resulting retrieval quality of the rewritten query. The absence of this connection can result in rewritten queries that seem correct yet produce unsatisfactory ranking results.

**中文**

•根据排名表现重写查询。基于提示的方法的典型范例是为法学硕士提供几个真实的重写案例（可选）以及查询重写器的任务描述。尽管法学硕士能够识别查询的潜在用户意图[338]，但他们缺乏对重写查询的检索质量的认识。缺少此连接可能会导致重写的查询看似正确，但产生的排名结果却不尽如人意。

### 段落 243 · Page 23

**EN**

Although some existing studies have used reinforcement learning to adjust the query rewriter process according to generation results [80], a substantial realm of research remains unexplored concerning the integration of ranking results. •Improving query rewriter in conversational search.As yet, primary efforts have been made to improve query rewriter in ad-hoc search. In contrast, conversational search presents a more developed landscape with a broader scope for LLMs to contribute to query understanding.

**中文**

尽管一些现有的研究已经使用强化学习根据生成结果调整查询重写过程[80]，但关于排名结果的整合仍有大量研究领域尚未探索。 •改进对话式搜索中的查询重写器。到目前为止，主要工作是改进即席搜索中的查询重写器。相比之下，对话式搜索呈现出更发达的前景，为法学硕士提供了更广泛的查询理解贡献范围。

### 段落 244 · Page 23

**EN**

By incorporating historical interactive information, LLMs can adapt system responses based on user preferences, providing a more effective conversational experience. However, this potential has not been explored in depth. In addition, LLMs could also be used to simulate user behavior in conversational search scenarios, providing more training data, which are urgently needed in current research. •Achieving personalized query rewriter.LLMs offer valuable contributions to personalized search through their capacity to analyze user-specific data.

**中文**

通过整合历史交互信息，法学硕士可以根据用户偏好调整系统响应，从而提供更有效的对话体验。然而，这种潜力尚未得到深入开发。此外，LLM还可以用于模拟会话搜索场景中的用户行为，提供更多的训练数据，这是当前研究迫切需要的。 •实现个性化查询重写器。法学硕士通过其分析用户特定数据的能力为个性化搜索做出了宝贵的贡献。

### 段落 245 · Page 23

**EN**

In terms of query rewriter, with the excellent language comprehension ability of LLMs, it is possible to leverage them to build user profiles based on users’ search histories (e.g., issued queries, clickthrough behaviors, and dwell time). This empowers the achievement of personalized query rewriter for enhanced IR and finally benefits personalized search or personalized recommendation. 8.2 Retriever Leveraging LLMs to improve retrieval models has received considerable attention, promising an enhanced understanding of queries and documents for improved ranking performance.

**中文**

在查询重写器方面，凭借法学硕士出色的语言理解能力，可以利用它们根据用户的搜索历史（例如发出的查询、点击行为和停留时间）构建用户档案。这使得能够实现个性化查询重写器以增强IR，并最终有利于个性化搜索或个性化推荐。 8.2 检索器 利用法学硕士来改进检索模型已受到相当多的关注，有望增强对查询和文档的理解，从而提高排名性能。

### 段落 246 · Page 23

**EN**

However, despite strides in this field, several challenges and limitations still need to be investigated in the future: •Reducing the latency of LLM-based retrievers.LLMs, with their massive parameters and world knowledge, often entail high latency during the inferring process. This delay poses a significant challenge for practical applications of LLM-based retrievers, as search engines require in-time responses. To address this issue, promising research directions include transferring the capabilities of LLMs to smaller models, exploring quantization techniques for LLMs in IR tasks, and so on.

**中文**

然而，尽管这一领域取得了长足的进步，但未来仍需要研究一些挑战和限制： •减少基于LLM的检索器的延迟。LLM具有大量参数和世界知识，在推理过程中通常会带来很高的延迟。这种延迟对基于 LLM 的检索器的实际应用提出了重大挑战，因为搜索引擎需要及时响应。为了解决这个问题，有前景的研究方向包括将 LLM 的能力转移到更小的模型，探索 IR 任务中 LLM 的量化技术等等。

### 段落 247 · Page 23

**EN**

•Simulating realistic queries for data augmentation.Since the high latency of LLMs usually blocks their online application for retrieval tasks, many existing studies have leveraged LLMs to augment training data, which is insensitive to inference latency. Existing methods that leverage LLMs for data augmentation often generate queries without aligning them with real user queries, leading to noise in the training data and limiting the effectiveness of retrievers. As a consequence, exploring techniques such as reinforcement learning

**中文**

•模拟数据增强的实际查询。由于LLM的高延迟通常会阻碍其在线应用检索任务，因此许多现有研究利用LLM来增强训练数据，这对推理延迟不敏感。利用 LLM 进行数据增强的现有方法通常会生成查询，而不将其与真实用户查询对齐，从而导致训练数据中出现噪音并限制检索器的有效性。因此，探索强化学习等技术

### Page 24

### 段落 248 · Page 24

**EN**

24 to enable LLMs to simulate the way that real queries are issued holds the potential for improving retrieval tasks. •Incremental indexing for generative retrieval.As elaborated in Section 4.2.2, the emergence of LLMs has paved the way for generative retrievers to generate document identifiers for retrieval tasks. This approach encodes document indexes and knowledge into the LLM parameters. However, the static nature of LLM parameters, coupled with the expensive fine-tuning costs, poses challenges for updating document indexes in generative retrievers when new documents are added.

**中文**

24 使法学硕士能够模拟实际查询的发出方式，具有改进检索任务的潜力。 • 用于生成检索的增量索引。正如第 4.2.2 节所述，LLM 的出现为生成检索器为检索任务生成文档标识符铺平了道路。这种方法将文档索引和知识编码到 LLM 参数中。然而，LLM 参数的静态性质，加上昂贵的微调成本，给添加新文档时更新生成检索器中的文档索引带来了挑战。

### 段落 249 · Page 24

**EN**

Therefore, it is crucial to explore methods for constructing an incremental index that allows for efficient updates in LLM-based generative retrievers. •Supporting multi-modal search.Web pages usually contain multi-modal information, including texts, images, audios, and videos. However, existing LLM-enhanced IR systems mainly support retrieval for text-based content. A straightforward solution is to replace the backbone with multi-modal large models, such as GPT-4 [339]. However, this undoubtedly increases the cost of deployment.

**中文**

因此，探索构建增量索引的方法至关重要，该索引允许在基于 LLM 的生成检索器中进行有效更新。 •支持多模态搜索。网页通常包含多模态信息，包括文本、图像、音频和视频。然而，现有的法学硕士增强型红外系统主要支持基于文本内容的检索。一个简单的解决方案是用多模态大型模型替换主干网，例如 GPT-4 [339]。然而，这无疑增加了部署成本。

### 段落 250 · Page 24

**EN**

A promising yet challenging direction is to combine the language understanding capability of LLMs with existing multi-modal retrieval models. By this means, LLMs can contribute their language skills in handling different types of content. 8.3 Reranker In Section 5, we have discussed the recent advanced techniques of utilizing LLMs for the reranking task. Some potential future directions in reranking are discussed as follows. •Enhancing the online availability of LLMs.Though effective, many LLMs have a massive number of parameters, making it challenging to deploy them in online applications.

**中文**

一个有前途但具有挑战性的方向是将法学硕士的语言理解能力与现有的多模态检索模型相结合。通过这种方式，法学硕士可以在处理不同类型的内容时贡献他们的语言技能。 8.3 重排器 在第 5 节中，我们讨论了利用 LLM 进行重排任务的最新先进技术。重排的一些潜在的未来方向讨论如下。 • 增强法学硕士的在线可用性。虽然许多法学硕士有效，但它们具有大量参数，这使得将它们部署到在线应用程序中具有挑战性。

### 段落 251 · Page 24

**EN**

Besides, many reranking methods [166, 169] rely on calling LLM APIs, incurring considerable costs. Consequently, devising effective approaches (such as distilling to small models) to enhance the online applicability of LLMs emerges as a research direction worth exploring. •Improving personalized search.Many existing LLM-based reranking methods mainly focus on the ad-hoc reranking task. However, by incorporating user-specific information, LLMs can also improve the effectiveness of the personalized reranking task.

**中文**

此外，许多重排方法[166, 169]依赖于调用LLM API，会产生相当大的成本。因此，设计有效的方法（例如提炼成小模型）来增强法学硕士的在线适用性成为一个值得探索的研究方向。 •改进个性化搜索。许多现有的基于LLM的重排序方法主要集中在ad-hoc重排序任务上。然而，通过合并用户特定的信息，法学硕士还可以提高个性化重排任务的有效性。

### 段落 252 · Page 24

**EN**

For example, by analyzing users’ search history, LLMs can construct accurate user profiles and rerank the search results accordingly, providing personalized results with higher user satisfaction. •Adapting to diverse ranking tasks.In addition to document reranking, there are also other ranking tasks, such as response ranking, evidence ranking, entity ranking and etc., which also belong to the universal information access system. Navigating LLMs towards adeptness in these diverse ranking tasks can be achieved through specialized methodologies, such as instruction tuning.

**中文**

例如，通过分析用户的搜索历史，法学硕士可以构建准确的用户档案，并对搜索结果进行相应的重新排序，从而提供具有更高用户满意度的个性化结果。 •适应多样化的排序任务。除了文档重排序之外，还有其他排序任务，如响应排序、证据排序、实体排序等，也属于通用信息访问系统。可以通过专门的方法（例如指令调整）来引导法学硕士熟练地完成这些不同的排名任务。

### 段落 253 · Page 24

**EN**

Exploring this avenue holds promise as an intriguing and valuable research trajectory. 8.4 Reader With the increasing capabilities of LLMs, the future interaction between users and IR systems will be significantly changed. Due to the powerful natural language processing and understanding capabilities of LLMs, the traditional search paradigm of providing ranking results is expected to be progressively replaced by synthesizing conclusive answering passages for user queries using the reader module.

**中文**

探索这一途径有望成为一条有趣且有价值的研究轨迹。 8.4 Reader 随着法学硕士能力的不断增强，未来用户与IR系统之间的交互将发生显着变化。由于法学硕士强大的自然语言处理和理解能力，提供排名结果的传统搜索范式预计将逐步被使用阅读器模块针对用户查询合成结论性答案段落所取代。

### 段落 254 · Page 24

**EN**

Although such strategies have already been investigated by academia and facilitated by industry as we stated in Section 6, there still exists much room for exploration. •Improving the reference quality for LLMs.To support answer generation, existing approaches usually directly feed the retrieved documents to the LLMs as references. However, since a document usually covers many topics, some passages in it may be irrelevant to the user queries and can introduce noise during LLMs’ generation.

**中文**

尽管正如我们在第 6 节中所述，学术界已经对此类策略进行了研究并得到了工业界的推动，但仍然存在很大的探索空间。 •提高法学硕士的参考质量。为了支持答案生成，现有方法通常直接将检索到的文档提供给法学硕士作为参考。然而，由于文档通常涵盖许多主题，其中的某些段落可能与用户查询无关，并且可能在 LLM 的生成过程中引入噪音。

### 段落 255 · Page 24

**EN**

Therefore, it is necessary to explore techniques for extracting relevant snippets from retrieved documents, enhancing the performance of retrieval-augmented generation. •Improving the answer reliability of LLMs.Incorporating the retrieved references has significantly alleviated the “hallucination” problem of LLMs. However, it remains uncertain whether the LLMs refer to these supported materials during answering queries. Some studies [252] have revealed that LLMs can still provide unfaithful answers even with additional references.

**中文**

因此，有必要探索从检索文档中提取相关片段的技术，提高检索增强生成的性能。 •提高LLM答案的可靠性。结合检索到的参考文献，显着缓解了LLM的“幻觉”问题。然而，目前还不确定法学硕士在回答查询时是否参考了这些支持的材料。一些研究[252]表明，即使有额外的参考资料，法学硕士仍然可以提供不忠实的答案。

### 段落 256 · Page 24

**EN**

Therefore, the reliability of the conclusive answers might be lower compared to the ranking results provided by traditional IR systems. It is essential to investigate the influence of these references on the generation process, thereby improving the credibility of reader-based novel IR systems. 8.5 Search Agent With the outstanding performance of LLMs, the patterns of searching may completely change from traditional IR systems to autonomous search agents. In Section 7, we have discussed many existing works that utilize a static or dynamic pipeline to autonomously browse the web.

**中文**

因此，与传统 IR 系统提供的排名结果相比，结论性答案的可靠性可能较低。有必要研究这些参考文献对生成过程的影响，从而提高基于读者的新型信息检索系统的可信度。 8.5 搜索代理 由于法学硕士的出色性能，搜索模式可能会完全从传统的IR系统转变为自主搜索代理。在第 7 节中，我们讨论了许多利用静态或动态管道自主浏览网络的现有作品。

### 段落 257 · Page 24

**EN**

These works are believed to be the pioneering works of the new searching paradigm. However, there is still plenty of room for further improvements. •Enhancing the Trustworthiness of LLMs.When LLMs are enabled to browse the web, it is important to ensure the validity of retrieved documents. Otherwise, the unfaithful information may increase the LLMs’ hallucination problem. Besides, even if the gathered information has high quality, it remains unclear whether they are really used for synthesizing responses. A potential strategy to address this issue is enabling LLMs to autonomously validate the documents they scrape.

**中文**

这些作品被认为是新搜索范式的开创性作品。然而，仍有很大的进一步改进的空间。 •增强法学硕士的可信度。当法学硕士能够浏览网络时，确保检索到的文档的有效性非常重要。否则，不忠实的信息可能会增加法学硕士的幻觉问题。此外，即使收集到的信息质量很高，但仍不清楚它们是否真正用于综合反应。解决这个问题的一个潜在策略是让法学硕士能够自主验证他们抓取的文档。

### 段落 258 · Page 24

**EN**

This self-validation process could incorporate mechanisms for assessing the credibility and accuracy of the information within these documents. •Mitigating Bias and Offensive Content in LLMs.The presence of biases and offensive content within LLM outputs is a pressing concern. This issue primarily stems from biases inherent in the training data and will be amplified by the lowquality information gathered from the web. Achieving this requires a multi-faceted approach, including improvements in training data, algorithmic adjustments, and continuous monitoring for bias and inappropriate content that LLMs collect and generate.

**中文**

这种自我验证过程可以包含评估这些文档中信息的可信度和准确性的机制。 •减少法学硕士中的偏见和攻击性内容。法学硕士输出中存在的偏见和攻击性内容是一个紧迫的问题。这个问题主要源于训练数据固有的偏差，并且会因从网络收集的低质量信息而被放大。实现这一目标需要采取多方面的方法，包括改进培训数据、调整算法以及持续监控法学硕士收集和生成的偏见和不当内容。

### Page 25

### 段落 259 · Page 25

**EN**

25 8.6 Evaluation LLMs have attracted significant attention in the field of IR due to their strong ability in context understanding and text generation. To validate the effectiveness of LLM-enhanced IR approaches, it is crucial to develop appropriate evaluation metrics. Given the growing significance of readers as integral components of IR systems, the evaluation should consider two aspects: assessing ranking performance and evaluating generation performance. •Generation-oriented ranking evaluation.Traditional evaluation metrics for ranking primarily focus on comparing the retrieval results of IR models with ground-truth (relevance) labels.

**中文**

25 8.6 评价 法学硕士因其强大的语境理解和文本生成能力而在国际关系学领域引起了广泛关注。为了验证法学硕士增强型 IR 方法的有效性，制定适当的评估指标至关重要。鉴于读者作为IR系统不可或缺的组成部分的重要性日益增强，评估应考虑两个方面：评估排名绩效和评估生成绩效。 •面向世代的排名评估。传统的排名评估指标主要侧重于将IR模型的检索结果与真实（相关性）标签进行比较。

### 段落 260 · Page 25

**EN**

Typical metrics include precision, recall, mean reciprocal rank (MRR) [340], mean average precision (MAP), and normalized discounted cumulative gain (nDCG) [341]. These metrics measure the alignment between ranking results and human preference on using these results. Nevertheless, these metrics may fall short in capturing a document’s role in the generation of passages or answers, as their relevance to the query alone might not adequately reflect this aspect. This effect could be leveraged as a means to evaluate the usefulness of documents more comprehensively.

**中文**

典型的指标包括精度、召回率、平均倒数排名（MRR）[340]、平均精度（MAP）和归一化折扣累积增益（nDCG）[341]。这些指标衡量排名结果与人们使用这些结果的偏好之间的一致性。然而，这些指标可能无法捕捉文档在生成段落或答案中的作用，因为它们与查询的相关性本身可能不足以反映这一方面。可以利用这种效应作为更全面地评估文档有用性的手段。

### 段落 261 · Page 25

**EN**

A formal and rigorous evaluation metric for ranking that centers on generation quality has yet to be defined. •Text generation evaluation.The wide application of LLMs in IR has led to a notable enhancement in their generation capability. Consequently, there is an imperative demand for novel evaluation strategies to effectively evaluate the performance of passage or answer generation. Previous evaluation metrics for text generation have several limitations, including: (1) Dependency on lexical matching: methods such as BLEU [342] or ROUGE [343] primarily evaluate the quality of generated outputs based onn-gram matching.

**中文**

以发电质量为中心的正式且严格的排名评估指标尚未确定。 •文本生成评估。法学硕士在信息检索领域的广泛应用导致其生成能力显着增强。因此，迫切需要新颖的评估策略来有效评估段落或答案生成的性能。以前的文本生成评估指标有几个局限性，包括：（1）对词汇匹配的依赖：BLEU [342]或ROUGE [343]等方法主要评估基于n-gram匹配的生成输出的质量。

### 段落 262 · Page 25

**EN**

This approach cannot account for lexical diversity and contextual semantics. As a result, models may favor generating common phrases or sentence structures rather than producing creative and novel content. (2) Insensitivity to subtle differences: existing evaluation methods may be insensitive to subtle differences in generated outputs. For example, if a generated output has minor semantic differences from the reference answer but is otherwise similar, traditional methods might overlook these nuanced distinctions. (3) Lack of ability to evaluate factuality: LLMs are prone to generating “hallucination” problems [344–347].

**中文**

这种方法无法解释词汇多样性和上下文语义。因此，模型可能倾向于生成常见的短语或句子结构，而不是生成创造性和新颖的内容。 (2) 对细微差异不敏感：现有的评估方法可能对生成输出的细微差异不敏感。例如，如果生成的输出与参考答案具有微小的语义差异，但在其他方面相似，则传统方法可能会忽略这些细微差别。 （3）缺乏评估事实的能力：法学硕士容易产生“幻觉”问题[344-347]。

### 段落 263 · Page 25

**EN**

The hallucinated texts can closely resemble the oracle texts in terms of vocabulary usage, sentence structures, and patterns, while having nonfactual content. Existing methods are hard to identify such problems, while the incorporation of additional knowledge sources such as knowledge bases or reference texts could potentially aid in addressing this challenge. 8.7 Bias Since ChatGPT was released, LLMs have drawn much attention from both academia and industry. The wide applications of LLMs have led to a notable increase in content on the Internet that is not authored by humans but rather generated by these language models.

**中文**

幻觉文本在词汇使用、句子结构和模式方面与甲骨文非常相似，但内容却非事实。现有方法很难识别此类问题，而纳入知识库或参考文本等其他知识源可能有助于解决这一挑战。 8.7 偏见 自 ChatGPT 发布以来，LLM 受到学术界和工业界的广泛关注。法学硕士的广泛应用导致互联网上非人类创作而是由这些语言模型生成的内容显着增加。

### 段落 264 · Page 25

**EN**

However, as LLMs may hallucinate and generate non-factual texts, the increasing number of LLM-generated contents also brings worries that these contents may provide fictitious information for users across IR systems. More severely, researchers [348, 349] show that some modules in IR systems such as retriever and reranker, especially those based on neural models, may prefer LLM-generated documents, since their topics are more consistent and the perplexity of them are lower compared with human-written documents. The authors refer to this phenomenon as the “source bias” towards LLM-generated text.

**中文**

然而，由于法学硕士可能会产生幻觉并生成非事实文本，法学硕士生成的内容数量不断增加也带来了人们的担忧，即这些内容可能会为跨IR系统的用户提供虚构信息。更严重的是，研究人员[348, 349]表明，IR系统中的一些模块，例如检索器和重排序器，尤其是基于神经模型的模块，可能更喜欢LLM生成的文档，因为与人类编写的文档相比，它们的主题更加一致，并且复杂度更低。作者将这种现象称为对法学硕士生成文本的“来源偏见”。

### 段落 265 · Page 25

**EN**

It is challenging but necessary to consider how to build IR systems free from this category of bias. 9 CONCLUSION In this survey, we have conducted a thorough exploration of the transformative impact of LLMs on IR across various dimensions. We have organized existing approaches into distinct categories based on their functions: query rewriter, retrieval, reranking, and reader modules. In the domain of query rewriter, LLMs have demonstrated their effectiveness in understanding ambiguous or multi-faceted queries, enhancing the accuracy of intent identification.

**中文**

考虑如何构建没有此类偏见的 IR 系统是具有挑战性的，但也是必要的。 9 结论 在本次调查中，我们对法学硕士在各个维度对 IR 的变革性影响进行了深入探索。我们根据现有方法的功能将其分为不同的类别：查询重写器、检索、重排和阅读器模块。在查询重写器领域，法学硕士已经证明了其在理解模糊或多方面查询方面的有效性，从而提高了意图识别的准确性。

### 段落 266 · Page 25

**EN**

In the context of retrieval, LLMs have improved retrieval accuracy by enabling more nuanced matching between queries and documents, considering context as well. Within the reranking realm, LLM-enhanced models consider more fine-grained linguistic nuances when re-ordering results. The incorporation of reader modules in IR systems represents a significant step towards generating comprehensive responses instead of mere document lists. The integration of LLMs into IR systems has brought about a fundamental change in how users engage with information and knowledge.

**中文**

在检索方面，法学硕士通过在查询和文档之间进行更细致的匹配并考虑上下文来提高检索准确性。在重排领域，法学硕士增强模型在对结果重新排序时会考虑更细粒度的语言细微差别。将阅读器模块纳入 IR 系统代表着向生成全面响应而不仅仅是文档列表迈出的重要一步。法学硕士与 IR 系统的集成为用户处理信息和知识的方式带来了根本性的变化。

### 段落 267 · Page 25

**EN**

From query rewriter to retrieval, reranking, and reader modules, LLMs have enriched each aspect of the IR process with advanced linguistic comprehension, semantic representation, and context-sensitive handling. As this field continues to progress, the journey of LLMs in IR portends a future characterized by more personalized, precise, and user-centric search encounters. This survey focuses on reviewing recent studies of applying LLMs to different IR components and using LLMs as search agents. Beyond this, a more significant problem brought by the appearance of LLMs is: is the conventional IR framework necessary in the era of LLMs?

**中文**

从查询重写器到检索、重排和阅读器模块，法学硕士通过高级语言理解、语义表示和上下文敏感处理丰富了 IR 流程的各个方面。随着这一领域的不断发展，IR 法学硕士的旅程预示着一个以更加个性化、精确和以用户为中心的搜索体验为特征的未来。本次调查的重点是回顾最近将法学硕士应用于不同 IR 组件以及使用法学硕士作为搜索代理的研究。除此之外，法学硕士的出现带来的一个更重要的问题是：法学硕士时代传统的IR框架还有必要吗？

### 段落 268 · Page 25

**EN**

For example, traditional IR aims to return a ranking list of documents that are relevant to issued queries. However, the development of generative language models has introduced a novel paradigm: the direct generation of answers to input questions. Furthermore, according to a recent perspective paper [50], IR might evolve into a fundamental service for diverse systems. For example, in a multi-agent simulation system [350], an IR component can be used for memory recall. This implies that there will be many new challenges in future IR. REFERENCES [1] Y. Wu, W. Wu, C. Xing, M. Zhou, and Z.

**中文**

例如，传统的 IR 旨在返回与发出的查询相关的文档的排名列表。然而，生成语言模型的发展引入了一种新颖的范式：直接生成输入问题的答案。此外，根据最近的一篇观点论文 [50]，IR 可能会演变成不同系统的基本服务。例如，在多智能体模拟系统[350]中，IR组件可用于记忆回忆。这意味着未来IR将面临许多新的挑战。参考文献 [1] Y. Wu，W. Wu，C. Xing，M. Zhou，Z.

### 段落 269 · Page 25

**EN**

Li, “Sequential matching network: A new architecture for multi-turn response selection in retrieval-based chatbots,” inProceedings of the 55th Annual Meeting of the Association for Computational Linguistics, ACL 2017, Vancouver, Canada, July 30 - August 4, Volume 1: Long

**中文**

Li，“顺序匹配网络：基于检索的聊天机器人中多轮响应选择的新架构”，计算语言学协会第 55 届年会记录，ACL 2017，加拿大温哥华，7 月 30 日至 8 月 4 日，第 1 卷：长

### Page 26

### 段落 270 · Page 26

**EN**

26 Papers, R. Barzilay and M. Kan, Eds. Association for Computational Linguistics, 2017, pp. 496–505. [2] H. Shum, X. He, and D. Li, “From eliza to xiaoice: challenges and opportunities with social chatbots,” Frontiers Inf. Technol. Electron. Eng., vol. 19, no. 1, pp. 10–26, 2018. [3] V . Karpukhin, B. Oguz, S. Min, P . S. H. Lewis, L. Wu, S. Edunov, D. Chen, and W. Yih, “Dense passage retrieval for open-domain question answering,” in Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing, EMNLP 2020, Online, November 16-20, 2020, B. Webber, T. Cohn, Y. He, and Y. Liu, Eds.

**中文**

26 论文，R. Barzilay 和 M. Kan，编辑。计算语言学协会，2017 年，第 496-505 页。 [2] H. Shum、X. He 和 D. Li，“从 eliza 到 xiaoice：社交聊天机器人的挑战和机遇”，Frontiers Inf。技术。电子。工程，卷。 19、没有。 1，第 10-26 页，2018 年。 [3] V .卡普欣，B.奥古兹，S.敏，P。 S. H. Lewis、L. Wu、S. Edunov、D. Chen 和 W. Yih，“开放域问答的密集段落检索”，《2020 年自然语言处理经验方法会议论文集》，EMNLP 2020，在线，2020 年 11 月 16-20 日，B. Webber、T. Cohn、Y. He 和 Y. Liu，编辑。

### 段落 271 · Page 26

**EN**

Association for Computational Linguistics, 2020, pp. 6769–6781. [4] R. Datta, D. Joshi, J. Li, and J. Z. Wang, “Image retrieval: Ideas, influences, and trends of the new age,” ACM Comput. Surv., vol. 40, no. 2, pp. 5:1–5:60, 2008. [5] C. Yuan, W. Zhou, M. Li, S. Lv, F. Zhu, J. Han, and S. Hu, “Multi-hop selector network for multiturn response selection in retrieval-based chatbots,” in Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing, EMNLP-IJCNLP 2019, Hong Kong, China, November 3- 7, 2019, K. Inui, J. Jiang, V . Ng, and X.

**中文**

计算语言学协会，2020 年，第 6769–6781 页。 [4] R. Datta、D. Joshi、J. Li 和 J. Z. Wang，“图像检索：新时代的思想、影响和趋势”，ACM Comput。幸存者，卷。 40，没有。 2，第 5:1–5:60，2008 年。[5] C. Yuan、W. Zhou、M. Li、S. Lv、F. Zhu、J. Han 和 S. Hu，“基于检索的聊天机器人中用于多轮响应选择的多跳选择器网络”，载于 2019 年自然语言处理经验方法会议和第九届自然语言处理国际联合会议论文集， EMNLP-IJCNLP 2019，中国香港，2019年11月3-7日，K. Inui, J. Jiang, V .吴、X.

### 段落 272 · Page 26

**EN**

Wan, Eds. Association for Computational Linguistics, 2019, pp. 111–120. [6] Y. Zhu, J. Nie, K. Zhou, P . Du, and Z. Dou, “Content selection network for document-grounded retrievalbased chatbots,” inAdvances in Information Retrieval - 43rd European Conference on IR Research, ECIR 2021, Virtual Event, March 28 - April 1, 2021, Proceedings, Part I, ser. Lecture Notes in Computer Science, D. Hiemstra, M. Moens, J. Mothe, R. Perego, M. Potthast, and F. Sebastiani, Eds., vol. 12656. Springer, 2021, pp. 755–769. [7] Y. Zhu, J. Nie, K. Zhou, P . Du, H. Jiang, and Z.

**中文**

万编辑。计算语言学协会，2019 年，第 111-120 页。 [6] 朱勇，聂家，周坤，P. Du 和 Z. Dou，“基于文档检索的聊天机器人的内容选择网络”，《信息检索进展 - 第 43 届欧洲 IR 研究会议》，ECIR 2021，虚拟活动，2021 年 3 月 28 日至 4 月 1 日，会议记录，第一部分，系列。计算机科学讲义，D. Hiemstra、M. Moens、J. Mothe、R. Perego、M. Potthast 和 F. Sebastiani，编辑，卷。 12656。施普林格，2021，第 755–769 页。 [7] 朱勇，聂家，周坤，P.杜，H.Jiang，Z.

### 段落 273 · Page 26

**EN**

Dou, “Proactive retrieval-based chatbots based on relevant knowledge and goals,” inSIGIR ’21: The 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, Virtual Event, Canada, July 11-15, 2021, F. Diaz, C. Shah, T. Suel, P . Castells, R. Jones, and T. Sakai, Eds. ACM, 2021, pp. 2000– 2004. [8] H. Qian, Z. Dou, Y. Zhu, Y. Ma, and J. Wen, “Learning implicit user profiles for personalized retrieval-based chatbot,”CoRR, vol. abs/2108.07935, 2021. [9] Y. Qu, Y. Ding, J. Liu, K. Liu, R. Ren, W. X. Zhao, D. Dong, H. Wu, and H.

**中文**

Dou，“基于相关知识和目标的主动检索聊天机器人”，inSIGIR ’21：第 44 届国际 ACM SIGIR 信息检索研究与开发会议，虚拟活动，加拿大，2021 年 7 月 11-15 日，F. Diaz、C. Shah、T. Suel、P。 Castells、R. Jones 和 T. Sakai，编辑。 ACM，2021，第 2000-2004 页。 [8] H.Qian、Z.Dou、Y.Zhu、Y.Ma 和 J.Wen，“学习基于个性化检索的聊天机器人的隐式用户配置文件”，CoRR，卷。 abs/2108.07935, 2021. [9] 曲勇、丁勇、刘建、刘坤、任荣、赵文新、董东、吴红、H.

### 段落 274 · Page 26

**EN**

Wang, “Rocketqa: An optimized training approach to dense passage retrieval for open-domain question answering,” inProceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, NAACL-HLT 2021, Online, June 6- 11, 2021, K. Toutanova, A. Rumshisky, L. Zettlemoyer, D. Hakkani-T ¨ur, I. Beltagy, S. Bethard, R. Cotterell, T. Chakraborty, and Y. Zhou, Eds. Association for Computational Linguistics, 2021, pp. 5835–5847. [10] Y. Arens, C. A. Knoblock, and W. Shen, “Query reformulation for dynamic information integration,”J. Intell. Inf. Syst., vol. 6, no. 2/3, pp.

**中文**

Wang，“Rocketqa：开放域问答的密集段落检索的优化训练方法”，载于计算语言学协会北美分会 2021 年会议记录：人类语言技术，NAACL-HLT 2021，在线，2021 年 6 月 6-11 日，K. Toutanova、A. Rumshisky、L. Zettlemoyer、D. Hakkani-T ur、I. Beltagy、S. Bethard、R. Cotterell、T. Chakraborty 和 Y. Zhou，编辑。计算语言学协会，2021 年，第 5835–5847 页。 [10] Y. Arens、C. A. Knoblock 和 W. Shen，“动态信息集成的查询重构”，J.英特尔。信息。系统，卷。 6、没有。 2/3，页。

### 段落 275 · Page 26

**EN**

99–130, 1996. [11] J. Huang and E. N. Efthimiadis, “Analyzing and evaluating query reformulation strategies in web search logs,” inProceedings of the 18th ACM Conference on Information and Knowledge Management, CIKM 2009, Hong Kong, China, November 2-6, 2009, D. W. Cheung, I. Song, W. W. Chu, X. Hu, and J. Lin, Eds. ACM, 2009, pp. 77–86. [12] R. F. Nogueira, W. Yang, K. Cho, and J. Lin, “Multistage document ranking with BERT,”CoRR, vol. abs/1910.14424, 2019. [13] R. Nogueira, Z. Jiang, R. Pradeep, and J.

**中文**

99–130, 1996。 [11] J. Huang 和 E. N. Efthimiadis，“分析和评估网络搜索日志中的查询重构策略”，第 18 届 ACM 信息和知识管理会议论文集，CIKM 2009，中国香港，2009 年 11 月 2-6 日，D. W. Cheung、I. Song、W. W. Chu、X. Hu 和J.林，编辑。 ACM，2009 年，第 77-86 页。 [12] R. F. Nogueira、W. Yang、K. Cho 和 J. Lin，“使用 BERT 进行多阶段文档排序”，CoRR，第 1 卷。 abs/1910.14424, 2019。 [13] R. Nogueira, Z. Jiang, R. Pradeep, and J.

### 段落 276 · Page 26

**EN**

Lin, “Document ranking with a pretrained sequence-to-sequence model,” inFindings of the Association for Computational Linguistics: EMNLP 2020, Online Event, 16-20 November 2020, ser. Findings of ACL, T. Cohn, Y. He, and Y. Liu, Eds., vol. EMNLP 2020. Association for Computational Linguistics, 2020, pp. 708–718. [14] Y. Zhu, J. Nie, Z. Dou, Z. Ma, X. Zhang, P . Du, X. Zuo, and H. Jiang, “Contrastive learning of user behavior sequence for context-aware document ranking,” in CIKM ’21: The 30th ACM International Conference on Information and Knowledge Management, Virtual Event, Queensland, Australia, November 1 - 5, 2021, G. Demartini, G.

**中文**

Lin，“使用预训练的序列到序列模型进行文档排名”，载于计算语言学协会的调查结果：EMNLP 2020，在线活动，2020 年 11 月 16-20 日，ser。 ACL 的发现，T. Cohn、Y. He 和 Y. Liu，编辑，卷。 EMNLP 2020。计算语言学协会，2020 年，第 708–718 页。 [14] 朱勇，聂静，窦正，马正，张旭，平。 Du、X. Zuo 和 H. Jiang，“上下文感知文档排名的用户行为序列的对比学习”，CIKM ’21：第 30 届 ACM 国际信息和知识管理会议，虚拟活动，澳大利亚昆士兰，2021 年 11 月 1 - 5 日，G. Demartini，G.

### 段落 277 · Page 26

**EN**

Zuccon, J. S. Culpepper, Z. Huang, and H. Tong, Eds. ACM, 2021, pp. 2780–2791. [15] J. Teevan, S. T. Dumais, and E. Horvitz, “Personalizing search via automated analysis of interests and activities,” inSIGIR 2005: Proceedings of the 28th Annual International ACM SIGIR Conference on Research and Development in Information Retrieval, Salvador, Brazil, August 15-19, 2005, R. A. Baeza-Yates, N. Ziviani, G. Marchionini, A. Moffat, and J. Tait, Eds. ACM, 2005, pp. 449–456. [16] P . N. Bennett, R. W. White, W. Chu, S. T. Dumais, P . Bailey, F. Borisyuk, and X.

**中文**

Zuccon、J. S. Culpepper、Z. Huang 和 H. Tong，编辑。 ACM，2021 年，第 2780–2791 页。 [15] J. Teevan、S. T. Dumais 和 E. Horvitz，“通过兴趣和活动的自动分析实现个性化搜索”，inSIGIR 2005：第 28 届国际 ACM SIGIR 信息检索研究与开发会议记录，巴西萨尔瓦多，2005 年 8 月 15-19 日，R. A. Baeza-Yates、N. Ziviani， G. Marchionini、A. Moffat 和 J. Tait，编辑。 ACM，2005 年，第 449–456 页。 [16] P. N.贝内特、R.W.怀特、W.楚、S.T.杜迈斯、P。贝利 (Bailey)、F. 鲍里修克 (F. Borisyuk) 和 X.

### 段落 278 · Page 26

**EN**

Cui, “Modeling the impact of short- and long-term behavior on search personalization,” inThe 35th International ACM SIGIR conference on research and development in Information Retrieval, SIGIR ’12, Portland, OR, USA, August 12-16, 2012, W. R. Hersh, J. Callan, Y. Maarek, and M. Sanderson, Eds. ACM, 2012, pp. 185–194. [17] S. Ge, Z. Dou, Z. Jiang, J. Nie, and J. Wen, “Personalizing search results using hierarchical RNN with query-aware attention,” inProceedings of the 27th ACM International Conference on Information and Knowledge Management, CIKM 2018, Torino, Italy, October 22-26, 2018, A. Cuzzocrea, J. Allan, N. W. Paton, D. Srivastava, R.

**中文**

Cui，“模拟短期和长期行为对搜索个性化的影响”，第 35 届国际 ACM SIGIR 信息检索研究与开发会议，SIGIR '12，美国俄勒冈州波特兰，2012 年 8 月 12-16 日，W. R. Hersh、J. Callan、Y. Maarek 和 M. Sanderson，编辑。 ACM，2012 年，第 185–194 页。 [17] S. Ge、Z. Dou、Z. Jiang、J. Nie 和 J. Wen，“使用具有查询感知注意力的分层 RNN 个性化搜索结果”，第 27 届 ACM 国际信息与知识管理会议论文集，CIKM 2018，意大利都灵，2018 年 10 月 22-26 日，A. Cuzzocrea、J. Allan、N. W. Paton、D.斯里瓦斯塔瓦，R.

### 段落 279 · Page 26

**EN**

Agrawal, A. Z. Broder, M. J. Zaki, K. S. Candan, A. Labrinidis, A. Schuster, and H. Wang, Eds. ACM, 2018, pp. 347–356. [18] Y. Zhou, Z. Dou, Y. Zhu, and J. Wen, “PSSL: selfsupervised learning for personalized search with contrastive sampling,” inCIKM ’21: The 30th ACM International Conference on Information and Knowledge Management, Virtual Event, Queensland, Australia, November 1 - 5, 2021, G. Demartini, G. Zuccon, J. S. Culpepper, Z. Huang, and H. Tong, Eds. ACM, 2021, pp. 2749– 2758. [19] J. G. Carbonell and J. Goldstein, “The use of mmr, diversity-based reranking for reordering documents and producing summaries,” inSIGIR ’98: Proceedings

**中文**

Agrawal、A. Z. Broder、M. J. Zaki、K. S. Candan、A. Labrinidis、A. Schuster 和 H. Wang，编辑。 ACM，2018 年，第 347–356 页。 [18] Y. Zhou、Z. Dou、Y. Zhu 和 J. Wen，“PSSL：通过对比抽样进行个性化搜索的自监督学习”，inCIKM ’21：第 30 届 ACM 国际信息和知识管理会议，虚拟活动，澳大利亚昆士兰，2021 年 11 月 1 - 5 日，G. Demartini、G. Zuccon、J. S. Culpepper、Z. Huang 和 H. Tong，编辑。 ACM，2021，第 2749–2758 页。 [19] J. G. Carbonell 和 J. Goldstein，“使用 mmr、基于多样性的重新排序来重新排序文档和生成摘要”，inSIGIR ’98：会议记录

### Page 27

### 段落 280 · Page 27

**EN**

27 of the 21st Annual International ACM SIGIR Conference on Research and Development in Information Retrieval, August 24-28 1998, Melbourne, Australia, W. B. Croft, A. Moffat, C. J. van Rijsbergen, R. Wilkinson, and J. Zobel, Eds. ACM, 1998, pp. 335–336. [20] R. Agrawal, S. Gollapudi, A. Halverson, and S. Ieong, “Diversifying search results,” inProceedings of the Second International Conference on Web Search and Web Data Mining, WSDM 2009, Barcelona, Spain, February 9-11, 2009, R. Baeza-Yates, P . Boldi, B. A. Ribeiro-Neto, and B. B. Cambazoglu, Eds. ACM, 2009, pp. 5–14. [21] J. Liu, Z. Dou, X. Wang, S. Lu, and J.

**中文**

第 21 届国际 ACM SIGIR 信息检索研究与开发年会第 27 期，1998 年 8 月 24-28 日，澳大利亚墨尔本，W. B. Croft、A. Moffat、C. J. van Rijsbergen、R. Wilkinson 和 J. Zobel，编辑。 ACM，1998 年，第 335–336 页。 [20] R. Agrawal、S. Gollapudi、A. Halverson 和 S. Ieong，“多样化搜索结果”，第二届网络搜索和网络数据挖掘国际会议记录，WSDM 2009，西班牙巴塞罗那，2009 年 2 月 9-11 日，R. Baeza-Yates, P . Boldi，B. A. Ribeiro-Neto，和 B. B. Cambazoglu，编辑。 ACM，2009 年，第 5-14 页。 [21] 刘建，窦正，王X，陆思，J.

### 段落 281 · Page 27

**EN**

Wen, “DVGAN: A minimax game for search result diversification combining explicit and implicit features,” inProceedings of the 43rd International ACM SIGIR conference on research and development in Information Retrieval, SIGIR 2020, Virtual Event, China, July 25-30, 2020, J. X. Huang, Y. Chang, X. Cheng, J. Kamps, V . Murdock, J. Wen, and Y. Liu, Eds. ACM, 2020, pp. 479–488. [22] Z. Su, Z. Dou, Y. Zhu, X. Qin, and J. Wen, “Modeling intent graph for search result diversification,” inSIGIR ’21: The 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, Virtual Event, Canada, July 11-15, 2021, F. Diaz, C.

**中文**

Wen，“DVGAN：结合显式和隐式特征的搜索结果多样化的极小极大游戏”，载于第 43 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR 2020，虚拟活动，中国，2020 年 7 月 25-30 日，J. X. Huang, Y. Chang, X. Cheng, J. Kamps, V . Murdock，J. Wen 和 Y. Liu，编辑。 ACM，2020 年，第 479–488 页。 [22] Z. Su、Z. Dou、Y. Zhu、X.qin 和 J. Wen，“搜索结果多样化的意图图建模”，inSIGIR '21：第 44 届国际 ACM SIGIR 信息检索研究与开发会议，虚拟活动，加拿大，2021 年 7 月 11-15 日，F. Diaz, C.

### 段落 282 · Page 27

**EN**

Shah, T. Suel, P . Castells, R. Jones, and T. Sakai, Eds. ACM, 2021, pp. 736–746. [23] S. Borgeaud, A. Mensch, J. Hoffmann, T. Cai, E. Rutherford, K. Millican, G. van den Driessche, J. Lespiau, B. Damoc, A. Clark, D. de Las Casas, A. Guy, J. Menick, R. Ring, T. Hennigan, S. Huang, L. Maggiore, C. Jones, A. Cassirer, A. Brock, M. Paganini, G. Irving, O. Vinyals, S. Osindero, K. Simonyan, J. W. Rae, E. Elsen, and L. Sifre, “Improving language models by retrieving from trillions of tokens,” inInternational Conference on Machine Learning, ICML 2022, 17-23 July 2022, Baltimore, Maryland, USA, ser. Proceedings of Machine Learning Research, K.

**中文**

沙阿 (Shah)，T. 苏埃尔 (Suel)，P. Castells、R. Jones 和 T. Sakai，编辑。 ACM，2021 年，第 736–746 页。 [23] S. Borgeaud、A. Mensch、J. Hoffmann、T. Cai、E. Rutherford、K. Millican、G. van den Driessche、J. Lespiau、B. Damoc、A. Clark、D. de Las Casas、A. Guy、J. Menick、R. Ring、T. Hennigan、S. Huang、L. Maggiore、C. Jones、A. Cassirer、A. Brock、 M. Paganini、G. Irving、O. Vinyals、S. Osindero、K. Simonyan、J. W. Rae、E. Elsen 和 L. Sifre，“通过从数万亿个标记中检索来改进语言模型”，载于国际机器学习会议，ICML 2022，2022 年 7 月 17-23 日，美国马里兰州巴尔的摩，ser。机器学习研究论文集，K.

### 段落 283 · Page 27

**EN**

Chaudhuri, S. Jegelka, L. Song, C. Szepesv ´ari, G. Niu, and S. Sabato, Eds., vol. 162. PMLR, 2022, pp. 2206–2240. [24] R. Nakano, J. Hilton, S. Balaji, J. Wu, L. Ouyang, C. Kim, C. Hesse, S. Jain, V . Kosaraju, W. Saunders, X. Jiang, K. Cobbe, T. Eloundou, G. Krueger, K. Button, M. Knight, B. Chess, and J. Schulman, “Webgpt: Browser-assisted question-answering with human feedback,”CoRR, vol. abs/2112.09332, 2021. [25] G. Salton and M. McGill,Introduction to Modern Information Retrieval. McGraw-Hill Book Company, 1984. [26] G. Salton, A. Wong, and C. Yang, “A vector space model for automatic indexing,”Commun. ACM, vol. 18, no. 11, pp.

**中文**

Chaudhuri、S. Jegelka、L. Song、C. Szepesv ´ari、G. Niu 和 S. Sabato，编辑，卷。 162.PMLR，2022 年，第 2206-2240 页。 [24] R. Nakano、J. Hilton、S. Balaji、J. Wu、L. Ouyang、C. Kim、C. Hesse、S. Jain、V。 Kosaraju、W. Saunders、X. Jiang、K. Cobbe、T. Eloundou、G. Krueger、K. Button、M. Knight、B. Chess 和 J. Schulman，“Webgpt：带有人类反馈的浏览器辅助问答”，CoRR，卷。 abs/2112.09332，2021。 [25] G. Salton 和 M. McGill，现代信息检索导论。 McGraw-Hill Book Company，1984。 [26] G. Salton、A. Wong 和 C. Yang，“自动索引的向量空间模型”，Commun。 ACM，卷。 18、没有。 11，页。

### 段落 284 · Page 27

**EN**

613–620, 1975. [27] F. Song and W. B. Croft, “A general language model for information retrieval,” inProceedings of the 1999 ACM CIKM International Conference on Information and Knowledge Management, Kansas City, Missouri, USA, November 2-6, 1999. ACM, 1999, pp. 316–321. [28] J. Martineau and T. Finin, “Delta TFIDF: an improved feature space for sentiment analysis,” inProceedings of the Third International Conference on Weblogs and Social Media, ICWSM 2009, San Jose, California, USA, May 17- 20, 2009, E. Adar, M. Hurst, T. Finin, N. S. Glance, N. Nicolov, and B. L. Tseng, Eds. The AAAI Press, 2009. [29] S. E. Robertson, S. Walker, S.

**中文**

613–620, 1975。 [27] F. Song 和 W. B. Croft，“信息检索的通用语言模型”，载于 1999 年 ACM CIKM 国际信息和知识管理会议记录，美国密苏里州堪萨斯城，1999 年 11 月 2-6 日。ACM，1999 年，第 316–321 页。 [28] J. Martineau 和 T. Finin，“Delta TFIDF：改进的情感分析特征空间”，载于第三届国际博客和社交媒体会议论文集，ICWSM 2009，美国加利福尼亚州圣何塞，2009 年 5 月 17-20 日，E. Adar、M. Hurst、T. Finin、N. S. Glance、N. Nicolov 和 B. L. Tseng，编辑。 AAAI 出版社，2009 年。 [29] S. E. Robertson、S. Walker、S.

### 段落 285 · Page 27

**EN**

Jones, M. Hancock- Beaulieu, and M. Gatford, “Okapi at TREC-3,” in Proceedings of The Third Text REtrieval Conference, TREC 1994, Gaithersburg, Maryland, USA, November 2-4, 1994, ser. NIST Special Publication, D. K. Harman, Ed., vol. 500-225. National Institute of Standards and Technology (NIST), 1994, pp. 109–126. [30] J. Guo, Y. Fan, Q. Ai, and W. B. Croft, “A deep relevance matching model for ad-hoc retrieval,” in Proceedings of the 25th ACM International Conference on Information and Knowledge Management, CIKM 2016, Indianapolis, IN, USA, October 24-28, 2016, S. Mukhopadhyay, C. Zhai, E. Bertino, F. Crestani, J. Mostafa, J. Tang, L.

**中文**

Jones, M. Hancock- Beaulieu 和 M. Gatford，“Okapi at TREC-3”，第三次文本检索会议记录，TREC 1994，美国马里兰州盖瑟斯堡，1994 年 11 月 2-4 日，系列。 NIST 特别出版物，D.K. Harman，编辑，卷。 500-225。美国国家标准与技术研究所 (NIST)，1994 年，第 109-126 页。 [30] J.Guo、Y.Fan、Q.Ai 和 W.B.Croft，“用于即席检索的深度相关性匹配模型”，第 25 届 ACM 国际信息和知识管理会议论文集，CIKM 2016，美国印第安纳州印第安纳波利斯，2016 年 10 月 24-28 日，S. Mukhopadhyay、C. Zhai、E. Bertino、F. Crestani， J.穆斯塔法，J.唐，L.

### 段落 286 · Page 27

**EN**

Si, X. Zhou, Y. Chang, Y. Li, and P . Sondhi, Eds. ACM, 2016, pp. 55–64. [31] L. Xiong, C. Xiong, Y. Li, K. Tang, J. Liu, P . N. Bennett, J. Ahmed, and A. Overwijk, “Approximate nearest neighbor negative contrastive learning for dense text retrieval,” in9th International Conference on Learning Representations, ICLR 2021, Virtual Event, Austria, May 3-7, 2021. OpenReview.net, 2021. [32] J. Lin, R. F. Nogueira, and A. Yates,Pretrained Transformers for Text Ranking: BERT and Beyond, ser. Synthesis Lectures on Human Language Technologies. Morgan & Claypool Publishers, 2021. [33] A. Radford, J. Wu, R. Child, D. Luan, D. Amodei, and I.

**中文**

斯，周X，张Y，李Y，P。桑迪，编辑。 ACM，2016 年，第 55-64 页。 [31] 熊立，熊成，李勇，唐坤，刘建平。 N. Bennett、J. Ahmed 和 A. Overwijk，“用于密集文本检索的近似最近邻负对比学习”，第九届学习表示国际会议，ICLR 2021，虚拟活动，奥地利，2021 年 5 月 3-7 日。OpenReview.net，2021。 [32] J. Lin、R. F. Nogueira 和 A. Yates，文本预训练 Transformers排名：BERT and Beyond，ser。人类语言技术综合讲座。 Morgan & Claypool Publishers，2021。 [33] A. Radford、J. Wu、R. Child、D. Luan、D. Amodei 和 I。

### 段落 287 · Page 27

**EN**

Sutskever, “Language models are unsupervised multitask learners,” 2019. [34] T. B. Brown, B. Mann, N. Ryder, M. Subbiah, J. Kaplan, P . Dhariwal, A. Neelakantan, P . Shyam, G. Sastry, A. Askell, S. Agarwal, A. Herbert-Voss, G. Krueger, T. Henighan, R. Child, A. Ramesh, D. M. Ziegler, J. Wu, C. Winter, C. Hesse, M. Chen, E. Sigler, M. Litwin, S. Gray, B. Chess, J. Clark, C. Berner, S. Mc- Candlish, A. Radford, I. Sutskever, and D. Amodei, “Language models are few-shot learners,” inAdvances in Neural Information Processing Systems 33: Annual Conference on Neural Information Processing Systems 2020, NeurIPS 2020, December 6-12, 2020, virtual, H.

**中文**

Sutskever，“语言模型是无监督的多任务学习者”，2019 年。 [34] T. B. Brown、B. Mann、N. Ryder、M. Subbiah、J. Kaplan、P . Dhariwal, A. Neelakantan, P . Shyam、G. Sastry、A. Askell、S. Agarwal、A. Herbert-Voss、G. Krueger、T. Henighan、R. Child、A. Ramesh、D. M. Ziegler、J. Wu、C. Winter、C. Hesse、M. Chen、E. Sigler、M. Litwin、S. Gray、B. Chess、J. Clark、C. Berner、S. Mc-Candlish、 A. Radford、I. Sutskever 和 D. Amodei，“语言模型是小样本学习者”，《神经信息处理系统进展 33：2020 年神经信息处理系统年会》，NeurIPS 2020，2020 年 12 月 6-12 日，虚拟，H.

### 段落 288 · Page 27

**EN**

Larochelle, M. Ranzato, R. Hadsell, M. Balcan, and H. Lin, Eds., 2020. [35] H. Touvron, T. Lavril, G. Izacard, X. Martinet, M. Lachaux, T. Lacroix, B. Rozi`ere, N. Goyal, E. Hambro, F. Azhar, A. Rodriguez, A. Joulin, E. Grave, and G. Lample, “Llama: Open and efficient foundation language models,”CoRR, vol. abs/2302.13971, 2023. [36] J. Zhang, R. Xie, Y. Hou, X. Zhao, L. Lin, and J. Wen, “Recommendation as instruction following: A large language model empowered recommendation approach,”ACM Trans. Inf. Syst., vol. 43, no. 5, pp. 114:1–114:37, 2025. [37] Y. Hou, J. Zhang, Z. Lin, H. Lu, R. Xie, J. J. McAuley, and W. X.

**中文**

Larochelle、M. Ranzato、R. Hadsell、M. Balcan 和 H. Lin，编辑，2020。 [35] H. Touvron、T. Lavril、G. Izacard、X. Martinet、M. Lachaux、T. Lacroix、B. Rozi`ere、N. Goyal、E. Hambro、F. Azhar、A. Rodriguez、A. Joulin、E. Grave 和 G. Lample，“Llama：开放高效的基础语言模型”，CoRR，卷。 abs/2302.13971, 2023。 [36] 张建、谢荣、侯勇、赵晓、林林、文建，“推荐作为指令：一种大语言模型赋能的推荐方法”，ACM Trans。信息。系统，卷。 43，没有。 5，第 114:1–114:37，2025。 [37] Y. Hou、J. Zhang、Z. Lin、H. Lu、R. Xie、J. J. McAuley 和 W. X.

### 段落 289 · Page 27

**EN**

Zhao, “Large language models are zeroshot rankers for recommender systems,” inAdvances in Information Retrieval - 46th European Conference on Information Retrieval, ECIR 2024, Glasgow, UK, March 24-28, 2024, Proceedings, Part II, ser. Lecture Notes in Computer Science, N. Goharian, N. Tonellotto, Y. He, A. Lipani, G. McDonald, C. Macdonald, and I. Ounis,

**中文**

赵，“大型语言模型是推荐系统的零样本排序器”，载于信息检索进展 - 第 46 届欧洲信息检索会议，ECIR 2024，英国格拉斯哥，2024 年 3 月 24-28 日，会议记录，第二部分，系列。计算机科学讲义，N. Goharian、N. Tonellotto、Y. He、A. Lipani、G. McDonald、C. Macdonald 和 I. Ounis，

### Page 28

### 段落 290 · Page 28

**EN**

28 Eds., vol. 14609. Springer, 2024, pp. 364–381. [38] Y. Xi, W. Liu, J. Lin, X. Cai, H. Zhu, J. Zhu, B. Chen, R. Tang, W. Zhang, and Y. Yu, “Towards open-world recommendation with knowledge augmentation from large language models,” inProceedings of the 18th ACM Conference on Recommender Systems, RecSys 2024, Bari, Italy, October 14-18, 2024, T. D. Noia, P . Lops, T. Joachims, K. Verbert, P . Castells, Z. Dong, and B. London, Eds. ACM, 2024, pp. 12–22. [39] Z. Zhao, W. Fan, J. Li, Y. Liu, X. Mei, Y. Wang, Z. Wen, F. Wang, X. Zhao, J. Tang, and Q. Li, “Recommender systems in the era of large language models (llms),” IEEE Trans. Knowl.

**中文**

28 编，卷。 14609。施普林格，2024 年，第 364-381 页。 [38] Y. Xi、W. Liu、J. Lin、X. Cai、H. Zhu、J. Zhu、B. Chen、R. Tang、W. Zhang 和 Y. Yu，“通过大语言模型的知识增强实现开放世界推荐”，第 18 届 ACM 推荐系统会议记录，RecSys 2024，意大利巴里，2024 年 10 月 14-18 日，T. D.诺亚，P。洛普斯 (Lops)，T. 约阿希姆斯 (Joachims)，K. 维伯特 (Verbert)，P。 Castells，Z. Dong 和 B. London，编辑。 ACM，2024 年，第 12-22 页。 [39]Z.Zhao，W.Fan，J.Li，Y.Liu，X.Mei，Y.Wang，Z.Wen，F.Wang，X.Zhao，J.Tang，and Q.Li，“大语言模型（llms）时代的推荐系统”，IEEE Trans。知道。

### 段落 291 · Page 28

**EN**

Data Eng., vol. 36, no. 11, pp. 6889– 6907, 2024. [40] S. Wu, O. Irsoy, S. Lu, V . Dabravolski, M. Dredze, S. Gehrmann, P . Kambadur, D. S. Rosenberg, and G. Mann, “Bloomberggpt: A large language model for finance,”CoRR, vol. abs/2303.17564, 2023. [41] J. Li, Y. Liu, W. Fan, X. Wei, H. Liu, J. Tang, and Q. Li, “Empowering molecule discovery for moleculecaption translation with large language models: A chatgpt perspective,”IEEE Trans. Knowl. Data Eng., vol. 36, no. 11, pp. 6071–6083, 2024. [42] J. Wei, Y. Tay, R. Bommasani, C. Raffel, B. Zoph, S. Borgeaud, D. Yogatama, M. Bosma, D. Zhou, D. Metzler, E. H. Chi, T. Hashimoto, O. Vinyals, P .

**中文**

数据工程，卷。 36、没有。 11，第 6889–6907 页，2024。 [40] S. Wu, O. Irsoy, S. Lu, V . Dabravolski，M. Dredze，S. Gehrmann，P。 Kambadur、D. S. Rosenberg 和 G. Mann，“Bloomberggpt：大型金融语言模型”，CoRR，卷。 Abs/2303.17564, 2023。 [41] J. Li、Y. Liu、W. Fan、X. Wei、H. Liu、J. Tang 和 Q. Li，“利用大型语言模型增强分子描述翻译的分子发现：chatgpt 视角”，IEEE Trans。知道。数据工程，卷。 36、没有。 11，第 6071–6083 页，2024 年。 [42] J. Wei、Y. Tay、R. Bommasani、C. Raffel、B. Zoph、S. Borgeaud、D. Yogatama、M. Bosma、D. Zhou、D. Metzler、E. H. Chi、T. Hashimoto、O. Vinyals、P .

### 段落 292 · Page 28

**EN**

Liang, J. Dean, and W. Fedus, “Emergent abilities of large language models,”Trans. Mach. Learn. Res., vol. 2022, 2022. [43] P . Liu, W. Yuan, J. Fu, Z. Jiang, H. Hayashi, and G. Neubig, “Pre-train, prompt, and predict: A systematic survey of prompting methods in natural language processing,”ACM Comput. Surv., vol. 55, no. 9, pp. 195:1–195:35, 2023. [44] X. Qiu, T. Sun, Y. Xu, Y. Shao, N. Dai, and X. Huang, “Pre-trained models for natural language processing: A survey,”CoRR, vol. abs/2003.08271, 2020. [45] Y. Cao, S. Li, Y. Liu, Z. Yan, Y. Dai, P . S. Yu, and L.

**中文**

Liang, J. Dean 和 W. Fedus，“大型语言模型的涌现能力”，Trans。马赫。学习。研究，卷。 2022, 2022. [43] P . Liu、W. Yuan、J. Fu、Z. Jiang、H. Hayashi 和 G. Neubig，“预训练、提示和预测：自然语言处理提示方法的系统调查”，ACM Comput。幸存者，卷。 55，没有。 9，第 195:1–195:35，2023 年。 [44] X. Qiu、T. Sun、Y. Xu、Y. Shao、N. Dai 和 X. Huang，“自然语言处理的预训练模型：一项调查”，CoRR，卷。 abs/2003.08271, 2020. [45] 曹云，李书，刘云，严子，戴云，P. S.于，L.

### 段落 293 · Page 28

**EN**

Sun, “A comprehensive survey of ai-generated content (AIGC): A history of generative AI from GAN to chatgpt,”CoRR, vol. abs/2303.04226, 2023. [46] J. Li, T. Tang, W. X. Zhao, and J. Wen, “Pretrained language model for text generation: A survey,” in Proceedings of the Thirtieth International Joint Conference on Artificial Intelligence, IJCAI 2021, Virtual Event / Montreal, Canada, 19-27 August 2021, Z. Zhou, Ed. ijcai.org, 2021, pp. 4492–4499. [47] Q. Dong, L. Li, D. Dai, C. Zheng, Z. Wu, B. Chang, X. Sun, J. Xu, L. Li, and Z. Sui, “A survey for in-context learning,”CoRR, vol. abs/2301.00234, 2023. [48] J. Huang and K. C.

**中文**

Sun，“人工智能生成内容（AIGC）的全面调查：从 GAN 到 chatgpt 的生成式人工智能的历史”，CoRR，卷。 abs/2303.04226，2023。 [46] J. Li、T. Tang、W. X. Zhu 和 J. Wen，“用于文本生成的预训练语言模型：一项调查”，载于第三十届国际人工智能联合会议论文集，IJCAI 2021，虚拟活动/加拿大蒙特利尔，2021 年 8 月 19-27 日，Z. Zhou，Ed. ijcai.org，2021 年，第 4492–4499 页。 [47] 董强，李丽，戴德，郑成，吴子，张本，孙旭，徐建，李丽，隋子，“情境学习综述”，CoRR，2011， abs/2301.00234, 2023。 [48] J. Huang 和 K. C.

### 段落 294 · Page 28

**EN**

Chang, “Towards reasoning in large language models: A survey,” inFindings of the Association for Computational Linguistics: ACL 2023, Toronto, Canada, July 9-14, 2023, A. Rogers, J. L. Boyd- Graber, and N. Okazaki, Eds. Association for Computational Linguistics, 2023, pp. 1049–1065. [49] W. X. Zhao, K. Zhou, J. Li, T. Tang, X. Wang, Y. Hou, Y. Min, B. Zhang, J. Zhang, Z. Dong, Y. Du, C. Yang, Y. Chen, Z. Chen, J. Jiang, R. Ren, Y. Li, X. Tang, Z. Liu, P . Liu, J. Nie, and J. Wen, “A survey of large language models,”CoRR, vol. abs/2303.18223, 2023. [50] Q. Ai, T. Bai, Z. Cao, Y. Chang, J. Chen, Z. Chen, Z. Cheng, S. Dong, Z. Dou, F. Feng, S.

**中文**

Chang，“走向大型语言模型的推理：一项调查”，载于计算语言学协会的调查结果：ACL 2023，加拿大多伦多，2023 年 7 月 9-14 日，A. Rogers、J. L. Boyd-Graber 和 N. Okazaki，编辑。计算语言学协会，2023 年，第 1049–1065 页。 [49] 赵文新，周坤，李建，唐涛，王旭，侯勇，民民，张本，张建，董子，杜勇，杨成，陈勇，陈志强，江建，任荣，李勇，唐旭，刘正平。刘杰、聂、文，“大语言模型综述”，CoRR，第 1 卷。 abs/2303.18223, 2023. [50] 艾问，白涛，曹志，张勇，陈俊，陈志，程志，董世，窦志，冯峰，世世。

### 段落 295 · Page 28

**EN**

Gao, J. Guo, X. He, Y. Lan, C. Li, Y. Liu, Z. Lyu, W. Ma, J. Ma, Z. Ren, P . Ren, Z. Wang, M. Wang, J. Wen, L. Wu, X. Xin, J. Xu, D. Yin, P . Zhang, F. Zhang, W. Zhang, M. Zhang, and X. Zhu, “Information retrieval meets large language models: A strategic report from chinese IR community,”CoRR, vol. abs/2307.09751, 2023. [51] X. Liu and W. B. Croft, “Statistical language modeling for information retrieval,”Annu. Rev. Inf. Sci. Technol., vol. 39, no. 1, pp. 1–31, 2005. [52] B. Mitra and N. Craswell, “Neural models for information retrieval,”CoRR, vol. abs/1705.01509, 2017. [53] W. X. Zhao, J. Liu, R. Ren, and J.

**中文**

高，郭，X，何，Y，兰，C，李，Y，刘，Z，吕，W，马，J，马，Z，任，P。任，王，王明，文，吴，辛，徐，丁，尹，P。张，F.Zhang，W.Zhang，M.Zhang，X.Zhu，“信息检索遇到大语言模型：来自中国 IR 界的战略报告”，CoRR，第 1 卷。 abs/2307.09751, 2023。 [51] X. Liu 和 W. B. Croft，“信息检索的统计语言建模”，Annu。修订版信息。科学。技术，卷。 39，没有。 1，第 1-31 页，2005 年。 [52] B. Mitra 和 N. Craswell，“信息检索的神经模型”，CoRR，卷。 abs/1705.01509, 2017. [53] 赵文轩, 刘建, 任荣, 等.

### 段落 296 · Page 28

**EN**

Wen, “Dense text retrieval based on pretrained language models: A survey,”ACM Trans. Inf. Syst., vol. 42, no. 4, pp. 89:1– 89:60, 2024. [54] M. E. Peters, M. Neumann, M. Iyyer, M. Gardner, C. Clark, K. Lee, and L. Zettlemoyer, “Deep contextualized word representations,” inProceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, NAACL-HLT 2018, New Orleans, Louisiana, USA, June 1-6, 2018, Volume 1 (Long Papers), M. A. Walker, H. Ji, and A. Stent, Eds. Association for Computational Linguistics, 2018, pp. 2227–2237. [55] J. Devlin, M. Chang, K. Lee, and K.

**中文**

Wen，“基于预训练语言模型的密集文本检索：一项调查”，ACM Trans。信息。系统，卷。 42、没有。 4，第 89:1–89:60，2024 年。 [54] M. E. Peters、M. Neumann、M. Iyyer、M. Gardner、C. Clark、K. Lee 和 L. Zettlemoyer，“深层语境化单词表征”，载于计算语言学协会北美分会 2018 年会议记录：人类语言Technologies，NAACL-HLT 2018，美国路易斯安那州新奥尔良，2018 年 6 月 1-6 日，第 1 卷（长论文），M. A. Walker、H. Ji 和 A. Stent，编辑。计算语言学协会，2018 年，第 2227–2237 页。 [55] J. Devlin、M. Chang、K. Lee 和 K.

### 段落 297 · Page 28

**EN**

Toutanova, “BERT: pre-training of deep bidirectional transformers for language understanding,” inProceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, NAACL-HLT 2019, Minneapolis, MN, USA, June 2-7, 2019, Volume 1 (Long and Short Papers), J. Burstein, C. Doran, and T. Solorio, Eds. Association for Computational Linguistics, 2019, pp. 4171–4186. [56] A. Vaswani, N. Shazeer, N. Parmar, J. Uszkoreit, L. Jones, A. N. Gomez, L. Kaiser, and I.

**中文**

Toutanova，“BERT：用于语言理解的深度双向Transformer的预训练”，载于计算语言学协会北美分会 2019 年会议记录：人类语言技术，NAACL-HLT 2019，美国明尼苏达州明尼阿波利斯，2019 年 6 月 2-7 日，第 1 卷（长论文和短论文），J. Burstein、C. Doran 和T.索洛里奥，编辑。计算语言学协会，2019 年，第 4171–4186 页。 [56] A. Vaswani、N. Shazeer、N. Parmar、J. Uszkoreit、L. Jones、A. N. Gomez、L. Kaiser 和 I。

### 段落 298 · Page 28

**EN**

Polosukhin, “Attention is all you need,” inAdvances in Neural Information Processing Systems 30: Annual Conference on Neural Information Processing Systems 2017, December 4-9, 2017, Long Beach, CA, USA, I. Guyon, U. von Luxburg, S. Bengio, H. M. Wallach, R. Fergus, S. V . N. Vishwanathan, and R. Garnett, Eds., 2017, pp. 5998– 6008. [57] M. Lewis, Y. Liu, N. Goyal, M. Ghazvininejad, A. Mohamed, O. Levy, V . Stoyanov, and L.

**中文**

Polosukhin，“注意力就是你所需要的”，载于《神经信息处理系统进展 30：2017 年神经信息处理系统年会》，2017 年 12 月 4-9 日，美国加利福尼亚州长滩，I. Guyon、U. von Luxburg、S. Bengio、H. M. Wallach、R. Fergus、S. V . N. Vishwanathan 和 R. Garnett，编辑，2017 年，第 5998–6008 页。 [57] M. Lewis、Y. Liu、N. Goyal、M. Ghazvininejad、A. Mohamed、O. Levy、V .斯托扬诺夫，L.

### 段落 299 · Page 28

**EN**

Zettlemoyer, “BART: denoising sequence-to-sequence pre-training for natural language generation, translation, and comprehension,” inProceedings of the 58th Annual Meeting of the Association for Computational Linguistics, ACL 2020, Online, July 5-10, 2020, D. Jurafsky, J. Chai, N. Schluter, and J. R. Tetreault, Eds. Association for Computational Linguistics, 2020, pp. 7871–7880. [58] C. Raffel, N. Shazeer, A. Roberts, K. Lee, S. Narang, M. Matena, Y. Zhou, W. Li, and P . J. Liu, “Exploring the limits of transfer learning with a unified text-totext transformer,”J. Mach. Learn. Res., vol. 21, pp. 140:1–140:67, 2020. [59] J. Kaplan, S.

**中文**

Zettlemoyer，“BART：用于自然语言生成、翻译和理解的去噪序列到序列预训练”，计算语言学协会第 58 届年会记录，ACL 2020，在线，2020 年 7 月 5 日至 10 日，D. Jurafsky、J. Chai、N. Schluter 和 J. R. Tetreault，编辑。计算语言学协会，2020 年，第 7871–7880 页。 [58] C. Raffel、N. Shazeer、A. Roberts、K. Lee、S. Narang、M. Matena、Y. Zhou、W. Li 和 P。 J. Liu，“利用统一的文本到文本转换器探索迁移学习的局限性”，J.马赫。学习。研究，卷。 21，第 140:1–140:67，2020 年。[59] J. Kaplan, S.

### 段落 300 · Page 28

**EN**

McCandlish, T. Henighan, T. B. Brown, B. Chess, R. Child, S. Gray, A. Radford, J. Wu, and D. Amodei, “Scaling laws for neural language mod-

**中文**

McCandlish、T. Henighan、T. B. Brown、B. Chess、R. Child、S. Gray、A. Radford、J. Wu 和 D. Amodei，“神经语言模型的缩放法则”

### Page 29

### 段落 301 · Page 29

**EN**

29 els,”CoRR, vol. abs/2001.08361, 2020. [60] A. Clark, D. de Las Casas, A. Guy, A. Mensch, M. Paganini, J. Hoffmann, B. Damoc, B. A. Hechtman, T. Cai, S. Borgeaud, G. van den Driessche, E. Rutherford, T. Hennigan, M. J. Johnson, A. Cassirer, C. Jones, E. Buchatskaya, D. Budden, L. Sifre, S. Osindero, O. Vinyals, M. Ranzato, J. W. Rae, E. Elsen, K. Kavukcuoglu, and K. Simonyan, “Unified scaling laws for routed language models,” inInternational Conference on Machine Learning, ICML 2022, 17-23 July 2022, Baltimore, Maryland, USA, ser. Proceedings of Machine Learning Research, K. Chaudhuri, S. Jegelka, L. Song, C. Szepesv ´ari, G. Niu, and S.

**中文**

29 els，”CoRR，卷。 abs/2001.08361，2020。[60] A. Clark、D. de Las Casas、A. Guy、A. Mensch、M. Paganini、J. Hoffmann、B. Damoc、B. A. Hechtman、T. Cai、S. Borgeaud、G. van den Driessche、E. Rutherford、T. Hennigan、M. J. Johnson、A. Cassirer、C. Jones、E. Buchatskaya、D. Budden、L. Sifre、S. Osindero、O. Vinyals、M. Ranzato、J. W. Rae、E. Elsen、K. Kavukcuoglu 和 K. Simonyan，“路由语言模型的统一缩放法则”，发表于国际机器学习会议，ICML 2022，2022 年 7 月 17-23 日，美国马里兰州巴尔的摩，ser。机器学习研究论文集，K. Chaudhuri、S. Jegelka、L. Song、C. Szepesv ´ari、G. Niu 和 S.

### 段落 302 · Page 29

**EN**

Sabato, Eds., vol. 162. PMLR, 2022, pp. 4057–4086. [61] E. J. Hu, Y. Shen, P . Wallis, Z. Allen-Zhu, Y. Li, S. Wang, L. Wang, and W. Chen, “Lora: Low-rank adaptation of large language models,” inThe Tenth International Conference on Learning Representations, ICLR 2022, Virtual Event, April 25-29, 2022. OpenReview.net, 2022. [62] X. L. Li and P .

**中文**

萨巴托，编辑，卷。 162.PMLR，2022 年，第 4057-4086 页。 [61] 胡 E. J.，沉 Y. P ． Wallis、Z. Allen-Zhu、Y. Li、S. Wang、L. Wang 和 W. Chen，“Lora：大型语言模型的低阶适应”，载于第十届学习表示国际会议，ICLR 2022，虚拟活动，2022 年 4 月 25-29 日。OpenReview.net，2022 年。[62] X. L. Li 和 P .

### 段落 303 · Page 29

**EN**

Liang, “Prefix-tuning: Optimizing continuous prompts for generation,” inProceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing, ACL/IJCNLP 2021, (Volume 1: Long Papers), Virtual Event, August 1- 6, 2021, C. Zong, F. Xia, W. Li, and R. Navigli, Eds. Association for Computational Linguistics, 2021, pp. 4582–4597. [63] B. Lester, R. Al-Rfou, and N.

**中文**

梁，“前缀调整：优化生成连续提示”，载于计算语言学协会第 59 届年会和第 11 届自然语言处理国际联合会议论文集，ACL/IJCNLP 2021，（第一卷：长论文），虚拟活动，2021 年 8 月 1-6 日，C. Zong、F. Xia、W. Li 和 R.纳维利，编辑。计算语言学协会，2021 年，第 4582–4597 页。 [63] B. Lester、R. Al-Rfou 和 N.

### 段落 304 · Page 29

**EN**

Constant, “The power of scale for parameter-efficient prompt tuning,” in Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing, EMNLP 2021, Virtual Event / Punta Cana, Dominican Republic, 7-11 November, 2021, M. Moens, X. Huang, L. Specia, and S. W. Yih, Eds. Association for Computational Linguistics, 2021, pp. 3045–3059. [64] T. Dettmers, A. Pagnoni, A. Holtzman, and L.

**中文**

Constant，“参数高效提示调整的规模力量”，收录于 2021 年自然语言处理经验方法会议论文集，EMNLP 2021，虚拟活动/多米尼加共和国蓬塔卡纳，2021 年 11 月 7-11 日，M. Moens、X. Huang、L. Specia 和 S. W. Yih，编辑。计算语言学协会，2021 年，第 3045–3059 页。 [64] T. Dettmers、A. Pagnoni、A. Holtzman 和 L.

### 段落 305 · Page 29

**EN**

Zettlemoyer, “Qlora: Efficient finetuning of quantized llms,” inAdvances in Neural Information Processing Systems 36: Annual Conference on Neural Information Processing Systems 2023, NeurIPS 2023, New Orleans, LA, USA, December 10 - 16, 2023, A. Oh, T. Naumann, A. Globerson, K. Saenko, M. Hardt, and S. Levine, Eds., 2023. [65] L. Wang, N. Yang, and F. Wei, “Query2doc: Query expansion with large language models,” pp. 9414– 9423, 2023. [66] H. K. Azad and A. Deepak, “Query expansion techniques for information retrieval: A survey,”Inf. Process. Manag., vol. 56, no. 5, pp. 1698–1735, 2019. [67] H. J. Peat and P .

**中文**

Zettlemoyer，“Qlora：量化 llms 的高效微调”，《神经信息处理系统进展 36：2023 年神经信息处理系统年会》，NeurIPS 2023，美国洛杉矶新奥尔良，2023 年 12 月 10 日至 16 日，A. Oh、T. Naumann、A. Globerson、K. Saenko、M. Hardt 和 S. Levine，Eds.，2023。 [65] L. Wang、N. Yang 和 F. Wei，“Query2doc：大型语言模型的查询扩展”，第 9414-9423 页，2023。 [66] H. K. Azad 和 A. Deepak，“信息检索的查询扩展技术：一项调查”，Inf。过程。管理，卷。 56，没有。 5，第 1698–1735 页，2019 年。 [67] H. J. Peat 和 P .

### 段落 306 · Page 29

**EN**

Willett, “The limitations of term co-occurrence data for query expansion in document retrieval systems,”J. Am. Soc. Inf. Sci., vol. 42, no. 5, pp. 378–383, 1991. [68] C. Fellbaum, “Wordnet: An electronic lexical database,”MIT Press google schola, vol. 2, pp. 678–686, 1998. [69] E. A. Fox, “Lexical relations: Enhancing effectiveness of information retrieval systems,”SIGIR Forum, vol. 15, no. 3, pp. 5–36, 1980. [70] H. Zohar, C. Liebeskind, J. Schler, and I. Dagan, “Automatic thesaurus construction for cross generation corpus,”ACM Journal on Computing and Cultural Heritage, vol. 6, no. 1, pp. 4:1–4:19, 2013. [71] S. Gauch, J. Wang, and S. M.

**中文**

Willett，“文档检索系统中查询扩展的术语共现数据的局限性”，J.是。苏克。信息。科学，卷。 42、没有。 5，第 378–383 页，1991 年。 [68] C. Fellbaum，“Wordnet：电子词汇数据库”，麻省理工学院出版社 google schola，卷。 2，第 678–686 页，1998 年。 [69] E. A. Fox，“词汇关系：增强信息检索系统的有效性”，SIGIR 论坛，第 1 卷。 15、没有。 3，第 5-36 页，1980 年。 [70] H. Zohar、C. Liebeskind、J. Schler 和 I. Dagan，“跨代语料库的自动同义词库构建”，ACM 计算与文化遗产杂志，卷。 6、没有。 1，第 4:1–4:19，2013 年。 [71] S. Gauch、J. Wang 和 S. M.

### 段落 307 · Page 29

**EN**

Rachakonda, “A corpus analysis approach for automatic query expansion and its extension to multiple databases,”ACM Trans. Inf. Syst., vol. 17, no. 3, pp. 250–269, 1999. [72] Y. Li, W. P . R. Luk, K. S. E. Ho, and F. L. K. Chung, “Improving weak ad-hoc queries using wikipedia asexternal corpus,” inProceedings of the 30th annual international ACM SIGIR conference on Research and development in information retrieval, 2007, pp. 797–798. [73] C. Xiong and J.

**中文**

Rachakonda，“一种用于自动查询扩展及其扩展到多个数据库的语料库分析方法”，ACM Trans。信息。系统，卷。 17、没有。 3，第250-269页，1999。 [72] Y. Li, W. P. R. Luk、K. S. E. Ho 和 F. L. K. Chung，“使用维基百科作为外部语料库改进弱即席查询”，第 30 届国际 ACM SIGIR 信息检索研究与开发年度会议记录，2007 年，第 797-798 页。 [73] C.熊和J.

### 段落 308 · Page 29

**EN**

Callan, “Query expansion with freebase,” inProceedings of the 2015 International Conference on The Theory of Information Retrieval, ICTIR 2015, Northampton, Massachusetts, USA, September 27- 30, 2015, J. Allan, W. B. Croft, A. P . de Vries, and C. Zhai, Eds. ACM, 2015, pp. 111–120. [74] J. Singh and A. Sharan, “A new fuzzy logic-based query expansion model for efficient information retrieval using relevance feedback approach,”Neural Comput. Appl., vol. 28, no. 9, pp. 2557–2580, 2017. [75] L. Gao, X. Ma, J. Lin, and J. Callan, “Precise zero-shot dense retrieval without relevance labels,”CoRR, vol. abs/2212.10496, 2022. [76] R. Jagerman, H.

**中文**

Callan，“使用 freebase 进行查询扩展”，2015 年信息检索理论国际会议记录，ICTIR 2015，美国马萨诸塞州北安普顿，2015 年 9 月 27-30 日，J. Allan、W. B. Croft、A. P. de Vries 和 C. Zhai，编辑。 ACM，2015 年，第 111-120 页。 [74] J. Singh 和 A. Sharan，“一种新的基于模糊逻辑的查询扩展模型，用于使用相关反馈方法进行高效信息检索”，神经计算。应用，卷。 28、没有。 9，第 2557–2580 页，2017 年。 [75] L. 高、X. Ma、J. Lin 和 J. Callan，“无相关标签的精确零样本密集检索”，CoRR，卷。绝对/2212.10496，2022。[76] R.贾格曼，H.

### 段落 309 · Page 29

**EN**

Zhuang, Z. Qin, X. Wang, and M. Bendersky, “Query expansion by prompting large language models,”CoRR, vol. abs/2305.03653, 2023. [77] I. Baek, J. Lee, J. Yang, and H. Lee, “Crafting the path: Robust query rewriting for information retrieval,” IEEE Access, vol. 13, pp. 24 171–24 180, 2025. [78] M. Alaofi, L. Gallagher, M. Sanderson, F. Scholer, and P . Thomas, “Can generative llms create query variants for test collections? an exploratory study,” inProceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2023, Taipei, Taiwan, July 23-27, 2023, H. Chen, W. E. Duh, H. Huang, M. P .

**中文**

Zhuang，Z.Qin，X.Wang，M.Bendersky，“通过提示大语言模型进行查询扩展”，CoRR，卷。 abs/2305.03653, 2023。 [77] I. Baek、J. Lee、J. Yang 和 H. Lee，“精心设计路径：用于信息检索的鲁棒查询重写”，IEEE Access，卷。 13，第 24 171–24 180 页，2025。 [78] M. Alaofi、L. Gallagher、M. Sanderson、F. Scholer 和 P . Thomas，“生成式 llms 能否为测试集合创建查询变体？一项探索性研究”，载于第 46 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR 2023，台湾台北，2023 年 7 月 23-27 日，H. Chen、W. E. Duh、H. Huang、M. P.

### 段落 310 · Page 29

**EN**

Kato, J. Mothe, and B. Poblete, Eds. ACM, 2023, pp. 1869–1873. [79] M. Li, H. Zhuang, K. Hui, Z. Qin, J. Lin, R. Jagerman, X. Wang, and M. Bendersky, “Can query expansion improve generalization of strong cross-encoder rankers?” inProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2024, Washington DC, USA, July 14-18, 2024, G. H. Yang, H. Wang, S. Han, C. Hauff, G. Zuccon, and Y. Zhang, Eds. ACM, 2024, pp. 2321– 2326. [80] X. Ma, Y. Gong, P . He, H. Zhao, and N. Duan, “Query rewriting for retrieval-augmented large language models,”CoRR, vol. abs/2305.14283, 2023. [81] W.

**中文**

Kato，J. Mothe 和 B. Poblete，编辑。 ACM，2023 年，第 1869–1873 页。 [79] M. Li、H. Zhuang、K. Hui、Z.qin、J. Lin、R. Jagerman、X. Wang 和 M. Bendersky，“查询扩展能否提高强跨编码器排序器的泛化能力？”第 47 届国际 ACM SIGIR 信息检索研究与开发会议记录，SIGIR 2024，美国华盛顿特区，2024 年 7 月 14-18 日，G. H. Yang、H. Wang、S. Han、C. Hauff、G. Zuccon 和 Y. Zhu，编辑。 ACM，2024，第 2321–2326 页。 [80] 马晓霞，龚勇平。他，H.Zhao，和N.Duan，“检索增强大型语言模型的查询重写”，CoRR，卷。绝对/2305.14283，2023。[81] W.

### 段落 311 · Page 29

**EN**

Peng, G. Li, Y. Jiang, Z. Wang, D. Ou, X. Zeng, D. Xu, T. Xu, and E. Chen, “Large language model based long-tail query rewriting in taobao search,” in Companion Proceedings of the ACM on Web Conference 2024, WWW 2024, Singapore, Singapore, May 13-17, 2024, T. Chua, C. Ngo, R. K. Lee, R. Kumar, and H. W. Lauw, Eds. ACM, 2024, pp. 20–28. [82] I. Mackie, S. Chatterjee, and J. Dalton, “Generative and pseudo-relevant feedback for sparse, dense and learned sparse retrieval,”CoRR, vol. abs/2305.07477, 2023.

**中文**

Peng、G. Li、Y. Jiang、Z. Wang、D. Ou、X. Zeng、D. Xu、T. Xu 和 E. Chen，“淘宝搜索中基于大语言模型的长尾查询重写”，ACM on Web Conference 2024 配套论文集，WWW 2024，新加坡，新加坡，2024 年 5 月 13-17 日，T. Chua, C. Ngo， R.K. Lee、R. Kumar 和 H. W. Lauw，编辑。 ACM，2024 年，第 20-28 页。 [82] I. Mackie、S. Chatterjee 和 J. Dalton，“稀疏、密集和学习稀疏检索的生成和伪相关反馈”，CoRR，卷。绝对/2305.07477，2023。

### Page 30

### 段落 312 · Page 30

**EN**

30 [83] I. Mackie, I. Sekulic, S. Chatterjee, J. Dalton, and F. Crestani, “GRM: generative relevance modeling using relevance-aware sample estimation for document retrieval,”CoRR, vol. abs/2306.09938, 2023. [84] J. Feng, C. Tao, X. Geng, T. Shen, C. Xu, G. Long, D. Zhao, and D. Jiang, “Knowledge refinement via interaction between search engines and large language models,”CoRR, vol. abs/2305.07402, 2023. [85] T. Shen, G. Long, X. Geng, C. Tao, Y. Lei, T. Zhou, M. Blumenstein, and D.

**中文**

30 [83] I. Mackie、I. Sekulic、S. Chatterjee、J. Dalton 和 F. Crestani，“GRM：使用相关性感知样本估计进行文档检索的生成相关性建模”，CoRR，卷。 Abs/2306.09938, 2023。 [84] J. Feng, C. Tao, X. Geng, T. Shen, C. Xu, G. Long, D. Zhao, and D. Jiang, “通过搜索引擎和大型语言模型之间的交互进行知识精炼，”CoRR，卷。 abs/2305.07402, 2023. [85] T. Shen, G. Long, X. Geng, C. Tao, Y. Lei, T. Zhou, M. Blumenstein, and D.

### 段落 313 · Page 30

**EN**

Jiang, “Retrieval-augmented retrieval: Large language models are strong zero-shot retriever,” inFindings of the Association for Computational Linguistics, ACL 2024, Bangkok, Thailand and virtual meeting, August 11-16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 15 933–15 946. [86] Y. Lei, Y. Cao, T. Zhou, T. Shen, and A. Yates, “Corpussteered query expansion with large language models,” inProceedings of the 18th Conference of the European Chapter of the Association for Computational Linguistics, EACL 2024 - Volume 2: Short Papers, St. Julian’s, Malta, March 17-22, 2024, Y. Graham and M.

**中文**

Jiang，“检索增强检索：大型语言模型是强大的零样本检索器”，载于计算语言学协会的调查结果，ACL 2024，泰国曼谷和虚拟会议，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V。斯里库马尔，编辑。计算语言学协会，2024 年，第 15 933–15 946 页。 [86] Y. Lei、Y. Cao、T. Zhou、T. Shen 和 A. Yates，“Corpussteered 查询扩展与大型语言模型”，载于计算语言学协会欧洲分会第 18 届会议记录，EACL 2024 - 卷2：短论文，马耳他圣朱利安，2024 年 3 月 17-22 日，Y. Graham 和 M.

### 段落 314 · Page 30

**EN**

Purver, Eds. Association for Computational Linguistics, 2024, pp. 393–401. [87] A. Anand, V . V , V . Setty, and A. Anand, “Context aware query rewriting for text rankers using LLM,” CoRR, vol. abs/2308.16753, 2023. [88] S. Mao, Y. Jiang, B. Chen, X. Li, P . Wang, X. Wang, P . Xie, F. Huang, H. Chen, and N. Zhang, “Rafe: Ranking feedback improves query rewriting for RAG,” in Findings of the Association for Computational Linguistics: EMNLP 2024, Miami, Florida, USA, November 12-16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 884–901. [89] K. Mao, Z. Dou, F. Mo, J. Hou, H. Chen, and H.

**中文**

普弗，编辑。计算语言学协会，2024 年，第 393-401 页。 [87] A.阿南德，V。 V , V . Setty 和 A. Anand，“使用 LLM 对文本排序器进行上下文感知查询重写”，CoRR，卷。 abs/2308.16753, 2023. [88] 毛三，姜玉，陈本，李晓，P.王X. 王P. Xie、F. Huang、H. Chen 和 N. Zhang，“Rafe：排名反馈改进了 RAG 的查询重写”，计算语言学协会的调查结果：EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 884-901 页。 [89] 毛坤，窦正，莫凤，侯建，陈浩，陈浩，

### 段落 315 · Page 30

**EN**

Qian, “Large language models know your contextual search intent: A prompting framework for conversational search,” inFindings of the Association for Computational Linguistics: EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 1211– 1225. [90] C. Huang, C. Hsu, T. Hsu, C. Li, and Y. Chen, “CON- VERSER: few-shot conversational dense retrieval with synthetic data generation,” inProceedings of the 24th Meeting of the Special Interest Group on Discourse and Dialogue, SIGDIAL 2023, Prague, Czechia, September 11 - 15, 2023, D. Schlangen, S. Stoyanchev, S. Joty, O.

**中文**

Qian，“大型语言模型了解您的上下文搜索意图：会话搜索的提示框架”，载于计算语言学协会的调查结果：EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 1211-1225 页。 [90] C. Huang、C. Hsu、T. Hsu、C. Li 和 Y. Chen，“CONVERSER：使用合成数据生成的少样本会话密集检索”，载于第 24 届话语和对话特别兴趣小组会议记录，SIGDIAL 2023，布拉格，捷克，2023 年 9 月 11 日至 15 日，D. Schlangen、S. Stoyanchev、S. Joty、O.

### 段落 316 · Page 30

**EN**

Dusek, C. Kennington, and M. Alikhani, Eds. Association for Computational Linguistics, 2023, pp. 381–387. [91] F. Ye, M. Fang, S. Li, and E. Yilmaz, “Enhancing conversational search: Large language model-aided informative query rewriting,” inFindings of the Association for Computational Linguistics: EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 5985–6006. [92] K. Mao, Z. Dou, H. Qian, F. Mo, X. Cheng, and Z.

**中文**

Dusek、C. Kennington 和 M. Alikhani，编辑。计算语言学协会，2023 年，第 381-387 页。 [91] F. Ye、M. Fang、S. Li 和 E. Yilmaz，“增强会话搜索：大型语言模型辅助信息查询重写”，载于计算语言学协会调查结果：EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 5985–6006 页。 [92] 毛坤，窦正，钱红，莫凤，程旭，Z.

### 段落 317 · Page 30

**EN**

Cao, “Convtrans: Transforming web search sessions for conversational dense retrieval,” inProceedings of the 2022 Conference on Empirical Methods in Natural Language Processing, EMNLP 2022, Abu Dhabi, United Arab Emirates, December 7-11, 2022, Y. Goldberg, Z. Kozareva, and Y. Zhang, Eds. Association for Computational Linguistics, 2022, pp. 2935–2946. [93] Z. Dai, A. T. Chaganty, V . Y. Zhao, A. Amini, Q. M. Rashid, M. Green, and K. Guu, “Dialog inpainting: Turning documents into dialogs,” inInternational Conference on Machine Learning, ICML 2022, 17-23 July 2022, Baltimore, Maryland, USA, ser. Proceedings of Machine Learning Research, K.

**中文**

Cao，“Convtrans：将网络搜索会话转变为会话式密集检索”，载于 2022 年自然语言处理经验方法会议论文集，EMNLP 2022，阿拉伯联合酋长国阿布扎比，2022 年 12 月 7-11 日，Y. Goldberg、Z. Kozareva 和 Y. Zhang，编辑。计算语言学协会，2022 年，第 2935-2946 页。 [93] Z. Dai，A. T. Chaganty，V。 Y. Zhao、A. Amini、Q. M. Rashid、M. Green 和 K. Guu，“对话修复：将文档转变为对话”，国际机器学习会议，ICML 2022，2022 年 7 月 17-23 日，美国马里兰州巴尔的摩，ser。机器学习研究论文集，K.

### 段落 318 · Page 30

**EN**

Chaudhuri, S. Jegelka, L. Song, C. Szepesv ´ari, G. Niu, and S. Sabato, Eds., vol. 162. PMLR, 2022, pp. 4558–4586. [94] Y. Chen, J. Yoon, D. S. Sachan, Q. Wang, V . Cohen- Addad, M. Bateni, C. Lee, and T. Pfister, “Re-invoke: Tool invocation rewriting for zero-shot tool retrieval,” inFindings of the Association for Computational Linguistics: EMNLP 2024, Miami, Florida, USA, November 12- 16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 4705–4726. [95] Y. Fan, Y. Zhu, K. Xue, J. Liu, and T.

**中文**

Chaudhuri、S. Jegelka、L. Song、C. Szepesv ´ari、G. Niu 和 S. Sabato，编辑，卷。 162.PMLR，2022 年，第 4558–4586 页。 [94] Y. Chen，J. Yoon，D. S. Sachan，Q. Wang，V。 Cohen-Addad、M. Bateni、C. Lee 和 T. Pfister，“重新调用：零样本工具检索的工具调用重写”，计算语言学协会的调查结果：EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 4705–4726 页。 [95] 范Y.，朱Y.，薛K.，J.刘，T.

### 段落 319 · Page 30

**EN**

Ruan, “Rrnorm: A novel framework for chinese disease diagnoses normalization via llm-driven terminology component recognition and reconstruction,” inFindings of the Association for Computational Linguistics, ACL 2024, Bangkok, Thailand and virtual meeting, August 11-16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 9162– 9175. [96] K. D. Dhole, R. Chandradevan, and E. Agichtein, “An interactive query generation assistant using llm-based prompt modification and user feedback,”CoRR, vol. abs/2311.11226, 2023. [97] R. Wilson, C. Carter, and C.

**中文**

Ruan，“Rrnorm：通过 llm 驱动的术语组件识别和重建实现中国疾病诊断标准化的新框架”，载于计算语言学协会的调查结果，ACL 2024，泰国曼谷和虚拟会议，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V。斯里库马尔，编辑。计算语言学协会，2024 年，第 9162–9175 页。 [96] K. D. Dhole、R. Chandradevan 和 E. Agichtein，“使用基于 llm 的提示修改和用户反馈的交互式查询生成助手”，CoRR，卷。 abs/2311.11226, 2023。 [97] R. Wilson、C. Carter 和 C.

### 段落 320 · Page 30

**EN**

Graham, “Contextualizing search queries in-context learning for conversational rewriting with llms,”CoRR, vol. abs/2502.15009, 2025. [98] C. Deng, K. Mao, and Z. Dou, “Learning interpretable legal case retrieval via knowledge-guided case reformulation,” inProceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, EMNLP 2024, Miami, FL, USA, November 12-16, 2024, Y. Al- Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 1253–1265. [99] M. Li, H. Zhuang, K. Hui, Z. Qin, J. Lin, R. Jagerman, X. Wang, and M.

**中文**

Graham，“使用 llms 将搜索查询置于上下文学习中进行对话重写”，CoRR，卷。 abs/2502.15009, 2025。 [98] C. Deng、K. Mao 和 Z. Dou，“通过知识引导的案例重构学习可解释的法律案例检索”，载于 2024 年自然语言处理经验方法会议论文集，EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al- Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 1253–1265 页。 [99] M. Li，H. Zhuang，K. Hui，Z.qin，J. Lin，R. Jagerman，X. Wang，and M.

### 段落 321 · Page 30

**EN**

Bendersky, “Generate, filter, and fuse: Query expansion via multi-step keyword generation for zero-shot neural rankers,”CoRR, vol. abs/2311.09175, 2023. [100] J. Wei, X. Wang, D. Schuurmans, M. Bosma, B. Ichter, F. Xia, E. H. Chi, Q. V . Le, and D. Zhou, “Chain-ofthought prompting elicits reasoning in large language models,” inNeurIPS, 2022. [101] W. Yu, D. Iter, S. Wang, Y. Xu, M. Ju, S. Sanyal, C. Zhu, M. Zeng, and M. Jiang, “Generate rather than retrieve: Large language models are strong context generators,” inThe Eleventh International Conference on Learning Representations, ICLR 2023, Kigali, Rwanda, May 1-5, 2023. OpenReview.net, 2023.

**中文**

Bendersky，“生成、过滤和融合：通过零样本神经排序器的多步关键字生成进行查询扩展”，CoRR，卷。 abs/2311.09175, 2023. [100] J. Wei, X. Wang, D. Schuurmans, M. Bosma, B. Ichter, F. Xia, E. H. Chi, Q. V. Le 和 D. Zhou，“思想链提示在大型语言模型中引发推理”，NeurIPS，2022。 [101] W. Yu、D. Iter、S. Wang、Y. Xu、M. Ju、S. Sanyal、C. Zhu、M. Zeng 和 M. Jiang，“生成而不是检索：大型语言模型是强大的上下文生成器”，载于第十一届学习表示国际会议，ICLR 2023 年，卢旺达基加利，2023 年 5 月 1-5 日。OpenReview.net，2023 年。

### 段落 322 · Page 30

**EN**

[102] T. Nguyen, M. Rosenberg, X. Song, J. Gao, S. Tiwary,

**中文**

[102] T. Nguyen、M. Rosenberg、X. Song、J. 高、S. Tiwary，

### Page 31

### 段落 323 · Page 31

**EN**

31 R. Majumder, and L. Deng, “MS MARCO: A human generated machine reading comprehension dataset,” inCoCo@NIPS, ser. CEUR Workshop Proceedings, vol. 1773. CEUR-WS.org, 2016. [103] T. Kwiatkowski, J. Palomaki, O. Redfield, M. Collins, A. P . Parikh, C. Alberti, D. Epstein, I. Polosukhin, J. Devlin, K. Lee, K. Toutanova, L. Jones, M. Kelcey, M. Chang, A. M. Dai, J. Uszkoreit, Q. Le, and S. Petrov, “Natural questions: a benchmark for question answering research,”Trans. Assoc. Comput. Linguistics, vol. 7, pp. 452–466, 2019. [104] Y. Wu, Y. Huang, N. Hu, Y. Hua, G. Qi, J. Chen, and J. Z.

**中文**

31 R. Majumder 和 L. Deng，“MS MARCO：人类生成的机器阅读理解数据集”，inCoCo@NIPS，ser。 CEUR 研讨会论文集，卷。 1773. CEUR-WS.org，2016。[103] T. Kwiatkowski、J. Palomaki、O. Redfield、M. Collins、A. P. Parikh、C. Alberti、D. Epstein、I. Polosukhin、J. Devlin、K. Lee、K. Toutanova、L. Jones、M. Kelcey、M. Chang、A. M. Dai、J. Uszkoreit、Q. Le 和 S. Petrov，“自然问题：问答研究的基准”，Trans。副教授。计算。语言学，卷。 7，第452-466页，2019。 [104] Y. Wu，Y. Huang，N. Hu，Y. Hua，G. Qi，J. Chen，J. Z.

### 段落 324 · Page 31

**EN**

Pan, “Cotkr: Chain-of-thought enhanced knowledge rewriting for complex knowledge graph question answering,” inProceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, EMNLP 2024, Miami, FL, USA, November 12- 16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 3501–3520. [105] I. Baek, J. Lee, J. Yang, and H. Lee, “Crafting the path: Robust query rewriting for information retrieval,” IEEE Access, vol. 13, pp. 24 171–24 180, 2025. [106] R. Rafailov, A. Sharma, E. Mitchell, C. D. Manning, S. Ermon, and C.

**中文**

Pan，“Cotkr：复杂知识图问答的思想链增强知识重写”，载于 2024 年自然语言处理经验方法会议论文集，EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 3501–3520 页。 [105] I. Baek、J. Lee、J. Yang 和 H. Lee，“精心设计路径：用于信息检索的鲁棒查询重写”，IEEE Access，卷。 13，第 24 171–24 180 页，2025。 [106] R. Rafailov、A. Sharma、E. Mitchell、C. D. Manning、S. Ermon 和 C.

### 段落 325 · Page 31

**EN**

Finn, “Direct preference optimization: Your language model is secretly a reward model,” inAdvances in Neural Information Processing Systems 36: Annual Conference on Neural Information Processing Systems 2023, NeurIPS 2023, New Orleans, LA, USA, December 10 - 16, 2023, A. Oh, T. Naumann, A. Globerson, K. Saenko, M. Hardt, and S. Levine, Eds., 2023. [107] DeepSeek-AI, D. Guo, D. Yang, H. Zhang, J. Song, R. Zhang, R. Xu, Q. Zhu, S. Ma, P . Wang, X. Bi, X. Zhang, X. Yu, Y. Wu, Z. F. Wu, Z. Gou, Z. Shao, Z. Li, Z. Gao, A. Liu, B. Xue, B. Wang, B. Wu, B. Feng, C. Lu, C. Zhao, C. Deng, C. Zhang, C. Ruan, D. Dai, D. Chen, D. Ji, E. Li, F. Lin, F.

**中文**

Finn，“直接偏好优化：你的语言模型实际上是一个奖励模型”，载于《神经信息处理系统进展 36：2023 年神经信息处理系统年会》，NeurIPS 2023，美国洛杉矶新奥尔良，2023 年 12 月 10 日至 16 日，A. Oh、T. Naumann、A. Globerson、K. Saenko、M. Hardt 和 S. Levine，编辑， 2023. [107] DeepSeek-AI，D.郭，D.杨，H.张，J.宋，R.张，R.徐，Q.朱，S.马，P.王X.毕、X.张、X.余、Y.吴、Z.F.吴、Z.苟、Z.邵、Z.李、Z.高、A.刘、B.薛、B.王、B.吴、B.冯、C.陆、C.赵、C.邓、C.张、C.阮、D.戴、D.陈、D.季、E.李、F.林、F.

### 段落 326 · Page 31

**EN**

Dai, F. Luo, G. Hao, G. Chen, G. Li, H. Zhang, H. Bao, H. Xu, H. Wang, H. Ding, H. Xin, H. Gao, H. Qu, H. Li, J. Guo, J. Li, J. Wang, J. Chen, J. Yuan, J. Qiu, J. Li, J. L. Cai, J. Ni, J. Liang, J. Chen, K. Dong, K. Hu, K. Gao, K. Guan, K. Huang, K. Yu, L. Wang, L. Zhang, L. Zhao, L. Wang, L. Zhang, L. Xu, L. Xia, M. Zhang, M. Zhang, M. Tang, M. Li, M. Wang, M. Li, N. Tian, P . Huang, P . Zhang, Q. Wang, Q. Chen, Q. Du, R. Ge, R. Zhang, R. Pan, R. Wang, R. J. Chen, R. L. Jin, R. Chen, S. Lu, S. Zhou, S. Chen, S. Ye, S. Wang, S. Yu, S. Zhou, S. Pan, and S. S.

**中文**

戴、罗、浩、陈、高、李、张、包、徐、王、丁、辛、高、曲、李、郭、李、王、陈、袁、邱、李、蔡、倪、梁、陈、董、胡、高、K.关，黄，余K.，王丽，张丽，赵丽，王丽，张丽，徐丽，夏丽，张明，张明，唐明，李明，王明，李明，田宁，P．黄P.张、王、陈、、杜、葛、张、潘、王、陈、金、陈、陆、周、陈、叶、王、于、周、潘、宋

### 段落 327 · Page 31

**EN**

Li, “Deepseek-r1: Incentivizing reasoning capability in llms via reinforcement learning,”CoRR, vol. abs/2501.12948, 2025. [108] P . Jiang, J. Lin, L. Cao, R. Tian, S. Kang, Z. Wang, J. Sun, and J. Han, “Deepretrieval: Hacking real search engines and retrievers with large language models via reinforcement learning,” 2025. [Online]. Available: https://arxiv.org/abs/2503.00223 [109] O. Weller, K. Lo, D. Wadden, D. J. Lawrie, B. V . Durme, A. Cohan, and L. Soldaini, “When do generative query and document expansions fail?

**中文**

李，“Deepseek-r1：通过强化学习激励 llms 的推理能力”，CoRR，卷。绝对/2501.12948，2025。[108]P。 Jiang、J. Lin、L. Cao、R. Tian、S. Kang、Z. Wang、J. Sun 和 J. Han，“深度检索：通过强化学习利用大型语言模型攻击真实搜索引擎和检索器”，2025 年。[在线]。可用：https://arxiv.org/abs/2503.00223 [109] O. Weller, K. Lo, D. Wadden, D. J. Lawrie, B. V. Durme、A. Cohan 和 L. Soldaini，“生成查询和文档扩展何时会失败？

### 段落 328 · Page 31

**EN**

A comprehensive study across methods, retrievers, and datasets,” inFindings of the Association for Computational Linguistics: EACL 2024, St. Julian’s, Malta, March 17-22, 2024, Y. Graham and M. Purver, Eds. Association for Computational Linguistics, 2024, pp. 1987–2003. [110] L. H. Bonifacio, H. Abonizio, M. Fadaee, and R. F. Nogueira, “Inpars: Data augmentation for information retrieval using large language models,”CoRR, vol. abs/2202.05144, 2022. [111] G. Ma, X. Wu, P . Wang, Z. Lin, and S. Hu, “Pretraining with large language model-based document expansion for dense passage retrieval,”CoRR, vol. abs/2308.08285, 2023. [112] V . Jeronymo, L.

**中文**

跨方法、检索器和数据集的综合研究”，载于计算语言学协会的调查结果：EACL 2024，马耳他圣朱利安，2024 年 3 月 17-22 日，Y. Graham 和 M. Purver，编辑。计算语言学协会，2024 年，第 1987-2003 页。 [110] L. H. Bonifacio、H. Abonizio、M. Fadaee 和 R. F. Nogueira，“Inpars：使用大型语言模型进行信息检索的数据增强”，CoRR，卷。 abs/2202.05144, 2022. [111] 马国强, 吴晓平. Wang、Z. Lin 和 S. Hu，“使用基于大型语言模型的文档扩展进行密集段落检索的预训练”，CoRR，卷。绝对/2308.08285，2023。[112]V。杰罗尼莫，L.

### 段落 329 · Page 31

**EN**

H. Bonifacio, H. Abonizio, M. Fadaee, R. de Alencar Lotufo, J. Zavrel, and R. F. Nogueira, “Inpars-v2: Large language models as efficient dataset generators for information retrieval,”CoRR, vol. abs/2301.01820, 2023. [113] Z. Dai, V . Y. Zhao, J. Ma, Y. Luan, J. Ni, J. Lu, A. Bakalov, K. Guu, K. B. Hall, and M. Chang, “Promptagator: Few-shot dense retrieval from 8 examples,” inICLR. OpenReview.net, 2023. [114] R. Meng, Y. Liu, S. Yavuz, D. Agarwal, L. Tu, N. Yu, J. Zhang, M. Bhat, and Y. Zhou, “Augtriever: Unsupervised dense retrieval by scalable data augmentation,” 2023. [115] J. Saad-Falcon, O. Khattab, K. Santhanam, R. Florian, M.

**中文**

H. Bonifacio、H. Abonizio、M. Fadaee、R. de Alencar Lotufo、J. Zavrel 和 R. F. Nogueira，“Inpars-v2：作为信息检索的高效数据集生成器的大型语言模型”，CoRR，卷。绝对/2301.01820，2023。[113]Z.戴，V。 Y. Zhao、J. Ma、Y. Luan、J. Ni、J. Lu、A. Bakalov、K. Guu、K. B. Hall 和 M. Chang，“Promptagator：来自 8 个示例的少样本密集检索”，载于 ICLR。 OpenReview.net，2023。[114] R.Meng、Y.Liu、S.Yavuz、D.Agarwal、L.Tu、N.Yu、J.Zhang、M.Bhat 和 Y.Zhou，“Augtriever：通过可扩展数据增强进行无监督密集检索”，2023。[115]J.Saad-Falcon、O.Khattab、K.Santhanam、R.Florian， M。

### 段落 330 · Page 31

**EN**

Franz, S. Roukos, A. Sil, M. A. Sultan, and C. Potts, “UDAPDR: unsupervised domain adaptation via LLM prompting and distillation of rerankers,” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 11 265–11 279. [116] Z. Peng, X. Wu, and Y. Fang, “Soft prompt tuning for augmenting dense retrieval with large language models,” 2023. [117] J. Lee, Z. Dai, X. Ren, B. Chen, D. Cer, J. R. Cole, K. Hui, M. Boratko, R. Kapadia, W. Ding, Y. Luan, S. M. K. Duddu, G. H. ´Abrego, W.

**中文**

Franz、S. Roukos、A. Sil、M. A. Sultan 和 C. Potts，“UDAPDR：通过 LLM 提示和重排序器蒸馏实现无监督领域适应”，载于 2023 年自然语言处理经验方法会议论文集，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023，第 11 265–11 279 页。 [116] Z. Peng、X. Wu 和 Y. Fang，“利用大型语言模型增强密集检索的软提示调整”，2023。 [117] J. Lee、Z. Dai、X. Ren、B. Chen、D. Cer、J. R. Cole、K. Hui、M. Boratko，R. Kapadia，W. Ding，Y. Luan，S. M. K. Duddu，G. H. ´Abrego，W.

### 段落 331 · Page 31

**EN**

Shi, N. Gupta, A. Kusupati, P . Jain, S. R. Jonnalagadda, M. Chang, and I. Naim, “Gecko: Versatile text embeddings distilled from large language models,”CoRR, vol. abs/2403.20327, 2024. [118] D. S. Sachan, M. Lewis, D. Yogatama, L. Zettlemoyer, J. Pineau, and M. Zaheer, “Questions are all you need to train a dense passage retriever,”Transactions of the Association for Computational Linguistics, vol. 11, pp. 600–616, 2023. [119] L. Wang, N. Yang, X. Huang, L. Yang, R. Majumder, and F.

**中文**

石，N.古普塔，A.库苏帕蒂，P。 Jain、S. R. Jonnalagadda、M. Chang 和 I. Naim，“Gecko：从大型语言模型中提取的多功能文本嵌入”，CoRR，卷。 abs/2403.20327, 2024。 [118] D. S. Sachan、M. Lewis、D. Yogatama、L. Zettlemoyer、J. Pineau 和 M. Zaheer，“训练密集通道检索器所需的全部就是问题”，计算语言学协会汇刊，卷。 11，第 600–616 页，2023。 [119] L. Wang、N. Yang、X. Huang、L. Yang、R. Majumder 和 F.

### 段落 332 · Page 31

**EN**

Wei, “Improving text embeddings with large language models,” inProceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), ACL 2024, Bangkok, Thailand, August 11-16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 11 897–11 916. [120] N. Thakur, N. Reimers, A. R ¨uckl´e, A. Srivastava, and I. Gurevych, “BEIR: A heterogeneous benchmark for zero-shot evaluation of information retrieval models,” inNeurIPS Datasets and Benchmarks, 2021. [121] N. Thakur, J. Ni, G. H. ´Abrego, J. Wieting, J. Lin,

**中文**

Wei，“利用大型语言模型改进文本嵌入”，载于计算语言学协会第 62 届年会论文集（第一卷：长论文），ACL 2024，泰国曼谷，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V。斯里库马尔，编辑。计算语言学协会，2024 年，第 11 897–11 916 页。 [120] N. Thakur、N. Reimers、A. R ´uckl´e、A. Srivastava 和 I. Gurevych，“BEIR：信息检索模型零样本评估的异构基准”，《NeurIPS 数据集和基准》，2021 年。 [121] N. Thakur、J. Ni、G. H. ´Abrego、J. Wieting、J. Lin，

### Page 32

### 段落 333 · Page 32

**EN**

32 and D. Cer, “Leveraging llms for synthesizing training data across many languages in multilingual dense retrieval,” inProceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers), NAACL 2024, Mexico City, Mexico, June 16-21, 2024, K. Duh, H. G ´omez-Adorno, and S. Bethard, Eds. Association for Computational Linguistics, 2024, pp. 7699–7724. [122] A. Neelakantan, T. Xu, R. Puri, A. Radford, J. M. Han, J. Tworek, Q. Yuan, N. Tezak, J. W. Kim, C. Hallacy, J. Heidecke, P . Shyam, B. Power, T. E. Nekoul, G. Sastry, G. Krueger, D.

**中文**

32 和 D. Cer，“利用 llms 在多语言密集检索中综合多种语言的训练数据”，载于 2024 年计算语言学协会北美分会会议记录：人类语言技术（第一卷：长论文），NAACL 2024，墨西哥墨西哥城，2024 年 6 月 16-21 日，K. Duh, H. G 'omez-Adorno 和 S. Bethard，编辑。计算语言学协会，2024 年，第 7699–7724 页。 [122] A. Neelakantan、T. Xu、R. Puri、A. Radford、J. M. Han、J. Tworek、Q. Yuan、N. Tezak、J. W. Kim、C. Hallacy、J. Heidecke、P。 Shyam, B. Power, T. E. Nekoul, G. Sastry, G. Krueger, D.

### 段落 334 · Page 32

**EN**

Schnurr, F. P . Such, K. Hsu, M. Thompson, T. Khan, T. Sherbakov, J. Jang, P . Welinder, and L. Weng, “Text and code embeddings by contrastive pre-training,”CoRR, vol. abs/2201.10005, 2022. [123] J. Ni, C. Qu, J. Lu, Z. Dai, G. H. ´Abrego, J. Ma, V . Y. Zhao, Y. Luan, K. B. Hall, M. Chang, and Y. Yang, “Large dual encoders are generalizable retrievers,” in EMNLP. Association for Computational Linguistics, 2022, pp. 9844–9855. [124] N. Muennighoff, “SGPT: GPT sentence embeddings for semantic search,”CoRR, vol. abs/2202.08904, 2022. [125] B. Peng, C. Li, P . He, M. Galley, and J. Gao, “Instruction tuning with GPT-4,”CoRR, vol.

**中文**

施努尔，F.P.例如，K. Hsu、M. Thompson、T. Khan、T. Sherbakov、J. Jang、P。 Welinder 和 L. Weng，“通过对比预训练进行文本和代码嵌入”，CoRR，卷。 ABS/2201.10005, 2022. [123] 倪建, 曲长, 陆建, 戴正, G. H. ´Abrego, J. Ma, V. Y.Zhao、Y.Luan、K.B.Hall、M.Chang 和 Y.Yang，“大型双编码器是可泛化的检索器”，EMNLP。计算语言学协会，2022 年，第 9844–9855 页。 [124] N. Muennighoff，“SGPT：用于语义搜索的 GPT 句子嵌入”，CoRR，卷。 abs/2202.08904, 2022. [125] B. Peng, C. Li, P.他、M. Galley 和 J. Gau，“使用 GPT-4 进行指令调整”，CoRR，第 1 卷。

### 段落 335 · Page 32

**EN**

abs/2304.03277, 2023. [126] A. Q. Jiang, A. Sablayrolles, A. Mensch, C. Bamford, D. S. Chaplot, D. de Las Casas, F. Bressand, G. Lengyel, G. Lample, L. Saulnier, L. R. Lavaud, M. Lachaux, P . Stock, T. L. Scao, T. Lavril, T. Wang, T. Lacroix, and W. E. Sayed, “Mistral 7b,”CoRR, vol. abs/2310.06825, 2023. [127] S. Gunasekar, Y. Zhang, J. Aneja, C. C. T. Mendes, A. D. Giorno, S. Gopi, M. Javaheripi, P . Kauffmann, G. de Rosa, O. Saarikivi, A. Salim, S. Shah, H. S. Behl, X. Wang, S. Bubeck, R. Eldan, A. T. Kalai, Y. T. Lee, and Y. Li, “Textbooks are all you need,”CoRR, vol. abs/2306.11644, 2023. [128] T. Mesnard, C. Hardin, R. Dadashi, S.

**中文**

abs/2304.03277, 2023。 [126] A. Q. Jiang、A. Sablayrolles、A. Mensch、C. Bamford、D. S. Chaplot、D. de Las Casas、F. Bressand、G. Lengyel、G. Lample、L. Saulnier、L. R. Lavaud、M. Lachaux、P . Stock、T. L. Scao、T. Lavril、T. Wang、T. Lacroix 和 W. E. Sayed，“Mistral 7b”，CoRR，卷。 abs/2310.06825, 2023。 [127] S. Gunasekar、Y. 张、J. Aneja、C. C. T. Mendes、A. D. Giorno、S. Gopi、M. Javaheripi、P . Kauffmann、G. de Rosa、O. Saarikivi、A. Salim、S. Shah、H. S. Behl、X. Wang、S. Bubeck、R. Eldan、A. T. Kalai、Y. T. Lee 和 Y. Li，“教科书就是您所需要的”，CoRR，卷。绝对/2306.11644，2023。[128] T.梅斯纳德，C.哈丁，R.达达什，S.

### 段落 336 · Page 32

**EN**

Bhupatiraju, S. Pathak, L. Sifre, M. Rivi `ere, M. S. Kale, J. Love, P . Tafti, L. Hussenot, A. Chowdhery, A. Roberts, A. Barua, A. Botev, A. Castro-Ros, A. Slone, A. H´eliou, A. Tacchetti, A. Bulanova, A. Paterson, B. Tsai, B. Shahriari, C. L. Lan, C. A. Choquette-Choo, C. Crepy, D. Cer, D. Ippolito, D. Reid, E. Buchatskaya, E. Ni, E. Noland, G. Yan, G. Tucker, G. Muraru, G. Rozhdestvenskiy, H. Michalewski, I. Tenney, I. Grishchenko, J. Austin, J. Keeling, J. Labanowski, J. Lespiau, J. Stanway, J. Brennan, J. Chen, J. Ferret, J. Chiu, and et al., “Gemma: Open models based on gemini research and technology,”CoRR, vol. abs/2403.08295, 2024.

**中文**

Bhupatiraju、S. Pathak、L. Sifre、M. Rivi `ere、M. S. Kale、J. Love、P。塔夫蒂、L. Hussenot、A. Chowdhery、A. Roberts、A. Barua、A. Botev、A. Castro-Ros、A. Slone、A. H´eliou、A. Tacchetti、A. Bulanova、A. Paterson、B. Tsai、B. Shahriari、C. L. Lan、C. A. Choquette-Choo、C. Crepy、D. Cer、D. Ippolito、 D. Reid、E. Buchatskaya、E. Ni、E. Noland、G. Yan、G. Tucker、G. Muraru、G. Rozhdestvenskiy、H. Michalewski、I. Tenney、I. Grishchenko、J. Austin、J. Keeling、J. Labanowski、J. Lespiau、J. Stanway、J. Brennan、J. Chen、J. Ferret、J. Chiu 等等人，“Gemma：基于 Gemini 研究和技术的开放模型”，CoRR，卷。绝对/2403.08295，2024。

### 段落 337 · Page 32

**EN**

[129] X. Ma, L. Wang, N. Yang, F. Wei, and J. Lin, “Finetuning llama for multi-stage text retrieval,” inProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2024, Washington DC, USA, July 14-18, 2024, G. H. Yang, H. Wang, S. Han, C. Hauff, G. Zuccon, and Y. Zhang, Eds. ACM, 2024, pp. 2421–2425. [130] R. Meng, Y. Liu, S. R. Joty, C. Xiong, Y. Zhou, and S. Yavuz, “Sfr-embedding-mistral: Enhance text retrieval with transfer learning,” Salesforce AI Research Blog, 2024. [131] J. Kim, S. Lee, J. Kwon, S. Gu, Y. Kim, M. Cho, and C. C.

**中文**

[129] X. Ma, L. Wang, N. Yang, F. Wei, and J. Lin, “Finetuning llama for multi-stage textretrieval,” in Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2024, Washington DC, USA, July 14-18, 2024, G. H. Yang, H. Wang, S. Han, C. Hauff、G.Zuccon 和 Y.Zhang，编辑。 ACM，2024 年，第 2421–2425 页。 [130] R.Meng、Y.Liu、S.R.Joty、C.Xiong、Y.Zhou 和 S.Yavuz，“Sfr-embedding-mistral：通过迁移学习增强文本检索”，Salesforce AI 研究博客，2024 年。 [131] J.Kim、S.Lee、J.Kwon、S.Gu、Y.Kim、M.Cho 和 C.C.

### 段落 338 · Page 32

**EN**

Jy-yong Sohn, “Linq-embed-mistral: Elevating text retrieval with improved gpt data through taskspecific control and quality refinement,” Linq AI Research Blog, 2024. [132] N. Muennighoff, N. Tazi, L. Magne, and N. Reimers, “MTEB: massive text embedding benchmark,” inProceedings of the 17th Conference of the European Chapter of the Association for Computational Linguistics, EACL 2023, Dubrovnik, Croatia, May 2-6, 2023, A. Vlachos and I. Augenstein, Eds. Association for Computational Linguistics, 2023, pp. 2006–2029. [133] C. Li, Z. Liu, S. Xiao, and Y. Shao, “Making large language models A better foundation for dense retrieval,”CoRR, vol.

**中文**

Jy-yong Sohn，“Linq-embed-mistral：通过特定于任务的控制和质量细化，利用改进的 gpt 数据提升文本检索”，Linq AI 研究博客，2024 年。 [132] N. Muennighoff、N. Tazi、L. Magne 和 N. Reimers，“MTEB：大规模文本嵌入基准”，载于欧洲协会欧洲分会第 17 届会议记录计算语言学，EACL 2023，克罗地亚杜布罗夫尼克，2023 年 5 月 2-6 日，A. Vlachos 和 I. Augenstein，编辑。计算语言学协会，2023 年，第 2006-2029 页。 [133] C. Li，Z. Liu，S. Shaw，Y. Shao，“让大型语言模型成为密集检索的更好基础”，CoRR，第 1 卷。

### 段落 339 · Page 32

**EN**

abs/2312.15503, 2023. [134] C. Lee, R. Roy, M. Xu, J. Raiman, M. Shoeybi, B. Catanzaro, and W. Ping, “Nv-embed: Improved techniques for training llms as generalist embedding models,” inThe Thirteenth International Conference on Learning Representations, ICLR 2025, Singapore, April 24-28, 2025. OpenReview.net, 2025. [135] H. Su, W. Shi, J. Kasai, Y. Wang, Y. Hu, M. Ostendorf, W. Yih, N. A. Smith, L. Zettlemoyer, and T. Yu, “One embedder, any task: Instruction-finetuned text embeddings,” inFindings of the Association for Computational Linguistics: ACL 2023, Toronto, Canada, July 9-14, 2023, A. Rogers, J. L. Boyd-Graber, and N. Okazaki, Eds.

**中文**

abs/2312.15503，2023。[134] C. Lee、R. Roy、M. Xu、J. Raiman、M. Shoeybi、B. Catanzaro 和 W. Ping，“Nv-embed：将 llms 训练为通用嵌入模型的改进技术”，载于第十三届学习表示国际会议，ICLR 2025，新加坡，4 月24-28, 2025. OpenReview.net, 2025. [135] H. Su, W. Shi, J. Kasai, Y. Wang, Y. Hu, M. Ostendorf, W. Yih, N. A. Smith, L. Zettlemoyer, 和 T. Yu，“一个嵌入器，任何任务：指令微调文本嵌入”，计算协会的调查结果语言学：ACL 2023，加拿大多伦多，2023 年 7 月 9-14 日，A. Rogers、J. L. Boyd-Graber 和 N. Okazaki，编辑。

### 段落 340 · Page 32

**EN**

Association for Computational Linguistics, 2023, pp. 1102–1121. [136] A. Asai, T. Schick, P . S. H. Lewis, X. Chen, G. Izacard, S. Riedel, H. Hajishirzi, and W. Yih, “Task-aware retrieval with instructions,” inFindings of the Association for Computational Linguistics: ACL 2023, Toronto, Canada, July 9-14, 2023, A. Rogers, J. L. Boyd-Graber, and N. Okazaki, Eds. Association for Computational Linguistics, 2023, pp. 3650–3675. [137] K. Luo, M. Qin, Z. Liu, S. Xiao, J. Zhao, and K.

**中文**

计算语言学协会，2023 年，第 1102–1121 页。 [136] A. Asai，T. Schick，P。 S. H. Lewis、X. Chen、G. Izacard、S. Riedel、H. Hajishirzi 和 W. Yih，“使用指令进行任务感知检索”，计算语言学协会的调查结果：ACL 2023，加拿大多伦多，2023 年 7 月 9-14 日，A. Rogers、J. L. Boyd-Graber 和 N. Okazaki，编辑。计算语言学协会，2023 年，第 3650–3675 ​​页。 [137] 罗克，秦明，刘子，肖思，赵建，K.

### 段落 341 · Page 32

**EN**

Liu, “Large language models as foundations for next-gen dense retrieval: A comprehensive empirical assessment,” inProceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, EMNLP 2024, Miami, FL, USA, November 12-16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 1354–1365. [138] K. Mao, C. Deng, H. Chen, F. Mo, Z. Liu, T. Sakai, and Z.

**中文**

Liu，“大型语言模型作为下一代密集检索的基础：全面的实证评估”，载于 2024 年自然语言处理经验方法会议论文集，EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 1354–1365 页。 [138] K. Mao，C. Deng，H. Chen，F. Mo，Z. Liu，T. Sakai，Z.

### 段落 342 · Page 32

**EN**

Dou, “Chatretriever: Adapting large language models for generalized and robust conversational dense retrieval,” inProceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, EMNLP 2024, Miami, FL, USA, November 12-16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 1227– 1240. [139] T. Jiang, S. Huang, Z. Luan, D. Wang, and F. Zhuang, “Scaling sentence embeddings with large language models,” inFindings of the Association for Computational Linguistics: EMNLP 2024, Miami, Florida, USA, November 12-16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen,

**中文**

Dou，“Chatretriever：调整大型语言模型以实现广义和鲁棒的会话密集检索”，载于 2024 年自然语言处理经验方法会议论文集，EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 1227–1240 页。 [139] T. Jiang、S. Huang、Z. Luan、D. Wang 和 F. Zhuang，“利用大型语言模型扩展句子嵌入”，载于计算语言学协会的调查结果：EMNLP 2024，美国佛罗里达州迈阿密，11 月 12-16 日， 2024，Y. Al-Onaizan、M. Bansal 和 Y. Chen，

### Page 33

### 段落 343 · Page 33

**EN**

33 Eds. Association for Computational Linguistics, 2024, pp. 3182–3196. [140] D. Metzler, Y. Tay, D. Bahri, and M. Najork, “Rethinking search: making domain experts out of dilettantes,” SIGIR Forum, vol. 55, no. 1, pp. 13:1–13:27, 2021. [141] Y. Zhou, J. Yao, Z. Dou, L. Wu, and J. Wen, “Dynamicretriever: A pre-trained model-based IR system without an explicit index,”Mach. Intell. Res., vol. 20, no. 2, pp. 276–288, 2023. [142] J. Chen, R. Zhang, J. Guo, Y. Liu, Y. Fan, and X.

**中文**

33编。计算语言学协会，2024 年，第 3182-3196 页。 [140] D. Metzler、Y. Tay、D. Bahri 和 M. Najork，“重新思考搜索：让业余爱好者成为领域专家”，SIGIR 论坛，第 1 卷。 55，没有。 1，第 13:1–13:27，2021 年。 [141] Y. Zhou、J. Yao、Z. Dou、L. Wu 和 J. Wen，“Dynamicretriever：一种基于预训练模型的无显式索引的 IR 系统”，Mach。英特尔。研究，卷。 20、没有。 2，第276-288页，2023年。 [142] J. Chen，R. Zhang，J.Guo，Y.Liu，Y.Fan，and X.

### 段落 344 · Page 33

**EN**

Cheng, “Corpusbrain: Pre-train a generative retrieval model for knowledge-intensive language tasks,” inProceedings of the 31st ACM International Conference on Information & Knowledge Management, Atlanta, GA, USA, October 17-21, 2022, M. A. Hasan and L. Xiong, Eds. ACM, 2022, pp. 191–200. [143] Y. Tay, V . Tran, M. Dehghani, J. Ni, D. Bahri, H. Mehta, Z. Qin, K. Hui, Z. Zhao, J. P . Gupta, T. Schuster, W. W. Cohen, and D. Metzler, “Transformer memory as a differentiable search index,” inNeurIPS, 2022. [144] N. Ziems, W. Yu, Z. Zhang, and M.

**中文**

Cheng，“Corpusbrain：为知识密集型语言任务预训练生成检索模型”，载于第 31 届 ACM 国际信息与知识管理会议记录，美国佐治亚州亚特兰大，2022 年 10 月 17-21 日，M. A. Hasan 和 L. Xiong，编辑。 ACM，2022 年，第 191-200 页。 [143] Y.Tay，V。 Tran、M. Dehghani、J. Ni、D. Bahri、H. Mehta、Z. 秦、K. Hui、Z. 赵、J. P。 Gupta、T. Schuster、W. W. Cohen 和 D. Metzler，“作为可微分搜索索引的 Transformer 内存”，inNeurIPS，2022 年。 [144] N. Ziems、W. Yu、Z. Zhu 和 M.

### 段落 345 · Page 33

**EN**

Jiang, “Large language models are built-in autoregressive search engines,” inFindings of the Association for Computational Linguistics: ACL 2023, Toronto, Canada, July 9-14, 2023, A. Rogers, J. L. Boyd-Graber, and N. Okazaki, Eds. Association for Computational Linguistics, 2023, pp. 2666–2678. [145] Y. Wang, Y. Hou, H. Wang, Z. Miao, S. Wu, Q. Chen, Y. Xia, C. Chi, G. Zhao, Z. Liu, X. Xie, H. Sun, W. Deng, Q. Zhang, and M.

**中文**

Jiang，“大型语言模型是内置的自回归搜索引擎”，载于计算语言学协会的调查结果：ACL 2023，加拿大多伦多，2023 年 7 月 9-14 日，A. Rogers、J. L. Boyd-Graber 和 N. Okazaki，编辑。计算语言学协会，2023 年，第 2666–2678 页。 [145] Y. Wang、Y. Hou、H. Wang、Z. Miao、S. Wu、Q. Chen、Y. Xia、C. Chi、G. Zhao、Z. Liu、X. Xie、H. Sun、W. Deng、Q.Zhang 和 M.

### 段落 346 · Page 33

**EN**

Yang, “A neural corpus indexer for document retrieval,” inAdvances in Neural Information Processing Systems 35: Annual Conference on Neural Information Processing Systems 2022, NeurIPS 2022, New Orleans, LA, USA, November 28 - December 9, 2022, S. Koyejo, S. Mohamed, A. Agarwal, D. Belgrave, K. Cho, and A. Oh, Eds., 2022. [146] M. Bevilacqua, G. Ottaviano, P . S. H. Lewis, S. Yih, S. Riedel, and F.

**中文**

Yang，“用于文档检索的神经语料库索引器”，《神经信息处理系统进展 35：2022 年神经信息处理系统年会》，NeurIPS 2022，美国洛杉矶新奥尔良，2022 年 11 月 28 日至 12 月 9 日，S. Koyejo、S. Mohamed、A. Agarwal、D. Belgrave、K. Cho 和 A. Oh，编辑， 2022. [146] M.贝维拉夸，G.奥塔维亚诺，P。 S. H. Lewis、S. Yih、S. Riedel 和 F.

### 段落 347 · Page 33

**EN**

Petroni, “Autoregressive search engines: Generating substrings as document identifiers,” inAdvances in Neural Information Processing Systems 35: Annual Conference on Neural Information Processing Systems 2022, NeurIPS 2022, New Orleans, LA, USA, November 28 - December 9, 2022, S. Koyejo, S. Mohamed, A. Agarwal, D. Belgrave, K. Cho, and A. Oh, Eds., 2022. [147] R. Pradeep, K. Hui, J. Gupta, ´A. D. Lelkes, H. Zhuang, J. Lin, D. Metzler, and V . Q.

**中文**

Petroni，“自回归搜索引擎：生成子字符串作为文档标识符”，《神经信息处理系统进展 35：2022 年神经信息处理系统年会》，NeurIPS 2022，美国洛杉矶新奥尔良，2022 年 11 月 28 日至 12 月 9 日，S. Koyejo、S. Mohamed、A. Agarwal、D. Belgrave、K. Cho 和 A. Oh，编辑，2022 年。[147] R. Pradeep、K. Hui、J. Gupta、´A. D. Lelkes、H. Zhuang、J. Lin、D. Metzler 和 V。问。

### 段落 348 · Page 33

**EN**

Tran, “How does generative retrieval scale to millions of passages?” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 1305–1321. [148] X. Li, Z. Dou, Y. Zhou, and F. Liu, “Corpuslm: Towards a unified language model on corpus for knowledge-intensive tasks,” inProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2024, Washington DC, USA, July 14-18, 2024, G. H. Yang, H. Wang, S. Han, C. Hauff, G.

**中文**

Tran，“生成检索如何扩展到数百万个段落？” 2023 年自然语言处理经验方法会议论文集，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 1305–1321 页。 [148] X. Li、Z. Dou、Y. Zhou 和 F. Liu，“Corpuslm：面向知识密集型任务的语料库的统一语言模型”，载于第 47 届国际 ACM SIGIR 信息检索研究与发展会议论文集，SIGIR 2024，美国华盛顿特区，2024 年 7 月 14-18 日，G. H. Yang、H. Wang， S. Han，C. Hauff，G.

### 段落 349 · Page 33

**EN**

Zuccon, and Y. Zhang, Eds. ACM, 2024, pp. 26–37. [149] J. Ju, J. Yang, and C. Wang, “Text-to-text multi-view learning for passage re-ranking,” inSIGIR ’21: The 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, Virtual Event, Canada, July 11-15, 2021, F. Diaz, C. Shah, T. Suel, P . Castells, R. Jones, and T. Sakai, Eds. ACM, 2021, pp. 1803–1807. [150] R. Pradeep, R. F. Nogueira, and J. Lin, “The expandomono-duo design pattern for text ranking with pretrained sequence-to-sequence models,”CoRR, vol. abs/2101.05667, 2021. [151] H. Zhuang, Z. Qin, R. Jagerman, K. Hui, J. Ma, J. Lu, J. Ni, X. Wang, and M.

**中文**

Zuccon 和 Y.Zhang，编辑。 ACM，2024 年，第 26-37 页。 [149] J. Ju、J. Yang 和 C. Wang，“用于段落重新排序的文本到文本多视图学习”，inSIGIR '21：第 44 届国际 ACM SIGIR 信息检索研究与开发会议，虚拟活动，加拿大，2021 年 7 月 11-15 日，F. Diaz、C. Shah、T. Suel、P。 Castells、R. Jones 和 T. Sakai，编辑。 ACM，2021 年，第 1803–1807 页。 [150] R. Pradeep、R. F. Nogueira 和 J. Lin，“使用预训练的序列到序列模型进行文本排名的扩展单双设计模式”，CoRR，卷。 abs/2101.05667, 2021. [151] H. Zhuang, Z.qin, R. Jagerman, K. Hui, J. Ma, J. Lu, J. Ni, X. Wang, and M.

### 段落 350 · Page 33

**EN**

Bendersky, “Rankt5: Finetuning T5 for text ranking with ranking losses,” inProceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2023, Taipei, Taiwan, July 23-27, 2023, H. Chen, W. E. Duh, H. Huang, M. P . Kato, J. Mothe, and B. Poblete, Eds. ACM, 2023, pp. 2308–2313. [152] S. Yoon, E. Choi, J. Kim, H. Yun, Y. Kim, and S. Hwang, “Listt5: Listwise reranking with fusion-in-decoder improves zero-shot retrieval,” inACL (1). Association for Computational Linguistics, 2024, pp. 2287–2308. [153] L. Zhang, Y. Zhang, D. Long, P . Xie, M. Zhang, and M.

**中文**

Bendersky，“Rankt5：微调 T5 进行排名损失的文本排名”，载于第 46 届国际 ACM SIGIR 信息检索研究与发展会议论文集，SIGIR 2023，台湾台北，2023 年 7 月 23-27 日，H. Chen、W. E. Duh、H. Huang、M. P. Kato，J. Mothe 和 B. Poblete，编辑。 ACM，2023 年，第 2308–2313 页。 [152] S. Yoon、E. Choi、J. Kim、H. Yun、Y. Kim 和 S. Hwang，“Listt5：使用解码器中融合进行列表重排序改进了零样本检索”，参见 ACL (1)。计算语言学协会，2024 年，第 2287-2308 页。 [153] 张丽，张勇，龙东，P．谢，M. 张，M.

### 段落 351 · Page 33

**EN**

Zhang, “A two-stage adaptation of large language models for text ranking,” inFindings of the Association for Computational Linguistics, ACL 2024, Bangkok, Thailand and virtual meeting, August 11-16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 11 880–11 891. [154] Z. Peng, X. Wu, Q. Wang, S. Rajanala, and Y. Fang, “Q-PEFT: query-dependent parameter efficient finetuning for text reranking with large language models,”CoRR, vol. abs/2404.04522, 2024. [155] C. Zhang, S. Hofst ¨atter, P . Lewis, R. Tang, and J.

**中文**

张，“用于文本排名的大型语言模型的两阶段改编”，载于计算语言学协会的调查结果，ACL 2024，泰国曼谷和虚拟会议，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V。斯里库马尔，编辑。计算语言学协会，2024 年，第 11 880–11 891 页。 [154] Z. Peng、X. Wu、Q. Wang、S. Rajanala 和 Y. Fang，“Q-PEFT：大型语言模型文本重排序的查询相关参数高效微调”，CoRR，卷。绝对/2404.04522，2024。[155] C.Zhang，S.Hofst ¡atter，P。刘易斯，R.唐，J.

### 段落 352 · Page 33

**EN**

Lin, “Rank-without-gpt: Building gpt-independent listwise rerankers on open-source large language models,” inAdvances in Information Retrieval - 47th European Conference on Information Retrieval, ECIR 2025, Lucca, Italy, April 6-10, 2025, Proceedings, Part II, ser. Lecture Notes in Computer Science, C. Hauff, C. Macdonald, D. Jannach, G. Kazai, F. M. Nardini, F. Pinelli, F. Silvestri, and N. Tonellotto, Eds., vol. 15573. Springer, 2025, pp. 233–247. [156] Q. Liu, B. Wang, N. Wang, and J. Mao, “Leveraging passage embeddings for efficient listwise reranking with large language models,”CoRR, vol. abs/2406.14848, 2024. [157] P . Liang, R.

**中文**

Lin，“Rank-without-gpt：在开源大型语言模型上构建独立于 gpt 的列表重排序器”，载于信息检索进展 - 第 47 届欧洲信息检索会议，ECIR 2025，意大利卢卡，2025 年 4 月 6-10 日，会议记录，第二部分，系列。计算机科学讲义，C. Hauff、C. Macdonald、D. Jannach、G. Kazai、F. M. Nardini、F. Pinelli、F. Silvestri 和 N. Tonellotto，编辑，卷。 15573。施普林格，2025 年，第 233-247 页。 [156] Q. Liu、B. Wang、N. Wang 和 J. Mao，“利用段落嵌入对大型语言模型进行高效的列表重排序”，CoRR，第 1 卷。绝对/2406.14848，2024。[157]P。梁，R.

### 段落 353 · Page 33

**EN**

Bommasani, T. Lee, D. Tsipras, D. Soylu, M. Yasunaga, Y. Zhang, D. Narayanan, Y. Wu, A. Kumar, B. Newman, B. Yuan, B. Yan, C. Zhang, C. Cosgrove, C. D. Manning, C. R ´e, D. Acosta-Navas, D. A. Hudson, E. Zelikman, E. Durmus, F. Ladhak, F. Rong, H. Ren, H. Yao, J. Wang, K. Santhanam, L. J. Orr, L. Zheng, M. Y ¨uksekg¨on ¨ul, M. Suzgun, N. Kim, N. Guha, N. S. Chatterji, O. Khattab, P . Henderson, Q. Huang, R. Chi, S. M. Xie, S. Santurkar, S. Ganguli, T. Hashimoto, T. Icard, T. Zhang, V . Chaudhary, W. Wang, X. Li, Y. Mai, Y. Zhang, and Y. Koreeda, “Holistic evaluation of language models,” Trans. Mach. Learn. Res., vol. 2023, 2023.

**中文**

Bommasani、T. Lee、D. Tsipras、D. Soylu、M. Yasunaga、Y. Zhang、D. Narayanan、Y. Wu、A. Kumar、B. Newman、B. Yuan、B. Yan、C. 张、C. Cosgrove、C. D. Manning、C. R ´e、D. Acosta-Navas、D. A. Hudson、E. Zelikman、E. Durmus、F. Ladhak、F. Rong、H. Ren、H. Yao、J. Wang、K. Santhanam、L. J. Orr、L. Cheng、M. Y uksekgon ul、M. Suzgun、N. Kim、N. Guha、N. S. Chatterji、O. Khattab、P。亨德森，Q.黄，R.Chi，S.M.Xie，S.Santurkar，S.Ganguli，T.Hashimoto，T.Icard，T.Zhang，V。 Chaudhary、W. Wang、X. Li、Y. Mai、Y. Zhang 和 Y. Koreeda，“语言模型的整体评估”，Trans。马赫。学习。研究，卷。 2023 年，2023 年。

### Page 34

### 段落 354 · Page 34

**EN**

34 [158] H. Zhuang, Z. Qin, K. Hui, J. Wu, L. Yan, X. Wang, and M. Bendersky, “Beyond yes and no: Improving zeroshot LLM rankers via scoring fine-grained relevance labels,” inProceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies: Short Papers, NAACL 2024, Mexico City, Mexico, June 16-21, 2024, K. Duh, H. G ´omez-Adorno, and S. Bethard, Eds. Association for Computational Linguistics, 2024, pp. 358–370. [159] F. Guo, W. Li, H. Zhuang, Y. Luo, Y. Li, L. Yan, and Y. Zhang, “Generating diverse criteria on-thefly to improve point-wise LLM rankers,”CoRR, vol.

**中文**

34 [158] H. Zhuang、Z.qin、K.Hui、J.Wu、L.Yan、X.Wang 和 M.Bendersky，“超越是与否：通过对细粒度相关性标签进行评分来改进零样本法学硕士排名”，载于计算语言学协会北美分会 2024 年会议记录：人类语言技术：短论文，NAACL 2024，墨西哥墨西哥城，2024 年 6 月 16-21 日，K. Duh、H. G ´omez-Adorno 和 S. Bethard 主编。计算语言学协会，2024 年，第 358-370 页。 [159] F.Guo、W.Li、H.Zhang、Y.Luo、Y.Li、L.Yan 和 Y.Zhang，“即时生成多样化标准以改进逐点 LLM 排名”，CoRR，卷。

### 段落 355 · Page 34

**EN**

abs/2404.11960, 2024. [160] D. S. Sachan, M. Lewis, M. Joshi, A. Aghajanyan, W. Yih, J. Pineau, and L. Zettlemoyer, “Improving passage retrieval with zero-shot question generation,” in EMNLP. Association for Computational Linguistics, 2022, pp. 3781–3797. [161] S. Zhuang, B. Liu, B. Koopman, and G. Zuccon, “Open-source large language models are strong zeroshot query likelihood models for document ranking,” inFindings of the Association for Computational Linguistics: EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 8807–8817. [162] S. Sun, S. Zhuang, S.

**中文**

abs/2404.11960, 2024。 [160] D. S. Sachan、M. Lewis、M. Joshi、A. Aghajanyan、W. Yih、J. Pineau 和 L. Zettlemoyer，“通过零样本问题生成改进段落检索”，EMNLP。计算语言学协会，2022 年，第 3781–3797 页。 [161] S. Zhuang、B. Liu、B. Koopman 和 G. Zuccon，“开源大型语言模型是用于文档排名的强大零样本查询似然模型”，载于计算语言学协会的调查结果：EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 8807–8817 页。 [162] 孙胜，庄胜，S.

### 段落 356 · Page 34

**EN**

Wang, and G. Zuccon, “An investigation of prompt variations for zero-shot llmbased rankers,”CoRR, vol. abs/2406.14117, 2024. [163] S. Cho, S. Jeong, J. Seo, and J. C. Park, “Discrete prompt optimization via constrained generation for zero-shot re-ranker,” inACL (Findings). Association for Computational Linguistics, 2023, pp. 960–971. [164] W. Liu, Y. Zhu, and Z. Dou, “Demorank: Selecting effective demonstrations for large language models in ranking task,”CoRR, vol. abs/2406.16332, 2024. [165] A. Drozdov, H. Zhuang, Z. Dai, Z. Qin, R. Rahimi, X. Wang, D. Alon, M. Iyyer, A. McCallum, D. Metzler, and K.

**中文**

Wang 和 G. Zuccon，“零样本 llm 排序器的即时变化调查”，CoRR，卷。 abs/2406.14117, 2024。 [163] S. Cho、S. Jeong、J. Seo 和 J. C. Park，“通过零样本重新排序器的约束生成进行离散提示优化”，载于 ACL（调查结果）。计算语言学协会，2023 年，第 960-971 页。 [164] W. Liu，Y. Zhu，Z. Dou，“Demorank：在排序任务中选择大语言模型的有效演示”，CoRR，卷。 abs/2406.16332, 2024。 [165] A. Drozdov、H. Zhuang、Z. Dai、Z. Qing、R. Rahimi、X. Wang、D. Alon、M. Iyyer、A. McCallum、D. Metzler 和 K.

### 段落 357 · Page 34

**EN**

Hui, “Parade: Passage ranking using demonstrations with llms,” inFindings of the Association for Computational Linguistics: EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 14 242–14 252. [166] W. Sun, L. Yan, X. Ma, S. Wang, P . Ren, Z. Chen, D. Yin, and Z. Ren, “Is chatgpt good at search? investigating large language models as re-ranking agents,” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds.

**中文**

Hui，“Parade：使用 llms 演示进行段落排名”，载于计算语言学协会的调查结果：EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023，第 14 242–14 252 页。 [166] W. Sun，L. Yan，X. Ma，S. Wang，P . Ren、Z. Chen、D. Yin 和 Z. Ren，“Chatgpt 擅长搜索吗？研究大型语言模型作为重新排序代理”，载于 2023 年自然语言处理经验方法会议论文集，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。

### 段落 358 · Page 34

**EN**

Association for Computational Linguistics, 2023, pp. 14 918–14 937. [167] W. Liu, X. Ma, Y. Zhu, Z. Zhao, S. Wang, D. Yin, and Z. Dou, “Sliding windows are not the end: Exploring full ranking with long-context large language models,”CoRR, vol. abs/2412.14574, 2024. [168] W. Liu, X. Ma, Y. Zhu, L. Su, S. Wang, D. Yin, and Z. Dou, “Coranking: Collaborative ranking with small and large ranking agents,”CoRR, vol. abs/2503.23427, 2025. [169] X. Ma, X. Zhang, R. Pradeep, and J. Lin, “Zero-shot listwise document reranking with a large language model,”CoRR, vol. abs/2305.02156, 2023. [170] R. Tang, X. Zhang, X. Ma, J. Lin, and F.

**中文**

计算语言学协会，2023，第 14 918–14 937 页。 [167] W. Liu、X. Ma、Y. Zhu、Z. Zhu、S. Wang、D. Yin 和 Z. Dou，“滑动窗口不是终点：探索长上下文大语言模型的完整排名”，CoRR，卷。 abs/2412.14574, 2024. [168] W. Liu, X. Ma, Y. Zhu, L. Su, S. Wang, D. Yin, and Z. Dou, “Coranking: 与小型和大型排名代理的协作排名”，CoRR，卷。 abs/2503.23427, 2025。 [169] X. Ma, X.Zhang, R. Pradeep, and J. Lin, “使用大型语言模型进行零样本列表文档重排序”，CoRR，卷。 abs/2305.02156, 2023。 [170] R. Tang、X. 张、X. Ma、J. Lin 和 F.

### 段落 359 · Page 34

**EN**

Ture, “Found in the middle: Permutation self-consistency improves listwise ranking in large language models,” inProceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers), NAACL 2024, Mexico City, Mexico, June 16-21, 2024, K. Duh, H. G ´omez-Adorno, and S. Bethard, Eds. Association for Computational Linguistics, 2024, pp. 2327–2340. [171] Y. Chen, Q. Liu, Y. Zhang, W. Sun, D. Shi, J. Mao, and D. Yin, “Tourrank: Utilizing large language models for documents ranking with a tournament-inspired strategy,”CoRR, vol. abs/2406.11678, 2024.

**中文**

Ture，“发现在中间：排列自一致性提高了大型语言模型中的列表排名”，载于计算语言学协会北美分会 2024 年会议记录：人类语言技术（第一卷：长论文），NAACL 2024，墨西哥墨西哥城，2024 年 6 月 16-21 日，K. Duh, H. G 'omez-Adorno 和 S. Bethard，编辑。计算语言学协会，2024 年，第 2327-2340 页。 [171] Y. Chen，Q. Liu，Y. Zhang，W. Sun，D. Shi，J. Mao，D. Yin，“Tourrank：利用大型语言模型通过锦标赛启发的策略进行文档排名”，CoRR，卷。绝对/2406.11678，2024。

### 段落 360 · Page 34

**EN**

[172] A. Parry, S. MacAvaney, and D. Ganguly, “Top-down partitioning for efficient list-wise ranking,”CoRR, vol. abs/2405.14589, 2024. [173] C. Jin, H. Peng, S. Zhao, Z. Wang, W. Xu, L. Han, J. Zhao, K. Zhong, S. Rajasekaran, and D. N. Metaxas, “APEER : Automatic prompt engineering enhances large language model reranking,” inWWW (Companion Volume). ACM, 2025, pp. 2494–2502. [174] Z. Qin, R. Jagerman, K. Hui, H. Zhuang, J. Wu, L. Yan, J. Shen, T. Liu, J. Liu, D. Metzler, X. Wang, and M.

**中文**

[172] A. Parry、S. MacAvaney 和 D. Ganguly，“用于高效列表排序的自上而下分区”，CoRR，卷。 abs/2405.14589, 2024. [173] C. Jin、H. Peng、S. Zhu、Z. Wang、W. Xu、L. Han、J. Zhu、K.zhong、S. Rajasekaran 和 D. N. Metaxas，“APEER：自动提示工程增强大型语言模型重新排序”，参见 WWW（配套卷）。 ACM，2025 年，第 2494–2502 页。 [174] Z.Qin、R.Jagerman、K.Hui、H.Zhang、J.Wu、L.Yan、J.Shen、T.Liu、J.Liu、D.Metzler、X.Wang和M.

### 段落 361 · Page 34

**EN**

Bendersky, “Large language models are effective text rankers with pairwise ranking prompting,” in Findings of the Association for Computational Linguistics: NAACL 2024, Mexico City, Mexico, June 16-21, 2024, K. Duh, H. G ´omez-Adorno, and S. Bethard, Eds. Association for Computational Linguistics, 2024, pp. 1504–1518. [175] S. Zhuang, H. Zhuang, B. Koopman, and G. Zuccon, “A setwise approach for effective and highly efficient zero-shot ranking with large language models,” inProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2024, Washington DC, USA, July 14- 18, 2024, G. H.

**中文**

Bendersky，“大型语言模型是具有成对排名提示的有效文本排名器”，载于计算语言学协会的调查结果：NAACL 2024，墨西哥墨西哥城，2024 年 6 月 16-21 日，K. Duh、H. G ´omez-Adorno 和 S. Bethard，编辑。计算语言学协会，2024 年，第 1504–1518 页。 [175] S. Zhuang、H. Zhuang、B. Koopman 和 G. Zuccon，“利用大型语言模型进行有效且高效的零样本排名的集合方法”，载于第 47 届国际 ACM SIGIR 信息检索研究与开发会议的会议记录，SIGIR 2024，美国华盛顿特区，2024 年 7 月 14-18 日，G. H.

### 段落 362 · Page 34

**EN**

Yang, H. Wang, S. Han, C. Hauff, G. Zuccon, and Y. Zhang, Eds. ACM, 2024, pp. 38–47. [176] J. Luo, X. Chen, B. He, and L. Sun, “Prp-graph: Pairwise ranking prompting to llms with graph aggregation for effective text re-ranking,” inACL (1). Association for Computational Linguistics, 2024, pp. 5766–5776. [177] L. Yan, Z. Qin, H. Zhuang, R. Jagerman, X. Wang, M. Bendersky, and H. Oosterhuis, “Consolidating ranking and relevance predictions of large language models through post-processing,”CoRR, vol. abs/2404.11791, 2024. [178] F. Ferraretto, T. Laitz, R. de Alencar Lotufo, and R. F.

**中文**

Yang、H. Wang、S. Han、C. Hauff、G. Zuccon 和 Y. 张，编辑。 ACM，2024 年，第 38-47 页。 [176] J. Luo、X. Chen、B. He 和 L. Sun，“Prp-graph：通过图形聚合对 llms 进行配对排名提示，以实现有效的文本重排”，载于 ACL (1)。计算语言学协会，2024 年，第 5766–5776 页。 [177] L. Yan，Z.qin，H. Zhuang，R. Jagerman，X. Wang，M. Bendersky 和 ​​H. Oosterhuis，“通过后处理巩固大型语言模型的排名和相关性预测”，CoRR，卷。 abs/2404.11791, 2024。 [178] F. Ferraretto、T. Laitz、R. de Alencar Lotufo 和 R. F.

### 段落 363 · Page 34

**EN**

Nogueira, “Exaranker: Synthetic explanations improve neural rankers,” inProceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2023, Taipei, Taiwan, July 23-27, 2023, H. Chen, W. E. Duh, H. Huang, M. P . Kato, J. Mothe, and B. Poblete, Eds. ACM, 2023, pp. 2409–2414. [179] F. Ferraretto, T. Laitz, R. de Alencar Lotufo, and R. Nogueira, “Exaranker-open: Synthetic explanation for IR using open-source llms,”CoRR, vol.

**中文**

Nogueira，“Exaranker：综合解释改善神经排名”，载于第 46 届国际 ACM SIGIR 信息检索研究与发展会议论文集，SIGIR 2023，台湾台北，2023 年 7 月 23-27 日，H. Chen、W. E. Duh、H. Huang、M. P. Kato，J. Mothe 和 B. Poblete，编辑。 ACM，2023 年，第 2409–2414 页。 [179] F. Ferraretto、T. Laitz、R. de Alencar Lotufo 和 R. Nogueira，“Exaranker-open：使用开源 llms 进行 IR 的综合解释”，CoRR，卷。

### Page 35

### 段落 364 · Page 35

**EN**

35 abs/2402.06334, 2024. [180] L. Boytsov, P . Patel, V . Sourabh, R. Nisar, S. Kundu, R. Ramanathan, and E. Nyberg, “Inpars-light: Costeffective unsupervised training of efficient rankers,” CoRR, vol. abs/2301.02998, 2023. [181] A. Askari, M. Aliannejadi, E. Kanoulas, and S. Verberne, “Generating synthetic documents for crossencoder re-rankers: A comparative study of chatgpt and human experts,”CoRR, vol. abs/2305.02320, 2023. [182] A. Askari, M. Aliannejadi, C. Meng, E. Kanoulas, and S. Verberne, “Expand, highlight, generate: Rldriven document generation for passage reranking,” inEMNLP. Association for Computational Linguistics, 2023, pp.

**中文**

35 绝对/2402.06334，2024。[180]L.博伊佐夫，P。帕特尔，V. Sourabh、R. Nisar、S. Kundu、R. Ramanathan 和 E. Nyberg，“Inpars-light：高效排序器的成本效益高的无监督训练”，CoRR，卷。 abs/2301.02998, 2023。 [181] A. Askari、M. Aliannejadi、E. Kanoulas 和 S. Verberne，“为交叉编码器重新排序器生成合成文档：chatgpt 和人类专家的比较研究”，CoRR，卷。 abs/2305.02320, 2023。 [182] A. Askari、M. Aliannejadi、C. Ming、E. Kanoulas 和 S. Verberne，“扩展、突出显示、生成：用于段落重排序的 Rl 驱动文档生成”，inEMNLP。计算语言学协会，2023 年，第 14 页。

### 段落 365 · Page 35

**EN**

10 087–10 099. [183] R. Pradeep, S. Sharifymoghaddam, and J. Lin, “Rankvicuna: Zero-shot listwise document reranking with open-source large language models,”CoRR, vol. abs/2309.15088, 2023. [184] ——, “Rankzephyr: Effective and robust zeroshot listwise reranking is a breeze!”CoRR, vol. abs/2312.02724, 2023. [185] W. Sun, Z. Chen, X. Ma, L. Yan, S. Wang, P . Ren, Z. Chen, D. Yin, and Z. Ren, “Instruction distillation makes large language models efficient zero-shot rankers,”CoRR, vol. abs/2311.01555, 2023. [186] W. Liu, X. Ma, W. Sun, Y. Zhu, Y. Li, D. Yin, and Z.

**中文**

10 087–10 099。 [183] R. Pradeep、S. Sharifymoghaddam 和 J. Lin，“Rankvicuna：使用开源大型语言模型进行零样本列表文档重排序”，CoRR，卷。 abs/2309.15088, 2023. [184] ——, “Rankzephyr: 有效且鲁棒的零样本列表重排序轻而易举！”CoRR, vol. abs/2312.02724, 2023. [185] 孙文，陈子，马晓，严丽，王世，P. Ren、Z. Chen、D. Yin 和 Z. Ren，“指令蒸馏使大型语言模型成为高效的零样本排序器”，CoRR，第 1 卷。 abs/2311.01555, 2023. [186] 刘伟、马晓、孙伟、朱勇、李勇、殷东、Z.

### 段落 366 · Page 35

**EN**

Dou, “Reasonrank: Empowering passage ranking with strong reasoning ability,”CoRR, vol. abs/2508.07050, 2025. [187] O. Weller, K. Ricci, E. Yang, A. Yates, D. J. Lawrie, and B. V . Durme, “Rank1: Test-time compute for reranking in information retrieval,”CoRR, vol. abs/2502.18418, 2025. [188] E. Yang, A. Yates, K. Ricci, O. Weller, V . Chari, B. V . Durme, and D. J. Lawrie, “Rank-k: Test-time reasoning for listwise reranking,”CoRR, vol. abs/2505.14432, 2025. [189] L. Zhang, B. Wang, X. Qiu, S. Reddy, and A. Agrawal, “REARANK: reasoning re-ranking agent via reinforcement learning,”CoRR, vol. abs/2505.20046, 2025. [190] S. Zhuang, X. Ma, B.

**中文**

窦，“Reasonrank：以强大的推理能力赋能文章排名”，CoRR，vol. abs/2508.07050, 2025。 [187] O. Weller、K. Ricci、E. Yang、A. Yates、D. J. Lawrie 和 B. V。 Durme，“Rank1：信息检索中重排的测试时计算”，CoRR，卷。 abs/2502.18418, 2025。 [188] E. Yang, A. Yates, K. Ricci, O. Weller, V.查里，B.V. Durme 和 D. J. Lawrie，“Rank-k：列表重排序的测试时推理”，CoRR，卷。 Abs/2505.14432，2025。 [189] L.Zhang、B.Wang、X.Qiu、S.Reddy 和 A.Agrawal，“REARANK：通过强化学习推理重排序代理”，CoRR，卷。 abs/2505.20046, 2025. [190] 庄三，马小兵，B.

### 段落 367 · Page 35

**EN**

Koopman, J. Lin, and G. Zuccon, “Rank-r1: Enhancing reasoning in llm-based document rerankers via reinforcement learning,”CoRR, vol. abs/2503.06034, 2025. [191] Y. Fan, X. Chen, D. Ye, J. Liu, H. Liang, J. Ma, B. He, Y. Sun, and T. Ruan, “Tfrank: Think-free reasoning enables practical pointwise LLM ranking,”CoRR, vol. abs/2508.09539, 2025. [192] C. J. C. Burges, T. Shaked, E. Renshaw, A. Lazier, M. Deeds, N. Hamilton, and G. N. Hullender, “Learning to rank using gradient descent,” inICML, ser. ACM International Conference Proceeding Series, vol. 119. ACM, 2005, pp. 89–96. [193] J. A. Baktash and M.

**中文**

Koopman、J. Lin 和 G. Zuccon，“Rank-r1：通过强化学习增强基于 llm 的文档重新排序器的推理”，CoRR，卷。 abs/2503.06034, 2025. [191] Y. Fan, X. Chen, D. Ye, J. Liu, H. Liang, J. Ma, B. He, Y. Sun, and T. Ruan, “Tfrank: 无思考推理可实现实用的逐点法学硕士排名”，CoRR，卷。 abs/2508.09539，2025。 [192] C. J. C. Burges、T. Shaked、E. Renshaw、A. Lazier、M. Deeds、N. Hamilton 和 G. N. Hullender，“学习使用梯度下降进行排名”，inICML，ser。 ACM 国际会议论文集，卷。 119. ACM，2005 年，第 89-96 页。 [193] J.A.巴克塔什和 M.

### 段落 368 · Page 35

**EN**

Dawodi, “Gpt-4: A review on advancements and opportunities in natural language processing,”CoRR, vol. abs/2305.03195, 2023. [194] R. G. Reddy, J. Doo, Y. Xu, M. A. Sultan, D. Swain, A. Sil, and H. Ji, “FIRST: faster improved listwise reranking with single token decoding,”CoRR, vol. abs/2406.15657, 2024. [195] N. Sinhababu, A. Parry, D. Ganguly, D. Samanta, and P . Mitra, “Few-shot prompting for pairwise ranking: An effective non-parametric retrieval model,” in Findings of the Association for Computational Linguistics: EMNLP 2024, Miami, Florida, USA, November 12-16, 2024. Association for Computational Linguistics, 2024, pp. 12 363–12 377.

**中文**

Dawodi，“Gpt-4：自然语言处理的进展和机遇回顾”，CoRR，卷。 abs/2305.03195, 2023。 [194] R. G. Reddy、J. Doo、Y. Xu、M. A. Sultan、D. Swain、A. Sil 和 H. Ji，“第一：通过单令牌解码更快地改进列表重排序”，CoRR，卷。 abs/2406.15657, 2024。 [195] N. Sinhababu、A. Parry、D. Ganguly、D. Samanta 和 P . Mitra，“成对排序的少量提示：一种有效的非参数检索模型”，计算语言学协会的调查结果：EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日。计算语言学协会，2024 年，第 12 363–12 377 页。

### 段落 369 · Page 35

**EN**

[196] H. Su, H. Yen, M. Xia, W. Shi, N. Muennighoff, H. Wang, H. Liu, Q. Shi, Z. S. Siegel, M. Tang, R. Sun, J. Yoon, S. ¨O. Arik, D. Chen, and T. Yu, “BRIGHT: A realistic and challenging benchmark for reasoningintensive retrieval,” inICLR. OpenReview.net, 2025. [197] L. Li, X. Zhou, and Z. Liu, “R2MED: A benchmark for reasoning-driven medical retrieval,”CoRR, vol. abs/2505.14558, 2025. [198] M. Rashid, J. Meem, Y. Dong, and V . Hristidis, “Eco- Rank: Budget-constrained text re-ranking using large language models,” inFindings of the Association for Computational Linguistics ACL 2024, L.-W. Ku, A. Martins, and V . Srikumar, Eds.

**中文**

[196] H. Su，H. Yen，M. Xia，W. Shi，N. Muennighoff，H. Wang，H. Liu，Q. Shi，Z. S. Siegel，M. Tang，R. Sun，J. Yoon，S. ¡ Arik、D. Chen 和 T. Yu，“BRIGHT：推理密集型检索的现实且具有挑战性的基准”，载于 ICLR。 OpenReview.net，2025。 [197] L. Li、X. Zhou 和 Z. Liu，“R2MED：推理驱动的医学检索基准”，CoRR，卷。 abs/2505.14558, 2025。 [198] M. Rashid、J. Meem、Y. Dong 和 V。 Hristidis，“生态排名：使用大型语言模型对预算受限的文本进行重排”，载于计算语言学协会 ACL 2024 年的调查结果，L.-W. Ku、A. 马丁斯和 V.斯里库马尔，编辑。

### 段落 370 · Page 35

**EN**

Bangkok, Thailand and virtual meeting: Association for Computational Linguistics, Aug. 2024. [199] S. Chen, B. J. Gutierrez, and Y. Su, “Attention in large language models yields efficient zero-shot rerankers,” inICLR. OpenReview.net, 2025. [200] C. Meng, N. Arabzadeh, A. Askari, M. Aliannejadi, and M. de Rijke, “Ranked list truncation for large language model-based re-ranking,” inSIGIR. ACM, 2024, pp. 141–151. [201] H. Wachsmuth, S. Syed, and B.

**中文**

泰国曼谷和虚拟会议：计算语言学协会，2024 年 8 月。[199] S. Chen、B. J. Gutierrez 和 Y. Su，“大语言模型中的注意力产生高效的零样本重排序”，载于 ICLR。 OpenReview.net，2025。[200] C.Meng、N.Arabzadeh、A.Askari、M.Aliannejadi 和 M.de Rijke，“基于大型语言模型的重排的排名列表截断”，inSIGIR。 ACM，2024 年，第 141–151 页。 [201] H. Wachsmuth、S. Syed 和 B.

### 段落 371 · Page 35

**EN**

Stein, “Retrieval of the best counterargument without prior topic knowledge,” inProceedings of the 56th Annual Meeting of the Association for Computational Linguistics, ACL 2018, Melbourne, Australia, July 15-20, 2018, Volume 1: Long Papers, I. Gurevych and Y. Miyao, Eds. Association for Computational Linguistics, 2018, pp. 241–251. [202] K. Guu, K. Lee, Z. Tung, P . Pasupat, and M. Chang, “Retrieval augmented language model pre-training,” inProceedings of the 37th International Conference on Machine Learning, ICML 2020, 13-18 July 2020, Virtual Event, ser. Proceedings of Machine Learning Research, vol. 119. PMLR, 2020, pp. 3929–3938.

**中文**

Stein，“在没有先验主题知识的情况下检索最佳反驳”，载于计算语言学协会第 56 届年会记录，ACL 2018，澳大利亚墨尔本，2018 年 7 月 15-20 日，第 1 卷：长论文，I. Gurevych 和 Y. Miyao，编辑。计算语言学协会，2018 年，第 241-251 页。 [202] 顾国强、李国强、董志平。 Pasupat 和 M. Chang，“检索增强语言模型预训练”，第 37 届国际机器学习会议记录，ICML 2020，2020 年 7 月 13-18 日，虚拟活动，系列。机器学习研究论文集，卷。 119.PMLR，2020 年，第 3929-3938 页。

### 段落 372 · Page 35

**EN**

[203] P . S. H. Lewis, E. Perez, A. Piktus, F. Petroni, V . Karpukhin, N. Goyal, H. K¨uttler, M. Lewis, W. Yih, T. Rockt ¨aschel, S. Riedel, and D. Kiela, “Retrievalaugmented generation for knowledge-intensive NLP tasks,” inAdvances in Neural Information Processing Systems 33: Annual Conference on Neural Information Processing Systems 2020, NeurIPS 2020, December 6-12, 2020, virtual, H. Larochelle, M. Ranzato, R. Hadsell, M. Balcan, and H. Lin, Eds., 2020. [204] W. Shi, S. Min, M. Yasunaga, M. Seo, R. James, M. Lewis, L. Zettlemoyer, and W.

**中文**

[203] P. S.H.刘易斯、E.佩雷斯、A.皮克图斯、F.佩特罗尼、V。 Karpukhin、N. Goyal、H. Küttler、M. Lewis、W. Yih、T. Rockt ¡aschel、S. Riedel 和 D. Kiela，“知识密集型 NLP 任务的检索生成”，发表于《神经信息处理系统进展》第 33 期：2020 年神经信息处理系统年会，NeurIPS 2020，12 月 6-12 日， 2020 年，虚拟，H. Larochelle、M. Ranzato、R. Hadsell、M. Balcan 和 H. Lin，Eds.，2020。 [204] W. Shi、S. Min、M. Yasunaga、M. Seo、R. James、M. Lewis、L. Zettlemoyer 和 W.

### 段落 373 · Page 35

**EN**

Yih, “REPLUG: retrieval-augmented black-box language models,” in Proceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers), NAACL 2024, Mexico City, Mexico, June 16-21, 2024, K. Duh, H. G ´omez-Adorno, and S. Bethard, Eds. Association for Computational Linguistics, 2024, pp. 8371–8384. [205] G. Izacard, P . S. H. Lewis, M. Lomeli, L. Hos-

**中文**

Yih，“REPLUG：检索增强的黑盒语言模型”，载于计算语言学协会北美分会 2024 年会议记录：人类语言技术（第一卷：长论文），NAACL 2024，墨西哥墨西哥城，2024 年 6 月 16-21 日，K. Duh、H. G ´omez-Adorno 和 S.贝萨德，编辑。计算语言学协会，2024 年，第 8371–8384 页。 [205] G.伊扎卡尔，P。 S. H. 刘易斯、M. 洛梅利、L. 霍斯-

### Page 36

### 段落 374 · Page 36

**EN**

36 seini, F. Petroni, T. Schick, J. Dwivedi-Yu, A. Joulin, S. Riedel, and E. Grave, “Atlas: Few-shot learning with retrieval augmented language models,”J. Mach. Learn. Res., vol. 24, pp. 251:1–251:43, 2023. [206] A. Lazaridou, E. Gribovskaya, W. Stokowiec, and N. Grigorev, “Internet-augmented language models through few-shot prompting for open-domain question answering,”CoRR, vol. abs/2203.05115, 2022. [207] H. He, H. Zhang, and D. Roth, “Rethinking with retrieval: Faithful large language model inference,” CoRR, vol. abs/2301.00303, 2023. [208] W. Yu, H. Zhang, X. Pan, P . Cao, K. Ma, J. Li, H. Wang, and D.

**中文**

36 seini、F. Petroni、T. Schick、J. Dwivedi-Yu、A. Joulin、S. Riedel 和 E. Grave，“Atlas：使用检索增强语言模型进行少量学习”，J.马赫。学习。研究，卷。 24，第 251:1–251:43，2023 年。 [206] A. Lazaridou、E. Gribovskaya、W. Stokowiec 和 N. Grigorev，“通过开放域问答的少量提示实现互联网增强语言模型”，CoRR，卷。 abs/2203.05115, 2022。 [207] H. He、H. Zhang 和 D. Roth，“检索检索的重新思考：忠实的大语言模型推理”，CoRR，卷。 abs/2301.00303, 2023. [208] 余伟, 张华, 潘X. P.曹，K. Ma，J. Li，H. Wang，和 D.

### 段落 375 · Page 36

**EN**

Yu, “Chain-of-note: Enhancing robustness in retrieval-augmented language models,” inProceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, EMNLP 2024, Miami, FL, USA, November 12-16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 14 672–14 685. [209] O. Ram, Y. Levine, I. Dalmedigos, D. Muhlgay, A. Shashua, K. Leyton-Brown, and Y. Shoham, “Incontext retrieval-augmented language models,”CoRR, vol. abs/2302.00083, 2023. [210] Z. Shao, Y. Gong, Y. Shen, M. Huang, N. Duan, and W.

**中文**

Yu，“Chain-of-note：增强检索增强语言模型的鲁棒性”，载于 2024 年自然语言处理经验方法会议论文集，EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 14 672–14 685 页。 [209] O. Ram、Y. Levine、I. Dalmedigos、D. Muhlgay、A. Shashua、K. Leyton-Brown 和 Y. Shoham，“上下文检索增强语言模型”，CoRR，卷。 abs/2302.00083, 2023. [210] 邵子，龚勇，沉阳，黄明，段宁，W.

### 段落 376 · Page 36

**EN**

Chen, “Enhancing retrieval-augmented large language models with iterative retrieval-generation synergy,” inFindings of the Association for Computational Linguistics: EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 9248–9274. [211] H. Trivedi, N. Balasubramanian, T. Khot, and A. Sabharwal, “Interleaving retrieval with chain-of-thought reasoning for knowledge-intensive multi-step questions,” inProceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), ACL 2023, Toronto, Canada, July 9-14, 2023, A.

**中文**

Chen，“通过迭代检索生成协同作用增强检索增强大型语言模型”，载于计算语言学协会的调查结果：EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 9248–9274 页。 [211] H. Trivedi、N. Balasubramanian、T. Khot 和 A. Sabharwal，“知识密集型多步骤问题的检索与思想链推理的交错”，载于计算语言学协会第 61 届年会记录（第 1 卷：长论文），ACL 2023，加拿大多伦多，7 月 9-14 日， 2023 年，A.

### 段落 377 · Page 36

**EN**

Rogers, J. L. Boyd-Graber, and N. Okazaki, Eds. Association for Computational Linguistics, 2023, pp. 10 014–10 037. [212] Z. Jiang, F. F. Xu, L. Gao, Z. Sun, Q. Liu, J. Dwivedi- Yu, Y. Yang, J. Callan, and G. Neubig, “Active retrieval augmented generation,” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 7969–7992. [213] A. Asai, Z. Wu, Y. Wang, A. Sil, and H.

**中文**

罗杰斯，J. L. Boyd-Graber 和 N. Okazaki，编辑。计算语言学协会，2023，第 10 014–10 037 页。 [212] Z. Jiang、F. F. Xu、L. Gau、Z. Sun、Q. Liu、J. Dwivedi- Yu、Y. Yang、J. Callan 和 G. Neubig，“主动检索增强生成”，载于 2023 年自然科学经验方法会议论文集语言处理，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 7969–7992 页。 [213] A. Asai、Z. Wu、Y. Wang、A. Sil 和 H.

### 段落 378 · Page 36

**EN**

Hajishirzi, “Self-rag: Learning to retrieve, generate, and critique through self-reflection,” inThe Twelfth International Conference on Learning Representations, ICLR 2024, Vienna, Austria, May 7-11, 2024. OpenReview.net, 2024. [214] J. Liu, J. Jin, Z. Wang, J. Cheng, Z. Dou, and J. Wen, “RETA-LLM: A retrieval-augmented large language model toolkit,”CoRR, vol. abs/2306.05212, 2023. [215] T. Vu, M. Iyyer, X. Wang, N. Constant, J. W. Wei, J. Wei, C. Tar, Y. Sung, D. Zhou, Q. V . Le, and T.

**中文**

Hajishirzi，“自我抹布：通过自我反思学习检索、生成和批判”，载于第十二届学习表征国际会议，ICLR 2024，奥地利维也纳，2024 年 5 月 7-11 日。OpenReview.net，2024。 [214] J. Liu、J. Jin、Z. Wang、J. Cheng、Z. Dou 和 J. Wen， “RETA-LLM：检索增强的大型语言模型工具包”，CoRR，卷。 abs/2306.05212, 2023. [215] T. Vu, M. Iyyer, X. Wang, N. Constant, J. W. Wei, J. Wei, C. Tar, Y. Sung, D. Zhou, Q. V.勒，T.

### 段落 379 · Page 36

**EN**

Luong, “Freshllms: Refreshing large language models with search engine augmentation,” inFindings of the Association for Computational Linguistics, ACL 2024, Bangkok, Thailand and virtual meeting, August 11-16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 13 697–13 720. [216] X. Lyu, S. Grafberger, S. Biegel, S. Wei, M. Cao, S. Schelter, and C. Zhang, “Improving retrievalaugmented large language models via data importance learning,”CoRR, vol. abs/2307.03027, 2023. [217] S. Wang, X. Yu, M. Wang, W. Chen, Y. Zhu, and Z.

**中文**

Luong，“Freshllms：通过搜索引擎增强刷新大型语言模型”，载于计算语言学协会的调查结果，ACL 2024，泰国曼谷和虚拟会议，2024 年 8 月 11 日至 16 日，L. Ku、A. Martins 和 V。斯里库马尔，编辑。计算语言学协会，2024 年，第 13 697–13 720 页。 [216] X. Lyu、S. Grafberger、S. Biegel、S. Wei、M. Cao、S. Schelter 和 C. Zhang，“通过数据重要性学习改进检索增强大型语言模型”，CoRR，卷。 abs/2307.03027, 2023。 [217] S. Wang, X. Yu, M. Wang, W. Chen, Y. Zhu, and Z.

### 段落 380 · Page 36

**EN**

Dou, “Richrag: Crafting rich responses for multifaceted queries in retrieval-augmented generation,” inProceedings of the 31st International Conference on Computational Linguistics, COLING 2025, Abu Dhabi, UAE, January 19-24, 2025, O. Rambow, L. Wanner, M. Apidianaki, H. Al-Khalifa, B. D. Eugenio, and S. Schockaert, Eds. Association for Computational Linguistics, 2025, pp. 11 317–11 333. [218] Y. Zhu, J. Jin, H. Qian, Z. Liu, Z. Dou, and J. Wen, “Single llm, multiple roles: A unified retrieval-augmented generation framework using role-specific token optimization,”CoRR, vol. abs/2505.15444, 2025. [219] Z. Jiang, X. Ma, and W.

**中文**

Dou，“Richrag：在检索增强生成中为多方面查询制作丰富的响应”，第 31 届国际计算语言学会议论文集，COLING 2025，阿联酋阿布扎比，2025 年 1 月 19-24 日，O. Rambow、L. Wanner、M. Apidianaki、H. Al-Khalifa、B. D. Eugenio 和S.Schockaert，编辑。计算语言学协会，2025，第 11 317–11 333 页。 [218] Y. Zhu、J. Jin、H. Qiu、Z. Liu、Z. Dou 和 J. Wen，“单一 llm，多个角色：使用特定于角色的标记优化的统一检索增强生成框架”，CoRR，卷。 abs/2505.15444, 2025. [219] Z. Jiang, X. Ma, and W.

### 段落 381 · Page 36

**EN**

Chen, “Longrag: Enhancing retrieval-augmented generation with long-context llms,”CoRR, vol. abs/2406.15319, 2024. [220] T. Gao, H. Yen, J. Yu, and D. Chen, “Enabling large language models to generate text with citations,” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 6465–6488. [221] Z. Xu, Z. Liu, Y. Liu, C. Xiong, Y. Yan, S. Wang, S. Yu, Z. Liu, and G. Yu, “Activerag: Revealing the treasures of knowledge via active learning,”CoRR, vol. abs/2402.13547, 2024.

**中文**

Chen，“Longrag：通过长上下文 LLMS 增强检索增强生成”，CoRR，卷。 abs/2406.15319，2024。 [220] T. Gau、H. Yen、J. Yu 和 D. Chen，“启用大型语言模型以生成带引文的文本”，载于 2023 年自然语言处理经验方法会议记录，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor, J.皮诺和 K. Bali，编辑。计算语言学协会，2023 年，第 6465–6488 页。 [221] 徐正、刘正、刘勇、熊昌、严彦、王胜、余胜、刘正、余刚，“Activerag：通过主动学习揭示知识的宝藏”，CoRR，卷。绝对/2402.13547，2024。

### 段落 382 · Page 36

**EN**

[222] X. Liang, S. Niu, Z. Li, S. Zhang, S. Song, H. Wang, J. Yang, F. Xiong, B. Tang, and C. Xi, “Empowering large language models to set up a knowledge retrieval indexer via self-learning,”CoRR, vol. abs/2405.16933, 2024. [223] Y. Wang, R. Ren, J. Li, X. Zhao, J. Liu, and J. Wen, “REAR: A relevance-aware retrievalaugmented framework for open-domain question answering,” inProceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, EMNLP 2024, Miami, FL, USA, November 12-16, 2024, Y. Al- Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 5613–5626. [224] H. Luo, T. Zhang, Y.

**中文**

[222] 梁X.，牛S.，李Z.，张S.，S.宋，H.王，J.杨，F.熊，B.唐，C.Xi，“赋能大型语言模型通过自学习建立知识检索索引器”，CoRR，卷。 abs/2405.16933，2024。[223] Y. Wang、R. Ren、J. Li、X. Zhu、J. Liu 和 J. Wen，“REAR：用于开放域问答的相关性感知检索增强框架”，载于 2024 年自然语言处理经验方法会议论文集，EMNLP 2024，美国佛罗里达州迈阿密，11 月2024 年 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 5613–5626 页。 [224] 罗浩，张涛，

### 段落 383 · Page 36

**EN**

Chuang, Y. Gong, Y. Kim, X. Wu, H. Meng, and J. R. Glass, “Search augmented instruction learning,” inFindings of the Association for Computational Linguistics: EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 3717–3729. [225] X. V . Lin, X. Chen, M. Chen, W. Shi, M. Lomeli, R. James, P . Rodriguez, J. Kahn, G. Szilvasy, M. Lewis, L. Zettlemoyer, and W. Yih, “RA-DIT: retrievalaugmented dual instruction tuning,” inThe Twelfth International Conference on Learning Representations, ICLR 2024, Vienna, Austria, May 7-11, 2024. OpenReview.net, 2024. [226] Z.

**中文**

Chang、Y.Gong、Y.Kim、X.Wu、H.Meng 和 J.R.Glass，“搜索增强教学学习”，载于计算语言学协会的调查结果：EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 3717-3729 页。 [225] X.V. Lin，X. Chen，M. Chen，W. Shi，M. Lomeli，R. James，P。 Rodriguez、J. Kahn、G. Szilvasy、M. Lewis、L. Zettlemoyer 和 W. Yih，“RA-DIT：检索增强双指令调优”，载于第十二届学习表示国际会议，ICLR 2024，奥地利维也纳，2024 年 5 月 7-11 日。OpenReview.net，2024 年。[226] Z.

### 段落 384 · Page 36

**EN**

Wei, W. Chen, and Y. Meng, “Instructrag: Instruct-

**中文**

Wei、W. Chen 和 Y.Meng，“Instructrag：指导-

### Page 37

### 段落 385 · Page 37

**EN**

37 ing retrieval-augmented generation with explicit denoising,”CoRR, vol. abs/2406.13629, 2024. [227] S. Xu, L. Pang, M. Yu, F. Meng, H. Shen, X. Cheng, and J. Zhou, “Unsupervised information refinement training of large language models for retrieval-augmented generation,” inProceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), ACL 2024, Bangkok, Thailand, August 11-16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 133–145. [228] Y. Zhu, Z. Huang, Z. Dou, and J. Wen, “One token can help!

**中文**

37 ing 具有显式去噪的检索增强生成，”CoRR，卷。 abs/2406.13629, 2024. [227] S. Xu, L. Pang, M. Yu, F. Meng, H. Shen, X. Cheng, and J. Zhou, “用于检索增强生成的大型语言模型的无监督信息细化训练”，载于计算语言学协会第 62 届年会论文集（第一卷：长论文），ACL 2024 年，泰国曼谷，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V .斯里库马尔，编辑。计算语言学协会，2024 年，第 133-145 页。 [228] Y. Zhu，Z. Huang，Z. Dou，J. Wen，“一个令牌可以帮助！

### 段落 386 · Page 37

**EN**

learning scalable and pluggable virtual tokens for retrieval-augmented large language models,” in AAAI-25, Sponsored by the Association for the Advancement of Artificial Intelligence, February 25 - March 4, 2025, Philadelphia, P A, USA, T. Walsh, J. Shah, and Z. Kolter, Eds. AAAI Press, 2025, pp. 26 166–26 174. [229] F. Ye, S. Li, Y. Zhang, and L. Chen, “Rˆ2ag: Incorporating retrieval information into retrieval augmented generation,”CoRR, vol. abs/2406.13249, 2024. [230] O. Yoran, T. Wolfson, O. Ram, and J.

**中文**

学习可扩展和可插入的虚拟标记以用于检索增强的大型语言模型”，载于 AAAI-25，由人工智能促进协会赞助，2025 年 2 月 25 日至 3 月 4 日，美国宾夕法尼亚州费城，T. Walsh、J. Shah 和 Z. Kolter，编辑。 AAAI Press，2025，第 26 166–26 174 页。 [229] F. Ye、S. Li、Y. Zhang 和 L. Chen，“Rˆ2ag：将检索信息纳入检索增强生成”，CoRR，卷。 abs/2406.13249, 2024。 [230] O. Yoran、T. Wolfson、O. Ram 和 J.

### 段落 387 · Page 37

**EN**

Berant, “Making retrieval-augmented language models robust to irrelevant context,” inThe Twelfth International Conference on Learning Representations, ICLR 2024, Vienna, Austria, May 7-11, 2024. OpenReview.net, 2024. [231] F. Fang, Y. Bai, S. Ni, M. Yang, X. Chen, and R. Xu, “Enhancing noise robustness of retrieval-augmented language models with adaptive adversarial training,” in Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), ACL 2024, Bangkok, Thailand, August 11-16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp.

**中文**

Berant，“使检索增强语言模型对不相关的上下文具有鲁棒性”，第十二届学习表示国际会议，ICLR 2024，奥地利维也纳，2024 年 5 月 7-11 日。OpenReview.net，2024。[231] F. Fang、Y. Bai、S. Ni、M. Yang、X. Chen 和 R. Xu，“增强检索增强的噪声鲁棒性具有适应性对抗训练的语言模型”，载于计算语言学协会第 62 届年会记录（第一卷：长论文），ACL 2024，泰国曼谷，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V .斯里库马尔，编辑。计算语言学协会，2024 年，第 14 页。

### 段落 388 · Page 37

**EN**

10 028–10 039. [232] J. Zhu, L. Yan, H. Shi, D. Yin, and L. Sha, “ATM: adversarial tuning multi-agent system makes a robust retrieval-augmented generator,” inProceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, EMNLP 2024, Miami, FL, USA, November 12-16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 10 902–10 919. [233] W. Yu, Z. Zhang, Z. Liang, M. Jiang, and A. Sabharwal, “Improving language models via plug-and-play retrieval feedback,”CoRR, vol. abs/2305.14002, 2023. [234] Z. Feng, X. Feng, D. Zhao, M. Yang, and B.

**中文**

10 028–10 039。 [232] J. Zhu、L. Yan、H. Shi、D. Yin 和 L. Sha，“ATM：对抗性调优多智能体系统打造强大的检索增强生成”，载于 2024 年自然语言处理经验方法会议记录，EMNLP 2024，美国佛罗里达州迈阿密，11 月 12-16 日， 2024 年，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 10 902–10 919 页。 [233] W. Yu、Z.Zhang、Z.Liang、M.Jiang 和 A.Sabharwal，“通过即插即用检索反馈改进语言模型”，CoRR，卷。 abs/2305.14002, 2023. [234] Z. Feng, X. Feng, D. Zhu, M. Yang, and B.

### 段落 389 · Page 37

**EN**

Qin, “Retrieval-generation synergy augmented large language models,” inIEEE International Conference on Acoustics, Speech and Signal Processing, ICASSP 2024, Seoul, Republic of Korea, April 14-19, 2024. IEEE, 2024, pp. 11 661–11 665. [235] D. Yang, J. Rao, K. Chen, X. Guo, Y. Zhang, J. Yang, and Y. Zhang, “IM-RAG: multi-round retrievalaugmented generation through learning inner monologues,” inProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2024, Washington DC, USA, July 14-18, 2024, G. H. Yang, H. Wang, S. Han, C. Hauff, G. Zuccon, and Y. Zhang, Eds. ACM, 2024, pp.

**中文**

秦，“检索生成协同增强大语言模型”，载于 IEEE 国际声学、语音和信号处理会议，ICASSP 2024，韩国首尔，2024 年 4 月 14-19 日。IEEE，2024，第 11 661–11 665 页。[235] D. Yang、J. Rao、K. Chen、X.Guo、Y.Zhang， J. Yang 和 Y. Zhang，“IM-RAG：通过学习内心独白进行多轮检索增强生成”，载于第 47 届国际 ACM SIGIR 信息检索研究与发展会议论文集，SIGIR 2024，美国华盛顿特区，2024 年 7 月 14-18 日，G. H. Yang、H. Wang、S. Han、C. Hauff、G. Zuccon 和Y.张，编辑。 ACM，2024 年，第 17 页。

### 段落 390 · Page 37

**EN**

730– 740. [236] Z. Shi, S. Zhang, W. Sun, S. Gao, P . Ren, Z. Chen, and Z. Ren, “Generate-then-ground in retrievalaugmented generation for multi-hop question answering,” inProceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), ACL 2024, Bangkok, Thailand, August 11-16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 7339–7353. [237] S. Kadavath, T. Conerly, A. Askell, T. Henighan, D. Drain, E. Perez, N. Schiefer, Z. Hatfield-Dodds, N. DasSarma, E. Tran-Johnson, S. Johnston, S. E. Showk, A. Jones, N. Elhage, T. Hume, A. Chen, Y.

**中文**

730–740。 [236] 史志，张三，孙文，高三，P。 Ren、Z. Chen 和 Z. Ren，“多跳问答的检索增强生成中的生成-然后接地”，计算语言学协会第 62 届年会记录（第一卷：长论文），ACL 2024，泰国曼谷，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V .斯里库马尔，编辑。计算语言学协会，2024 年，第 7339–7353 页。 [237] S. Kadavath、T. Conerly、A. Askell、T. Henighan、D. Drain、E. Perez、N. Schiefer、Z. Hatfield-Dodds、N. DasSarma、E. Tran-Johnson、S. Johnston、S. E. Showk、A. Jones、N. Elhage、T. Hume、A. Chen、Y.

### 段落 391 · Page 37

**EN**

Bai, S. Bowman, S. Fort, D. Ganguli, D. Hernandez, J. Jacobson, J. Kernion, S. Kravec, L. Lovitt, K. Ndousse, C. Olsson, S. Ringer, D. Amodei, T. Brown, J. Clark, N. Joseph, B. Mann, S. McCandlish, C. Olah, and J. Kaplan, “Language models (mostly) know what they know,”CoRR, vol. abs/2207.05221, 2022. [238] Z. Jiang, J. Araki, H. Ding, and G. Neubig, “How can we knowWhenlanguage models know? on the calibration of language models for question answering,” Trans. Assoc. Comput. Linguistics, vol. 9, pp. 962–977, 2021. [239] O. Press, M. Zhang, S. Min, L. Schmidt, N. A. Smith, and M.

**中文**

Bai、S. Bowman、S. Fort、D. Ganguli、D. Hernandez、J. Jacobson、J. Kernion、S. Kravec、L. Lovitt、K. Ndousse、C. Olsson、S. Ringer、D. Amodei、T. Brown、J. Clark、N. Joseph、B. Mann、S. McCandlish、C. Olah 和 J. Kaplan，“语言模型（大多数）知道什么他们知道，”CoRR，卷。 abs/2207.05221, 2022。 [238] Z. Jiang、J. Araki、H. Ding 和 G. Neubig，“我们如何知道语言模型何时知道？关于问答语言模型的校准”，Trans。副教授。计算。语言学，卷。 9，第 962–977 页，2021 年。 [239] O. Press、M. 张、S. Min、L. Schmidt、N. A. Smith 和 M.

### 段落 392 · Page 37

**EN**

Lewis, “Measuring and narrowing the compositionality gap in language models,” inFindings of the Association for Computational Linguistics: EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 5687–5711. [240] O. Khattab, K. Santhanam, X. L. Li, D. Hall, P . Liang, C. Potts, and M. Zaharia, “Demonstratesearch-predict: Composing retrieval and language models for knowledge-intensive NLP,”CoRR, vol. abs/2212.14024, 2022. [241] M. Lee, S. An, and M.

**中文**

Lewis，“测量和缩小语言模型中的组合性差距”，载于计算语言学协会的调查结果：EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 5687–5711 页。 [240] O. Khattab、K. Santhanam、X. L. Li、D. Hall、P。 Liang、C. Potts 和 M. Zaharia，“演示搜索预测：为知识密集型 NLP 构建检索和语言模型”，CoRR，卷。 abs/2212.14024, 2022。 [241] M. Lee, S. An 和 M.

### 段落 393 · Page 37

**EN**

Kim, “Planrag: A plan-thenretrieval augmented generation for generative large language models as decision makers,” inProceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers), NAACL 2024, Mexico City, Mexico, June 16-21, 2024, K. Duh, H. G ´omez-Adorno, and S. Bethard, Eds. Association for Computational Linguistics, 2024, pp. 6537–6555. [242] J. Wang, M. Chen, B. Hu, D. Yang, Z. Liu, Y. Shen, P . Wei, Z. Zhang, J. Gu, J. Zhou, J. Z. Pan, W. Zhang, and H.

**中文**

Kim，“Planrag：作为决策者的生成型大型语言模型的计划-然后检索增强生成”，载于 2024 年计算语言学协会北美分会会议记录：人类语言技术（第一卷：长论文），NAACL 2024，墨西哥墨西哥城，2024 年 6 月 16-21 日，K. Duh，H. G 'omez-Adorno 和 S. Bethard，编辑。计算语言学协会，2024 年，第 6537–6555 页。 [242] J.王，M.陈，B.胡，D.杨，Z.刘，Y.沉，P。魏，Z.张，J.顾，J.周，J.Z.潘，W.张，和H.

### 段落 394 · Page 37

**EN**

Chen, “Learning to plan for retrievalaugmented large language models from knowledge graphs,” inFindings of the Association for Computational Linguistics: EMNLP 2024, Miami, Florida, USA, November 12-16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 7813–7835. [243] O. Yoran, T. Wolfson, B. Bogin, U. Katz, D. Deutch, and J. Berant, “Answering questions by meta-reasoning over multiple chains of thought,” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds.

**中文**

Chen，“学习规划从知识图中检索增强的大型语言模型”，载于计算语言学协会的调查结果：EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 7813–7835 页。 [243] O. Yoran、T. Wolfson、B. Bogin、U. Katz、D. Deutch 和 J. Berant，“通过多个思想链的元推理回答问题”，载于 2023 年自然语言处理经验方法会议记录，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和K.巴厘岛，编辑。

### 段落 395 · Page 37

**EN**

Association for Computational Linguistics, 2023, pp. 5942–5966.

**中文**

计算语言学协会，2023 年，第 5942–5966 页。

### Page 38

### 段落 396 · Page 38

**EN**

38 [244] M. A. Arefeen, B. Debnath, and S. Chakradhar, “Leancontext: Cost-efficient domain-specific question answering using llms,”Nat. Lang. Process. J., vol. 7, p. 100065, 2024. [245] F. Xu, W. Shi, and E. Choi, “RECOMP: improving retrieval-augmented lms with context compression and selective augmentation,” inThe Twelfth International Conference on Learning Representations, ICLR 2024, Vienna, Austria, May 7-11, 2024. OpenReview.net, 2024. [246] Z. Wang, J. Araki, Z. Jiang, M. R. Parvez, and G. Neubig, “Learning to filter context for retrievalaugmented generation,”CoRR, vol. abs/2311.08377, 2023. [247] J. Liu, L. Li, T. Xiang, B.

**中文**

38 [244] M. A. Arefeen、B. Debnath 和 S. Chakradhar，“Leancontext：使用 llms 进行经济高效的特定领域问答”，Nat。郎.过程。 J.，卷。 7，p。 100065，2024。[245] F. Xu、W. Shi 和 E. Choi，“RECOMP：通过上下文压缩和选择性增强改进检索增强型 lms”，第十二届国际学习表征会议，ICLR 2024，奥地利维也纳，2024 年 5 月 7-11 日。OpenReview.net，2024 年。[246] Z. Wang， J. Araki、Z. Jiang、M. R. Parvez 和 G. Neubig，“学习过滤上下文以进行检索增强生成”，CoRR，卷。 abs/2311.08377, 2023. [247] 刘建, 李丽, 向涛, B.

### 段落 397 · Page 38

**EN**

Wang, and Y. Qian, “TCRA- LLM: token compression retrieval augmented large language model for inference cost reduction,” in Findings of the Association for Computational Linguistics: EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 9796–9810. [248] H. Yang, Z. Li, Y. Zhang, J. Wang, N. Cheng, M. Li, and J.

**中文**

Wang 和 Y.Qian，“TCRA-LLM：令牌压缩检索增强了大型语言模型以降低推理成本”，计算语言学协会的调查结果：EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 9796–9810 页。 [248] H.杨，Z.李，Y.张，J.王，N.程，M.李，和J.

### 段落 398 · Page 38

**EN**

Xiao, “PRCA: fitting black-box large language models for retrieval question answering via pluggable reward-driven contextual adapter,” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 5364–5375. [249] X. Cheng, X. Wang, X. Zhang, T. Ge, S. Chen, F. Wei, H. Zhang, and D.

**中文**

肖，“PRCA：通过可插入奖励驱动的上下文适配器拟合用于检索问题回答的黑盒大语言模型”，《2023 年自然语言处理经验方法会议论文集》，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 5364–5375 页。 [249] 程X.王X.张X.T.葛,S.陈S.陈,F.魏,X.张H.,D.

### 段落 399 · Page 38

**EN**

Zhao, “xrag: Extreme context compression for retrieval-augmented generation with one token,” inAdvances in Neural Information Processing Systems 38: Annual Conference on Neural Information Processing Systems 2024, NeurIPS 2024, Vancouver, BC, Canada, December 10 - 15, 2024, A. Globersons, L. Mackey, D. Belgrave, A. Fan, U. Paquet, J. M. Tomczak, and C. Zhang, Eds., 2024. [250] J. Jin, Y. Zhu, Y. Zhou, and Z.

**中文**

赵，“xrag：用一个令牌进行检索增强生成的极端上下文压缩”，载于神经信息处理系统进展 38：2024 年神经信息处理系统年会，NeurIPS 2024，加拿大不列颠哥伦比亚省温哥华，2024 年 12 月 10 - 15 日，A. Globersons、L. Mackey、D. Belgrave、A. Fan、U. Paquet、J. M. Tomczak 和 C. 张，编辑，2024。 [250] J. Jin，Y. Zhu，Y. Zhou，和 Z.

### 段落 400 · Page 38

**EN**

Dou, “BIDER: bridging knowledge inconsistency for efficient retrievalaugmented llms via key supporting evidence,” in Findings of the Association for Computational Linguistics, ACL 2024, Bangkok, Thailand and virtual meeting, August 11-16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 750–761. [251] N. F. Liu, K. Lin, J. Hewitt, A. Paranjape, M. Bevilacqua, F. Petroni, and P . Liang, “Lost in the middle: How language models use long contexts,”Trans. Assoc. Comput. Linguistics, vol. 12, pp. 157–173, 2024. [252] R. Ren, Y. Wang, Y. Qu, W. X. Zhao, J. Liu, H. Wu, J. Wen, and H.

**中文**

Dou，“BIDER：通过关键支持证据弥合知识不一致，实现高效检索增强 llms”，计算语言学协会的调查结果，ACL 2024，泰国曼谷和虚拟会议，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V。斯里库马尔，编辑。计算语言学协会，2024 年，第 750–761 页。 [251] N. F. Liu、K. Lin、J. Hewitt、A. Paranjape、M. Bevilacqua、F. Petroni 和 P。梁，“迷失在中间：语言模型如何使用长上下文”，翻译。副教授。计算。语言学，卷。 12，第 157-173 页，2024 年。 [252] R. Ren，Y. Wang，Y. Qu，W. X. Zhao，J. Liu，H. Wu，J. Wen，and H.

### 段落 401 · Page 38

**EN**

Wang, “Investigating the factual knowledge boundary of large language models with retrieval augmentation,” inProceedings of the 31st International Conference on Computational Linguistics, COLING 2025, Abu Dhabi, UAE, January 19-24, 2025, O. Rambow, L. Wanner, M. Apidianaki, H. Al-Khalifa, B. D. Eugenio, and S. Schockaert, Eds. Association for Computational Linguistics, 2025, pp. 3697–3715. [253] Y. Liu, S. Yavuz, R. Meng, M. Moorthy, S. Joty, C. Xiong, and Y. Zhou, “Exploring the integration strategies of retriever and large language models,” CoRR, vol. abs/2308.12574, 2023. [254] R. Aksitov, C. Chang, D. Reitter, S. Shakeri, and Y.

**中文**

Wang，“通过检索增强研究大语言模型的事实知识边界”，载于第 31 届国际计算语言学会议论文集，COLING 2025，阿联酋阿布扎比，2025 年 1 月 19-24 日，O. Rambow、L. Wanner、M. Apidianaki、H. Al-Khalifa、B. D. Eugenio 和 S.肖卡特，编辑。计算语言学协会，2025 年，第 3697–3715 页。 [253] Y. Liu，S. Yavuz，R. Meng，M. Moorthy，S. Joty，C. Xiong，and Y. Zhou，“探索检索器和大语言模型的集成策略”，CoRR，卷。 abs/2308.12574, 2023。 [254] R. Aksitov、C. Chang、D. Reitter、S. Shakeri 和 Y.

### 段落 402 · Page 38

**EN**

Sung, “Characterizing attribution and fluency tradeoffs for retrieval-augmented large language models,”CoRR, vol. abs/2302.05578, 2023. [255] A. Mallen, A. Asai, V . Zhong, R. Das, D. Khashabi, and H. Hajishirzi, “When not to trust language models: Investigating effectiveness of parametric and nonparametric memories,” inProceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), ACL 2023, Toronto, Canada, July 9-14, 2023, A. Rogers, J. L. Boyd-Graber, and N. Okazaki, Eds. Association for Computational Linguistics, 2023, pp. 9802–9822. [256] H. Ding, L. Pang, Z. Wei, H. Shen, and X.

**中文**

Sung，“表征检索增强型大型语言模型的归因和流畅性权衡”，CoRR，卷。 abs/2302.05578, 2023。 [255] A. Mallen, A. Asai, V . Chung, R. Das, D. Khashabi, 和 H. Hajishirzi，“何时不信任语言模型：调查参数和非参数记忆的有效性”，载于计算语言学协会第 61 届年会记录（第一卷：长论文），ACL 2023，加拿大多伦多，2023 年 7 月 9-14 日，A. Rogers, J. L. Boyd-Graber 和 N. Okazaki，编辑。计算语言学协会，2023 年，第 9802–9822 页。 [256] H.丁，L.庞，Z.魏，H.沉，X.

### 段落 403 · Page 38

**EN**

Cheng, “Retrieve only when it needs: Adaptive retrieval augmentation for hallucination mitigation in large language models,”CoRR, vol. abs/2402.10612, 2024. [257] H. Wang, B. Xue, B. Zhou, T. Zhang, C. Wang, G. Chen, H. Wang, and K. Wong, “Self-dc: When to retrieve and when to generate? self divide-and-conquer for compositional unknown questions,”CoRR, vol. abs/2402.13514, 2024. [258] S. Maekawa, H. Iso, S. Gurajada, and N. Bhutani, “Retrieval helps or hurts?

**中文**

Cheng，“仅在需要时检索：大语言模型中用于减轻幻觉的自适应检索增强”，CoRR，卷。 abs/2402.10612, 2024. [257] H. Wang, B. Xu, B. Zhou, T. Zhang, C. Wang, G. Chen, H. Wang, and K. Wong, “Self-dc：何时检索和何时生成？组合未知问题的自我分而治之”，CoRR，卷。 abs/2402.13514, 2024. [258] S. Maekawa、H. Iso、S. Gurajada 和 N. Bhutani，“检索是有帮助还是有伤害？

### 段落 404 · Page 38

**EN**

A deeper dive into the efficacy of retrieval augmentation to language models,” in Proceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers), NAACL 2024, Mexico City, Mexico, June 16-21, 2024, K. Duh, H. G ´omez-Adorno, and S. Bethard, Eds. Association for Computational Linguistics, 2024, pp. 5506–5521. [259] S. Ni, K. Bi, J. Guo, and X. Cheng, “When do llms need retrieval augmentation?

**中文**

深入探讨检索增强对语言模型的功效”，载于计算语言学协会北美分会 2024 年会议记录：人类语言技术（第一卷：长论文），NAACL 2024，墨西哥墨西哥城，2024 年 6 月 16-21 日，K. Duh、H. G ´omez-Adorno 和 S. Bethard，编辑。计算语言学协会，2024 年，第 5506–5521 页。 [259] S. Ni、K. Bi、J.Guo 和 X. Cheng，“LLMS 何时需要检索增强？

### 段落 405 · Page 38

**EN**

mitigating llms’ overconfidence helps retrieval augmentation,” inFindings of the Association for Computational Linguistics, ACL 2024, Bangkok, Thailand and virtual meeting, August 11- 16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 11 375–11 388. [260] Y. Wang, P . Li, M. Sun, and Y. Liu, “Self-knowledge guided retrieval augmentation for large language models,” inFindings of the Association for Computational Linguistics: EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 10 303–10 315. [261] J. Tan, Z.

**中文**

减轻 LLMS 的过度自信有助于检索增强”，见计算语言学协会的调查结果，ACL 2024，泰国曼谷和虚拟会议，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V。斯里库马尔，编辑。计算语言学协会，2024 年，第 11 375–11 388 页。 [260] Y. Wang, P . Li、M. Sun 和 Y. Liu，“大型语言模型的自我知识引导检索增强”，载于计算语言学协会的调查结果：EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 10 303–10 315 页。 [261] J. Tan, Z.

### 段落 406 · Page 38

**EN**

Dou, Y. Zhu, P . Guo, K. Fang, and J. Wen, “Small models, big insights: Leveraging slim proxy models to decide when and what to retrieve for llms,” inProceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), ACL 2024, Bangkok, Thailand, August 11- 16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 4420–4436. [262] Z. Jin, P . Cao, Y. Chen, K. Liu, X. Jiang, J. Xu, Q. Li, and J. Zhao, “Tug-of-war between knowl-

**中文**

窦勇.朱平.郭、K. Fang 和 J. Wen，“小模型，大见解：利用细长的代理模型来决定 llms 的检索时间和内容”，载于计算语言学协会第 62 届年会记录（第一卷：长论文），ACL 2024，泰国曼谷，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V .斯里库马尔，编辑。计算语言学协会，2024 年，第 4420–4436 页。 [262] Z.金，P。曹，Y. Chen，K. Liu，X. Jiang，J. Xu，Q. Li，J. Zhao，“知识与知识之间的拉锯战”

### Page 39

### 段落 407 · Page 39

**EN**

39 edge: Exploring and resolving knowledge conflicts in retrieval-augmented language models,” inProceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation, LREC/COLING 2024, 20-25 May, 2024, Torino, Italy, N. Calzolari, M. Kan, V . Hoste, A. Lenci, S. Sakti, and N. Xue, Eds. ELRA and ICCL, 2024, pp. 16 867–16 878. [263] S. Cho, S. Jeong, J. Seo, T. Hwang, and J.

**中文**

39 边缘：探索和解决检索增强语言模型中的知识冲突，”2024 年计算语言学、语言资源和评估联合国际会议论文集，LREC/COLING 2024，2024 年 5 月 20-25 日，意大利都灵，N. Calzolari、M. Kan、V . Hoste、A.Lenci、S.Sakti 和 N.Xue，编辑。 ELRA 和 ICCL，2024 年，第 16 867–16 878 页。 [263] S. Cho、S. Jeong、J. Seo、T. Hwang 和 J.

### 段落 408 · Page 39

**EN**

Park, “Typos that broke the rag’s back: Genetic attack on RAG pipeline by simulating documents in the wild via lowlevel perturbations,” inFindings of the Association for Computational Linguistics: EMNLP 2024, Miami, Florida, USA, November 12-16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 2826–2844. [264] J. Xue, M. Zheng, Y. Hu, F. Liu, X. Chen, and Q. Lou, “Badrag: Identifying vulnerabilities in retrieval augmented generation of large language models,”CoRR, vol. abs/2406.00083, 2024. [265] H. Chaudhari, G. Severi, J. Abascal, M. Jagielski, C. A. Choquette-Choo, M. Nasr, C.

**中文**

Park，“彻底的打字错误：通过低级扰动模拟野外文档对 RAG 管道进行基因攻击”，载于计算语言学协会的调查结果：EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 2826-2844 页。 [264] J.薛，M.郑，Y.Hu，F.Liu，X.Chen，和Q.Lou，“Badrag：识别大语言模型检索增强生成中的漏洞”，CoRR，卷。 abs/2406.00083, 2024。 [265] H. Chaudhari、G. Severi、J. Abascal、M. Jagielski、C. A. Choquette-Choo、M. Nasr、C.

### 段落 409 · Page 39

**EN**

Nita-Rotaru, and A. Oprea, “Phantom: General trigger attacks on retrieval augmented language generation,”CoRR, vol. abs/2405.20485, 2024. [266] S. Wang, J. Liu, S. Song, J. Cheng, Y. Fu, P . Guo, K. Fang, Y. Zhu, and Z. Dou, “Domainrag: A chinese benchmark for evaluating domain-specific retrievalaugmented generation,”CoRR, vol. abs/2406.05654, 2024. [267] F. Cuconasu, G. Trappolini, N. Tonellotto, and F. Silvestri, “A tale of trust and accuracy: Base vs. instruct llms in RAG systems,”CoRR, vol. abs/2406.14972, 2024. [268] Y. Wang, X. Ma, and W. Chen, “Augmenting blackbox llms with medical textbooks for clinical question answering,”CoRR, vol.

**中文**

Nita-Rotaru 和 A. Oprea，“Phantom：对检索增强语言生成的一般触发攻击”，CoRR，卷。 abs/2405.20485, 2024. [266] 王胜，刘建，宋胜，程建，付勇，P.郭，K. Fang，Y. Zhu，Z. Dou，“Domainrag：评估特定领域检索增强生成的中国基准”，CoRR，卷。 abs/2406.05654, 2024。 [267] F. Cuconasu、G. Trappolini、N. Tonellotto 和 F. Silvestri，“信任与准确性的故事：RAG 系统中的基础与指导 llms”，CoRR，卷。 Abs/2406.14972，2024。 [268] Y. Wang、X. Ma 和 W. Chen，“利用医学教科书增强黑盒 LLMS 进行临床问答”，CoRR，卷。

### 段落 410 · Page 39

**EN**

abs/2309.02233, 2023. [269] S. Munikoti, A. Acharya, S. Wagle, and S. Horawalavithana, “ATLANTIC: structureaware retrieval-augmented language model for interdisciplinary science,”CoRR, vol. abs/2311.12289, 2023. [270] X. Li, E. Nie, and S. Liang, “Crosslingual retrieval augmented in-context learning for bangla,”CoRR, vol. abs/2311.00587, 2023. [271] A. Lozano, S. L. Fleming, C. Chiang, and N. Shah, “Clinfo.ai: An open-source retrieval-augmented large language model system for answering medical questions using scientific literature,”CoRR, vol. abs/2310.16146, 2023. [272] B. Zhang, H. Yang, T. Zhou, A. Babar, and X.

**中文**

abs/2309.02233，2023。 [269] S. Munikoti、A. Acharya、S. Wagle 和 S. Horawalavithana，“大西洋：跨学科科学的结构感知检索增强语言模型”，CoRR，卷。 Abs/2311.12289, 2023。 [270] X. Li, E. Nie, and S. Liang, “跨语言检索增强孟加拉语境中的学习”，CoRR，卷。 Abs/2311.00587，2023。 [271] A. Lozano、S. L. Fleming、C. Jiang 和 N. Shah，“Clinfo.ai：一种使用科学文献回答医学问题的开源检索增强大型语言模型系统”，CoRR，卷。 abs/2310.16146, 2023. [272] B. 张、H. 杨、T. 周、A. Babar 和 X.

### 段落 411 · Page 39

**EN**

Liu, “Enhancing financial sentiment analysis via retrieval augmented large language models,” in4th ACM International Conference on AI in Finance, ICAIF 2023, Brooklyn, NY, USA, November 27-29, 2023. ACM, 2023, pp. 349–356. [273] A. Louis, G. van Dijck, and G.

**中文**

Liu，“通过检索增强大语言模型增强金融情绪分析”，第四届 ACM 国际金融人工智能会议，ICAIF 2023，美国纽约布鲁克林，2023 年 11 月 27-29 日。ACM，2023 年，第 349-356 页。 [273] A.路易斯，G.范迪克，和G.

### 段落 412 · Page 39

**EN**

Spanakis, “Interpretable long-form legal question answering with retrievalaugmented large language models,” inThirty-Eighth AAAI Conference on Artificial Intelligence, AAAI 2024, Thirty-Sixth Conference on Innovative Applications of Artificial Intelligence, IAAI 2024, Fourteenth Symposium on Educational Advances in Artificial Intelligence, EAAI 2014, February 20-27, 2024, Vancouver, Canada, M. J. Wooldridge, J. G. Dy, and S. Natarajan, Eds. AAAI Press, 2024, pp. 22 266–22 275. [274] Z. Wang, S. X. Teo, J. Ouyang, Y. Xu, and W.

**中文**

Spanakis，“可解释的长格式法律问答与检索增强大语言模型”，载于第三十八届 AAAI 人工智能会议，AAAI 2024，第三十六届人工智能创新应用会议，IAAI 2024，第十四届人工智能教育进展研讨会，EAAI 2014，2024 年 2 月 20-27 日，温哥华，加拿大，M. J. Wooldridge、J. G. Dy 和 S. Natarajan，编辑。 AAAI 出版社，2024 年，第 22 266–22 275 页。 [274] Z. Wang、S. X. Teo、J. Ouyang、Y. Xu 和 W.

### 段落 413 · Page 39

**EN**

Shi, “M-RAG: reinforcing large language model performance through retrieval-augmented generation with multiple partitions,” inProceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), ACL 2024, Bangkok, Thailand, August 11-16, 2024, L. Ku, A. Martins, and V . Srikumar, Eds. Association for Computational Linguistics, 2024, pp. 1966–1978. [275] G. Zyskind, T. South, and A. Pentland, “Don’t forget private retrieval: distributed private similarity search for large language models,”CoRR, vol. abs/2311.12955, 2023. [276] W. Jiang, M. Zeller, R. Waleffe, T. Hoefler, and G.

**中文**

Shi，“M-RAG：通过多个分区的检索增强生成来增强大型语言模型性能”，载于计算语言学协会第 62 届年会论文集（第一卷：长论文），ACL 2024，泰国曼谷，2024 年 8 月 11-16 日，L. Ku、A. Martins 和 V .斯里库马尔，编辑。计算语言学协会，2024 年，第 1966-1978 页。 [275] G. Zyskind、T. South 和 A. Pentland，“不要忘记私有检索：大型语言模型的分布式私有相似性搜索”，CoRR，卷。 abs/2311.12955, 2023。 [276] W. Jiang、M. Zeller、R. Waleffe、T. Hoefler 和 G.

### 段落 414 · Page 39

**EN**

Alonso, “Chameleon: a heterogeneous and disaggregated accelerator system for retrieval-augmented language models,”Proc. VLDB Endow., vol. 18, no. 1, pp. 42–52, 2024. [277] Y. Hoshi, D. Miyashita, Y. Ng, K. Tatsuno, Y. Morioka, O. Torii, and J. Deguchi, “Ralle: A framework for developing and evaluating retrieval-augmented large language models,” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023 - System Demonstrations, Singapore, December 6-10, 2023, Y. Feng and E. Lefever, Eds. Association for Computational Linguistics, 2023, pp. 52–69. [278] J. Jin, Y. Zhu, Z. Dou, G. Dong, X. Yang, C.

**中文**

阿隆索，“变色龙：用于检索增强语言模型的异构和分类加速器系统”，Proc。 VLDB 捐赠，卷。 18、没有。 1，第 42-52 页，2024 年。[277] Y. Hoshi、D. Miyashita、Y. Ng、K. Tatsuno、Y. Morioka、O. Torii 和 J. Deguchi，“Ralle：开发和评估检索增强大语言模型的框架”，载于 2023 年自然语言处理经验方法会议记录，EMNLP 2023 - 系统演示，新加坡，2023 年 12 月 6-10 日，Y. Feng 和 E. Lefever，编辑。计算语言学协会，2023 年，第 52-69 页。 [278] 金建，朱勇，窦正，董刚，杨旭，C.

### 段落 415 · Page 39

**EN**

Zhang, T. Zhao, Z. Yang, and J. Wen, “Flashrag: A modular toolkit for efficient retrieval-augmented generation research,” inCompanion Proceedings of the ACM on Web Conference 2025, WWW 2025, Sydney, NSW, Australia, 28 April 2025 - 2 May 2025, G. Long, M. Blumestein, Y. Chang, L. Lewin-Eytan, Z. H. Huang, and E. Yom- Tov, Eds. ACM, 2025, pp. 737–740. [279] R. Thoppilan, D. D. Freitas, J. Hall, N. Shazeer, A. Kulshreshtha, H. Cheng, A. Jin, T. Bos, L. Baker, Y. Du, Y. Li, H. Lee, H. S. Zheng, A. Ghafouri, M. Menegali, Y. Huang, M. Krikun, D. Lepikhin, J. Qin, D. Chen, Y. Xu, Z. Chen, A. Roberts, M. Bosma, Y. Zhou, C. Chang, I. Krivokon, W.

**中文**

张，T. 赵，Z. 杨，和 J. Wen，“Flashrag：用于高效检索增强生成研究的模块化工具包”，载于 ACM 2025 年网络会议配套论文集，WWW 2025，澳大利亚新南威尔士州悉尼，2025 年 4 月 28 日至 2025 年 5 月 2 日，G. Long、M. Blumestein、Y. Chang、L. Lewin-Eytan、Z. H. Huang 和 E. Yom-Tov，编辑。 ACM，2025 年，第 737–740 页。 [279] R. Thoppilan、D. D. Freitas、J. Hall、N. Shazeer、A. Kulshreshtha、H. Cheng、A. Jin、T. Bos、L. Baker、Y. Du、Y. Li、H. Lee、H. S. Cheng、A. Ghafouri、M. Menegali、Y. Huang、M. Krikun、D. Lepikhin、J. Qing、D. Chen、Y. Xu、Z. Chen, A. Roberts, M. Bosma, Y. Zhou, C. Chang, I. Krivokon, W.

### 段落 416 · Page 39

**EN**

Rusch, M. Pickett, K. S. Meier-Hellstern, M. R. Morris, T. Doshi, R. D. Santos, T. Duke, J. Soraker, B. Zevenbergen, V . Prabhakaran, M. Diaz, B. Hutchinson, K. Olson, A. Molina, E. Hoffman-John, J. Lee, L. Aroyo, R. Rajakumar, A. Butryna, M. Lamm, V . Kuzmina, J. Fenton, A. Cohen, R. Bernstein, R. Kurzweil, B. A. y Arcas, C. Cui, M. Croak, E. H. Chi, and Q. Le, “Lamda: Language models for dialog applications,”CoRR, vol. abs/2201.08239, 2022. [280] K. Shuster, M. Komeili, L. Adolphs, S. Roller, A. Szlam, and J.

**中文**

Rusch、M. Pickett、K. S. Meier-Hellstern、M. R. Morris、T. Doshi、R. D. Santos、T. Duke、J. Soraker、B. Zevenbergen、V . Prabhakaran、M. Diaz、B. Hutchinson、K. Olson、A. Molina、E. Hoffman-John、J. Lee、L. Aroyo、R. Rajakumar、A. Butryna、M. Lamm、V。 Kuzmina、J. Fenton、A. Cohen、R. Bernstein、R. Kurzweil、B. A. y Arcas、C. Cui、M. Croak、E. H. Chi 和 Q. Le，“Lamda：对话应用程序的语言模型”，CoRR，卷。 abs/2201.08239, 2022。 [280] K. Shuster、M. Komeili、L. Adolphs、S. Roller、A. Szlam 和 J.

### 段落 417 · Page 39

**EN**

Weston, “Language models that seek for knowledge: Modular search & generation for dialogue and prompt completion,” inFindings of the Association for Computational Linguistics: EMNLP 2022, Abu Dhabi, United Arab Emirates, December 7-11, 2022, Y. Goldberg, Z. Kozareva, and Y. Zhang, Eds. Association for Computational Linguistics, 2022, pp.

**中文**

Weston，“寻求知识的语言模型：对话和快速完成的模块化搜索和生成”，载于计算语言学协会的调查结果：EMNLP 2022，阿拉伯联合酋长国阿布扎比，2022 年 12 月 7-11 日，Y. Goldberg、Z. Kozareva 和 Y. Zhang，编辑。计算语言学协会，2022 年，第 14 页。

### Page 40

### 段落 418 · Page 40

**EN**

40 373–393. [281] X. Liu, H. Lai, H. Yu, Y. Xu, A. Zeng, Z. Du, P . Zhang, Y. Dong, and J. Tang, “Webglm: Towards an efficient web-enhanced question answering system with human preferences,” inProceedings of the 29th ACM SIGKDD Conference on Knowledge Discovery and Data Mining, KDD 2023, Long Beach, CA, USA, August 6-10, 2023, A. K. Singh, Y. Sun, L. Akoglu, D. Gunopulos, X. Yan, R. Kumar, F. Ozcan, and J. Ye, Eds. ACM, 2023, pp. 4549–4560. [282] I. Gur, H. Furuta, A. V . Huang, M. Safdari, Y. Matsuo, D. Eck, and A.

**中文**

40 373–393。 [281] 刘X.，赖H.，余H.，徐Y.，曾A.，杜Z.，P.张，Y. Dong，和 J. Tang，“Webglm：迈向符合人类偏好的高效网络增强问答系统”，载于第 29 届 ACM SIGKDD 知识发现和数据挖掘会议记录，KDD 2023，美国加利福尼亚州长滩，2023 年 8 月 6-10 日，A. K. Singh, Y. Sun, L. Akoglu, D. Gunopulos, X. Yan、R. Kumar、F. Ozcan 和 J. Ye，编辑。 ACM，2023 年，第 4549–4560 页。 [282] I.古尔，H.古尔塔，A.V。 Huang、M. Safdari、Y. Matsuo、D. Eck 和 A.

### 段落 419 · Page 40

**EN**

Faust, “A real-world webagent with planning, long context understanding, and program synthesis,” inThe Twelfth International Conference on Learning Representations, ICLR 2024, Vienna, Austria, May 7-11, 2024. OpenReview.net, 2024. [283] J. Menick, M. Trebacz, V . Mikulik, J. Aslanides, H. F. Song, M. J. Chadwick, M. Glaese, S. Young, L. Campbell-Gillingham, G. Irving, and N. McAleese, “Teaching language models to support answers with verified quotes,”CoRR, vol. abs/2203.11147, 2022. [284] X. Shi, J. Liu, Y. Liu, Q. Cheng, and W. Lu, “Know where to go: Make LLM a relevant, responsible, and trustworthy searchers,”Decis. Support Syst., vol.

**中文**

Faust，“具有规划、长上下文理解和程序综合功能的现实世界网络代理”，载于第十二届学习表示国际会议，ICLR 2024，奥地利维也纳，2024 年 5 月 7-11 日。OpenReview.net，2024 年。[283] J. Menick、M. Trebacz、V . Mikulik、J. Aslanides、H. F. Song、M. J. Chadwick、M. Glaese、S. Young、L. Campbell-Gillingham、G. Irving 和 N. McAleese，“教学语言模型以支持经过验证的引用的答案”，CoRR，卷。 abs/2203.11147, 2022. [284] X. Shi、J. Liu、Y. Liu、Q. Cheng 和 W. Lu，“知道该往哪里走：让法学硕士成为相关、负责和值得信赖的搜索者”，Decis。支持系统，卷。

### 段落 420 · Page 40

**EN**

188, p. 114354, 2025. [285] P . Gong, J. Li, and J. Mao, “Cosearchagent: A lightweight collaborative search agent with large language models,” inProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2024, Washington DC, USA, July 14-18, 2024, G. H. Yang, H. Wang, S. Han, C. Hauff, G. Zuccon, and Y. Zhang, Eds. ACM, 2024, pp. 2729–2733. [286] B. Jin, H. Zeng, Z. Yue, D. Wang, H. Zamani, and J. Han, “Search-r1: Training llms to reason and leverage search engines with reinforcement learning,” CoRR, vol. abs/2503.09516, 2025. [287] M. Chen, T. Li, H. Sun, Y. Zhou, C. Zhu, H.

**中文**

188，p。 114354, 2025. [285] P . Kong、J. Li 和 J. Mao，“Cosearchagent：具有大型语言模型的轻量级协作搜索代理”，载于第 47 届国际 ACM SIGIR 信息检索研究与发展会议论文集，SIGIR 2024，美国华盛顿特区，2024 年 7 月 14-18 日，G. H. Yang、H. Wang、S. Han、C. Hauff、G. Zuccon 和 Y. Zhang，编辑。 ACM，2024 年，第 2729–2733 页。 [286] B. Jin、H. Zeng、Z. Yue、D. Wang、H. Zamani 和 J. Han，“Search-r1：通过强化学习训练 llms 进行推理和利用搜索引擎”，CoRR，卷。 abs/2503.09516, 2025. [287] 陈明，李涛，孙红，周宇，朱成，H.

### 段落 421 · Page 40

**EN**

Wang, J. Z. Pan, W. Zhang, H. Chen, F. Yang, Z. Zhou, and W. Chen, “Research: Learning to reason with search for llms via reinforcement learning,”CoRR, vol. abs/2503.19470, 2025. [288] Z. Shao, P . Wang, Q. Zhu, R. Xu, J. Song, M. Zhang, Y. K. Li, Y. Wu, and D. Guo, “Deepseekmath: Pushing the limits of mathematical reasoning in open language models,”CoRR, vol. abs/2402.03300, 2024. [289] H. Song, J. Jiang, Y. Min, J. Chen, Z. Chen, W. X. Zhao, L. Fang, and J. Wen, “R1-searcher: Incentivizing the search capability in llms via reinforcement learning,” CoRR, vol. abs/2503.05592, 2025. [290] C. Li, M. Xue, Z. Zhang, J. Yang, B. Zhang, X. Wang, B.

**中文**

王，J. Z. 潘，W. 张，H. Chen，F. Yang，Z. Zhou，W. Chen，“研究：通过强化学习学习推理并搜索 llms”，CoRR，卷。 abs/2503.19470, 2025。 [288] Z. Shao, P . Wang，Q. Zhu，R. Xu，J. Song，M. Zhang，Y. K. Li，Y. Wu，and D.Guo，“Deepseekmath：在开放语言模型中突破数学推理的极限，”CoRR，卷。 abs/2402.03300, 2024. [289] H. Song, J. Jiang, Y. Min, J. Chen, Z. Chen, W. X. Zhu, L. Fang, and J. Wen, “R1-searcher: 通过强化学习激励 llms 中的搜索能力”，CoRR，卷。 abs/2503.05592, 2025. [290] 李成，薛明，张正，杨建，张本，王晓，B.

### 段落 422 · Page 40

**EN**

Yu, B. Hui, J. Lin, and D. Liu, “START: self-taught reasoner with tools,”CoRR, vol. abs/2503.04625, 2025. [291] Y. Deng, G. Wang, Z. Ying, X. Wu, J. Lin, W. Xiong, Y. Dai, S. Yang, Z. Zhang, Q. Wang, Y. Qin, Y. Wang, Q. Zha, S. Dai, and C. Meng, “Atom-searcher: Enhancing agentic deep research via fine-grained atomic thought reward,” 2025. [292] H. Pan, Z. Zhai, H. Yuan, Y. Lv, R. Fu, M. Liu, Z. Wang, and B. Qin, “Kwaiagents: Generalized informationseeking agent system with large language models,” CoRR, vol. abs/2312.04889, 2023. [293] L. Mei, Z. Yang, and C.

**中文**

Yu、B. Hui、J. Lin 和 D. Liu，“START：使用工具自学推理”，CoRR，卷。 abs/2503.04625, 2025. [291] Y. Deng, G. Wang, Z. Ying, X. Wu, J. Lin, W. Xiong, Y. Dai, S. Yang, Z.Zhang, Q. Wang, Y.qin, Y. Wang, Q. Zha, S. Dai, and C.Meng，“原子搜索者：通过细粒度原子思维奖励增强代理深度研究，” 2025. [292] H. Pan，Z. Zhai，H. Yuan，Y. Lv，R. Fu，M. Liu，Z. Wang，and B.qin，“Kwaiagents：具有大语言模型的广义信息搜索代理系统”，CoRR，卷。 abs/2312.04889, 2023. [293] L. Mei, Z. Yang, 和 C.

### 段落 423 · Page 40

**EN**

Chen, “Ai-searchplanner: Modular agentic search via pareto-optimal multiobjective reinforcement learning,” 2025. [294] Z. Chen, K. Liu, Q. Wang, J. Liu, W. Zhang, K. Chen, and F. Zhao, “Mindsearch: Mimicking human minds elicits deep AI searcher,” inThe Thirteenth International Conference on Learning Representations, ICLR 2025, Singapore, April 24-28, 2025. OpenReview.net, 2025. [295] J. Qiu, X. Qi, T. Zhang, X. Juan, J. Guo, Y. Lu, Y. Wang, Z. Yao, Q. Ren, X. Jiang, X. Zhou, D. Liu, L. Yang, Y. Wu, K. Huang, S. Liu, H. Wang, and M.

**中文**

Chen，“Ai-searchplanner：通过帕累托最优多目标强化学习进行模块化代理搜索”，2025 年。 [294] Z. Chen、K. Liu、Q. Wang、J. Liu、W. Zhang、K. Chen 和 F. Zhu，“Mindsearch：模仿人类思维引发深度 AI 搜索器”，第十三届学习表示国际会议，ICLR 2025，新加坡，4 月24-28, 2025. OpenReview.net, 2025. [295] J. Qiu, X. Qi, T. Zhang, X. Juan, J.Guo, Y. Lu, Y. Wang, Z. Yao, Q. Ren, X. Jiang, X. Zhou, D. Liu, L. Yang, Y. Wu, K. Huang, S. Liu, H. Wang, and M.

### 段落 424 · Page 40

**EN**

Wang, “Alita: Generalist agent enabling scalable agentic reasoning with minimal predefinition and maximal selfevolution,”CoRR, vol. abs/2505.20286, 2025. [296] M. Hu, Y. Zhou, W. Fan, Y. Nie, B. Xia, T. Sun, Z. Ye, Z. Jin, Y. Li, Q. Chen, Z. Zhang, Y. Wang, Q. Ye, B. Ghanem, P . Luo, and G. Li, “OWL: optimized workforce learning for general multi-agent assistance in real-world task automation,”CoRR, vol. abs/2505.23885, 2025. [297] K. Wan, H. Mu, R. Hao, H. Luo, T. Gu, and X.

**中文**

Wang，“Alita：通才智能体，以最小的预定义和最大的自我进化实现可扩展的代理推理”，CoRR，卷。 abs/2505.20286, 2025. [296] 胡明，周宇，范文，聂，夏，孙，叶，金，李，陈，张，王，叶，B. Ghanem, P. Luo 和 G. Li，“OWL：优化劳动力学习，以实现现实世界任务自动化中的通用多代理协助”，CoRR，卷。 abs/2505.23885, 2025. [297] K. Wan, H. Mu, R.hao, H. Luo, T. Gu, and X.

### 段落 425 · Page 40

**EN**

Chen, “A cognitive writing perspective for constrained longform text generation,” inFindings of the Association for Computational Linguistics, ACL 2025, Vienna, Austria, July 27 - August 1, 2025, W. Che, J. Nabende, E. Shutova, and M. T. Pilehvar, Eds. Association for Computational Linguistics, 2025, pp. 9832–9844. [298] P . Gong, J. Li, and J. Mao, “Cosearchagent: A lightweight collaborative search agent with large language models,” inProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR 2024, Washington DC, USA, July 14-18, 2024, G. H. Yang, H. Wang, S. Han, C. Hauff, G.

**中文**

Chen，“约束长文本生成的认知写作视角”，载于计算语言学协会的调查结果，ACL 2025，奥地利维也纳，2025 年 7 月 27 日至 8 月 1 日，W. Che、J. Nabende、E. Shutova 和 M. T. Pilehvar，编辑。计算语言学协会，2025 年，第 9832–9844 页。 [298] P. Kong, J. Li 和 J. Mao，“Cosearchagent：具有大型语言模型的轻量级协作搜索代理”，载于第 47 届国际 ACM SIGIR 信息检索研究与发展会议论文集，SIGIR 2024，美国华盛顿特区，2024 年 7 月 14-18 日，G. H. Yang、H. Wang、S. Han、C. Hauff、G.

### 段落 426 · Page 40

**EN**

Zuccon, and Y. Zhang, Eds. ACM, 2024, pp. 2729–2733. [299] X. Li, G. Dong, J. Jin, Y. Zhang, Y. Zhou, Y. Zhu, P . Zhang, and Z. Dou, “Search-o1: Agentic searchenhanced large reasoning models,”CoRR, vol. abs/2501.05366, 2025. [300] S. Schmidgall, Y. Su, Z. Wang, X. Sun, J. Wu, X. Yu, J. Liu, Z. Liu, and E. Barsoum, “Agent laboratory: Using LLM agents as research assistants,”CoRR, vol. abs/2501.04227, 2025. [301] C. Lu, C. Lu, R. T. Lange, J. N. Foerster, J. Clune, and D. Ha, “The AI scientist: Towards fully automated open-ended scientific discovery,”CoRR, vol. abs/2408.06292, 2024. [302] T. Yu, S. Zhang, and Y.

**中文**

Zuccon 和 Y.Zhang，编辑。 ACM，2024 年，第 2729–2733 页。 [299] 李X.，董G.，金J.，张Y.，周Y.，朱Y.，P.张和Z. Dou，“Search-o1：代理搜索增强的大型推理模型”，CoRR，卷。 Abs/2501.05366，2025。 [300] S. Schmidgall、Y. Su、Z. Wang、X. Sun、J. Wu、X. Yu、J. Liu、Z. Liu 和 E. Barsoum，“代理实验室：使用 LLM 代理作为研究助理”，CoRR，卷。 Abs/2501.04227，2025。 [301] C. Lu、C. Lu、R. T. Lange、J. N. Foerster、J. Clune 和 D. Ha，“人工智能科学家：迈向完全自动化的开放式科学发现”，CoRR，卷。绝对/2408.06292，2024。[302]T.Yu，S.Zhang，和Y.

### 段落 427 · Page 40

**EN**

Feng, “Auto-rag: Autonomous retrieval-augmented generation for large language models,”CoRR, vol. abs/2411.19443, 2024. [303] S. Sun, H. Song, Y. Wang, R. Ren, J. Jiang, J. Zhang, F. Bai, J. Deng, W. X. Zhao, Z. Liu, L. Fang, Z. Wang, and J. Wen, “Simpledeepsearcher: Deep information seeking via web-powered reasoning trajectory synthesis,”CoRR, vol. abs/2505.16834, 2025. [304] G. Dong, Y. Chen, X. Li, J. Jin, H. Qian, Y. Zhu, H. Mao, G. Zhou, Z. Dou, and J. Wen, “Tool-star: Empowering llm-brained multi-tool reasoner via reinforcement learning,”CoRR, vol. abs/2505.16410, 2025. [305] H. Sun, Z. Qiao, J. Guo, X. Fan, Y. Hou, Y. Jiang, P . Xie,

**中文**

Feng，“Auto-rag：大语言模型的自主检索增强生成”，CoRR，卷。 abs/2411.19443, 2024. [303] S. Sun, H. Song, Y. Wang, R. Ren, J. Jiang, J. Zhang, F. Bai, J. Deng, W. X. Zhao, Z. Liu, L. Fang, Z. Wang, and J. Wen，“Simpledeepsearcher：通过网络推理轨迹合成进行深度信息搜索”，CoRR，卷。 Abs/2505.16834, 2025. [304] G. Dong, Y. Chen, X. Li, J. Jin, H. Qian, Y. Zhu, H. Mao, G. Zhou, Z. Dou, and J. Wen, “工具之星：通过强化学习增强全脑多工具推理机”，CoRR，卷。 abs/2505.16410, 2025. [305] 孙宏，乔子，郭建，范晓，侯勇，江勇，P.谢，

### Page 41

### 段落 428 · Page 41

**EN**

41 Y. Zhang, F. Huang, and J. Zhou, “Zerosearch: Incentivize the search capability of llms without searching,” CoRR, vol. abs/2505.04588, 2025. [306] S. B. Islam, M. A. Rahman, K. S. M. T. Hossain, E. Hoque, S. Joty, and M. R. Parvez, “Open-rag: Enhanced retrieval augmented reasoning with opensource large language models,” inFindings of the Association for Computational Linguistics: EMNLP 2024, Miami, Florida, USA, November 12-16, 2024, Y. Al- Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 14 231–14 244. [307] X. Guan, J. Zeng, F. Meng, C. Xin, Y. Lu, H. Lin, X. Han, L. Sun, and J.

**中文**

41 Y.Zhang、F.Huang 和 J.Zhou，“Zerosearch：无需搜索即可激励 llms 的搜索能力”，CoRR，第 1 卷。 abs/2505.04588, 2025。 [306] S. B. Islam、M. A. Rahman、K. S. M. T. Hossain、E. Hoque、S. Joty 和 M. R. Parvez，“Open-rag：使用开源大语言模型增强检索增强推理”，收录于计算语言学协会的调查结果：EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024年，第14 231–14 244页。 [307] X.guan，J.Zeng，F.Meng，C.Xin，Y.Lu，H.Lin，X.Han，L.Sun，J.

### 段落 429 · Page 41

**EN**

Zhou, “Deeprag: Thinking to retrieve step by step for large language models,”arXiv preprint arXiv:2502.01142, 2025. [308] Z. Chen, M. Li, Y. Huang, Y. Du, M. Fang, and T. Zhou, “ATLAS: agent tuning via learning critical steps,” in Findings of the Association for Computational Linguistics, ACL 2025, Vienna, Austria, July 27 - August 1, 2025, W. Che, J. Nabende, E. Shutova, and M. T. Pilehvar, Eds. Association for Computational Linguistics, 2025, pp. 25 334–25 349. [309] L. Wang, H. Chen, N. Yang, X. Huang, Z. Dou, and F. Wei, “Chain-of-retrieval augmented generation,” CoRR, vol. abs/2501.14342, 2025. [310] T. Yu, S. Zhang, and Y.

**中文**

Zhou，“Deeprag：思考逐步检索大型语言模型”，arXiv 预印本 arXiv：2502.01142，2025。[308] Z. Chen、M. Li、Y. Huang、Y. Du、M. Fang 和 T. Zhou，“ATLAS：通过学习关键步骤进行代理调整”，计算语言学协会的发现，ACL 2025，维也纳，奥地利，2025 年 7 月 27 日至 8 月 1 日，W. Che、J. Nabende、E. Shutova 和 M. T. Pilehvar，编辑。计算语言学协会，2025，第 25 334–25 349 页。 [309] L. Wang、H. Chen、N. Yang、X. Huang、Z. Dou 和 F. Wei，“检索链增强生成”，CoRR，卷。 abs/2501.14342, 2025. [310] T. Yu, S. 张, 和 Y.

### 段落 430 · Page 41

**EN**

Feng, “Auto-rag: Autonomous retrieval-augmented generation for large language models,”CoRR, vol. abs/2411.19443, 2024. [311] G. Dong, H. Mao, K. Ma, L. Bao, Y. Chen, Z. Wang, Z. Chen, J. Du, H. Wang, F. Zhang, G. Zhou, Y. Zhu, J. Wen, and Z. Dou, “Agentic reinforced policy optimization,”CoRR, vol. abs/2507.19849, 2025. [312] Z. Wei, W. Yao, Y. Liu, W. Zhang, Q. Lu, L. Qiu, C. Yu, P . Xu, C. Zhang, B. Yin, H. Yun, and L. Li, “Webagentr1: Training web agents via end-to-end multi-turn reinforcement learning,”CoRR, vol. abs/2505.16421, 2025. [313] Y. Zheng, D. Fu, X. Hu, X. Cai, L. Ye, P . Lu, and P .

**中文**

Feng，“Auto-rag：大语言模型的自主检索增强生成”，CoRR，卷。 Abs/2411.19443, 2024. [311] G. Dong, H. Mao, K. Ma, L. Bao, Y. Chen, Z. Wang, Z. Chen, J. Du, H. Wang, F. Zhu, G. Zhou, Y. Zhu, J. Wen, and Z. Dou, “代理强化策略优化”，CoRR，卷。 abs/2507.19849, 2025. [312] 魏志伟，姚文伟，刘勇，张伟，鲁庆，邱立，于成，P. Xu，C.Zhang，B.Yin，H.Yun，L.Li，“Webagentr1：通过端到端多轮强化学习训练网络代理”，CoRR，卷。 abs/2505.16421, 2025. [313] 郑勇，付东，胡晓，蔡晓，叶丽，P.卢，P。

### 段落 431 · Page 41

**EN**

Liu, “Deepresearcher: Scaling deep research via reinforcement learning in real-world environments,” CoRR, vol. abs/2504.03160, 2025. [314] X. Li, J. Jin, G. Dong, H. Qian, Y. Zhu, Y. Wu, J. Wen, and Z. Dou, “Webthinker: Empowering large reasoning models with deep research capability,”CoRR, vol. abs/2504.21776, 2025. [315] J. Wu, B. Li, R. Fang, W. Yin, L. Zhang, Z. Tao, D. Zhang, Z. Xi, Y. Jiang, P . Xie, F. Huang, and J. Zhou, “Webdancer: Towards autonomous information seeking agency,”CoRR, vol. abs/2505.22648, 2025. [316] K. Li, Z. Zhang, H. Yin, L. Zhang, L. Ou, J. Wu, W. Yin, B. Li, Z. Tao, X. Wang, W. Shen, J. Zhang, D. Zhang, X. Wu, Y.

**中文**

Liu，“Deepresearcher：通过现实环境中的强化学习扩展深度研究”，CoRR，卷。 Abs/2504.03160, 2025. [314] X. Li, J. Jin, G. Dong, H. Qiu, Y. Zhu, Y. Wu, J. Wen, and Z. Dou, “Webthinker: 赋能具有深度研究能力的大型推理模型”，CoRR，卷。 abs/2504.21776, 2025. [315] 吴杰，李斌，方瑞，尹伟，张丽，陶子，张东，奚志，江玉，P.谢、F. Huang、J. Zhou，“Webdancer：迈向自主信息搜索机构”，CoRR，第 1 卷。 abs/2505.22648, 2025. [316] 李克，张正，殷宏，张丽，欧丽，吴建，尹伟，李本，陶子，王晓，沉伟，张建，张东，吴晓，Y.

### 段落 432 · Page 41

**EN**

Jiang, M. Yan, P . Xie, F. Huang, and J. Zhou, “Websailor: Navigating super-human reasoning for web agent,”CoRR, vol. abs/2507.02592, 2025. [317] Z. Tao, J. Wu, W. Yin, J. Zhang, B. Li, H. Shen, K. Li, L. Zhang, X. Wang, Y. Jiang, P . Xie, F. Huang, and J. Zhou, “Webshaper: Agentically data synthesizing via information-seeking formalization,”CoRR, vol. abs/2507.15061, 2025. [318] X. Geng, P . Xia, Z. Zhang, X. Wang, Q. Wang, R. Ding, C. Wang, J. Wu, Y. Zhao, K. Liet al., “Webwatcher: Breaking new frontiers of vision-language deep research agent,”arXiv preprint arXiv:2508.05748, 2025. [319] M. Joshi, E. Choi, D. S. Weld, and L.

**中文**

姜明. 严鹏.谢、F. Huang、J. Zhou，“Websailor：为网络代理导航超人类推理”，CoRR，第 1 卷。 Abs/2507.02592, 2025. [317] 陶子，吴建，尹伟，张建，李本，沉华，李凯，张丽，王晓，姜玉，P.谢、F. Huang、J. Zhou，“Webshaper：通过信息寻求形式化进行代理数据合成”，CoRR，卷。 abs/2507.15061, 2025. [318] X. Geng, P . Xia、Z.Zhang、X.Wang、Q.Wang、R.Ding、C.Wang、J.Wu、Y.Zhao、K.Liet 等人，“Webwatcher：突破视觉语言深度研究代理的新领域”，arXiv 预印本 arXiv:2508.05748，2025。 [319] M. Joshi、E. Choi、D. S. Weld 和 L.

### 段落 433 · Page 41

**EN**

Zettlemoyer, “Triviaqa: A large scale distantly supervised challenge dataset for reading comprehension,” inProceedings of the 55th Annual Meeting of the Association for Computational Linguistics, ACL 2017, Vancouver, Canada, July 30 - August 4, Volume 1: Long Papers, R. Barzilay and M. Kan, Eds. Association for Computational Linguistics, 2017, pp. 1601–1611. [320] J. Wei, N. Karina, H. W. Chung, Y. J. Jiao, S. Papay, A. Glaese, J. Schulman, and W. Fedus, “Measuring short-form factuality in large language models,” CoRR, vol. abs/2411.04368, 2024. [321] A. Mallen, A. Asai, V . Zhong, R. Das, D. Khashabi, and H.

**中文**

Zettlemoyer，“Triviaqa：用于阅读理解的大规模远程监督挑战数据集”，载于计算语言学协会第 55 届年会记录，ACL 2017，加拿大温哥华，7 月 30 日至 8 月 4 日，第 1 卷：长论文，R. Barzilay 和 M. Kan，编辑。计算语言学协会，2017 年，第 1601–1611 页。 [320] J. Wei、N. Karina、H. W. Chung、Y. J. Jiao、S. Papay、A. Glaese、J. Schulman 和 W. Fedus，“测量大型语言模型中的简短事实性”，CoRR，卷。绝对/2411.04368，2024。[321] A. Mallen，A. Asai，V。钟、R. Das、D. Khashabi 和 H.

### 段落 434 · Page 41

**EN**

Hajishirzi, “When not to trust language models: Investigating effectiveness of parametric and nonparametric memories,” inProceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), ACL 2023, Toronto, Canada, July 9-14, 2023, A. Rogers, J. L. Boyd-Graber, and N. Okazaki, Eds. Association for Computational Linguistics, 2023, pp. 9802–9822. [322] Z. Yang, P . Qi, S. Zhang, Y. Bengio, W. W. Cohen, R. Salakhutdinov, and C. D.

**中文**

Hajishirzi，“何时不信任语言模型：调查参数和非参数记忆的有效性”，载于计算语言学协会第 61 届年会记录（第一卷：长论文），ACL 2023，加拿大多伦多，2023 年 7 月 9-14 日，A. Rogers、J. L. Boyd-Graber 和 N. Okazaki，编辑。计算语言学协会，2023 年，第 9802–9822 页。 [322] Z.杨，P。 Qi、S. 张、Y. Bengio、W. W. Cohen、R. Salakhutdinov 和 C. D.

### 段落 435 · Page 41

**EN**

Manning, “Hotpotqa: A dataset for diverse, explainable multi-hop question answering,” inProceedings of the 2018 Conference on Empirical Methods in Natural Language Processing, Brussels, Belgium, October 31 - November 4, 2018, E. Riloff, D. Chiang, J. Hockenmaier, and J. Tsujii, Eds. Association for Computational Linguistics, 2018, pp. 2369– 2380. [323] X. Ho, A. D. Nguyen, S. Sugawara, and A. Aizawa, “Constructing A multi-hop QA dataset for comprehensive evaluation of reasoning steps,” inProceedings of the 28th International Conference on Computational Linguistics, COLING 2020, Barcelona, Spain (Online), December 8-13, 2020, D. Scott, N.

**中文**

Manning，“Hotpotqa：用于多样化、可解释的多跳问答的数据集”，载于 2018 年自然语言处理经验方法会议论文集，比利时布鲁塞尔，2018 年 10 月 31 日至 11 月 4 日，E. Riloff、D. Jiang、J. Hockenmaier 和 J. Tsujii，编辑。计算语言学协会，2018，第 2369–2380 页。 [323] X. Ho、A. D. Nguyen、S. Sukawara 和 A. Aizawa，“构建用于综合评估推理步骤的多跳 QA 数据集”，第 28 届国际计算语言学会议论文集，COLING 2020，西班牙巴塞罗那（在线），2020 年 12 月 8-13 日，D. Scott, N.

### 段落 436 · Page 41

**EN**

Bel, and C. Zong, Eds. International Committee on Computational Linguistics, 2020, pp. 6609–6625. [324] L. Phan, A. Gatti, Z. Han, N. Li, J. Hu, H. Zhang, S. Shi, M. Choi, A. Agrawal, A. Chopra, A. Khoja, R. Kim, J. Hausenloy, O. Zhang, M. Mazeika, D. Anderson, T. Nguyen, M. Mahmood, F. Feng, S. Y. Feng, H. Zhao, M. Yu, V . Gangal, C. Zou, Z. Wang, J. P . Wang, P . Kumar, O. Pokutnyi, R. Gerbicz, S. Popov, J. Levin, M. Kazakov, J. Schmitt, G. Galgon, A. Sanchez, Y. Lee, W. Yeadon, S. Sauers, M. Roth, C. Agu, S. Riis, F. Giska, S. Utpala, Z. Giboney, G. M. Goshu, J. of Arc Xavier, S. Crowson, M. M. Naiya, N. Burns, L. Finke, Z. Cheng, H.

**中文**

Bel 和 C. Zong，编辑。国际计算语言学委员会，2020 年，第 6609-6625 页。 [324] L.Phan、A.Gatti、Z.Han、N.Li、J.Hu、H.Zhang、S.Shi、M.Choi、A.Agrawal、A.Chopra、A.Khoja、R.Kim、J.Hausenloy、O.Zhang、M.Mazeika、D.Anderson、T.Nguyen、M.Mahmood、F.Feng、S.Y.Feng、H.Zhao、M.Yu、V。 Gangal, C. 邹, Z. 王, J. P.王P. Kumar、O. Pokutnyi、R. Gerbicz、S. Popov、J. Levin、M. Kazakov、J. Schmitt、G. Galgon、A. Sanchez、Y. Lee、W. Yeadon、S. Sauers、M. Roth、C. Agu、S. Riis、F. Giska、S. Utpala、Z. Giboney、G. M. Goshu、Arc Xavier 的 J.， S. Crowson、M. M. Naiya、N. Burns、L. Finke、Z. Cheng、H.

### 段落 437 · Page 41

**EN**

Park, F. Fournier- Facio, J. Wydallis, M. Nandor, A. Singh, T. Gehrunger, J. Cai, B. McCarty, D. Duclosel, J. Nam, J. Zampese, R. G. Hoerr, A. Bacho, G. A. Loume, A. Galal, H. Cao, A. C. Garretson, D. Sileo, Q. Ren, D. Cojoc, P . Arkhipov, U. Qazi, L. Li, S. Motwani, C. S. de Witt, E. Taylor, J. Veith, E. Singer, T. D. Hartman, P . Rissone, J. Jin, J. W. L. Shi, C. G. Willcocks, J. Robinson, A. Mikov, A. Prabhu, L. Tang, X. Alapont, J. L. Uro, K. Zhou, E. de Oliveira Santos, A. P . Maksimov, E. Vendrow, K. Zenitani, J. Guillod, Y. Li, J. Vendrow,

**中文**

Park、F. Fournier-Facio、J. Wydallis、M. Nandor、A. Singh、T. Gehrunger、J. Cai、B. McCarty、D. Duclosel、J. Nam、J. Zampese、R. G. Hoerr、A. Bacho、G. A. Loume、A. Galal、H. Cao、A. C. Garretson、D. Sileo、Q. Ren、D. Cojoc、 P。阿尔希波夫、U. Qazi、L. Li、S. Motwani、C. S. de Witt、E. Taylor、J. Veith、E. Singer、T. D. Hartman、P。 Rissone、J. Jin、J. W. L. Shi、C. G. Willcocks、J. Robinson、A. Mikov、A. Prabhu、L. Tang、X. Alapont、J. L. Uro、K. Zhou、E. de Oliveira Santos、A. P。马克西莫夫、E. Vendrow、K. Zenitani、J. Guillod、Y. Li、J. Vendrow、

### Page 42

### 段落 438 · Page 42

**EN**

42 V . Kuchkin, and N. Ze-An, “Humanity’s last exam,” CoRR, vol. abs/2501.14249, 2025. [325] J. Wei, Z. Sun, S. Papay, S. McKinney, J. Han, I. Fulford, H. W. Chung, A. T. Passos, W. Fedus, and A. Glaese, “Browsecomp: A simple yet challenging benchmark for browsing agents,”CoRR, vol. abs/2504.12516, 2025. [326] G. Mialon, C. Fourrier, T. Wolf, Y. LeCun, and T. Scialom, “GAIA: a benchmark for general AI assistants,” inThe Twelfth International Conference on Learning Representations, ICLR 2024, Vienna, Austria, May 7- 11, 2024. OpenReview.net, 2024. [327] O. Yoran, S. J. Amouyal, C. Malaviya, B. Bogin, O. Press, and J.

**中文**

42V。 Kuchkin 和 N. Ze-An，“人类的最后一次考试”，CoRR，卷。 abs/2501.14249，2025。[325] J. Wei、Z. Sun、S. Papay、S. McKinney、J. Han、I. Fulford、H. W. Chung、A. T. Passos、W. Fedus 和 A. Glaese，“Browsecomp：浏览代理的简单但具有挑战性的基准”，CoRR，卷。 abs/2504.12516，2025。[326] G. Mialon、C. Fourrier、T. Wolf、Y. LeCun 和 T. Scialom，“GAIA：通用人工智能助理的基准”，第十二届国际学习表征会议，ICLR 2024，奥地利维也纳，2024 年 5 月 7-11 日。OpenReview.net，2024 年。 [327] O. Yoran、S. J. Amouyal、C. Malaviya、B. Bogin、O. Press 和 J.

### 段落 439 · Page 42

**EN**

Berant, “Assistantbench: Can web agents solve realistic and time-consuming tasks?” in Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, EMNLP 2024, Miami, FL, USA, November 12-16, 2024, Y. Al-Onaizan, M. Bansal, and Y. Chen, Eds. Association for Computational Linguistics, 2024, pp. 8938–8968. [328] A. Fourney, G. Bansal, H. Mozannar, C. Tan, E. Salinas, E. Zhu, F. Niedtner, G. Proebsting, G. Bassman, J. Gerrits, J. Alber, P . Chang, R. Loynd, R. West, V . Dibia, A. Awadallah, E. Kamar, R. Hosn, and S. Amershi, “Magentic-one: A generalist multi-agent system for solving complex tasks,”CoRR, vol.

**中文**

Berant，“Assistantbench：网络代理能否解决现实且耗时的任务？” 2024 年自然语言处理经验方法会议论文集，EMNLP 2024，美国佛罗里达州迈阿密，2024 年 11 月 12-16 日，Y. Al-Onaizan、M. Bansal 和 Y. Chen，编辑。计算语言学协会，2024 年，第 8938–8968 页。 [328] A. Fourney、G. Bansal、H. Mozannar、C. Tan、E. Salinas、E. Zhu、F. Niedtner、G. Proebsting、G. Bassman、J. Gerrits、J. Alber、P。张，R.洛因德，R.韦斯特，V。 Dibia、A. Awadallah、E. Kamar、R. Hosn 和 S. Amershi，“Magentic-one：用于解决复杂任务的通用多智能体系统”，CoRR，卷。

### 段落 440 · Page 42

**EN**

abs/2411.04468, 2024. [329] C. E. Jimenez, J. Yang, A. Wettig, S. Yao, K. Pei, O. Press, and K. Narasimhan, “Swe-bench: Can language models resolve real-world github issues?” CoRR, vol. abs/2310.06770, 2023. [330] N. Muennighoff, Q. Liu, A. R. Zebaze, Q. Zheng, B. Hui, T. Y. Zhuo, S. Singh, X. Tang, L. von Werra, and S. Longpre, “Octopack: Instruction tuning code large language models,” inThe Twelfth International Conference on Learning Representations, ICLR 2024, Vienna, Austria, May 7-11, 2024. OpenReview.net, 2024. [331] J. S. Chan, N. Chowdhury, O. Jaffe, J. Aung, D. Sherburn, E. Mays, G. Starace, K. Liu, L. Maksin, T. Patwardhan, A.

**中文**

abs/2411.04468, 2024. [329] C. E. Jimenez、J. Yang、A. Wettig、S. Yao、K. Pei、O. Press 和 K. Narasimhan，“Swe-bench：语言模型能否解决现实世界的 github 问题？” CoRR，卷。 abs/2310.06770, 2023. [330] N. Muennighoff、Q. Liu、A. R. Zebaze、Q. Cheng、B. Hui、T. Y. Zhuo、S. Singh、X. Tang、L. von Werra 和 S. Longpre，“Octopack：指令调优代码大语言模型”，载于第十二届学习表示国际会议，ICLR 2024 年，奥地利维也纳，2024 年 5 月 7-11 日。OpenReview.net，2024。[331] J. S. Chan、N. Chowdhury、O. Jaffe、J. Aung、D. Sherburn、E. Mays、G. Starace、K. Liu、L. Maksin、T. Patwardhan、A.

### 段落 441 · Page 42

**EN**

Madry, and L. Weng, “Mle-bench: Evaluating machine learning agents on machine learning engineering,” inThe Thirteenth International Conference on Learning Representations, ICLR 2025, Singapore, April 24-28, 2025. OpenReview.net, 2025. [332] Q. Huang, J. Vora, P . Liang, and J. Leskovec, “Mlagentbench: Evaluating language agents on machine learning experimentation,” inForty-first International Conference on Machine Learning, ICML 2024, Vienna, Austria, July 21-27, 2024. OpenReview.net, 2024. [333] H. Wijk, T. Lin, J. Becker, S. Jawhar, N. Parikh, T. Broadley, L. Chan, M. Chen, J. Clymer, J. Dhyani, E. Ericheva, K. Garcia, B. Goodrich, N.

**中文**

Madry 和 L. Weng，“Mle-bench：评估机器学习工程中的机器学习代理”，第十三届学习表示国际会议，ICLR 2025，新加坡，2025 年 4 月 24-28 日。OpenReview.net，2025 年。[332] Q. Huang、J. Vora、P . Liang 和 J. Leskovec，“Mlagentbench：评估机器学习实验中的语言代理”，第 41 届机器学习国际会议，ICML 2024，奥地利维也纳，2024 年 7 月 21-27 日。OpenReview.net，2024。[333] H. Wijk、T. Lin、J. Becker、S. Jawhar、N. Parikh、T. Broadley、L. Chan、M. Chen、J. Clymer、J. Dhyani、E. Ericheva、K. Garcia、B. Goodrich、N.

### 段落 442 · Page 42

**EN**

Jurkovic, M. Kinniment, A. Lajko, S. Nix, L. Sato, W. Saunders, M. Taran, B. West, and E. Barnes, “Re-bench: Evaluating frontier AI r&d capabilities of language model agents against human experts,”CoRR, vol. abs/2411.15114, 2024. [334] H. Yu, Z. Hong, Z. Cheng, K. Zhu, K. Xuan, J. Yao, T. Feng, and J. You, “Researchtown: Simulator of human research community,”CoRR, vol. abs/2412.17767, 2024. [335] S. Zhou, F. F. Xu, H. Zhu, X. Zhou, R. Lo, A. Sridhar, X. Cheng, T. Ou, Y. Bisk, D. Fried, U. Alon, and G.

**中文**

Jurkovic、M. Kinniment、A. Lajko、S. Nix、L. Sato、W. Saunders、M. Taran、B. West 和 E. Barnes，“重新评估：针对人类专家评估语言模型代理的前沿人工智能研发能力”，CoRR，卷。 Abs/2411.15114, 2024. [334] 余浩、洪正、程正、朱坤、轩、姚建、冯涛、尤建，“Researchtown：人类研究共同体的模拟器”，CoRR，卷。 abs/2412.17767, 2024. [335] S. Zhou、F. F. Xu、H. Zhu、X. Zhou、R. Lo、A. Sridhar、X. Cheng、T. Ou、Y. Bisk、D. Fried、U. Alon 和 G.

### 段落 443 · Page 42

**EN**

Neubig, “Webarena: A realistic web environment for building autonomous agents,” inThe Twelfth International Conference on Learning Representations, ICLR 2024, Vienna, Austria, May 7-11, 2024. OpenReview.net, 2024. [336] J. Chen, D. Yuen, B. Xie, Y. Yang, G. Chen, Z. Wu, L. Yixing, X. Zhou, W. Liu, S. Wang, K. Zhou, R. Shao, L. Nie, Y. Wang, J. Hao, J. Wang, and K. Shao, “Spabench: a comprehensive benchmark for smartphone agent evaluation,” inThe Thirteenth International Conference on Learning Representations, ICLR 2025, Singapore, April 24-28, 2025. OpenReview.net, 2025. [337] J. Wu, W. Yin, Y. Jiang, Z. Wang, Z. Xi, R. Fang, L. Zhang, Y.

**中文**

Neubig，“Webarena：构建自主代理的现实网络环境”，第十二届学习表征国际会议，ICLR 2024，奥地利维也纳，2024 年 5 月 7-11 日。OpenReview.net，2024。 [336] J. Chen, D. Yuen, B. Xie, Y. Yang, G. Chen, Z. Wu, L. Yixing, X. Zhou, W. Liu, S. Wang, K. Zhou, R. Shao, L. Nie, Y. Wang, J.hao, J. Wang, and K. Shao，“Spabench：智能手机代理评估的综合基准”，第十三届学习表征国际会议，ICLR 2025，新加坡，2025 年 4 月 24-28 日。OpenReview.net，2025 年。[337] J. Wu、W. Yin、Y. Jiang、Z. Wang，奚志、方荣、张丽、Y.

### 段落 444 · Page 42

**EN**

He, D. Zhou, P . Xie, and F. Huang, “Webwalker: Benchmarking llms in web traversal,” in Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), ACL 2025, Vienna, Austria, July 27 - August 1, 2025, W. Che, J. Nabende, E. Shutova, and M. T. Pilehvar, Eds. Association for Computational Linguistics, 2025, pp. 10 290–10 305. [338] S. MacAvaney, C. Macdonald, R. Murray-Smith, and I. Ounis, “Intent5: Search result diversification using causal language models,”CoRR, vol. abs/2108.04026, 2021. [339] OpenAI, “GPT-4 technical report,”CoRR, vol. abs/2303.08774, 2023. [340] N.

**中文**

何德.周P. Xie 和 F. Huang，“Webwalker：网络遍历中的 llms 基准测试”，计算语言学协会第 63 届年会论文集（第一卷：长论文），ACL 2025，奥地利维也纳，2025 年 7 月 27 日至 8 月 1 日，W. Che、J. Nabende、E. Shutova 和 M. T.皮莱瓦尔，编辑。计算语言学协会，2025 年，第 10 290–10 305 页。 [338] S. MacAvaney、C. Macdonald、R. Murray-Smith 和 I. Ounis，“Intent5：使用因果语言模型的搜索结果多样化”，CoRR，卷。 abs/2108.04026, 2021。 [339] OpenAI，“GPT-4 技术报告”，CoRR，卷。绝对/2303.08774，2023。[340]N。

### 段落 445 · Page 42

**EN**

Craswell, “Mean reciprocal rank,” inEncyclopedia of Database Systems, L. Liu and M. T. ¨Ozsu, Eds. Springer US, 2009, p. 1703. [341] K. J ¨arvelin and J. Kek ¨al¨ainen, “Cumulated gain-based evaluation of IR techniques,”ACM Trans. Inf. Syst., vol. 20, no. 4, pp. 422–446, 2002. [342] K. Papineni, S. Roukos, T. Ward, and W. Zhu, “Bleu: a method for automatic evaluation of machine translation,” inProceedings of the 40th Annual Meeting of the Association for Computational Linguistics, July 6-12, 2002, Philadelphia, P A, USA. ACL, 2002, pp. 311–318. [343] C.-Y.

**中文**

Craswell，“平均倒数排名”，《数据库系统百科全书》，L. Liu 和 M. T. ¡Ozsu，编辑。施普林格美国，2009 年，第 14 页。 1703. [341] K. J ¡信息。系统，卷。 20、没有。 4，第 422–446 页，2002 年。 [342] K. Papineni、S. Roukos、T. Ward 和 W. Zhu，“Bleu：一种自动评估机器翻译的方法”，载于计算语言学协会第 40 届年会记录，2002 年 7 月 6-12 日，美国宾夕法尼亚州费城。 ACL，2002 年，第 311-318 页。 [343] C.-Y。

### 段落 446 · Page 42

**EN**

Lin, “ROUGE: A package for automatic evaluation of summaries,” inText Summarization Branches Out. Barcelona, Spain: Association for Computational Linguistics, Jul. 2004, pp. 74–81. [344] P . Manakul, A. Liusie, and M. J. F. Gales, “Selfcheckgpt: Zero-resource black-box hallucination detection for generative large language models,” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 9004–9017. [345] H. Qian, Y. Zhu, Z. Dou, H. Gu, X. Zhang, Z. Liu, R. Lai, Z. Cao, J.

**中文**

Lin，“ROUGE：自动评估摘要的包”，inText Summarization Branches Out。西班牙巴塞罗那：计算语言学协会，2004 年 7 月，第 74-81 页。 [344] P. Manakul、A. Liusie 和 M. J. F. Gales，“Selfcheckgpt：生成大语言模型的零资源黑盒幻觉检测”，《2023 年自然语言处理经验方法会议论文集》，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 9004–9017 页。 [345] 钱宏、朱勇、窦志、顾宏、张旭、刘志、赖荣、曹志、J.

### 段落 447 · Page 42

**EN**

Nie, and J. Wen, “Webbrain: Learning to generate factually correct articles for queries by grounding on large web corpus,”CoRR, vol. abs/2304.04358, 2023. [346] J. Li, X. Cheng, X. Zhao, J. Nie, and J. Wen, “Halueval: A large-scale hallucination evaluation benchmark for large language models,” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Pro-

**中文**

Nie 和 J. Wen，“Webbrain：学习通过基于大型网络语料库生成事实正确的查询文章”，CoRR，卷。 abs/2304.04358, 2023. [346] J. Li, X. Cheng, X. Zhao, J. Nie, and J. Wen，“Halueval：大型语言模型的大规模幻觉评估基准”，载于 2023 年自然语言专业经验方法会议论文集

### Page 43

### 段落 448 · Page 43

**EN**

43 cessing, EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 6449–6464. [347] L. Chen, Y. Deng, Y. Bian, Z. Qin, B. Wu, T. Chua, and K. Wong, “Beyond factuality: A comprehensive evaluation of large language models as knowledge generators,” inProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, EMNLP 2023, Singapore, December 6-10, 2023, H. Bouamor, J. Pino, and K. Bali, Eds. Association for Computational Linguistics, 2023, pp. 6325–6341. [348] S. Xu, D. Hou, L. Pang, J. Deng, J. Xu, H. Shen, and X.

**中文**

43 cessing，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor、J. Pino 和 K. Bali，编辑。计算语言学协会，2023 年，第 6449–6464 页。 [347] L. Chen、Y. Deng、Y. Bian、Z.qin、B. Wu、T. Chua 和 K. Wong，“超越事实：对大型语言模型作为知识生成器的综合评估”，载于 2023 年自然语言处理经验方法会议论文集，EMNLP 2023，新加坡，2023 年 12 月 6-10 日，H. Bouamor, J.皮诺和 K. Bali，编辑。计算语言学协会，2023 年，第 6325–6341 页。 [348] S. Xu，D. Hou，L. Pang，J. Deng，J. Xu，H. Shen，和 X.

### 段落 449 · Page 43

**EN**

Cheng, “Ai-generated images introduce invisible relevance bias to text-image retrieval,”CoRR, vol. abs/2311.14084, 2023. [349] S. Dai, Y. Zhou, L. Pang, W. Liu, X. Hu, Y. Liu, X. Zhang, and J. Xu, “Llms may dominate information access: Neural retrievers are biased towards llmgenerated texts,”CoRR, vol. abs/2310.20501, 2023. [350] J. S. Park, J. C. O’Brien, C. J. Cai, M. R. Morris, P . Liang, and M. S. Bernstein, “Generative agents: Interactive simulacra of human behavior,” inProceedings of the 36th Annual ACM Symposium on User Interface Software and Technology, UIST 2023, San Francisco, CA, USA, 29 October 2023- 1 November 2023, S.

**中文**

Cheng，“人工智能生成的图像给文本图像检索带来了隐形的相关性偏差”，CoRR，卷。 abs/2311.14084, 2023. [349] S. Dai, Y. Zhou, L. Pang, W. Liu, X. Hu, Y. Liu, X. Zhang, and J. Xu, “LLMS 可能主导信息访问：神经检索器偏向于 Llm 生成的文本”，CoRR，卷。 abs/2310.20501, 2023。 [350] J. S. Park, J. C. O’Brien, C. J. Cai, M. R. Morris, P .梁和 M. S. Bernstein，“生成代理：人类行为的交互式拟像”，载于第 36 届 ACM 用户界面软件和技术年度研讨会论文集，UIST 2023，美国加利福尼亚州旧金山，2023 年 10 月 29 日至 2023 年 11 月 1 日，S.

### 段落 450 · Page 43

**EN**

Follmer, J. Han, J. Steimle, and N. H. Riche, Eds. ACM, 2023, pp. 2:1–2:22.

**中文**

Follmer、J. Han、J. Steimle 和 N. H. Riche，编辑。 ACM，2023 年，第 2:1–2:22。
