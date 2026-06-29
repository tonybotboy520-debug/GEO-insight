# GEO信息洞察网站

这是一个可独立移动和打开的网站包，包含 GEO 信息洞察页面、统一中英对照阅读页、页面数据和对应的中英对照 MD 资料。

## 如何打开

- 直接打开 `index.html` 可以浏览 GEO 信息洞察首页。
- 首页搜索框右侧的“分类”支持多选筛选，并显示每个分类下的资料数量。
- 点击首页里的“中英对照阅读”会进入 `reader.html`，并按资料 ID 动态加载对应 MD，以带轻分隔的高密度连续文本流呈现：一段原文后紧跟一段中文译文。阅读页顶部会显示标题、译题和来源等资料信息。
- 如果通过本地 HTTP 服务打开，阅读页会优先读取 `materials/bilingual_reading` 下的实时 MD 文件。
- 如果直接用 `file://` 打开，阅读页会使用 `assets/data/bilingual-reader-data.js` 里的兜底数据，避免浏览器拦截本地 MD 读取。

## 目录说明

- `index.html`: GEO 信息洞察首页，也是网站入口。
- `reader.html`: 统一中英对照阅读页，文章和论文共用这一页。
- `assets/data/geo-insights.js`: 首页使用的文章、论文、观点摘要数据。
- `assets/data/bilingual-reader-data.js`: 阅读页本地打开时使用的 MD 内容兜底数据。
- `materials/bilingual_reading/`: 中英对照 MD 原文、分类目录和资料索引。
- `materials/weekly_monitoring_sources.md`: 每周固定监控来源清单，覆盖论文、官方文档、行业研究、GEO 工具博客和中文工程来源。

## 维护提醒

如果后续修改了 `materials/bilingual_reading` 里的 MD 文件，并且需要继续支持直接 `file://` 打开，请重新生成 `assets/data/bilingual-reader-data.js`。

## 每周更新流程

每周按 `materials/weekly_monitoring_sources.md` 检查新增内容。若发现新的 GEO / AI Search / AEO / RAG citation / AI visibility 相关资料：

1. 先用 URL、标题、arXiv ID 去重。
2. 生成摘要重点、GEO 相关观点、1-5 条核心观点、标签和分类。
3. 英文资料生成逐段中英对照；纯中文资料不重复翻译。
4. 新增双语 MD 到 `materials/bilingual_reading/`。
5. 同步更新 `assets/data/geo-insights.js`、`assets/data/bilingual-reader-data.js` 和 `materials/bilingual_reading/bilingual_index.json`。
6. 检查首页“中英对照阅读”和“原文链接”都可打开。
