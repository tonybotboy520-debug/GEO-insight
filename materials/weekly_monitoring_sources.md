# GEO 每周固定监控源清单

更新时间：2026-06-29  
用途：每周检查是否出现新的 GEO / AI Search / AEO / LLM Search / RAG citation / AI visibility 相关论文、官方文档、行业研究和资讯文章。发现新内容后，按当前网站格式生成摘要、GEO 原理、核心观点和中英对照阅读文件，并追加到站点数据。

## 监控原则

- 优先级 P0：论文、官方平台文档、搜索/AI 平台的一手数据更新。
- 优先级 P1：有数据样本、实验方法、产品指标或行业调查的研究型文章。
- 优先级 P2：观点文章、实践指南、工具榜单、新闻报道，只在有明确新观点或新证据时收录。
- 每周只收录“新增或明显更新”的内容，避免重复收录同一主题的泛化文章。
- 对英文内容生成逐段中英对照；纯中文内容不重复翻译。
- 每条新增内容必须保留远程原文 URL，不再保存本地原始 HTML/PDF 快照。

## P0 学术论文与预印本

| 来源 | 固定入口 / 查询 | 每周检索关键词 | 收录条件 |
|---|---|---|---|
| arXiv - GEO 精确查询 | https://arxiv.org/search/?query=%22Generative+Engine+Optimization%22&searchtype=all | `Generative Engine Optimization`, `GEO`, `AI search`, `citation`, `visibility` | 标题/摘要直接涉及 GEO、AI 搜索引用、品牌可见度、答案引擎优化 |
| arXiv - AI search / citation | https://arxiv.org/search/?query=%22AI+search%22+%22citation%22&searchtype=all | `AI search citation`, `source citation`, `cited responses`, `answer engines` | 涉及生成式搜索如何选源、引用、归因或吸收来源 |
| arXiv - RAG 与检索 | https://arxiv.org/search/?query=%22retrieval-augmented%22+%22search%22&searchtype=all | `RAG`, `retrieval augmented generation`, `rerank`, `long-document retrieval` | 对 GEO 内容结构、召回、重排、引用有可迁移价值 |
| arXiv - LLM 信息检索 | https://arxiv.org/search/?query=%22large+language+models%22+%22information+retrieval%22&searchtype=all | `LLM for IR`, `information retrieval`, `ranking`, `retriever bias` | 检索架构、排序、来源偏差、LLM 检索综述 |
| arXiv API | https://export.arxiv.org/api/query | 同上 | 后续自动化优先用 API 拉取候选，按发布时间去重 |
| Semantic Scholar | https://www.semanticscholar.org/search?q=generative%20engine%20optimization | `generative engine optimization`, `AI search citation`, `LLM search` | 用于补充 arXiv 未覆盖或已发表版本 |
| ACL Anthology | https://aclanthology.org/search/?q=retrieval%20augmented%20generation | `RAG`, `citation`, `retrieval`, `LLM search` | NLP/IR 会议论文，尤其是 RAG、引用可靠性、搜索对齐 |
| OpenReview | https://openreview.net/search?term=generative%20engine%20optimization | `GEO`, `LLM search`, `retrieval`, `citation` | ICLR/NeurIPS/ICML/WWW/KDD 等会议投稿和评审版 |
| ACM Digital Library | https://dl.acm.org/action/doSearch?AllField=generative+engine+optimization | `generative search`, `AI search`, `information retrieval` | TOIS、SIGIR、WWW、KDD 等正式论文 |
| DBLP | https://dblp.org/search?q=generative%20engine%20optimization | `GEO`, `AI search`, `retrieval augmented` | 用于发现正式出版版本和作者后续作品 |

## P0 官方平台与搜索生态

