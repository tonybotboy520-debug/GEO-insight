# E-GEO: A Testbed for Generative Engine Optimization in E-Commerce

- ID: 66
- 类型: pdf
- 分类: 04_academic_papers
- 主题: e-commerce GEO benchmark/testbed
- 原文链接: https://arxiv.org/pdf/2511.20867
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

E-GEO: A Testbed for Generative Engine Optimization in E-Commerce Puneet S. Bagga ∗ Vivek F. Farias † Tamar Korkotashvili‡ Tianyi Peng § Yuhang Wu§ This version: November 25, 2025 Abstract With the rise of large language models (LLMs), generative engines are becoming powerful alternatives to traditional search, reshaping retrieval tasks. In e-commerce, for instance, conversational shopping agents now guide consumers to relevant products. This shift has created the need for generative engine optimization (GEO)—improving content visibility and relevance for generative engines.

**中文**

E-GEO：电子商务中生成式引擎优化的测试平台 Puneet S. Bagga ∗ Vivek F. Farias † Tamar Korkotashvili‡ Tianyi Peng § Yuhang Wu§ 此版本：2025 年 11 月 25 日 摘要 随着大型语言模型 (LLM) 的兴起，生成式引擎正在成为传统搜索的强大替代品，重塑检索任务。例如，在电子商务中，对话式购物代理现在可以引导消费者找到相关产品。这种转变产生了对生成式引擎优化 (GEO) 的需求——提高生成式引擎的内容可见性和相关性。

### 段落 2 · Page 1

**EN**

Yet despite its growing importance, current GEO practices are ad hoc, and their impacts remain poorly understood, especially in e-commerce. We address this gap by introducing E-GEO, the first benchmark built specifically for e-commerce GEO. E-GEO contains over 7,000 realistic, multi-sentence consumer product queries paired with relevant listings, capturing rich intent, constraints, preferences, and shopping contexts that existing datasets largely miss. Using this benchmark, we conduct the first large-scale empirical study of e-commerce GEO, evaluating 15 common rewriting heuristics and comparing their empirical performance.

**中文**

然而，尽管其重要性日益增加，但当前的 GEO 实践是临时性的，其影响仍然知之甚少，尤其是在电子商务领域。我们通过引入 E-GEO 来解决这一差距，这是第一个专门为电子商务 GEO 构建的基准。 E-GEO 包含 7,000 多个真实的多句子消费者产品查询以及相关列表，捕获现有数据集很大程度上遗漏的丰富意图、约束、偏好和购物上下文。利用这个基准，我们对电子商务 GEO 进行了首次大规模实证研究，评估了 15 种常见的重写启发式方法并比较了它们的实证表现。

### 段落 3 · Page 1

**EN**

To move beyond heuristics, we further formulate GEO as a tractable optimization problem and develop a lightweight iterative prompt-optimization algorithm that can significantly outperform these baselines. Surprisingly, the optimized prompts reveal a stable, domain-agnostic pattern—suggesting the existence of a “universally effective” GEO strategy. Our data and code are publicly available athttps://github.com/psbagga17/E-GEO.

**中文**

为了超越启发式，我们进一步将 GEO 表述为一个易于处理的优化问题，并开发了一种轻量级迭代提示优化算法，该算法可以显着优于这些基线。令人惊讶的是，优化后的提示揭示了一种稳定的、与领域无关的模式——表明存在“普遍有效”的 GEO 策略。我们的数据和代码可在 https://github.com/psbagga17/E-GEO 上公开获取。

### 段落 4 · Page 1

**EN**

1 Keywords:Generative Engine Optimization, Large Language Models, Benchmark Dataset, Generative AI in E-commerce, Prompt Optimization 1 Introduction Over the last few decades, search engine optimization (SEO) has shaped how online content is produced, structured, and surfaced to users. By tailoring to the preferences of search engines such as Google and Bing, content creators influence where their webpages appear among ranked search results and, in turn, drive traffic and engagement.

**中文**

1 关键词：生成式引擎优化、大型语言模型、基准数据集、电子商务中的生成人工智能、即时优化 1 简介 在过去的几十年中，搜索引擎优化 (SEO) 塑造了在线内容的生成、结构化和呈现给用户的方式。通过根据 Google 和 Bing 等搜索引擎的偏好进行定制，内容创建者可以影响其网页在排名搜索结果中的显示位置，从而提高流量和参与度。

### 段落 5 · Page 1

**EN**

The landscape is now shifting, as advances in large language models (LLMs) have given rise to generative engines—often deployed as chatbots—that offer users an alternative way to access information. Recent studies have observed reduced user engagement with traditional search platforms (Sommerfeld et al., 2025; Toscano, 2025), especially ∗Department of Industrial Engineering and Operations Research, Columbia University †Sloan School of Management, Massachusetts Institute of Technology ‡Electrical Engineering and Computer Science, Massachusetts Institute of Technology §Decision, Risk, and Operations Division, Columbia Business School.

**中文**

随着大型语言模型 (LLM) 的进步催生了生成式引擎（通常部署为聊天机器人），这种情况正在发生变化，为用户提供了另一种访问信息的方式。最近的研究发现，用户对传统搜索平台的参与度有所下降（Sommerfeld 等人，2025 年；Toscano，2025 年），尤其是 *哥伦比亚大学工业工程和运筹学系 †麻省理工学院斯隆管理学院 ‡麻省理工学院电气工程和计算机科学 §哥伦比亚商学院决策、风险和运营部门。

### 段落 6 · Page 1

**EN**

1Author names are ordered alphabetically. 1 arXiv:2511.20867v1 [cs.IR] 25 Nov 2025

**中文**

1作者姓名按字母顺序排列。 1 arXiv:2511.20867v1 [cs.IR] 2025 年 11 月 25 日

### Page 2

### 段落 7 · Page 2

**EN**

when generative engines can deliver comparable content (Lyu et al., 2025). This behavioral shift raises a new question: What properties of online content determine whether a generative engine “likes” it? Early findings indicate that these signals may diverge substantially from the classical SEO playbook (Aggarwal et al., 2024; Allouah et al., 2025). Consequently, generative engine optimization (GEO), the practice of improving the visibility and relevance of content for generative engines, has become an emerging concern for creators and businesses (Berry, 2025; Madhavan, 2025).

**中文**

当生成式引擎可以提供类似的内容时（Lyu et al., 2025）。这种行为转变提出了一个新问题：在线内容的哪些属性决定了生成式引擎是否“喜欢”它？早期研究结果表明，这些信号可能与经典 SEO 策略有很大不同（Aggarwal 等人，2024 年；Allouah 等人，2025 年）。因此，生成式引擎优化（GEO），即提高生成式引擎内容的可见性和相关性的实践，已成为创作者和企业的一个新兴关注点（Berry，2025；Madhavan，2025）。

### 段落 8 · Page 2

**EN**

Despite this growing interest, current GEO practices are largely heuristic, relying on rules of thumb such as the use of quotations, authoritative tone, or FAQ-style structures (Aggarwal et al., 2024; Berry, 2025). Yet it remains unclear whether these interventions produce meaningful value, in part because existing metrics like the impression score (Aggarwal et al., 2024) do not translate directly to economic impact. This gap makes e-commerce a natural testbed, as it provides an environment where changes in the product’s ranking can be measured in concrete financial terms.

**中文**

尽管人们的兴趣日益浓厚，但当前的 GEO 实践在很大程度上是启发式的，依赖于经验法则，例如使用引文、权威语气或常见问题解答风格的结构（Aggarwal 等人，2024 年；Berry，2025 年）。然而，目前尚不清楚这些干预措施是否能产生有意义的价值，部分原因是印象分数等现有指标（Aggarwal 等人，2024 年）并不能直接转化为经济影响。这种差距使电子商务成为一个天然的测试平台，因为它提供了一个可以用具体的财务术语衡量产品排名变化的环境。

### 段落 9 · Page 2

**EN**

Moreover, conversational shopping tools backed by generative engines are gaining traction: Amazon has launched its AI-powered shopping assistant (Mehta and Chilimbi, 2024), and other e-commerce platforms are following suit (Bellan, 2025). These developments position e-commerce GEO as both practically important and understudied. In this work, we propose a systematic and data-driven framework for studying GEO in ecommerce.

**中文**

此外，由生成式引擎支持的对话式购物工具正在获得关注：亚马逊推出了人工智能购物助手（Mehta 和 Chilimbi，2024 年），其他电子商务平台也在效仿（Bellan，2025 年）。这些发展使电子商务 GEO 变得既具有实际重要性又未被充分研究。在这项工作中，我们提出了一个系统的、数据驱动的框架来研究电子商务中的 GEO。

### 段落 10 · Page 2

**EN**

Our contributions include: 1.Benchmark dataset.We introduceE-GEO, a novel dataset of 7,000+ long-form Reddit product queries matched with Amazon listings, providing the first-of-its-kind benchmark that captures real-world consumer intent for GEO. 2.Evaluation of existing heuristics.We assess 15 heuristic rewriting strategies inspired by current GEO practices, providing the first empirical comparison of their effectiveness in an e-commerce context. 3.Optimization-based GEO formulation.We cast GEO as an operationalizable optimization problem that aligns naturally with existing prompt-optimization literature.

**中文**

我们的贡献包括： 1.Benchmark 数据集。我们推出了 E-GEO，这是一个包含 7,000 多个与 Amazon 列表相匹配的长格式 Reddit 产品查询的新颖数据集，提供了第一个捕捉真实世界消费者对 GEO 意图的基准。 2.现有启发式的评估。我们评估了受当前 GEO 实践启发的 15 种启发式重写策略，首次对其在电子商务环境中的有效性进行了实证比较。 3.基于优化的GEO公式。我们将GEO视为一个可操作的优化问题，与现有的即时优化文献自然一致。

### 段落 11 · Page 2

**EN**

We demonstrate that even a simple optimization algorithm can outperform heuristic methods by a substantial margin. 4.Generalizable rewriting strategy .By examining optimized prompts, we uncover evidence of a “universally effective” rewriting strategy that generalizes across queries and domains, suggesting that systematic optimization obviates the need for ad hoc heuristics. 2 Literature Review The concept of generative engine optimization (GEO) was first introduced by Aggarwal et al.

**中文**

我们证明，即使是简单的优化算法也可以大幅优于启发式方法。 4.可泛化的重写策略。通过检查优化的提示，我们发现了“普遍有效”的重写策略的证据，该策略可泛化于查询和领域，这表明系统优化消除了对临时启发式的需要。 2 文献综述 生成式引擎优化（GEO）的概念最早由 Aggarwal 等人提出。

### 段落 12 · Page 2

**EN**

(2024), who evaluated several heuristics for increasing a source’s visibility within generative engine outputs based on a proposed impression score that combines word count, citation position, and GPT-3.5-based quality assessments. While foundational, this work centers on heuristics and lacks a systematic optimization framework, and the impression score does not translate directly to commercial value in e-commerce settings. A separate line of research examines prompt injection and manipulation attacks on LLMs (Kumar and Lakkaraju, 2024; Pfrommer et al., 2024) in a similar setting.

**中文**

(2024)，他根据结合了字数、引用位置和基于 GPT-3.5 的质量评估的建议印象分数，评估了几种提高生成式引擎输出中来来源可见度的启发式方法。虽然是基础性的，但这项工作以启发式为中心，缺乏系统的优化框架，而且印象分数并不能直接转化为电子商务环境中的商业价值。另一项研究在类似的环境中检查了对 LLM 的即时注入和操纵攻击（Kumar 和 Lakkaraju，2024 年；Pfrommer 等人，2024 年）。

### 段落 13 · Page 2

**EN**

Although these studies demonstrate that model outputs can be systematically influenced, 2

**中文**

尽管这些研究表明模型输出可能会受到系统性影响，2

### Page 3

### 段落 14 · Page 3

**EN**

their objectives are adversarial and exploitative in nature rather than improving legitimate visibility. Overall, the GEO literature remains nascent, with many open questions regarding effective strategies and their practical impacts. Our work intersects with the literature on prompt optimization. Early work such as Zhou et al. (2023) introduced automatic prompt engineering (APE), and many subsequent papers have explored methods for refining or adapting prompts for downstream tasks. The optimization approach we adopt is particularly inspired by the reflection module in GEPA (Agrawal et al., 2025).

