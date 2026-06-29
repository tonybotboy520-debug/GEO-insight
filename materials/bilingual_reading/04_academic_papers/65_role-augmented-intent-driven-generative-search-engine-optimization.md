# Role-Augmented Intent-Driven Generative Search Engine Optimization

- ID: 65
- 类型: pdf
- 分类: 04_academic_papers
- 主题: intent-driven G-SEO method
- 原文链接: https://arxiv.org/pdf/2508.11158
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

1 Role-Augmented Intent-Driven Generative Search Engine Optimization Xiaolu Chen, Haojie Wu, Jie Bao, Zhen Chen, Yong Liao, and Hu Huang Abstract—Generative Search Engines (GSE), powered by Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG), is reshaping information retrieval. While commercial systems (e.g., BingChat, Perplexity.ai) demonstrate impressive semantic synthesis capabilities, their black-box nature fundamentally undermines established Search Engine Optimization (SEO) practices.

**中文**

1 角色增强型意图驱动生成式搜索引擎优化 Cheniaolu Chen、Haojie Wu、Jie Bao、Zhen Chen、Yong Liao 和 Hu Huang 摘要：由大型语言模型 (LLM) 和检索增强生成 (RAG) 提供支持的生成式搜索引擎 (GSE) 正在重塑信息检索。虽然商业系统（例如 BingChat、Perplexity.ai）展示了令人印象深刻的语义合成能力，但它们的黑盒性质从根本上破坏了现有的搜索引擎优化 (SEO) 实践。

### 段落 2 · Page 1

**EN**

Content creators face a critical challenge: their optimization strategies, effective in traditional search engines, are misaligned with generative retrieval contexts, resulting in diminished visibility. To bridge this gap, we propose a Role-Augmented Intent-Driven Generative Search Engine Optimization (G-SEO) method, providing a structured optimization pathway tailored for GSE scenarios. Our method models search intent through reflective refinement across diverse informational roles, enabling targeted content enhancement.

**中文**

内容创建者面临着严峻的挑战：他们的优化策略在传统搜索引擎中有效，但与生成检索上下文不一致，导致可见性降低。为了弥补这一差距，我们提出了一种角色增强的意图驱动生成式搜索引擎优化（G-SEO）方法，提供了针对 GSE 场景量身定制的结构化优化路径。我们的方法通过跨不同信息角色的反思性细化来对搜索意图进行建模，从而实现有针对性的内容增强。

### 段落 3 · Page 1

**EN**

To better evaluate the method under realistic settings, we address the benchmarking limitations of prior work by: (1) extending the GEO dataset with diversified query variations reflecting real-world search scenarios and (2) introducing G-EV AL 2.0, a 6-level LLM-augmented evaluation rubric for fine-grained human-aligned assessment. Experimental results demonstrate that search intent serves as an effective signal for guiding content optimization, yielding significant improvements over single-aspect baseline approaches in both subjective impressions and objective content visibility within GSE responses.

**中文**

为了更好地在现实环境下评估该方法，我们通过以下方式解决了先前工作的基准测试局限性：（1）通过反映真实世界搜索场景的多样化查询变体扩展 GEO 数据集，以及（2）引入 G-EV AL 2.0，这是一种用于细粒度人类对齐评估的 6 级 LLM 增强评估标准。实验结果表明，搜索意图是指导内容优化的有效信号，与单方面基线方法相比，在 GSE 响应中的主观印象和客观内容可见性方面都有显着改进。

### 段落 4 · Page 1

**EN**

1 Index Terms—Generative Search Engine Optimization, Prompt Engineering, Large Language Model, Natural Language Processing. I. INTRODUCTION Generative Search Engines (GSE), such as ChatGPT and Perplexity.ai, are rapidly transforming how users access and interact with information. By integrating Large Language Models (LLMs) with Retrieval-Augmented Generation (RAG) techniques, GSE inherit the precise retrieval capabilities of traditional search engines while introducing advanced semantic understanding and natural language generation.

**中文**

1 索引词——生成式搜索引擎优化、即时工程、大语言模型、自然语言处理。 I. 简介 生成式搜索引擎 (GSE)，例如 ChatGPT 和 Perplexity.ai，正在迅速改变用户访问信息和与信息交互的方式。通过将大型语言模型（LLM）与检索增强生成（RAG）技术相集成，GSE继承了传统搜索引擎的精确检索能力，同时引入了高级语义理解和自然语言生成。

### 段落 5 · Page 1

**EN**

This allows them to selectively synthesize multi-source information and deliver context-aware, comprehensive responses to user queries. However, this emerging paradigm introduces unprecedented challenges for content creators, such as bloggers, journalists, and web developers, whose work is increasingly surfaced through GSE. Operating as black boxes, GSE offer little transparency into how content is selected, aggregated, and Xiaolu Chen, Haojie Wu, Jie Bao, Zhen Chen, Yong Liao, and Hu Huang are with School of Cyber Science and Technology, University of Science and Technology of China, Hefei 230026, China.

**中文**

这使他们能够有选择地合成多源信息，并对用户查询提供上下文感知的全面响应。然而，这种新兴范式给博主、记者和网络开发人员等内容创作者带来了前所未有的挑战，他们的作品越来越多地通过 GSE 出现。 GSE 作为黑匣子运行，对于内容的选择和聚合方式几乎不透明。陈晓璐、吴浩杰、鲍杰、陈震、廖勇和黄虎就职于中国科学技术大学网络科学与技术学院，中国合肥 230026。

### 段落 6 · Page 1

**EN**

(Email: xiaoluchen@mail.ustc.edu.cn; hiwuu@mail.ustc.edu.cn; baojie1996@mail.ustc.edu.cn; zhenchen@ustc.edu.cn; yliao@ustc.edu.cn; huanghu@ustc.edu.cn) Zhen Chen is Corresponding author. 1Our code and dataset will be released upon the acceptance of the paper. surfaced. Consequently, creators struggle to understand how their content is interpreted, ranked, and either included or excluded from generated outputs. This opacity significantly hinders their ability to improve content visibility, often resulting in high-quality content being misrepresented, ignored, or even underutilized.

**中文**

(Email: xiaoluchen@mail.ustc.edu.cn; hiwuu@mail.ustc.edu.cn; baojie1996@mail.ustc.edu.cn; zhenchen@ustc.edu.cn; yliao@ustc.edu.cn; huanghu@ustc.edu.cn) 陈震，通讯作者。 1我们的代码和数据集将在论文被接受后发布。浮出水面。因此，创作者很难理解他们的内容是如何被解释、排名以及如何包含或排除在生成的输出中的。这种不透明性极大地阻碍了他们提高内容可见性的能力，常常导致高质量内容被歪曲、忽视，甚至未得到充分利用。

### 段落 7 · Page 1

**EN**

While some existing studies have attempted to enhance visibility through content rewriting or search engine optimization (SEO) techniques, these methods generally overlook the unique semantic generation logic of GSE. Traditional SEO strategies focus on surface-level signals such as keyword matching [9] and hyperlink structures [12], lacking the semantic granularity required to influence LLM-driven generation. Similarly, some rewriting models that rely on supervised finetuning tend to target task-specific improvements and struggle to generalize across diverse user queries.

**中文**

虽然一些现有的研究试图通过内容重写或搜索引擎优化（SEO）技术来增强可视性，但这些方法通常忽略了 GSE 独特的语义生成逻辑。传统的 SEO 策略侧重于关键字匹配 [9] 和超链接结构 [12] 等表面信号，缺乏影响 LLM 驱动生成所需的语义粒度。同样，一些依赖监督微调的重写模型倾向于针对特定任务的改进，并且很难在不同的用户查询中进行泛化。

### 段落 8 · Page 1

**EN**

[20], [24] Notably, both approaches fail to directly optimize for content visibility within GSE contexts. Prompt injection methods [11], [18] have emerged to steer GSE toward specific content, but they typically fall short of improving the structural or semantic quality of the source content and often lack robustness. GEO [1] offers a promising direction by introducing rewriting strategies to enhance content presentation, yet it remains limited in handling diverse search intents and lacks a systematic optimization framework.

**中文**

[20]、[24] 值得注意的是，这两种方法都无法直接优化 GSE 上下文中的内容可见性。提示注入方法 [11]、[18] 已经出现，可以引导 GSE 转向特定内容，但它们通常无法提高源内容的结构或语义质量，并且通常缺乏鲁棒性。 GEO [1] 通过引入重写策略来增强内容呈现，提供了一个有前途的方向，但它在处理多样化搜索意图方面仍然有限，并且缺乏系统的优化框架。

### 段落 9 · Page 1

**EN**

To address these limitations, we propose Role- Augmented Intent-Driven Generative Search Engine Optimization (RAID G-SEO), an intent-aware optimization framework tailored for the GSE black-box setting. Our method explicitly models user latent search intents and introduces a four-stage structured pipeline comprising content summarization, intent inference and refinement, step planning, and content rewriting.

**中文**

为了解决这些限制，我们提出了角色增强意图驱动生成式搜索引擎优化（RAID G-SEO），这是一个专为 GSE 黑盒设置量身定制的意图感知优化框架。我们的方法显式地对用户潜在搜索意图进行建模，并引入了一个四阶段结构化管道，包括内容摘要、意图推断和细化、步骤规划和内容重写。

### 段落 10 · Page 1

**EN**

To align content more closely with user needs, we incorporate a multi-role deep reflection mechanism that enables content creators to infer and refine likely search intents from their own authorial perspective, providing semantically coherent and actionable guidance for optimization. Furthermore, we extend the existing GEO benchmark with a diverse set of user queries to better simulate real-world GSE interactions. We also introduce G-EV AL 2.0, a multi-dimensional evaluation protocol enabling fairer and more granular assessments of content visibility in GSE outputs.

**中文**

为了使内容更紧密地与用户需求保持一致，我们采用了多角色深度反射机制，使内容创建者能够从自己的作者角度推断和细化可能的搜索意图，从而为优化提供语义连贯且可操作的指导。此外，我们通过一组不同的用户查询扩展了现有的 GEO 基准，以更好地模拟现实世界的 GSE 交互。我们还推出了 G-EVAL 2.0，这是一种多维评估协议，可以对 GSE 输出中的内容可见性进行更公平、更精细的评估。

### 段落 11 · Page 1

**EN**

Our contributions are summarized as follows: •We formalize the GSE black-box setting with unknown user queries and introduce RAID G-SEO, the first structured intent-aware optimization framework, which significantly boosts content visibility across diverse queries. •We design a deep reflection mechanism grounded in the 4W principle and multiple role perspectives, enabling arXiv:2508.11158v2 [cs.IR] 18 Mar 2026

**中文**

我们的贡献总结如下： •我们将未知用户查询的GSE黑盒设置形式化，并引入RAID G-SEO，这是第一个结构化意图感知优化框架，可显着提高跨不同查询的内容可见性。 •我们设计了一种基于4W原理和多角色视角的深度反射机制，使arXiv:2508.11158v2 [cs.IR] 2026年3月18日成为可能

### Page 2

### 段落 12 · Page 2

**EN**

2 Fig. 1. Overview of Generative Search Engine (GSE) workflow. Upon receiving a user query, the system retrieves a set of relevant documents and feeds them into the large language model (LLM) to generate a synthesized response with source-level citations. Optimized content may increase its likelihood of being cited in the final response. Notably, in the black-box setting assumed in this work, the query is not visible to content creators. creator-centric semantic intent refinement. •We extend the GEO benchmark and propose G-EV AL 2.0, enabling more granular and consistent subjective evaluations across diverse retrieval scenarios. II.

**中文**

2 图 1. 生成式搜索引擎 (GSE) 工作流程概述。收到用户查询后，系统会检索一组相关文档并将其输入大语言模型 (LLM)，以生成具有源级引用的综合响应。优化的内容可能会增加在最终回复中被引用的可能性。值得注意的是，在本工作中假设的黑盒设置中，查询对内容创建者不可见。以创作者为中心的语义意图细化。 •我们扩展了GEO基准并提出了G-EVAL 2.0，从而能够在不同的检索场景中进行更细粒度和一致的主观评估。二.

### 段落 13 · Page 2

**EN**

RELATEDWORK A. Traditional Search Engine Optimization Techniques Search Engine Optimization (SEO) has long served as a cornerstone for improving content visibility in traditional web search [2], [21]. It typically relies on both on-page and offpage factors, including web link structures [12], page rendering strategies [10], and keyword placement [9], to improve rankings on Search Engine Results Pages (SERPs). Recent advances in LLMs have enabled their use in generating SEOoptimized content, including product descriptions and metadata to enhance visibility [4], [19].

**中文**

相关工作 A. 传统搜索引擎优化技术 搜索引擎优化 (SEO) 长期以来一直是提高传统 Web 搜索内容可视性的基石 [2]、[21]。它通常依赖于页内和页外因素，包括网络链接结构 [12]、页面呈现策略 [10] 和关键字放置 [9]，以提高搜索引擎结果页面 (SERP) 的排名。 LLM 的最新进展使其能够用于生成 SEO 优化的内容，包括产品描述和元数据以增强可见性 [4]、[19]。

### 段落 14 · Page 2

**EN**

However, these approaches are highly dependent on observable signals (e.g., keyword relevance or link authority) , which become less effective in GSE contexts, where the content selection process is driven by semantic alignment and system-level preferences. B. Content Optimization Beyond traditional SEO, content rewriting has become a prominent direction in optimization, particularly in the era of LLMs. Several studies have leveraged instruction-tuned LLMs to generate fluent and semantically faithful rewrites, guided by diverse editing instructions [13], [24].

**中文**

然而，这些方法高度依赖于可观察的信号（例如，关键字相关性或链接权威），这些信号在 GSE 上下文中变得不太有效，其中内容选择过程由语义对齐和系统级偏好驱动。 B. 内容优化 除了传统的SEO之外，内容重写已经成为优化的一个突出方向，尤其是在LLM时代。一些研究利用指令调整的法学硕士在不同的编辑指令的指导下生成流畅且语义忠实的重写[13]、[24]。

### 段落 15 · Page 2

**EN**

Other work [5], [14], [20] incorporates implicit knowledge into prompts to steer generation toward personalization or task-specific objectives. However, these methods prioritize linguistic quality and personalization, they do not directly tackle visibility in GSE. GEO [1] is the first systematic effort targeting this problem, introducing GEO-BENCH, the first benchmark tailored for GSE scenarios, along with rule-based strategies that target semantic prominence. Despite its initial success, GEO is constrained by static rewrite patterns which lack adaptability to diverse query intents.

**中文**

其他工作 [5]、[14]、[20] 将隐性知识纳入提示中，以引导一代人实现个性化或特定任务的目标。然而，这些方法优先考虑语言质量和个性化，它们并不直接解决 GSE 中的可见性问题。 GEO [1] 是针对此问题的第一个系统性工作，引入了 GEO-BENCH（第一个为 GSE 场景量身定制的基准）以及针对语义突出性的基于规则的策略。尽管取得了初步成功，GEO 仍受到静态重写模式的限制，缺乏对不同查询意图的适应性。

### 段落 16 · Page 2

**EN**

Meanwhile, a line of work [3], [6], [11], [18], [22] explores prompt injection strategies to manipulate GSE responses, but these methods might compromise semantic coherence, raising concerns regarding safety and content integrity. In contrast to static rewriting or prompt injection, we propose a multi-stage optimization framework based on explicit search intent modeling and role-augmented reflective prompting. Instead of injecting adversarial or misleading prompts, we decompose search intent into actionable subgoals and align them with role-specific informational expectations.

**中文**

