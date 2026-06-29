# Cloudflare Blog - Pay per crawl

- ID: 130
- 类型: html
- 分类: 05_tools_monitoring
- 主题: 生态/内容商业化
- 原文链接: https://blog.cloudflare.com/introducing-pay-per-crawl/
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

Introducing pay per crawl: Enabling content owners to charge AI crawlers for access Get Started Free | Contact Sales The Cloudflare Blog Subscribe to receive notifications of new posts: Subscribe AI Developers Radar Product News Security Policy & Legal Zero Trust Speed & Reliability Life at Cloudflare Partners AI Developers Radar Product News Security Policy & Legal Zero Trust Speed & Reliability Life at Cloudflare Partners Introducing pay per crawl: Enabling content owners to charge AI crawlers for access 2025-07-01 Will Allen Simon Newton 5 min read A changing landscape of consumption Many publishers, content creators and website owners currently feel like they have a binary choice — either leave the front door wide open for AI to consume everything they create, or create their own walled garden.

**中文**

引入按爬行付费：使内容所有者能够向 AI 爬行器收取访问费用联系销售人员 Cloudflare 博客 订阅以接收新帖子的通知： 订阅 AI 开发人员雷达产品新闻 安全政策和法律 零信任速度和可靠性 Cloudflare 合作伙伴的生活 AI 开发人员雷达产品新闻 安全政策和法律 零信任速度和可靠性 Cloudflare 合作伙伴的生活 引入按爬行付费：使内容所有者能够向 AI 爬虫的访问收费 2025 年 7 月 1 日 Will Allen Simon Newton 阅读 5 分钟 消费格局的变化 许多出版商、内容创作者网站所有者目前感觉他们有一个二元选择——要么敞开大门让人工智能消费他们创造的一切，要么创建自己的围墙花园。

### 段落 2

**EN**

But what if there was another way? At Cloudflare, we started from a simple principle: we wanted content creators to have control over who accesses their work. If a creator wants to block all AI crawlers from their content, they should be able to do so. If a creator wants to allow some or all AI crawlers full access to their content for free, they should be able to do that, too. Creators should be in the driver’s seat.

**中文**

但如果有其他方法呢？在 Cloudflare，我们从一个简单的原则开始：我们希望内容创建者能够控制谁访问他们的作品。如果创作者想要阻止所有人工智能爬虫访问其内容，他们应该能够做到。如果创作者希望允许部分或所有人工智能爬虫免费完全访问其内容，他们也应该能够做到这一点。创作者应该占据主导地位。

### 段落 3

**EN**

After hundreds of conversations with news organizations, publishers, and large-scale social media platforms, we heard a consistent desire for a third path: They’d like to allow AI crawlers to access their content, but they’d like to get compensated. Currently, that requires knowing the right individual and striking a one-off deal, which is an insurmountable challenge if you don’t have scale and leverage. What if I could charge a crawler? We believe your choice need not be binary — there should be a third, more nuanced option: You can charge for access.

**中文**

在与新闻机构、出版商和大型社交媒体平台进行数百次对话后，我们听到了对第三条道路的一致渴望：他们希望允许人工智能爬虫访问他们的内容，但他们希望获得补偿。目前，这需要了解合适的人选并达成一次性交易，如果您没有规模和影响力，这将是一项难以克服的挑战。如果我可以给爬行器充电怎么办？我们相信您的选择不必是二元的——应该有第三种更微妙的选择：您可以收取访问费用。

### 段落 4

**EN**

Instead of a blanket block or uncompensated open access, we want to empower content owners to monetize their content at Internet scale. We’re excited to help dust off a mostly forgotten piece of the web: HTTP response code 402 . Introducing pay per crawl Pay per crawl , in private beta, is our first experiment in this area. Pay per crawl integrates with existing web infrastructure, leveraging HTTP status codes and established authentication mechanisms to create a framework for paid content access.

**中文**

我们希望让内容所有者能够在互联网规模上将其内容货币化，而不是全面封锁或无偿开放访问。我们很高兴能够帮助清除网络上最容易被遗忘的部分：HTTP 响应代码 402。引入按次爬行付费 私人测试版中的按次爬行付费是我们在该领域的第一个实验。按爬网付费与现有的 Web 基础设施集成，利用 HTTP 状态代码和已建立的身份验证机制来创建付费内容访问的框架。

### 段落 5

**EN**

