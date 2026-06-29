# A Survey on RAG Meeting LLMs

- ID: 80
- 类型: pdf
- 分类: 04_academic_papers
- 主题: retrieval-augmented large language models survey
- 原文链接: https://arxiv.org/pdf/2405.06211
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Wenqi Fan wenqifan03@gmail.com The Hong Kong Polytechnic University, HK SAR Yujuan Ding∗ dingyujuan385@gmail.com The Hong Kong Polytechnic University, HK SAR Liangbo Ning BigLemon1123@gmail.com The Hong Kong Polytechnic University, HK SAR Shijie Wang shijie.wang@connect.polyu.hk The Hong Kong Polytechnic University, HK SAR Hengyun Li neilhengyun.li@polyu.edu.hk The Hong Kong Polytechnic University, HK SAR Dawei Yin yindawei@acm.org Baidu Inc, China Tat-Seng Chua dcscts@nus.edu.sg National University of Singapore, Singapore Qing Li csqli@comp.polyu.edu.hk The Hong

**中文**

RAG 会议法学硕士调查：迈向检索增强大语言模型 范文琪 wenqifan03@gmail.com 香港理工大学，香港特别行政区 丁玉娟* dingyujuan385@gmail.com 香港理工大学，香港特别行政区 宁良波 BigLemon1123@gmail.com 香港理工大学，香港特别行政区 王世杰shijie.wang@connect.polyu.hk 香港理工大学，香港特别行政区 Hengyun Li neilhengyun.li@polyu.edu.hk 香港理工大学，香港特别行政区 Dawei Yin yindawei@acm.org 百度公司，中国 Tat-Seng Chua dcscts@nus.edu.sg 新加坡国立大学，新加坡 Qing Li csqli@comp.polyu.edu.hk 香港

### 段落 2 · Page 1

**EN**

Kong Polytechnic University, HK SAR ABSTRACT As one of the most advanced techniques in AI, Retrieval-Augmented Generation (RAG) can offer reliable and up-to-date external knowledge, providing huge convenience for numerous tasks.

**中文**

香港理工大学 摘要 作为人工智能领域最先进的技术之一，检索增强生成（RAG）可以提供可靠且最新的外部知识，为众多任务提供巨大便利。

### 段落 3 · Page 1

**EN**

Particularly in the era of AI-Generated Content (AIGC), the powerful capacity of retrieval in providing additional knowledge enables RAG to assist existing generative AI in producing high-quality outputs. Recently, Large Language Models (LLMs) have demonstrated revolutionary abilities in language understanding and generation, while still facing inherent limitations, such as hallucinations and out-ofdate internal knowledge.

**中文**

特别是在人工智能生成内容（AIGC）时代，强大的检索能力提供额外的知识，使RAG能够协助现有的生成式人工智能产生高质量的输出。最近，大型语言模型（LLM）在语言理解和生成方面表现出了革命性的能力，但仍然面临着固有的局限性，例如幻觉和过时的内部知识。

### 段落 4 · Page 1

**EN**

Given the powerful abilities of RAG in providing the latest and helpful auxiliary information, Retrieval- Augmented Large Language Models (RA-LLMs) have emerged to harness external and authoritative knowledge bases, rather than solely relying on the model’s internal knowledge, to augment the generation quality of LLMs. In this survey, we comprehensively review existing research studies in RA-LLMs, covering three primary technical perspectives: architectures, training strategies, and applications. As the preliminary knowledge, we briefly introduce the foundations and recent advances of LLMs.

**中文**

鉴于RAG在提供最新且有用的辅助信息方面的强大能力，检索增强型大语言模型（RA-LLM）应运而生，利用外部权威知识库，而不是仅仅依赖模型的内部知识，来提高LLM的生成质量。在本次调查中，我们全面回顾了 RA-LLM 的现有研究，涵盖三个主要技术视角：架构、培训策略和应用。作为预备知识，我们简要介绍了LLM的基础和最新进展。

### 段落 5 · Page 1

**EN**

Then, to illustrate the practical significance of RAG for LLMs, we systematically review mainstream relevant work by their architectures, training strategies, and application areas, detailing specifically the challenges of each and the corresponding capabilities of RA-LLMs. Finally, to deliver deeper insights, we discuss current limitations and several promising directions for future research. Updated information about this survey can be found at https:// advanced-recommendersystems.github.io/ RAG-Meets-LLMs/1. KEYWORDS Retrieval-Augmented Generation (RAG), Large Language Model (LLM), Pre-training, Fine-tuning, In-context Learning, Prompting.

**中文**

然后，为了说明RAG对LLM的实际意义，我们从架构、培训策略和应用领域系统地回顾了主流相关工作，具体详细说明了每个RA-LLM面临的挑战以及相应的能力。最后，为了提供更深入的见解，我们讨论了当前的局限性和未来研究的几个有希望的方向。有关本次调查的更新信息请访问 https://advanced-recommendersystems.github.io/RAG-Meets-LLMs/1。关键词 检索增强生成（RAG）、大语言模型（LLM）、预训练、微调、上下文学习、提示。

### 段落 6 · Page 1

**EN**

∗Corresponding author: Yujuan Ding 1This is the long version of the survey to appear at KDD 2024 [33] 1 INTRODUCTION As one of the most fundamental data mining techniques, retrieval aims to understand the input query and extract relevant information from external data sources [ 24, 30, 67, 140]. It has found extensive application in various fields [ 8, 28, 106, 179], such as search, question answering, and recommender systems.

**中文**

*通讯作者：Yujuan Ding 1这是 KDD 2024 上发表的调查的长版本 [33] 1 简介 作为最基本的数据挖掘技术之一，检索旨在理解输入查询并从外部数据源中提取相关信息 [24,30,67,140]。它在各个领域都有广泛的应用[8,28,106,179]，例如搜索、问答和推荐系统。

### 段落 7 · Page 1

**EN**

For instance, search engines (e.g., Google, Bing, and Baidu) are the most successful applications of retrieval in the industry; they can filter and retrieve the most relevant web pages or documents that can match a user’s query [19, 179], enabling users to find the desired information effectively. Meanwhile, retrieval models, through effective data maintenance in external databases, can provide faithful and timely external knowledge, thereby serving vital functions in various knowledge-intensive tasks.

**中文**

例如，搜索引擎（例如 Google、Bing 和百度）是业界最成功的检索应用；他们可以过滤和检索与用户的查询相匹配的最相关的网页或文档[19, 179]，使用户能够有效地找到所需的信息。同时，检索模型通过对外部数据库的有效数据维护，可以提供忠实、及时的外部知识，从而在各种知识密集型任务中发挥重要作用。

### 段落 8 · Page 1

**EN**

Due to their powerful capacities, retrieval techniques have been successfully incorporated into advanced generative models in the era of AI-Generated Content (AIGC) [77, 132, 163]. Notably, the integration of retrieval models with language models has given rise to Retrieval-Augmented Generation (RAG) [ 74], which has emerged as one of the most representative techniques in the field of generative AI, aiming to enhance the quality of the generated text content with retrieved information [6, 74, 77].

**中文**

由于其强大的能力，检索技术已成功融入人工智能生成内容（AIGC）时代的先进生成模型中[77,132,163]。值得注意的是，检索模型与语言模型的集成催生了检索增强生成（RAG）[74]，它已成为生成人工智能领域最具代表性的技术之一，旨在提高利用检索信息生成的文本内容的质量[6,74,77]。

### 段落 9 · Page 1

**EN**

To advance generation models and enhance the generated results, RAG incorporates information or knowledge from external data sources, which serves as supplementary for the input query or the generated output [62, 103]. Specifically, RAG first invokes the retriever to search and extract the relevant documents from external databases, which are then leveraged as the context to enhance the generation process [54]. In practice, RAG techniques are feasible and efficient to apply in various generation tasks with simple adaptation of the retrieval component, requiring minimal or even no additional training [117].

**中文**

为了改进生成模型并增强生成的结果，RAG 结合了来自外部数据源的信息或知识，作为输入查询或生成的输出的补充 [62, 103]。具体来说，RAG 首先调用检索器从外部数据库中搜索和提取相关文档，然后将其用作上下文来增强生成过程 [54]。在实践中，RAG 技术是可行且有效的，可以通过简单地调整检索组件来应用于各种生成任务，需要很少甚至不需要额外的训练[117]。

### 段落 10 · Page 1

**EN**

Recent studies have demonstrated the great potential of RAG not only for knowledge-intensive tasks such as the Open-domain Question Answering (OpenQA) [6, 46, 109, 133], but also for general language tasks [48, 62, 170], and various downstream applications [90, 163]. 1 arXiv:2405.06211v3 [cs.CL] 17 Jun 2024

**中文**

最近的研究表明，RAG 不仅适用于知识密集型任务，例如开放域问答（OpenQA）[6,46,109,133]，而且适用于一般语言任务[48,62,170]和各种下游应用程序[90,163]。 1 arXiv:2405.06211v3 [cs.CL] 2024 年 6 月 17 日

### Page 2

### 段落 11 · Page 2

**EN**

Conference’17, July 2017, Washington, DC, USA Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li Spain won the Women's World Cup 2023. Which country won the Women's World Cup 2023? User w/o RAG with RAG Pre-trained LLMs External Database Output Prompt Output Prompt Query Additional information: New, Domain-specific, etc. ContextAs of my last update in January 2022, I can't provide whichcountry won ... 2023. Figure 1: Retrieval-Augmented Generation (RAG) meets Large Language Models (LLMs).

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 范文琪、丁玉娟、宁良博、王士杰、李恒云、殷大伟、蔡达成、李庆 西班牙赢得了 2023 年女足世界杯。哪个国家赢得了 2023 年女足世界杯？没有 RAG 且带有 RAG 预训练 LLM 的用户 外部数据库输出提示 输出提示查询 其他信息：新信息、特定于领域的信息等。 上下文 截至 2022 年 1 月的最后一次更新，我无法提供哪个国家/地区赢得了 ... 2023 年。图 1：检索增强生成 (RAG) 满足大型语言模型 (LLM)。

### 段落 12 · Page 2

**EN**

When the user’s query is outof-scope, e.g., unseen content in training data or the need for the latest information for the answer, LLMs might show inferior generation performance. With the help of RAG, LLMs can leverage additional relevant information from external database to enhance their text generation capability. Recent years have witnessed the rapid development of pre-trained foundation models, particularly Large Language Models (LLMs), which have demonstrated impressive performance across various tasks [1, 18], including recommender systems [195], molecule discovery [77], and report generation [27].

**中文**

当用户的查询超出范围时，例如训练数据中未见的内容或需要最新信息作为答案，LLM 可能会表现出较差的生成性能。在 RAG 的帮助下，法学硕士可以利用外部数据库中的其他相关信息来增强其文本生成能力。近年来，预训练基础模型的快速发展，特别是大型语言模型 (LLM)，在各种任务中表现出了令人印象深刻的性能 [1, 18]，包括推荐系统 [195]、分子发现 [77] 和报告生成 [27]。

### 段落 13 · Page 2

**EN**

Technically, the great success of LLMs can be technically attributed to the advanced architectures with billion-level parameters pre-training on a huge amount of training corpus from various sources. These technical improvements have given rise to the remarkable emergence capabilities of LLMs [ 194, 195], particularly in language understanding and generation, in-context learning, and others. For instance, GPT-FAR introduces detailed prompts to teach GPT-4 to perform image tagging, statistical analysis, and text analysis for multi-modal fashion report generation [27].

**中文**

从技术上讲，法学硕士的巨大成功在技术上可以归因于在各种来源的海量训练语料上进行十亿级参数预训练的先进架构。这些技术进步带来了法学硕士的卓越能力[194, 195]，特别是在语言理解和生成、情境学习等方面。例如，GPT-FAR 引入了详细的提示来教 GPT-4 执行图像标记、统计分析和文本分析，以生成多模式时尚报告 [27]。

### 段落 14 · Page 2

**EN**

LLMs also achieve promising performance in recommender systems by understanding users’ preferences towards items [154, 195]. Despite the success, LLMs still suffer from intrinsic limitations [194, 195], such as the lack of domain-specific knowledge, the problem of “hallucination”, and the substantial computational resources required for updating the models. These problems are particularly notable in domain-specific fields like medicine and law.

**中文**

法学硕士还通过了解用户对项目的偏好，在推荐系统中取得了良好的表现[154, 195]。尽管取得了成功，法学硕士仍然面临着内在的局限性[194, 195]，例如缺乏特定领域的知识、“幻觉”问题以及更新模型所需的大量计算资源。这些问题在医学和法律等特定领域尤其引人注目。

### 段落 15 · Page 2

**EN**

For instance, a recent study has demonstrated that legal hallucinations are pervasive and disturbing, with hallucination rates ranging from 69% to 88% in responses to specific legal queries for state-of-the-art LLMs [21]. Moreover, the challenges of tackling the hallucination problem become even harder due to the substantial computational resources required for fine-tuning LLMs with domain-specific or the latest data. This, in turn, significantly hinders the widespread adoption of LLMs in various real-world applications.

**中文**

例如，最近的一项研究表明，法律幻觉普遍存在且令人不安，在回答针对最先进的法学硕士的具体法律查询时，幻觉率从 69% 到 88% 不等 [21]。此外，由于使用特定领域或最新数据微调法学硕士需要大量计算资源，因此解决幻觉问题的挑战变得更加困难。这反过来又极大地阻碍了法学硕士在各种实际应用中的广泛采用。

### 段落 16 · Page 2

**EN**

To address these limitations, recent efforts have been made to take advantage of RAG to enhance the capabilities of LLMs in various tasks [ 6, 53, 62, 135], especially those demanding high for the latest and reliable knowledge such as Question Answer (QA), AI4Science, and software engineering. For example, Lozano et al. [92] introduces a scientific QA system based on retrieving scientific literature dynamically. MolReGPT leverages RAG to enhance the in-context learning ability of ChatGPT for molecular discovery [77]. It is also been demonstrated that RAG can effectively reduce hallucinations in conversational tasks [137, 171].

**中文**

为了解决这些限制，最近人们努力利用 RAG 来增强法学硕士在各种任务中的能力 [6,53,62,135]，特别是那些对最新和可靠知识要求较高的任务，例如问答（QA）、AI4Science 和软件工程。例如，洛萨诺等人。 [92]介绍了一种基于动态检索科学文献的科学问答系统。 MolReGPT 利用 RAG 来增强 ChatGPT 的上下文学习能力，以进行分子发现 [77]。研究还证明，RAG 可以有效减少会话任务中的幻觉 [137, 171]。

### 段落 17 · Page 2

**EN**

As illustrated in Figure 1, an LLM-based dialog system will not be able to answer well for out-of-scope queries. With the help of RAG to retrieve relevant knowledge from external database and integrate it into the process of generation, the dialog system succeeds in giving correct answers. Given the remarkable progress in advancing LLMs with RAG, there is an imperative need for a systematic review of recent advances in Retrieval-Augmented Large Language Models (RA-LLMs).

**中文**

如图 1 所示，基于 LLM 的对话系统将无法很好地回答超出范围的查询。借助RAG从外部数据库检索相关知识并将其整合到生成过程中，对话系统成功给出了正确答案。鉴于 RAG 在推进法学硕士方面取得的显着进展，迫切需要对检索增强大型语言模型 (RA-LLM) 的最新进展进行系统回顾。

### 段落 18 · Page 2

**EN**

This survey aims to provide a comprehensive overview of RA- LLMs by summarizing representative methods from the aspects of the architecture, training strategy, and application area respectively. More specifically, following a brief introduction to the background knowledge of LLMs in Section 2, we review existing research from several primary perspectives of RA-LLMs in terms of retrieval, generation, and augmentation in Section 3, as well as the necessity and application frequency of retrieval in RAG. Then, we summarize the main training techniques of RA-LLMs in Section 4 and various RA-LLMs applications in Section 5.

**中文**

本次调查旨在通过分别从架构、培训策略和应用领域等方面总结代表性方法，对 RA-LLM 提供全面的概述。更具体地说，继第2节简要介绍LLM的背景知识之后，我们在第3节从RA-LLM的检索、生成和增强的几个主要角度回顾了现有研究，以及RAG中检索的必要性和应用频率。然后，我们在第 4 节中总结了 RA-LLM 的主要培训技术，并在第 5 节中总结了各种 RA-LLM 的应用。

### 段落 19 · Page 2

**EN**

Finally, in Section 6, we discuss key challenges and potential directions for future exploration. Concurrent to our survey, several related surveys have diverse focuses for RAG and LLMs. For example, Zhao et al. [193] specifically review multi-modal information-based RAG techniques and Zhao et al. [192] discuss the RAG for AIGC. Gao et al. [41] conduct a relatively comprehensive overview of RAG for LLMs. Our survey differs from these surveys in concentrating on technical perspectives and systematically reviewing models according to the architecture and training paradigm in RA-LLMs, as well as application tasks.

**中文**

最后，在第 6 节中，我们讨论了未来探索的主要挑战和潜在方向。与我们的调查同时进行的还有几项相关调查针对 RAG 和 LLM 的不同关注点。例如，赵等人。 [193]专门回顾了基于多模态信息的RAG技术和Zhao等人。 [192]讨论 AIGC 的 RAG。高等人。 [41]对法学硕士的 RAG 进行了相对全面的概述。我们的调查与这些调查的不同之处在于，我们专注于技术视角，并根据 RA-LLM 的架构和培训范式以及应用任务系统地审查模型。

### 段落 20 · Page 2

**EN**

2 BACKGROUND In this section, we briefly present the background of large language models and prompt learning. 2.1 Large Language Models (LLMs) Recently, the significant breakthrough of LLMs has revolutionized the field of artificial intelligence [7, 37, 194]. The advanced LLMs are typically pre-trained on extensive data with billion-level parameters and have demonstrated the ability to understand and generate human-like text, leading to advancements in various natural language processing tasks such as text generation and information retrieval [194, 195].

**中文**

2 背景 在本节中，我们简要介绍大型语言模型和即时学习的背景。 2.1 大型语言模型（LLM） 最近，LLM 的重大突破彻底改变了人工智能领域[7,37,194]。高级法学硕士通常在具有数十亿级参数的大量数据上进行预训练，并展示了理解和生成类人文本的能力，从而导致文本生成和信息检索等各种自然语言处理任务的进步[194, 195]。

### 段落 21 · Page 2

**EN**

LLMs can be adapted to a variety of downstream tasks by fine-tuning them on specific datasets, allowing them to specialize in particular domains or applications. In general, most existing LLMs can be broadly divided into three main categories: Encoder-only, Decoder-only, and Encoder-Decoder models. Encoder-only models, such as the BERT (Bidirectional Encoder Representations from Transformers) [ 25] family of models, process input text by encoding it into a high-dimensional space.

**中文**

法学硕士可以通过在特定数据集上进行微调来适应各种下游任务，从而使它们能够专注于特定领域或应用程序。一般来说，大多数现有的法学硕士可以大致分为三个主要类别：仅编码器模型、仅解码器模型和编码器-解码器模型。仅编码器模型，例如 BERT（来自 Transformers 的双向编码器表示）[25]模型系列，通过将输入文本编码到高维空间来处理输入文本。

### 段落 22 · Page 2

**EN**

The key feature of Encoder-only models is their bi-directional nature, meaning that they can take into account both the left and right context of each token when encoding it. This bi-directionality allows Encoder-only models to better understand the meaning of words in context, which is crucial for tasks like sentiment analysis, review reading, and text classification [25, 169]. In contrast to these models, 2

**中文**

仅编码器模型的关键特征是它们的双向性质，这意味着它们在编码时可以考虑每个标记的左右上下文。这种双向性使得仅编码器模型能够更好GEO解上下文中单词的含义，这对于情感分析、评论阅读和文本分类等任务至关重要 [25, 169]。与这些模型相比，2

### Page 3

### 段落 23 · Page 3

**EN**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA 2019 2020 2021 2022 2023 2024 RAG Framework/Pipeline Retriever Learning RAG Learning Pre-/Post-Retrieval Technique RAG (Lewis, 2020) REALM (Guu, 2020) kNN-LM (Khandelwal, 2019) FiD (Izacard, 2021) SE-FiD (Komeili, 2021) RETRO (Borgeaud, 2022) OpenBook (Lazaridou, 2022) IRCoT (Trivedi, 2023) DSP (Khattab, 2022) In-Context RALM (Ram, 2023) FLARE (Jiang, 2023) Self-RAG (Asai, 2023) REPLUG (Shi, 2023) AAR (Yu, 2023) SKR (Wang, 2023) REFEED (Yu, 2023) ITER- RETGEN (Shao, 2023) RADA (Xu, 2023) COMBO (Zhang, 2023) ToC (Kim, 2

**中文**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA 2019 2020 2021 2022 2023 2024 RAG Framework/Pipeline Retriever Learning RAG Learning Pre-/Post-Retrieval Technique RAG (Lewis, 2020) REALM (Guu, 2020) kNN-LM (Khandelwal, 2019) FiD (Izacard, 2021) SE-FiD (Komeili, 2021) RETRO (Borgeaud, 2022) OpenBook (Lazaridou, 2022) IRCoT (Trivedi, 2023) DSP (Khattab, 2022) In-Context RALM (Ram, 2023) FLARE (Jiang, 2023) Self-RAG (Asai, 2023) REPLUG (Shi, 2023) AAR (Yu, 2023) SKR (Wang, 2023) REFEED (Yu, 2023) ITER- RETGEN (Shao, 2023) RADA (Xu, 2023) COMBO （张，2023）ToC（金，2

### 段落 24 · Page 3

**EN**

023) SlimPLM (Tan, 2024) DPR (Karpukhin, 2020) RAG (Lewis, 2020) FiD-KD (Izacard, 2021) EPR (Rubin, 2021) Contriever (Gautier, 2022) FiD-Light (Hofstatter, 2023) CEIL (Ye, 2023) UPRISE (Cheng, 2023) ITER- RETGEN (Shao, 2023) RA-DIT (Lin, 2023) SAIL (Luo, 2023) RADA (Xu, 2023) REVEN (Huang, 2023) REALM (Guu, 2020) EMDR2 (Singh, 2021) Atlas (Izacard, 2023) RETRO (Borgeaud, 2022) RAG-end2end (siriwardhana, 2023) RETRO++ (Wang, 2023) Self-RAG (Asai, 2023) PRCA (Yang, 2023) SPALM (Yogatama, 2021) Re2G (Glass, 2022) HyPE (Gao, 2022) R-BM25 (Agrawal, 2022) Query2doc (Wang, 2023) Dr.ICL (Luo, 2023) UDR (Li, 2023) RECOMP (Xu, 2023) SAIL (Luo, 2023) LL

**中文**

023) SlimPLM (Tan, 2024) DPR (Karpukhin, 2020) RAG (Lewis, 2020) FiD-KD (Izacard, 2021) EPR (Rubin, 2021) Contriever (Gautier, 2022) FiD-Light (Hofstatter, 2023) CEIL (Ye, 2023) UPRISE (Cheng, 2023) ITER-RETGEN (Shao, 2023) RA-DIT (Lin, 2023) SAIL (Luo, 2023) RADA (Xu, 2023) REVEN (Huang, 2023) REALM (Guu, 2020) EMDR2 (Singh, 2021) Atlas (Izacard, 2023) RETRO (Borgeaud, 2022) RAG-end2end (siriwardhana, 2023) RETRO++ (Wang, 2023) Self-RAG (Asai, 2023) PRCA (Yang, 2023) SPALM (Yogatama, 2021) Re2G (Glass, 2022) HyPE (Gao, 2022) R-BM25 (Agrawal, 2022) Query2doc (Wang, 2023) Dr.ICL (Luo, 2023) UDR (Li, 2023) RECOMP (Xu, 2023) SAIL (Luo, 2023) LL

### 段落 25 · Page 3

**EN**

M-R (Wang, 2023) PRCA (Yang, 2023) SlimPLM (Tan, 2024) BlendFilter (Wang, 2024) QueryRewriter (Ma, 2023) >1000 [500, 1000) [200, 500) [100, 200) [50, 100) [20, 50) <20Citation Figure 2: Representing RAG and RA-LLMs methods organized by their main design focus, proposed time and impact (shown by citation).

**中文**

M-R (Wang, 2023) PRCA (Yang, 2023) SlimPLM (Tan, 2024) BlendFilter (Wang, 2024) QueryRewriter (Ma, 2023) >1000 [500, 1000) [200, 500) [100, 200) [50, 100) [20, 50) <20 引文图 2：代表 RAG 和 RA-LLM 方法，按其主要设计重点、提出的时间和影响（按引文显示）组织。

### 段落 26 · Page 3

**EN**

Note that the first author and year shown in the figure along with the model name can be used to locate corresponding reference. Decoder-only models generate text in a left-to-right fashion. As a representative Decoder-only model, GPT (Generative Pre-trained Transformer) [114] predicts the next token in a sequence based on the context provided by the previous tokens. Their architecture makes them particularly effective for tasks like language generation, code generation, and creative writing. Encoder-Decoder models, such as T5 (Text-To-Text Transfer Transformer) [116], uniquely transform a variety of NLP tasks into text generation problems.

**中文**

请注意，图中显示的第一作者和年份以及型号名称可用于查找相应的参考文献。仅解码器模型以从左到右的方式生成文本。作为代表性的仅解码器模型，GPT（生成预训练变换器）[114]根据先前标记提供的上下文来预测序列中的下一个标记。它们的架构使它们对于语言生成、代码生成和创意写作等任务特别有效。编码器-解码器模型，例如 T5（文本到文本传输转换器）[116]，独特地将各种 NLP 任务转换为文本生成问题。

### 段落 27 · Page 3

**EN**

To be more specific, the encoder in T5 processes the input sequence to capture its meaning, while the decoder generates the output sequence based on the encoded information. This T5 architecture is well-suited for tasks that involve converting one sequence into another, such as machine translation, summarization, and conversational response generation. 2.2 Prompt Learning 2.2.1 Prompting Engineering. Due to the massive parameters of LLMs, prompt learning emerged as a paradigm to leverage the power of LLM to implement various tasks [ 194, 195], instead of fine-tuning the LLMs extensively.

**中文**

更具体地说，T5 中的编码器处理输入序列以捕获其含义，而解码器则根据编码信息生成输出序列。这种 T5 架构非常适合涉及将一个序列转换为另一序列的任务，例如机器翻译、摘要和会话响应生成。 2.2 及时学习 2.2.1 及时工程。由于法学硕士的参数庞大，即时学习成为一种范式，利用法学硕士的力量来实现各种任务[194, 195]，而不是对法学硕士进行广泛的微调。

### 段落 28 · Page 3

**EN**

Prompt learning carefully designs the input that guides the model to perform downstream tasks in LLMs. For example, early methods [7, 110] provide manually crafted templates to handle various tasks in NLP. Specifically, Encoder-only models like BERT typically adopt cloze prompts because they very closely match the form of their pre-training task [ 20, 110]. For other models like GPT, prefix prompts tend to be more suitable as they mesh well with the generation tasks [7]. However, manually designed prompts rely on human experience without effectiveness guarantees.

**中文**

即时学习仔细设计输入，指导模型执行法学硕士中的下游任务。例如，早期的方法 [7, 110] 提供手动制作的模板来处理 NLP 中的各种任务。具体来说，像 BERT 这样的纯编码器模型通常采用完形填空提示，因为它们与预训练任务的形式非常匹配 [20, 110]。对于 GPT 等其他模型，前缀提示往往更合适，因为它们与生成任务很好地配合 [7]。然而，手动设计的提示依赖于人类经验，缺乏有效性保证。

### 段落 29 · Page 3

**EN**

To address this limitation, soft prompt tuning was developed to learn the trainable continuous prompt embeddings [83, 150, 151]. For instance, Prefix-Tuning [83] prepends a series of prefix embedding in the input, which can be trained and updated. This apportion allows prompts not to be real text, giving more flexibility in the generation of prompts. However, due to the lack of domainspecific knowledge, the model might still not generate accurate responses when facing new tasks. 2.2.2 In-Context Learning (ICL). To overcome the limitations of vanilla prompt learning, recent efforts [66, 89, 191] have developed in-context learning (ICL).

**中文**

为了解决这个限制，开发了软提示调整来学习可训练的连续提示嵌入[83,150,151]。例如，前缀调整[83]在输入中预先添加一系列前缀嵌入，可以对其进行训练和更新。这种分配允许提示不是真实的文本，从而在提示的生成方面提供更大的灵活性。然而，由于缺乏特定领域的知识，模型在面对新任务时可能仍然无法生成准确的响应。 2.2.2 情境学习（ICL）。为了克服普通即时学习的局限性，最近的努力[66,89,191]开发了情境学习（ICL）。

### 段落 30 · Page 3

**EN**

ICL is a specific method of prompt learning that gives the model a few demonstrations of tasks within the prompt. This paradigm allows pre-trained LLMs to understand the pattern provided by the demonstrations to solve novel tasks without the need for fine-tuning. For example, by carefully selecting a few demonstrations, GPT-3 [7] has shown the capability to perform few-shot tasks [89]. This success indicates that LLMs have a remarkable ability to rapidly adapt to new tasks based on task-specific knowledge. 3

**中文**

ICL 是一种特定的提示学习方法，它为模型提供了一些提示中任务的演示。这种范例允许预先训练的法学硕士理解演示提供的模式来解决新任务，而无需进行微调。例如，通过仔细选择一些演示，GPT-3 [7] 显示了执行少量任务的能力 [89]。这一成功表明法学硕士具有基于特定任务知识快速适应新任务的卓越能力。 3

### Page 4

### 段落 31 · Page 4

**EN**

Conference’17, July 2017, Washington, DC, USA Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li Despite its effectiveness, ICL usually relies heavily on the quality of the provided demonstrations [143? ], which may lead to the generation of sub-optimal outputs. Even worse, ICL may not have enough necessary information or prior knowledge to guide the LLMs in generating accurate responses. To address the aforementioned limitations of ICL, more recent studies introduce Retrieval-Augmented Generation (RAG) technologies [74, 117, 135].

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Wenqi Fan、Yujuan Ding、Liangbo Ning、Shijie Wang、Hengyun Li、Dawei Yin、Tat-Seng Chua 和 Qing Li 尽管 ICL 有效，但通常严重依赖所提供演示的质量 [143？ ]，这可能会导致生成次优输出。更糟糕的是，ICL 可能没有足够的必要信息或先验知识来指导法学硕士生成准确的答案。为了解决 ICL 的上述局限性，最近的研究引入了检索增强生成 (RAG) 技术 [74,117,135]。

