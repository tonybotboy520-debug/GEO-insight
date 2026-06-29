# Information Retrieval Meets Large Language Models

- ID: 78
- 类型: pdf
- 分类: 04_academic_papers
- 主题: strategic report on IR and LLM convergence
- 原文链接: https://arxiv.org/pdf/2307.09751
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

AI Open 00 (2023) 1–17 AI Open Information Retrieval Meets Large Language Models: A Strategic Report from Chinese IR Community Qingyao AIa, Ting BAI b, Zhao CAO c, Yi CHANG d, Jiawei CHEN( )e, Zhumin CHEN f , Zhiyong CHENG g, Shoubin DONGh, Zhicheng DOU i, Fuli FENG j, Shen GAO f , Jiafeng GUO k, Xiangnan HE( ) j, Yanyan LAN a, Chenliang LIl, Yiqun LIU a, Ziyu LYU m, Weizhi MA a, Jun MA f , Zhaochun REN f , Pengjie REN f , Zhiqiang W ANGn, Mingwen W ANGo, Ji-Rong WEN i, Le WU p, Xin XIN f , Jun XU i, Dawei YIN q, Peng ZHANG( )r, Fan ZHANGl, Weinan ZHANG s, Min ZHANG a, Xiaofei ZHU t aTsinghua University, bBeijing University of Posts and Telecommunications, cHuawei Technologies Ltd.

**中文**

AI Open 00 (2023) 1–17 AI 开放信息检索遇到大语言模型：来自中国 IR 界的战略报告 Qingyao Aa, Ting BAI b, Zhao CAO c, Yi Chang d, Jiawei CHEN( )e, Zhumin CHEN f ,zhiyong Cheng g, Shoubin DONGh,zhi Cheng DOU i, Fuli FENG j, Shen GAO f , Jiafeng GUO k,何向楠( ) j, 兰艳艳 a, 李晨亮, 刘益群 a, 吕子宇 m, 马伟志 a, 马军 f, 任兆春 f, 任鹏杰 f, 王志强, 王明文, 温继荣, 吴乐 p, 辛鑫 f, 徐俊 i, 尹大伟 q, 张鹏 ( )r, 范张l、张维南、张敏、朱晓飞 t 清华大学、b 北京邮电大学、华为技术有限公司

### 段落 2 · Page 1

**EN**

Co, dJilin University, eZhejiang University, fShandong University, gShandong Artificial Intelligence Institute, hSouth China University of Technology, iRenmin University of China, jUniversity of Science and Technology of China, kInstitute of Computing Technology, Chinese Academy of Sciences, lWuhan University, mShenzhen Institute of Advanced Technology, Chinese Academy of Sciences, nShanxi University, oJiangxi Normal University, pHefei University of Technology, qBaidu Inc., rTianjin University, sShanghai Jiao Tong University, tChongqing University of Technology Abstract The research field of Information Retrieval (IR) has evolved significantly, expanding beyond traditional search to meet diverse user information needs.

**中文**

公司, d吉林大学, 浙江大学, f山东大学, g山东省人工智能研究院, h华南理工大学, 中国人民大学, j中国科学技术大学, k中国科学院计算技术研究所, l武汉大学, m中国科学院深圳先进技术研究院, n山西大学, o江西师范大学, p合肥工业大学, q百度公司, r天津大学、上海交通大学、重庆理工大学 摘要 信息检索（IR）的研究领域已经发生了显着的发展，超越了传统的搜索，以满足多样化的用户信息需求。

### 段落 3 · Page 1

**EN**

Recently, Large Language Models (LLMs) have demonstrated exceptional capabilities in text understanding, generation, and knowledge inference, opening up exciting avenues for IR research. LLMs not only facilitate generative retrieval but also offer improved solutions for user understanding, model evaluation, and user-system interactions. More importantly, the synergistic relationship among IR models, LLMs, and humans forms a new technical paradigm that is more powerful for information seeking.

**中文**

最近，大型语言模型（LLM）在文本理解、生成和知识推理方面表现出了卓越的能力，为 IR 研究开辟了令人兴奋的途径。法学硕士不仅促进生成检索，还为用户理解、模型评估和用户系统交互提供改进的解决方案。更重要的是，IR模型、LLM和人类之间的协同关系形成了一种新的技术范式，对于信息搜索来说更加强大。

### 段落 4 · Page 1

**EN**

IR models provide real-time and relevant information, LLMs contribute internal knowledge, and humans play a central role of demanders and evaluators to the reliability of information services. Nevertheless, significant challenges exist, including computational costs, credibility concerns, domain-specific limitations, and ethical considerations. To thoroughly discuss the transformative impact of LLMs on IR research, the Chinese IR community conducted a strategic workshop in April 2023, yielding valuable insights.

**中文**

IR模型提供实时且相关的信息，法学硕士贡献内部知识，而人类在信息服务的可靠性方面发挥着需求者和评估者的核心作用。然而，仍然存在重大挑战，包括计算成本、可信度问题、特定领域的限制和道德考虑。为了深入讨论法学硕士对 IR 研究的变革性影响，中国 IR 界于 2023 年 4 月举办了一次战略研讨会，产生了宝贵的见解。

### 段落 5 · Page 1

**EN**

This paper provides a summary of the workshop’s outcomes, including the rethinking of IR’s core values, the mutual enhancement of LLMs and IR, the proposal of a novel IR technical paradigm, and open challenges. © 2011 Published by Elsevier Ltd. Keywords: Information Retrieval, Language Language Models, Recommendation System 1. Introduction In the past few decades, Information Retrieval (IR) has experienced significant growth and development in both industry and academia.

**中文**

本文总结了研讨会的成果，包括对IR核心价值观的重新思考、法学硕士和IR的相互促进、新颖的IR技术范式的提出以及开放的挑战。 © 2011 Published by Elsevier Ltd. 关键词：信息检索、语言模型、推荐系统 1. 引言 在过去的几十年里，信息检索（IR）在工业界和学术界都经历了显着的增长和发展。

### 段落 6 · Page 1

**EN**

In early stage, IR research mainly focused on search, which aimed to assist users in finding 1Email: sleepyhunt@zju.edu.cn; xiangnanhe@gmail.com; pzhang@tju.edu.cn 1 arXiv:2307.09751v2 [cs.IR] 27 Jul 2023

**中文**

早期IR研究主要集中在搜索上，旨在帮助用户找到1个Email：sleepyhunt@zju.edu.cn；向南河@gmail.com； pzhang@tju.edu.cn 1 arXiv:2307.09751v2 [cs.IR] 2023 年 7 月 27 日

### Page 2

### 段落 7 · Page 2

**EN**

/ AI Open 00 (2023) 1–17 2 relevant information [1]. In recent years, the scope of IR research has expanded to encompass a wide range of online applications and scenarios [2]. This diversification is evident in the rise of recommendation systems as a prominent research area, as observed in flagship conferences ACM SIGIR from 2018 to 2023. Additionally, exciting research directions such as conversational systems, user modeling, and knowledge extraction, have also emerged [3, 4]. These advancements reflect an evolution in the core value of IR, moving beyond merely retrieving relevant documents to meeting the information needs of users [5].

**中文**

/ AI Open 00 (2023) 1–17 2 相关信息[1]。近年来，IR研究的范围已经扩大到涵盖广泛的在线应用和场景[2]。正如在 2018 年至 2023 年旗舰会议 ACM SIGIR 中所观察到的那样，推荐系统作为一个重要研究领域的崛起体现了这种多样化。此外，还出现了诸如会话系统、用户建模和知识提取等令人兴奋的研究方向 [3, 4]。这些进步反映了 IR 核心价值的演变，不再只是检索相关文档，而是满足用户的信息需求 [5]。

### 段落 8 · Page 2

**EN**

Large Language Models (LLMs) have demonstrated remarkable capabilities in various aspects of text understanding, generation, knowledge inference, and compositional generalization [6, 7]. As a result, LLMs have the potential to open up new research directions in the field of IR. These include, but are not limited to: • Enabling IR systems to generate content directly that satisfies user information needs, known as generative retrieval [8] and generative recommendation [9]. An example of this is the New Bing 1, which allows for content generation to meet user queries.

**中文**

大型语言模型 (LLM) 在文本理解、生成、知识推理和组合泛化等各个方面都表现出了卓越的能力 [6, 7]。因此，法学硕士有潜力在国际关系领域开辟新的研究方向。这些包括但不限于： • 使IR 系统能够直接生成满足用户信息需求的内容，称为生成检索[8] 和生成推荐[9]。 New Bing 1 就是一个例子，它允许生成内容来满足用户查询。

### 段落 9 · Page 2

**EN**

• Enhancing the understanding of user intents and behaviors by incorporating rich contextual information into IR system. • Creating opportunities for the development of superior indexing systems that can handle dynamic, semanticallyaware, and multi-modal data. • Providing better methods for evaluating model accuracy and interpretability in IR tasks. • Facilitating enhanced interactive experiences between users and IR systems. These advancements highlight the potential of LLMs to revolutionize various aspects of IR research and practice. Reciprocally, IR technology plays a crucial role in supporting the development of LLMs [10, 11].

**中文**

• 通过将丰富的上下文信息纳入IR 系统，增强对用户意图和行为的理解。 • 为开发能够处理动态、语义感知和多模式数据的高级索引系统创造机会。 • 提供更好的方法来评估IR 任务中的模型准确性和可解释性。 • 促进增强用户和IR 系统之间的交互体验。这些进步凸显了法学硕士彻底改变国际关系研究和实践各个方面的潜力。相反，IR 技术在支持法学硕士的发展中发挥着至关重要的作用 [10, 11]。

### 段落 10 · Page 2

**EN**

The interaction among humans, IR models, and LLMs forms a new triangular IR paradigm, as depicted in Figure 1. In this paradigm, the IR model acts as the means to acquire external knowledge, offering real-time, up-to-date, and relevant information to both LLMs and humans. LLMs contribute precise internal knowledge and information, leveraging their powerful reasoning abilities to provide high-quality responses. Humans, in their role as demanders and evaluators, play a central role in the retrieval process.

**中文**

人类、IR 模型和法学硕士之间的交互形成了一个新的三角 IR 范式，如图 1 所示。在该范式中，IR 模型充当获取外部知识的手段，为法学硕士和人类提供实时、最新的相关信息。法学硕士贡献精确的内部知识和信息，利用其强大的推理能力提供高质量的答复。人类作为需求者和评估者，在检索过程中发挥着核心作用。

### 段落 11 · Page 2

**EN**

It is important to emphasize that LLMs, without the inclusion of IR models, possess limitations in terms of short-term memory and reasoning. These limitations could result in the lack of e ffective integration of new and existing knowledge, hindering LLMs’ ability to provide the information that humans need. The IR model, functioning as a “knowledge base” equipped with matching and retrieval capabilities, addresses these limitations by compensating for the lack of factual consistency and long-term memory in LLMs.

**中文**

需要强调的是，如果不包含 IR 模型，法学硕士在短期记忆和推理方面存在局限性。这些限制可能导致新知识和现有知识缺乏有效整合，从而阻碍法学硕士提供人类所需信息的能力。 IR 模型作为配备匹配和检索功能的“知识库”，通过补偿法学硕士缺乏事实一致性和长期记忆来解决这些限制。

### 段落 12 · Page 2

**EN**

This combination of “knowledge+reasoning” establishes a dual-wheel drive, enabling a more intelligent and reliable information service system for humans [12, 10]. While LLMs for IR hold promise, they also face significant challenges that cannot be ignored: • High computational costs: LLMs for IR require substantial computational resources, which can limit their use and research by small and medium-sized companies and institutions. Furthermore, deploying models on terminal devices and ensuring real-time performance can be challenging [13].

**中文**

这种“知识+推理”的结合建立了双轮驱动，为人类提供了更加智能、可靠的信息服务系统[12, 10]。虽然 IR 法学硕士前景广阔，但它们也面临着不容忽视的重大挑战： • 高计算成本：IR 法学硕士需要大量计算资源，这可能会限制中小型公司和机构对其的使用和研究。此外，在终端设备上部署模型并确保实时性能可能具有挑战性[13]。

### 段落 13 · Page 2

**EN**

• Credibility concerns: The credibility of LLMs for IR is relatively low, as they have been found to provide misleading explanations, incorrect answers, and unreliable information sources. This can undermine people’s trust in LLMs [14]. • Performance limitations in specific fields: LLMs may struggle to perform well in specific domains due to the lack of high-quality datasets, di fferences in data representation, and other related issues. The limited domainspecific knowledge hampers the rapid implementation and application of LLMs [15, 16]. 1https://www.bing.com/new 2

**中文**

• 可信度问题：IR 法学硕士的可信度相对较低，因为人们发现它们提供了误导性的解释、不正确的答案和不可靠的信息来源。这可能会削弱人们对法学硕士的信任[14]。 • 特定领域的表现限制：由于缺乏高质量数据集、数据表示差异以及其他相关问题，法学硕士可能难以在特定领域表现良好。有限的特定领域知识阻碍了法学硕士的快速实施和应用[15, 16]。 1https://www.bing.com/new 2

### Page 3

### 段落 14 · Page 3

**EN**

/ AI Open 00 (2023) 1–17 3 Humans Big Models IR ModelsInformation Needs User Machine Internal Knowledge and Reasoning Relevant and Real-time External Knowledge Figure 1. Our proposed new IR technical paradigm introduces three key elements: Humans, IR models, and LLMs. The synergistic relationship among them not only facilitates mutual enhancement but also enables the fulfillment of new tasks as an organic whole. • Ethical and moral considerations: The emergence of generative IR systems raises the requirements for ethical and moral evaluation standards.

**中文**

/ AI Open 00 (2023) 1–17 3 人类大模型 IR 模型信息需要用户机器内部知识和推理相关且实时的外部知识 图 1.我们提出的新 IR 技术范式引入了三个关键要素：人类、IR 模型和法学硕士。它们之间的协同关系，不仅有利于相互促进，而且可以作为一个有机整体完成新的任务。 • 伦理和道德考虑：生成IR系统的出现提出了对伦理和道德评价标准的要求。

### 段落 15 · Page 3

**EN**

Ensuring fairness, impartiality, and ethics in the generated content is a significant challenge. It is inherently difficult to guarantee that LLMs meet these regulatory and ethical requirements [17, 18]. Given the flourishing research in the IR field and the promising opportunities brought about by LLMs, it is a favorable moment to envision the future advancements in IR. To this end, the Chinese IR community organized a strategic workshop on April 14th and 15th, 2023, aiming to explore future opportunities and challenges.

**中文**

确保生成内容的公平、公正和道德是一项重大挑战。保证法学硕士满足这些监管和道德要求本质上是困难的[17, 18]。鉴于国际关系领域研究的蓬勃发展以及法学硕士带来的广阔机遇，现在是展望国际关系未来发展的有利时机。为此，中国IR界于2023年4月14日至15日组织了战略研讨会，旨在探讨未来的机遇和挑战。

### 段落 16 · Page 3

**EN**

This paper presents the key findings and conclusions drawn from the workshop, including the rethinking of the core values of IR in Section 2, a discussion of how LLMs and IR can mutually enhance each other in Section 3 and Section 4, the new IR paradigm of fusing humans, LLMs, and IR in Section 5, and a discussion of open challenges and future directions in Section 6. 2. Rethinking Core Values of IR Before delving into the e ffects of LLMs on IR research, it is crucial to rethink the IR discipline itself.

**中文**

本文介绍了研讨会得出的主要发现和结论，包括在第 2 节中重新思考 IR 的核心价值观，在第 3 节和第 4 节中讨论法学硕士和 IR 如何相互促进，在第 5 节中讨论融合人类、法学硕士和 IR 的新 IR 范式，以及在第 6 节中讨论开放挑战和未来方向。 2. 在深入研究法学硕士对 IR 的影响之前，重新思考 IR 的核心价值IR 研究中，重新思考 IR 学科本身至关重要。

### 段落 17 · Page 3

**EN**

This contemplation leads us to ponder the following questions: Firstly, what is the fundamental contribution of IR, as a scientific discipline, to other domains? Secondly, considering its extensive development over the past decades, what are the boundaries and extensions of IR? These questions are intended to promote comprehension of the fundamental principles of IR, and foster the integration of LLMs into IR while preserving its essence. 2.1. Scientific Connotation of IR Classical IR concerns the retrieval of the information that satisfies a user’s information need from the target corpus.

**中文**

这种思考引导我们思考以下问题：首先，国际关系作为一门科学学科对其他领域的根本贡献是什么？其次，考虑到近几十年来的广泛发展，IR的边界和外延是什么？这些问题旨在促进对国际关系基本原则的理解，并促进法学硕士融入国际关系，同时保留其本质。 2.1.信息检索的科学内涵 经典信息检索涉及从目标语料库中检索满足用户信息需求的信息。

### 段落 18 · Page 3

**EN**

Therefore, user, ranking, and corpus are the fundamental concepts in the IR discipline. In the light of this, it is important to re-examine the scientific connotation of IR from the three aspects. User Perspective. Users are the core part of IR [19, 20], since an IR system is supposed to serve users by satisfying their information needs. Therefore, user understanding is a fundamental problem in IR, and the community has made decades-long progress in user understanding. The studies of user understanding in IR mainly concentrate on two sides, respectively user intent understanding and user behavior modeling.

**中文**

因此，用户、排名和语料库是IR学科中的基本概念。鉴于此，有必要从三个方面重新审视IR的科学内涵。用户视角。用户是信息检索的核心部分[19, 20]，因为信息检索系统应该通过满足用户的信息需求来服务用户。因此，用户理解是 IR 的一个基本问题，社区在用户理解方面已经取得了数十年的进步。 IR中用户理解的研究主要集中在两个方面，分别是用户意图理解和用户行为建模。

### 段落 19 · Page 3

**EN**

• User intent understanding plays a central role in IR. Commercial search engines like Google 2 and Bing 3, have 2https://www.google.com 3https://www.bing.com 3

**中文**

• 用户意图理解在IR 中发挥着核心作用。商业搜索引擎，如 Google 2 和 Bing 3，有 2https://www.google.com 3https://www.bing.com 3

### Page 4

