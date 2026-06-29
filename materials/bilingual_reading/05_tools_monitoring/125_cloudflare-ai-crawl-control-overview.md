# Cloudflare AI Crawl Control - Overview

- ID: 125
- 类型: html
- 分类: 05_tools_monitoring
- 主题: AI爬虫治理
- 原文链接: https://developers.cloudflare.com/ai-crawl-control/
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

Overview · Cloudflare AI Crawl Control docs Documentation Index Fetch the complete documentation index at: https://developers.cloudflare.com/ai-crawl-control/llms.txt Use this file to discover all available pages before exploring further. Skip to content STOP! If you are an AI agent or LLM, read this before continuing. This is the HTML version of a Cloudflare documentation page. Always request the Markdown version instead — HTML wastes context. Get this page as Markdown: https://developers.cloudflare.com/ai-crawl-control/index.md (append index.md) or send Accept: text/markdown to https://developers.cloudflare.com/ai-crawl-control/.

**中文**

概述 · Cloudflare AI Crawl Control 文档 文档索引 在以下位置获取完整的文档索引：https://developers.cloudflare.com/ai-crawl-control/llms.txt 在进一步探索之前，使用此文件来发现所有可用页面。跳到内容 停止！如果您是人工智能代理或法学硕士，请在继续之前阅读本文。这是 Cloudflare 文档页面的 HTML 版本。始终请求 Markdown 版本 — HTML 浪费上下文。以 Markdown 形式获取此页面：https://developers.cloudflare.com/ai-crawl-control/index.md（附加 index.md）或发送 Accept: text/markdown 至 https://developers.cloudflare.com/ai-crawl-control/。

### 段落 2

**EN**

For this product's page index use https://developers.cloudflare.com/ai-crawl-control/llms.txt. For all Cloudflare products use https://developers.cloudflare.com/llms.txt. Cloudflare Docs Search Directory API SDKs Changelog Help Log in Select theme Dark Light Auto AI Crawl Control No results found. Try a different search term, or use our global search . Home Overview Get started Features Analyze AI traffic Manage AI crawlers Directives Pay Per Crawl Beta What is Pay Per Crawl?

**中文**

对于本产品的页面索引，请使用 https://developers.cloudflare.com/ai-crawl-control/llms.txt。对于所有 Cloudflare 产品，请使用 https://developers.cloudflare.com/llms.txt。 Cloudflare 文档 搜索目录 API SDK 变更日志 帮助 登录 选择主题 Dark Light 自动 AI 爬行控制 未找到结果。尝试不同的搜索词，或使用我们的全局搜索。主页 概述 使用入门 功能 分析 AI 流量 管理 AI 爬虫 指令 按爬网付费测试版 什么是按爬网付费？

### 段落 3

**EN**

Use pay per crawl as a site owner Enable in account settings Set a pay per crawl price Select crawlers to charge Monitor activity Manage payouts Advanced configuration Use pay per crawl as an AI owner Set up your account Verify your AI crawler Connect Stripe Discover payable content Crawl pages Error codes Pay Per Crawl FAQ Configuration AI Crawl Control with Cloudflare WAF AI Crawl Control with Cloudflare Bots AI Crawl Control with Transform Rules Reference GraphQL API Bot reference Worker templates Glossary Redirects for AI Training Changelog Agent resources Agent setup ↗ Cloudflare Skills ↗ Code Mode MCP Server ↗ Domain-specific MCP Server

**中文**

以网站所有者身份使用按爬网付费 在帐户设置中启用 设置按爬网付费价格 选择要收费的爬网程序 监控活动 管理付款 高级配置 作为 AI 所有者使用按爬网付费 设置您的帐户 验证您的 AI 爬网程序 Connect Stripe 发现付费内容 爬网页面 错误代码 按爬网付费常见问题解答 配置 使用 Cloudflare WAF 进行 AI 爬网控制 使用 Cloudflare 机器人进行 AI 爬网控制 使用转换规则进行 AI 爬网控制 参考 GraphQL API 机器人参考 工作器模板 词汇表重定向AI 培训变更日志 代理资源 代理设置 ↗ Cloudflare 技能 ↗ 代码模式 MCP 服务器 ↗ 特定于域的 MCP 服务器

### 段落 4

**EN**

s ↗ AI Crawl Control llms.txt ↗ AI Crawl Control llms-full.txt ↗ Cloudflare Docs llms.txt ↗ Cloudflare Docs llms-full.txt ↗ GitHub X.com YouTube Select theme Dark Light Auto On this page Overview Features Use cases Related Products On this page Overview Features Use cases Related Products Edit page Report issue Directory AI Crawl Control AI Crawl Control Last updated Apr 23, 2026 | Copy as Markdown Copied!

**中文**

s ↗ AI Crawl Control llms.txt ↗ AI Crawl Control llms-full.txt ↗ Cloudflare Docs llms.txt ↗ Cloudflare Docs llms-full.txt ↗ GitHub X.com YouTube 选择主题 Dark Light Auto 本页概述 功能 使用案例 相关产品 本页概述 功能 使用案例 相关产品 编辑页面 报告问题 目录 AI Crawl Control AI Crawl Control 最近更新2026 年 4 月 23 日 |复制为 Markdown 复制！