与此同时，一系列工作 [3]、[6]、[11]、[18]、[22] 探索了操纵 GSE 响应的提示注入策略，但这些方法可能会损害语义一致性，引发对安全性和内容完整性的担忧。与静态重写或提示注入相比，我们提出了一种基于显式搜索意图建模和角色增强反射提示的多阶段优化框架。我们没有注入对抗性或误导性的提示，而是将搜索意图分解为可操作的子目标，并将其与特定于角色的信息期望保持一致。

### 段落 17 · Page 2

**EN**

This enables targeted content enhancement that preserves semantic integrity while adaptively enhancing visibility under opaque and non-deterministic GSE behaviors. III. METHODOLOGY A. Blackbox Generative Search Egine Assumption In real-world deployments, GSE such as Google’s Search Generative Experience (SGE) and Perplexity.ai typically adopt LLM-based RAG architectures while remaining largely opaque to external observers. To contextualize our work, we describe a typical GSE workflow, as illustrated in Fig.1. Upon

**中文**

这使得有针对性的内容增强能够保持语义完整性，同时自适应地增强不透明和非确定性 GSE 行为下的可见性。三．方法 A. Blackbox 生成式搜索引擎假设 在实际部署中，GSE（例如 Google 的搜索生成体验 (SGE) 和 Perplexity.ai）通常采用基于 LLM 的 RAG 架构，同时对外部观察者基本上保持不透明。为了结合我们的工作背景，我们描述了一个典型的 GSE 工作流程，如图 1 所示。之上

### Page 3

### 段落 18 · Page 3

**EN**

3 Fig. 2. Overview of the Role-Augmented Intent-Driven G-SEO method. The method leverages search intent to guide the optimization process and further integrates reflection-based modeling from multiple roles to enhance generalizability to diverse user needs in complex GSE scenarios. receiving a user queryq, the system retrieves a set of relevant content sourcesC=Retrieval(q) ={c 1, c2, . . . , cN }from a corpus authored by diverse creators, including bloggers, journalists, encyclopedists, and government entities.

**中文**

3 图 2. 角色增强型意图驱动 G-SEO 方法概述。该方法利用搜索意图来指导优化过程，并进一步集成来自多个角色的基于反射的建模，以增强复杂 GSE 场景中不同用户需求的通用性。接收到用户查询q，系统检索一组相关内容源C=Retrieval(q)={c 1, c2,…。。。 , cN }来自不同创作者（包括博主、记者、百科全书和政府实体）创作的语料库。

### 段落 19 · Page 3

**EN**

The retrieved documents are then passed to an LLM to generate a natural language responser=generate(C, q)composed of a sequence of sentences{l s}m s=1. Each sentencel s is linked to one or more evidence citations referencing sources Ct ⊆C,1≤ |C t| ≤N. Our goal is to improve the visibility of a target content itemc i ∈Cwithin the final responserthrough content-level optimization. We adopt the visibility evaluation settings and metrics proposed in GEO-BENCH and further extend them to broader scenarios. Crucially, we consider a black-box setting where the queryqis hidden from content creators, posing a fundamental challenge for G-SEO.

**中文**

然后将检索到的文档传递给 LLM 以生成由句子序列 {l s}m s=1 组成的自然语言responser=generate(C, q)。每个句子 s 都链接到一个或多个引用来源的证据引用 Ct ⊆C,1≤ |C t| ≤N。我们的目标是通过内容级优化来提高最终响应者中目标内容项的可见性。我们采用GEO-BENCH中提出的可见性评估设置和指标，并将其进一步扩展到更广泛的场景。至关重要的是，我们考虑了一种黑盒设置，其中查询对内容创建者隐藏，这对 G-SEO 构成了根本性挑战。

### 段落 20 · Page 3

**EN**

To address this, we propose the RAID-GEO method as illustrated in Fig. 2, an intentdriven framework that infers the likely user intent from the creator’s perspective and guides content rewriting accordingly, thus increasing the likelihood that the content will be selected or cited in GSE-generated outputs. B. Intent-Driven Four-Phase Optimization Given the early-stage nature of G-SEO and the absence of a well-established paradigm, we draw critical inspiration from traditional SEO strategies to address this gap.

**中文**

为了解决这个问题，我们提出了如图 2 所示的 RAID-GEO 方法，这是一个意图驱动的框架，可以从创建者的角度推断可能的用户意图，并相应地指导内容重写，从而增加在 GSE 生成的输出中选择或引用内容的可能性。 B. 意图驱动的四阶段优化鉴于 G-SEO 的早期性质以及缺乏完善的范式，我们从传统 SEO 策略中汲取重要灵感来解决这一差距。

### 段落 21 · Page 3

**EN**

Although conventional approaches, such as those based on keyword tuning or webpage structure modifications [10], [17], [19], are not directly applicable to the semantics-driven generation process inherent to GSE, their underlying principle remains valuable: anticipate search intent and tailor content expression accordingly. Building on this insight, we introduce search intent as a semantic intermediary that bridges latent user needs and optimized content. In our framework, search intent is defined as the underlying informational motivation or objective implicitly embedded within a user’s query.

**中文**

尽管传统方法，例如基于关键词调整或网页结构修改的方法[10]、[17]、[19]，并不直接适用于 GSE 固有的语义驱动生成过程，但其基本原则仍然有价值：预测搜索意图并相应地定制内容表达。基于这种见解，我们引入搜索意图作为语义中介，连接潜在的用户需求和优化的内容。在我们的框架中，搜索意图被定义为隐式嵌入用户查询中的潜在信息动机或目标。

### 段落 22 · Page 3

**EN**

It serves as the semantic anchor guiding the trajectory and strategy of content optimization. Recent advances in prompt engineering have enabled LLMs to make significant progress in intent understanding [16], [25], [26], [31]. To operationalize these advances in the context of G-SEO, we propose a novel framework: Role-Augmented Intent-Driven Generative Search Engine Optimization (RAID G-SEO) which implements a four-stage optimization pipeline driven by inferred search intent. The core stages are outlined below: •Step 1: Content Summarization.

**中文**

它充当指导内容优化的轨迹和策略的语义锚。即时工程的最新进展使法学硕士在意图理解方面取得了重大进展[16]、[25]、[26]、[31]。为了在 G-SEO 的背景下实施这些进步，我们提出了一个新颖的框架：角色增强的意图驱动生成式搜索引擎优化（RAID G-SEO），它实现了由推断的搜索意图驱动的四阶段优化管道。核心阶段概述如下： • 步骤1：内容摘要。

### 段落 23 · Page 3

**EN**

We employ an LLM to conduct a semantically-focused summarization of the target content, using a constrained summarization prompt to suppress stylistic redundancy and semantic noise. This step enables the model to distill the content’s core informational focus as intended by the creator. As demonstrated in our ablation study, this summarization substantially improves the effectiveness of the downstream intent inference process. •Step 2: Intent Inference and Refinement. We adopt a twostage modeling approach to infer search intent. First, the LLM generates an initial intent representation based on the original content and its summary.

**中文**

我们采用法学硕士对目标内容进行以语义为中心的摘要，使用约束摘要提示来抑制文体冗余和语义噪声。此步骤使模型能够按照创建者的意图提取内容的核心信息焦点。正如我们的消融研究所证明的那样，这种总结大大提高了下游意图推断过程的有效性。 •步骤2：意图推断和细化。我们采用两阶段建模方法来推断搜索意图。首先，法学硕士根据原始内容及其摘要生成初始意图表示。

### 段落 24 · Page 3

**EN**

However, this initial form often reflects the creator’s subjective projection of user interest, which may not generalize across user populations. To address this, we introduce a 4W multirole deep reflection module, which enhances the initial intent via structured introspection from multiple user-role perspectives. Drawing inspiration from sociological decision frameworks, this module performs role-augmented, structured reasoning over four axes (Who, What, Why, How), guiding the model to reanalyze and refine the search intent toward broader user alignment. Details of this module are provided in the next section. •Step 3: Step Planning.

**中文**

然而，这种初始形式通常反映了创建者对用户兴趣的主观预测，这可能无法推广到所有用户群体。为了解决这个问题，我们引入了一个 4W 多角色深度反射模块，该模块通过从多个用户角色角度进行结构化内省来增强初始意图。该模块从社会学决策框架中汲取灵感，在四个轴（谁、什么、为什么、如何）上执行角色增强的结构化推理，指导模型重新分析和细化搜索意图，以实现更广泛的用户一致性。该模块的详细信息将在下一节中提供。 •步骤3：步骤规划。

### 段落 25 · Page 3

**EN**

To minimize semantic drift during content rewriting, we prompt the model with the refined intent and instruct it to generate a sequence of explicit and interpretable optimization steps. This prompt-based planning decomposes the semantic intent into actionable revision strategies, enabling controllability and ensuring that subsequent edits preserve the intended semantic core. •Step 4: Content Rewriting. Following the planned steps, the model conducts intent-aligned rewriting to improve both semantic alignment and retrieval effectiveness.

**中文**

为了最大限度地减少内容重写过程中的语义漂移，我们用精炼的意图提示模型，并指示它生成一系列显式且可解释的优化步骤。这种基于提示的规划将语义意图分解为可操作的修订策略，从而实现可控性并确保后续编辑保留预期的语义核心。 •第四步：内容重写。按照计划的步骤，模型进行意图对齐的重写，以提高语义对齐和检索效率。

### 段落 26 · Page 3

**EN**

By enforcing consistency with the inferred intent and adhering to the step plan, the rewritten content achieves higher relevance and compatibility with potential user queries, especially under black-box GSE settings where query visibility is unavailable. Our RAID G-SEO framework is specifically designed to address the query-invisible nature of black-box GSE systems. By modeling latent user intent as a mediating signal and optimizing content from the creator’s perspective, our method provides a principled and structured optimization path.

**中文**

通过强制与推断意图的一致性并遵守步骤计划，重写的内容与潜在用户查询实现了更高的相关性和兼容性，特别是在查询可见性不可用的黑盒 GSE 设置下。我们的 RAID G-SEO 框架专为解决黑盒 GSE 系统的查询不可见性质而设计。通过将潜在用户意图建模为中介信号并从创建者的角度优化内容，我们的方法提供了原则性和结构化的优化路径。

### 段落 27 · Page 3

**EN**

This approach effectively mitigates semantic misalignment between content expression and user retrieval motivations, thereby

**中文**

这种方法有效地减轻了内容表达和用户检索动机之间的语义错位，从而

### Page 4

### 段落 28 · Page 4

**EN**

4 TABLE I OVERVIEW OFCOREPROMPTSUSED INRAID G-SEO Core Prompts of RAID G-SEO You will be given a source of web content. ### Your Task Content Summarization: Summarize the source clearly and concisely by extracting the key information and main points, avoiding irrelevant details, to make it understandable for readers who have not seen the original. Intent Inference: Carefully analyze the summary and identify the primary search intent. 4W multi-role deep reflection module: Reflect the intent from multiple role perspectives: - Think about 1-3 roles that are most likely associated with the intent.

**中文**

4 表 I RAID G-SEO 中使用的核心提示概述 RAID G-SEO 的核心提示 您将获得 Web 内容源。 ### 你的任务内容摘要：通过提取关键信息和要点，清晰、简洁地总结出处，避免不相关的细节，使没有看过原文的读者也能理解。意图推断：仔细分析摘要并确定主要搜索意图。 4W多角色深度反思模块：从多个角色角度反映意图： - 思考最有可能与意图相关的1-3个角色。

### 段落 29 · Page 4

**EN**

- Consider the core needs for each role, given their/its occupational backgrounds and knowledge. - Briefly analyze any potential mismatches between the primary intent and these role-specific needs. - Based on above insights, summarize a refined intent covering the core needs of all roles. If the original intent is already precise and sufficient, keep it unchanged. The output should only include the generalized intent without any additional explanations or analysis. Step Planning: Based on the intents, determine the best optimization strategy from multiple angles to increase visibility and user engagement.

**中文**

- 根据每个角色的职业背景和知识，考虑其核心需求。 - 简要分析主要意图和这些特定于角色的需求之间任何潜在的不匹配。 - 根据上述见解，总结出涵盖所有角色核心需求的精炼意图。如果初衷已经明确、充分，就保持不变。输出应仅包含一般意图，而无需任何额外的解释或分析。步骤规划：根据意图，从多个角度确定最佳优化策略，以提高可见性和用户参与度。

### 段落 30 · Page 4

**EN**

Prioritize the primary intent, while using the generalized intent for minor adjustments. Content Rewriting: Follow the above optimization steps to optimize the source, ensuring the core meaning and key information of the source remains unchanged. The output should only include the optimized source without any additional explanations or analysis. ### Input Format Original Source:{...} Source Summary:{...} ... ### Output Format Generalized Intent: [...] Optimized Source: [...] ... improving the adaptability and visibility of content across diverse GSE scenarios. C.

**中文**

优先考虑主要意图，同时使用广义意图进行细微调整。内容重写：按照上述优化步骤对源码进行优化，保证源码的核心含义和关键信息不变。输出应仅包含优化后的源，无需任何额外的解释或分析。 ### 输入格式 原始来源：{...} 来源摘要：{...} ... ### 输出格式 通用意图：[...] 优化来源：[...] ... 提高内容在不同 GSE 场景中的适应性和可见性。 C.

### 段落 31 · Page 4

**EN**

4W Multi-Role Deep Reflection To address the heterogeneity of user groups in diverse retrieval scenarios, it is essential to enhance the generalizability of search intent representation, enabling it to cover a broader spectrum of potential information needs. In the black-box setting of G-SEO, where creators lack direct access to user queries, we introduce a LLM-driven reflection mechanism to expand the semantic boundaries of the initially inferred intent. Reflection strategies have demonstrated efficacy in improving LLM performance across a variety of tasks [8], [23], especially in multi-perspective reflection paradigms [28], [29].

**中文**

4W多角色深度反思为了解决不同检索场景下用户群体的异质性，必须增强搜索意图表示的泛化性，使其能够覆盖更广泛的潜在信息需求。在 G-SEO 的黑盒设置中，创建者无法直接访问用户查询，我们引入了 LLM 驱动的反射机制来扩展最初推断意图的语义边界。反思策略已证明可以有效提高法学硕士在各种任务中的表现[8]、[23]，特别是在多视角反思范式中[28]、[29]。

### 段落 32 · Page 4

**EN**

These studies highlight LLMs’ capacity to simulate diverse cognitive roles and to construct alternative reasoning trajectories. However, most existing approaches rely on intuition-driven human-like reflection, lacking formal cognitive structure and scientific grounding. As such, they fall short in achieving the dual objective of semantic consistency and expressive breadth, both of which are essential for robust intent generalization in complex tasks. To overcome these limitations, we draw inspiration from sociological theories of problem framing and decision-making [27], [30].

**中文**

这些研究强调了法学硕士模拟不同认知角色和构建替代推理轨迹的能力。然而，大多数现有方法依赖于直觉驱动的类人反思，缺乏正式的认知结构和科学基础。因此，它们无法实现语义一致性和表达广度的双重目标，而这两者对于复杂任务中稳健的意图泛化至关重要。为了克服这些局限性，我们从问题框架和决策的社会学理论中汲取灵感[27]，[30]。

### 段落 33 · Page 4

**EN**

Specifically, we tailor this perspective to the G- SEO context by incorporating WH-analysis principles, which guide the model in decomposing and refining search intent from four critical dimensions: Who, What, Why, and How. In particular, the Who offers a multi-perspective lens, while intermediate outputs of the What and Why serve as constraints and guidance signals in the semantic reconstruction process of the How. This promotes intent representations that are both aligned and diversified. This forms the foundation of our multirole reflective framework, enabling LLMs to reinterpret the initial intent through augmented user-role reasoning.

