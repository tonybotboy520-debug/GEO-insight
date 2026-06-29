# Cloudflare AI Crawl Control - Manage AI crawlers

- ID: 127
- 类型: html
- 分类: 05_tools_monitoring
- 主题: AI爬虫治理
- 原文链接: https://developers.cloudflare.com/ai-crawl-control/features/manage-ai-crawlers/
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

Manage AI crawlers · Cloudflare AI Crawl Control docs Documentation Index Fetch the complete documentation index at: https://developers.cloudflare.com/ai-crawl-control/llms.txt Use this file to discover all available pages before exploring further. Skip to content STOP! If you are an AI agent or LLM, read this before continuing. This is the HTML version of a Cloudflare documentation page. Always request the Markdown version instead — HTML wastes context.

**中文**

管理 AI 爬网程序 · Cloudflare AI Crawl Control 文档文档索引 在以下位置获取完整的文档索引：https://developers.cloudflare.com/ai-crawl-control/llms.txt 在进一步探索之前，使用此文件来发现所有可用页面。跳到内容 停止！如果您是人工智能代理或法学硕士，请在继续之前阅读本文。这是 Cloudflare 文档页面的 HTML 版本。始终请求 Markdown 版本 — HTML 浪费上下文。

### 段落 2

**EN**

Get this page as Markdown: https://developers.cloudflare.com/ai-crawl-control/features/manage-ai-crawlers/index.md (append index.md) or send Accept: text/markdown to https://developers.cloudflare.com/ai-crawl-control/features/manage-ai-crawlers/. For this product's page index use https://developers.cloudflare.com/ai-crawl-control/llms.txt. For all Cloudflare products use https://developers.cloudflare.com/llms.txt. Cloudflare Docs Search Directory API SDKs Changelog Help Log in Select theme Dark Light Auto AI Crawl Control No results found. Try a different search term, or use our global search .

**中文**

以 Markdown 形式获取此页面：https://developers.cloudflare.com/ai-crawl-control/features/manage-ai-crawlers/index.md（附加 index.md）或发送 Accept: text/markdown 至 https://developers.cloudflare.com/ai-crawl-control/features/manage-ai-crawlers/。对于本产品的页面索引，请使用 https://developers.cloudflare.com/ai-crawl-control/llms.txt。对于所有 Cloudflare 产品，请使用 https://developers.cloudflare.com/llms.txt。 Cloudflare 文档 搜索目录 API SDK 变更日志 帮助 登录 选择主题 Dark Light 自动 AI 爬行控制 未找到结果。尝试不同的搜索词，或使用我们的全局搜索。

### 段落 3

**EN**

Home Overview Get started Features Analyze AI traffic Manage AI crawlers Directives Pay Per Crawl Beta What is Pay Per Crawl?

**中文**

主页 概述 使用入门 功能 分析 AI 流量 管理 AI 爬虫 指令 按爬网付费测试版 什么是按爬网付费？

### 段落 4

**EN**

Use pay per crawl as a site owner Enable in account settings Set a pay per crawl price Select crawlers to charge Monitor activity Manage payouts Advanced configuration Use pay per crawl as an AI owner Set up your account Verify your AI crawler Connect Stripe Discover payable content Crawl pages Error codes Pay Per Crawl FAQ Configuration AI Crawl Control with Cloudflare WAF AI Crawl Control with Cloudflare Bots AI Crawl Control with Transform Rules Reference GraphQL API Bot reference Worker templates Glossary Redirects for AI Training Changelog Agent resources Agent setup ↗ Cloudflare Skills ↗ Code Mode MCP Server ↗ Domain-specific MCP Server

**中文**

