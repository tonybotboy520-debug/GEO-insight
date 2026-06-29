# Answer.AI - /llms.txt proposal

- ID: 123
- 类型: html
- 分类: 02_search_indexing_structured_data
- 主题: LLM可读内容
- 原文链接: https://www.answer.ai/posts/2024-09-03-llmstxt.html
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

/llms.txt—a proposal to provide information to help LLMs use websites – Answer.AI Answer.AI On this page Summary Background Proposal Format Other Formats CommonMark /llms.txt—a proposal to provide information to help LLMs use websites ai webdev open-source tech We propose that those interested in providing LLM-friendly content add a /llms.txt file to their site. This is a markdown file that provides brief background information and guidance, along with links to markdown files providing more detailed information. Author Jeremy Howard Published September 3, 2024 Much of this content is copied from the llms.txt proposal .

**中文**

/llms.txt - 一项提供信息以帮助 LLM 使用网站的提案 – Answer.AI Answer.AI 本页摘要背景提案格式其他格式 CommonMark /llms.txt - 一项提供信息以帮助 LLM 使用网站的提案 ai webdev 开源技术 我们建议那些有兴趣提供 LLM 友好内容的人将 /llms.txt 文件添加到其网站。这是一个 Markdown 文件，提供简要的背景信息和指导，以及提供更详细信息的 Markdown 文件的链接。作者 Jeremy Howard 发布于 2024 年 9 月 3 日 本文大部分内容是从 llms.txt 提案中复制的。

### 段落 2

**EN**

See that link for more details, examples, and tools for using llms.txt files. Summary We propose adding a /llms.txt file to websites that are designed for reading by language models, not just humans. llms.txt is a file that outlines the information that a model may want to retrieve (with links) when assembling context for LLM prompts relevant to a website. Here’s an example llms.txt file . The llms.txt file may contain both external and internal links, which are curated to be appropriate for the subject matter, and suitable for direct ingestion by LLMs.

**中文**

有关使用 llms.txt 文件的更多详细信息、示例和工具，请参阅该链接。总结 我们建议将 /llms.txt 文件添加到专为语言模型（而不仅仅是人类）阅读而设计的网站。 llms.txt 是一个文件，概述了模型在组装与网站相关的 LLM 提示的上下文时可能想要检索（带有链接）的信息。这是 llms.txt 文件的示例。 llms.txt 文件可能包含外部和内部链接，这些链接经过精心设计，适合主题，并且适合法学硕士直接摄取。

### 段落 3

**EN**

The problem this solves is that today, constructing the right context for LLMs based on a website is ambiguous — do you: Crawl the sitemap and include every page, trying to automatically format into an LLM-friendly form? Selectively include external links in addition to the sitemap? For specific domains like software documentation should you also try to include all the source code? Site authors know best, and can provide a list of content that an LLM should use. We do not prescribe exactly how you should assemble and format the context.

**中文**

这个解决的问题是，如今，基于网站为法学硕士构建正确的上下文是不明确的——您是否：抓取站点地图并包含每个页面，尝试自动格式化为法学硕士友好的形式？除了站点地图之外，还有选择地包含外部链接吗？对于软件文档等特定领域，您是否还应该尝试包含所有源代码？网站作者最了解，并且可以提供法学硕士应使用的内容列表。我们没有准确规定您应该如何组装和格式化上下文。

### 段落 4

**EN**

We’re only proposing a standard where authors can outline the most pertinent and LLM-friendly context, and tools can later assemble and format that context in a form suitable for the application. llms.txt is programmatically parseable. We also propose making an LLM-friendly version of web pages available at a URL adds an .md suffix to the regular address—for instance, here is a regular HTML docs page , along with exact same URL but with a .md extension . For an example of how these can work together, here’s a custom GPT which answers questions about Answer.AI using the information from Answer.AI’s llms.txt .

**中文**

我们只是提出一个标准，作者可以在其中概述最相关且最适合法学硕士的上下文，并且工具可以稍后以适合应用程序的形式组装和格式化该上下文。 llms.txt 可以通过编程方式进行解析。我们还建议在 URL 上提供 LLM 友好版本的网页，将 .md 后缀添加到常规地址 - 例如，这里是一个常规 HTML 文档页面，以及完全相同的 URL，但带有 .md 扩展名。有关它们如何协同工作的示例，这里有一个自定义 GPT，它使用 Answer.AI 的 llms.txt 中的信息回答有关 Answer.AI 的问题。

### 段落 5

**EN**

Background Today websites are not just used to provide information to people, but they are also used to provide information to large language models. For instance, language models are often used to enhance development environments used by coders, with many systems including an option to ingest information about programming libraries and APIs from website documentation. Providing information for language models is a little different to providing information for humans, although there is plenty of overlap. Language models generally like to have information in a more concise form.

**中文**

