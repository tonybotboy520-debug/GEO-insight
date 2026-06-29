# 改进召回和引入重排提升 RAG 架构下的 LLM 应用效果

- ID: 208
- 类型: html
- 分类: 06_deep_geo_articles/domestic
- 主题: RAG召回/重排
- 原文链接: https://developer.volcengine.com/articles/7382248378773536806
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

改进召回（Retrieval）和引入重排（Reranking）提升RAG架构下的LLM应用效果 - 文章 - 开发者社区 - 火山引擎 文档 备案 控制台 登录 免费开始使用 首页 AI 大模型体验中心 动手实验室 Agent 评测集 AI 案例广场 火山杯大赛 学习中心 社区 去发布 首页 AI 大模型体验中心 动手实验室 Agent 评测集 AI 案例广场 学习中心 社区 改进召回（Retrieval）和引入重排（Reranking）提升RAG架构下的LLM应用效果 AI工程化 开源 技术 动手点关注 干货不迷路 如前文 LLM应用架构之检索增强（RAG）的缘起与架构介绍 ，RAG架构很好的解决了当前大模型Prompt learning过程中context window限制等问题，整体架构简明清晰，易于实现，得到了广泛的应用，但实际落地过程中有大量的实际问题需要改进优化。 llamaindex实现下的RAG架构 以RAG召回为例，最原始的做法是通过top-k的方式从向量数据库中检索背景数据然后直接提交给LLM去生成答案，但这样存在检索出来的chunks并不一定完全和上下文相关的问题，最后导致大模型生成的结果质量不佳。

### 段落 2

这个问题很大程度上是因为召回相关性不够或者是召回数量太少导致的，从扩大召回这个角度思考，借鉴推荐系统做法，引入粗排或重排的步骤来改进效果。其基本思路就是，原有的top-k向量检索召回扩大召回数目，再引入粗排模型，这里的模型可以是策略，轻量级的小模型，或者是LLM，对召回结果结合上下文进行重排，通过这样的改进模式可以有效提升RAG的效果。 下面介绍llamaindex在这方面的一些具体思路和实现。 1）基于LLM的召回或重排 在逻辑概念上，这种方法使用 LLM 来决定哪些文档/文本块与给定查询相关。prompt由一组候选文档组成，这时LLM 的任务是选择相关的文档集，并用内部指标对其相关性进行评分。为了避免因为大文档chunk化带来的内容分裂，在建库阶段也可做了一定优化，利用summary index对大文档进行索引。 基于 LLM 的检索工作原理简图 在LLM开发中有一个原则就是尽可能的使用大模型的能力，LLM并不只是最后作答，在关键词增强，答案一致性判定等上面都可以使用，在这里就可以利用大模型来判定生成结果最合适的候选问答。如何做好prompt就是关键，这是llamaindex内置的prompt，可以看到，这里用到了大模型的few-shot能力： A list of documents is shown below. Each document has a number next to it along with a summary of the document.

### 段落 3

**EN**

A question is also provided. Respond with the numbers of the documents you should consult to answer the question, in order of relevance, as well as the relevance score. The relevance score is a number from 1 – 10 based on how relevant you think the document is to the question. Do not include any documents that are not relevant to the question.

**中文**

还提供了一个问题。请回答您为回答问题而应参考的文档数量（按相关性顺序排列）以及相关性分数。相关性分数是 1 到 10 之间的数字，具体取决于您认为文档与问题的相关程度。不要包含与问题无关的任何文件。

### 段落 4

Example format: Document 1 : <summary of document 1 > Document 2 : <summary of document 2 > … Document 10 : <summary of document 10 > Question: <question> Answer: Doc: 9 , Relevance: 7 Doc: 3 , Relevance: 4 Doc: 7 , Relevance: 3 Let 's try this now: {context_str} Question: {query_str} Answer: 另外，这一召回过程可以执行多次，形成批次，这样可以更大范围召回相关文档，然后将每个批次从大模型获得的结果打分进行汇总，获得最终的候选文档。llama-index提供了两种形式的抽象：作为独立的检索模块（ListIndexLLMRetriever）或重排模块（LLMRerank）。 LLM Retriever (ListIndexLLMRetriever) 该模块是通过列表索引定义的，列表索引只是将一组节点存储为一个平面列表。你可以在一组文档上建立列表索引，然后使用 LLM 检索器从索引中检索相关文档。

### 段落 5

**EN**