### 段落 32 · Page 4

**EN**

By integrating retrieval with generation, RAG models provide a promising direction for enhancing the performance and adaptability of LLMs across various tasks. 3 RETRIEV AL-AUGMENTED LARGE LANGUAGE MODELS (RA-LLMS) The RAG framework in the era of LLMs consists of several major processes: retrieval, generation, and augmentation, as well as the mechanism to determine whether the retrieval is needed. In this section, we will introduce important techniques involved in each process.

**中文**

通过将检索与生成相结合，RAG 模型为增强 LLM 在各种任务中的性能和适应性提供了一个有前途的方向。 3 检索增强大型语言模型（RA-LLMS） LLM时代的RAG框架由检索、生成和增强几个主要过程组成，以及确定是否需要检索的机制。在本节中，我们将介绍每个过程中涉及的重要技术。

### 段落 33 · Page 4

**EN**

3.1 Retrieval Given the query from the input of LLMs, the retrieval process in RAG aims to provide relevant information from the external knowledge sources, which can be either open-sourced or closed-sourced as shown in Figure 3. The key component, retriever, as further detailed in Figure 4, consists of several procedures, functioning as a whole to measure the relevance between the query and documents in the database for effective information retrieval. The specific pipeline of the retrieval is further determined by whether the preand post-retrieval processes are included.

**中文**

3.1 检索 给定来自法学硕士输入的查询，RAG 中的检索过程旨在从外部知识源提供相关信息，外部知识源可以是开源的，也可以是闭源的，如图 3 所示。关键组件检索器（如图 4 中进一步详述）由多个过程组成，作为一个整体来衡量查询与数据库中文档之间的相关性，以实现有效的信息检索。检索的具体流程还根据是否包含检索前和检索后流程来进一步确定。

### 段落 34 · Page 4

**EN**

In this subsection, we will introduce the major techniques involved in the retrieval of traditional and LLM-based RAGs, including the retriever type, retrieval granularity, pre- and post-retrieval enhancement, and database construction. 3.1.1 Retriever Type. Retrieval methods can be generally categorized into two types: sparse and dense, based on the information encoding methods. Sparse retrieval is word-based and applied in text retrieval mostly, while dense retrieval embeds queries and external knowledge into vector spaces and can applied to various data formats.

**中文**

在本小节中，我们将介绍传统 RAG 和基于 LLM 的 RAG 检索中涉及的主要技术，包括检索器类型、检索粒度、检索前和检索后增强以及数据库构建。 3.1.1 猎犬类型。根据信息编码方法，检索方法通常可分为两类：稀疏和密集。稀疏检索是基于单词的，主要应用于文本检索，而密集检索将查询和外部知识嵌入到向量空间中，可以应用于各种数据格式。

### 段落 35 · Page 4

**EN**

As a straightforward approach, sparse retrieval, e.g., TF-IDF and BM25 [125, 142], usually relies on inverted index matching along with the raw data input. For example, many studies directly apply BM25 for passage-level retrieval to facilitate their RAG [ 10, 57, 117, 168, 196, 197], where passages are specifically represented as a bag of words and ranked based on term and inverse document frequencies [ 54]. On top of offering supplementary to enhance the input of the generator, sparse retrieval has also been used to find demonstrations to function in in-context learning for RA-LLMs [2, 96, 126, 138, 176].

**中文**

作为一种简单的方法，稀疏检索，例如 TF-IDF 和 BM25 [125, 142]，通常依赖于倒排索引匹配以及原始数据输入。例如，许多研究直接应用 BM25 进行段落级检索，以促进其 RAG [10,57,117,168,196,197]，其中段落被具体表示为词袋，并根据术语和逆文档频率进行排名 [54]。除了提供补充以增强生成器的输入之外，稀疏检索还被用来寻找在 RA-LLM 的上下文学习中起作用的演示 [2, 96, 126, 138, 176]。

### 段落 36 · Page 4

**EN**

The main limitation of applying sparse retrieval in RAG is its no-training nature, which makes the retrieval performance heavily rely on the quality of the database and the query. Moreover, such fixed term-based methods only support similarity-based retrieval, while cannot be adapted for other retrieval criteria possibly existing in LLM applications, such as the diversity [31]. Dense retrieval, on the contrary, embeds the query and documents into continuous vector space with certain criteria, for example, semantic similarity [61]. Dense retrieval methods are usually trainable, therefore holding more flexibility and potential in adaptation.

**中文**

在 RAG 中应用稀疏检索的主要限制是其无需训练的性质，这使得检索性能严重依赖于数据库和查询的质量。此外，这种基于固定术语的方法仅支持基于相似性的检索，而不能适应LLM应用中可能存在的其他检索标准，例如多样性[31]。相反，密集检索将查询和文档嵌入到具有特定标准的连续向量空间中，例如语义相似性[61]。密集检索方法通常是可训练的，因此具有更大的灵活性和适应潜力。

### 段落 37 · Page 4

**EN**

As the key component of dense retriever, the embedding models have delicately different designs in existing RAG models. A simple design [62, 72, 165] is to directly use a part of the generation model as the embedding layer of the retriever, which might be able to enhance the alignment between the retrieval and generation processes. BERT-based backbone [ 25] is widely applied in retrieval models. One common retriever design in RAG is to construct two-stream encoders with the BERT structure (one encoder for the query and the other for the documents), which is also called bi-encoder [135, 164].

**中文**

作为密集检索器的关键组成部分，嵌入模型与现有的RAG模型有着微妙的不同设计。一个简单的设计[62,72,165]是直接使用生成模型的一部分作为检索器的嵌入层，这可能能够增强检索和生成过程之间的对齐。基于BERT的主干网[25]广泛应用于检索模型中。 RAG 中一种常见的检索器设计是构建具有 BERT 结构的双流编码器（一个编码器用于查询，另一个编码器用于文档），也称为双编码器 [135, 164]。

### 段落 38 · Page 4

**EN**

Early-stage RAG methods tend to freeze [6, 117] or partially freeze [74] the parameters of the retriever to perform general-level relevant knowledge extraction and pay more attention to the knowledge leveraging and generator finetuning. Large-scale specialized pre-training further enhances RAG models to excel in more knowledge-intensive tasks. One typical success is Dense Passage Retriever (DPR) [61], which uses a BERTbased backbone and is pre-trained specifically for the OpenQA task with question-answer pair data.

**中文**

早期的RAG方法倾向于冻结[6, 117]或部分冻结[74]检索器的参数来执行一般级别的相关知识提取，并更加关注知识利用和生成器微调。大规模的专业预训练进一步增强了 RAG 模型，使其在知识密集型任务中表现出色。一个典型的成功案例是密集通道检索器（DPR）[61]，它使用基于 BERT 的骨干网，并专门针对带有问答对数据的 OpenQA 任务进行了预训练。

### 段落 39 · Page 4

**EN**

DPR has shown strong capacity as a pre-trained retriever, facilitating many RAG models to succeed in various downstream tasks [54, 74, 135, 139, 141]. It has also been regarded as the first step in the RAG paradigm for improving the performance of LLMs, which may further enhance the alignment of the embeddings between queries and relevant textual data through fine-tuning [16]. A recent study [122] has also discovered that DPR training decentralizes how knowledge is stored in the network, creating multiple access pathways to the same information.

**中文**

DPR 作为预训练检索器表现出了强大的能力，有助于许多 RAG 模型在各种下游任务中取得成功 [54,74,135,139,141]。它也被认为是 RAG 范式中提高 LLM 性能的第一步，可以通过微调进一步增强查询和相关文本数据之间嵌入的对齐[16]。最近的一项研究 [122] 还发现，DPR 训练分散了知识在网络中的存储方式，从而创建了对同一信息的多种访问途径。

### 段落 40 · Page 4

**EN**

With effective fine-tuning, bi-encoder retrievers are also applied widely in ICL-based RAG [82, 93, 101, 111, 126, 176]. Specifically, they have been more often used for sentence embedding similarity-based retrieval, as well as for some special requirement in ICL, such as diverse example retrieval [176]. Another stream of dense retrievers having been widely applied in RA-LLMs uses one encoder only, which may be based on Transformer, BERT or other off-the-shelf sequence modeling backbones.

**中文**

通过有效的微调，双编码器检索器也广泛应用于基于 ICL 的 RAG [82,93,101,111,126,176]。具体来说，它们更常用于基于句子嵌入相似性的检索，以及 ICL 中的一些特殊要求，例如多样化的示例检索[176]。另一种已广泛应用于 RA-LLM 的密集检索器流仅使用一个编码器，该编码器可能基于 Transformer、BERT 或其他现成的序列建模主干。

### 段落 41 · Page 4

**EN**

These one-encoder retrievers are generally pre-trained on largescale unaligned documents by contrastive learning [ 122], which may therefore excel for their versatility, meaning that they can transfer and generalize better to new domains or tasks. Such generalpurpose pre-trained retrievers, e.g., Contriever [42] and Spider [118], would be more flexible to use in LLMs targeting on various tasks and have demonstrated their effectiveness in many RA-LLM methods, such as In-Context RALM [117], Atlas [55] and Self-RAG [5].

**中文**

这些单编码器检索器通常通过对比学习 [122] 对大规模未对齐文档进行预训练，因此可能因其多功能性而表现出色，这意味着它们可以更好地迁移和泛化到新领域或任务。这种通用的预训练检索器，例如 Contriever [42] 和 Spider [118]，可以更灵活地用于针对各种任务的 LLM，并且已经在许多 RA-LLM 方法中证明了它们的有效性，例如 In-Context RALM [117]、Atlas [55] 和 Self-RAG [5]。

### 段落 42 · Page 4

**EN**

According to experimental results in existing studies [182], for opendomain QA tasks, when cooperated with InstructGPT [ 107], applying general-purpose pre-trained retriever (Contriever) without fine-tuning achieves comparable performance to sparse retriever (BM25). However, they are both worse than the DPR model finetuned on target datasets, showing the effectiveness of fine-tuning on targeted tasks and data. 3.1.2 Retrieval Granularity. Retrieval granularity denotes the retrieval unit in which the corpus is indexed, e.g., document, passage, token, or other levels like entity. For RAG, the choice of retrieval 4

**中文**

根据现有研究[182]的实验结果，对于开放域QA任务，当与InstructGPT[107]配合时，应用通用预训练检索器（Contriever）而不进行微调，可以达到与稀疏检索器（BM25）相当的性能。然而，它们都比在目标数据集上微调的 DPR 模型差，显示了对目标任务和数据进行微调的有效性。 3.1.2 检索粒度。检索粒度表示对语料库进行索引的检索单元，例如文档、段落、标记或其他级别（如实体）。对于RAG，检索4的选择

### Page 5

### 段落 43 · Page 5

**EN**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA Pre-retrieval Enhancement Post-retrieval Enhancement Generator Generator Generator According to your sympton and conditions, you are likely having Coronary Artery Disease (CAD). CAD is caused by plaque buidup in the wall of the arteries that supply blood to the heart (called coronary arteries).... Rewrite Expand Filter Compress Sympton: I had very bad cardiac pain this morning, also felt dizzy and nauseous. It lasted for a few minutes. Patient file: female, 34 years old, height: 170cm, weight: 55kg,...

**中文**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA 检索前增强 检索后增强 生成器 生成器 生成器 根据您的症状和情况，您可能患有冠状动脉疾病 (CAD)。 CAD 是由向心脏供血的动脉壁（称为冠状动脉）内积聚斑块引起的。... 重写 展开过滤器 压缩 症状： 今天早上我感到非常严重的心脏疼痛，还感到头晕和恶心。持续了几分钟。患者档案：女，34岁，身高：170cm，体重：55kg，...

### 段落 44 · Page 5

**EN**

Retriever OR OR Output-layer Augmentation Intermidiate-layer Augmentation Input-layer Augmentation ... ... The first symptom sign of a heart attack is sudden cardiac arrest. Angina pectoris is caused by a decrease in myocardial blood flow. Figure 3: Illustration of the basic Retrieval-Augmented Large Language Models (RA-LLMs) framework for a specific QA task, which consists of three main components: retrieval, augmentation, and generation. Retrieval may have different procedures with various designs, which optionally includes pre-retrieval and post-retrieval processes.

**中文**

猎犬或或输出层增强中间层增强输入层增强……心脏病发作的第一个症状是心脏骤停。心绞痛是由心肌血流量减少引起的。图 3：用于特定 QA 任务的基本检索增强大型语言模型 (RA-LLM) 框架的图示，该框架由三个主要组件组成：检索、增强和生成。检索可以具有具有不同设计的不同程序，其可选地包括检索前和检索后过程。

### 段落 45 · Page 5

**EN**

The retrieved documents are further leveraged in generation with the augmentation module, which may be at different integration stages. Database Query Chunking/ Tokenizing/ ... Indexing Dense Retrieval Embedding Sparse Retrieval Relevance Scoring Relevance Scoring Retrieved Results (Chunks/Documents/ Tokens/Entities/..) Figure 4: Illustration of the retriever in RA-LLMs, which can be implemented in either dense or sparse manners, each with several key operations.

**中文**

检索到的文档在生成过程中进一步利用增强模块，该模块可能处于不同的集成阶段。数据库查询分块/标记化/...索引密集检索嵌入稀疏检索相关性评分相关性评分检索结果（块/文档/令牌/实体/..）图4：RA-LLM中检索器的图示，可以以密集或稀疏方式实现，每种方式都有几个关键操作。

### 段落 46 · Page 5

**EN**

granularity can significantly impact the overall performance of the model in terms of effectiveness and efficiency as they determine the saving space for the database as well as the computational cost for searching [4]. Early stage retrieval-augmented language models [10] propose to retrieve whole pieces of documents, and then apply a machine comprehension model trained to detect answer spans in the returned documents, which focuses more on language reading and key information locating in the document.

**中文**

粒度可以显着影响模型在有效性和效率方面的整体性能，因为它们决定了数据库的节省空间以及搜索的计算成本[4]。早期的检索增强语言模型[10]提出检索整篇文档，然后应用经过训练的机器理解模型来检测返回文档中的答案范围，该模型更注重语言阅读和文档中关键信息的定位。

### 段落 47 · Page 5

**EN**

In generative language models, Chunk retrieval (also called passages in some references [46, 57, 61]) is common, which has been used in both traditional and LLM-based RAG models such as REALM [46], RAG [74] and Atlas [55]. A more fine-grained retrieval, i.e., token retrieval, instead can be done with faster searching but will bring more burden for the database saving. Token retrieval is more suitable in cases requiring rare patterns or out-of-domain data [ 62], meanwhile cooperates well with the every-token retrieval strategy as applied in kNN-LM and other similar work [ 47, 104, 180].

**中文**

在生成语言模型中，块检索（在一些参考文献中也称为段落[46,57,61]）很常见，它已被用于传统和基于LLM的RAG模型，例如REALM [46]、RAG [74]和Atlas [55]。更细粒度的检索，即令牌检索，可以通过更快的搜索来完成，但会给数据库节省带来更多负担。令牌检索更适合需要稀有模式或域外数据的情况[62]，同时与kNN-LM和其他类似工作中应用的每个令牌检索策略很好地配合[47,104,180]。

### 段落 48 · Page 5

**EN**

In comparison, a text chunk may contain compact and complete information with less redundancy and irrelevancy, therefore becoming the mainstream retrieval text granularity in RAG. Another major retrieval granularity proposed in RAG is entity retrieval. Unlike the above types of granularity, entity retrieval is designed from the perspective of knowledge rather than language. Févry et al . [39] introduce the Entities as Experts (E AE) model, which divides the parameter space of language models according to the entity identity.

**中文**

相比之下，文本块可以包含紧凑完整的信息，冗余和不相关性较少，因此成为RAG中主流的检索文本粒度。 RAG 中提出的另一个主要检索粒度是实体检索。与上述类型的粒度不同，实体检索是从知识而不是语言的角度设计的。费夫里等人。 [39]引入了实体专家（E AE）模型，该模型根据实体身份划分语言模型的参数空间。

### 段落 49 · Page 5

**EN**

The proposed EAE model aims to learn entity representations from the text along with other model parameters with the Wikipedia database and represent knowledge with entity memory. At a more fine-grained level, de Jong et al. [22] propose to build the knowledge base by learning and retrieving mention rather than entity. Overall, applying entity or mention-level retrieval in RAG would be more effective for entity-centric tasks, and more efficient in space compared to token-wise retrieval. 3.1.3 Pre-retrieval and Post-retrieval Enhancement.

**中文**

所提出的 EAE 模型旨在通过维基百科数据库从文本中学习实体表示以及其他模型参数，并使用实体记忆表示知识。在更细粒度的层面上，de Jong 等人。 [22]建议通过学习和检索提及而不是实体来构建知识库。总体而言，在 RAG 中应用实体或提及级检索对于以实体为中心的任务来说会更有效，并且与令牌明智的检索相比，在空间上也更高效。 3.1.3 检索前和检索后增强。

### 段落 50 · Page 5

**EN**

To ensure the retrieval quality, i.e., increase the accuracy and relevance of the retrieved results, various pre- and post-retrieval strategies have been proposed to further enhance the input and output of the retriever. Wang et al. [156] propose a query expansion approach Query2doc, which generates pseudo-documents by few-shot prompting LLMs and expands the query with the relevant information in pseudodocuments to improve the query disambiguation and guide the retrievers. They have empirically demonstrated that such a method can boost the performance of both the sparse and dense retriever [61] 5

**中文**

为了确保检索质量，即提高检索结果的准确性和相关性，人们提出了各种检索前和检索后策略来进一步增强检索器的输入和输出。王等人。 [156]提出了一种查询扩展方法Query2doc，它通过few-shot提示LLM生成伪文档，并用伪文档中的相关信息扩展查询，以改善查询消歧并指导检索器。他们凭经验证明这种方法可以提高稀疏和密集检索器的性能 [61] 5

### Page 6

### 段落 51 · Page 6

**EN**

Conference’17, July 2017, Washington, DC, USA Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li on ad-hoc information retrieval datasets. Similarly, Gao et al. [40] propose Hypothetical Document Embedding (HyDE) method, which instructs an LLM to generate hypothetical documents for the given query. The hypothetical documents are then used as new queries to get embedded and search for neighbors with the dense retriever.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Wenqi Fan、Yujuan Ding、Liangbo Ning、Shijie Wang、Hengyun Li、Dawei Yin、Tat-Seng Chua 和 Qing Li，关于临时信息检索数据集。同样，高等人。 [40]提出假设文档嵌入（HyDE）方法，该方法指示法学硕士为给定查询生成假设文档。然后，假设的文档被用作新的查询来嵌入并使用密集检索器搜索邻居。

### 段落 52 · Page 6

**EN**

Another pre-retrieval strategy,query rewrite [98], aims to close the gaps between the input text and the needed knowledge in retrieval, to reformulate the original question into a more conducive version to retrieve. Specifically, Ma et al. [98] propose the Rewrite- Retrieve-Read framework, which prompts an LLM to generate the query for the retrieval function. The motivation of the rewriting step is to clarify the retrieval need in the new query to ease the burden on the retrieval function to comprehend the input and enhance the output, i.e., retrieved relevant information.

**中文**

另一种预检索策略，查询重写[98]，旨在缩小输入文本与检索所需知识之间的差距，将原始问题重新表述为更有利于检索的版本。具体来说，Ma 等人。 [98]提出了重写-检索-读取框架，该框架提示法学硕士生成检索函数的查询。重写步骤的动机是澄清新查询中的检索需求，以减轻检索功能理解输入并增强输出（即检索相关信息）的负担。

### 段落 53 · Page 6

**EN**

They have tested both the settings of using a frozen LLM and a trainable model to be the rewriter, both outperforming naive RAG or generation models, demonstrating diverse performance on different tested QA datasets though. Tan et al. [146] also formulate a query rewriting strategy in their model that decomposes the heuristic answer from a proxy generation model into distinct claims. Yu et al. [183] propose query augmentation to combine the original query and the preliminary generated outputs as a new query, which is further used to retrieve relevant information from the external database.

**中文**

他们测试了使用冻结的 LLM 和可训练模型作为重写器的设置，两者都优于朴素的 RAG 或生成模型，但在不同的测试 QA 数据集上展示了不同的性能。谭等人。 [146]还在他们的模型中制定了查询重写策略，将代理生成模型的启发式答案分解为不同的声明。于等人。 [183]​​提出查询增强，将原始查询和初步生成的输出组合为新查询，进一步用于从外部数据库检索相关信息。

### 段落 54 · Page 6

**EN**

The retrieved results can inspire the language model to rethink the generated results and enhance them. Compared to applying only the original query, such augmentation may contribute more relevant information retrieved from the corpus for the directly clarification of query-output relationships. Including initial output in the new query further enhances the lexical and semantic overlap between the supporting documents to be retrieved with the given question. Query augmentation achieves overall better performance among these query enhancement strategies since it may process all retrieved knowledge collectively while generating answers [155].

**中文**

检索到的结果可以启发语言模型重新思考生成的结果并对其进行增强。与仅应用原始查询相比，这种增强可以贡献从语料库检索到的更多相关信息，以直接阐明查询-输出关系。在新查询中包括初始输出进一步增强了要通过给定问题检索的支持文档之间的词汇和语义重叠。查询增强在这些查询增强策略中实现了总体更好的性能，因为它可以在生成答案的同时集体处理所有检索到的知识[155]。

### 段落 55 · Page 6

**EN**

Post-retrieval enhancement denotes the procedure to process the extracted top-k documents from the retriever before feeding them to the generator for the sake of better alignment between the retrieval and generation stages [173], particularly for closed-source generators such as LLMs. For example, Yang et al. [173] propose the Pluggable Reward-driven Context Adapter (PRCA) that enables to fine-tune the lightweight adapter instead of the generator on specific datasets. It also distills the retrieved documents through reinforcement learning with the rewards resulting from the generator. Glass et al.

**中文**

检索后增强是指在将检索器提取的 top-k 文档馈送到生成器之前对其进行处理的过程，以便检索和生成阶段之间更好地对齐[173]，特别是对于诸如 LLM 之类的闭源生成器。例如，杨等人。 [173]提出了可插入奖励驱动上下文适配器（PRCA），它能够在特定数据集上微调轻量级适配器而不是生成器。它还通过强化学习和生成器产生的奖励来提取检索到的文档。格拉斯等人。

### 段落 56 · Page 6

**EN**

[44] propose Retrieve-Rerank-Generate (R2G) method, which assembles the retrieved documents of different retrieval approaches with the rerank operation to boost the robustness of the retrieval results. Another consideration for applying post-retrieval enhancement is that the retrieved information may sometimes be irrelevant or contain noise, which might not help with the generation model for the task, or even worse, harm the generation process [159]. Wang et al. [159], Asai et al. [5], Yu et al. [183] propose different strategies to mitigate the noise in retrieved knowledge documents. However, Xiong et al.

**中文**

[44]提出了Retrieve-Rerank-Generate（R2G）方法，该方法将不同检索方法的检索文档与重新排序操作组合起来，以提高检索结果的鲁棒性。应用检索后增强的另一个考虑因素是，检索到的信息有时可能不相关或包含噪声，这可能对任务的生成模型没有帮助，甚至更糟糕的是，损害生成过程[159]。王等人。 [159]，浅井等人。 [5]，余等人。 [183]​​提出了不同的策略来减轻检索到的知识文档中的噪声。然而，熊等人。

### 段落 57 · Page 6

**EN**

[166] empirically studied that these methods are dependent on the LLM’s confidence levels, which might not be as precise as expected. For this problem, Wang et al. [155] propose BlendFilter, which simultaneously considers the pre-retrieval query generation blending and the post-retrieval knowledge filtering. This method can tackle the complex questions as well as the noisy retrieved knowledge problems, therefore comprehensively enhancing the RA-LLM performance.

**中文**

[166]根据经验研究发现，这些方法取决于法学硕士的置信水平，这可能不如预期的那么精确。对于这个问题，Wang 等人。 [155]提出了BlendFilter，它同时考虑检索前查询生成混合和检索后知识过滤。该方法可以解决复杂问题以及噪声检索知识问题，从而全面提高 RA-LLM 的性能。

### 段落 58 · Page 6

**EN**

More recently, advanced RAG pipelines have been proposed using LLMs to generate reasoning paths and plans with the Information Retrieval (IR) module to iteratively retrieve knowledge to enhance LLM-based generation [130, 172, 175]. However, Zhu et al. [198] point out that if the outputs of IR and LLM are low-quality, the retrieval and generation processes will get hindered by each other with such an iterative guidance pipeline. To overcome this barrier, they propose a new reasoning approach for query and retrieved knowledge enhancement.

**中文**

最近，有人提出使用 LLM 来生成推理路径和计划的高级 RAG 管道，并使用信息检索 (IR) 模块迭代检索知识以增强基于 LLM 的生成 [130, 172, 175]。然而，朱等人。 [198]指出，如果 IR 和 LLM 的输出质量较低，检索和生成过程将在这种迭代指导管道中相互阻碍。为了克服这一障碍，他们提出了一种用于查询和检索知识增强的新推理方法。

### 段落 59 · Page 6

**EN**

Post-retrieval strategies may also function to enhance the compatibility between the retrieved results and the generation models. For example, one of the main limitations of existing LLMs is the length of the input tokens, which prevents long retrieved documents being directly incorporated into existing RA-LLMs. For this limitation, Xu et al. [168] propose Retrieve, Compress, Prepend (RECOMP), which adds an intermediate step to process the retrieved documents into a textual summary before in-context augmentation in the generation process.

**中文**

检索后策略还可以起到增强检索结果和生成模型之间的兼容性的作用。例如，现有 LLM 的主要限制之一是输入标记的长度，这阻止了长检索文档直接合并到现有 RA-LLM 中。对于这一限制，Xu 等人。 [168]提出检索、压缩、预置（RECOMP），它添加了一个中间步骤，用于在生成过程中进行上下文增强之前将检索到的文档处理为文本摘要。

### 段落 60 · Page 6

**EN**

From another perspective, long retrieved passage list leads to a high inference latency when using auto-regressive decoding at generation stage, which hurts the model’s efficiency. For this limitation, Hofstätter et al. [50] propose a light version of FiD model that compresses the encoded vectors per retrieved passage before concatenating and feeding them through the decoder and also includes a re-ranker on the retrieved results before applying them in the generation. 3.1.4 Database. Retrieval in RAG is conducted based on external knowledge source, which can be a closed- or open-sourced [98, 100], as illustrated in Figure 3.

**中文**

从另一个角度来看，在生成阶段使用自回归解码时，长检索的段落列表会导致较高的推理延迟，这会损害模型的效率。对于这一限制，Hofstätter 等人。 [50]提出了 FiD 模型的轻型版本，该模型在连接并通过解码器馈送编码向量之前压缩每个检索到的通道的编码向量，并且还包括在将检索结果应用于生成之前对检索结果进行重新排序。 3.1.4 数据库。 RAG 中的检索是基于外部知识源进行的，外部知识源可以是封闭源或开源的 [98, 100]，如图 3 所示。

### 段落 61 · Page 6

**EN**

Closed-sourced database generally stores key-value pairs for knowledge, which can be constructed in various ways. The keys are primarily used for similarity matching, being as sparse vectors such as in BM25 or dense embeddings from the retrieval encoding. The value depends on the specific retrieval target, which is raw text in most cases [6, 46, 54, 72, 74, 129]. For example, each Wikipedia article is split into disjoint 100-word chunks, to make a total of 21M documents in early RAG [74]. Each document is encoded by a dense embedding and saved in the database as the value and key, respectively.

**中文**

闭源数据库通常存储知识的键值对，可以通过多种方式构建。键主要用于相似性匹配，作为稀疏向量（例如 BM25 中的向量）或来自检索编码的密集嵌入。该值取决于具体的检索目标，大多数情况下是原始文本[6,46,54,72,74,129]。例如，每篇维基百科文章被分割成不相交的 100 个单词的块，在早期的 RAG 中总共形成 2100 万个文档 [74]。每个文档都通过密集嵌入进行编码，并分别作为值和键保存在数据库中。

### 段落 62 · Page 6

**EN**

The value can store tokens too, one for each as applied in kNN-LM [62] and SPALM [180]. The source of the database depends on the specific application domains and tasks.

**中文**

该值也可以存储令牌，每个令牌一个，如 kNN-LM [62] 和 SPALM [180] 中应用的那样。数据库的来源取决于具体的应用领域和任务。

### 段落 63 · Page 6

**EN**

Wikipedia is one of the most commonly applied general retrieval sets in previous RAG work, which stores factual structured 1Retrievers: [BE: Bi-Encoder (also referred as dual encoder), OE: One-Encoder, BT: BERT-style Transformer, GP: Partial Generation, SE: Search Engine, SR: Sparse Retrieval, DPR:[ 61]], Generators: [DT: Decoder-only Transformer, ET: Encoderonly Transformer, ED: Encoder-Decoder], Pre-/Post-Retrieval techniques: [RQG: Retrieval Query Generation, QE: Query Expansion, (T)RR: (Trainable) Re-Ranker, TRA: Trainable Retriever Adaptor, CR: Candidate Retrieval, CM: Critic Model], Augmentations:[Output: Output-layer Integration, Input

**中文**

Wikipedia 是以往 RAG 工作中最常用的通用检索集之一，存储了事实结构化的 1Retrievers：[BE: Bi-Encoder（也称为双编码器）、OE: One-Encoder、BT: BERT-style Transformer、GP: Partial Generation、SE: Search Engine、SR: Sparse Retrieval、DPR:[ 61]]、Generators：[DT: Decoder-only Transformer、ET:仅编码器Transformer，ED：编码器-解码器]，检索前/检索后技术：[RQG：检索查询生成，QE：查询扩展，（T）RR：（可训练）重排器，TRA：可训练检索器适配器，CR：候选检索，CM：批评模型]，增强：[输出：输出层集成，输入

### 段落 64 · Page 6

**EN**

: Input-layer Integration, Inter: Intermediate-layer Integration, Demon: As demonstration], Tasks: [AQA: Abstractive Question Answering, QG: Question Generation, NQ: Natural Questions, WQ: WebQuestions, CT: CuratedTrec, FV: Factor Verification, TQA: TriviaQA, WizInt: Wizard of the Internet task, WoW: Wizard of Wikipedia task, MHQA: Multi-hop QA, CQA: Conversational QA, EL: Entity Linking, SF: Slot-filling, MMLU: Massively-Multitask Language Understanding, CR: Commonsense Reasoning, LongQA: Long-form QA, OS: Open-domain Summarization, BG: Biography Generation, UR: Utterance Representing, RF: Retrieval Fusion] 6

**中文**

：输入层集成、Inter：中间层集成、Demon：作为演示]、任务：[AQA：抽象问答、QG：问题生成、NQ：自然问题、WQ：WebQuestions、CT：CulatedTrec、FV：因子验证、TQA：TriviaQA、WizInt：互联网任务向导、WoW：维基百科任务向导、MHQA：多跳 QA、CQA：会话QA、EL：实体链接、SF：槽位填充、MMLU：大规模多任务语言理解、CR：常识推理、LongQA：长格式 QA、OS：开放域摘要、BG：传记生成、UR：话语表示、RF：检索融合] 6

