# RFC 9309 - Robots Exclusion Protocol

- ID: 121
- 类型: html
- 分类: 02_search_indexing_structured_data
- 主题: 爬虫控制标准
- 原文链接: https://www.rfc-editor.org/rfc/rfc9309.html
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

RFC 9309: Robots Exclusion Protocol RFC 9309 Robots Exclusion Protocol (REP) September 2022 Koster, et al. Standards Track [Page] Stream: Internet Engineering Task Force (IETF) RFC: 9309 Category: Standards Track Published: September 2022 ISSN: 2070-1721 Authors: M. Koster G. Illyes Google LLC H. Zeller Google LLC L. Sassman Google LLC RFC 9309 Robots Exclusion Protocol Abstract This document specifies and extends the "Robots Exclusion Protocol" method originally defined by Martijn Koster in 1994 for service owners to control how content served by their services may be accessed, if at all, by automatic clients known as crawlers.

**中文**

RFC 9309：机器人排除协议 RFC 9309 机器人排除协议 (REP) 2022 年 9 月 Koster 等人。标准轨道 [页] 流：互联网工程任务组 (IETF) RFC：9309 类别：标准轨道 发布时间：2022 年 9 月 ISSN：2070-1721 作者：M. Koster G. Illyes Google LLC H. Zeller Google LLC L. Sassman Google LLC RFC 9309 机器人排除协议摘要 本文档指定并扩展了最初由 Martijn Koster 定义的“机器人排除协议”方法1994 年，服务所有者可以控制其服务所提供的内容如何被称为爬虫的自动客户端访问（如果有的话）。

### 段落 2

**EN**

Specifically, it adds definition language for the protocol, instructions for handling errors, and instructions for caching. ¶ Status of This Memo This is an Internet Standards Track document. ¶ This document is a product of the Internet Engineering Task Force (IETF). It represents the consensus of the IETF community. It has received public review and has been approved for publication by the Internet Engineering Steering Group (IESG). Further information on Internet Standards is available in Section 2 of RFC 7841.

**中文**

具体来说，它添加了协议的定义语言、处理错误的指令以及缓存的指令。 ¶ 本备忘录的状态 这是一份互联网标准跟踪文档。 ¶ 本文档是互联网工程任务组 (IETF) 的产品。它代表了IETF社区的共识。它已接受公众审查，并已被互联网工程指导小组 (IESG) 批准发布。有关互联网标准的更多信息，请参阅 RFC 7841 第 2 节。

### 段落 3

**EN**

¶ Information about the current status of this document, any errata, and how to provide feedback on it may be obtained at https://www.rfc-editor.org/info/rfc9309 . ¶ Copyright Notice Copyright (c) 2022 IETF Trust and the persons identified as the document authors. All rights reserved. ¶ This document is subject to BCP 78 and the IETF Trust's Legal Provisions Relating to IETF Documents ( https://trustee.ietf.org/license-info ) in effect on the date of publication of this document. Please review these documents carefully, as they describe your rights and restrictions with respect to this document.

**中文**

¶ 有关本文档当前状态、任何勘误表以及如何提供反馈的信息，请访问 https://www.rfc-editor.org/info/rfc9309。 ¶ 版权声明 版权所有 (c) 2022 IETF Trust 和文档作者。版权所有。 ¶ 本文档受本文档发布之日生效的 BCP 78 和 IETF Trust 与 IETF 文件相关的法律规定 ( https://trustee.ietf.org/license-info ) 的约束。请仔细阅读这些文件，因为它们描述了您与本文件相关的权利和限制。

### 段落 4

**EN**

Code Components extracted from this document must include Revised BSD License text as described in Section 4.e of the Trust Legal Provisions and are provided without warranty as described in the Revised BSD License. ¶ ▲ Table of Contents 1 . Introduction 1.1 . Requirements Language 2 . Specification 2.1 . Protocol Definition 2.2 . Formal Syntax 2.2.1 . The User-Agent Line 2.2.2 . The "Allow" and "Disallow" Lines 2.2.3 . Special Characters 2.2.4 . Other Records 2.3 . Access Method 2.3.1 . Access Results 2.3.1.1 . Successful Access 2.3.1.2 . Redirects 2.3.1.3 . "Unavailable" Status 2.3.1.4 . "Unreachable" Status 2.3.1.5 . Parsing Errors 2.4 .

**中文**

从本文档中提取的代码组件必须包括《信托法律条款》第 4.e 节中所述的修订版 BSD 许可证文本，并且不提供修订版 BSD 许可证中所述的保证。 ¶ ▲ 目录 1． 1.1 引言要求语言 2．规范2.1。协议定义 2.2。形式语法 2.2.1。用户代理线 2.2.2。 “允许”和“不允许”行 2.2.3。特殊字符 2.2.4。其他记录 2.3．访问方法2.3.1．访问结果 2.3.1.1。成功访问2.3.1.2。重定向 2.3.1.3。 “不可用”状态 2.3.1.4 . “无法访问”状态 2.3.1.5。 2.4 解析错误

### 段落 5

**EN**

Caching 2.5 . Limits 3 . Security Considerations 4 . IANA Considerations 5 . Examples 5.1 . Simple Example 5.2 . Longest Match 6 . References 6.1 . Normative References 6.2 . Informative References Authors' Addresses 1. Introduction This document applies to services that provide resources that clients can access through URIs as defined in [ RFC3986 ] . For example, in the context of HTTP, a browser is a client that displays the content of a web page. ¶ Crawlers are automated clients. Search engines, for instance, have crawlers to recursively traverse links for indexing as defined in [ RFC8288 ] .

**中文**

