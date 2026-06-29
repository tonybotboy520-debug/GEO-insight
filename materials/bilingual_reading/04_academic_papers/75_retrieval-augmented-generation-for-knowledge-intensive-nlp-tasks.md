# Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks

- ID: 75
- 类型: pdf
- 分类: 04_academic_papers
- 主题: foundational RAG paper
- 原文链接: https://arxiv.org/pdf/2005.11401
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks Patrick Lewis†‡, Ethan Perez⋆, Aleksandra Piktus†, Fabio Petroni†, Vladimir Karpukhin†, Naman Goyal†, Heinrich Küttler†, Mike Lewis†, Wen-tau Yih†, Tim Rocktäschel†‡, Sebastian Riedel†‡, Douwe Kiela† †Facebook AI Research;‡University College London;⋆New York University; plewis@fb.com Abstract Large pre-trained language models have been shown to store factual knowledge in their parameters, and achieve state-of-the-art results when ﬁne-tuned on downstream NLP tasks.

**中文**

知识密集型 NLP 任务的检索增强生成 Patrick Lewis†‡、Ethan Perez⋆、Aleksandra Piktus†、Fabio Petroni†、Vladimir Karpukhin†、Naman Goyal†、Heinrich Küttler†、Mike Lewis†、Wen-tau Yih†、Tim Rocktäschel†‡、Sebastian Riedel†‡、Douwe Kiela††Facebook AI 研究；‡大学学院伦敦；⋆纽约大学； plewis@fb.com 摘要 大型预训练语言模型已被证明可以在其参数中存储事实知识，并在下游 NLP 任务上进行微调时获得最先进的结果。

### 段落 2 · Page 1

**EN**

However, their ability to access and precisely manipulate knowledge is still limited, and hence on knowledge-intensive tasks, their performance lags behind task-speciﬁc architectures. Additionally, providing provenance for their decisions and updating their world knowledge remain open research problems. Pretrained models with a differentiable access mechanism to explicit non-parametric memory have so far been only investigated for extractive downstream tasks. We explore a general-purpose ﬁne-tuning recipe for retrieval-augmented generation (RAG) — models which combine pre-trained parametric and non-parametric memory for language generation.

**中文**

然而，它们访问和精确操作知识的能力仍然有限，因此在知识密集型任务上，它们的性能落后于特定于任务的架构。此外，为他们的决策提供依据并更新他们的世界知识仍然是悬而未决的研究问题。迄今为止，仅针对提取性下游任务研究了具有对显式非参数内存的可微访问机制的预训练模型。我们探索了一种用于检索增强生成（RAG）的通用微调方法，该模型结合了预先训练的参数和非参数记忆来生成语言。

### 段落 3 · Page 1

**EN**

We introduce RAG models where the parametric memory is a pre-trained seq2seq model and the non-parametric memory is a dense vector index of Wikipedia, accessed with a pre-trained neural retriever. We compare two RAG formulations, one which conditions on the same retrieved passages across the whole generated sequence, and another which can use different passages per token. We ﬁne-tune and evaluate our models on a wide range of knowledgeintensive NLP tasks and set the state of the art on three open domain QA tasks, outperforming parametric seq2seq models and task-speciﬁc retrieve-and-extract architectures.

**中文**

我们引入 RAG 模型，其中参数存储器是预训练的 seq2seq 模型，非参数存储器是维基百科的密集向量索引，可通过预训练的神经检索器访问。我们比较了两种 RAG 公式，一种以整个生成序列中相同的检索段落为条件，另一种可以为每个标记使用不同的段落。我们在广泛的知识密集型 NLP 任务上微调和评估我们的模型，并在三个开放域 QA 任务上设置最先进的技术，优于参数化 seq2seq 模型和特定于任务的检索和提取架构。

### 段落 4 · Page 1

**EN**

For language generation tasks, we ﬁnd that RAG models generate more speciﬁc, diverse and factual language than a state-of-the-art parametric-only seq2seq baseline. 1 Introduction Pre-trained neural language models have been shown to learn a substantial amount of in-depth knowledge from data [47]. They can do so without any access to an external memory, as a parameterized implicit knowledge base [51, 52]. While this development is exciting, such models do have downsides: They cannot easily expand or revise their memory, can’t straightforwardly provide insight into their predictions, and may produce “hallucinations” [ 38].

**中文**

对于语言生成任务，我们发现 RAG 模型比最先进的纯参数 seq2seq 基线生成更具体、更多样化和更真实的语言。 1 引言 预训练的神经语言模型已被证明可以从数据中学习大量深入的知识[47]。他们可以在不访问外部存储器的情况下做到这一点，作为参数化的隐式知识库 [51, 52]。虽然这种发展令人兴奋，但此类模型确实有缺点：它们无法轻松扩展或修改其记忆，无法直接提供对其预测的洞察，并且可能会产生“幻觉”[38]。

### 段落 5 · Page 1

**EN**

Hybrid models that combine parametric memory with non-parametric (i.e., retrieval-based) memories [20, 26, 48] can address some of these issues because knowledge can be directly revised and expanded, and accessed knowledge can be inspected and interpreted. REALM [ 20] and ORQA [ 31], two recently introduced models that combine masked language models [8] with a differentiable retriever, have shown promising results, arXiv:2005.11401v4 [cs.CL] 12 Apr 2021

**中文**

将参数记忆与非参数（即基于检索）记忆相结合的混合模型[20,26,48]可以解决其中一些问题，因为知识可以直接修改和扩展，并且可以检查和解释访问的知识。 REALM [20] 和 ORQA [31]，这两个最近引入的模型将屏蔽语言模型 [8] 与可微检索器相结合，已经显示出有希望的结果，arXiv:2005.11401v4 [cs.CL] 2021 年 4 月 12 日

### Page 2

### 段落 6 · Page 2

**EN**

The Divine Comedy (x) q Query Encoder q(x) MIPS pθ Generator pθ (Parametric) Marginalize This 14th century work is divided into 3 sections: "Inferno", "Purgatorio" & "Paradiso" (y) End-to-End Backprop through q and pθ Barack Obama was born in Hawaii.(x) Fact Veriﬁcation: Fact Query supports (y) Question Generation Fact Veriﬁcation: Label Generation Document Index Define "middle ear"(x) Question Answering: Question Query The middle ear includes the tympanic cavity and the three ossicles.

**中文**

神曲 (x) q 查询编码器 q(x) MIPS pθ 生成器 pθ（参数）边缘化 这部 14 世纪的作品分为 3 个部分：“地狱”、“炼狱”和“天堂” (y) 通过 q 和 pθ 进行端到端反向传播 Barack Obama 出生于夏威夷。(x) 事实验证：事实查询支持 (y) 问题生成 事实验证：标签生成文档索引 定义“中耳”(x) 问答：问题查询 中耳包括鼓室和三个小骨。

### 段落 7 · Page 2

**EN**

(y) Question Answering: Answer GenerationRetriever pη (Non-Parametric) z4 z3 z2 z1 d(z) Jeopardy Question Generation: Answer Query Figure 1: Overview of our approach. We combine a pre-trained retriever (Query Encoder + Document Index) with a pre-trained seq2seq model (Generator) and ﬁne-tune end-to-end. For queryx, we use Maximum Inner Product Search (MIPS) to ﬁnd the top-K documentszi. For ﬁnal predictiony, we treatz as a latent variable and marginalize over seq2seq predictions given different documents. but have only explored open-domain extractive question answering.

**中文**

(y) 问答：答案生成检索器 pη（非参数） z4 z3 z2 z1 d(z) 危险问题生成：答案查询 图 1：我们的方法概述。我们将预训练的检索器（查询编码器 + 文档索引）与预训练的 seq2seq 模型（生成器）相结合，并进行端到端微调。对于 queryx，我们使用最大内积搜索 (MIPS) 来查找前 K 个文档zi。对于最终的预测，我们将 z 视为潜在变量，并在给定不同文档的情况下边缘化 seq2seq 预测。但只探索了开放域提取问答。

### 段落 8 · Page 2

**EN**

Here, we bring hybrid parametric and non-parametric memory to the “workhorse of NLP,” i.e. sequence-to-sequence (seq2seq) models. We endow pre-trained, parametric-memory generation models with a non-parametric memory through a general-purpose ﬁne-tuning approach which we refer to as retrieval-augmented generation (RAG). We build RAG models where the parametric memory is a pre-trained seq2seq transformer, and the non-parametric memory is a dense vector index of Wikipedia, accessed with a pre-trained neural retriever. We combine these components in a probabilistic model trained end-to-end (Fig. 1).

**中文**

在这里，我们将混合参数和非参数记忆引入“NLP 的主力”，即序列到序列 (seq2seq) 模型。我们通过通用微调方法为预训练的参数记忆生成模型赋予非参数记忆，我们将其称为检索增强生成（RAG）。我们构建 RAG 模型，其中参数存储器是预先训练的 seq2seq 转换器，非参数存储器是维基百科的密集向量索引，可通过预先训练的神经检索器访问。我们将这些组件组合到一个端到端训练的概率模型中（图 1）。

### 段落 9 · Page 2

**EN**

The retriever (Dense Passage Retriever [26], henceforth DPR) provides latent documents conditioned on the input, and the seq2seq model (BART [32]) then conditions on these latent documents together with the input to generate the output. We marginalize the latent documents with a top-K approximation, either on a per-output basis (assuming the same document is responsible for all tokens) or a per-token basis (where different documents are responsible for different tokens). Like T5 [51] or BART, RAG can be ﬁne-tuned on any seq2seq task, whereby both the generator and retriever are jointly learned.

**中文**

检索器（Dense Passage Retriever [26]，下文称为 DPR）提供以输入为条件的潜在文档，然后 seq2seq 模型（BART [32]）以这些潜在文档和输入为条件来生成输出。我们使用 top-K 近似来边缘化潜在文档，无论是在每个输出的基础上（假设同一文档负责所有标记）还是在每个标记的基础上（其中不同的文档负责不同的标记）。与 T5 [51] 或 BART 一样，RAG 可以在任何 seq2seq 任务上进行微调，从而生成器和检索器都是共同学习的。

### 段落 10 · Page 2

**EN**

There has been extensive previous work proposing architectures to enrich systems with non-parametric memory which are trained from scratch for speciﬁc tasks, e.g. memory networks [ 64, 55], stackaugmented networks [25] and memory layers [ 30]. In contrast, we explore a setting where both parametric and non-parametric memory components are pre-trained and pre-loaded with extensive knowledge. Crucially, by using pre-trained access mechanisms, the ability to access knowledge is present without additional training.

**中文**

之前已经有大量的工作提出了用非参数内存来丰富系统的架构，这些系统是针对特定任务从头开始训练的，例如。内存网络 [64, 55]、堆栈增强网络 [25] 和内存层 [30]。相比之下，我们探索了一种参数和非参数记忆组件都经过预训练并预加载广泛知识的设置。至关重要的是，通过使用预先训练的访问机制，无需额外培训即可获得知识。

### 段落 11 · Page 2

**EN**

Our results highlight the beneﬁts of combining parametric and non-parametric memory with generation for knowledge-intensive tasks—tasks that humans could not reasonably be expected to perform without access to an external knowledge source. Our RAG models achieve state-of-the-art results on open Natural Questions [29], WebQuestions [3] and CuratedTrec [2] and strongly outperform recent approaches that use specialised pre-training objectives on TriviaQA [24]. Despite these being extractive tasks, we ﬁnd that unconstrained generation outperforms previous extractive approaches.

**中文**

我们的结果强调了将参数化和非参数化记忆与知识密集型任务的生成相结合的好处——如果不访问外部知识源，人类就无法合理地期望执行这些任务。我们的 RAG 模型在开放自然问题 [29]、WebQuestions [3] 和 CuratedTrec [2] 上取得了最先进的结果，并且远远优于最近在 TriviaQA [24] 上使用专门预训练目标的方法。尽管这些是提取任务，但我们发现无约束生成优于以前的提取方法。

### 段落 12 · Page 2

**EN**

For knowledge-intensive generation, we experiment with MS-MARCO [1] and Jeopardy question generation, and we ﬁnd that our models generate responses that are more factual, speciﬁc, and diverse than a BART baseline. For FEVER [56] fact veriﬁcation, we achieve results within 4.3% of state-of-the-art pipeline models which use strong retrieval supervision. Finally, we demonstrate that the non-parametric memory can be replaced to update the models’ knowledge as the world changes.1 2 Methods We explore RAG models, which use the input sequencex to retrieve text documentsz and use them as additional context when generating the target sequence y.

**中文**

对于知识密集型生成，我们尝试了 MS-MARCO [1] 和 Jeopardy 问题生成，我们发现我们的模型生成的响应比 BART 基线更加真实、具体和多样化。对于 FEVER [56] 事实验证，我们取得的结果与使用强检索监督的最先进管道模型的 4.3% 之内。最后，我们证明可以替换非参数存储器来随着世界的变化更新模型的知识。1 2 方法我们探索 RAG 模型，它使用输入序列 x 来检索文本文档 z 并在生成目标序列 y 时将它们用作附加上下文。

### 段落 13 · Page 2

**EN**

As shown in Figure 1, our models leverage two components: (i) a retriever pη(z|x) with parametersη that returns (top-K truncated) distributions over text passages given a queryx and (ii) a generatorpθ(yi|x,z,y 1:i−1) parametrized 1Code to run experiments with RAG has been open-sourced as part of the HuggingFace Transformers Library [66] and can be found at https://github.com/huggingface/transformers/blob/master/ examples/rag/. An interactive demo of RAG models can be found at https://huggingface.co/rag/ 2

**中文**

如图 1 所示，我们的模型利用两个组件：(i) 带有参数 η 的检索器 pη(z|x)，它返回给定查询 x 的文本段落的（前 K 截断）分布；(ii) 生成器 pθ(yi|x,z,y 1:i−1) 参数化 1 用于使用 RAG 运行实验的代码已作为 HuggingFace Transformers Library [66] 的一部分开源，可以在以下位置找到： https://github.com/huggingface/transformers/blob/master/examples/rag/。 RAG 模型的交互式演示可在 https://huggingface.co/rag/ 2 找到

### Page 3

### 段落 14 · Page 3

**EN**

byθ that generates a current token based on a context of the previousi− 1 tokensy1:i−1, the original inputx and a retrieved passagez. To train the retriever and generator end-to-end, we treat the retrieved document as a latent variable. We propose two models that marginalize over the latent documents in different ways to produce a distribution over generated text. In one approach, RAG-Sequence, the model uses the same document to predict each target token. The second approach, RAG-Token, can predict each target token based on a different document.

**中文**

byθ 根据前一个 i−1 tokensy1:i−1、原始输入 x 和检索到的段落 z 的上下文生成当前标记。为了端到端地训练检索器和生成器，我们将检索到的文档视为潜在变量。我们提出了两种模型，以不同的方式边缘化潜在文档，以产生生成文本的分布。在一种方法（RAG-Sequence）中，模型使用相同的文档来预测每个目标标记。第二种方法，RAG-Token，可以根据不同的文档预测每个目标令牌。

### 段落 15 · Page 3

**EN**

In the following, we formally introduce both models and then describe the pη andpθ components, as well as the training and decoding procedure. 2.1 Models RAG-Sequence Model The RAG-Sequence model uses the same retrieved document to generate the complete sequence. Technically, it treats the retrieved document as a single latent variable that is marginalized to get the seq2seq probability p(y|x) via a top-K approximation.

**中文**

下面，我们正式介绍这两个模型，然后描述 pη 和 pθ 分量，以及训练和解码过程。 2.1 模型 RAG-序列模型 RAG-序列模型使用相同的检索文档来生成完整的序列。从技术上讲，它将检索到的文档视为单个潜在变量，该变量被边缘化以通过 top-K 近似获得 seq2seq 概率 p(y|x)。

### 段落 16 · Page 3

**EN**

Concretely, the top K documents are retrieved using the retriever, and the generator produces the output sequence probability for each document, which are then marginalized, pRAG-Sequence(y|x) ≈ ∑ z∈top-k(p(·|x)) pη(z|x)pθ(y|x,z ) = ∑ z∈top-k(p(·|x)) pη(z|x) N∏ i pθ(yi|x,z,y 1:i−1) RAG-Token Model In the RAG-Token model we can draw a different latent document for each target token and marginalize accordingly. This allows the generator to choose content from several documents when producing an answer.

**中文**

具体来说，使用检索器检索前 K 个文档，生成器生成每个文档的输出序列概率，然后将其边缘化， pRAG-Sequence(y|x) ≈ Σ zεtop-k(p(·|x)) pη(z|x)pθ(y|x,z ) = Σ zεtop-k(p(·|x)) pη(z|x) N∏ i pθ(yi|x,z,y 1:i−1) RAG-Token 模型 在 RAG-Token 模型中，我们可以为每个目标 token 绘制不同的潜在文档并相应地边缘化。这允许生成器在生成答案时从多个文档中选择内容。

### 段落 17 · Page 3

**EN**

Concretely, the top K documents are retrieved using the retriever, and then the generator produces a distribution for the next output token for each document, before marginalizing, and repeating the process with the following output token, Formally, we deﬁne: pRAG-Token(y|x) ≈ N∏ i ∑ z∈top-k(p(·|x)) pη(z|x)pθ(yi|x,z,y 1:i−1) Finally, we note that RAG can be used for sequence classiﬁcation tasks by considering the target class as a target sequence of length one, in which case RAG-Sequence and RAG-Token are equivalent. 2.2 Retriever: DPR The retrieval componentpη(z|x) is based on DPR [26].

**中文**