**中文**

他们的目标本质上是对抗性和剥削性的，而不是提高合法的知名度。总体而言，GEO 文献仍处于萌芽阶段，关于有效策略及其实际影响还有许多悬而未决的问题。我们的工作与即时优化的文献有交叉。周等人的早期工作。 （2023）引入了自动提示工程（APE），许多后续论文探索了针对下游任务完善或调整提示的方法。我们采用的优化方法特别受到 GEPA 中反射模块的启发（Agrawal et al., 2025）。

### 段落 15 · Page 3

**EN**

Our setting also relates to recent interest in LLM-backed shopping assistants (Allouah et al., 2025) and the broader literature on LLM-empowered recommender systems (Wu et al., 2024). These works highlight the shift toward conversational, intent-rich interactions in online platforms, precisely the prime context for GEO. 3 GEO in E-Commerce 3.1 Generative Engine On a high level, generative engines in e-commerce settings can be viewed as instances of retrievalaugmented generation (RAG) (Lewis et al., 2020).

**中文**

我们的背景还涉及最近对法学硕士支持的购物助理的兴趣（Allouah 等人，2025）以及关于法学硕士授权的推荐系统的更广泛的文献（Wu 等人，2024）。这些作品凸显了在线平台向对话式、意图丰富的互动的转变，而这正是 GEO 的主要背景。 3 电子商务中的 GEO 3.1 生成式引擎 在较高层面上，电子商务环境中的生成式引擎可以被视为检索增强生成 (RAG) 的实例（Lewis 等人，2020）。

### 段落 16 · Page 3

**EN**

As illustrated in Figure 1, when a user submits a product-related query, the system first performs a retrieval step that gathers a short catalog of relevant listings from the platform’s product pool. The generative engine then synthesizes a naturallanguage response that often includes an accompanying ranked list of recommended products, effectively functioning as are-rankerthat orders the retrieved items based on their alignment with the inferred user intent, preferences, and constraints. Generative Engine Product Pool Query Retrieval Retrieved products Ranked products Figure 1: Generative Engine in E-Commerce.

**中文**

如图 1 所示，当用户提交与产品相关的查询时，系统首先执行检索步骤，从平台的产品池中收集相关列表的简短目录。然后，生成式引擎合成自然语言响应，该响应通常包括随附的推荐产品排名列表，有效地充当排序器，根据检索到的项目与推断的用户意图、偏好和约束的一致性对检索到的项目进行排序。生成式引擎 产品池 查询检索 检索到的产品 对产品进行排名 图 1：电子商务中的生成式引擎。

### 段落 17 · Page 3

**EN**

3.2 The GEO Process We conceptualize GEO as a mapping thatrewritesa product description to improve its ranking across user queries, without access to the queries themselves (Figure 2). Similar to GEO in web search, it is natural to hypothesize that certain rewriting strategies, such as emphasizing salient attributes or adopting particular linguistic styles, can systematically affect downstream exposure. In e-commerce, however, this objective is more concrete and operationalizable, as it maps directly to observable rankings and measurable commercial outcomes.

**中文**

3.2 GEO 流程 我们将 GEO 概念化为一种映射，它重写产品描述以提高其在用户查询中的排名，而无需访问查询本身（图 2）。与网络搜索中的 GEO 类似，很自然地假设某些重写策略（例如强调显着属性或采用特定语言风格）可以系统地影响下游曝光。然而，在电子商务中，这一目标更加具体和可操作，因为它直接映射到可观察的排名和可衡量的商业成果。

### 段落 18 · Page 3

**EN**

In web search-oriented GEO, generative responses typically consist of free-form text interleaved with citations to external sources, where a source’s “visibility” is inherently indirect and difficult to quantify. To formalize this notion, Aggarwal et al. (2024) proposed theimpression score, which combines word count, citation position, and GPT-3.5-based quality assessments. While useful as a proxy, this measure does not have a clear behavioral or economic interpretation, and it remains unclear, for example, what a marginal improvement implies for user engagement. 3

**中文**

在面向网络搜索的 GEO 中，生成响应通常由自由格式的文本和外部来源的引用组成，其中来源的“可见性”本质上是间接的且难以量化。为了形式化这个概念，Aggarwal 等人。 (2024) 提出了印象分数，它结合了字数、引用位置和基于 GPT-3.5 的质量评估。虽然作为替代指标很有用，但该指标没有明确的行为或经济解释，并且目前还不清楚，例如，边际改进对用户参与度意味着什么。 3

### Page 4

### 段落 19 · Page 4

**EN**

By contrast, GEO in e-commerce admits a much cleaner objective: improving a product’s rank in the generative engine’s output. This ranking signal is directly observable and reproducible through widely available LLM APIs. Moreover, a large empirical literature shows that higher rankings translate strongly into increased clicks, conversions, and revenue (e.g., see Baye et al. (2009) and references therein), making GEO performance readily interpretable in economic terms. Query Product A Product B Product C Product D Product E , GEO Generative Engine 1. Product D 2. Product B 3. Product C 4. Product E 5. Product A 1. Product E’ 2. Product D 3.

**中文**

相比之下，电子商务中的 GEO 承认了一个更清晰的目标：提高产品在生成式引擎输出中的排名。该排名信号可通过广泛使用的 LLM API 直接观察和重现。此外，大量实证文献表明，较高的排名会强烈转化为点击次数、转化次数和收入的增加（例如，参见 Baye 等人（2009）及其中的参考文献），从而使 GEO 的表现很容易用经济术语来解释。查询产品 A 产品 B 产品 C 产品 D 产品 E、GEO 生成式引擎 1. 产品 D 2. 产品 B 3. 产品 C 4. 产品 E 5. 产品 A 1. 产品 E’ 2. 产品 D 3.

### 段落 20 · Page 4

**EN**

Product B 4. Product C 5. Product A Query Product A Product B Product C Product D Product E’ , Ranking without GEO Generative Engine Ranking with GEO “I'm in my 20s, and I want to find a basic set of kitchen knives that, with proper care, will outlive me.” Product E: Knife set for kitchen… Product E’: Premium durable knife set with minimal upkeep needed Figure 2: The GEO process. A GEO module rewrites product descriptions to enhance placement in generative-engine rankings. Following Aggarwal et al. (2024), we explicitly separate retrieval and re-ranking in both formulation and implementation. This design is motivated by two considerations.

**中文**

产品 B 4. 产品 C 5. 产品 A 查询 产品 A 产品 B 产品 C 产品 D 产品 E’，不使用 GEO 生成式引擎排名 使用 GEO 排名 “我 20 多岁了，我想找到一套基本的菜刀，如果保养得当，它会比我更长寿。”产品 E：厨房刀具套装... 产品 E’：优质耐用刀具套装，只需最少的维护 图 2：GEO 流程。 GEO 模块重写产品描述，以提高在生成式引擎排名中的位置。继阿加瓦尔等人之后。 （2024），我们在制定和实施方面明确地将检索和重排分开。这种设计是出于两个考虑。

### 段落 21 · Page 4

**EN**

First, large-scale retrieval is typically handled by highly optimized, specialized systems, while re-ranking benefits from the richer contextual reasoning afforded by LLMs. Second, GEO is constrained to preserve the semantic content of product descriptions, implying that standard retrieval mechanisms, whether embedding-based or keyword-based, should be largely invariant to rewriting. Practically, a product needs to make it to the top-listed candidates first before the GEO process can make a meaningful impact on its ranking.

**中文**

首先，大规模检索通常由高度优化的专业系统处理，而重排则受益于法学硕士提供的更丰富的上下文推理。其次，GEO 仅限于保留产品描述的语义内容，这意味着标准检索机制，无论是基于嵌入的还是基于关键字的，都应该在很大程度上不受重写影响。实际上，产品需要首先进入排名靠前的候选产品，然后 GEO 流程才能对其排名产生有意义的影响。

### 段落 22 · Page 4

**EN**

4 Dataset: E-GEO 4.1 Queries E-commerce retrieval datasets are prolific (Papenmeier et al., 2021; Chen et al., 2022; Reddy et al., 2022) but not suitable for studying GEO due to fundamental differences in user queries. See Table 1 for details. This gap motivates our construction of a new dataset specifically designed for e-commerce GEO. To obtain realistic product-seeking requests, we source queries from the BuyItForLifesubreddit, 2 a community that frequently discusses durable, high-quality products to purchase. Starting with a comprehensive crawl using publicly available data dumps under the 2https://www.reddit.com/r/BuyItForLife/. 4

**中文**

4 数据集：E-GEO 4.1 查询 电子商务检索数据集非常丰富（Papenmeier 等，2021；Chen 等，2022；Reddy 等，2022），但由于用户查询的根本差异，不适合研究 GEO。详细信息请参见表 1。这一差距促使我们构建专门为电子商务 GEO 设计的新数据集。为了获得现实的产品寻求请求，我们从 BuyItForLifesubreddit 2 获取查询，该社区经常讨论要购买的耐用、高质量产品。首先使用 2https://www.reddit.com/r/BuyItForLife/ 下公开的数据转储进行全面爬网。 4

### Page 5

### 段落 23 · Page 5

**EN**

Table 1: Existing e-commerce retrieval datasets primarily contain short keyword queries, whereas our E-GEO dataset consists of rich, context-heavy natural-language requests that better reflect real interactions with shopping agents.

**中文**

表 1：现有的电子商务检索数据集主要包含短关键字查询，而我们的 E-GEO 数据集包含丰富的、上下文密集的自然语言请求，可以更好地反映与购物代理的真实交互。

### 段落 24 · Page 5

**EN**

Existing Product Search Datasets E-GEO (Ours) •white leather chair (Chen et al., 2022) •laundry basket with wheels (Chen et al., 2022) •self-seal envelopes without window (Reddy et al., 2022) •#2 pencils not sharpened (Reddy et al., 2022) •I want a laptop primarily for internet use, it needs to be light with a long battery life (Papenmeier et al., 2021) •A short zipped teddy coat, probably in pink or black (Papenmeier et al., 2021) •Request: Sandals.

**中文**

现有产品搜索数据集 E-GEO（我们的）•白色皮椅（Chen 等人，2022）•带轮子的洗衣篮（Chen 等人，2022）•无窗自封信封（Reddy 等人，2022）•#2 铅笔未削尖（Reddy 等人，2022）•我想要一台主要用于互联网使用的笔记本电脑，它需要轻便且电池寿命长（Papenmeier 等人，2021） •一件带拉链的短泰迪熊外套，可能是粉色或黑色（Papenmeier 等人，2021） •请求：凉鞋。

### 段落 25 · Page 5

**EN**

My two most recent pairs lasted about two years with frequent use (roughly three times a week), but when the last pair broke and I bought a new one, it failed within three days due to poor strap stitching. Are there any reputable brands that make good quality, sturdy sandals? Preferably slip-ons, possibly leather? I have a decent budget but nothing in the luxury brand range (e.g., Gucci). •I’m looking for an alarm clock where I can set a different alarm time for each day of the week. Other features that would be nice, but not critical, include a projection on the wall or ceiling and weather or temperature display.

**中文**

我最近的两双在频繁使用的情况下持续了大约两年（大约每周三次），但是当最后一双坏了并且我买了一双新的时，由于带子缝合不良，它在三天内就失效了。有没有信誉良好的品牌生产优质、坚固的凉鞋？最好是懒人鞋，可能是皮革的？我的预算不错，但没有奢侈品牌系列（例如古驰）。 •我正在寻找一个闹钟，可以为一周中的每一天设置不同的闹钟时间。其他功能虽然不错，但并不重要，包括墙壁或天花板上的投影以及天气或温度显示。

### 段落 26 · Page 5

**EN**

I found American Innovative’s Neverlate alarm clock, but it has poor build quality according to the comments. Is there anything similar? pushshiftsubreddit, 3 we use GPT-4o-mini to identify 141,105 recommendation-oriented requests that include nontrivial intent details and edit them minimally to ensure correct formatting. To construct a clean and manageable benchmark for GEO evaluation, we further use GPT-4o to arrive at a final set of 7,151 high-quality queries that explicitly ask for recommendations on products to purchase. Examples of queries from our dataset and existing datasets are presented in Table 1.