**中文**

具体来说，我们通过结合 WH 分析原则来根据 G-SEO 背景定制此视角，该原则指导模型从四个关键维度分解和细化搜索意图：谁、什么、为什么和如何。特别是，“谁”提供了多视角镜头，而“什么”和“为什么”的中间输出则在“如何”的语义重建过程中充当约束和指导信号。这促进了意图表达的一致性和多样化。这构成了我们多角色反思框架的基础，使法学硕士能够通过增强的用户角色推理重新解释最初的意图。

### 段落 34 · Page 4

**EN**

The 4W framework operates as follows: •Who is likely to retrieve this content? To balance generalization and precision, we prompt the LLM to infer a set of representative user roles most likely to search for the content (e.g., technical professionals, general readers, or decision-makers), based on the initial intent. •What are their retrieval needs? For each inferred user role, the model conditions intent generation on their domain background and knowledge profile, producing candidate motivations and search goals.

**中文**

4W 框架的运作方式如下： • 谁可能检索该内容？为了平衡泛化性和精确性，我们提示法学硕士根据最初的意图推断出一组最有可能搜索内容的代表性用户角色（例如，技术专业人员、普通读者或决策者）。 •他们的检索需求是什么？对于每个推断的用户角色，模型会根据其领域背景和知识概况来生成意图，从而产生候选动机和搜索目标。

### 段落 35 · Page 4

**EN**

By embedding role-specific constraints, uncontrolled semantic drift is limited to ensure higher factual alignment between generated intent and plausible needs. •Why does the initial intent misalign with their needs? The

**中文**

通过嵌入特定于角色的约束，不受控制的语义漂移受到限制，以确保生成的意图和合理的需求之间更高的事实一致性。 •为什么最初的意图与他们的需求不一致？这

### Page 5

### 段落 36 · Page 5

**EN**

5 TABLE II SAMPLE ORIGINAL QUERIES FROMGEO-BENCHAND THEIR FOURGPT-4–GENERATED VARIANTS Original Query Generated Queries Eastings 1) Applications of eastings in map reading 2) Historical development of eastings and northings in cartography 3) Comparison between eastings/northings and latitude/longitude systems 4) Innovations in digital mapping using eastings Who sings summer wine with lana del rey 1) History of the song Summer Wine 2) Impact of Lana Del Rey on modern music 3) Other famous duets similar to Summer Wine 4) Barrie-James O’Neill’s musical career after Summer Wine The most recent technological change to the u.s.

**中文**

5 表 II 来自 GEO-BENCH 的原始查询示例及其 FOURGPT-4 生成的变体 原始查询 生成的查询 东距 1) 东距在地图阅读中的应用 2) 东距和北距在制图学中的历史发展 3) 东距/北距和纬度/经度系统之间的比较 4) 使用东距的数字测绘创新lana del rey 1) 《Summer Wine》歌曲的历史 2) Lana Del Rey 对现代音乐的影响 3) 其他与《Summer Wine》类似的著名二重唱 4) Barrie-James O’Neill 在《Summer Wine》之后的音乐生涯 美国最新的技术变革

### 段落 37 · Page 5

**EN**

economy was 1) What are the implications of the most recent technological change on the U.S. economy? 2) What industries in the U.S. have been most affected by the recent technological change? 3) What are the opposing views on the impact of the most recent technological change on the U.S. economy? 4) What are the potential future trends in technology that could further impact the U.S. economy? Schedule a car service appointment for next week 1) How to prepare your car for a service appointment 2) Best practices for maintaining your vehicle between service appointments 3) Comparing dealership service vs.

**中文**

经济是 1) 最近的技术变革对美国经济有何影响？ 2) 美国哪些行业受近期技术变革影响最大？ 3) 对于最近的技术变革对美国经济的影响，有哪些相反的观点？ 4) 未来可能进一步影响美国经济的潜在技术趋势是什么？安排下周的汽车服务预约 1) 如何为服务预约准备您的汽车 2) 在服务预约之间维护车辆的最佳实践 3) 经销商服务与经销商服务的比较

### 段落 38 · Page 5

**EN**

independent auto shops for car maintenance 4) The impact of regular car service on vehicle longevity and resale value Should college education be free for all? 1) What are the potential economic impacts of free college education? 2) How does free college education affect the quality of education? 3) What are the arguments against free college education? 4) What are the latest developments in countries with free college education? model is tasked with identifying semantic gaps between the original intent and each role-specific need, followed by an explanation of the misalignment causes.

**中文**

独立的汽车维修店进行汽车维修 4) 定期汽车保养对车辆寿命和转售价值的影响 大学教育应该对所有人免费吗？ 1) 免费大学教育的潜在经济影响是什么？ 2）免费大学教育如何影响教育质量？ 3）反对免费大学教育的论点是什么？ 4）免费大学教育国家的最新进展是什么？模型的任务是识别原始意图和每个角色特定需求之间的语义差距，然后解释不一致的原因。

### 段落 39 · Page 5

**EN**

This step enables targeted and directed generalization, rather than generic expansion. •How should the initial intent be generalized? Leveraging the structured reflection outputs from the prior steps, we instruct the model via prompt-based reasoning to semantically reconstruct the initial intent. The refined version preserves the core informational focus while expanding its scope and adaptability across user contexts. Importantly, the entire reflection process is fully automated via prompt-based reasoning, requiring no human annotation or intervention, which ensures scalability across GSE settings.

**中文**

此步骤实现有针对性和定向的泛化，而不是泛型扩展。 • 应如何概括最初的意图？利用先前步骤的结构化反射输出，我们通过基于提示的推理来指导模型在语义上重建初始意图。改进后的版本保留了核心信息焦点，同时扩展了其范围和跨用户上下文的适应性。重要的是，整个反射过程通过基于提示的推理完全自动化，不需要人工注释或干预，这确保了跨 GSE 设置的可扩展性。

### 段落 40 · Page 5

**EN**

Through the 4W multi-role deep reflection module, we derive intent representations that maintain semantic coherence while effectively generalizing to diverse retrieval scenarios. The enhanced intent serves as a robust foundation for downstream G-SEO optimization, allowing the final content to achieve higher alignment with latent user queries.

**中文**

通过 4W 多角色深度反射模块，我们得到了保持语义一致性的意图表示，同时有效地推广到不同的检索场景。增强的意图为下游 G-SEO 优化奠定了坚实的基础，使最终内容能够与潜在用户查询实现更高的一致性。

### 段落 41 · Page 5

**EN**

We presents the core prompts used in the RAID G-SEO framework in Table I, covering two core components: the intent-driven four-phase framework (including Content Summarization, Intent Inference and Refinement, Step Planning, and Content Rewriting) and the 4W multi-role deep reflection module (Who, What, Why, How). All prompts are structurally organized by functional stage to facilitate understanding of the model’s reasoning process and ensure reproducibility of experimental settings. IV. EXPERIMENTS A.

**中文**

我们在表1中展示了RAID G-SEO框架中使用的核心提示，涵盖两个核心组件：意图驱动的四阶段框架（包括内容摘要、意图推理和细化、步骤规划和内容重写）和4W多角色深度反思模块（Who、What、Why、How）。所有提示均按功能阶段进行结构组织，以方便理解模型的推理过程并确保实验设置的可重复性。四．实验A.

### 段落 42 · Page 5

**EN**

Experimental Setup To ensure reproducibility and fairness, full generation configurations (e.g., sampling strategy, temperature, top-p) are included in Appendix C. 1) Generative Search Engine Simulation:We adopt the same setting as in GEO [1] to simulate the GSE environment, assuming a single-turn response generation task. In this setting, for each query, only five relevant content sources are accessible for response generation.

**中文**

实验设置为了确保可重复性和公平性，附录C中包含了完整的生成配置（例如采样策略、温度、top-p）。 1）生成式搜索引擎模拟：我们采用与GEO[1]中相同的设置来模拟GSE环境，假设单轮响应生成任务。在此设置中，对于每个查询，只有五个相关内容源可用于生成响应。

### 段落 43 · Page 5

**EN**

We employ the open-source GLM- 4-9B-0414 model, which exhibits a lower hallucination rate as reported in the Hallucination Leaderboard [7], and adopt answer generation prompts and sampling settings consistent with the prior work to minimize statistical bias. 2) Dataset:Building upon GEO-BENCH [1], we construct an extended version to better simulate diverse retrieval scenarios.

**中文**

我们采用开源 GLM-4-9B-0414 模型，如幻觉排行榜 [7] 中报告的那样，该模型表现出较低的幻觉率，并采用与之前的工作一致的答案生成提示和采样设置，以最大限度地减少统计偏差。 2）数据集：在GEO-BENCH [1]的基础上，我们构建了一个扩展版本，以更好地模拟不同的检索场景。

### 段落 44 · Page 5

**EN**

GEO-BENCH is a comprehensive benchmark for evaluating G-SEO methods, comprising real-world user queries collected from production systems such as Bing, Google, and Perplexity, as well as complex reasoning and debate-oriented questions, and a subset of synthetic queries generated by LLMs like GPT-4. To further enhance coverage across varied information needs, we use GPT-4 to generate four semantically related variants for each original query. This yields simulated retrieval samples, each consisting of five related queries and a corresponding group of five content sources. Each generated

**中文**

GEO-BENCH 是评估 G-SEO 方法的综合基准，包括从 Bing、Google 和 Perplexity 等生产系统收集的真实用户查询，以及复杂的推理和辩论导向的问题，以及由 GPT-4 等 LLM 生成的合成查询的子集。为了进一步增强对不同信息需求的覆盖，我们使用 GPT-4 为每个原始查询生成四个语义相关的变体。这会生成模拟检索样本，每个样本由五个相关查询和相应的一组五个内容源组成。每个生成的

### Page 6

### 段落 45 · Page 6

**EN**

6 variant shares only 1–2 keywords with the original query, and the average cosine similarity between variants and originals is 0.33, ensuring that generated queries preserve semantic relevance while maintaining diversity. Detailed generation prompts are provided in Appendix B. To ensure data quality, we performed human validation on 20% of the generated samples. Each sample was independently assessed by two annotators for relevance and logical consistency using a 1–5 scoring scale (1 = lowest, 5 = highest). All sampled queries received scores≥3, with a Cohen’s Kappa of 0.62, indicating high inter-annotator agreement.

**中文**

6变体与原始查询仅共享1-2个关键字，变体与原始查询之间的平均余弦相似度为0.33，确保生成的查询在保持多样性的同时保留语义相关性。附录 B 中提供了详细的生成提示。为了确保数据质量，我们对 20% 的生成样本进行了人工验证。每个样本均由两名注释者使用 1-5 评分量表（1 = 最低，5 = 最高）独立评估相关性和逻辑一致性。所有抽样查询的得分均≥3，Cohen’s Kappa 为 0.62，表明注释者间的一致性较高。

### 段落 46 · Page 6

**EN**

The evaluation confirms that the generated data maintain high semantic relevance and logical consistency. Table II presents a subset of generated samples to illustrate data quality. For each experiment, we randomly select 100 samples to evaluate model performance, ensuring robustness. This design retains the original characteristics of GEO-bench while introducing variant queries and diverse content sources to simulate more complex retrieval scenarios, providing a comprehensive benchmark for G-SEO evaluation.

**中文**

评估证实生成的数据保持了较高的语义相关性和逻辑一致性。表 II 提供了生成样本的子集，以说明数据质量。对于每个实验，我们随机选择 100 个样本来评估模型性能，确保稳健性。该设计保留了GEO-bench原有的特点，同时引入变体查询和多样化的内容源来模拟更复杂的检索场景，为G-SEO评估提供全面的基准。

### 段落 47 · Page 6

**EN**

3) Baselines:For task consistency and fair comparison, we do not include general text rewriting methods such as RewriteLM [24] or intent discovery methods such as Auto- Intent [31] as baselines. These methods are primarily designed for general text generation or intent prediction tasks, and their optimization objectives, input-output formats, and evaluation protocols differ significantly from those of the G-SEO task. Specifically, G-SEO aims to optimize the visibility and performance of content within generative search engines, rather than generating text itself or predicting user intent.

**中文**

3）基线：为了任务一致性和公平比较，我们不包括一般文本重写方法（例如RewriteLM [24]）或意图发现方法（例如Auto-Intent [31]）作为基线。这些方法主要是为一般文本生成或意图预测任务而设计的，其优化目标、输入输出格式和评估协议与G-SEO任务有很大不同。具体来说，G-SEO 旨在优化生成式搜索引擎中内容的可见性和性能，而不是生成文本本身或预测用户意图。

### 段落 48 · Page 6

**EN**

Consequently, without introducing additional task assumptions or complex adaptation mechanisms, it is non-trivial to achieve a direct and fair comparison. To ensure comparability and the validity of our conclusions, we adopt the nine optimization methods proposed by GEO [1], which are explicitly designed for the G-SEO task, as our baseline. Traditional SEO improves the likelihood that content will be retrieved and cited by inserting relevant keywords. The distinctive word optimization method rewrites text using rare or unique lexical items to enhance content recognizability.

**中文**

因此，在不引入额外的任务假设或复杂的适应机制的情况下，实现直接和公平的比较并非易事。为了确保我们的结论的可比性和有效性，我们采用 GEO [1] 提出的九种优化方法作为我们的基线，这些方法是专门为 G-SEO 任务设计的。传统的搜索引擎优化通过插入相关关键字来提高内容被检索和引用的可能性。独特的单词优化方法使用罕见或独特的词汇项目重写文本，以增强内容的可识别性。

### 段落 49 · Page 6

**EN**

Authority-based, fluency-based, and simplification-based optimization methods enhance textual expression in term of credibility, readability, and fluency. Beyond these, terminology-based, reputation-based, quotation-based, and statistics-based optimization methods incorporate factual or semi-factual natural language elements (e.g. specific terms, references to reputable reports, quotes from influential figures, and quantitative data) into the content. While these augmentations are not strictly required to be verifiable, they must remain contextually plausible and logically coherent.

**中文**

基于权威性、流畅性和简化性的优化方法增强了文本表达的可信度、可读性和流畅性。除此之外，基于术语、基于声誉、基于引用和基于统计的优化方法将事实或半事实的自然语言元素（例如特定术语、对信誉良好的报告的引用、有影响力的人物的引用和定量数据）纳入内容中。虽然这些增强并不严格要求可验证，但它们必须保持上下文合理且逻辑连贯。

### 段落 50 · Page 6

**EN**

All baseline methods, along with our proposed intent-driven optimization method, are implemented using the same model (GLM-4- 9B) and evaluated under identical procedures to ensure a fair comparison by eliminating model-induced variance. •Lexical strategies: Traditional SEO and distinctive word optimization, which enhance visibility through keyword insertion and rare lexical choices. •Expression enhancements: Authority-, fluency-, and simplification-based methods that improve content credibility, clarity, and readability.

**中文**

所有基线方法以及我们提出的意图驱动优化方法均使用相同的模型 (GLM-4-9B) 实施，并在相同的程序下进行评估，以通过消除模型引起的方差来确保公平比较。 •词汇策略：传统的SEO和独特的词优化，通过关键词插入和罕见的词汇选择来提高可见性。 •表达增强：基于权威、流畅和简化的方法，提高内容的可信度、清晰度和可读性。

### 段落 51 · Page 6

**EN**

•Content enrichment: Terminology-, reputation-, quotation-, and statistics-based methods that incorporate factual or semi-factual elements (e.g., domain-specific terms, reputable sources, quotations, and quantitative evidence) while remaining contextually plausible. All baselines and our proposed intent-driven method are implemented using GLM-4-9B and evaluated under identical conditions. 4) Evaluation Metrics:We adopt the evaluation metrics defined in GEO-BENCH [1] to perform objective and subjective assessments of G-SEO methods by measuring impressionbased improvements before and after content optimization.

