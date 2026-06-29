# Dense Passage Retrieval for Open-Domain Question Answering

- ID: 76
- 类型: pdf
- 分类: 04_academic_papers
- 主题: dense retrieval for open-domain QA
- 原文链接: https://arxiv.org/pdf/2004.04906
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

Dense Passage Retrieval for Open-Domain Question Answering Vladimir Karpukhin∗, Barlas O˘guz∗, Sewon Min†, Patrick Lewis, Ledell Wu, Sergey Edunov, Danqi Chen‡, Wen-tau Yih Facebook AI †University of Washington ‡Princeton University {vladk, barlaso, plewis, ledell, edunov, scottyih }@fb.com sewon@cs.washington.edu danqic@cs.princeton.edu Abstract Open-domain question answering relies on ef- ﬁcient passage retrieval to select candidate contexts, where traditional sparse vector space models, such as TF-IDF or BM25, are the de facto method.

**中文**

开放域问答的密集段落检索 Vladimir Karpukhin*, Barlas O˘guz*, Sewon Min†, Patrick Lewis, Ledell Wu, Sergey Edunov, Danqi Chen‡, Wen-tau Yih Facebook AI †华盛顿大学 ‡普林斯顿大学 {vladk, barlaso, plewis, ledell, edunov, scottyih }@fb.com sewon@cs.washington.edu danqic@cs.princeton.edu 摘要 开放域问答依赖于有效的段落检索来选择候选上下文，其中传统的稀疏向量空间模型（例如 TF-IDF 或 BM25）是事实上的方法。

### 段落 2 · Page 1

**EN**

In this work, we show that retrieval can be practically implemented using dense representations alone, where embeddings are learned from a small number of questions and passages by a simple dualencoder framework.

**中文**

在这项工作中，我们证明检索实际上可以仅使用密集表示来实现，其中嵌入是通过简单的双编码器框架从少量问题和段落中学习的。

### 段落 3 · Page 1

**EN**

When evaluated on a wide range of open-domain QA datasets, our dense retriever outperforms a strong Lucene- BM25 system greatly by 9%-19% absolute in terms of top-20 passage retrieval accuracy, and helps our end-to-end QA system establish new state-of-the-art on multiple open-domain QA benchmarks.1 1 Introduction Open-domain question answering (QA) (V oorhees, 1999) is a task that answers factoid questions using a large collection of documents. While early QA systems are often complicated and consist of multiple components (Ferrucci (2012); Moldovan et al.

**中文**

当在广泛的开放域 QA 数据集上进行评估时，我们的密集检索器在前 20 个段落检索准确率方面绝对优于强大的 Lucene-BM25 系统 9%-19%，并帮助我们的端到端 QA 系统在多个开放域 QA 基准上建立新的最先进技术。1 1 简介 开放域问答 (QA) (V oorhees, 1999) 是一项回答事实的任务使用大量文档提出问题。虽然早期的 QA 系统通常很复杂并且由多个组件组成（Ferrucci (2012)；Moldovan 等人，2012）。

### 段落 4 · Page 1

**EN**

(2003), inter alia), the advances of reading comprehension models suggest a much simpliﬁed two-stage framework: (1) a context retriever ﬁrst selects a small subset of passages where some of them contain the answer to the question, and then (2) a machine reader can thoroughly examine the retrieved contexts and identify the correct answer (Chen et al., 2017). Although reducing open-domain QA to machine reading is a very reasonable strategy, a huge performance degradation is often observed in practice2, indicating the needs of improving retrieval.

**中文**

（2003）等），阅读理解模型的进步提出了一个更加简化的两阶段框架：（1）上下文检索器首先选择一小部分段落，其中一些包含问题的答案，然后（2）机器阅读器可以彻底检查检索到的上下文并识别正确的答案（Chen 等人，2017）。尽管将开放域 QA 减少为机器阅读是一个非常合理的策略，但在实践中经常观察到巨大的性能下降，这表明需要改进检索。

### 段落 5 · Page 1

**EN**

∗Equal contribution 1The code and trained models have been released at https://github.com/facebookresearch/DPR. 2For instance, the exact match score on SQuAD v1.1 drops from above 80% to less than 40% (Yang et al., 2019a). Retrieval in open-domain QA is usually implemented using TF-IDF or BM25 (Robertson and Zaragoza, 2009), which matches keywords efﬁciently with an inverted index and can be seen as representing the question and context in highdimensional, sparse vectors (with weighting). Conversely, the dense, latent semantic encoding is complementary to sparse representations by design.

**中文**

＊平等贡献1代码和训练模型已发布于https://github.com/facebookresearch/DPR。 2例如，SQuAD v1.1 的精确匹配分数从 80% 以上下降到 40% 以下（Yang 等人，2019a）。开放域 QA 中的检索通常使用 TF-IDF 或 BM25 来实现（Robertson 和 Zaragoza，2009），它通过倒排索引有效地匹配关键字，并且可以被视为以高维、稀疏向量（带权重）表示问题和上下文。相反，密集的潜在语义编码在设计上与稀疏表示是互补的。

### 段落 6 · Page 1

**EN**

For example, synonyms or paraphrases that consist of completely different tokens may still be mapped to vectors close to each other. Consider the question “Who is the bad guy in lord of the rings?”, which can be answered from the context “Sala Baker is best known for portraying the villain Sauron in the Lord of the Rings trilogy. ”A term-based system would have difﬁculty retrieving such a context, while a dense retrieval system would be able to better match “bad guy” with “villain” and fetch the correct context.

**中文**

例如，由完全不同的标记组成的同义词或释义仍然可以映射到彼此接近的向量。考虑一下“谁是《指环王》中的坏人？”这个问题，可以从上下文中回答“萨拉·贝克因在《指环王》三部曲中扮演反派索伦而闻名。”基于术语的系统将很难检索这样的上下文，而密集的检索系统将能够更好地将“坏人”与“反派”匹配并获取正确的上下文。

### 段落 7 · Page 1

**EN**

Dense encodings are also learnable by adjusting the embedding functions, which provides additional ﬂexibility to have a task-speciﬁc representation. With special in-memory data structures and indexing schemes, retrieval can be done efﬁciently using maximum inner product search (MIPS) algorithms (e.g., Shrivastava and Li (2014); Guo et al. (2016)). However, it is generally believed that learning a good dense vector representation needs a large number of labeled pairs of question and contexts.

**中文**

密集编码也可以通过调整嵌入函数来学习，这为特定于任务的表示提供了额外的灵活性。借助特殊的内存数据结构和索引方案，可以使用最大内积搜索 (MIPS) 算法有效地完成检索（例如，Shrivastava 和 Li (2014)；Guo 等人 (2016)）。然而，人们普遍认为学习良好的密集向量表示需要大量带标签的问题和上下文对。

### 段落 8 · Page 1

**EN**

Dense retrieval methods have thus never be shown to outperform TF-IDF/BM25 for opendomain QA before ORQA (Lee et al., 2019), which proposes a sophisticated inverse cloze task (ICT) objective, predicting the blocks that contain the masked sentence, for additional pretraining. The question encoder and the reader model are then ﬁnetuned using pairs of questions and answers jointly. Although ORQA successfully demonstrates that dense retrieval can outperform BM25, setting new state-of-the-art results on multiple open-domain arXiv:2004.04906v3 [cs.CL] 30 Sep 2020

**中文**

因此，在 ORQA 之前，密集检索方法从未被证明能够优于 TF-IDF/BM25 的开放域 QA（Lee 等人，2019），ORQA 提出了一个复杂的逆完形填空任务 (ICT) 目标，预测包含屏蔽句子的块，以进行额外的预训练。然后，联合使用问题和答案对对问题编码器和阅读器模型进行微调。尽管 ORQA 成功证明密集检索可以优于 BM25，但在多个开放域 arXiv 上设置了新的最先进结果：2004.04906v3 [cs.CL] 2020 年 9 月 30 日

### Page 2

### 段落 9 · Page 2

**EN**

QA datasets, it also suffers from two weaknesses. First, ICT pretraining is computationally intensive and it is not completely clear that regular sentences are good surrogates of questions in the objective function. Second, because the context encoder is not ﬁne-tuned using pairs of questions and answers, the corresponding representations could be suboptimal. In this paper, we address the question: can we train a better dense embedding model using only pairs of questions and passages (or answers), without additional pretraining?

**中文**

QA 数据集，它也有两个弱点。首先，ICT 预训练是计算密集型的，并且尚不完全清楚常规句子是否能很好地替代目标函数中的问题。其次，由于上下文编码器没有使用问题和答案对进行微调，因此相应的表示可能不是最佳的。在本文中，我们解决了这个问题：我们是否可以仅使用问题和段落（或答案）对来训练更好的密集嵌入模型，而不需要额外的预训练？

### 段落 10 · Page 2

**EN**

By leveraging the now standard BERT pretrained model (Devlin et al., 2019) and a dual-encoder architecture (Bromley et al., 1994), we focus on developing the right training scheme using a relatively small number of question and passage pairs. Through a series of careful ablation studies, our ﬁnal solution is surprisingly simple: the embedding is optimized for maximizing inner products of the question and relevant passage vectors, with an objective comparing all pairs of questions and passages in a batch. Our Dense Passage Retriever (DPR) is exceptionally strong. It not only outperforms BM25 by a large margin (65.2% vs.

**中文**

通过利用现在标准的 BERT 预训练模型（Devlin 等人，2019）和双编码器架构（Bromley 等人，1994），我们专注于使用相对少量的问题和段落对开发正确的训练方案。通过一系列仔细的消融研究，我们的最终解决方案出人意料地简单：嵌入被优化以最大化问题和相关段落向量的内积，目标是比较一批中的所有问题和段落对。我们的密集通道猎犬 (DPR) 非常强壮。它不仅大幅优于 BM25（65.2% vs.

### 段落 11 · Page 2

**EN**

42.9% in Top-5 accuracy), but also results in a substantial improvement on the end-to-end QA accuracy compared to ORQA (41.5% vs. 33.3%) in the open Natural Questions setting (Lee et al., 2019; Kwiatkowski et al., 2019). Our contributions are twofold. First, we demonstrate that with the proper training setup, simply ﬁne-tuning the question and passage encoders on existing question-passage pairs is sufﬁcient to greatly outperform BM25. Our empirical results also suggest that additional pretraining may not be needed.

**中文**

Top-5 准确度为 42.9%），而且与开放自然问题设置中的 ORQA（41.5% vs. 33.3%）相比，端到端 QA 准确度也得到了显着提高（Lee 等人，2019 年；Kwiatkowski 等人，2019 年）。我们的贡献是双重的。首先，我们证明，通过适当的训练设置，只需在现有问题-段落对上微调问题和段落编码器就足以大大优于 BM25。我们的实证结果还表明可能不需要额外的预训练。

### 段落 12 · Page 2

**EN**

Second, we verify that, in the context of open-domain question answering, a higher retrieval precision indeed translates to a higher end-to-end QA accuracy. By applying a modern reader model to the top retrieved passages, we achieve comparable or better results on multiple QA datasets in the open-retrieval setting, compared to several, much complicated systems. 2 Background The problem of open-domain QA studied in this paper can be described as follows. Given a factoid question, such as “ Who ﬁrst voiced Meg on Family Guy?” or “Where was the 8th Dalai Lama born?”, a system is required to answer it using a large corpus of diversiﬁed topics.

**中文**

其次，我们验证了在开放域问答的背景下，更高的检索精度确实可以转化为更高的端到端 QA 准确性。通过将现代读者模型应用于检索到的最热门段落，与几个非常复杂的系统相比，我们在开放检索设置中的多个 QA 数据集上获得了可比较或更好的结果。 2 背景 本文研究的开放域问答问题可以描述如下。给出一个事实性问题，例如“谁第一个为《恶搞之家》中的梅格配音？”或者“八世达赖喇嘛出生在哪里？”，系统需要使用大量多样化主题的语料库来回答它。

### 段落 13 · Page 2

**EN**

More speciﬁcally, we assume the extractive QA setting, in which the answer is restricted to a span appearing in one or more passages in the corpus. Assume that our collection contains D documents, d1,d 2,··· ,d D. We ﬁrst split each of the documents into text passages of equal lengths as the basic retrieval units3 and getM total passages in our corpusC ={p1,p 2,...,p M}, where each passagepi can be viewed as a sequence of tokensw(i) 1 ,w (i) 2 ,··· ,w (i) |pi|. Given a questionq, the task is to ﬁnd a spanw(i) s ,w (i) s+1,··· ,w (i) e from one of the passagespi that can answer the question.

**中文**

更具体地说，我们假设提取式问答设置，其中答案仅限于语料库中一个或多个段落中出现的范围。假设我们的集合包含 D 个文档，d1,d 2,...,d D。我们首先将每个文档分割为等长的文本段落作为基本检索单元3，并得到语料库中的 M 个段落 C ={p1,p 2,...,p M}，其中每个段落 pi 可以看作是 tokensw(i) 1 ,w (i) 2 ,... ,w (i) |pi| 的序列。给定一个问题q，任务是从一段pi 中找到一个可以回答问题的spanw(i) s ,w (i) s+1,… ,w (i) e。

### 段落 14 · Page 2

**EN**

Notice that to cover a wide variety of domains, the corpus size can easily range from millions of documents (e.g., Wikipedia) to billions (e.g., the Web). As a result, any open-domain QA system needs to include an efﬁcientretriever component that can select a small set of relevant texts, before applying the reader to extract the answer (Chen et al., 2017). 4 Formally speaking, a retriever R : (q,C)→C F is a function that takes as input a questionq and a corpusC and returns a much smaller ﬁlter set of textsCF⊂C , where|CF| =k≪|C| .

**中文**