具体来说，使用检索器检索前 K 个文档，然后生成器为每个文档生成下一个输出标记的分布，然后进行边缘化，并使用以下输出标记重复该过程。 正式地，我们定义： pRAG-Token(y|x) ≈ N∏ i Σ z∈top-k(p(·|x)) pη(z|x)pθ(yi|x,z,y 1:i−1) 最后，我们注意到RAG 可用于序列分类任务，将目标类视为长度为 1 的目标序列，在这种情况下，RAG-Sequence 和 RAG-Token 是等效的。 2.2 检索器：DPR 检索分量pη(z|x) 基于DPR [26]。

### 段落 18 · Page 3

**EN**

DPR follows a bi-encoder architecture: pη(z|x)∝ exp ( d(z)⊤q(x) ) d(z) = BERTd(z), q(x) = BERTq(x) where d(z) is a dense representation of a document produced by a BERTBASE document encoder [8], and q(x) a query representation produced by a query encoder, also based on BERTBASE. Calculating top-k(pη(·|x)), the list ofk documentsz with highest prior probabilitypη(z|x), is a Maximum Inner Product Search (MIPS) problem, which can be approximately solved in sub-linear time [23]. We use a pre-trained bi-encoder from DPR to initialize our retriever and to build the document index.

**中文**

DPR 遵循双编码器架构：pη(z|x)∝ exp ( d(z)⊤q(x) ) d(z) = BERTd(z), q(x) = BERTq(x)，其中 d(z) 是 BERTBASE 文档编码器 [8] 生成的文档的密集表示，q(x) 是查询编码器生成的查询表示，也基于 BERTBASE。计算top-k(pη(·|x))，即具有最高先验概率pη(z|x)的k个文档z的列表，是一个最大内积搜索(MIPS)问题，可以在亚线性时间内近似解决[23]。我们使用 DPR 中的预训练双编码器来初始化检索器并构建文档索引。

### 段落 19 · Page 3

**EN**

This retriever was trained to retrieve documents which contain answers to TriviaQA [24] questions and Natural Questions [29]. We refer to the document index as the non-parametric memory. 2.3 Generator: BART The generator componentpθ(yi|x,z,y 1:i−1) could be modelled using any encoder-decoder. We use BART-large [32], a pre-trained seq2seq transformer [58] with 400M parameters. To combine the input x with the retrieved contentz when generating from BART, we simply concatenate them. BART was pre-trained using a denoising objective and a variety of different noising functions.

**中文**

该检索器经过训练，可以检索包含 TriviaQA [24] 问题和自然问题 [29] 答案的文档。我们将文档索引称为非参数存储器。 2.3 生成器：BART 生成器分量 pθ(yi|x,z,y 1:i−1) 可以使用任何编码器-解码器进行建模。我们使用 BART-large [32]，一个具有 400M 参数的预训练 seq2seq 转换器 [58]。为了在从 BART 生成时将输入 x 与检索到的内容 z 结合起来，我们只需将它们连接起来即可。 BART 使用降噪目标和各种不同的噪声函数进行了预训练。

### 段落 20 · Page 3

**EN**

It has obtained state-of-the-art results on a diverse set of generation tasks and outperforms comparably-sized T5 models [32]. We refer to the BART generator parametersθ as the parametric memory henceforth. 2.4 Training We jointly train the retriever and generator components without any direct supervision on what document should be retrieved. Given a ﬁne-tuning training corpus of input/output pairs(xj,yj), we 3

**中文**

它在多种生成任务上获得了最先进的结果，并且优于同等大小的 T5 模型 [32]。今后我们将 BART 发电机参数 θ 称为参数存储器。 2.4 培训 我们联合训练检索器和生成器组件，而无需直接监督应检索哪些文档。给定一个输入/输出对 (xj,yj) 的微调训练语料库，我们 3

### Page 4

### 段落 21 · Page 4

**EN**

minimize the negative marginal log-likelihood of each target,∑ j− logp(yj|xj) using stochastic gradient descent with Adam [28]. Updating the document encoder BERTd during training is costly as it requires the document index to be periodically updated as REALM does during pre-training [20]. We do not ﬁnd this step necessary for strong performance, and keep the document encoder (and index) ﬁxed, only ﬁne-tuning the query encoder BERTq and the BART generator. 2.5 Decoding At test time, RAG-Sequence and RAG-Token require different ways to approximatearg maxyp(y|x).

**中文**

Adam [28] 使用随机梯度下降来最小化每个目标的负边际对数似然，Σ j− logp(yj|xj)。在训练期间更新文档编码器 BERTd 的成本很高，因为它需要像 REALM 在预训练期间那样定期更新文档索引 [20]。我们认为这一步对于强大的性能来说不是必需的，并且保持文档编码器（和索引）固定，仅微调查询编码器 BERTq 和 BART 生成器。 2.5 解码 在测试时，RAG-Sequence 和 RAG-Token 需要不同的方式来近似 maxyp(y|x)。

### 段落 22 · Page 4

**EN**

RAG-Token The RAG-Token model can be seen as a standard, autoregressive seq2seq generator with transition probability: p′ θ(yi|x,y 1:i−1) = ∑ z∈top-k(p(·|x))pη(zi|x)pθ(yi|x,zi,y 1:i−1) To decode, we can plugp′ θ(yi|x,y 1:i−1) into a standard beam decoder. RAG-Sequence For RAG-Sequence, the likelihoodp(y|x) does not break into a conventional pertoken likelihood, hence we cannot solve it with a single beam search. Instead, we run beam search for each documentz, scoring each hypothesis usingpθ(yi|x,z,y 1:i−1). This yields a set of hypotheses Y , some of which may not have appeared in the beams of all documents.

**中文**

RAG-Token RAG-Token 模型可以被视为具有转移概率的标准自回归 seq2seq 生成器： p′ θ(yi|x,y 1:i−1) = Σ z∈top-k(p(·|x))pη(zi|x)pθ(yi|x,zi,y 1:i−1) 为了解码，我们可以将 p′ θ(yi|x,y 1:i−1) 插入标准束中解码器。 RAG-序列 对于 RAG-序列，似然性 p(y|x) 不会破坏传统的 pertoken 似然性，因此我们无法通过单波束搜索来解决它。相反，我们对每个文档 z 运行波束搜索，使用 pθ(yi|x,z,y 1:i−1) 对每个假设进行评分。这产生了一组假设 Y，其中一些假设可能没有出现在所有文档的光束中。

### 段落 23 · Page 4

**EN**

To estimate the probability of an hypothesis y we run an additional forward pass for each document z for which y does not appear in the beam, multiply generator probability withpη(z|x) and then sum the probabilities across beams for the marginals. We refer to this decoding procedure as “Thorough Decoding.” For longer output sequences,|Y| can become large, requiring many forward passes. For more efﬁcient decoding, we can make a further approximation thatpθ(y|x,zi)≈ 0 wherey was not generated during beam search fromx,zi. This avoids the need to run additional forward passes once the candidate set Y has been generated.

**中文**

为了估计假设 y 的概率，我们对 y 没有出现在光束中的每个文档 z 运行一次额外的前向传递，将生成器概率乘以 pη(z|x)，然后对边缘的跨光束概率求和。我们将此解码过程称为“彻底解码”。对于较长的输出序列，|Y|可能会变得很大，需要很多前向传球。为了更有效的解码，我们可以进一步近似 pθ(y|x,zi)≈ 0，其中 y 不是在从 x,zi 进行波束搜索期间生成的。这避免了在生成候选集 Y 后运行额外的前向传递的需要。

### 段落 24 · Page 4

**EN**

We refer to this decoding procedure as “Fast Decoding.” 3 Experiments We experiment with RAG in a wide range of knowledge-intensive tasks. For all experiments, we use a single Wikipedia dump for our non-parametric knowledge source. Following Lee et al. [31] and Karpukhin et al. [26], we use the December 2018 dump. Each Wikipedia article is split into disjoint 100-word chunks, to make a total of 21M documents. We use the document encoder to compute an embedding for each document, and build a single MIPS index using FAISS [23] with a Hierarchical Navigable Small World approximation for fast retrieval [37].

**中文**

我们将此解码过程称为“快速解码”。 3 实验 我们在广泛的知识密集型任务中使用 RAG 进行实验。对于所有实验，我们使用单个维基百科转储作为我们的非参数知识源。继李等人之后。 [31] 和卡普欣等人。 [26]，我们使用 2018 年 12 月的转储。每篇维基百科文章都被分割成不相交的 100 个单词的块，总共形成 2100 万个文档。我们使用文档编码器来计算每个文档的嵌入，并使用 FAISS [23] 和分层可导航小世界近似来构建单个 MIPS 索引，以实现快速检索 [37]。

### 段落 25 · Page 4

**EN**

During training, we retrieve the top k documents for each query. We considerk∈{ 5, 10} for training and setk for test time using dev data. We now discuss experimental details for each task. 3.1 Open-domain Question Answering Open-domain question answering (QA) is an important real-world application and common testbed for knowledge-intensive tasks [20]. We treat questions and answers as input-output text pairs (x,y ) and train RAG by directly minimizing the negative log-likelihood of answers.

**中文**

在训练期间，我们检索每个查询的前 k 个文档。我们考虑使用开发数据进行训练和测试时间 k ∈ { 5, 10}。我们现在讨论每项任务的实验细节。 3.1 开放域问答 开放域问答（QA）是知识密集型任务的重要现实应用和通用测试平台[20]。我们将问题和答案视为输入输出文本对 (x,y)，并通过直接最小化答案的负对数似然来训练 RAG。

### 段落 26 · Page 4

**EN**

We compare RAG to the popular extractive QA paradigm [5, 7, 31, 26], where answers are extracted spans from retrieved documents, relying primarily on non-parametric knowledge. We also compare to “Closed-Book QA” approaches [52], which, like RAG, generate answers, but which do not exploit retrieval, instead relying purely on parametric knowledge. We consider four popular open-domain QA datasets: Natural Questions (NQ) [29], TriviaQA (TQA) [24]. WebQuestions (WQ) [3] and CuratedTrec (CT) [2]. As CT and WQ are small, we follow DPR [26] by initializing CT and WQ models with our NQ RAG model.

**中文**

我们将 RAG 与流行的提取式 QA 范式进行比较 [5,7,31,26]，其中答案是从检索到的文档中提取的，主要依赖于非参数知识。我们还与“闭卷 QA”方法 [52] 进行比较，该方法与 RAG 一样，生成答案，但不利用检索，而是纯粹依赖参数知识。我们考虑四种流行的开放域 QA 数据集：Natural Questions (NQ) [29]、TriviaQA (TQA) [24]。 WebQuestions (WQ) [3] 和 CuratedTrec (CT) [2]。由于 CT 和 WQ 很小，我们遵循 DPR [26]，用我们的 NQ RAG 模型初始化 CT 和 WQ 模型。

### 段落 27 · Page 4

**EN**

We use the same train/dev/test splits as prior work [ 31, 26] and report Exact Match (EM) scores. For TQA, to compare with T5 [52], we also evaluate on the TQA Wiki test set. 3.2 Abstractive Question Answering RAG models can go beyond simple extractive QA and answer questions with free-form, abstractive text generation. To test RAG’s natural language generation (NLG) in a knowledge-intensive setting, we use the MSMARCO NLG task v2.1 [ 43]. The task consists of questions, ten gold passages retrieved from a search engine for each question, and a full sentence answer annotated from the retrieved passages.

**中文**

我们使用与之前的工作相同的训练/开发/测试分割[31, 26]并报告精确匹配（EM）分数。对于 TQA，为了与 T5 [52] 进行比较，我们还在 TQA Wiki 测试集上进行评估。 3.2 抽象问答 RAG 模型可以超越简单的提取式 QA，并通过自由形式的抽象文本生成来回答问题。为了在知识密集型环境中测试 RAG 的自然语言生成 (NLG)，我们使用 MSMARCO NLG 任务 v2.1 [43]。该任务包括问题、从搜索引擎中为每个问题检索的十个黄金段落，以及从检索到的段落中注释的完整句子答案。

### 段落 28 · Page 4

**EN**

We do not use the supplied passages, only the questions and answers, to treat 4

**中文**

我们不使用提供的段落，仅使用问题和答案来处理 4

### Page 5

### 段落 29 · Page 5

**EN**

MSMARCO as an open-domain abstractive QA task. MSMARCO has some questions that cannot be answered in a way that matches the reference answer without access to the gold passages, such as “What is the weather in V olcano, CA?” so performance will be lower without using gold passages. We also note that some MSMARCO questions cannot be answered using Wikipedia alone. Here, RAG can rely on parametric knowledge to generate reasonable responses. 3.3 Jeopardy Question Generation To evaluate RAG’s generation abilities in a non-QA setting, we study open-domain question generation.

**中文**

MSMARCO 作为开放域抽象 QA 任务。 MSMARCO 有一些问题，如果不访问黄金段落，就无法以与参考答案相匹配的方式来回答，例如“加利福尼亚州火山的天气如何？”因此，如果不使用黄金通道，性能会较低。我们还注意到，一些 MSMARCO 问题无法仅使用维基百科来回答。在这里，RAG 可以依靠参数知识来生成合理的响应。 3.3 危险问题生成 为了评估 RAG 在非 QA 环境中的生成能力，我们研究了开放域问题生成。

### 段落 30 · Page 5

**EN**

Rather than use questions from standard open-domain QA tasks, which typically consist of short, simple questions, we propose the more demanding task of generating Jeopardy questions. Jeopardy is an unusual format that consists of trying to guess an entity from a fact about that entity. For example, “The World Cup” is the answer to the question “In 1986 Mexico scored as the ﬁrst country to host this international sports competition twice.” As Jeopardy questions are precise, factual statements, generating Jeopardy questions conditioned on their answer entities constitutes a challenging knowledge-intensive generation task.

**中文**

我们不使用标准开放域 QA 任务中的问题（通常由简短的问题组成），而是提出要求更高的任务，即生成 Jeopardy 问题。 Jeopardy 是一种不寻常的格式，它包括尝试根据有关实体的事实来猜测该实体。例如，“世界杯”是对“1986 年墨西哥作为第一个两次主办这项国际体育赛事的国家”这一问题的答案。由于 Jeopardy 问题是精确的事实陈述，因此根据其答案实体生成 Jeopardy 问题构成了一项具有挑战性的知识密集型生成任务。

### 段落 31 · Page 5

**EN**

We use the splits from SearchQA [ 10], with 100K train, 14K dev, and 27K test examples. As this is a new task, we train a BART model for comparison. Following [67], we evaluate using the SQuAD-tuned Q-BLEU-1 metric [ 42]. Q-BLEU is a variant of BLEU with a higher weight for matching entities and has higher correlation with human judgment for question generation than standard metrics. We also perform two human evaluations, one to assess generation factuality, and one for speciﬁcity.

**中文**

我们使用 SearchQA [10] 中的拆分，其中包含 100K 训练样本、14K 开发样本和 27K 测试样本。由于这是一项新任务，我们训练了一个 BART 模型进行比较。继[67]之后，我们使用 SQuAD 调整的 Q-BLEU-1 指标进行评估[42]。 Q-BLEU 是 BLEU 的变体，与标准指标相比，具有更高的匹配实体权重，并且与人类对问题生成的判断具有更高的相关性。我们还进行了两项人工评估，一项是为了评估生成的真实性，另一项是为了评估具体性。

### 段落 32 · Page 5

**EN**

We deﬁne factuality as whether a statement can be corroborated by trusted external sources, and speciﬁcity as high mutual dependence between the input and output [33]. We follow best practice and use pairwise comparative evaluation [34]. Evaluators are shown an answer and two generated questions, one from BART and one from RAG. They are then asked to pick one of four options—quuestion A is better, question B is better, both are good, or neither is good. 3.4 Fact Veriﬁcation FEVER [ 56] requires classifying whether a natural language claim is supported or refuted by Wikipedia, or whether there is not enough information to decide.

**中文**

我们将事实性定义为是否可以通过可信的外部来源证实陈述，并将特异性定义为输入和输出之间的高度相互依赖[33]。我们遵循最佳实践并使用成对比较评估[34]。评估人员会看到一个答案和两个生成的问题，一个来自 BART，一个来自 RAG。然后，他们被要求从四个选项中选择一个——问题 A 更好，问题 B 更好，两者都好，或者都不好。 3.4 事实验证 FEVER [56] 需要对维基百科是否支持或反驳自然语言主张进行分类，或者是否没有足够的信息来决定。

### 段落 33 · Page 5

**EN**

The task requires retrieving evidence from Wikipedia relating to the claim and then reasoning over this evidence to classify whether the claim is true, false, or unveriﬁable from Wikipedia alone. FEVER is a retrieval problem coupled with an challenging entailment reasoning task. It also provides an appropriate testbed for exploring the RAG models’ ability to handle classiﬁcation rather than generation. We map FEVER class labels (supports, refutes, or not enough info) to single output tokens and directly train with claim-class pairs. Crucially, unlike most other approaches to FEVER, we do not use supervision on retrieved evidence.

**中文**

该任务需要从维基百科检索与该主张相关的证据，然后对该证据进行推理，以对该主张是否正确、错误或仅从维基百科无法验证进行分类。 FEVER 是一个检索问题，同时也是一项具有挑战性的蕴涵推理任务。它还提供了一个适当的测试平台，用于探索 RAG 模型处理分类而不是生成的能力。我们将 FEVER 类标签（支持、反驳或信息不足）映射到单个输出标记，并直接使用声明类对进行训练。至关重要的是，与大多数其他发烧方法不同，我们不对检索到的证据进行监督。

### 段落 34 · Page 5

**EN**