**中文**

•内容丰富：基于术语、声誉、引文和统计的方法，纳入事实或半事实元素（例如，特定领域术语、信誉良好的来源、引文和定量证据），同时保持上下文合理性。所有基线和我们提出的意图驱动方法均使用 GLM-4-9B 实施，并在相同条件下进行评估。 4）评估指标：我们采用GEO-BENCH [1]中定义的评估指标，通过测量内容优化前后基于印象的改进来对G-SEO方法进行客观和主观评估。

### 段落 52 · Page 6

**EN**

For objective evaluation, Position-Adjusted Word Count (PAWC) is used, which considers both the frequency and relative positions of cited words by assigning higher weights to those appearing earlier and cited more frequently in the response. For subjective evaluation, we follow the Subjective Impression metric, covering seven dimensions: relevance, fluency, diversity, uniqueness, click-follow likelihood, subjective positional prominence, and subjective content volume.

**中文**

为了进行客观评估，使用位置调整字数（PAWC），它通过为响应中出现较早且引用频率较高的单词分配较高的权重来考虑引用单词的频率和相对位置。对于主观评估，我们遵循主观印象指标，涵盖七个维度：相关性、流畅性、多样性、独特性、点击关注可能性、主观位置突出性和主观内容量。

### 段落 53 · Page 6

**EN**

Although GEO originally used G-EV AL [15] to simulate human subjective judgment, its evaluation prompts demonstrate inconsistent scoring granularity and ambiguous criteria across dimensions, which may affect the stability of cross-method comparisons. To improve the consistency and accuracy of the scoring criteria, we introduce a prompt-generate-prompt strategy to formalize the scoring rubric. For each dimension, we define a 0–5 scale, where 0 indicates the target citation is completely omitted from the response, and 5 denotes optimal performance with respect to the evaluated criterion.

**中文**

尽管GEO最初使用G-EVAL[15]来模拟人类主观判断，但其评估提示表现出评分粒度不一致和跨维度标准不明确，这可能会影响跨方法比较的稳定性。为了提高评分标准的一致性和准确性，我们引入了提示-生成-提示策略来形式化评分标准。对于每个维度，我们定义一个 0-5 的等级，其中 0 表示目标引用从响应中完全省略，5 表示相对于评估标准的最佳表现。

### 段落 54 · Page 6

**EN**

This refinement focuses solely on unifying and clarifying the scoring scales and strictly follows the original G-EV AL chain-of-thought–based formfilling evaluation procedure, whose alignment with human judgments has been validated in prior work [15]. The evaluation prompts are generated by GPT-4o, and the scoring process is carried out using GLM-4-9B. The prompt-generation prompt and dimension-specific template are provided in Appendix B, and the subjective impression evaluation procedure can be found in Appendix C, respectively. To quantify relative improvements, we normalize and smooth the visibility scores.

**中文**

这种改进仅侧重于统一和澄清评分量表，并严格遵循原始的基于 G-EV AL 思想链的表格填写评估程序，其与人类判断的一致性已在先前的工作中得到验证[15]。评估提示由GPT-4o生成，评分过程使用GLM-4-9B进行。附录B中提供了提示生成提示和维度特定模板，附录C中分别提供了主观印象评估程序。为了量化相对改进，我们对可见性分数进行标准化和平滑化。

### 段落 55 · Page 6

**EN**

Specifically, for each cited sourceC i, its relative visibility gain from the original responserto the optimizedr ′ is computed is computed as shown in Eq. (1), where impr denotes the specific objective or subjective impression score of citationC i. As this work aims to examine the feasibility and effectiveness of G-SEO methods in improving content visibility within GSE scenarios, rather than to derive statistically generalizable conclusions, we report results averaged over multiple randomized runs to mitigate randomness and do not perform additional statistical significance tests.

**中文**

具体来说，对于每个引用的源C i，计算其从原始响应r到优化r'的相对可见度增益，如等式1所示。 (1)，其中impr表示引用C i 的具体客观或主观印象得分。由于这项工作的目的是检查 G-SEO 方法在提高 GSE 场景中内容可见性方面的可行性和有效性，而不是得出统计上可概括的结论，因此我们报告了多次随机运行的平均结果，以减轻随机性，并且不执行额外的统计显着性测试。

### 段落 56 · Page 6

**EN**

improvementCi = imprCi (r′)−impr Ci (r) imprCi (r) + 1 ×10(1) Details regarding the evaluation procedure and implementation are provided in Appendix E. B. Results and Analysis

**中文**

ImproveCi = imprCi (r′)−impr Ci (r) imprCi (r) + 1 ×10(1) 有关评估程序和实施的详细信息，请参阅附录 E。 B. 结果和分析

### Page 7

### 段落 57 · Page 7

**EN**

7 TABLE III OBJECTIVE AND SUBJECTIVE PERFORMANCES OFG-SEOMETHODS ON THE EXPANDEDGEO-BENCH Method Objective Impression(PAWC) Subjective Impression Word Count Posi. CountOver. Rele. Infl. Uniq. Dive. Clic. Sub.Posi. Sub.V olu.Aver. Tran. SEO 1.27 0.26 0.77 2.06 1.99 6.73 2.56 0.88 1.68 4.12 2.06 Uniq. Word -10.40 -10.32 -10.77 -6.28 -3.05 -7.87 -3.40 -7.66 -4.40 -5.23 -6.02 Simp. Expr. -8.78 -9.62 -9.52 -0.68 -0.34 6.23 -0.37 -0.72 -1.27 -0.67 -0.66 Auth. Expr. 13.10 13.33 12.86 3.14 2.85 19.36 2.49 5.11 2.75 6.60 4.82 Flue. Expr. 15.80 16.16 16.84 1.37 3.41 17.80 1.35 4.08 1.86 6.45 3.95 Term. Addi.

**中文**

7 表 III G-SEO 方法在 EXPANDEDGEO-BENCH 方法上的客观和主观表现 客观印象 (PAWC) 主观印象 字数 位置。倒计时。相关。膨胀。独特。潜水。克利克。子Posi。亚卷平均。特兰.搜索引擎优化 1.27 0.26 0.77 2.06 1.99 6.73 2.56 0.88 1.68 4.12 2.06字 -10.40 -10.32 -10.77 -6.28 -3.05 -7.87 -3.40 -7.66 -4.40 -5.23 -6.02 简单。表达式。 -8.78 -9.62 -9.52 -0.68 -0.34 6.23 -0.37 -0.72 -1.27 -0.67 -0.66 授权表达式。 13.10 13.33 12.86 3.14 2.85 19.36 2.49 5.11 2.75 6.60 4.82 烟道。表达式。 15.80 16.16 16.84 1.37 3.41 17.80 1.35 4.08 1.86 6.45 3.95阿迪。

### 段落 58 · Page 7

**EN**

16.04 15.94 15.51 5.00 4.45 23.36 3.04 7.74 5.47 10.61 7.13 Repu. Addi. 14.47 14.68 14.90 5.89 3.83 14.68 2.12 6.64 3.26 6.39 5.04 Quot. Addi. 24.70 27.03 26.20 6.38 5.31 24.77 4.07 10.07 7.16 10.24 8.23 Stat. Addi. 22.53 23.09 23.17 4.72 2.90 29.04 0.63 7.35 3.25 8.21 6.33 RAID G-SEO 15.05 16.94 15.79 9.25 8.80 39.71 7.51 14.63 10.46 16.28 13.27 1) Main Result:We conducted a comprehensive evaluation of RAID G-SEO against nine representative optimization baselines from GEO [1], with the results summarized in Table. III. The best-performing method for each metric is in bold and the second isunderlined.

**中文**

16.04 15.94 15.51 5.00 4.45 23.36 3.04 7.74 5.47 10.61 7.13阿迪。 14.47 14.68 14.90 5.89 3.83 14.68 2.12 6.64 3.26 6.39 5.04阿迪。 24.70 27.03 26.20 6.38 5.31 24.77 4.07 10.07 7.16 10.24 8.23阿迪。 22.53 23.09 23.17 4.72 2.90 29.04 0.63 7.35 3.25 8.21 6.33 RAID G-SEO 15.05 16.94 15.79 9.25 8.80 39.71 7.51 14.63 10.46 16.28 13.27 1) 主要结果：我们针对 GEO [1] 的九个代表性优化基线对 RAID G-SEO 进行了全面评估，结果总结在表中。三．每个指标的最佳执行方法以粗体显示，第二个方法以下划线显示。

### 段落 59 · Page 7

**EN**

As both Objective impression Improvement and Subjective Impression Improvement consist of multiple sub-metrics, we report the overall score of the former and the average score of the latter as the main comparative indicators, following the original GEO-BENCH evaluation protocol to ensure fair and consistent comparison across methods. From an overall perspective, RAID G-SEO demonstrates consistently strong performance, substantially outperforming the average of all competing methods.

**中文**

由于客观印象改善和主观印象改善均由多个子指标组成，因此我们将前者的总分和后者的平均分作为主要比较指标，遵循原有的GEO-BENCH评估协议，以确保不同方法之间的公平和一致的比较。从整体角度来看，RAID G-SEO 表现出了一贯的强劲性能，大大超过了所有竞争方法的平均水平。

### 段落 60 · Page 7

**EN**

In particular, it achieves improvement scores of 15.79 on Objective Impression Improvement Overall and 13.27 on Subjective Impression Improvement Average, corresponding to relative gains of 57.98% and 286.91% over the baseline average, respectively. These results indicate that RAID G-SEO is highly effective in enhancing both overall content visibility and user-perceived quality in generative search scenarios, with especially pronounced advantages on subjective impression metrics that capture user attractiveness.

**中文**

特别是，它的总体客观印象改善得分为 15.79，主观印象改善平均得分为 13.27，相对于基线平均值分别提高了 57.98% 和 286.91%。这些结果表明，RAID G-SEO 在增强生成搜索场景中的整体内容可见性和用户感知质量方面非常有效，在捕捉用户吸引力的主观印象指标方面具有特别明显的优势。

### 段落 61 · Page 7

**EN**

A closer examination of subjective evaluation results further reveals that RAID G- SEO achieves comprehensive superiority in Subjective Impression Improvement, attaining an average improvement score of 13.27, which exceeds the second-best method by 61.35%. In the fine-grained analysis across individual subjective dimensions, RAID G-SEO consistently outperforms all baselines on every dimension. The smallest relative gain is observed on the uniqueness dimension, where RAID G-SEO surpasses the second-best method by at least 36.75%, while the largest gain appears on the diversity dimension, with an improvement margin of 84.63%.

**中文**

仔细考察主观评价结果进一步发现，RAID G-SEO在主观印象改善方面取得了综合优势，平均改善得分为13.27，比第二好的方法高出了61.35%。在跨个人主观维度的细粒度分析中，RAID G-SEO 在每个维度上始终优于所有基线。最小的相对增益出现在独特性维度上，其中 RAID G-SEO 超过第二好的方法至少 36.75%，而最大的增益出现在多样性维度上，改进幅度为 84.63%。

### 段落 62 · Page 7

**EN**

These results suggest that RAID G-SEO is particularly effective at enhancing the distinctiveness and discriminability of content sources within generated responses. It is worth noting that, on Objective Impression Improvement, RAID G-SEO underperforms quotation-based and statisticsbased optimization methods that rely heavily on explicit citation signals or statistical features.

**中文**

这些结果表明 RAID G-SEO 在增强生成的响应中内容源的独特性和可辨别性方面特别有效。值得注意的是，在客观印象改善方面，RAID G-SEO 的表现不如基于引用和基于统计的优化方法，这些方法严重依赖显式引用信号或统计特征。

### 段落 63 · Page 7

**EN**

In contrast, on the subjective positional prominence and subjective content volume metrics which also assess the position and proportion of content within responses from a subjective perspective, RAID G-SEO exhibits the opposite trend and achieves substantially larger improvements. We attribute this discrepancy to fundamental differences between GSE and traditional search engine taht the former emphasize holistic semantic expression and subjective information delivery rather than directly leveraging explicit citation cues.

**中文**

相比之下，在主观位置突出度和主观内容量指标（也从主观角度评估响应中内容的位置和比例）上，RAID G-SEO 表现出相反的趋势，并实现了显着更大的改进。我们将这种差异归因于 GSE 和传统搜索引擎之间的根本差异，前者强调整体语义表达和主观信息传递，而不是直接利用明确的引用线索。

### 段落 64 · Page 7

**EN**

By comparison, traditional keyword-based SEO methods achieve only marginal improvements of 0.08 and 0.21 on objective and subjective metrics respectively, performming significantly worse than other optimization strategies under the current evaluation setting. This observation suggests that, due to mismatches in optimization objectives and application scenarios, conventional SEO techniques do not readily transfer to GSE-oriented optimization tasks.

**中文**

相比之下，传统的基于关键词的 SEO 方法在客观和主观指标上仅分别实现了 0.08 和 0.21 的边际改进，在当前评估设置下表现明显差于其他优化策略。这一观察结果表明，由于优化目标和应用场景的不匹配，传统的SEO技术不容易转移到面向GSE的优化任务。

### 段落 65 · Page 7

**EN**

While our findings are broadly consistent with those reported in GEO [1] where quotation-based and statistics-based optimization methods exhibit strong overall competitiveness, particularly on objective metrics, we also observe notable differences in the relative performance ordering across methods. We conjecture that this coexistence of consistency and divergence may reflect intrinsic preferences of the underlying GSE foundation models in content selection and organization, offering potential insights for future research on knowledge injection and value alignment in LLM.

**中文**

虽然我们的研究结果与 GEO [1] 中报道的结果大致一致，其中基于报价和基于统计的优化方法表现出强大的整体竞争力，特别是在客观指标方面，但我们也观察到不同方法的相对性能排序存在显着差异。我们推测，这种一致性与分歧的共存可能反映了底层 GSE 基础模型在内容选择和组织方面的内在偏好，为法学硕士知识注入和价值调整的未来研究提供了潜在的见解。

### 段落 66 · Page 7

**EN**

2) Adaptability Analysis:To evaluate the adaptability of different optimization methods across diverse GSE retrieval scenarios, we conducted a statistical analysis over 500 optimization task samples. Specifically, we selected Objective Impression Improvement Overall and Subjective Impression Improvement Average as core metrics. Each positive improvement on these metrics was treated as an effective optimization, allowing us to quantify the overall effectiveness of each method in complex GSE environments in terms of both the number and proportion of effective optimizations, as illustrated in Fig. 3 (a).

**中文**

2）适应性分析：为了评估不同优化方法在不同GSE检索场景下的适应性，我们对500多个优化任务样本进行了统计分析。具体来说，我们选择总体客观印象改善和主观印象改善平均值作为核心指标。这些指标的每一次积极改进都被视为一次有效的优化，使我们能够根据有效优化的数量和比例来量化复杂 GSE 环境中每种方法的整体有效性，如图 3 (a) 所示。

### 段落 67 · Page 7

**EN**

The results show that RAID G- SEO achieves an average of 288 effective optimizations across both objective and subjective metrics, corresponding to an average effective optimization rate of 57.6%, which is 1.0 percentage point higher than the second-best terminologybased optimization method (56.6%). Although the absolute improvement is relatively modest, RAID G-SEO maintains consistent superiority across large-scale and diverse retrieval tasks, indicating stronger generalization capability and op-

**中文**

