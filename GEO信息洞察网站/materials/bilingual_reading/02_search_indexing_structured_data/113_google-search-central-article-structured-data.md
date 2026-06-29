# Google Search Central - Article structured data

- ID: 113
- 类型: html
- 分类: 02_search_indexing_structured_data
- 主题: 结构化数据
- 原文链接: https://developers.google.com/search/docs/appearance/structured-data/article
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

Article structured data to your news, blog, and sports article pages can help Google understand more about the web page and show better title text , images, and date information for the article in search results on Google Search and other properties (for example, Google News and the Google Assistant ). While there's no markup requirement to be eligible for Google News features like Top stories , you can add Article to more explicitly tell Google what your content is about (for example, that it's a news article, who the author is, or what the title of the article is). Example Here's an example of a page with Article structured data.

**中文**

新闻、博客和体育文章页面的文章结构化数据可以帮助 Google 了解有关网页的更多信息，并在 Google 搜索和其他媒体资源（例如 Google 新闻和 Google 助理）的搜索结果中显示更好的文章标题文本、图像和日期信息。虽然没有标记要求才能使用热门新闻等 Google 新闻功能，但您可以添加文章来更明确地告诉 Google 您的内容是关于什么的（例如，这是一篇新闻文章、作者是谁或文章的标题是什么）。示例 以下是包含文章结构化数据的页面示例。

### 段落 2

**EN**

JSON-LD <html> <head> <title>Title of a News Article</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "NewsArticle", "headline": "Title of a News Article", "image": [ "https://example.com/photos/1x1/photo.jpg", "https://example.com/photos/4x3/photo.jpg", "https://example.com/photos/16x9/photo.jpg" ], "datePublished": "2024-01-05T08:00:00+08:00", "dateModified": "2024-02-05T09:20:00+08:00", "author": [{ "@type": "Person", "name": "Jane Doe", "url": "https://example.com/profile/janedoe123" },{ "@type": "Person", "name": "John Doe", "url": "https://example.com/profile/johndoe123" }] } </script> </head> <bo

**中文**

JSON-LD <html> <head> <title>新闻文章标题</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "NewsArticle", "headline": "新闻文章标题", "image": [ "https://example.com/photos/1x1/photo.jpg", "https://example.com/photos/4x3/photo.jpg", "https://example.com/photos/16x9/photo.jpg" ], "datePublished": "2024-01-05T08:00:00+08:00", "dateModified": "2024-02-05T09:20:00+08:00", "author": [{ "@type": "Person", "name": "Jane Doe", "url": "https://example.com/profile/janedoe123" },{ "@type": "Person", "name": "John Doe", "url": "https://example.com/profile/johndoe123" }] } </script> </head> <bo

### 段落 3

**EN**

dy> </body> </html> <html> <head> <title>Title of a News Article</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "NewsArticle", "headline": "Title of a News Article", "image": [ "https://example.com/photos/1x1/photo.jpg", "https://example.com/photos/4x3/photo.jpg", "https://example.com/photos/16x9/photo.jpg" ], "datePublished": "2024-01-05T08:00:00+08:00", "dateModified": "2024-02-05T09:20:00+08:00", "author": [{ "@type": "Person", "name": "Jane Doe", "url": "https://example.com/profile/janedoe123" },{ "@type": "Person", "name": "John Doe", "url": "https://example.com/profile/johndoe123" }] } </script>

**中文**

