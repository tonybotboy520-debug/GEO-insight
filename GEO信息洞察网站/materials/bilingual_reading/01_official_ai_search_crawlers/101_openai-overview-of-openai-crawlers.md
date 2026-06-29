# OpenAI - Overview of OpenAI Crawlers

- ID: 101
- 类型: html
- 分类: 01_official_ai_search_crawlers
- 主题: 官方机制/爬虫
- 原文链接: https://developers.openai.com/api/docs/bots
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

OpenAI uses web crawlers (“robots”) and user agents to perform actions for its products, either automatically or triggered by user request. OpenAI uses OAI-SearchBot and GPTBot robots.txt tags to enable webmasters to manage how their sites and content work with AI. Each setting is independent of the others – for example, a webmaster can allow OAI-SearchBot in order to appear in search results while disallowing GPTBot to indicate that crawled content should not be used for training OpenAI’s generative AI foundation models.

**中文**

OpenAI 使用网络爬虫（“机器人”）和用户代理自动或由用户请求触发为其产品执行操作。 OpenAI 使用 OAI-SearchBot 和 GPTBot robots.txt 标签，使网站管理员能够管理其网站和内容如何与 AI 配合使用。每个设置都独立于其他设置 - 例如，网站管理员可以允许 OAI-SearchBot 出现在搜索结果中，同时禁止 GPTBot 来指示爬取的内容不应用于训练 OpenAI 的生成式 AI 基础模型。

### 段落 2

**EN**

If your site has allowed both bots, we may use the results from just one crawl for both use cases to avoid duplicative crawling. For search results, please note it can take ~24 hours from a site’s robots.txt update for our systems to adjust. User agent Description & details OAI-SearchBot OAI-SearchBot is for search. OAI-SearchBot is used to surface websites in search results in ChatGPT’s search features. Sites that are opted out of OAI-SearchBot will not be shown in ChatGPT search answers, though can still appear as navigational links.

**中文**

如果您的网站允许这两种机器人，我们可能会将一次抓取的结果用于这两种用例，以避免重复抓取。对于搜索结果，请注意，网站的 robots.txt 更新后，我们的系统可能需要大约 24 小时才能进行调整。用户代理 描述和详细信息 OAI-SearchBot OAI-SearchBot 用于搜索。 OAI-SearchBot 用于在 ChatGPT 搜索功能的搜索结果中显示网站。选择退出 OAI-SearchBot 的网站将不会显示在 ChatGPT 搜索答案中，但仍可以显示为导航链接。

### 段落 3

**EN**

To help ensure your site appears in search results, we recommend allowing OAI-SearchBot in your site’s robots.txt file and allowing requests from our published IP ranges below. Full user-agent string: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36; compatible; OAI-SearchBot/1.3; +https://openai.com/searchbot Published IP addresses: https://openai.com/searchbot.json OAI-AdsBot OAI-AdsBot is used to validate the safety of web pages submitted as ads on ChatGPT. When you submit an ad, OpenAI may visit the landing page to ensure it complies with our policies.

**中文**

为了帮助确保您的网站出现在搜索结果中，我们建议在您网站的 robots.txt 文件中允许 OAI-SearchBot，并允许来自我们在下面发布的 IP 范围的请求。完整的用户代理字符串：Mozilla/5.0（Macintosh；Intel Mac OS X 10_15_7）AppleWebKit/537.36（KHTML，如 Gecko）Chrome/131.0.0.0 Safari/537.36；兼容的; OAI-SearchBot/1.3； +https://openai.com/searchbot 发布的 IP 地址：https://openai.com/searchbot.json OAI-AdsBot OAI-AdsBot 用于验证在 ChatGPT 上作为广告提交的网页的安全性。当您提交广告时，OpenAI 可能会访问登陆页面以确保其符合我们的政策。

### 段落 4

**EN**

We may also use content from the landing page to determine when it’s most relevant to show the ad to users. OAI-AdsBot only visits pages submitted as ads, and the data collected by OAI-AdsBot is not used to train generative AI foundation models. Full user-agent string: Mozilla/5.0 AppleWebKit/537.36 (KHTML, like Gecko); compatible; OAI-AdsBot/1.0; +https://openai.com/adsbot Published IP addresses: https://openai.com/adsbot.json GPTBot GPTBot is used to make our generative AI foundation models more useful and safe. It is used to crawl content that may be used in training our generative AI foundation models.

**中文**

我们还可能使用着陆页中的内容来确定何时向用户展示广告最相关。 OAI-AdsBot 仅访问作为广告提交的页面，OAI-AdsBot 收集的数据不会用于训练生成式 AI 基础模型。完整的用户代理字符串：Mozilla/5.0 AppleWebKit/537.36（KHTML，如 Gecko）；兼容的; OAI-AdsBot/1.0； +https://openai.com/adsbot 已发布的 IP 地址：https://openai.com/adsbot.json GPTBot GPTBot 用于使我们的生成式 AI 基础模型更加有用和安全。它用于抓取可用于训练我们的生成式人工智能基础模型的内容。

### 段落 5

**EN**

Disallowing GPTBot indicates a site’s content should not be used in training generative AI foundation models. Full user-agent string: Mozilla/5.0 AppleWebKit/537.36 (KHTML, like Gecko); compatible; GPTBot/1.3; +https://openai.com/gptbot Published IP addresses: https://openai.com/gptbot.json ChatGPT-User OpenAI also uses ChatGPT-User for certain user actions in ChatGPT and Custom GPTs . When users ask ChatGPT or a CustomGPT a question, it may visit a web page with a ChatGPT-User agent. ChatGPT users may also interact with external applications via GPT Actions . ChatGPT-User is not used for crawling the web in an automatic fashion.

**中文**

禁止 GPTBot 表示网站的内容不应用于训练生成式 AI 基础模型。完整的用户代理字符串：Mozilla/5.0 AppleWebKit/537.36（KHTML，如 Gecko）；兼容的; GPTBot/1.3； +https://openai.com/gptbot 已发布的 IP 地址：https://openai.com/gptbot.json ChatGPT-User OpenAI 还使用 ChatGPT-User 在 ChatGPT 和自定义 GPT 中执行某些用户操作。当用户向 ChatGPT 或 CustomGPT 询问问题时，它可能会访问带有 ChatGPT 用户代理的网页。 ChatGPT 用户还可以通过 GPT 操作与外部应用程序交互。 ChatGPT-User 不用于以自动方式抓取网络。

### 段落 6

**EN**

Because these actions are initiated by a user, robots.txt rules may not apply. ChatGPT-User is not used to determine whether content may appear in Search. Please use OAI-SearchBot in robots.txt for managing Search opt outs and automatic crawl. Full user-agent string: Mozilla/5.0 AppleWebKit/537.36 (KHTML, like Gecko); compatible; ChatGPT-User/1.0; +https://openai.com/bot Published IP addresses: https://openai.com/chatgpt-user.json Ask AI Docs agent Loading docs agent...

**中文**

由于这些操作是由用户发起的，robots.txt 规则可能不适用。 ChatGPT-User 不用于确定内容是否可以出现在搜索中。请使用 robots.txt 中的 OAI-SearchBot 来管理搜索退出和自动抓取。完整的用户代理字符串：Mozilla/5.0 AppleWebKit/537.36（KHTML，如 Gecko）；兼容的; ChatGPT-用户/1.0； +https://openai.com/bot 已发布的 IP 地址：https://openai.com/chatgpt-user.json 询问 AI Docs 代理 正在加载文档代理...
