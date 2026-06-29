# A Survey of Long-Document Retrieval in the PLM and LLM Era

- ID: 84
- 类型: pdf
- 分类: 04_academic_papers
- 主题: long-document retrieval and chunking
- 原文链接: https://arxiv.org/pdf/2509.07759
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era MINGHAN LI,School of Computer Science and Technology, Soochow University, China MIYANG LUO,School of Computer Science and Technology, Soochow University, China TIANRUI LV,School of Computer Science and Technology, Soochow University, China YISHUAI ZHANG,School of Computer Science and Technology, Soochow University, China SIQI ZHAO,School of Computer Science and Technology, Soochow University, China ERCONG NIE,Center for Information and Language Processing (CIS), LMU Munich, Germany and Munich Center for Machine Learning (MCML), Germany GUODONG ZHOU,School of Computer Science and Technology, Soochow University, China The rapid growth of long-form documents presents a fundamental challenge to information retrieval (IR).

**中文**

PLM和LLM时代的长文献检索综述 李明汉，苏州大学计算机科学与技术学院 罗米阳，苏州大学计算机科学与技术学院 吕天瑞，苏州大学计算机科学与技术学院 张一帅，苏州大学计算机科学与技术学院 赵思琪，计算机科学与技术学院聂尔聪，德国慕尼黑大学信息与语言处理中心 (CIS) 和德国慕尼黑机器学习中心 (MCML) 周国栋，苏州大学计算机科学与技术学院 长篇文档的快速增长对信息检索 (IR) 提出了根本性挑战。

### 段落 2 · Page 1

**EN**

Their length, dispersed evidence, and complex structures demand approaches that go beyond standard passage-level techniques. This survey provides a comprehensive survey of long-document retrieval (LDR) and organizes existing work into three major eras of development. The survey traces progress from classical lexical and early neural models to pre-trained language models (PLMs) and large language models (LLMs). It highlights core paradigms such as passage aggregation, hierarchical encoding, efficient attention, and LLM-driven re-ranking and retrieval.

**中文**

它们的长度、分散的证据和复杂的结构需要超越标准段落级别技术的方法。这项调查对长文档检索（LDR）进行了全面的调查，并将现有工作分为三个主要的发展时代。该调查追踪了从经典词汇和早期神经模型到预训练语言模型 (PLM) 和大型语言模型 (LLM) 的进展。它强调了核心范例，例如段落聚合、分层编码、高效注意力以及法学硕士驱动的重新排序和检索。

### 段落 3 · Page 1

**EN**

In addition to methods, the survey summarizes domain-specific applications, available evaluation resources, and the benchmarks that shape empirical study. It identifies open challenges related to efficiency trade-offs, evidence localization, multimodal alignment, and interpretability. The survey primarily focuses on methodological advances, while also considering practical applications in diverse domains.

**中文**

除了方法之外，调查还总结了特定领域的应用、可用的评估资源以及形成实证研究的基准。它确定了与效率权衡、证据本地化、多模式对齐和可解释性相关的开放挑战。该调查主要关注方法论的进步，同时也考虑不同领域的实际应用。

### 段落 4 · Page 1

**EN**

The principal conclusion is that future progress in LDR will depend on hybrid solutions that combine sub-linear indexing, structure-aware modeling, and LLM-based reasoning, as identified through the methods and challenges systematized in this survey. CCS Concepts:•Information systems→Retrieval models and ranking.

**中文**

主要结论是，LDR 的未来进展将取决于结合了次线性索引、结构感知建模和基于 LLM 的推理的混合解决方案，正如本次调查中系统化的方法和挑战所确定的那样。 CCS概念：•信息系统→检索模型和排序。

### 段落 5 · Page 1

**EN**

Additional Key Words and Phrases: Information Retrieval, Long-Document Retrieval, Long-Context Models, Evaluation Benchmarks, Domain-Specific Retrieval, Reranking Models 1 Introduction and Contribution From locating a single critical clause in a multi-hundred-page legal contract to synthesizing evidence from thousands of biomedical research papers, the ability to retrieve precise information from long-form documents has become a foundational challenge in the modern information landscape.

**中文**

其他关键词和短语：信息检索、长文档检索、长上下文模型、评估基准、特定领域检索、重排序模型 1 简介和贡献 从在数百页法律合同中定位单个关键条款到综合数千篇生物医学研究论文中的证据，从长格式文档中检索精确信息的能力已成为现代信息领域的基本挑战。

### 段落 6 · Page 1

**EN**

The exponential growth of digital information has yielded corpora where such documents-scientific articles and patents, statutes and judicial opinions, financial and technical reports, clinical notes, books, and multimedia-rich web pages are the primary carriers of knowledge. These artifacts routinely span thousands to tens of thousands of tokens and exhibit rich internal structure. Retrieving evidence from such materials are foundational to web search, legal discovery, scientific knowledge mining, clinical decision support, and enterprise intelligence.

**中文**

数字信息的指数增长产生了语料库，其中诸如科学文章和专利、法规和司法意见、财务和技术报告、临床笔记、书籍和多媒体丰富的网页等文档是知识的主要载体。这些文物通常涵盖数千到数万个标记，并表现出丰富的内部结构。从此类材料中检索证据是网络搜索、法律发现、科学知识挖掘、临床决策支持和企业智能的基础。

### 段落 7 · Page 1

**EN**

Yet the very properties that make long documents valuable, such as distributed evidence, Authors’ Contact Information: Minghan Li, mhli@suda.edu.cn, School of Computer Science and Technology, Soochow University, Suzhou, Jiangsu, China; Miyang Luo, myluo@stu.suda.edu.cn, School of Computer Science and Technology, Soochow University, Suzhou, Jiangsu, China; Tianrui Lv, trlvtrlv@stu.

**中文**

然而，正是使长文档变得有价值的属性，例如分布式证据，作者联系信息：Minghan Li，mhli@suda.edu.cn，苏州大学计算机科学与技术学院，苏州，江苏，中国； Miyang Luo，myluo@stu.suda.edu.cn，苏州大学计算机科学与技术学院，江苏苏州；吕天瑞，trlvtrlv@stu。

### 段落 8 · Page 1

**EN**

suda.edu.cn, School of Computer Science and Technology, Soochow University, Suzhou, Jiangsu, China; Yishuai Zhang, yszhang13@stu.suda.edu.cn, School of Computer Science and Technology, Soochow University, Suzhou, Jiangsu, China; Siqi Zhao, sqzhaosqzhao@stu.suda.edu.cn, School of Computer Science and Technology, Soochow University, Suzhou, Jiangsu, China; Ercong Nie, nie@cis.lmu.de, Center for Information and Language Processing (CIS), LMU Munich, Munich, Germany and Munich Center for Machine Learning (MCML), Munich, Germany; Guodong Zhou, gdzhou@suda.edu.cn, School of Computer Science and Technology, Soochow University, Suzhou, Jiangsu, China.

**中文**

suda.edu.cn，苏州大学计算机科学与技术学院，江苏苏州；张一帅，yszhang13@stu.suda.edu.cn，苏州大学计算机科学与技术学院，江苏苏州；赵思琪，sqzhaosqzhao@stu.suda.edu.cn，苏州大学计算机科学与技术学院，江苏苏州； Ercong Nie, nie@cis.lmu.de，德国慕尼黑慕尼黑大学信息和语言处理中心 (CIS) 和德国慕尼黑机器学习中心 (MCML)；周国栋，gdzhou@suda.edu.cn，苏州大学计算机科学与技术学院，江苏苏州，中国。

### 段落 9 · Page 1

1 arXiv:2509.07759v2 [cs.IR] 25 Oct 2025

### Page 2

### 段落 10 · Page 2

**EN**

2 Li et al. hierarchical organization, and inter-document linkage, also make them challenging for conventional information retrieval pipelines. We study long-document retrieval : given a query𝑞 and a corpus D of long documents, the system returns a ranking over documents or intra-document units , ideally with span-level rationales. In practice, indices are built at multiple granularities, and relevance must couple document-level utility with coverage of supportive segments.

**中文**

2 李等人。分层组织和文档间链接也使它们对传统的信息检索管道提出了挑战。我们研究长文档检索：给定查询𝑞和长文档的语料库 D，系统返回文档或文档内单元的排名，最好具有跨级别的基本原理。在实践中，索引是在多个粒度上构建的，并且相关性必须将文档级实用性与支持性细分的覆盖范围结合起来。

### 段落 11 · Page 2

**EN**

LDR departs from standard ad hoc retrieval along three axes: (i) evidence dispersion, where relevant signals are scattered across many segments and must be aggregated; (ii) hierarchical and cross-document structure, where headings, citations, hyperlinks, and version graphs condition relevance; and (iii) computational constraints, since encoder and interaction costs scale unfavorably with length unless architectures or pipelines are adapted. The problem further generalizes to long-query regimes and to multimodal documents.

**中文**

LDR 在三个轴上偏离了标准的临时检索：(i) 证据分散，相关信号分散在许多部分，必须进行聚合； (ii) 分层和跨文档结构，其中标题、引文、超链接和版本图决定相关性； (iii) 计算限制，因为编码器和交互成本会随着长度的增加而不利地扩展，除非架构或管道进行了调整。该问题进一步推广到长查询机制和多模式文档。

### 段落 12 · Page 2

**EN**

Classical lexical methods are robust and efficient but degrade on long texts due to verbosity bias, topical drift, and an inability to model cross-segment dependencies. Early neural rankers improve matching at paragraph scale but remain bounded by input windows and quadratic attention, while naïve truncation or sliding-window heuristics sacrifice global coherence and induce ordering bias. These limitations have driven three waves of techniques that progressively address LDR-specific challenges. The PLM era extended pretrained transformer encoders to long inputs through three key innovations.

**中文**

经典的词汇方法稳健且高效，但由于冗长偏差、主题漂移以及无法对跨段依赖关系进行建模，因此在长文本上性能会下降。早期的神经排序器改善了段落规模的匹配，但仍然受到输入窗口和二次注意力的限制，而朴素的截断或滑动窗口启发式牺牲了全局一致性并引起排序偏差。这些限制催生了三波技术浪潮，逐步解决 LDR 特定的挑战。 PLM 时代通过三项关键创新将预训练Transformer编码器扩展到长输入。

### 段落 13 · Page 2

**EN**

First, passage-based "divide-and-conquer" strategies learned to aggregate scores from individual chunks, as seen in models like BERT-MaxP/SumP and PARADE. Second, hierarchical models were developed to pool information over a document’s explicit structure, with examples including KeyB and IDCM. Third, sparse and efficient attention mechanisms, such as those in Longformer and BigBird, were introduced to mitigate the quadratic cost of processing long sequences.

**中文**

首先，基于段落的“分而治之”策略学会了聚合各个块的分数，如 BERT-MaxP/SumP 和 PARADE 等模型中所示。其次，开发了分层模型来汇集文档显式结构的信息，例如 KeyB 和 IDCM。第三，引入了稀疏而高效的注意力机制，例如 Longformer 和 BigBird 中的机制，以减轻处理长序列的二次成本。

### 段落 14 · Page 2

**EN**

Building on these foundations, the LLM era has introduced instruction-following models for two primary roles: as powerful re-rankers, exemplified by listwise prompting approaches like RankGPT, and through fine-tuning as end-to-end retrievers, such as the bi-encoder variants RepLLaMA and RankLLaMA. This new wave is also accompanied by system-level innovations for long-context efficiency, including sparse attention for LLMs, prompt compression, and KV-cache reuse. Evaluation for LDR requires care. Label sparsity in web- and enterprise-scale testbeds, mixed relevance units , and graded judgments complicate standard metrics.

**中文**

在此基础上，LLM 时代引入了两个主要角色的指令跟踪模型：作为强大的重新排序器，例如 RankGPT 等列表提示方法，以及作为端到端检索器的微调，例如双编码器变体 RepLLaMA 和 RankLLaMA。这一新浪潮还伴随着长上下文效率的系统级创新，包括 LLM 的稀疏关注、即时压缩和 KV 缓存重用。 LDR 的评估需要谨慎。网络和企业规模测试平台中的标签稀疏性、混合相关性单元和分级判断使标准指标变得复杂。

### 段落 15 · Page 2

**EN**

Beyond document-level nDCG/MAP/MRR, segment-level adaptations and hierarchical recall are often necessary, especially under partial judgments. Specialized protocols address long-query QBD settings and structure- or layout-aware retrieval where section anchors and page elements govern relevance. Recent datasets also target cross-lingual and multimodal regimes, aligning assessments with realistic use. The methodologies reviewed in this survey are directly motivated by applications in which document longness is an intrinsic challenge.

**中文**

除了文档级 nDCG/MAP/MRR 之外，段级适应和分层召回通常也是必要的，尤其是在部分判断的情况下。专门的协议解决长查询 QBD 设置和结构或布局感知检索，其中部分锚点和页面元素控制相关性。最近的数据集还针对跨语言和多模式制度，使评估与实际使用保持一致。本次调查中审查的方法直接受到应用程序的推动，在这些应用程序中，文档长度是一个固有的挑战。

### 段落 16 · Page 2

**EN**

Legal retrieval requires case-to-case matching, statute version alignment, and multi-source research over documents with rhetorical roles and dense citation/version graphs. Biomedical literature search and clinical decision support rely on full-text evidence localization across PubMed/PMC and EHRs, increasingly with multimodal signals. Web search must retrieve from long-form news features and technical white papers, often aligning text with images, tables, or embedded media.

**中文**

法律检索需要个案匹配、法规版本对齐以及对具有修辞角色和密集引文/版本图的文档进行多源研究。生物医学文献检索和临床决策支持依赖于 PubMed/PMC 和 EHR 中的全文证据本地化，并且越来越多地使用多模态信号。网络搜索必须从长篇新闻专题和技术白皮书中检索，通常将文本与图像、表格或嵌入媒体对齐。

### 段落 17 · Page 2

**EN**

Scientific paper retrieval benefits from document-level representations informed by citation signals and LLM-guided concept indices, while cross-lingual LDR requires bridging languages without losing span-level provenance. Across these domains, effective systems preserve hierarchy, aggregate dispersed evidence, and provide auditable rationales.

**中文**

科学论文检索受益于由引文信号和法学硕士指导的概念索引提供的文档级表示，而跨语言 LDR 则需要在不丢失跨度级别出处的情况下桥接语言。在这些领域中，有效的系统保留层次结构，聚合分散的证据，并提供可审计的理由。

### Page 3

### 段落 18 · Page 3

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 3 Positioning Against Existing Surveys While comprehensive surveys exist for the broader fields of neural information retrieval [32], efficient Transformer architectures [78], and the general application of large language models to information retrieval [ 98], these works typically address long contexts as one of many challenges rather than as the central focus.

**中文**

PLM 和 LLM 时代长文档检索的调查 3 针对现有调查的定位 虽然神经信息检索 [32]、高效 Transformer 架构 [78] 以及大型语言模型在信息检索中的一般应用等更广泛领域存在综合调查 [98]，但这些工作通常将长上下文作为众多挑战之一而不是中心焦点。

### 段落 19 · Page 3

**EN**

Consequently, they do not provide a unified, end-to-end treatment of the specific problems intrinsic to LDR, such as evidence dispersion across vast texts, hierarchical structure modeling, and the evolution of evaluation protocols tailored for long-form content. To the best of our knowledge, this is the first survey to offer a holistic and consolidated view specifically onlongdocument retrieval, tracing its progression across three distinct eras: from classical lexical models to the latest PLM and LLM-based paradigms.

**中文**

因此，它们没有为 LDR 固有的特定问题提供统一的端到端处理，例如大量文本中的证据分散、层次结构建模以及为长格式内容量身定制的评估协议的演变。据我们所知，这是第一项针对长文档检索提供全面、综合观点的调查，追踪其在三个不同时代的进展：从经典词汇模型到最新的 PLM 和基于 LLM 的范式。

### 段落 20 · Page 3

**EN**

Our work distinguishes itself by not only systematizing the models but also providing integrated guidance on domain-specific applications, evaluation benchmarks, and a forward-looking research agenda, thus offering a complete reference for the field. Contributions To provide a clear roadmap for researchers and practitioners and to catalyze future innovation, this survey makes the following key contributions: • Unified problem formulation.We formalize LDR across document-, passage-, and layout-level targets under both short- and long-query regimes (including QBD), providing a common framework to connect previously fragmented research threads.

**中文**

我们的工作不仅使模型系统化，而且还提供特定领域应用的综合指导、评估基准和前瞻性研究议程，从而为该领域提供完整的参考。贡献 为了为研究人员和从业者提供清晰的路线图并促进未来的创新，本次调查做出了以下主要贡献： • 统一问题表述。我们在短查询和长查询制度（包括 QBD）下将跨文档、段落和布局级别目标的 LDR 形式化，提供了一个通用框架来连接以前分散的研究线索。

### 段落 21 · Page 3

**EN**

• Taxonomy across three eras.We systematize methods from lexical and early neural baselines to PLM-based passage/hierarchical/sparse-attention models and LLM-based retrievers/rerankers, clarifying how each class combats segment dilution, preserves global coherence, and manages computational cost. • Holistic relevance in the LLM era.We identify the field’s paradigm shift from local window voting to instruction-aligned, global modeling with span-grounded justification, analyzing listwise vs. pairwise prompting, calibration of LLM judgments, and hallucination risks.

**中文**

• 跨越三个时代的分类法。我们对从词汇和早期神经基线到基于 PLM 的段落/分层/稀疏注意力模型和基于 LLM 的检索器/重新排序器的方法进行系统化，阐明每个类别如何对抗片段稀释、保持全局一致性和管理计算成本。 • LLM 时代的整体相关性。我们确定了该领域的范式转变，从本地窗口投票到指令一致、具有跨度理由的全局建模、分析列表与成对提示、LLM 判断的校准和幻觉风险。

### 段落 22 · Page 3

**EN**

• Efficiency principles for long contexts.We distill design patterns: sparse attention, hierarchical pooling, query-focused routing, prompt compression, KV-cache reuse, and relate them to first-stage recall, re-ranking, and reading/generation. • Application blueprints.We present end-to-end system frameworks for settings such as law, biomedicine, and academia, which combine structure-aware indexing, graph-informed expansion, long-context re-ranking, and span-grounded generation, tied to domain constraints.

**中文**

• 长上下文的效率原则。我们提炼设计模式：稀疏注意力、分层池化、以查询为中心的路由、提示压缩、KV 缓存重用，并将它们与第一阶段召回、重新排序和读取/生成相关联。 • 应用蓝图。我们提出了适用于法律、生物医学和学术界等环境的端到端系统框架，该框架结合了结构感知索引、图形通知扩展、长上下文重新排序和跨度生成，并与领域约束相关联。

### 段落 23 · Page 3

**EN**

• A forward-looking research agenda.We articulate critical gaps in the field, including label sparsity, robust long-query handling, faithful multimodal retrieval, and efficiency-effectiveness trade-offs, outlining promising directions for future work. Roadmap. The survey first reviews pre-PLM baselines, then covers PLM-based LDR and LLM-based retrievers/rerankers with efficiency innovations and multimodal extensions. We next provide a comparative analysis, summarize datasets and evaluation protocols, and detail application blueprints in law, biomedicine, web/news, scientific retrieval, and cross-lingual settings.

**中文**

• 前瞻性的研究议程。我们阐明了该领域的关键差距，包括标签稀疏性、强大的长查询处理、忠实的多模态检索以及效率与效果的权衡，概述了未来工作的有希望的方向。路线图。该调查首先回顾了 PLM 之前的基线，然后涵盖基于 PLM 的 LDR 和基于 LLM 的检索器/重新排序器以及效率创新和多模式扩展。接下来，我们提供比较分析，总结数据集和评估协议，并详细介绍法律、生物医学、网络/新闻、科学检索和跨语言设置中的应用蓝图。

### 段落 24 · Page 3

**EN**

We conclude with open challenges and a research agenda.

**中文**

最后我们提出了公开的挑战和研究议程。

### Page 4

### 段落 25 · Page 4

**EN**

4 Li et al. Fig. 1. In queries targeting long documents, a comparison between general retrieval methods and long-document retrieval methods reveals distinct differences: general retrieval methods struggle to acquire and present detailed, scattered information within long documents, whereas long-document retrieval methods excel at retrieving and organizing in-depth content from large volumes of textual resources. 2 Problem Scope And Definition Long-Document Retrieval is an important branch task in information retrieval.

**中文**

4 李等人。图1. 在针对长文档的查询中，通用检索方法和长文档检索方法之间的比较显示出明显的差异：通用检索方法难以获取和呈现长文档中详细的、分散的信息，而长文档检索方法擅长从大量文本资源中检索和组织深度内容。 2 问题范围和定义长文档检索是信息检索中的一个重要分支任务。

### 段落 26 · Page 4

**EN**

Its goal is to retrieve the most relevant documents or document fragments based on the user’s query when facing a corpus containing a large number of long documents. Compared with classic document retrieval or paragraph retrieval tasks, LDR is unique in that it not only requires accurate identification of relevant information in a large document, but also requires efficient processing of redundant information and structural complexity while maintaining semantic integrity. As illustrated in Fig. 1 , a clear distinction emerges between two types of retrieval methods when the query target is information within long documents.

**中文**

其目标是在面对包含大量长文档的语料库时，根据用户的查询检索最相关的文档或文档片段。与经典的文档检索或段落检索任务相比，LDR的独特之处在于它不仅需要准确识别大型文档中的相关信息，而且需要高效处理冗余信息和结构复杂性，同时保持语义完整性。如图1所示，当查询目标是长文档中的信息时，两种检索方法之间出现了明显的区别。

### 段落 27 · Page 4

**EN**

General retrieval methods struggle to capture scattered and detailed information completely, making it difficult to extract key content from long documents and present it effectively. In contrast, long-document retrieval methods are specifically designed to address this issue. Their core strength lies in the ability to accurately retrieve deep information from large-scale textual resources and organize such information in a structured manner, thereby fulfilling query requirements in long-document scenarios.

**中文**

常规检索方法难以完整捕捉分散而详细的信息，难以从长文档中提取关键内容并有效呈现。相比之下，长文档检索方法是专门为解决这个问题而设计的。它们的核心优势在于能够从大规模文本资源中准确检索深层信息，并以结构化方式组织这些信息，从而满足长文档场景的查询需求。

### 段落 28 · Page 4

**EN**

The figure visually demonstrates the irreplaceability of long-document retrieval methods in specific contexts and provides clear guidance for the design of future methods. This capability gap also explains why "long documents" need to be defined from multiple dimensions (length, structure, and semantics). These characteristics are exactly the root causes of the ineffectiveness of general retrieval methods. Currently, there is no unified standard for the definition of "long documents".

**中文**

该图直观地展示了长文档检索方法在特定上下文中的不可替代性，并为未来方法的设计提供了明确的指导。这种能力差距也解释了为什么“长文档”需要从多个维度（长度、结构、语义）进行定义。这些特点正是导致一般检索方法无效的根本原因。目前，对于“长文档”的定义还没有统一的标准。

### 段落 29 · Page 4

**EN**

Research usually defines it based on the following dimensions: (1) Length dimension: The document length far exceeds the maximum input limit of the standard Transformer model , often ranging from thousands to tens of thousands of tokens; (2) Structural

**中文**

研究通常根据以下维度来定义：（1）长度维度：文档长度远远超过标准Transformer模型的最大输入限制，往往从数千到数万个token不等； (2) 结构

### Page 5

### 段落 30 · Page 5

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 5 Long-DocumentRetrieval Pre-PLM Era(Sec 3) Lexical Methods(Sec 3.1) TF-IDF [42], BM25 [67], Heuristic Chunking [11] Early Neural IR(Sec 3.2) DSSM [36], DRMM [31], MatchPyramid [62], PACRR [37], DeepRank [63] Core ParadigmsPLM & LLM Era(Sec 4) The Holistic Paradigm(Sec 4.1) Naive Truncation: DPR [43], ANCE [88] Long-Sequence Transformers: Longformer [8], BigBird [92], Reformer [45], FlashAttention [22],LongNet [25], LONGEMBED [97], M3-Embedding [14], QDS-Transformer [40], Socialformer [95] LLMs as Rerankers: RankGPT [77], RepLLaMA/RankLLaMA [58] Efficiency Mitigation: LongLoRA [15], L

**中文**

PLM 和 LLM 时代的长文档检索综述 5 前 PLM 时代的长文档检索（第 3 节） 词汇方法（第 3.1 节） TF-IDF [42]、BM25 [67]、启发式分块 [11] 早期神经 IR（第 3.2 节） DSSM [36]、DRMM [31]、MatchPyramid [62]、PACRR [37]、DeepRank [63] Core ParadigmsPLM & LLM Era(Sec 4) The Holistic Paradigm(Sec 4.1) Naive Truncation：DPR [43]、ANCE [88] 长序列 Transformers：Longformer [8]、BigBird [92]、Reformer [45]、FlashAttention [22]、LongNet [25]、 LONGEMBED [97]、M3-Embedding [14]、QDS-Transformer [40]、Socialformer [95] LLM 作为重新排序器：RankGPT [77]、RepLLaMA/RankLLaMA [58] 效率缓解：LongLoRA [15]、L

### 段落 31 · Page 5

**EN**

ongLLMLingua [39], DuoAttention [87] The Divide-and-ConquerParadigm (Sec 4.2) Pooling-based Heuristics: BERT-MaxP/SumP [21] Hierarchical Aggregation: PARADE [48], DRSCM [82], LTR-BERT [81], MORES+ [29] Key Block Selection: IDCM [35], KeyB [52], KeyB2 [50], BReps [51], DCS [71] Hybrid & Late Interaction: ICLI [49], Match-Ignition [61], Longtriever [89]Indexing-Structure-Oriented Paradigm(Sec 4.3) MC-indexing [27], HELD [12], RAPTOR [68] Long-Query Retrieval(Sec 4.4) RPRS [4] Evaluation(Sec 5) Datasets and Benchmarks(Sec 5.1) TREC Robust04 [80], Gov2/Terabyte Track [10], ClueWeb12 [47], TREC Deep Learning [18], MS MARCO [5],MLDR [14], LONGEMBED

**中文**

ongLLMLingua [39]、DuoAttention [87] 分而治之的范式（第 4.2 节） 基于池的启发式：BERT-MaxP/SumP [21] 分层聚合：PARADE [48]、DRSCM [82]、LTR-BERT [81]、MORES+ [29] 关键块选择：IDCM [35]、KeyB [52]、KeyB2 [50]、BReps [51]、DCS [71] 混合和后期交互：ICLI [49]、Match-Ignition [61]、Longtriever [89]索引结构导向范式（第 4.3 节） MC 索引 [27]、HELD [12]、RAPTOR [68] 长查询检索（第 4.4 节） RPRS [4] 评估（第 5 节）数据集和基准（第 5.1 节） TREC Robust04 [80]、Gov2/Terabyte Track [10]、ClueWeb12 [47]、TREC 深度学习 [18]、MS MARCO [5]、MLDR [14]、LONGEMBED

### 段落 32 · Page 5

**EN**

[97], Multi-CPR (Chinese) [56] Standard Metrics(Sec 5.2) nDCG@k, MAP, Recall@k, Precision@k, MRR,ERR Applications(Sec 6) Legal Retrieval(Sec 6.1) Lawformer [86], LegalBERT [13], LawGPT [96], ChatLaw [19], DISC-LawLLM [90] Scholarly Paper Retrieval(Sec 6.2) SciBERT [6], SPECTER [17], SciNCL [60], PRISM [65], CORANK [79], PaperQA [57], SemRank [94],DocReLM [83], LLM-KnowSimFuser [20], PaSa [34], SPAR [73] Biomedical Retrieval(Sec 6.3) PubMedBERT [30], Clinical-Longformer, Clinical-BigBird [54], BioClinical ModernBERT [74] Cross-Lingual Retrieval(Sec 6.4) mBERT [24], LaBSE [28], XLM-R, McCrolin [55], mGTE [93], CROSS [59] Fig.

**中文**

[97]、Multi-CPR（中文）[56] 标准指标（第 5.2 节） nDCG@k、MAP、Recall@k、Precision@k、MRR、ERR 应用（第 6 节） 法律检索（第 6.1 节） Lawformer [86]、LegalBERT [13]、LawGPT [96]、ChatLaw [19]、DISC-LawLLM [90] 学术论文检索（第 6.2 节） SciBERT [6]、SPECTRE [17]、SciNCL [60]、PRISM [65]、CORANK [79]、PaperQA [57]、SemRank [94]、DocReLM [83]、LLM-KnowSimFuser [20]、PaSa [34]、SPAR [73] 生物医学检索（第 6.3 节） PubMedBERT [30]、Clinical-Longformer、Clinical-BigBird [54]、BioClinical ModernBERT [74] 跨语言检索（第 6.4 节） mBERT [24]、LaBSE [28]、XLM-R、Mccrolin [55]、mGTE [93]、CROSS [59]

### 段落 33 · Page 5

**EN**