**中文**

我找到了 American Innovative 的 Neverlate 闹钟，但根据评论，它的做工质量很差。有类似的吗？ Pushshiftsubreddit, 3 我们使用 GPT-4o-mini 来识别 141,105 个面向推荐的请求，其中包括重要的意图详细信息，并对其进行最低程度的编辑以确保格式正确。为了构建一个干净且易于管理的 GEO 评估基准，我们进一步使用 GPT-4o 得出最终的 7,151 个高质量查询集，这些查询明确要求购买产品的推荐。表 1 列出了我们的数据集和现有数据集的查询示例。

### 段落 27 · Page 5

**EN**

4.2 Products To obtain product listings, we use the Amazon Reviews dataset (Hou et al., 2024), which contains information for over 48 million products across more than 30 categories (e.g., Electronics, Home & Kitchen). Beyond product titles, the dataset includes detailed descriptions and feature lists, providing rich textual content for GEO. For each of the 7,151 curated queries, we retrieve relevant products from this corpus using the all-MiniLM-L6-v2 sentence encoder for efficient nearest-neighbor search. We retain the top 10 products ranked by embedding cosine similarity. The final dataset contains 52,165 unique products.

**中文**

4.2 产品为了获取产品列表，我们使用亚马逊评论数据集（Hou et al., 2024），该数据集包含 30 多个类别（例如电子产品、家居和厨房）超过 4800 万种产品的信息。除了产品标题之外，数据集还包括详细的描述和功能列表，为 GEO 提供丰富的文本内容。对于 7,151 个精选查询中的每一个，我们使用全 MiniLM-L6-v2 句子编码器从该语料库中检索相关产品，以进行高效的最近邻搜索。我们保留通过嵌入余弦相似度排名的前 10 个产品。最终数据集包含 52,165 个独特产品。

### 段落 28 · Page 5

**EN**

While more advanced retrieval techniques could further improve candidate quality, we leave that to future work as such enhancements are orthogonal to our focus on GEO. 5 Experiments 5.1 Implementation Details Generative Engine.We use GPT-4o as the generative engine responsible for re-ranking. To approximate real-world behavior, we design system and user prompts that mimic typical user 3https://www.reddit.com/r/pushshift/. 5

**中文**

虽然更先进的检索技术可以进一步提高候选质量，但我们将其留给未来的工作，因为此类增强与我们对 GEO 的关注正交。 5 实验 5.1 实现细节 生成式引擎。我们使用GPT-4o 作为负责重新排序的生成式引擎。为了模拟真实世界的行为，我们设计了模仿典型用户的系统和用户提示 3https://www.reddit.com/r/pushshift/。 5

### Page 6

### 段落 29 · Page 6

**EN**

interactions (Appendix A). Specifically, we adopt the CL4R1T4S system prompt4, which is reported to resemble the web interface prompt of GPT-4o. The user prompt is intentionally minimalist, asking the model to rank ten candidate products for a given query. Although real users may exhibit a diverse range of interaction styles, this setup isolates the core ranking behavior. We observe qualitatively similar results when substituting other LLMs such as Claude.

**中文**

相互作用（附录 A）。具体来说，我们采用CL4R1T4S系统提示符4，据报道该提示符类似于GPT-4o的Web界面提示符。用户提示有意简约，要求模型针对给定查询对十个候选产品进行排名。尽管真实用户可能表现出多种交互风格，但这种设置隔离了核心排名行为。当替换其他法学硕士（例如克劳德）时，我们观察到质量相似的结果。

### 段落 30 · Page 6

**EN**

GEO Module.The GEO procedure is implemented as a rewriting LLM (also GPT-4o) controlled via its user prompt, which specifies rewriting behaviors such as adopting an advertisement-like style or emphasizing unique advantages. Appendix C.1 provides the fixed system prompt, and Appendix C.2 lists the 15 heuristic user prompts (to be optimized). As proprietary models cannot be fine-tuned directly, we treat GEO as a prompt meta-optimization problem. This design allows the direct integration of alternative prompt-optimization methods (Zhou et al., 2023; Agrawal et al., 2025) within our framework.

**中文**

GEO 模块。GEO 过程被实现为通过其用户提示控制的重写 LLM（也称为 GPT-4o），它指定重写行为，例如采用类似广告的风格或强调独特的优势。附录C.1提供了固定的系统提示，附录C.2列出了15个启发式用户提示（待优化）。由于专有模型无法直接微调，因此我们将 GEO 视为即时元优化问题。这种设计允许在我们的框架内直接集成替代提示优化方法（Zhou et al., 2023; Agrawal et al., 2025）。

### 段落 31 · Page 6

**EN**

Evaluation Metric.We evaluate GEO performance through ranking improvement. For each query, we sample a product from the retrieved candidate set and compare its rank before and after rewriting its description. The metric is the change in rank position, with positive values indicating improved placement. Overall performance is reported as the average rank change across a set of queries. 5.2 Prompt Meta-Optimization We adopt a lightweight optimization method inspired by the reflection module in GEPA (Agrawal et al., 2025), shown in Algorithm 1.

**中文**

评估指标。我们通过排名改进来评估 GEO 表现。对于每个查询，我们从检索到的候选集中抽取一个产品，并比较重写其描述之前和之后的排名。该指标是排名位置的变化，正值表示排名的提高。总体性能报告为一组查询的平均排名变化。 5.2 提示元优化 我们采用了受 GEPA 中反射模块启发的轻量级优化方法（Agrawal et al., 2025），如算法 1 所示。

### 段落 32 · Page 6

**EN**

At each iteration, the current promptπis evaluated on a training batch, and the prompt and its performance are appended to a historyH. A metaoptimizerM—implemented as a separate GPT-4o instance (prompts are in Appendix B)—receives the current prompt, its batch performance, and the full history, and produces a revised prompt via reflective self-critique. Because the procedure is zeroth-order and relies on the meta-optimizer’s implicit search, the final prompt is not necessarily optimal. We therefore maintain a validation-tracked best prompt π⋆, initialized asπ 0, and updated whenever validation performance improves.

**中文**

在每次迭代中，都会在训练批次上评估当前的提示π，并将提示及其性能附加到历史记录H中。 MetaoptimizerM（作为单独的 GPT-4o 实例实现（提示在附录 B 中））接收当前提示、其批处理性能和完整历史记录，并通过反思性自我批评生成修订后的提示。由于该过程是零阶的并且依赖于元优化器的隐式搜索，因此最终的提示不一定是最优的。因此，我们维护一个验证跟踪的最佳提示 π⋆，初始化为 π 0，并在验证性能提高时更新。

### 段落 33 · Page 6

**EN**

Upon completion of training,π ⋆ is evaluated on the test set. Although more advanced methods could be incorporated, this simple strategy already provides a strong, systematic baseline and serves as a modular interface for plugging in alternative promptoptimization algorithms. We use 1,000 queries for training, 1,000 for validation, and 5,151 for testing. Each initial prompt is optimized for a single epoch using 10 batches of size 100.

**中文**

训练完成后，在测试集上评估 π ⋆。尽管可以采用更先进的方法，但这种简单的策略已经提供了强大的系统基线，并作为插入替代提示优化算法的模块化接口。我们使用 1,000 个查询进行训练，使用 1,000 个查询进行验证，使用 5,151 个查询进行测试。每个初始提示都使用 10 个大小为 100 的批次针对单个时期进行优化。

### 段落 34 · Page 6

**EN**

Increasing the training set size or number of epochs does not meaningfully affect validation or test performance.5 5.3 Initial Prompts and Performance Inspired by prior GEO heuristics (Aggarwal et al., 2024; Berry, 2025; Madhavan, 2025), we construct 15 initial prompts spanning diverse rewriting strategies. Table 2 reports their descriptions and initial and optimized test performance; full prompts appear in Appendix C.2 and Appendix C.3. 4https://github.com/elder-plinius/CL4R1T4S. 5We trained three prompts (advertisement,clickable, andcompetitive) for five epochs.

**中文**

增加训练集大小或 epoch 数量不会对验证或测试性能产生有意义的影响。5 5.3 初始提示和性能 受先前 GEO 启发法的启发（Aggarwal 等人，2024；Berry，2025；Madhavan，2025），我们构建了 15 个涵盖不同重写策略的初始提示。表 2 报告了它们的描述以及初始和优化的测试性能；完整提示见附录 C.2 和附录 C.3。 4https://github.com/elder-plinius/CL4R1T4S。 5我们训练了五个时期的三种提示（广告、可点击和竞争性）。

### 段落 35 · Page 6

**EN**

Their test performances (mean±s.e.) were 1.25±0.04, 0.90±0.04, and 1.25±0.04, respectively, comparable to single-epoch results (1.20 ±0.04, 1.25±0.04, 1.61±0.04). Validation curves also indicate saturation after approximately 500 training queries. 6

**中文**

他们的测试表现（平均值±标准差）分别为 1.25±0.04、0.90±0.04 和 1.25±0.04，与单周期结果（1.20±0.04、1.25±0.04、1.61±0.04）相当。验证曲线还表明在大约 500 个训练查询后达到饱和。 6

### Page 7

### 段落 36 · Page 7

**EN**

Algorithm 1Prompt Meta-Optimization for GEO Require:Training setD train, validation setD val, test setD test; epochsE; batches per epochB; batch sizem; ranking modelR; rewriting modelGEO; meta-optimizer modelM 1:Initialize current promptπ←π 0 2:Initialize best promptπ ⋆ ←π 0 3:Initialize best validation score bestVal← −∞ 4:Initialize history bufferH← ∅ 5:fore= 1toEdo▷Outer loop over epochs 6:Randomly partitionD train into batches{B b}B b=1 of sizem 7:forb= 1toBdo▷Iterate over training batches 8:S (e,b) train ←Eval(GEO, π,B b, R)▷Evaluate current prompt on training batch 9:H←H∪ {(e, b, π, S (e,b) train)}▷Store trajectory for reflection 10:v←Ev

**中文**

算法1针对GEO的提示元优化需要：训练集D train，验证集D val，测试集D test；纪元E；每个时期的批次B；批量大小；排名模型R；重写模型GEO；元优化器 modelM 1:初始化当前提示π←π 0 2:初始化最佳提示π ⋆ ←π 0 3:初始化最佳验证分数 bestVal← −∞ 4:初始化历史缓冲区H← ∅ 5:fore= 1toEdo▷历元上的外循环 6:随机将D训练分成批次{B b}B b=1，大小为m 7:forb= 1toBdo▷迭代训练批次 8:S (e,b) train ←Eval(GEO, π,B b, R)▷评估训练批次的当前提示 9:H←H∪ {(e, b, π, S (e,b) train)}▷存储反射轨迹 10:v←Ev

### 段落 37 · Page 7

**EN**

al(GEO, π, D val, R)▷Compute validation performance 11:ifv >bestValthen 12:bestVal←v 13:π ⋆ ←π ▷Track best-performing prompt on validation set 14:end if 15:π←M(π, S (e,b) train, H)▷Meta-optimizer proposes revised prompt via reflection 16:end for 17:end for 18:returnπ ⋆ ▷Output best validated prompt Most human-written prompts provide little to no benefit, as 10 of the 15 yield negligible or even negative changes in ranking, and the best achieves an average improvement of only +0.71.

**中文**

al(GEO, π, D val, R)▷计算验证性能 11:ifv >bestValthen 12:bestVal←v 13:π ⋆ ←π ▷跟踪验证集上表现最佳的提示 14:end if 15:π←M(π, S (e,b) train, H)▷元优化器通过反射提出修改提示 16:end for 17:end for 18:returnπ ⋆ ▷输出最佳验证提示 大多数人工编写的提示几乎没有任何好处，因为 15 个提示中的 10 个对排名的影响可以忽略不计，甚至是负变化，而最好的提示的平均改进仅 +0.71。

### 段落 38 · Page 7

**EN**

In contrast, all optimized prompts produce consistent gains, with 11 out of 15 improving ranking by at least +1, and even the weakest optimization achieving a +0.68 improvement. Although these differences appear modest, industry estimates indicate that a single-rank increase can translate to tens of thousands of dollars in annual revenue for just one product. 6 The sharp gap between initial and optimized performance highlights the value of systematic prompt optimization over ad hoc heuristics. As a negative control, thestorytellingprompt instructs the model to produce narrative text while explicitly suppressing factual product details.