结果显示，RAID G-SEO在客观和主观指标上平均实现了288次有效优化，对应的平均有效优化率为57.6%，比第二好的基于术语的优化方法（56.6%）高出1.0个百分点。尽管绝对改进相对较小，但 RAID G-SEO 在大规模、多样化的检索任务中保持了一致的优势，表明具有更强的泛化能力和运算能力。

### Page 8

### 段落 68 · Page 8

**EN**

8 TABLE IV ABLATION RESULTS OFRAID G-SEOON THE EXPANDEDGEO-BENCH Method Objective Impression(PAWC) Subjective Impression Word Count Posi. CountOver. Rele. Infl. Uniq. Dive. Clic. Sub.Posi. Sub.V olu.Aver. Simple G-SEO (w/o Step) 6.52 9.00 7.97 4.68 3.64 21.87 4.93 7.84 3.72 8.84 6.51 Simple G-SEO (/w Step) 14.85 16.05 15.81 8.12 6.72 34.16 6.55 14.17 8.63 13.23 11.29 ID G-SEO (w/o Summ.) 14.33 17.54 16.69 7.61 6.81 35.24 5.44 14.96 8.96 13.15 11.29 ID G-SEO (w/ Summ.) 18.93 20.78 19.51 9.08 9.1938.86 7.22 15.369.96 14.66 12.95 RAID G-SEO 15.05 16.94 15.79 9.258.80 39.71 7.51 14.63 10.46 16.28 13.27 Fig. 3.

**中文**

8 表 IV RAID G-SEOON EXPANDEDGEO-BENCH 方法的消融结果 客观印象 (PAWC) 主观印象 字数 位置。倒计时。相关。膨胀。独特。潜水。克利克。子Posi。亚卷平均。简单 G-SEO（无步骤） 6.52 9.00 7.97 4.68 3.64 21.87 4.93 7.84 3.72 8.84 6.51 简单 G-SEO（/有步骤） 14.85 16.05 15.81 8.12 6.72 34.16 6.55 14.17 8.63 13.23 11.29 ID G-SEO（不含汇总） 14.33 17.54 16.69 7.61 6.81 35.24 5.44 14.96 8.96 13.15 11.29 ID G-SEO（含汇总） 18.93 20.78 19.51 9.08 9.1938.86 7.22 15.369.96 14.66 12.95 RAID G-SEO 15.05 16.94 15.79 9.258.80 39.71 7.51 14.63 10.46 16.28 13.27 图 3。

### 段落 69 · Page 8

**EN**

Adaptability of G-SEO methods across diverse GSE retrieval scenarios. We evaluate each method’s adaptability by counting the number of optimized content instances that yield observable improvements in subjective and objective visibility across multiple retrieval tasks. This reflects the generalization capacity and real-world utility of each approach. Figure (a) shows a comparison between RAID G-SEO and other baselines, and figure (b) presents part of the ablation analysis. timization consistency in different GSE scenarios.

**中文**

G-SEO 方法在不同 GSE 检索场景中的适应性。我们通过计算优化内容实例的数量来评估每种方法的适应性，这些实例在多个检索任务中在主观和客观可见性方面产生了可观察到的改进。这反映了每种方法的泛化能力和现实世界的实用性。图（a）显示了 RAID G-SEO 与其他基线之间的比较，图（b）显示了部分消融分析。不同GSE场景下的时间化一致性。

### 段落 70 · Page 8

**EN**

Further examination across objective and subjective dimensions reveals that, while RAID G-SEO attains the highest average effective optimization count on Subjective Impression (298), its performance on Objective Impression remains at a moderate level. This pattern is consistent with the main result findings and reflects the inherent differences in user-perceived visibility between GSE responses and traditional search engine results. It is also noteworthy that under the current evaluation setting, the average effective optimization rate of all methods does not exceed 60%.

**中文**

对客观和主观维度的进一步检查表明，虽然 RAID G-SEO 在主观印象上获得了最高的平均有效优化计数 (298)，但其在客观印象上的表现仍处于中等水平。这种模式与主要结果发现一致，反映了 GSE 响应和传统搜索引擎结果之间用户感知可见性的固有差异。还值得注意的是，在当前的评估设置下，所有方法的平均有效优化率不超过60%。

### 段落 71 · Page 8

**EN**

This observation highlights the substantial challenge of achieving robust content visibility improvements in generative retrieval scenarios involving multi-source information. At the same time, it underscores the research value and necessity of investigating G-SEO methods in such complex settings. 3) Ablation Study:We conduct an ablation study by progressively introducing different reasoning modules into RAID G-SEO, aiming to assess the practical contribution of each component to the optimization task. The detailed results are reported in Table IV.

**中文**

这一观察结果凸显了在涉及多源信息的生成检索场景中实现稳健的内容可见性改进所面临的重大挑战。同时，它强调了在如此复杂的环境下研究G-SEO方法的研究价值和必要性。 3）消融研究：我们通过在RAID G-SEO中逐步引入不同的推理模块来进行消融研究，旨在评估每个组件对优化任务的实际贡献。详细结果报告于表IV中。

### 段落 72 · Page 8

**EN**

As the method is incrementally augmented, RAID G-SEO exhibits stable and consistent performance improvements across all evaluation metrics, validating the effectiveness of the proposed intent-driven four-phase optimization framework and its accompanying 4W multi-role deep reflection mechanism in the G-SEO setting.

**中文**

随着该方法的逐步增强，RAID G-SEO 在所有评估指标上都表现出稳定一致的性能改进，验证了所提出的意图驱动四阶段优化框架及其随附的 4W 多角色深度反射机制在 G-SEO 设置中的有效性。

### 段落 73 · Page 8

**EN**

Through pairwise comparisons among the ablation variants that are Simple G- SEO (w/o Step), Simple G-SEO (w/ Step), ID G-SEO (w/o summ.), ID G-SEO (w/ summ.), we can clearly observe the performance gains contributed by each stage of the intentdriven four-phase framework, indicating that all stages make positive contributions to the overall optimization performance.

**中文**

通过对 Simple G-SEO (w/o Step)、Simple G-SEO (w/ Step)、ID G-SEO (w/o summ.)、ID G-SEO (w/ summ.) 等消融变体的两两比较，我们可以清楚地观察到意图驱动四阶段框架中每个阶段所贡献的性能增益，表明所有阶段都对整体优化性能做出了积极的贡献。

### 段落 74 · Page 8

**EN**

Specifically, the content summarization module provides a more focused semantic perspective for subsequent optimization, helping to identify the core aspects of content expression; the intent inference module explicitly models latent user intent, offering clear directional guidance for content reconstruction; and although the step planning module does not directly infer intent, it is able to implicitly capture cues of user’s underlying need, enabling the generated optimization steps to better align with the original content source.

**中文**

具体来说，内容摘要模块为后续优化提供了更加聚焦的语义视角，有助于识别内容表达的核心方面；意图推断模块显式地模拟潜在的用户意图，为内容重构提供清晰的方向性指导；尽管步骤规划模块不能直接推断意图，但它能够隐式捕获用户潜在需求的线索，使生成的优化步骤能够更好地与原始内容源保持一致。

### 段落 75 · Page 8

**EN**

After incorporating the 4W multi-role deep reflection mechanism, the method achieves further improvements on Subjective Impression metrics, while exhibiting a certain degree of degradation on Objective Impression. This phenomenon suggests that generalized intent representation, while enhancing the overall subjective quality of content expression, may in some cases weaken the precise alignment between the specific content sources and itself, thereby affecting objective impression metrics that rely on explicit citation and positional features.

**中文**

在融入4W多角色深度反思机制后，该方法在主观印象指标上实现了进一步的改进，同时在客观印象指标上出现了一定程度的退化。这种现象表明，广义意图表示虽然增强了内容表达的整体主观质量，但在某些情况下可能会削弱特定内容源与其本身之间的精确对齐，从而影响依赖于明确引用和位置特征的客观印象指标。

### 段落 76 · Page 8

**EN**

Notably, the variant ID G-SEO (w/ summ.) without the 4W reflection mechanism attains the best overall performance when jointly considering subjective and objective impression improvements, outperforming two strong baselines, quotation-based and statisticsbased optimization methods. This result further highlights the inherent trade-off between intent modeling precision and generalization capability. In addition, we evaluate the adaptability of different ablation variants in Fig. 4 (b).

**中文**

值得注意的是，在综合考虑主观和客观印象改进时，不带 4W 反射机制的变体 ID G-SEO（w/ summ.）获得了最佳的整体性能，优于两个强大的基线（基于报价和基于统计的优化方法）。这一结果进一步凸显了意图建模精度和泛化能力之间固有的权衡。此外，我们在图 4（b）中评估了不同消融变体的适应性。

### 段落 77 · Page 8

**EN**

The results indicate that the introduced reasoning modules not only improve single-instance optimization effectiveness but also contribute to enhanced stability across diverse retrieval tasks. Of particular interest, compared to ID G-SEO (w/ summ.), the full RAID G-SEO achieves a noticeably higher effective op-

**中文**

结果表明，引入的推理模块不仅提高了单实例优化效率，而且有助于增强跨不同检索任务的稳定性。特别有趣的是，与 ID G-SEO（带总和）相比，完整的 RAID G-SEO 实现了明显更高的有效操作

### Page 9

### 段落 78 · Page 9

**EN**

9 Fig. 4. Distribution of optimization step preferences in RAID G-SEO. Each generated optimization step is structurally parsed to identify its corresponding optimization objective and operational strategy type, followed by semantic clustering. Subfigure (a) shows the distribution across intent-aligned target dimensions (e.g., enhancing content completeness, improving factual credibility, increasing clarity), indicating where the intent prioritizes refinement.

**中文**

9 图 4. RAID G-SEO 中优化步骤偏好的分布。对每个生成的优化步骤进行结构解析，以确定其相应的优化目标和操作策略类型，然后进行语义聚类。子图 (a) 显示了与意图一致的目标维度的分布（例如，增强内容完整性、提高事实可信度、提高清晰度），表明意图优先考虑细化的地方。

### 段落 79 · Page 9

**EN**

Subfigure (b) presents the distribution over strategy categories (e.g., content restructuring, elaboration, redundancy reduction), capturing the model’s typical operational behavior under intent-driven guidance. Fig. 5. Distribution of RAID G-SEO across multi-role perspectives. We perform semantic clustering on the user role descriptions generated by the 4W multi-role deep reflection module to characterize the types of cognitive perspectives involved during intent generalization. The results illustrate the relative frequency of each role category, reflecting the model’s response pattern to perspective distribution during optimization.

**中文**

子图 (b) 显示了策略类别的分布（例如，内容重组、细化、减少冗余），捕获了模型在意图驱动指导下的典型操作行为。图 5. RAID G-SEO 跨多角色视角的分布。我们对 4W 多角色深度反射模块生成的用户角色描述进行语义聚类，以表征意图泛化过程中涉及的认知视角类型。结果说明了每个角色类别的相对频率，反映了模型在优化过程中对视角分布的响应模式。

### 段落 80 · Page 9

**EN**

timization rate on Objective Impression. We hypothesize that this improvement is associated with the expanded optimization coverage brought by intent refinement: although abstract intent representation may reduce precision for individual queries, it can generalize across a wider range of retrieval scenarios, thereby exhibiting advantages in terms of overall adaptability. Overall, this ablation analysis elucidates the specific roles of different modules in performance improvement and provides valuable empirical insights for future efforts to further enhance the precision and robustness of intent modeling in G-SEO.

**中文**

客观印象的时间化率。我们假设这种改进与意图细化带来的优化覆盖范围扩大有关：虽然抽象意图表示可能会降低单个查询的精度，但它可以泛化到更广泛的检索场景，从而在整体适应性方面表现出优势。总的来说，这种消融分析阐明了不同模块在性能改进中的具体作用，并为未来进一步提高 G-SEO 意图建模的精度和鲁棒性提供了宝贵的经验见解。

### 段落 81 · Page 9

**EN**

4) Preference Analysis:Role Perspective Preference Distribution. In the 4W multi-role deep reflection module of RAID G-SEO, we generate diverse user role perspectives based on the content creator’s preliminary assumptions about user search intents, leveraging prompt-based LLM. The result is shown in Fig. 5. A total of 8,030 role instances spanning 219 distinct role types were collected and subjected to semantic clustering, with the distribution visualized in Figure 4.

**中文**

4）偏好分析：角色视角偏好分布。在RAID G-SEO的4W多角色深度反思模块中，我们利用基于提示的LLM，根据内容创建者对用户搜索意图的初步假设生成不同的用户角色视角。结果如图 5 所示。共收集了涵盖 219 个不同角色类型的 8,030 个角色实例，并进行语义聚类，分布如图 4 所示。

### 段落 82 · Page 9

**EN**

The analysis reveals that RAID G-SEO predominantly favors two cognitive perspectives: Knowledge Producers and Researchers (e.g., Educator, Policy Maker) and Civic Everyday Actors (e.g., Home Cook, DIY Hobbyist) dominate the distribution, which together account for over two-thirds of the role instances. In contrast, Health and Care Stakeholders and Cultural and Creative Professionals represent only 6% and 3% of the total, respectively, often corresponding to more specialized or context-dependent viewpoints, while Economic Activity Participants fall in the mid-range.

**中文**

分析显示，RAID G-SEO 主要偏向两种认知视角：知识生产者和研究人员（例如教育者、政策制定者）和公民日常参与者（例如家庭厨师、DIY 爱好者）在分布中占主导地位，它们合计占角色实例的三分之二以上。相比之下，健康和护理利益相关者以及文化和创意专业人士分别仅占总数的 6% 和 3%，通常对应于更专业或取决于具体情况的观点，而经济活动参与者则处于中等水平。

### 段落 83 · Page 9

**EN**

This distribution suggests a tendency of the model to prioritize generalizable, publicly oriented perspectives during intent generalization, rather than narrowly specialized or context-restricted perspectives. We hypothesize that such roles are more effective in guiding generative models to emphasize interpretability, abstraction, and cross-context transferability, thereby yielding more robust intent representations across diverse query scenarios.

**中文**

这种分布表明模型倾向于在意图概括过程中优先考虑可概括的、面向公众的观点，而不是狭隘的专业化或受上下文限制的观点。我们假设这些角色可以更有效地指导生成模型强调可解释性、抽象性和跨上下文可转移性，从而在不同的查询场景中产生更强大的意图表示。

### 段落 84 · Page 9

**EN**

Overall, these findings empirically support the effectiveness of rolebased modeling in intent generalization and provide evidence for the design rationality of the 4W multi-role deep reflection mechanism in generative retrieval optimization tasks. Optimization Steps Preference Distribution. To analyze how search intent informs downstream optimization behaviors, we perform structured semantic parsing of all optimization steps generated during the Step Planning phase of RAID G-SEO. These steps are clustered according to their corresponding optimization objectives and operational types, with the results illustrated in Fig. 4.

**中文**

总的来说，这些发现从实证上支持了基于角色的建模在意图泛化中的有效性，并为生成检索优化任务中4W多角色深度反射机制的设计合理性提供了证据。优化步骤偏好分布。为了分析搜索意图如何通知下游优化行为，我们对 RAID G-SEO 的步骤规划阶段生成的所有优化步骤执行结构化语义解析。这些步骤根据相应的优化目标和操作类型进行聚类，结果如图4所示。

### 段落 85 · Page 9

**EN**

The results indicate that over 80% of the optimization steps explicitly target content quality enhancement, covering objectives such as improving completeness and clarity. This indicates that RAID G-SEO is able to effectively translate retrieval intent into quality-oriented optimization guidance at the planning stage. In terms of operational strategies, Content Enrichment and Expansion accounts for

**中文**

