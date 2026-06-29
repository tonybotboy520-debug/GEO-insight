# GEO: Generative Engine Optimization

- ID: 62
- 类型: pdf
- 分类: 04_academic_papers
- 主题: foundational GEO benchmark and visibility optimization paper
- 原文链接: https://arxiv.org/pdf/2311.09735
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### Page 1

### 段落 1 · Page 1

**EN**

GEO: Generative Engine Optimization Pranjal Aggarwal∗ Indian Institute of Technology Delhi New Delhi, India pranjal2041@gmail.com Vishvak Murahari∗ Princeton University Princeton, USA murahari@cs.princeton.edu Tanmay Rajpurohit Independent Seattle, USA tanmay.rajpurohit@gmail.com Ashwin Kalyan Independent Seattle, USA asaavashwin@gmail.com Karthik Narasimhan Princeton University Princeton, USA karthikn@princeton.edu Ameet Deshpande Princeton University Princeton, USA asd@princeton.edu ABSTRACT The advent of large language models (LLMs) has ushered in a new paradigm of search engines that use generative models to gather and summarize information to answer user queries.

**中文**

GEO：生成式引擎优化 Pranjal Aggarwal* 印度理工学院 德里 新德里，印度 pranjal2041@gmail.com Vishvak Murahari* 普林斯顿大学 普林斯顿，美国 murahari@cs.princeton.edu Tanmay Rajpurohit Independent 西雅图，美国 tanmay.rajpurohit@gmail.com Ashwin Kalyan Independent 西雅图，美国 asaavashwin@gmail.com Karthik Narasimhan 普林斯顿大学美国普林斯顿 karthikn@princeton.edu Ameet Deshpande 普林斯顿大学 美国普林斯顿 asd@princeton.edu 摘要 大语言模型 (LLM) 的出现带来了一种新的搜索引擎范例，该范例使用生成模型来收集和总结信息来回答用户查询。

### 段落 2 · Page 1

**EN**

This emerging technology, which we formalize under the unified framework of generative engines (GEs), can generate accurate and personalized responses, rapidly replacing traditional search engines like Google and Bing. Generative Engines typically satisfy queries by synthesizing information from multiple sources and summarizing them using LLMs. While this shift significantly improves user utility and generative search engine traffic, it poses a huge challenge for the third stakeholder – website and content creators.

**中文**

我们在生成式引擎 (GE) 的统一框架下将这种新兴技术正式化，可以生成准确且个性化的响应，迅速取代 Google 和 Bing 等传统搜索引擎。生成式引擎通常通过综合来自多个来源的信息并使用 LLM 对其进行汇总来满足查询。虽然这种转变显着提高了用户效用和生成式搜索引擎流量，但它给第三个利益相关者——网站和内容创建者带来了巨大的挑战。

### 段落 3 · Page 1

**EN**

Given the black-box and fast-moving nature of generative engines, content creators have little to no control over when and how their content is displayed. With generative engines here to stay, we must ensure the creator economy is not disadvantaged. To address this, we introduce Generative Engine Optimization (GEO), the first novel paradigm to aid content creators in improving their content visibility in generative engine responses through a flexible black-box optimization framework for optimizing and defining visibility metrics.

**中文**

鉴于生成式引擎的黑匣子和快速移动的性质，内容创建者几乎无法控制其内容的显示时间和方式。随着生成式引擎的存在，我们必须确保创作者经济不处于不利地位。为了解决这个问题，我们引入了生成式引擎优化（GEO），这是第一个新颖的范式，通过用于优化和定义可见性指标的灵活的黑盒优化框架，帮助内容创建者提高生成式引擎响应中的内容可见性。

### 段落 4 · Page 1

**EN**

We facilitate systematic evaluation by introducingGEO-bench, a large-scale benchmark of diverse user queries across multiple domains, along with relevant web sources to answer these queries. Through rigorous evaluation, we demonstrate that GEO can boost visibility by up to 40% in generative engine responses. Moreover, we show the efficacy of these strategies varies across domains, underscoring the need for domain-specific optimization methods.

**中文**

我们通过引入 GEO-bench（跨多个领域的不同用户查询的大规模基准）以及回答这些查询的相关网络资源来促进系统评估。通过严格的评估，我们证明 GEO 可以将生成式发动机响应的可见性提高高达 40%。此外，我们表明这些策略的功效在不同领域有所不同，强调了对特定领域优化方法的需求。

### 段落 5 · Page 1

**EN**

Our work opens a new frontier in information discovery systems, with profound implications for both developers of generative engines and content creators.1 ∗Equal Contribution 1Code and Data available at https://generative-engines.com/GEO/ Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. Copyrights for components of this work owned by others than the author(s) must be honored. Abstracting with credit is permitted.

**中文**

我们的工作开辟了信息发现系统的新领域，对生成式引擎的开发人员和内容创作者都具有深远的影响。1 *平等贡献1代码和数据可在 https://generative-engines.com/GEO/ 上获得。免费授予本作品的全部或部分的数字或硬拷贝以供个人或课堂使用，前提是副本不是为了盈利或商业利益而制作或分发，并且副本上附有此通知和完整引用。必须尊重作者以外的其他人拥有的本作品组件的版权。允许以信用方式提取。

### 段落 6 · Page 1

**EN**

To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee. Request permissions from permissions@acm.org. KDD ’24, August 25–29, 2024, Barcelona, Spain © 2024 Copyright held by the owner/author(s). Publication rights licensed to ACM. ACM ISBN 979-8-4007-0490-1/24/08 https://doi.org/10.1145/3637528.3671900 CCS CONCEPTS • Computing methodologies → Natural language processing ; Machine learning; • Information systems → Web searching and information discovery.

**中文**

要以其他方式复制、重新发布、发布到服务器上或重新分发到列表，需要事先获得特定许可和/或付费。从permissions@acm.org 请求权限。 KDD ’24，2024 年 8 月 25 日至 29 日，西班牙巴塞罗那 © 2024 版权所有由所有者/作者持有。出版权授权给 ACM。 ACM ISBN 979-8-4007-0490-1/24/08 https://doi.org/10.1145/3637528.3671900 CCS 概念 • 计算方法 → 自然语言处理；机器学习； • 信息系统→ 网络搜索和信息发现。

### 段落 7 · Page 1

**EN**

KEYWORDS generative models, search engines, datasets and benchmarks ACM Reference Format: Pranjal Aggarwal, Vishvak Murahari, Tanmay Rajpurohit, Ashwin Kalyan, Karthik Narasimhan, and Ameet Deshpande. 2024. GEO: Generative Engine Optimization. In Proceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining (KDD ’24), August 25–29, 2024, Barcelona, Spain. ACM, New York, NY, USA, 12 pages. https://doi.org/10.1145/3637528. 3671900 1 INTRODUCTION The invention of traditional search engines three decades ago revolutionized information access and dissemination globally [4].

**中文**

关键词 生成模型、搜索引擎、数据集和基准 ACM 参考格式：Pranjal Aggarwal、Vishvak Murahari、Tanmay Rajpurohit、Ashwin Kalyan、Karthik Narasimhan 和 Ameet Deshpande。 2024.GEO：生成式引擎优化。第 30 届 ACM SIGKDD 知识发现和数据挖掘会议 (KDD ’24) 会议记录，2024 年 8 月 25 日至 29 日，西班牙巴塞罗那。 ACM，美国纽约州纽约市，12 页。 https://doi.org/10.1145/3637528。 3671900 1 简介 三十年前传统搜索引擎的发明彻底改变了全球信息的访问和传播[4]。

### 段落 8 · Page 1

**EN**

While they were powerful and ushered in a host of applications like academic research and e-commerce, they were limited to providing a list of relevant websites for user queries. However, the recent success of large language models [ 5, 21] has paved the way for better systems like BingChat, Google’s SGE, and perplexity.ai that combine conventional search engines with generative models. We dub these systems generative engines (GE) because they search for information and generate multi-modal responses by using multiple sources.

**中文**

虽然它们功能强大并引入了学术研究和电子商务等大量应用程序，但它们仅限于提供相关网站列表以供用户查询。然而，大型语言模型 [5, 21] 最近的成功为 BingChat、Google 的 SGE 和 perplexity.ai 等将传统搜索引擎与生成模型相结合的更好系统铺平了道路。我们将这些系统称为生成式引擎（GE），因为它们通过使用多个来源搜索信息并生成多模式响应。

### 段落 9 · Page 1

**EN**

Technically, generative engines (Figure 2) retrieve relevant documents from a database (like the internet) and use large neural models to generate a response grounded on the sources, ensuring attribution and a way for the user to verify the information. The usefulness of generative engines for developers and users is evident – users access information faster and more accurately, while developers craft precise and personalized responses, improving user satisfaction and revenue. However, generative engines disadvantage the third stakeholder – website and content creators.

**中文**

从技术上讲，生成式引擎（图 2）从数据库（如互联网）检索相关文档，并使用大型神经模型生成基于来源的响应，确保归因以及用户验证信息的方式。生成式引擎对开发人员和用户的用处是显而易见的——用户更快、更准确地访问信息，而开发人员则制定精确和个性化的响应，从而提高用户满意度和收入。然而，生成式引擎对第三个利益相关者——网站和内容创建者——不利。

### 段落 10 · Page 1

**EN**

Generative Engines, in contrast to traditional search engines, remove the need to navigate to websites by directly providing a precise and comprehensive response, potentially reducing organic traffic to websites and impacting their visibility [16]. With millions of small businesses and individuals relying on online traffic and visibility for their livelihood, generative engines will significantly disrupt the creator economy. Further, the black-box and proprietary nature of generative engines makes it difficult for content arXiv:2311.09735v3 [cs.LG] 28 Jun 2024

**中文**

与传统搜索引擎相比，生成式引擎通过直接提供精确而全面的响应来消除导航到网站的需要，从而可能减少网站的自然流量并影响其可见性[16]。由于数以百万计的小企业和个人依靠在线流量和知名度来谋生，生成式引擎将极大地扰乱创作者经济。此外，生成式引擎的黑盒和专有性质使得内容变得困难 arXiv:2311.09735v3 [cs.LG] 28 Jun 2024

### Page 2

### 段落 11 · Page 2

**EN**

KDD ’24, August 25–29, 2024, Barcelona, Spain Pranjal Aggarwal et al. Figure 1: Our proposed Generative Engine Optimization (GEO) method optimizes websites to boost their visibility in Generative Engine responses. GEO’s black-box optimization framework then enables the website owner of the pizza website, which lacked visibility originally, to optimize their website to increase visibility under Generative Engines. Further, GEO’s general framework allows content creators to define and optimize their custom visibility metrics, giving them greater control in this new emerging paradigm.

**中文**

KDD '24，2024 年 8 月 25-29 日，西班牙巴塞罗那 Pranjal Aggarwal 等人。图 1：我们提出的生成式引擎优化 (GEO) 方法可优化网站，以提高其在生成式引擎响应中的可见性。 GEO 的黑盒优化框架使最初缺乏可见性的披萨网站的网站所有者能够优化其网站，以提高生成式引擎下的可见性。此外，GEO 的通用框架允许内容创建者定义和优化他们的自定义可见性指标，使他们能够更好地控制这一新兴范例。

### 段落 12 · Page 2

**EN**

creators to control and understand how their content is ingested and portrayed. In this work, we propose the first general creator-centric framework to optimize content for generative engines, which we dub Generative Engine Optimization (GEO), to empower content creators to navigate this new search paradigm. GEO is a flexible black-box optimization framework for optimizing web content visibility for proprietary and closed-source generative engines (Figure 1). GEO ingests a source website and outputs an optimized version by tailoring and calibrating the presentation, text style, and content to increase visibility in generative engines.

**中文**

创作者可以控制和了解他们的内容是如何被摄取和描绘的。在这项工作中，我们提出了第一个以创作者为中心的通用框架来优化生成式引擎的内容，我们将其称为生成式引擎优化（GEO），以使内容创作者能够驾驭这种新的搜索范例。 GEO 是一种灵活的黑盒优化框架，用于优化专有和闭源生成式引擎的 Web 内容可见性（图 1）。 GEO 摄取源网站并通过定制和校准演示文稿、文本样式和内容来输出优化版本，以提高生成式引擎的可见性。

### 段落 13 · Page 2

**EN**

Further, GEO introduces a flexible framework for defining visibility metrics tailor-made for generative engines as the notion of visibility in generative engines is more nuanced and multi-faceted than traditional search engines (Figure 3). While average ranking on the response page is a good measure of visibility in traditional search engines, which present a linear list of websites, this does not apply to generative engines. Generative Engines provide rich, structured responses and embed websites as inline citations in the response, often embedding them with different lengths, at varying positions, and with diverse styles.

**中文**

此外，GEO 引入了一个灵活的框架，用于定义专为生成式引擎量身定制的可见性指标，因为生成式引擎中的可见性概念比传统搜索引擎更加细致和多面（图 3）。虽然响应页面上的平均排名是传统搜索引擎中可见性的一个很好的衡量标准，它提供了线性的网站列表，但这并不适用于生成式引擎。生成式引擎提供丰富、结构化的响应，并将网站作为内联引用嵌入到响应中，通常以不同的长度、不同的位置和不同的样式嵌入它们。

### 段落 14 · Page 2

**EN**

This necessitates the need for visibility metrics tailor-made for generative engines, which measure the visibility of attributed sources over multiple dimensions, such as relevance and influence of citation to query, measured through both an objective and a subjective lens. To facilitate faithful and extensive evaluation of GEO methods, we propose GEO-bench, a benchmark consisting of 10000 queries from diverse domains and sources, adapted for generative engines.

**中文**

这就需要为生成式引擎量身定制可见性指标，衡量归因源在多个维度上的可见性，例如通过客观和主观镜头衡量的引用与查询的相关性和影响力。为了促进对 GEO 方法的忠实和广泛的评估，我们提出了 GEO-bench，这是一个由来自不同领域和来源的 10000 个查询组成的基准，适用于生成式引擎。

### 段落 15 · Page 2

**EN**

Through systematic evaluation, we demonstrate that our proposed Generative Engine Optimization methods can boost visibility by up to 40% on diverse queries, providing beneficial strategies for content creators. Among other things, we find that including citations, quotations from relevant sources, and statistics can significantly boost source visibility, with an increase of over 40% across various queries. We also demonstrate the efficacy of Generative Engine Optimization on Perplexity.ai, a real-world generative engine and demonstrate visibility improvements up to 37%.

**中文**

通过系统评估，我们证明我们提出的生成式引擎优化方法可以将各种查询的可见性提高高达 40%，为内容创建者提供有益的策略。除此之外，我们发现，包括引文、相关来源的引用和统计数据可以显着提高来来源可见度，各种查询的增加超过 40%。我们还展示了生成式引擎优化在现实生成式引擎 Perplexity.ai 上的功效，并展示了高达 37% 的可见性改进。

### 段落 16 · Page 2

**EN**

In summary, our contributions are three-fold: (1) We propose Generative Engine Optimization, the first general optimization framework for website owners to optimize their websites for generative engines. Generative Engine Optimization can improve the visibility of websites by up to 40% on a wide range of queries, domains, and real-world black-box generative engines. (2) Our framework proposes a comprehensive set of visibility metrics specifically designed for generative engines and enables content creators to flexibly optimize their content through customized visibility metrics.

**中文**

总之，我们的贡献有三方面：（1）我们提出生成式引擎优化，这是网站所有者针对生成式引擎优化其网站的第一个通用优化框架。生成式引擎优化可以在各种查询、域和现实世界的黑盒生成式引擎上将网站的可见性提高高达 40%。 (2)我们的框架提出了一套专门为生成式引擎设计的全面的可见性指标，使内容创建者能够通过定制的可见性指标灵活地优化其内容。

### 段落 17 · Page 2

**EN**

(3) To foster faithful evaluation of GEO methods in generative engines, we propose the first large-scale benchmark consisting of diverse search queries from wide-ranging domains and datasets specially tailored for Generative Engines.

**中文**

(3) 为了促进对生成式引擎中 GEO 方法的忠实评估，我们提出了第一个大规模基准，其中包括来自广泛领域的各种搜索查询和专门为生成式引擎定制的数据集。

### Page 3

### 段落 18 · Page 3

**EN**

GEO: Generative Engine Optimization KDD ’24, August 25–29, 2024, Barcelona, Spain Figure 2: Overview of Generative Engines. Generative Engines primrarily consists of a set of generative models and a search engine to retrieve relevant documents. Generative Engines take user query as input and through a series of steps generate a final response that is grounded in the retrieved sources with inline attributions. 2 FORMULATION & METHODOLOGY 2.1 Formulation of Generative Engines Despite the deployment of numerous generative engines to millions of users, there is currently no standard framework.

**中文**

GEO：生成式引擎优化 KDD '24，2024 年 8 月 25-29 日，西班牙巴塞罗那 图 2：生成式引擎概述。生成式引擎主要由一组生成模型和一个用于检索相关文档的搜索引擎组成。生成式引擎将用户查询作为输入，并通过一系列步骤生成最终响应，该响应基于具有内联属性的检索源。 2 公式与方法 2.1 生成式引擎的公式 尽管为数百万用户部署了众多的生成式引擎，但目前还没有标准框架。

### 段落 19 · Page 3

**EN**

We provide a formulation that accommodates various modular components in their design. We describe a generative engine, which includes several backend generative models and a search engine for source retrieval. A Generative Engine (GE) takes a user query 𝑞𝑢 and returns a natural language response 𝑟, where 𝑃𝑈 represents personalized user information.

**中文**

我们提供的配方可在设计中容纳各种模块化组件。我们描述了一个生成式引擎，其中包括几个后端生成模型和一个用于源检索的搜索引擎。生成式引擎（GE）接受用户查询𝑞𝑢并返回自然语言响应𝑟，其中𝑃𝑈表示个性化用户信息。

### 段落 20 · Page 3

**EN**

