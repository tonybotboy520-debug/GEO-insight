# Cloudflare Blog - The crawl-to-click gap

- ID: 128
- 类型: html
- 分类: 05_tools_monitoring
- 主题: 生态/监测数据
- 原文链接: https://blog.cloudflare.com/crawlers-click-ai-bots-training/
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

The crawl-to-click gap: Cloudflare data on AI bots, training, and referrals Get Started Free | Contact Sales The Cloudflare Blog Subscribe to receive notifications of new posts: Subscribe AI Developers Radar Product News Security Policy & Legal Zero Trust Speed & Reliability Life at Cloudflare Partners AI Developers Radar Product News Security Policy & Legal Zero Trust Speed & Reliability Life at Cloudflare Partners The crawl-to-click gap: Cloudflare data on AI bots, training, and referrals 2025-08-29 João Tomé 9 min read In 2025, Generative AI is reshaping how people and companies use the Internet.

**中文**

抓取到点击的差距：有关 AI 机器人、培训和推荐的 Cloudflare 数据 免费开始 |联系销售人员 Cloudflare 博客 订阅以接收新帖子通知： 订阅 AI 开发人员雷达产品新闻 安全政策和法律 零信任速度和可靠性 Cloudflare 合作伙伴的生活 AI 开发人员雷达产品新闻 安全政策和法律 零信任速度和可靠性 Cloudflare 合作伙伴的生活 抓取到点击的差距：有关 AI 机器人、培训和推荐的 Cloudflare 数据 2025 年 8 月 29 日 João Tomé 阅读 9 分钟 2025 年，生成式人工智能正在重塑人们和公司使用互联网的方式。

### 段落 2

**EN**

Search engines once drove traffic to content creators through links. Now, AI training crawlers — the engines behind commonly-used LLMs — are consuming vast amounts of web data, while sending far fewer users back. We covered this shift, along with related trends and Cloudflare features (like pay per crawl) in early July. Studies from Pew Research Center ( 1 , 2 ) and Authoritas already point to AI overviews — Google’s new AI-generated summaries shown at the top of search results — contributing to sharp declines in news website traffic.

**中文**

搜索引擎曾经通过链接为内容创建者带来流量。现在，人工智能训练爬虫——常用法学硕士背后的引擎——正在消耗大量的网络数据，而返回的用户却少得多。我们在 7 月初介绍了这一转变以及相关趋势和 Cloudflare 功能（例如按抓取付费）。皮尤研究中心 (1, 2) 和 Authoritas 的研究已经指出人工智能概述（谷歌新的人工智能生成的摘要显示在搜索结果顶部）导致新闻网站流量急剧下降。

### 段落 3

**EN**

For a news site, this means lots of bot hits, but far fewer real readers clicking through — which in turn means fewer people clicking on ads or chances to convert to subscriptions. Cloudflare's data shows the same pattern. Crawling by search engines and AI services surged in the first half of 2025 — up 24% year-over-year in June — before slowing to just 4% year-over-year growth in July. How is the space evolving? Which crawling purposes are most common, and how is that changing? Spoiler: training-related crawling is leading the way.

**中文**

对于新闻网站来说，这意味着大量的机器人点击，但真正点击的读者却少得多，这反过来意味着点击广告或转换为订阅的机会更少。 Cloudflare 的数据显示了相同的模式。 2025 年上半年，搜索引擎和人工智能服务的抓取量激增，6 月份同比增长 24%，7 月份同比增速放缓至仅 4%。空间如何演变？哪些爬行目的最常见？这种情况有何变化？剧透：与训练相关的爬行处于领先地位。

### 段落 4

**EN**

In this post, we track AI and search bot crawl activity, what purposes dominate, and which platforms contribute the least referral traffic back to creators. Key takeaways Training crawling grows: Training now drives nearly 80% of AI bot activity, up from 72% a year ago. Publisher referrals drop: Google referrals to news sites fell, with March 2025 down ~9% compared to January. AI & search crawling increase: Crawling rose 32% year-over-year in April 2025, before slowing to 4% year-over-year growth in July.

**中文**

在这篇文章中，我们跟踪人工智能和搜索机器人爬行活动，主要目的是什么，以及哪些平台为创作者贡献了最少的推荐流量。要点 训练爬行增长：训练现在驱动了近 80% 的 AI 机器人活动，高于一年前的 72%。发布商推荐量下降：Google 对新闻网站的推荐量下降，2025 年 3 月与 1 月相比下降了约 9%。人工智能和搜索爬行增长：2025 年 4 月爬行同比增长 32%，7 月份同比增长放缓至 4%。