2. A structured taxonomy of Long-Document Retrieval, categorizing existing research across eras, core paradigms, applications, and evaluation methods. dimension: Long documents usually have a clear hierarchical structure, such as chapters, paragraphs, titles, tables, and appendices, and the information distribution has obvious heterogeneity; (3) Semantic dimension: Long documents often contain multiple topics or multiple arguments, and there are problems of topic drift and long semantic span.

**中文**

2. 长文献检索的结构化分类法，对现有研究进行跨时代、核心范式、应用和评估方法的分类。维度：长文档通常具有清晰的层次结构，如章节、段落、标题、表格、附录等，信息分布具有明显的异质性； (3)语义维度：长文档往往包含多个主题或多个论点，存在主题漂移和语义跨度长的问题。

### 段落 34 · Page 5

**EN**

Therefore, LDR not only faces the problem of information extraction, but also needs to pay attention to document structure perception and semantic focus capabilities.

**中文**

因此，LDR不仅面临信息抽取问题，还需要关注文档结构感知和语义聚焦能力。

### 段落 35 · Page 5

**EN**

According to different retrieval objectives and downstream task requirements, long-document retrieval can be divided into the following task forms: (1) Document-level retrieval: using the entire document as the retrieval unit, returning the most relevant documents from the long document collection; (2) Passage/Section retrieval: using paragraphs, chapters or fragments generated by sliding windows as units, retrieving content fragments that are strongly relevant to the query; (3) Evidence retrieval: extracting fragments from documents that serve as the basis for answers for tasks such as question answering and reasoning, often used in multi-ho

**中文**

根据不同的检索目标和下游任务需求，长文档检索可以分为以下几种任务形式：（1）文档级检索：以整个文档为检索单元，从长文档集合中返回最相关的文档； （2）Passage/Section检索：以滑动窗口生成的段落、章节或片段为单位，检索与查询强相关的内容片段； (3) 证据检索：从文档中提取片段，作为问答、推理等任务答案的基础，常用于多人协作

### 段落 36 · Page 5

**EN**

p question answering or RAG systems; (4) Structure-aware retrieval: using the logical structure of the document for retrieval, such as title/paragraph tag/citation network, to improve semantic positioning accuracy; (5) Cross-document retrieval: supporting the aggregation and cross-comparison of relevant information in multiple long documents, targeting complex reasoning and content synthesis.

**中文**

p 问答系统或 RAG 系统； （4）结构感知检索：利用文档的逻辑结构进行检索，如标题/段落标签/引文网络，提高语义定位精度； （5）跨文档检索：支持多个长文档中相关信息的聚合和交叉比较，针对复杂的推理和内容合成。

### 段落 37 · Page 5

**EN**

Furthermore, LDR often intersects and integrates with other retrieval tasks, such as open-domain question answering, document reranking, summary generation, and retrieval-augmented generation (RAG), forming a complex information processing pipeline. Therefore, accurately defining the boundaries and forms of LDR is fundamental for subsequent modeling, evaluation, and method design.

**中文**

此外，LDR经常与其他检索任务交叉和集成，例如开放域问答、文档重排序、摘要生成和检索增强生成（RAG），形成复杂的信息处理管道。因此，准确界定LDR的边界和形式是后续建模、评估和方法设计的基础。

### Page 6

### 段落 38 · Page 6

**EN**

6 Li et al. 2.1 Core Challenges 2.1.1 Sparse and Inconsistent Supervision Signals.In the majority of public benchmarks, relevance annotations for lengthy documents are typically concentrated at the document or paragraph level, while actual queries frequently involve only small fragments within the document. As a result of this discrepancy, the model’s discriminative power is diminished, and fine-grained alignment becomes more difficult.

**中文**

6 李等人。 2.1 核心挑战 2.1.1 监督信号稀疏且不一致。在大多数公共基准测试中，长文档的相关性注释通常集中在文档或段落级别，而实际查询往往只涉及文档中的小片段。由于这种差异，模型的判别能力被削弱，细粒度的对齐变得更加困难。

### 段落 39 · Page 6

**EN**

For instance, the Natural Questions dataset introduced by Kwiatkowski[46] provides paragraph-level long answers and brief answer annotations for each question, which somewhat parallel the query-local fragment correspondence. Nevertheless, this annotation type continues to fall short of addressing the fine-grained supervisory requirements at the sentence or even evidence chain level. Conversely, sparse relevance judgements are typically implemented by mainstream training and evaluation resources in the retrieval domain, including MS MARCO and TREC Deep Learning.

**中文**

例如，Kwiatkowski[46]引入的自然问题数据集为每个问题提供了段落级的长答案和简短的答案注释，这在某种程度上与查询本地片段对应关系相似。然而，这种注释类型仍然无法满足句子甚至证据链级别的细粒度监督要求。相反，稀疏相关性判断通常由检索领域的主流训练和评估资源来实现，包括 MS MARCO 和 TREC Deep Learning。

### 段落 40 · Page 6

**EN**

The official MS MARCO leaderboard is based on pre-collected sparse judgements, as explicitly stated by Craswell[18] in their TREC 2022 review. Additionally, the sparse character of MS MARCO labels is underscored in the TREC DL overview. Arabzadeh[ 2] conducted an analysis of this sparse supervision method, observing that it may result in external validity issues in evaluations by obstructing the learning of more detailed matching patterns by models. 2.1.2 Document Segmentation and Chunking.To facilitate indexing and retrieval, it is frequently necessary to divide lengthy documents into smaller blocks, such as paragraphs or chunks.

**中文**

正如 Craswell[18] 在其 TREC 2022 评论中明确指出的那样，官方 MS MARCO 排行榜基于预先收集的稀疏判断。此外，TREC DL 概述中强调了 MS MARCO 标签的稀疏特征。 Abuzadeh[2]对这种稀疏监督方法进行了分析，观察到它可能会阻碍模型学习更详细的匹配模式，从而导致评估中的外部有效性问题。 2.1.2 文档分段和分块。为了便于索引和检索，经常需要将冗长的文档分成较小的块，例如段落或块。

### 段落 41 · Page 6

**EN**

A long-standing challenge is determining the optimal segmentation without sacrificing semantic context. As a result of mechanical segmentation, traditional fixed-length chunking frequently disrupts sentence logic or conceptual units, resulting in "semantic fragmentation" during retrieval. Through multi-dataset analysis, Bhat[9] systematically evaluated the influence of fixed-length chunking strategies on retrieval performance. They discovered that smaller chunks are more effective in short-answer scenarios, as they are able to accurately identify individual factual information.

**中文**

一个长期存在的挑战是在不牺牲语义上下文的情况下确定最佳分割。由于机械分段，传统的固定长度分块经常破坏句子逻辑或概念单元，导致检索过程中的“语义碎片”。 Bhat[9]通过多数据集分析，系统评估了固定长度分块策略对检索性能的影响。他们发现，较小的数据块在简答题场景中更有效，因为它们能够准确识别单个事实信息。

### 段落 42 · Page 6

**EN**

Conversely, larger chunks are more advantageous for tasks that necessitate a broader contextual understanding, such as thematic summarisation of long documents and novel plot analysis. Different embedding models exhibit varying sensitivities to block size, which they emphasise. For example, lightweight embedding models are more efficient when using smaller chunks, whereas large parameter models necessitate larger chunks to completely capture deep semantic information. This renders the selection of a segmentation strategy a complex yet essential step in the pursuit of a balance between semantic integrity and retrieval efficiency.

**中文**

相反，较大的块对于需要更广泛的上下文理解的任务更有利，例如长文档的主题总结和新颖的情节分析。不同的嵌入模型对块大小表现出不同的敏感性，这是他们所强调的。例如，轻量级嵌入模型在使用较小的块时效率更高，而大参数模型则需要较大的块才能完全捕获深层语义信息。这使得分割策略的选择成为追求语义完整性和检索效率之间平衡的复杂但重要的步骤。

### 段落 43 · Page 6

**EN**

2.1.3 Computational and Efficiency Issues.The computational and storage overhead are substantially increased when long texts are processed. The retrieval throughput and latency are influenced by the larger index sizes and the increased number of word vectors or embeddings that must be computed when the documents are longer. This problem is especially evident in deep learning-based retrieval, particularly in Transformer-based re-ranking models. The computational complexity of the self-attention mechanism increases quadratically with the length of the input, rendering it nearly impossible to process ultra-long sequences in a single pass.

**中文**

2.1.3 计算和效率问题。处理长文本时，计算和存储开销大大增加。检索吞吐量和延迟受到较大索引大小以及文档较长时必须计算的词向量或嵌入数量增加的影响。这个问题在基于深度学习的检索中尤其明显，特别是在基于 Transformer 的重排序模型中。自注意力机制的计算复杂度随着输入的长度呈二次方增加，使得单次处理超长序列几乎不可能。

### 段落 44 · Page 6

**EN**

Researchers have suggested a variety of enhancements in various directions to resolve this bottleneck. On the one hand, BigBird [92] and Longformer [8] employ sparse attention mechanisms to effectively enhance the model’s capacity to manage lengthy sequences, thereby reducing computational complexity at the structural level. In contrast, Seo[ 69] proposed Colour (Compression for Long Context Retrieval), an input-level approach that reduces input size by compressing paragraphs and retaining core information, thereby avoiding redundant computations caused by irrelevant content.

**中文**

研究人员提出了各种不同方向的增强措施来解决这一瓶颈。一方面，BigBird [92]和Longformer [8]采用稀疏注意力机制来有效增强模型管理长序列的能力，从而降低结构层面的计算复杂度。相比之下，Seo[69]提出了Color（用于长上下文检索的压缩），这是一种输入级方法，通过压缩段落并保留核心信息来减少输入大小，从而避免由不相关内容引起的冗余计算。

### 段落 45 · Page 6

**EN**

The former enhances scalability by optimising the model structure, whereas the latter achieves cost reduction and efficiency gains through content compression.

**中文**

前者通过优化模型结构增强可扩展性，后者通过内容压缩实现降本增效。

### Page 7

### 段落 46 · Page 7

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 7 3 Pre-PLM Era Before the advent of pre-trained Transformers, LDR relied on lexical statistics and early neural architectures. While these methods laid essential foundations, their scalability to book- or report-length inputs is limited by (i) sensitivity to topic drift and dispersed evidence, (ii) computational growth with document length, and (iii) loss of global discourse when truncation or coarse windowing is used. We summarize representative approaches and highlight how these models’ limitations motivate PLM/LLM-era designs.

**中文**

PLM 和 LLM 时代的长文档检索综述 7 3 Pre-PLM 时代 在预训练 Transformer 出现之前，LDR 依赖于词汇统计和早期神经架构。虽然这些方法奠定了必要的基础，但它们对书籍或报告长度输入的可扩展性受到以下因素的限制：(i) 对主题漂移和分散证据的敏感性，(ii) 计算量随文档长度的增长，以及 (iii) 使用截断或粗窗口时全局话语的损失。我们总结了代表性方法，并强调了这些模型的局限性如何激发 PLM/LLM 时代的设计。

### 段落 47 · Page 7

**EN**

3.1 Lexical Methods: TF–IDF, BM25, and Heuristic Structure Classic vector-space retrieval [42] weights terms by within-document frequency (TF) and across-corpus rarity (IDF): 𝑇 𝐹𝑖,𝑗 = 𝑛𝑖,𝑗Í 𝑘 𝑛𝑘,𝑗 , 𝐼 𝐷𝐹 𝑖 =log |𝐷| 1+ |{𝑗:𝑡 𝑖 ∈𝑑 𝑗 }| ,TF-IDF=𝑇 𝐹×𝐼 𝐷𝐹 .(1) Where 𝑛𝑖,𝑗 is the count of term 𝑡𝑖 in document 𝑑 𝑗 ; Í 𝑘 𝑛𝑘,𝑗 is the total number of terms in 𝑑 𝑗 ; 𝑇 𝐹𝑖,𝑗 (term frequency of 𝑡𝑖 in 𝑑 𝑗 ) equals 𝑛𝑖,𝑗 divided by Í 𝑘 𝑛𝑘,𝑗 ; |𝐷| is the total number of documents in the corpus; |{𝑗 : 𝑡𝑖 ∈𝑑 𝑗 }| is the number of documents containing 𝑡𝑖 (the "+1" in IDF’s denominator avoids division by zero);𝐼 𝐷𝐹𝑖 measures 𝑡𝑖’s rarity across the corpus; andTF-IDFis the product of𝑇 𝐹 𝑖,𝑗 and𝐼 𝐷𝐹 𝑖, quantifying𝑡 𝑖’s importance in𝑑𝑗 relative to the corpus.

**中文**

3.1 词汇方法：TF–IDF、BM25 和启发式结构 经典向量空间检索 [42] 通过文档内频率 (TF) 和跨语料库稀有度 (IDF) 对术语进行加权： 𝑇 𝐹𝑖,𝑗 = 𝑛𝑖,𝑗Í 𝑘 𝑛𝑘,𝑗 , 𝐼 𝐷𝐹 𝑖 =log |𝐷| 1+ |{𝑗:𝑡 𝑖 ε𝑑 𝑗 }| ,TF-IDF=𝑇 𝐹×𝐼 𝐷𝐹。(1) 其中 𝑛𝑖,𝑗 是文档 𝑑 𝑗 中术语 𝑡𝑖 的计数； Í 𝑘 𝑛𝑘,𝑗 是 𝑑 𝑗 中的项总数； 𝑇 𝐹𝑖,𝑗 （𝑑 𝑗 中𝑡𝑖 的词频）等于 𝑛𝑖,𝑗 除以 Í 𝑘 𝑛𝑘,𝑗； |𝐷|是语料库中的文档总数； |{𝑗 : 𝑡𝑖 ε𝑑 𝑗 }|是包含 𝑡𝑖 的文档数量（IDF 分母中的“+1”避免被零除）；𝐼 𝐷𝐹𝑖 衡量𝑡𝑖 在整个语料库中的稀有性；而TF-ID是𝑇𝐹𝑖、𝑗和𝐼𝐷𝐹𝑖的乘积，量化了𝑡𝑖在𝑑𝑗中相对于语料库的重要性。

### 段落 48 · Page 7

**EN**

TF–IDF scales well and is interpretable, but ignores synonymy/polysemy and long-range semantics; in long documents, frequent background terms can dominate, and topic drift obscures sparse, query-relevant evidence.

**中文**

TF-IDF 具有良好的扩展性和可解释性，但忽略了同义/一词多义和远程语义；在长文档中，频繁的背景术语可能占主导地位，而主题漂移会掩盖稀疏的、与查询相关的证据。

### 段落 49 · Page 7

**EN**

Okapi BM25 [67] refines lexical matching with saturation and length normalization: score(𝑑, 𝑄)= ∑︁ 𝑞∈𝑄 IDF(𝑞) · TF(𝑞, 𝑑) · (𝑘 1 +1) TF(𝑞, 𝑑) +𝑘 1 · 1−𝑏+𝑏· |𝑑| avgdl  .(2) Where score(𝑑, 𝑄) is the relevance score between document𝑑 and query 𝑄; 𝑑 is the document evaluated;𝑄 represents the user’s query;𝑞 is an individual term in 𝑄; TF(𝑞, 𝑑) is 𝑞’s frequency in𝑑; 𝑘1 controls term frequency saturation; 𝑏 normalizes document length effects; |𝑑| is 𝑑’s term count;avgdl is the corpus average document length; and the score sums weighted contributions of each 𝑞, integrating IDF(𝑞) (as in TF-IDF) and normalized term frequency adjusted by 𝑘1 and𝑏.

**中文**

Okapi BM25 [67] 通过饱和度和长度归一化来细化词汇匹配：score(𝑑, 𝑄)= Σ︁ 𝑞ε𝑄 IDF(𝑞) · TF(𝑞, 𝑑) · (𝑘 1 +1) TF(𝑞, 𝑑) +𝑘 1 · 1−𝑏+𝑏·|𝑑| avgdl .(2) 其中score(𝑑, 𝑄)是文档𝑑和查询𝑄之间的相关性得分； 𝑑 是评估的文档；𝑄 代表用户的查询；𝑞 是𝑄 中的单个术语； TF(𝑞, 𝑑) 是𝑞在𝑑中的频率； 𝑘1 控制词频饱和度； 𝑏 标准化文档长度影响； |𝑑|是𝑑的术语数；avgdl是语料库平均文档长度；得分对每个 𝑞 的加权贡献进行求和，整合 IDF(𝑞)（如 TF-IDF）以及由 𝑘1 和 𝑏 调整的归一化术语频率。

### 段落 50 · Page 7

**EN**

BM25 remains a strong, unsupervised baseline even for long documents due to robustness and efficiency [84]. Yet it is still lexical: dispersed, semantically related evidence without exact term overlap is easily missed. Heuristic chunking and structure-aware weighting. To mitigate dispersion, classical systems adopt paragraph/passage indexing and structure-aware priors. Callan’s segmented indexing [11] scores overlapping windows and then aggregates at the document level, reducing the chance that relevant text is split across boundaries. Structured metadata weighting [1] emphasizes salient sections (e.g., abstract, conclusions, legal clauses).

**中文**

由于稳健性和效率，即使对于长文档，BM25 仍然是一个强大的、无监督的基线 [84]。然而它仍然是词汇上的：分散的、语义相关的证据，没有确切的术语重叠，很容易被错过。启发式分块和结构感知加权。为了减轻分散性，经典系统采用段落/段落索引和结构感知先验。 Callan 的分段索引 [11] 对重叠窗口进行评分，然后在文档级别进行聚合，从而减少相关文本跨边界分割的机会。结构化元数据加权 [1] 强调显着部分（例如摘要、结论、法律条款）。

### 段落 51 · Page 7

**EN**

These heuristics help, but their fixed granularity and rule dependence struggle with heterogeneous long documents and cross-section reasoning. Why lexical methods struggle with long documents. (1)Signal dilution: relevance spans few sentences amid thousands of tokens; global bag-of-words mixing drowns weak signals. (2)Topic drift: multi-topic, long narratives produce misleading TF/IDF statistics. (3)Structure unawareness: discourse, section hierarchy, and cross-references are not modeled, limiting holistic understanding.

**中文**

这些启发式方法有所帮助，但它们的固定粒度和规则依赖与异构长文档和横截面推理相矛盾。为什么词法方法难以处理长文档。 (1)信号稀释：相关性跨越数千个标记中的几个句子；全球词袋混合淹没了微弱的信号。 (2)主题漂移：多主题、长叙述会产生误导性的 TF/IDF 统计数据。 (3)结构无意识：话语、章节层次结构和交叉引用没有建模，限制了整体理解。

### Page 8

### 段落 52 · Page 8

**EN**

8 Li et al. 3.2 Early Neural IR: Representation vs. Interaction Models Neural IR prior to Transformers pursued two lines: (i) representation-based models map queries/documents to vectors and compare them; (ii) interaction-based models compute fine-grained similarity matrices and learn matching patterns. Both improved beyond lexical matching, yet long-document scalability remained a core obstacle. DSSM (representation-based) [36] projects queries and documents into a shared semantic space (cosine similarity), with letter-𝑛gram hashing for vocabulary compression.

**中文**

8 李等人。 3.2 早期神经 IR：表示与交互模型 Transformers 之前的神经 IR 追求两条路线：（i）基于表示的模型将查询/文档映射到向量并进行比较；（i）基于表示的模型将查询/文档映射到向量并进行比较； (ii) 基于交互的模型计算细粒度相似性矩阵并学习匹配模式。两者都超越了词汇匹配，但长文档的可扩展性仍然是一个核心障碍。 DSSM（基于表示）[36]将查询和文档投影到共享语义空间（余弦相似性）中，并使用字母𝑛gram哈希进行词汇压缩。

### 段落 53 · Page 8

**EN**

While effective on web search logs, single-vector representations suffer semantic dilution on long, multi-topic documents, and lack explicit modeling of dispersed evidence. DRMM (interaction-based) [31] builds histogram features of query-term×document-term similarities and aggregates with a term-gating network (e.g., IDF). Its focus on exact/strong matches suits ad-hoc retrieval, including longer pages; however, the implicit interaction matrix scales with 𝑂(|𝑞| · |𝑑|) , making very long inputs costly without aggressive candidate pruning.

**中文**

虽然单向量表示对网络搜索日志有效，但在长的多主题文档上会受到语义稀释，并且缺乏对分散证据的明确建模。 DRMM（基于交互）[31]构建查询术语×文档术语相似性的直方图特征，并与术语门控网络（例如IDF）进行聚合。它专注于精确/强匹配，适合临时检索，包括较长的页面；然而，隐式交互矩阵随 𝑂(|𝑞| · |𝑑|) 缩放，如果没有积极的候选剪枝，那么很长的输入会变得昂贵。

### 段落 54 · Page 8

**EN**

Treating matching as image recognition, MatchPyramid (interaction-based) [62] applies CNNs over the query–document similarity matrix with dynamic pooling to handle variable length. For long documents, the |𝑞| × |𝑑| map becomes large; dynamic pooling may discard subtle, far-apart evidence, and the model lacks explicit hierarchical aggregation. PACRR (interaction-based) [37] convolves over the similarity matrix with 𝑛-gram kernels and uses 𝑘-max pooling per query term, followed by an LSTM combiner.

**中文**

将匹配视为图像识别，MatchPyramid（基于交互）[62] 将 CNN 应用于查询-文档相似度矩阵，并使用动态池来处理可变长度。对于长文档，|𝑞| × |𝑑|地图变大；动态池可能会丢弃微妙的、相距遥远的证据，并且该模型缺乏明确的层次聚合。 PACRR（基于交互）[37] 使用 𝑛-gram 内核对相似性矩阵进行卷积，并针对每个查询项使用 𝑘-max 池化，然后是 LSTM 组合器。

### 段落 55 · Page 8

**EN**

To keep computation tractable, inputs are truncated or selected via firstk/kwindow, which reintroduces positional bias and risks missing late-occurring evidence in long documents. DeepRank (query-centric contexts) [63] detects query-term occurrences and extracts local windows for focused matching, then aggregates across positions with positional decay and term importance. This avoids building a full similarity matrix and is robust to noisy long pages. Its main limitation is reliance on lexical overlap and fixed windows, which can miss semantically relevant, cross-sentence evidence spanning larger discourse units.

**中文**

为了保持计算的易处理性，输入被截断或通过 firstk/kwindow 选择，这会重新引入位置偏差，并有可能丢失长文档中迟到的证据。 DeepRank（以查询为中心的上下文）[63] 检测查询术语的出现并提取局部窗口以进行重点匹配，然后根据位置衰减和术语重要性跨位置进行聚合。这避免了构建完整的相似性矩阵，并且对于嘈杂的长页面具有鲁棒性。它的主要局限性是依赖词汇重叠和固定窗口，这可能会错过跨越较大话语单元的语义相关的跨句子证据。

### 段落 56 · Page 8

**EN**

Why early neural models struggle with long documents. (1)Quadratic or linear-in-length interaction cost: similarity maps and late-interaction pipelines scale with |𝑑| , straining memory/latency on thousands of tokens. (2)Truncation/windowing side-effects: necessary length control breaks discourse and induces head/tail bias; critical evidence after cutoffs is lost. (3)Insufficient global structure: CNN/RNN over local patterns lacks explicit modeling of document hierarchy, cross-section dependencies, and global coherence demanded by long-form inputs.

**中文**

为什么早期的神经模型难以处理长文档。 (1) 二次或​​线性长度交互成本：相似性图和后期交互管道随 |𝑑| 缩放，使数千个令牌的内存/延迟变得紧张。 (2)截断/窗口副作用：必要的长度控制会破坏话语并引起头/尾偏差；截止后的关键证据丢失。 (3)全局结构不足：局部模式上的 CNN/RNN 缺乏对文档层次结构、横截面依赖性和长格式输入所需的全局一致性的明确建模。

### 段落 57 · Page 8

**EN**

Lexical and early neural methods introduced efficient baselines and fine-grained matching, but their assumptions (bag-of-words, fixed windows, global single vectors, or full similarity matrices) misalign with the length, structure, and dispersed evidence of long documents. These limitations directly motivate PLM-era strategies: efficient/sparse long-context attention, divide-and-conquer aggregation, and select-then-process cascades, as well as the LLM-era use of holistic rerankers with long-context optimizations.

**中文**

词汇和早期神经方法引入了有效的基线和细粒度匹配，但它们的假设（词袋、固定窗口、全局单向量或完全相似性矩阵）与长文档的长度、结构和分散证据不一致。这些限制直接激发了 PLM 时代的策略：高效/稀疏的长上下文注意力、分而治之聚合和选择然后处理级联，以及 LLM 时代使用具有长上下文优化的整体重排序器。

### 段落 58 · Page 8

**EN**

4 PLM and LLM Era Models for Long-Document Retrieval The advent of Pre-trained Language Models and Large Language Models has marked a paradigm shift in the field of long-document retrieval. To address the challenges posed by extensive contexts, researchers have moved beyond traditional bag-of-words models and shallow neural networks, developing a range of more powerful and sophisticated modeling strategies. To systematically organize these cutting-edge approaches, this chapter categorizes them into several core paradigms, whose architectural overviews are illustrated inFig.

**中文**

4 长文档检索的 PLM 和 LLM 时代模型 预训练语言模型和大型语言模型的出现标志着长文档检索领域的范式转变。为了解决广泛上下文带来的挑战，研究人员超越了传统的词袋模型和浅层神经网络，开发了一系列更强大、更复杂的建模策略。为了系统地组织这些前沿方法，本章将它们分为几个核心范式，其架构概述如图 1 所示。

### 段落 59 · Page 8

**EN**

3: (1)the Holistic Paradigm(detailed in Section 4.1), which aims to model and interact with the entire document as a single, indivisible unit; (2)the Divide-and-Conquer

**中文**

3：（1）整体范式（详见 4.1 节），旨在将整个文档作为一个不可分割的单元进行建模和交互； (2)分而治之

### Page 9

### 段落 60 · Page 9

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 9 Paradigm(detailed in Section 4.2), which segments long documents into smaller pieces for localized processing before aggregating global information; (3)Long-Query Retrieval(detailed in Section 4.4), which tackles scenarios where queries themselves are long documents (e.g., legal case retrieval, patent prior-art search).

**中文**

PLM 和 LLM Era 9 Paradigm 中的长文档检索综述（详见第 4.2 节），该范式将长文档分割成较小的片段，以便在聚合全局信息之前进行本地化处理； (3)长查询检索（详见4.4节），它解决查询本身是长文档的场景（例如，法律案例检索、专利现有技术检索）。

### 段落 61 · Page 9

**EN**

Additionally, we discuss theIndexing-Structure-Oriented Paradigmin Section 4.3, this paradigm focuses on innovating how documents are chunked and indexed (note: its workflows are highly diverse and difficult to consolidate into a single generalized diagram, so it is elaborated separately). Each subgraph visually summarizes the core workflow of its corresponding paradigm, providing intuition before we delve into technical details. The following sections will delve into the representative models and technical evolution within each of these paradigms. Fig. 3. An overview of the long-document retrieval paradigm in the PLM and LLM era.

**中文**

此外，我们在第 4.3 节讨论了面向索引结构的范式，该范式侧重于创新文档分块和索引的方式（注意：其工作流程高度多样化，难以合并到单个广义图表中，因此单独阐述）。每个子图直观地总结了其相应范例的核心工作流程，在我们深入研究技术细节之前提供直觉。以下部分将深入研究每个范例中的代表性模型和技术演变。图 3. PLM 和 LLM 时代长文档检索范例的概述。

### 段落 62 · Page 9

**EN**

Methods evolve from (1) The Holistic Paradigm in the PLM & LLM Era to (2) Divide-and-conquer Paradigm for Long Documents and (3) Long-Query Retrieval, reflecting the field’s progression in balancing effectiveness, efficiency, and scalability. 4.1 The Holistic Paradigm in the PLM & LLM Era The holistic paradigm aims to model the entire document or interact with the global context of the query-document pair, thereby avoiding the segmentation and pooling biases of traditional methods. The advantage of this approach lies in its ability to preserve the global semantics and structure of the document.

**中文**

方法从 (1) PLM 和 LLM 时代的整体范式发展到 (2) 长文档的分而治之范式和 (3) 长查询检索，反映了该领域在平衡有效性、效率和可扩展性方面的进展。 4.1 PLM 和 LLM 时代的整体范式 整体范式旨在对整个文档进行建模或与查询-文档对的全局上下文进行交互，从而避免传统方法的分段和池化偏差。这种方法的优点在于它能够保留文档的全局语义和结构。

### 段落 63 · Page 9

**EN**

However, it faces significant challenges in terms of computational cost and architecture, particularly when dealing with ultra-long documents. Despite these challenges, it performs well in tasks involving short or smaller-scale documents. The next section will explore the "Divide-and-Conquer Paradigm, " which addresses the computational efficiency issues of the holistic paradigm by processing documents in smaller chunks, while also achieving significant results in long-document retrieval.

**中文**

然而，它在计算成本和架构方面面临着巨大的挑战，特别是在处理超长文档时。尽管存在这些挑战，它在涉及简短或较小规模文档的任务中表现良好。下一节将探讨“分而治之的范式”，它通过处理较小块的文档来解决整体范式的计算效率问题，同时在长文档检索中也取得了显着的结果。

