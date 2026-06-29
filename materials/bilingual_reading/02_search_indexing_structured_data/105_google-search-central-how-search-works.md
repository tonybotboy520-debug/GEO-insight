# Google Search Central - How Search Works

- ID: 105
- 类型: html
- 分类: 02_search_indexing_structured_data
- 主题: 搜索基础机制
- 原文链接: https://developers.google.com/search/docs/fundamentals/how-search-works
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

How Search Works site , which explains how Search works from a searcher's perspective. A few notes before we get started Before we get into the details of how Search works, it's important to note that Google doesn't accept payment to crawl a site more frequently, or rank it higher. If anyone tells you otherwise, they're wrong. Google doesn't guarantee that it will crawl, index, or serve your page, even if your page follows the Google Search Essentials .

**中文**

搜索工作原理网站，从搜索者的角度解释搜索工作原理。开始之前的一些注意事项 在我们详细了解搜索的工作原理之前，需要注意的是，Google 不接受付费来更频繁地抓取网站或提高网站排名。如果有人告诉你不然，他们就错了。即使您的网页遵循 Google 搜索要点，Google 也不保证能够对您的网页进行抓取、编制索引或提供服务。

### 段落 2

**EN**

Introducing the three stages of Google Search Google Search works in three stages, and not all pages make it through each stage: Crawling: Google downloads text, images, and videos from pages it found on the internet with automated programs called crawlers. Indexing: Google analyzes the text, images, and video files on the page, and stores the information in the Google index, which is a large database. Serving search results: When a user searches on Google, Google returns information that's relevant to the user's query. Crawling The first stage is finding out what pages exist on the web.

**中文**

介绍 Google 搜索的三个阶段 Google 搜索分为三个阶段，并非所有页面都能通过每个阶段： 抓取：Google 使用称为抓取工具的自动化程序从互联网上找到的页面下载文本、图像和视频。索引：Google 分析页面上的文本、图像和视频文件，并将信息存储在 Google 索引中，Google 索引是一个大型数据库。提供搜索结果：当用户在 Google 上搜索时，Google 会返回与用户查询相关的信息。爬行第一阶段是找出网络上存在哪些页面。

### 段落 3

**EN**

There isn't a central registry of all web pages, so Google must constantly look for new and updated pages and add them to its list of known pages. This process is called "URL discovery". Some pages are known because Google has already visited them. Other pages are discovered when Google extracts a link from a known page to a new page: for example, a hub page, such as a category page, links to a new blog post. Still other pages are discovered when you submit a list of pages (a sitemap ) for Google to crawl. Once Google discovers a page's URL, it may visit (or "crawl") the page to find out what's on it.

**中文**

没有所有网页的中央注册表，因此谷歌必须不断寻找新的和更新的页面并将它们添加到其已知页面列表中。此过程称为“URL 发现”。有些页面是已知的，因为 Google 已经访问过它们。当 Google 提取从已知页面到新页面的链接时，会发现其他页面：例如，中心页面（例如类别页面）链接到新博客文章。当您提交页面列表（站点地图）供 Google 抓取时，还会发现其他页面。一旦 Google 发现某个页面的 URL，它就可能会访问（或“抓取”）该页面以找出其上的内容。

### 段落 4

**EN**

We use a huge set of computers to crawl billions of pages on the web. The program that does the fetching is called Googlebot (also known as a crawler, robot, bot, or spider). Googlebot uses an algorithmic process to determine which sites to crawl, how often, and how many pages to fetch from each site. Google's crawlers are also programmed such that they try not to crawl the site too fast to avoid overloading it. This mechanism is based on the responses of the site (for example, HTTP 500 errors mean "slow down" ). However, Googlebot doesn't crawl all the pages it discovered.

**中文**

我们使用大量计算机来抓取网络上数十亿个页面。执行抓取操作的程序称为 Googlebot（也称为爬虫、机器人、机器人或蜘蛛）。 Googlebot 使用算法过程来确定抓取哪些网站、抓取的频率以及从每个网站抓取的页面数量。谷歌的抓取工具也经过编程，尽量不要抓取网站太快，以避免网站过载。该机制基于站点的响应（例如，HTTP 500 错误意味着“放慢速度”）。但是，Googlebot 不会抓取它发现的所有网页。

### 段落 5

**EN**

Some pages may be disallowed for crawling by the site owner, other pages may not be accessible without logging in to the site. During the crawl, Google renders the page and runs any JavaScript it finds using a recent version of Chrome , similar to how your browser renders pages you visit. Rendering is important because websites often rely on JavaScript to bring content to the page, and without rendering Google might not see that content. Crawling depends on whether Google's crawlers can access the site.

**中文**

网站所有者可能禁止抓取某些页面，如果不登录网站则可能无法访问其他页面。在抓取过程中，Google 会使用最新版本的 Chrome 渲染页面并运行它找到的任何 JavaScript，类似于浏览器渲染您访问的页面的方式。渲染很重要，因为网站通常依赖 JavaScript 将内容带到页面，如果不渲染，Google 可能看不到该内容。抓取取决于Google的抓取工具是否可以访问该网站。