### 段落 5

**EN**

AI-only crawler shifts: OpenAI’s GPTBot more than doubled in share of AI crawling traffic (4.7% to 11.7%), Anthropic’s ClaudeBot rose (6% to ~10%), while ByteDance’s Bytespider fell from 14.1% to 2.4%. Crawl-to-refer imbalance (how many pages a bot crawls per page that a user clicks back to): Anthropic increased referrals but still leads with 38,000 crawls per visitor in July (down from 286,000:1 in January). Perplexity decreased referrals in 2025 — with more crawling but fewer referrals at 194 crawls per visitor in July.

**中文**

仅AI爬虫的转变：OpenAI的GPTBot在AI爬虫流量中的份额增长了一倍多（4.7％至11.7％），Anthropic的ClaudeBot上涨（6％至10％），而字节跳动的Bytespider从14.1％下降至2.4％。抓取引用不平衡（机器人抓取用户点击返回的每个页面的页面数）：Anthropic 增加了引用，但 7 月份每位访问者的抓取次数仍然领先，为 38,000 次（低于 1 月份的 286,000:1）。 2025 年，Perplexity 的推荐量有所下降——爬行次数增多，但推荐次数减少，7 月份每位访问者的爬行次数为 194 次。

### 段落 6

**EN**

Several of the trends in this blog use Cloudflare Radar’s new AI Insights features, explained in more detail in the post: “ A deeper look at AI crawlers: breaking down traffic by purpose and industry .” Google referrals fall as AI Overviews expand Referral traffic from search is already shifting, as we noted above and as studies have shown. In our dataset of news-related customers (spanning the Americas, Europe, and Asia), Google’s referrals have been clearly declining since February 2025.

**中文**

本博客中的一些趋势使用了 Cloudflare Radar 的新 AI Insights 功能，在帖子中进行了更详细的解释：“深入了解 AI 爬虫：按用途和行业细分流量。”随着人工智能概述的扩展，谷歌推荐量下降 正如我们上面指出的和研究表明的那样，来自搜索的推荐流量已经发生了变化。在我们的新闻相关客户数据集中（横跨美洲、欧洲和亚洲），自 2025 年 2 月以来，Google 的推荐量一直在明显下降。

### 段落 7

**EN**

This drop is unusual, since overall Internet traffic (and referrals as well) historically has only dipped during July and August — the summer months when the Northern Hemisphere is largely on break from school or work. The sharpest and least seasonal decline came in March. Despite being a 31-day month, March had almost the same referral volume as the shorter, 28-day February. Looking at longer comparisons: March 2025 referral traffic from Google was 9% lower than January, the same drop seen in June. April was worse, down 15% compared with January. This drop seems to coincide with some of Google’s changes. AI Overviews launched in the U.S.

**中文**

这种下降是不寻常的，因为从历史上看，总体互联网流量（以及推荐量）仅在七月和八月（北半球大部分在夏季放假或放假）期间下降。最剧烈且季节性最小的下降出现在三月份。尽管 3 月份只有 31 天，但其推荐量与较短的 28 天的 2 月份几乎相同。进行更长期的比较：2025 年 3 月，来自 Google 的推荐流量比 1 月下降了 9%，与 6 月的降幅相同。 4 月份情况更糟，比 1 月份下降了 15%。这一下降似乎与谷歌的一些变化相吻合。 AI 概述在美国推出

### 段落 8

**EN**

in May 2024 , but in March 2025, Google upgraded AI Overviews with Gemini 2.0, introduced AI Mode in Labs, and expanded Overviews to more European countries. By May 2025, AI Mode rolled out broadly in the U.S. with Gemini 2.5, adding conversational search, Deep Search, and personalized recommendations. The search-to-news site pipeline seems to be weakening, replaced in part by AI-driven results. Looking at a daily perspective, we can also spot a clear U.S.-election-related peak in referrals from Google to the cohort of known news sites on November 5–6, 2024.

**中文**

2024年5月，但2025年3月，谷歌用Gemini 2.0升级了AI Overviews，在Labs中引入了AI模式，并将Overviews扩展到更多欧洲国家。到 2025 年 5 月，AI 模式随 Gemini 2.5 在美国广泛推出，增加了对话式搜索、深度搜索和个性化推荐。从搜索到新闻网站的渠道似乎正在减弱，部分被人工智能驱动的结果所取代。从每日角度来看，我们还可以发现 2024 年 11 月 5 日至 6 日期间，谷歌向已知新闻网站群体的推荐量出现了明显的美国大选相关峰值。