### Page 7

### 段落 65 · Page 7

**EN**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA Time Model Cite Retriever RetTrain RetAug Stage Pre-/Post- Retrieval Generator Aug Evaluation 2019 kNN-LM [62] 619 DR(GP) No Inf RA DT Output LG 2020 REALM [46] 1437 DR(BE,BT) Yes PT+FT / ET Input OpenQA(NQ, WQ, CT) 2020 RAG [74] 2125 DR(DPR) Yes FT / ED (BART) Input OpenQA, AQA, Jeopardy QG, FV 2021 FiD [54] 780 SR(BM25)/ DR(DPR) No FT / ED (T5/BART) Input OpenQA 2021 SE-FiD [68] 286 SE(Bing) No Inf RQG FiD Input WizInt, WoW 2021 FiD-KD [53] 190 DR(BE) Yes FT CR FiD Input OpenQA 2021 RETRO [6] 683 DR(BERT, DPR) No PT

**中文**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, Washington, DC, USA Time Model Cite Retriever RetTrain RetAug Stage Pre-/Post- Retrieval Generator Aug Assessment 2019 kNN-LM [62] 619 DR(GP) No Inf RA DT Output LG 2020 REALM [46] 1437 DR(BE,BT) 有 PT+FT / ET 输入 OpenQA(NQ, WQ, CT) 2020 RAG [74] 2125 DR(DPR) 有 FT / ED (BART) 输入 OpenQA, AQA, Jeopardy QG, FV 2021 FiD [54] 780 SR(BM25)/ DR(DPR) 无 FT / ED (T5/BART) 输入 OpenQA 2021 SE-FiD [68] 286 SE(Bing) 无 Inf RQG FiD 输入 WizInt、WoW 2021 FiD-KD [53] 190 DR(BE) 是 FT CR FiD 输入 OpenQA 2021 RETRO [6] 683 DR(BERT, DPR) 无 PT

### 段落 66 · Page 7

**EN**

/ ED Inter LM, OpenQA 2021 EPR [126] 384 DR(DPR) Yes Inf CR GPT-3,J,Neo, CODEX Demon UR 2022 OpenBook [70] 145 SE+SR No QE GOPHER LM Input QA, FV 2022 DSP [63] 117 ColBERTv2 No Inf RQG, RF GPT-3.5 Demon OpenQA, MHQA, CQA 2023 In-Context RALM [117] 211 DR/SR No Inf TRR GPT-2,J,Neo Input LM, OpenQA 2023 Atlas [55] 367 DR(OE) Yes PT+FT / ED Input OpenQA, FV, WoW, EL,SF, MMLU 2023 FLARE [57] 133 SR(BM25)/ SE(Bing) No Inf RQG GPT-3.5 Input MHQA, CR, LongQA, OS 2023 IRCoT [149] 114 SR(BM25) No Inf / GPT-3,Flan-T5 Input OpenQA 2023 Self-RAG [5] 85 DR(OE) No FT CM tunable LLM OpenQA, LongQA, FV, BG 2023 REPLUG [135] 48 DR(BE) Yes FT TRA GPT-2,3 Inppu

**中文**

/ ED Inter LM, OpenQA 2021 EPR [126] 384 DR(DPR) 有 Inf CR GPT-3,J,Neo, CODEX Demon UR 2022 OpenBook [70] 145 SE+SR 无 QE GOPHER LM 输入 QA, FV 2022 DSP [63] 117 ColBERTv2 无 Inf RQG, RF GPT-3.5 Demon OpenQA, MHQA, CQA 2023 In-Context RALM [117] 211 DR/SR No Inf TRR GPT-2,J,Neo 输入 LM, OpenQA 2023 Atlas [55] 367 DR(OE) 是 PT+FT / ED 输入 OpenQA, FV, WoW, EL,SF, MMLU 2023 FLARE [57] 133 SR(BM25)/ SE(Bing) 无 Inf RQG GPT-3.5 输入 MHQA、CR、LongQA、OS 2023 IRCoT [149] 114 SR(BM25) 无 Inf / GPT-3、Flan-T5 输入 OpenQA 2023 Self-RAG [5] 85 DR(OE) 无 FT CM 可调 LLM OpenQA、LongQA、FV、 BG 2023 REPLUG [135] 48 DR(BE) 有 FT TRA GPT-2,3 Inppu

### 段落 67 · Page 7

**EN**

t MMLU, OpenQA 2023 UDR [80] 42 DR(DPR) Yes FT CR GPT-Neo Demon 40 NLP tasks 2023 ITER- RETGEN [130] 40 DR(DPR) Yes FT RR InstructGPT, Llama-2 Input MHQA, FV, CR Table 1: Basic publication information and main technical designs of high-impact RAG and RA-LLM models.

**中文**

t MMLU, OpenQA 2023 UDR [80] 42 DR(DPR) 是 FT CR GPT-Neo Demon 40 NLP 任务 2023 ITER-RETGEN [130] 40 DR(DPR) 是 FT RR InstructGPT, Llama-2 输入 MHQA, FV, CR 表 1：高影响力 RAG 和 RA-LLM 的基本发表信息和主要技术设计模型。

### 段落 68 · Page 7

**EN**

1 information and has several versions differing in scale, from billion token-level [22, 39, 46, 62, 74, 117, 135, 168, 180] to trillion tokenlevel [6]. Domain-specific database is also used for downstream tasks. For example, for the code generation task, Zan et al . [185] collect API information and code files of public libraries to build their APIretriever database. In addition, Zhou et al [197] propose to use a documentation pool frequently updated with new content (newly released libraries) in their model.

**中文**

1 信息，并有几个不同规模的版本，从十亿代币级别 [22, 39, 46, 62, 74, 117, 135, 168, 180] 到万亿代币级别 [6]。特定于域的数据库也用于下游任务。例如，对于代码生成任务，Zan 等人。 [185]收集公共图书馆的API信息和代码文件，构建其APIretriever数据库。此外，Zhou 等人[197]建议在其模型中使用经常更新新内容（新发布的库）的文档池。

### 段落 69 · Page 7

**EN**

Applying Internet searching engine [95] such as Bing and Google avoids the maintenance of the search index and can access up-todate knowledge [68, 70]. Meanwhile, it provides a broader knowledge base than the closed-sourced database [ 5, 70]. It can also provide high-quality ranking after being tuned over decades of use. Internet search has been widely incorporated with black-box LLMs and shows effectiveness for different functions such as knowledge augmentation [70], fact-checking [100] and LLM agent enhancement [175].

**中文**

应用Bing和Google等互联网搜索引擎[95]避免了搜索索引的维护，并且可以获取最新的知识[68, 70]。同时，它提供了比闭源数据库更广泛的知识库[5, 70]。经过数十年的使用调整后，它还可以提供高质量的排名。互联网搜索已广泛与黑盒法学硕士结合起来，并显示出对不同功能的有效性，例如知识增强[70]、事实检查[100]和法学硕士代理增强[175]。

### 段落 70 · Page 7

**EN**

Compared to traditional RAG, Internet search has been leveraged more as the retriever in RA-LLMs owing to the extraordinary capability of LLMs to be the Reader to comprehend the searching results, i.e., the retrieved documents, as well as LLMs’ ability to use tools to process and analyze the them [98]. Existing studies [182] have shown that leveraging search engines (e.g., InstrucGPT) is particularly effective for LLMs on zero-shot knowledge-intensive tasks such as OpenQA and fact checking. 3.2 Generation The design of the generator heavily depends on the downstream tasks.

**中文**

与传统的 RAG 相比，由于法学硕士作为读者理解搜索结果（即检索到的文档）的非凡能力，以及法学硕士使用工具处理和分析它们的能力，互联网搜索在 RA-LLM 中被更多地利用作为检索器 [98]。现有研究 [182] 表明，利用搜索引擎（例如 InstrucGPT）对于法学硕士在零样本知识密集型任务（例如 OpenQA 和事实检查）上特别有效。 3.2 生成 生成器的设计在很大程度上取决于下游任务。

### 段落 71 · Page 7

**EN**

For most text generation tasks, Decoder-only and Encoder- Decoder are two dominant structures [ 194]. The recent development of commercial closed-sourced large foundation models makes black-box generation models mainstream in RA-LLMs. In this part, we will briefly review studies with these two types of generators: parameter-accessible (white-box) and parameter-inaccessible (black-box). 3.2.1 Parameter-Accessible Generators (White-box). The structure of Encoder-Decoder processes the input and the target independently with different sets of parameters, in which a cross-attention component is developed to connect input tokens to target tokens.

**中文**

对于大多数文本生成任务，仅解码器和编码器-解码器是两种主要结构[194]。最近商业闭源大型基础模型的发展使得黑盒生成模型成为 RA-LLM 的主流。在这一部分中，我们将简要回顾这两种类型的生成器的研究：参数可访问（白盒）和参数不可访问（黑盒）。 3.2.1 参数可访问的生成器（白盒）。编码器-解码器的结构使用不同的参数集独立地处理输入和目标，其中开发了交叉注意组件来将输入标记连接到目标标记。

### 段落 72 · Page 7

**EN**

Representative Encoder-Decoder models include T5 [116] and BART [73]. In comparison, Decoder-only models process inputs and targets after concatenation, which makes the representations of the two parts concurrently built layer-by-layer as they propagate up the network. These two types of generators are widely applied in existing RAG work. For example, RAG [74] and Re2G [44] employ BART; FID [54] and EMDR2 utilize T5. There are other models [6, 84] leveraging Transformer-based Encoder-Decoder architecture but with some customized design.

**中文**

代表性的编码器-解码器模型包括 T5 [116] 和 BART [73]。相比之下，仅解码器模型在连接后处理输入和目标，这使得两个部分的表示在网络上传播时同时逐层构建。这两类发电机在现有的RAG工作中得到了广泛的应用。例如，RAG[74]和Re2G[44]采用BART； FID [54] 和 EMDR2 使用 T5。还有其他模型 [6, 84] 利用基于 Transformer 的编码器-解码器架构，但具有一些定制设计。

### 段落 73 · Page 7

**EN**

Generators in RAG differ themselves from general ones by incorporating retrieved data to enhance the generation 7

**中文**

RAG 中的生成器与一般生成器不同，它结合检索到的数据来增强第 7 代生成器

### Page 8

### 段落 74 · Page 8

**EN**

Conference’17, July 2017, Washington, DC, USA Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li accuracy and relevance. Furthermore, white-box generators allow parameter optimization, which can be trained to adapt to different retrieval and augmentation approaches for a better performance of generation. 3.2.2 Parameter-Inaccessible Generators (Black-box).

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Wenqi Fan、Yujuan Ding、Liangbo Ning、Shijie Wang、Hengyun Li、Dawei Yin、Tat-Seng Chua 和 Qing Li 准确性和相关性。此外，白盒生成器允许参数优化，可以对其进行训练以适应不同的检索和增强方法，以获得更好的生成性能。 3.2.2 参数不可访问的生成器（黑盒）。

### 段落 75 · Page 8

**EN**

A certain proportion of LLMs are released without the disclosure of internal structures or the accessibility of parameters, especially those particularly large-scale ones such as GPT series [1], Codex [12] and Claude, which are called black-box generation models. These generators only allow the operations of feeding queries (input) and receiving responses (output) while not allowing the internal structure to be altered or parameters to be updated. From another perspective, LLMs, even those open for fine-tuning, are large in scale and difficult to tune for downstream domain-specific tasks with only a limited amount of data.

**中文**

一定比例的LLM是在不公开内部结构或参数可访问性的情况下发布的，特别是那些特别大规模的LLM如GPT系列[1]、Codex[12]和Claude，被称为黑盒生成模型。这些生成器仅允许提供查询（输入）和接收响应（输出）的操作，而不允许更改内部结构或更新参数。从另一个角度来看，LLM，即使是那些开放微调的，其规模也很大，并且很难利用有限的数据来调整下游特定领域的任务。

### 段落 76 · Page 8

**EN**

Black-box RA-LLMs, therefore, focus more on the retrieval and augmentation processes, trying to enhance the generator by augmenting the input (also called prompt in the context of LLMs) with better knowledge, guidance, or examples for the generation. For example, Rubin et al. [126] proposes to train a prompt retriever with the data labeled by language models themselves, which can be used to provide better examples for in-context learning, therefore enhancing the final generation performance. Xu et al.

**中文**

因此，黑盒 RA-LLM 更关注检索和增强过程，尝试通过使用更好的知识、指导或生成示例来增强输入（在 LLM 的背景下也称为提示）来增强生成器。例如，鲁宾等人。 [126]提出用语言模型本身标记的数据来训练提示检索器，这可以为上下文学习提供更好的例子，从而提高最终的生成性能。徐等人。

### 段落 77 · Page 8

**EN**

[168] propose to compress the retrieved documents before in-context integration, which can reduce the computational costs and also relieve the burden of LMs to identify relevant information in long retrieved documents. 3.3 Retrieval Integration for Generation Augmentation Augmentation describes the technical process that integrates retrieval and generation parts, which is the essential part of RA-LLMs. In this subsection, we introduce three main designs of augmentation, which are conducted at the input, output, and intermediate layers of generator respectively, as illustrated in Figure 3. 3.3.1 Input-Layer Integration.

**中文**

[168]建议在上下文集成之前压缩检索到的文档，这可以降低计算成本，也减轻语言模型在长检索文档中识别相关信息的负担。 3.3 生成增强的检索集成增强描述了集成检索和生成部分的技术流程，这是RA-LLM的重要组成部分。在本小节中，我们介绍三种主要的增强设计，分别在生成器的输入层、输出层和中间层进行，如图3所示。 3.3.1 输入层集成。

### 段落 78 · Page 8

**EN**

A common way to integrate retrieved information/documents is to combine them with the original input/query and jointly pass them to the generator, which is called input-layer integration. For example, In-Context RALM [117] applies input-layer integration by specifically concatenating the original input and all retrieved documents into a single sequence as the new input for the generation model. Despite the effectiveness, such integration is limited to the number of retrieved documents, since the concatenated new input may be too long to be processed by the generation model.

**中文**

集成检索到的信息/文档的常见方法是将它们与原始输入/查询相结合，并将它们共同传递给生成器，这称为输入层集成。例如，In-Context RALM [117] 通过将原始输入和所有检索到的文档专门连接成单个序列作为生成模型的新输入来应用输入层集成。尽管有效，但这种集成仅限于检索到的文档数量，因为连接的新输入可能太长而无法由生成模型处理。

### 段落 79 · Page 8

**EN**

In-context RALM specifically alleviates this limitation by removing tokens from the beginning of the new input. To avoid information loss with such a token removing strategy, FID [54] employs a different integration method that processes each retrieved document independently in the encoder. This strategy is scalable to a large number of contexts as it only performs selfattention over one context at a time in the follow-up processing. Atlas [55] and REPLUG [135] apply a similar parallel integration by concatenating the query and one retrieved document at a time.

**中文**

上下文中的 RALM 通过从新输入的开头删除标记来专门缓解此限制。为了避免这种标记删除策略造成的信息丢失，FID [54] 采用了不同的集成方法，在编码器中独立处理每个检索到的文档。该策略可扩展到大量上下文，因为它在后续处理中一次仅对一个上下文执行自注意力。 Atlas [55] 和 REPLUG [135] 通过一次连接查询和一个检索到的文档来应用类似的并行集成。

### 段落 80 · Page 8

**EN**

In general, most black-box generation-based RAG methods apply input-layer integration since neither the intermediate layer of the generation model or the output distribution is accessible. More specially for LLMs, input-layer integration may use the retrieved content as (additional) prompts or demonstrations on top of using it as supplementary to the original input as in traditional RAGs [126]. Prompt retrieval aims to find suitable natural language prompts automatically through retrieval to teach the LLM to learn in context [7] or to induce the LLM to reason[162].

**中文**

一般来说，大多数基于黑盒生成的 RAG 方法都应用输入层集成，因为生成模型的中间层或输出分布都不可访问。更特别的是，对于法学硕士来说，输入层集成除了像传统 RAG 中那样将其用作原始输入的补充之外，还可以使用检索到的内容作为（附加）提示或演示 [126]。提示检索旨在通过检索自动找到合适的自然语言提示，教法学硕士在上下文中学习[7]或诱导法学硕士推理[162]。

### 段落 81 · Page 8

**EN**

It may boost the zero-shot ability of LLMs without delicate prompt engineering. For example, Cheng et al. [16] propose to learn a prompt retriever based on the input-prompt pair data with score labels resulting from a frozen LLM. 3.3.2 Output-Layer Integration. Another kind of augmentation is post-hoc, i.e., output-layer integration, which joints retrieval and generation results. For example, kNN-LM [ 62] interpolates two next-token distributions in prediction: one induced by the LM and the other induced by the nearest neighbors from the retrieval corpus.

**中文**

它可以提高法学硕士的零样本能力，而无需精细的即时工程。例如，程等人。 [16]建议根据输入提示对数据学习提示检索器，该数据具有由冻结的 LLM 产生的分数标签。 3.3.2 输出层集成。另一种增强是事后增强，即输出层集成，它将检索和生成结果结合起来。例如，kNN-LM [62] 在预测中插入两个下一个标记分布：一个由 LM 诱导，另一个由检索语料库中的最近邻居诱导。

### 段落 82 · Page 8

**EN**

Output-layer linear integration [45, 196] is flexible to apply since it can be plugged into most generation models without additional training. However, the simplicity of output-layer integration also limits the model’s ability to reason about the retrieved text. To tackle this limitation, Yogatama et al. [180] propose to add an extra gating network to post-process the retrieved data and achieve comparatively better performance. For LLMs, output-layer integration is as reasonable and adaptive as input-layer integration.

**中文**

输出层线性积分[45, 196]应用起来很灵活，因为它可以插入大多数生成模型而无需额外的训练。然而，输出层集成的简单性也限制了模型推理检索到的文本的能力。为了解决这个限制，Yogatama 等人。 [180]建议添加一个额外的门控网络来对检索到的数据进行后处理并获得相对更好的性能。对于法学硕士来说，输出层集成与输入层集成一样合理且具有适应性。

### 段落 83 · Page 8

**EN**

REFEED [183] proposes an answer refining mechanism that applies an LLM to evaluate the retrieved information and adjust the initial answer accordingly to enhance the accuracy of the response. Similarly, Zhang et al. [190] propose the COMBO framework, which matches LLM-generated passages with retrieved counterparts into compatible pairs based on pre-trained discriminators. The passage pairs are then handled by a Fusion-in-Decoder-based [54] to derive a final answer. 3.3.3 Intermediate-Layer Integration.

**中文**

REFEED [183]提出了一种答案精炼机制，该机制应用法学硕士来评估检索到的信息并相应地调整初始答案以提高响应的准确性。同样，张等人。 [190]提出了 COMBO 框架，该框架根据预先训练的鉴别器将 LLM 生成的段落与检索到的对应段落匹配成兼容对。然后，基于 Fusion-in-Decoder 的 [54] 处理这些段落对，以得出最终答案。 3.3.3 中间层集成。

### 段落 84 · Page 8

**EN**

Compared to the above two non-parametric approaches, a more engaging augmentation is to design a semi-parametric module to integrate the retrieved results through the internal layers of the generation model, which is called intermediate-layer integration. Such integration might add additional complexity and is promising to enhance the capability of the generation model with effective training. Typically, a Transformer module is introduced to leverage retrieved information (mostly encoded into dense representations) into the generation model to interact with the representations in the middle stage of the generation.

**中文**

与上述两种非参数方法相比，更有吸引力的增强是设计一个半参数模块，通过生成模型的内部层集成检索结果，这称为中间层集成。这种集成可能会增加额外的复杂性，并有望通过有效的训练来增强生成模型的能力。通常，引入 Transformer 模块来将检索到的信息（主要编码为密集表示）引入到生成模型中，以便在生成的中间阶段与表示进行交互。

### 段落 85 · Page 8

**EN**

For example, RETRO [6] introduces a Chunked Cross Attention (CCA) layer to process the retrieved chunks in the generator blocks, and Wu et al. [165]introduces the kNN-Augmented Attention Layer. Similarly, EAE [39] and TOME [22] use Entity Memory and MemoryAttention layer to incorporate the retrieved Entity and Entity Mentions, respectively. Such intermediate-layer integration can use many blocks frequently and efficiently to enhance the capability of the whole RAG model.

**中文**

例如，RETRO [6] 引入了分块交叉注意（CCA）层来处理生成器块中检索到的块，Wu 等人。 [165]引入了 kNN 增强注意力层。类似地，EAE [39] 和 TOME [22] 使用 Entity Memory 和 MemoryAttention 层分别合并检索到的实体和实体提及。这种中间层集成可以频繁有效地使用许多块来增强整个RAG模型的能力。

### 段落 86 · Page 8

**EN**

It offers an efficient alternative to incorporate a large number of text chunks frequently retrieved, which are challenging to process with input-layer integration due to the input length limit of LMs [6]. However, it also needs to be noted that intermediate-layer integration requires high access to the generation models, which is not feasible for most LLMs that are accessible through inference APIs [98]. 8

**中文**

它提供了一种有效的替代方案来合并大量经常检索的文本块，由于语言模型 [6] 的输入长度限制，输入层集成处理这些文本块具有挑战性。然而，还需要注意的是，中间层集成需要对生成模型的高度访问，这对于大多数可通过推理 API 访问的法学硕士来说是不可行的[98]。 8

### Page 9

### 段落 87 · Page 9

**EN**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA 3.4 Retrieval Augmentation Necessity and Frequency The retrieval operation in LLM-based generation generally aims to supplement knowledge to enhance generation. Although retrievalaugmented models have emerged promising, they have been criticized for not being a universal solution [75, 109] as indiscriminately augmenting LLMs with irrelevant passages can override potentially correct knowledge already possessed by LLMs and result in incorrect responses instead [99]. Thakur et al.

**中文**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA 3.4 检索增强的必要性和频率 基于 LLM 的生成中的检索操作通常旨在补充知识以增强生成。尽管检索增强模型看起来很有希望，但它们被批评为不是通用的解决方案 [75, 109]，因为不加区别地用不相关的段落来增强 LLM 可能会覆盖 LLM 已经拥有的潜在正确知识，并导致错误的响应 [99]。塔库尔等人。

### 段落 88 · Page 9

**EN**

[147] contribute a human-annotated dataset to help evaluate the robustness of LLMs against errors in external retrieved knowledge and observe that LLMs may double the hallucination rate on the non-relevant retrieved passages than on the relevant ones. Therefore, it is critical for RA-LLMs to accurately recall the prior knowledge while selectively incorporating retrieved information only when necessary, which is the path to robust RA-LLMs. Most existing methods determine the necessity of retrieval based on the preliminary answers of LLMs or their internal reasoning results [102, 117].

**中文**

[147] 贡献了一个人工注释的数据集，以帮助评估法学硕士针对外部检索知识中的错误的鲁棒性，并观察到法学硕士对不相关检索段落的幻觉率可能是相关段落的两倍。因此，对于 RA-LLM 来说，准确回忆先验知识，同时仅在必要时选择性地合并检索到的信息至关重要，这是通往稳健的 RA-LLM 的道路。大多数现有方法根据法学硕士的初步答案或其内部推理结果来确定检索的必要性[102, 117]。

### 段落 89 · Page 9

**EN**

For example, Self-RAG [ 5] introduces special tokens to assess the necessity of retrieval and control retrieval behavior. Other methods design iterative prompts to decide if extra information is required during generation, which thereby needs to invoke retrieval or other actions for LLMs [162, 175]. Wang et al. [159] propose Self-Knowledge guided Retrieval augmentation (SKR) method, which uses LLMs themselves or explicit small trainable models to offer self-knowledge as the reference for the adaptive calling of a retriever.

**中文**

例如，Self-RAG [5]引入了特殊的标记来评估检索的必要性并控制检索行为。其他方法设计迭代提示来决定在生成过程中是否需要额外信息，从而需要调用 LLM 的检索或其他操作 [162, 175]。王等人。 [159]提出了自我知识引导检索增强（SKR）方法，该方法使用LLM本身或显式的小型可训练模型来提供自我知识作为检索器自适应调用的参考。

### 段落 90 · Page 9

**EN**

In traditional RAGs, retrieval necessity judgment has also been explored and proposed to address by intuitive approaches such as assessing the confidence of the logits produced by the generation models [47, 56, 59]. Such a solution is also applicable to RA-LLMs, for example, FLARE [57] dynamically triggers RAG if logits are lower than a specific threshold. Tan et al. [146] introduce a more flexible model SlimPLM, which detects missing knowledge in LLMs with a slim proxy model, which functions to generate a “heuristic answer”.

**中文**

在传统的 RAG 中，检索必要性判断也被探索并提出通过直观的方法来解决，例如评估生成模型产生的 logits 的置信度 [47,56,59]。这样的解决方案也适用于 RA-LLM，例如，如果 logits 低于特定阈值，FLARE [57] 就会动态触发 RAG。谭等人。 [146]引入了一种更灵活的模型SlimPLM，它通过一个瘦代理模型来检测法学硕士中缺失的知识，该模型的作用是生成“启发式答案”。

### 段落 91 · Page 9

**EN**

The “heuristic answer” is used to assess the necessity of retrieval and facilitate the retrieval process for query rewriting when necessary. In traditional RAGs that rarely consider retrieval necessity, retrieval frequency (also called retrieval stride) is an important design aspect to determine the degree of using the retrieval in the generation, thereby greatly affecting the overall performance of RAG models [117]. Retrieval frequency controls how much to rely on the retrieval results, thereby affecting both the efficiency and effectiveness of the model.

**中文**

“启发式答案”用于评估检索的必要性，并在必要时促进检索过程以进行查询重写。在很少考虑检索必要性的传统RAG中，检索频率（也称为检索步幅）是一个重要的设计方面，决定着生成中使用检索的程度，从而极大地影响RAG模型的整体性能[117]。检索频率控制着对检索结果的依赖程度，从而影响模型的效率和有效性。

### 段落 92 · Page 9

**EN**

When the necessity of retrieval is not considered, retrieval frequency is often pre-defined and fixed, which have three common settings: one-time, every-n-token, and every-token. Onetime retrieval invokes the retrieval function only once and tries to find all desired information in that one-time operation. One-time retrieval is usually operated at the beginning of the generation process, and then provides all retrieved documents to the generation models along with the original input, as applied in REALM [ 46]. One-time retrieval is more suitable for the cases that the information needs in external databases are obvious to LLMs [57].

**中文**

当不考虑检索的必要性时，检索频率往往是预先定义和固定的，常见的设置有一次性、每n个令牌和每个令牌三种。一次性检索仅调用检索函数一次，并尝试在该一次性操作中查找所有所需信息。一次性检索通常在生成过程开始时进行，然后将所有检索到的文档与原始输入一起提供给生成模型，如 REALM [46] 中所应用的那样。一次性检索更适合LLMs明显需要外部数据库中的信息的情况[57]。

### 段落 93 · Page 9

**EN**

However, for language tasks requiring long-form output such as open-domain summarization, the dependency among the tokens in the output is more important to be considered during the generation. In these cases, pre-retrieved documents (through one-time retrieval) might not be enough to support the generation of the whole sequence of output, which calls for in-generation retrieval operations. To this end, In-Context RALM [117] and RETRO [6] apply every-n-token retrieval in the process of generation for better augmentation.

**中文**

然而，对于需要长格式输出的语言任务（例如开放域摘要），在生成过程中更需要考虑输出中标记之间的依赖性。在这些情况下，预先检索的文档（通过一次性检索）可能不足以支持整个输出序列的生成，这需要生成内检索操作。为此，In-Context RALM [117] 和 RETRO [6] 在生成过程中应用 every-n-token 检索，以实现更好的增强。

### 段落 94 · Page 9

**EN**

In comparison, kNN-LM [62] adopts a more frequent retrieval strategy, which retrieves information for the prediction of every token during the generation. Overall, applying different frequencies of retrieval can impact both the effectiveness and efficiency of the whole RAG method. For example, more frequent retrieval leads to better performance but also increases the computing cost [117]. Choosing retrieval frequency is almost a trade-off between computing cost and performance.

**中文**

相比之下，kNN-LM[62]采用了更频繁的检索策略，在生成过程中检索每个标记的预测信息。总体而言，应用不同的检索频率会影响整个 RAG 方法的有效性和效率。例如，更频繁的检索会带来更好的性能，但也会增加计算成本[117]。选择检索频率几乎是计算成本和性能之间的权衡。

### 段落 95 · Page 9

**EN**

4 RA-LLMS TRAINING Based on whether training is required or not, existing RAG methods can be categorized into two main classes: train-free approaches and training-based approaches. Training-free methods usually directly leverage the retrieved knowledge during inference time without introducing extra training by inserting the retrieved text into the prompt, which is computationally efficient. However, one potential challenge is that the retriever and generator components are not specifically optimized for downstream tasks, which could easily lead to sub-optimal utilization of the retrieved knowledge.

**中文**

4 RA-LLMS 训练 根据是否需要训练，现有的RAG 方法可以分为两大类：免训练方法和基于训练的方法。免训练方法通常在推理期间直接利用检索到的知识，而无需通过将检索到的文本插入到提示中来引入额外的训练，这在计算上是高效的。然而，一个潜在的挑战是检索器和生成器组件没有专门针对下游任务进行优化，这很容易导致检索到的知识的利用率不高。

### 段落 96 · Page 9

**EN**

To fully exploit the external knowledge, extensive methods are proposed to fine-tune the retriever and generator, thereby guiding large language models to effectively adapt and integrate retrieved information [127, 128, 130, 135, 153, 199].