| 来源 | 固定入口 | 每周关注点 | 收录条件 |
|---|---|---|---|
| Google Search Central Blog | https://developers.google.com/search/blog | AI features、structured data、robots、sitemaps、Search Console、AI optimization | Google 官方改变 AI 搜索、抓取、索引、预览或结构化数据规则 |
| Google Search 产品更新 | https://blog.google/products-and-platforms/products/search/ | AI Overviews、AI Mode、Search 产品功能 | 与 AI 搜索展示、来源引用、发布者可见度有关 |
| Google Search 文档 | https://developers.google.com/search/docs | AI features、SEO fundamentals、robots、structured data | 文档新增或修改，尤其影响“可抓取、可索引、可引用” |
| Bing Webmaster Blog | https://blogs.bing.com/webmaster | AI Performance、IndexNow、Webmaster Tools | Bing / Copilot 引用、citation、grounding query 相关更新 |
| Bing Search Blog | https://blogs.bing.com/search | AI Visibility Insights、Copilot、Bing AI summaries | AI 可见度指标、citation share、intent/topic 等功能更新 |
| Microsoft Advertising / AI Performance | https://about.ads.microsoft.com/ | AI Performance Dashboard、publisher visibility | 微软对 AI web / citation reporting 的方法论更新 |
| OpenAI Developers Docs | https://developers.openai.com/ | OAI-SearchBot、GPTBot、ChatGPT-User、robots | OpenAI 爬虫、搜索、引用、发布者控制相关变化 |
| OpenAI Blog | https://openai.com/news/ | ChatGPT Search、shopping、browser、publisher partnerships | ChatGPT Search / commerce / publisher 相关功能 |
| Anthropic Support / Docs | https://support.claude.com/ | ClaudeBot、Claude-SearchBot、Claude-User | Claude 抓取/搜索访问规则或发布者控制变动 |
| Perplexity Docs / Blog | https://www.perplexity.ai/ | crawler、publisher、Pages、Comet/search features | Perplexity 抓取、引用、出版商合作和搜索产品变化 |
| Cloudflare Blog | https://blog.cloudflare.com/ | AI crawlers、crawl-to-click、pay per crawl、Radar | AI bot 流量、内容授权、爬虫控制、AI 搜索回流数据 |
| Cloudflare AI Crawl Control Docs | https://developers.cloudflare.com/ai-crawl-control/ | bot reference、crawler management、pay per crawl | AI 爬虫治理规则或 bot 列表变化 |
| Cloudflare Radar AI Insights | https://radar.cloudflare.com/ | crawl/refer ratio、AI bot activity | 可用于 GEO 监测口径和行业趋势 |
| IndexNow | https://www.indexnow.org/documentation | URL 提交协议、搜索发现 | 影响新文章发现速度和提交链路 |
| Schema.org | https://schema.org/docs/releases.html | Article、Organization、Product、FAQPage | 实体/结构化词表更新 |

## P1 行业研究、数据与实操指南

| 来源 | 固定入口 | 每周关注点 | 收录条件 |
|---|---|---|---|
| Search Engine Land - GEO 专栏 | https://searchengineland.com/library/ai-seo/generative-engine-optimization | GEO 框架、指标、AI visibility、平台变化 | 有清晰方法论、指标或案例 |
| Search Engine Land - SEO / AI Search | https://searchengineland.com/library/channel/seo | Google/Bing/ChatGPT/Perplexity 搜索变化 | 与 AI 搜索可见度或引用相关 |
| Search Engine Journal | https://www.searchenginejournal.com/ | AEO、GEO、AI search、Google AI Overviews | 新闻和实操指南，有平台变化或研究数据时收录 |
| Ahrefs Blog | https://ahrefs.com/blog/ | AI Overview citations、Brand Radar、AI traffic | 有样本量和数据方法的 AI 引用/可见度研究 |
| Semrush Blog | https://www.semrush.com/blog/ | AI Visibility Toolkit、GEO、AI SEO statistics | 有可操作指标、工具数据或趋势统计 |
| BrightEdge Resources | https://www.brightedge.com/resources | AI Overviews、Generative Parser、brand risk | 企业级 AI 搜索可见度数据 |
| Similarweb Blog | https://www.similarweb.com/blog/ | AI traffic、ChatGPT referral、search behavior | AI 搜索流量和用户行为数据 |
| SparkToro Blog | https://sparktoro.com/blog/ | zero-click、search behavior、AI answer impact | 搜索需求和点击行为变化 |
| Moz Blog | https://moz.com/blog | AI Overviews、technical SEO、entity SEO | 与传统 SEO 到 AI 搜索迁移相关 |
| SISTRIX Blog | https://www.sistrix.com/blog/ | Google SERP、AI Overviews visibility | SERP 变化和可见度数据 |
| Conductor Blog | https://www.conductor.com/blog/ | enterprise SEO、AI search、content intelligence | 企业 SEO / AI search 运营方法 |
| Botify Blog | https://www.botify.com/blog | crawling、indexing、enterprise search | 技术 SEO、抓取/索引适配 |
| Lumar Blog | https://www.lumar.io/blog/ | technical SEO、crawl health、structured data | 技术底座和可抓取性 |
| iPullRank Blog | https://ipullrank.com/blog | AI search、content engineering、SEO research | 深度技术和策略文章 |

## P1 GEO / AI Visibility 工具与实验来源

