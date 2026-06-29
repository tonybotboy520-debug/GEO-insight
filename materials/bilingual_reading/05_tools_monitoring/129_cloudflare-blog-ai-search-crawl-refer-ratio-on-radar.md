# Cloudflare Blog - AI search crawl/refer ratio on Radar

- ID: 129
- 类型: html
- 分类: 05_tools_monitoring
- 主题: 生态/监测数据
- 原文链接: https://blog.cloudflare.com/ai-search-crawl-refer-ratio-on-radar/
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

The crawl before the fall… of referrals: understanding AI’s impact on content providers Get Started Free | Contact Sales | ▼ The Cloudflare Blog Subscribe to receive notifications of new posts: Subscribe AI Developers Radar Product News Security Policy & Legal Zero Trust Speed & Reliability Life at Cloudflare Partners AI Developers Radar Product News Security Policy & Legal Zero Trust Speed & Reliability Life at Cloudflare Partners The crawl before the fall… of referrals: understanding AI’s impact on content providers 2025-07-01 David Belson Sam Rhea 7 min read This post is also available in 简体中文 , Français , Deutsch , 日本語 , 한국어 , Español , Nederlands and 繁體中文 .

**中文**

秋天之前的爬行……推荐：了解人工智能对内容提供商的影响 免费开始 |联系销售人员 | ▼ Cloudflare 博客 订阅以接收新帖子的通知： 订阅 AI 开发人员雷达产品新闻 安全政策和法律 零信任速度和可靠性 Cloudflare 合作伙伴的生活 AI 开发人员雷达产品新闻 安全政策和法律 零信任速度和可靠性 Cloudflare 合作伙伴的生活 秋季前的爬行……推荐：了解 AI 对内容提供商的影响 2025-07-01 David Belson Sam Rhea 阅读 7 分钟 此文章也提供简体中文版本，法语、德语、日本语、한국어、西班牙语、荷兰语和繁体中文。

### 段落 2

**EN**

Content publishers welcomed crawlers and bots from search engines because they helped drive traffic to their sites. The crawlers would see what was published on the site and surface that material to users searching for it. Site owners could monetize their material because those users still needed to click through to the page to access anything beyond a short title. Artificial Intelligence (AI) bots also crawl the content of a site, but with an entirely different delivery model.

**中文**

内容发布商欢迎来自搜索引擎的爬虫和机器人，因为它们有助于增加其网站的流量。爬虫会看到网站上发布的内容，并向搜索它的用户显示该材料。网站所有者可以通过他们的材料获利，因为这些用户仍然需要点击进入页面才能访问除短标题之外的任何内容。人工智能 (AI) 机器人也会抓取网站内容，但采用完全不同的交付模式。

### 段落 3

**EN**

These Large Language Models (LLMs) do their best to read the web to train a system that can repackage that content for the user, without the user ever needing to visit the original publication. The AI applications might still try to cite the content, but we’ve found that very few users actually click through relative to how often the AI bot scrapes a given website. We have discussed this challenge in smaller settings, and today we are excited to publish our findings as a new metric shown on the AI Insights page on Cloudflare Radar .

**中文**

这些大型语言模型 (LLM) 尽最大努力阅读网络来训练一个系统，该系统可以为用户重新打包该内容，而用户无需访问原始出版物。人工智能应用程序可能仍会尝试引用内容，但我们发现，相对于人工智能机器人抓取给定网站的频率，很少有用户真正点击。我们已经在较小的环境中讨论了这一挑战，今天我们很高兴将我们的发现作为新指标发布在 Cloudflare Radar 的 AI Insights 页面上。

### 段落 4

**EN**

Visitors to Cloudflare Radar can now review how often a given AI model sends traffic to a site relative to how often it crawls that site. We are sharing this analysis with a broad audience so that site owners can have better information to help them make decisions about which AI bots to allow or block and so that users can understand how AI usage in aggregate impacts Internet traffic. How does this measurement work?

**中文**

Cloudflare Radar 的访问者现在可以查看给定 AI 模型向网站发送流量的频率相对于其抓取该网站的频率。我们正在与广大受众分享这一分析结果，以便网站所有者能够获得更好的信息，帮助他们决定允许或阻止哪些人工智能机器人，并让用户能够了解人工智能的总体使用如何影响互联网流量。这种测量是如何进行的？

### 段落 5

**EN**

As HTML pages are arguably the most valuable content for these crawlers, the ratios displayed are calculated by dividing the total number of requests from relevant user agents associated with a given search or AI platform where the response was of Content-type: text/html by the total number of requests for HTML content where the Referer header contained a hostname associated with a given search or AI platform. The diagrams below illustrate two common crawling scenarios, and show that companies may use different user agents depending on the purpose of the crawler.