### Page 10

### 段落 64 · Page 10

**EN**

10 Li et al. 4.1.1 Naive Truncation Baselines.Early dense retrieval models such as DPR [ 43] and ANCE [ 88] highlighted the potential of pre-trained language models to surpass lexical retrieval by leveraging contrastive learning. However, they are constrained by BERT’s 512-token limit, and thus apply a naive truncation strategy: retaining only the first 512 tokens of a long document, based on the common assumption that important summary information resides at the beginning.

**中文**

10 李等人。 4.1.1 朴素截断基线。早期的密集检索模型，如 DPR [ 43] 和 ANCE [ 88] 强调了预训练语言模型通过利用对比学习超越词汇检索的潜力。然而，它们受到 BERT 512 个 token 限制的限制，因此应用了一种朴素的截断策略：基于重要摘要信息位于开头的常见假设，仅保留长文档的前 512 个 token。

### 段落 65 · Page 10

**EN**

This design introduces three critical flaws: (i) information loss, as relevant evidence beyond the cutoff is discarded; (ii) destruction of discourse structure, since long-range dependencies are severed; and (iii) positional bias, as the beginning of a document is always over-emphasized. Consequently, While DPR and ANCE pioneered dense retrieval, their truncation assumptions clearly fail in the context of long document IR. Truncation not only results in systematic information loss but also severely impairs the model’s ability to model discourse-level relevance.

**中文**

这种设计引入了三个关键缺陷：（i）信息丢失，因为超出截止范围的相关证据被丢弃； (ii) 话语结构被破坏，因为远程依赖性被切断； (iii) 位置偏见，因为文件的开头总是被过分强调。因此，虽然 DPR 和 ANCE 开创了密集检索的先河，但他们的截断假设显然在长文档 IR 的背景下失败了。截断不仅会导致系统性信息丢失，还会严重损害模型对话语级相关性进行建模的能力。

### 段落 66 · Page 10

**EN**

Furthermore, the performance ceiling of this approach is very low, making it difficult to serve as an effective baseline for long-document retrieval. 4.1.2 Long-Sequence Transformer Architectures.A major research thrust has therefore been to extend Transformer architectures to efficiently handle long sequences.Longformer[ 8] introduced a hybrid attention mechanism: a sliding window for local context (𝑂(𝑛×𝑤)complexity) combined with global attention tokens to capture long-range dependencies.

**中文**

此外，这种方法的性能上限很低，很难作为长文档检索的有效基线。 4.1.2 长序列 Transformer 架构。因此，一个主要的研究重点是扩展 Transformer 架构以有效地处理长序列。Longformer[8]引入了一种混合注意力机制：局部上下文的滑动窗口（𝑂（𝑛×𝑤）复杂性）与全局注意力标记相结合以捕获远程依赖性。

### 段落 67 · Page 10

**EN**

It established a foundation for models such asBigBird[ 91], which used blockwise sparse attention and random connections to achieve linear scaling, and demonstrated state-of-the-art performance on long-document QA and summarization. Sparse attention models, such as Longformer and BigBird, significantly expand the context they can handle. However, their scalability to millions of documents remains questionable, especially in real-world retrieval scenarios, where models must simultaneously process multi-document interactions, not just the long context within a single document.

**中文**

它为 BigBird[91] 等模型奠定了基础，该模型使用块式稀疏注意力和随机连接来实现线性缩放，并在长文档 QA 和摘要方面展示了最先进的性能。 Longformer 和 BigBird 等稀疏注意力模型显着扩展了它们可以处理的上下文。然而，它们对数百万文档的可扩展性仍然存在问题，特别是在现实世界的检索场景中，模型必须同时处理多文档交互，而不仅仅是单个文档中的长上下文。

### 段落 68 · Page 10

**EN**

Furthermore, cross-paragraph and cross-section evidence aggregation remains fragile, and sparse connectivity patterns can miss key matches, leading to low recall.Reformer[ 45] replaced quadratic attention with locality-sensitive hashing, whileFlashAttention[ 22] restructured attention into an IO-aware exact algorithm, reducing memory latency and enabling efficient > 16k context. More recently,LongNet[ 25] scales to billion-token inputs using dilated attention without catastrophic forgetting of shorter contexts. Zhu et al.

**中文**

此外，跨段落和跨部分的证据聚合仍然脆弱，稀疏的连接模式可能会错过关键匹配，从而导致召回率较低。Reformer[45]用局部敏感哈希替换了二次注意力，而FlashAttention[22]将注意力重构为IO感知的精确算法，减少了内存延迟并实现了高效的> 16k上下文。最近，LongNet[25]使用扩展注意力扩展到十亿个令牌输入，而不会灾难性地忘记较短的上下文。朱等人。

### 段落 69 · Page 10

**EN**

introducedLONGEMBED[ 97], a benchmark for long-context retrieval, alongside methods to extend context length in embedding models. They proposed both training-free and training-based strategies for Absolute Position Encoding (APE) models, enabling context expansion from 512 to 4k through position embedding reuse, interpolation, or fine-tuning. For Rotary Position Encoding (RoPE) models, they leveraged relative position encoding via self-extrapolation and NTK-aware interpolation to extend E5-Mistral’s context to 32k without compromising short-context performance. Beyond efficiency-driven architectures, IR-specific adaptations emerged.

**中文**

引入了 LONGEMBED[97]，这是长上下文检索的基准，以及在嵌入模型中扩展上下文长度的方法。他们为绝对位置编码 (APE) 模型提出了免训练和基于训练的策略，通过位置嵌入重用、插值或微调，实现从 512 到 4k 的上下文扩展。对于旋转位置编码 (RoPE) 模型，他们通过自外推和 NTK 感知插值利用相对位置编码，将 E5-Mistral 的上下文扩展到 32k，而不影响短上下文性能。除了效率驱动的架构之外，还出现了针对 IR 的适应方案。

### 段落 70 · Page 10

**EN**

TheQDS-Transformer[ 40] integrates IR axioms (locality, hierarchy, query matching) into a structured sparse attention pattern: 𝐴QDS =𝐴 local ∪𝐴 sent ∪𝐴 query ∪𝐴 [CLS] , where 𝐴local enforces windowed interactions, 𝐴sent links tokens to sentence-level [SOS] markers, and 𝐴query globally connects document words to query tokens. On TREC DL’19, QDS-Transformer achieved improvements over strong baselines on nDCG@10 while cutting inference latency in half. By embedding IR axioms into attention models, QDS achieves improvements on small-scale benchmarks, but its highly task-specific sparse structure limits generalization.

**中文**

QDS-Transformer[40] 将 IR 公理（局部性、层次结构、查询匹配）集成到结构化稀疏注意力模式中： 𝐴QDS =𝐴 local ∪𝐴 发送 ∪𝐴 查询 ∪𝐴 [CLS]，其中 𝐴local 强制窗口化交互，𝐴sent 将标记链接到句子级 [SOS] 标记，并且𝐴query 将文档单词与查询标记全局连接。在 TREC DL’19 上，QDS-Transformer 在 nDCG@10 的基础上实现了改进，同时将推理延迟减少了一半。通过将 IR 公理嵌入到注意力模型中，QDS 实现了小规模基准的改进，但其高度特定于任务的稀疏结构限制了泛化。

### 段落 71 · Page 10

**EN**

Its design assumptions (such as sentence-level [SOS] tagging) may not hold true in multi-domain or cross-lingual long-document retrieval, and its complex sparse kernel implementation hinders widespread replication.

**中文**

它的设计假设（例如句子级[SOS]标记）可能不适用于多域或跨语言长文档检索，并且其复杂的稀疏内核实现阻碍了广泛的复制。

### Page 11

### 段落 72 · Page 11

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 11 Inspired by the “small-world” phenomenon,Socialformer[ 95] dynamically samples long-range links based on centrality and query-aware distance. It partitions token graphs into “circles” and propagates information via intraand inter-circle Transformers, a method that significantly outperforms BigBird on TREC DL tasks. Compared to static sparse patterns, Socialformer thus exemplifies a shift toward more data-adaptive and dynamic connectivity.

**中文**

PLM 和 LLM 时代的长文档检索综述 11 受“小世界”现象的启发，Socialformer[95]根据中心性和查询感知距离动态采样远程链接。它将令牌图划分为“圈”，并通过圈内和圈间 Transformer 传播信息，这种方法在 TREC DL 任务上显着优于 BigBird。因此，与静态稀疏模式相比，Socialformer 体现了向数据适应性更强和动态连接的转变。

### 段落 73 · Page 11

**EN**

A key practical advantage is its straightforward implementation using standard PyTorch libraries, which avoids the engineering overhead of custom CUDA kernels common in other sparse-attention models. However, its sampling-based strategy can introduce result instability, and the model’s scalability beyond 8,000 tokens remains unverified. M3-Embedding[14], as an innovative embedding model, offers solutions that cater to multilingualism, multifunctionality, and multigranularity.

**中文**

一个关键的实际优势是它使用标准 PyTorch 库直接实现，这避免了其他稀疏注意力模型中常见的自定义 CUDA 内核的工程开销。然而，其基于采样的策略可能会导致结果不稳定，并且该模型超过 8,000 个代币的可扩展性尚未得到验证。 M3-Embedding[14]作为一种创新的嵌入模型，提供了满足多语言、多功能和多粒度的解决方案。

### 段落 74 · Page 11

**EN**

This model is capable of processing long documents containing up to 8,192 tokens and supports various functionalities, including dense retrieval, sparse retrieval, and multi-vector retrieval. M3-Embedding employs a novel self-knowledge distillation method that enhances training quality and retrieval accuracy by integrating relevance scores from different retrieval functions. Its efficient training strategy and robust multilingual support make it highly effective in multilingual retrieval tasks and long-document processing.

**中文**

该模型能够处理包含多达 8,192 个 token 的长文档，并支持各种功能，包括密集检索、稀疏检索和多向量检索。 M3-Embedding 采用了一种新颖的自知识蒸馏方法，通过集成不同检索函数的相关性分数来提高训练质量和检索准确性。其高效的训练策略和强大的多语言支持使其在多语言检索任务和长文档处理中非常有效。

### 段落 75 · Page 11

**EN**

Additionally, M3-Embedding optimizes its batch processing strategy, allowing for efficient handling of large-scale data, especially excelling in long-document retrieval and cross-lingual tasks. 4.1.3 LLMs as Holistic Rerankers.With the advent of large language models , holistic modeling has advanced from efficient Transformers to end-to-end ranking.RankGPT[77] demonstrated that GPT-4 can act as a universal reranker by generating explicit ranked lists (e.g., “[2]>[3]>[1]”), rather than independent scores.

**中文**

此外，M3-Embedding还优化了批处理策略，可以高效处理大规模数据，尤其在长文档检索和跨语言任务方面表现出色。 4.1.3 LLM 作为整体重排序器。随着大型语言模型的出现，整体建模已经从高效的 Transformer 发展到端到端排序。RankGPT[77] 证明，GPT-4 可以通过生成显式排序列表（例如，“[2]>[3]>[1]”）而不是独立分数来充当通用重排序器。

### 段落 76 · Page 11

**EN**

Using a sliding-window strategy, it successfully reranked hundreds of passages, and permutation distillation further transferred this ability to a lightweight 440M DeBERTa, achieving superior nDCG@10 on BEIR with only 1k labels. RankGPT demonstrates the unique capabilities of LLM for listwise ranking. However, its reliance on sliding windows to join long documents can easily introduce query drift: the model may make inconsistent judgments for the same query in different windows. Furthermore, its high inference cost and prompt sensitivity make it difficult to deploy at scale [33].

**中文**

使用滑动窗口策略，它成功地对数百个通道进行了重新排序，排列蒸馏进一步将这种能力转移到轻量级 440M DeBERTa，仅用 1k 个标签就在 BEIR 上实现了卓越的 nDCG@10。 RankGPT 展示了 LLM 在列表排名方面的独特功能。然而，它依赖滑动窗口来连接长文档很容易引入查询漂移：模型可能会对不同窗口中的同一查询做出不一致的判断。此外，其高推理成本和快速敏感性使其难以大规模部署[33]。

### 段落 77 · Page 11

**EN**

More systematically,RepLLaMAandRankLLaMA[ 58] explored fine-tuning LLaMA models as dense retrievers and rerankers, directly encoding full 2k-token documents without segmentation. RepLLaMA uses the </s> embedding as a dense vector for retrieval, while RankLLaMA concatenates query and document for scalar scoring. Together, they established new state-of-the-art results on MS MARCO DL (nDCG@10 = 77.9), eliminating heuristic pooling and proving that LLMs can encode long documents holistically.

**中文**

更系统地，RepLLaMA和RankLLaMA[58]探索了将LLaMA模型微调为密集检索器和重新排序器，直接编码完整的2k-token文档而无需分割。 RepLLaMA 使用 </s> 嵌入作为检索的密集向量，而 RankLLaMA 连接查询和文档以进行标量评分。他们共同在 MS MARCO DL (nDCG@10 = 77.9) 上建立了新的最先进结果，消除了启发式池并证明法学硕士可以对长文档进行整体编码。

### 段落 78 · Page 11

**EN**

Unlike RankGPT’s prompt-based reranking, fine-tuned LLaMA variants support efficient parallel inference, bridging the gap between academic benchmarks and practical deployment. These LLaMA-based models demonstrate the feasibility of globally encoding long documents and have achieved state-of-the-art performance on benchmarks such as MS MARCO. However, their context windows are still limited (2k–4k bytes), making them difficult to directly address the needs of long document IR. Furthermore, fine-tuning can lead to catastrophic forgetting, which degrades performance in short-text retrieval or cross-domain tasks, undermining their practicality.

**中文**

与 RankGPT 基于提示的重排不同，经过微调的 LLaMA 变体支持高效的并行推理，缩小了学术基准与实际部署之间的差距。这些基于 LLaMA 的模型展示了对长文档进行全局编码的可行性，并在 MS MARCO 等基准测试中实现了最先进的性能。然而，它们的上下文窗口仍然有限（2k-4k 字节），这使得它们很难直接满足长文档 IR 的需求。此外，微调可能会导致灾难性遗忘，从而降低短文本检索或跨域任务的性能，从而破坏其实用性。

### 段落 79 · Page 11

**EN**

4.1.4 Efficiency Challenges and Mitigation.While holistic modeling offers strong representational capacity for longdocument retrieval, its deployment in real-world systems is often constrained by efficiency bottlenecks. The primary challenges arise in several dimensions. First, the computational cost of Transformer-based architectures grows quadratically with sequence length, making it prohibitive to process ultra-long inputs or large document collections. Second, storage and indexing overheads increase significantly, as high-dimensional dense embeddings for long documents require substantial memory and incur latency .

**中文**

4.1.4 效率挑战和缓解措施。虽然整体建模为长文档检索提供了强大的表示能力，但其在现实系统中的部署常常受到效率瓶颈的限制。主要挑战出现在几个方面。首先，基于 Transformer 的架构的计算成本随着序列长度呈二次方增长，使得处理超长输入或大型文档集合变得令人望而却步。其次，存储和索引开销显着增加，因为长文档的高维密集嵌入需要大量内存并产生延迟。

### 段落 80 · Page 11

**EN**

Third, inference throughput is limited by the high cost of large language

**中文**

第三，推理吞吐量受到大语言成本高的限制

### Page 12

### 段落 81 · Page 12

**EN**

12 Li et al. Table 1. Representative holistic approaches for long-document retrieval.

**中文**

12 李等人。表 1. 长文档检索的代表性整体方法。

### 段落 82 · Page 12

**EN**

Method Core Mechanism Max Context Length Engineering Complexity IR Effectiveness Key Limitations Naive Truncation (DPR, ANCE) Retain first 512 tokens of BERT; contrastive learning on truncated docs 512 tokens Low (standard PLM) Effective for short passages; weak for longdoc IR Severe information loss; positional bias; ignores discourse structure Longformer / Big- Bird Sparse/blockwise attention (sliding window + global tokens / random links) 4k–16k tokens Medium (custom CUDA kernels often required) Strong on QA/summarization; moderate on IR May miss cross-block evidence; implementation barrier Reformer / FlashAttention LSH attention / IO-awar

**中文**

方法核心机制 最大上下文长度 工程复杂度 IR 有效性 主要限制 Naive Truncation (DPR, ANCE) 保留 BERT 的前 512 个 token；截断文档的对比学习 512 个标记 低（标准 PLM） 对短文有效； longdoc IR 较弱 严重信息丢失；位置偏差；忽略话语结构 Longformer / BigBird 稀疏/块式注意力（滑动窗口 + 全局标记/随机链接） 4k–16k 标记 中等（通常需要自定义 CUDA 内核） QA/总结能力强；对 IR 持温和态度可能会错过跨区块证据；实施障碍 Reformer / FlashAttention LSH 注意力 / IO-awar

### 段落 83 · Page 12

**EN**

e exact attention 8k–16k+ tokens Medium–High (special kernels, memory tuning) Efficient for long text modeling Limited IR-specific optimization; harder training stability LONGEMBED Expand the context size of the embedding model 32k tokens Medium(trainingfree and training strategies) Expand the length of the context.

**中文**

e 精确注意力 8k–16k+ 令牌 中–高（特殊内核、内存调整） 对于长文本建模有效 IR 特定优化有限；更难的训练稳定性 LONGEMBED 扩展嵌入模型的上下文大小 32k tokens 中（trainingfree 和训练策略） 扩展上下文的长度。

### 段落 84 · Page 12

**EN**

Need to explore more context expansion methods based on training.

**中文**

需要探索更多基于训练的上下文扩展方法。

### 段落 85 · Page 12

**EN**

QDS- Transformer IR-axiom-driven sparse pattern (locality, hierarchy, query matching) 4k tokens High (structured sparse kernels) +3.25% nDCG@10 on TREC DL’19 Task-specific design; limited generalizability Socialformer Small-world graph attention; dynamic token circles 8k tokens Medium (Py- Torch only, no custom kernels) Outperforms BigBird on TREC DL Dynamic sampling may destabilize training; scaling beyond 10k unclear RankGPT GPT-4 as reranker; explicit listwise ranking via prompts 8k–32k tokens (via sliding windows) Low (prompting)Strong reranking; distillable into small models Expensive inference; window fragmentation; prompt sensitivity R

**中文**

QDS- Transformer IR 公理驱动的稀疏模式（局部性、层次结构、查询匹配） 4k 标记高（结构化稀疏内核）+3.25% nDCG@10 on TREC DL’19 特定于任务的设计；有限的普遍性 Socialformer 小世界图注意力；动态令牌圈 8k 令牌 中等（仅限 Py-Torch，无自定义内核） 在 TREC DL 上优于 BigBird 动态采样可能会破坏训练的稳定性；缩放超过 10k 不清楚 RankGPT GPT-4 作为重新排序器；通过提示进行明确的列表排名 8k–32k 令牌（通过滑动窗口） 低（提示）强重排；可蒸馏成小模型 昂贵的推理；窗口碎片；提示灵敏度R

### 段落 86 · Page 12

**EN**

epLLaMA / RankLLaMA Fine-tuned LLaMA for retrieval/reranking; holistic doc encoding 2k–4k tokens (native LLaMA) Medium (finetuning infra) SOTA on MS MARCO DL (nDCG@10=77.9) Context length limited; domain robustness concerns LongLoRA / LongLLMLingua / DuoAttention Sparse/grouped-query attention; prompt compression; head specialization 8k–32k tokens High (LLM training + compression) Significant latency reduction; negligible quality loss Faithfulness issues; still quadratic bottlenecks for very long docs model (LLM) rerankers, which are difficult to scale in latency-sensitive retrieval scenarios.

**中文**

epLLaMA / RankLLaMA 用于检索/重排的微调 LLaMA；整体文档编码 2k–4k 令牌（原生 LLaMA） 中等（微调如下） MS MARCO DL 上的 SOTA (nDCG@10=77.9) 上下文长度有限；领域稳健性涉及 LongLoRA / LongLLMLingua / DuoAttention 稀疏/分组查询注意力；及时压缩；头部专业化 8k–32k 令牌 高（LLM 训练 + 压缩） 显着减少延迟；质量损失可忽略不计 忠诚度问题；对于很长的文档模型（LLM）重新排序器来说仍然是二次瓶颈，这在延迟敏感的检索场景中很难扩展。

### 段落 87 · Page 12

**EN**

Finally, multi-document interactions—a common requirement in information retrieval—further amplify the computational burden, since evidence must be aggregated across multiple long contexts. To mitigate these issues, research has explored multiple complementary strategies. On the architectural side, sparseattention mechanisms (e.g., Longformer, BigBird, QDS-Transformer) and hashing-based approximations (e.g., Reformer, Performer, FlashAttention) reduce the asymptotic complexity of self-attention, while hierarchical and graph-based models (e.g., Socialformer) capture global structure with improved scalability.

**中文**

最后，多文档交互（信息检索中的常见要求）进一步加大了计算负担，因为证据必须跨多个长上下文进行聚合。为了缓解这些问题，研究探索了多种互补策略。在架构方面，稀疏注意力机制（例如，Longformer、BigBird、QDS-Transformer）和基于散列的近似（例如，Reformer、Performer、FlashAttention）减少了自注意力的渐近复杂性，而分层和基于图的模型（例如，Socialformer）则以改进的可扩展性捕获全局结构。

### 段落 88 · Page 12

**EN**

Representation-level techniques such as multi-vector encoding (e.g., ColBERT, M3-Embedding), vector quantization, and knowledge distillation enable efficient storage and faster retrieval without severely degrading accuracy. At the retrieval pipeline level, multi-stage architectures remain dominant: a lightweight retriever conducts coarse filtering, followed by query-aware truncation, windowing, or LLM-based reranking. System-level optimizations, including batch inference, caching, and distributed ANN indexing, further enhance throughput in large-scale deployments.

**中文**

多向量编码（例如 ColBERT、M3-Embedding）、向量量化和知识蒸馏等表示级技术可实现高效存储和更快检索，而不会严重降低准确性。在检索管道级别，多阶段架构仍然占主导地位：轻量级检索器进行粗略过滤，然后是查询感知截断、窗口或基于 LLM 的重排。系统级优化，包括批量推理、缓存和分布式 ANN 索引，进一步提高大规模部署中的吞吐量。

### 段落 89 · Page 12

**EN**

Looking forward, efficiency will remain the central challenge for holistic long-document retrieval. Promising directions include adaptive retrieval strategies that dynamically allocate computation based on query complexity, tighter integration of retrieval and reranking models through distillation or adapters, and joint optimization across model,

**中文**

展望未来，效率仍将是整体长文档检索的核心挑战。有希望的方向包括根据查询复杂性动态分配计算的自适应检索策略，通过蒸馏或适配器更紧密地集成检索和重新排序模型，以及跨模型的联合优化，

### Page 13

### 段落 90 · Page 13

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 13 index, and hardware layers. Such approaches aim to bridge the gap between the holistic paradigm’s strong modeling capacity and the stringent efficiency requirements of real-world information retrieval systems. 4.1.5 Limitations and Open Problems.Holistic paradigms, while promising, remain constrained by efficiency, multimodality, and evaluation challenges. First, trade-offs between effectiveness and computational cost remain acute: million-token contexts (e.g., legal codes, technical manuals) remain impractical despite sparse attention and compression.

**中文**

PLM 和 LLM Era 13 索引和硬件层中的长文档检索调查。这些方法旨在弥合整体范式的强大建模能力与现实世界信息检索系统严格的效率要求之间的差距。 4.1.5 局限性和开放性问题。整体范式虽然很有前途，但仍然受到效率、多模态和评估挑战的限制。首先，有效性和计算成本之间的权衡仍然很严重：尽管注意力稀疏和压缩，但百万代币上下文（例如法律法规、技术手册）仍然不切实际。

### 段落 91 · Page 13

**EN**

Second, multimodal long documents: scientific papers with figures or news with embedded tables, remain largely unsupported; current VLMs (e.g., CLIP) lack robust alignment for 10k+ token multimodal contexts. Third, evaluation misalignment threatens progress: standard IR metrics (NDCG, Recall@k) fail to capture LLM-specific issues such as hallucinated evidence or failure to actually use context. Task-oriented metrics for faithfulness and attribution are urgently needed.

**中文**

其次，多模式长文档：带有数字的科学论文或带有嵌入表格的新闻，在很大程度上仍然不受支持；当前的 VLM（例如 CLIP）缺乏针对 10k+ 令牌多模态上下文的稳健对齐。第三，评估不一致会威胁进展：标准IR指标（NDCG、Recall@k）无法捕捉LLM特定的问题，例如幻觉证据或未能实际使用上下文。迫切需要以任务为导向的忠诚度和归因指标。

### 段落 92 · Page 13

**EN**

Finally, robustness concerns including adversarial injections, pretraining contamination, and domain adaptation fragility underscore that LLMs cannot blindly replace IR pipelines. Summary.The holistic paradigm illustrates a clear trajectory: from truncation-limited PLMs, through sparse longsequence Transformers, to end-to-end LLM rerankers. Each generation alleviates prior bottlenecks, but efficiency, faithfulness, and robustness remain fundamental challenges.

**中文**

最后，包括对抗性注入、预训练污染和领域适应脆弱性在内的鲁棒性问题强调了法学硕士不能盲目取代 IR 管道。摘要：整体范式展示了一条清晰的轨迹：从截断限制的 PLM，到稀疏长序列 Transformer，再到端到端的 LLM 重新排序器。每一代都缓解了之前的瓶颈，但效率、忠实性和稳健性仍然是根本挑战。

### 段落 93 · Page 13

**EN**

For practical LDR, holistic approaches must be judiciously integrated with divide-and-conquer strategies, suggesting a hybrid future where block selection, efficient long-sequence encoding, and LLM reranking co-exist within the same pipeline. 4.2 Divide-and-Conquer Paradigm for Long Documents (PLM & LLM Era) In contrast to the holistic paradigm, the divide-and-conquer paradigm tackles the computational bottleneck caused by document length by segmenting long documents into smaller units, applying localized processing, and then aggregating the results.

**中文**

对于实际的 LDR，整体方法必须明智地与分而治之的策略相结合，这表明块选择、高效长序列编码和 LLM 重新排序在同一管道中共存的混合未来。 4.2 长文档的分而治之范式（PLM & LLM 时代） 与整体范式相反，分而治之范式通过将长文档分割成更小的单元，应用本地化处理，然后聚合结果来解决由文档长度引起的计算瓶颈。

### 段落 94 · Page 13

**EN**

In this section, we will examine several key approaches within the divide-and-conquer paradigm, including pooling heuristics, hierarchical aggregation, and key block selection. While these methods are more computationally efficient, they face the challenge of effectively aggregating evidence dispersed across multiple blocks. Fig. 4. A typical workflow for the key block selection approach within the divide-and-conquer paradigm, exemplified by models like KeyB. This approach concatenates the text of selected blocks before a final reranking.

**中文**

在本节中，我们将研究分治范式中的几种关键方法，包括池启发法、分层聚合和关键块选择。虽然这些方法的计算效率更高，但它们面临着有效聚合分散在多个区块中的证据的挑战。图 4. 分而治之范式中关键块选择方法的典型工作流程，以 KeyB 等模型为例。此方法在最终重排之前连接所选块的文本。

### Page 14

### 段落 95 · Page 14

**EN**

14 Li et al. 4.2.1 Pooling-based Heuristics: BERT-MaxP and SumP.The earliest adaptation simply applied BERT to fixed-length passages and aggregated passage scores. Dai and Callan [21] introducedBERT-MaxP/SumP, where each document 𝑑 is segmented into passages {𝑝1, . . . , 𝑝𝑛 }; query–passage pairs (𝑞, 𝑝𝑖 ) are scored by a fine-tuned BERT cross-encoder, and document-level scores are aggregated: MaxP :𝑆(𝑑, 𝑞)=max 𝑖 𝑓BERT (𝑞, 𝑝𝑖 ),(3) SumP :𝑆(𝑑, 𝑞)= ∑︁ 𝑖 𝑓BERT (𝑞, 𝑝𝑖 ).(4) MaxP typically performs best, as it highlights the most relevant passage, but suffers when relevance is spread across multiple passages.

**中文**

14 李等人。 4.2.1 基于池化的启发式算法：BERT-MaxP 和 SumP。最早的改编只是将 BERT 应用于固定长度的段落和聚合的段落分数。 Dai 和 Callan [21] 引入了 BERT-MaxP/SumP，其中每个文档 𝑑 被分割成段落 {𝑝1, .。。 , 𝑝𝑛 };查询-段落对 (𝑞, 𝑝𝑖 ) 由微调的 BERT 交叉编码器进行评分，并聚合文档级分数： MaxP :𝑆(𝑑, 𝑞)=max 𝑖 𝑓BERT (𝑞, 𝑝𝑖 ),(3) SumP :𝑆(𝑑, 𝑞)= Σ︁ 𝑖 𝑓BERT (𝑞, 𝑝𝑖 )。(4) MaxP 通常表现最好，因为它突出显示了最相关的段落，但当相关性分布在多个段落中时，它就会受到影响。

### 段落 96 · Page 14

**EN**

