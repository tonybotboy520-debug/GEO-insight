# Google Search Central - Organization structured data

- ID: 114
- 类型: html
- 分类: 02_search_indexing_structured_data
- 主题: 结构化数据
- 原文链接: https://developers.google.com/search/docs/appearance/structured-data/organization
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

organization structured data to your home page can help Google better understand your organization's administrative details and disambiguate your organization in search results. Some properties are used behind the scenes to disambiguate your organization from other organizations (like iso6523 and naics ), while others can influence visual elements in Search results (such as which logo is shown in Search results and your knowledge panel ). If you're a merchant, you can influence more details in your merchant knowledge panel and brand profile , such as return policy, address, and contact information.

**中文**

将组织结构化数据添加到您的主页可以帮助 Google 更好地了解您组织的管理详细信息，并在搜索结果中消除您组织的歧义。某些属性在幕后用于消除您的组织与其他组织的歧义（例如 iso6523 和 naics ），而其他属性则可以影响搜索结果中的视觉元素（例如在搜索结果和您的知识面板中显示哪个徽标）。如果您是商家，您可以影响商家知识面板和品牌简介中的更多详细信息，例如退货政策、地址和联系信息。

### 段落 2

**EN**

There are no required properties; instead, we recommend adding as many properties that are relevant to your organization. How to add structured data Structured data is a standardized format for providing information about a page and classifying the page content. If you're new to structured data, you can learn more about how structured data works . Here's an overview of how to build, test, and release structured data. Add as many recommended properties that apply to your web page. There are no required properties; instead, add the properties that apply to your content.

**中文**

没有必需的属性；相反，我们建议添加尽可能多的与您的组织相关的属性。如何添加结构化数据 结构化数据是一种标准化格式，用于提供有关页面的信息并对页面内容进行分类。如果您不熟悉结构化数据，可以详细了解结构化数据的工作原理。以下概述了如何构建、测试和发布结构化数据。添加尽可能多的适用于您的网页的推荐属性。没有必需的属性；相反，添加适用于您的内容的属性。

### 段落 3

**EN**

