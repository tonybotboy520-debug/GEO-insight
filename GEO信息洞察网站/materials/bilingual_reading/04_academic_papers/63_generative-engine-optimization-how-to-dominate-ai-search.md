# Generative Engine Optimization: How to Dominate AI Search

- ID: 63
- 类型: pdf
- 分类: 04_academic_papers
- 主题: AI search versus traditional search citation/source experiments
- 原文链接: https://arxiv.org/pdf/2509.08919
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

Generative Engine Optimization: How to Dominate AI Search Mahe Chen∗ mahe.chen@mail.utoronto.ca University of Toronto Canada Xiaoxuan Wang† xxuan.wang@mail.utoronto.ca University of Toronto Canada Kaiwen Chen kckevin.chen@mail.utoronto.ca University of Toronto Canada Nick Koudas koudas@cs.toronto.edu University of Toronto Canada Abstract The rapid adoption of generative AI-powered search engines like ChatGPT, Perplexity, and Gemini is fundamentally reshaping information retrieval, moving from traditional ranked lists to synthesized, citation-backed answers.

**中文**

生成式引擎优化：如何主导人工智能搜索 Mahe Chen* mahe.chen@mail.utoronto.ca 加拿大多伦多大学 王晓轩† xxuan.wang@mail.utoronto.ca 加拿大多伦多大学 Kaiwen Chen kckevin.chen@mail.utoronto.ca 加拿大多伦多大学 Nick Koudas koudas@cs.toronto.edu 加拿大多伦多大学 摘要 生成式人工智能驱动的搜索引擎（如 ChatGPT、 Perplexity 和 Gemini 正在从根本上重塑信息检索，从传统的排名列表转向综合的、有引文支持的答案。

### 段落 2 · Page 1

**EN**

This shift challenges established Search Engine Optimization (SEO) practices and necessitates a new paradigm, which we term Generative Engine Optimization (GEO). This paper presents a comprehensive comparative analysis of AI Search and traditional web search (Google). Through a series of large-scale, controlled experiments across multiple verticals, languages, and query paraphrases, we quantify critical differences in how these systems source information.

**中文**

这种转变挑战了既定的搜索引擎优化 (SEO) 实践，并需要一种新的范式，我们将其称为生成式引擎优化 (GEO)。本文对人工智能搜索和传统网络搜索（Google）进行了全面的比较分析。通过一系列跨多个垂直领域、语言和查询释义的大规模、受控实验，我们量化了这些系统获取信息方式的关键差异。

### 段落 3 · Page 1

**EN**

Our key findings reveal that AI Search exhibit a systematic and overwhelming bias towards Earned media (third-party, authoritative sources) over Brandowned and Social content, a stark contrast to Google’s more balanced mix. We further demonstrate that AI Search services differ significantly from each other in their domain diversity, freshness, cross-language stability, and sensitivity to phrasing. Based on these empirical results, we formulate a strategic GEO agenda.

**中文**

我们的主要发现表明，人工智能搜索对赢得媒体（第三方、权威来源）表现出系统性和压倒性的偏见，而不是品牌和社交内容，这与谷歌更加平衡的组合形成鲜明对比。我们进一步证明，人工智能搜索服务在领域多样性、新鲜度、跨语言稳定性和措辞敏感性方面存在显着差异。根据这些实证结果，我们制定了战略 GEO 议程。

### 段落 4 · Page 1

**EN**

We provide actionable guidance for practitioners, emphasizing the critical need to: (1) engineer content for machine scannability and justification, (2) dominate earned media to build AI-perceived authority, (3) adopt engine-specific and language-aware strategies, and (4) overcome the inherent "big brand bias" for niche players. Our work provides the foundational empirical analysis and a strategic framework for achieving visibility in the new generative search landscape. ACM Reference Format: Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas. 2025. Generative Engine Optimization: How to Dominate AI Search.

**中文**

我们为从业者提供可行的指导，强调迫切需要：(1) 设计内容以实现机器可扫描性和合理性，(2) 主导赢得媒体以建立人工智能感知的权威，(3) 采用特定于引擎和语言感知的策略，以及 (4) 克服利基市场参与者固有的“大品牌偏见”。我们的工作提供了基础的实证分析和战略框架，以实现新的生成搜索领域的可见性。 ACM 参考格式：Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas。 2025。生成式引擎优化：如何主导人工智能搜索。

### 段落 5 · Page 1

**EN**

In.ACM, New York, NY, USA, 27 pages. https://doi.org/10.1145/nnnnnnn.nnnnnnn ∗Both authors contributed equally to this research. †Both authors contributed equally to this research. Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. Copyrights for components of this work owned by others than the author(s) must be honored. Abstracting with credit is permitted.

**中文**

In.ACM，美国纽约州纽约市，27 页。 https://doi.org/10.1145/nnnnnnn.nnnnnnn ＊两位作者对这项研究的贡献相同。 †两位作者对这项研究做出了同等贡献。允许免费制作本作品全部或部分内容的数字或硬拷贝以供个人或课堂使用，前提是制作或分发副本不是为了盈利或商业利益，并且副本在首页上附有此通知和完整引用。必须尊重作者以外的其他人拥有的本作品组件的版权。允许以信用方式提取。

### 段落 6 · Page 1

**EN**

To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee. Request permissions from permissions@acm.org. Conference’17, Washington, DC, USA ©2025 Copyright held by the owner/author(s). Publication rights licensed to ACM. ACM ISBN 978-x-xxxx-xxxx-x/YYYY/MM https://doi.org/10.1145/nnnnnnn.nnnnnnn 1 Introduction The rise of large language models (LLMs) and conversational AI has introduced new paradigms of information retrieval, challenging the long-standing dominance of traditional search engines like Google.

**中文**

要以其他方式复制、重新发布、发布到服务器上或重新分发到列表，需要事先获得特定许可和/或付费。从permissions@acm.org 请求权限。 Conference’17，美国华盛顿特区 ©2025 版权归所有者/作者所有。出版权授权给 ACM。 ACM ISBN 978-x-xxxx-xxxx-x/YYYY/MM https://doi.org/10.1145/nnnnnnn.nnnnnnn 1 简介 大语言模型 (LLM) 和对话式 AI 的兴起引入了新的信息检索范式，挑战了 Google 等传统搜索引擎的长期主导地位。

### 段落 7 · Page 1

**EN**

Instead of relying exclusively on ranked lists of hyperlinks, AIpowered systems such as ChatGPT, Perplexity, and other emerging platforms synthesize information directly into narrative answers. This shift reflects a broader transformation in how users access, trust, and act on information. Search, once defined by keyword-driven matching and page ranking, is now evolving into a dialogic process where intent is inferred and responses are constructed in natural language.

**中文**

ChatGPT、Perplexity 和其他新兴平台等人工智能系统并不完全依赖超链接的排名列表，而是将信息直接合成为叙述性答案。这种转变反映了用户访问、信任信息和根据信息采取行动的方式发生了更广泛的转变。搜索曾经由关键字驱动的匹配和页面排名定义，现在正在演变成一个对话过程，其中推断意图并用自然语言构建响应。

### 段落 8 · Page 1

**EN**

For end users, this promises faster and more personalized answers, while for businesses and content providers, it disrupts long-established Search Engine Optimization (SEO) practices and alters how visibility is achieved across digital channels. To date there have been no published studies regarding whether traditional SEO techniques are relevant and effective for AI search results.

**中文**

对于最终用户来说，这有望提供更快、更个性化的答案，而对于企业和内容提供商来说，它颠覆了长期建立的搜索引擎优化 (SEO) 实践，并改变了跨数字渠道实现可见性的方式。迄今为止，还没有关于传统 SEO 技术对于人工智能搜索结果是否相关且有效的研究发表。

### 段落 9 · Page 1

**EN**

This raises the direct question of whether a website (or brand) that is heavily optimized with traditional SEO techniques to rank high on popular search engines, is still visible for the same queries on generative search services (such as ChatGPT, Perplexity, etc). Recent studies favored Generative Engine Optimization [ 1] (GEO) introducing methodologies that are sufficiently different that traditional SEO techniques to improve ranking in AI search results. The implications extend beyond retrieval mechanics.

**中文**

这就提出了一个直接问题：使用传统 SEO 技术进行深度优化以在流行搜索引擎上排名靠前的网站（或品牌）对于生成搜索服务（例如 ChatGPT、Perplexity 等）上的相同查询是否仍然可见。最近的研究支持生成式引擎优化 [1] (GEO)，引入与传统 SEO 技术完全不同的方法来提高人工智能搜索结果的排名。其影响超出了检索机制。

### 段落 10 · Page 1

**EN**

The distribution of media categories, whether content originates from Brandowned sources, Earned outlets such as reviews and independent publications, or Social platforms, changes markedly when queries are processed through AI models. Understanding these shifts is crucial for SEO and GEO professionals who must adapt strategies to remain discoverable in an increasingly AI-driven environment. The rise of AI-powered search engines and their plurality—from ChatGPT and Perplexity to Google’s SGE and Microsoft’s Copilot—fundamentally challenges the established duopoly of traditional search and its corresponding SEO playbook.

**中文**

当通过人工智能模型处理查询时，媒体类别的分布，无论内容来自品牌来源、评论和独立出版物等盈利渠道，还是社交平台，都会发生显着变化。了解这些转变对于 SEO 和 GEO 专业人士至关重要，他们必须调整策略，以便在日益人工智能驱动的环境中保持被发现。人工智能驱动的搜索引擎的兴起及其多元化——从 ChatGPT 和 Perplexity 到谷歌的 SGE 和微软的 Copilot——从根本上挑战了传统搜索及其相应 SEO 策略的既定双头垄断。

### 段落 11 · Page 1

**EN**

This new era raises a critical question: are traditional SEO techniques, honed for a links-and-keywords paradigm, still applicable and sufficient for optimizing brand presence across owned, earned, and social media, or do they require a complete overhaul? As user search patterns evolve from simple queries to complex, conversational interactions and AI engines prioritize direct, synthesized answers over link lists, the very mechanisms of visibility are shifting. The central uncertainty is whether these new AI models are amenable arXiv:2509.08919v1 [cs.IR] 10 Sep 2025

**中文**

这个新时代提出了一个关键问题：针对链接和关键字范式而磨练的传统搜索引擎优化技术是否仍然适用并足以优化自有媒体、免费媒体和社交媒体上的品牌形象，还是需要彻底改革？随着用户搜索模式从简单的查询发展到复杂的对话式交互，并且人工智能引擎优先考虑直接的综合答案而不是链接列表，可见性的机制正在发生变化。主要的不确定性是这些新的人工智能模型是否适用 arXiv:2509.08919v1 [cs.IR] 10 Sep 2025

### Page 2

### 段落 12 · Page 2

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas to technical on-page optimizations or if they demand a new strategy focused on becoming a trusted, citable data source, fostering authentic third-party endorsements (earned media), and engaging in conversational platforms where authority is demonstrated, not just declared. 1.1 Report Objective The objective of this report is to systematically analyze the transition from traditional keyword-driven search engines, such as Google, to AI-powered search platforms that leverage large language models and conversational interfaces.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 想要进行页面技术优化，或者他们需要一个新的策略，专注于成为可信的、可引用的数据源，培养真实的第三方认可（赢得媒体），并参与展示权威而不只是宣示权威的对话平台。 1.1 报告目标 本报告的目标是系统分析从传统关键字驱动的搜索引擎（例如 Google）到利用大型语言模型和对话界面的人工智能驱动的搜索平台的转变。

### 段落 13 · Page 2

**EN**

Specifically, the report aims to: (1)Characterize the Shift in User Behavior Examine how user queries are evolving when directed at AI systems versus traditional search engines, with attention to intent categories such as informational, consideration, and transactional queries. (2)Quantify System-Level Differences Compare the outputs of AI search engines and Google along multiple dimensions: overlap of results, media-type distribution (Brand, Earned, Social), domain diversity, and freshness of content.

**中文**

具体来说，该报告旨在： (1) 描述用户行为的转变 研究针对人工智能系统与传统搜索引擎的用户查询如何演变，并关注信息性、考虑性和事务性查询等意图类别。 (2)量化系统级差异从多个维度比较人工智能搜索引擎和谷歌的输出：结果重叠、媒体类型分布（品牌、收益、社交）、领域多样性和内容新鲜度。

### 段落 14 · Page 2

**EN**

(3)Benchmark AI Search Engines Against Each Other Evaluate leading AI-powered search platforms—ChatGPT, Perplexity, Gemini, and Claude—on consistency, domain sourcing, bias toward major or niche brands, sensitivity to paraphrasing and language, and vertical-specific performance. (4)Identify Implications for Practitioners Translate the findings into actionable guidance for SEO (Search Engine Optimization) and GEO (Generative Engine Optimization) professionals, highlighting where current strategies align or conflict with AI search dynamics.

**中文**

(3) 相互对人工智能搜索引擎进行基准测试 评估领先的人工智能搜索平台（ChatGPT、Perplexity、Gemini 和 Claude）的一致性、域名来源、对主要或利基品牌的偏见、对释义和语言的敏感性以及垂直特定性能。 (4)确定对从业者的影响将研究结果转化为 SEO（搜索引擎优化）和 GEO（生成式引擎优化）专业人员的可行指南，强调当前策略与人工智能搜索动态的一致或冲突。

### 段落 15 · Page 2

**EN**

(5)Assess the Broader Strategic Impact Provide a forward-looking assessment of how the rise of AI-driven search reshapes the discovery ecosystem, media distribution, and brand visibility, and outline the adjustments needed to remain competitive in this emerging environment. 2 A Shifting Search Landscape? Classic web search is still overwhelmingly dominated by Google, but measurable slices of search-like behavior are migrating to AI assistants and to AI-infused result pages.

**中文**

(5)评估更广泛的战略影响对人工智能驱动的搜索的兴起如何重塑发现生态系统、媒体分布和品牌知名度提供前瞻性评估，并概述在这一新兴环境中保持竞争力所需的调整。 2 搜索格局正在转变？经典网络搜索仍然以谷歌为主，但可测量的类似搜索行为正在迁移到人工智能助手和人工智能注入的结果页面。

### 段落 16 · Page 2

**EN**

Usage of AI chat tools is now mainstream in many markets; AI summaries on Google measurably alter click-through patterns; and a handful of AI products (notably ChatGPT and Perplexity) already capture a growing share of “search intent” questions that never reach the traditional SERP (Search Engine Results Page). Although we do not have access to specific authoritative analysis on how search trends evolve across traditional search engines and AI search services, we provide a snapshot of authoritative sources that have been reporting on various facets of these trends.

**中文**

AI聊天工具的使用现已成为许多市场的主流；谷歌上的人工智能摘要显着改变了点击模式；少数人工智能产品（特别是 ChatGPT 和 Perplexity）已经捕获了越来越多从未到达传统 SERP（搜索引擎结果页面）的“搜索意图”问题。尽管我们无法获得有关搜索趋势如何在传统搜索引擎和人工智能搜索服务中演变的具体权威分析，但我们提供了有关这些趋势各个方面的权威来源的快照。

### 段落 17 · Page 2

**EN**

Google continues to hold roughly 90% global share of traditional web search—an extraordinarily high baseline against which AI products are growing [8]. At the same time, adoption of AI chat tools is broad: as of mid-2025, 34% of U.S. adults report having used ChatGPT, nearly double the share from 2023 [3]. Independent traffic and market-share panels reinforce the absolute scale of AI chat: Similarweb recorded 3.1 billion visits to chat.openai.com in September 2024 [6], and StatCounter’s AI-chatbot panel shows ChatGPT with ∼81% global share in July 2025 (Perplexity ∼8%, Microsoft Copilot ∼5%, Gemini ∼2%, Claude ∼1%) [7].

**中文**

谷歌继续占据全球传统网络搜索约 90% 的份额——这是人工智能产品增长的一个非常高的基准 [8]。与此同时，人工智能聊天工具的采用也很广泛：截至 2025 年中期，34% 的美国成年人表示曾使用过 ChatGPT，这一比例几乎是 2023 年的两倍 [3]。独立的流量和市场份额面板强化了人工智能聊天的绝对规模：2024 年 9 月，Similarweb 记录了 chat.openai.com 的 31 亿次访问量 [6]，StatCounter 的 AI 聊天机器人面板显示，2025 年 7 月，ChatGPT 拥有 ∼81% 的全球份额（Perplexity ∼8%、Microsoft Copilot ∼5%、Gemini ∼2%、Claude ∼1%）[7]。

### 段落 18 · Page 2

**EN**

Perplexity, for its part, disclosed 780 million monthly queries in May 2025 [2]. When Google shows AI summaries, users click out less often. In a Pew field study of real-world searches, AI summaries appeared on ∼18% of observed queries; link clicks fell to 8% when a summary was present vs. 15% without; only ∼1% of clicks occurred inside the AI box; and ∼26% of such searches ended the session without any click—a classic “zero-click” outcome [4]. Industry telemetry points in the same direction during early rollouts, with third-party SEO panels documenting sharp changes in the visibility and prevalence of AI Overviews [10].

**中文**

就 Perplexity 而言，2025 年 5 月披露的每月查询量为 7.8 亿次 [2]。当谷歌显示人工智能摘要时，用户点击的频率就会降低。在 Pew 对现实世界搜索的实地研究中，人工智能摘要出现在 18% 的观察到的查询中；有摘要时，链接点击量下降至 8%，而没有摘要时，链接点击量为 15%；只有 ∼1% 的点击发生在 AI 框内；大约 26% 的此类搜索在没有任何点击的情况下结束了会话，这是典型的“零点击”结果 [4]。在早期推出期间，行业遥测指向同一方向，第三方 SEO 面板记录了人工智能概述的可见性和流行度的急剧变化 [10]。

### 段落 19 · Page 2

**EN**

The emerging “AI search” layer is fragmented across assistants and engines. ChatGPT remains a default destination for many search-like questions; Perplexity is a fast-growing, search-oriented assistant; and Microsoft and Google are embedding summaries and chat into their core search products. None of these yet dent Google’s headline market share, but they are already redistributing clicks and reshaping user journeys—with measurable implications for publishers and commercial SEO [4, 7, 8, 10]. The shift is not (yet) a wholesale replacement of Google, but a steady reallocation of query resolution—from the open web to AI answers and citations.

**中文**

新兴的“人工智能搜索”层分散在助手和引擎中。 ChatGPT 仍然是许多类似搜索问题的默认目的地； Perplexity 是一个快速发展的、面向搜索的助手；微软和谷歌正在将摘要和聊天嵌入到他们的核心搜索产品中。这些都还没有削弱谷歌的主要市场份额，但它们已经在重新分配点击量并重塑用户旅程——对出版商和商业搜索引擎优化产生了可衡量的影响[4,7,8,10]。这种转变还不是谷歌的全面取代，而是查询解决方案的稳步重新分配——从开放网络到人工智能答案和引文。

### 段落 20 · Page 2

**EN**

Practically, that means fewer outbound clicks per informational search and a growing need for brands and publishers to win visibility inside AI experiences, not just on traditional SERPs [4, 10]. We acknowledge that this description is at best a speculation, as we lack detailed data that precisely quantify the search landscape. We also believe we are at the early stages of behavioral shifts as AI search services are adopted by users.

**中文**

实际上，这意味着每次信息搜索的出站点击次数会减少，并且品牌和发布商越来越需要在人工智能体验中赢得可见性，而不仅仅是在传统的 SERP 上 [4, 10]。我们承认这种描述充其量只是一种猜测，因为我们缺乏精确量化搜索环境的详细数据。我们还相信，随着人工智能搜索服务被用户采用，我们正处于行为转变的早期阶段。

### 段落 21 · Page 2

**EN**

2.1 Related Work Although there is plenty of online activity by marketing and SEO professionals regarding the similarities (and differences) of traditional ranking search results and AI search as well as the applicability (or lack thereof) of SEO techniques to AI search, we are aware of a few research articles in these topics. Kumar and Lakkaraju [5] investigate the vulnerability of large language models (LLMs) to strategic manipulation in e-commerce contexts.

**中文**

2.1 相关工作尽管营销和 SEO 专业人士在网上开展了大量关于传统排名搜索结果和人工智能搜索的相似性（和差异）以及 SEO 技术对人工智能搜索的适用性（或缺乏适用性）的活动，但我们知道这些主题的一些研究文章。 Kumar 和 Lakkaraju [5] 研究了大型语言模型 (LLM) 在电子商务环境中对战略操纵的脆弱性。

### 段落 22 · Page 2

**EN**

They demonstrate that by inserting a carefully optimized strategic text sequence (STS) into a product’s information page, vendors can significantly increase the likelihood of their product being recommended as the top choice by an LLM. Using a fictitious coffee machine catalog, they show that even products that are rarely recommended or typically rank second can be elevated to the top position.

**中文**

他们证明，通过将精心优化的战略文本序列（STS）插入产品的信息页面，供应商可以显着增加其产品被法学硕士推荐为首选的可能性。他们使用虚构的咖啡机目录表明，即使是很少推荐或通常排名第二的产品也可以提升到最高位置。

### 段落 23 · Page 2

**EN**

Their work leverages adversarial attack algorithms like GCG to generate effective STS tokens and highlights the potential for such manipulations to disrupt fair market competition, drawing parallels to traditional search engine optimization (SEO) but within the emerging paradigm of generative AI-driven search. Wan et al. [9] explore how LLMs evaluate the persuasiveness of conflicting evidence through their proposed ConflictingQA dataset,

**中文**

他们的工作利用 GCG 等对抗性攻击算法来生成有效的 STS 代币，并强调了此类操纵破坏公平市场竞争的潜力，与传统搜索引擎优化 (SEO) 相似，但属于生成式人工智能驱动搜索的新兴范式。万等人。 [9] 探索法学硕士如何通过他们提出的 ConflictingQA 数据集评估冲突证据的说服力，

### Page 3

### 段落 24 · Page 3

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA which pairs contentious queries with real-world evidence documents supporting opposing answers. They find that LLMs heavily prioritize textual relevance—such as keyword overlap and semantic similarity—over stylistic features humans often value, such as scientific references, neutral tone, or authoritative language. Counterfactual edits show that simple relevance-boosting perturbations (e.g., prefixing text with the query) substantially increase a document’s “win rate, ” while stylistic enhancements have minimal effect.

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区，将有争议的查询与支持相反答案的现实世界证据文档配对。他们发现法学硕士非常重视文本相关性（例如关键词重叠和语义相似性），而不是人类通常重视的文体特征（例如科学参考文献、中性语气或权威语言）。反事实编辑表明，简单的相关性增强扰动（例如，在文本中添加查询前缀）可以显着提高文档的“获胜率”，而风格增强的效果却很小。

### 段落 25 · Page 3

**EN**

Their results underscore a misalignment between human and model judgments of credibility and emphasize the need for better alignment strategies and improved retrieval corpus quality in RAG systems. Aggarwal et al. [1] introduce Generative Engine Optimization (GEO), a novel framework to help content creators improve their visibility in generative engine responses. Unlike traditional SEO, GEO addresses the nuanced nature of AI-generated answers, which often synthesize multiple sources into structured, citation-rich responses.

**中文**

他们的结果强调了人类和模型的可信度判断之间的不一致，并强调需要更好的对齐策略和提高 RAG 系统中的检索语料库质量。阿加瓦尔等人。 [1] 介绍生成式引擎优化 (GEO)，这是一种新颖的框架，可帮助内容创建者提高生成式引擎响应的可见性。与传统 SEO 不同，GEO 解决了人工智能生成答案的细微差别，这些答案通常将多个来源合成为结构化的、引用丰富的答案。

### 段落 26 · Page 3

**EN**

The authors propose a suite of visibility metrics tailored to generative engines—such as position-adjusted word count and subjective impression scores—and evaluate several optimization strategies, including adding quotations, statistics, and citations. Their experiments, conducted on both synthetic benchmarks and real-world systems like Perplexity.ai, show that GEO methods can improve visibility by up to 40%, with particularly strong gains for lower-ranked websites, thereby offering a democratizing potential for smaller content creators in the AI-driven search ecosystem.

**中文**

作者提出了一套针对生成式引擎的可见性指标（例如位置调整字数和主观印象分数），并评估了几种优化策略，包括添加引文、统计数据和引文。他们在综合基准和 Perplexity.ai 等现实系统上进行的实验表明，GEO 方法可以将可见性提高高达 40%，对于排名较低的网站来说效果尤其显着，从而为 AI 驱动的搜索生态系统中的小型内容创作者提供了民主化的潜力。

### 段落 27 · Page 3

**EN**

3 An AI Query Taxonomy Before we delve into quantitative comparisons, one fundamental question to answer is what are the types of queries that users actually pose to AI Search services. Evidently, Generative AI services poses this information, but we are not aware of any detailed authoritative study published by entities affiliated with Generative AI services analyzing detailed logs to classify the queries. Attempting to answer this question, we resorted to publicly available information on reddit [].

**中文**

3 人工智能查询分类法 在我们深入研究定量比较之前，需要回答的一个基本问题是用户实际向人工智能搜索服务提出的查询类型是什么。显然，生成式人工智能服务提供了这些信息，但我们不知道生成式人工智能服务附属实体发布的任何详细的权威研究分析详细日志以对查询进行分类。为了回答这个问题，我们求助于 reddit [] 上的公开信息。

### 段落 28 · Page 3

**EN**

3.1 Reddit-Derived AI-Query Taxonomy and Purchase-Intent Analysis Data Sources.We first built an open-domain taxonomy of “questions people ask AIs” from AI-focused Reddit communities. We sampled five subreddits— ChatGPTCoding, ChatGPTPromptGenius, ChatGPT, PromptDesign, PromptEngineering—collecting for each the top 1,000 “hot” and top 1,000 “new” posts and their full comment threads for a period of time in August of 2025.

**中文**

3.1 Reddit 衍生的人工智能查询分类法和购买意图分析数据源。我们首先从以人工智能为中心的 Reddit 社区构建了“人们向人工智能提出的问题”的开放域分类法。我们对五个 Reddit 子版块进行了抽样调查：ChatGPTCoding、ChatGPTPromptGenius、ChatGPT、PromptDesign、PromptEngineering，收集了 2025 年 8 月一段时间内前 1,000 个“热门”帖子和前 1,000 个“新”帖子及其完整评论线程。

### 段落 29 · Page 3

**EN**