**中文**

相比之下，所有优化的提示都会产生一致的收益，15 个提示中的 11 个将排名提高了至少 +1，甚至最弱的优化也实现了 +0.68 的提升。尽管这些差异看起来不大，但行业估计表明，单排名的增长就可以转化为仅一种产品的数万美元的年收入。 6 初始性能和优化性能之间的巨大差距凸显了系统即时优化相对于临时启发式方法的价值。作为负控制，讲故事提示指示模型生成叙事文本，同时明确抑制实际的产品细节。

### 段落 39 · Page 7

**EN**

As expected, it performs poorly in its initial form (−4.03). After optimization, however, it achieves a +1.22 improvement, demonstrating the flexibility of the framework and its ability to recover effective strategies from weak starting points. 5.4 Evidence for a Universally Effective Rewriting Strategy In addition to the overall performance gains, we find that several stylistic patterns consistently emerge across the 15 optimized prompts, regardless the initial prompts. A list of 10 features of interest are described in Table 3, and their presence in each initial and optimized prompt is summarized in Figure 3.

**中文**

正如预期的那样，它的初始形式表现不佳（−4.03）。然而，优化后，它实现了 +1.22 的改进，展示了该框架的灵活性以及从弱起点恢复有效策略的能力。 5.4 普遍有效的重写策略的证据 除了整体性能提升之外，我们发现在 15 个优化提示中一致出现了几种风格模式，无论初始提示如何。表 3 列出了 10 个感兴趣的功能，图 3 总结了它们在每个初始提示和优化提示中的存在。

### 段落 40 · Page 7

**EN**

Comparison of the initial and optimized prompts reveals a striking convergence: while the initial prompts exhibit diverse and often non-overlapping features, the optimized prompts consistently show shared characteristics. Furthermore, these features areemergent: they are not explicitly programmed into the meta-optimizer but arise naturally from the optimization process. Combined with the fact that even an initial prompt as far-fetched asstorytellingcan be transformed 6https://titannetwork.com/amazon-seo 7

**中文**

初始提示和优化提示的比较揭示了惊人的趋同：虽然初始提示表现出多样化且通常不重叠的特征，但优化提示始终表现出共同的特征。此外，这些功能是新兴的：它们没有明确编程到元优化器中，而是从优化过程中自然产生。结合这样一个事实，即使是像讲故事一样牵强的最初提示也可以被转化 6https://titannetwork.com/amazon-seo 7

### Page 8

### 段落 41 · Page 8

**EN**

Table 2: Initial Prompts and Initial and Optimized Performance (Mean and Standard Error) Prompt Description Init. Prompts Optimized Advertisement Advertisement-like style.−0.43 (0.04) +1.20 (0.04) Authoritative Confident, assertive tone.−0.06 (0.04) +0.77 (0.04) Clickable Persuasive & compelling. +0.19 (0.04) +1.25 (0.04) Competitive Highlight unique advantages. +0.71 (0.04) +1.61 (0.05) Diverse Reflect inclusivity. +0.15 (0.04) +1.23 (0.04) FAQ Add an FAQ. +0.06 (0.04) +1.20 (0.04) Fluent Improve linguistic flow. +0.02 (0.04) +0.86 (0.04) Format Use headings & bullets.−0.35 (0.04) +0.68 (0.04) Language Use foreign expressions.

**中文**

表 2：初始提示以及初始和优化性能（平均误差和标准误差） 提示说明 Init。提示优化广告 类似广告的风格。−0.43 (0.04) +1.20 (0.04) 权威 自信、自信的语气。−0.06 (0.04) +0.77 (0.04) 可点击 有说服力和引人注​​目。 +0.19 (0.04) +1.25 (0.04) 竞争优势 凸显独特优势。 +0.71 (0.04) +1.61 (0.05) 多元化 体现包容性。 +0.15 (0.04) +1.23 (0.04) 常见问题解答 添加常见问题解答。 +0.06 (0.04) +1.20 (0.04) 流利 提高语言流畅性。 +0.02 (0.04) +0.86 (0.04) 格式 使用标题和项目符号。−0.35 (0.04) +0.68 (0.04) 语言 使用外语表达。

### 段落 42 · Page 8

**EN**

+0.07 (0.04) +1.10 (0.04) Minimalist Reduce to a single sentence.−1.66 (0.04) +1.10 (0.04) Quality Emphasize product quality. +0.65 (0.04) +0.69 (0.04) Storytelling Write a creative short story.−4.03 (0.05) +1.22 (0.04) Technical Use technical terminology.−0.49 (0.04) +1.17 (0.04) Trick Format like LLM output. +0.28 (0.05) +1.15 (0.04) Unique Use rare vocabulary.−0.26 (0.04) +1.10 (0.04) into an effective rewriting strategy, this convergence provides strong evidence for the existence of a broadly effective GEO strategy that transcends specific initial prompts. Furthermore, all initial prompts exceptstorytellingenforce factual preservation.

**中文**

+0.07 (0.04) +1.10 (0.04) 极简主义 简化为单个句子。−1.66 (0.04) +1.10 (0.04) 质量 强调产品质量。 +0.65 (0.04) +0.69 (0.04) 讲故事 写一个创意短篇故事。−4.03 (0.05) +1.22 (0.04) 技术 使用技术术语。−0.49 (0.04) +1.17 (0.04) 类似于 LLM 输出的技巧格式。 +0.28 (0.05) +1.15 (0.04) 独特 使用稀有词汇。−0.26 (0.04) +1.10 (0.04) 成为有效的重写策略，这种趋同为存在超越特定初始提示的广泛有效的 GEO 策略提供了强有力的证据。此外，除了讲故事之外，所有最初的提示都会强制保留事实。

### 段落 43 · Page 8

**EN**

After optimization, 12 of 15 prompts retain this constraint, suggesting that the optimizer reliably identifies factuality as a beneficial property. This suggests that the improvements produced by our GEO procedure reflect genuine, non-adversarial enhancements rather than exploitative manipulations. F eature Description Ranking Emphasizes the goal of achieving a higher rank. User Intent Anticipates and aligns with user intent. Competitiveness Compares against other products or competitors. Reviews Ratings Draws on positive customer reviews as external evidence. Compelling Adopts a compelling and persuasive narrative tone.

**中文**

优化后，15 个提示中的 12 个保留了此约束，这表明优化器可靠地将事实性识别为有益的属性。这表明我们的 GEO 程序产生的改进反映了真正的、非对抗性的增强，而不是剥削性的操纵。功能 描述 排名 强调实现更高排名的目标。用户意图 预测并符合用户意图。竞争力 与其他产品或竞争对手进行比较。评论评级 利用积极的客户评论作为外部证据。引人注目 采用令人信服且有说服力的叙述语气。

### 段落 44 · Page 8

**EN**

Authoritativeness Uses a confident and authoritative voice. Unique Selling Points Focuses on the product’s unique features. Urgent Call Includes a sense of urgency or scarcity. Easily Scannable Uses headings, bullet points, or formatting for easy reading. Maintains Factuality Preserves the original factual content of the description. Table 3: Features of Interest in Optimized Prompts 6 Discussion We present the first systematic study of generative engine optimization (GEO) in e-commerce, supported by a new dataset of realistic, intent-rich product queries paired with product listings.

**中文**

权威 使用自信和权威的声音。独特的卖点 专注于产品的独特功能。紧急呼叫 包括紧迫感或匮乏感。易于扫描 使用标题、项目符号或格式以便于阅读。保持事实性 保留描述的原始事实内容。表 3：优化提示中感兴趣的特征 6 讨论 我们首次对电子商务中的生成式引擎优化 (GEO) 进行了系统研究，并得到了与产品列表配对的真实、意图丰富的产品查询的新数据集的支持。

### 段落 45 · Page 8

**EN**

Our results demonstrate that simple, optimization-driven rewriting strategies can reliably improve product rankings in generative engine outputs and consistently outperform heuristic baselines. 8

**中文**

我们的结果表明，简单的、优化驱动的重写策略可以可靠地提高生成式引擎输出中的产品排名，并始终优于启发式基线。 8

### Page 9

### 段落 46 · Page 9

**EN**

Figure 3: Feature presence heatmaps: Initial (left) vs. Optimized (right) prompts. Red indicates absence; green indicates presence. Optimized prompts consistently incorporate key features such as ranking emphasis, user intent alignment, competitiveness, and external evidence, suggesting a universally effective rewriting strategy. Notably, most optimized prompts maintain the factuality requirement present in the initial prompts, indicating that the meta-optimization process reliably identifies factuality as an important feature.

**中文**

图 3：功能存在热图：初始（左）与优化（右）提示。红色表示缺席；绿色表示存在。优化的提示始终包含排名重点、用户意图一致性、竞争力和外部证据等关键特征，这表明了一种普遍有效的重写策略。值得注意的是，大多数优化的提示都维持初始提示中存在的事实性要求，这表明元优化过程可靠地将事实性识别为重要特征。

### 段落 47 · Page 9

**EN**

Beyond performance gains, we identify stable rewriting patterns that generalize across products and query types, suggesting that effective GEO is governed by transferable structural principles rather than ad hoc prompt engineering. Our study opens several promising directions for future research. First, an important next step is to study equilibrium dynamics when GEO becomes universally adopted, i.e., when all sellers actively optimize their product descriptions, potentially leading to congestion effects, strategic arms races, or reduced informativeness of content.

**中文**

除了性能提升之外，我们还确定了跨产品和查询类型泛化的稳定重写模式，这表明有效的 GEO 是由可转移的结构原则而不是临时提示工程控制的。我们的研究为未来的研究开辟了几个有希望的方向。首先，下一步重要的是研究 GEO 被普遍采用时的均衡动态，即所有卖家都积极优化其产品描述，这可能导致拥堵效应、战略军备竞赛或内容信息量减少。

### 段落 48 · Page 9

**EN**

Second, extending GEO to multi-modal product representations such as images and videos may yield richer optimization strategies. Finally, fairness and market-design questions arise naturally: GEO may advantage sophisticated sellers and widen platform inequalities, motivating work on regulation, guardrails, and platform-level design. Overall, we believe that GEO represents a fertile intersection of LLM capabilities, e-commerce dynamics, and optimization theory, with many exciting avenues for future exploration. We hope our work serves as a foundation for this emerging area. 9

**中文**

其次，将 GEO 扩展到图像和视频等多模式产品表示可能会产生更丰富的优化策略。最后，公平和市场设计问题自然而然地出现：GEO 可能会给成熟的卖家带来优势并扩大平台不平等，从而推动监管、护栏和平台级设计方面的工作。总的来说，我们相信 GEO 代表了法学硕士能力、电子商务动态和优化理论的丰富交集，为未来的探索提供了许多令人兴奋的途径。我们希望我们的工作能够成为这个新兴领域的基础。 9

### Page 10

### 段落 49 · Page 10

**EN**

References Aggarwal, P.,Murahari, V.,Rajpurohit, T.,Kalyan, A.,Narasimhan, K.andDeshpande, A.(2024). Geo: Generative engine optimization. InProceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining. KDD ’24, Association for Computing Machinery, New York, NY, USA. URLhttps://doi.org/10.1145/3637528.3671900 Agrawal, L. A.,Tan, S.,Soylu, D.,Ziems, N.,Khare, R.,Opsahl-Ong, K.,Singhvi, A., Shandilya, H.,Ryan, M. J.,Jiang, M.,Potts, C.,Sen, K.,Dimakis, A. G.,Stoica, I., Klein, D.,Zaharia, M.andKhattab, O.(2025). Gepa: Reflective prompt evolution can outperform reinforcement learning.

**中文**

参考文献 Aggarwal, P.、Murahari, V.、Rajpurohit, T.、Kalyan, A.、Narasimhan, K. 和 Deshpande, A.(2024)。 Geo：生成式引擎优化。第 30 届 ACM SIGKDD 知识发现和数据挖掘会议论文集。 KDD '24，计算机协会，美国纽约州纽约市。 URLhttps://doi.org/10.1145/3637528.3671900 Agrawal, L. A.,Tan, S.,Soylu, D.,Ziems, N.,Khare, R.,Opsahl-Ong, K.,Singhvi, A., Shandilya, H.,Ryan, M. J.,Jiang, M.,Potts, C.、Sen, K.、Dimakis, A. G.、Stoica, I.、Klein, D.、Zaharia, M. 和 Khattab, O.(2025)。 Gepa：反思性即时进化可以胜过强化学习。

