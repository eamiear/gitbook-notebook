# 配置

GitBook 通过 `book.json` 文件进行图书配置。

### 常规配置

| 变量 | 描述 |
| -------- | ----------- |
| `root` | 包含所有图书文件的根目录路径, `book.json` 除外|
| `structure` | 定义 `Readme`, `Summary`, `Glossary` 路径. |
| `title` | 图书标题，默认从README.md中提取. |
| `description` | 图书简介，默认从README中提取 |
| `author` | 图书作者 |
| `isbn` | 图书 ISBN |
| `language` | 图书语言 |
| `direction` | 文本方向( `rtl` 或 `ltr`), 默认由图书语言决定 |
| `gitbook` | `gitbook`  |

### 插件

| 变量 | 描述 |
| -------- | ----------- |
| `plugins` | 插件列表 |
| `pluginsConfig` |插件配置 |

### 结构

除根 (`root`) 变量外，可以指定`Readme`, `Summary`， `Glossary`, `languages`的文件名称，以修改 `GitBook` 默认文件名。这些文件需要放在图书根目录下。

| 变量 | 描述 |
| -------- | ----------- |
| `structure.readme` | Readme文件名 (默认是 `README.md`) |
| `structure.summary` | Summary文件名 (默认`SUMMARY.md`) |
| `structure.glossary` | Glossary文件名 (默认 `GLOSSARY.md`) |
| `structure.languages` | Languages文件名 (默认 `LANGS.md`) |

### PDF选项

可对导出的PDF进行属性配置

| 变量 | 描述 |
| -------- | ----------- |
| `pdf.pageNumbers` | 每页添加页数 (默认 `true`) |
| `pdf.fontSize` | 基本的字体大小 (默认 `12`) |
| `pdf.fontFamily` | 基本字体系列 (默认 `Arial`) |
| `pdf.paperSize` | 纸张大小, 可选项有`'a0', 'a1', 'a2', 'a3', 'a4', 'a5', 'a6', 'b0', 'b1', 'b2', 'b3', 'b4', 'b5', 'b6', 'legal', 'letter'` (默认 `a4`) |
| `pdf.margin.top` | 顶部边距 (默认 `56`) |
| `pdf.margin.bottom` | 底部边距 (默认`56`) |
| `pdf.margin.right` | 右边距 (默认 `62`) |
| `pdf.margin.left` | 左边距 (默认 `62`) |