Despite its simplicity, BERT-MaxP/SumP already outperformed strong lexical and neural baselines on Robust04 and ClueWeb09-B, especially for longer natural language queries. However, these heuristics inherit three key limitations: (i) distributed signals across passages may be lost; (ii) overemphasis on a single high-scoring passage risks missing complementary evidence; (iii) no mechanism for modeling document structure.

**中文**

尽管很简单，但 BERT-MaxP/SumP 在 Robust04 和 ClueWeb09-B 上的性能已经优于强大的词汇和神经基线，特别是对于较长的自然语言查询。然而，这些启发式方法继承了三个关键局限性：（i）跨通道的分布式信号可能会丢失； (ii) 过分强调单个高分段落可能会丢失补充证据； (iii) 没有对文档结构进行建模的机制。

### 段落 97 · Page 14

**EN**

4.2.2 Hierarchical Aggregation: PARADE, DRSCM, LTR-BERT, and MORES+.To specifically address the loss of distributed signals and the overemphasis on a single high-scoring passage inherent in simple pooling, later works introduced explicit mechanisms to aggregate passage-level signals into document-level representations. PARADE [48] encodes each (𝑞, 𝑝𝑖 ) pair using a cross-encoder PLM to obtain passage representations ℎ𝑖, then aggregates them via multiple strategies, from simple pooling to learned networks.

**中文**

4.2.2 分层聚合：PARADE、DRSCM、LTR-BERT 和 MORES+。为了专门解决分布式信号的丢失以及简单池化中固有的对单个高分段落的过分强调，后来的工作引入了显式机制，将段落级信号聚合为文档级表示。 PARADE [48] 使用交叉编码器 PLM 对每个 (𝑞, 𝑝𝑖) 对进行编码，以获得段落表示 ℎ𝑖，然后通过多种策略（从简单池化到学习网络）聚合它们。

### 段落 98 · Page 14

**EN**

Among its learned strategies, PARADE-Attn uses a trainable vector to weigh passage importance, while the most powerful variant, PARADE- Transformer, employs a second Transformer encoder to model global dependencies between the passages. The final aggregated representation is then passed to a linear layer for scoring, allowing the model to form a holistic judgment based on evidence scattered across the text. The authors show that such learned aggregation methods consistently outperform simple heuristics, demonstrating that relevance in long documents often emerges from these cross-passage interactions.

**中文**

在其学习策略中，PARADE-Attn 使用可训练向量来衡量段落重要性，而最强大的变体 PARADE-Transformer 采用第二个 Transformer 编码器来模拟段落之间的全局依赖关系。然后，最终的聚合表示被传递到线性层进行评分，使模型能够根据分散在文本中的证据形成整体判断。作者表明，这种学习的聚合方法始终优于简单的启发式方法，这表明长文档中的相关性通常来自这些跨段落的交互。

### 段落 99 · Page 14

**EN**

DRSCM [82] argues that relevance cannot be assessed locally alone, since topically divergent but locally relevant passages may dominate scores. To address this, it computes a segment correlation matrix offline, capturing the global centrality of each passage within the document. During online retrieval, passage scores are a linear combination of this global weight and the local query similarity, yielding robustness against topic drift. This architecture is highly efficient, as the computationally expensive correlation matrix is pre-computed, leaving only the lightweight combination for inference.

**中文**

DRSCM [82] 认为相关性不能单独在局部进行评估，因为主题不同但局部相关的段落可能会主导分数。为了解决这个问题，它离线计算片段相关矩阵，捕获文档中每个段落的全局中心性。在在线检索期间，段落分数是全局权重和本地查询相似性的线性组合，从而产生针对主题漂移的鲁棒性。这种架构非常高效，因为计算成本昂贵的相关矩阵是预先计算的，只留下轻量级组合用于推理。

### 段落 100 · Page 14

**EN**

These combined segment scores are then aggregated using a final pooling step (e.g., taking the maximum score) to produce the document-level ranking. DRSCM thus effectively bridges local query matching with the global semantic structure of the document. LTR-BERT [81] decouples heavy offline document encoding from lightweight online query processing. Long documents are segmented and encoded offline, producing compressed passage embeddings. At query time, a short query is expanded and encoded online, then matched to stored embeddings using a parameter-free late interaction mechanism.

**中文**

然后使用最终合并步骤（例如，取最高分数）聚合这些组合的分段分数以产生文档级排名。因此，DRSCM 有效地将本地查询匹配与文档的全局语义结构联系起来。 LTR-BERT [81] 将繁重的离线文档编码与轻量级的在线查询处理解耦。长文档被离线分段和编码，产生压缩的段落嵌入。在查询时，在线扩展和编码短查询，然后使用无参数的后期交互机制与存储的嵌入进行匹配。

### 段落 101 · Page 14

**EN**

This lightweight matching operates token-wise: for each query token, it finds the most similar document token within a passage, and the final score is computed by comparing the averaged vectors of the query and these selected best-match tokens. Notably, the model is trained efficiently on short-text pairs and uses a BERT-MaxP-style final aggregation, but achieves its speed by replacing the expensive cross-encoder with its parameter-free calculation. The result is a large

**中文**

这种轻量级匹配按标记进行操作：对于每个查询标记，它会找到段落中最相似的文档标记，并通过比较查询的平均向量和这些选定的最佳匹配标记来计算最终分数。值得注意的是，该模型在短文本对上进行了有效的训练，并使用了 BERT-MaxP 式的最终聚合，但通过用无参数计算替换昂贵的交叉编码器来实现其速度。结果是一个大

### Page 15

### 段落 102 · Page 15

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 15 efficiency gain: processing up to 333 times more documents per millisecond, while still outperforming cross-encoder baselines on MS MARCO document ranking. MORES+ [29] is a modular Transformer re-ranker that enables full query-to-document token interaction. Documents are chunked into segments, independently encoded by an encoder module, then jointly attended by a query-aware interaction module. Architecturally, it achieves this by using a BART encoder to process each chunk and a modified BART decoder for the joint query-to-all-chunk cross-attention.

**中文**

PLM 和 LLM Era 15 中的长文档检索调查 效率增益：每毫秒处理的文档数量增加了 333 倍，同时在 MS MARCO 文档排名上仍然优于跨编码器基线。 MORES+ [29] 是一个模块化 Transformer 重新排序器，可实现完整的查询到文档令牌交互。文档被分成片段，由编码器模块独立编码，然后由查询感知交互模块共同参与。在架构上，它通过使用 BART 编码器来处理每个块和修改后的 BART 解码器来实现联合查询到所有块的交叉注意。

### 段落 103 · Page 15

**EN**

This design is highly efficient, maintaining linear complexity with respect to document length and supporting offline pre-computation of chunk representations to speed up inference. Unlike PARADE, MORES+ allows cross-attention across all document tokens, mitigating information loss from pooling. On Robust04 and MS MARCO, MORES+ outperformed PARADE and BERT-MaxP, establishing new state-of-the-art results at the time. Hierarchical methods demonstrate that aggregating dispersed evidence is essential in long documents.

**中文**

这种设计非常高效，保持了文档长度的线性复杂性，并支持块表示的离线预计算以加速推理。与 PARADE 不同，MORES+ 允许跨所有文档标记进行交叉关注，从而减少池化造成的信息丢失。在 Robust04 和 MS MARCO 上，MORES+ 的表现优于 PARADE 和 BERT-MaxP，建立了当时新的最先进结果。分层方法表明，在长文档中聚合分散的证据至关重要。

### 段落 104 · Page 15

**EN**

PARADE and DRSCM emphasize learned and global aggregation, while LTR-BERT and MORES+ highlight architectural innovations for efficiency and fine-grained query–document interactions. Yet, their reliance on fixed segmentation risks fragmenting semantics, motivating selective and dynamic strategies. 4.2.3 Key Passage/Block Selection: IDCM, KeyB, KeyB2, and DCS.Another strategy is to first filter key content before deep re-ranking, reducing both cost and noise. IDCM[35] addresses the high query latency of re-ranking all passages in a long document with a powerful model.

**中文**

PARADE 和 DRSCM 强调学习和全局聚合，而 LTR-BERT 和 MORES+ 则强调效率和细粒度查询-文档交互的架构创新。然而，它们对固定分割的依赖可能会导致语义碎片化，从而激发选择性和动态策略。 4.2.3 关键段落/块选择：IDCM、KeyB、KeyB2 和 DCS。另一种策略是在深度重新排序之前首先过滤关键内容，从而降低成本和噪声。 IDCM[35] 使用强大的模型解决了对长文档中的所有段落重排的高查询延迟问题。

### 段落 105 · Page 15

**EN**

It employs a two-stage cascade where a lightweight "student" model first rapidly selects the top- 𝑘 most promising passages from within the document. Subsequently, a more powerful but computationally expensive "teacher" model re-scores only this small candidate set. Notably, the student model is trained to mimic the teacher’s scoring behavior through a three-step knowledge distillation process, rather than being trained on ground-truth labels directly.

**中文**

它采用两阶段级联，其中轻量级“学生”模型首先从文档中快速选择最有希望的段落。随后，一个更强大但计算成本昂贵的“教师”模型仅对这个小候选集重新评分。值得注意的是，学生模型被训练为通过三步知识蒸馏过程来模仿教师的评分行为，而不是直接在真实标签上进行训练。

### 段落 106 · Page 15

**EN**

This strategy allows IDCM to achieve effectiveness comparable to a full BERT-based evaluation while reducing median query latency by more than four times, crucially avoiding the need for expensive manual passage-level annotations. KeyB [52] analyzed that relevance signals are widely distributed but uneven in long documents. KeyB first selects key blocks using either a fast BM25 scorer or a more powerful learned BERT-based selector, then concatenates them for final ranking via a Transformer model like BERT or PARADE.

**中文**

该策略使 IDCM 能够实现与完全基于 BERT 的评估相当的有效性，同时将中值查询延迟减少四倍以上，至关重要的是避免了昂贵的手动段落级注释的需要。 KeyB[52]分析发现，相关信号在长文档中分布广泛但不均匀。 KeyB 首先使用快速 BM25 评分器或更强大的基于 BERT 的学习选择器来选择关键块，然后通过 BERT 或 PARADE 等 Transformer 模型将它们连接起来以进行最终排名。

### 段落 107 · Page 15

**EN**

Its most innovative variant, known as "BERT in BERT, " cleverly reuses the same Transformer model to first score and select the key blocks and then to perform the final ranking on the concatenated result. While this learned selection scheme achieves state-of-the-art results on benchmarks like TREC DL, the simpler and much faster BM25-based selector offers a strong practical alternative by providing an excellent balance between performance and efficiency. This select-then-process strategy allows KeyB to consistently surpass sparse-attention models and pooling baselines.

**中文**

其最具创新性的变体被称为“BERT in BERT”，巧妙地重用相同的 Transformer 模型来首先评分并选择关键块，然后对串联结果执行最终排名。虽然这种学习选择方案在 TREC DL 等基准测试中取得了最先进的结果，但更简单、更快的基于 BM25 的选择器通过在性能和效率之间提供出色的平衡，提供了强大的实用替代方案。这种先选择后处理的策略使 KeyB 能够持续超越稀疏注意力模型和池基线。

### 段落 108 · Page 15

**EN**

KeyB2[50] adapts the KeyB framework for the LLM era by employing a variety of selectors—including BM25, crossencoders, and bi-encoders—to identify key blocks. These blocks are then processed by large LLM rerankers, such as LLaMA-3. In terms of effectiveness, this approach achieves state-of-the-art performance on the TREC DL benchmark, as measured by NDCG@10. The model also demonstrates significant efficiency gains, doubling the inference speed compared to full-document rerankers like RankLLaMA. This speedup is possible because the LLM only needs to process a small, highly relevant subset of the document’s content.

**中文**

KeyB2[50]通过采用各种选择器（包括 BM25、交叉编码器和双编码器）来识别关键块，从而适应 LLM 时代的 KeyB 框架。然后，这些块由大型 LLM 重新排序器（例如 LLaMA-3）进行处理。就有效性而言，根据 NDCG@10 的衡量，该方法在 TREC DL 基准上实现了最先进的性能。该模型还显示出显着的效率提升，与 RankLLaMA 等全文档重新排序器相比，推理速度提高了一倍。这种加速是可能的，因为法学硕士只需要处理文档内容的一小部分高度相关的子集。

### 段落 109 · Page 15

**EN**

The success of KeyB2 demonstrates that even with powerful LLMs, strategic block selection remains crucial for reducing redundancy and focusing model capacity on the most salient evidence.

**中文**

KeyB2 的成功表明，即使拥有强大的法学硕士，战略块选择对于减少冗余并将模型能力集中在最显着的证据上仍然至关重要。

### Page 16

### 段落 110 · Page 16

**EN**

16 Li et al. BReps [51] introduces a block-level representation framework for LDR. Documents are segmented into short, semantically coherent blocks, each encoded independently by a LLM. At query time, the query embedding is matched against all block embeddings, and the top-𝑘 relevant block scores are aggregated to produce the document-level score. This design enables offline pre-computation of block representations and lightweight online scoring, while capturing fine-grained matching signals that are often lost in single-vector representations.

**中文**

16 李等人。 BReps [51] 引入了 LDR 的块级表示框架。文档被分割成简短的、语义连贯的块，每个块都由法学硕士独立编码。在查询时，查询嵌入与所有块嵌入进行匹配，并且顶部𝑘相关块分数被聚合以产生文档级分数。这种设计可以实现块表示的离线预计算和轻量级在线评分，同时捕获在单向量表示中经常丢失的细粒度匹配信号。

### 段落 111 · Page 16

**EN**

Compared with dense (e.g., RepLLaMA) and late-interaction baselines, BReps achieves higher effectiveness, demonstrating consistent gains across multiple long document benchmarks. DCS [71] addresses the incoherence of fixed-length segmentation through a two-stage process. First, for dynamic chunking, it identifies topic boundaries by calculating the semantic distance between adjacent sentences to create coherent segments. This is achieved by using Sentence-BERT embeddings and identifying split points where the cosine similarity between adjacent sentences is lowest, indicating a topic shift.

**中文**

与密集（例如 RepLLaMA）和后期交互基线相比，BReps 实现了更高的有效性，在多个长文档基准测试中表现出一致的收益。 DCS [71]通过两阶段过程解决了固定长度分段的不连贯性。首先，对于动态分块，它通过计算相邻句子之间的语义距离来识别主题边界，以创建连贯的片段。这是通过使用 Sentence-BERT 嵌入并识别相邻句子之间的余弦相似度最低（表明主题转移）的分割点来实现的。

### 段落 112 · Page 16

**EN**

Next, a lightweight classifier is trained to mimic the attention patterns of a more powerful teacher LLM via feature distillation. Specifically, the classifier learns to predict chunk relevance from features distilled from the teacher LLM’s cross-attention matrix between the question and the context. This allows the classifier to efficiently select the most relevant chunks to feed into the final model. Experiments on long-context QA benchmarks show DCS robustly outperforms static chunking and maintains high accuracy even at 256k tokens. Selection methods explicitly balance efficiency and effectiveness.

**中文**

接下来，训练一个轻量级分类器，通过特征蒸馏来模仿更强大的法学硕士教师的注意力模式。具体来说，分类器学习从教师法学硕士问题和上下文之间的交叉注意力矩阵中提取的特征来预测块相关性。这使得分类器能够有效地选择最相关的块来输入最终模型。长上下文 QA 基准测试表明，DCS 的性能明显优于静态分块，即使在 256k 个标记下也能保持高精度。选择方法明确地平衡了效率和效果。

### 段落 113 · Page 16

**EN**

IDCM cascades reduce latency; KeyB and KeyB2 show that intelligent block selection can even outperform full-document LLM rerankers; DCS demonstrates dynamic, semantically coherent segmentation. However, learned selectors may be costly to train, and the risk of missing critical evidence remains. 4.2.4 Hybrid Cascades and Late Interaction: ICLI, Match-Ignition, and Longtriever.Hybrid approaches combine multiple paradigms to jointly exploit local and global semantics. ICLI[49] model utilizes a single BERT architecture within a cascaded ranking process to balance efficiency and effectiveness.

**中文**

IDCM级联减少延迟； KeyB 和 KeyB2 表明，智能块选择甚至可以优于完整文档的 LLM 重新排序器； DCS 展示了动态的、语义连贯的分割。然而，学习选择器的训练成本可能很高，并且丢失关键证据的风险仍然存在。 4.2.4 混合级联和后期交互：ICLI、Match-Ignition 和 Longtriever。混合方法结合了多种范式，共同利用局部和全局语义。 ICLI[49]模型在级联排名过程中利用单个 BERT 架构来平衡效率和效果。

### 段落 114 · Page 16

**EN**

First, a fast pre-ranking stage uses the [CLS] token embedding of each passage to quickly identify a small set of top-𝑘 candidates from the long document. Subsequently, a more precise but computationally expensive re-ranking stage, based on a ColBERT-style MaxSim operation, is applied only to this filtered set of passages. This entire two-stage process is trained end-to-end with multi-task learning, enabling the single model to master both tasks. The approach yields significant gains, improving NDCG@10 by 8% over ColBERT[44] while achieving three times the inference speed of BERT-CAT.

**中文**

首先，快速预排名阶段使用每个段落的 [CLS] 令牌嵌入来快速从长文档中识别一小部分 top-𝑘 候选者。随后，基于 ColBERT 式 MaxSim 操作的更精确但计算成本昂贵的重新排序阶段仅应用于这组经过过滤的段落。整个两阶段过程通过多任务学习进行端到端训练，使单个模型能够掌握这两项任务。该方法取得了显着的成果，与 ColBERT[44] 相比，NDCG@10 提高了 8%，同时推理速度是 BERT-CAT 的三倍。

### 段落 115 · Page 16

**EN**

Match-Ignition [61] is a hierarchical noise-filtering framework designed to mitigate the signal dilution problem common in long-document matching. It operates using a two-stage filtering cascade. First, a lightweight scorer prunes sentences with low cross-document similarity to remove noisy, unrelated content. Second, a word-level co-occurrence graph is constructed from the remaining text, and the PageRank algorithm is used to identify and filter out lowimportance words.

**中文**

Match-Ignition [61] 是一个分层噪声过滤框架，旨在减轻长文档匹配中常见的信号稀释问题。它使用两级过滤级联进行操作。首先，轻量级评分器修剪跨文档相似度较低的句子，以删除嘈杂的、不相关的内容。其次，根据剩余文本构建单词级共现图，并使用 PageRank 算法来识别和过滤掉低重要性单词。

### 段落 116 · Page 16

**EN**

This aggressive distillation of the input allows a standard Transformer to match the documents’ salient components without exceeding token limits, leading to strong performance on tasks like plagiarism detection and citation recommendation. Longtriever [89] addresses the limitations of traditional hierarchical models, where document blocks are often processed independently, leading to a loss of global context. Its architecture introduces a "tightly-coupled" interaction mechanism between local and global semantics.

**中文**

这种对输入的积极提炼使得标准 Transformer 能够在不超出标记限制的情况下匹配文档的显着组件，从而在抄袭检测和引文推荐等任务上表现出强大的性能。 Longtriever [89]解决了传统分层模型的局限性，其中文档块通常是独立处理的，导致全局上下文的丢失。其架构引入了局部语义和全局语义之间的“紧耦合”交互机制。

### 段落 117 · Page 16

**EN**

At each layer, an inter-block encoder first models the global context by attending over special [DOC] and [CLS] tokens from all blocks. This global context is then fed back into the intra-block

**中文**

在每一层，块间编码器首先通过关注来自所有块的特殊 [DOC] 和 [CLS] 标记来对全局上下文进行建模。然后这个全局上下文被反馈到块内

### Page 17

### 段落 118 · Page 17

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 17 encoders, allowing each block to be processed with an awareness of the full document’s content. To combat annotation scarcity, Longtriever also introduces a novel pre-training task, Local Masked Autoencoder (LMAE), which learns to reconstruct tokens by fusing both global and local representations. This design leads to state-of-the-art performance on benchmarks like the MS MARCO Document Ranking and TREC Deep Learning tracks, outperforming other hierarchical and sparse-attention models.

**中文**

PLM 和 LLM Era 17 编码器中的长文档检索调查，允许在了解完整文档内容的情况下处理每个块。为了解决注释稀缺问题，Longtriever 还引入了一种新颖的预训练任务，即本地掩码自动编码器 (LMAE)，它通过融合全局和局部表示来学习重建标记。这种设计在 MS MARCO 文档排名和 TREC 深度学习轨道等基准测试中实现了最先进的性能，优于其他分层和稀疏注意力模型。

### 段落 119 · Page 17

**EN**

Furthermore, it achieves this effectiveness while maintaining a favorable efficiency profile, with a sub-quadratic complexity and inference latency comparable to other block-based methods. Hybrid designs aim to unify efficiency and comprehensiveness. ICLI integrates dense retrieval with late interaction in a single architecture; Match-Ignition filters noise hierarchically; Longtriever couples local and global encoders. While effective, these models introduce additional architectural complexity and require careful efficiency–effectiveness trade-offs.

**中文**

此外，它在保持良好效率的同时实现了这种有效性，其复杂度和推理延迟与其他基于块的方法相当。混合设计旨在统一效率和综合性。 ICLI 将密集检索与后期交互集成在单一架构中； Match-Ignition 分层过滤噪声； Longtriever 连接本地和全局编码器。虽然有效，但这些模型引入了额外的架构复杂性，并且需要仔细的效率与效果权衡。

### 段落 120 · Page 17

**EN**

4.2.5 Overall Assessment.Divide-and-conquer remains the most mature and widely explored paradigm for adapting PLMs and LLMs to long documents. It offers practical compromises by decomposing input, but faces three persistent challenges: (i) semantic fragmentation from segmentation; (ii) risk of missing distributed signals in selection; (iii) computational inefficiency when scaling to millions of documents.

**中文**

4.2.5 总体评估。分而治之仍然是使 PLM 和 LLM 适应长文档的最成熟且探索最广泛的范例。它通过分解输入提供了实际的妥协，但面临三个持续的挑战：（i）分割带来的语义碎片； (ii) 选择时丢失分布式信号的风险； (iii) 当扩展到数百万个文档时计算效率低下。

### 段落 121 · Page 17

**EN**

Emerging LLM-based methods suggest that intelligent selection, hierarchical modeling, and hybrid cascades can substantially mitigate these issues, yet further innovations in efficiency, robustness, and multimodal integration remain critical for real-world deployment.The persistent challenge of semantic fragmentation from fixed segmentation also motivated a different line of research that focuses not on the model architecture, but on the indexing structure itself, as discussed in the next section.

**中文**

新兴的基于 LLM 的方法表明，智能选择、分层建模和混合级联可以大大缓解这些问题，但效率、鲁棒性和多模式集成方面的进一步创新对于现实世界的部署仍然至关重要。固定分割带来的语义碎片的持续挑战也激发了不同的研究方向，这些研究重点不是模型架构，而是索引结构本身，如下一节所述。

### 段落 122 · Page 17

**EN**

4.3 Indexing-Structure-Oriented Paradigm While most long-document retrieval research focuses on model architectures , a complementary line of work emphasizes how documents are segmented and indexed. Naive fixed-length chunking often truncates relevant content or mixes unrelated information, limiting the effectiveness of even strong retrievers. Recent studies therefore redesign the indexing structure itself, providing orthogonal improvements that can seamlessly integrate with sparse or dense retrievers. This section reviews three representative paradigms, whose core workflows are conceptually illustrated in Figure 5.

**中文**

4.3 面向索引结构的范式 虽然大多数长文档检索研究都集中在模型架构上，但互补的工作重点是如何对文档进行分段和索引。简单的固定长度分块通常会截断相关内容或混合不相关的信息，从而限制了即使是强大的检索器的有效性。因此，最近的研究重新设计了索引结构本身，提供了可以与稀疏或密集检索器无缝集成的正交改进。本节回顾了三种代表性范例，其核心工作流程在概念上如图 5 所示。

### 段落 123 · Page 17

**EN**

MC-indexing [27] improves retrieval by optimizing the indexing structure itself, rather than the retriever model. As illustrated in Figure 5 (a), this process begins by segmenting a long document into semantically coherent units via "content-aware chunking. " This initial step is critical, as it uses the document’s header hierarchy to preserve semantic boundaries often broken by arbitrary fixed-length methods. Subsequently, each unit is indexed under three complementary views: the original raw text, an LLM-generated summary, and a set of extracted keywords.

**中文**

MC-indexing [27] 通过优化索引结构本身而不是检索器模型来改进检索。如图 5 (a) 所示，此过程首先通过“内容感知分块”将长文档分割成语义连贯的单元。这个初始步骤至关重要，因为它使用文档的标头层次结构来保留经常被任意固定长度方法打破的语义边界。随后，每个单元都在三个互补视图下建立索引：原始文本、LLM 生成的摘要和一组提取的关键字。

### 段落 124 · Page 17

**EN**

During retrieval, an off-the-shelf retriever scores each view independently before the results are aggregated. The method’s unsupervised and plug-and-play design requires no retriever fine-tuning and can be seamlessly integrated with both sparse models like BM25 and various dense encoders. This leads to substantial recall improvements on long-document QA benchmarks, with gains of up to 40% on WikiWeb2M. HELD [12] model automatically extracts variable-depth logical hierarchies from long documents. Its workflow, depicted in Figure 5 (b), innovatively mimics the human reading process.

**中文**

在检索过程中，现成的检索器会在聚合结果之前对每个视图进行独立评分。该方法的无监督和即插即用设计不需要检索器微调，并且可以与 BM25 等稀疏模型和各种密集编码器无缝集成。这导致长文档 QA 基准的召回率大幅提高，在 WikiWeb2M 上提升高达 40%。 HELD [12]模型自动从长文档中提取可变深度的逻辑层次结构。其工作流程如图 5 (b) 所示，创新地模仿了人类阅读过程。

### 段落 125 · Page 17

**EN**

It sequentially processes document objects like paragraphs and tables, feeding them into a “Put-or-Skip” classifier. This classifier makes its decision by fusing both textual features and crucial visual cues, such as font size and indentation, from the document objects. This core mechanism then determines the correct attachment point for each object within a dynamically growing tree structure. To maintain efficiency and the document’s original reading order, the model cleverly constrains this search to the

**中文**

它按顺序处理段落和表格等文档对象，将它们输入“放置或跳过”分类器。该分类器通过融合文档对象的文本特征和关键视觉提示（例如字体大小和缩进）来做出决定。然后，该核心机制确定动态生长的树结构中每个对象的正确附着点。为了保持效率和文档的原始阅读顺序，该模型巧妙地将搜索限制在

### Page 18

### 段落 126 · Page 18

**EN**

18 Li et al. Fig. 5. Conceptual overview of three indexing-structure-oriented paradigms: (a) MC-indexing, (b) HELD, and (c) RAPTOR. "rightmost-branch" of the tree. A particularly effective two-step variant first constructs a tree from the document’s headings before attaching content blocks. This approach not only achieves over 97% accuracy on financial datasets but also significantly improves downstream passage retrieval, demonstrating the value of structural indexing over flat chunking. RAPTOR[68] organizes a document into a semantic tree through a process of recursive clustering and summarization.

**中文**

18 李等人。图 5. 三种面向索引结构的范式的概念概述：(a) MC 索引、(b) HELD 和 (c) RAPTOR。树的“最右边的分支”。一个特别有效的两步变体首先根据文档的标题构建一棵树，然后再附加内容块。这种方法不仅在金融数据集上实现了超过 97% 的准确率，而且还显着改善了下游段落检索，证明了结构索引相对于平面分块的价值。 RAPTOR[68]通过递归聚类和摘要的过程将文档组织成语义树。

### 段落 127 · Page 18

**EN**

As visualized in Figure 5 (c), this bottom-up construction begins with initial text chunks (leaf nodes). These chunks are then recursively clustered based on semantic similarity and summarized by an LLM to form higher-level nodes. The diagram illustrates this iterative process, showing how multiple layers of summaries are built until a single root node is formed, effectively grouping semantically related information regardless of its original position in the text. For querying, RAPTOR’s more robust "collapsed tree" strategy was found to be superior to a simple top-down traversal.

**中文**

如图 5 (c) 所示，这种自下而上的构造从初始文本块（叶节点）开始。然后根据语义相似性对这些块进行递归聚类，并由 LLM 进行总结以形成更高级别的节点。该图说明了这个迭代过程，显示了如何构建多层摘要直到形成单个根节点，从而有效地对语义相关的信息进行分组，无论其在文本中的原始位置如何。对于查询，RAPTOR 更强大的“折叠树”策略被发现优于简单的自顶向下遍历。

### 段落 128 · Page 18

**EN**

This approach works by flattening all nodes from the tree (both original chunks and all levels of summaries) into a single pool. A standard dense retrieval is then performed across this entire pool, allowing the query to match information at any level of abstraction. By leveraging these multiple levels of abstraction, RAPTOR achieves notable gains on complex question-answering tasks. For instance, on the QuALITY dataset[64] , it boosts accuracy by over 8 percentage points compared to a DPR baseline, highlighting the potential of hierarchical, abstraction-aware indexing.

**中文**

