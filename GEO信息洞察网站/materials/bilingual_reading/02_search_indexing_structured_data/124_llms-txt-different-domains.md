# llms.txt - Different domains

- ID: 124
- 类型: html
- 分类: 02_search_indexing_structured_data
- 主题: LLM可读内容
- 原文链接: https://llmstxt.org/domains.html
- 翻译说明: 英中翻译优先由在线机器翻译批量生成，失败段落回退本地 Argos Translate，并做了GEO术语后处理；建议重要引用仍回看原文。

## 段落对照

### 段落 1

**EN**

domains – llms-txt llms-txt Tutorials llms.txt in Different Domains The /llms.txt file Code Python module & CLI Python source JavaScript Editors and IDEs ed , the standard text editor Tutorials llms.txt in Different Domains How to help LLMs understand your nbdev project On this page llms.txt in Different Domains Restaurants Report an issue Other Formats CommonMark Tutorials llms.txt in Different Domains llms.txt in Different Domains This page has some guidelines and suggestions for how different domains could utilize llms.txt to allow LLMs to better interface with their site if they so choose.

**中文**

域 – llms-txt llms-txt 教程 不同域中的 llms.txt /llms.txt 文件 代码 Python 模块和 CLI Python 源代码 JavaScript 编辑器和 IDE ed，标准文本编辑器 教程 不同域中的 llms.txt 如何帮助 LLM 理解您的 nbdev 项目 本页 不同域中的 llms.txt 餐厅 报告问题 其他格式 CommonMark 教程 不同域中的 llms.txt 不同域中的 llms.txt 这页面提供了一些关于不同域如何利用 llms.txt 来允许法学硕士更好地与其网站交互的指南和建议（如果他们愿意的话）。

### 段落 2

**EN**

Remember, when constructing your llms.txt you should “use concise, clear language. When linking to resources, include brief, informative descriptions. Avoid ambiguous terms or unexplained jargon.” Additionally, the best way to determine if your llms.txt works well with LLMs is to test it with them!

**中文**

请记住，在构建 llms.txt 时，您应该“使用简洁、清晰的语言。链接到资源时，包括简短、信息丰富的描述。避免模棱两可的术语或无法解释的行话。”此外，确定您的 llms.txt 是否适用于 LLM 的最佳方法是使用它们进行测试！

### 段落 3

**EN**

Here is a minimal way to test Anthropic’s Claude against your llms.txt : # /// script # requires-python = ">=3.8" # dependencies = [ # "claudette", # "llms-txt", # "requests", # ] # /// from claudette import * from llms_txt import create_ctx import requests model = models[ 1 ] # Sonnet 3.5 chat = Chat(model, sp = """You are a helpful and concise assistant.""" ) url = 'your_url/llms.txt' text = requests.get(url).text llm_ctx = create_ctx(text) chat(llm_ctx + ' \n\n The above is necessary context for the conversation.' ) while True : msg = input ( 'Your question about the site: ' ) res = chat(msg) print ( 'From Claude:' , contents(res)) The above script utilizes the relatively new uv syntax for python scripts.

**中文**

以下是根据 llms.txt 测试 Anthropic 的 Claude 的最小方法： # /// script # require-python = ">=3.8" # dependency = [ # "claudette", # "llms-txt", # "requests", # ] # /// from claudette import * from llms_txt import create_ctx import requests model = models[ 1 ] # Sonnet 3.5 chat = Chat(model, sp = """你是一位乐于助人且简洁的助手。""" ) url = 'your_url/llms.txt' text = requests.get(url).text llm_ctx = create_ctx(text) chat(llm_ctx + ' \n\n 以上是对话的必要上下文。' ) while True : msg = input ( '您关于网站的问题： ' ) res = chat(msg) print ( 'From Claude:' , content(res)) 上面的脚本使用了相对较新的 python 脚本 uv 语法。

### 段落 4

**EN**

If you install uv , you can simply run the above script with uv run test_llms_txt.py and it will handle installing the necessary library dependencies in an isolated python environment. Else you can install the requirements manually and run it like any ordinary python script with python test_llms_txt.py . Restaurants Here is an example llms.txt that a restaurant could construct for consumption by LLMs: # Nate the Great's Grill > Nate the Great's Grill is a popular destination off of Sesame Street that has been serving the community for over 20 years. We offer the best BBQ for a great price.

**中文**

如果安装 uv，则只需使用 uv run test_llms_txt.py 运行上述脚本，它将在隔离的 python 环境中安装必要的库依赖项。否则，您可以手动安装要求并像任何普通 python 脚本一样使用 python test_llms_txt.py 运行它。餐馆 以下是餐馆可以构建供法学硕士消费的 llms.txt 示例： # Nate the Great's Grill > Nate the Great's Grill 是芝麻街附近的一个热门目的地，已为社区服务了 20 多年。我们以优惠的价格提供最好的烧烤。

### 段落 5

**EN**

Here are our weekly hours: - Monday - Friday: 9am - 9pm - Saturday: 11am - 9pm - Sunday: Closed ## Menus - [Lunch Menu](https://host/lunch.html.md): Our lunch menu served from 11am to 4pm every day. - [Dinner Menu](https://host/dinner.html.md): Our dinner menu served from 4pm to 9pm every day.

**中文**

以下是我们每周的营业时间： - 周一至周五：上午 9 点至晚上 9 点 - 周六：上午 11 点至晚上 9 点 - 周日：休息 ## 菜单 - [午餐菜单](https://host/lunch.html.md)：我们的午餐菜单每天上午 11 点至下午 4 点供应。 - [晚餐菜单](https://host/dinner.html.md): 我们的晚餐菜单每天下午 4 点至 9 点供应。

### 段落 6

**EN**

## Optional - [Dessert Menu](https://host/dessert.md): A subset of the Starlette docs And here is an example lunch menu taken from Franklin’s BBQ : ## By The Pound | Item | Price | | -------------- | ----------- | | Brisket | 34 | | Pork Spare Ribs | 30 | | Pulled Pork | 28 | ## Drinks | Item | Price | | -------------- | ----------- | | Iced Tea | 3 | | Mexican Coke | 3 | ## Sides | Item | Price | | -------------- | ----------- | | Potato Salad | 4 | | Slaw | 4 | Report an issue

**中文**

## 可选 - [甜点菜单](https://host/dessert.md)：Starlette 文档的子集 以下是取自 Franklin’s BBQ 的午餐菜单示例：## 按磅 |项目 |价格| | -------------- | ----------- | |牛胸肉| 34 | 34 |排骨| 30| |手撕猪肉| 28 | 28 ## 饮料 |项目 |价格| | -------------- | ----------- | |冰茶| 3 | |墨西哥可乐| 3 | ## 双方 |项目 |价格| | -------------- | ----------- | |土豆沙拉| 4 | |色拉| 4 |报告问题