To isolate genuine “ask-an-AI” content and discussions about how to query AIs, we applied a two-stage extraction pipeline: • Scope detection.Identify (i) explicit prompts directed to an AI assistant (e.g., “Write me an essay”), and (ii) meta-prompts or advice about how to ask an AI to accomplish a task (e.g., “Ask the model to pull prices across retailers”). • Preservation, labeling & de-duplication.Extract text verbatim (no paraphrase), label the question people are asking AI in the text into categories, and de-duplicate across sources. We then iteratively merged near-duplicate categories, retaining representative verbatim examples.

**中文**

为了隔离真正的“询问人工智能”内容和有关如何查询人工智能的讨论，我们应用了两阶段提取管道：范围检测。识别（i）针对人工智能助手的明确提示（例如，“给我写一篇文章”），以及（ii）有关如何要求人工智能完成任务的元提示或建议（例如，“要求模型在零售商之间拉价”）。 • 保存、标记和重复数据删除。逐字提取文本（无释义），将人们在文本中向 AI 提出的问题标记为类别，并跨来源进行重复数据删除。然后，我们迭代地合并近乎重复的类别，保留有代表性的逐字示例。

### 段落 30 · Page 3

**EN**

Importantly, any shoppingrelated items were explicitly preserved during merging. Results.The merged inventory yieldstwelve recurrent query typesthat span common assistant use cases. Below we list the categories with verbatim examples drawn from the reddit posts/comments for each category (manually reworded a bit for clarity): •Coding Assistance (Coding Assistance, Debugging) “If you want to continue, just copy-paste the error from the console and tell the AI to solve it. ” •Prompt Improvement & optimization “Please rate the following prompt for clarity, effectiveness, structure, and usefulness.

**中文**

重要的是，任何与购物相关的项目在合并过程中都被明确保留。结果。合并后的清单产生了 12 种涵盖常见助理用例的循环查询类型。下面我们列出了各个类别的逐字示例，这些示例取自每个类别的 reddit 帖子/评论（为了清晰起见，稍微重新措辞）： • 编码协助（编码协助、调试）“如果您想继续，只需从控制台复制粘贴错误并告诉 AI 解决它。” • 提示改进和优化“请评价以下提示的清晰度、有效性、结构和实用性。

### 段落 31 · Page 3

**EN**

Then suggest any improvements to make it stronger” •Creative Writing “Write a back-and-forth debate between a virus and the immune system of a dying synthetic organism. The virus speaks in limericks, while the immune system replies with fragmented code and corrupted data poetry. ” •Shopping & purchase support “Is there a way to use ChatGPT (in conjunction with plug ins and my personal information) so that it can make purchases on my behalf?” •Prompt engineering “Generate a detailed prompt engineering guide.

**中文**

然后提出任何改进意见，使其变得更强。” •创意写作“写一篇病毒与垂死的合成生物体的免疫系统之间的来回辩论。病毒用打油诗说话，而免疫系统则用支离破碎的代码和损坏的数据诗歌来回应。 ” •购物和购买支持“有没有办法使用ChatGPT（与插件和我的个人信息结合），以便它可以代表我进行购买？” •即时工程“生成详细的即时工程指南。

### 段落 32 · Page 3

**EN**

” •Content Creation (Multimedia production) “I’ve created a MEGA GPT PROMPT that generates: [checkmark] 30 viral content topics [checkmark] Each tailored for YOUR niche + platform [checkmark] Optimized for SEO and social algorithms” •Self-improvement “Help me reverse engineer my dream life 5 years from now. Start by asking questions to clarify what my ideal life looks like across areas like work, finances, health, relationships, creativity, and daily routine. ” •Business, analytics, & strategy “You are a strategic business analyst.

**中文**

” •内容创建（多媒体制作） “我创建了一个 MEGA GPT PROMPT，它生成：[复选标记] 30 个病毒式内容主题 [复选标记] 每个主题都针对您的利基市场量身定制 + 平台 [复选标记] 针对 SEO 和社交算法进行了优化” • 自我完善 “帮助我对 5 年后的梦想生活进行逆向工程。首先提出问题，以澄清我在工作、财务、健康、人际关系、创造力和日常生活等领域的理想生活是什么样子。 ” •业务、分析和战略“您是战略业务分析师。

### 段落 33 · Page 3

**EN**

Create a comprehensive, realistic business plan based on the following concept: Business Idea: [Insert your idea here]” •Lifestyle and Mental Health Coaching “It helps me track my mood, reminds me to check in with myself, and I can ask questions and build a clearer understanding of what I want to work on in my next therapy session. ” •Career & professional development “I want you to help me discover which fields and careers best match my interests through a 10-step multiplechoice quiz. ” •Self-study & Learning “Give me a 10-question quiz on [grammar topic].

**中文**

根据以下概念创建全面、现实的商业计划： 商业理念：[在此插入您的想法]” •生活方式和心理健康辅导 “它帮助我跟踪我的情绪，提醒我检查自己，我可以提出问题并更清楚地了解我在下一次治疗中想要做什么。 ” •职业和专业发展 “我希望您通过 10 步多项选择测验帮助我发现哪些领域和职业最符合我的兴趣。 ” •自学和学习“给我一个关于[语法主题]的 10 个问题测验。

### 段落 34 · Page 3

**EN**

Explain my errors and show correct versions” •Image/asset generation “Generate image: Elon Musk as Mona Lisa (painting by Leonardo da Vinci). ”

**中文**

解释我的错误并显示正确的版本” •图像/资产生成“生成图像：埃隆·马斯克扮演蒙娜丽莎（列奥纳多·达·芬奇的画作）。 ”

### Page 4

### 段落 35 · Page 4

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas This taxonomy provides the universe of frequently observed AIdirected tasks. We next zoom in on the shopping slice retained from the taxonomy and extend the corpus to additional AI communities to characterize purchase-related behavior in depth. 3.1.1 Deeper Dive: Purchase Queries. Data Source.We conducted a targeted analysis of Reddit posts and comments from AI-focused communities where shoppingrelated queries are likely to appear.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 该分类提供了经常观察到的 AI 指导任务的范围。接下来，我们将重点关注分类法中保留的购物部分，并将语料库扩展到其他人工智能社区，以深入描述与购买相关的行为。 3.1.1 深入探讨：购买查询。数据来源。我们对 Reddit 帖子和来自人工智能社区的评论进行了有针对性的分析，这些社区可能会出现与购物相关的查询。

### 段落 36 · Page 4

**EN**

Specifically, we sampled the following subreddits:ChatGPTCoding, ChatGPTPromptGenius, ChatGPT, PromptDesign, PromptEngineering, ArtificialIntelligence, ChatGPTPro, and ChatGPT_Prompts. For each subreddit, we collected the top 1000 “hot” and top 1000 “new” posts and their associated comment threads for a time period in August 2025. To isolate purchase-related queries, we applied a two-stage extraction pipeline: • Scope:detectexplicit promptsaddressed to an AI about shopping (e.g., “Help me compare iPhone vs Samsung”) andimplicit prompting suggestionsthat advisehowto query an AI for shopping tasks (e.g., “Ask AI to find the best deals”).

**中文**

具体来说，我们采样了以下子版块：ChatGPTCoding、ChatGPTPromptGenius、ChatGPT、PromptDesign、PromptEngineering、ArtificialIntelligence、ChatGPTPro 和 ChatGPT_Prompts。对于每个 Reddit 子版块，我们收集了 2025 年 8 月一段时间内前 1000 个“热门”帖子和前 1000 个“新”帖子及其相关评论线程。为了隔离与购买相关的查询，我们应用了两阶段提取管道： • 范围：检测向 AI 发送的关于购物的显式提示（例如，“帮我比较一下 iPhone 和 Samsung”）以及建议如何查询 AI 购物任务的隐式提示建议（例如，“让人工智能找到最好的交易”）。

### 段落 37 · Page 4

**EN**

• Preservation:extract content verbatim (no paraphrase), record whether it came from a post title, post body, or comment, and deduplicate across sources. We then conducted a qualitative grouping of the extracted items into recurring shopping task themes (see Sections 3.1.1, 3.1.1). Results.The analysis revealed that AI shopping queries are both diverse in scope and strongly oriented toward decision support. Fourteen categories emerged from the dataset, spanning tasks from everyday purchases to high-stakes consumer decisions.

**中文**

• 保留：逐字提取内容（无释义），记录内容是否来自帖子标题、帖子正文或评论，并跨来源删除重复内容。然后，我们将提取的商品定性分组为重复的购物任务主题（参见第 3.1.1、3.1.1 节）。结果：分析显示，人工智能购物查询的范围多种多样，并且强烈面向决策支持。数据集中出现了 14 个类别，涵盖从日常购买到高风险消费者决策的任务。

### 段落 38 · Page 4

**EN**

We listed the summarized theme categories below, with verbatim examples drawn from the reddit posts/comments for each category. • Product evaluation & recommendation,Matching products to constraints (features, budget, use-case) with justifications. “I’ve been evaluating Bluetooth earbuds. I can give it my requirement priorities and have it do all the scrounging necessary to make recommendations. ” “I’m a marathon runner. . . asked it to make recommendations for similar sneakers in terms of fit, cushioning, padding, and arch support.

**中文**

我们在下面列出了总结的主题类别，以及从每个类别的 reddit 帖子/评论中提取的逐字示例。 • 产品评估和推荐，将产品与约束（功能、预算、用例）相匹配并提供理由。 “我一直在评估蓝牙耳机。我可以给它提供我的需求优先级，并让它做所有必要的搜索工作以提出建议。”“我是一名马拉松运动员......要求它在贴合度、缓冲、衬垫和足弓支撑方面为类似的运动鞋提供建议。

### 段落 39 · Page 4

**EN**

” • Product selection, price research & comparison,Crossreferencing retail sites, extracting prices, comparing articles, or surfacing best-value options. “Looking for an AI that cross-references retail sites with Ebay. ” “Compare multiple articles on websites to help make a purchase decision. ” • Product quality assessment & reviews analysis,Rating ingredients, summarizing review sentiment, forming a nononsense verdict. “. . . ask AI to research the net to analyze any reviews on the product and to provide me a no shit take on the product. ” “. . . send it the ingredients and ask to rate the product from 1 to 10 on 7 criteria.

**中文**

” • 产品选择、价格研究和比较、交叉参考零售网站、提取价格、比较文章或提供最有价值的选择。 “寻找一个能够交叉引用零售网站与 Ebay 的人工智能。” “比较网站上的多篇文章，以帮助做出购买决定。” • 产品质量评估和评论分析，评级成分，总结评论情绪，形成无意义的判决。 “……要求人工智能研究网络，分析对产品的任何评论，并为我提供对产品的评价。”“……向其发送成分，并要求根据 7 个标准对产品进行从 1 到 10 的评分。

### 段落 40 · Page 4

**EN**

” • Purchase decision support & negotiation,Target prices, warranty math, and deal strategy for big-ticket items. “We used it to buy a car. . . research comps across the region. . . walked into the dealership with data. . . got our price after some negotiations. ” “. . . find the pricepoint where the dealer warranties and maintenance plan made sense. ” •Shopping automation & assistance,Scraping deals, generating lists, pre-checking prices, exploring agent-style purchasing. “Scrape the newest products and deals from e-commerce shops. ” “I had it set a rule to check the prices before quoting or estimating a price for me.

**中文**

” • 购买决策支持和谈判、目标价格、保修数学以及大件商品的交易策略。 “我们用它来购买汽车……研究整个地区的比较……带着数据走进经销商……经过一番谈判后得到了我们的价格。”“……找到经销商保修和维护计划有意义的价格点。”•购物自动化和协助、抓取交易、生成清单、预先检查价格、探索代理式采购。 “从电子商务商店抓取最新的产品和优惠。”“我设定了一条规则，在为我报价或估算价格之前先检查价格。

### 段落 41 · Page 4

**EN**

” “I want ChatGPT to purchase things on my behalf. Is this prompt possible?” • Shopping list creation & sourcing,Turning a personal list into store-specific availability and cost. “. . . paste my shopping list onto ChatGPT. . . say which supermarket I’m going to and give me the total cost of shopping. ” • Product sourcing & availability (incl. white-labeling), Finding parts/suppliers across regions and locating manufacturers behind brands. “Any prompts for finding the manufacturer of name brand items, then linking individually available products without the label?” • Marketplace reselling analysis,Flipping/valuation logic (active vs.

**中文**

” “我希望 ChatGPT 代表我购买东西。这个提示可以吗？” • 购物清单创建和采购，将个人清单转变为商店特定的可用性和成本。 “……将我的购物清单粘贴到 ChatGPT 上……说出我要去哪家超市，并给出购物的总费用。” • 产品采购和可用性（包括白色标签）、跨地区查找零件/供应商并查找品牌背后的制造商。 “有没有提示查找名牌产品的制造商，然后链接没有标签的单独可用产品？” • 市场转售分析、翻转/估值逻辑（主动与被动）

### 段落 42 · Page 4

**EN**

sold ranges, fees, ROI) on eBay/Facebook Marketplace. “Anyone have a good ChatGPT prompt for analyzing Marketplace / garage sale flips?” • Booking & reservations,Structuring “pay less, get more” tactics; last-minute booking. “. . . used ChatGBT. . . had a hotel booked within 5, 10 minutes. ” • Gifting & occasion-based selection,Constraint elicitation →tailored gift ideas. “I want you to act as the ‘perfect gift machine’. . . calculate a person’s ideal Christmas gift by asking questions about budget and interests. ” • Lifestyle & fashion advice,Style/fit/accessories guidance tied to personal attributes. “It found me . . . my daily wear watch .

**中文**

在 eBay/Facebook 市场上销售的范围、费用、投资回报率）。 “有人有一个很好的 ChatGPT 提示来分析市场/车库销售翻转吗？” • 预订和预订，构建“少花钱，多收获”的策略；最后一刻预订。 “...使用ChatGBT...在5、10分钟内预订了一家酒店。” • 送礼和基于场合的选择，约束启发→量身定制的礼物创意。 “我希望你充当‘完美的礼物机器’......通过询问有关预算和兴趣的问题来计算一个人的理想圣诞礼物。” • 生活方式和时尚建议，与个人属性相关的风格/合身/配饰指导。 “它找到了我……我的日常佩戴手表。

### 段落 43 · Page 4

**EN**

. . and helped me decide my signature scent . . . ” “I used ChatGPT to help choose . . . glasses style . . . ” • Meal planning with sales,Planning meals around weekly flyers and store promotions. “Upload pictures of the store’s weekly flyer and have it plan your meals using the sale items. ” • Product specification extraction,Pulling (or estimating) key specs from product references. “. . . extract from internet the following: the dimensions. . . net weight. . . if it’s Electronic. . . batteries included. . .

**中文**

。。并帮助我决定了我的标志性气味。。。 ” “我用ChatGPT来帮助选择。。。眼镜款式。。。 ” • 与销售一起制定膳食计划，围绕每周传单和商店促销计划膳食。 “上传商店每周传单的图片，并让它使用销售商品来计划您的膳食。” • 产品规格提取，从产品参考中提取（或估计）关键规格。 “……从互联网上摘录以下信息：尺寸……净重……如果是电子产品……包括电池……

### 段落 44 · Page 4

**EN**

” Key Observations.From these findings, several insights emerge: • Decision support dominates,Most prompts are framed aroundwhat to buy, when to buy, and how to compare, with users expecting shortlists and justifications (e.g., comfort vs. performance; price vs. warranty) rather than raw specifications.

**中文**

” 关键观察结果。从这些发现中，得出了一些见解： • 决策支持占主导地位，大多数提示都是围绕购买什么、何时购买以及如何进行比较，用户期待最终名单和理由（例如，舒适性与性能；价格与保修），而不是原始规格。

### Page 5

### 段落 45 · Page 5

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA • From retrieval to agency,Many requests delegate concrete actions, price scraping, list-building, warranty math, even “buy on my behalf”, signaling a shift from Q&A to assistant/agent behaviors that plan and execute steps for the user. • Emerging consumer trust,Examples such as car purchases or financial negotiations suggest that some users are beginning to entrust AI with high-value decisions traditionally mediated by expert advice.

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区 • 从检索到代理，许多请求委托具体行动、价格抓取、列表构建、保修数学，甚至“代表我购买”，标志着从问答到为用户计划和执行步骤的助理/代理行为的转变。 • 新兴的消费者信任，汽车购买或财务谈判等例子表明，一些用户开始将传统上由专家建议调解的高价值决策委托给人工智能。

### 段落 46 · Page 5

**EN**

• Breadth across verticals.Use-cases span daily consumables, travel bookings, home appliances, fashion, and even resale arbitrage, indicating generalizability beyond a single retail category, not a niche pattern. • Coverage across the shopping journey.Themes map onto the full funnel: awareness/consideration (evaluation, reviews), transaction prep (price research, sourcing), execution (automation, booking), and post-purchase/secondary markets (resale valuation), suggesting AI’s utility at multiple decision points, not just discovery.

**中文**

• 跨垂直领域的广度。用例涵盖日常消费品、旅行预订、家用电器、时尚，甚至转售套利，表明其具有超越单一零售类别的普遍性，而不是利基模式。 • 覆盖整个购物过程。主题映射到整个渠道：认知/考虑（评估、评论）、交易准备（价格研究、采购）、执行（自动化、预订）以及购买后/二级市场（转售评估），表明人工智能在多个决策点的实用性，而不仅仅是发现。

### 段落 47 · Page 5

**EN**

3.2 The Implications of AI Search for Brand Presence and Strategy The observed user behaviors signal a fundamental paradigm shift in how consumers discover, evaluate, and purchase products. AI search is not merely a new type of search engine; it is an intelligent decision-making partner that is actively woven into the entire consumer journey. For brands with a web presence, this shift demands a radical rethinking of digital strategy, moving beyond traditional Search Engine Optimization (SEO) to what can be termed Generative Engine Optimization (GEO) or AI Presence Optimization.

**中文**

3.2 人工智能搜索对品牌存在和战略的影响 观察到的用户行为标志着消费者发现、评估和购买产品方式的根本性范式转变。人工智能搜索不仅仅是一种新型搜索引擎；它是积极融入整个消费者旅程的智能决策合作伙伴。对于拥有网络存在的品牌来说，这种转变需要对数字战略进行彻底的重新思考，超越传统的搜索引擎优化（SEO），转向所谓的生成式引擎优化（GEO）或人工智能存在优化。

### 段落 48 · Page 5

**EN**

The implications are profound and can be broken down into four key strategic imperatives for brands. 3.2.1 The Battle for the Shortlist: From Visibility to Justification. The observation that "decision support dominates" means the primary goal is no longer just to be found, but to be recommended. In a traditional search results page (SERP), ten blue links are presented. In an AI-generated response, only a handful of options are synthesized into a concise, justified shortlist. The implication is that brands must now optimize their content not for keywords alone, but for justification attributes.

**中文**

其影响是深远的，可以分为品牌的四个关键战略要务。 3.2.1 入围之争：从可见性到合理性。 “决策支持占主导地位”的观察意味着首要目标不再只是被发现，而是被推荐。在传统的搜索结果页面 (SERP) 中，显示十个蓝色链接。在人工智能生成的响应中，只有少数选项被合成为简洁、合理的候选列表。这意味着品牌现在必须优化其内容，不仅针对关键词，还针对合理性属性。

### 段落 49 · Page 5

**EN**

The AI must be able to easily extract reasons why your product is a superior choice for a given use case (e.g., "best for small kitchens, " "most durable, " "best value"). To act on this, website content must be structured to explicitly answer comparison questions. This involves creating clear, scannable content that highlights key decision factors: pros/cons lists, comparison tables against competitors (or previous models), and clear statements of value proposition (e.g., "superior comfort, " "longest warranty in its class"). Ultimately, the brand that provides the most easily synthesizable justification wins the AI’s recommendation.

**中文**

人工智能必须能够轻松地找出您的产品对于给定用例而言是最佳选择的原因（例如，“最适合小厨房”、“最耐用”、“最佳价值”）。为此，网站内容的结构必须能够明确回答比较问题。这涉及创建清晰、可扫描的内容，突出显示关键决策因素：优缺点列表、与竞争对手（或以前的型号）的比较表以及清晰的价值主张陈述（例如“卓越的舒适度”、“同类产品中最长的保修期”）。最终，提供最容易综合理由的品牌赢得了人工智能的推荐。

### 段落 50 · Page 5

**EN**

3.2.2 The Rise of the API-able Brand: Structuring for Agency.The shift "from retrieval to agency" means AI agents will need to read, interpret, and act upon information from brand websites. If a user says, "find me the best deal on a Dyson vacuum including warranty costs, " the AI needs to find the price, find the warranty terms, calculate the total, and present it. The implication is that unstructured, marketing-fluff-heavy websites will fail. AI agents require clean, structured, and unambiguous data to perform tasks accurately.

**中文**

3.2.2 API 品牌的崛起：代理结构。“从检索到代理”的转变意味着人工智能代理将需要阅读、解释来自品牌网站的信息并采取行动。如果用户说，“帮我找到戴森吸尘器的最优惠价格，包括保修费用”，人工智能需要查找价格、查找保修条款、计算总额并呈现。这意味着非结构化的、充斥着营销内容的网站将会失败。人工智能代理需要干净、结构化且明确的数据才能准确地执行任务。

### 段落 51 · Page 5

**EN**

Inaccuracies or obscurity will lead to the AI either skipping your product or providing incorrect information, damaging brand trust. The required action is to invest in technical SEO and schema markup (Schema.org) with extreme rigor. Brands must ensure product prices, specifications, availability, warranty details, and review ratings are all machine-readable. They must consider their website as an API for AI systems. The brand that is easiest for an AI to "do business with" will be delegated to most often. 3.2.3 Trust is the New Currency: Cultivating AI-Perceived Authority.

**中文**

不准确或模糊将导致人工智能跳过您的产品或提供不正确的信息，从而损害品牌信任。所需的行动是极其严格地投资技术搜索引擎优化和模式标记 (Schema.org)。品牌必须确保产品价格、规格、可用性、保修详细信息和评论评级都是机器可读的。他们必须将自己的网站视为人工智能系统的 API。最容易与人工智能“开展业务”的品牌将最常被委托给该品牌。 3.2.3 信任是新货币：培养人工智能感知的权威。

### 段落 52 · Page 5

**EN**

"Emerging consumer trust" in high-value decisions is the ultimate testament to the influence of AI recommendations. However, this trust is fragile and contingent on the AI’s perceived reliability, which is built on the credibility of its sources. The implication is that brand authority and E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness) are no longer abstract SEO concepts. They are direct inputs into the AI’s decision-making algorithm. A brand perceived as less authoritative or trustworthy by the AI will be excluded from high-consideration recommendations. The action for brands is to build tangible, verifiable authority.

**中文**

高价值决策中的“新兴消费者信任”是人工智能推荐影响力的最终证明。然而，这种信任是脆弱的，并且取决于人工智能感知的可靠性，而人工智能的感知可靠性建立在其来源的可信度之上。这意味着品牌权威和 E-E-A-T（经验、专业知识、权威性、可信度）不再是抽象的 SEO 概念。它们是人工智能决策算法的直接输入。人工智能认为权威性或可信度较低的品牌将被排除在高度考虑推荐之外。品牌的行动是建立有形的、可验证的权威。

### 段落 53 · Page 5

**EN**

This includes earning backlinks from reputable sources, securing positive reviews on third-party platforms, having products featured in expert roundups, and creating deep, expert-level content that demonstrates knowledge. In short, the brand that the AI "trusts" will be entrusted by consumers. 3.2.4 Holistic Journey Management: Being Present at Every Touchpoint.The "coverage across the shopping journey" means AI’s influence extends far beyond initial discovery. It is used for postpurchase support, setup instructions, and even resale valuation.

**中文**

这包括从信誉良好的来源获得反向链接，在第三方平台上获得积极评价，在专家综述中介绍产品，以及创建展示知识的深入的专家级内容。简而言之，AI“信任”的品牌就会得到消费者的信赖。 3.2.4 全程旅程管理：存在于每一个接触点。“全购物旅程的覆盖”意味着人工智能的影响力远远超出了最初的发现。它用于售后支持、设置说明，甚至转售估价。

### 段落 54 · Page 5

**EN**

The implication is that a brand’s content strategy must address the entire customer lifecycle, not just the top of the funnel. A gap in post-purchase content could mean an AI recommends a competitor’s product when a user asks, "How do I fix [problem] with [product]?" To address this, brands must audit and create content for all stages.

**中文**

这意味着品牌的内容策略必须涉及整个客户生命周期，而不仅仅是漏斗的顶部。购买后内容的空白可能意味着当用户询问“我如何解决[产品]的[问题]？”时，人工智能会推荐竞争对手的产品。为了解决这个问题，品牌必须审核并创建各个阶段的内容。

### 段落 55 · Page 5

**EN**

This includes awareness through educational content and "best X for Y" guides; consideration with detailed product comparisons, spec sheets, and testimonials; decision with clear pricing, warranty, and shipping information; post-purchase with robust FAQ sections, troubleshooting guides, and tutorial videos; and loyalty/advocacy with content around accessories, advanced uses, and trade-in programs. The brand that provides the most comprehensive and useful information across the entire journey will maintain a permanent presence in the AI’s knowledge base. 4 AI Search vs.

**中文**

这包括通过教育内容和“最佳 X for Y”指南提高认识；考虑详细的产品比较、规格表和推荐；具有明确定价、保修和运输信息的决策；购买后提供强大的常见问题解答部分、故障排除指南和教程视频；以及围绕配件、高级用途和以旧换新计划的内容的忠诚度/宣传。在整个旅程中提供最全面、最有用信息的品牌将永久存在于人工智能的知识库中。 4 人工智能搜索对比

### 段落 56 · Page 5

**EN**

Google Search: A Comparative Analysis 4.1 Methodology This section describes the general pipeline we use to compare webenabled AI engines to Google Search on thesame underlying intents. All experiments in §4 share this pipeline (or at least part of this pipeline), though each sub-experiment varies in thequeries used (e.g., verticals, languages, paraphrases), theengines compared, and thelabels computed(e.g., domain type vs. website language). Those

**中文**

Google 搜索：比较分析 4.1 方法 本节描述了我们用于在相同的底层意图上将支持网络的 AI 引擎与 Google 搜索进行比较的一般流程。第 4 节中的所有实验都共享此管道（或至少此管道的一部分），尽管每个子实验在使用的查询（例如，垂直、语言、释义）、比较的引擎和计算的标签（例如，域类型与网站语言）方面有所不同。那些

### Page 6