Based on the format you're using, learn where to insert structured data on the page . Using a CMS? It may be easier to use a plugin that's integrated into your CMS. Using JavaScript? Learn how to generate structured data with JavaScript . Follow the guidelines . Validate your code using the Rich Results Test and fix any critical errors. Consider also fixing any non-critical issues that may be flagged in the tool, as they can help improve the quality of your structured data (however, this isn't necessary to be eligible for rich results).

**中文**

根据您使用的格式，了解在页面上的何处插入结构化数据。使用内容管理系统？使用集成到 CMS 中的插件可能会更容易。使用 JavaScript？了解如何使用 JavaScript 生成结构化数据。遵循指导方针。使用丰富的结果测试验证您的代码并修复任何严重错误。还应考虑修复工具中可能标记的任何非关键问题，因为它们可以帮助提高结构化数据的质量（但是，这并不是获得丰富结果的必要条件）。

### 段落 4

**EN**

Deploy a few pages that include your structured data and use the URL Inspection tool to test how Google sees the page. Be sure that your page is accessible to Google and not blocked by a robots.txt file, the noindex tag, or login requirements. If the page looks okay, you can ask Google to recrawl your URLs . Note : Allow time for re-crawling and re-indexing. Remember that it may take several days after publishing a page for Google to find and crawl it. To keep Google informed of future changes, we recommend that you submit a sitemap . You can automate this with the Search Console Sitemap API .

**中文**

部署一些包含结构化数据的页面，并使用 URL 检查工具来测试 Google 如何查看该页面。确保 Google 可以访问您的网页，并且不会被 robots.txt 文件、noindex 标记或登录要求阻止。如果页面看起来没问题，您可以要求 Google 重新抓取您的网址。注意：留出时间进行重新爬网和重新索引。请记住，发布页面后 Google 可能需要几天时间才能找到并抓取该页面。为了让 Google 了解未来的变化，我们建议您提交站点地图。您可以使用 Search Console Sitemap API 自动执行此操作。

### 段落 5

**EN**

Examples Organization Here's an example of organization information in JSON-LD code.

**中文**

示例组织 以下是 JSON-LD 代码中的组织信息示例。

### 段落 6

**EN**

<html> <head> <title>About Us</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "Organization", "url": "https://www.example.com", "sameAs": ["https://example.net/profile/example1234", "https://example.org/example1234"], "logo": "https://www.example.com/images/logo.png", "name": "Example Corporation", "description": "The example corporation is well-known for producing high-quality widgets", "email": "contact@example.com", "telephone": "+47-99-999-9999", "address": { "@type": "PostalAddress", "streetAddress": "Rue Improbable 99", "addressLocality": "Paris", "addressCountry": "FR", "addressRegion": "Ile-de-

**中文**

<html> <head> <title>关于我们</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "组织", "url": "https://www.example.com", "sameAs": ["https://example.net/profile/example1234", "https://example.org/example1234"], "logo": "https://www.example.com/images/logo.png", "name": "示例公司", "description": "示例公司因生产高质量小部件而闻名", "电子邮件": "contact@example.com", "电话": "+47-99-999-9999", "地址": { "@type": "PostalAddress", "streetAddress": "Rue Improbable 99", "addressLocality": "巴黎", "addressCountry": "FR", "addressRegion": "Ile-de-

### 段落 7

**EN**

France", "postalCode": "75001" }, "vatID": "FR12345678901", "iso6523Code": "0199:724500PMK2A2M1SQQ228" } </script> </head> <body> </body> </html> <html> <head> <title>About Us</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "Organization", "url": "https://www.example.com", "sameAs": ["https://example.net/profile/example1234", "https://example.org/example1234"], "logo": "https://www.example.com/images/logo.png", "name": "Example Corporation", "description": "The example corporation is well-known for producing high-quality widgets", "email": "contact@example.com", "telephone": "+47-99-999-9999", "address

**中文**

法国", "postalCode": "75001" }, "vatID": "FR12345678901", "iso6523Code": "0199:724500PMK2A2M1SQQ228" } </script> </head> <body> </body> </html> <html> <head> <title>关于我们</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "组织", "url": "https://www.example.com", "sameAs": ["https://example.net/profile/example1234", "https://example.org/example1234"], "logo": "https://www.example.com/images/logo.png", "name": "示例Corporation", "description": "示例公司因生产高质量小部件而闻名", "电子邮件": "contact@example.com", "电话": "+47-99-999-9999", "地址

### 段落 8

**EN**

": { "@type": "PostalAddress", "streetAddress": "Rue Improbable 99", "addressLocality": "Paris", "addressCountry": "FR", "addressRegion": "Ile-de-France", "postalCode": "75001" }, "vatID": "FR12345678901", "iso6523Code": "0199:724500PMK2A2M1SQQ228" } </script> </head> <body> </body> </html> OnlineStore (subtype of Organization ) with a shipping policy and return policy Here's an example of an online store with both a shipping policy and a return policy in JSON-LD code.

**中文**

": { "@type": "PostalAddress", "streetAddress": "Rue Improbable 99", "addressLocality": "巴黎", "addressCountry": "FR", "addressRegion": "法兰西岛", "postalCode": "75001" }, "vatID": "FR12345678901", "iso6523Code": "0199:724500PMK2A2M1SQQ228" } </script> </head> <body> </body> </html> OnlineStore（Organization 的子类型），具有送货政策和退货政策 下面是一个在线商店的示例，其中包含 JSON-LD 代码中的送货政策和退货政策。

### 段落 9

**EN**

Refer to the separate Merchant return policy markup documentation for more examples and detailed information for merchant-level standard return policies.

**中文**

有关商家级标准退货政策的更多示例和详细信息，请参阅单独的商家退货政策标记文档。

### 段落 10

**EN**

<html> <head> <title>About Us</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "OnlineStore", "name": "Example Online Store", "url": "https://www.example.com", "sameAs": [ "https://example.net/profile/example12", "https://example.org/@example34" ], "logo": "https://www.example.com/assets/images/logo.png", "contactPoint": { "contactType": "Customer Service", "email": "support@example.com", "telephone": "+47-99-999-9900" }, "vatID": "FR12345678901", "iso6523Code": "0199:724500PMK2A2M1SQQ228", "hasShippingService": [ { "@type": "ShippingService", "name": "shipping to CH and FR", "description": "Shipping to

**中文**

<html> <head> <title>关于我们</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "OnlineStore", "name": "示例在线商店", "url": "https://www.example.com", "sameAs": [ "https://example.net/profile/example12", "https://example.org/@example34" ], "logo": "https://www.example.com/assets/images/logo.png", "contactPoint": { "contactType": "客户服务", "电子邮件": "support@example.com", "电话": "+47-99-999-9900" }, "vatID": "FR12345678901", "iso6523Code": "0199:724500PMK2A2M1SQQ228", "hasShippingService": [ { "@type": "ShippingService", "name": "运送至中国和法国", "description": "运送至

### 段落 11

**EN**

CH 5% of order value, shipping to FR always free", "fulfillmentType": "FulfillmentTypeDelivery", "shippingConditions": [ { "@type": "ShippingConditions", "shippingOrigin": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingDestination": { "@type": "DefinedRegion", "addressCountry": "CH" }, "shippingRate": { "@type": "ShippingRateSettings", "orderPercentage": "0.05" } }, { "@type": "ShippingConditions", "shippingOrigin": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingDestination": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingRate": { "@type": "MonetaryAmount", "value": "0", "currency": "EUR" } } ]

**中文**

CH 订单价值的 5%，运送至法国始终免费", "fulfillmentType": "FulfillmentTypeDelivery", "shippingConditions": [ { "@type": "ShippingConditions", "shippingOrigin": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingDestination": { "@type": "DefinedRegion", "addressCountry": "CH" }, "shippingRate": { "@type": "ShippingRateSettings", "orderPercentage": "0.05" } }, { "@type": "ShippingConditions", "shippingOrigin": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingDestination": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingRate": { "@type": "MonetaryAmount", "value": "0", "currency": "EUR" } } ]

### 段落 12

**EN**

} ], "hasMerchantReturnPolicy": { "@type": "MerchantReturnPolicy", "applicableCountry": [ "FR", "CH" ], "returnPolicyCountry": "FR", "returnPolicyCategory": "https://schema.org/MerchantReturnFiniteReturnWindow", "merchantReturnDays": 60, "returnMethod": "https://schema.org/ReturnByMail", "returnFees": "https://schema.org/FreeReturn", "refundType": "https://schema.org/FullRefund" } // Other Organization-level properties // ...

**中文**

} ], "hasMerchantReturnPolicy": { "@type": "MerchantReturnPolicy", "applicableCountry": [ "FR", "CH" ], "returnPolicyCountry": "FR", "returnPolicyCategory": "https://schema.org/MerchantReturnFiniteReturnWindow", "merchantReturnDays": 60, "returnMethod": "https://schema.org/ReturnByMail", "returnFees": "https://schema.org/FreeReturn", "refundType": "https://schema.org/FullRefund" } // 其他组织级属性 // ...