### 段落 6

**EN**

Some common issues with Googlebot accessing sites include: Problems with the server handling the site Network issues robots.txt rules preventing Googlebot's access to the page Indexing After a page is crawled, Google tries to understand what the page is about. This stage is called indexing and it includes processing and analyzing the textual content and key content tags and attributes, such as <title> elements and alt attributes, images , videos , and more. During the indexing process, Google determines if a page is a duplicate of another page on the internet or canonical . The canonical is the page that may be shown in search results.

**中文**

Googlebot 访问网站的一些常见问题包括： 处理网站的服务器问题 网络问题 robots.txt 规则阻止 Googlebot 访问网页 索引 抓取网页后，Google 会尝试了解该网页的内容。此阶段称为索引，它包括处理和分析文本内容以及关键内容标签和属性，例如 <title> 元素和 alt 属性、图像、视频等。在索引过程中，Google 会确定某个页面是否与互联网上的另一个页面重复或是否规范。规范页面是可能在搜索结果中显示的页面。

### 段落 7

**EN**

To select the canonical, we first group together (also known as clustering) the pages that we found on the internet that have similar content, and then we select the one that's most representative of the group. The other pages in the group are alternate versions that may be served in different contexts, like if the user is searching from a mobile device or they're looking for a very specific page from that cluster. Google also collects signals about the canonical page and its contents, which may be used in the next stage, where we serve the page in search results.

**中文**

为了选择规范，我们首先将在互联网上找到的具有相似内容的页面分组在一起（也称为聚类），然后选择最有代表性的页面。该组中的其他页面是可以在不同上下文中提供的替代版本，例如用户正在从移动设备进行搜索或者他们正在从该集群中查找非常特定的页面。谷歌还收集有关规范页面及其内容的信号，这些信号可能会在下一阶段使用，即我们在搜索结果中提供页面。

### 段落 8

**EN**

Some signals include the language of the page, the country the content is local to, and the usability of the page. The collected information about the canonical page and its cluster may be stored in the Google index, a large database hosted on thousands of computers. Indexing isn't guaranteed; not every page that Google processes will be indexed. Indexing also depends on the content of the page and its metadata.

**中文**

一些信号包括页面的语言、内容所在的国家/地区以及页面的可用性。收集到的关于规范页面及其集群的信息可以存储在 Google 索引中，Google 索引是托管在数千台计算机上的大型数据库。不保证索引；并非 Google 处理的每个页面都会被编入索引。索引还取决于页面的内容及其元数据。

### 段落 9

**EN**

Some common indexing issues can include: The quality of the content on page is low Robots meta rules disallow indexing The design of the website might make indexing difficult Serving search results Google doesn't accept payment to rank pages higher, and ranking is done programmatically. Learn more about ads on Google Search . When a user enters a query, our machines search the index for matching pages and return the results we believe are the highest quality and most relevant to the user's query.

**中文**

一些常见的索引问题可能包括： 页面内容质量低 机器人元规则不允许索引 网站的设计可能会使索引变得困难 提供搜索结果 Google 不接受付费来对页面进行更高的排名，并且排名是通过编程完成的。详细了解 Google 搜索上的广告。当用户输入查询时，我们的机器会在索引中搜索匹配的页面，并返回我们认为质量最高且与用户查询最相关的结果。

### 段落 10

**EN**

Relevancy is determined by hundreds of factors, which could include information such as the user's location, language, and device (desktop or phone). For example, searching for "bicycle repair shops" would show different results to a user in Paris than it would to a user in Hong Kong. Based on the user's query the search features that appear on the search results page also change. For example, searching for "bicycle repair shops" will likely show local results and no image results , however searching for "modern bicycle" is more likely to show image results, but not local results.

**中文**

相关性由数百个因素决定，其中可能包括用户位置、语言和设备（桌面或电话）等信息。例如，搜索“自行车修理店”向巴黎的用户显示的结果与向香港的用户显示的结果不同。根据用户的查询，搜索结果页面上显示的搜索功能也会发生变化。例如，搜索“自行车修理店”可能会显示本地结果，而不会显示图像结果，但是搜索“现代自行车”更有可能显示图像结果，但不会显示本地结果。

### 段落 11

**EN**

You can explore the most common UI elements of Google web search in our Visual Element gallery . Search Console might tell you that a page is indexed, but you don't see it in search results. This might be because: The content on the page is irrelevant to users' queries The quality of the content is low Robots meta rules prevent serving While this guide explains how Search works, we are always working on improving our algorithms. You can keep track of these changes by following the Google Search Central blog .

**中文**