缓存2.5。限制 3．安全考虑 4． IANA 考虑因素 5．例子 5.1.简单示例 5.2。最长匹配 6 .参考文献6.1。规范性引用文件6.2．资料性参考文献 作者地址 1. 简介 本文档适用于提供客户端可通过 [RFC3986] 中定义的 URI 访问的资源的服务。例如，在 HTTP 上下文中，浏览器是显示网页内容的客户端。 ¶ 爬虫是自动化客户端。例如，搜索引擎有爬虫程序来递归地遍历链接以进行索引，如 [RFC8288] 中所定义。

### 段落 6

**EN**

¶ It may be inconvenient for service owners if crawlers visit the entirety of their URI space. This document specifies the rules originally defined by the "Robots Exclusion Protocol" [ ROBOTSTXT ] that crawlers are requested to honor when accessing URIs. ¶ These rules are not a form of access authorization. ¶ 1.1.

**中文**

¶ 如果爬虫访问服务所有者的整个 URI 空间，这可能会给服务所有者带来不便。本文档指定了最初由“机器人排除协议”[ ROBOTSTXT ] 定义的规则，爬虫在访问 URI 时需要遵守这些规则。 ¶ 这些规则不是访问授权的一种形式。 ¶ 1.1.

### 段落 7

**EN**

Requirements Language The key words " MUST ", " MUST NOT ", " REQUIRED ", " SHALL ", " SHALL NOT ", " SHOULD ", " SHOULD NOT ", " RECOMMENDED ", " NOT RECOMMENDED ", " MAY ", and " OPTIONAL " in this document are to be interpreted as described in BCP 14 [ RFC2119 ] [ RFC8174 ] when, and only when, they appear in all capitals, as shown here. ¶ 2. Specification 2.1. Protocol Definition The protocol language consists of rule(s) and group(s) that the service makes available in a file named "robots.txt" as described in Section 2.3 : ¶ Rule: A line with a key-value pair that defines how a crawler may access URIs. See Section 2.2.2 .

**中文**

要求语言 本文档中的关键词“必须”、“不得”、“必需”、“应”、“不应”、“应该”、“不应该”、“推荐”、“不推荐”、“可以”和“可选”当且仅当它们出现在所有大写字母中，如下所示。 ¶ 2. 规范 2.1。协议定义 协议语言由服务在名为“robots.txt”的文件中提供的规则和组组成，如第 2.3 节中所述： ¶ 规则：带有键值对的行，定义爬网程序如何访问 URI。参见第 2.2.2 节。

### 段落 8

**EN**

¶ Group: One or more user-agent lines that are followed by one or more rules. The group is terminated by a user-agent line or end of file. See Section 2.2.1 . The last group may have no rules, which means it implicitly allows everything. ¶ 2.2. Formal Syntax Below is an Augmented Backus-Naur Form (ABNF) description, as described in [ RFC5234 ] . ¶ robotstxt = *(group / emptyline) group = startgroupline ; We start with a user-agent ; line *(startgroupline / emptyline) ; ...

**中文**

¶ 组：一个或多个用户代理行，后面跟着一个或多个规则。该组由用户代理行或文件末尾终止。参见第 2.2.1 节。最后一组可能没有规则，这意味着它隐式允许一切。 ¶ 2.2.形式语法 下面是增强巴科斯范式 (ABNF) 描述，如 [RFC5234] 中所述。 ¶ robotstxt = *(组/空行) 组 = startgroupline ;我们从用户代理开始；行*(起始组行/空行); ...

### 段落 9

**EN**

and possibly more ; user-agent lines *(rule / emptyline) ; followed by rules relevant ; for the preceding ; user-agent lines startgroupline = *WS "user-agent" *WS ":" *WS product-token EOL rule = *WS ("allow" / "disallow") *WS ":" *WS (path-pattern / empty-pattern) EOL ; parser implementors: define additional lines you need (for ; example, Sitemaps).

**中文**

可能还有更多；用户代理行*(规则/空行);遵循相关规则；对于前面的；用户代理行 startgroupline = *WS "用户代理" *WS ":" *WS 产品令牌 EOL 规则 = *WS ("允许" / "禁止") *WS ":" *WS (路径模式/空模式) EOL ;解析器实现者：定义您需要的其他行（例如，站点地图）。

### 段落 10

**EN**

product-token = identifier / "*" path-pattern = "/" *UTF8-char-noctl ; valid URI path pattern empty-pattern = *WS identifier = 1*(%x2D / %x41-5A / %x5F / %x61-7A) comment = "#" *(UTF8-char-noctl / WS / "#") emptyline = EOL EOL = *WS [comment] NL ; end-of-line may have ; optional trailing comment NL = %x0D / %x0A / %x0D.0A WS = %x20 / %x09 ; UTF8 derived from RFC 3629, but excluding control characters UTF8-char-noctl = UTF8-1-noctl / UTF8-2 / UTF8-3 / UTF8-4 UTF8-1-noctl = %x21 / %x22 / %x24-7F ; excluding control, space, "#" UTF8-2 = %xC2-DF UTF8-tail UTF8-3 = %xE0 %xA0-BF UTF8-tail / %xE1-EC 2UTF8-tail / %xED %x80-9F UTF8-tail / %xEE-EF 2UTF8-tail UTF8-4 = %xF0 %x90-BF 2UTF8-tail / %xF1-F3 3UTF8-tail / %xF4 %x80-8F 2UTF8-tail UTF8-tail = %x80-BF ¶ 2.2.1.

**中文**