Each time an AI crawler requests content, they either present payment intent via request headers for successful access ( HTTP response code 200 ), or receive a 402 Payment Required response with pricing. Cloudflare acts as the Merchant of Record for pay per crawl and also provides the underlying technical infrastructure. Publisher controls and pricing Pay per crawl grants domain owners full control over their monetization strategy. They can define a flat, per-request price across their entire site. Publishers will then have three distinct options for a crawler: Allow: Grant the crawler free access to content.

**中文**

每次 AI 爬虫请求内容时，它们要么通过请求标头呈现付款意图以成功访问（ HTTP 响应代码 200 ），要么收到包含定价的 402 Payment Needed 响应。 Cloudflare 充当按爬行付费的记录商家，并提供底层技术基础设施。发布商控制和定价 按抓取付费使域所有者能够完全控制其获利策略。他们可以在整个网站上根据请求定义统一的价格。然后，发布者将为爬网程序提供三个不同的选项： 允许：授予爬网程序对内容的自由访问权限。

### 段落 6

**EN**

Charge: Require payment at the configured, domain-wide price. Block: Deny access entirely, with no option to pay. An important mechanism here is that even if a crawler doesn’t have a billing relationship with Cloudflare, and thus couldn’t be charged for access, a publisher can still choose to ‘charge’ them. This is the functional equivalent of a network level block (an HTTP 403 Forbidden response where no content is returned) — but with the added benefit of telling the crawler there could be a relationship in the future.

**中文**

费用：需要按配置的全域价格付款。阻止：完全拒绝访问，且无法选择付费。这里的一个重要机制是，即使爬虫与 Cloudflare 没有计费关系，因此无法收取访问费用，发布者仍然可以选择向它们“收费”。这在功能上相当于网络级块（不返回任何内容的 HTTP 403 禁止响应），但还有一个额外的好处，即告诉爬虫将来可能存在某种关系。

### 段落 7

**EN**

While publishers currently can define a flat price across their entire site, they retain the flexibility to bypass charges for specific crawlers as needed. This is particularly helpful if you want to allow a certain crawler through for free, or if you want to negotiate and execute a content partnership outside the pay per crawl feature. To ensure integration with each publisher’s existing security posture, Cloudflare enforces Allow or Charge decisions via a rules engine that operates only after existing WAF policies and bot management or bot blocking features have been applied.

**中文**

虽然发布商目前可以在整个网站上定义统一价格，但他们仍然可以根据需要灵活地绕过特定爬虫的费用。如果您想免费允许某个爬网程序通过，或者您想在按爬网付费功能之外协商并执行内容合作伙伴关系，则此功能特别有用。为了确保与每个发布商的现有安全状况集成，Cloudflare 通过规则引擎强制执行允许或收费决策，该规则引擎仅在应用现有 WAF 策略和机器人管理或机器人阻止功能后运行。

### 段落 8

**EN**

Payment headers and access As we were building the system, we knew we had to solve an incredibly important technical challenge: ensuring we could charge a specific crawler, but prevent anyone from spoofing that crawler. Thankfully, there’s a way to do this using Web Bot Auth proposals. For crawlers, this involves: Generating an Ed25519 key pair, and making the JWK -formatted public key available in a hosted directory Registering with Cloudflare to provide the URL of your key directory and user agent information. Configuring your crawler to use HTTP Message Signatures with each request.

**中文**

支付标头和访问 在构建系统时，我们知道必须解决一个极其重要的技术挑战：确保我们可以对特定爬虫进行收费，但防止任何人欺骗该爬虫。值得庆幸的是，有一种方法可以使用 Web Bot Auth 提案来做到这一点。对于爬网程序，这涉及： 生成 Ed25519 密钥对，并使 JWK 格式的公钥在托管目录中可用 向 Cloudflare 注册以提供密钥目录的 URL 和用户代理信息。配置您的爬网程序以对每个请求使用 HTTP 消息签名。

### 段落 9

**EN**

Once registration is accepted, crawler requests should always include signature-agent , signature-input , and signature headers to identify your crawler and discover paid resources.

**中文**

一旦注册被接受，爬虫请求应始终包含签名代理、签名输入和签名标头，以识别您的爬虫并发现付费资源。

### 段落 10

**EN**