这种方法的工作原理是将树中的所有节点（原始块和所有级别的摘要）展平到单个池中。然后在整个池中执行标准密集检索，允许查询匹配任何抽象级别的信息。通过利用这些多层次的抽象，RAPTOR 在复杂的问答任务上取得了显着的成果。例如，在 QuALITY 数据集[64] 上，与 DPR 基线相比，它的准确性提高了 8 个百分点以上，凸显了分层、抽象感知索引的潜力。

### 段落 129 · Page 18

**EN**

Collectively, these indexing-structure-oriented paradigms highlight three complementary strategies: MC-indexing enriches chunk representations through multiple views, HELD reconstructs a document’s explicit logical hierarchy, and RAPTOR builds an implicit semantic hierarchy via recursive summarization. These methods underscore a crucial insight: retrieval effectiveness is not solely dependent on model architecture but is fundamentally constrained by how documents are segmented, represented, and indexed.

**中文**

总的来说，这些面向索引结构的范式突出了三种互补策略：MC索引通过多个视图丰富块表示，HELD重建文档的显式逻辑层次结构，RAPTOR通过递归摘要构建隐式语义层次结构。这些方法强调了一个重要的见解：检索有效性不仅取决于模型架构，而且从根本上受到文档分段、表示和索引方式的限制。

### 段落 130 · Page 18

**EN**

Significant open challenges remain, particularly in handling heterogeneous document formats , integrating multimodal elements, and aligning these advanced indexing strategies with LLM-based retrievers for end-to-end optimization.

**中文**

仍然存在重大的开放挑战，特别是在处理异构文档格式、集成多模式元素以及将这些高级索引策略与基于 LLM 的检索器相结合以进行端到端优化方面。

### Page 19

### 段落 131 · Page 19

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 19 4.4 Long-Query Retrieval: The Query-by-Document Task In specialized domains such as legal case retrieval, patent prior-art search, and scientific literature analysis, search tasks often move beyond short keywords, giving rise to the Query-by-Document paradigm. In this setting, the query itself is a long, complex document used to find other semantically related documents. This "query-by-example" approach dramatically intensifies the core challenges of LDR.

**中文**

PLM 和 LLM 时代的长文档检索综述 19 4.4 长查询检索：按文档查询任务 在法律案例检索、专利现有技术检索和科学文献分析等专业领域，检索任务往往超越短关键字，从而产生了按文档查询范式。在此设置中，查询本身是一个长而复杂的文档，用于查找其他语义相关的文档。这种“示例查询”方法极大地加剧了 LDR 的核心挑战。

### 段落 132 · Page 19

**EN**

The problem of managing document length is squared—as both queries and candidates can span thousands of tokens—making efficiency and pre-computation paramount. Relevance signals also become more dispersed, demanding robust methods to aggregate conceptual similarity in the absence of strong lexical overlap. Consequently, conventional solutions are often inadequate: naive truncation risks information loss and positional bias, while exhaustive cross-encoder comparisons across all passages are computationally prohibitive.

**中文**

管理文档长度的问题是平方的——因为查询和候选都可以跨越数千个标记——使得效率和预计算变得至关重要。相关性信号也变得更加分散，需要稳健的方法来在没有强烈词汇重叠的情况下聚合概念相似性。因此，传统的解决方案通常是不够的：简单的截断可能会导致信息丢失和位置偏差，而对所有段落进行详尽的跨编码器比较在计算上是令人望而却步的。

### 段落 133 · Page 19

**EN**

To address these challenges, sentence-level bi-encoder models have been proposed, including one based on aReranking withProportionalRelevanceScore (RPRS) [ 4]. Built on SBERT, RPRS operates by segmenting both the query𝑄 and candidate document 𝐷 into sentences.

**中文**

为了解决这些挑战，人们提出了句子级双编码器模型，其中包括基于比例相关性分数重排（RPRS）的模型[4]。 RPRS 基于 SBERT 构建，通过将查询𝑄 和候选文档 𝐷 分割成句子来运行。

### 段落 134 · Page 19

**EN**

Each sentence is then passed through an encoder 𝐸(·) to produce its vector embedding: u𝑖 =𝐸(𝑞 𝑖 ),v 𝑗 =𝐸(𝑑 𝑗 ), 𝑠 𝑖 𝑗 =cos(u 𝑖,v 𝑗 ).(5) Based on a similarity threshold𝜏, it then computes two coverage proportions: QP(𝑄→𝐷)= 1 𝑚 𝑚∑︁ 𝑖=1 I  max 𝑗 𝑠𝑖 𝑗 ≥𝜏  ,(6) DP(𝐷→𝑄)= 1 𝑛 𝑛∑︁ 𝑗=1 I  max 𝑖 𝑠𝑖 𝑗 ≥𝜏  ,(7) where QP measures the fraction of query sentences that find a close match in 𝐷, and DP measures the fraction of document sentences covered by𝑄. The final Proportional Relevance Score is the product of these two components: 𝑆RPRS (𝑄, 𝐷)=QP(𝑄→𝐷) ×DP(𝐷→𝑄).(8) This sentence-level design is key to its effectiveness in QBD settings.

**中文**

然后，每个句子通过编码器 𝐸(·) 生成其向量嵌入： u𝑖 =𝐸(𝑞 𝑖 ),v 𝑗 =𝐸(𝑑 𝑗 ), 𝑠 𝑖 𝑗 =cos(u 𝑖,v 𝑗 )。(5) 基于相似度阈值𝜏，然后计算两个覆盖比例： QP(𝑄→𝐷)= 1 𝑚 𝑚Σ︁ 𝑖=1 I max 𝑗 𝑠𝑖 𝑗 ≥𝜏 ,(6) DP(𝐷→𝑄)= 1 𝑛 𝑛Σ︁ 𝑗=1 I max 𝑖 𝑠𝑖 𝑗 ≥𝜏 ,(7) 其中 QP 测量在 𝐷 中找到紧密匹配的查询句子的比例，DP 测量 𝑄 覆盖的文档句子的比例。最终的比例相关性得分是这两个部分的乘积：𝑆RPRS (𝑄, 𝐷)=QP(𝑄→𝐷) ×DP(𝐷→𝑄)。(8) 这种句子级设计是其在 QBD 设置中有效性的关键。

### 段落 135 · Page 19

**EN**

It offers full-length coverage without truncation and is highly ANN-friendly, as document sentence embeddings can be pre-computed for scalable nearest-neighbor search. Furthermore, its reliance on coverage scoring requires low supervision, making it suitable for domains like legal search where labels are scarce. A frequency-aware variant, RPRS w/freq, extends this approach by incorporating BM25-style frequency saturation and length normalization to handle repeated matches more robustly [67]. In a modern retrieval pipeline, RPRS serves as a versatile and efficient re-ranker.

**中文**

它提供无截断的全长覆盖，并且对人工神经网络高度友好，因为可以预先计算文档句子嵌入以进行可扩展的最近邻搜索。此外，它对覆盖率评分的依赖需要较低的监督，使其适合标签稀缺的法律搜索等领域。频率感知变体 RPRS w/freq 通过结合 BM25 式频率饱和度和长度归一化来扩展此方法，以更稳健地处理重复匹配 [67]。在现代检索流程中，RPRS 充当多功能且高效的重新排序器。

### 段落 136 · Page 19

**EN**

By explicitly balancing query and document coverage, it avoids the pitfalls of methods that may over-emphasize a few salient passages while ignoring broad topical alignment. The source paper shows that while RPRS is robust, its effectiveness can be further improved by tuning its three parameters (𝑛, 𝑘1, 𝑏) on a small amount of labeled data. Future work includes adapting the method for first-stage retrieval and exploring techniques to make it parameter-free by dynamically computing its parameters.

**中文**

通过明确平衡查询和文档覆盖范围，它避免了可能过度强调一些显着段落而忽略广泛主题对齐的方法的陷阱。源论文表明，虽然 RPRS 很稳健，但通过在少量标记数据上调整其三个参数（𝑛、𝑘1、𝑏）可以进一步提高其有效性。未来的工作包括调整第一阶段检索的方法，并探索通过动态计算参数使其无参数的技术。

### 段落 137 · Page 19

**EN**

5 Datasets and Empirical Benchmarks This section summarizes representative datasets for evaluating long-document retrieval, together with evaluation protocols and benchmarking practices. We emphasize benchmarks where document length, dispersed evidence, or structure/layout are intrinsic to the task.

**中文**

5 数据集和经验基准 本节总结了用于评估长文档检索的代表性数据集，以及评估协议和基准测试实践。我们强调文档长度、分散证据或结构/布局是任务固有的基准。

### Page 20

### 段落 138 · Page 20

**EN**

20 Li et al. 5.1 Datasets TREC DL Document Ranking Track (2019–2023).The document ranking task in the TREC Deep Learning (DL) track has been evaluated annually since 2019, with two subtasks: (i) full ranking from the entire corpus and (ii) top-100 re-ranking using organizer-provided candidates. Graded relevance labels (0–3) are used for testing, and NDCG@10 is the primary metric. • MS MARCO v1 (2019–2020): The 2019 and 2020 editions used the MS MARCO v1 document collection of approximately 3.21M web documents. For training, document labels were transferred from passage labels—a document was marked relevant if it contained a relevant passage.

**中文**

20 李等人。 5.1 数据集 TREC DL 文档排名轨道（2019-2023）。自 2019 年以来，TREC 深度学习（DL）轨道中的文档排名任务每年进行一次评估，有两个子任务：（i）整个语料库的完整排名和（ii）使用组织者提供的候选者重排前 100 名。分级相关性标签 (0–3) 用于测试，NDCG@10 是主要指标。 • MS MARCO v1（2019-2020）：2019 和 2020 版使用了包含约 321 万个 Web 文档的 MS MARCO v1 文档集。对于训练，文档标签是从段落标签转移而来的——如果文档包含相关段落，则该文档被标记为相关。

### 段落 139 · Page 20

**EN**

For evaluation, however, NIST provided independent human judgments at the document level (43 topics in 2019; 45 topics in 2020). Both full ranking and top-100 re-ranking subtasks were offered. • MS MARCO v2 (2021–2023): From 2021, the track switched to the larger MS MARCO v2 corpus with about 11.9M documents. In 2021, document evaluation combined independent document judgments with labels propagated from passage annotations (57 topics). In 2022 and 2023, evaluation resources focused on building a reusable passage test set; the document task’s labels were inferred from passage judgments (76 topics in 2022; 82 topics in 2023).

**中文**

然而，对于评估，NIST 在文档级别提供了独立的人类判断（2019 年为 43 个主题；2020 年为 45 个主题）。提供了完整排名和前 100 名重排子任务。 • MS MARCO v2（2021-2023）：从2021年开始，该轨道切换到更大的MS MARCO v2语料库，包含约1190万个文档。 2021 年，文档评估将独立文档判断与从段落注释（57 个主题）传播的标签相结合。 2022年和2023年，评估资源重点建设可重复使用的通行测试集；文档任务的标签是根据段落判断推断出来的（2022 年为 76 个主题；2023 年为 82 个主题）。

### 段落 140 · Page 20

**EN**

TREC Robust04.The TREC Robust04 1 dataset is a classic benchmark in the information retrieval field, widely used in research on long document retrieval tasks [80]. This dataset originates from the TREC Robust Track 2004, with the core goal of evaluating the robustness of retrieval systems when facing difficult queries. The TREC Robust document collection is from TREC disks 4 and 5. It contains approximately 528,000 long news documents covering multiple news sources, 250 topics, and approximately 31,000 qrels. Relevance judgments in Robust04 are binary: documents are either marked as relevant (1) or non-relevant (0).

**中文**

TREC Robust04。TREC Robust04 1数据集是信息检索领域的经典基准，广泛应用于长文档检索任务的研究[80]。该数据集源自 TREC Robust Track 2004，核心目标是评估检索系统在面对困难查询时的鲁棒性。 TREC Robust 文档集合来自 TREC 磁盘 4 和 5。它包含大约 528,000 个长新闻文档，涵盖多个新闻源、250 个主题和大约 31,000 个 qrel。 Robust04 中的相关性判断是二元的：文档要么被标记为相关（1），要么被标记为不相关（0）。

### 段落 141 · Page 20

**EN**

GOV2 / Terabyte Track.Gov2 2 is a large-scale web page corpus released by TREC in 2004 and is the core dataset of the TREC Terabyte Track (2004–2006) [10]. GOV2 contains documents resulting from a crawl of .gov websites made in early 2004 and contains approximately 25 million web pages, with documents truncated to 256 kilobytes (KB), for an average document size of approximately 17.7 KB. It contains 150 queries with three level judgment: 0 (irrelevant), 1 (relevant) or 2 (very relevant). ClueWeb12.The ClueWeb12 dataset is designed to support research in information retrieval and related human language technologies.

**中文**

GOV2 / Terabyte Track.Gov2 2是TREC于2004年发布的大型网页语料库，是TREC Terabyte Track（2004-2006）的核心数据集[10]。 GOV2 包含 2004 年初对 .gov 网站进行爬网所产生的文档，包含大约 2500 万个网页，文档被截断为 256 KB，平均文档大小约为 17.7 KB。它包含 150 个查询，具有三个级别的判断：0（不相关）、1（相关）或 2（非常相关）。 ClueWeb12。ClueWeb12 数据集旨在支持信息检索和相关人类语言技术的研究。

### 段落 142 · Page 20

**EN**

It contains 733,019,372 English web pages [ 47]. The dataset is divided into segments, each containing approximately 50 million documents. These documents are HTML web pages containing noisy content such as navigation, advertisements, and templates. Long, noisy pages make it suitable for testing robustness and dispersed relevance. MQ2007/2008.The MQ2007 and MQ2008 datasets are part of the LETOR 4.0 benchmark [ 66], constructed from the GOV2 web collection of approximately 25 million documents and the TREC Million Query Tracks of 2007 and 2008.

**中文**

它包含 733,019,372 个英文网页 [47]。该数据集分为多个部分，每个部分包含大约 5000 万个文档。这些文档是包含导航、广告和模板等嘈杂内容的 HTML 网页。长而嘈杂的页面使其适合测试稳健性和分散的相关性。 MQ2007/2008。MQ2007 和 MQ20​​08 数据集是 LETOR 4.0 基准的一部分 [66]，由大约 2500 万个文档的 GOV2 Web 集合以及 2007 年和 2008 年的 TREC 百万查询轨迹构建而成。

### 段落 143 · Page 20

**EN**

MQ2007 contains around 1,700 queries with roughly 65K judged query-document pairs, while MQ2008 includes about 800 queries with 14K pairs. Each query-document pair is represented by a 46-dimensional feature vector, incorporating various retrieval signals such as BM25 scores, language model features, and link-based features. Relevance annotations are graded on three levels (0, 1, 2), and the benchmark provides 5-fold cross-validation partitions for training, validation, and testing.

**中文**

MQ2007 包含大约 1,700 个查询和大约 65K 个已判断的查询文档对，而 MQ2008 包含大约 800 个查询和 14K 个对。每个查询-文档对由 46 维特征向量表示，包含各种检索信号，例如 BM25 分数、语言模型特征和基于链接的特征。相关性注释分为三个级别（0、1、2），基准测试为训练、验证和测试提供 5 倍交叉验证分区。

### 段落 144 · Page 20

**EN**

Although originally designed for learning-to-rank research, MQ2007/2008 are also cited in the context of 1https://trec.nist.gov/data/robust/04.guidelines.html 2https://ir.dcs.gla.ac.uk/test_collections/gov2-summary.htm

**中文**

尽管最初是为学习排名研究而设计的，但 MQ2007/2008 也在 1https://trec.nist.gov/data/robust/04.guidelines.html 2https://ir.dcs.gla.ac.uk/test_collections/gov2-summary.htm 的上下文中被引用

### Page 21

### 段落 145 · Page 21

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 21 long document retrieval because they are derived from full web pages in the GOV2 corpus. The relevance judgment of query-document labels enable training and evaluation of long document IR models. MLDR.MLDR is a multilingual long document retrieval dataset based on Wikipedia, Wudao, and mC4, covering 13 typologically diverse languages [14]. It is constructed by extracting long articles from these datasets and randomly selecting paragraphs from them. GPT-3.5 is then used to generate questions based on these paragraphs.

**中文**

PLM 和 LLM Era 21 中长文档检索的调查 长文档检索，因为它们源自 GOV2 语料库中的完整网页。查询文档标签的相关性判断可以训练和评估长文档 IR 模型。 MLDR.MLDR是一个基于Wikipedia、Wudao和mC4的多语言长文档检索数据集，涵盖13种不同类型的语言[14]。它是通过从这些数据集中提取长文章并从中随机选择段落来构建的。然后使用 GPT-3.5 根据这些段落生成问题。

### 段落 146 · Page 21

**EN**

The generated questions and the extracted articles constitute the new text pairs in the dataset. It contains 41,434 training documents, 2,600 test documents, and 3,800 validation documents, with an average document length of 4,737. Domain corpora.Collections such as PubMed (biomedical articles) and MIMIC-IV (clinical records) [ 41] are rich sources for building long-context retrieval tasks; however, they are not standardized retrieval benchmarks by themselves and typically require task-specific query/label construction. 5.2 Evaluation protocols and metrics This section reviews standard IR metrics that are also widely used for LDR.

**中文**

生成的问题和提取的文章构成数据集中的新文本对。它包含 41,434 个训练文档、2,600 个测试文档和 3,800 个验证文档，平均文档长度为 4,737。领域语料库。PubMed（生物医学文章）和 MIMIC-IV（临床记录）等集合[41]是构建长上下文检索任务的丰富资源；然而，它们本身并不是标准化的检索基准，并且通常需要特定于任务的查询/标签构建。 5.2 评估协议和指标 本节回顾了也广泛用于 LDR 的标准 IR 指标。

### 段落 147 · Page 21

**EN**

We first present their definitions, followed by a summary of potential challenges and considerations specific to LDR scenarios. Let 𝑄 be the set of queries, 𝐿𝑞 ={𝑑 1, . . . , 𝑑𝑁 } the ranked list for query 𝑞, and rel𝑖 ∈ { 0, . . . , 𝐺} the (graded) relevance of𝑑 𝑖 at rank𝑖. LetI[·]be the indicator function and𝑅 𝑞 ={𝑑: rel(𝑞, 𝑑)>0}the set of relevant documents for𝑞. Precision@𝑘. P@𝑘(𝑞)= 1 𝑘 𝑘∑︁ 𝑖=1 I[rel𝑖 >0].(9) Measures the proportion of relevant documents in the top-𝑘results. Recall@𝑘. Recall@𝑘(𝑞)= Í𝑘 𝑖=1 I[rel𝑖 >0] |𝑅𝑞 | .(10) Evaluates coverage of relevant documents retrieved within the top-𝑘. Mean Reciprocal Rank (MRR).

**中文**

我们首先介绍它们的定义，然后总结针对 LDR 场景的潜在挑战和注意事项。令 𝑄 为查询集，𝐿𝑞 ={𝑑 1, .。。 , 𝑑𝑁 } 查询 𝑞 的排名列表，rel𝑖 ∈ { 0, .。。 , 𝐺} 𝑑 𝑖 在排名𝑖 的（分级）相关性。设 I[·] 为指示函数，𝑅 𝑞 ={𝑑: rel(𝑞, 𝑑)>0} 𝑞 的相关文档集。精度@𝑘。 P@𝑘(𝑞)= 1 𝑘 𝑘Σ︁ 𝑖=1 I[rel𝑖 >0]。(9) 测量相关文档在顶部𝑘结果中的比例。回想一下@𝑘。回忆@𝑘(𝑞)= Í𝑘 𝑖=1 I[rel𝑖 >0] |𝑅𝑞 | .(10) 评估在 top-𝑘 中检索到的相关文档的覆盖范围。平均倒数排名 (MRR)。

### 段落 148 · Page 21

**EN**

MRR= 1 |𝑄| ∑︁ 𝑞∈𝑄 1 rank𝑞 ,(11) whererank 𝑞 is the position of the first relevant document. Captures how early the first relevant document appears. Normalized Discounted Cumulative Gain (nDCG@𝑘). DCG@𝑘(𝑞)= 𝑘∑︁ 𝑖=1 2rel𝑖 −1 log2 (𝑖+1) ,nDCG@𝑘(𝑞)= DCG@𝑘(𝑞) IDCG@𝑘(𝑞) .(12) Accounts for graded relevance and rank position through logarithmic discounting. Mean Average Precision (MAP). AP(𝑞)= 1 |𝑅𝑞 | 𝑁∑︁ 𝑖=1 P@𝑖(𝑞) ·I[rel 𝑖 >0],MAP= 1 |𝑄| ∑︁ 𝑞 AP(𝑞).(13) Aggregates precision across recall levels to evaluate overall ranking quality. Beyond accuracy, efficiency is also critical in LDR.

**中文**

MRR= 1 |𝑄| Σ︁ 𝑞ε𝑄 1rank𝑞 ,(11) 其中rank𝑞是第一个相关文档的位置。捕获第一个相关文档出现的时间。标准化贴现累积增益 (nDCG@𝑘)。 DCG@𝑘(𝑞)= 𝑘Σ︁ 𝑖=1 2rel𝑖 −1 log2 (𝑖+1) ,nDCG@𝑘(𝑞)= DCG@𝑘(𝑞) IDCG@𝑘(𝑞) .(12) 通过对数贴现计算分级相关性和排名位置。平均精度 (MAP)。 AP(𝑞)= 1 |𝑅𝑞 | 𝑁Σ︁ 𝑖=1 P@𝑖(𝑞) ·I[rel 𝑖 >0],MAP= 1 |𝑄| Σ︁ 𝑞 AP(𝑞).(13) 聚合各个召回级别的精确度以评估总体排名质量。除了准确性之外，效率对于 LDR 也至关重要。

### 段落 149 · Page 21

**EN**

Measures include end-to-end latency (per query), index size and GPU usage. These factors determine practical deployability and comparability across methods.

**中文**

衡量指标包括端到端延迟（每个查询）、索引大小和 GPU 使用情况。这些因素决定了方法之间的实际可部署性和可比性。

### Page 22

### 段落 150 · Page 22

**EN**

22 Li et al. Discussion.Traditional IR metrics remain the foundation of evaluation in LDR, but several characteristics of long documents complicate their interpretation. First, judgments are typically applied at the document level, which obscures finer distinctions such as “partially relevant” or “locally relevant” segments. Second, relevance evidence can be dispersed across different sections, while these metrics only consider whether the document as a whole is relevant. Third, coarse relevance scales are often insufficient to reflect nuanced utility in long documents.

**中文**

22 李等人。讨论。传统的 IR 指标仍然是 LDR 评估的基础，但长文档的几个特征使它们的解释变得复杂。首先，判断通常应用于文档级别，这模糊了更精细的区别，例如“部分相关”或“局部相关”片段。其次，相关性证据可以分散在不同的部分，而这些指标只考虑整个文档是否相关。第三，粗略的相关性尺度通常不足以反映长文档中细致入微的实用性。

### 段落 151 · Page 22

**EN**

Future work may extend metrics to incorporate evidence localization and finer-grained relevance levels. 6 Applications and Use Cases This chapter delves into the applications of LDR across various fields and the core challenges it faces. We begin by reviewing the progress of LDR technologies and, based on this foundation, analyze their specific applications in different domains, particularly highlighting their significance in law, academia, and life sciences. In addition, we explore the challenges that LDR encounters, such as efficiency bottlenecks, domain adaptability, and cross-modal retrieval issues.

**中文**

未来的工作可能会扩展指标以纳入证据本地化和更细粒度的相关性级别。 6 应用与用例 本章深入探讨了LDR在各个领域的应用及其面临的核心挑战。我们首先回顾LDR技术的进展，并在此基础上分析其在不同领域的具体应用，特别强调其在法律、学术界和生命科学领域的意义。此外，我们还探讨了 LDR 遇到的挑战，例如效率瓶颈、领域适应性和跨模态检索问题。

### 段落 152 · Page 22

**EN**

Through Figure 6, we present a schematic representation of LDR technologies applied across different fields, providing a clear framework for understanding how various tasks leverage LDR methods. Each domain in the figure corresponds to distinct technical requirements and solutions, such as long-document-based legal retrieval, academic paper retrieval, and cross-lingual retrieval. As LDR technologies continue to evolve, these applications demonstrate varying challenges and breakthroughs in practical implementation, especially when dealing with complex, structured documents and multimodal information retrieval. Fig. 6.

**中文**

通过图 6，我们展示了应用于不同领域的 LDR 技术的示意图，为理解各种任务如何利用 LDR 方法提供了清晰的框架。图中的每个领域都对应着不同的技术需求和解决方案，例如基于长文档的法律检索、学术论文检索、跨语言检索等。随着 LDR 技术的不断发展，这些应用程序在实际实施中表现出不同的挑战和突破，特别是在处理复杂的结构化文档和多模式信息检索时。图 6.

### 段落 153 · Page 22

**EN**

The applications of Long-Document Retrieval 6.1 Legal Retrieval Traditional keyword-based retrieval methods are rendered ineffective by the high specialisation, complex hierarchical structures, and extensive texts that characterise legal long-document retrieval. For instance, cross-version and cross-level

**中文**

6. 长文档检索的应用 6.1 法律检索 法律长文档检索专业性强、层次结构复杂、文本量大，传统的基于关键词的检索方法效率低下。比如跨版本、跨级别

### Page 23

### 段落 154 · Page 23

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 23 mappings of provisions are frequently employed in judicial documents, legal provisions, and legal interpretations. The retrieval system must not only comprehend the rigors logic of legal language but also facilitate cross-document reasoning and query explainability. The system must distinguish between the consistency of legal principles and the similarity of case facts in case retrieval. Legal comparison necessitates the precise matching of changes in provisions across new and old versions.

**中文**

PLM 和 LLM 时代长文档检索调查 23 条文映射经常用于司法文件、法律条文和法律解释中。检索系统不仅必须理解法律语言的严格逻辑，还要促进跨文档推理和查询可解释性。系统在案件检索中必须区分法律原则的一致性和案件事实的相似性。法律比较需要准确匹配新旧版本的条款变化。

### 段落 155 · Page 23

**EN**

Comprehensive legal research necessitates the integration of case law, regulations, academic commentary, and judicial interpretations, resulting in a logically coherent chain of evidence. The research community has created a series of retrieval models that are specifically designed to address the characteristics of legal texts in order to overcome these challenges. Lawformer[ 86], which is constructed on the Longformer[8] architecture, integrates global attention mechanisms with local sliding windows.

**中文**

全面的法律研究需要将判例、法规、学术评论和司法解释结合起来，形成逻辑上连贯的证据链。研究界创建了一系列专门针对法律文本特征的检索模型，以克服这些挑战。 Lawformer[86]是在Longformer[8]架构上构建的，将全局注意力机制与局部滑动窗口相结合。

### 段落 156 · Page 23

**EN**

This allows it to effectively manage judgement documents containing thousands of tokens and excel in legal question answering and case retrieval tasks . Another model, Legal-BigBird[23], adapts the long-range Transformer model BigBird for legal document processing. It leverages BigBird’s ability to handle long sequences with reduced computational costs, making it well-suited for the extensive length of legal texts. By further training BigBird on legal corpora, Legal-BigBird improves the representation of legal documents, enhancing its performance in tasks such as legal case retrieval.

**中文**

这使得它能够有效管理包含数千个标记的判决文件，并在法律问答和案件检索任务中表现出色。另一个模型 Legal-BigBird[23] 采用远程 Transformer 模型 BigBird 进行法律文档处理。它利用 BigBird 处理长序列的能力，同时降低计算成本，使其非常适合大长度的法律文本。通过进一步在法律语料库上训练 BigBird，Legal-BigBird 改善了法律文档的表示，提高了其在法律案例检索等任务中的性能。

### 段落 157 · Page 23

**EN**

Furthermore, LawGPT[96] is pretrained on a substantial corpus of legal literature, which includes legal judgements, regulations, and academic articles, in order to effectively convey the intricate logical relationships and profound semantics that are inherent in legal texts. LawGPT is capable of rapidly extracting pertinent information from lengthy legal documents during cross-document reasoning, thereby facilitating legal deduction and cross-document reasoning.

**中文**

此外，LawGPT[96]是在大量法律文献语料库上进行预训练的，其中包括法律判决、法规和学术文章，以有效传达法律文本固有的复杂逻辑关系和深刻语义。 LawGPT能够在跨文档推理时从冗长的法律文档中快速提取相关信息，从而方便法律推演和跨文档推理。

### 段落 158 · Page 23

**EN**

In conclusion, in order to effectively analyse intricate legal provisions, judicial rulings, and regulatory interpretations, legal lengthy document retrieval systems must possess a profound comprehension of the structure and semantics of legal documents. Secondly, the system must have the ability to integrate information from various sources in order to create a comprehensive legal evidence chain, which necessitates strong cross-document reasoning capabilities.

**中文**

总之，为了有效地分析错综复杂的法律条文、司法判决和监管解释，法律长篇文献检索系统必须对法律文献的结构和语义有深刻的理解。其次，系统必须具备整合多方信息的能力，形成完整的法律证据链，这就需要强大的跨文档推理能力。