产品令牌 = 标识符 / "*" 路径模式 = "/" *UTF8-char-noctl ;有效的 URI 路径模式 空模式 = *WS 标识符 = 1*(%x2D / %x41-5A / %x5F / %x61-7A) 注释 = "#" *(UTF8-char-noctl / WS / "#") 空行 = EOL EOL = *WS [注释] NL ;行尾可能有 ;可选的尾随注释 NL = %x0D / %x0A / %x0D.0A WS = %x20 / %x09 ; UTF8 源自 RFC 3629，但不包括控制字符 UTF8-char-noctl = UTF8-1-noctl / UTF8-2 / UTF8-3 / UTF8-4 UTF8-1-noctl = %x21 / %x22 / %x24-7F；不包括控制、空格、“#” UTF8-2 = %xC2-DF UTF8-tail UTF8-3 = %xE0 %xA0-BF UTF8-tail / %xE1-EC 2UTF8-tail / %xED %x80-9F UTF8-tail / %xEE-EF 2UTF8-tail UTF8-4 = %xF0 %x90-BF 2UTF8-tail / %xF1-F3 3UTF8-tail / %xF4 %x80-8F 2UTF8-tail UTF8-tail = %x80-BF ¶ 2.2.1.

### 段落 11

**EN**

The User-Agent Line Crawlers set their own name, which is called a product token, to find relevant groups. The product token MUST contain only uppercase and lowercase letters ("a-z" and "A-Z"), underscores ("_"), and hyphens ("-"). The product token SHOULD be a substring of the identification string that the crawler sends to the service. For example, in the case of HTTP [ RFC9110 ] , the product token SHOULD be a substring in the User-Agent header. The identification string SHOULD describe the purpose of the crawler.

**中文**

用户代理线路爬虫设置自己的名称（称为产品令牌）来查找相关组。产品令牌必须仅包含大写和小写字母（“a-z”和“A-Z”）、下划线（“_”）和连字符（“-”）。产品令牌应该是爬虫发送到服务的标识字符串的子字符串。例如，在 HTTP [RFC9110] 的情况下，产品令牌应该是 User-Agent 标头中的子字符串。标识字符串应该描述爬虫的目的。

### 段落 12

**EN**

Here's an example of a User-Agent HTTP request header with a link pointing to a page describing the purpose of the ExampleBot crawler, which appears as a substring in the User-Agent HTTP header and as a product token in the robots.txt user-agent line: ¶ +==========================================+========================+ | User-Agent HTTP header | robots.txt user-agent | | | line | +==========================================+========================+ | User-Agent: Mozilla/5.0 (compatible; | user-agent: ExampleBot | | ExampleBot/0.1; | | | https://www.example.com/bot.html) | | +------------------------------------------+----------------------

**中文**

以下是 User-Agent HTTP 请求标头的示例，其中包含一个指向描述 ExampleBot 爬网程序用途的页面的链接，该链接显示为 User-Agent HTTP 标头中的子字符串以及 robots.txt 用户代理行中的产品令牌： ¶ +============================================+==========================+ |用户代理 HTTP 标头 | robots.txt 用户代理 | | |线 | +============================================+==========================+ |用户代理：Mozilla/5.0（兼容；| 用户代理：ExampleBot | | ExampleBot/0.1；| | | https://www.example.com/bot.html）| | +------------------------------------------------------+----------------------

### 段落 13

**EN**

--+ Figure 1 : Example of a User-Agent HTTP header and robots.txt user-agent line for the ExampleBot product token Note that the product token (ExampleBot) is a substring of the User-Agent HTTP header.

**中文**

--+ 图 1：ExampleBot 产品令牌的 User-Agent HTTP 标头和 robots.txt 用户代理行示例 请注意，产品令牌 (ExampleBot) 是 User-Agent HTTP 标头的子字符串。

### 段落 14

**EN**

¶ Crawlers MUST use case-insensitive matching to find the group that matches the product token and then obey the rules of the group. If there is more than one group matching the user-agent, the matching groups' rules MUST be combined into one group and parsed according to Section 2.2.2 .

**中文**

¶ 爬虫必须使用不区分大小写的匹配来查找与产品令牌匹配的组，然后遵守该组的规则。如果有多个组与用户代理匹配，则匹配组的规则必须合并为一组并根据第 2.2.2 节进行解析。

### 段落 15

**EN**

¶ +========================================+========================+ | Two groups that match the same product | Merged group | | token exactly | | +========================================+========================+ | user-agent: ExampleBot | user-agent: ExampleBot | | disallow: /foo | disallow: /foo | | disallow: /bar | disallow: /bar | | | disallow: /baz | | user-agent: ExampleBot | | | disallow: /baz | | +----------------------------------------+------------------------+ Figure 2 : Example of how to merge two robots.txt groups that match the same product token If no matching group exists, crawlers MUST obey the group with a user-agent line with the "*" value, if present.

**中文**

¶ +========================================+========================+ |匹配相同产品的两组 |合并组 | |令牌正是| | +==========================================+==========================+ |用户代理：ExampleBot |用户代理：ExampleBot | |禁止：/foo |禁止：/foo | |禁止：/bar |禁止：/bar | | |禁止：/baz | |用户代理：ExampleBot | | |禁止：/baz | | +------------------------------------------------+------------------------+ 图 2：如何合并两个匹配相同产品标记的 robots.txt 组的示例 如果不存在匹配组，爬虫必须服从带有“*”值（如果存在）的用户代理行的组。

### 段落 16

**EN**

¶ +==================================+======================+ | Two groups that don't explicitly | Applicable group for | | match ExampleBot | ExampleBot | +==================================+======================+ | user-agent: * | user-agent: * | | disallow: /foo | disallow: /foo | | disallow: /bar | disallow: /bar | | | | | user-agent: BazBot | | | disallow: /baz | | +----------------------------------+----------------------+ Figure 3 : Example of no matching groups other than the "*" for the ExampleBot product token If no group matches the product token and there is no group with a user-agent line with the "*" value, or no groups are present at all, no rules apply.

