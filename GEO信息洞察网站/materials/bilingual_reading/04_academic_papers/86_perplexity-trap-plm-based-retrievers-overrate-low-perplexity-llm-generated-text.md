# Perplexity Trap: PLM-Based Retrievers Overrate Low-Perplexity LLM-Generated Text

- ID: 86
- 类型: pdf
- 分类: 04_academic_papers
- 主题: retriever source bias toward LLM-generated content
- 原文链接: https://arxiv.org/pdf/2503.08684
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

Published as a conference paper at ICLR 2025 PERPLEXITY -T RAP : PLM-B ASED RETRIEVERS OVERRATE LOW PERPLEXITY DOCUMENTS Haoyu Wang1∗, Sunhao Dai 1∗, Haiyuan Zhao 1, Liang Pang 2, Xiao Zhang 1 Gang Wang3, Zhenhua Dong 3, Jun Xu 1†, Ji-Rong Wen1 1Gaoling School of Artificial Intelligence, Renmin University of China, Beijing, China 2CAS Key Laboratory of AI Safety, Institute of Computing Technology, Beijing, China 3Huawei Noah’s Ark Lab, Shenzhen, China {wanghaoyu0924,sunhaodai,junxu}@ruc.edu.cn, ABSTRACT Previous studies have found that PLM-based retrieval models exhibit a preference for LLM-generated content, assigning higher relevance scores to these documents even when their semantic quality is comparable to human-written ones.

**中文**

以会议论文形式发表在 ICLR 2025 PERPLEXITY -T RAP : PLM-B ASED RETRIEVERS OVERRATE LOW PERPLEXITY DOCUMENTShaoyu Wang1*, Sunhao Dai 1*, Haiyuan Zhao 1, Liang Pang 2, Xiao Zhang 1 Gang Wang3, Zhunhua Dong 3, Jun Xu 1†, Ji-Rong Wen1 1中国人民大学高岭人工智能学院,北京，中国 2中国科学院计算技术研究所人工智能安全重点实验室，中国北京 3华为诺亚方舟实验室，中国深圳 {wanghaoyu0924,sunhaodai,junxu}@ruc.edu.cn, 摘要 先前的研究发现，基于 PLM 的检索模型表现出对 LLM 生成内容的偏好，为这些文档分配更高的相关性分数，即使这些文档的语义质量与人类编写的文档相当。

### 段落 2 · Page 1

**EN**

This phenomenon, known as source bias, threatens the sustainable development of the information access ecosystem. However, the underlying causes of source bias remain unexplored. In this paper, we explain the process of information retrieval with a causal graph and discover that PLM-based retrievers learn perplexity features for relevance estimation, causing source bias by ranking the documents with low perplexity higher. Theoretical analysis further reveals that the phenomenon stems from the positive correlation between the gradients of the loss functions in language modeling task and retrieval task.

**中文**

这种现象被称为来源偏差，威胁着信息获取生态系统的可持续发展。然而，来源偏差的根本原因仍未得到探索。在本文中，我们用因果图解释了信息检索的过程，并发现基于 PLM 的检索器学习用于相关性估计的困惑度特征，通过将低困惑度的文档排名较高而导致来源偏差。理论分析进一步揭示，这种现象源于语言建模任务和检索任务中损失函数的梯度之间的正相关性。

### 段落 3 · Page 1

**EN**

Based on the analysis, a causal-inspired inferencetime debiasing method is proposed, called Causal Diagnosis and Correction (CDC). CDC first diagnoses the bias effect of the perplexity and then separates the bias effect from the overall estimated relevance score. Experimental results across three domains demonstrate the superior debiasing effectiveness of CDC, emphasizing the validity of our proposed explanatory framework 1.

**中文**

基于分析，提出了一种受因果启发的推理时间去偏差方法，称为因果诊断和纠正（CDC）。 CDC 首先诊断困惑的偏差效应，然后将偏差效应与总体估计的相关性得分分开。三个领域的实验结果证明了 CDC 卓越的去偏有效性，强调了我们提出的解释框架 1 的有效性。

### 段落 4 · Page 1

**EN**

1 I NTRODUCTION The rapid advancement of large language models (LLMs) has driven a significant increase in AIgenerated content (AIGC), leading to information retrieval (IR) systems that now index both humanwritten and LLM-generated contents (Cao et al., 2023; Dai et al., 2024b; 2025). However, recent studies (Dai et al., 2024a;c; Xu et al., 2024) have uncovered that Pretrained Language Model (PLM) based retrievers (Guo et al., 2022; Zhao et al., 2024) exhibit preferences for LLM-generated documents, ranking them higher even when their semantic quality is comparable to human-written content.

**中文**

1 简介 大语言模型 (LLM) 的快速发展推动了人工智能生成内容 (AIGC) 的显着增加，导致信息检索 (IR) 系统现在可以索引人类书写和 LLM 生成的内容（Cao 等人，2023；Dai 等人，2024b；2025）。然而，最近的研究（Dai 等人，2024a;c；Xu 等人，2024）发现，基于预训练语言模型（PLM）的检索器（Guo 等人，2022；Zhao 等人，2024）表现出对 LLM 生成文档的偏好，即使它们的语义质量与人类编写的内容相当，它们也会对它们排名更高。

### 段落 5 · Page 1

**EN**

This phenomenon, referred to as source bias, is prevalent among various popular PLM-based retrievers across different domains (Dai et al., 2024a). If the problem is not resolved promptly, human authors’ creative willingness will be severely reduced, and the existing content ecosystem may collapse. So it’s urgent to comprehensively understand the mechanism behind source bias, especially when the amount of online AIGC is rapidly increasing (Burtch et al., 2024; Liu et al., 2024).

**中文**

这种现象被称为源偏差，在不同领域的各种流行的基于 PLM 的检索器中普遍存在（Dai 等人，2024a）。如果问题不及时解决，人类作者的创作意愿将严重降低，现有的内容生态系统可能会崩溃。因此，迫切需要全面了解来源偏差背后的机制，尤其是当在线 AIGC 的数量迅速增加时（Burtch et al., 2024；Liu et al., 2024）。

### 段落 6 · Page 1

**EN**

Existing studies identify perplexity (PPL) as a key indicator for distinguishing between LLMgenerated and human-written contents (Mitchell et al., 2023; Bao et al., 2023). Dai et al. (2024c) find that although the semantics of the text remain unchanged, LLM-rewritten documents possess much lower perplexity than their human-written counterparts. However, it’s still unclearwhether document perplexity has a causal impact on the relevance score estimation of PLM-based retrievers (which may lead to source bias), and if so, why such causal impact exists.

**中文**

现有研究将困惑度（PPL）确定为区分 LLM 生成的内容和人类编写的内容的关键指标（Mitchell 等人，2023；Bao 等人，2023）。戴等人。 (2024c) 发现，尽管文本的语义保持不变，但法学硕士重写的文档比人类编写的文档具有更低的复杂性。然而，目前尚不清楚文档的复杂性是否对基于 PLM 的检索器的相关性得分估计有因果影响（这可能导致来源偏差），如果有，为什么会存在这种因果影响。

### 段落 7 · Page 1

**EN**

In this paper, we delve deeper into the cause of source bias by examining the role of perplexity in PLM-based retrievers. By manipulating sampling temperature when generating with LLMs, we ∗Equal contributions. †Corresponding author. 1Codes are available at https://github.com/WhyDwelledOnAi/Perplexity-Trap. 1 arXiv:2503.08684v1 [cs.CL] 11 Mar 2025

**中文**

在本文中，我们通过研究困惑度在基于 PLM 的检索器中的作用，更深入地探讨了来源偏差的原因。通过在使用 LLM 生成时操纵采样温度，我们 * 做出了平等的贡献。 †通讯作者。 1代码可从 https://github.com/WhyDwelledOnAi/Perplexity-Trap 获取。 1 arXiv:2503.08684v1 [cs.CL] 2025 年 3 月 11 日

### Page 2

### 段落 8 · Page 2

**EN**

Published as a conference paper at ICLR 2025 observe a negative correlation between estimated relevance scores and perplexity. Inspired by this, we construct a causal graph where document perplexity plays as a treatment and document semantic plays as a confounder (Figure 2). We adopt a two-stage least squares (2SLS) regression procedure (Angrist and Pischke, 2009; Hartford et al., 2017) to eliminate the influence of confounders when estimating this biased effect, the experimental results indicate the effect is significantly negative.

**中文**

作为 ICLR 2025 会议论文发表，观察到估计相关性分数与困惑度之间存在负相关性。受此启发，我们构建了一个因果图，其中文档困惑度充当处理方法，文档语义充当混杂因素（图 2）。我们采用两阶段最小二乘（2SLS）回归程序（Angrist and Pischke，2009；Hartford et al.，2017）来消除估计这种偏差效应时混杂因素的影响，实验结果表明该效应显着为负。

### 段落 9 · Page 2

**EN**

Based on these findings, the cause of source bias can be elucidated as the unexpected causal effect of perplexity on estimated relevance scores. For semantically identical documents, the documents with low perplexity causally get higher estimated relevance scores from PLM-based retrievers. Since LLM-generated documents typically have lower perplexity than human-written ones, they receive higher estimated relevance scores and are ranked higher, leading to the presence of source bias.

**中文**

基于这些发现，来源偏差的原因可以被阐明为困惑对估计相关性分数的意外因果影响。对于语义相同的文档，具有低困惑度的文档会从基于 PLM 的检索器中获得更高的估计相关性分数。由于法学硕士生成的文档通常比人工编写的文档具有更低的复杂性，因此它们获得更高的估计相关性分数并且排名更高，从而导致存在来源偏差。

### 段落 10 · Page 2

**EN**

To further understand why estimated relevance scores of PLM-based retrievers are influenced by perplexity, we provide a theoretical analysis for the overlap between masked language modeling (MLM) task and mean-pooling retrieval task. Analysis in the linear decoder scenario shows that, the retrieval objective’s gradients are positively correlated to the language modeling gradients. This correlation causes the retrievers to consider not only the document semantics required for retrieval but also the bias introduced by perplexity.

**中文**

为了进一步理解为什么基于 PLM 的检索器的估计相关性分数会受到困惑度的影响，我们对掩码语言建模 (MLM) 任务和均值池检索任务之间的重叠进行了理论分析。线性解码器场景的分析表明，检索目标的梯度与语言建模梯度正相关。这种相关性使得检索器不仅要考虑检索所需的文档语义，还要考虑因困惑而引入的偏差。

### 段落 11 · Page 2

**EN**

Meanwhile, this correlation further explains the trade-off between retrieval performance and source bias observed in previous study (Dai et al., 2024a): the stronger the ranking performance of the PLM-based retrievers, the greater the impact of perplexity. Based on the analysis, we propose an inference-time debiasing method calledCDC (Causal Diagnosis and Correction). With the proposed causal graph, we separate the causal effect of perplexity from the overall estimated relevance scores during inference, achieving calibrated unbiased relevance scores.

**中文**

同时，这种相关性进一步解释了先前研究中观察到的检索性能和来源偏差之间的权衡（Dai et al., 2024a）：基于 PLM 的检索器的排名性能越强，困惑度的影响就越大。基于分析，我们提出了一种称为 CDC（因果诊断和纠正）的推理时间去偏差方法。通过所提出的因果图，我们在推理过程中将困惑度的因果效应与总体估计的相关性得分分开，从而实现了校准的无偏相关性得分。

### 段落 12 · Page 2

**EN**

Specifically, CDC first estimates the biased causal effect of perplexity on a small set of training samples, which is then applied to de-bias the test samples at the inference stage. This debiasing process is inference-time and can be seamlessly integrated into existing trained PLM-based retrievers. We demonstrate the debiasing effectiveness of CDC with experiments across six popular PLM-based retrievers. Experimental results show that the estimated causal effect of perplexity can be generalized to other data domains and LLMs, highlighting its practical potential in eliminating source bias.

**中文**

具体来说，CDC首先估计一小组训练样本上的困惑度的有偏因果效应，然后在推理阶段将其应用于测试样本的去偏。该去偏过程是推理时间的，可以无缝集成到现有的经过训练的基于 PLM 的检索器中。我们通过六种流行的基于 PLM 的检索器的实验证明了 CDC 的去偏有效性。实验结果表明，困惑度的估计因果效应可以推广到其他数据领域和法学硕士，突出了其在消除源偏差方面的实际潜力。

### 段落 13 · Page 2

**EN**

We summarize the major contributions of this paper as follows: • We construct a causal graph and estimate the causal effect through experiments, demonstrating that PLM-based retrievers causally assign higher relevance scores to documents with lower perplexity, which is the cause of source bias. • We provide a theoretical analysis explaining that the effect of perplexity in PLM-based retrievers is due to the positive correlation between objective gradients of retrieval and language modeling.

**中文**

我们总结本文的主要贡献如下： • 我们构建了因果图，并通过实验估计了因果效应，证明基于 PLM 的检索器会为具有较低困惑度的文档分配较高的相关性分数，这是来源偏差的原因。 • 我们提供了理论分析，解释了基于 PLM 的检索器中困惑度的影响是由于检索的客观梯度和语言建模之间的正相关性所致。

### 段落 14 · Page 2

**EN**

• We propose CDC for PLM-based retrievers to counteract the biased effect of perplexity, with experiments demonstrating its effectiveness and generalizability in eliminating source bias. 2 R ELATED WORK With the rapid development of LLMs (Zhao et al., 2023), the internet has quickly integrated a huge amount of AIGC (Cao et al., 2023; Dai et al., 2024b; 2025). Potential bias may occur when these generated contents are judged by neural networks as a competitor together with human works. For example, Dai et al.

**中文**

• 我们建议基于PLM 的检索器使用CDC 来抵消困惑的偏差影响，并通过实验证明其在消除源偏差方面的有效性和普遍性。 2 相关工作随着LLM的快速发展(Zhao et al., 2023)，互联网迅速整合了大量的AIGC(Cao et al., 2023; Dai et al., 2024b; 2025)。当这些生成的内容被神经网络判断为与人类作品一起竞争时，可能会出现潜在的偏差。例如，戴等人。

### 段落 15 · Page 2

**EN**

(2024c) are the first to highlight a paradigm shift in information retrieval (IR): the content indexed by IR systems is transitioning from exclusively human-written corpora to a coexistence of human-written and LLM-generated corpora. They then uncover an important finding that mainstream neural retrievers based on pretrained language models (PLMs) prefer LLM-generated content, a phenomenon termed source bias (Dai et al., 2024a;c). Xu et al.

**中文**

(2024c) 是第一个强调信息检索 (IR) 范式转变的人：IR 系统索引的内容正在从完全由人类编写的语料库过渡到人类编写的语料库和法学硕士生成的语料库并存。然后，他们发现了一个重要发现，即基于预训练语言模型 (PLM) 的主流神经检索器更喜欢 LLM 生成的内容，这种现象称为来源偏差 (Dai et al., 2024a;c)。徐等人。

### 段落 16 · Page 2

**EN**

(2024) further discover that this bias extends to text-image retrieval, and similarly, other works further observe the existence of source bias in other IR scenarios, such as recommender systems (RS) (Zhou et al., 2024), retrievalaugmented generation (RAG) (Chen et al., 2024) and question answering (QA) (Tan et al., 2024). In the context of LLMs-as-judges, similar bias is discovered as self-enhancement bias (Zheng et al., 2024), likelihood bias (Ohi et al., 2024), and familiarity bias (Stureborg et al., 2024), where LLM overates AIGC when serving as a judge.

**中文**

（2024）进一步发现这种偏差扩展到文本图像检索，类似地，其他工作进一步观察了其他 IR 场景中源偏差的存在，例如推荐系统（RS）（Zhou 等人，2024）、检索增强生成（RAG）（Chen 等人，2024）和问题回答（QA）（Tan 等人，2024）。在法学硕士担任法官的背景下，类似的偏见被发现为自我增强偏见（Zheng et al., 2024）、可能性偏见（Ohi et al., 2024）和熟悉性偏见（Stureborg et al., 2024），其中法学硕士在担任法官时夸大了 AIGC。

### 段落 17 · Page 2

**EN**

Existing works provide intuitive explanations suggesting that this kind of bias may stem from coupling between neural judges and LLMs (Dai et al., 2024c; Xu et al., 2024), such as similarities in model 2

**中文**

现有的工作提供了直观的解释，表明这种偏差可能源于神经法官和法学硕士之间的耦合（Dai et al., 2024c; Xu et al., 2024），例如模型 2 中的相似之处

### Page 3

### 段落 18 · Page 3

**EN**

Published as a conference paper at ICLR 2025 /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017/uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001a/uni00000016/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000017/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000018/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000019/uni00000013 /uni0000001

**中文**

作为会议论文发表在 ICLR 2025 /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017 /uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001a/uni00000016/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000017/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000018/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000019/uni00000013 /uni0000001

### 段落 19 · Page 3

**EN**

4/uni00000011/uni0000001a/uni0000001a/uni00000013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000018/uni0000001a/uni00000013 /uni00000013/uni00000011/uni00000018/uni0000001a/uni00000016 /uni00000013/uni00000011/uni00000018/uni0000001a/uni00000019 /uni00000013/uni00000011/uni00000018/uni0000001a/uni0000001c /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni000

**中文**

4/uni00000011/uni0000001a/uni0000001a/uni00000013/uni00000033/uni00000048/uni0000005 5/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000018/uni0000001a/uni00000013 /uni00000013/uni00000011/uni00000018/uni0000001a/uni00000016 /uni00000013/uni00000011/uni00000018/uni0000001a/uni00000019 /uni00000013/uni00000011/uni00000018/uni0000001a/uni0000001c /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni000

### 段落 20 · Page 3

**EN**

00003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni00000011/uni0000001c/uni0000001c /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (a) DL19 /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000

**中文**

00003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00 000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049 /uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni00 00001d/uni00000003/uni00000010/uni00000013/uni00000011/uni0000001c/uni0000001c /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (a) DL19 /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000

### 段落 21 · Page 3

**EN**

013/uni00000011/uni00000017/uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni00000019/uni00000013/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000015/uni00000013 /uni00000014/uni00000011/uni00000019/uni00000016/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000018/uni00000013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni0

**中文**

013/uni00000011/uni00000017/uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni00000019/uni00000013/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000015/uni00000013 /uni00000014/uni00000011/uni00000019/uni00000016/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000018/uni00000013/uni00000033/uni00000048/uni00 000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni0

### 段落 22 · Page 3

**EN**

0000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni0000001c/uni0000001a/uni00000013 /uni00000013/uni00000011/uni0000001c/uni0000001a/uni00000018 /uni00000013/uni00000011/uni0000001c/uni0000001b/uni00000013 /uni00000013/uni00000011/uni0000001c/uni0000001b/uni00000018 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/

**中文**

0000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni0000001c/uni0000001a/uni00000013 /uni00000013/uni00000011/uni0000001c/uni0000001a/uni00000018 /uni00000013/uni00000011/uni0000001c/uni0000001b/uni00000013 /uni00000013/uni00000011/uni0000001c/uni0000001b/uni00000018 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/

### 段落 23 · Page 3

**EN**

uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni00000011/uni0000001c/uni00000014 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (b) TREC-COVID /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017/uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000

**中文**

uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051 /uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni00000011/uni0000001c/uni00000014 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (b) TREC-新冠肺炎/uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017 /uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000

### 段落 24 · Page 3

**EN**

053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001c/uni00000019/uni00000013 /uni00000014/uni00000011/uni0000001c/uni0000001b/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000013/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000015/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000017/uni00000013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni

**中文**

053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001c/uni00000019/uni00000013 /uni00000014/uni00000011/uni0000001c/uni0000001b/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000013/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000015/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000017/uni00000013/uni00000033/uni00000048/uni00 000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni

### 段落 25 · Page 3

**EN**

00000011/uni00000019/uni0000001a/uni00000013 /uni00000013/uni00000011/uni00000019/uni0000001b/uni00000013 /uni00000013/uni00000011/uni00000019/uni0000001c/uni00000013 /uni00000013/uni00000011/uni0000001a/uni00000013/uni00000013 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/

**中文**

00000011/uni00000019/uni0000001a/uni00000013/uni00000013/uni00000011/uni00000019/uni0000001b/uni00000013 /uni00000013/uni00000011/uni00000019/uni0000001c/uni00000013 /uni00000013/uni00000011/uni0000001a/uni00000013/uni00000013 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052 /uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/

### 段落 26 · Page 3

**EN**

uni00000003/uni00000010/uni00000013/uni00000011/uni0000001b/uni00000016 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (c) SCIDOCS Figure 1: Perplexity and estimated relevance scores of ANCE on positive query-document pairs in three dataset, where documents are generated by LLM rewriting with different sampling temperatures.