### 段落 9

**EN**

AI and search crawling: spring surge (+24%), summer slowdown In June , we talked about search and AI crawler growth, and our picture of the trend is now more complete with more data. To focus only on AI and search crawlers, and to remove the bias of customer growth, we analyzed a fixed set of customers from specific weeks, a method we’ve also used in the Cloudflare Radar Year in Review . What the data shows: crawling spiked twice: first in November 2024, then again between March and April 2025. April 2025 alone was up 32% compared with May 2024, the first full month where we have comparable data. After that surge, growth stabilized.

**中文**

人工智能和搜索爬行：春季激增（+24%），夏季放缓 6 月份，我们讨论了搜索和人工智能爬行器的增长，现在我们通过更多数据对趋势进行了更完整的了解。为了仅关注人工智能和搜索爬虫，并消除客户增长的偏差，我们分析了特定周内的一组固定客户，我们也在 Cloudflare Radar 年度回顾中使用了这种方法。数据显示：抓取次数激增两次：第一次是在 2024 年 11 月，第二次是在 2025 年 3 月至 4 月之间。仅 2025 年 4 月就比 2024 年 5 月（我们拥有可比数据的第一个完整月份）增长了 32%。在那次激增之后，增长趋于稳定。

### 段落 10

**EN**

In June 2025, crawling traffic was still 24% higher year-over-year, but by July the increase was down to just 4%. That shift highlights how quickly crawler activity can accelerate and then cool down. As the chart below shows, crawling traffic rose sharply in March and April. It remained high but slightly lower in May, before starting to drop in June.

**中文**

2025 年 6 月，爬行流量仍同比增长 24%，但到 7 月增幅已降至仅 4%。这种转变凸显了爬虫活动加速然后冷却的速度有多快。如下图所示，3、4月份爬行流量大幅上升。 5 月份仍处于高位，但略有下降，6 月份开始下降。

### 段落 11

**EN**

The seasonal dip is similar to what we see in overall Internet traffic during the Northern Hemisphere’s summer months (August and September are often the quietest), though in the case of crawlers, this is likely due to reduced overall web activity rather than bots themselves taking a “break.” Historically, activity tends to rise again in November — as it did in 2024 for AI and search bot traffic — when people spend more time online for shopping and seasonal habits (a pattern we’ve seen in past years ).

**中文**

这种季节性下降与我们在北半球夏季的总体互联网流量中看到的情况类似（八月和九月通常是最安静的），尽管就爬虫而言，这可能是由于总体网络活动减少，而不是机器人本身“休息”。从历史上看，11 月的活动往往会再次上升——就像 2024 年人工智能和搜索机器人流量一样——当人们花更多时间上网购物和季节性习惯时（我们在过去几年看到的模式）。

### 段落 12

**EN**

Googlebot is still the anchor, accounting for 39% of all AI and search crawler traffic, but the fastest growth now comes from AI-specific crawlers, though bots related to Amazon and ByteDance (Bytespider) have lost significant ground. GPTBot’s share grew from 4.7% in July 2024 to 11.7% in July 2025. ClaudeBot also increased, from 6% to nearly 10%, while Meta’s crawler jumped from 0.9% to 7.5%. By contrast, Amazonbot dropped from 10.2% to 5.9%, and ByteDance’s Bytespider dropped from 14.1% to just 2.4%.

**中文**

Googlebot 仍然是主力，占所有 AI 和搜索爬虫流量的 39%，但现在增长最快的增长来自于 AI 专用爬虫，尽管与亚马逊和字节跳动 (Bytespider) 相关的机器人已经失去了显着的市场份额。 GPTBot 的份额从 2024 年 7 月的 4.7% 增长到 2025 年 7 月的 11.7%。ClaudeBot 也有所增长，从 6% 增长到近 10%，而 Meta 的爬虫则从 0.9% 跃升至 7.5%。相比之下，亚马逊bot从10.2%下降到5.9%，字节跳动的Bytespider从14.1%下降到仅2.4%。

### 段落 13

**EN**