**中文**

¶ +====================================+========================+ |两个没有明确说明的群体 |适用群体为 | |匹配示例机器人 |示例机器人 | +==================================+======================+ |用户代理：* |用户代理：* | |禁止：/foo |禁止：/foo | |禁止：/bar |禁止：/bar | | | | |用户代理：BazBot | | |禁止：/baz | | +----------------------------------+----------------------+ 图 3：ExampleBot 产品令牌的“*”之外没有任何匹配组的示例 如果没有组与产品令牌匹配，并且不存在带有“*”值的用户代理行的组，或者根本不存在任何组，则不适用任何规则。

### 段落 17

**EN**

¶ 2.2.2. The "Allow" and "Disallow" Lines These lines indicate whether accessing a URI that matches the corresponding path is allowed or disallowed. ¶ To evaluate if access to a URI is allowed, a crawler MUST match the paths in "allow" and "disallow" rules against the URI. The matching SHOULD be case sensitive. The matching MUST start with the first octet of the path. The most specific match found MUST be used. The most specific match is the match that has the most octets. Duplicate rules in a group MAY be deduplicated. If an "allow" rule and a "disallow" rule are equivalent, then the "allow" rule SHOULD be used.

**中文**

¶ 2.2.2. “Allow”和“Disallow”行 这些行指示是否允许或禁止访问与相应路径匹配的 URI。 ¶ 要评估是否允许访问 URI，爬虫必须将“允许”和“禁止”规则中的路径与 URI 进行匹配。匹配应该区分大小写。匹配必须以路径的第一个八位字节开始。必须使用找到的最具体的匹配。最具体的匹配是具有最多八位位组的匹配。组中的重复规则可以进行重复数据删除。如果“允许”规则和“禁止”规则等效，则应该使用“允许”规则。

### 段落 18

**EN**

If no match is found amongst the rules in a group for a matching user-agent or there are no rules in the group, the URI is allowed. The /robots.txt URI is implicitly allowed. ¶ Octets in the URI and robots.txt paths outside the range of the ASCII coded character set, and those in the reserved range defined by [ RFC3986 ] , MUST be percent-encoded as defined by [ RFC3986 ] prior to comparison. ¶ If a percent-encoded ASCII octet is encountered in the URI, it MUST be unencoded prior to comparison, unless it is a reserved character in the URI as defined by [ RFC3986 ] or the character is outside the unreserved character range.

**中文**

如果在组中的规则中未找到匹配用户代理的匹配项，或者组中没有规则，则允许使用该 URI。隐式允许 /robots.txt URI。 ¶ URI 和 robots.txt 路径中超出 ASCII 编码字符集范围的八位字节以及在 [ RFC3986 ] 定义的保留范围内的八位字节，必须在比较之前按照 [ RFC3986 ] 的定义进行百分比编码。 ¶ 如果在 URI 中遇到百分比编码的 ASCII 八位字节，则在比较之前必须对其进行未编码，除非它是 [ RFC3986 ] 定义的 URI 中的保留字符或者该字符超出了非保留字符范围。

### 段落 19

**EN**

The match evaluates positively if and only if the end of the path from the rule is reached before a difference in octets is encountered.

**中文**

当且仅当在遇到八位字节差异之前到达规则路径的末尾时，匹配才会进行肯定评估。

### 段落 20

**EN**

¶ For example: ¶ +==================+=======================+=======================+ | Path | Encoded Path | Path to Match | +==================+=======================+=======================+ | /foo/bar?baz=quz | /foo/bar?baz=quz | /foo/bar?baz=quz | +------------------+-----------------------+-----------------------+ | /foo/bar?baz= | /foo/bar?baz= | /foo/bar?baz= | | https://foo.bar | https%3A%2F%2Ffoo.bar | https%3A%2F%2Ffoo.bar | +------------------+-----------------------+-----------------------+ | /foo/bar/ | /foo/bar/%E3%83%84 | /foo/bar/%E3%83%84 | | U+E38384 | | | +------------------+-----------------------+-----------------------

**中文**

¶ 例如： ¶ +==================+==========================+========================+ |路径|编码路径|匹配路径| +==================+========================+========================+ | /foo/bar?baz=quz | /foo/bar?baz=quz | /foo/bar?baz=quz | +------------------+------------------------------------+------------------------+ | /foo/bar?baz= | /foo/bar?baz= | /foo/bar?baz= | | https://foo.bar | https%3A%2F%2Ffoo.bar | https%3A%2F%2Ffoo.bar | https%3A%2F%2Ffoo.bar | https%3A%2F%2Ffoo.bar | +------------------+------------------------------------+------------------------+ | /foo/bar/ | /foo/bar/%E3%83%84 | /foo/bar/%E3%83%84 | /foo/bar/%E3%83%84 | /foo/bar/%E3%83%84 | | U+E38384 | | | +--------------------------------+------------------------------------+------------------------

### 段落 21

**EN**

+ | /foo/ | /foo/bar/%E3%83%84 | /foo/bar/%E3%83%84 | | bar/%E3%83%84 | | | +------------------+-----------------------+-----------------------+ | /foo/ | /foo/bar/%62%61%7A | /foo/bar/baz | | bar/%62%61%7A | | | +------------------+-----------------------+-----------------------+ Figure 4 : Examples of matching percent-encoded URI components The crawler SHOULD ignore "disallow" and "allow" rules that are not in any group (for example, any rule that precedes the first user-agent line).

**中文**