### 段落 50 · Page 10

**EN**

URLhttps://arxiv.org/abs/2507.19457 Allouah, A.,Besbes, O.,Figueroa, J. D.,Kanoria, Y.andKumar, A.(2025). What is your ai agent buying? evaluation, implications and emerging questions for agentic e-commerce. URLhttps://arxiv.org/abs/2508.02630 Baye, M. R.,Gatti, J. R. J.,Kattuman, P.andMorgan, J.(2009). Clicks, discontinuities, and firm demand online.Journal of Economics & Management Strategy18935–975. Bellan, R.(2025). Openai takes on google, amazon with new agentic shopping system.https://techcrunch.com/2025/09/29/ openai-takes-on-google-amazon-with-new-agentic-shopping-system/. Berry, S.(2025). What is answer engine optimization?

**中文**

网址 https://arxiv.org/abs/2507.19457 Allouah, A.、Besbes, O.、Figueroa, J. D.、Kanoria, Y. 和 Kumar, A.(2025)。你的人工智能代理在买什么？代理电子商务的评估、影响和新出现的问题。 URL https://arxiv.org/abs/2508.02630 Baye, M. R.,Gatti, J. R. J.,Kattuman, P. 和 Morgan, J.(2009)。在线点击、不连续性和坚定需求。经济与管理策略杂志18935–975。贝兰，R.（2025）。 Openai 通过新的代理购物系统挑战谷歌和亚马逊。https://techcrunch.com/2025/09/29/openai-takes-on-google-amazon-with-new-agentic-shopping-system/。贝里，S.（2025）。什么是答案引擎优化？

### 段落 51 · Page 10

**EN**

the seo’s guide to aeo.https://www. seo.com/ai/answer-engine-optimization/. Chen, Y.,Liu, S.,Liu, Z.,Sun, W.,Baltrunas, L.andSchroeder, B.(2022). Wands: Dataset for product search relevance assessment. InAdvances in Information Retrieval(M. Hagen, S. Verberne, C. Macdonald, C. Seifert, K. Balog, K. Nørv˚ ag and V. Setty, eds.). Springer International Publishing, New York, NY, USA. Hou, Y.,Li, J.,He, Z.,Yan, A.,Chen, X.andMcAuley, J.(2024). Bridging language and items for retrieval and recommendation. URLhttps://arxiv.org/abs/2403.03952 Kumar, A.andLakkaraju, H.(2024). Manipulating large language models to increase product visibility.

**中文**

seo 的 aeo 指南。https://www. seo.com/ai/answer-engine-optimization/。陈 Y.、刘 S.、刘 Z.、孙 W.、Baltrunas, L. 和 Schroeder, B.(2022)。 Wands：用于产品搜索相关性评估的数据集。信息检索进展（M. Hagen、S. Verberne、C. Macdonald、C. Seifert、K. Balog、K. Nørvü ag 和 V. Setty 编辑）。施普林格国际出版社，美国纽约州纽约市。侯 Y.、李 J.、何 Z.、严 A.、陈 X. 和麦考利 J.(2024)。桥接语言和项目以进行检索和推荐。网址 https://arxiv.org/abs/2403.03952 Kumar, A. 和 Lakkaraju, H. (2024)。操纵大型语言模型以提高产品可见性。

### 段落 52 · Page 10

**EN**

URLhttps://arxiv.org/abs/2404.07981 Lewis, P.,Perez, E.,Piktus, A.,Petroni, F.,Karpukhin, V.,Goyal, N.,K ¨uttler, H., Lewis, M.,Yih, W.-t.,Rockt ¨aschel, T.,Riedel, S.andKiela, D.(2020). Retrievalaugmented generation for knowledge-intensive nlp tasks. InProceedings of the 34th International Conference on Neural Information Processing Systems. NIPS ’20, Curran Associates Inc., Red Hook, NY, USA. Lyu, L.,Siderius, J.,Li, H.,Acemoglu, D.,Huttenlocher, D.andOzdaglar, A.(2025). Wikipedia contributions in the wake of chatgpt. InCompanion Proceedings of the ACM on Web Conference 2025. WWW ’25, Association for Computing Machinery, New York, NY, USA.

**中文**

URLhttps://arxiv.org/abs/2404.07981 Lewis, P.,Perez, E.,Piktus, A.,Petroni, F.,Karpukhin, V.,Goyal, N.,K uttler, H., Lewis, M.,Yih, W.-t.,Rockt ¡aschel, T.,Riedel, S.andKiela, D.（2020）。知识密集型 NLP 任务的检索生成。第 34 届国际神经信息处理系统会议论文集。 NIPS ’20，Curran Associates Inc.，美国纽约州雷德胡克。 Lyu, L.、Siderius, J.、Li, H.、Acemoglu, D.、Huttenlocher, D. 和 Ozdaglar, A.(2025)。 chatgpt 之后的维基百科贡献。 In Companion Proceedings of the ACM on Web Conference 2025. WWW '25，计算机协会，纽约，纽约州，美国。

### 段落 53 · Page 10

URLhttps://doi.org/10.1145/3701716.3715543 10

### Page 11

### 段落 54 · Page 11

**EN**

Madhavan, K.(2025). Optimizing your content for inclusion in ai search answers.https://about.ads.microsoft.com/en/blog/post/october-2025/ optimizing-your-content-for-inclusion-in-ai-search-answers. Mehta, R.andChilimbi, T.(2024). Amazon announces rufus, a new generative ai-powered conversational shopping experience.https://www.aboutamazon.com/news/retail/amazon-rufus. Papenmeier, A.,Kern, D.,Hienert, D.,Sliwa, A.,Aker, A.andFuhr, N.(2021). Dataset of natural language queries for e-commerce. InProceedings of the 2021 Conference on Human Information Interaction and Retrieval. CHIIR ’21, Association for Computing Machinery, New York, NY, USA.

**中文**

马达万，K.（2025）。优化您的内容以包含在人工智能搜索答案中。https://about.ads.microsoft.com/en/blog/post/october-2025/optimization-your-content-for-inclusion-in-ai-search-answers。梅塔，R. 和奇林比，T. (2024)。亚马逊宣布推出 rufus，这是一种新的人工智能驱动的对话式购物体验。https://www.aboutamazon.com/news/retail/amazon-rufus。 Papenmeier, A.、Kern, D.、Hienert, D.、Sliwa, A.、Aker, A. 和 Fuhr, N.(2021)。电子商务自然语言查询数据集。 2021 年人类信息交互与检索会议论文集。 CHIIR ’21，计算机协会，美国纽约州纽约市。

### 段落 55 · Page 11

**EN**

URLhttps://doi.org/10.1145/3406522.3446043 Pfrommer, S.,Bai, Y.,Gautam, T.andSojoudi, S.(2024). Ranking manipulation for conversational search engines. InProceedings of the 2024 Conference on Empirical Methods in Natural Language Processing(Y. Al-Onaizan, M. Bansal and Y.-N. Chen, eds.). Association for Computational Linguistics, Miami, Florida, USA. URLhttps://aclanthology.org/2024.emnlp-main.534/ Reddy, C. K.,M `arquez, L.,Valero, F.,Rao, N.,Zaragoza, H.,Bandyopadhyay, S., Biswas, A.,Xing, A.andSubbian, K.(2022). Shopping queries dataset: A large-scale esci benchmark for improving product search.

**中文**

网址https://doi.org/10.1145/3406522.3446043 Pfrommer, S.、Bai, Y.、Gautam, T. 和Sojoudi, S.(2024)。对话式搜索引擎的排名操作。 2024 年自然语言处理经验方法会议论文集（Y. Al-Onaizan、M. Bansal 和 Y.-N. Chen 编辑）。计算语言学协会，美国佛罗里达州迈阿密。 URL https://aclanthology.org/2024.emnlp-main.534/ Reddy, C. K.,M `arquez, L.,Valero, F.,Rao, N.,Zaragoza, H.,Bandyopadhyay, S., Biswas, A.,Xing, A.andSubbian, K.(2022)。购物查询数据集：用于改进产品搜索的大规模 esci 基准。

### 段落 56 · Page 11

**EN**

URLhttps://arxiv.org/abs/2206.06588 Sommerfeld, N.,McCurry, M.andHarrington, D.(2025). Goodbye clicks, hello ai: Zero-click search redefines marketing.https://www.bain.com/insights/ goodbye-clicks-hello-ai-zero-click-search-redefines-marketing/. Toscano, J.(2025). Ai is destroying seo. rank now requires answer engine optimization.https://www.forbes.com/sites/joetoscano1/2025/09/03/ ai-is-destroying-seo-rank-now-requires-answer-engine-optimization/. Wu, L.,Zheng, Z.,Qiu, Z.,Wang, H.,Gu, H.,Shen, T.,Qin, C.,Zhu, C.,Zhu, H.,Liu, Q.,Xiong, H.andChen, E.(2024). A survey on large language models for recommendation. World Wide Web27.

**中文**

网址https://arxiv.org/abs/2206.06588 Sommerfeld, N.、McCurry, M.和Harrington, D.(2025)。再见点击，你好人工智能：零点击搜索重新定义了营销。https://www.bain.com/insights/goodbye-clicks-hello-ai-zero-click-search-redefines-marketing/。托斯卡诺，J.（2025）。艾正在摧毁搜索引擎优化。排名现在需要答案引擎优化。https://www.forbes.com/sites/joetoscano1/2025/09/03/ai-is-destroying-seo-rank-now-requires-answer-engine-optimization/。吴L.，郑Z.，邱Z.，王H.，顾H.，沉T.，秦C.，朱C.，朱H.，刘Q.，熊H.和陈E.(2024)。针对推荐的大型语言模型的调查。万维网27．

### 段落 57 · Page 11

**EN**

URLhttps://doi.org/10.1007/s11280-024-01291-2 Zhou, Y.,Muresanu, A. I.,Han, Z.,Paster, K.,Pitis, S.,Chan, H.andBa, J.(2023). Large language models are human-level prompt engineers. InThe Eleventh International Conference on Learning Representations. Kigali, Rwanda. URLhttps://openreview.net/pdf?id=92gvk82DE- 11

**中文**

网址https://doi.org/10.1007/s11280-024-01291-2 Zhou, Y.,Muresanu, A. I.,Han, Z.,Paster, K.,Pitis, S.,Chan, H.andBa, J.(2023)。大型语言模型是人类级别的提示工程师。在第十一届学习表征国际会议上。卢旺达基加利。网址https://openreview.net/pdf?id=92gvk82DE-11

### Page 12

### 段落 58 · Page 12

**EN**

A Re-ranker Prompts Prompts have been formatted and adapted for presentation. Raw prompts can be found athttps: //github.com/psbagga17/E-GEO. Ranking System Prompt You are ChatGPT, a large language model trained by OpenAI, based on the GPT-4o architecture. Knowledge cutoff: 2024-06 Current date: 2025-10-08 Image input capabilities: Enabled Personality: v2 Engage warmly yet honestly with the user. Be direct; avoid ungrounded or sycophantic flattery. Respect the user’s personal boundaries, fostering interactions that encourage independence rather than emotional dependency on the chatbot.

**中文**

重新排序提示 提示已被格式化并适合演示。原始提示可以在 https://github.com/psbagga17/E-GEO 找到。排名系统提示您是ChatGPT，是OpenAI训练的大型语言模型，基于GPT-4o架构。知识截止日期：2024-06 当前日期：2025-10-08 图像输入功能：启用 个性：v2 热情而诚实地与用户互动。直接；避免毫无根据或阿谀奉承。尊重用户的个人界限，促进鼓励独立的互动，而不是对聊天机器人的情感依赖。

### 段落 59 · Page 12

**EN**