结果表明，超过 80% 的优化步骤明确以增强内容质量为目标，涵盖提高完整性和清晰度等目标。这表明RAID G-SEO能够在规划阶段有效地将检索意图转化为面向质量的优化指导。运营策略上，内容丰富与拓展

### Page 10

### 段落 86 · Page 10

**EN**

10 Fig. 6. Success and failure case analysis of RAID G-SEO. Based on the improvement scores in subjective and objective impression, we select one representative successful case and one failed case, and compare the sources and their presentations in the generated responses before and after optimization, providing a qualitative analysis of RAID G-SEO’s optimization behavior under different scenarios. The bold citation in the responses represent the source to optimization.

**中文**

10 图6. RAID G-SEO 成功与失败案例分析。根据主观印象和客观印象的改善分数，选择一个具有代表性的成功案例和一个失败案例，比较优化前后生成的响应中的来源及其表现形式，对不同场景下的 RAID G-SEO 优化行为进行定性分析。响应中的粗体引用代表优化的来源。

### 段落 87 · Page 10

**EN**

more than 30% of all actions, suggesting that the model, under intent-aware constraints, preferentially adopts information augmentation and semantic expansion to better support the requirements of generative retrieval. Overall, RAID G-SEO exhibits a hybrid planning paradigm in the Step Planning stage that jointly covers multiple optimization objectives, rather than relying on a single optimization strategy. These findings further validate the effectiveness of intent-driven planning mechanisms for G-SEO tasks.

**中文**

超过30%的动作，表明该模型在意图感知约束下，优先采用信息增强和语义扩展，以更好地支持生成检索的要求。总体而言，RAID G-SEO在步骤规划阶段展示了混合规划范式，共同涵盖多个优化目标，而不是依赖于单一优化策略。这些发现进一步验证了 G-SEO 任务的意图驱动规划机制的有效性。

### 段落 88 · Page 10

**EN**

5) Case Analysis:To further elucidate the practical working mechanisms of RAID G-SEO, we conduct a case study by selecting one successful and one failed optimization example based on improvements in both subjective and objective impression, as illustrated in Fig. 6. In the successful case, RAID G-SEO performs refinements on the original content source across linguistic expression, information structure, and content organization. Specifically, RAID G-SEO transforms the original encyclopedic and linearly descriptive writing style into a more engaging and descriptive narrative form.

**中文**

5）案例分析：为了进一步阐明RAID G-SEO的实际工作机制，我们基于主观和客观印象的改善，选择了一个成功的和一个失败的优化示例进行案例研究，如图6所示。在成功的案例中，RAID G-SEO从语言表达、信息结构和内容组织等方面对原始内容源进行了细化。具体来说，RAID G-SEO将原来的百科全书式、线性描述性的写作风格转变为更具吸引力和描述性的叙事形式。

### 段落 89 · Page 10

**EN**

Key information, such as head-first cues, is deliberately front-loaded into the introductory paragraph, which substantially enhances semantic salience and readability without introducing any new

**中文**

关键信息，例如头在先的提示，被故意预先加载到介绍性段落中，这大大增强了语义显着性和可读性，而无需引入任何新的内容

### Page 11

### 段落 90 · Page 11

**EN**

11 factual content. This form of semantics-driven word order adjustment is rarely observed in traditional SEO practices and highlights the fundamental distinction between G-SEO and keyword-centric optimization paradigms. Moreover, RAID G- SEO reorganizes the content through hierarchical and modular restructuring, explicitly separating information units such as introductions and historical background, and emphasizing critical facts via headings and bold formatting. This allows the source to be presented to the generative model of GSE in a more structured manner.

**中文**

11 内容真实。这种语义驱动的词序调整形式在传统 SEO 实践中很少见，它凸显了 G-SEO 和以关键词为中心的优化范式之间的根本区别。此外，RAID G-SEO通过分层和模块化重组来重新组织内容，明确分离介绍和历史背景等信息单元，并通过标题和粗体格式强调关键事实。这使得源能够以更加结构化的方式呈现给 GSE 的生成模型。

### 段落 91 · Page 11

**EN**

Meanwhile, the method applies moderate content compression by de-emphasizing peripheral information and highlighting representative facts, thereby increasing information density while preserving completeness and improving generative retrieval friendliness. These refinements lead to a clear improvement in the expressive quality of the source, which is further reflected in its visibility within generated responses. Specifically, the optimized source was not cited in the original response, whereas after optimization it not only appears in the generated output but also occupies a more prominent visual position with increased share.

**中文**

同时，该方法通过弱化外围信息并突出代表性事实来应用适度的内容压缩，从而在保持完整性的同时提高信息密度并提高生成检索的友好性。这些改进导致源的表达质量明显提高，这进一步反映在生成的响应中的可见性上。具体来说，原始响应中没有引用优化后的源，而优化后它不仅出现在生成的输出中，而且占据了更突出的视觉位置，份额增加了。

### 段落 92 · Page 11

**EN**

Correspondingly, the Objective Impression Overall score increases from 0.09 to 0.32, and the Subjective Impression Average rises from 27.9 to 28.2. In contrast, in the failed optimization case, RAID G-SEO similarly restructures the content and explicitly summarizes previously implicit and dispersed information. By introducing an overview-style lead paragraph, the optimized source is designed to better cover diverse retrieval intents. This process reflects the role of the 4W multi-role deep reflection module in guiding intent generalization and enhancing the adaptability of sources across heterogeneous user scenarios.

**中文**

相应地，客观印象总分从0.09上升到0.32，主观印象平均分从27.9上升到28.2。相比之下，在优化失败的情况下，RAID G-SEO同样对内容进行了重组，并明确总结了先前隐含且分散的信息。通过引入概述式引导段落，优化的源旨在更好地涵盖不同的检索意图。这个过程体现了4W多角色深度反射模块在指导意图泛化和增强源跨异构用户场景的适应性方面的作用。

### 段落 93 · Page 11

**EN**

However, despite improvements in overall readability and guidance, the visibility of the optimized source in the generated response does not improve. The source’s position remains largely unchanged, and it co-supports the same generated segment alongside other sources, thereby weakening its perceived individual contribution. As a result, the Objective Impression Overall score decreases from 0.75 to 0.52, and the Subjective Impression Average drops from 26.70 to 23.90. Further analysis suggests that the primary cause of this failure lies in the high semantic overlap between the optimized source and other competing sources.

**中文**

然而，尽管整体可读性和指导有所改进，但生成的响应中优化源的可见性并没有提高。来源的立场基本保持不变，它与其他来源共同支持同一生成的细分市场，从而削弱了其感知到的个人贡献。结果，客观印象总分从0.75下降到0.52，主观印象平均分从26.70下降到23.90。进一步的分析表明，这种失败的主要原因在于优化源和其他竞争源之间的高度语义重叠。

### 段落 94 · Page 11

**EN**

Consequently, the generative model tends to integrate information from multiple sources during citation, which reduces the distinctiveness of any single source. Through a comparative examination of both successful and failed cases, we identify inherent limitations of RAID G- SEO. While RAID G-SEO demonstrates strong potential in improving content expressiveness and visibility in generative retrieval senarios, its effectiveness critically depends on maintaining a balance between semantic uniqueness of the source and the degree of intent generalization.

**中文**

因此，生成模型倾向于在引用过程中整合来自多个来源的信息，这降低了任何单一来源的独特性。通过对成功和失败案例的比较研究，我们发现了 RAID G-SEO 的固有局限性。虽然 RAID G-SEO 在提高生成检索场景中的内容表达力和可见性方面表现出强大的潜力，但其有效性关键取决于在源的语义唯一性和意图泛化程度之间保持平衡。

### 段落 95 · Page 11

**EN**

Although the multi-role reflection mechanism enables RAID G-SEO to infer relatively generalized intents, such intents remain constrained by the domain boundaries of the source and may fail to fully align with the query, thereby affecting downstream optimization outcomes.

**中文**

尽管多角色反射机制使 RAID G-SEO 能够推断相对广义的意图，但此类意图仍然受到源的域边界的限制，并且可能无法与查询完全一致，从而影响下游优化结果。

### 段落 96 · Page 11

**EN**

For instance, in the failed case, the generalized intent inferred from the source, “Find and share a recipe for a quick, easy-to-make, customizable, and versatile Lemon Balsamic Salad Dressing”—remains strongly tied to the recipe context and exhibits low relevance to nutrition- or medicine-oriented query, limiting the effectiveness of optimization under the given query setting. Notably, across both successful and failed cases, RAID G-SEO consistently applies a combination of multiple optimization operations rather than a single strategy.

**中文**

例如，在失败的案例中，从源中推断出的广义意图“查找并分享快速、易于制作、可定制和多功能柠檬香醋沙拉酱的食谱”仍然与食谱上下文紧密相关，并且与营养或药物导向的查询相关性较低，从而限制了给定查询设置下优化的有效性。值得注意的是，无论是成功还是失败的案例，RAID G-SEO 始终采用多种优化操作的组合，而不是单一策略。

### 段落 97 · Page 11

**EN**

Compared with existing GEO [1] approaches, which typically rely on a single type of optimization, RAID G-SEO offers a broader operational space for optimization and provides a foundation for future exploration of more fine-grained intent alignment mechanisms. V. CONCLUSION This work addresses the task of generative search engine optimization under diverse retrieval scenarios, and introduces an intent-generalization-enhanced optimization approach.

**中文**

与现有的GEO[1]方法通常依赖于单一类型的优化相比，RAID G-SEO提供了更广阔的优化操作空间，并为未来探索更细粒度的意图对齐机制提供了基础。五、结论这项工作解决了不同检索场景下的生成式搜索引擎优化的任务，并引入了一种意图泛化增强的优化方法。

### 段落 98 · Page 11

**EN**

We design an intent-driven four-phase optimization framework , and incorporate a 4W multi-role deep reflection mechanism to improve the generalizability of the inferred intent, enabling creators to perform adaptive and targeted content optimization even in the absence of explicit user queries. To support more comprehensive and objective evaluation, we extend GEO- BENCH to cover a broader range of retrieval scenarios, and develop G-EV AL 2.0, a fine-grained subjective evaluation framework for assessing content visibility.

**中文**

我们设计了意图驱动的四阶段优化框架，并结合了4W多角色深度反射机制来提高推断意图的泛化性，使创作者即使在没有明确的用户查询的情况下也能够进行自适应和有针对性的内容优化。为了支持更全面、客观的评估，我们扩展了GEO-BENCH以覆盖更广泛的检索场景，并开发了G-EVAL 2.0，这是一个用于评估内容可见性的细粒度主观评估框架。

### 段落 99 · Page 11

**EN**

Experimental results demonstrate that intent modeling plays a pivotal role in G-SEO, with generalized intent representations contributing significantly to optimization effectiveness. Nevertheless, balancing the precision and generalizability of intent representations remains a key open challenge. VI. LIMITATIONS While our results demonstrate that incorporating search intent provides more focused guidance for optimization in G- SEO tasks, we observe that overly specific intents may lead to content rewrites that overfit to particular queries, thereby reducing generalizability.

**中文**

实验结果表明，意图建模在 G-SEO 中发挥着关键作用，广义意图表示对优化效果有显着贡献。然而，平衡意图表示的准确性和普遍性仍然是一个关键的开放挑战。六．局限性 虽然我们的结果表明，合并搜索意图为 G-SEO 任务的优化提供了更有针对性的指导，但我们观察到，过于具体的意图可能会导致内容重写，过度适合特定查询，从而降低普遍性。

### 段落 100 · Page 11

**EN**

This observation underscores a central challenge in targeted G-SEO: balancing the precision of intent modeling with the adaptability of optimization strategies. Our approach relies primarily on prompt engineering for preliminary intent extraction, which remains limited in granularity control and contextual consistency. Future work may explore integrating domain-specific knowledge or developing dedicated intent modeling modules to improve the effectiveness of G-SEO methods.

**中文**

这一观察结果强调了目标 G-SEO 的一个核心挑战：平衡意图建模的精度与优化策略的适应性。我们的方法主要依赖于快速工程来进行初步意图提取，这在粒度控制和上下文一致性方面仍然受到限制。未来的工作可能会探索整合特定领域的知识或开发专用的意图建模模块，以提高 G-SEO 方法的有效性。

### 段落 101 · Page 11

**EN**

Furthermore, our proposed method, like most existing G-SEO approaches, focuses solely on plain text without accounting for visual or multimodal elements such as images, diagrams, or tables that may influence content visibility in real-world GSE. Extending G-SEO to Visual-Language Models (VLMs) for unified multimodal optimization poses an important avenue for future research. VII. ETHICALSTATEMENT We strictly adhere to the ethical standards and best practices of the AI research community. We employ LLMs in full compliance with their licensing terms. Our study focuses on improving content visibility within GSE.

**中文**

此外，我们提出的方法与大多数现有的 G-SEO 方法一样，仅关注纯文本，而不考虑视觉或多模式元素，例如可能影响现实世界 GSE 内容可见性的图像、图表或表格。将 G-SEO 扩展到视觉语言模型 (VLM) 以实现统一的多模式优化，为未来的研究提供了重要途径。七．道德声明我们严格遵守人工智能研究社区的道德标准和最佳实践。我们聘用法学硕士时完全遵守他们的许可条款。我们的研究重点是提高 GSE 内的内容可见性。

### 段落 102 · Page 11

**EN**

All experiments are conducted in simulated environments without interfering with,

**中文**

所有实验均在模拟环境中进行，无干扰，

### Page 12

### 段落 103 · Page 12

**EN**

12 misleading, or manipulating the behavior of any real-world systems. To support evaluation, we extend the GEO benchmark by generating synthetic text data using the LLM and applying targeted optimizations. All generated or modified content is intended solely for research and experimentation. The resulting data does not reflect factual information and should not be interpreted as expressing any subjective opinions or value judgments of the authors or the underlying models. REFERENCES [1] Aggarwal, P.; Murahari, V .; Rajpurohit, T.; Kalyan, A.; Narasimhan, K.; and Deshpande, A. 2024. Geo: Generative engine optimization.

**中文**

12 误导或操纵任何现实世界系统的行为。为了支持评估，我们通过使用 LLM 生成合成文本数据并应用有针对性的优化来扩展 GEO 基准。所有生成或修改的内容仅用于研究和实验。所得数据不反映事实信息，不应被解释为表达作者或底层模型的任何主观意见或价值判断。参考文献 [1] Aggarwal, P.；穆拉哈里，V.；拉杰普罗希特，T.；卡延，A.；纳拉西姆汗，K.；和 Deshpande, A. 2024。Geo：生成式引擎优化。

### 段落 104 · Page 12

**EN**

InProceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining, KDD ’24, 5–16. New York, NY , USA: Association for Computing Machinery. ISBN 9798400704901. [2] Almukhtar, F.; Mahmoodd, N.; and Kareem, S. 2021. Search engine optimization: a review.Applied computer science, 17(1): 70–80. [3] Bardas, N.; Mordo, T.; Kurland, O.; Tennenholtz, M.; and Zur, G. 2025. White Hat Search Engine Optimization using Large Language Models. arXiv:2502.07315. [4] Chodak, G.; and Bła ˙zyczek, K. 2024. Large language models for search engine optimization in e-commerce. In Garg, D.; Rodrigues, J. J. P. C.; Gupta, S.

**中文**