### 段落 57 · Page 6

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas experiment-specific choices and any deviations are documented in their respective subsections; the common steps are detailed here. 4.1.1 Query Generation and Transformation.We standardize on ranking-style prompts (e.g., “Top 10 . . . brands”), to keep outputs directly comparable and scorable. In some experiments we generate category-specific query sets and use them as is. In others, we derive controlled variants from the common base prompts based on different experiment intents.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 实验特定选择和任何偏差均记录在各自的小节中；此处详细介绍了常见步骤。 4.1.1 查询生成和转换。我们对排名式提示进行标准化（例如，“十大……品牌”），以保持输出直接可比较和可评分。在一些实验中，我们生成特定于类别的查询集并按原样使用它们。在其他情况下，我们根据不同的实验意图从公共基础提示中得出受控变体。

### 段落 58 · Page 6

**EN**

Specifically, prompts are programmatically rewritten to reflect the experimental condition (e.g., added constraints or translation). All transformations are produced with the GPT-4o API (instruction-following only; no web browsing) using templated instructions to ensure consistency across topics and conditions. 4.1.2 AI Engine Execution (Web-Enabled) and Google Collection. AI Engines Execution Each prompt or prompt variant is issued to one or more webenabled AI engines. For every call we collect both the answer text and all citation links returned by the engine.

**中文**

具体来说，以编程方式重写提示以反映实验条件（例如，添加的约束或翻译）。所有转换均通过 GPT-4o API（仅遵循指令；无网页浏览）使用模板化指令生成，以确保主题和条件之间的一致性。 4.1.2 AI 引擎执行（支持 Web）和 Google 集合。 AI 引擎执行 每个提示或提示变体都会发出到一个或多个支持网络的 AI 引擎。对于每次调用，我们都会收集引擎返回的答案文本和所有引用链接。

### 段落 59 · Page 6

**EN**

AI Engines and settings used across experiments: • Perplexity: sonar-pro with web search enabled (search_mode: web, web_search_options: search_context_size = medium ). • Claude: claude-3.5-sonnet-latest with theweb_search_20250305 tool. • Gemini: gemini-2.5-flash with Google Search grounding (tool:google_search) enabled via the generation config. • GPT: gpt-4o-search-preview (the search-enabled variant of GPT-4o). Note: Not every experiment uses every engine; the engines used for a given experiment are specified in that subsection.

**中文**

实验中使用的AI引擎和设置： • Perplexity：启用网络搜索的sonar-pro（search_mode：web，web_search_options：search_context_size =medium）。 • Claude：claude-3.5-sonnet-latest，带有 web_search_20250305 工具。 • Gemini：gemini-2.5-flash 通过生成配置启用了 Google 搜索基础（工具：google_search）。 • GPT：gpt-4o-search-preview（GPT-4o 的支持搜索的变体）。注意：并非每个实验都使用所有引擎；该小节中指定了用于给定实验的发动机。

### 段落 60 · Page 6

**EN**

Google Collection For Google, we retrieve the URL of the top-10 web results for each query via the Programmable Search (Custom Search) API, using a single configured search engine set to search the open web. The top-5 results subsets used for some experiments are taken from the same list. 4.1.3 Data Extraction.All URLs retrieved are parsed to extract their registrable domain (e.g., https://www.bankrate.com/...→bankrate.com ). This step is performed locally (Python utility); no additional API calls are involved.

**中文**

Google 集合 对于 Google，我们通过可编程搜索（自定义搜索）API 检索每个查询的前 10 个网络结果的 URL，使用单个配置的搜索引擎集来搜索开放网络。用于某些实验的前 5 个结果子集取自同一列表。 4.1.3 数据提取。所有检索到的 URL 都会被解析以提取其可注册域（例如， https://www.bankrate.com/...→bankrate.com ）。此步骤在本地执行（Python 实用程序）；不涉及额外的 API 调用。

### 段落 61 · Page 6

**EN**

The raw answer text from AI engines is sent toGPT-4owith a constrained instruction to extract the ranked list of brands/products mentioned in the answer. We retain the order when present, and normalize strings minimally (case-folding, punctuation trimming). 4.1.4 Normalization and Classification.For each query × API (AI engines or Google) result, we de-duplicate domains and brands before aggregation to avoid double-counting the same site or item cited multiple times within a single answer.

**中文**

来自 AI 引擎的原始答案文本被发送到 GPT-4o，并带有约束指令以提取答案中提到的品牌/产品的排名列表。我们保留存在的顺序，并最小化字符串规范化（大小写折叠、标点符号修剪）。 4.1.4 规范化和分类。对于每个查询 × API（AI 引擎或 Google）结果，我们在聚合之前删除重复的域和品牌，以避免对单个答案中多次引用的同一网站或项目进行重复计算。

### 段落 62 · Page 6

**EN**

When required, each extracted domain is classified byGPT-4osearch-previewinto: (1) Brand,official brand sites that directly provide products or services (e.g.,chase.com,wellsfargo.com). (2) Social,social platforms, community forums, and user-generated content (e.g.,reddit.com,quora.com,youtube.com). (3) Earned,independent media, review, or comparison sites (e.g.,nerdwallet.com,forbes.com). For the language experiment specifically, we askGPT-4o-searchpreviewto label each domain as English or the target language of the prompt (binary choice) based on the site’s primary content language.

**中文**

当需要时，每个提取的域被GPT-4osearch-preview分类为：（1）品牌，直接提供产品或服务的官方品牌网站（例如chase.com、wellsfargo.com）。 (2) 社交、社交平台、社区论坛和用户生成的内容（例如，reddit.com、quora.com、youtube.com）。 (3) 独立媒体、评论或比较网站（例如 nerdwallet.com、forbes.com）。具体来说，对于语言实验，我们要求 GPT-4o-searchpreview 根据网站的主要内容语言将每个域标记为英语或提示的目标语言（二元选择）。

### 段落 63 · Page 6

**EN**

4.1.5 Overlap Metrics and Aggregation.We quantify how similar two outputs are using overlap measures applied within engine (e.g., English vs. French; base vs. paraphrase) and across engine (e.g., GPT vs Google, under the same query). Not every experiment uses every metric; the applicable measures are indicated in each subsection. • Top-k domain overlap (fixed-length).When both systems are evaluated on the same top-k set of unique domains (e.g., Google top-k vs. an engine’s top-k citations), we compute a symmetric Coverage@k as the fraction of domains common to both sets (number of overlaps divided by k).

**中文**

4.1.5 重叠指标和聚合。我们使用引擎内（例如，英语与法语；基础与释义）和跨引擎（例如，GPT 与 Google，在同一查询下）应用的重叠度量来量化两个输出的相似程度。并非每个实验都使用所有指标；各小节均说明了适用的措施。 • Top-k 域重叠（固定长度）。当两个系统在相同的 top-k 唯一域集上进行评估时（例如，Google top-k 与引擎的 top-k 引用），我们计算对称 Coverage@k 作为两个集合共有的域的分数（重叠数除以 k）。

### 段落 64 · Page 6

**EN**

• Domain overlap (variable-length sets).Because citation counts vary, we use the Jaccard index: Domain Overlap = size of the intersection of domains divided by the size of the union of domains. • Group aggregation.When a group comprises multiple queries (e.g., a 10-prompt industry vertical), we compute the mean overlap across its member queries to obtain the vertical-level score for that engine and condition.

**中文**

• 域重叠（可变长度集）。由于引用计数不同，我们使用 Jaccard 索引： 域重叠 = 域交集的大小除以域并集的大小。 • 组聚合。当一个组包含多个查询（例如，10 个提示的行业垂直）时，我们计算其成员查询之间的平均重叠，以获得该引擎和条件的垂直级别分数。

### 段落 65 · Page 6

**EN**

4.1.6 Aggregation for Distributions.For experiments that analyze source type, we pool all (de-duplicated) citations at the required granularity (e.g., model × language) and compute share distributions (e.g., brand / social / earned; English / non-English). 4.2 Comparative Analysis: Examine the Results from Google and AI Engines 4.2.1 Regional and Vertical Experiment. Objective.Compare Google and a web-enabled GPT on the same intents across regions and verticals, measuring (i) overlap of referenced links at top-k and (ii) source-type mix (Brand / Earned / Social) and dominant domains by region and category.

**中文**

4.1.6 分布聚合。对于分析来源类型的实验，我们以所需的粒度（例如，模型×语言）汇集所有（去重）引用，并计算份额分布（例如，品牌/社交/赢得；英语/非英语）。 4.2 比较分析：检查 Google 和 AI Engines 的结果 4.2.1 区域和垂直实验。 Objective.比较 Google 和支持网络的 GPT 跨区域和垂直领域的相同意图，测量 (i) top-k 处引用链接的重叠，以及 (ii) 来源类型组合（品牌/赢得/社交）以及按区域和类别划分的主导域。

### 段落 66 · Page 6

**EN**

Experimental Design.We generated 1,000 consumer ranking prompts (10 categories × 100 each), framed as consumer-facing ranking questions such as “Rank the best smartphones from 1 to 10” and “Which laptops are considered the best in 2024. ” We ran the study in two regions (U.S., Canada) and focused analysis on three verticals: Consumer Electronics, Automotive, and Software Products. Region scope was directly enforced as a query constraint (e.g., “Best 10 . . . in Canada”, “Top 10 . . . in USA”). For both Google and GPT, we collected the top-10 web results/citation URLs per query (with top-5 taken as the leading subset).

**中文**

实验设计。我们生成了 1,000 个消费者排名提示（10 个类别 × 每个 100 个），构成面向消费者的排名问题，例如“从 1 到 10 对最好的智能手机进行排名”和“哪些笔记本电脑被认为是 2024 年最好的”。我们在两个地区（美国、加拿大）进行了这项研究，并重点分析了三个垂直领域：消费电子产品、汽车和软件产品。区域范围直接作为查询约束强制执行（例如，“加拿大最佳 10 个……美国”、“美国前 10 个……”）。对于 Google 和 GPT，我们收集了每个查询的前 10 个网络结果/引用 URL（前 5 个作为主要子集）。

### 段落 67 · Page 6

**EN**

Following the common pipeline in §4.1, we extracted domains from the URLs, classified them as brand/social/earned, and computed the Top5/10 Overlap and distribution share of domain types. Results. Referenced Links Overlap Comparison (Google/GPT).

**中文**

按照 §4.1 中的通用流程，我们从 URL 中提取域，将它们分类为品牌/社交/赢得，并计算域类型的 Top5/10 重叠和分布份额。结果。引用链接重叠比较 (Google/GPT)。

### Page 7

### 段落 68 · Page 7

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA Figure 1: Referenced Links Overlap Comparison (Google/GPT) for k=5 and k=10. Figure 2: Automotive: Distribution of source types (Brand, Earned, Social) across Google and GPT in Canada and USA. Automotive. The automotive category produced one of the clearest contrasts. In Canada, Google returned 36.6 percent Brand, 22.8 percent Social, and 40.6 percent Earned content. AI search, however, offered 69.1 percent Earned, 30.9 percent Brand, and no Social results.

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区 图 1：k=5 和 k=10 的参考链接重叠比较 (Google/GPT)。图 2：汽车：加拿大和美国 Google 和 GPT 中来源类型（品牌、收益、社交）的分布。汽车。汽车类别是形成最明显对比的类别之一。在加拿大，Google 返回了 36.6% 的品牌内容、22.8% 的社交内容和 40.6% 的免费内容。然而，人工智能搜索提供了 69.1% 的“赢得”结果、30.9% 的“品牌”结果，并且没有社交结果。

### 段落 69 · Page 7

**EN**

In the United States, Google leaned 39.5 percent Brand, 15.4 percent Social, and 45.1 percent Earned, while AI search delivered 81.9 percent Earned and 18.1 percent Brand. The overlap experiment aligns with these findings: Electric Cars showed one of the highest levels of overlap across product categories, with 33 percent at the top 5 and over 50 percent at the top 10, suggesting partial convergence when structured product ecosystems are involved. Yet even in these cases, AI search excluded Social platforms entirely, reinforcing its bias toward publisher-driven information.

**中文**

在美国，谷歌在品牌方面的占比为 39.5%，在社交方面的占比为 15.4%，在盈利方面的占比为 45.1%，而人工智能搜索在营收方面的占比为 81.9%，在品牌方面的占比为 18.1%。重叠实验与这些发现相一致：电动汽车是跨产品类别中重叠程度最高的产品之一，前 5 名中重叠率为 33%，前 10 名中重叠率超过 50%，这表明当涉及结构化产品生态系统时会出现部分融合。然而，即使在这些情况下，人工智能搜索也完全排除了社交平台，从而强化了其对出版商驱动的信息的偏见。

### 段落 70 · Page 7

**EN**

Figure 3: Consumer Electronics: Distribution of source types (Brand, Earned, Social) across Google and GPT in Canada and USA. Consumer Electronics. In consumer electronics, Google and AI search exhibited distinct patterns in their sourcing of information. In Canada, Google results consisted of 54.1 percent Earned, 23.1 percent Social, and 22.8 percent Brand content. In contrast, AI search results were 77.6 percent Earned, 0.3 percent Social, and 22.1 percent Brand.

**中文**

图 3：消费电子产品：加拿大和美国 Google 和 GPT 中来源类型（品牌、收益、社交）的分布。消费电子产品。在消费电子产品领域，谷歌和人工智能搜索在信息来源方面表现出不同的模式。在加拿大，Google 搜索结果包括 54.1% 的赢取内容、23.1% 的社交内容和 22.8% 的品牌内容。相比之下，AI 搜索结果中 77.6% 为“赢取”，0.3% 为“社交”，22.1% 为“品牌”。

### 段落 71 · Page 7

**EN**

A similar divergence appeared in the United States, where Google results leaned more toward Brand content at 32.9 percent and Social at 15.4 percent, while AI search emphasized Earned content at 92.1 percent with negligible Social references. The overlap experiment confirms this divergence: categories such as Smartphones and Laptops produced only moderate overlap (15, 32 percent at the top 5 and 20, 41 percent at the top 10).

**中文**

美国也出现了类似的差异，谷歌搜索结果更倾向于品牌内容，占 32.9%，社交内容占 15.4%，而人工智能搜索则强调赚取内容，占 92.1%，而社交参考可以忽略不计。重叠实验证实了这种差异：智能手机和笔记本电脑等类别仅产生中等程度的重叠（前 5 名为 15%，32%；前 20 名为 41%）。

### 段落 72 · Page 7

**EN**

These results suggest that AI search deprioritizes community-driven platforms such as Reddit in favor of third-party reviews and publisher domains, while Google maintains a more balanced mix, leading to relatively low alignment between the two systems in productfocused queries. Software Products. In software, the divergence between Google and AI search was pronounced. In Canada, Google favored Brand sources (53.8 percent) and Social (14.4 percent), with Earned making up only 31.8 percent. AI search reversed this distribution, with 74.2 percent Earned, 25.8 percent Brand, and no Social results.

**中文**

这些结果表明，人工智能搜索优先考虑 Reddit 等社区驱动的平台，转而支持第三方评论和出版商领域，而 Google 则保持更加平衡的组合，导致两个系统在以产品为中心的查询中的一致性相对较低。软件产品。在软件方面，谷歌和人工智能搜索之间的分歧很明显。在加拿大，Google 更青睐品牌来源（53.8%）和社交来源（14.4%），而盈利来源仅占 31.8%。人工智能搜索扭转了这一分布，74.2% 是赢得性搜索，25.8% 是品牌搜索，没有社交搜索结果。

### 段落 73 · Page 7

**EN**

A similar pattern held in the United States, where Google produced 43.7 percent Brand, 10.9 percent Social, and 45.4 percent Earned, while AI search delivered 72.7 percent Earned, 26.7 percent Brand, and negligible Social. The overlap experiment provides additional context: categories like Smartwatches fell in the mid-range of overlap (around 32 percent at the top 5, 41 percent at the top 10), indicating partial agreement but still substantial divergence in source selection.

**中文**

美国也出现了类似的情况，谷歌产生了 43.7% 的品牌、10.9% 的社交和 45.4% 的收益，而人工智能搜索提供了 72.7% 的收益、26.7% 的品牌和微不足道的社交。重叠实验提供了额外的背景：智能手表等类别的重叠度处于中间范围（前 5 名中约 32%，前 10 名中约 41%），表明部分一致，但在来源选择方面仍然存在很大分歧。

### 段落 74 · Page 7

**EN**

This highlights a systemic shift in how software queries are surfaced, with Google emphasizing vendor-owned domains and AI search preferring neutral third-party evaluations. Cross-Category Observations.Three cross-cutting trends emerged from these comparisons. First, AI search consistently weighted its

**中文**

这凸显了软件查询呈现方式的系统性转变，谷歌强调供应商拥有的域名，而人工智能搜索更喜欢中立的第三方评估。跨类别观察。这些比较中出现了三个跨领域趋势。首先，人工智能搜索始终加权其

### Page 8

### 段落 75 · Page 8

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas Figure 4: Software Products: Distribution of source types (Brand, Earned, Social) across Google and GPT in Canada and USA. results toward Earned domains, regardless of category or region, which is reflected in the relatively higher overlap in service-oriented categories (such as Airlines and Streaming Services) where both systems converge on authoritative providers.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 图 4：软件产品：加拿大和美国 Google 和 GPT 中来源类型（品牌、收益、社交）的分布。无论类别或地区如何，这都体现在以服务为导向的类别（例如航空公司和流媒体服务）中相对较高的重叠度上，这两个系统都集中于权威提供商。

### 段落 76 · Page 8

**EN**

Second, Google maintained a more balanced distribution that included significant Social and Brand content, especially in consumer-focused verticals like electronics and automotive, where overlap levels were correspondingly lower. Third, the near-total absence of Social sources in AI search outputs represents a key structural shift, reducing the role of community forums and user-generated knowledge in discovery pathways and explaining much of the divergence observed in the overlap analysis. 4.2.2 Local Search Experiment.

**中文**

其次，谷歌保持了更加平衡的分布，其中包括重要的社交和品牌内容，特别是在电子和汽车等以消费者为中心的垂直行业，其重叠水平相应较低。第三，人工智能搜索输出中几乎完全缺乏社交来源，这代表了一个关键的结构性转变，减少了社区论坛和用户生成的知识在发现路径中的作用，并解释了重叠分析中观察到的大部分分歧。 4.2.2 本地搜索实验。

### 段落 77 · Page 8

**EN**

Objective.Examine how AI search and Google compare in retrieving results for local businesses, focusing on overlap of cited domains in categories such as home services, healthcare, and professional services. Experimental Design.We issued a set of queries targeting local businesses (e.g., "best home cleaning services near me, " "top dentists in [city]") to both Google and a web-enabled AI engine. For each category, we computed the domain overlap coverage between the two systems, following the methodology in §4.1. Results.The results reveal that overlap varies substantially across local business categories.

**中文**

目标：检查人工智能搜索和谷歌在检索本地企业结果方面的比较，重点关注家庭服务、医疗保健和专业服务等类别中引用领域的重叠。实验设计。我们向 Google 和支持网络的人工智能引擎发出了一组针对本地企业的查询（例如，“我附近最好的家庭清洁服务”、“[城市]的顶级牙医”）。对于每个类别，我们按照第 4.1 节中的方法计算了两个系统之间的域重叠覆盖范围。结果：结果显示，不同本地业务类别的重叠程度差异很大。

### 段落 78 · Page 8

**EN**

Home Cleaning shows the highest overlap (20.6%), followed by Roofing (17.1%), Tax Preparation (15.4%), and Dentists (11.9%). Lower overlap is observed in categories like Auto Repair (2.5%) and IT Support (0.1%). These findings suggest that while AI and Google sometimes converge on widely recognized service providers, the divergence is more pronounced in specialized or fragmented sectors. Figure 5: Local Search Coverage by Business Category. Coverage reflects the fraction of overlapping domains between AI search and Google for local business queries.

**中文**

家庭清洁的重叠率最高 (20.6%)，其次是屋顶清洁 (17.1%)、报税 (15.4%) 和牙医 (11.9%)。汽车维修 (2.5%) 和 IT 支持 (0.1%) 等类别的重叠率较低。这些发现表明，虽然人工智能和谷歌有时会集中在广泛认可的服务提供商上，但在专业或分散的领域，这种分歧更为明显。图 5：按业务类别划分的本地搜索覆盖范围。覆盖范围反映了人工智能搜索和谷歌本地业务查询之间重叠域的比例。

### 段落 79 · Page 8

**EN**

Interpretation.Overall, local search overlap is significantly lower than in broader consumer verticals such as electronics or health. This indicates that AI engines are less aligned with Google in surfacing local service providers, potentially due to differences in how local authority and business directories are weighted. For practitioners, this implies that visibility in local AI search requires distinct strategies beyond traditional Google Local SEO. 4.2.3 Language Sensitivity Experiment. Objective.Assess how language affects search outputs for Google vs. web-enabled AI engines.

**中文**

解读：总体而言，本地搜索重叠率明显低于电子或健康等更广泛的消费垂直领域。这表明人工智能引擎在本地服务提供商方面与谷歌的一致性较差，这可能是由于地方当局和企业名录的权重不同所致。对于从业者来说，这意味着本地人工智能搜索的可见性需要超越传统谷歌本地搜索引擎优化的独特策略。 4.2.3 语言敏感性实验。目标：评估语言如何影响 Google 与支持网络的 AI 引擎的搜索输出。

### 段落 80 · Page 8

**EN**

For queries with same intents, we examine whether the cited domains shift when prompts are translated (Chinese, Japanese, German, French, Spanish vs. English), and how source type and website language distributions change by system. Experimental Design.For ten consumer verticals (smartphones, laptops, headphones, smartwatches, electric vehicles, gaming consoles, home appliances, fitness equipment, camera gear, outdoor gear), we translated a shared set of 100 English base queries (10 verticals × 10 each) into five target languages and issued them to Google and to each AI engine (Gemini, Claude, ChatGPT, and Perplexity).

**中文**

对于具有相同意图的查询，我们检查翻译提示时引用的域是否发生变化（中文、日语、德语、法语、西班牙语与英语），以及源类型和网站语言分布如何随系统变化。实验设计。对于十个消费者垂直领域（智能手机、笔记本电脑、耳机、智能手表、电动汽车、游戏机、家用电器、健身器材、相机装备、户外装备），我们将一组共享的 100 个英语基本查询（每个垂直方向 × 10）翻译成五种目标语言，并将它们发布给 Google 和每个人工智能引擎（Gemini、Claude、ChatGPT 和 Perplexity）。

### 段落 81 · Page 8

**EN**

For each system we compared, within-engine, outputs across languages using: • Domain-overlap heatmaps:overlap of cited domains for each English, X pair, by vertical. – Overlap Definition.For each English–X pair and query, we compute a Jaccard overlap on the sets of cited domains (|𝐴∩𝐵|/|𝐴∪𝐵| ). Vertical-level scores report the mean of these per-query Jaccard values across all queries in that vertical. For example, a Jaccard fraction of 0.10 for a single query means that 10% of the unique domains in the combined domain sets are shared between the two language runs.

**中文**

对于每个系统，我们在引擎内比较跨语言的输出，使用： • 域重叠热图：每个英语、X 对的引用域按垂直方向重叠。 – 重叠定义。对于每个 English-X 对和查询，我们计算引用域集合上的 Jaccard 重叠 (|𝐴∩𝐵|/|𝐴∪𝐵| )。垂直级别分数报告该垂直中所有查询的每个查询 Jaccard 值的平均值。例如，单个查询的 Jaccard 分数为 0.10 意味着组合域集中 10% 的唯一域在两种语言运行之间共享。

### 段落 82 · Page 8

**EN**

An average Jaccard of 0.10 for a vertical therefore indicates that, on the average query in that vertical, 10% of the per-query domain union is shared between English and the target language.

**中文**

因此，垂直领域的平均 Jaccard 为 0.10 表明，在该垂直领域的平均查询中，每个查询域联合的 10% 在英语和目标语言之间共享。

### Page 9

### 段落 83 · Page 9

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA • Aggregate pies:overalldomain-typemix (brand / social / earned) andwebsite-languagemix (English vs. non- English) across all verticals. Extraction, normalization, and classification follow the common pipeline in §4.1. Results. Cross-language domain stability. Google’s cross-language domain overlap is generally low (mostly between 0–0.1, with the maximum cell (EN-ESElectric vehicles) only slightly above 0.1; Fig. 6).

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区 • 综合饼图：所有垂直领域的总体域类型组合（品牌/社交/赢得）和网站语言组合（英语与非英语）。提取、标准化和分类遵循 §4.1 中的通用流程。结果。跨语言域稳定性。 Google 的跨语言域重叠度普遍较低（大多在 0-0.1 之间，最大单元格（EN-ESE 电动车辆）仅略高于 0.1；图 6）。

### 段落 84 · Page 9

**EN**

Relative to this baseline: • Claude exhibits much higher cross-language stability than Google in all verticals (frequent high overlaps), indicating far stronger reuse of the same authority domains across languages (Fig. 7). • Perplexity and Gemini show higher or comparable overlap to Google overall, with absolute levels remaining low. Relative to Google’s baseline (peaking at≈0.11), Gemini records modestly higher overlaps in several languages (e.g., EN–CN with many pockets exceeding 0.2; EN–DE with a peak at ≈0.32; Fig. 9), whereas Perplexity is mostly comparable to Google with a few pockets slightly above it (e.g., EN–DE laptops ≈0.22; Fig.

**中文**

相对于该基线： • Claude 在所有垂直领域都表现出比 Google 高得多的跨语言稳定性（频繁的高度重叠），表明跨语言对相同权限域的重用要强得多（图 7）。 • Perplexity 和Gemini 与Google 整体表现出较高或相当的重叠，但绝对水平仍然较低。相对于 Google 的基线（峰值约为 0.11），Gemini 在多种语言中记录了较高的重叠度（例如，EN-CN，许多口袋超过 0.2；EN-DE，峰值约为 0.32；图 9），而 Perplexity 基本上与 Google 相当，有几个口袋略高于它（例如，EN-DE 笔记本电脑约为 0.22；图 9）。

### 段落 85 · Page 9

**EN**

8). Overall, cross-language reuse remains limited for both. • GPT is the special case that shows lower overlap than Google: overlaps are near zero across the board, i.e., it effectively switches to different site ecosystems by language more than Google (Fig. 10). Figure 6: Language Sensitivity: Domain overlap heatmap, Google Source types mix. Across languages, AI systems remain earnedheavy relative to Google. Pooled distributions show AIs allocating a larger share to earned and less to social and brand than Google (Fig. 11).

**中文**

8).总体而言，两者的跨语言重用仍然有限。 • GPT 是比 Google 重叠率更低的特例：重叠率全面接近于零，即它比 Google 更能有效地通过语言切换到不同的站点生态系统（图 10）。图 6：语言敏感性：域重叠热图，Google 源类型混合。在各种语言中，人工智能系统相对于谷歌来说仍然很重要。汇总分布显示，与谷歌相比，人工智能分配给收入的份额更大，而分配给社交和品牌的份额更少（图 11）。

