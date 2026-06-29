# 什么是检索增强生成 (RAG)？ | Google Cloud

- ID: 202
- 类型: html
- 分类: 06_deep_geo_articles/domestic
- 主题: RAG官方机制
- 原文链接: https://cloud.google.com/use-cases/retrieval-augmented-generation?hl=zh-CN
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

什么是检索增强生成 (RAG)？ | Google Cloud 页面内容 主题 RAG 什么是检索增强生成 (RAG)？ RAG（即检索增强生成）是一种 AI 框架，将传统信息检索系统（例如搜索和数据库）的优势与生成式 大语言模型 (LLM) 的功能相结合。通过将您的数据和世界知识与 LLM 语言技能相结合， 接地输出 更准确、更及时，并且与您的具体需求相关。请阅读此电子书，挖掘您的“ 企业真实数据 ”。 免费开始使用 35:30 使用 Gemini Enterprise Agent Platform 上的 Agent Search 和 DIY RAG 为 Gemini 建立依据 检索增强生成是如何工作的？ RAG 通过几个主要步骤来帮助增强生成式 AI 输出： 检索和预处理 ：RAG 利用强大的搜索算法查询外部数据，例如网页、知识库和数据库。检索完毕后，相关信息会进行预处理，包括标记化、词干提取和停用词移除。 接地输出 ：经过预处理的检索到的信息接着会无缝整合到预训练的 LLM 中。此整合增强了 LLM 的上下文，使其能够更全面地理解主题。这种增强的上下文使 LLM 能够生成更精确、更翔实且更具吸引力的回答。 为什么使用 RAG？

### 段落 2

RAG 在传统文本生成方法的基础上增添了多项优势，尤其是在处理事实信息或数据驱动型回答时。以下是使用 RAG 技术的一些主要优势： 获取最新信息 大型语言模型 (LLM) 的知识来源于预训练数据，这使得它们容易给出过时甚至不准确的答案。而 RAG 技术通过为 LLM 提供实时更新的信息，有效克服了这一局限性。 事实依据 LLM 是生成富有创意且引人入胜的文本的强大工具，但有时它们在事实准确性方面会力不从心。这是因为 LLM 是使用大量文本数据训练的，其中可能包含不准确的信息或存在偏差的信息。 将“事实”作为输入提示的一部分提供给 LLM 可以减轻“ 生成式 AI 幻觉 ”。这种方法的关键是确保向 LLM 提供最相关的事实，并确保 LLM 输出完全基于这些事实，同时还要回答用户的问题并遵循系统指令和安全限制。 使用 Gemini 的长上下文窗口 (LCW) 是向 LLM 提供源材料的绝佳方式。如果您需要提供的详细信息超出了 LCW 的限制，或者您需要提高性能，可以使用 RAG 方法来减少 token 的数量，从而节省时间和费用。 使用向量数据库和相关性重新排名算法进行搜索 RAG 通常通过搜索检索事实，而现代搜索引擎现在利用矢量数据库来高效检索相关文档。矢量数据库将文档作为嵌入存储在高维空间中，允许基于语义相似度快速、准确地进行检索。多模态嵌入可用于处理图片、音频和视频等内容，这些媒体嵌入可与文本嵌入或多语言嵌入一起检索。

### 段落 3

Gemini Enterprise Agent Platform 上的 Agent Search 等高级搜索引擎同时使用 语义搜索 和关键字搜索（称为混合搜索），并使用重新排名工具对搜索结果进行评分，以确保返回的排名靠前的搜索结果具有最高相关性。此外，如果查询内容清晰、简洁且无拼写错误，搜索效果会更好；因此，在查找之前，先进的搜索引擎会转换查询并更正拼写错误。 相关性、准确性和质量 RAG 中的检索机制至关重要。您需要在精选的知识库之上使用最佳的语义搜索，以确保检索到的信息与输入的查询或上下文相关。如果您检索的信息不相关，生成的内容可能接地，但与主题无关或不正确。 RAG 通过微调或 提示工程 来优化 LLM，使其完全基于检索到的知识来生成文本，从而有助于最大限度地减少所生成文本中的矛盾和不一致之处。这大大提高了生成文本的质量，并改善了用户体验。

### 段落 4

Gemini Enterprise Agent Platform 中的模型评估 现在可以根据“coherence”“fluency”“groundedness”“safety”“instruction_following”“question_answering_quality”等指标对 LLM 生成的文本和检索的文本块进行评分。这些指标可帮助您衡量从 LLM 中获得的接地文本（对于某些指标，是与您提供的标准答案进行比较）。实施这些评估可为您提供基准测量结果，您可以通过配置搜索引擎、精选来源数据、改进来源布局解析或分块策略，或者在搜索之前优化用户的问题，从而优化 RAG 质量。这种 RAG Ops 指标驱动型方法将帮助您通过不断优化实现高质量的 RAG 和接地输出。 RAG、智能体和聊天机器人 RAG 和接地可集成到任何需要访问新鲜、私有或专业数据的大型语言模型 (LLM) 应用或智能体中。通过访问外部信息，由 RAG 提供支持的 聊天机器人 和对话代理可以利用外部知识提供更加全面、翔实和上下文内容感知的回答，从而改善整体用户体验。 您使用生成式 AI 构建的内容取决于您的数据和应用场景。RAG 和接地可高效、可伸缩地将您的数据引入 LLM。 哪些 Google Cloud 产品和服务与 RAG 相关？

### 段落 5