The GE can be represented as a function: 𝑓𝐺𝐸 := (𝑞𝑢, 𝑃𝑈 ) → 𝑟 (1) Generative Engines comprise two crucial components: a.) A set of generative models𝐺 = {𝐺1, 𝐺2...𝐺𝑛 }, each serving a specific purpose like query reformulation or summarization, and b.) A search engine 𝑆𝐸 that returns a set of sources 𝑆 = {𝑠1, 𝑠2...𝑠𝑚 } given a query 𝑞. We present a representative workflow in Figure 2, which, at the time of writing, closely resembles the design of BingChat. This workflow breaks down the input query into a set of simpler queries that are easier to consume for the search engine.

**中文**

GE 可以表示为一个函数： 𝑓𝐺𝐸 := (𝑞𝑢, 𝑃𝑈 ) → 𝑟 (1) 生成式引擎包含两个关键组件： a.) 一组生成模型𝐺 = {𝐺1, 𝐺2...𝐺𝑛 }，每个模型服务于特定目的，例如查询重构或总结，以及 b.) 一个搜索引擎 𝑆𝐸，根据查询 𝑞 返回一组源 𝑆 = {𝑠1, 𝑠2...𝑠𝑚 }。我们在图 2 中展示了一个代表性的工作流程，在撰写本文时，该工作流程与 BingChat 的设计非常相似。此工作流将输入查询分解为一组更简单的查询，更易于搜索引擎使用。

### 段落 21 · Page 3

**EN**

Given a query, a query re-formulating generative model, 𝐺1 = 𝐺𝑞𝑟 , generates a set of queries 𝑄1 = {𝑞1, 𝑞2...𝑞𝑛 }, which are then passed to the search engine 𝑆𝐸 to retrieve a set of ranked sources𝑆 = {𝑠1, 𝑠2, ..., 𝑠𝑚 }. The sets of sources 𝑆 are passed to a summarizing model 𝐺2 = 𝐺𝑠𝑢𝑚, which generates a summary 𝑆𝑢𝑚 𝑗 for each source in 𝑆, resulting in the summary set (𝑆𝑢𝑚 = {𝑆𝑢𝑚1, 𝑆𝑢𝑚2, ..., 𝑆𝑢𝑚𝑚 }). The summary set is passed to a response-generating model 𝐺3 = 𝐺𝑟𝑒𝑠𝑝 , which generates a cumulative response𝑟 backed by sources𝑆.

**中文**

给定一个查询，重新制定生成模型的查询 𝐺1 = 𝐺𝑞𝑟 会生成一组查询 𝑄1 = {𝑞1, 𝑞2...𝑞𝑛 }，然后将其传递到搜索引擎 𝑆𝐸 以检索一组排名源𝑆 = {𝑠1, 𝑠2, ...，𝑠𝑚}。源集 𝑆 被传递到汇总模型 𝐺2 = 𝐺𝑠𝑢𝑚，该模型为 𝑆 中的每个源生成汇总 𝑆𝑢𝑚 𝑗，从而产生汇总集 (𝑆𝑢𝑚 = {𝑆𝑢𝑚1, 𝑆𝑢𝑚2，...，𝑆𝑢𝑚𝑚}）。摘要集被传递到响应生成模型 𝐺3 = 𝐺𝑟𝑒𝑠𝑝，该模型生成由源𝑆 支持的累积响应𝑟。

### 段落 22 · Page 3

**EN**

In this work, we focus on single-turn Generative Engines, but the formulation can be extended to multi-turn Conversational Generative Engines (Appendix A). The response 𝑟 is typically a structured text with embedded citations. Citations are important given the tendency of LLMs to hallucinate information [ 10]. Specifically, consider a response 𝑟 composed of sentences {𝑙1, 𝑙2...𝑙𝑜 }. Each sentence may be backed by a set of citations that are part of the retrieved set of documents 𝐶𝑖 ⊂ 𝑆.

**中文**

在这项工作中，我们专注于单轮生成式引擎，但该公式可以扩展到多轮对话生成式引擎（附录 A）。响应𝑟通常是带有嵌入引文的结构化文本。鉴于法学硕士容易产生幻觉信息的倾向，引用很重要[10]。具体来说，考虑由句子 {𝑙1, 𝑙2...𝑙𝑜 } 组成的响应 𝑟。每个句子都可能有一组引文作为支持，这些引文是检索到的文档集的一部分𝐶𝑖 ⊂ 𝑆。

### 段落 23 · Page 3

**EN**

An ideal generative engine should ensure all statements in the response are supported by relevant citations (high citation recall), and all citations accurately support the statements they’re associated with (high citation precision) [14]. We refer readers to Figure 3 for a representative generative engine response. 2.2 Generative Engine Optimization The advent of search engines led to search engine optimization (SEO), a process to help website creators optimize their content to improve search engine rankings. Higher rankings correlate with increased visibility and website traffic.

**中文**

理想的生成式引擎应确保响应中的所有陈述都得到相关引用的支持（高引用召回率），并且所有引用都准确地支持与其相关的陈述（高引用精度）[14]。我们建议读者参考图 3，了解代表性的生成式引擎响应。 2.2 生成式引擎优化 搜索引擎的出现导致了搜索引擎优化（SEO），这是一个帮助网站创建者优化其内容以提高搜索引擎排名的过程。较高的排名与可见度和网站流量的增加相关。

### 段落 24 · Page 3

**EN**

However, traditional SEO methods are not directly applicable to Generative Engines. This is because, unlike traditional search engines, the generative model in generative engines is not limited to keyword matching, and the use of language models in ingesting source documents and response generation results in a more nuanced understanding of text documents and user query. With generative engines rapidly emerging as the primary information delivery paradigm and SEO is not directly applicable; new techniques are needed.

**中文**

然而，传统的SEO方法并不直接适用于生成式引擎。这是因为，与传统搜索引擎不同，生成式引擎中的生成模型不仅限于关键字匹配，并且在摄取源文档和响应生成中使用语言模型可以更细致GEO解文本文档和用户查询。随着生成式引擎迅速成为主要的信息传递范式，SEO 并不直接适用；需要新的技术。

### 段落 25 · Page 3

**EN**

To this end, we propose Generative Engine Optimization, a new paradigm where content creators aim to increase their visibility (or impression) in generative engine responses. We define the visibility of a website (also referred to as a citation)𝑐𝑖 in a cited response 𝑟 by the function 𝐼𝑚𝑝 (𝑐𝑖, 𝑟), which the website creator wants to maximize.

**中文**

为此，我们提出了生成式引擎优化，这是一种新范例，内容创建者旨在提高生成式引擎响应中的可见性（或印象）。我们通过函数 𝐼𝑚𝑝 (𝑐𝑖, 𝑟) 来定义被引用的响应 𝑟 中网站（也称为引用）𝑐𝑖 的可见性，网站创建者希望最大化该可见性。

### 段落 26 · Page 3

**EN**

From the generative engine’s perspective, the goal is to maximize the visibility of citations most relevant to the user query, i.e., maximize Í 𝑖 𝑓 (𝐼𝑚𝑝 (𝑐𝑖, 𝑟), 𝑅𝑒𝑙 (𝑐𝑖, 𝑞, 𝑟)), where 𝑅𝑒𝑙 (𝑐𝑖, 𝑞, 𝑟) measures the relevance of citation 𝑐𝑖 to the query 𝑞 in the context of response 𝑟 and 𝑓 is determined by the exact algorithmic design of generative engine and is a black-box function to end-users. Further, both the functions 𝐼𝑚𝑝 and 𝑅𝑒𝑙 are subjective and not well-defined yet for generative engines, and we define them next. 2.2.1 Impressions for Generative Engines.

**中文**

从生成式引擎的角度来看，目标是最大化与用户查询最相关的引文的可见性，即最大化 Í 𝑖 𝑓 (𝐼𝑚𝑝 (𝑐𝑖, 𝑟), 𝑅𝑒𝑙 (𝑐𝑖, 𝑞, 𝑟))，其中𝑅𝑒𝑙（𝑐𝑖、𝑞、𝑟）在响应𝑟和𝑓的上下文中测量引文𝑐𝑖与查询𝑞的相关性，𝑓由生成式引擎的精确算法设计确定，对于最终用户来说是一个黑盒函数。此外，函数 𝐼𝑚𝑝 和 𝑅𝑒𝑙 都是主观的，对于生成式引擎来说还没有明确定义，我们接下来定义它们。 2.2.1 生成式引擎的印象。

### 段落 27 · Page 3

**EN**

In SEO, a website’s impression (or visibility) is determined by its average ranking over a range of queries. However, generative engines’ output nature necessitates different impression metrics. Unlike search engines, Generative Engines combine information from multiple sources in a single response. Factors such as length, uniqueness, and presentation of the cited website determine the true visibility of a citation.

**中文**

在搜索引擎优化中，网站的印象（或可见度）取决于其在一系列查询中的平均排名。然而，生成式引擎的输出性质需要不同的印象指标。与搜索引擎不同，生成式引擎将多个来源的信息组合在一个响应中。引用网站的长度、独特性和呈现方式等因素决定了引文的真实可见性。

### 段落 28 · Page 3

**EN**

Thus, as illustrated in Figure 3, while a simple ranking on the response page serves as an effective metric for impression and visibility in conventional search engines, such metrics are not applicable to generative engine responses. In response to this challenge, we propose a suite of impression metrics designed with three key principles in mind: 1.) The metrics should hold relevance for creators, 2.) They should be explainable, and 3.) They should be easily comprehensible by a broad spectrum of content creators. The first of these metrics, the “Word Count” metric, is the normalized word count of sentences related to a citation.

**中文**

因此，如图 3 所示，虽然响应页面上的简单排名可作为传统搜索引擎中印象和可见度的有效度量，但此类度量不适用于生成式引擎响应。为了应对这一挑战，我们提出了一套印象指标，其设计考虑了三个关键原则：1.）这些指标应该与创作者相关，2.）它们应该是可解释的，3.）它们应该易于被广泛的内容创作者理解。第一个指标是“字数”指标，是与引文相关的句子的标准化字数。

### 段落 29 · Page 3

**EN**

Mathematically, this is defined as: 𝐼𝑚𝑝 𝑤𝑐 (𝑐𝑖, 𝑟) = Í 𝑠 ∈𝑆𝑐𝑖 |𝑠 | Í 𝑠 ∈𝑆𝑟 |𝑠 | (2) Here 𝑆𝑐𝑖 is the set of sentences citing 𝑐𝑖, 𝑆𝑟 is the set of sentences in the response, and |𝑠 | is the number of words in sentence 𝑠. In cases where a sentence is cited by multiple sources, we share the word count equally with all the citations. Intuitively, a higher word count correlates with the source playing a more important part in the answer, and thus, the user gets higher exposure to that source.

**中文**

从数学上讲，这定义为： 𝐼𝑚𝑝 𝑤𝑐 (𝑐𝑖, 𝑟) = Í 𝑠 ε𝑆𝑐𝑖 |𝑠 | Í 𝑠 ε𝑆𝑟 |𝑠 | (2) 这里𝑆𝑐𝑖是引用𝑐𝑖的句子集合，𝑆𝑟是响应中的句子集合，|𝑠 |是句子𝑠中的单词数。如果一个句子被多个来源引用，我们将与所有引用平等地共享字数。直观上，较高的字数与来源在答案中扮演更重要的角色相关，因此，用户对该来源的曝光度更高。

### Page 4

### 段落 30 · Page 4

**EN**

KDD ’24, August 25–29, 2024, Barcelona, Spain Pranjal Aggarwal et al. Figure 3: Ranking and Visibility Metrics are straightforward in traditional search engines, which list website sources in ranked order with verbatim content. However, Generative Engines generate rich, structured responses, often embedding citations in a single block interleaved with each other. This makes ranking and visibility nuanced and multi-faceted. Further, unlike search engines, where significant research has been conducted on improving visibility, optimizing visibility in generative engine responses remains unclear.

**中文**

KDD '24，2024 年 8 月 25-29 日，西班牙巴塞罗那 Pranjal Aggarwal 等人。图 3：排名和可见性指标在传统搜索引擎中非常简单，它按排名顺序列出网站源并逐字内容。然而，生成式引擎会生成丰富的、结构化的响应，通常将引文嵌入到彼此交错的单个块中。这使得排名和可见度变得细致入微且多方面。此外，与搜索引擎不同，搜索引擎在提高可见性方面进行了大量研究，但优化生成式引擎响应的可见性仍不清楚。

### 段落 31 · Page 4

**EN**

To address these challenges, our black-box optimization framework proposes a series of well-designed impression metrics that creators can use to gauge and optimize their website’s performance and also allows the creator to define their impression metrics.

**中文**

为了应对这些挑战，我们的黑盒优化框架提出了一系列精心设计的印象指标，创建者可以使用这些指标来衡量和优化其网站的性能，并允许创建者定义其印象指标。

### 段落 32 · Page 4

**EN**

However, since “Word Count” is not impacted by the ranking of the citations (whether it appears first, for example), we propose a position-adjusted count that reduces the weight by an exponentially decaying function of the citation position: 𝐼𝑚𝑝 𝑝𝑤𝑐 (𝑐𝑖, 𝑟) = Í 𝑠 ∈𝑆𝑐𝑖 |𝑠 | · 𝑒 − 𝑝𝑜𝑠 (𝑠 ) |𝑆 | Í 𝑠 ∈𝑆𝑟 |𝑠 | (3) Intuitively, sentences that appear first in the response are more likely to be read, and the exponent term in definition 𝐼𝑚𝑝 𝑝𝑤𝑐 gives higher weightage to such citations. Thus, a website cited at the top may have a higher impression despite having a lower word count than a website cited in the middle or end of the response.

**中文**

然而，由于“字数”不受引用排名的影响（例如，是否出现在前面），因此我们提出了一种位置调整计数，通过引用位置的指数衰减函数来减少权重： 𝐼𝑚𝑝 𝑝𝑤𝑐 (𝑐𝑖, 𝑟) = Í 𝑠 ε𝑆𝑐𝑖 |𝑠 | · 𝑒 − 𝑝𝑜𝑠 (𝑠 ) |𝑆 | Í 𝑠 ε𝑆𝑟 |𝑠 | (3) 直观上，回答中首先出现的句子更有可能被阅读，并且定义中的指数项𝐼𝑚𝑝 𝑝𝑤𝑐 赋予此类引用更高的权重。因此，尽管字数较少，但顶部引用的网站可能比响应中间或末尾引用的网站具有更高的印象。

### 段落 33 · Page 4

**EN**

Further, the choice of exponentially decaying function is motivated by several studies showing click-through rates follow a power-law as a function of ranking in search engines [7, 8]. While the above impression metrics are objective and well-grounded, they ignore the subjective aspects of the impact of citations on the user’s attention.

**中文**

此外，指数衰减函数的选择是由几项研究推动的，这些研究表明点击率遵循幂律作为搜索引擎排名的函数[7, 8]。虽然上述印象指标是客观且有根据的，但它们忽略了引用对用户注意力影响的主观方面。

### 段落 34 · Page 4

**EN**

To address this, we propose the "Subjective Impression" metric, which incorporates facets such as the relevance of the cited material to the user query, influence of the citation, uniqueness of the material presented by a citation, subjective position, subjective count, probability of clicking the citation, and diversity in the material presented. We use G-Eval [15], the current state-of-the-art for evaluation with LLMs, to measure each of these sub-metrics. 2.2.2 Generative Engine Optimization methods for website. To improve impression metrics, content creators must make changes to their website content.

**中文**

为了解决这个问题，我们提出了“主观印象”指标，它包含了诸如被引用材料与用户查询的相关性、引文的影响、引文所呈现材料的独特性、主观立场、主观计数、点击引文的概率以及所呈现材料的多样性等方面。我们使用 G-Eval [15]（目前最先进的法学硕士评估方法）来衡量每个子指标。 2.2.2 网站生成式引擎优化方法。为了提高印象指标，内容创建者必须对其网站内容进行更改。

### 段落 35 · Page 4

**EN**

We present several generative engineagnostic strategies, referred to as Generative Engine Optimization methods (GEO). Mathematically, every GEO method is a function 𝑓 : 𝑊 → 𝑊 ′ 𝑖 , where 𝑊 is the initial web content, and 𝑊 ′ is the modified content after applying the GEO method. The modifications can range from simple stylistic alterations to incorporating new content in a structured format. A well-designed GEO is equivalent to a black-box optimization method that, without knowing the exact algorithmic design of generative engines, can increase the website’s visibility and implement textual modifications to𝑊 independent of the exact queries.

**中文**

我们提出了几种与生成式引擎无关的策略，称为生成式引擎优化方法（GEO）。从数学上讲，每个 GEO 方法都是一个函数 𝑓 : 𝑊 → 𝑊 ′ 𝑖，其中 𝑊 是初始网页内容，𝑊 ′ 是应用 GEO 方法后修改的内容。修改的范围可以从简单的风格改变到以结构化格式合并新内容。精心设计的 GEO 相当于一种黑盒优化方法，在不知道生成式引擎的确切算法设计的情况下，可以提高网站的可见性，并实现独立于确切查询的文本修改。

### 段落 36 · Page 4

**EN**

For our experiments, we apply Generative Engine Optimization methods on website content using a large language model, prompted to perform specific stylistic and content changes to the website. In particular, based on the GEO method defining a specific set of desired characteristics, the source content is modified accordingly. We propose and evaluate several such methods: 1: Authoritative: Modifies text style of the source content to be more persuasive and authoritative,2. Statistics Addition: Modifies content to include quantitative statistics instead of qualitative discussion, wherever possible, 3.

**中文**

在我们的实验中，我们使用大型语言模型对网站内容应用生成式引擎优化方法，提示对网站执行特定的风格和内容更改。特别地，基于定义一组特定的期望特征的GEO方法，源内容被相应地修改。我们提出并评估了几种这样的方法：1：权威：修改源内容的文本风格，使其更具说服力和权威性，2。统计添加：尽可能修改内容以包括定量统计而不是定性讨论，3.

### 段落 37 · Page 4

**EN**

Keyword Stuffing:Modifies content to include more keywords from the query, as expected in classical SEO optimization. 4. Cite Sources & 5. Quotation Addition: Adds relevant citations and quotations from credible sources respectively, 6.) 6. Easy-to-Understand: Simplifies the language of website, while 7. Fluency Optimization improves the fluency of website text. 8. Unique Words & 9. Technical Terms: involves adding unique and technical terms respectively wherever possible, These methods cover diverse general strategies that website owners can implement quickly and use regardless of the website content.