**中文**

为了充分利用外部知识，人们提出了广泛的方法来微调检索器和生成器，从而指导大型语言模型有效地适应和集成检索到的信息[127,128,130,135,153,199]。

### 段落 97 · Page 9

**EN**

According to the training strategies, we categorize these trainingbased approaches into three classes: 1) Independent Training approaches independently train each component in the RAG procedure, 2) Sequential Training methods train one module first and freeze the well-trained component to guide the tuning process of the other part, and 3) Joint Training approaches train retriever and generator simultaneously. In the following section, we will comprehensively review the training-free, independent training, sequential training, and joint training methods. The comparison of these different training methods is depicted in Figure 5.

**中文**

根据训练策略，我们将这些基于训练的方法分为三类：1）独立训练方法独立训练RAG过程中的每个组件，2）顺序训练方法首先训练一个模块，然后冻结训练有素的组件以指导另一部分的调整过程，3）联合训练方法同时训练检索器和生成器。在下面的部分中，我们将全面回顾免训练、独立训练、顺序训练和联合训练方法。这些不同训练方法的比较如图 5 所示。

### 段落 98 · Page 9

**EN**

4.1 Training-free With the huge number of parameters, LLMs have exhibited humanlevel intelligence and achieved promising prediction performance on various downstream tasks. However, it is extremely challenging to frequently perform fine-tuning and update the knowledge stored in the model parameters [ 74] due to the considerable time and computational resources required.

**中文**

4.1 免训练 凭借大量的参数，法学硕士展现出了人类水平的智能，并在各种下游任务上取得了有希望的预测性能。然而，由于需要大量的时间和计算资源，频繁地执行微调和更新模型参数中存储的知识[74]极具挑战性。

### 段落 99 · Page 9

**EN**

Recently, numerous studies have suggested enhancing LLMs with retrieval mechanisms, enabling them to dynamically acquire new knowledge from external sources without extra training processes (i.e., training-free) [54, 57, 63], instead of relying solely on the implicit knowledge encoded in the model’s parameters. These approaches have shown significant performance improvement for various knowledge-intensive tasks, such as open-domain question answering [74].

**中文**

最近，大量研究建议通过检索机制增强法学硕士，使他们能够从外部来源动态获取新知识，而无需额外的训练过程（即免训练）[54,57,63]，而不是仅仅依赖于模型参数中编码的隐式知识。这些方法已经显示出各种知识密集型任务的显着性能改进，例如开放域问答[74]。

### 段落 100 · Page 9

**EN**

According to the different ways in which LLMs utilize retrieved information, we categorize these training-free methods into two categories: 1)Prompt Engineering-based Methods integrate retrieved knowledge into 9

**中文**

根据法学硕士利用检索到的信息的不同方式，我们将这些免训练的方法分为两类：1）基于工程的快速方法将检索到的知识整合为 9 种方法。

### Page 10

### 段落 101 · Page 10

**EN**

Conference’17, July 2017, Washington, DC, USA Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li Retriever Datastore Input Output Datastore Retriever Input Output Retriever Datastore Input Output Retriever Datastore Input Output Retriever Datastore Input Output Retriever Datastore Input Output 1. Independent Training of Retriever 2. Independent Training of LLMs Independent Training Training-Free Joint Training Sequential Training 1. Retriever First 2.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Wenqi Fan、Yujuan Ding、Liangbo Ning、Shijie Wang、Hengyun Li、Dawei Yin、Tat-Seng Chua 和 Qing Li 检索器数据存储输入输出数据存储检索器输入输出检索器数据存储输入输出检索器数据存储输入输出检索器数据存储输入输出检索器数据存储输入输出1. 检索器的独立培训2. 法学硕士的独立培训独立训练 自由训练 联合训练 顺序训练 1. 猎犬优先 2.

### 段落 102 · Page 10

**EN**

LLMs First Forward Backward Retrieved Documents Trainable Frozen Large Language Models Large Language Models Large Language Models Large Language Models Large Language Models Large Language Models Figure 5: An illustration of different training methods in Retrieval-Augmented Large Language Models (RA-LLMs). Existing RA- LLMs approaches can be categorized into two classes: training-free approaches usually directly leverage retrieved information during the inference time by integrating the retrieved knowledge into the prompt, and training-based approaches fine-tune the retrieval and generator to enhance the generation performance.

**中文**

LLM 首次向前向后检索文档 可训练 冻结 大语言模型 大型语言模型 大型语言模型 大型语言模型 大型语言模型 大型语言模型 图 5：检索增强大型语言模型 (RA-LLM) 中不同训练方法的图示。现有的 RA-LLM 方法可以分为两类：免训练方法通常通过将检索到的知识集成到提示中来直接利用推理时间内检索到的信息，而基于训练的方法则微调检索和生成器以提高生成性能。

### 段落 103 · Page 10

**EN**

Based on the training strategies, training-based methods can be further categorized into three groups: independent training, where the retrieval and generator components are trained independently; sequential training, where they are trained sequentially; and joint training, where they are trained jointly. the original prompt directly, and 2)Retrieval-Guided Token Generation Methods retrieve information to calibrate the token generation process. 4.1.1 Prompt Engineering-based Methods.

**中文**

根据训练策略，基于训练的方法可以进一步分为三类：独立训练，其中检索和生成组件独立训练；顺序训练，按顺序进行训练；联合训练，他们接受联合训练。直接原始提示，以及2）检索引导的令牌生成方法检索信息以校准令牌生成过程。 4.1.1 及时的基于工程的方法。

### 段落 104 · Page 10

**EN**

As the LLMs’ generation performance highly depends on the input query, numerous trainingfree RAG approaches employ external knowledge by refining the original prompts [57, 63, 81]. Specifically, the retrieved texts are usually used as contextual information and combined with the original prompt to guide the generation of LLMs [54, 57, 63, 65, 81, 112, 158]. For example, In-Context RALM [117] keeps the LLM parameters unchanged and directly incorporates the retrieved document before the original prompt to augment the generation process.

**中文**

由于 LLM 的生成性能高度依赖于输入查询，因此许多免训练 RAG 方法通过细化原始提示来利用外部知识 [57,63,81]。具体来说，检索到的文本通常用作上下文信息，并与原始提示相结合来指导LLM的生成[54,57,63,65,81,112,158]。例如，In-Context RALM [117]保持LLM参数不变，并在原始提示之前直接合并检索到的文档以增强生成过程。

### 段落 105 · Page 10

**EN**

IRCoT [149] interleaves chain-of-thought (CoT) generation and knowledge retrieval steps, enabling the retrieval of more relevant information for subsequent reasoning steps compared to standard retrieval methods that rely solely on the question as the query. Instead of retrieving knowledge from a large corpus, GENREAD [182] first prompts a LLM to generate contextual documents based on the query, and then generate answers based on the given context and question.

**中文**

IRCoT [149] 交织思想链（CoT）生成和知识检索步骤，与仅依赖问题作为查询的标准检索方法相比，能够为后续推理步骤检索更多相关信息。 GENREAD [182] 不是从大型语料库中检索知识，而是首先提示法学硕士根据查询生成上下文文档，然后根据给定的上下文和问题生成答案。

### 段落 106 · Page 10

**EN**

SKR [159] proposes guiding LLMs to determine whether they can answer a given question based on their internal knowledge, enabling flexible utilization of both internal and external knowledge by selectively calling the retriever. TOC [65] first retrieves relevant knowledge for ambiguous questions and recursively constructs a tree structure by clarifying ambiguous questions into multiple disambiguate questions, which is further aggregated to generate long-form answers. 4.1.2 Retrieval-Guided Token Generation Methods.

**中文**

SKR[159]建议指导法学硕士根据其内部知识确定是否可以回答给定的问题，通过有选择地调用检索器来灵活利用内部和外部知识。 TOC[65]首先检索歧义问题的相关知识，并通过将歧义问题澄清为多个消歧问题来递归地构建树结构，进一步聚合以生成长格式答案。 4.1.2 检索引导的令牌生成方法。

### 段落 107 · Page 10

**EN**

In addition to directly integrating external knowledge into the original prompt, the auxiliary information can be employed to adjust the token generation process. For example, KNN-KMs [62] first retrieves 𝑘 most relevant contexts from the datastore based on the given query, and computes a neighbor distribution based on the distance. The output distribution is calibrated by interpolating the neighbor distribution and the original model’s output distribution.

**中文**

除了将外部知识直接融入到原始提示中之外，还可以利用辅助信息来调整令牌生成过程。例如，KNN-KMs [62] 首先根据给定的查询从数据存储中检索最相关的上下文，并根据距离计算邻居分布。通过对邻近分布和原始模型的输出分布进行插值来校准输出分布。

### 段落 108 · Page 10

**EN**

Rest [49] is proposed to replace the parametric draft model with a non-parametric retrieval datastore and retrieves relevant tokens based on the current context for speculative decoding [9, 71, 145]. 10

**中文**

Rest [49]建议用非参数检索数据存储替换参数草稿模型，并根据当前上下文检索相关标记以进行推测解码[9,71,145]。 10

### Page 11

### 段落 109 · Page 11

**EN**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA 4.2 Independent Training Independent training refers to training the retriever and LLMs as two entirely independent processes, in which there is no interaction between the retriever and the LLMs during the training process [61, 69, 197]. Compared with training-free methods, the performance of the RAG-empowered models can be effectively enhanced by training LLMs to leverage the retrieved knowledge or retrievers to bridge the gap between information retrieval and language generation.

**中文**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA 4.2 独立训练 独立训练是指将检索器和法学硕士作为两个完全独立的过程进行训练，在训练过程中检索器和法学硕士之间没有交互[61,69,197]。与免训练方法相比，通过训练法学硕士利用检索到的知识或检索器来弥合信息检索和语言生成之间的差距，可以有效提高 RAG 授权模型的性能。

### 段落 110 · Page 11

**EN**

For the training of LLMs, the negative loglikelihood loss is the most representative training objective [115, 148], which aims to guide the LLMs to generate desired output based on the given input. Regarding the retriever, it can be categorized into two types: 1) Sparse retriever [120, 125], and 2) Dense retriever [61, 69, 197]. The sparse retrievers usually exploit sparse features, e.g., word frequencies, to represent the documents and calculate the relevance scores based on task-specific metrics [77, 120, 125] such as TF-IDF and BM25.

**中文**

对于LLM的训练，负对数似然损失是最具代表性的训练目标[115, 148]，其目的是指导LLM根据给定的输入生成期望的输出。关于检索器，可以分为两种类型：1）稀疏检索器[120,125]和2）密集检索器[61,69,197]。稀疏检索器通常利用稀疏特征（例如词频）来表示文档，并根据特定于任务的指标 [77,120,125]（例如 TF-IDF 和 BM25）计算相关性得分。

### 段落 111 · Page 11

**EN**

As for the dense retrievers, deep neural networks are employed to encode the query and documents into dense representations, and then the inner product is usually used to calculate relevance scores and retrieve the relevant external knowledge. For example, DPR [61] adopts two independent BERT [25] networks to encode the query and passages respectively, and trains these models by utilizing contrastive learning. CoG [69] proposes to train a prefix encoder and a phrase encoder for retrieval and reformulate the text generation as multiple copy-and-paste operations from existing source text collection.

**中文**

对于密集检索器，采用深度神经网络将查询和文档编码为密集表示，然后通常使用内积来计算相关性分数并检索相关的外部知识。例如，DPR[61]采用两个独立的BERT[25]网络分别对查询和段落进行编码，并利用对比学习来训练这些模型。 CoG [69]建议训练一个前缀编码器和一个短语编码器用于检索，并将文本生成重新表述为来自现有源文本集合的多个复制和粘贴操作。

### 段落 112 · Page 11

**EN**

4.3 Sequential Training Independent training is an efficient approach to exploit the external knowledge during the generation process since the retriever and generator can be trained offline and any off-the-shelf models can be utilized, avoiding extra training costs. To better enhance the synergy between the retriever and generator, several methods have been proposed to train the retriever and LLMs sequentially. In these sequential training methods, the process typically begins with the independent pre-training of either the retriever or the generator, after which the pre-trained module is fixed while the other module undergoes training.

**中文**

4.3 顺序训练独立训练是在生成过程中利用外部知识的有效方法，因为检索器和生成器可以离线训练，并且可以使用任何现成的模型，从而避免额外的训练成本。为了更好地增强检索器和生成器之间的协同作用，人们提出了几种方法来顺序训练检索器和 LLM。在这些顺序训练方法中，该过程通常从检索器或生成器的独立预训练开始，之后固定预训练模块，同时另一个模块接受训练。

### 段落 113 · Page 11

**EN**

Note that various existing models (e.g., BERT [25, 64, 123], CLIP [113], T5 [116]) can be directly employed as the fixed retriever and generator, thereby bypassing the first pertaining process. Compared to independent training, sequential training involves coordinated training of the retriever and generator, where the trainable module benefits from the assistance of the fixed module. Based on the training order between the retriever and generator, sequential training can be categorized into two classes: 1) Retriever First [5, 127, 128, 153, 199], and 2) LLMs First [130, 135, 157]. 4.3.1 Retriever First.

**中文**

请注意，各种现有模型（例如，BERT [25,64,123]，CLIP [113]，T5 [116]）可以直接用作固定检索器和生成器，从而绕过第一个相关过程。与独立训练相比，顺序训练涉及检索器和生成器的协调训练，其中可训练模块受益于固定模块的协助。根据检索器和生成器之间的训练顺序，顺序训练可以分为两类：1）检索器优先[5,127,128,153,199]和2）LLM优先[130,135,157]。 4.3.1 检索器优先。

### 段落 114 · Page 11

**EN**

These methods first train the retrieval model and then fix it. LLMs are then trained by utilizing the retrieved knowledge. For instance, RETRO [6] adopts the BERT model that is pre-trained independently as the retriever, and an encoder-decoder architecture is trained to integrate retrieval chunks into the model’s predictions. RALMs [ 181] adopts Google Search and the opensource COLBERTV2 [ 64] as the pre-trained retriever and finetunes the LLM to effectively leverage the retrieved passages.

**中文**

这些方法首先训练检索模型，然后修复它。然后利用检索到的知识对法学硕士进行培训。例如，RETRO[6]采用独立预训练的BERT模型作为检索器，并训练编码器-解码器架构以将检索块集成到模型的预测中。 RALMs [181] 采用 Google 搜索和开源 COLBERTV2 [64] 作为预训练的检索器，并对 LLM 进行微调以有效地利用检索到的段落。

### 段落 115 · Page 11

**EN**

ITER- RTGEN [124] utilizes the pre-trained S-BERT [123] as the retriever and introduces an adaptive hybrid retrieval strategy for retrieving demonstrations. Additionally, it leverages T5 [116] as the generator, which undergoes further fine-tuning based on the target label and input combining the original prompt with retrieved demonstrations. SMALLCAP [121] proposes using the CLIP [113], which is a powerful pre-trained multi-modal network, to encode the input image and the textual data of the external datastore and retrieve the most relevant items based on the cosine similarity.

**中文**

ITER-RTGEN [124] 利用预先训练的 S-BERT [123] 作为检索器，并引入自适应混合检索策略来检索演示。此外，它利用 T5 [116] 作为生成器，根据目标标签和输入结合原始提示与检索到的演示进行进一步的微调。 SMALLCAP [121] 提出使用 CLIP [113]（一种强大的预训练多模态网络）对输入图像和外部数据存储的文本数据进行编码，并根据余弦相似度检索最相关的项目。

### 段落 116 · Page 11

**EN**

A cross-attention layer is trained and GPT-2 [115] is used as the decoder to produce captions. 4.3.2 LLMs First. Similarly, it can also pre-train LLMs first, and then tune the retriever under the supervision of the well-trained LLMs. For example, DKRR [53] shows that attention scores from a sequence-to-sequence model can indicate the document’s relevance. Therefore, they propose to leverage the attention scores of a reader model to produce synthetic labels to train the retriever. AAR [184] proposes using a small language model to generate the supervised signal for training retrievers.

**中文**

训练交叉注意力层并使用 GPT-2 [115] 作为解码器来生成字幕。 4.3.2 法学硕士优先。同样，它也可以先预训练 LLM，然后在训练有素的 LLM 的监督下调整检索器。例如，DKRR [53]表明序列到序列模型的注意力分数可以表明文档的相关性。因此，他们建议利用读者模型的注意力分数来生成合成标签来训练检索器。 AAR [184]建议使用小型语言模型来生成用于训练检索器的监督信号。

### 段落 117 · Page 11

**EN**

The well-trained retriever can be further leveraged to enhance the performance of black-box LLMs. RA-DIT [86] first fine-tunes the LLMs to enhance their ability to leverage retrieved knowledge, and then train the retriever to better align its output with LLMs. UPRISE [ 16] proposes a lightweight method to enhance the zero-shot performance of LLMs in unseen tasks by introducing a prompt retriever. A frozen LLM is employed to guide the fine-tuning process of the prompt retriever, and this retriever then retrieves prompts for different tasks with various LLMs during inference.

**中文**

训练有素的检索器可以进一步利用来提高黑盒法学硕士的性能。 RA-DIT [86] 首先对 LLM 进行微调，以增强其利用检索到的知识的能力，然后训练检索器以更好地使其输出与 LLM 保持一致。 UPRISE [16] 提出了一种轻量级方法，通过引入提示检索器来增强 LLM 在未见过的任务中的零样本性能。采用冻结的 LLM 来指导提示检索器的微调过程，然后该检索器在推理过程中使用各种 LLM 检索不同任务的提示。

### 段落 118 · Page 11

**EN**

4.4 Joint Training Joint training methods [17, 51, 60, 79, 167, 196] employ the end-toend paradigm to optimize the retriever and generator simultaneously. Instead of training each module sequentially, joint training methods effectively enhance the retriever’s ability to locate external knowledge for generation and the generator’s capacity to effectively leverage the retrieved information. For instance, RAG [74] minimizes the negative loglikelihood to jointly train the retriever and generator.

**中文**

4.4 联合训练联合训练方法[17,51,60,79,167,196]采用端到端范式来同时优化检索器和生成器。联合训练方法不是按顺序训练每个模块，而是有效增强检索器定位外部知识以进行生成的能力以及生成器有效利用检索到的信息的能力。例如，RAG [74] 最小化负对数似然来联合训练检索器和生成器。

### 段落 119 · Page 11

**EN**

REALM [46] adopts a similar training paradigm to that of RAG [74], and Maximum Inner Product Search (MIPS) [15, 29, 119, 131] technique is used to locate the most relevant documents. To employ MIPS, all external documents are embedded first and a search index is produced for each embedding. An asynchronous index updating strategy [46, 52, 55, 141] is proposed to refresh the index every several hundred training steps to avoid time consumption of re-indexing all documents. 5 APPLICATIONS In this section, we will introduce some representative applications of retrieval-augmented large language models (RA-LLMs).

**中文**

REALM [46]采用与RAG [74]类似的训练范式，并使用最大内积搜索（MIPS）[15,29,119,131]技术来定位最相关的文档。为了使用 MIPS，首先嵌入所有外部文档，并为每个嵌入生成搜索索引。提出了一种异步索引更新策略[46,52,55,141]，每几百个训练步骤刷新一次索引，以避免重新索引所有文档的时间消耗。 5 应用在本节中，我们将介绍检索增强大语言模型（RA-LLM）的一些代表性应用。

### 段落 120 · Page 11

**EN**

To provide a clear overview of the applications of RA-LLMs, we will review them from three perspectives: NLP applications, downstream tasks, and domain-specific applications . The studies mentioned in this section are summarized and categorized in Figure 6. 11

**中文**

为了清楚地概述 RA-LLM 的应用，我们将从三个角度对其进行回顾：NLP 应用、下游任务和特定领域应用。本节提到的研究在图 6 中进行了总结和分类。 11

### Page 12

### 段落 121 · Page 12

**EN**

Conference’17, July 2017, Washington, DC, USA Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li Applications NLP Applications QA Systems ChatBots Fact Verification Downstream Tasks Recommendations Software Engineering Domain-specific Applications AI for Science Finance RETRO [6] Fusion-in-Decoder [54] REALM [46], etc. Ghazvininejad et al . [43] KDBTS [14] Komeili et al. [68] Wang et al. [152], etc. RAG [74] Atlas [55] Self-RAG [5], etc. Di Palma [26] CoRAL [163] RevCore [94], etc. Clinfo. ai [92] RetMol [160] MoleculeSTM [90] PMINet [174] BioBridge [161] RSA [97] Graphvf [144], etc.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Wenqi Fan、Yujuan Ding、Liangbo Ning、Shijie Wang、Hengyun Li、Dawei Yin、Tat-Seng Chua 和 Qing Li 应用 NLP 应用 QA 系统 ChatBots 事实验证下游任务推荐 软件工程领域特定应用 AI for Science Finance RETRO [6] Fusion-in-Decoder [54] REALM [46] 等。加兹维内贾德等人。 [43] KDBTS [14] Komeili 等人。 [68] 王等人。 [152] 等 RAG [74] Atlas [55] Self-RAG [5] 等 Di Palma [26] CoRAL [163] RevCore [94] 等 Clinfo。 ai [92] RetMol [160] MoleculeSTM [90] PMINet [174] BioBridge [161] RSA [97] Graphvf [144] 等

### 段落 122 · Page 12

**EN**

Docprompting [197] Atlas [105] Dater [177] SheetCopilo [76] Xricl [134] Synchromesh [111], etc. Zhang et al. [187] AlphaFin [78] ChatDOC [85] Yepes et al. [178], etc. Figure 6: A summary of applications of RA-LLMs categorized by NLP applications, downstream tasks, and domain-specific application. Specifically, NLP applications include QA systems, ChatBots, and fact verification; downstream tasks include recommendations and software engineering; and domain-specific applications include AI for Science and Finance.

**中文**

Docprompting [197] Atlas [105] Dater [177] SheetCpilo [76] Xricl [134] Synchromesh [111] 等。 [187] AlphaFin [78] ChatDOC [85] Yepes 等人。 [178]等。图6：按NLP应用、下游任务和特定领域应用分类的RA-LLM应用摘要。具体来说，NLP应用包括QA系统、ChatBots和事实验证；下游任务包括建议和软件工程；特定领域的应用包括科学和金融人工智能。

### 段落 123 · Page 12

**EN**

5.1 NLP Applications Due to the intrinsic capability in text generation, RA-LLMs have various applications in the NLP field, such as Question Answer (QA) Systems, ChatBot, and Fact Verification. 5.1.1 QA Systems. QA Systems aim to provide precise answers to user’s queries. However, even when trained on extensive data, these systems may lack the latest information or specific domain knowledge that is not included in their training data [54, 91].

**中文**

5.1 NLP 应用 由于文本生成的内在能力，RA-LLM 在 NLP 领域有各种应用，例如问答（QA）系统、ChatBot 和事实验证。 5.1.1 质量保证系统。 QA 系统旨在为用户的查询提供准确的答案。然而，即使在大量数据上进行训练，这些系统也可能缺乏训练数据中未包含的最新信息或特定领域知识 [54, 91]。

### 段落 124 · Page 12

**EN**

To address this limitation, the integration of RA-LLMs has played a crucial role in advancing the capabilities of QA systems by enhancing their ability to retrieve and synthesize relevant information [6, 54]. Specifically, RA-LLMs can provide coherent and contextually relevant answers by leveraging their retrieval component to access a vast knowledge base. For example, REALM [46] integrates a knowledge retriever that can retrieve information from a large corpus during pre-training, fine-tuning, and inference. This approach allows REALM to effectively retrieve from a vast knowledge corpus, thereby improving the accuracy of its responses.

**中文**

为了解决这一限制，RA-LLM 的集成通过增强 QA 系统检索和综合相关信息的能力，在提高 QA 系统的能力方面发挥了至关重要的作用 [6, 54]。具体来说，RA-LLM 可以利用其检索组件访问庞大的知识库，提供连贯且上下文相关的答案。例如，REALM [46]集成了一个知识检索器，可以在预训练、微调和推理过程中从大型语料库中检索信息。这种方法使 REALM 能够有效地从庞大的知识库中检索，从而提高其响应的准确性。

### 段落 125 · Page 12

**EN**

Similarly, Fusionin-Decoder [54] retrieves passages from support documents and then fuses them with questions to generate the answer, achieving higher accuracy. In addition, Borgeaud et al. [6] indicate that the quality of the answers may rely more on the output of retrieval. 5.1.2 ChatBot. ChatBot is designed to interact with users in a natural and conversational manner [ 87]. Different from the QA system, ChatBot focuses on maintaining a coherent and contextually rich conversation with the user.

**中文**

类似地，Fusionin-Decoder [54] 从支持文档中检索段落，然后将它们与问题融合以生成答案，从而实现更高的准确性。此外，Borgeaud 等人。 [6]表明答案的质量可能更多地依赖于检索的输出。 5.1.2 聊天机器人。 ChatBot 旨在以自然的对话方式与用户交互[87]。与 QA 系统不同，ChatBot 专注于与用户保持连贯且上下文丰富的对话。

### 段落 126 · Page 12

**EN**

To enhance these capabilities, recent methods focus on integrating RA-LLMs [60, 68, 188] for its ability to augment the ChatBot with relevant external knowledge, facilitating more engaging and context-rich interactions with users. For example, some studies [ 14, 43] retrieve relevant knowledge from static databases (e.g., a Wikipedia dump) to augment conversation. Komeili et al. [68] propose retrieving information from the internet search to further augment conversation performance.

**中文**

为了增强这些功能，最近的方法侧重于集成 RA-LLM [60,68,188]，因为它能够利用相关的外部知识增强 ChatBot，从而促进与用户更具吸引力和上下文丰富的交互。例如，一些研究 [14, 43] 从静态数据库（例如维基百科转储）中检索相关知识以增强对话。科梅利等人。 [68]建议从互联网搜索中检索信息以进一步增强对话性能。

### 段落 127 · Page 12

**EN**

Considering the dynamic nature of knowledge in the world, another model [152] further accesses large amounts of dynamic information in search engines to generate responses. 5.1.3 Fact Verification. Fact Verification is a critical task in verifying the accuracy and reliability of information. With the need for trusted evidence, RA-LLMs are being utilized to enhance the capabilities of fact verification [ 55, 74, 74]. Lewis et al . [74] first propose retrieval of external knowledge to augment a range of knowledge-intensive tasks including fact verification.

**中文**

考虑到世界上知识的动态性质，另一个模型[152]进一步访问搜索引擎中的大量动态信息以生成响应。 5.1.3 事实核查。事实验证是验证信息准确性和可靠性的关键任务。由于需要可信证据，RA-LLM 被用来增强事实验证的能力 [55,74,74]。刘易斯等人。 [74]首先提出检索外部知识来增强一系列知识密集型任务，包括事实验证。

### 段落 128 · Page 12

**EN**

On the other hand, Atlas [55] examines the performance of the RA-LLMs for fact verification under few-shot learning. Recently, Self-RAG [5] has greatly made a notable impression by incorporating a self-reflective mechanism. Specifically, Self-RAG reflects on whether retrieved information is helpful and judges the reliability of retrieved information, thereby greatly improving the verification accuracy. 5.2 Downstream Tasks In addition to NLP applications, RA-LLMs can also be applied to various downstream tasks, such as recommendations and software engineering. 5.2.1 Recommendations.

**中文**

另一方面，Atlas [55] 检查了 RA-LLM 在小样本学习下进行事实验证的性能。最近，Self-RAG [5] 通过结合自我反思机制给人留下了深刻的印象。具体来说，Self-RAG会反思检索到的信息是否有帮助，并判断检索到的信息的可靠性，从而大大提高了验证的准确性。 5.2 下游任务 除了NLP应用之外，RA-LLM还可以应用于各种下游任务，例如推荐和软件工程。 5.2.1 建议。

### 段落 129 · Page 12

**EN**

Recommender systems play an important role in modeling users’ preferences and providing personalized recommendations [34–36, 154, 189, 195]. Recently, RA-LLMs have demonstrated great potential in providing personalized and contextually relevant recommendations by integrating retrieval and generation processes [26, 94, 163]. For example, Di Palma [26] proposes a simple retrieval-augmented recommendation model, that leverages knowledge from movie or book datasets to enhance recommendations. Additionally, Lu et al. [94] further retrieval from the reviews to enrich item information in recommender systems. 12

**中文**

推荐系统在建模用户偏好和提供个性化推荐方面发挥着重要作用[34-36,154,189,195]。最近，RA-LLM 在通过集成检索和生成过程来提供个性化和上下文相关的推荐方面表现出了巨大的潜力 [26,94,163]。例如，Di Palma [26] 提出了一种简单的检索增强推荐模型，该模型利用电影或书籍数据集中的知识来增强推荐。此外，Lu 等人。 [94]进一步从评论中检索以丰富推荐系统中的项目信息。 12

### Page 13

### 段落 130 · Page 13

**EN**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA CoRAL [163] utilizes reinforcement learning to retrieve collaborative information from the dataset and align it with semantic information for more accurate recommendations. 5.2.2 Software Engineering. The rise of RA-LLMs has influenced many aspects of software engineering [105, 177, 197]. For example, some studies propose the retrieval-augmented generation paradigm for code generation [ 197] and program repair [ 105]. Similarly, Parvez et al.

**中文**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA CoRAL [163] 利用强化学习从数据集中检索协作信息，并将其与语义信息对齐，以获得更准确的推荐。 5.2.2 软件工程。 RA-LLM 的兴起影响了软件工程的许多方面 [105, 177, 197]。例如，一些研究提出了用于代码生成[197]和程序修复[105]的检索增强生成范式。同样，Parvez 等人。

### 段落 131 · Page 13

**EN**

[108] retrieve top-ranked codes or summaries from the codebase and aggregate them with input to enhance code generation and summarization. In addition, RA-LLMs show potential in tabular data processing [76, 177] and Text-to-SQL semantic parsing [111, 134]. 5.3 Domain-specific Applications RA-LLMs have been widely adopted for various domain-specific tasks, such as AI for Science and Finance. 5.3.1 AI for Science. RA-LLMs have proven to be beneficial for the realms of science, such as molecular and protein. Molecules include identifying the molecule’s property and predicting new molecules, thereby favoring drug discovery.

**中文**