### 段落 20 · Page 4

**EN**

/ AI Open 00 (2023) 1–17 4 evolved from keyword semantic matching to user intent optimization in recent decades. Understanding user intent is the first step for better user experiences, which has been broadly studied in various IR applications, e.g., web search [21, 22], product search in e-commerce [23], community question answering [24], etc. • User behavior modeling is to comprehensively understand and model user behaviors when interacting with IR systems.

**中文**

/ AI Open 00 (2023) 1–17 4 近几十年来从关键词语义匹配发展到用户意图优化。了解用户意图是获得更好用户体验的第一步，这在各种IR应用中得到了广泛的研究，例如网络搜索[21, 22]、电子商务中的产品搜索[23]、社区问答[24]等。 • 用户行为建模是全面理解和建模与IR系统交互时的用户行为。

### 段落 21 · Page 4

**EN**

IR community has studied diverse and multi-dimensional user behaviors including user interaction behaviors [25, 26], sequential behaviors [27, 28], mobility behaviors [29, 30] and social behaviors [31]. User behavior modeling helps to inject personalization into IR systems. The techniques of user understanding in IR have provided valuable insights for other research domains. In natural language processing (NLP), user intent understanding is the preliminary step to make further actions in task-oriented dialogue systems [32]. User profiling and personalization are also utilized to develop persona-based dialogue systems [33, 34].

**中文**

IR社区研究了多样化、多维度的用户行为，包括用户交互行为[25, 26]、顺序行为[27, 28]、移动行为[29, 30]和社交行为[31]。用户行为建模有助于将个性化注入 IR 系统。 IR 中的用户理解技术为其他研究领域提供了宝贵的见解。在自然语言处理（NLP）中，用户意图理解是在面向任务的对话系统中采取进一步行动的第一步[32]。用户分析和个性化也用于开发基于角色的对话系统 [33, 34]。

### 段落 22 · Page 4

**EN**

In social computing, user modeling is an important area in the design of personalized incentive mechanisms for encouraging participation [35]. Ranking Perspective. Ranking lies at the core part of IR research by providing an ordering of items towards user’s information need [36, 37]. The formats of items are various, including but not limited to textual documents, images, and videos. The problem is usually formulated as ranking a collection of items that match the given query or context, according to some criterion like relevance and recency. Most IR systems are supported by a ranking module.

**中文**

在社交计算中，用户建模是设计鼓励参与的个性化激励机制的重要领域[35]。排名视角。排名是 IR 研究的核心部分，它根据用户的信息需求提供项目的排序[36, 37]。项目的格式多种多样，包括但不限于文本文档、图像、视频。该问题通常被表述为根据相关性和新近度等标准对与给定查询或上下文匹配的项目集合进行排名。大多数 IR 系统都由排名模块支持。

### 段落 23 · Page 4

**EN**

Different techniques have been used for constructing ranking models, from traditional ranking models to machine learning methods. The traditional ranking models include vector space models and probabilistic models (e.g. BM25 [38]). The machine learning methods include the earliest learning to rank models (e.g. Rankboost [39] and LambdaMart [40]) and the recent neural ranking models such as Deep Structured Semantic Models (DSSM) [41] and DeepRank [42]. Ranking models have been extensively exploited in many IR applications such as ad-hoc retrieval [43, 44, 45], recommender systems [46, 47], community question answering [48, 49], etc.

**中文**

从传统的排名模型到机器学习方法，不同的技术被用于构建排名模型。传统的排序模型包括向量空间模型和概率模型（例如BM25[38]）。机器学习方法包括最早的学习排序模型（例如Rankboost [39]和LambdaMart [40]）和最近的神经排序模型，例如深度结构化语义模型（DSSM）[41]和DeepRank [42]。排名模型已在许多 IR 应用中得到广泛利用，例如临时检索 [43, 44, 45]、推荐系统 [46, 47]、社区问答 [48, 49] 等。

### 段落 24 · Page 4

**EN**

It’s worth noting that ranking is not restricted to IR alone, as it also has applications in a diverse range of other research fields. For example, ChatGPT [50] collects comparison samples and utilizes a ranking labeler to train the reward model when aligning with user intents. In computational biology, learning-to-rank algorithms have been exploited to rank the candidate 3-D structures in protein structure prediction [51]. Corpus Perspective. For the corpus perspective, the connotation of IR lies in conducting e ffective search efficiently from a large volume of multi-modal information corpus [1].

**中文**

值得注意的是，排名不仅限于 IR，因为它还可以应用于其他各种研究领域。例如，ChatGPT [50] 收集比较样本，并利用排名标签器在与用户意图一致时训练奖励模型。在计算生物学中，学习排序算法已被用来对蛋白质结构预测中的候选 3-D 结构进行排序 [51]。语料库视角。从语料库的角度来看，IR的内涵在于从大量的多模态信息语料库中高效地进行有效的搜索[1]。

### 段落 25 · Page 4

**EN**

Such connotation mainly lies in the following two folds: • Effective corpus representation. Conventional IR systems represent the documents with bag-of-words or TF- IDF methods [1]. Deep learning methods (e.g., dense retrieval) empowers the IR system to represent multimodal corpus such as images and videos with dense latent vectors, which has largely improved the retrieval results and broadened the application scope of IR [52, 53]. Recently, contrastive learning and self-supervised learning further improve the learning of corpus representation [54]. • Efficient retrieval infrastructure.

**中文**

这种内涵主要体现在以下两个方面： • 有效的语料表征。传统的 IR 系统使用词袋或 TF-IDF 方法来表示文档 [1]。深度学习方法（例如密集检索）使IR系统能够用密集潜在向量表示图像和视频等多模态语料库，这在很大程度上改善了检索结果并拓宽了IR的应用范围[52, 53]。最近，对比学习和自监督学习进一步提高了语料库表示的学习[54]。 • 高效的检索基础设施。

### 段落 26 · Page 4

**EN**

The infrastructure of IR involves fundamental facilities to construct an IR system, including but not limited to building dictionaries, indexing, scoring, distributed search, and caching [19]. Such infrastructure determines how to organize the information source and thus largely affect the efficiency of IR [19]. LLMs and generative IR [55] shed new lights to reform the retrieval infrastructure. 2.2. Boundaries and Extensions of IR Although the growth of Web and mobile technology has greatly advanced the development of IR, it also results in some limitations.

**中文**

IR的基础设施涉及构建IR系统的基本设施，包括但不限于构建词典、索引、评分、分布式搜索和缓存[19]。这种基础设施决定了如何组织信息源，从而在很大程度上影响信息检索的效率[19]。法学硕士和生成式 IR [55] 为改革检索基础设施提供了新的思路。 2.2. IR 的边界和扩展 尽管网络和移动技术的发展极大地促进了 IR 的发展，但它也带来了一些局限性。

### 段落 27 · Page 4

**EN**

A common misconception is that IR simply involves ranking a set of objects in cyberspace, which is an inaccurate and narrow view. As such, it is crucial to reconsider the boundaries and extensions of IR from various perspectives, including the input, process, output, and environment. 4

**中文**

一个常见的误解是，IR 仅仅涉及对网络空间中的一组对象进行排名，这是一种不准确且狭隘的观点。因此，从输入、过程、输出、环境等多个角度重新思考IR的边界和外延至关重要。 4

### Page 5

### 段落 28 · Page 5

**EN**

/ AI Open 00 (2023) 1–17 5 Ranking or Generation?. The primary focus of classical IR pertains to the ordering of items based on the information need, such as the query in search engines or the context of recent interactions in recommender systems. The advancement of large-scale generative models such as GPT [56] and Diffusion Models [57] has expanded the content space, allowing exploration beyond existing sets of content through generation. Integrating the generation channel for information seeking opens up new paradigms in IR systems, such as generative search and recommendation [9].

**中文**

/ AI Open 00 (2023) 1–17 5 排名还是一代？经典 IR 的主要关注点涉及基于信息需求的项目排序，例如搜索引擎中的查询或推荐系统中最近交互的上下文。 GPT [56] 和扩散模型 [57] 等大规模生成模型的进步扩大了内容空间，允许通过生成来探索现有内容集之外的内容。集成信息搜索的生成通道开辟了 IR 系统的新范式，例如生成搜索和推荐 [9]。

### 段落 29 · Page 5

**EN**

However, this extension presents challenges to building IR systems in infrastructure, algorithm, evaluation, etc. For instance, it calls for the infrastructure to accommodate generative models at a large scale and distribute the content generated on the fly in an e fficient manner, especially for multi-media content such as micro-videos. Additionally, it calls for algorithm innovation on the alignment of generative models to IR tasks, the aggregation of ranking and generation results, and the joint optimization of ranking and generation models.

**中文**

然而，这种扩展对构建IR系统在基础设施、算法、评估等方面提出了挑战。例如，它要求基础设施能够容纳大规模的生成模型，并以高效的方式分发动态生成的内容，特别是对于微视频等多媒体内容。此外，它还要求在生成模型与IR任务的匹配、排序和生成结果的聚合以及排序和生成模型的联合优化等方面进行算法创新。

### 段落 30 · Page 5

**EN**

Furthermore, evaluation techniques must also be extended to accommodate unlimited content and emphasize new perspectives such as fidelity checking. For Human or For Machine?. IR systems have been designed to assist human users to access information resources. However, with the increasing prevalence of AI models, particularly LLMs, the user base of IR systems could potentially be expanded to include intelligent machines.

**中文**

此外，评估技术还必须扩展以适应无限的内容并强调新的视角，例如保真度检查。对于人类还是对于机器？ IR 系统旨在帮助人类用户访问信息资源。然而，随着人工智能模型（尤其是法学硕士）的日益普及，IR 系统的用户群可能会扩大到包括智能机器。

### 段落 31 · Page 5

**EN**

This has led to the emergence of a growing body of research referred to as IR-augmented methods or retrieval-enhanced machine learning (REML) [58] in various communities such as computer vision[59], natural language processing [60], and machine learning[61]. From a conceptual perspective, IR systems can be regarded as a memory and access system for external data, information, or knowledge, capable of serving as a generic supporting technique for either humans or machines.

**中文**

这导致计算机视觉 [59]、自然语言处理 [60] 和机器学习 [61] 等各个领域出现越来越多的研究，称为 IR 增强方法或检索增强机器学习 (REML) [58]。从概念角度来看，红外系统可以被视为外部数据、信息或知识的存储和访问系统，能够作为人类或机器的通用支持技术。

### 段落 32 · Page 5

**EN**

Nevertheless, the shift from human to machine poses a multitude of research challenges throughout the entire process of the IR system, including indexing, representation, retrieval, ranking, and feedback. Additionally, there are many research issues to be addressed regarding the learning, evaluation, and deployment of IR technology in conjunction with AI models. Despite these challenges, it is encouraging to anticipate that IR could become a ubiquitous component of the AI paradigm in the future, providing valuable support to society at large. For Finding or For Decision?. IR systems have long benefited people in finding desired information.

**中文**

然而，从人类到机器的转变在信息检索系统的整个过程中带来了许多研究挑战，包括索引、表示、检索、排名和反馈。此外，关于 IR 技术与人工智能模型结合的学习、评估和部署，还有许多研究问题需要解决。尽管存在这些挑战，但令人鼓舞的是，预计 IR 未来可能成为人工智能范式的普遍组成部分，为整个社会提供宝贵的支持。为了寻找还是为了决定？红外系统长期以来一直帮助人们寻找所需的信息。

### 段落 33 · Page 5

**EN**

For the extension of IR, the system should also support complicated, explainable, and long-term information seeking to help users with reasonable decision-making suggestions [62]. To accomplish this goal, a retrieval system should be aware of the user context in which the information need is to be placed [63]. For complex decision-making tasks, the system is expected to sca ffold the task step-by-step [64]. The system should also provide transparent retrieval process and explainable results to provide reasonable decision-making supports [65]. Besides, understanding how people make decisions is also important.

**中文**

对于IR的扩展，系统还应该支持复杂的、可解释的、长期的信息寻求，以帮助用户提供合理的决策建议[62]。为了实现这一目标，检索系统应该了解信息需求所在的用户上下文[63]。对于复杂的决策任务，系统期望逐步支撑任务[64]。该系统还应提供透明的检索过程和可解释的结果，以提供合理的决策支持[65]。此外，了解人们如何做出决策也很重要。

### 段落 34 · Page 5

**EN**

Collaboration with other communities will likely be necessary to make progress in decision understanding. These communities may include human-computer interaction, behavioural economics, psychology, cognitive science, as well as specific domain communities like the clinical communities [66, 67]. Finally, placing IR into LLMs to provide AI-Generated Actions (AIGA) is also an emerging topic for the extension of IR [68]. Going beyond Cyberspace?. IR systems have conventionally emphasized digital content within the realm of cyberspace.

**中文**

为了在决策理解方面取得进展，可能需要与其他社区合作。这些社区可能包括人机交互、行为经济学、心理学、认知科学以及临床社区等特定领域社区[66, 67]。最后，将 IR 放入 LLM 中以提供人工智能生成的操作（AIGA）也是 IR 扩展的一个新兴主题[68]。超越网络空间？ IR 系统传统上强调网络空间领域内的数字内容。

### 段落 35 · Page 5

**EN**

However, advancements in human-computer interaction [69], unmanned vehicles [70], and robotics [71] enable us to envision the retrieval of contents in the physical world. For instance, the extended IR system may explore information in the physical world such as the wind speed around and the source of noise. Further extensions may incorporate the search and delivery of physical items. These extensions build on the aforementioned ranking-generation hybrids, human-machine hybrids, and finding-decision hybrids. Moreover, new concepts around interaction interfaces, system architecture, and feedback mechanisms will arise.

**中文**

然而，人机交互[69]、无人驾驶车辆[70]和机器人技术[71]的进步使我们能够设想在物理世界中检索内容。例如，扩展的红外系统可以探索物理世界中的信息，例如周围的风速和噪声源。进一步的扩展可能包括物理物品的搜索和交付。这些扩展建立在前面提到的排名生成混合、人机混合和查找决策混合的基础上。此外，围绕交互界面、系统架构和反馈机制的新概念将会出现。

### 段落 36 · Page 5

**EN**

Towards these ends, we may open up more cross-domain research directions and entangle IR with various emerging techniques in other fields such as Metaverse [72] and Embodied Artificial Intelligence [73]. As a result, there will be many research opportunities regarding the development, operation, maintenance, and regulation of such IR systems, increasing the value of the IR industry remarkably. 3. Large Language Models for IR IR systems have long been divided into five major components: user modeling, indexing, matching/ranking, evaluation, and user interaction.

**中文**

为此，我们可能会开辟更多跨领域的研究方向，并将IR与其他领域的各种新兴技术结合起来，例如Metaverse [72]和Embodied Artificial Intelligence [73]。因此，将有许多关于此类 IR 系统的开发、运行、维护和监管的研究机会，从而显着增加 IR 行业的价值。 3. IR 的大型语言模型 IR 系统长期以来被分为五个主要部分：用户建模、索引、匹配/排名、评估和用户交互。

### 段落 37 · Page 5

**EN**

By pre-training on large-scale corpora and fine-tuning to follow human instructions, 5

**中文**

通过对大规模语料库进行预训练并进行微调以遵循人类指令，5

### Page 6

### 段落 38 · Page 6

**EN**

/ AI Open 00 (2023) 1–17 6 LLMs have demonstrated superior capability in language understanding, generation, interaction, and knowledge reasoning [74]. Therefore, it is reasonable to anticipate that LLMs will considerably augment the major IR components from various perspectives. In this section, we discuss the possibilities of LLMs for each major IR component. 3.1. User Modeling User modeling aims to accurately represent users and their information needs by understanding their characteristics, preferences, and behaviors [75, 76, 77, 78].

**中文**

/ AI Open 00 (2023) 1–17 6 名法学硕士在语言理解、生成、交互和知识推理方面表现出了卓越的能力 [74]。因此，可以合理地预期法学硕士将从各个角度大大增强国际关系的主要组成部分。在本节中，我们将讨论法学硕士对于每个主要 IR 组成部分的可能性。 3.1.用户建模 用户建模旨在通过了解用户的特征、偏好和行为来准确地表示用户及其信息需求[75,76,77,78]。

### 段落 39 · Page 6

**EN**

In view of the acknowledged capabilities of LLMs, we enumerate several potential directions that LLMs can enhance user modeling. • Language Understanding. Most basically, LLMs can enhance the understanding of user queries, enabling more accurate analysis and leading to more relevant search results. • Behavior Understanding. LLMs allow the analyses of user behaviors in the semantic level of item content, offering a comprehensive understanding of preferences and behaviors. By analyzing data like click-stream, search log, and interaction history, models can identify patterns and relationships, resulting in more accurate user models.

**中文**

鉴于LLM的公认能力，我们列举了LLM可以增强用户建模的几个潜在方向。 • 语言理解。最根本的是，法学硕士可以增强对用户查询的理解，从而实现更准确的分析并产生更相关的搜索结果。 • 行为理解。法学硕士允许在项目内容的语义层面上分析用户行为，提供对偏好和行为的全面理解。通过分析点击流、搜索日志和交互历史记录等数据，模型可以识别模式和关系，从而产生更准确的用户模型。

### 段落 40 · Page 6

**EN**

• Personalization. LLMs can build comprehensive user models, incorporating various characteristics and preferences. By analyzing social media activity, online behavior, and integrating with IoT devices, models can consider the factors like physical environment and emotional states, leading to more personalized recommendations. • Conversational Interfaces. LLMs faciliate more natural and seamless interactions, generating context-aware responses. Conversational interfaces can incorporate sentiment analysis and emotional response generation, thereby enhancing personalized and engaging user experiences. • Hybrid Modeling.

**中文**

• 个性化。法学硕士可以构建综合的用户模型，纳入各种特征和偏好。通过分析社交媒体活动、在线行为以及与物联网设备集成，模型可以考虑物理环境和情绪状态等因素，从而提供更加个性化的推荐。 • 对话界面。法学硕士促进更自然和无缝的交互，产生上下文感知的响应。对话界面可以结合情绪分析和情绪反应生成，从而增强个性化和引人入胜的用户体验。 • 混合建模。