**中文**

关键字填充：修改内容以包含查询中的更多关键字，正如经典 SEO 优化中所预期的那样。 4. 引用来源 & 5. 引用添加：分别添加相关引用和来自可靠来源的引用，6.) 6. 易于理解：简化网站语言，7. 流畅性优化提高网站文本的流畅性。 8.独特词语和9.技术术语：涉及尽可能分别添加独特和技术术语，这些方法涵盖了网站所有者可以快速实施和使用的各种通用策略，无论网站内容如何。

### 段落 38 · Page 4

**EN**

Further, except for methods 3, 4, and 5, the remaining methods enhance the presentation of existing content to increase its persuasiveness or appeal to the generative engine, without requiring extra content. On the other hand, methods 3,4 and 5 may

**中文**

此外，除了方法3、4和5之外，其余方法增强了现有内容的呈现，以增加其说服力或对生成式引擎的吸引力，而不需要额外的内容。另一方面，方法 3,4 和 5 可能

### Page 5

### 段落 39 · Page 5

**EN**

GEO: Generative Engine Optimization KDD ’24, August 25–29, 2024, Barcelona, Spain require some form of additional content. To analyze the performance gain of our methods, for each input user query, we randomly select one source website to be optimized and apply each of the GEO methods separately on the same source. We refer readers to Appendix B.4 for more details on GEO methods. 3 EXPERIMENTAL SETUP 3.1 Evaluated Generative Engine In accordance with previous works [14], we use a 2-step setup for Generative Engine design.

**中文**

GEO：生成式引擎优化 KDD '24，2024 年 8 月 25 日至 29 日，西班牙巴塞罗那，需要某种形式的附加内容。为了分析我们方法的性能增益，对于每个输入用户查询，我们随机选择一个要优化的源网站，并在同一源上分别应用每种 GEO 方法。我们建议读者参阅附录 B.4，了解有关 GEO 方法的更多详细信息。 3 实验设置 3.1 评估生成式引擎 根据以前的工作[14]，我们使用两步设置进行生成式引擎设计。

### 段落 40 · Page 5

**EN**

The first step involves fetching relevant sources for input query, followed by a second step where an LLM generates a response based on the fetched sources. Similar to prevous works, we do not use summarization and provide the whole response for each source. Due to context length limitations and quadratic scaling cost based on the context size of transformer models, only the top 5 sources are fetched from the Google search engine for every query. The setup closely mimics the workflow used in previous works and the general design adopted by commercial GEs such as you.com and perplexity.ai.

**中文**

第一步涉及获取输入查询的相关来源，第二步是法学硕士根据获取的来源生成响应。与以前的工作类似，我们不使用摘要，而是为每个来源提供完整的响应。由于上下文长度限制和基于 Transformer 模型上下文大小的二次缩放成本，每次查询仅从 Google 搜索引擎获取前 5 个源。该设置非常模仿以前作品中使用的工作流程以及 you.com 和 perplexity.ai 等商业 GE 采用的总体设计。

### 段落 41 · Page 5

**EN**

The answer is then generated by the gpt3.5-turbo model [ 20] using the same prompt as prior work [14]. We sample 5 different responses at temperature=0.7, to reduce statistical deviations. Further in Section C.1, we evaluate the sameGenerative Engine Optimization methods on Perplexity.ai, which is a commercially deployed generative engine, highlighting the generalizability of our proposed Generative Engine Optimization methods.

**中文**

然后，gpt3.5-turbo 模型 [20] 使用与之前的工作 [14] 相同的提示生成答案。我们在温度 = 0.7 时对 5 个不同的响应进行采样，以减少统计偏差。在 C.1 节中，我们在 Perplexity.ai 上评估了相同的生成式引擎优化方法，Perplexity.ai 是一个商业部署的生成式引擎，强调了我们提出的生成式引擎优化方法的通用性。

### 段落 42 · Page 5

**EN**

3.2 Benchmark : GEO-bench Since there is currently no publicly available dataset containing Generative Engine related queries, we curateGEO-bench, a benchmark consisting of 10K queries from multiple sources, repurposed for generative engines, along with synthetically generated queries. The benchmark includes queries from nine different sources, each further categorized based on their target domain, difficulty, query intent, and other dimensions. Datasets: 1. MS Macro, 2. ORCAS-1, and 3. Natural Questions: [1, 6, 13] These datasets contain real anonymized user queries from Bing and Google Search Engines.

**中文**

3.2 基准：GEO-bench 由于目前没有包含生成式引擎相关查询的公开数据集，因此我们策划了 GEO-bench，这是一个由来自多个来源的 10K 查询组成的基准，重新用于生成式引擎以及综合生成的查询。该基准包括来自九个不同来源的查询，每个来源都根据其目标领域、难度、查询意图和其他维度进一步分类。数据集：1. MS Macro、2. ORCAS-1 和 3. Natural Questions：[1,6,13] 这些数据集包含来自 Bing 和 Google 搜索引擎的真实匿名用户查询。

### 段落 43 · Page 5

**EN**

These three collectively represent the common set of datasets that are used in search engine related research. However, Generative Engines will be posed with far more difficult and specific queries with the intent of synthesizing answers from multiple sources instead of searching for them. To this end, we repurpose several other publicly available datasets: 4. AllSouls: This dataset contains essay questions from "All Souls College, Oxford University. " The queries in this dataset require Generative Engines to perform appropriate reasoning to aggregate information from multiple sources. 5.

**中文**

这三个共同代表了搜索引擎相关研究中使用的通用数据集。然而，生成式引擎将面临更加困难和具体的查询，其目的是从多个来源合成答案，而不是搜索它们。为此，我们重新利用了其他几个公开可用的数据集： 4. AllSouls：该数据集包含来自“牛津大学 All Souls 学院”的问答题。该数据集中的查询需要生成式引擎执行适当的推理来聚合来自多个来源的信息。 5.

### 段落 44 · Page 5

**EN**

LIMA: [25] contains challenging questions requiring Generative Engines to not only aggregate information but also perform suitable reasoning to answer the question (e.g., writing a short poem, python code.). 6. Davinci-Debtate [14] contains debate questions generated for testing Generative Engines. 7. Perplexity.ai Discover 2: These queries are sourced from Perplexity.ai’s Discover section, which is 2https://www.perplexity.ai/discover an updated list of trending queries on the platform. 8. ELI-53: This dataset contains questions from the ELI5 subreddit, where users ask complex questions and expect answers in simple, layman’s terms. 9.

**中文**

LIMA：[25] 包含具有挑战性的问题，要求生成式引擎不仅要聚合信息，还要执行适当的推理来回答问题（例如，写一首短诗、Python 代码）。 6. Davinci-Debtate [14] 包含为测试生成式引擎而生成的辩论问题。 7. Perplexity.ai Discover 2：这些查询来自 Perplexity.ai 的 Discover 部分，该部分是 2https://www.perplexity.ai/discover 平台上趋势查询的更新列表。 8. ELI-53：该数据集包含来自 ELI5 subreddit 的问题，用户在其中提出复杂的问题并期望以简单、通俗易懂的方式得到答案。 9.

### 段落 45 · Page 5

**EN**

GPT-4 Generated Queries: To supplement diversity in query distribution, we prompt GPT-4 [21] to generate queries ranging from various domains (e.g., science, history) and based on query intent (e.g., navigational, transactional) and based on difficulty and scope of generated response (e.g., open-ended, fact-based). . Our benchmark comprises 10K queries divided into 8K, 1K, and 1K for train, validation, and test splits, respectively. We preserve the real-world query distribution, with our benchmark containing 80% informational queries and 10% each for transactional and navigational queries.

**中文**

GPT-4 生成的查询：为了补充查询分布的多样性，我们提示 GPT-4 [21] 生成来自不同领域（例如科学、历史）并基于查询意图（例如导航、事务）以及生成响应的难度和范围（例如开放式、基于事实）的查询。。我们的基准测试包括 10K 个查询，分为 8K、1K 和 1K，分别用于训练、验证和测试拆分。我们保留了真实世界的查询分布，我们的基准测试包含 80% 的信息查询，以及事务和导航查询各 10%。

### 段落 46 · Page 5

**EN**

Each query is augmented with the cleaned text content of the top 5 search results from the Google search engine. Tags. Optimizing website content often requires targeted changes based on the task’s domain. Additionally, a user of Generative Engine Optimization may need to identify an appropriate method for only a subset of queries, considering multiple factors such as domain, user intent, and query nature. To facilitate this, we tag each query with one of seven different categories. For tagging, we employ the GPT-4 model and manually verify high recall and precision on the test split.

**中文**

每个查询都使用来自 Google 搜索引擎的前 5 个搜索结果的经过清理的文本内容进行扩充。标签。优化网站内容通常需要根据任务领域进行有针对性的更改。此外，生成式引擎优化的用户可能需要考虑多个因素（例如领域、用户意图和查询性质），仅针对查询子集确定适当的方法。为了促进这一点，我们用七个不同类别之一来标记每个查询。对于标记，我们采用 GPT-4 模型并手动验证测试拆分的高召回率和精度。

### 段落 47 · Page 5

**EN**

Overall, GEO-bench consists of queries from 25 diverse domains such as Arts, Health, and Games; it features a range of query difficulties from simple to multi-faceted; includes 9 different types of queries such as informational and transactional; and encompasses 7 different categorizations. Owing to its specially designed high diversity, the size of the benchmark, and its real-world nature,GEObench is a comprehensive benchmark for evaluating Generative Engines and serves as a standard testbed for assessing them for various purposes in this and future works. We provide more details about GEO-bench in Appendix B.2.

**中文**

总体而言，GEO-bench 包含来自 25 个不同领域的查询，例如艺术、健康和游戏；它具有从简单到多方面的一系列查询困难；包括 9 种不同类型的查询，例如信息查询和事务查询；并包含 7 个不同的类别。由于其专门设计的高度多样性、基准的规模及其现实世界的性质，GEObench 是一个用于评估生成式引擎的综合基准，并可作为在本次工作和未来工作中评估它们用于各种目的的标准测试平台。我们在附录 B.2 中提供了有关 GEO-bench 的更多详细信息。

### 段落 48 · Page 5

**EN**

3.3 GEO Methods We evaluate 9 different proposed GEO methods as described in Section 2.2.2. We compare them with a baseline, which measures the impression metric of unmodified website sources. We evaluate methods on the complete GEO-bench test split. Further, to reduce variance in results, we run our experiments on five different random seeds and report the average. 3.4 Evaluation Metrics We utilize the impression metrics as defined in Section 2.2.1. Specifically, we employ two impression metrics: 1. Position-Adjusted Word Count, which combines word count and position count.

**中文**

3.3 GEO 方法 我们评估了 2.2.2 节中描述的 9 种不同的建议 GEO 方法。我们将它们与基线进行比较，该基线测量未经修改的网站源的印象指标。我们在完整的 GEO-bench 测试拆分上评估方法。此外，为了减少结果的方差，我们对五个不同的随机种子进行实验并报告平均值。 3.4 评估指标 我们使用第 2.2.1 节中定义的印象指标。具体来说，我们采用两个印象指标： 1. 位置调整字数，它结合了字数和位置计数。

### 段落 49 · Page 5

**EN**

To analyze the effect of individual components, we also report scores on the two sub-metrics separately. 2. Subjective Impression, which is a subjective metric encompassing seven different aspects: 1) relevance of the cited sentence to the user query, 2) influence of the citation, assessing the extent to which the generated response relies on the citation, 3) uniqueness of the material presented by a citation, 4) subjective position, gauging the prominence of the positioning of source from the user’s viewpoint, 5) subjective count, measuring the amount of content presented from the 3https://huggingface.co/datasets/eli5_category

**中文**

为了分析各个组成部分的影响，我们还分别报告两个子指标的分数。 2. 主观印象，这是一个主观指标，包含七个不同方面：1) 被引用句子与用户查询的相关性；2) 引文的影响力，评估生成的响应对引文的依赖程度；3) 引文呈现的材料的独特性；4) 主观立场，从用户的角度衡量来源定位的突出程度；5) 主观计数，衡量从引文呈现的内容量。 3https://huggingface.co/datasets/eli5_category

### Page 6

### 段落 50 · Page 6

**EN**

KDD ’24, August 25–29, 2024, Barcelona, Spain Pranjal Aggarwal et al. Method Position-Adjusted Word Count Subjective Impression Word Position Overall Rel. Infl. Unique Div. FollowUp Pos.

**中文**

KDD '24，2024 年 8 月 25-29 日，西班牙巴塞罗那 Pranjal Aggarwal 等人。方法 位置调整字数 主观印象 字位置 整体相关。膨胀。独特的部门。跟进职位。

### 段落 51 · Page 6

**EN**

Count Average Performance without Generative Engine Optimization No Optimization 19.5 19 .3 19 .3 19 .3 19 .3 19 .3 19 .3 19 .3 19 .3 19 .3 19 .3 Non-Performing Generative Engine Optimization methods Keyword Stuffing 17.8 17 .7 17 .7 19 .8 19 .1 20 .5 20 .4 20 .3 20 .5 20 .4 20 .2 Unique Words 20.7 20 .5 20 .5 20 .5 20 .1 19 .9 20 .4 20 .2 20 .7 20 .2 20 .4 High-Performing Generative Engine Optimization methods Easy-to-Understand 22.2 22 .4 22 .0 20 .2 21 .0 20 .0 20 .1 20 .1 20 .9 19 .9 20 .5 Authoritative 21.8 21 .3 21 .3 22 .3 22 .1 22 .4 23 .1 22 .2 23 .1 22 .7 22 .9 Technical Terms 23.1 22 .7 22 .7 20 .9 21 .7 20 .5 21 .2 20 .8 21 .9 20

**中文**

计数未生成式引擎优化的平均性能 无优化 19.5 19 .3 19 .3 19 .3 19 .3 19 .3 19 .3 19 .3 19 .3 19 .3 19 .3 表现不佳的生成式引擎优化方法 关键字堆砌 17.8 17 .7 17 .7 19 .8 19 .1 20 .5 20 .4 20 .3 20 .5 20 .4 20 .2 独特单词 20.7 20 .5 20 .5 20 .5 20 .1 19 .9 20 .4 20 .2 20 .7 20 .2 20 .4 高性能生成式引擎优化方法 通俗易懂 22.2 22 .4 22 .0 20 .2 21 .0 20 .0 20 .1 20 .1 20 .9 19 .9 20 .5 权威 21.8 21 .3 21 .3 22 .3 22 .1 22 .4 23 .1 22 .2 23 .1 22 .7 22 .9 技术术语 23.1 22 .7 22 .7 20 .9 21 .7 20 .5 21 .2 20 .8 21 .9 20

### 段落 52 · Page 6

**EN**

.8 21 .4 Fluency Optimization 25.1 24 .6 24 .7 21 .1 22 .9 20 .4 21 .6 21 .0 22 .4 21 .1 21 .9 Cite Sources 24.9 24 .5 24 .6 21 .4 22 .5 21 .0 21 .6 21 .2 22 .2 20 .7 21 .9 Quotation Addition 27.8 27 .3 27.2 23.8 25 .4 23 .9 24 .4 22 .9 24 .9 23 .2 24.7 Statistics Addition 25.9 25 .4 25 .2 22 .5 24 .5 23 .0 23 .3 21 .6 24 .2 23 .0 23 .7 Table 1: Absolute impression metrics of GEO methods on GEO-bench.

**中文**

.8 21 .4 流畅度优化 25.1 24 .6 24 .7 21 .1 22 .9 20 .4 21 .6 21 .0 22 .4 21 .1 21 .9 引用来源 24.9 24 .5 24 .6 21 .4 22 .5 21 .0 21 .6 21 .2 22 .2 20 .7 21 .9 报价添加 27.8 27 .3 27.2 23.8 25 .4 23 .9 24 .4 22 .9 24 .9 23 .2 24.7 统计添加 25.9 25 .4 25 .2 22 .5 24 .5 23 .0 23 .3 21 .6 24 .2 23 .0 23 .7 表 1：GEO-bench 上 GEO 方法的绝对印象指标。

### 段落 53 · Page 6

**EN**

Performance Measured on Two metrics and their sub-metrics. Compared to baselines, simple methods like Keyword Stuffing traditionally used in SEO don’t perform well. However, our proposed methods such as Statistics Addition and Quotation Addition show strong performance improvements across all metrics. The best methods improve upon baseline by 41% and 28% on Position-Adjusted Word Count and Subjective Impression respectively. For readability, Subjective Impression scores are normalized with respect to Position-Adjusted Word Count resulting in similar baseline scores.

**中文**

根据两个指标及其子指标衡量绩效。与基线相比，SEO 中传统使用的关键字填充等简单方法效果不佳。然而，我们提出的方法（例如统计加法和报价加法）在所有指标上都显示出强大的性能改进。最好的方法在位置调整字数和主观印象上分别比基线提高了 41% 和 28%。为了便于阅读，主观印象分数根据位置调整字数进行标准化，从而产生相似的基线分数。

### 段落 54 · Page 6

**EN**

citation as perceived by the user, 6) likelihood of the user clicking the citation, and 7) diversity of the material presented. These submetrics assess diverse aspects that content creators can target to improve one or more areas effectively. Each sub-metric is evaluated using GPT-3.5, following a methodology akin to that described in G-Eval [15]. In G-Eval, a form-based evaluation template is provided to the language model, along with a GE generated response with citations. The model outputs a score (computed by sampling multiple times) for each citation.

**中文**

用户感知到的引文，6) 用户点击引文的可能性，以及 7) 所呈现材料的多样性。这些子指标评估内容创建者可以针对有效改进一个或多个领域的各个方面。每个子指标均使用 GPT-3.5 进行评估，遵循类似于 G-Eval [15] 中描述的方法。在 G-Eval 中，向语言模型提供基于表单的评估模板，以及 GE 生成的带引文的响应。该模型为每次引用输出一个分数（通过多次采样计算得出）。

### 段落 55 · Page 6

**EN**