### 段落 159 · Page 23

**EN**

Lastly, the system should improve its cross-lingual adaptability and explainability to guarantee its effective application in a variety of legal environments worldwide, thereby satisfying the requirements of judicial and legal research in various countries. 6.2 Scholarly Long-Document Retrieval Scholarly articles are long and multi-faceted (research questions, methods, datasets, results), so relevant evidence is dispersed across distant sections and easily diluted by length.

**中文**

最后，提高系统的跨语言适应性和可解释性，保证其在全球多种法律环境中的有效应用，满足各国司法和法律研究的需要。 6.2 学术性长文献检索 学术性文章篇幅较长且涉及多个方面（研究问题、方法、数据集、结果），因此相关证据分散在相距较远的部分，并且很容易因长度而被稀释。

### 段落 160 · Page 23

**EN**

Queries are often themselves long (e.g., paper-to-paper search), requiring decomposition into facet-specific intents and span-grounded verification to maintain provenance. Citation graphs additionally shape relatedness, making it necessary to reason over long-range, multi-hop links rather than purely local lexical overlap.

**中文**

查询本身通常很长（例如，纸到纸搜索），需要分解为特定方面的意图和基于跨度的验证以维护出处。引文图还塑造了相关性，使得有必要对远程、多跳链接进行推理，而不是纯粹的局部词汇重叠。

### 段落 161 · Page 23

**EN**

Citation- and concept-aware encoders provide high-recall seeds and stable geometry for long-corpus search: SciBERT supplies scientific-domain pretraining model for passage encodings [7]; SPECTER injects citation signals via triplet training (query paper, cited positive, uncited/hard-negative) to yield document embeddings aligned with scholarly relatedness, which is well-suited for document-level initial retrieval refined at passage level [ 17]; SciNCL replaces discrete “cited/not” labels with neighborhood-contrastive sampling over a citation-graph embedding, improving global geometry for paper-to-paper search [60].

**中文**

引文和概念感知编码器为长语料库搜索提供高召回率种子和稳定的几何结构：SciBERT 为段落编码提供科学领域预训练模型 [7]； SPECTRE 通过三元组训练（查询论文、引用正面、未引用/硬负面）注入引用信号，以产生与学术相关性一致的文档嵌入，这非常适合在段落级别细化的文档级初始检索[17]； SciNCL 用引文图嵌入上的邻域对比采样取代了离散的“被引用/未引用”标签，改进了纸到纸搜索的全局几何结构[60]。

### 段落 162 · Page 23

**EN**

Concept-indexed and aspect-aware retrieval narrows drift: SemRank builds a multi-granular concept index (topics + key phrases) per paper and uses LLM-guided concept selection at query time to match first at the concept layer before

**中文**

概念索引和方面感知检索缩小了偏差：SemRank 为每篇论文构建多粒度概念索引（主题 + 关键短语），并在查询时使用 LLM 引导的概念选择来首先在概念层进行匹配

### Page 24

### 段落 163 · Page 24

**EN**

24 Li et al. verifying at passage level [94]; PRISM decomposes a query paper into motivation/method/experiments subqueries, retrieves over a multi-vector corpus of 3k-token chunks, and fuses rankings (RRF) to operationalize “whole-document yet facet-specific” matching [65]. To control cost on long texts, CORANK extracts zero-shot LLM features (categories/sections/keywords) to rerank large candidate pools, then applies full-text reranking only to the top-𝑀 candidates, preserving LDR coverage while reducing token and latency budgets [79].

**中文**

24 李等人。在通过级别进行验证[94]； PRISM 将查询论文分解为动机/方法/实验子查询，检索 3k-token 块的多向量语料库，并融合排名 (RRF) 以操作“整个文档但特定于方面”匹配 [65]。为了控制长文本的成本，CORANK 提取零样本 LLM 特征（类别/部分/关键字）来对大型候选池进行重排，然后仅对顶级候选者应用全文重排，保留 LDR 覆盖范围，同时减少令牌和延迟预算 [79]。

### 段落 164 · Page 24

**EN**

LLM-enhanced systems further tighten grounding and recall: PaperQA retrieves full texts, scores chunks with LLMbased relevance, and synthesizes answers with citations to curb hallucinations [57]; DocReLM trains retrievers/rerankers with LLM-generated pseudo-queries and traverses citation networks to gather supporting references [83]; ensemble strategies such as LLM-KnowSimFuser fuse similarities from multiple LLM-enhanced embedder families with a LoRAtuned academic encoder to stabilize ranking [20].

**中文**

LLM 增强的系统进一步加强了基础和回忆：PaperQA 检索全文，对基于 LLM 的相关性进行评分，并通过引用合成答案以抑制幻觉 [57]； DocReLM 使用 LLM 生成的伪查询训练检索器/重新排序器，并遍历引文网络以收集支持参考文献 [83]； LLM-KnowSimFuser 等集成策略将多个 LLM 增强型嵌入器系列的相似性与 LoRAtuned 学术编码器融合在一起，以稳定排名 [20]。

### 段落 165 · Page 24

**EN**

Multi-agent designs (e.g., PaSa, SPAR) modularize query understanding, citation-graph expansion, and reranking, harvesting long-range, multi-hop evidence while keeping verification passage-grounded [34, 73]. In general, LDR for scholarly papers tames length by (i) abstracting queries to concepts/aspects to steer recall, (ii) leveraging citation graphs for long-range candidate proposals, and (iii) delaying full-text interaction to a narrow shortlist while enforcing span-level attribution to preserve provenance.

**中文**

多智能体设计（例如 PaSa、SPAR）模块化查询理解、引文图扩展和重排，收获远程、多跳证据，同时保持验证段落的基础 [34, 73]。一般来说，学术论文的 LDR 通过以下方式来控制长度：(i) 将查询抽象为概念/方面以引导回忆，(ii) 利用长期候选提案的引用图，以及 (iii) 将全文交互延迟到狭窄的候选列表，同时强制执行跨级别归因以保留出处。

### 段落 166 · Page 24

**EN**

6.3 Biomedical Literature Search High demands for multimodal fusion, strong knowledge interdependencies, and heterogeneous data structures characterise biomedical extended document retrieval, presenting unique challenges. The biomedical field’s precise requirements are not satisfactorily addressed by conventional keyword-based retrieval methods. For instance, medical literature, electronic health records (EHR), and genetic reports require cross-disciplinary information mapping. This mapping must allow systems to interpret specialised terminology, support cross-modal reasoning, and result in traceability.

**中文**

6.3 生物医学文献检索 生物医学扩展文档检索的特点是对多模态融合的高要求、强知识相互依赖性和异构数据结构，带来了独特的挑战。传统的基于关键词的检索方法并不能很好地满足生物医学领域的精确要求。例如，医学文献、电子健康记录 (EHR) 和基因报告需要跨学科的信息映射。这种映射必须允许系统解释专业术语、支持跨模式推理并实现可追溯性。

### 段落 167 · Page 24

**EN**

Disease diagnosis support necessitates the integration of electronic health records (EHRs) with clinical guidelines, while clinical trial retrieval must align with trial designs, efficacy indicators, and patient characteristics. The integration of target literature, experimental data, and adverse reaction reports is necessary for drug repurposing . To address the challenges of long clinical sequence processing, the research community has developed several models specifically designed for long-text retrieval. By optimizing the Transformer model, Clinical-Longformer and Clinical-BigBird[54] can process clinical texts with up to 4096 tokens.

**中文**

疾病诊断支持需要将电子健康记录 (EHR) 与临床指南相结合，而临床试验检索必须与试验设计、疗效指标和患者特征保持一致。目标文献、实验数据和不良反应报告的整合对于药物再利用是必要的。为了解决长临床序列处理的挑战，研究界开发了几种专门为长文本检索设计的模型。通过优化 Transformer 模型，Clinical-Longformer 和 Clinical-BigBird[54] 可以处理最多 4096 个标记的临床文本。

### 段落 168 · Page 24

**EN**

They adopt sparse attention mechanisms, which effectively reduce memory consumption and enable the processing of long texts without compromising performance. Meanwhile, they also excel at capturing long-range dependencies, making them perform exceptionally well in long-text retrieval tasks—particularly in clinical domain tasks such as question answering and document classification. These models can understand and retrieve complete clinical records in a single processing step, without splitting information into multiple segments, thus avoiding the issues of information loss or context fragmentation.

**中文**

它们采用稀疏注意力机制，有效减少内存消耗，并能够在不影响性能的情况下处理长文本。同时，它们还擅长捕获远程依赖性，使它们在长文本检索任务中表现得异常出色，尤其是在问答和文档分类等临床领域任务中。这些模型可以在单个处理步骤中理解和检索完整的临床记录，而无需将信息拆分为多个片段，从而避免信息丢失或上下文碎片的问题。

### 段落 169 · Page 24

**EN**

Additionally, BioClinical ModernBERT[74], a domain-adapted encoder based on ModernBERT, also supports the needs of long-text retrieval and can handle longer contextual information. By integrating biomedical and clinical corpora, it not only significantly improves retrieval efficiency but also addresses the catastrophic forgetting problem commonly encountered in long-text processing. When processing large-scale patient health records, BioClinical ModernBERT can maintain the coherence and integrity of information, and it has demonstrated outstanding performance especially in tasks such as phenotype classification and clinical decision support.

**中文**

此外，基于ModernBERT的领域自适应编码器BioClinical ModernBERT[74]也支持长文本检索的需求，可以处理更长的上下文信息。通过整合生物医学和临床语料库，它不仅显着提高了检索效率，还解决了长文本处理中常见的灾难性遗忘问题。在处理大规模患者健康记录时，BioClinical ModernBERT 可以保持信息的连贯性和完整性，尤其在表型分类和临床决策支持等任务中表现出了出色的性能。

### Page 25

### 段落 170 · Page 25

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 25 Biomedical long-document retrieval relies on multimodal fusion and deep semantic understanding when processing massive and complex data. With the continuous advancement of model technologies, a range of advanced biomedical retrieval models have significantly enhanced their ability to process biomedical long-document by incorporating optimized attention mechanisms and deep learning approaches.

**中文**

PLM 和 LLM 时代长文档检索综述 25 生物医学长文档检索在处理海量复杂数据时依赖于多模态融合和深度语义理解。随着模型技术的不断进步，一系列先进的生物医学检索模型通过结合优化的注意力机制和深度学习方法，显着增强了其处理生物医学长文档的能力。

### 段落 171 · Page 25

**EN**

The development of these technologies has not only promoted the accuracy and efficiency of literature retrieval but also provided crucial technical support for fields such as clinical decision-making and disease prediction. In the future, with the further expansion of data scale and continuous technological innovation, biomedical long-document retrieval will face more challenges and opportunities. 6.4 Cross-Lingual Long-Text Retrieval Cross-lingual information retrieval is particularly challenging when evidence resides in long documents such as encyclopedic articles or legal texts.

**中文**

这些技术的发展不仅提升了文献检索的准确性和效率，也为临床决策、疾病预测等领域提供了关键的技术支撑。未来，随着数据规模的进一步扩大和技术的不断创新，生物医学长文档检索将面临更多的挑战和机遇。 6.4 跨语言长文本检索 当证据存在于百科全书文章或法律文本等长文档中时，跨语言信息检索尤其具有挑战性。

### 段落 172 · Page 25

**EN**

Systems must simultaneously align semantics across languages and handle lengthy, structured content where relevant evidence is scattered. A representative benchmark is XOR-QA[3], which decouples the query language from the evidence language (e.g., a Japanese query with only English evidence). Since Wikipedia articles are long and multi-sectioned, models must not only retrieve passages across languages but also aggregate them for provenance-aware answers. Building on this benchmark, McCrolin[55] introduces a multi-consistency training framework with a teacher-student setup (frozen mUSE as teacher).

**中文**

系统必须同时协调跨语言的语义，并处理相关证据分散的冗长、结构化内容。一个代表性的基准是 XOR-QA[3]，它将查询语言与证据语言解耦（例如，仅包含英语证据的日语查询）。由于维基百科文章很长且由多个部分组成，因此模型不仅必须检索跨语言的段落，而且还必须将它们聚合起来以获得来源感知的答案。在此基准的基础上，McCrolin[55] 引入了一个具有师生设置的多一致性训练框架（冻结 mUSE 作为教师）。

### 段落 173 · Page 25

**EN**

It enforces cross-lingual semantic consistency and stable ranking via tailored loss functions, showing strong results on long-document retrieval across different encoders. Beyond XOR-QA–based research, mGTE[93] develops a long-context multilingual encoder (up to 8k tokens) with Rotary Position Embedding, unpadding, and two-stage pre-training, further enhanced by hybrid dense–sparse representations and a reranker to balance efficiency and accuracy.

**中文**

它通过定制的损失函数强制执行跨语言语义一致性和稳定排名，在跨不同编码器的长文档检索上显示出强大的结果。除了基于 XOR-QA 的研究之外，mGTE[93] 还开发了一种长上下文多语言编码器（最多 8k 个标记），具有旋转位置嵌入、去填充和两阶段预训练，并通过混合稠密-稀疏表示和重排序器进一步增强，以平衡效率和准确性。

### 段落 174 · Page 25

**EN**

CROSS[59] targets ultra-long texts (up to 512k tokens) through a two-phase process: sentence-level retrieval with multilingual embeddings followed by selective reasoning with LLMs (e.g., GPT-4o-mini, Llama 3.2), effectively mitigating the “lost-in-the-middle” problem. Although differing in architecture, context length, and optimization strategy, these approaches converge on the core pain points of cross-lingual long-text retrieval: semantic alignment, scattered evidence, and computational efficiency, while offering complementary solutions for cross-lingual long-context scenarios.

**中文**

CROSS[59]通过两阶段过程针对超长文本（最多 512k 个标记）：使用多语言嵌入进行句子级检索，然后使用 LLM（例如 GPT-4o-mini、Llama 3.2）进行选择性推理，有效缓解“中间丢失”问题。尽管在架构、上下文长度和优化策略上有所不同，但这些方法都集中在跨语言长文本检索的核心痛点上：语义对齐、分散的证据和计算效率，同时为跨语言长上下文场景提供了补充解决方案。

### 段落 175 · Page 25

**EN**

6.5 Other Applications In addition to specialized fields such as legal, medical, and academic retrieval, long-document retrieval (LDR) has found widespread applications across various other domains. These applications have been driven by the explosive growth of digital content and the increasing complexity of information structures. As the scope of LDR continues to expand, it becomes crucial to explore how these retrieval systems adapt to broader and more complex domains.

**中文**

6.5 其他应用 除了法律、医学和学术检索等专业领域外，长文档检索（LDR）在其他各个领域也得到了广泛的应用。这些应用是由数字内容的爆炸性增长和信息结构日益复杂性推动的。随着 LDR 范围的不断扩大，探索这些检索系统如何适应更广泛、更复杂的领域变得至关重要。

### 段落 176 · Page 25

**EN**

This section will examine these emerging applications, focusing on the unique challenges they present and the customized solutions developed to enhance retrieval performance. 6.5.1 Web and News Retrieval.With the explosive growth of digital content, long-document retrieval technology has shown great potential in the fields of web search and news retrieval. As information sources become increasingly diverse and content updates accelerate, traditional retrieval methods face unprecedented challenges.

**中文**

本节将研究这些新兴应用程序，重点关注它们带来的独特挑战以及为增强检索性能而开发的定制解决方案。 6.5.1 网络和新闻检索。随着数字内容的爆炸式增长，长文档检索技术在网络搜索和新闻检索领域显示出巨大的潜力。随着信息来源的日益多样化和内容更新的加快，传统的检索方法面临着前所未有的挑战。

### 段落 177 · Page 25

**EN**

To address this issue, researchers have proposed multi-document retrieval tasks aimed at extracting relevant information sources from vast amounts of news articles to support efficient query execution. This task specifically emphasizes the high demands placed on retrieval systems due to the broadness of information and the diversity of sources in news reporting[75].

**中文**

为了解决这个问题，研究人员提出了多文档检索任务，旨在从大量新闻文章中提取相关信息源，以支持高效的查询执行。这项任务特别强调了由于新闻报道中信息的广泛性和来源的多样性而对检索系统提出的高要求[75]。

### Page 26

### 段落 178 · Page 26

**EN**

26 Li et al. The introduction of long-document retrieval technology enables efficient extraction of key data from lengthy news articles, blogs, and multimedia reports, and allows for real-time tracking of event developments, improving the speed and accuracy of information retrieval. 6.5.2 Multimedia and Interactive Document Processing.Modern long-document retrieval must increasingly contend with multimedia content, where meaning is conveyed through a complex interplay of text, layout, images, and tables. This has spurred the development of multimodal architectures and, critically, new evaluation frameworks to benchmark them.

**中文**

26 李等人。引入长文档检索技术，可以从长篇新闻、博客、多媒体报道中高效提取关键数据，实时跟踪事件发展，提高信息检索的速度和准确性。 6.5.2 多媒体和交互式文档处理。现代长文档检索必须越来越多地应对多媒体内容，其中意义是通过文本、布局、图像和表格的复杂相互作用来传达的。这刺激了多模式架构的发展，更重要的是，刺激了新的评估框架来对其进行基准测试。

### 段落 179 · Page 26

**EN**

A key example is the MMDocIR benchmark [26], which introduces page- and layout-level retrieval tasks specifically designed to assess performance on visually rich documents. The emergence of such dedicated benchmarks signifies a critical shift, pushing the field beyond text-centric models toward systems capable of genuine cross-modal reasoning and information fusion. M3DocRAG [16] uses a multimodal retriever and MLM to find relevant documents and answer questions, allowing it to efficiently process single or multiple documents while preserving visual information.

**中文**

一个重要的例子是 MMDocIR 基准测试 [26]，它引入了页面和布局级别的检索任务，专门用于评估视觉丰富的文档的性能。这种专用基准的出现标志着一个关键的转变，推动该领域超越以文本为中心的模型，转向能够真正跨模态推理和信息融合的系统。 M3DocRAG [16] 使用多模式检索器和 MLM 来查找相关文档并回答问题，使其能够有效地处理单个或多个文档，同时保留视觉信息。

### 段落 180 · Page 26

**EN**

6.5.3 Enterprise Knowledge Management.In the field of Enterprise Knowledge Management (EKM), as the volume of internal documents within companies continues to increase, traditional retrieval methods are increasingly inadequate to meet the need for efficient information retrieval. Research has shown that deep learning techniques demonstrate significant advantages in enterprise knowledge retrieval, effectively handling complex cross-domain knowledge retrieval tasks.

**中文**

6.5.3企业知识管理。在企业知识管理（EKM）领域，随着企业内部文档量的不断增加，传统的检索方法越来越不能满足高效信息检索的需要。研究表明，深度学习技术在企业知识检索方面表现出显着的优势，能够有效处理复杂的跨领域知识检索任务。

### 段落 181 · Page 26

**EN**

With the generation and storage of large volumes of documents within organizations, long-document retrieval technology not only helps employees quickly find the most relevant information but also provides strong support in decision-making processes, thereby improving work efficiency. For example, the eSapiens system [72] combines a text-to-SQL planner with a hybrid Retrieval Augmented Generation (RAG) pipeline to support natural language access to both structured databases and unstructured text, further enhancing the accuracy and consistency of enterprise knowledge retrieval.

**中文**

随着组织内部大量文档的生成和存储，长文档检索技术不仅可以帮助员工快速找到最相关的信息，而且可以为决策过程提供强有力的支持，从而提高工作效率。例如，eSapiens系统[72]将文本到SQL规划器与混合检索增强生成（RAG）管道相结合，支持自然语言访问结构化数据库和非结构化文本，进一步提高企业知识检索的准确性和一致性。

### 段落 182 · Page 26

**EN**

7 Current Challenges and Future Directions Despite substantial progress, long-document retrieval (LDR) remains an open and rapidly evolving research frontier. Below we summarize critical challenges and outline promising research directions. 7.1 Key Challenges (1) Efficient Scaling.Even with long-context PLMs/LLMs (e.g., 32K–100K windows), end-to-end processing of full documents remains expensive. Sparse/kernelized attention, chunking, and compression reduce cost but can attenuate fine-grained matching signals that matter for retrieval and QA.

**中文**

7 当前的挑战和未来的方向 尽管取得了重大进展，长文档检索 (LDR) 仍然是一个开放且快速发展的研究前沿。下面我们总结了关键挑战并概述了有前途的研究方向。 7.1 主要挑战 (1) 高效扩展。即使使用长上下文 PLM/LLM（例如 32K–100K 窗口），完整文档的端到端处理仍然昂贵。稀疏/核化注意力、分块和压缩可以降低成本，但会削弱对检索和质量保证很重要的细粒度匹配信号。

### 段落 183 · Page 26

**EN**

A core challenge is to design architectures and indexing schemes that scale sub-linearly in document length while preserving retrieval fidelity. Systematic “scaling laws” for accuracy–cost trade-offs at extreme context lengths are still underexplored. (2) Relevance Localization and Multi-Granularity.Long documents interleave relevant and irrelevant content. Retrievers must localize small yet critical spans and synthesize document-level evidence.

**中文**

核心挑战是设计架构和索引方案，在保持检索保真度的同时，以次线性方式扩展文档长度。极端上下文长度下的准确性成本权衡的系统性“缩放法则”仍未得到充分探索。 (2)相关性本地化和多粒度。长文档中相关内容和不相关内容交织在一起。检索人员必须定位小但关键的跨度并综合文档级证据。

### 段落 184 · Page 26

**EN**

Existing block/segment selection (e.g., KeyB/KeyB2, hierarchical selectors, LLM-guided in-context selection) alleviates cost but can suffer from query drift, redundancy, or broken cross-block reasoning. Discourse- and structure-aware retrieval that respects document organization (sections, tables, figures, citations) remains limited. (3) Data Scarcity.High-quality document-level supervision is costly, making fully supervised learning difficult. Synthetic/weak supervision helps, but is often sentence-level and lacks document- or paragraph-granularity alignment.

**中文**

现有的块/段选择（例如，KeyB/KeyB2、分层选择器、LLM 引导的上下文选择）可降低成本，但可能会遭受查询漂移、冗余或损坏的跨块推理的影响。尊重文档组织（章节、表格、图表、引文）的话语和结构感知检索仍然有限。 (3)数据稀缺。高质量的文档级监督成本高昂，使得完全监督学习变得困难。综合/弱监督有所帮助，但通常是句子级别的，并且缺乏文档或段落粒度的​​对齐。

### Page 27

### 段落 185 · Page 27

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 27 Leveraging cross-task signals (summarization, QA, citation linking) or implicit interaction signals is a promising route to richer supervision at document scale. (4) Domain and Language Adaptation.Specialized domains (legal, biomedical, scholarly) and multilingual LDR introduce domain-specific structures and terminology. Transfer from English-centric datasets remains challenging (e.g., MLDR-zh). Structured artifacts, e.g., clause numbering, formulas, tables, layouts are seldom integrated into retrieval models, limiting cross-domain generalization.

**中文**

PLM 和 LLM 时代的长文档检索调查 27 利用跨任务信号（摘要、QA、引文链接）或隐式交互信号是在文档规模上实现更丰富监督的一条有前途的途径。 (4) 领域和语言适应。专业领域（法律、生物医学、学术）和多语言 LDR 引入了特定领域的结构和术语。从以英语为中心的数据集进行传输仍然具有挑战性（例如 MLDR-zh）。结构化工件，例如子句编号、公式、表格、布局很少集成到检索模型中，限制了跨域泛化。

### 段落 186 · Page 27

**EN**

(5) Interpretability and User Trust.Users need to understand why a long document is retrieved. Current neural/LLM models offer weak attribution: attention maps or post-hoc highlights may not reflect actual decision signals, and hallucination risks grow when models summarize long evidence. Span-level rationales, attribution-aware training, and user-centered evaluation protocols are urgently needed. 7.2 Future Directions Unified Retrieval–Reading Models.LLMs increasingly blur the retrieval–reasoning boundary by consuming long contexts.

**中文**

(5)可解释性和用户信任。用户需要理解为什么长文档被检索。当前的神经/法学硕士模型提供的归因较弱：注意力图或事后亮点可能无法反映实际的决策信号，并且当模型总结长期证据时，幻觉风险会增加。迫切需要跨度的基本原理、归因意识培训和以用户为中心的评估协议。 7.2 未来方向统一检索-阅读模型。法学硕士通过消耗长上下文越来越模糊检索-推理边界。

### 段落 187 · Page 27

**EN**

Jointly optimizing retrieval and reading, aided by context compression (e.g., LongLLMLingua [39]), selective pruning [53], and abstraction prompts, is promising. Open questions include when retrieval-free pipelines suffice, and how to characterize their cost–benefit at corpus scale. Advances in Long-Context Architectures.Progress in efficient attention (sparse/kernelized/chunked), improved positional schemes (e.g., RoPE variants [76]), and external memory [85] suggests hybrid designs that combine local/global attention with hierarchical representations.

**中文**

在上下文压缩（例如 LongLLMLingua [39]）、选择性修剪 [53] 和抽象提示的帮助下，联合优化检索和阅读是有希望的。悬而未决的问题包括免检索管道何时足够，以及如何在语料库规模上描述其成本效益。长上下文架构的进展。高效注意力（稀疏/核化/分块）、改进的位置方案（例如，RoPE 变体[76]）和外部记忆[85]方面的进展表明将局部/全局注意力与分层表示相结合的混合设计。

### 段落 188 · Page 27

**EN**

Structured or episodic memory that bridges symbolic storage (graphs, tables, layouts) and neural context modeling is a natural next step beyond 100K tokens. Retrieval-Enhanced LLMs.RAG for long documents remains under-engineered. Beyond plug-and-play retrieval, systems should support iterative retrieval-generation cycles [70], query refinement, and adaptive granularity (document/section/passage). Tighter integration of retrieval signals into LLM reasoning, e.g., retrieval-conditioned decoding, retrieval-aware training, may improve faithfulness and efficiency.

**中文**

连接符号存储（图形、表格、布局）和神经上下文建模的结构化或情景记忆是超越 100K 令牌的自然下一步。针对长文档的检索增强型 LLMs.RAG 仍然没有得到充分设计。除了即插即用检索之外，系统还应该支持迭代检索生成周期[70]、查询细化和自适应粒度（文档/部分/段落）。将检索信号更紧密地集成到法学硕士推理中，例如检索条件解码、检索感知训练，可以提高忠实度和效率。

### 段落 189 · Page 27

**EN**

Benchmarking and Evaluation.Conventional metrics (nDCG, Recall) overlook long-context issues such as attribution, multi-hop reasoning, and user effort. Many benchmarks emphasize short passages or moderate-length articles rather than truly long artifacts (patents, legal codes, books). Future resources should combine span-level and document-level annotations, include task-aware metrics (correctness vs. faithfulness), and report user-centric measures (e.g., time-to-answer, cognitive load) alongside latency and throughput.

**中文**

基准测试和评估。传统指标（nDCG、召回率）忽略了长上下文问题，例如归因、多跳推理和用户努力。许多基准强调短文或中等长度的文章，而不是真正长的工件（专利、法律法规、书籍）。未来的资源应该结合跨度级别和文档级别注释，包括任务感知指标（正确性与忠实度），并报告以用户为中心的衡量标准（例如，回答时间、认知负荷）以及延迟和吞吐量。

### 段落 190 · Page 27

**EN**

Cross-pollination and Multimodality.Insights from summarization, discourse parsing, and knowledge graphs can inspire structure-aware indexing. Many long documents are multimodal; aligning tables, figures, and text for joint indexing and retrieval remains open. Benchmarks such as VideoWebArena [ 38] expose large gaps to human performance; integrating layout modeling (e.g., LayoutLM-style features) and multimodal reasoning is a key avenue. 7.3 Summary LDR sits at the intersection of IR efficiency, document understanding, and LLM reasoning.

**中文**

异花授粉和多模态。来自摘要、话语解析和知识图的见解可以激发结构感知索引。许多长文档都是多模式的；对齐表格、图形和文本以进行联合索引和检索仍然处于开放状态。 VideoWebArena [38] 等基准测试暴露了人类表现的巨大差距；集成布局建模（例如 LayoutLM 风格的特征）和多模态推理是一个关键途径。 7.3 总结 LDR 位于 IR 效率、文档理解和 LLM 推理的交叉点。

### 段落 191 · Page 27

**EN**

No single paradigm suffices: progress will hinge on hybrid solutions that combine sub-linear indexing, structure-aware modeling, and LLM-based reasoning with robustness, interpretability, and domain generalization. Equally important are realistic long-document benchmarks and user-centered evaluation to ensure LDR systems are trustworthy and deployable.

**中文**

单一范例是不够的：进步将取决于混合解决方案，将次线性索引、结构感知建模和基于 LLM 的推理与鲁棒性、可解释性和领域泛化相结合。同样重要的是现实的长文档基准和以用户为中心的评估，以确保 LDR 系统值得信赖和可部署。

### Page 28

### 段落 192 · Page 28

**EN**