| 来源 | 固定入口 | 每周关注点 | 收录条件 |
|---|---|---|---|
| Profound Blog | https://www.tryprofound.com/blog | AI visibility、answer engine analytics | 品牌可见度、答案引擎监测、工具数据 |
| Peec AI Blog | https://peec.ai/blog | AI search visibility、GEO tactics | GEO 实操和监测方法 |
| OtterlyAI Blog | https://otterly.ai/blog/ | llms.txt、AI crawler、GEO experiments | 有实验数据或日志分析 |
| Scrunch AI Blog | https://www.scrunchai.com/blog | AI search visibility、brand monitoring | AI 可见度工具和案例 |
| ZipTie.dev / ZipTie Blog | https://ziptie.dev/ | AI search monitoring、citations | AI search 监测和 citation 研究 |
| Writesonic / AI Search Visibility | https://writesonic.com/blog | AI search optimization、GEO tools | 只收录有数据或方法论的新内容 |
| Frase Blog | https://www.frase.io/blog/ | Answer Engine Optimization、content optimization | AEO/GEO 实操和内容结构 |
| Amsive Blog | https://www.amsive.com/insights/ | answer engine optimization、AI search | 企业级 AEO/GEO 方法论 |
| Reboot Online Blog | https://www.rebootonline.com/blog/ | GEO experiments、llms.txt tests | 有实验数据时收录 |

## P2 中文与国内工程来源

| 来源 | 固定入口 / 查询方式 | 每周关注点 | 收录条件 |
|---|---|---|---|
| 腾讯云开发者 | https://cloud.tencent.com/developer/search/article-RAG | RAG、GEO、重排、向量检索、AI 搜索 | 中文工程实践，有结构化方法或案例 |
| 阿里云开发者 | https://developer.aliyun.com/search?q=RAG | RAG、知识库、向量检索、实体对齐 | 与内容召回、检索质量闭环相关 |
| 火山引擎开发者 | https://developer.volcengine.com/search?keyword=RAG | RAG、检索、重排、知识库 | 可迁移到 GEO 内容结构和检索优化 |
| 百度开发者中心 | https://developer.baidu.com/search?keyword=GEO | GEO、AI 搜索、RAG | 只收录较完整的实践指南 |
| SegmentFault | https://segmentfault.com/search?q=GEO | GEO、RAG、AI 搜索 | 技术深度足够、非泛化营销文 |
| CSDN / GitCode | https://so.csdn.net/so/search?q=生成式引擎优化 | GEO、RAG、LLM 检索 | 谨慎筛选，优先长文和工程实践 |
| InfoQ 中文 | https://www.infoq.cn/search?q=RAG | RAG、AI 搜索、知识库 | 行业趋势、技术架构、企业案例 |
| 机器之心 | https://www.jiqizhixin.com/search?search_in=all&keywords=RAG | 论文、RAG、搜索增强 | 论文解读和研究趋势 |
| 量子位 | https://www.qbitai.com/?s=RAG | AI 搜索、RAG、Agent | 仅收录与搜索/检索/引用强相关内容 |

## 每周新增内容处理流程

1. 按本清单抓取或人工检查最近 7 天新增内容。
2. 用 URL、标题、arXiv ID 去重，对照 `assets/data/geo-insights.js` 和 `materials/bilingual_reading/bilingual_index.json`。
3. 候选内容按 P0/P1/P2 评级：
   - P0 必看，符合主题即收录。
   - P1 有数据、实验、指标、方法论才收录。
   - P2 只收录中文高质量长文或工程实践。
4. 对新增内容抽取：
   - 中文标题
   - 英文原标题
   - 原文 URL
   - 摘要重点
   - GEO 相关观点 / 规则
   - 1-5 条核心观点
   - 标签、分类、来源类型、深度评分
5. 生成 `materials/bilingual_reading/.../*.md`：
   - 英文逐段中英对照。
   - 中文内容保留中文段落，不重复翻译。
6. 更新：
   - `assets/data/geo-insights.js`
   - `assets/data/bilingual-reader-data.js`
   - `materials/bilingual_reading/bilingual_index.json`
   - `materials/bilingual_reading/README.md`
7. 校验：
   - 首页/阅读页能打开。
   - 新增条目的“中英对照阅读”和“原文链接”都有效。
   - 不生成本地原始 HTML/PDF 快照链接。

## 每周检索关键词包

英文关键词：

- `Generative Engine Optimization`
- `GEO AI search`
- `answer engine optimization`
- `AI search optimization`
- `AI visibility`
- `AI Overview citations`
- `ChatGPT search citations`
- `Perplexity citations`
- `LLM search source attribution`
- `citation selection`
- `citation absorption`
- `retrieval augmented generation search`
- `long document retrieval`
- `source bias LLM generated content`
- `AI crawlers robots.txt`
- `llms.txt experiment`

中文关键词：

- `生成式引擎优化`
- `GEO 优化`
- `AI 搜索优化`
- `答案引擎优化`
- `AI 可见度`
- `AI 引用`
- `AI 搜索 引用 来源`
- `RAG 检索 重排`
- `向量检索 Rerank`
- `AI 爬虫 robots.txt`
- `llms.txt 实验`