dy> </body> </html> <html> <head> <title>新闻文章标题</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "NewsArticle", "headline": "新闻文章标题", "image": [ "https://example.com/photos/1x1/photo.jpg", “https://example.com/photos/4x3/photo.jpg”，“https://example.com/photos/16x9/photo.jpg”]，“datePublished”：“2024-01-05T08：00：00+08：00”，“dateModified”：“2024-02-05T09：20：00+08：00”，“作者”：[{ "@type": "Person", "name": "Jane Doe", "url": "https://example.com/profile/janedoe123" },{ "@type": "Person", "name": "John Doe", "url": "https://example.com/profile/johndoe123" }] } </script>

### 段落 4

**EN**

</head> <body> </body> </html> Microdata <html> <head> <title>Title of a News Article</title> </head> <body> <div itemscope itemtype="https://schema.org/NewsArticle"> <div itemprop="headline">Title of News Article</div> <meta itemprop="image" content="https://example.com/photos/1x1/photo.jpg" /> <meta itemprop="image" content="https://example.com/photos/4x3/photo.jpg" /> <img itemprop="image" src="https://example.com/photos/16x9/photo.jpg" /> <div> <span itemprop="datePublished" content="2024-01-05T08:00:00+08:00"> January 5, 2024 at 8:00am </span> (last modified <span itemprop="dateModified" content="2024-02-05T09:20:00+08:00"> February 5,

**中文**

</head> <body> </body> </html> 微数据 <html> <head> <title>新闻文章标题</title> </head> <body> <div itemscope itemtype="https://schema.org/NewsArticle"> <div itemprop="headline">新闻文章标题</div> <meta itemprop="image" content="https://example.com/photos/1x1/photo.jpg" /> <meta itemprop="image" content="https://example.com/photos/4x3/photo.jpg" /> <img itemprop="image" src="https://example.com/photos/16x9/photo.jpg" /> <div> <span itemprop="datePublished" content="2024-01-05T08:00:00+08:00"> 2024 年 1 月 5 日上午 8:00 </span>（最后修改<span itemprop="dateModified" content="2024-02-05T09:20:00+08:00"> 2 月 5 日

### 段落 5

**EN**

2024 at 9:20am </span> ) </div> <div> by <span itemprop="author" itemscope itemtype="https://schema.org/Person"> <a itemprop="url" href="https://example.com/profile/janedoe123"> <span itemprop="name">Jane Doe</span> </a> </span> and <span itemprop="author" itemscope itemtype="https://schema.org/Person"> <a itemprop="url" href="https://example.com/profile/johndoe123"> <span itemprop="name">John Doe</span> </a> </span> </div> </div> </body> </html> <html> <head> <title>Title of a News Article</title> </head> <body> <div itemscope itemtype="https://schema.org/NewsArticle"> <div itemprop="headline">Title of News Article</div> <meta itemprop="imag

**中文**

2024 年上午 9:20 </span> ) </div> <div> 作者： <span itemprop="author" itemscope itemtype="https://schema.org/Person"> <a itemprop="url" href="https://example.com/profile/janedoe123"> <span itemprop="name">Jane Doe</span> </a> </span> 和 <span itemprop="author" itemscope itemtype="https://schema.org/Person"> <a itemprop="url" href="https://example.com/profile/johndoe123"> <span itemprop="name">John Doe</span> </a> </span> </div> </div> </body> </html> <html> <head> <title>新闻文章标题</title> </head> <body> <div itemscope itemtype="https://schema.org/NewsArticle"> <div itemprop="headline">新闻文章标题</div> <meta itemprop="imag

### 段落 6

**EN**

e" content="https://example.com/photos/1x1/photo.jpg" /> <meta itemprop="image" content="https://example.com/photos/4x3/photo.jpg" /> <img itemprop="image" src="https://example.com/photos/16x9/photo.jpg" /> <div> <span itemprop="datePublished" content="2024-01-05T08:00:00+08:00"> January 5, 2024 at 8:00am </span> (last modified <span itemprop="dateModified" content="2024-02-05T09:20:00+08:00"> February 5, 2024 at 9:20am </span> ) </div> <div> by <span itemprop="author" itemscope itemtype="https://schema.org/Person"> <a itemprop="url" href="https://example.com/profile/janedoe123"> <span itemprop="name">Jane Doe</span> </a> </span> and <span it

**中文**

e" content="https://example.com/photos/1x1/photo.jpg" /> <meta itemprop="image" content="https://example.com/photos/4x3/photo.jpg" /> <img itemprop="image" src="https://example.com/photos/16x9/photo.jpg" /> <div> <span itemprop="datePublished" content="2024-01-05T08:00:00+08:00"> 2024 年 1 月 5 日上午 8:00 </span> （最后修改 <span itemprop="dateModified" content="2024-02-05T09:20:00+08:00"> 2024 年 2 月 5 日上午 9:20 </span> ） </div> <div> 作者： <span itemprop="author" itemscope itemtype="https://schema.org/Person"> <a itemprop="url" href="https://example.com/profile/janedoe123"> <span itemprop="name">Jane Doe</span> </a> </span> 和 <span it

### 段落 7

**EN**