以下 Google Cloud 产品与检索增强生成相关： Gemini Enterprise Agent Platform RAG 引擎 用于开发上下文增强型 LLM 应用的数据框架，有助于实现检索增强生成。 Gemini Enterprise Agent Platform 上的 Agent Search Agent Search：用 Google 搜索技术赋能您的数据，开箱即用，全托管式，轻松构建搜索和 RAG 应用。 Gemini Enterprise Agent Platform 上的 Vector Search 为 Agent Search 提供支持的超高性能向量索引；能够以高召回率和高查询速率，从大量嵌入集合中进行语义和混合搜索和检索。 BigQuery 可用于训练包括 Agent Platform 上的 Vector Search 模型在内的多种机器学习模型的大型数据集。 Grounded Generation API Gemini 高保真模式，依托 Google 搜索的强大支持和内嵌的事实核查机制，确保信息准确可靠。您也可以选择接入您自己的搜索引擎，定制专属体验。 AlloyDB AI 在 Agent Platform 中运行模型，并使用熟悉的 SQL 查询在您的应用中访问这些模型。使用 Google 模型（如 Gemini）或您自己的自定义模型。 更多详情 通过这些资源详细了解如何使用检索增强生成。

### 段落 6

Google 搜索技术赋能的 RAG RAG 与 Google Cloud 上的数据库 用于构建您自己的搜索和检索增强生成 (RAG) 系统的 API 如何在 BigQuery 中使用 RAG 来增强 LLM 用于熟悉 RAG 的代码示例和快速入门 使用 GKE 且支持 RAG 的生成式 AI 应用的基础设施 迈出下一步 获享 $300 赠金以及 20 多种提供“始终免费”用量的产品，开始在 Google Cloud 上构建项目。 免费开始使用 不知从何入手，需要一点帮助？ 联系销售团队 与值得信赖的合作伙伴携手 寻找合作伙伴 继续浏览 查看所有产品 menu 概览 解决方案 产品 价格 资源 文档 支持 与我们联系  文档 支持 控制台 登录 免费开始使用吧 免费开始使用吧 与我们联系 close 加快数字化转型的速度 在数字化转型之旅中，无论您的企业是处于早期阶段还是已初见成效，Google Cloud 都可以帮助解决最棘手的难题。 了解详情 主要优势 为什么选择 Google Cloud 企业选择我们的首要原因。 AI 与智能体 获取企业级 AI。 多云 在您需要的任何位置运行您的应用。 全球基础架构 在 Google 自用的基础架构上构建应用。 数据云 根据统一数据做出更明智的决策。 现代基础设施云 新一代云基础设施。 安全 保护您的用户、数据和应用。 工作效率与协作 将团队与基于 AI 的应用联系起来。 报告和数据洞见 高管数据洞见 高管观点精选。

### 段落 7

分析师报告 阅读并了解行业分析师对我们的看法。 白皮书 浏览并下载热门白皮书。 客户案例 浏览案例研究和视频。 close 行业解决方案 应用现代化改造 人工智能 API 和应用 数据分析 数据库 基础架构 工作效率与协作 安全 初创公司和中小型企业 查看所有解决方案 行业解决方案 降低费用、提高运营敏捷性并抓住新的市场机遇。 零售 面向零售业价值链的分析工具和协作工具。 快速消费品 适用于快速消费品数字转型与品牌成长的解决方案。 金融服务 面向金融服务业的计算、数据管理和分析工具。 医疗保健和生命科学 推进大规模的研究并推动医疗保健创新。 媒体和娱乐 用于内容制作和分发运营的各种解决方案。 电信 用于部署 5G 并通过 5G 创收的各种混合云和多云端服务。 游戏 帮助您更快地构建游戏并为其扩容的各种 AI 驱动型解决方案。 制造 可优化制造业价值链的各种迁移工具和 AI 工具。 供应链与物流 跨供应链和物流运营实现可持续、高效且有弹性的以数据为依据的操作。 政府 面向政府机构的数据存储、AI 和分析解决方案。 教育 可提供更具吸引力的学习体验的各种教学工具。 没有看到您需要的内容？ 查看所有行业解决方案 应用现代化改造 评估、规划、实施和衡量软件做法与功能，以对贵组织的业务应用组合进行现代化改造和简化。 CAMP 使用 DORA 改进软件交付功能的计划。 对传统应用进行现代化改造 对传统工作负载进行分析和分类，并开始进行云迁移。

### 段落 8

从 PaaS 迁移：Cloud Foundry 或 Openshift 可帮助您将现有容器迁移到 Google 的代管式容器服务的工具。 从大型主机迁移 可帮助您将大型主机应用迁移到云端的自动化工具和规范性指南。 对软件交付进行现代化改造 软件供应链最佳实践 - 内部循环效率、CI/CD 和 S3C。 DevOps 最佳实践 可帮助您在组织中实施 DevOps 的各种流程和资源。 SRE 原则 可帮助您在组织中采用 SRE 的工具和资源。 平台工程设计 全面的托管式服务套件和黄金路径，可用于构建和管理 IDP 或扩大其规模。 设计适合多云环境的架构 使用一致的平台跨多个云管理工作负载。 人工智能 借助 AI 和机器学习技术，让您的企业更加智能高效。 Gemini Enterprise for Customer Experience 构建和管理贯穿整个客户生命周期的智能体。 Gemini Enterprise 面向整个组织的统一智能体产品组合。 AI Commerce Search 面向零售商的 Google 品质的搜索和产品推荐功能。 内置 Gemini 的 Google Cloud 适用于应用开发、编码等的 AI 助理。 物理 AI 模拟、训练和操作新一代机器人、自动驾驶汽车、工业设备和机器。 API 和应用 使用 API、应用和自动化功能，加速创新而无需编写代码。 使用 API 开拓新的业务渠道 吸引开发者与合作伙伴形成生态系统，并为他们提供支持。

### 段落 9