**中文**

由于 HTML 页面可以说是这些爬虫程序最有价值的内容，因此显示的比率是通过将来自与给定搜索或 AI 平台（响应为内容类型：text/html）的相关用户代理的请求总数除以对 HTML 内容（其中 Referer 标头包含与给定搜索或 AI 平台关联的主机名）的请求总数来计算的。下图说明了两种常见的爬行场景，并显示公司可以根据爬行程序的目的使用不同的用户代理。

### 段落 6

**EN**

The top one represents a simple transaction where the example AI platform is requesting content for the purposes of training an LLM, representing itself as AIBot . The bottom one represents a scenario where the example AI platform is requesting content to service a user request — looking for flight information, for example. In this case, it is representing itself as AIBot-User . Request traffic from both of these user agents would be aggregated under a single platform name for the purposes of our analysis.

**中文**

最上面的一个代表一个简单的交易，其中示例 AI 平台正在请求内容以训练 LLM，将自己表示为 AIBot。底部的场景表示示例 AI 平台正在请求内容来服务用户请求，例如查找航班信息。在本例中，它将自身表示为 AIBot-User。出于我们分析的目的，来自这两个用户代理的请求流量将聚合在单个平台名称下。

### 段落 7

**EN**

When a user clicks on a link on a website or application, the client will often send a Referer: header as part of the request to the target site. In the diagram below, the example AI platform has returned content that contains links to external sites in response to a user interaction. When the user clicks on a link, a request is made to the content provider that includes ai.example.com in the Referer: header, letting them know where that request traffic came from. Hostnames are associated with their respective platforms for the purpose of our analysis.

**中文**

当用户单击网站或应用程序上的链接时，客户端通常会发送 Referer: 标头作为对目标站点的请求的一部分。在下图中，示例 AI 平台已返回包含外部站点链接的内容以响应用户交互。当用户单击链接时，系统会向内容提供商发出请求，其中在 Referer: 标头中包含 ai.example.com，让他们知道请求流量来自何处。出于我们分析的目的，主机名与其​​各自的平台相关联。

### 段落 8

**EN**

Observations Reviewing the ratios The new metric is presented as a simple table, comparing the number of aggregate HTML page requests from crawlers (user agents) associated with a given platform to the number of HTML page requests from clients referred by a hostname associated with a given platform. The calculated ratio is always normalized to a single referral request. The table below shows that for the period June 19-26, 2025, as an example, the ratios range from Anthropic’s 70,900:1 down to Mistral’s 0.1:1.

**中文**

观察回顾比率新指标以一个简单的表格形式呈现，将来自与给定平台关联的爬虫（用户代理）的聚合 HTML 页面请求数量与来自由与给定平台关联的主机名引用的客户端的 HTML 页面请求数量进行比较。计算出的比率始终标准化为单个推荐请求。下表显示，以 2025 年 6 月 19 日至 26 日为例，比率范围从 Anthropic 的 70,900:1 到 Mistral 的 0.1:1。

### 段落 9

**EN**

This means that Anthropic’s AI platform Claude made nearly 71,000 HTML page requests for every HTML page referral, while Mistral sent 10x as many referrals as crawl requests. (However, traffic referred by Claude’s native app does not include a Referer: header, and we believe that the same holds true for traffic generated from other native apps as well. As such, because the referral counts only include traffic from the Web-based tools from these providers, these calculations may overstate the respective ratios, but it is unclear by how much.) Of course, due in part to changes in crawling patterns, these ratios will change over time.

**中文**

这意味着 Anthropic 的 AI 平台 Claude 对每个 HTML 页面引用发出了近 71,000 个 HTML 页面请求，而 Mistral 发送的引用数量是抓取请求的 10 倍。 （但是，Claude 的本机应用程序引用的流量不包含 Referer: 标头，我们相信其他本机应用程序生成的流量也同样如此。因此，由于引用计数仅包括来自这些提供商的基于 Web 的工具的流量，这些计算可能夸大了各自的比率，但尚不清楚夸大了多少。）当然，部分由于抓取模式的变化，这些比率将随着时间的推移而变化。

### 段落 10

**EN**

The table above also displays the ratio changes as compared to the previous period, with changes ranging from increases of over 6% for DuckDuckGo and Yandex to Google’s 19.4% decrease. The week-over-week drop in Google’s ratio is related to an observed drop in crawling traffic from GoogleBot starting on June 24, while Yandex’s week-over-week growth is related to an observed increase in YandexBot crawling activity that started on June 21, as seen in the graphs below. Radar’s Data Explorer includes a time series view of how these ratios change over time , such as in the Baidu example below.