请注意，为了覆盖广泛的领域，语料库的大小很容易从数百万个文档（例如维基百科）到数十亿个文档（例如网络）。因此，任何开放域 QA 系统都需要包含一个高效的检索器组件，该组件可以在应用阅读器提取答案之前选择一小组相关文本（Chen 等人，2017）。 4 从形式上来说，检索器 R : (q,C)→C F 是一个函数，它将问题 q 和语料库 C 作为输入，并返回一个小得多的文本过滤集 CF⊂C，其中 |CF| =k≪|C|。

### 段落 15 · Page 2

**EN**

For a ﬁxed k, a retriever can be evaluated in isolation on top-k retrieval accuracy, which is the fraction of questions for whichCF contains a span that answers the question. 3 Dense Passage Retriever (DPR) We focus our research in this work on improving the retrieval component in open-domain QA. Given a collection ofM text passages, the goal of our dense passage retriever (DPR) is to index all the passages in a low-dimensional and continuous space, such that it can retrieve efﬁciently the top k passages relevant to the input question for the reader at run-time.

**中文**

对于固定的 k，检索器可以根据 top-k 检索精度单独评估，这是 CF 包含回答问题的范围的问题的分数。 3 密集通道检索器 (DPR) 我们在这项工作中的研究重点是改进开放域 QA 中的检索组件。给定 M 个文本段落的集合，我们的密集段落检索器 (DPR) 的目标是在低维连续空间中索引所有段落，以便它可以在运行时有效地检索与读者输入问题相关的前 k 个段落。

### 段落 16 · Page 2

**EN**

Note thatM can be very large (e.g., 21 million passages in our experiments, described in Section 4.1) andk is usually small, such as 20–100. 3.1 Overview Our dense passage retriever (DPR) uses a dense encoderEP (·) which maps any text passage to addimensional real-valued vectors and builds an index for all theM passages that we will use for retrieval. 3The ideal size and boundary of a text passage are functions of both the retriever and reader. We also experimented with natural paragraphs in our preliminary trials and found that using ﬁxed-length passages performs better in both retrieval and ﬁnal QA accuracy, as observed by Wang et al.

**中文**

请注意，M 可能非常大（例如，我们的实验中有 2100 万次传代，如第 4.1 节所述），而 k 通常很小，例如 20-100。 3.1 概述 我们的密集段落检索器（DPR）使用密集编码器EP（·），它将任何文本段落映射到多维实值向量，并为我们将用于检索的所有M个段落构建索引。 3文本段落的理想大小和边界是检索器和阅读器的函数。我们还在初步试验中尝试了自然段落，发现使用固定长度的段落在检索和最终 QA 准确性方面表现更好，正如 Wang 等人所观察到的。

### 段落 17 · Page 2

**EN**

(2019). 4Exceptions include (Seo et al., 2019) and (Roberts et al., 2020), which retrieves and generates the answers, respectively.

**中文**

（2019）。 4 例外情况包括 (Seo et al., 2019) 和 (Roberts et al., 2020)，它们分别检索和生成答案。

### Page 3

### 段落 18 · Page 3

**EN**

At run-time, DPR applies a different encoderEQ(·) that maps the input question to a d-dimensional vector, and retrievesk passages of which vectors are the closest to the question vector. We deﬁne the similarity between the question and the passage using the dot product of their vectors: sim(q,p ) = EQ(q)⊺EP (p). (1) Although more expressive model forms for measuring the similarity between a question and a passage do exist, such as networks consisting of multiple layers of cross attentions, the similarity function needs to be decomposable so that the representations of the collection of passages can be precomputed.

**中文**

在运行时，DPR 应用不同的编码器EQ(·)，将输入问题映射到 d 维向量，并检索哪些向量与问题向量最接近的段落。我们使用向量的点积来定义问题和文章之间的相似度：sim(q,p) = EQ(q)⊺EP (p)。 （1）虽然确实存在用于测量问题和段落之间相似性的更具表现力的模型形式，例如由多层交叉注意力组成的网络，但相似性函数需要可分解，以便可以预先计算段落集合的表示。

### 段落 19 · Page 3

**EN**

Most decomposable similarity functions are some transformations of Euclidean distance (L2). For instance, cosine is equivalent to inner product for unit vectors and the Mahalanobis distance is equivalent to L2 distance in a transformed space. Inner product search has been widely used and studied, as well as its connection to cosine similarity and L2 distance (Mussmann and Ermon, 2016; Ram and Gray, 2012). As our ablation study ﬁnds other similarity functions perform comparably (Section 5.2; Appendix B), we thus choose the simpler inner product function and improve the dense passage retriever by learning better encoders.

**中文**

大多数可分解相似函数是欧几里得距离（L2）的一些变换。例如，余弦相当于单位向量的内积，马哈拉诺比斯距离相当于变换空间中的 L2 距离。内积搜索及其与余弦相似度和 L2 距离的联系已被广泛使用和研究（Mussmann 和 Ermon，2016；Ram 和 Gray，2012）。由于我们的消融研究发现其他相似函数的性能相当（第 5.2 节；附录 B），因此我们选择更简单的内积函数，并通过学习更好的编码器来改进密集通道检索器。

### 段落 20 · Page 3

**EN**

Encoders Although in principle the question and passage encoders can be implemented by any neural networks, in this work we use two independent BERT (Devlin et al., 2019) networks (base, uncased) and take the representation at the [CLS] token as the output, sod = 768. Inference During inference time, we apply the passage encoderEP to all the passages and index them using FAISS (Johnson et al., 2017) ofﬂine. FAISS is an extremely efﬁcient, open-source library for similarity search and clustering of dense vectors, which can easily be applied to billions of vectors.

**中文**

编码器 虽然原则上问题和段落编码器可以由任何神经网络实现，但在这项工作中，我们使用两个独立的 BERT (Devlin et al., 2019) 网络（base, uncased），并将 [CLS] 标记处的表示作为输出，sod = 768。 推理 在推理期间，我们将段落编码器 EP 应用于所有段落，并使用 FAISS 对它们进行索引（Johnson et al., 2017）离线。 FAISS 是一个极其高效的开源库，用于密集向量的相似性搜索和聚类，可以轻松应用于数十亿个向量。

### 段落 21 · Page 3

**EN**

Given a questionq at run-time, we derive its embeddingvq =EQ(q) and retrieve the topk passages with embeddings closest tovq. 3.2 Training Training the encoders so that the dot-product similarity (Eq. (1)) becomes a good ranking function for retrieval is essentially a metric learning problem (Kulis, 2013). The goal is to create a vector space such that relevant pairs of questions and passages will have smaller distance (i.e., higher similarity) than the irrelevant ones, by learning a better embedding function. LetD = {⟨qi,p + i ,p− i,1,··· ,p− i,n⟩}m i=1 be the training data that consists of m instances.

**中文**

给定运行时的问题 q，我们推导出它的嵌入 vq = EQ(q) 并检索嵌入最接近 vq 的 topk 段落。 3.2 训练训练编码器使点积相似度（方程（1））成为检索的良好排序函数本质上是一个度量学习问题（Kulis，2013）。目标是通过学习更好的嵌入函数，创建一个向量空间，使得相关的问题和段落对比​​不相关的问题和段落具有更小的距离（即更高的相似性）。设D = {⟨qi,p + i ,p− i,1,···· ,p− i,n⟩}m i=1 为由 m 个实例组成的训练数据。

### 段落 22 · Page 3

**EN**

Each instance contains one questionqi and one relevant (positive) passagep+ i , along withn irrelevant (negative) passagesp− i,j. We optimize the loss function as the negative log likelihood of the positive passage: L(qi,p + i ,p− i,1,··· ,p− i,n) (2) = − log esim(qi,p+ i ) esim(qi,p+ i ) +∑n j=1esim(qi,p− i,j ). Positive and negative passages For retrieval problems, it is often the case that positive examples are available explicitly, while negative examples need to be selected from an extremely large pool. For instance, passages relevant to a question may be given in a QA dataset, or can be found using the answer.

**中文**

每个实例包含一个问题qi 和一个相关（正）段落p+ i，以及n 个不相关（负）段落sp− i,j。我们将损失函数优化为正通道的负对数似然： L(qi,p + i ,p− i,1,··· ,p− i,n) (2) = − log esim(qi,p+ i ) esim(qi,p+ i ) +Σn j=1esim(qi,p− i,j )。正面和负面段落 对于检索问题，通常情况下，正面示例是明确可用的，而负面示例则需要从非常大的池中选择。例如，与问题相关的段落可能会在 QA 数据集中给出，或者可以使用答案找到。

### 段落 23 · Page 3

**EN**

All other passages in the collection, while not speciﬁed explicitly, can be viewed as irrelevant by default. In practice, how to select negative examples is often overlooked but could be decisive for learning a high-quality encoder. We consider three different types of negatives: (1) Random: any random passage from the corpus; (2) BM25: top passages returned by BM25 which don’t contain the answer but match most question tokens; (3) Gold: positive passages paired with other questions which appear in the training set. We will discuss the impact of different types of negative passages and training schemes in Section 5.2.

**中文**

该集合中的所有其他段落虽然没有明确指定，但默认情况下可以被视为无关紧要。在实践中，如何选择负例经常被忽视，但对于学习高质量的编码器可能是决定性的。我们考虑三种不同类型的否定：（1）随机：来自语料库的任何随机段落； (2) BM25：BM25返回的最上面的段落，不包含答案，但与大多数问题标记匹配； (3) 金级：积极的段落与训练集中出现的其他问题配对。我们将在 5.2 节中讨论不同类型的负面段落和培训计划的影响。

### 段落 24 · Page 3

**EN**

Our best model uses gold passages from the same mini-batch and one BM25 negative passage. In particular, re-using gold passages from the same batch as negatives can make the computation efﬁcient while achieving great performance. We discuss this approach below. In-batch negatives Assume that we have B questions in a mini-batch and each one is associated with a relevant passage. Let Q and P be the (B×d) matrix of question and passage embeddings in a batch of sizeB. S = QPT is a (B×B) matrix of similarity scores, where each row of which corresponds to a question, paired withB passages.

**中文**

我们最好的模型使用来自同一小批量的黄金通道和一个 BM25 负通道。特别是，重复使用同一批次的黄金通道作为底片可以提高计算效率，同时实现出色的性能。我们下面讨论这种方法。批次内否定假设我们在小批次中有 B 问题，并且每个问题都与相关段落相关联。令 Q 和 P 为一批 sizeB 中问题和段落嵌入的 (B×d) 矩阵。 S = QPT 是相似度分数的 (B×B) 矩阵，其中每一行对应一个问题，与 B 个段落配对。

### 段落 25 · Page 3

**EN**

In this way, we reuse computation and effectively train onB2 (qi,pj) question/passage pairs in each batch. Any (qi,pj) pair is a positive example when i =j, and negative otherwise. This createsB training instances in each batch, where there areB− 1

**中文**

通过这种方式，我们重用计算并有效地训练每批中的 onB2 (qi,pj) 问题/段落对。当 i =j 时，任何 (qi,pj) 对都是正例，否则为负例。这会在每个批次中创建 B 个训练实例，其中有 B− 1

### Page 4

### 段落 26 · Page 4

**EN**

negative passages for each question. The trick of in-batch negatives has been used in the full batch setting (Yih et al., 2011) and more recently for mini-batch (Henderson et al., 2017; Gillick et al., 2019). It has been shown to be an effective strategy for learning a dual-encoder model that boosts the number of training examples. 4 Experimental Setup In this section, we describe the data we used for experiments and the basic setup. 4.1 Wikipedia Data Pre-processing Following (Lee et al., 2019), we use the English Wikipedia dump from Dec. 20, 2018 as the source documents for answering questions.

**中文**

每个问题的否定段落。批量负数的技巧已用于全批量设置（Yih 等人，2011），最近又用于小批量设置（Henderson 等人，2017；Gillick 等人，2019）。它已被证明是学习双编码器模型的有效策略，可以增加训练示例的数量。 4 实验设置 在本节中，我们描述用于实验的数据和基本设置。 4.1 维基百科数据预处理（Lee et al., 2019）之后，我们使用 2018 年 12 月 20 日的英文维基百科转储作为回答问题的源文档。

### 段落 27 · Page 4

**EN**

We ﬁrst apply the pre-processing code released in DrQA (Chen et al., 2017) to extract the clean, text-portion of articles from the Wikipedia dump. This step removes semi-structured data, such as tables, infoboxes, lists, as well as the disambiguation pages. We then split each article into multiple, disjoint text blocks of 100 words as passages, serving as our basic retrieval units, following (Wang et al., 2019), which results in 21,015,324 passages in the end.5 Each passage is also prepended with the title of the Wikipedia article where the passage is from, along with an [SEP] token.

**中文**

我们首先应用 DrQA 中发布的预处理代码（Chen 等人，2017）从维基百科转储中提取文章的干净文本部分。此步骤将删除半结构化数据，例如表格、信息框、列表以及消歧页面。然后，我们将每篇文章分成多个不相交的文本块，每个文本块包含 100 个单词作为段落，作为我们的基本检索单元，如下（Wang 等人，2019），最终得到 21,015,324 个段落。5 每个段落还前面加上该段落所在维基百科文章的标题以及 [SEP] 标记。

### 段落 28 · Page 4

**EN**

4.2 Question Answering Datasets We use the same ﬁve QA datasets and training/dev/testing splitting method as in previous work (Lee et al., 2019). Below we brieﬂy describe each dataset and refer readers to their paper for the details of data preparation. Natural Questions (NQ) (Kwiatkowski et al., 2019) was designed for end-to-end question answering. The questions were mined from real Google search queries and the answers were spans in Wikipedia articles identiﬁed by annotators. TriviaQA(Joshi et al., 2017) contains a set of trivia questions with answers that were originally scraped from the Web.