以网站所有者身份使用按爬网付费 在帐户设置中启用 设置按爬网付费价格 选择要收费的爬网程序 监控活动 管理付款 高级配置 作为 AI 所有者使用按爬网付费 设置您的帐户 验证您的 AI 爬网程序 Connect Stripe 发现付费内容 爬网页面 错误代码 按爬网付费常见问题解答 配置 使用 Cloudflare WAF 进行 AI 爬网控制 使用 Cloudflare 机器人进行 AI 爬网控制 使用转换规则进行 AI 爬网控制 参考 GraphQL API 机器人参考 工作器模板 词汇表重定向AI 培训变更日志 代理资源 代理设置 ↗ Cloudflare 技能 ↗ 代码模式 MCP 服务器 ↗ 特定于域的 MCP 服务器

### 段落 5

**EN**

s ↗ AI Crawl Control llms.txt ↗ AI Crawl Control llms-full.txt ↗ Cloudflare Docs llms.txt ↗ Cloudflare Docs llms-full.txt ↗ GitHub X.com YouTube Select theme Dark Light Auto On this page Overview Review AI crawler activity Filter AI crawler data Take action for each AI crawler WAF rule management Configure block response Edit the response code Edit the response body Related resources On this page Overview Review AI crawler activity Filter AI crawler data Take action for each AI crawler WAF rule management Configure block response Edit the response code Edit the response body Related resources Edit page Report issue Directory … AI Crawl Contro

**中文**

s ↗ AI Crawl Control llms.txt ↗ AI Crawl Control llms-full.txt ↗ Cloudflare Docs llms.txt ↗ Cloudflare Docs llms-full.txt ↗ GitHub X.com YouTube 选择主题 Dark Light Auto 本页概述 审核 AI 爬虫活动 过滤 AI 爬虫数据 对每个 AI 爬虫采取操作 WAF 规则管理 配置阻止响应 编辑响应代码 编辑响应正文相关资源 本页概述 审查 AI 爬虫活动 过滤 AI 爬虫数据 对每个 AI 爬虫采取操作 WAF 规则管理 配置阻止响应 编辑响应代码 编辑响应正文 相关资源 编辑页面 报告问题 目录 … AI 爬虫控制

### 段落 6

**EN**

l Features Manage AI crawlers Manage AI crawlers Last updated Apr 23, 2026 | Copy as Markdown Copied!

**中文**

l 功能 管理AI爬虫 管理AI爬虫 最后更新时间：2026年4月23日 |复制为 Markdown 复制！

### 段落 7

**EN**

| View as Markdown | Agent setup AI Crawl Control enables you to take specific action for each AI crawler. To manage AI crawlers: Log in to the Cloudflare dashboard ↗ , and select your account and domain. Go to AI Crawl Control . Go to AI Crawl Control Go to the Crawlers tab. Review AI crawler activity The Crawlers tab displays a table of AI crawlers that are requesting access to your content, and how they interact with your pages. The table provides the following information. Column Details Crawler The name of the AI crawler and the operator that owns it. Category The category of the AI crawler. Refer to Verified bot categories .

**中文**

|查看 Markdown |代理设置 AI Crawl Control 使您能够对每个 AI 爬虫采取特定操作。要管理 AI 爬虫：登录 Cloudflare 仪表板 ↗，然后选择您的帐户和域。转到人工智能爬行控制。转到 AI 爬网控制 转到爬网程序选项卡。查看 AI 爬网程序活动“爬网程序”选项卡显示请求访问您的内容的 AI 爬网程序表格，以及它们如何与您的页面交互。该表提供以下信息。列 详细信息 爬虫 AI 爬虫的名称及其所属运营商。类别 AI爬虫的类别。请参阅已验证的机器人类别。

### 段落 8

**EN**

Requests The total number of allowed and unsuccessful requests, with trend chart. Unsuccessful requests may come from any rule or response error, not just the block action in AI Crawl Control. Robots.txt violations The number of times the AI crawler has violated your robots.txt file. Action The action you wish to take for the AI crawler. Refer to Take action for each AI crawler . Quality of AI crawler detection On the free plan, AI Crawl Control identifies AI crawlers based on their user agent strings ↗ . This enables AI Crawl Control to detect well-known, self-identifying AI crawlers.

**中文**