In many real-world applications, retrieval supervision signals aren’t available, and models that do not require such supervision will be applicable to a wider range of tasks. We explore two variants: the standard 3-way classiﬁcation task (supports/refutes/not enough info) and the 2-way (supports/refutes) task studied in Thorne and Vlachos [57]. In both cases we report label accuracy. 4 Results 4.1 Open-domain Question Answering Table 1 shows results for RAG along with state-of-the-art models. On all four open-domain QA tasks, RAG sets a new state of the art (only on the T5-comparable split for TQA).

**中文**

在许多现实应用中，检索监督信号不可用，不需要这种监督的模型将适用于更广泛的任务。我们探索了两种变体：标准的 3 路分类任务（支持/反驳/信息不足）和 Thorne 和 Vlachos [57] 研究的 2 路（支持/反驳）任务。在这两种情况下，我们都会报告标签准确性。 4 结果 4.1 开放域问答 表 1 显示了 RAG 的结果以及最先进的模型。在所有四个开放域 QA 任务中，RAG 都设定了新的技术水平（仅在 TQA 的 T5 相当的分割上）。

### 段落 35 · Page 5

**EN**

RAG combines the generation ﬂexibility of the “closed-book” (parametric only) approaches and the performance of "open-book" retrieval-based approaches. Unlike REALM and T5+SSM, RAG enjoys strong results without expensive, specialized “salient span masking” pre-training [ 20]. It is worth noting that RAG’s retriever is initialized using DPR’s retriever, which uses retrieval supervision on Natural Questions and TriviaQA. RAG compares favourably to the DPR QA system, which uses a BERT-based “crossencoder” to re-rank documents, along with an extractive reader.

**中文**

RAG 结合了“闭卷”（仅参数）方法的生成灵活性和“开卷”基于检索的方法的性能。与 REALM 和 T5+SSM 不同，RAG 无需昂贵的专门“显着跨度掩蔽”预训练即可获得出色的结果 [20]。值得注意的是，RAG 的检索器是使用 DPR 的检索器初始化的，该检索器使用对 Natural Questions 和 TriviaQA 的检索监督。 RAG 与 DPR QA 系统相比具有优势，后者使用基于 BERT 的“交叉编码器”以及提取式阅读器对文档进行重新排序。

### 段落 36 · Page 5

**EN**

RAG demonstrates that neither a re-ranker nor extractive reader is necessary for state-of-the-art performance. There are several advantages to generating answers even when it is possible to extract them. Documents with clues about the answer but do not contain the answer verbatim can still contribute towards a correct answer being generated, which is not possible with standard extractive approaches, leading 5

**中文**

RAG 表明，对于最先进的性能来说，重新排序器和提取读取器都不是必需的。即使可以提取答案，生成答案也有几个优点。包含有关答案的线索但不逐字包含答案的文档仍然有助于生成正确的答案，而这对于标准提取方法来说是不可能的，导致 5

### Page 6

### 段落 37 · Page 6

**EN**

Table 1: Open-Domain QA Test Scores. For TQA, left column uses the standard test set for Open- Domain QA, right column uses the TQA-Wiki test set. See Appendix D for further details. Model NQ TQA WQ CT Closed Book T5-11B [52] 34.5 - /50.1 37.4 - T5-11B+SSM[52] 36.6 - /60.5 44.7 - Open Book REALM [20] 40.4 - / - 40.7 46.8 DPR [26] 41.5 57.9/ - 41.1 50.6 RAG-Token 44.1 55.2/66.1 45.5 50.0 RAG-Seq. 44.5 56.8/68.0 45.2 52.2 Table 2: Generation and classiﬁcation Test Scores. MS-MARCO SotA is [4], FEVER-3 is [68] and FEVER-2 is [ 57] *Uses gold context/evidence. Best model without gold access underlined.

**中文**

表 1：开放域 QA 测试分数。对于 TQA，左列使用开放域 QA 的标准测试集，右列使用 TQA-Wiki 测试集。详细信息请参见附录 D。型号 NQ TQA WQ CT 闭卷 T5-11B [52] 34.5 - /50.1 37.4 - T5-11B+SSM[52] 36.6 - /60.5 44.7 - 开卷 REALM [20] 40.4 - / - 40.7 46.8 DPR [26] 41.5 57.9/ - 41.1 50.6 RAG 代币 44.1 55.2/66.1 45.5 50.0 RAG 序列44.5 56.8/68.0 45.2 52.2 表 2：生成和分类测试分数。 MS-MARCO SotA 是 [4]，FEVER-3 是 [68]，FEVER-2 是 [57] *使用黄金背景/证据。没有黄金通道的最佳型号下划线。

### 段落 38 · Page 6

**EN**

Model Jeopardy MSMARCO FVR3 FVR2 B-1 QB-1 R-L B-1 Label Acc. SotA - - 49.8* 49.9* 76.8 92.2 * BART 15.1 19.7 38.2 41.6 64.0 81.1 RAG-Tok. 17.3 22.2 40.1 41.5 72.5 89.5RAG-Seq. 14.7 21.4 40.8 44.2 to more effective marginalization over documents. Furthermore, RAG can generate correct answers even when the correct answer is not in any retrieved document, achieving 11.8% accuracy in such cases for NQ, where an extractive model would score 0%. 4.2 Abstractive Question Answering As shown in Table 2, RAG-Sequence outperforms BART on Open MS-MARCO NLG by 2.6 Bleu points and 2.6 Rouge-L points.

**中文**

型号 Jeopardy MSMARCO FVR3 FVR2 B-1 QB-1 R-L B-1 标签 Acc. SotA - - 49.8* 49.9* 76.8 92.2 * BART 15.1 19.7 38.2 41.6 64.0 81.1 RAG-Tok。 17.3 22.2 40.1 41.5 72.5 89.5RAG 序列14.7 21.4 40.8 44.2 更有效地边缘化文件。此外，即使正确答案不在任何检索到的文档中，RAG 也可以生成正确答案，在这种情况下，NQ 的准确率达到 11.8%，而提取模型的得分为 0%。 4.2 抽象问答 如表 2 所示，RAG-Sequence 在 Open MS-MARCO NLG 上的性能优于 BART 2.6 个 Bleu 点和 2.6 个 Rouge-L 点。

### 段落 39 · Page 6

**EN**

RAG approaches state-of-the-art model performance, which is impressive given that (i) those models access gold passages with speciﬁc information required to generate the reference answer , (ii) many questions are unanswerable without the gold passages, and (iii) not all questions are answerable from Wikipedia alone. Table 3 shows some generated answers from our models. Qualitatively, we ﬁnd that RAG models hallucinate less and generate factually correct text more often than BART. Later, we also show that RAG generations are more diverse than BART generations (see §4.5).

**中文**

RAG 接近最先进的模型性能，这是令人印象深刻的，因为 (i) 这些模型访问带有生成参考答案所需的特定信息的黄金段落，(ii) 如果没有黄金段落，许多问题是无法回答的，(iii) 并非所有问题都可以仅从维基百科来回答。表 3 显示了我们的模型生成的一些答案。定性地讲，我们发现 RAG 模型比 BART 模型产生的幻觉更少，并且更频繁地生成事实上正确的文本。后来，我们还表明 RAG 世代比 BART 世代更加多样化（参见第 4.5 节）。

### 段落 40 · Page 6

**EN**

4.3 Jeopardy Question Generation Table 2 shows that RAG-Token performs better than RAG-Sequence on Jeopardy question generation, with both models outperforming BART on Q-BLEU-1. 4 shows human evaluation results, over 452 pairs of generations from BART and RAG-Token. Evaluators indicated that BART was more factual than RAG in only 7.1% of cases, while RAG was more factual in 42.7% of cases, and both RAG and BART were factual in a further 17% of cases, clearly demonstrating the effectiveness of RAG on the task over a state-of-the-art generation model. Evaluators also ﬁnd RAG generations to be more speciﬁc by a large margin.

**中文**

4.3 Jeopardy 问题生成 表 2 显示，RAG-Token 在 Jeopardy 问题生成上的表现优于 RAG-Sequence，两种模型在 Q-BLEU-1 上的表现均优于 BART。图 4 显示了 BART 和 RAG-Token 超过 452 对代的人类评估结果。评估人员表示，BART 仅在 7.1% 的情况下比 RAG 更真实，而 RAG 在 42.7% 的情况下更真实，RAG 和 BART 在另外 17% 的情况下都更真实，这清楚地证明了 RAG 相对于最先进的生成模型在任务上的有效性。评估人员还发现 RAG 世代更加具体。

### 段落 41 · Page 6

**EN**

Table 3 shows typical generations from each model. Jeopardy questions often contain two separate pieces of information, and RAG-Token may perform best because it can generate responses that combine content from several documents. Figure 2 shows an example. When generating “Sun”, the posterior is high for document 2 which mentions “The Sun Also Rises”. Similarly, document 1 dominates the posterior when “A Farewell to Arms” is generated. Intriguingly, after the ﬁrst token of each book is generated, the document posterior ﬂattens. This observation suggests that the generator can complete the titles without depending on speciﬁc documents.

**中文**

表 3 显示了每个型号的典型世代。 Jeopardy 问题通常包含两条独立的信息，而 RAG-Token 可能表现最佳，因为它可以生成结合多个文档内容的响应。图 2 显示了一个示例。当生成“Sun”时，文档 2 提到“太阳照常升起”的后验较高。类似地，当生成“永别了，武器”时，文档 1 主导后验。有趣的是，在生成每本书的第一个标记后，文档后验会变平。这一观察结果表明生成器可以在不依赖于特定文档的情况下完成标题。

### 段落 42 · Page 6

**EN**

In other words, the model’s parametric knowledge is sufﬁcient to complete the titles. We ﬁnd evidence for this hypothesis by feeding the BART-only baseline with the partial decoding"The Sun. BART completes the generation "The Sun Also Rises" is a novel by this author of "The Sun Also Rises" indicating the title "The Sun Also Rises" is stored in BART’s parameters. Similarly, BART will complete the partial decoding "The Sun Also Rises" is a novel by this author of "A with "The Sun Also Rises" is a novel by this author of "A Farewell to Arms".

**中文**

换句话说，模型的参数知识足以完成标题。我们通过向 BART-only 基线提供部分解码《太阳》来找到这一假设的证据。BART 完成生成《太阳照常升起》是《太阳照常升起》作者的一部小说，表明标题《太阳照常升起》存储在 BART 的参数中。同样，BART 将完成部分解码《太阳照常升起》是《太阳照常升起》作者的一部小说。武器”。

### 段落 43 · Page 6

**EN**

This example shows how parametric and non-parametric memories work together—the non-parametric component helps to guide the generation, drawing out speciﬁc knowledge stored in the parametric memory. 4.4 Fact Veriﬁcation Table 2 shows our results on FEVER. For 3-way classiﬁcation, RAG scores are within 4.3% of state-of-the-art models, which are complex pipeline systems with domain-speciﬁc architectures and substantial engineering, trained using intermediate retrieval supervision, which RAG does not require. 6

**中文**

这个例子展示了参数化和非参数化存储器如何协同工作——非参数化组件有助于指导生成，提取存储在参数化存储器中的特定知识。 4.4 事实验证 表 2 显示了我们对 FEVER 的结果。对于三向分类，RAG 分数与最先进模型的误差在 4.3% 以内，这些模型是具有特定领域架构和大量工程的复杂管道系统，使用中间检索监督进行训练，而 RAG 不需要。 6

### Page 7

### 段落 44 · Page 7

**EN**

Document 1: his works are considered classics of American literature ... His wartime experiences formed the basis for his novel ”A Farewell to Arms” (1929) ... Document 2: ... artists of the 1920s ”Lost Generation” expatriate community . His debut novel, ”The Sun Also Rises” , was published in 1926. BOS ” TheSunAlso R ises ” is a novel by this author of ” A Farewellto Arms ” Doc 1 Doc 2 Doc 3 Doc 4 Doc 5 Figure 2: RAG-Token document posteriorp(zi|x,yi,y−i) for each generated token for input “Hemingway" for Jeopardy generation with 5 retrieved documents.

**中文**

文件1：他的作品被认为是美国文学的经典……他的战时经历构成了他的小说《永别了，武器》（1929）的基础……文件2：……1920年代“迷惘的一代”侨民群体的艺术家。他的处女作《太阳照常升起》于 1926 年出版。 BOS “TheSunAlso Rises” 是《告别武器》作者的小说 Doc 1 Doc 2 Doc 3 Doc 4 Doc 5 图 2：RAG-Token 文档后验 p(zi|x,yi,y−i) 对于每个生成的令牌，用于输入“Hemingway”，危险生成为 5检索到的文档。

### 段落 45 · Page 7

**EN**

The posterior for document 1 is high when generating “A Farewell to Arms" and for document 2 when generating “The Sun Also Rises". Table 3: Examples from generation tasks. RAG models generate more speciﬁc and factually accurate responses. ‘?’ indicates factually incorrect responses, * indicates partially correct responses. Task Input Model Generation MS- MARCO deﬁne middle ear BART ?The middle ear is the part of the ear between the middle ear and the nose. RAG-T The middle ear is the portion of the ear internal to the eardrum. RAG-S The middle ear includes the tympanic cavity and the three ossicles.

**中文**

当生成“永别了，武器”时，文档 1 的后验较高，而当生成“太阳照常升起”时，文档 2 的后验较高。表 3：生成任务的示例。 RAG 模型生成更具体、更准确的响应。 ‘?’ 表示实际上不正确的响应，* 表示部分正确的响应。任务输入模型生成 MS-MARCO 定义中耳 BART？中耳是耳朵中位于中耳和鼻子之间的部分。 RAG-T 中耳是耳朵内部鼓膜的部分。 RAG-S 中耳包括鼓室和三个小骨。

### 段落 46 · Page 7

**EN**

what currency needed in scotland BART The currency needed in Scotland is Pound sterling. RAG-T Pound is the currency needed in Scotland. RAG-S The currency needed in Scotland is the pound sterling. Jeopardy Question Gener -ation Washington BART ?This state has the largest number of counties in the U.S. RAG-T It’s the only U.S. state named for a U.S.

**中文**

苏格兰 需要什么货币 BART 苏格兰 需要的货币是 英镑。 RAG-T 英镑是苏格兰所需的货币。 RAG-S 苏格兰所需的货币是英镑。危险问题生成 华盛顿 BART？该州拥有美国最多的县 RAG-T 它是美国唯一以美国命名的州

### 段落 47 · Page 7

**EN**

president RAG-S It’s the state where you’ll ﬁnd Mount Rainier National Park The Divine Comedy BART *This epic poem by Dante is divided into 3 parts: the Inferno, the Purgatorio & the Purgatorio RAG-T Dante’s "Inferno" is the ﬁrst part of this epic poem RAG-S This 14th century work is divided into 3 sections: "Inferno", "Purgatorio" & "Paradiso" For 2-way classiﬁcation, we compare against Thorne and Vlachos [57], who train RoBERTa [35] to classify the claim as true or false given the gold evidence sentence. RAG achieves an accuracy within 2.7% of this model, despite being supplied with only the claim and retrieving its own evidence.

**中文**

总统 RAG-S 雷尼尔山国家公园所在的州 神曲 BART *但丁的这部史诗分为 3 部分：《地狱》、《炼狱》和《炼狱》 RAG-T 但丁的《地狱》是这部史诗的第一部分 RAG-S 这部 14 世纪的作品分为 3 个部分：《地狱》、《炼狱》和“Paradiso” 对于 2 路分类，我们与 Thorne 和 Vlachos [57] 进行比较，他们训练 RoBERTa [35] 在给出黄金证据句子的情况下将主张分类为真或假。尽管仅提供了声明并检索了自己的证据，但 RAG 的准确度在该模型的 2.7% 以内。

### 段落 48 · Page 7

**EN**

We also analyze whether documents retrieved by RAG correspond to documents annotated as gold evidence in FEVER. We calculate the overlap in article titles between the topk documents retrieved by RAG and gold evidence annotations. We ﬁnd that the top retrieved document is from a gold article in 71% of cases, and a gold article is present in the top 10 retrieved articles in 90% of cases. 4.5 Additional Results Generation Diversity Section 4.3 shows that RAG models are more factual and speciﬁc than BART for Jeopardy question generation.

**中文**

我们还分析了 RAG 检索到的文档是否对应于 FEVER 中注释为黄金证据的文档。我们计算 RAG 检索到的 topk 文档与黄金证据注释之间文章标题的重叠度。我们发现，在 71% 的情况下，检索最多的文档来自黄金文章，而在 90% 的情况下，前 10 条检索到的文章中都出现了黄金文章。 4.5 附加结果生成多样性 第 4.3 节表明，对于 Jeopardy 问题生成，RAG 模型比 BART 更真实、更具体。

### 段落 49 · Page 7

**EN**

Following recent work on diversity-promoting decoding [33, 59, 39], we also investigate generation diversity by calculating the ratio of distinct ngrams to total ngrams generated by different models. Table 5 shows that RAG-Sequence’s generations are more diverse than RAG-Token’s, and both are signiﬁcantly more diverse than BART without needing any diversity-promoting decoding. Retrieval Ablations A key feature of RAG is learning to retrieve relevant information for the task. To assess the effectiveness of the retrieval mechanism, we run ablations where we freeze the retriever during training.

**中文**

继最近关于多样性促进解码的工作[33,59,39]之后，我们还通过计算不同模型生成的不同 ngram 与总 ngram 的比率来研究生成多样性。表 5 显示，RAG-Sequence 的世代比 RAG-Token 的世代更加多样化，并且两者都比 BART 更加多样化，而不需要任何促进多样性的解码。检索消融 RAG 的一个关键特征是学习检索任务的相关信息。为了评估检索机制的有效性，我们在训练期间冻结检索器来进行消融。

### 段落 50 · Page 7

**EN**

