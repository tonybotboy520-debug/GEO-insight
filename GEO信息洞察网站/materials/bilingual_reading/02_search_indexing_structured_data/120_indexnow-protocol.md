# IndexNow - Protocol

- ID: 120
- 类型: html
- 分类: 02_search_indexing_structured_data
- 主题: URL发现/提交
- 原文链接: https://www.indexnow.org/documentation
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

Documentation | IndexNow.org IndexNow.org Home Documentation FAQ EN English (United States) English (United States) Arabic العربية Basque euskara Bulgarian български Catalan català Chinese (Simplified) Legacy 中文(简体) 旧版 Chinese (Traditional) Legacy 中文(繁體) 舊版 Croatian hrvatski Czech čeština Danish dansk Dutch Nederlands English (United Kingdom) English (United Kingdom) Estonian eesti Finnish suomi French français Galician galego German Deutsch Greek Ελληνικά Hebrew עברית Hindi हिन्दी Hungarian magyar Icelandic íslenska Italian italiano Japanese 日本語 Korean 한국어 Latvian latviešu Lithuanian lietuvių Malay Melayu Norwegian, Bokmål (Norway) norsk bok

**中文**

文档 | IndexNow.org IndexNow.org 主页 文档 常见问题 EN 英语（美国） 英语（美国） 阿拉伯语 巴克语 euskara 保加利亚语 български 加泰罗尼亚语 català 中文（简体） 旧版中文（繁体） 旧版中文（繁体） 旧版 克罗地亚语 hrvatski 捷克语 čeština 丹麦语 dansk 荷兰语 荷兰语 英语（美国）王国) 英语 (英国) 爱沙尼亚语 eesti 芬兰语 suomi 法语 français 加利西亚语 galego 德语 德语 希腊语 Ελληνικά 希伯来语 עברйת 印地语 हिन्दी 匈牙利语 magyar 冰岛语 íslenska 意大利语 意大利语 日语 日本语 韩语 한국어 拉脱维亚语 latviešu立陶宛语 lietuvių 马来语 Melayu 挪威语、博克马尔语（挪威）norsk bok

### 段落 2

**EN**

mål (Norge) Polish polski Portuguese (Brazil) português (Brasil) Portuguese (Portugal) português (Portugal) Romanian română Russian русский Serbian srpski Slovak slovenčina Slovenian slovenščina Spanish español Swedish svenska Thai ไทย Turkish Türkçe Ukrainian українська Vietnamese Tiếng Việt Documentation Submitting One URL To submit a URL using an HTTP request (replace with the URL provided by the search engine), issue your request to the following URL: https://<searchengine>/indexnow?

**中文**

mål（挪威） 波兰语 polski 葡萄牙语（巴西） português（巴西） 葡萄牙语（葡萄牙） português（葡萄牙） 罗马尼亚语 română 俄语 русский 塞尔维亚语 srpski 斯洛伐克语 slovenčina 斯洛文尼亚语 slovenščina 西班牙语 español 瑞典语 svenska 泰语 ไทย 土耳其语 Türkçe乌克兰语 українська 越南语 Tiếng Việt 文档 提交一个 URL 要使用 HTTP 请求提交 URL（替换为搜索引擎提供的 URL），请将请求发送到以下 URL：https://<searchengine>/indexnow?

### 段落 3

**EN**

url =url-changed& key =your-key url-changed is a URL of your website which has been added, updated, or deleted. URL must be URL-escaped and encoded and please make sure that your URLs follow the RFC-3986 standard for URIs. Your-key should have a minimum of 8 and a maximum of 128 hexadecimal characters. The key can contain only the following characters: lowercase characters (a-z), uppercase characters (A-Z), numbers (0-9), and dashes (-). For example, if you want to notify search engines that https://www.example.com/product.html has been updated, and you want to use this key your URL will be: https://<searchengine>/indexnow?

**中文**

url =url-changed& key =your-key url-changed 是已添加、更新或删除的网站的 URL。 URL 必须进行 URL 转义和编码，并且请确保您的 URL 遵循 URI 的 RFC-3986 标准。您的密钥应至少包含 8 个、最多 128 个十六进制字符。该密钥只能包含以下字符：小写字符 (a-z)、大写字符 (A-Z)、数字 (0-9) 和破折号 (-)。例如，如果您想通知搜索引擎 https://www.example.com/product.html 已更新，并且您想使用此键，您的 URL 将是：https://<searchengine>/indexnow?

### 段落 4

**EN**