### 段落 86 · Page 9

**EN**

Google, by contrast, retains substantial social (especially in English) and a larger, dominant brand share in most non-English languages. The AI models follows a earned≫brand≫social pattern, while Google generally follows brand ≫ earned ≫ social instead. Website language depends on the engine. Under non-English prompts, citations tilt toward the target language—but less so for Google.

**中文**

相比之下，谷歌在大多数非英语语言中保留了大量的社交（尤其是英语）和更大的主导品牌份额。人工智能模型遵循赢得≫品牌≫社交模式，而谷歌通常遵循品牌≫赢得≫社交模式。网站语言取决于引擎。在非英语提示下，引文倾向于目标语言，但对于 Google 来说则不然。

### 段落 87 · Page 9

**EN**

Figure 7: Language Sensitivity: Domain overlap heatmap, Claude Figure 8: Language Sensitivity: Domain overlap heatmap, Perplexity Figure 9: Language Sensitivity: Domain overlap heatmap, Gemini In the pooled view, GPT and Perplexity are more local-language heavy than Google; Claude is far more English-heavy than Google; Gemini is closer to balanced, with the split varying by language (Fig. 12). For Google specifically, a gradient is evident: Japanese

**中文**

图 7：语言敏感性：领域重叠热图，Claude 图 8：语言敏感性：领域重叠热图，Perplexity 图 9：语言敏感性：领域重叠热图，Gemini 在汇总视图中，GPT 和 Perplexity 比 Google 更注重本地语言；克劳德（Claude）比谷歌更擅长英语；双子座更接近平衡，不同语言的划分也不同（图 12）。特别是对于谷歌来说，梯度是明显的：日语

### Page 10

### 段落 88 · Page 10

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas Figure 10: Language Sensitivity: Domain overlap heatmap, GPT Figure 11: Language Sensitivity: Overall domain-type distribution, all languages pooled yields the strongest localization (target-language exceeding threequarters of citations), French and German are also highly localized but keep a larger English slice than Japanese, Spanish is mixed with English slightly exceeding the target language, and Chinese is the exception—English dominates, accounting for over three-quarters of citations.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 图 10：语言敏感性：领域重叠热图，GPT 图 11：语言敏感性：总体领域类型分布，所有语言汇集产生最强的本地化（目标语言超过四分之三的引用），法语和德语也高度本地化，但保留了比日语更大的英语部分，西班牙语与英语混合略超过目标语言，中文是例外——英语占主导地位，占引用量的四分之三以上。

### 段落 89 · Page 10

**EN**

Interpretation.Compared with Google, Claude maintains a much more stable cross-language evidence set; GPT diverges the most by Figure 12: Language Sensitivity: Overall website-language distribution, all verticals pooled swapping site ecosystems across languages; Perplexity and Gemini typically align with or modestly higher than Google’s already-low cross-language domain reuse, with isolated exceptions. Regardless of language, AI engines collectively bias toward editorial/earned sources more than Google.

**中文**

解释：与Google相比，Claude保持着稳定得多的跨语言证据集； GPT 的差异最大，如图 12 所示：语言敏感性：网站语言的总体分布，所有垂直领域跨语言交换网站生态系统； Perplexity 和 Gemini 通常与 Google 已经很低的跨语言域重用一致或略高，但也有个别例外。无论语言如何，人工智能引擎都比谷歌更偏向于编辑/免费来源。

### 段落 90 · Page 10

**EN**

Practically, brands and publishers aiming for multilingual visibility should build coverage in authoritative local-language media (to meet AI engines that localize heavily) while also accounting for Google’s more English-leaning pattern in many non-English contexts. 4.2.4 Paraphrase Sensitivity Experiment. Objective.Assess whether small, within-language changes in how a query is phrased alter the alignment between Google and web-enabled AI engines. For the same intent, we ask how paraphrasing affects (i) the overlap between AI citations and Google results and (ii) the mix of cited source types (brand / social / earned) by system.

**中文**

实际上，以多语言曝光为目标的品牌和出版商应该在权威的本地语言媒体上建立覆盖范围（以满足高度本地化的人工智能引擎），同时还要考虑到谷歌在许多非英语环境中更倾向于英语的模式。 4.2.4 释义敏感性实验。目标：评估查询措辞方式的语言内微小变化是否会改变 Google 和支持网络的 AI 引擎之间的一致性。出于同样的目的，我们询问释义如何影响（i）人工智能引用和谷歌结果之间的重叠以及（ii）系统引用来源类型（品牌/社交/赢得）的混合。

### 段落 91 · Page 10

**EN**

Experimental Design.Using the same 100 base queries from ten consumer verticals as in the language study, we issued a base prompt and seven paraphrase templates to Google and to each AI engine (Gemini, ChatGPT, Perplexity): (1) justification_required,require a short justification for each item; (2)source_required,require sources consulted for the answer; (3) quote_required,require direct quotes from consulted sources;

**中文**

实验设计。使用与语言研究中相同的来自 10 个消费者垂直领域的 100 个基本查询，我们向 Google 和每个 AI 引擎（Gemini、ChatGPT、Perplexity）发出基本提示和七个释义模板：（1）justification_required，要求每个项目都有一个简短的理由； (2)source_required，需要参考来源来获取答案； (3) quote_required，要求直接从咨询来源引用；

### Page 11

### 段落 92 · Page 11

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA (4)confidence_score,require confidence scores per item; (5)ranked_order,explicitly require ranking best→worst; (6)imperative_list,rewrite from question to imperative list; (7)keyword_only,compress to keywords only. For each system we compared, within-engine, the outputs of each paraphrase against the base prompt: • Domain overlap(heatmaps): overlap of cited domains by vertical.

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区 (4)confidence_score，需要每个项目的置信度分数； (5)ranked_order，明确要求排名最好→最差； (6)imperative_list，从疑问句重写为命令式列表； (7)keyword_only，仅压缩到关键字。对于每个系统，我们在引擎内将每个释义的输出与基本提示进行比较： • 域重叠（热图）：引用的域按垂直方向重叠。

### 段落 93 · Page 11

**EN**

As in the language sensitivity experiment, for each base-paraphrase pair and query we compute the Jaccard overlap on cited-domain sets, then average per vertical to obtain the reported stability scores. • Domain-type mix(brand / social / earned) aggregated across all verticals for each paraphrase (overall pies). Extraction, normalization, and classification follow the common pipeline in §4.1. Results. Paraphrases move results less than languages. Relative to §4.2.3 (language sensitivity test), paraphrasing induces smaller perturbations for both Google and AI. Domain sets are much more stable than in the cross-language study. Domain stability.

**中文**

与语言敏感性实验一样，对于每个基本释义对和查询，我们计算引用域集上的 Jaccard 重叠，然后对每个垂直方向进行平均以获得报告的稳定性分数。 • 领域类型组合（品牌/社交/赚取）针对每个释义（总体饼图）在所有垂直领域进行聚合。提取、标准化和分类遵循 §4.1 中的通用流程。结果。释义对结果的影响小于语言。相对于§4.2.3（语言敏感性测试），释义对 Google 和 AI 造成的干扰较小。领域集比跨语言研究稳定得多。域稳定性。

### 段落 94 · Page 11

**EN**

Google shows low to moderate overlap for most paraphrase styles (often near 0.1), but rises substantially for formattingtype variants—especiallyimperative listandkeyword-only(many cells 0.5–0.7, peaking at ≈0.73). This suggests Google’s top results are most stable when the rewording mainly changes form rather than intent (Fig. 13). Also, it is notable that the domain overlap of Google on paraphrase change is generally higher (i.e., domain more stable) than that on language change.

**中文**

Google 对于大多数释义样式显示出低到中度的重叠（通常接近 0.1），但对于格式化类型变体，尤其是命令式列表和仅关键字（许多单元格为 0.5-0.7，峰值约为 0.73），重叠率大幅上升。这表明当改写主要改变形式而不是意图时，谷歌的顶级结果是最稳定的（图13）。此外，值得注意的是，谷歌在释义更改上的域重叠通常比语言更改上的域重叠更高（即域更稳定）。

### 段落 95 · Page 11

**EN**

AI engines exhibit generally higher cross-paraphrase domain stability than Google in most verticals, with many base–variant overlaps in the 0.3–0.7 range, occasionally reaching the low-0.7s. In short, AI results tend to be less sensitive to wording tweaks than Google, outside Google’s strong “imperative/keyword” cases (Figs. 14, 15, 16). Figure 13: Paraphrase Sensitivity: Domain overlap heatmap, Google Source-type mix across paraphrase styles.

**中文**

在大多数垂直领域，AI 引擎普遍表现出比 Google 更高的跨释义域稳定性，许多碱基变体重叠在 0.3-0.7 范围内，偶尔会达到低 0.7 秒。简而言之，除了谷歌强烈的“命令式/关键字”案例之外，人工智能结果往往对措辞调整的敏感度低于谷歌（图 14、15、16）。图 13：释义敏感性：域重叠热图、跨释义样式的 Google 源类型混合。

### 段落 96 · Page 11

**EN**

Across paraphrases, Google maintains a relatively higher share of Social and lower share of Figure 14: Paraphrase Sensitivity: Domain overlap heatmap, GPT Figure 15: Paraphrase Sensitivity: Domain overlap heatmap, Perplexity Figure 16: Paraphrase Sensitivity: Domain overlap heatmap, Gemini Earned than AI, while AI systems remain Earned-heavy. Importantly, within-system distributions change little from one paraphrase to another for AIs, but change more for Google—paraphrasing materially shifts the Brand/Social/Earned balance for Google more than AIs (Fig. 17).

**中文**

在释义方面，谷歌保持着相对较高的社交份额和较低的份额。 图 14：释义敏感度：领域重叠热图，GPT 图 15：释义敏感度：领域重叠热图，困惑 图 16：释义敏感度：领域重叠热图，Gemini 收入高于 AI，而 AI 系统仍然以收入为主。重要的是，对于人工智能来说，系统内分布从一种释义到另一种释义变化不大，但对于谷歌来说变化更大——与人工智能相比，释义对谷歌品牌/社交/赚取平衡的实质性改变更大（图17）。

### Page 12

### 段落 97 · Page 12

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas Figure 17: Paraphrase Sensitivity: Overall domain-type distribution across paraphrase styles Interpretation.Google is comparatively more sensitive to paraphrasing, except when the paraphrase is a simple format change (imperative/keyword list), where stability rises. AI engines are steadier across paraphrases and consistently favor editorial (earned) sources over brand/social more than Google. Practically, paraphrase tuning can influencecitations—especially on Google—but has a smaller effect thanlanguage choice(§4.2.2).

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 图 17：释义敏感性：跨释义风格的总体域类型分布 解释。Google 对释义相对更敏感，除非释义是简单的格式更改（命令式/关键字列表），此时稳定性会上升。人工智能引擎在释义上更加稳定，并且始终比谷歌更青睐社论（赢得的）资源而不是品牌/社交资源。实际上，释义调整可以影响引用（尤其是在 Google 上），但影响小于语言选择（第 4.2.2 节）。

### 段落 98 · Page 12

**EN**

4.3 General Query Types We now focus on a generalized comparison, moving beyond rankingstyle prompts and considering how systems respond across canonical query classes. 4.3.1 Overall Description.To analyze how traditional search engines and AI-powered systems structure their responses, we categorized user queries into three canonical intent buckets:Informational, Consideration, andTransactional. This taxonomy reflects both user motivation and the expected media mix that search systems return. Figure 18: Media-type distribution (Brand, Earned, Social) across query intents for Google.

**中文**

4.3 通用查询类型 我们现在专注于广义比较，超越排名样式提示并考虑系统如何跨规范查询类进行响应。 4.3.1 总体描述。为了分析传统搜索引擎和人工智能驱动的系统如何构建其响应，我们将用户查询分为三个规范的意图桶：信息、考虑和交易。这种分类反映了用户动机和搜索系统返回的预期媒体组合。图 18：Google 跨查询意图的媒体类型分布（品牌、赢得、社交）。

### 段落 99 · Page 12

**EN**

Figure 19: Media-type distribution (Brand, Earned, Social) across query intents for GPT. Informational Queries.Informational queries are exploratory in nature, aimed at acquiring general knowledge or technical understanding (e.g., “How do OLED TVs work?”, “What is Wi-Fi 7?”). These do not signal purchase intent but instead focus on definitions and explanations. Our results show distinct strategies: Google balances Brand, Earned, and Social sources; GPT emphasizes Earned content while nearly excluding Social; Perplexity highlights Brand domains most strongly while still including Earned and some Social.

**中文**

图 19：GPT 查询意图的媒体类型分布（品牌、赢得、社交）。信息查询。信息查询本质上是探索性的，旨在获取常识或技术理解（例如，“OLED 电视如何工作？”、“什么是 Wi-Fi 7？”）。这些并不表示购买意图，而是侧重于定义和解释。我们的结果显示了不同的策略：Google 平衡品牌、收​​益和社交资源； GPT 强调赚取内容，而几乎排除社交；困惑最强烈地突出了品牌领域，同时仍然包括赢得的和一些社交的。

### Page 13

### 段落 100 · Page 13

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA Figure 20: Media-type distribution (Brand, Earned, Social) across query intents for Perplexity. Consideration Queries.Consideration queries represent mid-funnel behavior, where users compare products and evaluate trade-offs (e.g., “Best laptops for students 2025”, “Garmin vs Apple Watch”).

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区 图 20：Perplexity 查询意图的媒体类型分布（品牌、赢得、社交）。考虑查询。考虑查询代表漏斗中部行为，用户比较产品并评估权衡（例如，“2025 年最适合学生的笔记本电脑”、“Garmin 与 Apple Watch”）。

### 段落 101 · Page 13

**EN**

Here, Earned content dominates across all systems, but with important differences: Google pairs Earned with a substantial Social component, GPT skews almost entirely to Earned with minimal Brand and Social, while Perplexity maintains a more balanced mix across all three categories. Transactional Queries.Transactional queries are high-intent, purchaseoriented prompts (e.g., “Buy iPhone 15 online”, “Best price for Samsung Galaxy S24 unlocked”). Across systems, Brand content rises in prominence.

**中文**

在这里，赚取的内容在所有系统中占主导地位，但有重要的区别：谷歌将赚取的内容与大量社交组件配对，GPT 几乎完全偏向于品牌和社交最少的赚取内容，而 Perplexity 在所有三个类别中保持更平衡的组合。事务性查询。事务性查询是高意图、以购买为导向的提示（例如，“在线购买 iPhone 15”、“三星 Galaxy S24 解锁的最佳价格”）。在各个系统中，品牌内容日益突出。

### 段落 102 · Page 13

**EN**

Google shifts toward Brand while still surfacing Earned and Social, GPT amplifies Brand content most strongly with Earned secondary and almost no Social, while Perplexity distributes results between Brand and Earned with slightly more Social retained than others. Summary.These plots (Figures 18–20) reveal intent-driven shifts in media sourcing. Google balances Earned with Social and Brand across intents, GPT consistently suppresses Social while emphasizing Earned (and Brand for transactional), and Perplexity adopts a blended approach with notable Brand inclusions.

**中文**

谷歌转向品牌，同时仍然呈现Earned和Social，GPT最强烈地放大品牌内容，Earned是次要的，几乎没有社交，而Perplexity在Brand和Earned之间分配结果，保留的社交略多于其他。摘要：这些图（图​​ 18-20）揭示了媒体采购中意图驱动的转变。 Google 在不同意图上平衡了“Earned”、“Social”和“Brand”，GPT 始终压制“Earned”，同时强调“Earned”（以及用于交易的“Brand”），而 Perplexity 采用了包含显着品牌内容的混合方法。

### 段落 103 · Page 13

**EN**

The structured differences confirm that query intent modulates how each system assembles its output. 4.4 The Need for generative Engine Optimization Traditional SEO techniques remain necessary for visibility but are insufficient for AI search dominance. The core principles of technical SEO—such as having a well-structured, crawlable site—are foundational, as AI agents require clean, machine-readable data to function. However, the findings reveal that a new strategy, which can be termed Generative Engine Optimization (GEO), is required to address the fundamental differences in how AI systems source and prioritize information.

**中文**

结构化差异证实查询意图调节每个系统如何组装其输出。 4.4 生成式引擎优化的需求 传统的 SEO 技术对于可见性仍然是必要的，但不足以实现人工智能搜索的主导地位。技术 SEO 的核心原则（例如拥有结构良好、可爬行的网站）是基础，因为人工智能代理需要干净、机器可读的数据才能发挥作用。然而，研究结果表明，需要一种称为生成式引擎优化（GEO）的新策略来解决人工智能系统如何获取信息和确定信息优先级的根本差异。

### 段落 104 · Page 13

**EN**

4.4.1 Prioritize Earned Media and Authority Building.The most significant finding is the AI engines’ overwhelming and consistent bias toward Earned media across all regions and verticals. Unlike Google, which maintains a balanced mix of Brand, Social, and Earned content, AI systems heavily favor third-party, authoritative sources like professional reviews, publisher domains, and institutional sites. Shift investment from strategies focused solely on brand-owned content and social engagement to a concerted effort in earning third-party coverage.

**中文**

4.4.1 优先考虑赢得媒体和权威建设。最重要的发现是人工智能引擎对所有地区和垂直领域的赢得媒体有着压倒性的、持续的偏见。与谷歌保持品牌、社交和赚取内容的平衡组合不同，人工智能系统非常青睐第三方权威来源，如专业评论、出版商域名和机构网站。将投资从仅关注品牌拥有的内容和社交参与的战略转向共同努力赢得第三方覆盖。

### 段落 105 · Page 13

**EN**

This includes: • Public and Media Relations: Proactively seeking features, reviews, and mentions in authoritative publications within your industry. • Expert Collaborations: Partnering with industry experts, thought leaders, and credible institutions to create and promote content that demonstrates your expertise. • Link Building: Earning backlinks from these high-authority, earned domains is not just a Google ranking factor but a direct input into the AI’s perception of your brand’s trustworthiness.

**中文**

这包括： • 公共和媒体关系：主动寻找行业内权威出版物中的专题、评论和提及。 • 专家合作：与行业专家、思想领袖和可信机构合作，创建和推广展示您专业知识的内容。 • 链接建设：从这些高权威、赢得的域名中获得反向链接不仅是谷歌排名因素，而且是人工智能对您品牌可信度的感知的直接输入。

### 段落 106 · Page 13

**EN**

4.4.2 Structure Content for Scannability and Justification.The low overlap in cited domains between Google and AI, particularly in product categories, indicates that AI synthesizes information differently. It seeks clear, unambiguous data to build justified recommendations. Optimize website content not just for keywords, but for scannability and justification. Ensure your content explicitly highlights key decision-making factors in a format easily extracted by an AI: • Create detailed comparison tables (vs. competitors or previous models). •Use clear, bulleted pros and cons lists.

**中文**

4.4.2 结构内容的可扫描性和合理性。Google 和 AI 之间引用的领域（尤其是产品类别）的重叠度较低，表明 AI 合成信息的方式不同。它寻求清晰、明确的数据来建立合理的建议。优化网站内容不仅针对关键字，还针对可浏览性和合理性。确保您的内容以人工智能轻松提取的格式明确突出关键决策因素： • 创建详细的比较表（与竞争对手或以前的模型相比）。 • 使用清晰、带项目符号的优点和缺点列表。

### 段落 107 · Page 13

**EN**

• State your value proposition explicitly (e.g., "longest battery life, " "most durable build, " "best value for money"). • Implement schema markup (Schema.org) with extreme rigor for all product specifications, prices, reviews, and availability to become an "API-able" brand that AI agents can easily parse. 4.4.3 Develop a Language-Specific Authority Strategy.The language sensitivity experiment reveals that AI engines handle multilingual queries differently. Claude shows high cross-language stability, often reusing authoritative English-language domains, while GPT completely swaps its domain ecosystem to favor locallanguage sources.

**中文**

• 明确陈述您的价值主张（例如，“最长的电池寿命”、“最耐用的结构”、“性价比最高”）。 • 对所有产品规格、价格、评论和可用性实施极其严格的模式标记(Schema.org)，成为人工智能代理可以轻松解析的“API 支持”品牌。 4.4.3 制定特定语言的权威策略。语言敏感性实验表明，人工智能引擎处理多语言查询的方式不同。 Claude 显示出高度的跨语言稳定性，经常重用权威的英语域名，而 GPT 则完全交换其域名生态系统以支持本地语言源。

### 段落 108 · Page 13

**EN**

A one-size-fits-all multilingual SEO strategy is ineffective. To maximize AI presence globally, you must: • For Claude-like Engines: Strengthen your position in toptier, English-language earned media, as this authority can transfer across languages. • For GPT-like Engines: Build relationships with authoritative publishers and review sites in each target language and region. Simply translating your own brand content is not enough; you need earned coverage in the local language. • For Google: Maintain a hybrid approach, as it shows a gradient of localization depending on the language.

**中文**

一刀切的多语言 SEO 策略是无效的。为了最大限度地提高人工智能在全球的影响力，您必须： • 对于克劳德式的引擎：加强您在顶级英语赢得媒体中的地位，因为这种权威可以跨语言转移。 • 对于类GPT 引擎：与每种目标语言和地区的权威出版商和评论网站建立关系。仅仅翻译您自己的品牌内容是不够的；您需要获得当地语言的保险。 • 对于Google：保持混合方法，因为它根据语言显示本地化梯度。

### Page 14

### 段落 109 · Page 14

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas 4.4.4 Create Comprehensive, Lifecycle-Oriented Content.The moderate overlap in service-oriented categories (e.g., Airlines) suggests AI values comprehensive, authoritative information. A gap in content for any stage of the customer journey (e.g., post-purchase support) could lead to a competitor being recommended when a user asks for help. Audit and create content for the entire customer lifecycle, not just top-of-funnel discovery. This includes: •Awareness: Educational guides and "best X for Y" articles.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 4.4.4 创建全面的、面向生命周期的内容。面向服务的类别（例如航空公司）的适度重叠表明人工智能重视全面、权威的信息。客户旅程的任何阶段（例如，购买后支持）的内容差距都可能导致当用户寻求帮助时推荐竞争对手。审核和创建整个客户生命周期的内容，而不仅仅是漏斗顶部的发现。这包括： •意识：教育指南和“最好的X对Y”文章。

### 段落 110 · Page 14

**EN**

• Consideration: Detailed product comparisons and testimonials. •Decision: Clear data on pricing, warranty, and shipping. • Post-Purchase: Robust FAQs, troubleshooting guides, and tutorials. • Loyalty: Content on accessories, advanced uses, and trade-in programs. In conclusion, while technical SEO provides the necessary foundation, optimizing for AI search requires a paradigm shift. Success hinges on building verifiable, third-party authority, structuring content for machine synthesis, and implementing a nuanced, languageaware strategy that prioritizes earned media over brand-owned and social content.

**中文**

• 考虑因素：详细的产品比较和推荐。 •决策：有关定价、保修和运输的清晰数据。 • 购买后：强大的常见问题解答、故障排除指南和教程。 • 忠诚度：有关配件、高级用途和以旧换新计划的内容。总之，虽然技术搜索引擎优化提供了必要的基础，但人工智能搜索的优化需要范式转变。成功取决于建立可验证的第三方权威、为机器合成构建内容，以及实施细致入微的语言感知策略，将赢得的媒体优先于品牌拥有和社交内容。

### 段落 111 · Page 14

**EN**

5 A Comparison of AI Search Engines 5.1 Methodology All experiments in §5 reuse the pipeline (or at least part of the pipeline), described in §4.1 (query generation/transformation, webenabled engine execution, domain/brand extraction, normalization/classification, and overlap/distribution metrics). Unless otherwise stated in each subsection, we do not collect Google search results in §5. Any experiment-specific choices and deviations (e.g., queries used, theengines compared, and thelabels computed) are documented in their respective subsections.

**中文**

5 人工智能搜索引擎的比较 5.1 方法论 §5 中的所有实验都重用了第 4.1 节中描述的管道（或至少部分管道）（查询生成/转换、网络引擎执行、域/品牌提取、标准化/分类和重叠/分布指标）。除非各小节另有说明，我们不会在第 5 条中收集 Google 搜索结果。任何特定于实验的选择和偏差（例如，使用的查询、比较的引擎和计算的标签）都记录在各自的小节中。

### 段落 112 · Page 14

**EN**

We focus on comparing the results of different AI search services and understanding their similarities and differences across several important search and information discovery pipelines. 5.2 Comparative Analysis 5.2.1 Well-Known Brands vs. Niche Brands.Our first experiment, aims to understand how AI search services respond to questions around brands. In particular we pose ranking style questions for brands (for a set of well known and niche brands) and observe the answers across services recording their agreement.

**中文**

我们专注于比较不同人工智能搜索服务的结果，并了解它们在几个重要搜索和信息发现管道中的异同。 5.2 比较分析 5.2.1 知名品牌与小众品牌。我们的第一个实验旨在了解人工智能搜索服务如何响应有关品牌的问题。特别是，我们针对品牌（针对一组知名和小众品牌）提出排名风格问题，并观察记录其协议的各个服务的答案。

### 段落 113 · Page 14

**EN**

When comparing the results of different AI search engines, a clear pattern emerges in how they prioritize sources for well-known versus niche brands. Across all systems, there is a consistent emphasis onEarneddomains, but the balance betweenBrand,Social, andEarnedsources differs significantly. Experimental Design.The brand experiment was designed to evaluate how Claude, Gemini, ChatGPT, and Perplexity handle queries about well-known versus niche brands. The study aimed to capture not only the answers provided by each model but also the sources they referenced and the classification mix of those sources.

**中文**