**中文**

4.2 问答数据集 我们使用与之前的工作相同的五个 QA 数据集和训练/开发/测试分割方法（Lee et al., 2019）。下面我们简要描述每个数据集，并建议读者参阅他们的论文以了解数据准备的详细信息。 Natural Questions (NQ)（Kwiatkowski et al., 2019）是为端到端问答而设计的。这些问题是从真实的谷歌搜索查询中挖掘出来的，答案是由注释者识别的维基百科文章中的内容。 TriviaQA（Joshi 等人，2017）包含一组琐事问题及其最初从网络上抓取的答案。

### 段落 29 · Page 4

**EN**

WebQuestions (WQ)(Berant et al., 2013) consists of questions selected using Google Suggest API, where the answers are entities in Freebase. CuratedTREC (TREC) (Baudiˇs and ˇSediv`y, 2015) sources questions from TREC QA tracks 5However, Wang et al. (2019) also propose splitting documents into overlapping passages, which we do not ﬁnd advantageous compared to the non-overlapping version. Dataset Train Dev Test Natural Questions 79,168 58,880 8,757 3,610 TriviaQA 78,785 60,413 8,837 11,313 WebQuestions 3,417 2,474 361 2,032 CuratedTREC 1,353 1,125 133 694 SQuAD 78,713 70,096 8,886 10,570 Table 1: Number of questions in each QA dataset.

**中文**

WebQuestions (WQ)（Berant et al., 2013）由使用 Google Suggest API 选择的问题组成，其中答案是 Freebase 中的实体。 CuratedTREC (TREC)（Baudiˇs 和 ˇSediv`y，2015）从 TREC QA 轨道中获取问题5然而，Wang 等人。 （2019）还建议将文档分割成重叠的段落，与非重叠的版本相比，我们认为这没有优势。数据集训练开发测试自然问题 79,168 58,880 8,757 3,610 TriviaQA 78,785 60,413 8,837 11,313 WebQuestions 3,417 2,474 361 2,032 CuratedTREC 1,353 1,125 133 694 SQuAD 78,713 70,096 8,886 10,570 表 1：每个 QA 数据集中的问题数量。

### 段落 30 · Page 4

**EN**

The two columns of Train denote the original training examples in the dataset and the actual questions used for training DPR after ﬁltering. See text for more details. as well as various Web sources and is intended for open-domain QA from unstructured corpora. SQuAD v1.1 (Rajpurkar et al., 2016) is a popular benchmark dataset for reading comprehension. Annotators were presented with a Wikipedia paragraph, and asked to write questions that could be answered from the given text. Although SQuAD has been used previously for open-domain QA research, it is not ideal because many questions lack context in absence of the provided paragraph.

**中文**

Train的两列表示数据集中的原始训练示例和过滤后用于训练DPR的实际问题。请参阅文本了解更多详细信息。以及各种 Web 资源，旨在用于非结构化语料库的开放域 QA。 SQuAD v1.1（Rajpurkar et al., 2016）是一个流行的阅读理解基准数据集。向注释者展示了维基百科的一个段落，并要求他们写出可以从给定文本中回答的问题。尽管 SQuAD 之前已用于开放域 QA 研究，但它并不理想，因为许多问题在没有提供的段落的情况下缺乏上下文。

### 段落 31 · Page 4

**EN**

We still include it in our experiments for providing a fair comparison to previous work and we will discuss more in Section 5.1. Selection of positive passages Because only pairs of questions and answers are provided in TREC, WebQuestions and TriviaQA6, we use the highest-ranked passage from BM25 that contains the answer as the positive passage. If none of the top 100 retrieved passages has the answer, the question will be discarded.

**中文**

我们仍然将其包含在我们的实验中，以便与以前的工作进行公平的比较，我们将在第 5.1 节中讨论更多内容。正面段落的选择 由于 TREC、WebQuestions 和 TriviaQA6 中仅提供问题和答案对，因此我们使用 BM25 中包含答案的排名最高的段落作为正面段落。如果检索到的前 100 篇文章中没有一篇有答案，则该问题将被丢弃。

### 段落 32 · Page 4

**EN**

For SQuAD and Natural Questions, since the original passages have been split and processed differently than our pool of candidate passages, we match and replace each gold passage with the corresponding passage in the candidate pool.7 We discard the questions when the matching is failed due to different Wikipedia versions or pre-processing. Table 1 shows the number of questions in training/dev/test sets for all the datasets and the actual questions used for training the retriever.

**中文**

对于 SQuAD 和自然问题，由于原始段落的分割和处理方式与我们的候选段落池不同，我们将每个黄金段落与候选池中的相应段落进行匹配和替换。7 当由于不同的维基百科版本或预处理而导致匹配失败时，我们会丢弃这些问题。表 1 显示了所有数据集的训练/开发/测试集中的问题数量以及用于训练检索器的实际问题。

### 段落 33 · Page 4

**EN**

5 Experiments: Passage Retrieval In this section, we evaluate the retrieval performance of our Dense Passage Retriever (DPR), along with analysis on how its output differs from 6We use the unﬁltered TriviaQA version and discard the noisy evidence documents mined from Bing. 7The improvement of using gold contexts over passages that contain answers is small. See Section 5.2 and Appendix A.

**中文**

5 实验：段落检索 在本节中，我们评估了密集段落检索器 (DPR) 的检索性能，并分析了其输出与 6 的不同之处。我们使用未过滤的 TriviaQA 版本，并丢弃从 Bing 中挖掘的噪声证据文档。 7使用黄金上下文相对于包含答案的段落的改进很小。参见第 5.2 节和附录 A。

### Page 5

### 段落 34 · Page 5

**EN**

Training Retriever Top-20 Top-100 NQ TriviaQA WQ TREC SQuAD NQ TriviaQA WQ TREC SQuAD None BM25 59.1 66.9 55.0 70.9 68.8 73.7 76.7 71.1 84.1 80.0 Single DPR 78.4 79.4 73.2 79.8 63.2 85.4 85.0 81.4 89.1 77.2 BM25 + DPR 76.6 79.8 71.0 85.2 71.5 83.8 84.5 80.5 92.7 81.3 Multi DPR 79.4 78.8 75.0 89.1 51.6 86.0 84.7 82.9 93.9 67.6 BM25 + DPR 78.0 79.9 74.7 88.5 66.2 83.9 84.4 82.3 94.1 78.6 Table 2: Top-20 & Top-100 retrieval accuracy on test sets, measured as the percentage of top 20/100 retrieved passages that contain the answer.

**中文**

训练猎犬 Top-20 Top-100 NQ TriviaQA WQ TREC SQuAD NQ TriviaQA WQ TREC SQuAD 无 BM25 59.1 66.9 55.0 70.9 68.8 73.7 76.7 71.1 84.1 80.0 单 DPR 78.4 79.4 73.2 79.8 63.2 85.4 85.0 81.4 89.1 77.2 BM25 + DPR 76.6 79.8 71.0 85.2 71.5 83.8 84.5 80.5 92.7 81.3 多 DPR 79.4 78.8 75.0 89.1 51.6 86.0 84.7 82.9 93.9 67.6 BM25 + DPR 78.0 79.9 74.7 88.5 66.2 83.9 84.4 82.3 94.1 78.6 表 2：测试集上的 Top-20 和 Top-100 检索准确度，以检索到的前 20/100 个的百分比来衡量包含答案的段落。

### 段落 35 · Page 5

**EN**

Single and Multi denote that our Dense Passage Retriever (DPR) was trained using individial or combined training datasets (all the datasets excluding SQuAD). See text for more details. traditional retrieval methods, the effects of different training schemes and the run-time efﬁciency. The DPR model used in our main experiments is trained using the in-batch negative setting (Section 3.2) with a batch size of128 and one additional BM25 negative passage per question.

**中文**

Single 和 Multi 表示我们的密集通道检索器 (DPR) 是使用单独或组合训练数据集（除 SQuAD 之外的所有数据集）进行训练的。请参阅文本了解更多详细信息。传统的检索方法、不同训练方案的效果和运行时效率。我们主要实验中使用的 DPR 模型是使用批量大小为 128 的批内负设置（第 3.2 节）进行训练的，每个问题有一个额外的 BM25 负通道。

### 段落 36 · Page 5

**EN**

We trained the question and passage encoders for up to 40 epochs for large datasets (NQ, TriviaQA, SQuAD) and 100 epochs for small datasets (TREC, WQ), with a learning rate of 10−5 using Adam, linear scheduling with warm-up and dropout rate 0.1. While it is good to have the ﬂexibility to adapt the retriever to each dataset, it would also be desirable to obtain a single retriever that works well across the board.

**中文**

我们对大型数据集（NQ、TriviaQA、SQuAD）的问题和段落编码器进行了最多 40 个时期的训练，对小型数据集（TREC、WQ）进行了 100 个时期的训练，使用 Adam 的学习率为 10−5，线性调度的预热和退出率为 0.1。虽然让检索器能够灵活地适应每个数据集是件好事，但也希望获得一个能在所有方面都能很好地工作的检索器。

### 段落 37 · Page 5

**EN**

To this end, we train a multidataset encoder by combining training data from all datasets excluding SQuAD.8 In addition to DPR, we also present the results of BM25, the traditional retrieval method9 and BM25+DPR, using a linear combination of their scores as the new ranking function. Speciﬁcally, we obtain two initial sets of top-2000 passages based on BM25 and DPR, respectively, and rerank the union of them using BM25(q,p) +λ· sim(q,p ) as the ranking function. We usedλ = 1.1 based on the retrieval accuracy in the development set.

**中文**

为此，我们通过组合除 SQuAD 之外的所有数据集的训练数据来训练多数据集编码器。8 除了 DPR 之外，我们还提供了 BM25、传统检索方法 9 和 BM25+DPR 的结果，使用它们分数的线性组合作为新的排序函数。具体来说，我们分别基于 BM25 和 DPR 获得前 2000 个段落的两个初始集合，并使用 BM25(q,p) +λ· sim(q,p ) 作为排序函数对它们的并集进行重新排序。根据开发集中的检索精度，我们使用λ = 1.1。

### 段落 38 · Page 5

**EN**

5.1 Main Results Table 2 compares different passage retrieval systems on ﬁve QA datasets, using the top-k accuracy (k∈{ 20, 100}). With the exception of SQuAD, DPR performs consistently better than BM25 on all datasets. The gap is especially large whenk is small (e.g., 78.4% vs. 59.1% for top-20 accuracy on Natural Questions). When training with mul- 8SQuAD is limited to a small set of Wikipedia documents and thus introduces unwanted bias. We will discuss this issue more in Section 5.1. 9Lucene implementation. BM25 parameters b = 0.4 (document length normalization) and k1 = 0 .9 (term frequency scaling) are tuned using development sets.

**中文**

5.1 主要结果 表 2 使用 top-k 准确率 (k∈{ 20, 100}) 比较了五个 QA 数据集上的不同段落检索系统。除 SQuAD 之外，DPR 在所有数据集上的表现始终优于 BM25。当 k 很小时，差距尤其大（例如，自然问题前 20 名的准确率分别为 78.4% 和 59.1%）。当使用 mul-8SQuAD 进行训练时，仅限于一小部分维基百科文档，从而引入不必要的偏差。我们将在 5.1 节中详细讨论这个问题。 9Lucene实现。 BM25 参数 b = 0.4（文档长度归一化）和 k1 = 0 .9（术语频率缩放）使用开发集进行调整。

### 段落 39 · Page 5

**EN**

20 40 60 80 100 k: # of retrieved passages 40 50 60 70 80 90Top-k accuracy (%) BM25 # Train: 1k # Train: 10k # Train: 20k # Train: 40k # Train: all (59k) Figure 1: Retriever top-k accuracy with different numbers of training examples used in our dense passage retriever vs BM25. The results are measured on the development set of Natural Questions. Our DPR trained using 1,000 examples already outperforms BM25. tiple datasets, TREC, the smallest dataset of the ﬁve, beneﬁts greatly from more training examples. In contrast, Natural Questions and WebQuestions improve modestly and TriviaQA degrades slightly.

**中文**

20 40 60 80 100 k: 检索到的段落数量 40 50 60 70 80 90Top-k 准确率 (%) BM25 # Train: 1k # Train: 10k # Train: 20k # Train: 40k # Train: all (59k) 图 1：我们的密集段落检索器中使用的不同数量训练示例的检索器 top-k 精度与BM25。结果是根据自然问题的发展集来衡量的。我们使用 1,000 个示例进行训练的 DPR 性能已经优于 BM25。在三个数据集中，TREC 是五个数据集中最小的数据集，它从更多的训练示例中受益匪浅。相比之下，自然问题和网络问题略有改善，而 TriviaQA 略有下降。

### 段落 40 · Page 5

**EN**

Results can be improved further in some cases by combining DPR with BM25 in both single- and multi-dataset settings. We conjecture that the lower performance on SQuAD is due to two reasons. First, the annotators wrote questions after seeing the passage. As a result, there is a high lexical overlap between passages and questions, which gives BM25 a clear advantage. Second, the data was collected from only 500+ Wikipedia articles and thus the distribution of training examples is extremely biased, as argued previously by Lee et al. (2019).

**中文**

在某些情况下，通过在单数据集和多数据集设置中将 DPR 与 BM25 相结合，可以进一步改善结果。我们推测 SQuAD 性能较低有两个原因。首先，注释者看到文章后提出问题。因此，段落和问题之间存在高度的词汇重叠，这给 BM25 带来了明显的优势。其次，数据仅从 500 多篇维基百科文章中收集，因此训练示例的分布存在极大偏差，正如 Lee 等人之前所说的那样。 （2019）。

### 段落 41 · Page 5

**EN**

5.2 Ablation Study on Model Training To understand further how different model training options affect the results, we conduct several additional experiments and discuss our ﬁndings below.

**中文**

5.2 模型训练的消融研究为了进一步了解不同的模型训练选项如何影响结果，我们进行了一些额外的实验并在下面讨论我们的发现。

### Page 6

### 段落 42 · Page 6

**EN**

Sample efﬁciency We explore how many training examples are needed to achieve good passage retrieval performance. Figure 1 illustrates the top-k retrieval accuracy with respect to different numbers of training examples, measured on the development set of Natural Questions. As is shown, a dense passage retriever trained using only 1,000 examples already outperforms BM25. This suggests that with a general pretrained language model, it is possible to train a high-quality dense retriever with a small number of question–passage pairs. Adding more training examples (from 1k to 59k) further improves the retrieval accuracy consistently.

**中文**

样本效率我们探讨需要多少训练样本才能实现良好的段落检索性能。图 1 说明了在自然问题的开发集上测量的不同数量训练示例的 top-k 检索准确性。如图所示，仅使用 1,000 个示例训练的密集通道检索器已经优于 BM25。这表明，使用通用的预训练语言模型，可以用少量的问题-段落对来训练高质量的密集检索器。添加更多训练示例（从 1k 到 59k）进一步持续提高检索精度。

### 段落 43 · Page 6

**EN**

In-batch negative training We test different training schemes on the development set of Natural Questions and summarize the results in Table 3. The top block is the standard 1-of-N training setting, where each question in the batch is paired with a positive passage and its own set of n negative passages (Eq. (2)). We ﬁnd that the choice of negatives — random, BM25 or gold passages (positive passages from other questions) — does not impact the top-k accuracy much in this setting whenk≥ 20. The middle bock is the in-batch negative training (Section 3.2) setting.

**中文**

批量负训练我们在自然问题的开发集上测试了不同的训练方案，并将结果总结在表 3 中。顶部块是标准的 1-of-N 训练设置，其中批次中的每个问题都与一个正样本和它自己的一组 n 个负样本配对（等式（2））。我们发现，当 k≥ 20 时，负样本的选择——随机、BM25 或黄金段落（来自其他问题的正样本段落）——不会对 top-k 准确率产生太大影响。中间的块是批内负训练（第 3.2 节）设置。

### 段落 44 · Page 6

**EN**

We ﬁnd that using a similar conﬁguration (7 gold negative passages), in-batch negative training improves the results substantially. The key difference between the two is whether the gold negative passages come from the same batch or from the whole training set. Effectively, in-batch negative training is an easy and memory-efﬁcient way to reuse the negative examples already in the batch rather than creating new ones. It produces more pairs and thus increases the number of training examples, which might contribute to the good model performance. As a result, accuracy consistently improves as the batch size grows.

**中文**

我们发现使用类似的配置（7 个黄金负向通道），批量负向训练可以显着改善结果。两者之间的主要区别在于黄金负通道是来自同一批次还是来自整个训练集。实际上，批量负面训练是一种简单且节省内存的方法，可以重用批次中已有的负面示例，而不是创建新的负面示例。它会产生更多对，从而增加训练示例的数量，这可能有助于获得良好的模型性能。因此，随着批量大小的增加，准确性不断提高。

### 段落 45 · Page 6

**EN**

Finally, we explore in-batch negative training with additional “hard” negative passages that have high BM25 scores given the question, but do not contain the answer string (the bottom block). These additional passages are used as negative passages for all questions in the same batch. We ﬁnd that adding a single BM25 negative passage improves the result substantially while adding two does not help further. Impact of gold passages We use passages that match the gold contexts in the original datasets (when available) as positive examples (Section 4.2).

**中文**

最后，我们探索批处理负面训练，其中包含额外的“困难”负面段落，这些段落在给定问题的情况下具有高 BM25 分数，但不包含答案字符串（底部块）。这些附加段落用作同一批次中所有问题的否定段落。我们发现添加单个 BM25 阴性通道可以显着改善结果，而添加两个则无济于事。黄金段落的影响 我们使用与原始数据集中的黄金上下文（如果可用）匹配的段落作为正面示例（第 4.2 节）。

### 段落 46 · Page 6

**EN**

Type #N IB Top-5 Top-20 Top-100 Random 7  47.0 64.3 77.8 BM25 7  50.0 63.3 74.8 Gold 7  42.6 63.1 78.3 Gold 7  51.1 69.1 80.8 Gold 31  52.1 70.8 82.1 Gold 127  55.8 73.0 83.1 G.+BM25(1) 31+32  65.0 77.3 84.4 G.+BM25(2) 31+64  64.5 76.4 84.0 G.+BM25(1) 127+128  65.8 78.0 84.9 Table 3: Comparison of different training schemes, measured as top-k retrieval accuracy on Natural Questions (development set). #N: number of negative examples, IB: in-batch training. G.+BM25 (1) and G.+BM25(2) denote in-batch training with 1 or 2 additional BM25 negatives, which serve as negative passages for all questions in the batch.

**中文**

类型 #N IB Top-5 Top-20 Top-100 随机 7 47.0 64.3 77.8 BM25 7 50.0 63.3 74.8 Gold 7 42.6 63.1 78.3 Gold 7 51.1 69.1 80.8 Gold 31 52.1 70.8 82.1 Gold 127 55.8 73.0 83.1 G.+BM25(1) 31+32 65.0 77.3 84.4 G.+BM25(2) 31+64 64.5 76.4 84.0 G.+BM25(1) 127+128 65.8 78.0 84.9 表3：不同训练方案的比较，以自然问题（开发集）的 top-k 检索精度来衡量。 #N：负例数量，IB：批量训练。 G.+BM25 (1) 和 G.+BM25(2) 表示具有 1 或 2 个附加 BM25 负数的批内训练，这些负数作为批次中所有问题的负数段落。

### 段落 47 · Page 6

**EN**

Our experiments on Natural Questions show that switching to distantly-supervised passages (using the highest-ranked BM25 passage that contains the answer), has only a small impact: 1 point lower top-k accuracy for retrieval. Appendix A contains more details. Similarity and loss Besides dot product, cosine and Euclidean L2 distance are also commonly used as decomposable similarity functions. We test these alternatives and ﬁnd that L2 performs comparable to dot product, and both of them are superior to cosine.

**中文**

我们对自然问题的实验表明，切换到远程监督的段落（使用包含答案的排名最高的 BM25 段落）只会产生很小的影响：检索的 top-k 准确度降低 1 个百分点。附录 A 包含更多详细信息。相似度和损失 除了点积之外，余弦和欧几里德 L2 距离也常用作可分解的相似度函数。我们测试了这些替代方案，发现 L2 的性能与点积相当，并且两者都优于余弦。

### 段落 48 · Page 6

**EN**

Similarly, in addition to negative loglikelihood, a popular option for ranking is triplet loss, which compares a positive passage and a negative one directly with respect to a question (Burges et al., 2005). Our experiments show that using triplet loss does not affect the results much. More details can be found in Appendix B. Cross-dataset generalization One interesting question regarding DPR’s discriminative training is how much performance degradation it may suffer from a non-iid setting. In other words, can it still generalize well when directly applied to a different dataset without additional ﬁne-tuning?

**中文**

类似地，除了负对数似然之外，一种流行的排名选项是三元组损失，它直接比较某个问题的正段落和负段落（Burges 等，2005）。我们的实验表明，使用三重态损失不会对结果产生太大影响。更多细节可以在附录 B 中找到。 跨数据集泛化 关于 DPR 判别训练的一个有趣的问题是，它可能会因非独立同分布设置而遭受多少性能下降。换句话说，当直接应用于不同的数据集而无需额外的微调时，它仍然可以很好地泛化吗？

### 段落 49 · Page 6

**EN**

To test the cross-dataset generalization, we train DPR on Natural Questions only and test it directly on the smaller WebQuestions and CuratedTREC datasets. We ﬁnd that DPR generalizes well, with 3-5 points loss from the best performing ﬁne-tuned model in top-20 retrieval accuracy (69.9/86.3 vs. 75.0/89.1 for WebQuestions and TREC, respectively), while still greatly outperforming the BM25 baseline (55.0/70.9).

**中文**

为了测试跨数据集泛化，我们仅在 Natural Questions 上训练 DPR，并直接在较小的 WebQuestions 和 CuratedTREC 数据集上进行测试。我们发现 DPR 的泛化能力很好，在前 20 名检索准确度中，比表现最好的微调模型损失了 3-5 分（WebQuestions 和 TREC 分别为 69.9/86.3 与 75.0/89.1），但仍然大大优于 BM25 基线（55.0/70.9）。

### Page 7

### 段落 50 · Page 7

**EN**

5.3 Qualitative Analysis Although DPR performs better than BM25 in general, passages retrieved by these two methods differ qualitatively. Term-matching methods like BM25 are sensitive to highly selective keywords and phrases, while DPR captures lexical variations or semantic relationships better. See Appendix C for examples and more discussion. 5.4 Run-time Efﬁciency The main reason that we require a retrieval component for open-domain QA is to reduce the number of candidate passages that the reader needs to consider, which is crucial for answering user’s questions in real-time.

**中文**

5.3 定性分析 虽然DPR 总体上比BM25 表现更好，但这两种方法检索到的段落在质量上有所不同。 BM25 等术语匹配方法对高度选择性的关键字和短语敏感，而 DPR 可以更好地捕获词汇变化或语义关系。有关示例和更多讨论，请参阅附录 C。 5.4 运行时效率 我们需要开放域问答的检索组件的主要原因是为了减少读者需要考虑的候选段落的数量，这对于实时回答用户的问题至关重要。

### 段落 51 · Page 7

**EN**

We proﬁled the passage retrieval speed on a server with Intel Xeon CPU E5-2698 v4 @ 2.20GHz and 512GB memory. With the help of FAISS in-memory index for real-valued vectors10, DPR can be made incredibly efﬁcient, processing 995.0 questions per second, returning top 100 passages per question. In contrast, BM25/Lucene (implemented in Java, using ﬁle index) processes 23.7 questions per second per CPU thread. On the other hand, the time required for building an index for dense vectors is much longer. Computing dense embeddings on 21-million passages is resource intensive, but can be easily parallelized, taking roughly 8.8 hours on 8 GPUs.

**中文**

我们对配备 Intel Xeon CPU E5-2698 v4 @ 2.20GHz 和 512GB 内存的服务器上的段落检索速度进行了分析。借助 FAISS 实值向量内存索引10，DPR 可以变得非常高效，每秒处理 995.0 个问题，每个问题返回前 100 个段落。相比之下，BM25/Lucene（用 Java 实现，使用文件索引）每个 CPU 线程每秒处理 23.7 个问题。另一方面，为密集向量构建索引所需的时间要长得多。在 2100 万个通道上计算密集嵌入需要大量资源，但可以轻松并行化，在 8 个 GPU 上大约需要 8.8 小时。

### 段落 52 · Page 7

**EN**

However, building the FAISS index on 21-million vectors on a single server takes 8.5 hours. In comparison, building an inverted index using Lucene is much cheaper and takes only about 30 minutes in total. 6 Experiments: Question Answering In this section, we experiment with how different passage retrievers affect the ﬁnal QA accuracy. 6.1 End-to-end QA System We implement an end-to-end question answering system in which we can plug different retriever systems directly. Besides the retriever, our QA system consists of a neural reader that outputs the answer to the question.

**中文**

然而，在单个服务器上对 2100 万个向量构建 FAISS 索引需要 8.5 小时。相比之下，使用 Lucene 构建倒排索引要便宜得多，总共只需要 30 分钟左右。 6 实验：问答 在本节中，我们实验不同的段落检索器如何影响最终的 QA 准确性。 6.1 端到端的问答系统 我们实现了一个端到端的问答系统，我们可以在其中直接插入不同的检索器系统。除了检索器之外，我们的 QA 系统还包含一个输出问题答案的神经阅读器。

### 段落 53 · Page 7

**EN**

Given the top k retrieved passages (up to 100 in our experiments), the reader assigns a passage selection score to each passage. In addition, it extracts an answer span from each passage and assigns a span score. The best span from the passage with the highest passage selection 10FAISS conﬁguration: we used HNSW index type on CPU, neighbors to store per node = 512, construction time search depth = 200, search depth = 128. score is chosen as the ﬁnal answer. The passage selection model serves as a reranker through crossattention between the question and the passage.

**中文**

给定检索到的前 k 个段落（在我们的实验中最多 100 个），读者为每个段落分配一个段落选择分数。此外，它还从每个段落中提取答案跨度并分配跨度分数。具有最高段落选择的段落的最佳跨度10FAISS配置：我们在CPU上使用HNSW索引类型，每个节点存储的邻居= 512，构建时间搜索深度= 200，搜索深度= 128。选择分数作为最终答案。段落选择模型通过问题和段落之间的交叉注意力来充当重新排序器。

### 段落 54 · Page 7

**EN**

Although cross-attention is not feasible for retrieving relevant passages in a large corpus due to its nondecomposable nature, it has more capacity than the dual-encoder model sim(q,p ) as in Eq. (1). Applying it to selecting the passage from a small number of retrieved candidates has been shown to work well (Wang et al., 2019, 2018; Lin et al., 2018). Speciﬁcally, let Pi ∈ RL×h (1≤ i≤ k) be a BERT (base, uncased in our experiments) representation for the i-th passage, where L is the maximum length of the passage andh the hidden dimension.

**中文**

虽然交叉注意力由于其不可分解的性质而无法在大型语料库中检索相关段落，但它比双编码器模型 sim(q,p ) 具有更大的容量，如等式 1 所示。 (1).将其应用于从少量检索到的候选者中选择段落已被证明效果良好（Wang et al., 2019, 2018; Lin et al., 2018）。具体来说，令 Pi ∈ RL×h (1≤ i≤ k) 为第 i 段的 BERT（基础，在我们的实验中未加大小写）表示，其中 L 是该段的最大长度，h 是隐藏维度。

### 段落 55 · Page 7

**EN**

The probabilities of a token being the starting/ending positions of an answer span and a passage being selected are deﬁned as: Pstart,i(s) = softmax ( Piwstart ) s, (3) Pend,i(t) = softmax ( Piwend ) t, (4) Pselected(i) = softmax (ˆP⊺wselected ) i, (5) where ˆP = [ P[CLS] 1 ,..., P[CLS] k ] ∈ Rh×k and wstart, wend, wselected∈ Rh are learnable vectors. We compute a span score of thes-th tot-th words from thei-th passage asPstart,i(s)×Pend,i(t), and a passage selection score of the i-th passage as Pselected(i).

**中文**

标记作为答案范围和被选择的段落的起始/结束位置的概率定义为： Pstart,i(s) = softmax ( Piwstart ) s, (3) Pend,i(t) = softmax ( Piwend ) t, (4) Pselected(i) = softmax (ˆP⊺wselected ) i, (5) 其中 ˆP = [ P[CLS] 1 ,..., P[CLS] k ] ∈ Rh×k 和 wstart, wend, wselected ∈ Rh 是可学习向量。我们计算第i个段落中第s个到第t个单词的跨度分数作为Pstart,i(s)×Pend,i(t)，以及第i个段落的段落选择分数作为Pselected(i)。

### 段落 56 · Page 7

**EN**

During training, we sample one positive and ˜m− 1 negative passages from the top 100 passages returned by the retrieval system (BM25 or DPR) for each question. ˜m is a hyper-parameter and we use ˜m = 24 in all the experiments. The training objective is to maximize the marginal log-likelihood of all the correct answer spans in the positive passage (the answer string may appear multiple times in one passage), combined with the log-likelihood of the positive passage being selected. We use the batch size of 16 for large (NQ, TriviaQA, SQuAD) and 4 for small (TREC, WQ) datasets, and tunek on the development set.

**中文**

在训练过程中，我们从检索系统（BM25 或 DPR）返回的每个问题的前 100 个段落中采样一个正向段落和 ~m−1 个负向段落。 〜m 是一个超参数，我们在所有实验中使用〜m = 24。训练目标是最大化正向段落中所有正确答案范围的边际对数似然（答案字符串可能在一篇段落中出现多次），并结合所选择的正向段落的对数似然。对于大型（NQ、TriviaQA、SQuAD）数据集，我们使用批量大小 16，对于小型（TREC、WQ）数据集，我们使用批量大小 4，并在开发集上进行tunek。

### 段落 57 · Page 7

**EN**

For experiments on small datasets under the Multi setting, in which using other datasets is allowed, we ﬁne-tune the reader trained on Natural Questions to the target dataset. All experiments were done on eight 32GB GPUs. 6.2 Results Table 4 summarizes our ﬁnal end-to-end QA results, measured by exact match with the reference answer after minor normalization as in (Chen et al., 2017; Lee et al., 2019). From the table, we can

**中文**

对于“多重”设置下的小数据集实验（允许使用其他数据集），我们将接受过自然问题训练的读者微调到目标数据集。所有实验均在八个 32GB GPU 上完成。 6.2 结果 表 4 总结了我们最终的端到端 QA 结果，通过轻微标准化后与参考答案的精确匹配来衡量，如（Chen 等人，2017 年；Lee 等人，2019 年）。从表中我们可以

### Page 8

### 段落 58 · Page 8

**EN**

Training Model NQ TriviaQA WQ TREC SQuAD Single BM25+BERT (Lee et al., 2019) 26.5 47.1 17.7 21.3 33.2 Single ORQA (Lee et al., 2019) 33.3 45.0 36.4 30.1 20.2 Single HardEM (Min et al., 2019a) 28.1 50.9 - - - Single GraphRetriever (Min et al., 2019b) 34.5 56.0 36.4 - - Single PathRetriever (Asai et al., 2020) 32.6 - - - 56.5 Single REALM Wiki (Guu et al., 2020) 39.2 - 40.2 46.8 - Single REALM News (Guu et al., 2020) 40.4 - 40.7 42.9 - Single BM25 32.6 52.4 29.9 24.9 38.1 DPR 41.5 56.8 34.6 25.9 29.8 BM25+DPR 39.0 57.0 35.2 28.0 36.7 Multi DPR 41.5 56.8 42.4 49.4 24.1 BM25+DPR 38.8 57.9 41.1 50.6 35.8 Table 4: End-to-end QA (Exact Match) Accuracy.

**中文**

训练模型 NQ TriviaQA WQ TREC SQuAD Single BM25+BERT (Lee et al., 2019) 26.5 47.1 17.7 21.3 33.2 Single ORQA (Lee et al., 2019) 33.3 45.0 36.4 30.1 20.2 Single HardEM (Min et al., 2019a) 28.1 50.9 - - - Single GraphRetriever (Min et al., 2019b) 34.5 56.0 36.4 - - Single PathRetriever (Asai et al., 2020) 32.6 - - - 56.5 Single REALM Wiki (Guu et al., 2020) 39.2 - 40.2 46.8 - Single REALM 新闻（Guu 等人，2020） 40.4 - 40.7 42.9 - 单 BM25 32.6 52.4 29.9 24.9 38.1 DPR 41.5 56.8 34.6 25.9 29.8 BM25+DPR 39.0 57.0 35.2 28.0 36.7 多 DPR 41.5 56.8 42.4 49.4 24.1 BM25+DPR 38.8 57.9 41.1 50.6 35.8 表 4：端到端 QA（精确匹配）准确度。

### 段落 59 · Page 8

**EN**

The ﬁrst block of results are copied from their cited papers. REALMWiki and REALMNews are the same model but pretrained on Wikipedia and CC-News, respectively.Single and Multi denote that our Dense Passage Retriever (DPR) is trained using individual or combined training datasets (all except SQuAD). For WQ and TREC in the Multi setting, we ﬁne-tune the reader trained on NQ. see that higher retriever accuracy typically leads to better ﬁnal QA results: in all cases except SQuAD, answers extracted from the passages retrieved by DPR are more likely to be correct, compared to those from BM25.

**中文**

第一个结果块是从他们引用的论文中复制的。 REALMWiki 和 REALMNews 是相同的模型，但分别在 Wikipedia 和 CC-News 上进行了预训练。Single 和 Multi 表示我们的密集通道检索器 (DPR) 使用单独或组合训练数据集（除 SQuAD 之外的所有数据集）进行训练。对于 Multi 设置中的 WQ 和 TREC，我们对在 NQ 上训练的读者进行微调。可以看出，较高的检索器准确度通常会带来更好的最终 QA 结果：在除 SQuAD 之外的所有情况下，与 BM25 中的答案相比，从 DPR 检索到的段落中提取的答案更有可能是正确的。

### 段落 60 · Page 8

**EN**

For large datasets like NQ and TriviaQA, models trained using multiple datasets (Multi) perform comparably to those trained using the individual training set (Single). Conversely, on smaller datasets like WQ and TREC, the multidataset setting has a clear advantage. Overall, our DPR-based models outperform the previous stateof-the-art results on four out of the ﬁve datasets, with 1% to 12% absolute differences in exact match accuracy. It is interesting to contrast our results to those of ORQA (Lee et al., 2019) and also the concurrently developed approach, REALM (Guu et al., 2020).

**中文**

对于 NQ 和 TriviaQA 等大型数据集，使用多个数据集（多）训练的模型的性能与使用单个训练集（单）训练的模型相当。相反，在 WQ 和 TREC 等较小的数据集上，多数据集设置具有明显的优势。总体而言，我们基于 DPR 的模型在五个数据集中的四个上优于之前最先进的结果，精确匹配精度有 1% 到 12% 的绝对差异。将我们的结果与 ORQA（Lee 等人，2019）以及同时开发的方法 REALM（Guu 等人，2020）的结果进行对比是很有趣的。

### 段落 61 · Page 8

**EN**

While both methods include additional pretraining tasks and employ an expensive end-to-end training regime, DPR manages to outperform them on both NQ and TriviaQA, simply by focusing on learning a strong passage retrieval model using pairs of questions and answers. The additional pretraining tasks are likely more useful only when the target training sets are small. Although the results of DPR on WQ and TREC in the single-dataset setting are less competitive, adding more question–answer pairs helps boost the performance, achieving the new state of the art.

**中文**

虽然这两种方法都包含额外的预训练任务并采用昂贵的端到端训练机制，但 DPR 仅仅通过专注于使用问题和答案对学习强大的段落检索模型，就成功地在 NQ 和 TriviaQA 上超越了它们。仅当目标训练集较小时，额外的预训练任务可能才更有用。尽管在单数据集设置中 DPR 在 WQ 和 TREC 上的结果竞争力较差，但添加更多问答对有助于提高性能，实现新的最先进水平。

### 段落 62 · Page 8

**EN**

To compare our pipeline training approach with joint learning, we run an ablation on Natural Questions where the retriever and reader are jointly trained, following Lee et al. (2019). This approach obtains a score of 39.8 EM, which suggests that our strategy of training a strong retriever and reader in isolation can leverage effectively available supervision, while outperforming a comparable joint training approach with a simpler design (Appendix D). One thing worth noticing is that our reader does consider more passages compared to ORQA, although it is not completely clear how much more time it takes for inference.

**中文**

为了将我们的管道训练方法与联合学习进行比较，我们按照 Lee 等人的研究，对自然问题进行了消融，其中检索器和阅读器被联合训练。 （2019）。这种方法获得了 39.8 EM 的分数，这表明我们单独训练强大的检索器和阅读器的策略可以利用有效的可用监督，同时优于具有更简单设计的类似联合训练方法（附录 D）。值得注意的一件事是，与 ORQA 相比，我们的读者确实考虑了更多的段落，尽管尚不完全清楚推理需要多花多少时间。

### 段落 63 · Page 8

**EN**

While DPR processes up to 100 passages for each question, the reader is able to ﬁt all of them into one batch on a single 32GB GPU, thus the latency remains almost identical to the single passage case (around 20ms). The exact impact on throughput is harder to measure: ORQA uses 2-3x longer passages compared to DPR (288 word pieces compared to our 100 tokens) and the computational complexity is superlinear in passage length. We also note that we foundk = 50 to be optimal for NQ, and k = 10 leads to only marginal loss in exact match accuracy (40.8 vs. 41.5 EM on NQ), which should be roughly comparable to ORQA’s 5-passage setup.

**中文**

虽然 DPR 为每个问题处理多达 100 篇文章，但读者能够将所有这些文章放入单个 32GB GPU 上的一批中，因此延迟几乎与单篇文章的情况相同（大约 20 毫秒）。对吞吐量的确切影响更难以衡量：与 DPR 相比，ORQA 使用 2-3 倍长的段落（与我们的 100 个标记相比，有 288 个单词片段），并且计算复杂度在段落长度上是超线性的。我们还注意到，我们发现 k = 50 对于 NQ 来说是最佳的，而 k = 10 只会导致精确匹配精度的边际损失（NQ 上的 EM 为 40.8 vs. 41.5 EM），这应该与 ORQA 的 5 通道设置大致相当。

### 段落 64 · Page 8

**EN**

7 Related Work Passage retrieval has been an important component for open-domain QA (V oorhees, 1999). It not only effectively reduces the search space for answer extraction, but also identiﬁes the support context for users to verify the answer. Strong sparse vector space models like TF-IDF or BM25 have

**中文**

7 相关工作 段落检索一直是开放域 QA 的重要组成部分（V oorhees，1999）。它不仅有效地减少了答案提取的搜索空间，而且还识别了用户验证答案的支持上下文。强稀疏向量空间模型（如 TF-IDF 或 BM25）具有

### Page 9

### 段落 65 · Page 9

**EN**

been used as the standard method applied broadly to various QA tasks (e.g., Chen et al., 2017; Yang et al., 2019a,b; Nie et al., 2019; Min et al., 2019a; Wolfson et al., 2020). Augmenting text-based retrieval with external structured information, such as knowledge graph and Wikipedia hyperlinks, has also been explored recently (Min et al., 2019b; Asai et al., 2020). The use of dense vector representations for retrieval has a long history since Latent Semantic Analysis (Deerwester et al., 1990).

**中文**

已被用作广泛应用于各种 QA 任务的标准方法（例如，Chen 等人，2017；Yang 等人，2019a,b；Nie 等人，2019；Min 等人，2019a；Wolfson 等人，2020）。最近还探索了利用外部结构化信息（例如知识图和维基百科超链接）增强基于文本的检索（Min 等人，2019b；Asai 等人，2020）。自潜在语义分析以来，使用密集向量表示进行检索已有很长的历史（Deerwester 等人，1990）。

### 段落 66 · Page 9

**EN**

Using labeled pairs of queries and documents, discriminatively trained dense encoders have become popular recently (Yih et al., 2011; Huang et al., 2013; Gillick et al., 2019), with applications to cross-lingual document retrieval, ad relevance prediction, Web search and entity retrieval. Such approaches complement the sparse vector methods as they can potentially give high similarity scores to semantically relevant text pairs, even without exact token matching. The dense representation alone, however, is typically inferior to the sparse one.

**中文**

使用标记的查询和文档对，有区别地训练的密集编码器最近变得流行（Yih et al., 2011; Huang et al., 2013; Gillick et al., 2019），并应用于跨语言文档检索、广告相关性预测、网络搜索和实体检索。这些方法补充了稀疏向量方法，因为即使没有精确的标记匹配，它们也可以为语义相关的文本对提供高相似度分数。然而，仅密集表示通常不如稀疏表示。

### 段落 67 · Page 9

**EN**

While not the focus of this work, dense representations from pretrained models, along with cross-attention mechanisms, have also been shown effective in passage or dialogue re-ranking tasks (Nogueira and Cho, 2019; Humeau et al., 2020). Finally, a concurrent work (Khattab and Zaharia, 2020) demonstrates the feasibility of full dense retrieval in IR tasks. Instead of employing the dual-encoder framework, they introduced a late-interaction operator on top of the BERT encoders. Dense retrieval for open-domain QA has been explored by Das et al. (2019), who propose to retrieve relevant passages iteratively using reformulated question vectors.

**中文**

虽然不是这项工作的重点，但预训练模型的密集表示以及交叉注意机制在段落或对话重新排序任务中也被证明是有效的（Nogueira 和 Cho，2019 年；Humeau 等人，2020 年）。最后，一项并行工作（Khattab 和 Zaharia，2020）证明了 IR 任务中全密集检索的可行性。他们没有采用双编码器框架，而是在 BERT 编码器之上引入了后期交互算子。 Das 等人探索了开放域 QA 的密集检索。 （2019），他建议使用重新表述的问题向量迭代检索相关段落。

### 段落 68 · Page 9

**EN**

As an alternative approach that skips passage retrieval, Seo et al. (2019) propose to encode candidate answer phrases as vectors and directly retrieve the answers to the input questions efﬁciently. Using additional pretraining with the objective that matches surrogates of questions and relevant passages, Lee et al. (2019) jointly train the question encoder and reader. Their approach outperforms the BM25 plus reader paradigm on multiple open-domain QA datasets in QA accuracy, and is further extended by REALM (Guu et al., 2020), which includes tuning the passage encoder asynchronously by re-indexing the passages during training.

**中文**

作为跳过段落检索的替代方法，Seo 等人。 （2019）建议将候选答案短语编码为向量，并直接有效地检索输入问题的答案。 Lee 等人使用额外的预训练，其目标是匹配问题的替代项和相关段落。 （2019）联合训练问题编码器和阅读器。他们的方法在 QA 准确性方面优于多个开放域 QA 数据集上的 BM25 plus reader 范例，并通过 REALM 进一步扩展（Guu 等人，2020），其中包括通过在训练期间重新索引段落来异步调整段落编码器。

### 段落 69 · Page 9

**EN**

The pretraining objective has also recently been improved by Xiong et al. (2020b). In contrast, our model provides a simple and yet effective solution that shows stronger empirical performance, without relying on additional pretraining or complex joint training schemes. DPR has also been used as an important module in very recent work. For instance, extending the idea of leveraging hard negatives, Xiong et al. (2020a) use the retrieval model trained in the previous iteration to discover new negatives and construct a different set of examples in each training iteration.

**中文**

Xiong 等人最近也改进了预训练目标。 （2020b）。相比之下，我们的模型提供了一个简单而有效的解决方案，显示出更强的经验性能，而不依赖于额外的预训练或复杂的联合训练方案。 DPR 在最近的工作中也被用作一个重要模块。例如，熊等人扩展了利用硬底片的想法。 (2020a) 使用前一次迭代中训练的检索模型来发现新的负例，并在每次训练迭代中构建一组不同的示例。

### 段落 70 · Page 9

**EN**

Starting from our trained DPR model, they show that the retrieval performance can be further improved. Recent work (Izacard and Grave, 2020; Lewis et al., 2020b) have also shown that DPR can be combined with generation models such as BART (Lewis et al., 2020a) and T5 (Raffel et al., 2019), achieving good performance on open-domain QA and other knowledge-intensive tasks. 8 Conclusion In this work, we demonstrated that dense retrieval can outperform and potentially replace the traditional sparse retrieval component in open-domain question answering.

**中文**

从我们训练的 DPR 模型开始，他们表明检索性能可以进一步提高。最近的工作（Izacard 和 Grave，2020；Lewis 等人，2020b）还表明，DPR 可以与 BART（Lewis 等人，2020a）和 T5（Raffel 等人，2019）等生成模型相结合，在开放域 QA 和其他知识密集型任务上取得良好的性能。 8 结论 在这项工作中，我们证明了密集检索可以优于并有可能取代开放域问答中的传统稀疏检索组件。

### 段落 71 · Page 9

**EN**

While a simple dual-encoder approach can be made to work surprisingly well, we showed that there are some critical ingredients to training a dense retriever successfully. Moreover, our empirical analysis and ablation studies indicate that more complex model frameworks or similarity functions do not necessarily provide additional values. As a result of improved retrieval performance, we obtained new state-of-the-art results on multiple open-domain question answering benchmarks. Acknowledgments We thank the anonymous reviewers for their helpful comments and suggestions.

**中文**

虽然简单的双编码器方法可以取得令人惊讶的效果，但我们表明，成功训练密集检索器有一些关键因素。此外，我们的实证分析和消融研究表明，更复杂的模型框架或相似函数不一定提供额外的价值。由于检索性能的提高，我们在多个开放域问答基准上获得了最新的结果。致谢我们感谢匿名审稿人提出的有益的意见和建议。

### 段落 72 · Page 9

**EN**

References Akari Asai, Kazuma Hashimoto, Hannaneh Hajishirzi, Richard Socher, and Caiming Xiong. 2020. Learning to retrieve reasoning paths over Wikipedia graph for question answering. In International Conference on Learning Representations (ICLR). Petr Baudi ˇs and Jan ˇSediv`y. 2015. Modeling of the question answering task in the yodaqa system. In International Conference of the Cross-Language Evaluation Forum for European Languages, pages 222– 228. Springer. Jonathan Berant, Andrew Chou, Roy Frostig, and Percy Liang. 2013. Semantic parsing on Freebase from

**中文**

参考文献 Akari Asai、Kazuma Hashimoto、Hannaneh Hajishirzi、Richard Socher 和 Caiming Xiong。 2020. 学习通过维基百科图检索推理路径以进行问答。在国际学习表征会议（ICLR）中。 Petr Baudi ˇs 和 Jan ˇSediv`y。 2015. yodaqa系统中问答任务的建模。欧洲语言跨语言评估论坛国际会议，第 222-228 页。Springer。乔纳森·贝兰特、安德鲁·周、罗伊·弗罗斯蒂格和珀西·梁。 2013. Freebase 上的语义解析来自

### Page 10

### 段落 73 · Page 10

**EN**

question-answer pairs. In Empirical Methods in Natural Language Processing (EMNLP). Jane Bromley, Isabelle Guyon, Yann LeCun, Eduard S¨ackinger, and Roopak Shah. 1994. Signature veriﬁcation using a “Siamese” time delay neural network. In NIPS, pages 737–744. Chris Burges, Tal Shaked, Erin Renshaw, Ari Lazier, Matt Deeds, Nicole Hamilton, and Greg Hullender. 2005. Learning to rank using gradient descent. In Proceedings of the 22nd international conference on Machine learning, pages 89–96. Danqi Chen, Adam Fisch, Jason Weston, and Antoine Bordes. 2017. Reading Wikipedia to answer opendomain questions.

**中文**

问答对。在自然语言处理（EMNLP）的经验方法中。简·布罗姆利、伊莎贝尔·盖恩、扬·勒昆、爱德华·塞金格和鲁帕克·沙阿。 1994. 使用“连体”延时神经网络进行签名验证。 NIPS，第 737-744 页。克里斯·伯吉斯、塔尔·沙克德、艾琳·伦肖、阿里·拉齐尔、马特·迪兹、妮可·汉密尔顿和格雷格·胡伦德。 2005.学习使用梯度下降进行排名。第 22 届国际机器学习会议记录，第 89-96 页。陈丹琪、亚当·费什、杰森·韦斯顿和安托万·博德斯。 2017.阅读维基百科来回答开放域问题。

### 段落 74 · Page 10

**EN**

In Association for Computational Linguistics (ACL), pages 1870–1879. Rajarshi Das, Shehzaad Dhuliawala, Manzil Zaheer, and Andrew McCallum. 2019. Multi-step retrieverreader interaction for scalable open-domain question answering. In International Conference on Learning Representations (ICLR). Scott Deerwester, Susan T Dumais, George W Furnas, Thomas K Landauer, and Richard Harshman. 1990. Indexing by latent semantic analysis. Journal of the American society for information science , 41(6):391–407. Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. 2019.

**中文**

计算语言学协会 (ACL)，第 1870-1879 页。 Rajarshi Das、Shehzaad Dhuliawala、Manzil Zaheer 和 Andrew McCallum。 2019.用于可扩展开放域问答的多步骤检索器阅读器交互。在国际学习表征会议（ICLR）中。斯科特·迪尔韦斯特、苏珊·T·杜迈斯、乔治·W·弗纳斯、托马斯·K·兰道尔和理查德·哈什曼。 1990。通过潜在语义分析进行索引。美国信息科学学会杂志，41（6）：391-407。雅各布·德夫林、张明伟、肯顿·李和克里斯蒂娜·图塔诺娃。 2019.

### 段落 75 · Page 10

**EN**

BERT: Pre-training of deep bidirectional transformers for language understanding. In North American Association for Computational Linguistics (NAACL). David A Ferrucci. 2012. Introduction to “This is Watson”. IBM Journal of Research and Development , 56(3.4):1–1. Daniel Gillick, Sayali Kulkarni, Larry Lansing, Alessandro Presta, Jason Baldridge, Eugene Ie, and Diego Garcia-Olano. 2019. Learning dense representations for entity retrieval. In Computational Natural Language Learning (CoNLL). Ruiqi Guo, Sanjiv Kumar, Krzysztof Choromanski, and David Simcha. 2016. Quantization based fast inner product search.

**中文**

BERT：用于语言理解的深度双向转换器的预训练。在北美计算语言学协会（NAACL）。大卫·A·费鲁奇. 2012.“这就是沃森”简介。 IBM 研究与开发杂志，56(3.4):1–1。丹尼尔·吉利克、萨亚里·库尔卡尼、拉里·兰辛、亚历山德罗·普雷斯塔、杰森·鲍德里奇、尤金·伊伊和迭戈·加西亚-奥拉诺。 2019.学习实体检索的密集表示。计算自然语言学习（CoNLL）。郭瑞琪、Sanjiv Kumar、Krzysztof Choromanski 和 David Simcha。 2016.基于量化的快速内积搜索。

### 段落 76 · Page 10

**EN**

In Artiﬁcial Intelligence and Statistics, pages 482–490. Kelvin Guu, Kenton Lee, Zora Tung, Panupong Pasupat, and Ming-Wei Chang. 2020. REALM: Retrieval-augmented language model pre-training. ArXiv, abs/2002.08909. Matthew Henderson, Rami Al-Rfou, Brian Strope, Yunhsuan Sung, L ´aszl´o Luk´acs, Ruiqi Guo, Sanjiv Kumar, Balint Miklos, and Ray Kurzweil. 2017. Efﬁcient natural language response suggestion for smart reply. ArXiv, abs/1705.00652. Po-Sen Huang, Xiaodong He, Jianfeng Gao, Li Deng, Alex Acero, and Larry Heck. 2013. Learning deep structured semantic models for Web search using clickthrough data.

**中文**

《人工智能与统计》，第 482-490 页。 Kelvin Guu、Kenton Lee、Zora Tung、Panupong Pasupat 和 Ming-Wei Chang。 2020. REALM：检索增强语言模型预训练。 ArXiv，abs/2002.08909。马修·亨德森、拉米·阿尔福、布莱恩·斯特普、宋云轩、L´aszl´o Luk´acs、郭瑞琪、桑吉夫·库马尔、巴林特·米克洛斯和雷·库兹韦尔。 2017.高效自然语言回复建议，实现智能回复。 ArXiv，abs/1705.00652。黄珀森、何晓东、高剑峰、邓力、Alex Acero 和 Larry Heck。 2013 年。使用点击数据学习网络搜索的深度结构化语义模型。

### 段落 77 · Page 10

**EN**

In ACM International Conference on Information and Knowledge Management (CIKM), pages 2333–2338. Samuel Humeau, Kurt Shuster, Marie-Anne Lachaux, and Jason Weston. 2020. Poly-encoders: Architectures and pre-training strategies for fast and accurate multi-sentence scoring. In International Conference on Learning Representations (ICLR). Gautier Izacard and Edouard Grave. 2020. Leveraging passage retrieval with generative models for open domain question answering. ArXiv, abs/2007.01282. Jeff Johnson, Matthijs Douze, and Herv ´e J´egou. 2017. Billion-scale similarity search with GPUs. ArXiv, abs/1702.08734.

**中文**

ACM 国际信息和知识管理会议 (CIKM)，第 2333-2338 页。塞缪尔·休莫、库尔特·舒斯特、玛丽-安妮·拉肖和杰森·韦斯顿。 2020. 多编码器：用于快速准确的多句子评分的架构和预训练策略。在国际学习表征会议（ICLR）中。戈蒂埃·伊扎卡尔和爱德华·格雷夫。 2020。利用段落检索和生成模型进行开放域问答。 ArXiv，abs/2007.01282。杰夫·约翰逊、马蒂斯·杜兹和赫夫·杰古。 2017. 使用 GPU 进行十亿级相似性搜索。 ArXiv，abs/1702.08734。

### 段落 78 · Page 10

**EN**

Mandar Joshi, Eunsol Choi, Daniel Weld, and Luke Zettlemoyer. 2017. TriviaQA: A large scale distantly supervised challenge dataset for reading comprehension. In Association for Computational Linguistics (ACL), pages 1601–1611. Omar Khattab and Matei Zaharia. 2020. ColBERT: Efﬁcient and effective passage search via contextualized late interaction over BERT. In ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR), pages 39–48. Brian Kulis. 2013. Metric learning: A survey. Foundations and Trends in Machine Learning, 5(4):287– 364.