+ | /foo/| /foo/bar/%E3%83%84 | /foo/bar/%E3%83%84 | /foo/bar/%E3%83%84 | /foo/bar/%E3%83%84 | |条/%E3%83%84 | | | +------------------+------------------------------------+------------------------+ | /foo/ | /foo/bar/%62%61%7A | /foo/bar/%62%61%7A | /foo/bar/baz | |条/%62%61%7A | | | +------------------+------------------------------------+------------------------+ 图 4：匹配百分比编码的 URI 组件的示例 爬网程序应该忽略不在任何组中的“禁止”和“允许”规则（例如，第一个用户代理行之前的任何规则）。

### 段落 22

**EN**

¶ Implementors MAY bridge encoding mismatches if they detect that the robots.txt file is not UTF-8 encoded. ¶ 2.2.3. Special Characters Crawlers MUST support the following special characters: ¶ +===========+===================+==============================+ | Character | Description | Example | +===========+===================+==============================+ | # | Designates a line | allow: / # comment in line | | | comment. | | | | | # comment on its own line | +-----------+-------------------+------------------------------+ | $ | Designates the | allow: /this/path/exactly$ | | | end of the match | | | | pattern.

**中文**

¶ 如果实施者检测到 robots.txt 文件不是 UTF-8 编码，则可以桥接编码不匹配。 ¶ 2.2.3.特殊字符 爬虫必须支持以下特殊字符： ¶ +==========+====================+==============================+ |人物 |描述 |示例| +==========+====================+================================+ | ＃|指定一行 |允许: / # 行中的注释 | | |评论。 | | | | | # 在自己的行上发表评论 | +---------+--------------------+------------------------------+ | $ |指定 |允许：/this/path/exactly$ | | |比赛结束| | | |图案。

### 段落 23

**EN**

| | +-----------+-------------------+------------------------------+ | * | Designates 0 or | allow: /this/*/exactly | | | more instances of | | | | any character. | | +-----------+-------------------+------------------------------+ Figure 5 : List of special characters in robots.txt files If crawlers match special characters verbatim in the URI, crawlers SHOULD use "%" encoding.

**中文**

| | +---------+--------------------+------------------------------+ | * |指定 0 或 |允许：/这个/*/完全| | | | 更多实例| | |任何字符。 | | +---------+--------------------+------------------------------+ 图 5：robots.txt 文件中的特殊字符列表 如果爬虫在 URI 中逐字匹配特殊字符，则爬虫应该使用“%”编码。

### 段落 24

**EN**

For example: ¶ +============================+====================================+ | Percent-encoded Pattern | URI | +============================+====================================+ | /path/file-with-a-%2A.html | https://www.example.com/path/ | | | file-with-a-*.html | +----------------------------+------------------------------------+ | /path/foo-%24 | https://www.example.com/path/foo-$ | +----------------------------+------------------------------------+ Figure 6 : Example of percent-encoding 2.2.4. Other Records Crawlers MAY interpret other records that are not part of the robots.txt protocol -- for example, "Sitemaps" [ SITEMAPS ] .

**中文**

例如： ¶ +============================+======================================+ |百分比编码模式 |统一资源定位符 | +============================+======================================+ | /path/file-with-a-%2A.html | https://www.example.com/path/| | |文件-with-*.html | +----------------------------------------+------------------------------------+ | /路径/foo-%24 | https://www.example.com/path/foo-$ | https://www.example.com/path/foo-$ | +----------------------------------------+------------------------------------+ 图 6：百分比编码 2.2.4 的示例。其他记录爬虫可以解释不属于 robots.txt 协议的其他记录——例如，“站点地图”[SITEMAPS]。

### 段落 25

**EN**

Crawlers MAY be lenient when interpreting other records. For example, crawlers may accept common misspellings of the record. ¶ Parsing of other records MUST NOT interfere with the parsing of explicitly defined records in Section 2 . For example, a "Sitemaps" record MUST NOT terminate a group. ¶ 2.3. Access Method The rules MUST be accessible in a file named "/robots.txt" (all lowercase) in the top-level path of the service. The file MUST be UTF-8 encoded (as defined in [ RFC3629 ] ) and Internet Media Type "text/plain" (as defined in [ RFC2046 ] ).

**中文**

爬虫在解释其他记录时可能会很宽松。例如，爬虫可以接受记录的常见拼写错误。 ¶ 其他记录的解析不得干扰第 2 节中明确定义的记录的解析。例如，“站点地图”记录不得终止组。 ¶ 2.3。访问方法 必须可以在服务顶级路径中名为“/robots.txt”（全部小写）的文件中访问规则。文件必须采用 UTF-8 编码（如 [RFC3629] 中定义）且互联网媒体类型为“text/plain”（如 [RFC2046] 中定义）。

### 段落 26

**EN**

¶ As per [ RFC3986 ] , the URI of the robots.txt file is: ¶ "scheme:[//authority]/robots.txt" ¶ For example, in the context of HTTP or FTP, the URI is: ¶ https://www.example.com/robots.txt ftp://ftp.example.com/robots.txt ¶ 2.3.1. Access Results 2.3.1.1. Successful Access If the crawler successfully downloads the robots.txt file, the crawler MUST follow the parseable rules. ¶ 2.3.1.2. Redirects It's possible that a server responds to a robots.txt fetch request with a redirect, such as HTTP 301 or HTTP 302 in the case of HTTP.

**中文**

¶ 根据 [ RFC3986 ]，robots.txt 文件的 URI 为： ¶ "scheme:[//authority]/robots.txt" ¶ 例如，在 HTTP 或 FTP 上下文中，URI 为： ¶ https://www.example.com/robots.txt ftp://ftp.example.com/robots.txt ¶ 2.3.1.访问结果 2.3.1.1。成功访问如果爬虫成功下载robots.txt文件，则爬虫必须遵循可解析的规则。 ¶ 2.3.1.2。重定向 服务器可能会使用重定向来响应 robots.txt 获取请求，例如 HTTP 情况下的 HTTP 301 或 HTTP 302。