**中文**

上表还显示了与上一时期相比的比率变化，变化范围从 DuckDuckGo 和 Yandex 的增长超过 6% 到 Google 的下降 19.4%。 Google 比率的周环比下降与从 6 月 24 日开始观察到的 GoogleBot 抓取流量下降有关，而 Yandex 的周环比增长则与从 6 月 21 日开始观察到的 YandexBot 抓取活动增加有关，如下图所示。 Radar 的 Data Explorer 包含一个时间序列视图，显示这些比率如何随时间变化，例如下面的百度示例。

### 段落 11

**EN**

The time series data is also available through an API endpoint . Patterns in referral traffic Changes and trends in the underlying activity can be seen in the associated Data Explorer view , as well as in the raw data available via API endpoints ( timeseries , summary ). Note that the shares of both referral and crawl traffic are relative to the sets of referrers and crawlers included in the graphs, and not Cloudflare traffic overall.

**中文**

时间序列数据也可通过 API 端点获得。引荐流量的模式可以在关联的数据浏览器视图以及通过 API 端点（时间序列、摘要）提供的原始数据中看到基础活动的变化和趋势。请注意，引荐流量和爬网流量的份额与图表中包含的引荐来源网址和爬网程序集相关，而不是与总体 Cloudflare 流量相关。

### 段落 12

**EN**

For example, in the referrer-centric view below, covering nearly the first four weeks of June 2025, we can see that referral traffic is dominated by search platform Google, with a fairly consistent diurnal pattern visible in the data. (The google.* entry covers referral traffic from the main google.com site, as well as local sites, such as google.es or google.com.tw .) Because of prefetching driven by the use of speculation rules , referral traffic coming from Google’s ASN (AS15169) is specifically excluded from analysis here, as it doesn’t represent active user consumption of content.

**中文**

例如，在下面以引荐来源为中心的视图中，几乎覆盖了 2025 年 6 月的前四个星期，我们可以看到引荐流量由搜索平台 Google 主导，数据中可见相当一致的昼夜模式。 （google.* 条目涵盖来自 google.com 主站点以及本地站点（例如 google.es 或 google.com.tw）的引荐流量。）由于使用推测规则驱动的预取，来自 Google 的 ASN (AS15169) 的引荐流量在此被明确排除在分析之外，因为它不代表活跃用户对内容的消费。

### 段落 13

**EN**

Clear diurnal patterns are also visible in the referral request shares of other search platforms, although the request shares are a fraction of what is seen from Google. Throughout June, the share of traffic referred by AI platforms was significantly lower, even in aggregate, than the share of traffic referred by search platforms. Changes in crawling traffic As noted above, the change in ratio values over time can be driven by shifts in crawling activity. These shifts are visible in the crawling traffic shares available in Data Explorer , as well as in the raw data available via API endpoints ( timeseries , summary ).

**中文**

在其他搜索平台的推荐请求份额中也可以看到清晰的昼夜模式，尽管请求份额只是 Google 所见的一小部分。整个 6 月，人工智能平台引用的流量份额（即使从总体来看）也明显低于搜索平台引用的流量份额。爬行流量的变化 如上所述，比率值随时间的变化可能是由爬行活动的变化驱动的。这些变化在 Data Explorer 中可用的爬行流量份额以及通过 API 端点（时间序列、摘要）提供的原始数据中可见。

### 段落 14

**EN**

In the crawler-centric view below, covering nearly the first four weeks of June 2025, we can see that the share of requests related to Google’s crawling activity for both their Googlebot and GoogleOther identifiers falls over the course of the month, with several peak/valley periods. A similar pattern observed in HTTP request traffic from Google’s AS15169 during that same time period loosely matches this observed drop in share. In addition, it appears that OpenAI’s GPTBot saw multiple periods where little-to-no crawling activity was observed throughout the month.

**中文**

在下面以爬虫为中心的视图中，几乎覆盖了 2025 年 6 月的前四个星期，我们可以看到，与 Google 对 Googlebot 和 GoogleOther 标识符的爬行活动相关的请求份额在整个月内呈下降趋势，并出现了几个高峰/低谷期。在同一时间段内，在来自 Google AS15169 的 HTTP 请求流量中观察到的类似模式与观察到的份额下降大致相符。此外，OpenAI 的 GPTBot 似乎在整个月内多次观察到几乎没有爬行活动。