**中文**

曼达尔·乔希、恩索尔·崔、丹尼尔·韦尔德和卢克·泽特尔莫耶。 2017.TriviaQA：用于阅读理解的大规模远程监督挑战数据集。计算语言学协会 (ACL)，第 1601-1611 页。奥马尔·哈塔布和马泰·扎哈里亚。 2020. ColBERT：通过 BERT 上的上下文后期交互进行高效且有效的段落搜索。摘自 ACM SIGIR 信息检索研究与开发会议 (SIGIR)，第 39-48 页。布赖恩·库利斯. 2013。度量学习：一项调查。机器学习的基础和趋势，5(4)：287–364。

### 段落 79 · Page 10

**EN**

Tom Kwiatkowski, Jennimaria Palomaki, Olivia Red- ﬁeld, Michael Collins, Ankur Parikh, Chris Alberti, Danielle Epstein, Illia Polosukhin, Matthew Kelcey, Jacob Devlin, Kenton Lee, Kristina N. Toutanova, Llion Jones, Ming-Wei Chang, Andrew Dai, Jakob Uszkoreit, Quoc Le, and Slav Petrov. 2019. Natural questions: a benchmark for question answering research. Transactions of the Association of Computational Linguistics (TACL). Kenton Lee, Ming-Wei Chang, and Kristina Toutanova. 2019. Latent retrieval for weakly supervised open domain question answering. In Association for Computational Linguistics (ACL), pages 6086–6096.