使用 API 发掘旧式应用的潜力 用于对旧式应用进行扩展和现代化改造的各种云服务。 Open Banking APIx 更简单、更快速地安全交付符合 Open Banking 要求的 API。 数据分析 借助可大幅简化分析过程的全代管式无服务器分析平台，即时根据任何规模的数据生成分析洞见。 数据迁移 借助 AI 赋能的迁移服务，迁移您的数据仓库和数据湖并对其进行现代化改造。 数据湖仓一体 利用高性能的开放式数据湖仓一体架构，统一并管理您的多模态数据。 实时分析 通过提取、处理和分析事件流发掘数据洞见。 营销分析 用于收集、分析和利用客户数据的各种解决方案。 数据集 来自 Google、公共来源和商业提供商的数据，可充实您的分析和 AI 计划。 商业智能 用于对 BI 栈进行现代化改造和打造丰富数据体验的解决方案。 数据分析智能体 用于数据生命周期的内置智能体，以及构建您自有智能体的工具。 地理空间分析 可大规模处理地理空间应用场景的综合平台。 数据科学 托管式服务和集成式工作流，可用于构建、管理和扩缩数据科学解决方案。 数据库 借助具备安全性、可靠性和高可用性的全代管式数据服务，迁移和管理企业数据。 数据库迁移 有助于简化数据库迁移生命周期的各种指南和工具。 数据库现代化改造 可对您的运营数据库基础架构进行现代化改造的各种升级服务。 游戏数据库 利用 Google Cloud 数据库构建全球实时游戏。

### 段落 10

Google Cloud 数据库 用于对数据进行迁移、管理和现代化改造的各种数据库服务。 将 Oracle 工作负载迁移到 Google Cloud 重新托管您的 Oracle 工作负载，为其更换平台或者重写代码。 开源数据库 具有企业级支持服务的全代管式开源数据库。 SQL Server on Google Cloud 用于在 Google Cloud 上运行 SQL Server 虚拟机的各种方案。 用于数据库的 Gemini 利用 AI 助力数据库开发和管理。 基础架构 借助适用于 SAP、VMware、Windows、Oracle 和其他工作负载的解决方案，快速完成迁移工作。 应用迁移 可帮助您迁移到云端的各种发现和分析工具。 SAP on Google Cloud 有助于您运行 SAP 应用和 SAP HANA 的各种认证。 高性能计算 可支持任何工作负载的各种计算、存储和网络方案。 Windows on Google Cloud 可协助您运行 Windows 工作负载的工具和合作伙伴。 数据中心迁移 适用于虚拟机、应用和数据库等的迁移解决方案。 Active Assist 提供自动云端资源优化功能和更高的安全性。 虚拟桌面 适用于桌面和应用的远程工作解决方案（VDI 和 DaaS）。 快速迁移和现代化改造计划 用于简化云迁移路径的端到端迁移计划。 备份和灾难恢复 确保满足您的业务连续性需求。

### 段落 11

Red Hat on Google Cloud Google 和 Red Hat 为传统的本地应用和自定义应用提供了一个企业级平台。 跨云网络 简化混合网络和多云网络，并保护您的工作负载、数据和用户。 工作效率与协作 借助直观易用且极具成效的解决方案，改变团队的工作方式。 Google Workspace 面向企业的协作和办公工具。 Google Workspace 基本功能版 为团队提供安全的视频会议功能和现代化协作功能。 Cloud Identity IT 管理员用于管理用户设备和应用的统一平台。 Chrome 企业版 专为企业打造的 ChromeOS、Chrome 浏览器和 Chrome 设备。 安全 检测、调查和应对在线威胁，帮助保护您的企业。 智能体 SOC 借助 AI 代理，实现更好的防护效果。 Web 应用和 API 保护 适用于 Web 应用和 API 的威胁及欺诈防护。 安全和弹性框架 适用于安全和弹性生命周期各个阶段的解决方案。 风险和合规即代码 (RCaC) 通过自动化技术对您的治理、风险与合规性功能进行现代化改造的解决方案。 软件供应链安全 用于提高端到端软件供应链安全的解决方案。 Security Foundation 可帮助您实现可靠安全状况的推荐产品。 初创公司和中小型企业 借助量身定制的解决方案和计划加快初创公司和中小型企业的发展。 初创公司计划 获得财务、业务和技术支持，让您的初创公司迈上新台阶。

### 段落 12

中小型企业 探索网站托管、应用开发、AI 和分析领域的解决方案。 软件即服务 构建更出色的 SaaS 产品，高效伸缩，并推动您的业务增长。 close 精选产品 AI 和机器学习 商业智能 计算 容器 数据分析 数据库 开发者工具 分布式云 混合云和多云 针对特定行业 集成服务 管理工具 地图和地理空间 媒体服务 迁移 网络 运维 工作效率与协作 安全和身份 无服务器 存储 Web3 查看所有产品（100 多款） 精选产品 Gemini Enterprise 应用 一个安全可靠的平台，可助力员工轻松探索、创建、运行和管理 AI 智能体。 Agent Platform 一个统一平台，集机器学习模型、生成式 AI 与智能体构建功能于一体。 Compute Engine 在 Google 的数据中心运行的虚拟机。 Cloud Storage 安全、耐用且可伸缩的对象存储服务。 BigQuery 具备自主数据管理能力的 AI 平台，可用于数据分析和数据科学。 Cloud Run 用于运行容器化应用的全代管式环境。 Google Kubernetes Engine 用于运行容器化应用的代管式环境。 Looker 提供商业智能、数据应用和嵌入式分析的平台。 Apigee API Management 随时随地以直观且可掌控的方式来管理 API 的整个生命周期。 Cloud SQL 适用于 MySQL、PostgreSQL 和 SQL Server 的关系型数据库服务。

### 段落 13