**中文**

uni00000003/uni00000010/uni00000013/uni00000011/uni0000001b/uni00000016 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (c) SCIDOCS 图 1：三个数据集中的正查询文档对的 ANCE 的困惑度和估计相关性得分，其中文档是通过使用不同采样温度的 LLM 重写生成的。

### 段落 27 · Page 3

**EN**

The Pearson coefficients highlight the significant negative correlation between the two variables. architectures and training objectives. However, the specific nature of this coupling, how it operates to cause source bias, and why it exists remains unclear. Ohi et al. (2024) find the correlation between perplexity and bias, while our work is the first to systematically analyze the effect of perplexity for neural models’ preference. Given that both PLMs and LLMs are highly complex neural network models, investigating this question is particularly challenging and difficult.

**中文**

皮尔逊系数突出了两个变量之间的显着负相关性。架构和培训目标。然而，这种耦合的具体性质、它如何导致源偏差以及它存在的原因仍不清楚。奥伊等人。 （2024）发现困惑度和偏差之间的相关性，而我们的工作是第一个系统分析困惑度对神经模型偏好的影响的工作。鉴于 PLM 和 LLM 都是高度复杂的神经网络模型，研究这个问题尤其具有挑战性和困难。

### 段落 28 · Page 3

**EN**

3 E LUCIDATING SOURCE BIAS WITH CAUSAL GRAPH This section first conducts intervention experiments to illustrate the motivation. Subsequently, we construct a causal graph to explain source bias and demonstrate the rationality of the causal graph. 3.1 M OTIVATION : I NTERVENTION EXPERIMENTS ON TEMPERATURE Previous studies have revealed a significant difference in the perplexity (PPL) distribution between LLM-generated content and human-written content (Mitchell et al., 2023; Bao et al., 2023), suggesting that PPL might be a key indicator for analyzing the cause of source bias (Dai et al., 2024c).

**中文**

3 用因果图阐明源偏差本节首先进行干预实验来说明动机。随后，我们构建了一个因果图来解释源偏差并证明因果图的合理性。 3.1 动机：温度干预实验 先前的研究表明，LLM 生成的内容与人类编写的内容之间的困惑度（PPL）分布存在显着差异（Mitchell 等，2023；Bao 等，2023），这表明 PPL 可能是分析来源偏差原因的关键指标（Dai 等，2024c）。

### 段落 29 · Page 3

**EN**

To verify whether perplexity causally affects estimated relevance scores, we use LLMs (in following chapters the LLMs we use are Llama2-7B-chat (Touvron et al., 2023) unless emphasized) to generate documents with almost identical semantics but varying perplexity, where semantics are expected as the only associated variable when retrieval. Specifically, we manipulate the sampling temperatures during generation to obtain LLM-generated documents with different PPLs but similar semantic content. Following the method of Dai et al. (2024c), we use the following simple prompt: “Please rewrite the following text: {human-written text}”.

**中文**

为了验证困惑度是否会因果影响估计的相关性分数，我们使用LLM（在接下来的章节中，除非强调，我们使用的LLM是Llama2-7B-chat（Touvron等人，2023））来生成具有几乎相同语义但不同困惑度的文档，其中语义被期望作为检索时唯一的关联变量。具体来说，我们在生成过程中操纵采样温度，以获得具有不同 PPL 但相似语义内容的 LLM 生成的文档。遵循戴等人的方法。 (2024c)，我们使用以下简单提示：“请重写以下文本：{人类编写的文本}”。

### 段落 30 · Page 3

**EN**

We also recruit human annotators to conduct evaluations to ensure the quality of the generated LLM content. The results, shown in Appendix E.2.1, indicate that there are fewer quality discrepancies between documents generated at different sampling temperatures compared to the original humanwritten documents. This ensures the reliability of the subsequent experiments. We then explore the relationship between perplexity and estimated relevance scores on the corpora generated with different temperatures, where perplexity is calculated by BERT masked language modelling following previous work (Dai et al., 2024c).

**中文**

我们还聘请人工注释者进行评估，以确保生成的法学硕士内容的质量。附录 E.2.1 中显示的结果表明，与原始的人工书写文档相比，在不同采样温度下生成的文档之间的质量差异较小。这保证了后续实验的可靠性。然后，我们探索了不同温度下生成的语料库的困惑度和估计相关性分数之间的关系，其中困惑度是根据之前的工作通过 BERT 掩码语言模型计算的（Dai 等人，2024c）。

### 段落 31 · Page 3

**EN**

Figure 1 presents the average perplexity and estimated relevance scores by ANCE across three datasets from different domains. As expected, lower sampling temperatures result in less randomness in LLM-generated content and thus lower PPL. Meanwhile, we find that documents generated with lower temperatures were also more likely to be assigned higher estimated relevance scores. The Pearson coefficients for the three datasets are all below -0.8, emphasizing the strong negative linear correlation between document perplexity and relevance score. Similar results for other PLM-based retrievers are provided in Appendix E.2.2.

**中文**

图 1 显示了 ANCE 在来自不同领域的三个数据集上的平均困惑度和估计的相关性得分。正如预期的那样，较低的采样温度会导致 LLM 生成内容的随机性较小，从而降低 PPL。同时，我们发现在较低温度下生成的文档也更有可能被分配更高的估计相关性分数。三个数据集的 Pearson 系数均低于 -0.8，强调文档困惑度和相关性得分之间存在很强的负线性相关性。附录 E.2.2 中提供了其他基于 PLM 的检索器的类似结果。

### 段落 32 · Page 3

**EN**

Since document semantics remain unchanged during rewriting, the synchronous variation between document perplexity and estimated relevance scores reflects a causal effect. These findings offer an intuitive explanation for source bias: LLM-generated content typically has lower PPL, and since documents with lower perplexity are more likely to receive higher relevance scores, LLM-generated content is more likely to be ranked highly, leading to source bias. 3

**中文**

由于文档语义在重写期间保持不变，因此文档困惑度和估计相关性分数之间的同步变化反映了因果效应。这些发现为来源偏差提供了直观的解释：LLM 生成的内容通常具有较低的 PPL，并且由于困惑度较低的文档更有可能获得较高的相关性分数，LLM 生成的内容更有可能排名靠前，从而导致来源偏差。 3

### Page 4

### 段落 33 · Page 4

**EN**

Published as a conference paper at ICLR 2025 3.2 C AUSAL GRAPH FOR SOURCE BIAS Inspired by the findings above, we propose a causal graph to elucidate source bias (Fan et al., 2022), as illustrated in Figure 2. Let Q denotes the query set and C denote the corpus. During the inference stage for a certain PLM-based retriever, given a queryq ∈ Q and a document d ∈ C , the estimated relevance score ˆRq,d ∈ R is simultaneously determined by both the golden relevance scoreRq,d ∈ R and document perplexity Pd ∈ R +.

**中文**

作为 ICLR 2025 的会议论文发表 3.2 C AUSAL GRAPH FOR SOURCE BIAS 受上述发现的启发，我们提出了一个因果图来阐明源偏差（Fan et al., 2022），如图 2 所示。设 Q 表示查询集，C 表示语料库。在某个基于 PLM 的检索器的推理阶段，给定查询 q ∈ Q 和文档 d ∈ C，估计的相关性得分 ˆRq,d ∈ R 同时由黄金相关性得分 Rq,d ∈ R 和文档困惑度 Pd ∈ R + 确定。

### 段落 34 · Page 4

**EN**

Note that the fundamental goal of IR is to calculate the similarity between document semantics Md and query semantics Mq for document ranking, Rq,d → ˆRq,d is considered an unbiased effect, while the influence of Pd → ˆRq,d is considered as a biased effect. Subsequently, we explain the rationale behind each edge in the causal graph as follows: 𝑀𝑑 Source Document Semantic Perplexity Bias Effect Query Semantic Estimated Relevance Score 𝑆𝑑 𝑀𝑞 𝑃𝑑 𝑅𝑞,𝑑 𝑆𝑑 Source Document Semantic Perplexity Query Semantic Estimated Relevance Score 𝑀𝑑 𝑀𝑞 𝑃𝑑 Golden Relevance Score 𝑅𝑞,𝑑 ෠𝑅𝑞,𝑑 Figure 2: The proposed causal graph for explaining source bias.

**中文**

请注意，IR 的根本目标是计算文档语义 Md 和查询语义 Mq 之间的相似度以进行文档排序，Rq,d → ˆRq,d 被认为是无偏效应，而 Pd → ˆRq,d 的影响被认为是有偏效应。随后，我们解释因果图中每条边背后的基本原理如下： 源文档语义困惑偏差效应查询语义估计相关性分数估计相关性得分 𝑀𝑑 𝑀𝑞 𝑃𝑑 黄金相关性得分 𝑅𝑞,𝑑 ෠𝑅𝑞,𝑑 图 2：用于解释源偏差的拟议因果图。

### 段落 35 · Page 4

**EN**

First, let the document source Sd is a binary variable where Sd = 1 denotes the document is generated by LLM and Sd = 0 denotes the document is written by human. As suggested in (Dai et al., 2024c), LLMgenerated documents through rewriting possess lower perplexity than their original documents, even though there is no significant difference in their semantic content. Thus, an edge Sd → Pd exists. This phenomenon can be attributed to two main reasons: (1) Sampling strategies aimed at probability maximization, such as greedy algorithms, discard long-tailed documents during LLM inference.

**中文**

首先，让文档来源Sd是一个二进制变量，其中Sd = 1表示该文档是由LLM生成的，Sd = 0表示该文档是由人编写的。正如 (Dai et al., 2024c) 中所建议的，LLM 通过重写生成的文档比原始文档具有更低的复杂性，即使它们的语义内容没有显着差异。因此，存在边Sd→Pd。这种现象主要有两个原因：（1）以概率最大化为目标的采样策略，例如贪心算法，在LLM推理过程中丢弃长尾文档。

### 段落 36 · Page 4

**EN**

More detailed analysis and verification can be found in (Dai et al., 2024c). (2) Approximation error during LLM training causes the tails of the document distribution to be lost (Shumailov et al., 2023). Next, the document semantics Md reflect the topics of the document d, including domain, events, sentiment information, and so on. Since documents with different semantic meanings convey different amounts of information, their difficulties in masked token prediction vary. This means that different document semantics lead to different document perplexities.

**中文**

更详细的分析和验证可以参见（Dai et al., 2024c）。 （2）LLM训练过程中的近似误差导致文档分布的尾部丢失（Shumailov et al., 2023）。接下来，文档语义Md反映了文档d的主题，包括领域、事件、情感信息等。由于不同语义的文档传达的信息量不同，因此它们在掩码标记预测中的难度也有所不同。这意味着不同的文档语义会导致不同的文档困惑。

### 段落 37 · Page 4

**EN**

For example, colloquial conversations are more predictable than research papers due to their less specialized vocabulary. Thus, the content directly affects the perplexity, establishing the edge Md → Pd. Finally, as retrieval models are trained to estimate ground-truth relevance, their outputs are valid approximations of the golden relevance scores, making Md → Rq,d ← Mq a natural unbiased effect. However, retrieval models may also learn non-causal features unrelated to semantic matching, especially high-dimensional features in deep learning.

**中文**

例如，口语对话比研究论文更容易预测，因为它们的专业词汇较少。因此，内容直接影响困惑度，建立边Md→Pd。最后，当训练检索模型来估计真实相关性时，它们的输出是黄金相关性分数的有效近似值，使得 Md → Rq,d ← Mq 成为自然的无偏效应。然而，检索模型也可能学习与语义匹配无关的非因果特征，尤其是深度学习中的高维特征。

### 段落 38 · Page 4

**EN**

According to findings in Section 3.1, document perplexity Pd has emerged as a potential non-causal feature learned by PLM-based retrievers, where higher relevance estimations coincide with lower document perplexity. Moreover, Since document perplexity is determined at the time of document generation, which temporally predates the existence of estimated relevance scores, document perplexity should be a cause rather than a consequence of changes in relevance. Hence, a biased effect of Pd → ˆRq,d exists.

**中文**

根据第 3.1 节的发现，文档困惑度 Pd 已成为基于 PLM 的检索器学习的潜在非因果特征，其中较高的相关性估计与较低的文档困惑度相一致。此外，由于文档困惑度是在文档生成时确定的，这在时间上早于估计相关性分数的存在，因此文档困惑度应该是相关性变化的原因而不是结果。因此，存在 Pd → ˆRq,d 的偏置效应。

### 段落 39 · Page 4

**EN**

3.3 E XPLAINING SOURCE BIAS VIA THE PROPOSED CAUSAL GRAPH Based on the causal graph constructed above, source bias can be explained as follows: Although the content generated by LLMs retains similar semantics to the human-written content, LLM-generated content typically exhibits lower perplexity. Coincidentally, retrievers learn and incorporate perplexity features into their relevance estimation processes, consequently assigning higher relevance scores to LLM-generated documents. This leads to the lower ranking of human-written documents. It is worth noting that source bias is an inherent issue in PLM-based retrievers.

**中文**

3.3 通过提出的因果图解释源偏差 根据上面构建的因果图，源偏差可以解释如下：虽然 LLM 生成的内容保留了与人类编写的内容相似的语义，但 LLM 生成的内容通常表现出较低的复杂性。巧合的是，检索器学习并将困惑度特征纳入其相关性估计过程中，从而为法学硕士生成的文档分配更高的相关性分数。这导致人类编写的文档的排名较低。值得注意的是，来源偏差是基于 PLM 的检索器的一个固有问题。

### 段落 40 · Page 4

**EN**

Before the advent of LLMs, these retrievers had already learned non-causal perplexity features from purely human-written corpora. However, because the document ranking was predominantly conducted on human-written corpora, the relationship between PLM-based retrievers and perplexity was not evident. As powerful LLMs have become more accessible, the emergence of LLM-generated content has accentuated the perplexity effect. The content generated by LLMs exhibits a perceptibly different perplexity distribution compared to human-written content.

**中文**

在法学硕士出现之前，这些检索器已经从纯人类编写的语料库中学习了非因果困惑特征。然而，由于文档排名主要是在人工编写的语料库上进行的，因此基于 PLM 的检索器与困惑度之间的关系并不明显。随着强大的法学硕士变得越来越容易获得，法学硕士生成的内容的出现加剧了困惑效应。与人类编写的内容相比，法学硕士生成的内容表现出明显不同的困惑度分布。

### 段落 41 · Page 4

**EN**

This disparity in perplexity distribution causes documents from different sources to receive significantly different relevance rankings. 4

**中文**

这种困惑度分布的差异导致来自不同来源的文档获得显着不同的相关性排名。 4

### Page 5

### 段落 42 · Page 5

**EN**

Published as a conference paper at ICLR 2025 Table 1: Quantified causal effects (and corresponding p-value) for document perplexity on estimated relevance scores via two-stage regression. Bold indicates that the estimate can pass a significance test with p-value< 0.05. Significant negative causal effects are prevalent across various PLM-based retrievers in different domain datasets.

**中文**

作为 ICLR 2025 会议论文发表 表 1：通过两阶段回归对估计相关性分数的文档困惑度进行量化因果效应（以及相应的 p 值）。粗体表示估计值可以通过 p 值 < 0.05 的显着性检验。不同领域数据集中各种基于 PLM 的检索器普遍存在显着的负面因果效应。

### 段落 43 · Page 5

**EN**

Dataset BERT RoBERTa ANCE TAS-B Contriever coCondenser DL19 -9.32 (1e-4) -28.15 (2e-12) -0.52 (9e-3) -0.96 (1e-2) -0.02 (0.33) -0.69 (3e-2) TREC-COVID -1.69 (2e-2) 2.42 (8e-2) 0.09 (0.21) -0.48 (6e-3) -0.05 (7e-7) -0.32 (8e-3) SCIDOCS -2.44 (6e-2) -6.42 (2e-3) -0.23 (0.15) -0.39 (0.10) -0.02 (0.24) -0.26 (0.41) 4 E MPIRICAL AND THEORETICAL ANALYSIS ON THE EFFECT OF PERPLEXITY In this section, we conduct empirical experiments and theoretical analysis to substantiate that PLMbased retrievers assign higher relevance scores to documents with lower perplexity.

**中文**

数据集 BERT RoBERTa ANCE TAS-B Contriever coCondenser DL19 -9.32 (1e-4) -28.15 (2e-12) -0.52 (9e-3) -0.96 (1e-2) -0.02 (0.33) -0.69 (3e-2) TREC-COVID -1.69 (2e-2) 2.42 (8e-2) 0.09 (0.21) -0.48 (6e-3) -0.05 (7e-7) -0.32 (8e-3) SCIDOCS -2.44 (6e-2) -6.42 (2e-3) -0.23 (0.15) -0.39 (0.10) -0.02 (0.24) -0.26 (0.41) 4 关于困惑度影响的实证和理论分析 在本节中，我们进行实证实验和理论分析，以证实基于 PLM 的检索器为困惑度较低的文档分配较高的相关性分数。

### 段落 44 · Page 5

**EN**

4.1 E XPLORING THE BIASED EFFECT CAUSED BY PERPLEXITY 4.1.1 E STIMATION METHODS From the temperature intervention experiments in Section 3.1, we observe a clear negative correlation between document perplexity and estimated relevance scores. Despite human evaluation allows us to largely confirm that document semantics Md generated from different temperatures are almost the same, estimating the biased effect of Pd → ˆRq,d directly is problematic due to inevitable minor variations in document semantics, which, though subtle, are significant in causal effect estimation.

**中文**

4.1 探索困惑度造成的偏差效应 4.1.1 估计方法 从3.1节的温度干预实验中，我们观察到文档困惑度和估计的相关性得分之间存在明显的负相关关系。尽管人类评估使我们能够在很大程度上确认不同温度生成的文档语义 Md 几乎相同，但由于文档语义不可避免地存在微小变化，直接估计 Pd → ˆRq,d 的偏差效应是有问题的，尽管这种变化很微妙，但在因果效应估计中却很重要。

### 段落 45 · Page 5

**EN**

From the causal view, to robustly estimate the causal effect of Pd → ˆRq,d, the document semantics Md, query semantics Mq and golden relevance scores Rq,d are considered as confounders. Therefore, directly estimating this biased causal effect is not feasible without addressing this confounding factor. We use 2SLS based on instrumental variable (IV) methods (Angrist and Pischke, 2009; Hartford et al., 2017) to more accurately evaluate the causal effect of document perplexity on estimated relevance scores, more details about the method can be found in Appendix D.

**中文**

从因果关系的角度来看，为了稳健地估计 Pd → ˆRq,d 的因果效应，文档语义 Md、查询语义 Mq 和黄金相关性得分 Rq,d 被视为混杂因素。因此，如果不解决这个混杂因素，直接估计这种有偏差的因果效应是不可行的。我们使用基于工具变量（IV）方法（Angrist and Pischke，2009；Hartford et al.，2017）的2SLS来更准确地评估文档困惑度对估计相关性分数的因果影响，有关该方法的更多详细信息可以在附录D中找到。

### 段落 46 · Page 5

**EN**

According to the causal graph, document source Sd serves as an IV for estimating the effect of Pd → ˆRq,d. The IV is independent of confounders: query semantics Mq, document semantics Md, and golden relevance scores Rq,d. In the first stage of the regression, we use linear regression to predict document perplexity Pd based on document source Sd: Pd = β1Sd + ˜Pd, (1) where ˜Pd is independent with document source Sd and therefore depends solely on document semantics Md. As a result, we obtain coefficient ˆβ1 and the predicted document perplexity ˆPd.

**中文**

根据因果图，文档源Sd作为IV来估计Pd → ˆRq,d的效果。 IV 独立于混杂因素：查询语义 Mq、文档语义 Md 和黄金相关性得分 Rq,d。在回归的第一阶段，我们使用线性回归根据文档源 Sd 来预测文档困惑度 Pd：Pd = β1Sd + ～Pd， (1) 其中 ～Pd 与文档源 Sd 无关，因此仅取决于文档语义 Md。因此，我们获得系数 β1 和预测文档困惑度 ^Pd。

### 段落 47 · Page 5

**EN**

In the second stage, we substitute Pd with ˆPd = ˆβ1Sd to estimate the predicted relevance score ˆRq,d from the certain PLM-based retrievers: ˆRq,d = β2 ˆPd + ˜Rq,d, . (2) where residual term ˜Rq,d represents the part of the estimated relevance scores that can’t be explained by document perplexity. Since ˆPd is independent of document semanticsMd, the estimated coefficient ˆβ2 can accurately reflect the causal effect of perplexity on estimated relevance scores.

**中文**

