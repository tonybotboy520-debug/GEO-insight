# llms.txt - The /llms.txt file

- ID: 122
- 类型: html
- 分类: 02_search_indexing_structured_data
- 主题: LLM可读内容
- 原文链接: https://llmstxt.org/
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

The /llms.txt file – llms-txt llms-txt The /llms.txt file The /llms.txt file Code Python module & CLI Python source JavaScript Editors and IDEs ed , the standard text editor Tutorials llms.txt in Different Domains How to help LLMs understand your nbdev project On this page Background Proposal Format Existing standards Example Directories Integrations Next steps Report an issue Other Formats CommonMark The /llms.txt file A proposal to standardise on using an /llms.txt file to provide information to help LLMs use a website at inference time.

**中文**

/llms.txt 文件 – llms-txt llms-txt /llms.txt 文件 /llms.txt 文件 代码 Python 模块和 CLI Python 源代码 JavaScript 编辑器和 IDE ed，标准文本编辑器 教程 不同领域中的 llms.txt 如何帮助 LLM 理解您的 nbdev 项目 本页 背景 提案格式 现有标准 示例目录 集成 后续步骤 报告问题 其他格式 CommonMark /llms.txt 文件 标准化提案使用 /llms.txt 文件提供信息以帮助 LLM 在推理时使用网站。

### 段落 2

**EN**

Author Jeremy Howard Published September 3, 2024 Background Large language models increasingly rely on website information, but face a critical limitation: context windows are too small to handle most websites in their entirety. Converting complex HTML pages with navigation, ads, and JavaScript into LLM-friendly plain text is both difficult and imprecise. While websites serve both human readers and LLMs, the latter benefit from more concise, expert-level information gathered in a single, accessible location.

**中文**

作者 Jeremy Howard 发表于 2024 年 9 月 3 日 背景 大型语言模型越来越依赖网站信息，但面临着一个关键的限制：上下文窗口太小，无法完整处理大多数网站。将包含导航、广告和 JavaScript 的复杂 HTML 页面转换为 LLM 友好的纯文本既困难又不精确。虽然网站同时为人类读者和法学硕士提供服务，但后者受益于在单个可访问位置收集的更简洁的专家级信息。

### 段落 3

**EN**

This is particularly important for use cases like development environments, where LLMs need quick access to programming documentation and APIs. Proposal llms.txt logo We propose adding a /llms.txt markdown file to websites to provide LLM-friendly content. This file offers brief background information, guidance, and links to detailed markdown files. llms.txt markdown is human and LLM readable, but is also in a precise format allowing fixed processing methods (i.e. classical programming techniques such as parsers and regex).

**中文**

这对于开发环境等用例尤其重要，在这些用例中，法学硕士需要快速访问编程文档和 API。提案 llms.txt 徽标 我们建议向网站添加 /llms.txt markdown 文件以提供 LLM 友好的内容。此文件提供简短的背景信息、指导以及详细 Markdown 文件的链接。 llms.txt markdown 是人类和法学硕士可读的，但也是精确的格式，允许固定的处理方法（即解析器和正则表达式等经典编程技术）。

### 段落 4

**EN**

We furthermore propose that pages on websites that have information that might be useful for LLMs to read provide a clean markdown version of those pages at the same URL as the original page, but with .md appended. (URLs without file names should append index.html.md instead.) The FastHTML project follows these two proposals for its documentation. For instance, here is the FastHTML docs llms.txt . And here is an example of a regular HTML docs page , along with exact same URL but with a .md extension . This proposal does not include any particular recommendation for how to process the llms.txt file, since it will depend on the application.

**中文**

我们还建议网站上包含可能对 LLM 阅读有用的信息的页面提供这些页面的干净 Markdown 版本，其 URL 与原始页面相同，但附加 .md。 （没有文件名的 URL 应附加 index.html.md。）FastHTML 项目的文档遵循这两个建议。例如，这里是 FastHTML 文档 llms.txt。下面是一个常规 HTML 文档页面的示例，以及完全相同的 URL，但带有 .md 扩展名。该提案不包括有关如何处理 llms.txt 文件的任何特定建议，因为它将取决于应用程序。

### 段落 5

**EN**

For example, the FastHTML project opted to automatically expand the llms.txt to two markdown files with the contents of the linked URLs, using an XML-based structure suitable for use in LLMs such as Claude. The two files are: llms-ctx.txt , which does not include the optional URLs, and llms-ctx-full.txt , which does include them. They are created using the llms_txt2ctx command line application, and the FastHTML documentation includes information for users about how to use them.

**中文**