[108]从代码库中检索排名最高的代码或摘要，并将它们与输入聚合以增强代码生成和摘要。此外，RA-LLM 在表格数据处理 [76, 177] 和文本到 SQL 语义解析 [111, 134] 方面显示出潜力。 5.3 特定领域的应用 RA-LLM 已广泛应用于各种特定领域的任务，例如科学和金融领域的人工智能。 5.3.1 科学人工智能。 RA-LLM 已被证明对分子和蛋白质等科学领域有益。分子包括识别分子的特性和预测新分子，从而有利于药物发现。

### 段落 132 · Page 13

**EN**

Currently, some RA- LLMs have been applied to molecules by integrating retrieval of molecule structure and biomedical entities like protein, molecule, and disease [90, 160, 161, 174], etc. Li et al. [77], Wang et al. [160] propose retrieval-based frameworks by retrieving from the database to guide molecule generation. Liu et al. [90]introduce a multi-modal molecule structure-text model by retrieving textual knowledge from a large-scale dataset for molecular property prediction. In addition, RA-LLMs also significantly influence Protein representation and generation [97, 144].

**中文**

目前，一些 RA-LLM 已通过整合分子结构检索和蛋白质、分子和疾病等生物医学实体来应用于分子[90,160,161,174]等。 [77]，王等人。 [160]提出了基于检索的框架，通过从数据库检索来指导分子生成。刘等人。 [90]通过从大规模数据集中检索文本知识来进行分子特性预测，引入多模式分子结构文本模型。此外，RA-LLM 还显着影响蛋白质的表达和生成 [97, 144]。

### 段落 133 · Page 13

**EN**

For instance, RSA [ 97] queries protein sequences associated with a collection of structurally or functionally similar sequences in the database to enhance protein representations. Furthermore, Lozano et al. [92] present a clinical QA system based on retrieving published review articles. 5.3.2 Finance. In the highly data-driven and information-intensive field of finance, RA-LLMs have proved to be a significant technology for enhancing decision-making [78, 178, 187]. For example, Zhang et al.

**中文**

例如，RSA [97] 查询与数据库中结构或功能相似序列集合相关的蛋白质序列，以增强蛋白质表示。此外，洛萨诺等人。 [92]提出了一个基于检索已发表评论文章的临床质量保证系统。 5.3.2 财务。在高度数据驱动和信息密集的金融领域，RA-LLM 已被证明是增强决策的重要技术[78,178,187]。例如，张等人。

### 段落 134 · Page 13

**EN**

[187] retrieve financial information from external sources, such as news platforms (e.g., Bloomberg and Reuters) and social media platforms (e.g., Twitter, Reddit), to combine with the original query to enhance the precision of financial sentiment analysis. In addition, financial QA is another primary task of financial analysis, which usually extracts relevant knowledge from financial documents. As professional documents are usually stored in PDF format, Lin [85] introduces a PDF parser combined with RA-LLMs to retrieve knowledge from financial reports. On the other hand, Yepes et al.

**中文**

[187]从外部来源检索金融信息，例如新闻平台（例如彭博社和路透社）和社交媒体平台（例如Twitter，Reddit），与原始查询结合以提高金融情绪分析的精度。此外，财务QA是财务分析的另一个主要任务，通常从财务文档中提取相关知识。由于专业文档通常以 PDF 格式存储，Lin [85] 引入了 PDF 解析器与 RA-LLM 相结合，从财务报告中检索知识。另一方面，耶佩斯等人。

### 段落 135 · Page 13

**EN**

[178] propose a document chunking method based on structure instead of chunking based on paragraphs, further improving the quality of RA-LLMs outputs. 6 FUTURE CHALLENGES AND OPPORTUNITIES Since the studies of RA-LLMs are still in the early stage, we present some potential research directions that can be explored in the future in the field of RA-LLMs. Trustworthy RA-LLMs. The essential objective of developing RAG-empowered LLMs is to enhance the capability of the language models, thereby benefiting users and society by alleviating redundant and meaningless labor, increasing conveniences, and spurring social progress.

**中文**

[178]提出了一种基于结构的文档分块方法，而不是基于段落的分块，进一步提高了 RA-LLM 输出的质量。 6 未来的挑战和机遇 由于 RA-LLM 的研究仍处于早期阶段，我们提出了 RA-LLM 领域未来可以探索的一些潜在研究方向。值得信赖的 RA-LLM。发展RAG赋能的法学硕士的根本目标是增强语言模型的能力，从而通过减少冗余和无意义的劳动、增加便利性、促进社会进步来造福用户和社会。

### 段落 136 · Page 13

**EN**

However, recent research indicates that RA-LLMs can be maliciously and unintentionally manipulated to make unreliable decisions and harm humans [ 23, 200], which may have serious consequences in safety-critical scenarios [11, 13, 32, 38, 88]. In addition, private retrieval database has a risk of leakage, raising concerns regarding the privacy of RA-LLMs [186]. Therefore, developing trustworthy RA-LLMs is of paramount importance as it can significantly mitigate the potential negative impacts of LLMs technology and provide people with powerful AI models that can be fully trusted.

**中文**

然而，最近的研究表明，RA-LLM 可能会被恶意和无意地操纵，做出不可靠的决策并伤害人类 [23, 200]，这可能在安全关键场景中产生严重后果 [11, 13, 32, 38, 88]。此外，私人检索数据库存在泄露风险，引起人们对 RA-LLM 隐私的担忧[186]。因此，开发值得信赖的 RA-LLM 至关重要，因为它可以显着减轻 LLM 技术的潜在负面影响，并为人们提供可以完全信任的强大 AI 模型。

### 段落 137 · Page 13

**EN**

To be specific, the ideal trustworthiness in RA-LLMs systems should possess the following characteristics: 1) robustness, 2) fairness, 3) explainability, and 4) privacy. For example, robustness means a trustworthy RA-LLMs system should be robust against malicious or inadvertent perturbations introduced by attackers. Fairness indicates a trustworthy RA-LLMs system ought to avoid discrimination during the decision-making process. Explainability requires a complete understanding of the intrinsic workings of RA-LLMs systems, i.e., the predictions of RA-LLMs systems are explainable and transparent.

**中文**

具体来说，RA-LLMs系统中理想的可信度应具备以下特征：1）稳健性，2）公平性，3）可解释性，4）隐私性。例如，稳健性意味着值得信赖的 RA-LLM 系统应该能够抵御攻击者恶意或无意的干扰。公平性表明一个值得信赖的 RA-LLM 系统应该在决策过程中避免歧视。可解释性需要完全理解 RA-LLMs 系统的内在工作原理，即 RA-LLMs 系统的预测是可解释的和透明的。

### 段落 138 · Page 13

**EN**

Privacy entails safeguarding the safety of this private information housed within the datastore when establishing trustworthy RA-LLMs systems. Multi-Lingual RA-LLMs. The ability of leveraging knowledge from multiple languages can greatly enhance the capabilities of retrieval-augmented language models. As the world becomes increasingly interconnected, there is a growing need for AI systems that can understand and communicate across different languages.

**中文**

在建立值得信赖的 RA-LLM 系统时，隐私需要保护数据存储中存储的私人信息的安全。多语言 RA-LLM。利用多种语言知识的能力可以极大地增强检索增强语言模型的能力。随着世界变得越来越互联，对能够理解和跨不同语言进行交流的人工智能系统的需求不断增长。

### 段落 139 · Page 13

**EN**

By incorporating multilingual knowledge retrieval and generation, these models can access and synthesize information from diverse linguistic sources, enabling more comprehensive and nuanced understanding and generation capabilities. Additionally, multilingual models can facilitate cross-cultural communication and knowledge sharing and breaking down language barriers, thereby bringing convenience to people across different regions of the world, especially those in areas with minority languages [58, 81].

**中文**

通过结合多语言知识检索和生成，这些模型可以访问和合成来自不同语言源的信息，从而实现更全面、细致的理解和生成能力。此外，多语言模式可以促进跨文化交流和知识共享，打破语言障碍，从而为世界不同地区的人们，特别是小语种地区的人们带来便利[58, 81]。

### 段落 140 · Page 13

**EN**

For example, users from countries with less prevalent languages can utilize abundant English and Chinese corpora for knowledge retrieval, enhancing the performance of large language models in downstream tasks. Multi-modal RA-LLMs. Multi-modal retrieval-augmented generation extends the knowledge sources beyond text to include various data modalities such as images, videos, and audio. By integrating various modalities, LLMs can leverage richer contextual information than single-modal RAG and develop a more comprehensive understanding of users’ needs, bringing precise, fine-grained, and high-quality generation.

**中文**

例如，来自语言不太流行的国家的用户可以利用丰富的英文和中文语料库进行知识检索，从而增强大型语言模型在下游任务中的性能。多模式 RA-LLM。多模态检索增强生成将知识源扩展到文本之外，包括图像、视频和音频等各种数据模态。通过整合各种模态，法学硕士可以利用比单模态 RAG 更丰富的上下文信息，更全面地了解用户的需求，从而带来精确、细粒度和高质量的生成。

### 段落 141 · Page 13

**EN**

For instance, an image or video can provide valuable visual cues that complement textual information, leading to more precise language generation [51, 199]. By fusing multiple modalities, multi-modal RA-LLMs can develop a more comprehensive understanding of the world, leading to more accurate and insightful outputs, benefiting a wide range of domains, including healthcare [199], drug discovery [136], molecular analysis [3, 90], etc. 13

**中文**

例如，图像或视频可以提供有价值的视觉线索来补充文本信息，从而产生更精确的语言[51, 199]。通过融合多种模式，多模式 RA-LLM 可以对世界有更全面的了解，从而产生更准确和更有洞察力的输出，使广泛的领域受益，包括医疗保健 [199]、药物发现 [136]、分子分析 [3, 90] 等13

### Page 14

### 段落 142 · Page 14

**EN**

Conference’17, July 2017, Washington, DC, USA Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li Quality of External Knowledge . As a commonly used datastore in current RAG systems, Wikipedia [61, 199] serves as a vast repository of external textual knowledge used to augment the generation process, which contains millions of articles covering various disciplines. However, the reliability and accuracy of individual articles within Wikipedia vary significantly, and the introduction of some texts that deviate from facts might even mislead the model’s generation process.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Wenqi Fan、Yujuan Ding、Liangbo Ning、Shijie Wang、Hengyun Li、Dawei Yin、Tat-Seng Chua 和 Qing Li 外部知识质量。作为当前 RAG 系统中常用的数据存储，维基百科 [61, 199] 作为一个巨大的外部文本知识存储库，用于增强生成过程，其中包含数百万篇涵盖各个学科的文章。然而，维基百科内个别文章的可靠性和准确性差异很大，一些偏离事实的文本的引入甚至可能会误导模型的生成过程。

### 段落 143 · Page 14

**EN**

Therefore, it is crucial to enhance the quality of the external knowledge corpus and mitigate the negative impact of lowquality knowledge on the performance of LLMs. By enhancing the quality of the external knowledge and tailing robust mechanisms by filtering out low-quality or unreliable information, the RA-LLM systems might produce more accurate, reliable outputs, thereby improving their effectiveness in various real-world applications.

**中文**

因此，提高外部知识库的质量，减轻低质量知识对法学硕士成绩的负面影响至关重要。通过过滤低质量或不可靠的信息来提高外部知识的质量和尾随稳健机制，RA-LLM 系统可能会产生更准确、更可靠的输出，从而提高其在各种实际应用中的有效性。

### 段落 144 · Page 14

**EN**

7 CONCLUSION Retrieval-augmented generation (RAG), a cutting-edge AI technique, has achieved remarkable success across various applications, including recommendation, molecule generation, protein representation, and software engineering, owing to the potent capabilities of retrieval in providing supplementary information to enhance generation performance.

**中文**

7 结论 检索增强生成（RAG）是一种前沿的人工智能技术，由于检索在提供补充信息以增强生成性能方面具有强大的能力，因此在推荐、分子生成、蛋白质表示和软件工程等各种应用中取得了显着的成功。

### 段落 145 · Page 14

**EN**

Recently, increasing efforts have been made to alleviate the limitations of large language models (LLMs), such as hallucination and out-of-date internal knowledge, by leveraging retrieval to provide the latest auxiliary information and teaching LLMs to harness the retrieved external knowledge. With the rapid advancements in retrieval-augmented large language models (RA- LLMs), there is a pressing need for a comprehensive and systematic overview.

**中文**

最近，人们越来越努力地通过利用检索提供最新的辅助信息并教导LLM利用检索到的外部知识来缓解大语言模型（LLM）的局限性，例如幻觉和过时的内部知识。随着检索增强大语言模型（RA-LLM）的快速发展，迫切需要全面、系统的概述。

### 段落 146 · Page 14

**EN**

To bridge this gap, in this paper, we comprehensively review the RA-LLMs from the perspectives of morel architecture, training strategy, and application area, providing researchers with an in-depth understanding. Moreover, since the studies of RA-LLMs are still in the early stage, we also discuss the current limitations and several potential research directions for future research. REFERENCES [1] Josh Achiam, Steven Adler, Sandhini Agarwal, Lama Ahmad, Ilge Akkaya, Florencia Leoni Aleman, Diogo Almeida, Janko Altenschmidt, Sam Altman, Shyamal Anadkat, et al. 2023. Gpt-4 technical report. arXiv preprint arXiv:2303.08774 (2023).

**中文**

为了弥补这一差距，在本文中，我们从羊肚菌架构、培训策略和应用领域的角度全面回顾了 RA-LLM，为研究人员提供了深入的理解。此外，由于RA-LLMs的研究仍处于早期阶段，我们还讨论了当前的局限性和未来研究的几个潜在研究方向。参考文献 [1] Josh Achiam、Steven Adler、Sandhini Agarwal、Lama Ahmad、Ilge Akkaya、Florencia Leoni Aleman、Diogo Almeida、Janko Altenschmidt、Sam Altman、Shyamal Anadkat 等。 2023.Gpt-4 技术报告。 arXiv 预印本 arXiv:2303.08774 (2023)。

### 段落 147 · Page 14

**EN**

[2] Sweta Agrawal, Chunting Zhou, Mike Lewis, Luke Zettlemoyer, and Marjan Ghazvininejad. 2023. In-context Examples Selection for Machine Translation. In ACL (Findings). Association for Computational Linguistics, 8857–8873. [3] Miles C Andrews, Junna Oba, Chang-Jiun Wu, Haifeng Zhu, Tatiana Karpinets, Caitlin A Creasy, Marie-Andrée Forget, Xiaoxing Yu, Xingzhi Song, Xizeng Mao, et al. 2022. Multi-modal molecular programs regulate melanoma cell state. Nature communications 13, 1 (2022), 4000. [4] Akari Asai, Sewon Min, Zexuan Zhong, and Danqi Chen. 2023. Retrieval-based language models and applications.

**中文**

[2] Sweta Agrawal、Chunting Zhou、Mike Lewis、Luke Zettlemoyer 和 Marjan Ghazvininejad。 2023.机器翻译的上下文示例选择。在 ACL（调查结果）中。计算语言学协会，8857–8873。 [3] Miles C Andrews、Junna Oba、吴昌均、朱海峰、Tatiana Karpinets、Caitlin A Creasy、Marie-Andrée Forget、于晓星、宋行志、毛喜增等。 2022.多模式分子程序调节黑色素瘤细胞状态。自然通讯 13, 1 (2022), 4000。 [4] Akari Asai、Sewon Min、Zexuan Chung 和 Danqi Chen。 2023.基于检索的语言模型和应用。

### 段落 148 · Page 14

**EN**

In Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 6: Tutorial Abstracts) . 41–46. [5] Akari Asai, Zeqiu Wu, Yizhong Wang, Avirup Sil, and Hannaneh Hajishirzi. 2023. Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection. In The Twelfth International Conference on Learning Representations . [6] Sebastian Borgeaud, Arthur Mensch, Jordan Hoffmann, Trevor Cai, Eliza Rutherford, Katie Millican, George Bm Van Den Driessche, Jean-Baptiste Lespiau, Bogdan Damoc, Aidan Clark, et al. 2022. Improving language models by retrieving from trillions of tokens.

**中文**

计算语言学协会第 61 届年会论文集（第 6 卷：教程摘要）。 41-46。 [5] Akari Asai，Zeqiu Wu，Yizhong Wang，Avirup Sil，Hannaneh Hajishirzi。 2023.Self-RAG：通过自我反思学习检索、生成和批判。在第十二届国际学习表征会议上。 [6] Sebastian Borgeaud、Arthur Mensch、Jordan Hoffmann、Trevor Cai、Eliza Rutherford、Katie Millican、George Bm Van Den Driessche、Jean-Baptiste Lespiau、Bogdan Damoc、Aidan Clark 等。 2022 年。通过检索数万亿个代币来改进语言模型。

### 段落 149 · Page 14

**EN**

In International conference on machine learning . PMLR, 2206–2240. [7] Tom Brown, Benjamin Mann, Nick Ryder, Melanie Subbiah, Jared D Kaplan, Prafulla Dhariwal, Arvind Neelakantan, Pranav Shyam, Girish Sastry, Amanda Askell, et al. 2020. Language models are few-shot learners. Advances in neural information processing systems 33 (2020), 1877–1901. [8] Stefan Buttcher, Charles LA Clarke, and Gordon V Cormack. 2016. Information retrieval: Implementing and evaluating search engines . Mit Press. [9] Charlie Chen, Sebastian Borgeaud, Geoffrey Irving, Jean-Baptiste Lespiau, Laurent Sifre, and John Jumper. 2023.

**中文**

在国际机器学习会议上。 PMLR，2206–2240。 [7] Tom Brown、Benjamin Mann、Nick Ryder、Melanie Subbiah、Jared D Kaplan、Prafulla Dhariwal、Arvind Neelakantan、Pranav Shyam、Girish Sastry、Amanda Askell 等。 2020 年。语言模型是小样本学习者。神经信息处理系统的进展 33 (2020), 1877–1901。 [8] 斯特凡·布彻、查尔斯·LA·克拉克和戈登·V·科马克。 2016.信息检索：实施和评估搜索引擎。麻省理工学院出版社。 [9] Charlie Chen、Sebastian Borgeaud、Geoffrey Irving、Jean-Baptiste Lespiau、Laurent Sifre 和 John Jumper。 2023 年。

### 段落 150 · Page 14

**EN**

Accelerating large language model decoding with speculative sampling. arXiv preprint arXiv:2302.01318 (2023). [10] Danqi Chen, Adam Fisch, Jason Weston, and Antoine Bordes. 2017. Reading Wikipedia to Answer Open-Domain Questions. In ACL (1). Association for Computational Linguistics, 1870–1879. [11] Jingfan Chen, Wenqi Fan, Guanghui Zhu, Xiangyu Zhao, Chunfeng Yuan, Qing Li, and Yihua Huang. 2022. Knowledge-enhanced Black-box Attacks for Recommendations. In Proceedings of the 28th ACM SIGKDD Conference on Knowledge Discovery and Data Mining . 108–117.

**中文**

通过推测采样加速大型语言模型解码。 arXiv 预印本 arXiv:2302.01318 (2023)。 [10] 陈丹琪、亚当·费什、杰森·韦斯顿和安托万·博德斯。 2017。阅读维基百科来回答开放领域问题。在 ACL (1) 中。计算语言学协会，1870-1879。 [11] 陈静帆，范文琪，朱光辉，赵翔宇，袁春风，李清，黄一华。 2022.针对推荐的知识增强黑盒攻击。第 28 届 ACM SIGKDD 知识发现和数据挖掘会议论文集。 108-117。

### 段落 151 · Page 14

**EN**

[12] Mark Chen, Jerry Tworek, Heewoo Jun, Qiming Yuan, Henrique Ponde de Oliveira Pinto, Jared Kaplan, Harri Edwards, Yuri Burda, Nicholas Joseph, Greg Brockman, et al. 2021. Evaluating large language models trained on code. arXiv preprint arXiv:2107.03374 (2021). [13] Xiao Chen, Wenqi Fan, Jingfan Chen, Haochen Liu, Zitao Liu, Zhaoxiang Zhang, and Qing Li. 2023. Fairly adaptive negative sampling for recommendations. In Proceedings of the ACM Web Conference 2023 . 3723–3733. [14] Xiuyi Chen, Fandong Meng, Peng Li, Feilong Chen, Shuang Xu, Bo Xu, and Jie Zhou. 2020.

**中文**

[12] Mark Chen、Jerry Tworek、Heewoo Jun、Qiming Yuan、Henrique Ponde de Oliveira Pinto、Jared Kaplan、Harri Edwards、Yuri Burda、Nicholas Joseph、Greg Brockman 等。 2021.评估基于代码训练的大型语言模型。 arXiv 预印本 arXiv:2107.03374 (2021)。 [13] 陈晓，范文琪，陈静凡，刘浩辰，刘子涛，张兆祥，李庆。 2023. 相当自适应的负采样建议。 2023 年 ACM 网络会议论文集。 3723–3733。 [14] 陈秀一，孟繁东，李鹏，陈飞龙，徐爽，徐波，周杰。 2020.

### 段落 152 · Page 14

**EN**

Bridging the gap between prior and posterior knowledge selection for knowledge-grounded dialogue generation. In Proceedings of the 2020 conference on empirical methods in natural language processing (EMNLP) . 3426–3437. [15] Yudong Chen, Zhihui Lai, Yujuan Ding, Kaiyi Lin, and Wai Keung Wong. 2019. Deep supervised hashing with anchor graph. In Proceedings of the IEEE/CVF international conference on computer vision . 9796–9804. [16] Daixuan Cheng, Shaohan Huang, Junyu Bi, Yuefeng Zhan, Jianfeng Liu, Yujing Wang, Hao Sun, Furu Wei, Weiwei Deng, and Qi Zhang. 2023. UPRISE: Universal Prompt Retrieval for Improving Zero-Shot Evaluation.

**中文**

弥合基于知识的对话生成的先验知识选择和后验知识选择之间的差距。 2020 年自然语言处理实证方法 (EMNLP) 会议论文集。 3426–3437。 [15]陈玉东，赖志辉，丁玉娟，林凯伊，黄伟强。 2019. 使用锚图进行深度监督哈希。 IEEE/CVF 计算机视觉国际会议论文集。 9796–9804。 [16] 程代轩，黄少涵，毕俊宇，詹跃峰，刘剑锋，王玉静，孙浩，魏福如，邓伟伟，张琪。 2023. UPRISE：用于改进零样本评估的通用提示检索。

### 段落 153 · Page 14

**EN**

InProceedings of the 2023 Conference on Empirical Methods in Natural Language Processing . 12318–12337. [17] Xin Cheng, Di Luo, Xiuying Chen, Lemao Liu, Dongyan Zhao, and Rui Yan. 2024. Lift yourself up: Retrieval-augmented text generation with self-memory. Advances in Neural Information Processing Systems 36 (2024). [18] Aakanksha Chowdhery, Sharan Narang, Jacob Devlin, Maarten Bosma, Gaurav Mishra, Adam Roberts, Paul Barham, Hyung Won Chung, Charles Sutton, Sebastian Gehrmann, et al. 2023. Palm: Scaling language modeling with pathways. Journal of Machine Learning Research 24, 240 (2023), 1–113.

**中文**

2023 年自然语言处理经验方法会议论文集。 12318–12337。 [17] 程鑫，罗迪，陈秀英，刘乐茂，赵冬艳，严锐。 2024.提升自己：具有自我记忆的检索增强文本生成。神经信息处理系统的进展 36 (2024)。 [18] Aakanksha Chowdhery、Sharan Narang、Jacob Devlin、Maarten Bosma、Gaurav Mishra、Adam Roberts、Paul Barham、Hyung Won Chung、Charles Sutton、Sebastian Gehrmann 等。 2023. Palm：通过路径扩展语言建模。机器学习研究杂志 24, 240 (2023), 1–113。

### 段落 154 · Page 14

**EN**

[19] W Bruce Croft, Donald Metzler, and Trevor Strohman. 2010. Search engines: Information retrieval in practice . Vol. 520. Addison-Wesley Reading. [20] Leyang Cui, Yu Wu, Jian Liu, Sen Yang, and Yue Zhang. 2021. Template-Based Named Entity Recognition Using BART. In ACL/IJCNLP (Findings) (Findings of ACL, Vol. ACL/IJCNLP 2021). Association for Computational Linguistics, 1835– 1845. [21] Matthew Dahl, Varun Magesh, Mirac Suzgun, and Daniel E Ho. 2024. Large legal fictions: Profiling legal hallucinations in large language models. arXiv preprint arXiv:2401.01301 (2024).

**中文**

[19] W·布鲁斯·克罗夫特、唐纳德·梅茨勒和特雷弗·斯特罗曼。 2010。搜索引擎：信息检索实践。卷。 520.艾迪生-韦斯利阅读。 [20] 崔乐阳，吴宇，刘健，杨森，张悦。 2021。使用 BART 基于模板的命名实体识别。在 ACL/IJCNLP（调查结果）中（ACL 的调查结果，ACL/IJCNLP 2021 卷）。计算语言学协会，1835-1845。 [21] Matthew Dahl、Varun Magesh、Mirac Suzgun 和 Daniel E Ho。 2024.大型法律虚构：在大型语言模型中分析法律幻觉。 arXiv 预印本 arXiv:2401.01301 (2024)。

### 段落 155 · Page 14

**EN**

[22] Michiel de Jong, Yury Zemlyanskiy, Nicholas FitzGerald, Fei Sha, and William W. Cohen. 2022. Mention Memory: incorporating textual knowledge into Transformers through entity mention attention. In ICLR. OpenReview.net. [23] Gelei Deng, Yi Liu, Kailong Wang, Yuekang Li, Tianwei Zhang, and Yang Liu. 2024. Pandora: Jailbreak GPTs by Retrieval Augmented Generation Poisoning. arXiv preprint arXiv:2402.08416 (2024). [24] Ziqing Deng, Zhihui Lai, Yujuan Ding, Heng Kong, and Xu Wu. 2024. Deep Scaling Factor Quantization Network for Large-scale Image Retrieval. In ICMR. ACM, 851–859.

**中文**

[22] Michiel de Jong、Yury Zemlyanskiy、Nicholas FitzGerald、Fei Sha 和 William W. Cohen。 2022.提及记忆：通过实体提及注意力将文本知识融入变形金刚中。在 ICLR 中。 OpenReview.net。 [23] 邓格蕾，刘毅，王凯龙，李跃康，张天伟，刘洋。 2024.潘多拉：通过检索增强生成中毒来越狱 GPT。 arXiv 预印本 arXiv:2402.08416 (2024)。 [24] 邓子清，赖志辉，丁玉娟，孔恒，吴旭。 2024.用于大规模图像检索的深度缩放因子量化网络。在ICMR中。 ACM，851–859。

### 段落 156 · Page 14

**EN**

[25] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. 2019. BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. In NAACL-HLT (1). Association for Computational Linguistics, 4171–4186. [26] Dario Di Palma. 2023. Retrieval-augmented recommender system: Enhancing recommender systems with large language models. In Proceedings of the 17th ACM Conference on Recommender Systems . 1369–1373. [27] Yujuan Ding, Yunshan Ma, Wenqi Fan, Yige Yao, Tat-Seng Chua, and Qing Li. 2024. FashionReGen: LLM-Empowered Fashion Report Generation. arXiv preprint arXiv:2403.06660 (2024). [28] Yujuan Ding, P. Y.

**中文**

[25] Jacob Devlin、Ming-Wei Chang、Kenton Lee 和 Kristina Toutanova。 2019.BERT：用于语言理解的深度双向Transformer的预训练。在 NAACL-HLT (1) 中。计算语言学协会，4171–4186。 [26] 达里奥·迪·帕尔马。 2023. 检索增强推荐系统：使用大型语言模型增强推荐系统。第 17 届 ACM 推荐系统会议论文集。 1369–1373。 [27] 丁玉娟，马云山，范文琪，姚一戈，蔡达成，李庆。 2024.FashionReGen：法学硕士授权时尚报告生成。 arXiv 预印本 arXiv:2403.06660 (2024)。 [28] 丁玉娟，P. Y.

### 段落 157 · Page 14

**EN**

Mok, Yunshan Ma, and Yi Bin. 2023. Personalized fashion outfit generation with user coordination preference learning.Inf. Process. Manag. 60, 5 (2023), 103434. [29] Yujuan Ding, Wai Keung Wong, Zhihui Lai, and Zheng Zhang. 2020. Bilinear Supervised Hashing Based on 2D Image Features. IEEE Trans. Circuits Syst. Video Technol. 30, 2 (2020), 590–602. [30] Yujuan Ding, Wai Keung Wong, Zhihui Lai, and Zheng Zhang. 2020. Discriminative dual-stream deep hashing for large-scale image retrieval. Information Processing & Management 57, 6 (2020), 102288.

**中文**

莫克，马云山，宜宾。 2023.具有用户协调偏好学习的个性化时尚服装生成。Inf。过程。马纳格。 60, 5 (2023), 103434。 [29] 丁玉娟，黄伟强，赖志辉，张正。 2020.基于二维图像特征的双线性监督哈希。 IEEE 传输。电路系统。视频技术。 30, 2 (2020), 590–602。 [30] 丁玉娟，黄伟强，赖志辉，张正。 2020. 用于大规模图像检索的判别性双流深度哈希。信息处理与管理 57, 6 (2020), 102288.

### 段落 158 · Page 14

**EN**

[31] Andrew Drozdov, Nathanael Schärli, Ekin Akyürek, Nathan Scales, Xinying Song, Xinyun Chen, Olivier Bousquet, and Denny Zhou. 2022. Compositional semantic parsing with large language models. In The Eleventh International Conference on Learning Representations . [32] Wenqi Fan, Tyler Derr, Xiangyu Zhao, Yao Ma, Hui Liu, Jianping Wang, Jiliang Tang, and Qing Li. 2021. Attacking black-box recommendations via copying 14

**中文**

[31] Andrew Drozdov、Nathanael Schärli、Ekin Akyürek、Nathan Scales、Xinying Song、Xinyun Chen、Olivier Bousquet 和 Denny Zhou。 2022.大型语言模型的组合语义解析。在第十一届学习表征国际会议上。 [32] 范文琪，泰勒·德尔，赵翔宇，马耀，刘辉，王建平，唐吉良，李庆。 2021. 通过复制攻击黑盒推荐 14

### Page 15

### 段落 159 · Page 15

**EN**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA cross-domain user profiles. In 2021 IEEE 37th International Conference on Data Engineering (ICDE). IEEE, 1583–1594. [33] Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li. 2024. A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models. Proroceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery & Data Mining (2024). [34] Wenqi Fan, Xiaorui Liu, Wei Jin, Xiangyu Zhao, Jiliang Tang, and Qing Li. 2022.