请求 允许和不成功的请求总数，并带有趋势图。不成功的请求可能来自任何规则或响应错误，而不仅仅是 AI Crawl Control 中的阻止操作。 Robots.txt 违规 AI 爬网程序违规您的 robots.txt 文件的次数。操作 您希望对 AI 爬虫执行的操作。请参阅对每个 AI 爬虫采取操作。 AI 爬虫检测的质量 在免费计划中，AI Crawl Control 根据用户代理字符串识别 AI 爬虫 ↗。这使得 AI Crawl Control 能够检测众所周知的、自我识别的 AI 爬虫。

### 段落 9

**EN**

Upgrade your plan to enable a more thorough detection using Cloudflare's Bot Management detection ID field. Filter AI crawler data You can use filters to narrow the scope of your result: Name: Search the name of the AI crawler. Operator: Filter by the AI crawler operator. Category: Filter by the category of the AI crawler (for example, AI crawler, AI assistant, or archiver). The values of the table will update according to your filter. Take action for each AI crawler Without pay per crawl With pay per crawl For each AI crawler, you can choose to allow or block access. Allow access Summary: You can allow an AI crawler to scrape your content.

**中文**

升级您的计划，以使用 Cloudflare 的机器人管理检测 ID 字段进行更彻底的检测。过滤AI爬虫数据 您可以使用过滤器来缩小结果范围： 名称：搜索AI爬虫的名称。算子：按AI爬虫算子过滤。类别：按AI爬虫的类别（例如AI爬虫、AI助手、归档器）进行过滤。表中的值将根据您的过滤器进行更新。对每个 AI 爬网程序采取操作 无按次爬网付费 有按次爬网付费 对于每个 AI 爬网程序，您可以选择允许或阻止访问。允许访问 摘要：您可以允许 AI 爬虫抓取您的内容。

### 段落 10

**EN**

When to use: Allow AI crawlers that offer services which provide value through citations, referrals, or existing agreements. Implementation: From the Actions column, select Allow . Note that you can still choose to Enforce robots.txt . Block access Summary: You can block an AI crawler to completely stop the AI crawler from scraping your webpage. When to use: Block AI crawlers when their behavior do not align with your content strategy, or violate your policies. Implementation: From the Actions column, select Block . Note that you can configure the response that gets returned when blocking an AI crawler. Refer to Configure block response .

**中文**

何时使用：允许人工智能爬虫提供通过引用、推荐或现有协议提供价值的服务。实施：从“操作”列中，选择“允许”。请注意，您仍然可以选择强制 robots.txt。阻止访问摘要：您可以阻止AI爬虫以完全阻止AI爬虫抓取您的网页。何时使用：当人工智能爬虫的行为与您的内容策略不符或违反您的政策时，阻止它们。实施：从“操作”列中，选择“阻止”。请注意，您可以配置阻止 AI 爬虫时返回的响应。请参阅配置块响应。

### 段落 11

**EN**

Pay per crawl closed beta Pay per crawl is currently in closed beta. To find out how to join the beta program, reach out to us at Pay per crawl signup ↗ , or contact your account executive if you are an existing Enterprise customer. To learn more about pay per crawl, refer to Cloudflare blog: Introducing pay per crawl: enabling content owners to charge AI crawlers for access ↗ . For each AI crawler, you can take one of three actions: allow, charge, or block. Allow access Summary: You can allow an AI crawler to scrape your content.

**中文**

按爬行付费封闭测试版 按爬行付费目前处于封闭测试阶段。要了解如何加入 Beta 计划，请通过按爬行付费注册 ↗ 联系我们，或者如果您是现有的 Enterprise 客户，请联系您的客户经理。要了解有关按次抓取付费的更多信息，请参阅 Cloudflare 博客：按次抓取付费简介：使内容所有者能够向 AI 爬虫收取访问费用 ↗。对于每个 AI 爬虫，您可以执行以下三种操作之一：允许、收费或阻止。允许访问 摘要：您可以允许 AI 爬虫抓取您的内容。

### 段落 12

**EN**