28 Li et al. 8 Conclusion Long-Document Retrieval remains a fundamental yet unresolved problem in information retrieval, where the central challenge is to balance computational efficiency with the ability to accurately locate sparse but critical signals within lengthy contexts. Through this survey, we traced the evolution of the field from classical lexical approaches to neural architectures, and further to the recent integration of large language models.

**中文**

28 李等人。 8 结论 长文档检索仍然是信息检索中尚未解决的基本问题，其中的核心挑战是平衡计算效率与在冗长上下文中准确定位稀疏但关键信号的能力。通过这项调查，我们追踪了该领域从经典词汇方法到神经架构的演变，并进一步到最近大型语言模型的集成。

### 段落 193 · Page 28

**EN**

We synthesized existing methods into four complementary paradigms: Holistic modeling of entire documents, Divideand-Conquer strategies that segment and re-aggregate evidence, Indexing-Structure innovations that exploit document organization, and specialized approaches for long-query retrieval. This taxonomy highlights the shift from static pipelines toward more dynamic, agentic retrieval systems empowered by LLMs. Across diverse domains such as legal case analysis, biomedical literature retrieval, and scientific paper search, these technologies are already demonstrating their capacity to mitigate information overload.

**中文**

我们将现有方法综合为四个互补的范式：整个文档的整体建模、分割和重新聚合证据的分而治之策略、利用文档组织的索引结构创新以及用于长查询检索的专门方法。这种分类法强调了从静态管道向由法学硕士支持的更动态、更代理的检索系统的转变。在法律案例分析、生物医学文献检索和科学论文搜索等不同领域，这些技术已经证明了它们减轻信息过载的能力。

### 段落 194 · Page 28

**EN**

Yet, our review underscores that no single paradigm offers a universal solution. Instead, the optimal choice is inherently application-dependent, demanding a careful balance of trade-offs between computational efficiency, inference latency, and retrieval effectiveness, guided by the specific nature of the documents and user information needs. Looking ahead, we argue that the most promising progress will come from hybrid architectures: systems that fuse the efficiency of classical IR indexing, the semantic depth of neural encoders, and the reasoning capabilities of LLMs.

**中文**

然而，我们的评论强调，没有任何单一范式可以提供通用的解决方案。相反，最佳选择本质上取决于应用程序，需要在计算效率、推理延迟和检索有效性之间进行仔细权衡，并以文档的特定性质和用户信息需求为指导。展望未来，我们认为最有希望的进展将来自混合架构：融合经典 IR 索引的效率、神经编码器的语义深度和法学硕士的推理能力的系统。

### 段落 195 · Page 28

**EN**

Equally important is the development of next-generation evaluation frameworks that move beyond coarse-grained metrics to capture attribution, faithfulness, and user-centered utility in long-document settings. As these hybrid systems mature, they promise to transform how we interact with large-scale information, moving beyond simple document retrieval towards a future of deep evidence synthesis and automated knowledge discovery at scale. References [1] 2002. Automatic Indexing. Springer US, Boston, MA, 105–137. https://doi.org/10.1007/0-306-47031-4_5 [2] Negar Arabzadeh, Alexandra Vtyurina, Xinyi Yan, and Charles LA Clarke. 2022.

**中文**

同样重要的是下一代评估框架的开发，该框架超越了粗粒度的指标，以捕获长文档环境中的归因、忠实度和以用户为中心的效用。随着这些混合系统的成熟，它们有望改变我们与大规模信息交互的方式，超越简单的文档检索，走向深度证据合成和大规模自动化知识发现的未来。参考文献 [1] 2002 年。自动索引。施普林格美国，波士顿，马萨诸塞州，105–137。 https://doi.org/10.1007/0-306-47031-4_5 [2] Negar Arabzadeh、Alexandra Vtyurina、Xinyi Yan 和 Charles LA Clarke。 2022 年。

### 段落 196 · Page 28

**EN**

Shallow pooling for sparse labels. Information Retrieval Journal 25, 4 (2022), 365–385. [3] Akari Asai, Tatsunori Hashimoto, Hannaneh Hajishirzi, Richard Socher, and Caiming Xiong. 2020. XOR QA: Cross-lingual Open-Retrieval Question Answering. arXiv preprint arXiv:2010.11856 (2020). https://arxiv.org/abs/2010.11856 [4] Arian Askari, Suzan Verberne, Amin Abolghasemi, Wessel Kraaij, and Gabriella Pasi. 2024. Retrieval for extremely long queries and documents with RPRS: a highly efficient and effective transformer-based re-ranker. ACM Transactions on Information Systems 42, 5 (2024), 1–32.

**中文**

稀疏标签的浅池。信息检索杂志 25, 4 (2022), 365–385。 [3] Akari Asai、Tatsunori Hashimoto、Hannaneh Hajishirzi、Richard Socher 和 Caiming Xiong。 2020. XOR QA：跨语言开放检索问答。 arXiv 预印本 arXiv:2010.11856 (2020)。 https://arxiv.org/abs/2010.11856 [4] Arian Askari、Suzan Verberne、Amin Abolghasemi、Wessel Kraaij 和 Gabriella Pasi。 2024. 使用 RPRS 检索极长的查询和文档：一种高效且有效的基于Transformer的重新排序器。 ACM 信息系统汇刊 42, 5 (2024), 1–32。

### 段落 197 · Page 28

**EN**

[5] Payal Bajaj, Daniel Campos, Nick Craswell, Li Deng, Jianfeng Gao, Xiaodong Liu, Rangan Majumder, Andrew McNamara, Bhaskar Mitra, Tri Nguyen, Mir Rosenberg, and Sachin Tiwary. 2016. MS MARCO: A Human Generated Machine Reading Comprehension Dataset. arXiv preprint arXiv:1611.09268 (2016). https://arxiv.org/abs/1611.09268 [6] Iz Beltagy, Kyle Lo, and Arman Cohan. 2019. SciBERT: A pretrained language model for scientific text. arXiv preprint arXiv:1903.10676 (2019). [7] Iz Beltagy, Kyle Lo, and Arman Cohan. 2019. SciBERT: A Pretrained Language Model for Scientific Text.

**中文**

[5] Payal Bajaj、Daniel Campos、Nick Craswell、邓力、高剑锋、刘晓东、Rangan Majumder、Andrew McNamara、Bhaskar Mitra、Tri Nguyen、Mir Rosenberg 和 Sachin Tiwary。 2016. MS MARCO：人类生成的机器阅读理解数据集。 arXiv 预印本 arXiv:1611.09268 (2016)。 https://arxiv.org/abs/1611.09268 [6] Iz Beltagy、Kyle Lo 和 Arman Cohan。 2019.SciBERT：科学文本的预训练语言模型。 arXiv 预印本 arXiv:1903.10676 (2019)。 [7] 伊兹·贝尔塔吉 (Iz Beltagy)、凯尔·洛 (Kyle Lo) 和阿曼·科汉 (Arman Cohan)。 2019.SciBERT：科学文本的预训练语言模型。

### 段落 198 · Page 28

**EN**

arXiv:1903.10676 [cs.CL] https: //arxiv.org/abs/1903.10676 [8] Iz Beltagy, Matthew E Peters, and Arman Cohan. 2020. Longformer: The long-document transformer. arXiv preprint arXiv:2004.05150 (2020). [9] Sinchana Ramakanth Bhat, Max Rudat, Jannis Spiekermann, and Nicolas Flores-Herr. 2025. Rethinking Chunk Size For Long-Document Retrieval: A Multi-Dataset Analysis. arXiv preprint arXiv:2505.21700 (2025). [10] Stefan Büttcher, Charles L. A. Clarke, and Ian Soboroff. 2006. The TREC 2006 Terabyte Track. In TREC. [11] James P. Callan. 1994. Passage-Level Evidence in Document Retrieval. In SIGIR ’94, Bruce W. Croft and C. J. van Rijsbergen (Eds.).

**中文**

arXiv:1903.10676 [cs.CL] https://arxiv.org/abs/1903.10676 [8] Iz Beltagy、Matthew E Peters 和 Arman Cohan。 2020.Longformer：长文档转换器。 arXiv 预印本 arXiv:2004.05150 (2020)。 [9] Sinchana Ramakanth Bhat、Max Rudat、Jannis Spiekermann 和 Nicolas Flores-Herr。 2025。重新思考长文档检索的块大小：多数据集分析。 arXiv 预印本 arXiv:2505.21700 (2025)。 [10] Stefan Büttcher、Charles L. A. Clarke 和 Ian Soboroff。 2006 年。TREC 2006 太字节赛道。在特雷克。 [11] 詹姆斯·P·卡兰。 1994.文档检索中的段落级证据。在 SIGIR ’94 中，Bruce W. Croft 和 C. J. van Rijsbergen（编辑）。

### 段落 199 · Page 28

**EN**

Springer London, London, 302–310. [12] Rong-Yu Cao, Yi-Xuan Cao, Gan-Bin Zhou, and Ping Luo. 2022. Extracting variable-depth logical document hierarchy from long documents: method, evaluation, and application. Journal of Computer Science and Technology 37, 3 (2022), 699–718. [13] Ilias Chalkidis, Manos Fergadiotis, Prodromos Malakasiotis, Nikolaos Aletras, and Ion Androutsopoulos. 2020. LEGAL-BERT: The muppets straight out of law school. arXiv preprint arXiv:2010.02559 (2020). [14] Jianlv Chen, Shitao Xiao, Peitian Zhang, Kun Luo, Defu Lian, and Zheng Liu. 2024.

**中文**

施普林格伦敦，伦敦，302-310。 [12] 曹荣宇，曹益轩，周干斌，罗平。 2022.从长文档中提取可变深度的逻辑文档层次结构：方法、评估和应用。计算机科学与技术杂志 37, 3 (2022), 699–718。 [13] Ilias Chalkidis、Manos Fergadiotis、Prodromos Malakasiotis、Nikolaos Aletras 和 Ion Androutsopoulos。 2020. LEGAL-BERT：法学院刚毕业的布偶。 arXiv 预印本 arXiv:2010.02559 (2020)。 [14] 陈建旅，肖世涛，张培田，罗昆，连德福，刘峥。 2024 年。

### 段落 200 · Page 28

**EN**

BGE M3-Embedding: Multi-Lingual, Multi-Functionality, Multi-Granularity Text Embeddings Through Self-Knowledge Distillation. arXiv:2402.03216 [cs.CL]

**中文**

BGE M3-Embedding：通过自我知识蒸馏实现多语言、多功能、多粒度文本嵌入。 arXiv:2402.03216 [cs.CL]

### Page 29

### 段落 201 · Page 29

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 29 [15] Yukang Chen, Shengju Qian, Haotian Tang, Xin Lai, Zhijian Liu, Song Han, and Jiaya Jia. 2023. Longlora: Efficient fine-tuning of long-context large language models. arXiv preprint arXiv:2309.12307 (2023). [16] Jaemin Cho, Debanjan Mahata, Ozan Irsoy, Yujie He, and Mohit Bansal. 2024. M3docrag: Multi-modal retrieval is what you need for multi-page multi-document understanding. arXiv preprint arXiv:2411.04952 (2024). [17] Arman Cohan, Sergey Feldman, Iz Beltagy, Doug Downey, and Daniel S. Weld. 2020.

**中文**

PLM和LLM时代的长文献检索综述29 [15] 陈宇康，钱盛举，唐浩天，赖鑫，刘志坚，韩松，贾亚雅。 2023. Longlora：长上下文大语言模型的高效微调。 arXiv 预印本 arXiv：2309.12307 (2023)。 [16] Jaemin Cho，Debanjan Mahata，Ozan Irsoy，Yujie He，Mohit Bansal。 2024. M3docrag：多模式检索是多页面多文档理解所需要的。 arXiv 预印本 arXiv:2411.04952 (2024)。 [17] 阿曼·科汉、谢尔盖·费尔德曼、伊兹·贝尔塔吉、道格·唐尼和丹尼尔·S·韦尔德。 2020.

### 段落 202 · Page 29

**EN**

SPECTER: Document-level Representation Learning using Citation-informed Transformers. arXiv:2004.07180 [cs.CL] https://arxiv.org/abs/2004.07180 [18] Nick Craswell, Bhaskar Mitra, Emine Yilmaz, Daniel Campos, and Ellen M Voorhees. 2020. Overview of the TREC 2019 deep learning track. arXiv e-prints (2020), arXiv–2003. [19] Jiaxi Cui, Zongjian Li, Yang Yan, Bohua Chen, and Li Yuan. 2023. Chatlaw: Open-source legal large language model with integrated external knowledge bases. CoRR (2023). [20] Wei Dai, Peng Fu, and Chunjing Gan. 2024. Advancing Academic Knowledge Retrieval via LLM-enhanced Representation Similarity Fusion.

**中文**

SPECTRE：使用引用通知Transformer的文档级表示学习。 arXiv:2004.07180 [cs.CL] https://arxiv.org/abs/2004.07180 [18] Nick Craswell、Bhaskar Mitra、Emine Yilmaz、Daniel Campos 和 Ellen M Voorhees。 2020。TREC 2019 深度学习赛道概述。 arXiv 电子印刷品 (2020)，arXiv–2003。 [19] 崔家喜，李宗建，杨岩，陈博华，李源。 2023.Chatlaw：具有集成外部知识库的开源法律大语言模型。 CoRR（2023）。 [20]戴伟，付鹏，甘春晶。 2024.通过法学硕士增强的表示相似性融合推进学术知识检索。

### 段落 203 · Page 29

**EN**

arXiv:2410.10455 [cs.IR] https://arxiv.org/abs/2410.10455 [21] Zhuyun Dai and Jamie Callan. 2019. Deeper text understanding for IR with contextual neural language modeling. In Proceedings of the 42nd international ACM SIGIR conference on research and development in information retrieval. 985–988. [22] Tri Dao, Dan Fu, Stefano Ermon, Atri Rudra, and Christopher Ré. 2022. Flashattention: Fast and memory-efficient exact attention with io-awareness. Advances in neural information processing systems 35 (2022), 16344–16359. [23] Loic Kwate Dassi and Loic Kwate. 2021. Legal-bigbird: An adapted long-range transformer for legal documents.

**中文**

arXiv:2410.10455 [cs.IR] https://arxiv.org/abs/2410.10455 [21] Zhuyun Dai 和 Jamie Callan。 2019.通过上下文神经语言模型对 IR 进行更深入的文本理解。第 42 届国际 ACM SIGIR 信息检索研究与开发会议论文集。 985–988。 [22] Tri Dao、Dan Fu、Stefano Ermon、Atri Rudra 和 Christopher Ré。 2022. Flashattention：具有 io 意识的快速、内存高效的精确注意力。神经信息处理系统的进展 35 (2022), 16344–16359。 [23] 卢伊克·夸特·达西和卢伊克·夸特。 2021.Legal-bigbird：适用于法律文件的远程Transformer。

### 段落 204 · Page 29

**EN**

In Proceedings of the 35th International Conference on Neural Information Processing Systems, Black in AI Workshop. Curran Associates, Inc. [24] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. 2018. BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. arXiv preprint arXiv:1810.04805 (2018). https://arxiv.org/abs/1810.04805 [25] Jiayu Ding, Shuming Ma, Li Dong, Xingxing Zhang, Shaohan Huang, Wenhui Wang, Nanning Zheng, and Furu Wei. 2023. Longnet: Scaling transformers to 1,000,000,000 tokens. arXiv preprint arXiv:2307.02486 (2023).

**中文**

第 35 届神经信息处理系统国际会议论文集，Black in AI Workshop。 Curran Associates, Inc. [24] Jacob Devlin、Ming-Wei Chang、Kenton Lee 和 Kristina Toutanova。 2018.BERT：用于语言理解的深度双向Transformer的预训练。 arXiv 预印本 arXiv:1810.04805 (2018)。 https://arxiv.org/abs/1810.04805 [25] 丁家玉，马树明，董立，张星星，黄少涵，王文辉，郑南宁，魏福如。 2023. Longnet：将 Transformer 扩展到 1,000,000,000 个代币。 arXiv 预印本 arXiv:2307.02486 (2023)。

### 段落 205 · Page 29

**EN**

[26] Kuicai Dong, Yujing Chang, Xin Deik Goh, Dexun Li, Ruiming Tang, and Yong Liu. 2025. Mmdocir: Benchmarking multi-modal retrieval for long documents. arXiv preprint arXiv:2501.08828 (2025). [27] Kuicai Dong, Derrick Goh Xin Deik, Yi Lee, Hao Zhang, Xiangyang Li, Cong Zhang, and Yong Liu. 2024. MC-indexing: Effective Long Document Retrieval via Multi-view Content-aware Indexing. In Findings of the Association for Computational Linguistics: EMNLP 2024. 2673–2691. [28] Fangxiaoyu Feng, Yinfei Yang, Daniel Cer, Naveen Arivazhagan, and Wei Wang. 2020. Language-agnostic BERT Sentence Embedding. arXiv preprint arXiv:2007.01852 (2020).

**中文**

[26] 董奎才，张玉晶，吴欣德，李德勋，唐瑞明，刘勇。 2025. Mmdocir：长文档多模式检索基准测试。 arXiv 预印本 arXiv:2501.08828 (2025)。 [27] 董奎才，Derrick Goh Xin Deik，李毅，张浩，李向阳，张聪，刘勇。 2024. MC-indexing：通过多视图内容感知索引进行有效的长文档检索。计算语言学协会的调查结果：EMNLP 2024。2673–2691。 [28] 冯方晓宇，杨银飞，Daniel Cer，Naveen Arivazhagan，王伟。 2020. 与语言无关的 BERT 句子嵌入。 arXiv 预印本 arXiv:2007.01852 (2020)。

### 段落 206 · Page 29

**EN**

https://arxiv.org/abs/2007.01852 [29] Luyu Gao and Jamie Callan. 2022. Long document re-ranking with modular re-ranker. In Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval. 2371–2376. [30] Yu Gu, Robert Tinn, Hao Cheng, Michael Lucas, Naoto Usuyama, Xiaodong Liu, Tristan Naumann, Jianfeng Gao, and Hoifung Poon. 2021. Domainspecific language model pretraining for biomedical natural language processing. ACM Transactions on Computing for Healthcare (HEALTH) 3, 1 (2021), 1–23. [31] Jiafeng Guo, Yixing Fan, Qingyao Ai, and W. Bruce Croft. 2016.

**中文**

https://arxiv.org/abs/2007.01852 [29] 高鲁宇和杰米·卡兰。 2022. 使用模块化重新排序器对长文档进行重新排序。第 45 届国际 ACM SIGIR 信息检索研究与开发会议论文集。 2371–2376。 [30] Yu Gu、Robert Tinn、Hao Cheng、Michael Lucas、Naoto Usuyama、Xiaodong Liu、Tristan Naumann、Jianfeng Gau 和 Hoifung Poon。 2021. 用于生物医学自然语言处理的领域特定语言模型预训练。 ACM 医疗保健计算交易 (HEALTH) 3, 1 (2021), 1–23。 [31] 郭嘉峰，范宜兴，艾庆耀，W.布鲁斯·克罗夫特。 2016年。

### 段落 207 · Page 29

**EN**

A Deep Relevance Matching Model for Ad-hoc Retrieval. In Proceedings of the 25th ACM International on Conference on Information and Knowledge Management (Indianapolis, Indiana, USA) (CIKM ’16). Association for Computing Machinery, New York, NY, USA, 55–64. https://doi.org/10.1145/2983323.2983769 [32] Jiafeng Guo, Yixing Fan, Liang Pang, Liu Yang, Qingyao Ai, Hamed Zamani, Chen Wu, W Bruce Croft, and Xueqi Cheng. 2020. A deep look into neural ranking models for information retrieval. Information Processing & Management 57, 6 (2020), 102067. [33] Lovisa Hagström, Ercong Nie, Ruben Halifa, Helmut Schmid, Richard Johansson, and Alexander Junge.

**中文**

用于即席检索的深度相关性匹配模型。第 25 届 ACM 国际信息和知识管理会议（美国印第安纳州印第安纳波利斯）会议记录 (CIKM '16)。计算机协会，美国纽约州纽约市，55–64。 https://doi.org/10.1145/2983323.2983769 [32] 郭嘉峰，范宜兴，庞亮，刘洋，艾庆耀，Hamed Zamani，吴晨，W Bruce Croft，程学奇。 2020。深入研究信息检索的神经排序模型。信息处理与管理 57, 6 (2020), 102067。 [33] Lovisa Hagström、Ercong Nie、Ruben Halifa、Helmut Schmid、Richard Johansson 和 Alexander Junge。

### 段落 208 · Page 29

**EN**

2025. Language Model Re-rankers are Fooled by Lexical Similarities. In Proceedings of the Eighth Fact Extraction and VERification Workshop (FEVER). 18–33. [34] Yichen He, Guanhua Huang, Peiyuan Feng, Yuan Lin, Yuchen Zhang, Hang Li, and Weinan E. 2025. PaSa: An LLM Agent for Comprehensive Academic Paper Search. arXiv:2501.10120 [cs.IR] https://arxiv.org/abs/2501.10120 [35] Sebastian Hofstätter, Bhaskar Mitra, Hamed Zamani, Nick Craswell, and Allan Hanbury. 2021. Intra-document cascading: Learning to select passages for neural document ranking.

**中文**

2025. 语言模型重新排序者被词汇相似性愚弄了。第八届事实提取和验证研讨会（FEVER）的会议记录。 18-33。 [34] 何一尘、黄冠华、冯培元、林元、张雨辰、李航、E维南. 2025. PaSa：法学硕士综合学术论文检索代理。 arXiv:2501.10120 [cs.IR] https://arxiv.org/abs/2501.10120 [35] Sebastian Hofstätter、Bhaskar Mitra、Hamed Zamani、Nick Craswell 和 Allan Hanbury。 2021.文档内级联：学习选择神经文档排序的段落。

### 段落 209 · Page 29

**EN**

In Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval. 1349–1358. [36] Po-Sen Huang, Xiaodong He, Jianfeng Gao, Li Deng, Alex Acero, and Larry Heck. 2013. Learning deep structured semantic models for web search using clickthrough data. In Proceedings of the 22nd ACM International Conference on Information & Knowledge Management (San Francisco, California, USA) (CIKM ’13). Association for Computing Machinery, New York, NY, USA, 2333–2338. https://doi.org/10.1145/2505515.2505665 [37] Kai Hui, Andrew Yates, Klaus Berberich, and Gerard De Melo. 2017.

**中文**

第 44 届国际 ACM SIGIR 信息检索研究与发展会议论文集。 1349–1358。 [36]黄宝森，何晓东，高剑峰，邓力，Alex Acero，Larry Heck。 2013 年。使用点击数据学习网络搜索的深度结构化语义模型。第 22 届 ACM 国际信息与知识管理会议（美国加利福尼亚州旧金山）（CIKM '13）论文集。计算机协会，美国纽约州纽约市，2333–2338。 https://doi.org/10.1145/2505515.2505665 [37] Kai Hui、Andrew Yates、Klaus Berberich 和 Gerard De Melo。 2017年。

### 段落 210 · Page 29

**EN**

PACRR: A Position-Aware Neural IR Model for Relevance Matching. In Proceedings of the 2017 Conference on Empirical Methods in Natural Language Processing. 1049–1058. [38] Lawrence Keunho Jang, Yinheng Li, Charles Ding, Justin Lin, Paul Pu Liang, Dan Zhao, Rogerio Bonatti, and Kazuhito Koishida. [n. d.]. VideoWebArena: Evaluating Long Context Multimodal Agents with Video Understanding Web Tasks. In NeurIPS 2024 Workshop on Open-World Agents. [39] Huiqiang Jiang, Qianhui Wu, Xufang Luo, Dongsheng Li, Chin-Yew Lin, Yuqing Yang, and Lili Qiu. 2024. LongLLMLingua: Accelerating and Enhancing LLMs in Long Context Scenarios via Prompt Compression.

**中文**

PACRR：用于相关性匹配的位置感知神经 IR 模型。 2017 年自然语言处理经验方法会议论文集。 1049–1058。 [38] Lawrence Keunho Jang、Yinheng Li、Charles Ding、Justin Lin、Paul Pu Liang、Dan Zhu、Rogerio Bonatti 和 Kazuhito Koishida。 [n. d.]。 VideoWebArena：通过视频理解 Web 任务评估长上下文多模式代理。在 NeurIPS 2024 开放世界智能体研讨会上。 [39]蒋惠强，吴千惠，罗旭芳，李东升，林清耀，杨雨清，邱莉莉。 2024. LongLLMLingua：​​通过即时压缩在长上下文场景中加速和增强法学硕士。

### 段落 211 · Page 29

**EN**

In Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers). 1658–1677.

**中文**

计算语言学协会第 62 届年会论文集（第一卷：长论文）。 1658–1677。

### Page 30

### 段落 212 · Page 30

**EN**

30 Li et al. [40] Jyun-Yu Jiang, Chenyan Xiong, Chia-Jung Lee, and Wei Wang. 2020. Long document ranking with query-directed sparse transformer. arXiv preprint arXiv:2010.12683 (2020). [41] Alistair Johnson, Lucas Bulgarelli, Tom Pollard, Steven Horng, Leo Anthony Celi, and Roger Mark. 2020. Mimic-iv. PhysioNet. Available online at: https://physionet. org/content/mimiciv/1.0/(accessed August 23, 2021) (2020), 49–55. [42] Karen Sparck Jones. 1973. Index term weighting.Information Storage and Retrieval 9, 11 (1973), 619–633.

**中文**

30 李等人。 [40]姜俊宇，熊陈艳，李家正，王伟。 2020. 使用查询导向的稀疏变换器对长文档进行排名。 arXiv 预印本 arXiv:2010.12683 (2020)。 [41] 阿利斯泰尔·约翰逊、卢卡斯·布尔加雷利、汤姆·波拉德、史蒂文·霍恩、利奥·安东尼·塞利和罗杰·马克。 2020.模仿-iv。生理网。在线提供：https://phyonet。 org/content/mimiciv/1.0/（2021 年 8 月 23 日访问）（2020 年），49-55。 [42]凯伦·斯帕克·琼斯。 1973. 索引项加权。信息存储和检索 9, 11 (1973), 619–633。

### 段落 213 · Page 30

**EN**

https://doi.org/10.1016/0020-0271(73)90043- 0 [43] Vladimir Karpukhin, Barlas Oguz, Sewon Min, Patrick SH Lewis, Ledell Wu, Sergey Edunov, Danqi Chen, and Wen-tau Yih. 2020. Dense Passage Retrieval for Open-Domain Question Answering.. In EMNLP (1). 6769–6781. [44] Omar Khattab and Matei Zaharia. 2020. Colbert: Efficient and effective passage search via contextualized late interaction over bert. In Proceedings of the 43rd International ACM SIGIR conference on research and development in Information Retrieval. 39–48. [45] Nikita Kitaev, Lukasz Kaiser, and Anselm Levskaya. [n. d.]. Reformer: The Efficient Transformer.

**中文**

https://doi.org/10.1016/0020-0271(73)90043-0 [43] Vladimir Karpukhin、Barlas Oguz、Sewon Min、Patrick SH Lewis、Ledell Wu、Sergey Edunov、Danqi Chen 和 Wen-tau Yih。 2020. 用于开放域问答的密集段落检索.. 在 EMNLP (1) 中。 6769–6781。 [44] 奥马尔·哈塔布和马泰·扎哈里亚。 2020. Colbert：通过 bert 上的上下文化后期交互进行高效且有效的段落搜索。第 43 届国际 ACM SIGIR 信息检索研究与开发会议论文集。 39-48。 [45] 尼基塔·基塔耶夫、卢卡斯·凯泽和安塞姆·列夫斯卡娅。 [n. d.]。改革者：高效的Transformer。

### 段落 214 · Page 30

**EN**

In International Conference on Learning Representations. [46] Tom Kwiatkowski, Jennimaria Palomaki, Olivia Redfield, Michael Collins, Ankur Parikh, Chris Alberti, Danielle Epstein, Illia Polosukhin, Jacob Devlin, Kenton Lee, et al. 2019. Natural questions: a benchmark for question answering research.Transactions of the Association for Computational Linguistics 7 (2019), 453–466. [47] Lemur Project. 2012. ClueWeb12 Dataset. Online. https://lemurproject.org/clueweb12/ Accessed on July 22, 2025. [48] Canjia Li, Andrew Yates, Sean MacAvaney, Ben He, and Yingfei Sun. 2023. Parade: Passage representation aggregation fordocument reranking.

**中文**

在国际学习代表会议上。 [46] Tom Kwiatkowski、Jennimaria Palomaki、Olivia Redfield、Michael Collins、Ankur Parikh、Chris Alberti、Danielle Epstein、Illia Polosukhin、Jacob Devlin、Kenton Lee 等人。 2019. 自然问题：问答研究的基准。计算语言学协会汇刊 7 (2019), 453–466。 [47] 狐猴项目。 2012.ClueWeb12 数据集。在线的。 https://lemurproject.org/clueweb12/ 访问时间：2025 年 7 月 22 日。 [48] Canjia Li、Andrew Yates、Sean MacAvaney、Ben He 和 Yingfei Sun。 2023.Parade：用于文档重排的段落表示聚合。