**中文**

关于 RAG 会议法学硕士的调查：迈向检索增强大型语言模型会议’17，2017 年 7 月，美国华盛顿特区跨域用户配置文件。 2021 年 IEEE 第 37 届国际数据工程会议（ICDE）。 IEEE，1583–1594。 [33] 范文琪，丁玉娟，宁良波，王士杰，李恒云，尹大伟，蔡达成，李庆。 2024. RAG 会议法学硕士调查：走向检索增强大型语言模型。第 30 届 ACM SIGKDD 知识发现和数据挖掘会议论文集（2024 年）。 [34] 范文琪，刘晓瑞，金伟，赵翔宇，唐吉良，李庆。 2022 年。

### 段落 160 · Page 15

**EN**

Graph Trend Filtering Networks for Recommendation. InProceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval. 112–121. [35] Wenqi Fan, Yao Ma, Qing Li, Yuan He, Eric Zhao, Jiliang Tang, and Dawei Yin. 2019. Graph neural networks for social recommendation. In The world wide web conference. 417–426. [36] Wenqi Fan, Yao Ma, Qing Li, Jianping Wang, Guoyong Cai, Jiliang Tang, and Dawei Yin. 2020. A graph neural network framework for social recommendations. IEEE Transactions on Knowledge and Data Engineering (2020).

**中文**

用于推荐的图趋势过滤网络。第 45 届国际 ACM SIGIR 信息检索研究与发展会议论文集。 112-121。 [35] 范文琪，马耀，李青，何渊，赵伟，唐吉良，尹大伟。 2019.用于社交推荐的图神经网络。在万维网会议中。 417–426。 [36] 范文琪，马耀，李庆，王建平，蔡国勇，唐吉良，尹大伟。 2020.用于社交推荐的图神经网络框架。 IEEE 知识与数据工程汇刊 (2020)。

### 段落 161 · Page 15

**EN**

[37] Wenqi Fan, Shijie Wang, Jiani Huang, Zhikai Chen, Yu Song, Wenzhuo Tang, Haitao Mao, Hui Liu, Xiaorui Liu, Dawei Yin, et al. 2024. Graph Machine Learning in the Era of Large Language Models (LLMs).arXiv preprint arXiv:2404.14928 (2024). [38] Wenqi Fan, Xiangyu Zhao, Xiao Chen, Jingran Su, Jingtong Gao, Lin Wang, Qidong Liu, Yiqi Wang, Han Xu, Lei Chen, et al. 2022. A Comprehensive Survey on Trustworthy Recommender Systems. arXiv preprint arXiv:2209.10117 (2022). [39] Thibault Févry, Livio Baldini Soares, Nicholas FitzGerald, Eunsol Choi, and Tom Kwiatkowski. 2020. Entities as Experts: Sparse Memory Access with Entity Supervision.

**中文**

[37] 范文琪，王世杰，黄佳妮，陈志凯，宋宇，唐文卓，毛海涛，刘辉，刘晓瑞，尹大伟，等。 2024 年。大型语言模型 (LLM) 时代的图机器学习。arXiv 预印本 arXiv:2404.14928 (2024)。 [38] 范文琪，赵翔宇，陈晓，苏静然，高静桐，王林，刘启东，王一琪，徐涵，陈雷，等。 2022。可信赖推荐系统的综合调查。 arXiv 预印本 arXiv：2209.10117 (2022)。 [39]蒂博·费夫里、利维奥·巴尔迪尼·苏亚雷斯、尼古拉斯·菲茨杰拉德、恩索尔·崔和汤姆·科维亚特科斯基。 2020。实体作为专家：具有实体监督的稀疏内存访问。

### 段落 162 · Page 15

**EN**

In EMNLP (1). Association for Computational Linguistics, 4937– 4951. [40] Luyu Gao, Xueguang Ma, Jimmy Lin, and Jamie Callan. 2023. Precise Zero- Shot Dense Retrieval without Relevance Labels. In ACL (1). Association for Computational Linguistics, 1762–1777. [41] Yunfan Gao, Yun Xiong, Xinyu Gao, Kangxiang Jia, Jinliu Pan, Yuxi Bi, Yi Dai, Jiawei Sun, and Haofen Wang. 2023. Retrieval-augmented generation for large language models: A survey. arXiv preprint arXiv:2312.10997 (2023). [42] Izacard Gautier, Caron Mathilde, Hosseini Lucas, Riedel Sebastian, Bojanowski Piotr, Joulin Armand, and Grave Edouard. 2022.

**中文**

在 EMNLP (1) 中。计算语言学协会，4937-4951。 [40]高鲁宇，马学光，林吉米，杰米卡伦。 2023.无相关标签的精确零样本密集检索。在 ACL (1) 中。计算语言学协会，1762-1777。 [41] 高云帆，熊云，高新宇，贾康祥，潘金六，毕玉玺，戴毅，孙家伟，王浩芬。 2023.大型语言模型的检索增强生成：一项调查。 arXiv 预印本 arXiv:2312.10997 (2023)。 [42] Izacard Gautier、Caron Mathilde、Hosseini Lucas、Riedel Sebastian、Bojanowski Piotr、Joulin Armand 和 Grave Edouard。 2022 年。

### 段落 163 · Page 15

**EN**

Unsupervised dense information retrieval with contrastive learning. Transactions on Machine Learning Research (2022). [43] Marjan Ghazvininejad, Chris Brockett, Ming-Wei Chang, Bill Dolan, Jianfeng Gao, Wen-tau Yih, and Michel Galley. 2018. A knowledge-grounded neural conversation model. In Proceedings of the AAAI Conference on Artificial Intelligence , Vol. 32. [44] Michael R. Glass, Gaetano Rossiello, Md. Faisal Mahbub Chowdhury, Ankita Naik, Pengshan Cai, and Alfio Gliozzo. 2022. Re2G: Retrieve, Rerank, Generate. In NAACL-HLT. Association for Computational Linguistics, 2701–2715. [45] Edouard Grave, Armand Joulin, and Nicolas Usunier.

**中文**

具有对比学习的无监督密集信息检索。机器学习研究汇刊 (2022)。 [43] Marjan Ghazvininejad、Chris Brockett、Ming-Wei Chang、Bill Dolan、Jianfeng Taka、Wen-tau Yih 和 Michel Galley。 2018.基于知识的神经对话模型。 AAAI 人工智能会议论文集，卷。 32. [44] Michael R. Glass、Gaetano Rossiello、Md. Faisal Mahbub Chowdhury、Ankita Naik、Pengshan Cai 和 Alfio Gliozzo。 2022.Re2G：检索、重新排序、生成。在 NAACL-HLT 中。计算语言学协会，2701-2715。 [45] 爱德华·格雷夫、阿曼德·朱林和尼古拉斯·乌苏尼尔。

### 段落 164 · Page 15

**EN**

2017. Improving Neural Language Models with a Continuous Cache. In ICLR (Poster). OpenReview.net. [46] Kelvin Guu, Kenton Lee, Zora Tung, Panupong Pasupat, and Mingwei Chang. 2020. Retrieval augmented language model pre-training. In International conference on machine learning . PMLR, 3929–3938. [47] Junxian He, Graham Neubig, and Taylor Berg-Kirkpatrick. 2021. Efficient Nearest Neighbor Language Models. In EMNLP (1). Association for Computational Linguistics, 5703–5714. [48] Qiuxiang He, Guoping Huang, Qu Cui, Li Li, and Lemao Liu. 2021. Fast and accurate neural machine translation with translation memory.

**中文**

2017。通过连续缓存改进神经语言模型。在 ICLR（海报）中。 OpenReview.net。 [46] Kelvin Guu、Kenton Lee、Zora Tung、Panupong Pasupat 和 Mingwei Chang。 2020.检索增强语言模型预训练。在国际机器学习会议上。 PMLR，3929–3938。 [47] 何俊贤、格雷厄姆·纽比格和泰勒·伯格-柯克帕特里克。 2021.高效的最近邻语言模型。在 EMNLP (1) 中。计算语言学协会，5703–5714。 [48] 何秋香，黄国平，崔曲，李丽，刘乐茂。 2021 年。带有翻译记忆库的快速准确的神经机器翻译。

### 段落 165 · Page 15

**EN**

In Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (Volume 1: Long Papers). 3170–3180. [49] Zhenyu He, Zexuan Zhong, Tianle Cai, Jason D Lee, and Di He. 2023. Rest: Retrieval-based speculative decoding. arXiv preprint arXiv:2311.08252 (2023). [50] Sebastian Hofstätter, Jiecao Chen, Karthik Raman, and Hamed Zamani. 2023. FiD-Light: Efficient and Effective Retrieval-Augmented Text Generation. In SIGIR. ACM, 1437–1447.

**中文**

计算语言学协会第 59 届年会暨第 11 届自然语言处理国际联合会议论文集（第一卷：长论文）。 3170–3180。 [49] 何振宇，钟泽轩，蔡天乐，Jason D Lee，何迪。 2023.休息：基于检索的推测解码。 arXiv 预印本 arXiv:2311.08252 (2023)。 [50] Sebastian Hofstätter、Jiecao Chen、Karthik Raman 和 Hamed Zamani。 2023.FiD-Light：高效且有效的检索增强文本生成。在西吉尔。 ACM，1437–1447。

### 段落 166 · Page 15

**EN**

[51] Ziniu Hu, Ahmet Iscen, Chen Sun, Zirui Wang, Kai-Wei Chang, Yizhou Sun, Cordelia Schmid, David A Ross, and Alireza Fathi. 2023. Reveal: Retrievalaugmented visual-language pre-training with multi-source multimodal knowledge memory. In Proceedings of the IEEE/CVF conference on computer vision and pattern recognition. 23369–23379. [52] Jie Huang, Wei Ping, Peng Xu, Mohammad Shoeybi, Kevin Chen-Chuan Chang, and Bryan Catanzaro. 2023. Raven: In-context learning with retrieval augmented encoder-decoder language models. arXiv preprint arXiv:2308.07922 (2023). [53] Gautier Izacard and Edouard Grave. 2021.

**中文**

[51] 胡紫牛，艾哈迈德·伊森，孙晨，王自瑞，张凯伟，孙一洲，Cordelia Schmid，David A Ross，Alireza Fathi。 2023.揭示：利用多源多模态知识记忆检索视觉语言预训练。 IEEE/CVF 计算机视觉和模式识别会议论文集。 23369–23379。 [52] 黄杰，平卫，徐鹏，Mohammad Shoeybi，Kevin Chen-Chuan Chang，Bryan Catanzaro。 2023. Raven：利用检索增强编码器-解码器语言模型进行上下文学习。 arXiv 预印本 arXiv:2308.07922 (2023)。 [53]戈蒂埃·伊扎卡尔和爱德华·格雷夫。 2021 年。

### 段落 167 · Page 15

**EN**

Distilling Knowledge from Reader to Retriever for Question Answering. In ICLR 2021-9th International Conference on Learning Representations. [54] Gautier Izacard and Edouard Grave. 2021. Leveraging Passage Retrieval with Generative Models for Open Domain Question Answering. In EACL 2021-16th Conference of the European Chapter of the Association for Computational Linguistics. Association for Computational Linguistics, 874–880. [55] Gautier Izacard, Patrick Lewis, Maria Lomeli, Lucas Hosseini, Fabio Petroni, Timo Schick, Jane Dwivedi-Yu, Armand Joulin, Sebastian Riedel, and Edouard Grave. 2023.

**中文**

将读者的知识提炼给检索器以进行问答。 ICLR 2021-第九届学习表征国际会议。 [54]戈蒂埃·伊扎卡尔和爱德华·格雷夫。 2021。利用段落检索和生成模型进行开放域问答。计算语言学协会欧洲分会 EACL 2021-16 届会议。计算语言学协会，874–880。 [55] Gautier Izacard、Patrick Lewis、Maria Lomeli、Lucas Hosseini、Fabio Petroni、Timo Schick、Jane Dwivedi-Yu、Armand Joulin、Sebastian Riedel 和 Edouard Grave。 2023 年。

### 段落 168 · Page 15

**EN**

Atlas: Few-shot Learning with Retrieval Augmented Language Models. Journal of Machine Learning Research 24, 251 (2023), 1–43. [56] Zhengbao Jiang, Jun Araki, Haibo Ding, and Graham Neubig. 2021. How can we know when language models know? on the calibration of language models for question answering. Transactions of the Association for Computational Linguistics 9 (2021), 962–977. [57] Zhengbao Jiang, Frank F Xu, Luyu Gao, Zhiqing Sun, Qian Liu, Jane Dwivedi- Yu, Yiming Yang, Jamie Callan, and Graham Neubig. 2023. Active Retrieval Augmented Generation. In Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing .

**中文**

Atlas：使用检索增强语言模型进行少样本学习。机器学习研究杂志 24, 251 (2023), 1–43。 [56]蒋正宝，荒木俊，丁海波，Graham Neubig。 2021.我们如何知道语言模型何时知道？关于问答语言模型的校准。计算语言学协会汇刊 9 (2021), 962–977。 [57] 蒋正宝，Frank F Xu，高鲁宇，孙志清，刘谦，Jane Dwivedi-Yu，Yiming Yang，Jamie Callan，Graham Neubig。 2023.主动检索增强生成。 2023 年自然语言处理经验方法会议论文集。

### 段落 169 · Page 15

**EN**

7969–7992. [58] Anubha Kabra, Emmy Liu, Simran Khanuja, Alham Fikri Aji, Genta Winata, Samuel Cahyawijaya, Anuoluwapo Aremu, Perez Ogayo, and Graham Neubig. 2023. Multi-lingual and Multi-cultural Figurative Language Understanding. In The 61st Annual Meeting Of The Association For Computational Linguistics . [59] Saurav Kadavath, Tom Conerly, Amanda Askell, Tom Henighan, Dawn Drain, Ethan Perez, Nicholas Schiefer, Zac Hatfield-Dodds, Nova DasSarma, Eli Tran- Johnson, et al. 2022. Language models (mostly) know what they know. arXiv preprint arXiv:2207.05221 (2022). [60] Minki Kang, Jin Myung Kwak, Jinheon Baek, and Sung Ju Hwang. 2023.

**中文**

7969–7992。 [58] Anubha Kabra、Emmy Liu、Simran Khanuja、Alham Fikri Aji、Genta Winata、Samuel Cahyawijaya、Anuoluwapo Aremu、Perez Ogayo 和 Graham Neubig。 2023.多语言和多文化比喻语言理解。在计算语言学协会第61届年会上。 [59] Saurav Kadavath、Tom Conerly、Amanda Askell、Tom Henighan、Dawn Drain、Ethan Perez、Nicholas Schiefer、Zac Hatfield-Dodds、Nova DasSarma、Eli Tran-Johnson 等。 2022 年。语言模型（大部分）知道他们所知道的。 arXiv 预印本 arXiv:2207.05221 (2022)。 [60] Minki Kang、Jin Myung Kwak、Jinheon Baek 和 Sung Ju Hwang。 2023 年。

### 段落 170 · Page 15

**EN**

Knowledge graph-augmented language models for knowledge-grounded dialogue generation. arXiv preprint arXiv:2305.18846 (2023). [61] Vladimir Karpukhin, Barlas Oguz, Sewon Min, Patrick S. H. Lewis, Ledell Wu, Sergey Edunov, Danqi Chen, and Wen-tau Yih. 2020. Dense Passage Retrieval for Open-Domain Question Answering. In EMNLP (1). Association for Computational Linguistics, 6769–6781. [62] Urvashi Khandelwal, Omer Levy, Dan Jurafsky, Luke Zettlemoyer, and Mike Lewis. 2020. Generalization through Memorization: Nearest Neighbor Language Models. In International Conference on Learning Representations .

**中文**

用于基于知识的对话生成的知识图增强语言模型。 arXiv 预印本 arXiv:2305.18846 (2023)。 [61] Vladimir Karpukhin、Barlas Oguz、Sewon Min、Patrick S. H. Lewis、Ledell Wu、Sergey Edunov、Danqi Chen 和 Wen-tau Yih。 2020.用于开放域问答的密集段落检索。在 EMNLP (1) 中。计算语言学协会，6769–6781。 [62] Urvashi Khandelwal、Omer Levy、Dan Jurafsky、Luke Zettlemoyer 和 Mike Lewis。 2020。通过记忆进行泛化：最近邻语言模型。在国际学习代表会议上。

### 段落 171 · Page 15

**EN**

[63] Omar Khattab, Keshav Santhanam, Xiang Lisa Li, David Hall, Percy Liang, Christopher Potts, and Matei Zaharia. 2022. Demonstrate-search-predict: Composing retrieval and language models for knowledge-intensive nlp. arXiv preprint arXiv:2212.14024 (2022). [64] Omar Khattab and Matei Zaharia. 2020. Colbert: Efficient and effective passage search via contextualized late interaction over bert. In Proceedings of the 43rd International ACM SIGIR conference on research and development in Information Retrieval. 39–48. [65] Gangwoo Kim, Sungdong Kim, Byeongguk Jeon, Joonsuk Park, and Jaewoo Kang. 2023.

**中文**

[63] Omar Khattab、Keshav Santhanam、Xiang Lisa Li、David Hall、Percy Liang、Christopher Potts 和 Matei Zaharia。 2022. 演示搜索预测：为知识密集型 NLP 构建检索和语言模型。 arXiv 预印本 arXiv:2212.14024 (2022)。 [64] 奥马尔·哈塔布和马泰·扎哈里亚。 2020. Colbert：通过 bert 上的上下文化后期交互进行高效且有效的段落搜索。第 43 届国际 ACM SIGIR 信息检索研究与开发会议论文集。 39-48。 [65] Gangwoo Kim、Sungdong Kim、Byeongguk Jeon、Joonsuk Park 和 Jaewoo Kang。 2023 年。

### 段落 172 · Page 15

**EN**

Tree of Clarifications: Answering Ambiguous Questions with Retrieval- Augmented Large Language Models. InThe 2023 Conference on Empirical Methods in Natural Language Processing . [66] Hyuhng Joon Kim, Hyunsoo Cho, Junyeob Kim, Taeuk Kim, Kang Min Yoo, and Sang-goo Lee. 2022. Self-generated in-context learning: Leveraging autoregressive language models as a demonstration generator. arXiv preprint arXiv:2206.08082 (2022). [67] Mei Kobayashi and Koichi Takeda. 2000. Information retrieval on the web.ACM computing surveys (CSUR) 32, 2 (2000), 144–173. [68] Mojtaba Komeili, Kurt Shuster, and Jason Weston. 2022.

**中文**

澄清之树：用检索增强的大型语言模型回答模棱两可的问题。在 2023 年自然语言处理经验方法会议上。 [66] Hyuhng Joon Kim、Hyunsoo Cho、Junyeob Kim、Taeuk Kim、Kang Min Yoo 和 Sang-goo Lee。 2022. 自生成上下文学习：利用自回归语言模型作为演示生成器。 arXiv 预印本 arXiv:2206.08082 (2022)。 [67]小林梅和武田浩一。 2000 年。网络信息检索。ACM 计算调查 (CSUR) 32, 2 (2000), 144–173。 [68] Mojtaba Komeili、Kurt Shuster 和 Jason Weston。 2022 年。

### 段落 173 · Page 15

**EN**

Internet-Augmented Dialogue Generation. In ACL (1). Association for Computational Linguistics, 8460–8478. [69] Tian Lan, Deng Cai, Yan Wang, Heyan Huang, and Xian-Ling Mao. 2022. Copy is All You Need. In The Eleventh International Conference on Learning Representations. [70] Angeliki Lazaridou, Elena Gribovskaya, Wojciech Stokowiec, and Nikolai Grigorev. 2022. Internet-augmented language models through few-shot prompting for open-domain question answering. arXiv preprint arXiv:2203.05115 (2022). [71] Yaniv Leviathan, Matan Kalman, and Yossi Matias. 2023. Fast inference from transformers via speculative decoding.

**中文**

互联网增强对话生成。在 ACL (1) 中。计算语言学协会，8460–8478。 [69]田兰，蔡邓，王岩，黄鹤彦，毛先灵。 2022 年。您所需要的就是文案。在第十一届国际学习表征会议上。 [70] Angeliki Lazaridou、Elena Gribovskaya、Wojciech Stokowiec 和 Nikolai Grigorev。 2022 年。通过少量提示进行开放域问答的互联网增强语言模型。 arXiv 预印本 arXiv:2203.05115 (2022)。 [71] Yaniv Leviathan、Matan Kalman 和 Yossi Matias。 2023. 通过推测解码从 Transformer 进行快速推理。

### 段落 174 · Page 15

**EN**

In International Conference on Machine Learning. PMLR, 19274–19286. [72] Mike Lewis, Marjan Ghazvininejad, Gargi Ghosh, Armen Aghajanyan, Sida Wang, and Luke Zettlemoyer. 2020. Pre-training via paraphrasing. Advances in Neural Information Processing Systems 33 (2020), 18470–18481. [73] Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Veselin Stoyanov, and Luke Zettlemoyer. 2020. BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension. In ACL. Association for Computational Linguistics, 7871–7880.

**中文**

在国际机器学习会议上。 PMLR，19274–19286。 [72] Mike Lewis、Marjan Ghazvininejad、Gargi Ghosh、Armen Aghajanyan、Sida Wang 和 Luke Zettlemoyer。 2020.通过释义进行预训练。神经信息处理系统的进展 33 (2020), 18470–18481。 [73] Mike Lewis、Yinhan Liu、Naman Goyal、Marjan Ghazvininejad、Abdelrahman Mohamed、Omer Levy、Veselin Stoyanov 和 Luke Zettlemoyer。 2020.BART：用于自然语言生成、翻译和理解的去噪序列到序列预训练。在ACL中。计算语言学协会，7871–7880。

### 段落 175 · Page 15

**EN**

[74] Patrick Lewis, Ethan Perez, Aleksandra Piktus, Fabio Petroni, Vladimir Karpukhin, Naman Goyal, Heinrich Küttler, Mike Lewis, Wen-tau Yih, Tim Rocktäschel, et al. 2020. Retrieval-augmented generation for knowledge-intensive nlp tasks. Advances in Neural Information Processing Systems 33 (2020), 9459–9474. [75] Daliang Li, Ankit Singh Rawat, Manzil Zaheer, Xin Wang, Michal Lukasik, Andreas Veit, Felix Yu, and Sanjiv Kumar. 2022. Large language models with controllable working memory. arXiv preprint arXiv:2211.05110 (2022). [76] Hongxin Li, Jingran Su, Yuntao Chen, Qing Li, and ZHAO-XIANG ZHANG. 2024.

**中文**

[74] Patrick Lewis、Ethan Perez、Aleksandra Piktus、Fabio Petroni、Vladimir Karpukhin、Naman Goyal、Heinrich Küttler、Mike Lewis、Wen-tau Yih、Tim Rocktäschel 等人。 2020.知识密集型 NLP 任务的检索增强生成。神经信息处理系统的进展 33 (2020), 9459–9474。 [75] 李大亮、Ankit Singh Rawat、Manzil Zaheer、Xin Wang、Michal Lukasik、Andreas Veit、Felix Yu 和 Sanjiv Kumar。 2022.具有可控工作记忆的大型语言模型。 arXiv 预印本 arXiv:2211.05110 (2022)。 [76] 李红鑫，苏静然，陈云涛，李庆，张兆祥。 2024 年。

### 段落 176 · Page 15

**EN**

SheetCopilot: Bringing Software Productivity to the Next Level through Large Language Models. Advances in Neural Information Processing Systems 36 (2024). 15

**中文**

SheetCopilot：通过大型语言模型将软件生产力提升到新的水平。神经信息处理系统的进展 36 (2024)。 15

### Page 16

### 段落 177 · Page 16

**EN**

Conference’17, July 2017, Washington, DC, USA Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li [77] Jiatong Li, Yunqing Liu, Wenqi Fan, Xiao-Yong Wei, Hui Liu, Jiliang Tang, and Qing Li. 2023. Empowering Molecule Discovery for Molecule-Caption Translation with Large Language Models: A ChatGPT Perspective.arXiv preprint arXiv:2306.06615 (2023). [78] Xiang Li, Zhenyu Li, Chen Shi, Yong Xu, Qing Du, Mingkui Tan, Jun Huang, and Wei Lin. 2024. AlphaFin: Benchmarking Financial Analysis with Retrieval- Augmented Stock-Chain Framework. arXiv preprint arXiv:2403.12582 (2024).

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Wenqi Fan、Yujuan Ding、Liangbo Ning、Shijie Wang、Hengyun Li、Dawei Yin、Tat-Seng Chua 和 Qing Li [77] Jiatong Li、Yunqing Liu、Wenqi Fan、Xiao-Yong Wei、Hui Liu、Jiliang Tang 和 Qing Li。 2023. 使用大型语言模型增强分子标题翻译的分子发现：ChatGPT Perspective.arXiv 预印本 arXiv:2306.06615 (2023)。 [78] 李翔，李振宇，陈实，徐勇，杜庆，谭明奎，黄军，林伟。 2024.AlphaFin：使用检索增强的股票链框架进行基准财务分析。 arXiv 预印本 arXiv:2403.12582 (2024)。

### 段落 178 · Page 16

**EN**

[79] Xinze Li, Zhenghao Liu, Chenyan Xiong, Shi Yu, Yu Gu, Zhiyuan Liu, and Ge Yu. 2023. Structure-Aware Language Model Pretraining Improves Dense Retrieval on Structured Data. In The 61st Annual Meeting Of The Association For Computational Linguistics. [80] Xiaonan Li, Kai Lv, Hang Yan, Tianyang Lin, Wei Zhu, Yuan Ni, Guotong Xie, Xiaoling Wang, and Xipeng Qiu. 2023. Unified Demonstration Retriever for In-Context Learning. In ACL (1). Association for Computational Linguistics, 4644–4668. [81] Xiaoqian Li, Ercong Nie, and Sheng Liang. 2023. From Classification to Generation: Insights into Crosslingual Retrieval Augmented ICL.

**中文**

[79] 李新泽，刘正浩，熊晨燕，石宇，谷宇，刘志远，余戈。 2023。结构感知语言模型预训练改进了结构化数据的密集检索。在计算语言学协会第 61 届年会上。 [80] 李晓楠，吕凯，严航，林天阳，朱伟，倪媛，谢国通，王晓玲，邱西鹏。 2023.用于情境学习的统一演示检索器。在 ACL (1) 中。计算语言学协会，4644–4668。 [81] 李晓倩，聂尔聪，梁盛。 2023。从分类到生成：跨语言检索增强 ICL 的见解。

### 段落 179 · Page 16

**EN**

In NeurIPS 2023 Workshop on Instruction Tuning and Instruction Following . [82] Xiaonan Li and Xipeng Qiu. 2023. MoT: Memory-of-Thought Enables ChatGPT to Self-Improve. In Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing . Association for Computational Linguistics, Singapore, 6354–6374. [83] Xiang Lisa Li and Percy Liang. 2021. Prefix-Tuning: Optimizing Continuous Prompts for Generation. In ACL/IJCNLP (1). Association for Computational Linguistics, 4582–4597. [84] Zonglin Li, Ruiqi Guo, and Sanjiv Kumar. 2022. Decoupled context processing for context augmented language modeling.

**中文**

在 NeurIPS 2023 指令调优和指令跟踪研讨会中。 [82] 李晓楠，邱西鹏。 2023. MoT：思维记忆使 ChatGPT 能够自我改进。 2023 年自然语言处理经验方法会议论文集。计算语言学协会，新加坡，6354–6374。 [83] 李翔，梁珀西。 2021.前缀调优：优化生成的连续提示。在 ACL/IJCNLP (1) 中。计算语言学协会，4582–4597。 [84]李宗林，郭瑞琪，Sanjiv Kumar。 2022. 用于上下文增强语言建模的解耦上下文处理。

### 段落 180 · Page 16

**EN**

Advances in Neural Information Processing Systems 35 (2022), 21698–21710. [85] Demiao Lin. 2024. Revolutionizing Retrieval-Augmented Generation with Enhanced PDF Structure Recognition. arXiv preprint arXiv:2401.12599 (2024). [86] Xi Victoria Lin, Xilun Chen, Mingda Chen, Weijia Shi, Maria Lomeli, Richard James, Pedro Rodriguez, Jacob Kahn, Gergely Szilvasy, Mike Lewis, et al. 2023. RA-DIT: Retrieval-Augmented Dual Instruction Tuning. In The Twelfth International Conference on Learning Representations . [87] Haochen Liu, Jamell Dacon, Wenqi Fan, Hui Liu, Zitao Liu, and Jiliang Tang. 2020. Does Gender Matter?

**中文**

神经信息处理系统的进展 35 (2022), 21698–21710。 [85] 林德苗. 2024 年。通过增强的 PDF 结构识别彻底改变检索增强生成。 arXiv 预印本 arXiv：2401.12599 (2024)。 [86] Xi Victoria Lin、Xilun Chen、Mingda Chen、Weijia Shi、Maria Lomeli、Richard James、Pedro Rodriguez、Jacob Kahn、Gergely Szilvasy、Mike Lewis 等。 2023.RA-DIT：检索增强双指令调优。在第十二届国际学习表征会议上。 [87]刘浩辰，Jamell Dacon，范文琪，刘辉，刘子涛，唐吉良。 2020.性别重要吗？

### 段落 181 · Page 16

**EN**

Towards Fairness in Dialogue Systems. In Proceedings of the 28th International Conference on Computational Linguistics . 4403–4416. [88] Haochen Liu, Yiqi Wang, Wenqi Fan, Xiaorui Liu, Yaxin Li, Shaili Jain, Yunhao Liu, Anil K Jain, and Jiliang Tang. 2021. Trustworthy ai: A computational perspective. arXiv preprint arXiv:2107.06641 (2021). [89] Jiachang Liu, Dinghan Shen, Yizhe Zhang, Bill Dolan, Lawrence Carin, and Weizhu Chen. 2022. What Makes Good In-Context Examples for GPT-3?. In DeeLIO@ACL. Association for Computational Linguistics, 100–114.

**中文**