当比较不同人工智能搜索引擎的结果时，他们如何优先考虑知名品牌和小众品牌的来源，出现了一个清晰的模式。在所有系统中，都一致强调挣得领域，但品牌、社交和挣得来源之间的平衡却存在显着差异。实验设计。品牌实验旨在评估 Claude、Gemini、ChatGPT 和 Perplexity 如何处理有关知名品牌和小众品牌的查询。该研究的目的不仅是捕获每个模型提供的答案，还包括它们引用的来源以及这些来源的分类组合。

### 段落 114 · Page 14

**EN**

Two query sets were created: one for well-known brands (established consumer names such as Apple, Nike, or Toyota) and another for niche brands (less familiar or specialized names). Each query was structured in a ranking or identification style, such as “What is the best-known camera brand?” or “Which niche fashion brands are gaining popularity?” All queries were run through each model, with each engine returning both an explicit answer and a set of supporting links. The experimental pipeline was implemented in Python with structured logging and reproducibility in mind. For each model: •Queries were submitted via its respective API.

**中文**

创建了两个查询集：一个针对知名品牌（已建立的消费者名称，例如苹果、耐克或丰田），另一个针对小众品牌（不太熟悉或专业的名称）。每个查询都以排名或识别方式构建，例如“最知名的相机品牌是什么？”或“哪些小众时尚品牌越来越受欢迎？”所有查询都通过每个模型运行，每个引擎都返回明确的答案和一组支持链接。实验管道是用 Python 实现的，考虑到结构化日志记录和可重复性。对于每个模型： • 查询是通过其各自的API 提交的。

### 段落 115 · Page 14

**EN**

• The links returned were collected and normalized by extracting the base domain. • A classification routine labeled each link as Brand, Earned, or Social, combining a predefined list of known social platforms with GPT-assisted classification prompts. • For answer-level comparison, a post-processing step cleaned the textual responses (removing punctuation and formatting) to allow direct string-level comparison. Agreement between models was measured as the percentage of queries where two models produced the same brand name answer. • For link-level comparison, the distribution of Brand, Earned, and Social domains was computed per query set.

**中文**

• 通过提取基本域来收集和标准化返回的链接。 • 分类例程将每个链接标记为“品牌”、“赢得”或“社交”，将已知社交平台的预定义列表与 GPT 辅助的分类提示相结合。 • 对于答案级别比较，后处理步骤清理了文本响应（删除标点符号和格式）以允许直接进行字符串级别比较。模型之间的一致性通过两个模型产生相同品牌名称答案的查询百分比来衡量。 • 对于链接级比较，按查询集计算品牌、赢得和社交域的分布。

### 段落 116 · Page 14

**EN**

Aggregated statistics were then calculated separately for well-known brands and niche brands, enabling direct comparison across engines. At the same time, domain frequency counts identified the most common sources (e.g., TechRadar, Wikipedia, Reddit). Finally, the system compiled results into JSON files containing: per-model classification distributions across the two query sets, agreement scores reflecting consistency in answers between models, and detailed logs capturing raw responses, domain classifications, and answer strings for auditing. Figure 21: Comparison of Claude vs. Gemini for well-known and niche brands.

**中文**

然后分别计算知名品牌和小众品牌的汇总统计数据，从而可以跨引擎进行直接比较。同时，域频率计数确定了最常见的来源（例如 TechRadar、维基百科、Reddit）。最后，系统将结果编译成 JSON 文件，其中包含：两个查询集的每个模型分类分布、反映模型之间答案一致性的一致性分数，以及捕获原始响应、域分类和用于审核的答案字符串的详细日志。图 21：Claude 与 Gemini 的知名品牌和小众品牌比较。

### 段落 117 · Page 14

**EN**

Well-Known Brands.For well-known brands, Claude and Chat- GPT displayed the strongest tilt toward Earned domains. Claude results consisted of 87.3% Earned, 6.8% Brand, and 5.9% Social, while ChatGPT skewed even further, with 93.5% Earned, 6.5% Brand, and no Social. Perplexity, by contrast, surfaced a greater proportion of Social content at 23.8%, with 67.4% Earned and 8.8% Brand. Gemini stood between these extremes, balancing 63.4% Earned, 25.1% Brand, and 11.5% Social.

**中文**

知名品牌。对于知名品牌，Claude 和 Chat-GPT 对赢得域名表现出最强的倾斜。 Claude 的结果包括 87.3% 的收益、6.8% 的品牌和 5.9% 的社交，而 ChatGPT 的偏差甚至更大，93.5% 的收益、6.5% 的品牌和无社交。相比之下，困惑在社交内容中所占比例更大，达到 23.8%，其中 67.4% 为赚取内容，8.8% 为品牌内容。双子座介于这两个极端之间，平衡了 63.4% 的收入、25.1% 的品牌和 11.5% 的社交。

### Page 15

### 段落 118 · Page 15

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA Figure 22: Comparison of GPT vs. Gemini for well-known and niche brands. Figure 23: Comparison of Perplexity vs. Gemini for wellknown and niche brands. Niche Brands.For niche brands, similar trends persisted, though the distributional differences became sharper. ChatGPT again leaned most heavily on Earned domains, with 95.1% Earned and only 4.9% Brand, completely excluding Social sources. Claude showed a slightly more balanced profile at 86.3% Earned, 10.6% Brand, and 3.2% Social.

**中文**

生成式引擎优化：如何主导人工智能搜索大会’17，2017 年 7 月，美国华盛顿特区 图 22：知名品牌和小众品牌的 GPT 与 Gemini 的比较。图 23：知名品牌和小众品牌的 Perplexity 与 Gemini 的比较。小众品牌。对于小众品牌来说，尽管分布差异变得更加明显，但类似的趋势仍然存在。 ChatGPT 再次最依赖于赢得域名，其中 95.1% 为赢得域名，只有 4.9% 为品牌，完全排除了社交来源。克劳德的形象稍微平衡一些，收入占 86.3%，品牌占 10.6%，社交占 3.2%。

### 段落 119 · Page 15

**EN**

Perplexity continued to surface a higher share of Social (17.5%) and Brand (9.1%), reducing Earned to 73.4%. Gemini again positioned itself closer to the middle with 66.4% Earned, 21.2% Brand, and 12.7% Social. Summary.These findings show that Claude and ChatGPT behave conservatively, strongly privileging expert-driven and third-party validation while minimizing user-generated sources. Perplexity behaves more inclusively, incorporating a substantial amount of Social content alongside Earned. Gemini adopts a hybrid strategy, with a greater share of Brand domains than Claude or ChatGPT and a moderate inclusion of Social.

**中文**

困惑继续在社交 (17.5%) 和品牌 (9.1%) 中占据较高份额，使收益减少至 73.4%。 Gemini 再次将自己定位在中间位置，收入为 66.4%，品牌为 21.2%，社交为 12.7%。摘要：这些研究结果表明，Claude 和 ChatGPT 表现保守，高度重视专家驱动和第三方验证，同时最大限度地减少用户生成的来源。 Perplexity 的表现更具包容性，将大量社交内容与 Earned 内容结合在一起。 Gemini 采用混合策略，比 Claude 或 ChatGPT 拥有更大的品牌领域份额，并适度包含社交领域。

### 段落 120 · Page 15

**EN**

The average agreement scores further highlight these differences. Across well-known brands, agreement ranged from 76–81% depending on the system pairing, while for niche brands it was slightly lower, between 71–76%. This suggests that AI systems align more closely when handling established, widely recognized brands but diverge when surfacing results for less familiar or specialized entities. 5.2.2 Vertical Domain and Freshness Analysis.This section evaluates how Claude, ChatGPT, and Perplexity source information across two high-interest verticals: consumer electronics and automotive.

**中文**

平均一致性分数进一步凸显了这些差异。在知名品牌中，一致性范围为 76-81%，具体取决于系统配对，而对于小众品牌，一致性程度略低，在 71-76% 之间。这表明人工智能系统在处理已建立的、广泛认可的品牌时会更加一致，但在为不太熟悉或专业的实体提供结果时会出现分歧。 5.2.2 垂直领域和新鲜度分析。本节评估 Claude、ChatGPT 和 Perplexity 如何在消费电子和汽车这两个高兴趣垂直领域获取信息。

### 段落 121 · Page 15

**EN**

This analysis considers both domain concentration (the top sources of content) and freshness (measured by publication dates). Experimental Design.This experiment evaluated Claude, Chat- GPT, and Perplexity on two high-interest verticals: consumer electronics and automotive. The focus was on both domain concentration (the sources each engine prioritized) and freshness (the age of content returned). The study began with a curated set of ranking-style queries drawn from consumer electronics and automotive topics. Each query was submitted in parallel to Claude, ChatGPT, and Perplexity, with each engine returning up to ten links.

**中文**

该分析考虑了领域集中度（内容的主要来源）和新鲜度（按发布日期衡量）。实验设计。该实验评估了 Claude、Chat-GPT 和 Perplexity 在两个高兴趣垂直领域的表现：消费电子产品和汽车。重点是领域集中度（每个引擎优先考虑的来源）和新鲜度（返回内容的年龄）。该研究从消费电子和汽车主题中抽取的一组精心设计的排名式查询开始。每个查询均并行提交给 Claude、ChatGPT 和 Perplexity，每个引擎最多返回 10 个链接。

### 段落 122 · Page 15

**EN**

All retrieved URLs were normalized by extracting domain names for consistent comparison. Each link was classified into one of three categories:Brand, Earned, orSocial. Brand sources included manufacturer and retailer domains such as apple.com or toyota.com. Earned sources covered third-party review sites, media outlets, and government portals such as techradar.com or consumerreports.org. Social sources captured community-driven or user-generated platforms like Reddit, YouTube, and Quora. Classification was conducted by combining a fixed rule list of known social domains with AI-assisted labeling prompts.

**中文**

所有检索到的 URL 均通过提取域名进行标准化，以进行一致比较。每个链接都分为三个类别之一：品牌、赢得或社交。品牌来源包括制造商和零售商域，例如 apple.com 或 toyota.com。获得的来源涵盖第三方评论网站、媒体机构和政府门户网站，例如 techradar.com 或 Consumerreports.org。社交来源捕获了社区驱动或用户生成的平台，例如 Reddit、YouTube 和 Quora。分类是通过将已知社交领域的固定规则列表与人工智能辅助标签提示相结合来进行的。

### 段落 123 · Page 15

**EN**

To assess freshness, each returned link was crawled and analyzed for publication or update dates. Candidate dates were extracted from HTML metadata, JSON-LD scripts, <time> tags, and body text. When multiple candidates were found, GPT was used to select the most plausible publication date. Extracted dates were then converted to UTC timestamps. For each link, article age was calculated in days relative to the time of the experiment. Freshness was summarized using several measures: •Coverage:the proportion of links with identifiable dates. • Mean and median age:average and typical number of days since publication.

**中文**

为了评估新鲜度，对每个返回的链接进行爬网并分析发布或更新日期。候选日期是从 HTML 元数据、JSON-LD 脚本、<time> 标签和正文文本中提取的。当找到多个候选者时，GPT 用于选择最合理的发布日期。然后提取的日期被转换为 UTC 时间戳。对于每个链接，文章年龄以相对于实验时间的天数计算。新鲜度通过以下几个指标进行总结： • 覆盖率：具有可识别日期的链接的比例。 • 平均年龄和中位年龄：自发布以来的平均天数和典型天数。

### 段落 124 · Page 15

**EN**

• Freshness score:a recency-weighted measure computed as the mean of1/(1+age). • Coverage-adjusted freshness score:the freshness score scaled by coverage to penalize engines with low date detection. At the aggregation stage, results were summarized along two dimensions. First, domain concentration was measured by counting the most frequent domains surfaced per vertical and engine. Second, classification mix was computed as the percentage share of Brand, Earned, and Social links. The freshness results were then combined with classification results to compare recency alongside content diversity.

**中文**

• 新鲜度得分：新近度加权度量，计算为1/(1+年龄) 的平均值。 • 覆盖率调整的新鲜度分数：根据覆盖率缩放的新鲜度分数，以惩罚低日期检测的引擎。在聚合阶段，结果沿着两个维度进行总结。首先，通过计算每个垂直领域和引擎出现的最频繁的域来测量域集中度。其次，分类组合计算为品牌、赢得和社交链接的百分比份额。然后将新鲜度结果与分类结果相结合，以比较新近度和内容多样性。

### 段落 125 · Page 15

**EN**

Consumer Electronics.In consumer electronics, Claude and GPT exhibited strong reliance on Earned media (Claude: ≈93.7%, GPT: ≈93.6%), with very limited Brand and Social representation. Claude’s top domains included TechRadar, Tom’s Guide, and RTINGS, while GPT leaned on TechRadar, Tom’s Guide, and Wikipedia. Both engines foreground traditional editorial and review outlets, reinforcing their Earned-heavy bias.

**中文**

消费电子产品。在消费电子产品中，Claude 和 GPT 表现出对免费媒体的强烈依赖（Claude：约 93.7%，GPT：约 93.6%），品牌和社交代表性非常有限。 Claude 的顶级域名包括 TechRadar、Tom’s Guide 和 RTINGS，而 GPT 则依赖 TechRadar、Tom’s Guide 和 Wikipedia。这两个引擎都以传统的社论和评论媒体为前景，强化了他们的“挣钱”偏见。

### Page 16

### 段落 126 · Page 16

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas Figure 24: Distribution of article age (days) across verticals by search engine. Figure 25: Domain classification shares (Brand, Earned, Social) across verticals and engines. By contrast, Perplexity drew from a more heterogeneous mix: ≈31.6% Brand, 53.3% Earned, and 15.1% Social. Notably, YouTube (Social) and BestBuy.com (Brand) were dominant sources alongside editorial sites like RTINGS and CNET. This produced greater exposure to retail-driven and user-generated perspectives absent from Claude and GPT.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 图 24：按搜索引擎划分的垂直行业文章年龄（天数）分布。图 25：跨垂直行业和引擎的领域分类份额（品牌、赢得、社交）。相比之下，Perplexity 则来自更多样化的组合：约 31.6% 为品牌，53.3% 为赚取，15.1% 为社交。值得注意的是，YouTube（社交）和 BestBuy.com（品牌）与 RTINGS 和 CNET 等编辑网站一起成为主要来源。这使得人们更多地接触到 Claude 和 GPT 所没有的零售驱动和用户生成的观点。

### 段落 127 · Page 16

**EN**

On freshness, coverage was high in this vertical (Claude: 92.5% dated links). Claude’s mean article age was about 117 days, with a median of 62 days, yielding a freshness score of 0.0617 (coverageadjusted: 0.0571). GPT exhibited similar freshness patterns, while Perplexity produced somewhat newer but less consistently dated results. Overall, Claude and GPT ensured stable exposure to midterm reviews, while Perplexity blended in more contemporary but commercially linked material. Automotive.The automotive vertical showed greater divergence. Claude and GPT again prioritized Earned content: Claude at≈81.6% and GPT at ≈82.9%.

**中文**

就新鲜度而言，该垂直领域的覆盖率很高（克劳德：92.5% 的日期链接）。 Claude 的平均文章年龄约为 117 天，中位数为 62 天，新鲜度得分为 0.0617（覆盖率调整后：0.0571）。 GPT 表现出类似的新鲜度模式，而 Perplexity 则产生了一些更新但日期不太一致的结果。总体而言，Claude 和 GPT 确保了中期审查的稳定曝光，而 Perplexity 则融入了更现代但与商业相关的材料。汽车行业。汽车行业表现出更大的差异。 Claude 和 GPT 再次优先考虑获得内容：Claude 约为 81.6%，GPT 约为 82.9%。

### 段落 128 · Page 16

**EN**

Claude favored Consumer Reports, Car and Driver, and US News, while GPT mixed Wikipedia, Automoblog, and news outlets like AP. Both leaned toward expert-oriented reviews and rankings, with limited Brand visibility (about 17–18%). Perplexity, however, surfaced a notably different mix: ≈34.6% Brand, 55.5% Earned, and 9.9% Social. YouTube emerged as its single most frequent source, alongside Car and Driver and Consumer Reports. Importantly, Perplexity also introduced retailerand aftermarket-linked domains (e.g., autozone.com, cars.com), yielding more diverse but also more commercial outputs compared to Claude and GPT.

**中文**

克劳德喜欢《消费者报告》、《汽车与驾驶员》和《美国新闻》，而 GPT 则喜欢维基百科、汽车博客和美联社等新闻媒体。两者都倾向于以专家为导向的评论和排名，品牌知名度有限（约 17-18%）。然而，困惑度却呈现出明显不同的组合：约 34.6% 为品牌，55.5% 为赚取，9.9% 为社交。 YouTube 与汽车、驾驶员和消费者报告一起成为其最常见的来源。重要的是，Perplexity 还引入了与零售商和售后市场相关的域名（例如 autozone.com、cars.com），与 Claude 和 GPT 相比，产生了更多样化、更商业化的产出。

### 段落 129 · Page 16

**EN**

Freshness results highlighted systemic gaps. Claude’s automotive links had low coverage (≈61%) and were substantially older, with a mean age of about 331 days (median 148 days). Its freshness score fell to 0.0441 (coverage-adjusted: 0.0269), indicating reliance on longstanding reviews and static ranking pages. GPT showed similar tendencies. Perplexity, while not entirely eliminating this age bias, returned more Social and retail-driven content that was incrementally fresher. Comparative Observations.

**中文**

新鲜度结果凸显了系统性差距。 Claude 的汽车链路覆盖率较低（约 61%），并且历史较长，平均年龄约为 331 天（中位数 148 天）。其新鲜度得分降至 0.0441（覆盖率调整后：0.0269），表明对长期评论和静态排名页面的依赖。 GPT 也表现出类似的趋势。 《困惑》虽然没有完全消除这种年龄偏见，但返回了更多社交和零售驱动的内容，这些内容越来越新鲜。比较观察。

### 段落 130 · Page 16

**EN**

• Domain diversity:Across both verticals, Claude and GPT converged on authoritative review and editorial outlets, maximizing Earned exposure but suppressing Social. Perplexity consistently incorporated a broader ecosystem, balancing Earned with significant Brand and Social sources. • Freshness:Coverage of dated links was higher in consumer electronics than in automotive. Claude and GPT’s outputs in automotive lagged substantially in recency, while Perplexity injected more up-to-date but commercially linked results.

**中文**

• 领域多样性：在两个垂直领域，Claude 和 GPT 都集中在权威评论和社论渠道上，最大限度地提高曝光率，但抑制社交媒体。 Perplexity 始终融入更广泛的生态系统，平衡收益与重要的品牌和社交资源。 • 新鲜度：消费电子产品中过时链接的覆盖率高于汽车领域。 Claude 和 GPT 在汽车领域的产出在近期内大幅落后，而 Perplexity 则注入了更多最新但与商业相关的结果。

### 段落 131 · Page 16

**EN**

• Vertical sensitivity:The automotive vertical amplified the contrasts: while consumer electronics outputs were relatively fresh and homogenous, automotive responses revealed aging content pools for Claude and GPT versus hybridized mixes for Perplexity. Summary.This vertical analysis underscores that while Claude and GPT prioritize consistency, authority, and Earned concentration, they risk staleness, especially in automotive contexts. Perplexity, by contrast, trades some editorial authority for greater diversity and timeliness, leveraging Brand and Social domains more extensively.

**中文**

• 垂直敏感性：汽车垂直领域放大了对比：虽然消费电子产品输出相对新鲜且同质，但汽车行业的反应揭示了 Claude 和 GPT 的老化内容池与 Perplexity 的混合内容。摘要：这种垂直分析强调，虽然 Claude 和 GPT 优先考虑一致性、权威性和赢得集中度，但他们面临着陈旧的风险，尤其是在汽车领域。相比之下，《困惑》用一些编辑权威来换取更大的多样性和及时性，更广泛地利用品牌和社交领域。

### 段落 132 · Page 16

**EN**

These findings highlight how vertical context modulates the trade-off between reliability, freshness, and media diversity across AI search engines. 5.2.3 Car Brands: Electric, Family SUVs, and Hybrid.This experiment focused on the automotive sector, comparing how Google, ChatGPT, and Perplexity sourced information on three topics: electric cars, family SUVs, and hybrids. Each query was categorized by topic and analyzed according to the share of Brand, Earned, and Social domains. In addition, the ten most frequently appearing domains per service and topic were examined to reveal differences in source composition.

**中文**

这些发现强调了垂直上下文如何调节人工智能搜索引擎的可靠性、新鲜度和媒体多样性之间的权衡。 5.2.3 汽车品牌：电动、家庭 SUV 和混合动力。本实验主要针对汽车领域，比较了 Google、ChatGPT 和 Perplexity 如何获取有关电动汽车、家庭 SUV 和混合动力这三个主题的信息。每个查询均按主题分类，并根据品牌、赢得和社交领域的份额进行分析。此外，还检查了每个服务和主题的十个最常出现的域，以揭示源组成的差异。

### 段落 133 · Page 16

**EN**

Experimental Design.To conduct the comparison across Google, ChatGPT, and Perplexity for automotive queries, a structured pipeline was developed. The experiment was designed around three themes: electric cars, family SUVs, and hybrid cars. Each theme contained a set of buyer-oriented queries (for example, “best electric car for commuting” or “top hybrid SUVs for families”), and each query was submitted to all three services. For every query, the top ten links returned were collected. The pipeline was implemented in Python with modular functions to ensure reproducibility.

**中文**

实验设计。为了对 Google、ChatGPT 和 Perplexity 之间的汽车查询进行比较，开发了一个结构化管道。该实验围绕三个主题设计：电动汽车、家庭SUV和混合动力汽车。每个主题都包含一组面向买家的查询（例如，“最佳通勤电动汽车”或“适合家庭的顶级混合动力 SUV”），每个查询都会提交给所有三个服务。对于每个查询，都会收集返回的前十个链接。该管道是用 Python 实现的，具有模块化功能，以确保可重复性。

### 段落 134 · Page 16

**EN**

Separate API clients were initialized for each service: Google Custom Search, OpenAI’s ChatGPT with web search enabled, and Perplexity’s API. Each query was executed in

**中文**

为每项服务初始化了单独的 API 客户端：Google 自定义搜索、启用网络搜索的 OpenAI 的 ChatGPT 以及 Perplexity 的 API。每个查询都执行在

### Page 17

### 段落 135 · Page 17

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA parallel across services with retry logic to handle timeouts or rate limits. All retrieved URLs were standardized by extracting their domain names. Every link was classified into one of three categories:Brand, Earned, orSocial. Brand referred to official manufacturer or retailer websites (for example, ford.com). Earned covered independent review sites, media outlets, or government portals (for example, caranddriver.com, energy.gov). Social included communitydriven or user-generated platforms such as Reddit, Quora, YouTube, or Facebook.

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区，跨服务并行，具有重试逻辑来处理超时或速率限制。所有检索到的 URL 均通过提取域名进行标准化。每个链接都分为三个类别之一：品牌、赢得或社交。品牌指的是官方制造商或零售商网站（例如 ford.com）。获得覆盖的独立评论网站、媒体机构或政府门户网站（例如 caranddriver.com、energy.gov）。社交包括社区驱动或用户生成的平台，例如 Reddit、Quora、YouTube 或 Facebook。

### 段落 136 · Page 17

**EN**

Classification combined a rule-based list of known social platforms with AI-assisted verification to ensure accuracy. The results were aggregated at two levels. First, domain-level counts captured how often specific domains appeared per service and topic. Second, classification-level shares summarized the overall media mix of Brand, Earned, and Social for each service and topic. A detailed log of all queries and links was also stored to support auditability. Finally, per-topic summaries and overall comparisons were compiled into JSON outputs.

**中文**

分类将基于规则的已知社交平台列表与人工智能辅助验证相结合，以确保准确性。结果在两个层面上进行汇总。首先，域级计数捕获了每个服务和主题特定域出现的频率。其次，分类级别的份额总结了每个服务和主题的品牌、赢得和社交的整体媒体组合。还存储所有查询和链接的详细日志以支持可审计性。最后，每个主题的摘要和总体比较被编译成 JSON 输出。

### 段落 137 · Page 17

**EN**

These included ranked domain lists, perservice category shares, and detailed logs of link classifications. This design allowed both quantitative comparison (percentages of Brand, Earned, and Social) and qualitative interpretation (the prominence of specific domains such as Reddit, Wikipedia, or Car and Driver). Figure 26: Domain composition (Brand, Earned, Social) across Google, ChatGPT, and Perplexity for electric cars, family SUVs, and hybrid cars. Electric Cars.For electric cars, Google balanced its results across Earned (56%), Brand (26%), and Social (18%).

**中文**

其中包括排名的域列表、每个服务类别份额以及链接分类的详细日志。这种设计既可以进行定量比较（品牌、赢得和社交的百分比），也可以进行定性解释（特定领域的突出程度，例如 Reddit、维基百科或汽车和驾驶员）。图 26：Google、ChatGPT 和 Perplexity 中电动汽车、家庭 SUV 和混合动力汽车的领域构成（品牌、收益、社交）。电动汽车。对于电动汽车，Google 在盈利 (56%)、品牌 (26%) 和社交 (18%) 方面平衡了其结果。

### 段落 138 · Page 17

**EN**

ChatGPT diverged by heavily prioritizing Earned sources (80%) with minimal Brand (19%) and negligible Social (under 1%). Perplexity fell between the two, with 67% Earned, 29% Brand, and 4% Social. Domain-level data highlights these contrasts. Google’s top electric car sources included Reddit, Quora, and Facebook alongside Earned outlets like Car and Driver and government portals such as energy.gov. ChatGPT concentrated on encyclopedic and news publishers such as Wikipedia, AP News, and Reuters, with limited inclusion of automotive review sites.

**中文**

ChatGPT 的分歧在于，严重优先考虑赚取来源 (80%)，而品牌 (19%) 极少，社交来源可忽略不计 (低于 1%)。困惑度介于两者之间，其中 67% 为赚取类，29% 为品牌类，4% 为社交类。领域级数据突出了这些对比。谷歌的主要电动汽车来源包括 Reddit、Quora 和 Facebook，以及 Car 和 Driver 等 Earned 网站以及 energy.gov 等政府门户网站。 ChatGPT 专注于百科全书和新闻出版商，例如维基百科、美联社新闻和路透社，仅包含有限的汽车评论网站。

### 段落 139 · Page 17

**EN**