在第二阶段，我们用 ^Pd = ^β1Sd 替换 Pd，以估计来自某些基于 PLM 的检索器的预测相关性得分 ^Rq,d： ^Rq,d = β2 ^Pd + ∼Rq,d,...。 (2) 其中残差项 ~Rq,d 表示估计相关性得分中无法用文档困惑度解释的部分。由于Pd与文档语义Md无关，因此估计系数β2可以准确地反映困惑度对估计相关性分数的因果影响。

### 段落 48 · Page 5

**EN**

4.1.2 E XPERIMENTAL RESULTS AND ANALYSIS In this section, we apply the causal effect estimation method described previously to assess the impact of document perplexity Pd on the estimated relevance score ˆRq,d. Models. To comprehensively evaluate this causal effect, we select several representative PLM-based retrieval models from the Cocktail benchmark (Dai et al., 2024a), including: (1) BERT (Devlin et al., 2019); (2) RoBERTa (Liu et al., 2019); (3) ANCE (Xiong et al., 2020); (4) TAS-B (Hofstätter et al., 2021); (5) Contriever (Izacard et al., 2022); (6) coCondenser (Gao and Callan, 2022). We employ the officially released checkpoints.

**中文**

4.1.2 实验结果与分析 在本节中，我们应用前面描述的因果效应估计方法来评估文档困惑度 Pd 对估计的相关性得分 ^Rq,d 的影响。模型。为了综合评估这种因果效应，我们从 Cocktail benchmark (Dai et al., 2024a) 中选择了几种具有代表性的基于 PLM 的检索模型，包括： (1) BERT (Devlin et al., 2019)； (2) RoBERTa（Liu 等人，2019）； (3) ANCE（Xiong等，2020）； (4) TAS-B（Hofstätter 等人，2021）； (5) 发明者 (Izacard et al., 2022)； (6) coCondenser（Gao 和 Callan，2022）。我们采用官方发布的检查点。

### 段落 49 · Page 5

**EN**

For more details, please refer to Appendix E.1. 5

**中文**

详细信息请参见附录E.1。 5

### Page 6

### 段落 50 · Page 6

**EN**

Published as a conference paper at ICLR 2025 Datasets. We select three widely-used IR datasets from different domains to ensure the broad applicability of our findings: (1) DL19 dataset (Craswell et al., 2020) for exploring retrieval across miscellaneous domains. (2) TREC-COVID dataset (V oorhees et al., 2021) focused on biomedical information retrieval. (3) SCIDOCS (Cohan et al., 2020) dedicated to the retrieval of scientific scholarly articles.

**中文**

作为 ICLR 2025 数据集的会议论文发表。我们选择了来自不同领域的三个广泛使用的 IR 数据集，以确保我们的研究结果具有广泛的适用性：（1）DL19 数据集（Craswell 等人，2020）用于探索跨其他领域的检索。 (2) TREC-COVID 数据集（V oorhees et al., 2021）专注于生物医学信息检索。 (3) SCIDOCS (Cohan et al., 2020) 致力于科学学术文章的检索。

### 段落 51 · Page 6

**EN**

Given that source bias arises from the ranking orders of positive samples from different sources, we only compare the estimated relevance scores of human-written and LLMgenerated relevant documents against their corresponding queries. Results and Analysis. The results across different datasets and different PLM-based retrievers are shown in Table 1. As we can see, in most cases, perplexity exhibits a consistently negative causal effect on relevance estimation, with documents of lower perplexity more likely to receive higher relevance scores.

**中文**

鉴于来源偏差是由不同来源的正样本的排名顺序引起的，我们仅将人类编写的和法学硕士生成的相关文档的估计相关性得分与其相应的查询进行比较。结果与分析。表 1 显示了不同数据集和不同基于 PLM 的检索器的结果。正如我们所见，在大多数情况下，困惑度对相关性估计表现出一致的负面因果影响，困惑度较低的文档更有可能获得较高的相关性得分。

### 段落 52 · Page 6

**EN**

Although this causal effect is relatively weak, it is statistically significant, with p-values < 0.05 in most instances. We also explore whether this causal effect changes with different sampling temperature. Results in Appendix Table 5 indicate that ˆβ2 is robust for temperature changes, that is, this causal effect is independent with generation temperature. This finding is crucial as retrieval tasks emphasize the relative ranking of relevance scores rather than their absolute values.

**中文**

尽管这种因果效应相对较弱，但具有统计显着性，大多数情况下 p 值 < 0.05。我们还探讨了这种因果效应是否随着不同的采样温度而变化。附录表5中的结果表明，β2对于温度变化是稳健的，也就是说，这种因果效应与生成温度无关。这一发现至关重要，因为检索任务强调相关性分数的相对排名而不是其绝对值。

### 段落 53 · Page 6

**EN**

Even a slight preferential increase in estimated relevance scores for LLM-generated content over human-written content will lead to a consistent trend of higher rankings for LLM-generated documents by PLM-based retrievers, further confirming the observations in Figure 1. Finding 1: For PLM-based retrievers, document perplexity has a causal effect on estimated relevance scores. Lower perplexity can lead to higher relevance scores. 4.2 A NALYZING MECHANISM BEHIND THE BIASED EFFECT 4.2.1 W HY PERPLEXITY AFFECTS PLM- BASED RETRIEVERS ?

**中文**

即使 LLM 生成的内容的估计相关性分数比人工编写的内容略有优先增加，也会导致基于 PLM 的检索器对 LLM 生成的文档排名较高的一致趋势，进一步证实了图 1 中的观察结果。发现 1：对于基于 PLM 的检索器，文档困惑度对估计的相关性分数有因果影响。较低的困惑度可以带来较高的相关性分数。 4.2 偏差效应背后的分析机制 4.2.1 为什么困惑会影响基于 PLM 的检索器？

### 段落 54 · Page 6

**EN**

In Section 4.1, our empirical experiments have confirmed that PLM-based retrievers take perplexity features into account for document retrieval. However, the reason why perplexity-related features play a role, particularly when these models are primarily designed for document ranking, remains unclear. Considering that PLM-based retrievers are generally fine-tuned from PLMs on retrieval tasks, we delve into the relationship between the mask language modeling task in the pre-training stage and the mean-pooling document retrieval task in the fine-tuning stage. Our formulation are as follows and explanations can be found in Appendix C.1.

**中文**

在第 4.1 节中，我们的实证实验证实，基于 PLM 的检索器在文档检索时考虑了困惑度特征。然而，与困惑相关的特征发挥作用的原因，特别是当这些模型主要用于文档排名时，仍不清楚。考虑到基于 PLM 的检索器通常是根据 PLM 在检索任务上进行微调的，因此我们深入研究了预训练阶段的掩码语言建模任务和微调阶段的均值池文档检索任务之间的关系。我们的表述如下，解释参见附录 C.1。

### 段落 55 · Page 6

**EN**

Model Architecture. To simplify our analysis, we assume a common architecture for PLM-based retrievers, consisting of an encoder f(t; θ) : T L×D 7→ R L×N and a one-layer decoder g(z; W ) = σ(zW ), where T denotes the set composed of one-hot vectors, L is the length of query or document, D is the dictionary size, N is the dimension of embedding vector, and σ(·) maps real vectors to simplexes. For the ease of qualitative analysis, we replace softmax operation with a linear operation, and zW is assumed positive to ensure the well-definition of the probability distribution. Masked Language Modeling (MLM) Task.

**中文**

模型架构。为了简化我们的分析，我们假设基于 PLM 的检索器的通用架构，由编码器 f(t; θ) : T L×D 7→ R L×N 和单层解码器 g(z; W ) = σ(zW ) 组成，其中 T 表示由 one-hot 向量组成的集合，L 是查询或文档的长度，D 是字典大小，N 是嵌入向量的维度，σ(·) 将真实向量映射到单纯形。为了便于定性分析，我们用线性运算代替softmax运算，并假设zW为正以确保概率分布的明确定义。掩码语言建模 (MLM) 任务。

### 段落 56 · Page 6

**EN**

The PLM is initially pre-trained on the MLM task with CrossEntropy loss: L1(d) = − 1 L 1T L[d ⊙ log g(f(d))]1D, where ⊙ denotes the Hadamard product, 1 L 1L means averages over the length of the documents, [d ⊙ log g(f(d))]1D is the expression of CrossEntropy using one-hot vectors. Document Retrieval Task. In the fine-tuning stage for the document retrieval task, the retrieval model estimates the relevance for given query-document pairs by computing the dot product of the document embedding vectors demb = f(d, θ) and query embedding vectors qemb = f(q, θ). Without loss of generality, we assume ∥demb l ∥2 = 1, l = 1, . . .

**中文**

PLM 最初在具有 CrossEntropy 损失的 MLM 任务上进行预训练：L1(d) = − 1 L 1T L[d ⊙ log g(f(d))]1D，其中 ⊙ 表示 Hadamard 乘积，1 L 1L 表示文档长度上的平均值，[d ⊙ log g(f(d))]1D 是使用 one-hot 向量的 CrossEntropy 的表达式。文档检索任务。在文档检索任务的微调阶段，检索模型通过计算文档嵌入向量 demb = f(d, θ) 和查询嵌入向量 qemb = f(q, θ) 的点积来估计给定查询文档对的相关性。不失一般性，我们假设 ∥demb l ∥2 = 1, l = 1,...。。。

### 段落 57 · Page 6

**EN**

, L, which means the embeddings of each token is normalized. The loss function can be written as L2(d, q) = −tr[( 1 L 1Ldemb)T ( 1 L 1Lqemb)], where 1 L 1L[·] is the mean pooling operation of the embeddings over the document length L. With the formulation above, we further explore the theoretical underpinnings of why perplexity influences retrieval performance by examining the gradients of the loss functions for both the MLM task and the document retrieval task, as shown in the following Theorem 1: Theorem 1. Given the following three conditions: 6

**中文**

, L，这意味着每个标记的嵌入都被标准化。损失函数可以写为 L2(d, q) = −tr[( 1 L 1Ldemb)T ( 1 L 1Lqemb)]，其中 1 L 1L[·] 是文档长度 L 上嵌入的均值池化操作。根据上述公式，我们通过检查 MLM 任务和文档检索任务的损失函数的梯度，进一步探索为什么困惑度影响检索性能的理论基础，如下所示以下定理 1： 定理 1. 给定以下三个条件： 6

### Page 7

### 段落 58 · Page 7

**EN**

Published as a conference paper at ICLR 2025 •Representation Collinearity: the embedding vectors of relevant query-document pairs are collinear after mean pooling, i.e., 1L×Lf(q) = λ1L×Lf(d), λ > 0. • Semi-Orthogonal Weight Matrix: the weight matrix of the decoder is semi-orthogonal, i.e., W W T = IN . •Encoder-decoder Cooperation: fine-tuning does not disrupt the corresponding function between encoder and decoder, i.e., f(d) = g−1(d). Then there exists a matrix K = h λkl L(1−kl) i ln ∈ R L×N + , kl =PD d (dembW )ld which satisfies ∂L2 ∂demb = K ⊙ ∂L1 ∂demb .

**中文**

在 ICLR 2025 上以会议论文形式发表。 • 表示共线性：相关查询-文档对的嵌入向量在均值池化后是共线的，即 1L×Lf(q) = λ1L×Lf(d)，λ > 0。 • 半正交权重矩阵：解码器的权重矩阵是半正交的，即 W W T = IN。 •编码器-解码器协作：微调不会破坏编码器和解码器之间的相应功能，即f(d) = g−1(d)。则存在矩阵 K = h λkl L(1−kl) i ln ∈ R L×N + , kl =PD d (dembW )ld 满足 ∂L2 ∂demb = K ⊙ ∂L1 ∂demb。

### 段落 59 · Page 7

**EN**

The three conditions made with their rationale are explained in Appendix C.1 and the proof of Theorem 1 can be found in Appendix C.2. From Theorem 1, we observe that the gradients of the two losses of MLM task and the retrieval task have a positive linear relationship. Note that L1(d) actually represent the document perplexity Pd and L2(d, q) actually represent the negative estimated relevance score − ˆRq,d. Then we can easily derive the following Corollary, which illustrates how the key conclusion ∂L2/∂demb = K ⊙ ∂L1/∂demb in Theorem 1 leads to the biased effect of document perplexity Pd on estimated relevance score ˆRq,d: Corollary 1.

**中文**

附录 C.1 解释了这三个条件及其原理，附录 C.2 给出了定理 1 的证明。从定理1我们观察到MLM任务和检索任务的两个损失的梯度具有正线性关系。请注意，L1(d) 实际上代表文档困惑度 Pd，L2(d, q) 实际上代表负估计相关性得分 − ˆRq,d。那么我们可以很容易地推导出以下推论，它说明了定理 1 中的关键结论 ∂L2/∂demb = K ⊙ ∂L1/∂demb 如何导致文档困惑度 Pd 对估计相关性得分 ˆRq,d 产生偏差：推论 1。

### 段落 60 · Page 7

**EN**

Consider a human-written document d1 and its LLM-rewritten document d2, they are both relevant with query q. Assume LLM-rewritten documents possess lower perplexity at token level (Mitchell et al., 2023). Let rvec/vec be matrix-to-row/column-vector operator,Ll 1(d) denote the perplexity of the l-th token in the document, (demb 2 )l denote the embedding of the l-th token, Ll 1(d1) − Ll 1(d2) = ∂L1(d2) ∂(demb 2 )l · ∂(demb 2 )l ∂d2 · vec(d1 − d2) > 0, l = 1, . . . , L, where 1st-order approximation of Chain rule is taken as the surrogate function (Grabocka et al., 2019; Nguyen et al., 2009) for Ll 1(d).

**中文**

考虑一个人工编写的文档 d1 及其 LLM 重写的文档 d2，它们都与查询 q 相关。假设 LLM 重写的文档在令牌级别具有较低的复杂性（Mitchell 等人，2023）。令 rvec/vec 为矩阵到行/列向量运算符，Ll 1(d) 表示文档中第 l 个标记的复杂度，(demb 2 )l 表示第 l 个标记的嵌入，Ll 1(d1) − Ll 1(d2) = ∂L1(d2) ∂(demb 2 )l · ∂(demb 2 )l ∂d2 · vec(d1 − d2) > 0, l = 1, .。。，L，其中链式法则的一阶近似被视为 Ll 1(d) 的代理函数（Grabocka 等人，2019 年；Nguyen 等人，2009 年）。

### 段落 61 · Page 7

**EN**

According to Theorem 1 and 1st-order approximation of L2(d), ˆRq,d1 − ˆRq,d2 = −[L2(d1) − L2(d2)] = −rvec(K ⊙ ∂L1(demb 2 ) ∂demb 2 ) · ∂demb 2 ∂d2 · vec(d1 − d2) = − LX l=1 λkl L(1 − kl) ∂L1(d2) ∂(demb 2 )l ∂(demb 2 )l ∂d2 vec(d1 − d2) = − LX l=1 λkl L(1 − kl) Ll 1(d1) − Ll 1(d2)  < 0. Corollay 1 indicates that human-written document will receive lower relevance estimation than its LLM-written document, resulting in source bias. It is important to note that our theoretical analysis does not cover all situations in reality, we will discuss these limitations in Appendix B.

**中文**

根据定理1和L2(d)的一阶近似， ˆRq,d1 − ˆRq,d2 = −[L2(d1) − L2(d2)] = −rvec(K ⊙ ∂L1(demb 2 ) ∂demb 2 ) · ∂demb 2 ∂d2 · vec(d1 − d2) = − LX l=1 λkl L(1 − kl) ∂L1(d2) ∂(demb 2 )l ∂(demb 2 )l ∂d2 vec(d1 − d2) = − LX l=1 λkl L(1 − kl) Ll 1(d1) − Ll 1(d2) < 0。推论 1 表明人工编写的文档将收到的相关性估计低于其法学硕士撰写的文档，从而导致来源偏差。值得注意的是，我们的理论分析并没有涵盖现实中的所有情况，我们将在附录 B 中讨论这些局限性。

### 段落 62 · Page 7

**EN**

Finding 2: For PLM-based retrievers, the gradients of MLM and IR loss functions (metrics) possess linear overlap, leading to the biased effect of perplexity on estimated relevance scores. 4.2.2 F URTHER VERIFICATION OF THEOREM 1 Theorem 1 reveals the linear relationship between language modeling gradients and retrieval gradients w.r.t. document embedding vectors demb. For a more comprehensive verification for its reliability, we derive Corollay 2 from Theorem 1 and provide supporting experiments about the corollay. The derivation is similar with that in Corollary 1. Corollary 2.

**中文**

发现 2：对于基于 PLM 的检索器，MLM 和 IR 损失函数（度量）的梯度具有线性重叠，导致困惑度对估计的相关性分数产生偏差。 4.2.2 定理 1 的进一步验证 定理 1 揭示了语言建模梯度和检索梯度之间的线性关系。文档嵌入向量 demb。为了更全面地验证其可靠性，我们从定理1推导出推论2，并提供了有关推论的支持实验。推导与推论1、推论2类似。

### 段落 63 · Page 7

**EN**

For two retrievers f(t; θ1), f(t; θ2) which share the same PLM, such as BERT. If retriever f(t; θ1) possesses more powerful language modeling ability than f(t; θ2), i.e., Ed∈D[Ll 1(d; θ1)] − Ed∈D[Ll 1(d; θ2)] < 0, l = 1, . . . , L, 7

**中文**

对于共享相同 PLM 的两个检索器 f(t; θ1)、f(t; θ2)，例如 BERT。如果检索器 f(t; θ1) 比 f(t; θ2) 拥有更强大的语言建模能力，即 Ed ∈ D[Ll 1(d; θ1)] − Ed ∈ D[Ll 1(d; θ2)] < 0, l = 1, .。。 , L, 7

### Page 8

### 段落 64 · Page 8

**EN**

Published as a conference paper at ICLR 2025 then similar to the Corollary 1, we have Ed∈D[L2(d; θ1)] − Ed∈D[L2(d; θ2)] = Ed∈D  rvec  ∂L2(demb; θ2) ∂demb  · ∂demb ∂θ2 · vec(θ1 − θ2)  =E  rvec(K ⊙ ∂L1(demb; θ2) ∂demb ) ∂demb ∂θ2 vec(θ1 − θ2)  = E " LX l=1 λkl L(1 − kl) Ll 1(d; θ1) − Ll 1(d; θ2)  # < 0. Note that Ed∈D[L1(d; θ)] is a typical measure of language modeling ability and Ed∈D[L2(d; θ)] reflects the ranking performance, Corollary 2 indicates that if a retriever possesses more powerful language modeling ability, its ranking performance will be better.

**中文**

作为 ICLR 2025 的会议论文发表，与推论 1 类似，我们有 EdεD[L2(d; θ1)] − EdεD[L2(d; θ2)] = EdεD rvec ∂L2(demb; θ2) ∂demb · ∂demb ∂θ2 · vec(θ1 − θ2) =E rvec(K ⊙ ∂L1(demb; θ2) ∂demb ) ∂demb ∂θ2 vec(θ1 − θ2) = E " LX l=1 λkl L(1 − kl) Ll 1(d; θ1) − Ll 1(d; θ2) # < 0。请注意，Ed∈D[L1(d; θ)] 是语言建模能力的典型衡量标准， Ed∈D[L2(d; θ)]反映了排序性能，推论2表明如果检索器拥有更强大的语言建模能力，则其排序性能会更好。

### 段落 65 · Page 8

**EN**

To offer empirical support for the corollary, we evaluate the language modeling ability of PLM-based retrieval models with different ranking performances. By taking the retrieval model directly as a PLM encoder to do MLM task, we calculate the average text perplexity of the retrieval corpus to evaluate their language modeling ability, which offers support for the encoder-decoder corporation assumption at the same time. As illustrated in Figure 3, there is a clear correlation between text perplexity and retrieval accuracy (except Contriever).

**中文**

为了给推论提供实证支持，我们评估了具有不同排名性能的基于 PLM 的检索模型的语言建模能力。通过将检索模型直接作为PLM编码器来完成MLM任务，我们计算检索语料库的平均文本困惑度来评估其语言建模能力，同时为编码器-解码器公司假设提供支持。如图 3 所示，文本困惑度和检索准确性之间存在明显的相关性（Contriever 除外）。

### 段落 66 · Page 8

**EN**

These results, demonstrating that language modeling capabilities are indeed correlated with retrieval performance, strengthen the practical reliability of our assumptions and conclusions as the deductive verification of the above hypothesis we used. This finding also explains why PLM dramatically improve the performance of retrievers over past years. 2 3 4 5 6 7 8 9 10 11 Perplexity 40 42 44 46 48 50 52 54Ranking Performance BERT RoBERTa ANCE TAS-B Contriever coCondenser Figure 3: Model perplexity and ranking performance (NDCG@3) on averaged results of DL19, TREC-COVID, and SCIDOCS.