However, since G-Eval scores are poorly calibrated, we normalize them to have the same mean and variance as Position-Adjusted Word Count to enable a fair and meaningful comparison. We provide the exact templates used in Appendix B.3. Furthermore, all impression metrics are normalized by multiplying them with a constant factor so that the sum of the impressions of all citations in a response equals 1. In our analysis, we compare methods by calculating the relative improvement in impression. For an initial generated response 𝑟 from sources 𝑆𝑖 ∈ { 𝑠1, . . .

**中文**

然而，由于 G-Eval 分数校准不佳，我们将其标准化为与位置调整字数具有相同的均值和方差，以实现公平且有意义的比较。我们提供了附录 B.3 中使用的确切模板。此外，所有印象指标都通过乘以常数因子进行归一化，以便响应中所有引用的印象之和等于 1。在我们的分析中，我们通过计算印象的相对改进来比较方法。对于来自源 𝑆𝑖 ∈ { 𝑠1, . 的初始生成响应 𝑟。。。

### 段落 56 · Page 6

**EN**

, 𝑠𝑚 }, and a modified response 𝑟 ′, the relative improvement in impression for each source 𝑠𝑖 is measured as: 𝐼𝑚𝑝𝑟𝑜𝑣𝑒𝑚𝑒𝑛𝑡 𝑠𝑖 = 𝐼𝑚𝑝𝑠𝑖 (𝑟 ′) − 𝐼𝑚𝑝𝑠𝑖 (𝑟 ) 𝐼𝑚𝑝𝑠𝑖 (𝑟 ) × 100 (4) The modified response 𝑟 ′ is produced by applying the GEO method being evaluated to one of the sources 𝑠𝑖. The source 𝑠𝑖 selected for optimization is chosen randomly but remains constant for a particular query across all GEO methods. 4 RESULTS We evaluate various Generative Engine Optimization methods designed to optimize website content for better visibility in Generative Engine responses, compared against a baseline with no optimization.

**中文**

, 𝑠𝑚 } 和修改后的响应 𝑟 ′，每个来源 𝑠𝑖 的印象相对改善测量如下： 𝐼𝑚𝑝𝑟𝑜𝑣𝑒𝑚𝑒𝑛𝑡 𝑠𝑖 = 𝐼𝑚𝑝𝑠𝑖 (𝑟 ′) − 𝐼𝑚𝑝𝑠𝑖 (𝑟 ) 𝐼𝑚𝑝𝑠𝑖 (𝑟 ) × 100 (4) 修改响应 𝑟 ′ 是通过将正在评估的 GEO 方法应用于其中之一来生成的来源𝑠𝑖。选择用于优化的源𝑠𝑖是随机选择的，但对于所有 GEO 方法中的特定查询保持不变。 4 结果 我们评估了各种旨在优化网站内容的生成式引擎优化方法，以便与未优化的基线相比，在生成式引擎响应中获得更好的可见性。

### 段落 57 · Page 6

**EN**

Our evaluation used GEO-bench, a diverse benchmark of user queries from multiple domains and settings. Performance was measured using two metrics: Position-Adjusted Word Count and Subjective Impression. The former considers word count and citation position in the GE’s response, while the latter computes multiple subjective factors, giving an overall impression score. Table 1 details the absolute impression metrics of different methods on multiple metrics. The results reveal that our GEO methods consistently outperform the baseline across all metrics on GEObench.

**中文**

我们的评估使用了 GEO-bench，这是来自多个域和设置的用户查询的多样化基准。使用两个指标来衡量绩效：位置调整字数和主观印象。前者考虑 GE 回复中的字数和引用位置，而后者则计算多个主观因素，给出总体印象分数。表1详细介绍了不同方法在多个指标上的绝对展示指标。结果表明，我们的 GEO 方法在 GEObench 上的所有指标上始终优于基线。

### 段落 58 · Page 6

**EN**

This shows the robustness of these methods to varying queries, yielding significant improvements despite query diversity. Specifically, our top-performing methods, Cite Sources, Quotation Addition, and Statistics Addition, achieved a relative improvement of 30-40% on the Position-Adjusted Word Count metric and 15-30% on the Subjective Impression metric.

**中文**

这显示了这些方法对不同查询的鲁棒性，尽管查询存在多样性，但仍产生了显着的改进。具体来说，我们表现最好的方法，即引用来源、引文添加和统计添加，在位置调整字数指标上实现了 30-40% 的相对改进，在主观印象指标上实现了 15-30% 的相对改进。

### 段落 59 · Page 6

**EN**

These methods, involving adding relevant statistics (Statistics Addition), incorporating credible quotes (Quotation Addition), and including citations from reliable sources (Cite Sources) in the website content, require minimal changes but significantly improve visibility in GE responses, enhancing both the credibility and richness of the content. Interestingly, stylistic changes such as improving fluency and readability of the source text (Fluency Optimization and Easy-to- Understand) also resulted in a significant visibility boost of 15-30%. This suggests that Generative Engines value not only content but also information presentation.

**中文**

这些方法涉及添加相关统计数据（统计添加）、纳入可信引用（引用添加）以及在网站内容中包含来自可靠来源的引用（引用来源），只需进行最少的更改，但可显着提高 GE 回复中的可见性，从而增强内容的可信度和丰富性。有趣的是，诸如提高源文本的流畅性和可读性（流畅性优化和易于理解）等文体变化也导致可见性显着提升 15-30%。这表明生成式引擎不仅重视内容，还重视信息呈现。

### Page 7

### 段落 60 · Page 7

**EN**

GEO: Generative Engine Optimization KDD ’24, August 25–29, 2024, Barcelona, Spain Method Relative Improvement (%) in Visibility Rank-1 Rank-2 Rank-3 Rank-4 Rank-5 Authoritative -6.0 4.1 -0.6 12.6 6.1 Fluency Opt. -2.0 5.2 3.6 -4.4 2.2 Cite Sources -30.3 2.5 20.4 15.5 115.1 Quotation Addition -22.9 -7.0 3.5 25.1 99.7 Statistics Addition -20.6 -3.9 8.1 10.0 97.9 Table 2: Visibility changes through GEO methods for sources with different Rankings in Search Engine. GEO is especially helpful for lower ranked websites. Method Top Performing Tags Rank-1 Rank-2 Rank-3 Authoritative Debate History Science Fluency Opt.

**中文**

GEO：生成式引擎优化 KDD '24，2024 年 8 月 25-29 日，西班牙巴塞罗那 方法 可见性相对改进 (%) Rank-1 Rank-2 Rank-3 Rank-4 Rank-5 权威 -6.0 4.1 -0.6 12.6 6.1 流畅度选项。 -2.0 5.2 3.6 -4.4 2.2 引用来源 -30.3 2.5 20.4 15.5 115.1 引用添加 -22.9 -7.0 3.5 25.1 99.7 统计添加 -20.6 -3.9 8.1 10.0 97.9 表 2：通过 GEO 方法对来源的可见性变化在搜索引擎中具有不同的排名。 GEO 对于排名较低的网站特别有帮助。方法 表现最佳标签 排名 1 排名 2 排名 3 权威辩论 历史 科学流利程度 选择。

### 段落 61 · Page 7

**EN**

Business Science Health Cite Sources Statement Facts Law & Gov. Quotation AdditionPeople & Society Explanation History Statistics Addition Law & Gov. Debate Opinion Table 3: Top Performing categories for each of the GEO methods. Website-owners can choose relevant GEO strategy based on their target domain. Further, given generative models are often designed to follow instructions, one would expect a more persuasive and authoritative tone in website content to boost visibility. However, we find no significant improvement, demonstrating that Generative Engines are already somewhat robust to such changes.

**中文**

商业科学 健康 引用来源 声明事实 法律与政府 引文添加 人民与社会 解释历史 统计数据 添加 法律与政府辩论意见 表 3：每种 GEO 方法的最佳表现类别。网站所有者可以根据自己的目标域选择相关的GEO策略。此外，鉴于生成模型通常被设计为遵循指令，人们会期望网站内容具有更具说服力和权威的语气，以提高可见性。然而，我们没有发现显着的改进，这表明生成式引擎已经对此类变化具有一定的鲁棒性。

### 段落 62 · Page 7

**EN**

This highlights the need for website owners to focus on improving content presentation and credibility. Finally, we evaluate keyword stuffing, i.e., adding more relevant keywords to website content. While widely used for Search Engine Optimization, we find such methods offer little to no improvement on generative engine’s responses. This underscores the need for website owners to rethink optimization strategies for generative engines, as techniques effective in search engines may not translate to success in this new paradigm.

**中文**

这凸显了网站所有者需要专注于提高内容呈现和可信度。最后，我们评估关键字堆砌，即向网站内容添加更多相关的关键字。虽然广泛用于搜索引擎优化，但我们发现此类方法对生成式引擎的响应几乎没有改善。这强调了网站所有者需要重新考虑生成式引擎的优化策略，因为在搜索引擎中有效的技术可能无法在这种新范式中转化为成功。

### 段落 63 · Page 7

**EN**

5 ANALYSIS 5.1 Domain-Specific Generative Engine Optimizations In Section 4, we presented the improvements achieved by GEO across the entirety of the GEO-bench benchmark. However, in real-world SEO scenarios, domain-specific optimizations are often applied. With this in mind, and considering that we provide categories for every query in GEO-bench, we delve deeper into the performance of various GEO methods across these categories. Table 3 provides a detailed breakdown of the categories where our GEO methods have proven to be most effective. A careful analysis of these results reveals several intriguing observations.

**中文**

5 分析 5.1 特定领域的生成式引擎优化 在第 4 节中，我们介绍了 GEO 在整个 GEO-bench 基准测试中取得的改进。然而，在现实的 SEO 场景中，经常应用特定领域的优化。考虑到这一点，并考虑到我们为 GEO-bench 中的每个查询提供类别，我们更深入地研究了这些类别中各种 GEO 方法的性能。表 3 详细列出了我们的 GEO 方法已被证明最有效的类别。对这些结果的仔细分析揭示了一些有趣的观察结果。

### 段落 64 · Page 7

**EN**

For instance, Authoritative significantly improves performance in debatestyle questions and queries related to the “historical” domain. This aligns with our intuition, as a more persuasive form of writing is likely to hold more value in debates. Similarly, the addition of citations through Cite Sources is particularly beneficial for factual questions, likely because citations provide a source of verification for the facts presented, thereby enhancing the credibility of the response. The effectiveness of different GEO methods varies across domains.

**中文**

例如，权威显着提高了与“历史”领域相关的辩论式问题和查询的性能。这符合我们的直觉，因为更具说服力的写作形式可能在辩论中具有更大的价值。同样，通过引用来源添加引文对于事实问题特别有益，可能是因为引文为所呈现的事实提供了验证来源，从而提高了答复的可信度。不同 GEO 方法的有效性因领域而异。

### 段落 65 · Page 7

**EN**

For example, as shown in row 5 of Table 3, domains such as ‘Law & Government’ and question types like ‘Opinion’ benefit significantly from the addition of relevant statistics in the website content, as implemented by Statistics Addition. This suggests that data-driven evidence can enhance the visibility of a website in particular contexts. The method Quotation Addition is most effective in the ‘People & Society, ’ ‘Explanation, ’ and ‘History’ domains.

**中文**

例如，如表 3 第 5 行所示，“法律与政府”等领域和“意见”等问题类型显着受益于在网站内容中添加相关统计数据，如统计添加所实施的那样。这表明数据驱动的证据可以提高网站在特定环境下的可见性。引用添加方法在“人与社会”、“解释”和“历史”领域最有效。

### 段落 66 · Page 7

**EN**

This could be because these domains often fluency statistics citation quotes fluency statistics citation quotes 22.4% 35.8% 34.4% 33.0% 35.8% 27.0% 30.3% 35.4% 34.4% 30.3% 19.1% 20.1% 33.0% 35.4% 20.1% 30.3% 31.4% 32.1% 26.0% 29.7% Average Improvement 20 22 24 26 28 30 32 34 Figure 4: Relative Improvement on using combination of GEO strategies. Using Fluency Optimization and Statistics Addition in conjunction results in maximum performance. The rightmost column shows using Fluency Optimization with other strategies is most beneficial.

**中文**

这可能是因为这些域经常 流畅性统计 引文引用 流畅性统计引文引用 22.4% 35.8% 34.4% 33.0% 35.8% 27.0% 30.3% 35.4% 34.4% 30.3% 19.1% 20.1% 33.0% 35.4% 20.1% 30.3% 31.4% 32.1% 26.0% 29.7% 平均改进 20 22 24 26 28 30 32 34 图 4：使用 GEO 策略组合的相对改进。结合使用流畅度优化和统计添加可以实现最佳性能。最右栏显示将流畅度优化与其他策略结合使用是最有益的。

### 段落 67 · Page 7

**EN**

involve personal narratives or historical events, where direct quotes can add authenticity and depth to the content. Overall, our analysis suggests that website owners should strive towards making domain-specific targeted adjustments to their websites for higher visibility. 5.2 Optimization of Multiple Websites In the evolving landscape of Generative Engines, GEO methods are expected to become widely adopted, leading to a scenario where all source contents are optimized using GEO. To understand the implications, we conducted an evaluation of GEO methods by optimizing all source contents simultaneously, with results presented in Table 2.

**中文**

涉及个人叙述或历史事件，直接引用可以增加内容的真实性和深度。总体而言，我们的分析表明，网站所有者应努力对其网站进行针对特定领域的有针对性的调整，以获得更高的可见度。 5.2 多个网站的优化 在生成式引擎不断发展的格局中，GEO 方法预计将被广泛采用，从而导致所有源内容都使用 GEO 进行优化的场景。为了理解其含义，我们通过同时优化所有源内容对 GEO 方法进行了评估，结果如表 2 所示。

### 段落 68 · Page 7

**EN**

A key observation is the differential impact of GEO on websites based on their Search Engine Results Pages (SERP) ranking. Notably, lower-ranked websites, which typically struggle for visibility, benefit significantly more from GEO. This is because traditional search engines rely on multiple factors, such as the number of backlinks and domain presence, which are challenging for small creators to achieve. However, since Generative Engines utilize

**中文**

一个关键的观察结果是 GEO 对基于搜索引擎结果页面 (SERP) 排名的网站的不同影响。值得注意的是，排名较低的网站通常很难获得可见性，但从 GEO 中受益更多。这是因为传统搜索引擎依赖于多种因素，例如反向链接的数量和域名的存在，这对于小型创作者来说是一个挑战。然而，由于生成式引擎利用

### Page 8

### 段落 69 · Page 8

**EN**

KDD ’24, August 25–29, 2024, Barcelona, Spain Pranjal Aggarwal et al. Method GEOOptimization Relative Improvement Query:What is the secret of Swiss chocolate With per capita annual consumption averaging between 11 and 12 kilos, Swiss people rank among the top chocolate lovers in the world(According to a survey conducted by The International Chocolate Consumption Research Group [1]) Cite Sources 132.4% Query:Should robots replace humans in the workforce? Source:Not here, and not now — until recently.

**中文**

KDD '24，2024 年 8 月 25-29 日，西班牙巴塞罗那 Pranjal Aggarwal 等人。方法 GEOOptimization 相对改进 查询：瑞士巧克力的秘密是什么 瑞士人的人均年消费量在 11 至 12 公斤之间，瑞士人跻身世界顶级巧克力爱好者之列（根据国际巧克力消费研究小组的一项调查[1]） 引用来源 132.4% 查询：机器人应该取代人类劳动力吗？资料来源：不在这里，也不现在——直到最近。

### 段落 70 · Page 8

**EN**

The big difference is that the robots have come not to destroy our lives, but to disrupt our work, with a staggering 70% increase in robotic involvement in the last decade. Statistics Addition 65.5% Query:Did the jacksonville jaguars ever make it to the superbowl? Source:It is important to note that The Jaguars have neverappearedmade an appearance in the Super Bowl.However, They haveachievedan impressive feat by securing 4 divisional titles to their name., a testament to their prowess and determination. Authoritative 89.1% Table 4: Representative examples of GEO methods optimizing source website.

**中文**

最大的区别在于，机器人的出现并不是为了摧毁我们的生活，而是为了扰乱我们的工作，在过去十年中，机器人的参与度增加了 70%，令人震惊。统计加成 65.5% 查询：杰克逊维尔美洲虎队曾经进入过超级碗吗？资料来源：值得注意的是，美洲虎队从未出现在超级碗中。然而，他们已经取得了令人印象深刻的壮举，获得了 4 个分区冠军，这证明了他们的实力和决心。权威性89.1% 表4：GEO方法优化源网站的代表性例子。

### 段落 71 · Page 8

**EN**

Additions are marked in green and Deletions in red. Without adding any substantial new information, GEO methods significantly increase the visibility of the source content. generative models conditioned on website content, factors such as backlink building should not disadvantage small creators. This is evident from the relative improvements in visibility shown in Table 2. For example, the Cite Sources method led to a substantial 115.1% increase in visibility for websites ranked fifth in SERP, while on average, the visibility of the top-ranked website decreased by 30.3%.

**中文**

添加标记为绿色，删除标记为红色。在不添加任何实质性新信息的情况下，GEO 方法显着提高了源内容的可见性。以网站内容为条件的生成模型，反向链接建设等因素不应使小型创作者处于不利地位。这从表 2 中显示的可见度的相对提高中可以明显看出。例如，Cite Sources 方法使 SERP 中排名第五的网站的可见度大幅提高了 115.1%，而平均而言，排名靠前的网站的可见度下降了 30.3%。

### 段落 72 · Page 8

**EN**

This finding highlights GEO’s potential as a tool to democratize the digital space. Many lower-ranked websites are created by small content creators or independent businesses, who traditionally struggle to compete with larger corporations in top search engine results. The advent of Generative Engines might initially seem disadvantageous to these smaller entities. However, the application of GEO methods presents an opportunity for these content creators to significantly improve their visibility in Generative Engine responses.

**中文**

这一发现凸显了 GEO 作为数字空间民主化工具的潜力。许多排名较低的网站是由小型内容创建者或独立企业创建的，他们传统上很难在顶级搜索引擎结果中与大公司竞争。生成式引擎的出现最初似乎对这些较小的实体不利。然而，GEO 方法的应用为这些内容创建者提供了一个机会，可以显着提高他们在生成式引擎响应中的可见性。