The table below shows how market shares have shifted between July 2024 and July 2025: Bot name % share July 2024 % share July 2025 Δ percentage-point change 1 Googlebot 37.5 39 1.5 2 GPTBot 4.7 11.7 7 3 ClaudeBot 6 9.9 3.9 4 Bingbot 8.7 9.3 0.6 5 Meta-ExternalAgent 0.9 7.5 6.5 6 Amazonbot 10.2 5.9 -4.3 7 Googlebot-Image 4.1 3.3 -0.8 8 Yandex 5 2.9 -2.1 9 GoogleOther 4.6 2.7 -1.8 10 Bytespider 14.1 2.4 -11.6 11 Applebot 1.8 1.5 -0.3 12 ChatGPT-User 0.1 0.9 0.9 13 OAI-SearchBot 0 0.9 0.9 14 Baiduspider 0.5 0.5 0 15 Googlebot-Mobile 0.2 0.4 0.2 AI-only crawlers: OpenAI rises, ByteDance falls Looking only at AI bot traffic (as tracked on our Radar AI page ), the trend is clear.

**中文**

下表显示了 2024 年 7 月至 2025 年 7 月期间市场份额的变化情况： 机器人名称 % 份额 2024 年 7 月 % 份额 2025 年 7 月 Δ 百分点变化 1 Googlebot 37.5 39 1.5 2 GPTBot 4.7 11.7 7 3 ClaudeBot 6 9.9 3.9 4 Bingbot 8.7 9.3 0.6 5 元外部代理 0.9 7.5 6.5 6 Amazonbot 10.2 5.9 -4.3 7 Googlebot-Image 4.1 3.3 -0.8 8 Yandex 5 2.9 -2.1 9 Google其他 4.6 2.7 -1.8 10 Bytespider 14.1 2.4 -11.6 11 Applebot 1.8 1.5 -0.3 12 ChatGPT-User 0.1 0.9 0.9 13 OAI-SearchBot 0 0.9 0.9 14 Baispider 0.5 0.5 0 15 Googlebot-Mobile 0.2 0.4 0.2 仅人工智能爬虫：OpenAI 上升，字节跳动下降趋势很明显。

### 段落 14

**EN**

Since January 2025, GPTBot has steadily increased its crawling volume, driven mainly by training-related activity. ClaudeBot crawling accelerated in June, while Amazonbot and Bytespider activity slowed. The chart below shows how GPTBot surged over the past 12 months, overtaking Amazonbot and Bytespider, which both fell sharply: A comparison between July 2024 and July 2025 makes the shift even more obvious. GPTBot gained 16 percentage points, Meta’s crawler rose by more than 15, and ClaudeBot grew by 8. On the shrinking side, Amazonbot dropped 12 percentage points and Bytespider dropped over 31 percentage points.

**中文**

自 2025 年 1 月以来，GPTBot 的爬行量稳步增加，主要由培训相关活动推动。 ClaudeBot 爬行在 6 月份加速，而 Amazonbot 和 Bytespider 活动放缓。下图显示了 GPTBot 在过去 12 个月中的飙升，超过了均大幅下跌的 Amazonbot 和 Bytespider：2024 年 7 月和 2025 年 7 月的比较使这种转变更加明显。 GPTBot 增长了 16 个百分点，Meta 的爬虫增长了超过 15 个百分点，ClaudeBot 增长了 8 个百分点。在萎缩方面，Amazonbot 下降了 12 个百分点，Bytespider 下降了超过 31 个百分点。

### 段落 15

**EN**

AI-only bots July 2024 % July 2025 % Δ percentage-point change 1 GPTBot 11.9 28.1 16.1 2 ClaudeBot 15 23.3 8.3 3 Meta-ExternalAgent 2.4 17.7 15.3 4 Amazonbot 26.4 14.1 -12.3 5 Bytespider 37.3 5.8 -31.5 6 Applebot 4.9 3.7 -1.2 7 ChatGPT-User 0.2 2.4 2.2 8 OAI-SearchBot 0 2.2 2.2 9 TikTokSpider 0 0.7 0.7 10 imgproxy 0 0.7 0.7 11 PerplexityBot 0 0.4 0.4 12 Google-CloudVertexBot 0 0.3 0.3 13 AI2Bot 0 0.2 0.2 14 Timpibot 0.6 0.1 -0.5 15 CCBot 0.1 0.1 0 We covered the functionality of these bots in our June blog post . Crawling by purpose: training dominates Training is the clear leader.

**中文**