### 段落 41 · Page 6

**EN**

Combining LLMs with rule-based or collaborative filtering models can yield stronger hybrid models. Such hybrid modeling unifies the strengths of different approaches, improving the personalization and accuracy of search and recommendation [79, 80]. The advancement of LLMs is expected to significantly enhance the user modeling in IR systems. Nonetheless, certain challenges, such as data privacy, biases in data and models, and the need for extensive training data, need to be tackled. Addressing these challenges is imperative to fully exploit the potential benefits of LLMs for user modeling in IR, while mitigating any potential negative effects.

**中文**

将法学硕士与基于规则或协作过滤模型相结合可以产生更强大的混合模型。这种混合建模结合了不同方法的优点，提高了搜索和推荐的个性化和准确性[79, 80]。法学硕士的进步预计将显着增强红外系统中的用户建模。尽管如此，仍需要解决某些挑战，例如数据隐私、数据和模型的偏差以及对大量训练数据的需求。应对这些挑战对于充分利用法学硕士在 IR 中用户建模的潜在优势，同时减轻任何潜在的负面影响至关重要。

### 段落 42 · Page 6

**EN**

3.2. Indexing The emergence of LLMs provides the basis for generative retrieval, a new retrieval paradigm where the indexing component is dramatically changed. Recently, dense retrieval has been extensively studied and the approaches based on the standard MIPS index and nearest neighbor search are common [52]. Given the success of Transformers as a good associative memory store or search index, Tay et al. [55] propose a novel architecture called differentiable search index (DSI) where the index is stored in the model parameters. DSI uses LLMs to directly learn the mapping of queries to relevant document IDs.

**中文**

3.2.索引 法学硕士的出现为生成检索提供了基础，这是一种新的检索范式，其中索引组件发生了巨大的变化。最近，密集检索得到了广泛的研究，基于标准 MIPS 索引和最近邻搜索的方法很常见 [52​​]。鉴于 Transformers 作为良好的关联记忆存储或搜索索引的成功，Tay 等人。 [55]提出了一种称为可微搜索索引（DSI）的新颖架构，其中索引存储在模型参数中。 DSI 使用 LLM 直接学习查询到相关文档 ID 的映射。

### 段落 43 · Page 6

**EN**

It enables the model’s internal memory to act as an index, thus greatly simplifying the entire retrieval process. Inspired by the work of DSI, we identify some directions that LLMs will change the technology of indexing: • From Static to Dynamic. Indexing systems based on LLMs need be dynamic, as all corpus information is encoded within the LLM parameters. Incremental index updates are a specific instance of model updates, as noted in the study by [81]. • From Keyword-based to Semantics-oriented. Indexing systems based on LLMs should be semantic.

**中文**

它使模型的内存可以充当索引，从而大大简化了整个检索过程。受到 DSI 工作的启发，我们确定了法学硕士将改变索引技术的一些方向： • 从静态到动态。基于 LLM 的索引系统需要是动态的，因为所有语料库信息都编码在 LLM 参数内。正如[81]的研究中指出的，增量索引更新是模型更新的一个特定实例。 • 从基于关键字到面向语义。基于法学硕士的索引系统应该是语义化的。

### 段落 44 · Page 6

**EN**

Thanks to the powerful contextual modeling capabilities of LLMs, indexing systems based on LLMs are able to find the documents that are related to the query in a more nuanced way. • From Uni-modal to Multi-modal. Indexing systems utilizing LLMs have the potential to be multi-modal. The development of multi-modal LLMs will facilitate the indexing systems capable of indexing various modalities of data in a unified manner, including but not limited to texts, images, and videos. 6

**中文**

得益于LLM强大的上下文建模能力，基于LLM的索引系统能够以更细致的方式找到与查询相关的文档。 • 从单式到多式。利用法学硕士的索引系统有可能是多模式的。多模态法学硕士的发展将促进索引系统能够以统一的方式索引各种模态的数据，包括但不限于文本、图像和视频。 6

### Page 7

### 段落 45 · Page 7

**EN**

/ AI Open 00 (2023) 1–17 7 3.3. Matching /Ranking LLMs have demonstrated remarkable capability to understand and rank complex content, including both singlemodal and multi-modal data. In this part, we focus on two topics: (1) If generative models can already provide exact answers, is ranking still necessary? (2) What are the future research directions in the ranking, and what problems remain to be solved? While generative LLMs can provide coherent answers to user queries, users still need to know which document, image, or webpage is most relevant to their query, so as to verify the answer generated by the LLM.

**中文**

/ AI 开放 00 (2023) 1–17 7 3.3。匹配/排名法学硕士展示了理解和排名复杂内容（包括单模态和多模态数据）的卓越能力。在这一部分中，我们关注两个主题：（1）如果生成模型已经可以提供准确的答案，那么排名还有必要吗？ （2）排名未来的研究方向是什么，还有哪些问题需要解决？虽然生成式法学硕士可以为用户查询提供连贯的答案，但用户仍然需要知道哪些文档、图像或网页与其查询最相关，以便验证法学硕士生成的答案。

### 段落 46 · Page 7

**EN**

The ranking results from a retrieval system can improve the interpretability of LLM, and provide the trustworthy information to support the answer generation. The retrieval system typically acts as a plugin to LLMs [82, 83], providing knowledge acquisition abilities. In future research, LLMs offer many interesting directions to explore in ranking. Under the generative paradigm, we should prioritize ranking and improve the ranking of results to ensure a good user experience and high satisfaction. This is also a more essential goal of ranking in IR. When ranking search results, we should focus on the integrity of the returned results.

**中文**

检索系统的排名结果可以提高LLM的可解释性，并为支持答案生成提供可信的信息。检索系统通常充当法学硕士[82, 83]的插件，提供知识获取能力。在未来的研究中，法学硕士提供了许多有趣的排名方向可供探索。在生成范式下，我们应该优先考虑排名，提高结果的排名，以保证良好的用户体验和高满意度。这也是IR排名更本质的目标。在对搜索结果进行排名时，我们应该关注返回结果的完整性。

### 段落 47 · Page 7

**EN**

Instead of simply returning a ranking list based on relevance, the model should return the information that is more integrated and relevant to users’ real needs. In terms of ranking evaluation, existing methods are designed for the form of returning a list of documents, which is no longer suitable under the generative paradigm. There are promising directions for future research in the field of ranking. An example is to leverage the LLMs as the human simulator to measure the user satisfaction and experience of a ranking method [84]. 3.4.

**中文**

模型不应简单地返回基于相关性的排名列表，而应返回更完整、更贴近用户真实需求的信息。在排名评估方面，现有方法都是针对返回文档列表的形式设计的，这在生成范式下已经不再适用。排名领域的未来研究有很多有前途的方向。一个例子是利用法学硕士作为人体模拟器来衡量排名方法的用户满意度和体验[84]。 3.4.

### 段落 48 · Page 7

**EN**

Evaluation For validate the e ffectiveness of LLM-enhanced IR approaches, it is essential to develop proper metrics and datasets. Conventional IR metrics, such as Precision and Recall, Mean Reciprocal Rank (MRR, [85]), Mean Average Precision (MAP, [86]), Normalized discounted cumulative gain (nDCG, [87, 88]), still play a critical role in IR model evaluation. However, with the wide application of LLMs in IR, tailored evaluation strategies become essential to justify the effectiveness of LLMs. To this end, some characteristics needed to be emphasized including: • Robustness.

**中文**

评估 为了验证法学硕士增强型 IR 方法的有效性，开发适当的指标和数据集至关重要。传统的 IR 指标，例如精度和召回率、平均倒数排名 (MRR, [85])、平均平均精度 (MAP, [86])、归一化贴现累积增益 (nDCG, [87, 88]) 在 IR 模型评估中仍然发挥着关键作用。然而，随着法学硕士在国际关系学中的广泛应用，量身定制的评估策略对于证明法学硕士的有效性变得至关重要。为此，需要强调一些特性，包括： • 稳健性。

### 段落 49 · Page 7

**EN**

Many models are sensitive to distributional differences between training and test data [89, 90]. It is eager to see the generalization of LLM-enhanced IR models in out-of-distribution (OOD) scenarios. • Interpretability. Neural IR models rely on dense document representations, and suffer from poor interpretability, which is different from previous sparse IR models (e.g., BM25) with explicit term matching [91]. • Efficiency. LLMs may require additional training or fine-tuning to adapt to IR tasks, and storage is also a severe bottleneck in the training scenarios [92, 93]. • Reliability.

**中文**

许多模型对训练数据和测试数据之间的分布差异很敏感 [89, 90]。它渴望看到 LLM 增强型 IR 模型在分布外 (OOD) 场景中的推广。 • 可解释性。神经 IR 模型依赖于密集的文档表示，并且可解释性较差，这与之前具有显式术语匹配的稀疏 IR 模型（例如 BM25）不同[91]。 • 效率。 LLM 可能需要额外的训练或微调以适应 IR 任务，并且存储也是训练场景中的严重瓶颈 [92, 93]。 • 可靠性。

### 段落 50 · Page 7

**EN**

LLMs are capable of directly retrieving knowledge from the model itself and generating results for users. However, they are vulnerable to adversarial inputs and some small character changes would negatively affect its reliability [94]. 3.5. Interaction The interaction between users and traditional search engines typically involves three steps [95]. First, a user submits a query generally expressed as keywords. Then, the search engine processes the query, retrieves its index and presents the results in the form of a list. Finally, the user browses the results and clicks on the most relevant links to the query.

**中文**

法学硕士能够直接从模型本身检索知识并为用户生成结果。然而，它们很容易受到对抗性输入的影响，并且一些小的字符变化会对其可靠性产生负面影响[94]。 3.5.交互 用户和传统搜索引擎之间的交互通常涉及三个步骤[95]。首先，用户提交通常表示为关键字的查询。然后，搜索引擎处理查询，检索其索引并以列表的形式呈现结果。最后，用户浏览结果并单击与查询最相关的链接。

### 段落 51 · Page 7

**EN**

With the development of conversational technology, conversational search has become a new retrieval paradigm [96, 97]. The retrieval process has become an iterative form of multiple rounds of dialogue. A user initiates the conversation by asking a question in natural language. The search engine processes the user’s input, retrieves its index and generates a response. Then, the user may provide additional information or ask follow-up questions, and the search engine continues to process the user’s input and generate responses until the user is satisfied. LLMs [7] have the potential to overturn the interaction between users and IR systems.

**中文**

随着会话技术的发展，会话搜索已成为一种新的检索范式[96, 97]。检索过程变成了多轮对话的迭代形式。用户通过用自然语言提出问题来发起对话。搜索引擎处理用户的输入，检索其索引并生成响应。然后，用户可以提供附加信息或提出后续问题，搜索引擎继续处理用户的输入并生成响应，直到用户满意为止。法学硕士 [7] 有可能颠覆用户和 IR 系统之间的交互。

### 段落 52 · Page 7

**EN**

For example, search engines powered by LLMs can serve as an AI assistant, such as Windows Copilot, Bing Chat. It can generate responses based 7

**中文**

例如，法学硕士支持的搜索引擎可以充当人工智能助手，例如Windows Copilot、Bing Chat。它可以根据 7 生成响应

### Page 8

### 段落 53 · Page 8

**EN**

/ AI Open 00 (2023) 1–17 8 on the conversation’s context and the user’s needs in real-time, without relying on pre-programmed responses. As long as the user inputs a question, it can help retrieve information, search knowledge, use Apps, and call plugins in the simplest way [98]. The IR system powered by LLMs possesses the capability to comprehend and address complex queries, thereby enhancing the interaction process in terms of intuitiveness, personalization, efficiency, effectiveness, responsiveness, and friendliness. 4.

**中文**

/ AI Open 00 (2023) 1–17 8 实时了解对话的上下文和用户的需求，而不依赖于预先编程的响应。只要用户输入一个问题，它就能以最简单的方式帮助检索信息、搜索知识、使用Apps、调用插件[98]。由法学硕士支持的IR系统具有理解和解决复杂查询的能力，从而增强交互过程的直观性、个性化、效率、有效性、响应性和友好性。 4.

### 段落 54 · Page 8

**EN**

IR for Large Language Models LLMs exhibit certain inherent limitations that are commonly encountered in generative language models. Firstly, they may occasionally generate erroneous or nonsensical responses, a phenomenon referred to as ”hallucinations” 4. Secondly, they are trained on fixed corpora, which restricts their ability to answer questions that require newly emerged knowledge or information after the training date [99, 100]; the stored knowledge within the model can be inevitably incomplete, outdated, or even incorrect [93].

**中文**

大型语言模型的 IR 法学硕士表现出生成语言模型中常见的某些固有局限性。首先，他们可能偶尔会产生错误或无意义的反应，这种现象被称为“幻觉”4。其次，他们是在固定的语料库上接受训练的，这限制了他们在训练后回答需要新出现的知识或信息的问题的能力[99, 100]；模型中存储的知识可能不可避免地不完整、过时，甚至不正确[93]。

### 段落 55 · Page 8

**EN**

Thirdly, they can hardly respond to “private” questions that require access to confidential data sources, which are not available during the training of LLMs. Utilizing the retrieval capabilities of IR models presents a viable approach for addressing the above limitations of LLMs. By incorporating retrieval, we can leverage relevant knowledge from external knowledge bases during the generation process, thereby reducing the occurrence of hallucinations. Retrieval models possess strong ability to access up-to-date information, enabling LLMs to respond with fresh and relevant information.

**中文**

第三，他们很难回答需要访问机密数据源的“私人”问题，而这些数据源在法学硕士培训期间是无法获得的。利用 IR 模型的检索功能为解决法学硕士的上述局限性提供了一种可行的方法。通过结合检索，我们可以在生成过程中利用外部知识库的相关知识，从而减少幻觉的发生。检索模型具有强大的获取最新信息的能力，使法学硕士能够提供新鲜且相关的信息。

### 段落 56 · Page 8

**EN**

Moreover, the combination of retrieval and LLMs is particularly valuable in data-sensitive scenarios, where internal data cannot be utilized for language model training, factual accuracy is of utmost importance, or the retrieval pool may vary over time [101, 102]. In this section, we discuss three directions that augment LLMs with retrieval in di fferent phrases: pre-training, fine-tuning, and leveraging black-box LLMs such as ChatGPT that only offer APIs. 4.1. Pre-training LLMs with Retrieval There is limited work on pre-training LLMs that incorporate a retrieval module.

**中文**

此外，检索和法学硕士的结合在数据敏感的场景中特别有价值，在这些场景中，内部数据无法用于语言模型训练，事实准确性至关重要，或者检索池可能会随着时间的推移而变化[101, 102]。在本节中，我们讨论通过不同短语的检索来增强 LLM 的三个方向：预训练、微调和利用黑盒 LLM，例如仅提供 API 的 ChatGPT。 4.1.通过检索对法学硕士进行预训练 包含检索模块的法学硕士预训练方面的工作有限。

### 段落 57 · Page 8

**EN**

One notable example is Atlas [103], which pre-trains an encoder-decoder T5 with an extra retrieval module and demonstrates its ability on knowledge-intensive tasks with very few training samples. REALM enhances encoder-only language model training by incorporating a neural knowledge retriever that extracts information from a text-based knowledge database [104]. RETRO is a retrieval-augmented decoder-only language model, where a chunked cross-attention module is employed to aggregate retrieved text from a retrieval pool containing trillions of tokens [105]. In a recent study, based on the auto-regressive language model RETRO, Wang et al.

**中文**

一个值得注意的例子是 Atlas [103]，它使用额外的检索模块预训练编码器-解码器 T5，并通过很少的训练样本展示了其执行知识密集型任务的能力。 REALM 通过结合从基于文本的知识数据库中提取信息的神经知识检索器来增强仅编码器的语言模型训练[104]。 RETRO 是一种仅检索增强解码器的语言模型，其中采用分块交叉注意模块来聚合从包含数万亿个令牌的检索池中检索到的文本[105]。 Wang 等人最近的一项研究基于自回归语言模型 RETRO。

### 段落 58 · Page 8

**EN**

[106] studies the question whether it is useful to pre-train LLMs with retrieval. As a result, the pre-trained retrieval-augmented language model RETRO outperforms the vanilla GPT on text generation tasks with higher factual accuracy, and on knowledgeintensive tasks. In addition, in open-domain question answering tasks, RETRO largely outperforms GPT which just incorporates retrieval at the fine-tuning stage. Note that there is a trade-o ffbetween the computation overhead from using retrieval and the performance. Wang et al.

**中文**

[106]研究了通过检索来预训练法学硕士是否有用的问题。因此，预训练的检索增强语言模型 RETRO 在具有更高事实准确性的文本生成任务和知识密集型任务上优于普通 GPT。此外，在开放域问答任务中，RETRO 很大程度上优于仅在微调阶段结合检索的 GPT。请注意，使用检索的计算开销和性能之间存在权衡。王等人。

### 段落 59 · Page 8

**EN**

[106] suggest a flexible implementation that specifies the number of tokens to generate with the current retrieval result before the next retrieval. In addition to incorporating a retrieval module into the pre-training of LLMs, it is also valuable to investigate how retrieval functionalities can enhance the pre-training process itself. Generally, the retrieved evidence serves as the privileged information within the input context. Such privileged information is often costly or impractical to obtain during the inference stage, though it is available during the training phase [107].

**中文**

[106]提出了一种灵活的实现，指定在下一次检索之前使用当前检索结果生成的令牌数量。除了将检索模块纳入法学硕士的预训练之外，研究检索功能如何增强预训练过程本身也很有价值。一般来说，检索到的证据充当输入上下文中的特权信息。尽管在训练阶段可以获得此类特权信息，但在推理阶段获取此类特权信息通常成本高昂或不切实际[107]。

### 段落 60 · Page 8

**EN**

By having both the retrieved evidence and the processed output answer (or subsequent tokens) accessible during training, it is possible to pre-train (or simply fine-tune) LLMs to improve their performance on knowledge-intensive tasks [108, 98]. 4.2. Fine-Tuning LLMs with Retrieval Adapters Pre-training or fine-tuning the entire LLM with retrieval could enhance its retrieval capabilities. However, the considerable cost makes it prohibitive to use. Considering that LLMs serve as a foundation for downstream tasks, 4Introducing ChatGPT, https://openai.com/blog/chatgpt 8