### 段落 73 · Page 8

**EN**

By enhancing their content with GEO, they can reach a wider audience, leveling the playing field and allowing them to compete more effectively with larger corporations. 5.3 Combination of GEO Strategies While individual GEO strategies show significant improvements across various domains, in practice, website owners are expected to employ multiple strategies in conjunction. To study the performance improvements achieved by combining GEO strategies, we consider all pairs of combinations of the top 4 performing GEO methods, namely Cite Sources, Fluency Optimization, Statistics Addition, and Quotation Addition.

**中文**

通过使用 GEO 增强内容，他们可以覆盖更广泛的受众，创造公平的竞争环境，并让他们能够更有效地与大公司竞争。 5.3 GEO 策略的组合 虽然单个 GEO 策略在各个领域都显示出显着的改进，但在实践中，网站所有者应该结合使用多种策略。为了研究通过组合 GEO 策略所实现的性能改进，我们考虑了排名前 4 的 GEO 方法的所有组合对，即引用来源、流畅性优化、统计添加和引文添加。

### 段落 74 · Page 8

**EN**

Figure 4 displays the heatmap of relative improvement in the Position-Adjusted Word Count visibility metric achieved by combining different GEO strategies. The analysis demonstrates that the combination of Generative Engine Optimization methods can enhance performance, with the best combination (Fluency Optimization and Statistics Addition) outperforming any single GEO strategy by more than 5.5%4.

**中文**

图 4 显示了通过组合不同 GEO 策略实现的位置调整字数可见性指标相对改进的热图。分析表明，生成式引擎优化方法的组合可以提高性能，最佳组合（流畅性优化和统计添加）比任何单一 GEO 策略的性能提高了 5.5% 以上4。

### 段落 75 · Page 8

**EN**

Furthermore, Cite Sources significantly boosts performance when used 4Due to cost constraints, the analysis was conducted on a subset of 200 examples from the test split, and therefore the numbers presented here differ from those in Table 1 in conjunction with other methods (Average: 31.4%), despite it being relatively less effective when used alone (8% lower than Quotation Addition). The findings underscore the importance of studyingGEO methods in combination, as they are likely to be used by content creators in the real world.

**中文**

此外，使用 Cite Sources 可以显着提高性能 4 由于成本限制，分析是对测试拆分中的 200 个示例的子集进行的，因此此处提供的数字与表 1 中与其他方法结合使用的数字不同（平均：31.4%），尽管单独使用时效果相对较差（比引用添加低 8%）。研究结果强调了组合研究 GEO 方法的重要性，因为它们很可能被现实世界中的内容创建者使用。

### 段落 76 · Page 8

**EN**

5.4 Qualitative Analysis We present a qualitative analysis of GEO methods in Table 4, containing representative examples where GEO methods boost source visibility with minimal changes. Each method optimizes a source through suitable text additions and deletions. In the first example, we see that simply adding the source of a statement can significantly boost visibility in the final answer, requiring minimal effort from the content creator. The second example demonstrates that adding relevant statistics wherever possible ensures increased source visibility in the final Generative Engine response.

**中文**

5.4 定性分析 我们在表 4 中对 GEO 方法进行了定性分析，其中包含 GEO 方法以最小的变化提高来源可见度的代表性示例。每种方法都通过适当的文本添加和删除来优化源。在第一个示例中，我们看到，只需添加语句来源即可显着提高最终答案的可见性，而内容创建者只需付出最少的努力。第二个示例演示了尽可能添加相关统计信息可确保提高最终生成式引擎响应中的来源可见度。

### 段落 77 · Page 8

**EN**

Finally, the third row suggests that merely emphasizing parts of the text and using a persuasive text style can also lead to improvements in visibility. 6 GEO IN THE WILD : EXPERIMENTS WITH DEPLOYED GENERATIVE ENGINE Method Position-Adjusted Word Count Subjective Impression No Optimization 24.1 24 .7 Keyword Stuffing 21.9 28 .1 Quotation Addition 29.1 32.1 Statistics Addition 26.2 33.9 Table 5: Absolute impression metrics of GEO methods on GEO-bench with Perplexity.ai as GE.

**中文**

最后，第三行表明，仅强调文本的某些部分并使用有说服力的文本样式也可以提高可视性。 6 GEO 野外实验：部署生成式引擎方法的实验 位置调整字数 主观印象 无优化 24.1 24 .7 关键词堆砌 21.9 28 .1 引用添加 29.1 32.1 统计添加 26.2 33.9 表 5：GEO 方法在 GEO-bench 上的绝对印象度量Perplexity.ai 为 GE。

### 段落 78 · Page 8

**EN**

While SEO methods such as Keyword Stuffing perform poorly, our proposed GEO methods generalize well to multiple generative engines significanlty improve content visibility. To reinforce the efficacy of our proposedGenerative Engine Optimization methods, we evaluate them on Perplexity.ai, a real deployed Generative Engine with a large user base. Results are

**中文**

虽然关键字填充等 SEO 方法表现不佳，但我们提出的 GEO 方法可以很好地推广到多个生成式引擎，从而显着提高内容可见性。为了增强我们提出的生成式引擎优化方法的有效性，我们在 Perplexity.ai 上对其进行了评估，Perplexity.ai 是一个具有庞大用户群的真实部署的生成式引擎。结果是

### Page 9

### 段落 79 · Page 9

**EN**

GEO: Generative Engine Optimization KDD ’24, August 25–29, 2024, Barcelona, Spain in Table 5. Similar to our generative engine, Quotation Addition performs best in Position-Adjusted Word Count with a 22% improvement over the baseline. Methods that performed well in our generative engine such as Cite Sources, Statistics Addition show improvements of up to 9% and 37% on the two metrics. Our observations, such as the ineffectiveness of traditional SEO methods like Keyword Stuffing, are further highlighted, as it performs 10% worse than the baseline.

**中文**

GEO：生成式引擎优化 KDD ’24，2024 年 8 月 25-29 日，西班牙巴塞罗那，见表 5。与我们的生成式引擎类似，引用添加在位置调整字数方面表现最佳，比基线提高了 22%。在我们的生成式引擎中表现良好的方法（例如引用来源、统计添加）显示这两个指标分别提高了 9% 和 37%。我们的观察结果，例如关键字填充等传统 SEO 方法的无效性，进一步凸显，因为它的表现比基线差 10%。

### 段落 80 · Page 9

**EN**

The results are significant for three reasons: 1) they underscore the importance of developing different Generative Engine Optimization methods to benefit content creators, 2) they highlight the generalizability of our proposed GEO methods on different generative engines, 3) they demonstrate that content creators can use our easy-to-implement proposed GEO methods directly, thus having a high real-world impact. We refer readers to Appendix C.1 for more details. 7 RELATED WORK Evidence-based Answer Generation: Previous works have used several techniques for answer generation backed by sources. Nakano et al.

**中文**

结果具有重要意义，原因有三个：1）它们强调了开发不同的生成式引擎优化方法以使内容创建者受益的重要性，2）它们强调了我们提出的 GEO 方法在不同生成式引擎上的通用性，3）它们表明内容创建者可以直接使用我们易于实现的提出的 GEO 方法，从而在现实世界中产生很高的影响。我们建议读者参阅附录 C.1 了解更多详细信息。 7 相关工作 基于证据的答案生成：以前的工作已经使用了多种由来源支持的答案生成技术。中野等人。

### 段落 81 · Page 9

**EN**

[19] trained GPT-3 to navigate web environments to generate source-backed answers. Similarly, other methods [17, 23, 24] fetch sources via search engines for answer generation. Our work unifies these approaches and provides a common benchmark for improving these systems in the future. In a recent working draft, Kumar and Lakkaraju [11] showed that strategic text sequences can manipulate LLM recommendations to enhance product visibility in generative engines.

**中文**

[19] 训练 GPT-3 来导航网络环境以生成有源支持的答案。类似地，其他方法 [17,23,24] 通过搜索引擎获取来源以生成答案。我们的工作统一了这些方法，并为未来改进这些系统提供了共同的基准。在最近的工作草案中，Kumar 和 Lakkaraju [11] 表明，战略文本序列可以操纵 LLM 建议，以增强生成式引擎中的产品可见性。

### 段落 82 · Page 9

**EN**

While their approach focuses on increasing product visibility through adversarial text, our method introduces non-adversarial strategies to optimize any website content for improved visibility in generative engine search results. Retrieval-Augmented Language Models: Several recent works have tackled the issues of limited memory of language models by fetching relevant sources from a knowledge base to complete a task [3, 9, 18]. However, Generative Engine needs to generate an answer and provide attributions throughout the answer. Further, Generative Engine is not limited to a single text modality regarding both input and output.

**中文**

虽然他们的方法侧重于通过对抗性文本提高产品可见性，但我们的方法引入了非对抗性策略来优化任何网站内容，以提高生成式引擎搜索结果的可见性。检索增强语言模型：最近的几项工作通过从知识库中获取相关资源来完成任务来解决语言模型内存有限的问题[3,9,18]。然而，生成式引擎需要生成答案并在整个答案中提供归因。此外，生成式引擎不限于关于输入和输出的单一文本模态。

### 段落 83 · Page 9

**EN**

Additionally, the framework of Generative Engine is not limited to fetching relevant sources but instead comprises multiple tasks such as query reformulation, source selection, and making decisions on how and when to perform them. Search Engine Optimization: In nearly the past 25 years, extensive research has optimized web content for search engines [2, 12, 22]. These methods fall into On-Page SEO, improving content and user experience, and Off-Page SEO, boosting website authority through link building. In contrast, GEO deals with a more complex environment involving multi-modality, conversational settings.

**中文**

此外，生成式引擎的框架不仅限于获取相关源，而是包含多项任务，例如查询重构、源选择以及决定如何以及何时执行它们。搜索引擎优化：在近 25 年中，广泛的研究已经针对搜索引擎优化了 Web 内容 [2,12,22]。这些方法分为页面搜索引擎优化（On-Page SEO）和站外搜索引擎优化（Off-Page SEO），前者改善内容和用户体验，后者通过链接建设提高网站权威。相比之下，GEO 处理更复杂的环境，涉及多模态、对话设置。

### 段落 84 · Page 9

**EN**

Since GEO is optimized against a generative model not limited to simple keyword matching, traditional SEO strategies will not apply to Generative Engine settings, highlighting the need for GEO. 8 CONCLUSION In this work, we formulate search engines augmented with generative models that we dub generative engines. We propose Generative Engine Optimization (GEO) to empower content creators to optimize their content under generative engines.

**中文**

由于 GEO 针对生成模型进行优化，而不仅仅限于简单的关键字匹配，因此传统的 SEO 策略将不适用于生成式引擎设置，这凸显了 GEO 的必要性。 8 结论 在这项工作中，我们制定了增强了生成模型的搜索引擎，我们将其称为生成式引擎。我们提出生成式引擎优化（GEO），使内容创作者能够在生成式引擎下优化其内容。

### 段落 85 · Page 9

**EN**

We define impression metrics for generative engines and propose and release GEO-bench: a benchmark encompassing diverse user queries from multiple domains and settings, along with relevant sources needed to answer those queries. We propose several ways to optimize content for generative engines and demonstrate that these methods can boost source visibility by up to 40% in generative engine responses. Among other findings, we show that including citations, quotations from relevant sources, and statistics can significantly boost source visibility.

**中文**

我们定义生成式引擎的印象指标，并提出并发布 GEO-bench：一个基准，包含来自多个域和设置的不同用户查询，以及回答这些查询所需的相关来源。我们提出了几种优化生成式引擎内容的方法，并证明这些方法可以将生成式引擎响应中的来源可见度提高高达 40%。除其他发现外，我们还表明，包括引文、相关来源的引用和统计数据可以显着提高来来源可见度。

### 段落 86 · Page 9

**EN**

Further, we discover a dependence of GEO methods’ effectiveness on the query domain and the potential of combining multiple GEO strategies in conjunction. We show promising results on a commercially deployed generative engine with millions of active users, showcasing the real-world impact of our work. In summary, our work is the first to formalize the important and timely GEO paradigm, releasing algorithms and infrastructure (benchmarks, datasets, and metrics) to facilitate rapid progress in generative engines by the community.

**中文**

此外，我们发现 GEO 方法的有效性对查询域的依赖性以及结合多种 GEO 策略的潜力。我们在拥有数百万活跃用户的商业部署的生成式引擎上展示了有希望的结果，展示了我们工作的现实世界影响。总之，我们的工作是第一个将重要且及时的 GEO 范式形式化的工作，发布算法和基础设施（基准、数据集和指标）以促进社区在生成式引擎方面的快速进展。

### 段落 87 · Page 9

**EN**

This serves as a first step towards understanding the impact of generative engines on the digital space and the role of GEO in this new paradigm of search engines. 9 LIMITATIONS While we rigorously test our proposed methods on two generative engines, including a publicly available one, methods may need to adapt over time as GEs evolve, mirroring the evolution of SEO. Additionally, despite our efforts to ensure the queries in our GEObench closely resemble real-world queries, the nature of queries can change over time, necessitating continuous updates.

**中文**

这是了解生成式引擎对数字空间的影响以及 GEO 在这种新的搜索引擎范式中的作用的第一步。 9 局限性 虽然我们在两个生成式引擎（包括公开可用的引擎）上严格测试了我们提出的方法，但随着 GE 的发展，方法可能需要随着时间的推移进行调整，这反映了 SEO 的发展。此外，尽管我们努力确保 GEObench 中的查询与现实世界的查询非常相似，但查询的性质可能会随着时间的推移而发生变化，因此需要不断更新。

### 段落 88 · Page 9

**EN**

Further, owing to the black-box nature of search engine algorithms, we didn’t evaluate howGEO methods affect search rankings. However, we note that changes made by GEO methods are targeted changes in textual content, bearing some resemblance with SEO methods, while not affecting other metadata such as domain name, backlinks, etc, and thus, they are less likely to affect search engine rankings. Further, as larger context lengths in language models become economical, it is expected that future generative models will be able to ingest more sources, thus reducing the impact of search rankings.

**中文**

此外，由于搜索引擎算法的黑盒性质，我们没有评估GEO方法如何影响搜索排名。但我们注意到，GEO方法所做的改变是针对文本内容的改变，与SEO方法有一定相似之处，同时不会影响域名、反向链接等其他元数据，因此影响搜索引擎排名的可能性较小。此外，随着语言模型中更大的上下文长度变得经济，预计未来的生成模型将能够摄取更多的资源，从而减少搜索排名的影响。

### 段落 89 · Page 9

**EN**

Lastly, while every query in our proposedGEO-bench is tagged and manually inspected, there may be discrepancies due to subjective interpretations or errors in labeling. 10 ACKNOWLEDGEMENTS This material is based upon work supported by the National Science Foundation under Grant No. 2107048. Any opinions, findings, and conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the National Science Foundation. REFERENCES [1] Daria Alexander, Wojciech Kusa, and Arjen P. de Vries. 2022. ORCAS-I: Queries Annotated with Intent using Weak Supervision.

**中文**

最后，虽然我们提出的 GEO-bench 中的每个查询都被标记并手动检查，但由于主观解释或标记错误，可能会存在差异。 10 致谢 本材料基于美国国家科学基金会资助号 2107048 资助的工作。本材料中表达的任何意见、发现、结论或建议均为作者个人观点，并不一定反映美国国家科学基金会的观点。参考文献 [1] Daria Alexander、Wojciech Kusa 和 Arjen P. de Vries。 2022.ORCAS-I：使用弱监督的意图注释的查询。

### 段落 90 · Page 9

**EN**

Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval (2022). https://api.semanticscholar.org/CorpusID:248495926 [2] Prashant Ankalkoti. 2017. Survey on Search Engine Optimization Tools & Techniques. Imperial journal of interdisciplinary research 3 (2017). https: //api.semanticscholar.org/CorpusID:116487363 [3] Akari Asai, Xinyan Velocity Yu, Jungo Kasai, and Hannaneh Hajishirzi. 2021. One Question Answering Model for Many Languages with Cross-lingual

**中文**

第 45 届国际 ACM SIGIR 信息检索研究与开发会议（2022 年）论文集。 https://api.semanticscholar.org/CorpusID:248495926 [2] Prashant Ankalkoti。 2017。搜索引擎优化工具和技术调查。帝国跨学科研究杂志 3 (2017)。 https://api.semanticscholar.org/CorpusID:116487363 [3] Akari Asai、Xinyan Velocity Yu、Jungo Kasai 和 Hannaneh Hajishirzi。 2021. 一种多语言跨语言问答模型

### Page 10

### 段落 91 · Page 10

**EN**

KDD ’24, August 25–29, 2024, Barcelona, Spain Pranjal Aggarwal et al. Dense Passage Retrieval. In Neural Information Processing Systems . https: //api.semanticscholar.org/CorpusID:236428949 [4] Sergey Brin and Lawrence Page. 1998. The Anatomy of a Large-Scale Hypertextual Web Search Engine. Comput. Networks 30 (1998), 107–117.

**中文**

KDD '24，2024 年 8 月 25-29 日，西班牙巴塞罗那 Pranjal Aggarwal 等人。密集通道检索。在神经信息处理系统中。 https://api.semanticscholar.org/CorpusID:236428949 [4] 谢尔盖·布林和劳伦斯·佩奇。 1998。大规模超文本网络搜索引擎的剖析。计算。网络 30 (1998), 107–117。

### 段落 92 · Page 10

**EN**

https: //api.semanticscholar.org/CorpusID:7587743 [5] Tom Brown, Benjamin Mann, Nick Ryder, Melanie Subbiah, Jared D Kaplan, Prafulla Dhariwal, Arvind Neelakantan, Pranav Shyam, Girish Sastry, Amanda Askell, Sandhini Agarwal, Ariel Herbert-Voss, Gretchen Krueger, Tom Henighan, Rewon Child, Aditya Ramesh, Daniel Ziegler, Jeffrey Wu, Clemens Winter, Chris Hesse, Mark Chen, Eric Sigler, Mateusz Litwin, Scott Gray, Benjamin Chess, Jack Clark, Christopher Berner, Sam McCandlish, Alec Radford, Ilya Sutskever, and Dario Amodei. 2020. Language Models are Few-Shot Learners. In Advances in Neural Information Processing Systems , H. Larochelle, M.