url =https://www.example.com/product.html& key = You can issue the HTTP request using your browser, wget, curl, or any other mechanism of your choosing. A successful request will return an HTTP 200 response code; if you receive a different response, verify that you don’t submit too often, that the key and URL are valid and resubmit the request. The HTTP 200 response code only indicates that the search engine has received your URL. Submitting set of URLs To submit a set of URLs using an HTTP request issue your POST JSON request to the URL provided by Search Engines. Replace by the host name of the search engine.

**中文**

url =https://www.example.com/product.html& key = 您可以使用浏览器、wget、curl 或您选择的任何其他机制发出 HTTP 请求。成功请求将返回 HTTP 200 响应代码；如果您收到不同的响应，请验证您是否提交得过于频繁，密钥和 URL 是否有效，然后重新提交请求。 HTTP 200 响应代码仅表明搜索引擎已收到您的 URL。提交一组 URL 要使用 HTTP 请求提交一组 URL，请向搜索引擎提供的 URL 发出 POST JSON 请求。替换为搜索引擎的主机名。

### 段落 5

**EN**

POST /indexnow HTTP /1.1 Content-Type : application/json; charset=utf-8 Host : <searchengine> { "host" : "www.example.com", "key" : " ", "urlList" : [ "https://www.example.com/url1", "https://www.example.com/folder/url2", "https://www.example.com/url3" ] } You can submit up to 10,000 URLs per post, mixing http and https URLs if needed. You can issue the HTTP request using wget, curl, or another mechanism of your choosing. A successful request will return an HTTP 200 response code; if you receive a different response, you should verify your request and if everything looks fine, resubmit your request.

**中文**

POST /indexnow HTTP /1.1 内容类型：application/json； charset=utf-8 Host : <searchengine> { "host" : "www.example.com", "key" : " ", "urlList" : [ "https://www.example.com/url1", "https://www.example.com/folder/url2", "https://www.example.com/url3" ] } 每个帖子最多可以提交 10,000 个 URL，如果需要，可以混合 http 和 https URL。您可以使用 wget、curl 或您选择的其他机制发出 HTTP 请求。成功请求将返回 HTTP 200 响应代码；如果您收到不同的回复，您应该验证您的请求，如果一切正常，请重新提交您的请求。

### 段落 6

**EN**

The HTTP 200 response code only indicates that the search engine has received your set of URLs. The recommended way is to automate submission of URLs as soon as the content is added, updated, or deleted up to some limit; see best practices for user generated content in the Frequently Asked Questions. Verifying ownership via the key To submit URLs, you must "prove" ownership of the host for which URLs are being submitted by hosting at least one text file within the host. Once you submit your URLs to search engines, search engines will crawl the key file to verify ownership and use the key until you change the key.

**中文**

HTTP 200 响应代码仅表明搜索引擎已收到您的 URL 集。推荐的方法是在内容添加、更新或删除达到一定限制后立即自动提交 URL；请参阅常见问题中的用户生成内容的最佳实践。通过密钥验证所有权 要提交 URL，您必须通过在主机内托管至少一个文本文件来“证明”要为其提交 URL 的主机的所有权。一旦您将 URL 提交给搜索引擎，搜索引擎将抓取密钥文件以验证所有权并使用该密钥，直到您更改密钥为止。

### 段落 7

**EN**

Only you and the search engines should know the key and your file key location. We offer two ways to verify ownership. Option 1 Hosting a text key file at the root directory of your host. You must host a UTF-8 encoded text key file {your-key}.txt listing the key in the file at the root directory of your website. For instance for the previous examples, you will need to host your UTF-8 key file at https://www.example.com/ .txt and this file must contain the key Option 2 Hosting a text key file within your host.

**中文**

只有您和搜索引擎应该知道密钥和您的文件密钥位置。我们提供两种方法来验证所有权。选项 1 在主机的根目录中托管文本密钥文件。您必须托管一个 UTF-8 编码的文本密钥文件 {your-key}.txt，其中列出了网站根目录下文件中的密钥。例如，对于前面的示例，您需要将 UTF-8 密钥文件托管在 https://www.example.com/.txt，并且该文件必须包含密钥 选项 2 在您的主机中托管文本密钥文件。

### 段落 8

**EN**

You can also host one to many UTF-8 encoded text key files in other locations within the same host and you must tell search engines the location of this text key file in each IndexNow notification by specifying the location using the keyLocation variable. If you submit an URL, specify the key file location as keyLocation URLs parameter value. https://<searchengine>/indexnow? url =http://www.example.com/product.html& key = & keyLocation =http://www.example.com/myIndexNowKey63638.txt If you submit a set of URLs, specify the key file location as keyLocation variable in the JSON content.