例如，FastHTML 项目选择使用适合 Claude 等 LLM 的基于 XML 的结构，自动将 llms.txt 扩展为两个包含链接 URL 内容的 Markdown 文件。这两个文件是： llms-ctx.txt （不包含可选 URL）和 llms-ctx-full.txt （包含可选 URL）。它们是使用 llms_txt2ctx 命令行应用程序创建的，FastHTML 文档包含有关用户如何使用它们的信息。

### 段落 6

**EN**

The versatility of llms.txt files means they can serve many purposes - from helping developers find their way around software documentation, to giving businesses a way to outline their structure, or even breaking down complex legislation for stakeholders. They’re just as useful for personal websites where they can help answer questions about someone’s CV, for e-commerce sites to explain products and policies, or for schools and universities to provide quick access to their course information and resources. Note that all nbdev projects now create .md versions of all pages by default.

**中文**

llms.txt 文件的多功能性意味着它们可以用于多种用途 - 从帮助开发人员找到软件文档的方法，到为企业提供概述其结构的方法，甚至为利益相关者打破复杂的立法。它们对于个人网站同样有用，可以帮助回答有关某人简历的问题；对于电子商务网站来说，它们可以解释产品和政策；对于学校和大学来说，它们也可以提供对其课程信息和资源的快速访问。请注意，所有 nbdev 项目现在默认创建所有页面的 .md 版本。

### 段落 7

**EN**

All Answer.AI and fast.ai software projects using nbdev have had their docs regenerated with this feature. For an example, see the markdown version of fastcore’s docments module . Format At the moment the most widely and easily understood format for language models is Markdown. Simply showing where key Markdown files can be found is a great first step. Providing some basic structure helps a language model to find where the information it needs can come from. The llms.txt file is unusual in that it uses Markdown to structure the information rather than a classic structured format such as XML.

**中文**

所有使用 nbdev 的 Answer.AI 和 fast.ai 软件项目都已使用此功能重新生成了文档。有关示例，请参阅 fastcore 文档模块的 markdown 版本。格式 目前最广泛、最容易理解的语言模型格式是 Markdown。简单地显示关键 Markdown 文件的位置是很好的第一步。提供一些基本结构有助于语言模型找到其所需信息的来源。 llms.txt 文件的不同寻常之处在于它使用 Markdown 来构建信息，而不是使用 XML 等经典的结构化格式。

### 段落 8

**EN**

The reason for this is that we expect many of these files to be read by language models and agents. Having said that, the information in llms.txt follows a specific format and can be read using standard programmatic-based tools. The llms.txt file spec is for files located in the root path /llms.txt of a website (or, optionally, in a subpath). A file following the spec contains the following sections as markdown, in the specific order: An optional byte-order mark (BOM) An H1 with the name of the project or site.

**中文**

原因是我们期望语言模型和代理能够读取其中许多文件。尽管如此，llms.txt 中的信息遵循特定的格式，可以使用标准的基于编程的工具读取。 llms.txt 文件规范适用于位于网站根路径 /llms.txt 中（或者可选地位于子路径中）的文件。遵循规范的文件包含以下部分作为降价，按特定顺序： 可选的字节顺序标记 (BOM) 带有项目或站点名称的 H1。

### 段落 9

**EN**

This is the only required section A blockquote with a short summary of the project, containing key information necessary for understanding the rest of the file Zero or more markdown sections (e.g. paragraphs, lists, etc) of any type except headings, containing more detailed information about the project and how to interpret the provided files Zero or more markdown sections delimited by H2 headers, containing “file lists” of URLs where further detail is available Each “file list” is a markdown list, containing a required markdown hyperlink [name](url) , then optionally a : and notes about the file.

**中文**

这是唯一必需的部分 带有项目简短摘要的块引用，包含理解文件其余部分所需的关键信息 除标题之外的任何类型的零个或多个 Markdown 部分（例如段落、列表等），包含有关项目以及如何解释提供的文件的更多详细信息 零个或多个由 H2 标头分隔的 Markdown 部分，包含可用的 URL 的“文件列表” 每个“文件列表”是一个 Markdown 列表，包含所需的 Markdown 超链接[name](url)，然后是可选的 : 和有关文件的注释。

### 段落 10

**EN**

Here is a mock example: # Title > Optional description goes here Optional details go here ## Section name - [ Link title ](https://link_url) : Optional link details ## Optional - [ Link title ](https://link_url) Note that the “Optional” section has a special meaning—if it’s included, the URLs provided there can be skipped if a shorter context is needed. Use it for secondary information which can often be skipped. Existing standards llms.txt is designed to coexist with current web standards. While sitemaps list all pages for search engines, llms.txt offers a curated overview for LLMs.

**中文**