GET /example.html Signature-Agent: "https://signature-agent.example.com" Signature-Input: sig2=("@authority" "signature-agent") ;created=1735689600 ;keyid="poqkLGiymh_W0uP6PZFw-dvez3QJT5SolqXBCW38r0U" ;alg="ed25519" ;expires=1735693200 ;nonce="e8N7S2MFd/qrd6T2R3tdfAuuANngKI7LFtKYI/vowzk4lAZYadIX6wW25MwG7DCT9RUKAJ0qVkU0mEeLElW1qg==" ;tag="web-bot-auth" Signature: sig2=:jdq0SqOwHdyHr9+r5jw3iYZH6aNGKijYp/EstF4RQTQdi5N5YYKrD+mCT1HA1nZDsi6nJKuHxUi/5Syp3rLWBA==: Accessing paid content Once a crawler is set up, determination of whether content requires payment can happen via two flows: Reactive (discovery-first) Should a crawler request a paid URL, Cloudflare returns an HTTP 402 Payment Required response, accompanied by a crawler-price header.

**中文**

GET /example.html 签名代理：“https://signature-agent.example.com” 签名输入：sig2=("@authority" "signature-agent") ;created=1735689600 ;keyid="poqkLGiymh_W0uP6PZFw-dvez3QJT5SolqXBCW38r0U" ;alg="ed25519" ;expires=1735693200 ;nonce="e8N7S2MFd/qrd6T2R3tdfAuuANngKI7LFtKYI/vowzk4lAZYadIX6wW25MwG7DCT9RUKAJ0qVkU0mEeLElW1qg==" ;tag="web-bot-auth"签名： sig2=:jdq0SqOwHdyHr9+r5jw3iYZH6aNGKijYp/EstF4RQTQdi5N5YYKrD+mCT1HA1nZDsi6nJKuHxUi/5Syp3rLWBA==：访问付费内容一旦设置了爬虫，可以通过两个流程确定内容是否需要付费： 反应式（发现优先）如果爬网程序请求付费 URL，Cloudflare 将返回 HTTP 402 需要付款响应，并附有爬网程序价格标头。

### 段落 11

**EN**

This signals that payment is required for the requested resource. HTTP 402 Payment Required crawler-price: USD XX.XX The crawler can then decide to retry the request, this time including a crawler-exact-price header to indicate agreement to pay the configured price. GET /example.html crawler-exact-price: USD XX.XX Proactive (intent-first) Alternatively, a crawler can preemptively include a crawler-max-price header in its initial request.

**中文**

这表明所请求的资源需要付费。 HTTP 402 Payment requiredcrawler-price: USD XX.XX 然后，爬网程序可以决定重试请求，这次包括一个crawler-exact-price 标头，以指示同意支付配置的价格。 GET /example.htmlcrawler-exact-price: USD XX.XX 主动（意图优先） 或者，爬网程序可以抢先在其初始请求中包含一个crawler-max-price 标头。

### 段落 12

**EN**

GET /example.html crawler-max-price: USD XX.XX If the price configured for a resource is equal to or below this specified limit, the request proceeds, and the content is served with a successful HTTP 200 OK response, confirming the charge: HTTP 200 OK crawler-charged: USD XX.XX server: cloudflare If the amount in a crawler-max-price request is greater than the content owner’s configured price, only the configured price is charged. However, if the resource’s configured price exceeds the maximum price offered by the crawler, an HTTP 402 Payment Required response is returned, indicating the specified cost.

**中文**

GET /example.htmlcrawler-max-price：USD XX.XX 如果为资源配置的价格等于或低于此指定限制，则请求将继续，并通过成功的 HTTP 200 OK 响应提供内容，确认收费：HTTP 200 OKcrawler-charged：USD XX.XX 服务器：cloudflare 如果crawler-max-price 请求中的金额大于内容所有者的配置价格，则仅按配置的价格收费。但是，如果资源配置的价格超过爬虫提供的最高价格，则会返回 HTTP 402 Payment Needed 响应，指示指定的费用。

### 段落 13

**EN**

Only a single price declaration header, crawler-exact-price or crawler-max-price , may be used per request. The crawler-exact-price or crawler-max-price headers explicitly declare the crawler's willingness to pay. If all checks pass, the content is served, and the crawl event is logged. If any aspect of the request is invalid, the edge returns an HTTP 402 Payment Required response. Financial settlement Crawler operators and content owners must configure pay per crawl payment details in their Cloudflare account.

**中文**

每个请求只能使用一个价格声明标头，crawler-exact-price 或crawler-max-price。 crawler-exact-price 或crawler-max-price 标头明确声明爬虫的支付意愿。如果所有检查都通过，则提供内容并记录爬网事件。如果请求的任何方面无效，边缘将返回 HTTP 402 Payment Needed 响应。财务结算 爬网程序运营商和内容所有者必须在其 Cloudflare 帐户中配置按爬网付费的付款详细信息。