**中文**

这些结果证明语言建模能力确实与检索性能相关，增强了我们的假设和结论的实际可靠性，作为我们使用的上述假设的演绎验证。这一发现还解释了为什么 PLM 在过去几年中显着提高了猎犬的性能。 2 3 4 5 6 7 8 9 10 11 困惑度 40 42 44 46 48 50 52 54排名性能 BERT RoBERTa ANCE TAS-B Contriever coCondenser 图 3：基于 DL19、TREC-COVID 和 SCIDOCS 平均结果的模型困惑度和排名性能 (NDCG@3)。

### 段落 67 · Page 8

**EN**

Combining the previous findings, we can further understand the relationship between model retrieval performance and the degree of source bias. On one hand, if the PLM-based retriever demonstrates a better MLM capability, it tends to be more sensitive to document perplexity, which leads to more severe source bias (Corollary 1). On the other hand, a retriever with better MLM capabilities can also achieve more accurate relevance estimations, leading to better ranking performance (Corollary 2). Consequently, PLM-based retrievers encounter a trade-off between accuracy in retrieval and the severity of source bias.

**中文**

结合之前的研究结果，我们可以进一步理解模型检索性能与来源偏差程度之间的关系。一方面，如果基于 PLM 的检索器表现出更好的 MLM 能力，它往往对文档的复杂性更加敏感，从而导致更严重的来源偏差（推论 1）。另一方面，具有更好MLM能力的检索器也可以实现更准确的相关性估计，从而获得更好的排名性能（推论2）。因此，基于 PLM 的检索器需要在检索准确性和来源偏差严重性之间进行权衡。

### 段落 68 · Page 8

**EN**

Specifically, higher ranking performance is associated with more significant source bias. This relationship has been noted in previous research (Dai et al., 2024a), and we are the first to offer a plausible explanation for this phenomenon. Finding 3: Better language modeling improves PLM-based retriever’s ranking performance, but also heightens its sensitivity to perplexity, thus increasing source bias severity. 5 C AUSAL -I NSPIRED SOURCE BIAS MITIGATION In this section, we further propose a causal-inspired debiasing method to eliminate the source bias, which can be naturally derived from our above causal analysis.

**中文**

具体来说，较高的排名表现与更显着的来源偏差相关。这种关系在之前的研究中已经被注意到（Dai et al., 2024a），我们是第一个对这种现象提供合理解释的人。发现 3：更好的语言建模提高了基于 PLM 的检索器的排名性能，但也提高了其对困惑的敏感性，从而增加了源偏差的严重性。 5 因果启发的源偏差缓解 在本节中，我们进一步提出了一种因果启发的去偏差方法来消除源偏差，这可以自然地从我们上述的因果分析中得出。

### 段落 69 · Page 8

**EN**

We then conduct experiments to evaluate the effectiveness of the proposed debiasing method. 5.1 P ROPOSED DEBIASING METHOD : C AUSAL DIAGNOSIS AND CORRECTION In Section 3 and 4, we have constructed a causal graph and estimated the biased effect of perplexity on the final predicted relevance score. Based on these insights, we propose an inference-time debiased method via Causal Diagnosis Correction (CDC). The main procedure of CDC lies on two stage: (i) Bias Diagnosis: Employing the Instrumental Variable method for estimating the bias effect ˆβ2 of perplexity Pd to estimated relevance score ˆRq,d.

**中文**

然后我们进行实验来评估所提出的去偏方法的有效性。 5.1 提出的去偏方法：因果诊断和校正 在第 3 节和第 4 节中，我们构建了一个因果图，并估计了困惑度对最终预测相关性得分的偏差影响。基于这些见解，我们提出了一种通过因果诊断校正（CDC）的推理时间去偏方法。 CDC的主要过程分为两个阶段：（i）偏差诊断：采用工具变量方法来估计困惑度Pd对估计的相关性得分^Rq,d的偏差效应^β2。

### 段落 70 · Page 8

**EN**

(ii) Bias Correction: Separating the biased effect of document perplexity from the overall estimated relevance scores ˆRq,d. 8

**中文**

(ii) 偏差校正：将文档困惑度的偏差影响与总体估计相关性得分 ˆRq,d 分开。 8

### Page 9

### 段落 71 · Page 9

**EN**

Published as a conference paper at ICLR 2025 Algorithm 1: The Proposed CDC: Debiasing with Causal Diagnosis and Correction Input: training set D, test query set Q, test corpus C, estimation budget M Output: unbiased estimated relevance scores ˜R 1 // Bias Diagnosis 2 Initialize the estimation set for estimating biased effect De ← ∅ 3 for training pairs (qi, dH i ) ∈ D and |De| < M do 4 Instruct LLM to generate doc dG i via rewriting the original human-written doc dH i 5 Predict the estimated relevance scores ˆrH i , ˆrG i for pairs (qi, dH i ) and (qi, dG i ) 6 Calculate perplexity pH i , pG i for doc dH i and doc dG i , respectively 7 Updating the estimation set De ← D e ∪ (ˆrH i , ˆrG i , pH i , pG i ) 8 end 9 Estimate the biased effect coefficient ˆβ2 with 2-stage regression using Eq.

**中文**

作为 ICLR 2025 会议论文发表 算法 1：提议的 CDC：通过因果诊断和校正进行去偏 输入：训练集 D、测试查询集 Q、测试语料库 C、估计预算 M 输出：无偏估计相关性分数 ∼R 1 // 偏倚诊断 2 初始化估计集，用于估计训练对的偏倚效应 De ← ∅ 3 (qi, dH i ) ε D 和|De| < M do 4 指示 LLM 通过重写原始人工编写的 doc dH i 来生成 doc dG i 5 预测 (qi, dH i ) 和 (qi, dG i ) 对的估计相关性分数 ˆrH i , ˆrG i 6 分别计算 doc dH i 和 doc dG i 的困惑度 pH i , pG i 7 更新估计集 De ← De ∪ (ˆrH i , ˆrG i , pH i , pG i ) 8 end 9 使用等式 2 阶段回归估计偏效应系数 ˆβ2。

### 段落 72 · Page 9

**EN**

(2) on De 10 // Bias Correction 11 for test query qt ∈ Q do 12 Predict the estimated relevance scores ˆrt for each pair (qt, dt) with dt ∈ C 13 Calculate document perplexity pt for each doc dt ∈ C 14 Debias the original model prediction ˆrt using Eq. (3), add the calibrated score ˜rt to ˜R 15 end 16 return ˜R Table 2: Performance (NDCG@3) and bias (Relative ∆ (Dai et al., 2024c) on NDCG@3) of different PLM-based retrievers with and without our proposed CDC debiased method on three datasets.

**中文**

(2) on De 10 // 测试查询 qt ∈ Q 的偏差校正 11 do 12 使用 dt ∈ C 预测每对 (qt, dt) 的估计相关性分数 ˆrt 13 计算每个文档 dt ∈ C 的文档困惑度 pt 14 使用等式对原始模型预测 ˆrt 进行去偏。 (3)，将校准分数 rt 添加到 R 15 end 16 return ～R 表 2：在三个数据集上使用和不使用我们提出的 CDC 去偏方法的不同基于 PLM 的检索器的性能 (NDCG@3) 和偏差（NDCG@3 上的相对 Δ (Dai 等人，2024c)）。

### 段落 73 · Page 9

**EN**

Note that a more negative bias metric value indicates a greater bias towards LLM-generated documents, while a more positive value indicates a greater bias towards human-written documents.

**中文**

请注意，负偏差指标值越大，表示对 LLM 生成的文档的偏差越大，而正值越大，表示对人类编写的文档的偏差越大。

### 段落 74 · Page 9

**EN**

Model DL19 (In-Domain) TREC-COVID (Out-of-Domain) SCIDOCS (Out-of-Domain) Performance Bias Performance Bias Performance Bias Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDC BERT 75.92 77.65 -23.68 5.90 53.72 45.88 -39.58 -18.40 10.80 10.44 -2.85 29.19 Roberta 72.79 71.33 -36.32 4.45 46.31 45.86 -48.14 -10.51 8.85 8.24 -30.90 32.13 ANCE 69.41 67.73 -21.03 34.95 71.01 69.94 -33.59 -1.94 12.73 12.31 -1.57 26.26 TAS-B 74.97 75.63 -49.17 -9.97 63.95 62.84 -73.36 -37.42 15.04 14.15 -1.90 23.48 Contriever 72.61 73.83 -21.93 -5.33 63.17 61.35 -62.26 -31.33 15.45 15.09 -6.96 1.63 coCondenser 75.50 75.36 -18.99 9.60 70.94 71.07 -67.95 -45.39 13.9

**中文**

模型 DL19（域内） TREC-COVID（域外） SCIDOCS（域外） 性能偏差 性能偏差 性能偏差 Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDC BERT 75.92 77.65 -23.68 5.90 53.72 45.88 -39.58 -18.40 10.80 10.44 -2.85 29.19 罗伯塔 72.79 71.33 -36.32 4.45 46.31 45.86 -48.14 -10.51 8.85 8.24 -30.90 32.13 安斯 69.41 67.73 -21.03 34.95 71.01 69.94 -33.59 -1.94 12.73 12.31 -1.57 26.26 TAS-B 74.97 75.63 -49.17 -9.97 63.95 62.84 -73.36 -37.42 15.04 14.15 -1.90 23.48 发明者 72.61 73.83 -21.93 -5.33 63.17 61.35 -62.26 -31.33 15.45 15.09 -6.96 1.63 共冷凝器 75.50 75.36 -18.99 9.60 70.94 71.07 -67.95 -45.39 13.9

### 段落 75 · Page 9

**EN**

3 13.79 -5.95 1.06 Specifically, the final calibrated score ˜Rq,d for document ranking can be formulated as follows: ˜Rq,d = ˆRq,d − ˆβ2Pd, (3) which can be derived by rearranging Eq.

**中文**

3 13.79 -5.95 1.06 具体来说，文档排名的最终校准分数 〜Rq,d 可以表述如下： 〜Rq,d = ˆRq,d − ˆβ2Pd, (3) 可以通过重新排列方程 3 来导出。

### 段落 76 · Page 9

**EN**

(2). In this formula, ˜Rq,d is independent to document source and perplexity. Therefore, it serves as a good proxy for semantic relevance ranking. Specifically, we first take M samples from the training set D to construct the estimation set De for estimating the biased effect ˆβ2 (lines 2-8), where M is the estimation budget. To construct the estimation set De, we instruct an LLM to generate document dG i by rewriting the original humanwritten document dH i . For these two types of samples, we use the retriever to predict their relevance scores ˆrH i and ˆrG i for the given query and calculate their document perplexities pH i and pG i .

**中文**

（2）。在这个公式中，~Rq,d 与文档来源和困惑度无关。因此，它可以作为语义相关性排名的良好代理。具体来说，我们首先从训练集 D 中取出 M 个样本来构建估计集 De，用于估计偏置效应 β2（第 2-8 行），其中 M 是估计预算。为了构造估计集 De，我们指示 LLM 通过重写原始的人工书写文档 dH i 来生成文档 dG i。对于这两类样本，我们使用检索器来预测给定查询的相关性得分 ˆrH i 和 ˆrG i，并计算它们的文档困惑度 pH i 和 pG i。

### 段落 77 · Page 9

**EN**

Further, following the practice in Section 4.1, we use two-stage IV regression on the estimation set De to estimate the biased coefficient ˆβ2 (line 9). During testing, we use Eq. (3) to correct the original model prediction ˆrt, obtaining the calibrated score ˜rt for final document ranking (line 11-15). We summarize the overall procedure of CDC in Algorithm 1. 5.2 E XPERIMENTS AND ANALYSIS To evaluate the effectiveness of CDC, we implement it across various retrievers in simulated-realistic debiasing scenarios, where generated documents are from different domains and LLMs.

**中文**

此外，按照4.1节的做法，我们在估计集De上使用两阶段IV回归来估计有偏系数β2（第9行）。在测试过程中，我们使用等式。 (3) 修正原始模型预测 rt，获得最终文档排名的校准分数 rt（第 11-15 行）。我们在算法 1 中总结了 CDC 的整体过程。 5.2 实验和分析 为了评估 CDC 的有效性，我们在模拟现实去偏场景中的各种检索器上实现它，其中生成的文档来自不同的领域和法学硕士。

### 段落 78 · Page 9

**EN**

In this case, we investigate the generalizability of the CDC method at both LLM level and Domain level. At domain-level, we employ bias diagnosis on the training set of DL19 to estimate the biased effect ˆβ2 for each retrieval model, and then conduct in-domain and cross-domain evaluation on the test sets 9

**中文**

在本例中，我们研究了 CDC 方法在法学硕士级别和领域级别的通用性。在领域层面，我们对DL19的训练集进行偏差诊断来估计每个检索模型的偏差效应^β2，然后对测试集进行域内和跨域评估9

### Page 10

### 段落 79 · Page 10

**EN**

Published as a conference paper at ICLR 2025 Table 3: Performance (NDCG@3) and bias (Relative ∆ (Dai et al., 2024c) on NDCG@ 3) of the retrievers on mixed SciFact corpus from different LLMs. Bias Diagnosis is conducted on DL19 corpus from Llama-2, where CDC performs generalization at both LLM and data-domain levels.

**中文**

作为 ICLR 2025 会议论文发表 表 3：检索器在来自不同法学硕士的混合 SciFact 语料库上的性能 (NDCG@3) 和偏差（NDCG@3 上的相对 Δ (Dai et al., 2024c)）。偏差诊断是在 Llama-2 的 DL19 语料库上进行的，其中 CDC 在 LLM 和数据域级别上进行泛化。

### 段落 80 · Page 10

**EN**

Model Llama-2 (In-Domain) GPT-4 (Out-of-Domain) GPT-3.5 (Out-of-Domain) Mistral (Out-of-Domain) Performance Bias Performance Bias Performance Bias Performance Bias Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDCBERT 35.67 35.08 -12.37 6.75 36.47 35.75 -3.69 6.04 35.97 35.27 -5.03 18.08 35.13 35.08 0.73 13.07RoBERTa 38.09 36.76 -29.54 -0.88 38.53 37.70 -11.98 4.52 39.17 38.00 -35.39 14.09 38.29 37.28 -17.95 16.78ANCE 42.13 42.13 -8.81 4.59 42.67 42.99 -5.53 3.28 42.76 42.96 -13.59 6.09 42.62 42.71 -8.59 1.82TAS-B 52.95 53.94 -15.04 -7.96 52.12 52.44 -4.94 -0.05 52.83 52.90 -5.65 5.57 52.18 52.69 -8.71 -2.00Contriever 55

**中文**

型号 Llama-2（域内） GPT-4（域外） GPT-3.5（域外） Mistral（域外） 性能偏差 性能偏差 性能偏差 性能偏差 Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDC Raw +CDCBERT 35.67 35.08 -12.37 6.75 36.47 35.75 -3.69 6.04 35.97 35.27 -5.03 18.08 35.13 35.08 0.73 13.07罗贝尔塔 38.09 36.76 -29.54 -0.88 38.53 37.70 -11.98 4.52 39.17 38.00 -35.39 14.09 38.29 37.28 -17.95 16.78 42.13 42.13 -8.81 4.59 42.67 42.99 -5.53 3.28 42.76 42.96 -13.59 6.09 42.62 42.71 -8.59 1.82TAS-B 52.95 53.94 -15.04 -7.96 52.12 52.44 -4.94 -0.05 52.83 52.90 -5.65 5.57 52.18 52.69 -8.71 -2.00Contriever 55

### 段落 81 · Page 10

**EN**

.19 55.37 -2.87 1.07 55.78 55.70 -5.32 -4.44 56.11 56.17 -7.43 -2.81 56.13 56.28 -4.13 -2.39coCondenser 49.53 49.40 -12.98 -9.26 48.57 48.91 5.04 6.04 48.59 48.81 -1.00 5.30 49.57 49.92 -5.90 -0.76 of DL19, TREC-COVID, SCIDOCS.

**中文**

.19 55.37 -2.87 1.07 55.78 55.70 -5.32 -4.44 56.11 56.17 -7.43 -2.81 56.13 56.28 -4.13 -2.39co冷凝器 49.53 49.40 -12.98 -9.26 DL19、TREC-COVID、SCIDOCS 的 48.57 48.91 5.04 6.04 48.59 48.81 -1.00 5.30 49.57 49.92 -5.90 -0.76。

### 段落 82 · Page 10

**EN**

Note that only 128 samples (i.e., estimation budget M = 128) are used for bias diagnosis, this sample size is sufficient for effective results. More detailed settings can be found in Appendix E.1. The averaged results over five different seeds are reported in Table 2. As we can see, using the estimated biased coefficient of in-domain retrieval data, our debiasing CDC successfully mitigates or even reverses the retrieval models’ preference towards human-written documents without fine-tuning retrievers. Meanwhile, this estimated biased coefficient demonstrates generalizability across out-of-domain datasets.

**中文**

请注意，仅使用 128 个样本（即估计预算 M = 128）进行偏差诊断，此样本量足以获得有效结果。更详细的设置可参见附录 E.1。表 2 报告了五种不同种子的平均结果。正如我们所看到的，使用域内检索数据的估计偏差系数，我们的去偏差 CDC 成功地减轻甚至逆转了检索模型对人类编写的文档的偏好，而无需微调检索器。同时，这个估计的偏差系数证明了跨域外数据集的普遍性。

### 段落 83 · Page 10

**EN**

The majority of the retrieval performance degradation was generally less than 2 percentage points, revealing that our debiasing CDC has acceptable impact on ranking performance, see detailed significance test in Appendix Table 7. In addition, the mean and standard deviation of performance and bias after CDC debiasing for the five sampling sessions is provided in Appendix Table 6, indicating the robustness of CDC to training samples. We also find that the debiasing results may vary across different retrievers.

**中文**

大多数检索性能下降一般小于2个百分点，表明我们的去偏CDC对排名性能具有可接受的影响，请参阅附录表7中的详细显着性测试。此外，附录表6中提供了五个采样会话的CDC去偏后的性能和偏差的平均值和标准差，表明CDC对训练样本的稳健性。我们还发现不同检索器的去偏结果可能会有所不同。

### 段落 84 · Page 10

**EN**

Specifically, CDC has more significant effects on vanilla models like BERT while exhabits lower impacts on stronger retrievers such as Contriever. We offer the following analysis to explain such observations. Stronger retrievers are developed using more sophisticated contrastive learning algorithms, which enhance their abilities to differentiate between highly relevant documents and the others. In this way, it may be more challenging for CDC corrections to alter the initial rankings. So a more aligned or model-specific approach could potentially enhance the debiasing process.

**中文**

具体来说，CDC 对 BERT 等普通模型有更显着的影响，而对 Contriever 等更强的检索器的影响则较小。我们提供以下分析来解释这些观察结果。更强大的检索器是使用更复杂的对比学习算法开发的，这增强了它们区分高度相关文档和其他文档的能力。这样一来，CDC修正改变初始排名的难度可能会更大。因此，更加一致或特定于模型的方法可能会增强去偏过程。

### 段落 85 · Page 10

**EN**

Considering that the web content may be generated by diverse LLMs, we expand our evaluations to assess the generalizability of the CDC method across corpora generated by different LLMs, including Llama (Touvron et al., 2023), GPT-4 (Achiam et al., 2023), GPT-3.5, and Mistral (Jiang et al., 2023). Due to the cost of computing resources, we conducted experiments on a smaller dataset SciFact, which is also used in previous works (Dai et al., 2024c;a). In this setup, CDC used Llama’s rewritten DL19 documents to estimate β2 and subsequently correct retrieval results on SciFact corpora mixed with each LLM separately.

**中文**

考虑到网络内容可能由不同的法学硕士生成，我们扩展了评估范围，以评估 CDC 方法在不同法学硕士生成的语料库中的通用性，包括 Llama (Touvron et al., 2023)、GPT-4 (Achiam et al., 2023)、GPT-3.5 和 Mistral (Jiang et al., 2023)。由于计算资源的成本，我们在较小的数据集 SciFact 上进行了实验，该数据集也在之前的工作中使用过（Dai et al., 2024c;a）。在此设置中，CDC 使用 Llama 重写的 DL19 文档来估计 β2，并随后在分别与每个 LLM 混合的 SciFact 语料库上纠正检索结果。

### 段落 86 · Page 10

**EN**

The results displayed in Table 3 confirm that CDC is capable to generalize across various LLMs and maintain high retrieval performance while effectively mitigating bias. In summary, these empirical results validate the feasibility of our proposed debiasing method by effectively reducing the biased impact of document perplexity on model outputs. And this method can be integrated efficiently into dual-encoder architerctures used in ANN search by pre-computing and indexing query-independent document perplexity with embeddings.