背景当今的网站不仅用于向人们提供信息，还用于向大型语言模型提供信息。例如，语言模型通常用于增强编码人员使用的开发环境，许多系统都包含从网站文档中获取有关编程库和 API 的信息的选项。为语言模型提供信息与为人类提供信息略有不同，尽管有很多重叠之处。语言模型通常喜欢以更简洁的形式提供信息。

### 段落 6

**EN**

This can be more similar to what a human expert would want to read. Language models can ingest a lot of information quickly, so it can be helpful to have a single place where all of the key information can be collated. Proposal llms.txt logo We propose that those interested in providing LLM-friendly content add a /llms.txt file to their site. This is a markdown file that provides brief background information and guidance, along with links to markdown files (which can also link to external sites) providing more detailed information.

**中文**

这可能更类似于人类专家想要阅读的内容。语言模型可以快速吸收大量信息，因此拥有一个可以整理所有关键信息的地方会很有帮助。提案 llms.txt 徽标 我们建议那些有兴趣提供 LLM 友好内容的人将 /llms.txt 文件添加到其网站。这是一个 Markdown 文件，提供简要的背景信息和指导，以及提供更详细信息的 Markdown 文件链接（也可以链接到外部站点）。

### 段落 7

**EN**

This can be used, for instance, in order to provide information necessary for coders to use a library, or as part of research to learn about a person or organization and so forth. You are free to use the llms.txt logo on your site to indicate your support if you wish. llms.txt markdown is human and LLM readable, but is also in a precise format allowing fixed processing methods (i.e. classical programming techniques such as parsers and regex). For instance, there is an llms-txt project providing a CLI and Python module for parsing llms.txt files and generating LLM context from them. There is also a sample JavaScript implementation.

**中文**

例如，这可以用来为编码人员提供使用图书馆所需的信息，或者作为研究的一部分来了解个人或组织等。如果您愿意，您可以在您的网站上自由使用 llms.txt 徽标来表示您的支持。 llms.txt markdown 是人类和法学硕士可读的，但也是精确的格式，允许固定的处理方法（即解析器和正则表达式等经典编程技术）。例如，有一个 llms-txt 项目提供 CLI 和 Python 模块，用于解析 llms.txt 文件并从中生成 LLM 上下文。还有一个 JavaScript 实现示例。

### 段落 8

**EN**

We furthermore propose that pages on websites that have information that might be useful for LLMs to read provide a clean markdown version of those pages at the same URL as the original page, but with .md appended. (URLs without file names should append index-commonmark.md instead.) The FastHTML project follows these two proposals for its documentation. For instance, here is the FastHTML docs llms.txt . And here is an example of a regular HTML docs page , along with exact same URL but with a .md extension .

**中文**

我们还建议网站上包含可能对 LLM 阅读有用的信息的页面提供这些页面的干净 Markdown 版本，其 URL 与原始页面相同，但附加 .md。 （没有文件名的 URL 应附加 index-commonmark.md。）FastHTML 项目的文档遵循这两个建议。例如，这里是 FastHTML 文档 llms.txt。下面是一个常规 HTML 文档页面的示例，以及完全相同的 URL，但带有 .md 扩展名。

### 段落 9

**EN**

Note that all nbdev projects now create .md versions of all pages by default, and all Answer.AI and fast.ai software projects using nbdev have had their docs regenerated with this feature—for instance, see the markdown version of fastcore’s docments module . This proposal does not include any particular recommendation for how to process the file, since it will depend on the application. For example, FastHTML automatically builds a new version of two markdown files including the contents of the linked URLs, using an XML-based structure suitable for use in LLMs such as Claude.

**中文**

请注意，所有 nbdev 项目现在默认创建所有页面的 .md 版本，并且所有使用 nbdev 的 Answer.AI 和 fast.ai 软件项目都已使用此功能重新生成了文档 - 例如，请参阅 fastcore 文档模块的 markdown 版本。该提案不包括有关如何处理文件的任何特定建议，因为这将取决于应用程序。例如，FastHTML 使用适合 Claude 等 LLM 的基于 XML 的结构，自动构建两个 Markdown 文件的新版本，包括链接 URL 的内容。

### 段落 10

**EN**

The two files are: llms-ctx.txt , which does not include the optional URLs, and llms-ctx-full.txt , which does include them. They are created using the llms_txt2ctx command line application, and the FastHTML documentation includes information for users about how to use them. llms.txt files can be used in various scenarios. For software libraries, they can provide a structured overview of documentation, making it easier for LLMs to locate specific features or usage examples. In corporate websites, they can outline organizational structure and key information sources.

**中文**

这两个文件是： llms-ctx.txt （不包含可选 URL）和 llms-ctx-full.txt （包含可选 URL）。它们是使用 llms_txt2ctx 命令行应用程序创建的，FastHTML 文档包含有关用户如何使用它们的信息。 llms.txt 文件可用于各种场景。对于软件库，它们可以提供结构化的文档概述，使法学硕士更容易找到特定功能或使用示例。在企业网站中，他们可以概述组织结构和关键信息来源。