### 段落 215 · Page 30

**EN**

ACM Transactions on Information Systems 42, 2 (2023), 1–26. [49] Minghan Li and Eric Gaussier. 2022. Bert-based dense intra-ranking and contextualized late interaction via multi-task learning for long document retrieval. In Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval. 2347–2352. [50] Minghan Li, Eric Gaussier, Juntao Li, and Guodong Zhou. 2024. KeyB2: Selecting Key Blocks is Also Important for Long Document Ranking with Large Language Models. arXiv preprint arXiv:2411.06254 (2024). [51] Minghan Li, Eric Gaussier, and Guodong Zhou. 2025.

**中文**

ACM 信息系统汇刊 42, 2 (2023), 1–26。 [49]李明汉和埃里克·高西尔。 2022. 基于 Bert 的密集内部排名和通过多任务学习进行情境化后期交互以进行长文档检索。第 45 届国际 ACM SIGIR 信息检索研究与开发会议论文集。 2347–2352。 [50] 李明汉，Eric Gaussier，李俊涛，周国栋。 2024.KeyB2：选择关键块对于大型语言模型的长文档排名也很重要。 arXiv 预印本 arXiv:2411.06254 (2024)。 [51] 李明汉，Eric Gaussier，周国栋。 2025 年。

### 段落 216 · Page 30

**EN**

Enhanced Retrieval of Long Documents: Leveraging Fine-Grained Block Representations with Large Language Models. arXiv preprint arXiv:2501.17039 (2025). [52] Minghan Li, Diana Nicoleta Popa, Johan Chagnon, Yagmur Gizem Cinar, and Eric Gaussier. 2023. The power of selecting key blocks with local pre-ranking for long document information retrieval. ACM Transactions on Information Systems 41, 3 (2023), 1–35. [53] YUCHENG LI, BO DONG, Frank Guerin, and Chenghua Lin. [n. d.]. Compressing Context to Enhance Inference Efficiency of Large Language Models. In The 2023 Conference on Empirical Methods in Natural Language Processing.

**中文**

增强长文档检索：利用大型语言模型的细粒度块表示。 arXiv 预印本 arXiv:2501.17039 (2025)。 [52] 李明汉、戴安娜·尼科莱塔·波帕、约翰·查格农、亚格穆尔·吉泽姆·西纳尔和埃里克·高西尔。 2023.通过本地预排序选择关键块以进行长文档信息检索的能力。 ACM 信息系统汇刊 41, 3 (2023), 1–35。 [53] 李玉成，董波，Frank Guerin，林成华。 [n. d.]。压缩上下文以提高大型语言模型的推理效率。 2023 年自然语言处理经验方法会议。

### 段落 217 · Page 30

**EN**

[54] Yikuan Li, Ramsey M Wehbe, Faraz S Ahmad, Hanyin Wang, and Yuan Luo. 2022. Clinical-longformer and clinical-bigbird: Transformers for long clinical sequences. arXiv preprint arXiv:2201.11838 (2022). [55] Peerat Limkonchotiwat, Wuttikorn Ponwitayarat, Lalita Lowphansirikul, Potsawee Manakul, Can Udomcharoenchaikit, Ekapol Chuangsuwanich, and Sarana Nutanong. 2024. McCrolin: Multi-consistency Cross-lingual Training for Retrieval Question Answering. In Findings of the Association for Computational Linguistics: EMNLP 2024, Yaser Al-Onaizan, Mohit Bansal, and Yun-Nung Chen (Eds.).

**中文**

[54]李毅宽，Ramsey M Wehbe，Faraz S Ahmad，王汉银，罗媛。 2022. Clinical-longformer 和 Clinical-bigbird：用于长临床序列的 Transformers。 arXiv 预印本 arXiv:2201.11838 (2022)。 [55] Peerat Limkonchotiwat、Wuttikorn Ponwitayarat、Lalita Lowphansirikul、Potsawee Manakul、Can Udomcharoenchaikit、Ekapol Chuangsuwanich 和 Sarana Nutanong。 2024. McCrolin：检索问答的多一致性跨语言训练。计算语言学协会的调查结果：EMNLP 2024，Yaser Al-Onaizan、Mohit Bansal 和 Yun-Nung Chen（编辑）。

### 段落 218 · Page 30

**EN**

Association for Computational Linguistics, Miami, Florida, USA, 2780–2793. https://doi.org/10.18653/v1/2024.findings-emnlp.157 [56] Dingkun Long, Qiong Gao, Kuan Zou, Guangwei Xu, Pengjun Xie, Rui Guo, Jianfeng Xu, Guanjun Jiang, Luxi Xing, and P. Yang. 2022. Multi-CPR: A Multi Domain Chinese Dataset for Passage Retrieval. (2022). [57] Jakub Lála, Odhran O’Donoghue, Aleksandar Shtedritski, Sam Cox, Samuel G. Rodriques, and Andrew D. White. 2023. PaperQA: Retrieval-Augmented Generative Agent for Scientific Research. arXiv:2312.07559 [cs.CL] https://arxiv.org/abs/2312.07559 [58] Xueguang Ma, Liang Wang, Nan Yang, Furu Wei, and Jimmy Lin. 2024.

**中文**

计算语言学协会，美国佛罗里达州迈阿密，2780-2793。 https://doi.org/10.18653/v1/2024.findings-emnlp.157 [56] 龙定坤，高琼，邹宽，徐光伟，谢鹏军，郭锐，徐剑峰，蒋冠军，邢鲁西，杨鹏。 2022. Multi-CPR：用于段落检索的多域中文数据集。 （2022）。 [57] Jakub Lála、Odhran O’Donoghue、Aleksandar Shtedritski、Sam Cox、Samuel G. Rodriques 和 Andrew D. White。 2023.PaperQA：用于科学研究的检索增强生成代理。 arXiv:2312.07559 [cs.CL] https://arxiv.org/abs/2312.07559 [58] 马学光、王亮、杨楠、魏福如和林吉米。 2024 年。

### 段落 219 · Page 30

**EN**

Fine-Tuning LLaMA for Multi-Stage Text Retrieval. In SIGIR. [59] Sina Bagheri Nezhad and Ameeta Agrawal. 2025. CROSS: Analyzing the Trade-offs in Long-Context Cross-lingual Retrieval. InICLR 2025 Workshop on Foundation Models in the Wild. https://openreview.net/forum?id=sOXznQZgnM [60] Malte Ostendorff, Nils Rethmeier, Isabelle Augenstein, Bela Gipp, and Georg Rehm. 2022. Neighborhood Contrastive Learning for Scientific Document Representations with Citation Embeddings. arXiv:2202.06671 [cs.CL] https://arxiv.org/abs/2202.06671 [61] Liang Pang, Yanyan Lan, and Xueqi Cheng. 2021.

**中文**

微调 LLaMA 以进行多阶段文本检索。在西吉尔。 [59] 西娜·巴盖里·内扎德和阿米塔·阿格拉瓦尔。 2025.CROSS：分析长上下文跨语言检索的权衡。 InICLR 2025 野外基础模型研讨会。 https://openreview.net/forum?id=sOXznQZgnM [60] Malte Ostendorff、Nils Rethmeier、Isabelle Augenstein、Bela Gipp 和 Georg Rehm。 2022.带有引文嵌入的科学文档表示的邻域对比学习。 arXiv:2202.06671 [cs.CL] https://arxiv.org/abs/2202.06671 [61] 庞亮、兰岩岩和程学奇。 2021 年。

### 段落 220 · Page 30

**EN**

Match-ignition: Plugging pagerank into transformer for long-form text matching. In Proceedings of the 30th ACM international conference on information & knowledge management. 1396–1405. [62] Liang Pang, Yanyan Lan, Jiafeng Guo, Jun Xu, Shengxian Wan, and Xueqi Cheng. 2016. Text matching as image recognition. In Proceedings of the Thirtieth AAAI Conference on Artificial Intelligence (Phoenix, Arizona) (AAAI’16). AAAI Press, 2793–2799. [63] Liang Pang, Yanyan Lan, Jiafeng Guo, Jun Xu, Jingfang Xu, and Xueqi Cheng. 2017. Deeprank: A new deep architecture for relevance ranking in information retrieval.

**中文**

Match-ignition：将 pagerank 插入转换器以进行长格式文本匹配。第 30 届 ACM 国际信息与知识管理会议论文集。 1396–1405。 [62] 庞亮，兰艳艳，郭家峰，徐军，万胜贤，程学奇。 2016.文本匹配作为图像识别。第三十届 AAAI 人工智能会议记录（亚利桑那州菲尼克斯）(AAAI’16)。 AAAI 出版社，2793–2799。 [63] 庞亮，兰艳艳，郭家峰，徐军，徐静芳，程学奇。 2017. Deeprank：信息检索中相关性排名的新深度架构。

### 段落 221 · Page 30

**EN**

In Proceedings of the 2017 ACM on Conference on Information and Knowledge Management. 257–266. [64] Richard Yuanzhe Pang, Alicia Parrish, Nitish Joshi, Nikita Nangia, Jason Phang, Angelica Chen, Vishakh Padmakumar, Johnny Ma, Jana Thompson, He He, et al. 2021. QuALITY: Question answering with long input texts, yes! arXiv preprint arXiv:2112.08608 (2021). [65] Sangwoo Park, Jinheon Baek, Soyeong Jeong, and Sung Ju Hwang. 2025. PRISM: Fine-Grained Paper-to-Paper Retrieval with Multi-Aspect-Aware Query Optimization. arXiv:2507.10057 [cs.IR] https://arxiv.org/abs/2507.10057 [66] Tao Qin and Tie-Yan Liu. 2013. Introducing LETOR 4.0 datasets.

**中文**

2017 年 ACM 信息和知识管理会议论文集。 257–266。 [64] Richard Yuanzhe Pang，Alicia Parrish，Nitish Joshi，Nikita Nangia，Jason Phang，Angelica Chen，Vishakh Padmakumar，Johnny Ma，Jana Thompson，He He，等。 2021. 质量：用长输入文本回答问题，是的！ arXiv 预印本 arXiv:2112.08608 (2021)。 [65] Sangwoo Park、Jinheon Baek、Soying Jeong 和 Sung Ju Hwang。 2025. PRISM：具有多方面感知查询优化的细粒度纸到纸检索。 arXiv:2507.10057 [cs.IR] https://arxiv.org/abs/2507.10057 [66] 秦涛和刘铁岩。 2013 年。引入 LETOR 4.0 数据集。

### 段落 222 · Page 30

**EN**

arXiv preprint arXiv:1306.2597 (2013). [67] Stephen Robertson, S. Walker, S. Jones, M. M. Hancock-Beaulieu, and M. Gatford. 1995. Okapi at TREC-3. In Overview of the Third Text REtrieval Conference (TREC-3) (overview of the third text retrieval conference (trec–3) ed.). Gaithersburg, MD: NIST, 109–126. https://www.microsoft.com/en-

**中文**

arXiv 预印本 arXiv:1306.2597 (2013)。 [67] 斯蒂芬·罗伯逊、S.沃克、S.琼斯、M.M.汉考克-博利厄和M.盖特福德。 1995. 霍加狓在 TREC-3。在第三次文本检索会议概述 (TREC-3) 中（第三次文本检索会议概述 (trec-3) 编辑）。马里兰州盖瑟斯堡：NIST，109-126。 https://www.microsoft.com/en-

### Page 31

### 段落 223 · Page 31

**EN**

A Survey of Long-Document Retrieval in the PLM and LLM Era 31 us/research/publication/okapi-at-trec-3/ [68] Parth Sarthi, Salman Abdullah, Aditi Tuli, Shubh Khanna, Anna Goldie, and Christopher D Manning. 2024. Raptor: Recursive abstractive processing for tree-organized retrieval. In The Twelfth International Conference on Learning Representations. [69] Minju Seo, Jinheon Baek, Seongyun Lee, and Sung Ju Hwang. 2024. Efficient Long Context Language Model Retrieval with Compression. arXiv preprint arXiv:2412.18232 (2024). [70] Zhihong Shao, Yeyun Gong, Yelong Shen, Minlie Huang, Nan Duan, and Weizhu Chen. 2023.

**中文**

PLM 和 LLM 时代的长文档检索调查 31 us/research/publication/okapi-at-trec-3/ [68] Parth Sarthi、Salman Abdullah、Aditi Tuli、Shubh Khanna、Anna Goldie 和 Christopher D Manning。 2024. Raptor：用于树组织检索的递归抽象处理。第十二届国际学习表征会议。 [69] Minju Seo、Jinheon Baek、Seongyun Lee 和 Sung Ju Hwang。 2024.通过压缩进行高效的长上下文语言模型检索。 arXiv 预印本 arXiv:2412.18232 (2024)。 [70] 邵志宏，宫业云，沉业龙，黄敏烈，段楠，陈伟柱。 2023 年。

### 段落 224 · Page 31

**EN**

Enhancing Retrieval-Augmented Large Language Models with Iterative Retrieval-Generation Synergy. In Findings of the Association for Computational Linguistics: EMNLP 2023. 9248–9274. [71] Boheng Sheng, Jiacheng Yao, Meicong Zhang, and Guoxiu He. 2025. Dynamic Chunking and Selection for Reading Comprehension of Ultra-Long Context in Large Language Models. arXiv preprint arXiv:2506.00773 (2025). [72] Isaac Shi, Zeyuan Li, Wenli Wang, Lewei He, Yang Yang, and Tianyu Shi. 2025. eSapiens: A Real-World NLP Framework for Multimodal Document Understanding and Enterprise Knowledge Processing. arXiv preprint arXiv:2506.16768 (2025).

**中文**

通过迭代检索生成协同作用增强检索增强大型语言模型。计算语言学协会的调查结果：EMNLP 2023。9248–9274。 [71]盛博恒，姚家成，张美聪，何国秀。 2025.大型语言模型中超长上下文阅读理解的动态分块和选择。 arXiv 预印本 arXiv:2506.00773 (2025)。 [72] Isaac Shi，Zeyuan Li，Wenli Wang，Lewei He，Yang Yang，Tianyu Shi。 2025. eSapiens：用于多模式文档理解和企业知识处理的真实 NLP 框架。 arXiv 预印本 arXiv:2506.16768 (2025)。

### 段落 225 · Page 31

**EN**

[73] Xiaofeng Shi, Yuduo Li, Qian Kou, Longbin Yu, Jinxin Xie, and Hua Zhou. 2025. SPAR: Scholar Paper Retrieval with LLM-based Agents for Enhanced Academic Search. arXiv:2507.15245 [cs.IR] https://arxiv.org/abs/2507.15245 [74] Thomas Sounack, Joshua Davis, Brigitte Durieux, Antoine Chaffin, Tom J Pollard, Eric Lehman, Alistair EW Johnson, Matthew McDermott, Tristan Naumann, and Charlotta Lindvall. 2025. BioClinical ModernBERT: A State-of-the-Art Long-Context Encoder for Biomedical and Clinical NLP. arXiv preprint arXiv:2506.10896 (2025). [75] Alexander Spangher, Tenghao Huang, Yiqin Huang, Lucas Spangher, Sewon Min, and Mark Dredze. 2025.

**中文**

[73]石晓峰，李玉多，寇谦，余龙斌，谢金新，周华。 2025. SPAR：使用基于法学硕士的代理进行学术论文检索，以增强学术搜索。 arXiv:2507.15245 [cs.IR] https://arxiv.org/abs/2507.15245 [74] Thomas Sounack、Joshua Davis、Brigitte Durieux、Antoine Chaffin、Tom J Pollard、Eric Lehman、Alistair EW Johnson、Matthew McDermott、Tristan Naumann 和 Charlotta Lindvall。 2025. BioClinical ModernBERT：用于生物医学和临床 NLP 的最先进的长上下文编码器。 arXiv 预印本 arXiv:2506.10896 (2025)。 [75] 亚历山大·斯潘格、黄腾浩、黄益勤、卢卡斯·斯潘格、Sewon Min 和马克·德雷泽。 2025 年。

### 段落 226 · Page 31

**EN**

A Novel Multi-Document Retrieval Benchmark: Journalist Source-Selection in Newswriting. In Proceedings of the 4th International Workshop on Knowledge-Augmented Methods for Natural Language Processing. 180–204. [76] Jianlin Su, Murtadha Ahmed, Yu Lu, Shengfeng Pan, Wen Bo, and Yunfeng Liu. 2024. Roformer: Enhanced transformer with rotary position embedding. Neurocomputing 568 (2024), 127063. [77] Weiwei Sun, Lingyong Yan, Xinyu Ma, Shuaiqiang Wang, Pengjie Ren, Zhumin Chen, Dawei Yin, and Zhaochun Ren. 2023. Is ChatGPT Good at Search? Investigating Large Language Models as Re-Ranking Agents. In EMNLP.

**中文**

新颖的多文档检索基准：新闻写作中的记者来源选择。第四届自然语言处理知识增强方法国际研讨会论文集。 180–204。 [76] 苏建林，Murtadha Ahmed，陆宇，潘胜峰，波文，刘云峰。 2024. Roformer：具有旋转位置嵌入的增强型Transformer。神经计算 568 (2024), 127063. [77] 孙伟伟，严令勇，马新宇，王帅强，任鹏杰，陈祝民，尹大伟，任兆春。 2023. ChatGPT 擅长搜索吗？研究大型语言模型作为重新排序代理。在 EMNLP 中。

### 段落 227 · Page 31

**EN**

[78] Yi Tay, Mostafa Dehghani, Dara Bahri, and Donald Metzler. 2023. Efficient Transformers: A Survey. Comput. Surveys 55, 8, Article 176 (2023), 40 pages. https://doi.org/10.1145/3530811 [79] Runchu Tian, Xueqiang Xu, Bowen Jin, SeongKu Kang, and Jiawei Han. 2025. LLM-Based Compact Reranking with Document Features for Scientific Retrieval. arXiv:2505.13757 [cs.IR] https://arxiv.org/abs/2505.13757 [80] Ellen Voorhees. 2004. Overview of the TREC 2004 Robust Retrieval Track. In TREC. [81] Junmei Wang, Jimmy X Huang, and Jinhua Sheng. 2024. An efficient long-text semantic retrieval approach via utilizing presentation learning on short-text.

**中文**

[78] Yi Tay、Mostafa Dehghani、Dara Bahri 和 Donald Metzler。 2023。高效Transformer：一项调查。计算。调查 55, 8，第 176 条 (2023)，40 页。 https://doi.org/10.1145/3530811 [79]田润初，徐学强，金博文，康圣库，韩家伟。 2025.基于 LLM 的紧凑重排序，具有用于科学检索的文档特征。 arXiv:2505.13757 [cs.IR] https://arxiv.org/abs/2505.13757 [80] 艾伦·沃里斯。 2004。TREC 2004 稳健检索轨道概述。在特雷克。 [81]王俊梅，黄吉米，盛金华。 2024.一种利用短文本表示学习的高效长文本语义检索方法。

### 段落 228 · Page 31

**EN**

Complex & Intelligent Systems 10, 1 (2024), 963–979. [82] Jiajia Wang, Weizhong Zhao, Xinhui Tu, and Tingting He. 2023. A novel dense retrieval framework for long document retrieval. Frontiers of Computer Science 17, 4 (2023), 174609. [83] Gengchen Wei, Xinle Pang, Tianning Zhang, Yu Sun, Xun Qian, Chen Lin, Han-Sen Zhong, and Wanli Ouyang. 2024. DocReLM: Mastering Document Retrieval with Language Model. arXiv:2405.11461 [cs.IR] https://arxiv.org/abs/2405.11461 [84] Chen Wu, Ruqing Zhang, Jiafeng Guo, Yixing Fan, and Xueqi Cheng. 2022. Are Neural Ranking Models Robust? ACM Trans. Inf. Syst. 41, 2, Article 29 (Dec. 2022), 36 pages.

**中文**

复杂与智能系统 10, 1 (2024), 963–979。 [82] 王佳佳，赵伟忠，涂新辉，何婷婷。 2023.一种用于长文档检索的新颖的密集检索框架。计算机科学前沿 17, 4 (2023), 174609. [83] 魏庚辰，庞欣乐，张天宁，孙宇，钱迅，林陈，钟汉森，欧阳万里。 2024.DocReLM：利用语言模型掌握文档检索。 arXiv:2405.11461 [cs.IR] https://arxiv.org/abs/2405.11461 [84] 吴晨、张如青、郭嘉峰、范宜兴和程学奇。 2022. 神经排序模型稳健吗？ ACM 翻译。信息。系统。 41, 2，第 29 条（2022 年 12 月），36 页。

### 段落 229 · Page 31

**EN**

https://doi.org/10.1145/3534928 [85] Yuhuai Wu, Markus Norman Rabe, DeLesley Hutchins, and Christian Szegedy. [n. d.]. Memorizing Transformers. InInternational Conference on Learning Representations. [86] Chaojun Xiao, Xueyu Hu, Zhiyuan Liu, Cunchao Tu, and Maosong Sun. 2021. Lawformer: A pre-trained language model for chinese legal long documents. AI Open 2 (2021), 79–84. [87] Guangxuan Xiao, Jiaming Tang, Jingwei Zuo, Shang Yang, Haotian Tang, Yao Fu, Song Han, et al. [n. d.]. DuoAttention: Efficient Long-Context LLM Inference with Retrieval and Streaming Heads. In The Thirteenth International Conference on Learning Representations.

**中文**

https://doi.org/10.1145/3534928 [85] 吴玉怀、马库斯·诺曼·拉贝、德莱斯利·哈钦斯和克里斯蒂安·塞格迪。 [n. d.]。记忆变形金刚。在国际学习代表会议上。 [86] 肖朝军，胡雪玉，刘志远，涂存超，孙茂松。 2021.Lawformer：中国法律长文档的预训练语言模型。 AI 公开赛 2（2021），79–84。 [87]肖光轩，唐家明，左经纬，商阳，唐浩天，付耀，韩松，等。 [n. d.]。 DuoAttention：具有检索和流处理头的高效长上下文 LLM 推理。在第十三届学习表征国际会议上。

### 段落 230 · Page 31

**EN**

[88] Lee Xiong, Chenyan Xiong, Ye Li, Kwok-Fung Tang, Jialin Liu, Paul Bennett, Junaid Ahmed, and Arnold Overwijk. 2020. Approximate nearest neighbor negative contrastive learning for dense text retrieval. arXiv preprint arXiv:2007.00808 (2020). [89] Junhan Yang, Zheng Liu, Chaozhuo Li, Guangzhong Sun, and Xing Xie. 2023. Longtriever: a pre-trained long text encoder for dense document retrieval. In Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing. 3655–3665. [90] Shengbin Yue, Wei Chen, Siyuan Wang, Bingxuan Li, Chenchen Shen, Shujun Liu, Yuxuan Zhou, Yao Xiao, Song Yun, Xuanjing Huang, et al. 2023.

**中文**

[88] Lee Xiong、Chenyan Xiong、Ye Li、Kwok-Fung Tang、Jialin Liu、Paul Bennett、Junaid Ahmed 和 Arnold Overwijk。 2020.用于密集文本检索的近似最近邻负对比学习。 arXiv 预印本 arXiv:2007.00808 (2020)。 [89] 杨俊瀚，刘峥，李超卓，孙光中，谢兴。 2023. Longtriever：用于密集文档检索的预训练长文本编码器。 2023 年自然语言处理经验方法会议论文集。 3655–3665。 [90] 岳胜斌，陈伟，王思源，李冰轩，沉晨晨，刘淑君，周宇轩，肖姚，宋赟，黄轩静，等。 2023 年。

### 段落 231 · Page 31

**EN**

Disc-lawllm: Fine-tuning large language models for intelligent legal services. arXiv preprint arXiv:2309.11325 (2023). [91] Manzil Zaheer, Guru Guruganesh, Avinava Dubey, Joshua Ainslie, Chris Alberti, Santiago Ontanón, Philip Pham, Anirudh Ravula, Qifan Wang, Li Yang, and Amr Ahmed. 2020. Big Bird: Transformers for Longer Sequences.arXiv preprint arXiv:2007.14062 (2020). https://arxiv.org/abs/2007.14062 [92] Manzil Zaheer, Guru Guruganesh, Kumar Avinava Dubey, Joshua Ainslie, Chris Alberti, Santiago Ontanon, Philip Pham, Anirudh Ravula, Qifan Wang, Li Yang, et al. 2020. Big bird: Transformers for longer sequences.

**中文**

Disc-lawllm：微调大型语言模型以提供智能法律服务。 arXiv 预印本 arXiv:2309.11325 (2023)。 [91] Manzil Zaheer、Guru Guruganesh、Avinava Dubey、Joshua Ainslie、Chris Alberti、Santiago Ontanón、Philip Pham、Anirudh Ravula、Qifan Wang、Li Yang 和 Amr Ahmed。 2020. 大鸟：更长序列的变形金刚.arXiv 预印本 arXiv:2007.14062 (2020)。 https://arxiv.org/abs/2007.14062 [92] Manzil Zaheer、Guru Guruganesh、Kumar Avinava Dubey、Joshua Ainslie、Chris Alberti、Santiago Ontanon、Philip Pham、Anirudh Ravula、Qifan Wang、Li Yang 等。 2020. 大鸟：更长序列的变形金刚。

### 段落 232 · Page 31

**EN**

Advances in neural information processing systems 33 (2020), 17283–17297. [93] Xin Zhang, Yanzhao Zhang, Dingkun Long, Wen Xie, Ziqi Dai, Jialong Tang, Huan Lin, Baosong Yang, Pengjun Xie, Fei Huang, Meishan Zhang, Wenjie Li, and Min Zhang. 2024. mGTE: Generalized Long-Context Text Representation and Reranking Models for Multilingual Text Retrieval. arXiv:2407.19669 [cs.CL] https://arxiv.org/abs/2407.19669

**中文**

神经信息处理系统的进展 33 (2020), 17283–17297。 [93] 张鑫，张艳照，龙定坤，谢文，戴子奇，唐家龙，林焕，杨宝松，谢鹏军，黄飞，张美山，李文杰，张敏。 2024. mGTE：用于多语言文本检索的广义长上下文文本表示和重排序模型。 arXiv:2407.19669 [cs.CL] https://arxiv.org/abs/2407.19669

### Page 32

### 段落 233 · Page 32

**EN**

32 Li et al. [94] Yunyi Zhang, Ruozhen Yang, Siqi Jiao, SeongKu Kang, and Jiawei Han. 2025. Scientific Paper Retrieval with LLM-Guided Semantic-Based Ranking. arXiv:2505.21815 [cs.IR] https://arxiv.org/abs/2505.21815 [95] Yujia Zhou, Zhicheng Dou, Huaying Yuan, and Zhengyi Ma. 2022. Socialformer: Social network inspired long document modeling for document ranking. In Proceedings of the ACM Web Conference 2022. 339–347. [96] Zhi Zhou, Jiang-Xin Shi, Peng-Xiao Song, Xiao-Wen Yang, Yi-Xuan Jin, Lan-Zhe Guo, and Yu-Feng Li. 2024. Lawgpt: A chinese legal knowledgeenhanced large language model. arXiv preprint arXiv:2406.04614 (2024).

**中文**

32 李等人。 [94] 张云逸，杨若真，焦思琪，康圣库，韩家伟。 2025. 法学硕士引导的基于语义的排序的科学论文检索。 arXiv:2505.21815 [cs.IR] https://arxiv.org/abs/2505.21815 [95] 周宇佳、窦志成、袁华英和马正毅。 2022. Socialformer：社交网络启发了用于文档排名的长文档建模。 2022 年 ACM 网络会议论文集。339-347。 [96]周志，石江新，宋鹏晓，杨晓文，金艺轩，郭兰哲，李玉峰。 2024.Lawgpt：中国法律知识增强大语言模型。 arXiv 预印本 arXiv:2406.04614 (2024)。

### 段落 234 · Page 32

**EN**

[97] Dawei Zhu, Liang Wang, Nan Yang, Yifan Song, Wenhao Wu, Furu Wei, and Sujian Li. 2024. LongEmbed: Extending Embedding Models for Long Context Retrieval. arXiv:2404.12096 [cs.CL] https://arxiv.org/abs/2404.12096 [98] Yutao Zhu, Huaying Yuan, Shuting Wang, Jiongnan Liu, Wenhan Liu, Chenlong Deng, Haonan Chen, Zheng Liu, Zhicheng Dou, and Ji-Rong Wen. 2023. Large language models for information retrieval: A survey. arXiv preprint arXiv:2308.07107 (2023).

**中文**

[97] 朱大为，王亮，杨南，宋一凡，吴文浩，魏福如，李素健。 2024.LongEmbed：扩展长上下文检索的嵌入模型。 arXiv:2404.12096 [cs.CL] https://arxiv.org/abs/2404.12096 [98] Yutao Zhu、Huaying Yuan、Shuting Wang、Jionongnan Liu、Wenhan Liu、Chenlong Deng、Haonan Chen、Zheng Liu、Zhi Cheng Dou 和 Ji-Rong Wen。 2023. 用于信息检索的大型语言模型：一项调查。 arXiv 预印本 arXiv:2308.07107 (2023)。