from llama_index import GPTListIndex from llama_index.indices.list.retrievers import ListIndexLLMRetriever index = GPTListIndex.from_documents(documents, service_context=service_context) # high - level API query_str = "What did the author do during his time in college?" retriever = index.as_retriever(retriever_mode= "llm" ) nodes = retriever.retrieve(query_str) # lower-level API retriever = ListIndexLLMRetriever() response_synthesizer = ResponseSynthesizer.from_args() query_engine = RetrieverQueryEngine(retriever=retriever, response_synthesizer=response_synthesizer) response = query_engine.query(query_str) 通过这种召回模式来代替传统的向量检索模式，这种实现是相对来讲会比较慢，适合召回文档比较少的情况，但可以省去重排阶段。

**中文**

from llama_index import GPTListIndex from llama_index.indices.list.retrievers import ListIndexLLMRetriever index = GPTListIndex.from_documents(documents, service_context=service_context) # 高级 API query_str = "作者在大学期间做了什么？"检索器 = index.as_retriever(retriever_mode= "llm" ) 节点 =检索器.retrieve(query_str) # 较低级别的 API 检索器 = ListIndexLLMRetriever() response_synthesizer = ResponseSynthesizer.from_args() query_engine = RetrieverQueryEngine(retriever=retriever, response_synthesizer=response_synthesizer) response = query_engine.query(query_str) 通过这种认知模式来代替传统的支持搜索模式，这种实现相对来说会比较慢，适合去认知文档比较少的情况，但可以省去重排阶段。

### 段落 6

LLM Reranker (LLMRerank) 它是本方案中典型的一种实现，被定义为 NodePostprocessor 抽象的一部分，用于初始检索传递后的第二阶段处理。后处理器可单独使用，也可作为 RetrieverQueryEngine 调用的一部分使用。在下面的示例中，我们展示了如何在通过向量索引进行初始检索调用后，将后处理器作为独立模块使用。

### 段落 7

**EN**

from llama_index.indices.query.schema import QueryBundle query_bundle = QueryBundle(query_str) # configure retriever retriever = VectorIndexRetriever( index =index, similarity_top_k =vector_top_k, ) retrieved_nodes = retriever.retrieve(query_bundle) # configure reranker reranker = LLMRerank(choice_batch_size= 5 , top_n=reranker_top_n, service_context=service_context) retrieved_nodes = reranker.postprocess_nodes(retrieved_nodes, query_bundle) 需要说明的是，基于LLM召回或重排存在一些缺陷，首先就是慢，第二就是增加了LLM的调用成本，第三，由于打分是分批进行的，存在着无法全局对齐的问题。 对比演示 下面基于top-k和基于LLM召回做一个例子，基于the Great Gatsby(了不起的盖茨比) 和 the 2021 Lyft SEC 10-k两份数据，只对比召回阶段的效果。

**中文**

from llama_index.indices.query.schema import QueryBundle query_bundle = QueryBundle(query_str) # 配置检索器retrieve = VectorIndexRetriever(index =index, approximation_top_k =vector_top_k, ) returned_nodes =retrieve.retrieve(query_bundle) # 配置重新排序器 reranker = LLMRerank(choice_batch_size= 5 , top_n=reranker_top_n, service_context=service_context) returned_nodes = reranker.postprocess_nodes(retrieved_nodes, query_bundle) 需要说明的是，基于LLM回收或重排存在的一些缺陷，首先就是慢，第二就是增加了LLM的调用成本，第三，由于打分是分批进行的，存在无法全局拓扑的问题。下面基于top-k和基于LLM认知做一个例子，基于了不起的盖茨比（了不起的盖茨比）和2021 Lyft SEC 10-k两份数据，只对比认知阶段的效果。

### 段落 8

**EN**

The Great Gatsby 在这例子中，将《the Great Gatsby》作为文档对象载入，并在其上建立一个向量索引（块大小设置为 512）。 # LLM Predictor (gpt-3.5-turbo) + service context llm_predictor = LLMPredictor(llm=ChatOpenAI(temperature= 0 , model_name= "gpt-3.5-turbo" )) service_context = ServiceContext.from_defaults(llm_predictor=llm_predictor, chunk_size_limit= 512 ) # load documents documents = SimpleDirectoryReader( '../../../examples/gatsby/data' ).load_data() index = GPTVectorStoreIndex.from_documents(documents, service_context=service_context) 然后，我们定义了一个 get_retrieved_nodes 函数，该函数既可以只对索引进行基于向量检索，也可以进行基于向量检索 + 重排序。

**中文**