### 段落 11

**EN**

Information about new legislation and necessary background and context could be curated in an llms.txt file to help stakeholders understand it. llms.txt files can be adapted for various domains. Personal portfolio or CV websites could use them to help answer questions about an individual. In e-commerce, they could outline product categories and policies. Educational institutions might use them to summarize course offerings and resources. Format At the moment the most widely and easily understood format for language models is Markdown. Simply showing where key Markdown files can be found is a great first step.

**中文**

有关新立法以及必要的背景和背景的信息可以在 llms.txt 文件中整理，以帮助利益相关者理解它。 llms.txt 文件可以适用于各种域。个人作品集或简历网站可以使用它们来帮助回答有关个人的问题。在电子商务中，他们可以概述产品类别和政策。教育机构可能会使用它们来总结课程设置和资源。格式 目前最广泛、最容易理解的语言模型格式是 Markdown。简单地显示关键 Markdown 文件的位置是很好的第一步。

### 段落 12

**EN**

Providing some basic structure helps a language model to find where the information it needs can come from. The llms.txt file is unusual in that it uses Markdown to structure the information rather than a classic structured format such as XML. The reason for this is that we expect many of these files to be read by language models and agents. Having said that, the information in llms.txt follows a specific format and can be read using standard programmatic-based tools. The llms.txt file spec is for files located in the root path /llms.txt of a website (or, optionally, in a subpath).

**中文**

提供一些基本结构有助于语言模型找到其所需信息的来源。 llms.txt 文件的不同寻常之处在于它使用 Markdown 来构建信息，而不是使用 XML 等经典的结构化格式。原因是我们期望语言模型和代理能够读取其中许多文件。尽管如此，llms.txt 中的信息遵循特定的格式，可以使用标准的基于编程的工具读取。 llms.txt 文件规范适用于位于网站根路径 /llms.txt 中（或者可选地位于子路径中）的文件。

### 段落 13

**EN**

A file following the spec contains the following sections as markdown, in the specific order: An H1 with the name of the project or site. This is the only required section A blockquote with a short summary of the project, containing key information necessary for understanding the rest of the file Zero or more markdown sections (e.g.

**中文**

遵循规范的文件包含以下降价部分，按特定顺序： 带有项目或站点名称的 H1。这是唯一必需的部分带有项目简短摘要的块引用，包含理解文件其余部分所需的关键信息零个或多个降价部分（例如

### 段落 14

**EN**

paragraphs, lists, etc) of any type except headings, containing more detailed information about the project and how to interpret the provided files Zero or more markdown sections delimited by H2 headers, containing “file lists” of URLs where further detail is available Each “file list” is a markdown list, containing a required markdown hyperlink [name](url) , then optionally a : and notes about the file.

**中文**

除标题之外的任何类型的段落、列表等），包含有关项目的更多详细信息以及如何解释所提供的文件 零个或多个由 H2 标头分隔的 Markdown 部分，包含可提供更多详细信息的 URL 的“文件列表” 每个“文件列表”是一个 Markdown 列表，包含所需的 Markdown 超链接 [name](url)，然后可选地包含一个 : 和有关文件的注释。

### 段落 15

**EN**

Here is a mock example: # Title > Optional description goes here Optional details go here ## Section name - [ Link title ](https://link_url) : Optional link details ## Optional - [ Link title ](https://link_url) Note that the “Optional” section has a special meaning—if it’s included, the URLs provided there can be skipped if a shorter context is needed. Use it for secondary information which can often be skipped. To create effective llms.txt files, consider these guidelines: Use concise, clear language. When linking to resources, include brief, informative descriptions. Avoid ambiguous terms or unexplained jargon.

**中文**

下面是一个模拟示例： # Title > 可选描述在此处 可选详细信息在此处 ## 部分名称 - [ 链接标题 ](https://link_url) : 可选链接详细信息 ## 可选 - [ 链接标题 ](https://link_url) 请注意，“可选”部分具有特殊含义 - 如果包含该部分，则如果需要较短的上下文，则可以跳过其中提供的 URL。将其用于通常可以跳过的次要信息。要创建有效的 llms.txt 文件，请考虑以下准则： 使用简洁、清晰的语言。链接到资源时，请包含简短且内容丰富的描述。避免模​​棱两可的术语或无法解释的行话。

### 段落 16

**EN**

Run a tool that expands your llms.txt file into an LLM context file and test a number of language models to see if they can answer questions about your content.

**中文**

运行一个工具，将您的 llms.txt 文件扩展为 LLM 上下文文件，并测试多种语言模型，看看它们是否可以回答有关您的内容的问题。