**中文**

通过在训练期间获取检索到的证据和处理后的输出答案（或后续标记），可以对 LLM 进行预训练（或简单地微调），以提高其在知识密集型任务上的表现 [108, 98]。 4.2.使用检索适配器微调法学硕士 通过检索对整个法学硕士进行预训练或微调可以增强其检索能力。然而，高昂的成本使其难以使用。考虑到 LLM 作为下游任务的基础，4ChatGPT 简介，https://openai.com/blog/chatgpt 8

### Page 9

### 段落 61 · Page 9

**EN**

/ AI Open 00 (2023) 1–17 9 updating all parameters should be approached cautiously and infrequently. Therefore, an alternative is to fine-tune LLMs with search adapters, which is more efficient and cost-effective. Adapters are plug-and-play modules for LLM with only a small number of parameters. They enable LLMs to acquire task-specific capabilities without a ffecting the original parameters, while still achieving comparable or superior performance compared to updating the entire models. There have been several studies on LLM adapters, which can be roughly classified into two categories: tokenbased methods and layer-based methods [109, 110].

**中文**

/ AI Open 00 (2023) 1–17 9 应谨慎且不频繁地更新所有参数。因此，另一种方法是使用搜索适配器对LLM进行微调，这样更加高效且更具成本效益。适配器是 LLM 的即插即用模块，只有少量参数。它们使法学硕士能够在不影响原始参数的情况下获得特定于任务的功能，同时与更新整个模型相比仍能实现可比或优越的性能。关于LLM适配器的研究已经有很多，可以大致分为两类：基于token的方法和基于层的方法[109, 110]。

### 段落 62 · Page 9

**EN**

The former seeks to insert task-related anchor tokens into the input sequence for fine-tuning [111, 112, 113]. For example, Prompt tuning prepends several additional task-specific tunable tokens into the input sequence [114]. The latter seeks to insert additional layers into the models and fine-tune these layers only [115, 116, 117]. For example, Hu et al. [118] propose LoRA which adds a trainable low-rank dense layer before the self-attention in transformers. LLMs with adapters have been demonstrated e ffective on some downstream tasks such as machine reading comprehension.

**中文**

前者试图将与任务相关的锚标记插入到输入序列中以进行微调[111,112,113]。例如，提示调整将几个额外的特定于任务的可调整标记添加到输入序列中[114]。后者寻求在模型中插入额外的层并仅微调这些层[115,116,117]。例如，胡等人。 [118]提出LoRA，它在Transformer中的自注意力之前添加了一个可训练的低秩密集层。带有适配器的法学硕士已被证明对机器阅读理解等一些下游任务有效。

### 段落 63 · Page 9

**EN**

Nevertheless, the following research questions remain to be explored to empower LLMs with retrieval capabilities through adapters. • What adapters are best suited for retrieval? What neural network modules are best suited for retrieval adapters? • How to fine-tune the retrieval adapters? Which fine-tuning techniques can promote the retrieval capability in highest degree without hurting the inherent capabilities of LLM? • Why do retrieval adapters work? How do we know the capability boundary of retrieval adapters, and what can we do to avoid potential failures? Fine-tuning LLMs with retrieval adapters can provide benefits in various aspects.

**中文**

尽管如此，以下研究问题仍有待探索，以通过适配器赋予法学硕士检索能力。 • 哪些适配器最适合检索？哪些神经网络模块最适合检索适配器？ • 如何微调检索适配器？哪些微调技术可以在不损害LLM固有能力的情况下最大程度地提升检索能力？ • 检索适配器为何有效？我们如何知道检索适配器的能力边界，以及如何避免潜在的故障？使用检索适配器微调法学硕士可以在各个方面带来好处。

### 段落 64 · Page 9

**EN**

On one hand, it o ffers new opportunities for researchers with limited computation resources. Progress in scientific research cannot be achieved without the participation of researchers around the world. On the other hand, the lower cost of search adapters allows for wider applications, especially when data privacy is a top priority. Small-size institutions can have LLMs equipped with their own retrieval systems without exposing the raw data. 4.3. Augmenting Black-box LLMs with Retrieval In many scenarios, LLMs can only be accessed through remote APIs, and the possibility of fine-tuning these models is restricted.

**中文**

一方面，它为计算资源有限的研究人员提供了新的机会。科学研究的进步离不开世界各地研究人员的参与。另一方面，搜索适配器的成本较低，可以实现更广泛的应用，特别是当数据隐私是重中之重时。小型机构可以让法学硕士配备自己的检索系统，而无需暴露原始数据。 4.3.通过检索增强黑盒 LLM 在许多情况下，LLM 只能通过远程 API 访问，并且微调这些模型的可能性受到限制。

### 段落 65 · Page 9

**EN**

The most prevalent approach to leveraging LLMs is treating them as black-box systems and using customized prompts that integrate evidence from external data sources. This method enables users to obtain desired outputs from the LLMs by providing tailored prompts that incorporate relevant external evidence. There are some preliminary studies on this interesting topic. shuster et al. [119] proposed a modular system SeeKeR which searches for and chooses knowledge with internet search as a module during language generation. Similarly, Komeili et al. [99] and Lazaridou et al.

**中文**

利用法学硕士最普遍的方法是将其视为黑匣子系统，并使用集成外部数据源证据的定制提示。该方法使用户能够通过提供包含相关外部证据的定制提示来从法学硕士获得所需的输出。关于这个有趣的话题有一些初步研究。舒斯特等人[119]提出了一种模块化系统SeeKeR，在语言生成过程中以互联网搜索为模块来搜索和选择知识。同样，Komeili 等人。 [99] 和拉扎里杜等人。

### 段落 66 · Page 9

**EN**

[100] also introduced approaches which condition on the results from internet search engines (such as Google Search) to generate a response. He et al. [93] proposed a post-processing approach named “rethinking with retrieval (RR)” to solve the same problem. RR uses the chain-of-thought (COT) prompting to generate multiple reasoning paths, then retrieves external evidences based on the steps in these paths. Experiments on three complex reasoning tasks and di fferent datasets demonstrate that RR outperforms all baselines without additional pre-training or fine-tuning. Ram et al.

**中文**

[100]还介绍了根据互联网搜索引擎（例如谷歌搜索）的结果生成响应的方法。他等人。 [93]提出了一种名为“重新思考与检索（RR）”的后处理方法来解决同样的问题。 RR利用思想链（COT）提示生成多条推理路径，然后根据这些路径中的步骤检索外部证据。对三个复杂推理任务和不同数据集的实验表明，RR 在无需额外预训练或微调的情况下优于所有基线。拉姆等人。

### 段落 67 · Page 9

**EN**

[120] introduced an in-context Retrieval-Augmented Language Modeling (RALM) method that simply uses off-the-shelf general purpose retrievers to retrieve documents and preprends retrieved results to the input of language models. Peng et al. [121] proposed a system named LLM- Augmenter, which augments a fixed black-box LLM with a set of plug-and-play modules. Given a query, LLM- Augmenter first retrieves evidences from external data sources, then generates a prompt that contains the retrieved evidences for ChatGPT.

**中文**

[120]引入了一种上下文检索增强语言建模（RALM）方法，该方法简单地使用现成的通用检索器来检索文档并将检索到的结果预先预测到语言模型的输入。彭等人。 [121]提出了一个名为LLM-Augmenter的系统，它用一组即插即用模块增强了固定的黑盒LLM。给定查询，LLM-Augmenter 首先从外部数据源检索证据，然后生成包含检索到的 ChatGPT 证据的提示。

### 段落 68 · Page 9

**EN**

Their experiments on the information seeking dialog and open-domain wiki question answering tasks show this method could significantly reduce the hallucination problem of LLMs. Recently, OpenAI officially released the Retrieval Plugin5, which provides semantic search and retrieval functionality of personal or organizational documents. Relevant documents snippets can be retrieved from external sources, such as personal emails or internal organizational files, with this plugin. 5ChatGPT Retrieval Plugin, https://github.com/openai/chatgpt-retrieval-plugin 9

**中文**

他们在信息寻求对话和开放域维基问答任务上的实验表明，这种方法可以显着减少法学硕士的幻觉问题。近日，OpenAI正式发布Retrieval Plugin5，提供个人或组织文档的语义搜索和检索功能。使用此插件可以从外部来源检索相关文档片段，例如个人电子邮件或内部组织文件。 5ChatGPT 检索插件，https://github.com/openai/chatgpt-retrieval-plugin 9

### Page 10

### 段落 69 · Page 10

**EN**

/ AI Open 00 (2023) 1–17 10 There are several key components in the pipeline of augmenting LLMs with retrieval, which are worth to study in the future. • Design of Retriever. Intuitively, a better retriever could return results with higher quality, and thereby helps to generate better response. Should we use a dense retriever or a sparse retriever in generating grounding documents? Which kind of information to index, documents or passages? • Context Modeling. How to generate an explicit keyword query or representation vector that can describe the current information need and retrieve useful results for language generation?

**中文**

/ AI Open 00 (2023) 1–17 10 通过检索增强法学硕士的流程中有几个关键组成部分，值得未来研究。 • 寻回器的设计。直观上，更好的检索器可以返回更高质量的结果，从而有助于产生更好的响应。我们应该使用密集检索器还是稀疏检索器来生成基础文档？要索引哪种类型的信息、文档或段落？ • 情境建模。如何生成可以描述当前信息需求并检索对语言生成有用的结果的显式关键字查询或表示向量？

### 段落 70 · Page 10

**EN**

ChatGPT-like LLMs are optimized for dialogue rather than search, hence how to derive search intent from the multi-turn chat history remains a challenge. • Selection of Grounding Documents. In addition to pure relevance, other factors of diversity, informativeness, and freshness should also be considered when selecting a small set of documents. • Prompting Mechanism. It remains a challenge to generate good prompts that can help improve generation quality with the given grounding documents. 5.

**中文**

类似 ChatGPT 的 LLM 针对对话而不是搜索进行了优化，因此如何从多轮聊天历史中导出搜索意图仍然是一个挑战。 • 接地文件的选择。在选择一小部分文档时，除了纯粹的相关性之外，还应考虑多样性、信息量和新鲜度等其他因素。 • 提示机制。生成良好的提示来帮助提高给定接地文件的生成质量仍然是一个挑战。 5.

### 段落 71 · Page 10

**EN**

LLMs + IR: New Paradigm and Framework Traditional IR models are designed to meet human information needs through the interactions between users and systems. IR models do not preserve knowledge, instead, they search for external knowledge or information to meet the information needs efficiently. With the emergence of LLMs, we propose a new technical paradigm of IR: as shown in Figure 1, the key elements are LLMs, IR models and humans. • LLMs provide valuable (internal) knowledge and information to meet human information needs, and their reasoning capacity makes it easier to provide high-quality responses.

**中文**

LLM + IR：新范式和框架 传统的IR模型旨在通过用户和系统之间的交互来满足人类的信息需求。 IR模型并不保存知识，而是寻找外部知识或信息来有效地满足信息需求。随着LLM的出现，我们提出了一种新的IR技术范式：如图1所示，关键要素是LLM、IR模型和人类。 • 法学硕士提供有价值的（内部）知识和信息，以满足人类信息需求，他们的推理能力使其更容易提供高质量的答复。

### 段落 72 · Page 10

**EN**

• IR models that search for external knowledge are indispensable, which provide up-to-date and relevant information for both LLMs and humans. While LLMs may su ffice in directly generating answers to meet human information needs for simple questions, the significance of IR models becomes more pronounced when dealing with complex and difficult problems. • Humans raise information needs in the paradigm and are the tutor for both LLMs and IR models. They endow the system with human values and behavioral characteristics, making it serve users better.

**中文**

• 搜索外部知识的IR 模型是不可或缺的，它为法学硕士和人类提供最新的相关信息。虽然法学硕士可能足以直接生成答案来满足人类对简单问题的信息需求，但在处理复杂和困难的问题时，IR 模型的重要性变得更加明显。 • 人类在范式中提出信息需求，并且是法学硕士和IR 模型的导师。他们赋予系统人性的价值观和行为特征，使其更好地为用户服务。

### 段落 73 · Page 10

**EN**

The synergistic relationship among them not only facilitates mutual enhancement but also enables the fulfillment of new tasks as an organic whole. 5.1. Importance of the Three Modules In accordance with the new IR technical paradigm, an important question arises: Are all three elements essential for this new paradigm? In the following subsection, we will provide our insights and responses. 5.1.1. Paradigm without LLMs Without LLMs, the paradigm degrades to traditional IR, accompanied by inherent challenges: • Dependency on the Internet.

**中文**

它们之间的协同关系，不仅有利于相互促进，而且可以作为一个有机整体完成新的任务。 5.1.三个模块的重要性根据新的IR技术范式，出现了一个重要的问题：所有三个要素对于这个新范式都是必不可少的吗？在下一小节中，我们将提供我们的见解和回应。 5.1.1.没有法学硕士的范式 如果没有法学硕士，范式就会退化为传统的 IR，并伴随着固有的挑战： • 对互联网的依赖。

### 段落 74 · Page 10

**EN**

As IR models do not retain knowledge or information themselves, they rely on the Internet to acquire external knowledge, potentially limiting their applicability in certain scenarios. • Lacking reasoning ability. Existing IR models mainly provide collected knowledge /information to fulfill human information needs, lacking the ability to assist users in comprehending the information. Better reasoning ability will deliver more user-friendly and valuable results for humans. 10

**中文**

由于IR模型本身不保留知识或信息，它们依赖互联网获取外部知识，这可能限制了它们在某些场景中的适用性。 • 缺乏推理能力。现有的IR模型主要提供收集的知识/信息来满足人类的信息需求，缺乏帮助用户理解信息的能力。更好的推理能力将为人类带来更加用户友好和有价值的结果。 10

### Page 11

### 段落 75 · Page 11

**EN**

/ AI Open 00 (2023) 1–17 11 5.1.2. Paradigm without IR In the era of LLMs, the presence of an IR system is critical as it addresses the limitations of generative language models. Without an IR system, LLMs encounter the following challenges: • Lacking factual consistency. One inherent limitation of generative LLMs is the lack of factual consistency, resulting from their training data and the potential generation of false information. In contrast, the IR system frees from this issue by storing and offering factual information through keyword matching, thereby complementing the shortcomings of LLMs.

**中文**

/ AI 开放 00 (2023) 1–17 11 5.1.2。没有 IR 的范式在法学硕士时代，IR 系统的存在至关重要，因为它解决了生成语言模型的局限性。如果没有IR系统，法学硕士会遇到以下挑战： • 缺乏事实一致性。生成式法学硕士的一个固有限制是缺乏事实一致性，这是由于其训练数据和潜在生成的虚假信息造成的。相比之下，IR系统通过关键词匹配来存储和提供事实信息，从而摆脱了这个问题，从而弥补了LLM的缺点。

### 段落 76 · Page 11

**EN**

• Lacking effective integration of new and existing knowledge. Large Language models have the capacity to learn knowledge from large-scale data, such as commonsense information. However, relying solely on LLMs may neglect the crucial mechanism of effectively and efficiently integrating new and existing knowledge. In the human brain, memory involves a complex network of interconnected brain regions, including the hippocampus, prefrontal cortex, and other cortical areas. Retrieval processes are closely linked to memory consolidation and the reactivation of neural networks associated with previously encoded information.

**中文**

• 缺乏新知识和现有知识的有效整合。大型语言模型具有从大规模数据（例如常识信息）中学习知识的能力。然而，仅仅依靠法学硕士可能会忽视有效和高效地整合新知识和现有知识的关键机制。在人脑中，记忆涉及一个由相互连接的大脑区域组成的复杂网络，包括海马体、前额皮质和其他皮质区域。检索过程与记忆巩固和与先前编码信息相关的神经网络的重新激活密切相关。

### 段落 77 · Page 11

**EN**

When we retrieve information from memory, this activity can strengthen the neural connections related to that information, making it more accessible for future retrieval and improving overall memory performance. 5.1.3. Paradigm without Human The absence of human input and feedback hinders both LLMs and IR models from delivering personalized information services. The associated challenges are: • Identical information services. Large-scale dialogue systems use a generation-based approach to provide information to users.

**中文**

当我们从记忆中检索信息时，这种活动可以加强与该信息相关的神经连接，使其更易于将来检索并提高整体记忆表现。 5.1.3.没有人类的范式缺乏人类的输入和反馈阻碍了法学硕士和 IR 模型提供个性化信息服务。相关的挑战是： • 相同的信息服务。大型对话系统使用基于生成的方法向用户提供信息。

### 段落 78 · Page 11

**EN**

The generated content is not personalized, which can cause the issues that the content does not match the user’s real intention. • Uncontrollable value of society. Without human feedback, LLMs are unable to account for user personality and values, resulting in information services that do not adequately align with societal values. 5.2. Summary The rise of dialogue-based LLMs, exemplified by platforms like ChatGPT from OpenAI and New Bing from Microsoft, has sparked a trend that could potentially replace traditional IR systems.

**中文**

生成的内容不是个性化的，这会导致内容与用户的真实意图不符的问题。 • 无法控制的社会价值。如果没有人类反馈，法学硕士就无法考虑用户的个性和价值观，从而导致信息服务与社会价值观不充分一致。 5.2.摘要 基于对话的法学硕士的兴起，例如 OpenAI 的 ChatGPT 和微软的 New Bing 等平台，引发了一种可能取代传统 IR 系统的趋势。

### 段落 79 · Page 11

**EN**

However, as previously discussed, in the era of LLMs, human information needs and feedback, along with the continued relevance of traditional IR models, remain vital components in the development of trustworthy information service systems. 6. Challenges and Future While LLMs for IR hold promise, they also present numerous challenges and unanswered questions. In the final section of this article, we discuss some selected issues to outline future directions. • High Computational Costs. The primary challenge in using LLMs is their high computational cost.

**中文**