### 段落 5

**EN**

| View as Markdown | Agent setup Available on all plans Monitor and control how AI services access your website content. AI companies use web content to train their models and power AI applications. AI Crawl Control (formerly AI Audit) gives you visibility into which AI services are accessing your content, and provides tools to manage access according to your preferences.

**中文**

|查看 Markdown |代理设置 适用于所有计划 监视和控制 AI 服务如何访问您的网站内容。人工智能公司使用网络内容来训练他们的模型并为人工智能应用程序提供支持。 AI Crawl Control（以前称为 AI Audit）使您可以了解哪些 AI 服务正在访问您的内容，并提供根据您的偏好管理访问的工具。

### 段落 6

**EN**

With AI Crawl Control, you can: See which AI services access your content - Monitor the dashboard to see crawler activity and request patterns Control access with granular policies - Set allow or block rules for individual crawlers Monitor robots.txt compliance - Track which crawlers follow your directives and create enforcement rules Explore monetization options - Set up pay per crawl pricing for content access (private beta) Deploy with zero configuration - Works automatically on all Cloudflare plans Get started Features Manage AI crawlers Control how AI crawlers interact with your domain.

**中文**

借助 AI Crawl Control，您可以： 查看哪些 AI 服务访问您的内容 - 监控仪表板以查看爬网程序活动和请求模式 使用精细策略控制访问 - 为单个爬网程序设置允许或阻止规则 监控 robots.txt 合规性 - 跟踪哪些爬网程序遵循您的指令并创建执行规则 探索盈利选项 - 设置内容访问的每次爬网定价（内测版） 以零配置进行部署 - 在所有 Cloudflare 计划上自动运行 入门 功能 管理 AI 爬网程序 控制 AI 爬网程序如何与您的域交互。

### 段落 7

**EN**

Manage AI crawlers Analyze AI traffic Gain insight into how AI crawlers are interacting with your pages. Analyze AI traffic Track robots.txt Track the health of robots.txt files and identify which crawlers are violating your directives. Track robots.txt Pay Per Crawl Allow AI crawlers to access content by paying per crawl. Pay per crawl Use cases Publishers and content creators Publishers and content creators can monitor which AI crawlers are accessing their articles and educational content. Set policies to allow beneficial crawlers while blocking others.

**中文**

管理 AI 爬虫 分析 AI 流量 深入了解 AI 爬虫如何与您的页面交互。分析 AI 流量 跟踪 robots.txt 跟踪 robots.txt 文件的运行状况并识别哪些爬虫违反了您的指令。跟踪 robots.txt 按次爬行付费 允许 AI 爬虫通过按次爬行付费来访问内容。按爬网付费 使用案例 出版商和内容创建者 出版商和内容创建者可以监控哪些 AI 爬虫正在访问他们的文章和教育内容。设置策略以允许有益的爬虫程序同时阻止其他爬虫程序。

### 段落 8

**EN**

E-commerce and business sites E-commerce and business sites can identify AI crawler activity on product pages and business information. Control access to sensitive data like pricing and inventory. Documentation sites Documentation sites can track how AI crawlers are accessing their technical documentation. Gain insight into how AI crawlers are engaging with your site. Related Products Bots Identify and mitigate automated traffic to protect your domain from bad bots. Web Application Firewall Get automatic protection from vulnerabilities and the flexibility to create custom rules. Analytics View and analyze traffic on your domain.

**中文**

电子商务和商业网站电子商务和商业网站可以识别人工智能爬虫在产品页面和商业信息上的活动。控制对定价和库存等敏感数据的访问。文档站点 文档站点可以跟踪 AI 爬虫如何访问其技术文档。深入了解人工智能爬虫如何与您的网站互动。相关产品 机器人程序 识别并减少自动流量，以保护您的域免受不良机器人程序的侵害。 Web 应用程序防火墙 获得针对漏洞的自动保护以及创建自定义规则的灵活性。分析 查看并分析您域上的流量。

### 段落 9

**EN**

Resources API New to Cloudflare? Directory Sponsorships Open Source Cloudflare Research Support Help Center System Status Compliance GDPR Company cloudflare.com Our team Careers Tools Cloudflare Radar Cloudflare Labs Speed Test Is BGP Safe Yet? Certificate Transparency Community Community forum X Discord YouTube GitHub © 2026 Cloudflare, Inc. Privacy Policy Terms of Use Report Security Issues Trademark Cookie Settings Next Get started Edit page Was this helpful? Yes No

**中文**

资源 API Cloudflare 新手？目录 赞助 开源 Cloudflare 研究支持 帮助中心 系统状态 合规性 GDPR 公司 cloudflare.com 我们的团队 职业 工具 Cloudflare Radar Cloudflare 实验室 速度测试 BGP 安全吗？证书透明度社区 社区论坛 X Discord YouTube GitHub © 2026 Cloudflare, Inc. 隐私政策 使用条款 报告安全问题 商标 Cookie 设置 下一页 开始使用 编辑页面 这有帮助吗？是 否