**中文**

Tom Kwiatkowski、Jennimaria Palomaki、Olivia Redfield、Michael Collins、Ankur Parikh、Chris Alberti、Danielle Epstein、Illia Polosukhin、Matthew Kelcey、Jacob Devlin、Kenton Lee、Kristina N. Toutanova、Llion Jones、Ming-Wei Chang、Andrew Dai、Jakob Uszkoreit、Quoc Le 和 Slav Petrov。 2019.自然问题：问答研究的基准。计算语言学协会 (TACL) 汇刊。肯顿·李、张明伟和克里斯蒂娜·图塔诺娃。 2019.弱监督开放域问答的潜在检索。计算语言学协会 (ACL)，第 6086-6096 页。

### 段落 80 · Page 10

**EN**

Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Veselin Stoyanov, and Luke Zettlemoyer. 2020a. BART: Denoising sequence-to-sequence pretraining for natural language generation, translation, and comprehension. In Association for Computational Linguistics (ACL), pages 7871–7880. Patrick Lewis, Ethan Perez, Aleksandara Piktus, Fabio Petroni, Vladimir Karpukhin, Naman Goyal, Heinrich K ¨uttler, Mike Lewis, Wen-tau Yih, Tim Rockt ¨aschel, Sebastian Riedel, and Douwe Kiela. 2020b. Retrieval-augmented generation for knowledge-intensive NLP tasks.