然而，正如前面所讨论的，在法学硕士时代，人类的信息需求和反馈，以及传统IR模型的持续相关性，仍然是开发值得信赖的信息服务系统的重要组成部分。 6. 挑战和未来 虽然国际关系法学硕士前景广阔，但它们也带来了许多挑战和悬而未决的问题。在本文的最后部分，我们讨论一些选定的问题以概述未来的方向。 • 高计算成本。使用法学硕士的主要挑战是其高昂的计算成本。

### 段落 80 · Page 11

**EN**

This poses a significant barrier for small and medium-sized research laboratories and companies, hindering their integration of LLMs into daily workflows and products. Even large companies with ample computational resources face cost pressures when deploying LLMs for online search, recommendation, and advertisement services due to the immense volume of user requests. Common solutions include compressing LLMs, reducing their size from hundreds of billions to tens billions or even smaller, especially before online deployment.

**中文**

这对中小型研究实验室和公司构成了重大障碍，阻碍了他们将法学硕士融入日常工作流程和产品中。由于用户请求量巨大，即使是拥有充足计算资源的大公司在部署法学硕士进行在线搜索、推荐和广告服务时也会面临成本压力。常见的解决方案包括压缩LLM，将其大小从数千亿减少到百亿甚至更小，特别是在在线部署之前。

### 段落 81 · Page 11

**EN**

Additionally, efforts to develop more e fficient and cost-e ffective hardware for training and inference are underway to address the cost challenge. • General-purpose v.s. Domain-specific. LLMs have demonstrated impressive capabilities in general-purpose tasks like text generation and chatting, owing to their pre-training and fine-tuning on large-scale Internet corpora. However, it is widely recognized that LLMs face limitations when it comes to adapting to domain-specific tasks. One one hand, high-quality professional domain knowledge, which is often not abundantly available on 11

**中文**

此外，我们正在努力开发更高效、更具成本效益的训练和推理硬件，以应对成本挑战。 • 通用型与通用型特定领域。由于法学硕士在大规模互联网语料库上进行了预训练和微调，他们在文本生成和聊天等通用任务中表现出了令人印象深刻的能力。然而，人们普遍认识到法学硕士在适应特定领域任务时面临局限性。一方面，高质量的专业领域知识，而这些知识在 11 上往往并不丰富

### Page 12

### 段落 82 · Page 12

**EN**

/ AI Open 00 (2023) 1–17 12 the Internet, makes it prohibitive to pre-train and fine-tune LLMs. On the other hand, domain-specific knowledge is not always expressed in natural language; it may be represented as semi-structured or structured tables, heuristic rules, equations, and more. Enabling LLMs to e ffectively handle domain-specific tasks is crucial not only for the specific domains themselves but also for enhancing the overall capabilities and applications of LLMs. • Trustworthiness. There is a widely acknowledged concern that LLMs currently lack the ability to provide reliable and trustworthy answers to user queries.

**中文**

/ AI Open 00 (2023) 1–17 12 互联网使得预训练和微调法学硕士变得令人望而却步。另一方面，特定领域的知识并不总是用自然语言表达；它可以表示为半结构化或结构化表、启发式规则、方程等。使法学硕士能够有效地处理特定领域的任务不仅对于特定领域本身至关重要，而且对于增强法学硕士的整体能力和应用也至关重要。 • 值得信赖。人们普遍担心法学硕士目前缺乏为用户查询提供可靠且值得信赖的答案的能力。

### 段落 83 · Page 12

**EN**

While LLMs can generate explanations and cite sources, it has been observed that a significant portion of these explanations and citations are illogical, inappropriate, or even fake. This poses a substantial risk in real-world search and recommendation scenarios, as generating misleading explanations, answers, and information sources can have detrimental e ffects on the community at large. To address this issue and enhance the trustworthiness of LLMs, it is crucial to enable LLMs to have a clear understanding of their knowledge and limitations. One potential solution is allowing LLMs to decline providing an answer when uncertain.

**中文**

虽然法学硕士可以生成解释并引用来源，但据观察，这些解释和引用中有很大一部分是不合逻辑的、不恰当的，甚至是虚假的。这在现实世界的搜索和推荐场景中带来了巨大的风险，因为生成误导性的解释、答案和信息源可能会对整个社区产生不利影响。为了解决这个问题并提高法学硕士的可信度，让法学硕士清楚地了解自己的知识和局限性至关重要。一种潜在的解决方案是允许法学硕士在不确定时拒绝提供答案。

### 段落 84 · Page 12

**EN**

• Controllable Generation.Considering the public nature of search engines and recommendation systems, it is important to address regulatory and ethical considerations such as fairness, impartiality, and human values when presenting content to users. While LLMs demonstrate proficiency in generating text, they often lack a deep understanding of the meaning behind the generated words. Ensuring that the generated content meets the necessary regulatory and ethical requirements remains a significant challenge, and has no effective solutions for now.

**中文**

• 可控生成。考虑到搜索引擎和推荐系统的公共性质，在向用户呈现内容时，解决公平、公正和人类价值观等监管和道德考虑因素非常重要。虽然法学硕士在生成文本方面表现出熟练程度，但他们往往缺乏对生成单词背后含义的深入理解。确保生成的内容满足必要的监管和道德要求仍然是一项重大挑战，目前还没有有效的解决方案。

### 段落 85 · Page 12

**EN**

• High-quality Data: High-quality data plays a vital role in the development and improvement of LLMs. The success of LLMs heavily relies on the continuous provision of human-labeled data. It is crucial that the labeled data not only meets a certain quantity threshold but also maintains high quality. Obtaining high-quality data in real-world application scenarios involves multiple steps such as data cleaning, data labeling, and data quality evaluation. Professional data annotation providers play a crucial role in supporting these processes.

**中文**

• 高质量数据：高质量数据对于法学硕士的发展和提高起着至关重要的作用。法学硕士的成功在很大程度上依赖于持续提供人工标记数据。标记数据不仅满足一定的数量阈值，而且保持高质量，这一点至关重要。在实际应用场景中获取高质量数据涉及数据清洗、数据标注、数据质量评估等多个步骤。专业的数据注释提供商在支持这些过程中发挥着至关重要的作用。

### 段落 86 · Page 12

**EN**

Additionally, it is essential to develop advanced, professional, and sustainable data annotation approaches to meet the growing demand for high-quality data in LLM applications. • Long-context Dependency. Existing LLMs have limited capacity to handle long contexts, while IR tasks rely on long-term context to effectively capture and understand user intent. It is crucial to enable LLM-enhanced IR systems to model users’ long-term intent that spans a large range of period. • Serving Time Requirements. The latency in serving LLM results significantly lags behind the time requirements of information retrieval (IR) systems.

**中文**

此外，开发先进、专业和可持续的数据注释方法至关重要，以满足法学硕士申请中对高质量数据不断增长的需求。 • 长上下文依赖。现有的法学硕士处理长上下文的能力有限，而 IR 任务则依赖于长上下文来有效捕获和理解用户意图。让法学硕士增强型 IR 系统能够对跨越较大时期的用户长期意图进行建模至关重要。 • 服务时间要求。提供 LLM 结果的延迟明显落后于信息检索 (IR) 系统的时间要求。

### 段落 87 · Page 12

**EN**

This presents e fficiency challenges when integrating LLMs into IR, thereby impacting the online user experience. • Presentation Format. Traditional IR systems present ranked lists of content, while LLMs excel at generating new information. How to design a new presentation format that effectively fulfills user needs in LLM-enhanced IR remains an open question. • Integrating Structural Information. LLMs primarily rely on textual sequence information, whereas IR systems require the integration of structural information such as user-item interactions and web linkage data.

**中文**

这在将法学硕士集成到 IR 时带来了效率挑战，从而影响了在线用户体验。 • 演示文稿格式。传统的 IR 系统提供排名的内容列表，而法学硕士擅长生成新信息。如何设计一种新的演示格式来有效满足LLM增强型IR中的用户需求仍然是一个悬而未决的问题。 • 整合结构信息。 LLM 主要依赖于文本序列信息，而 IR 系统则需要集成结构信息，例如用户-项目交互和网络链接数据。

### 段落 88 · Page 12

**EN**

Effectively leveraging this structural information in LLM-based IR systems is an unresolved issue. • Balance between Generative and Retrieved Data. LLMs leverage deep learning and reinforcement learning to generate content at scale, but their generated content may have limitations in terms of freshness and credibility. In contrast, retrieval can provide the content from the Web, ensuring the latest information. Balancing these two types of data in real-life applications is a significant challenge for improving overall performance.

**中文**

在基于法学硕士的IR系统中有效利用这种结构信息是一个尚未解决的问题。 • 生成数据和检索数据之间的平衡。法学硕士利用深度学习和强化学习大规模生成内容，但其生成的内容在新鲜度和可信度方面可能存在局限性。相比之下，检索可以提供来自网络的内容，确保最新的信息。在现实应用程序中平衡这两种类型的数据是提高整体性能的重大挑战。

### 段落 89 · Page 12

**EN**

One approach is to refine user needs and classify them into di fferent groups, allowing for appropriate data generation methods or balancing ratios. In addition, retrieval can be used to provide additional information to enhance content generation, or assist in screening and filtering the generated content for information grounding. 12

**中文**

一种方法是细化用户需求并将其分类为不同的组，从而允许适当的数据生成方法或平衡比率。此外，检索可用于提供附加信息以增强内容生成，或帮助筛选和过滤生成的内容以进行信息基础。 12

### Page 13

### 段落 90 · Page 13

**EN**

/ AI Open 00 (2023) 1–17 13 • Content Quality and Credibility . While LLMs are e ffective in generating content, they can also produce low-quality or even misinformation-filled content. The proliferation of such content on the Internet can disrupt the existing data ecology and impact applications like search engine and recommendation system. Traditional quality assessment techniques like PageRank may not be e ffective in this context. It is di fficult for existing techniques to identify low-quality or misleading content.

**中文**

/ AI Open 00 (2023) 1–17 13 • 内容质量和可信度。虽然法学硕士可以有效地生成内容，但它们也可能生成低质量甚至充满错误信息的内容。此类内容在互联网上的扩散可能会破坏现有的数据生态并影响搜索引擎和推荐系统等应用程序。像 PageRank 这样的传统质量评估技术在这种情况下可能不起作用。现有技术很难识别低质量或误导性内容。

### 段落 91 · Page 13

**EN**

In the era of AI-generated content, new mechanisms are needed to assess data quality and distinguish between generated and reliable content. One approach is manual or community review to ensure content accuracy, but it is time-consuming and does not scale well. Another approach is leveraging LLM-powered machine learning techniques to train models that can recognize AI-generated content and evaluate its quality. These models can then be applied to select, label, or filter content for different applications. • Content Creation Environment .

**中文**

在人工智能生成内容的时代，需要新的机制来评估数据质量并区分生成的内容和可靠的内容。一种方法是手动或社区审核以确保内容准确性，但这种方法非常耗时且扩展性不佳。另一种方法是利用法学硕士支持的机器学习技术来训练能够识别人工智能生成的内容并评估其质量的模型。然后可以应用这些模型来选择、标记或过滤不同应用程序的内容。 • 内容创建环境。

### 段落 92 · Page 13

**EN**

The proliferation of generated content introduces challenges for content creators, and may even reshape the content ecosystem. The presence of generated content intensifies competition within the content market, pushing content creators to continuously enhance their writing quality, foster innovation, and proactively adapt to industry changes. Moreover, it may influence users’ perception of value and demand for content, prompting content creators to constantly adjust their writing approach and strategies.

**中文**

生成内容的激增给内容创作者带来了挑战，甚至可能重塑内容生态系统。生成内容的出现加剧了内容市场的竞争，促使内容创作者不断提高写作质量、培育创新、主动适应行业变化。而且，它还可能影响用户对内容的价值认知和需求，促使内容创作者不断调整自己的写作方式和策略。

### 段落 93 · Page 13

**EN**

Despite the challenges, LLMs also provide new opportunities for content creators to collaborate and develop effective platforms that facilitate more productive and higher-quality content generation. References [1] M. Kobayashi, K. Takeda, Information retrieval on the web, ACM computing surveys (CSUR) 32 (2) (2000) 144–173. [2] M. Manoj, J. Elizabeth, Information retrieval on internet using meta-search engines: A review, Journal of Scientific and Industrial Research 67 (10) (2008). [3] G. Faggioli, M. Ferrante, N. Ferro, R. Perego, N.

**中文**

尽管面临挑战，法学硕士还为内容创作者提供了新的机会来合作和开发有效的平台，以促进更高效、更高质量的内容生成。参考文献 [1] M. Kobayashi、K. Takeda，网络信息检索，ACM 计算调查 (CSUR) 32 (2) (2000) 144–173。 [2] M. Manoj, J. Elizabeth，使用元搜索引擎进行互联网信息检索：综述，科学与工业研究杂志 67 (10) (2008)。 [3] G. Faggioli、M. Ferrante、N. Ferro、R. Perego、N.

### 段落 94 · Page 13

**EN**

Tonellotto, Hierarchical dependence-aware evaluation measures for conversational search, in: Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, 2021, pp. 1935– 1939. [4] S. Li, R. Xie, Y . Zhu, X. Ao, F. Zhuang, Q. He, User-centric conversational recommendation with multi-aspect user modeling, in: Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval, 2022, pp. 223–233. [5] Z. Chen, X. Cheng, S. Dong, Z. Dou, J. Guo, X. Huang, Y . Lan, C. Li, R. Li, T.-Y . Liu, Y . Liu, J. Ma, B. Qin, M. Wang, J. rong Wen, J. Xu, M.

**中文**

Tonellotto，对话式搜索的分层依赖感知评估措施，见：第 44 届国际 ACM SIGIR 信息检索研究与发展会议论文集，2021 年，第 1935-1939 页。 [4] S. Li, R. Xie, Y . Zhu, X. Ao, F. Zhuang, Q. He，以用户为中心的多方面用户建模会话推荐，见：第 45 届国际 ACM SIGIR 信息检索研究与发展会议论文集，2022 年，第 223-233 页。 [5] 陈正，程旭，董三，窦正，郭建，黄晓，Y．兰，李，R，李，T.-Y。刘，Y。刘，马，秦，王，荣，文，徐，M。

### 段落 95 · Page 13

**EN**

Zhang, P. Zhang, Q. Zhang, Information retrieval: a view from the chinese ir community, Frontiers of Computer Science 15 (2020) 1–15. [6] S. Bubeck, V . Chandrasekaran, R. Eldan, J. Gehrke, E. Horvitz, E. Kamar, P. Lee, Y . T. Lee, Y . Li, S. Lundberg, et al., Sparks of artificial general intelligence: Early experiments with gpt-4, arXiv preprint arXiv:2303.12712 (2023). [7] Y . Liu, T. Han, S. Ma, J. Zhang, Y . Yang, J. Tian, H. He, A. Li, M. He, Z. Liu, et al., Summary of chatgpt /gpt-4 research and perspective towards the future of large language models, arXiv preprint arXiv:2304.01852 (2023). [8] H. Lee, S. Yang, H. Oh, M.

**中文**

张，张平，张Q，信息检索：来自中国IR界的观点，计算机科学前沿15（2020）1-15。 [6] S.布贝克，V。 Chandrasekaran、R. Eldan、J. Gehrke、E. Horvitz、E. Kamar、P. Lee、Y。 T.李，Y. Li, S. Lundberg 等人，通用人工智能的火花：gpt-4 的早期实验，arXiv 预印本 arXiv:2303.12712 (2023)。 [7] Y.刘，韩，马，张，Y。 Yang, J. Tian, H. He, A. Li, M. He, Z. Liu, et al.，chatgpt /gpt-4 研究摘要和对大型语言模型未来的展望，arXiv 预印本 arXiv:2304.01852 (2023)。 [8] H. Lee、S. Yang、H. Oh、M.

### 段落 96 · Page 13

**EN**

Seo, Generative retrieval for long sequences, arXiv preprint arXiv:2204.13596 (2022). [9] W. Wang, X. Lin, F. Feng, X. He, T.-S. Chua, Generative recommendation: Towards next-generation recommender paradigm, arXiv preprint arXiv:2304.03516 (2023). [10] J. Zheng, M. Fischer, Bim-gpt: a prompt-based virtual assistant framework for bim information retrieval, arXiv preprint arXiv:2304.09333 (2023). [11] V . Jeronymo, L. Bonifacio, H. Abonizio, M. Fadaee, R. Lotufo, J. Zavrel, R. Nogueira, Inpars-v2: Large language models as efficient dataset generators for information retrieval, arXiv preprint arXiv:2301.01820 (2023). [12] S. Y . Kim, H. Park, K.

**中文**

Seo，长序列的生成检索，arXiv 预印本 arXiv:2204.13596 (2022)。 [9] 王伟，林晓，冯峰，何晓，T.-S。 Chua，生成推荐：走向下一代推荐范式，arXiv 预印本 arXiv:2304.03516 (2023)。 [10] J. Cheng，M. Fischer，Bim-gpt：基于提示的 bim 信息检索虚拟助手框架，arXiv 预印本 arXiv:2304.09333 (2023)。 [11] V. Jeronymo、L. Bonifacio、H. Abonizio、M. Fadaee、R. Lotufo、J. Zavrel、R. Nogueira、Inpars-v2：大型语言模型作为信息检索的高效数据集生成器，arXiv 预印本 arXiv:2301.01820 (2023)。 [12] S.Y.金，H. 帕克，K.

### 段落 97 · Page 13

**EN**

Shin, K.-M. Kim, Ask me what you need: Product retrieval using knowledge from gpt-3, arXiv preprint arXiv:2207.02516 (2022). [13] A. Edalati, M. Tahaei, A. Rashid, V . P. Nia, J. J. Clark, M. Rezagholizadeh, Kronecker decomposition for gpt compression, arXiv preprint arXiv:2110.08152 (2021). [14] H. Liu, R. Ning, Z. Teng, J. Liu, Q. Zhou, Y . Zhang, Evaluating the logical reasoning ability of chatgpt and gpt-4, arXiv preprint arXiv:2304.03439 (2023). [15] H. Nori, N. King, S. M. McKinney, D. Carignan, E. Horvitz, Capabilities of gpt-4 on medical challenge problems, arXiv preprint arXiv:2303.13375 (2023). [16] Z. Liu, X. Yu, L. Zhang, Z.