When to use: Allow AI crawlers that offer services which provide value through citations, referrals, or existing agreements. Implementation: From the Actions column, select Allow . Note that you can still choose to Enforce robots.txt . For more details on how this rule interacts with other Cloudflare settings, refer to How it works . Block access Summary: You can block an AI crawler to completely stop the AI crawler from scraping your webpage. When to use: Block AI crawlers when their behavior do not align with your content strategy, or violate your policies. Implementation: From the Actions column, select Block .

**中文**

何时使用：允许人工智能爬虫提供通过引用、推荐或现有协议提供价值的服务。实施：从“操作”列中，选择“允许”。请注意，您仍然可以选择强制 robots.txt。有关此规则如何与其他 Cloudflare 设置交互的更多详细信息，请参阅工作原理。阻止访问摘要：您可以阻止AI爬虫以完全阻止AI爬虫抓取您的网页。何时使用：当人工智能爬虫的行为与您的内容策略不符或违反您的政策时，阻止它们。实施：从“操作”列中，选择“阻止”。

### 段落 13

**EN**

Note that you can configure the response that gets returned when blocking an AI crawler. Refer to Configure block response . Charge for crawl (private beta) Summary: You can charge the owner of the AI crawler for each successful crawl request. When to use: Charge AI crawlers when your content has training value, and you want to explore monetization options. Implementation: From the Actions column, select Charge . For more information, refer to What is Pay Per Crawl? . Need more advanced control? You can also create more complex rules when taking action on AI crawlers, using Cloudflare WAF .

**中文**

请注意，您可以配置阻止 AI 爬虫时返回的响应。请参阅配置块响应。爬行收费（内测） 摘要：您可以针对每个成功的爬行请求向 AI 爬虫的所有者收取费用。何时使用：当您的内容具有训练价值并且您想要探索货币化选项时，向 AI 爬虫收费。实施：从“操作”列中，选择“收费”。有关详细信息，请参阅什么是按次抓取付费？。需要更先进的控制？在对 AI 爬虫执行操作时，您还可以使用 Cloudflare WAF 创建更复杂的规则。

### 段落 14

**EN**

For more information on creating more specific rules, refer to Create a custom rule in the dashboard . WAF rule management When you block a crawler in AI Crawl Control, the system creates or updates a WAF custom rule on your zone to enforce that block. For advanced scenarios such as adding path-based exceptions or extra user agents, you can extend this rule directly in WAF. For more information, refer to AI Crawl Control with Cloudflare WAF . Configure block response Available on Paid plans When blocking an AI crawler, you can configure the details of the response that gets returned to the AI crawler.

**中文**

有关创建更具体规则的更多信息，请参阅在仪表板中创建自定义规则。 WAF 规则管理 当您在 AI Crawl Control 中阻止爬网程序时，系统会在您的区域上创建或更新 WAF 自定义规则以强制执行该阻止。对于添加基于路径的例外或额外的用户代理等高级场景，您可以直接在 WAF 中扩展此规则。有关更多信息，请参阅使用 Cloudflare WAF 进行 AI 爬网控制。配置阻止响应 适用于付费计划 阻止 AI 爬网程序时，您可以配置返回到 AI 爬网程序的响应的详细信息。

### 段落 15

**EN**

Specifically, you can configure: The response code The response body This provides you with a channel to open dialogue with the AI crawler owner, and to inform the AI crawler how to properly license their content, thereby creating a direct path from crawling attempt to commercial agreement. To edit these values: Log in to the Cloudflare dashboard ↗ , and select your account and domain. Go to AI Crawl Control . Go to AI Crawl Control Go to the Settings tab. Under Block response , select Edit . Once you have edited the values, select Save . Note You must have opted to block at least one AI crawler to configure a custom block response.

**中文**