纯人工智能机器人 2024 年 7 月 % 2025 年 7 月 % Δ 百分点变化 1 GPTBot 11.9 28.1 16.1 2 ClaudeBot 15 23.3 8.3 3 Meta-ExternalAgent 2.4 17.7 15.3 4 Amazonbot 26.4 14.1 -12.3 5 Bytespider 37.3 5.8 -31.5 6 Applebot 4.9 3.7 -1.2 7 ChatGPT-User 0.2 2.4 2.2 8 OAI-SearchBot 0 2.2 2.2 9 TikTokSpider 0 0.7 0.7 10 imgproxy 0 0.7 0.7 11 PerplexityBot 0 0.4 0.4 12 Google-CloudVertexBot 0 0.3 0.3 13 AI2Bot 0 0.2 0.2 14 Timpibot 0.6 0.1 -0.5 15 CCBot 0.1 0.1 0 我们在 6 月份的博客文章中介绍了这些机器人的功能。按目的爬行：培训占主导地位 培训是明显的领导者。

### 段落 16

**EN**

(We classify purpose based on operator disclosures and industry sources, a method we explained in this AI Week blog .) Over the past 12 months, 80% of AI crawling was for training, compared with 18% for search and just 2% for user actions. In the last six months, the share for training rose further to 82%, while search dropped to 15% and user actions increased slightly to 3%. The chart below shows how training-related crawling steadily grew over the past year, far outpacing other purposes: The year-over-year comparison reinforces this trend. In July 2024, training accounted for 72% of AI crawling. By July 2025, it had risen to 79%.

**中文**

（我们根据运营商披露和行业来源对目的进行分类，我们在本次《AI Week》博客中解释了这种方法。）在过去 12 个月中，80% 的 AI 爬行用于训练，而 18% 用于搜索，只有 2% 用于用户操作。在过去六个月中，培训的份额进一步上升至 82%，而搜索则下降至 15%，用户操作略有上升至 3%。下图显示了与训练相关的爬行在过去一年中如何稳步增长，远远超过其他目的：逐年比较强化了这一趋势。 2024年7月，训练占AI爬行的72%。到2025年7月，这一比例已上升至79%。

### 段落 17

**EN**

Over the same period, search fell from 26% to 17%, while user actions grew modestly from 2% to 3.2%. Crawl-to-refer ratios shifts: tens of thousands of bot crawls per human click The crawl-to-refer ratio measures how many pages a platform crawls compared with how often it drives users to a website. In practice, a high ratio means heavy crawling but little referral traffic. For example, for every visitor Anthropic refers back to a website, its crawlers have already visited tens of thousands of pages. Why does this metric matter? It highlights the imbalance between how much content AI systems consume and how little traffic they return.

**中文**

同一时期，搜索量从 26% 下降至 17%，而用户操作量则从 2% 适度增长至 3.2%。抓取引用比率发生变化：每次人类点击数以万计的机器人抓取抓取引用比率衡量的是平台抓取的页面数量与其吸引用户访问网站的频率。在实践中，高比率意味着大量爬行但很少有推荐流量。例如，对于每个访问者 Anthropic 引用一个网站，其爬虫已经访问了数万个页面。为什么这个指标很重要？它凸显了人工智能系统消耗的内容量与返回的流量量之间的不平衡。

### 段落 18

**EN**

For publishers, it can feel like giving away the raw material for free. With that in mind, here’s how different platforms compare from January to July 2025. Anthropic remains the most crawl-heavy platform. Even after an 87% decline this year, it still crawled 38,000 pages for every referred page visit in July 2025 — the highest imbalance among major AI players. Referrals may be improving, though, after Anthropic added web search to Claude in March 2025 (initially for U.S. paid users) and expanded it globally by May to all users, including the free tier .

**中文**

对于出版商来说，这感觉就像免费赠送原材料。考虑到这一点，以下是从 2025 年 1 月到 7 月不同平台的比较。Anthropic 仍然是爬行最繁重的平台。即使今年下降了 87%，2025 年 7 月，每次引用的页面访问它仍然爬行了 38,000 个页面，这是主要 AI 参与者中最不平衡的。不过，在 Anthropic 于 2025 年 3 月为 Claude 添加网络搜索（最初针对美国付费用户）并于 5 月将其扩展到全球所有用户（包括免费用户）之后，推荐量可能正在改善。

### 段落 19

**EN**

The feature introduced direct citations with clickable URLs, creating new referral pathways.

**中文**

该功能引入了带有可点击 URL 的直接引用，从而创建了新的推荐途径。

### 段落 20

**EN**