**中文**

表 3 中显示的结果证实，CDC 能够在各种法学硕士之间进行泛化，并保持较高的检索性能，同时有效地减少偏差。总之，这些实证结果通过有效减少文档困惑度对模型输出的偏差影响，验证了我们提出的去偏差方法的可行性。通过使用嵌入预先计算和索引与查询无关的文档困惑度，该方法可以有效地集成到 ANN 搜索中使用的双编码器架构中。

### 段落 87 · Page 10

**EN**

Moreover, ˆβ2 can be adjusted according to specific requirements, where a larger absolute value of ˆβ2 leads to further preference for human-written texts albeit at the potential cost of ranking performance degradation. More discussion about the open question that “Should we debias toward human-written contents?” is in Appendix A.1. 6 C ONCLUSION This paper aims to explain the phenomenon of source bias where PLM-based retrievers overrate lowperplexity documents. Our core conclusion is that PLM-based retrievers use perplexity features for relevance estimation, leading to source bias.

**中文**

此外，β2可以根据具体要求进行调整，其中β2的绝对值越大，就会导致对人类编写的文本的进一步偏好，尽管潜在的代价是排名性能下降。关于“我们应该消除对人类书写内容的偏见吗？”这个悬而未决的问题的更多讨论见附录 A.1。 6 结论 本文旨在解释基于 PLM 的检索器高估低困惑度文档的来源偏差现象。我们的核心结论是，基于 PLM 的检索器使用困惑度特征进行相关性估计，从而导致来源偏差。

### 段落 88 · Page 10

**EN**

To verify this, we conducted a two-stage IV regression and found a negative causal effect from perplexity to relevance estimation. Theoretic analysis reveals that the gradient correlation between language modeling and retrieval tasks contributes to this causal effect. Based on the analysis, a causal-inspired inference-time debiasing method called CDC is proposed. Experimental results verified its effectiveness in terms of debiasing the source bias. 10

**中文**

为了验证这一点，我们进行了两阶段 IV 回归，发现了困惑度与相关性估计之间的负因果效应。理论分析表明，语言建模和检索任务之间的梯度相关性促成了这种因果效应。基于分析，提出了一种称为 CDC 的因果推理时间去偏方法。实验结果验证了其在消除源偏置方面的有效性。 10

### Page 11

### 段落 89 · Page 11

**EN**

Published as a conference paper at ICLR 2025 7 A CKNOWLEDGEMENTS This work was funded by the National Key R&D Program of China (2023YFA1008704), the National Natural Science Foundation of China (62472426, 62276248, 62376275), the Youth Innovation Promotion Association CAS under Grants (2023111), fund for building world-class universities (disciplines) of Renmin University of China, the Fundamental Research Funds for the Central Universities, PCC@RUC, and the Research Funds of Renmin University of China (RUC24QSDL013).

**中文**

作为会议论文发表于 ICLR 2025 7 A 致谢 本工作得到国家重点研发计划项目（2023YFA1008704）、国家自然科学基金项目（62472426、62276248、62376275）、中国科学院青年创新促进会资助项目（2023111）、建设基金资助中国人民大学世界一流大学（学科）、中央高校基本科研业务费专项资金、PCC@RUC、中国人民大学科研基金项目（RUC24QSDL013）。

### 段落 90 · Page 11

**EN**

Work partially done at Engineering Research Center of Next-Generation Intelligent Search and Recommendation, Ministry of Education. REFERENCES Josh Achiam, Steven Adler, Sandhini Agarwal, Lama Ahmad, Ilge Akkaya, Florencia Leoni Aleman, Diogo Almeida, Janko Altenschmidt, Sam Altman, Shyamal Anadkat, et al. Gpt-4 technical report. arXiv preprint arXiv:2303.08774, 2023. Joshua D Angrist and Jörn-Steffen Pischke. Mostly harmless econometrics: An empiricist’s companion. Princeton university press, 2009. Guangsheng Bao, Yanbin Zhao, Zhiyang Teng, Linyi Yang, and Yue Zhang.

**中文**

部分工作在下一代智能搜索与推荐教育部工程研究中心完成。参考文献 Josh Achiam、Steven Adler、Sandhini Agarwal、Lama Ahmad、Ilge Akkaya、Florencia Leoni Aleman、Diogo Almeida、Janko Altenschmidt、Sam Altman、Shyamal Anadkat 等人。 Gpt-4 技术报告。 arXiv 预印本 arXiv:2303.08774, 2023。Joshua D Angrist 和 Jörn-Steffen Pischke。基本无害的计量经济学：经验主义者的伴侣。普林斯顿大学出版社，2009。包广生，赵彦斌，滕志阳，杨林一，张悦。

### 段落 91 · Page 11

**EN**

Fast-detectgpt: Efficient zero-shot detection of machine-generated text via conditional probability curvature. arXiv preprint arXiv:2310.05130, 2023. Gordon Burtch, Dokyun Lee, and Zhichen Chen. Generative ai degrades online communities. Communications of the ACM, 67(3):40–42, 2024. Yihan Cao, Siyu Li, Yixin Liu, Zhiling Yan, Yutong Dai, Philip S Yu, and Lichao Sun. A comprehensive survey of ai-generated content (aigc): A history of generative ai from gan to chatgpt. arXiv preprint arXiv:2303.04226, 2023. Xiaoyang Chen, Ben He, Hongyu Lin, Xianpei Han, Tianshu Wang, Boxi Cao, Le Sun, and Yingfei Sun.

**中文**

Fast-detectgpt：通过条件概率曲率对机器生成的文本进行高效的零样本检测。 arXiv 预印本 arXiv：2310.05130，2023。Gordon Burtch、Dokyun Lee 和zhichen Chen。生成式人工智能降低了在线社区的质量。 ACM 通讯，67(3):40–42，2024。Yihan Cao、Siyu Li、Yixin Liu、Zhiling Yan、Yutong Dai、Philip S Yu 和 Lichao Sun。人工智能生成内容（aigc）的全面调查：从 gan 到 chatgpt 的生成人工智能的历史。 arXiv 预印本 arXiv:2303.04226, 2023。陈晓阳、何本、林宏宇、韩先培、王天舒、曹博西、孙乐和孙英飞。

### 段落 92 · Page 11

**EN**

Spiral of silences: How is large language model killing information retrieval?–a case study on open domain question answering. Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics, 2024. Arman Cohan, Sergey Feldman, Iz Beltagy, Doug Downey, and Daniel S Weld. Specter: Document-level representation learning using citation-informed transformers. arXiv preprint arXiv:2004.07180, 2020. Nick Craswell, Bhaskar Mitra, Emine Yilmaz, Daniel Campos, and Ellen M V oorhees. Overview of the trec 2019 deep learning track. arXiv preprint arXiv:2003.07820, 2020.

**中文**

沉默的螺旋：大型语言模型如何杀死信息检索？——开放域问答的案例研究。计算语言学协会第 62 届年会论文集，2024 年。Arman Cohan、Sergey Feldman、Iz Beltagy、Doug Downey 和 Daniel S Weld。 Spectre：使用引用通知转换器进行文档级表示学习。 arXiv 预印本 arXiv：2004.07180，2020。Nick Craswell、Bhaskar Mitra、Emine Yilmaz、Daniel Campos 和 Ellen M V oorhees。 trec 2019 深度学习赛道概述。 arXiv 预印本 arXiv:2003.07820, 2020。

### 段落 93 · Page 11

**EN**

Sunhao Dai, Weihao Liu, Yuqi Zhou, Liang Pang, Rongju Ruan, Gang Wang, Zhenhua Dong, Jun Xu, and Ji-Rong Wen. Cocktail: A comprehensive information retrieval benchmark with llm-generated documents integration. Findings of the Association for Computational Linguistics: ACL 2024 , 2024a. Sunhao Dai, Chen Xu, Shicheng Xu, Liang Pang, Zhenhua Dong, and Jun Xu. Bias and unfairness in information retrieval systems: New challenges in the llm era. In Proceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining, pages 6437–6447, 2024b.

**中文**

戴孙浩、刘伟豪、周雨琪、庞亮、阮荣菊、王刚、董振华、徐军和温继荣。 Cocktail：与 llm 生成的文档集成的综合信息检索基准。计算语言学协会的调查结果：ACL 2024、2024a。戴孙浩、徐晨、徐世成、庞亮、董振华、徐军。信息检索系统中的偏见和不公平：LLM时代的新挑战。第 30 届 ACM SIGKDD 知识发现和数据挖掘会议记录，第 6437-6447 页，2024b。

### 段落 94 · Page 11

**EN**

Sunhao Dai, Yuqi Zhou, Liang Pang, Weihao Liu, Xiaolin Hu, Yong Liu, Xiao Zhang, Gang Wang, and Jun Xu. Neural retrievers are biased towards llm-generated content. In Proceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining, pages 526–537, 2024c. Sunhao Dai, Chen Xu, Shicheng Xu, Liang Pang, Zhenhua Dong, and Jun Xu. Unifying bias and unfairness in information retrieval: New challenges in the llm era. In Proceedings of the 18th ACM International Conference on Web Search and Data Mining, 2025. Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova.

**中文**

戴孙浩、周雨琪、庞亮、刘伟豪、胡晓林、刘勇、张晓、王刚和徐军。神经检索器偏向于 llm 生成的内容。第 30 届 ACM SIGKDD 知识发现和数据挖掘会议论文集，第 526-537 页，2024c。戴孙浩、徐晨、徐世成、庞亮、董振华、徐军。统一信息检索中的偏见和不公平：法学硕士时代的新挑战。 2025 年第 18 届 ACM 国际网络搜索和数据挖掘会议论文集。Jacob Devlin、Ming-Wei Chang、Kenton Lee 和 Kristina Toutanova。

### 段落 95 · Page 11

**EN**

Bert: Pre-training of deep bidirectional transformers for language understanding. arXiv preprint arXiv:1810.04805, 2018. 11

**中文**

Bert：用于语言理解的深度双向转换器的预训练。 arXiv 预印本 arXiv:1810.04805, 2018. 11

### Page 12

### 段落 96 · Page 12

**EN**

Published as a conference paper at ICLR 2025 Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. BERT: Pre-training of deep bidirectional transformers for language understanding. In Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, pages 4171–4186, 2019. Shaohua Fan, Xiao Wang, Yanhu Mo, Chuan Shi, and Jian Tang. Debiasing graph neural networks via learning disentangled causal substructure. Advances in Neural Information Processing Systems, 35:24934–24946, 2022. Luyu Gao and Jamie Callan.

**中文**

Jacob Devlin、Ming-Wei Chang、Kenton Lee 和 Kristina Toutanova 在 ICLR 2025 上作为会议论文发表。 BERT：用于语言理解的深度双向转换器的预训练。计算语言学协会北美分会 2019 年会议记录：人类语言技术，第 4171-4186 页，2019 年。范少华、王晓、莫彦虎、石川和唐健。通过学习解开的因果子结构来消除图神经网络的偏差。神经信息处理系统的进展，35：24934–24946，2022。Luyu Gau 和 Jamie Callan。

### 段落 97 · Page 12

**EN**

Unsupervised corpus aware language model pre-training for dense passage retrieval. In Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pages 2843–2853, 2022. Tianyu Gao, Xingcheng Yao, and Danqi Chen. Simcse: Simple contrastive learning of sentence embeddings. arXiv preprint arXiv:2104.08821, 2021. Charles Goodhart. Problems of monetary management: the uk experience in papers in monetary economics. Monetary Economics, 1, 1975. Josif Grabocka, Randolf Scholz, and Lars Schmidt-Thieme. Learning surrogate losses. arXiv preprint arXiv:1905.10108, 2019.

**中文**

用于密集段落检索的无监督语料库感知语言模型预训练。计算语言学协会第 60 届年会论文集（第一卷：长论文），第 2843-2853 页，2022 年。高天宇、姚兴成和陈丹琪。 Simcse：句子嵌入的简单对比学习。 arXiv 预印本 arXiv:2104.08821, 2021。查尔斯·古德哈特。货币管理问题：英国货币经济学论文中的经验。货币经济学，1，1975。Josif Grabocka、Randolf Scholz 和 Lars Schmidt-Thieme。学习替代损失。 arXiv 预印本 arXiv:1905.10108, 2019。

### 段落 98 · Page 12

**EN**

Jiafeng Guo, Yinqiong Cai, Yixing Fan, Fei Sun, Ruqing Zhang, and Xueqi Cheng. Semantic models for the first-stage retrieval: A comprehensive review. ACM Transactions on Information Systems (TOIS), 40(4):1–42, 2022. Jason Hartford, Greg Lewis, Kevin Leyton-Brown, and Matt Taddy. Deep iv: A flexible approach for counterfactual prediction. In International Conference on Machine Learning, pages 1414–1423. PMLR, 2017. Sebastian Hofstätter, Sheng-Chieh Lin, Jheng-Hong Yang, Jimmy Lin, and Allan Hanbury. Efficiently teaching an effective dense retriever with balanced topic aware sampling.

**中文**

郭家峰、蔡银琼、范艺兴、孙飞、张如青、程学奇。第一阶段检索的语义模型：综合回顾。 ACM 信息系统汇刊 (TOIS)，40(4):1–42，2022 年。Jason Hartford、Greg Lewis、Kevin Leyton-Brown 和 Matt Taddy。 Deep iv：一种灵活的反事实预测方法。国际机器学习会议，第 1414-1423 页。 PMLR，2017。Sebastian Hofstätter、Sheng-Chieh Lin、Jheng-Hong Yang、Jimmy Lin 和 Allan Hanbury。通过平衡的主题感知采样有效地教授有效的密集检索器。

### 段落 99 · Page 12

**EN**

In Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval, pages 113–122, 2021. Gautier Izacard, Mathilde Caron, Lucas Hosseini, Sebastian Riedel, Piotr Bojanowski, Armand Joulin, and Edouard Grave. Unsupervised dense information retrieval with contrastive learning. Transactions on Machine Learning Research, 2022. Kalervo Järvelin and Jaana Kekäläinen. Cumulated gain-based evaluation of ir techniques. ACM Transactions on Information Systems (TOIS), 20(4):422–446, 2002.

**中文**

第 44 届国际 ACM SIGIR 信息检索研究与开发会议记录，第 113-122 页，2021 年。Gautier Izacard、Mathilde Caron、Lucas Hosseini、Sebastian Riedel、Piotr Bojanowski、Armand Joulin 和 Edouard Grave。具有对比学习的无监督密集信息检索。机器学习研究汇刊，2022 年。Kalervo Järvelin 和 Jaana Kekäläinen。基于累积增益的红外技术评估。 ACM 信息系统汇刊 (TOIS)，20(4)：422–446，2002 年。

### 段落 100 · Page 12

**EN**

Albert Q Jiang, Alexandre Sablayrolles, Arthur Mensch, Chris Bamford, Devendra Singh Chaplot, Diego de las Casas, Florian Bressand, Gianna Lengyel, Guillaume Lample, Lucile Saulnier, et al. Mistral 7b. arXiv preprint arXiv:2310.06825, 2023. Bohan Li, Hao Zhou, Junxian He, Mingxuan Wang, Yiming Yang, and Lei Li. On the sentence embeddings from pre-trained language models. arXiv preprint arXiv:2011.05864, 2020. Jiawei Liu, Chunqiu Steven Xia, Yuyao Wang, and Lingming Zhang. Is your code generated by chatgpt really correct? rigorous evaluation of large language models for code generation.

**中文**

Albert Q Jiang、Alexandre Sablayrolles、Arthur Mensch、Chris Bamford、Devendra Singh Chaplot、Diego de las Casas、Florian Bressand、Gianna Lengyel、Guillaume Lample、Lucile Saulnier 等。米斯特拉尔 7b. arXiv 预印本 arXiv:2310.06825, 2023。Bohan Li、Hao Zhou、Junxian He、Mingxuan Wang、Yiming Yang 和 Lei Li。关于预训练语言模型的句子嵌入。 arXiv 预印本 arXiv:2011.05864, 2020。Jiawei Liu、Chunqiu Steven Xia、Yuyao Wang 和 Lingming Zhang。你的chatgpt生成的代码真的正确吗？用于代码生成的大型语言模型的严格评估。

### 段落 101 · Page 12

**EN**

Advances in Neural Information Processing Systems, 36, 2024. Yinhan Liu, Myle Ott, Naman Goyal, Jingfei Du, Mandar Joshi, Danqi Chen, Omer Levy, Mike Lewis, Luke Zettlemoyer, and Veselin Stoyanov. Roberta: A robustly optimized bert pretraining approach. arXiv preprint arXiv:1907.11692, 2019. Eric Mitchell, Yoonho Lee, Alexander Khazatsky, Christopher D Manning, and Chelsea Finn. Detectgpt: Zero-shot machine-generated text detection using probability curvature. InInternational Conference on Machine Learning, pages 24950–24962. PMLR, 2023. Michael Mitzenmacher and Eli Upfal.

**中文**

神经信息处理系统进展，36，2024。Yinhan Liu、Myle Ott、Naman Goyal、Jingfei Du、Mandar Joshi、Danqi Chen、Omer Levy、Mike Lewis、Luke Zettlemoyer 和 Veselin Stoyanov。 Roberta：一种稳健优化的 bert 预训练方法。 arXiv 预印本 arXiv：1907.11692，2019。Eric Mitchell、Yoonho Lee、Alexander Khazatsky、Christopher D Manning 和 Chelsea Finn。 Detectgpt：使用概率曲率的零样本机器生成文本检测。国际机器学习会议，第 24950-24962 页。 PMLR，2023。Michael Mitzenmacher 和 Eli Upfal。

### 段落 102 · Page 12

**EN**

Probability and computing: Randomization and probabilistic techniques in algorithms and data analysis. Cambridge university press, 2017. 12

**中文**

概率与计算：算法和数据分析中的随机化和概率技术。剑桥大学出版社，2017. 12

### Page 13

### 段落 103 · Page 13

**EN**

Published as a conference paper at ICLR 2025 Niklas Muennighoff, Nouamane Tazi, Loïc Magne, and Nils Reimers. Mteb: Massive text embedding benchmark. arXiv preprint arXiv:2210.07316, 2022. XuanLong Nguyen, Martin J Wainwright, and Michael I Jordan. On surrogate loss functions and f-divergences. 2009. Masanari Ohi, Masahiro Kaneko, Ryuto Koike, Mengsay Loem, and Naoaki Okazaki. Likelihoodbased mitigation of evaluation bias in large language models. arXiv preprint arXiv:2402.15987, 2024. N Reimers. Sentence-bert: Sentence embeddings using siamese bert-networks. arXiv preprint arXiv:1908.10084, 2019.

**中文**

作为 ICLR 2025 Niklas Muennighoff、Nouamane Tazi、Loïc Magne 和 Nils Reimers 的会议论文发表。 Mteb：大规模文本嵌入基准。 arXiv 预印本 arXiv：2210.07316，2022。XuanLong Nguyen、Martin J Wainwright 和 Michael I Jordan。关于替代损失函数和 f 散度。 2009. 大井正成、金子正宏、小池龙人、Mengsay Loem 和冈崎直明。基于似然的大型语言模型中评估偏差的缓解。 arXiv 预印本 arXiv:2402.15987, 2024。N Reimers。 Sentence-bert：使用暹罗 bert 网络的句子嵌入。 arXiv 预印本 arXiv:1908.10084, 2019。

### 段落 104 · Page 13

**EN**

Gerard Salton, Anita Wong, and Chung-Shu Yang. A vector space model for automatic indexing. Communications of the ACM, 18(11):613–620, 1975. Ilia Shumailov, Zakhar Shumaylov, Yiren Zhao, Yarin Gal, Nicolas Papernot, and Ross Anderson. The curse of recursion: Training on generated data makes models forget. arXiv preprint arXiv:2305.17493, 2023. Rickard Stureborg, Dimitris Alikaniotis, and Yoshi Suhara. Large language models are inconsistent and biased evaluators. arXiv preprint arXiv:2405.01724, 2024. Hexiang Tan, Fei Sun, Wanli Yang, Yuanzhuo Wang, Qi Cao, and Xueqi Cheng.

**中文**

杰拉德·索尔顿、安妮塔·王和杨忠书。用于自动索引的向量空间模型。 ACM 通讯，18(11):613–620, 1975。Ilia Shumailov、Zakhar Shumaylov、Yiren Zhu、Yarin Gal、Nicolas Papernot 和 Ross Anderson。递归的诅咒：对生成的数据进行训练会使模型忘记。 arXiv 预印本 arXiv：2305.17493，2023。Rickard Stureborg、Dimitris Alikaniotis 和 Yoshi Suhara。大型语言模型是不一致且有偏见的评估器。 arXiv 预印本 arXiv:2405.01724, 2024。谭鹤翔、孙飞、杨万里、王元卓、曹奇和程学奇。