**中文**

https://api.semanticscholar.org/CorpusID:7587743 [5] Tom Brown、Benjamin Mann、Nick Ryder、Melanie Subbiah、Jared D Kaplan、Prafulla Dhariwal、Arvind Neelakantan、Pranav Shyam、Girish Sastry、Amanda Askel、Sandhini Agarwal、Ariel Herbert-Voss、Gretchen Krueger、Tom Henighan、Rewon Child、Aditya Ramesh、Daniel Ziegler、Jeffrey Wu、Clemens Winter、Chris Hesse、Mark Chen、Eric Sigler、Mateusz Litwin、Scott Gray、Benjamin Chess、Jack Clark、Christopher Berner、Sam McCandlish、Alec Radford、Ilya Sutskever 和 Dario Amodei。 2020 年。语言模型是少样本学习者。 《神经信息处理系统进展》，H. Larochelle，M.

### 段落 93 · Page 10

**EN**

Ranzato, R. Hadsell, M.F. Balcan, and H. Lin (Eds.), Vol. 33. Curran Associates, Inc., 1877–1901. https://proceedings.neurips.cc/paper_files/paper/2020/file/ 1457c0d6bfcb4967418bfb8ac142f64a-Paper.pdf [6] Nick Craswell, Bhaskar Mitra, Emine Yilmaz, Daniel Fernando Campos, and Jimmy J. Lin. 2021. MS MARCO: Benchmarking Ranking Models in the Large-Data Regime. Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval (2021). https://api.semanticscholar.org/ CorpusID:234336491 [7] Brian Dean. 2023. We Analyzed 4 Million Google Search Results.

**中文**

Ranzato，R. Hadsell，M.F. Balcan 和 H. Lin（编辑），卷。 33. Curran Associates, Inc.，1877-1901。 https://proceedings.neurips.cc/paper_files/paper/2020/file/1457c0d6bfcb4967418bfb8ac142f64a-Paper.pdf [6] Nick Craswell、Bhaskar Mitra、Emine Yilmaz、Daniel Fernando Campos 和 Jimmy J. Lin。 2021.MS MARCO：大数据体系中的基准排名模型。第 44 届国际 ACM SIGIR 信息检索研究与开发会议（2021 年）论文集。 https://api.semanticscholar.org/ CorpusID:234336491 [7] 布莱恩·迪恩。 2023 年。我们分析了 400 万个 Google 搜索结果。

### 段落 94 · Page 10

**EN**

Here’s What We Learned About Organic Click Through Rate. https://backlinko.com/googlectr-stats Accessed: 2024-06-08. [8] Danny Goodwin. 2011. Top Google Result Gets 36.4% of Clicks [Study]. https://www.searchenginewatch.com/2011/04/21/top-google-resultgets-36-4-of-clicks-study/ [9] Kelvin Guu, Kenton Lee, Zora Tung, Panupong Pasupat, and Ming-Wei Chang. 2020. REALM: Retrieval-Augmented Language Model Pre-Training. ArXiv abs/2002.08909 (2020). https://api.semanticscholar.org/CorpusID:211204736 [10] Ziwei Ji, Nayeon Lee, Rita Frieske, Tiezheng Yu, Dan Su, Yan Xu, Etsuko Ishii, Ye Jin Bang, Andrea Madotto, and Pascale Fung. 2023.

**中文**

以下是我们对有机点击率的了解。 https://backlinko.com/googlectr-stats 访问时间：2024 年 6 月 8 日。 [8] 丹尼·古德温。 2011 年。Google 排名靠前的结果获得了 36.4% 的点击率 [研究]。 https://www.searchenginewatch.com/2011/04/21/top-google-resultgets-36-4-of-clicks-study/ [9] Kelvin Guu、Kenton Lee、Zora Tung、Panupong Pasupat 和 Ming-Wei Chang。 2020.REALM：检索增强语言模型预训练。 ArXiv abs/2002.08909 (2020)。 https://api.semanticscholar.org/CorpusID:211204736 [10] Ziwei Ji、Nayeon Lee、Rita Frieske、Tiezheng Yu、Dan Su、Yan Xu、Etsuko Ishii、Ye Jin Bang、Andrea Madotto 和 Pascale Fung。 2023 年。

### 段落 95 · Page 10

**EN**

Survey of hallucination in natural language generation. Comput. Surveys 55, 12 (2023), 1–38. [11] Aounon Kumar and Himabindu Lakkaraju. 2024. Manipulating Large Language Models to Increase Product Visibility. arXiv:2404.07981 [cs.IR] [12] R.Anil Kumar, Zaiduddin Shaik, and Mohammed Furqan. 2019. A Survey on Search Engine Optimization Techniques. International Journal of P2P Network Trends and Technology (2019). https://doi.org/10.14445/22492615/IJPTT-V9I1P402 [13] Tom Kwiatkowski, Jennimaria Palomaki, Olivia Redfield, Michael Collins, Ankur P.

**中文**

自然语言生成中的幻觉调查。计算。调查 55、12 (2023)、1-38。 [11]奥农·库马尔和希玛宾杜·拉卡拉朱。 2024。操纵大型语言模型以提高产品可见性。 arXiv:2404.07981 [cs.IR] [12] R.Anil Kumar、Zaiduddin Shaik 和 Mohammed Furqan。 2019。搜索引擎优化技术调查。国际 P2P 网络趋势与技术杂志 (2019)。 https://doi.org/10.14445/22492615/IJPTT-V9I1P402 [13] Tom Kwiatkowski、Jennimaria Palomaki、Olivia Redfield、Michael Collins、Ankur P.

### 段落 96 · Page 10

**EN**

Parikh, Chris Alberti, Danielle Epstein, Illia Polosukhin, Jacob Devlin, Kenton Lee, Kristina Toutanova, Llion Jones, Matthew Kelcey, Ming-Wei Chang, Andrew M. Dai, Jakob Uszkoreit, Quoc V. Le, and Slav Petrov. 2019. Natural Questions: A Benchmark for Question Answering Research. Transactions of the Association for Computational Linguistics 7 (2019), 453–466. https: //api.semanticscholar.org/CorpusID:86611921 [14] Nelson F. Liu, Tianyi Zhang, and Percy Liang. 2023. Evaluating Verifiability in Generative Search Engines. ArXiv abs/2304.09848 (2023). https://api.

**中文**

Parikh、Chris Alberti、Danielle Epstein、Illia Polosukhin、Jacob Devlin、Kenton Lee、Kristina Toutanova、Llion Jones、Matthew Kelcey、Ming-Wei Chang、Andrew M. Dai、Jakob Uszkoreit、Quoc V. Le 和 Slav Petrov。 2019。自然问题：问答研究的基准。计算语言学协会汇刊 7 (2019), 453–466。 https://api.semanticscholar.org/CorpusID:86611921 [14] Nelson F. Liu，张天一，梁珀西。 2023.评估生成式搜索引擎的可验证性。 ArXiv abs/2304.09848 (2023)。 https://api.

### 段落 97 · Page 10

**EN**

semanticscholar.org/CorpusID:258212854 [15] Yang Liu, Dan Iter, Yichong Xu, Shuo Wang, Ruochen Xu, and Chenguang Zhu. 2023. G-Eval: NLG Evaluation using GPT-4 with Better Human Alignment.ArXiv abs/2303.16634 (2023). https://api.semanticscholar.org/CorpusID:257804696 [16] G. D. Maayan. 2023. How Google SGE will impact your traffic – and 3 SGE recovery case studies. Search Engine Land (5 Sep 2023).

**中文**

Semanticscholar.org/CorpusID:258212854 [15] Yang Liu，Dan Iter，Yichong Xu，Shuo Wang，Ruochen Xu 和 Chenuang Zhu。 2023.G-Eval：使用 GPT-4 和更好的人类对齐进行 NLG 评估。ArXiv abs/2303.16634 (2023)。 https://api.semanticscholar.org/CorpusID:257804696 [16] G. D. Maayan。 2023 年。Google SGE 将如何影响您的流量 – 以及 3 个 SGE 恢复案例研究。搜索引擎土地（2023 年 9 月 5 日）。

### 段落 98 · Page 10

**EN**

https://searchengineland.com/how-google-sge-will-impact-your-trafficand-3-sge-recovery-case-studies-431430 [17] Jacob Menick, Maja Trebacz, Vladimir Mikulik, John Aslanides, Francis Song, Martin Chadwick, Mia Glaese, Susannah Young, Lucy Campbell-Gillingham, Geoffrey Irving, and Nathan McAleese. 2022. Teaching language models to support answers with verified quotes. ArXiv abs/2203.11147 (2022).

**中文**

https://searchengineland.com/how-google-sge-will-impact-your-trafficand-3-sge-recovery-case-studies-431430 [17] Jacob Menick、Maja Trebacz、Vladimir Mikulik、John Aslanides、Francis Song、Martin Chadwick、Mia Glaese、Susannah Young、Lucy Campbell-Gillingham、Geoffrey Irving 和 Nathan麦卡利斯。 2022. 教授语言模型以支持经过验证的引用的答案。 ArXiv abs/2203.11147 (2022)。

### 段落 99 · Page 10

**EN**

https: //api.semanticscholar.org/CorpusID:247594830 [18] Grégoire Mialon, Roberto Dessì, Maria Lomeli, Christoforos Nalmpantis, Ramakanth Pasunuru, Roberta Raileanu, Baptiste Rozière, Timo Schick, Jane Dwivedi-Yu, Asli Celikyilmaz, Edouard Grave, Yann LeCun, and Thomas Scialom. 2023. Augmented Language Models: a Survey. ArXiv abs/2302.07842 (2023). https://api.semanticscholar.org/CorpusID:256868474 [19] Reiichiro Nakano, Jacob Hilton, S.

**中文**

https://api.semanticscholar.org/CorpusID:247594830 [18] Grégoire Mialon、Roberto Dessì、Maria Lomeli、Christoforos Nalmpantis、Ramakanth Pasunuru、Roberta Raileanu、Baptiste Rozière、Timo Schick、Jane Dwivedi-Yu、Asli Celikyilmaz、Edouard Grave、Yann勒昆和托马斯·夏洛姆。 2023.增强语言模型：一项调查。 ArXiv abs/2302.07842 (2023)。 https://api.semanticscholar.org/CorpusID:256868474 [19] Reiichiro Nakano, Jacob Hilton, S.

### 段落 100 · Page 10

**EN**

Arun Balaji, Jeff Wu, Ouyang Long, Christina Kim, Christopher Hesse, Shantanu Jain, Vineet Kosaraju, William Saunders, Xu Jiang, Karl Cobbe, Tyna Eloundou, Gretchen Krueger, Kevin Button, Matthew Knight, Benjamin Chess, and John Schulman. 2021. WebGPT: Browser-assisted question-answering with human feedback. ArXiv abs/2112.09332 (2021). https: //api.semanticscholar.org/CorpusID:245329531 [20] OpenAI. 2022. Introducing ChatGPT.

**中文**

Arun Balaji、Jeff Wu、欧阳龙、Christina Kim、Christopher Hesse、Shantanu Jain、Vineet Kosaraju、William Saunders、徐江、Karl Cobbe、Tyna Eloundou、Gretchen Krueger、Kevin Button、Matthew Knight、Benjamin Chess 和 John Schulman。 2021.WebGPT：浏览器辅助问答与人工反馈。 ArXiv abs/2112.09332 (2021)。 https://api.semanticscholar.org/CorpusID:245329531 [20] OpenAI。 2022 年。ChatGPT 简介。

### 段落 101 · Page 10

**EN**

https://openai.com/index/chatgpt/ [21] OpenAI, Josh Achiam, Steven Adler, Sandhini Agarwal, Lama Ahmad, Ilge Akkaya, Florencia Leoni Aleman, Diogo Almeida, Janko Altenschmidt, Sam Altman, Shyamal Anadkat, Red Avila, Igor Babuschkin, Suchir Balaji, Valerie Balcom, Paul Baltescu, Haiming Bao, Mohammad Bavarian, Jeff Belgum, Irwan Bello, Jake Berdine, Gabriel Bernadett-Shapiro, Christopher Berner, Lenny Bogdonoff, Oleg Boiko, Madelaine Boyd, Anna-Luisa Brakman, Greg Brockman, Tim Brooks, Miles Brundage, Kevin Button, Trevor Cai, Rosie Campbell, Andrew Cann, Brittany Carey, Chelsea Carlson, Rory Carmichael, Brooke Chan, Che Chang, Fotis Chantzis,

**中文**

https://openai.com/index/chatgpt/ [21] OpenAI, Josh Achiam, Steven Adler, Sandhini Agarwal, Lama Ahmad, Ilge Akkaya, Florencia Leoni Aleman, Diogo Almeida, Janko Altenschmidt, Sam Altman, Shyamal Anadkat, Red Avila, Igor Babuschkin, Suchir Balaji, Valerie Balcom, Paul Baltescu, Haiming Bao,穆罕默德·巴伐利亚,杰夫·贝尔古姆,伊尔万·贝罗,杰克·伯丁,加布里埃尔·伯纳戴特-夏皮罗,克里斯托弗·伯纳,兰尼·博格多诺夫,奥列格·博伊科,玛德琳·博伊德,安娜-路易莎·布拉克曼,格雷格·布罗克曼,蒂姆·布鲁克斯,迈尔斯·布伦戴奇,凯文·巴顿,特雷弗·蔡,罗茜·坎贝尔,安德鲁·卡恩,布列塔尼·凯莉,切尔西·卡尔森,罗里·卡迈克尔,布鲁克·陈,车·昌、福蒂斯·尚齐斯、

### 段落 102 · Page 10

**EN**

Derek Chen, Sully Chen, Ruby Chen, Jason Chen, Mark Chen, Ben Chess, Chester Cho, Casey Chu, Hyung Won Chung, Dave Cummings, Jeremiah Currier, Yunxing Dai, Cory Decareaux, Thomas Degry, Noah Deutsch, Damien Deville, Arka Dhar, David Dohan, Steve Dowling, Sheila Dunning, Adrien Ecoffet, Atty Eleti, Tyna Eloundou, David Farhi, Liam Fedus, Niko Felix, Simón Posada Fishman, Juston Forte, Isabella Fulford, Leo Gao, Elie Georges, Christian Gibson, Vik Goel, Tarun Gogineni, Gabriel Goh, Rapha Gontijo-Lopes, Jonathan Gordon, Morgan Grafstein, Scott Gray, Ryan Greene, Joshua Gross, Shixiang Shane Gu, Yufei Guo, Chris Hallacy, Jesse Han, Jeff Harris,

**中文**

德里克·陈、Sully Chen、Ruby Chen、Jason Chen、Mark Chen、Ben Chess、Chester Cho、Casey Chu、Hung Won Chung、Dave Cummings、Jeremiah Currier、戴云星、Cory Decareaux、Thomas Degry、Noah Deutsch、Damien Deville、Arka Dhar、David Dohan、Steve Dowling、Sheila Dunning、Adrien Ecoffet、Atty Eleti、Tyna Eloundou、David法尔希、利亚姆·费杜斯、尼科·菲利克斯、西蒙·波萨达·菲什曼、贾斯顿·福特、伊莎贝拉·富尔福德、里奥·高、埃利·乔治、克里斯蒂安·吉布森、维克·戈尔、塔伦·戈吉内尼、加布里埃尔·吴、拉法·贡蒂霍-洛佩斯、乔纳森·戈登、摩根·格拉夫斯坦、斯科特·格雷、瑞安·格林、约书亚·格罗斯、顾世翔、郭宇飞、克里斯·哈拉西、杰西·韩、杰夫哈里斯，

### 段落 103 · Page 10

**EN**

Yuchen He, Mike Heaton, Johannes Heidecke, Chris Hesse, Alan Hickey, Wade Hickey, Peter Hoeschele, Brandon Houghton, Kenny Hsu, Shengli Hu, Xin Hu, Joost Huizinga, Shantanu Jain, Shawn Jain, Joanne Jang, Angela Jiang, Roger Jiang, Haozhun Jin, Denny Jin, Shino Jomoto, Billie Jonn, Heewoo Jun, Tomer Kaftan, Łukasz Kaiser, Ali Kamali, Ingmar Kanitscheider, Nitish Shirish Keskar, Tabarak Khan, Logan Kilpatrick, Jong Wook Kim, Christina Kim, Yongjik Kim, Jan Hendrik Kirchner, Jamie Kiros, Matt Knight, Daniel Kokotajlo, Łukasz Kondraciuk, Andrew Kondrich, Aris Konstantinidis, Kyle Kosic, Gretchen Krueger, Vishal Kuo, Michael Lampe, Ikai Lan, Teddy

**中文**

何宇辰, 迈克·希顿, 约翰内斯·海德克, 克里斯·赫塞, 艾伦·希基, 韦德·希基, 彼得·赫舍勒, 布兰登·霍顿, 许肯尼, 胡胜利, 胡欣, Joost Huizinga, Shantanu Jain, Shawn Jain, Joanne Jang, Angela Jiang, Roger Jiang, 金浩准, Denny Jin, Shino Jomoto, Billie Jonn, Heewoo Jun, Tomer Kaftan,武卡斯·凯撒、阿里·卡玛利、英格玛·卡尼茨谢德尔、尼特什·希尔什·凯斯卡、塔巴拉克·汗、洛根·基尔帕特里克、金钟郁、克里斯蒂娜·金、Yongjik Kim、Jan Hendrik Kirchner、杰米·基罗斯、马特·奈特、丹尼尔·科科塔伊洛、武卡斯·康德拉丘克、安德鲁·康德里奇、阿里斯·康斯坦丁尼迪斯、凯尔·科西奇、格雷琴克鲁格、郭维沙、迈克尔·兰佩、伊凯·兰、泰迪

### 段落 104 · Page 10

**EN**