**中文**

Mike Lewis、Yinhan Liu、Naman Goyal、Marjan Ghazvininejad、Abdelrahman Mohamed、Omer Levy、Veselin Stoyanov 和 Luke Zettlemoyer。 2020a. BART：用于自然语言生成、翻译和理解的去噪序列到序列预训练。计算语言学协会 (ACL)，第 7871–7880 页。帕特里克·刘易斯、伊桑·佩雷斯、亚历山大·皮克图斯、法比奥·彼得罗尼、弗拉基米尔·卡普欣、纳曼·戈亚尔、海因里希·库特勒、迈克·刘易斯、叶文涛、蒂姆·罗克特·阿舍尔、塞巴斯蒂安·里德尔和道威·基拉。 2020b.知识密集型 NLP 任务的检索增强生成。

### 段落 81 · Page 10

**EN**

In Advances in Neural Information Processing Systems (NeurIPS).

**中文**

神经信息处理系统 (NeurIPS) 的进展。

### Page 11

### 段落 82 · Page 11

**EN**

Yankai Lin, Haozhe Ji, Zhiyuan Liu, and Maosong Sun. 2018. Denoising distantly supervised open-domain question answering. In Association for Computational Linguistics (ACL), pages 1736–1745. Sewon Min, Danqi Chen, Hannaneh Hajishirzi, and Luke Zettlemoyer. 2019a. A discrete hard EM approach for weakly supervised question answering. In Empirical Methods in Natural Language Processing (EMNLP). Sewon Min, Danqi Chen, Luke Zettlemoyer, and Hannaneh Hajishirzi. 2019b. Knowledge guided text retrieval and reading for open domain question answering. ArXiv, abs/1911.03868. Dan Moldovan, Marius Pas ¸ca, Sanda Harabagiu, and Mihai Surdeanu. 2003.