Cloud CDN 用于分发 Web 内容和视频内容的内容分发网络。 没有看到您需要的内容？ 查看所有产品（100 多款） AI 和机器学习 Gemini Enterprise Agent Platform 一个统一平台，集机器学习模型、生成式 AI 与智能体构建功能于一体。 Gemini Enterprise 应用 一个安全可靠的平台，可助力员工轻松探索、创建、运行和管理 AI 智能体。 Gemini Enterprise for Customer Experience 构建和管理贯穿整个客户生命周期的智能体。 Model Garden 一站式获取 Google 及 Google 合作伙伴提供的 200 多个模型。 Customer Experience Agent Studio 使用确定性和生成式 AI 功能构建对话式 AI。 智能体搜索 为您的企业应用和体验构建 Google 品质的搜索功能。 Speech-to-Text 支持 125 种语言的语音识别和转录服务。 Text-to-Speech 支持 220 多种语音和 40 多种语言的语音合成服务。 Translation AI 提供语言检测、翻译和术语表支持。 Vision AI 用于检测情绪、文本等内容的各种自定义模型和预训练模型。 联络中心即服务 云原生全渠道联络中心解决方案。 没有看到您需要的内容？ 查看所有 AI 和机器学习产品 商业智能 Looker 提供商业智能、数据应用和嵌入式分析的平台。

### 段落 14

数据洞察 用于信息汇总、报告和分析的交互式数据套件。 计算 Compute Engine 在 Google 的数据中心运行的虚拟机。 App Engine 适用于应用和后端的无服务器应用平台。 Cloud GPU 可助力机器学习、科学计算和 3D 可视化的 GPU。 Migrate to Virtual Machines 用于将服务器和虚拟机迁移到 Compute Engine。 Spot 虚拟机 适用于批量作业和容错工作负载的计算实例。 批量 用于安排批量作业的全代管式服务。 单租户节点 满足合规性、许可及管理需求的专用硬件。 裸金属 用于在 Google Cloud 上运行特殊工作负载的基础架构。 Recommender 针对 Google Cloud 产品和服务的使用建议。 VMware Engine 全代管式原生 VMware Cloud Foundation 软件栈。 Cloud Run 用于运行容器化应用的全代管式环境。 没有看到您需要的内容？ 查看所有计算产品 容器 Google Kubernetes Engine 用于运行容器化应用的代管式环境。 Cloud Run 用于运行容器化应用的全代管式环境。 Cloud Build 用于在 Docker 容器中运行构建步骤的解决方案。 Artifact Registry 构建制品和依赖项的软件包管理器。 Cloud Code 可提供 IDE 支持，帮助您编写、运行和调试 Kubernetes 应用。

### 段落 15

Cloud Deploy 以全代管式方式持续交付到 GKE 和 Cloud Run。 Migrate to Containers 用于将虚拟机迁移到 GKE 上的系统容器的各种组件。 Deep Learning Containers 具有各种数据科学框架、库和工具的容器。 Knative 用于构建 Kubernetes 原生云软件的组件。 数据分析 BigQuery 具备自主数据管理能力的 AI 平台，可用于数据分析和数据科学。 Managed Service for Apache Spark 零运维无服务器或托管式集群，在 Lightning Engine 的加持下实现全面加速。 Dataflow 用于流式处理和批处理的实时分析服务。 Looker 提供商业智能、数据应用和嵌入式分析的平台。 湖仓一体 具有企业级存储和性能的开放式湖仓一体平台。 Pub/Sub 用于提取和传送事件的消息传递服务。 Managed Service for Apache Airflow 基于 Apache Airflow 构建的工作流编排服务。 Knowledge Catalog 始终在线的 AI 目录，旨在为智能体提供全局上下文。 数据分析智能体 用于数据生命周期的内置智能体，以及构建您自有智能体的工具。 数据分析迁移服务 AI 赋能的云原生数据迁移服务，可免费使用。

### 段落 16

Managed Service for Apache Kafka 用于运行高可用性 Apache Kafka 集群的托管式 Kafka 服务。 没有看到您需要的内容？ 查看所有数据分析产品 数据库 AlloyDB for PostgreSQL 与 PostgreSQL 兼容的全代管式数据库，适用于企业工作负载。 Cloud SQL 面向 MySQL、PostgreSQL 和 SQL Server 的全代管式数据库。 Firestore 扩容能力极强的无服务器 NoSQL 文档数据库，兼容 MongoDB。 Spanner 云原生关系型数据库，规模不受限制，可用性高达 99.999%。 Bigtable 适用于大规模、低延迟工作负载的云原生宽列数据库。 Datastream 无服务器变更数据捕获和复制服务。 Database Migration Service 使用无服务器技术以最短停机时间迁移到 Cloud SQL。 裸金属解决方案 面向 Oracle 工作负载的全托管式基础设施。 Memorystore 全托管式 Redis 和 Memcached，可实现亚毫秒级的数据访问。 开发者工具 Artifact Registry 构建制品和依赖项的通用软件包管理器。 Cloud Code 可提供 IDE 支持，帮助您编写、运行和调试 Kubernetes 应用。 Cloud Build 持续集成和持续交付平台。

### 段落 17

Cloud Deploy 以全代管式方式持续交付到 GKE 和 Cloud Run。 Cloud Deployment Manager 用于创建和管理 Google Cloud 资源的服务。 Cloud SDK 适用于 Google Cloud 的命令行工具和库。 Cloud Scheduler 用于自动执行以及管理任务的 Cron 作业调度器。 Cloud Source Repositories 用于存储、管理和跟踪代码的私有 Git 代码库。 Infrastructure Manager 使用 Terraform 自动管理基础架构。 Cloud Workstations 安全的代管式云端开发环境。 Gemini Code Assist AI 赋能的助理，可在 Google Cloud 和 IDE 中使用。 没有看到您需要的内容？ 查看所有开发者工具 分布式云 Google Distributed Cloud Connected 适用于边缘工作负载的分布式云服务。 Google Distributed Cloud Air-gapped 适用于经过网闸隔离的工作负载的分布式云。 混合云和多云 Google Kubernetes Engine 用于运行容器化应用的代管式环境。 Apigee API Management API 管理、开发和安全平台。 Migrate to Containers 用于将工作负载和现有应用迁移到 GKE 的工具。