**中文**

您还可以在同一主机内的其他位置托管一对多的 UTF-8 编码文本密钥文件，并且您必须通过使用 keyLocation 变量指定位置来告诉搜索引擎每个 IndexNow 通知中此文本密钥文件的位置。如果您提交 URL，请将密钥文件位置指定为 keyLocation URLs 参数值。 https://<搜索引擎>/indexnow? url =http://www.example.com/product.html& key = & keyLocation =http://www.example.com/myIndexNowKey63638.txt 如果您提交一组 URL，请将密钥文件位置指定为 JSON 内容中的 keyLocation 变量。

### 段落 9

**EN**

POST /indexnow HTTP /1.1 Content-Type : application/json; charset=utf-8 Host : <searchengine> { "host" : "www.example.com", "key" : " ", "keyLocation" : "https://www.example.com/myIndexNowKey63638.txt", "urlList" : [ "https://www.example.com/url1", "https://www.example.com/folder/url2", "https://www.example.com/url3" ] } In this option 2, the location of a key file determines the set of URLs that can be included with this key. A key file located at http://example.com/catalog/key12457EDd.txt can include any URLs starting with http://example.com/catalog/ but cannot include URLs starting with http://example.com/help/ .

**中文**

POST /indexnow HTTP /1.1 内容类型：application/json； charset=utf-8 Host : <searchengine> { "host" : "www.example.com", "key" : " ", "keyLocation" : "https://www.example.com/myIndexNowKey63638.txt", "urlList" : [ "https://www.example.com/url1", "https://www.example.com/folder/url2", "https://www.example.com/url3" ]在此选项 2 中，密钥文件的位置决定了可以包含在该密钥中的 URL 集。位于 http://example.com/catalog/key12457EDd.txt 的密钥文件可以包含以 http://example.com/catalog/ 开头的任何 URL，但不能包含以 http://example.com/help/ 开头的 URL。

### 段落 10

**EN**

URLs considered valid in http://example.com/catalog/ include: http://example.com/catalog/show?item=23 http://example.com/catalog/show?item=233&user=3453 URLs not considered valid in http://example.com/catalog/ include: http://example.com/image/show?item=23 http://example.com/image/show?item=233&user=3453 URLs that are not considered valid in option 2 may not be considered for indexing. It is strongly recommended that you use Option 1 and place your file key at the root directory of your web server. Response format HTTP Code Response Reasons 200 OK URL submitted successfully 202 Accepted URL received. IndexNow key validation pending.

**中文**

http://example.com/catalog/ 中被视为有效的 URL 包括：http://example.com/catalog/show?item=23 http://example.com/catalog/show?item=233&user=3453 http://example.com/catalog/ 中被视为无效的 URL 包括：http://example.com/image/show?item=23 http://example.com/image/show?item=233&user=3453 URL在选项 2 中被视为无效的内容可能不会被考虑用于索引。强烈建议您使用选项 1 并将文件密钥放置在 Web 服务器的根目录中。响应格式 HTTP 代码 响应原因 200 OK URL 提交成功 202 已收到接受的 URL。 IndexNow 密钥验证待决。

### 段落 11

**EN**

400 Bad request Invalid format 403 Forbidden In case of key not valid (e.g. key not found, file found but key not in the file) 422 Unprocessable Entity In case of URLs which don’t belong to the host or the key is not matching the schema in the protocol 429 Too Many Requests Too Many Requests (potential Spam) Requirement for search engines Search engines adopting the IndexNow protocol agree that submitted URLs will be automatically shared with all other participating search engines.

**中文**

400 Bad request 格式无效 403 Forbidden 如果密钥无效（例如密钥未找到，找到文件但密钥不在文件中） 422 Unprocessable Entity 如果 URL 不属于主机或密钥与协议中的模式不匹配 429 Too Many Requests 太多请求（潜在的垃圾邮件） 对搜索引擎的要求 采用 IndexNow 协议的搜索引擎同意提交的 URL 将自动与所有搜索引擎共享其他参与的搜索引擎。

### 段落 12

**EN**

To participate, search engines must have a noticeable presence in at least one market or be closely linked to the search market and make a significant contribution to the number of url submissions. Learn more Terms and Conditions

**中文**

要参与其中，搜索引擎必须在至少一个市场中占有显着地位，或者与搜索市场密切相关，并对 URL 提交数量做出重大贡献。了解更多条款和条件