第 30 届 ACM SIGKDD 知识发现和数据挖掘会议记录，KDD ’24, 5-16。美国纽约州纽约市：计算机协会。 ISBN 9798400704901。 [2] Almukhtar, F.；马哈茂德，N.； Kareem, S. 2021。搜索引擎优化：综述。应用计算机科学，17(1)：70–80。 [3] 巴尔达斯，N.；莫多，T.；库尔兰，O.；滕南霍尔茨，M.；和 Zur, G. 2025。使用大型语言模型的白帽搜索引擎优化。 arXiv：2502.07315。 [4] 乔达克，G.；和 Bła ˙zyczek, K. 2024。电子商务中搜索引擎优化的大型语言模型。在加尔格，D.；罗德里格斯，J.J.P.C.；古普塔，S.

### 段落 105 · Page 12

**EN**

K.; Cheng, X.; Sarao, P.; and Patel, G. S., eds., International Advanced Computing Conference, 2023, 333–344. Springer, Cham: Springer Nature Switzerland. ISBN 978-3-031-56700-1. [5] Chong, R.; Kong, C.; Wu, L.; Liu, Z.; Jin, Z.; Yang, L.; Fan, Y .; Fan, H.; and Yang, E. 2023. Leveraging prefix transfer for multiintent text revision. In Rogers, A.; Boyd-Graber, J.; and Okazaki, N., eds.,Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers), 1219–1228. Toronto, Canada: Association for Computational Linguistics.

**中文**

K.；程X；萨劳，P.；和 Patel, G. S. 编辑，国际先进计算会议，2023 年，333–344。 Springer, Cham：施普林格自然瑞士。 ISBN 978-3-031-56700-1。 [5] 冲，R.；孔，C.；吴L.；刘，Z.；金，Z。杨，L。范，Y。范，H.； Yang, E. 2023。利用前缀传输进行多意图文本修订。在罗杰斯，A.；博伊德·格雷伯，J.；和 Okazaki, N., eds.，计算语言学协会第 61 届年会记录（第 2 卷：短论文），1219–1228。加拿大多伦多：计算语言学协会。

### 段落 106 · Page 12

**EN**

[6] Greshake, K.; Abdelnabi, S.; Mishra, S.; Endres, C.; Holz, T.; and Fritz, M. 2023. Not what you’ve signed up for: Compromising real-world llmintegrated applications with indirect prompt injection. InProceedings of the 16th ACM workshop on artificial intelligence and security, AISec ’23, 79–90. New York, NY , USA: Association for Computing Machinery. ISBN 9798400702600. [7] Hughes, S.; Bae, M.; and Li, M. 2023. Vectara Hallucination Leaderboard. https://github.com/vectara/hallucination-leaderboard. Accessed: 2025-07- 16. [8] Ji, Z.; Yu, T.; Xu, Y .; Lee, N.; Ishii, E.; and Fung, P. 2023.

**中文**

[6]格雷沙克，K.；阿卜杜勒纳比，S.；米什拉，S.；恩德烈斯，C.；霍尔兹，T.；和 Fritz, M. 2023。这不是您所注册的：通过间接提示注入破坏现实世界的 llmintegrated 应用程序。第 16 届 ACM 人工智能和安全研讨会论文集，AISec ’23, 79-90。美国纽约州纽约市：计算机协会。 ISBN 9798400702600。 [7] 休斯，S.；裴，M.；和 Li, M. 2023。Vectara 幻觉排行榜。 https://github.com/vectara/hallucination-leaderboard。访问时间：2025 年 7 月 16 日。 [8] Ji, Z.；于，T。徐，Y。李，N.；石井，E.；和冯，P.2023。

### 段落 107 · Page 12

**EN**

Towards Mitigating LLM Hallucination via Self Reflection. In Bouamor, H.; Pino, J.; and Bali, K., eds.,Findings of the Association for Computational Linguistics: EMNLP 2023, 1827–1843. Singapore: Association for Computational Linguistics. [9] Kanara, A. P.; Kumari, P.; and Prathap, B. R. 2024. Python Driven Keyword Analysis for SEO Optimization. In2024 10th International Conference on Advanced Computing and Communication Systems (ICACCS), volume 1, 1170–1176. IEEE. [10] Kowalczyk, K.; and Szandala, T. 2024. Enhancing SEO in single-page web applications in contrast with multi-page applications.IEEE Access, 12: 11597–11614.

**中文**

通过自我反思减轻法学硕士幻觉。在布阿莫尔，H.；皮诺，J.； Bali, K., eds.，计算语言学协会的调查结果：EMNLP 2023, 1827–1843。新加坡：计算语言学协会。 [9] 卡纳拉，A.P.；库玛丽，P.；和 Prathap, B. R. 2024。用于 SEO 优化的 Python 驱动的关键字分析。 2024 年第十届高级计算和通信系统国际会议 (ICACCS)，第 1 卷，1170–1176。 IEEE。 [10] 科瓦尔奇克，K.；和 Szandala, T. 2024。与多页面应用程序相比，增强单页 Web 应用程序中的 SEO。IEEE Access，12：11597–11614。

### 段落 108 · Page 12

**EN**

[11] Kumar, A.; and Lakkaraju, H. 2024. Manipulating Large Language Models to Increase Product Visibility. arXiv:2404.07981. [12] Lewandowski, D. 2023.Understanding search engines. Springer. [13] Li, C.; Zhang, M.; Mei, Q.; Kong, W.; and Bendersky, M. 2024. Learning to rewrite prompts for personalized text generation. InProceedings of the ACM Web Conference 2024, WWW ’24, 3367–3378. New York, NY , USA: Association for Computing Machinery. ISBN 9798400701719. [14] Li, Y .; Luo, M.; Gong, Y .; Lin, C.; Jiao, J.; Liu, Y .; and Huang, K. 2025. DeepThink: Aligning Language Models with Domain-Specific User Intents. arXiv:2502.05497.

**中文**

[11] 库马尔，A.；和 Lakkaraju, H. 2024。操纵大型语言模型以提高产品可见性。 arXiv：2404.07981。 [12] Lewandowski, D. 2023。了解搜索引擎。施普林格。 [13] 李成；张，M。梅，Q。孔，W。和 Bendersky, M. 2024。学习重写个性化文本生成的提示。 2024 年 ACM 网络会议记录，WWW ’24, 3367–3378。美国纽约州纽约市：计算机协会。 ISBN 9798400701719。 [14] 李，Y.;罗，M。龚，Y。林，C.；焦，J。刘，Y。和 Huang, K. 2025。DeepThink：使语言模型与特定领域的用户意图保持一致。 arXiv：2502.05497。

### 段落 109 · Page 12

**EN**

[15] Liu, Y .; Iter, D.; Xu, Y .; Wang, S.; Xu, R.; and Zhu, C. 2023. G-Eval: NLG Evaluation using Gpt-4 with Better Human Alignment. In Bouamor, H.; Pino, J.; and Bali, K., eds.,Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, 2511–2522. Singapore: Association for Computational Linguistics. [16] Mao, K.; Dou, Z.; Mo, F.; Hou, J.; Chen, H.; and Qian, H. 2023. Large Language Models Know Your Contextual Search Intent: A Prompting Framework for Conversational Search. In Bouamor, H.; Pino, J.; and Bali, K., eds.,Findings of the Association for Computational Linguistics: EMNLP 2023, 1211–1225.

**中文**

[15] 刘，Y.；伊特尔，D.；徐，Y。王，S。徐，R。 Zhu, C. 2023。G-Eval：使用 Gpt-4 进行 NLG 评估，并具有更好的人类对齐能力。在布阿莫尔，H.；皮诺，J.； Bali, K. 编辑，2023 年自然语言处理经验方法会议论文集，2511-2522。新加坡：计算语言学协会。 [16]毛K.；窦，Z。莫，F。侯，J。陈，H。和Qian, H. 2023。大型语言模型了解您的上下文搜索意图：会话搜索的提示框架。在布阿莫尔，H.；皮诺，J.； Bali, K., eds.，计算语言学协会的调查结果：EMNLP 2023, 1211–1225。

### 段落 110 · Page 12

**EN**

Singapore: Association for Computational Linguistics. [17] Nagpal, M.; and Petersen, J. A. 2021. Keyword Selection Strategies in Search Engine Optimization: How Relevant is Relevance?Journal of Retailing, 97(4): 746–763. SI: Metrics and Analytics. [18] Pfrommer, S.; Bai, Y .; Gautam, T.; and Sojoudi, S. 2024. Ranking Manipulation for Conversational Search Engines. In Al-Onaizan, Y .; Bansal, M.; and Chen, Y .-N., eds.,Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing, 9523–9552. Miami, Florida, USA: Association for Computational Linguistics. [19] Samarah, T.; Alrawashdeh, T.; Mughaid, A.; and AlZu’Bi, S.

**中文**

新加坡：计算语言学协会。 [17] 纳格帕尔，M.；和 Petersen, J. A. 2021。搜索引擎优化中的关键词选择策略：相关性如何？零售杂志，97(4)：746–763。 SI：指标和分析。 [18] 普弗默，S.；白，Y。高塔姆，T.；和 Sojoudi, S. 2024。会话式搜索引擎的排名操作。在 Al-Onaizan，Y .；班萨尔，M.；和 Chen, Y.-N.，编辑，2024 年自然语言处理经验方法会议论文集，9523–9552。美国佛罗里达州迈阿密：计算语言学协会。 [19] 萨马拉，T.；阿尔拉瓦什德，T.；穆格海德，A.；和 AlZu'Bi，S.

### 段落 111 · Page 12

**EN**

2024. Utilizing LLMs for Enhancing Search Engine Optimization Strategies in Digital Marketing. In2024 2nd International Conference on Foundation and Large Language Models (FLLM), 284–288. IEEE. [20] Sarkar, R.; Sarrafzadeh, B.; Chandrasekaran, N.; Rangan, N.; Resnik, P.; Yang, L.; and Jauhar, S. K. 2025. Conversational User-AI Intervention: A Study on Prompt Rewriting for Improved LLM Response Generation. arXiv:2503.16789. [21] Shahzad, A.; Jacob, D. W.; Nawi, N. M.; Mahdin, H.; and Saputri, M. E. 2020.

**中文**

2024 年。利用法学硕士增强数字营销中的搜索引擎优化策略。 2024 年第二届基础和大型语言模型国际会议 (FLLM)，284–288。 IEEE。 [20] 萨卡，R.；萨拉夫扎德，B.；钱德拉塞卡兰，N.；兰甘，N.；雷斯尼克，P.；杨，L。和 Jauhar, S. K. 2025。对话式用户人工智能干预：关于改进 LLM 响应生成的提示重写的研究。 arXiv：2503.16789。 [21] 沙赫扎德，A.；雅各布，D.W.；新墨西哥州纳维；马赫丁，H.；和 Saputri，M.E. 2020。

### 段落 112 · Page 12

**EN**

The new trend for search engine optimization, tools and techniques.Indonesian Journal of Electrical Engineering and Computer Science, 18(3): 1568–1583. [22] Shi, J.; Yuan, Z.; Liu, Y .; Huang, Y .; Zhou, P.; Sun, L.; and Gong, N. Z. 2024. Optimization-based prompt injection attack to llm-as-a-judge. InProceedings of the 2024 on ACM SIGSAC Conference on Computer and Communications Security, CCS ’24, 660–674. New York, NY , USA: Association for Computing Machinery. ISBN 9798400706363. [23] Shinn, N.; Cassano, F.; Gopinath, A.; Narasimhan, K.; and Yao, S. 2023. Reflexion: language agents with verbal reinforcement learning.

**中文**

搜索引擎优化、工具和技术的新趋势。印度尼西亚电气工程和计算机科学杂志，18(3)：1568–1583。 [22] 施杰；袁，Z.；刘，Y。黄，Y。周，P。孙，L.；和Gong, N. Z. 2024。对 llm-as-a-judge 的基于优化的提示注入攻击。 2024 年 ACM SIGSAC 计算机和通信安全会议记录，CCS ’24, 660–674。美国纽约州纽约市：计算机协会。 ISBN 9798400706363。 [23] Shinn，N.；卡萨诺，F.；戈皮纳特，A.；纳拉西姆汗，K.；和 Yao, S. 2023。反射：具有言语强化学习的语言代理。

### 段落 113 · Page 12

**EN**

In Oh, A.; Naumann, T.; Globerson, A.; Saenko, K.; Hardt, M.; and Levine, S., eds.,Advances in Neural Information Processing Systems 36, NIPS 2023, volume 36, 8634–8652. Curran Associates, Inc. [24] Shu, L.; Luo, L.; Hoskere, J.; Zhu, Y .; Liu, Y .; Tong, S.; Chen, J.; and Meng, L. 2024. RewriteLM: An Instruction-Tuned Large Language Model for Text Rewriting. InProceedings of the AAAI Conference on Artificial Intelligence, 2024, volume 38, 18970–18980. AAAI Press. [25] Sun, Z.; Liu, H.; Qu, X.; Feng, K.; Wang, Y .; and Ong, Y . S. 2024. Large Language Models for Intent-Driven Session Recommendations.

**中文**

在哦，A.；瑙曼，T.；格洛伯森，A.；萨恩科，K.；哈特，M.； Levine, S., eds.，神经信息处理系统进展 36，NIPS 2023，第 36 卷，8634–8652。 Curran Associates, Inc. [24] Shu, L.；罗L.；霍斯克雷，J.；朱，Y。刘，Y。童，S。陈，J。和Meng, L. 2024。RewriteLM：用于文本重写的指令调整大型语言模型。 AAAI 人工智能会议记录，2024 年，第 38 卷，18970-18980。 AAAI出版社。 [25]孙Z.；刘，H.；曲，X。冯，K.；王，Y。和翁，Y。 S.2024。用于意图驱动会话推荐的大型语言模型。

### 段落 114 · Page 12

**EN**

InProceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval, SIGIR ’24, 324–334. New York, NY , USA: Association for Computing Machinery. ISBN 9798400704314. [26] Wang, X.; Huang, T.; Wang, D.; Yuan, Y .; Liu, Z.; He, X.; and Chua, T.-S. 2021. Learning Intents behind Interactions with Knowledge Graph for Recommendation. InProceedings of the Web Conference 2021, WWW ’21, 878–887. New York, NY , USA: Association for Computing Machinery. ISBN 9781450383127. [27] Ward, V . 2017. Why, whose, what and how? A framework for knowledge mobilisers.Evidence and Policy, 13(3): 477 – 497.

**中文**

第 47 届国际 ACM SIGIR 信息检索研究与开发会议论文集，SIGIR ’24, 324–334。美国纽约州纽约市：计算机协会。 ISBN 9798400704314。 [26] 王X.；黄，T。王，D。袁，Y。刘，Z.；他，X。和 Chua，T.-S。 2021. 与知识图谱交互背后的学习意图进行推荐。 2021 年网络会议记录，WWW ’21, 878–887。美国纽约州纽约市：计算机协会。 ISBN 9781450383127。 [27] 沃德，V。 2017. 为什么、谁、什么以及如何？知识动员框架。证据与政策，13(3)：477 – 497。

### 段落 115 · Page 12

**EN**

[28] Yan, H.; Zhu, Q.; Wang, X.; Gui, L.; and He, Y . 2024. Mirror: Multipleperspective Self-Reflection Method for Knowledge-rich Reasoning. In Ku, L.-W.; Martins, A.; and Srikumar, V ., eds.,Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), 7086–7103. Bangkok, Thailand: Association for Computational Linguistics. [29] Zhang, W.; Shen, Y .; Wu, L.; Peng, Q.; Wang, J.; Zhuang, Y .; and Lu, W. 2024. Self-Contrast: Better Reflection Through Inconsistent Solving Perspectives.

**中文**