emprop="author" itemscope itemtype="https://schema.org/Person"> <a itemprop="url" href="https://example.com/profile/johndoe123"> <span itemprop="name">John Doe</span> </a> </span> </div> </div> </body> </html> How to add structured data Structured data is a standardized format for providing information about a page and classifying the page content.

**中文**

emprop="author" itemscope itemtype="https://schema.org/Person"> <a itemprop="url" href="https://example.com/profile/johndoe123"> <span itemprop="name">John Doe</span> </a> </span> </div> </div> </body> </html> 如何添加结构化数据 结构化数据是一种标准化格式，用于提供有关页面的信息并对页面内容进行分类。

### 段落 8

**EN**

If you're new to structured data, you can learn more about how structured data works . Here's an overview of how to build, test, and release structured data. Add as many recommended properties that apply to your web page. There are no required properties; instead, add the properties that apply to your content. Based on the format you're using, learn where to insert structured data on the page . Using a CMS? It may be easier to use a plugin that's integrated into your CMS. Using JavaScript? Learn how to generate structured data with JavaScript . Follow the guidelines . Validate your code using the Rich Results Test and fix any critical errors.

**中文**

如果您不熟悉结构化数据，可以详细了解结构化数据的工作原理。以下概述了如何构建、测试和发布结构化数据。添加尽可能多的适用于您的网页的推荐属性。没有必需的属性；相反，添加适用于您的内容的属性。根据您使用的格式，了解在页面上的何处插入结构化数据。使用内容管理系统？使用集成到 CMS 中的插件可能会更容易。使用 JavaScript？了解如何使用 JavaScript 生成结构化数据。遵循指导方针。使用丰富的结果测试验证您的代码并修复任何严重错误。

### 段落 9

**EN**