As shown in Table 6, learned retrieval improves results for all tasks. We compare RAG’s dense retriever to a word overlap-based BM25 retriever [53]. Here, we replace RAG’s retriever with a ﬁxed BM25 system, and use BM25 retrieval scores as logits when calculating p(z|x). Table 6 shows the results. For FEVER, BM25 performs best, perhaps since FEVER claims are heavily entity-centric and thus well-suited for word overlap-based retrieval. Differentiable retrieval improves results on all other tasks, especially for Open-Domain QA, where it is crucial.

**中文**

如表 6 所示，学习检索改进了所有任务的结果。我们将 RAG 的密集检索器与基于单词重叠的 BM25 检索器进行比较 [53]。在这里，我们用固定的 BM25 系统替换 RAG 的检索器，并在计算 p(z|x) 时使用 BM25 检索分数作为 logits。结果如表6所示。对于 FEVER，BM25 表现最好，也许是因为 FEVER 声明很大程度上以实体为中心，因此非常适合基于单词重叠的检索。可微分检索可以改善所有其他任务的结果，特别是对于开放域 QA 而言，这一点至关重要。

### 段落 51 · Page 7

**EN**

Index hot-swapping An advantage of non-parametric memory models like RAG is that knowledge can be easily updated at test time. Parametric-only models like T5 or BART need further training to update their behavior as the world changes. To demonstrate, we build an index using the DrQA [5] Wikipedia dump from December 2016 and compare outputs from RAG using this index to the newer index from our main results (December 2018). We prepare a list of 82 world leaders who had changed 7

**中文**

索引热交换 RAG 等非参数内存模型的一个优点是可以在测试时轻松更新知识。 T5 或 BART 等纯参数模型需要进一步训练，以便随着世界的变化更新其行为。为了进行演示，我们使用 2016 年 12 月的 DrQA [5] 维基百科转储构建了一个索引，并将使用该索引的 RAG 的输出与我们主要结果（2018 年 12 月）的新索引进行比较。我们准备了一份 82 位世界领导人的名单，他们更换了 7 位领导人

### Page 8

### 段落 52 · Page 8

**EN**

Table 4: Human assessments for the Jeopardy Question Generation Task. Factuality Speciﬁcity BART better 7.1% 16.8% RAG better 42.7% 37.4% Both good 11.7% 11.8% Both poor 17.7% 6.9% No majority 20.8% 20.1% Table 5: Ratio of distinct to total tri-grams for generation tasks. MSMARCO Jeopardy QGen Gold 89.6% 90.0% BART 70.7% 32.4% RAG-Token 77.8% 46.8% RAG-Seq. 83.5% 53.8% Table 6: Ablations on the dev set. As FEVER is a classiﬁcation task, both RAG models are equivalent.

**中文**

表 4：危险问题生成任务的人类评估。事实特异性 BART 更好 7.1% 16.8% RAG 更好 42.7% 37.4% 都好 11.7% 11.8% 都差 17.7% 6.9% 没有多数 20.8% 20.1% 表 5：生成任务中不同三元组与总三元组的比率。 MSMARCO Jeopardy QGen Gold 89.6% 90.0% BART 70.7% 32.4% RAG-Token 77.8% 46.8% RAG-Seq。 83.5% 53.8% 表 6：开发集上的消融。由于 FEVER 是一项分类任务，因此两个 RAG 模型是等效的。

### 段落 53 · Page 8

**EN**

Model NQ TQA WQ CT Jeopardy-QGen MSMarco FVR-3 FVR-2 Exact Match B-1 QB-1 R-L B-1 Label Accuracy RAG-Token-BM25 29.7 41.5 32.1 33.1 17.5 22.3 55.5 48.4 75.1 91.6RAG-Sequence-BM25 31.8 44.1 36.6 33.8 11.1 19.5 56.5 46.9 RAG-Token-Frozen 37.8 50.1 37.1 51.1 16.7 21.7 55.9 49.4 72.9 89.4RAG-Sequence-Frozen 41.2 52.1 41.8 52.6 11.8 19.6 56.7 47.3 RAG-Token 43.5 54.8 46.5 51.9 17.9 22.6 56.2 49.4 74.5 90.6RAG-Sequence 44.0 55.8 44.9 53.4 15.3 21.5 57.2 47.5 between these dates and use a template “Who is {position}?” (e.g. “Who is the President of Peru?”) to query our NQ RAG model with each index.

**中文**

型号 NQ TQA WQ CT Jeopardy-QGen MSMarco FVR-3 FVR-2 精确匹配 B-1 QB-1 R-L B-1 标签精度 RAG-Token-BM25 29.7 41.5 32.1 33.1 17.5 22.3 55.5 48.4 75.1 91.6RAG-Sequence-BM25 31.8 44.1 36.6 33.8 11.1 19.5 56.5 46.9 RAG 令牌冻结 37.8 50.1 37.1 51.1 16.7 21.7 55.9 49.4 72.9 89.4RAG 序列冻结 41.2 52.1 41.8 52.6 11.8 19.6 56.7 47.3 RAG 代币 43.5 54.8 46.5 51.9 17.9 22.6 56.2 49.4 74.5 90.6RAG 序列 44.0 55.8 44.9 53.4 15.3 21.5 57.2 47.5 在这些日期之间并使用模板“谁是 {position}？” （例如“谁是秘鲁总统？”）使用每个索引查询我们的 NQ RAG 模型。

### 段落 54 · Page 8

**EN**

RAG answers 70% correctly using the 2016 index for 2016 world leaders and 68% using the 2018 index for 2018 world leaders. Accuracy with mismatched indices is low (12% with the 2018 index and 2016 leaders, 4% with the 2016 index and 2018 leaders). This shows we can update RAG’s world knowledge by simply replacing its non-parametric memory. Effect of Retrieving more documents Models are trained with either 5 or 10 retrieved latent documents, and we do not observe signiﬁcant differences in performance between them. We have the ﬂexibility to adjust the number of retrieved documents at test time, which can affect performance and runtime.

**中文**

RAG 使用 2016 年世界领导人指数的 2016 年指数回答正确率为 70%，使用 2018 年世界领导人指数的 2018 年指数回答正确率为 68%。不匹配指数的准确性较低（2018 年指数和 2016 年领先者为 12%，2016 年指数和 2018 年领先者为 4%）。这表明我们可以通过简单地替换 RAG 的非参数内存来更新 RAG 的世界知识。检索更多文档的效果模型使用 5 或 10 个检索到的潜在文档进行训练，我们没有观察到它们之间的性能存在显着差异。我们可以灵活地调整测试时检索的文档数量，这可能会影响性能和运行时间。

### 段落 55 · Page 8

**EN**

Figure 3 (left) shows that retrieving more documents at test time monotonically improves Open-domain QA results for RAG-Sequence, but performance peaks for RAG-Token at 10 retrieved documents. Figure 3 (right) shows that retrieving more documents leads to higher Rouge-L for RAG-Token at the expense of Bleu-1, but the effect is less pronounced for RAG-Sequence.

**中文**

图 3（左）显示，在测试时检索更多文档会单调改善 RAG-Sequence 的开放域 QA 结果，但 RAG-Token 在检索 10 个文档时性能达到峰值。图 3（右）显示，检索更多文档会导致 RAG-Token 的 Rouge-L 更高，但会牺牲 Bleu-1，但对于 RAG-Sequence 的影响不太明显。

### 段落 56 · Page 8

**EN**

10 20 30 40 50 KR e t r i e v e dD o c s 39 40 41 42 43 44NQ Exact Match RAG-Tok RAG-Seq 10 20 30 40 50 KR e t r i e v e dD o c s 40 50 60 70 80NQ Answer Recall @ K RAG-Tok RAG-Seq Fixed DPR BM25 10 20 30 40 50 KR e t r i e v e dD o c s 48 50 52 54 56Bleu-1 / Rouge-L score RAG-Tok R-L RAG-Tok B-1 RAG-Seq R-L RAG-Seq B-1 Figure 3: Left: NQ performance as more documents are retrieved. Center: Retrieval recall performance in NQ. Right: MS-MARCO Bleu-1 and Rouge-L as more documents are retrieved.

**中文**

10 20 30 40 50 KR etrieve dDoc s 39 40 41 42 43 44NQ 精确匹配 RAG-Tok RAG-Seq 10 20 30 40 50 KR etrieve dDoc s 40 50 60 70 80NQ 答案召回@ K RAG-Tok RAG-Seq 固定 DPR BM25 10 20 30 40 50 KR e t r i e v e dD o c s 48 50 52 54 56Bleu-1 / Rouge-L 分数 RAG-Tok R-L RAG-Tok B-1 RAG-Seq R-L RAG-Seq B-1 图 3：左：NQ 性能为检索到更多文档。中：NQ 中的检索召回性能。右图：检索到更多文档时的 MS-MARCO Bleu-1 和 Rouge-L。

### 段落 57 · Page 8

**EN**

5 Related Work Single-Task Retrieval Prior work has shown that retrieval improves performance across a variety of NLP tasks when considered in isolation. Such tasks include open-domain question answering [5, 29], fact checking [ 56], fact completion [ 48], long-form question answering [ 12], Wikipedia article generation [36], dialogue [ 41, 65, 9, 13], translation [ 17], and language modeling [ 19, 27]. Our work uniﬁes previous successes in incorporating retrieval into individual tasks, showing that a single retrieval-based architecture is capable of achieving strong performance across several tasks. 8

**中文**

5 相关工作 单任务检索 先前的工作表明，单独考虑时，检索可以提高各种 NLP 任务的性能。这些任务包括开放域问答[5, 29]、事实检查[56]、事实补全[48]、长式问答[12]、维基百科文章生成[36]、对话[41,65,9,13]、翻译[17]和语言建模[19,27]。我们的工作结合了之前将检索合并到各个任务中的成功，表明单一基于检索的架构能够在多个任务中实现强大的性能。 8

### Page 9

### 段落 58 · Page 9

**EN**

General-Purpose Architectures for NLP Prior work on general-purpose architectures for NLP tasks has shown great success without the use of retrieval. A single, pre-trained language model has been shown to achieve strong performance on various classiﬁcation tasks in the GLUE benchmarks [60, 61] after ﬁne-tuning [49, 8]. GPT-2 [50] later showed that a single, left-to-right, pre-trained language model could achieve strong performance across both discriminative and generative tasks.

**中文**

NLP 的通用架构 之前针对 NLP 任务的通用架构的工作在不使用检索的情况下已经取得了巨大的成功。经过微调 [49, 8] 后，单一的预训练语言模型已被证明可以在 GLUE 基准测试 [60, 61] 中的各种分类任务中实现出色的性能。 GPT-2 [50] 后来表明，单一的、从左到右、预训练的语言模型可以在判别性和生成性任务中取得出色的性能。

### 段落 59 · Page 9

**EN**

For further improvement, BART [32] and T5 [51, 52] propose a single, pre-trained encoder-decoder model that leverages bi-directional attention to achieve stronger performance on discriminative and generative tasks. Our work aims to expand the space of possible tasks with a single, uniﬁed architecture, by learning a retrieval module to augment pre-trained, generative language models. Learned Retrieval There is signiﬁcant work on learning to retrieve documents in information retrieval, more recently with pre-trained, neural language models [ 44, 26] similar to ours.

**中文**

为了进一步改进，BART [32] 和 T5 [51, 52] 提出了一个单一的、预训练的编码器-解码器模型，该模型利用双向注意力在判别和生成任务上实现更强的性能。我们的工作旨在通过学习检索模块来增强预先训练的生成语言模型，以单一、统一的架构扩展可能的任务空间。学习检索 在信息检索中学习检索文档方面开展了大量工作，最近使用了与我们类似的预训练神经语言模型 [44, 26]。

### 段落 60 · Page 9

**EN**

Some work optimizes the retrieval module to aid in a speciﬁc, downstream task such as question answering, using search [46], reinforcement learning [6, 63, 62], or a latent variable approach [31, 20] as in our work. These successes leverage different retrieval-based architectures and optimization techniques to achieve strong performance on a single task, while we show that a single retrieval-based architecture can be ﬁne-tuned for strong performance on a variety of tasks. Memory-based Architectures Our document index can be seen as a large external memory for neural networks to attend to, analogous to memory networks [64, 55].

**中文**

一些工作优化了检索模块，以帮助完成特定的下游任务，例如使用搜索 [46]、强化学习 [6, 63, 62] 或潜在变量方法 [31, 20] 来回答问题，就像我们的工作一样。这些成功利用不同的基于检索的架构和优化技术来在单个任务上实现强大的性能，同时我们表明，可以对单个基于检索的架构进行微调，以在各种任务上实现强大的性能。基于内存的架构我们的文档索引可以被视为供神经网络处理的大型外部存储器，类似于内存网络[64, 55]。

### 段落 61 · Page 9

**EN**

Concurrent work [14] learns to retrieve a trained embedding for each entity in the input, rather than to retrieve raw text as in our work. Other work improves the ability of dialog models to generate factual text by attending over fact embeddings [15, 13]. A key feature of our memory is that it is comprised of raw text rather distributed representations, which makes the memory both (i) human-readable, lending a form of interpretability to our model, and (ii) human-writable, enabling us to dynamically update the model’s memory by editing the document index.

**中文**

并发工作 [14] 学习为输入中的每个实体检索经过训练的嵌入，而不是像我们的工作中那样检索原始文本。其他工作通过关注事实嵌入来提高对话模型生成事实文本的能力 [15, 13]。我们的记忆的一个关键特征是它由原始文本而不是分布式表示组成，这使得记忆既（i）人类可读，为我们的模型提供了一种可解释性，（ii）人类可写，使我们能够通过编辑文档索引来动态更新模型的记忆。

### 段落 62 · Page 9

**EN**

This approach has also been used in knowledge-intensive dialog, where generators have been conditioned on retrieved text directly, albeit obtained via TF-IDF rather than end-to-end learnt retrieval [9]. Retrieve-and-Edit approaches Our method shares some similarities with retrieve-and-edit style approaches, where a similar training input-output pair is retrieved for a given input, and then edited to provide a ﬁnal output. These approaches have proved successful in a number of domains including Machine Translation [ 18, 22] and Semantic Parsing [21].

**中文**

这种方法也被用于知识密集型对话，其中生成器直接以检索到的文本为条件，尽管是通过 TF-IDF 而不是端到端学习检索获得的 [9]。检索和编辑方法我们的方法与检索和编辑风格的方法有一些相似之处，其中针对给定的输入检索类似的训练输入输出对，然后进行编辑以提供最终输出。这些方法已在包括机器翻译 [18, 22] 和语义解析 [21] 在内的许多领域取得了成功。

### 段落 63 · Page 9

**EN**

Our approach does have several differences, including less of emphasis on lightly editing a retrieved item, but on aggregating content from several pieces of retrieved content, as well as learning latent retrieval, and retrieving evidence documents rather than related training pairs. This said, RAG techniques may work well in these settings, and could represent promising future work. 6 Discussion In this work, we presented hybrid generation models with access to parametric and non-parametric memory. We showed that our RAG models obtain state of the art results on open-domain QA.

**中文**

我们的方法确实有几个区别，包括不太强调对检索到的项目进行轻微编辑，而是强调从多个检索到的内容中聚合内容，以及学习潜在检索和检索证据文档而不是相关的训练对。也就是说，RAG 技术可能在这些环境中表现良好，并且可能代表着有前途的未来工作。 6 讨论 在这项工作中，我们提出了可以访问参数和非参数内存的混合生成模型。我们展示了我们的 RAG 模型在开放域 QA 上获得了最先进的结果。

### 段落 64 · Page 9

**EN**

We found that people prefer RAG’s generation over purely parametric BART, ﬁnding RAG more factual and speciﬁc. We conducted an thorough investigation of the learned retrieval component, validating its effectiveness, and we illustrated how the retrieval index can be hot-swapped to update the model without requiring any retraining. In future work, it may be fruitful to investigate if the two components can be jointly pre-trained from scratch, either with a denoising objective similar to BART or some another objective.

**中文**

我们发现人们更喜欢 RAG 的生成而不是纯参数化的 BART，发现 RAG 更真实、更具体。我们对学习的检索组件进行了彻底的调查，验证了其有效性，并说明了如何热插拔检索索引以更新模型，而无需任何重新训练。在未来的工作中，研究这两个组件是否可以从头开始联合预训练，无论是使用类似于 BART 的去噪目标还是其他目标，可能会富有成果。

### 段落 65 · Page 9

**EN**

Our work opens up new research directions on how parametric and non-parametric memories interact and how to most effectively combine them, showing promise in being applied to a wide variety of NLP tasks. 9

**中文**

我们的工作开辟了关于参数和非参数记忆如何相互作用以及如何最有效地将它们结合起来的新研究方向，显示出应用于各种 NLP 任务的前景。 9

### Page 10

### 段落 66 · Page 10

**EN**

Broader Impact This work offers several positive societal beneﬁts over previous work: the fact that it is more strongly grounded in real factual knowledge (in this case Wikipedia) makes it “hallucinate” less with generations that are more factual, and offers more control and interpretability. RAG could be employed in a wide variety of scenarios with direct beneﬁt to society, for example by endowing it with a medical index and asking it open-domain questions on that topic, or by helping people be more effective at their jobs.

**中文**

更广泛的影响 与之前的工作相比，这项工作提供了一些积极的社会效益：事实上，它更牢固地基于真实的事实知识（在本例中是维基百科），这使得它对更真实的几代人产生的“幻觉”更少，并提供更多的控制和可解释性。 RAG 可以应用于多种对社会有直接好处的场景，例如赋予它医疗指数并询问有关该主题的开放领域问题，或者帮助人们提高工作效率。

### 段落 67 · Page 10

**EN**