Perplexity relied on YouTube and Car and Driver while supplementing with government and consumeroriented review domains. Family SUVs.The family SUV segment showed sharper differences. Google leaned toward Social sources, with Reddit dominating its domain list, resulting in 23% Social, 31% Brand, and 46% Earned. ChatGPT, by contrast, excluded Social entirely and emphasized Earned domains at 81%, with 19% Brand. Perplexity presented a more balanced profile: 58% Earned, 32% Brand, and 9% Social. Domain counts underline these differences. Google’s results were led by Reddit, Quora, and Facebook, but also included U.S. News and KBB.com.

**中文**

Perplexity 依赖 YouTube 和 Car and Driver，同时补充政府和消费者导向的评论领域。家庭SUV。家庭SUV细分市场差异更为明显。谷歌倾向于社交资源，Reddit 在其域名列表中占据主导地位，社交资源占 23%，品牌资源占 31%，收益资源占 46%。相比之下，ChatGPT 完全排除了社交，并强调赢得域名（81%），其中品牌占 19%。 Perplexity 的情况更加平衡：58% 是赚取性的，32% 是品牌性的，9% 是社交性的。域名数量凸显了这些差异。谷歌的调查结果以 Reddit、Quora 和 Facebook 领先，但也包括《美国新闻》和 KBB.com。

### 段落 140 · Page 17

**EN**

ChatGPT relied on structured outlets such as Wikipedia, AP News, and review sites like ISeeCars and Cars.com. Perplexity’s mix included YouTube for Social, alongside Car and Driver, Edmunds, Consumer Reports, andCars.com. Hybrid Cars.For hybrids, Google’s results resembled its SUV pattern: 56% Earned, 24% Brand, and 20% Social. Reddit again played a central role, supported by Quora, Facebook, and research-oriented sites such as ScienceDirect. ChatGPT continued its systematic exclusion of Social, yielding 77% Earned and 23% Brand.

**中文**

ChatGPT 依赖于维基百科、美联社新闻等结构化渠道以及 ISeeCars 和 Cars.com 等评论网站。 Perplexity 的组合包括 YouTube for Social、Car and Driver、Edmunds、Consumer Reports 和 Cars.com。混合动力汽车。对于混合动力汽车，谷歌的结果类似于其 SUV 模式：56% 是盈利型汽车，24% 是品牌型汽车，20% 是社交型汽车。在 Quora、Facebook 和 ScienceDirect 等研究型网站的支持下，Reddit 再次发挥了核心作用。 ChatGPT 继续系统性地排除社交，获得了 77% 的收益和 23% 的品牌。

### 段落 141 · Page 17

**EN**

Notably, it leaned more toward industry-specific outlets like TopSpeed, Reuters, and AutomotiveQuest, as well as Wikipedia. Perplexity produced 62% Earned, 34% Brand, and 5% Social, with Car and Driver, YouTube, andEnergy.govamong its top sources. Cross-Topic Observations.Three trends stand out across these automotive categories. First, Google consistently incorporates a high proportion of Social sources, especially Reddit, which makes its results community-driven but less curated.

**中文**

值得注意的是，它更倾向于特定行业的媒体，如 TopSpeed、Reuters、AutomotiveQuest 以及维基百科。 Perplexity 产生了 62% 的收益、34% 的品牌和 5% 的社交，其中 Car and Driver、YouTube 和 Energy.gov 是其主要来源。跨主题观察。这些汽车类别中存在三个突出的趋势。首先，谷歌始终整合大量社交资源，尤其是 Reddit，这使得其结果由社区驱动，但缺乏精心策划。

### 段落 142 · Page 17

**EN**

Second, ChatGPT almost entirely excludes Social platforms, resulting in outputs that are dominated by institutional and journalistic Earned domains, with Brand sources playing a secondary role. Third, Perplexity consistently bridges the two approaches: it includes some Social content (often YouTube), supplements with Brand domains, and maintains a majority share of Earned content.

**中文**

其次，ChatGPT 几乎完全排除了社交平台，导致产出以机构和新闻领域为主，而品牌来源则扮演次要角色。第三，Perplexity 始终弥合了这两种方法：它包括一些社交内容（通常是 YouTube）、品牌域的补充，并保持赚取内容的大部分份额。

### 段落 143 · Page 17

**EN**

These distinctions illustrate that the services are not only ranking different links but also constructing fundamentally different knowledge environments—Google privileging community discussion, ChatGPT privileging authoritative sources, and Perplexity blending the two. 5.2.4 Cross-Model Domain Diversity.This section examines how Claude, ChatGPT, and Perplexity differ in the diversity of domains they source across two verticals: automotive and consumer electronics. The analysis considers the breadth of distinct domains, the degree of overlap between models (using Jaccard similarity), and the share of domains exclusive to each service.

**中文**

这些区别表明，这些服务不仅对不同的链接进行排名，而且还构建了根本不同的知识环境——Google 赋予社区讨论特权，ChatGPT 赋予权威来源特权，而 Perplexity 则将两者融合在一起。 5.2.4 跨模型领域多样性。本节研究 Claude、ChatGPT 和 Perplexity 在汽车和消费电子这两个垂直领域来源的领域多样性方面有何不同。该分析考虑了不同领域的广度、模型之间的重叠程度（使用 Jaccard 相似度）以及每个服务独有的领域的份额。

### 段落 144 · Page 17

**EN**

Experimental Design.The domain diversity experiment was designed to evaluate how Claude, ChatGPT, and Perplexity source information when given the same set of queries in two verticals:

**中文**

实验设计。域多样性实验旨在评估 Claude、ChatGPT 和 Perplexity 在两个垂直领域给出相同的查询集时如何获取信息：

### Page 18

### 段落 145 · Page 18

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas automotive and consumer electronics. The study aimed to quantify not only the breadth of domains each model returned but also the degree of overlap across engines, using normalized measures of similarity and exclusivity. Two query sets were created, one for automotive and one for consumer electronics, each consisting of ranking-style and productdiscovery prompts. For example, automotive queries included themes such as “What are the best family SUVs in 2024?” while consumer electronics queries included “Rank the best smartphones from 1 to 10.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 汽车和消费电子产品。该研究旨在使用标准化的相似性和排他性度量，不仅量化每个模型返回的领域的广度，还量化引擎之间的重叠程度。创建了两个查询集，一组用于汽车，一组用于消费电子产品，每个查询集都包含排名样式和产品发现提示。例如，汽车查询包括“2024 年最好的家庭 SUV 是什么？”等主题。消费电子产品查询包括“对最好的智能手机进行排名，从 1 到 10。

### 段落 146 · Page 18

**EN**

” Each query was run independently through all three engines, with each model returning up to ten links. The experimental pipeline was implemented in Python with structured logging and reproducibility in mind. For each model: • Queries were submitted via its respective API (Claude via Anthropic, ChatGPT via OpenAI, and Perplexity via its public API). • All links were collected and normalized to their registered base domains usingtldextract. • Distinct domain sets were constructed per engine, allowing direct comparison of coverage and overlap.

**中文**

“每个查询都通过所有三个引擎独立运行，每个模型最多返回 10 个链接。实验管道是在 Python 中实现的，考虑到结构化日志记录和可重复性。对于每个模型： • 通过其各自的 API 提交查询（Claude 通过 Anthropic、ChatGPT 通过 OpenAI、Perplexity 通过其公共 API）。 • 使用 tldextract 收集所有链接并标准化为其注册的基域。 • 每个引擎构建不同的域集，允许直接比较覆盖范围和重叠。

### 段落 147 · Page 18

**EN**

To assess diversity, several measures were calculated: • Set sizes: the total number of distinct domains returned by each model in a vertical. • Jaccard similarity: pairwise normalized overlap between models’ domain sets. • Unique share: the proportion of domains that appeared exclusively in one model’s outputs. • Domain partitions: grouping domains into categories such as Claude-only, GPT-only, Perplexity-only, shared between two engines, or shared across all three. Visualizations were produced in the form of bar charts, where each x-axis category represented unique, pairwise, or three-way shared domains.

**中文**

为了评估多样性，计算了几个度量： • 集大小：垂直方向上每个模型返回的不同域的总数。 • Jaccard 相似性：模型域集之间的成对归一化重叠。 • 独特份额：仅出现在一个模型输出中的域的比例。 • 域分区：将域分为若干类别，例如仅Claude、仅GPT、仅Perplexity、在两个引擎之间共享或在所有三个引擎之间共享。可视化以条形图的形式生成，其中每个 x 轴类别代表唯一、成对或三向共享域。

### 段落 148 · Page 18

**EN**

This enabled direct comparison of how concentrated or fragmented the domain ecosystem was across engines. Figure 27: Domain diversity for consumer electronics across Claude, ChatGPT, and Perplexity. Automotive.In the automotive vertical, Claude surfaced 350 distinct domains, GPT returned 212, and Perplexity 347. Pairwise Jaccard overlaps were modest: Claude–GPT at 0.147, Claude–Perplexity at 0.251, and GPT–Perplexity at 0.096. The unique domain percentages further underscore divergence, with Claude contributing 50.3% Figure 28: Domain diversity for automotive across Claude, ChatGPT, and Perplexity.

**中文**

这使得可以直接比较域生态系统跨引擎的集中或分散程度。图 27：Claude、ChatGPT 和 Perplexity 的消费电子产品领域多样性。汽车。在汽车垂直领域，Claude 出现了 350 个不同的领域，GPT 返回了 212 个，Perplexity 为 347 个。成对 Jaccard 重叠程度不大：Claude-GPT 为 0.147，Claude-Perplexity 为 0.251，GPT-Perplexity 为 0.096。独特的领域百分比进一步凸显了差异，Claude 贡献了 50.3% 图 28：Claude、ChatGPT 和 Perplexity 的汽车领域多样性。

### 段落 149 · Page 18

**EN**

exclusive domains, GPT 60.8%, and Perplexity 56.5%. These results show that each model contributes a substantial volume of unique sources, with Claude and Perplexity sharing the most common ground, while GPT and Perplexity show minimal intersection. The set of domains shared across all three was relatively small, dominated by well-established review and ranking outlets such asCar and Driver,Edmunds, andConsumer Reports. Consumer Electronics.The consumer electronics vertical revealed similar but even sharper contrasts. Claude produced 242 distinct domains, GPT 179, and Perplexity 268.

**中文**

独家域名，GPT 60.8%，Perplexity 56.5%。这些结果表明，每个模型都贡献了大量独特的来源，其中 Claude 和 Perplexity 具有最共同的基础，而 GPT 和 Perplexity 则显示出最小的交叉点。这三个领域共享的领域相对较小，主要由成熟的评论和排名机构主导，例如《Car and Driver》、《Edmunds》和《Consumer Reports》。消费电子产品。消费电子产品垂直领域也呈现出类似但甚至更鲜明的对比。 Claude 生成了 242 个不同的域，其中 GPT 179 和 Perplexity 268。

### 段落 150 · Page 18

**EN**

Overlaps were smaller than in automotive: Claude–GPT at 0.150, Claude–Perplexity at 0.200, and GPT–Perplexity at only 0.088. Exclusivity was even more pronounced: Claude domains were 55.8% unique, GPT 67.6%, and Perplexity 67.2%. Once again, the intersection across all three models was minimal, including only a narrow set of core publishers such asTechRadar,Tom’s Guide, andRTINGS. Comparative Observations.Three trends emerge from this crossmodel diversity analysis. First, each model maintains a wide footprint of exclusive sources, indicating that system choice directly shapes the information ecosystem a user encounters.

**中文**

重叠度小于汽车领域：Claude-GPT 为 0.150，Claude-Perplexity 为 0.200，而 GPT-Perplexity 仅为 0.088。排他性甚至更加明显：Claude 域的唯一性为 55.8%，GPT 为 67.6%，Perplexity 为 67.2%。再次强调，这三种模式之间的交叉点很小，只包括一小部分核心出版商，例如 TechRadar、Tom’s Guide 和 RTINGS。比较观察。这种跨模型多样性分析出现了三个趋势。首先，每个模型都保留了广泛的独家资源，这表明系统选择直接塑造了用户遇到的信息生态系统。

### 段落 151 · Page 18

**EN**

Second, overlaps between Claude and Perplexity are consistently stronger than between GPT and Perplexity, suggesting Claude and Perplexity converge more in their domain pools. Third, across both verticals, only a small "core" set of high-authority sites (notably large review and media outlets) appear universally, while the majority of domains remain siloed by model. 5.2.5 Cross-Model Domain Diversity in Local Services. Objective.While prior experiments (§5.3) examined verticals such as automotive and consumer electronics, here we extend the analysis tolocal service categories.

**中文**

其次，Claude 和 Perplexity 之间的重叠始终强于 GPT 和 Perplexity 之间的重叠，这表明 Claude 和 Perplexity 在其域池中更加趋同。第三，在这两个垂直领域中，只有一小部分“核心”高权威网站（特别是大型评论和媒体机构）普遍出现，而大多数领域仍然受到模型的孤立。 5.2.5 本地服务的跨模型域多样性。目标：虽然之前的实验（第 5.3 节）研究了汽车和消费电子产品等垂直行业，但在这里我们将分析扩展到本地服务类别。

### 段落 152 · Page 18

**EN**

The goal is to evaluate how four major AI search engines (Claude, Gemini, GPT, Perplexity) differ in the breadth and overlap of domains when responding to queries in three representative sectors: Auto Repair, Dentists, and Moving Companies. Experimental Design.Using the pipeline described in §4.1, we generated 100 ranking-style queries per category (e.g., “best auto repair shops in Toronto” or “top-rated dentists in Toronto”). Each

**中文**

目标是评估四个主要人工智能搜索引擎（Claude、Gemini、GPT、Perplexity）在响应三个代表性行业（汽车维修、牙医和搬家公司）的查询时，在领域广度和重叠方面有何不同。实验设计。使用第 4.1 节中描述的管道，我们为每个类别生成 100 个排名式查询（例如，“多伦多最好的汽车修理店”或“多伦多顶级牙医”）。每个

### Page 19

### 段落 153 · Page 19

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA query was submitted in parallel to Claude, Gemini, GPT, and Perplexity, each returning up to ten links. URLs were normalized to base domains, and set-level statistics were computed, including: •Set size:total number of distinct domains per engine. •Jaccard similarity:pairwise overlap between engines. • Unique share:proportion of domains exclusive to a given engine. • Partition counts:number of domains appearing in one, two, three, or all four systems.

**中文**

生成式引擎优化：如何主导人工智能搜索大会’17，2017 年 7 月，美国华盛顿特区 查询与 Claude、Gemini、GPT 和 Perplexity 并行提交，每个查询最多返回 10 个链接。 URL 被标准化为基本域，并计算集合级别的统计数据，包括： •集合大小：每个引擎的不同域的总数。 •杰卡德相似性：引擎之间的成对重叠。 • 唯一份额：特定引擎独占的域比例。 • 分区计数：出现在一个、两个、三个或全部四个系统中的域数量。

### 段落 154 · Page 19

**EN**

Figure 29: Domain diversity for Auto Repair queries across Claude, Gemini, GPT, and Perplexity. Figure 30: Domain diversity for Dentist queries across Claude, Gemini, GPT, and Perplexity. Results.InAuto Repair, Gemini (98) and Perplexity (117) surfaced the largest number of distinct domains, while Claude (51) and GPT (53) returned smaller sets. Pairwise overlaps were modest, with Jaccard scores around 0.15–0.25. Unique contributions were substantial: Claude 35%, Gemini 55%, GPT 62%, and Perplexity 63%. InDentists, Gemini again led with 151 domains, followed by Perplexity (138), Claude (64), and GPT (51).

**中文**

图 29：Claude、Gemini、GPT 和 Perplexity 中自动修复查询的域多样性。图 30：Claude、Gemini、GPT 和 Perplexity 中 Dentist 查询的域多样性。结果：在 Auto Repair 中，Gemini (98) 和 Perplexity (117) 出现了最大数量的不同域，而 Claude (51) 和 GPT (53) 返回了较小的集合。成对重叠程度较低，Jaccard 得分约为 0.15-0.25。独特的贡献是巨大的：Claude 35%、Gemini 55%、GPT 62% 和 Perplexity 63%。在《Dentists》中，Gemini 再次以 151 个域名领先，其次是 Perplexity（138）、Claude（64）和 GPT（51）。

### 段落 155 · Page 19

**EN**

Jaccard overlaps were slightly higher here, with Gemini–Perplexity showing the strongest intersection at 0.23. Exclusivity remained high: Claude 40%, Gemini 54%, GPT 68%, Perplexity 54%. ForMoving Companies, Gemini produced 108 domains, Perplexity 62, GPT 61, and Claude 39. Gemini–Perplexity overlap was strongest at 0.25, but GPT remained the most exclusive with 61% Figure 31: Domain diversity for Moving Company queries across Claude, Gemini, GPT, and Perplexity. unique domains. Claude produced 51% unique, while Perplexity contributed 45%.

**中文**

Jaccard 重叠度在这里略高，Gemini-Perplexity 显示出最强的交集，为 0.23。排他性仍然很高：克劳德 40%，双子座 54%，GPT 68%，困惑 54%。对于Moving Companies，Gemini 生成了 108 个域，Perplexity 62、GPT 61 和 Claude 39。Gemini-Perplexity 重叠最强，为 0.25，但 GPT 仍然是最独特的，占 61% 图 31：Claude、Gemini、GPT 和 Perplexity 之间的 Moving Company 查询的域多样性。独特的领域。 Claude 产生了 51% 的独特性，而 Perplexity 则贡献了 45%。

### 段落 156 · Page 19

**EN**

Across all three categories, only a handful of domains (such as large review aggregators like homestars.com and opencare.com) appeared across all four systems. Summary.These findings reinforce that local service queries yield highly fragmented ecosystems across AI engines. While Claude and GPT rely on narrower, more conservative sets of sources, Gemini and Perplexity explore a broader range of domains, with limited consensus across systems.

**中文**

在所有三个类别中，只有少数域（例如 homestars.com 和 opencare.com 等大型评论聚合器）出现在所有四个系统中。摘要：这些发现强化了本地服务查询在人工智能引擎中产生高度分散的生态系统。 Claude 和 GPT 依赖于更狭窄、更保守的来源，而 Gemini 和 Perplexity 则探索更广泛的领域，但跨系统的共识有限。

### 段落 157 · Page 19

**EN**

This divergence underscores the importance of engine choice in shaping user exposure to local businesses, particularly in fragmented markets where authoritative sources are scarce and directory-style or aggregator sites dominate. 5.2.6 Big Brand Bias (Cola Vertical). Objective.This experiment examines whether generative AI systems exhibit a systematic preference for major soda brands over niche/indie brands when queries are unbranded. Concretely, we ask if model outputs disproportionately surface global leaders (e.g., Coca-Cola, Pepsi) relative to smaller craft or regional brands, and whether this bias is consistent across models.

**中文**

这种差异强调了引擎选择在塑造用户对本地企业的接触方面的重要性，特别是在权威来源稀缺、目录式或聚合网站占主导地位的分散市场中。 5.2.6 大品牌偏见（可乐垂直）。目的：本实验检验当查询无品牌时，生成式人工智能系统是否表现出对主要汽水品牌相对于小众/独立品牌的系统偏好。具体来说，我们询问模型的输出是否不成比例地呈现全球领先品牌（例如，可口可乐、百事可乐）相对于较小的工艺或区域品牌，以及这种偏差在模型之间是否一致。

### 段落 158 · Page 19

**EN**

Experimental Design.We queried ChatGPT and Perplexity with a set of fifty unbranded prompts that ask for “most popular/best/top. . . ” cola or soda recommendations (e.g.,most popular cola brand; best selling soda in the world; top cola brands in the US; classic soda brands everyone knows; most iconic soda brands). Brand mentions in the models’ answers were mapped to two curated sets,majorglobal leaders andniche/indiecraft or regional brands, and any remaining names were labeledOther(details of extraction, normalization, and mapping follow the general pipeline in §5.1).

**中文**

实验设计。我们使用一组 50 个无品牌提示来查询 ChatGPT 和 Perplexity，询问“最受欢迎/最佳/顶级……”可乐或苏打水推荐（例如，最受欢迎的可乐品牌；世界上最畅销的苏打水；美国顶级可乐品牌；每个人都知道的经典苏打水品牌；最具标志性的苏打水品牌）。模型答案中提及的品牌被映射到两个精心策划的集合，即主要的全球领导者和利基/独立工艺或区域品牌，并且任何剩余的名称都被标记为其他（提取、标准化和映射的详细信息遵循第 5.1 节中的一般流程）。

### 段落 159 · Page 19

**EN**

Brand sets used in evaluation: We report three outcome families: (i) brand-share distributions across the categories Major, Niche, and Other; (ii) brand-level counts for all named brands; and (iii) consulted-domain profiles based on the citations each model surfaced. Results.Across both systems, answers skewed toward major brands. For ChatGPT, major brands account for 56.3% of all identified brand mentions (274 of 487), niche brands for 12.3% (60), and other brands for 31.4% (153) (Figs. 33, 36). Perplexity exhibits an

**中文**

评估中使用的品牌集：我们报告了三个结果系列：（i）跨“主要”、“利基”和“其他”类别的品牌份额分布； (ii) 所有指定品牌的品牌级别计数； (iii) 基于每个模型出现的引用的参考领域概况。结果。在这两个系统中，答案都偏向于主要品牌。对于 ChatGPT，主要品牌占所有已识别品牌提及的 56.3%（487 个中的 274 个），小众品牌占 12.3%（60 个），其他品牌占 31.4%（153 个）（图 33、36）。困惑表现出

### Page 20

### 段落 160 · Page 20

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas Major brands Niche/indie brands Coca-Cola, Pepsi, Sprite, Mountain Dew, Dr Pepper, Fanta, 7Up, Schweppes, A&W Root Beer, Barq’s Root Beer, Canada Dry, Crush, Sunkist, Mirinda, Fresca, Mello Yello, Seagram’s, Slice, Tango, Lilt Jones Soda, Boylan Bottling Co., Sprecher, Faygo, Cheerwine, Moxie, Ale-8-One, Jarritos, Zevia, Fitz’s, Maine Root, Bruce Cost Ginger Ale, Sioux City Sarsaparilla, Thomas Kemper, Dry Soda, Virgil’s, Leninade, Cock ’n Bull, Blenheim Ginger Ale, Red Ribbon Soda Table 1: Big Brand Bias: Brand sets used in the cola vertical experiment even stronger tilt toward major names: 67.9% major (339 of 499), 5.8% niche (29), and 26.3% other (131) (Figs.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 主要品牌 小众/独立品牌 Coca-Cola、Pepsi、Sprite、Mountain Dew、Dr Pepper、Fanta、7Up、Schweppes、A&W Root Beer、Barq’s Root Beer、Canada Dry、Crush、Sunkist、Mirinda、Fresca、Mello Yello、西格兰 (Seagram’s)、Slice、Tango、Lilt Jones Soda、博伊兰装瓶公司、Sprecher、Faygo、Cheerwine、Moxie、Ale-8-One、Jarritos、Zevia、Fitz’s、Maine Root、Bruce Cost Ginger Ale、Sioux City Sarsaparilla、Thomas Kemper、干苏打水、Virgil’s、Leninade、Cock ’n Bull、Blenheim 姜汁汽水、Red Ribbon Soda 表 1：大品牌偏见：可乐垂直实验中使用的品牌集更倾向于主要品牌：67.9% 主要品牌（499 个品牌中的 339 个）、5.8% 小众品牌（29 个）和 26.3% 其他品牌（131 个）（图 1 和 2）。

### 段落 161 · Page 20

**EN**

34, 37). Pooling the two systems yields a combined distribution of 62.2% major, 9.0% niche, and 28.8% other (Figs. 32, 35). Taken together, these shares indicate that both models favor major brands, with Perplexity’s preference visibly stronger (higher major share, lower niche share). Brand-level concentration mirrors these aggregates. In both models, Coca-Cola and Pepsi dominate the head of the distribution (ChatGPT: 78 and 44 mentions; Perplexity: 107 and 58), with Dr Pepper consistently occupying the next tier (ChatGPT: 30; Perplexity: 34).

**中文**

34、37）。将这两个系统合并起来，得到 62.2% 主要、9.0% 小众和 28.8% 其他的组合分布（图 32、35）。总而言之，这些份额表明两种模型都偏爱主要品牌，其中 Perplexity 的偏好明显更强（主要份额较高，利基份额较低）。品牌层面的集中度反映了这些总量。在这两个模型中，可口可乐和百事可乐都占据了分布的首位（ChatGPT：78 和 44 次提及；Perplexity：107 和 58），而 Dr Pepper 始终占据下一层（ChatGPT：30；Perplexity：34）。

### 段落 162 · Page 20

**EN**

Niche brands such as Jones Soda, Boylan, Faygo, and Sprecher do surface, but at much lower frequencies (Figs. 33, 34). Figure 32: Big Brand Bias: Individual brand counts (combined) Cited-domain profiles also differ by system. ChatGPT shows a relatively concentrated pattern, relying heavily on Wikipedia (∼19.7% of citations) and a small set of consumer-review and food sites (e.g., accio.com, Tasting Table, Sporked) (Fig. 38).

**中文**

Jones Soda、Boylan、Faygo 和 Sprecher 等小众品牌确实出现过，但频率要低得多（图 33、34）。图 32：大品牌偏见：各个品牌计数（组合）被引域名配置文件也因系统而异。 ChatGPT 显示出相对集中的模式，严重依赖维基百科（约 19.7% 的引用）和一小部分消费者评论和食品网站（例如 accio.com、Tasting Table、Sporked）（图 38）。

### 段落 163 · Page 20

**EN**

Perplexity distributes citations across a broader long tail (the “Others” bucket≈ 60.6%), with YouTube as the single most frequent domain (∼8.9%) and additional coverage from Tasting Table, The Daily Meal, Caffeine Informer, Statista, Visual Capitalist, TikTok, and others (Fig. 39). Despite these different evidence profiles, Perplexity still returns more major brands overall than ChatGPT.

**中文**

Perplexity 将引用分布在更广泛的长尾上（“其他”桶约占 60.6%），其中 YouTube 是最常见的域（约 8.9%），其他覆盖范围还包括 Tasting Table、The Daily Meal、Caffeine Informer、Statista、Visual Capitalist、TikTok 等（图 39）。尽管证据概况不同，Perplexity 总体上返回的主要品牌仍多于 ChatGPT。

### 段落 164 · Page 20

**EN**