在这个例子中，将《了不起的盖茨比》作为文档对象加载，并在其上建立一个支持索引（块大小设置为 512）。 # LLM Predictor (gpt-3.5-turbo) + service context llm_predictor = LLMPredictor(llm=ChatOpenAI(Temperature= 0 , model_name= "gpt-3.5-turbo" )) service_context = ServiceContext.from_defaults(llm_predictor=llm_predictor, chunk_size_limit= 512 ) # 加载文档 Documents = SimpleDirectoryReader( '../../../examples/gatsby/data' ).load_data() index = GPTVectorStoreIndex.from_documents(documents, service_context=service_context) 然后，我们定义了一个 get_retrieved_nodes函数，该函数既可以只对索引进行基于索引的搜索，也可以基于搜索+重排序进行。

### 段落 9

**EN**

def get_retrieved_nodes( query_str, vector_top_k = 10 , reranker_top_n= 3 , with_reranker= False ): query_bundle = QueryBundle(query_str) # configure retriever retriever = VectorIndexRetriever( index =index, similarity_top_k =vector_top_k, ) retrieved_nodes = retriever.retrieve(query_bundle) if with_reranker: # configure reranker reranker = LLMRerank(choice_batch_size= 5 , top_n=reranker_top_n, service_context=service_context) retrieved_nodes = reranker.postprocess_nodes(retrieved_nodes, query_bundle) return retrieved_nodes 然后我们提出一些问题。对于基于原来的向量检索，我们设定 k=3。对于两阶段检索，我们设定向量检索的 k=10 和基于 LLM 的重排序的 n=3。

**中文**

def get_retrieved_nodes( query_str, vector_top_k = 10 , reranker_top_n= 3 , with_reranker= False ): query_bundle = QueryBundle(query_str) # 配置检索器retrieve = VectorIndexRetriever(index =index, approximation_top_k =vector_top_k, ) returned_nodes =retrieve.retrieve(query_bundle) if with_reranker: # configure reranker reranker = LLMRerank(choice_batch_size= 5 , top_n=reranker_top_n, service_context=service_context) returned_nodes = reranker.postprocess_nodes(retrieved_nodes, query_bundle) return returned_nodes 那么我们提出了一些问题。对于基于原来的搜索搜索，我们设置 k=3。对于两阶段搜索，我们设置搜索搜索的k=10并且基于LLM的重排序的n=3。

### 段落 10

测试问题: ”Who was driving the car that hit Myrtle?” 对于那些不熟悉《the Great Gatsby》的人来说，叙述者后来从Gatsby那里发现，开车的其实是Daisy，但Gatsby替她背了黑锅。 检索到的top上下文如下图所示。我们可以看到，在基于嵌入的检索中，前两个文本包含了车祸的语义，但没有提供关于谁是真正责任人的细节。只有第三个文本包含正确答案。 使用top-k向量检索召回的上下文 (baseline) 相反，两阶段方法只返回一个相关的上下文，并且它包含正确的答案。 使用向量检索+重排获得的上下文 2021 Lyft SEC 10-K 测试就 2021 年 Lyft SEC 10-K 提出一些问题，特别是关于 COVID-19 的影响和应对措施。Lyft SEC 10-K 长达 238 页，按 ctrl-f 查找 "COVID-19 "可找到 127 条匹配信息。 使用了与上述 Gatsby 示例类似的设置。主要区别在于，将分块大小设置为 128 而非 512，将 k=5 设置为向量检索基线，将 k=40 和 ranker n=5 设置为向量检索+重排序的组合使用方法。

### 段落 11

测试问题 ：”What initiatives are the company focusing on independently of COVID-19?” 基线的结果如上图所示。可以看到，指数 0、1、3、4 所对应的结果都是直接针对 COVID-19 而采取的措施，尽管该问题是专门针对独立于 COVID-19 大流行的公司措施。 使用top-k向量检索召回的上下文 (baseline) 在方法 2 中，将前 k 项扩大到 40 项，然后使用 LLM 筛选前 5 项，从而得到更多相关结果。独立公司的举措包括 “expansion of Light Vehicles” (1), “incremental investments in brand/marketing” (2), international expansion (3), and accounting for misc. risks such as natural disasters and operational risks in terms of financial performance (4)。 使用向量检索+重排获得的上下文 可以看到，基于LLM的召回或重排相对于传统Top-k直接向量检索在效果上有比较大的提升，但同样存在一些问题，需要结合实际的场景来综合选择。

### 段落 12