### 段落 18

Cloud Build 用于在 Google Cloud 基础架构上执行构建作业的服务。 可观测性 监控、日志记录和应用性能套件。 Cloud Service Mesh 基于 Envoy 和 Istio 的全托管式服务网格。 Google Distributed Cloud 适用于边缘和数据中心的全代管式解决方案。 针对特定行业 反洗钱 AI 借助 AI 检测可疑的潜在洗钱活动。 Cloud Healthcare API 用于衔接现有医疗保健系统与 Google Cloud 上应用的解决方案。 关联 Fitbit 设备 通过 Google Cloud 上的关联 Fitbit 数据全方位了解患者。 电信网络自动化 适用于电信网络的现成云原生自动化。 电信数据编织 使用自动化方法进行电信数据管理和分析。 Telecom Subscriber Insights 注入数据以提升订阅者获取率和留存率。 Spectrum Access System (SAS) 控制对公民宽带无线电服务 (CBRS) 的基本访问权限。 集成服务 Application Integration 无需编写代码即可连接到第三方应用并保证数据一致性。 Workflows 无服务器产品和 API 服务的工作流编排。 Apigee API Management 随时随地以直观且可掌控的方式来管理 API 的整个生命周期。 Cloud Tasks 用于异步执行任务的任务管理服务。

### 段落 19

Cloud Scheduler 用于自动执行以及管理任务的 Cron 作业调度器。 Managed Service for Apache Spark 零运维无服务器或托管式集群，在 Lightning Engine 的加持下实现全面加速。 Cloud Data Fusion 用于构建和管理数据流水线的数据集成服务。 Managed Service for Apache Airflow 基于 Apache Airflow 构建的工作流编排服务。 Pub/Sub 用于提取和传送事件的消息传递服务。 Eventarc 构建一个可连接任何服务的事件驱动型架构。 管理工具 Cloud Shell 带有内置命令行的交互式 Shell 环境。 Cloud 控制台 基于 Web 的界面，可用于管理和监控云应用。 Cloud Endpoints Google Cloud 上的 API 部署和开发管理服务。 Cloud IAM 适用于 Google Cloud 资源的权限管理系统。 Cloud API Google Cloud 服务的编程接口。 Service Catalog 有助于管理员管理内部企业解决方案的服务目录。 费用管理 用于监测、控制和优化费用的工具。 可观测性 监控、日志记录和应用性能套件。 碳足迹 用于查看和导出 Google Cloud 碳排放量报告的信息中心。 Config Connector 用于管理 Google Cloud 资源的 Kubernetes 插件。

### 段落 20

Active Assist 用于轻松管理性能、安全性和费用的工具。 没有看到您需要的内容？ 查看所有管理工具 地图和地理空间 Earth Engine 提供地球观测数据和分析的地理空间平台。 Google Maps Platform 打造基于地理位置的沉浸式体验，并改进业务运营。 媒体服务 Cloud CDN 用于提供 Web 内容和视频内容的内容分发网络。 Live Stream API 这项服务可用来转换实时视频和软件包以进行流式传输。 OpenCue 专为视效和动画行业设计的开源渲染管理器。 Transcoder API 转换并打包视频文件，以优化视频传输。 Video Stitcher API 用于动态广告插播或服务器端广告插播的服务。 迁移 迁移中心 用于通过 Google Cloud 进行迁移和现代化改造的统一平台。 应用迁移 用于将应用迁移到云端，以实现低费用更新周期。 Migrate to Virtual Machines 用于将虚拟机和物理服务器迁移到 Compute Engine 的各种组件。 Cloud Foundation Toolkit 适用于 Deployment Manager 和 Terraform 的参考模板。 Database Migration Service 使用无服务器技术以最短停机时间迁移到 Cloud SQL。 Migrate to Containers 用于将虚拟机迁移到 GKE 上的系统容器的各种组件。

### 段落 21

数据分析迁移服务 简化的数据仓库和数据湖迁移工具及激励措施。 快速迁移和现代化改造计划 用于简化云迁移路径的端到端迁移计划。 Transfer Appliance 用于将大量数据迁移到 Google Cloud 的存储服务器。 Storage Transfer Service 用于将数据从在线和本地来源转移到 Cloud Storage 的服务。 VMware Engine 将您的 VMware 工作负载迁移到 Google Cloud 并继续以原生方式运行。 网络 Cloud Armor 针对 Web 攻击和 DDoS 攻击的安全政策和防御机制。 Cloud CDN 和媒体 CDN 用于提供 Web 内容和视频内容的内容分发网络。 Cloud DNS 提供可靠、低延迟的域名查询服务的域名系统。 Cloud Load Balancing 跨应用和区域分配流量的服务。 Cloud NAT 用于向私有实例授予互联网访问权限的 NAT 服务。 云连接 适合 VPN、对等互连和企业需求的连接方案。 Network Connectivity Center 可帮助简化和扩缩网络的连接管理解决方案。 Network Intelligence Center 网络监控、验证和优化平台。 Network Service Tiers 基于性能、可用性和费用的 Cloud 网络方案。 虚拟私有云 整个组织使用一个 VPC，在项目中进行隔离。

### 段落 22