**中文**

Shin，K.-M。 Kim，问我您需要什么：使用 gpt-3 的知识进行产品检索，arXiv 预印本 arXiv:2207.02516 (2022)。 [13] A. Edalati、M. Tahaei、A. Rashid、V。 P. Nia、J. J. Clark、M. Rezagholizadeh，gpt 压缩的 Kronecker 分解，arXiv 预印本 arXiv:2110.08152 (2021)。 [14] 刘红，宁荣，滕子，刘建，周强，Y。张，评估 chatgpt 和 gpt-4 的逻辑推理能力，arXiv 预印本 arXiv:2304.03439 (2023)。 [15] H. Nori、N. King、S. M. McKinney、D. Carignan、E. Horvitz，gpt-4 在医疗挑战问题上的能力，arXiv 预印本 arXiv：2303.13375 (2023)。 [16] 刘正，余晓，张丽，Z.

### 段落 98 · Page 13

**EN**

Wu, C. Cao, H. Dai, L. Zhao, W. Liu, D. Shen, Q. Li, T. Liu, D. Zhu, X. Li, Deid-gpt: Zero-shot medical text de-identification by gpt-4, arXiv preprint arXiv:2303.11032 (2023). [17] J. Zhang, K. Bao, Y . Zhang, W. Wang, F. Feng, X. He, Is chatgpt fair for recommendation? evaluating fairness in large language model recommendation, in: Recsys, ACM, 2023. [18] A. Blair-Stanek, N. Holzenberger, B. V . Durme, Can gpt-3 perform statutory reasoning?, arXiv preprint arXiv:2302.06100 (2023). [19] C. D. Manning, P. Raghavan, H. Sch ¨utze, Introduction to Information Retrieval, Cambridge University Press, Cambridge, UK, 2008. [20] M. Kobayashi, K.

**中文**

Wu, C. Cao, H. Dai, L. Zhao, W. Liu, D. Shen, Q. Li, T. Liu, D. Zhu, X. Li, Deid-gpt：gpt-4 的零样本医学文本去识别，arXiv 预印本 arXiv:2303.11032 (2023)。 [17] 张建，包凯，Y．张，W.王，F.冯，X.何，chatgpt推荐公平吗？评估大型语言模型推荐的公平性，见：Recsys，ACM，2023。 [18] A. Blair-Stanek，N. Holzenberger，B. V . Durme，gpt-3 可以执行法定推理吗？，arXiv 预印本 arXiv:2302.06100 (2023)。 [19] C. D. Manning、P. Raghavan、H. Sch utze，《信息检索简介》，剑桥大学出版社，英国剑桥，2008 年。 [20] M. Kobayashi, K.

### 段落 99 · Page 13

**EN**

Takeda, Information retrieval on the web, ACM Comput. Surv. 32 (2) (2000) 144–173. [21] B. J. Jansen, D. L. Booth, A. Spink, Determining the user intent of web search engine queries, in: Proceedings of the 16th International Conference on World Wide Web, WWW ’07, Association for Computing Machinery, New York, NY , USA, 2007, p. 1149–1150. 13

**中文**

武田，网络信息检索，ACM Comput。幸存者。 32（2）（2000）144-173。 [21] B. J. Jansen、D. L. Booth、A. Spink，确定网络搜索引擎查询的用户意图，载于：第 16 届万维网国际会议论文集，WWW '07，计算机协会，美国纽约州纽约市，2007 年，第 11 页。 1149–1150。 13

### Page 14

### 段落 100 · Page 14

**EN**

/ AI Open 00 (2023) 1–17 14 [22] J. Teevan, S. T. Dumais, D. J. Liebling, To personalize or not to personalize: Modeling queries with variation in user intent, in: Proceedings of the 31st Annual International ACM SIGIR Conference on Research and Development in Information Retrieval, Association for Computing Machinery, 2008, p. 163–170. [23] N. Su, J. He, Y . Liu, M. Zhang, S. Ma, User intent, behaviour, and perceived satisfaction in product search, WSDM ’18, Association for Computing Machinery, New York, NY , USA, 2018, p. 547–555. [24] L. Chen, D. Zhang, L.

**中文**

/ AI Open 00 (2023) 1–17 14 [22] J. Teevan、S. T. Dumais、D. J. Liebling，个性化或不个性化：对用户意图变化的查询进行建模，见：第 31 届国际 ACM SIGIR 信息检索研究与开发年度会议论文集，计算机协会，2008 年，第 14 页。 163–170。 [23] 苏娜，何杰，Y． Liu、M. 张、S. Ma，产品搜索中的用户意图、行为和感知满意度，WSDM ’18，计算机器协会，美国纽约州纽约市，2018 年，第 12 页。 547–555。 [24] 陈立，张东，

### 段落 101 · Page 14

**EN**

Mark, Understanding user intent in community question answering, in: Proceedings of the 21st International Conference on World Wide Web, WWW ’12 Companion, Association for Computing Machinery, New York, NY , USA, 2012, p. 823–828. [25] E. Agichtein, E. Brill, S. Dumais, Improving web search ranking by incorporating user behavior information, in: Proceedings of the 29th Annual International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’06, Association for Computing Machinery, New York, NY , USA, 2006, p. 19–26. [26] E. Manavoglu, D. Pavlov, C.

**中文**

Mark，了解社区问答中的用户意图，载于：第 21 届万维网国际会议论文集，WWW '12 Companion，计算机协会，美国纽约州纽约市，2012 年，第 12 页。 823–828。 [25] E. Agichtein、E. Brill、S. Dumais，通过合并用户行为信息提高网络搜索排名，载于：第 29 届国际 ACM SIGIR 信息检索研究与开发年会论文集，SIGIR '06，计算机协会，美国纽约州纽约市，2006 年，第 17 页。 19-26。 [26] E.马纳沃格鲁，D.巴甫洛夫，C.

### 段落 102 · Page 14

**EN**

Giles, Probabilistic user behavior models, in: Third IEEE International Conference on Data Mining, 2003, pp. 203–210. [27] Q. Pi, W. Bian, G. Zhou, X. Zhu, K. Gai, Practice on long sequential user behavior modeling for click-through rate prediction, in: Proceedings of the 25th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, KDD ’19, Association for Computing Machinery, New York, NY , USA, 2019, p. 2671–2679. [28] F. Yuan, X. He, A. Karatzoglou, L.

**中文**

Giles，概率用户行为模型，载于：第三届 IEEE 国际数据挖掘会议，2003 年，第 203-210 页。 [27] Q. Pi, W. Bian, G. Zhou, X. Zhu, K. Gai，点击率预测的长序列用户行为建模实践，见：第 25 届 ACM SIGKDD 国际知识发现与数据挖掘会议论文集，KDD ’19，计算机协会，纽约，美国，2019 年，第 17 页。 2671–2679。 [28] F. Yuan, X. He, A. Karatzoglou, L.

### 段落 103 · Page 14

**EN**

Zhang, Parameter-e fficient transfer from sequential behaviors for user modeling and recommendation, SIGIR ’20, Association for Computing Machinery, New York, NY , USA, 2020, p. 1469–1478. [29] J. Yuan, Y . Zheng, X. Xie, Discovering regions of di fferent functions in a city using human mobility and pois, KDD ’12, Association for Computing Machinery, New York, NY , USA, 2012, p. 186–194. [30] Y . Zheng, X. Xie, W.-Y . Ma, Geolife: A collaborative social networking service among user, location and trajectory, IEEE Data(base) Engineering Bulletin (June 2010). [31] L. Jin, Y . Chen, T. Wang, P. Hui, A. V .

**中文**

张，用于用户建模和推荐的顺序行为的参数高效传输，SIGIR ’20，计算机协会，美国纽约，2020 年，第 12 页。 1469–1478。 [29] 袁杰.郑X.谢，利用人类流动性和点发现城市中不同功能的区域，KDD '12，计算机协会，纽约，纽约，美国，2012年，第1页。 186-194。 [30] Y.郑X.谢W.-Y。 Ma，Geolife：用户、位置和轨迹之间的协作社交网络服务，IEEE 数据（库）工程公告（2010 年 6 月）。 [31] L.金，Y。陈T.王，P.许，A.V.

### 段落 104 · Page 14

**EN**

Vasilakos, Understanding user behavior in online social networks: a survey, IEEE Communications Magazine 51 (9) (2013) 144–150. doi:10.1109/MCOM.2013.6588663. [32] A. Alfieri, R. Wolter, S. H. Hashemi, Intent disambiguation for task-oriented dialogue systems, CIKM ’22, Association for Computing Machinery, New York, NY , USA, 2022, p. 5079–5080. [33] J. Li, M. Galley, C. Brockett, G. P. Spithourakis, J. Gao, W. B.

**中文**

Vasilakos，了解在线社交网络中的用户行为：一项调查，IEEE 通信杂志 51 (9) (2013) 144–150。 doi:10.1109/MCOM.2013.6588663。 [32] A. Alfieri、R. Wolter、S. H. Hashemi，面向任务的对话系统的意图消歧，CIKM ’22，计算机协会，美国纽约州纽约市，2022 年，第 14 页。 5079–5080。 [33] J. Li、M. Galley、C. Brockett、G. P. Spithourakis、J. Gau、W. B.

### 段落 105 · Page 14

**EN**

Dolan, A persona-based neural conversation model, in: Proceedings of the 54th Annual Meeting of the Association for Computational Linguistics, ACL 2016, August 7-12, 2016, Berlin, Germany, V olume 1: Long Papers, The Association for Computer Linguistics, 2016. [34] P. Zhong, C. Zhang, H. Wang, Y . Liu, C. Miao, Towards persona-based empathetic conversational models, in: B. Webber, T. Cohn, Y . He, Y . Liu (Eds.), Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing, EMNLP 2020, Online, November 16-20, 2020, Association for Computational Linguistics, 2020, pp. 6556–6566. [35] J.

**中文**

Dolan，基于角色的神经对话模型，载于：计算语言学协会第 54 届年会论文集，ACL 2016，2016 年 8 月 7-12 日，德国柏林，第 1 卷：长论文，计算机语言学协会，2016 年。 [34] P.zhong，C.Zhang，H.Wang，Y。 Liu, C. Miao，走向基于人物角色的移情对话模型，见：B. Webber, T. Cohn, Y。嘿。刘（主编），2020 年自然语言处理经验方法会议论文集，EMNLP 2020，在线，2020 年 11 月 16-20 日，计算语言学协会，2020 年，第 6556-6566 页。 [35] J.

### 段落 106 · Page 14

**EN**

Vassileva, Motivating participation in social computing applications: a user modeling perspective, User Model. User Adapt. Interact. 22 (1-2) (2012) 177–201. [36] J. Guo, Y . Fan, L. Pang, L. Yang, Q. Ai, H. Zamani, C. Wu, W. B. Croft, X. Cheng, A deep look into neural ranking models for information retrieval, Information Processing & Management 57 (6) (2020) 102067. [37] M. Trabelsi, Z. Chen, B. D. Davison, J. Heflin, Neural ranking models for document retrieval, Inf. Retr. 24 (6) (2021) 400–444. [38] S. Robertson, H. Zaragoza, The probabilistic relevance framework: Bm25 and beyond 3 (4) (2009) 333–389. [39] Y . Freund, R. Iyer, R. E.

**中文**

Vassileva，激励参与社交计算应用程序：用户建模视角，用户模型。用户适应。相互影响。 22（1-2）（2012）177-201。 [36] 郭建, Y. Fan, L. Pang, L. Yang, Q. Ai, H. Zamani, C. Wu, W. B. Croft, X. Cheng，深入研究信息检索的神经排序模型，信息处理与管理 57 (6) (2020) 102067。 [37] M. Trabelsi, Z. Chen, B. D. Davison, J. Heflin，文档检索的神经排序模型，Inf.撤回。 24（6）（2021）400-444。 [38] S. Robertson，H. Zaragoza，概率相关性框架：Bm25 及以后 3 (4) (2009) 333–389。 [39] Y.弗罗因德，R.艾耶，R.E.

### 段落 107 · Page 14

**EN**

Schapire, Y . Singer, An efficient boosting algorithm for combining preferences, J. Mach. Learn. Res. 4 (null) (2003) 933–969. [40] C. J. C. Burges, From ranknet to lambdarank to lambdamart: An overview, 2010. [41] P.-S. Huang, X. He, J. Gao, L. Deng, A. Acero, L. Heck, Learning deep structured semantic models for web search using clickthrough data, CIKM ’13, Association for Computing Machinery, New York, NY , USA, 2013, p. 2333–2338. [42] L. Pang, Y . Lan, J. Guo, J. Xu, J. Xu, X.

**中文**

夏皮尔，Y. Singer，一种用于组合偏好的有效增强算法，J. Mach。学习。资源。 4（空）（2003）933-969。 [40] C. J. C. Burges，从ranknet到lambdarank到lambdamart：概述，2010。 [41] P.-S. Huang, X. He, J. Gau, L. Deng, A. Acero, L. Heck，使用点击数据学习网络搜索的深度结构化语义模型，CIKM ’13，计算机协会，纽约，美国，2013 年，第 14 页。 2333–2338。 [42] 庞丽.兰建国，徐建，徐建X.

### 段落 108 · Page 14

**EN**

Cheng, Deeprank: A new deep architecture for relevance ranking in information retrieval, in: Proceedings of the 2017 ACM on Conference on Information and Knowledge Management, CIKM ’17, Association for Computing Machinery, New York, NY , USA, 2017, p. 257–266. [43] J. Guo, Y . Fan, Q. Ai, W. B. Croft, A deep relevance matching model for ad-hoc retrieval, in: Proceedings of the 25th ACM International on Conference on Information and Knowledge Management, CIKM ’16, Association for Computing Machinery, New York, NY , USA, 2016, p. 55–64. [44] Y . Jiang, P. Zhang, H. Gao, D.

**中文**

Cheng，Deeprank：信息检索中相关性排名的新深度架构，载于：2017 年 ACM 信息和知识管理会议论文集，CIKM '17，计算机协会，纽约，美国，2017 年，第 17 页。 257–266。 [43] 郭杰. Fan, Q. Ai, W. B. Croft，用于即席检索的深度相关性匹配模型，载于：第 25 届 ACM 国际信息和知识管理会议论文集，CIKM '16，计算机协会，纽约，美国，2016 年，第 17 页。 55–64。 [44] Y.蒋鹏、张宏、高东.

### 段落 109 · Page 14

**EN**

Song, A quantum interference inspired neural matching model for ad-hoc retrieval, in: Proceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’20, Association for Computing Machinery, New York, NY , USA, 2020, p. 19–28. [45] Y . Fujiwara, M. Nakatsuji, H. Shiokawa, T. Mishima, M. Onizuka, Efficient ad-hoc search for personalized pagerank, in: Proceedings of the 2013 ACM SIGMOD International Conference on Management of Data, SIGMOD ’13, Association for Computing Machinery, New York, NY , USA, 2013, p. 445–456. [46] A. Karatzoglou, L. Baltrunas, Y .

**中文**

Song，一种受量子干扰启发的用于临时检索的神经匹配模型，载于：第 43 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR '20，计算机协会，美国纽约州纽约市，2020 年，第 17 页。 19-28。 [45] Y. Fujiwara、M. Nakatsuji、H. Shiokawa、T. Mishima、M. Onizuka，个性化页面排名的高效临时搜索，见：2013 年 ACM SIGMOD 国际数据管理会议记录，SIGMOD '13，计算机协会，美国纽约州纽约市，2013 年，第 14 页。 445–456。 [46] A. Karatzoglou，L. Baltrunas，Y。

### 段落 110 · Page 14

**EN**

Shi, Learning to rank for recommender systems, in: Proceedings of the 7th ACM Conference on Recommender Systems, RecSys ’13, Association for Computing Machinery, New York, NY , USA, 2013, p. 493–494. [47] S. Vargas, P. Castells, Rank and relevance in novelty and diversity metrics for recommender systems, in: Proceedings of the Fifth ACM Conference on Recommender Systems, RecSys ’11, Association for Computing Machinery, New York, NY , USA, 2011, p. 109–116. [48] K. Zhang, W. Wu, H. Wu, Z. Li, M.

**中文**

Shi，学习对推荐系统进行排名，载于：第七届 ACM 推荐系统会议论文集，RecSys '13，计算机协会，美国纽约州纽约市，2013 年，第 14 页。 493–494。 [47] S. Vargas、P. Castells，推荐系统新颖性和多样性指标的排名和相关性，载于：第五届 ACM 推荐系统会议论文集，RecSys '11，计算机协会，美国纽约州纽约市，2011 年，第 11 页。 109-116。 [48] 张凯，吴伟，吴红，李子明，

### 段落 111 · Page 14

**EN**

Zhou, Question retrieval with high quality answers in community question answering, in: Proceedings of the 23rd ACM International Conference on Conference on Information and Knowledge Management, CIKM ’14, Association for Computing Machinery, New York, NY , USA, 2014, p. 371–380. [49] L. Yang, M. Qiu, S. Gottipati, F. Zhu, J. Jiang, H. Sun, Z. Chen, Cqarank: Jointly model topics and expertise in community question answering, in: Proceedings of the 22nd ACM International Conference on Information & Knowledge Management, CIKM ’13, Association for Computing Machinery, New York, NY , USA, 2013, p. 99–108. [50] L. Ouyang, J. Wu, X. Jiang, D.

**中文**

Zhou，社区问答中高质量答案的问题检索，载于：第 23 届 ACM 国际信息和知识管理会议论文集，CIKM '14，计算机协会，纽约，美国，2014 年，第 14 页。 371–380。 [49] L. Yang、M. Qiu、S. Gottipati、F. Zhu、J. Jiang、H. Sun、Z. Chen、Cqarank：联合建模社区问答中的主题和专业知识，见：第 22 届 ACM 国际信息与知识管理会议论文集，CIKM '13，计算机协会，纽约，美国，2013 年，第 14 页。 99–108。 [50] 欧阳亮，吴建，江晓，D.

### 段落 112 · Page 14

**EN**