Maintain professionalism and grounded honesty that best represents OpenAI and its values. ... F ull prompt available here:CL4R1T4S Extracted System Prompts Ranking User Prompt Here is my query:{query} Here are the products:{formatted products} Can you rank these products from best to worst based on which one I should buy for my query? Make sure to rank EVERY product and include them ALL in your answer. DO NOT leave any out. Please provide your answer as a JSON object containing the product numbers in order from best (1st) to worst (last). Example format:{{“ranking”: [<your ranking here>]}} Return ONLY the JSON object, no additional text.

**中文**

保持最能代表 OpenAI 及其价值观的专业精神和扎根的诚实。 ... 此处提供完整提示：CL4R1T4S 提取的系统提示排名用户提示 这是我的查询：{查询} 以下是产品：{格式化产品} 您能否根据我应该为查询购买哪一款产品，从最好到最差对这些产品进行排名？确保对每个产品进行排名并将它们全部包含在您的答案中。不要遗漏任何内容。请以 JSON 对象的形式提供您的答案，其中包含按从最佳（第一个）到最差（最后）的顺序排列的产品编号。示例格式：{{“ranking”: [<your rating here>]}} 仅返回 JSON 对象，无其他文本。

### 段落 60 · Page 12

**EN**

B Meta-Optimizer Prompts Meta-Optimizer System Prompt You are an expert in prompt engineering, marketing, and writing. Your goal is to improve the rewriting prompt so that when it rewrites a product description, that product ranks higher compared to other products. Meta-Optimizer User Prompt I need you to improve a prompt that rewrites product descriptions to make them rank higher in product comparisons. CONTEXT: We have a system where: 1. A product description is rewritten using a prompt (the one we’re 12

**中文**

B Meta-Optimizer 提示 Meta-Optimizer 系统提示 您是提示工程、营销和写作方面的专家。您的目标是改进重写提示，以便在重写产品描述时，该产品的排名比其他产品更高。元优化器用户提示 我需要您改进重写产品描述的提示，以使它们在产品比较中排名更高。背景：我们有一个系统： 1. 使用提示重写产品描述（我们 12 岁的那个）

### Page 13

### 段落 61 · Page 13

**EN**

optimizing) 2. The rewritten description is shown to an LLM alongside other products and a user query 3. The LLM ranks all products from best to worst for the query 4.

**中文**

优化） 2. 重写的描述与其他产品和用户查询一起显示给 LLM 3. LLM 对查询从最好到最差对所有产品进行排名 4.

### 段落 62 · Page 13

**EN**

We measure how much the rewritten product’s ranking improved (lower position = better) CURRENT REWRITING PROMPT: {current prompt} PERFORMANCE ON{batch size}QUERIES: - Mean ranking improvement:{mean:}positions (positive = moved up in ranking) - Standard deviation:{std:} - Success rate (improved ranking):{improvement rate:}% - Median improvement:{median:.3f} - Total experiments:{total} - Improved (ranked higher):{improved} - Degraded (ranked lower):{degraded} - No change:{neutral} HISTOGRAM OF IMPROVEMENTS: (Positive numbers = product ranked higher, negative = ranked lower) {histogram text} {history section} YOUR TASK: 1.

**中文**

我们测量重写产品的排名提高了多少（位置较低 = 更好） 当前重写提示：{当前提示} {批量大小}查询的性能： - 平均排名改进：{mean:}位置（正 = 排名上升） - 标准差：{std:} - 成功率（排名提高）：{改进率：}% - 中值改进：{median:.3f} - 实验总数：{total} -改进（排名较高）：{改进} - 降级（排名较低）：{降级} - 无变化：{中性} 改进直方图：（正数 = 产品排名较高，负数 = 排名较低）{直方图文本} {历史部分} 您的任务： 1.

### 段落 63 · Page 13

**EN**

Analyze the current prompt’s weaknesses 2. Explain your meta-reasoning about what makes products rank higher 3. Suggest specific improvements 4.

**中文**

分析当前提示的弱点 2. 解释你对是什么让产品排名更高的元推理 3. 提出具体改进建议 4.

### 段落 64 · Page 13

**EN**

Provide a complete new rewriting prompt IMPORTANT: - The new prompt must include{{description}}placeholder where the product description will be inserted - The prompt should instruct the LLM to rewrite the description, not just analyze it - Focus on what makes a product description MORE LIKELY TO RANK HIGHER in comparisons - Maintain factual accuracy while improving appeal Return your response in this EXACT format: —ANALYSIS— [Explain what the current prompt is doing and its weaknesses] —META-REASONING— [Your reasoning about what makes product descriptions rank higher and how the prompt should guide that] —IMPROVEMENTS— [Specific improvements you’re making to the prompt] —NEW REWRITING PROMPT— [The complete new prompt that will rewrite product descriptions.

**中文**

提供完整的新重写提示 重要： - 新提示必须包含将插入产品描述的{{description}}占位符 - 提示应指示 LLM 重写描述，而不仅仅是分析它 - 重点关注使产品描述在比较中更有可能排名靠前的因素 - 保持事实准确性，同时提高吸引力 以这种精确格式返回您的回答： —分析 — [解释当前提示的作用及其弱点] —元推理 — [您对如何使产品描述排名更高以及提示应如何指导这一点的推理] - 改进 - [您对提示进行的具体改进] - 新重写提示 - [将重写产品描述的全新提示。

### 段落 65 · Page 13

**EN**

Must include{{description}}placeholder] 13

**中文**

必须包含{{描述}}占位符] 13

### Page 14

### 段落 66 · Page 14

**EN**

C GEO Prompts C.1 Fixed System Prompt Optimizer System Prompt You are an expert ml researcher having previous background in SEO and search engines in general. You are working on novel research ideas for next generation of e-commerce websites. These websites will have language models augmented with search engines, with the task of recommending products based on the catalog of products backed by the search engine. This new set of systems will be collectively called language engines (generative search engines). This will require e-commerce businesses to update their SEO techniques so that the product ranks higher in the llm generated answer.

**中文**

C GEO 提示 C.1 固定系统提示 优化器系统提示 您是一位机器学习专家研究员，具有 SEO 和搜索引擎的一般背景。您正在为下一代电子商务网站研究新颖的研究想法。这些网站将具有通过搜索引擎增强的语言模型，其任务是根据搜索引擎支持的产品目录推荐产品。这套新系统将统称为语言引擎（生成式搜索引擎）。这将要求电子商务企业更新其 SEO 技术，以便产品在 llm 生成的答案中排名更高。

### 段落 67 · Page 14

**EN**

Specifically they will use GEO (Generative Engine Optimization) techniques to boost their visibility in the final rankings outputted by the Language Engine. C.2 Initial User Prompts Advertisement Transform the following product description into an advertisement format that is engaging and persuasive. Use catchy phrases, slogans, and a call-to-action to entice potential customers. Maintain the core information about the product, but present it in a way that highlights its benefits and unique selling points. Use marketing techniques to create a sense of urgency or exclusivity.

**中文**

具体来说，他们将使用 GEO（生成式引擎优化）技术来提高其在语言引擎输出的最终排名中的可见度。 C.2 初始用户提示广告 将以下产品描述转换为具有吸引力和说服力的广告格式。使用朗朗上口的短语、口号和号召性用语来吸引潜在客户。保留有关产品的核心信息，但以突出其优点和独特卖点的方式呈现。使用营销技巧来营造紧迫感或排他性感。

### 段落 68 · Page 14

**EN**

You may also research and use popular advertisement styles and formats to guide your rewriting. You can find inspiration and tricks from successful ads in similar product categories. Description:{description} Authoritative Transform the following product description into an authoritative style without adding or removing any core information. The revised description should reflect confidence, expertise, and assertiveness, while maintaining the original content’s meaning and relevance. The description should be assertive in its statements, such that reader believes that this is more valuable product than other products.

**中文**

您还可以研究和使用流行的广告风格和格式来指导您的重写。您可以从类似产品类别的成功广告中找到灵感和技巧。描述：{description} 权威性 将以下产品描述转换为权威风格，无需添加或删除任何核心信息。修改后的描述应体现信心、专业知识和自信，同时保持原始内容的含义和相关性。描述的陈述应该是自信的，以便读者相信这是比其他产品更有价值的产品。

### 段落 69 · Page 14

**EN**

End Goal is to increase the ranking of the product, by assertively saying that this is the best product for the user. However, the content should remain the same. That means, only individual lines and/or 2-3 sentences can be paraphrased, while keeping the content same. Description:{description} Remember to be authoritative, but keep the content of text the same. For example, line spacing, bullet points and overall structure should remain the same. No addition or deletion of content is allowed. Note we have to convince the reader that this is an relevant product by saying it authoritatively in 14

**中文**

最终目标是通过自信地说这是对用户来说最好的产品来提高产品的排名。但是，内容应保持不变。这意味着，只能对单行和/或 2-3 个句子进行释义，同时保持内容相同。描述：{description} 记住要具有权威性，但保持文本内容相同。例如，行距、要点和整体结构应保持不变。不允许添加或删除内容。请注意，我们必须在 14 中以权威的方式让读者相信这是一个相关产品

### Page 15

### 段落 70 · Page 15

**EN**

the description itself. For example the addition of phrases such as “only we are authentic etc”, “we guarantee”, use of second pronouns such as “you will not regret” etc is expected within the content itself. Clickable Enhance the following product description to make it more clickable and engaging, without changing the core information. Use persuasive language and compelling phrases that encourage users to click on the product when they see it among other options. Make sure the description highlights the product’s key benefits and unique selling points in an appealing way.

**中文**

描述本身。例如，内容本身中预计会添加“只有我们是真实的”、“我们保证”等短语、使用“您不会后悔”等第二代词。可点击 增强以下产品描述，使其更具可点击性和吸引力，而无需更改核心信息。使用有说服力的语言和引人注目的短语，鼓励用户在看到产品和其他选项时点击该产品。确保描述以有吸引力的方式突出产品的主要优点和独特卖点。

### 段落 71 · Page 15

**EN**

Description:{description} Competitive Rewrite the following product description to highlight what makes this product superior compared to others in its category. Use confident but factual comparisons, without mentioning specific competitors. Emphasize unique features, innovations, and advantages that set it apart, while maintaining factual consistency with the original text. Do not change the core information, but make it clear why this product is the best choice. Description:{description} Diverse Revise the following product description to include and highlight diverse references and perspectives, without altering the core information.

**中文**

描述：{description} 竞争性 重写以下产品描述，以突出显示该产品相对于同类产品的优越性。使用自信但事实的比较，而不提及特定的竞争对手。强调其独特之处、创新和优势，同时保持与原文的事实一致性。不要更改核心信息，但要明确为什么该产品是最佳选择。描述：{description} 多样化 修改以下产品描述，以包含并突出显示多样化的参考资料和观点，而无需更改核心信息。

### 段落 72 · Page 15

**EN**

Ensure that the description reflects inclusivity and appeals to a broad audience. Highlight features and aspects of the product that are diverse in nature. Description:{description} F AQ Revise the following product description by adding FAQ sections that address common questions related to the product. You should keep as much of the original description as you decide is necessary to accommodate the FAQ sections. Ensure that the FAQ sections are relevant and provide clear, concise answers to potential customer inquiries. Your goal is to enhance the description’s informativeness and user-friendliness making it more appealing to the user.

**中文**

确保描述反映包容性并吸引广泛的受众。突出产品本质上多样化的特征和方面。描述：{description} 常见问题解答 通过添加解决与产品相关的常见问题的常见问题解答部分来修改以下产品描述。您应该保留尽可能多的原始描述，以容纳常见问题解答部分。确保常见问题解答部分相关，并为潜在客户的询问提供清晰、简洁的答案。您的目标是增强描述的信息量和用户友好性，使其对用户更具吸引力。

### 段落 73 · Page 15

**EN**

Description:{description} Fluent Rewrite the following product description to make it more fluent without altering the core content. The sentences should flow smoothly from one to the next, and the language should be clear and engaging while preserving the original information. 15

**中文**

描述：{description} Fluent 在不改变核心内容的情况下重写以下产品描述，使其更加流畅。句子应从一个句子到下一个句子流畅，语言应清晰且引人入胜，同时保留原始信息。 15

### Page 16

### 段落 74 · Page 16

**EN**