**中文**

林彦凯，吉浩哲，刘志远，孙茂松。 2018. 去噪远程监督的开放域问答。计算语言学协会 (ACL)，第 1736-1745 页。 Sewon Min、Danqi Chen、Hannaneh Hajishirzi 和 Luke Zettlemoyer。 2019a.用于弱监督问答的离散硬 EM 方法。在自然语言处理（EMNLP）的经验方法中。 Sewon Min、Danqi Chen、Luke Zettlemoyer 和 Hannaneh Hajishirzi。 2019b.用于开放域问答的知识引导文本检索和阅读。 ArXiv，abs/1911.03868。 Dan Moldovan、Marius Pas¸ca、Sanda Harabagiu 和 Mihai Surdeanu。 2003年。

### 段落 83 · Page 11

**EN**

Performance issues and error analysis in an open-domain question answering system. ACM Transactions on Information Systems (TOIS), 21(2):133–154. Stephen Mussmann and Stefano Ermon. 2016. Learning and inference via maximum inner product search. In International Conference on Machine Learning (ICML), pages 2587–2596. Yixin Nie, Songhe Wang, and Mohit Bansal. 2019. Revealing the importance of semantic retrieval for machine reading at scale. In Empirical Methods in Natural Language Processing (EMNLP). Rodrigo Nogueira and Kyunghyun Cho. 2019. Passage re-ranking with BERT. ArXiv, abs/1901.04085.

**中文**

开放域问答系统中的性能问题和错误分析。 ACM 信息系统汇刊 (TOIS)，21(2)：133–154。斯蒂芬·穆斯曼和斯特凡诺·埃尔蒙。 2016.通过最大内积搜索进行学习和推理。国际机器学习会议 (ICML)，第 2587-2596 页。聂益欣、王松鹤、Mohit Bansal。 2019。揭示语义检索对于大规模机器阅读的重要性。在自然语言处理（EMNLP）的经验方法中。罗德里戈·诺盖拉和曹庆贤。 2019. 使用 BERT 进行段落重排。 ArXiv，abs/1901.04085。

### 段落 84 · Page 11

**EN**

Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, and Peter J Liu. 2019. Exploring the limits of transfer learning with a uniﬁed text-to-text transformer. ArXiv, abs/1910.10683. Pranav Rajpurkar, Jian Zhang, Konstantin Lopyrev, and Percy Liang. 2016. SQuAD: 100,000+ questions for machine comprehension of text. In Empirical Methods in Natural Language Processing (EMNLP), pages 2383–2392. Parikshit Ram and Alexander G Gray. 2012. Maximum inner-product search using cone trees.

**中文**

Colin Raffel、Noam Shazeer、Adam Roberts、Katherine Lee、Sharan Narang、Michael Matena、Yanqi Zhou、Wei Li 和 Peter J Liu。 2019。使用统一的文本到文本转换器探索迁移学习的局限性。 ArXiv，abs/1910.10683。 Pranav Rajpurkar、张健、康斯坦丁·洛佩列夫和珀西·梁。 2016. SQuAD：100,000 多个机器理解文本的问题。自然语言处理的经验方法 (EMNLP)，第 2383-2392 页。帕里克希特·拉姆 (Parikshit Ram) 和亚历山大·G·格雷 (Alexander G Gray)。 2012.使用圆锥树的最大内积搜索。

### 段落 85 · Page 11

**EN**

In Proceedings of the 18th ACM SIGKDD international conference on Knowledge discovery and data mining , pages 931–939. Adam Roberts, Colin Raffel, and Noam Shazeer. 2020. How much knowledge can you pack into the parameters of a language model? ArXiv, abs/2002.08910. Stephen Robertson and Hugo Zaragoza. 2009. The probabilistic relevance framework: BM25 and beyond. Foundations and Trends in Information Retrieval, 3(4):333–389. Minjoon Seo, Jinhyuk Lee, Tom Kwiatkowski, Ankur Parikh, Ali Farhadi, and Hannaneh Hajishirzi. 2019. Real-time open-domain question answering with dense-sparse phrase index.

**中文**

第 18 届 ACM SIGKDD 知识发现和数据挖掘国际会议记录，第 931-939 页。亚当·罗伯茨、科林·拉斐尔和诺姆·沙泽尔。 2020.你可以将多少知识装入语言模型的参数中？ ArXiv，abs/2002.08910。斯蒂芬·罗伯逊和雨果·萨拉戈萨。 2009。概率相关性框架：BM25 及以后。信息检索的基础和趋势，3(4)：333–389。 Minjoon Seo、Jinhyuk Lee、Tom Kwiatkowski、Ankur Parikh、Ali Farhadi 和 Hannaneh Hajishirzi。 2019.具有密集稀疏短语索引的实时开放域问答。

### 段落 86 · Page 11

**EN**

In Association for Computational Linguistics (ACL). Anshumali Shrivastava and Ping Li. 2014. Asymmetric LSH (ALSH) for sublinear time maximum inner product search (MIPS). In Advances in Neural Information Processing Systems (NIPS) , pages 2321– 2329. Ellen M V oorhees. 1999. The TREC-8 question answering track report. In TREC, volume 99, pages 77–82. Shuohang Wang, Mo Yu, Xiaoxiao Guo, Zhiguo Wang, Tim Klinger, Wei Zhang, Shiyu Chang, Gerry Tesauro, Bowen Zhou, and Jing Jiang. 2018. Rˆ3: Reinforced ranker-reader for open-domain question answering. In Conference on Artiﬁcial Intelligence (AAAI).

**中文**

在计算语言学协会（ACL）。 Anshumali Shrivastava 和李萍。 2014. 用于亚线性时间最大内积搜索 (MIPS) 的非对称 LSH (ALSH)。 《神经信息处理系统 (NIPS) 进展》，第 2321-2329 页。Ellen M V oorhees。 1999. TREC-8 问答跟踪报告。 TREC，第 99 卷，第 77-82 页。王硕航、于墨、郭晓晓、王志国、Tim Klinger、张伟、常世宇、Gerry Tesauro、周博文和蒋静。 2018.R^3：用于开放域问答的强化排序阅读器。在人工智能会议（AAAI）中。

### 段落 87 · Page 11

**EN**

Zhiguo Wang, Patrick Ng, Xiaofei Ma, Ramesh Nallapati, and Bing Xiang. 2019. Multi-passage BERT: A globally normalized bert model for open-domain question answering. In Empirical Methods in Natural Language Processing (EMNLP). Tomer Wolfson, Mor Geva, Ankit Gupta, Matt Gardner, Yoav Goldberg, Daniel Deutch, and Jonathan Berant. 2020. Break it down: A question understanding benchmark. Transactions of the Association of Computational Linguistics (TACL). Lee Xiong, Chenyan Xiong, Ye Li, Kwok-Fung Tang, Jialin Liu, Paul Bennett, Junaid Ahmed, and Arnold Overwijk. 2020a.

**中文**

王志国、吴帕特里克、马晓飞、拉梅什·纳拉帕蒂和项冰。 2019.多通道BERT：用于开放域问答的全局标准化BERT模型。在自然语言处理（EMNLP）的经验方法中。托默·沃尔夫森、莫尔·吉瓦、安基特·古普塔、马特·加德纳、约夫·戈德堡、丹尼尔·多伊奇和乔纳森·贝兰特。 2020。分解：问题理解基准。计算语言学协会 (TACL) 汇刊。 Lee Xiong、Chenyan Xiong、Ye Li、Kwok-Fung Tang、Jialin Liu、Paul Bennett、Junaid Ahmed 和 Arnold Overwijk。 2020a.

### 段落 88 · Page 11

**EN**

Approximate nearest neighbor negative contrastive learning for dense text retrieval. ArXiv, abs/2007.00808. Wenhan Xiong, Hankang Wang, and William Yang Wang. 2020b. Progressively pretrained dense corpus index for open-domain question answering. ArXiv, abs/2005.00038. Wei Yang, Yuqing Xie, Aileen Lin, Xingyu Li, Luchen Tan, Kun Xiong, Ming Li, and Jimmy Lin. 2019a. End-to-end open-domain question answering with bertserini. In North American Association for Computational Linguistics (NAACL), pages 72–77. Wei Yang, Yuqing Xie, Luchen Tan, Kun Xiong, Ming Li, and Jimmy Lin. 2019b.

**中文**

用于密集文本检索的近似最近邻负对比学习。 ArXiv，abs/2007.00808。熊文汉、王汉康、王威廉杨。 2020b.用于开放域问答的渐进式预训练密集语料库索引。 ArXiv，abs/2005.00038。杨伟、谢雨晴、林艾琳、李星宇、谭鲁辰、熊坤、李明和林吉米。 2019a.使用 bertserini 进行端到端开放域问答。北美计算语言学协会 (NAACL)，第 72-77 页。杨伟、谢雨晴、谭陆辰、熊坤、李明和林志颖。 2019b.

### 段落 89 · Page 11

**EN**