### 段落 105 · Page 13

**EN**

Blinded by generated contexts: How language models merge generated and retrieved contexts for open-domain qa? Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics, 2024. Hugo Touvron, Louis Martin, Kevin Stone, Peter Albert, Amjad Almahairi, Yasmine Babaei, Nikolay Bashlykov, Soumya Batra, Prajjwal Bhargava, Shruti Bhosale, et al. Llama 2: Open foundation and fine-tuned chat models. arXiv preprint arXiv:2307.09288, 2023. Ellen V oorhees, Tasmeer Alam, Steven Bedrick, Dina Demner-Fushman, William R Hersh, Kyle Lo, Kirk Roberts, Ian Soboroff, and Lucy Lu Wang.

**中文**

被生成的上下文蒙蔽：语言模型如何合并生成和检索的上下文以进行开放域问答？计算语言学协会第 62 届年会论文集，2024 年。Hugo Touvron、Louis Martin、Kevin Stone、Peter Albert、Amjad Almahairi、Yasmine Babaei、Nikolay Bashlykov、Soumya Batra、Prajjwal Bhargava、Shruti Bhosale 等。 Llama 2：开放基础和微调的聊天模型。 arXiv 预印本 arXiv：2307.09288，2023。Ellen V oorhees、Tasmeer Alam、Steven Bedrick、Dina Demner-Fushman、William R Hersh、Kyle Lo、Kirk Roberts、Ian Soboroff 和 Lucy Lu Wang。

### 段落 106 · Page 13

**EN**

Trec-covid: constructing a pandemic information retrieval test collection. In ACM SIGIR Forum, volume 54, pages 1–12. ACM New York, NY , USA, 2021. Lee Xiong, Chenyan Xiong, Ye Li, Kwok-Fung Tang, Jialin Liu, Paul Bennett, Junaid Ahmed, and Arnold Overwijk. Approximate nearest neighbor negative contrastive learning for dense text retrieval. arXiv preprint arXiv:2007.00808, 2020. Shicheng Xu, Danyang Hou, Liang Pang, Jingcheng Deng, Jun Xu, Huawei Shen, and Xueqi Cheng. Ai-generated images introduce invisible relevance bias to text-image retrieval.

**中文**

Trec-covid：构建流行病信息检索测试集。 ACM SIGIR 论坛，第 54 卷，第 1-12 页。 ACM 美国纽约州纽约，2021 年。Lee Xiong、Chenyan Xiong、Ye Li、Kwok-Fung Tang、Jialin Liu、Paul Bennett、Junaid Ahmed 和 Arnold Overwijk。用于密集文本检索的近似最近邻负对比学习。 arXiv 预印本 arXiv:2007.00808, 2020。徐世成、侯丹阳、庞亮、邓景城、徐军、沉华为和程学奇。人工智能生成的图像给文本图像检索带来了隐形的相关性偏差。

### 段落 107 · Page 13

**EN**

Proceedings of the 47th international ACM SIGIR conference on research and development in information retrieval, 2024. Wayne Xin Zhao, Kun Zhou, Junyi Li, Tianyi Tang, Xiaolei Wang, Yupeng Hou, Yingqian Min, Beichen Zhang, Junjie Zhang, Zican Dong, et al. A survey of large language models. arXiv preprint arXiv:2303.18223, 2023. Wayne Xin Zhao, Jing Liu, Ruiyang Ren, and Ji-Rong Wen. Dense text retrieval based on pretrained language models: A survey. ACM Transactions on Information Systems, 42(4):1–60, 2024. Lianmin Zheng, Wei-Lin Chiang, Ying Sheng, Siyuan Zhuang, Zhanghao Wu, Yonghao Zhuang, Zi Lin, Zhuohan Li, Dacheng Li, Eric Xing, et al.

**中文**

第 47 届国际 ACM SIGIR 信息检索研究与开发会议论文集，2024 年。 Wayne Xin Zhao、Kun Zhou、Junyi Li、Tianyi Tang、Xiaolei Wang、Yupeng Hou、Yingqian Min、Beichen Zhang、Junjie Zhang、Zican Dong 等。大型语言模型的调查。 arXiv 预印本 arXiv:2303.18223, 2023。Wayne Xin Zhao、Jing Liu、Ruiyang Ren 和 Ji-Rong Wen。基于预训练语言模型的密集文本检索：一项调查。 ACM 信息系统学报，42(4):1–60, 2024。Lianmin Cheng、Wei-Lin Jiang、Ying Shen、Siyuan Zhuang、Zhanghao Wu、Yonghao Zhuang、Zi Lin、Zzhuohan Li、Da Cheng Li、Eric Xing 等。

### 段落 108 · Page 13

**EN**

Judging llm-as-a-judge with mt-bench and chatbot arena. Advances in Neural Information Processing Systems, 36, 2024. Yuqi Zhou, Sunhao Dai, Liang Pang, Gang Wang, Zhenhua Dong, Jun Xu, and Ji-Rong Wen. Source echo chamber: Exploring the escalation of source bias in user, data, and recommender system feedback loop. arXiv preprint arXiv:2405.17998, 2024. 13

**中文**

使用 mt-bench 和聊天机器人竞技场对 llm 进行评判。神经信息处理系统进展，36，2024。Yuqi Zhou、Sunhao Dai、Liang Pang、Gang Wang、Zhenhua Dong、Jun Xu 和 Ji-Rong Wen。源回声室：探索用户、数据和推荐系统反馈循环中源偏差的升级。 arXiv 预印本 arXiv:2405.17998, 2024. 13

### Page 14

### 段落 109 · Page 14

**EN**

Published as a conference paper at ICLR 2025 A D ISCUSSION A.1 S HOULD WE DEBIAS TOWARD HUMAN -WRITTEN CONTENTS ? While we refer to the retrievers’ preference for LLM-rewritten content as a “bias”, it’s crucial to recognize that not all biases are harmful. As illustrated in previous works (Dai et al., 2024c; Zhou et al., 2024), from content creators’ perspective, reducing preference toward LLM-rewritten content helps guarantee sufficient incentives for authors to encourage creativity, and thus sustain a healthier content ecosystem.

**中文**

作为会议论文发表于 ICLR 2025 A DISCUSSION A.1 我们是否应该消除对人类书写内容的偏见？虽然我们将检索者对法学硕士重写内容的偏好称为“偏见”，但重要的是要认识到并非所有偏见都是有害的。正如之前的研究（Dai et al.，2024c；Zhou et al.，2024）所示，从内容创作者的角度来看，减少对LLM重写内容的偏好有助于保证作者有足够的动力来鼓励创造力，从而维持更健康的内容生态系统。

### 段落 110 · Page 14

**EN**

From users’ perspective, LLM-rewritten documents might possess enhanced quality, such as better coherence, and improved reading experience. In this work, our debiasing approach is primarily a methodological application derived from our causal graph analysis, serving to validate the “perplexity-trap” hypothesis further. At the same time, our framework allows for adjustable preference levels between human-written and LLM-generated documents, catering to specific practical requirements. This flexibility ensures our approach can be tailored to balance between enhancing information quality and maintaining content provider fairness.

**中文**

从用户的角度来看，LLM重写的文档可能具有更高的质量，例如更好的连贯性和更好的阅读体验。在这项工作中，我们的去偏方法主要是源自因果图分析的方法应用，旨在进一步验证“困惑陷阱”假设。同时，我们的框架允许在人工编写的文档和法学硕士生成的文档之间调整偏好级别，以满足特定的实际需求。这种灵活性确保我们的方法可以量身定制，以在提高信息质量和维护内容提供商公平性之间取得平衡。

### 段落 111 · Page 14

**EN**

A.2 S HOULD PERPLEXITY BE A CAUSAL FACTOR TO QUERY-D OCUMENT RELEVANCE ? It’s one of the assumptions of this work that perplexity should not be a causal factor to querydocument relevance. It is true that there may be a correlation between perplexity and query-document relevance, e.g., the coherence of a document may also have an impact on relevance. However, there is an insurmountable gap between the perplexity of LLM-rewritten documents and human work, because people do not intentionally take PPL into account when writing, but LLMs do generation with perplexity as a goal.

**中文**

A.2 困惑是否应该成为查询文档相关性的一个原因？这项工作的假设之一是困惑不应该成为查询文档相关性的因果因素。确实，困惑度和查询文档相关性之间可能存在相关性，例如，文档的连贯性也可能对相关性产生影响。然而，LLM重写的文档的困惑度与人类工作之间存在着不可逾越的差距，因为人们在写作时并没有刻意考虑PPL，但LLM却以困惑度为目标进行生成。

### 段落 112 · Page 14

**EN**

We are currently faced with a situation where this perplexity gap has breached the range of human perception of relevance, leading to serious source bias even when the rewritten documents share nearly the same semantics with human works, as verified and discussed in previous literature (Dai et al., 2024c). It’s just like what Goodhart’s Law (Goodhart, 1975) states: “When a measure becomes a target, it ceases to be a good measure.” So perhaps a threshold should be set, and when perplexity is less than the threshold, it should be made independent with relevance.

**中文**

我们目前面临的情况是，这种困惑度差距已经突破了人类感知相关性的范围，即使重写的文档与人类作品具有几乎相同的语义，也会导致严重的来源偏差，正如之前的文献所验证和讨论的那样（Dai et al., 2024c）。就像古德哈特定律（Goodhart，1975）所说：“当一项措施成为目标时，它就不再是一个好的措施。”所以也许应该设置一个阈值，当困惑度小于阈值时，应该使其与相关性无关。

### 段落 113 · Page 14

**EN**

B L IMITATIONS This study has several limitations that are important to acknowledge. Data and Experiments. Firstly, while our analysis was conducted on three representative datasets, it is recognized that there are numerous other IR datasets that could have been included. Our selection, although limited in scope, was strategic to ensure a broad representation across different domains, and we believe that our findings can be generalized to other domains. Secondly, due to the cost associated with human evaluation, we were constrained to perform only 6 × 20 evaluations for each dataset, corresponding to six different sampling temperatures.

**中文**

局限性 这项研究有几个必须承认的局限性。数据和实验。首先，虽然我们的分析是对三个代表性数据集进行的，但我们认识到还可以包括许多其他 IR 数据集。我们的选择虽然范围有限，但具有战略意义，以确保在不同领域具有广泛的代表性，并且我们相信我们的发现可以推广到其他领域。其次，由于与人工评估相关的成本，我们只能对每个数据集执行 6 × 20 次评估，对应于六个不同的采样温度。

### 段落 114 · Page 14

**EN**

This decision, while pragmatic, may limit the extent to which we can generalize our results to other conditions. Thirdly, we have to admit that impacts of LLM rewriting on semantics indeed lack more consideration although they have been designed possibly credible. Since simulated environment construction is not our main contribution, we have adopted the datasets provided by previous works (Dai et al., 2024b) or follow their methodology (Dai et al., 2024c) to evaluate the source bias of retrievers. In Dai et al.

**中文**

这一决定虽然务实，但可能会限制我们将结果推广到其他条件的程度。第三，我们不得不承认LLM重写对语义的影响确实缺乏更多的考虑，尽管它们的设计可能是可信的。由于模拟环境构建不是我们的主要贡献，因此我们采用了先前作品提供的数据集（Dai et al., 2024b）或遵循他们的方法（Dai et al., 2024c）来评估检索器的源偏差。在戴等人。

### 段落 115 · Page 14

**EN**

(2024c), the document embeddings are compared using cosine similarity, and a more detailed human evaluation was conducted to assess the various impacts of LLM rewriting, which indicated no significant changes in document semantics. We will conduct more meticulous semantic checks to pursue more rigorous conclusions if possible. Theoretical Analysis In our theoretical proofs, we made certain assumptions and simplifications. Specifically, we narrow our analysis in PLM-based dual-encoder and mean-pooling scenario.

**中文**

(2024c)，使用余弦相似度比较文档嵌入，并进行更详细的人工评估来评估 LLM 重写的各种影响，这表明文档语义没有显着变化。如果可能的话，我们将进行更细致的语义检查，以得出更严格的结论。理论分析在我们的理论证明中，我们做出了某些假设和简化。具体来说，我们缩小了基于 PLM 的双编码器和均值池场景的分析范围。

### 段落 116 · Page 14

**EN**

These are necessary to achieve mathematical tractability and are grounded in practical considerations, which have been discussed in the previous sections. We believe these assumptions are reasonable and have validated the reliability of our conclusions through experimental verification. For the other scenarios, such as auto-regressive embedding models and CLS-based retrievers, we will explore and discuss them in the future work. 14

**中文**

这些对于实现数学易处理性是必要的，并且基于实际考虑，这些已经在前面的章节中讨论过。我们认为这些假设是合理的，并通过实验验证验证了我们结论的可靠性。对于其他场景，例如自回归嵌入模型和基于 CLS 的检索器，我们将在未来的工作中进行探索和讨论。 14

### Page 15

### 段落 117 · Page 15

**EN**

Published as a conference paper at ICLR 2025 Despite these limitations, we maintain that our work provides valuable insights into the subject matter and serves as a foundation for future research. C N OTES ON THEORETICAL ANALYSIS In this section, we provide detailed reasons to our assumptions and proof to our proposed theorem in Section 4.2. C.1 E XPLANATION ON ASSUMPTIONS Our theoretical analysis are based on a set of assumptions, to which we’re going to offer the reasons.

**中文**

作为 ICLR 2025 会议论文发表 尽管存在这些限制，我们仍然认为我们的工作提供了对该主题的宝贵见解，并可作为未来研究的基础。关于理论分析的注释 在本节中，我们提供了我们的假设的详细理由以及我们在 4.2 节中提出的定理的证明。 C.1 对假设的解释 我们的理论分析基于一组假设，我们将对此给出理由。

### 段落 118 · Page 15

**EN**

•Encoder-Only Retrievers Encoder-only architectures are generally considered more suitable for textual representation tasks, while encoder-decoder and decoder-only models are typically used for generative tasks. Thus, encoder-only models have been widely employed for retrieval tasks and have demonstrated effective results. In fact, most of the mainstream dense retrievers listed on the MTEB (Muennighoff et al., 2022) leaderboard are based on encoder-only architectures. •Mean-Pooling Strategy.

**中文**

•仅编码器检索器 仅编码器架构通常被认为更适合文本表示任务，而编码器-解码器和仅解码器模型通常用于生成任务。因此，仅编码器模型已广泛应用于检索任务，并展示了有效的结果。事实上，MTEB（Muennighoff 等人，2022）排行榜上列出的大多数主流密集检索器都基于纯编码器架构。 • 均值池策略。

### 段落 119 · Page 15

**EN**

We use of mean pooling for query/doc embeddings in the derivation of Theorem 1, while a simplification, differs from the practice of using CLS token embeddings in BERT-like models. From a practical perspective, (weighted) mean pooling embedding outperform CLS token embedding when ranking, which has been widely confirmed in previous works (Dai et al., 2024b; Reimers, 2019). From a theoretical perspective, (weighted) mean pooling is able to retain more local information about documents, which is important for retrieval tasks, as a query is regarded related to a document when the query is related to a particular sentence in the document.

**中文**

我们在推导定理 1 时对查询/文档嵌入使用均值池化，虽然是一种简化，但与在类 BERT 模型中使用 CLS 令牌嵌入的实践不同。从实际角度来看，（加权）均值池嵌入在排名时优于 CLS 令牌嵌入，这在之前的工作中已得到广泛证实（Dai 等人，2024b；Reimers，2019）。从理论角度来看，（加权）均值池能够保留更多有关文档的本地信息，这对于检索任务很重要，因为当查询与文档中的特定句子相关时，查询被视为与文档相关。

### 段落 120 · Page 15

**EN**

Furthermore, there is literature indicating that CLS token embeddings may not always effectively capture sentence representations, which can be a limitation in retrieval contexts (Li et al., 2020). • Representation Collinearity Hypothesis Representation Collinearity Hypothesis is a fundamental assumption long implemented in information retrieval systems (Salton et al., 1975). When measuring relevance scores by calculating dot or cosine similarity, we assume that the best relevant document owns an embedding that is collinear with the query embedding (given that the norm of the document embedding is held constant).

**中文**

此外，有文献表明 CLS 令牌嵌入可能并不总是有效地捕获句子表示，这可能是检索上下文的限制（Li et al., 2020）。 • 表示共线性假设 表示共线性假设是信息检索系统中长期实施的一个基本假设（Salton 等人，1975）。当通过计算点或余弦相似度来测量相关性分数时，我们假设最佳相关文档拥有与查询嵌入共线的嵌入（假定文档嵌入的范数保持不变）。

### 段落 121 · Page 15

**EN**

In practice, dense retrievers are trained on contrastive learning to maximize the similarity between query and its relevant documents while minimize the similarity of irrelevant documents (Gao et al., 2021; Zhao et al., 2024). • Semi-Orthogonal Weight Matrix Hypothesis W ∈ RN ×D satisfies the Semi-Orthogonal Weight Matrix assumption W W T = IN , which is necessary to achieve mathematical tractability. Since practical PLMs uses 2-layer MLPs rather than the weight matrix W , this can’t be verified directly.

**中文**

在实践中，密集检索器经过对比学习的训练，以最大化查询与其相关文档之间的相似性，同时最小化不相关文档的相似性（Gao et al., 2021；Zhao et al., 2024）。 • 半正交权重矩阵假设W ∈ RN ×D 满足半正交权重矩阵假设W W T = IN，这是实现数学易处理性所必需的。由于实际 PLM 使用 2 层 MLP 而不是权重矩阵 W，因此无法直接验证。

### 段落 122 · Page 15

**EN**

If we ignore the activation function in the MLPs of BERT, let W = W1W2, then 1 N 2 ∥W W T ∥F ≈ 50 · 1 N 2 ∥diag(W W T )∥F , which suggests that the diagonal elements are much larger than the others. One reasonable intuition is a conclusion in high-dimension probabilities which states "for any ϵ > 0, there are m = Ω(eN) vectors in RN such that any pair of them are nearly orthogonal."(Mitzenmacher and Upfal, 2017) Since N ≥ 768 for commonly-used retrievers, the hypothesis holds with high probability. • Encoder-decoder Cooperation Hypothesis This assumption has a certain practical background.

**中文**

如果我们忽略 BERT 的 MLP 中的激活函数，令 W = W1W2，则 1 N 2 ∥W W T ∥F ≈ 50 · 1 N 2 ∥diag(W W T )∥F，这表明对角线元素比其他元素大得多。一个合理的直觉是高维概率的结论，其中指出“对于任何 ϵ > 0，RN 中存在 m = Ω(eN) 向量，使得它们中的任何一对几乎正交。”（Mitzenmacher 和 Upfal，2017）由于常用检索器的 N ≥ 768，因此该假设成立的概率很高。 • 编码器-解码器合作假设 该假设有一定的实际背景。

### 段落 123 · Page 15

**EN**

The experiment in Section4 can be viewed as a verification of this assumption, where finetuned encoder is used with unfinetuned MLPs to do MLM task. In this setting, the hybrid model recieve relatively low perplexity as PLMs. In practice, the beginning learning rate of finetuning retrievers is usually set at 1 · e−5, which makes retrievers more likely to the conserve of inversion property. C.2 P ROOF OF THEOREM 1 In this section, we provide the proof of Theorem 1. Note that the three conditions made are naturally satisfied: (1) Representation collinearity is a fundamental assumption long implemented in information retrieval systems.

**中文**

第 4 节中的实验可以看作是对这一假设的验证，其中微调的编码器与未微调的 MLP 一起使用来执行 MLM 任务。在此设置中，混合模型与 PLM 相比具有相对较低的复杂度。在实践中，微调检索器的起始学习率通常设置为1·e−5，这使得检索器更有可能保持反转性质。 C.2 定理 1 的证明 在本节中，我们提供定理 1 的证明。注意，所提出的三个条件自然满足： (1) 表示共线性是信息检索系统中长期实现的基本假设。

### 段落 124 · Page 15

**EN**

(2) Matrix orthogonality is a common and intuitive property of the decoder’s weight matrix. (3) Encoder-decoder adheres to the original design principles of auto-encoder networks. Then we give the proof as follows: Proof. Given the following three conditions: 15

**中文**

(2) 矩阵正交性是解码器权重矩阵的一个常见且直观的属性。 (3)编码器-解码器遵循自动编码器网络的原始设计原则。那么我们给出证明如下： 证明。给定以下三个条件： 15

### Page 16

### 段落 125 · Page 16

**EN**