实现对话系统的公平。第 28 届国际计算语言学会议论文集。 4403–4416。 [88]刘浩辰，王一琪，范文琪，刘晓瑞，李亚欣，Shaili Jain，刘云浩，Anil K Jain，唐吉良。 2021.值得信赖的人工智能：计算视角。 arXiv 预印本 arXiv:2107.06641 (2021)。 [89]刘家昌，沉定汉，张一哲，比尔·多兰，劳伦斯·卡林，陈伟竹。 2022.什么是 GPT-3 的良好上下文示例？在 DeeLIO@ACL。计算语言学协会，100-114。

### 段落 182 · Page 16

**EN**

[90] Shengchao Liu, Weili Nie, Chengpeng Wang, Jiarui Lu, Zhuoran Qiao, Ling Liu, Jian Tang, Chaowei Xiao, and Animashree Anandkumar. 2023. Multi-modal molecule structure–text model for text-based retrieval and editing. Nature Machine Intelligence 5, 12 (2023), 1447–1457. [91] Ye Liu, Semih Yavuz, Rui Meng, Dragomir Radev, Caiming Xiong, and Yingbo Zhou. 2022. Uni-Parser: Unified Semantic Parser for Question Answering on Knowledge Base and Database. In EMNLP. Association for Computational Linguistics, 8858–8869. [92] Alejandro Lozano, Scott L Fleming, Chia-Chun Chiang, and Nigam Shah. 2023. Clinfo.

**中文**

[90] 刘胜超，聂伟丽，王成鹏，陆嘉瑞，乔卓然，刘凌，唐健，肖超伟，Animashree Anandkumar。 2023.用于基于文本的检索和编辑的多模式分子结构-文本模型。自然机器智能 5, 12 (2023), 1447–1457。 [91] 刘晔，Semih Yavuz，孟锐，Dragomir Radev，熊彩明，周英波。 2022. Uni-Parser：用于知识库和数据库问答的统一语义解析器。在 EMNLP 中。计算语言学协会，8858–8869。 [92] 亚历杭德罗·洛扎诺、斯科特·L·弗莱明、Chia-Chun Jiang 和 Nigam Shah。 2023.克林信息。

### 段落 183 · Page 16

**EN**

ai: An open-source retrieval-augmented large language model system for answering medical questions using scientific literature. In PACIFIC SYMPOSIUM ON BIOCOMPUTING 2024 . World Scientific, 8–23. [93] Pan Lu, Liang Qiu, Kai-Wei Chang, Ying Nian Wu, Song-Chun Zhu, Tanmay Rajpurohit, Peter Clark, and Ashwin Kalyan. 2023. Dynamic Prompt Learning via Policy Gradient for Semi-structured Mathematical Reasoning. In ICLR. OpenReview.net. [94] Yu Lu, Junwei Bao, Yan Song, Zichen Ma, Shuguang Cui, Youzheng Wu, and Xiaodong He. 2021. RevCore: Review-Augmented Conversational Recommendation. In ACL/IJCNLP (Findings) (Findings of ACL, Vol.

**中文**

ai：一种开源检索增强大型语言模型系统，用于使用科学文献回答医学问题。在 2024 年太平洋生物计算研讨会上。世界科学，8-23。 [93] 潘璐，邱亮，张凯伟，吴英年，朱松春，Tanmay Rajpurohit，Peter Clark，Ashwin Kalyan。 2023.通过半结构化数学推理的策略梯度进行动态即时学习。在 ICLR 中。 OpenReview.net。 [94] 陆宇，鲍俊伟，宋岩，马子晨，崔曙光，吴友正，何晓东。 2021.RevCore：审查增强对话建议。在 ACL/IJCNLP（调查结果）中（ACL 的调查结果，卷。

### 段落 184 · Page 16

**EN**

ACL/IJCNLP 2021) . Association for Computational Linguistics, 1161–1173. [95] Hongyin Luo, Tianhua Zhang, Yung-Sung Chuang, Yuan Gong, Yoon Kim, Xixin Wu, Helen Meng, and James R. Glass. 2023. Search Augmented Instruction Learning. In EMNLP (Findings). Association for Computational Linguistics, 3717– 3729. [96] Man Luo, Xin Xu, Zhuyun Dai, Panupong Pasupat, Mehran Kazemi, Chitta Baral, Vaiva Imbrasaite, and Vincent Y Zhao. 2023. Dr. icl: Demonstration-retrieved in-context learning. arXiv preprint arXiv:2305.14128 (2023). [97] Chang Ma, Haiteng Zhao, Lin Zheng, Jiayi Xin, Qintong Li, Lijun Wu, Zhihong Deng, Yang Lu, Qi Liu, and Lingpeng Kong.

**中文**

ACL/IJCNLP 2021）。计算语言学协会，1161–1173。 [95] 罗红银、张天华、庄永松、龚原、Yoon Kim、吴西新、孟海伦和詹姆斯·R·格拉斯。 2023.搜索增强教学学习。在 EMNLP（调查结果）中。计算语言学协会，3717-3729。 [96] 罗曼，徐鑫，戴竹云，Panupong Pasupat，Mehran Kazemi，Chitta Baral，Vaiva Imbrasaite 和 Vincent Y Zhu。 2023. icl 博士：示范检索情境学习。 arXiv 预印本 arXiv:2305.14128 (2023)。 [97] 马昌，赵海腾，郑林，辛佳怡，李勤潼，吴丽君，邓志宏，路阳，刘琪，孔令鹏。

### 段落 185 · Page 16

**EN**

2023. Retrieved Sequence Augmentation for Protein Representation Learning. bioRxiv (2023), 2023–02. [98] Xinbei Ma, Yeyun Gong, Pengcheng He, Hai Zhao, and Nan Duan. 2023. Query rewriting for retrieval-augmented large language models. arXiv preprint arXiv:2305.14283 (2023). [99] Seiji Maekawa, Hayate Iso, Sairam Gurajada, and Nikita Bhutani. 2024. Retrieval Helps or Hurts? A Deeper Dive into the Efficacy of Retrieval Augmentation to Language Models. arXiv preprint arXiv:2402.13492 (2024).

**中文**

2023.检索蛋白质表示学习的序列增强。 BioRxiv (2023)，2023–02。 [98]马新贝，宫业云，何鹏程，赵海，段南。 2023.检索增强大型语言模型的查询重写。 arXiv 预印本 arXiv:2305.14283 (2023)。 [99] Seiji Maekawa、Hayate Iso、Sairam Gurajada 和 Nikita Bhutani。 2024. 检索是有帮助还是有害？深入研究语言模型检索增强的功效。 arXiv 预印本 arXiv:2402.13492 (2024)。

### 段落 186 · Page 16

**EN**

[100] Jacob Menick, Maja Trebacz, Vladimir Mikulik, John Aslanides, Francis Song, Martin Chadwick, Mia Glaese, Susannah Young, Lucy Campbell-Gillingham, Geoffrey Irving, et al. 2022. Teaching language models to support answers with verified quotes. arXiv preprint arXiv:2203.11147 (2022). [101] Aristides Milios, Siva Reddy, and Dzmitry Bahdanau. 2023. In-context learning for text classification with many labels. In Proceedings of the 1st GenBench Workshop on (Benchmarking) Generalisation in NLP . 173–184. [102] Sewon Min, Xinxi Lyu, Ari Holtzman, Mikel Artetxe, Mike Lewis, Hannaneh Hajishirzi, and Luke Zettlemoyer. 2022.

**中文**

[100] Jacob Menick、Maja Trebacz、Vladimir Mikulik、John Aslanides、Francis Song、Martin Chadwick、Mia Glaese、Susannah Young、Lucy Campbell-Gillingham、Geoffrey Irving 等。 2022. 教授语言模型以支持经过验证的引用的答案。 arXiv 预印本 arXiv:2203.11147 (2022)。 [101] 阿里斯蒂德斯·米利奥斯、西瓦·雷迪和德兹米特里·巴德瑙。 2023.具有许多标签的文本分类的上下文学习。在关于 NLP 泛化（基准测试）的第一届 GenBench 研讨会的会议记录中。 173–184。 [102] Sewon Min、Xinxi Lyu、Ari Holtzman、Mikel Artetxe、Mike Lewis、Hannaneh Hajishirzi 和 Luke Zettlemoyer。 2022 年。

### 段落 187 · Page 16

**EN**

Rethinking the Role of Demonstrations: What Makes In-Context Learning Work?. In EMNLP. Association for Computational Linguistics, 11048–11064. [103] Sewon Min, Julian Michael, Hannaneh Hajishirzi, and Luke Zettlemoyer. 2020. AmbigQA: Answering Ambiguous Open-domain Questions. In EMNLP (1). Association for Computational Linguistics, 5783–5797. [104] Sewon Min, Weijia Shi, Mike Lewis, Xilun Chen, Wen-tau Yih, Hannaneh Hajishirzi, and Luke Zettlemoyer. 2023. Nonparametric Masked Language Modeling. In ACL (Findings). Association for Computational Linguistics, 2097–2118. [105] Noor Nashid, Mifta Sintaha, and Ali Mesbah. 2023.

**中文**

重新思考演示的作用：什么使情境学习发挥作用？在 EMNLP 中。计算语言学协会，11048–11064。 [103] Sewon Min、Julian Michael、Hannaneh Hajishirzi 和 Luke Zettlemoyer。 2020.AmbigQA：回答模棱两可的开放域问题。在 EMNLP (1) 中。计算语言学协会，5783–5797。 [104] Sewon Min、Weijia Shi、Mike Lewis、Xilun Chen、Wen-tau Yih、Hannaneh Hajishirzi 和 Luke Zettlemoyer。 2023.非参数屏蔽语言建模。在 ACL（调查结果）中。计算语言学协会，2097-2118。 [105] 努尔·纳希德、米夫塔·辛塔哈和阿里·梅斯巴。 2023 年。

### 段落 188 · Page 16

**EN**

Retrieval-based prompt selection for code-related few-shot learning. In2023 IEEE/ACM 45th International Conference on Software Engineering (ICSE) . IEEE, 2450–2462. [106] Neil O’Hare, Paloma De Juan, Rossano Schifanella, Yunlong He, Dawei Yin, and Yi Chang. 2016. Leveraging user interaction signals for web image search. In Proceedings of the 39th International ACM SIGIR conference on Research and Development in Information Retrieval . 559–568. [107] Long Ouyang, Jeffrey Wu, Xu Jiang, Diogo Almeida, Carroll Wainwright, Pamela Mishkin, Chong Zhang, Sandhini Agarwal, Katarina Slama, Alex Ray, et al. 2022.

**中文**

基于检索的提示选择，用于与代码相关的小样本学习。 2023年IEEE/ACM第45届国际软件工程会议（ICSE）。 IEEE，2450–2462。 [106] Neil O’Hare、Paloma De Juan、Rossano Schifanella、何云龙、尹大伟、张毅。 2016.利用用户交互信号进行网络图像搜索。第 39 届国际 ACM SIGIR 信息检索研究与开发会议论文集。 559–568。 [107] 欧阳龙，吴杰弗里，江旭，迪奥戈·阿尔梅达，卡罗尔·温赖特，帕梅拉·米什金，张冲，桑迪尼·阿加瓦尔，卡塔琳娜·斯拉马，亚历克斯·雷，等。 2022 年。

### 段落 189 · Page 16

**EN**

Training language models to follow instructions with human feedback.Advances in neural information processing systems 35 (2022), 27730–27744. [108] Md. Rizwan Parvez, Wasi Uddin Ahmad, Saikat Chakraborty, Baishakhi Ray, and Kai-Wei Chang. 2021. Retrieval Augmented Code Generation and Summarization. In EMNLP (Findings). Association for Computational Linguistics, 2719–2734. [109] Fabio Petroni, Patrick S. H. Lewis, Aleksandra Piktus, Tim Rocktäschel, Yuxiang Wu, Alexander H. Miller, and Sebastian Riedel. 2020. How Context Affects Language Models’ Factual Predictions. InAKBC.

**中文**

训练语言模型以遵循人类反馈的指令。神经信息处理系统的进展 35 (2022), 27730–27744。 [108] Md. Rizwan Parvez、Wasi Uddin Ahmad、Saikat Chakraborty、Baishakhi Ray 和 Kai-Wei Chang。 2021.检索增强代码生成和摘要。在 EMNLP（调查结果）中。计算语言学协会，2719-2734。 [109] 法比奥·佩特罗尼 (Fabio Petroni)、帕特里克·S·H·刘易斯 (Patrick S. H. Lewis)、亚历山大·皮克图斯 (Aleksandra Piktus)、蒂姆·洛克塔舍尔 (Tim Rocktäschel)、吴宇翔 (Yuxiang Wu)、亚历山大·H·米勒 (Alexander H. Miller) 和塞巴斯蒂安·里德尔 (Sebastian Riedel)。 2020。上下文如何影响语言模型的事实预测。在AKBC。

### 段落 190 · Page 16

**EN**

[110] Fabio Petroni, Tim Rocktäschel, Patrick Lewis, Anton Bakhtin, Yuxiang Wu, Alexander H Miller, and Sebastian Riedel. 2019. Language models as knowledge bases? arXiv preprint arXiv:1909.01066 (2019). [111] Gabriel Poesia, Alex Polozov, Vu Le, Ashish Tiwari, Gustavo Soares, Christopher Meek, and Sumit Gulwani. 2022. Synchromesh: Reliable Code Generation from Pre-trained Language Models. In ICLR. OpenReview.net. [112] Anupam Purwar and Rahul Sundar. 2023. Keyword Augmented Retrieval: Novel framework for Information Retrieval integrated with speech interface. arXiv preprint arXiv:2310.04205 (2023).

**中文**

[110] 法比奥·彼得罗尼、蒂姆·罗克塔舍尔、帕特里克·刘易斯、安东·巴赫金、吴宇翔、亚历山大·H·米勒和塞巴斯蒂安·里德尔。 2019.语言模型作为知识库？ arXiv 预印本 arXiv:1909.01066 (2019)。 [111] Gabriel Poesia、Alex Polozov、Vu Le、Ashish Tiwari、Gustavo Soares、Christopher Meek 和 Sumit Gulwani。 2022. Synchromesh：从预先训练的语言模型生成可靠的代码。在 ICLR 中。 OpenReview.net。 [112]阿努潘·普瓦尔和拉胡尔·桑达尔。 2023. 关键字增强检索：与语音接口集成的信息检索新框架。 arXiv 预印本 arXiv:2310.04205 (2023)。

### 段落 191 · Page 16

**EN**

[113] Alec Radford, Jong Wook Kim, Chris Hallacy, Aditya Ramesh, Gabriel Goh, Sandhini Agarwal, Girish Sastry, Amanda Askell, Pamela Mishkin, Jack Clark, et al. 2021. Learning transferable visual models from natural language supervision. In International conference on machine learning . PMLR, 8748–8763. [114] Alec Radford, Karthik Narasimhan, Tim Salimans, Ilya Sutskever, et al. 2018. Improving language understanding by generative pre-training. (2018). [115] Alec Radford, Jeffrey Wu, Rewon Child, David Luan, Dario Amodei, Ilya Sutskever, et al. 2019. Language models are unsupervised multitask learners. OpenAI blog 1, 8 (2019), 9.

**中文**

[113] Alec Radford、Jong Wook Kim、Chris Hallacy、Aditya Ramesh、Gabriel Goh、Sandhini Agarwal、Girish Sastry、Amanda Askell、Pamela Mishkin、Jack Clark 等。 2021.从自然语言监督中学习可迁移的视觉模型。在国际机器学习会议上。 PMLR，8748–8763。 [114] Alec Radford、Karthik Narasimhan、Tim Salimans、Ilya Sutskever 等人。 2018.通过生成预训练提高语言理解。 （2018）。 [115] Alec Radford、Jeffrey Wu、Rewon Child、David Luan、Dario Amodei、Ilya Sutskever 等。 2019。语言模型是无监督的多任务学习者。 OpenAI 博客 1, 8 (2019), 9。

### 段落 192 · Page 16

**EN**

[116] Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, and Peter J Liu. 2020. Exploring the limits of transfer learning with a unified text-to-text transformer. Journal of machine learning research 21, 140 (2020), 1–67. [117] Ori Ram, Yoav Levine, Itay Dalmedigos, Dor Muhlgay, Amnon Shashua, Kevin Leyton-Brown, and Yoav Shoham. 2023. In-context retrieval-augmented language models. Transactions of the Association for Computational Linguistics 11 (2023), 1316–1331. [118] Ori Ram, Gal Shachaf, Omer Levy, Jonathan Berant, and Amir Globerson. 2022.

**中文**

[116] Colin Raffel、Noam Shazeer、Adam Roberts、Katherine Lee、Sharan Narang、Michael Matena、Yanqi Zhou、Wei Li 和 Peter J Liu。 2020。使用统一的文本到文本转换器探索迁移学习的局限性。机器学习研究杂志 21, 140 (2020), 1–67。 [117] Ori Ram、Yoav Levine、Itay Dalmedigos、Dor Muhlgay、Amnon Shashua、Kevin Leyton-Brown 和 Yoav Shoham。 2023.上下文检索增强语言模型。计算语言学协会汇刊 11 (2023), 1316–1331。 [118] 奥里·拉姆、加尔·沙查夫、奥马尔·利维、乔纳森·贝兰特和阿米尔·格洛伯森。 2022 年。

### 段落 193 · Page 16

**EN**

Learning to Retrieve Passages without Supervision. InNAACL-HLT. Association for Computational Linguistics, 2687–2700. [119] Parikshit Ram and Alexander G Gray. 2012. Maximum inner-product search using cone trees. InProceedings of the 18th ACM SIGKDD international conference on Knowledge discovery and data mining . 931–939. [120] Juan Ramos et al. 2003. Using tf-idf to determine word relevance in document queries. In Proceedings of the first instructional conference on machine learning , Vol. 242. Citeseer, 29–48. [121] Rita Ramos, Bruno Martins, Desmond Elliott, and Yova Kementchedjhieva. 2023.

**中文**

学习在没有监督的情况下检索段落。在NAACL-HLT。计算语言学协会，2687-2700。 [119] 帕里克希特·拉姆和亚历山大·G·格雷。 2012.使用圆锥树的最大内积搜索。第 18 届 ACM SIGKDD 知识发现和数据挖掘国际会议论文集。 931–939。 [120] 胡安·拉莫斯等人。 2003.使用 tf-idf 确定文档查询中的单词相关性。在第一届机器学习教学会议记录中，卷。 242.Citeseer，29-48。 [121] 丽塔·拉莫斯、布鲁诺·马丁斯、德斯蒙德·埃利奥特和约瓦·凯门切吉耶娃。 2023 年。

### 段落 194 · Page 16

**EN**

Smallcap: lightweight image captioning prompted with retrieval augmentation. In Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2840–2849. [122] Benjamin Z. Reichman and Larry Heck. 2024. Retrieval-Augmented Generation: Is Dense Passage Retrieval Retrieving? CoRR abs/2402.11035 (2024). 16

**中文**

Smallcap：带有检索增强提示的轻量级图像字幕。 IEEE/CVF 计算机视觉和模式识别会议论文集。 2840–2849。 [122] 本杰明·Z·赖克曼和拉里·赫克。 2024.检索增强生成：密集通道检索是检索吗？ CoRR 绝对/2402.11035 (2024)。 16

### Page 17

### 段落 195 · Page 17

**EN**

A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models Conference’17, July 2017, Washington, DC, USA [123] Nils Reimers and Iryna Gurevych. 2019. Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks. InProceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP) . 3982–3992. [124] Yubing Ren, Yanan Cao, Ping Guo, Fang Fang, Wei Ma, and Zheng Lin. 2023. Retrieve-and-sample: Document-level event argument extraction via hybrid retrieval augmentation.

**中文**

关于 RAG 会议法学硕士的调查：迈向检索增强大型语言模型会议’17，2017 年 7 月，美国华盛顿特区 [123] Nils Reimers 和 Iryna Gurevych。 2019.Sentence-BERT：使用 Siamese BERT 网络的句子嵌入。 2019年自然语言处理经验方法会议暨第九届自然语言处理国际联合会议（EMNLP-IJCNLP）论文集。 3982–3992。 [124] 任玉兵，曹亚楠，郭平，方方，马伟，林正。 2023.检索和样本：通过混合检索增强进行文档级事件参数提取。

### 段落 196 · Page 17

**EN**

In Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) . 293–306. [125] Stephen Robertson, Hugo Zaragoza, et al . 2009. The probabilistic relevance framework: BM25 and beyond. Foundations and Trends® in Information Retrieval 3, 4 (2009), 333–389. [126] Ohad Rubin, Jonathan Herzig, and Jonathan Berant. 2022. Learning To Retrieve Prompts for In-Context Learning. In NAACL-HLT. Association for Computational Linguistics, 2655–2671. [127] Sara Sarto, Marcella Cornia, Lorenzo Baraldi, and Rita Cucchiara. 2022. Retrievalaugmented transformer for image captioning.

**中文**

计算语言学协会第 61 届年会论文集（第一卷：长论文）。 293–306。 [125] 斯蒂芬·罗伯逊、雨果·萨拉戈萨等人。 2009。概率相关性框架：BM25 及以后。信息检索基础和趋势® 3, 4 (2009), 333–389。 [126] 奥哈德·鲁宾、乔纳森·赫齐格和乔纳森·贝兰特。 2022.学习检索情境学习的提示。在 NAACL-HLT 中。计算语言学协会，2655-2671。 [127] 萨拉·萨尔托、马塞拉·科尼亚、洛伦佐·巴拉尔迪和丽塔·库奇亚拉。 2022.检索用于图像字幕的Transformer。

### 段落 197 · Page 17

**EN**

In Proceedings of the 19th international conference on content-based multimedia indexing . 1–7. [128] Timo Schick, Jane Dwivedi-Yu, Roberto Dessì, Roberta Raileanu, Maria Lomeli, Eric Hambro, Luke Zettlemoyer, Nicola Cancedda, and Thomas Scialom. 2024. Toolformer: Language models can teach themselves to use tools. Advances in Neural Information Processing Systems 36 (2024). [129] Minjoon Seo, Jinhyuk Lee, Tom Kwiatkowski, Ankur P Parikh, Ali Farhadi, and Hannaneh Hajishirzi. 2019. Real-time open-domain question answering with dense-sparse phrase index. arXiv preprint arXiv:1906.05807 (2019).

**中文**

第 19 届基于内容的多媒体索引国际会议论文集。 1-7。 [128] Timo Schick、Jane Dwivedi-Yu、Roberto Dessì、Roberta Raileanu、Maria Lomeli、Eric Hambro、Luke Zettlemoyer、Nicola Cancedda 和 Thomas Scialom。 2024. Toolformer：语言模型可以自学使用工具。神经信息处理系统的进展 36 (2024)。 [129] Minjoon Seo、Jinhyuk Lee、Tom Kwiatkowski、Ankur P Parikh、Ali Farhadi 和 Hannaneh Hajishirzi。 2019.具有密集稀疏短语索引的实时开放域问答。 arXiv 预印本 arXiv:1906.05807 (2019)。

### 段落 198 · Page 17

**EN**

[130] Zhihong Shao, Yeyun Gong, Minlie Huang, Nan Duan, Weizhu Chen, et al . 2023. Enhancing Retrieval-Augmented Large Language Models with Iterative Retrieval-Generation Synergy. In The 2023 Conference on Empirical Methods in Natural Language Processing. [131] Fumin Shen, Wei Liu, Shaoting Zhang, Yang Yang, and Heng Tao Shen. 2015. Learning binary codes for maximum inner product search. In Proceedings of the IEEE International Conference on Computer Vision . 4148–4156. [132] Shelly Sheynin, Oron Ashual, Adam Polyak, Uriel Singer, Oran Gafni, Eliya Nachmani, and Yaniv Taigman. 2023. kNN-Diffusion: Image Generation via Large-Scale Retrieval.

**中文**

[130] 邵志宏，宫业云，黄敏烈，段楠，陈伟柱，等。 2023.通过迭代检索生成协同作用增强检索增强大型语言模型。 2023 年自然语言处理经验方法会议。 [131] 沉福民，刘伟，张绍亭，杨阳，沉恒涛。 2015.学习二进制代码以实现最大内积搜索。 IEEE 国际计算机视觉会议论文集。 4148–4156。 [132] Shelly Sheynin、Oron Ashual、Adam Polyak、Uriel Singer、Oran Gafni、Eliya Nachmani 和 Yaniv Taigman。 2023.kNN-Diffusion：通过大规模检索生成图像。

### 段落 199 · Page 17

**EN**

In ICLR. OpenReview.net. [133] Kaize Shi, Xueyao Sun, Qing Li, and Guandong Xu. 2024. Compressing Long Context for Enhancing RAG with AMR-based Concept Distillation. arXiv preprint arXiv:2405.03085 (2024). [134] Peng Shi, Rui Zhang, He Bai, and Jimmy Lin. 2022. XRICL: Cross-lingual Retrieval-Augmented In-Context Learning for Cross-lingual Text-to-SQL Semantic Parsing. In EMNLP (Findings). Association for Computational Linguistics, 5248–5259. [135] Weijia Shi, Sewon Min, Michihiro Yasunaga, Minjoon Seo, Rich James, Mike Lewis, Luke Zettlemoyer, and Wen-tau Yih. 2023. Replug: Retrieval-augmented black-box language models.

**中文**

在 ICLR 中。 OpenReview.net。 [133]石凯泽，孙雪耀，李青，徐冠东。 2024. 通过基于 AMR 的概念蒸馏压缩长上下文以增强 RAG。 arXiv 预印本 arXiv:2405.03085 (2024)。 [134] 石鹏，张锐，何白，林志颖。 2022. XRICL：用于跨语言文本到 SQL 语义解析的跨语言检索增强上下文学习。在 EMNLP（调查结果）中。计算语言学协会，5248–5259。 [135] Weijia Shi、Sewon Min、Michihiro Yasunaga、Minjoon Seo、Rich James、Mike Lewis、Luke Zettlemoyer 和 Wen-tau Yih。 2023. Replug：检索增强的黑盒语言模型。

### 段落 200 · Page 17

**EN**

arXiv preprint arXiv:2301.12652 (2023). [136] Guy Shtar. 2021. Multimodal machine learning for drug knowledge discovery. In Proceedings of the 14th ACM International Conference on Web Search and Data Mining. 1115–1116. [137] Kurt Shuster, Spencer Poff, Moya Chen, Douwe Kiela, and Jason Weston. 2021. Retrieval Augmentation Reduces Hallucination in Conversation. In EMNLP (Findings). Association for Computational Linguistics, 3784–3803. [138] Suzanna Sia and Kevin Duh. 2023. In-context learning as maintaining coherency: A study of on-the-fly machine translation using large language models. arXiv preprint arXiv:2305.03573 (2023).

**中文**

arXiv 预印本 arXiv:2301.12652 (2023)。 [136] 盖伊·什塔尔。 2021.用于药物知识发现的多模式机器学习。第 14 届 ACM 国际网络搜索和数据挖掘会议论文集。 1115–1116。 [137] 库尔特·舒斯特、斯宾塞·波夫、莫亚·陈、杜威·基拉和杰森·韦斯顿。 2021.检索增强减少对话中的幻觉。在 EMNLP（调查结果）中。计算语言学协会，3784-3803。 [138] 苏珊娜·西亚和凯文·杜。 2023. 上下文学习保持一致性：使用大型语言模型进行即时机器翻译的研究。 arXiv 预印本 arXiv:2305.03573 (2023)。

### 段落 201 · Page 17

**EN**

[139] Devendra Singh, Siva Reddy, Will Hamilton, Chris Dyer, and Dani Yogatama. 2021. End-to-end training of multi-document reader and retriever for opendomain question answering. Advances in Neural Information Processing Systems 34 (2021), 25968–25981. [140] Amit Singhal et al. 2001. Modern information retrieval: A brief overview. IEEE Data Eng. Bull. 24, 4 (2001), 35–43. [141] Shamane Siriwardhana, Rivindu Weerasekera, Elliott Wen, Tharindu Kaluarachchi, Rajib Rana, and Suranga Nanayakkara. 2023. Improving the domain adaptation of retrieval augmented generation (RAG) models for open domain question answering.

**中文**

[139]德文德拉·辛格、西瓦·雷迪、威尔·汉密尔顿、克里斯·戴尔和丹尼·瑜伽塔玛。 2021 年。用于开放域问答的多文档阅读器和检索器的端到端培训。神经信息处理系统的进展 34 (2021), 25968–25981。 [140]阿米特·辛哈尔等人。 2001. 现代信息检索：简要概述。 IEEE 数据工程。公牛。 24, 4 (2001), 35–43。 [141]Shamane Siriwardhana、Rivindu Weerasekera、Elliott Wen、Tharindu Kaluarachchi、R​​ajib Rana 和 Suranga Nanayakkara。 2023. 改进开放域问答的检索增强生成（RAG）模型的域适应。

### 段落 202 · Page 17

**EN**

Transactions of the Association for Computational Linguistics 11 (2023), 1–17. [142] Karen Sparck Jones. 1972. A statistical interpretation of term specificity and its application in retrieval. Journal of documentation 28, 1 (1972), 11–21. [143] Hongjin Su, Jungo Kasai, Chen Henry Wu, Weijia Shi, Tianlu Wang, Jiayi Xin, Rui Zhang, Mari Ostendorf, Luke Zettlemoyer, Noah A. Smith, and Tao Yu. 2023. Selective Annotation Makes Language Models Better Few-Shot Learners. In ICLR. OpenReview.net. [144] Fang Sun, Zhihao Zhan, Hongyu Guo, Ming Zhang, and Jian Tang. 2023.

**中文**

计算语言学协会汇刊 11 (2023), 1–17。 [142]凯伦·斯帕克·琼斯。 1972.术语特异性的统计解释及其在检索中的应用。文献杂志 28, 1 (1972), 11–21。 [143] Hongjin Su，Jungo Kasai，Chen Henry Wu，Weijia Shi，Tianlu Wang，Jiayi Xin，Rui Zhu，Mari Ostendorf，Luke Zettlemoyer，Noah A. Smith和Tao Yu。 2023.选择性注释使语言模型更好地适应少样本学习者。在 ICLR 中。 OpenReview.net。 [144]孙芳，詹志浩，郭宏宇，张明，唐健。 2023 年。

### 段落 203 · Page 17

**EN**