With these advantages also come potential downsides: Wikipedia, or any potential external knowledge source, will probably never be entirely factual and completely devoid of bias. Since RAG can be employed as a language model, similar concerns as for GPT-2 [50] are valid here, although arguably to a lesser extent, including that it might be used to generate abuse, faked or misleading content in the news or on social media; to impersonate others; or to automate the production of spam/phishing content [54]. Advanced language models may also lead to the automation of various jobs in the coming decades [16].

**中文**

这些优点也带来了潜在的缺点：维基百科或任何潜在的外部知识源可能永远不会完全真实且完全没有偏见。由于 RAG 可以用作语言模型，因此与 GPT-2 [50] 类似的担忧在这里也是有效的，尽管可以说程度较小，包括它可能被用来在新闻或社交媒体上生成滥用、伪造或误导性内容；冒充他人；或自动生成垃圾邮件/网络钓鱼内容 [54]。先进的语言模型还可能导致未来几十年各种工作的自动化[16]。

### 段落 68 · Page 10

**EN**

In order to mitigate these risks, AI systems could be employed to ﬁght against misleading content and automated spam/phishing. Acknowledgments The authors would like to thank the reviewers for their thoughtful and constructive feedback on this paper, as well as HuggingFace for their help in open-sourcing code to run RAG models. The authors would also like to thank Kyunghyun Cho and Sewon Min for productive discussions and advice. EP thanks supports from the NSF Graduate Research Fellowship. PL is supported by the FAIR PhD program.

**中文**

为了减轻这些风险，可以采用人工智能系统来对抗误导性内容和自动垃圾邮件/网络钓鱼。致谢 作者要感谢审稿人对本文提出的深思熟虑和建设性的反馈，以及 HuggingFace 在运行 RAG 模型的开源代码方面提供的帮助。作者还要感谢 Kyunghyun Cho 和 Sewon Min 富有成效的讨论和建议。 EP 感谢 NSF 研究生研究奖学金的支持。 PL 得到 FAIR 博士项目的支持。

### 段落 69 · Page 10

**EN**

References [1] Payal Bajaj, Daniel Campos, Nick Craswell, Li Deng, Jianfeng Gao, Xiaodong Liu, Rangan Majumder, Andrew McNamara, Bhaskar Mitra, Tri Nguyen, Mir Rosenberg, Xia Song, Alina Stoica, Saurabh Tiwary, and Tong Wang. MS MARCO: A Human Generated MAchine Reading COmprehension Dataset. arXiv:1611.09268 [cs], November 2016. URL http: //arxiv.org/abs/1611.09268. arXiv: 1611.09268. [2] Petr Baudiš and Jan Šediv`y. Modeling of the question answering task in the yodaqa system. In International Conference of the Cross-Language Evaluation Forum for European Languages, pages 222–228. Springer, 2015.

**中文**

参考文献 [1] Payal Bajaj、Daniel Campos、Nick Craswell、Li Deng、Jianfeng Gang、Xiaodong Liu、Rangan Majumder、Andrew McNamara、Bhaskar Mitra、Tri Nguyen、Mir Rosenberg、Xia Song、Alina Stoica、Saurabh Tiwary 和 Tong Wang。 MS MARCO：人类生成的机器阅读理解数据集。 arXiv:1611.09268 [cs]，2016 年 11 月。URL http://arxiv.org/abs/1611.09268。 arXiv：1611.09268。 [2] Petr Baudiš 和 Jan Šediv`y。 yodaqa 系统中问答任务的建模。欧洲语言跨语言评估论坛国际会议，第 222-228 页。施普林格，2015。

### 段落 70 · Page 10

**EN**

URL https://link.springer.com/chapter/10.1007% 2F978-3-319-24027-5_20 . [3] Jonathan Berant, Andrew Chou, Roy Frostig, and Percy Liang. Semantic Parsing on Freebase from Question-Answer Pairs. In Proceedings of the 2013 Conference on Empirical Methods in Natural Language Processing, pages 1533–1544, Seattle, Washington, USA, October 2013. Association for Computational Linguistics. URL http://www.aclweb.org/anthology/ D13-1160. [4] Bin Bi, Chenliang Li, Chen Wu, Ming Yan, and Wei Wang. Palm: Pre-training an autoencoding&autoregressive language model for context-conditioned generation. ArXiv, abs/2004.07159, 2020.

**中文**

网址 https://link.springer.com/chapter/10.1007% 2F978-3-319-24027-5_20。 [3] 乔纳森·贝兰特、安德鲁·周、罗伊·弗罗斯蒂格和珀西·梁。 Freebase 上问答对的语义解析。 2013 年自然语言处理经验方法会议论文集，第 1533-1544 页，美国华盛顿州西雅图，2013 年 10 月。计算语言学协会。网址 http://www.aclweb.org/anthology/D13-1160。 [4] 毕斌，李陈亮，吴晨，严明，王伟。 Palm：预训练用于上下文条件生成的自编码和自回归语言模型。 ArXiv，abs/2004.07159，2020。

### 段落 71 · Page 10

**EN**

URL https://arxiv.org/abs/2004.07159. [5] Danqi Chen, Adam Fisch, Jason Weston, and Antoine Bordes. Reading Wikipedia to Answer Open-Domain Questions. In Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pages 1870–1879, Vancouver, Canada, July 2017. Association for Computational Linguistics. doi: 10.18653/v1/P17-1171. URL https://www.aclweb.org/anthology/P17-1171. [6] Eunsol Choi, Daniel Hewlett, Jakob Uszkoreit, Illia Polosukhin, Alexandre Lacoste, and Jonathan Berant. Coarse-to-ﬁne question answering for long documents.

**中文**

网址 https://arxiv.org/abs/2004.07159。 [5] 陈丹琪、亚当·费什、杰森·韦斯顿和安托万·博德斯。阅读维基百科来回答开放领域问题。计算语言学协会第 55 届年会论文集（第一卷：长论文），第 1870-1879 页，加拿大温哥华，2017 年 7 月。计算语言学协会。 doi：10.18653/v1/P17-1171。网址 https://www.aclweb.org/anthology/P17-1171。 [6] Eunsol Choi、Daniel Hewlett、Jakob Uszkoreit、Illia Polosukhin、Alexandre Lacoste 和 Jonathan Berant。针对长文档从粗到细的问答。

### 段落 72 · Page 10

**EN**

In Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pages 209–220, Vancouver, Canada, July 2017. Association for Computational Linguistics. doi: 10.18653/v1/P17-1020. URL https://www.aclweb.org/anthology/P17-1020. 10

**中文**

计算语言学协会第 55 届年会论文集（第一卷：长论文），第 209-220 页，加拿大温哥华，2017 年 7 月。计算语言学协会。 doi：10.18653/v1/P17-1020。网址 https://www.aclweb.org/anthology/P17-1020。 10

### Page 11

### 段落 73 · Page 11

**EN**

[7] Christopher Clark and Matt Gardner. Simple and Effective Multi-Paragraph Reading Comprehension. arXiv:1710.10723 [cs], October 2017. URL http://arxiv.org/abs/1710.10723. arXiv: 1710.10723. [8] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. In Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long and Short Papers), pages 4171–4186, Minneapolis, Minnesota, June 2019. Association for Computational Linguistics. doi: 10.18653/v1/N19-1423.

**中文**

[7] 克里斯托弗·克拉克和马特·加德纳。简单有效的多段落阅读理解。 arXiv:1710.10723 [cs]，2017 年 10 月。URL http://arxiv.org/abs/1710.10723。 arXiv：1710.10723。 [8] Jacob Devlin、Ming-Wei Chang、Kenton Lee 和 Kristina Toutanova。 BERT：用于语言理解的深度双向Transformer的预训练。计算语言学协会北美分会 2019 年会议记录：人类语言技术，第 1 卷（长论文和短论文），第 4171-4186 页，明尼苏达州明尼阿波利斯，2019 年 6 月。计算语言学协会。 doi：10.18653/v1/N19-1423。

### 段落 74 · Page 11

**EN**

URL https://www.aclweb.org/anthology/N19-1423. [9] Emily Dinan, Stephen Roller, Kurt Shuster, Angela Fan, Michael Auli, and Jason Weston. Wizard of wikipedia: Knowledge-powered conversational agents. In International Conference on Learning Representations, 2019. URL https://openreview.net/forum?id=r1l73iRqKm. [10] Matthew Dunn, Levent Sagun, Mike Higgins, V . Ugur Guney, V olkan Cirik, and Kyunghyun Cho. SearchQA: A New Q&A Dataset Augmented with Context from a Search Engine. arXiv:1704.05179 [cs], April 2017. URL http://arxiv.org/abs/1704.05179. arXiv: 1704.05179. [11] Angela Fan, Mike Lewis, and Yann Dauphin.

**中文**

网址 https://www.aclweb.org/anthology/N19-1423。 [9] 艾米丽·迪南、史蒂芬·罗勒、库尔特·舒斯特、安吉拉·范、迈克尔·奥利和杰森·韦斯顿。维基百科向导：知识驱动的对话代理。国际学习表征会议，2019。URL https://openreview.net/forum?id=r1l73iRqKm。 [10] 马修·邓恩、莱文特·萨贡、迈克·希金斯、V。 Ugur Guney、Volkan Cirik 和 Kyunghyun Cho。 SearchQA：一个新的问答数据集，通过搜索引擎的上下文进行了增强。 arXiv:1704.05179 [cs]，2017 年 4 月。URL http://arxiv.org/abs/1704.05179。 arXiv：1704.05179。 [11] 安吉拉·范、迈克·刘易斯和扬·多芬。

### 段落 75 · Page 11

**EN**

Hierarchical neural story generation. In Proceedings of the 56th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pages 889–898, Melbourne, Australia, July 2018. Association for Computational Linguistics. doi: 10.18653/v1/P18-1082. URL https://www.aclweb.org/anthology/ P18-1082. [12] Angela Fan, Yacine Jernite, Ethan Perez, David Grangier, Jason Weston, and Michael Auli. ELI5: Long form question answering. In Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics, pages 3558–3567, Florence, Italy, July 2019. Association for Computational Linguistics.

**中文**

分层神经故事生成。计算语言学协会第 56 届年会论文集（第一卷：长论文），第 889-898 页，澳大利亚墨尔本，2018 年 7 月。计算语言学协会。 doi：10.18653/v1/P18-1082。网址 https://www.aclweb.org/anthology/P18-1082。 [12] Angela Fan、Yacine Jernite、Ethan Perez、David Grangier、Jason Weston 和 Michael Auli。 ELI5：长式问答。计算语言学协会第 57 届年会论文集，第 3558-3567 页，意大利佛罗伦萨，2019 年 7 月。计算语言学协会。

### 段落 76 · Page 11

**EN**

doi: 10.18653/v1/P19-1346. URL https://www.aclweb.org/ anthology/P19-1346. [13] Angela Fan, Claire Gardent, Chloe Braud, and Antoine Bordes. Augmenting transformers with KNN-based composite memory, 2020. URL https://openreview.net/forum?id= H1gx1CNKPH. [14] Thibault Févry, Livio Baldini Soares, Nicholas FitzGerald, Eunsol Choi, and Tom Kwiatkowski. Entities as experts: Sparse memory access with entity supervision. ArXiv, abs/2004.07202, 2020. URL https://arxiv.org/abs/2004.07202. [15] Marjan Ghazvininejad, Chris Brockett, Ming-Wei Chang, Bill Dolan, Jianfeng Gao, Wen tau Yih, and Michel Galley. A knowledge-grounded neural conversation model.

**中文**

doi：10.18653/v1/P19-1346。网址 https://www.aclweb.org/anthology/P19-1346。 [13] 安吉拉·范、克莱尔·加登特、克洛伊·布劳德和安托万·博德斯。使用基于 KNN 的复合内存增强Transformer，2020 年。URL https://openreview.net/forum?id= H1gx1CNKPH。 [14]蒂博·费夫里、利维奥·巴尔迪尼·苏亚雷斯、尼古拉斯·菲茨杰拉德、恩索尔·崔和汤姆·科维亚特科斯基。实体作为专家：具有实体监督的稀疏内存访问。 ArXiv，abs/2004.07202，2020。网址 https://arxiv.org/abs/2004.07202。 [15] Marjan Ghazvininejad、Chris Brockett、Ming-Wei Chang、Bill Dolan、Jianfeng Taka、Wen tau Yih 和 Michel Galley。基于知识的神经对话模型。

### 段落 77 · Page 11

**EN**

In AAAI Conference on Artiﬁcial Intelligence, 2018. URL https://www.aaai.org/ocs/index.php/ AAAI/AAAI18/paper/view/16710. [16] Katja Grace, John Salvatier, Allan Dafoe, Baobao Zhang, and Owain Evans. When will AI exceed human performance? evidence from AI experts. CoRR, abs/1705.08807, 2017. URL http://arxiv.org/abs/1705.08807. [17] Jiatao Gu, Yong Wang, Kyunghyun Cho, and Victor O.K. Li. Search engine guided neural machine translation. In AAAI Conference on Artiﬁcial Intelligence , 2018. URL https: //www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/view/17282. [18] Jiatao Gu, Yong Wang, Kyunghyun Cho, and Victor O.K. Li.

**中文**

AAAI 人工智能会议，2018 年。URL https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/view/16710。 [16] Katja Grace、John Salvatier、Allan Dafoe、Baobao 张和 Owain Evans。人工智能何时能超越人类？来自人工智能专家的证据。 CoRR，abs/1705.08807，2017。网址http://arxiv.org/abs/1705.08807。 [17] 顾嘉涛，王勇，曹京贤，Victor O.K.李。搜索引擎引导神经机器翻译。 AAAI 人工智能会议，2018。URL https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/view/17282。 [18] 顾嘉涛，王勇，曹京贤，Victor O.K.李。

### 段落 78 · Page 11

**EN**

Search engine guided neural machine translation. In 32nd AAAI Conference on Artiﬁcial Intelligence, AAAI 2018 , 32nd AAAI Conference on Artiﬁcial Intelligence, AAAI 2018, pages 5133–5140. AAAI press, 2018. 32nd AAAI Conference on Artiﬁcial Intelligence, AAAI 2018 ; Conference date: 02-02-2018 Through 07-02-2018. [19] Kelvin Guu, Tatsunori B. Hashimoto, Yonatan Oren, and Percy Liang. Generating sentences by editing prototypes. Transactions of the Association for Computational Linguistics, 6:437–450, 2018. doi: 10.1162/tacl_a_00030. URL https://www.aclweb.org/anthology/Q18-1031. 11

**中文**

搜索引擎引导神经机器翻译。第 32 届 AAAI 人工智能会议，AAAI 2018，第 32 届 AAAI 人工智能会议，AAAI 2018，第 5133–5140 页。 AAAI 出版社，2018 年。第 32 届 AAAI 人工智能会议，AAAI 2018；会议日期：2018年2月2日至2018年2月7日。 [19] Kelvin Guu、Tatsunori B. Hashimoto、Yonatan Oren 和 Percy Liang。通过编辑原型生成句子。计算语言学协会汇刊，6:437–450, 2018。doi: 10.1162/tacl_a_00030。网址 https://www.aclweb.org/anthology/Q18-1031。 11

### Page 12

### 段落 79 · Page 12

**EN**

[20] Kelvin Guu, Kenton Lee, Zora Tung, Panupong Pasupat, and Ming-Wei Chang. REALM: Retrieval-augmented language model pre-training. ArXiv, abs/2002.08909, 2020. URL https: //arxiv.org/abs/2002.08909. [21] Tatsunori B Hashimoto, Kelvin Guu, Yonatan Oren, and Percy S Liang. A retrieve-and-edit framework for predicting structured outputs. In S. Bengio, H. Wallach, H. Larochelle, K. Grauman, N. Cesa-Bianchi, and R. Garnett, editors, Advances in Neural Information Processing Systems 31 , pages 10052– 10062. Curran Associates, Inc., 2018. URL http://papers.nips.cc/paper/ 8209-a-retrieve-and-edit-framework-for-predicting-structured-outputs. pdf.

**中文**

[20] Kelvin Guu、Kenton Lee、Zora Tung、Panupong Pasupat 和 Ming-Wei Chang。 REALM：检索增强语言模型预训练。 ArXiv，abs/2002.08909，2020。URL https：//arxiv.org/abs/2002.08909。 [21] Tatsunori B Hashimoto、Kelvin Guu、Yonatan Oren 和 Percy S Liang。用于预测结构化输出的检索和编辑框架。 S. Bengio、H. Wallach、H. Larochelle、K. Grauman、N. Cesa-Bianchi 和 R. Garnett，编辑，《神经信息处理系统进展》31，第 10052–10062 页。Curran Associates, Inc.，2018。URL http://papers.nips.cc/paper/ [8209] 用于预测结构化输出的检索和编辑框架。 pdf。

### 段落 80 · Page 12

**EN**

[22] Nabil Hossain, Marjan Ghazvininejad, and Luke Zettlemoyer. Simple and effective retrieveedit-rerank text generation. In Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics, pages 2532–2538, Online, July 2020. Association for Computational Linguistics. doi: 10.18653/v1/2020.acl-main.228. URL https://www.aclweb.org/ anthology/2020.acl-main.228. [23] Jeff Johnson, Matthijs Douze, and Hervé Jégou. Billion-scale similarity search with gpus. arXiv preprint arXiv:1702.08734, 2017. URL https://arxiv.org/abs/1702.08734. [24] Mandar Joshi, Eunsol Choi, Daniel Weld, and Luke Zettlemoyer.

**中文**