### 段落 13

**EN**

} </script> </head> <body> </body> </html> <html> <head> <title>About Us</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "OnlineStore", "name": "Example Online Store", "url": "https://www.example.com", "sameAs": [ "https://example.net/profile/example12", "https://example.org/@example34" ], "logo": "https://www.example.com/assets/images/logo.png", "contactPoint": { "contactType": "Customer Service", "email": "support@example.com", "telephone": "+47-99-999-9900" }, "vatID": "FR12345678901", "iso6523Code": "0199:724500PMK2A2M1SQQ228", "hasShippingService": [ { "@type": "ShippingService", "name": "shipping

**中文**

} </script> </head> <body> </body> </html> <html> <head> <title>关于我们</title> <script type="application/ld+json"> { "@context": "https://schema.org", "@type": "OnlineStore", "name": "示例在线商店", "url": "https://www.example.com", "sameAs": [ "https://example.net/profile/example12", "https://example.org/@example34" ], "logo": "https://www.example.com/assets/images/logo.png", "contactPoint": { "contactType": "客户服务", "电子邮件": "support@example.com", "电话": "+47-99-999-9900" }, "vatID": "FR12345678901", "iso6523Code": "0199:724500PMK2A2M1SQQ228", "hasShippingService": [ { "@type": "ShippingService", "名称": "运输

### 段落 14

**EN**

to CH and FR", "description": "Shipping to CH 5% of order value, shipping to FR always free", "fulfillmentType": "FulfillmentTypeDelivery", "shippingConditions": [ { "@type": "ShippingConditions", "shippingOrigin": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingDestination": { "@type": "DefinedRegion", "addressCountry": "CH" }, "shippingRate": { "@type": "ShippingRateSettings", "orderPercentage": "0.05" } }, { "@type": "ShippingConditions", "shippingOrigin": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingDestination": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingRate": { "@type": "MonetaryAmo

**中文**

至 CH 和 FR", "description": "运送至 CH 订单价值的 5%，运送至 FR 始终免费", "fulfillmentType": "FulfillmentTypeDelivery", "shippingConditions": [ { "@type": "ShippingConditions", "shippingOrigin": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingDestination": { "@type": "DefinedRegion", "addressCountry": "CH" }, "shippingRate": { "@type": "ShippingRateSettings", "orderPercentage": "0.05" } }, { "@type": "ShippingConditions", "shippingOrigin": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingDestination": { "@type": "DefinedRegion", "addressCountry": "FR" }, "shippingRate": { "@type": "MonetaryAmo

### 段落 15

**EN**

unt", "value": "0", "currency": "EUR" } } ] } ], "hasMerchantReturnPolicy": { "@type": "MerchantReturnPolicy", "applicableCountry": [ "FR", "CH" ], "returnPolicyCountry": "FR", "returnPolicyCategory": "https://schema.org/MerchantReturnFiniteReturnWindow", "merchantReturnDays": 60, "returnMethod": "https://schema.org/ReturnByMail", "returnFees": "https://schema.org/FreeReturn", "refundType": "https://schema.org/FullRefund" } // Other Organization-level properties // ...

**中文**

unt", "value": "0", "currency": "EUR" } } ] } ], "hasMerchantReturnPolicy": { "@type": "MerchantReturnPolicy", "applicableCountry": [ "FR", "CH" ], "returnPolicyCountry": "FR", "returnPolicyCategory": "https://schema.org/MerchantReturnFiniteReturnWindow", "merchantReturnDays": 60, "returnMethod": "https://schema.org/ReturnByMail", "returnFees": "https://schema.org/FreeReturn", "refundType": "https://schema.org/FullRefund" } // 其他组织级属性 // ...

### 段落 16

**EN**

} </script> </head> <body> </body> </html> Guidelines You must follow these guidelines to enable structured data to be eligible for inclusion in Google Search results. Warning: If your site violates one or more of these guidelines, then Google may take manual action against it. Once you have remedied the problem, you can submit your site for reconsideration . Technical guidelines Search Essentials General structured data guidelines Technical guidelines We recommend placing this information on your home page, or a single page that describes your organization, for example the about us page.

**中文**

} </script> </head> <body> </body> </html> 准则 您必须遵循这些准则才能使结构化数据有资格包含在 Google 搜索结果中。警告：如果您的网站违反了这些准则中的一项或多项，那么 Google 可能会对其采取手动操作。解决问题后，您可以提交您的网站以供重新审核。技术指南 搜索要点 一般结构化数据指南 技术指南 我们建议将此信息放置在您的主页或描述您的组织的单个页面上，例如“关于我们”页面。

### 段落 17

**EN**

You don't need to include it on every page of your site. We recommend using the most specific schema.org subtype of Organization that matches your organization. For example, if you have an ecommerce site, then we recommend using the OnlineStore subtype instead of OnlineBusiness . And if your site is about a local business, for example a restaurant or a physical store, then we recommend providing your administrative details using the most specific subtype(s) of LocalBusiness and following the required and recommended fields for Local business in addition to the fields recommended in this guide.

**中文**

您无需将其包含在网站的每个页面上。我们建议使用与您的组织匹配的最具体的 schema.org 组织子类型。例如，如果您有一个电子商务网站，那么我们建议使用 OnlineStore 子类型而不是 OnlineBusiness。如果您的网站涉及本地企业（例如餐厅或实体店），那么我们建议您使用本地企业最具体的子类型提供管理详细信息，并遵循本地企业的必填字段和建议字段以及本指南中建议的字段。

### 段落 18

**EN**

Structured data type definitions Google recognizes the following properties of an Organization . To help Google better understand your page, include as many recommended properties that apply to your web page. There are no required properties; instead, add the properties that apply to your organization. We recommend focusing on properties that are useful to your users, such as name or alternateName for your business name as well as an indication of real-world presence (for example, address or telephone ) and online presence (for example, url or logo ).

**中文**

结构化数据类型定义 Google 识别组织的以下属性。为了帮助 Google 更好地了解您的网页，请包含尽可能多的适用于您的网页的推荐属性。没有必需的属性；相反，添加适用于您的组织的属性。我们建议重点关注对您的用户有用的属性，例如您的公司名称的名称或替代名称，以及现实世界状态的指示（例如，地址或电话）和在线状态（例如，网址或徽标）。

### 段落 19

**EN**

Recommended properties address PostalAddress The address (physical or mailing) of your organization, if applicable. Include all properties that apply to your country. The more properties you provide, the higher quality the result is for users. You can provide multiple addresses if you have a location in multiple cities, states, or countries.

**中文**

推荐属性 地址 PostalAddress 您组织的地址（实际地址或邮寄地址）（如果适用）。包括适用于您所在国家/地区的所有属性。您提供的属性越多，为用户提供的结果质量就越高。如果您在多个城市、州或国家/地区有一个位置，则可以提供多个地址。

### 段落 20

**EN**

For example: "address" : [{ "@type" : "PostalAddress" , "streetAddress" : "999 W Example St Suite 99 Unit 9" , "addressLocality" : "New York" , "addressRegion" : "NY" , "postalCode" : "10019" , "addressCountry" : "US" },{ "streetAddress" : "999 Rue due exemple" , "addressLocality" : "Paris" , "postalCode" : "75001" , "addressCountry" : "FR" }] address.addressCountry Text The country for your postal address, using the two-letter ISO 3166-1 alpha-2 country code. address.addressLocality Text The city of your postal address. address.addressRegion Text The region of your postal address, if applicable. For example, a state.

**中文**

例如： "address" : [{ "@type" : "PostalAddress" , "streetAddress" : "999 W Example St Suite 99 Unit 9" , "addressLocality" : "New York" , "addressRegion" : "NY" , "postalCode" : "10019" , "addressCountry" : "US" },{ "streetAddress" : "999 Rue due example" , "addressLocality" : "Paris" , "postalCode" : "75001" , "addressCountry" : "FR" }] address.addressCountry 文本 您的邮政地址所在的国家/地区，使用两个字母的 ISO 3166-1 alpha-2 国家/地区代码。 address.addressLocality 文本 您的邮政地址所在的城市。 address.addressRegion 文本 您的邮政地址所在的区域（如果适用）。例如，一个国家。

### 段落 21

**EN**

address.postalCode Text The postal code for your address. address.streetAddress Text The full street address of your postal address. alternateName Text Another common name that your organization goes by, if applicable. contactPoint ContactPoint The best way for a user to contact your business, if applicable. Include all support methods available to your users following Google recommended best practices . For example: "contactPoint" : { "@type" : "ContactPoint" , "telephone" : "+9-999-999-9999" , "email" : "contact@example.com" } contactPoint.email Text The email address to contact your business, if applicable.

**中文**

address.postalCode 文本 您地址的邮政编码。 address.streetAddress 文本 您的邮政地址的完整街道地址。 AlternativeName 文本 您的组织使用的另一个常用名称（如果适用）。 contactPoint ContactPoint 用户联系您的企业的最佳方式（如果适用）。遵循 Google 推荐的最佳实践，包括可供用户使用的所有支持方法。例如： "contactPoint" : { "@type" : "ContactPoint" , "telephone" : "+9-999-999-9999" , "email" : "contact@example.com" } contactPoint.email 文本 用于联系您的企业的电子邮件地址（如果适用）。

### 段落 22

**EN**

If you are using a LocalBusiness type, specify a primary email address at the LocalBusiness level before using contactPoint to specify multiple ways to reach your organization. contactPoint.telephone Text The phone number to contact your business, if applicable. Be sure to include the country code and area code in the phone number. If you are using a LocalBusiness type, specify a primary phone number at the LocalBusiness level before using contactPoint to specify multiple ways to reach your organization. description Text A detailed description of your organization, if applicable.

**中文**

如果您使用的是 LocalBusiness 类型，请在使用 contactPoint 指定多种联系组织的方式之前指定 LocalBusiness 级别的主电子邮件地址。 contactPoint.telephone 文本 联系您的企业的电话号码（如果适用）。请务必在电话号码中包含国家/地区代码和区号。如果您使用的是 LocalBusiness 类型，请先在 LocalBusiness 级别指定主要电话号码，然后再使用 contactPoint 指定联系您的组织的多种方式。描述文本 您的组织的详细描述（如果适用）。

### 段落 23

**EN**

duns Text The Dun & Bradstreet DUNS number for identifying your Organization , if applicable. We encourage using the iso6523Code field with prefix 0060: instead. email Text The email address to contact your business, if applicable. foundingDate Date The date your Organization was founded in ISO 8601 date format , if applicable. globalLocationNumber Text The GS1 Global Location Number identifying the location of your Organization , if applicable. hasMerchantReturnPolicy Repeated MerchantReturnPolicy The return policy of your Organization , if applicable.

**中文**

Duns 文本 用于识别您的组织的 Dun & Bradstreet DUNS 编号（如果适用）。我们鼓励使用前缀为 0060: 的 iso6523Code 字段。电子邮件文本 用于联系您的企业的电子邮件地址（如果适用）。 foundingDate 日期 您的组织成立的日期，采用 ISO 8601 日期格式（如果适用）。 globalLocationNumber 文本 标识您的组织位置的 GS1 全球位置编号（如果适用）。 hasMerchantReturnPolicy 重复 MerchantReturnPolicy 您组织的退货政策（如果适用）。

### 段落 24

**EN**

See Merchant return policy markup for detailed information on required and optional properties for MerchantReturnPolicy . If you don't provide a return policy for your Organization , or if some of your products have specific return policies for which you need to override the return policies defined for your Organization , use this property also under merchant listing markup . hasMemberProgram Repeated MemberProgram A member (loyalty) program that you provide, if applicable. See Member program markup for detailed information on required and optional properties for MemberProgram .

**中文**

有关 MerchantReturnPolicy 必需和可选属性的详细信息，请参阅商家退货政策标记。如果您没有为您的组织提供退货政策，或者如果您的某些产品具有特定的退货政策而您需要覆盖为您的组织定义的退货政策，请在商家列表标记下也使用此属性。 hasMemberProgram 重复会员计划 您提供的会员（忠诚度）计划（如果适用）。有关 MemberProgram 必需和可选属性的详细信息，请参阅 Memberprogram 标记。

### 段落 25

**EN**

hasShippingService Repeated ShippingService The shipping policy of your Organization , if applicable. See Merchant shipping policy markup for detailed information on required and optional properties for ShippingService . If you don't provide a shipping policy for your Organization , or if some of your products have specific shipping policies for which you need to override the shipping policies defined for your Organization , use this property also under merchant listing markup . iso6523Code Text The ISO 6523 identifier of your organization, if applicable.

**中文**

hasShippingService Repeated ShippingService 您组织的运输政策（如果适用）。有关 ShippingService 必需和可选属性的详细信息，请参阅商家运输政策标记。如果您没有为您的组织提供送货政策，或者如果您的某些产品具有特定的送货政策而您需要覆盖为您的组织定义的送货政策，请在商家列表标记下也使用此属性。 iso6523Code 文本 您组织的 ISO 6523 标识符（如果适用）。

### 段落 26

**EN**

The first part of an ISO 6523 identifier is an ICD (International Code Designator) which defines which identification scheme is used. The second part is the actual identifier. We recommend separating the ICD and the identifier with a colon character ( U+003A ). Common ICD values include: 0060 : Dun & Bradstreet Data Universal Numbering System (DUNS) 0088 : GS1 Global Location Number (GLN) 0199 : Legal Entity Identifier (LEI) legalName Text The registered, legal name of your Organization , if applicable and different from the name property. leiCode Text The identifier for your Organization as defined in ISO 17442, if applicable.

**中文**

ISO 6523 标识符的第一部分是 ICD（国际代码指示符），它定义使用哪种识别方案。第二部分是实际标识符。我们建议使用冒号字符 ( U+003A ) 分隔 ICD 和标识符。常见的 ICD 值包括： 0060：Dun & Bradstreet 数据通用编号系统 (DUNS) 0088：GS1 全球位置编号 (GLN) 0199：法人实体标识符 (LEI) legalName 文本 您组织的注册法定名称（如果适用）且与名称属性不同。 leiCode 文本 ISO 17442 中定义的组织标识符（如果适用）。

### 段落 27

**EN**

We encourage using the iso6523Code field with prefix 0199: instead. logo URL or ImageObject A logo that is representative of your organization, if applicable. Adding this property can help Google better understand which logo you want to show, for example in Search results and knowledge panels. Image guidelines: The image must be 112x112px, at minimum. The image URL must be crawlable and indexable. The image file format must be supported by Google Images .

**中文**

我们鼓励使用前缀为 0199: 的 iso6523Code 字段。徽标 URL 或 ImageObject 代表您的组织的徽标（如果适用）。添加此属性可以帮助 Google 更好地了解您想要显示的徽标，例如在搜索结果和知识面板中。图片指南：图片尺寸必须至少为 112x112 像素。图像 URL 必须可抓取且可索引。图像文件格式必须受 Google Images 支持。

### 段落 28

**EN**

Make sure the image looks how you intend it to look on a purely white background (for example, if the logo is mostly white or gray, it may not look how you want it to look when displayed on a white background). If you use the ImageObject type, make sure that it has a valid contentUrl property or url property that follows the same guidelines as a URL type. naics Text The North American Industry Classification System (NAICS) code for your Organization , if applicable. name Text The name of your organization. Use the same name and alternateName that you're using for your site name .

**中文**

确保图像在纯白色背景上的外观符合您的预期（例如，如果徽标大部分为白色或灰色，则在白色背景上显示时，它可能不会达到您希望的外观）。如果您使用 ImageObject 类型，请确保它具有有效的 contentUrl 属性或 url 属性，且遵循与 URL 类型相同的准则。 naics 文本 您组织的北美行业分类系统 (NAICS) 代码（如果适用）。 name 文本 您的组织的名称。使用与站点名称相同的名称和替代名称。

### 段落 29

**EN**

numberOfEmployees QuantitativeValue The number of employees in your Organization , if applicable. Example with a specific number of employees: "numberOfEmployees" : { "@type" : "QuantitativeValue" , "value" : 2056 } Example with the number of employees in a range: "numberOfEmployees" : { "@type" : "QuantitativeValue" , "minValue" : 100 , "maxValue" : 999 } sameAs URL The URL of a page on another website with additional information about your organization, if applicable. For example, a URL to your organization's profile page on a social media or review site. You can provide multiple sameAs URLs.

**中文**

numberOfEmployees QuantitativeValue 您组织中的员工人数（如果适用）。特定员工数量的示例： "numberOfEmployees" : { "@type" : "QuantitativeValue" , "value" : 2056 } 某个范围内的员工数量示例： "numberOfEmployees" : { "@type" : "QuantitativeValue" , "minValue" : 100 , "maxValue" : 999 } sameAs URL 另一个网站上页面的 URL，其中包含有关您的附加信息组织（如果适用）。例如，社交媒体或评论网站上您组织的个人资料页面的 URL。您可以提供多个 SameAs URL。

### 段落 30

**EN**

taxID Text The tax ID associated with your Organization , if applicable. Make sure taxID matches the country that you provided in the address field. telephone Text A business phone number meant to be the primary contact method for customers, if applicable. Be sure to include the country code and area code in the phone number. url URL The URL of the website of your organization, if applicable. This helps Google uniquely identify your organization. vatID Text The VAT (Value Added Tax) code associated with your Organization , if applicable to your country and business.

**中文**

taxID 文本 与您的组织关联的税号（如果适用）。确保taxID 与您在地址字段中提供的国家/地区匹配。电话文本 企业电话号码，作为客户的主要联系方式（如果适用）。请务必在电话号码中包含国家/地区代码和区号。 url URL 您组织的网站的 URL（如果适用）。这有助于 Google 唯一地识别您的组织。 vatID 文本 与您的组织关联的增值税（增值税）代码（如果适用于您所在的国家/地区和企业）。

### 段落 31

**EN**

This is an important trust signal for users (for example, users can look up your business in public VAT registries). Troubleshooting If you're having trouble implementing or debugging structured data, here are some resources that may help you. If you're using a content management system (CMS) or someone else is taking care of your site, ask them to help you. Make sure to forward any Search Console message that details the issue to them. Google does not guarantee that features that consume structured data will show up in search results.

**中文**

这对于用户来说是一个重要的信任信号（例如，用户可以在公共增值税登记处查找您的业务）。故障排除 如果您在实施或调试结构化数据时遇到问题，这里有一些资源可能会对您有所帮助。如果您正在使用内容管理系统 (CMS) 或其他人正在维护您的网站，请让他们帮助您。请务必将任何详细说明问题的 Search Console 消息转发给他们。 Google 不保证使用结构化数据的功能会出现在搜索结果中。

### 段落 32

**EN**

For a list of common reasons why Google may not show your content in a rich result, see the General Structured Data Guidelines . You might have an error in your structured data. Check the list of structured data errors and the Unparsable structured data report . If you received a structured data manual action against your page, the structured data on the page will be ignored (although the page can still appear in Google Search results). To fix structured data issues , use the Manual Actions report . Review the guidelines again to identify if your content isn't compliant with the guidelines.

**中文**

有关 Google 可能无法在富媒体搜索结果中显示您的内容的常见原因列表，请参阅通用结构化数据指南。您的结构化数据可能有错误。检查结构化数据错误列表和不可解析的结构化数据报告。如果您收到针对您的网页的结构化数据手动操作，则该网页上的结构化数据将被忽略（尽管该网页仍会出现在 Google 搜索结果中）。要修复结构化数据问题，请使用手动操作报告。再次查看指南以确定您的内容是否不符合指南。

### 段落 33

**EN**

The problem can be caused by either spammy content or spammy markup usage. However, the issue may not be a syntax issue, and so the Rich Results Test won't be able to identify these issues. Troubleshoot missing rich results / drop in total rich results . Allow time for re-crawling and re-indexing. Remember that it may take several days after publishing a page for Google to find and crawl it. For general questions about crawling and indexing, check the Google Search crawling and indexing FAQ . Post a question in the Google Search Central forum .

**中文**

该问题可能是由垃圾内容或垃圾标记使用引起的。但是，该问题可能不是语法问题，因此富结果测试将无法识别这些问题。解决丰富搜索结果丢失/丰富搜索结果总数下降的问题。留出时间进行重新爬网和重新索引。请记住，发布页面后 Google 可能需要几天时间才能找到并抓取该页面。有关抓取和索引的一般问题，请查看 Google 搜索抓取和索引常见问题解答。在 Google 搜索中心论坛中发布问题。

### 段落 34

**EN**

Send feedback Except as otherwise noted, the content of this page is licensed under the Creative Commons Attribution 4.0 License , and code samples are licensed under the Apache 2.0 License . For details, see the Google Developers Site Policies . Java is a registered trademark of Oracle and/or its affiliates. Last updated 2026-04-15 UTC. Need to tell us more?

**中文**

发送反馈 除非另有说明，本页内容已根据 Creative Commons Attribution 4.0 License 获得许可，代码示例根据 Apache 2.0 License 获得许可。有关详细信息，请参阅 Google 开发者网站政策。 Java 是 Oracle 和/或其附属公司的注册商标。最后更新时间：世界标准时间 2026 年 4 月 15 日。需要告诉我们更多吗？

### 段落 35

**EN**

[[["Easy to understand","easyToUnderstand","thumb-up"],["Solved my problem","solvedMyProblem","thumb-up"],["Other","otherUp","thumb-up"]],[["Missing the information I need","missingTheInformationINeed","thumb-down"],["Too complicated / too many steps","tooComplicatedTooManySteps","thumb-down"],["Out of date","outOfDate","thumb-down"],["Samples / code issue","samplesCodeIssue","thumb-down"],["Other","otherDown","thumb-down"]],["Last updated 2026-04-15 UTC."],[],["To enhance Google Search visibility, implement `Organization` structured data on your website's homepage, specifying details like name, logo, and contact information.

**中文**

[[["易于理解","easyToUnderstand","thumb-up"],["解决了我的问题","solvedMyProblem","thumb-up"],["其他","otherUp","thumb-up"]],[["缺少我需要的信息","missingTheInformationINeed","thumb-down"],["太复杂/太复杂许多步骤","tooComplicatedTooManySteps","thumb-down"],["过时","outOfDate","thumb-down"],["示例/代码问题","samplesCodeIssue","thumb-down"],["其他","otherDown","thumb-down"]],["最后更新时间为 2026-04-15 UTC。"],[],["为了提高 Google 搜索可见性，请在网站主页上实施“组织”结构化数据，指定名称、徽标和联系信息等详细信息。

### 段落 36

**EN**

Key actions include: adding relevant properties, adhering to guidelines, validating with the Rich Results Test, deploying and testing on a few pages, and maintaining by submitting sitemaps. For online stores, utilize `OnlineStore` subtype with `contactPoint` and `hasMerchantReturnPolicy`. The merchant return policy requires defining properties like `applicableCountry` and `returnPolicyCategory`, and also allows recommended properties like `refundType`.

**中文**

关键操作包括：添加相关属性、遵守指南、使用丰富结果测试进行验证、在几个页面上进行部署和测试以及通过提交站点地图进行维护。对于在线商店，请使用带有“contactPoint”和“hasMerchantReturnPolicy”的“OnlineStore”子类型。商家退货政策需要定义“applicableCountry”和“returnPolicyCategory”等属性，并且还允许“refundType”等推荐属性。

### 段落 37

**EN**

Maintain and re-crawl the data.\n"]] LinkedIn Join us on LinkedIn YouTube Watch our videos Blog Subscribe to our RSS feed Podcast Listen to Search Off the Record X (Twitter) Join us on X (Twitter) Get support Go to the help forum Submit a question for office hours Report spam, phishing, or malware More support resources Resources Do you need an SEO?

**中文**

维护并重新抓取数据。\n"]] LinkedIn 在 LinkedIn 上加入我们 YouTube 观看我们的视频 博客 订阅我们的 RSS 源 播客 收听搜索 关闭记录 X (Twitter) 在 X 上加入我们 (Twitter) 获取支持 转至帮助论坛 在办公时间提交问题 报告垃圾邮件、网络钓鱼或恶意软件 更多支持资源 资源 您需要 SEO 吗？

### 段落 38

**EN**

SEO Starter Guide Status of Search systems Search Console documentation Case Studies Tools Search Console Rich Results Test PageSpeed Insights AMP Test Android Chrome Firebase Google Cloud Platform Google AI All products Terms Privacy Manage cookies English Deutsch Español Español – América Latina Français Indonesia Italiano Polski Português – Brasil Tiếng Việt Türkçe Русский العربيّة हिंदी ภาษาไทย 中文 – 简体 中文 – 繁體 日本語 한국어

**中文**

SEO 入门指南 搜索系统状态 搜索控制台文档 案例研究 工具 搜索控制台 富结果测试 PageSpeed Insights AMP 测试 Android Chrome Firebase Google Cloud Platform Google AI 所有产品 条款 隐私 管理 cookie 英语 德语 西班牙语 法语 印度尼西亚 意大利语 波兰语 葡萄牙语 – 巴西 Tiếng Việt Türkçe Русский ????????? हिंदी ภาษาไทย 中文 – 简体中文 – 繁体日本语 한국어
