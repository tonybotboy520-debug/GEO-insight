# Anthropic Support - Claude crawlers and blocking

- ID: 102
- 类型: html
- 分类: 01_official_ai_search_crawlers
- 主题: 官方机制/爬虫
- 原文链接: https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

Does Anthropic crawl data from the web, and how can site owners block the crawler? | Claude Help Center Skip to main content API Docs Release Notes How to Get Support English Français Deutsch Bahasa Indonesia Italiano 日本語 한국어 Português Pусский 简体中文 Español 繁體中文 English API Docs Release Notes How to Get Support English Français Deutsch Bahasa Indonesia Italiano 日本語 한국어 Português Pусский 简体中文 Español 繁體中文 English Search for articles... All Collections Privacy and legal Does Anthropic crawl data from the web, and how can site owners block the crawler? Does Anthropic crawl data from the web, and how can site owners block the crawler?

**中文**

Anthropic 是否从网络上抓取数据？网站所有者如何阻止抓取工具？ | Claude 帮助中心 跳至主要内容 API 文档 发行说明 如何获得支持 English Français Deutsch Bahasa Indonesia Italiano 日本语 한국어 Português Pусский 简体中文 Español 繁体中文 English API 文档 发行说明 如何获得支持 English Français Deutsch Bahasa Indonesia Italiano 日本语 한국어 Português Pусский 简体中文 Español 繁体中文 English 搜索文章... 所有收藏 隐私和法律 Anthropic 是否从网络上抓取数据？网站所有者如何阻止抓取工具？ Anthropic 是否从网络上抓取数据？网站所有者如何阻止抓取工具？

### 段落 2

**EN**

April 7, 2026 As per industry standard, Anthropic uses a variety of robots to gather data from the public web for model development, to search the web, and to retrieve web content at users’ direction. Anthropic uses different robots to enable website owner transparency and choice. Below is information on the three robots that Anthropic uses and how to set your site preferences to enable those you want to access your content and limit those you don’t.

**中文**

2026 年 4 月 7 日 根据行业标准，Anthropic 使用各种机器人从公共网络收集数据以进行模型开发、搜索网络并按照用户的指示检索网络内容。 Anthropic 使用不同的机器人来提高网站所有者的透明度和选择权。以下是有关 Anthropic 使用的三个机器人的信息，以及如何设置您的网站首选项，以允许您想要访问您的内容的人并限制那些您不想访问的人。

### 段落 3

**EN**

Bot Use What happens when you disable it ClaudeBot ClaudeBot helps enhance the utility and safety of our generative AI models by collecting web content that could potentially contribute to their training. When a site restricts ClaudeBot access, it signals that the site's future materials should be excluded from our AI model training datasets. Claude-User Claude-User supports Claude AI users. When individuals ask questions to Claude, it may access websites using a Claude-User agent. Claude-User allows site owners to control which sites can be accessed through these user-initiated requests.

**中文**

机器人使用 禁用它后会发生什么 ClaudeBot ClaudeBot 通过收集可能有助于其训练的 Web 内容，帮助增强我们的生成式 AI 模型的实用性和安全性。当某个网站限制 ClaudeBot 访问时，就表明该网站未来的材料应从我们的 AI 模型训练数据集中排除。 Claude-User Claude-User 支持 Claude AI 用户。当个人向 Claude 提问时，它可能会使用 Claude 用户代理访问网站。 Claude-User 允许网站所有者通过这些用户发起的请求来控制可以访问哪些网站。

### 段落 4

**EN**

Disabling Claude-User on your site prevents our system from retrieving your content in response to a user query, which may reduce your site's visibility for user-directed web search. Claude-SearchBot Claude-SearchBot navigates the web to improve search result quality for users. It analyzes online content specifically to enhance the relevance and accuracy of search responses. Disabling Claude-SearchBot on your site prevents our system from indexing your content for search optimization, which may reduce your site's visibility and accuracy in user search results.

**中文**

在您的网站上禁用 Claude-User 会阻止我们的系统响应用户查询来检索您的内容，这可能会降低您的网站在用户引导的网络搜索中的可见性。 Claude-SearchBot Claude-SearchBot 导航网络以提高用户的搜索结果质量。它专门分析在线内容，以提高搜索响应的相关性和准确性。在您的网站上禁用 Claude-SearchBot 会阻止我们的系统对您的内容编制索引以进行搜索优化，这可能会降低您网站在用户搜索结果中的可见性和准确性。