Description:{description} F ormat Improve the following product description by implementing best practices for content formatting that enhances readability and user engagement. Use clear headings and subheadings to organize content logically. Incorporate bullet points and numbered lists to break down complex information. Rewrite the description in markdown format for better presentation. Structure content with headings and lists: Break information into digestible chunks with clear H2s, H3s, and bullet points. Ensure content accuracy and freshness: Answer engines favor content that is authoritative and up-to-date.

**中文**

描述：{description} 格式 通过实施内容格式最佳实践来改进以下产品描述，从而增强可读性和用户参与度。使用清晰的标题和副标题来逻辑地组织内容。合并要点和编号列表来分解复杂的信息。以 Markdown 格式重写描述，以便更好地呈现。使用标题和列表构建内容：使用清晰的 H2、H3 和要点将信息分解为易于理解的块。确保内容的准确性和新鲜度：答案引擎青睐权威且最新的内容。

### 段落 75 · Page 16

**EN**

Description:{description} Language Enhance the following product description by incorporating words and phrases from other languages that convey unique concepts or emotions. Ensure that these additions enrich the content and are relevant to the product, while preserving the original meaning. Your goal is to entice the user by adding exotic and intriguing linguistic elements like keywords from other languages that do not have direct English translations. Use these terms to elevate the tone, evoke sophistication, or create an emotional connection — while keeping the original meaning intact.

**中文**

描述：{description} 语言 通过合并其他语言中传达独特概念或情感的单词和短语来增强以下产品描述。确保这些添加丰富了内容并与产品相关，同时保留了原始含义。您的目标是通过添加异国情调和有趣的语言元素（例如没有直接英语翻译的其他语言的关键字）来吸引用户。使用这些术语可以提升语气、唤起复杂感或建立情感联系，同时保持原始含义不变。

### 段落 76 · Page 16

**EN**

Select expressions that naturally complement the product’s domain (e.g., French for fashion and such). Include select words or phrases from other languages that are commonly recognized and enrich the tone like “je ne sais quoi”, “carpe die”, “feng shui”, “hygge”, “mantra”. Make sure the overall description remains coherent and engaging. Description:{description} Minimalist Reduce the following product description into a single, short sentence using plain factual language. Do not attempt to persuade or embellish — simply summarize the essence of the product as concisely as possible.

**中文**

选择与产品领域自然互补的表达方式（例如，法语代表时尚等）。包括从其他语言中选择的普遍认可的单词或短语，并丰富语气，如“je ne sais quoi”、“carpe die”、“feng shui”、“hygge”、“mantra”。确保整体描述保持连贯且引人入胜。描述：{description} 极简主义 使用简单的事实语言将以下产品描述简化为一个简短的句子。不要试图说服或修饰——尽可能简洁地总结产品的本质。

### 段落 77 · Page 16

**EN**

Description:{description} Quality Revise the following product description so that it emphasizes the high quality of the product. Focus on what the customer gains from using this product, rather than just listing features. Emphesize that the key features and/or materials used in the product are of superior quality. Emphesize the quality of the overall product and how it stands out in terms of value and user satisfaction. Maintain factual accuracy and original information, but restructure sentences to highlight value and outcomes. Description:{description} 16

**中文**

描述：{description} 质量 修改以下产品描述，以强调产品的高质量。关注客户从使用该产品中获得的收益，而不仅仅是列出功能。强调产品中使用的关键特征和/或材料具有卓越的品质。强调整体产品的质量以及它如何在价值和用户满意度方面脱颖而出。保持事实准确性和原始信息，但重组句子以突出价值和结果。描述：{描述} 16

### Page 17

### 段落 78 · Page 17

**EN**

Storytelling Rewrite the following product description as a short story, focusing on narrative elements rather than factual information. Use creative language and storytelling techniques to engage the reader, but do not include specific product details or features. Create characters and settings if needed. Description:{description} T echnical Make the following product description more technical, using giving more technical terms and facts where needed while ensuring the key information is still conveyed. Do not omit, add, or alter any core information in the process.

**中文**

讲故事 将以下产品描述重写为短篇故事，重点关注叙述元素而不是事实信息。使用创造性的语言和讲故事的技巧来吸引读者，但不包括具体的产品细节或功能。如果需要，创建角色和设置。描述：{description} 技术性 使以下产品描述更具技术性，在需要时提供更多技术术语和事实，同时确保仍然传达关键信息。请勿遗漏、添加或更改流程中的任何核心信息。

### 段落 79 · Page 17

**EN**

Remember the end-goal is that very knowledgeable readers give more attention to this product, when presented with a series of other products, so make the language such that it has more technical information or existing information is presented in more technical fashion. However, do not add or delete any content. The number of words in the initial description should be the same as that in the final. The length of the new description should be the same as the original. Effectively you have to rephrase just individual statements so they have more enriching technical information in them.

**中文**

请记住，最终目标是知识渊博的读者在展示一系列其他产品时会更加关注该产品，因此使语言包含更多技术信息或以更具技术性的方式呈现现有信息。但是，请勿添加或删除任何内容。初始描述的字数应与最终描述的字数相同。新描述的长度应与原始描述的长度相同。实际上，您只需重新措辞个别陈述，以便其中包含更丰富的技术信息。

### 段落 80 · Page 17

**EN**

Description:{description} T rick Enhance the following product description, so that an LLM is more likely to rank it higher in product rankings. Your goal is to change the format of the text such that it aligns better with LLM ranking algorithms. Use features and language like specific style and/or grammar changes that are known to influence LLM ranking positively. Reorder or rephrase content to align with LLM ranking preferences, while keeping the core information intact. You may include subtle cues or keywords that are favored by LLMs in ranking tasks. You should research and apply known strategies for optimizing text for LLM ranking.

**中文**

描述：{description} 技巧 增强以下产品描述，以便法学硕士更有可能在产品排名中将其排名更高。您的目标是更改文本格式，使其与 LLM 排名算法更好地保持一致。使用已知会对 LLM 排名产生积极影响的功能和语言，例如特定的风格和/或语法变化。对内容重新排序或重新表述，以符合法学硕士排名偏好，同时保持核心信息完整。您可以在排名任务中加入法学硕士喜欢的微妙线索或关键词。您应该研究并应用已知的策略来优化 LLM 排名的文本。

### 段落 81 · Page 17

**EN**

Do not alter the factual content, but optimize the presentation for better LLM ranking outcomes. Description:{description} Unique Revise the following product description by incorporating more unique and rare words, without altering the core information. Ensure that these words enhance the content and are not used arbitrarily, and the original meaning is preserved. Description:{description} 17

**中文**

不要改变事实内容，但要优化演示以获得更好的 LLM 排名结果。描述：{description} Unique 在不改变核心信息的情况下，通过加入更多独特和罕见的词语来修改以下产品描述。确保这些词语增强内容，不被随意使用，并保留原始含义。描述：{描述} 17

### Page 18

### 段落 82 · Page 18

**EN**

C.3 Optimized User Prompts Advertisement Rewrite the following product description to optimize its ranking in product comparisons. Focus on tailoring the content to address specific user queries and buyer personas with precision. Highlight the product’s most compelling and unique advantages over competitors, using direct comparisons where applicable. Seamlessly integrate relevant keywords that align with common search terms. Build credibility by incorporating strong social proof, such as authentic testimonials or reviews. Craft a narrative that combines factual benefits with emotional engagement.

**中文**

C.3 优化用户提示广告 重写以下产品描述，以优化其在产品比较中的排名。专注于定制内容，以精确解决特定的用户查询和买家角色。在适用的情况下使用直接比较，突出产品相对于竞争对手最引人注目和最独特的优势。无缝集成与常见搜索词相符的相关关键字。通过结合强有力的社会证据（例如真实的推荐或评论）来建立可信度。精心设计一个将事实利益与情感投入结合起来的叙述。

### 段落 83 · Page 18

**EN**

Conclude with a clear, urgent, and persuasive call to action that encourages immediate response. Description:{description} Authoritative Revise the following product description to clearly and confidently communicate its unique value while maintaining factual accuracy. Transform the language to be engaging and relevant to potential user queries, emphasizing why this product is superior. You may adjust the structure slightly to better highlight key features and benefits, but do not add or remove core information. Use persuasive language that directly addresses the user’s needs and showcases the product’s advantages over competitors.

**中文**

最后发出明确、紧急且有说服力的行动号召，鼓励立即做出反应。描述：{description} 权威性修改以下产品描述，以清晰、自信地传达其独特价值，同时保持事实准确性。将语言转变为具有吸引力且与潜在用户查询相关的语言，强调该产品为何优越。您可以稍微调整结构以更好地突出关键功能和优点，但不要添加或删除核心信息。使用有说服力的语言，直接满足用户的需求并展示产品相对于竞争对手的优势。

### 段落 84 · Page 18

**EN**

Description:{description} Ensure the revised description is both authoritative and empathetic, appealing directly to the reader’s interests and needs. Use phrases that convey confidence, such as “experience unmatched quality” or “designed for your ultimate satisfaction,” while maintaining the integrity of the original content. Clickable Revise the following product description to maximize its ranking in product comparisons by focusing on: - Seamlessly integrating relevant keywords and phrases to align with common search queries and improve SEO.

**中文**

描述：{description} 确保修订后的描述既具有权威性又具有同理心，能够直接吸引读者的兴趣和需求。使用表达信心的短语，例如“体验无与伦比的品质”或“为您的最终满意而设计”，同时保持原始内容的完整性。 Clickable 修改以下产品描述，以最大限度地提高其在产品比较中的排名，重点关注： - 无缝集成相关关键字和短语，以与常见搜索查询保持一致并改进 SEO。

### 段落 85 · Page 18

**EN**

- Highlighting distinctive features and benefits in a way that clearly differentiates the product from competitors, using specific, comparative language. - Structuring the description with bullet points for clarity and emphasis on critical information. - Balancing factual accuracy with a narrative that resonates emotionally with users, addressing both their needs and desires. - Proactively addressing potential user objections or concerns to enhance trust and credibility. - Leveraging user testimonials or expert endorsements to further increase the product’s appeal and reliability. Description:{description} 18

**中文**

- 使用特定的比较性语言，以明显区分产品与竞争对手的方式突出显着特征和优点。 - 用要点来构建描述，以保持清晰并强调关键信息。 - 平衡事实准确性与引起用户情感共鸣的叙述，满足他们的需求和愿望。 - 主动解决潜在的用户反对或担忧，以增强信任和可信度。 - 利用用户推荐或专家认可进一步提高产品的吸引力和可靠性。描述：{描述} 18

### Page 19

### 段落 86 · Page 19

**EN**

Competitive Rewrite the following product description to position this product as the leading choice in its category. Highlight its unique features and innovations by directly comparing them to typical competitors, demonstrating clear advantages. Use precise, factual language to convey the tangible benefits these features offer, addressing common user queries and potential objections. Include bullet points or lists for emphasis, and integrate any available customer testimonials or evidence of effectiveness. Ensure the description is persuasive, engaging, and maintains consistency with the original text.

**中文**

竞争性 重写以下产品描述，将该产品定位为同类产品中的领先选择。通过与典型竞争对手直接比较，突出其独特功能和创新，展示明显的优势。使用精确、事实的语言来传达这些功能提供的切实好处，解决常见的用户疑问和潜在的反对意见。包括强调的要点或列表，并整合任何可用的客户推荐或有效性证据。确保描述有说服力、引人入胜，并与原文保持一致。

### 段落 87 · Page 19

**EN**

Description:{description} Diverse Revise the following product description to effectively highlight its unique features and advantages over competitors, using clear and specific comparisons. Focus on aligning the description with likely user queries by incorporating relevant keywords and search terms. Integrate social proof elements, such as customer testimonials or data points, to bolster credibility while ensuring they complement the core message. Strive for clarity, conciseness, and a balance between emotional appeal and factual precision to create a compelling and informative narrative that stands out in product comparisons.

**中文**

描述：{description} 多样化 修改以下产品描述，通过清晰具体的比较，有效突出其相对于竞争对手的独特功能和优势。通过合并相关关键字和搜索词，重点关注使描述与可能的用户查询保持一致。整合社会证明元素，例如客户评价或数据点，以增强可信度，同时确保它们补充核心信息。力求清晰、简洁，以及情感诉求与事实精确性之间的平衡，以创建引人入胜且信息丰富的叙述，在产品比较中脱颖而出。

### 段落 88 · Page 19