The full dataset is below, showing January–July 2025 ratios by platform ordered by the highest ratio average: (Note: a rising ratio means more bot crawling per human click sent back, while a falling ratio means less bot crawling per human click sent back) Crawl-to-refer ratio (from Cloudflare Radar’s data ) Service Jan Feb Mar Apr May Jun Jul Average % Change Jan-Jul Anthropic 286,930.1 271,748.2 121,612.7 130,330.2 114,313 71,282.8 38,065.7 147,754.7 -86.7% OpenAI 1,217.4 1,774.5 2,217 1200 995.6 1,655.9 1,091.4 1,437.8 -10.4% Perplexity 54.6 55.3 201.3 300.9 199.1 200.6 194.8 172.4 256.7% Microsoft 38.5 44.2 42.3 43.3 45.1 42 40.7 42.3 5.7%

**中文**

完整数据集如下，显示按最高比率平均值排序的 2025 年 1 月至 7 月各平台的比率：（注：比率上升意味着发回的每次人类点击的机器人爬行次数增多，而比率下降则意味着发回的每次人类点击的机器人爬行次数减少） 爬行引用比率（来自 Cloudflare Radar 的数据） 服务 Jan 二月 三月 四月 五月 六月 七月 平均百分比变化 一月至七月 人类 286,930.1 271,748.2 121,612.7 130,330.2 114,313 71,282.8 38,065.7 147,754.7 -86.7% OpenAI 1,217.4 1,774.5 2,217 1200 995.6 1,655.9 1,091.4 1,437.8 -10.4% 困惑度 54.6 55.3 201.3 300.9 199.1 200.6 194.8 172.4 256.7% 微软 38.5 44.2 42.3 43.3 45.1 42 40.7 42.3 5.7%

### 段落 21

**EN**

Yandex 15.5 13.1 13.1 15.7 14.7 15.9 21.4 15.6 38.3% Google 3.8 6.3 14.6 22.5 16.7 13.1 5.4 11.8 43% ByteDance 18 16.4 3.5 2.3 1.6 1.6 0.9 6.3 -95% Baidu 0.6 0.7 0.8 1.5 1.2 1 0.9 1 44.5% DuckDuckGo 0.1 0.2 0.2 0.2 0.3 0.3 0.3 0.2 116.3% Looking at the changes from January to July 2025: Anthropic recorded the steepest decrease in bot to human traffic, down 86.7% .

**中文**

Yandex 15.5 13.1 13.1 15.7 14.7 15.9 21.4 15.6 38.3% 谷歌 3.8 6.3 14.6 22.5 16.7 13.1 5.4 11.8 43% 字节跳动 18 16.4 3.5 2.3 1.6 1.6 0.9 6.3 -95% 百度 0.6 0.7 0.8 1.5 1.2 1 0.9 1 44.5% DuckDuckGo 0.1 0.2 0.2 0.2 0.3 0.3 0.3 0.2 116.3% 从 2025 年 1 月到 7 月的变化来看：Anthropic 的跌幅最大机器人对人类的流量下降了 86.7%。

### 段落 22

**EN**

From 286,930 bots per human in January, to 38,065 bots per human in July, the change shows a dramatic increase in referrals. Despite the change, it remains by far the most crawl-heavy platform, with tens of thousands of pages still crawled for every referral. Perplexity moved in the opposite direction, with bot crawling increasing +256.7% relative to human visitors; climbing from 54 bots per human in January to 195 bots per human in July. While the ratio is still far below Anthropic, the increase shows it is crawling more heavily, relative to the traffic it refers, than it did earlier.

**中文**

从 1 月份的人均 286,930 个机器人增加到 7 月份的人均 38,065 个机器人，这一变化表明推荐量急剧增加。尽管发生了变化，它仍然是迄今为止爬行最繁重的平台，每次推荐仍会爬行数万个页面。困惑度向相反方向发展，机器人爬行相对于人类访问者增加了 256.7%；从 1 月份的每人 54 个机器人上升到 7 月份的每人 195 个机器人。虽然该比率仍远低于 Anthropic，但这一增长表明，相对于其所引用的流量，其爬行速度比之前更加严重。

### 段落 23

**EN**

OpenAI ratio dropped slightly, from 1,217 bots per human in January to 1,091 in July (-10%). The shift is smaller than Anthropic’s but suggests OpenAI is sending a bit more referral traffic relative to its crawling. Microsoft stayed steady, with its ratio moving only slightly, from 38.5 bots per human in January to 40.7 in July (+6%). This consistency suggests stable behavior from Bing-linked services. Yandex increased from 15.5 bots per human in January to 21.4 in July (+38%). The overall ratio is far smaller than Anthropic’s or Perplexity’s, but it shows Yandex is crawling more heavily relative to the traffic it sends back.

**中文**