Consider also fixing any non-critical issues that may be flagged in the tool, as they can help improve the quality of your structured data (however, this isn't necessary to be eligible for rich results). Deploy a few pages that include your structured data and use the URL Inspection tool to test how Google sees the page. Be sure that your page is accessible to Google and not blocked by a robots.txt file, the noindex tag, or login requirements. If the page looks okay, you can ask Google to recrawl your URLs . Note : Allow time for re-crawling and re-indexing.

**中文**

还应考虑修复工具中可能标记的任何非关键问题，因为它们可以帮助提高结构化数据的质量（但是，这并不是获得丰富结果的必要条件）。部署一些包含结构化数据的页面，并使用 URL 检查工具来测试 Google 如何查看该页面。确保 Google 可以访问您的网页，并且不会被 robots.txt 文件、noindex 标记或登录要求阻止。如果页面看起来没问题，您可以要求 Google 重新抓取您的网址。注意：留出时间进行重新爬网和重新索引。

### 段落 10

**EN**

Remember that it may take several days after publishing a page for Google to find and crawl it. To keep Google informed of future changes, we recommend that you submit a sitemap . You can automate this with the Search Console Sitemap API . Guidelines You must follow these guidelines to enable structured data to be eligible for inclusion in Google Search results. Warning: If your site violates one or more of these guidelines, then Google may take manual action against it. Once you have remedied the problem, you can submit your site for reconsideration .

**中文**

请记住，发布页面后 Google 可能需要几天时间才能找到并抓取该页面。为了让 Google 了解未来的变化，我们建议您提交站点地图。您可以使用 Search Console Sitemap API 自动执行此操作。准则 您必须遵循这些准则才能使结构化数据有资格包含在 Google 搜索结果中。警告：如果您的网站违反了这些准则中的一项或多项，那么 Google 可能会对其采取手动操作。解决问题后，您可以提交您的网站以供重新审核。

### 段落 11

**EN**

Search Essentials General structured data guidelines Technical guidelines Technical guidelines For multi-part articles, make sure that the rel=canonical points at either each individual page or a "view-all" page (and not to page 1 of a multi-part series). Learn more about canonicalization . If you offer subscription-based access to your website content, or if users must register for access, consider adding structured data for subscription and paywalled content . Structured data type definitions To help Google better understand your page, include as many recommended properties that apply to your web page.

**中文**

搜索要点 一般结构化数据指南 技术指南 技术指南 对于多部分文章，请确保 rel=canonical 指向每个单独页面或“查看全部”页面（而不是多部分系列的第 1 页）。了解有关规范化的更多信息。如果您提供对网站内容的基于订阅的访问，或者用户必须注册才能访问，请考虑为订阅和付费内容添加结构化数据。结构化数据类型定义 为了帮助 Google 更好GEO解您的网页，请包含尽可能多的适用于您的网页的推荐属性。

### 段落 12

**EN**

There are no required properties; instead, add the properties that apply to your content. Article objects Article objects must be based on one of the following schema.org types: Article , NewsArticle , BlogPosting . The Google-supported properties are the following: Recommended properties author Person or Organization The author of the article. To help Google best understand authors across various features, we recommend following the author markup best practices . author.name Text The name of the author. author.url URL A link to a web page that uniquely identifies the author of the article.

**中文**

没有必需的属性；相反，添加适用于您的内容的属性。文章对象 文章对象必须基于以下 schema.org 类型之一： Article、 NewsArticle、 BlogPosting。 Google 支持的属性如下： 推荐属性 作者 个人或组织 文章的作者。为了帮助 Google 更好地了解作者的各种功能，我们建议遵循作者标记最佳实践。 author.name 文本 作者姓名。 author.url URL 指向唯一标识文章作者的网页的链接。

### 段落 13

**EN**

For example, the author's social media page, an "about me" page, or a bio page. If the URL is an internal profile page, we recommend marking up that author using profile page structured data . You can use the sameAs property as an alternative. Google can understand both sameAs and url when disambiguating authors. dateModified DateTime The date and time the article was most recently modified, in ISO 8601 format . We recommend that you provide timezone information; otherwise, we will default to the timezone used by Googlebot . Add the dateModified property if you want to provide more accurate date information to Google.

**中文**

例如，作者的社交媒体页面、“关于我”页面或个人简介页面。如果 URL 是内部个人资料页面，我们建议使用个人资料页面结构化数据来标记该作者。您可以使用 sameAs 属性作为替代方案。在消除作者歧义时，Google 可以理解 sameAs 和 url。 dateModified DateTime 最近修改文章的日期和时间，采用 ISO 8601 格式。我们建议您提供时区信息；否则，我们将默认为 Googlebot 使用的时区。如果您想向 Google 提供更准确的日期信息，请添加 dateModified 属性。

### 段落 14

**EN**

The Rich Results Test doesn't show a warning for this property, as it's only recommended if you decide that it's applicable to your site. datePublished DateTime The date and time the article was first published, in ISO 8601 format . We recommend that you provide timezone information; otherwise, we will default to the timezone used by Googlebot . Add the datePublished property if you want to provide more accurate date information to Google. The Rich Results Test doesn't show a warning for this property, as it's only recommended if you decide that it's applicable to your site. headline Text The title of the article.

**中文**

富媒体搜索结果测试不会显示此属性的警告，因为仅当您确定它适用于您的网站时才建议使用它。 datePublished DateTime 文章首次发布的日期和时间，采用 ISO 8601 格式。我们建议您提供时区信息；否则，我们将默认为 Googlebot 使用的时区。如果您想向 Google 提供更准确的日期信息，请添加 datePublished 属性。富媒体搜索结果测试不会显示此属性的警告，因为仅当您确定它适用于您的网站时才建议使用它。标题文本 文章的标题。

### 段落 15

**EN**

Consider using a concise title, as long titles may be truncated on some devices. image Repeated ImageObject or URL The URL to an image that is representative of the article. Use images that are relevant to the article, rather than logos or captions. Additional image guidelines: Image URLs must be crawlable and indexable. To check if Google can access your URLs, use the URL Inspection tool . Images must represent the marked up content. Images must be in a file format that's supported by Google Images .

**中文**

考虑使用简洁的标题，因为长标题可能在某些设备上被截断。 image 重复 ImageObject 或 URL 代表文章的图像的 URL。使用与文章相关的图像，而不是徽标或标题。其他图像准则：图像 URL 必须可抓取且可索引。要检查 Google 是否可以访问您的网址，请使用网址检查工具。图像必须代表标记的内容。图片必须采用 Google 图片 支持的文件格式。

### 段落 16

**EN**

For best results, we recommend providing multiple high-resolution images (minimum of 50K pixels when multiplying width and height) with the following aspect ratios: 16x9, 4x3, and 1x1.

**中文**

为了获得最佳效果，我们建议提供具有以下长宽比的多个高分辨率图像（宽度和高度相乘时至少为 50K 像素）：16x9、4x3 和 1x1。

### 段落 17

**EN**

For example: "image": [ "https://example.com/photos/1x1/photo.jpg", "https://example.com/photos/4x3/photo.jpg", "https://example.com/photos/16x9/photo.jpg" ] Author markup best practices To help Google best understand and represent the author of the content, we recommend following these best practices when specifying authors in markup: Best practices for author markup Include all authors in the markup Make sure that all the authors that are presented as authors on the web page are also included in markup.

**中文**

例如： "image": [ "https://example.com/photos/1x1/photo.jpg", "https://example.com/photos/4x3/photo.jpg", "https://example.com/photos/16x9/photo.jpg" ] 作者标记最佳做法 为了帮助 Google 最好GEO解和代表内容的作者，我们建议在标记中指定作者时遵循以下最佳做法： 作者标记的最佳做法 在标记中包含所有作者 确保所有在网页上显示为作者的作者也包含在标记中。

### 段落 18

**EN**

Specifying multiple authors When specifying multiple authors, list each author in their own author field: "author": [ {"name": "Willow Lane"}, {"name": "Regula Felix"} ] Don't merge multiple authors in the same author field: "author": { "name": "Willow Lane, Regula Felix" } Use additional fields To help Google better understand who the author is, we strongly recommend using the type and url (or sameAs ) properties. Use valid URLs for the url or sameAs properties.

**中文**

指定多个作者 指定多个作者时，请在各自的作者字段中列出每个作者： "author": [ {"name": "Willow Lane"}, {"name": "Regula Felix"} ] 不要在同一作者字段中合并多个作者： "author": { "name": "Willow Lane, Regula Felix" } 使用其他字段 为了帮助 Google 更好地了解作者是谁，我们强烈建议使用 type 和 url （或 sameAs ）属性。对 url 或 sameAs 属性使用有效的 URL。

### 段落 19

**EN**

For example, if the author is a person, you could link to an author's page that provides more information about the author: "author" : [ { "@type" : "Person" , "name" : "Willow Lane" , "url" : "https://www.example.com/staff/willow_lane" } ] If the author is an organization, you could link to the organization's home page. "author" : [ { "@type" : "Organization" , "name" : "Some News Agency" , "url" : "https://www.example.com/" } ] Only specify the author's name in the author.name property In the author.name property, only specify the name of the author. Don't add any other piece of information.

**中文**

例如，如果作者是个人，您可以链接到提供有关作者的更多信息的作者页面： "author" : [ { "@type" : "Person" , "name" : "Willow Lane" , "url" : "https://www.example.com/staff/willow_lane" } ] 如果作者是一个组织，您可以链接到该组织的主页。 "author" : [ { "@type" : "Organization" , "name" : "Some News Agency" , "url" : "https://www.example.com/" } ] 在author.name属性中仅指定作者姓名在author.name属性中，仅指定作者姓名。不要添加任何其他信息。

### 段落 20

**EN**

More specifically, don't add the following information: The name of the publisher. Instead, use the publisher property. The author's job title. Instead, use the appropriate property if you want to specify that information ( jobTitle ). Honorific prefix or suffix. Instead, use the appropriate property if you want to specify that information ( honorificPrefix or honorificSuffix ). Introductory words (for example, don't include words like "posted by").

**中文**

更具体地说，请勿添加以下信息： 发布者的名称。相反，请使用发布者属性。作者的职称。相反，如果您想指定该信息 ( jobTitle )，请使用适当的属性。敬语前缀或后缀。相反，如果您想指定该信息（honorificPrefix 或honorificSuffix），请使用适当的属性。介绍性词语（例如，不要包含“发布者”等词语）。

### 段落 21

**EN**

"author" : [ { "@type" : "Person" , "name" : "Echidna Jones" , "honorificPrefix" : "Dr" , "jobTitle" : "Editor in Chief" } ], "publisher" : [ { "@type" : "Organization" , "name" : "Bugs Daily" } ] } Use the appropriate Type Use the Person type for people, and the Organization type for organizations. Don't use the Thing type, and don't use the wrong type (for example, using the Organization type for a person).

**中文**

"author" : [ { "@type" : "Person" , "name" : "Echidna Jones" , "honorificPrefix" : "Dr" , "jobTitle" : "Editor in Chief" } ], "publisher" : [ { "@type" : "Organization" , "name" : "Bugs Daily" } ] } 使用适当的类型 对人员使用 Person 类型，并且组织的组织类型。不要使用事物类型，也不要使用错误的类型（例如，对人员使用组织类型）。