[22] 纳比尔·侯赛因、马里安·加兹维内贾德和卢克·泽特尔莫耶。简单有效的检索编辑重新排序文本生成。计算语言学协会第 58 届年会记录，第 2532-2538 页，在线，2020 年 7 月。计算语言学协会。 doi：10.18653/v1/2020.acl-main.228。网址 https://www.aclweb.org/anthology/2020.acl-main.228。 [23] 杰夫·约翰逊、马蒂斯·杜兹和埃尔维·杰古。使用 GPU 进行十亿级相似性搜索。 arXiv 预印本 arXiv:1702.08734, 2017。URL https://arxiv.org/abs/1702.08734。 [24] Mandar Joshi、Eunsol Choi、Daniel Weld 和 Luke Zettlemoyer。

### 段落 81 · Page 12

**EN**

TriviaQA: A Large Scale Distantly Supervised Challenge Dataset for Reading Comprehension. In Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pages 1601–1611, Vancouver, Canada, July 2017. Association for Computational Linguistics. doi: 10.18653/v1/P17-1147. URL https://www.aclweb.org/anthology/P17-1147. [25] Armand Joulin and Tomas Mikolov. Inferring algorithmic patterns with stackaugmented recurrent nets. In Proceedings of the 28th International Conference on Neural Information Processing Systems - Volume 1 , NIPS’15, page 190–198, Cambridge, MA, USA, 2015. MIT Press.

**中文**

TriviaQA：用于阅读理解的大规模远程监督挑战数据集。计算语言学协会第 55 届年会论文集（第一卷：长论文），第 1601-1611 页，加拿大温哥华，2017 年 7 月。计算语言学协会。 doi：10.18653/v1/P17-1147。网址 https://www.aclweb.org/anthology/P17-1147。 [25] 阿曼德·茹林和托马斯·米科洛夫。使用堆栈增强循环网络推断算法模式。第 28 届神经信息处理系统国际会议论文集 - 第 1 卷，NIPS’15，第 190-198 页，美国马萨诸塞州剑桥，2015 年。麻省理工学院出版社。

### 段落 82 · Page 12

**EN**

URL https://papers.nips.cc/paper/ 5857-inferring-algorithmic-patterns-with-stack-augmented-recurrent-nets . [26] Vladimir Karpukhin, Barlas Oguz, Sewon Min, Ledell Wu, Sergey Edunov, Danqi Chen, and Wen-tau Yih. Dense passage retrieval for open-domain question answering. arXiv preprint arXiv:2004.04906, 2020. URL https://arxiv.org/abs/2004.04906. [27] Urvashi Khandelwal, Omer Levy, Dan Jurafsky, Luke Zettlemoyer, and Mike Lewis. Generalization through memorization: Nearest neighbor language models. In International Conference on Learning Representations, 2020. URL https://openreview.net/forum?id=HklBjCEKvH. [28] Diederik P.

**中文**

网址 https://papers.nips.cc/paper/5857-inferring-algorithmic-patterns-with-stack-augmented-recurrent-nets。 [26] Vladimir Karpukhin、Barlas Oguz、Sewon Min、Ledell Wu、Sergey Edunov、Danqi Chen 和 Wen-tau Yih。用于开放域问答的密集段落检索。 arXiv 预印本 arXiv:2004.04906, 2020。URL https://arxiv.org/abs/2004.04906。 [27] Urvashi Khandelwal、Omer Levy、Dan Jurafsky、Luke Zettlemoyer 和 Mike Lewis。通过记忆进行泛化：最近邻语言模型。 2020 年国际学习表征会议。URL https://openreview.net/forum?id=HklBjCEKvH。 [28] 迪德里克·P.

### 段落 83 · Page 12

**EN**

Kingma and Jimmy Ba. Adam: A method for stochastic optimization. In Yoshua Bengio and Yann LeCun, editors, 3rd International Conference on Learning Representations, ICLR 2015, San Diego, CA, USA, May 7-9, 2015, Conference Track Proceedings, 2015. URL http://arxiv.org/abs/1412.6980. [29] Tom Kwiatkowski, Jennimaria Palomaki, Olivia Redﬁeld, Michael Collins, Ankur Parikh, Chris Alberti, Danielle Epstein, Illia Polosukhin, Matthew Kelcey, Jacob Devlin, Kenton Lee, Kristina N. Toutanova, Llion Jones, Ming-Wei Chang, Andrew Dai, Jakob Uszkoreit, Quoc Le, and Slav Petrov. Natural Questions: a Benchmark for Question Answering Research.

**中文**

金玛和吉米巴。 Adam：一种随机优化方法。 Yoshua Bengio 和 Yann LeCun，编辑，第三届学习表征国际会议，ICLR 2015，美国加利福尼亚州圣地亚哥，2015 年 5 月 7-9 日，会议记录，2015 年。URL http://arxiv.org/abs/1412.6980。 [29] Tom Kwiatkowski、Jennimaria Palomaki、Olivia Redfield、Michael Collins、Ankur Parikh、Chris Alberti、Danielle Epstein、Illia Polosukhin、Matthew Kelcey、Jacob Devlin、Kenton Lee、Kristina N. Toutanova、Llion Jones、Ming-Wei Chang、Andrew Dai、Jakob Uszkoreit、Quoc Le 和 Slav Petrov。自然问题：问答研究的基准。

### 段落 84 · Page 12

**EN**

Transactions of the Association of Computational Linguistics, 2019. URL https://tomkwiat.users.x20web.corp.google.com/papers/ natural-questions/main-1455-kwiatkowski.pdf . [30] Guillaume Lample, Alexandre Sablayrolles, Marc’ Aurelio Ranzato, Ludovic Denoyer, and Herve Jegou. Large memory layers with product keys. In H. Wallach, H. Larochelle, A. Beygelzimer, F. d’ Alché-Buc, E. Fox, and R. Garnett, editors, Advances in Neural Information Processing Systems 32, pages 8548–8559. Curran Associates, Inc., 2019. URL http: //papers.nips.cc/paper/9061-large-memory-layers-with-product-keys.pdf .

**中文**

计算语言学协会汇刊，2019 年。URL https://tomkwiat.users.x20web.corp.google.com/papers/natural-questions/main-1455-kwiatkowski.pdf。 [30] Guillaume Lample、Alexandre Sablayrolles、Marc’ Aurelio Ranzato、Ludovic Denoyer 和 Herve Jegou。带有产品密钥的大存储层。见 H. Wallach、H. Larochelle、A. Beygelzimer、F. d’ Alché-Buc、E. Fox 和 R. Garnett，编辑，神经信息处理系统进展 32，第 8548-8559 页。 Curran Associates, Inc.，2019。URL http://papers.nips.cc/paper/9061-large-memory-layers-with-product-keys.pdf。

### 段落 85 · Page 12

**EN**

[31] Kenton Lee, Ming-Wei Chang, and Kristina Toutanova. Latent retrieval for weakly supervised open domain question answering. In Proceedings of the 57th Annual Meeting of the Association 12

**中文**

[31] Kenton Lee、Ming-Wei Chang 和 Kristina Toutanova。弱监督开放域问答的潜在检索。协会第 57 届年会记录 12

### Page 13

### 段落 86 · Page 13

**EN**

for Computational Linguistics, pages 6086–6096, Florence, Italy, July 2019. Association for Computational Linguistics. doi: 10.18653/v1/P19-1612. URL https://www.aclweb.org/ anthology/P19-1612. [32] Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Veselin Stoyanov, and Luke Zettlemoyer. BART: Denoising sequence-to-sequence pre-training for natural language generation, translation, and comprehension. arXiv preprint arXiv:1910.13461, 2019. URL https://arxiv.org/abs/1910.13461. [33] Jiwei Li, Michel Galley, Chris Brockett, Jianfeng Gao, and Bill Dolan.

**中文**

计算语言学，第 6086-6096 页，意大利佛罗伦萨，2019 年 7 月。计算语言学协会。 doi：10.18653/v1/P19-1612。网址 https://www.aclweb.org/anthology/P19-1612。 [32] Mike Lewis、Yinhan Liu、Naman Goyal、Marjan Ghazvininejad、Abdelrahman Mohamed、Omer Levy、Veselin Stoyanov 和 Luke Zettlemoyer。 BART：用于自然语言生成、翻译和理解的序列到序列去噪预训练。 arXiv 预印本 arXiv:1910.13461, 2019。URL https://arxiv.org/abs/1910.13461。 [33]李继伟、米歇尔·加利、克里斯·布罗克特、高剑峰和比尔·多兰。

### 段落 87 · Page 13

**EN**

A diversity-promoting objective function for neural conversation models. In Proceedings of the 2016 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, pages 110–119, San Diego, California, June 2016. Association for Computational Linguistics. doi: 10.18653/v1/N16-1014. URL https://www.aclweb.org/anthology/ N16-1014. [34] Margaret Li, Jason Weston, and Stephen Roller. Acute-eval: Improved dialogue evaluation with optimized questions and multi-turn comparisons. ArXiv, abs/1909.03087, 2019. URL https://arxiv.org/abs/1909.03087.

**中文**

神经对话模型的多样性促进目标函数。计算语言学协会北美分会 2016 年会议记录：人类语言技术，第 110-119 页，加利福尼亚州圣地亚哥，2016 年 6 月。计算语言学协会。 doi：10.18653/v1/N16-1014。网址 https://www.aclweb.org/anthology/N16-1014。 [34] 玛格丽特·李、杰森·韦斯顿和斯蒂芬·罗勒。 Acute-eval：通过优化问题和多轮比较改进对话评估。 ArXiv，abs/1909.03087，2019。网址 https://arxiv.org/abs/1909.03087。

### 段落 88 · Page 13

**EN**

[35] Hairong Liu, Mingbo Ma, Liang Huang, Hao Xiong, and Zhongjun He. Robust neural machine translation with joint textual and phonetic embedding. In Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics, pages 3044–3049, Florence, Italy, July 2019. Association for Computational Linguistics. doi: 10.18653/v1/P19-1291. URL https://www.aclweb.org/anthology/P19-1291. [36] Peter J. Liu*, Mohammad Saleh*, Etienne Pot, Ben Goodrich, Ryan Sepassi, Lukasz Kaiser, and Noam Shazeer. Generating wikipedia by summarizing long sequences. In International Conference on Learning Representations, 2018.

**中文**

[35] 刘海蓉，马明波，黄亮，熊浩，何中军。具有联合文本和语音嵌入的鲁棒神经机器翻译。计算语言学协会第 57 届年会论文集，第 3044-3049 页，意大利佛罗伦萨，2019 年 7 月。计算语言学协会。 doi：10.18653/v1/P19-1291。网址 https://www.aclweb.org/anthology/P19-1291。 [36] Peter J. Liu*、Mohammad Saleh*、Etienne Pot、Ben Goodrich、Ryan Sepassi、Lukasz Kaiser 和 Noam Shazeer。通过总结长序列来生成维基百科。学习表征国际会议，2018。

### 段落 89 · Page 13

**EN**

URL https://openreview.net/forum? id=Hyg0vbWC-. [37] Yury A. Malkov and D. A. Yashunin. Efﬁcient and robust approximate nearest neighbor search using hierarchical navigable small world graphs. IEEE Transactions on Pattern Analysis and Machine Intelligence, 42:824–836, 2016. URL https://arxiv.org/abs/1603.09320. [38] Gary Marcus. The next decade in ai: four steps towards robust artiﬁcial intelligence. arXiv preprint arXiv:2002.06177, 2020. URL https://arxiv.org/abs/2002.06177. [39] Luca Massarelli, Fabio Petroni, Aleksandra Piktus, Myle Ott, Tim Rocktäschel, Vassilis Plachouras, Fabrizio Silvestri, and Sebastian Riedel.

**中文**

网址 https://openreview.net/forum? id=Hyg0vbWC-. [37]尤里·A·马尔科夫和D·A·亚舒宁。使用分层可导航小世界图进行高效且稳健的近似最近邻搜索。 IEEE 模式分析和机器智能汇刊，42：824–836，2016。URL https://arxiv.org/abs/1603.09320。 [38] Gary Marcus.人工智能的下一个十年：迈向强大人工智能的四个步骤。 arXiv 预印本 arXiv:2002.06177, 2020。URL https://arxiv.org/abs/2002.06177。 [39] 卢卡·马萨雷利、法比奥·彼得罗尼、亚历山大·皮克图斯、迈尔·奥特、蒂姆·洛克塔舍尔、瓦西利斯·普拉乔拉斯、法布里奇奥·西尔维斯特里和塞巴斯蒂安·里德尔。

### 段落 90 · Page 13

**EN**

How decoding strategies affect the veriﬁability of generated text. arXiv preprint arXiv:1911.03587 , 2019. URL https: //arxiv.org/abs/1911.03587. [40] Paulius Micikevicius, Sharan Narang, Jonah Alben, Gregory Diamos, Erich Elsen, David Garcia, Boris Ginsburg, Michael Houston, Oleksii Kuchaiev, Ganesh Venkatesh, and Hao Wu. Mixed precision training. In ICLR, 2018. URL https://openreview.net/forum?id=r1gs9JgRZ. [41] Nikita Moghe, Siddhartha Arora, Suman Banerjee, and Mitesh M. Khapra. Towards exploiting background knowledge for building conversation systems.

**中文**

解码策略如何影响生成文本的可验证性。 arXiv 预印本 arXiv:1911.03587，2019。URL https://arxiv.org/abs/1911.03587。 [40] Paulius Micikevicius、Sharan Narang、Jonah Alben、Gregory Diamos、Erich Elsen、David Garcia、Boris Ginsburg、Michael Houston、Oleksii Kuchaiev、Ganesh Venkatesh 和吴浩。混合精准训练。 ICLR，2018 年。URL https://openreview.net/forum?id=r1gs9JgRZ。 [41] Nikita Moghe、Siddhartha Arora、Suman Banerjee 和 Mitesh M. Khapra。利用背景知识来构建对话系统。

### 段落 91 · Page 13

**EN**

In Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing, pages 2322–2332, Brussels, Belgium, October-November 2018. Association for Computational Linguistics. doi: 10.18653/v1/D18-1255. URL https://www.aclweb.org/anthology/D18-1255. [42] Preksha Nema and Mitesh M. Khapra. Towards a better metric for evaluating question generation systems. In Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing, pages 3950–3959, Brussels, Belgium, October-November 2018. Association for Computational Linguistics. doi: 10.18653/v1/D18-1429. URL https://www.aclweb.org/ anthology/D18-1429.

**中文**

2018 年自然语言处理经验方法会议论文集，第 2322-2332 页，比利时布鲁塞尔，2018 年 10 月至 11 月。计算语言学协会。 doi：10.18653/v1/D18-1255。网址 https://www.aclweb.org/anthology/D18-1255。 [42] Preksha Nema 和 Mitesh M. Khapra。寻求更好的评估问题生成系统的指标。 2018 年自然语言处理经验方法会议论文集，第 3950-3959 页，比利时布鲁塞尔，2018 年 10 月至 11 月。计算语言学协会。 doi：10.18653/v1/D18-1429。网址 https://www.aclweb.org/anthology/D18-1429。

### 段落 92 · Page 13

**EN**

[43] Tri Nguyen, Mir Rosenberg, Xia Song, Jianfeng Gao, Saurabh Tiwary, Rangan Majumder, and Li Deng. MS MARCO: A human generated machine reading comprehension dataset. In Tarek Richard Besold, Antoine Bordes, Artur S. d’Avila Garcez, and Greg Wayne, editors, Proceedings of the Workshop on Cognitive Computation: Integrating neural and symbolic 13

**中文**

[43] Tri Nguyen，Mir Rosenberg，夏宋，高剑锋，Saurabh Tiwary，Rangan Majumder，邓力。 MS MARCO：人类生成的机器阅读理解数据集。载于 Tarek Richard Besold、Antoine Bordes、Artur S. d’Avila Garcez 和 Greg Wayne，编辑，认知计算研讨会论文集：整合神经和符号 13

### Page 14

### 段落 93 · Page 14

**EN**

approaches 2016 co-located with the 30th Annual Conference on Neural Information Processing Systems (NIPS 2016), Barcelona, Spain, December 9, 2016, volume 1773 of CEUR Workshop Proceedings. CEUR-WS.org, 2016. URL http://ceur-ws.org/Vol-1773/CoCoNIPS_ 2016_paper9.pdf. [44] Rodrigo Nogueira and Kyunghyun Cho. Passage re-ranking with BERT. arXiv preprint arXiv:1901.04085, 2019. URL https://arxiv.org/abs/1901.04085. [45] Myle Ott, Sergey Edunov, Alexei Baevski, Angela Fan, Sam Gross, Nathan Ng, David Grangier, and Michael Auli. fairseq: A fast, extensible toolkit for sequence modeling.

**中文**

2016 年即将到来，与第 30 届神经信息处理系统年会 (NIPS 2016) 同期举行，西班牙巴塞罗那，2016 年 12 月 9 日，CEUR 研讨会论文集第 1773 卷。 CEUR-WS.org，2016 年。网址 http://ceur-ws.org/Vol-1773/CoCoNIPS_2016_paper9.pdf。 [44] 罗德里戈·诺盖拉和曹庆贤。使用 BERT 对段落重新排序。 arXiv 预印本 arXiv:1901.04085, 2019。URL https://arxiv.org/abs/1901.04085。 [45] Myle Ott、Sergey Edunov、Alexei Baevski、Angela Fan、Sam Gross、Nathan Ng、David Grangier 和 Michael Auli。 fairseq：一个快速、可扩展的序列建模工具包。

### 段落 94 · Page 14

**EN**

In Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics (Demonstrations), pages 48–53, Minneapolis, Minnesota, June 2019. Association for Computational Linguistics. doi: 10.18653/v1/N19-4009. URL https://www.aclweb. org/anthology/N19-4009. [46] Ethan Perez, Siddharth Karamcheti, Rob Fergus, Jason Weston, Douwe Kiela, and Kyunghyun Cho. Finding generalizable evidence by learning to convince q&a models.

**中文**