Published as a conference paper at ICLR 2025 •Representation Collinearity: the embedding vectors of relevant query-document pairs are collinear after mean pooling, i.e., 1L×Lf(q) = λ1L×Lf(d). • Orthogonal Weight Matrix: the weight matrix of the decoder is orthogonal, i.e., W W T = I. • Encoder-decoder cooperation: fine-tuning does not disrupt the corresponding function between encoder and decoder, i.e., f(d) = g−1(d). Our goal is to prove ∂L2/∂demb = K ⊙ ∂L1/∂demb. Note that the two losses are both involved with demb, ∂L1 ∂demb = − 1 L 1L×L[g(demb) − d]W T = − 1 L 1L×L[σ(dembW ) − d]W T . ∂L2 ∂demb = − 1 L2 1L×Lqemb.

**中文**

在 ICLR 2025 上作为会议论文发表。 •表示共线性：相关查询文档对的嵌入向量在均值池化后是共线的，即 1L×Lf(q) = λ1L×Lf(d)。 • 正交权重矩阵：解码器的权重矩阵是正交的，即 W W T = I。 • 编码器-解码器协作：微调不会破坏编码器和解码器之间的相应功能，即 f(d) = g−1(d)。我们的目标是证明 ∂L2/∂demb = K ⊙ ∂L1/∂demb。请注意，这两个损失都与 demb 相关， ∂L1 ∂demb = − 1 L 1L×L[g(demb) − d]W T = − 1 L 1L×L[σ(dembW ) − d]W T。 ∂L2 ∂demb = − 1 L2 1L×Lqemb。

### 段落 126 · Page 16

**EN**

Replacing the softmax operation with linear normalization, let · · denote element-wise division, [σ(x)]l = 1PN n xln xl, l = 1, . . . , L. Considering the following matrix identity, (AM ×N · BN ×K) ⊙ (cM · 1T K) = (AM ×N ⊙ (cM · 1T N)) · BN ×K, it reveals that the gradient of L1 can be rearranged as [σ(dembW ) − d]W T = ( dembW kL1T D − d)W T = ( demb kL1T N W − d)W T , where column vector kL ∈ RL satisfies kl = PD d (dembW )ld > 0 because σ(dembW )l is a complex. Meanwhile, using mean inequality (also called QM-AM inequality), we can find that kl ≤ vuut 1 N DX d (dembW )2 ld = r 1 N (dembW )l(dembW )T l = 1√ N ∥demb l ∥2 = 1√ N < 1.

**中文**

用线性归一化代替 softmax 运算，令·· 表示逐元素除法，[σ(x)]l = 1PN n xln xl, l = 1,...。。。 , L. 考虑以下矩阵恒等式 (AM ×N · BN ×K) ⊙ (cM · 1T K) = (AM ×N ⊙ (cM · 1T N)) · BN ×K，表明 L1 的梯度可以重新排列为 [σ(dembW ) − d]W T = ( dembW kL1T D − d)W T = ( demb kL1T N W − d)W T，其中列向量 kL ∈ RL 满足 kl = PD d (dembW )ld > 0 因为 σ(dembW )l 是复数。同时，利用均值不等式（也称为 QM-AM 不等式），我们可以发现 kl ≤ vuut 1 N DX d (dembW )2 ld = r 1 N (dembW )l(dembW )T l = 1√ N ∥demb l ∥2 = 1√ N < 1。

### 段落 127 · Page 16

**EN**

According to the orthogonal weight matrix assumption, ( demb kL1T N W − d)W T = demb kL1T N − dW T = demb kL1T N − σ−1(d)W T = demb kL1T N − g−1(d). From the encoder-decoder cooperation condition, we obtain ∂L1 ∂demb = − 1 L 1L×L[ demb kL1T N −f(d)] = − 1 L 1L×L[demb⊙( 1L − kL kL 1T N)] = − 1 L 1L×Ldiag( 1L − kL kL )demb. Considering the positive query-document pair q, d, assume their embedding vectors are collinear, ∂L2 ∂demb = − 1 L2 1L×Lqemb = − λ L2 1L×Ldemb. we can observe that ∂L2 ∂demb = λ Ldiag( kL 1L − kL ) ∂L1 ∂demb . Let K = λ L kL 1L−kL 1T N , then it holds that ∂L2 ∂demb = K ⊙ ∂L1 ∂demb . 16

**中文**

根据正交权重矩阵假设， ( demb kL1T N W − d)W T = demb kL1T N − dW T = demb kL1T N − σ−1(d)W T = demb kL1T N − g−1(d)。根据编解码器协作条件，我们得到 ∂L1 ∂demb = − 1 L 1L×L[ demb kL1T N −f(d)] = − 1 L 1L×L[demb⊙( 1L − kL kL 1T N)] = − 1 L 1L×Ldiag( 1L − kL kL )demb。考虑正查询文档对 q、d，假设它们的嵌入向量共线，∂L2 ∂demb = − 1 L2 1L×Lqemb = − λ L2 1L×Ldemb。我们可以观察到 ∂L2 ∂demb = λ Ldiag( kL 1L − kL ) ∂L1 ∂demb。令K = λ L kL 1L−kL 1T N，则有∂L2 ∂demb = K ⊙ ∂L1 ∂demb。 16

### Page 17

### 段落 128 · Page 17

**EN**

Published as a conference paper at ICLR 2025 𝑆𝑑 Outcome 𝑀𝑑 𝑀𝑞 𝑅𝑞,𝑑 ෠𝑅𝑞,𝑑 Treatment Reconstruction Instrumental Variable Confounder ෨𝑃𝑑 ෠𝑃𝑑 𝑃𝑑 𝑆𝑑 𝑀𝑑 𝑀𝑞 𝑅𝑞,𝑑 ෠𝑅𝑞,𝑑 Confounder ෨𝑃𝑑 ෠𝑃𝑑 መ𝛽1 መ𝛽2 𝑃𝑑 Instrumental Variable Outcome Treatment Figure 4: By leveraging IV regression on Sd, Pd is decomposed into causal and non-causal parts. A precise causal effect can be obtained from the coefficient of the second-stage regression, i.e., ˆβ2. D I NSTRUMENTAL VARIABLE REGRESSION In statistics, instrumental variable (IV) is used to estimate causal effects. The changes of IV induces changes of explanatory variable but keeps error term constant.

**中文**

在 ICLR 2025 上作为会议论文发表 𝑆𝑑 结果 𝑀𝑑 𝑀𝑞 𝑅𝑞,𝑑 ෠𝑅𝑞,𝑑 治疗重建工具变量混杂因素 ෨𝑃𝑑 ෠𝑃𝑑 𝑃𝑑 𝑆𝑑 𝑀𝑑 𝑀𝑞 𝑅𝑞,𝑑 ෠𝑅𝑞,𝑑 混杂因素 ෨𝑃𝑑 ෠𝑃𝑑 መ𝛽1 መ𝛽2 𝑃𝑑 工具变量结果处理 图 4：通过利用 Sd 上的 IV 回归，Pd 被分解为因果部分和非因果部分。从第二阶段回归的系数 ^β2 可以得到精确的因果效应。工具变量回归 在统计学中，工具变量（IV）用于估计因果效应。 IV 的变化引起解释变量的变化，但保持误差项不变。

### 段落 129 · Page 17

**EN**

The basic method to estimate causal effect is 2SLS. In the first stage, 2SLS regress explanatory variable on instrumental variable and obtain the predicted values of explanatory variable. In the second stage, 2SLS regress output variable on predicted explanatory variable. Then, the coefficient corresponding to the predicted explanatory variable can be viewed as a measure of causal effects. According to our proposed causal graph, the document source Sd has three properties: (1) It is correlated to the document perplexity Pd.

**中文**

估计因果效应的基本方法是2SLS。第一阶段，2SLS对工具变量进行解释变量回归，得到解释变量的预测值。在第二阶段，2SLS 将输出变量回归到预测的解释变量上。然后，与预测的解释变量对应的系数可以被视为因果效应的度量。根据我们提出的因果图，文档源 Sd 具有三个属性：（1）它与文档困惑度 Pd 相关。

### 段落 130 · Page 17

**EN**

(2) It is independent with Document semantics Md because we can instruct LLMs to rewrite human documents for any document semantics. (3) It only affect the estimated relevance score ˆRq,d through document perplexity Pd. Thus, document source Sd can be considered a instrumental variable to evaluate the causal effect of document perplexity on estimated relevance scores. As depicted in Figure 4, we estimate document perplexity Pd based on document source Sd in the first stage.

**中文**

(2) 它与文档语义 Md 无关，因为我们可以指示 LLM 为任何文档语义重写人类文档。 (3)它仅影响通过文档困惑度Pd估计的相关性得分^Rq,d。因此，文档来源 Sd 可以被认为是一个工具变量，用于评估文档困惑度对估计相关性分数的因果影响。如图 4 所示，我们在第一阶段根据文档源 Sd 估计文档困惑度 Pd。

### 段落 131 · Page 17

**EN**

The results, coefficient ˆβ1 and predicted document perplexity ˆPd = ˆβ1Sd, are used in the second stage to estimated the predicted relevance score ˆRq,d via linear regression, where the estimated coefficient ˆβ2 is a valid measure for the magnitude of the causal effect. E M ORE EXPERIMENTS E.1 E XPERIMENTAL DETAILS Our experiments are all conducted on machines equipped with NVIDIA A6000 GPUs and 52-core Intel(R) Xeon(R) Gold 6230R CPUs at 2.10GHz. For better reproducibility, we employ the following officially released checkpoints: BERT (Devlin et al., 2018; 2019) and RoBERTa (Liu et al., 2019) are used in dense retrieval as PLM encoders.

**中文**

结果系数 β1 和预测文档困惑度 βPd = β1Sd 在第二阶段用于通过线性回归估计预测相关性得分 βRq,d，其中估计系数 β2 是因果效应大小的有效度量。更多实验 E.1 实验细节 我们的实验均在配备 NVIDIA A6000 GPU 和 52 核 Intel(R) Xeon(R) Gold 6230R CPU（频率为 2.10GHz）的机器上进行。为了更好的再现性，我们采用以下官方发布的检查点：BERT（Devlin et al., 2018; 2019）和 RoBERTa（Liu et al., 2019）作为 PLM 编码器用于密集检索。

### 段落 132 · Page 17

**EN**

We employ the trained models from the Cocktail benchmark (Dai et al., 2024a). The models are available at https://huggingface.co/IR-Cocktail/ bert-base-uncased-mean-v3-msmarco and https://huggingface.co/ IR-Cocktail/roberta-base-mean-v3-msmarco , respectively. ANCE (Xiong et al., 2020) improves dense retrieval by sampling hard negatives via the Approximate Nearest Neighbor (ANN) index. The model is available at https://huggingface.co/ sentence-transformers/msmarco-roberta-base-ance-firstp . TAS-B (Hofstätter et al., 2021), leverages balanced margin sampling for efficient query selection.

**中文**

我们采用 Cocktail 基准中经过训练的模型（Dai 等人，2024a）。这些模型分别可在 https://huggingface.co/IR-Cocktail/bert-base-uncased-mean-v3-msmarco 和 https://huggingface.co/IR-Cocktail/roberta-base-mean-v3-msmarco 上获取。 ANCE（Xiong 等人，2020）通过近似最近邻 (ANN) 索引对硬负例进行采样，改进了密集检索。该模型可在 https://huggingface.co/sentence-transformers/msmarco-roberta-base-ance-firstp 上获取。 TAS-B（Hofstätter et al., 2021）利用平衡边际采样来实现高效的查询选择。

### 段落 133 · Page 17

**EN**

The model is available at https://huggingface.co/sentence-transformers/ msmarco-distilbert-base-tas-b . 17

**中文**

该模型可在 https://huggingface.co/sentence-transformers/msmarco-distilbert-base-tas-b 上获取。 17 号

### Page 18

### 段落 134 · Page 18

**EN**

Published as a conference paper at ICLR 2025 Table 4: Human evaluation on which document is more relevant to the given query semantically? The numbers in parentheses are the proportion agreed upon by all three human annotators.

**中文**

作为 ICLR 2025 会议论文发表 表 4：对哪个文档在语义上与给定查询更相关的人工评估？括号中的数字是所有三位人类注释者都同意的比例。

### 段落 135 · Page 18

**EN**

Temperature DL19 Human LLM Equal 0.00 0.0% (0.0%) 5% (0.0%) 95% (83.8%) 0.20 0.0%(0.0%) 5% (0.0%) 95% (94.2%) 0.40 0.0% (0.0%) 0.0% (0.0%) 100% (79.6%) 0.60 0.0% (0.0%) 0.0% (0.0%) 100% (84.6%) 0.80 0.0% (0.0%) 0.0% (0.0%) 100% (94.5%) 1.00 0.0%(0.0%) 0.0% (0.0%) 100% (94.5%) Temperature TREC-COVID Human LLM Equal 0.00 0.0% (0.0%) 0.0% (0.0%) 100% (84.6%) 0.20 0.0% (0.0%) 0.0% (0.0%) 100% (94.5%) 0.40 0.0% (0.0%) 0.0% (0.0%) 100% (74.6%) 0.60 0.0% (0.0%) 0.0% (0.0%) 100% (94.5%) 0.80 0.0% (0.0%) 0.0% (0.0%) 100% (79.6%) 1.00 0.0% (0.0%) 0.0% (0.0%) 100% (84.6%) Temperature SCIDOCS Human LLM Equal 0.00 0.0% (0.0%) 0.0% (0.0%) 100% (84.6%) 0.20

**中文**

温度 DL19 人类 LLM 等于 0.00 0.0% (0.0%) 5% (0.0%) 95% (83.8%) 0.20 0.0%(0.0%) 5% (0.0%) 95% (94.2%) 0.40 0.0% (0.0%) 0.0% (0.0%) 100% (79.6%) 0.60 0.0% (0.0%) 0.0% (0.0%) 100% (84.6%) 0.80 0.0% (0.0%) 0.0% (0.0%) 100% (94.5%) 1.00 0.0%(0.0%) 0.0% (0.0%) 100% (94.5%) 温度 TREC-COVID 人类 LLM 等于 0.00 0.0% (0.0%) 0.0% (0.0%) 100% (84.6%) 0.20 0.0% (0.0%) 0.0% (0.0%) 100% (94.5%) 0.40 0.0% (0.0%) 0.0% (0.0%) 100% (74.6%) 0.60 0.0% (0.0%) 0.0% (0.0%) 100% (94.5%) 0.80 0.0% (0.0%) 0.0% (0.0%) 100% (79.6%) 1.00 0.0% (0.0%) 0.0% (0.0%) 100% (84.6%) 温度 SCIDOCS 人类 LLM 等于 0.00 0.0% (0.0%) 0.0% (0.0%) 100% (84.6%) 0.20

### 段落 136 · Page 18

**EN**

0.0% (0.0%) 0.0% (0.0%) 100% (84.6%) 0.40 0.0% (0.0%) 0.0% (0.0%) 100% (79.6%) 0.60 0.0% (0.0%) 5.0% (0.0%) 95% (83.8%) 0.80 0.0% (0.0%) 0.0% (0.0%) 100% (79.6%) 1.00 0.0% (0.0%) 5% (0.0%) 95% (89.0%) Contriever (Izacard et al., 2022) employs contrastive learning with positive samples generated through cropping and token sampling.

**中文**

0.0% (0.0%) 0.0% (0.0%) 100% (84.6%) 0.40 0.0% (0.0%) 0.0% (0.0%) 100% (79.6%) 0.60 0.0% (0.0%) 5.0% (0.0%) 95% (83.8%) 0.80 0.0% (0.0%) 0.0% (0.0%) 100% (79.6%) 1.00 0.0% (0.0%) 5% (0.0%) 95% (89.0%) Contriever (Izacard et al., 2022) 采用对比学习，通过裁剪和令牌采样生成正样本。

### 段落 137 · Page 18

**EN**

The model is available at https://huggingface.co/ facebook/contriever-msmarco. coCondenser (Gao and Callan, 2022) is a retriever that conducts both pre-training and supervised fine-tuning. The model is available at https://huggingface.co/ sentence-transformers/msmarco-bert-co-condensor . We follow the metrics proposed by previous work when measuring ranking performance and source bias. For ranking performance, we use NDCG@k (Järvelin and Kekäläinen, 2002).

**中文**

该模型可在 https://huggingface.co/facebook/contriever-msmarco 上获取。 coCondenser（Gao 和 Callan，2022）是一种进行预训练和监督微调的检索器。该模型可在 https://huggingface.co/sentence-transformers/msmarco-bert-co-condensor 上获取。在衡量排名表现和来源偏差时，我们遵循以前的工作提出的指标。对于排名性能，我们使用 NDCG@k（Järvelin 和 Kekäläinen，2002）。

### 段落 138 · Page 18

**EN**

For source bias, we use Relative ∆ NDCG@k (Dai et al., 2024a;c; Xu et al., 2024; Zhou et al., 2024), which is formulated as Relative∆ = M etricHuman − M etricLLM 1 2(M etricHuman + M etricLLM) × 100%. In CDC debiasing, considering the sample size we conduct bias correction for the top 10 candidates in retrival. Rising up the candidates number leads to less preference for LLM-generated documents while ranking performance may drop a little.

**中文**

对于源偏差，我们使用相对ΔNDCG@k（Dai et al., 2024a;c; Xu et al., 2024; Zhou et al., 2024），其公式为RelativeΔ = M etricHuman − M etricLLM 1 2(M etricHuman + M etricLLM) × 100%。在CDC去偏中，考虑到样本量，我们对检索中前10名候选者进行偏差校正。候选人数量的增加会导致对 LLM 生成的文档的偏好降低，而排名表现可能会略有下降。

### 段落 139 · Page 18

**EN**

E.2 M ORE RESULTS OF GENERATED CORPUS WITH VARYING SAMPLING TEMPERATURE E.2.1 H UMAN EVALUATION Although LLM-generated documents are solely based on their corresponding human documents, it is still necessary to verify that the generated document has the same relevance scores with given query as the original documents. To provide empirical support on the fact that LLM-generated documents are not injected with extraneous information about queries, we conduct a human evaluation. We randomly select 20 (query, human-written document, LLM-generated document) triples for each dataset and each sampling temperature.

**中文**

E.2 不同采样温度下生成的语料库的更多结果 E.2.1 人类评估 尽管 LLM 生成的文档完全基于其相应的人类文档，但仍然有必要验证生成的文档与给定查询具有与原始文档相同的相关性分数。为了为 LLM 生成的文档未注入有关查询的无关信息这一事实提供实证支持，我们进行了人工评估。我们为每个数据集和每个采样温度随机选择 20 个（查询、人工编写的文档、LLM 生成的文档）三元组。

### 段落 140 · Page 18

**EN**

The human annotators who have at least Bachelor’s degrees are asked to evaluate which document is more relevant without knowing document sources. Their results are transferred into the “Human”, “LLM”, or “Equal” options later. The final labels of each 18

**中文**

至少拥有学士学位的人工注释者被要求在不知道文档来源的情况下评估哪个文档更相关。他们的结果稍后会转移到“人类”、“法学硕士”或“平等”选项中。每18个的最终标签

### Page 19

### 段落 141 · Page 19

**EN**

Published as a conference paper at ICLR 2025 /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017/uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001a/uni00000016/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000017/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000018/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000019/uni00000013 /uni0000001

**中文**

作为会议论文发表在 ICLR 2025 /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017 /uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001a/uni00000016/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000017/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000018/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000019/uni00000013 /uni0000001

### 段落 142 · Page 19

**EN**

4/uni00000011/uni0000001a/uni0000001a/uni00000013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000017/uni00000013/uni00000015 /uni00000013/uni00000011/uni00000017/uni00000013/uni00000016 /uni00000013/uni00000011/uni00000017/uni00000013/uni00000017 /uni00000013/uni00000011/uni00000017/uni00000013/uni00000018 /uni00000013/uni00000011/uni00000017/uni00000013/uni00000019 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00

**中文**

4/uni00000011/uni0000001a/uni0000001a/uni00000013/uni00000033/uni00000048/uni0000005 5/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000017/uni00000013/uni00000015 /uni00000013/uni00000011/uni00000017/uni00000013/uni00000016 /uni00000013/uni00000011/uni00000017/uni00000013/uni00000017 /uni00000013/uni00000011/uni00000017/uni00000013/uni00000018 /uni00000013/uni00000011/uni00000017/uni00000013/uni00000019 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00

### 段落 143 · Page 19

**EN**

000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni00000011/uni0000001c/uni00000019 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (a) DL19 /uni00000013/uni0000

**中文**

000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00 000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049 /uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni00 00001d/uni00000003/uni00000010/uni00000013/uni00000011/uni0000001c/uni00000019 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (a)DL19/uni00000013/uni0000

### 段落 144 · Page 19

**EN**