2）基于相对轻量的模型和算法 这种做法是LLM模式的一种简化，采用BM25, Cohere Rerank等方法对召回结果进行粗排，在效果和性能上取得折中。 使用例子： cohere_rerank = CohereRerank(api_key=os.environ[ "COHERE_API_KEY" ], top_n=top_k) reranking_query_engine = index.as_query_engine( similarity_top_k =top_k, node_postprocessors =[cohere_rerank], ) ‍ 3）基于规则 在粗排阶段，也可以借鉴推荐系统里的做法一样，在进入精排模型前，粗排模型也可以用一些规则替代，有时候高质量的规则会有更好的表现。在llamaindex中可以设置后处理器（ Postprocessor）。这些后处理器可以在从索引 返回结果后修改查询结果。 比如增加一个优先选择最近的文档的策略。可将其定义为FixedRecencyPostprocessor。

### 段落 13

**EN**

recency_postprocessor = FixedRecencyPostprocessor(service_context=service_context, top_k= 1 ) recency_query_engine = index.as_query_engine( similarity_top_k =top_k, node_postprocessors =[recency_postprocessor], ) 这里面FixedRecencyPostprocessor可以通过过滤chunknode上metadata里的Date字段来进行排序。 > Source (Doc id: 24ec05e1-cb35-492e-8741-fdfe2c582e43): date: 2017-01-28 00:00:00 Under the category: THE WORLDPOST: World Leaders React To The Reality ... > Source (Doc id: 098c2482-ce52-4e31-aa1c-825a385b56a1): date: 2015-01-18 00:00:00 Under the category: POLITICS: The Issue That's Looming Over The Final ...

**中文**

recency_postprocessor = FixRecencyPostprocessor(service_context=service_context, top_k= 1 ) recency_query_engine = index.as_query_engine( approximation_top_k =top_k, node_postprocessors =[recency_postprocessor], ) 这里面FixedRecencyPostprocessor可以通过过滤chunknode上元数据里的日期字段来进行排序。 > Source (Doc id: 24ec05e1-cb35-492e-8741-fdfe2c582e43): 日期: 2017-01-28 00:00:00 类别下: 世界邮报: 世界领导人对现实的反应 ... > 来源 (文档 ID: 098c2482-ce52-4e31-aa1c-825a385b56a1): 日期: 2015-01-18 00:00:00 类别下: 政治: 决赛中隐现的问题......

### 段落 14

值得说明的是，善于使用metadata对于RAG架构中很多问题都有奇效，后 面文章中将介绍Metadata的一些使用案例。 不止如此，在llamaindex中，这些postprocessor是可以联合使用的，形成一些链式规则，比如将刚才的cohere_rerank和recency_postprocessor合并使用，进一步精细化排序。 query_engine = index.as_query_engine( similarity_top_k =top_k, node_postprocessors =[cohere_rerank, recency_postprocessor], ) 总结 RAG架构来自于实际问题，而很多问题都是相似的，在效果优化层面，我们可以借鉴一些推荐系统等传统AI系统的优化经验，将其迁移过来，这对于改进RAG效果有很大的帮助，在后面的文章里，还将继续介绍具体场景的一些使用问题，欢迎关注。 注：本文部分内容参考于llamaindex和qdrant官方博客。

### 段落 15

阅读至此了，分享、点赞、在看三选一吧🙏 0 0 0 0 点赞 评论 收藏 关于作者 AI工程化 关于作者 AI工程化 文章 0 获赞 0 收藏 0 相关资源 KubeZoo: 轻量级 Kubernetes 多租户方案探索与实践 伴随云原生技术的发展，多个租户共享 Kubernetes 集群资源的业务需求应运而生，社区现有方案各有侧重，但是在海量小租户的场景下仍然存在改进空间。本次分享对现有多租户方案进行了总结和对比，然后提出一种基于协议转换的轻量级 Kubernetes 网关服务：KubeZoo，该方案能够显著降低多租户控制面带来的资源和运维成本，同时提供安全可靠的租户隔离性。 点击下载 相关产品 推荐阅读 TRAE 中国版「优速通」抽奖活动开启！助你告别高峰期等待 Cursor 3.0 来了！界面大改！ 2026年4月GitHub热门开源项目榜单：AI智能体正式迈入工业化协作时代 TRAE 中国版「优速通」抽奖活动第二期开启！ 四款AI视频解说工具横评：2026年深度实测与选型 评论 未登录 看完啦， 登录 分享一下感受吧～ 暂无评论