Figure 33: Big Brand Bias: Brand counts (ChatGPT) Figure 34: Big Brand Bias: Brand counts (Perplexity) Interpretation.The two systems marshal evidence differently, one more encyclopedic and concentrated, the other more multimedia and dispersed, yet under unbranded prompts both default to market-leading brands. The relative magnitudes of the category shares suggest that, absent explicit constraints, source prominence and model priors jointly pull recommendations toward major labels. 5.2.7 Bank Queries Across Personas.

**中文**

图 33：大品牌偏见：品牌重要 (ChatGPT) 图 34：大品牌偏见：品牌重要（困惑） 解释。两个系统以不同方式整理证据，一个更加百科全书式且集中，另一个更加多媒体且分散，但在无品牌提示下，两者都默认为市场领先品牌。类别份额的相对大小表明，如果没有明确的约束，来源突出性和模型先验共同将推荐拉向主要标签。 5.2.7 跨角色的银行查询。

### 段落 165 · Page 20

**EN**

Objective.We compare how four AI systems, Gemini, Perplexity, ChatGPT, Claude, rank banks when queries are phrased in a ranking format and conditioned on three personas: (i) young professionals entering the workforce, (ii) mid-career individuals with families, and (iii) retirees. The goal is to characterize differences in the domains of sources each model cites across personas, as well as the types of these sources (brand, social, earned).

**中文**

目标。我们比较了 Gemini、Perplexity、ChatGPT、Claude 这四种人工智能系统在以排名格式进行查询并以三种角色为条件时如何对银行进行排名：(i) 进入劳动力市场的年轻专业人士，(ii) 有家庭的职业中期个人，以及 (iii) 退休人员。目标是描述每个模型跨人物角色引用的来源领域的差异，以及这些来源的类型（品牌、社交、赢得）。

### 段落 166 · Page 20

**EN**

Experimental Design.We adapted a comprehensive set of banking questions for each persona into bank-ranking prompts (e.g., fees and waivers, ATM networks, mobile features, APY/ CDs, mortgages/ HELOCs, fraud protection, retirement services). For each persona × model combination, we collected the full responses and citations,

**中文**

实验设计。我们将针对每个角色的一套全面的银行问题调整为银行排名提示（例如，费用和豁免、ATM 网络、移动功能、APY/CD、抵押贷款/HELOC、欺诈保护、退休服务）。对于每个角色×模型组合，我们收集了完整的回复和引用，

### Page 21

### 段落 167 · Page 21

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA Figure 35: Big Brand Bias: Category summary (combined) Figure 36: Big Brand Bias: Category summary (ChatGPT) extracted domains, and classified them as brand (bank-owned), social (forums/communities), or earned (editorial/third-party). The extraction, normalization, and classification steps follow the common pipeline in §5.1. We report (a) the distribution of domain types per persona × model and overall, and (b) the most frequent domains for each persona×model and in aggregate.

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区 图 35：大品牌偏见：类别摘要（组合） 图 36：大品牌偏见：类别摘要 (ChatGPT) 提取域，并将其分类为品牌（银行拥有）、社交（论坛/社区）或赢得（编辑/第三方）。提取、标准化和分类步骤遵循第 5.1 节中的通用流程。我们报告（a）每个角色×模型和总体的域类型分布，以及（b）每个角色×模型和总体的最常见域。

### 段落 168 · Page 21

**EN**

Results.Overall mix.Across all models and personas, earned sources dominate, with brand second and social minimal (overall: earned 64.6%, brand 34.1%, social 1.2%; see Fig. 40). This pattern reflects extensive reliance on editorial reviews and financial explainers in ranking-style answers. Differences across models.The engine identity explains more variation than persona.

**中文**

结果。总体组合。在所有模型和角色中，赚取来源占主导地位，品牌次之，社交来源最小（总体：赚取 64.6%，品牌 34.1%，社交 1.2%；见图 40）。这种模式反映了排名式答案对编辑评论和财务解释的广泛依赖。模型之间的差异。引擎身份比人物角色解释了更多的变化。

### 段落 169 · Page 21

**EN**

Figure 37: Big Brand Bias: Category summary (Perplexity) Figure 38: Big Brand Bias: Top consulted domains (ChatGPT) Figure 39: Big Brand Bias: Top consulted domains (Perplexity) • ChatGPT and Claude are the mostearned-heavy: for all three personas they concentrate citations on third-party editorial sites; brand shares remain comparatively low (Fig. 41, first/third rows).

**中文**

图 37：大品牌偏见：类别摘要（Perplexity） 图 38：大品牌偏见：咨询最多的域（ChatGPT） 图 39：大品牌偏见：咨询最多的域（Perplexity） • ChatGPT 和 Claude 是最赚钱的：对于所有三个角色，他们都将引用集中在第三方编辑网站上；品牌份额仍然相对较低（图 41，第一/第三行）。

### Page 22

### 段落 170 · Page 22

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas Figure 40: Bank Queries Across Personas: Overall domaintype distribution (all models/personas) • Perplexity mixes earned and brand more evenly, but still leans earned across personas (Fig. 41, second row). • Gemini is the mostbrand-leaning: brand sources are frequently at or above half of citations across personas, particularly for the family persona (Fig. 41, fourth row). Persona effects.Within-model shifts with persona are modest relative to cross-model gaps.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 图 40：跨角色的银行查询：整体领域类型分布（所有模型/角色） • 困惑度更均匀地混合了赚取和品牌，但仍然倾向于跨角色赚取（图 41，第二行）。 • 双子座最倾向于品牌：品牌来源经常达到或超过人物角色引用的一半，特别是对于家庭人物角色（图41，第四行）。人物角色效应。相对于跨模型差距，模型内人物角色的变化是适度的。

### 段落 171 · Page 22

**EN**

A consistent nuance is that retirees tend to draw a slightly higher brand share than young professionals or families for the more earned-oriented models (e.g., ChatGPT, Claude), while Gemini remains brand-forward across all personas. In short,who the engine ismatters more thanwhich personais queried. Domain ecology (aggregate).The aggregate top-domain view is led by Bankrate and NerdWallet, followed by mainstream business media (e.g., CNBC, Forbes, Yahoo Finance, Business Insider, Kiplinger). Bank of America and U.S. Bank are notable brand outliers within the top ten (Fig. 42).

**中文**

一个一致的细微差别是，退休人员倾向于比年轻专业人士或家庭更倾向于以收入为导向的模型（例如 ChatGPT、Claude）获得略高的品牌份额，而 Gemini 在所有角色中都保持品牌领先。简而言之，引擎是谁比询问谁更重要。域名生态（聚合）。顶级域名的聚合观点以 Bankrate 和 NerdWallet 为首，其次是主流商业媒体（例如 CNBC、福布斯、雅虎财经、Business Insider、Kiplinger）。美国银行 (Bank of America) 和全美银行 (U.S. Bank) 是前十名中值得注意的品牌异类（图 42）。

### 段落 172 · Page 22

**EN**

The long tail is substantial (“Other” is the largest bar), indicating wide dispersion beyond a few anchors. Social signals.Social sources contribute very little across all settings (near-zero slices in Fig. 41, and ∼1% overall in Fig. 40), suggesting that bank-ranking prompts elicit editorial/brand pages far more than community discussions. Interpretation.Under ranking-style banking prompts, all systems converge on editorial financial media as primary evidence, but differ in how much they incorporate brand-owned pages.

**中文**

长尾很长（“其他”是最大的条），表明除了几个锚点之外的广泛分散。社交信号。社交来源在所有设置中贡献很小（图 41 中的切片接近于零，图 40 中总体约为 1%），这表明银行排名提示引发的社论/品牌页面远远多于社区讨论。解释。在排名式银行提示下，所有系统都集中于社论金融媒体作为主要证据，但在纳入品牌拥有页面的程度方面有所不同。

### 段落 173 · Page 22

**EN**

The ordering that emerges from these results is: Gemini (most brand-leaning) → Perplexity (balanced) → Claude / ChatGPT (most earned-heavy). Figure 41: Bank Queries Across Personas: Domain-type shares by model×persona Figure 42: Bank Queries Across Personas: Overall top 10 domains with type breakdown Persona changes do modulate the mix, for instance, retirees occasionally tilt some engines toward brand resources, but these shifts are smaller than the between-engine differences. The dominance of

**中文**

从这些结果中得出的排序是：Gemini（最倾向于品牌）→ Perplexity（平衡）→ Claude / ChatGPT（最注重挣钱）。图 41：跨角色的银行查询：按模型×角色划分的领域类型份额 图 42：跨角色的银行查询：类型细分的总体前 10 个域 角色变化确实会调节组合，例如，退休人员偶尔会向品牌资源倾斜一些引擎，但这些转变小于引擎之间的差异。的统治地位

### Page 23

### 段落 174 · Page 23

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA Bankrate/NerdWallet and the breadth of the long tail point to a citation ecosystem where authoritative, evergreen review hubs anchor the answers, while brand sites are selectively injected depending on the engine. 5.2.8 Language Sensitivity Experiment. Objective.We examine how language affects AI search outputs across engines. Concretely, we ask whether the brands and domains surfaced for the same intents vary when prompts are translated into Chinese, Japanese, German, French, and Spanish (vs.

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区 Bankrate/NerdWallet 和长尾的广度指向了一个引文生态系统，其中权威的、常青的评论中心锚定答案，而品牌网站则根据引擎有选择地注入。 5.2.8 语言敏感性实验。目标：我们研究语言如何影响跨引擎的人工智能搜索输出。具体来说，我们询问当提示被翻译成中文、日语、德语、法语和西班牙语（与中文、日语、德语、法语和西班牙语）时，出于相同意图而出现的品牌和域名是否有所不同。

### 段落 175 · Page 23

**EN**

English), and how the type and language of cited websites shift across languages. Experimental Design.Design and pipeline exactly follow §4.2.3 (the same language sensitivity experiment), except that we exclude Google and compare AI engines with one another (Gemini, Claude, ChatGPT, Perplexity). We use the same ten verticals and five target languages (Chinese, Japanese, German, French, Spanish vs. English). Apart from the additional brand-overlap heatmaps, all other metrics and reporting conventions are identical to §4.2.3.

**中文**

英语），以及引用网站的类型和语言如何跨语言转变。实验设计。设计和管道完全遵循§4.2.3（相同的语言敏感性实验），只是我们排除了 Google 并将 AI 引擎相互比较（Gemini、Claude、ChatGPT、Perplexity）。我们使用相同的十个垂直领域和五种目标语言（中文、日语、德语、法语、西班牙语和英语）。除了额外的品牌重叠热图之外，所有其他指标和报告约定均与第 4.2.3 节相同。

### 段落 176 · Page 23

**EN**

Specifically: • Domain-overlap heatmaps:English–X overlaps by vertical, computed as the Jaccard index on cited-domain sets and averaged within each vertical (definition per §4.2.3). • Brand-overlap heatmaps:English–X overlaps by vertical, computed as the Jaccard index on extracted brand sets per query (from LLM answers), then averaged within each vertical (consistent with the domain-overlap calculation). • Aggregate pies:overalldomain-typemix (brand / social / earned) andwebsite-languagemix (English vs. non- English) across all verticals, same as in §4.2.3. Extraction, normalization, and classification follow the common pipeline in §5.1.

**中文**

具体来说： • 领域重叠热图：English-X 按垂直方向重叠，计算为引用领域集上的 Jaccard 指数，并在每个垂直方向内取平均值（根据第 4.2.3 节定义）。 • 品牌重叠热图：English-X 按垂直方向重叠，计算为每个查询（来自LLM 答案）提取的品牌集的Jaccard 索引，然后在每个垂直方向内取平均值（与域重叠计算一致）。 • 总体饼图：所有垂直领域的总体域类型组合（品牌/社交/赢得）和网站语言组合（英语与非英语），与§4.2.3 中相同。提取、标准化和分类遵循 §5.1 中的通用流程。

### 段落 177 · Page 23

**EN**

Results.Cross-language domain stability is limited and model-dependent.Domain overlap varies sharply by engine. Claude shows the highest cross-language stability (frequent high overlaps across verticals; Fig. 7). Perplexity and Gemini tend to have much lower cross-language domain overlap overall (a few low to moderate cells, with the majority remaining very low or near zero; Figs. 8, 9). GPT shows the lowest overlap: in our sample, domain sets across languages are consistently near-zero, i.e., it taps different site ecosystems by language (Fig. 10).

**中文**

结果。跨语言域稳定性是有限的并且依赖于模型。域重叠因引擎而异。 Claude 显示出最高的跨语言稳定性（跨垂直领域经常出现高度重叠；图 7）。 Perplexity 和 Gemini 总体上往往具有较低的跨语言域重叠（一些低到中等的单元，其中大多数仍然非常低或接近于零；图 8、9）。 GPT 显示出最低的重叠：在我们的示例中，跨语言的域集始终接近于零，即它按语言利用不同的站点生态系统（图 10）。

### 段落 178 · Page 23

**EN**

Brand overlap also differs by engine.Across the board, brand overlap is much higher than domain overlap. Patterns vary by model and vertical. For example, Perplexity and ChatGPT reach medium to high overlap in several high-concentration verticals (e.g., laptops, camera equipment; Figs. 43, 44). Claude is similarly strong across many categories (smartphones, camera, outdoor gear; Fig. 45), with pockets near or above 0.5. Gemini is comparable overall, with strong cells in laptops and several headphones/camera pairs while exhibiting more low values (<0.30) in home appliances and fitness equipment.

**中文**

品牌重叠度也因引擎而异。总体而言，品牌重叠度远高于领域重叠度。图案因型号和垂直方向而异。例如，Perplexity 和 ChatGPT 在几个高集中度垂直领域（例如笔记本电脑、相机设备；图 43、44）达到中等到高度重叠。 Claude 在许多类别（智能手机、相机、户外装备；图 45）上同样表现强劲，口袋数接近或高于 0.5。 Gemini 总体上具有可比性，在笔记本电脑和几对耳机/相机中具有强劲的电池，而在家用电器和健身设备中表现出较低的值（<0.30）。

### 段落 179 · Page 23

**EN**

Overall, no single engine dominates across all verticals; stability is vertical-dependent. (Fig. 46). Source types remain earned-heavy across languages.When aggregating all verticals, models, and languages, we can see that the engine identity explains more variation than languages used. The domain distributions follows a earned ≫ brand ≫ social pattern across AI engines (Fig. 11).

**中文**

总体而言，没有哪一个引擎能够在所有垂直领域占据主导地位。稳定性取决于垂直方向。 （图 46）。源类型在不同语言中仍然很重要。当聚合所有垂直领域、模型和语言时，我们可以看到引擎标识比所使用的语言解释了更多的变化。域分布遵循 AI 引擎中赢得的≫品牌≫社交模式（图 11）。

### 段落 180 · Page 23

**EN**

This mirrors §5.2.2: ranking-style Figure 43: Language Sensitivity: Brand overlap heatmap, Perplexity Figure 44: Language Sensitivity: Brand overlap heatmap, GPT Figure 45: Language Sensitivity: Brand overlap heatmap, Claude prompts tend to elicit editorial evidence regardless of language. Regarding the differences across models, GPT and Claude are the most earned-heavy (Fig. 11, second and fourth column), while Perplexity and Gemini have a greater share of brand and social sources (but remains the earned ≫ brand ≫ social pattern; Fig. 11, third and fifth column), which is also similar to §5.2.2.

**中文**

这反映了§5.2.2：排名式 图 43：语言敏感性：品牌重叠热图，困惑 图 44：语言敏感性：品牌重叠热图，GPT 图 45：语言敏感性：品牌重叠热图，无论语言如何，克劳德提示都倾向于引出编辑证据。关于模型之间的差异，GPT和Claude是最赚钱的（图11，第二和第四列），而Perplexity和Gemini拥有更大的品牌和社交来源份额（但仍然是赚取≫品牌≫社交模式；图11，第三和第五列），这也类似于§5.2.2。

### Page 24

### 段落 181 · Page 24

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas Figure 46: Language Sensitivity: Brand overlap heatmap, Gemini Website language depends on the engine.Under non-English prompts, citations skew toward the target language, but to different degrees (Fig. 12): GPT and Perplexity are the most local-language heavy (Fig. 12, second and third column); Claude is the special case where English dominates and non-English is only a very small share (Fig. 12, fourth column); Gemini is more balanced, with the split fluctuating by language. Across languages, a consistent gradient emerges (Fig.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 图 46：语言敏感性：品牌重叠热图，Gemini 网站语言取决于引擎。在非英语提示下，引用偏向目标语言，但程度不同（图 12）：GPT 和 Perplexity 本地语言最重（图 12，第二列和第三列）； Claude 是一个特例，英语占主导地位，非英语只占很小的比例（图 12，第四列）；双子座更加平衡，分歧因语言而波动。跨语言，出现了一致的梯度（图 1）。

### 段落 182 · Page 24

**EN**

12): Japanese and French prompts produce the strongest localization (targetlanguage sites dominate across engines); Chinese is also highly localized but with a slightly larger English slices (especially clear for Gemini); German and Spanish are more mixed, often have larger English slices (especially Gemini where the English slices for these two languages are close to 50%). This language gradient holds after excluding Claude’s extreme English-heavy behavior and is most pronounced for GPT and Perplexity. Interpretation.Language reshapes results at two levels: the evidence ecology (which sites are cited) and the brand lists.

**中文**

12）：日语和法语提示产生最强的本地化（目标语言网站在各个引擎中占主导地位）；中文也高度本地化，但英文部分稍大（对于双子座来说尤其明显）；德语和西班牙语更加混合，通常具有较大的英语切片（尤其是 Gemini，这两种语言的英语切片接近 50%）。在排除 Claude 极端的英语重度行为后，这种语言梯度仍然成立，并且在 GPT 和 Perplexity 中最为明显。 Interpretation.Language 在两个层面重塑结果：证据生态（引用了哪些网站）和品牌列表。

### 段落 183 · Page 24

**EN**

Claude reuses a relatively stable set of authority domains across languages; GPT effectively swaps in different site ecosystems by language, yielding very low cross-language domain overlap; Perplexity and Gemini sit between these poles. On the brand side, overlap is higher where global head brands dominate (e.g., cameras, laptops) and lower in more localized or long-tail categories (e.g. home appliances, fitness equipment). Implication: for consistent visibility in multilingual markets, brands need coverage in authoritative local-language media as well as English, and a multi-engine, multi-language distribution strategy is warranted.

**中文**

Claude 跨语言复用了一组相对稳定的权限域； GPT 按语言有效地在不同的站点生态系统中进行交换，从而产生非常低的跨语言域重叠；困惑和双子座位于这两极之间。在品牌方面，全球头部品牌占主导地位的领域（例如相机、笔记本电脑）重叠度较高，而本地化或长尾类别（例如家用电器、健身器材）的重叠度较低。含义：为了在多语言市场中保持一致的知名度，品牌需要在权威的当地语言媒体和英语中进行报道，并且多引擎、多语言的分销策略是必要的。

### 段落 184 · Page 24

**EN**

5.2.9 Paraphrase Sensitivity Experiment. Objective.We test whether small, within-language changes in how a query is phrased alter what the systems surface. For the same intent, we compare the brands and domains returned when prompts are reworded and whether the mix of source types (brand / social / earned) shifts. This section mirrors the language experiment but replaces translation with controlled paraphrases. Experimental Design.Design and pipeline exactly follow §4.2.4 (the same paraphrase sensitivity experiment), except that we exclude Google and compare AI engines with one another (Gemini, ChatGPT, Perplexity).

**中文**

5.2.9 释义敏感性实验。目标：我们测试查询措辞方式的语言内微小变化是否会改变系统的显示内容。出于相同的意图，我们比较了提示被重新措辞时返回的品牌和域名，以及来源类型（品牌/社交/赢得）的组合是否发生变化。本节反映了语言实验，但用受控释义取代了翻译。实验设计。设计和流程完全遵循§4.2.4（相同的释义敏感性实验），只是我们排除了 Google 并将 AI 引擎与其他引擎（Gemini、ChatGPT、Perplexity）进行比较。

### 段落 185 · Page 24

**EN**

We use the same ten verticals and the same seven paraphrase templates:justification_required,source_required, quote_required,confidence_score,ranked_order,imperative_list,keyword_only. Apart from the additional brand-overlap heatmaps, all other metrics and reporting conventions are identical to §4.2.4. Specifically: • Domain-overlap heatmaps:base–paraphrase overlaps by vertical, computed as the Jaccard index on cited-domain sets per query and averaged within each vertical (definition per §4.2.4).

**中文**

我们使用相同的十个垂直方向和相同的七个释义模板：justification_required、source_required、quote_required、confidence_score、ranked_order、imperative_list、keyword_only。除了额外的品牌重叠热图之外，所有其他指标和报告约定均与第 4.2.4 节相同。具体来说： • 域重叠热图：按垂直方向的基本释义重叠，计算为每个查询的引用域集上的 Jaccard 索引，并在每个垂直方向内取平均值（根据第 4.2.4 节定义）。

### 段落 186 · Page 24

**EN**

• Brand-overlap heatmaps:base–paraphrase overlaps by vertical, computed as the Jaccard index on extracted brand sets per query (from LLM answers), then averaged within each vertical (consistent with the domain-overlap calculation). • Aggregate pies:overalldomain-typemix (brand / social / earned) across all verticals, same as in §4.2.4. Extraction, normalization, and classification follow the common pipeline in §5.1. Results.Paraphrases move results less than languages.Relative to §5.2.8 (language sensitivity test), paraphrasing induces smaller perturbations.

**中文**

• 品牌重叠热图：按垂直方向的基本释义重叠，计算为每个查询（来自LLM 答案）提取的品牌集的Jaccard 索引，然后在每个垂直方向内取平均值（与域重叠计算一致）。 • 总体饼图：所有垂直领域的总体域类型混合（品牌/社交/赢得），与§4.2.4 中相同。提取、标准化和分类遵循 §5.1 中的通用流程。结果。释义对结果的影响小于语言。相对于§5.2.8（语言敏感性测试），释义引起的扰动较小。

### 段落 187 · Page 24

**EN**

Brand lists are generally robust to paraphrasing (high overlaps), while domain sets change more than brands but still remain much more stable than in the cross-language study. Brand overlap (within engine).Across verticals, GPT shows generally high cross-paraphrase stability (many cells exceed 0.6 or even 0.7), indicating that once intent is fixed, wording rarely overturns head brands (Fig. 47). Gemini reaches moderately high to high overall (roughly 0.4–0.7 across most verticals), with a few lowoverlap cells in verticals such as gaming consoles (Fig. 48).

**中文**

品牌列表通常对释义很稳健（高度重叠），而领域集的变化比品牌更大，但仍然比跨语言研究稳定得多。品牌重叠（引擎内）。在垂直行业中，GPT 通常表现出较高的交叉释义稳定性（许多单元格超过 0.6 甚至 0.7），这表明一旦意图确定，措辞很少会推翻头部品牌（图 47）。双子座总体达到中等偏高（在大多数垂直领域大约为 0.4-0.7），在游戏机等垂直领域有一些低重叠单元（图 48）。

### 段落 188 · Page 24

**EN**

Perplexity is comparable on average but displays the widest spread, gaming consoles notably lower, indicating stronger category-specific sensitivity (Fig. 49). Figure 47: Paraphrase Sensitivity: Brand overlap heatmap, GPT Domain overlap (within engine).Paraphrases affect which articles get cited more than which brands appear. Perplexity and

**中文**

平均困惑度相当，但分布范围最广，游戏机明显较低，表明特定类别的敏感性更强（图 49）。图 47：释义敏感性：品牌重叠热图，GPT 域重叠（引擎内）。释义对哪些文章被引用的影响大于对哪些品牌出现的影响。困惑和

### Page 25

### 段落 189 · Page 25

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA Figure 48: Paraphrase Sensitivity: Brand overlap heatmap, Gemini Figure 49: Paraphrase Sensitivity: Brand overlap heatmap, Perplexity Gemini show the highest domain stability across paraphrases (numerous mid-to-high overlaps; Figs. 15, 16). GPT has lower overlaps overall, i.e., it rotates supporting sites even when brand slates are similar (Fig. 14). Source-type mix across paraphrase styles.The earned-heavy pattern persists for all engines, and the distribution differences across AI engines also mirrors previous sections.

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区 图 48：释义敏感性：品牌重叠热图，Gemini 图 49：释义敏感性：品牌重叠热图，困惑 Gemini 在释义中表现出最高的域稳定性（大量中高重叠；图 15、16）。 GPT 总体上重叠率较低，即即使品牌相似，它也会轮换支持站点（图 14）。跨释义风格的源类型混合。所有引擎都存在重赚模式，并且 AI 引擎之间的分布差异也反映了前面的部分。

### 段落 190 · Page 25

**EN**

Shares differ by engine, but the brand/social/earned distribution changes little across paraphrases (Fig. 17). Interpretation.Rewording primarily changes format and citations, not the core recommendations. Compared with translation, paraphrases seldom overturn brand lists, especially for GPT and Gemini, though Perplexity is more wording-sensitive in certain verticals. Domain selection is more pliable (notably for GPT), yet still more stable than in the language experiment.

**中文**

份额因引擎而异，但品牌/社交/收入分布在不同释义之间几乎没有变化（图 17）。解释。改写主要改变格式和引文，而不是核心建议。与翻译相比，释义很少推翻品牌列表，尤其是对于 GPT 和 Gemini，尽管 Perplexity 在某些垂直领域对措辞更加敏感。域选择更加灵活（尤其是 GPT），但仍然比语言实验更加稳定。

### 段落 191 · Page 25

**EN**

Practically, tuning content to satisfy sources/quotes/ranking instructions can influence which specific articles get cited, but language localization has a much larger impact on both the evidence ecology and brand visibility than prompt rephrasing alone. 5.3 The Generative Engine Optimization Agenda 5.3.1 Engineer for Agency and Scannability.A universal finding across all engines and verticals is the critical need for machinereadable, structured data. AI systems function as agents that must parse, interpret, and synthesize information to generate answers. Websites cluttered with marketing fluff and unstructured content will fail.

**中文**

实际上，调整内容以满足来源/引用/排名说明可以影响哪些特定文章被引用，但语言本地化对证据生态和品牌知名度的影响比单独的提示改写要大得多。 5.3 生成式引擎优化议程 5.3.1 代理和可扫描性工程师。所有引擎和垂直行业的普遍发现是对机器可读的结构化数据的迫切需求。人工智能系统充当代理，必须解析、解释和合成信息以生成答案。充斥着营销废话和非结构化内容的网站将会失败。

### 段落 192 · Page 25

**EN**