0011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017/uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni00000019/uni00000013/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000015/uni00000013 /uni00000014/uni00000011/uni00000019/uni00000016/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000018/uni00000013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0

**中文**

0011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017/uni000000 13/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni00000019/uni00000013/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000015/uni00000013 /uni00000014/uni00000011/uni00000019/uni00000016/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000018/uni00000013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0

### 段落 145 · Page 19

**EN**

000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000017/uni00000017/uni00000018 /uni00000013/uni00000011/uni00000017/uni00000018/uni00000013 /uni00000013/uni00000011/uni00000017/uni00000018/uni00000018 /uni00000013/uni00000011/uni00000017/uni00000019/uni00000013 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056

**中文**

000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000017/uni00000017/uni00000018 /uni00000013/uni00000011/uni00000017/uni00000018/uni00000013 /uni00000013/uni00000011/uni00000017/uni00000018/uni00000018 /uni00000013/uni00000011/uni00000017/uni00000019/uni00000013 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056

### 段落 146 · Page 19

**EN**

/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni00000011/uni00000019/uni0000001c /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (b) TREC-COVID /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017/uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000

**中文**

/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046/uni00 00004c/uni00000048/uni00000051/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni00000011/uni00000019/uni0000001c /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (b) TREC-新冠肺炎/uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni 00000017/uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000

### 段落 147 · Page 19

**EN**

011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001c/uni00000019/uni00000013 /uni00000014/uni00000011/uni0000001c/uni0000001b/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000013/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000015/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000017/uni00000013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni

**中文**

011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001c/uni00000019/uni00000013 /uni00000014/uni00000011/uni0000001c/uni0000001b/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000013/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000015/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000017/uni00000013/uni00000033/uni00000048/uni00 000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni

### 段落 148 · Page 19

**EN**

0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000015/uni00000015/uni00000014 /uni00000013/uni00000011/uni00000015/uni00000015/uni00000015 /uni00000013/uni00000011/uni00000015/uni00000015/uni00000016 /uni00000013/uni00000011/uni00000015/uni00000015/uni00000016 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046

**中文**

0000005b/uni0000004c/uni00000057/uni0000005c/uni00000013/uni00000011/uni00000015/uni00000015/uni00000014 /uni00000013/uni00000011/uni00000015/uni00000015/uni00000015 /uni00000013/uni00000011/uni00000015/uni00000015/uni00000016 /uni00000013/uni00000011/uni00000015/uni00000015/uni00000016 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00 000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046

### 段落 149 · Page 19

**EN**

/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni00000011/uni0000001c/uni0000001a /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (c) SCIDOCS Figure 5: Perplexity and estimated relevance scores of Contriever on positive query-document pairs in three datasets, where documents are generated by LLM with different sampling temperatures.

**中文**

/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni00000011/uni0000001c/uni0000001a /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (c) SCIDOCS 图 5：Contriever 对三个数据集中的正查询文档对的困惑度和估计相关性得分，其中文档是由 LLM 在不同采样温度下生成的。

### 段落 150 · Page 19

**EN**

/uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017/uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001a/uni00000016/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000017/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000018/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000019/uni00000013 /uni00000014/uni00000011/uni0000001a/uni0000001a/uni0000

**中文**

/uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017 /uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001a/uni00000016/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000017/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000018/uni00000013 /uni00000014/uni00000011/uni0000001a/uni00000019/uni00000013 /uni00000014/uni00000011/uni0000001a/uni0000001a/uni0000

### 段落 151 · Page 19

**EN**

0013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni0000001a/uni00000014/uni00000015 /uni00000013/uni00000011/uni0000001a/uni00000015/uni00000013 /uni00000013/uni00000011/uni0000001a/uni00000015/uni0000001b /uni00000013/uni00000011/uni0000001a/uni00000016/uni00000019 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni

**中文**

0013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni0000001a/uni00000014/uni00000015 /uni00000013/uni00000011/uni0000001a/uni00000015/uni00000013 /uni00000013/uni00000011/uni0000001a/uni00000015/uni0000001b /uni00000013/uni00000011/uni0000001a/uni00000016/uni00000019 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni0000 0051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni

### 段落 152 · Page 19

**EN**

00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni00000011/uni0000001a/uni00000018 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (a) DL19 /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017/uni00000013/uni00

**中文**

00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00 000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049 /uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni00 00001d/uni00000003/uni00000010/uni00000013/uni00000011/uni0000001a/uni00000018 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (a) DL19 /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017/uni00000013/uni00

### 段落 153 · Page 19

**EN**

000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni00000019/uni00000013/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000015/uni00000013 /uni00000014/uni00000011/uni00000019/uni00000016/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000018/uni00000013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/u

**中文**

000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni00000019/uni00000013/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000015/uni00000013 /uni00000014/uni00000011/uni00000019/uni00000016/uni00000018 /uni00000014/uni00000011/uni00000019/uni00000018/uni00000013/uni00000033/uni00000048/uni00 000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/u

### 段落 154 · Page 19

**EN**

ni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000014/uni00000015/uni00000013 /uni00000013/uni00000011/uni00000014/uni00000015/uni0000001b /uni00000013/uni00000011/uni00000014/uni00000016/uni00000019 /uni00000013/uni00000011/uni00000014/uni00000017/uni00000017 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni000000

**中文**

ni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000014/uni00000015/uni00000013 /uni00000013/uni00000011/uni00000014/uni00000015/uni0000001b /uni00000013/uni00000011/uni00000014/uni00000016/uni00000019 /uni00000013/uni00000011/uni00000014/uni00000017/uni00000017 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni0000005 1/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni000000

### 段落 155 · Page 19

**EN**

4c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni00000011/uni00000019/uni0000001c /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (b) TREC-COVID /uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017/uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00

**中文**

4c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001 d/uni00000003/uni00000010/uni00000013/uni00000011/uni00000019/uni0000001c /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (b) TREC-新冠肺炎/uni00000013/uni00000011/uni00000013/uni00000013/uni00000011/uni00000015/uni00000013/uni00000011/uni00000017 /uni00000013/uni00000011/uni00000019/uni00000013/uni00000011/uni0000001b/uni00000014/uni00000011/uni00000013 /uni00000037/uni00000048/uni00000050/uni00000053/uni00000048/uni00000055/uni00000044/uni00

### 段落 156 · Page 19

**EN**

000057/uni00000058/uni00000055/uni00000048 /uni00000014/uni00000011/uni0000001c/uni00000019/uni00000013 /uni00000014/uni00000011/uni0000001c/uni0000001b/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000013/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000015/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000017/uni00000013/uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000016/uni00000016/uni00000013

**中文**

000057/uni00000058/uni00000055/uni00000048/uni00000014/uni00000011/uni0000001c/uni00000019/uni00000013 /uni00000014/uni00000011/uni0000001c/uni0000001b/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000013/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000015/uni00000013 /uni00000015/uni00000011/uni00000013/uni00000017/uni00000013/uni00000033/uni00000048/uni00 000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000033/uni00000048/uni00000055/uni00000053/uni0000004f/uni00000048/uni0000005b/uni0000004c/uni00000057/uni0000005c /uni00000013/uni00000011/uni00000016/uni00000016/uni00000013

### 段落 157 · Page 19

**EN**

/uni00000013/uni00000011/uni00000016/uni00000017/uni00000013 /uni00000013/uni00000011/uni00000016/uni00000018/uni00000013 /uni00000013/uni00000011/uni00000016/uni00000019/uni00000013 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni00000052/uni00000051/uni00000003/uni00000026/uni00000052/uni00000048/uni00000049/uni00000049/uni0000004c/uni00000046/uni0000004c/uni00000048/uni00000051/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni000000

**中文**

/uni00000013/uni00000011/uni00000016/uni00000017/uni00000013 /uni00000013/uni00000011/uni00000016/uni00000018/uni00000013 /uni00000013/uni00000011/uni00000016/uni00000019/uni00000013 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 /uni00000033/uni00000048/uni00000044/uni00000055/uni00000056/uni0000005 2/uni00000051/uni00000003/uni00000026/uni00000052/uni00000048/uni0000004 9/uni00000049/uni0000004c/uni00000046/uni0000004c/uni00000048/uni000000 51/uni00000057/uni0000001d/uni00000003/uni00000010/uni00000013/uni000000

### 段落 158 · Page 19

**EN**

11/uni0000001a/uni00000015 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (c) SCIDOCS Figure 6: Perplexity and estimated relevance scores of TAS-B on positive query-document pairs in three datasets, where documents are generated by LLM with different sampling temperatures.

**中文**

11/uni0000001a/uni00000015 /uni00000035/uni00000048/uni0000004f/uni00000048/uni00000059/uni00000044/uni00000051/uni00 000046/uni00000048/uni00000003/uni00000036/uni00000046/uni00000052/uni00000055/uni00000048 (c) SCIDOCS 图 6：TAS-B 在三个数据集中的正查询文档对上的困惑度和估计相关性得分，其中文档是由 LLM 在不同采样温度下生成的。

### 段落 159 · Page 19

**EN**

triple are determined by the votes of three different annotators. The results in Table 4 illustrate that documents from different sources possess the same relevance to the corresponding queries, which guarantees the correctness of our controlled variables experiments. E.2.2 R ESULTS WITH MORE PLM- BASED RETRIEVERS In Section 3.1 we discover the negative correlation between document perplexity and estimated relevance scores by Contriever. In this section, we demonstrate the replicability of the discovery by providing similar results on TAS-B and Contriever.

**中文**

三元组由三个不同注释者的投票决定。表4的结果表明，不同来源的文档与相应的查询具有相同的相关性，这保证了我们控制变量实验的正确性。 E.2.2 更多基于 PLM 的检索器的结果 在第 3.1 节中，我们发现文档困惑度与 Contriever 估计的相关性分数之间存在负相关。在本节中，我们通过在 TAS-B 和 Contriever 上提供类似的结果来证明这一发现的可复制性。

### 段落 160 · Page 19

**EN**

As depicted in Figure 5 and Figure 6, there is a significant negative correlation between document perplexity and estimated relevance scores as sampling temperature changes. Documents with lower perplexity obtain prevalent higher estimated relevance scores across different PLM-based retrievers, further affirming the universality of the phenomenon. E.2.3 M ORE RESULTS OF β2 ESTIMATION In Section 4.1, we estimated the causal effect of perplexity on estimated relevance scores through 2SLS. Since the estimation needs LLM generation, it’s natural to explore the hyperparameters related to the generation.

**中文**

如图 5 和图 6 所示，随着采样温度的变化，文档困惑度和估计的相关性分数之间存在显着的负相关性。困惑度较低的文档在不同的基于 PLM 的检索器中获得普遍较高的估计相关性分数，进一步证实了该现象的普遍性。 E.2.3 β2 估计的更多结果 在第 4.1 节中，我们通过 2SLS 估计了困惑度对估计相关性得分的因果影响。由于估计需要LLM生成，因此很自然地探索与生成相关的超参数。

### 段落 161 · Page 19

**EN**

According to the causal graph we proposed, the sampling temperature does affect ˆβ1 in the first stage of the regression, but is independent with ˆβ2. We explore whether ˆβ1 changes in turn affects the value of ˆβ2 by using documents generated with different sampling temperature. The ˆβ1 and ˆβ2 obtained from our estimation on the set of rewritten texts with different sampling temperatures are shown in Table 5.

**中文**

根据我们提出的因果图，在回归的第一阶段，采样温度确实影响β1，但与β2无关。我们通过使用不同采样温度生成的文档来探讨β1的变化是否反过来影响β2的值。我们对不同采样温度的重写文本集进行估计得到的 β1 和 β2 如表 5 所示。

### 段落 162 · Page 19

**EN**

It can be found that under the maximum sampling temperature difference, the variation of ˆβ1 is within 15% and the variation of ˆβ2 is within 20%, and such variations are similar to the errors brought by random sampling, so the variation of the sampling temperature is acceptable in the CDC algorithm. 19

**中文**

可以发现，在最大采样温差下，β1的变化在15%以内，β2的变化在20%以内，这种变化与随机采样带来的误差类似，因此CDC算法中采样温度的变化是可以接受的。 19

### Page 20

### 段落 163 · Page 20

**EN**

Published as a conference paper at ICLR 2025 Table 5: The influence of generation temperatures on the magnitude of the causal coefficients β1, β2. The coefficients are estimated from all positive query-document pairs.

**中文**

作为 ICLR 2025 会议论文发表 表 5：发电温度对因果系数 β1、β2 大小的影响。系数是根据所有正查询文档对估计的。

### 段落 164 · Page 20

**EN**

DL19 TREC-COVID SCIDOCS Temperature 0.0 0.2 0.4 0.6 0.0 0.2 0.4 0.6 0.0 0.2 0.4 0.6 ˆβ2(BERT) -7.80 -7.78 -7.77 -7.94 -1.21 -1.20 -1.24 -1.26 -2.29 -2.29 -2.33 -2.46 ˆβ2(RoBERTa) -23.57 -23.50 -23.45 -23.97 1.73 1.73 1.77 1.80 -6.02 -6.04 -6.13 -6.47 ˆβ2(ANCE) -0.44 -0.44 -0.44 -0.45 0.07 0.07 0.07 0.07 -0.22 -0.22 -0.22 -0.23 ˆβ2(TAS-B) -0.81 -0.80 -0.80 -0.82 -0.34 -0.34 -0.35 -0.35 -0.37 -0.37 -0.37 -0.39 ˆβ2(Contriever) -0.01 -0.01 -0.01 -0.01 -0.03 -0.03 -0.04 -0.04 -0.02 -0.02 -0.02 -0.02 ˆβ2(coCondenser) -0.58 -0.58 -0.58 -0.59 -0.23 -0.23 -0.24 -0.24 -0.25 -0.25 -0.25 -0.26 ˆβ1 -0.44 -0.44 -0.44 -0.43 -0.41 -0.41 -0.40 -0.39 -0.41 -0.

**中文**

DL19 TREC-COVID SCIDOCS 温度 0.0 0.2 0.4 0.6 0.0 0.2 0.4 0.6 0.0 0.2 0.4 0.6 β2(BERT) -7.80 -7.78 -7.77 -7.94 -1.21 -1.20 -1.24 -1.26 -2.29 -2.29 -2.33 -2.46 β2(罗贝尔塔) -23.57 -23.50 -23.45 -23.97 1.73 1.73 1.77 1.80 -6.02 -6.04 -6.13 -6.47 β2(ANCE) -0.44 -0.44 -0.44 -0.45 0.07 0.07 0.07 0.07 -0.22 -0.22 -0.22 -0.23 β2(TAS-B) -0.81 -0.80 -0.80 -0.82 -0.34 -0.34 -0.35 -0.35 -0.37 -0.37 -0.37 -0.39 β2(Contriever) -0.01 -0.01 -0.01 -0.01 -0.03 -0.03 -0.04 -0.04 -0.02 -0.02 -0.02 -0.02 β2(coCondenser) -0.58 -0.58 -0.58 -0.59 -0.23 -0.23 -0.24 -0.24 -0.25 -0.25 -0.25 -0.26 β1 -0.44 -0.44 -0.44 -0.43 -0.41 -0.41 -0.40 -0.39 -0.41 -0。

### 段落 165 · Page 20

**EN**

40 -0.40 -0.38 E.3 M ORE RESULTS OF CDC D EBIASING In this section, we report more experimental results to provide a more comprehensive analysis of CDC, including robustness analysis with error bar (Table 6) and significance test (Tabel 7).

**中文**

40 -0.40 -0.38 E.3 CDC D EBIASING 的更多结果 在本节中，我们报告了更多实验结果，以提供对 CDC 的更全面的分析，包括误差条的稳健性分析（表 6）和显着性检验（表 7）。

### 段落 166 · Page 20

**EN**

Table 6: Mean and standard deviation of Performance (NDCG@3) and bias (Relative ∆ (Dai et al., 2024c) on NDCG@3) of different PLM-based retrievers with our proposed CDC debiased method on three datasets in five repetitions.

**中文**

表 6：不同基于 PLM 的检索器的性能 (NDCG@3) 和偏差（NDCG@3 上的相对 Δ（Dai 等人，2024c））的平均值和标准差，采用我们提出的 CDC 去偏差方法对三个数据集进行五次重复。

### 段落 167 · Page 20

**EN**

Model DL19 (In-Domain) TREC-COVID (Out-of-Domain) SCIDOCS (Out-of-Domain) Performance Bias Performance Bias Performance Bias Mean Std Mean Std Mean Std Mean Std Mean Std Mean Std BERT 77.65 0.89 5.90 4.40 45.88 1.14 -18.40 6.72 10.44 0.19 29.19 9.35 RoBERTa 71.33 0.48 4.45 0.80 45.86 0.78 -10.51 3.58 8.24 0.18 32.13 7.28 ANCE 67.73 0.15 34.95 11.51 69.94 0.77 -1.94 4.63 12.31 0.33 26.26 10.61 TAS-B 75.63 0.24 -9.97 5.25 62.84 0.48 -37.42 3.99 14.15 0.16 23.48 5.84 Contriever 73.83 0.27 -5.33 1.93 61.35 0.73 -31.33 3.22 15.09 0.10 1.63 1.89 coCondenser 75.36 0.47 9.60 8.49 71.07 0.45 -45.39 8.55 13.79 0.21 1.06 2.79 Table 7: The p-value of sig

**中文**

模型 DL19（域内） TREC-COVID（域外） SCIDOCS（域外） 性能偏差 性能偏差 性能偏差 Mean Std Mean Std Mean Std Mean Std Mean Std Mean Std BERT 77.65 0.89 5.90 4.40 45.88 1.14 -18.40 6.72 10.44 0.19 29.19 9.35 罗伯塔 71.33 0.48 4.45 0.80 45.86 0.78 -10.51 3.58 8.24 0.18 32.13 7.28 安斯 67.73 0.15 34.95 11.51 69.94 0.77 -1.94 4.63 12.31 0.33 26.26 10.61 TAS-B 75.63 0.24 -9.97 5.25 62.84 0.48 -37.42 3.99 14.15 0.16 23.48 5.84 探索者 73.83 0.27 -5.33 1.93 61.35 0.73 -31.33 3.22 15.09 0.10 1.63 1.89 共冷凝器 75.36 0.47 9.60 8.49 71.07 0.45 -45.39 8.55 13.79 0.21 1.06 2.79 表 7：sig 的 p 值

### 段落 168 · Page 20

**EN**

nificance test conducted on the NDCG@3 and Relative∆ (Dai et al., 2024c) on NDCG@3 with and without CDC debias method, with bold fonts indicating the Performance or Bias can pass a significance test with p-value< 0.05.

**中文**

使用和不使用 CDC debias 方法对 NDCG@3 和相对Δ (Dai et al., 2024c) 对 NDCG@3 进行显着性检验，粗体字体表示性能或偏差可以通过 p 值 < 0.05 的显着性检验。

### 段落 169 · Page 20

**EN**

As expected, most Performance DOES NOT pass the significance test while all the Bias DOES pass the significance test. Model DL19 TREC-COVID SCIDOCS Performance Bias Performance Bias Performance Bias BERT 4.56e-03 5.33e-04 1.87e-03 3.97e-05 1.37e-01 1.47e-03 RoBERTa 7.26e-02 2.33e-04 1.22e-01 5.46e-05 8.48e-01 9.45e-07 ANCE 1.74e-01 4.48e-03 4.61e-01 3.09e-04 1.62e-01 2.25e-05 TAS-B 6.16e-01 3.19e-04 8.58e-01 1.27e-03 6.67e-04 2.16e-04 Contriever 2.77e-01 3.94e-02 2.98e-01 5.03e-04 4.44e-02 7.65e-03 coCondenser 8.82e-01 1.16e-02 5.95e-01 3.81e-04 2.71e-01 1.58e-03 20

**中文**

正如预期的那样，大多数绩效未通过显着性测试，而所有偏差均通过显着性测试。型号 DL19 TREC-COVID SCIDOCS 性能偏差 性能偏差 性能偏差 BERT 4.56e-03 5.33e-04 1.87e-03 3.97e-05 1.37e-01 1.47e-03 RoBERTa 7.26e-02 2.33e-04 1.22e-01 5.46e-05 8.48e-01 9.45e-07 安斯 1.74e-01 4.48e-03 4.61e-01 3.09e-04 1.62e-01 2.25e-05 塔斯-B 6.16e-01 3.19e-04 8.58e-01 1.27e-03 6.67e-04 2.16e-04 冷凝器 2.77e-01 3.94e-02 2.98e-01 5.03e-04 4.44e-02 7.65e-03 共冷凝器 8.82e-01 1.16e-02 5.95e-01 3.81e-04 2.71e-01 1.58e-03 20