### 段落 27

**EN**

The crawlers SHOULD follow at least five consecutive redirects, even across authorities (for example, hosts in the case of HTTP). ¶ If a robots.txt file is reached within five consecutive redirects, the robots.txt file MUST be fetched, parsed, and its rules followed in the context of the initial authority. ¶ If there are more than five consecutive redirects, crawlers MAY assume that the robots.txt file is unavailable. ¶ 2.3.1.3. "Unavailable" Status "Unavailable" means the crawler tries to fetch the robots.txt file and the server responds with status codes indicating that the resource in question is unavailable.

**中文**

爬虫应该遵循至少五个连续的重定向，即使是跨权限的（例如，HTTP 情况下的主机）。 ¶ 如果在连续五个重定向内到达 robots.txt 文件，则必须获取、解析 robots.txt 文件，并在初始权限的上下文中遵循其规则。 ¶ 如果连续重定向超过五个，爬虫可能会假设 robots.txt 文件不可用。 ¶ 2.3.1.3。 “不可用”状态 “不可用”表示爬网程序尝试获取 robots.txt 文件，并且服务器以状态代码进行响应，表明相关资源不可用。

### 段落 28

**EN**

For example, in the context of HTTP, such status codes are in the 400-499 range. ¶ If a server status code indicates that the robots.txt file is unavailable to the crawler, then the crawler MAY access any resources on the server. ¶ 2.3.1.4. "Unreachable" Status If the robots.txt file is unreachable due to server or network errors, this means the robots.txt file is undefined and the crawler MUST assume complete disallow. For example, in the context of HTTP, server errors are identified by status codes in the 500-599 range.

**中文**

例如，在 HTTP 上下文中，此类状态代码在 400-499 范围内。 ¶ 如果服务器状态代码表明 robots.txt 文件对于爬网程序不可用，则爬网程序可以访问服务器上的任何资源。 ¶ 2.3.1.4。 “无法访问”状态 如果 robots.txt 文件由于服务器或网络错误而无法访问，则意味着 robots.txt 文件未定义，并且爬网程序必须假定完全禁止。例如，在 HTTP 上下文中，服务器错误由 500-599 范围内的状态代码标识。

### 段落 29

**EN**

¶ If the robots.txt file is undefined for a reasonably long period of time (for example, 30 days), crawlers MAY assume that the robots.txt file is unavailable as defined in Section 2.3.1.3 or continue to use a cached copy. ¶ 2.3.1.5. Parsing Errors Crawlers MUST try to parse each line of the robots.txt file. Crawlers MUST use the parseable rules. ¶ 2.4. Caching Crawlers MAY cache the fetched robots.txt file's contents. Crawlers MAY use standard cache control as defined in [ RFC9111 ] . Crawlers SHOULD NOT use the cached version for more than 24 hours, unless the robots.txt file is unreachable. ¶ 2.5.

**中文**

¶ 如果 robots.txt 文件在相当长的一段时间内（例如 30 天）未定义，爬虫可能会假定 robots.txt 文件不可用（如第 2.3.1.3 节中定义）或继续使用缓存的副本。 ¶ 2.3.1.5。解析错误 爬虫必须尝试解析 robots.txt 文件的每一行。爬虫必须使用可解析的规则。 ¶ 2.4。缓存爬虫可以缓存获取的 robots.txt 文件的内容。爬虫程序可以使用[RFC9111]中定义的标准缓存控制。爬网程序不应使用缓存版本超过 24 小时，除非 robots.txt 文件无法访问。 ¶ 2.5.

### 段落 30

**EN**

Limits Crawlers SHOULD impose a parsing limit to protect their systems; see Section 3 . The parsing limit MUST be at least 500 kibibytes [ KiB ] . ¶ 3. Security Considerations The Robots Exclusion Protocol is not a substitute for valid content security measures. Listing paths in the robots.txt file exposes them publicly and thus makes the paths discoverable. To control access to the URI paths in a robots.txt file, users of the protocol should employ a valid security measure relevant to the application layer on which the robots.txt file is served -for example, in the case of HTTP, HTTP Authentication as defined in [ RFC9110 ] .

**中文**

限制 爬虫应该施加解析限制以保护其系统；参见第 3 节。解析限制必须至少为 500 KB [KiB]。 ¶ 3. 安全注意事项 机器人排除协议不能替代有效的内容安全措施。在 robots.txt 文件中列出路径会公开它们，从而使路径可被发现。为了控制对 robots.txt 文件中 URI 路径的访问，协议的用户应采用与 robots.txt 文件所服务的应用程序层相关的有效安全措施 - 例如，在 HTTP 的情况下，使用 [RFC9110] 中定义的 HTTP 身份验证。

### 段落 31

**EN**

¶ To protect against attacks against their system, implementors of robots.txt parsing and matching logic should take the following considerations into account: ¶ Memory management: Section 2.5 defines the lower limit of bytes that must be processed, which inherently also protects the parser from out-of-memory scenarios. ¶ Invalid characters: Section 2.2 defines a set of characters that parsers and matchers can expect in robots.txt files. Out-of-bound characters should be rejected as invalid, which limits the available attack vectors that attempt to compromise the system.

**中文**

¶ 为了防止针对其系统的攻击，robots.txt 解析和匹配逻辑的实现者应考虑以下因素： ¶ 内存管理：第 2.5 节定义了必须处理的字节下限，这本质上也可以保护解析器免受内存不足情况的影响。 ¶ 无效字符：第 2.2 节定义了解析器和匹配器在 robots.txt 文件中可以预期的一组字符。越界字符应被视为无效而被拒绝，这限制了试图破坏系统的可用攻击媒介。