[28] 严 H.；朱Q。王X；桂，L.；和他，Y。 2024.镜子：知识丰富推理的多视角自我反思方法。在Ku，L.-W.；马丁斯，A.；和 Srikumar, V . 编辑，计算语言学协会第 62 届年会记录（第 1 卷：长论文），7086–7103。泰国曼谷：计算语言学协会。 [29] 张文；沉，Y。吴L.；彭，Q。王，J。庄，Y。和 Lu, W. 2024。自我对比：通过不一致的解决视角更好地反思。

### 段落 116 · Page 12

**EN**

In Ku, L.-W.; Martins, A.; and Srikumar, V ., eds.,Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), 3602–3622. Bangkok, Thailand: Association for Computational Linguistics. [30] ˇSk˙erien˙e, S.; and Jucevi ˇcien˙e, P. 2020. Problem solving through values: A challenge for thinking and capability development.Thinking Skills and Creativity, 37: 100694. [31] Kim, J.; Kim, D.-K.; Logeswaran, L.; Sohn, S.; and Lee, H. 2024. Auto-Intent: Automated Intent Discovery and Self-Exploration for Large Language Model Web Agents.

**中文**

在Ku，L.-W.；马丁斯，A.；和 Srikumar, V . 编辑，计算语言学协会第 62 届年会记录（第一卷：长论文），3602–3622。泰国曼谷：计算语言学协会。 [30] ˇSk˙erien˙e，S.；和 Jucevi ˇcien˙e, P. 2020。通过价值观解决问题：思维和能力发展的挑战。思维技能和创造力，37: 100694。 [31] Kim, J.；金，D.-K.；洛格斯瓦兰，L.；索恩，S.；和 Lee, H. 2024。自动意图：大型语言模型 Web 代理的自动意图发现和自我探索。

### 段落 117 · Page 12

**EN**

In Al-Onaizan, Y .; Bansal, M.; and Chen, Y .-N., eds.,Findings of the Association for Computational Linguistics: EMNLP 2024, 16531–16541. Miami, Florida, USA: Association for Computational Linguistics.

**中文**

在 Al-Onaizan，Y .；班萨尔，M.；和 Chen, Y.-N., eds.，计算语言学协会的调查结果：EMNLP 2024, 16531–16541。美国佛罗里达州迈阿密：计算语言学协会。

### Page 13

### 段落 118 · Page 13

**EN**

13 TABLE V PROMPT USED FOR QUERY VARIANT GENERATION Query variants Generation Prompt You are a user of the Generative Search Engine, seeking to explore a specific topic. You will be given a query representing what you want to learn about. Your task is to generate 4 new queries that approach the topic from different perspectives. Ensure that: 1. Each query is relevant to the original but not a direct repetition. 2. The queries cover a range of perspectives, such as related concepts, practical applications, contrasting viewpoints, emerging trends, or any other meaningful dimension. But do not limit to these directions. 3.

**中文**

13 表V 用于查询变体生成的提示 查询变体生成提示 您是生成式搜索引擎的用户，正在寻求探索特定主题。您将收到一个代表您想要了解的内容的查询。您的任务是生成 4 个新查询，从不同角度探讨该主题。确保： 1. 每个查询都与原始查询相关，但不是直接重复。 2. 查询涵盖一系列观点，例如相关概念、实际应用、对比观点、新兴趋势或任何其他有意义的维度。但不限于这些方向。 3.

### 段落 119 · Page 13

**EN**

Output ONLY 1 query per line. ### Input Format {query original} ### Output Format query 1 query 2 query 3 query 4 VIII. QUERY VARIANTSGENERATIONPROMPT To simulate diverse retrieval scenarios in real-world GSE applications, we extended the GEO-BENCH dataset. Specifically, for each original query in GEO-BENCH, we constructed four semantically related but lexically and stylistically distinct variants, each reflecting a different retrieval scenario. Each variant preserves the core meaning while introducing variation in wording, tone, or semantic framing. The prompt used to generate these variants is presented in Table V. IX.

**中文**

每行仅输出 1 个查询。 ### 输入格式{查询原始} ### 输出格式 query 1 query 2 query 3 query 4 VIII. QUERY VARIANTSGENERATIONPROMPT 为了模拟现实 GSE 应用程序中的各种检索场景，我们扩展了 GEO-BENCH 数据集。具体来说，对于 GEO-BENCH 中的每个原始查询，我们构建了四个语义相关但词汇和风格不同的变体，每个变体反映了不同的检索场景。每个变体都保留了核心含义，同时引入了措辞、语气或语义框架的变化。表 V. IX 中列出了用于生成这些变体的提示。

### 段落 120 · Page 13

**EN**

G-EVALPROMPTGENERATIONPROMPT AND EVALUATIONPROMPTTEMPLATE G-eval is a natural language generation (NLG) evaluation framework that integrates Chain-of-Thought (CoT) reasoning with a form-filling paradigm. GEO extended this framework to the G-SEO context to enable subjective evaluation of content source attribution in GSE outputs. In this work, we conduct an in-depth analysis of the G-eval mechanism as adopted by GEO.

**中文**

G-EVALPROMPT生成提示和评估提示模板 G-eval 是一种自然语言生成 (NLG) 评估框架，它将思想链 (CoT) 推理与表单填写范例集成在一起。 GEO 将此框架扩展到 G-SEO 环境中，以便能够对 GSE 输出中的内容源归因进行主观评估。在这项工作中，我们对GEO采用的G-eval机制进行了深入分析。

### 段落 121 · Page 13

**EN**

While the framework provides reasonably comprehensive coverage across seven subjective impression dimensions, we identify three key limitations when applied to the G-SEO setting: (1) several evaluation criteria are underspecified, leading to potential inconsistencies in annotator interpretation; (2) the mapping between scoring levels and their semantic interpretations is vague, which undermines the clarity and interpretability of the results; and (3) the prevalent issue of “unreferenced original content” in GSE responses is not explicitly addressed, increasing the risk of misjudging inexistent content as grounded.

**中文**

虽然该框架在七个主观印象维度上提供了相当全面的覆盖，但我们在应用于 G-SEO 设置时发现了三个关键限制：(1) 一些评估标准未指定，导致注释者解释可能存在不一致； (2) 评分级别与其语义解释之间的映射模糊，损害了结果的清晰度和可解释性； (3) GSE 回复中普遍存在的“未引用原始内容”问题没有得到明确解决，增加了将不存在的内容误判为有根据的风险。

### 段落 122 · Page 13

**EN**

To address these limitations, we propose an enhanced evaluation framework, G-eval 2.0, designed to support more fine-grained, fair, and reproducible subjective assessment.

**中文**

为了解决这些限制，我们提出了一个增强的评估框架，G-eval 2.0，旨在支持更细粒度、公平和可重复的主观评估。

### 段落 123 · Page 13

**EN**

We standardize structured rubrics across all seven dimensions and design corresponding prompts for automatic evaluation logic generation, covering key aspects such as dimension definition, core scoring elements, and the semantic mapping of score levels, thereby TABLE VI STRUCTURED PROMPT FOR GENERATING SCORING RUBRICS ACROSS SEVEN SUBJECTIVE DIMENSIONS G-EV AL Prompt Generation Prompt You are an evaluator for answers generated by the Generative Search Engine, providing subjective evaluations... Your tasks: 1. Refine the criteria: Review the given description and improve it to be concise, consistency, and completeness. 2.

**中文**

我们标准化了所有七个维度的结构化量规，并设计了自动评估逻辑生成的相应提示，涵盖维度定义、核心评分元素和分数级别的语义映射等关键方面，从而表六用于生成跨七个主观维度的评分量规的结构化提示G-EV AL提示生成提示您是生成式搜索引擎生成的答案的评估者，提供主观评估...您的任务： 1. 细化标准：审查给定的描述并改进其简洁、一致和完整。 2.

### 段落 124 · Page 13

**EN**

Propose an Evaluation Procedure: Based on the refined criteria, outline a clear, concise, step-by-step process specifically for scoring Source [1] only. If the source not exsist, score should be 0. Please ensure your generation is easy to understand. ### Input Format Example:Relevance of Citation to Query (0-5): The dimension evaluates the degree to which the citation from Source [1] is related to the query, indicating how useful and pertinent the information provided to address the query.... ### Output Format Evaluation Criteria: [...] Evaluation Steps: 1. Step 1 description... 2. Step 2 description... ...

**中文**

提出评估程序：根据细化的标准，概述一个清晰、简洁、分步的流程，专门用于对源 [1] 进行评分。如果来源不存在，则分数应为 0。请确保您的生成易于理解。 ### 输入格式示例：引文与查询的相关性 (0-5)：该维度评估来源 [1] 的引文与查询的相关程度，表明所提供的信息对于解决查询的有用性和相关性... ### 输出格式 评估标准：[...] 评估步骤： 1. 第 1 步描述... 2. 第 2 步描述... ...

### 段落 125 · Page 13

**EN**

TABLE VII UNIFIED EVALUATION PROCEDURE TEMPLATE ING-EVAL2.0 Query variants Generation Prompt You are a user of Generative Search Engine, capable of providing subjective evaluations of retrieved answers... Please read and understand these instructions carefully, and then proceed with your scoring (score ONLY). ### Evaluation Criteria [Evaluation Criteria]: [...] ### Evaluation Steps [...] ### Input Format Query:{query} Answer:{answer} ### Output Format (score ONLY) [score] ensuring consistency, executability, and interpretability across all dimensions, as is shown in Table VI.

**中文**

表VII 统一评估程序模板ING-EVAL2.0 查询变体生成提示您是生成式搜索引擎的用户，能够对检索到的答案提供主观评估...请仔细阅读并理解这些说明，然后继续进行评分（仅评分）。 ### 评估标准 [评估标准]：[...] ### 评估步骤 [...] ### 输入格式查询：{query} 答案：{answer} ### 输出格式（仅限分数）[分数] 确保所有维度的一致性、可执行性和可解释性，如表 VI 所示。

### 段落 126 · Page 13

**EN**

Additionally, we develop a unified evaluation procedure template applicable across dimensions as shown in Table VII, integrating the CoT reasoning paradigm. The template standardizes the full evaluation process, from content interpretation and key scoring element extraction to structured scoring. To maintain focus on the core evaluation methodology, task-specific background information is omitted in this appendix section.

**中文**

此外，我们开发了一个适用于各个维度的统一评估程序模板，如表七所示，集成了 CoT 推理范式。该模板标准化了整个评估过程，从内容解释和关键评分元素提取到结构化评分。为了保持对核心评估方法的关注，本附录部分省略了特定任务的背景信息。

### Page 14

### 段落 127 · Page 14

**EN**

14 TABLE VIII CORE CONFIGURATIONS OFLLMS USED IN OUR WORK. Model Temperature Top p Max token Application GPT-4 0.5 1 1024 Query Variants Generation GPT-4o 0.5 1 3192 G-eval 2.0 Prompt Generation GLM-4-9B-0414 0.5 1 1024 GSE Response Generation Simulation do sample=False 1 3192 G-SEO Methods Implementation do sample=False 1 2 G-eval 2.0 Subjective Impression Evaluation X. EXPERIMENTDETAILS A. Software and Hardware Environment All experiments in this work were conducted on a server equipped with two NVIDIA GeForce RTX 3090 GPUs (24GB VRAM each), running Ubuntu 20.04.

**中文**

14 表 VIII 我们工作中使用的 LLMS 核心配置。模型温度 Top p 最大令牌应用 GPT-4 0.5 1 1024 查询变体生成 GPT-4o 0.5 1 3192 G-eval 2.0 提示生成 GLM-4-9B-0414 0.5 1 1024 GSE 响应生成模拟 dosample=False 1 3192 G-SEO 方法实施 dosample=False 1 2 G-eval 2.0主观印象评估 X. 实验细节 A. 软件和硬件环境 这项工作中的所有实验都是在配备两个 NVIDIA GeForce RTX 3090 GPU（每个 24GB VRAM）、运行 Ubuntu 20.04 的服务器上进行的。

### 段落 128 · Page 14

**EN**

The core software stack includes Python 3.9.19, PyTorch 2.1.0 with CUDA 11.8 support, and Transformers 4.35.3. All model loading and inference were carried out using the Hugging Face Transformers interface, and environment dependencies were managed via Conda. Unless otherwise specified, all experiments were run with a fixed random seed (seed = 42) to ensure reproducibility. B.

**中文**

核心软件堆栈包括Python 3.9.19、支持 CUDA 11.8 的 PyTorch 2.1.0 和 Transformers 4.35.3。所有模型加载和推理都是使用 Hugging Face Transformers 接口进行的，并且环境依赖项通过 Conda 进行管理。除非另有说明，所有实验均使用固定随机种子（种子 = 42）进行，以确保重现性。 B.

### 段落 129 · Page 14

**EN**

Configuration Parameters of LLMs To support reproducibility and transparency, Table VIII summarizes the key configuration parameters of LLMs used at different stages of our work, including model name, temperature, top-p, maximum tokens, and the specific usage scenario for each configuration. C. Subjective Impression Evaluation Procedure for G-SEO Mehtods To more accurately assess the effectiveness of the G-SEO methods in enhancing the subjective impression of target content under diverse retrieval scenarios in GSE, we designed the evaluation procedure illustrated in 7.

**中文**

LLM 的配置参数 为了支持可重复性和透明度，表 VIII 总结了我们工作不同阶段使用的 LLM 的关键配置参数，包括模型名称、温度、top-p、最大令牌以及每个配置的具体使用场景。 C. G-SEO 方法的主观印象评估程序为了更准确地评估 G-SEO 方法在 GSE 中不同检索场景下增强目标内容主观印象的有效性，我们设计了如图 7 所示的评估程序。

### 段落 130 · Page 14

**EN**

We randomly sampled 100 diverse-retrieval examples from the GEO-BENCH dataset (seed = 42). Each sample consists of one original query and four paraphrased variants that preserve the core semantic focus, resulting in five queries per sample. For each query, we generated responses from five content sources both before and after optimization. The subjective impression scoring mechanism was then applied to assess the visibility of each source within each response. We first averaged the scores of the five responses under each query to obtain a query-level score.

**中文**

我们从 GEO-BENCH 数据集中随机抽取了 100 个多样化检索示例（种子 = 42）。每个样本由一个原始查询和四个保留核心语义焦点的释义变体组成，从而每个样本有五个查询。对于每个查询，我们在优化前后从五个内容源生成响应。然后应用主观印象评分机制来评估每个响应中每个来源的可见性。我们首先对每个查询下的五个响应的分数进行平均，以获得查询级别的分数。

### 段落 131 · Page 14

**EN**

Next, we averaged the five query-level scores within each sample to obtain a sample-level evaluation. Finally, we averaged across all 100 samples to derive the overall effectiveness score for the optimization method.

**中文**

接下来，我们对每个样本中的五个查询级别分数进行平均，以获得样本级别的评估。最后，我们对所有 100 个样本进行平均，得出优化方法的总体有效性得分。

### Page 15

### 段落 132 · Page 15

**EN**

15 Fig. 7. Evaluation process for optimization methods. For each query, responses are generated from five content sources before and after optimization. By comparing the relative impression scores of each source in the responses, we assess the effectiveness of G-SEO methods in enhancing content visibility. Each diverse-retrieval sample includes one original query and four paraphrased variants. For each query, five responses are generated, evaluated, and averaged to obtain the query-level result. Overall performance is obtained by averaging the query-level results across all five queries.

**中文**

15 图 7. 优化方法的评估过程。对于每个查询，优化前后的五个内容源都会生成响应。通过比较回复中每个来源的相对印象分数，我们评估 G-SEO 方法在提高内容可见性方面的有效性。每个多样化检索样本都包含一个原始查询和四个释义变体。对于每个查询，生成、评估和平均五个响应以获得查询级结果。总体性能是通过对所有五个查询的查询级结果进行平均来获得的。