### 段落 22

**EN**

Here's an example that applies the author markup best practices: "author" : [ { "@type" : "Person" , "name" : "Willow Lane" , "jobTitle" : "Journalist" , "url" : "https://www.example.com/staff/willow-lane" }, { "@type" : "Person" , "name" : "Echidna Jones" , "jobTitle" : "Editor in Chief" , "url" : "https://www.example.com/staff/echidna-jones" } ], "publisher" : { "@type" : "Organization" , "name" : "The Daily Bug" , "url" : "https://www.example.com" }, // + Other fields related to the article... } Troubleshooting If you're having trouble implementing or debugging structured data, here are some resources that may help you.

**中文**

以下是应用作者标记最佳实践的示例： "author" : [ { "@type" : "Person" , "name" : "Willow Lane" , "jobTitle" : "Journalist" , "url" : "https://www.example.com/staff/willow-lane" }, { "@type" : "Person" , "name" : "Echidna Jones" , "jobTitle" : "Editor in Chief" , "url" : "https://www.example.com/staff/echidna-jones" } ], "publisher" : { "@type" : "Organization" , "name" : "The Daily Bug" , "url" : "https://www.example.com" }, // + 与文章相关的其他字段... } 疑难解答 如果您在实现或调试结构化时遇到问题数据，这里有一些可能对您有帮助的资源。