OpenAI 比率略有下降，从 1 月份的人均 1,217 个机器人减少到 7 月份的 1,091 个（-10%）。这一变化比 Anthropic 的变化要小，但表明 OpenAI 发送的推荐流量相对于其爬行而言要多一些。微软保持稳定，其比率仅略有变化，从 1 月份的人均 38.5 个机器人增加到 7 月份的 40.7 个（+6%）。这种一致性表明 Bing 链接服务的行为稳定。 Yandex 从 1 月份的每人 15.5 个机器人增加到 7 月份的 21.4 个（+38%）。总体比率远小于 Anthropic 或 Perplexity 的比率，但它表明 Yandex 的爬行相对于其发回的流量而言更为严重。

### 段落 24

**EN**

Alongside measuring crawling volumes and referral traffic (now also visible on the AI Insights page of Cloudflare Radar ), it’s worth looking at whether AI operators follow good practices when deploying their bots. Cloudflare data shows that most leading AI crawlers are on our verified bots list, meaning their IP addresses match published ranges and they respect robots.txt. But adoption of newer standards like WebBotAuth — which uses cryptographic signatures in HTTP messages to confirm a request comes from a specific bot, and is especially relevant today — is still missing.

**中文**

除了测量爬行量和推荐流量（现在也可以在 Cloudflare Radar 的 AI Insights 页面上看到）之外，值得关注的是 AI 操作员在部署机器人时是否遵循良好实践。 Cloudflare 数据显示，大多数领先的 AI 爬虫都在我们经过验证的机器人列表中，这意味着它们的 IP 地址与发布的范围匹配，并且它们尊重 robots.txt。但像 WebBotAuth 这样的新标准的采用仍然缺失，该标准使用 HTTP 消息中的加密签名来确认请求来自特定的机器人，并且在今天尤其重要。

### 段落 25

**EN**

Meta, OpenAI, and Anthropic run distinct bots for different purposes, while Google and Microsoft rely on unified crawlers. Anthropic, however, still lags in verification, which makes it easier for bad actors to spoof its crawler and ignore robots.txt. Without verification, it’s difficult to distinguish real from fake traffic — leaving its compliance effectively unclear. (A longer list of AI bots is available here ). Conclusion and what’s next If training-related crawling continues to dominate while referrals stay flat, creators face a paradox: feeding AI systems without gaining traffic in return.

**中文**

Meta、OpenAI 和 Anthropic 出于不同目的运行不同的机器人，而 Google 和 Microsoft 则依赖统一的爬虫。然而，Anthropic 在验证方面仍然滞后，这使得不良行为者更容易欺骗其爬虫并忽略 robots.txt。如果没有验证，就很难区分真实流量和虚假流量，从而导致其合规性实际上不明确。 （此处提供了更长的人工智能机器人列表）。结论和下一步如果与训练相关的爬行继续占据主导地位，而推荐量却持平，那么创作者将面临一个悖论：为人工智能系统提供数据，却没有获得流量回报。

### 段落 26

**EN**

Many want their content to appear in chatbot answers, but without monetization or cooperation, the incentive to produce quality work declines. The Web now stands at a fork in the road. Either a new balance emerges — one where the new AI era helps sustain publishers and creators — or AI turns the open web into a one-way training set, extracting value with little flowing back. You can learn more about some of these data trends on Cloudflare Radar’s updated AI Insights page .

**中文**

许多人希望他们的内容出现在聊天机器人的答案中，但如果没有货币化或合作，创作高质量作品的动力就会下降。网络现在正站在岔路口。要么出现一种新的平衡——新的人工智能时代有助于维持出版商和创作者的生存——要么人工智能将开放网络变成一个单向训练集，在几乎没有回流的情况下提取价值。您可以在 Cloudflare Radar 更新的 AI Insights 页面上了解有关其中一些数据趋势的更多信息。

### 段落 27

**EN**

AI Week AI Radar Internet Trends Traffic Bots Follow on X João Tomé | @emot Cloudflare | @cloudflare Related posts June 19, 2026 Temporary Cloudflare Accounts for AI agents The moment an agent needs to deploy something, it slams face-first into a wall built for humans. Today we're rolling out Temporary Accounts on Cloudflare Workers. Any agent can now run wrangler deploy — temporary and get a live Worker in seconds. ...

**中文**

人工智能周 人工智能雷达 互联网趋势 交通机器人跟随 X João Tomé | @emot Cloudflare | @cloudflare 相关帖子 2026 年 6 月 19 日 AI 代理的临时 Cloudflare 帐户 当代理需要部署某些东西时，它会正面撞向为人类建造的墙壁。今天，我们在 Cloudflare Workers 上推出临时账户。现在，任何代理都可以运行临时牧马人部署，并在几秒钟内获得实时工作人员。 ...