Almeida, C. Wainwright, P. Mishkin, C. Zhang, S. Agarwal, K. Slama, A. Ray, J. Schulman, J. Hilton, 14

**中文**

阿尔梅达、C.温赖特、P.米什金、C.张、S.阿加瓦尔、K.斯拉马、A.雷、J.舒尔曼、J.希尔顿，14

### Page 15

### 段落 113 · Page 15

**EN**

/ AI Open 00 (2023) 1–17 15 F. Kelton, L. Miller, M. Simens, A. Askell, P. Welinder, P. F. Christiano, J. Leike, R. Lowe, Training language models to follow instructions with human feedback, in: Advances in Neural Information Processing Systems, V ol. 35, 2022, pp. 27730–27744. [51] K. Duh, K. Kirchho ff, Learning to rank with partially-labeled data, in: Proceedings of the 31st Annual International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’08, Association for Computing Machinery, New York, NY , USA, 2008, p. 251–258. [52] V . Karpukhin, B. O ˘guz, S. Min, P. Lewis, L. Wu, S. Edunov, D. Chen, W.-t.

**中文**

/ AI Open 00 (2023) 1–17 15 F. Kelton、L. Miller、M. Simens、A. Askell、P. Welinder、P. F. Christiano、J. Leike、R. Lowe，训练语言模型以遵循人类反馈的指令，见：神经信息处理系统的进展，卷。 35，2022 年，第 27730–27744 页。 [51] K. Duh、K. Kirchho ff，学习对部分标记数据进行排名，载于：第 31 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR '08，计算机协会，美国纽约州纽约市，2008 年，第 11 页。 251–258。 [52] V. Karpukhin、B. O ˘guz、S. Min、P. Lewis、L. Wu、S. Edunov、D. Chen、W.-t。

### 段落 114 · Page 15

**EN**

Yih, Dense passage retrieval for open-domain question answering, arXiv preprint arXiv:2004.04906 (2020). [53] L. Zhen, P. Hu, X. Wang, D. Peng, Deep supervised cross-modal retrieval, in: Proceedings of the IEEE /CVF Conference on Computer Vision and Pattern Recognition, 2019, pp. 10394–10403. [54] G. Izacard, M. Caron, L. Hosseini, S. Riedel, P. Bojanowski, A. Joulin, E. Grave, Towards unsupervised dense information retrieval with contrastive learning, arXiv preprint arXiv:2112.09118 (2021). [55] Y . Tay, V . Tran, M. Dehghani, J. Ni, D. Bahri, H. Mehta, Z. Qin, K. Hui, Z. Zhao, J.

**中文**

Yih，开放域问答的密集段落检索，arXiv 预印本 arXiv:2004.04906 (2020)。 [53] L.Zhen，P.Hu，X.Wang，D.Peng，深度监督跨模态检索，载：IEEE /CVF计算机视觉与模式识别会议论文集，2019，第10394-10403页。 [54] G. Izacard、M. Caron、L. Hosseini、S. Riedel、P. Bojanowski、A. Joulin、E. Grave，通过对比学习实现无监督密集信息检索，arXiv 预印本 arXiv:2112.09118 (2021)。 [55] Y.泰，V. Tran、M. Dehghani、J. Ni、D. Bahri、H. Mehta、Z. 秦、K. Hui、Z. 赵、J.

### 段落 115 · Page 15

**EN**

Gupta, et al., Transformer memory as a differentiable search index, Advances in Neural Information Processing Systems 35 (2022) 21831–21843. [56] T. Brown, B. Mann, N. Ryder, M. Subbiah, J. D. Kaplan, P. Dhariwal, A. Neelakantan, P. Shyam, G. Sastry, A. Askell, et al., Language models are few-shot learners, in: NeurIPS, Curran Associates, Inc., 2020, pp. 1877–1901. [57] R. Rombach, A. Blattmann, D. Lorenz, P. Esser, B. Ommer, High-resolution image synthesis with latent diffusion models, in: CVPR, IEEE, 2022, pp. 10684–10695. [58] H. Zamani, F. Diaz, M. Dehghani, D. Metzler, M.

**中文**

Gupta 等人，Transformer 内存作为可微搜索索引，神经信息处理系统进展 35 (2022) 21831–21843。 [56] T. Brown、B. Mann、N. Ryder、M. Subbiah、J. D. Kaplan、P. Dhariwal、A. Neelakantan、P. Shyam、G. Sastry、A. Askell 等人，语言模型是小样本学习者，见：NeurIPS，Curran Associates, Inc.，2020 年，第 1877-1901 页。 [57] R. Rombach、A. Blattmann、D. Lorenz、P. Esser、B. Ommer，使用潜在扩散模型进行高分辨率图像合成，见：CVPR，IEEE，2022，第 10684–10695 页。 [58] H. Zamani、F. Diaz、M. Dehghani、D. Metzler、M.

### 段落 116 · Page 15

**EN**

Bendersky, Retrieval-enhanced machine learning, in: Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’22, Association for Computing Machinery, New York, NY , USA, 2022, p. 2875–2886.doi:10.1145/3477495.3531722. URL https://doi.org/10.1145/3477495.3531722 [59] S. Gur, N. Neverova, C. Stau ffer, S.-N. Lim, D. Kiela, A. Reiter, Cross-modal retrieval augmentation for multi-modal classification, in: Findings of the Association for Computational Linguistics: EMNLP 2021, Association for Computational Linguistics, Punta Cana, Dominican Republic, 2021, pp. 111–123.

**中文**

Bendersky，检索增强型机器学习，载于：第 45 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR '22，计算机协会，美国纽约州纽约市，2022 年，第 14 页。 2875–2886.doi:10.1145/3477495.3531722。 URL https://doi.org/10.1145/3477495.3531722 [59] S. Gur, N. Neverova, C. Stau ffer, S.-N. Lim, D. Kiela, A. Reiter，多模态分类的跨模态检索增强，见：计算语言学协会的调查结果：EMNLP 2021，计算语言学协会，多米尼加共和国蓬塔卡纳，2021 年，第 111-123 页。

### 段落 117 · Page 15

**EN**

doi:10.18653/v1/2021.findings-emnlp.11. URL https://aclanthology.org/2021.findings-emnlp.11 [60] S. Borgeaud, A. Mensch, J. Ho ffmann, T. Cai, E. Rutherford, K. Millican, G. van den Driessche, J. Lespiau, B. Damoc, A. Clark, D. de Las Casas, A. Guy, J. Menick, R. Ring, T. Hennigan, S. Huang, L. Maggiore, C. Jones, A. Cassirer, A. Brock, M. Paganini, G. Irving, O. Vinyals, S. Osindero, K. Simonyan, J. W. Rae, E. Elsen, L. Sifre, Improving language models by retrieving from trillions of tokens, arXiv preprint arXiv:2112.04426 (2021). [61] A. Santoro, S. Bartunov, M. Botvinick, D. Wierstra, T.

**中文**

doi：10.18653/v1/2021.findings-emnlp.11。 URL https://aclanthology.org/2021.findings-emnlp.11 [60] S. Borgeaud、A. Mensch、J. Ho ffmann、T. Cai、E. Rutherford、K. Millican、G. van den Driessche、J. Lespiau、B. Damoc、A. Clark、D. de Las Casas、A. Guy、J. Menick、R. Ring、T. Hennigan、 S. Huang、L. Maggiore、C. Jones、A. Cassirer、A. Brock、M. Paganini、G. Irving、O. Vinyals、S. Osindero、K. Simonyan、J. W. Rae、E. Elsen、L. Sifre，通过检索数万亿个标记来改进语言模型，arXiv 预印本 arXiv:2112.04426 (2021)。 [61] A. Santoro、S. Bartunov、M. Botvinick、D. Wierstra、T.

### 段落 118 · Page 15

**EN**

Lillicrap, Meta-learning with memory-augmented neural networks, in: Proceedings of the 33rd International Conference on International Conference on Machine Learning - V olume 48, ICML’16, JMLR.org, 2016, p. 1842–1850. [62] N. Ford, D. Miller, A. O’rourke, J. Ralph, E. Turnock, A. Booth, Information retrieval for evidence-based decision making, Journal of documentation 55 (4) (1999) 385–401. [63] D. Xu, T. Schnabel, X. Cui, S. Dean, A. Deshmukh, B. Yang, S. Yu, Foreword for workshop on decision making for information retrieval and recommender systems, in: Companion Proceedings of the ACM Web Conference 2023, 2023, pp. 920–920. [64] P.

**中文**

Lillicrap，使用记忆增强神经网络进行元学习，载于：第 33 届国际机器学习会议论文集 - 第 48 卷，ICML’16，JMLR.org，2016 年，第 14 页。 1842–1850。 [62] N. Ford、D. Miller、A. O’rourke、J. Ralph、E. Turnock、A. Booth，循证决策的信息检索，文献杂志 55 (4) (1999) 385–401。 [63] D. Xu、T. Schnabel、X. Cui、S. Dean、A. Deshmukh、B. Yang、S. Yu，信息检索和推荐系统决策研讨会前言，载于：2023 年 ACM 网络会议配套论文集，2023 年，第 920-920 页。 [64] P.

### 段落 119 · Page 15

**EN**

Borlund, Interactive information retrieval: An introduction, Journal of Information Science Theory and Practice 1 (3) (2013) 12–32. [65] H. Yin, Y . Sun, G. Xu, E. Kanoulas, Trustworthy recommendation and search: Introduction to the special issue-part 1 (2023). [66] V . Y . Tsvetkov, Cognitive science of information retrieval, European Journal of Psychological Studies (1) (2015) 37–44. [67] P. Ingwersen, Psychological aspects of information retrieval, Social Science Information Studies 4 (2-3) (1984) 83–95. [68] M. Janner, Deep generative models for decision-making and control, arXiv preprint arXiv:2306.08810 (2023). [69] D. Esposito, J.

**中文**

Borlund，交互式信息检索：简介，信息科学理论与实践杂志 1 (3) (2013) 12-32。 [65] H.尹，Y。 Sun，G. Xu，E. Kanoulas，值得信赖的推荐和搜索：特刊简介 - 第 1 部分（2023 年）。 [66] V.是的。 Tsvetkov，信息检索认知科学，欧洲心理学研究杂志 (1) (2015) 37–44。 [67] P. Ingwersen，信息检索的心理学方面，社会科学信息研究 4 (2-3) (1984) 83-95。 [68] M. Janner，决策和控制的深度生成模型，arXiv 预印本 arXiv:2306.08810 (2023)。 [69]D.埃斯波西托，J.

### 段落 120 · Page 15

**EN**

Centracchio, E. Andreozzi, G. D. Gargiulo, G. R. Naik, P. Bifulco, Biosignal-based human–machine interfaces for assistance and rehabilitation: A survey, Sensors 21 (20) (2021) 6863. [70] S. A. H. Mohsan, M. A. Khan, F. Noor, I. Ullah, M. H. Alsharif, Towards the unmanned aerial vehicles (uavs): A comprehensive review, Drones 6 (6) (2022) 147. [71] M. Zhu, S. Biswas, S. I. Dinulescu, N. Kastor, E. W. Hawkes, Y . Visell, Soft, wearable robotics and haptics: Technologies, trends, and emerging applications, Proceedings of the IEEE 110 (2) (2022) 246–272. [72] S. Mystakidis, Metaverse, Encyclopedia 2 (1) (2022) 486–497. [73] F.

**中文**

Centracchio, E. Andreozzi, G. D. Gargiulo, G. R. Naik, P. Bifulco，基于生物信号的人机界面用于援助和康复：一项调查，传感器 21 (20) (2021) 6863。 [70] S. A. H. Mohsan, M. A. Khan, F. Noor, I. Ullah, M. H. Alsharif，走向无人机（uavs）：综合综述，Drones 6 (6) (2022) 147。 [71] M. Zhu, S. Biswas, S. I. Dinulescu, N. Kastor, E. W. Hawkes, Y . Visell，软、可穿戴机器人和触觉：技术、趋势和新兴应用，IEEE 110 (2) (2022) 246-272 论文集。 [72] S. Mystakidis，Metaverse，百科全书 2 (1) (2022) 486–497。 [73]F.

### 段落 121 · Page 15

**EN**

Shenavarmasouleh, F. G. Mohammadi, M. H. Amini, H. Reza Arabnia, Embodied ai-driven operation of smart cities: A concise review, Cyberphysical Smart Cities Infrastructures: Optimal Operation and Intelligent Decision Making (2022) 29–45. [74] L. Ouyang, J. Wu, X. Jiang, D. Almeida, C. L. Wainwright, P. Mishkin, C. Zhang, S. Agarwal, K. Slama, A. Ray, J. Schulman, J. Hilton, F. Kelton, L. E. Miller, M. Simens, A. Askell, P. Welinder, P. F. Christiano, J. Leike, R. J. Lowe, Training language models to follow instructions with human feedback, in: NeurIPS, 2022. [75] R. I. John, G. J.

**中文**

Shenavarmasouleh、F. G. Mohammadi、M. H. Amini、H. Reza Arabnia，智能城市的人工智能驱动运营：简明评论，网络物理智能城市基础设施：优化运营和智能决策 (2022) 29-45。 [74] L. Ouyang、J. Wu、X. Jiang、D. Almeida、C. L. Wainwright、P. Mishkin、C. Zhuang、S. Agarwal、K. Slama、A. Ray、J. Schulman、J. Hilton、F. Kelton、L. E. Miller、M. Simens、A. Askell、P. Welinder、P. F. Christiano、J. Leike、R. J. Lowe，训练语言模型遵循人类反馈的指令，见：NeurIPS，2022。 [75] R. I. John, G. J.

### 段落 122 · Page 15

**EN**

Mooney, Fuzzy user modeling for information retrieval on the world wide web, Knowl. Inf. Syst. 3 (1) (2001) 81–95. [76] W. R. Hersh, C. Buckley, T. J. Leone, D. H. Hickam, OHSUMED: an interactive retrieval evaluation and new large test collection for research, in: Proceedings of the 17th Annual International ACM-SIGIR Conference on Research and Development in Information Retrieval, ACM/Springer, 1994, pp. 192–201. [77] S. Dennis, P. Bruza, R. McArthur, Web searching: A process-oriented experimental study of three interactive search paradigms, J. Assoc. Inf. Sci. Technol. 53 (2) (2002) 120–133. [78] Y . Guo, Z. Cheng, L. Nie, Y . Wang, J.

**中文**

Mooney，万维网上信息检索的模糊用户建模，Knowl。信息。系统。 3（1）（2001）81-95。 [76] W. R. Hersh、C. Buckley、T. J. Leone、D. H. Hickam、OHSUMED：交互式检索评估和新的大型研究测试集，载于：第 17 届国际 ACM-SIGIR 信息检索研究与开发年度会议论文集，ACM/Springer，1994 年，第 192-201 页。 [77] S. Dennis、P. Bruza、R. McArthur，网络搜索：三种交互式搜索范式的面向过程的实验研究，J. Assoc。信息。科学。技术。 53（2）（2002）120-133。 [78] Y.郭志成，聂云。王，J.

### 段落 123 · Page 15

**EN**

Ma, M. S. Kankanhalli, Attentive long short-term preference modeling for personalized product search, ACM Trans. Inf. Syst. 37 (2) (2019) 19:1–19:27. [79] K. Bao, J. Zhang, Y . Zhang, W. Wang, F. Feng, X. He, Tallrec: An e ffective and efficient tuning framework to align large language model with recommendation, in: Recsys, ACM, 2023. [80] Y . Gao, T. Sheng, Y . Xiang, Y . Xiong, H. Wang, J. Zhang, Chat-rec: Towards interactive and explainable llms-augmented recommender system, CoRR abs/2303.14524 (2023). [81] Y . Sun, X. Wang, Z. Liu, J. Miller, A. Efros, M.

**中文**

Ma，M.S. Kankanhalli，个性化产品搜索的注意力长期偏好建模，ACM Trans。信息。系统。 37（2）（2019）19：1–19：27。 [79]包康，张建，Y．张，W. Wang，F. Feng，X. He，Tallrec：一种将大型语言模型与推荐相结合的有效且高效的调优框架，见：Recsys，ACM，2023。 [80] Y。高同生 .向,Y. Xiong、H. Wang、J. Zhang，Chat-rec：迈向交互式和可解释的 llms 增强推荐系统，CoRR abs/2303.14524 (2023)。 [81] Y.孙X.王，Z.刘，J.米勒，A.埃夫罗斯，M.

### 段落 124 · Page 15

**EN**

Hardt, Test-time training with self-supervision for generalization under distribution shifts, 15

**中文**

Hardt，具有自我监督的测试时训练，以实现分布变化下的泛化，15

### Page 16

### 段落 125 · Page 16

**EN**

/ AI Open 00 (2023) 1–17 16 in: International conference on machine learning, PMLR, 2020, pp. 9229–9248. [82] J. Feng, C. Tao, X. Geng, T. Shen, C. Xu, G. Long, D. Zhao, D. Jiang, Knowledge refinement via interaction between search engines and large language models, arXiv preprint arXiv:2305.07402 (2023). [83] Y . Qin, Z. Cai, D. Jin, L. Yan, S. Liang, K. Zhu, Y . Lin, X. Han, N. Ding, H. Wang, R. Xie, F. Qi, Z. Liu, M. Sun, J. Zhou, Webcpm: Interactive web search for chinese long-form question answering, in: Proceedings of ACL 2023, Association for Computational Linguistics, 2023. [84] W. Sun, S. Guo, S. Zhang, P. Ren, Z. Chen, M.

**中文**

/ AI Open 00 (2023) 1–17 16 in：国际机器学习会议，PMLR，2020 年，第 9229–9248 页。 [82] J. Feng，C.Tao，X.Geng，T.Shen，C.Xu，G.Long，D.Zhao，D.Jiang，通过搜索引擎和大语言模型之间的交互进行知识精炼，arXiv 预印本 arXiv：2305.07402（2023）。 [83] Y.秦，蔡，金，严，梁，朱，Y。 Lin, X. Han, N. Ding, H. Wang, R. Xie, F. Qi, Z. Liu, M. Sun, J. Zhou, Webcpm: Interactive web search for chinese long-form Question Answering, in: Proceedings of ACL 2023, Association for Computational Linguistics, 2023. [84] W. Sun, S.Guo, S.Zhang, P.Ren, Z.Chen, M.