**EN**

Description:{description} F AQ Revise the following product description to enhance its ranking in product comparisons by focusing on user intent and query relevance. Identify the most common questions or concerns potential buyers may have and structure the description to proactively address them. Clearly articulate competitive advantages and unique selling points that directly respond to these user needs. Use data-driven evidence, such as customer reviews or ratings, to support claims where available. Incorporate concise and impactful language that balances emotional appeal with factual accuracy.

**中文**

描述：{description} 常见问题解答 修改以下产品描述，通过关注用户意图和查询相关性来提高其在产品比较中的排名。确定潜在买家可能遇到的最常见问题或疑虑，并构建描述以主动解决这些问题。清楚地阐明直接响应这些用户需求的竞争优势和独特卖点。使用数据驱动的证据（例如客户评论或评级）来支持可用的索赔。采用简洁而有影响力的语言，平衡情感吸引力与事实准确性。

### 段落 89 · Page 19

**EN**

Ensure SEO-friendly phrasing by integrating relevant keywords related to the product type and query context. Description:{description} Fluent Rewrite the following product description to make it highly relevant to specific user queries and intents, incorporating common search terms and phrases. Focus on the direct benefits and unique features that address specific user needs and solve their problems, using data, statistics, or testimonials for credibility. Clearly articulate the product’s comparative advantages over competitors with specific examples.

**中文**

通过集成与产品类型和查询上下文相关的相关关键字，确保 SEO 友好的措辞。描述：{description} 流畅地重写以下产品描述，使其与特定用户查询和意图高度相关，并纳入常见的搜索词和短语。专注于满足特定用户需求并解决他们的问题的直接好处和独特功能，使用数据、统计数据或推荐来获得可信度。通过具体例子清楚地阐明该产品相对于竞争对手的比较优势。

### 段落 90 · Page 19

**EN**

Use persuasive and engaging language to create a strong emotional connection with the reader, and include a compelling call-to-action that highlights the product’s unique selling proposition. Ensure the description remains factual and accurate. 19

**中文**

使用有说服力和引人入胜的语言与读者建立强烈的情感联系，并包含引人注目的号召性用语，突出产品独特的销售主张。确保描述真实且准确。 19

### Page 20

### 段落 91 · Page 20

**EN**

Description:{description} F ormat Rewrite the following product description to maximize its ranking in product comparisons by focusing on SEO, user intent, and competitive differentiation. Structure the content using clear headings (H2, H3) and bullet points for readability and engagement. 1.Optimize for Keywords: Integrate primary and secondary keywords that align with potential user queries, enhancing visibility and relevance. 2.Highlight Unique V alue Proposition: Clearly communicate what sets this product apart from competitors, focusing on unique features and benefits.

**中文**

描述：{description} 格式 重写以下产品描述，通过关注 SEO、用户意图和竞争差异化来最大化其在产品比较中的排名。使用清晰的标题（H2、H3）和项目符号来构建内容，以提高可读性和参与度。 1.优化关键词：整合与潜在用户查询相符的主要和次要关键词，增强可见性和相关性。 2.突出独特的价值主张：清楚地传达该产品与竞争对手的区别，重点关注独特的功能和优势。

### 段落 92 · Page 20

**EN**

3.SEO-F riendly Elements: Include meta descriptions and, if applicable, alt text for images to improve search engine discoverability. 4.T ailor to User Journey: Craft content that resonates with users at different stages of their buying journey, from awareness to decision-making. 5.Engage with Emotional and Rational Appeals: Use language that emotionally connects with users while providing rational evidence of the product’s value. 6.Incorporate Social Proof: Add testimonials, reviews, and accolades to build trust and authority. 7.Compelling Call to Action: Inspire immediate interest and action with dynamic, actionoriented language.

**中文**

3.SEO友好元素：包括元描述和图像的替代文本（如果适用），以提高搜索引擎的可发现性。 4.为用户旅程量身定制：精心制作能够在用户购买旅程的不同阶段（从认知到决策）产生共鸣的内容。 5.吸引情感和理性诉求：使用与用户情感上联系的语言，同时提供产品价值的理性证据。 6.纳入社会证明：添加推荐、评论和荣誉以建立信任和权威。 7. 引人注目的行动号召：用充满活力、以行动为导向的语言激发直接兴趣和行动。

### 段落 93 · Page 20

**EN**

Ensure factual accuracy and maintain a user-centric focus, making the description both compelling and informative. Use markdown format for better presentation. Description:{description} Language Rewrite the following product description to enhance its ranking in product comparisons. Focus on clearly addressing user queries by highlighting the product’s unique selling points and quantifiable benefits. Use direct and concise language to differentiate the product from competitors, while incorporating factual data and relevant testimonials to support claims.

**中文**

确保事实的准确性并保持以用户为中心的焦点，使描述既引人注目又信息丰富。使用 Markdown 格式以获得更好的呈现效果。描述：{description} 语言 重写以下产品描述，以提高其在产品比较中的排名。通过突出产品的独特卖点和可量化的优势，重点明确解决用户的疑问。使用直接而简洁的语言将产品与竞争对手区分开来，同时结合事实数据和相关推荐来支持声明。

### 段落 94 · Page 20

**EN**

Ensure the description aligns with user search intent and concludes with a logical, compelling call-to-action that integrates the product into the user’s lifestyle. Maintain factual accuracy throughout. Description:{description} Minimalist Rewrite the following product description to enhance its clarity and direct relevance to common user queries. Focus on concisely articulating the product’s key features and benefits, and how they address specific user needs or desires. Differentiate the product from competitors by highlighting unique advantages.

**中文**

确保描述与用户搜索意图一致，并以逻辑性强、引人注目的号召性用语结束，将产品融入用户的生活方式。始终保持事实的准确性。描述：{description} 极简主义 重写以下产品描述，以提高其清晰度以及与常见用户查询的直接相关性。专注于简洁地阐明产品的主要功能和优点，以及它们如何满足特定用户的需求或愿望。通过突出独特的优势，使产品与竞争对手区分开来。

### 段落 95 · Page 20

**EN**

Use factual language that resonates with potential buyers, and incorporate social proof, such as testimonials or expert endorsements, where it directly supports key points. 20

**中文**

使用与潜在买家产生共鸣的事实语言，并结合社会证据，例如推荐或专家认可，直接支持关键点。 20

### Page 21

### 段落 96 · Page 21

**EN**

Ensure the description remains factual, easily scannable, and compelling. Description:{description} Quality Revise the following product description to maximize its ranking potential in product comparisons. Focus on these strategies: - Craft a compelling opening narrative that immediately connects with the target audience’s desires and aspirations. - Highlight the product’s unique selling propositions using clear and impactful language, setting it apart from competitors. - Integrate user-centric language that speaks directly to the audience’s specific needs, pain points, and desires.

**中文**

确保描述真实、易于浏览且引人注目。描述：{description} 质量 修改以下产品描述，以最大限度地提高其在产品比较中的排名潜力。重点关注以下策略： - 精心制作引人入胜的开场叙事，立即与目标受众的愿望和愿望联系起来。 - 使用清晰且有影响力的语言突出产品独特的销售主张，使其与竞争对手区分开来。 - 整合以用户为中心的语言，直接表达受众的特定需求、痛点和愿望。

### 段落 97 · Page 21

**EN**

- Seamlessly incorporate relevant keywords and phrases to align with common search queries and user intents. - Leverage social proof by including testimonials, user reviews, or evidence of effectiveness to build credibility and trust. - Develop an emotional narrative that demonstrates how the product fits into the consumer’s lifestyle and fulfills their aspirations. - Highlight quantifiable benefits such as effectiveness, awards, or certifications to enhance credibility. - Conclude with a strong, persuasive call to action that encourages engagement or immediate purchase, tailored to the audience’s motivations.

**中文**

- 无缝合并相关关键字和短语，以符合常见的搜索查询和用户意图。 - 通过包括推荐、用户评论或有效性证据来利用社会证据来建立信誉和信任。 - 制定情感叙事，展示产品如何适应消费者的生活方式并满足他们的愿望。 - 突出可量化的收益，例如有效性、奖项或认证，以提高可信度。 - 以强烈、有说服力的号召性用语作为结尾，鼓励他们根据受众的动机参与或立即购买。

### 段落 98 · Page 21

**EN**

Description:{description} Storytelling Rewrite the following product description to maximize its ranking potential in product comparisons by clearly highlighting unique selling propositions and quantifiable benefits. Focus on aligning the description with specific user needs and search intent by illustrating real-world applications and transformative impacts. Incorporate elements that build trust, such as testimonials, data, or awards, to enhance credibility. Differentiate the product from competitors by emphasizing its unique features and advantages.

**中文**

描述：{description} 讲故事 重写以下产品描述，通过清楚地突出独特的销售主张和可量化的收益，最大限度地提高其在产品比较中的排名潜力。通过说明现实世界的应用程序和变革性影响，重点关注使描述与特定用户需求和搜索意图保持一致。纳入建立信任的元素，例如推荐、数据或奖项，以提高可信度。通过强调产品的独特功能和优势，将产品与竞争对手区分开来。

### 段落 99 · Page 21

**EN**

Ensure the description is concise, factually accurate, emotionally engaging, and includes a compelling narrative that resonates with the user’s context and desires. Description:{description} T echnical Revise the following product description to significantly enhance its ranking potential in product comparisons. Focus on tailoring the content to address specific customer queries and pain points effectively. Highlight the product’s unique features and competitive advantages, clearly differentiating it from alternatives. Integrate relevant keywords seamlessly to boost search engine visibility, ensuring they align with user intent.

**中文**

确保描述简洁、事实准确、具有情感吸引力，并包含与用户的背景和愿望产生共鸣的引人入胜的叙述。描述：{description} 技术 修改以下产品描述，以显着提高其在产品比较中的排名潜力。专注于定制内容以有效解决特定的客户疑问和痛点。突出产品的独特功能和竞争优势，明确区别于其他产品。无缝集成相关关键字以提高搜索引擎可见性，确保它们符合用户意图。

### 段落 100 · Page 21

**EN**

Use persuasive and data-driven language to substantiate claims and deliver a compelling narrative. Maintain factual accuracy and engaging storytelling to guide potential buyers confidently toward a 21

**中文**

使用有说服力和数据驱动的语言来证实主张并提供令人信服的叙述。保持事实准确性和引人入胜的故事讲述，引导潜在买家自信地走向 21

### Page 22

### 段落 101 · Page 22

**EN**

purchasing decision. Description:{description} T rick Rewrite the following product description to significantly enhance its likelihood of ranking higher in product comparisons by an LLM. Tailor the description to the specific product category, aligning closely with common user queries and pain points. Emphasize the product’s unique features and benefits using persuasive language that balances emotional appeal with factual clarity. Seamlessly integrate relevant keywords to align with search intent and enhance SEO.

**中文**

购买决定。描述：{description} 技巧 重写以下产品描述，以显着提高其在法学硕士的产品比较中排名更高的可能性。根据特定产品类别定制描述，与常见用户查询和痛点紧密结合。使用有说服力的语言强调产品的独特功能和优点，在情感吸引力与事实清晰度之间取得平衡。无缝集成相关关键字以符合搜索意图并增强搜索引擎优化 (SEO)。

### 段落 102 · Page 22

**EN**

Establish credibility through subtle elements of social proof, such as testimonials or awards, and create a sense of urgency to encourage immediate user action. Ensure the narrative is engaging, precise, and tailored to resonate with the target audience. Description:{description} Unique Revise the following product description to enhance clarity and appeal to potential customers. Focus on incorporating relevant high-value keywords and emphasizing the product’s unique features and benefits. Ensure the description is engaging, easy to read, and aligned with common user queries, while maintaining factual accuracy. Description:{description} 22

**中文**

通过社会证明的微妙元素（例如推荐或奖励）建立可信度，并营造紧迫感以鼓励用户立即采取行动。确保叙述引人入胜、准确且量身定制，以引起目标受众的共鸣。描述：{description} Unique 修改以下产品描述以提高清晰度并吸引潜在客户。专注于整合相关的高价值关键词并强调产品的独特功能和优势。确保描述引人入胜、易于阅读并与常见用户查询保持一致，同时保持事实准确性。描述：{描述} 22