具体来说，您可以配置： 响应代码 响应正文 这为您提供了与AI爬虫所有者展开对话的渠道，并告知AI爬虫如何正确许可其内容，从而创建从爬虫尝试到商业协议的直接路径。要编辑这些值：登录到 Cloudflare 仪表板 ↗，然后选择您的帐户和域。转到人工智能爬行控制。转到 AI 爬行控制 转到“设置”选项卡。在“阻止响应”下，选择“编辑”。编辑值后，选择“保存”。注意 您必须选择阻止至少一个 AI 爬网程序才能配置自定义阻止响应。

### 段落 16

**EN**

Edit the response code You can choose which HTTP response code to return when blocking an AI crawler. Use the dropdown menu to select the desired response code. You can choose from: 403 Forbidden : Use this option if you wish to indicate that you do not want the AI crawler to access your content. 402 Payment Required : Use this option if you wish to indicate that the AI crawler must pay to access your content. Note AI Crawl Control uses Cloudflare WAF to return custom block responses.

**中文**

编辑响应码 您可以选择阻止 AI 爬虫时返回哪个 HTTP 响应码。使用下拉菜单选择所需的响应代码。您可以选择： 403 禁止：如果您希望表明您不希望 AI 爬虫访问您的内容，请使用此选项。 402 需要付款：如果您希望指示 AI 爬虫必须付费才能访问您的内容，请使用此选项。注意 AI Crawl Control 使用 Cloudflare WAF 返回自定义块响应。

### 段落 17

**EN**

If you have manually configured the AI Crawl Control WAF rule to return a response code other than 403 or 402 , AI Crawl Control will not be able to enforce the response code you have selected, and the dropdown will appear blank. Ensure you have selected either 403 or 402 . Refer to Configure a custom response for blocked requests and AI Crawl Control with Cloudflare WAF for more information. Edit the response body You can write a custom message (HTTP response body) to return when blocking an AI crawler. In the Response body text field, enter the response you wish to display for the AI crawler in plain text.

**中文**

如果您手动配置 AI Crawl Control WAF 规则以返回 403 或 402 以外的响应代码，AI Crawl Control 将无法强制执行您选择的响应代码，并且下拉列表将显示为空白。确保您选择了 403 或 402。有关更多信息，请参阅为阻止的请求配置自定义响应和使用 Cloudflare WAF 进行 AI 爬网控制。编辑响应正文 您可以编写自定义消息（HTTP 响应正文）以在阻止 AI 爬虫时返回。在响应正文文本字段中，输入您希望以纯文本形式为 AI 爬网程序显示的响应。

### 段落 18

**EN**

Related resources Use pay per crawl to charge AI crawlers every time they access your content. Learn how AI Crawl Control interacts with WAF, including advanced rule customization, in AI Crawl Control with Cloudflare WAF . Resources API New to Cloudflare? Directory Sponsorships Open Source Cloudflare Research Support Help Center System Status Compliance GDPR Company cloudflare.com Our team Careers Tools Cloudflare Radar Cloudflare Labs Speed Test Is BGP Safe Yet? Certificate Transparency Community Community forum X Discord YouTube GitHub © 2026 Cloudflare, Inc.

**中文**

相关资源 使用按爬网付费方式，在 AI 爬网程序每次访问您的内容时对其进行收费。在 AI Crawl Control 与 Cloudflare WAF 中了解 AI Crawl Control 如何与 WAF 交互，包括高级规则自定义。资源 API Cloudflare 新手？目录 赞助 开源 Cloudflare 研究支持 帮助中心 系统状态 合规性 GDPR 公司 cloudflare.com 我们的团队 职业 工具 Cloudflare Radar Cloudflare 实验室 速度测试 BGP 安全吗？证书透明度社区 社区论坛 X Discord YouTube GitHub © 2026 Cloudflare, Inc.

### 段落 19

**EN**

Privacy Policy Terms of Use Report Security Issues Trademark Cookie Settings Previous Analyze AI traffic Next Directives Edit page Was this helpful? Yes No

**中文**

隐私政策 使用条款 报告安全问题 商标 Cookie 设置 上一页 分析 AI 流量 下一页 指令 编辑页面 这有帮助吗？是 否