### 段落 14

**EN**

Billing events are recorded each time a crawler makes an authenticated request with payment intent and receives an HTTP 200-level response with a crawler-charged header. Cloudflare then aggregates all the events, charges the crawler, and distributes the earnings to the publisher. Content for crawlers today, agents tomorrow At its core, pay per crawl begins a technical shift in how content is controlled online. By providing creators with a robust, programmatic mechanism for valuing and controlling their digital assets, we empower them to continue creating the rich, diverse content that makes the Internet invaluable.

**中文**

每次爬网程序发出带有付款意图的经过身份验证的请求并收到带有爬网程序收费标头的 HTTP 200 级别响应时，都会记录计费事件。然后，Cloudflare 聚合所有事件，向爬虫收费，并将收入分配给发布者。今天为爬虫提供内容，明天为代理提供内容 从本质上讲，按爬行付费开始了在线内容控制方式的技术转变。通过为创作者提供强大的、程序化的机制来评估和控制他们的数字资产，我们使他们能够继续创造丰富、多样化的内容，从而使互联网变得无价。

### 段落 15

**EN**

We expect pay per crawl to evolve significantly. It’s very early: we believe many different types of interactions and marketplaces can and should develop simultaneously. We are excited to support these various efforts and open standards. For example, a publisher or new organization might want to charge different rates for different paths or content types. How do you introduce dynamic pricing based not only upon demand, but also how many users your AI application has? How do you introduce granular licenses at internet scale, whether for training, inference , search, or something entirely new?

**中文**

我们预计每次抓取付费将显着发展。现在还为时尚早：我们相信许多不同类型的互动和市场可以而且应该同时发展。我们很高兴能够支持这些不同的努力和开放标准。例如，发布者或新组织可能希望对不同的路径或内容类型收取不同的费率。如何不仅根据需求，而且根据您的人工智能应用程序拥有多少用户来引入动态定价？如何在互联网范围内引入细粒度许可证，无论是用于训练、推理、搜索还是全新的东西？

### 段落 16

**EN**

The true potential of pay per crawl may emerge in an agentic world. What if an agentic paywall could operate entirely programmatically? Imagine asking your favorite deep research program to help you synthesize the latest cancer research or a legal brief, or just help you find the best restaurant in Soho — and then giving that agent a budget to spend to acquire the best and most relevant content. By anchoring our first solution on HTTP response code 402 , we enable a future where intelligent agents can programmatically negotiate access to digital resources. Getting started Pay per crawl is currently in private beta.

**中文**

按爬行付费的真正潜力可能会在代理世界中显现出来。如果代理付费墙可以完全以编程方式运行怎么办？想象一下，要求您最喜欢的深度研究项目来帮助您综合最新的癌症研究或法律摘要，或者只是帮助您找到 Soho 区最好的餐厅，然后为该代理人提供预算，用于获取最好和最相关的内容。通过将我们的第一个解决方案锚定在 HTTP 响应代码 402 上，我们实现了智能代理可以以编程方式协商对数字资源的访问的未来。开始使用 按抓取付费目前处于内测阶段。

### 段落 17

**EN**

We’d love to hear from you if you’re either a crawler interested in paying to access content or a content creator interested in charging for access. You can reach out to us at http://www.cloudflare.com/paypercrawl-signup/ or contact your Account Executive if you’re an existing Enterprise customer. Pay Per Crawl AI Bots Bots AI Bot Management Follow on X Will Allen | @williamallen Cloudflare | @cloudflare Related posts June 19, 2026 Temporary Cloudflare Accounts for AI agents The moment an agent needs to deploy something, it slams face-first into a wall built for humans. Today we're rolling out Temporary Accounts on Cloudflare Workers.

**中文**

如果您是有兴趣付费访问内容的爬虫或有兴趣收取访问费用的内容创建者，我们很乐意听取您的意见。您可以通过 http://www.cloudflare.com/paypercrawl-signup/ 联系我们，或者如果您是现有的 Enterprise 客户，请联系您的客户经理。按次抓取付费 AI 机器人 机器人 AI 机器人管理 关注 X Will Allen | @williamallen Cloudflare | @cloudflare 相关帖子 2026 年 6 月 19 日 AI 代理的临时 Cloudflare 帐户 当代理需要部署某些东西时，它会正面撞向为人类建造的墙壁。今天，我们在 Cloudflare Workers 上推出临时账户。

### 段落 18

**EN**