### 段落 23

**EN**

If you're using a content management system (CMS) or someone else is taking care of your site, ask them to help you. Make sure to forward any Search Console message that details the issue to them. Google does not guarantee that features that consume structured data will show up in search results. For a list of common reasons why Google may not show your content in a rich result, see the General Structured Data Guidelines . You might have an error in your structured data. Check the list of structured data errors and the Unparsable structured data report .

**中文**

如果您正在使用内容管理系统 (CMS) 或其他人正在维护您的网站，请让他们帮助您。请务必将任何详细说明问题的 Search Console 消息转发给他们。 Google 不保证使用结构化数据的功能会出现在搜索结果中。有关 Google 可能无法在富媒体搜索结果中显示您的内容的常见原因列表，请参阅通用结构化数据指南。您的结构化数据可能有错误。检查结构化数据错误列表和不可解析的结构化数据报告。

### 段落 24

**EN**

If you received a structured data manual action against your page, the structured data on the page will be ignored (although the page can still appear in Google Search results). To fix structured data issues , use the Manual Actions report . Review the guidelines again to identify if your content isn't compliant with the guidelines. The problem can be caused by either spammy content or spammy markup usage. However, the issue may not be a syntax issue, and so the Rich Results Test won't be able to identify these issues. Troubleshoot missing rich results / drop in total rich results . Allow time for re-crawling and re-indexing.

**中文**

如果您收到针对您的网页的结构化数据手动操作，则该网页上的结构化数据将被忽略（尽管该网页仍会出现在 Google 搜索结果中）。要修复结构化数据问题，请使用手动操作报告。再次查看指南以确定您的内容是否不符合指南。该问题可能是由垃圾内容或垃圾标记使用引起的。但是，该问题可能不是语法问题，因此富结果测试将无法识别这些问题。解决丰富搜索结果丢失/丰富搜索结果总数下降的问题。留出时间进行重新爬网和重新索引。

### 段落 25

**EN**

Remember that it may take several days after publishing a page for Google to find and crawl it. For general questions about crawling and indexing, check the Google Search crawling and indexing FAQ . Post a question in the Google Search Central forum . Send feedback Except as otherwise noted, the content of this page is licensed under the Creative Commons Attribution 4.0 License , and code samples are licensed under the Apache 2.0 License . For details, see the Google Developers Site Policies . Java is a registered trademark of Oracle and/or its affiliates. Last updated 2025-12-10 UTC. Need to tell us more?

**中文**