计算语言学协会北美分会 2019 年会议记录（演示），第 48-53 页，明尼苏达州明尼阿波利斯，2019 年 6 月。计算语言学协会。 doi：10.18653/v1/N19-4009。网址 https://www.aclweb。 org/anthology/N19-4009。 [46] 伊森·佩雷斯 (Ethan Perez)、悉达思·卡拉姆切蒂 (Siddharth Karamcheti)、罗布·弗格斯 (Rob Fergus)、杰森·韦斯顿 (Jason Weston)、道威·基拉 (Douwe Kiela) 和曹京贤 (Kyunghyun Cho)。通过学习说服问答模型来寻找普遍的证据。

### 段落 95 · Page 14

**EN**

In Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP) , pages 2402–2411, Hong Kong, China, November 2019. Association for Computational Linguistics. doi: 10.18653/v1/D19-1244. URL https://www.aclweb.org/anthology/D19-1244. [47] Fabio Petroni, Tim Rocktäschel, Sebastian Riedel, Patrick Lewis, Anton Bakhtin, Yuxiang Wu, and Alexander Miller. Language models as knowledge bases?

**中文**

2019 年自然语言处理经验方法会议和第九届自然语言处理国际联合会议 (EMNLP-IJCNLP) 论文集，第 2402–2411 页，中国香港，2019 年 11 月。计算语言学协会。 doi：10.18653/v1/D19-1244。网址 https://www.aclweb.org/anthology/D19-1244。 [47] 法比奥·彼得罗尼、蒂姆·洛克塔舍尔、塞巴斯蒂安·里德尔、帕特里克·刘易斯、安东·巴赫金、吴宇翔和亚历山大·米勒。语言模型作为知识库？

### 段落 96 · Page 14

**EN**

In Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP), pages 2463–2473, Hong Kong, China, November 2019. Association for Computational Linguistics. doi: 10.18653/v1/ D19-1250. URL https://www.aclweb.org/anthology/D19-1250. [48] Fabio Petroni, Patrick Lewis, Aleksandra Piktus, Tim Rocktäschel, Yuxiang Wu, Alexander H. Miller, and Sebastian Riedel. How context affects language models’ factual predictions. In Automated Knowledge Base Construction, 2020. URL https://openreview.net/forum? id=025X0zPfn.

**中文**

2019 年自然语言处理经验方法会议和第九届自然语言处理国际联合会议 (EMNLP-IJCNLP) 论文集，第 2463–2473 页，中国香港，2019 年 11 月。计算语言学协会。 doi：10.18653/v1/D19-1250。网址 https://www.aclweb.org/anthology/D19-1250。 [48] 法比奥·佩特罗尼 (Fabio Petroni)、帕特里克·刘易斯 (Patrick Lewis)、亚历山大·皮克图斯 (Aleksandra Piktus)、蒂姆·洛克塔舍尔 (Tim Rocktäschel)、吴宇翔、亚历山大·H·米勒 (Alexander H. Miller) 和塞巴斯蒂安·里德尔 (Sebastian Riedel)。上下文如何影响语言模型的事实预测。自动化知识库建设，2020。URL https://openreview.net/forum? id=025X0zPfn。

### 段落 97 · Page 14

**EN**

[49] Alec Radford, Karthik Narasimhan, Tim Salimans, and Ilya Sutskever. Improving Language Understanding by Generative Pre-Training, 2018. URL https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/ language-unsupervised/language_understanding_paper.pdf. [50] Alec Radford, Jeff Wu, Rewon Child, David Luan, Dario Amodei, and Ilya Sutskever. Language models are unsupervised multitask learners, 2019. URL https://d4mucfpksywv.cloudfront.net/better-language-models/language_ models_are_unsupervised_multitask_learners.pdf.

**中文**

[49] 亚历克·雷德福德、卡蒂克·纳拉西姆汉、蒂姆·萨利曼和伊利亚·苏茨克弗。通过生成预训练提高语言理解，2018。URL https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/ language-unsupervised/language_understand_paper.pdf。 [50] 亚历克·雷德福德、杰夫·吴、Rewon Child、大卫·卢安、达里奥·阿莫代和伊利亚·苏茨克弗。语言模型是无监督多任务学习者，2019 年。URL https://d4mucfpksywv.cloudfront.net/better-language-models/language_ models_are_unsupervised_multitask_learners.pdf。

### 段落 98 · Page 14

**EN**

[51] Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, and Peter J. Liu. Exploring the limits of transfer learning with a uniﬁed text-to-text transformer. arXiv e-prints, 2019. URL https://arxiv.org/abs/1910.10683. [52] Adam Roberts, Colin Raffel, and Noam Shazeer. How much knowledge can you pack into the parameters of a language model? arXiv e-prints, 2020. URL https://arxiv.org/abs/ 2002.08910. [53] Stephen Robertson and Hugo Zaragoza. The probabilistic relevance framework: Bm25 and beyond. Found. Trends Inf. Retr., 3(4):333–389, April 2009. ISSN 1554-0669. doi: 10.1561/ 1500000019.

**中文**

[51] Colin Raffel、Noam Shazeer、Adam Roberts、Katherine Lee、Sharan Narang、Michael Matena、Yanqi Zhou、Wei Li 和 Peter J. Liu。使用统一的文本到文本转换器探索迁移学习的局限性。 arXiv 电子印刷品，2019 年。URL https://arxiv.org/abs/1910.10683。 [52] 亚当·罗伯茨、科林·拉斐尔和诺姆·沙泽尔。您可以将多少知识装入语言模型的参数中？ arXiv 电子印刷品，2020 年。URL https://arxiv.org/abs/2002.08910。 [53] 斯蒂芬·罗伯逊和雨果·萨拉戈萨。概率相关性框架：Bm25 及更高版本。成立。趋势信息。回顾，3(4)：333–389，2009 年 4 月。ISSN 1554-0669。 DOI：10.1561/1500000019。

### 段落 99 · Page 14

**EN**

URL https://doi.org/10.1561/1500000019. [54] Irene Solaiman, Miles Brundage, Jack Clark, Amanda Askell, Ariel Herbert-V oss, Jeff Wu, Alec Radford, and Jian-Bing Wang. Release strategies and the social impacts of language models. ArXiv, abs/1908.09203, 2019. [55] Sainbayar Sukhbaatar, Arthur Szlam, Jason Weston, and Rob Fergus. End-to-end memory networks. In C. Cortes, N. D. Lawrence, D. D. Lee, M. Sugiyama, and R. Garnett, editors,Advances in Neural Information Processing Systems 28, pages 2440–2448. Curran Associates, Inc., 2015. URL http://papers.nips.cc/paper/5846-end-to-end-memory-networks.pdf . 14

**中文**

网址 https://doi.org/10.1561/1500000019。 [54] 艾琳·索莱曼、迈尔斯·布伦戴奇、杰克·克拉克、阿曼达·阿斯克尔、阿里尔·赫伯特-沃斯、杰夫·吴、亚历克·雷德福和王建兵。语言模型的发布策略和社会影响。 ArXiv，abs/1908.09203，2019。 [55] Sainbayar Sukhbaatar、Arthur Szlam、Jason Weston 和 Rob Fergus。端到端内存网络。 C. Cortes、N. D. Lawrence、D. D. Lee、M. Sugiyama 和 R. Garnett，编辑，神经信息处理系统进展 28，第 2440-2448 页。 Curran Associates, Inc.，2015。URL http://papers.nips.cc/paper/5846-end-to-end-memory-networks.pdf。 14

### Page 15

### 段落 100 · Page 15

**EN**

[56] James Thorne, Andreas Vlachos, Christos Christodoulopoulos, and Arpit Mittal. FEVER: a large-scale dataset for fact extraction and VERiﬁcation. In Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers), pages 809–819, New Orleans, Louisiana, June 2018. Association for Computational Linguistics. doi: 10.18653/v1/N18-1074. URL https://www.aclweb.org/anthology/N18-1074. [57] James H. Thorne and Andreas Vlachos.

**中文**

[56] 詹姆斯·索恩、安德烈亚斯·弗拉科斯、克里斯托·克里斯托杜洛普洛斯和阿尔皮特·米塔尔。 FEVER：用于事实提取和验证的大规模数据集。计算语言学协会北美分会 2018 年会议记录：人类语言技术，第 1 卷（长论文），第 809-819 页，路易斯安那州新奥尔良，2018 年 6 月。计算语言学协会。 doi：10.18653/v1/N18-1074。网址 https://www.aclweb.org/anthology/N18-1074。 [57] 詹姆斯·H·索恩和安德烈亚斯·弗拉科斯。

### 段落 101 · Page 15

**EN**

Avoiding catastrophic forgetting in mitigating model biases in sentence-pair classiﬁcation with elastic weight consolidation. ArXiv, abs/2004.14366, 2020. URL https://arxiv.org/abs/2004.14366. [58] Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N Gomez, Ł ukasz Kaiser, and Illia Polosukhin. Attention is all you need. In I. Guyon, U. V . Luxburg, S. Bengio, H. Wallach, R. Fergus, S. Vishwanathan, and R. Garnett, editors,Advances in Neural Information Processing Systems 30, pages 5998–6008. Curran Associates, Inc., 2017. URL http://papers.nips.cc/paper/7181-attention-is-all-you-need.pdf .

**中文**

通过弹性权重巩固减轻句子对分类中的模型偏差，避免灾难性遗忘。 ArXiv，abs/2004.14366，2020。URL https://arxiv.org/abs/2004.14366。 [58] Ashish Vaswani、Noam Shazeer、Niki Parmar、Jakob Uszkoreit、Llion Jones、Aidan N Gomez、Ł ukasz Kaiser 和 Illia Polosukhin。您所需要的就是关注。在 I.Guyon，U.V. Luxburg、S. Bengio、H. Wallach、R. Fergus、S. Vishwanathan 和 R. Garnett，编辑，神经信息处理系统进展 30，第 5998–6008 页。 Curran Associates, Inc.，2017 年。URL http://papers.nips.cc/paper/7181-attention-is-all-you-need.pdf。

### 段落 102 · Page 15

**EN**

[59] Ashwin Vijayakumar, Michael Cogswell, Ramprasaath Selvaraju, Qing Sun, Stefan Lee, David Crandall, and Dhruv Batra. Diverse beam search for improved description of complex scenes. AAAI Conference on Artiﬁcial Intelligence, 2018. URL https://www.aaai.org/ocs/index. php/AAAI/AAAI18/paper/view/17329. [60] Alex Wang, Amanpreet Singh, Julian Michael, Felix Hill, Omer Levy, and Samuel Bowman. GLUE: A multi-task benchmark and analysis platform for natural language understanding. In Proceedings of the 2018 EMNLP Workshop BlackboxNLP: Analyzing and Interpreting Neural Networks for NLP, pages 353–355, Brussels, Belgium, November 2018.

**中文**

[59] Ashwin Vijayakumar、Michael Cogswell、Ramprasaath Selvaraju、Qing Sun、Stefan Lee、David Crandall 和 Dhruv Batra。多样化波束搜索可改进复杂场景的描述。 AAAI 人工智能会议，2018。URL https://www.aaai.org/ocs/index。 php/AAAI/AAAI18/paper/view/17329.php/AAAI/AAAI18/paper/view/17329. [60] Alex Wang、Amanpreet Singh、Julian Michael、Felix Hill、Omer Levy 和 Samuel Bowman。 GLUE：用于自然语言理解的多任务基准测试和分析平台。 2018 年 EMNLP 研讨会 BlackboxNLP：分析和解释 NLP 神经网络的会议记录，第 353-355 页，比利时布鲁塞尔，2018 年 11 月。

### 段落 103 · Page 15

**EN**

Association for Computational Linguistics. doi: 10.18653/v1/W18-5446. URL https://www.aclweb.org/ anthology/W18-5446. [61] Alex Wang, Yada Pruksachatkun, Nikita Nangia, Amanpreet Singh, Julian Michael, Felix Hill, Omer Levy, and Samuel Bowman. SuperGLUE: A Stickier Benchmark for General- Purpose Language Understanding Systems. In H. Wallach, H. Larochelle, A. Beygelzimer, F. d\textquotesingle Alché-Buc, E. Fox, and R. Garnett, editors,Advances in Neural Information Processing Systems 32, pages 3261–3275. Curran Associates, Inc., 2019. URL https:// arxiv.org/abs/1905.00537.

**中文**

计算语言学协会。 doi：10.18653/v1/W18-5446。网址 https://www.aclweb.org/anthology/W18-5446。 [61] Alex Wang、Yada Pruksachatkun、Nikita Nangia、Amanpreet Singh、Julian Michael、Felix Hill、Omer Levy 和 Samuel Bowman。 SuperGLUE：通用语言理解系统的更具粘性的基准。摘自 H. Wallach、H. Larochelle、A. Beygelzimer、F. d\textquotesingle Alché-Buc、E. Fox 和 R. Garnett，编辑，神经信息处理系统进展 32，第 3261-3275 页。 Curran Associates, Inc.，2019。URL https://arxiv.org/abs/1905.00537。

### 段落 104 · Page 15

**EN**

[62] Shuohang Wang, Mo Yu, Xiaoxiao Guo, Zhiguo Wang, Tim Klinger, Wei Zhang, Shiyu Chang, Gerry Tesauro, Bowen Zhou, and Jing Jiang. R3: Reinforced ranker-reader for open-domain question answering. In Sheila A. McIlraith and Kilian Q. Weinberger, editors, Proceedings of the Thirty-Second AAAI Conference on Artiﬁcial Intelligence, (AAAI-18), the 30th innovative Applications of Artiﬁcial Intelligence (IAAI-18), and the 8th AAAI Symposium on Educational Advances in Artiﬁcial Intelligence (EAAI-18), New Orleans, Louisiana, USA, February 2-7, 2018, pages 5981–5988. AAAI Press, 2018. URL https://www.aaai.org/ocs/index.

**中文**

[62] 王硕航，于墨，郭晓晓，王志国，Tim Klinger，张伟，常世宇，Gerry Tesauro，周博文，江静。 R3：用于开放域问答的强化排名阅读器。 Sheila A. McIlraith 和 Kilian Q. Weinberger，编辑，《第三十二届 AAAI 人工智能会议论文集》(AAAI-18)、第 30 届人工智能创新应用 (IAAI-18) 和第八届 AAAI 人工智能教育进展研讨会 (EAAI-18)，路易斯安那州新奥尔良，美国，2018 年 2 月 2-7 日，第 5981-5988 页。 AAAI 出版社，2018 年。网址 https://www.aaai.org/ocs/index。

### 段落 105 · Page 15

**EN**

php/AAAI/AAAI18/paper/view/16712. [63] Shuohang Wang, Mo Yu, Jing Jiang, Wei Zhang, Xiaoxiao Guo, Shiyu Chang, Zhiguo Wang, Tim Klinger, Gerald Tesauro, and Murray Campbell. Evidence aggregation for answer reranking in open-domain question answering. In ICLR, 2018. URL https://openreview. net/forum?id=rJl3yM-Ab. [64] Jason Weston, Sumit Chopra, and Antoine Bordes. Memory networks. In Yoshua Bengio and Yann LeCun, editors, 3rd International Conference on Learning Representations, ICLR 2015, San Diego, CA, USA, May 7-9, 2015, Conference Track Proceedings , 2015. URL http://arxiv.org/abs/1410.3916.

**中文**

php/AAAI/AAAI18/paper/view/16712.php/AAAI/AAAI18/paper/view/16712. [63] 王硕航，于墨，姜静，张伟，郭晓晓，常世宇，王志国，Tim Klinger，Gerald Tesauro，Murray Campbell。开放域问答中答案重排的证据聚合。 ICLR，2018。URL https://openreview。网/论坛？id=rJl3yM-Ab。 [64]杰森·韦斯顿、苏米特·乔普拉和安托万·博德斯。记忆网络。 Yoshua Bengio 和 Yann LeCun，编辑，第三届学习表征国际会议，ICLR 2015，美国加利福尼亚州圣地亚哥，2015 年 5 月 7-9 日，会议记录，2015 年。URL http://arxiv.org/abs/1410.3916。

### 段落 106 · Page 15

**EN**

[65] Jason Weston, Emily Dinan, and Alexander Miller. Retrieve and reﬁne: Improved sequence generation models for dialogue. In Proceedings of the 2018 EMNLP Workshop SCAI: The 2nd International Workshop on Search-Oriented Conversational AI, pages 87–92, Brussels, Belgium, October 2018. Association for Computational Linguistics. doi: 10.18653/v1/W18-5713. URL https://www.aclweb.org/anthology/W18-5713. 15

**中文**

[65] 杰森·韦斯顿、艾米丽·迪南和亚历山大·米勒。检索和细化：改进的对话序列生成模型。 2018 年 EMNLP 研讨会 SCAI 论文集：第二届面向搜索的会话人工智能国际研讨会，第 87-92 页，比利时布鲁塞尔，2018 年 10 月。计算语言学协会。 doi：10.18653/v1/W18-5713。网址 https://www.aclweb.org/anthology/W18-5713。 15

### Page 16

### 段落 107 · Page 16

**EN**

[66] Thomas Wolf, Lysandre Debut, Victor Sanh, Julien Chaumond, Clement Delangue, Anthony Moi, Pierric Cistac, Tim Rault, Rémi Louf, Morgan Funtowicz, Joe Davison, Sam Shleifer, Patrick von Platen, Clara Ma, Yacine Jernite, Julien Plu, Canwen Xu, Teven Le Scao, Sylvain Gugger, Mariama Drame, Quentin Lhoest, and Alexander M. Rush. Huggingface’s transformers: State-of-the-art natural language processing. ArXiv, abs/1910.03771, 2019. [67] Shiyue Zhang and Mohit Bansal. Addressing semantic drift in question generation for semisupervised question answering.