Private Service Connect 保护 VPC 与各服务之间的连接。 没有看到您需要的内容？ 查看所有网络产品 运维 Cloud Logging 管理 Google Cloud 审核日志、平台日志和应用日志。 Cloud Monitoring 通过丰富的指标帮助您了解基础架构和应用的运行状况。 错误报告 识别和分析应用错误。 Managed Service for Prometheus Google Cloud 上的全托管式 Prometheus。 Cloud Trace 用于从应用中收集延迟数据的跟踪系统。 Cloud Profiler 用于分析应用性能的 CPU 和堆性能分析器。 Cloud 配额 管理所有 Google Cloud 服务的配额。 工作效率与协作 AppSheet 用于构建和扩展应用的无代码开发平台。 AppSheet Automation 在统一平台上构建自动化和应用。 Gemini Enterprise 应用 一个安全可靠的平台，可助力员工轻松探索、创建、运行和管理 AI 智能体。 Google Workspace 面向个人和组织的协作和办公工具。 Google Workspace 基本功能版 为团队提供安全的视频会议功能和现代化协作功能。 Cloud Identity IT 管理员用于管理用户设备和应用的统一平台。 Chrome 企业版 专为企业打造的 ChromeOS、Chrome 浏览器和 Chrome 设备。

### 段落 23

安全和身份 Cloud IAM 适用于 Google Cloud 资源的权限管理系统。 敏感数据保护 帮助您发现、分类和保护宝贵的数据资产。 Mandiant Managed Defense 自信满满地全天候查找和消除威胁。 Security Command Center 用于保护 Google Cloud 资产免遭安全威胁的平台。 Cloud Key Management 在 Google Cloud 上管理加密密钥。 Mandiant Incident Response 尽可能减少安全事故的影响。 Chrome 企业进阶版 借助广泛的端点可见性，获得安全的企业浏览体验。 Assured Workloads 针对敏感工作负载的合规与安全控制措施。 Google Security Operations 检测、调查和应对网络威胁。 Mandiant Consulting 在突发事件前后及期间获得专家指导。 没有看到您需要的内容？ 查看所有安全和身份产品 无服务器 Cloud Run 用于运行容器化应用的全代管式环境。 Cloud Functions 用于创建云事件响应函数的平台。 App Engine 适用于应用和后端的无服务器应用平台。 Workflows 无服务器产品和 API 服务的工作流编排。 API Gateway 借助全代管式网关开发、部署、保护和管理 API。 存储 Cloud Storage 安全、耐用且可伸缩的对象存储服务。

### 段落 24

块存储 适用于 AI、分析、数据库和企业应用的高性能存储服务。 Filestore 伸缩能力极强且安全可靠的文件存储服务。 Persistent Disk 适用于 Google Cloud 上运行的虚拟机实例的块存储服务。 Cloud Storage for Firebase 用于存储和提供用户生成的内容的对象存储服务。 本地 SSD 本地挂接以满足高性能需求的块存储。 Storage Transfer Service 用于将数据从在线和本地来源转移到 Cloud Storage 的服务。 Google Cloud Managed Lustre 高性能托管式并行文件服务。 Google Cloud NetApp Volumes 适用于 NFS、SMB 和多协议环境的文件存储服务。 备份和灾难恢复服务 用于实现具有应用一致性的集中式数据保护的服务。 Web3 Blockchain Node Engine 帮助开发者在区块链上进行开发的全代管式节点托管解决方案。 区块链 RPC 帮助在区块链上进行构建的企业级远程过程调用 (RPC)。 close 利用我们透明的定价方法节省资金 Google Cloud 的随用随付价格方案会根据预付费资源的每月用量和折扣费率自动为您节省费用。请立即联系我们，获取报价。 请求报价 价格概览和工具 Google Cloud 价格 用多少付多少，没有限制 价格计算器 计算您可节省的云服务费用。

### 段落 25

Google Cloud 免费层级 探索提供每月免费用量的产品。 费用优化框架 了解优化工作负载费用的最佳实践。 费用管理工具 用于监控和控制费用的工具。 产品详细价格 Compute Engine Cloud SQL Google Kubernetes Engine Cloud Storage BigQuery 查看 100 多种产品的完整价格表 close 学习与构建 Google Cloud 免费计划 获享 $300 赠金以及 20 多种提供“始终免费”用量的产品。 快速入门 获取教程和演示。 博客 阅读我们最新的产品资讯和案例。 学习中心 通过基于角色的学习发展您的职业生涯 认证 准备并注册认证。 云架构中心 了解参考架构和最佳实践。 连接 创新者 加入 Google Cloud 合作伙伴计划。 开发者中心 及时获得最新资讯并保持联系。 活动和在线讲座 浏览即将到来的活动和点播观看活动。 Google Cloud 社区 提出问题、寻找答案并与他人交流。 咨询与合作伙伴 Google Cloud 咨询服务 与我们的专家合作处理云项目。 Google Cloud Marketplace 只需点击几下即可部署即时可用的解决方案。 Google Cloud 合作伙伴 探索与合作伙伴合作的好处。 成为合作伙伴 加入 Partner Advantage 计划。

### 段落 26

close 概览 arrow_forward 解决方案 arrow_forward 产品 arrow_forward 价格 arrow_forward 资源 arrow_forward 文档 支持 控制台 加快数字化转型的速度 了解详情 主要优势 为什么选择 Google Cloud AI 与智能体 多云 全球基础架构 数据云 现代基础设施云 安全 工作效率与协作 报告和数据洞见 高管数据洞见 分析师报告 白皮书 客户案例 行业解决方案 零售 快速消费品 金融服务 医疗保健和生命科学 媒体和娱乐 电信 游戏 制造 供应链与物流 政府 教育 查看所有行业解决方案 查看所有解决方案 应用现代化改造 CAMP 对传统应用进行现代化改造 从 PaaS 迁移：Cloud Foundry 或 Openshift 从大型主机迁移 对软件交付进行现代化改造 DevOps 最佳实践 SRE 原则 平台工程设计 设计适合多云环境的架构 人工智能 Gemini Enterprise for Customer Experience Gemini Enterprise AI Commerce Search 内置 Gemini 的 Google Cloud 物理 AI API 和应用 使用 API 开拓新的业务渠道 使用 API 发掘旧式应用的潜力 Open Banking APIx 数据分析 数据迁移 数据湖仓一体 实时分析 营销分析 数据集 商业智能 数据分析智能体 地理空间分析 数据科学 数据库 数据