Lee, Jan Leike, Jade Leung, Daniel Levy, Chak Ming Li, Rachel Lim, Molly Lin, Stephanie Lin, Mateusz Litwin, Theresa Lopez, Ryan Lowe, Patricia Lue, Anna Makanju, Kim Malfacini, Sam Manning, Todor Markov, Yaniv Markovski, Bianca Martin, Katie Mayer, Andrew Mayne, Bob McGrew, Scott Mayer McKinney, Christine McLeavey, Paul McMillan, Jake McNeil, David Medina, Aalok Mehta, Jacob Menick, Luke Metz, Andrey Mishchenko, Pamela Mishkin, Vinnie Monaco, Evan Morikawa, Daniel Mossing, Tong Mu, Mira Murati, Oleg Murk, David Mély, Ashvin Nair, Reiichiro Nakano, Rajeev Nayak, Arvind Neelakantan, Richard Ngo, Hyeonwoo Noh, Long Ouyang, Cullen O’Keefe, Jaku

**中文**

Lee、Jan Leike、Jade Leung、Daniel Levy、Chak Ming Li、Rachel Lim、Molly Lin、Stephanie Lin、Mateusz Litwin、Theresa Lopez、Ryan Lowe、Patricia Lue、Anna Makanju、Kim Malfacini、Sam Manning、Todor Markov、Yaniv Markovski、Bianca Martin、Katie Mayer、Andrew Mayne、Bob McGrew、Scott Mayer McKinney、Christine McLeavey、保罗·麦克米伦、杰克·麦克尼尔、大卫·梅迪纳、阿洛克·梅塔、雅各布·梅尼克、卢克·梅茨、安德烈·米申科、帕梅拉·米什金、维尼·莫纳科、埃文·森川、丹尼尔·莫辛、童木、米拉·穆拉蒂、奥列格·默克、大卫·梅利、阿什文·奈尔、中野礼一郎、拉杰夫·纳亚克、阿尔文德·尼拉坎坦、理查德·吴、贤宇Noh、欧阳龙、Cullen O’Keefe、Jaku

### 段落 105 · Page 10

**EN**

b Pachocki, Alex Paino, Joe Palermo, Ashley Pantuliano, Giambattista Parascandolo, Joel Parish, Emy Parparita, Alex Passos, Mikhail Pavlov, Andrew Peng, Adam Perelman, Filipe de Avila Belbute Peres, Michael Petrov, Henrique Ponde de Oliveira Pinto, Michael, Pokorny, Michelle Pokrass, Vitchyr H.

**中文**

b Pachocki、Alex Paino、Joe Palermo、Ashley Pantuliano、Giambattista Parascandolo、Joel Parish、Emy Parparita、Alex Passos、Mikhail Pavlov、Andrew Peng、Adam Perelman、Filipe de Avila Belbute Peres、Michael Petrov、Henrique Ponde de Oliveira Pinto、Michael、Pokorny、Michelle Pokrass、Vitchyr H.

### 段落 106 · Page 10

**EN**

Pong, Tolly Powell, Alethea Power, Boris Power, Elizabeth Proehl, Raul Puri, Alec Radford, Jack Rae, Aditya Ramesh, Cameron Raymond, Francis Real, Kendra Rimbach, Carl Ross, Bob Rotsted, Henri Roussez, Nick Ryder, Mario Saltarelli, Ted Sanders, Shibani Santurkar, Girish Sastry, Heather Schmidt, David Schnurr, John Schulman, Daniel Selsam, Kyla Sheppard, Toki Sherbakov, Jessica Shieh, Sarah Shoker, Pranav Shyam, Szymon Sidor, Eric Sigler, Maddie Simens, Jordan Sitkin, Katarina Slama, Ian Sohl, Benjamin Sokolowsky, Yang Song, Natalie Staudacher, Felipe Petroski Such, Natalie Summers, Ilya Sutskever, Jie Tang, Nikolas Tezak, Madeleine B.

**中文**

Pong、托利·鲍威尔、Aletha Power、鲍里斯·鲍尔、伊丽莎白·普罗尔、劳尔·普里、亚历克·雷德福、杰克·雷、阿迪亚·拉梅什、卡梅伦·雷蒙德、弗朗西斯·雷亚尔、肯德拉·里姆巴赫、卡尔·罗斯、鲍勃·罗斯特德、亨利·鲁塞斯、尼克·莱德、马里奥·萨尔塔雷利、特德·桑德斯、希巴尼·桑图卡、吉里什·萨斯特里、希瑟·施密特、大卫·施努尔、约翰舒尔曼、丹尼尔·赛尔萨姆、凯拉·谢泼德、托基·谢尔巴科夫、杰西卡·谢、莎拉·肖克、普拉纳夫·希亚姆、西蒙·西多、埃里克·西格勒、麦迪·西蒙斯、乔丹·席特金、卡塔琳娜·斯拉玛、伊恩·索尔、本杰明·索科洛斯基、杨松、娜塔莉·施陶达赫、费利佩·彼得罗斯基·萨奇、娜塔莉·萨默斯、伊利亚·苏茨克弗、唐杰、尼古拉斯特扎克，马德琳·B.

### 段落 107 · Page 10

**EN**

Thompson, Phil Tillet, Amin Tootoonchian, Elizabeth Tseng, Preston Tuggle, Nick Turley, Jerry Tworek, Juan Felipe Cerón Uribe, Andrea Vallone, Arun Vijayvergiya, Chelsea Voss, Carroll Wainwright, Justin Jay Wang, Alvin Wang, Ben Wang, Jonathan Ward, Jason Wei, CJ Weinmann, Akila Welihinda, Peter Welinder, Jiayi Weng, Lilian Weng, Matt Wiethoff, Dave Willner, Clemens Winter, Samuel Wolrich, Hannah Wong, Lauren Workman, Sherwin Wu, Jeff Wu, Michael Wu, Kai Xiao, Tao Xu, Sarah Yoo, Kevin Yu, Qiming Yuan, Wojciech Zaremba, Rowan Zellers, Chong Zhang, Marvin Zhang, Shengjia Zhao, Tianhao Zheng, Juntang Zhuang, William Zhuk, and Barret Zoph. 2024.

**中文**

Thompson, Phil Tillet, Amin Tootoonchian, Elizabeth Tseng, Preston Tuggle, Nick Turley, Jerry Tworek, Juan Felipe Cerón Uribe, Andrea Vallone, Arun Vijayvergiya, Chelsea Voss, Carroll Wainwright, Justin Jay Wang, Alvin Wang, Ben Wang, Jonathan Ward, Jason Wei, CJ Weinmann, Akila Welihinda, Peter Welinder, Jiayi Weng, Lilian Weng、Matt Wiethoff、Dave Willner、Clemens Winter、Samuel Wolrich、Hannah Wong、Lauren Workman、Sherwin Wu、Jeff Wu、Michael Wu、Kai Shaw、Tao Xu、Sarah Yoo、Kevin Yu、Qiming Yuan、Wojciech Zaremba、Rowan Zellers、Chong Chang、Marvin 张、Shengjia Chao、郑天浩、Juntang Zhuang、William Zhuk 和 Barret Zoph。 2024 年。

### 段落 108 · Page 10

**EN**

GPT-4 Technical Report. arXiv:2303.08774 [cs.CL] [22] A. Shahzad, Deden Witarsyah Jacob, Nazri M. Nawi, Hairulnizam Bin Mahdin, and Marheni Eka Saputri. 2020. The new trend for search engine optimization, tools and techniques. Indonesian Journal of Electrical Engineering and Computer Science 18 (2020), 1568. https://api.semanticscholar.org/CorpusID:213123106 [23] Kurt Shuster, Jing Xu, Mojtaba Komeili, Da Ju, Eric Michael Smith, Stephen Roller, Megan Ung, Moya Chen, Kushal Arora, Joshua Lane, Morteza Behrooz, W.K.F. Ngan, Spencer Poff, Naman Goyal, Arthur Szlam, Y-Lan Boureau, Melanie Kambadur, and Jason Weston. 2022.

**中文**

GPT-4 技术报告。 arXiv:2303.08774 [cs.CL] [22] A. Shahzad、Deden Witarsyah Jacob、Nazri M. Nawi、Hairulnizam Bin Mahdin 和 Marheni Eka Saputri。 2020年。搜索引擎优化、工具和技术的新趋势。印度尼西亚电气工程与计算机科学杂志 18 (2020), 1568. https://api.semanticscholar.org/CorpusID:213123106 [23] Kurt Shuster, Jing Xu, Mojtaba Komeili, Da Ju, Eric Michael Smith, Stephen Roller, Megan Ung, Moya Chen, Kushal Arora, Joshua Lane, Morteza Behrooz, W.K.F. Ngan、Spencer Poff、Naman Goyal、Arthur Szlam、Y-Lan Boureau、Melanie Kambadur 和 Jason Weston。 2022 年。

### 段落 109 · Page 10

**EN**

BlenderBot 3: a deployed conversational agent that continually learns to responsibly engage. ArXiv abs/2208.03188 (2022).

**中文**

BlenderBot 3：一个部署的对话代理，不断学习负责任地参与。 ArXiv abs/2208.03188 (2022)。

### 段落 110 · Page 10

**EN**

https://api.semanticscholar.org/CorpusID:251371589 [24] Romal Thoppilan, Daniel De Freitas, Jamie Hall, Noam Shazeer, Apoorv Kulshreshtha, Heng-Tze Cheng, Alicia Jin, Taylor Bos, Leslie Baker, Yu Du, YaGuang Li, Hongrae Lee, Huaixiu Steven Zheng, Amin Ghafouri, Marcelo Menegali, Yanping Huang, Maxim Krikun, Dmitry Lepikhin, James Qin, Dehao Chen, Yuanzhong Xu, Zhifeng Chen, Adam Roberts, Maarten Bosma, Vincent Zhao, Yanqi Zhou, Chung-Ching Chang, Igor Krivokon, Will Rusch, Marc Pickett, Pranesh Srinivasan, Laichee Man, Kathleen Meier-Hellstern, Meredith Ringel Morris, Tulsee Doshi, Renelito Delos Santos, Toju Duke, Johnny Soraker, Ben Zevenbe

**中文**

https://api.semanticscholar.org/CorpusID:251371589 [24] Romal Thoppilan, Daniel De Freitas, Jamie Hall, Noam Shazeer, Apoorv Kulshreshtha, Heng-Tze Cheng, Alicia Jin, Taylor Bos, Leslie Baker, Yu Du, YaGuang Li, Hongrae Lee, Huaxiu Steven Cheng, Amin Ghafouri, Marcelo Menegali、黄艳平、马克西姆·克里昆、德米特里·莱皮欣、詹姆斯·秦、陈德豪、徐元中、陈志峰、亚当·罗伯茨、马丁·博斯马、赵文森、周艳奇、张中正、伊戈尔·克里沃孔、威尔·拉什、马克·皮克特、普拉内什·斯里尼瓦桑、莱奇·曼、凯瑟琳·梅尔-赫尔斯特恩、梅雷迪斯·林格尔·莫里斯、图尔西·多西、雷内利托德洛斯·桑托斯、托朱·杜克、约翰尼·索雷克、本·泽文贝

### 段落 111 · Page 10

**EN**

rgen, Vinodkumar Prabhakaran, Mark Diaz, Ben Hutchinson, Kristen Olson, Alejandra Molina, Erin Hoffman-John, Josh Lee, Lora Aroyo, Ravi Rajakumar, Alena Butryna, Matthew Lamm, Viktoriya Kuzmina, Joe Fenton, Aaron Cohen, Rachel Bernstein, Ray Kurzweil, Blaise Aguera-Arcas, Claire Cui, Marian Croak, Ed Chi, and Quoc Le.

**中文**

rgen、维诺库玛·普拉巴卡兰、马克·迪亚兹、本·哈钦森、克里斯汀·奥尔森、亚历杭德拉·莫里纳、艾琳·霍夫曼-约翰、乔什·李、洛拉·阿罗约、拉维·拉贾库玛、阿琳娜·布特里纳、马修·拉姆、维克多利亚·库兹米纳、乔·芬顿、亚伦·科恩、雷切尔·伯恩斯坦、雷·库兹韦尔、布莱斯·阿格拉-阿卡斯、克莱尔·崔、玛丽安·克罗克 (Marian Croak)、艾德·奇 (Ed Chi) 和夸克·勒 (Quoc Le)。

### 段落 112 · Page 10

**EN**

2022. LaMDA: Language Models for Dialog Applications. arXiv:2201.08239 [cs.CL] [25] Chunting Zhou, Pengfei Liu, Puxin Xu, Srini Iyer, Jiao Sun, Yuning Mao, Xuezhe Ma, Avia Efrat, Ping Yu, L. Yu, Susan Zhang, Gargi Ghosh, Mike Lewis, Luke Zettlemoyer, and Omer Levy. 2023. LIMA: Less Is More for Alignment. ArXiv abs/2305.11206 (2023). https://api.semanticscholar.org/CorpusID:258822910

**中文**

2022.LaMDA：对话应用程序的语言模型。 arXiv:2201.08239 [cs.CL] [25] Chunting Zhou、Pengfei Liu、Puxin Xu、Srini Iyer、Jiao Sun、Yuning Mao、Xuezhe Ma、Avia Efrat、Ping Yu、L. Yu、Susan Zhang、Gargi Ghosh、Mike Lewis、Luke Zettlemoyer 和 Omer Levy。 2023. LIMA：对齐少即是多。 ArXiv abs/2305.11206 (2023)。 https://api.semanticscholar.org/CorpusID:258822910

### Page 11

### 段落 113 · Page 11

**EN**

GEO: Generative Engine Optimization KDD ’24, August 25–29, 2024, Barcelona, Spain Listing 1: Prompt used for Generative Engine. The GE takes the query and 5 sources as input and outputs the response to query with response grounded in the sources. 1 Write an accurate and concise answer for the given user question, using _only_ the provided summarized web search results. The answer should be correct, high-quality, and written by an expert using an unbiased and journalistic tone. The user 's language of choice such as English, Francais, Espamol, Deutsch, or should be used. The answer should be informative, interesting, and engaging.

**中文**

GEO：生成式引擎优化 KDD ’24，2024 年 8 月 25-29 日，西班牙巴塞罗那 列表 1：用于生成式引擎的提示。 GE 将查询和 5 个源作为输入，并输出对查询的响应，响应基于源。 1 仅使用提供的汇总网络搜索结果，为给定的用户问题写出准确、简洁的答案。答案应该是正确的、高质量的，并且由专家以公正的新闻语气撰写。或应使用用户选择的语言，例如英语、法语、西班牙语、德语。答案应该内容丰富、有趣且有吸引力。

### 段落 114 · Page 11

**EN**

The answer 's logic and reasoning should be rigorous and defensible. Every sentence in the answer should be _immediately followed_ by an in-line citation to the search result(s). The cited search result(s) should fully support _all_ the information in the sentence. Search results need to be cited using [ index]. When citing several search results, use [1][2][3] format rather than [1, 2, 3] . You can use multiple search results to respond comprehensively while avoiding irrelevant search results.

**中文**

回答的逻辑和推理要严密、站得住脚。答案中的每个句子都应该“紧随其后”对搜索结果进行内联引用。引用的搜索结果应完全支持句子中的_所有_信息。搜索结果需要使用[索引]引用。引用多个搜索结果时，请使用 [1][2][3] 格式而不是 [1, 2, 3]。您可以使用多个搜索结果进行全面响应，同时避免不相关的搜索结果。

### 段落 115 · Page 11

**EN**

2 3 Question: {query} 4 5 Search Results : 6 {source_text} A CONVERSATIONAL GENERATIVE ENGINE In Section 2.1, we discussed a single-turn Generative Enginethat outputs a single response given the user query. However, one of the strengths of upcoming Generative Engines will be their ability to engage in an active back-and-forth conversation with the user. The conversation allows users to provide clarifications to their queries or Generative Engine response and ask follow-ups. Specifically, in equation 1, instead of the input being a single query 𝑞𝑢, it is modeled as a conversation history 𝐻 = (𝑞𝑡𝑢, 𝑟𝑡 ) pairs.

**中文**

2 3 问题：{query} 4 5 搜索结果：6 {source_text} 对话式生成式引擎 在第 2.1 节中，我们讨论了单轮生成式引擎，它根据用户查询输出单个响应。然而，即将推出的生成式引擎的优势之一是它们能够与用户进行积极的来回对话。该对话允许用户对其查询或生成式引擎响应进行澄清并询问后续问题。具体来说，在等式 1 中，输入不是单个查询 𝑞𝑢，而是被建模为对话历史记录 𝐻 = (𝑞𝑡𝑢, 𝑟𝑡 ) 对。

### 段落 116 · Page 11

**EN**

The response 𝑟𝑡 +1 is then defined as: 𝐺𝐸 := 𝑓𝐿𝐸 (𝐻, 𝑃𝑈 ) → 𝑟 𝑡 +1 (5) where 𝑡 is the turn number. Further, to engage the user in a conversation, a separate LLM, 𝐿𝑓 𝑜𝑙𝑙𝑜𝑤 or 𝐿𝑟𝑒𝑠𝑝 , may generate suggested follow-up queries based on 𝐻, 𝑃𝑈 , and 𝑟𝑡 +1. The suggested follow-up queries are typically designed to maximize the likelihood of user engagement. This not only benefits Generative Engine providers by increasing user interaction but also benefits website owners by enhancing their visibility. Furthermore, these follow-up queries can help users by getting more detailed information.

**中文**

响应 𝑟𝑡 +1 然后定义为： 𝐺𝐸 := 𝑓𝐿𝐸 (𝐻, 𝑃𝑈 ) → 𝑟 𝑡 +1 (5) 其中 𝑡 是回合数。此外，为了让用户参与对话，单独的 LLM、 𝐿𝑓 𝑜𝑙𝑙𝑜𝑤 或 𝐿𝑟𝑒𝑠𝑝 可能会基于 𝐻、 𝑃𝑈 和 𝑟𝑡 +1 生成建议的后续查询。建议的后续查询通常旨在最大化用户参与的可能性。这不仅通过增加用户交互使生成式引擎提供商受益，而且通过提高网站所有者的可见性也使网站所有者受益。此外，这些后续查询可以帮助用户获取更详细的信息。

### 段落 117 · Page 11

**EN**