### 段落 5

**EN**

As part of our mission to build safe and reliable frontier systems and advance the field of responsible AI development, we’re sharing the principles by which we collect data as well as instructions on how to opt out of our crawling going forward: Our collection of data should be transparent . Anthropic uses the Bots described above to access web content. Our crawling should not be intrusive or disruptive . We aim for minimal disruption by being thoughtful about how quickly we crawl the same domains and respecting Crawl-delay where appropriate.

**中文**

作为我们构建安全可靠的前沿系统并推进负责任的人工智能开发领域的使命的一部分，我们正在分享我们收集数据的原则以及如何选择退出我们的爬行的说明：我们的数据收集应该是透明的。 Anthropic 使用上述机器人来访问 Web 内容。我们的爬行不应该是侵入性的或破坏性的。我们的目标是通过考虑抓取相同域的速度并在适当的情况下尊重抓取延迟来最大限度地减少干扰。

### 段落 6

**EN**

Anthropic’s Bots respect “do not crawl” signals by honoring industry standard directives in robots.txt. Anthropic’s Bots respect anti-circumvention technologies (e.g., we will not attempt to bypass CAPTCHAs for the sites we crawl.) To limit crawling activity, we support the non-standard Crawl-delay extension to robots.txt. An example of this might be: User-agent: ClaudeBot Crawl-delay: 1 To block a Bot from your entire website, add this to the robots.txt file in your top-level directory. Please do this for every subdomain that you wish to opt out from.

**中文**

Anthropic 的机器人通过遵守 robots.txt 中的行业标准指令来尊重“请勿抓取”信号。 Anthropic 的机器人尊重反规避技术（例如，我们不会尝试绕过我们抓取的网站的验证码。）为了限制抓取活动，我们支持 robots.txt 的非标准抓取延迟扩展。例如： 用户代理：ClaudeBot 抓取延迟：1 要阻止机器人访问您的整个网站，请将其添加到顶级目录中的 robots.txt 文件中。请对您希望退出的每个子域执行此操作。

### 段落 7

**EN**

An example of this is: User-agent: ClaudeBot Disallow: / Opting out of being crawled by Anthropic Bots requires modifying the robots.txt file in the manner above. Alternate methods like blocking IP address(es) from which Anthropic Bots operates may not work correctly or persistently guarantee an opt-out, as doing so impedes our ability to read your robots.txt file. If a crawler has a source IP address on this list , it indicates that the crawler is coming from Anthropic. You can learn more about our data handling practices and commitments at our Help Center .

**中文**

例如： 用户代理：ClaudeBot 禁止：/ 选择不被 Anthropic Bot 抓取需要按照上述方式修改 robots.txt 文件。阻止 Anthropic Bot 运行的 IP 地址等替代方法可能无法正常工作或持续保证选择退出，因为这样做会妨碍我们读取您的 robots.txt 文件。如果某个爬虫的源IP地址在此列表中，则表明该爬虫来自Anthropic。您可以在我们的帮助中心了解有关我们的数据处理实践和承诺的更多信息。

### 段落 8

**EN**

If you have further questions, or believe that our Bots may be malfunctioning, please reach out to [email protected] . Please reach out from an email that includes the domain you are contacting us about, as it is otherwise difficult to verify reports. You can be notified of substantial changes to this article by clicking here and completing the form: Subscribe to updates Related Articles Reporting, Blocking, and Removing Content from Claude How to get support Reporting, Blocking, and Removing Content from Claude Get started with Claude in Chrome Claude in Chrome Permissions Guide Did this answer your question?

**中文**

如果您还有其他疑问，或认为我们的机器人可能出现故障，请联系 [email protected]。请通过包含您与我们联系的域的电子邮件进行联系，否则很难验证报告。单击此处并填写表格，您可以收到有关本文的重大更改的通知： 订阅更新 相关文章 报告、阻止和删除 Claude 的内容 如何获得支持 报告、阻止和删除 Claude 的内容 在 Chrome 中开始使用 Claude Chrome 权限指南中的 Claude 这是否回答了您的问题？

### 段落 9

**EN**

😞 😐 😃 Product Research Company News Careers Terms of Service - Consumer Terms of Service - Commercial Privacy Policy Usage Policy Responsible Disclosure Policy Compliance

**中文**

😞 😐 😃 产品研究 公司新闻 职业生涯 服务条款 - 消费者服务条款 - 商业 隐私政策 使用政策 负责任的披露政策 合规性