下面是一个模拟示例： # Title > 可选描述在此处 可选详细信息在此处 ## 部分名称 - [ 链接标题 ](https://link_url) : 可选链接详细信息 ## 可选 - [ 链接标题 ](https://link_url) 请注意，“可选”部分具有特殊含义 - 如果包含该部分，则如果需要较短的上下文，则可以跳过其中提供的 URL。将其用于通常可以跳过的次要信息。现有标准 llms.txt 旨在与当前 Web 标准共存。站点地图列出了搜索引擎的所有页面，而 llms.txt 则为法学硕士提供了精心策划的概述。

### 段落 11

**EN**

It can complement robots.txt by providing context for allowed content. The file can also reference structured data markup used on the site, helping LLMs understand how to interpret this information in context. The approach of standardising on a path for the file follows the approach of /robots.txt and /sitemap.xml . robots.txt and llms.txt have different purposes—robots.txt is generally used to let automated tools know what access to a site is considered acceptable, such as for search indexing bots.

**中文**

它可以通过提供允许内容的上下文来补充 robots.txt。该文件还可以引用网站上使用的结构化数据标记，帮助法学硕士了解如何在上下文中解释此信息。标准化文件路径的方法遵循 /robots.txt 和 /sitemap.xml 的方法。 robots.txt 和 llms.txt 具有不同的用途 - robots.txt 通常用于让自动化工具知道对站点的哪些访问被认为是可接受的，例如搜索索引机器人。

### 段落 12

**EN**

On the other hand, llms.txt information will often be used on demand when a user explicitly requests information about a topic, such as when including a coding library’s documentation in a project, or when asking a chat bot with search functionality for information. Our expectation is that llms.txt will mainly be useful for inference , i.e. at the time a user is seeking assistance, as opposed to for training . However, perhaps if llms.txt usage becomes widespread, future training runs could take advantage of the information in llms.txt files too. sitemap.xml is a list of all the indexable human-readable information available on a site.

**中文**

另一方面，当用户明确请求有关某个主题的信息时，例如在项目中包含编码库的文档时，或者向具有搜索功能的聊天机器人询问信息时，通常会按需使用 llms.txt 信息。我们的期望是 llms.txt 主要用于推理，即在用户寻求帮助时，而不是用于训练。然而，也许如果 llms.txt 的使用变得广泛，未来的训练运行也可以利用 llms.txt 文件中的信息。 sitemap.xml 是站点上所有可用的可索引人类可读信息的列表。

### 段落 13

**EN**

This isn’t a substitute for llms.txt since it: Often won’t have the LLM-readable versions of pages listed Doesn’t include URLs to external sites, even though they might be helpful to understand the information Will generally cover documents that in aggregate will be too large to fit in an LLM context window, and will include a lot of information that isn’t necessary to understand the site.

**中文**

这不能替代 llms.txt，因为它： 通常不会列出 LLM 可读版本的页面 不包含外部站点的 URL，即使它们可能有助于理解信息 通常会涵盖总体而言太大而无法放入 LLM 上下文窗口的文档，并且将包含许多理解站点不需要的信息。

### 段落 14

**EN**

Example Here’s an example of llms.txt , in this case a cut down version of the file used for the FastHTML project (see also the full version ): # FastHTML > FastHTML is a python library which brings together Starlette, Uvicorn, HTMX, and fastcore's `FT` "FastTags" into a library for creating server-rendered hypermedia applications. Important notes: - Although parts of its API are inspired by FastAPI, it is *not* compatible with FastAPI syntax and is not targeted at creating API services - FastHTML is compatible with JS-native web components and any vanilla JS library, but not with React, Vue, or Svelte.

**中文**

示例 下面是 llms.txt 的示例，在本例中是用于 FastHTML 项目的文件的缩减版本（另请参阅完整版本）： # FastHTML > FastHTML 是一个 Python 库，它将 Starlette、Uvicorn、HTMX 和 fastcore 的 `FT`“FastTags”汇集到一个库中，用于创建服务器渲染的超媒体应用程序。重要提示： - 尽管其部分 API 受到 FastAPI 的启发，但它与 FastAPI 语法“不”兼容，并且不以创建 API 服务为目标 - FastHTML 与 JS 原生 Web 组件和任何普通 JS 库兼容，但与 React、Vue 或 Svelte 不兼容。

### 段落 15

**EN**

## Docs - [ FastHTML quick start ](https://fastht.ml/docs/tutorials/quickstart_for_web_devs.html.md) : A brief overview of many FastHTML features - [ HTMX reference ](https://github.com/bigskysoftware/htmx/blob/master/www/content/reference.md) : Brief description of all HTMX attributes, CSS classes, headers, events, extensions, js lib methods, and config options ## Examples - [ Todo list application ](https://github.com/AnswerDotAI/fasthtml/blob/main/examples/adv_app.py) : Detailed walk-thru of a complete CRUD app in FastHTML showing idiomatic use of FastHTML and HTMX patterns.