Data augmentation for bert ﬁne-tuning in open-domain question answering. ArXiv, abs/1904.06652. Wen-tau Yih, Kristina Toutanova, John C Platt, and Christopher Meek. 2011. Learning discriminative projections for text similarity measures. In Computational Natural Language Learning (CoNLL) , pages 247–256.

**中文**

用于开放域问答中 bert 微调的数据增强。 ArXiv，abs/1904.06652。叶文涛、克里斯蒂娜·图塔诺娃、约翰·C·普拉特和克里斯托弗·米克。 2011.学习文本相似性度量的判别性预测。计算自然语言学习 (CoNLL)，第 247-256 页。

### Page 12

### 段落 90 · Page 12

**EN**

A Distant Supervision When training our ﬁnal DPR model using Natural Questions, we use the passages in our collection that best match the gold context as the positive passages. As some QA datasets contain only the question and answer pairs, it is thus interesting to see when using the passages that contain the answers as positives (i.e., the distant supervision setting), whether there is a signiﬁcant performance degradation. Using the question and answer together as the query, we run Lucene-BM25 and pick the top passage that contains the answer as the positive passage.

**中文**

远程监督当使用自然问题训练我们的最终 DPR 模型时，我们使用集合中最符合黄金上下文的段落作为积极段落。由于一些 QA 数据集仅包含问题和答案对，因此，当使用包含答案的段落作为正例（即远程监督设置）时，观察是否存在显着的性能下降是很有趣的。使用问题和答案一起作为查询，我们运行 Lucene-BM25 并选择包含答案的顶部段落作为肯定段落。

### 段落 91 · Page 12

**EN**

Table 5 shows the performance of DPR when trained using the original setting and the distant supervision setting. B Alternative Similarity Functions & Triplet Loss In addition to dot product (DP) and negative loglikelihood based on softmax (NLL), we also experiment with Euclidean distance (L2) and the triplet loss. We negate L2 similarity scores before applying softmax and change signs of question-topositive and question-to-negative similarities when applying the triplet loss on dot product scores. The margin value of the triplet loss is set to 1. Table 6 summarizes the results.

**中文**

表 5 显示了使用原始设置和远程监督设置进行训练时 DPR 的性能。 B 替代相似函数和三元组损失 除了点积 (DP) 和基于 softmax (NLL) 的负对数似然之外，我们还尝试了欧氏距离 (L2) 和三元组损失。我们在应用 softmax 之前否定 L2 相似度分数，并在对点积分数应用三元组损失时将问题与正向和问题与负向相似度的符号更改。三元组损失的裕度值设置为 1。表 6 总结了结果。

### 段落 92 · Page 12

**EN**

All these additional experiments are conducted using the same hyperparameters tuned for the baseline (DP, NLL). Note that the retrieval accuracy for our “baseline” settings reported in Table 5 (Gold) and Table 6 (DP, NLL) is slightly better than those reported in Table 3. This is due to a better hyper-parameter setting used in these analysis experiments, which is documented in our code release. C Qualitative Analysis Although DPR performs better than BM25 in general, the retrieved passages of these two retrievers actually differ qualitatively.

**中文**

所有这些额外的实验都是使用针对基线（DP、NLL）调整的相同超参数进行的。请注意，表 5（Gold）和表 6（DP、NLL）中报告的“基线”设置的检索精度略好于表 3 中报告的结果。这是由于这些分析实验中使用了更好的超参数设置，这在我们的代码发布中进行了记录。 C 定性分析 虽然DPR 总体上表现优于BM25，但这两种检索器检索到的段落实际上在定性上有所不同。

### 段落 93 · Page 12

**EN**

Methods like BM25 are sensitive to highly selective keywords and phrases, but cannot capture lexical variations or semantic relationships well. In contrast, DPR excels at semantic representation, but might lack sufﬁcient capacity to represent salient phrases which appear rarely. Table 7 illustrates this phenomenon with two examples. In the ﬁrst example, the top scoring passage from BM25 is irrelevant, even though keywords such as England and Ireland appear multiple times. In comparison, DPR is able to return Top-1 Top-5 Top-20 Top-100 Gold 44.9 66.8 78.1 85.0 Dist. Sup.

**中文**

像 BM25 这样的方法对高度选择性的关键词和短语很敏感，但不能很好地捕获词汇变化或语义关系。相比之下，DPR 擅长语义表示，但可能缺乏足够的能力来表示很少出现的显着短语。表 7 通过两个例子说明了这一现象。在第一个示例中，BM25 中得分最高的段落是无关紧要的，即使诸如英格兰和爱尔兰之类的关键字出现多次。相比之下，DPR 能够返回 Top-1 Top-5 Top-20 Top-100 Gold 44.9 66.8 78.1 85.0 Dist。高级。

### 段落 94 · Page 12

**EN**

43.9 65.3 77.1 84.4 Table 5: Retrieval accuracy on the development set of Natural Questions, trained on passages that match the gold context (Gold) or the top BM25 passage that contains the answer (Dist. Sup.). Sim Loss Retrieval Accuracy Top-1 Top-5 Top-20 Top-100 DP NLL 44.9 66.8 78.1 85.0 Triplet 41.6 65.0 77.2 84.5 L2 NLL 43.5 64.7 76.1 83.1 Triplet 42.2 66.0 78.1 84.9 Table 6: Retrieval Top-k accuracy on the development set of Natural Questions using different similarity and loss functions. the correct answer, presumably by matching “body of water” with semantic neighbors such as sea and channel, even though no lexical overlap exists.

**中文**

43.9 65.3 77.1 84.4 表 5：自然问题开发集的检索准确性，在与黄金上下文 (Gold) 匹配的段落或包含答案的顶部 BM25 段落 (Dist. Sup.) 上进行训练。 Sim 损失检索精度 Top-1 Top-5 Top-20 Top-100 DP NLL 44.9 66.8 78.1 85.0 Triplet 41.6 65.0 77.2 84.5 L2 NLL 43.5 64.7 76.1 83.1 Triplet 42.2 66.0 78.1 84.9表 6：使用不同的相似度和损失函数对自然问题的开发集检索 Top-k 准确性。正确的答案，大概是通过将“水体”与诸如海和通道之类的语义邻居相匹配，即使不存在词汇重叠。

### 段落 95 · Page 12

**EN**

The second example is one where BM25 does better. The salient phrase “Thoros of Myr” is critical, and DPR is unable to capture it. D Joint Training of Retriever and Reader We ﬁx the passage encoder in our joint-training scheme while allowing only the question encoder to receive backpropagation signal from the combined (retriever + reader) loss function. This allows us to leverage the HNSW-based FAISS index for efﬁcient low-latency retrieving, without reindexing the passages during model updates.

**中文**

第二个例子是 BM25 做得更好的例子。显着的短语“Thoros of Myr”至关重要，DPR 无法捕捉到它。 D 检索器和阅读器的联合训练 我们在联合训练方案中修复了段落编码器，同时只允许问题编码器接收来自组合（检索器 + 阅读器）损失函数的反向传播信号。这使我们能够利用基于 HNSW 的 FAISS 索引进行高效的低延迟检索，而无需在模型更新期间重新索引段落。

### 段落 96 · Page 12

**EN**

Our loss function largely follows ORQA’s approach, which uses log probabilities of positive passages selected from the retriever model, and correct spans and passages selected from the reader model. Since the passage encoder is ﬁxed, we could use larger amount of retrieved passages when calculating the retriever loss. Speciﬁcally, we get top 100 passages for each question in a mini-batch and use the method similar to in-batch negative training: all retrieved passages’ vectors participate in the loss calculation for all questions in a batch.

**中文**

我们的损失函数很大程度上遵循 ORQA 的方法，该方法使用从检索器模型中选择的阳性段落的对数概率，以及从阅读器模型中选择的正确跨度和段落。由于段落编码器是固定的，因此在计算检索器损失时我们可以使用大量检索到的段落。具体来说，我们获取小批量中每个问题的前 100 个段落，并使用类似于批量负训练的方法：所有检索到的段落向量都参与批量中所有问题的损失计算。

### 段落 97 · Page 12

**EN**

Our training batch size is set to 16, which effectively gives 1,600 passages per question to calculate retriever loss. The reader still uses 24 passages per question, which are selected

**中文**

我们的训练批量大小设置为 16，这实际上为每个问题提供 1,600 段文章来计算检索器损失。读者仍然使用每个问题 24 个段落，这些段落是经过选择的

### Page 13

### 段落 98 · Page 13

**EN**

Question Passage received by BM25 Passage retrieved by DPR What is the body of water between England and Ireland? Title:British Cycling Title: Irish Sea . . .England is not recognised as a region by the UCI, and there is no English cycling team outside the Commonwealth Games. For those occasions, British Cycling selects and supports the England team. Cycling is represented on the Isle of Man by the Isle of Man Cycling Association. Cycling in Northern Ireland is organised under Cycling Ulster, part of the all-Ireland governing body Cycling Ireland. Until 2006, a rival governing body existed, . . . . . .

**中文**

问题 BM25 收到的通道 DPR 检索到的通道 英格兰和爱尔兰之间的水域是什么？标题：英国自行车赛 标题：爱尔兰海。。 .英格兰不被UCI承认为一个地区，在英联邦运动会之外也没有英国自行车队。在这些场合，英国自行车协会会选择并支持英格兰队。马恩岛自行车协会是马恩岛自行车运动的代表。北爱尔兰自行车运动由阿尔斯特自行车协会组织，该协会是全爱尔兰管理机构“爱尔兰自行车协会”的一部分。直到 2006 年，存在一个竞争性的管理机构，.。。。。。

### 段落 99 · Page 13

**EN**

Annual trafﬁc between Great Britain andIreland amounts to over 12 million passengers and of traded goods. The Irish Sea is connected to the North Atlantic at both its northern and southern ends. To the north, the connection is through the North Channel between Scotland and Northern Ireland and the Malin Sea. The southern end is linked to the Atlantic through the St George’s Channel between Ireland and Pembrokeshire, and the Celtic Sea. . . . Who plays Thoros of Myr in Game of Thrones? Title: No One (Game of Thrones) Title: P˚al Sverre Hagen . . .

**中文**

英国和爱尔兰之间的年客运量和贸易货物量超过 1200 万人次。爱尔兰海的南北两端与北大西洋相连。在北部，通过苏格兰和北爱尔兰之间的北海峡和马林海连接。南端通过爱尔兰和彭布罗克郡之间的圣乔治海峡以及凯尔特海与大西洋相连。。。。 《权力的游戏》中密尔的索罗斯是谁扮演的？标题：No One（权力的游戏） 标题：P?al Sverre Hagen。。。

### 段落 100 · Page 13

**EN**

He may be ”no one,” but there’s still enough of a person left in him to respect, and admire who this girl is and what she’s become. Arya ﬁnally tells us something that we’ve kind of known all along, that she’s not no one, she’s Arya Stark of Winterfell.” ”No One” saw the reintroduction of Richard Dormer and Paul Kaye, who portrayed Beric Dondarrion and Thoros of Myr, respectively, in the third season, . . . P˚al Sverre Valheim Hagen (born 6 November 1980) is a Norwegian stage and screen actor. He appeared in the Norwegian ﬁlm ”Max Manus” and played Thor Heyerdahl in the Oscar-nominated 2012 ﬁlm ”Kon-Tiki”.

**中文**

他可能“无名小卒”，但他身上仍然有足够的人来尊重和钦佩这个女孩是谁以及她变成了什么。艾莉亚终于告诉我们一些我们一直都知道的事情，那就是她不是任何人，她是临冬城的艾莉亚·史塔克。” 《无人》中理查德·多默和保罗·凯重新登场，他们在第三季中分别饰演贝里·唐德利恩和密尔的索罗斯。。。 P?al Sverre Valheim Hagen（1980 年 11 月 6 日出生）是一位挪威舞台和银幕演员。他出现在挪威电影《Max Manus》中，并在 2012 年奥斯卡提名电影《Kon-Tiki》中扮演托尔·海尔达尔 (Thor Heyerdahl)。

### 段落 101 · Page 13

**EN**

Pl Hagen was born in Stavanger, Norway, the son of Roar Hagen, a Norwegian cartoonist who has long been associated with Norway´s largest daily, ”VG”. He lived in Jtten, a neighborhood in the city of Stavanger in south-western Norway. . . . Table 7: Examples of passages returned from BM25 and DPR. Correct answers are written inblue and the content words in the question are written in bold. from the top 5 positive and top 30 negative passages (from the set of top 100 passages retrieved from the same question). The question encoder’s initial state is taken from a DPR model previously trained on the NQ dataset.

**中文**

普拉·哈根（Pl Hagen）出生于挪威斯塔万格，是挪威漫画家罗尔·哈根（Roar Hagen）的儿子，长期与挪威最大的日报“VG”有联系。他住在挪威西南部斯塔万格市的 Jtten 社区。。。。表 7：从 BM25 和 DPR 返回的段落示例。正确答案用蓝色写出，问题中的实词用粗体写出。来自前 5 个正面段落和前 30 个负面段落（从同一问题检索的前 100 个段落集中）。问题编码器的初始状态取自之前在 NQ 数据集上训练的 DPR 模型。

### 段落 102 · Page 13

**EN**

The reader’s initial state is a BERT-base model. In terms of the end-to-end QA results, our joint-training scheme does not provide better results compared to the usual retriever/reader training pipeline, resulting in the same 39.8 exact match score on NQ dev as in our regular reader model training.

**中文**

读者的初始状态是基于 BERT 的模型。就端到端 QA 结果而言，与通常的检索器/阅读器训练流程相比，我们的联合训练方案并未提供更好的结果，导致 NQ dev 上的精确匹配分数与我们的常规阅读器模型训练中相同，为 39.8。