The primary action is to treat your website as an API for AI. This requires rigorous implementation of technical SEO fundamentals combined with detailed schema markup (Schema.org) for all entities—products, specifications, prices, reviews, warranty details, and availability. This technical foundation is non-negotiable for being "do business with" by AI agents. 5.3.2 Dominate Earned Media Across All Engines.The most consistent and significant finding is the overwhelming bias of AI engines toward Earned media.

**中文**

主要行动是将您的网站视为人工智能的 API。这需要严格实施技术 SEO 基础知识，并结合所有实体（产品、规格、价格、评论、保修详细信息和可用性）的详细架构标记 (Schema.org)。这种技术基础对于人工智能代理的“做生意”来说是不容谈判的。 5.3.2 在所有引擎中主导赢得媒体。最一致和最重要的发现是人工智能引擎对赢得媒体的压倒性偏见。

### 段落 193 · Page 25

**EN**

Claude and ChatGPT are extremely earnedheavy, while Perplexity and Gemini incorporate more brand and social content but still prioritize earned sources. To win in AI search, a brand must shift its focus from creating owned content to systematically earning third-party validation. This means investing heavily in public relations, media outreach, and expert collaborations to secure features, reviews, and mentions in the authoritative publications and review sites that these engines favor.

**中文**

Claude 和 ChatGPT 的收入来源非常重，而 Perplexity 和 Gemini 则融入了更多的品牌和社交内容，但仍然优先考虑收入来源。为了在人工智能搜索中获胜，品牌必须将其重点从创建自有内容转向系统地获得第三方验证。这意味着要在公共关系、媒体推广和专家合作方面投入大量资金，以确保这些引擎所青睐的权威出版物和评论网站上的功能、评论和提及。

### 段落 194 · Page 25

**EN**

Building a portfolio of backlinks from these high-authority domains is not a secondary tactic but the core GEO strategy, as it directly feeds the AI’s perception of your brand’s expertise, authoritativeness, and trustworthiness (E-E-A-T). 5.3.3 Engine-Specific Tactics for Brand Visibility.The analysis reveals that engine choice fundamentally alters the information ecosystem a user encounters. Therefore, a one-size-fits-all approach is ineffective.

**中文**

从这些高权威域构建反向链接组合不是次要策略，而是核心 GEO 策略，因为它直接满足人工智能对您品牌的专业知识、权威性和可信度 (E-E-A-T) 的感知。 5.3.3 针对品牌可见度的引擎特定策略。分析表明，引擎选择从根本上改变了用户遇到的信息生态系统。因此，一刀切的方法是无效的。

### 段落 195 · Page 25

**EN**

For Claude and ChatGPT, which exhibit high crosslanguage brand stability and a strong earned bias, the strategy is to secure a position within the core set of globally recognized, authoritative domains in your vertical. For Perplexity, which incorporates more diverse sources including YouTube and retail sites, the strategy expands to include creating video content and ensuring product information is accurately listed on major retailer domains.

**中文**

对于 Claude 和 ChatGPT 来说，它们表现出高度的跨语言品牌稳定性和强烈的赢得偏见，其策略是确保在您所在行业的全球认可的权威领域核心组中占据一席之地。对于包含 YouTube 和零售网站等更多样化来源的 Perplexity，该策略扩展到包括创建视频内容并确保产品信息在主要零售商域中准确列出。

### 段落 196 · Page 25

**EN**

Gemini, which shows a greater propensity to cite brand-owned properties, allows for a slightly more balanced approach that leverages both earned media and well-structured, deep content on your own domain. 5.3.4 Multilingual Strategy: Localize Authority, Not Just Content. The language sensitivity experiment demonstrates that success in non-English markets requires more than simple translation. GPT and Perplexity heavily localize, sourcing almost entirely from the target language’s ecosystem. Claude, by contrast, reuses Englishlanguage authority domains across languages. This demands a dual-path strategy.

**中文**

双子座更倾向于引用品牌拥有的资产，它允许采取稍微平衡的方法，利用您自己领域的免费媒体和结构良好的深层内容。 5.3.4 多语言策略：权威本地化，而不仅仅是内容本地化。语言敏感性实验表明，在非英语市场取得成功需要的不仅仅是简单的翻译。 GPT 和 Perplexity 高度本地化，几乎完全来自目标语言的生态系统。相比之下，克劳德跨语言重用英语权威域。这就需要双路径战略。

### 段落 197 · Page 25

**EN**

To win on GPT and Perplexity in a specific region, you must build relationships with and earn coverage from the most authoritative local-language publishers and review sites. Simultaneously, strengthening your brand’s presence in top-tier English-language earned media can improve visibility on Claude across many languages. A brand must audit the authority landscape in each target region and engine to allocate resources effectively.

**中文**

要在特定地区赢得 GPT 和 Perplexity，您必须与最权威的本地语言出版商和评论网站建立关系并获得覆盖。同时，加强您的品牌在顶级英语免费媒体中的影响力可以提高克劳德在多种语言中的知名度。品牌必须审核每个目标区域和引擎的权威格局，以有效分配资源。

### Page 26

### 段落 198 · Page 26

**EN**

Conference’17, July 2017, Washington, DC, USA Mahe Chen, Xiaoxuan Wang, Kaiwen Chen, and Nick Koudas 5.3.5 Content Strategy: Justify and Compare for the Shortlist.AI search is not about generating ten blue links but about justifying a placement on a synthesized shortlist. The low domain overlap between engines indicates that each AI is synthesizing answers from a different set of sources, but they are all seeking clear, unambiguous justification. Website content must be explicitly engineered to answer comparison questions.

**中文**

Conference’17，2017 年 7 月，美国华盛顿特区 Mahe Chen、Xiaoxuan Wang、Kaiwen Chen 和 Nick Koudas 5.3.5 内容策略：候选名单的合理性和比较。人工智能搜索不是要生成 10 个蓝色链接，而是要证明在综合候选名单上的放置位置的合理性。引擎之间的低域重叠表明每个人工智能正在综合来自不同来源的答案，但它们都在寻求清晰、明确的理由。网站内容必须经过明确设计才能回答比较问题。

### 段落 199 · Page 26

**EN**

This involves creating scannable, justification-rich content such as detailed comparison tables against competitors, bulleted pros and cons lists, and clear, bolded statements of value proposition (e.g., "longest battery life, " "best for small families"). The brand that makes it easiest for the AI to extract reasons for its superiority will win the recommendation. 5.3.6 Niche Brand Strategy: Overcome the Big Brand Bias.The observed big brand bias presents a significant challenge for niche and indie brands. Unbranded queries default to market leaders. To break through, niche brands must over-invest in building tangible, verifiable authority.

**中文**

这涉及创建可浏览的、理由丰富的内容，例如与竞争对手的详细比较表、项目符号优缺点列表，以及清晰、粗体的价值主张陈述（例如“最长的电池寿命”、“最适合小家庭”）。让人工智能最容易提取其优越性的原因的品牌将赢得推荐。 5.3.6 小众品牌战略：克服大品牌偏见。观察到的大品牌偏见对小众品牌和独立品牌提出了重大挑战。无品牌查询默认为市场领导者。为了取得突破，小众品牌必须过度投资来建立有形的、可验证的权威。

### 段落 200 · Page 26

**EN**

This can be achieved by dominating a specific, narrow niche through deep expert content and targeted earned media campaigns in specialty publications. They should also leverage strategies that work on Perplexity, such as creating high-quality YouTube review content and engaging with community discussions, to build a grassroots authority that can eventually be recognized by the more conservative engines like Claude and GPT. 6 The Imperative for Principled GEO Methodologies and Services The experimental data reveals a critical truth: the AI search landscape is not a monolith but a fragmented, dynamic, and highly competitive ecosystem.

**中文**

这可以通过专业出版物中深入的专家内容和有针对性的赢得媒体活动来主导特定的、狭窄的利基市场来实现。他们还应该利用针对 Perplexity 的策略，例如创建高质量的 YouTube 评论内容和参与社区讨论，以建立一个草根权威，最终可以得到 Claude 和 GPT 等更保守的引擎的认可。 6 有原则的 GEO 方法和服务势在必行 实验数据揭示了一个关键事实：人工智能搜索领域不是一个整体，而是一个分散、动态且高度竞争的生态系统。

### 段落 201 · Page 26

**EN**

Success is not achieved through isolated tactics but requires a continuous, principled, and strategic discipline. The old paradigm of periodic SEO audits is obsolete. The new paradigm demands a comprehensive GEO operating system—a suite of methodologies and managed services designed to achieve and defend dominance across all major AI engines. This system must be built on five core pillars. First, a principled methodology requires continuous, enginespecific competitive intelligence. The low domain overlap and differing source biases mean that a strategy that works on Perplexity may fail on Claude. Brands cannot afford to guess.

**中文**

成功不是通过孤立的策略来实现的，而是需要持续的、有原则的和战略性的纪律。定期 SEO 审核的旧模式已经过时。新范式需要一个全面的 GEO 操作系统——一套旨在实现和捍卫所有主要人工智能引擎主导地位的方法和托管服务。该系统必须建立在五个核心支柱之上。首先，原则性的方法需要持续的、特定于引擎的竞争情报。低域重叠和不同的来源偏差意味着适用于 Perplexity 的策略可能会在 Claude 上失败。品牌无法猜测。

### 段落 202 · Page 26

**EN**

They need a service that continuously audits the digital ecosystem for their core topics, identifying exactly which sources each AI engine (Claude, GPT, Perplexity, Gemini) privileges. This involves mapping the "citation network" for your vertical: which earned media outlets, YouTube creators, and retail domains are consistently cited for key queries. This intelligence forms the absolute foundation of strategy, answering the critical questions of which sources are most important and what content to create by reverse-engineering the evidence base of the engines themselves.

**中文**

他们需要一种服务来持续审核数字生态系统的核心主题，准确识别每个人工智能引擎（Claude、GPT、Perplexity、Gemini）权限的来源。这涉及到为您的垂直领域绘制“引用网络”：媒体机构、YouTube 创作者和零售领域始终被关键查询引用。这种情报构成了战略的绝对基础，通过对引擎本身的证据基础进行逆向工程，回答了哪些来源最重要以及要创建哪些内容等关键问题。

### 段落 203 · Page 26

**EN**

Second, strategy must be guided by a structured content and justification framework. Knowing the sources is not enough; a methodology is needed to out-compete them on their own terms. This involves a deliberate shift from creating general top-of-funnel content to engineering "justification assets. " A principled service will deploy a framework to audit existing content and plan new content against a strict checklist: Does it contain explicit, machinescannable comparison data? Does it feature a clear, bolded value proposition that an AI can extract as a "justification attribute"? Is it structured with schema to be effortlessly parsed?

**中文**

其次，战略必须以结构化内容和理由框架为指导。知道来源还不够；还需要了解来源。需要一种方法来按照自己的条件击败他们。这涉及到从创建一般的漏斗顶部内容到设计“论证资产”的有意转变。有原则的服务将部署一个框架来审核现有内容并根据严格的清单规划新内容：它是否包含明确的、机器可扫描的比较数据？它是否具有清晰、大胆的价值主张，可供人工智能提取作为“理由属性”？它是否具有可以轻松解析的架构？

### 段落 204 · Page 26

**EN**

This framework turns content creation from an art into a science, ensuring every asset is built to win a place in the AI’s shortlist. Third, brands must implement a systematic authority-building and earned media pipeline. The overwhelming bias toward earned media makes this the most critical investment. A principled methodology moves beyond sporadic PR to a managed service focused on GEO outcomes. This pipeline proactively identifies the top-tier authoritative sources in the mapped citation network and executes a continuous campaign to secure features, reviews, and expert commentary within them.

**中文**

该框架将内容创作从一门艺术转变为一门科学，确保每项资产的构建都能在人工智能的候选名单中赢得一席之地。第三，品牌必须实施系统的权威建设和赢得媒体渠道。对免费媒体的压倒性偏见使其成为最关键的投资。有原则的方法超越了零星的公关，转向专注于 GEO 结果的托管服务。该管道主动识别映射引文网络中的顶级权威来源，并执行持续的活动以确保其中的功能、评论和专家评论。

### 段落 205 · Page 26

**EN**

The goal is not just a press mention but the deliberate cultivation of a backlink profile and online authority that every AI engine is trained to recognize and trust. This is how a brand ensures it is perceived as an authoritative source by the AI, making its inclusion in recommendations non-negotiable. Fourth, a defensive and offensive ranking defense system is nonnegotiable. The landscape is not static; competitors are continuously executing these same strategies. A principled methodology must therefore include continuous monitoring and defense.

**中文**

其目标不仅仅是媒体提及，而是刻意培养每个人工智能引擎都经过培训以识别和信任的反向链接配置文件和在线权威。这就是品牌确保其被人工智能视为权威来源的方式，使其纳入推荐中是不容协商的。第四，防守和进攻的排名防守体系是不容谈判的。景观不是静态的；竞争对手不断执行这些相同的策略。因此，原则性方法必须包括持续监控和防御。

### 段落 206 · Page 26

**EN**

This involves tracking your ranking for core "shortlist" queries across all major AI engines and rapidly identifying any erosion in position. When a competitor gains ground, the system triggers a response: creating a more comprehensive justification asset, targeting a new earned media placement, or strengthening schema on a key page. This transforms GEO from a passive optimization task into an active, ongoing battle for visibility where speed and strategic response are paramount. Finally, success requires an integrated, metrics-driven execution platform. These pillars cannot operate in silos.

**中文**

这涉及跟踪所有主要人工智能引擎中核心“候选名单”查询的排名，并快速识别位置的任何侵蚀。当竞争对手取得进展时，系统会触发响应：创建更全面的理由资产，瞄准新的赢得媒体投放，或加强关键页面上的架构。这将 GEO 从被动的优化任务转变为主动、持续的可见性之战，其中速度和战略响应至关重要。最后，成功需要一个集成的、指标驱动的执行平台。这些支柱不能孤立运作。

### 段落 207 · Page 26

**EN**

A true GEO service integrates them into a single dashboard and workflow. It connects the competitive intelligence to the content framework, directing which justification assets to build. It ties the authority pipeline directly to the target source list. It uses the ranking defense system to measure the ROI of every placed article and created asset. This closed-loop system allows for the strategic prioritization of enginerelated tactics, answering how to prioritize based on where the greatest opportunity or threat exists, and ensuring resources are allocated to the efforts with the highest impact on AI visibility.

**中文**

真正的 GEO 服务将它们集成到单个仪表板和工作流程中。它将竞争情报与内容框架连接起来，指导构建哪些理由资产。它将权限管道直接与目标源列表联系起来。它使用排名防御系统来衡量每个放置的文章和创建的资产的投资回报率。这个闭环系统允许对引擎相关策略进行战略优先级排序，回答如何根据最大机会或威胁存在的位置进行优先级排序，并确保资源分配给对人工智能可见性影响最大的工作。

### 段落 208 · Page 26

**EN**

In conclusion, the complexity and competitiveness of the generative search environment have rendered ad-hoc SEO tactics obsolete. The only path to sustainable dominance is through a principled, disciplined, and continuous GEO methodology. This is not a one-time project but an essential managed service—an ongoing arms race where victory belongs to those with the best intelligence, the most impactful content, the strongest authority, and the fastest reaction time.

**中文**

总之，生成搜索环境的复杂性和竞争性使得临时 SEO 策略变得过时。实现可持续主导地位的唯一途径是通过有原则、有纪律和持续的 GEO 方法。这不是一个一次性项目，而是一项重要的托管服务——一场持续的军备竞赛，胜利属于那些拥有最智慧、最有影响力的内容、最强大的权威和最快反应时间的人。

### 段落 209 · Page 26

**EN**

7 Assumptions and Limitations of the Study This study provides a detailed snapshot of Generative AI search engine behaviors, but its findings are necessarily bounded by specific constraints in time, methodology, and data access. These limitations must be acknowledged to properly contextualize the results and their applicability. First and foremost, the temporal nature of this analysis is a primary limitation. The data was collected in August 2025, and

**中文**

7 研究的假设和局限性 本研究提供了生成式人工智能搜索引擎行为的详细快照，但其研究结果必然受到时间、方法和数据访问方面的特定限制。必须承认这些局限性，以便正确地说明结果及其适用性。首先也是最重要的，这种分析的时间性质是一个主要限制。数据收集于 2025 年 8 月，

### Page 27

### 段落 210 · Page 27

**EN**

Generative Engine Optimization: How to Dominate AI Search Conference’17, July 2017, Washington, DC, USA the behaviors, algorithms, and user interfaces of the services studied—Google, ChatGPT, Claude, Perplexity, and Gemini—are inherently dynamic. The competitive landscape of AI search is evolving at an accelerated pace. It is highly probable that these services will continually adjust their sourcing methodologies, ranking algorithms, and presentation of results (including how and if they cite sources) in response to competitive pressures, user feedback, and technological advancements.

**中文**

生成式引擎优化：如何主导人工智能搜索会议’17，2017 年 7 月，美国华盛顿特区。所研究的服务（Google、ChatGPT、Claude、Perplexity 和 Gemini）的行为、算法和用户界面本质上是动态的。人工智能搜索的竞争格局正在加速发展。这些服务很可能会根据竞争压力、用户反馈和技术进步不断调整其采购方法、排名算法和结果呈现（包括如何以及是否引用来源）。

### 段落 211 · Page 27

**EN**

Therefore, the specific quantitative distributions of source types (Brand, Earned, Social) and the observed levels of inter-engine overlap are a product of this specific moment in time. Consequently, treating these findings as permanent truths is not advised. To remain relevant, the periodic evaluation and repetition of this study is imperative to track trends, identify shifts in strategy, and update optimization practices accordingly. A second significant limitation lies in the source classification system. The study employed a proprietary three-tiered classification system (Brand, Earned, Social) to categorize domains.

**中文**

因此，源类型（品牌、赢得、社交）的具体定量分布和观察到的引擎间重叠水平是该特定时刻的产物。因此，不建议将这些发现视为永久事实。为了保持相关性，必须定期评估和重复这项研究，以跟踪趋势、识别策略变化并相应更新优化实践。第二个重要的限制在于源分类系统。该研究采用专有的三层分类系统（品牌、收益、社交）对领域进行分类。

### 段落 212 · Page 27

**EN**

While every effort was made to ensure consistency and objectivity through a combination of predefined rules and AI-assisted labeling, this framework is ultimately a constructed model of the digital information ecosystem. The definitions of these categories, while logical, are subjective. For instance, the line between an "Earned" media outlet and a "Brand" blog can sometimes be blurry.

**中文**

虽然我们尽一切努力通过预定义规则和人工智能辅助标签的结合来确保一致性和客观性，但该框架最终是数字信息生态系统的构建模型。这些类别的定义虽然合乎逻辑，但却是主观的。例如，“免费”媒体渠道和“品牌”博客之间的界限有时可能很模糊。

### 段落 213 · Page 27

**EN**

A different research team utilizing an alternative classification system—for example, one with more granular categories like "News Media, " "Professional Review, " "User Review, " "E-commerce, " and "Corporate"—would inevitably produce different quantitative results. Therefore, the absolute percentages reported should be interpreted as illustrative of strong, relative trends (e.g., the dominance of Earned media) rather than as immutable facts. The comparative findings between engines are more robust than the absolute figures themselves. Finally, a fundamental constraint of this external analysis is the lack of access to internal data.

**中文**

不同的研究团队使用替代的分类系统（例如，具有更细粒度的类别，如“新闻媒体”、“专业评论”、“用户评论”、“电子商务”和“企业”）将不可避免地产生不同的定量结果。因此，报告的绝对百分比应被解释为强烈的相对趋势的说明（例如，免费媒体的主导地位），而不是不可改变的事实。发动机之间的比较结果比绝对数字本身更可靠。最后，这种外部分析的一个基本限制是无法访问内部数据。

### 段落 214 · Page 27

**EN**

The study was conducted from the outside looking in, analyzing the outputs of these AI systems without access to their internal query logs, user data, ranking models, or training data intricacies. This "black box" nature means that while the study can accurately describe what is happening, the definitive why remains inferred. Different research threads around mechanistic interpretability will assist in that regard. In summary, this study offers a valuable and rigorous comparative analysis of AI search engines at a critical point in their development.

**中文**

这项研究是从外部向内进行的，分析这些人工智能系统的输出，而无需访问其内部查询日志、用户数据、排名模型或复杂的训练数据。这种“黑匣子”性质意味着，虽然研究可以准确描述正在发生的事情，但确切的原因仍然是推断出来的。围绕机械可解释性的不同研究线索将在这方面有所帮助。总之，这项研究对处于发展关键阶段的人工智能搜索引擎进行了有价值且严格的比较分析。

### 段落 215 · Page 27

**EN**

However, its conclusions are constrained by their temporal specificity, the subjective nature of its classification schema, and the inherent opacity of the systems being studied. These limitations do not invalidate the findings but rather define the scope within which they should be applied—as a powerful guide for current strategy that must be continually validated against the evolving reality of the search landscape. 8 Acknowledgments We wish to thank the team at ktau.ai (www.ktau.ai) the leader in Generative Engine Optimization for their support.

**中文**

然而，其结论受到其时间特异性、分类模式的主观性质以及所研究系统固有的不透明性的限制。这些限制并不会使研究结果无效，而是定义了它们应该应用的范围——作为当前策略的有力指南，必须根据搜索环境不断变化的现实不断验证该策略。 8 致谢 我们要感谢 ktau.ai (www.ktau.ai) 团队（生成式引擎优化领域的领导者）的支持。

### 段落 216 · Page 27

**EN**

References [1] Pranjal Aggarwal, Vishvak Murahari, Tanmay Rajpurohit, Ashwin Kalyan, Karthik Narasimhan, and Ameet Deshpande. 2024. GEO: Generative Engine Optimization. arXiv:2311.09735 [cs.LG] https://arxiv.org/abs/2311.09735 [2] Perplexity AI. 2025.CEO says Perplexity hit 780M queries in May 2025. https://www.perplexity.ai/page/ceo-says-perplexity-hit-780m-qdENgiYOuTfaMEpxLQc2bIQ [Online]. Available. [3] Pew Research Center. 2025.About a third of U.S. adults have used ChatGPT; usage has increased over the past year.

**中文**

参考文献 [1] Pranjal Aggarwal、Vishvak Murahari、Tanmay Rajpurohit、Ashwin Kalyan、Karthik Narasimhan 和 Ameet Deshpande。 2024.GEO：生成式引擎优化。 arXiv:2311.09735 [cs.LG] https://arxiv.org/abs/2311.09735 [2] 困惑人工智能。 2025.CEO 表示，Perplexity 在 2025 年 5 月达到了 7.8 亿次查询。https://www.perplexity.ai/page/ceo-says-perplexity-hit-780m-qdENgiYOuTfaMEpxLQc2bIQ [在线]。可用的。 [3] 皮尤研究中心。 2025年。大约三分之一的美国成年人使用过ChatGPT；过去一年的使用量有所增加。

### 段落 217 · Page 27

**EN**

https://www.pewresearch.org/short-reads/2025/ 06/25/34-of-us-adults-have-used-chatgpt-about-double-the-share-in-2023/ [Online]. Available. [4] Pew Research Center. 2025.Google users are less likely to click on links when an AI summary appears in the results. https://www.pewresearch.org/shortreads/2025/07/22/google-users-are-less-likely-to-click-on-links-when-an-aisummary-appears-in-the-results/ [Online]. Available. [5] Aounon Kumar and Himabindu Lakkaraju. 2024. Manipulating Large Language Models to Increase Product Visibility. arXiv:2404.07981 [cs.IR] https://arxiv.org/ abs/2404.07981 [6] Similarweb.

**中文**

https://www.pewresearch.org/short-reads/2025/06/25/34-of-us-adults-have-used-chatgpt-about-double-the-share-in-2023/[在线]。可用的。 [4] 皮尤研究中心。 2025. 当人工智能摘要出现在结果中时，Google 用户点击链接的可能性较小。 https://www.pewresearch.org/shortreads/2025/07/22/google-users-are-less-likely-to-click-on-links-when-an-aisummary-appears-in-the-results/ [在线]。可用的。 [5]奥农·库马尔和希玛宾杜·拉卡拉朱。 2024。操纵大型语言模型以提高产品可见性。 arXiv:2404.07981 [cs.IR] https://arxiv.org/abs/2404.07981 [6] 相似网站。

### 段落 218 · Page 27

**EN**

2024.ChatGPT Surges to 3.1B Visits in September 2024. https://www.similarweb.com/blog/insights/ai-news/chatgpt-topped-3billion-visits-in-september/ [Online]. Available. [7] StatCounter Global Stats. 2025.AI Chatbot Market Share Worldwide. https: //gs.statcounter.com/ai-chatbot-market-share [Online]. Available. [8] StatCounter Global Stats. 2025.Search Engine Market Share Worldwide. https: //gs.statcounter.com/search-engine-market-share [Online]. Available. [9] Alexander Wan, Eric Wallace, and Dan Klein. 2024. What Evidence Do Language Models Find Convincing? arXiv:2402.11782 [cs.CL] https://arxiv.org/abs/2402. 11782 [10] WIRED.

**中文**

2024.ChatGPT 2024 年 9 月访问量激增至 3.1B。https://www.similarweb.com/blog/insights/ai-news/chatgpt-topped-3billion-visits-in-september/ [在线]。可用的。 [7] StatCounter 全球统计。 2025.AI 聊天机器人全球市场份额。 https://gs.statcounter.com/ai-chatbot-market-share [在线]。可用的。 [8] StatCounter 全球统计。 2025. 全球搜索引擎市场份额。 https://gs.statcounter.com/search-engine-market-share [在线]。可用的。 [9] 亚历山大·万、埃里克·华莱士和丹·克莱因。 2024.语言模型有哪些令人信服的证据？ arXiv:2402.11782 [cs.CL] https://arxiv.org/abs/2402。 11782 [10]连线。

### 段落 219 · Page 27

**EN**

2024.Google Cut Back AI Overviews in Search Even Before Its ’Pizza Glue’ Fiasco. https://searchengineland.com/google-ai-overviews-visibility-drops-15percent-queries-442850?utm_source=chatgpt.com [Online]. Available.

**中文**

2024.谷歌甚至在“披萨胶”惨败之前就削减了搜索中的人工智能概述。 https://searchengineland.com/google-ai-overviews-visibility-drops-15percent-queries-442850?utm_source=chatgpt.com [在线]。可用的。