### 段落 28

**EN**

By Sid Chatterjee , Celso Martinho , Brendan Irvine-Broque Agents , Wrangler , AI , Cloudflare Workers June 18, 2026 Build your own vulnerability harness We break down the technical architecture behind our multi-stage vulnerability discovery harness and automated triage loop. Learn how we manage state controls, squash false positives through adversarial review, and route around LLM context limits. ...

**中文**

作者：Sid Chatterjee、Celso Martinho、Brendan Irvine-Broque Agents、Wrangler、AI、Cloudflare Workers 2026 年 6 月 18 日 构建您自己的漏洞工具 我们详细介绍了多阶段漏洞发现工具和自动分类循环背后的技术架构。了解我们如何管理状态控制、通过对抗性审查消除误报以及绕过法学硕士背景限制。 ...

### 段落 29

**EN**

By Dan Jones , Alexandra Godoi , Grant Bourzikas Security , AI , Engineering , Research , Vulnerabilities June 17, 2026 Bringing more agent harnesses and frameworks to Cloudflare, starting with Flue The Agents SDK is now a runtime any agent framework can build on. Today we're opening up the Agents SDK primitives, with Flue as a first framework targeting Agents SDK, and rolling out agents in the dashboard. ...

**中文**

作者：Dan Jones、Alexandra Godoi、Grant Bourzikas 安全、人工智能、工程、研究、漏洞 2026 年 6 月 17 日 从 Flue 开始，将更多代理工具和框架引入 Cloudflare Agents SDK 现在是任何代理框架都可以构建的运行时。今天，我们开放 Agents SDK 原语，以 Flue 作为第一个针对 Agents SDK 的框架，并在仪表板中推出代理。 ...

### 段落 30

**EN**

By Thomas Gauvin AI , Cloudflare Workers , Developers , Developer Platform , Durable Objects , SDK , MCP June 15, 2026 Growing the Cloudflare AI team with talent from Ensemble AI Cloudflare is deepening our investment in AI with the addition of team members from Ensemble AI, focusing on machine learning infrastructure and efficiency. ...

**中文**

作者：Thomas Gauvin AI、Cloudflare Workers、开发人员、开发人员平台、Durable Objects、SDK、MCP 2026 年 6 月 15 日 利用来自 Ensemble AI 的人才壮大 Cloudflare AI 团队 Cloudflare 正在深化我们对 AI 的投资，增加了来自 Ensemble AI 的团队成员，重点关注机器学习基础设施和效率。 ...

### 段落 31

**EN**

By Alex Reneau , Zach Albertson , Michelle Chen Workers AI , AI Getting Started Free plans For enterprises Compare plans Get a recommendation Request a demo Contact Sales Resources Learning Center Analyst reports Cloudflare Radar Cloudflare TV Case Studies Webinars White Papers Developer docs theNet Solutions Connectivity cloud SSE and SASE services Application services Network services Developer services Community Community Hub Project Galileo Athenian Project Cloudflare for Campaigns Connect 2024 Support Help center Cloudflare Status Compliance GDPR Trust & Safety Company About Cloudflare Our team Investor relations Press Careers Diversity, equity & inclusion Impact/ESG Network Map Logos & press kit Become a partner © 2026 Cloudflare, Inc.

**中文**

作者：Alex Reneau、Zach Albertson、Michelle Chen 工人 AI、AI 入门 免费计划 针对企业 比较计划 获取推荐 请求演示 联系销售资源 学习中心 分析师报告 Cloudflare Radar Cloudflare TV 案例研究 网络研讨会 白皮书 开发人员文档 theNet 解决方案 连接云 SSE 和 SASE 服务 应用程序服务 网络服务 开发人员服务 社区 社区中心 项目 Galileo Athenian 项目 Cloudflare for Campaigns Connect 2024 支持 帮助中心 Cloudflare 状态 合规性 GDPR 信任与安全 公司 关于 Cloudflare 我们的团队 投资者关系 媒体 职业生涯 多元化、公平和包容性 影响/ESG 网络地图 徽标和新闻资料袋 成为合作伙伴 © 2026 Cloudflare, Inc.

### 段落 32

**EN**

| Privacy Policy | Terms of Use | Report Security Issues | Cookie Preferences | Trademark

**中文**

|隐私政策 |使用条款 |报告安全问题 | Cookie 偏好 |商标