**中文**

[66] 托马斯·沃尔夫、Lysandre Debut、维克多·桑、朱利安·肖蒙德、克莱门特·德朗格、安东尼·莫伊、皮埃里克·西斯塔克、蒂姆·劳特、雷米·卢夫、摩根·芬托维奇、乔·戴维森、萨姆·施莱弗、帕特里克·冯·普拉滕、克拉拉·马、亚辛·杰尼特、朱利安·普鲁、徐灿文、特文·勒·斯考、西尔万·古格、玛丽亚玛·德拉梅、昆汀洛斯特和亚历山大·M·拉什。 Huggingface 的变形金刚：最先进的自然语言处理。 ArXiv，abs/1910.03771，2019。[67]Shiyue Zhang 和 Mohit Bansal。解决半监督问答问题生成中的语义漂移。

### 段落 108 · Page 16

**EN**

In Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP) , pages 2495–2509, Hong Kong, China, November 2019. Association for Computational Linguistics. doi: 10.18653/v1/D19-1253. URL https://www.aclweb.org/anthology/D19-1253. [68] Wanjun Zhong, Jingjing Xu, Duyu Tang, Zenan Xu, Nan Duan, Ming Zhou, Jiahai Wang, and Jian Yin. Reasoning over semantic-level graph for fact checking. ArXiv, abs/1909.03745, 2019. URL https://arxiv.org/abs/1909.03745. 16

**中文**

2019 年自然语言处理经验方法会议和第九届自然语言处理国际联合会议 (EMNLP-IJCNLP) 论文集，第 2495–2509 页，中国香港，2019 年 11 月。计算语言学协会。 doi：10.18653/v1/D19-1253。网址 https://www.aclweb.org/anthology/D19-1253。 [68] 钟万军，徐晶晶，唐杜宇，徐泽南，段南，周明，王家海，尹建。对语义级图进行推理以进行事实检查。 ArXiv，abs/1909.03745，2019。网址 https://arxiv.org/abs/1909.03745。 16

### Page 17

### 段落 109 · Page 17

**EN**

Appendices for Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks A Implementation Details For Open-domain QA we report test numbers using 15 retrieved documents for RAG-Token models. For RAG-Sequence models, we report test results using 50 retrieved documents, and we use the Thorough Decoding approach since answers are generally short. We use greedy decoding for QA as we did not ﬁnd beam search improved results. For Open-MSMarco and Jeopardy question generation, we report test numbers using ten retrieved documents for both RAG-Token and RAG-Sequence, and we also train a BART-large model as a baseline.

**中文**

知识密集型 NLP 任务的检索增强生成附录 A 实施细节 对于开放域 QA，我们使用 RAG-Token 模型的 15 个检索文档报告测试编号。对于 RAG 序列模型，我们使用 50 个检索到的文档报告测试结果，并且我们使用彻底解码方法，因为答案通常很短。我们使用贪婪解码进行 QA，因为我们没有发现波束搜索改进的结果。对于 Open-MSMarco 和 Jeopardy 问题生成，我们使用 RAG-Token 和 RAG-Sequence 的 10 个检索文档来报告测试数字，并且我们还训练 BART-large 模型作为基线。

### 段落 110 · Page 17

**EN**

We use a beam size of four, and use the Fast Decoding approach for RAG-Sequence models, as Thorough Decoding did not improve performance. B Human Evaluation Figure 4: Annotation interface for human evaluation of factuality. A pop-out for detailed instructions and a worked example appear when clicking "view tool guide". Figure 4 shows the user interface for human evaluation. To avoid any biases for screen position, which model corresponded to sentence A and sentence B was randomly selected for each example.

**中文**

我们使用大小为 4 的波束，并对 RAG 序列模型使用快速解码方法，因为彻底解码并没有提高性能。 B 人类评估 图 4：用于人类评估事实性的注释界面。单击“查看工具指南”时，会弹出详细说明和工作示例。图 4 显示了用于人工评估的用户界面。为了避免屏幕位置的任何偏差，为每个示例随机选择对应于句子 A 和句子 B 的模型。

### 段落 111 · Page 17

**EN**

Annotators were encouraged to research the topic using the internet, and were given detailed instructions and worked examples in a full instructions tab. We included some gold sentences in order to assess the accuracy of the annotators. Two annotators did not perform well on these examples and their annotations were removed from the results. C Training setup Details We train all RAG models and BART baselines using Fairseq [45].2 We train with mixed precision ﬂoating point arithmetic [ 40], distributing training across 8, 32GB NVIDIA V100 GPUs, though training and inference can be run on one GPU.

**中文**

鼓励注释者使用互联网研究该主题，并在完整的说明选项卡中获得详细的说明和工作示例。我们加入了一些黄金句子，以评估注释者的准确性。两个注释者在这些示例上表现不佳，他们的注释已从结果中删除。 C 训练设置详细信息 我们使用 Fairseq [45] 训练所有 RAG 模型和 BART 基线。2 我们使用混合精度浮点算法进行训练 [40]，将训练分布在 8 个 32GB NVIDIA V100 GPU 上，尽管训练和推理可以在一个 GPU 上运行。

### 段落 112 · Page 17

**EN**

We ﬁnd that doing Maximum Inner Product Search with FAISS is sufﬁciently fast on CPU, so we store document index vectors on CPU, requiring∼ 100 GB of CPU memory for all of Wikipedia. After submission, We have ported our code to HuggingFace Transformers [66]3, which achieves equivalent performance to the previous version but is a cleaner and easier to use implementation. This version is also open-sourced. We also compress the document index using FAISS’s compression tools, reducing the CPU memory requirement to 36GB.

**中文**

我们发现使用 FAISS 进行最大内积搜索在 CPU 上足够快，因此我们将文档索引向量存储在 CPU 上，所有维基百科需要约 100 GB 的 CPU 内存。提交后，我们将代码移植到 HuggingFace Transformers [66]3，它实现了与之前版本相当的性能，但实现更干净、更易于使用。这个版本也是开源的。我们还使用 FAISS 的压缩工具压缩文档索引，将 CPU 内存需求减少到 36GB。

### 段落 113 · Page 17

**EN**

Scripts to run experiments with RAG can be found athttps://github.com/huggingface/transformers/ blob/master/examples/rag/README.md and an interactive demo of a RAG model can be found at https://huggingface.co/rag/ 2https://github.com/pytorch/fairseq 3https://github.com/huggingface/transformers 17

**中文**

使用 RAG 运行实验的脚本可以在 https://github.com/huggingface/transformers/ blob/master/examples/rag/README.md 中找到，RAG 模型的交互式演示可以在 https://huggingface.co/rag/ 2 https://github.com/pytorch/fairseq 3 https://github.com/huggingface/transformers 17 中找到

### Page 18

### 段落 114 · Page 18

**EN**

D Further Details on Open-Domain QA For open-domain QA, multiple answer annotations are often available for a given question. These answer annotations are exploited by extractive models during training as typically all the answer annotations are used to ﬁnd matches within documents when preparing training data. For RAG, we also make use of multiple annotation examples for Natural Questions and WebQuestions by training the model with each (q,a ) pair separately, leading to a small increase in accuracy.

**中文**

D 关于开放域 QA 的更多详细信息 对于开放域 QA，给定问题通常可以使用多个答案注释。这些答案注释在训练期间被提取模型利用，因为通常所有答案注释都用于在准备训练数据时在文档中查找匹配项。对于 RAG，我们还通过分别使用每个 (q,a ) 对训练模型来利用自然问题和 WebQuestions 的多个注释示例，从而导致准确性小幅提高。

### 段落 115 · Page 18

**EN**

For TriviaQA, there are often many valid answers to a given question, some of which are not suitable training targets, such as emoji or spelling variants. For TriviaQA, we ﬁlter out answer candidates if they do not occur in top 1000 documents for the query. CuratedTrec preprocessing The answers for CuratedTrec are given in the form of regular expressions, which has been suggested as a reason why it is unsuitable for answer-generation models [20].

**中文**

对于 TriviaQA，给定问题通常有许多有效答案，其中一些不是合适的训练目标，例如表情符号或拼写变体。对于 TriviaQA，如果候选答案未出现在查询的前 1000 个文档中，我们就会过滤掉它们。 CuratedTrec 预处理 CuratedTrec 的答案以正则表达式的形式给出，这被认为是它不适合答案生成模型的原因[20]。

### 段落 116 · Page 18

**EN**

To overcome this, we use a pre-processing step where we ﬁrst retrieve the top 1000 documents for each query, and use the answer that most frequently matches the regex pattern as the supervision target. If no matches are found, we resort to a simple heuristic: generate all possible permutations for each regex, replacing non-deterministic symbols in the regex nested tree structure with a whitespace. TriviaQA Evaluation setups The open-domain QA community customarily uses public development datasets as test datasets, as test data for QA datasets is often restricted and dedicated to reading compehension purposes.

**中文**

为了克服这个问题，我们使用预处理步骤，首先检索每个查询的前 1000 个文档，并使用最常与正则表达式模式匹配的答案作为监督目标。如果没有找到匹配项，我们采用简单的启发式方法：为每个正则表达式生成所有可能的排列，用空格替换正则表达式嵌套树结构中的非确定性符号。 TriviaQA 评估设置 开放域 QA 社区通常使用公共开发数据集作为测试数据集，因为 QA 数据集的测试数据通常受到限制并专用于阅读理解目的。

### 段落 117 · Page 18

**EN**

We report our results using the datasets splits used in DPR [26], which are consistent with common practice in Open-domain QA. For TriviaQA, this test dataset is the public TriviaQA Web Development split. Roberts et al.[52] used the TriviaQA ofﬁcial Wikipedia test set instead. Févry et al. [14] follow this convention in order to compare with Roberts et al. [52] (See appendix of [14]). We report results on both test sets to enable fair comparison to both approaches.

**中文**

我们使用 DPR [26] 中使用的数据集分割来报告我们的结果，这与开放域 QA 中的常见做法一致。对于 TriviaQA，此测试数据集是公共 TriviaQA Web 开发拆分。罗伯茨等人[52]相反，使用了 TriviaQA 官方维基百科测试集。费夫里等人。 [14] 遵循这一惯例以便与 Roberts 等人进行比较。 [52]（见[14]附录）。我们报告两个测试集的结果，以便对两种方法进行公平比较。

### 段落 118 · Page 18

**EN**

We ﬁnd that our performance is much higher using the ofﬁcial Wiki test set, rather than the more conventional open-domain test set, which we attribute to the ofﬁcial Wiki test set questions being simpler to answer from Wikipedia. E Further Details on FEVER For FEVER classiﬁcation, we follow the practice from [ 32], and ﬁrst re-generate the claim, and then classify using the representation of the ﬁnal hidden state, before ﬁnally marginalizing across documents to obtain the class probabilities. The FEVER task traditionally has two sub-tasks.

**中文**

我们发现使用官方 Wiki 测试集，而不是更传统的开放域测试集，我们的性能要高得多，我们将其归因于官方 Wiki 测试集问题更容易从维基百科中回答。 E 关于 FEVER 的更多细节 对于 FEVER 分类，我们遵循[32]中的实践，首先重新生成声明，然后使用最终隐藏状态的表示进行分类，最后在文档之间进行边缘化以获得类别概率。 FEVER 任务传统上有两个子任务。

### 段落 119 · Page 18

**EN**

The ﬁrst is to classify the claim as either "Supported", "Refuted" or "Not Enough Info", which is the task we explore in the main paper. FEVER’s other sub-task involves extracting sentences from Wikipedia as evidence supporting the classiﬁcation prediction. As FEVER uses a different Wikipedia dump to us, directly tackling this task is not straightforward. We hope to address this in future work. F Null Document Probabilities We experimented with adding "Null document" mechanism to RAG, similar to REALM [20] in order to model cases where no useful information could be retrieved for a given input.

**中文**

首先是将主张分类为“支持”、“驳斥”或“信息不足”，这是我们在主论文中探讨的任务。 FEVER 的另一个子任务涉及从维基百科中提取句子作为支持分类预测的证据。由于 FEVER 使用与我们不同的维基百科转储，因此直接解决此任务并不简单。我们希望在未来的工作中解决这个问题。 F 空文档概率 我们尝试向 RAG 添加“空文档”机制，类似于 REALM [20]，以便对给定输入无法检索到有用信息的情况进行建模。

### 段落 120 · Page 18

**EN**

Here, ifk documents were retrieved, we would additionally "retrieve" an empty document and predict a logit for the null document, before marginalizing overk + 1 predictions. We explored modelling this null document logit by learning (i) a document embedding for the null document, (ii) a static learnt bias term, or (iii) a neural network to predict the logit. We did not ﬁnd that these improved performance, so in the interests of simplicity, we omit them.

**中文**

在这里，如果检索了 k 个文档，我们将另外“检索”一个空文档并预测空文档的 logit，然后再边缘化 overk + 1 预测。我们通过学习（i）空文档的文档嵌入，（ii）静态学习偏差项，或（iii）预测 logit 的神经网络来探索对空文档 logit 进行建模。我们没有发现这些改进了性能，因此为了简单起见，我们忽略了它们。

### 段落 121 · Page 18

**EN**

For Open MS-MARCO, where useful retrieved documents cannot always be retrieved, we observe that the model learns to always retrieve a particular set of documents for questions that are less likely to beneﬁt from retrieval, suggesting that null document mechanisms may not be necessary for RAG. G Parameters Our RAG models contain the trainable parameters for the BERT-base query and document encoder of DPR, with 110M parameters each (although we do not train the document encoder ourselves) and 406M trainable parameters from BART-large, 406M parameters, making a total of 626M trainable 18

**中文**

对于 Open MS-MARCO，有用的检索文档不能总是检索到，我们观察到该模型学会总是检索一组特定的文档，以解决不太可能从检索中受益的问题，这表明空文档机制对于 RAG 可能不是必需的。 G 参数 我们的 RAG 模型包含 DPR 的基于 BERT 的查询和文档编码器的可训练参数，每个参数有 110M 个参数（尽管我们自己不训练文档编码器）和来自 BART-large 的 406M 个可训练参数，406M 个参数，总共 626M 个可训练参数 18

### Page 19

### 段落 122 · Page 19

**EN**

Table 7: Number of instances in the datasets used. *A hidden subset of this data is used for evaluation Task Train Development Test Natural Questions 79169 8758 3611 TriviaQA 78786 8838 11314 WebQuestions 3418 362 2033 CuratedTrec 635 134 635 Jeopardy Question Generation 97392 13714 26849 MS-MARCO 153726 12468 101093* FEVER-3-way 145450 10000 10000 FEVER-2-way 96966 6666 6666 parameters. The best performing "closed-book" (parametric only) open-domain QA model is T5-11B with 11 Billion trainable parameters.

**中文**

表 7：所用数据集中的实例数量。 *此数据的隐藏子集用于评估 任务训练开发测试 自然问题 79169 8758 3611 TriviaQA 78786 8838 11314 WebQuestions 3418 362 2033 CuratedTrec 635 134 635 Jeopardy Question Generation 97392 13714 26849 MS-MARCO 153726 12468 101093* FEVER-3 路 145450 10000 10000 FEVER-2 路 96966 6666 6666 参数。性能最佳的“闭卷”（仅参数）开放域 QA 模型是 T5-11B，具有 110 亿个可训练参数。

### 段落 123 · Page 19

**EN**

The T5 model with the closest number of parameters to our models is T5-large (770M parameters), which achieves a score of 28.9 EM on Natural Questions [52], substantially below the 44.5 that RAG-Sequence achieves, indicating that hybrid parametric/nonparametric models require far fewer trainable parameters for strong open-domain QA performance. The non-parametric memory index does not consist of trainable parameters, but does consists of 21M 728 dimensional vectors, consisting of 15.3B values. These can be easily be stored at 8-bit ﬂoating point precision to manage memory and disk footprints.

**中文**

参数数量与我们的模型最接近的 T5 模型是 T5-large（770M 个参数），它在自然问题 [52] 上获得了 28.9 EM 的分数，远低于 RAG-Sequence 达到的 44.5，这表明混合参数/非参数模型需要更少的可训练参数来实现强大的开放域 QA 性能。非参数记忆索引不由可训练参数组成，而是由 21M 728 维向量组成，由 15.3B 个值组成。这些可以轻松地以 8 位浮点精度存储，以管理内存和磁盘占用空间。

### 段落 124 · Page 19

**EN**

H Retrieval Collapse In preliminary experiments, we observed that for some tasks such as story generation [ 11], the retrieval component would “collapse” and learn to retrieve the same documents regardless of the input. In these cases, once retrieval had collapsed, the generator would learn to ignore the documents, and the RAG model would perform equivalently to BART. The collapse could be due to a less-explicit requirement for factual knowledge in some tasks, or the longer target sequences, which could result in less informative gradients for the retriever.

**中文**

H 检索崩溃 在初步实验中，我们观察到，对于某些任务（例如故事生成[11]），检索组件将“崩溃”并学习检索相同的文档，而不管输入如何。在这些情况下，一旦检索崩溃，生成器将学会忽略文档，并且 RAG 模型的性能将与 BART 相同。崩溃可能是由于某些任务中对事实知识的要求不太明确，或者目标序列较长，这可能导致检索器的信息梯度较少。

### 段落 125 · Page 19

**EN**

Perez et al.[46] also found spurious retrieval results when optimizing a retrieval component in order to improve performance on downstream tasks. I Number of instances per dataset The number of training, development and test datapoints in each of our datasets is shown in Table 7. 19

**中文**

佩雷斯等人[46]在优化检索组件以提高下游任务的性能时，还发现了虚假的检索结果。 I 每个数据集的实例数 我们每个数据集中的训练、开发和测试数据点的数量如表 7 所示。 19