### 段落 15

**EN**

What this means for content providers These ratios directly impact the viability of content publication on the Internet. While they will vary over time, the trend continues to be more crawls and fewer referrals when compared in relation to each other. Legacy search index crawlers would scan your content a couple of times, or less, for each visitor sent. A site’s availability to crawlers made their revenue model more viable, not less. The new data we are observing suggests that is no longer the case. These models continue to consume more content, more frequently, despite sending the same or less traffic to the source of its content.

**中文**

这对内容提供商意味着什么 这些比率直接影响互联网上内容发布的可行性。虽然它们会随着时间的推移而变化，但相互比较时，趋势仍然是抓取更多、推荐更少。对于每个发送的访问者，传统的搜索索引爬虫都会扫描您的内容几次或更少。网站对爬虫的可用性使其收入模式变得更加可行，而不是更少。我们观察到的新数据表明情况已不再如此。尽管向内容源发送的流量相同或更少，但这些模型仍会继续更频繁地消费更多内容。

### 段落 16

**EN**

We have released new tools over the last year to help site owners take control back. With a single click, publishers can block the kinds of AI crawlers that train against their content . And today, we announced new ways to make the exchange of value fair for both sides of the equation. However, we continue to recommend that content creators audit and then enforce their preferred policies for AI crawlers. One more thing… In addition to providing these new insights around crawling and referral traffic and associated trends, we’ve also taken the opportunity to launch expanded Verified Bots content.

**中文**

去年我们发布了新工具来帮助网站所有者夺回控制权。只需单击一下，出版商就可以阻止针对其内容进行训练的人工智能爬虫。今天，我们宣布了使等式双方的价值交换公平的新方法。但是，我们仍然建议内容创建者审核并执行他们针对人工智能爬虫的首选策略。还有一件事......除了提供有关爬行和推荐流量以及相关趋势的新见解之外，我们还借此机会推出了扩展的已验证机器人内容。

### 段落 17

**EN**

The Bots page on Cloudflare Radar includes a paginated list of Verified Bots , displaying the bot name, owner, category, and rank (based on request volume). This list has now been expanded into a standalone directory in a new Bots section . The directory, shown below, displays a card for each Verified Bot, showing the bot name, a description, the bot owner and category, and verification status. Users can search the directory by bot name, owner, or description, and can also filter by category (selecting just Monitoring & Analytics bots, for example).

**中文**

Cloudflare Radar 上的机器人页面包括已验证机器人的分页列表，显示机器人名称、所有者、类别和排名（基于请求量）。该列表现已扩展为新的 Bots 部分中的独立目录。如下所示的目录显示每个已验证机器人的卡片，其中显示机器人名称、描述、机器人所有者和类别以及验证状态。用户可以按机器人名称、所有者或描述搜索目录，还可以按类别过滤（例如，仅选择监控和分析机器人）。

### 段落 18

**EN**

Clicking on a bot name within a card brings up a bot-specific page that includes metadata about the bot, information on how the bot’s user agent is represented in HTTP request headers and how it should be specified in robots.txt directives , and a traffic graph that shows associated HTTP request volume trends for the selected time period (with a default comparison to the previous period). Associated data is also available via the API . As we add additional information to these bot-specific pages in the future, we will document the updates in Changelog entries .

**中文**

单击卡片中的机器人名称会显示特定于机器人的页面，其中包括有关机器人的元数据、有关如何在 HTTP 请求标头中表示机器人的用户代理以及如何在 robots.txt 指令中指定的信息，以及显示所选时间段内相关 HTTP 请求量趋势的流量图（默认与上一时间段进行比较）。相关数据也可通过 API 获取。当我们将来向这些特定于机器人的页面添加其他信息时，我们将在变更日志条目中记录更新。

### 段落 19

**EN**

Pay Per Crawl Radar Internet Traffic AI Bots Follow on X David Belson | @dbelson Sam Rhea | @LakeAustinBlvd Cloudflare | @cloudflare Related posts June 19, 2026 Temporary Cloudflare Accounts for AI agents The moment an agent needs to deploy something, it slams face-first into a wall built for humans. Today we're rolling out Temporary Accounts on Cloudflare Workers. Any agent can now run wrangler deploy — temporary and get a live Worker in seconds. ...

**中文**

按次付费的雷达互联网流量人工智能机器人关注 X David Belson | @dbelson 萨姆·雷亚 | @LakeAustinBlvd Cloudflare | @cloudflare 相关帖子 2026 年 6 月 19 日 AI 代理的临时 Cloudflare 帐户 当代理需要部署某些东西时，它会正面撞向为人类建造的墙壁。今天，我们在 Cloudflare Workers 上推出临时账户。现在，任何代理都可以运行临时牧马人部署，并在几秒钟内获得实时工作人员。 ...