Graphvf: Controllable protein-specific 3d molecule generation with variational flow.arXiv preprint arXiv:2304.12825 (2023). [145] Ziteng Sun, Ananda Theertha Suresh, Jae Hun Ro, Ahmad Beirami, Himanshu Jain, and Felix Yu. 2024. Spectr: Fast speculative decoding via optimal transport. Advances in Neural Information Processing Systems 36 (2024). [146] Jiejun Tan, Zhicheng Dou, Yutao Zhu, Peidong Guo, Kun Fang, and Ji-Rong Wen. 2024. Small Models, Big Insights: Leveraging Slim Proxy Models To Decide When and What to Retrieve for LLMs. arXiv preprint arXiv:2402.12052 (2024).

**中文**

Graphvf：具有变分流的可控蛋白质特异性 3D 分子生成。arXiv 预印本 arXiv：2304.12825（2023）。 [145] Ziteng Sun、Ananda Theertha Suresh、Jae Hun Ro、Ahmad Beirami、Himanshu Jain 和 Felix Yu。 2024. Spectr：通过最佳传输进行快速推测解码。神经信息处理系统的进展 36 (2024)。 [146] 谭杰军，窦志成，朱玉涛，郭培东，方坤，文继荣。 2024 年。小模型，大见解：利用细长的代理模型来决定法学硕士检索的时间和内容。 arXiv 预印本 arXiv:2402.12052 (2024)。

### 段落 204 · Page 17

**EN**

[147] Nandan Thakur, Luiz Bonifacio, Xinyu Zhang, Odunayo Ogundepo, Ehsan Kamalloo, David Alfonso-Hermelo, Xiaoguang Li, Qun Liu, Boxing Chen, Mehdi Rezagholizadeh, et al . 2023. NoMIRACL: Knowing When You Don’t Know for Robust Multilingual Retrieval-Augmented Generation. arXiv preprint arXiv:2312.11361 (2023). [148] Hugo Touvron, Louis Martin, Kevin Stone, Peter Albert, Amjad Almahairi, Yasmine Babaei, Nikolay Bashlykov, Soumya Batra, Prajjwal Bhargava, Shruti Bhosale, et al. 2023. Llama 2: Open foundation and fine-tuned chat models. arXiv preprint arXiv:2307.09288 (2023).

**中文**

[147] Nandan Thakur，Luiz Bonifacio，张新宇，Odunayo Ogundepo，Ehsan Kamalloo，David Alfonso-Hermelo，李晓光，刘群，陈拳击，Mehdi Rezagholizadeh，等。 2023.NoMIRACL：当你不知道时就知道，以实现强大的多语言检索增强生成。 arXiv 预印本 arXiv:2312.11361 (2023)。 [148] Hugo Touvron、Louis Martin、Kevin Stone、Peter Albert、Amjad Almahairi、Yasmine Babaei、Nikolay Bashlykov、Soumya Batra、Prajjwal Bhargava、Shruti Bhosale 等。 2023. Llama 2：开放基础和微调的聊天模型。 arXiv 预印本 arXiv:2307.09288 (2023)。

### 段落 205 · Page 17

**EN**

[149] Harsh Trivedi, Niranjan Balasubramanian, Tushar Khot, and Ashish Sabharwal. 2023. Interleaving Retrieval with Chain-of-Thought Reasoning for Knowledge- Intensive Multi-Step Questions. In The 61st Annual Meeting Of The Association For Computational Linguistics. [150] Lifu Tu, Caiming Xiong, and Yingbo Zhou. 2022. Prompt-Tuning Can Be Much Better Than Fine-Tuning on Cross-lingual Understanding With Multilingual Language Models. In EMNLP (Findings). Association for Computational Linguistics, 5478–5485. [151] Tu Vu, Brian Lester, Noah Constant, Rami Al-Rfou’, and Daniel Cer. 2022.

**中文**

[149] Harsh Trivedi、Niranjan Balasubramanian、Tushar Khot 和 Ashish Sabharwal。 2023.知识密集型多步骤问题的交叉检索与思想链推理。在计算语言学协会第 61 届年会上。 [150]屠立夫，熊才明，周英波。 2022 年。对于多语言语言模型的跨语言理解，即时调整比微调要好得多。在 EMNLP（调查结果）中。计算语言学协会，5478–5485。 [151] Tu Vu、Brian Lester、Noah Constant、Rami Al-Rfou' 和 Daniel Cer。 2022 年。

### 段落 206 · Page 17

**EN**

SPoT: Better Frozen Model Adaptation through Soft Prompt Transfer. In ACL (1). Association for Computational Linguistics, 5039–5059. [152] Ante Wang, Linfeng Song, Qi Liu, Haitao Mi, Longyue Wang, Zhaopeng Tu, Jinsong Su, and Dong Yu. 2023. Search-engine-augmented dialogue response generation with cheaply supervised query production. Artificial Intelligence 319 (2023), 103874. [153] Boxin Wang, Wei Ping, Peng Xu, Lawrence McAfee, Zihan Liu, Mohammad Shoeybi, Yi Dong, Oleksii Kuchaiev, Bo Li, Chaowei Xiao, et al. 2023. Shall We Pretrain Autoregressive Language Models with Retrieval? A Comprehensive Study.

**中文**

SPoT：通过软提示传输更好地适应冻结模型。在 ACL (1) 中。计算语言学协会，5039–5059。 [152]王安特，宋林峰，刘奇，米海涛，王龙跃，涂兆鹏，苏劲松，于东。 2023 年。搜索引擎增强对话响应生成与廉价的监督查询生成。人工智能 319 (2023), 103874。 [153] 王博鑫，平伟，徐鹏，Lawrence McAfee，刘子涵，Mohammad Shoeybi，董易，Oleksii Kuchaiev，李博，肖超伟，等。 2023.我们应该通过检索来预训练自回归语言模型吗？一项综合研究。

### 段落 207 · Page 17

**EN**

In Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing. 7763–7786. [154] Hanbing Wang, Xiaorui Liu, Wenqi Fan, Xiangyu Zhao, Venkataramana Kini, Devendra Yadav, Fei Wang, Zhen Wen, Jiliang Tang, and Hui Liu. 2024. Rethinking Large Language Model Architectures for Sequential Recommendations. arXiv preprint arXiv:2402.09543 (2024). [155] Haoyu Wang, Tuo Zhao, and Jing Gao. 2024. BlendFilter: Advancing Retrieval- Augmented Large Language Models via Query Generation Blending and Knowledge Filtering. arXiv preprint arXiv:2402.11129 (2024). [156] Liang Wang, Nan Yang, and Furu Wei. 2023.

**中文**

2023 年自然语言处理经验方法会议论文集。 7763–7786。 [154] 王寒冰，刘晓瑞，范文琪，赵翔宇，Venkataramana Kini，Devendra Yadav，王飞，文震，唐吉良，刘辉。 2024。重新思考顺序推荐的大型语言模型架构。 arXiv 预印本 arXiv:2402.09543 (2024)。 [155]王浩宇，赵拓，高靖。 2024. BlendFilter：通过查询生成混合和知识过滤推进检索-增强大型语言模型。 arXiv 预印本 arXiv:2402.11129 (2024)。 [156] 王亮，杨南，魏福如。 2023 年。

### 段落 208 · Page 17

**EN**

Query2doc: Query Expansion with Large Language Models. In EMNLP. Association for Computational Linguistics, 9414–9423. [157] Liang Wang, Nan Yang, and Furu Wei. 2024. Learning to Retrieve In-Context Examples for Large Language Models. In EACL (1). Association for Computational Linguistics, 1752–1767. [158] Xintao Wang, Qianwen Yang, Yongting Qiu, Jiaqing Liang, Qianyu He, Zhouhong Gu, Yanghua Xiao, and Wei Wang. 2023. Knowledgpt: Enhancing large language models with retrieval and storage access on knowledge bases. arXiv preprint arXiv:2308.11761 (2023). [159] Yile Wang, Peng Li, Maosong Sun, and Yang Liu. 2023.

**中文**

Query2doc：使用大型语言模型进行查询扩展。在 EMNLP 中。计算语言学协会，9414–9423。 [157] 王亮，杨南，魏福如。 2024.学习检索大型语言模型的上下文示例。在 EACL (1) 中。计算语言学协会，1752-1767。 [158]王新涛，杨干文，邱永廷，梁嘉庆，何千宇，谷周红，肖阳华，王伟。 2023.Knowledgpt：通过知识库的检索和存储访问增强大型语言模型。 arXiv 预印本 arXiv:2308.11761 (2023)。 [159]王一乐，李鹏，孙茂松，刘阳。 2023 年。

### 段落 209 · Page 17

**EN**

Self-Knowledge Guided Retrieval Augmentation for Large Language Models. In The 2023 Conference on Empirical Methods in Natural Language Processing . [160] Zichao Wang, Weili Nie, Zhuoran Qiao, Chaowei Xiao, Richard G. Baraniuk, and Anima Anandkumar. 2023. Retrieval-based Controllable Molecule Generation. In ICLR. OpenReview.net. [161] Zifeng Wang, Zichen Wang, Balasubramaniam Srinivasan, Vassilis N Ioannidis, Huzefa Rangwala, and Rishita Anubhai. 2023. BioBridge: Bridging Biomedical Foundation Models via Knowledge Graph. arXiv preprint arXiv:2310.03320 (2023).

**中文**

大型语言模型的自我知识引导检索增强。在 2023 年自然语言处理经验方法会议中。 [160] 王子超，聂伟力，乔卓然，肖超伟，Richard G. Baraniuk，Anima Anandkumar。 2023.基于检索的可控分子生成。在 ICLR 中。 OpenReview.net。 [161] 王子峰、王子晨、Balasubramaniam Srinivasan、Vassilis N Ioannidis、Huzefa Rangwala 和 Rishita Anubhai。 2023. BioBridge：通过知识图桥接生物医学基础模型。 arXiv 预印本 arXiv:2310.03320 (2023)。

### 段落 210 · Page 17

**EN**

[162] Jason Wei, Xuezhi Wang, Dale Schuurmans, Maarten Bosma, Fei Xia, Ed Chi, Quoc V Le, Denny Zhou, et al. 2022. Chain-of-thought prompting elicits reasoning in large language models. Advances in neural information processing systems 35 (2022), 24824–24837. [163] Junda Wu, Cheng-Chun Chang, Tong Yu, Zhankui He, Jianing Wang, Yupeng Hou, and Julian McAuley. 2024. CoRAL: Collaborative Retrieval-Augmented Large Language Models Improve Long-tail Recommendation. arXiv preprint arXiv:2403.06447 (2024). [164] Ledell Wu, Fabio Petroni, Martin Josifoski, Sebastian Riedel, and Luke Zettlemoyer. 2020.

**中文**

[162] Jason Wei，Xuezhi Wang，Dale Schuurmans，Maarten Bosma，Fei Xia，Ed Chi，Quoc V Le，Denny Zhou，等。 2022. 思维链提示引发大型语言模型的推理。神经信息处理系统的进展 35 (2022), 24824–24837。 [163]吴俊达，张正春，余童，何占奎，王佳宁，侯玉鹏，朱利安·麦考利。 2024. CoRAL：协作检索增强大型语言模型改善长尾推荐。 arXiv 预印本 arXiv:2403.06447 (2024)。 [164] Ledell Wu、Fabio Petroni、Martin Josifoski、Sebastian Riedel 和 Luke Zettlemoyer。 2020.

### 段落 211 · Page 17

**EN**

Scalable Zero-shot Entity Linking with Dense Entity Retrieval. In EMNLP (1). Association for Computational Linguistics, 6397–6407. [165] Yuhuai Wu, Markus Norman Rabe, DeLesley Hutchins, and Christian Szegedy. 2022. Memorizing Transformers. In ICLR. OpenReview.net. [166] Miao Xiong, Zhiyuan Hu, Xinyang Lu, Yifei Li, Jie Fu, Junxian He, and Bryan Hooi. 2023. Can llms express their uncertainty? an empirical evaluation of confidence elicitation in llms. arXiv preprint arXiv:2306.13063 (2023). [167] Benfeng Xu, Chunxu Zhao, Wenbin Jiang, PengFei Zhu, Songtai Dai, Chao Pang, Zhuo Sun, Shuohuan Wang, and Yu Sun. 2023.

**中文**

可扩展的零样本实体链接与密集实体检索。在 EMNLP (1) 中。计算语言学协会，6397–6407。 [165] 吴玉怀、马库斯·诺曼·拉贝、德莱斯利·哈钦斯和克里斯蒂安·塞格迪。 2022. 记忆变形金刚。在 ICLR 中。 OpenReview.net。 [166] 熊苗，胡志远，路新阳，李逸飞，付杰，何俊贤，Bryan Hooi。 2023. LLMS 可以表达他们的不确定性吗？ LLMS 中信心激发的实证评估。 arXiv 预印本 arXiv:2306.13063 (2023)。 [167]徐本峰，赵春旭，姜文斌，朱鹏飞，戴松泰，庞超，孙卓，王硕环，孙宇。 2023 年。

### 段落 212 · Page 17

**EN**

Retrieval-augmented domain adaptation of language models. In Proceedings of the 8th Workshop on Representation Learning for NLP (RepL4NLP 2023) . 54–64. 17

**中文**

语言模型的检索增强领域适应。第八届 NLP 表征学习研讨会 (RepL4NLP 2023) 论文集。 54–64。 17 号

### Page 18

### 段落 213 · Page 18

**EN**

Conference’17, July 2017, Washington, DC, USA Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li [168] Fangyuan Xu, Weijia Shi, and Eunsol Choi. 2023. RECOMP: Improving retrievalaugmented LMs with context compression and selective augmentation. In The Twelfth International Conference on Learning Representations . [169] Hu Xu, Bing Liu, Lei Shu, and Philip S. Yu. 2019. BERT Post-Training for Review Reading Comprehension and Aspect-based Sentiment Analysis. In NAACL-HLT (1). Association for Computational Linguistics, 2324–2335. [170] Jitao Xu, Josep-Maria Crego, and Jean Senellart. 2020.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Wenqi Fan、Yujuan Ding、Liangbo Ning、Shijie Wang、Hengyun Li、Dawei Yin、Tat-Seng Chua 和 Qing Li [168] Fangyuan Xu、Weijia Shi 和 Eunsol Choi。 2023. RECOMP：通过上下文压缩和选择性增强来改进检索增强型语言模型。在第十二届国际学习表征会议上。 [169] 徐虎，刘兵，舒雷，余菲利普。 2019. BERT 评论阅读理解和基于方面的情感分析后培训。在 NAACL-HLT (1) 中。计算语言学协会，2324-2335。 [170] 徐继涛，何塞普·玛丽亚·克雷戈，让·塞内拉特。 2020.

### 段落 214 · Page 18

**EN**

Boosting neural machine translation with similar translations. In Annual Meeting of the Association for Computational Linguistics. Association for Computational Linguistics, 1570– 1579. [171] Jing Xu, Arthur Szlam, and Jason Weston. 2022. Beyond Goldfish Memory: Long- Term Open-Domain Conversation. In ACL (1). Association for Computational Linguistics, 5180–5197. [172] Shicheng Xu, Liang Pang, Huawei Shen, Xueqi Cheng, and Tat-seng Chua. 2023. Search-in-the-chain: Towards the accurate, credible and traceable content generation for complex knowledge-intensive tasks. arXiv preprint arXiv:2304.14732 (2023).

**中文**

通过类似的翻译促进神经机器翻译。在计算语言学协会年会上。计算语言学协会，1570-1579。 [171] Jing Xu，Arthur Szlam，和 Jason Weston。 2022.超越金鱼记忆：长期开放领域对话。在 ACL (1) 中。计算语言学协会，5180–5197。 [172] 徐世成，庞亮，沉华伟，程学奇，蔡达成。 2023.链中搜索：为复杂的知识密集型任务生成准确、可信和可追踪的内容。 arXiv 预印本 arXiv:2304.14732 (2023)。

### 段落 215 · Page 18

**EN**

[173] Haoyan Yang, Zhitao Li, Yong Zhang, Jianzong Wang, Ning Cheng, Ming Li, and Jing Xiao. 2023. PRCA: Fitting Black-Box Large Language Models for Retrieval Question Answering via Pluggable Reward-Driven Contextual Adapter. In EMNLP. Association for Computational Linguistics, 5364–5375. [174] Ling Yang, Zhilin Huang, Xiangxin Zhou, Minkai Xu, Wentao Zhang, Yu Wang, Xiawu Zheng, Wenming Yang, Ron O Dror, Shenda Hong, et al. 2023. Promptbased 3d molecular diffusion models for structure-based drug design. (2023). [175] Shunyu Yao, Jeffrey Zhao, Dian Yu, Nan Du, Izhak Shafran, Karthik R. Narasimhan, and Yuan Cao. 2023.

**中文**

[173] 杨浩彦，李志涛，张勇，王建宗，程宁，李明，肖静。 2023. PRCA：通过可插入奖励驱动的上下文适配器拟合黑盒大型语言模型以进行检索问答。在 EMNLP 中。计算语言学协会，5364–5375。 [174] 杨凌，黄志林，周祥鑫，徐敏凯，张文涛，王宇，郑夏武，杨文明，Ron O Dror，洪申达，等。 2023. 用于基于结构的药物设计的基于提示的 3D 分子扩散模型。 （2023）。 [175] 姚舜宇、赵杰弗里、余殿、杜南、Izhak Shafran、Karthik R. Narasimhan、曹元。 2023 年。

### 段落 216 · Page 18

**EN**

ReAct: Synergizing Reasoning and Acting in Language Models. In ICLR. OpenReview.net. [176] Jiacheng Ye, Zhiyong Wu, Jiangtao Feng, Tao Yu, and Lingpeng Kong. 2023. Compositional exemplars for in-context learning. In International Conference on Machine Learning. PMLR, 39818–39833. [177] Yunhu Ye, Binyuan Hui, Min Yang, Binhua Li, Fei Huang, and Yongbin Li. 2023. Large Language Models are Versatile Decomposers: Decomposing Evidence and Questions for Table-based Reasoning. In SIGIR. ACM, 174–184. [178] Antonio Jimeno Yepes, Yao You, Jan Milczek, Sebastian Laverde, and Leah Li. 2024.

**中文**

ReAct：在语言模型中协同推理和行动。在 ICLR 中。 OpenReview.net。 [176]叶家成，吴志勇，冯江涛，余涛，孔令鹏。 2023.情境学习的作文范例。在国际机器学习会议上。 PMLR，39818–39833。 [177]叶云虎，惠斌源，杨敏，李斌华，黄飞，李永斌。 2023.大型语言模型是多功能分解器：分解基于表格的推理的证据和问题。在西吉尔。 ACM，174-184。 [178] 安东尼奥·吉梅诺·耶佩斯、姚游、扬·米尔切克、塞巴斯蒂安·拉维德和利亚·李。 2024 年。

### 段落 217 · Page 18

**EN**

Financial Report Chunking for Effective Retrieval Augmented Generation. arXiv preprint arXiv:2402.05131 (2024). [179] Dawei Yin, Yuening Hu, Jiliang Tang, Tim Daly, Mianwei Zhou, Hua Ouyang, Jianhui Chen, Changsung Kang, Hongbo Deng, Chikashi Nobata, et al . 2016. Ranking relevance in yahoo search. In Proceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining . 323–332. [180] Dani Yogatama, Cyprien de Masson d’Autume, and Lingpeng Kong. 2021. Adaptive semiparametric language models. Transactions of the Association for Computational Linguistics 9 (2021), 362–373.

**中文**

财务报告分块以有效检索增强生成。 arXiv 预印本 arXiv:2402.05131 (2024)。 [179] 尹大伟，胡月宁，唐吉良，蒂姆·戴利，周绵伟，欧阳华，陈建辉，康昌盛，邓洪波，野畑直，等。 2016.雅虎搜索中的相关性排名。第 22 届 ACM SIGKDD 国际知识发现和数据挖掘会议论文集。 323–332。 [180] Dani Yogatama、Cyprien de Masson d’Autume 和 Lingpeng Kong。 2021.自适应半参数语言模型。计算语言学协会汇刊 9 (2021), 362–373。

### 段落 218 · Page 18

**EN**

[181] Ori Yoran, Tomer Wolfson, Ori Ram, and Jonathan Berant. 2023. Making Retrieval-Augmented Language Models Robust to Irrelevant Context. In The Twelfth International Conference on Learning Representations . [182] Wenhao Yu, Dan Iter, Shuohang Wang, Yichong Xu, Mingxuan Ju, Soumya Sanyal, Chenguang Zhu, Michael Zeng, and Meng Jiang. 2023. Generate rather than Retrieve: Large Language Models are Strong Context Generators. In ICLR. OpenReview.net. [183] Wenhao Yu, Zhihan Zhang, Zhenwen Liang, Meng Jiang, and Ashish Sabharwal. 2023. Improving language models via plug-and-play retrieval feedback. arXiv preprint arXiv:2305.14002 (2023).

**中文**

[181] 奥里·约兰、托默·沃尔夫森、奥里·拉姆和乔纳森·贝兰特。 2023. 使检索增强语言模型对不相关的上下文具有鲁棒性。在第十二届国际学习表征会议上。 [182] 余文浩，丹·伊特尔，王硕航，徐一冲，鞠明轩，Soumya Sanyal，朱晨光，迈克尔·曾，姜孟。 2023.生成而不是检索：大型语言模型是强大的上下文生成器。在 ICLR 中。 OpenReview.net。 [183]​​于文浩，张志涵，梁振文，蒋孟，Ashish Sabharwal。 2023 年。通过即插即用检索反馈改进语言模型。 arXiv 预印本 arXiv:2305.14002 (2023)。

### 段落 219 · Page 18

**EN**

[184] Zichun Yu, Chenyan Xiong, Shi Yu, and Zhiyuan Liu. 2023. Augmentation- Adapted Retriever Improves Generalization of Language Models as Generic Plug- In. In Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) . 2421–2436. [185] Daoguang Zan, Bei Chen, Zeqi Lin, Bei Guan, Yongji Wang, and Jian-Guang Lou. 2022. When Language Model Meets Private Library. In EMNLP (Findings). Association for Computational Linguistics, 277–288. [186] Shenglai Zeng, Jiankun Zhang, Pengfei He, Yue Xing, Yiding Liu, Han Xu, Jie Ren, Shuaiqiang Wang, Dawei Yin, Yi Chang, et al. 2024.

**中文**

[184]于子春，熊陈艳，石宇，刘志远。 2023.增强自适应检索器改进了语言模型作为通用插件的泛化。计算语言学协会第 61 届年会论文集（第一卷：长论文）。 2421–2436。 [185] 赞道光，陈蓓，林泽琪，关蓓，王永吉，楼建光。 2022。当语言模型遇到私人图书馆。在 EMNLP（调查结果）中。计算语言学协会，277-288。 [186] 曾胜来，张建坤，何鹏飞，邢悦，刘一丁，徐涵，任杰，王帅强，尹大伟，常毅，等。 2024 年。

### 段落 220 · Page 18

**EN**

The Good and The Bad: Exploring Privacy Issues in Retrieval-Augmented Generation (RAG). arXiv preprint arXiv:2402.16893 (2024). [187] Boyu Zhang, Hongyang Yang, Tianyu Zhou, Muhammad Ali Babar, and Xiao- Yang Liu. 2023. Enhancing financial sentiment analysis via retrieval augmented large language models. InProceedings of the Fourth ACM International Conference on AI in Finance . 349–356. [188] Houyu Zhang, Zhenghao Liu, Chenyan Xiong, and Zhiyuan Liu. 2020. Grounded Conversation Generation as Guided Traverses in Commonsense Knowledge Graphs. In ACL. Association for Computational Linguistics, 2031–2043.

**中文**

好与坏：探索检索增强生成（RAG）中的隐私问题。 arXiv 预印本 arXiv:2402.16893 (2024)。 [187] 张博宇，杨红阳，周天宇，穆罕默德·阿里·巴巴尔，刘晓阳。 2023.通过检索增强大型语言模型来增强金融情绪分析。第四届 ACM 国际金融人工智能会议论文集。 349–356。 [188]张厚宇，刘正浩，熊陈艳，刘志远。 2020. 基础对话生成作为常识知识图中的引导遍历。在ACL中。计算语言学协会，2031-2043。

### 段落 221 · Page 18

**EN**

[189] Jiahao Zhang, Rui Xue, Wenqi Fan, Xin Xu, Qing Li, Jian Pei, and Xiaorui Liu. 2024. Linear-Time Graph Neural Networks for Scalable Recommendations. arXiv preprint arXiv:2402.13973 (2024). [190] Yunxiang Zhang, Muhammad Khalifa, Lajanugen Logeswaran, Moontae Lee, Honglak Lee, and Lu Wang. 2023. Merging generated and retrieved knowledge for open-domain QA. arXiv preprint arXiv:2310.14393 (2023). [191] Zhuosheng Zhang, Aston Zhang, Mu Li, and Alex Smola. 2023. Automatic Chain of Thought Prompting in Large Language Models. In ICLR. OpenReview.net.

**中文**

[189] 张嘉豪，薛睿，范文琪，徐鑫，李青，裴健，刘晓睿。 2024.用于可扩展建议的线性时间图神经网络。 arXiv 预印本 arXiv:2402.13973 (2024)。 [190] 张云翔、穆罕默德·哈利法、Lajanugen Logeswaran、Moontae Lee、Honglak Lee 和 Lu Wang。 2023. 合并生成和检索的知识以进行开放域 QA。 arXiv 预印本 arXiv：2310.14393 (2023)。 [191] 张卓胜，张阿斯顿，李穆，亚历克斯·斯莫拉。 2023.大型语言模型中的自动思维提示链。在 ICLR 中。 OpenReview.net。

### 段落 222 · Page 18

**EN**

[192] Penghao Zhao, Hailin Zhang, Qinhan Yu, Zhengren Wang, Yunteng Geng, Fangcheng Fu, Ling Yang, Wentao Zhang, and Bin Cui. 2024. Retrieval- Augmented Generation for AI-Generated Content: A Survey. arXiv preprint arXiv:2402.19473 (2024). [193] Ruochen Zhao, Hailin Chen, Weishi Wang, Fangkai Jiao, Xuan Long Do, Chengwei Qin, Bosheng Ding, Xiaobao Guo, Minzhi Li, Xingxuan Li, et al. 2023. Retrieving multimodal information for augmented generation: A survey. arXiv preprint arXiv:2303.10868 (2023). [194] Wayne Xin Zhao, Kun Zhou, Junyi Li, Tianyi Tang, Xiaolei Wang, Yupeng Hou, Yingqian Min, Beichen Zhang, Junjie Zhang, Zican Dong, et al. 2023.

**中文**

[192] 赵鹏浩，张海林，于勤瀚，王正仁，耿云腾，付方成，杨凌，张文涛，崔斌。 2024 年。人工智能生成内容的检索增强生成：一项调查。 arXiv 预印本 arXiv:2402.19473 (2024)。 [193] 赵若辰，陈海林，王伟石，焦方凯，杜旋龙，秦成伟，丁博胜，郭小宝，李敏智，李兴轩，等。 2023。检索多模式信息以增强发电：一项调查。 arXiv 预印本 arXiv:2303.10868 (2023)。 [194] 赵鑫、周昆、李俊毅、唐天一、王小雷、侯玉鹏、民迎千、张北辰、张俊杰、董子灿等。 2023 年。

### 段落 223 · Page 18

**EN**

A survey of large language models. arXiv preprint arXiv:2303.18223 (2023). [195] Zihuai Zhao, Wenqi Fan, Jiatong Li, Yunqing Liu, Xiaowei Mei, Yiqi Wang, Zhen Wen, Fei Wang, Xiangyu Zhao, Jiliang Tang, et al. 2024. Recommender systems in the era of large language models (llms). IEEE Transactions on Knowledge and Data Engineering (2024). [196] Zexuan Zhong, Tao Lei, and Danqi Chen. 2022. Training Language Models with Memory Augmentation. In 2022 Conference on Empirical Methods in Natural Language Processing, EMNLP 2022 . [197] Shuyan Zhou, Uri Alon, Frank F Xu, Zhengbao Jiang, and Graham Neubig. 2022.

**中文**

大型语言模型的调查。 arXiv 预印本 arXiv:2303.18223 (2023)。 [195] 赵子怀，范文琪，李佳桐，刘云清，梅小伟，王一奇，文振，王飞，赵翔宇，唐吉良，等。 2024。大语言模型（llms）时代的推荐系统。 IEEE 知识与数据工程汇刊 (2024)。 [196]钟泽轩，雷涛，陈丹琪。 2022。通过记忆增强训练语言模型。 2022 年自然语言处理经验方法会议，EMNLP 2022。 [197] Shuyan Zhou，Uri Alon，Frank F Xu，Zhengbao Jiang，Graham Neubig。 2022 年。

### 段落 224 · Page 18

**EN**

Docprompting: Generating code by retrieving the docs. In The Eleventh International Conference on Learning Representations . [198] Yin Zhu, Zhiling Luo, and Gong Cheng. 2023. Furthest Reasoning with Plan Assessment: Stable Reasoning Path with Retrieval-Augmented Large Language Models. arXiv preprint arXiv:2309.12767 (2023). [199] Yinghao Zhu, Changyu Ren, Shiyun Xie, Shukai Liu, Hangyuan Ji, Zixiang Wang, Tao Sun, Long He, Zhoujun Li, Xi Zhu, et al. 2024. REALM: RAG-Driven Enhancement of Multimodal Electronic Health Records Analysis via Large Language Models. arXiv preprint arXiv:2402.07016 (2024).

**中文**

Docprompting：通过检索文档生成代码。在第十一届学习表征国际会议上。 [198]朱银，罗志玲，程功。 2023.带有计划评估的最远推理：具有检索增强大型语言模型的稳定推理路径。 arXiv 预印本 arXiv：2309.12767 (2023)。 [199] 朱英豪，任昌宇，谢世云，刘书凯，纪航元，王子翔，孙涛，何龙，李周军，朱曦，等。 2024. REALM：通过大型语言模型进行 RAG 驱动的多模式电子健康记录分析增强。 arXiv 预印本 arXiv:2402.07016 (2024)。

### 段落 225 · Page 18

**EN**

[200] Wei Zou, Runpeng Geng, Binghui Wang, and Jinyuan Jia. 2024. PoisonedRAG: Knowledge Poisoning Attacks to Retrieval-Augmented Generation of Large Language Models. arXiv preprint arXiv:2402.07867 (2024). 18

**中文**

[200]邹伟，耿润鹏，王丙辉，贾金元。 2024. PoisonedRAG：对大型语言模型的检索增强生成的知识中毒攻击。 arXiv 预印本 arXiv:2402.07867 (2024)。 18