### 段落 27

库迁移 数据库现代化改造 游戏数据库 Google Cloud 数据库 将 Oracle 工作负载迁移到 Google Cloud 开源数据库 SQL Server on Google Cloud 用于数据库的 Gemini 基础架构 应用迁移 SAP on Google Cloud 高性能计算 Windows on Google Cloud 数据中心迁移 Active Assist 虚拟桌面 快速迁移和现代化改造计划 备份和灾难恢复 Red Hat on Google Cloud 跨云网络 工作效率与协作 Google Workspace Google Workspace 基本功能版 Cloud Identity Chrome 企业版 安全 智能体 SOC Web 应用和 API 保护 安全和弹性框架 风险和合规即代码 (RCaC) 软件供应链安全 Security Foundation 初创公司和中小型企业 初创公司计划 中小型企业 软件即服务 精选产品 Gemini Enterprise 应用 Agent Platform Compute Engine Cloud Storage BigQuery Cloud Run Google Kubernetes Engine Looker Apigee API Management Cloud SQL Cloud CDN 查看所有产品（100 多款） AI 和机器学习 Gemini Enterprise Agent Platform

### 段落 28

**EN**

Gemini Enterprise 应用 Gemini Enterprise for Customer Experience Model Garden Customer Experience Agent Studio 智能体搜索 Speech-to-Text Text-to-Speech Translation AI Vision AI 联络中心即服务 查看所有 AI 和机器学习产品 商业智能 Looker 数据洞察 计算 Compute Engine App Engine Cloud GPU Migrate to Virtual Machines Spot 虚拟机 批量 单租户节点 裸金属 Recommender VMware Engine Cloud Run 查看所有计算产品 容器 Google Kubernetes Engine Cloud Run Cloud Build Artifact Registry Cloud Code Cloud Deploy Migrate to Containers Deep Learning Containers Knative 数据分析 BigQuery Managed Service for Apache Spark Dataflow Looker 湖仓一体 Pub/Sub Managed Service for Apache Airflow Knowledge Catalog 数据分析智能体 数据分析迁移服务 Managed Ser

**中文**

Gemini Enterprise 应用 Gemini Enterprise for Customer Experience Model Garden Customer Experience Agent Studio 智能体搜索 Speech-to-Text Text-to-Speech Translation AI Vision AI 联络中心即服务 查看所有 AI 和机器学习产品 商业智能 Looker 数据洞察计算 Compute Engine App Engine Cloud GPU 迁移到虚拟机 Spot 虚拟机 批量物流节点 裸金属推荐器 VMware Engine Cloud Run 查看所有计算产品容器 Google Kubernetes Engine Cloud Run Cloud Build Artifact Register Cloud Code Cloud Deploy迁移到容器 深度学习容器 Knative 数据分析 BigQuery Apache Spark 托管服务 Dataflow Looker 湖仓一体 Pub/Sub Apache Airflow 托管服务 知识目录 数据分析智能体 数据分析迁移服务 托管服务

### 段落 29

**EN**

vice for Apache Kafka 查看所有数据分析产品 数据库 AlloyDB for PostgreSQL Cloud SQL Firestore Spanner Bigtable Datastream Database Migration Service 裸金属解决方案 Memorystore 开发者工具 Artifact Registry Cloud Code Cloud Build Cloud Deploy Cloud Deployment Manager Cloud SDK Cloud Scheduler Cloud Source Repositories Infrastructure Manager Cloud Workstations Gemini Code Assist 查看所有开发者工具 分布式云 Google Distributed Cloud Connected Google Distributed Cloud Air-gapped 混合云和多云 Google Kubernetes Engine Apigee API Management Migrate to Containers Cloud Build 可观测性 Cloud Service Mesh Google Distributed Cloud 针对特定行业 反洗钱 AI Cloud Healthcare API 关联 Fitbit 设备 电信网络自动化 电信数据编织 Telecom Sub

**中文**

Vice for Apache Kafka 查看所有数据分析产品 数据库 AlloyDB for PostgreSQL Cloud SQL Firestore Spanner Bigtable Datastream 数据库迁移服务 Memorystore 开发者工具 Artifact Registry 云代码 云构建 云部署 云部署管理器 云 SDK 云调度程序 云源存储库 基础设施管理器 云工作站 Gemini 代码辅助 查看所有开发者工具 混合云 Google 分布式云连接 Google 分布式云 气隙混合云和多云 Google Kubernetes Engine Apigee API 管理 迁移到容器云 构建可落地性 云服务网格 Google 分布式云 特定目标行业 反洗钱 AI Cloud Healthcare API 关联 Fitbit 设备 电信网络自动化 电信数据创业 电信子系统

### 段落 30

**EN**

scriber Insights Spectrum Access System (SAS) 集成服务 Application Integration Workflows Apigee API Management Cloud Tasks Cloud Scheduler Managed Service for Apache Spark Cloud Data Fusion Managed Service for Apache Airflow Pub/Sub Eventarc 管理工具 Cloud Shell Cloud 控制台 Cloud Endpoints Cloud IAM Cloud API Service Catalog 费用管理 可观测性 碳足迹 Config Connector Active Assist 查看所有管理工具 地图和地理空间 Earth Engine Google Maps Platform 媒体服务 Cloud CDN Live Stream API OpenCue Transcoder API Video Stitcher API 迁移 迁移中心 应用迁移 Migrate to Virtual Machines Cloud Foundation Toolkit Database Migration Service Migrate to Containers 数据分析迁移服务 快速迁移和现代化改造计划 Transfer Appliance Storage