B EXPERIMENTAL SETUP B.1 Evaluated Generative Engine The exact prompt used is shown in Listing 1. B.2 Benchmark GEO-bench contains queries from nine datasets. Representative queries from each of the datasets are shown in Figure 2. Further, we tag each of the queries based on a pool of 7 different categories. For tagging, we use the GPT-4 model and manually confirm high recall and precision in tagging. However, owing to such an automated system, the tags can be noisy and should not be considered carefully.

**中文**

B 实验设置 B.1 评估的生成式引擎 所使用的确切提示如清单 1 所示。 B.2 基准 GEO-bench 包含来自九个数据集的查询。每个数据集的代表性查询如图 2 所示。此外，我们根据 7 个不同类别的池来标记每个查询。对于标注，我们使用GPT-4模型并手动确认标注的高召回率和精度。然而，由于这样的自动化系统，标签可能会有噪音，不应该仔细考虑。

### 段落 118 · Page 11

**EN**

Details about each of these queries are presented here: Listing 2: Representative Queries from each of the 9 datasets in GEO-bench 1 ### ORCAS 2 - what does globalization mean 3 - wine pairing list 4 5 ### AllSouls 6 - Are open-access journals the future of academic publishing? 7 - Should the study of non-Western philosophy be a requirement for a philosophy degree in the UK? 8 9 ### Davinci-Debate 10 - Should all citizens receive a basic income? 11 - Should governments promote atheism? 12 13 ### ELI5 14 - Why does my cat kick its toys when playing with them? 15 - what does caffeine actually do your muscles, especially regarding exercising?

**中文**

有关每个查询的详细信息如下： 清单 2：GEO-bench 中 9 个数据集的代表性查询 1 ### ORCAS 2 - 全球化意味着什么 3 - 葡萄酒搭配列表 4 5 ### AllSouls 6 - 开放获取期刊是学术出版的未来吗？ 7 - 非西方哲学的研究应该成为英国哲学学位的要求吗？ 8 9 ### 达芬奇辩论10 - 所有公民都应该获得基本收入吗？ 11 - 政府应该宣扬无神论吗？ 12 13 ### ELI5 14 - 为什么我的猫在玩玩具时会踢玩具？ 15 - 咖啡因实际上对你的肌肉有什么作用，尤其是在锻炼时？

### 段落 119 · Page 11

**EN**

16 17 ### GPT-4 18 - What are the benefits of a keto diet? 19 - What are the most profound impacts of the Renaissance period on modern society? 20 21 ### LIMA 22 - What are the primary factors that influence consumer behavior? 23 - What would be a great twist for a murder mystery? I 'm looking for something creative, not to rehash old tropes.

**中文**

16 17 ### GPT-4 18 - 生酮饮食有什么好处？ 19 - 文艺复兴时期对现代社会最深远的影响是什么？ 20 21 ### LIMA 22 - 影响消费者行为的主要因素是什么？ 23 - 对于谋杀之谜来说，什么是一个大转折？我正在寻找一些有创意的东西，而不是重复旧的比喻。

### 段落 120 · Page 11

**EN**

24 25 ### MS-Macro 26 - what does monogamous 27 - what is the normal fbs range for children 28 29 ### Natural Questions 30 - where does the phrase bee line come from 31 - what is the prince of persia in the bible 32 33 ### Perplexity.ai 34 - how to gain more followers on LinkedIn 35 - why is blood sugar higher after a meal • Difficulty Level: The complexity of the query, ranging from simple to complex. • Nature of Query: The type of information sought by the query, such as factual, opinion, or comparison. • Genre: The category or domain of the query, such as arts and entertainment, finance, or science.

**中文**

24 25 ### MS-Macro 26 - 一夫一妻制是什么 27 - 孩子的正常脸书范围是多少 28 29 ### 自然问题 30 - 蜜蜂线这个短语来自哪里 31 - 圣经中的波斯王子是什么 32 33 ### Perplexity.ai 34 - 如何在 LinkedIn 上获得更多关注者 35 - 为什么饭后血糖会更高 • 难度级别：查询的复杂程度，从简单到复杂。 • 查询的性质：查询所寻求的信息类型，例如事实、意见或比较。 • 类型：查询的类别或领域，例如艺术和娱乐、金融或科学。

### 段落 121 · Page 11

**EN**

• Specific Topics: The specific subject matter of the query, such as physics, economics, or computer science. • Sensitivity: Whether the query involves sensitive topics or not. • User Intent: The purpose behind the user’s query, such as research, purchase, or entertainment. • Answer Type: The format of the answer that the query is seeking, such as fact, opinion, or list. B.3 Evaluation Metrics We use 7 different subjective impression metrics, whose prompts are presented in our our public repository: https://github.com/GEOoptim/GEO.

**中文**

• 特定主题：查询的特定主题，例如物理学、经济学或计算机科学。 • 敏感度：查询是否涉及敏感主题。 • 用户意图：用户查询背后的目的，例如研究、购买或娱乐。 • 答案类型：查询所寻求的答案的格式，例如事实、意见或列表。 B.3 评估指标 我们使用 7 种不同的主观印象指标，其提示显示在我们的公共存储库中：https://github.com/GEOoptim/GEO。

### 段落 122 · Page 11

**EN**

B.4 GEO Methods We propose 9 differentGenerative Engine Optimizationmethods to optimize website content for generative engines. We evaluate these methods on the complete GEO-bench test split. Further, to

**中文**

B.4 GEO 方法 我们提出了 9 种不同的生成式引擎优化方法来优化生成式引擎的网站内容。我们在完整的 GEO-bench 测试中评估这些方法。此外，为了

### Page 12

### 段落 123 · Page 12

**EN**

KDD ’24, August 25–29, 2024, Barcelona, Spain Pranjal Aggarwal et al. Method Position-Adjusted Word Count Subjective Impression Word Position Overall Rel. Infl. Unique Div. FollowUp Pos.

**中文**

KDD '24，2024 年 8 月 25-29 日，西班牙巴塞罗那 Pranjal Aggarwal 等人。方法 位置调整字数 主观印象 字位置 整体相关。膨胀。独特的部门。跟进职位。

### 段落 124 · Page 12

**EN**

Count Average Performance withoutGenerative Engine Optimization No Optimization 19.7(±0.7) 19.6(±0.5) 19.8(±0.6) 19.8(±0.9) 19.8(±1.6) 19.8(±0.6) 19.8(±1.1) 19.8(±1.0) 19.8(±1.0) 19.8(±0.9) 19.8(±0.9) Non-PerformingGenerative Engine Optimizationmethods Keyword Stuffing 19.6(±0.5) 19.5(±0.6) 19.8(±0.5) 20.8(±0.8) 19.8(±1.0) 20.4(±0.5) 20.6(±0.9) 19.9(±0.9) 21.1(±1.0) 21.0(±0.9) 20.6(±0.7) Unique Words 20.6(±0.6) 20.5(±0.7) 20.7(±0.5) 20.8(±0.7) 20.3(±1.3) 20.5(±0.3) 20.9(±0.3) 20.4(±0.7) 21.5(±0.6) 21.2(±0.4) 20.9(±0.4) High-PerformingGenerative Engine Optimizationmethods Easy-to-Understand 21.5(±0.7) 22.0(±0.8) 21.5(±0.6) 21.0(±1.1) 21.1(±1.8

**中文**

计算没有生成式引擎优化的平均性能 无优化 19.7(±0.7) 19.6(±0.5) 19.8(±0.6) 19.8(±0.9) 19.8(±1.6) 19.8(±0.6) 19.8(±1.1) 19.8(±1.0) 19.8(±1.0) 19.8(±0.9) 19.8(±0.9) 不良生成式引擎优化方法 关键词堆砌 19.6(±0.5) 19.5(±0.6) 19.8(±0.5) 20.8(±0.8) 19.8(±1.0) 20.4(±0.5) 20.6(±0.9) 19.9(±0.9) 21.1(±1.0) 21.0(±0.9) 20.6(±0.7) 独特词 20.6(±0.6) 20.5(±0.7) 20.7(±0.5) 20.8(±0.7) 20.3(±1.3) 20.5(±0.3) 20.9(±0.3) 20.4(±0.7) 21.5(±0.6) 21.2(±0.4) 20.9(±0.4) 易于理解的高性能发电引擎优化方法 21.5(±0.7) 22.0(±0.8) 21.5(±0.6) 21.0(±1.1) 21.1(±1.8

### 段落 125 · Page 12

**EN**

) 21.2(±0.9) 20.9(±1.1) 20.6(±1.0) 21.9(±1.1) 21.4(±0.9) 21.3(±1.0) Authoritative 21.3(±0.7) 21.2(±0.9) 21.1(±0.8) 22.3(±0.8) 22.9(±0.8) 22.1(±0.9) 23.2(±0.7) 21.9(±0.4) 23.9(±1.2) 23.0(±1.1) 23.1(±0.7) Technical Terms 22.5(±0.6) 22.4(±0.6) 22.5(±0.6) 21.2(±0.7) 21.8(±0.8) 20.5(±0.5) 21.1(±0.6) 20.5(±0.6) 22.1(±0.6) 21.2(±0.2) 21.4(±0.4) Fluency Optimization24.4(±0.8) 24.4(±0.6) 24.4(±0.8) 21.3(±0.9) 23.2(±1.5) 21.2(±1.0) 21.4(±1.4) 20.8(±1.3) 23.2(±1.8) 21.5(±1.3) 22.1(±1.2) Cite Sources 25.5(±0.7) 25.3(±0.6) 25.3(±0.6) 22.8(±0.9) 24.2(±0.7) 21.7(±0.3) 22.3(±0.8) 21.3(±0.9) 23.5(±0.4) 21.7(±0.6) 22.9(±0.5) Quotation Addition 27.5(±0.8) 27.6(

**中文**

) 21.2(±0.9) 20.9(±1.1) 20.6(±1.0) 21.9(±1.1) 21.4(±0.9) 21.3(±1.0) 权威 21.3(±0.7) 21.2(±0.9) 21.1(±0.8) 22.3(±0.8) 22.9(±0.8) 22.1(±0.9) 23.2(±0.7) 21.9(±0.4) 23.9(±1.2) 23.0(±1.1) 23.1(±0.7) 技术术语 22.5(±0.6) 22.4(±0.6) 22.5(±0.6) 21.2(±0.7) 21.8(±0.8) 20.5(±0.5) 21.1(±0.6) 20.5(±0.6) 22.1(±0.6) 21.2(±0.2) 21.4(±0.4) 流畅度优化24.4(±0.8) 24.4(±0.6) 24.4(±0.8) 21.3(±0.9) 23.2(±1.5) 21.2(±1.0) 21.4(±1.4) 20.8(±1.3) 23.2(±1.8) 21.5(±1.3) 22.1(±1.2) 引用来源 25.5(±0.7) 25.3(±0.6) 25.3(±0.6) 22.8(±0.9) 24.2(±0.7) 21.7(±0.3) 22.3(±0.8) 21.3(±0.9) 23.5(±0.4) 21.7(±0.6) 22.9(±0.5) 报价添加27.5(±0.8) 27.6(

### 段落 126 · Page 12

**EN**

±0.8) 27.1(±0.6) 24.4(±1.0) 26.7(±1.1) 24.6(±0.7) 24.9(±0.9) 23.2(±0.9) 26.4(±1.0) 24.1(±1.2) 25.5(±0.9) Statistics Addition 25.8(±1.2) 26.0(±0.8) 25.5(±1.2) 23.1(±1.4) 26.1(±0.9) 23.6(±0.9) 24.5(±1.2) 22.4(±1.2) 26.1(±1.2) 23.8(±1.2) 24.8(±1.1) Table 6: Absolute impression metrics of GEO methods on GEO-bench.

**中文**

±0.8) 27.1(±0.6) 24.4(±1.0) 26.7(±1.1) 24.6(±0.7) 24.9(±0.9) 23.2(±0.9) 26.4(±1.0) 24.1(±1.2) 25.5(±0.9) 统计相加25.8(±1.2) 26.0(±0.8) 25.5(±1.2) 23.1(±1.4) 26.1(±0.9) 23.6(±0.9) 24.5(±1.2) 22.4(±1.2) 26.1(±1.2) 23.8(±1.2) 24.8(±1.1) 表 6：GEO-bench 上 GEO 方法的绝对印象指标。

### 段落 127 · Page 12

**EN**

Compared to baselines, simple methods like Keyword Stuffing traditionally used in SEO don’t perform well. However, our proposed methods such as Statistics Addition and Quotation Addition show strong performance improvements across all metrics. The best methods improve upon baseline by 41% and 28% on Position-Adjusted Word Count and Subjective Impression respectively. Method Position-Adjusted Word Count Subjective Impression Word Position Overall Rel. Infl. Unique Div. FollowUp Pos.

**中文**

与基线相比，SEO 中传统使用的关键字填充等简单方法效果不佳。然而，我们提出的方法（例如统计加法和报价加法）在所有指标上都显示出强大的性能改进。最好的方法在位置调整字数和主观印象上分别比基线提高了 41% 和 28%。方法 位置调整字数 主观印象 字位置 整体相关。膨胀。独特的部门。跟进职位。

### 段落 128 · Page 12

**EN**

Count Average Performance without Generative Engine Optimization No Optimization 24.0 24 .4 24 .1 24 .7 24 .7 24 .7 24 .7 24 .7 24 .7 24 .7 24 .7 Non-Performing Generative Engine Optimization methods Keyword Stuffing 21.9 21 .4 21 .9 26 .3 27 .2 27 .2 30 .2 27 .9 28 .2 26 .9 28 .1 Unique Words 24.0 23 .7 23 .6 24 .9 25 .1 24 .7 24 .4 23 .0 23 .6 23 .9 24 .1 High-Performing Generative Engine Optimization methods Authoritative 25.6 25 .7 25 .9 28 .9 30 .9 31 .2 31 .7 31 .5 26 .9 29 .5 30 .6 Fluency Optimization 25.8 26 .2 26 .0 28 .9 29 .4 29 .8 30 .6 30 .1 29 .6 29 .6 30 .0 Cite Sources 26.6 26 .9 26 .8 19 .8 20 .7 19 .5 18 .9 20 .0 18 .5 18 .

**中文**

计数未生成式引擎优化的平均性能 无优化 24.0 24 .4 24 .1 24 .7 24 .7 24 .7 24 .7 24 .7 24 .7 24 .7 24 .7 表现不佳的生成式引擎优化方法 关键字堆砌 21.9 21 .4 21 .9 26 .3 27 .2 27 .2 30 .2 27 .9 28 .2 26 .9 28 .1 独特单词 24.0 23 .7 23 .6 24 .9 25 .1 24 .7 24 .4 23 .0 23 .6 23 .9 24 .1 高性能生成式引擎优化方法 权威 25.6 25 .7 25 .9 28 .9 30 .9 31 .2 31 .7 31 .5 26 .9 29 .5 30 .6 流畅度优化 25.8 26 .2 26 .0 28 .9 29 .4 29 .8 30 .6 30 .1 29 .6 29 .6 30 .0 引用来源 26.6 26 .9 26 .8 19 .8 20 .7 19 .5 18 .9 20 .0 18 .5 18 .

### 段落 129 · Page 12

**EN**

9 19 .0 Quotation Addition 28.8 28 .7 29.1 31.4 31 .9 31 .9 32 .3 31 .4 31 .7 30 .9 32 .1 Statistics Addition 25.8 26 .6 26 .2 31 .6 33 .4 34 .0 33 .7 34 .0 33 .3 33 .1 33.9 Table 7: Performance improvement of GEO methods on GEO-bench with Perplexity.ai as generative engine.

**中文**

9 19 .0 报价添加 28.8 28 .7 29.1 31.4 31 .9 31 .9 32 .3 31 .4 31 .7 30 .9 32 .1 统计添加 25.8 26 .6 26 .2 31 .6 33 .4 34 .0 33 .7 34 .0 33 .3 33 .1 33.9 表 7：以 Perplexity.ai 作为生成式引擎的 GEO 方法在 GEO-bench 上的性能改进。

### 段落 130 · Page 12

**EN**

Compared to the baselines simple methods such as Keyword Stuffing traditionally used in SEO often perform worse. However, our proposed methods such as Statistics Addition and Quotation Addition show strong performance improvements across the board. The best performing methods improve upon baseline by 22% on Position-Adjusted Word Count and 37% on Subjective Impression. reduce variance in results, we run our experiments on five different random seeds and report the average. B.5 Prompts for GEO methods We present all prompts in our our public repository: https://github. com/GEO-optim/GEO. GPT-3.5 turbo was used for all experiments.

**中文**

与基线相比，简单的方法（例如传统上用于 SEO 的关键字填充）通常表现较差。然而，我们提出的方法（例如统计加法和报价加法）显示出全面的强​​大性能改进。表现最佳的方法在位置调整字数方面比基线提高了 22%，在主观印象方面提高了 37%。减少结果的方差，我们对五个不同的随机种子进行实验并报告平均值。 B.5 GEO 方法的提示 我们在我们的公共存储库中提供所有提示：https://github。 com/GEO-optim/GEO.所有实验均使用 GPT-3.5 Turbo。

### 段落 131 · Page 12

**EN**

C RESULTS We perform experiments on 5 random seeds and present results with statistical deviations in Table 6 C.1 GEO in the Wild : Experiments with Deployed Generative Engine We also evaluate our proposed Generative Engine Optimization methods on real-world deployed Generative Engine: Perplexity.ai. Since perplexity.ai does not allow the user to specify source URLs, we instead provide source text as file uploads to perplexity.ai while ensuring all answers are generated only using the file sources provided. We evaluate all our methods on a subset of 200 samples of our test set. Results using Perplexity.ai are shown in Table 7.

**中文**

C 结果 我们对 5 个随机种子进行实验，并在表 6 C.1 GEO 野外：部署生成式引擎的实验中呈现带有统计偏差的结果。我们还在现实世界部署的生成式引擎：Perplexity.ai 上评估了我们提出的生成式引擎优化方法。由于 perplexity.ai 不允许用户指定源 URL，因此我们将源文本作为文件上传到 perplexity.ai 提供，同时确保仅使用提供的文件源生成所有答案。我们在测试集的 200 个样本的子集上评估我们的所有方法。使用 Perplexity.ai 的结果如表 7 所示。