您可以在我们的视觉元素库中探索 Google 网络搜索最常见的 UI 元素。 Search Console 可能会告诉您某个页面已编入索引，但您在搜索结果中看不到它。这可能是因为： 页面上的内容与用户的查询无关 内容质量低 机器人元规则阻止服务 虽然本指南解释了搜索的工作原理，但我们始终致力于改进我们的算法。您可以通过关注 Google 搜索中心博客来跟踪这些更改。

### 段落 12

**EN**

Send feedback Except as otherwise noted, the content of this page is licensed under the Creative Commons Attribution 4.0 License , and code samples are licensed under the Apache 2.0 License . For details, see the Google Developers Site Policies . Java is a registered trademark of Oracle and/or its affiliates. Last updated 2025-12-18 UTC. Need to tell us more?

**中文**

发送反馈 除非另有说明，本页内容已根据 Creative Commons Attribution 4.0 License 获得许可，代码示例根据 Apache 2.0 License 获得许可。有关详细信息，请参阅 Google 开发者网站政策。 Java 是 Oracle 和/或其附属公司的注册商标。最后更新时间：世界标准时间 2025 年 12 月 18 日。需要告诉我们更多吗？

### 段落 13

**EN**

[[["Easy to understand","easyToUnderstand","thumb-up"],["Solved my problem","solvedMyProblem","thumb-up"],["Other","otherUp","thumb-up"]],[["Missing the information I need","missingTheInformationINeed","thumb-down"],["Too complicated / too many steps","tooComplicatedTooManySteps","thumb-down"],["Out of date","outOfDate","thumb-down"],["Samples / code issue","samplesCodeIssue","thumb-down"],["Other","otherDown","thumb-down"]],["Last updated 2025-12-18 UTC."],[],["Google Search operates in three stages: crawling, indexing, and serving.

**中文**

[[["易于理解","easyToUnderstand","thumb-up"],["解决了我的问题","solvedMyProblem","thumb-up"],["其他","otherUp","thumb-up"]],[["缺少我需要的信息","missingTheInformationINeed","thumb-down"],["太复杂/太复杂许多步骤","tooComplicatedTooManySteps","thumb-down"],["过时","outOfDate","thumb-down"],["示例/代码问题","samplesCodeIssue","thumb-down"],["其他","otherDown","thumb-down"]],["最后更新时间为2025年12月18日UTC。"],[],["Google 搜索分三个阶段运行：抓取、索引和服务。

### 段落 14

**EN**

Crawling involves automated web crawlers (Googlebot) discovering and downloading content (text, images, videos) from web pages. Indexing analyzes this content, determining its relevance and canonical status, storing it in Google's database. Serving involves matching user queries with indexed pages and displaying the most relevant results, considering factors like user location and device.

**中文**

爬行涉及自动网络爬虫（Googlebot）从网页中发现和下载内容（文本、图像、视频）。索引分析该内容，确定其相关性和规范状态，并将其存储在 Google 的数据库中。服务涉及将用户查询与索引页面进行匹配并显示最相关的结果，同时考虑用户位置和设备等因素。

### 段落 15

**EN**

Google does not accept payment for crawling, indexing or ranking and can't guarantee that the content will be crawled, indexed or served.\n"]] LinkedIn Join us on LinkedIn YouTube Watch our videos Blog Subscribe to our RSS feed Podcast Listen to Search Off the Record X (Twitter) Join us on X (Twitter) Get support Go to the help forum Submit a question for office hours Report spam, phishing, or malware More support resources Resources Do you need an SEO?

**中文**

Google 不接受为抓取、索引或排名付费，并且不能保证内容将被抓取、索引或提供。\n"]] LinkedIn 在 LinkedIn 上加入我们 YouTube 观看我们的视频 博客 订阅我们的 RSS 源 播客 收听搜索 不记录 X (Twitter) 在 X 上加入我们 (Twitter) 获取支持 转至帮助论坛 在办公时间提交问题 报告垃圾邮件、网络钓鱼或恶意软件 更多支持资源 资源 您需要 SEO 吗？

### 段落 16

**EN**

SEO Starter Guide Status of Search systems Search Console documentation Case Studies Tools Search Console Rich Results Test PageSpeed Insights AMP Test Android Chrome Firebase Google Cloud Platform Google AI All products Terms Privacy Manage cookies English Deutsch Español Español – América Latina Français Indonesia Italiano Polski Português – Brasil Tiếng Việt Türkçe Русский العربيّة हिंदी ภาษาไทย 中文 – 简体 中文 – 繁體 日本語 한국어

**中文**

SEO 入门指南 搜索系统状态 搜索控制台文档 案例研究 工具 搜索控制台 富结果测试 PageSpeed Insights AMP 测试 Android Chrome Firebase Google Cloud Platform Google AI 所有产品 条款 隐私 管理 cookie 英语 德语 西班牙语 法语 印度尼西亚 意大利语 波兰语 葡萄牙语 – 巴西 Tiếng Việt Türkçe Русский ????????? हिंदी ภาษาไทย 中文 – 简体中文 – 繁体日本语 한국어