**中文**

## 文档 - [ FastHTML 快速入门 ](https://fastht.ml/docs/tutorials/quickstart_for_web_devs.html.md) : 许多 FastHTML 功能的简要概述 - [ HTMX 参考 ](https://github.com/bigskysoftware/htmx/blob/master/www/content/reference.md) : 所有 HTMX 属性、CSS 类、标头、事件、扩展、js 的简要描述lib 方法和配置选项 ## 示例 - [待办事项列表应用程序](https://github.com/AnswerDotAI/fasthtml/blob/main/examples/adv_app.py)：FastHTML 中完整 CRUD 应用程序的详细演练，显示 FastHTML 和 HTMX 模式的惯用用法。

### 段落 16

**EN**

## Optional - [ Starlette full documentation ](https://gist.githubusercontent.com/jph00/809e4a4808d4510be0e3dc9565e9cbd3/raw/9b717589ca44cedc8aaf00b2b8cacef922964c0f/starlette-sml.md) : A subset of the Starlette documentation useful for FastHTML development. To create effective llms.txt files, consider these guidelines: Use concise, clear language. When linking to resources, include brief, informative descriptions. Avoid ambiguous terms or unexplained jargon. Run a tool that expands your llms.txt file into an LLM context file and test a number of language models to see if they can answer questions about your content.

**中文**

## 可选 - [ Starlette 完整文档 ](https://gist.githubusercontent.com/jph00/809e4a4808d4510be0e3dc9565e9cbd3/raw/9b717589ca44cedc8aaf00b2b8cacef922964c0f/starlette-sml.md)：Starlette 文档的子集，可用于快速 HTML 开发。要创建有效的 llms.txt 文件，请考虑以下准则： 使用简洁、清晰的语言。链接到资源时，请包含简短且内容丰富的描述。避免模​​棱两可的术语或无法解释的行话。运行一个工具，将您的 llms.txt 文件扩展为 LLM 上下文文件，并测试多种语言模型，看看它们是否可以回答有关您的内容的问题。

### 段落 17

**EN**

Directories Here are a few directories that list the llms.txt files available on the web: llmstxt.site directory.llmstxt.cloud Integrations Various tools and plugins are available to help integrate the llms.txt specification into your workflow: llms_txt2ctx - CLI and Python module for parsing llms.txt files and generating LLM context JavaScript Implementation - Sample JavaScript implementation vitepress-plugin-llms - VitePress plugin that automatically generates LLM-friendly documentation for the website following the llms.txt specification docusaurus-plugin-llms - Docusaurus plugin for generating LLM-friendly documentation following the llmt

**中文**

目录 以下是一些列出了网络上可用的 llms.txt 文件的目录： llmstxt.site directory.llmstxt.cloud 集成 可以使用各种工具和插件来帮助将 llms.txt 规范集成到您的工作流程中： llms_txt2ctx - 用于解析 llms.txt 文件并生成 LLM 上下文的 CLI 和 Python 模块 JavaScript 实现 - 示例 JavaScript 实现 vitepress-plugin-llms - VitePress 插件，可为以下网站自动生成 LLM 友好的文档llms.txt 规范 docusaurus-plugin-llms - Docusaurus 插件，用于按照 llmt 生成 LLM 友好的文档

### 段落 18

**EN**

xt.org standard Drupal LLM Support - A Drupal Recipe providing full support for the llms.txt proposal on any Drupal 10.3+ site llms-txt-php - A library for writing and reading llms.txt Markdown files VS Code PagePilot Extension - PagePilot is a VS Code Chat participant that automatically loads external context (documentation, APIs, README files) to provide enhanced responses.

**中文**

xt.org 标准 Drupal LLM 支持 - Drupal Recipe，为任何 Drupal 10.3+ 站点上的 llms.txt 提案提供全面支持 llms-txt-php - 用于编写和读取 llms.txt Markdown 文件的库 VS Code PagePilot 扩展 - PagePilot 是 VS Code 聊天参与者，可自动加载外部上下文（文档、API、自述文件）以提供增强的响应。

### 段落 19

**EN**

Next steps The llms.txt specification is open for community input. A GitHub repository hosts this informal overview , allowing for version control and public discussion. A community discord channel is available for sharing implementation experiences and discussing best practices. Report an issue

**中文**

后续步骤 llms.txt 规范开放供社区输入。 GitHub 存储库托管此非正式概述，允许版本控制和公共讨论。社区不和谐频道可用于分享实施经验和讨论最佳实践。报告问题