请记住，发布页面后 Google 可能需要几天时间才能找到并抓取该页面。有关抓取和索引的一般问题，请查看 Google 搜索抓取和索引常见问题解答。在 Google 搜索中心论坛中发布问题。发送反馈 除非另有说明，本页内容已根据 Creative Commons Attribution 4.0 License 获得许可，代码示例根据 Apache 2.0 License 获得许可。有关详细信息，请参阅 Google 开发者网站政策。 Java 是 Oracle 和/或其附属公司的注册商标。最后更新时间：世界标准时间 2025 年 12 月 10 日。需要告诉我们更多吗？

### 段落 26

**EN**

[[["Easy to understand","easyToUnderstand","thumb-up"],["Solved my problem","solvedMyProblem","thumb-up"],["Other","otherUp","thumb-up"]],[["Missing the information I need","missingTheInformationINeed","thumb-down"],["Too complicated / too many steps","tooComplicatedTooManySteps","thumb-down"],["Out of date","outOfDate","thumb-down"],["Samples / code issue","samplesCodeIssue","thumb-down"],["Other","otherDown","thumb-down"]],["Last updated 2025-12-10 UTC."],[],["Adding `Article` structured data to news, blog, or sports articles helps Google understand the content better.

**中文**

[[["易于理解","easyToUnderstand","thumb-up"],["解决了我的问题","solvedMyProblem","thumb-up"],["其他","otherUp","thumb-up"]],[["缺少我需要的信息","missingTheInformationINeed","thumb-down"],["太复杂/太复杂许多步骤","tooComplicatedTooManySteps","thumb-down"],["过时","outOfDate","thumb-down"],["示例/代码问题","samplesCodeIssue","thumb-down"],["其他","otherDown","thumb-down"]],["最后更新时间为 2025-12-10 UTC。"],[],["将 `Article` 结构化数据添加到新闻、博客或体育文章中有助于 Google 更好GEO解内容。

### 段落 27

**EN**

Implement `Article`, `NewsArticle`, or `BlogPosting` schema types using recommended properties like `author`, `datePublished`, `dateModified`, `headline`, and `image`. Validate your code with the Rich Results Test, deploy a few pages, and use the URL Inspection tool.

**中文**

使用建议的属性（如“author”、“datePublished”、“dateModified”、“headline”和“image”）实现“Article”、“NewsArticle”或“BlogPosting”模式类型。使用富结果测试验证您的代码，部署几个页面，并使用 URL 检查工具。

### 段落 28

**EN**

Follow all guidelines and best practices to improve your content's visibility on Google Search and associated platforms, and ensure accurate author information.\n"]] LinkedIn Join us on LinkedIn YouTube Watch our videos Blog Subscribe to our RSS feed Podcast Listen to Search Off the Record X (Twitter) Join us on X (Twitter) Get support Go to the help forum Submit a question for office hours Report spam, phishing, or malware More support resources Resources Do you need an SEO?

**中文**

遵循所有指南和最佳做法，提高您的内容在 Google 搜索和相关平台上的可见度，并确保准确的作者信息。\n"]] LinkedIn 在 LinkedIn 上加入我们 YouTube 观看我们的视频 博客 订阅我们的 RSS 源 播客 收听搜索 记录中的 X (Twitter) 在 X 上加入我们 (Twitter) 获取支持 转至帮助论坛 在办公时间提交问题 举报垃圾邮件、网络钓鱼或恶意软件 更多支持资源 资源 您需要 SEO 吗？

### 段落 29

**EN**

SEO Starter Guide Status of Search systems Search Console documentation Case Studies Tools Search Console Rich Results Test PageSpeed Insights AMP Test Android Chrome Firebase Google Cloud Platform Google AI All products Terms Privacy Manage cookies English Deutsch Español Español – América Latina Français Indonesia Italiano Polski Português – Brasil Tiếng Việt Türkçe Русский العربيّة हिंदी ภาษาไทย 中文 – 简体 中文 – 繁體 日本語 한국어

**中文**

SEO 入门指南 搜索系统状态 搜索控制台文档 案例研究 工具 搜索控制台 富结果测试 PageSpeed Insights AMP 测试 Android Chrome Firebase Google Cloud Platform Google AI 所有产品 条款 隐私 管理 cookie 英语 德语 西班牙语 法语 印度尼西亚 意大利语 波兰语 葡萄牙语 – 巴西 Tiếng Việt Türkçe Русский ????????? हिंदी ภาษาไทย 中文 – 简体中文 – 繁体日本语 한국어