### 段落 20

**EN**

By Sid Chatterjee , Celso Martinho , Brendan Irvine-Broque Agents , Wrangler , AI , Cloudflare Workers June 18, 2026 Build your own vulnerability harness We break down the technical architecture behind our multi-stage vulnerability discovery harness and automated triage loop. Learn how we manage state controls, squash false positives through adversarial review, and route around LLM context limits. ...

**中文**

作者：Sid Chatterjee、Celso Martinho、Brendan Irvine-Broque Agents、Wrangler、AI、Cloudflare Workers 2026 年 6 月 18 日 构建您自己的漏洞工具 我们详细介绍了多阶段漏洞发现工具和自动分类循环背后的技术架构。了解我们如何管理状态控制、通过对抗性审查消除误报以及绕过法学硕士背景限制。 ...

### 段落 21

**EN**

By Dan Jones , Alexandra Godoi , Grant Bourzikas Security , AI , Engineering , Research , Vulnerabilities June 17, 2026 Bringing more agent harnesses and frameworks to Cloudflare, starting with Flue The Agents SDK is now a runtime any agent framework can build on. Today we're opening up the Agents SDK primitives, with Flue as a first framework targeting Agents SDK, and rolling out agents in the dashboard. ...

**中文**

作者：Dan Jones、Alexandra Godoi、Grant Bourzikas 安全、人工智能、工程、研究、漏洞 2026 年 6 月 17 日 从 Flue 开始，将更多代理工具和框架引入 Cloudflare Agents SDK 现在是任何代理框架都可以构建的运行时。今天，我们开放 Agents SDK 原语，以 Flue 作为第一个针对 Agents SDK 的框架，并在仪表板中推出代理。 ...

### 段落 22

**EN**

By Thomas Gauvin AI , Cloudflare Workers , Developers , Developer Platform , Durable Objects , SDK , MCP June 15, 2026 Growing the Cloudflare AI team with talent from Ensemble AI Cloudflare is deepening our investment in AI with the addition of team members from Ensemble AI, focusing on machine learning infrastructure and efficiency. ...

**中文**

作者：Thomas Gauvin AI、Cloudflare Workers、开发人员、开发人员平台、Durable Objects、SDK、MCP 2026 年 6 月 15 日 利用来自 Ensemble AI 的人才壮大 Cloudflare AI 团队 Cloudflare 正在深化我们对 AI 的投资，增加了来自 Ensemble AI 的团队成员，重点关注机器学习基础设施和效率。 ...

### 段落 23

**EN**

By Alex Reneau , Zach Albertson , Michelle Chen Workers AI , AI Getting Started Free plans For enterprises Compare plans Get a recommendation Request a demo Contact Sales Resources Learning Center Analyst reports Cloudflare Radar Cloudflare TV Case Studies Webinars White Papers Developer docs theNet Solutions Connectivity cloud SSE and SASE services Application services Network services Developer services Community Community Hub Project Galileo Athenian Project Cloudflare for Campaigns Connect 2024 Support Help center Cloudflare Status Compliance GDPR Trust & Safety Company About Cloudflare Our team Investor relations Press Careers Diversity, equity & inclusion Impact/ESG Network Map Logos & press kit Become a partner © 2026 Cloudflare, Inc.

**中文**

作者：Alex Reneau、Zach Albertson、Michelle Chen 工人 AI、AI 入门 免费计划 针对企业 比较计划 获取推荐 请求演示 联系销售资源 学习中心 分析师报告 Cloudflare Radar Cloudflare TV 案例研究 网络研讨会 白皮书 开发人员文档 theNet 解决方案 连接云 SSE 和 SASE 服务 应用程序服务 网络服务 开发人员服务 社区 社区中心 项目 Galileo Athenian 项目 Cloudflare for Campaigns Connect 2024 支持 帮助中心 Cloudflare 状态 合规性 GDPR 信任与安全 公司 关于 Cloudflare 我们的团队 投资者关系 媒体 职业生涯 多元化、公平和包容性 影响/ESG 网络地图 徽标和新闻资料袋 成为合作伙伴 © 2026 Cloudflare, Inc.

### 段落 24

**EN**

| Privacy Policy | Terms of Use | Report Security Issues | Cookie Preferences | Trademark

**中文**

|隐私政策 |使用条款 |报告安全问题 | Cookie 偏好 |商标