**中文**

scriber Insights 频谱访问系统 (SAS) 集成服务 应用程序集成 工作流程 Apigee API 管理 云任务 Cloud Scheduler Apache Spark 托管服务 Cloud Data Fusion Apache Airflow Pub/Sub 托管服务 Eventarc 管理工具 Cloud Shell Cloud 控制台 云端点 Cloud IAM Cloud API 服务目录 费用管理 可安装性 碳足迹配置连接器 Active Assist 查看所有管理工具 地图和GEO空间 Earth Engine Google Maps Platform 媒体服务 Cloud CDN Live Stream API OpenCue Transcoder API Video Stitcher API 迁移 迁移中心应用迁移 迁移到虚拟机 Cloud Foundation Toolkit 数据库迁移服务 迁移到容器 数据分析迁移服务 快速迁移和现代化改造计划 迁移设备存储

### 段落 31

**EN**

Transfer Service VMware Engine 网络 Cloud Armor Cloud CDN 和媒体 CDN Cloud DNS Cloud Load Balancing Cloud NAT 云连接 Network Connectivity Center Network Intelligence Center Network Service Tiers 虚拟私有云 Private Service Connect 查看所有网络产品 运维 Cloud Logging Cloud Monitoring 错误报告 Managed Service for Prometheus Cloud Trace Cloud Profiler Cloud 配额 工作效率与协作 AppSheet AppSheet Automation Gemini Enterprise 应用 Google Workspace Google Workspace 基本功能版 Cloud Identity Chrome 企业版 安全和身份 Cloud IAM 敏感数据保护 Mandiant Managed Defense Security Command Center Cloud Key Management Mandiant Incident Response Chrome 企业进阶版 Assured Workloads Google Security Operations Mandiant Consult

**中文**

传输服务 VMware Engine 网络云 Armor Cloud CDN 和媒体 CDN Cloud DNS 云负载均衡 Cloud NAT 云连接 网络连接中心 网络智能中心 网络服务层 虚拟主机云 Private Service Connect 查看所有网络产品 运维 云日志 云监控 错误报告 Prometheus 托管服务 Cloud Trace Cloud Profiler Cloud 轻松工作效率与协作 AppSheet AppSheet Automation Gemini Enterprise 应用 Google Workspace Google Workspace 基本功能版 Cloud Identity Chrome 企业版安全与身份 Cloud IAM敏感数据保护 Mandiant 托管防御 安全指挥中心 云密钥管理 Mandiant 事件响应 Chrome 企业进阶版 保证工作负载 Google 安全运营 Mandiant Consult

### 段落 32

ing 查看所有安全和身份产品 无服务器 Cloud Run Cloud Functions App Engine Workflows API Gateway 存储 Cloud Storage 块存储 Filestore Persistent Disk Cloud Storage for Firebase 本地 SSD Storage Transfer Service Google Cloud Managed Lustre Google Cloud NetApp Volumes 备份和灾难恢复服务 Web3 Blockchain Node Engine 区块链 RPC 利用我们透明的定价方法节省资金 请求报价 价格概览和工具 Google Cloud 价格 价格计算器 Google Cloud 免费层级 费用优化框架 费用管理工具 产品详细价格 Compute Engine Cloud SQL Google Kubernetes Engine Cloud Storage BigQuery 查看 100 多种产品的完整价格表 学习与构建 Google Cloud 免费计划 快速入门 博客 学习中心 认证 云架构中心 连接 创新者 开发者中心 活动和在线讲座 Google Cloud 社区 咨询与合作伙伴 Google Cloud 咨询服务 Google Cloud Marketplace Google Cloud 合作伙伴 成为合作伙伴 为什么选择 Google 选择 Google

### 段落 33

Cloud 信任与安全 现代基础设施云 多云 全球基础架构 位置 客户和案例研究 分析师报告 白皮书 博客 产品和价格 Google Cloud 价格 Google Workspace 价格 查看所有产品 解决方案 基础架构现代化改造 数据库 应用现代化改造 智能分析 人工智能 安全 生产力和工作方式转变 行业解决方案 DevOps 解决方案 小企业解决方案 查看所有解决方案 资源 Google Cloud 联属营销计划 Google Cloud 文档 Google Cloud 快速入门 Google Cloud Marketplace 了解云计算 支持 代码示例 云架构中心 培训 认证 Google Developers Google Cloud 初创公司计划 系统状态 版本说明 互动 联系业务代表 寻找合作伙伴 成为合作伙伴 事件 播客 开发者中心 媒体资讯角 Google Cloud 在 YouTube 上的频道 YouTube 上的 Google Cloud Tech 在 Twitter 上关注 参与用户调查 Google Cloud 诚聘英才，欢迎加入！

### 段落 34

**EN**

Google Cloud 社区 关于 Google 隐私权 网站条款 Google Cloud 术语 Cookie 管理控件 环境行动的第三个十年：加入我们 订阅 Google Cloud 简报 订阅 language ‪简体中文‬ ‪English‬ ‪Deutsch‬ ‪Español‬ ‪Español (Latinoamérica)‬ ‪Français‬ ‪Indonesia‬ ‪Italiano‬ ‪Português (Brasil)‬ ‪简体中文‬ ‪繁體中文‬ ‪日本語‬ ‪한국어‬

**中文**

Google Cloud 社区 关于 Google 隐私权 网站条款 Google Cloud 术语 Cookie 管理控制 环境行动的第三个十年：加入我们订阅 Google Cloud 简报订阅语言 简体中文 English Deutsch Español Español (Latinoamérica) Français Indonesia Italiano Português (Brasil) 简体中文 繁体中文 日本语 한국어