### 段落 32

**EN**

¶ Untrusted content: Implementors should treat the content of a robots.txt file as untrusted content, as defined by the specification of the application layer used. For example, in the context of HTTP, implementors should follow the Security Considerations section of [ RFC9110 ] . ¶ 4. IANA Considerations This document has no IANA actions. ¶ 5. Examples 5.1. Simple Example The following example shows: ¶ *: A group that's relevant to all user agents that don't have an explicitly defined matching group.

**中文**

¶ 不受信任的内容：实施者应将 robots.txt 文件的内容视为不受信任的内容，如所使用的应用程序层规范所定义。例如，在 HTTP 上下文中，实现者应遵循 [RFC9110] 的安全注意事项部分。 ¶ 4. IANA 考虑因素 本文档没有 IANA 行动。 ¶ 5. 示例 5.1。简单示例 以下示例显示： ¶ *：与没有显式定义的匹配组的所有用户代理相关的组。

### 段落 33

**EN**

It allows access to the URLs with the /publications/ path prefix, and it restricts access to the URLs with the /example/ path prefix and to all URLs with a .gif suffix. The "*" character designates any character, including the otherwise-required forward slash; see Section 2.2 . ¶ foobot: A regular case. A single user agent followed by rules. The crawler only has access to two URL path prefixes on the site -- /example/page.html and /example/allowed.gif. The rules of the group are missing the optional space character, which is acceptable as defined in Section 2.2 . ¶ barbot and bazbot: A group that's relevant for more than one user agent.

**中文**

它允许访问带有 /publications/ 路径前缀的 URL，并限制对带有 /example/ 路径前缀的 URL 和带有 .gif 后缀的所有 URL 的访问。 “*”字符指定任何字符，包括否则需要的正斜杠；参见第 2.2 节。 ¶ foobot：一个常规案例。遵循规则的单个用户代理。爬网程序只能访问网站上的两个 URL 路径前缀 - /example/page.html 和 /example/allowed.gif。该组的规则缺少可选的空格字符，根据第 2.2 节的定义，这是可以接受的。 ¶ barbot 和 bazbot：与多个用户代理相关的一组。

### 段落 34

**EN**

The crawlers are not allowed to access the URLs with the /example/page.html path prefix but otherwise have unrestricted access to the rest of the URLs on the site. ¶ quxbot: An empty group at the end of the file. The crawler has unrestricted access to the URLs on the site. ¶ User-Agent: * Disallow: *.gif$ Disallow: /example/ Allow: /publications/ User-Agent: foobot Disallow:/ Allow:/example/page.html Allow:/example/allowed.gif User-Agent: barbot User-Agent: bazbot Disallow: /example/page.html User-Agent: quxbot EOF ¶ 5.2. Longest Match The following example shows that in the case of two rules, the longest one is used for matching.

**中文**

爬网程序不允许访问带有 /example/page.html 路径前缀的 URL，但可以不受限制地访问网站上的其余 URL。 ¶ quxbot：文件末尾的空组。爬虫可以不受限制地访问网站上的 URL。 ¶ 用户代理：* 禁止：*.gif$ 禁止：/example/ 允许：/publications/ 用户代理：foobot 禁止：/ 允许：/example/page.html 允许：/example/allowed.gif 用户代理：barbot 用户代理：bazbot 禁止：/example/page.html 用户代理：quxbot EOF ¶ 5.2.最长匹配 下面的示例显示，在有两条规则的情况下，使用最长的一条进行匹配。

### 段落 35

**EN**

In the following case, /example/page/disallowed.gif MUST be used for the URI example.com/example/page/disallow.gif. ¶ User-Agent: foobot Allow: /example/page/ Disallow: /example/page/disallowed.gif ¶ 6. References 6.1. Normative References [RFC2046] Freed, N. and N. Borenstein , "Multipurpose Internet Mail Extensions (MIME) Part Two: Media Types" , RFC 2046 , DOI 10.17487/RFC2046 , November 1996 , < https://www.rfc-editor.org/info/rfc2046 > . [RFC2119] Bradner, S. , "Key words for use in RFCs to Indicate Requirement Levels" , BCP 14 , RFC 2119 , DOI 10.17487/RFC2119 , March 1997 , < https://www.rfc-editor.org/info/rfc2119 > .

**中文**

在以下情况下，/example/page/disallowed.gif 必须用于 URI example.com/example/page/disallow.gif。 ¶ 用户代理：foobot 允许：/example/page/ 不允许：/example/page/disallowed.gif ¶ 6. 参考文献 6.1。规范参考文献 [RFC2046] Freed, N. 和 N. Borenstein，“多用途 Internet 邮件扩展 (MIME) 第二部分：媒体类型”，RFC 2046，DOI 10.17487/RFC2046，1996 年 11 月，< https://www.rfc-editor.org/info/rfc2046 >。 [RFC2119] Bradner, S.，“RFC 中用于指示需求级别的关键字”，BCP 14，RFC 2119，DOI 10.17487/RFC2119，1997 年 3 月，< https://www.rfc-editor.org/info/rfc2119 >。

### 段落 36

**EN**