Any agent can now run wrangler deploy — temporary and get a live Worker in seconds. ... By Sid Chatterjee , Celso Martinho , Brendan Irvine-Broque Agents , Wrangler , AI , Cloudflare Workers June 18, 2026 Build your own vulnerability harness We break down the technical architecture behind our multi-stage vulnerability discovery harness and automated triage loop. Learn how we manage state controls, squash false positives through adversarial review, and route around LLM context limits. ...

**中文**

现在，任何代理都可以运行临时牧马人部署，并在几秒钟内获得实时工作人员。 ... 作者：Sid Chatterjee、Celso Martinho、Brendan Irvine-Broque Agents、Wrangler、AI、Cloudflare Workers 2026 年 6 月 18 日 构建您自己的漏洞工具 我们分解了多阶段漏洞发现工具和自动分类循环背后的技术架构。了解我们如何管理状态控制、通过对抗性审查消除误报以及绕过法学硕士背景限制。 ...

### 段落 19

**EN**

By Dan Jones , Alexandra Godoi , Grant Bourzikas Security , AI , Engineering , Research , Vulnerabilities June 17, 2026 Bringing more agent harnesses and frameworks to Cloudflare, starting with Flue The Agents SDK is now a runtime any agent framework can build on. Today we're opening up the Agents SDK primitives, with Flue as a first framework targeting Agents SDK, and rolling out agents in the dashboard. ...

**中文**

作者：Dan Jones、Alexandra Godoi、Grant Bourzikas 安全、人工智能、工程、研究、漏洞 2026 年 6 月 17 日 从 Flue 开始，将更多代理工具和框架引入 Cloudflare Agents SDK 现在是任何代理框架都可以构建的运行时。今天，我们开放 Agents SDK 原语，以 Flue 作为第一个针对 Agents SDK 的框架，并在仪表板中推出代理。 ...

### 段落 20

**EN**

By Thomas Gauvin AI , Cloudflare Workers , Developers , Developer Platform , Durable Objects , SDK , MCP June 15, 2026 Growing the Cloudflare AI team with talent from Ensemble AI Cloudflare is deepening our investment in AI with the addition of team members from Ensemble AI, focusing on machine learning infrastructure and efficiency. ...

**中文**

作者：Thomas Gauvin AI、Cloudflare Workers、开发人员、开发人员平台、Durable Objects、SDK、MCP 2026 年 6 月 15 日 利用来自 Ensemble AI 的人才壮大 Cloudflare AI 团队 Cloudflare 正在深化我们对 AI 的投资，增加了来自 Ensemble AI 的团队成员，重点关注机器学习基础设施和效率。 ...

### 段落 21

**EN**

By Alex Reneau , Zach Albertson , Michelle Chen Workers AI , AI Getting Started Free plans For enterprises Compare plans Get a recommendation Request a demo Contact Sales Resources Learning Center Analyst reports Cloudflare Radar Cloudflare TV Case Studies Webinars White Papers Developer docs theNet Solutions Connectivity cloud SSE and SASE services Application services Network services Developer services Community Community Hub Project Galileo Athenian Project Cloudflare for Campaigns Connect 2024 Support Help center Cloudflare Status Compliance GDPR Trust & Safety Company About Cloudflare Our team Investor relations Press Careers Diversity, equity & inclusion Impact/ESG Network Map Logos & press kit Become a partner © 2026 Cloudflare, Inc.

**中文**

作者：Alex Reneau、Zach Albertson、Michelle Chen 工人 AI、AI 入门 免费计划 针对企业 比较计划 获取推荐 请求演示 联系销售资源 学习中心 分析师报告 Cloudflare Radar Cloudflare TV 案例研究 网络研讨会 白皮书 开发人员文档 theNet 解决方案 连接云 SSE 和 SASE 服务 应用程序服务 网络服务 开发人员服务 社区 社区中心 项目 Galileo Athenian 项目 Cloudflare for Campaigns Connect 2024 支持 帮助中心 Cloudflare 状态 合规性 GDPR 信任与安全 公司 关于 Cloudflare 我们的团队 投资者关系 媒体 职业生涯 多元化、公平和包容性 影响/ESG 网络地图 徽标和新闻资料袋 成为合作伙伴 © 2026 Cloudflare, Inc.

### 段落 22

**EN**

| Privacy Policy | Terms of Use | Report Security Issues | Cookie Preferences | Trademark

**中文**

|隐私政策 |使用条款 |报告安全问题 | Cookie 偏好 |商标