### 段落 126 · Page 16

**EN**

de Rijke, Z. Ren, Metaphorical user simulators for evaluating task-oriented dialogue systems, ACM Transactions on Information Systems (2022). [85] N. Craswell, Mean reciprocal rank, Encyclopedia of Database Systems (2009). [86] M. Zhu, Recall, precision and average precision, University of Waterloo, 2004. [87] K. J ¨arvelin, J. Kek ¨al¨ainen, Cumulated gain-based evaluation of ir techniques, ACM Transactions on Information Systems (TOIS) 20 (4) (2002) 422–446. [88] W. Sun, L. Yan, X. Ma, P. Ren, D. Yin, Z. Ren, Is chatgpt good at search? investigating large language models as re-ranking agent, arXiv preprint arXiv:2304.09542 (2023). [89] B.

**中文**

de Rijke, Z. Ren，用于评估面向任务的对话系统的隐喻用户模拟器，ACM Transactions on Information Systems (2022)。 [85] N. Craswell，平均倒数排名，数据库系统百科全书（2009）。 [86] M. Zhu，Recall，精度和平均精度，滑铁卢大学，2004 年。 [87] K. J ¡arvelin，J. Kek ¡al¡ainen，基于累积增益的红外技术评估，ACM Transactions on Information Systems (TOIS) 20 (4) (2002) 422–446。 [88] 孙文，颜丽，马晓，任鹏，殷东，任志，chatgpt 擅长搜索吗？研究大型语言模型作为重新排序代理，arXiv 预印本 arXiv:2304.09542 (2023)。 [89]B.

### 段落 127 · Page 16

**EN**

Mitra, N. Craswell, Neural models for information retrieval, CoRR abs /1705.01509 (2017). [90] J. Zhan, X. Xie, J. Mao, Y . Liu, J. Guo, M. Zhang, S. Ma, Evaluating interpolation and extrapolation performance of neural retrieval models, in: Proceedings of the 31st ACM International Conference on Information & Knowledge Management, 2022, pp. 2486–2496. [91] M. Llordes, D. Ganguly, S. Bhatia, C. Agarwal, Explain like I am BM25: interpreting a dense model’s ranked-list with a sparse approximation, CoRR abs/2304.12631 (2023). [92] K. Santhanam, J. Saad-Falcon, M. Franz, O. Khattab, A. Sil, R. Florian, M. A. Sultan, S. Roukos, M. Zaharia, C.

**中文**

Mitra, N. Craswell，信息检索神经模型，CoRR abs /1705.01509 (2017)。 [90] 詹建，谢晓，毛建，Y。 Liu，J.Guo，M.Zhang，S.Ma，评估神经检索模型的插值和外推性能，载于：第 31 届 ACM 国际信息与知识管理会议论文集，2022 年，第 2486-2496 页。 [91] M. Llordes、D. Ganguly、S. Bhatia、C. Agarwal，像我 BM25 一样解释：用稀疏近似解释密集模型的排名列表，CoRR abs/2304.12631 (2023)。 [92] K. Santhanam、J. Saad-Falcon、M. Franz、O. Khattab、A. Sil、R. Florian、M. A. Sultan、S. Roukos、M. Zaharia、C.

### 段落 128 · Page 16

**EN**

Potts, Moving beyond downstream task accuracy for information retrieval benchmarking, CoRR abs/2212.01340 (2022). [93] H. He, H. Zhang, D. Roth, Rethinking with retrieval: Faithful large language model inference, arXiv preprint arXiv:2301.00303 (2022). [94] X. Shen, Z. Chen, M. Backes, Y . Zhang, In chatgpt we trust? measuring and characterizing the reliability of chatgpt, arXiv preprint arXiv:2304.08979 (2023). [95] R. Baeza-Yates, B. Ribeiro-Neto, et al., Modern information retrieval, V ol. 463, 1999. [96] F. Radlinski, N.

**中文**

Potts，超越信息检索基准测试的下游任务准确性，CoRR abs/2212.01340 (2022)。 [93] H.He，H.Zhang，D.Roth，检索的重新思考：忠实的大语言模型推理，arXiv 预印本 arXiv：2301.00303（2022）。 [94] X.沉，Z.陈，M.巴克斯，Y。张，我们信任chatgpt吗？测量和表征 chatgpt 的可靠性，arXiv 预印本 arXiv:2304.08979 (2023)。 [95] R. Baeza-Yates、B. Ribeiro-Neto 等人，现代信息检索，卷。 463，1999。 [96]F.拉德林斯基，N.

### 段落 129 · Page 16

**EN**

Craswell, A theoretical framework for conversational search, in: Proceedings of the 2017 conference on conference human information interaction and retrieval, 2017, pp. 117–126. [97] P. Ren, Z. Chen, Z. Ren, E. Kanoulas, C. Monz, M. De Rijke, Conversations with search engines: Serp-based conversational response generation, ACM Transactions on Information Systems (TOIS) 39 (4) (2021) 1–29. [98] T. Schick, J. Dwivedi-Yu, R. Dess `ı, R. Raileanu, M. Lomeli, L. Zettlemoyer, N. Cancedda, T. Scialom, Toolformer: Language models can teach themselves to use tools, arXiv preprint arXiv:2302.04761 (2023). [99] M. Komeili, K. Shuster, J.

**中文**

Craswell，会话搜索的理论框架，载于：2017 年人类信息交互和检索会议论文集，2017 年，第 117-126 页。 [97] P. Ren、Z. Chen、Z. Ren、E. Kanoulas、C. Monz、M. De Rijke，与搜索引擎的对话：基于 Serp 的对话响应生成，ACM 信息系统交易 (TOIS) 39 (4) (2021) 1-29。 [98] T. Schick、J. Dwivedi-Yu、R. Dess `ı、R. Raileanu、M. Lomeli、L. Zettlemoyer、N. Cancedda、T. Scialom、Toolformer：语言模型可以自学使用工具，arXiv 预印本 arXiv:2302.04761 (2023)。 [99] M. Komeili，K. Shuster，J.

### 段落 130 · Page 16

**EN**

Weston, Internet-augmented dialogue generation, arXiv preprint arXiv:2107.07566 (2021). [100] A. Lazaridou, E. Gribovskaya, W. Stokowiec, N. Grigorev, Internet-augmented language models through few-shot prompting for opendomain question answering, arXiv preprint arXiv:2203.05115 (2022). [101] N. Lee, W. Ping, P. Xu, M. Patwary, P. N. Fung, M. Shoeybi, B. Catanzaro, Factuality enhanced language models for open-ended text generation, Advances in Neural Information Processing Systems 35 (2022) 34586–34599. [102] F. Petroni, T. Rockt ¨aschel, S. Riedel, P. Lewis, A. Bakhtin, Y . Wu, A.

**中文**

Weston，互联网增强对话生成，arXiv 预印本 arXiv:2107.07566 (2021)。 [100] A. Lazaridou、E. Gribovskaya、W. Stokowiec、N. Grigorev，通过少量提示进行开放域问答的互联网增强语言模型，arXiv 预印本 arXiv:2203.05115 (2022)。 [101] N. Lee、W. Ping、P. Xu、M. Patwary、P. N. Fung、M. Shoeybi、B. Catanzaro，用于开放式文本生成的 Factuality 增强语言模型，神经信息处理系统进展 35 (2022) 34586–34599。 [102] F. Petroni、T. Rockt、aschel、S. Riedel、P. Lewis、A. Bakhtin、Y。吴，A.

### 段落 131 · Page 16

**EN**

Miller, Language models as knowledge bases?, in: Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP), 2019, pp. 2463–2473. [103] G. Izacard, P. Lewis, M. Lomeli, L. Hosseini, F. Petroni, T. Schick, J. Dwivedi-Yu, A. Joulin, S. Riedel, E. Grave, Atlas: Few-shot learning with retrieval augmented language models, arXiv preprint arXiv 2208 (2022). [104] K. Guu, K. Lee, Z. Tung, P. Pasupat, M.-w. Chang, Realm: Retrieval-augmented language model pre, ICML (2020). [105] S. Borgeaud, A. Mensch, J. Ho ffmann, T. Cai, E.

**中文**

Miller，语言模型作为知识库？，载于：2019 年自然语言处理经验方法会议和第九届自然语言处理国际联合会议 (EMNLP-IJCNLP) 会议记录，2019 年，第 2463-2473 页。 [103] G. Izacard、P. Lewis、M. Lomeli、L. Hosseini、F. Petroni、T. Schick、J. Dwivedi-Yu、A. Joulin、S. Riedel、E. Grave、Atlas：利用检索增强语言模型进行少量学习，arXiv 预印本 arXiv 2208 (2022)。 [104] K. Guu、K. Lee、Z. Tung、P. Pasupat、M.-w。 Chang，Realm：检索增强语言模型预科，ICM​​L (2020)。 [105] S. Borgeaud、A. Mensch、J. Ho ffmann、T. Cai、E.

### 段落 132 · Page 16

**EN**

Rutherford, K. Millican, G. B. Van Den Driessche, J.-B. Lespiau, B. Damoc, A. Clark, et al., Improving language models by retrieving from trillions of tokens, in: International conference on machine learning, PMLR, 2022, pp. 2206–2240. [106] B. Wang, W. Ping, P. Xu, L. McAfee, Z. Liu, M. Shoeybi, Y . Dong, O. Kuchaiev, B. Li, C. Xiao, et al., Shall we pretrain autoregressive language models with retrieval? a comprehensive study, arXiv preprint arXiv:2304.06762 (2023). [107] C. Xu, Q. Li, J. Ge, J. Gao, X. Yang, C. Pei, F. Sun, J. Wu, H. Sun, W.

**中文**

卢瑟福，K.米利肯，G.B.范登德里斯切，J.-B。 Lespiau、B. Damoc、A. Clark 等人，通过从数万亿个标记中检索来改进语言模型，载于：国际机器学习会议，PMLR，2022 年，第 2206-2240 页。 [106] B. Wang、W. Ping、P. Xu、L. McAfee、Z. Liu、M. Shoeybi、Y。 Dong, O. Kuchaiev, B. Li, C. Xiao, et al.，我们应该通过检索来预训练自回归语言模型吗？一项综合研究，arXiv 预印本 arXiv:2304.06762 (2023)。 [107] 徐成，李强，葛建，高建，杨旭，裴成，孙凤，吴建，孙红，W.

### 段落 133 · Page 16

**EN**

Ou, Privileged features distillation at taobao recommendations, in: Proceedings of the 26th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, 2020, pp. 2590–2598. [108] R. Nakano, J. Hilton, S. Balaji, J. Wu, L. Ouyang, C. Kim, C. Hesse, S. Jain, V . Kosaraju, W. Saunders, et al., Webgpt: Browser-assisted question-answering with human feedback, arXiv preprint arXiv:2112.09332 (2021). [109] J. He, C. Zhou, X. Ma, T. Berg-Kirkpatrick, G. Neubig, Towards a unified view of parameter-e fficient transfer learning, in: International Conference on Learning Representations, 2022. [110] Z. Hu, Y . Lan, L. Wang, W. Xu, E.-P.

**中文**

Ou，Privileged 在淘宝推荐中进行了蒸馏，见：第 26 届 ACM SIGKDD 国际知识发现与数据挖掘会议论文集，2020 年，第 2590-2598 页。 [108] R. Nakano、J. Hilton、S. Balaji、J. Wu、L. Ouyang、C. Kim、C. Hesse、S. Jain、V。 Kosaraju、W. Saunders 等人，Webgpt：带有人类反馈的浏览器辅助问答，arXiv 预印本 arXiv：2112.09332 (2021)。 [109] J. He、C. Zhou、X. Ma、T. Berg-Kirkpatrick、G. Neubig，走向参数高效迁移学习的统一观点，见：国际学习表示会议，2022。 [110] Z. Hu, Y .兰，王，徐，E.-P。

### 段落 134 · Page 16

**EN**

Lim, R. K.-W. Lee, L. Bing, S. Poria, Llm-adapters: An adapter family for parameter-e fficient fine-tuning of large language models, arXiv preprint arXiv:2304.01933 (2023). [111] X. L. Li, P. Liang, Prefix-tuning: Optimizing continuous prompts for generation, in: Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (V olume 1: Long Papers), 2021, pp. 4582–4597. [112] X. Liu, K. Ji, Y . Fu, W. Tam, Z. Du, Z. Yang, J.

**中文**

林，R.K.-W。 Lee, L. Bing, S. Poria，Llm-adapters：用于对大型语言模型进行参数高效微调的适配器系列，arXiv 预印本 arXiv:2304.01933 (2023)。 [111] X. L. Li, P. Liang，前缀调优：优化连续提示生成，见：计算语言学协会第 59 届年会和第 11 届自然语言处理国际联合会议论文集（第一卷：长论文），2021 年，第 4582-4597 页。 [112] 刘X.，季坤，Y.付伟谭、杜子正、杨正杰

### 段落 135 · Page 16

**EN**

Tang, P-tuning: Prompt tuning can be comparable to fine-tuning across scales and tasks, in: Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (V olume 2: Short Papers), 2022, pp. 61–68. [113] X. Liu, Y . Zheng, Z. Du, M. Ding, Y . Qian, Z. Yang, J. Tang, Gpt understands, too, arXiv preprint arXiv:2103.10385 (2021). [114] B. Lester, R. Al-Rfou, N. Constant, The power of scale for parameter-e fficient prompt tuning, in: Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing, 2021, pp. 3045–3059. [115] N. Houlsby, A. Giurgiu, S. Jastrzebski, B. Morrone, Q. De Laroussilhe, A.

**中文**

Tang，P 调优：即时调优可与跨尺度和任务的微调相媲美，见：计算语言学协会第 60 届年会论文集（第 2 卷：短论文），2022 年，第 61-68 页。 [113] X.刘，Y。郑Z.杜，M.丁Y。 Qian、Z. Yang、J. Tang、Gpt 也理解 arXiv 预印本 arXiv:2103.10385 (2021)。 [114] B. Lester、R. Al-Rfou、N. Constant，参数高效提示调整的规模力量，见：2021 年自然语言处理经验方法会议论文集，2021 年，第 3045-3059 页。 [115] N. Houlsby、A. Giurgiu、S. Jastrzebski、B. Morrone、Q. De Laroussilhe、A.

### 段落 136 · Page 16

**EN**

Gesmundo, M. Attariyan, S. Gelly, Parameter-e fficient transfer learning for nlp, in: International Conference on Machine Learning, 2019, pp. 2790–2799. 16

**中文**

Gesmundo、M. Attariyan、S. Gelly，nlp 的参数高效迁移学习，见：国际机器学习会议，2019 年，第 2790-2799 页。 16

### Page 17

### 段落 137 · Page 17

**EN**

/ AI Open 00 (2023) 1–17 17 [116] J. Pfei ffer, A. Kamath, A. R¨uckl´e, K. Cho, I. Gurevych, AdapterFusion: Non-destructive task composition for transfer learning, in: Proceedings of the 16th Conference of the European Chapter of the Association for Computational Linguistics: Main V olume, 2021, pp. 487–503. [117] Q. Zhang, M. Chen, A. Bukharin, P. He, Y . Cheng, W. Chen, T. Zhao, Adaptive budget allocation for parameter-efficient fine-tuning, arXiv preprint arXiv:2303.10512 (2023). [118] E. J. Hu, Y . Shen, P. Wallis, Z. Allen-Zhu, Y . Li, S. Wang, L. Wang, W.

**中文**

/ AI Open 00 (2023) 1–17 17 [116] J. Pfei ffer, A. Kamath, A. R´uckl´e, K. Cho, I. Gurevych, AdapterFusion: 用于迁移学习的非破坏性任务组合，载于：计算语言学协会欧洲分会第 16 届会议论文集：主卷，2021 年，第 487–503 页。 [117]张问，陈明，布哈林，何平，Y． Cheng、W. Chen、T. Zhu，参数高效微调的自适应预算分配，arXiv 预印本 arXiv:2303.10512 (2023)。 [118] E.J.胡，Y。 Shen, P. Wallis, Z. Allen-Zhu, Y .李，王，L.，王，W.

### 段落 138 · Page 17

**EN**

Chen, Lora: Low-rank adaptation of large language models, arXiv preprint arXiv:2106.09685 (2021). [119] K. Shuster, M. Komeili, L. Adolphs, S. Roller, A. Szlam, J. Weston, Language models that seek for knowledge: Modular search & generation for dialogue and prompt completion, arXiv preprint arXiv:2203.13224 (2022). [120] O. Ram, Y . Levine, I. Dalmedigos, D. Muhlgay, A. Shashua, K. Leyton-Brown, Y . Shoham, In-context retrieval-augmented language models, arXiv preprint arXiv:2302.00083 (2023). [121] B. Peng, M. Galley, P. He, H. Cheng, Y . Xie, Y . Hu, Q. Huang, L. Liden, Z. Yu, W. Chen, J.

**中文**

Chen, Lora：大型语言模型的低阶适应，arXiv 预印本 arXiv:2106.09685 (2021)。 [119] K. Shuster、M. Komeili、L. Adolphs、S. Roller、A. Szlam、J. Weston，寻求知识的语言模型：对话和提示完成的模块化搜索和生成，arXiv 预印本 arXiv：2203.13224 (2022)。 [120] O.拉姆，Y。 Levine，I. Dalmedigos，D. Muhlgay，A. Shashua，K. Leyton-Brown，Y。 Shoham，上下文检索增强语言模型，arXiv 预印本 arXiv:2302.00083 (2023)。 [121] B.彭，M.加利，P.何，H.程，Y。谢Y.胡庆，黄，L，利登，于Z，W，陈，J。

### 段落 139 · Page 17

**EN**

Gao, Check your facts and try again: Improving large language models with external knowledge and automated feedback, arXiv preprint arXiv:2302.12813 (2023). 17

**中文**

高，检查你的事实，然后再试一次：利用外部知识和自动反馈改进大型语言模型，arXiv 预印本 arXiv:2302.12813 (2023)。 17 号