[RFC3629] Yergeau, F. , "UTF-8, a transformation format of ISO 10646" , STD 63 , RFC 3629 , DOI 10.17487/RFC3629 , November 2003 , < https://www.rfc-editor.org/info/rfc3629 > . [RFC3986] Berners-Lee, T. , Fielding, R. , and L. Masinter , "Uniform Resource Identifier (URI): Generic Syntax" , STD 66 , RFC 3986 , DOI 10.17487/RFC3986 , January 2005 , < https://www.rfc-editor.org/info/rfc3986 > . [RFC5234] Crocker, D., Ed. and P. Overell , "Augmented BNF for Syntax Specifications: ABNF" , STD 68 , RFC 5234 , DOI 10.17487/RFC5234 , January 2008 , < https://www.rfc-editor.org/info/rfc5234 > . [RFC8174] Leiba, B.

**中文**

[RFC3629] Yergeau, F.，“UTF-8，ISO 10646 的转换格式”，STD 63，RFC 3629，DOI 10.17487/RFC3629，2003 年 11 月，< https://www.rfc-editor.org/info/rfc3629 >。 [RFC3986] Berners-Lee, T.、Fielding, R. 和 L. Masinter，“统一资源标识符 (URI)：通用语法”，STD 66，RFC 3986，DOI 10.17487/RFC3986，2005 年 1 月，< https://www.rfc-editor.org/info/rfc3986 > . [RFC5234] 克罗克，D.，编辑。和 P. Overell，“语法规范的增强 BNF：ABNF”，STD 68，RFC 5234，DOI 10.17487/RFC5234，2008 年 1 月，< https://www.rfc-editor.org/info/rfc5234 >。 [RFC8174] 莱巴，B.

### 段落 37

**EN**

, "Ambiguity of Uppercase vs Lowercase in RFC 2119 Key Words" , BCP 14 , RFC 8174 , DOI 10.17487/RFC8174 , May 2017 , < https://www.rfc-editor.org/info/rfc8174 > . [RFC8288] Nottingham, M. , "Web Linking" , RFC 8288 , DOI 10.17487/RFC8288 , October 2017 , < https://www.rfc-editor.org/info/rfc8288 > . [RFC9110] Fielding, R., Ed. , Nottingham, M., Ed. , and J. Reschke, Ed. , "HTTP Semantics" , STD 97 , RFC 9110 , DOI 10.17487/RFC9110 , June 2022 , < https://www.rfc-editor.org/info/rfc9110 > . [RFC9111] Fielding, R., Ed. , Nottingham, M., Ed. , and J. Reschke, Ed.

**中文**

，“RFC 2119 关键字中大写与小写的歧义”，BCP 14，RFC 8174，DOI 10.17487/RFC8174，2017 年 5 月，< https://www.rfc-editor.org/info/rfc8174 >。 [RFC8288] 诺丁汉，M.，“网络链接”，RFC 8288，DOI 10.17487/RFC8288，2017 年 10 月，< https://www.rfc-editor.org/info/rfc8288 >。 [RFC9110] 菲尔丁，R.，编辑。，诺丁汉，M.，埃德。，和 J. Reschke，埃德。，“HTTP 语义”，STD 97，RFC 9110，DOI 10.17487/RFC9110，2022 年 6 月，< https://www.rfc-editor.org/info/rfc9110 >。 [RFC9111] 菲尔丁，R.，编辑。，诺丁汉，M.，埃德。，和 J. Reschke，埃德。

### 段落 38

**EN**

, "HTTP Caching" , STD 98 , RFC 9111 , DOI 10.17487/RFC9111 , June 2022 , < https://www.rfc-editor.org/info/rfc9111 > . 6.2. Informative References [KiB] "Kibibyte" , Simple English Wikipedia, the free encyclopedia , 17 September 2020 , < https://simple.wikipedia.org/wiki/Kibibyte > . [ROBOTSTXT] "The Web Robots Pages (including /robots.txt)" , 2007 , < https://www.robotstxt.org/ > . [SITEMAPS] "What are Sitemaps? (Sitemap protocol)" , April 2020 , < https://www.sitemaps.org/index.html > .

**中文**

，“HTTP 缓存”，STD 98，RFC 9111，DOI 10.17487/RFC9111，2022 年 6 月，< https://www.rfc-editor.org/info/rfc9111 >。 6.2.信息参考文献 [KiB]“Kibibyte”，简单英语维基百科，免费百科全书，2020 年 9 月 17 日，< https://simple.wikipedia.org/wiki/Kibibyte >。 [ROBOTSTXT]“Web 机器人页面（包括 /robots.txt）”，2007 年，< https://www.robotstxt.org/>。 [SITEMAPS]“什么是 Sitemap？（Sitemap 协议）”，2020 年 4 月，< https://www.sitemaps.org/index.html >。

### 段落 39

**EN**

Authors' Addresses Martijn Koster Stalworthy Manor Farm Suton Lane Wymondham, Norfolk NR18 9JG United Kingdom Email: m.koster@greenhills.co.uk Gary Illyes Google LLC Brandschenkestrasse 110 CH- 8002 Zürich Switzerland Email: garyillyes@google.com Henner Zeller Google LLC 1600 Amphitheatre Pkwy Mountain View , CA 94043 United States of America Email: henner@google.com Lizzi Sassman Google LLC Brandschenkestrasse 110 CH- 8002 Zürich Switzerland Email: lizzi@google.com

**中文**

作者地址 Martijn Koster Stalworthy Manor Farm Suton Lane Wymondham, Norfolk NR18 9JG United Kingdom 电子邮件：m.koster@greenhills.co.uk Gary Illyes Google LLC Brandschenkestrasse 110 CH- 8002 Zürich Switzerland 电子邮件：garyillyes@google.com Henner Zeller Google LLC 1600 Amphitheatre Pkwy Mountain View , CA 94043 美国 电子邮件：henner@google.com Lizzi Sassman Google LLC Brandschenkestrasse 110 CH- 8002 Zürich Switzerland 电子邮件：lizzi@google.com
